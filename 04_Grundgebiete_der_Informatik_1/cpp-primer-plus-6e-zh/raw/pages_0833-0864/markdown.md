再假设有如下代码:

```txt
Someclass sc;
sc.redo(5);
```

int 值 5 将被提升为 5.0，进而执行方法 redo()。

现在假设将 Someclass 类的定义改成了下面这样:

```matlab
class Someclass
{
public:
...
    void redo(double);
    void redo(int) = delete;
...
};
```

在这种情况下，方法调用 sc.redo(5)与原型 redo(int) 匹配。编译器检测到这一点以及 redo(int) 被禁用后，将这种调用视为编译错误。这说明了禁用函数的重要一点:它们只用于查找匹配函数，使用它们将导致编译错误。

## 18.3.3 委托构造函数

如果给类提供了多个构造函数，您可能重复编写相同的代码。也就是说，有些构造函数可能需要包含其他构造函数中已有的代码。为让编码工作更简单、更可靠，C++11允许您在一个构造函数的定义中使用另一个构造函数。这被称为委托，因为构造函数暂时将创建对象的工作委托给另一个构造函数。委托使用成员初始化列表语法的变种:

```cpp
class Notes {
    int k;
    double x;
    std::string st;
public:
    Notes();
    Notes(int);
    Notes(int, double);
    Notes(int, double, std::string);
};
Notes::Notes(int kk, double xx, std::string stt) : k(kk),
        x(xx), st(stt) {/*do stuff*/}
Notes::Notes() : Notes(0, 0.01, "Oh") {/* do other stuff*/}
Notes::Notes(int kk) : Notes(kk, 0.01, "Ah") {/* do yet other stuff*/ }
Notes::Notes( int kk, double xx ) : Notes(kk, xx, "Uh") {/* ditto*/ }
```

例如，上述默认构造函数使用第一个构造函数初始化数据成员并执行其函数体，然后再执行自己的函数体。

## 18.3.4 继承构造函数

为进一步简化编码工作，C++11 提供了一种让派生类能够继承基类构造函数的机制。C++98 提供了一种让名称空间中函数可用的语法:

```txt
namespace Box
{
    int fn(int) { ... }
    int fn(double) { ... }
    int fn(const char *) { ... }
}
using Box::fn;
```

这让函数 fn 的所有重载版本都可用。也可使用这种方法让基类的所有非特殊成员函数对派生类可用。

例如，请看下面的代码:

```cpp
class C1
{
...
public:
...
    int fn(int j) { ... }
    double fn(double w) { ... }
    void fn(const char * s) { ... }
};
class C2 : public C1
{
...
public:
...
    using C1::fn;
    double fn(double) { ... };
};
...
C2 c2;
int k = c2.fn(3);      // uses C1::fn(int)
double z = c2.fn(2.4);  // uses C2::fn(double)
```

C2 中的 using 声明让 C2 对象可使用 C1 的三个 fn() 方法，但将选择 C2 而不是 C1 定义的方法 fn(double)。

C++11 将这种方法用于构造函数。这让派生类继承基类的所有构造函数（默认构造函数、复制构造函数和移动构造函数除外），但不会使用与派生类构造函数的特征标匹配的构造函数:

```cpp
class BS
{
    int q;
    double w;
public:
    BS() : q(0), w(0) {}
    BS(int k) : q(k), w(100) {}
    BS(double x) : q(-1), w(x) {}
    B0(int k, double x) : q(k), w(x) {}
    void Show() const {std::cout << q <<", " << w << '\n';}
};

class DR : public BS
{
    short j;
public:
    using BS::BS;
    DR() : j(-100) {}      // DR needs its own default constructor
    DR(double x) : BS(2*x), j(int(x)) {}
    DR(int i) : j(-2), BS(i, 0.5* i) {}
    void Show() const {std::cout << j << ", "; BS::Show();}
};
int main()
{
    DR o1;          // use DR()
    DR o2(18.81);   // use DR(double) instead of BS(double)
    DR o3(10, 1.8); // use BS(int, double)
    ...
}
```

由于没有构造函数 DR(int, double)，因此创建 DR 对象 o3 时，将使用继承而来的 BS(int, double)。请注意，继承的基类构造函数只初始化基类成员；如果还要初始化派生类成员，则应使用成员列表初始化语法:

```txt
DR(int i, int k, double x) : j(i), BS(k,x) {}
```

## 18.3.5 管理虚方法: override 和 final

虚方法对实现多态类层次结构很重要，让基类引用或指针能够根据指向的对象类型调用相应的方法，但虚方法也带来了一些编程陷阱。例如，假设基类声明了一个虚方法，而您决定在派生类中提供不同的版本，这将覆盖旧版本。但正如第13章讨论的，如果特征标不匹配，将隐藏而不是覆盖旧版本:

```cpp
class Action
{
    int a;
public:
    Action(int i = 0) : a(i) {}
    int val() const {return a;};
    virtual void f(char ch) const { std::cout << val() << ch << "\n";}
};
class Bingo : public Action
{
public:
    Bingo(int i = 0) : Action(i) {}
    virtual void f(char * ch) const { std::cout << val() << ch << "!\n"; }
};
```

由于类 Bingo 定义的是 f(char \* ch) 而不是 f(char ch)，将对 Bingo 对象隐藏 f(char ch)，这导致程序不能使用类似于下面的代码:

```javascript
Bingo b(10);
b.f('@');  // works for Action object, fails for Bingo object
```

在 C++11 中，可使用虚说明符 override 指出您要覆盖一个虚函数:将其放在参数列表后面。如果声明与基类方法不匹配，编译器将视为错误。因此，下面的 Bingo::f() 版本将生成一条编译错误消息:

```cpp
virtual void f(char * ch) const override { std::cout << val()
                        << ch  << "!\n"; }
```

例如，在 Microsoft Visual C++ 2010 中，出现的错误消息如下:

```txt
method with override specifier 'override' did not override any base class methods
```

说明符 final 解决了另一个问题。您可能想禁止派生类覆盖特定的虚方法，为此可在参数列表后面加上 final。例如，下面的代码禁止 Action 的派生类重新定义函数 f():

```cpp
virtual void f(char ch) const final { std::cout << val() << ch << "\n";}
```

说明符 override 和 final 并非关键字，而是具有特殊含义的标识符。这意味着编译器根据上下文确定它们是否有特殊含义:在其他上下文中，可将它们用作常规标识符，如变量名或枚举。

## 18.4 Lambda 函数

见到术语 lambda 函数（也叫 lambda 表达式，常简称为 lambda）时，您可能怀疑 C++11 添加这项新功能旨在帮助编程新手。看到下面的 lambda 函数示例后，您可能坚定了自己的怀疑:

```javascript
[&count](int x){count += (x % 13 == 0);}
```

但 lambda 函数并不像看起来那么晦涩难懂，它们提供了一种有用的服务，对使用函数谓词的 STL 算

法来说尤其如此。

## 18.4.1 比较函数指针、函数符和 Lambda 函数

来看一个示例，它使用三种方法给 STL 算法传递信息:函数指针、函数符和 lambda。出于方便的考虑，将这三种形式通称为函数对象，以免不断地重复“函数指针、函数符或 lambda”。假设您要生成一个随机整数列表，并判断其中多少个整数可被 3 整除，多个少整数可被 13 整除。

生成这样的列表很简单。一种方案是，使用 vector&lt;int&gt;存储数字，并使用 STL 算法 generate() 在其中填充随机数:

```cpp
#include <vector>
#include <algorithm>
#include <cmath>
...
std::vector<int>-numbers(1000);
std::generate(vector.begin(), vector.end(), std::rand);
```

函数 generate() 接受一个区间(由前两个参数指定)，并将每个元素设置为第三个参数返回的值，而第三个参数是一个不接受任何参数的函数对象。在上述示例中，该函数对象是一个指向标准函数 rand() 的指针。

通过使用算法 count\_if()，很容易计算出有多少个元素可被 3 整除。与函数 generate()一样，前两个参数应指定区间，而第三个参数应是一个返回 true 或 false 的函数对象。函数 count\_if() 计算这样的元素数，即它使得指定的函数对象返回 true。为判断元素能否被 3 整除，可使用下面的函数定义:

```txt
bool f3(int x) {return x % 3 == 0;}
```

同样，为判断元素能否被13整除，可使用下面的函数定义——

```txt
bool f13(int x)—{return x % 13 == 0;}
```

定义上述函数后，便可计算复合条件的元素数了，如下所示:

```cpp
int count3 = std::count_if(numbers.begin(), numbers.end(); f3);
cout << "Count_of_numbers_divisible by 3:" << count3 << '\n';
int_count13 = std::count_if(numbers.begin(), numbers.end(), f13);
cout << "Count_of_numbers_divisible by 13:" << count13 << "\n\n";
```

下面复习一下如何使用函数符来完成这个任务。第16章介绍过，函数符是一个类对象，并非只能像函数名那样使用它，这要归功于类方法 operator()()。就这个示例而言，函数符的优点之一是，可使用同一个函数符来完成这两项计数任务。下面是一种可能的定义:

```cpp
class f_mod
{
private:
    int dv;
public:
    f_mod(int d = 1) : dv(d) {}
    bool operator() (int x) {return x & dv == 0;}
};
```

这为何可行呢？因为可使用构造函数创建存储特定整数值的f mod对象:

```txt
f_mod obj(3); // f_mod.dv set to 3
```

而这个对象可使用方法 operator() 来返回一个 bool 值:

```txt
bool is_div_by_3 = obj(7); // same as obj.operator(7)(7)-
```

构造函数本身可用作诸如 count\_if() 等函数的参数:

```txt
count3 = std::count_if(numbers.begin(F), numbers.end(), f_mod(3));
```

参数 f\_mod(3) 创建一个对象，它存储了值 3；而 count\_if() 使用该对象来调用 operator()()，并将参数 x 设置为 numbers 的一个元素。要计算有多少个数字可被 13（而不是 3）整除，只需将第三个参数设置为 f\_mod(3)。

最后，来看看使用 lambda 的情况。名称 lambda 来自 lambda calculus（λ 演算）——一种定义和应用函数的数学系统。这个系统让您能够使用匿名函数——即无需给函数命名。在 C++11 中，对于接受函数指针或函数符的函数，可使用匿名函数定义（lambda）作为其参数。与前述函数 f3() 对应的 lambda 如下:

```lisp
[] (int x) {return x % 3 == 0;}
```

这与f3()的函数定义很像:

```txt
bool f3(int x) {return x % 3 == 0;}
```

差别有两个:使用[]替代了函数名（这就是匿名的由来）；没有声明返回类型。返回类型相当于使用decltype 根据返回值推断得到的，这里为 bool。如果 lambda 不包含返回语句，推断出的返回类型将为 void。就这个示例而言，您将以如下方式使用该 lambda:

```txt
count3 = std::count_if(numbers.begin(), numbers.end(),
         [](int x){return x % 3 == 0;});
```

也就是说，使用使用整个 lambad 表达式替换函数指针或函数符构造函数。

仅当 lambad 表达式完全由一条返回语句组成时，自动类型推断才管用；否则，需要使用新增的返回类型后置语法:

```txt
[] (double x)->double{int y = x; return x - y;}  // return type is double
```

程序清单 18.4 演示了前面讨论的各个要点。

程序清单 18.4 lambda0.cpp

```cpp
// lambda0.cpp -- using lambda expressions
#include <iostream>
#include <vector>
#include <algorithm>
#include <cmath>
#include <ctime>
const long Size1 = 39L;
const long Size2 = 100*Size1;
const long Size3 = 100*Size2;
bool f3(int x) {return x % 3 == 0;}
bool f13(int x) {return x % 13 == 0;}

int main()
{
    using std::cout;
    std::vector<int> numbers(Size1);

    std::srand(std::time(0));
    std::generate(numbers.begin(), numbers.end(), std::rand);

// using function pointers
    cout << "Sample size = " << Size1 << '\n';

    int count3 = std::count_if(numbers.begin(), numbers.end(), f3);
    cout << "Count of numbers divisible by 3: " << count3 << '\n';
    int count13 = std::count_if(numbers.begin(), numbers.end(), f13);
    cout << "Count of numbers divisible by 13: " << count13 << "\n\n";

// increase number of numbers
```

```cpp
numbers.resize(Size2);
std::generate(numbers.begin(), numbers.end(), std::rand);
cout << "Sample size = " << Size2 << '\n';
// using a functor
class f_mod
{
private:
    int dv;
public:
    f_mod(int d = 1) : dv(d) {}
    bool operator()(int x) {return x % dv == 0;}
};

count3 = std::count_if(numbers.begin(), numbers.end(), f_mod(3));
cout << "Count of numbers divisible by 3: " << count3 << '\n';
count13 = std::count_if(numbers.begin(), numbers.end(), f_mod(13));
cout << "Count of numbers divisible by 13: " << count13 << "\n\n";

// increase number of numbers again
numbers.resize(Size3);
std::generate(numbers.begin(), numbers.end(), std::rand);
cout << "Sample size = " << Size3 << '\n';
// using lambdas
count3 = std::count_if(numbers.begin(), numbers.end(),
            [](int x){return x % 3 == 0;});
cout << "Count of numbers divisible by 3: " << count3 << '\n';
count13 = std::count_if(numbers.begin(), numbers.end(),
            [](int x){return x % 13 == 0;});
cout << "Count of numbers divisible by 13: " << count13 << '\n';

return 0;
}
```

下面是该程序的输出示例:

```txt
Sample size = 39
Count of numbers divisible by 3: 15
Count of numbers divisible by 13: 6

Sample size = 3900
Count of numbers divisible by 3: 1305
Count of numbers divisible by 13: 302

Sample size = 390000
Count of numbers divisible by 3: 130241

    Count of numbers divisible by 13: 29860
```

输出表明，样本很小时，得到的统计数据并不可靠。

## 18.4.2 为何使用 lambda

您可能会问，除那些表达式狂热爱好者，谁会使用 lambda 呢？下面从 4 个方面探讨这个问题:距离、简洁、效率和功能。

很多程序员认为，让定义位于使用的地方附近很有用。这样，就无需翻阅多页的源代码，以了解函数调用 count\_if() 的第三个参数了。另外，如果需要修改代码，涉及的内容都将在附近；而剪切并粘贴代码以便在其他地方使用时，涉及的内容也在一起。从这种角度看，lambda 是理想的选择，因为其定义和使用是在同一个地方进行的；而函数是最糟糕的选择，因为不能在函数内部定义其他函数，因此函数的定义可能离使用它的地方很远。函数符是不错的选择，因为可在函数内部定义类（包含函数符类），因此定义离使用地点可以很近。

从简洁的角度看，函数符代码比函数和 lambda 代码更繁琐。函数和 lambda 的简洁程度相当，一个显而易见的例外是，需要使用同一个 lambda 两次:

```cpp
count1 = std::count_if(n1.begin(), n1.end(),
         [](int x){return x % 3 == 0;});
count2 = std::count_if(n2.begin(), n2.end(),
         [](int x){return x % 3 == 0;});
```

但并非必须编写 lambda 两次，而可给 lambda 指定一个名称，并使用该名称两次:

```cpp
auto mod3 = [](int x){return x % 3 == 0;}  // mod3 a name for the lambda
count1 = std::count_if(n1.begin(), n1.end(), mod3);
count2 = std::count_if(n2.begin(), n2.end(), mod3);
```

您甚至可以像使用常规函数那样使用有名称的 lambda:

```txt
bool result = mod3(z); // result is true if z % 3 == 0
```

然而，不同于常规函数，可在函数内部定义有名称的 lambda。mod3 的实际类型随实现而异，它取决于编译器使用什么类型来跟踪 lambda。

这三种方法的相对效率取决于编译器内联那些东西。函数指针方法阻止了内联，因为编译器传统上不会内联其地址被获取的函数，因为函数地址的概念意味着非内联函数。而函数符和 lambda 通常不会阻止内联。

最后，lambda 有一些额外的功能。具体地说，lambad 可访问作用域内的任何动态变量；要捕获要使用的变量，可将其名称放在中括号内。如果只指定了变量名，如[z]，将按值访问变量；如果在名称前加上&，如[&count]，将按引用访问变量。[&]让您能够按引用访问所有动态变量，而[=]让您能够按值访问所有动态变量。还可混合使用这两种方式，例如，[ted, &ed]让您能够按值访问 ted 以及按引用访问 ed，[&, ted]让您能够按值访问 ted 以及按引用访问其他所有动态变量，[=, &ed]让您能够按引用访问 ed 以及按值访问其他所有动态变量。在程序清单 18.4 中，可将下述代码:

```txt
int count13;
...
count13 = std::count_if(numbers.begin(), numbers.end(),
            [](int x){return x % 13 == 0;});
```

替换为如下代码:

```cpp
int count13 = 0;
std::for_each(numbers.begin(), numbers.end(),
        [&count13](int x){count13 += x % 13 == 0;});
```

[&count13]让 lambda 能够在其代码中使用 count13。由于 count13 是按引用捕获的，因此在 lambda 对 count13 所做的任何修改都将影响原始 count13。如果 x 能被 13 整除，则表达式 x % 13 = 0 将为 true，添加到 count13 中时，true 将被转换为 1。同样，false 将被转换为 0。因此，for\_each() 将 lambda 应用于 numbers 的每个元素后，count13 将为能被 13 整除的元素数。

通过利用这种技术，可使用一个 lambda 表达式计算可被 3 整除的元素数和可被 13 整除的元素数:

```txt
int count3 = 0;
int count13 = 0;
std::for_each(numbers.begin(), numbers.end(),
    [&](int x){count3 += x % 3 == 0; count13 += x % 13 == 0;});
```

在这里，[&]让您能够在 lambad 表达式中使用所有的自动变量，包括 count3 和 count13。

程序清单 18.5 演示了如何使用这些技术。

程序清单 18.5 lambda1.cpp

```cpp
//lambda1.cpp -- use captured variables
#include <iostream>
#include <vector>
#include <algorithm>
#include <cmath>
#include <ctime>
const long Size = 390000L;

int main(){
    using std::cout;
    std::vector<int> numbers(Size);

    std::srand(std::time(0));
    std::generate(numbers.begin(), numbers.end(), std::rand);
    cout << "Sample size = " << Size << '\n';
// using lambdas
    int count3 = std::count_if(numbers.begin(), numbers.end(),
        [](int x){return x % 3 == 0;}};
    cout << "Count of numbers divisible by 3: " << count3 << '\n';
    int count13 = 0;
    std::for_each(numbers.begin(), numbers.end(),
        [&count13]{int x}{count13 += x % 13 == 0;}};
    cout << "Count of numbers divisible by 13: " << count13 << '\n';
// using a single lambda
    count3 = count13 = 0;
    std::for_each(numbers.begin(), numbers.end(),
        [&](int x){count3 += x % 3 == 0; count13 += x % 13 == 0;});
    cout << "Count of numbers divisible by 3: " << count3 << '\n';
    cout << "Count of numbers divisible by 13: " << count13 << '\n';
    return 0;
}
```

下面是该程序的示例输出:

```txt
Sample size = 390000
Count of numbers divisible by 3: 130274
Count of numbers divisible by 13: 30009
Count of numbers divisible by 3: 130274
Count of numbers divisible by 13: 30009
```

输出表明，该程序使用的两种方法（两个独立的 lambda 和单个 lambda）的结果相同。

在 C++ 中引入 lambda 的主要目的是，让您能够将类似于函数的表达式用作接受函数指针或函数符的函数的参数。因此，典型的 lambda 是测试表达式或比较表达式，可编写为一条返回语句。这使得 lambda 简洁而易于理解，且可自动推断返回类型。然而，有创意的 C++ 程序员可能开发出其他用法。

## 18.5 包装器

C++提供了多个包装器（wrapper，也叫适配器[adapter]）。这些对象用于给其他编程接口提供更一致或更合适的接口。例如，第16章讨论了bind1st和bind2ed，它们让接受两个参数的函数能够与这样的STL算法匹配，即它要求将接受一个参数的函数作为参数。C++11提供了其他的包装器，包括模板bind、men\_fn和reference\_wrapper以及包装器function。其中模板bind可替代bind1st和bind2nd，但更灵活；模板mem\_fn让您能够将成员函数作为常规函数进行传递；模板reference\_wrapper让您能够创建行为像引用但可被复制的对象；而包装器function让您能够以统一的方式处理多种类似于函数的形式。

下面更详细地介绍包装器 function 及其解决的问题。

## 18.5.1 包装器 function 及模板的低效性

请看下面的代码行:

```javascript
answer = ef(q);
```

ef 是什么呢？它可以是函数名、函数指针、函数对象或有名称的 lambda 表达式。所有这些都是可调用的类型（callable type）。鉴于可调用的类型如此丰富，这可能导致模板的效率极低。为明白这一点，来看一个简单的案例。

首先，在头文件中定义一些模板，如程序清单 18.6 所示。

程序清单 18.6 somedefs.h

```cpp
// somedefs.h
#include <iostream>

template <typename T, typename F>
T use_f(T v, F f)
{
    static int count = 0;
    count++;
    std::cout << " use_f count = " << count
        << ", &count = " << &count << std::endl;
    return f(v);
}

class Fp
{
private:
    double z_;
public:
    Fp(double z = 1.0) : z_(z) {}
    double operator()(double p) { return z_*p; }
};

class Fq
{
private:
    double z_;
public:
    Fq(double z = 1.0) : z_(z) {}
    double operator()(double q) { return z_+ q; }
};
```

模板 use\_f 使用参数 f 表示调用类型:

```javascript
return f(v);
```

接下来，程序清单 18.7 所示的程序调用模板函数 use\_f()6 次。

程序清单 18.7 callable.cpp

```cpp
// callable.cpp -- callable types and templates
#include "somedef.s.h"
#include <iostream>

double dub(double x) {return 2.0*x;}
double square(double x) {return x*x;}
int main()
{
    using std::cout;
    using std::endl;

    double y = 1.21;
    cout << "Function pointer dub:\n";
    cout << " " << use_f(y, dub) << endl;
    cout << "Function pointer square:\n";
    cout << " " << use_f(y, square) << endl;
    cout << "Function object Fp:\n";
    cout << " " << use_f(y, Fp(5.0)) << endl;
    cout << "Function object Fq:\n";
    cout << " " << use_f(y, Fq(5.0)) << endl;
    cout << "Lambda expression 1:\n";
    cout << " " << use_f(y, [](double u) {return u*u;}) << endl;
    cout << "Lambda expression 2:\n";
    cout << " " << use_f(y, [](double u) {return u+u/2.0;}) << endl;
    return 0;
}
```

在每次调用中，模板参数 T 都被设置为类型 double。模板参数 F 呢？每次调用时，F 都接受一个 double 值并返回一个 double 值，因此在 6 次 use\_of() 调用中，好像 F 的类型都相同，因此只会实例化模板一次。但正如下面的输出表明的，这种想法太天真了:

```txt
Function pointer dub:
    use_f count = 1, &count = 0x402028
    2.42

Function pointer square:
    use_f count = 2, &count = 0x402028
    1.1

Function object Fp:
    use_f count = 1, &count = 0x402020
    6.05

Function object Fq:
    use_f count = 1, &count = 0x402024
    6.21

Lambda expression 1:
    use_f count = 1, &count = 0x405020
    1.4641

Lambda expression 2:
    use_f count = 1, &count = 0x40501c
    1.815
```

模板函数 use\_f()有一个静态成员 count，可根据它的地址确定模板实例化了多少次。有 5 个不同的地址，这表明模板 use\_f()有 5 个不同的实例化。

为了解其中的原因，请考虑编译器如何判断模板参数 F 的类型。首先，来看下面的调用:

```javascript
use_f(y, dub);
```

其中的 dub 是一个函数的名称，该函数接受一个 double 参数并返回一个 double 值。函数名是指针，因此参数 F 的类型为 double(\*) (double): 一个指向这样的函数的指针，即它接受一个 double 参数并返回一个 double 值。

下一个调用如下:

```txt
use_f(y, square);
```

第二个参数的类型也是 double(\*) (double)，因此该调用使用的 use\_f() 实例化与第一个调用相同。

在接下来的两个 use\_f() 调用中，第二个参数为对象，F 的类型分别为 Fp 和 Fq，因为将为这些 F 值实例化 use\_f() 模板两次。最后，最后两个调用将 F 的类型设置为编译器为 lambda 表达式使用的类型。

## 18.5.2 修复问题

包装器 function 让您能够重写上述程序，使其只使用 use\_f() 的一个实例而不是 5 个。注意到程序清单 18.7 中的函数指针、函数对象和 lambda 表达式有一个相同的地方，它们都接受一个 double 参数并返回一个 double 值。可以说它们的调用特征标（call signature）相同。调用特征标是有返回类型以及用括号括起并用头号分隔的参数类型列表定义的，因此，这六个实例的调用特征标都是 double (double)。

模板 function 是在头文件 functional 中声明的，它从调用特征标的角度定义了一个对象，可用于包装调用特征标相同的函数指针、函数对象或 lambda 表达式。例如，下面的声明创建一个名为 fdci 的 function 对象，它接受一个 char 参数和一个 int 参数，并返回一个 double 值:

```cpp
std::function<double(char, int)> fdci;
```

然后，可以将接受一个 char 参数和一个 int 参数，并返回一个 double 值的任何函数指针、函数对象或 lambda 表达式赋给它。

在程序清单 18.7 中，所有可调用参数的调用特征标都相同:double (double)。要修复程序清单 18.7 以减少实例化次数，可使用 function&lt;double(double)&gt;创建六个包装器，用于表示 6 个函数、函数符和 lambda。这样，在对 use\_f() 的全部 6 次调用中，让 F 的类型都相同（function&lt;double(double)&gt;），因此只实例化一次。据此修改后的程序如程序清单 18.8 所示。

程序清单 18.8 wrapped.cpp

```cpp
//wrapped.cpp -- using a function wrapper as an argument
#include "somedef.s.h"
#include <iostream>
#include <functional>

double dub(double x) {return 2.0*x;}
double square(double x) {return x*x;}

int main()
{
    using std::cout;
    using std::endl;
    using std::function;

    double y = 1.21;
    function<double(double)> ef1 = dub;
    function<double(double)> ef2 = square;
    function<double(double)> ef3 = Fq(10.0);
    function<double(double)> ef4 = Fp(10.0);
    function<double(double)> ef5 =   [](double u) {return u*u;};
    function<double(double)> ef6 =   [](double u) {return u+u/2.0;};
    cout << "Function pointer dub:\n";
    cout << "      " << use_f(y, ef1) << endl;
```

```cpp
cout << "Function pointer square:\n";
cout << "  " << use_f(y, ef2) << endl;
cout << "Function object Fp:\n";
cout << "  " << use_f(y, ef3) << endl;
cout << "Function object Fq:\n";
cout << "  " << use_f(y, ef4) << endl;
cout << "Lambda expression 1:\n";
cout << "  " << use_f(y, ef5) << endl;
cout << "Lambda expression 2:\n";
cout << "  " << use_f(y,ef6) << endl;
return 0;
}
```

下面是该程序的示例输出:

```python
Function pointer dub:
    use_f count = 1, &count = 0x404020
    2.42
Function pointer sqrt:
    use_f count = 2, &count = 0x404020
    1.1
Function object Fp:
    use_f count = 3, &count = 0x404020
    11.21
Function object Fq:
    use_f count = 4, &count = 0x404020
    12.1
Lambda expression 1:
    use_f count = 5, &count = 0x404020
    1.4641
Lambda expression 2:
    use_f count = 6, &count = 0x404020
    1.815
```

从上述输出可知，count 的地址都相同，而 count 的值表明，use\_f() 被调用了 6 次。这表明只有一个实例，并调用了该实例 6 次，这缩小了可执行代码的规模。

## 18.5.3 其他方式

下面介绍使用 function 可完成的其他两项任务。首先，在程序清单 18.8 中，不用声明 6 个 function&lt;double (double)&gt;对象，而只使用一个临时 function&lt;double (double)&gt;对象，将其用作函数 use\_f() 的参数:

```txt
typedef function<double(double)> fdd; // simplify the type declaration
cout << use_f(y, fdd(dub)) << endl;   // create and initialize object to dub
cout << use_f(y, fdd(square)) << endl;
...
```

其次，程序清单 18.8 让 use\_f() 的第二个实参与形参 f 匹配，但另一种方法是让形参 f 的类型与原始实参匹配。为此，可在模板 use\_f() 的定义中，将第二个参数声明为 function 包装器对象，如下所示:

```cpp
#include <functional>
template <typename T>
T use_f(T v, std::function<T(T)> f) // f call signature is T(T)
{
    static int count = 0;
    count++;
    std::cout << " use_f count = " << count
        << ", &count = " << &count << std::endl;
```

```txt
return f(v);
}
```

这样函数调用将如下:

```erlang
cout << " " << use_f<double>(y, dub) << endl;
cout << " " << use_f<double>(y, Fp(5.0)) << endl;
cout << " " << use_f<double>(y, [] (double u) {return u*u;}) << endl;
```

参数 dub、Fp(5.0)等本身的类型并不是 function<double(double)，因此在 use\_f 后面使用了&lt;double&gt;来指出所需的具体化。这样，T 被设置为 double，而 std::function&lt;T(T)&gt;变成了 std::function<double(double)。

## 18.6 可变参数模板

可变参数模板（variadic template）让您能够创建这样的模板函数和模板类，即可接受可变数量的参数。这里介绍可变参数模板函数。例如，假设要编写一个函数，它可接受任意数量的参数，参数的类型只需是cout能够显示的即可，并将参数显示为用逗号分隔的列表。请看下面的代码:

```txt
int n = 14;
double x = 2.71828;
std::string mr = "Mr. String objects!";
show_list(n, x);
show_list(x*x, "!', 7, mr);
```

这里的目标是，定义 show\_list()，让上述代码能够通过编译并生成如下输出:

```txt
14, 2.71828
7.38905, !, 7, Mr. String objects!
```

要创建可变参数模板，需要理解几个要点:

● 模板参数包（parameter pack）;
- 函数参数包:
- 展开（unpack）参数包；
- 递归。

## 18.6.1 模板和函数参数包

为理解参数包的工作原理，首先来看一个简单的模板函数，它显示一个只有一项的列表:

```cpp
template<typename T>
void show_list0{T value}
{
    std::cout << value << ", ";
}
```

在上述定义中，有两个参数列表。模板参数列表只包含 T，而函数参数列表只包含 value。下面的函数调用将模板参数列表中的 T 设置为 double，将函数参数列表中的 value 设置为 2.15:

```javascript
.show_list0(2.15);
```

C++11 提供了一个用省略号表示的元运算符（meta-operator），让您能够声明表示模板参数包的标识符，模板参数包基本上是一个类型列表。同样，它还让您能够声明表示函数参数包的标识符，而函数参数包基本上是一个值列表。其语法如下:

```txt
template<typename... Args>    // Args is a template parameter pack
void show_list1(Args... args) // args is a function parameter pack
{
...
}
```

其中，Args 是一个模板参数包，而 args 是一个函数参数包。与其他参数名一样，可将这些参数包的名称指定为任何符合 C++ 标识符规则的名称。Args 和 T 的差别在于，T 与一种类型匹配，而 Args 与任意数量（包括零）的类型匹配。请看下面的函数调用:

```javascript
show_list1('S', 80, "sweet", 4.5);
```

在这种情况下，参数包 Args 包含与函数调用中的参数匹配的类型:char、int、const char \* 和 double。

下面的代码指出 value 的类型为 T:

```txt
void show_list0(T value)
```

同样，下面的代码指出 args 的类型为 Args:

```txt
void show_list1(Args... args)  // args is a function parameter pack
```

更准确地说，这意味着函数参数包 args 包含的值列表与模板参数包 Args 包含的类型列表匹配——无论是类型还是数量。在上面的示例中，args 包含值‘S’、80、“sweet”和 4.5。

这样，可变参数模板 show\_list1()与下面的函数调用都匹配:

```txt
show_list1();
show_list1(99);
show_list1(88.5, "cat");
show_list1(2,4,6,8, "who do we", std::string("appreciate));
```

就最后一个函数调用而言，模板参数包 Args 包含类型 int、int、int、int、const char \*和 std::string，而函数参数包 args 包含值 2、4、6、8、“who do we”和 std::string("appreciate")。

## 18.6.2 展开参数包

但函数如何访问这些包的内容呢？索引功能在这里不适用，即您不能使用 Args[2] 来访问包中的第三个类型。相反，可将省略号放在函数参数包名的右边，将参数包展开。例如，请看下述有缺陷的代码:

```txt
template<typename... Args>    // Args is a template parameter pack
void show_list1(Args... args) // args is a function parameter pack
{
    show_list1(args...); // passes unpacked args to show_list1()
}
```

这是什么意思呢？为何说它存在缺陷？假设有如下函数调用:

```javascript
show_list1(5,'L',0.5);
```

这将把 5、‘L’和 0.5 封装到 args 中。在该函数内部，下面的调用:

```txt
show_list1(args...);
```

将展开成如下所示:

```javascript
show_list1(5,'L',0.5);
```

也就是说，args 被替换为三给存储在 args 中的值。因此，表示法 args...展开为一个函数参数列表。不幸的是，该函数调用与原始函数调用相同，因此它将使用相同的参数不断调用自己，导致无限递归（这存在缺陷）。

## 18.6.3 在可变参数模板函数中使用递归

虽然前面的递归让 show\_list() 成为有用函数的希望破灭，但正确使用递归为访问参数包的内容提供了解决方案。这里的核心理念是，将函数参数包展开，对列表中的第一项进行处理，再将余下的内容传递给递归调用，以此类推，直到列表为空。与常规递归一样，确保递归将终止很重要。这里的技巧是将模板头改为如下所示:

```cpp
template<typename T, typename... Args>
void show_list3(T value, Args... args)
```

对于上述定义，show\_list3(-)的第一个实参决定了 T 和 value 的值，而其他实参决定了 Args 和 args 的值。这让函数能够对 value 进行处理，如显示它。然后，可递归调用 show\_list3()，并以 args...的方式将其他实参传递给它。每次递归调用都将显示一个值，并传递缩短了的列表，直到列表为空为止。程序清单 18.9 提供了一种实现，它虽然不完美，但演示了这种技巧。

程序清单18.9 variadic1.cpp

```cpp
//variadic1.cpp ---using recursion to unpack a parameter pack
#include <iostream>
#include <string>
// definition-for 0 parameters -- terminating calI
void show_1=st3() {}

// definition for 1 or more parameters
template<typename T, typename... Args>
void show_list3( T value, Args... args)
{
    std::cout << value << ", ";
    show_list3(args...);
}

int main()
{
    int n = 14;
    double x = 2.71828;
    std::string mr = "Mr. String objects";
    show_list3(n, x);
    show_list3(x*x,'F', 7, mr);
    return 0;
}
```

## 1. 程序说明

请看下面的函数调用:

```txt
show_list3(x*x, '!', 7, mr);
```

第一个实参导致 T 为 double，value 为 x\*x。其他三种类型（char、int 和 std::string）将放入 Args 包中，而其他三个值（'!'、7 和 mr）将放入 args 包中。

接下来，函数 show\_list3() 使用 cout 显示 value（大约为 7.38905）和字符串 “，”。这完成了显示列表中第一项的工作。

接下来是下面的调用:

```txt
show_list3(args...);
```

考虑到 args... 的展开作用，这与如下代码等价:

```javascript
show_list3('!', 7, mr);
```

前面说过，列表将每次减少一项。这次 T 和 value 分别为 char 和 '!'，而余下的两种类型和两个值分别被包装到 Args 和 args 中，下次递归调用将处理这些缩小了的包。最后，当 args 为空时，将调用不接受任何参数的 show\_list3()，导致处理结束。

程序清单 18.9 中两个函数调用的输出如下:

14, 2.71828, 7.38905, !, 7, Mr. String objects!,

## 2. 改进

可对 show\_list3() 做两方面的改进。当前，该函数在列表的每项后面显示一个逗号，但如果能省去最后一项后面的逗号就好了。为此，可添加一个处理一项的模板，并让其行为与通用模板稍有不同:

```cpp
// definition for 1 parameter
template<typename T>
void show_list3(T value)
{
    std::cout << value << '\n';
}
```

这样，当 args 包缩短到只有一项时，将调用这个版本，而它打印换行符而不是逗号。另外，由于没有递归调用 show\_list3()，它也将终止递归。

另一个可改进的地方是，当前的版本按值传递一切。对于这里使用的简单类型来说，这没问题，但对于cout可打印的大型类来说，这样做的效率很低。在可变参数模板中，可指定展开模式（pattern）。为此，可将下述代码:

```javascript
show_list3(Args... args);
```

替换为如下代码:

```txt
show_list3(const Args&... args);
```

这将对每个函数参数应用模式 const &。这样，最后分析的参数将不是 std::string mr，而是 const std::string& mr。

程序清单 18.10 包含这两项修改。

程序清单 18.10 variadic2.cpp

```cpp
// variadic2.cpp
#include <iostream>
#include <string>

// definition for 0 parameters
void show_list() {}

// definition for 1 parameter
template<typename T>
void show_list(const T& value)
{
    std::cout << value << '\n';
}
// definition for 2 or more parameters
template<typename T, typename... Args>
void show_list(const T& value, const Args&... args)
{
    std::cout << value << ", ";
    show_list(args...);
}

int main()
{
    int n = 14;
    double x = 2.71828;
```

```txt
std::string mr == "Mr. String_objects!";
    show_list(n, x);
    show_list(x*x, '!', 7; mr);
    return 0;
}
```

该程序的输出如下:

14, 2.71828

7.38905,!, 7, Mr. String\_objects!

## 18.7 C++11 新增的其他功能

C++Π 增加了很多功能，本书无法全面介绍；另外，本书编写期间，其中很多功能还未得到广泛实现。然而，有些功能有必要简要地介绍一下。

## 18.7.1 并行编程

当前，为提高计算机性能，增加处理器数量比提高处理器速度更容易。因此，装备了双核、四核处理器甚至多个多核处理器的计算机很常见，这让计算机能够同时执行多个线程，其中一个处理器可能处理视频下载，而另一个处理器处理电子表格。

有些操作能受益于多线程，但有些不能。考虑单向链表的搜索:程序必须从链表开头开始，沿链接依次向下搜索，直到到达链表末尾；在这种情况下，多线程的帮助不大。再来看未经排序的数组。考虑到数组的随机存取特征，可让一个线程从数组开头开始搜索，并让另一个线程从数组中间开始搜索，这将让搜索时间减半。

多线程确实带来了很多问题。如果一个线程挂起或两个线程试图同时访问同一项数据，结果将如何呢？为解决并行性问题，C++定义了一个支持线程化执行的内存模型；添加了关键字 thread\_local，提供了相关的库支持。关键字 thread\_local 将变量声明为静态存储，其持续性与特定线程相关；即定义这种变量的线程过期时，变量也将过期。

库支持由原子操作（atomic operation）库和线程支持库组成，其中原子操作库提供了头文件 atomic，而线程支持库提供了头文件 thread、mutex、condition\_variable 和 future。

## 18.7.2 新增的库

C++k1 添加了多个专用库。头文件 random 支持的可扩展随机数库提供了大量比 rand() 复杂的随机数工具。例如，您可以选择随机数生成器和分布状态，分布状态包括均匀分布（类似于 rand()）、二项式分布和正态分布等。

头文件 chrono 提供了处理时间间隔的途径。

头文件 tuple 支持模板 tuple。tuple 对象是广义的 pair 对象。pair 对象可存储两个类型不同的值，而 tuple 对象可存储任意多个类型不同的值。

头文件 ratio 支持的编译阶段有理数算术库让您能够准确地表示任何有理数，其分子和分母可用最宽的整型表示。它还支持对这些有理数进行算术运算。

在新增的库中，最有趣的一个是头文件 regex 支持的正则表达式库。正则表达式指定了一种模式，可用于与文本字符串的内容匹配。例如，方括号表达式与方括号中的任何单个字符匹配，因此[cCkK]与 c、C、k 和 K 都匹配，而[cCkK] at 与单词 cat、Cat、kat 和 Kat 都匹配。其他模式包括与一位数字匹配的 d、与一个单词匹配的 w、与制表符匹配的 t 等。在 C++ 中，斜杠具有特殊含义，因此对于模式 \d\t\w\d（即依次为一位数字、制表符、单词和一位数字），必须写成字符字面量 “\d\t\w\d”，即使用 \表示。这是引入原始字符串的原因之一（参见第 4 章），它让您能够将该模式写成 R “\d\t\w\d”。

ed、grep 和 awk 等 UNIX 工具都使用正则表达式，而解释型语言 Perl 扩展了正则表达式的功能。C++

正则表达式库让您能够选择多种形式的正则表达式。

## 18.7.3 低级编程

低级编程中的“低级”指的是抽象程度，而不是编程质量。低级意味着接近于计算机硬件和机器语言使用的比特和字节。对嵌入式编程和改善操作的效率而言，低级编程很重要。C++11给低级编程人员提供了一些帮助。

变化之一是放松了 POD（Plain Old Data）的要求。在 C++98 中，POD 是标量类型（单值类型，如 int 或 double）或没有构造函数、基类、私有数据、虚函数等的老式结构。以前的理念是，POD 是可安全地逐字节复制的东西。这种理念没变，但 C++11 认识到，在满足 C++98 的某些约束的情况下，仍可以是合法的 POD。这有助于低级编程，因为有些低级操作（如使用 C 语言函数进行逐字节复制或二进制 I/O）要求处理对象为 POD。

另一项修改是，允许共用体的成员有构造函数和析构函数，这让共用体更灵活；但保留了其他一些限制，如成员不能有虚函数。在需要最大程度地减少占用的内存时，通常使用共用体；上述新规则在这些情况下给程序员有更大的灵活性和功能。

C++11 解决了内存对齐问题。计算机系统可能对数据在内存中的存储方式有一定的限制。例如，一个系统可能要求 double 值的内存地址为偶数，而另一个系统可能要求其起始位置为 8 的整数倍。要获悉有关类型或对象的对齐要求，可使用运算符 alignof()（参见附录 E）。要控制对齐方式，可使用说明符 alignas。

constexpr 机制让编译器能够在编译阶段计算结果为常量的表达式，让 const 变量可存储在只读内存中，这对嵌入式编程来说很有用（在运行阶段初始化的变量存储在随机访问内存中）。

## 18.7.4 杂项

C99 引入了依赖于实现的扩展整型，C++11 继承了这种传统。在使用 128 位整数的系统中，可使用这样的类型。在 C 语言中，扩展类型由头文件 stdint.h 支持，而在 C++ 中，为头文件 cstdint。

C++11 提供了一种创建用户自定义字面量的机制:字面量运算符（literal operator）。使用这种机制可定义二进制字面量，如 1001001b，相应的字面量运算符将把它转换为整数值。

C++提供了调试工具 assert。这是一个宏，它在运行阶段对断言进行检查，如果为 true，则显示一条消息，否则调用 abort()。断言通常是程序员认为在程序的某个阶段应为 true 的东西。C++11 新增了关键字 static\_assert，可用于在编译阶段对断言进行测试。这样做的主要目的在于，对于在编译阶段（而不是运行阶段）实例化的模板，调试起来将更简单。

C++11 加强了对元编程（metaprogramming）的支持。元编程指的是编写这样的程序，它创建或修改其他程序，甚至修改自身。在 C++ 中，可使用模板在编译阶段完成这种工作。

## 18.8 语言变化

计算机语言是如何成长和发展的呢？C++的使用范围足够广后，显然需要国际标准，并将其控制权交给标准委员会:最初是ANSI委员会，随后是ISO/ANSI联合委员会，当前是ISO/IEC JTC1/SC22/WG21（C++标准委员会）。ISO是国际标准组织，IEC是国际电子技术委员会，JEC1是前两家组织组建的联合技术委员会1，SC22是JTC1下属的编程语言委员会，而WG21是SC22下属的C++工作小组。

委员会考虑缺陷报告和有关语言修改和扩展的提议，并试图达成一致。这个过程既繁琐又漫长，《The Dsign and Evolution of C++》（Stroustrup，Addison-Wesley，1994）介绍了这方面的一些情况。寻求一致的委员会沉闷而争议不断，可能不是鼓励创新的好方式，这也不是标准委员会应扮演的角色。

但就 C++ 而言，还有另一种变更的途径，那就是充满创意的 C++ 编程社区的直接行动。程序员无法不受羁绊地改进语言，但可创建有用的库。设计良好的库可改善语言的用途和功能，提高可靠性，让编程更容易、更有乐趣。库是在现有语言功能的基础上创建的，不需要额外的编译器支持。如果库是通过模板实现的，则可以头文件（文本文件）的方式分发。

一项这样的变革是STL，它主要是Alexander Stepanov创建的，Hewlett-Packard免费提供它。STL在编程社区获得了巨大成功，成了第一个ANSI/ISO标准的候选内容。事实上，其设计影响新标准的其他方面。

## 18.8.1 Boost项目

最近，Boost 库成了 C++ 编程的重要部分，给 C++11 带来了深远影响。Boost 项目发起于 1998 年，当时的 C++ 库工作小组主席 Beman Dawes 召集其他几位小组成员制定了一项计划，准备在标准委员会的框架外创建新库。该计划的基本理念是，创建一个充当开放论坛的网站，让人发布免费的 C++ 库。这个项目提供有关许可和编程实践的指南，并要求对提议的库进行同行审阅。其最终的成果是，一系列得到高度赞扬和广泛使用的库。这个项目提供了一个环境，让编程社区能够检验和评估编程理念以及提供反馈。

## 18.8.2 TR1

TR1（Technical Report 1）是 C++标准委员会的部分成员发起的一个项目，它是一个库扩展选集，这些扩展与 C++98 标准兼容，但不是必不可少的。这些扩展是下一个 C++标准的候选内容。TR1 库让 C++社区能够检验其组成部分的价值。当标准委员会将 TR1 的大部分内容融入 C++11 时，面对的是众所皆知且经过实践检验的库。

在 TR1 中，Boost 库占了很大一部分。这包括模板类 tuple 和 array、模板 bind 和 function、智能指针（对名称和实现做了一定的修改）、static\_assert、regex 库和 random 库。另外，Boost 社区和 TR1 用户的经验也导致了实际的语言变更，如异常规范的摒弃和可变参数模板的添加，其中可变参数模板让 tuple 模板类和 function 模板的实现更好了。

## 18.8.3 使用Boost

虽然在 C++11 中，可访问 Boost 开发的众多库，但还有很多其他的 Boost 库。例如，Conversion 库中的 lexical\_cast 让您能够在数值和字符串类型之间进行简单地转换，其语法类似于 dynamic\_cast:将模板参数指定为目标类型。程序清单 18.11 是一个简单示例。

程序清单 18.11 lexcast.cpp

```cpp
// lexcast.cpp -- simple cast from float to string
#include <iostream>
#include <string>
#include "boost/lexical_cast.hpp"
int main()
{
    using namespace std;

    cout << "Enter your weight: ";
    float weight;
    cin >> weight;
    string gain = "A 10% increase raises ";
    string wt = boost::lexical_cast<string>(weight);
    gain = gain + wt + " to ";  // string operator+()
    weight = 1.1 * weight;
    gain = gain + boost::lexical_cast<string>(weight) + ".";
    cout << gain << endl;
    return 0;
}
```

下面是两次运行该程序的情况:

Enter your weight: 150

A 10% increase raises 150 to 165.

Enter your weight: 156

A 10% increase raises 156 to 171.600006.

第二次运行的结果凸显了 lexical\_cast 的局限性:它未能很好地控制浮点数的格式。为控制浮点数的格式，需要使用更精致的内核格式化工具，这在第 17 章讨论过。

还可以使用 lexical\_cast 将字符串转换为数值。

显然，Boost 提供的功能比这里介绍的要多得多。例如，Any 库让您能够在 STL 容器中存储一系列不同类型的值和对象，方法是将 Any 模板用作各种值的包装器。Math 库在标准 math 库的基础上增加了数学函数。Filesystem 库让您编写的代码可在使用不同文件系统的平台之间移植。有关这个库以及如何将其加入到各种平台的更详细信息，请参阅 Boost 网站（www.boost.org）。另外，有些 C++ 编译器（如 Cygwin 编译器）还自带了 Boost 库。

## 18.9 接下来的任务

如果仔细阅读了本书，则应很好地掌握了 C++ 的规则。然而，这仅仅是学习这种语言的开始，接下来需要学习如何高效地使用该语言，这样的路更长。最好的情况是，工作或学习环境让您能够接触优秀的 C++ 代码和程序员。另外，了解 C++ 后，便可以阅读一些介绍高级主题和面向对象编程的书籍，附录 H 列出了一些这样的资源。

OOP 有助于开发大型项目，并提高其可靠性。OOP 方法的基本活动之一是发明能够表示正在模拟的情形（被称为问题域（problem domain））的类。由于实际问题通常很复杂，因此找到适当的类富有挑战性。创建复杂的系统时，从空白开始通常不可行，最好采用逐步迭代的方式。为此，该领域的实践者开发了多种技术和策略。具体地说，重要的是在分析和设计阶段完成尽可能多的迭代工作，而不要不断地修改实际代码。

常用的技术有两种:用例分析（use-case analysis）和 CRC 卡（CRC card）。在用例分析中，开发小组列出了常见的使用方式或最终系统将用于的场景；找出元素、操作和职责，以确定可能要使用的类和类特性。CRC（Class/Responsibilities/Collaborators 的简称）卡片是一种分析场景的简单方法。开发小组为每个类创建索引卡片，卡片上列出了类名、类责任（如表示的数据和执行的操作）以及类的协作者（如必须与之交互的其他类）。然后，小组使用 CRC 卡片提供的接口模拟场景。这可能提出新的类、转换责任等。

在更大的规模上，是用于整个项目的系统方法。在这方面，最新的工具是统一建模语言（Unified Modeling Language，UML），它不是一种编程语言，而是一种用于表示编程项目的分析和设计语言，是由Grady Booch、Jim Rumbaugh和Ivar Jacobson开发的，他们分别是更早的3种建模语言（Booch Method、OMT（对象建模技术，Object Modeling Technique）和OOSE（面向对象的软件工程，Object-Oriented Software Engineering））的主要开发人员。UML是从这3种语言演化而来的，于2005年被ISO/IEC批准为标准。

除加深对 C++ 的总体理解外，还可能需要学习特定的类库。例如，Microsoft 和 Embarcadero 提供了大量简化 Windows 编程的类库，而 Apple Xcode 提供了简化 Apple 平台（如 iPhone）编程的类库。

## 18.10 总结

C++新标准新增了大量功能。有些旨在让 C++更容易学习和使用，这包括用大括号括起的统一的列表初始化、使用 auto 自动推断类型、类内成员初始化以及基于范围的 for 循环；而有些旨在增强类设计以及使其更容易理解，这包括默认的和禁用的方法、委托构造函数、继承构造函数以及让虚函数设计更清晰的说明符 override 和 final。

有几项改进旨在提供程序和编程效率。lambda 表达式比函数指针和函数符更好，模板 function 可用于减少模板实例数量，右值引用让您能够使用移动语义以及实现移动构造函数和移动赋值运算符。

其他改进提供了更佳的工作方式。作用域内枚举让您能够更好地控制枚举的作用域和底层类型；模板 unique\_ptr 和 shared\_ptr 让您能够更好地处理使用 new 分配的内存。

新增的 decltype、返回类型后置、模板别名和可变参数模板让模板设计得到了改进。

修改后的共用体和 POD 规则、alignof()运算符、alignas 说明符以及 constexpr 机制支持低级编程。新增了多个库（包括新的 STL 类、tuple 模板和 regex 库）为众多常见的编程问题提供了解决方案

为支持并行编程，新标准还添加了关键字 thread\_local 和 atomic 库。

总之，无论对新手还是专家来说，新标准都改善了 C++ 的可用性和可靠性。

## 18.11 复习题

1. 使用用大括号括起的初始化列表语法重写下述代码。重写后的代码不应使用数组 ar:

```cpp
class Z200
{
private:
    int j;
    char ch;
    double z;
public:
    Z200(int jv, char chv, zv) : j(jv), ch(chv), z(zv) {}
...
};

double x = 8.8;
std::string s = "What a bracing effect!";
int k(99);
Z200 zip(200,'Z',0.675);
std::vector<int> ai(5);
int ar[5] = {3, 9, 4, 7, 1};
for (auto pt = ai.begin(), int i = 0; pt != ai.end(); ++pt, ++i)
    *pt = ai[i];
```

2. 在下述简短的程序中，哪些函数调用不对？为什么？对于合法的函数调用，指出其引用参数指向的是什么。

```cpp
#include <iostream>
using namespace std;

double up(double x) { return 2.0* x;}
void r1(const double &rx) {cout << rx << endl;}
void r2(double &rx) {cout << rx << endl;}
void r3(double &&rx) {cout << rx << endl;}

int main()
{
    double w = 10.0;
    r1(w);
    r1(w+1);
    r1(up(w));
    r2(w);
    r2(w+1);
```

```c
r2(up(w));
    r3(w);
    r3(w+1);
    r3(up(w));
    return 0;
}
```

3. a. 下述简短的程序显示什么？为什么？

```cpp
#include <iostream>
using namespace std;

double up(double x) { return 2.0* x;}
void r1(const double &rx) {cout << "const double & rx\n";}
void r1(double &rx) {cout << "double & rx\n";

int main()
{
    double w = 10.0;
    r1(w);
    r1(w+1);
    r1(up(w));
    return 0;
}
```

b. 下述简短的程序显示什么？为什么？

```cpp
#include <iostream>
using namespace std;

double up(double x) { return 2.0* x;}
void r1(double &rx) {cout << "double & rx\n";}
void r1(double &&rx) {cout << "double && rx\n;q}

int main()
{
    double w = 10.0;
    r1(w);
    r1(w+1);
    r1(up(w));
    return 0;
}
```

c. 下述简短的程序显示什么？为什么？

```cpp
#include <iostream>
using namespace std;
double up(double x) {return 2.0* x;}
void r1(const double &rx) {cout << "const double & rx\n";}
void r1(double &&rx) {cout << "double && rx\n";

int main()
{
    double w = 10.0;
    r1(w);
    r1(w+1);
    r1(up(w));
    return 0;
}
```

4. 哪些成员函数是特殊的成员函数？它们特殊的原因是什么？
5. 假设 Fizzle 类只有如下所示的数据成员:

```txt
class Fizzle
{
private:
    double bubbles[4000];
...
};
```

为什么不适合给这个类定义移动构造函数？要让这个类适合定义移动构造函数，应如何修改存储4000个double值的方式？

6. 修改下述简短的程序，使其使用 lambda 表达式而不是 f1()。请不要修改 show2()。

```cpp
#include <iostream>
template<typename T>
  void show2(double x; T& fp) {std::cout << x << " -> " << fp(x) << '\n';}
double f1(double x){ return 1:8*x+32;}
int main()
{
    show2(18.0; f1);
    return 0;
}
```

7. 修改下述简短而丑陋的程序，使其使用 lambda 表达式而不是函数符 Adder。请不要修改 sum()。

```cpp
#include <iostream>
#include <array>
const int Size = 5;
template<typename T>
  void sum(std::array<double,Size> a, T& fp);
class Adder
{
    double tot;
public:
      Adder(double q = 0) : tot(q) {}
      void operator()(double w) { tot +=w; }
      double tot_v () const {return tot;};
};
int main()
{
    double total = 0.0;
    Adder ad(total);
    std::array<double, Size> temp_c = {32.1, 34.3, 37.8, 35.2, 34.7};
    sum(temp_c,ad);
    total = _ad.tot_v();
    std::cout << "total: " << ad.tot_v() << '\n';
    return 0;
}
template<typename T>
  void sum(std::array<double,Size> a, T& fp)
{
    for(auto pt = a.begin(); pt != a.end(); ++pt)
    {
      fp(*pt);
    }
}
```

## 18.12 编程练习

1. 下面是一个简短程序的一部分:

```cpp
int main()
{
    using namespace std;
    // list of double deduced from list contents
        auto q = average_list({15.4, 10.7, 9.0});
        cout << q << endl;
// list of int deduced from list contents
        cout << average_list({20, 30, 19, 17, 45, 38}) << endl;
//forced list of double
        auto ad = average_list<double>{{'A', 70, 65.33}};
        cout << ad << endl;
        return 0;
}
```

请提供函数 average\_list()，让该程序变得完整。它应该是一个模板函数，其中的类型参数指定了用作函数参数的 initilize\_list 模板的类型以及函数的返回类型。

2. 下面是类 Cpmv 的声明:

```cpp
class Cpmv
{
public:
    struct Info
    {
        std::string qcode;
        std::string zcode;
    };
private:
    Info *pi;
public:
    Cpmv();
    Cpmv(std::string q, std::string z);
    Cpmv(const @pmv & cp);
    Cpmv(Cpmv && mv);
    ~Cpmv();
    Cpmv & operator={const Cpmv & cp};
    Cpmv & operator=(Cpmv && mv);
    Cpmv operator+(const Cpmv & obj) const;
    void Display() const;
};
```

函数 operator+() 应创建一个对象，其成员 qcode 和 zcode 有操作数的相应成员拼接而成。请提供为移动构造函数和移动赋值运算符实现移动语义的代码。编写一个使用所有这些方法的程序。为方便测试，让各个方法都显示特定的内容，以便知道它们被调用。

3. 编写并测试可变参数模板函数 sum\_value()，它接受任意长度的参数列表（其中包含数值，但可以是任何类型），并以 long double 的方式返回这些数值的和。
4. 使用 lambda 重新编写程序清单16.5。具体地说，使用一个有名称的 lambda 替换函数 outint()，并将函数符替换为两个匿名 lambda 表达式。

## 附录A 计数系统

人们使用很多计数系统来表示数字。有些计数系统（如罗马数字）不适合用于算术运算；而印度计数系统经过改进，并传入到欧洲后变成了阿拉伯计数系统，这种数字方便了数学、科学和商业计算。现代的计算机计数系统是基于占位符概念的，使用了最先出现在印度计数系统中的零。然而，这种原理被推广到其他计数系统。因此，虽然在日常生活中使用的是下一节将介绍的十进制，但计算领域通常使用八进制、十六进制和二进制。

## A.1 十进制数

数字的书写方式是基于 10 的幂数。例如，对于数字 2468，2 表示 2 个 1000，4 表示 4 个 100，6 表示 6 个 10，8 表示 8 个 1。

$$
2 4 6 8 = 2 \times 1 0 0 0 + 4 \times 1 0 0 + 6 \times 1 0 + 8 \times 1
$$

一千是  $10 \times 10 \times 10$  或 10 的 3 次幂，用  $10^{3}$  表示。使用这种表示法，可以这样书写上述关系:

$$
2 4 6 8 = 2 \times 1 0 ^ {3} + 4 \times 1 0 ^ {2} + 6 \times 1 0 ^ {1} + 8 \times 1 0 ^ {0}
$$

因为这种数字表示法是基于10的幂，所以将它称作基数为10的表示法或十进制表示法。可以用任何数作基数。例如，C++允许使用基数8（八进制）和基数16（十六进制）来书写整数（请注意， $10^{0}$ 为1，任何非零数的0次幂都为1）。

## A.2 八进制整数

八进制数是基于8的幂的，所以基数为8的表示法用数字0-7来书写数字。C++用前缀0来表示八进制表示法。也就是说，0177是一个八进制值。可以用8的幂来找到对应的十进制值:

| 八进制 | 十进制 |
| --- | --- |
| 177 | $= 1 \times {8}^{2} + 7 \times {8}^{1} + 7 \times {8}^{0}$ |
|  | $= 1 \times {64} + 7 \times 8 + 7 \times 1$ |
|  | =127 |

由于 UNIX 操作系统常使用八进制来表示值，因此 C++ 和 C 提供了八进制表示法。

## A.3 十六进制数

十六进制数是基于16的幂的。这意味着十六进制的10表示 $16 + 0$ ，即16。为表示9-16值，需要其他一些数字，标准的十六进制表示法使用字母a-f。 $\mathrm{C + + }$ 接受这些字符的大写和小写版本，如表A.1所示。

表 A.1 十六进制数

| 十六进制数 | 十进制值 |
| --- | --- |
| a或A | 10 |
| b或B | 11 |
| c或C | 12 |
| d或D | 13 |
| e或E | 14 |
| f或F | 15 |

C++使用 0x 或 0X 来指示十六进制表示法。因此 0x2B3 是一个十六进制值，可使用 16 的幂来得到对应的十进制值。

| 十六进制 | 十 进 制 |
| --- | --- |
| 0x2B3- | $= 2 \times {16}^{2} + {11} \times {16}^{1} + 3 \times {16}^{0}$ |
|  | $= 2 \times {256} + {11} \times {16} + 3 \times 1$ |
| - | =691 |

硬件文档常使用十六进制来表示诸如内存单元和端口号等值。

## A.4 二进制数

不管是使用十进制、八进制，还是十六进制表示法来书写整数，计算机都将它存储为二进制值（即基数为2）。二进制表示法只使用两个数字——0和1。例如，100E10E1就是二进制数。但C++没有提供二进制表示法来书写数字的方式。二进制数是基于2的幂。

| 二进制 | 十进制 |
| --- | --- |
| 100H1011 | $= 1 \times {2}^{7} + 0 \times {2}^{6} + 0 \times {2}^{5} + 1 \times {2}^{4} + 1 \times {2}^{3} + 0 \times {2}^{2} + 1 \times {2}^{1} + 1 \times {2}^{0 - }$ |
|  | $= {128} + 0 + 0 + {16} + 8 + 0 + 2 + 1$ |
|  | =155 |

二进制表示法与计算机内存完全对应，在内存中，每个单元（位）都可以设置成开或关。只是将关表示为0，将开表示为1。内存通常是以字节为单位组织的，每个字节包含8位（正如第2章指出的，C++字节并非一定是8位，但本附录采用常见的做法，用字节表示八位组）。字节中的位被编号，对应于相关的2的幂。这样，最右侧的位编号为0，然后是1，依此类推。例如，图A.1表示一个2字节的整数。

![](images/page_857_image_11.jpg)

<details>
<summary>text_image</summary>

位编号
15 14 13 12 11 10 9 8 7 6 . 5 4 3 2 1 0
0 0 0 0 1 0 0 1 0 0 1 0 0 0 1 0
</details>

$$
\begin{array}{l} \text {值} = 1 \times 2 ^ {1 1} + 1 \times 2 ^ {8} + 1 \times 2 ^ {5} + 1 \times 2 ^ {1} \\ = 2 0 4 8 + 2 5 6 + 3 2 + 2 \\ = 2 3 3 8 \\ \end{array}
$$

图 A.1 2 字节整数值

## A.5 二进制和十六进制

十六进制表示法常用于提供更为方便的二进制数据（如内存地址或存储位标记设置的整数）视图。这样做的原因是，每个十六进制位对应于4位。表A.2说明了这种对应关系。

表 A.2 十六进制数和对应的二进制数

| 十六进制位 | 对应的二进制数 |
| --- | --- |
| 0 | 0000 |
| 1 | 0001 |
| 2 | 0010 |
| 3 | 0011 |
| 4 | 0100- |
| 5 | 0101 |
| 6 | 0110 |
| 7 | 0111 |
| 8 | 1000 |
| 9 | 1001 |
| A | 1010 |
| B | 1011 |
| C | 1100 |
| D | 1101 |
| E | 1110= |
| F | 1111 |

要将十六进制值转换为二进制，只需将每个十六进制位替换为相应的二进制数即可。例如，十六进制0xA4对应于二进制数10100100。同样，可以轻松地将二进制值转换为十六进制，方法是将每4位转换为对应的十六进制位。例如，二进制值10010101将被转换为0x95。

## Big-Endian 和 Little Endian

奇怪的是，都使用整数的二进制表示的两个计算平台对同一个值的表示可能并不相同。例如，Intel 计算机使用 Little Endian 体系结构来存储字节，而 Motorola 处理器、IBM 大型机、SPARC 处理器和 ARM 处理器使用 Big Endian 方案（但最后的两种系统可配置成使用上述任何一种方案）。

术语 Big Endian 和 Little Endian 是从 “Big End In” 和 “Little End In”（指内存中单词（通常为两个字节）的字节顺序）衍生而来的。在 InteF 计算机（Little-Endian）中，先存储低位字节，这意味着十六进制值 -0xABCD 在内存中将被存储为 0xCD 0xAB。Motorola（Big Endian）计算机按相反的顺序存储，因此 0xABCD 在内存中被存储为 0xAB·0xCD。

这些术语最先出现在 Jonathan Swift 编写的《Gulliver's Travels》一书中。为讽刺众多政治斗争的非理性，Swift 杜撰了假想国中两个喜欢争论的政治派别:Big Endians 和 Little Endians，前者坚持认为从大的一头打破鸡蛋更合理，而后者坚持认为从小的一头打破鸡蛋更合理。

作为软件工程师，应了解目标平台的词序，它会影响对通过网络传输的数据的解释方式以及数据在二进制文件中的存储方式。在上面的例子中，二字节内存模式0xABCD在Little Endian计算机上表示十进制值52651，而在Big Endian计算机上表示十进制值43981。

# 附录 B C++保留字

C++保留了一些单词供自己和C++库使用。程序员不应将保留字用作声明中的标识符。保留字分三类:关键字、替代标记（alternative token）和C++库保留名称。

## B.1 C++关键字

关键字是组成编程语言词汇表的标识符，它们不能用于其他用途，如用作变量名。表 B.1 列出了 C++ 关键字，其中以粗体显示的关键字也是 ANSI C99 标准中的关键字，而以斜体显示的关键字是 C++11 新增的。

表 B.1 C++关键字

| alignas | -alignof | asm | auto- | bool- |
| --- | --- | --- | --- | --- |
| break | _case | catch | char | char16_t |
| char32_t | class | const | const_cast | constexpr |
| continue | decltype | default | delete | do |
| double- | dynamic_cast | else | enum | explicit |
| export | extern. | false | float | for |
| friend | goto | if | inline | int |
| long. | mutable | namespace | new | noexcept |
| nullptr | operator | private- | protected | public. |
| register- | reinterpret_cast | -return | short | signed |
| sizeof | static | static_assert | static_cast | struct |
| switch | -template | this | thread_local | throw |
| true | try | typedef | typeid | typename |
| union | unsigned | using | virtual | void |
| volatile | wchar_t | while |  |  |

## B.2 替代标记

除关键字外，C++还有一些运算符的字母替代表示，它们被称为替代标记。替代标记也被保留，表 B.2 列出了替代标记及其表示的运算符。

表 B.2 C++保留的替代标记及其含义

| 标记 | 含义 |
| --- | --- |
| and | &amp;&amp; |
| and_eq | &amp;= — |
| bitand | &amp; |
| bitor | \| |
| compl | ~ |
| not | ! |
| not_eq | != |
| or | \|\| |
| or_eq | \|= |
| xor | ^ |
| xor_eq | ^= |

## B.3 C++库保留名称

编译器不允许程序员将关键字和替代标记用作名称。还有另一类禁止使用（但并非绝对不能用）的名称——保留名称，它们是保留给 C++ 库使用的名称。如果您将这种名称用作标识符，后果将是不确定的。也就是说，可能导致编译器错误、警告、程序不能正确运行或根本不会导致任何问题。

C++语言保留了库头文件中使用的宏名。如果程序包含某个头文件，则不应将该头文件（以及该头文件包含的头文件，依此类推）中定义的宏名用作其他目的。例如，如果您直接或间接地包含了头文件&lt;climits&gt;，则不应将CHAR\_BIT用作标识符，因为它已被用作该头文件中一个宏的名称。

C++语言保留了以两个下划线或下划线和大写字母打头的名称，还将以单个下划线打头的名称保留用作全局变量。因此，程序员不能在全局名称空间使用诸如\_\_gink、\_\_Lynx 和\_lynx 等名称。

C++语言保留了在库头文件中被声明为链接性为外部的名称。对于函数，这包括函数的特征标（名称和参数列表）。例如，假设有如下代码:

```cpp
#include <cmath>
using namespace std;
```

则函数特征标 tan（double）被保留。这意味着您的程序不应声明一个原型如下所示的函数:

```txt
int tan{double};  // don't do it
```

该原型确实与库函数  $\tan()$  的原型不同，因为后者的返回类型为 double，但特征标部分确实相同。然而，定义下面的原型是可以的:

```txt
char * tan(char *);  // ok
```

这是因为虽然其名称与库函数  $\tan()$  相同，但特征标不同。

## B.4 有特殊含义的标识符

C++社区讨厌新增关键字，因为它们可能与现有代码发生冲突。这就是标准委员会改变关键字 auto 的用法，并赋予其他关键字（如 virtual 和 delete）新用法的原因所在。C++11 提供了另一种避免新增关键字的机制，即使用具有特殊含义的标识符。这些标识符不是关键字，但用于实现语言功能。编译器根据上下文来判断它们是常规标识符还是用于实现语言功能:

```lisp
class F
{
    int final;                     // #1
public:
...
    virtual void unfold() {...} = final;  // #2
};
```

在上述代码中，语句#1中的final是一个常规标识符，而语句#2中的final使用了一种语言功能。这两种用法彼此不会冲突。

另外，C++还有很多经常出现在程序中，但不被保留的标识符。这包括头文件名、库函数名和 main（必不可少的函数的名称，程序从该函数开始执行）。只要不发生名称空间冲突，就可将这些标识符用于其他目的，但没有理由这样做。也就是说，完全可以编写下面的代码，但常识告诉您不应这样做:

```cpp
// allowable but silly
#include <iostream>
int iostream(int a);
int main ()
{
    std::
cout << iostream(5) << '\n';
    return 0;
}

int iostream(int a)
{
    int main = a + 1;
    int cout = a -1;
    return main*cout;
}
```

## 附录 C ASCII 字符集

计算机使用数字代码来存储字符。ASCII 码是美国最常用的编码，它是 Unicode 的一个子集（一个非常小的子集）。C++使得能够直接表示大多数字符，方法是将字符用单引号括起，例如‘A’表示字符 A。也可以用前面带反斜杠的八进制或十六进制编码来表示单个字符，例如，‘\012’和‘\0xa’表示的都是换行符（LF）。这种转义序列还可放在字符串中，如“Hello, \012my dear”。

表 C.1 列出了以各种方式表示的 ASCII 字符集。在该表中，当被用作前缀时，^字符表示使用 Ctrl 键。

表 C.1 ASC II 字符集

| 十进制 | 八进制 | 十六进制 | 二进制 | 字符 | ASCII名称 |
| --- | --- | --- | --- | --- | --- |
| 0 | 0 | 0 | 00000000 | ^@ | NUL |
| 1 | 01 | 0x1 | 00000001 | ^A | SOH |
| 2 | 02 | 0x2 | 00000010 | ^B | STX |
| 3 | 03 | 0x3 | 00000011 | ^C | ETX |
| 4 | 04 | 0x4 | 00000100 | ^D | EOT |
| 5 | 05 | 0x5 | 00000101 | ^E | ENQ |
| 6 | 06 | 0x6 | 00000110 | ^F | ACK |
| 7 | 07 | 0x7 | 00000111 | ^G | BEL |
| 8 | 010 | 0x8 | 00001000 | ^H | BS |
| 9 | 011 | 0x9 | 00001001 | ^I, tab | HT |
| 10 | 012 | 0xa | 00001010 | ^J | LF |
| 11 | 013 | 0xb | 00001011 | ^K | VT |
| 12 | 014 | 0xc | 00001100 | ^L | FF |
| 13 | 015 | 0xd | 00001101 | ^M | CR |
| 14 | 016 | 0xe | 00001110 | ^N | SO |
| 15 | 017 | 0xf | 00001111 | ^O | SI |
| 16 | 020 | 0x10 | 00010000 | ^P | DLE |
| 17 | 021 | 0x11 | 00010001 | ^Q | DC1 |
| 18 | 022 | 0x12 | 00010010 | ^R | DC2 |
| 19 | 023 | 0x13 | 00010011 | ^S | DC3 |
| 20 | 024 | 0x14 | 00010100 | ^T | DC4 |
| 21 | 025 | 0x15 | 00010101 | ^U | NAK |
| 22 | 026 | 0x16 | 00010110 | ^V | SYN |
| 23 | 027 | 0x17 | 00010111 | ^W | ETB |
| 24 | 030 | 0x18 | 00011000 | ^X | CAN |
| 25 | 031 | 0x19 | 00011001 | ^Y | EM |
| 26 | 032 | 0x1a | 00011010 | ^Z | SUB |
| 27 | 033 | 0x1b | 00011011 | ^[, Esc | ESC |
| 28 | 034 | 0x1c | 00011100 | ^\\ | FS |
| 29 | 035 | 0x1d | 00011101 | ^] | GS |
| 30 | 036 | 0x1e | 00011110 | ^^ | RS |
| 31 | 037 | 0x1f | 00011111 | ^ | US |
| 32 | 040- | 0x20 | 00100000 | 空格 | SP |
| 33 | 041 | 0x21 | 00100001 | ! |  |
| 34 | 042 | 0x22 | 00100010 | " |  |
| 35 | 043 | 0x23 | 00100011 | # |  |
| 36 | 044 | 0x24 | 00100100 | $ |  |
| 37 | 045 | 0x25 | 00100101 | % |  |
| 38 | 046 | 0x26 | 00100110 | &amp; |  |
| 39 | 047 | 0x27 | 00100111 | ' |  |
| 40 | 050 | 0x28 | 00101000 | ( |  |
| 41 | 051 | 0x29 | 00101001 | ) |  |
| 42 | 052 | 0x2a | 00101010 | * |  |
| 43 | 053 | 0x2b | 00101011 | + |  |
| 44 | 054 | 0x2c | 00101100 | ' |  |
| 45 | 055 | 0x2d | 00101101 | - |  |
| 46 | 056 | 0x2e | 00101110 |  |  |
| 47 | 057 | 0x2f | 00101111 | / |  |
| 48 | 060 | 0x30 | 00110000 | 0 |  |
| 49 | 061 | 0x31 | 00110001 | 1 |  |
| 50 | 062 | 0x32 | 00110010 | 2 |  |
| 51 | 063 | 0x33 | 00110011 | 3 |  |
| 52 | 064 | 0x34 | 00110100 | 4 |  |
| 53 | 065 | 0x35- | 00110101 | 5 |  |
| 54 | 066 | 0x36 | 00110110 | 6 |  |
| 55 | 067 | 0x37 | 00110111 | 7 |  |
| 56 | 070 | 0x38 | 00111000 | 8 |  |
| 57 | 071 | 0x39 | 00111001 | 9 |  |
| 58 | 072 | 0x3a | 00111010 | : | - |
| 59 | 073 | 0x3b- | 00111011 | ; |  |
| 60 | 074 | 0x3c | 00111100- | &lt; |  |
| 61 | 075 | 0x3d | 00111101 | = |  |
| 62 | 076 | 0x3e | 00111110 | > |  |
| 63 | 077 | 0x3f | 00111111 | ? |  |
| 64 | 0100 | 0x40- | 01000000 | @ |  |
| 65 | 0101 | 0x41 | 01000001 | A |  |
| 66 | 0102 | 0x42 | 01000010 | B |  |
| 67 | 0103 | 0x43 | 01000011 | C |  |
| 68 | 0104 | 0x44 | 01000100 | D |  |
| 69 | 0105 | 0x45 | 01000101 | E |  |