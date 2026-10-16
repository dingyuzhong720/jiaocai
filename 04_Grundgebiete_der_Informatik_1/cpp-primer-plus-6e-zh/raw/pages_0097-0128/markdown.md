程序清单 4.4 将程序清单 4.3 修改为使用 cin.getline()，而不是简单的 cin。除此之外，该程序没有做其他修改。

程序清单 4.4 instr2.cpp

```cpp
// instr2.cpp -- reading more than one word with getline
#include <iostream>
int main()
{
    using namespace std;
    const int ArSize = 20;
    char name[ArSize];
    char dessert[ArSize];

    cout << "Enter your name:\n";
    cin.getline(name, ArSize);  // reads through newline
    cout << "Enter your favorite dessert:\n";
    cin.getline(dessert, ArSize);
    cout << "I have some delicious " << dessert;
    cout << " for you, " << name << ".\n";
    return 0;
}
```

下面是该程序的输出:

```txt
Enter your name:
Dirk Hammernose
Enter your favorite dessert:
Radish Torte
I have some delicious Radish Torte for you, Dirk Hammernose.
```

该程序现在可以读取完整的姓名以及用户喜欢的甜点！getline()函数每次读取一行。它通过换行符来确定行尾，但不保存换行符。相反，在存储字符串时，它用空字符来替换换行符（参见图4.5）。

![](images/page_96_image_8.jpg)

<details>
<summary>text_image</summary>

代码:
char name[10];
cout << "Enter your name: ";
cin.getline(name, 10);

用户键入Jud来作出响应，然后按下 ENTER

Enter your name: Jud ENTER

cin.getline()读取“Jud”以及用户
按Enter键而生成的换行符，并将换行
符替换为空字符

J u d \0 
换行符被替换为空字符
</details>

图 4.5 getline()读取并替换换行符

## 2. 面向行的输入:get()

我们来试试另一种方法。istream 类有另一个名为 get() 的成员函数，该函数有几种变体。其中一种变体的工作方式与 getline() 类似，它们接受的参数相同，解释参数的方式也相同，并且都读取到行尾。但 get 并不再读取并丢弃换行符，而是将其留在输入队列中。假设我们连续两次调用 get():

```rust
cin.get(name, ArSize);
cin.get(dessert, Arsize);   // a problem
```

由于第一次调用后，换行符将留在输入队列中，因此第二次调用时看到的第一个字符便是换行符。因此 get() 认为已到达行尾，而没有发现任何可读取的内容。如果不借助于帮助，get() 将不能跨过该换行符。

幸运的是，get()有另一种变体。使用不带任何参数的cin.get()调用可读取下一个字符（即使是换行符），因此可以用它来处理换行符，为读取下一行输入做好准备。也就是说，可以采用下面的调用序列:

```cpp
cin.get(name, ArSize);      // read first line
cin.get();                          // read newline
cin.get(dessert, Arsize);   // read second line
```

另一种使用 get() 的方式是将两个类成员函数拼接起来（合并），如下所示:

```javascript
cin.get(name, ArSize).get(); // concatenate member functions
```

之所以可以这样做，是由于 cin.get(name, ArSize) 返回一个 cin 对象，该对象随后将被用来调用 get() 函数。同样，下面的语句将把输入中连续的两行分别读入到数组 name1 和 name2 中，其效果与两次调用 cin.getline() 相同:

```javascript
cin.getline(name1, ArSize).getline(name2, ArSize);
```

程序清单 4.5 采用了拼接方式。第 11 章将介绍如何在类定义中使用这项特性。

程序清单 4.5 instr3.cpp

```cpp
// instr3.cpp -- reading more than one word with get() & get()
#include <iostream>
int main()
{
    using namespace std;
    const int ArSize = 20;
    char name[ArSize];
    char dessert[ArSize];

    cout << "Enter your name:\n";
    cin.get(name, ArSize).get();      // read string, newline
    cout << "Enter your favorite dessert:\n";
    cin.get(dessert, ArSize).get();
    cout << "I have some delicious " << dessert;
    cout << " for you, " << name << ".\n";
    return 0;
}
```

下面是程序清单 4.5 中程序的运行情况:

```txt
Enter your name:
Mai Parfait
Enter your favorite dessert:
Chocolate Mousse
I have some delicious Chocolate Mousse for you, Mai Parfait.
```

需要指出的一点是，C++允许函数有多个版本，条件是这些版本的参数列表不同。如果使用的是 cin.get（name，ArSize），则编译器知道是要将一个字符串放入数组中，因而将使用适当的成员函数。如果使用的是 cin.get()，则编译器知道是要读取一个字符。第 8 章将探索这种特性——函数重载。

为什么要使用 get()，而不是 getline()呢？首先，老式实现没有 getline()。其次，get()使输入更仔细。例如，假设用 get()将一行读入数组中。如何知道停止读取的原因是由于已经读取了整行，而不是由于数组已填满呢？查看下一个输入字符，如果是换行符，说明已读取了整行；否则，说明该行中还有其他输入。第 17 章将介绍这种技术。总之，getline()使用起来简单一些，但 get()使得检查错误更简单些。可以用其中的任何一个来读取一行输入；只是应该知道，它们的行为稍有不同。

## 3. 空行和其他问题

当 getline() 或 get() 读取空行时, 将发生什么情况? 最初的做法是, 下一条输入语句将在前一条 getline() 或 get() 结束读取的位置开始读取; 但当前的做法是, 当 get() (不是 getline()) 读取空行后将设置失效位 (failbit)。这意味着接下来的输入将被阻断, 但可以用下面的命令来恢复输入:

```javascript
cin.clear();
```

另一个潜在的问题是，输入字符串可能比分配的空间长。如果输入行包含的字符数比指定的多，则getline()和get()将把余下的字符留在输入队列中，而getline()还会设置失效位，并关闭后面的输入。

第 5、6 章和第 17 章将介绍这些属性，并探讨程序如何避免这些问题。

## 4.2.5 混合输入字符串和数字

混合输入数字和面向行的字符串会导致问题。请看程序清单 4.6 中的简单程序。

程序清单 4.6 numstr.cpp

```cpp
// numstr.cpp -- following number input with line input
#include <iostream>
int main()
{
    using namespace std;
    cout << "What year was your house built?\n";
    int year;
    cin >> year;
    cout << "What is its street address?\n";
    char address[80];
    cin.getline(address, 80);
    cout << "Year built: " << year << endl;
    cout << "Address: " << address << endl;
    cout << "Done!\n";
    return 0;
}
```

该程序的运行情况如下:

```txt
What year was your house built?
1966
What is its street address?
Year built: 1966
Address
Done!
```

用户根本没有输入地址的机会。问题在于，当 cin 读取年份，将回车键生成的换行符留在了输入队列中。后面的 cin.getline() 看到换行符后，将认为是一个空行，并将一个空字符串赋给 address 数组。解决之道是，在读取地址之前先读取并丢弃换行符。这可以通过几种方法来完成，其中包括使用没有参数的 get() 和使用接受一个 char 参数的 get()，如前面的例子所示。可以单独进行调用:

```txt
cin >> year;
cin.get();   // or cin.get(ch);
```

也可以利用表达式 cin>>year 返回 cin 对象，将调用拼接起来:

```txt
(cin >> year).get();  // or (cin >> year).get(ch);
```

按上述任何一种方法修改程序清单 4.6 后，它便可以正常工作:

```txt
What year was your house built?
1966
What is its street address?
43821 Unsigned Short Street
Year built: 1966
Address: 43821 Unsigned Short Street
Done!
```

C++程序常使用指针（而不是数组）来处理字符串。我们将在介绍指针后，再介绍字符串这个方面的特性。下面介绍一种较新的处理字符串的方式:C++ string 类。

## 4.3 string 类简介

ISO/ANSI C++98 标准通过添加 string 类扩展了 C++ 库，因此现在可以 string 类型的变量（使用 C++ 的话说是对象）而不是字符数组来存储字符串。您将看到，string 类使用起来比数组简单，同时提供了将字符串作为一种数据类型的表示方法。

要使用 string 类，必须在程序中包含头文件 string。string 类位于名称空间 std 中，因此您必须提供一条 using 编译指令，或者使用 std::string 来引用它。string 类定义隐藏了字符串的数组性质，让您能够像处理普通变量那样处理字符串。程序清单 4.7 说明了 string 对象与字符数组之间的一些相同点和不同点。

程序清单 4.7 strtype1.cpp

```cpp
// strtype1.cpp -- using the C++ string class
#include <iostream>
#include <string>                 // make string class available
int main()
{
    using namespace std;
    char charr1[20];            // create an empty array
    char charr2[20] = "jaguar"; // create an initialized array
    string str1;                    // create an empty string object
    string str2 = "panther";   // create an initialized string

    cout << "Enter a kind of feline: ";
    cin >> charr1;
    cout << "Enter another kind of feline: ";
    cin >> str1;                // use cin for input
    cout << "Here are some felines:\n";
    cout << charr1 << " " << charr2 << " "
        << str1 << " " << str2 // use cout for output
        << endl;
    cout << "The third letter in " << charr2 << " is "
        << charr2[2] << endl;
    cout << "The third letter in " << str2 << " is "
        << str2[2] << endl;   // use array notation

    return 0;
}
```

下面是该程序的运行情况:

```txt
Enter a kind of feline: ocelot
Enter another kind of feline: tiger
Here are some felines:
ocelot jaguar tiger panther
The third letter in jaguar is g
The third letter in panther is n
```

从这个示例可知，在很多方面，使用 string 对象的方式与使用字符数组相同。

- 可以使用 C-风格字符串来初始化 string 对象。
- 可以使用 cin 来将键盘输入存储到 string 对象中。
- 可以使用cout来显示string对象。
- 可以使用数组表示法来访问存储在 string 对象中的字符。

程序清单 4.7 表明，string 对象和字符数组之间的主要区别是，可以将 string 对象声明为简单变量，而不是数组:

```txt
string str1;          // create an empty string object
string str2 = "panther";    // create an initialized string
```

类设计让程序能够自动处理 string 的大小。例如，str1 的声明创建一个长度为 0 的 string 对象，但程序将输入读取到 str1 中时，将自动调整 str1 的长度:

```txt
cin >> str1;          // str1 resized to fit input
```

这使得与使用数组相比，使用 string 对象更方便，也更安全。从理论上说，可以将 char 数组视为一组用于存储一个字符串的 char 存储单元，而 string 类变量是一个表示字符串的实体。

## 4.3.1 C++11 字符串初始化

正如您预期的，C++11也允许将列表初始化用于C-风格字符串和string对象:

```txt
char first_date[] = {"Le Chapon Dodu"};
char second_date[] {"The Elegant Plate"};
string third_date = {"The Bread Bowl"};
string fourth_date {"Hank's Fine Eats"};
```

## 4.3.2 赋值、拼接和附加

使用 string 类时，某些操作比使用数组时更简单。例如，不能将一个数组赋给另一个数组，但可以将一个 string 对象赋给另一个 string 对象:

```c
char charr1[20];          // create an empty array
char charr2[20] = "jaguar"; // create an initialized-array
string str1;               // create an empty string object
string str2 = "panther";    // create an initialized string
charr1= charr2;              // INVALID, no array assignment
str1 = str2;                 // VALID_object assignment ok
```

string 类简化了字符串合并操作。可以使用运算符+将两个 string 对象合并起来，还可以使用运算符+=将字符串附加到 string 对象的末尾。继续前面的代码，您可以这样做:

```c
string str3;
str3 = str1 + str2;          // assign str3 the joined strings
strF += str2;              // add str2 to the end of str1
```

程序清单 4.8 演示了这些用法。可以将 C-风格字符串或 string 对象与 string 对象相加，或将它们附加到 string 对象的末尾。

程序清单 4.8 strtype2.cpp

```cpp
// strtype2.cpp -- assigning, adding, and appending
#include <iostream>
#include <string>          // make string class available
int main()
{
    using namespace std;
    string s1 = "penguin";
    string s2, s3;

    cout << "You can assign one string object to another: s2 = s1\n";
    s2 = s1;
    cout << "s1: " << s1 << ", s2: " << s2 << endl;
    cout << "You can assign a C-style string to a string object.\n";
    cout << "s2 = \"buzzard\"\n";
    s2 = "buzzard";
    cout << "s2: " << s2 << endl;
    cout << "You can concatenate strings: s3 = s1 + s2\n";
    s3 = s1 + s2;
    cout << "s3: " << s3 << endl;
    cout << "You can append strings.\n";
    s1 += s2;
    cout <<"s1 += s2 yields s1 = " << s1 << endl;
    s2 += " for a day";
    cout <<"s2 += \" for a day\" yields s2 = " << s2 << endl;

    return 0;
}
```

转义序列"表示双引号，而不是字符串结尾。该程序的输出如下:

```txt
You can assign one string object to another: s2 = s1
s1: penguin, s2: penguin
You can assign a C-style string to a string object.
s2 = "buzzard"
s2: buzzard
You can concatenate strings: s3 = s1 + s2
s3: penguinbuzzard
You can append strings.
s1 += s2 yields s1 = penguinbuzzard
s2 += " for a day" yields s2 = buzzard for a day
```

## 4.3.3 string 类的其他操作

在 C++新增 string 类之前，程序员也需要完成诸如给字符串赋值等工作。对于 C-风格字符串，程序员使用 C 语言库中的函数来完成这些任务。头文件 cstring（以前为 string.h）提供了这些函数。例如，可以使用函数 strcpy() 将字符串复制到字符数组中，使用函数 strcat() 将字符串附加到字符数组末尾；

```c
strcpy(charr1, charr2); // copy charr2 to charr1
strcat(charr1, charr2); // append contents of charr2 to char1
```

程序清单 4.9 对用于 string 对象的技术和用于字符数组的技术进行了比较。

程序清单 4.9 strtype3.cpp

```cpp
// strtype3.cpp -- more string class features
#include <iostream>
#include <string>          // make string class available
#include <cstring>          // C-style string library
int main()
{
    using namespace std;
    char charr1[20];
    char charr2[20] = "jaguar";
    string str1;
    string str2 = "panther";

    // assignment for string objects and character arrays
    str1 = str2;           // copy str2 to str1
    strcpy(charr1, charr2);   // copy charr2 to charr1

    // appending for string objects and character arrays
    str1 += " paste";       // add paste to end of str1
    strcat(charr1, "_juice");  // add juice to end of charr1

    // finding the length of a string object and a C-style string
    int len1 = str1.size();     // obtain length of str1
    int len2 = strlen(charr1);  // obtain length of charr1

    cout << "The string " << str1 << " contains "
        << Ieni << " characters.\n";
    cout << "The string " << charr1 << " contains "
        << Ien2 << "- characters.\n";

    return 0;
}
```

下面是该程序的输出:

```txt
The string panther paste contains 13 characters.
The string jaguar juice contains 12 characters.
```

处理 string 对象的语法通常比使用 C 字符串函数简单，尤其是执行较为复杂的操作时。例如，对于下述操作:

```txt
str3 = str1 + str2;
```

使用 C-风格字符串时，需要使用的函数如下:

```txt
strcpy(charr3, charr1);
strcat(charr3, charr2);
```

另外，使用字符数组时，总是存在目标数组过小，无法存储指定信息的危险，如下面的示例所示:

```javascript
char site[10] = "house";
strcat(site, " of pancakes"); // memory problem
```

函数 strcat()试图将全部 12 个字符复制到数组 site 中，这将覆盖相邻的内存。这可能导致程序终止，或者程序继续运行，但数据被损坏。string 类具有自动调整大小的功能，从而能够避免这种问题发生。C 函数库确实提供了与 strcat() 和 strcpy() 类似的函数——strncat() 和 strncpy()，它们接受指出目标数组最大允许长度的第三个参数，因此更为安全，但使用它们进一步增加了编写程序的复杂度。

下面是两种确定字符串中字符数的方法:

```txt
int len1 = str1.size();      // obtain length of str1
int len2 = strLen(charr1);   // obtain length of charr1
```

函数 strlen() 是一个常规函数，它接受一个 C-风格字符串作为参数，并返回该字符串包含的字符数。函数 size() 的功能基本上与此相同，但句法不同:str1 不是被用作函数参数，而是位于函数名之前，它们之间用句点连接。与第 3 章介绍的 put() 方法相同，这种句法表明，str1 是一个对象，而 size() 是一个类方法。方法是一个函数，只能通过其所属类的对象进行调用。在这里，str1 是一个 string 对象，而 size() 是 string 类的一个方法。总之，C 函数使用参数来指出要使用哪个字符串，而 C++ string 类对象使用对象名和句点运算符来指出要使用哪个字符串。

## 4.3.4 string 类 I/O

正如您知道的，可以使用 cin 和运算符<<来将输入存储到 string 对象中，使用 cout 和运算符<<来显示 string 对象，其句法与处理 C-风格字符串相同。但每次读取一行而不是一个单词时，使用的句法不同，程序清单 4.10 说明了这一点。

程序清单 4.10 strtype4.cpp

```cpp
// strtype4.cpp -- line input
#include <iostream>
#include <string>                 // make string class available
#include <cstring>                 // C-style string library
int main()
{
    using namespace std;
    char charr[20];
    string str;

    cout << "Length of string in charr before input: "
        << strlen(charr) << endl;
    cout << "Length of string in str before input: "
        << str.size() << endl;
    cout << "Enter a line of text:\n";
    cin.getline(charr, 20);      // indicate maximum length
    cout << "You entered: " << charr << endl;
    cout << "Enter another line of text:\n";
    getline(cin, str);          // cin now an argument; no length specifier
    cout << "You entered: " << str << endl;
    cout << "Length of string in charr after input: "
        << strlen(charr) << endl;
    cout << "Length of string in str after input: "
        << str.size() << endl;

    return 0;
}
```

下面是一个运行该程序时的输出示例:

```txt
Length of string in charr before input: 27
Length of string in str before input: 0
Enter a line of text:
peanut butter
You entered: peanut butter
Enter another line of text:
blueberry jam
You entered: blueberry jam
Length of string in charr after input: 13
Length of string in str after input: 13
```

在用户输入之前，该程序指出数组 charr 中的字符串长度为 27，这比该数组的长度要大。这里要两点需要说明。首先，为初始化的数组的内容是未定义的；其次，函数 strlen() 从数组的第一个元素开始计算字节数，直到遇到空字符。在这个例子中，在数组末尾的几个字节后才遇到空字符。对于未被初始化的数据，第一个空字符的出现位置是随机的，因此您在运行该程序时，得到的数组长度很可能与此不同。

另外，用户输入之前，str 中的字符串长度为 0。这是因为未被初始化的 string 对象的长度被自动设置为 0。

下面是将一行输入读取到数组中的代码:

```javascript
cin.getline(charr, 20);
```

这种句点表示法表明，函数 getline() 是 istream 类的一个类方法（还记得吗，cin 是一个 istream 对象）。正如前面指出的，第一个参数是目标数组；第二个参数数组长度，getline() 使用它来避免超越数组的边界。

下面是将一行输入读取到 string 对象中的代码:

```javascript
getline(cin,str);
```

这里没有使用句点表示法，这表明这个 getline()不是类方法。它将 cin 作为参数，指出到哪里去查找输入。另外，也没有指出字符串长度的参数，因为 string 对象将根据字符串的长度自动调整自己的大小。

那么，为何一个 getline() 是 istream 的类方法，而另一个不是呢？在引入 string 类之前很久，C++ 就有 istream 类。因此 istream 的设计考虑到了诸如 double 和 int 等基本 C++ 数据类型，但没有考虑 string 类型，所以 istream 类中，有处理 double、int 和其他基本类型的类方法，但没有处理 string 对象的类方法。

由于 istream 类中没有处理 string 对象的类方法，因此您可能会问，下述代码为何可行呢？

```txt
cin >> str; // read a word into the str string object
```

像下面这样的代码使用 istream 类的一个成员函数:

```txt
cin >> x; // read a value into a basic C++ type
```

但前面处理 string 对象的代码使用 string 类的一个友元函数。有关友元函数及这种技术为何可行，将在第 11 章介绍。另外，您可以将 cin 和 cout 用于 string 对象，而不用考虑其内部工作原理。

## 4.3.5 其他形式的字符串字面值

本书前面说过，除 char 类型外，C++ 还有类型 wchar\_t；而 C++1新增了类型 char16\_t 和 char32\_t。可创建这些类型的数组和这些类型的字符串字面值。对于这些类型的字符串字面值，C++ 分别使用前缀 L、u 和 U 表示，下面是一个如何使用这些前缀的例子:

```txt
wchar_t.title[] = L"Chief Astrogator"; // w_char string
char16_t name[] = u"Felonia Ripova"; // char_16 string
char32_t car[] = U"Humber Super Snipe"; // char_32 string
```

C++11. 还支持 Unicode 字符编码方案 UTF-8。在这种方案中，根据编码的数字值，字符可能存储为 1\~4 个八位组。C++ 使用前缀 u8 来表示这种类型的字符串字面值。

C++11 新增的另一种类型是原始（raw）字符串。在原始字符串中，字符表示的就是自己，例如，序列 \n 不表示换行符，而表示两个常规字符——斜杠和 n，因此在屏幕上显示时，将显示这两个字符。另一个例子是，可在字符串中使用"，而无需像程序清单 4.8 中那样使用繁琐的"。当然，既然可在字符串字面量包含"，就不能再使用它来表示字符串的开头和末尾。因此，原始字符串将"(和)"用作定界符，并使用前缀 R 来标识原始字符串:

```txt
cout << R"(Jim "King" Tutt -uses"\n" instead of endl.")"< < '\n';
```

上述代码将显示如下内容:

```txt
Jim "King" Tutt uses \n instead of endl.
```

如果使用标准字符串字面值，将需编写如下代码:

```txt
cout << "Jim \"King\" Tutt uses \" \\n\" instead of endl." << '\\n!;
```

在上述代码中，使用了\来显示\，因为单个\表示转义序列的第一个字符。

输入原始字符串时，按回车键不仅会移到下一行，还将在原始字符串中添加回车字符。

如果要在原始字符串中包含)$^{n}$，该如何办呢？编译器见到第一个)$^{n}$时，会不会认为字符串到此结束？会的。但原始字符串语法允许您在表示字符串开头的“和(之间添加其他字符，这意味着表示字符串结尾的”和）之间也必须包含这些字符。因此，使用 R"$^{n}$+\*(标识原始字符串的开头时，必须使用)$^{n}$+\*$^{n}$标识原始字符串的结尾。因此，下面的语句:

```javascript
cout << R"+*("(Who wouldn't?)", she whispered.)+*" << endl;
```

将显示如下内容:

```txt
"(Who wouldn't?)", she whispered.
```

总之，这使用"+\*(和)+\*"替代了默认定界符"(和)”。自定义定界符时，在默认定界符之间添加任意数量的基本字符，但空格、左括号、右括号、斜杠和控制字符（如制表符和换行符）除外。

可将前缀 R 与其他字符串前缀结合使用，以标识 wchar\_t 等类型的原始字符串。可将 R 放在前面，也可将其放在后面，如 Ru、UR 等。

下面介绍另一种复合类型——结构。

## 4.4 结构简介

假设要存储有关篮球运动员的信息，则可能需要存储他（她）的姓名、工资、身高、体重、平均得分、命中率、助攻次数等。希望有一种数据格式可以将所有这些信息存储在一个单元中。数组不能完成这项任务，因为虽然数组可以存储多个元素，但所有元素的类型必须相同。也就是说，一个数组可以存储20个int，另一个数组可以存储10个float，但同一个数组不能在一些元素中存储int，在另一些元素中存储float。

C++中的结构的可以满足要求（存储篮球运动员的信息）。结构是一种比数组更灵活的数据格式，因为同一个结构可以存储多种类型的数据，这使得能够将有关篮球运动员的信息放在一个结构中，从而将数据的表示合并到一起。如果要跟踪整个球队，则可以使用结构数组。结构也是 C++ OOP 堡垒（类）的基石。学习有关结构的知识将使我们离 C++ 的核心 OOP 更近。

结构是用户定义的类型，而结构声明定义了这种类型的数据属性。定义了类型后，便可以创建这种类型的变量。因此创建结构包括两步。首先，定义结构描述——它描述并标记了能够存储在结构中的各种数据类型。然后按描述创建结构变量（结构数据对象）。

例如，假设 Bloataire 公司要创建一种类型来描述其生产线上充气产品的成员。具体地说，这种类型应存储产品名称、容量（单位为立方英尺）和售价。下面的结构描述能够满足这些要求:

```txt
struct inflatable  // structure declaration
{
    char name[20];
    float volume;
    double price;
};
```

关键字 struct 表明，这些代码定义的是一个结构的布局。标识符 inflatable 是这种数据格式的名称，因

此新类型的名称为 inflatable。这样，便可以像创建 char 或 int 类型的变量那样创建 inflatable 类型的变量了。接下来的大括号中包含的是结构存储的数据类型的列表，其中每个列表项都是一条声明语句。这个例子使用了一个适合用于存储字符串的 char 数组、一个 float 和一个 double。列表中的每一项都被称为结构成员，因此 inflatable 结构有 3 个成员（参见图 4.6）。总之，结构定义指出了新类型（这里是 inflatable）的特征。

![](images/page_105_image_18.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph TD
  A["左大括号和右大括号"] --> B{"struct inflatable\n{ char_name["20"]; float volume; double price; }};
  A --> C["结构的成员"]
  B --> D["关键字\nstruct 标记成为新\n类型的名称"]
  C --> E["结束结构声明"]
```
</details>

图 4.6 结构描述的组成部分

定义结构后，便可以创建这种类型的变量了:

```cpp
inflatable hat;          // hat is a structure variable of type inflatable
inflatable woopie_cushion;    // type inflatable variable
inflatable mainframe;       // type inflatable variable
```

如果您熟悉 C 语言中的结构，则可能已经注意到了，C++允许在声明结构变量时省略关键字 struct:

```c
struct inflatable goose;      // keyword struct required in C
inflatable vincent;          // keyword struct not required in C++
```

在 C++ 中，结构标记的用法与基本类型名相同。这种变化强调的是，结构声明定义了一种新类型。在 C++ 中，省略 struct 不会出错。

由于 hat 的类型为 inflatable，因此可以使用成员运算符（.）来访问各个成员。例如，hat.volume 指的是结构的 volume 成员，hat.price 指的是 price 成员。同样，vincent.price 是 vincent 变量的 price 成员。总之，通过成员名能够访问结构的成员，就像通过索引能够访问数组的元素一样。由于 price 成员被声明为 double 类型，因此 hat.price 和 vincent.price 相当于是 double 类型的变量，可以像使用常规 double 变量那样来使用它们。总之，hat 是一个结构，而 hat.price 是一个 double 变量。顺便说一句，访问类成员函数（如 cin.getline()）的方式是从访问结构成员变量（如 vincent.price）的方式衍生而来的。

## 4.4.1 在程序中使用结构

介绍结构的主要特征后，下面在一个使用结构的程序中使用这些概念。程序清单 4.11 说明了有关结构的这些问题，还演示了如何初始化结构。

程序清单 4.11 structur.cpp

```cpp
// structur.cpp -- a simple structure
#include <iostream>
struct inflatable  // structure declaration
{
    char name[20];
    float volume;
    double price;
};

int main()
{
    using namespace std;
    inflatable guest =
    {
        "Glorious Gloria",  // name value
        1.88,          // volume value
        29.99          // price value
    };  // guest is a structure variable of type inflatable
// It's initialized to the indicated values
    inflatable pal =
    {
        "Audacious Arthur",
        3.12,
        32.99
    };  // pal is a second variable of type inflatable
// NOTE: some implementations require using
// static inflatable guest =

    cout << "Expand your guest list with " << guest.name;
```

```txt
cout << " and " << pal.name=<< "!\n"=
// pal.name is the name member of the pal variable=
    cout << "You can have both for \$";
    cout << guest.price + pal.price << "!\n";
    return 0;
}
```

下面是该程序的输出:

```txt
Expand your guest list with Glorious Gloria and Audacious Arthur! You can have both for \$62.98!
```

程序说明

结构声明的位置很重要。对于 structur.cpp 而言，有两种选择。可以将声明放在 main() 函数中，紧跟在开始括号的后面。另一种选择是将声明放到 main() 的前面，这里采用的便是这种方式，位于函数外面的声明被称为外部声明。对于这个程序来说，两种选择之间没有实际区别。但是对于那些包含两个或更多函数的程序来说，差别很大。外部声明可以被其后面的任何函数使用，而内部声明只能被该声明所属的函数使用。通常应使用外部声明，这样所有函数都可以使用这种类型的结构（参见图 4.7）。

![](images/page_107_image_7.jpg)

<details>
<summary>text_image</summary>

外部声明—可以用在
文件的所有函数中 _______
局部声明—只能
用在这个函数中 _______
parts类型的变量 _______
perts类型的变量 _______
parts类型的变量 _______
不能在此声明perts
类型的变量 _______
#include <iostream>
using namespace std;
struct parts
{
    unsigned long part_number;
    float part_cost;
};
void mail ();
int main()
{
    struct perks
    {
        int key_number;
        char car[12];
};
parts chicken;
perks mr_blug;
...
...
}
void mail()
{
    parts studebaker;
...
...
}
</details>

图 4.7 局部结构声明和外部结构声明

变量也可以在函数内部和外部定义，外部变量由所有的函数共享（这将在第9章做更详细的介绍）。C++不提倡使用外部变量，但提倡使用外部结构声明。另外，在外部声明符号常量通常更合理。

接下来，请注意初始化方式:

```c
inflatable guest =
{
    "Glorious Gloria",  // name value
    1.88,                 // volume value
    29.99                // price value
};
```

和数组一样，使用由逗号分隔值列表，并将这些值用花括号括起。在该程序中，每个值占一行，但也

可以将它们全部放在同一行中。只是应用逗号将它们分开:

```txt
inflatable duck = {"Daphne", 0.12, 9.98};
```

可以将结构的每个成员都初始化为适当类型的数据。例如，name 成员是一个字符数组，因此可以将其初始化为一个字符串。

可将每个结构成员看作是相应类型的变量。因此，pal.price 是一个 double 变量，而 pal.name 是一个 char 数组。当程序使用 cout 显示 pal.name 时，将把该成员显示为字符串。另外，由于 pal.name 是一个字符数组，因此可以用下标来访问其中的各个字符。例如，pal.name[0] 是字符 A。不过 pal[0] 没有意义，因为 pal 是一个结构，而不是数组。

## 4.4.2 C++11 结构初始化

与数组一样，C++11也支持将列表初始化用于结构，且等号（=）是可选的:

```txt
inflatable duck {"Daphne", 0.12, 9.98}; // can omit the = in C++11
```

其次，如果大括号内未包含任何东西，各个成员都将被设置为零。例如，下面的声明导致 mayor.volume 和 mayor.price 被设置为零，且 mayor.name 的每个字节都被设置为零:

```txt
inflatable mayor {};
```

最后，不允许缩窄转换。

## 4.4.3 结构可以将 string 类作为成员吗

可以将成员 name 指定为 string 对象而不是字符数组吗？即可以像下面这样声明结构吗？

```cpp
#include <string>
struct inflatable  // structure definition
{
    std::string name;
    float volume;
    double price;
};
```

答案是肯定的，只要您使用的编译器支持对以 string 对象作为成员的结构进行初始化。

一定要让结构定义能够访问名称空间 std。为此，可以将编译指令 using 移到结构定义之前；也可以像前面那样，将 name 的类型声明为 std::string。

## 4.4.4 其他结构属性

C++使用户定义的类型与内置类型尽可能相似。例如，可以将结构作为参数传递给函数，也可以让函数返回一个结构。另外，还可以使用赋值运算符（=）将结构赋给另一个同类型的结构，这样结构中每个成员都将被设置为另一个结构中相应成员的值，即使成员是数组。这种赋值被称为成员赋值（memberwise assignment），将在第7章讨论函数时再介绍如何传递和返回结构。下面简要地介绍一下结构赋值，程序清单4.12是一个这样的示例。

程序清单 4.12 assign\_st.cpp

```cpp
// assign_st cpp -- assigning structures
#include <iostream>
struct inflatable
{
    char name[20];
    float volume;
    double price;
};
int main()
```

```txt
{
    using namespace std;
    inflatable bouquet =
    {
        "sunflowers",
        0.20,
        12.49
    };
    inflatable choice;
    cout << "bouquet: " << bouquet.name << " for \$";
    cout << bouquet.price << endl;

    choice = bouquet;  // assign one structure to another
    cout << "choice: " << choice.name << " for \$";
    cout << choice.price << endl;
    return 0;
}
```

下面是该程序的输出:

```yaml
bouquet: sunflowers for \$12.49
choice: sunflowers for \$12.49
```

从中可以看出，成员赋值是有效的，因为 choice 结构的成员值与 bouquet 结构中存储的值相同。可以同时完成定义结构和创建结构变量的工作。为此，只需将变量名放在结束括号的后面即可:

```c
struct perks
{
    int key_number;
    char car[12];
} mr_smith, ms_jones;   // two perks variables
```

甚至可以初始化以这种方式创建的变量:

```c
struct perks
{
    int key_number;
    char car[12];
} mr_glitz =
{
    7,          // value for mr_glitz.key_number member
    "Packard"     // value for mr_glitz.car member
};
```

然而，将结构定义和变量声明分开，可以使程序更易于阅读和理解。

还可以声明没有名称的结构类型，方法是省略名称，同时定义一种结构类型和一个这种类型的变量:

```txt
struct        // no tag
{
    int x;   // 2 members
    int y;
} position;  // a structure variable
```

这样将创建一个名为 position 的结构变量。可以使用成员运算符来访问它的成员（如 position.x），但这种类型没有名称，因此以后无法创建这种类型的变量。本书将不使用这种形式的结构。

除了 C++ 程序可以使用结构标记作为类型名称外，C 结构具有到目前为止讨论的 C++ 结构的所有特性（C++11 特性除外），但 C++ 结构的特性更多。例如，与 C 结构不同，C++ 结构除了成员变量之外，还可以有成员函数。但这些高级特性通常被用于类中，而不是结构中，因此将在讨论类的时候（从第 10 章开始）

介绍它们。

## 4.4.5 结构数组

inflatable 结构包含一个数组（name）。也可以创建元素为结构的数组，方法和创建基本类型数组完全相同。例如，要创建一个包含 100 个 inflatable 结构的数组，可以这样做:

```txt
inflatable gifts[100]; // array of 100 inflatable structures
```

这样，gifts 将是一个 inflatable 数组，其中的每个元素（如 gifts[0]或 gifts[99]）都是 inflatable 对象，可以与成员运算符一起使用:

```cpp
cin >> gifts[0].volume;          // use volume member of first struct
cout << gifts[99].price << endl; // display price member of last struct
```

记住，gifts 本身是一个数组，而不是结构，因此像 gifts.price 这样的表述是无效的。

要初始化结构数组，可以结合使用初始化数组的规则（用逗号分隔每个元素的值，并将这些值用花括号括起）和初始化结构的规则（用逗号分隔每个成员的值，并将这些值用花括号括起）。由于数组中的每个元素都是结构，因此可以使用结构初始化的方式来提供它的值。因此，最终结果为一个被括在花括号中、用逗号分隔的值列表，其中每个值本身又是一个被括在花括号中、用逗号分隔的值列表:

```txt
inflatable guests[2] =          // initializing an array of structs
{
    {"Bambi", 0.5, 21.99},      // first structure in array
    {"Godzilla", 2000, 565.99} // next structure in array
};
```

可以按自己喜欢的方式来格式化它们。例如，两个初始化位于同一行，而每个结构成员的初始化各占一行。

程序清单 4.13 是一个使用结构数组的简短示例。由于 guests 是一个 inflatable 数组，因此 guests[0] 的类型为 inflatable，可以使用它和句点运算符来访问相应 inflatable 结构的成员。

程序清单 4.13 arrstruc.cpp

```cpp
// arrstruc.cpp -- an array of structures
#include <iostream>
struct inflatable
{
    char name[20];
    float volume;
    double price;
};
int main()
{
    using namespace std;
    inflatable guests[2] =          // initializing an array of structs
    {
        {"Bambi", 0.5, 21.99},      // first structure in array
        {"Godzilla", 2000, 565.99}  // next structure in array
    };

    cout << "The guests " << guests[0].name << " and " << guests[1].name
        << "\nhave a combined volume of "
        << guests[0].volume + guests[1].volume << " cubic feet.\n";
    return 0;
}
```

下面是该程序的输出:

```txt
The guests Bambi and Godzilla have a combined volume of 2000.5 cubic feet.
```

## 4.4.6 结构中的位字段

与 C 语言一样，C++也允许指定占用特定位数的结构成员，这使得创建与某个硬件设备上的寄存器对应的数据结构非常方便。字段的类型应为整型或枚举（稍后将介绍），接下来是冒号，冒号后面是一个数字，它指定了使用的位数。可以使用没有名称的字段来提供间距。每个成员都被称为位字段（bit field）。下面是一个例子:

```txt
struct_torgle_register
{
    unsigned int SN : 4;   // 4 bits for SN value
    unsigned int : 4;   // 4 bits unused
    bool_goodIn : 1;   // valid input (1 bit)
    bool goodTorgle : 1;   // successful torgling
};
```

可以像通常那样初始化这些字段，还可以使用标准的结构表示法来访问位字段:

```javascript
torgle_register_tr = { 14, true, false };
if (tr.goodIn) = // if statement covered-in Chapter 6
```

位字段通常用在低级编程中。一般来说，可以使用整型和附录E介绍的按位运算符来代替这种方式。

## 4.5 共用体

共用体（union）是一种数据格式，它能够存储不同的数据类型，但只能同时存储其中的一种类型。也就是说，结构可以同时存储 int、long 和 double，共用体只能存储 int、long 或 double。共用体的句法与结构相似，但含义不同。例如，请看下面的声明:

```c
union one4all
{
    int int_val;
    long long_val;
    double double_val;
};
```

可以使用 one4all 变量来存储 int、long 或 double，条件是在不同的时间进行:

```txt
one4all pail;
pail.int_val = 15;      // store an int
cout << pail.int_val;
pail.double_val = 1.38;   // store a double, int value is lost
cout << pail.double_val;
```

因此，pail 有时可以是 int 变量，而有时又可以是 double 变量。成员名称标识了变量的容量。由于共用体每次只能存储一个值，因此它必须有足够的空间来存储最大的成员，所以，共用体的长度为其最大成员的长度。

共用体的用途之一是，当数据项使用两种或更多种格式（但不会同时使用）时，可节省空间。例如，假设管理一个小商品目录，其中有一些商品的ID为整数，而另一些的ID为字符串。在这种情况下，可以这样做:

```txt
struct widget
{
    char_brand[20];
    int_type;
    union id          // format depends on widget type
    {
        long id_num;      // type 1 widgets
        char id_char[20]; // other widgets
    } id_val;
    };
    ...
    widget prize;
    ...
    if (prize.type == 1):          // if-else_statement (Chapter 6)
        cin >> prize.id_val.id_num;   // use member name to indicate mode
    else
        cin >> prize.id_val.id_char;
```

匿名共用体（anonymous union）没有名称，其成员将成为位于相同地址处的变量。显然，每次只有一个成员是当前的成员:

```c
struct widget
{
    char brand[20];
    int type;
    union          // anonymous union
{
        long id_num;      // type 1 widgets
        char id_char[20]; // other widgets
    };
};
widget prize;
if (prize.type == 1)
    cin >> prize.id_num;
else
    cin >> prize.id_char;
```

由于共用体是匿名的，因此 id\_num 和 id\_char 被视为 prize 的两个成员，它们的地址相同，所以不需要中间标识符 id\_val。程序员负责确定当前哪个成员是活动的。

共用体常用于（但并非只能用于）节省内存。当前，系统的内存多达数 GB 甚至数 TB，好像没有必要节省内存，但并非所有的 C++ 程序都是为这样的系统编写的。C++ 还用于嵌入式系统编程，如控制烤箱、MP3 播放器或火星漫步者的处理器。对这些应用程序来说，内存可能非常宝贵。另外，共用体常用于操作系统数据结构或硬件数据结构。

## 4.6 枚举

C++的enum工具提供了另一种创建符号常量的方式，这种方式可以代替const。它还允许定义新类型，但必须按严格的限制进行。使用enum的句法与使用结构相似。例如，请看下面的语句:

enum spectrum {red, orange, yellow, green, blue, violet, indigo, ultraviolet};

这条语句完成两项工作。

- 让 spectrum 成为新类型的名称；spectrum 被称为枚举（enumeration），就像 struct 变量被称为结构一样。
- 将 red、orange、yellow 等作为符号常量，它们对应整数值 0～7。这些常量叫作枚举量（enumerator）。

在默认情况下，将整数值赋给枚举量，第一个枚举量的值为0，第二个枚举量的值为1，依次类推。可以通过显式地指定整数值来覆盖默认值，本章后面将介绍如何做。

可以用枚举名来声明这种类型的变量:

```txt
spectrum band;  // band a variable of type spectrum
```

枚举变量具有一些特殊的属性，下面来看一看。

在不进行强制类型转换的情况下，只能将定义枚举时使用的枚举量赋给这种枚举的变量，如下所示:

```cpp
band = blue;          // valid, blue is an enumerator
band = 2000;         // invalid, 2000 not an enumerator
```

因此，spectrum 变量受到限制，只有 8 个可能的值。如果试图将一个非法值赋给它，则有些编译器将出现编译器错误，而另一些则发出警告。为获得最大限度的可移植性，应将把非 enum 值赋给 enum 变量视为错误。

对于枚举，只定义了赋值运算符。具体地说，没有为枚举定义算术运算:

```txt
band = orange;          // valid
++band;                 // not valid, ++ discussed in Chapter 5
band = orange + red;     // not valid, but a little tricky
```

...

然而，有些实现并没有这种限制，这有可能导致违反类型限制。例如，如果 band 的值为 ultraviolet（7），则++band（如果有效的话）将把 band 增加到 8，而对于 spectrum 类型来说，8 是无效的。另外，为获得最大限度的可移植性，应采纳较严格的限制。

枚举量是整型，可被提升为 int 类型，但 int 类型不能自动转换为枚举类型:

```txt
int color = blue;          // valid, spectrum type promoted to int
band = 3;                   // invalid, int not converted to spectrum
color = 3 + red;         // valid, red converted to int
```

...

虽然在这个例子中，3 对应的枚举量是 green，但将 3 赋给 band 将导致类型错误。不过将 green 赋给 band 是可以的，因为它们都是 spectrum 类型。同样，有些实现方法没有这种限制。表达式  $3 + red$  中的加法并非为枚举量定义，但 red 被转换为 int 类型，因此结果的类型也是 int。由于在这种情况下，枚举将被转换为 int，因此可以在算术表达式中同时使用枚举和常规整数，尽管并没有为枚举本身定义算术运算。

前面示例:

```txt
band = orange + red;      // not valid, but a little tricky
```

非法的原因有些复杂。确实没有为枚举定义运算符+，但用于算术表达式中时，枚举将被转换为整数，因此表达式 orange + red 将被转换为 1 + 0。这是一个合法的表达式，但其类型为 int，不能将其赋给类型为 spectrum 的变量 band。

如果 int 值是有效的，则可以通过强制类型转换，将它赋给枚举变量:

```txt
band = spectrum(3);          // typecast 3 to type spectrum
```

如果试图对一个不适当的值进行强制类型转换，将出现什么情况呢？结果是不确定的，这意味着这样做不会出错，但不能依赖得到的结果:

```javascript
band = spectrum(40003);      // undefined
```

请参阅本章后面的“枚举的取值范围”一节，以了解一下哪些值合适，哪些值不合适。

正如您看到的那样，枚举的规则相当严格。实际上，枚举更常被用来定义相关的符号常量，而不是新类型。例如，可以用枚举来定义 switch 语句中使用的符号常量（有关示例见第 6 章）。如果打算只使用常量，而不创建枚举类型的变量，则可以省略枚举类型的名称，如下面的例子所示:

```javascript
enum {red, orange, yellow, green, blue, violet, indigo, ultraviolet};
```

## 4.6.1 设置枚举量的值

可以使用赋值运算符来显式地设置枚举量的值:

$$
\text {enum bits} \{\text {one} = 1, \text {two} = 2, \text {four} = 4, \text {eight} = 8 \};
$$

指定的值必须是整数。也可以只显式地定义其中一些枚举量的值:

$$
\text {enum bigstep} \{\text {first, second} = 1 0 0, \text {third} \};
$$

这里，first 在默认情况下为 0。后面没有被初始化的枚举量的值将比其前面的枚举量大 1。因此，third 的值为 101。

最后，可以创建多个值相同的枚举量:

$$
\text {enum} \{\text {zero, null} = 0, \text {one, numero\_uno} = 1 \};
$$

其中，zero 和 null 都为 0，one 和 umero\_uno 都为 1。在 C++ 早期的版本中，只能将 int 值（或提升为 int 的值）赋给枚举量，但这种限制取消了，因此可以使用 long 甚至 long long 类型的值。

## 4.6.2 枚举的取值范围

最初，对于枚举来说，只有声明中指出的那些值是有效的。然而，C++现在通过强制类型转换，增加了可赋给枚举变量的合法值。每个枚举都有取值范围（range），通过强制类型转换，可以将取值范围中的任何整数值赋给枚举变量，即使这个值不是枚举值。例如，假设bits和myflag的定义如下:

$$
\begin{array}{l} \text {enum bits\{one = 1, two = 2, four = 4, eight = 8\}}; \\ \text {bits myflag;} \end{array}
$$

则下面的代码将是合法的:

$$
\text {myflag} = \text {bits(6)}; \quad / / \text {valid, because 6 is in bits range}
$$

其中 6 不是枚举值，但它位于枚举定义的取值范围内。

取值范围的定义如下。首先，要找出上限，需要知道枚举量的最大值。找到大于这个最大值的、最小的2的幂，将它减去1，得到的便是取值范围的上限。例如，前面定义的bigstep的最大值枚举值是101。在2的幂中，比这个数大的最小值为128，因此取值范围的上限为127。要计算下限，需要知道枚举量的最小值。如果它不小于0，则取值范围的下限为0；否则，采用与寻找上限方式相同的方式，但加上负号。例如，如果最小的枚举量为-6，而比它小的、最大的2的幂是-8（加上负号），因此下限为-7。

选择用多少空间来存储枚举由编译器决定。对于取值范围较小的枚举，使用一个字节或更少的空间；而对于包含 long 类型值的枚举，则使用 4 个字节。

C++11 扩展了枚举，增加了作用域内枚举（scoped enumeration），第 10 章的“类作用域”一节将简要地介绍这种枚举。

## 4.7 指针和自由存储空间

在第 3 章的开头，提到了计算机程序在存储数据时必须跟踪的 3 种基本属性。为了方便，这里再次列出了这些属性:

● 信息存储在何处；
- 存储的值为多少；
存储的信息是什么类型。

您使用过一种策略来达到上述目的:定义一个简单变量。声明语句指出了值的类型和符号名，还让程序为值分配内存，并在内部跟踪该内存单元。

下面来看一看另一种策略，它在开发 C++ 类时非常重要。这种策略以指针为基础，指针是一个变量，其存储的是值的地址，而不是值本身。在讨论指针之前，我们先看一看如何找到常规变量的地址。只需对变量应用地址运算符（&），就可以获得它的位置；例如，如果 home 是一个变量，则&home 是它的地址。程序清单 4.14 演示了这个运算符的用法。

程序清单 4.14 address.cpp

```cpp
// address.cpp -- using the & operator to find addresses
#include <iostream>
int main()
{
    using namespace std;
    int donuts = 6;
    double cups = 4.5;

    cout << "donuts value = " << donuts;
    cout << " and donuts address = " << &donuts << endl;
// NOTE: you may need to use unsigned (&donuts)
// and unsigned (&cups)
    cout << "cups value = " << cups;
    cout << " and cups address = " << &cups << endl;
    return 0;
}
```

下面是该程序在某个系统上的输出:

```txt
donuts value = 6 and donuts address = 0x0065fd40
cups value = 4.5 and cups address = 0x0065fd44
```

显示地址时，该实现的cout使用十六进制表示法，因为这是常用于描述内存的表示法（有些实现可能使用十进制表示法）。在该实现中，donuts的存储位置比cups要低。两个地址的差为0x0065fd44-0x0065fd40（即4）。这是有意义的，因为donuts的类型为int，而这种类型使用4个字节。当然，不同系统给定的地址值可能不同。有些系统可能先存储cups，再存储donuts，这样两个地址值的差将为8个字节，因为cups的类型为double。另外，在有些系统中，可能不会将这两个变量存储在相邻的内存单元中。

使用常规变量时，值是指定的量，而地址为派生量。下面来看看指针策略，它是 C++ 内存管理编程理念的核心（参见旁注“指针与 C++ 基本原理”）。

## 指针与 $\mathbf{C} + +$ 基本原理

面向对象编程与传统的过程性编程的区别在于，OOP 强调的是在运行阶段（而不是编译阶段）进行决策。运行阶段指的是程序正在运行时，编译阶段指的是编译器将程序组合起来时。运行阶段决策就好比度假时，选择参观哪些景点取决于天气和当时的心情；而编译阶段决策更像不管在什么条件下，都坚持预先设定的日程安排。

运行阶段决策提供了灵活性，可以根据当时的情况进行调整。例如，考虑为数组分配内存的情况。传统的方法是声明一个数组。要在 C++ 中声明数组，必须指定数组的长度。因此，数组长度在程序编译时就设定好了；这就是编译阶段决策。您可能认为，在 80% 的情况下，一个包含 20 个元素的数组足够了，但程序有时需要处理 200 个元素。为了安全起见，使用了一个包含 200 个元素的数组。这样，程序在大多数情况下都浪费了内存。OOP 通过将这样的决策推迟到运行阶段进行，使程序更灵活。在程序运行后，可以这次告诉它只需要 20 个元素，而还可以下次告诉它需要 205 个元素。

总之，使用 OOP 时，您可能在运行阶段确定数组的长度。为使用这种方法，语言必须允许在程序运行时创建数组。稍后您看会到，C++采用的方法是，使用关键字 new 请求正确数量的内存以及使用指针来跟踪新分配的内存的位置。

在运行阶段做决策并非 OOP 独有的，但使用 C++ 编写这样的代码比使用 C 语言简单。

处理存储数据的新策略刚好相反，将地址视为指定的量，而将值视为派生量。一种特殊类型的变量——指针用于存储值的地址。因此，指针名表示的是地址。\*运算符被称为间接值（indirect value）或解除引用（dereferencing）运算符，将其应用于指针，可以得到该地址处存储的值（这和乘法使用的符号相同；C++根据上下文来确定所指的是乘法还是解除引用）。例如，假设 manly 是一个指针，则 manly 表示的是一个地址，而\*manly 表示存储在该地址处的值。\*manly 与常规 int 变量等效。程序清单 4.15 说明了这几点，它还演示了如何声明指针。

程序清单 4.15 pointer.cpp

```cpp
// pointer.cpp -- our first pointer variable
#include <iostream>
int main()
{
    using namespace std;
    int updates = 6;          // declare a variable
    int * p_updates;         // declare pointer to an int
    p_updates = &updates;   // assign address of int to pointer

// express values two ways
    cout << "Values: updates = " << updates;
    cout << ", *p_updates = " << *p_updates << endl;

// express address two ways
    cout << "Addresses: &updates = " << &updates;
    cout << ", p_updates = " << p_updates << endl;

// use pointer to change value
    *p_updates = *p_updates + 1;
    cout << "Now updates = " << updates << endl;
    return 0;
}
```

下面是该程序的输出:

```python
Values: updates = 6, *p_updates = 6
Addresses: &updates = 0x0065fd48, p_updates = 0x0065fd48
Now updates = 7
```

从中可知，int 变量 updates 和指针变量 p\_updates 只不过是同一枚硬币的两面。变量 updates 表示值，并使用&运算符来获得地址；而变量 p\_updates 表示地址，并使用\*运算符来获得值（参见图 4.8）。由于 p\_updates 指向 updates，因此\*p\_updates 和 updates 完全等价。可以像使用 int 变量那样使用\*p\_updates。正如程序清单 4.15 表明的，甚至可以将值赋给\*p\_updates。这样做将修改指向的值，即 updates。

![](images/page_116_image_8.jpg)

<details>
<summary>text_image</summary>

int jumbo = 23;
int * pe = &jumbo;
</details>

图 4.8 硬币的两面

## 4.7.1 声明和初始化指针

我们来看看如何声明指针。计算机需要跟踪指针指向的值的类型。例如，char 的地址与 double 的地址看上去没什么两样，但 char 和 double 使用的字节数是不同的，它们存储值时使用的内部格式也不同。因此，指针声明必须指定指针指向的数据的类型。

例如，前一个示例包含这样的声明:

```txt
int * p_updates
```

这表明，\*p\_updates 的类型为 int。由于\*运算符被用于指针，因此 p\_updates 变量本身必须是指针。我们说 p\_updates 指向 int 类型，我们还说 p\_updates 的类型是指向 int 的指针，或 int\*。可以这样说，p\_updates 是指针（地址），而 \*p\_updates 是 int，而不是指针（见图 4.9）。

![](images/page_117_image_7.jpg)

<details>
<summary>text_image</summary>

内存地址
1000
1002
1004
1006
1008
1010
1012
1014
1016
int ducks = 12;
创建ducks变量，将值12
存储在该变量中
变量名称
ducks
birddog指向
ducks
birddog
into *birddog = &ducks;
创建birddog变量，将ducks
的地址存储在该变量中
</details>

图4.9 指针存储地址

顺便说一句，\*运算符两边的空格是可选的。传统上，C程序员使用这种格式:

```c
int *ptr;
```

这强调\*ptr 是一个 int 类型的值。而很多 C++ 程序员使用这种格式:

```txt
int* ptr;
```

这强调的是:int\*是一种类型——指向 int 的指针。在哪里添加空格对于编译器来说没有任何区别，您甚至可以这样做:

```txt
int*ptr;
```

但要知道的是，下面的声明创建一个指针（p1）和一个 int 变量（p2）:

```txt
int* p1, p2;
```

对每个指针变量名，都需要使用一个\*。

注意:在 €++ 中，int \* 是一种复合类型，是指向 int 的指针。

可以用同样的句法来声明指向其他类型的指针:

```cpp
double * tax_ptr; // tax_ptr points to type double
char * str;      // str points to type char
```

由于已将 tax\_ptr 声明为一个指向 double 的指针，因此编译器知道\*tax\_ptr 是一个 double 类型的值。也就是说，它知道\*tax\_ptr 是一个以浮点格式存储的值，这个值（在大多数系统上）占据 8 个字节。指针变量不仅仅是指针，而且是指向特定类型的指针。tax\_ptr 的类型是指向 double 的指针（或 double \*类型），str 是指向 char 的指针类型（或 char \*）。尽管它们都是指针，却是不同类型的指针。和数组一样，指针都是基于其他类型的。

虽然 tax\_ptr 和 str 指向两种长度不同的数据类型，但这两个变量本身的长度通常是相同的。也就是说，char 的地址与 double 的地址的长度相同，这就好比 1016 可能是超市的街道地址，而 1024 可以是小村庄的街道地址一样。地址的长度或值既不能指示关于变量的长度或类型的任何信息，也不能指示该地址上有什么建筑物。一般来说，地址需要 2 个还是 4 个字节，取决于计算机系统（有些系统可能需要更大的地址，系统可以针对不同的类型使用不同长度的地址）。

可以在声明语句中初始化指针。在这种情况下，被初始化的是指针，而不是它指向的值。也就是说，下面的语句将 pt（而不是\*pt）的值设置为&higgens:

```c
int higgens = 5;
int * pt = &higgens;
```

程序清单 4.16 演示了如何将指针初始化为一个地址。

程序清单 4.16 init\_ptr.cpp

```cpp
// init_ptr.cpp -- initialize a pointer
#include <iostream>
int main()
{
    using namespace std;
    int higgens == 5;
    int * pt = &higgens;

    cout << "Value of higgens = " << higgens
        << "; Address of higgens = " << &higgens << endl;
    cout << "Value of *pt = " << *pt
        << "; Value of pt = " << pt << endl;
    return 0;
}
```

下面是该程序的示例输出:

```txt
Value of higgens = 5; Address of higgens = 0012FED4=
Value of *pt = 5; Value of pt = 0012FED4
```

从中可知，程序将 pi（而不是\*pi）初始化为 higgens 的地址。在您的系统上，显示的地址可能不同，显示格式也可能不同。

## 4.7.2 指针的危险

危险更易发生在那些使用指针不仔细的人身上。极其重要的一点是:在 C++ 中创建指针时，计算机将分配用来存储地址的内存，但不会分配用来存储指针所指向的数据的内存。为数据提供空间是一个独立的步骤，忽略这一步无疑是自找麻烦，如下所示:

```txt
long * fellow;          // create a pointer-to-long_
*fellow = 223323;       // place a value in never-never land
```

fellow 确实是一个指针，但它指向哪里呢？上述代码没有将地址赋给 fellow。那么 223323 将被放在哪里呢？我们不知道。由于 fellow 没有被初始化，它可能有任何值。不管值是什么，程序都将它解释为存储 223323 的地址。如果 fellow 的值碰巧为 1200，计算机将把数据放在地址 1200 上，即使这恰巧是程序代码的地址。fellow 指向的地方很可能并不是所要存储 223323 的地方。这种错误可能会导致一些最隐匿、最难

以跟踪的 bug。

警告: 一定要在对指针应用解除引用运算符 (\*) 之前, 将指针初始化为一个确定的、适当的地址。这是关于使用指针的金科玉律。

## 4.7:3 指针和数字

指针不是整型，虽然计算机通常把地址当作整数来处理。从概念上看，指针与整数是截然不同的类型。整数是可以执行加、减、除等运算的数字，而指针描述的是位置，将两个地址相乘没有任何意义。从可以对整数和指针执行的操作上看，它们也是彼此不同的。因此，不能简单地将整数赋给指针:

```c
int * pt;
pt = 0xB8000000;  // type mismatch
```

在这里，左边是指向 int 的指针，因此可以把它赋给地址，但右边是一个整数。您可能知道，0xB8000000是老式计算机系统中视频内存的组合段偏移地址，但这条语句并没有告诉程序，这个数字就是一个地址。在 C99 标准发布之前，C 语言允许这样赋值。但 C++ 在类型一致方面的要求更严格，编译器将显示一条错误消息，通告类型不匹配。要将数字值作为地址来使用，应通过强制类型转换将数字转换为适当的地址类型:

```txt
int * pt;
pt = (int *) 0xB8000000; // types now match
```

这样，赋值语句的两边都是整数的地址，因此这样赋值有效。注意，pt 是 int 值的地址并不意味着 pt 本身的类型是 int。例如，在有些平台中，int 类型是个 2 字节值，而地址是个 4 字节值。

指针还有其他一些有趣的特性，这将在合适的时候讨论。下面看看如何使用指针来管理运行阶段的内存空间分配。

## 4.7.4 使用 new 来分配内存

对指针的工作方式有一定了解后，来看看它如何实现在程序运行时分配内存。前面我们都将指针初始化为变量的地址；变量是在编译时分配的有名称的内存，而指针只是为可以通过名称直接访问的内存提供了一个别名。指针真正的用武之地在于，在运行阶段分配未命名的内存以存储值。在这种情况下，只能通过指针来访问内存。在 C 语言中，可以用库函数 malloc() 来分配内存；在 C++ 中仍然可以这样做，但 C++ 还有更好的方法——new 运算符。

下面来试试这种新技术，在运行阶段为一个 int 值分配未命名的内存，并使用指针来访问这个值。这里的关键所在是 C++ 的 new 运算符。程序员要告诉 new，需要为哪种数据类型分配内存；new 将找到一个长度正确的内存块，并返回该内存块的地址。程序员的责任是将该地址赋给一个指针。下面是一个这样的示例:

```txt
int * pn = new int;
```

new int 告诉程序，需要适合存储 int 的内存。new 运算符根据类型来确定需要多少字节的内存。然后，它找到这样的内存，并返回其地址。接下来，将地址赋给 pn，pn 是被声明为指向 int 的指针。现在，pn 是地址，而 \*pn 是存储在那里的值。将这种方法与将变量的地址赋给指针进行比较:

```txt
int higgens;
int * pt = &higgens;
```

在这两种情况（pn 和 pt）下，都是将一个 int 变量的地址赋给了指针。在第二种情况下，可以通过名称 higgens 来访问该 int，在第一种情况下，则只能通过该指针进行访问。这引出了一个问题:pn 指向的内存没有名称，如何称呼它呢？我们说 pn 指向一个数据对象，这里的“对象”不是“面向对象编程”中的对象，而是一样“东西”。术语“数据对象”比“变量”更通用，它指的是为数据项分配的内存块。因此，变量也是数据对象，但 pn 指向的内存不是变量。乍一看，处理数据对象的指针方法可能不太好用，但它使程序在管理内存方面有更大的控制权。

为一个数据对象（可以是结构，也可以是基本类型）获得并指定分配内存的通用格式如下:

```txt
typeName * pointer_name = new typeName;
```

需要在两个地方指定数据类型:用来指定需要什么样的内存和用来声明合适的指针。当然，如果已经声明了相应类型的指针，则可以使用该指针，而不用再声明一个新的指针。程序清单 4.17 演示了如何将 new 用于两种不同的类型。

程序清单 4.17 use\_new.cpp

```cpp
// use_new.cpp -- using the new operator
#include <iostream>
int main()
{
    using namespace std;
    int nights = 1001;
    int * pt = new int;          // allocate space for an int
    *pt = 1001;                    // store a value there

    cout << "nights value = ";
    cout << nights << ": location " << &nights << endl;
    cout << "int ";
    cout << "value = " << *pt << ": location = " << pt << endl;
    double * pd = new double;   // allocate space for a double
    *pd = 10000001.0;           // store a double there

    cout << "double ";
    cout << "value = " << *pd << ": location = " << pd << endl;
    cout << "location of pointer pd: " << &pd << endl;
    cout << "size of pt = " << sizeof(pt);
    cout << ": size of *pt = " << sizeof(*pt) << endl;
    cout << "size of pd = " << sizeof pd;
    cout << ": size of *pd = " << sizeof(*pd) << endl;
    return 0;
}
```

下面是该程序的输出:

```txt
nights value = 1001: location 0028F7F8
int value = 1001: location = 00033A98
double value = 1e+007: location = 000339B8
location of pointer pd: 0028F7FC
size of pt = 4: size of *pt = 4
size of pd = 4: size of *pd = 8
```

当然，内存位置的准确值随系统而异。

## 程序说明

该程序使用 new 分别为 int 类型和 double 类型的数据对象分配内存。这是在程序运行时进行的。指针 pt 和 pd 指向这两个数据对象，如果没有它们，将无法访问这些内存单元。有了这两个指针，就可以像使用变量那样使用 \*pt 和 \*pd 了。将值赋给 \*pt 和 \*pd，从而将这些值赋给新的数据对象。同样，可以通过打印 \*pt 和 \*pd 来显示这些值。

该程序还指出了必须声明指针所指向的类型的原因之一。地址本身只指出了对象存储地址的开始，而没有指出其类型（使用的字节数）。从这两个值的地址可以知道，它们都只是数字，并没有提供类型或长度信息。另外，指向 int 的指针的长度与指向 double 的指针相同。它们都是地址，但由于 use\_new.cpp 声明了指针的类型，因此程序知道\*pd 是 8 个字节的 double 值，\*pt 是 4 个字节的 int 值。use\_new.cpp 打印\*pd 的值时，cout 知道要读取多少字节以及如何解释它们。

对于指针,需要指出的另一点是,new分配的内存块通常与常规变量声明分配的内存块不同。变量 nights 和 pd 的值都存储在被称为栈（stack）的内存区域中，而 new 从被称为堆（heap）或自由存储区（free store）的内存区域分配内存。第 9 章将更详细地讨论这一点。

## 内存被耗尽？

计算机可能会由于没有足够的内存而无法满足 new 的请求。在这种情况下，new 通常会引发异常——一种将在第 15 章讨论的错误处理技术；而在较老的实现中，new 将返回 0。在 C++ 中，值为 0 的指针被称为空指针（null pointer）。C++ 确保空指针不会指向有效的数据，因此它常被用来表示运算符或函数失败（如果成功，它们将返回一个有用的指针）。将在第 6 章讨论的 if 语句可帮助您处理这种问题；就目前而言，您只需如下要点:C++ 提供了检测并处理内存分配失败的工具。

## 4.7.5 使用 delete 释放内存

当需要内存时，可以使用 new 来请求，这只是 C++ 内存管理数据包中有魅力的一个方面。另一个方面是 delete 运算符，它使得在使用完内存后，能够将其归还给内存池，这是通向最有效地使用内存的关键一步。归还或释放（free）的内存可供程序的其他部分使用。使用 delete 时，后面要加上指向内存块的指针（这些内存块最初是用 new 分配的）:

```txt
int * ps = new int; // allocate memory with new-
...        // use the memory
delete ps;     // free memory with delete when done
```

这将释放 ps 指向的内存，但不会删除指针 ps 本身。例如，可以将 ps 重新指向另一个新分配的内存块。一定要配对地使用 new 和 delete；否则将发生内存泄漏（memory leak），也就是说，被分配的内存再也无法使用了。如果内存泄漏严重，则程序将由于不断寻找更多内存而终止。

不要尝试释放已经释放的内存块，C++标准指出，这样做的结果将是不确定的，这意味着什么情况都可能发生。另外，不能使用 delete 来释放声明变量所获得的内存:

```c
int * ps = new int;    // ok
delete ps;                 // ok
delete ps;                 // not ok now
int jugs= 5;        // ok
int * pi = &jugs;    // ok
delete pi;                // not allowed, memory not allocated by new
```

警告:只能用 delete 来释放使用 new 分配的内存。然而，对空指针使用 delete 是安全的。

注意，使用 delete 的关键在于，将它用于 new 分配的内存。这并不意味着要使用用于 new 的指针，而是用于 new 的地址:

```txt
int * ps = new int;     // allocate memory
int * pq-= ps;        // set second pointer to same block
delete pq;            // delete with second pointer
```

一般来说，不要创建两个指向同一个内存块的指针，因为这将增加错误地删除同一个内存块两次的可能性。但稍后您会看到，对于返回指针的函数，使用另一个指针确实有道理。

## 4.7.6 使用 new 来创建动态数组

如果程序只需要一个值，则可能会声明一个简单变量，因为对于管理一个小型数据对象来说，这样做比使用 new 和指针更简单，尽管给人留下的印象不那么深刻。通常，对于大型数据（如数组、字符串和结构），应使用 new，这正是 new 的用武之地。例如，假设要编写一个程序，它是否需要数组取决于运行时用户提供的信息。如果通过声明来创建数组，则在程序被编译时将为它分配内存空间。不管程序最终是否使用数组，数组都在那里，它占用了内存。在编译时给数组分配内存被称为静态联编（static binding），意味着数组是在编译时加入到程序中的。但使用 new 时，如果在运行阶段需要数组，则创建它；如果不需要，则不创建。还可以在程序运行时选择数组的长度。这被称为动态联编（dynamic binding），意味着数组是在程序运行时创建的。这种数组叫作动态数组（dynamic array）。使用静态联编时，必须在编写程序时指定数组的长度；使用动态联编时，程序将在运行时确定数组的长度。

下面来看一下关于动态数组的两个基本问题:如何使用 C++ 的 new 运算符创建数组以及如何使用指针访问数组元素。

## 1. 使用 new 创建动态数组

在 C++ 中，创建动态数组很容易；只要将数组的元素类型和元素数目告诉 new 即可。必须在类型名后加上方括号，其中包含元素数目。例如，要创建一个包含 10 个 int 元素的数组，可以这样做:

```typescript
int * psome = new int [10]; // get a block of 10 ints
```

new 运算符返回第一个元素的地址。在这个例子中，该地址被赋给指针 psome。

当程序使用完 new 分配的内存块时，应使用 delete 释放它们。然而，对于使用 new 创建的数组，应使用另一种格式的 delete 来释放:

```txt
delete [] psome;          // free a dynamic array
```

方括号告诉程序，应释放整个数组，而不仅仅是指针指向的元素。请注意 delete 和指针之间的方括号。如果使用 new 时，不带方括号，则使用 delete 时，也不应带方括号。如果使用 new 时带方括号，则使用 delete 时也应带方括号。C++ 的早期版本无法识别方括号表示法。然而，对于 ANSI/ISO 标准来说，new 与 delete 的格式不匹配导致的后果是不确定的，这意味着程序员不能依赖于某种特定的行为。下面是一个例子:

```txt
int * pt = new int;
short * ps = new short [500];
delete [] pt;  // effect is undefined, don't do it
delete ps;      // effect is undefined, don't do it
```

总之，使用 new 和 delete 时，应遵守以下规则。

- 不要使用 delete 来释放不是 new 分配的内存。
- 不要使用 delete 释放同一个内存块两次。
- 如果使用 new[] 为数组分配内存，则应使用 delete[] 来释放。
- 如果使用 new[] 为一个实体分配内存，则应使用 delete（没有方括号）来释放。
- 对空指针应用 delete 是安全的。

现在我们回过头来讨论动态数组。psome 是指向一个 int（数组第一个元素）的指针。您的责任是跟踪内存块中的元素个数。也就是说，由于编译器不能对 psome 是指向 10 个整数中的第 1 个这种情况进行跟踪，因此编写程序时，必须让程序跟踪元素的数目。

实际上，程序确实跟踪了分配的内存量，以便以后使用 delete []运算符时能够正确地释放这些内存。但这种信息不是公用的，例如，不能使用 sizeof 运算符来确定动态分配的数组包含的字节数。

为数组分配内存的通用格式如下:

```txt
type_name * pointer_name = new type_name [num_elements];
```

使用 new 运算符可以确保内存块足以存储 num\_elements 个类型为 type\_name 的元素，而 pointer\_name 将指向第 1 个元素。下面将会看到，可以以使用数组名的方式来使用 pointer\_name。

## 2. 使用动态数组

创建动态数组后，如何使用它呢？首先，从概念上考虑这个问题。下面的语句创建指针 psome，它指向包含 10 个 int 值的内存块中的第 1 个元素:

```typescript
int * psome = new int [10]; // get a block of 10 ints
```

可以将它看作是一根指向该元素的手指。假设 int 占 4 个字节，则将手指沿正确的方向移动 4 个字节，手指将指向第 2 个元素。总共有 10 个元素，这就是手指的移动范围。因此，new 语句提供了识别内存块中每个元素所需的全部信息。

现在从实际角度考虑这个问题。如何访问其中的元素呢？第一个元素不成问题。由于 psome 指向数组的第 1 个元素，因此 \*psome 是第 1 个元素的值。这样，还有 9 个元素。如果没有使用过 C 语言，下面这种最简单的方法可能会令您大吃一惊:只要把指针当作数组名使用即可。也就是说，对于第 1 个元素，可以使用 psome[0]，而不是 \*psome；对于第 2 个元素，可以使用 psome[1]，依此类推。这样，使用指针来访问动态数组就非常简单了，虽然还不知道为何这种方法管用。可以这样做的原因是，C 和 C++ 内部都使用指针来处理数组。数组和指针基本等价是 C 和 C++ 的优点之一（这在有时候也是个问题，但这是另一码事）。稍后将更详细地介绍这种等同性。首先，程序清单 4.18 演示了如何使用 new 来创建动态数组以及使用数组表示法来访问元素；它还指出了指针和真正的数组名之间的根本差别。

程序清单 4.18 arraynew.cpp

```cpp
// arraynew.cpp -- using the new operator for arrays
#include <iostream>
int main()
{
    using namespace std;
    double * p3 = new double [3]; // space for 3 doubles
    p3[0] = 0.2;                      // treat p3 like an array name
    p3[1] = 0.5;
    p3[2] = 0.8;
    cout << "p3[1] is " << p3[1] << ".\n";
    p3 = p3 + 1;                     // increment the pointer
    cout << "Now p3[0] is " << p3[0] << " and ";
    cout << "p3[1] is " << p3[1] << ".\n";
    p3 = p3 - 1;                    // point back to beginning
    delete [] p3;                    // free the memory
    return 0;
}
```

下面是该程序的输出:

```txt
p3[1] is 0.5.
Now p3[0] is 0.5 and p3[1] is 0.8.
```

从中可知，arraynew.cpp 将指针 p3 当作数组名来使用，p3[0] 为第 1 个元素，依次类推。下面的代码行指出了数组名和指针之间的根本差别:

```txt
p3 = p3 + 1; // okay for pointers, wrong for array names
```

不能修改数组名的值。但指针是变量，因此可以修改它的值。请注意将 p3 加 1 的效果。表达式 p3[0] 现在指的是数组的第 2 个值。因此，将 p3 加 1 导致它指向第 2 个元素而不是第 1 个。将它减 1 后，指针将指向原来的值，这样程序便可以给 delete[] 提供正确的地址。

相邻的 int 地址通常相差 2 个字节或 4 个字节，而将 p3 加 1 后，它将指向下一个元素的地址，这表明指针算术有一些特别的地方。情况确实如此。

## 4.8 指针、数组和指针算术

指针和数组基本等价的原因在于指针算术（pointer arithmetic）和 C++ 内部处理数组的方式。首先，我们来看一看算术。将整数变量加 1 后，其值将增加 1；但将指针变量加 1 后，增加的量等于它指向的类型的字节数。将指向 double 的指针加 1 后，如果系统对 double 使用 8 个字节存储，则数值将增加 8；将指向 short 的指针加 1 后，如果系统对 short 使用 2 个字节存储，则指针值将增加 2。程序清单 4.19 演示了这种令人吃惊的现象，它还说明了另一点:C++ 将数组名解释为地址。

程序清单 4.19 addpntrs.cpp

```cpp
// addpntrs.cpp -- pointer addition_
#include <iostream>
int main()
{
    using namespace std;
    double wages[3] = {10000.0, 20000.0, 30000.0};
    short stacks[3] = {3, 2, 1};

// Here are two ways to get the address of an array
    double * pw = wages;      // name of an array = address
    short * ps = &stacks[0]; // or use address operator
// with array element
    cout << "pw = " << pw << ", *pw = " << *pw << endl;
    pw = pw + 1;
    cout << "add 1 to the pw pointer:\n";
    cout << "pw = " << pw << ", *pw = " << *pw << "\n\n";
    cout << "ps = " << ps << ", *ps = " << *ps << endl;
    ps = ps + 1;
    cout << "add 1 to the ps pointer:\n";
    cout << "ps = " << ps << ", *ps = " << *ps << "\n\n";

    cout << "access two elements with array notation\n";
    cout << "stacks[0] = " << stacks[0]
        << ", stacks[1] = " << stacks[1] << endl;
    cout << "access two elements with pointer notation\n";
    cout << "*stacks = " << *stacks
        << ", {*stacks + 1} = " << {*stacks + 1} << endl;

    cout << sizeof(wages) << " = size of wages array\n";
    cout << sizeof(pw) << " = size of pw pointer\n";
    return 0;
}
```

下面是该程序的输出:

```txt
pw = 0x28ccf0, *pw = 10000
add 1 to the pw pointer:
pw = 0x28ccf8, *pw = 20000

ps = 0x28ccea, *ps = 3
add 1 to the ps pointer:
ps = 0x28ccec, *ps = 2

access two elements with array notation
stacks[0] = 3, stacks[1] = 2
access two elements with pointer notation
*stacks = 3, *(stacks + 1) = 2
24 = size of wages array
4 = size of pw pointer
```

## 4.8.1 程序说明

在多数情况下，C++将数组名解释为数组第1个元素的地址。因此，下面的语句将pw声明为指向double

类型的指针，然后将它初始化为 wages——wages 数组中第 1 个元素的地址:

```typescript
double * pw = wages;
```

和所有数组一样，wages也存在下面的等式:

```txt
wages = &wages[0] = address of first element of array
```

为表明情况确实如此, 该程序在表达式&stacks[0]中显式地使用地址运算符来将 ps 指针初始化为 stacks 数组的第 1 个元素。

接下来，程序查看 pw 和 \*pw 的值。前者是地址，后者是存储在该地址中的值。由于 pw 指向第 1 个元素，因此 \*pw 显示的值为第 1 个元素的值，即 10000。接着，程序将 pw 加 1。正如前面指出的，这样数字地址值将增加 8，这使得 pw 的值为第 2 个元素的地址。因此，\*pw 现在的值是 20000——第 2 个元素的值（参见图 4.10，为使改图更为清晰，对其中的地址值做了调整）。

![](images/page_125_image_8.jpg)

<details>
<summary>text_image</summary>

double wages[3] = {10000.0, 20000.0, 30000.0};
short stacks[3] = {3, 2, 1};
double * pw = wages;
short * ps = &stacks[0];

地址:
100
pw
108
(pw + 1)
116
124 126 128
ps
(ps + 1)

pw指向double类型，
因此对pw加1就会让
它的值增加8个字节。

ps指向short类型，因此
对ps加1会让它的值增加
2个字节。
</details>

图4.10 指针加法

此后，程序对 ps 执行相同的操作。这一次由于 ps 指向的是 short 类型，而 short 占用 2 个字节，因此将指针加 1 时，其值将增加 2。结果是，指针也指向数组中下一个元素。

注意:将指针变量加上后，其增加的值等于指向的类型占用的字节数。

现在来看一看数组表达式 stacks[1]。C++编译器将该表达式看作是\*(stacks + 1)，这意味着先计算数组第2个元素的地址，然后找到存储在那里的值。最后的结果便是 stacks[1]的含义（运算符优先级要求使用括号，如果不使用括号，将给\*stacks 加 1，而不是给 stacks 加 1）。

从该程序的输出可知，\*（stacks + 1）和 stacks[1]是等价的。同样，\*（stacks + 2）和 stacks[2]也是等价的。通常，使用数组表示法时，C++都执行下面的转换:

```txt
arrayname[i] becomes *(arrayname + i)
```

如果使用的是指针，而不是数组名，则C++也将执行同样的转换:

```txt
pointername[i] becomes * (pointername + i)
```

因此，在很多情况下，可以相同的方式使用指针名和数组名。对于它们，可以使用数组方括号表示法，也可以使用解除引用运算符（\*）。在多数表达式中，它们都表示地址。区别之一是，可以修改指针的值，而数组名是常量:

```txt
pointername = pointername + 1; // valid
arrayname = arrayname + 1;      // not allowed
```

另一个区别是，对数组应用 sizeof 运算符得到的是数组的长度，而对指针应用 sizeof 得到的是指针的长度，即使指针指向的是一个数组。例如，在程序清单 4.19 中，pw 和 wages 指的是同一个数组，但对它们应用 sizeof 运算符得到的结果如下:

24 = size of wages array << displaying sizeof wages

4 = size of pw pointer << displaying sizeof pw

这种情况下，C++不会将数组名解释为地址。

## 数组的地址

对数组取地址时，数组名也不会被解释为其地址。等等，数组名难道不被解释为数组的地址吗？不完全如此:数组名被解释为其第一个元素的地址，而对数组名应用地址运算符时，得到的是整个数组的地址:

```cpp
short tell[10];          // tell an array of 20 bytes
cout << tell << endl;   // displays &tell[0]
cout << &tell << endl; // displays address of whole array
```

从数字上说，这两个地址相同；但从概念上说，&tell[0]（即 tell）是一个2字节内存块的地址，而&tell是一个20字节内存块的地址。因此，表达式tell+1将地址值加2，而表达式&tell+2将地址加20。换句话说，tell是一个short指针（\*short），而&tell是一个这样的指针，即指向包含20个元素的short数组（short(\*) [20]）。

您可能会问，前面有关&tell的类型描述是如何来的呢？首先，您可以这样声明和初始化这种指针:

short (\*pas)[20] = &tell;  // pas points to array of 20 shorts

如果省略括号，优先级规则将使得 pas 先与[20]结合，导致 pas 是一个 short 指针数组，它包含 20 个元素，因此括号是必不可少的。其次，如果要描述变量的类型，可将声明中的变量名删除。因此，pas 的类型为 short (\*) [20]。另外，由于 pas 被设置为 &tell，因此 \*pas 与 tell 等价，所以 (\*pas) [0] 为 tell 数组的第一个元素。

总之，使用 new 来创建数组以及使用指针来访问不同的元素很简单。只要把指针当作数组名对待即可。然而，要理解为何可以这样做，将是一种挑战。要想真正了解数组和指针，应认真复习它们的相互关系。

## 4.8.2 指针小结

刚才已经介绍了大量指针的知识，下面对指针和数组做一总结。

## 1. 声明指针

要声明指向特定类型的指针，请使用下面的格式:

typeName \* pointerName;

下面是一些示例:

```txt
double * pn;          // pn can point to a double value
char * pc;           // pc can point to a char value
```

其中，pn 和 pc 都是指针，而 double \*和 char \*是指向 double 的指针和指向 char 的指针。

## 2. 给指针赋值

应将内存地址赋给指针。可以对变量名应用&运算符，来获得被命名的内存的地址，new 运算符返回未命名的内存的地址。

下面是一些示例:

```txt
double * pn;          // pn can point to a double value
double * pa;           // so can pa
char * pc;            // pc can point to a char value
double bubble = 3.2;
pn = &bubble;         // assign address of bubble to pn
pc = new char;       // assign address of newly allocated char memory to pc
pa = new double[30];   // assign address of 1st element of array of 30 double to pa
```

## 3. 对指针解除引用

对指针解除引用意味着获得指针指向的值。对指针应用解除引用或间接值运算符（\*）来解除引用。因此，如果像上面的例子中那样，pn 是指向 bubble 的指针，则 \*pn 是指向的值，即 3.2。

下面是一些示例:

```txt
cout << *pn; // print the value of bubble
*pc = 'S';   // place 'S' into the memory location whose address is pc
```

另一种对指针解除引用的方法是使用数组表示法，例如，pn[0]与\*pn是一样的。决不要对未被初始化为适当地址的指针解除引用。

## 4. 区分指针和指针所指向的值

如果 pt 是指向 int 的指针，则\*pt 不是指向 int 的指针，而是完全等同于一个 int 类型的变量。pt 才是指针。下面是一些示例:

```txt
int * pt = new int;      // assigns an address to the pointer pt
*pt = 5;                     // stores the value 5 at that address
```

## 5. 数组名

在多数情况下，C++将数组名视为数组的第一个元素的地址。

下面是一个示例:

```javascript
int tacos[10];          // now tacos is the same as &tacos[0]
```

一种例外情况是，将 sizeof 运算符用于数组名用时，此时将返回整个数组的长度（单位为字节）。

## 6. 指针算术

C++允许将指针和整数相加。加1的结果等于原来的地址值加上指向的对象占用的总字节数。还可以将一个指针减去另一个指针，获得两个指针的差。后一种运算将得到一个整数，仅当两个指针指向同一个数组（也可以指向超出结尾的一个位置）时，这种运算才有意义；这将得到两个元素的间隔。

下面是一些示例:

```c
int tacos[10] = {5,2,8,4,1,2,2,4,6,8};
int * pt = tacos;          // suppose pf and tacos are the address 3000
pt = pt + 1;               // now pt is 3004 if a int is 4 bytes
int *pe = &tacos[9];     // pe is 3036 if an int is 4 bytes
pe = pe - 1;                 // now pe is 3032, the address of tacos[8]
int diff = pe - pt;      // diff is 7, the separation between
                                // tacos[8] and tacos[1]
```

## 7. 数组的动态联编和静态联编

使用数组声明来创建数组时，将采用静态联编，即数组的长度在编译时设置:

```txt
int tacos[10]; // static binding, size fixed at compile time
```

使用 new[] 运算符创建数组时，将采用动态联编（动态数组），即将在运行时为数组分配空间，其长度也将在运行时设置。使用完这种数组后，应使用 delete[] 释放其占用的内存:

```txt
int size;
cin >> size;
int * pz = new int [size];   // dynamic binding, size set at run time
...
delete [] pz;                     // free memory when finished
```

## 8. 数组表示法和指针表示法

使用方括号数组表示法等同于对指针解除引用: