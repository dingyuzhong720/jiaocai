```cpp
<< "Transaction is aborted.\n";
}
else
{
    shares += num;
    share_val = price;
    set_tot();
}
}
void Stock::sell(long num, double price)
{
    using std::cout;
    if (num < 0)
    {
        cout << "Number of shares sold can't be negative. "
            << "Transaction is aborted.\n";
    }
    else if (num > shares)
    {
        cout << "You can't sell more than-you have! "
            << "Transaction is aborted.\n";
    }
    else
    {
        shares -= num;
        share_val = price;
        set_tot();
    }
}
void Stock::update(double price)
{
    share_val = price;
    set_tot();
}
void Stock::show() const
{
    using std::cout;
    using std::ios_base;
    // set_format to.#.###
    ios_base::fmtflags orig =
        cout.setf(ios_base::fixed, ios_base::floatfield);
    std::streamsize_prec = cout.precision(3);

    cout << "Company: " << company
        <<" Shares: " << shares << '\n';
    cout << " Share Price: $" << share_val;
    // set_format_to#.###
    cout.precision(2);
    cout << " Total Worth: $" << total_val << '\n';
}
// restore original format
```

```cpp
// restore original format
    cout.setf(orig, ios_base::floatfield);
    cout.precision(prec);
}

const Stock & Stock::topval(const Stock & s) const
{
    if (s.total_val > total_val)
        return s;
    else
        return *this;
}
```

当然，我们想知道 this 指针是否有用。显然，应在一个包含对象数组的程序中使用这种新方法。因此接下来介绍对象数组这一主题。

## 10.5 对象数组

和 Stock 示例一样，用户通常要创建同一个类的多个对象。可以创建独立对象变量，就像本章前面的示例所做的，但创建对象数组将更合适。这似乎是在介绍一个未知领域，但实际上，声明对象数组的方法与声明标准类型数组相同:

```txt
Stock mystuff[4]; // creates an array of 4 Stock objects
```

前面讲过，当程序创建未被显式初始化的类对象时，总是调用默认构造函数。上述声明要求，这个类要么没有显式地定义任何构造函数（在这种情况下，将使用不执行任何操作的隐式默认构造函数），要么定义了一个显式默认构造函数（就像这个例子那样）。每个元素（mystuff[0]、mystuff[1]等）都是 Stock 对象，可以使用 Stock 方法:

```txt
mystuff[0].update();      // apply update() to 1st element
mystuff[3].show();        // apply show() to 4th element
const Stock * tops = mystuff[2].topval(mystuff[1]);
    // compare 3rd and 2nd elements and set tops
    // to point at the one with a higher total value
```

可以用构造函数来初始化数组元素。在这种情况下，必须为每个元素调用构造函数:

```txt
const int STKS = 4;
Stock stocks[STKS] = {
    Stock("NanoSmart", 12.5, 20),
    Stock("Boffo Objects", 200, 2.0),
    Stock("Monolithic Obelisks", 130, 3.25),
    Stock("Fleep Enterprises", 60, 6.5)
};
```

这里的代码使用标准格式对数组进行初始化:用括号括起的、以逗号分隔的值列表。其中，每次构造函数调用表示一个值。如果类包含多个构造函数，则可以对不同的元素使用不同的构造函数:

```txt
const int STKS = 10;
Stock stocks[STKS] = {
    Stock("NanoSmart", 12.5, 20),
    Stock(),
    Stock("Monolithic Obelisks", 130, 3.25),
};
```

上述代码使用 Stock(const string & co, long n, double pr) 初始化 stock[0] 和 stock[2], 使用构造函数 Stock()

初始化 stock[1]。由于该声明只初始化了数组的部分元素，因此余下的 7 个元素将使用默认构造函数进行初始化。

初始化对象数组的方案是，首先使用默认构造函数创建数组元素，然后花括号中的构造函数将创建临时对象，然后将临时对象的内容复制到相应的元素中。因此，要创建类对象数组，则这个类必须有默认构造函数。

程序清单 10.9 在一个小程序中使用了这些原理，该程序对 4 个数组元素进行初始化，显示它们的内容，并找出这些元素中总值最高的一个。由于 topval() 每次只检查两个对象，因此程序使用 for 循环来检查整个数组。另外，它使用 stock 指针来跟踪值最高的元素。该程序使用程序清单 10.7 中的头文件和程序清单 10.8 中的方法文件。

程序清单 10.9 usestock2.cpp

```cpp
// usestok2.cpp -- using the Stock class
// compile with stock20.cpp
#include <iostream>
#include "stock20.h"

const int STKS = 4;
int main()
{
// create an array of initialized objects
    Stock stocks[STKS] = {
        Stock("NanoSmart", 12, 20.0),
        Stock("Boffo Objects", 200, 2.0),
        Stock("Monolithic Obelisks", 130, 3.25),
        Stock("Fleep Enterprises", 60, 6.5)
    };

    std::cout << "Stock holdings:\n";
    int st;
    for (st = 0; st < STKS; st++)
        stocks[st].show();
// set pointer to first element
    const Stock * top = &stocks[0];
    for (st = 1; st < STKS; st++)
        top = &top->topval(stocks[st]);
// now top points to the most valuable holding
    std::cout << "\nMost valuable holding:\n";
    top->show();
    return 0;
}
```

下面是该程序的输出:

```txt
Stock holdings:
Company: NanoSmart Shares: 12
Share Price: $20.000 Total Worth: $240.00
Company: Boffo Objects Shares: 200
Share Price: $2.000 Total Worth: $400.00
Company: Monolithic Obelisks Shares: 130
Share Price: $3.250 Total Worth: $422.50
Company: Fleep Enterprises Shares: 60
Share Price: $6.500 Total Worth: $390.00

Most valuable holding:
Company: Monolithic Obelisks Shares: 130
Share Price: $3.250 Total Worth: $422.50
```

有关程序清单10.9，需要注意的一点是，大部分工作是在类设计中完成的。完成类设计后，编写程序的工作本身便相当简单。

顺便说一句，知道 this 指针就可以更深入了解 C++ 的工作方式。例如，最初的 UNIX 实现使用 C++ 前端 cfront 将 C++ 程序转换为 C 程序。处理方法的定义时，只需将下面这样的 C++ 方法定义:

```cpp
void Stock::show() const
{
    cout << "Company: " << company
        << "  Shares: " << shares << '\n'
        << "  Share Price: $" << share_val
        << "  Total Worth: $" << total_val << '\n';
```

转换为下面这样的 C-风格定义:

```txt
void show(const Stock * this)
{
    cout << "Company: " << this->company
        << " Shares: " << this->shares << '\n'
        << " Share Price: $" << this->share_val
        << " Total Worth: $" << this->total_val << '\n';
}
```

即将 Stock::限定符转换为函数参数（指向 Stock 的指针），然后用这个指针来访问类成员。

同样，该前端将下面的函数调用:

```txt
top.show();
```

转换为:

```javascript
show(&top);
```

这样，将调用对象的地址赋给了 this 指针（实际情况可能更复杂些）。

## 10.6 类作用域

第 9 章介绍了全局（文件）作用域和局部（代码块）作用域。可以在全局变量所属文件的任何地方使用它，而局部变量只能在其所属的代码块中使用。函数名称的作用域也可以是全局的，但不能是局部的。C++类引入了一种新的作用域:类作用域。

在类中定义的名称（如类数据成员名和类成员函数名）的作用域都为整个类，作用域为整个类的名称只在该类中是已知的，在类外是不可知的。因此，可以在不同类中使用相同的类成员名而不会引起冲突。例如，Stock 类的 shares 成员不同于 JobRide 类的 shares 成员。另外，类作用域意味着不能从外部直接访问类的成员，公有成员函数也是如此。也就是说，要调用公有成员函数，必须通过对象:

```javascript
Stock sleeper("Exclusive Ore", 100, 0.25); // create object
sleeper.show();      // use object to invoke a member function
show();          // invalid -- can't call method directly
```

同样，在定义成员函数时，必须使用作用域解析运算符:

```txt
void Stock::update(double price)
{
    ...
}
```

总之，在类声明或成员函数定义中，可以使用未修饰的成员名称（未限定的名称），就像 sell() 调用 set\_tot() 成员函数时那样。构造函数名称在被调用时，才能被识别，因为它的名称与类名相同。在其他情况下，使用类成员名时，必须根据上下文使用直接成员运算符（.）、间接成员运算符（->）或作用域解析运算符（::）。下面的代码片段演示了如何访问具有类作用域的标识符:

```cpp
class Ik
{
private:
    int fuss;      // fuss has class scope
public:
    Ik(int f = 9) {fuss = f; } // fuss is in scope
    void ViewIk() const;        // ViewIk has class scope
};

void Ik::ViewIk() const   //Ik:: places ViewIk into Ik scope
{
    cout << fuss << endl;   // fuss in scope within class methods
}
...
int main()
{
    Ik * pik = new Ik;
    Ik ee = Ik(8); // constructor in scope because has class name
    ee.ViewIk();   // class object brings ViewIk into scope
    pik->ViewIk(); // pointer-to-Ik brings ViewIk into scope
...
```

## 10.6.1 作用域为类的常量

有时候，使符号常量的作用域为类很有用。例如，类声明可能使用字面值30来指定数组的长度，由于该常量对于所有对象来说都是相同的，因此创建一个由所有对象共享的常量是个不错的主意。您可能以为这样做可行:

```txt
class Bakery
{
private:
    const int Months = 12;     // declare a constant? FAILS
    double costs[Months];
    ...
```

但这是行不通的，因为声明类只是描述了对象的形式，并没有创建对象。因此，在创建对象前，将没有用于存储值的空间（实际上，C++11 提供了成员初始化，但不适用于前述数组声明，第 12 章将介绍该主题）。然而，有两种方式可以实现这个目标，并且效果相同。

第一种方式是在类中声明一个枚举。在类声明中声明的枚举的作用域为整个类，因此可以用枚举为整型常量提供作用域为整个类的符号名称。也就是说，可以这样开始 Bakery 声明:

```txt
class Bakery
{
private:
    enum {Months = 12};
    double costs[Months];
    ...
```

注意，用这种方式声明枚举并不会创建类数据成员。也就是说，所有对象中都不包含枚举。另外，Months只是一个符号名称，在作用域为整个类的代码中遇到它时，编译器将用30来替换它。

由于这里使用枚举只是为了创建符号常量，并不打算创建枚举类型的变量，因此不需要提供枚举名。顺便说一句，在很多实现中，ios\_base 类在其公有部分中完成了类似的工作，诸如 ios\_base::fixed 等标识符就来自这里。其中，fixed 是 ios\_base 类中定义的典型的枚举量。

C++提供了另一种在类中定义常量的方式——使用关键字 static:

```txt
class Bakery
{
private:
    static-const int Months ==12;
    double costs[Months];
    ...
```

-- 这将创建一个名为 Months 的常量，该常量将与其他静态变量存储在一起，而不是存储在对象中。因此，只有一个 Months 常量，被所有 Bakery 对象共享。第 12 章将深入介绍静态类成员。在 C++98 中，只能使用这种技术声明值为整数或枚举的静态常量，而不能存储 double 常量。C++11 消除了这种限制。

## 10:6.2 作用域内枚举（C++11）

传统的枚举存在一些问题，其中之一是两个枚举定义中的枚举量可能发生冲突。假设有一个处理鸡蛋和T恤的项目，其中可能包含类似下面这样的代码:

```txt
enum egg {Small, Medium, Large, Jumbo};
enum t_shirt {Small=Medium, Large, Xlarge};
```

这将无法通过编译，因为 egg Small 和 t-shirt Small 位于相同的作用域内，它们将发生冲突。为避免这种问题，C++11 提供了一种新枚举，其枚举量的作用域为类。这种枚举的声明类似于下面这样:

```txt
enum class egg_{SmaFl, Medium, Large, Jumbo};
enum class_t_shirt {SmaFl, Medium, Large, Xlarge};
```

也可使用关键字 struct 代替 class。无论使用哪种方式，都需要使用枚举名来限定枚举量:

```txt
egg choice = egg::Large; // the Large-enumerator of the egg enum
t_shirt Floyd = t_shirt::Large; // the Large-enumerator of the t_shirt enum
```

枚举量的作用域为类后，不同枚举定义中的枚举量就不会发生名称冲突了，而您可继续编写处理鸡蛋和T恤的项目。

C++Fl 还提高了作用域内枚举的类型安全。在有些情况下，常规枚举将自动转换为整型，如将其赋给 int 变量或用于比较表达式时，但作用域内枚举不能隐式地转换为整型:

```cpp
enum egg_old {-Small, Medium, Large, Jumbo};          // unscoped-
enum_class-t_shirt {Small, Medium, large, Xlarge}; // scoped
egg_old one = Medium;                          // unscoped
t_shirt rolf = t_shirt::Large;                 // scoped
int king = one;        //-implicit type conversion for_unscoped
int-ring = rolf;       // not allowed, no implicit type conversion
if (king<-Jumbo)     // allowed
    std::cout << "Jumbo converted to int before comparison.\n";
if (king < t_shirt::Medium)   // not allowed
    std::cout << "Not allowed: < not defined for scoped enum.\n";
```

但在必要时，可进行显式类型转换:

```rust
int_Frodo = int(t_shirt::Small); // Frodo set to 0
```

枚举用某种底层整型类型表示，在 C++98 中，如何选择取决于实现，因此包含枚举的结构的长度可能随系统而异。对于作用域内枚举，C++11 消除了这种依赖性。默认情况下，C++11 作用域内枚举的底层类型为 int。另外，还提供了一种语法，可用于做出不同的选择:

```txt
// underlying type for pizza is short
enum class : short pizza {Small, Medium, Large, XLarge};
```

:short 将底层类型指定为 short。底层类型必须为整型。在 C++11 中，也可使用这种语法来指定常规枚举的底层类型，但如果没有指定，编译器选择的底层类型将随实现而异。

## 10.7 抽象数据类型

Stock 类非常具体。然而，程序员常常通过定义类来表示更通用的概念。例如，就实现计算机专家们所说的抽象数据类型（abstract data type，ADT）而言，使用类是一种非常好的方式。顾名思义，ADT 以通用的方式描述数据类型，而没有引入语言或实现细节。例如，通过使用栈，可以以这样的方式存储数据，即总是从堆顶添加或删除数据。例如，C++程序使用栈来管理自动变量。当新的自动变量被生成后，它们被添加到堆顶；消亡时，从栈中删除它们。

下面简要地介绍一下栈的特征。首先，栈存储了多个数据项（该特征使得栈成为一个容器——一种更为通用的抽象）；其次，栈由可对它执行的操作来描述。

- 可创建空栈。
- 可将数据项添加到堆顶（压入）。
- 可从栈顶删除数据项（弹出）。
- 可查看栈否填满。
- 可查看栈是否为空。

可以将上述描述转换为一个类声明，其中公有成员函数提供了表示栈操作的接口，而私有数据成员负责存储栈数据。类概念非常适合于 ADT 方法。

私有部分必须表明数据存储的方式。例如，可以使用常规数组、动态分配数组或更高级的数据结构（如链表）。然而，公有接口应隐藏数据表示，而以通用的术语来表达，如创建栈、压入等。程序清单10.10演示了一种方法，它假设系统实现了bool类型。如果您使用的系统没有实现，可以使用int、0和1代替bool、false和true。

程序清单 10.10 stack.h

```c
// stack.h -- class definition for the stack ADT
#ifndef STACK_H_
#define STACK_H_

typedef unsigned long Item;

class Stack
{
private:
    enum {MAX = 10};      // constant specific to class
    Item items[MAX];     // holds stack items
    int top;                 // index for top stack item
public:
    Stack();
    bool isempty() const;
    bool isfull() const;
    // push() returns false if stack already is full, true otherwise
    bool push(const Item & item);   // add item to stack
    // pop() returns false if stack already is empty, true otherwise
    bool pop(Item & item);          // pop top into item
};
#endif
```

在程序清单 10.10 所示的示例中，私有部分表明，栈是使用数组实现的；而公有部分隐藏了这一点。因此，可以使用动态数组来代替数组，而不会改变类的接口。这意味着修改栈的实现后，不需要重新编写使用栈的程序，而只需重新编译栈代码，并将其与已有的程序代码链接起来即可。

接口是冗余的，因为 pop() 和 push() 返回有关栈状态的信息（满或空），而不是 void 类型。在如何处理超出栈限制或者清空栈方面，这为程序员提供了两种选择。他可以在修改栈前使用 isempty() 和 isfull() 来查看，也可以使用 push() 和 pop() 的返回值来确定操作是否成功。

这个类不是根据特定的类型来定义栈，而是根据通用的 Item 类型来描述。在这个例子中，头文件使用 typedef 用 Item 代替 unsigned long。如果需要 double 栈或结构类型的栈，则只需修改 typedef 语句，而类声明和方法定义保持不变。类模板（参见第 14 章）提供了功能更强大的方法，来将存储的数据类型与类设计隔离开来。

接下来需要实现类方法，程序清单 10.11 提供了一种可行的实现。

程序清单 10.11 stack.cpp

```cpp
// stack.cpp -- Stack member functions
#include "stack.h"
Stack::Stack()    // create an empty stack
{
    top = 0;
}

bool Stack::isempty() const
{
    return top == 0;
}

bool Stack::isfull() const
{
    return top == MAX;
}

bool Stack::push(const Item & item)
{
    if (top < MAX)
    {
        items[top++] = item;
        return true;
    }
    else
        return false;
}

bool Stack::pop(Item & item)
{
    if (top > 0)
    {
        item = items[--top];
        return true;
    }
    else
        return false;
}
```

默认构造函数确保所有栈被创建时都为空。pop()和push()的代码确保栈顶被正确地处理。这种保证措施是OOP更可靠的原因之一。假设要创建一个独立数组来表示栈，创建一个独立变量来表示栈顶索引。则每次创建新栈时，都必须确保代码是正确的。没有私有数据提供的保护，则很可能由于无意修改了数据而导致程序出现非常严重的故障。

下面来测试该栈。程序清单 10.12 模拟了售货员的行为——使用栈的后进先出方式，从购物筐的最上面开始处理购物订单。

程序清单 10.12 stacker.cpp

```cpp
// stacker.cpp -- testing the Stack class
#include <iostream>
#include <cctype>  // or ctype.h
#include "stack.h"
int main()
{
    using namespace std;
    Stack st; // create an empty stack
    char ch;
    unsigned long po;
    cout << "Please enter A to add a purchase order,\n"
        << "P to process a PO, or Q to quit.\n";
    while (cin >> ch && toupper(ch) != 'Q')
    {
        while (cin.get() != '\n')
            continue;
        if (!isalpha(ch))
        {
            cout << '\a';
            continue;
        }
        switch(ch)
        {
            case 'A':
            case 'a': cout << "Enter a PO number to add: ";
                cin >> po;
                if (st.isfull())
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
            }
            break;
        }
        cout << "Please enter A to add a purchase order,\n"
            << "P to process a PO, or Q to quit.\n";
    }
    cout << "Bye\n";
    return 0;
}
```

程序清单 10.12 中的 while 循环删除输入行中剩余部分，就现在而言这并非是必不可少的，但它使程序的修改更方便（第 14 章将对这个程序进行修改）。下面是该程序的运行情况:

```txt
Please enter A to add a purchase order,
P to process a PO, or Q to quit.
A
Enter a PO number to add: 17885
Please enter A to add a purchase order,
P to process a PO, or Q to quit.
P
PO #17885 popped
Please enter A to add a purchase order,
P to process a PO, or Q to quit.
A
Enter a PO number to add: 17965
Please enter A to add a purchase order,
P to process a PO, or Q to quit.
A
Enter a PO number to add: 18002
Please enter A to add a purchase order,
P to process a PO, or Q to quit.
P
PO #18002 popped
Please enter A to add a purchase order,
P to process a PO, or Q to quit.
P
PO #17965 popped
Please enter A to add a purchase order,
P to process a PO, or Q to quit.
P
stack already empty
Please enter A to add a purchase order,
P to process a PO, or Q to quit.
Q
Bye
```

## 10.8 总结

面向对象编程强调的是程序如何表示数据。使用 OOP 方法解决编程问题的第一步是根据它与程序之间的接口来描述数据，从而指定如何使用数据。然后，设计一个类来实现该接口。一般来说，私有数据成员存储信息，公有成员函数（又称为方法）提供访问数据的唯一途径。类将数据和方法组合成一个单元，其私有性实现数据隐藏。

通常，将类声明分成两部分组成，这两部分通常保存在不同的文件中。类声明（包括由函数原型表示的方法）应放到头文件中。定义成员函数的源代码放在方法文件中。这样便将接口描述与实现细节分开了。从理论上说，只需知道公有接口就可以使用类。当然，可以查看实现方法（除非只提供了编译形式），但程序不应依赖于其实现细节，如知道某个值被存储为 int。只要程序和类只通过定义接口的方法进行通信，程序员就可以随意地对任何部分做独立的改进，而不必担心这样做会导致意外的不良影响。

类是用户定义的类型，对象是类的实例。这意味着对象是这种类型的变量，例如由 new 按类描述分配的内存。C++试图让用户定义的类型尽可能与标准类型类似，因此可以声明对象、指向对象的指针和对象数组。可以按值传递对象、将对象作为函数返回值、将一个对象赋给同类型的另一个对象。如果提供了构造函数，则在创建对象时，可以初始化对象。如果提供了析构函数方法，则在对象消亡后，程序将执行该函数。

每个对象都存储自己的数据，而共享类方法。如果 mr\_object 是对象名，try\_me() 是成员函数，则可以使用成员运算符句点调用成员函数:mr\_object.try\_me()。在 OOP 中，这种函数调用被称为将 try\_me 消息发送给 mr\_object 对象。在 try\_me() 方法中引用类数据成员时，将使用 mr\_object 对象相应的数据成员。同样，函数调用 i\_object.try\_me() 将访问 i\_object 对象的数据成员。

如果希望成员函数对多个对象进行操作，可以将额外的对象作为参数传递给它。如果方法需要显式地引用调用它的对象，则可以使用 this 指针。由于 this 指针被设置为调用对象的地址，因此 \*this 是该对象的别名。

类很适合用于描述 ADT。公有成员函数接口提供了 ADT 描述的服务，类的私有部分和类方法的代码提供了实现，这些实现对类的客户隐藏。

## 10.9 复习题

1. 什么是类？
2. 类如何实现抽象、封装和数据隐藏？
3. 对象和类之间的关系是什么？
4. 除了是函数之外，类函数成员与类数据成员之间的区别是什么？

5. 定义一个类来表示银行帐户。数据成员包括储户姓名、账号（使用字符串）和存款。成员函数执行如下操作:

创建一个对象并将其初始化；
- 显示储户姓名、账号和存款；
- 存入参数指定的存款；
取出参数指定的款项。

请提供类声明，而不用给出方法实现。（编程练习1将要求编写实现）

6. 类构造函数在何时被调用？类析构函数呢？

7. 给出复习题 5 中的银行账户类的构造函数的代码。

8. 什么是默认构造函数，拥有默认构造函数有何好处？

9. 修改 Stock 类的定义（stock20.h 中的版本），使之包含返回各个数据成员值的成员函数。注意:返回公司名的成员函数不应为修改数组提供便利，也就是说，不能简单地返回 string 引用。

10. this 和 \*this 是什么?

## 10.10 编程练习

1. 为复习题 5 描述的类提供方法定义，并编写一个小程序来演示所有的特性。
2. 下面是一个非常简单的类定义:

```cpp
class Person {
private:
    static const LIMIT = 25;
    string lname;      // Person's last name
    char fname[LIMIT];  // Person's first name
public:
    Person() {lname = ""; fname[0] = '\0'; } // #1
    Person(const string & ln, const_char * fn = "Heyyou");  // #2
// the following methods display lname and fname
    void Show() const;        // firstname lastname format
    void FormalShow() const; // lastname, firstname format
};
```

它使用了一个 string 对象和一个字符数组，让您能够比较它们的用法。请提供未定义的方法的代码，以完成这个类的实现。再编写一个使用这个类的程序，它使用了三种可能的构造函数调用（没有参数、一个参数和两个参数）以及两种显示方法。下面是一个使用这些构造函数和方法的例子:

```javascript
Person one;                     // use default constructor
Person two("Smythecraft");       // use #2 with_one_defaultargument
Person three("Dimwiddy", "Sam"); // use #2, no defaults
one.Show();
cout << endl;
one.FormalShow();
// etc. for two and three
```

3. 完成第9章的编程练习1，但要用正确的golf类声明替换那里的代码。用带合适参数的构造函数替换setgolf（golf &, const char \*, int），以提供初始值。保留setgolf()的交互版本，但要用构造函数来实现它（例如，setgolf()的代码应该获得数据，将数据传递给构造函数来创建一个临时对象，并将其赋给调用对象，即\*this)。

4. 完成第9章的编程练习4，但将Sales结构及相关的函数转换为一个类及其方法。用构造函数替换setSales（sales &，double[]，int）函数。用构造函数实现setSales（Sales &）方法的交互版本。将类保留在名称空间SALES中。

5. 考虑下面的结构声明:

```javascript
struct customer {
    char fullname[35];
    double payment;
};
```

编写一个程序，它从栈中添加和删除 customer 结构（栈用 Stack 类声明表示）。每次 customer 结构被删除时，其 payment 的值都被加入到总数中，并报告总数。注意:应该可以直接使用 Stack 类而不作修改；只需修改 typedef 声明，使 Item 的类型为 customer，而不是 unsigned long 即可。

6. 下面是一个类声明:

```cpp
class Move
{
private:
    double x;
    double y;
public:
    Move(double a = 0, double b = 0); // sets x, y to a, b
    showmove() const;          // shows current x, y values
    Move add(const Move & m) const;
// this function adds x of m to x of invoking object to get new x,
// adds y of m to y of invoking object to get new y, creates a new
// move object initialized to new x, y values and returns it
    reset(double a = 0, double b = 0); // resets x,y to a, b
};
```

请提供成员函数的定义和测试这个类的程序。

7. Betelgeusean plórg 有这些特征。

数据:

- plorg 的名称不超过 19 个字符；
- plorg 有满意指数（CI），这是一个整数。

操作:

- 新的 plorg 将有名称，其 CI 值为 50;
- plorg 的 CI 可以修改；

- plorg可以报告其名称和CI;
- plorg 的默认名称为“Plorga”。

请编写一个 Plorg 类声明（包括数据成员和成员函数原型）来表示 plorg，并编写成员函数的函数定义。然后编写一个小程序，以演示 Plorg 类的所有特性。

8. 可以将简单列表描述成下面这样:

- 可存储 0 或多个某种类型的列表；
⑧ 可创建空列表；
- 可在列表中添加数据项；
- 可确定列表是否为空；
- 可确定列表是否为满；
- 可访问列表中的每一个数据项，并对它执行某种操作。

可以看到，这个列表确实很简单，例如，它不允许插入或删除数据项。

请设计一个 List 类来表示这种抽象类型。您应提供头文件 list.h 和实现文件 list.cpp，前者包含类定义，后者包含类方法的实现。您还应创建一个简短的程序来使用这个类。

该列表的规范很简单，这主要旨在简化这个编程练习。可以选择使用数组或链表来实现该列表，但公有接口不应依赖于所做的选择。也就是说，公有接口不应有数组索引、节点指针等。应使用通用概念来表达创建列表、在列表中添加数据项等操作。对于访问数据项以及执行操作，通常应使用将函数指针作为参数的函数来处理:

```c
void visit(void (*pf)(Item &));
```

其中，pf 指向一个将 Item 引用作为参数的函数（不是成员函数），Item 是列表中数据项的类型。visit() 函数将该函数用于列表中的每个数据项。

## 第11章 使用类

## 本章内容包括:

运算符重载。
● 友元函数。
- 重载<<运算符，以便用于输出。
● 状态成员。
- 使用 rand()生成随机值。
● 类的自动转换和强制类型转换。
类转换函数。

C++类特性丰富、复杂、功能强大。在第9章，您通过学习定义和使用简单的类，已踏上了面向对象编程之旅。通过定义用于表示对象的数据的类型以及（通过成员函数）定义可对数据执行的操作，您知道了类是如何定义数据类型的。我们还学习了两个特殊的成员函数——构造函数和析构函数，其作用是管理类对象的创建和删除。本章将进一步探讨类的特征，重点是类设计技术，而不是通用原理。您可能发现，本章介绍的一些特性很容易，而另一些很微妙。要更好地理解这些新特性，应使用这些示例进行练习。如果函数使用常规参数而不是引用参数，将发生什么情况呢？如果忽略了析构函数，又将发生什么情况呢？不要害怕犯错误，因为在解决问题的过程中学到的知识，比生搬硬套而不犯错误时要多得多（然而，不要认为所有的错误就都会让人增长见识）。这样，您将更全面地了解C++是如何工作的以及它可以为我们做哪些工作。

本章首先介绍运算符重载，它允许将标准 C++ 运算符（如=和+）用于类对象。然后介绍友元，这种 C++ 机制使得非成员函数可以访问私有数据。最后介绍如何命令 C++ 对类执行自动类型转换。学习本章和第 12 章后，您将对类构造函数和类析构函数所起的作用有更深入的了解。另外，您还将知道开发和改进类设计时，需要执行的步骤。

学习 C++ 的难点之一是需要记住大量的东西，但在拥有丰富的实践经验之前，根本不可能全部记住这些东西。从这种意义上说，学习 C++ 就像学习功能复杂的字处理程序或电子制表程序一样。任何特性都不可怕，但多数人只掌握了那些经常使用的特性，如查找文本或设置为斜体等。您可能在那里曾经学过如何生成替换字符或者创建目录，除非经常使用它们，否则这些技能可能根本与日常工作无关。也许，学习本章知识的最好方法是，在我们自己开发的 C++ 程序中使用其中的新特性。对这些新特性有了充分的认识后，就可以添加其他 C++ 特性了。正如 C++ 创始人 Bjarne Stroustrup 在一次 C++ 专业程序员大会上所建议的:“轻松地使用这种语言。不要觉得必须使用所有的特性，不要在第一次学习时就试图使用所有的特性。”

## 11.1 运算符重载

下面介绍一种使对象操作更美观的技术。运算符重载是一种形式的 C++ 多态。第 8 章介绍了 C++ 是如何使用户能够定义多个名称相同但特征标（参数列表）不同的函数的。这被称为函数重载或函数多态，旨在让您能够用同名的函数来完成相同的基本操作，即使这种操作被用于不同的数据类型（想象一下，如果必须对不同的物体使用不同的动词，如抬起左脚（lift\_lft），拿起汤匙（lift\_sp），英语将会多么笨拙）。运算符重载将重载的概念扩展到运算符上，允许赋予C++运算符多种含义。实际上，很多C++（也包括C语言）运算符已经被重载。例如，将\*运算符用于地址，将得到存储在这个地址中的值；但将它用于两个数字时，得到的将是它们的乘积。C++根据操作数的数目和类型来决定采用哪种操作。

C++允许将运算符重载扩展到用户定义的类型，例如，允许使用+将两个对象相加。编译器将根据操作数的数目和类型决定使用哪种加法定义。重载运算符可使代码看起来更自然。例如，将两个数组相加是一种常见的运算。通常，需要使用下面这样的for循环来实现:

```javascript
for (int i = 0; i < 20; i++) evening[i] = sam[i] + janet[i]; // add element by element
```

但在 C++ 中，可以定义一个表示数组的类，并重载+运算符。于是便可以有这样的语句；evening = sam + janet; // add two array objects

这种简单的加法表示法隐藏了内部机理，并强调了实质，这是OOP的另一个目标。

要重载运算符，需使用被称为运算符函数的特殊函数形式。运算符函数的格式如下:operatorop(argument-list)

例如，operator +()重载+运算符，operator \*()重载\*运算符。op 必须是有效的 C++运算符，不能虚构一个新的符号。例如，不能有 operator@()这样的函数，因为 C++中没有@运算符。然而，operator [ ](-)函数将重载[ ]运算符，因为[ ]是数组索引运算符。例如，假设有一个 Salesperson 类，并为它定义了一个 operator +()成员函数，以重载+运算符，以便能够将两个 Saleperson 对象的销售额相加，则如果 district2、sid 和 sara 都是 Salesperson 类对象，便可以编写这样的等式:

```txt
district2 = sid + sara;
```

编译器发现，操作数是 Salesperson 类对象，因此使用相应的运算符函数替换上述运算符:

```txt
district2 = sid.operator+(sara);
```

然后该函数将隐式地使用 sid（因为它调用了方法），而显式地使用 sara 对象（因为它被作为参数传递），来计算总和，并返回这个值。当然最重要的是，可以使用简便的+运算符表示法，而不必使用笨拙的函数表示法。

虽然 C++ 对运算符重载做了一些限制，但了解重载的工作方式后，这些限制就很容易理解了。因此，下面首先通过一些示例对运算符重载进行阐述，然后再讨论这些限制。

## 11.2 计算时间:一个运算符重载示例

如果今天早上在Priggs的账户上花费了2小时35分钟，下午又花费了2小时40分钟，则总共花了多少时间呢？这个示例与加法概念很吻合，但要相加的单位（小时与分钟的混合）与内置类型不匹配。第7章通过定义一个travel\_time结构和将这种结构相加的sum()函数来处理类似的情况。现在将其推广，采用一个使用方法来处理加法的Time类。首先使用一个名为Sum()的常规方法，然后介绍如何将其转换为重载运算符。程序清单11.1列出了这个类的声明。

程序清单 11.1 mytime0.h

```txt
// mytime0.h -- Time class before operator overloading
#ifndef MYTIME0_H_
#define=MYTIME0_H_

class Time-
{
```

```cpp
private:
    int hours;
    int minutes;
public:
    Time();
    Time(int h, int m = 0);
    void AddMin(int m);
    void AddHr(int h);
    void Reset(int h = 0, int m = 0);
    Time Sum(const Time & t) const;
    void Show() const;
};
#endif
```

Time 类提供了用于调整和重新设置时间、显示时间、将两个时间相加的方法。程序清单 11.2 列出了方法定义。请注意，当总的分钟数超过 59 时，AddMin() 和 Sum() 方法是如何使用整数除法和求模运算符来调整 minutes 和 hours 值的。另外，由于这里只使用了 iostream 的 cout，且只使用了一次，因此使用 std::cout 比导入整个名称空间更经济。

程序清单 11.2 mytime0.cpp

```cpp
// mytime0.cpp -- implementing Time methods
#include <iostream>
#include "mytime0.h"

Time::Time()
{
    hours = minutes = 0;
}

Time::Time(int h, int m )
{
    hours = h;
    minutes = m;
}

void Time::AddMin(int m)
{
    minutes += m;
    hours += minutes / 60;
    minutes %= 60;
}

void Time::AddHr(int h)
{
    hours += h;
}

void Time::Reset(int h, int m)
{
    hours = h;
    minutes = m;
}

Time Time::Sum(const Time & t) const
{
```

```cpp
Time sum;
sum.minutes = minutes + t.minutes;
sum.hours = hours + t.hours + sum.minutes / 60;
sum.minutes %= 60;
return sum;
}
void Time::Show() const
{
    std::cout << hours << " hours," " << minutes << " minutes";
}
```

来看一下Sum()函数的代码。注意参数是引用，但返回类型却不是引用。将参数声明为引用的目的是为了提高效率。如果按值传递Time对象，代码的功能将相同，但传递引用，速度将更快，使用的内存将更少。

然而，返回值不能是引用。因为函数将创建一个新的 Time 对象（sum），来表示另外两个 Time 对象的和。返回对象（如代码所做的那样）将创建对象的副本，而调用函数可以使用它。然而，如果返回类型为 Time &，则引用的将是 sum 对象。但由于 sum 对象是局部变量，在函数结束时将被删除，因此引用将指向一个不存在的对象。使用返回类型 Time 意味着程序将在删除 sum 之前构造它的拷贝，调用函数将得到该拷贝。

警告:不要返回指向局部变量或临时对象的引用。函数执行完毕后，局部变量和临时对象将消失，引用将指向不存在的数据。

最后，程序清单 11.3 对 Time 类中计算时间总和的部分进行了测试。

程序清单 11.3 usetime0.cpp

```cpp
//usetime0.cpp -- using the first draft of the Time class
//compile usetime0.cpp and mytime0.cpp together
#include <iostream>
#include "mytime0.h"

int main()
{
    using std::cout;
    using std::endl;
    Time planning;
    Time coding(2, 40);
    Time fixing(5, 55);
    Time total;

    cout << "planning time = ";
    planning.Show();
    cout << endl;

    cout << "coding time = ";
    coding.Show();
    cout << endl;

    cout << "fixing time = ";
    fixing.Show();
    cout << endl;

    total = coding.Sum(fixing);
```

```txt
cout << "coding.Sum(fixing) = ";
    total.Show();
    cout << endl;

    return 0;
}
```

下面是程序清单 11.1、程序清单 11.2 和程序清单 11.3 组成的程序的输出:

```txt
planning time = 0 hours, 0 minutes
coding time = 2 hours, 40 minutes
fixing time = 5 hours, 55 minutes
coding.Sum(fixing) = 8 hours, 35 minutes
```

## 11.2.1 添加加法运算符

将 Time 类转换为重载的加法运算符很容易，只要将 Sum() 的名称改为 operator +( ) 即可。这样做是对的，只要把运算符（这里为 +）放到 operator 的后面，并将结果用作方法名即可。在这里，可以在标识符中使用字母、数字或下划线之外的其他字符。程序清单 11.4 和程序清单 11.5 反映了这些细微的修改。

程序清单 11.4 mytime1.h

```cpp
// mytime1.h -- Time class before operator overloading
#ifndef MYTIME1_H_
#define MYTIME1_H_

class Time
{
private:
    int hours;
    int minutes;
public:
    Time();
    Time(int h, int m = 0);
    void AddMin(int m);
    void AddHr(int h);
    void Reset(int h = 0, int m = 0);
    Time operator+(const Time & t) const;
    void Show() const;
};
#endif
```

程序清单 11.5 mytime1.cpp

```cpp
// mytime1.cpp -- implementing Time methods
#include <iostream>
#include "mytime1.h"

Time::Time{}
{
    hours = minutes = 0;
}
Time::Time(int h; int m)
{
    hours = h;
    minutes = m;
```

```cpp
void Time::AddMin(int m)
{
    minutes += m;
    hours += minutes / 60;
    minutes %= 60;
}

void Time::AddHr(int h)
{
    hours=+= h;
}

void Time::Reset(int h, int m)
{
    hours = h;
    minutes = m;
}

Time Time::operator+(const Time & t) const
{
    Time sum;
    sum.minutes = minutes + t.minutes;
    sum.hours = hours + t.hours + sum,Eminutes / 60;
    sum_minutes %= 60;
    return_sum;
}

void Time::Show() const
{
    std::cout << hours << "hours,"<< minutes<< "minutes";
}
```

和 Sum() 一样，$\overline{\text{operator}} + ()$ 也是由 Time 对象调用的，它将第二个 Time 对象作为参数，并返回一个 Time 对象。因此，可以像调用 Sum() 那样来调用 $\overline{\text{operator}} + ()$ 方法:

```javascript
total = coding.operator+(fixing); // function notation
```

但将该方法命令为 operator+() 后，也可以使用运算符表示法:

```txt
total = coding + fixing; // operator notation
```

这两种表示法都将调用 operator +() 方法。注意，在运算符表示法中，运算符左侧的对象（这里为 coding）是调用对象，运算符右边的对象（这里为 fixing）是作为参数被传递的对象。程序清单 11.6 说明了这一点。

程序清单 11.6 usetime1.cpp

```cpp
// usetime1.cpp -- using the second draft of the Time class
// compile usetime1.cpp and mytime1.cpp together
#include <iostream>
#include "mytime1.h"

int main()
= ____
using std::cout;
using std::endl;
Time planning;
```

```dart
Time coding(2, 40);
Time fixing(5, 55);
Time total;

cout << "planning time = ";
planning.Show();
cout << endl;

cout << "coding time = ";
coding.Show();
cout << endl;

cout << "fixing time = ";
fixing.Show();
cout << endl;

total = coding + fixing;
// operator notation
cout << "coding + fixing = ";
total.Show();
cout << endl;

Time morefixing(3, 28);
cout << "more fixing time = ";
morefixing.Show();
cout << endl;
total = morefixing.operator+(total);
// function notation
cout << "morefixing.operator+(total) = ";
total.Show();
cout << endl;

return 0;
}
```

下面是程序清单 11.4～程序清单 11.6 组成的程序的输出:

```txt
planning time = 0 hours, 0 minutes
coding time = 2 hours, 40 minutes
fixing time = 5 hours, 55 minutes
coding + fixing = 8 hours, 35 minutes
more fixing time = 3 hours, 28 minutes
norefixing.operator+(total) = 12 hours, 3 minutes
```

总之，operator +()函数的名称使得可以使用函数表示法或运算符表示法来调用它。编译器将根据操作数的类型来确定如何做:

```txt
int a, b, c;
Time A, B, C;
c = a + b;      // use int addition
C = A + B;       // use addition as defined for Time objects
```

可以将两个以上的对象相加吗？例如，如果 t1、t2、t3 和 t4 都是 Time 对象，可以这样做吗:

```txt
t4 = t1 + t2 + t3;                                // valid?
```

为回答这个问题，来看一些上述语句将被如何转换为函数调用。由于+是从左向右结合的运算符，因此上述语句首先被转换成下面这样:

```javascript
t4 = t1.operator+(t2 + t3);          // valid?
```

然后，函数参数本身被转换成一个函数调用，结果如下:

```javascript
t4 = -t1.operator+(t2.operator+(t3)-);   // valid? YES
```

上述语句合法吗？是的。函数调用 t2.operator+(t3) 返回一个 Time 对象，后者是 t2 和 t3 的和。然而，该对象成为函数调用 t1.operator+() 的参数，该调用返回 t1 与表示 t2 和 t3 之和的 Time 对象的和。总之，最后的返回值为 t1、t2 和 t3 之和，这正是我们期望的。

## 11.2.2 重载限制

多数 C++运算符（参见表 11.1）都可以用这样的方式重载。重载的运算符（有些例外情况）不必是成员函数，但必须至少有一个操作数是用户定义的类型。下面详细介绍 €++对用户定义的运算符重载的限制。

1. 重载后的运算符必须至少有一个操作数是用户定义的类型，这将防止用户为标准类型重载运算符。因此，不能将减法运算符（-）重载为计算两个 double 值的和，而不是它们的差。虽然这种限制将对创造性有所影响，但可以确保程序正常运行。
2. 使用运算符时不能违反运算符原来的句法规则。例如，不能将求模运算符（%）重载成使用一个操作数:

```matlab
int x;
Time shiva;
% x;      // invalid for modulus operator
% shiva;  // invalid for overloaded operator
```

同样，不能修改运算符的优先级。因此，如果将加号运算符重载成将两个类相加，则新的运算符与原来的加号具有相同的优先级。

3. 不能创建新运算符。例如，不能定义 operator \*\*()函数来表示求幂。
4. 不能重载下面的运算符。

- sizeof: sizeof 运算符。
- :成员运算符。
- .\*: 成员指针运算符。
- :: 作用域解析运算符。
- ?: 条件运算符。
- typeid: 一个 RTTI 运算符。
- const\_cast: 强制类型转换运算符。
- dynamic\_cast: 强制类型转换运算符。
- reinterpret\_cast: 强制类型转换运算符。
- static\_cast: 强制类型转换运算符。

然而，表 11.1 中所有的运算符都可以被重载。

5. 表 11.1 中的大多数运算符都可以通过成员或非成员函数进行重载，但下面的运算符只能通过成员函数进行重载。

$\bullet =$ :赋值运算符。
- ( ): 函数调用运算符。
- []: 下标运算符。

\- ->:通过指针访问类成员的运算符。

注意:本章不介绍这里列出的所有运算符，但附录E对本书正文中没有介绍的运算符进行了总结。

表 11.1 可重载的运算符

| + | - | * | / | % | ^ |
| --- | --- | --- | --- | --- | --- |
| &amp; | \| | ~= | ! | = | &lt; |
| > | += | -= | *= | /= | %= |
| ^= | &amp;= | \|= | &lt;&lt; | >> | >>= |
| &lt;&lt;= | = | \|= | &lt;= | >= | &amp;&amp; |
| \|\| | ++ | - | - | ->* | -> |
| .0 | []^- | new | delete | new [] | delete [] |

除了这些正式限制之外，还应在重载运算符时遵循一些明智的限制。例如，不要将\*运算符重载成交换两个 Time-对象的数据成员。表示法中没有任何内容可以表明运算符完成的工作，因此最好定义一个其名称具有说明性的类方法，如 Swap()。

## 11.2.3 其他重载运算符

还有一些其他的操作对 Time 类来说是有意义的。例如，可能要将两个时间相减或将时间乘以一个因子，这需要重载减法和乘法运算符。这和重载加法运算符采用的技术相同，即创建 operator -() 和 operator \*() 方法。也就是说，将下面的原型添加到类声明中:

```c
Time operator-(const Time & t) const;
Time operator*(double n) const;
```

程序清单11.7是新的头文件。

程序清单 11.7 mytime2.h

```c
// mytime2.h -- Time class after operator overloading _
#ifndef MYTIME2_H_
#define MYTIME2_H_

class Time
{
    private:
        int hours;
        int minutes;
public:
        Time();
        Time(int h, int m = 0);
        void AddMin(int m);
        void AddHr(int h);
        void Reset(int h = 0, int m = 0);
        Time operator+(const Time & t) const;
        Time operator-(const Time & t) const;
        Time operator*(double n) const;
        void Show() const;
};
#endif
```

然后将新增方法的定义添加到实现文件中，如程序清单 11.8 所示。

程序清单 11.8 mytime2.cpp

```cpp
// mytime2.cpp --- implementing Time methods
#include <iostream>
#include "mytime2.h"

Time::Time()
{
    hours = minutes = 0;
}
```

```cpp
Time::Time(int h, int m)
{
    hours = h;
    minutes = m;
}
void Time::AddMin(int m)
{
    minutes += m;
    hours += minutes / 60;
    minutes %= 60;
}
void Time::AddHr(int h)
{
    hours += h;
}

void Time::Reset(int h, int m)
{
    hours = h;
    minutes = m;
}

Time Time::operator+(const Time & t) const
{
    Time sum;
    sum.minutes = minutes+-t.minutes;
    sum.hours = hours + t.hours + sum.minutes / 60;
    sum.minutes %= 60;
    return sum;
}

Time Time::operator-(const Time & t) const
{
    Time diff;
    int tot1, tot2;
    tot1 = t.minutes + 60 * t.hours;
    tot2 = minutes + 60 * hours;
    diff.minutes = (tot2 - tot1) % 60;
    diff.hours = (tot2 - tot1) / 60;
    return diff;
}

Time Time::operator*(double mult) const
{
    Time result;
    long totalminutes = hours * mult * 60 + minutes * mult;
    result.hours = totalminutes / 60;
    result.minutes = totalminutes % 60;
    return result;
}

void Time::Show() const
{
    std::cout << hours << " hours, " << minutes << " minutes";
}
```

完成上述修改后，就可以使用程序清单 11.9 中的代码来测试新定义了。

程序清单 11.9 usetime2.cpp

```cpp
// usetime2.cpp -- using the third draft of the Time class
// compile usetime2.cpp and mytime2.cpp together
#include <iostream>
#include "mytime2.h"

int main(){
    using std::cout;
    using std::endl;
    Time weeding(4, 35);
    Time waxing(2, 47);
    Time total;
    Time diff;
    Time adjusted;

    cout << "weeding time = ";
    weeding.Show();
    cout << endl;

    cout << "waxing time = ";
    waxing.Show();
    cout << endl;

    cout << "total work time = -";
    total = weeding + waxing;   // use operator+()
    total.Show();
    cout << endl;

    diff = weeding - waxing;   // use operator-()
    cout << "weeding time - waxing time = -";
    diff.Show();
    cout << endl;

    adjusted = total * 1.5;      // use operator+()
    cout << "adjusted work time = -";
    adjusted.Show();
    cout << endl;
    return 0;
}
```

下面是程序清单11.7～程序清单11.9组成的程序得到的输出:

```txt
weeding time = 4 hours, 35 minutes
waxing time = 2 hours, 47 minutes
total work time = -7 hours, 22 minutes
weeding time -- waxing time = 1 hours, 48 minutes
adjusted work time = 11 hours, 3 minutes
```

## 11.3 友元

您知道，C++控制对类对象私有部分的访问。通常，公有类方法提供唯一的访问途径，但是有时候这种限制太严格，以致于不适合特定的编程问题。在这种情况下，C++提供了另外一种形式的访问权限:友元。友元有3种:

- 友元函数；
- 友元类;
- 友元成员函数。

通过让函数成为类的友元，可以赋予该函数与类的成员函数相同的访问权限。下面介绍友元函数，其他两种友元将在第15章介绍。

介绍如何成为友元前，先介绍为何需要友元。在为类重载二元运算符时（带两个参数的运算符）常常需要友元。将 Time 对象乘以实数就属于这种情况，下面来看看。

在前面的 Time 类示例中，重载的乘法运算符与其他两种重载运算符的差别在于，它使用了两种不同的类型。也就是说，加法和减法运算符都结合两个 Time 值，而乘法运算符将一个 Time 值与一个 double 值结合在一起。这限制了该运算符的使用方式。记住，左侧的操作数是调用对象。也就是说，下面的语句:

```javascript
A = B * 2.75;
```

将被转换为下面的成员函数调用:

```javascript
A = B.operator*(2.75);
```

但下面的语句又如何呢？

```javascript
A = 2.75 * B;      // cannot correspond to a member function
```

从概念上说，2.75 \* B 应与 B \* 2.75 相同，但第一个表达式不对应于成员函数，因为 2.75 不是 Time 类型的对象。记住，左侧的操作数应是调用对象，但 2.75 不是对象。因此，编译器不能使用成员函数调用来替换该表达式。

解决这个难题的一种方式是，告知每个人（包括程序员自己），只能按 B \* 2.75 这种格式编写，不能写成 2.75 \* B。这是一种对服务器友好-客户警惕的（server-friendly, client-beware）解决方案，与 OOP 无关。

然而，还有另一种解决方式——非成员函数（记住，大多数运算符都可以通过成员或非成员函数来重载）。非成员函数不是由对象调用的，它使用的所有值（包括对象）都是显式参数。这样，编译器能够将下面的表达式:

```javascript
A = 2.75 * B;      // cannot correspond to a member function
```

与下面的非成员函数调用匹配:

```javascript
A = operator*(2.75, B);
```

该函数的原型如下:

```txt
Time operator*(double m, const Time & t);
```

对于非成员重载运算符函数来说，运算符表达式左边的操作数对应于运算符函数的第一个参数，运算符表达式右边的操作数对应于运算符函数的第二个参数。而原来的成员函数则按相反的顺序处理操作数，也就是说，double 值乘以 Time 值。

使用非成员函数可以按所需的顺序获得操作数（先是 double，然后是 Time），但引发了一个新问题:非成员函数不能直接访问类的私有数据，至少常规非成员函数不能访问。然而，有一类特殊的非成员函数可以访问类的私有成员，它们被称为友元函数。

## 11.3.1 创建友元

创建友元函数的第一步是将其原型放在类声明中，并在原型声明前加上关键字 friend:

```txt
friend Time operator*(double m, const Time & t);  // goes in class declaration
```

该原型意味着下面两点:

- 虽然 operator \*()函数是在类声明中声明的, 但它不是成员函数, 因此不能使用成员运算符来调用;
- 虽然 operator \*()函数不是成员函数，但它与成员函数的访问权限相同。

第二步是编写函数定义。因为它不是成员函数，所以不要使用 Time::限定符。另外，不要在定义中使

用关键字 friend，定义应该如下:

```txt
Time operator*(double m, const Time & t)  // friend not used in definition
{
    Time result;
    long totalminutes = t.hours * mult * 60 +t. minutes * mult;
    result.hours = totalminutes / 60;
    result.minutes = totalminutes % 60;
    return result;
}
```

有了上述声明和定义后，下面的语句:

```javascript
A = 2.75 * B;
```

将转换为如下语句，从而调用刚才定义的非成员友元函数:

```javascript
A = operator*(2.75, B);
```

总之，类的友元函数是非成员函数，其访问权限与成员函数相同。

## 友元是否有悖于 OOP

乍一看,您可能会认为友元违反了 OOP 数据隐藏的原则,因为友元机制允许非成员函数访问私有数据。然而,这个观点太片面了。相反,应将友元函数看作类的扩展接口的组成部分。例如,从概念上看,double 乘以 Time 和 Time 乘以 double 是完全相同的。也就是说,前一个要求有友元函数,后一个使用成员函数,这是 C++ 句法的结果,而不是概念上的差别。通过使用友元函数和类方法,可以用同一个用户接口表达这两种操作。另外请记住,只有类声明可以决定哪一个函数是友元,因此类声明仍然控制了哪些函数可以访问私有数据。总之,类方法和友元只是表达类接口的两种不同机制。

实际上，按下面的方式对定义进行修改（交换乘法操作数的顺序），可以将这个友元函数编写为非友元函数:

```cpp
Time operator*(double m, const Time & t)
{
    return t * m;      // use t.operator*(m)
}
```

原来的版本显式地访问 t(minutes 和 t.hours，所以它必须是友元。这个版本将 Time 对象 t 作为一个整体使用，让成员函数来处理私有值，因此不必是友元。然而，将该版本作为友元也是一个好主意。最重要的是，它将该作为正式类接口的组成部分。其次，如果以后发现需要函数直接访问私有数据，则只要修改函数定义即可，而不必修改类原型。

提示:如果要为类重载运算符，并将非类的项作为其第一个操作数，则可以用友元函数来反转操作数的顺序。

## 11.3.2 常用的友元:重载<<运算符

一个很有用的类特性是，可以对<<运算符进行重载，使之能与cout一起来显示对象的内容。与前面介绍的示例相比，这种重载要复杂些，因此我们分两步（而不是一步）来完成。

假设 trip 是一个 Time 对象。为显示 Time 的值，前面使用的是 Show()。然而，如果可以像下面这样操作将更好:

```txt
cout << trip;  // make cout recognize Time class?
```

之所以可以这样做，是因为<<是可被重载的C++运算符之一。实际上，它已经被重载很多次了。最初，<<运算符是C和C++的位运算符，将值中的位左移（参见附录E）。ostream类对该运算符进行了重载，将其转换为一个输出工具。前面讲过，cout是一个ostream对象，它是智能的，能够识别所有的C++基本类型。这是因为对于每种基本类型，ostream类声明中都包含了相应的重载的operator<<()定义。也就是说，一个定义使用 int 参数，一个定义使用 double 参数，等等。因此，要使 cout 能够识别 Time 对象，一种方法是将一个新的函数运算符定义添加到 ostream 类声明中。但修改 iostream 文件是个危险的主意，这样做会在标准接口上浪费时间。相反，通过 Time 类声明来让 Time 类知道如何使用 cout。

## 1. <<的第一种重载版本

要使 Time 类知道使用 cout，必须使用友元函数。这是什么原因呢？因为下面这样的语句使用两个对象，其中第一个是 ostream 类对象（cout）:

```txt
cout << trip;
```

如果使用一个 Time 成员函数来重载<<，Time 对象将是第一个操作数，就像使用成员函数重载\*运算符那样。这意味着必须这样使用<<:

```txt
trip << cout;   // if operator<<() were a Time member function
```

这样会令人迷惑。但通过使用友元函数，可以像下面这样重载运算符:

```javascript
void operator<<(ostream & os, const Time & t)
{
    os << t.hours << " hours, " << t.minutes << " minutes";
}
```

这样可以使用下面的语句:

```txt
cout << trip;
```

按下面这样的格式打印数据:

```txt
4 hours, 23 minutes
```

## 友元还是非友元？

新的 Time 类声明使 operatro<<()函数成为 Time 类的一个友元函数。但该函数不是 ostream 类的友元(尽管对 ostream 类并无害处)。operator<<()函数接受一个 ostream 参数和一个 Time 参数，因此表面看来它必须同时是这两个类的友元。然而，看看函数代码就会发现，尽管该函数访问了 Time 对象的各个成员，但从始至终都将 ostream 对象作为一个整体使用。因为 operator<<()直接访问 Time 对象的私有成员，所以它必须是 Time 类的友元。但由于它并不直接访问 ostream 对象的私有成员，所以并不一定必须是 ostream 类的友元。这很好，因为这就意味着不必修订 ostream 的定义。

注意，新的 operator<<()定义使用 ostream 引用 os 作为它的第一个参数。通常情况下，os 引用 cout 对象，如表达式 cout << trip 所示。但也可以将这个运算符用于其他 ostream 对象，在这种情况下，os 将引用相应的对象。

## 不知道其他ostream对象？

另一个 ostream 对象是 cerr，它将输出发送到标准输出流——默认为显示器，但在 UNIX、Linux 和 Windows 命令行环境中，可将标准错误流重定向到文件。另外，第 6 章介绍的 ofstream 对象可用于将输出写入到文件中。通过继承(参见第 13 章)，ofstream 对象可以使用 ostream 的方法。这样，便可以用 operator<<() 定义来将 Time 的数据写入到文件和屏幕上，为此只需传递一个经过适当初始化的 ofstream 对象（而不是 cout 对象）。

调用cout << trip应使用cout对象本身，而不是它的拷贝，因此该函数按引用（而不是按值）来传递该对象。这样，表达式cout << trip将导致os成为cout的一个别名；而表达式cerr << trip将导致os成为cerr的一个别名。Time对象可以按值或按引用来传递，因为这两种形式都使函数能够使用对象的值。按引用传递使用的内存和时间都比按值传递少。

## 2. <<的第二种重载版本

前面介绍的实现存在一个问题。像下面这样的语句可以正常工作:

```txt
cout << trip;
```

但这种实现不允许像通常那样将重新定义的<<运算符与cout一起使用:

```txt
cout << "Trip time: " << trip << " (Tuesday)\n"; // can't do
```

要理解这样做不可行的原因以及必须如何做才能使其可行，首先需要了解关于 cout 操作的一点知识。请看下面的语句:

```txt
int x = 5;
int y = 8;
cout << x << y;
```

C++从左至右读取输出语句，意味着它等同于:

```txt
(cout << x) << y;
```

正如 iosream 中定义的那样，<<运算符要求左边是一个 ostream 对象。显然，因为 cout 是 ostream 对象，所以表达式 cout << x 满足这种要求。然而，因为表达式 cout << x 位于<< y 的左侧，所以输出语句也要求该表达式是一个 ostream 类型的对象。因此，ostream 类将 operator<<() 函数实现为返回一个指向 ostream 对象的引用。具体地说，它返回一个指向调用对象（这里是 cout）的引用。因此，表达式(cout << x)本身就是 ostream 对象 cout，从而可以位于<<运算符的左侧。

可以对友元函数采用相同的方法。只要修改 operator<<()函数，让它返回 ostream 对象的引用即可:

```javascript
ostream & operator<<(ostream & os, const Time & t)
{
    os << t.hours << " hours, " << t.minutes << " minutes";
    return os;
}
```

注意，返回类型是 ostream &。这意味着该函数返回 ostream 对象的引用。因为函数开始执行时，程序传递了一个对象引用给它，这样做的最终结果是，函数的返回值就是传递给它的对象。也就是说，下面的语句:

```txt
cout << trip;
```

将被转换为下面的调用:

```txt
operator<<(cout, trip);
```

而该调用返回 cout 对象。因此，下面的语句可以正常工作:

```txt
cout << "Trip time: " << trip << " (Tuesday)\n"; // can do
```

我们将这条语句分成多步，来看看它是如何工作的。首先，下面的代码调用 ostream 中的<<定义，它显示字符串并返回 cout 对象:

```txt
cout << "Trip time: "
```

因此表达式 cout << “Trip time:” 将显示字符串，然后被它的返回值 cout 所替代。原来的语句被简化为下面的形式:

```txt
cout << trip << " (Tuesday)\n";
```

接下来，程序使用<<的 Time 声明显示 trip 值，并再次返回 cout 对象。这将语句简化为:

```txt
cout << " (Tuesday)\n";
```

现在，程序使用 ostream 中用于字符串的<<定义，来显示最后一个字符串，并结束运行。

有趣的是，这个 operator<<()版本还可用于将输出写入到文件中:

```txt
#include <fstream>
...
ofstream fout;
fout.open("savetime.txt");
Time trip(12, 40);
fout << trip;
```

其中最后一条语句将被转换为这样:

```txt
operator<<(fout, trip);
```

另外，正如第8章指出的，类继承属性让ostream引用能够指向ostream对象和ofstream对象。

提示:一般来说，要重载<<运算符来显示c\_name的对象，可使用一个友元函数，其定义如下:

```cpp
ostream & operator<<(ostream-& os, const c_name & obj)=
{
    os-<< ... ;  // display object contents
    return os;
}
```

程序清单 11.10 列出了修改后的类定义，其中包括 operator\*( )和 operator<<()这两个友元函数。它将第一个友元函数作为内联函数，因为其代码很短。（当定义同时也是原型时，就像这个例子中那样，要使用 friend 前缀。）

警告:只有在类声明中的原型中才能使用 friend 关键字。除非函数定义也是原型，否则不能在函数定义中使用该关键字。

程序清单 11.10 mytime3.h

```cpp
// mytime3.h -- Time class with friends
#ifndef MYTIME3_H_
#define MYTIME3_H_
#include <iostream>

class Time
{
private:
    int hours;
    int minutes;
public:
    Time();
    Time(int h, int m = 0);
    void AddMin(int m);
    void AddHr(int h);
    void Reset(int h = 0, int m = 0);
    Time operator+(const Time & t) const;
    Time operator-(const Time & t) const;
    Time operator*(double n) const;
    friend Time-operator*(double m, const Time=& t)
        { return-t * m; }= // inline definition
    friend std::ostream & operator<<(std::ostream & os, const Time & t);
};

#endif
```

程序清单 11.11 列出了修改后的定义。方法使用了 Time::限定符，而友元函数不使用该限定符。另外，由于在 mytime3.h 中包含了 iostream 并提供了 using 声明 std::ostream，因此在 mytime3.cpp 中包含 mytime3.h 后，便提供了在实现文件中使用 ostream 的支持。

程序清单 11.11 mytime3.cpp

```cpp
// mytime3.cpp -- implementing Time methods
#include "mytime3.h"

Time::Time()
{
    hours = minutes== 0;
}

Time::Time(int h7 int m)
{
```

```cpp
hours = h;
minutes = m;
}

void Time::AddMin(int m)
{
    minutes += m;
    hours += minutes / 60;
    minutes %= 60;
}
void Time::AddHr(int h)
{
    hours += h;
}

void Time::Reset(int h, int m)
{
    hours = h;
    minutes== m;
}

Time Time::operator+(const_Time & t)-const
{
    Time sum;
    sum.minutes = minutes + t.minutes;
    sum.hours = hours + t.hours + sum.minutes / 60;
    sum.minutes *= 60;
    return sum;
}

Time Time::operator-(const_Time & t) const
{
    Time diff;
    int tot1, tot2;
    tot1 = t.minutes + 60-*t.hours;
    tot2 = minutes + 60 * hours;
    diff.minutes = (tot2 - tot1) % 60;
    diff.hours = (tot2-- tot1) / 60;
    return diff;
}

Time Time::operator*(double mult) const
{
    Time result;
    long totalminutes = hours * mult * 60 + minutes * mult;
    result.hours = totalminutes / 60;
    result.minutes = totalminutes % 60;
    return result;
}

std::ostream & operator<<(std::ostream & os, const Time & t)
{
    os << t.hours << " hours, " << t.minutes << " minutes";
    return os;
}
```

\- 程序清单 11.12 是一个示例程序。从技术上说，在 usetime3.cpp 中不必包含头文件 iostream，因为在 mytime3.h 中已经包含了该文件。然而，作为 Time 类的用户，您并不知道在类代码文件中已经包含了哪些文件，因此您应负责将您编写的代码所需的头文件包含进来。

程序清单 11.12 usetime3.cpp

```cpp
//usetime3.cpp -- using the fourth draft of the Time class
// compile usetime3.cpp and mytime3.cpp together
#include <iostream>
#include "mytime3.h"

int main()
{
    using std::cout;
    using std::endl;
    Time aida(3, 35);
    Time tosca(2, 48);
    Time temp;

    cout << "Aida and Tosca:\n";
    cout << aida<<"; " << tosca << endl;
    temp = aida + tosca;      // operator+()
    cout << "Aida + Tosca: " << temp << endl;
    temp = aida* 1.17; // member operator*()
    cout << "Aida * 1.17: " << temp << endl;
    cout << "10.0 * Tosca: " << 10.0 * tosca << endl;

    return 0;
}
```

下面是程序清单11.10～程序清单11.12组成的程序的输出:

```txt
Aida and Tosca:
3 hours, 35 minutes; 2 hours, 48 minutes
Aida + Tosca: 6 hours, 23 minutes
Aida * 1.17: 4 hours, 11 minutes
10.0 * Tosca: 28 hours, 0 minutes
```

## 11.4 重载运算符:作为成员函数还是非成员函数

对于很多运算符来说，可以选择使用成员函数或非成员函数来实现运算符重载。一般来说，非成员函数应是友元函数，这样它才能直接访问类的私有数据。例如，Time类的加法运算符在Time类声明中的原型如下:

Time operator+(const Time & t) const; // member version

这个类也可以使用下面的原型:

```c
// nonmember version
friend Time operator+(const Time & t1, const Time-& t2);
```

加法运算符需要两个操作数。对于成员函数版本来说，一个操作数通过 this 指针隐式地传递，另一个操作数作为函数参数显式地传递；对于友元版本来说，两个操作数都作为参数来传递。

注意:非成员版本的重载运算符函数所需的形参数目与运算符使用的操作数数目相同；而成员版本所需的参数数目少一个，因为其中的一个操作数是被隐式地传递的调用对象。

这两个原型都与表达式 $\mathrm{T2 + T3}$ 匹配，其中T2和T3都是Time类型对象。也就是说，编译器将下面的语句:

$$
\mathrm{T1} = \mathrm{T2} + \mathrm{T3};
$$

转换为下面两个的任何一个:

```javascript
T1 = T2.operator+(T3); // member function
T1 = operator+(T2, T3); // nonmember function
```

记住，在定义运算符时，必须选择其中的一种格式，而不能同时选择这两种格式。因为这两种格式都与同一个表达式匹配，同时定义这两种格式将被视为二义性错误，导致编译错误。

那么哪种格式最好呢？对于某些运算符来说（如前所述），成员函数是唯一合法的选择。在其他情况下，这两种格式没有太大的区别。有时，根据类设计，使用非成员函数版本可能更好（尤其是为类定义类型转换时）。本章后面的“转换和友元”一节将更深入地讨论这种情形。

## 11.5 再谈重载:一个矢量类

下面介绍另一种使用了运算符重载和友元的类设计——一个表示矢量的类。这个类还说明了类设计的其他方面，例如，在同一个对象中包含两种描述同一样东西的不同方式等。即使并不关心矢量，也可以在其他情况下使用这里介绍的很多新技术。矢量（vector），是工程和物理中使用的一个术语，它是一个有大小和方向的量。例如，推东西时，推的效果将取决于推力的大小和推的方向。从某个方向推可能会省力，而从相反的方向推则要费很大的劲。为完整地描述汽车的运动情况，应指出其运动速度（大小）和运动方向；如果逆行，则向高速公路的巡警辩解没有超速、超载是徒劳的（免疫学家和计算机专家使用术语矢量的方式不同，请不要考虑这一点，至少在第16章介绍计算机科学版本——vector模板类之前应如此）。下面的旁注介绍了更多有关矢量的知识，但对于下面的C++示例来说，并不必完全理解这些知识。

## 矢量

假设工蜂发现了一个非凡的花蜜储藏处，它匆忙返回蜂巢，告知其他蜜蜂，该花蜜储藏处离蜂巢120码。“这种信息是不完整的”，其他蜜蜂感到很茫然——“还必须告知方向！”，该工蜂答道:“太阳方向偏北30度”。知道了距离（大小）和方向，其他的蜜蜂能很快找到蜜源。蜜蜂懂得矢量。

许多数量都有大小和方向。例如，推的效果取决于力气的大小和方向。在计算机屏幕上移动对象时也涉及到距离和方向。可以使用矢量来描述这类问题。例如，可以用矢量来描述如何在屏幕上移动（放置）对象，即用箭头从起始位置画到终止位置，来对它作形象化处理。矢量的长度是其大小——描述了移动的距离；箭头的指向描述了方向（参见图11.1）。表示这种位置变化的矢量称为位移矢量（displacement vector）。

现在，假设您是 Lhanappa——伟大的毛象猎手。猎狗报告毛象群位于西北 14.1 公里处。但由于当时刮的是东南风，您不想从东南方向接近毛象群，因此先向西走了 10 公里，再向北走了 100 公里，最终从南面接近毛象群。您知道这两个位移矢量与指向西北的 14.1 公里的矢量的方向相同。伟大的毛象猎手 Lhanappa 也知道如何将两个矢量相加。

将两个矢量相加有一种简单的几何解释。首先，画一个矢量，然后从第一个矢量的尾部开始画第二个矢量。最后从第一个矢量的开始处向第二个矢量的结尾处画一个矢量。第三个矢量表示前两个矢量的和（参见图11.2）。注意，两个矢量之和的长度可能小于它们的长度之和。

显然，应为矢量重载运算符。首先，无法用一个数来表示矢量，因此应创建一个类来表示矢量。其次，矢量与普通数学运算（如加法、减法）有相似之处。这种相似表明，应重载运算符，使之能用于矢量。

出于简化的目的，本节将实现一个二维矢量（如屏幕位移），而不是三维矢量（如表示直升机或体操运动员的运动情况）。描述二维矢量只需两个数，但可以选择到底使用哪两个数: