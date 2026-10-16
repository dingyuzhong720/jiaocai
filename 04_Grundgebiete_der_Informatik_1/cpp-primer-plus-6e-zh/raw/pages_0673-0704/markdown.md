# 第 16 章 string 类和标准模板库

## 本章内容包括:

- 标准 C++ string 类。
- 模板 auto\_ptr、unique\_ptr 和 shared\_ptr。
● 标准模板库（STL）。
- 容器类。
- 迭代器。
- 函数对象（functor）。
- STL算法。
- 模板 initializer\_list。

至此您熟悉了 C++ 可重用代码的目标，这样做的一个很大的回报是可以重用别人编写的代码，这正是类库的用武之地。有很多商业 C++ 类库，也有一些库是 C++ 程序包自带的。例如，曾使用过的头文件 ostream 支持的输入/输出类。本章介绍一些其他可重用代码，它们将给编程工作带来快乐。

本书前面介绍过 string 类，本章将更深入地讨论它；然后介绍“智能指针”模板类，它们让管理动态内存更容易；接下来介绍标准模板库（STL），它是一组用于处理各种容器对象的模板。STL 演示了一种编程模式——泛型编程；最后，本章将介绍 C++11 新增的模板 initializer\_list，它让您能够将初始化列表语法用于 STL 对象。

## 16.1 string 类

很多应用程序都需要处理字符串。C语言在string.h（在 $\mathrm{C + + }$ 中为cstring）中提供了一系列的字符串函数，很多早期的 $\mathrm{C + + }$ 实现为处理字符串提供了自己的类。第4章介绍了ANSI/ISO $\mathrm{C + + }$ string类，而第12章创建了一个不大的String类，以说明设计表示字符串的类的某些方面。

string 类是由头文件 string 支持的（注意，头文件 string.h 和 cstring 支持对 C-风格字符串进行操纵的 C 库字符串函数，但不支持 string 类）。要使用类，关键在于知道它的公有接口，而 string 类包含大量的方法，其中包括了若干构造函数，用于将字符串赋给变量、合并字符串、比较字符串和访问各个元素的重载运算符以及用于在字符串中查找字符和子字符串的工具等。简而言之，string 类包含的内容很多。

## 16.1.1 构造字符串

先来看 string 的构造函数。毕竟，对于类而言，最重要的内容之一是，有哪些方法可用于创建其对象。程序清单 16.1 使用了 string 的 7 个构造函数（用 ctor 标识，这是传统 C++ 中构造函数的缩写）。表 16.1 简要地描述了这些构造函数，它首先使用顺序简要描述了程序清单 16.1 使用的 7 个构造函数，然后列出了 C++11 新增的两个构造函数。使用构造函数时都进行了简化，即隐藏了这样一个事实:string 实际上是模板具体化 basic\_string&lt;char&gt;的一个 typedef，同时省略了与内存管理相关的参数（这将在本章后面和附录 F中讨论)。size\_type 是一个依赖于实现的整型，是在头文件 string 中定义的。string 类将 string::npos 定义为字符串的最大长度，通常为 unsigned int 的最大值。另外，表格中使用缩写 NBTS（null-terminated string）来表示以空字符结束的字符串——传统的 C 字符串。

表 16.1

string 类的构造函数

<table><tr><td>构造函数</td><td>描述</td></tr><tr><td>string(const char * s)</td><td>将 string 对象初始化为 s 指向的 NBTS</td></tr><tr><td>string(size_type n, char c)</td><td>创建一个包含 n 个元素的 string 对象,其中每个元素都被初始化为字符 c</td></tr><tr><td>string(const string &amp; str)</td><td>将一个 string 对象初始化为 string 对象 str(复制构造函数)</td></tr><tr><td>string()</td><td>创建一个默认的 sting 对象,长度为 0(默认构造函数)</td></tr><tr><td>string(const char * s, size_type n)</td><td>将 string 对象初始化为 s 指向的 NBTS 的前 n 个字符,即使超过了 NBTS 结尾</td></tr><tr><td>template</td><td rowspan="2">将 string 对象初始化为区间[begin, end)内的字符,其中 begin 和 end 的行为就像指针,用于指定位置,范围包括 begin 在内,但不包括 end</td></tr><tr><td>string(Iter begin, Iter end)</td></tr><tr><td>string(const string &amp; str, string size_type pos = 0, size_type n = npos)</td><td>将一个 string 对象初始化为对象 str 中从位置 pos 开始到结尾的字符,或从位置 pos 开始的 n 个字符</td></tr><tr><td>string(string &amp;&amp; str) noexcept</td><td>这是 C++11 新增的,它将一个 string 对象初始化为 string 对象 str,并可能修改 str(移动构造函数)</td></tr><tr><td>string(initializer_list&#x27;il)</td><td>这是 C++11 新增的,它将一个 string 对象初始化为初始化列表 il 中的字符</td></tr></table>

程序清单 16.1 str1.cpp

```cpp
// str1.cpp -- introducing the string class
#include <iostream>
#include <string>
// using string constructors

int main()
{
    using namespace std;
    string one("Lottery Winner!");      // ctor #1
    cout << one << endl;             // overloaded <<
    string two(20, '\$');              // ctor #2
    cout << two << endl;
    string three(one);                 // ctor #3
    cout << three << endl;
    one += " Oops!";               // overloaded +=
    cout << one << endl;
    two = "Sorry! That was ";
    three[0] = 'P';
    string four;                             // ctor #4
    four = two + three;                 // overloaded +, =
    cout << four << endl;
    char alls[] = "All's well that ends well";
    string five(alls,20);                // ctor #5
    cout << five << "!\n";
    string six(alls+6, alls + 10);     // ctor #6
    cout << six << ", ";
    string seven(&five[6], &five[10]); // ctor #6 again
    cout << seven << "...\n";
    string eight(four, 7, 16);        // ctor #7
```

```txt
cout << eight << " in motion!" << endl;
    return 0;
}
```

程序清单 16.1 中程序还使用了重载+=运算符，它将一个字符串附加到另一个字符串的后面；重载的=运算符用于将一个字符串赋给另一个字符串；重载的<<运算符用于显示 string 对象；重载的[]运算符用于访问字符串中的各个字符。

下面是程序清单16.1中程序的输出:

```txt
Lottery Winner!
$$$$$$$$$$$$$$$$$$$$
Lottery Winner!
Lottery Winner! Oops!
Sorry! That was Pottery Winner!
All's well that ends!
well, well...
That was Pottery in motion!
```

## 1. 程序说明

程序清单 16.1 中的程序首先演示了可以将 string 对象初始化为常规的 C-风格字符串，然后使用重载的<<运算符来显示它:

```cpp
string one("Lottery Winner!");    // ctor #1
cout << one << endl;           // overloaded <<
```

接下来的构造函数将 string 对象 two 初始化为由 20 个\$字符组成的字符串:

```txt
string two(20, '$'); // ctor #2
```

复制构造函数将 string 对象 three 初始化为 string 对象 one:

```javascript
string three(one);== // ctor #3
```

重载的+=运算符将字符串 “Oops!” 附加到字符串 one 的后面:

```javascript
one += " Oops!";          // overloaded +=
```

这里是将一个 C-风格字符串附加到一个 string 对象的后面。但+=运算符被多次重载，以便能够附加 string 对象和单个字符:

```txt
one += two;   // append a string object (not in program)
one += '!';   // append a type char value (not-in program)
```

同样，=运算符也被重载，以便可以将 string 对象、C-风格字符串或 char 值赋给 string 对象:

```txt
two = "Sorry! That was "; // assign a C-style string
two = one;                 // assign a string object (not in program)=
two = '?';                   // assign a char value (not in program)
```

重载[]运算符（就像第12章的String示例那样）使得可以使用数组表示法来访问string对象中的各个字符:

```javascript
three[0] = 'P';
```

默认构造函数创建一个以后可对其进行赋值的空字符串:

```txt
string four;                      // ctor #4
four = two + three;                 // overloaded +, =
```

第 2 行使用重载的+运算符创建了一个临时 string 对象，然后使用重载的=运算符将它赋给对象 four。正如所预料的，+运算符将其两个操作数组合成一个 string 对象。该运算符被多次重载，以便第二个操作数可以是 string 对象、C-风格字符串或 char 值。

第 5 个构造函数将一个 C-风格字符串和一个整数作为参数，其中的整数参数表示要复制多少个字符:

```javascript
char alls[] = "All's well that ends-well";
string five(alls,20);          // ctor #5
```

从输出可知，这里只使用了前 20 个字符（“All's well that ends”）来初始化 five 对象。正如表 16.1 指出的，如果字符数超过了 C-风格字符串的长度，仍将复制请求数目的字符。所以在上面的例子中，如果用 40 代替 20，将导致 15 个无用字符被复制到 five 的结尾处（即构造函数将内存中位于字符串“All's well that ends well”后面的内容作为字符）。

第6个构造函数有一个模板参数:

```cpp
template<class Iter> string(Iter begin, Iter end);
```

begin 和 end 将像指针那样，指向内存中两个位置（通常，begin 和 end 可以是迭代器——广泛用于 STE 中的广义化指针）。构造函数将使用 begin 和 end 指向的位置之间的值，对 string 对象进行初始化。[begin, end) 来自数学中，意味着包括 begin，但不包括 end 在内的区间。也就是说，end 指向被使用的最后一个值后面的一个位置。请看下面的语句:

```txt
string six(alls+6, alls + I0); // ctor #6-
```

由于数组名相当于指针，所以 alls +6 和 alls +10 的类型都是 char \*，因此使用模板时，将用类型 char \* 替换 Iter。第一个参数指向数组 alls 中的第一个 w，第二个参数指向第一个 well 后面的空格。因此，six 将被初始化为字符串 “well”。图 16.1 说明了该构造函数的工作原理。

![](images/page_675_image_10.jpg)

<details>
<summary>text_image</summary>

char alls[] = "All's well" that ends well";
string six(alls + 6, alls + 10);
    range = [alls + 6, alls + 10]
alls: A l l s w e l l t h a t e n d s w e l l \0
0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25
six: w e l l
</details>

图 16.1 使用区间的 string 构造函数

现在假设要用这个构造函数将对象初始化为另一个 string 对象（假设为 five）的一部分内容，则下面的语句不管用:

```txt
string seven(five + 6, five + 10);
```

原因在于，对象名（不同于数组名）不会被看作是对象的地址，因此 five 不是指针，所以 five + 6 是没有意义的。然而，five[6] 是一个 char 值，所以 &five[6] 是一个地址，因此可被用作该构造函数的一个参数。

```c
string seven(&five[6], &five[10]); // ctor #6 again
```

第 7 个构造函数将一个 string 对象的部分内容复制到构造的对象中:

```javascript
string-eight(four, 7, -16); // ctor #7
```

上述语句从 four 的第 8 个字符（位置 7）开始，将 16 个字符复制到 eight 中。

2. C++11 新增的构造函数

构造函数 string（string && str）类似于复制构造函数，导致新创建的 string 为 str 的副本。但与复制构造函数不同的是，它不保证将 str 视为 const。这种构造函数被称为移动构造函数（move constructor）。在有些情况下，编译器可使用它而不是复制构造函数，以优化性能。第 18 章的“移动语义和右值引用”一节将讨论这个主题。

构造函数 string（initializer\_list&lt;char&gt; il）让您能够将列表初始化语法用于 string 类。也就是说，它使得下面这样的声明是合法的:

```txt
string piano_man = {'L', 'i', 's','z','t'};
string comp_lang {'L', 'i', 's', 'p'};
```

就 string 类而言，这可能用处不大，因为使用 C-风格字符串更容易，但确实实现了让列表初始化语法普遍实用的意图。本章后面将更深入地讨论模板 initializer\_list。

## 16.1.2 string 类输入

对于类，很有帮助的另一点是，知道有哪些输入方式可用。对于 C-风格字符串，有 3 种方式:

```txt
char info[100];
cin >> info;          // read a word
cin.getline(info, 100);   // read a line, discard \n
cin.get(info, 100);     // read a line, leave \n in queue
```

对于 string 对象，有两种方式:

```c
string stuff;
cin >> stuff;          // read a word
getline(cin, stuff);     // read a line, discard \n
```

两个版本的 getline()都有一个可选参数，用于指定使用哪个字符来确定输入的边界:

```javascript
cin.getline(info,100,':',      // read up to :, discard :
getline(stuff, ':');          // read up to :, discard :
```

在功能上，它们之间的主要区别在于，string 版本的 getline() 将自动调整目标 string 对象的大小，使之刚好能够存储输入的字符:

```c
char fname[10];
string lname;
cin >> fname;      // could be a problem if input size > 9 characters
cin >> lname;       // can read a very, very long word
cin.getline(fname, 10);   // may truncate input
getline(cin, fname);     // no truncation
```

自动调整大小的功能让 string 版本的 getline() 不需要指定读取多少个字符的数值参数。

在设计方面的一个区别是，读取 C-风格字符串的函数是 istream 类的方法，而 string 版本是独立的函数。这就是对于 C-风格字符串输入，cin 是调用对象；而对于 string 对象输入，cin 是一个函数参数的原因。这种规则也适用于>>形式，如果使用函数形式来编写代码，这一点将显而易见:

```cpp
cin.operator>>(fname);      // ostream class method
operator>>(cin, lname);     // regular function
```

下面更深入地探讨一下 string 输入函数。正如前面指出的，这两个函数都自动调整目标 string 的大小，使之与输入匹配。但也存在一些限制。第一个限制因素是 string 对象的最大允许长度，由常量 string::npos 指定。这通常是最大的 unsigned int 值，因此对于普通的交互式输入，这不会带来实际的限制；但如果您试图将整个文件的内容读取到单个 string 对象中，这可能成为限制因素。第二个限制因素是程序可以使用的内存量。

string 版本的 getline() 函数从输入中读取字符，并将其存储到目标 string 中，直到发生下列三种情况之一:

\- 到达文件尾，在这种情况下，输入流的 eofbit 将被设置，这意味着方法 fail() 和 eof() 都将返回 true;

● 遇到分界字符（默认为\n），在这种情况下，将把分界字符从输入流中删除，但不存储它；
- 读取的字符数达到最大允许值（string::npos 和可供分配的内存字节数中较小的一个），在这种情况下，将设置输入流的failbit，这意味着方法 fail() 将返回 true。

输入流对象有一个统计系统，用于跟踪流的错误状态。在这个系统中，检测到文件尾后将设置 eofbit 寄存器，检测到输入错误时将设置 failbit 寄存器，出现无法识别的故障（如硬盘故障）一时将设置 badbit 寄存器，一切顺利时将设置 goodbit 寄存器。第 17 章将更深入地讨论这一点。

string 版本的 operator>>()函数的行为与此类似，只是它不断读取，直到遇到空白字符并将其留在输入队列中，而不是不断读取，直到遇到分界字符并将其丢弃。空白字符指的是空格、换行符和制表符，更普遍地说，是任何将其作为参数来调用 isspace()时，该函数返回 ture 的字符。

本书前面有多个控制台 string 输入示例。由于用于 string 对象的输入函数使用输入流，能够识别文件尾，因此也可以使用它们来从文件中读取输入。程序清单 16.2 是一个从文件中读取字符串的简短示例，它假设文件中包含用冒号字符分隔的字符串，并使用指定分界符的 getline() 方法。然后，显示字符串并给它们编号，每个字符串占一行。

程序清单 16.2 strfile.cpp

```cpp
// strfile.cpp -- read strings from a file
#include <iostream>
#include <fstream>
#include <string>
#include <cstdlib>
int main()
{
    using namespace std;
    ifstream fin;
    fin.open("tobuy.txt");
    if (fin.is_open() == false)
    {
        cerr << "Can't open file. Bye.\n";
        exit(EXIT_FAILURE);
    }
    string item;
    int count = 0;
    getline(fin, item, ':');
    while (fin)  // while input is good
    {
        ++count;
        cout << count <<": " << item-<< endl;
        getline(fin, item, ':');
    }
    cout << "Done\n";
    fin.close();
    return 0;
}
```

下面是文件 tobuy.txt 的内容:

```yaml
sardines:chocolate ice cream:pop corn:leeks:
cottage cheese:olive=orf:butter:tofu:
```

通常，对于程序要查找的文本文件，应将其放在可执行程序或项目文件所在的目录中；否则必须提供完整的路径名。在 Windows 系统中，C-风格字符串中的转义序列\表示一个斜杠:

```txt
fin.open("C=\CPP\Progs\tobuy.txt")，// file = C:\CPP\Progs\tobuy.txt
```

下面是程序清单 16.2 中程序的输出:

```txt
sardines
chocolate ice cream
pop corn
leeks
cottage cheese
olive oil
butter
tofu
Done
```

注意，将:指定为分界字符后，换行符将被视为常规字符。因此文件 tobuy.txt 中第一行末尾的换行符将成为包含 “cottage cheese” 的字符串中的第一个字符。同样，第二行末尾的换行符是第 9 个输入字符串中唯一的内容。

## 16.1.3 使用字符串

现在，您知道可以使用不同方式来创建 string 对象、显示 string 对象的内容、将数据读取和附加到 string 对象中、给 string 对象赋值以及将两个 string 对象连结起来。除此之外，还能做些什么呢？

可以比较字符串。String 类对全部 6 个关系运算符都进行了重载。如果在机器排列序列中，一个对象位于另一个对象的前面，则前者被视为小于后者。如果机器排列序列为 ASCII 码，则数字将小于大写字符，而大写字符小于小写字符。对于每个关系运算符，都以三种方式被重载，以便能够将 string 对象与另一个 string 对象、C-风格字符串进行比较，并能够将 C-风格字符串与 string 对象进行比较:

```txt
string snake1("cobra");
string snake2("coral");
char snake3[20] = "anaconda";
if (snake1 < snake 2)          // operator<(const string &, const string &) ...
if (snake1 == snake3)         // operator==(const string &, const char *)
    ...
if (snake3 != snake2)         // operator!=(const char *, const string &)
```

可以确定字符串的长度。size()和length()成员函数都返回字符串中的字符数:

```txt
if (snake1.length() == snake2.size())
    cout << "Both strings have the same length.\n"
```

为什么这两个函数完成相同的任务呢？length()成员来自较早版本的string类，而size()则是为提供STL兼容性而添加的。

可以以多种不同的方式在字符串中搜索给定的子字符串或字符。表 16.2 简要地描述了 find() 方法的 4 个版本。如前所述，string ::npos 是字符串可存储的最大字符数，通常是无符号 int 或无符号 long 的最大取值。

表 16.2

重载的 find() 方法

| 方法原型 | 描述 |
| --- | --- |
| size_type find(const string &amp; str,size_type pos = 0)const | 从字符串的pos位置开始,查找子字符串str。如果找到,则返回该子字符串首次出现时其首字符的索引;否则,返回string::npos |
| size_type find(const char * s,size_type pos = 0)const | 从字符串的pos位置开始,查找子字符串s。如果找到,则返回该子字符串首次出现时其首字符的索引;否则,返回string::npos |
| size_type find(const char * s,size_type pos=0, size_type n) | 从字符串的pos位置开始,查找s的前n个字符组成的子字符串。如果找到,则返回该子字符串首次出现时其首字符的索引;否则,返回string::npos |
| size_type find(char ch,size_type pos=0,const- | 从字符串的pos位置开始,查找字符ch。如果找到,则返回该字符首次出现的位置;否则,返回string::npos |

string 库还提供了相关的方法:rfind()、find\_first\_of()、find\_last\_of()、find\_first\_not\_of()和 find\_last\_not\_of()，它们的重载函数特征标都与 find()方法相同。rfind()方法查找子字符串或字符最后一次出现的位置；find\_first\_of()方法在字符串中查找参数中任何一个字符首次出现的位置。例如，下面的语句返回 r 在“cobra”中的位置（即索引3），因为这是“hark”中各个字母在“cobra”首次出现的位置:

```javascript
int where = snake1.find_first_of("hark");
```

find\_last\_of()方法的功能与此相同，只是它查找的是最后一次出现的位置。因此，下面的语句返回 a 在“cobra”中的位置:

```javascript
int where = snake1.last_first_of("hark");
```

find\_first\_not\_of()方法在字符串中查找第一个不包含在参数中的字符，因此下面的语句返回 c 在“cobra”中的位置，因为“hark”中没有 c:

```javascript
int where = snake1.find_first_not_of("hark");
```

在本章最后的练习中，您将了解 find\_last\_not\_of()。

还有很多其他的方法，这些方法足以创建一个非图形版本的 Hangman 拼字游戏。该游戏将一系列的单词存储在一个 string 对象数组中，然后随机选择一个单词，让人猜测单词的字母。如果猜错 6 次，玩家就输了。该程序使用 find() 函数来检查玩家的猜测，使用 += 运算符创建一个 string 对象来记录玩家的错误猜测。为记录玩家猜对的情况，程序创建了一个单词，其长度与被猜的单词相同，但包含的是连字符。玩家猜对字符时，将用该字符替换相应的连字符。程序清单 16.3 列出了该程序的代码。

程序清单 16.3 hangman.cpp

```cpp
// hangman.cpp -- some string methods
#include <iostream>
#include <string>
#include <cstdlib>
#include <ctime>
#include <cctype>
using std::string;
const int NUM = 26;
const string wordlist[NUM] = {"apiary", "beetle", "cereal",
    "danger", "ensign", "florid", "garage", "health", "insult",
    "jackal", "keeper", "loaner", "manage", "nonce", "onset",
    "plaid", "quilt","remote", "stolid", "train", "useful",
    "valid", "whence", "xenon", "yearn", "zippy"};

int main()
{
    using std::cout;
    using std::cin;
    using std::tolower;
    using std::endl;
    std::srand(std::time(0));
    char play;
    cout << "WilF you play a word game? <y/n> ";
```

```cpp
cin >> play;
play = tolower(play);
while (play == 'y'[ 
{
    string-target = wordlist[std::rand() % NUM];
    int length = target.length();
    string attempt(length, '-');
    string badchars;
    int guesses = 6;
    cout << "Guess my secret-word. It has " << length
        << " letters, and you guess\n"
        << "one-letter at a time. You get " << guesses
<< " wrong guesses.\n";
cout << "Your word: " << attempt << endl;
while (guesses > 0 && attempt != target)-
{
    char letter;
    cout << "Guess a letter: ";
    cin >> letter;
    if (badchars.find(letter) != string::npos
        || attempt.find(letter) != string::npos)
    {
        cout << "You already guessed that. Try again.\n";
            continue;
    }
    int loc = target.find(letter);
    if (loc == string::npos)
    {
        cout << "Oh, bad guess!\n";
        --guesses;
        badchars += letter; // add to string
    }
    else
    {
        cout << "Good guess!\n";
        attempt[loc]=letter;
        // check if letter appears again
        loc = target.find(letter, loc + 1);
        while (loc != string::npos)
        {
            attempt[loc]=letter;
            loc = target.find(letter, loc + 1);
        }
    }
    cout << "Your word: " << attempt << endl;
    if (attempt != target)
    {
        if (badchars.length() > 0)
            cout << "Bad choices: " << badchars << endl;
        cout << guesses << " bad guesses=left\n";
    }
}
if (guesses > 0)
    cout << "That's right!\n";
else
```

```perl
cout << "Sorry, the word is " << target << ".\n";
        cout << "Will you play another? <y/n> ";
        cin >> play;
        play = tolower(play);
}

cout << "Bye\n";

return 0;
}
```

程序清单16.3中程序的运行情况如下:

```txt
Will you play a word game? <y/n> y
Guess my secret word. It has 6 letters, and you guess one letter at a time. You get 6 wrong guesses.
Your word: ------
Guess a letter: e
Oh, bad guess!
Your word: --------
Bad choices: e
5 bad guesses left
Guess a letter: a
Good guess!
Your word: a--a--
Bad choices: e
5 bad guesses left
Guess a letter: t
Oh, bad guess!
Your word: a--a--
Bad choices: et
4 bad guesses left
Guess a letter: r
Good guess!
Your word: a--ar-
Bad choices: et
4 bad guesses left
Guess a letter: y
Good guess!
Your word: a--ary
Bad choices: et
4 bad guesses left
Guess a letter: i
Good guess!
Your word: a-iary
Bad choices: et
4 bad guesses left
Guess a letter: p
Good guess!
Your word: apiary
That's right!
Will you play another? <y/n> n
Bye
```

## 程序说明

在程序清单 16.3 中，由于关系运算符被重载，因此可以像对待数值变量那样对待字符串:

```txt
while (guesses > 0 && attempt != target)
```

与对 C-风格字符串使用 strcmp()相比，这样简单些。

该程序使用 find() 来检查玩家以前是否猜过某个字符。如果是，则它要么位于 badchars 字符串（猜错）中，要么位于 attempt 字符串（猜对）中:

```txt
if (badchars.find(letter) != string::npos
    || attempt.find(letter) != string::npos)
```

npos 变量是 string 类的静态成员，它的值是 string 对象能存储的最大字符数。由于索引从 0 开始，所以它比最大的索引值大 1，因此可以使用它来表示没有查找到字符或字符串。

该程序利用了这样一个事实:+=运算符的某个重载版本使得能够将一个字符附加到字符串中:

```txt
badchars += letter;  // append a char to a string object
```

该程序的核心是从检查玩家选择的字符是否位于被猜测的单词中开始的:

```javascript
int loc = target.find(letter);
```

如果 loc 是一个有效的值，则可以将该字母放置在答案字符串的相应位置:

```javascript
attempt[loc]=letter;
```

然而，由于字母在被猜测的单词中可能出现多次，所以程序必须一直进行检查。该程序使用了 find() 的第二个可选参数，该参数可以指定从字符串什么位置开始搜索。因为字母是在位置 loc 找到的，所以下一次搜索应从 loc+1 开始。while 循环使搜索一直进行下去，直到找不到该字符为止。如果 loc 位于字符串尾，则表明 find() 没有找到该字符。

```rust
// check if letter appears again
loc = target.find(letter, loc + 1);
while (loc != string::npos)
{
    attempt[loc]=letter;
    loc = target.find(letter, loc + 1);
}
```

## 16.1.4 string 还提供了哪些功能

string 库提供了很多其他的工具，包括完成下述功能的函数:删除字符串的部分或全部内容、用一个字符串的部分或全部内容替换另一个字符串的部分或全部内容、将数据插入到字符串中或删除字符串中的数据、将一个字符串的部分或全部内容与另一个字符串的部分或全部内容进行比较、从字符串中提取子字符串、将一个字符串中的内容复制到另一个字符串中、交换两个字符串的内容。这些函数中的大多数都被重载，以便能够同时处理 C-风格字符串和 string 对象。附录 F 简要地介绍了 string 库中的函数。

首先来看自动调整大小的功能。在程序清单16.3中，每当程序将一个字母附加到字符串末尾时将发生什么呢？不能仅仅将已有的字符串加大，因为相邻的内存可能被占用了。因此，可能需要分配一个新的内存块，并将原来的内容复制到新的内存单元中。如果执行大量这样的操作，效率将非常低，因此很多C++实现分配一个比实际字符串大的内存块，为字符串提供了增大空间。然而，如果字符串不断增大，超过了内存块的大小，程序将分配一个大小为原来两倍的新内存块，以提供足够的增大空间，避免不断地分配新的内存块。方法capacity()返回当前分配给字符串的内存块的大小，而reserve()方法让您能够请求内存块的最小长度。程序清单16.4是一个使用这些方法的示例。

程序清单 16.4 str2.cpp

```cpp
// str2.cpp -- capacity() and reserve()
#include <iostream>
#include <string>
```

```cpp
int main()
{
    using namespace std;
    string empty;
    string small = "bit";
    string larger = "Elephants are a girl's best friend";
    cout << "Sizes:\n";
    cout << "\temporary: " << empty.size() << endl;
    cout << "\tsmall: " << small.size() << endl;
    cout << "\tlarger: " << larger.size() << endl;
    cout << "Capacities:\n";
    cout << "\temporary: " << empty.capacity() << endl;
    cout << "\tsmall: " << small.capacity() << endl;
    cout << "\tlarger: " << larger.capacity() << endl;
    empty.reserve(50);
    cout << "Capacity after empty.reserve(50): _
        << empty.capacity() << endl;
    return 0;
}
```

下面是使用某种C++实现时，程序清单16.4中程序的输出:

```yaml
Sizes:
    empty: 0
    small: 3
    larger: 34
Capacities:
    empty: 15
    small: 15
    larger: 47
Capacity after empty.reserve(50): 63
```

注意，该实现使用的最小容量为 E5 个字符，这比标准容量选择（E6 的倍数）小 1。其他实现可能做出不同的选择。

如果您有 string 对象, 但需要 C-风格字符串, 该如何办呢? 例如, 您可能想打开一个其名称存储在 string 对象中的文件:

```txt
string filename;
cout << "Enter file name: ";
cin >> filename;
ofstream fout;
```

不幸的是，open()方法要求使用一个C-风格字符串作为参数；幸运的是，c\_str()方法返回一个指向C-风格字符串的指针，该C-风格字符串的内容与用于调用c\_str()方法的string对象相同。因此可以这样做:

```txt
fout.open(filename:c_str());
```

## 16.1.5 字符串种类

本节将 string 类看作是基于 char 类型的。事实上，正如前面指出的，string 库实际上是基于一个模板类的:

```cpp
template<class charT, class traits = char _traits<charT>,
    class Allocator = allocator<charT> >
basic_string {...};
```

模板 basic\_string 有 4 个具体化，每个具体化都有一个 typedef 名称:

```c
typedef basic_string<char> string;
typedef basic_string<wchar_t> wstring;
typedef basic_string<char16_t> u16string;  // C++11
typedef basic_string<char32_t> u32string ;  // C++11
```

这让您能够使用基于类型 wchar\_t、char16\_t、char32\_t 和 char 的字符串。甚至可以开发某种类似字符的类，并对它使用 basic\_string 类模板（只要它满足某些要求）。traits 类描述关于选定字符类型的特定情况，如如何对值进行比较。对于 wchar\_t、char16\_t、char32\_t 和 char 类型，有预定义的 char\_traits 模板具体化，它们都是 traits 的默认值。Allocator 是一个管理内存分配的类。对于各种字符类型，都有预定义的 allocator 模板具体化，它们都是默认的。它们使用 new 和 delete。

## 16.2 智能指针模板类

智能指针是行为类似于指针的类对象，但这种对象还有其他功能。本节介绍三个可帮助管理动态内存分配的智能指针模板。先来看需要哪些功能以及这些功能是如何实现的。请看下面的函数:

```cpp
void remodel(std::string & str)
{
    std::string * ps = new std::string(str);
    ...
    str = ps;
    return;
}
```

您可能发现了其中的缺陷。每当调用时，该函数都分配堆中的内存，但从不收回，从而导致内存泄漏。您可能也知道解决之道——只要别忘了在 return 语句前添加下面的语句，以释放分配的内存即可:

```sql
delete ps;
```

然而，但凡涉及“别忘了”的解决方法，很少是最佳的。因为您有时可能忘了，有时可能记住了，但可能在不经意间删除或注释掉了这些代码。即使确实没有忘记，也可能有问题。请看下面的变体:

```cpp
void remodel(std::string & str)
{
    std::string * ps = new std::string(str);
    ...
    if (weird_thing())
        throw exception();
    str = *ps;
    delete ps;
    return;
}
```

当出现异常时，delete 将不被执行，因此也将导致内存泄漏。

可以按第 14 章介绍的方式修复这种问题，但如果有更灵巧的解决方法就好了。来看一下需要些什么。当 remodel() 这样的函数终止（不管是正常终止，还是由于出现了异常而终止），本地变量都将从栈内存中删除——因此指针 ps 占据的内存将被释放。如果 ps 指向的内存也被释放，那该有多好啊。如果 ps 有一个析构函数，该析构函数将在 ps 过期时释放它指向的内存。因此，ps 的问题在于，它只是一个常规指针，不是有析构函数的类对象。如果它是对象，则可以在对象过期时，让它的析构函数删除指向的内存。这正是 auto\_ptr、unique\_ptr 和 shared\_ptr 背后的思想。模板 auto\_ptr 是 C++98 提供的解决方案，C++11 已将其摒弃，并提供了另外两种解决方案。然而，虽然 auto\_ptr 被摒弃，但它已使用了多年:同时，如果您的编译器不支持其他两种解决方案，auto\_ptr 将是唯一的选择。

## 16.2.1 使用智能指针

这三个智能指针模板（auto\_ptr、unique\_ptr 和 shared\_ptr）都定义了类似指针的对象，可以将 new 获得（直接或间接）的地址赋给这种对象。当智能指针过期时，其析构函数将使用 delete 来释放内存。因此，如果将 new 返回的地址赋给这些对象，将无需记住稍后释放这些内存:在智能指针过期时，这些内存将自动被释放。图 16.2 说明了 auto\_ptr 和常规指针在行为方面的差别；share\_ptr 和 unique\_ptr 的行为与 auto\_ptr 相同。

![](images/page_685_image_4.jpg)

<details>
<summary>text_image</summary>

void demol()
{
    double * pd = new double; // #1
    *pd = 25.5;                 // #2
    return;                    // #3
}
#1.为pd和一个double值分配存储空间，保存地址：
pd      10000
           4000              10000
#2.将值复制到动态内存中：
pd      10000       25.5
           4000              10000
#3.删除pd,值被保留在动态内存中：
            25.5
            10000
void demo2()
{
    auto_ptr<double> ap(new double); // #1
    *ap = 25.5;                  // #2
    return;                   // #3
}
#1.为ap和一个double值分配存储空间，保存地址：
ap      10080
           6000              10080
#2.将值复制到动态内存中：
ap      10080       25.5
           6000              10000
#3.删除ap, ap的析构函数释放动态内存。
</details>

图 16.2 常规指针与 auto\_ptr

要创建智能指针对象，必须包含头文件 memory，该文件模板定义。然后使用通常的模板语法来实例化所需类型的指针。例如，模板 auto\_ptr 包含如下构造函数:

```cpp
template<class X> class auto_ptr {
public:
    explicit auto_ptr(X* p =0) throw();
...};
```

本书前面说过，throw()意味着构造函数不会引发异常；与 auto\_ptr 一样，throw()也被摒弃。因此，请求 X 类型的 auto\_ptr 将获得一个指向 X 类型的 auto\_ptr:

```txt
auto_ptr<double> pd(new double); // pd an auto_ptr to double
// {use in place of double * pd}
auto_ptr<string> ps(new string); // ps an auto_ptr to string
// {use in place of string * ps}
```

new double 是 new 返回的指针，指向新分配的内存块。它是构造函数 auto\_ptr&lt;double&gt; 的参数，即对应于原型中形参 p 的实参。同样，new string 也是构造函数的实参。其他两种智能指针使用同样的语法:

```cpp
unique_ptr<double> pdu(new double);  // pdu an unique_ptr to double
shared_ptr<string> pss(new string);  // pss a shared_ptr to string
```

因此，要转换 remodel() 函数，应按下面 3 个步骤进行:

1. 包含头文件 memory;
2. 将指向 string 的指针替换为指向 string 的智能指针对象；
3. 删除 delete 语句。

下面是使用 auto\_ptr 修改该函数的结果:

```cpp
#include <memory>
void remodel(std::string & str)
{
    std::auto_ptr<std::string> ps (new std::string(str));
    ...
    if (weird_thing())
        throw exception();
    str = *ps;
    // delete ps;  NO LONGER NEEDED
    return;
}
```

注意到智能指针模板位于名称空间 std 中。程序清单 16.5 是一个简单的程序，演示了如何使用全部三种智能指针。要编译该程序，您的编译器必须支持 C++11 新增的类 share\_ptr 和 unique\_ptr。每个智能指针都放在一个代码块内，这样离开代码块时，指针将过期。Report 类使用方法报告对象的创建和销毁。

程序清单 16.5 smrtptrs.cpp

```cpp
// smrtptrs.cpp -- using three kinds of smart pointers
// requires support of C++11 shared_ptr and unique_ptr
#include <iostream>
#include <string>
#include <memory>

class Report
{
private:
    std::string str;
public:
    Report(const std::string s) : str(s)
        { std::cout << "Object created!\n"; }
    -Report() { std::cout << "Object deleted!\n"; }
    void comment() const { std::cout << str << "\n"; }
};

int main()
{
```

```cpp
{
    std::auto_ptr<Report> ps (new Report("using auto_ptr"));
    ps->comment();   // use -> to invoke a member function
}
{
    std::shared_ptr<Report> ps (new Report("using shared_ptr"));
    ps->comment();
}
{
    std::unique_ptr<Report> ps (new Report("using unique_ptr"));
    ps->comment();
}
return 0;
}
```

该程序的输出如下:

```txt
Object created!
using auto_ptr
Object deleted!
Object created!
using shared_ptr
Object deleted!
Object created!
using unique_ptr
Object deleted!
```

所有智能指针类都一个 explicit 构造函数，该构造函数将指针作为参数。因此不需要自动将指针转换为智能指针对象:

```lisp
shared_ptr<double> pd;
double *p_reg = new double;
pd = p_reg;                      // not allowed (implicit conversion)
pd = shared_ptr<double>(p_reg);     // allowed (explicit conversion
shared_ptr<double> pshared = p_reg; // not allowed (implicit conversion)
shared_ptr<double> pshared(p_reg);  // allowed (explicit conversion)
```

由于智能指针模板类的定义方式，智能指针对象的很多方面都类似于常规指针。例如，如果 ps 是一个智能指针对象，则可以对它执行解除引用操作（\*ps）、用它来访问结构成员（ps->puffIndex）、将它赋给指向相同类型的常规指针。还可以将智能指针对象赋给另一个同类型的智能指针对象，但将引起一个问题，这将在下一节进行讨论。

但在此之前，先说说对全部三种智能指针都应避免的一点:

```txt
string vacation("I wandered lonely as a cloud.");
shared_ptr<string> pvac(&vacation);  // NO!
```

pvac 过期时，程序将把 delete 运算符用于非堆内存，这是错误的。

就程序清单 16.5 演示的情况而言，三种智能指针都能满足要求，但情况并非总是这样简单。

## 16.2.2 有关智能指针的注意事项

为何有三种智能指针呢？实际上有4种，但本书不讨论weak\_ptr。为何摒弃auto\_ptr呢？

先来看下面的赋值语句:

```txt
auto_ptr<string> ps (new string("I reigned lonely as a cloud."));
auto_ptr<string> vocation;
vocation = ps;
```

上述赋值语句将完成什么工作呢？如果 ps 和 vocation 是常规指针，则两个指针将指向同一个 string 对象。这是不能接受的，因为程序将试图删除同一个对象两次——一次是 ps 过期时，另一次是 vocation 过期时。要避免这种问题，方法有多种。

- 定义赋值运算符，使之执行深复制。这样两个指针将指向不同的对象，其中的一个对象是另一个对象的副本。
- 建立所有权（ownership）概念，对于特定的对象，只能有一个智能指针可拥有它，这样只有拥有对象的智能指针的构造函数会删除该对象。然后，让赋值操作转让所有权。这就是用于 auto\_ptr 和 unique\_ptr 的策略，但 unique\_ptr 的策略更严格。
- 创建智能更高的指针，跟踪引用特定对象的智能指针数。这称为引用计数（reference counting）。例如，赋值时，计数将加1，而指针过期时，计数将减1。仅当最后一个指针过期时，才调用delete。这是shared\_ptr采用的策略。

当然，同样的策略也适用于复制构造函数。

每种方法都有其用途。程序清单 16.6 是一个不适合使用 auto\_ptr 的示例。

程序清单 16.6 fowl.cpp

```cpp
// fowl.cpp --- auto_ptr a poor choice
#include <iostream>
#include <string>—
#include <memory>

int main()
{
    using namespace std;
    auto_ptr<string> films[5] =
    {
        auto_ptr<string> (new string("Fowl Balls")),
        auto_ptr<string> (new string("Duck Walks管控"))
        auto_ptr<string> (new string("Chicken Runs")),
        auto_ptr<string> (new string("Turkey Errors管控"),
        auto_ptr<string> (new string("Goose Eggs管控"))
    };
    auto_ptr<string> pwin;
    pwin = films[2];  // films[2] loses ownership=

    cout << "The nominees for best avian baseball=film are\n";
    for {-int i = 0; i < 5; i++}
        cout << *films[i] << endl;
    cout << "The winner is " << *pwin << "!\n";
    cin.get();
    return 0;
}
```

下面是该程序的输出:

```txt
The nominees for best avian baseball film are
Fowl Balls
Duck-Walks
Segmentation fault (core dumped)
```

消息 core dumped 表明，错误地使用 auto\_ptr 可能导致问题（这种代码的行为是不确定的，其行为可能随系统而异）。这里的问题在于，下面的语句将所有权从 films[2]转让给 pwin:

```javascript
pwin = films[2];   // films[2]—loses ownership
```

这导致 films[2]不再引用该字符串。在 auto\_ptr 放弃对象的所有权后，便可能使用它来访问该对象。当程序打印 films[2]指向的字符串时，却发现这是一个空指针，这显然讨厌的意外。

如果在程序清单 16.6 中使用 shared\_ptr 代替 auto\_ptr（这要求编译器支持 C++11 新增的 shared\_ptr 类），则程序将正常运行，其输出如下:

```txt
The nominees for best avian baseball film are
Fowl Balls
Duck Walks
Chicken Runs
Turkey Errors
Goose Eggs
The winner is Chicken Runs!
```

差别在于程序的如下部分:

```txt
shared_ptr<string> pwin;
pwin = films[2];
```

这次 pwin 和 films[2]指向同一个对象，而引用计数从 1 增加到 2。在程序末尾，后声明的 pwin 首先调用其析构函数，该析构函数将引用计数降低到 1。然后，shared\_ptr 数组的成员被释放，对 filmsp[2] 调用析构函数时，将引用计数降低到 0，并释放以前分配的空间。

因此使用 shared\_ptr 时，程序清单 16.6 运行正常；而使用 auto\_ptr 时，该程序在运行阶段崩溃。如果使用 unique\_ptr，结果将如何呢？与 auto\_ptr 一样，unique\_ptr 也采用所有权模型。但使用 unique\_ptr 时，程序不会等到运行阶段崩溃，而在编译器因下述代码行出现错误:

```javascript
pwin = films[2];
```

显然，该进一步探索 auto\_ptr 和 unique\_ptr 之间的差别。

## 16.2.3 unique\_ptr 为何优于 auto\_ptr

请看下面的语句:

```cpp
auto_ptr<string> p1(new string("auto");  //#1
auto_ptr<string> p2;                      //#2
p2 = p1;                            //#3
```

在语句#3中，p2接管string对象的所有权后，p1的所有权将被剥夺。前面说过，这是件好事，可防止p1和p2的析构函数试图删除同一个对象；但如果程序随后试图使用p1，这将是件坏事，因为p1不再指向有效的数据。

下面来看使用 unique\_ptr 的情况:

```txt
unique_ptr<string> p3(new string("auto");  //#4
unique_ptr<string> p4;                  //#5
p4 = p3;                            //#6
```

编译器认为语句#6非法，避免了p3不再指向有效数据的问题。因此，unique\_ptr比auto\_ptr更安全（编译阶段错误比潜在的程序崩溃更安全）。

但有时候，将一个智能指针赋给另一个并不会留下危险的悬挂指针。假设有如下函数定义:

```c
unique_ptr<string> demo(const char * s)
{
    unique_ptr<string> temp(new string(s));
    return temp;
}
```

并假设编写了如下代码:

```txt
unique_ptr<string> ps;
ps = demo("Uniquely special");
```

demo()返回一个临时 unique\_ptr，然后 ps 接管了原本归返回的 unique\_ptr 所有的对象，而返回的 unique\_ptr 被销毁。这没有问题，因为 ps 拥有了 string 对象的所有权。但这里的另一个好处是，demo()返回的临时 unique\_ptr 很快被销毁，没有机会使用它来访问无效的数据。换句话说，没有理由禁止这种赋值。神奇的是，编译器确实允许这种赋值！

总之，程序试图将一个 unique\_ptr 赋给另一个时，如果源 unique\_ptr 是个临时右值，编译器允许这样做；如果源 unique\_ptr 将存在一段时间，编译器将禁止这样做:

```txt
using namespace std;
unique_ptr< string> pu1(new string "Hi ho!");
unique_ptr< string> pu2;
pu2 = pu1;                                //#1 not allowed
unique_ptr<string> pu3;
pu3 = unique_ptr<string>(new string "Yo!");  //#2 allowed
```

语句#1 将留下悬挂的 unique\_ptr（pul），这可能导致危害。语句#2 不会留下悬挂的 unique\_ptr，因为它调用 unique\_ptr 的构造函数，该构造函数创建的临时对象在其所有权转让给 pu 后就会被销毁。这种随情况而异的行为表明，unique\_ptr 优于允许两种赋值的 auto\_ptr。这也是禁止（只是一种建议，编译器并不禁止）在容器对象中使用 auto\_ptr，但允许使用 unique\_ptr 的原因。如果容器算法试图对包含 unique\_ptr 的容器执行类似于语句#1 的操作，将导致编译错误；如果算法试图执行类似于语句#2 的操作，则不会有任何问题。而对于 auto\_ptr，类似于语句#1 的操作可能导致不确定的行为和神秘的崩溃。

当然，您可能确实想执行类似于语句#1的操作。仅当以非智能的方式使用遗弃的智能指针（如解除引用时），这种赋值才不安全。要安全地重用这种指针，可给它赋新值。C++有一个标准库函数 std::move()，让您能够将一个 unique\_ptr 赋给另一个。下面是一个使用前述 demo() 函数的例子，该函数返回一个 unique\_ptr&lt;string&gt;对象:

```txt
using namespace std;
unique_ptr<string> ps1, ps2;
ps1 = demo("Uniquely special");
ps2 = move(ps1);                      // enable assignment
ps1 = demo(" and more");
cout << *ps2 << *ps1 << endl;
```

您可能会问，unique\_ptr 如何能够区分安全和不安全的用法呢？答案是它使用了 C++11 新增的移动构造函数和右值引用，这将在第 18 章讨论。

相比于 auto\_ptr, unique\_ptr 还有另一个优点。它有一个可用于数组的变体。别忘了，必须将 delete 和 new 配对，将 delete [] 和 new [] 配对。模板 auto\_ptr 使用 delete 而不是 delete []，因此只能与 new 一起使用，而不能与 new [] 一起使用。但 unique\_ptr 有使用 new [] 和 delete [] 的版本:

```rust
std::unique_ptr< double[]>pda(new double(5));  // will use delete []
```

警告:使用 new 分配内存时，才能使用 auto\_ptr 和 shared\_ptr，使用 new [ ]分配内存时，不能使用它们。不使用 new 分配内存时，不能使用 auto\_ptr 或 shared\_ptr；不使用 new 或 new []分配内存时，不能使用 unique\_ptr。

## 16.2.4 选择智能指针

应使用哪种智能指针呢？如果程序要使用多个指向同一个对象的指针，应选择 shared\_ptr。这样的情况包括:有一个指针数组，并使用一些辅助指针来标识特定的元素，如最大的元素和最小的元素；两个对象包含都指向第三个对象的指针；STL 容器包含指针。很多 STL 算法都支持复制和赋值操作，这些操作可用于 shared\_ptr，但不能用于 unique\_ptr（编译器发出警告）和 auto\_ptr（行为不确定）。如果您的编译器没有提供 shared\_ptr，可使用 Boost 库提供的 shared\_ptr。

如果程序不需要多个指向同一个对象的指针，则可使用 unique\_ptr。如果函数使用 new 分配内存，并返回指向该内存的指针，将其返回类型声明为 unique\_ptr 是不错的选择。这样，所有权将转让给接受返回值的 unique\_ptr，而该智能指针将负责调用 delete。可将 unique\_ptr 存储到 STL 容器中，只要不调用将一个 unique\_ptr 复制或赋给另一个的方法或算法（如 sort()）。例如，可在程序中使用类似于下面的代码段，这里假设程序包含正确的 include 和 using 语句:

```txt
unique_ptr<int> make_int(int n)
{
    return unique_ptr<int>(new int(n));
}
void show(unique_ptr<int> & pi)          // pass by reference
{
    cout << *a << ' ';
}
int main()
{
...
    vector<unique_ptr<int> > vp(size);
    for (int i = 0; i < vp.size(); i++)
        vp[i] = make_int(rand() % 1000);   // copy temporary unique_ptr
    vp.push_back(make_int(rand() % 1000))  // ok because arg is temporary
    for_each(vp.begin(), vp.end(), show);  // use for_each()
...
}
```

其中的 push\_back() 调用没有问题，因为它返回一个临时 unique\_ptr，该 unique\_ptr 被赋给 vp 中的一个 unique\_ptr。另外，如果按值而不是按引用给 show() 传递对象，for\_each() 语句将非法，因为这将导致使用一个来自 vp 的非临时 unique\_ptr 初始化 pi，而这是不允许的。前面说过，编译器将发现错误使用 unique\_ptr 的企图。

在 unique\_ptr 为右值时，可将其赋给 shared\_ptr，这与将一个 unique\_ptr 赋给另一个需要满足的条件相同。与前面一样，在下面的代码中，make\_int() 的返回类型为 unique\_ptr&lt;int&gt;:

```cpp
unique_ptr<int> pup(make_int(rand() % 1000); // ok
shared_ptr<int> spp(pup);                 // not allowed, pup an lvalue
shared_ptr<int> spr(make_int(rand() % 1000); // ok
```

模板 shared\_ptr 包含一个显式构造函数，可用于将右值 unique\_ptr 转换为 shared\_ptr。shared\_ptr 将接管原来归 unique\_ptr 所有的对象。

在满足 unique\_ptr 要求的条件时，也可使用 auto\_ptr，但 unique\_ptr 是更好的选择。如果您的编译器没有提供 unique\_ptr，可考虑使用 BOOST 库提供的 scoped\_ptr，它与 unique\_ptr 类似。

## 16.3 标准模板库

STL 提供了一组表示容器、迭代器、函数对象和算法的模板。容器是一个与数组类似的单元，可以存储若干个值。STL 容器是同质的，即存储的值的类型相同；算法是完成特定任务（如对数组进行排序或在链表中查找特定值）的处方；迭代器能够用来遍历容器的对象，与能够遍历数组的指针类似，是广义指针；函数对象是类似于函数的对象，可以是类对象或函数指针（包括函数名，因为函数名被用作指针）。STL 使得能够构造各种容器（包括数组、队列和链表）和执行各种操作（包括搜索、排序和随机排列）。

Alex Stepanov 和 Meng Lee 在 Hewlett-Packard 实验室开发了 STL，并于 1994 年发布其实现。ISO/ANSI C++委员会投票同意将其作为 C++标准的组成部分。STL 不是面向对象的编程，而是一种不同的编程模式——泛型编程（generic programming）。这使得 STL 在功能和方法方面都很有趣。关于 STL 的信息很多，无法用一章的篇幅全部介绍，所以这里将介绍一些有代表性的例子，并领会泛型编程方法的精神。先来看几个具体的例子，让您对容器、迭代器和算法有一些感性的认识，然后再介绍底层的设计理念，并简要地介绍 STL。附录 G 对各种 STL 方法和函数进行了总结。

## 16.3.1 模板类 vector

第 4 章简要地介绍了 vector 类，下面更详细地介绍它。在计算中，矢量（vector）对应数组，而不是第 11 章介绍的数学矢量（在数学中，可以使用 N 个分量来表示 N 维数学矢量，因此从这方面讲，数学矢量类似一个 N 维数组。然而，数学矢量还有一些计算机矢量不具备的其他特征，如内乘积和外乘积）。计算矢量存储了一组可随机访问的值，即可以使用索引来直接访问矢量的第 10 个元素，而不必首先访问前面第 9 个元素。所以 vector 类提供了与第 14 章介绍的 valarray 和 ArrayTP 以及第 4 章介绍的 array 类似的操作，即可以创建 vector 对象，将一个 vector 对象赋给另一个对象，使用 [ ] 运算符来访问 vector 元素。要使类成为通用的，应将它设计为模板类，STL 正是这样做的——在头文件 vector（以前为 vector.h）中定义了一个 vector 模板。

要创建 vector 模板对象，可使用通常的&lt;type&gt;表示法来指出要使用的类型。另外，vector 模板使用动态内存分配，因此可以用初始化参数来指出需要多少矢量:

```cpp
#include vector
using namespace std;
vector<int> ratings(5);      // a vector of 5 ints
int n;
cin >> n;
vector<double> scores(n);     // a vector of n doubles
```

由于运算符[]被重载，因此创建 vector 对象后，可以使用通常的数组表示法来访问各个元素:

```txt
ratings[0] = 9;
for (int i = 0; i < n; i++)
    cout << scores[i] << endl;
```

## 分配器

与 string 类相似，各种 STL 容器模板都接受一个可选的模板参数，该参数指定使用哪个分配器对象来管理内存。例如，vector 模板的开头与下面类似:

```typescript
template <class T, class Allocator = allocator<T> >
    class vector {...
```

如果省略该模板参数的值，则容器模板将默认使用 allocator&lt;T&gt;类。这个类使用 new 和 delete。

程序清单 16.7 是一个要求不高的应用程序，它使用了这个类。该程序创建了两个 vector 对象——一个是 int 规范，另一个是 string 规范，它们都包含 5 个元素。

## 程序清单 16.7 vect1.cpp

```cpp
// vect1.cpp -- introducing the vector template
#include <iostream>
#include <string>
#include <vector>

const int NUM = 5;
int main()
{
    using std::vector;
    using std::string;
    using std::cin;
    using std::cout;
```

```txt
vector<int> ratings(NUM);
vector<string> titles(NUM);
cout << "You will do exactly as told. You will enter\n"
    << NUM << " book.titles and.your ratings_(0-10):\n";
int i;
for (i = 0; i < NUM; i++)
{
    cout << "Enter title.#"<< i + 1 << ": ";
    getline(cin,titles[i]);
    cout << "Enter your rating (0-10): ";
    cin >> ratings[i];
    cin.get();
}
cout << "Thank you: You entered the following:\n"
    << "Rating\tBook\n";
for (i = 0-i < NUM; i++)
{
    cout << ratings[i] << "\t" << titles[$] << endl;
}
return 0;
```

程序清单 16.7 中程序的运行情况如下:

```txt
You will do exactly as told. You will enter
5 book titles and your ratings (0-10).
Enter title #1: The Cat Who Knew C++
Enter your rating (0-10): 6
Enter title #2: Felonious Felines
Enter your rating (0-10): 4
Enter title #3: Warlords of Wonk
Enter your rating (0-10): 3
Enter title #4: Don't Touch That Metaphor
Enter your rating (0-10): 5
Enter title #5: Panic Oriented Programming
Enter your rating (0-10): 8
Thank you. You entered the following:
Rating Book
6 The Cat Who Knew C++
4 Felonious Felines
3 Warlords of Wonk
5 Don't Touch That Metaphor
8 Panic Oriented Programming
```

该程序使用 vector 模板只是为方便创建动态分配的数组。下一节将介绍一个使用更多类方法的例子。

## 16.3.2 可对矢量执行的操作

除分配存储空间外，vector 模板还可以完成哪些任务呢？所有的 STL 容器都提供了一些基本方法，其中包括 size()——返回容器中元素数目、swap()——交换两个容器的内容、begin()——返回一个指向容器中第一个元素的迭代器、end()——返回一个表示超过容器尾的迭代器。

什么是迭代器？它是一个广义指针。事实上，它可以是指针，也可以是一个可对其执行类似指针的操作——如解除引用（如 operator\*( )）和递增（如 operator++()）——的对象。稍后将知道，通过将指针广义化为迭代器，让STL能够为各种不同的容器类（包括那些简单指针无法处理的类）提供统一的接口。每个容器类都定义了一个合适的迭代器，该迭代器的类型是一个名为iterator的typedef，其作用域为整个类。例如，要为vector的double类型规范声明一个迭代器，可以这样做:

```cpp
vector<double>::iterator pd;  // pd an iterator
```

假设 scores 是一个 vector&lt;double&gt;对象:

```txt
vector<double> scores;
```

则可以使用迭代器pd执行这样的操作:

```txt
pd = scores.begin(); // have pd point to the first element
*pd = 22.3;          // dereference pd and assign value to first element
++pd;                  // make pd point to the next element.
```

正如您看到的，迭代器的行为就像指针。顺便说一句，还有一个C++11自动类型推断很有用的地方。例如，可以不这样做:

```txt
vector<double>::iterator pd = scores.begin();
```

而这样做:

```txt
auto pd = scores.begin() := // €++1I automatic-type deduction
```

回到前面的示例。什么是超过结尾（past-the-end）呢？它是一种迭代器，指向容器最后一个元素后面的那个元素。这与C-风格字符串最后一个字符后面的空字符类似，只是空字符是一个值，而“超过结尾”是一个指向元素的指针（迭代器）。end()成员函数标识超过结尾的位置。如果将迭代器设置为容器的第一个元素，并不断地递增，则最终它将到达容器结尾，从而遍历整个容器的内容。因此，如果scores和pd的定义与前面的示例中相同，则可以用下面的代码来显示容器的内容:

```txt
for (pd = scores.begin[] ; pd_! = _scores.end()-; pd++)
cout << *pd << endl;;
```

所有容器都包含刚才讨论的那些方法。vector 模板类也包含一些只有某些 STL 容器才有的方法。push\_back() 是一个方便的方法，它将元素添加到矢量末尾。这样做时，它将负责内存管理，增加矢量的长度，使之能够容纳新的成员。这意味着可以编写这样的代码:

```cpp
vector<double> scores; //- create an empty vector
double temp;
while (cin >> temp && temp >= 0)
    scores.push_back(temp);
cout << "You entered" << "scores.size().<< "scores.\n";
```

每次循环都给 scores 对象增加一个元素。在编写或运行程序时，无需了解元素的数目。只要能够取得足够的内存，程序就可以根据需要增加 scores 的长度。

erase()方法删除矢量中给定区间的元素。它接受两个迭代器参数，这些参数定义了要删除的区间。了解STL如何使用两个迭代器来定义区间至关重要。第一个迭代器指向区间的起始处，第二个迭代器位于区间终止处的后一个位置。例如，下述代码删除第一个和第二个元素，即删除begin()和begin()+1指向的元素（由于vector提供了随机访问功能，因此vector类迭代器定义了诸如begin()+2等操作）:

```javascript
scores.erase(scores.begin(), scores.begin(+[- + 2]);
```

如果 it1 和 it2 是迭代器，则 STL 文档使用[p1, p2]来表示从 p1 到 p2（不包括 p2）的区间。因此，区间[begin(), end()]将包括集合的所有内容（参见图 16.3），而区间[p1, p1]为空。[]表示法并不是 C++ 的组成部分，因此不能在代码中使用，而只能出现在文档中。

注意:区间[it1, it2)由迭代器it1和it2指定，其范围为it1到it2（不包括it2）。

insert()方法的功能与 erase()相反。它接受 3 个迭代器参数，第一个参数指定了新元素的插入位置，第二个和第三个迭代器参数定义了被插入区间，该区间通常是另一个容器对象的一部分。例如，下面的代码将矢量 new\_v 中除第一个元素外的所有元素插入到 old\_v 矢量的第一个元素前面:

```matlab
vector<int> old_v;
vector<int> new_v;
...
old_v.insert(old_v.begin(), new_v.begin() + 1, new_v.end());
```

![](images/page_695_image_3.jpg)

<details>
<summary>text_image</summary>

区间:
[things.begin(), things.end()]
2 4 7 1 8 5 9 6 3
100 104 108 112 116 120 124 128 132 136
things.begin()          things.end()
</details>

图 16.3 STL 的区间概念

顺便说一句，对于这种情况，拥有超尾元素是非常方便的，因为这使得在矢量尾部附加元素非常简单。下面的代码将新元素插入到 old.end()前面，即矢量最后一个元素的后面。

```javascript
old_v.insert(old_v.end(), new_v.begin() + 1, new_v.end());
```

程序清单 16.8 演示了 size()、begin()、end()、push\_back()、erase() 和 insert() 的用法。为简化数据处理，将程序清单 16.7 中的 rating 和 title 组合成了一个 Review 结构，并使用 FillReview() 和 ShowReview() 函数来输入和输出 Review 对象。

程序清单 16.8 vect2.cpp

```cpp
// vect2.cpp -- methods and iterators
#include <iostream>
#include <string>
#include <vector>

struct Review {
    std::string title;
    int rating;
};
bool FillReview(Review & rr);
void ShowReview(const Review & rr);

int main()
{
    using std::cout;
    using std::vector;
    vector<Review> books;
    Review temp;
    while {FillReview(temp))
```

```cpp
books.push_back(temp);
int num = books.size();
if (num > 0)
{
    cout << "Thank you. You entered the following:\n"
        << "Rating\tBook\n";
    for (int i = 0; i < num; i++)
        ShowReview(books[i]);
    cout << "Reprising:\n"
        << "Rating\tBook\n";
    vector<Review>::iterator pr;
    for (pr = books.begin(); pr != books.end(); pr++)
        ShowReview(*pr);
    vector <Review> oldlist(books);      // copy constructor used
    if (num > 3)
    {
        // remove 2 items
        books.erase(books.begin() + 1, books.begin() + 3);
        cout << "After erasure:\n";
        for (pr = books.begin(); pr != books.end(); pr++)
            ShowReview(*pr);
        // insert 1 item
        books.insert(books.begin(), oldlist.begin() + 1,
                oldlist.begin() + 2);
        cout << "After insertion:\n";
        for (pr = books.begin(); pr != books.end(); pr++)
            ShowReview(*pr);
    }
    books.swap(oldlist);
    cout << "Swapping oldlist with books:\n";
    for (pr = books.begin(); pr != books.end(); pr++)
        ShowReview(*pr);
}
else
    cout << "Nothing entered, nothing gained.\n";
return 0;
}

bool FillReview(Review & rr)
{
    std::cout << "Enter book title (quit to quit): ";
    std::getline(std::cin,rr.title);
    if (rr.title == "quit")
        return false;
    std::cout << "Enter book rating: ";
    std::cin >> rr.rating;
    if (!std::cin)
        return false;
    // get rid of rest of input line
    while (std::cin.get() != '\n')
        continue;
    return true;
}

void ShowReview(const Review & rr)
```

```cpp
{
    std::cout << rr.rating << "\t" << rr.title << std::endl;
}
```

程序清单16.8中程序的运行情况如下:

```txt
Enter book title (quit to quit): The Cat Who Knew Vectors
Enter book rating: 5
Enter book title (quit to quit): Candid Canines
Enter book rating: -7
Enter book title (quit to quit): Warriors of Wonk
Enter book rating: 4
Enter book title (quit to quit): Quantum Manners
Enter book rating: 8
Enter book title (quit to quit): quit
Thank you. You entered the following:
Rating Book
5 The Cat Who Knew Vectors
7 Candid Canines
4 Warriors of Wonk
8 Quantum Manners
Reprising:
Rating Book
5 The Cat Who Knew Vectors
7 Candid Canines
4 Warriors of Wonk
8 Quantum Manners
After erasure:
5 The Cat Who Knew Vectors_
8 Quantum Manners
After insertion:
7 Candid Canines
5 The Cat Who Knew Vectors
8 Quantum Manners
Swapping oldlist with books:
5 The Cat Who Knew Vectors_
7 Candid Canines
4 Warriors of Wonk
8 Quantum Manners
```

## 16.3.3 对矢量可执行的其他操作

程序员通常要对数组执行很多操作，如搜索、排序、随机排序等。矢量模板类包含了执行这些常见的操作的方法吗？没有！STL从更广泛的角度定义了非成员（non-member）函数来执行这些操作，即不是为每个容器类定义find()成员函数，而是定义了一个适用于所有容器类的非成员函数find()。这种设计理念省去了大量重复的工作。例如，假设有8个容器类，需要支持10种操作。如果每个类都有自己的成员函数，则需要定义80（8\*10）个成员函数。但采用STL方式时，只需要定义10个非成员函数即可。在定义新的容器类时，只要遵循正确的指导思想，则它也可以使用已有的10个非成员函数来执行查找、排序等操作。

另一方面，即使有执行相同任务的非成员函数，STL有时也会定义一个成员函数。这是因为对有些操作来说，类特定算法的效率比通用算法高，因此，vector的成员函数-swap()的效率比非成员函数-swap()高，但非成员函数让您能够交换两个类型不同的容器的内容。

下面来看 3 个具有代表性的 STL 函数:for\_each()、random\_shuffle() 和 sort()。for\_each() 函数可用于很多容器类，它接受 3 个参数。前两个是定义容器中区间的迭代器，最后一个是指向函数的指针（更普遍地说，最后一个参数是一个函数对象，函数对象将稍后介绍)。for\_each()函数将被指向的函数应用于容器区间中的各个元素。被指向的函数不能修改容器元素的值。可以用for\_each()函数来代替for循环。例如，可以将代码:

```txt
vector<Review>::iterator pr;
for (pr = books.begin(); pr != books.end(); pr++)
    ShowReview(*pr);
```

替换为:

```txt
for_each(books.begin(), books.end(), ShowReview);
```

这样可避免显式地使用迭代器变量。

Random\_shuffle()函数接受两个指定区间的迭代器参数，并随机排列该区间中的元素。例如，下面的语句随机排列 books 矢量中所有元素:

```javascript
random_shuffle(books.begin(), books.end());
```

与可用于任何容器类的 for\_each 不同，该函数要求容器类允许随机访问，\_vector 类可以做到这一点。

sort()函数也要求容器支持随机访问。该函数有两个版本，第一个版本接受两个定义区间的迭代器参数，并使用为存储在容器中的类型元素定义的<运算符，对区间中的元素进行操作。例如，下面的语句按升序对coolstuff的内容进行排序，排序时使用内置的<运算符对值进行比较:

```txt
vector<int> coolstuff;---
...
sort(coolstuff.begin(), coolstuff.end{});
```

如果容器元素是用户定义的对象，则要使用 sort()，必须定义能够处理该类型对象的 operator<()函数。例如，如果为 Review 提供了成员或非成员函数 operator<()，则可以对包含 Review 对象的矢量进行排序。由于 Review 是一个结构，因此其成员是公有的，这样的非成员函数将为:

```typescript
bool operator<(const Review & r1, const Review & r2)
{
    if (r1.title < r2.title)
        return true;
    else if (r1.title == r2.title && r1.rating < r2.rating)
        return true;
    else
        return false;
}
```

有了这样的函数后，就可以对包含 Review 对象（如 books）的矢量进行排序了:

```javascript
sort(books.begin(), books.end());
```

上述版本的 operator<()函数按 title 成员的字母顺序排序。如果 title 成员相同，则按照 rating 排序。然而，如果想按降序或是按 rating（而不是 title）排序，该如何办呢？可以使用另一种格式的 sort()。它接受 3 个参数，前两个参数也是指定区间的迭代器。最后一个参数是指向要使用的函数的指针（函数对象），而不是用于比较的 operator<()。返回值可转换为 bool，false 表示两个参数的顺序不正确。下面是一个例子:

```txt
bool WorseThan(const Review & r1, const Review.&.r2)
{
    if (r1.rating < r2.rating)
        return true;
    else
        return false;
}
```

有了这个函数后，就可以使用下面的语句将包含 Review 对象的 books 矢量按 rating 升序排列:

```javascript
sort(books.begin(), books.end(), WorseThan);
```

注意，与 operator<()相比，WorseThan()函数执行的对 Review 对象进行排序的工作不那么完整。如果两个对象的 title 成员相同，operator<()函数将按 rating 进行排序，而 WorseThan()将它们视为相同。第一种排序称为全排序（total ordering），第二种排序称为完整弱排序（strict weak ordering）。在全排序中，如果 a<b 和 b<a 都不成立，则 a 和 b 必定相同。在完整弱排序中，情况就不是这样了。它们可能相同，也可能只是在某方面相同，如 WorseThan()示例中的 rating 成员。所以在完整弱排序中，只能说它们等价，而不是相同。

程序清单 16.9 演示了这些 STL 函数的用法。

程序清单 16.9 vect3.cpp

```cpp
// vect3.cpp -- using STL functions
#include <iostream>
#include <string>
#include <vector>
#include <algorithm>

struct Review {
    std::string title;
    int rating;
};

bool operator<(const Review & r1, const Review & r2);
bool worseThan(const Review & r1, const Review & r2);
bool FillReview(Review & rr);
void ShowReview(const Review & rr);
int main()
{
    using namespace std;

    vector<Review> books;
    Review temp;
    while (FillReview(temp))
        books.push_back(temp);
    if (books.size() > 0)
    {
        cout << "Thank you. You entered the following "
            << books.size() << " ratings:\n"
            << "Rating\tBook\n";
        for_each(books.begin(), books.end(), ShowReview);

        sort(books.begin(), books.end());
        cout << "Sorted by title:\nRating\tBook\n";
        for_each(books.begin(), books.end(), ShowReview);

        sort(books.begin(), books.end(), worseThan);
        cout << "Sorted by rating:\nRating\tBook\n";
        for_each(books.begin(), books.end(), ShowReview);

        random_shuffle(books.begin(), books.end());
        cout << "After shuffling:\nRating\tBook\n";
        for_each(books.begin(), books.end(), ShowReview);
    }
    else
        cout << "No entries. ";
```

```cpp
cout << "Bye.\n";
    return 0;
}

bool operator<(const Review & r1, const Review & r2)
{
    if (r1.title < r2.title)
        return true;
    else if (r1.title == r2.title && r1.rating < r2.rating)
        return true;
    else
        return false;
}

bool worseThan(const Review & r1, const Review & r2)
{
    if (r1.rating < r2.rating)
        return true;
    else
        return false;
}

bool FillReview(Review & rr)
{
    std::cout << "Enter book title (quit to quit): ";
    std::getline(std::cin,rr.title);
    if (rr.title == "quit")
        return false;
    std::cout << "Enter book rating: ";
    std::cin >> rr.rating;
    if (!std::cin)
        return false;
    // get rid of rest of input line
    while (std::cin.get() != '\n')
        continue;
    return true;
}

void ShowReview(const Review & rr)
{
    std::cout << rr.rating << "\t" << rr.title << std::endl;
}
```

程序清单 16.9 中程序的运行情况如下:

```txt
Enter book title (quit to quit): The Cat Who Can Teach You Weight Loss
Enter book rating: 8
Enter book title (quit to quit): The Dogs of Dharma
Enter book rating: 6
Enter book title (quit to quit): The Wimps of Wonk
Enter book rating: 3
Enter book title (quit to quit): Farewell and Delete
Enter book rating: 7
Enter book title (quit to quit): quit
Thank you. You entered the following 4 ratings:
Rating Book
```

```txt
8 The Cat Who Can Teach You Weight Loss
6 The Dogs of Dharma
3 The Wimps of Wonk
7 Farewell and Delete
Sorted by title:
Rating Book
7 Farewell and Delete
8 The Cat Who Can Teach You Weight Loss
6 The Dogs of Dharma
3 The Wimps of Wonk
Sorted by rating:
Rating Book
3 The Wimps of Wonk
6 The Dogs of Dharma
7 Farewell and Delete
8 The Cat Who Can Teach You Weight Loss
After shuffling:
Rating Book
7 Farewell and Delete
3 The Wimps of Wonk
6 The Dogs of Dharma
8 The Cat Who Can Teach You Weight Loss
Bye.
```

## 16.3.4 基于范围的 for 循环（C++11）

第5章说过，基于范围的for循环是为用于STL而设计的。为复习该循环，下面是第5章的第一个示例:

```txt
double prices[5] = {4.99, 10.99, 6.87, 7.99, 8.49};
for (double x : prices)
    cout << x << std::endl;
```

在这种 for 循环中，括号内的代码声明一个类型与容器存储的内容相同的变量，然后指出了容器的名称。接下来，循环体使用指定的变量依次访问容器的每个元素。例如，对于下述摘自程序清单 16.9 的语句:

```txt
for_each(books.begin(), books.end(), ShowReview);
```

可将其替换为下述基于范围的 for 循环:

```txt
for (auto x : books) ShowReview(x);
```

根据 book 的类型（vector&lt;Review&gt;），编译器将推断出 x 的类型为 Review，而循环将依次将 books 中的每个 Review 对象传递给 ShowReview()。

不同于 for\_each()，基于范围的 for 循环可修改容器的内容，诀窍是指定一个引用参数。例如，假设有如下函数:

```javascript
void InflateReview(Review &r){r.rating++;}
```

可使用如下循环对 books 的每个元素执行该函数:

```typescript
for (auto & x: books) InflateReview(x);
```

## 16.4 泛型编程

有了一些使用 STL 的经验后，来看一看底层理念。STL 是一种泛型编程（generic programming）。面向对象编程关注的是编程的数据方面，而泛型编程关注的是算法。它们之间的共同点是抽象和创建可重用代码，但它们的理念绝然不同。

泛型编程旨在编写独立于数据类型的代码。在 C++ 中，完成通用程序的工具是模板。当然，模板使得能够按泛型定义函数或类，而 STL 通过通用算法更进了一步。模板让这一切成为可能，但必须对元素进行仔细地设计。为解模板和设计是如何协同工作的，来看一看需要迭代器的原因。

## 16.4.1 为何使用迭代器

理解迭代器是理解 STL 的关键所在。模板使得算法独立于存储的数据类型，而迭代器使算法独立于使用的容器类型。因此，它们都是 STL 通用方法的重要组成部分。

为了解为何需要迭代器，我们来看如何为两种不同数据表示实现 find 函数，然后来看如何推广这种方法。首先看一个在 double 数组中搜索特定值的函数，可以这样编写该函数:

```cpp
double * find_ar(double * ar, int nF const double & val)
{
    for (int i = 0; F < n; i++)
        if (ar[i] == val)
            return &ar[i];
    return 0; // orF in C++11, return nullptr;
}
```

如果函数在数组中找到这样的值，则返回该值在数组中的地址，否则返回一个空指针。该函数使用下标来遍历数组。可以用模板将这种算法推广到包含 $=$ =运算符的、任意类型的数组。尽管如此，这种算法仍然与一种特定的数据结构（数组）关联在一起。

下面来看搜索另一种数据结构——链表的情况（第 12 章使用链表实现了 Queue 类）。链表由链接在一起的 Node 结构组成:

```txt
struct Node
{
    double item;
    Node * p_next;
};
```

假设有一个指向链表第一个节点的指针，每个节点的 p\_next 指链都指向下一个节点，链表最后一个节点的 p\_next 指针被设置为 0，则可以这样编写 find\_ll() 函数:

```c
Node* find_ll(Node * head, const double & val)
{
    Node * start;
    for (start = head; start!= 0; start = start->p_next)
        if (start->item == val)
            return start;
    return 0;
}
```

同样，也可以使用模板将这种算法推广到支持==运算符的任何数据类型的链表。然而，这种算法也是与特定的数据结构——链表关联在一起。

从实现细节上看，这两个 find 函数的算法是不同的:一个使用数组索引来遍历元素，另一个则将 start 重置为 start->p\_next。但从广义上说，这两种算法是相同的:将值依次与容器中的每个值进行比较，直到找到匹配的为止。

泛型编程旨在使用同一个 find 函数来处理数组、链表或任何其他容器类型。即函数不仅独立于容器中存储的数据类型，而且独立于容器本身的数据结构。模板提供了存储在容器中的数据类型的通用表示，因此还需要遍历容器中的值的通用表示，迭代器正是这样的通用表示。

要实现 find 函数，迭代器应具备哪些特征呢？下面是一个简短的列表。

- 应能够对迭代器执行解除引用的操作，以便能够访问它引用的值。即如果 $p$ 是一个迭代器，则应对\* $p$ 进行定义。
- 应能够将一个迭代器赋给另一个。即如果 $p$ 和 $q$ 都是迭代器，则应对表达式 $p = q$ 进行定义。
- 应能够将一个迭代器与另一个进行比较，看它们是否相等。即如果 p 和 q 都是迭代器，则应对 p==q 和 p!=q 进行定义。
- 应能够使用迭代器遍历容器中的所有元素，这可以通过为迭代器 p 定义++p 和 p++来实现。

迭代器也可以完成其他的操作，但有上述功能就足够了，至少对于 find 函数是如此。实际上，STL 按功能的强弱定义了多种级别的迭代器，这将在后面介绍。顺便说一句，常规指针就能满足迭代器的要求，因此，可以这样重新编写 find\_arr()函数:

```c
typedef double * iterator;
iterator-find_ar(iterator ar, int n, const double & val)
{
    for (int i = 0; i < n; i++, ar++)
        if (*ar == val)
            return ar;
    return 0;
}
```

然后可以修改函数参数，使之接受两个指示区间的指针参数，其中的一个指向数组的起始位置，另一个指向数组的超尾（程序清单7.8与此类似）；同时函数可以通过返回尾指针，来指出没有找到要找的值。下面的find\_ar()版本完成了这些修改:

```c
typedef double * iterator;
iterator find_ar(iterator begin, iterator end, const double & val)
{
    iterator ar;
    for (ar = begin; ar != end; ar++)
        if (*ar == val)
            return ar;
    return end; // indicates val not found
}
```

对于 find\_ll()函数，可以定义一个迭代器类，其中定义了运算符\*和++:

```cpp
struct Node
{
    double item;
    Node * p_next;
};

class iterator
{
    Node * pt;
public:
    iterator()- : pt(0) {}
    iterator (Node * pn) : pt(pn) {}
    double operator*(=){ return pt->item;}
    iterator& operator++()=      // for ++it
    {
        pt =pt->p_next; _
        return *this;
    }
    iterator operator++(int)  // for it++
    {
```