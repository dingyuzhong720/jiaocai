相对于文件开始处的偏移量。常量 ios\_base::cur 指相对于当前位置的偏移量；常量 ios\_base::end 指相对于文件尾的偏移量。下面是一些调用示例，这里假设 fin 是一个 ifstream 对象:

```rust
fin.seekg(30, ios_base::beg);    // 30 bytes beyond the beginning
fin.seekg(-1, ios_base::cur);    // back up one byte
fin.seekg(0, ios_base::end);    // go to the end of the file
```

下面来看第二个原型。streampos 类型的值定位到文件中的一个位置。它可以是类，但如果是这样的话，这个类将包含一个接受 streamoff 参数的构造函数和一个接受整数参数的构造函数，以便将两种类型转换为 streampos 值。streampos 值表示文件中的绝对位置（从文件开始处算起）。可以将 streampos 位置看作是相对于文件开始处的位置（以字节为单位，第一个字节的编号为 0）。因此下面的语句将文件指针指向第 112 个字节，这是文件中的第 113 个字节:

```javascript
fin.seekg(112);
```

如果要检查文件指针的当前位置，则对于输入流，可以使用 tellg() 方法，对于输出流，可以使用 tellp() 方法。它们都返回一个表示当前位置的 streampos 值（以字节为单位，从文件开始处算起）。创建 fstream 对象时，输入指针和输出指针将一前一后地移动，因此 tellg() 和 tellp() 返回的值相同。然而，如果使用 istream 对象来管理输入流，而使用 ostream 对象来管理同一个文件的输出流，则输入指针和输出指针将彼此独立地移动，因此 tellg() 和 tellp() 将返回不同的值。

然后，可以使用 seekg()移到文件的开头。下面是打开文件、移到文件开头并显示文件内容的代码片段:

```cpp
fstream finout;      // read and write streams
finout.open(file,ios::in | ios::out |ios::binary);
//NOTE: Some Unix systems require omitting | ios::binary
int ct = 0;
if (finout.is_open())
{
    finout.seekg(0);     // go to beginning
    cout << "Here are the current contents of the "
           << file << " file:\n";
    while (finout.read((char *) &pl, sizeof pl))
    {
        cout << ct++ << ": " << setw(LIM) << pl.name << ": "
            << setprecision(0) << setw(12) << pl.population
            << setprecision(2) << setw(6) << pl.g << endl;
    }
    if (finout.eof())
        finout.clear(); // clear eof flag
    else
    {
        cerr << "Error in reading " << file << ".\n";
        exit(EXIT_FAILURE);
    }
}
else
{
    cerr << file << " could not be opened -- bye.\n";
    exit(EXIT_FAILURE);
}
```

这与程序清单 17.19 的开头很相似，但也修改和添加了一些内容。首先，程序以读/写模式使用一个fstream对象，并使用 seekg() 将文件指针放在文件开头（对于这个例子而言，这其实不是必须的，但它说明了如何使用 seekg()）。接下来，程序在给记录编号方面做了一些小的改动。然后添加了以下重要的代码:

```txt
if (finout.eof())
    finout.clear() // clear eof flag
else
{
    cerr << "Error_in_reading " << file << "\n"
    exit(EXIT_FAILURE);
}
```

上述代码解决的问题是，程序读取并显示整个文件后，将设置cofbit元素。这使程序相信，它已经处理完文件，并禁止对文件做进一步的读写。使用clear()方法重置流状态，并打开cofbit后，程序便可以再次访问该文件。else部分处理程序因到达文件尾之外的其他原因（如硬件故障）而停止读取的情况。

接下来需要确定要修改的记录，并修改它。为此，程序让用户输入记录号。将该编号与记录包含的字节数相乘，得到该记录第一个字节的编号。如果 record 是记录号，则字节编号为 record \* sizeof.pl:

```cpp
cout << "Enter the record number you wish to change: ";
long rec;
cin >> rec;
eatline();          // get rid of newline
if (rec < 0 || rec >= ct)
{
    cerr << "Invalid record number -- bye\n";
    exit(EXIT_FAILURE);
}
streampos place = rec * sizeof pl; // convert to streampos type
finout.seekg(place);   // random access
```

变量 ct 表示记录号。如果试图超出文件尾，程序将退出。

接下来，程序显示当前的记录:

```cpp
finout.read((char *) &pl, sizeof pl);
cout << "Your selection:\n";
cout << rec << ":" << setw(LIM) << pI.name << ": "
<< setprecision(0) << setw(12) << pl.population
<< setprecision(2) << setw(6) << pl.g << endl;
if (finout.eof())
    finout.clear();      // clear eof flag
```

显示记录后，程序让您修改记录:

```txt
cout << "Enter planet name: ";
cin.get( pl.name, LIME);
eatline();
cout << "Enter planetary population: ";
cin >> pl.population;
cout << "Enter planet's acceleration of gravity: ";
cin >> pl.g;
finout.seekp(place); // go back
finout.write((char *) &pl, sizeof pl) << flush;

if (finout.fail())
{
    cert << "Error on -attempted write\n";
    exit(EXIT_FAILURE);
}
```

=程序刷新输出，以确保进入下一步之前，文件被更新。

最后，为显示修改后的文件，程序使用seekg()将文件指针重新指向开头。程序清单17.20列出了完整

的程序。不要忘了，该程序假设 binary.cpp 创建的 planets.dat 文件是可用的。

注意:实现越旧，与 C++ 标准相冲突的可能性越大。一些系统不能识别二进制标记、fixed 和 right 控制符以及 ios\_base。

程序清单 17.20 random.cpp

```cpp
// random.cpp -- random access to a binary file
#include <iostream>      // not required by most systems
#include <fstream>
#include <iomanip>
#include <cstdlib>          // for exit()
const int LIM = 20;
struct planet
{
    char name[LIM];      // name of planet
    double population;   // its population
    double g;          // its acceleration of gravity
};

const char * file = "planets.dat"; // ASSUMED TO EXIST (binary.cpp example)
inline void eatline() { while (std::cin.get() != '\n') continue; }

int main()
{
    using namespace std;
    planet.pl;
    cout << fixed;

// show initial contents
    fstream finout;     // read and write streams
    finout.open(file,
        ios_base::in | ios_base::out | ios_base::binary);
    //NOTE: Some Unix systems require omitting | ios::binary
    int ct = 0;
    if (finout.is_open())
    {
        finout.seekg(0);      // go to beginning
        cout << "Here are the current contents of the "
            << file << " file:\n";
        while (finout.read((char *) &pl, sizeof.pl))
        {
            cout << ct++ << ": " << setw(LIM) << pl.name << " : "
                << setprecision(0) << setw(12) << pl.population
                << setprecision(2) << setw(6) << pl.g << endl;
        }
        if (finout.eof())
            finout.clear(-); // clear eof flag
        else
        {
            cerr << "Error in reading " << file << ".\n";
            exit(EXIT_FAILURE);
        }
    }
else
```

```cpp
{
    cerr << file << "could not be opened -- bye.\n";
    exit(EXIT_FAILURE);
}

// change a record
    cout << "Enter the record number you wish to change=";
    long rec;
    cin >> rec;
    eatline();          // get rid of newline
    if (rec < 0 || rec >= ct)
    {
        cerr << "Invalid record number -- bye\n";
        exit(EXIT_FAILURE);
    }
    streampos place = rec * sizeof pl; // convert to streampos type
    finout.seekg(place);   // random access
    if (finout.fail()) {
        cerr << "Error on attempted seek\n";
        exit(EXIT_FAILURE);
    }
    finout.read((char *) &pl, sizeof pl);
    cout << "Your selection:\n";
    cout << rec << ": " << setw(LIM) << pl.name << ": "
        << setprecision(0) << setw(12) << pl.population
        << setprecision(2) << setw(6) << pl.g << endl;
    if (finout.eof()) {
        finout.clear();      // clear eof_flag
        cout << "Enter planet name: ";
        cin.get(pl.name, LIM);
        eatline();
        cout << "Enter planetary population: ";
        cin >> pl.population;
        cout << "Enter planet's acceleration of gravity: ";
        cin >> pl.g;
        finout.seekp(place);     // go back
        finout.write((char *) &pl, sizeof_pl) << flush;
        if (finout.fail()) {
            cerr << "Error on attempted write\n";
            exit(EXIT_FAILURE);
        }
}
// show revised file
    ct = 0;
    finout.seekg(0);          // go to beginning of file
    cout << "Here are the new contents of the " << file
        << " file:\n";
    while (finout.read((char *) &pl, sizeof pl))
    {
        cout << ct++ << ": " << setw(LIM) << pl.name << ": "
            << setprecision(0) << setw(12) << pl.population
```

```cpp
<< setprecision(2) << setw(6) << p1=g << endl;
    }
    finout.close()-;
    cout << "Done.\n";
    return 0;   -
}
```

下面是程序清单 17.20 中的程序基于 planets.dat 文件的运行情况，该文件比上次见到时多了一些条目:

```txt
Here are the current contents of the planets.dat file:
0:           Earth: 6928198253 9.81 -
1:           Jenny's World: 32155648 8.93
2:            Tramtor: 89000000000 15.03
3:            Trellan:   5214000 9.62
4:            Freestone: 3945851000 8.68
5:            Taanagoot: 361000004 10.23
6:            Marin:   252409 9.79   - -
Enter the record number you wish to change: 2
Your selection:
2:           Tramtor: 89000000000 15.03
Enter planet name: Trantor
Enter planetary population: 89521844777
Enter planet's acceleration of gravity: 10.53
Here are the new contents of the planets.dat file:
0:           Earth: 6928198253 9.81
1:           Jenny's World:   32155648 8.93
2:            Trantor: 89521844777 10.53
3:            Trellan:   5214000 9.62
4:            Freestone: 3945851000 8.68
5:            Taanagoot:   361000004 10.23
6:            Marin:   252409 9.79
Done.
```

通过使用该程序中的技术，对其进行扩展，使之能够让用户添加新信息和删除记录。如果打算扩展该程序，最好通过使用类和函数来重新组织它。例如，可以将 planet 结构转换为一个类定义，然后对<<插入运算符进行重载，使得 cout<<pl 按示例的格式显示类的数据成员。另外，该示例没有对输入进行检查，您可以添加代码来检查数值输入是否合适。

## 使用临时文件

开发应用程序时，经常需要使用临时文件，这种文件的存在是短暂的，必须受程序控制。您是否考虑过，在 C++ 中如何使用临时文件呢？创建临时文件、复制另一个文件的内容并删除文件其实都很简单。首先，需要为临时文件制定一个命名方案，但如何确保每个文件都被指定了独一无二的文件名呢？cstdio 中声明的 tmpnam() 标准函数可以帮助您。

```javascript
char* tmpnam( char* pszName );
```

tmpnam()函数创建一个临时文件名，将它放在pszName指向的C-风格字符串中。常量L\_tmpnam和TMP\_MAX（二者都是在cstdio中定义的）限制了文件名包含的字符数以及在确保当前目录中不生成重复文件名的情况下tmpnam()可被调用的最多次数。下面是生成10个临时文件名的代码。

```cpp
#include <cstdio>
#include <iostream>

int main()
{
    using namespace std;
```

```cpp
cout << "This system can generate up to " << TMP_MAX
        << " temporary names of up to " << L_tmpnam
        << " characters.\n";
    char pszName[ L_tmpnam ] = {'\0'};
    cout << "Here are ten names:\n";
    for( int i=0; 10 > i; i++ )
    {
        tmpnam( pszName );
        cout << pszName << endl;
    }
    return 0;
}
```

更具体地说，使用 tmpnam() 可以生成 TMP\_NAM 个不同的文件名，其中每个文件名包含的字符不超过 L\_tmpnam 个。生成什么样的文件名取决于实现，您可以运行该程序，来看看编译器给您生成的文件名。

## 17.5 内核格式化

iostream 族（family）支持程序与终端之间的 I/O，而 fstream 族使用相同的接口提供程序和文件之间的 I/O。C++ 库还提供了 sstream 族，它们使用相同的接口提供程序和 string 对象之间的 I/O。也就是说，可以使用于 cout 的 ostream 方法将格式化信息写入到 string 对象中，并使用 istream 方法（如 getline()）来读取 string 对象中的信息。读取 string 对象中的格式化信息或将格式化信息写入 string 对象中被称为内核格式化（incore formatting）。下面简要地介绍一下这些工具（string 的 sstream 族支持取代了 char 数组的 strstream.h 族支持）。

头文件 sstream 定义了一个从 ostream 类派生而来的 ostringstream 类（还有一个基于 wostream 的 wostringstream 类，这个类用于宽字符集）。如果创建了一个 ostringstream 对象，则可以将信息写入其中，它将存储这些信息。可以将可用于 cout 的方法用于 ostringstream 对象。也就是说，可以这样做:

```html
ostringstream outstr;
double price = 380.0;
char * ps = " for a copy of the ISO/EIC C++ standard!";
outstr.precision(2);
outstr << fixed;
outstr << "Pay only CHF " << price << ps << endl;
```

格式化文本进入缓冲区，在需要的情况下，该对象将使用动态内存分配来增大缓冲区。ostringstream 类有一个名为 str() 的成员函数，该函数返回一个被初始化为缓冲区内容的字符串对象:

```java
string mesg = outstr.str();    // returns string with formatted information
```

使用 str() 方法可以 “冻结” 该对象，这样便不能将信息写入该对象中。

程序清单 17.21 是一个有关内核格式化的简短示例。

程序清单 17.21  strut.cpp

```cpp
// trout.cpp -- incore formatting (output)
#include <iostream>
#include <sstream>
#include <string>
int main()
{
    using namespace std;
    ostringstream outstr;   // manages a string stream
```

```txt
string hdisk;
cout << "What's the name of your hard disk? ";
getline(cin, hdisk);
int cap;
cout << "What's its capacity in GB? ";
cin >> cap;
// write formatted information to string stream
outstr << "The hard disk " << hdisk << " has a capacity of "
       << cap << " gigabytes.\n";
string result = outstr.str();   // save result
cout << result;                  // show contents

return 0;

}
```

下面是程序清单 17.21 中程序的运行情况:

```txt
What's the name of your hard disk? Datarapture
What's its capacity in GB? 2000
The hard disk Datarapture has a capacity of 2000 gigabytes.
```

istringsstream 类允许使用 istream 方法族读取 istringsstream 对象中的数据，istringsstream 对象可以使用 string 对象进行初始化。

假设 facts 是一个 string 对象，则要创建与该字符串相关联的 istringsstream 对象，可以这样做:istringsstream instr(facts); // use facts to initialize stream

这样，便可以使用 istream 方法读取 instr 中的数据。例如，如果 instr 包含大量字符格式的整数，则可以这样读取它们:

```txt
int n;
int sum = 0;
while (instr >> n)
    sum += n;
```

程序清单 17.22 使用重载的>>运算符读取字符串中的内容，每次读取一个单词

程序清单 17.22 strin.cpp

```cpp
// strin.cpp -- formatted reading from a char array
#include <iostream>
#include <sstream>
#include <string>
int main()
{
    using namespace std;
    string lit = "It was a dark and stormy day, and"
        "-the full moon glowed brilliantly."]
    istringsstream instr(lit); // use buf for input
    string word;
    while-(instr >> word)      // read a word a time
        cout << word << endl;
    return 0;
}
```

下面是程序清单 F7.22 中程序的输出:

```ignorefile
It
was
a
dark
and
stormy
day,
and
the
full
moon
glowed
brilliantly.
```

总之，istringstream 和 ostringstream 类使得能够使用 istream 和 ostream 类的方法来管理存储在字符串中的字符数据。

## 17.6 总结

流是进出程序的字节流。缓冲区是内存中的临时存储区域，是程序与文件或其他I/O设备之间的桥梁。信息在缓冲区和文件之间传输时，将使用设备（如磁盘驱动器）处理效率最高的尺寸以大块数据的方式进行传输。信息在缓冲区和程序之间传输时，是逐字节传输的，这种方式对于程序中的处理操作更为方便。C++通过将一个被缓冲流同程序及其输入源相连来处理输入。同样，C++也通过将一个被缓冲流与程序及其输出目标相连来处理输出。iostream和fstream文件构成了I/O类库，该类库定义了大量用于管理流的类。包含了iostream文件的C++程序将自动打开8个流，并使用8个对象管理它们。cin对象管理标准输入流，后者默认与标准输入设备（通常为键盘）相连；cout对象管理标准输出流，后者默认与标准输出设备（通常为显示器）相连；cerr和clog对象管理与标准错误设备（通常为显示器）相连的未被缓冲的流和被缓冲的流。这4个对象有都有用于宽字符的副本，它们是wcin、wcout、wcerr和wclog。

I/O 类库提供了大量有用的方法。istream 类定义了多个版本的抽取运算符（>>），用于识别所有基本的 C++类型，并将字符输入转换为这些类型。get()方法族和 getline()方法为单字符输入和字符串输入提供了进一步的支持。同样，ostream 类定义了多个版本的插入运算符（<<），用于识别所有的 C++基本类型，并将它们转换为相应的字符输出。put()方法对单字符输出提供了进一步的支持。wistream 和 wostream 类对宽字符提供了类似的支持。

使用 ios\_base 类方法以及文件 iostream 和 iomanip 中定义的控制符（可与插入运算符拼接的函数），可以控制程序如何格式化输出。这些方法和控制符使得能够控制计数系统、字段宽度、小数位数、显示浮点变量时采用的计数系统以及其他元素。

fstream 文件提供了将 iostream 方法扩展到文件 I/O 的类定义。ifstream 类是从 istream 类派生而来的。通过将 ifstream 对象与文件关联起来，可以使用所有的 istream 方法来读取文件。同样，通过将 ofstream 对象与文件关联起来，可以使用 ostream 方法来写文件；通过将 fstream 对象与文件关联起来，可以将输入和输出方法用于文件。

要将文件与流关联起来，可以在初始化文件流对象时提供文件名，也可以先创建一个文件流对象，然后用 open() 方法将这个流与文件关联起来。close() 方法终止流与文件之间的连接。类构造函数和 open() 方法接受可选的第二个参数，该参数提供文件模式。文件模式决定文件是否被读和/或写、打开文件以便写入时是否截短文件、试图打开不存在的文件时是否会导致错误、是使用二进制模式还是文本模式等。

文本文件以字符格式存储所有的信息，例如，数字值将被转换为字符表示。常规的插入和抽取运算符以及 get() 和 getline() 都支持这种模式。二进制文件使用计算机内部使用的二进制表示来存储信息。与文本文件相比，二进制文件存储数据（尤其是浮点值）更为精确、简洁，但可移植性较差。read() 和 write() 方

法都支持二进制输入和输出。

seekg()和 seekp()函数提供对文件的随机存取。这些类方法使得能够将文件指针放置到相对于文件开头、文件尾和当前位置的某个位置。tellg()和 tellp()方法报告当前的文件位置。

sstream 头文件定义了 istringstream 和 ostringstream 类，这些类使得能够使用 istream 和 ostream 方法来抽取字符串中的信息，并对要放入到字符串中的信息进行格式化。

## 17.7 复习题

1. iostream 文件在 C++ I/O 中扮演何种角色？
2. 为什么键入数字（如121）作为输入要求程序进行转换？
3. 标准输出与标准错误之间有什么区别？
4. 为什么在不为每个类型提供明确指示的情况下，cout 仍能够显示不同的 C++ 类型？
5. 输出方法的定义的哪一特征让您能够拼接输出？

6. 编写一个程序，要求用户输入一个整数，然后以十进制、八进制和十六进制显示该整数。在宽度为15个字符的字段中显示每种形式，并将它们显示在同一行上，同时使用C++数基前缀。

7. 编写一个程序，请求用户输入下面的信息，并按下面的格式显示它们:

```txt
Enter your name: Billy Gruff
Enter your hourly wages: 12
Enter number of hours worked: 7.5
First format:
            Billy Gruff: $      12.00:  7.5
Second format:
Billy Gruff                  : $12.00     :7.5
```

8. 对于下面的程序:

```cpp
//rql7-8.cpp
#include <iostream>

int main()
{
    using namespace std;
    char ch;
    int ctl = 0;

    cin >> ch;
    while (ch != 'q')
    {
        ctl++;
        cin >> ch;
    }

    int ctl2 = 0;
    cin.get(ch);
    while (ch != 'q')
    {
        ctl2++;
        cin.get(ch);
    }
    cout << "ctl = " << ctl << "; ctl2 = " << ctl2 << "\n";
```

```scss
return 0;
}
```

如果输入如下，该程序将打印什么内容？

```txt
I see a q<Enter>
I see a q<Enter>
```

其中，&lt;Enter&gt;表示按回车键。

9. 下面的两条语句都读取并丢弃行尾之前的所有字符（包括行尾）。这两条语句的行为在哪方面不同？

```javascript
while (cin.get() != '\n')
    continue;
cin.ignore(80, '\n');
```

## 17.8 编程练习

1. 编写一个程序计算输入流中第一个\$之前的字符数目，并将\$留在输入流中。
2. 编写一个程序，将键盘输入（直到模拟的文件尾）复制到通过命令行指定的文件中。
3. 编写一个程序，将一个文件复制到另一个文件中。让程序通过命令行获取文件名。如果文件无法打开，程序将指出这一点。
4. 编写一个程序，它打开两个文本文件进行输入，打开一个文本文件进行输出。该程序将两个输入文件中对应的行并接起来，并用空格分隔，然后将结果写入到输出文件中。如果一个文件比另一个短，则将较长文件中余下的几行直接复制到输出文件中。例如，假设第一个输入文件的内容如下:

```txt
eggs kites donuts
balloons hammers
stones
```

而第二个输入文件的内容如下:

```txt
zero lassitude
finance drama
```

则得到的文件的内容将如下:

```txt
eggs kites donuts zero lassitude
balloons hammers finance drama
stones
```

5. Mat 和 Pat 想邀请他们的朋友来参加派对，就像第 16 章中的编程练习 8 那样，但现在他们希望程序使用文件。他们请您编写一个完成下述任务的程序。

- 从文本文件 mat.dat 中读取 Mat 朋友的姓名清单，其中每行为一个朋友。姓名将被存储在容器，然后按顺序显示出来。
- 从文本文件 pat.dat 中读取 Pat 朋友的姓名清单，其中每行为一个朋友。姓名将被存储在容器中，然后按顺序显示出来。
- 合并两个清单，删除重复的条目，并将结果保存在文件 matnpat.dat 中，其中每行为一个朋友。

6. 考虑 14 章的编程练习 5 中的类定义。如果还没有完成这个练习，请现在就做，然后完成下面的任务。

编写一个程序，它使用标准 C++ I/O、文件 I/O 以及 14 章的编程练习 5 中定义的 employee、manager、fink 和 highfink 类型的数据。该程序应包含程序清单 17.17 中的代码行，即允许用户将新数据添加到文件中。该程序首次被运行时，将要求用户输入数据，然后显示所有的数据，并将这些信息保存到一个文件中。当该程序再次被运行时，将首先读取并显示文件中的数据，然后让用户添加数据，并显示所有的数据。差别之一是，应通过一个指向 employee 类型的指针数组来处理数据。这样，指针可以指向 employee 对象，也可以指向从 employee 派生出来的其他三种对象中的任何一种。使数组较小有助于检查程序，例如，您可能将数组限定为最多包含 10 个元素:

```txt
const int MAX = 10;      // no more than 10 objects
...
employee * pc[MAX];
```

为通过键盘输入，程序应使用一个菜单，让用户选择要创建的对象类型。菜单将使用一个 switch，以便使用 new 来创建指定类型的对象，并将它的地址赋给 pc 数组中的一个指针。然后该对象可以使用虚函数 setall()来提示用户输入相应的数据:

```javascript
pc[i]->setall();  // invokes function corresponding to type of object
```

为将数据保存到文件中，应设计一个虚函数 writeall():

```c
for (i = 0; i < index; i++)
    pc[i]->writeall(fout);// fout ofstream connected to output file
```

注意:对于这个练习，应使用文本 I/O，而不是二进制 I/O（遗憾的是，虚对象包含指向虚函数指针表的指针，而 write() 将把这种信息复制到文件中。使用 read() 读取文件的内容，以填充对象时，函数指针值将为乱码，这将扰乱虚函数的行为）。可使用换行符将字段分隔开，这样在输入时将很容易识别各个字段。也可以使用二进制 I/O，但不能将对象作为一个整体写入，而应该提供分别对每个类成员应用 write() 和 read() 的类方法。这样，程序将只把所需的数据保存到文件中。

比较难处理的部分是使用文件恢复数据。问题在于:程序如何才能知道接下来要恢复的项目是 employee 对象、manager 对象、fink 对象还是 highfink 对象？一种方法是，在对象的数据写入文件时，在数据前面加上一个指示对象类型的整数。这样，在文件输入时，程序便可以读取该整数，并使用 switch 语句创建一个适当的对象来接收数据:

```txt
enum classkind{Employee, Manager, Fink, Highfink}; // in class header
...
int classtype;
while((fin >> classtype).get(ch)){ // newline separates int from data
    switch(classtype) {
        case Employee : pc[i] = new employee;
            : break;
```

然后便可以使用指针调用虚函数 getall() 来读取信息:

```javascript
pc[i++] ->getall();
```

7. 下面是某个程序的部分代码。该程序将键盘输入读取到一个由 string 对象组成的 vector 中，将字符串内容（而不是 string 对象）存储到一个文件中，然后该文件的内容复制到另一个由 string 对象组成的 vector 中。

```cpp
int main()
{
    using namespace std;
    vector<string> vostr;
    string temp;

// acquire strings
    cout << "Enter strings (empty line to quit):\n";
    while (getline(cin,temp) && temp[0] != '\0')
        vostr.push_back(temp);
    cout << "Here is your input.\n";
    for_each(vostr.begin(), vostr.end(), ShowStr);
```

```cpp
// store in a file
    ofstream fout("strings.dat", ios_base::out{| ios_base::binary};
    for_each(vostr.begin(), vostr.end(), Store(fout)};
    fout.close();
// recover file contents
    vector<string> vistr;
    ifstream fin("strings.dat", ios_base::in | ios_base::binary};
    if (!fin.is_open(){
        {
            cerr << "Could not open file for input.\n";
            exit(EXIT_FAILURE);
        }
        GetStrs(fin, vistr);
        cout << "\nHere are the strings read from the file:\n";
        for_each(vistr.begin(), vistr.end(), ShowStr);

        return 0;
}
```

该程序以二进制格式打开文件，并想使用 read() 和 write() 来完成 I/O。余下的工作如下所述。

- 编写函数 void ShowStr(const string &), 它显示一个 string 对象, 并在显示完后换行。
- 编写函数符 Store，它将字符串信息写入到文件中。Store 的构造函数应接受一个指定 ifstream 对象的参数，而重载的 operator()(const string &) 应指出要写入到文件中的字符串。一种可行的计划是，首先将字符串的长度写入到文件中，然后将字符串的内容写入到文件中。例如，如果 len 存储了字符串的长度，可以这样做:

```cpp
os.write((char *)&len, sizeof(std::size_t));  // store length
os.write(s.data(), len);                     // store characters
```

成员函数 data() 返回一个指针，该指针指向一个其中存储了字符串中字符的数组。它类似于成员函数 c\_str()，只是后者在数组末尾加上了一个空字符。

\- 编写函数 GetStrs()，它根据文件恢复信息。该函数可以使用 read() 来获得字符串的长度，然后使用一个循环从文件中读取相应数量的字符，并将它们附加到一个原来为空的临时 string 末尾。由于 string 的数据是私有的，因此必须使用 string 类的方法来将数据存储到 string 对象中，而不能直接存储。

# 第18章 探讨C++新标准

本章首先复习前面介绍过的 C++11 功能，然后介绍如下主题:

- 移动语义和右值引用。
- Lambda 表达式。
- 包装器模板 function。
- 可变参数模板。

本章重点介绍 C++11 对 C++ 所做的改进。本书前面介绍过多项 C++11 功能，本章首先复习这些功能，并详细介绍其他一些功能。然后，指出一些超出了本书范围的 C++11 新增功能（考虑到 C++11 草案的篇幅比 C++98 长 98%，本书无法全面介绍）。最后，将简要地探讨 BOOST 库。

## 18.复习前面介绍过的C++11功能

本书前面介绍过很多 C++11 改进，但您现在可能忘了，本节简要地复习这些改进。

## 18.1.1 新类型

C++11 新增了类型 long long 和 unsigned long long，以支持 64 位（或更宽）的整型；新增了类型 char16\_t 和 char32\_t，以支持 16 位和 32 位的字符表示，还新增了“原始”字符串。第 3 章讨论了这些新增的类型。

## 18.8.2 统一的初始化

€++11 扩大了用大括号括起的列表（初始化列表）的适用范围，使其可用于所有内置类型和用户定义的类型（即类对象）。使用初始化列表时，可添加等号（=），也可不添加:

```javascript
int x = {5};
double y {2.75};
short quar[5] {4,5,2,76,1};
```

另外，列表初始化语法也可用于 new 表达式中:

```txt
int * ar= new int [4] {2,4,6,7}; // C++11
```

创建对象时，也可使用大括号（而不是圆括号）括起的列表来调用构造函数:

```txt
class Stump-
{
private:
    int roots;
    double weight;
public:
    Stump(int r, double w) : roots(r), weight(w) {}
};
```

```javascript
Stump s1{3,15.6};      // old style
Stump s2{5, 43.4};     // C++11
Stump s3 = {4, 32.1};   // C++11
```

然而，如果类有将模板 std::initializer\_list 作为参数的构造函数，则只有该构造函数可以使用列表初始化形式。第 3 章、4 章、9 章、10 章和第 16 章讨论了列表初始化的各个方面。

## 1. 缩窄

初始化列表语法可防止缩窄，即禁止将数值赋给无法存储它的数值变量。常规初始化允许程序员执行可能没有意义的操作:

```txt
char c1 = 1.57e27;   // double-to-char, undefined behavior
char c2 = 459585821; // int-to-char, undefined behavior
```

然而，如果使用初始化列表语法，编译器将禁止进行这样的类型转换，即将值存储到比它“窄”的变量中:

```javascript
char c1 {1.57e27};      // double-to-char, compile-time error
char c2 = {459585821};// int-to-char,out of range, compile-time error
```

但允许转换为更宽的类型。另外，只要值在较窄类型的取值范围内，将其转换为较窄的类型也是允许的:

```txt
char c1 {66};      // int-to-char, in range, allowed
double c2 = {66}; // int-to-double, allowed
```

## 2. std::initializer\_list

C++11 提供了模板类 initializer\_list，可将其用作构造函数的参数，这在第 16 章讨论过。如果类有接受 initializer\_list 作为参数的构造函数，则初始化列表语法就只能用于该构造函数。列表中的元素必须是同一种类型或可转换为同一种类型。STL 容器提供了将 initializer\_list 作为参数的构造函数:

```txt
vector<int> a1(10);    // uninitialized vector with 10 elements
vector<int> a2{10};    // initializer-list, a2 has 1 element set to 10
vector<int> a3{4,6,1}; // 3 elements set to 4,6,1
```

头文件 initializer\_list 提供了对模板类 initializer\_list 的支持。这个类包含成员函数 begin() 和 end()，可用于获悉列表的范围。除用于构造函数外，还可将 initializer\_list 用作常规函数的参数:

```cpp
#include <initializer_list>
double sum(std::initializer_list<double> il);
int main()
{
    double total = sum({2.5,3..1,4});  //4 converted to 4.0
}
double sum(std::initializer_list<double> il)
{
    double tot = 0;
    for (auto p = il.begin(); p-!=il.end(); p++)
        tot += *p;
    return tot;
}
```

## 18.1.3 声明

C++11 提供了多种简化声明的功能，尤其在使用模板时。

## 1. auto

以前，关键字 auto 是一个存储类型说明符（见第 9 章），C++11 将其用于实现自动类型推断（见第 3 章）。这要求进行显式初始化，让编译器能够将变量的类型设置为初始值的类型:

```c
auto maton = 112;   // maton is type int
auto pt = &maton;   // pt is type int *
double fm(double, int);
auto pf = fm;       // pf is type double (*)(double,int)
```

关键字 auto 还可简化模板声明。例如，如果 il 是一个 std::initializer\_list&lt;double&gt;对象，则可将下述代码:

```cpp
for (std::initializer_list<double>::iterator p = il.begin();
                   p !=il.end(); p++)
```

替换为如下代码:

```javascript
for (auto p = il.begin(); p !=il.end(); p++)
```

## 2. decltype

关键字 decltype 将变量的类型声明为表达式指定的类型。下面的语句的含义是，让 y 的类型与 x 相同，其中 x 是一个表达式:

```javascript
decltype(x) y;
```

下面是几个示例:

```txt
double x;
int n;
decltype(x*n) q; // q same type as x*n, i.e., double
decltype(&x) pd; // pd same as &x, i.e., double *
```

这在定义模板时特别有用，因为只有等到模板被实例化时才能确定类型:

```txt
template<typename T, typename U)
void ef(T t, U u)
{
    decltype(T*U) tu;
    ...
}
```

其中 tu 将为表达式 T\*U 的类型，这里假定定义了运算 T\*U。例如，如果 T 为 char，U 为 short，则 tu 将为 int，这是由整型算术自动执行整型提升导致的。

decltype 的工作原理比 auto 复杂，根据使用的表达式，指定的类型可以为引用和 const。下面是几个示例:

```cpp
int j = 3;
int &k = j
const int &n = j;
decltype(n) i1;      // i1 type const int &
decltype(j) i2;       // i2 type int
decltype((j)) i3;   // i3 type int &
decltype(k + 1) i4;  // i4 type int
```

有关导致上述结果的规则的详细信息，请参阅第8章。

## 3. 返回类型后置

C++11 新增了一种函数声明语法:在函数名和参数列表后面（而不是前面）指定返回类型:

```cpp
double f1(double, int);          // traditional syntax
auto f2(double, int) -> double;  // new syntax, return type is double
```

就常规函数的可读性而言，这种新语法好像是倒退，但让您能够使用 decltype 来指定模板函数的返回类型:

```txt
template<typename T, typename=U}_ _
auto eff(T t, U u)^ -> dec1type(T*U)-{
    ...  - -  - -      -
}   _
```

这里解决的问题是，在编译器遇到 eff 的参数列表前，T 和 U 还不在作用域内，因此必须在参数列表后使用 decltype。这种新语法使得能够这样做。

## 4. 模板别名:using =

对于冗长或复杂的标识符，如果能够创建其别名将很方便。以前，€++为此提供了typedef:

```rust
typedef std::vector<std::string>::iterator.itType;
```

C++11 提供了另一种创建别名的语法，这在第 14 章讨论过:

```txt
using LossType = std::vector<std::string>::iterator;
```

差别在于，新语法也可用于模板部分具体化，但 typedef 不能:

```cpp
template<typename T>
  using arr12 = std::array<T,12>,- // template for multiple aliases
```

上述语句具体化模板 array&lt;T, int&gt;(将参数 int 设置为 12)。例如，对于下述声明:

```txt
std::array<double, 12> a1;
std::array<std::string, 12> a2;
```

可将它们替换为如下声明:

```txt
arr12<double> a1;
arr12(std::string> a2;
```

## 5. nullptr

空指针是不会指向有效数据的指针。以前，C++在源代码中使用0表示这种指针，但内部表示可能不同。这带来了一些问题，因为这使得0即可表示指针常量，又可表示整型常量。正如第12章讨论的，C++11新增了关键字nullptr，用于表示空指针；它是指针类型，不能转换为整型类型。为向后兼容，-C++11仍允许使用0来表示空指针，因此表达式nullptr==0为true，但使用nullptr而不是0提供了更高的类型安全。例如，-可将0传递给接受int参数的函数，但如果您试图将nullptr传递给这样的函数，编译器将此视为错误。因此，出于清晰和安全考虑，请使用nullptr——如果您的编译器支持它。

## 18.1.4 智能指针

如果在程序中使用new从堆（自由存储区）分配内存，等到不再需要时，应使用delete将其释放。C++引入了智能指针auto\_ptr，以帮助自动完成这个过程。随后的编程体验（尤其是使用STL时）表明，需要有更精致的机制。基于程序员的编程体验和BOOST库提供的解决方案，C++11摒弃了auto\_ptr，并新增了三种智能指针:unique\_ptr、shared\_ptr和weak\_ptr，第16章讨论了前两种。

所有新增的智能指针都能与STL容器和移动语义协同工作。

## 18.1.5 异常规范方面的修改

以前，C++提供了一种语法，可用于指出函数可能引发哪些异常（参见第15章）:

```cpp
void £501(int) throw(bad_dog);- // can=threw_type=bad_dog_exception_
void £733(long longF throw(); // doesn't throw an_exception
```

与 auto\_ptr 一样，C++编程社区的集体经验表明，异常规范的效果没有预期的好。因此，C++11 摒弃的

异常规范。然而，标准委员会认为，指出函数不会引发异常有一定的价值，他们为此添加了关键字 noexcept:

void f875(short, short) noexcept; // doesn't throw an exception

## 18.1.6 作用域内枚举

传统的 C++ 枚举提供了一种创建名称常量的方式，但其类型检查相当低级。另外，枚举名的作用域为枚举定义所属的作用域，这意味着如果在同一个作用域内定义两个枚举，它们的枚举成员不能同名。最后，枚举可能不是可完全移植的，因为不同的实现可能选择不同的底层类型。为解决这些问题，C++11 新增了一种枚举。这种枚举使用 class 或 struct 定义:

```txt
enum Old1 {yes, no, maybe};          // traditional form
enum class New1 {never, sometimes, often, always}; // new form
enum struct New2 {never, lever, sever};         // new form
```

新枚举要求进行显式限定，以免发生名称冲突。因此，引用特定枚举时，需要使用 New1::never 和 New2::never 等。更详细的信息请参阅第 10 章。

## 18.1.7 对类的修改

为简化和扩展类设计，C++11做了多项改进。这包括允许构造函数被继承和彼此调用、更佳的方法访问控制方式以及移动构造函数和移动赋值运算符，这些都将在本章介绍。下面先来复习本书前面介绍过的改进。

## 1. 显式转换运算符

有趣的是，C++很早就支持对象自动转换。但随着编程经验的积累，程序员逐渐认识到，自动类型转换可能导致意外转换的问题。为解决这种问题，C++引入了关键字explicit，以禁止单参数构造函数导致的自动转换:

```txt
class Plebe
{
    Plebe(int);   // automatic int-to-plebe conversion
    explicit Plebe(double);  // requires explicit use
    ...
};
...
Plebe a, b;
a = 5;            // implicit conversion, call Plebe(5)
b = 0.5;           // not allowed
b = Plebe(0.5);  // explicit conversion
```

C++11 拓展了 explicit 的这种用法，使得可对转换函数做类似的处理（参见第 11 章）:

```matlab
class Plebe
{
...
// conversion functions
    operator int() const;
    explicit operator double() const;

    ...
};
...
Plebe a, b;
int n = a;      // int-to-Plebe automatic conversion
double x = b;   // not allowed
x = double(b);  // explicit conversion, allowed
```

## 2. 类内成员初始化

很多首次使用 C++ 的用户都会问，为何不能在类定义中初始化成员？现在可以这样做了，其语法类似于下面这样:

```cpp
class Session
{
    int mem1== 10;          // in-class initialization
    double mem2 {1966.54}; // in-class initialization
    short mem3;
public:
    Session(){}                                       // #1
    Session(short s) : mem3(s) {}                      // #2
    Session(int n, double-d, short s) : mem1(n), mem2(d), mem3(s) {} // #3
...
```

可使用等号或大括号版本的初始化，但不能使用圆括号版本的初始化。其结果与给前两个构造函数提供成员初始化列表，并指定 mem1 和 mem2 的值相同:

```javascript
Session(): mem1(10), mem2(1966.54) {}
Session(short s) : mem1(10),_mem2(1966.54), mem3(s) {}
```

通过使用类内初始化，可避免在构造函数中编写重复的代码，从而降低了程序员的工作量、厌倦情绪和出错的机会。

如果构造函数在成员初始化列表中提供了相应的值，这些默认值将被覆盖，因此第三个构造函数覆盖了类内成员初始化。

## 18.1.8 模板和STL方面的修改

为改善模板和标准模板库的可用性，C++Fl做了多个改进；有些是库本身，有些与易用性相关。本章前面提到了模板别名和适用于STL的智能指针。

## 1. 基于范围的 for 循环

对于内置数组以及包含方法 begin() 和 end() 的类（如 std::string）和 STL 容器，基于范围的 for 循环（第 5 章和第 16 章讨论过）可简化为它们编写循环的工作。这种循环对数组或容器中的每个元素执行指定的操作:

```cpp
double prices[5] = {4.99, 10.99, 6.87, 7.99, 8.49};
for (double x : prices)
    std::cout << x << std::endl;
```

其中，x 将依次为 prices 中每个元素的值。x 的类型应与数组元素的类型匹配。一种更容易、更安全的方式是，使用 auto 来声明 x，这样编译器将根据 prices 声明中的信息来推断 x 的类型:

```cpp
double prices[5] = {4.99, 10.99, 6.87, 7.99, 8.49};
for {auto x : prices}
    std::cout << x << std::endl;
```

如果要在循环中修改数组或容器的每个元素，可使用引用类型:

```cpp
std::vector<int> vi(6);
for (auto & x: vi).... // use a reference if loop-alters contents
    x = std::rand();
```

## 2. 新的STL容器

C++11 新增了 STL 容器 forward\_list、unordered\_map、unordered\_multimap、unordered\_set 和 unordered\_multiset （参见第 16 章）。容器 forward\_list 是一种单向链表，只能沿一个方向遍历；与双向链接的 list 容器相比，它更简单，在占用存储空间方面更经济。其他四种容器都是使用哈希表实现的。

C++11 还新增了模板 array（这在第 4 和 16 章讨论过）。要实例化这种模板，可指定元素类型和固定的元素数:

```rust
std::array<int,360> ar;  // array of 360 ints
```

这个模板类没有满足所有的常规模板需求。例如，由于长度固定，您不能使用任何修改容器大小的方法，如put\_back()。但array确实有方法begin()和end()，这让您能够对array对象使用众多基于范围的STL算法。

## 3. 新的STL方法

C++11 新增了 STL 方法 cbegin() 和 cend()。与 begin() 和 end() 一样，这些新方法也返回一个迭代器，指向容器的第一个元素和最后一个元素的后面，因此可用于指定包含全部元素的区间。另外，这些新方法将元素视为 const。与此类似，crbegin() 和 crend() 是 rbegin() 和 rend() 的 const 版本。

更重要的是，除传统的复制构造函数和常规赋值运算符外，STL 容器现在还有移动构造函数和移动赋值运算符。移动语义将在本章后面介绍。

## 4. valarray 升级

模板 valarray 独立于 STL 开发的，其最初的设计导致无法将基于范围的 STL 算法用于 valarray 对象。C++11 添加了两个函数（begin() 和 end()），它们都接受 valarray 作为参数，并返回迭代器，这些迭代器分别指向 valarray 对象的第一个元素和最后一个元素后面。这让您能够将基于范围的 STL 算法用于 valarray（参见第 16 章）。

## 5. 摒弃 export

C++98 新增了关键字 export，旨在提供一种途径，让程序员能够将模板定义放在接口文件和实现文件中，其中前者包含原型和模板声明，而后者包含模板函数和方法的定义。实践证明这不现实，因此 C++11 终止了这种用法，但仍保留了关键字 export，供以后使用。

## 6. 尖括号

为避免与运算符>>混淆，C++要求在声明嵌套模板时使用空格将尖括号分开:

```rust
std::vector<std::list<int> > v1; // >> not ok
```

C++11 不再这样要求:

```cpp
std::vector<std::list<int>> vl; // >> ok in C++11
```

## 18.1.9 右值引用

传统的 C++ 引用（现在称为左值引用）使得标识符关联到左值。左值是一个表示数据的表达式（如变量名或解除引用的指针），程序可获取其地址。最初，左值可出现在赋值语句的左边，但修饰符 const 的出现使得可以声明这样的标识符，即不能给它赋值，但可获取其地址:

```c
int n;
int * pt = new int;
const int b = 101;   // can't assign to b, but &b is valid
int & rn = n;           // n identifies datum at address &n
int & rt = *pt;     // *pt identifies datum at address pt
const int & rb = b; // b identifies const datum at address &b
```

C++11 新增了右值引用（这在第 8 章讨论过），这是使用&&表示的。右值引用可关联到右值，即可出现在赋值表达式右边，但不能对其应用地址运算符的值。右值包括字面常量（C-风格字符串除外，它表示地址）、诸如 x+y 等表达式以及返回值的函数（条件是该函数返回的不是引用）:

```txt
int x = 10;
int y = 23;
int && r1 = 13;
int && r2 = x + y;
double && r3 = std::sqrt(2.0);
```

注意，r2 关联到的是当时计算  $x + y$  得到的结果。也就是说，r2 关联到的是 23，即使以后修改了 x 或 y，也不会影响到 r2。

有趣的是，将右值关联到右值引用导致该右值被存储到特定的位置，且可以获取该位置的地址。也就是说，虽然不能将运算符&用于13，但可将其用于r1。通过将数据与特定的地址关联，使得可以通过右值引用来访问该数据。

程序清单 18.1 是一个简短的示例，演示了上述有关右值引用的要点。

程序清单 18.1 rvref.cpp

```cpp
// rvref.cpp -- simple uses of rvalue references
#include <iostream>

inline double f(double tf) {return 5.0*(tf-32.0)/9.0;};
int main()
{
    using namespace std;
    double tc = 21.5;
    double && rd1 = 7.07;
    double && rd2 = 1.8 * tc + 32.0;
    double && rd3 = f(rd2);
    cout << " tc value and address: " << tc <<", " << &tc << endl;
    cout << "rd1 value and address: " << rd1 <<", " << &rd1 << endl;
    cout << "rd2 value and address: " << rd2 <<", " << &rd2 << endl;
    cout << "rd3 value and address: " << rd3 <<", " << &rd3 << endl;
    cin.get();
    return 0;
}
```

该程序的输出如下:

```txt
tc value and address: 21.5, 002FF744
rd1 value and address: 7.07, 002FF728
rd2 value and address: 70.7, 002FF70C
rd3 value and address: 21.5, 002FF6F0
```

引入右值引用的主要目的之一是实现移动语义，这是本章将讨论的下一个主题。

## 18.2 移动语义和右值引用

现在介绍本书前面未讨论的主题。C++11 支持移动语义，这就提出了一些问题:什么是移动语义？C++11 如何支持它？为何需要移动语义？下面首先讨论第一个问题。

## 18.2.1 为何需要移动语义

先来看 C++11 之前的复制过程。假设有如下代码:

```txt
vector<string> vstr;
// build up a vector of 20,000 strings, each of 1000 characters
...
vector<string> vstr_copy1(vstr);  // make vstr_copy1 a copy of vstr
```

vector 和 string 类都使用动态内存分配，因此它们必须定义使用某种 new 版本的复制构造函数。为初始化对象 vstr\_copy1，复制构造函数 vector&lt;string&gt; 将使用 new 给 20000 个 string 对象分配内存，而每个 string 对象又将调用 string 的复制构造函数，该构造函数使用 new 为 1000 个字符分配内存。接下来，全部 20000000 个字符都将从 vstr 控制的内存中复制到 vstr\_copy1 控制的内存中。这里的工作量很大，但只要妥当就行。

但这确实妥当吗？有时候答案是否定的。例如，假设有一个函数，它返回一个vector&lt;string&gt;对象:

```txt
vector<string> allcaps(const vector<string> & vs)
{
    vector<string> temp;
// code that stores an all-uppercase version of vs in temp
    return temp;
}
```

接下来，假设以下面这种方式使用它:

```txt
vector<string> vstr;
// build up a vector of 20,000 strings, each of 1000 characters
vector<string> vstr_copy1(vstr);          // #1
vector<string> vstr_copy2(allcaps(vstr));     // #2
```

从表面上看，语句#1 和#2 类似，它们都使用一个现有的对象初始化一个 vector&lt;string&gt;对象。如果深入探索这些代码，将发现 allcaps() 创建了对象 temp，该对象管理着 20000000 个字符；vector 和 string 的复制构造函数创建这 20000000 个字符的副本，然后程序删除 allcaps() 返回的临时对象（迟钝的编译器甚至可能将 temp 复制给一个临时返回对象，删除 temp，再删除临时返回对象）。这里的要点是，做了大量的无用功。考虑到临时对象被删除了，如果编译器将对数据的所有权直接转让给 vstr\_copy2，不是更好吗？也就是说，不将 20000000 个字符复制到新地方，再删除原来的字符，而将字符留在原来的地方，并将 vstr\_copy2 与之相关联。这类似于在计算机中移动文件的情形:实际文件还留在原来的地方，而只修改记录。这种方法被称为移动语义（move semantics）。有点悖论的是，移动语义实际上避免了移动原始数据，而只是修改了记录。

要实现移动语义，需要采取某种方式，让编译器知道什么时候需要复制，什么时候不需要。这就是右值引用发挥作用的地方。可定义两个构造函数。其中一个是常规复制构造函数，它使用 const 左值引用作为参数，这个引用关联到左值实参，如语句#1 中的 vstr；另一个是移动构造函数，它使用右值引用作为参数，该引用关联到右值实参，如语句#2 中 allcaps(vstr) 的返回值。复制构造函数可执行深复制，而移动构造函数只调整记录。在将所有权转移给新对象的过程中，移动构造函数可能修改其实参，这意味着右值引用参数不应是 const。

## 18.2.2 一个移动示例

下面通过一个示例演示移动语义和右值引用的工作原理。程序清单 18.2 定义并使用了 Useless 类，这个类动态分配内存，并包含常规复制构造函数和移动构造函数，其中移动构造函数使用了移动语义和右值引用。为演示流程，构造函数和析构函数都比较啰嗦，同时 Useless 类还使用了一个静态变量来跟踪对象数量。另外，省略了一些重要的方法，如赋值运算符。

程序清单 18.2 useless.cpp

```cpp
// useless.cpp -- an otherwise useless class with move semantics
#include <iostream>
using namespace std;

// interface
class Useless
{
private:
```

```cpp
int n;          // number of elements
    char * pc;      // pointer to data
    static int ct;  //_number of objects——
    void ShowObject() const;
public:
    Useless();
    explicit Useless(int k);
    Useless(int k, char ch);
    Useless(const Useless & f); // regular copy constructor
    Useless(Useless && f);      // move-constructor
    ~Useless();
    Useless operator+(const Useless & f)const;
// need operator=() in copy and move versions
    void ShowData() const;
};

// implementation
int Useless::ct = 0;

Useless::Useless()
{
    ++ct;
    n = 0;
    pc = nullptr;
    cout << "default constructor called; number of objects: " << ct << endl;
    ShowObject();
}

Useless::Useless(int k) : n(k)
{
    ++ct;
    cout << "int constructor called; number of objects: " << ct << endl;
    pc = new char[n];
    ShowObject();
}

Useless::Useless(int k, char ch) : n(k)
{
    ++ct;
    cout << "int, char constructor called; number of objects: " << ct
        << endl;
    pc = new char[n];
    for (int i = 0; i < n; i++)
        pc[i] = ch;
    ShowObject();
}

Useless::Useless(const Useless & f): n(f.n)
{
    ++ct;
    cout << "copy const called; number of objects: " << ct << endl;
    pc = new char[n];
    for (int i = 0; i < n; i++)
        pc[i] = f.pc[i];
    ShowObject();
```

```cpp
}
Useless::Useless(Useless && f): n(f.n)
{
    ++ct;
    cout << "move constructor called; number of objects: " << ct << endl;
    pc = f.pc;          // steal address_
    f.pc = nullptr;  // give old object nothing in return=
    f.n = 0;
    ShowObject();
}
Useless::~Useless()
{
    cout << "destructor called; objects left: " << --ct << endl;
    cout << "deleted object:\n";
    ShowObject();
    delete [] pc;
}
Useless Useless::operator+(const Useless & f)const
{
    cout << "Entering operator+\()\n";
    Useless temp = Useless(n +-f.n);
    for (int i = 0; i < n; i++)
        temp.pc[i] = pc[i];
    for (int i = n; i < temp.n; i++)
        temp.pc[i] = f.pc[i - n];
    cout << "temp object:\n";
    cout << "Leaving operator+\()\n";
    return temp;
}
void Useless::ShowObject() const
{
    cout << "Number of eFements: " << n;
    cout << " Data address: " << (void *) pc << endl;
}
void Useless::ShowData() const
{
    if (n == 0)
        cout << "(object empty)";
    else
        for (int i = 0; i < n; i++)
            cout << pc[i];
    cout << endl;
}
// application
int main()
{
    {
        Useless one(F0, 'x');
        Useless two = one;          // calIs copy constructor
        Useless three(20, 'o');
```

```javascript
Useless four (one + three); // calls operator+, move constructor
cout << "object one: ";
one.ShowData();
cout << "object two: ";
two.ShowData();
cout << "object three: ";
three.ShowData();
cout << "object four: ";
four.ShowData();
```

其中最重要的是复制构造函数和移动构造函数的定义。首先来看复制构造函数（删除了输出语句）:

```cpp
Useless::Useless(const.Useless &_f): n(f.n)
{
    ++ct;
    pc = new char[n];
    for (int i = 0; i < n; i++)
        pc[i] = f.pc[i];
}
```

它执行深复制，是下面的语句将使用的构造函数:

```txt
Useless two = one;          // calls copy constructor
```

引用f将指向左值对象one。

接下来看移动构造函数，这里也删除了输出语句:

```cpp
Useless::Useless(Useless && f): n(f.n)
{
    ++ct;
    pc = f.pc;      // steal address
    f.pc = nullptr;  // give old object nothing in return
    f.n = 0;
}
```

它让 pc 指向现有的数据，以获取这些数据的所有权。此时，pc 和 f.pc 指向相同的数据，调用析构函数时这将带来麻烦，因为程序不能对同一个地址调用 delete [ ] 两次。为避免这种问题，该构造函数随后将原来的指针设置为空指针，因为对空指针执行 delete [ ] 没有问题。这种夺取所有权的方式常被称为窃取 (pilfering)。上述代码还将原始对象的元素数设置为零；这并非必不可少的；但让这个示例的输出更一致。注意，由于修改了 f 对象，这要求不能在参数声明中使用 const。

在下面的语句中，将使用这个构造函数:

```txt
Useless-four (one + three); // calls move constructor
```

表达式 one + three 调用 Useless::operator+( )，而右值引用 f 将关联到该方法返回的临时对象。

下面是在 Microsoft Visual C++ 2010 中编译时，该程序的输出:

```txt
int, char constructor called; number of objects: 1
Number of elements: 10 Data address: 006F4B68
copy const called; number of objects: 2
Number of elements: 10 Data address: 006F4BB0
int, char constructor called; number of objects: 3
Number of elements: 20 Data address: 006F4BF8
Entering operator+()
int constructor called; number of objects: 4
Number of elements: 30 Data address: 006F4C48
temp object:
```

```csv
Leaving operator+()
move constructor called; number of objects: 5
Number of elements: 30 Data address: 006F4C48
destructor called; objects left: 4
deleted object:
Number of elements: 0 Data address: 00000000
object one: xxxxxxxxxxx
object two: xxxxxxxxxxx
object three: oooooooooooooooooooo
object four: xxxxxxxxxxxxooooooooooooooooooooooo
destructor called; objects left: 3
deleted object:
Number of elements: 30 Data address: 006F4C48
destructor called; objects left: 2
deleted object:
Number of elements: 20 Data address: 006F4BF8
destructor called; objects left: 1
deleted object:
Number of elements: 10 Data address: 006F4BB0
destructor called; objects left: 0
deleted object:
Number of elements: 10 Data address: 006F4B68
```

注意到对象 two 是对象 one 的副本:它们显示的数据输出相同，但显示的数据地址不同（006F4B68 和 006F4BB0）。另一方面，在方法 Useless::operator+() 中创建的对象的数据地址与对象 four 存储的数据地址相同（都是 006F4C48），其中对象 four 是由移动复制构造函数创建的。另外，注意到创建对象 four 后，为临时对象调用了析构函数。之所以知道这是临时对象，是因为其元素数和数据地址都是 0。

如果使用编译器 g++4.5.0 和标记 -std=c++11 编译该程序（但将 nullptr 替换为 0），输出将不同，这很有趣:

```txt
int, char constructor called; number of objects: 1
Number of elements: 10 Data address: 0xa50338
copy const called; number of objects: 2
Number of elements: 10 Data address: 0xa50348
int, char constructor called; number of objects: 3
Number of elements: 20 Data address: 0xa50358
Entering operator+()
int constructor called; number of objects: 4
Number of elements: 30 Data address: 0xa50370
temp object:
Leaving operator+()
object one: xxxxxxxxxxxx
object two: xxxxxxxxxxxx
object three: oooooooooooooooooooo
object four: xxxxxxxxxxxxooooooooooooooooooooooo
destructor called; objects left: 3
deleted object:
Number of elements: 30 Data address: 0xa50370
destructor called; objects left: 2
deleted object:
Number of elements: 20 Data address: 0xa50358
destructor called; objects left: 1
deleted object:
Number of elements: 10 Data address: 0xa50348
destructor called; objects left: 0
deleted object:
Number of elements: 10 Data address: 0xa50338
```

注意到没有调用移动构造函数，且只创建了4个对象。创建对象four时，该编译器没有调用任何构造函数；相反，它推断出对象four是operator+()所做工作的受益人，因此将operator+()创建的对象转到four的名下。一般而言，编译器完全可以进行优化，只要结果与未优化时相同。即使您省略该程序中的移动构造函数，并使用g++进行编译，结果也将相同。

## 18.2.3 移动构造函数解析

虽然使用右值引用可支持移动语义，但这并不会神奇地发生。要让移动语义发生，需要两个步骤。首先，右值引用让编译器知道何时可使用移动语义:

```cpp
Useless two== one; // matches=Useless::Useless(const Useless &) 
Useless four (one + three); // matches=Useless::Useless(Useless &&|
```

对象 one 是左值，与左值引用匹配，而表达式 one + three 是右值，与右值引用匹配。因此，右值引用谁编译器使用移动构造函数来初始化对象 four。实现移动语义的第二步是，编写移动构造函数，使其提供所需的行为。

总之，通过提供一个使用左值引用的构造函数和一个使用右值引用的构造函数，将初始化分成了两组。使用左值对象初始化对象时，将使用复制构造函数，而使用右值对象初始化对象时，将使用移动构造函数。程序员可根据需要赋予这些构造函数不同的行为。

这就带来了一个问题:在引入右值引用前，情况是什么样的呢？如果没有移动构造函数，且编译器未能通过优化消除对复制构造函数的需求，结果将如何呢？在C++98中，下面的语句将调用复制构造函数=

```javascript
Useless=four {one + three};
```

但左值引用不能指向右值。结果将如何呢？第8章介绍过，如果实参为右值，const引用形参将指向一个临时变量:

```c
int twfce(const & rx) {return 2-* rx;}
...
int main()=
{
    int m = 6;
    // below, rx refers to-m
    int n = twice(m);
    // below, rx refers to a temporary variable initialized to 2r
    int k = twice(21);
```

就 Useless 而言，形参 f 将被初始化一个临时对象，而该临时对象被初始化为 operator+() 返回的值。下面是使用老式编译器进行编译时，程序清单 18.2 所示程序（删除了移动构造函数）的部分输出:

```txt
Entering operator+()
int constructor called; number of objects: 4
Number of elements: 30 Data address: 01C337C4
temp object:
Leaving operator+()
copy const called; number of objects: 5
Number of elements: 30 Data address: 01C337E8
destructor called; objects left: 4
deleted object:
Number of elements: 30 Data address: 01C337C4
copy const called; number of objects: 5
Number of elements: 30 Data address: 01C337C4
destructor called; objects left: 4
deleted object:
Number of elements: 30 Data address: 01C337E8...
```

首先，在方法 Useless::operator+() 内，调用构造函数创建了 temp，并在 01C337C4 处给它分配了存储 30 个元素的空间。然后，调用复制构造函数创建了一个临时复制信息（其地址为 01C337E8），f 指向该副本。接下来，删除了地址为 01C337C4 的对象 temp。然后，新建了对象 four，它使用了 01C337C4 处刚释放的内存。接下来，删除了 01C337E8 处的临时参数对象。这表明，总共创建了三个对象，但其中的两个被删除。这些就是移动语义旨在消除的额外工作。

正如 $\mathrm{g}++$ 示例表明的，机智的编译器可能自动消除额外的复制工作，但通过使用右值引用，程序员可指出何时该使用移动语义。

## 18.2.4\_ 赋值

适用于构造函数的移动语义考虑也适用于赋值运算符。例如，下面演示了如何给 Useless 类编写复制赋值运算符和移动赋值运算符:

```cpp
Useless & Useless::operator=(const Useless & f) // copy assignment
{
    if (this == &f)
        return *this;
    delete [] pc;
    n = f.n;
    pc = new char[n];
    for (int i = 0; i < n; i++)
        pc[i] = f.pc[i];
    return *this;
}

Useless & Useless::operator=(Useless && f) // move assignment
{
    if (this == &f)
        return *this;
    delete [] pc;
    n = f.n;
    pc = f.pc;
    f.n = 0;
    f.pc = nullptr;
    return *this;
}
```

上述复制赋值运算符采用了第 12 章介绍的常规模式，而移动赋值运算符删除目标对象中的原始数据，并将源对象的所有权转让给目标。不能让多个指针指向相同的数据，这很重要，因此上述代码将源对象中的指针设置为空指针。

与移动构造函数一样，移动赋值运算符的参数也不能是const引用，因为这个方法修改了源对象。

## 18.2.5 强制移动

移动构造函数和移动赋值运算符使用右值。如果要让它们使用左值，该如何办呢？例如，程序可能分析一个包含候选对象的数组，选择其中一个对象供以后使用，并丢弃数组。如果可以使用移动构造函数或移动赋值运算符来保留选定的对象，那该多好啊。然而，假设您试图像下面这样做:

```txt
Useless choices[10];
Useless best;
int_pick;
... // select one object, set pick to index
best = choices[pick];
```

由于 choices[pick]是左值，因此上述赋值语句将使用复制赋值运算符，而不是移动赋值运算符。但如果能让 choices[pick]看起来像右值，便将使用移动赋值运算符。为此，可使用运算符 static\_cast<>将对象的类型强制转换为 Useless &&，但 C++11 提供了一种更简单的方式——使用头文件 utility 中声明的函数 std::move()。程序清单 18.3 演示了这种技术，它在 Useless 类中添加了啰嗦的赋值运算符，并让以前啰嗦的构造函数和析构函数保持沉默。

程序清单 18.3 stdmove.cpp

```cpp
// stdmove.cpp -- using std::move()
#include <iostream>
#include <utility>

// interface
class Useless
{
private:
    int n;          // number of elements
    char * pc;      // pointer to data
    static int ct;  // number of objects
    void ShowObject() const;
public:
    Useless();
    explicit Useless(int k);
    Useless(int k, char ch);
    Useless(const Useless & f); // regular copy constructor
    Useless(Useless && f);     // move constructor
    ~Useless();
    Useless operator+(const Useless & f)const;
    Useless & operator=(const Useless & f); // copy assignment
    Useless & operator=(Useless && f);       // move assignment
    void ShowData() const;
};

// implementation
int Useless::ct = 0;

Useless::Useless()
{
    ++ct;
    n = 0;
    pc = nullptr;
}

Useless::Useless(int k) : n(k)
{
    ++ct;
    pc = new char[n];
}
Useless::Useless(int k, char ch) : n(k)
{
    ++ct;
    pc = new char[n];
    for (int i = 0; i < n; i++)
        pc[i] = ch;
}
```

```cpp
Useless::Useless(const Useless & f): n(f.n)
{
    ++ct;
    pc = new char[n];
    for (int i = 0; i < n; i++)
        pc[i] = f.pc[i];
}

Useless::Useless(Useless && f): n(f.n)
{
    ++ct;
    pc = f.pc;          // steal address
    f.pc = nullptr;   // give old object nothing in return
    f.n = 0;
}

Useless::~Useless()
{
    delete [] pc;
}

Useless & Useless::operator=(const Useless & f)  // copy assignment
{
    std::cout << "copy assignment operator called:\n";
    if (this == &f)
        return *this;
    delete [] pc;
    n = f.n;
    pc = new char[n];
    for (int i = 0; i < n; i++)
        pc[i] = f.pc[i];
    return *this;
}

Useless & Useless::operator=(Useless && f)      // move assignment
{
    std::cout << "move assignment operator called:\n";
    if (this == &f)
        return *this;
    delete [] pc;
    n = f.n;
    pc = f.pc;
    f.n = 0;
    f.pc = nullptr;
    return *this;
}

Useless Useless::operator+(const Useless & f)const
{
    Useless temp = Useless(n + f.n);
    for (int i = 0; i < n; i++)
        temp.pc[i] = pc[i];
    for (int i = n; i < temp.n; i++)
        temp.pc[i] = f.pc[i - n];
    return temp;
```

```cpp
void Useless::ShowObject() const
{
    std::cout << "Number of elements: " << n;
    std::cout << " Data address: " << (void *) pc << std::endl;
}

void Useless::ShowData() const
{
    if (n == 0)
        std::cout << "(object empty)";
    else
        for (int i = 0; i < n; i++)
            std::cout << pc[i];
    std::cout << std::endl;
}

// application
int main()
{
    using std::cout;
    {
        Useless one(10, 'x');
        Useless two = one +one;   // calls move constructor
        cout << "object one: ";
        one.ShowData();
        cout << "object two: ";
        two.ShowData();
        Useless three, four;
        cout << "three = one\n";
        three = one;                 // automatic copy assignment
        cout << "now object three = ";
        three.ShowData();
        cout << "and object one = ";
        one.ShowData();
        cout << "four = one + two\n";
        four = one + two;           // automatic move assignment
        cout << "now object four = ";
        four.ShowData();
        cout << "four = move(one)\n";
        four = std::move(one);     // forced move assignment
        cout << "now object four = ";
        four.ShowData();
        cout << "and object one = ";
        one.ShowData();
    }
}
```

该程序的输出如下:

```txt
object one: xxxxxxxxxxx
object two: xxxxxxxxxxxxxxxxxxxxxxx
three = one
copy assignment operator called:
```

```txt
now object three = xxxxxxxxxxx
and object one = xxxxxxxxxxx
four = one + two
move assignment operator called:
now object four = xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
four = move(one)
move assignment operator called:
now object four = xxxxxxxxxxx
and object one = (object empty)
```

正如您看到的，将 one 赋给 three 调用了复制赋值运算符，但将 move(one) 赋给 four 调用的是移动赋值运算符。

需要知道的是，函数 std::move() 并非一定会导致移动操作。例如，假设 Chunk 是一个包含私有数据的类，而您编写了如下代码:

```txt
Chunk one;
...
Chunk two;
two = std::move(one);  // move semantics?
```

表达式 std::move(one) 是右值，因此上述赋值语句将调用 Chunk 的移动赋值运算符——如果定义了这样的运算符。但如果 Chunk 没有定义移动赋值运算符，编译器将使用复制赋值运算符。如果也没有定义复制赋值运算符，将根本不允许上述赋值。

对大多数程序员来说，右值引用带来的主要好处并非是让他们能够编写使用右值引用的代码，而是能够使用利用右值引用实现移动语义的库代码。例如，STL 类现在都有复制构造函数、移动构造函数、复制赋值运算符和移动赋值运算符。

## 18.3 新的类功能

除本章前面提到的显式转换运算符和类内成员初始化外，C++11还新增了其他几个类功能。

## 18.3.1 特殊的成员函数

在原有 4 个特殊成员函数（默认构造函数、复制构造函数、复制赋值运算符和析构函数）的基础上，C++11 新增了两个:移动构造函数和移动赋值运算符。这些成员函数是编译器在各种情况下自动提供的。

前面说过，在没有提供任何参数的情况下，将调用默认构造函数。如果您没有给类定义任何构造函数，编译器将提供一个默认构造函数。这种版本的默认构造函数被称为默认的默认构造函数。对于使用内置类型的成员，默认的默认构造函数不对其进行初始化；对于属于类对象的成员，则调用其默认构造函数。

另外，如果您没有提供复制构造函数，而代码又需要使用它，编译器将提供一个默认的复制构造函数；如果您没有提供移动构造函数，而代码又需要使用它，编译器将提供一个默认的移动构造函数。假定类名为 Someclass，这两个默认的构造函数的原型如下:

```cpp
Someclass::Someclass(const Someclass &);  // defaulted copy constructor
Someclass::Someclass(Someclass &&);      // defaulted move constructor
```

在类似的情况下，编译器将提供默认的复制运算符和默认的移动运算符，它们的原型如下:

```cpp
Someclass & Someclass::operator(const Someclass &); // defaulted copy assignment
Someclass & Someclass::operator(Someclass &&); // defaulted move assignment
```

最后，如果您没有提供析构函数，编译器将提供一个。

对于前面描述的情况，有一些例外。如果您提供了析构函数、复制构造函数或复制赋值运算符，编译器将不会自动提供移动构造函数和移动赋值运算符；如果您提供了移动构造函数或移动赋值运算符，编译器将不会自动提供复制构造函数和复制赋值运算符。

另外，默认的移动构造函数和移动赋值运算符的工作方式与复制版本类似:执行逐成员初始化并复制内置类型。如果成员是类对象，将使用相应类的构造函数和赋值运算符，就像参数为右值一样。如果定义了移动构造函数和移动赋值运算符，这将调用它们；否则将调用复制构造函数和复制赋值运算符。

## 18.3.2 默认的方法和禁用的方法

C++11 让您能够更好地控制要使用的方法。假定您要使用某个默认的函数，而这个函数由于某种原因不会自动创建。例如，您提供了移动构造函数，因此编译器不会自动创建默认的构造函数、复制构造函数和复制赋值构造函数。在这些情况下，您可使用关键字 default 显式地声明这些方法的默认版本:

```cpp
class Someclass
{
public:
    Someclass(Someclass &&);
    Someclass() = default;      // use compiler-generated default constructor
    Someclass(const Someclass &) = default;
    Someclass & operator=(const Someclass &) = default;
...
};
```

编译器将创建在您没有提供移动构造函数的情况下将自动提供的构造函数。

另一方面，关键字 delete 可用于禁止编译器使用特定方法。例如，要禁止复制对象，可禁用复制构造函数和复制赋值运算符:

```cpp
class Someclass
{
public:
    Someclass() = default;      // use compiler-generated default constructor
// disable copy constructor and copy assignment operator:
    Someclass(const Someclass &) = delete;
    Someclass & operator=(const Someclass &) = delete;
// use compiler-generated move constructor and move assignment operator:
    Someclass(Someclass &&) = default;
    Someclass & operator=(Someclass &&) = default;
    Someclass & operator+(const Someclass &) const;
...
};
```

第 12 章说过，要禁止复制，可将复制构造函数和赋值运算符放在类定义的 private 部分，但使用 delete 也能达到这个目的，且更不容易犯错、更容易理解。

如果在启用移动方法的同时禁用复制方法，结果将如何呢？前面说过，移动操作使用的右值引用只能关联到右值表达式，这意味着:

```cpp
Someclass one;
Someclass two;
Someclass three(one);      // not allowed, one an lvalue
Someclass four(one + two);  // allowed, expression is an rvalue
```

关键字 default 只能用于 6 个特殊成员函数，但 delete 可用于任何成员函数。delete 的一种可能用法是禁止特定的转换。例如，假设 Someclass 类有一个接受 double 参数的方法:

```matlab
class Someclass
{
public:
...
    void redo(double);
...
};
```