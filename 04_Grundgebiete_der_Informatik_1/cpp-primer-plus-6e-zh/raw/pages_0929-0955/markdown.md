# 附录 I 转换为 ISO 标准 C++

您可能想将一些用 C 或老式 C++ 版本开发的程序转换为标准 C++, 本附录提供了这方面的一些指南。其中的一些内容是关于从 C 转换为 C++ 的，另一些是关于从老式 C++ 转换为标准 C++ 的。

## 1.1 使用一些预处理器编译指令的替代品

C/C++预处理器提供了一系列的编译指令。通常，C++惯例是使用这些编译指令来管理编译过程，而避免用编译指令替换代码。例如，#include 编译指令是管理程序文件的重要组件。其他编译指令（如#ifndef 和 #endif）使得能够控制是否对特定的代码块进行编译。#pragma 编译指令使得能够控制编译器特定的编译选项。这些都是非常有帮助（有时是必不可少）的工具。但使用#define 编译指令时应谨慎。

## I.1.1 使用 const 而不是#define 来定义常量

符号常量可提高代码的可读性和可维护性。常量名指出了其含义，如果要修改它的值，只需定义修改一次，然后重新编译即可。C 使用预处理器来创建常量的符号名称。

```c
#define MAX_LENGTH 100
```

这样，预处理器将在编译之前对源代码执行文本置换，即用 100 替换所有的 MAX\_LENGTH。

而 C++ 则在变量声明使用限定符 const:

```javascript
const int MAX_LENGTH = 100;
```

这样 MAX\_LENGTH 将被视为一个只读的 int 变量。

使用 const 的方法有很多优越性。首先，声明显式指明了类型。使用# define 时，必须在数字后加上各种后缀来指出除 char、int 或 double 之外的类型。例如，使用 100L 来表明 long 类型，使用 3.14F 来表明 float 类型。更重要的是，const 方法可以很方便地用于复合类型，如下例所示:

```txt
const int base_vals[5] = {1000, 2000, 3500, 6000, 10000};
const string ans[3] = {"yes", "no", "maybe"};
```

最后，const标识符遵循变量的作用域规则，因此，可以创建作用域为全局、名称空间或数据块的常量。在特定函数中定义常量时，不必担心其定义会与程序的其他地方使用的全局常量冲突。例如，对于下面的代码:

```txt
#define n 5
const int dz = 12;
...
void fizzle()
{
    int n;
    int dz;
    ...
}
```

预处理器将把:

```txt
int n;
```

替换为:

int 5;

从而导致编译错误。而 fizzle() 中定义的 dz 是本地变量。另外，必要时，fizzle() 可以使用作用域解析运算符 (::)，以 ::dz 的方式访问该常量。

虽然 C++ 借鉴了 C 语言中的关键字 const，但 C++ 版本更有用。例如，对于外部 const 值，C++ 版本有内部链接，而不是变量和 C 中 const 所使用的默认外部链接。这意味着使用 const 的程序中的每个文件都必须定义该 const。这好像增加了工作量，但实际上，它使工作更简单。使用内部链接时，可以将 const 定义放在工程中的各种文件使用的头文件中。对于外部链接，这将导致编译错误，但对于内部链接，情况并非如此。另外，由于 const 必须在使用它的文件中定义（在该文件使用的头文件中定义也满足这样的要求），因此可以将 const 值用作数组长度参数:

```txt
const int MAX_LENGTH = 100;
...
double loads[MAX_LENGTH];
for (int i = 0; i < MAX_LENGTH; i++)
    loads[i] = 50;
```

这在 C 语言中是行不通的，因为定义 MAX\_LENGTH 的声明可能位于一个独立的文件中，在编译时，该文件可能不可用。坦白地说，在 C 语言中，可以使用 static 限定符来创建内部链接常量。也就是说，C++ 通过默认使用 static，让您可以少记住一件事。

顺便说一句，修订后的 C 标准（C99）允许将 const 用作数组长度，但必须将数组作为一种新式数组——变量数组，而这不是 C++标准的一部分。

在控制何时编译头文件方面，# define 编译指令仍然很有帮助:

```c
// blooper.h
#ifndef _BLOOPER_H_
#define _BLOOPER_H_
// code goes here
#endif
```

但对于符号常量，习惯上还是使用 const，而不是#define。另一个好方法——尤其是在有一组相关的整型常量时——是使用 enum:

```javascript
enum {LEVEL1 = 1, LEVEL2 = 2, LEVEL3 = 4, LEVEL4 = 8};
```

## I.1.2 使用 inline 而不是# define 来定义小型函数

在创建类似于内联函数的东西时，传统的 C 语言方式是使用一个#define 宏定义:

#define Cube(X) X\*X\*X

这将导致预处理器进行文本置换，将 X 替换为 Cube() 的参数:

```javascript
y = Cube(x);      // replaced with y = x*x*x;
y = Cube(x + z++);  // replaced with x + z++*x + z++*x + z++;
```

由于预处理器使用文本置换，而不是真正地传递参数，因此使用这种宏可能导致意外的、错误的结果。要避免这种错误，可以在宏中使用大量的圆括号来确保正确的运算顺序:

```lisp
#define Cube(X) ((X)*(X)*(X))
```

但即使这样做，也无法处理使用诸如  $Z++$  等值的情况。

C++方法是使用关键字 inline 来标识内联函数，这种方法更可靠，因为它采用的是真正的参数传递。另外，C++内联函数可以是常规函数，也可以是类方法:

```txt
class dormant
{
private:
    int period;
```

```txt
...
public:
    int Period() const { return period; } // automatically inline
    ...
};
```

#define 宏的一个优点是，它是无类型的，因此将其用于任何类型，运算都是有意义的。在 C++ 中，可以创建内联模板来使函数独立于类型，同时传递参数。

总之，请使用 C++内联技术，而不是 C 语言中的#define 宏。

## 1.2 使用函数原型

实际上，您没有选择的余地。虽然在 C 语言中，原型是可选的，但在 C++ 中，它确实是必不可少的。请注意，在使用之前定义的函数（如内联函数）是其原型。

应尽可能在函数原型和函数头中使用 const。具体地说，对于表示不可修改的数据的指针参数和引用参数，应使用 const。这不仅使编译器能够捕获修改数据的错误，也使函数更为通用。也就是说，接受 const 指针或引用的函数能够同时处理 const 数据和非 const 数据，而不使用 const 指针或引用的函数只能处理非 const 数据。

## 1.3 使用类型转换

Stroustrup 对 C 语言的抱怨之一是其无规律可循的类型转换运算符。确实，类型转换通常是必需的，但标准类型转换太不严格。例如，对于下面的代码:

```c
struct Doof
{
    double feeb;
    double steeb;
    char sgif[10];
};
Doof leam;
short * ps = (short *) & leam;  // old syntax
int * pi = int * (&leam);          // new syntax
```

C 语言不能防止将一种类型的指针转换为另一种完全不相关的类型的指针。

从某种意义上看，这种情况与 goto 语句相似。goto 语句的问题太灵活了，导致代码混乱。解决方法是提供更严格的、结构化程度更高的 goto 版本，来处理需要使用 goto 语句的常见任务，诸如 for 循环、while 循环和 if else 语句等语言元素应运而生。对于类型转换不严格的问题，标准 C++ 提供了类似的解决方案，即用严格的类型转换来处理最常见的、需要进行类型转换的情况。下面是第 15 章介绍的类型转换运算符:

```txt
- dynamic_cast;
- static_cast;
- const_cast;
- reinterpret_cast.
```

因此，在执行涉及指针的类型转换时，应尽可能使用上述运算符之一。这样做不但可以指出类型转换的目的，并可以检查类型转换是否是按预期那样使用的。

## 1.4 熟悉 C++特性

如果使用的是 malloc() 和 free()，请改用 new 和 delete；如果是使用 setjmp() 和 longjmp() 处理错误，

则请改用 try、throw 和 catch。另外，对于表示 true 和 false 的值，应将其类型声明为 bool。

## 1.5 使用新的头文件

C++标准指定了头文件的新名称，请参见第2章。如果使用的是老式头文件，则应当改用新名称。这样做不仅仅是形式上的改变，因为新版本有时新增了特性。例如，头文件ostream提供了对宽字符输入和输出的支持，还提供了新的控制符，如boolalpha和fixed（请参见第17章）。对于众多格式化选项的设置来说，这些控制符提供的接口比使用setf()或iomanip函数更简单。如果确实使用的是setf()，则在指定常量时，请使用ios\_base而不是ios，即使用ios\_base::fixed而不是ios::fixed。另外，新的头文件包含名称空间。

## 1.6 使用名称空间

名称空间有助于组织程序中使用的标识符，避免名称冲突。由于标准库是使用新的头文件组织实现的，它将名称放在 std 名称空间中，因此使用这些头文件需要处理名称空间。

出于简化的目的，本书的示例通常使用编译指令 using 来使 std 名称空间中的名称可用:

```cpp
#include <iostream>
#include <string>
#include <vector>
using namespace std;            // a using-directive
```

然而，不管需要与否，都导出名称空间中的所有名称，是与名称空间的初衷背道而驰的。

稍微要好些的方法是，在函数中使用 using 编译指令，这将使名称在该函数中可用。

更好也是推荐的方法是，使用 using 声明或作用域解析运算符（::），只使程序需要的名称可用。例如，下面的代码使 cin、cout 和 end1 可用于文件的剩余部分:

```cpp
#include <iostream>
using std::cin;                      // a using-declaration
using std::cout;
using std::endl;
```

但使用作用域解析运算符只能使名称在使用该运算符的表达式中可用:

```cpp
cout << std::fixed << x << endl;    //using the scope resolution operator
```

这样做可能很麻烦，但可以将通用的 using 声明放在一个头文件中:

```txt
// mynames - a header file
using std::cin;                      // a using-declaration
using std::cout;
using std::endl;
```

还可以将通用的 using 声明放在一个名称空间中:

```cpp
// mynames - a header file
#include <iostream>

namespace io
{
    using std::cin;
    using std::cout;
    using std::endl;
}

namespace formats
{
```

```txt
using std::fixed;
using std::scientific;
using std:boolalpha;
```

这样，程序可以包含该文件，并使用所需的名称空间:

```cpp
#include "mynames"
using namespace 10;
```

## 1.7 使用智能指针

每个 new 都应与 delete 配对使用。如果使用 new 的函数由于引发异常而提前结束，将导致问题。正如第 15 章介绍的，使用 autoptr 对象跟踪 new 创建的对象将自动完成 delete 操作。C++11 新增的 unique\_ptr 和 shared\_ptr 提供了更佳的替代方案。

## 1.8 使用 string 类

传统的 C 风格字符串深受不是真正的类型之苦。可以将字符串存储在字符数组中，也可以将字符数组初始化为字符串。但不能使用赋值运算符将字符串赋给字符数组，而必须使用 strcpy() 或 strncpy()。不能使用关系运算符来比较 C 风格字符串，而必须使用 strcmp()（如果忘记了这一点，使用了>运算符，将不会出现语法错误；程序将比较字符串的地址，而不是字符串的内容）。

而 string 类（参见第 16 章和附录 F）使得能够使用对象来表示字符串，并定义了赋值运算符、关系运算符和加法运算符（用于拼接）。另外，string 类还提供了自动内存管理功能，因此通常不用担心字符串被保存前，有人可能会跨越数组边界或将字符串截短。

String 类提供了许多方便的方法。例如，可以将一个 string 对象追加到另一个对象的后面，也可以将 C 风格的字符串，甚至 char 值追加到 string 对象的后面。对于接受 C 风格字符串参数的函数，可以使用 c\_str() 方法来返回一个适当的 char 指针。

string 类不仅提供了一组设计良好的方法来处理与字符串相关的工作（如查找子字符串），而且与 STL 兼容，因此，可以将 STL 算法用于 string 对象。

## 1.9 使用STL

标准模板库（请参见第16章和附录G）为许多编程需要提供了现成的解决方案，应使用它。例如，与其声明一个double或string对象数组，不如创建vector&lt;double&gt;对象或vector&lt;string&gt;对象。这样做的好处与使用string对象（而不是C风格字符串）相似。赋值运算符已被定义，因此可以使用赋值运算符将一个vector对象赋给另一个vector对象。可以按引用传递vector对象，接收这种对象的函数可以使用size()方法来确定vector对象中元素数目。内置的内存管理功能使得当使用pushback()方法在vector对象中添加元素时，其大小将自动调整。当然，还可以根据实际需要来使用其他有用的类方法和通用算法。在C++11中，如果长度固定的数组是更好的解决方案，可使用array&lt;double&gt;或array&lt;string&gt;。

如果需要链表、双端队列（或队列）、栈、常规队列、集合或映射，应使用 STL，它提供了有用的容器模板。算法库使得可以将矢量的内容轻松地复制到链表中，或将集合的内容同矢量进行比较。这种设计使得 STL 成为一个工具箱，它提供了基本部件，可以根据自己的需要进行装配。

在设计内容广泛的算法库时，效率是一个主要的设计目标，因此只需要完成少量的编程工作，便可以得到最好的结果。另外，实现算法时使用了迭代器的概念，这意味着这些算法不仅可用于STL容器。具体地说，它们也可用于传统数组。

## 附录 J 复习题答案

## 第2章复习题答案

1. 它们叫作函数。
2. 这将导致在最终的编译之前，使用iostream文件的内容替换该编译指令。
3. 它使得程序可以使用 std 名称空间中的定义。
cout << "Hello, world\n";
或
cout << "Hello, world" << endl;
5. int cheeses;
6. cheeses = 32;
7. cin >> cheeses;
8. cout << "We-have" << cheeses << "varieties of cheese\n";
9. 调用函数 froop()时，应提供一个参数，该参数的类型为 double，而该函数将返回一个 int 值。例如，可以像下面这样使用它:

```javascript
int gval = froop(3.14159);
```

函数 rattle() 接受一个 int 参数且没有返回值。例如，可以这样使用它:

```javascript
rattle(37);
```

函数 prune()不接受任何参数且返回一个 int 值。例如，可以这样使用它:

```javascript
int residue = prune();
```

10. 当函数的返回类型为 void 时，不用在函数中使用 return。然而，如果不提供返回值，则可以使用它:

```txt
return;
```

## 第3章复习题答案

1. 有多种整型类型，可以根据特定需求选择最适合的类型。例如，可以使用 short 来存储空格，使用 long 来确保存储容量，也可以寻找可提高特定计算的速度的类型。

```c
short rbis = 80;          // or short int rbis = 80;
unsigned int q = 42110;     // or unsigned q = 42110;
unsigned long ants = 3000000000;
// or long long ants = 3000000000;
```

注意:不要指望 int 变量能够存储 3000000000；另外，如果系统支持通用的列表初始化，可使用它:

```c
short rbis = {80};          // = is optional
unsigned int q {42110};     // could use = {42110}
long long ants {3000000000};
```

3. C++没有提供自动防止超出整型限制的功能，可以使用头文件climits来确定限制情况。
4. 常量 33L 的类型为 long，常量 33 的类型为 int。
5. 这两条语句并不真正等价，虽然对于某些系统来说，它们是等效的。最重要的是，只有在使用 ASCII码的系统上，第一条语句才将得分设置为字母 A，而第二条语句还可用于使用其他编码的系统。其次，65 是一个 int 常量，而 'A' 是一个 char 常量。

6. 下面是 4 种方式:

```txt
char c = 88;
cout << c << endl;          // char type prints as character

cout.put(char(88));            // put() prints char as character

cout << char(88) << endl;    // new-style type cast value to char

cout << (char)88 << endl;   // old-style type cast value to char
```

7. 这个问题的答案取决于这两个类型的长度。如果 long 为 4 个字节，则没有损失。因为最大的 long 值将是 20 亿，即有 10 位数。由于 double 提供了至少 13 位有效数字，因而不需要进行任何舍入。long long 类型可提供 19 位有效数字，超过了 double 保证的 13 位有效数字。

<div class="docvortex-algorithm" style="white-space: pre-wrap; font-family:monospace;">
8. a. $8*9 + 2$ is $72 + 2$ is 74  
b. $6*3 / 4$ is $18 / 4$ is 4  
c. $3 / 4*6$ is $0*6$ is 0  
d. $6.0*3 / 4$ is $18.0 / 4$ is 4.5  
e. $15\%$ 4 is 3
</div>

9. 下面的代码都可用于完成第一项任务:

```txt
int pos = (int) x1 + (int) x2;
int pos = int(x1) + int(x2);
```

要将它们作为 double 类型相加，再进行转换，可采取下述方式之一:

```txt
int pos = (int) (x1 + x2);
int pos = int(x1 + x2);
```

```txt
a. int
b. float
c. char
d. char32_t
e. double
```

## 第4章复习题答案

a. char actors[30];
b. short betsie[100];
c. float chuck[13];
d. long double dipsea[64];
a. array&lt;char,30&gt; -actors;
b. array&lt;short, 100&gt; betsie;
c. array&lt;float, 13&gt; -chuck;
d. array&lt;long double, 64&gt; -dipsea;
3. int oddly[5] = {1, 3, 5, 7, 9};
4. int even = oddly[0] + oddly[4];

5. cout << ideas[1] << "\n"; // or << endl;
6. char lunch[13] = "cheeseburger"; // number of characters + 1
或者
char lunch[] = "cheeseburger"; // let the compiler count elements
7. string lunch- = "Waldorf Salad";
如果没有 using 编译指令，则为:
struct fish {
    char kind[20];
    int weight;
    float length;
};
fish petes =
{
    "trout",
    12,
    26.25
};
10. enum Response {No, Yes, Maybe};
double \* pd = &ted;
cout << \*pd << "\n";
float \* pf = treacle;  // or = &treacle[0]
    cout << pf[0] << " " <<·pf[9]<< "\n";
        // or use \*pf and \*(pf + 9)

```rust
std::string lunch = "WaIdorf Salad";
```

13. 这里假设已经包含了头文件iostream和vector，并有一条using编译指令:

```txt
unsigned-int size;-
cout << "Enter a positive integer: ";
cin >> size;
int * dyn = new int [size];
vector<int> dv(size);
```

14. 是的，它是有效的。表达式 “home of the jolly bytes” 是一个字符串常量，因此，它将判定为字符串开始的地址。cout 对象将 char 地址解释为打印字符串，但类型转换(int \*)将地址转换为 int 指针，然后作为地址被打印。总之，该语句打印字符串的地址，只要 int 类型足够宽，能够存储该地址。

struct fish
{
    char kind[20];
    int weight;
    fFloat length;-
};
= \_\_\_\_
fish \* pole = new fish;
cout << "Enter kind of fish: ";
cin >> pole->kind;

16. 使用 cin >> address 将使得程序跳过空白，直到找到非空白字符为止。然后它将读取字符，直到再次遇到空白为止。因此，它将跳过数字输入后的换行符，从而避免这种问题。另一方面，它只读取一个单词，而不是整行。

#include &lt;string&gt;
#include = &lt;vector&gt;

```cpp
#include <array>
const int Str_num {10};  // or = 10
...
std::vector<std::string> vstr(Str_num);
std::array<std::string, Str_num> astr;
```

## 第5章复习题答案

1. 输入条件循环在进入输入循环体之前将评估测试表达式。如果条件最初为 false，则循环不会执行其循环体。退出条件循环在处理循环体之后评估测试表达式。因此，即使测试表达式最初为 false，循环也将执行一次。for 和 while 循环都是输入条件循环，而 do while 循环是退出条件循环。

2. 它将打印下面的内容:

01234

注意，cout<<endl;不是循环体的组成部分，因为没有大括号。

3. 它将打印下面的内容:

0369
12

4. 它将打印下面的内容:

6
8

5. 它将打印下面的内容:

k = 8

6. 使用 $^{*}$ = 运算符最简单:

```txt
for (int num = 1; num <= 64; num *= 2)
    cout << num << " ";
```

7. 将语句放在一对大括号中将形成一个复合语句或代码块。

8. 当然，第一条语句是有效的。表达式1,024由两个表达式组成——1和024，用逗号运算符连接。值为右侧表达式的值。这是024，八进制为20，因此该声明将值20赋给X。第二条语句也是有效的。然而，运算符优先级将导致它被判定成这样:

(y = 1), 024;

也就是说，左侧表达式将 y 设置成 1，整个表达式的值（没有使用）为 024 或 20（八进制）。

9. cin>>ch 将跳过空格、换行符和制表符，其他两种格式将读取这些字符。

## 第6章复习题答案

1. 这两个版本将给出相同的答案，但 if else 版本的效率更高。例如，考虑当 ch 为空格时的情况。版本 1 对空格加 1，然后看它是否为换行符。这将浪费时间，因为程序已经知道 ch 为空格，因此它不是换行符。在这种情况下，版本 2 将不会查看字符是否为换行符。

2. ++ch 和 ch + 1 得到的数值相同。但++ch 的类型为 char，将作为字符打印，而 ch + 1 是 int 类型（因为将 char 和 int 相加），将作为数字打印。

3. 由于程序使用 ch = '\$', 而不是 ch == '\$', 因此输入和输出将如下:

```txt
Hi!
H\$i\$!\$
\$Send \$10 or \$20 now!
S\$e\$n\$d\$ \$ct1 = 9, ct2 = 9
```

在第二次打印前,每个字符都被转换为\$字符。另外,表达式 ch=\$的值为\$字符的编码,因此它是非0值,因而为 true;所以每次 ct2 将被加1。

```txt
a. weight >= 115 && weight < 125
b. ch == 'q' || ch == 'Q'
c. x % 2 == 0 && x != 26
d. x % 2 == 0 && !(x % 26 == 0)
e. donation >= 1000 && donation <= 2000 || guest == 1
f. (ch >= 'a' && ch <= 'z') || (ch >= 'A' && ch <= 'Z')
```

5. 不一定。例如，如果 x 为 10，则!x 为 0，!!x 为 1。然而，如果 x 为 bool 变量，则!!x 为 x。

```txt
6. (x < 0)? -x : x
或
(x >= 0)? x : -x;
```

```txt
switch (ch)
{
    case 'A': a_grade++;
        break;
    case 'B': b_grade++;
        break;
    case 'C': c_grade++;
        break;
    case 'D': d_grade++;
        break;
    default: f_grade++;
        break;
}
```

8. 如果使用整数标签，且用户输入了非整数（如 q），则程序将因为整数输入不能处理字符而挂起。但是，如果使用字符标签，而用户输入了整数（如 5），则字符输入将 5 作为字符处理。然后，switch 语句的 default 部分将提示输入另一个字符。

9. 下面是一个版本:

```txt
int line = 0;
char ch;
while (cin.get(ch) && ch != 'Q')
{
    if (ch == '\n')
        line++;
}
```

## 第7章复习题答案

1. 这 3 个步骤是定义函数、提供原型、调用函数。

```txt
a. void igor(void); // or void igor()
b. float tofu(int n); // or float tofu(int);
c. double mpg(double miles, double gallons);
d. long summation(long harray[], int size);
e. double doctor(const char * str);
f. void ofcourse(boss dude);
g. char * plot(map *pmap);
```

```lisp
void set_array(int arr[], int size, int value)
{
    for (int i = 0; i < size; i++)
        arr[i] = value;
}
void set_array(int * begin, int * end, int value)
{
    for (int * pt = begin; pt != end; pt++)
        pt* = value;
}
double_biggest (const double foot[], int size)
{
    double max;
    if (size < 1)
    {
        cout << "Invalid array size of " << size << endl;
        cout << "Returning a value of 0\n";
        return 0;
    }
    else // not necessary because return terminates program
    {
        max = foot[0];
        for (int i = 1; i < size; i++)
            if (foot[i] > max)
                max = foot[i];
        return max;
    }
}
```

6. 将 const 限定符用于指针，以防止指向的原始数据被修改。程序传递基本类型（如 int 或 double）时，它将按值传递，以便函数使用副本。这样，原始数据将得到保护。

7. 字符串可以存储在 char 数组中，可以用带双引号的字符串来表示，也可以用指向字符串第一个字符的指针来表示。

```txt
int.replace(char *str, char c1, char c2)
{
    int count = 0;
    while (*str)      // while not at end of string
    {
        if (*str == c1)
        {
            *str = c2;
            count++;
        }
        str++;          // advance to next character
    }
    return count;
```

9. 由于 C++ 将 “pizza” 解释为其第一个元素的地址，因此使用 \* 运算符将得到第一个元素的值，即字符 p。由于 C++ 将 “taco” 解释为第一个元素的地址，因此它将 “taco” [2] 解释为第二个元素的值，即字符 c。换句话说，字符串常量的行为与数组名相同。
10. 要按值传递它，只要传递结构名 glitz 即可。要传递它的地址，请使用地址运算符&glitz。按值传递将自动保护原始数据，但这是以时间和内存为代价的。按地址传递可节省时间和内存，但不能保护原始数据，除非对函数参数使用了 const 限定符。另外，按值传递意味着可以使用常规的结构成员表示法，但传递指针则必须使用间接成员运算符。

int judge (int (\*pf)(const char \*));

12. a. 注意，如果 ap 是一个 applicant 结构，则 ap.credit\_ratings 就是一个数组名，而 ap.credit\_ratings[i] 是一个数组元素:

```cpp
void display(applicant ap)
{
    cout << ap.name << endl;
    for (int i = 0; i < 3; i++)
        cout << ap.credit_ratings[i] << endl;
}
```

b. 注意，如果 pa 是一个指向 applicant 结构的指针，则 pa->credit\_ratings 就是一个数组名，而 pa->credit\_ratings[i] 是一个数组元素:

```c
void show(const applicant * pa)
{
    cout << pa->name << endl;
    for (int i = 0; i < 3; i++)
        cout << pa->credit_ratings[i] << endl;
}

typedef void (*p_f1)(applicant *);
    p_f1 p1 = f1;
    typedef const char * (*p_f2)(const applicant *, const applicant *);
    p_f2 p2 = f2;
    p_f1 ap[5];
    p_f2 (*pa)[10];
```

## 第8章复习题答案

1. 只有一行代码的小型、非递归函数适合作为内联函数。

2. a. void song(const char \* name, int times = 1);

b. 没有。只有原型包含默认值的信息。

c. 是的，如果保留 times 的默认值:

```txt
void song(char * name = "0, My Papa", int times = 1);
```

3. 可以使用字符串"\"或字符""来打印引号，下面的函数演示了这两种方法。

```c
#include <iostream.h>
void iquote(int n)
{
    cout << "\" << n << "\"";
}

void iquote(double x)
{
    cout << '"' << x << ''";
}

void iquote(const char * str)
{
    cout << "\" << str << "\"";
}
```

4. a. 该函数不应修改结构成员，所以使用 const 限定符。

```txt
void show_box(const box & container)
{
    cout << "Made_by " << container. maker << endl;
    cout << "Height = " << container.height << endl;
    cout << "Width = " << container.width << endl;
    cout << "Length = " << container.length << endl;
    cout << "Volume = " << container.volume << endl;
}

b. void set_volume(box & crate)
{
    crate.volume = crate.height * crate.width * crate.length;
}
```

5. 首先，将原型修改成下面这样:

```cpp
// function to modify array object
void fill(std::array<double, Seasons> & pa};
// function that uses array object without modifying it
void show(const std::array<double, Seasons> & da);
```

注意，show()应使用 const，以禁止修改对象。

接下来，在 main() 中，将 fill() 调用改为下面这样:

```javascript
fill(expenses);
```

函数 show() 的调用不需要修改。

接下来，新的 fill() 应类似于下面这样:

```txt
void fill(std:array<double, Seasons> & pa) // changed
{
    using namespace std;
    for (int i = 0; i < Seasons; i++)
    {
        cout << "Enter" << Snames[i] << " expenses: ";
        cin >> pa[i];      // changed
    }
}
```

注意到(\*pa)[i]变成了更简单的 pa[i]。

最后，修改 show() 的函数头:

```cpp
void show(std::array<double, Seasons> & da)
```

6. a. 通过为第二个参数提供默认值:

```txt
double mass(double d, double v = 1:0);
```

也可以通过函数重载:

```txt
double mass(double d, double v);
double mass(double d);
```

b. 不能为重复的值使用默认值，因为必须从右到左提供默认值。可以使用重载:

```c
void repeat(int times, const char * str);
void repeat(const char * str);
```

c. 可以使用函数重载:

```txt
int average(int a, int b);
double average(double x, double y);
```

d. 不能这样做，因为两个版本的特征标将相同。

```txt
template<class T>
    T max(T t1, T t2)  // or T max(const T & t1, const T & t2)
    {
        return t1 > t2? t1 : t2;
    }

template<> box max(box b1, box b2)
    {
        return b1.volume > b2.volume? b1 : b2;
    }
```

9. v1 的类型为 float, v2 的类型为 float &, v3 的类型为 float &, v4 的类型为 int, v5 的类型为 double。字面值 2.0 的类型为 double，因此表达式 2.0 \* m 的类型为 double。

## 第9章复习题答案

F. a. homer 将自动成为自动变量。
b. 应该在一个文件中将 secret 定义为外部变量，并在第二个文件中使用 extern 来声明它。
c. 可以在外部定义前加上关键字 static，将 topsecret 定义为一个有内部链接的静态变量。也可在一个未命名的名称空间中进行定义。
d. 应在函数中的声明前加上关键字 static，将 beencalled 定义为一个本地静态变量。

2. using 声明使得名称空间中的单个名称可用，其作用域与 using 所在的声明区域相同。using 编译指令使名称空间中的所有名称可用。使用 using 编译指令时，就像在一个包含 using 声明和名称空间本身的最小声明区域中声明了这些名称一样。

```cpp
#include <iostream>
int main(){
{
    double x;
    std::cout << "Enter value: ";
    while (! (std::cin->> x) )
    {
        std::cout << "Bad input. Please enter a number: ";
        std::cin.clear();
        while (std::cin.get() != '\n')
            continue;
    }
    std::cout << "Value = " << x << std::end};
    return 0;
}
```

4. 下面是修改后的代码:

```cpp
#include <iostream>
int main() _
{
    using std::cin;
    using std::cout;
    using std::endl;
    double x;
    cout << "Enter value: ";
```

```txt
while (! (cin >> x) )
{
    cout << "Bad input. Please enter a number: ";
    cin.clear();
    while (cin.get() != '\n')
        continue;
}
cout << "Value = " << x << endl;
return 0;
}
```

5. 可以在每个文件中包含单独的静态函数定义。或者每个文件都在未命名的名称空间中定义一个合适的 average() 函数。

```asm
6. 10
    4
    0
    Other: 10, 1
    another(): 10, -4
7. 1
    4, 1, 2
    2
    2
    4, 1, 2
    2
```

## 第 10 章复习题答案

1. 类是用户定义的类型的定义。类声明指定了数据将如何存储，同时指定了用来访问和操纵这些数据的方法（类成员函数）。
2. 类表示人们可以类方法的公有接口对类对象执行的操作, 这是抽象。类的数据成员可以是私有的(默认值), 这意味着只能通过成员函数来访问这些数据, 这是数据隐藏。实现的具体细节(如数据表示和方法的代码)都是隐藏的, 这是封装。
3. 类定义了一种类型，包括如何使用它。对象是一个变量或其他数据对象（如由 new 生成的），并根据类定义被创建和使用。类和对象之间的关系同标准类型与其变量之间的关系相同。
4. 如果创建给定类的多个对象，则每个对象都有其自己的数据内存空间；但所有的对象都使用同一组成员函数（通常，方法是公有的，而数据是私有的，但这只是策略方面的问题，而不是对类的要求）。

5. 这个示例使用 char 数组来存储字符数据，但可以使用 string 类对象。

```cpp
// #include <cstring>

// class definition
class BankAccount
{
private:
    char name[40];      // or std::string name;
    char acctnum[25];  // or std::string acctnum;
    double balance;
public:
    BankAccount(const char * client, const char * num, double bal = 0.0);
//or BankAccount(const std::string & client,
//                  const std::string & num, double bal = 0.0);

    void show(void) const;
    void deposit(double cash);
```

```javascript
void withdraw(double cash);
};
```

6. 在创建类对象或显式调用构造函数时，类的构造函数都将被调用。当对象过期时，类的析构函数将被调用。
7. 有两种可能的解决方案（要使用 strncpy()，必须包含头文件 cstring 或 string.h; 要使用 string 类，必须包含头文件 string):

```cpp
BankAccount::BankAccount(const char * client, const char * num, double-bal)
{
    strncpy(name, client, 39);
    name[39] = '\0';
    strncpy(acctnum, num, 24);
    acctnum[24] = '\0';
    balance = bal;
}
```

或者:

```cpp
BankAccount::BankAccount(const std::string & client,
                               const std::string & num, double bal)
{
    name = client;
    acctnum== num;
    balance== bal;
}
```

请记住，默认参数位于原型中，而不是函数定义中。

8. 默认构造函数是没有参数或所有参数都有默认值的构造函数。拥有默认构造函数后，可以声明对象，而不初始化它，即使已经定义了初始化构造函数。它还使得能够声明数组。

```cpp
// stock30.h
#ifndef STOCK30_H_
#define STOCK30_H_

class Stock
{
private:
    std::string company;
    long shares;
    double share_val;
    double total_val;
    void set_tot() { total_val = shares * share_val; }
public:
    Stock();          // default constructor
    Stock(const std::string & co, long n, double pr);
    ~Stock() {}         // do-nothing destructor
    void buy(long num, double price);
    void sell(long num, double price);
    void update(double price);
    void show() const;
    const Stock & topval(const Stock & s) const;
    int numshares() const { return shares; }
    double shareval() const { return share_val; }
    double totalval() const { return total_val; }
    const string & co_name() const { return company; }
};
```

10. this 指针是类方法可以使用的指针，它指向用于调用方法的对象。因此，this 是对象的地址，\*this 是对象本身。

## 第 11 章复习题答案

1. 下面是类定义文件的原型和方法文件的函数定义:

```cpp
// prototype
Stonewt operator*(double mult);

// definition - let constructor do the work
Stonewt Stonewt::operator*(double mult)
{
    return Stonewt(mult * pounds);
}
```

2. 成员函数是类定义的一部分，通过特定的对象来调用。成员函数可以隐式访问调用对象的成员，而无需使用成员运算符。友元函数不是类的组成部分，因此被称为直接函数调用。友元函数不能隐式访问类成员，而必须将成员运算符用于作为参数传递的对象。请比较复习题1和复习题4的答案。

3. 要访问私有成员，它必须是友元，但要访问公有成员，可以不是友元。
4. 下面是类定义文件的原型和方法文件的函数定义:

```c
// prototype
friend Stonewt operator*(double mult, const Stonewt & s);

// definition - let constructor do the work
Stonewt operator*(double mult, const Stonewt & s)
{
    return Stonewt(mult * s.pounds);
}
```

5. 下面的 5 个运算符不能重载:

```txt
- sizeof。
- .°
- .*°
- ::°
- ?:°
```

6. 这些运算符必须使用成员函数来定义。

7. 下面是一个可能的原型和定义:

```txt
// prototype and inline definition
operator double () {return mag;}
```

但请注意，使用 magval() 方法比定义该转换函数更符合逻辑。

## 第 12 章复习题答案

1. a. 语法是正确的，但该构造函数没有将 str 指针初始化。该构造函数应将指针设置成 NULL 或使用 new [] 来初始化它。
b. 该构造函数没有创建新的字符串，而只是复制了原有字符串的地址。它应当使用 new [ ] 和 strcpy()。
c. 它复制了字符串，但没有给它分配存储空间，应使用 new char[len + 1] 来分配适当数量的内存。

2. 首先，当这种类型的对象过期时，对象的成员指针指向的数据仍将保留在内存中，这将占用空间，同时不可访问，因为指针已经丢失。可以让类析构函数删除构造函数中 new 分配的内存，来解决这种问题。其次，析构函数释放这种内存后，如果程序将这样的对象初始化为另一个对象，则析构函数将试图释放这些内存两次。这是因为将一个对象初始化为另一个对象的默认初始化，将复制指针值，但不复制指向的数据，这将使两个指针指向相同的数据。解决方法是，定义一个复制构造函数，使初始化复制指向的数据。第三，将一个对象赋给另一个对象也将导致两个指针指向相同的数据。解决方法是重载赋值运算符，使之复制数据，而不是指针。

3. C++自动提供下面的成员函数:

- 如果没有定义构造函数，将提供默认构造函数。
- 如果没有定义复制构造函数，将提供复制构造函数。
- 如果没有定义赋值运算符，将提供赋值运算符。
- 如果没有定义析构函数，将提供默认析构函数。
- 如果没有定义地址运算符，将提供地址运算符。

默认构造函数不完成任何工作，但使得能够声明数组和未初始化的对象。默认复制构造函数和默认赋值运算符使用成员赋值。默认析构函数也不完成任何工作。隐式地址运算符返回调用对象的地址（即 this 指针的值）。

4. 应将 personality 成员声明为字符数组或 car 指针，或者将其声明为 String 对象或 string 对象。该声明没有将方法设置为公有的，因此会有几个小错误。下面是一种可能的解决方法，修改的地方以粗体显示:

```cpp
#include <iostream>
#include <cstring>
using namespace std;
class nifty
{
private: // optional
    char personality[40];     // provide array size
    int talents;
public: // needed
// methods
    nifty();
    nifty(const char * s);
    friend ostream & operator<<(ostream & os, const nifty & n);
};    // note closing semicolon

nifty::nifty()
{
    personality[0] = '\0';
    talents = 0;
}

nifty::nifty(const char * s)
{
    strcpy(personality, s);
    talents = 0;
}

ostream & operator<<(ostream & os, const nifty & n)
{
    os << n.personality << '\n';
    os << n.talent << '\n';
    return os;
}
```

下面是另一种解决方案:

```cpp
#include <iostream>
#include <cstring>
using namespace std;
class nifty
{
private: // optional
    char * personality;    // create a pointer
    int talents;
public: // needed
// methods
    nifty();
    nifty(const char * s);
    nifty(const nifty & n);
    ~nifty() { delete [] personality; }
    nifty & operator=(const nifty & n) const;
    friend ostream & operator<<(ostream & os, const nifty & n);
};    // note closing semicolon

nifty::nifty()
{
    personality = NULL;
    talents = 0;
}

nifty::nifty(const char * s)
{
    personality = new char [strlen(s) + 1];
    strcpy(personality, s);
    talents = 0;
}

ostream & operator<<(ostream & os, const nifty & n)
{
    os << n.personality << '\n';
    os << n.talent << '\n';
    return os;
}

5. a. Golfer nancy; // default constructor
    Golfer lulu("Little Lulu"); // Golfer(const char * name, int g)
    Golfer roy("Roy Hobbs", 12); // Golfer(const char * name, int g)
    Golfer * par = new Golfer; // default constructor
    Golfer next = lulu; // Golfer(const Golfer &g)
    Golfer hazard = "Weed Thwacker"; // Golfer(const char * name, int g)
    *par = nancy; // default assignment operator
    nancy = "Nancy Putter";// Golfer(const char * name, int g), then
        // the default assignment operator
```

注意，对于语句 5 和 6，有些编译器还将调用默认的赋值运算符。

b. 类应定义一个复制数据（而不是地址）的赋值运算符。

## 第13章复习题答案

1. 基类的公有成员成为派生类的公有成员。基类的保护成员成为派生类的保护成员。基类的私有成员被继承，但不能直接访问。复习题2的答案提供了这些通用规定的特例。

2. 不能继承构造函数、析构函数、赋值运算符和友元。
3. 如果返回的类型为 void，仍可以使用单个赋值，但不能使用连锁赋值:

```txt
baseDMA magazine("Pandering to Glitz",-1);
baseDMA gift1, gift2, gift3;
gift1 = magazine; // ok
gift 2 = gift3 = gift1; // no longer valid
```

如果方法返回一个对象，而不是引用，则该方法的执行速度将有所减慢，这是因为返回语句需要复制对象。

4. 按派生的顺序调用构造函数，最早的构造函数最先调用。调用析构函数的顺序正好相反。
5. 是的，每个类都必须有自己的构造函数。如果派生类没有添加新成员，则构造函数可以为空，但必须存在。
6. 只调用派生类方法。它取代基类定义。仅当派生类没有重新定义方法或使用作用域解析运算符时，才会调用基类方法。然而，应把将所有要重新定义的函数声明为虚函数。
7. 如果派生类构造函数使用 new 或 new[] 运算符来初始化类的指针成员，则应定义一个赋值运算符。更普遍地说，如果对于派生类成员来说，默认赋值不正确，则应定义赋值运算符。
8. 当然，可以将派生类对象的地址赋给基类指针；但只有通过显式类型转换，才可以将基类对象的地址赋给派生类指针（向下转换），而使用这样的指针不一定安全。
9. 是的，可以将派生类对象赋给基类对象。对于派生类中新增的数据成员都不会传递给基类对象。然而，程序将使用基类的赋值运算符。仅当派生类定义了转换运算符（即包含将基类引用作为唯一参数的构造函数）或使用基类为参数的赋值运算符时，相反方向的赋值才是可能的。
10. 它可以这样做，因为 C++ 允许基类引用指向从该基类派生而来的任何类型。
11. 按值传递对象将调用复制构造函数。由于形参是基类对象，因此将调用基类的复制构造函数。复制构造函数以基类引用为参数，该引用可以指向作为参数传递的派生对象。最终结果是，将生成一个新的基类对象，其成员对应于派生对象的基类部分。
12. 按引用（而不是按值）传递对象，这样可以确保函数从虚函数受益。另外，按引用（而不是按值）传递对象可以节省内存和时间，尤其对于大型对象。按值传递对象的主要优点在于可以保护原始数据，但可以通过将引用作为 const 类型传递，来达到同样的目的。
13. 如果 head() 是一个常规方法，则 ph->head() 将调用 Corporation::head(); 如果 head() 是一个虚函数，则 ph->head() 将调用 PublicCorporation::head()。
14. 首先，这种情况不符合 is-a 模型，因此公有继承不适用。其次，House 中的 area() 定义隐藏了 area() 的 Kitchen 版本，因为这两个方法的特征标不同。

第14章复习题答案

1.-

| Class Bear | class PolarBear | 公有,北极熊是一种熊 |
| --- | --- | --- |
| class Kitchen | class Home | 私有,家里有厨房 |
| class Person | class Programmer | 公有,程序员是一种人 |
| class Person | class HorseAndJockey | 私有,马和驯马师的组合中包含一个人 |
| class Person | class Driver | 人是公有的,因为司机是一个人;汽车是私有的,因为司机有一辆汽车 |
| class Automobile |  |  |

```cpp
Gloam::Gloam(int g, const char *s) : gflip(g), fb(s) { }
Gloam::Gloam(int g, const Frabjous & fr) : glip(g), fb(fr) { }
// note: the above uses the default Frabjous copy constructor
void Gloam::tell()
{
    fb::tell();
    cout << glip << endl;
}
```

```cpp
Gloam::Gloam(int g, const char * s)
            : glip(g), Frabjous(s) { }
Gloam::Gloam(int g, const Frabjous & fr)
            : glip(g), Frabjous(fr) { }
// note: the above uses the default Frabjous copy constructor
void Gloam::tell()
{
    Frabjous::tell();
    cout << glip << endl;
}

class Stack<Worker */
{
private:
    enum {MAX = 10};          // constant specific to class
    Worker * items[MAX];     // holds stack items
    int top;                    // index for top stack item
public:
    Stack();
    Boolean isempty();
    Boolean isfull();
    Boolean push(const Worker * & item); // add item to stack
    Boolean pop(Worker * & item);         // pop top into item
};

ArrayTP<string> sa;
StackTP< ArrayTP<double> > stck_arr_db;
ArrayTP< StackTP<Worker *> > arr_stk_wpr;
```

程序清单 14.18 生成 4 个模板: ArrayTP&lt;int, 10&gt;、ArrayTP&lt;double, 10&gt;、ArrayTP&lt;int, 5&gt; 和 Array<ArrayTP&lt;int, 5&gt;, 10>。

6. 如果两条继承路线有相同的祖先，则类中将包含祖先成员的两个拷贝。将祖先类作为虚基类可以解决这种问题。

## 第 15 章复习题答案

1. a. 友元声明如下:

friend class clasp;

b. 这需要一个前向声明，以便编译器能够解释 void snip (muff&):

```cpp
snip(muff &):
class muff;    // forward declaration
class cuff {
public:
    void snip(muff &) { ... }
    ...
};
class muff {
    friend void cuff::snip(muff &);
    ...
```

c. 首先，cuff 类声明应在 muff 类之前，以便编译器可以理解 cuff::snip()。其次，编译器需要 muff 的一个前向声明，以便可以理解 snip(muff &)。

```cpp
class muff;    // forward declaration
class cuff {
public:
    void snip(muff &) { ... }
    ...
};
class muff {
    friend void cuff::snip(muff &);
    ...
};
```

2. 不。为使类 A 拥有一个本身为类 B 的成员函数的友元，B 的声明必须位于 A 的声明之前。一个前向声明是不够的，因为这种声明可以告诉 A:B 是一个类；但它不能指出类成员的名称。同样，如果 B 拥有一个本身是 A 的成员函数的友元，则 A 的这个声明必须位于 B 的声明之前。这两个要求是互斥的。
3. 访问类的唯一方法是通过其有接口，这意味着对于 Sauce 对象，只能调用构造函数来创建一个。其他成员（soy 和 sugar）在默认情况下是私有的。
4. 假设函数 f1() 调用函数 f2()。f2() 中的返回语句导致程序执行在函数 f1() 中调用函数 f2() 后面的一条语句。throw 语句导致程序沿函数调用的当前序列回溯，直到找到直接或间接包含对 f2() 的调用的 try 语句块为止。它可能在 f1() 中、调用 f1() 的函数中或其他函数中。找到这样的 try 语句块后，将执行下一个匹配的 catch 语句块，而不是函数调用后的语句。
5. 应按从子孙到祖先的顺序排列 catch 语句块。
6. 对于示例#1, 如果 pg 指向一个 Superb 对象或从 Superb 派生而来的任何类的对象, 则 if 条件为 true。具体地说, 如果 pg 指向 Magnificent 对象, 则 if 条件也为 true。对于示例#2, 仅当指向 Superb 对象时, if 条件才为 true, 如果指向的是从 Superb 派生出来的对象, 则 if 条件不为 true。
7. Dynamic\_cast 运算符只允许沿类层次结构向上转换，而 static\_cast 运算符允许向上转换和向下转换。static\_cast 运算符还允许枚举类型和整型之间以及数值类型之间的转换。

## 第16章复习题答案

```cpp
#include <string>
using namespace std;
cFass RQ1
{
private:
    string-st;      // a string object
public:
    RQ1() : st("")={=} 
    RQ1(const char * s) : st(s){}
    ~RQ1()={};
// more stuff
};
```

不再需要显式复制构造函数、析构程序和赋值运算符，因为 string 对象提供了自己的内存管理功能。

2. 可以将一个 string 对象赋给另一个。string 对象提供了自己的内存管理功能，所以一般不需要担心字符串超出存储容量。
#include &lt;string&gt;
#include &lt;cctype&gt;
using namespace std;
void ToUpper(string & str)

```lisp
{
    for (int i = 0; i < str.size(); i++)
        str[i] = toupper(str[i]);
}
```

auto\_ptr&lt;int&gt; pia= new int[20]; // wrong, use with new, not new[]
auto\_ptr&lt;string&gt;(new string); // wrong, no name for pointer
int rigue = 7;
auto\_ptr&lt;int&gt;(&rigue); // wrong, memory not allocated by new
auto\_ptr dbl (new double); // wrong, omits &lt;double&gt;

5. 栈的 LIFO 特征意味着可能必须在到达所需要的球棍（club）之前删除很多球棍。
6. 集合将只存储每个值的一个拷贝，因此，5个5分将被存储为1个5分。
7. 使用迭代器使得能够使用接口类似于指针的对象遍历不以数组方式组织的数据，如双向链表中的数据。
8. STL 方法使得可以将 STL 函数用于指向常规数组的常规指针以及指向 STL 容器类的迭代器，因此提高了通用性。
9. 可以将一个 vector 对象赋给另一个。vector 管理自己的内存，因此可以将元素插入到矢量中，并让它自动调整长度。使用 at() 方法，可以自动检查边界。
10. 这两个 vector 函数和 random\_shuffle() 函数要求随机访问迭代器，而 list 对象只有双向迭代器。可以使用 list 模板类的 sort() 成员函数（参见附录 G），而不是通用函数来排序，但没有与 random\_shuffle() 等效的成员函数。然而，可以将链表复制到矢量中，然后打乱矢量，并将结果重新复制到链表中。

## 第17章复习题答案

1. iostream 文件定义了用于管理输入和输出的类、常量和操纵符，这些对象管理用于处理 I/O 的流和缓冲区。该文件还创建了一些标准对象（cin、cout、cerr 和 clog 以及对应的宽字符对象），用于处理与每个程序相连的标准输入和输出流。
2. 键盘输入生成一系列字符。输入 121 将生成 3 个字符，每个字符都由一个 1 字节的二进制码表示。要将这个值存储为 int 类型，则必须将这 3 个字符转换为 121 值的二进制表示。
3. 在默认情况下，标准输出和标准错误都将输出发送给标准输出设备（通常为显示器）。然而，如果要求操作系统将输出重定向到文件，则标准输出将与文件（而不是显示器）相连，但标准错误仍与显示器相连。
4. ostream 类为每种 C++ 基本类型定义了一个 operator <<() 函数的版本。编译器将下面的表达式:

```txt
cout << spot
```

解释为:

```txt
cout.operator<<(spot)
```

这样，它便能够将该方法调用与具有相同参数类型的函数原型匹配。

5. 可以将返回 ostream & 类型的输出方法拼接。这样，通过一个对象调用方法时，将返回该对象。然后，返回对象将可以调用序列中的下一个方法。

//rq17-6.cpp
#include &lt;iostream&gt;
#include &lt;iomanip&gt;

int main()
{
    using namespace std;

```cpp
cout << "Enter an integer: ";
int n;
cin >> n;
cout << setw(15) << "base ten" << setw(15)
        << "base sixteen" << setw(15) << "base eight" << "\n";
cout.setf(ios::showbase);    // or cout << showbase;
cout << setw(15) << n << hex << setw(15) << n
        << oct << setw(15) << n << "\n";

return 0;
}

//rq17-7.cpp
#include <iostream>
#include <iomanip>

int main()
{
    using namespace std;
    char name[20];
    float hourly;
    float hours;

    cout << "Enter your name: ";
    cin.get(name, 20).get();
    cout << "Enter your hourly wages: ";
    cin >> hourly;
    cout << "Enter number of hours worked: ";
    cin >> hours;

    cout.setf(ios::showpoint);
    cout.setf(ios::fixed, ios::floatfield);
    cout.setf(ios::right, ios::adjustfield);
// or cout << showpoint << fixed << right;
    cout << "First format:\n";
    cout << setw(30) << name << ": \$" << setprecision(2)
        << setw(10) << hourly << ":" << setprecision(1)
        << setw(5) << hours << "\n";
    cout << "Second format:\n";
    cout.setf(ios::left, ios::adjustfield);
    cout << setw(30) << name << ": \$" << setprecision(2)
        << setw(10) << hourly << ":" << setprecision(1)
        << setw(5) << hours << "\n";

    return 0;
}
```

8. 下面是输出:

```javascript
ct1 = 5; ct2 = 9
```

该程序的前半部分忽略空格和换行符，而后半部分没有。注意，程序的后半部分从第一个 q 后面的换行符开始读取，将换行符计算在内。

9. 如果输入行超过 80 个字符，ignore() 将不能正常工作。在这种情况下，它将跳过前 80 个字符。

## 第18章复习题答案

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

double x {8.8};  // or = {8.8}
std::string s {"What a bracing effect!"};
int k{99};
Z200 zip{200,'Z',0.67});
std::vector<int> ai {3, 9, 4, 7, 1};
```

2. rl(w)合法，形参 rx 指向 w。

r1(w+1)合法，形参rx指向一个临时变量，这个变量被初始化为w+1。

r1(up(w))合法，形参 rx 指向一个临时变量，这个变量被初始化为 up(w) 的返回值。

一般而言，将左值传递给 const 左值引用参数时，参数将被初始化为左值。将右值传递给函数时，const 左值引用参数将指向右值的临时拷贝。

r2(w)合法，形参rx指向w。

r2(w+1)非法，因为 w+1 是一个右值。

r2(up(w))非法，因为 up(w)的返回值是一个右值。

一般而言，将左值传递给非 const 左值引用参数时，参数将被初始化为左值；但非 const 左值形参不能接受右值实参。

r3(w)非法，因为右值引用不能指向左值（如 w）。

r3(w+1)合法，rx指向表达式w+1的临时拷贝。

r3(up(w))合法，rx 指向 up(w)的临时返回值。

```typescript
3. a. double & rx
    const double & rx
    const double & rx
```

非 const 左值引用与左值实参 w 匹配。其他两个实参为右值，const 左值引用可指向它们的拷贝。

```txt
b. double & rx
    double && rx
    double && rx
```

左值引用与左值实参 w 匹配，而右值引用与两个右值实参匹配。

```txt
c. const double & rx
    double && rx
    double && rx
```

const 左值引用与左值实参 w 匹配，而右值引用与两个右值实参匹配。

总之，非 const 左值形参与左值实参匹配，非 const 右值形参与右值实参匹配；const 左值形参可与左值或右值形参匹配，但编译器优先选择前两种方式（如果可供选择的话）。

4. 它们是默认构造函数、复制构造函数、移动构造函数、析构函数、复制赋值运算符和移动赋值运算

符。这些函数之所以特殊，是因为编译器将根据情况自动提供它们的默认版本。

5. 在转让数据所有权（而不是复制数据）可行时，可使用移动构造函数，但对于标准数组，没有转让其所有权的机制。如果 Fizzle 使用指针和动态内存分配，则可将数据的地址赋给新指针，以转让其所有权。

```cpp
#include <iostream>
#include <algorithm>
template<typename T>
    void show2(double x, T fp) {std::cout << x << " -> " << fp(x) << '\n';}
int main()
{
    show2(18.0, [](double x){return 1.8*x + 32;});
    return 0;
}

#include <iostream>
#include <array>
#include <algorithm>
const int Size = 5;
template<typename T>
    void sum(std::array<double,Size> a, T& fp);
int main()
{
    double total = 0.0;
    std::array<double, Size> temp_c = {32.1, 34.3, 37.8, 35.2, 34.7};
    sum(temp_c, [&total](double w){total += w;});
    std::cout << "total: " << total << '\n';
    std::cin.get();
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

[General Information]

书名=C++ Primer Plus 第6版 中文版

作者=(美)普拉达著

页数=936

出版社=北京市:人民邮电出版社

出版日期=2012.06

SS号=13010684

DX号=000008301948

URL=http://book.szdnet.org.cn/bookDetail.jsp?dxNumber=000008301948&d=AE012D9B1AFA912ABBAAA26E5136D8F3