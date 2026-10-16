编译器将用 int 替换 TT，并生成下面的类定义:

```cpp
class HasFriendT<int>
{
...
    friend-void_counts<int>();
    friend void report<>(HasFriendT<int> &);
};
```

基于 FT 的具体化将变为 int，基于 HasFriend&lt;FF&gt; 的具体化将变为 HasFriend&lt;int&gt;。因此，模板具体化 counts&lt;int&gt;() 和 report<HasFriendT&lt;int&gt;() 被声明为 HasFriendT&lt;int&gt; 类的友元。

程序必须满足的第三个要求是，为友元提供模板定义。程序清单 14.23 说明了这 3 个方面。请注意，程序清单 14.22 包含 1 个 count() 函数，它是所有 HasFriend 类的友元；而程序清单 14.23 包含两个 count() 函数，它们分别是某个被实例化的类类型的友元。因为 count() 函数调用没有可被编译器用来推断出所需具体化的函数参数，所以这些调用使用 count&lt;int&gt; 和 coount&lt;double&gt;() 指明具体化。但对于 report() 调用，编译器可以从参数类型推断出要使用的具体化。使用 <> 格式也能获得同样的效果:

report<HasFriendT&lt;int&gt;>(hfi2);  // same as report(hfi2);

程序清单 14.23 tmp2tmp.cpp

```cpp
// tmp2tmp.cpp -- template friends to a template class
#include <iostream>
using std::cout;
using std::endl;
// template prototypes
template <typename T> void counts();
template <typename T> void report(T &);

// template class
template <typename TT>
class HasFriendT
{
private:
    TT item;
    static int ct;
public:
    HasFriendT(const TT & i) : item(i) {ct++;}
    ~HasFriendT() { ct--; }
    friend void counts<TT>();
    friend void report<>(HasFriendT<TT> &);
};

template <typename T>
int HasFriendT<T>::ct = 0;

// template friend functions definitions
template <typename T>
void counts()
{
    cout << "template size: " << sizeof(HasFriendT<T>) << "; ";
    cout << "template counts(): " << HasFriendT<T>::ct << endl;
}

template <typename T>
void report(T & hf)
{
```

```cpp
cout << hf.item << endl;
}

int main(){
{
    counts<int>();
    HasFriendT<int> hfi1(10);
    HasFriendT<int> hfi2(20);
    HasFriendT<double> hfdb(10.5);
    report(hfi1);  // generate report(HasFriendT<int> &)
    report(hfi2);  // generate report(HasFriendT<int> &)—
    report(hfdb);  // generate report(HasFriendT<double> &)=
    cout__<< "counts<int>()_output:\n";
    counts<int>();
    cout <<_"counts<double>() output:\n";
    counts<double>();

    return 0;_
}
```

下面是程序清单 14.23 所示程序的输出:

```txt
template_size: 4; template counts(): 0
10
20
10.5
counts<int>() output:
template-size: 4; template counts(): 2
counts<double>() output:
template-size: 8; template counts(): 1
```

正如您看到的，counts&lt;double&gt;和 counts&lt;int&gt;报告的模板大小不同，这表明每种 T 类型都有自己的友元函数 count()。

## 3. 模板类的非约束模板友元函数

前一节中的约束模板友元函数是在类外面声明的模板的具体化。int 类具体化获得 int 函数具体化，依此类推。通过在类内部声明模板，可以创建非约束友元函数，即每个函数具体化都是每个类具体化的友元。对于非约束友元，友元模板类型参数与模板类类型参数是不同的:

```txt
template <typename T>
class ManyFriend
{
```

```c
template <typename C, typename D> friend void show2(C & , D &);
```

程序清单 14.24 是一个使用非约束友元的例子。其中，函数调用 show2（hfi1，hfi2）与下面的具体化匹配:

```txt
void show2<ManyFriend<int>&, ManyFriend<int>&>
{
  (ManyFriend<int>& c, ManyFriend<int>& d)
```

因为它是所有 ManyFriend 具体化的友元，所以能够访问所有具体化的 item 成员，但它只访问了 ManyFriend&lt;int&gt;对象。

同样，show2(hfd, hfi2)与下面具体化匹配:

```txt
void show2<ManyFriend<double> &, ManyFriend<int> &>
    (ManyFriend<double> & c, ManyFriend<int> & d);
```

它也是所有 ManyFriend 具体化的友元，并访问了 ManyFriend&lt;int&gt;对象的 item 成员和 ManyFriend&lt;double&gt;对象的 item 成员。

程序清单-14.24 manyfrnd.cpp

```cpp
// manyfrnd.cpp -- unbound template friend to a template class
#include <iostream>
using std::cout;
using std::endl;

template <typename T>
class ManyFriend
{
private:
    T-item;
public:
    ManyFriend(const T & i) : item(i) {}
    template <typename C, typename D> friend void show2(C&, D &);
};

template <typename C, typename D> void show2(C & c, D & d)
{
    cout << c.item << ","" << d.item << endl;
}

int main()
{
    ManyFriend<int> hfi1(10);
    ManyFriend<int> hfi2(20);
    ManyFriend<double> hfdb(10.5);
    cout << "hfi1, hfi2: ";
    show2(hfi1, hfi2);
    cout << "hfdb, hfi2: ";
    show2(hfdb, hfi2);

    return 0;
}
```

程序清单 14.24 所示程序的输出如下:

```txt
hfil, hfi2: 10, 20
hfdb, hfi2: 10.5, 20
```

## 14.4.10 模板别名（C++11）

如果能为类型指定别名，将很方便，在模板设计中尤其如此。可使用 typedef 为模板具体化指定别名:

```cpp
// define three typedef aliases
typedef std::array<double, 12> arrd;
typedef std::array<int, 12> arri;
typedef std::array<std::string, 12> arrst;
arrd gallons;  // gallons is type std::array<double, 12>
arri days;    // days is type std::array<int, 12>
arrst months;  // months is type std::array<std::string, 12>
```

但如果您经常编写类似于上述 typedef 的代码，您可能怀疑要么自己忘记了可简化这项任务的 C++ 功能，要么 C++ 没有提供这样的功能。C++11 新增了一项功能——使用模板提供一系列别名，如下所示:

```cpp
template<typename T>
  using arrtype = std::array<T,12>;  // template to create multiple aliases
```

这将 arrtype 定义为一个模板别名，可使用它来指定类型，如下所示:

```cpp
arrtype<double> gallons;      // gallons is type std::array<double, 12>
arrtype<int> days;          // days is type std::array<int, 12>
arrtype<std::string> months;   // months is type std::array<std::string, 12>
```

总之，arrtype&lt;T&gt;表示类型 std::array&lt;T, 12&gt;。

C++11 允许将语法 using = 用于非模板。用于非模板时，这种语法与常规 typedef 等价:

```cpp
typedef const char * pc1;          // typedef syntax
using pc2 = const char *;         // using = syntax
typedef const int *(*pa1)[10];  // typedef syntax
using pa2 = const int *(*)[10]; // using = syntax
```

习惯这种语法后，您可能发现其可读性更强，因为它让类型名和类型信息更清晰。

C++11 新增的另一项模板功能是可变参数模板（variadic template），让您能够定义这样的模板类和模板函数，即可接受可变数量的参数。这个主题将在第 18 章介绍。

## 14.5 总结

C++提供了几种重用代码的手段。第13章介绍的公有继承能够建立is-a关系，这样派生类可以重用基类的代码。私有继承和保护继承也使得能够重用基类的代码，但建立的是has-a关系。使用私有继承时，基类的公有成员和保护成员将成为派生类的私有成员；使用保护继承时，基类的公有成员和保护成员将成为派生类的保护成员。无论使用哪种继承，基类的公有接口都将成为派生类的内部接口。这有时候被称为继承实现，但并不继承接口，因为派生类对象不能显式地使用基类的接口。因此，不能将派生对象看作是一种基类对象。由于这个原因，在不进行显式类型转换的情况下，基类指针或引用将不能指向派生类对象。

还可以通过开发包含对象成员的类来重用类代码。这种方法被称为包含、层次化或组合，它建立的也是has-a关系。与私有继承和保护继承相比，包含更容易实现和使用，所以通常优先采用这种方式。然而，私有继承和保护继承比包含有一些不同的功能。例如，继承允许派生类访问基类的保护成员；还允许派生类重新定义从基类那里继承的虚函数。因为包含不是继承，所以通过包含来重用类代码时，不能使用这些功能。另一方面，如果需要使用某个类的几个对象，则用包含更适合。例如，State类可以包含一组County对象。

多重继承（MI）使得能够在类设计中重用多个类的代码。私有 MI 或保护 MI 建立 has-a 关系，而公有 MI 建立 is-a 关系。MI 会带来一些问题，即多次定义同一个名称，继承多个基类对象。可以使用类限定符来解决名称二义性的问题，使用虚基类来避免继承多个基类对象的问题。但使用虚基类后，就需要为编写构造函数初始化列表以及解决二义性问题引入新的规则。

类模板使得能够创建通用的类设计，其中类型（通常是成员类型）由类型参数表示。典型的模板如下:

```txt
template <class T>
class Ic
{
    T v;
    ...
public:
    Ic(const T & val) : v(val) { }
    ...
};
```

其中，T 是类型参数，用作以后将指定的实际类型的占位符（这个参数可以是任意有效的 C++ 名称，

但通常使用 T 和 Type)。在这种环境下，也可以使用 typename 代替 class:

```txt
template <typename T> // same as template <class T>
class Rev {...} ;
```

类定义（实例化）在声明类对象并指定特定类型时生成。例如，下面的声明导致编译器生成类声明，用声明中的实际类型 short 替换模板中的所有类型参数 T:

```cpp
class_Ic<short> sic; //_impFicit:instantiation
```

这里，一类名为 Ic&lt;short&gt;，而不是 Ic。Ic&lt;short&gt;称为模板具体化。具体地说，这是一个隐式实例化。

使用关键字 template 声明类的特定具体化时，将发生显式实例化:

```txt
template class IC<int>; //-explicit instantiation
```

在这种情况下，编译器将使用通用模板生成一个 int 具体化——Ic&lt;int&gt;，虽然尚未请求这个类的对象。

可以提供显式具体化——覆盖模板定义的具体类声明。方法是以 template<> 打头，然后是模板类名称，再加上尖括号（其中包含要具体化的类型）。例如，为字符指针提供专用 lc 类的代码如下:

```cpp
template <> class Ic<char *>
{
    char * str;
public
    Ic(const char * s) * str(s).{s}
```

这样，下面这样的声明将为 chic 使用专用定义，而不是通用模板:

```javascript
class Ic<char *> chic;
```

类模板可以指定多个泛型，也可以有非类型参数:

```txt
template <class T, class-TT, -int n>
class Pals {...};
```

下面的声明将生成一个隐式实例化，用 double 代替 T，用 string 代替 TT，用 6 代替 n:

```txt
Pals<double, string, 6>_mix;
```

类模板还可以包含本身就是模板的参数:

```txt
template <- template <-typename T> class-CL, typename U,..int z>
class-Trophy {...};
```

其中 z 是一个 int 值，U 为类型名，CL 为一个使用 template&lt;typename, T&gt;声明的类模板。

类模板可以被部分具体化:

```txt
template <class T> Pals<T, T, 10> {...};
template <class T, class TT> Pals<T, TT, 100> {...};
template <class T, int n> Pals<T, T*, n> {...};
```

第一个声明为两个类型相同，且 n 的值为 6 的情况创建了一个具体化。同样，第二个声明为 n 等于 100 的情况创建一个具体化；第三个声明为第二个类型是指向第二个类型的指针的情况创建了一个具体化。

模板类可用作其他类、结构和模板的成员。

所有这些机制的目的都是为了让程序员能够重用经过测试的代码，而不用手工复制它们。这样可以简化编程工作，提供程序的可靠性。

## 14.6 复习题

1. 以 A 栏的类为基类时，B 栏的类采用公有派生还是私有派生更合适。

A

```txt
class Bear
class Kitchen
class Person-
class Person-
class Person, class Automobile
class PolarBear
class Home
class Programmer
class HorseAndJockey
class Driver
```

2. 假设有下面的定义:

```cpp
class-Frabjous {
private:
    char fab[20];
public:
    Frabjous(const char * s = "C++") = : fab(s) { }
    virtual void tell() { cout << fab; }
};

class-Gloam {
private:
    int glip;
    Frabjous fb;
public:
    Gloam(int g = 0, const char * s = "C++");
    Gloam(int g, const Frabjous & f);
    void tell();
};
```

假设 Gloam 版本的 tell() 应显示 glip 和 fb 的值，请为这 3 个 Gloam 方法提供定义。

3. 假设有下面的定义:

```cpp
class Frabjous {
private:
    char fab[20];
public:
    Frabjous(const char * s = "C++")=: fab(s) { }
    virtual void tell() !=cout << fab; }
};
class Gloam : private Frabjous{
private=
    int gFlip;
public:
    Gloam(int g = 0, const char * s = "C++");
    Gloam(int g, const Frabjous & f);
    void tell();
};
```

假设 Gloam 版本的 tell() 应显示 glip 和 fab 的值，请为这 3 个 Gloam 方法提供定义。

4. 假设有下面的定义，它是基于程序清单 14.13 中的 Stack 模板和程序清单 14.10 中的 Woker 类的:

```txt
Stack<Worker *> sw;
```

请写出将生成的类声明。只实现类声明，不实现非内联类方法。

5. 使用本章中的模板定义对下面的内容进行定义:

- string 对象数组;
- double 数组栈;

\- 指向 Worker 对象的指针的栈数组。

程序清单 14.18 生成了多少个模板类定义？

6. 指出虚基类与非虚基类之间的区别。

## 14.7 编程练习

1. Wine 类有一个 string 类对象成员（参见第 4 章）和一个 Pair 对象（参见本章）:其中前者用于存储葡萄酒的名称，而后者有 2 个 valarray&lt;int&gt;对象（参见本章），这两个 valarray&lt;int&gt;对象分别保存了葡萄酒的酿造年份和该年生产的瓶数。例如，Pair 的第 1 个 valarray&lt;int&gt;对象可能为 1988、1992 和 1996 年，第 2 个 valarray&lt;int&gt;对象可能为 24、48 和 144 瓶。Wine 最好有 1 个 int 成员用于存储年数。另外，一些 typedef 可能有助于简化编程工作:

```txt
typedef std::valarray<int> ArrayInt;
typedef Pair<ArrayInt, ArrayInt> PairArray;
```

这样，PairArray 表示的是类型 Pair<std::valarray&lt;int&gt;, std::valarray&lt;int&gt;>。使用包含来实现 Wine 类，并用一个简单的程序对其进行测试。Wine 类应该有一个默认构造函数以及如下构造函数:

```c
// initialize label to l, number of years to y,
// vintage years to yr[], bottles to bot[]
Wine(const char * l, int y, const int yr[], const int bot[]);
// initialize label to l, number of years to y,
// create array objects of length y
Wine(const char * l, int y);
```

Wine 类应该有一个 GetBottles() 方法，它根据 Wine 对象能够存储几种年份（y），提示用户输入年份和瓶数。方法 Label() 返回一个指向葡萄酒名称的引用。sum() 方法返回 Pair 对象中第二个 valarray&lt;int&gt;对象中的瓶数总和。

测试程序应提示用户输入葡萄酒名称、元素个数以及每个元素存储的年份和瓶数等信息。程序将使用这些数据来构造一个 Wine 对象，然后显示对象中保存的信息。

下面是一个简单的测试程序:

```cpp
// pe14-1.cpp  -- using Wine class with containment
#include <iostream>
#include "winec.h"

int main ( void )
{
    using std::cin;
    using std::cout;
    using std::endl;

    cout << "Enter name of wine: ";
    char lab[50];
    cin.getline(lab, 50);
    cout << "Enter number of years: ";
    int yrs;
    cin >> yrs;

    Wine holding(lab, yrs); // store label, years, give arrays yrs elements
    holding.GetBottles();   // solicit input for year, bottle count
    holding.Show();          // display object contents

    const int YRS = 3;
```

```cpp
int y[YRS] = {1993, 1995, 1998};
int b[YRS] = {.48, 60, 72};
// create new object, initialize using data in arrays y and b
Mine more("Gushing Grape Red", YRS, y, b);
more Show();
cout << "Total bottles for " << more Label() & // use Label() method
<< ": " << more sum() << endl; // use sum() method;
cout << "Bye\n";
return 0;
```

下面是该程序的运行情况:

```txt
Enter name of wine: Gully Wash
Enter number of years: 4
Enter Gully Wash data for 4 year
Enter year: 1988
Enter bottles for that year: 42
Enter year: 1994
Enter bottles for that year: 58
Enter year: 1998
Enter bottles for that year: 122
Enter year: 2001
Enter bottles for that year: 144
Wine: Gully Wash
Year Bottles
1988 42
1994 58
1998 122
2001 144
Wine: Gushing Grape Red
Year Bottles
1993 48
1995 60
1998 72
Total bottles for Gushing Grape R Bye
```

2. 采用私有继承而不是包含来完成编程练习1、同样，一些typedef可能会有所帮助；另外，您可能还需要考虑诸如下面这样的语句的含义:

```javascript
PairArray: operator=(PairArray(ArrayInt(), ArrayInt()));
cout << (const string &)(*this);
```

\- 您设计的类应该可以使用编程练习1中的测试程序进行测试。

3. 定义一个 QueueTp 模板。然后在一个类似于程序清单 14.12 的程序中创建一个指向 Worker 的指针队列（参见程序清单 14.10 中的定义），并使用该队列来测试它。
4. Person 类保存人的名和姓。除构造函数外，它还有 Show() 方法，用于显示名和姓。Gunslinger 类以 Person 类为虚基类派生而来，它包含一个 Draw() 成员，该方法返回一个 double 值，表示枪手的拔枪时间。这个类还包含一个 int 成员，表示枪手枪上的刻痕数。最后，这个类还包含一个 Show() 函数，用于显示所有这些信息。

PokerPlayer 类以 Person 类为虚基类派生而来。它包含一个 Draw() 成员，该函数返回一个 1\~52 的随机数，用于表示扑克牌的值（也可以定义一个 Card 类，其中包含花色和面值成员，然后让 Draw() 返回一个 Card 对象）。PokerPlayer 类使用 Person 类的 show() 函数。BadDude() 类从 Gunslinger 和 PokerPlayer 类公有派生而来。它包含 Gdraw() 成员（返回坏蛋拔枪的时间）和 Cdraw() 成员（返回下一张扑克牌），另外还有一个合适的 Show() 函数。请定义这些类和方法以及其他必要的方法（如用于设置对象值的方法），并使用一个类似于程序清单 14.12 的简单程序对它们进行测试。

5. 下面是一些类声明:

```cpp
// emp.h -- header file for abstr_emp class and children

#include <iostream>
#include <string>

class abstr_emp
{
private:
    std::string fname;     // abstr_emp's first name
    std::string lname;     // abstr_emp's last name
    std::string job;
public:
    abstr_emp();
    abstr_emp(const std::string & fn, const std::string &  ln,
           const std::string &  j);
    virtual void ShowAll() const;      // labels and shows all data
    virtual void SetAll();          // prompts user for values
    friend std::ostream &
           operator<<(std::ostream & os, const abstr_emp & e);
    // just displays first and last name
    virtual ~abstr_emp() = 0;         // virtual base class
};

class employee : public abstr_emp
{
public:
    employee();
    employee(const std::string & fn, const std::string &  ln,
           const std::string &  j);
    virtual void ShowAll() const;
    virtual void SetAll();
};

class manager:  virtual public abstr_emp
{
private:
    int inchargeof;        // number of abstr_emps managed
protected:
    int InChargeOf() const { return inchargeof; } // output
    int & InChargeOf(){ return inchargeof; }       // input
public:
    manager();
    manager(const std::string & fn, const std::string & ln,
           const std::string & j, int ico = 0);
    manager(const abstr_emp & e, int ico);
    manager(const manager & m);
    virtual void ShowAll() const;
    virtual void SetAll();
};

class fink: virtual public abstr_emp
```

```cpp
{
private:
    std::string reportsto;          // to whom fink reports
protected:
    const std::string ReportsTo() const { return reportsto; }
    std::string & ReportsTo(){ return reportsto; }
public:
    fink();
    fink(const std::string & fn, const std::string & ln,
        const std::string & j, const std::string & rpo);
    fink(const abstr_emp &e, const std::string & rpo);
    fink(const fink & e);
    virtual void ShowAll() const;
    virtual void SetAll();
};

class highfink: public manager, public fink // management fink
{
public:
    highfink();
    highfink(const std::string & fn, const std::string & ln,
        const std::string & j, const std::string & rpo,
        int ico);
    highfink(const abstr_emp & e, const std::string & rpo, int ico);
    highfink(const fink & f, int ico);
    highfink(const manager & m, const std::string & rpo);
    highfink(const highfink & h);
    virtual void ShowAll() const;
    virtual void SetAll();
};
```

注意，该类层次结构使用了带虚基类的MI，所以要牢记这种情况下用于构造函数初始化列表的特殊规则。还需要注意的是，有些方法被声明为保护的。这可以简化一些highfink方法的代码（例如，如果highfink::ShowAll()只是调用fink::ShowAll()和manager::ShwAll()，则它将调用abstr\_emp::ShowAll()两次）。请提供类方法的实现，并在一个程序中对这些类进行测试。下面是一个小型测试程序:

```cpp
// pe14-5.cpp
// useemp1.cpp -- using the abstr_emp classes

#include <iostream>
using namespace std;
#include "emp.h"

int main(void)
{
    employee em("Trip", "Harris", "Thumper");
    cout << em << endl;
    em.ShowAll();
    manager ma("Amorphia", "Spindragon", "Nuancer", 5);
    cout << ma << endl;
    ma.ShowAll();

    fink fi("Matt", "Oggs", "Oiler", "Juno Barr");
    cout << fi << endl;
```

```cpp
fi.ShowAll();
highfink hf (ma, "Curly Kew"); //recruitment?
hf.ShowAll();
cout << "Press a key for next phase:\n";
cin.get();
highfink hf2;
hf2.SetAll();

cout << "Using an abstr_emp * pointer:\n";
abstr_emp * tri[4] = {&em, &fi, &hf, &hf2};
for (int i = 0; i < 4; i++)
    tri[i]->ShowAll();

return 0;
}
```

为什么没有定义赋值运算符？

为什么要将 ShowAll() 和 SetAll() 定义为虚的？

为什么要将 abstr\_emp 定义为虚基类？

为什么 highfink 类没有数据部分？

为什么只需要一个 operator<<() 版本?

如果使用下面的代码替换程序的结尾部分，将会发生什么情况？

```c
abstr_emp  tri[4] = {em, fi, hf, hf2};
for (int i = 0; i < 4; i++)
    tri[i].ShowAll();
```

## 第 15 章 友元、异常和其他

## 本章内容包括:

- 友元类。
- 友元类方法。
- 嵌套类。
- 引发异常、try 块和 catch 块。
- 异常类。
● 运行阶段类型识别（RTTI）。
- dynamic\_cast 和 typeid。
- static\_cast、const\_cast 和 reinterpret\_cast。

本章先介绍一些 C++ 语言最初就有的特性，然后介绍 C++ 语言新增的一些特性。前者包括友元类、友元成员函数和嵌套类，它们是在其他类中声明的类；后者包括异常、运行阶段类型识别（RTTI）和改进后的类型转换控制。C++ 异常处理提供了处理特殊情况的机制，如果不对其进行处理，将导致程序终止。RTTI 是一种确定对象类型的机制。新的类型转换运算符提高了类型转换的安全性。后 3 种特性是 C++ 新增的，老式编译器不支持它们。

## 15.1 友元

本书前面的一些示例将友元函数用于类的扩展接口中，类并非只能拥有友元函数，也可以将类作为友元。在这种情况下，友元类的所有方法都可以访问原始类的私有成员和保护成员。另外，也可以做更严格的限制，只将特定的成员函数指定为另一个类的友元。哪些函数、成员函数或类为友元是由类定义的，而不能从外部强加友情。因此，尽管友元被授予从外部访问类的私有部分的权限，但它们并不与面向对象的编程思想相悖；相反，它们提高了公有接口的灵活性。

## 15.1.1 友元类

什么时候希望一个类成为另一个类的友元呢？我们来看一个例子。假定需要编写一个模拟电视机和遥控器的简单程序。决定定义一个Tv类和一个Remote类，来分别表示电视机和遥控器。很明显，这两个类之间应当存在某种关系，但是什么样的关系呢？遥控器并非电视机，反之亦然，所以公有继承的is-a关系并不适用。遥控器也非电视机的一部分，反之亦然，因此包含或私有继承和保护继承的has-a关系也不适用。事实上，遥控器可以改变电视机的状态，这表明应将Romote类作为Tv类的一个友元。

首先定义 Tv 类。可以用一组状态成员（描述电视各个方面的变量）来表示电视机。下面是一些可能的状态:

- 开/关；
- 频道设置；

- 音量设置；
● 有线电视或天线调节模式；
- TV 调谐或 A/V 输入。

调节模式指的是，在美国，对于有线接收和 UHF 广播接收，14 频道和 14 频道以上的频道间隔是不同的。输入选择包括 TV（有线 TV 或广播 TV）和 DVD。有些电视机可能提供更多的选择，如多种 DVD/蓝光输入，但对于这个示例的目的而言，这个清单足够了。

另外，电视机还有一些不是状态变量的参数。例如，可接收频道数随电视机而异，可以包括一个记录这个值的成员。

接下来，必须给类提供一些修改这些设置的方法。当前，很多电视机都将控件藏在面板后面，但大多数电视机还是可以在不使用遥控器的情况下进行换台等工作的，通常只能逐频道换台，而不能随意选台。同样，通常还有两个按钮，分别用来增加和降低音量。

遥控器的控制能力应与电视机内置的控制功能相同，它的很多方法都可通过使用 Tv 方法来实现。另外，遥控器通常都提供随意选择频道的功能，即可以直接从 2 频道换到 20 频道，并不用逐次切换频道。另外，很多遥控器都有多种工作模式，如用作电视控制器和 DVD 遥控器。

这些考虑因素表明，定义应类似于程序清单 15.1。定义中包括一些被定义为枚举的常数。下面的语句使 Remote 成为友元类:

```txt
friend class Remote;
```

友元声明可以位于公有、私有或保护部分，其所在的位置无关紧要。由于 Remote 类提到了 Tv 类，所以编译器必须了解 Tv 类后，才能处理 Remote 类，为此，最简单的方法是首先定义 Tv 类。也可以使用前向声明（forward delaration），这将稍后介绍。

程序清单 15.1 tv.h

```cpp
// tv.h -- Tv and Remote classes
#ifndef TV_H_
#define TV_H_

class Tv
{
public:
    friend class Remote;   // Remote can access Tv private parts
    enum {Off, On};
    enum {MinVal,MaxVal = 20};
    enum {Antenna, Cable};
    enum {TV, DVD};

    Tv(int s = Off, int mc = 125) : state(s), volume(5),
        maxchannel(mc), channel(2), mode(Cable), input(TV) {}
    void onoff() {state = (state == On)? Off : On;}
    bool ison() const {return state == On;}
    bool volup();
    bool voldown();
    void chanup();
    void chandown();
    void set_mode() {mode = (mode == Antenna)? Cable : Antenna;}
    void set_input() {input = (input == TV)? DVD : TV;}
    void settings() const; // display all settings
private:
    int state;            // on or off
    int volume;            // assumed to be digitized
    int maxchannel;          // maximum number of channels
```

```cpp
int channel;             // current channel setting
    int mode;                 // broadcast or cable
    int input;                // TV or DVD
};
class Remote
{
private:
    int mode;            // controls TV or DVD
public:
    Remote(int m = Tv::TV) : mode(m) {}
    bool volup(Tv & t) { return t.volup();}
    bool voldown(Tv & t) { return t.voldown();}
    void onoff(Tv & t) { t.onoff(); }
    void chanup(Tv & t) {t.chanup();}
    void chandown(Tv & t) {t.chandown();}
    void set_chan(Tv & t, int c) {t.channel = c;}
    void set_mode(Tv & t) {t.set_mode();}
    void set_input(Tv & t) {t.set_input();} .
};
#endif
```

在程序清单 15.1 中，大多数类方法都被定义为内联的。除构造函数外，所有的 Romote 方法都将一个 Tv 对象引用作为参数，这表明遥控器必须针对特定的电视机。程序清单 15.2 列出了其余的定义。音量设置函数将音量成员增减一个单位，除非声音到达最大或最小。频道选择函数使用循环方式，最低的频道设置为 1，它位于最高的频道设置 maxchannel 之后。

很多方法都使用条件运算符在两种状态之间切换:

```txt
void onoff() {state = (state == On)? Off : On;}
```

如果两种状态值分别为 true（1）和 false（0），则可以结合使用将在附录 E 讨论的按位异或和赋值运算符（^=）来简化上述代码:

```txt
void onoff() {state ^= 1;}
```

事实上，在单个无符号 char 变量中可存储多达 8 个双状态设置，分别对它们进行切换；但现在已经不用这样做了，使用附录 E 中讨论的按位运算符就可以完成。

程序清单 15.2 tv.cpp

```cpp
// tv.cpp -- methods for the Tv class (Remote methods are inline)
#include <iostream>
#include "tv.h"

bool Tv::volup()
{
    if (volume < MaxVal)
    {
        volume++;
        return true;
    }
    else
        return false;
}
bool Tv::voldown()
{
    if (volume > MinVal)
    {
```

```cpp
volume--;
    return true;
}
else
    return false;
}

void Tv::chanup()
{
    if (channel < maxchannel)
        channel++;
    else
        channel = 1;
}

void Tv::chandown()
{
    if (channel > 1)
        channel--;
    else
        channel = maxchannel;
}

void Tv::settings() const
{
    using std::cout;
    using std::endl;
    cout << "TV is " << (state == Off? "Off" : "On") << endl;
    if (state == On)
    {
        cout << "Volume setting = " << volume << endl;
        cout << "Channel setting = " << channel << endl;
        cout << "Mode = "
            << (mode == Antenna? "antenna" : "cable") << endl;
        cout << "Input = "
            << (input == TV? "TV" : "DVD") << endl;
    }
}
```

程序清单 15.3 是一个简短的程序，可以测试一些特性。另外，可使用同一个遥控器控制两台不同的电视机。

程序清单 15.3 use\_tv.cpp

```cpp
//use_tv.cpp -- using the Tv and Remote classes
#include <iostream>
#include "tv.h"

int main()
{
    using std::cout;
    Tv s42;
    cout << "Initial settings for 42\" TV:\n";
    s42.settings();
    s42.onoff();
    s42.chanup();
    cout << "\nAdjusted settings for 42\" TV:\n";
```

```txt
s42.chanup();
cout << "\nAdjusted settings for 42\" TV:\n";
s42.settings();

Remote grey;

grey.set_chan(s42, 10);
grey.volup(s42);
grey.volup(s42);
cout << "\n42\" settings after using remote:\n";
s42.settings();

Tv s58(Tv::On);
s58.set_mode();
grey.set_chan(s58,28);
cout << "\n58\" settings:\n";
s58.settings();
return 0;
}
```

下面是程序清单 15.1～程序清单 15.3 组成的程序的输出:

```python
Initial settings for 42" TV:
TV is Off
Adjusted settings for 42" TV:
TV is On
Volume setting = 5
Channel setting = 3
Mode = cable
Input = TV

42" settings after using remote:
TV is On
Volume setting = 7
Channel setting = 10
Mode = cable
Input = TV

58" settings:
TV is On
Volume setting = 5
Channel setting = 28
Mode = antenna
Input = TV
```

这个练习的主要目的在于表明，类友元是一种自然用语，用于表示一些关系。如果不使用某些形式的友元关系，则必须将 Tv 类的私有部分设置为公有的，或者创建一个笨拙的、大型类来包含电视机和遥控器。这种解决方法无法反应这样的事实，即同一个遥控器可用于多台电视机。

## 15.1.2 友元成员函数

从上一个例子中的代码可知，大多数 Remote 方法都是用 Tv 类的公有接口实现的。这意味着这些方法不是真正需要作为友元。事实上，唯一直接访问 Tv 成员的 Remote 方法是 Remote::set\_chan()，因此它是唯一需要作为友元的方法。确实可以选择仅让特定的类成员成为另一个类的友元，而不必让整个类成为友元，但这样做稍微有点麻烦，必须小心排列各种声明和定义的顺序。下面介绍其中的原因。

让 Remote::set\_chan()成为 Tv 类的友元的方法是，在 Tv 类声明中将其声明为友元:

```cpp
class Tv
{
    friend void Remote::set_chan(Tv & t, int c);
    ...
};
```

然而，要使编译器能够处理这条语句，它必须知道 Remote 的定义。否则，它无法知道 Remote 是一个类，而 set\_chan 是这个类的方法。这意味着应将 Remote 的定义放到 Tv 的定义前面。Remote 的方法提到了 Tv 对象，而这意味着 Tv 定义应当位于 Remote 定义之前。避开这种循环依赖的方法是，使用前向声明（forward declaration）。为此，需要在 Remote 定义的前面插入下面的语句:

```txt
class Tv;                  // forward declaration
```

这样，排列次序应如下:

```txt
class Tv;  // forward declaration
class Remote { ... };
class Tv { ... };
```

能否像下面这样排列呢？

```javascript
class Remote;          // forward declaration
class Tv { ... };
class Remote { ... };
```

答案是不能。原因在于，在编译器在 Tv 类的声明中看到 Remote 的一个方法被声明为 Tv 类的友元之前，应该先看到 Remote 类的声明和 set\_chan() 方法的声明。

还有一个麻烦。程序清单 15.1 的 Remote 声明包含了内联代码，例如:

```txt
void onoff(Tv & t) { t.onoff(); }
```

由于这将调用 Tv 的一个方法，所以编译器此时必须已经看到了 Tv 类的声明，这样才能知道 Tv 有哪些方法，但正如看到的，该声明位于 Remote 声明的后面。这种问题的解决方法是，使 Remote 声明中只包含方法声明，并将实际的定义放在 Tv 类之后。这样，排列顺序将如下:

```txt
class Tv;            // forward declaration
class Remote { ... };     // Tv-using methods as prototypes only
class Tv { ... };
// put Remote method definitions here
```

Remote 方法的原型与下面类似:

```txt
void onoff(Tv & t);
```

检查该原型时，所有的编译器都需要知道 Tv 是一个类，而前向声明提供了这样的信息。当编译器到达真正的方法定义时，它已经读取了 Tv 类的声明，并拥有了编译这些方法所需的信息。通过在方法定义中使用 inline 关键字，仍然可以使其成为内联方法。程序清单 15.4 列出了修订后的头文件。

程序清单 15.4 tvfm.h

```cpp
// tvfm.h -- Tv and Remote classes using a friend member
#ifndef TVFM_H_
#define TVFM_H_

class Tv;                                // forward declaration

class Remote
{
public:
    enum State{Off, On};
    enum {MinVal,MaxVal = 20};
    enum {Antenna, Cable};
```

```cpp
enum {TV, DVD};
private:
    int mode;
public:
    Remote(int m = TV) : mode(m) {}
    bool volup(Tv & t);          // prototype only
    bool voldown(Tv & t);
    void onoff(Tv & t) ;
    void chanup(Tv & t) ;
    void chandown(Tv & t) ;
    void set_mode(Tv & t) ;
    void set_input(Tv & t);
    void set_chan(Tv & t, int c);

};

class Tv
{
public:
    friend void Remote::set_chan(Tv & t, int c);
    enum State{Off, On};
    enum {MinVal,MaxVal = 20};
    enum {Antenna, Cable};
    enum {TV, DVD};

    Tv(int s = Off, int mc = 125) : state(s), volume(5),
        maxchannel(mc), channel(2), mode(Cable), input(TV) {}
    void onoff() {state = (state == On)? Off : On;}
    bool ison() const {return state == On;}
    bool volup();
    bool voldown();
    void chanup();
    void chandown();
    void set_mode() {mode = (mode == Antenna)? Cable : Antenna;}
    void set_input() {input = (input == TV)? DVD : TV;}
    void settings() const;
private:
    int state;
    int volume;
    int maxchannel;
    int channel;
    int mode;
    int input;
};

// Remote methods as-inline functions
inline bool Remote::volup(Tv & t) { return t.volup();}
inline bool Remote::voldown(Tv & t) { return t.voldown();}
inline void Remote::onoff(Tv & t) { t.onoff(); }
inline void Remote::chanup(Tv & t)= {t.chanup();}
inline void Remote::chandown(Tv & t) {t.chandown();}
inline void Remote::set_mode(Tv & t) {t.set_mode();}
inline void Remote::set_input(Tv & t) {t.set_input();}
inline void Remote::set_chan(Tv & t, int c) {t.channel = c;}
#endif
```

如果在 tv.cpp 和 use\_tv.cpp 中包含 tvfm.h 而不是 tv.h，程序的行为与前一个程序相同，区别在于，只有一个 Remote 方法是 Tv 类的友元，而在原来的版本中，所有的 Remote 方法都是 Tv 类的友元。图 15.1 说明了这种区别。

![](images/page_626_image_3.jpg)

图 15.1 类友元与类成员友元

本书前面介绍过，内联函数的链接性是内部的，这意味着函数定义必须在使用函数的文件中。在这个例子中，内联定义位于头文件中，因此在使用函数的文件中包含头文件可确保将定义放在正确的地方。也可以将定义放在实现文件中，但必须删除关键字 inline，这样函数的链接性将是外部的。

顺便说一句，让整个 Remote 类成为友元并不需要前向声明，因为友元语句本身已经指出 Remote 是一个类: friend class Remote;

## 15.1.3 其他友元关系

除本章前面讨论的，还有其他友元和类的组合形式，下面简要地介绍其中的一些。

假设由于技术进步，出现了交互式遥控器。例如，交互式遥控器让您能够回答电视节目中的问题，如果回答错误，电视将在控制器上产生嗡嗡声。忽略电视使用这种设施安排观众进入节目的可能性，我们只看 C++ 的编程方面。新的方案将受益于相互的友情，一些 Remote 方法能够像前面那样影响 Tv 对象，而一些 Tv 方法也能影响 Remote 对象。这可以通过让类彼此成为对方的友元来实现，即除了 Remote 是 Tv 的友元外，Tv还是 Remote 的友元。需要记住的一点是，对于使用 Remote 对象的 Tv 方法，其原型可在 Remote 类声明之前声明，但必须在 Remote 类声明之后定义，以便编译器有足够的信息来编译该方法。这种方案与下面类似:

```cpp
class Tv
{
friend class.Remote;
public:
    void buzz(Remote & r);
    ...
};
class Remote
{
friend class Tv;
public:
    void Bool volup(Tv.& t){t.volup();}
};
inline void Tv::buzz(Remote & r)
{
    ...
}
```

由于 Remote 的声明位于 Tv 声明的后面，所以可以在类声明中定义 Remote::volup()，但 Tv::buzz() 方法必须在 Tv 声明的外部定义，使其位于 Remote 声明的后面。如果不希望 buzz() 是内联的，则应在一个单独的方法定义文件中定义它。

## 15.1.4 共同的友元

需要使用友元的另一种情况是，函数需要访问两个类的私有数据。从逻辑上看，这样的函数应是每个类的成员函数，但这是不可能的。它可以是一个类的成员，同时是另一个类的友元，但有时将函数作为两个类的友元更合理。例如，假定有一个 Probe 类和一个 Analyzer 类，前者表示某种可编程的测量设备，后者表示某种可编程的分析设备。这两个类都有内部时钟，且希望它们能够同步，则应该包含下述代码行:

```dart
class Analyzer; // forward declaration
class Probe
{
    friend void sync(Analyzer & a, const Probe & p); // sync a to p
    friend void sync(Probe & p, const Analyzer & a); // sync p to a
    ...
};
class Analyzer
{
    friend void sync(Analyzer & a, const Probe & p); // sync a to p
    friend void sync(Probe & p, const Analyzer & a); // sync p to a
    ...
};
// define the friend functions
inline void sync(Analyzer & a, const Probe & p)
{
    ...
}
inline void sync(Probe & p, const Analyzer & a)
{
    ...
}
```

前向声明使编译器看到 Probe 类声明中的友元声明时，知道 Analyzer 是一种类型。

## 15.2 嵌套类

在 C++ 中，可以将类声明放在另一个类中。在另一个类中声明的类被称为嵌套类（nested class），它通过提供新的类型类作用域来避免名称混乱。包含类的成员函数可以创建和使用被嵌套类的对象；而仅当声明位于公有部分，才能在包含类的外面使用嵌套类，而且必须使用作用域解析运算符（然而，旧版本的 C++ 不允许嵌套类或无法完全实现这种概念）。

对类进行嵌套与包含并不同。包含意味着将类对象作为另一个类的成员，而对类进行嵌套不创建类成员，而是定义了一种类型，该类型仅在包含嵌套类声明的类中有效。

对类进行嵌套通常是为了帮助实现另一个类，并避免名称冲突。Queue 类示例（第 12 章的程序清单 12.8）嵌套了结构定义，从而实现了一种变相的嵌套类:

```lisp
class Queue
{
private:
// class scope_definitions
    // Node is a nested structure-definition local to this class
    struct Node {Item item; struct Node ← next;}
    ...
};
```

由于结构是一种其成员在默认情况下为公有的类，所以 Node 实际上是一个嵌套类，但该定义并没有充分利用类的功能。具体地说，它没有显式构造函数，下面进行补救。

首先，找到Queue示例中创建Node对象的位置。从类声明（程序清单11.10）和方法定义（程序清单12.61）可知，唯一创建了Node对象的地方是enqueue()方法:

```cpp
bool Queue::enqueue(const Item & item)
{
    if (isfull())
    return false;
    Node * add = new Node; // create node
// on_failure, new throws std::bad_alloc exception
    add->item = item;      // set node pointers
    add->next = NULL;
    ...
}
```

上述代码创建 Node 后，显式地给 Node 成员赋值，这种工作更适合由构造函数来完成。

知道应在什么地方以及如何使用构造函数后，便可以提供一个适当的构造函数定义:

```txt
class Queue
{
// class scope definitions
    // Node is a nested class=definition local to this class
    class Node
    {
    public:
        Item_item;
        Node * next;
        Node(const Item & i) : item(i), next(0) { }
    };
    ...
};
```

该构造函数将节点的 item 成员初始化为 i，并将 next 指针设置为 0，这是使用 C++ 编写空值指针的方法之一（使用 NULL 时，必须包含一个定义 NULL 的头文件；如果您使用的编译器支持 C++11，可使用 nullptr）。由于使用 Queue 类创建的所有节点的 next 的初始值都被设置为空指针，因此这个类只需要该构造函数。

接下来，需要使用构造函数重新编写 enqueue():

```cpp
bool Queue::enqueue(const Item & item)
{
    if (isfull())
        return false;
    Node * add = new Node(item);  // create, initialize node
// on failure, new throws std::bad_alloc exception
    ...
}
```

这使得 enqueue()的代码更短，也更安全，因为它自动进行初始化，无需程序员记住应做什么。

这个例子在类声明中定义了构造函数。假设想在方法文件中定义构造函数，则定义必须指出 Node 类是在 Queue 类中定义的。这是通过使用两次作用域解析运算符来完成的:

```rust
Queue::Node::Node(const Item & i) : item(i), next(0) { }
```

## 15.2.1 嵌套类和访问权限

有两种访问权限适合于嵌套类。首先，嵌套类的声明位置决定了嵌套类的作用域，即它决定了程序的哪些部分可以创建这种类的对象。其次，和其他类一样，嵌套类的公有部分、保护部分和私有部分控制了对类成员的访问。在哪些地方可以使用嵌套类以及如何使用嵌套类，取决于作用域和访问控制。下面将更详细地进行介绍。

## 1. 作用域

如果嵌套类是在另一个类的私有部分声明的，则只有后者知道它。在前一个例子中，被嵌套在 Queue 声明中的 Node 类就属于这种情况（看起来 Node 是在私有部分之前定义的，但别忘了，类的默认访问权限是私有的），因此，Queue 成员可以使用 Node 对象和指向 Node 对象的指针，但是程序的其他部分甚至不知道存在 Node 类。对于从 Queue 派生而来的类，Node 也是不可见的，因为派生类不能直接访问基类的私有部分。

如果嵌套类是在另一个类的保护部分声明的，则它对于后者来说是可见的，但是对于外部世界则是不可见的。然而，在这种情况中，派生类将知道嵌套类，并可以直接创建这种类型的对象。

如果嵌套类是在另一个类的公有部分声明的，则允许后者、后者的派生类以及外部世界使用它，因为它是公有的。然而，由于嵌套类的作用域为包含它的类，因此在外部世界使用它时，必须使用类限定符。例如，假设有下面的声明:

```txt
class Team
{
public:
    class Coach { ... };
    ...
};
```

现在假定有一个失业的教练，他不属于任何球队。要在 Team 类的外面创建 Coach 对象，可以这样做:

```cpp
Team::Coach forhire;  // create a Coach object outside the Team class
```

嵌套结构和枚举的作用域与此相同。其实，很多程序员都使用公有枚举来提供可供客户程序员使用的类常数。例如，很多类实现都被定义为支持 iostream 使用这种技术来提供不同的格式选项，前面已经介绍过这方面的内容，第 17 章将更加全面地进行介绍。表 15.1 总结了嵌套类、结构和枚举的作用域特征。

表 15.1

嵌套类、结构和枚举的作用域特征

| 声明位置 | 包含它的类是否可以使用它 | 从包含它的类派生而来的类是否可以使用它 | 在外部是否可以使用 |
| --- | --- | --- | --- |
| 私有部分 | 是 | 否 | 否 |
| 保护部分 | 是 | 是 | 否 |
| 公有部分 | 是 | 是 | 是,通过类限定符来使用 |

## 2. 访问控制

类可见后，起决定作用的将是访问控制。对嵌套类访问权的控制规则与对常规类相同。在 Queue 类声明中声明 Node 类并没有赋予 Queue 类任何对 Node 类的访问特权，也没有赋予 Node 类任何对 Queue 类的访问特权。因此，Queue 类对象只能显示地访问 Node 对象的公有成员。由于这个原因，在 Queue 示例中，Node 类的所有成员都被声明为公有的。这样有悖于应将数据成员声明为私有的这一惯例，但 Node 类是 Queue 类内部实现的一项特性，对外部世界是不可见的。这是因为 Node 类是在 Queue 类的私有部分声明的。所以，虽然 Queue 的方法可直接访问 Node 的成员，但使用 Queue 类的客户不能这样做。

总之，类声明的位置决定了类的作用域或可见性。类可见后，访问控制规则（公有、保护、私有、友元）将决定程序对嵌套类成员的访问权限。

## 15.2.2 模板中的嵌套

您知道，模板很适合用于实现诸如 Queue 等容器类。您可能会问，将 Queue 类定义转换为模板时，是否会由于它包含嵌套类而带来问题？答案是不会。程序清单 15.5 演示了如何进行这种转换。和类模板一样，该头文件也包含类模板和方法函数模板。

程序清单 15.5 queuetp.h

```cpp
// queuetp.h -- queue template with a nested class
#ifndef QUEUETP_H_
#define QUEUETP_H_

template <class Item>
class QueueTP
{
private:
    enum {Q_SIZE = 10};
    // Node is a nested class definition
    class Node
    {
    public:
        Item item;
        Node * next;
        Node(const Item & i):item(i), next(0){ }
    };
    Node * front;          // pointer to front of Queue
    Node * rear;          // pointer to rear of Queue
    int items;          // current number of items in Queue
    const int qsize;   // maximum number of items in Queue
    QueueTP(const QueueTP & q) : qsize(0) {}
    QueueTP & operator=(const QueueTP & q) { return *this; }
public:
    QueueTP(int qs = Q_SIZE);
    -QueueTP();
    bool isempty() const
    {
```

```cpp
return items == 0;
}
bool isfull() const
{
    return items == qsize;
}
int queuecount() const
{
    return items;
}
bool enqueue(const Item &item); // add item to end
bool dequeue(Item &item);      // remove item from front
};
// QueueTP methods
template <class Item>
QueueTP<Item>::QueueTP(int qs) : qsize(qs)
{
    front = rear = 0;
    items = 0;
}

template <class Item>
QueueTP<Item>::~QueueTP()
{
    Node * temp;
    while (front != 0)      // while queue is not yet empty
    {
        temp = front;       // save address of front item
        front = front->next;// reset pointer to next item
        delete temp;       // delete former front
    }
}

// Add item to queue
template <class Item>
bool QueueTP<Item>::enqueue(const Item & item)
{
    if (isfull()) {
        return false;
    Node * add = new Node(item);   // create node
// on failure, new throws std::bad_alloc exception
    items++;
    if (front == 0)          // if queue is empty,
        front = add;       // place item at front
    else
        rear->next = add;   // else place at rear
    rear = add;               // have rear point to new node
    return true;
}

// Place front item into item variable and remove from queue
template <class Item>
bool QueueTP<Item>::dequeue(Item & item)
{
    if (front == 0)
```

```c
return false;
    item = front->item;      // set item to first item in queue
    items--;
    Node * temp = front;     // save location of first item
    front = front->next;     // reset front to next item
    delete temp;             // delete former first item
    if (items == 0)
        rear = 0;
    return true;
}
#endif
```

程序清单 15.5 中模板有趣的一点是，Node 是利用通用类型 Item 来定义的。所以，下面的声明将导致 Node 被定义成用于存储 double 值:

```txt
QueueTp<double>_ dq;
```

而下面的声明将导致 Node 被定义成用于存储 char 值:

```txt
QueueTp<char>.cq;
```

这两个 Node 类将在两个独立的 QueueTP 类中定义，因此不会发生名称冲突。即一个节点的类型为 QueueTP&lt;double&gt;::Node，另一个节点的类型为 QueueTP&lt;char&gt;::Node。

程序清单15.6是一个小程序，可用于测试这个新的类。

程序清单 15.6 nested.cpp

```cpp
// nested.cpp -- using a queue that has a nested class
#include <iostream>

#include <string>
#include "queuetp.h"

int main()
{
    using std::string;
    using std::cin;
    using std::cout;

    QueueTP<string> cs(5);
    string temp;

    while (!cs.isfull())
    {
        cout << "Please enter your name. You will be "
            "served in the order of arrival.\n"
            "name: ";
        getline(cin, temp);
        cs.enqueue(temp);
    }
    cout << "The queue is full. Processing begins!\n";

    while (!cs.isempty())
    {
        cs.dequeue(temp);
        cout << "Now processing " << temp << "...\n";
```

```scss
}
    return 0;
}
```

程序清单 15.5 和程序清单 15.6 组成的程序的运行情况如下:

```txt
Please enter your name. You will be served in the order of arrival.
name: Kinsey Millhone
Please enter your name. You will be served in the order of arrival.
name: Adam Dalgliesh
Please enter your name. You will be served in the order of arrival.
name: Andrew Dalziel
Please enter your name. You will be served in the order of arrival.
name: Kay Scarpetta
Please enter your name. You will be served in the order of arrival.
name: Richard Jury
The queue is full. Processing begins!
Now processing Kinsey Millhone...
Now processing Adam Dalgliesh...
Now processing Andrew Dalziel...
Now processing Kay Scarpetta...
Now processing Richard Jury...
```

## 15.3 异常

程序有时会遇到运行阶段错误，导致程序无法正常地运行下去。例如，程序可能试图打开一个不可用的文件，请求过多的内存，或者遭遇不能容忍的值。通常，程序员都会试图预防这种意外情况。C++异常为处理这种情况提供了一种功能强大而灵活的工具。异常是相对较新的 C++功能，有些老式编译器可能没有实现。另外，有些编译器默认关闭这种特性，您可能需要使用编译器选项来启用它。

讨论异常之前，先来看看程序员可使用的一些基本方法。作为试验，以一个计算两个数的调和平均数的函数为例。两个数的调和平均数的定义是:这两个数字倒数的平均值的倒数，因此表达式为:

```txt
2.0 × x × y / (x + y)
```

如果 y 是 x 的负值，则上述公式将导致被零除——一种不允许的运算。对于被零除的情况，很多新式编译器通过生成一个表示无穷大的特殊浮点值来处理，cout 将这种值显示为 Inf、inf、INF 或类似的东西；而其他的编译器可能生成在发生被零除时崩溃的程序。最好编写在所有系统上都以相同的受控方式运行的代码。

## 15.3.1 调用 abort()

对于这种问题，处理方式之一是，如果其中一个参数是另一个参数的负值，则调用 abort() 函数。Abort() 函数的原型位于头文件 cstdlib（或 stdlib.h）中，其典型实现是向标准错误流（即 cerr 使用的错误流）发送消息 abnormal program termination（程序异常终止），然后终止程序。它还返回一个随实现而异的值，告诉操作系统（如果程序是由另一个程序调用的，则告诉父进程），处理失败。abort() 是否刷新文件缓冲区（用于存储读写到文件中的数据的内存区域）取决于实现。如果愿意，也可以使用 exit()，该函数刷新文件缓冲区，但不显示消息。程序清单 15.7 是一个使用 abort() 的小程序。

## 程序清单 15.7 error1.cpp

```cpp
//error1.cpp -- using the abort() function
#include <iostream>
#include <cstdlib>
double hmean(double a, double b);
```

```cpp
int main()
{
    double x, y, z;

    std::cout << "Enter two numbers: ";
    while-(std::cin >> x >> y)
    {
        z = hmean(x,y);
        std::cout << "Harmonic mean of " << x << " and " << y
            << " is " << z << std::endl;
        std::cout << "Enter next set of numbers <q to quft>: ";
    }
    std::cout << "Bye!\n";
    return 0;
}

double hmean(double a, double b)
{
    if (a == -b)
    {
        std::cout << "untenable arguments to hmean()\n";
        std::abort();
    }
    return 2.0 * a * b / (a + b);
}
```

程序清单 15.7 中程序的运行情况如下:

```txt
Enter two numbers: 3 6
Harmonic mean of 3 and 6 is 4
Enter next set of numbers <q to quit>: 10 -10
untenable arguments to hmean()
abnormal program termination
```

注意，在hmean()中调用abort()函数将直接终止程序，而不是先返回到main()。一般而言，显示的程序异常中断消息随编译器而异，下面是另一种编译器显示的消息:

```txt
This application has requested the Runtime-to terminate it in an unusual way. Please contact the application's support team for more information.
```

为了避免异常终止，程序应在调用 hmean(-)函数之前检查 x 和 y 的值。然而，依靠程序员来执行这种检查是不安全的。

## 15.3.2 返回错误码

一种比异常终止更灵活的方法是，使用函数的返回值来指出问题。例如，ostream 类的-get（void）成员通常返回下一个输入字符的 ASCII 码，但到达文件尾时，将返回特殊值 EOF。对 hmean() 来说，这种方法不管用。任何数值都是有效的返回值，因此不存在可用于指出问题的特殊值。在这种情况下，可使用指针参数或引用参数来将值返回给调用程序，并使用函数的返回值来指出成功还是失败。istream 族重载>>运算符使用了这种技术的变体。通过告知调用程序是成功了还是失败了，使得程序可以采取除异常终止程序之外的其他措施。程序清单 15.8 是一个采用这种方式的示例，它将 hmean() 的返回值重新定义为 bool，让返回值指出成功了还是失败了，另外还给该函数增加了第三个参数，用于提供答案。

程序清单 15.8 error2.cpp

```cpp
//error2.cpp -- returning an error code
#include <iostream>
#include <cfloat>  // (or float.h) for DBL_MAX

bool hmean(double a, double b, double * ans);

int main()
{
    double x, y, z;

    std::cout << "Enter two numbers: ";
    while (std::cin >> x >> y)
    {
        if (hmean(x,y,&z))
            std::cout << "Harmonic mean of " << x << " and " << y
                << " is " << z << std::endl;
        else
            std::cout << "One value should not be the negative "
                << "of the other - try again.\n";
        std::cout << "Enter next set of numbers <q to quit>: ";
    }
    std::cout << "Bye!\n";
    return 0;
}

bool hmean(double a, double b, double * ans)
{
    if (a == -b)
    {
        *ans = DBL_MAX;
        return false;
    }
    else
    {
        *ans = 2.0 * a * b / (a + b);
        return true;
    }
}
```

程序清单 15.8 中程序的运行情况如下:

```txt
Enter two numbers: 3 6
Harmonic mean of 3 and 6 is 4
Enter next set of numbers <q to quit>: 10 -10
One value should not be the negative of the other - try again.
Enter next set of numbers <q to quit>: 1 19
Harmonic mean of 1 and 19 is 1.9
Enter next set of numbers <q to quit>: q
Bye!
```

## 程序说明

在程序清单 15.8 中，程序设计避免了错误输入导致的恶果，让用户能够继续输入。当然，设计确实依靠用户检查函数的返回值，这项工作是程序员所不经常做的。例如，为使程序短小精悍，本书的程序清单都没有检查 cout 是否成功地处理了输出。

第三参数可以是指针或引用。对内置类型的参数，很多程序员都倾向于使用指针，因为这样可以明显看出是哪个参数用于提供答案。

另一种在某个地方存储返回条件的方法是使用一个全局变量。可能问题的函数可以在出现问题时将该全局变量设置为特定的值，而调用程序可以检查该变量。传统的 C 语言数学库使用的就是这种方法，它使用的全局变量名为 errno。当然，必须确保其他函数没有将该全局变量用于其他目的。

## 15.3.3 异常机制

下面介绍如何使用异常机制来处理错误。C++异常是对程序运行过程中发生的异常情况（例如被0除）的一种响应。异常提供了将控制权从程序的一个部分传递到另一部分的途径。对异常的处理有3个组成部分:

- 引发异常；
- 使用处理程序捕获异常；
- 使用try块。

程序在出现问题时将引发异常。例如，可以修改程序清单 15.7 中的 hmean()，使之引发异常，而不是调用 abort() 函数。throw 语句实际上是跳转，即命令程序跳到另一条语句。throw 关键字表示引发异常，紧随其后的值（例如字符串或对象）指出了异常的特征。

程序使用异常处理程序（exception handler）来捕获异常，异常处理程序位于要处理问题的程序中。catch 关键字表示捕获异常。处理程序以关键字 catch 开头，随后是位于括号中的类型声明，它指出了异常处理程序要响应的异常类型；然后是一个用花括号括起的代码块，指出要采取的措施。catch 关键字和异常类型用作标签，指出当异常被引发时，程序应跳到这个位置执行。异常处理程序也被称为 catch 块。

try 块标识其中特定的异常可能被激活的代码块，它后面跟一个或多个 catch 块。try 块是由关键字 try 指示的，关键字 try 的后面是一个由花括号括起的代码块，表明需要注意这些代码引发的异常。

要了解这3个元素是如何协同工作的，最简单的方法是看一个简短的例子，如程序清单15.9所示。

程序清单 15.9 = error3.cpp

```cpp
// error3.cpp -- using an exception
#include <iostream>
double hmean(double a, double-b);

int_main()
{
    double-x, y, z;

    std::cout << "Enter two numbers: ";
    while (std::cin >> x >> y)
    {
        try { // start of try block
            z = hmean(x,y);
        } // end of try block_
        catch (const char * s) // start of exception handler
        {
            std::cout<< s << std::endl;
            std::cout<< "Enter a new pair of numbers:";
            continue;
        } - // end of handler
        std::cout << "Harmonic mean of " << x << " and " << y
            << " is " << z << std::endl;
        std::cout << "Enter next set of numbers<q to quit>: ";
    }
    std::cout << "Bye!\n";
```

```txt
return 0;
}

double hmean(double a, double b)
{
    if (a == -b)
        throw "bad hmean() arguments: a = -b not allowed";
    return 2.0 * a * b / (a + b);
}
```

程序清单 15.9 中程序的运行情况如下:

```txt
Enter two numbers: 3 6
Harmonic mean of 3 and 6 is 4
Enter next set of numbers <q to quit>: 10 -10
bad hmean() arguments: a = -b not allowed
Enter a new pair of numbers: 1 19
Harmonic mean of 1 and 19 is 1.9
Enter next set of numbers <q to quit>: q
Bye!
```

## 程序说明

在程序清单 15.9 中，try 块与下面类似:

```txt
try {                               // start of try block
    z = hmean(x,y);
}                             // end of try block
```

如果其中的某条语句导致异常被引发，则后面的 catch 块将对异常进行处理。如果程序在 try 块的外面调用 hmean()，将无法处理异常。

引发异常的代码与下面类似:

```txt
if (a == -b)
    throw "bad hmean() arguments: a = -b not allowed";
```

其中被引发的异常是字符串 “bad hmean()arguments: a = -b not allowed”。异常类型可以是字符串（就像这个例子中那样）或其他 C++ 类型；通常为类类型，本章后面的示例将说明这一点。

执行 throw 语句类似于执行返回语句，因为它也将终止函数的执行；但 throw 不是将控制权返回给调用程序，而是导致程序沿函数调用序列后退，直到找到包含 try 块的函数。在程序清单 15.9 中，该函数是调用函数。稍后将有一个沿函数调用序列后退多步的例子。另外，在这个例子中，throw 将程序控制权返回给 main()。程序将在 main() 中寻找与引发的异常类型匹配的异常处理程序（位于 try 块的后面）。

处理程序（或 catch 块）与下面类似:

```cpp
catch (char * s)  // start of exception handler
{
    std::cout << s << std::endl;
    sdt::cout << "Enter a new pair of numbers: ";
    continue;
}                                      // end of handler
```

catch 块点类似于函数定义，但并不是函数定义。关键字 catch 表明这是一个处理程序，而 char\*s 则表明该处理程序与字符串异常匹配。s 与函数参数定义极其类似，因为匹配的引发将被赋给 s。另外，当异常与该处理程序匹配时，程序将执行括号中的代码。

执行完 try 块中的语句后，如果没有引发任何异常，则程序跳过 try 块后面的 catch 块，直接执行处理程序后面的第一条语句。因此处理值 3 和 6 时，程序清单 15.9 中程序执行报告结果的输出语句。

接下来看将 10 和 -10 传递给 hmean() 函数后发生的情况。If 语句导致 hmean() 引发异常。这将终止hmean()的执行。程序向后搜索时发现，hmean()函数是从 main()中的 try 块中调用的，因此程序查找与异常类型匹配的 catch 块。程序中唯一的一个 catch 块的参数为 char\*，因此它与引发异常匹配。程序将字符串 “bad hmean()arguments: a = -b not allowed” 赋给变量 s，然后执行处理程序中的代码。处理程序首先打印 s——捕获的异常，然后打印要求用户输入新数据的指示，最后执行 continue 语句，命令程序跳过 while 循环的剩余部分，跳到起始位置。continue 使程序跳到循环的起始处，这表明处理程序语句是循环的一部分，而 catch 行是指引程序流程的标签（参见图 15.2）。

![](images/page_638_image_3.jpg)

<details>
<summary>flowchart</summary>

This image displays a C-style loop flowchart for an algorithm named 'hmean', illustrating the sequence of operations including checking if the function is true, checking if it is true, and returning to the previous state.
</details>

图 15.2 出现异常时的程序流程

您可能会问，如果函数引发了异常，而没有 try 块或没有匹配的处理程序时，将会发生什么情况。在默认情况下下，程序最终将调用 abort() 函数，但可以修改这种行为。稍后将讨论这个问题。

## 15.3.4 将对象用作异常类型

通常，引发异常的函数将传递一个对象。这样做的重要优点之一是，可以使用不同的异常类型来区分不同的函数在不同情况下引发的异常。另外，对象可以携带信息，程序员可以根据这些信息来确定引发异常的原因。同时，catch块可以根据这些信息来决定采取什么样的措施。例如，下面是针对函数hmean()引发的异常而提供的一种设计:

```cpp
class bad_hmean
{
private:
    double v1;
    double v2;
public:
    bad_hmean(int a = 0, int b = 0) : v1(a), v2(b){}
    void mesg();
};

inline void bad_hmean::mesg()
{
```

```cpp
std::cout << "hmean(" << v1 << ", " << v2 <<"): "
              << "invalid arguments: a = -b\n";
```

可以将一个 bad\_hmean 对象初始化为传递给函数 hmcan() 的值，而方法 mesg() 可用于报告问题（包括传递给函数 hmena() 的值）。函数 hmean() 可以使用下面这样的代码:

```javascript
if (a == -b)
    throw bad_hmean(a,b);
```

上述代码调用构造函数 bad\_hmean()，以初始化对象，使其存储参数值。

程序清单 15.10 和 15.11 添加了另一个异常类 bad\_gmean 以及另一个名为 gmean() 的函数，该函数引发 bad\_gmean 异常。函数 gmean() 计算两个数的几何平均值，即乘积的平方根。这个函数要求两个参数都不为负，如果参数为负，它将引发异常。程序清单 15.10 是一个头文件，其中包含异常类的定义:而程序清单 15.11 是一个示例程序，它使用了该头文件。注意，try 块的后面跟着两个 catch 块:

```txt
try {                  // start of try block
...
}// end of try block
catch (bad_hmean & bg)    // start of catch block
{
...
}
catch (bad_gmean & hg)
{
...
}// end of catch block
```

如果函数 hmean()引发 bad\_hmean 异常，第一个 catch 块将捕获该异常；如果 gmean()引发 bad\_gmean 异常，异常将逃过第一个 catch 块，被第二个 catch 块捕获。

程序清单 15.10 exc\_mean.h

```cpp
// exc_mean_h --- exception classes for_hmean{}; gmean():
#include <iostream>
class bad_hmean
{
private:
    double v1;
    double v2;
public:
    bad_hmean(double a = 0, double b = .0); v1(a), v2(b) {}
    void mesg();
};
inline void bad_hmean::mesg(){
{
    std: cout << "hmean(" << v1 << ", " << v2 << ")."
        << "invalid arguments: a = -b\n";
}
class bad_gmean
{
public:
    double v1;
    double.v2;
    bad_gmean(double a = 0, double b = .0); v1(a), v2(b) {}
```