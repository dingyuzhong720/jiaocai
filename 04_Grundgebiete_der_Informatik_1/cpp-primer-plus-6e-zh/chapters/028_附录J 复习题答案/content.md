# 附录J 复习题答案

原始 PDF 第 934–955 页。

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
5. 这两条语句并不真正等价，虽然对于某些系统来说，它们是等效的。最重要的是，只有在使用 ASCII

---

附录 J 复习题答案

917

码的系统上，第一条语句才将得分设置为字母 A，而第二条语句还可用于使用其他编码的系统。其次，65 是一个 int 常量，而 'A' 是一个 char 常量。

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

---

918

C++ Primer Plus（第6版）中文版

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

---

附录 J 复习题答案

919

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

---

920

C++ Primer Plus（第6版）中文版

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

---

附录J 复习题答案

921

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
10. 要按值传递它，只要传递结构名 glitz 即可。要传递它的地址，请使用地址运算符&glitz。按值传递将自动保护原始数据，但这是以时间和内存为代价的。按地址传递可节省时间和内存，但不能保护原始

---

922

C++ Primer Plus（第6版）中文版

数据，除非对函数参数使用了 const 限定符。另外，按值传递意味着可以使用常规的结构成员表示法，但传递指针则必须使用间接成员运算符。

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

---

附录J 复习题答案

923

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

---

924

C++ Primer Plus（第6版）中文版

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

---

附录 J 复习题答案

925

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

---

926

C++ Primer Plus（第6版）中文版

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

---

附录 J 复习题答案

927

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

2. 首先，当这种类型的对象过期时，对象的成员指针指向的数据仍将保留在内存中，这将占用空间，同时不可访问，因为指针已经丢失。可以让类析构函数删除构造函数中 new 分配的内存，来解决这种问题。其次，析构函数释放这种内存后，如果程序将这样的对象初始化为另一个对象，则析构函数将试图释放这

---

928

C++ Primer Plus（第6版）中文版

些内存两次。这是因为将一个对象初始化为另一个对象的默认初始化，将复制指针值，但不复制指向的数据，这将使两个指针指向相同的数据。解决方法是，定义一个复制构造函数，使初始化复制指向的数据。第三，将一个对象赋给另一个对象也将导致两个指针指向相同的数据。解决方法是重载赋值运算符，使之复制数据，而不是指针。

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

---

附录 J 复习题答案

929

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

---

930

C++ Primer Plus (第6版) 中文版

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

---

附录 J 复习题答案

931

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

---

932

C++ Primer Plus（第6版）中文版

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

---

附录 J 复习题答案

933

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

---

934

C++ Primer Plus（第6版）中文版

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

---

附录 J 复习题答案

935

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

---

936

C++ Primer Plus（第6版）中文版

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

---

[General Information]

书名=C++ Primer Plus 第6版 中文版

作者=(美)普拉达著

页数=936

出版社=北京市:人民邮电出版社

出版日期=2012.06

SS号=13010684

DX号=000008301948

URL=http://book.szdnet.org.cn/bookDetail.jsp?dxNumber=000008301948&d=AE012D9B1AFA912ABBAAA26E5136D8F3
