```cpp
cout << "Name: " <<:fullname << "\n";
    cout << "Employee ID: " << id << "\n";
}

void Waiter::Show() const
{
    Worker::Show();
    cout << "Panache rating: " << panache << "\n";
}
void HeadWaiter::Show() const
{
    Waiter::Show();
    cout << "Presence rating: " << presence << "\n";
}
```

然而，这种递增的方式对 SingingWaiter 示例无效。下面的方法将无效，因为它忽略了 Waiter 组件:

```rust
void SingingWaiter::Show()
{
    Singer::Show();
}
```

可以通过同时调用 Waiter 版本的 Show() 来补救:

```cpp
void SingingWaiter::Show()
{
    Singer::Show()
    _Waiter::Show();
}
```

然而，这将显示姓名和 ID 两次，因为 Singer::Show() 和 Waiter::Show() 都调用了 Worker::Show()。

如果解决呢？一种办法是使用模块化方式，而不是递增方式，即提供一个只显示 Worker 组件的方法和一个只显示 Waiter 组件或 Singer 组件（而不是 Waiter 和 Worker 组件）的方法。然后，在 SingingWaiter::Show() 方法中将组件组合起来。例如，可以这样做:

```cpp
void Worker::Data() const
{
    cout << "Name: " << fulname << "\n";
    cout << "Employee ID: " << id << "\n";
}
void Waiter::Data() const
{
    cout << "Panache rating: " << panache << "\n";
}
void Singer::Data() const
{
    cout << "Vocal range: " << pv[voice] << "\n";
}
void SingingWaiter::Data() const
{
    Singer::Data();
    Waiter::Data();
}
void SingingWaiter::Show() const
```

```cpp
cout << "Category: singing waiter\n";
Worker::Data();
Data();
}
```

与此相似，其他 Show() 方法可以组合适当的 Data() 组件。

采用这种方式，对象仍可使用 Show() 方法。而 Data() 方法只在类内部可用，作为协助公有接口的辅助方法。然而，使 Data() 方法成为私有的将阻止 Waiter 中的代码使用 Worker::Data()，这正是保护访问类的用武之地。如果 Data() 方法是保护的，则只能在继承层次结构中的类中使用它，在其他地方则不能使用。

另一种办法是将所有的数据组件都设置为保护的，而不是私有的，不过使用保护方法（而不是保护数据）将可以更严格地控制对数据的访问。

Set()方法取得数据，以设置对象值，该方法也有类似的问题。例如，SingingWaiter::Set()应请求 Worker 信息一次，而不是两次。对此，可以使用前面的解决方法。可以提供一个受保护的 Get()方法，该方法只请求一个类的信息，然后将使用 Get()方法作为构造块的 Set()方法集合起来。

总之，在祖先相同时，使用 MI 必须引入虚基类，并修改构造函数初始化列表的规则。另外，如果在编写这些类时没有考虑到 MI，则还可能需要重新编写它们。程序清单 14.10 列出了修改后的类声明，程序清单 14.11 列出实现。

程序清单 14.10- workermi.h

```cpp
// workermi :h -- working classes with MI
#ifndef WORKERMI _H
#define WORKERMI _H

#include <string>

class Worker // an abstract base class
{
private:
    std::string fullname;
    long id;
protected:
    virtual void Data() const;
    virtual void Get();
public:
    Worker() : fullname("no one") : id(0L) {}
    Worker(const std : string & s, long n);
        fullname(s), id(n) {}
    virtual -Worker() = 0; // pure virtual function
    virtual void Set() = 0;
    virtual void Show() const = 0;
};
class Waiter : virtual public Worker
{
private:
    int panache;
protected:
    void Data() const;
    void Get();
```

```cpp
public:
    Waiter() : Worker(), panache(0) {-}
    Waiter(const std::string & s, long n, int p = 0)
        : Worker(s, n), panache(p) {-}
    Waiter(const Worker & wk, int_p = 0)
        : Worker(wk), panache(p) {-}
    void Set();
    void Show() const;
};

class Singer : virtual public Worker
{
protected:
enum {other, alto, contralto, soprano,
            bass, baritone, tenor};
enum {Vtypes = 7};
void Data() const;
void Get();
private:
static char *pv[Vtypes]; // string equivs of voice types
int voice;
public:
Singer() : Worker(), voice(other) {-}
Singer(const std::string & s, long n, int v = other)
: Worker(s, n), voice(v) {-}
Singer(const Worker & wk, int v = other)
: Worker(wk), voice(v) {-}
void Set();
void Show() const;
};

// multiple inheritance
class SingingWaiter : public Singer, public Waiter
{
protected:
    void Data() const;
    void Get();
public:
    SingingWaiter() {-}
    SingingWaiter(const std::string & s, long n, int p = 0,
                    int v = other)
        : Worker(s,n), Waiter(s, n, p), Singer(s, n, v) {-}
    SingingWaiter(const Worker & wk, int p = 0, int v = other)
        : Worker(wk), Waiter(wk,p), Singer(wk,v) {-}
    SingingWaiter(const Waiter & wt, int v = other)
        : Worker(wt), Waiter(wt), Singer(wt,v) {-}
    SingingWaiter(const Singer & wt, int p = 0)
        : Worker(wt), Waiter(wt,p), Singer(wt)-{-}
    void Set();
    void Show() const;
};

#endif
```

程序清单 14.1f workermi.cpp

```cpp
// workermi.cpp -- working class methods with MI
#include "workermi.h"
#include <iostream>
using_std::cout;
using_std::cin;
using_std::endl;
// Worker methods
Worker::-Worker(Γ { }

// protected methods
void Worker::Data() const
{
    cout << "Name: " << fulName<< endl;
    cout << "Employee-ID: " << id<< endl;
}

void Worker::Get()
{
    getline(cin, fullname);
    cout << "Enter worker's ID: ";
    cin >> id;
    while (cin.get() != '\n')
        continue;
}

// Waiter methods
void Waiter::Set()
{
    cout << "Enter waiter's name: ";
    Worker::Get();
    Get();
}

void Waiter::Show() const
{
    cout << "Category: waiter\n";
    Worker::Data();
    Data();
}

// protected methods
void Waiter::Data() const
{
    cout << "Panache rating: " << panache << endl;
}
void Waiter::Get()
{
    cout << "Enter waiter's panache rating: ";
    cin >> panache;
    while (cin.get() != '\n')
        continue;
}
```

```cpp
//-Singer methods

char * Singer::pv[Singer::Vtypes] = {"other", "alto", "contralto",
            "soprano", "bass", "baritone", "tenor"};

void Singer::Set()
{
    cout << "Enter-singer's name: ";_
    Worker::Get();
    Get();
}

void Singer::Show() const
{
    cout << "Category: singer\n";
    Worker::Data();
    Data();
}

// protected methods
void Singer::Data() const
{
    cout << "Vocal range: " << pv[voice] << endl;
}

void Singer::Get()
{
    cout << "Enter number for singer's vocal range:\n";
    int i;
    for (i = 0; i < Vtypes; i++)
    {
        cout << i << ": " << pv[i] << "   ";
        if ( i % 4 == 3)
            cout << endl;
    }
    if (i % 4 != 0)
        cout << '\n';
    cin >> voice;
    while (cin.get() != '\n')
        continue;
}

// SingingWaiter methods
void SingingWaiter::Data() const
{
    Singer::Data();
    Waiter::Data();
}

void SingingWaiter::Get()
{
    Waiter::Get();
    Singer::Get();
}
```

```cpp
void SingingWaiter::Set()
{
    cout << "Enter singing waiter's name: ";
    Worker::Get();
    Get();
}

void SingingWaiter::Show() const
{
    cout << "Category: singing waiter\n";
    Worker::Data();
    Data();
}
```

当然，好奇心要求我们测试这些类，程序清单 14.12 提供了测试代码。注意，该程序使用了多态属性，将各种类的地址赋给基类指针。另外，该程序还在下面的检测中使用了 C-风格字符串库函数 strchr():

```txt
while (strchr("wstq", choice) == NULL)
```

该函数返回参数 choice 指定的字符在字符串 “wstq” 中第一次出现的地址，如果没有这样的字符，则返回 NULL 指针。使用这种检测比使用 if 语句将 choice 指定的字符同每个字符进行比较简单。

请将程序清单 14.12 与 workermi.cpp 一起编译。

程序清单 14.12 workmi.cpp

```cpp
// workmi.cpp -- multiple inheritance
// compile with workermi.cpp
#include <iostream>
#include <cstring>
#include "workermi.h"
const int SIZE = 5;

int main()
{
    using std::cin;
    using std::cout;
    using std::endl;
    using std::strchr;

    Worker * lolas[SIZE];

    int ct;
    for (ct = 0; ct < SIZE; ct++)
    {
        char choice;
        cout << "Enter the employee category:\n"
            << "w: waiter s: singer "
            << "t: singing waiter q: quit\n";
        cin >> choice;
        while (strchr("wstq", choice) == NULL)
        {
            cout << "Please enter a w, s, t, or q: ";
            cin >> choice;
        }
        if (choice == 'q')
            break;
```

```cpp
switch(choice)
{
    case 'w':  lolas[ct] = new Waiter;
        break;
    case 's':  lolas[ct] = new Singer;
        break;
    case 't':  lolas[ct] = new SingingWaiter;
        break;
}
cin.get();
lolas[ct]->Set();
}

cout << "\nHere is your staff:\n";
int i;
for (i = 0; i < ct; i++)
{
    cout << endl;
    lolas[i]->Show();
}
for (i = 0; i <- ct; i++)
    delete lolas[i];
cout << "Bye.\n";
return 0;
}
```

下面是程序清单14.10～程序清单14.12组成的程序的运行情况:

```snap
Enter the employee category:
w: waiter s: singer t: singing waiter q: quit
w
Enter waiter's_name: Wally Slipshod
Enter worker's ID: 1040
Enter waiter's panache rating: 4
Enter the employee category:
w: waiter s: singer t: singing waiter q: quit
s
Enter singer's name: Sinclair Parma
Enter worker's ID: 1044
Enter number for singer's vocal range:
0: other 1: alto 2: contralto 3: soprano
4: bass 5: baritone 6: tenor
5
Enter the employee category:
w: waiter s: singer t: singing waiter q: quit
t
Enter singing waiter's name: Natasha Gargalova
Enter worker's ID: 1021
Enter waiter's panache rating: 6
Enter number for singer's vocal range:
0: other 1: alto—2: contralto. 3: soprano
4: bass 5: baritone 6: tenor
3
Enter the employee category:
w: waiter s: singer t: singing waiter q: quit
q
```

```txt
Here is your staff:

Category: waiter
Name: Wally Slipshod
Employee ID: 1040
Panache rating: 4

Category: singer
Name: Sinclair Parma
Employee ID: 1044
Vocal range: baritone

Category: singing waiter
Name: Natasha Gargalova
Employee ID: 1021
Vocal range: soprano
Panache rating: 6
Bye.
```

下面介绍其他一些有关 MI 的问题。

## 1. 混合使用虚基类和非虚基类

再来看一下通过多种途径继承一个基类的派生类的情况。如果基类是虚基类，派生类将包含基类的一个子对象；如果基类不是虚基类，派生类将包含多个子对象。当虚基类和非虚基类混合时，情况将如何呢？例如，假设类B被用作类C和D的虚基类，同时被用作类X和Y的非虚基类，而类M是从C、D、X和Y派生而来的。在这种情况下，类M从虚派生祖先（即类C和D）那里共继承了一个B类子对象，并从每一个非虚派生祖先（即类X和Y）分别继承了一个B类子对象。因此，它包含三个B类子对象。当类通过多条虚途径和非虚途径继承某个特定的基类时，该类将包含一个表示所有的虚途径的基类子对象和分别表示各条非虚途径的多个基类子对象。

## 2. 虚基类和支配

使用虚基类将改变 C++ 解析二义性的方式。使用非虚基类时，规则很简单。如果类从不同的类那里继承了两个或更多的同名成员（数据或方法），则使用该成员名时，如果没有用类名进行限定，将导致二义性。但如果使用的是虚基类，则这样做不一定会导致二义性。在这种情况下，如果某个名称优先于（dominates）其他所有名称，则使用它时，即便不使用限定符，也不会导致二义性。

那么，一个成员名如何优先于另一个成员名呢？派生类中的名称优先于直接或间接祖先类中的相同名称。例如，在下面的定义中:

```txt
class B
{
public:
    short q();
    ...
};
class C : virtual public B
{
public:
    long q();
    int omg()
    ...
};
```

```txt
class D : public C
{
    ...
};

class E : virtual public B
{
private:
    int -omg();
    ...
};
class F: public-D, public
{ -
    ...
};
```

类 C 中的 q() 定义优先于类 B 中的 q() 定义，因为类 C 是从类 B 派生而来的。因此，F 中的方法可以使用 q() 来表示 C::q()。另一方面，任何一个 omg() 定义都不优先于其他 omg() 定义，因为 C 和 E 都不是对方的基类。所以，在 F 中使用非限定的 omg() 将导致二义性。

虚二义性规则与访问规则无关，也就是说，即使 E::omg() 是私有的，不能在 F 类中直接访问，但使用 omg() 仍将导致二义性。同样，即使 C::q() 是私有的，它也将优先于 D::q()。在这种情况下，可以在类 F 中调用 B::q()，但如果不限定 q()，则将意味着要调用不可访问的 C::q()。

## 14.3.3- MI小结

首先复习一下不使用虚基类的MI。这种形式的MI不会引入新的规则。然而，如果一个类从两个不同的类那里继承了两个同名的成员，则需要在派生类中使用类限定符来区分它们。即在从GunSlinger和PokersonPlayer派生而来的BadDude类中，将分别使用Gunslinger::draw()和PokersonPlayer::draw()来区分从这两个类那里继承的draw()方法。否则，编译器将指出二义性。

如果一个类通过多种途径继承了一个非虚基类，则该类从每种途径分别继承非虚基类的一个实例。在某些情况下，这可能正是所希望的，但通常情况下，多个基类实例都是问题。

接下来看一看使用虚基类的 MI。当派生类使用关键字 virtual 来指示派生时，基类就成为虚基类:

```javascript
class-marketing : public-virtual reality { ... };
```

主要变化（同时也是使用虚基类的原因）是，从虚基类的一个或多个实例派生而来的类将只继承了一个基类对象。为实现这种特性，必须满足其他要求:

有间接虚基类的派生类包含直接调用间接基类构造函数的构造函数，这对于间接非虚基类来说是非法的；
● 通过优先规则解决名称二义性。

正如您看到的，MI会增加编程的复杂程度。然而，这种复杂性主要是由于派生类通过多条途径继承同一个基类引起的。避免这种情况后，唯一需要注意的是，在必要时对继承的名称进行限定。

## 14.4 类模板

继承（公有、私有或保护）-和包含并不总是能够满足重用代码的需要。例如，Stack 类（参见第 10 章）和 Queue 类（参见第 12 章）都是容器类（container class），容器类设计用来存储其他对象或数据类型。例如，第 10 章的 Stack 类设计用于存储 unsigned long 值。可以定义专门用于存储 double 值或 string 对象的 Stack 类，除了保存的对象类型不同外，这两种 Stack 类的代码是相同的。然而，与其编写新的类声明，不如编写一个泛型（即独立于类型的）栈，然后将具体的类型作为参数传递给这个类。这样就可以使用通用的代码生成存储不同类型值的栈。第 10 章的 Stack 示例使用 typedef 处理这种需求。然而，这种方法有两个缺点:首先，每次修改类型时都需要编辑头文件；其次，在每个程序中只能使用这种技术生成一种栈，即不能让 typedef 同时代表两种不同的类型，因此不能使用这种方法在同一个程序中同时定义 int 栈和 string 栈。

C++的类模板为生成通用的类声明提供了一种更好的方法（C++最初不支持模板，但模板被引入后，就一直在演化，因此有的编译器可能不支持这里介绍的所有特性）。模板提供参数化（parameterized）类型，即能够将类型名作为参数传递给接收方来建立类或函数。例如，将类型名 int 传递给 Queue 模板，可以让编译器构造一个对 int 进行排队的 Queue 类。

C++库提供了多个模板类，本章前面使用了模板类 valarray，第 4 章介绍了模板类 vector 和 array，而第 16 章将讨论的 C++标准模板库（STL）提供了几个功能强大而灵活的容器类模板实现。本章将介绍如何设计一些基本的特性。

## 14.4.1 定义类模板

下面以第10章的Stack类为基础来建立模板。原来的类声明如下:

```cpp
typedef unsigned long Item;

class Stack
{
private:
    enum {MAX = 10};      // constant specific to class
    Item items[MAX];     // holds stack items
    int top;               // index for top stack item
public:
    Stack();
    bool isempty() const;
    bool isfull() const;
    // push() returns false if stack already is full, true otherwise
    bool push(const Item & item);   // add item to stack
    // pop() returns false if stack already is empty, true otherwise
    bool pop(Item & item);          // pop top into item
};
```

采用模板时，将使用模板定义替换 Stack 声明，使用模板成员函数替换 Stack 的成员函数。和模板函数一样，模板类以下面这样的代码开头:

```txt
template <class Type>
```

关键字 template 告诉编译器，将要定义一个模板。尖括号中的内容相当于函数的参数列表。可以把关键字 class 看作是变量的类型名，该变量接受类型作为其值，把 Type 看作是该变量的名称。

这里使用 class 并不意味着 Type 必须是一个类；而只是表明 Type 是一个通用的类型说明符，在使用模板时，将使用实际的类型替换它。较新的 C++ 实现允许在这种情况下使用不太容易混淆的关键字 typename 代替 class:

```txt
template <typename Type>  // newer choice
```

可以使用自己的泛型名代替 Type，其命名规则与其他标识符相同。当前流行的选项包括 T 和 Type，我们将使用后者。当模板被调用时，Type 将被具体的类型值（如 int 或 string）取代。在模板定义中，可以使用泛型名来标识要存储在栈中的类型。对于 Stack 来说，这意味着应将声明中所有的 typedef 标识符 Item 替换为 Type。例如，

```txt
Item items[MAX];  // holds stack items
```

应改为:

Type items[MAX]; // holds stack items

同样，可以使用模板成员函数替换原有类的类方法。每个函数头都将以相同的模板声明打头:

template &lt;class Type&gt;

同样应使用泛型名 Type 替换 typedef 标识符 Item。另外，还需将类限定符从 Stack::改为 Stack&lt;Type&gt;::。例如，

```cpp
bool Stack::push(const-Item & item)
{
...
}
应该为:
template <class Type>          // or template <typename:Type>
bool Stack<Type>::push(const Type & item)...
{
...
}
```

如果在类声明中定义了方法（内联定义），则可以省略模板前缀和类限定符。

程序清单 14.13 列出了类模板和成员函数模板。知道这些模板不是类和成员函数定义至关重要。它们是 C++ 编译器指令，说明了如何生成类和成员函数定义。模板的具体实现——如用来处理 string 对象的栈类——被称为实例化（instantiation）或具体化（specialization）。不能将模板成员函数放在独立的实现文件中（以前，C++ 标准确实提供了关键字 export，让您能够将模板成员函数放在独立的实现文件中，但支持该关键字的编译器不多；C++11 不再这样使用关键字 export，而将其保留用于其他用途）。由于模板不是函数，它们不能单独编译。模板必须与特定的模板实例化请求一起使用。为此，最简单的方法是将所有模板信息放在三个头文件中，并在要使用这些模板的文件中包含该头文件。

程序清单 14.13 stacktp.h

```cpp
// stacktp.h --- a stack template
#ifndef STACKTP_H
#define STACKTP_H
template <class Type>
class Stack
{
private:
    enum (MAX = 10);   // constant specific to class
    Type items[MAX];   // holds stack items
    int top;           // index for top stack item
public:
    Stack();
    bool isempty();
    bool isfull();
    bool push(const Type & item); // add item to stack
    bool pop(Type & item);   // pop top into item
};
template <class Type>
Stack<Type>::Stack()
{
    top = 0;
}
template <class Type>
bool Stack<Type>::isempty()
```

```cpp
{
    return top == 0;
}

template <class Type>
bool Stack<Type>::isfull()
{
    return top == MAX;
}

template <class Type>
bool Stack<Type>::push(const Type & item)
{
    if (top < MAX)
    {
        items[top++] = item;
        return true;
    }
    else
        return false;
}

template <class Type>
bool Stack<Type>::pop(Type & item)
{
    if (top > 0)
    {
        item = items[--top];
        return true;
    }
    else
        return false;
}

#endif
```

## 14.4.2 使用模板类

仅在程序包含模板并不能生成模板类，而必须请求实例化。为此，需要声明一个类型为模板类的对象，方法是使用所需的具体类型替换泛型名。例如，下面的代码创建两个栈，一个用于存储 int，另一个用于存储 string 对象:

```cpp
Stack<int> kernels;      // create a stack of ints
Stack<string> colonels;  // create a stack of string objects
```

看到上述声明后，编译器将按 Stack&lt;Type&gt;模板来生成两个独立的类声明和两组独立的类方法。类声明 Stack&lt;int&gt;将使用 int 替换模板中所有的 Type，而类声明 Stack&lt;string&gt;将用 string 替换 Type。当然，使用的算法必须与类型一致。例如，Stack 类假设可以将一个项目赋给另一个项目。这种假设对于基本类型、结构和类来说是成立的（除非将赋值运算符设置为私有的），但对于数组则不成立。

泛型标识符——例如这里的 Type——称为类型参数（type parameter），这意味着它们类似于变量，但赋给它们的不能是数字，而只能是类型。因此，在 kernel 声明中，类型参数 Type 的值为 int。

注意，必须显式地提供所需的类型，这与常规的函数模板是不同的，因为编译器可以根据函数的参数类型来确定要生成哪种函数:

```txt
template <class T>
void simple(T t) { cout << t << '\n';}
...
simple(2);      // generate void simple(int)
simple("two");  // generate void simple(const char *)
```

程序清单 14.14 修改了原来的栈测试程序（程序清单 11.12），使用字符串而不是 unsigned long 值作为订单 ID。

程序清单 14.14 stacktem.cpp

```cpp
// stacktem.cpp -- testing the template stack class
#include <iostream>
#include <string>
#include <cctype>
#include "stacktp.h"
using std::cin;
using std::cout;

int main()
{
    Stack<std::string> st;  // create an empty stack
    char_ch;
    std::string po;
    cout << "Please enter A to add a purchase order,\n"
        << "P to process a PO, or Q to quit.\n";
    while (cin >> ch && std::toupper(ch) != 'Q')
    {
        while (cin.get() != '\n')
            continue;
        if (!std::isalpha(ch))=
        {
            cout << '\a';
            continue;
        }
        switch(ch)
        {
            case 'A':
            case 'a': cout << "Enter a PO number to add: ";
                cin >> po;
                if (st.isfull())_
                    cout << "stack already full\n";
                else
                    st.push(po);
                break;
            case 'P':
            case 'p': if (st.isempty())
                cout << "stack already empty\n";
            else {
                st.pop(po);
                cout << "PO #" << po << " popped\n";
                break;
            }
        }
        cout << "Please enter A to add a purchase order,\n"
            << "P to process a PO, or Q to quit.\n";
```

```cpp
}
    cout << "Bye\n";
    return 0;
}
```

程序清单14.14所示程序的运行情况如下:

```txt
Please enter A to add a purchase order,
P to process a PO, or Q to quit.
```

A

```txt
Enter a PO number to=add: red911porsche
Please enter A to add—a purchase order,
P to process a-PO, or Q-to quit.
```

A

```txt
Enter a PO number to add: blueR8audi
Please enter A-to-add a purchase order,
P-to process a=PO, or Q-to quit.
```

A

```txt
Enter a PO number to add: silver747boeing
Please enter A to add a purchase order,
P to process a PO, or Q to quit.
```

P

```txt
PO #silver747boeing popped
Please enter A to add a purchase order,
P to process a PO, or Q-to quit.
```

P

```txt
PO #blueR8audi popped
Please enter A to add a purchase order,
P to process a PO, or Q to quit.
```

P

```txt
PO #red911porsche popped
Please enter A to add a purchase order,
P to process a PO, or Q to quit.
```

P

```txt
stack already empty
Please enter A to add a purchase order,
P to process a PO, or Q to quit.
```

Q

Bye

## 14.4.3 深入探讨模板类

可以将内置类型或类对象用作类模板 Stack&lt;Type&gt; 的类型。指针可以吗？例如，可以使用 char 指针替换程序清单 14.14 中的 string 对象吗？毕竟，这种指针是处理 C-风格字符串的内置方式。答案是可以创建指针栈，但如果不对程序做重大修改，将无法很好地工作。编译器可以创建类，但使用效果如何就因人而异了。下面解释程序清单 14.14 不太适合使用指针栈的原因，然后介绍一个指针栈很有用的例子。

## 1. 不正确地使用指针栈

我们将简要地介绍3个试图对程序清单14.14进行修改，使之使用指针栈的简单（但有缺陷的）示例。这几个示例揭示了设计模板时应牢记的一些教训，切忌盲目使用模板。这3个示例都以完全正确的Stack&lt;Type&gt;模板为基础:

```txt
Stack<char *> st; // create a stack for pointers-to-char
```

版本1将程序清单14.14中的:

```txt
string po;
```

替换为:

```txt
char * po;
```

这旨在用 char 指针而不是 string 对象来接收键盘输入。这种方法很快就失败了，因为仅仅创建指针，没有创建用于保存输入字符串的空间（程序将通过编译，但在 cin 试图将输入保存在某些不合适的内存单元中时崩溃）。

版本2将

```txt
string po;
```

替换为:

```txt
char po[40];
```

这为输入的字符串分配了空间。另外，po 的类型为 char \*，因此可以被放在栈中。但数组完全与 pop() 方法的假设相冲突:

```cpp
template <class Type>
bool Stack<Type>::pop(Type & item)
{
    if (top > 0)_
    {
        item = items[--top];
        return true;
    }
    else
        return false;
}
```

首先，引用变量 item=必须引用某种类型的左值，而不是数组名。其次，代码假设可以给 item 赋值。即使 item 能够引用数组，也不能为数组名赋值。因此这种方法失败了。

版本3将

```txt
string po;
```

替换为:

```javascript
char * po = new char[40];
```

这为输入的字符串分配了空间。另外，po 是变量，因此与 pop() 的代码兼容。然而，这里将会遇到最基本的问题:只有一个 pop 变量，该变量总是指向相同的内存单元。确实，在每当读取新字符串时，内存的内容都将发生改变，但每次执行压入操作时，加入到栈中的的地址都相同。因此，对栈执行弹出操作时，得到的地址总是相同的，它总是指向读入的最后一个字符串。具体地说，栈并没有保存每一个新字符串，因此没有任何用途。

## 2. 正确使用指针栈

使用指针栈的方法之一是，让调用程序提供一个指针数组，其中每个指针都指向不同的字符串。把这些指针放在栈中是有意义的，因为每个指针都将指向不同的字符串。注意，创建不同指针是调用程序的职责，而不是栈的职责。栈的任务是管理指针，而不是创建指针。

例如，假设我们要模拟下面的情况。某人将一车文件夹交付给了 Plodson。如果 Plodson 的收取篮（in-basket）是空的，他将取出车中最上面的文件夹，将其放入收取篮；如果收取篮是满的，Plodson 将取出篮中最上面的文件，对它进行处理，然后放入发出篮（out-basket）中。如果收取篮既不是空的也不是满的，Plodson 将处理收取篮中最上面的文件，也可能取出车中的下一个文件，把它放入收取篮。他采取了自认为是比较鲁莽的行动——扔硬币来决定要采取的措施。下面来讨论他的方法对原始文件处理顺序的影响。

可以用一个指针数组来模拟这种情况，其中的指针指向表示车中文件的字符串。每个字符串都包含文件所描述的人的姓名。可以用栈表示收取篮，并使用第二个指针数组来表示发出篮。通过将指针从输入数组压入到栈中来表示将文件添加到收取篮中，同时通过从栈中弹出项目，并将它添加到发出篮中来表示处理文件。

应考虑该问题的各个方面，因此栈的大小必须是可变的。程序清单 14.15 重新定义了 Stack&lt;Type&gt;类，使 Stack 构造函数能够接受一个可选大小的参数。这涉及到在内部使用动态数组，因此，Stack 类需要包含一个析构函数、一个复制构造函数和一个赋值运算符。另外，通过将多个方法作为内联函数，精减了代码。

程序清单 14.15 stcktp1.h

```cpp
// stcktp1.h -- modified Stack template
#ifndef STCKTP1_H_
#define STCKTP1_H_

template <class Type>
class Stack
{
private:
    enum {SIZE = 10};      // default size
    int stacksize;
    Type * items;          // holds stack items
    int top;                // index for top stack item
public:
    explicit Stack(int ss = SIZE);
    Stack(const Stack & st);
    ~Stack() { delete [] items; }
    bool isempty() { return top == 0; }
    bool isfull() { return top == stacksize; }
    bool push(const Type & item);   // add item to stack
    bool pop(Type & item);        // pop top into item
    Stack & operator=(const Stack & st);
};

template <class Type>
Stack<Type>::Stack(int ss) : stacksize(ss), top(0)
{
    items = new Type [stacksize];
}

template <class Type>
Stack<Type>::Stack(const Stack & st)
{
    stacksize = st.stacksize;
    top = st.top;
    items = new Type [stacksize];
    for (int i = 0; i < top; i++)
        items[i] = st.items[i];
}
template <class Type>
bool Stack<Type>::push(const Type & item)
{
    if (top < stacksize)
    {
        items[top++] = item;
        return true;
    }
    else
        return false;
}
```

```cpp
template <class Type>
bool Stack<Type>::pop(Type & item)
{
    if (top > 0)
    {
        item = items[--top];
        return true;
    }
    else
        return false;
}

template <class Type>
Stack<Type> & Stack<Type>::operator=(const Stack<Type> & st)
{
    if (this == &st)
        return *this;
    delete [] items;
    stacksize = st.stacksize;
    top = st.top;
    items = new Type [stacksize];
    for (int i = 0; i < top; i++)
        items[i] = st.items[i];
    return *this;
}

#endif
```

原型将赋值运算符函数的返回类型声明为 Stack 引用，而实际的模板函数定义将类型定义为 Stack&lt;Type&gt;。前者是后者的缩写，但只能在类中使用。即可以在模板声明或模板函数定义内使用 Stack，但在类的外面，即指定返回类型或使用作用域解析运算符时，必须使用完整的 Stack&lt;Type&gt;。

程序清单 14.16 中的程序使用新的栈模板来实现 Plodson 模拟，它像以前介绍的模拟那样使用 rand()、srand() 和 time() 来生成随机数，这里是随机生成 0 和 1，来模拟掷硬币的结果。

程序清单 14.16 stkoptr1.cpp

```cpp
// stkoptrl.cpp -- testing stack of pointers
#include <iostream>
#include <cstdlib>      // for rand(), srand()
#include <ctime>          // for time()
#include "stcktp1.h"
const int Num = 10;
int main()
{
    std::srand(std::time(0)); // randomize rand()
    std::cout << "Please enter stack size: ";
    int stacksize;
    std::cin >> stacksize;
// create an empty stack with stacksize slots
    Stack<const char *> st(stacksize);

// in basket
    const char * in[Num] = {
        " 1: Hank Gilgamesh", " 2: Kiki Ishtar",
```

```txt
" 3: Betty Rocker", " 4: Ian Flagranti",
" 5: Wolfgang Kibble", " 6: Portia Koop",
" 7: Joy Almondo", " 8: Xaverie Paprika",
" 9: Juan_Moore", "F0: Misha Mache"
};
// out basket
const char * out[Num];

int processed = 0;
int nextin== 0;
while (processed < Num)
{
    if (st.isempty{}) {
        st.push(in[nextin++]);
    else if (st.isfull()) {
        st.pop(out[processed++]);
    else if (std::rand() % 2 && nextin < Num) // 50-50 chance
        st.push(in[nextin++]);
    else
        st.pop(out[processed++]);
}
for (int i = 0; i < Num; i++)
    std::cout << out[i] << std::endl;

std::cout << "Bye\n";
return 0;
}
```

下面是程序清单 14:16 所示程序的两次运行情况。注意，由于使用了随机特性，每次运行时，文件最后的顺序都可能不同，即使栈大小保持不变。

```txt
Please enter stack size: 5
2: Kiki Ishtar
1: Hank Gilgamesh
3: Betty Rocker
5: Wolfgang Kibble
4: Ian Flagranti
7: Joy Almondo
9: Juan Moore
8: Xäverie Paprika
6: Portia Koop
10: Misha Mache
Bye
```

```txt
Please enter stack size: 5
3: Betty Rocker _
5: Wolfgang Kibble
6: Portia Koop
4: Ian Flagranti _
8: Xaverie Paprika
9: Juan Moore
10: Misha Mache
7: Joy Almondo
2: Kiki-Ishtar
1: Hank Gilgamesh
Bye
```

## 程序说明

在程序清单 14.16 中，字符串本身永远不会移动。把字符串压入栈实际上是新建一个指向该字符串的指针，即创建一个指针，该指针的值是现有字符串的地址。从栈弹出字符串将把地址值复制到 out 数组中。

该程序使用的类型是 const char \*，因为指针数组将被初始化为一组字符串常量。

栈的析构函数对字符串有何影响呢？没有。构造函数使用 new 创建一个用于保存指针的数组，析构函数删除该数组，而不是数组元素指向的字符串。

## 14.4.4 数组模板示例和非类型参数

模板常用作容器类，这是因为类型参数的概念非常适合于将相同的存储方案用于不同的类型。确实，为容器类提供可重用代码是引入模板的主要动机，所以我们来看看另一个例子，深入探讨模板设计和使用的其他几个方面。具体地说，将探讨一些非类型（或表达式）参数以及如何使用数组来处理继承族。

首先介绍一个允许指定数组大小的简单数组模板。一种方法是在类中使用动态数组和构造函数参数来提供元素数目，最后一个版本的 Stack 模板采用的就是这种方法。另一种方法是使用模板参数来提供常规数组的大小，€++11 新增的模板 array 就是这样做的。程序清单 14.17 演示了如何做。

程序清单 14.17 arraytp.h

```cpp
//arraytp.h -- Array Template
#ifndef ARRAYTP_H_
#define ARRAYTP_H_

#include <iostream>
#include <cstdlib>

template <class T, int n>
class ArrayTP
{
private:
    T ar[n];
public:
    ArrayTP() {};
    explicit ArrayTP(const T & v);
    virtual T & operator[](int i);
    virtual T operator[](int i) const;
};

template <class T, int n>
ArrayTP<T,n>::ArrayTP(const T & v)
{
    for (int i = 0; i < n; i++)
        ar[i] = v;
}
template <class T, int n>
T & ArrayTP<T,n>::operator[](int i)
{
    if (i < 0 || i >= n)
    {
        std::cerr << "Error in array limits: " << i
            << " is out of range\n";
        std::exit(EXIT_FAILURE);
    }
    return ar[i];
```

```cpp
}
template <class T, int n>
T ArrayTP<T,n>::operator[](int i) const
{
    if (i < 0 || i >= n)
    {
        std::cerr << "Error in array limits: " << i
            << " is out of range\n";
        std::exit(EXIT_FAILURE);
    }
    return ar[i];
}

#endif
```

请注意程序清单 14.17 中的模板头:

```txt
template <class T, int n>
```

关键字 class（或在这种上下文中等价的关键字 typename）指出 T 为类型参数，int 指出 n 的类型为 int。这种参数（指定特殊的类型而不是用作泛型名）称为非类型（non-type）或表达式（expression）参数。假设有下面的声明:

```txt
ArrayTP<double, 12> eggweights;
```

这将导致编译器定义名为 ArrayTP&lt;double, 12&gt;的类，并创建一个类型为 ArrayTP&lt;double, 12&gt;的 cggweight 对象。定义类时，编译器将使用 double 替换 T，使用 12 替换 n。

表达式参数有一些限制。表达式参数可以是整型、枚举、引用或指针。因此，double m 是不合法的，但 double \* rm 和 double \* pm 是合法的。另外，模板代码不能修改参数的值，也不能使用参数的地址。所以，在 ArrayTP 模板中不能使用诸如 n++ 和 &n 等表达式。另外，实例化模板时，用作表达式参数的值必须是常量表达式。

与 Stack 中使用的构造函数方法相比，这种改变数组大小的方法有一个优点。构造函数方法使用的是通过 new 和 delete 管理的堆内存，而表达式参数方法使用的是为自动变量维护的内存栈。这样，执行速度将更快，尤其是在使用了很多小型数组时。

表达式参数方法的主要缺点是，每种数组大小都将生成自己的模板。也就是说，下面的声明将生成两个独立的类声明:

```txt
ArrayTP<double, 12> eggweights;
ArrayTP<double, 13> donuts;
```

但下面的声明只生成一个类声明，并将数组大小信息传递给类的构造函数:

```typescript
Stack<int> eggs(12);
Stack<int> dunkers(13);
```

另一个区别是，构造函数方法更通用，这是因为数组大小是作为类成员（而不是硬编码）存储在定义中的。这样可以将一种尺寸的数组赋给另一种尺寸的数组，也可以创建允许数组大小可变的类。

## 14.4.5 模板多功能性

可以将用于常规类的技术用于模板类。模板类可用作基类，也可用作组件类，还可用作其他模板的类型参数。例如，可以使用数组模板实现栈模板，也可以使用数组模板来构造数组——数组元素是基于栈模板的栈。即可以编写下面的代码:

```txt
template <typename T>   // or <class T>
class Array
{
```

```cpp
private:
    T entry;
    ...
};

template <typename Type>
class GrowArray : public Array<Type> {...};  // inheritance

template <typename Tp>
class Stack
{
    Array<Tp> ar;      // use an Array<> as a component
    ...
};
...
Array < Stack<int> > asi;  // an array of stacks of int
```

在最后一条语句中，C++98 要求使用至少一个空白字符将两个>符号分开，以免与运算符>>混淆。C++11 不要求这样做。

## 1. 递归使用模板

另一个模板多功能性的例子是，可以递归使用模板。例如，对于前面的数组模板定义，可以这样使用它:

```txt
ArrayTP< ArrayTP<int,5>, 10> twodee;
```

这使得 twodee 是一个包含 10 个元素的数组，其中每个元素都是一个包含 5 个 int 元素的数组。与之等价的常规数组声明如下:

```javascript
int twodee[10][5];
```

请注意，在模板语法中，维的顺序与等价的二维数组相反。程序清单 14.18 使用了这种方法，同时使用 ArrayTP 模板创建了一维数组，来分别保存这 10 个组（每组包含 5 个数）的总数和平均值。方法调用 cout.width(2) 以两个字符的宽度显示下一个条目（如果整个数字的宽度不超过两个字符）。

程序清单 14.18 twod.cpp

```cpp
// twod.cpp -- making a 2-d array
#include <iostream>
#include "arraytp.h"
int main(void)
{
    using std::cout;
    using std::endl;
    ArrayTP<int, 10> sums;
    ArrayTP<double, 10> aves;
    ArrayTP< ArrayTP<int,5>, 10> twodee;

    int i, j;

    for (i = 0; i < 10; i++)
    {
        sums[i] = 0;
        for (j = 0; j_< 5;- j++)
        {
            twodee[i][j] = (i + 1)- * (j + 1);
```

```txt
sums[i] += twodee[f][j];
}
aves[i] = (double) sums[i] / 10;
}
for (i = 0; i < 10; i++)
{
    for (j = -0; j < 5; -j++)
    {
        cout.width(2);
        cout<< twodee[i][j] << " ';
    }
    cout << ": sum = "";
    cout.width(3);
    cout << sums[i] << ", average = " << aves[i] << endl;
}

cout << "Done.\n";

return 0;
}
```

下面是程序清单 14.18 所示程序的输出。在 twodee 的 10 个元素（每个元素又是一个包含 5 个元素的数组）中，每个元素对应于 1 行:列出了每个元素包含的值、这些值的总和以及平均值。

```txt
1 2 3 4 5 : sum = 15, average = 1.5
2 4 6 8 10- : sum= 30, average = 3
3 6 9 12 15- : sum = 45, average = 4.5-
4- 8 12 16 20 : sum= 60, average = 6
5-10 15 20 25- : sum = 75, average = 7.5
6-12 18 24-30- : sum= 90, average = 9
7 14 21-28 35- : sum= 105, average = 10.5
8-16 24 32 40- : sum= 120, average = 12
9-18 27 36 45 : sum = 135, average = 13.5
10 20 30 40 50 : sum = 150, average = 15
Done.
```

## 2. 使用多个类型参数

模板可以包含多个类型参数。例如，假设希望类可以保存两种值，则可以创建并使用 Pair 模板来保存两个不同的值（标准模板库提供了类似的模板，名为 pair）。程序清单 14.19 所示的小程序是一个这样的示例。其中，方法 first() const 和 second() const 报告存储的值，由于这两个方法返回 Pair 数据成员的引用，因此让您能够通过赋值重新设置存储的值。

程序清单 14.19 pairs.cpp

```cpp
// pairs.cpp -- defining and using a Pair template
#include <iostream>
#include <string>
template <class T1, class T2>
class Pair
{
private:
    T1 a;
    T2 b;
public:
    T1 & first();
    T2 & second();
```

```cpp
T1 first() const { -return a; }
T2 second() const { return b; }
Pair(const T1 & aval, const T2 & bval) : a(aval), b(bval) { }
Pair() {-}
};
template<class T1, class T2>
T1 & Pair<T1,T2>::first()
{
    return a;
}
template<class T1, class T2>
T2 & Pair<T1,T2>::second()
{
    return b;
}

int main(-)
{
    using std::cout;-
    using std::endl;
    using std::string;
    Pair<string, int> ratings[4] =
    {
        Pair<string, int>("The Purpled Duck", 5),
        Pair<string, int>("Jaquie's Frisco Al Fresco", 4),
        Pair<string, int>("Cafe Souffle", 5),
        Pair<string, int>("Bertie's Eats", 3)
    };

    int joints = sizeof(ratings) / sizeof (Pair<string, int>);
    cout << "Rating:\t Eatery\n";
    for (int i = 0; i < joints; i++)
        cout << ratings[i].second() << ":\t "
            << ratings[i].first() << endl;
    cout << "Oops! Revised rating:\n";
    ratings[3].first() = "Bertie's Fab Eats";
    ratings[3].second() = 6;
    cout << ratings[3].second() << ":\t "
        << ratings[3].first() << endl;
    return 0;
}
```

对于程序清单 14.19，需要注意的一点是，在 main() 中必须使用 Pair&lt;string, int&gt; 来调用构造函数，并将它作为 sizeof 的参数。这是因为类名是 Pair&lt;string, int&gt;，而不是 Pair。另外，Pair&lt;char *, double&gt; 是另一个完全不同的类的名称。

下面是程序清单 14.19 所示程序的输出:

```txt
Rating: Eatery
5: The Purpled Duck
4: Jaquie's Frisco Al Fresco
5: Cafe Souffle
3: Bertie's Eats
Oops! Revised rating:
6: Bertie's Fab Eats
```

## 3. 默认类型模板参数

类模板的另一项新特性是，可以为类型参数提供默认值:

```txt
template <class T1, class T2 = int> class Topo {...};
```

这样，如果省略 T2 的值，编译器将使用 int:

```txt
Topo<double, double> m1; // T1 is double, T2 is double
Topo<double> m2;          // T1 is double, T2 is int
```

第 16 章将讨论的标准模板库经常使用该特性，将默认类型设置为类。

虽然可以为类模板类型参数提供默认值，但不能为函数模板参数提供默认值。然而，可以为非类型参数提供默认值，这对于类模板和函数模板都是适用的。

## 14.4.6 模板的具体化

类模板与函数模板很相似，因为可以有隐式实例化、显式实例化和显式具体化，它们统称为具体化（specialization）。模板以泛型的方式描述类，而具体化是使用具体的类型生成类声明。

## 1. 隐式实例化

到目前为止，本章所有的模板示例使用的都是隐式实例化（implicit instantiation），即它们声明一个或多个对象，指出所需的类型，而编译器使用通用模板提供的处方生成具体的类定义:

```txt
ArrayTP<int, 100> stuff; // implicit instantiation
```

编译器在需要对象之前，不会生成类的隐式实例化:

```txt
ArrayTP<double, 30> * pt;      // a pointer, no object needed yet
pt = new ArrayTP<double, 30>; // now an object is needed
```

第二条语句导致编译器生成类定义，并根据该定义创建一个对象。

## 2. 显式实例化

当使用关键字 template 并指出所需类型来声明类时，编译器将生成类声明的显式实例化（explicit instantiation）。声明必须位于模板定义所在的名称空间中。例如，下面的声明将 ArrayTP&lt;string, 100&gt;声明为一个类:

```typescript
template class ArrayTP<string, 100>; // generate ArrayTP<string, 100> class
```

在这种情况下，虽然没有创建或提及类对象，编译器也将生成类声明（包括方法定义）。和隐式实例化一样，也将根据通用模板来生成具体化。

## 3. 显式具体化

显式具体化（explicit specialization）是特定类型（用于替换模板中的泛型）的定义。有时候，可能需要在为特殊类型实例化时，对模板进行修改，使其行为不同。在这种情况下，可以创建显式具体化。例如，假设已经为用于表示排序后数组的类（元素在加入时被排序）定义了一个模板:

```cpp
template <typename T>
class SortedArray
{
    ...// details omitted
};
```

另外，假设模板使用>运算符来对值进行比较。对于数字，这管用；如果 T 表示一种类，则只要定义了 T::operator>() 方法，这也管用；但如果 T 是由 const char \*表示的字符串，这将不管用。实际上，模板倒是可以正常工作，但字符串将按地址（按照字母顺序）排序。这要求类定义使用 strcmp()，而不是>来对值进行比较。在这种情况下，可以提供一个显式模板具体化，这将采用为具体类型定义的模板，而不是为泛型定义的模板。当具体化模板和通用模板都与实例化请求匹配时，编译器将使用具体化版本。

具体化类模板定义的格式如下:

```txt
template <> class Classname<specialized-type-name> { ... };
```

早期的编译器可能只能识别早期的格式，这种格式不包括前缀 template<>:

```typescript
class Classname<specialized-type-name> { ... };
```

要使用新的表示法提供一个专供 const char \*类型使用的 SortedArray 模板，可以使用类似于下面的代码:

```cpp
template <> class SortedArray<const char char *>
{
    ...// details omitted
};
```

其中的实现代码将使用 strcmp()（而不是>）来比较数组值。现在，当请求 const char \*类型的 SortedArray 模板时，编译器将使用上述专用的定义，而不是通用的模板定义:

```txt
SortedArray<int> scores;          // use general definition
SortedArray<const char *> dates;  // use specialized definition
```

## 4. 部分具体化

C++还允许部分具体化（partial specialization），即部分限制模板的通用性。例如，部分具体化可以给类型参数之一指定具体的类型:

```txt
// general template
    template <class T1, class T2> class Pair {...};
// specialization with T2 set to int
    template <class T1> class Pair<T1, int> {...};
```

关键字 template 后面的<>声明的是没有被具体化的类型参数。因此，上述第二个声明将 T2 具体化为 int，但 T1 保持不变。注意，如果指定所有的类型，则<>内将为空，这将导致显式具体化:

```txt
// specialization with T1 and T2 set to int
  template <> class Pair<int, int> {...};
```

如果有多个模板可供选择，编译器将使用具体化程度最高的模板。给定上述三个模板，情况如下:

```cpp
Pair<double, double> p1; // use general Pair template
Pair<double, int> p2;     // use Pair<T1, int> partial specialization
Pair<int, int> p3;       // use Pair<int, int> explicit specialization
```

也可以通过为指针提供特殊版本来部分具体化现有的模板:

```cpp
template<class T>          // general version
class Feeb { ... };
template<class T*>         // pointer partial specialization
class Feeb { ... };       // modified code
```

如果提供的类型不是指针，则编译器将使用通用版本；如果提供的是指针，则编译器将使用指针具体化版本:

```txt
Feeb<char> fb1;          // use general Feeb template, T is char
Feeb<char *> fb2;         // use Feeb T* specialization, T is char
```

如果没有进行部分具体化，则第二个声明将使用通用模板，将 T 转换为 char \*类型。如果进行了部分具体化，则第二个声明将使用具体化模板，将 T 转换为 char。

部分具体化特性使得能够设置各种限制。例如，可以这样做:

```dart
// general template
    template <class T1, class T2, class T3> class Trio{...};
// specialization with T3 set to T2
    template <class T1, class T2> class Trio<T1, T2, T2> {...};
// specialization with T3 and T2 set to T1*
    template <class T1> class Trio<T1, T1*, T1*> {...};
```

给定上述声明，编译器将作出如下选择:

```c
Trio<int, short, char *> t1; // use general template
Trio<int, short> t2; // use Trio<T1, T2, T2>
Trio<char, char *, char *> t3; use Trio<T1, T1*, T1*>
```

## 14.4.7 成员模板

模板可用作结构、类或模板类的成员。要完全实现STL的设计，必须使用这项特性。程序清单14.20是一个简短的模板类示例，该模板类将另一个模板类和模板函数作为其成员。

程序清单 14.20 tempmemb.cpp

```cpp
// tempmemb.cpp -- template members
#include <iostream>
using std::cout;
using std::endl;
template <typename T>
class beta
{
private:
    template <typename V>  // nested template class member
    class hold
    {
    private:
        V val;
    public:
        hold(V v = 0) : val(v) {}
        void show() const { cout << val << endl; }
        V Value() const { return val; }
    };
    hold<T> q;            // template object
    hold<int> n;          // template object
public:
    beta( T t, int i) : q(t), n(i) {}
    template<typename U>   // template method
    U blab(U u, T t) { return (n.Value() + q.Value()) * u / t; }
    void Show() const { q.show(); n.show();}
};

int main()
{
    beta<double> guy(3.5, 3);
    cout << "T was set to double\n";
    guy.Show();
    cout << "V was set to T, which is double, then V was set to int\n";
    cout << guy.blab(10, 2.3) << endl;
    cout << "U was set to int\n";
    cout << guy.blab(10.0, 2.3) << endl;
    cout << "U was set to double\n";
    cout << "Done\n";
    return 0;
}
```

在程序清单 14.20 中，hold 模板是在私有部分声明的，因此只能在 beta 类中访问它。beta 类使用 hold 模板声明了两个数据成员:

```txt
hold<T> q;          // template object
hold<int> n;         // template object
```

n 是基于 int 类型的 hold 对象，而 q 成员是基于 T 类型（beta 模板参数）的 hold 对象。在 main() 中，下述声明使得 T 表示的是 double，因此 q 的类型为 hold&lt;double&gt;:

```txt
beta<double> guy(3.5, 3);
```

blab()方法的 U 类型由该方法被调用时的参数值显式确定，T 类型由对象的实例化类型确定。在这个例子中，guy 的声明将 T 的类型设置为 double，而下述方法调用的第一个参数将 U 的类型设置为 int（参数 10 对应的类型）:

```javascript
cout << guy.blab(10, 2.5) << endl;
```

因此，虽然混合类型引起的自动类型转换导致 blab() 中的计算以 double 类型进行，但返回值的类型为 U（即 int），因此它被截断为 28，如下面的程序输出所示:

```csv
T was set to double
3.5
3
V was set to T, which is double, then V was set to int
28
U was set to int
28.2609
U was set to double
Done
```

注意到调用 guy.blab()时，使用 10.0 代替了 10，因此 U 被设置为 double，这使得返回类型为 double，因此输出为 28.2608。

正如前面指出的，guy 对象的声明将第二个参数的类型设置为 double。与第一个参数不同的是，第二个参数的类型不是由函数调用设置的。例如，下面的语句仍将 blah() 实现为 blah(int, double)，并根据常规函数原型规则将 3 转换为类型 double:

```javascript
cout << guy.blab(10, 3) << endl;
```

可以在 beta 模板中声明 hold 类和 blah 方法，并在 beta 模板的外面定义它们。然而，很老的编译器根本不接受模板成员，而另一些编译器接受模板成员（如程序清单 14.20 所示），但不接受类外面的定义。然而，如果所用的编译器接受类外面的定义，则在 beta 模板之外定义模板方法的代码如下:

```cpp
template <typename T>
class beta
{
private:
    template <typename V>  // declaration
    class hold;
    hold<T> q;
    hold<int> n;
public:
    beta( T t, int i) : q(t), n(i) {}
    template<typename U>   // declaration
    U blab(U u, T t);
    void Show() const { q.show(); n.show();}
};

// member definition
template <typename T>
    template<typename V>
        class beta<T>::hold
        {
```

```cpp
{
        private:
            V val;
        public:
            hold{V v = 0} : val{v} {}
            void show{} const { std::cout << val << std::endl; }
            V Value() const { return val; }
        }
// member definition
template <typename T>
template <typename U>
U beta<T>::blab(U u, T t)
    {
        return (n.Value() + q.Value()){ * u / -t;
    }
```

上述定义将T、V和U用作模板参数。因为模板是嵌套的，因此必须使用下面的语法:

```txt
template <typename T>
  template <typename V>
```

而不能使用下面的语法:

```txt
template<typename T, typename V>
```

定义还必须指出 hold 和 blab 是 beta&lt;T&gt;类的成员，这是通过使用作用域解析运算符来完成的。

## 14.4.8 将模板用作参数

您知道，模板可以包含类型参数（如-typename T）和非类型参数（如 int n）。模板还可以包含本身就是模板的参数，这种参数是模板新增的特性，用于实现 STL。

在程序清单14.21所示的示例中，开头的代码如下:

```txt
template <template <typename T> class Thing>
class Crab
```

模板参数是 template &lt;typename T&gt; class Thing，其中 template &lt;typename T&gt; class 是类型，Thing 是参数。这意味着什么呢？假设有下面的声明:

```txt
Crab<King> legs;
```

为使上述声明被接受，模板参数 King 必须是一个模板类，其声明与模板参数 Thing 的声明匹配:

```txt
template <typename.T>
class King{...};
```

在程序清单14.21中，Crab的声明声明了两个对象:

```txt
Thing<int> s1;
Thing<double> s2;
```

前面的 legs 声明将用 King&lt;int&gt;替换 Thing&lt;int&gt;，用 King&lt;double&gt;替换 Thing&lt;double&gt;。然而，程序清单 14.2T 包含下面的声明:

```txt
Crab<Stack>= nebula;
```

因此，Thing&lt;int&gt;将被实例化为 Stack&lt;int&gt;，而 Thing&lt;double&gt;将被实例化为 Stack&lt;double&gt;。总之，模板参数 Thing 将被替换为声明 Crab 对象时被用作模板参数的模板类型。

Crab 类的声明对 Thing 代表的模板类做了另外 3 个假设，即这个类包含一个 push() 方法，包含一个 pop() 方法，且这些方法有特定的接口。Crab 类可以使用任何与 Thing 类型声明匹配，并包含方法 push() 和 pop() 的模板类。本章恰巧有一个这样的类——stacktp.h 中定义的 Stack 模板，因此这个例子将使用它。

程序清单 14.21 tempparm.cpp

```cpp
// tempparm.cpp - templates as parameters
#include <iostream>
#include "stacktp.h"

template <template <typename T> class Thing>
class Crab
{
private:
    Thing<int>-s1;
    Thing<double> s2;
public:
    Crab() {};
    // assumes the thing class has push() and pop()-members
    bool push(int a, double x) { return s1.push(a) && s2.push(x); }
    bool pop(int & a, double & x){ return s1.pop(a) && s2.pop(x); }
};

int main()
{
    using std::cout;
    using std::cin;
    using std::endl;
    Crab<Stack> nebula;
// Stack must match template <-typename T> class thing
    int -ni;
    double nb;
    cout << "Enter_int double pairs, such as 4 3.5 (0 0-to end):\n";
    while (cin>> ni >> nb && ni > 0 && nb > 0)
    {
        if (!nebula.push(ni, nb))
            break;
    }

    while (nebula.pop(ni, nb))
        cout << ni << ", " << nb=<< endl;
    cout << "Done.\n";

    return 0;
}
```

下面是程序清单 14.21 所示程序的运行情况:

```txt
Enter int double pairs, such as 4 3.5 (0-0 to end):
50 22.48
25 33.87
60 19.12
0-0
60, 19.12
25, 33.87
50, 22.48
Done.
```

可以混合使用模板参数和常规参数，例如，Crab类的声明可以像下面这样打头:

```txt
template <template <typename T> class Thing, typename U, typename V>
class Crab
```

```txt
{
private:
    Thing<U> s1;
    Thing<V> s2;
```

现在，成员 s1 和 s2 可存储的数据类型为泛型，而不是用硬编码指定的类型。这要求将程序中 nebula 的声明修改成下面这样:

Crab&lt;Stack, int, double&gt;-nebula; // T=Stack, U=int, V=double

模板参数 T 表示一种模板类型，而类型参数 U 和 V 表示非模板类型。

## 14.4.9 模板类和友元

模板类声明也可以有友元。模板的友元分3类:

- 非模板友元；
- 约束（bound）模板友元，即友元的类型取决于类被实例化时的类型；
- 非约束（unbound）模板友元，即友元的所有具体化都是类的每一个具体化的友元。

下面分别介绍它们。

## 1. 模板类的非模板友元函数

在模板类中将一个常规函数声明为友元:

```cpp
template <class T>
class HasFriend
{
public
    friend void counts();      // friend to all HasFriend instantiations
};
```

上述声明使 counts() 函数成为模板所有实例化的友元。例如，它将是类 hasFriend&lt;int&gt; 和 HasFriend&lt;string&gt; 的友元。

counts()函数不是通过对象调用的（它是友元，不是成员函数）；也没有对象参数，那么它如何访问HasFriend对象呢？有很多种可能性。它可以访问全局对象；可以使用全局指针访问非全局对象；可以创建自己的对象；可以访问独立于对象的模板类的静态数据成员。

假设要为友元函数提供模板类参数，可以如下所示来进行友元声明吗？

```txt
friend void report (HasFriend &); // possible?
```

答案是不可以。原因是不存在 HasFriend 这样的对象，而只有特定的具体化，如 HasFriend&lt;short&gt;。要提供模板类参数，必须指明具体化。例如，可以这样做:

```cpp
template <class T>
class HasFriend
{
    friend void report(HasFriend<T>&); // bound template friend
};
```

为理解上述代码的功能，想想声明一个特定类型的对象时，将生成的具体化:

```txt
HasFriend<int>hf;
```

编译器将用 int 替代模板参数 T，因此友元声明的格式如下:

```txt
class HasFriend<int>
{
    friend void report(HasFriend<int>&); // bound template friend
    ...
};
```

也就是说，带 HasFriend&lt;int&gt;参数的 report() 将成为 HasFriend&lt;int&gt;类的友元。同样，带 HasFriend&lt;double&gt;参数的 report() 将是 report() 的一个重载版本——它是 Hasfriend&lt;double&gt;类的友元。

注意，report()本身并不是模板函数，而只是使用一个模板作参数。这意味着必须为要使用的友元定义显式具体化:

```txt
void report(HasFriend<short> &) {-...}; // explicit specialization for short
void report(HasFriend<int> &) {...};   // explicit specialization for int
```

程序清单14.22说明了上面几点。HasFriend模板有一个静态成员ct。这意味着这个类的每一个特定的具体化都将有自己的静态成员。count()方法是所有HasFriend具体化的友元，它报告两个特定的具体化（HasFriend&lt;int&gt;和HasFriend&lt;double&gt;）的ct的值。该程序还提供两个report()函数，它们分别是某个特定HasFriend具体化的友元。

程序清单 14.22 frnd2tmp.cpp

```cpp
// frnd2tmp.cpp -- template class with non-template friends
#include <iostream>
using std::cout;
using std::endl;

template <typename T>
class HasFriend
{
private:
    T item;
    static int_ct;
public:
        HasFriend(const T & i) : item(i) {ct++;
        ~HasFriend() {ct--; }
        friend void counts();
        friend void reports(HasFriend<T> &); // template parameter
};

//-each specialization has its own static data member
template <typename T>
int HasFriend<T>::ct = 0;

// non-template friend to all HasFriend<T> classes
void counts()
{
    cout << "int count: " << HasFriend<int>::ct << "; ";
    cout << "double_count: "<< HasFriend<double>::ct << endl;
}

// non-template friend to the HasFriend<int> class
void reports(HasFriend<int> & hf)
{
    cout <<"HasFriend<int>: " << hf_item << endl;
}

// non-template friend to the HasFriend<double> class
void reports(HasFriend<double> & hf)
{
    cout <<"HasFriend<double>: "<< hf.item << endl;
}

int main()
```

```typescript
{
    cout << "No objects declared: ";
    counts();
    HasFriend<int> hfi1(10);
    cout << "After hfi1 declared: ";
    counts();
    HasFriend<int> hfi2(20);
    cout << "After hfi2 declared: ";
    counts();
    HasFriend<double> hfdb(10.5);
    cout << "After hfdb declared: ";
    counts();
    reports(hfi1);
    reports(hfi2);
    reports(hfdb);

    return 0;
}
```

有些编译器将对您使用非模板友元发出警告。下面是程序清单 14.22 所示程序的输出:

```txt
No objects declared: int count: 0; double count: 0-
After hfi1 declared: int count: 1; double count: 0-
After hfi2 declared: int count: 2; double count: 0=
After hfdb decFared: int count: 2; double count: 1
HasFriend<int>: 10
HasFriend<int>: 20
HasFriend<double>: 10.5
```

## 2. 模板类的约束模板友元函数

可以修改前一个示例，使友元函数本身成为模板。具体地说，为约束模板友元作准备，要使类的每一个具体化都获得与友元匹配的具体化。这比非模板友元复杂些，包含以下3步。

首先，在类定义的前面声明每个模板函数。

```txt
template <typename T> void counts();
template <typename T> void report(T &);
```

然后，在函数中再次将模板声明为友元。这些语句根据类模板参数的类型声明具体化:

```cpp
template <typename TT>
class HasFriendT
{
    friend void counts<TT>();
    friend void report<>(HasFriendT<TT> &);
};
```

声明中的◇指出这是模板具体化。对于 report()，◇可以为空，因为可以从函数参数推断出如下模板类型参数:

```txt
HasFriendT<TT>
```

然而，也可以使用:

```typescript
report<HasFriendT<TT> >(HasFriendT<TT>&)
```

但 counts() 函数没有参数，因此必须使用模板参数语法（&lt;TT&gt;）来指明其具体化。还需要注意的是，TT 是 HasFriendT 类的参数类型。

同样，理解这些声明的最佳方式也是设想声明一个特定具体化的对象时，它们将变成什么样。例如，假设声明了这样一个对象:

```typescript
HasFriendT<int> squack;
```