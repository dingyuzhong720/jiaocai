使用library[2].value的原因是:library[2]是结构变量名，正如library[1]是另一个变量名。

顺带一提，下面的表达式代表什么？

library[2].title[4]

这是library数组第3个结构变量（library[2]部分）中书名的第5个字符（title[4]部分）。以程序清单14.2的输出为例，这个字符是e。该例指出，点运算符右侧的下标作用于各个成员，点运算符左侧的下标作用与结构数组。

最后，总结一下:

library // 一个book 结构的数组

library[2] // 一个数组元素，该元素是book结构

library[2].title // 一个char数组（library[2]的title成员）

library[2].title[4] // 数组中library[2]元素的title 成员的一个字符

下面，我们来讨论一下这个程序。

## 14.4.3 程序讨论

较之程序清单14.1，该程序主要的改动之处是:插入一个while循环读取多个项。该循环的条件测试是:

while (count < MAXBKS && s\_gets(library[count].title, MAXTITL) != NULL

&& library[count].title[0] != '\0')

表达式 s\_gets(library[count].title, MAXTITL)读取一个字符串作为书名，如果 s\_gets()尝试读到文件结尾后面，该表达式则返回NULL。表达式library[count].title[0] != '\0'判断字符串中的首字符是否是空字符（即，该字符串是否是空字符串）。如果在一行开始处用户按下 Enter 键，相当于输入了一个空字符串，循环将结束。程序中还检查了图书的数量，以免超出数组的大小。

然后，该程序中有如下几行:

```txt
while (getchar() != '\n')
```

continue; /\* 清理输入行 \*/

前面章节介绍过，这段代码弥补了scanf()函数遇到空格和换行符就结束读取的问题。当用户输入书的价格时，可能输入如下信息:

12.50[Enter]

其传送的字符序列如下:

12.50\n

scanf()函数接受1、2、.、5和0，但是把\n留在输入序列中。如果没有上面两行清理输入行的代码，就会把留在输入序列中的换行符当作空行读入，程序以为用户发送了停止输入的信号。我们插入的这两行代码只会在输入序列中查找并删除\n，不会处理其他字符。这样s\_gets()就可以重新开始下一次输入。

## 14.5 嵌套结构

有时，在一个结构中包含另一个结构（即嵌套结构）很方便。例如，Shalala Pirosky创建了一个有关她朋友信息的结构。显然，结构中需要一个成员表示朋友的姓名。然而，名字可以用一个数组来表示，其中包含名和姓这两个成员。程序清单14.3是一个简单的示例。

程序清单14.3 friend.c程序

```c
// friend.c -- 嵌套结构示例

#include <stdio.h>

#define LEN 20

const char * msgs[5] =
{
"   Thank you for the wonderful evening, ",
"You certainly prove that a ",
"is a special kind of guy.We must get together",
"over a delicious ",
" and have a few laughs"
};
struct names {                  // 第1个结构
char first[LEN];
char last[LEN];
```

```c
};
struct guy {                               // 第2个结构
struct names handle;       // 嵌套结构
char favfood[LEN];
char job[LEN];
float income;
};
int main(void)
{
struct guy fellow = {        // 初始化一个结构变量
{ "Ewen", "Villard" },
"grilled salmon",
"personality coach",
68112.00
};
printf("Dear %s, \n\n", fellow.handle.first);
printf("%s%s.\n", msgs[0], fellow.handle.first);
printf("%s%s\s\n", msgs[1], fellow.job);
printf("%s\n", msgs[2]);
```

printf("%s%s%s", msgs[3], fellow.favfood, msgs[4]);

if (fellow.income > 150000.0)

puts("!!");

else if (fellow.income > 75000.0)

puts("!");

else

puts(".");

printf("\n%40s%s\n", " ", "See you soon,");

printf("%40s%s\n", " ", "Shalala");

return 0;

}

下面是该程序的输出:

Dear Ewen,

Thank you for the wonderful evening, Ewen.

You certainly prove that a personality coach

is a special kind of guy.We must get together

over a delicious grilled salmon and have a few laughs.

See you soon,

Shalala

首先，注意如何在结构声明中创建嵌套结构。和声明int类型变量一样，进行简单的声明:

struct names handle;

该声明表明handle是一个struct name类型的变量。当然，文件中也应包含结构names的声明。

其次，注意如何访问嵌套结构的成员，这需要使用两次点运算符:

printf("Hello, %s!\n", fellow.handle.first);

从左往右解释fellow.handle.first:

(fellow.handle).first

也就是说，找到fellow，然后找到fellow的handle的成员，再找到handle的first成员。

## 14.6 指向结构的指针

喜欢使用指针的人一定很高兴能使用指向结构的指针。至少有 4 个理由可以解释为何要使用指向结构的指针。第一，就像指向数组的指针比数组本身更容易操控（如，排序问题）一样，指向结构的指针通常比结构本身更容易操控。第二，在一些早期的C实现中，结构不能作为参数传递给函数，但是可以传递指向结构的指针。第三，即使能传递一个结构，传递指针通常更有效率。第四，一些用于表示数据的结构中包含指向其他结构的指针。

下面的程序（程序清单14.4）演示了如何定义指向结构的指针和如何用这样的指针访问结构的成员。

程序清单**14.4 friends.c**程序

/\* friends.c -- 使用指向结构的指针 \*/

```c
#include <stdio.h>

#define LEN 20

struct names {

char first[LEN];

char last[LEN];

};

struct guy {

struct names handle

char favfood[LEN]

char job[LEN];
```

```c
float income;
};
int main(void)
{
struct guy fellow[2] = {
{ { "Ewen", "Villard" },
"grilled salmon",
"personality coach",
68112.00
},
{ { "Rodney", "Swillbelly" },
"tripe",
"tabloid editor",
432400.00
}
};
struct guy * him;      /* 这是一个指向结构的指针 */
printf("address #1: %p #2: %p\n", &fellow[0], &fellow[1]);
him = &fellow[0];     /* 告诉编译器该指针指向何处 */
```

```c
printf("pointer #1: %p #2: %p\n", him, him + 1);
printf("him->income is \$%.2f: (*him).income is \$%.2f\n",
him->income, (*him).income);
him++; /* 指向下一个结构 */
printf("him->favfood is %s: him->handle.last is %s\n",
him->favfood, him->handle.last);
return 0;
}
```

该程序的输出如下:

```txt
address #1: 0x7fff5fbff820 #2: 0x7fff5fbff874
pointer #1: 0x7fff5fbff820 #2: 0x7fff5fbff874
him->income is \$68112.00: (*him).income is \$68112.00
him->favfood is tripe: him->handle.last is Swillbelly
```

我们先来看如何创建指向guy类型结构的指针，然后再分析如何通过该指针指定结构的成员。

## 14.6.1 声明和初始化结构指针

声明结构指针很简单:

struct guy \* him;

首先是关键字 struct，其次是结构标记 guy，然后是一个星号（\*），其后跟着指针名。这个语法和其他指针声明一样。

该声明并未创建一个新的结构，但是指针him现在可以指向任意现有的guy类型的结构。例如，如果barney是一个guy类型的结构，可以这样写:

$$
\text {him} = \& \text {barney};
$$

和数组不同的是，结构名并不是结构的地址，因此要在结构名前面加上&运算符。

在本例中，fellow 是一个结构数组，这意味着 fellow[0]是一个结构。所以，要让 him 指向fellow[0]，可以这样写:

$$
\text {him} = \& \text {fellow} [ 0 ];
$$

输出的前两行说明赋值成功。比较这两行发现，him指向fellow[0]，him + 1指向fellow[1]。注意，him加1相当于him指向的地址加84。在十六进制中，874 - 820 = 54（十六进制）= 84（十进制），因为每个guy结构都占用84字节的内存:names.first占用20字节，names.last占用20字节，favfood占用20字节，job占用20字节，income占用4字节（假设系统中float占用4字节）。顺带一提，在有些系统中，一个结构的大小可能大于它各成员大小之和。这是因为系统对数据进行校准的过程中产生了一些“缝隙”。例如，有些系统必须把每个成员都放在偶数地址上，或4的倍数的地址上。在这种系统中，结构的内部就存在未使用的“缝隙”。

## 14.6.2 用指针访问成员

指针him指向结构变量fellow[0]，如何通过him获得fellow[0]的成员的值？程序清单14.4中的第3行输出演示了两种方法。

第1种方法也是最常用的方法:使用->运算符。该运算符由一个连接号（-）后跟一个大于号（>）组成。我们有下面的关系:

如果him == &barney，那么him->income 即是 barney.income

如果him == &fellow[0]，那么him->income 即是 fellow[0].income

换句话说，->运算符后面的结构指针和.运算符后面的结构名工作方式相同（不能写成him.incone，因为him不是结构名）。

这里要着重理解him是一个指针，但是hime->income是该指针所指向结构的一个成员。所以在该例中，him->income是一个float类型的变量。

第2种方法是，以这样的顺序指定结构成员的值:如果him == &fellow[0]，那么\*him == fellow[0]，因为&和\*是一对互逆运算符。因此，可以做以下替代:

$$
\text {fellow} [ 0 ]. \text {income} = = (* \text {him}). \text {income}
$$

必须要使用圆括号，因为.运算符比\*运算符的优先级高。

总之，如果him是指向guy类型结构barney的指针，下面的关系恒成立:

$$
\text {barney.income} = (* \text {him}). \text {income} = \text {him-} > \text {income} / / \text {假设 him} = = \& \text {barney}
$$

接下来，我们来学习结构和函数的交互。

## 14.7 向函数传递结构的信息

函数的参数把值传递给函数。每个值都是一个数字——可能是int类型、float类型，可能是ASCII字符码，或者是一个地址。然而，一个结构比一个单独的值复杂，所以难怪以前的C实现不允许把结构作为参数传递给函数。当前的实现已经移除了这个限制，ANSI C允许把结构作为参数使用。所以程序员可以选择是传递结构本身，还是传递指向结构的指针。如果你只关心结构中的某一部分，也可以把结构的成员作为参数。我们接下来将分析这3种传递方式，首先介绍以结构成员作为参数的情况。

## 14.7.1 传递结构成员

只要结构成员是一个具有单个值的数据类型（即，int及其相关类型、char、float、double或指针），便可把它作为参数传递给接受该特定类型的函数。程序清单14.5中的财务分析程序（初级版本）演示了这一点，该程序把客户的银行账户添加到他/她的储蓄和贷款账户中。

程序清单**14.5 funds1.c**程序

/\* funds1.c -- 把结构成员作为参数传递 \*/

#include &lt;stdio.h&gt;

#define FUNDLEN 50

struct funds {

char bank[FUNDLEN];

double bankfund;

char save[FUNDLEN];

double savefund;

```c
};
double sum(double, double);
int main(void)
{
struct funds stan = {
"Garlic-Melon Bank",
4032.27,
"Lucky's Savings and Loan",
8543.94
};
printf("Stan has a total of \$%.2f.\n",
sum(stan.bankfund, stan.savefund));
return 0;
}
/* 两个double类型的数相加 */
double sum(double x, double y)
{
return(x + y);
}
```

运行该程序后输出如下:

Stan has a total of \$12576.21.

看来，这样传递参数没问题。注意，sum()函数既不知道也不关心实际的参数是否是结构的成员，它只要求传入的数据是double类型。

当然，如果需要在被调函数中修改主调函数中成员的值，就要传递成员的地址:

modify(&stan.bankfund);

这是一个更改银行账户的函数。

把结构的信息告诉函数的第2种方法是，让被调函数知道自己正在处理一个结构。

## 14.7.2 传递结构的地址

我们继续解决前面的问题，但是这次把结构的地址作为参数。由于函数要处理funds结构，所以必须声明funds结构。如程序清单14.6所示。

程序清单**14.6 funds2.c**程序

/\* funds2.c -- 传递指向结构的指针 \*/

#include &lt;stdio.h&gt;

#define FUNDLEN 50

struct funds {

char bank[FUNDLEN];

double bankfund;

```c
char save[FUNDLEN];
double savefund;
};
double sum(const struct funds *); /* 参数是一个指针 */
int main(void)
{
struct funds stan = {
"Garlic-Melon Bank",
4032.27,
"Lucky's Savings and Loan",
8543.94
};
printf("Stan has a total of \$%.2f.\n", sum(&stan));
return 0;
}
double sum(const struct funds * money)
{
return(money->bankfund + money->savefund);
}
```

运行该程序后输出如下:

Stan has a total of \$12576.21.

sum()函数使用指向funds结构的指针（money）作为它的参数。把地址&stan传递给该函数，使得指针money指向结构stan。然后通过->运算符获取stan.bankfund和stan.savefund的值。由于该函数不能改变指针所指向值的内容，所以把money声明为一个指向const的指针。

虽然该函数并未使用其他成员，但是也可以访问它们。注意，必须使用&运算符来获取结构的地址。和数组名不同，结构名只是其地址的别名。

## 14.7.3 传递结构

对于允许把结构作为参数的编译器，可以把程序清单14.6重写为程序清单14.7。

程序清单**14.7 funds3.c**程序

/\* funds3.c -- 传递一个结构 \*/

#include &lt;stdio.h&gt;

#define FUNDLEN 50

struct funds {

char bank[FUNDLEN];

double bankfund;

char save[FUNDLEN];

double savefund;

};

double sum(struct funds moolah); /\* 参数是一个结构 \*/

int main(void)

struct funds stan = {

"Garlic-Melon Bank",

4032.27,

"Lucky's Savings and Loan",

8543.94

printf("Stan has a total of \$%.2f.\n", sum(stan));

return 0;

}

double sum(struct funds moolah)

{

return(moolah.bankfund + moolah.savefund);

}

下面是运行该程序后的输出:

Stan has a total of \$12576.21.

该程序把程序清单14.6中指向struct funds类型的结构指针money替换成struct funds类型的结构变量moolah。调用sum()时，编译器根据funds模板创建了一个名为moolah的自动结构变量。然后，该结构的各成员被初始化为 stan结构变量相应成员的值的副本。因此，程序使用原来结构的副本进行计算，然而，传递指针的程序清单14.6使用的是原始的结构进行计算。由于moolah是一个结构，所以该程序使用moolah.bankfund，而不是moolah->bankfund。另一方面，由于money是指针，不是结构，所以程序清单14.6使用的是monet->bankfund。

## 14.7.4 其他结构特性

现在的C允许把一个结构赋值给另一个结构，但是数组不能这样做。也就是说，如果n\_data和o\_data都是相同类型的结构，可以这样做:

这条语句把n\_data的每个成员的值都赋给o\_data的相应成员。即使成员是数组，也能完成赋值。另外，还可以把一个结构初始化为相同类型的另一个结构:

struct names right\_field = {"Ruthie", "George"};

现在的C（包括ANSI C），函数不仅能把结构本身作为参数传递，还能把结构作为返回值返回。把结构作为函数参数可以把结构的信息传送给函数；把结构作为返回值的函数能把结构的信息从被调函数传回主调函数。结构指针也允许这种双向通信，因此可以选择任一种方法来解决编程问题。我们通过另一组程序示例来演示这两种方法。

为了对比这两种方法，我们先编写一个程序以传递指针的方式处理结构，然后以传递结构和返回结构的方式重写该程序。

程序清单**14.8 names1.c**程序

/\* names1.c -- 使用指向结构的指针 \*/

#include &lt;stdio.h&gt;

#include &lt;string.h&gt;

#define NLEN 30

struct namect {

char fname[NLEN];

char lname[NLEN];

int letters;

void getinfo(struct namect \*);

void makeinfo(struct namect \*);

void showinfo(const struct namect \*);

char \* s\_gets(char \* st, int n);

int main(void)

{

struct namect person;

getinfo(&person);

makeinfo(&person);

showinfo(&person);

```c
return 0;
}
void getinfo(struct namect * pst)
{
printf("Please enter your first name.\n");
s_gets(pst->fname, NLEN);
printf("Please enter your last name.\n");
s_gets(pst->lname, NLEN);
}
void makeinfo(struct namect * pst)
{
pst->letters = strlen(pst->fname) +strlen(pst->lname);
}
void showinfo(const struct namect * pst)
{
printf("%s %s, your name contains %d letters.\n",
pst->fname, pst->lname, pst->letters);
}
char * s_gets(char * st, int n)
```

```c
{
char * ret_val;

char * find;

ret_val = fgets(st, n, stdin);

if (ret_val)

{

find = strchr(st, '\n'); // 查找换行符

if (find) // 如果地址不是 NULL,

*find = '\0'; // 在此处放置一个空字符

else

while (getchar() != '\n')

continue; // 处理输入行的剩余字符

}

return ret_val;

}
```

下面是编译并运行该程序后的一个输出示例:

Please enter your first name.

## Viola

Please enter your last name.

## Plunderfest

Viola Plunderfest, your name contains 16 letters.

该程序把任务分配给3个函数来完成，都在main()中调用。每调用一个函数就把person结构的地址传递给它。

getinfo()函数把结构的信息从自身传递给main()。该函数通过与用户交互获得姓名，并通过pst指针定位，将其放入 person 结构中。由于 pst->lname意味着 pst 指向结构的 lname 成员，这使得pst->lname等价于char数组的名称，因此做s\_gets()的参数很合适。注意，虽然getinfo()给main()提供了信息，但是它并未使用返回机制，所以其返回类型是void。

makeinfo()函数使用双向传输方式传送信息。通过使用指向 person 的指针，该指针定位了储存在该结构中的名和姓。该函数使用C库函数strlen()分别计算名和姓中的字母总数，然后使用person的地址储存两数之和。同样，makeinfo()函数的返回类型也是void。

showinfo()函数使用一个指针定位待打印的信息。因为该函数不改变数组的内容，所以将其声明为const。

所有这些操作中，只有一个结构变量 person，每个函数都使用该结构变量的地址来访问它。一个函数把信息从自身传回主调函数，一个函数把信息从主调函数传给自身，一个函数通过双向传输来传递信息。

现在，我们来看如何使用结构参数和返回值来完成相同的任务。第一，为了传递结构本身，函数的参数必须是person，而不是&person。那么，相应的形式参数应声明为struct namect，而不是指向该类型的指针。第二，可以通过返回一个结构，把结构的信息返回给main()。程序清单14.9演示了不使用指针的版本。

程序清单**14.9 names2.c**程序

/\* names2.c -- 传递并返回结构 \*/

```c
#include <stdio.h>

#include <string.h>

#define NLEN 30

struct namect {

char fname[NLEN];

char lname[NLEN];

int letters;

};

struct namect getinfo(void);

struct namect makeinfo(struct namect);

void showinfo(struct namect);

char * s_gets(char * st, int n);

int main(void)

{

struct namect person;

person = getinfo();

person = makeinfo(person);

showinfo(person);

return 0;
```

```c
}
struct namect getinfo(void)
{
struct namect temp;
printf("Please enter your first name.\n");
s_gets(temp.fname, NLEN);
printf("Please enter your last name.\n");
s_gets(temp.lname, NLEN);
return temp;
}
struct namect makeinfo(struct namect info)
{
info.letters = strlen(info.fname) + strlen(info.lname);
return info;
}
void showinfo(struct namect info)
{
printf("%s %s, your name contains %d letters.\n",
info.fname, info.lname, info.letters);
```

```c
}
char * s_gets(char * st, int n)
{
char * ret_val;
char * find;
ret_val = fgets(st, n, stdin);
if (ret_val)
{
find = strchr(st, '\n');    // 查找换行符
if (find)                      // 如果地址不是 NULL,
*find = '\0';          // 在此处放置一个空字符
else
while (getchar() != '\n')
continue;              // 处理输入行的剩余部分
}
return ret_val;
}
```

该版本最终的输出和前面版本相同，但是它使用了不同的方式。程序中的每个函数都创建了自己的person备份，所以该程序使用了4个不同的结构，不像前面的版本只使用一个结构。

例如，考虑makeinfo()函数。在第1个程序中，传递的是person的地址，该函数实际上处理的是person的值。在第2个版本的程序中，创建了一个新的结构info。储存在person中的值被拷贝到info中，函数处理的是这个副本。因此，统计完字母个数后，计算结果储存在info中，而不是person中。然而，返回机制弥补了这一点。makeinfo()中的这行代码:

return info;

与main()中的这行结合:

$$
\text {person} = \text {makeinfo(person)};
$$

把储存在info中的值拷贝到person中。注意，必须把makeinfo()函数声明为struct namect类型，所以该函数要返回一个结构。

## 14.7.5 结构和结构指针的选择

假设要编写一个与结构相关的函数，是用结构指针作为参数，还是用结构作为参数和返回值？两者各有优缺点。

把指针作为参数有两个优点:无论是以前还是现在的C实现都能使用这种方法，而且执行起来很快，只需要传递一个地址。缺点是无法保护数据。被调函数中的某些操作可能会意外影响原来结构中的数据。不过，ANSI C新增的const限定符解决了这个问题。例如，如果在程序清单14.8中，showinfo()函数中的代码改变了结构的任意成员，编译器会捕获这个错误。

把结构作为参数传递的优点是，函数处理的是原始数据的副本，这保护了原始数据。另外，代码风格也更清楚。假设定义了下面的结构类型:

struct vector {double x; double y;};

如果用vector类型的结构ans储存相同类型结构a和b的和，就要把结构作为参数和返回值:

```matlab
struct vector ans, a, b;

struct vector sum_vect(struct vector, struct vector);

...

ans = sum_vect(a,b);
```

对程序员而言，上面的版本比用指针传递的版本更自然。指针版本如下:

```c
struct vector ans, a, b;

void sum_vect(const struct vector *, const struct vector *, struct vector *);
...

sum_vect(&a, &b, &ans);
```

另外，如果使用指针版本，程序员必须记住总和的地址应该是第1个参数还是第2个参数的地址。

传递结构的两个缺点是:较老版本的实现可能无法处理这样的代码，而且传递结构浪费时间和存储空间。尤其是把大型结构传递给函数，而它只使用结构中的一两个成员时特别浪费。这种情况下传递指针或只传递函数所需的成员更合理。

通常，程序员为了追求效率会使用结构指针作为函数参数，如需防止原始数据被意外修改，使用const限定符。按值传递结构是处理小型结构最常用的方法。

## 14.7.6 结构中的字符数组和字符指针

到目前为止，我们在结构中都使用字符数组来储存字符串。是否可以使用指向 char 的指针来代替字符数组？例如，程序清单14.3中有如下声明:

```txt
#define LEN 20

struct names {

char first[LEN];

char last[LEN];

};
```

其中的结构声明是否可以这样写:

```txt
struct pnames {

char * first;

char * last;

};
```

当然可以，但是如果不理解这样做的含义，可能会有麻烦。考虑下面的代码:

```txt
struct names veep = {"Talia", "Summers"};
struct pnames treas = {"Brad", "Fallingjaw"};
printf("%s and %s\n", veep.first, treas.first);
```

以上代码都没问题，也能正常运行，但是思考一下字符串被储存在何处。对于struct names类型的结构变量veep，以上字符串都储存在结构内部，结构总共要分配40字节储存姓名。然而，对于struct pnames类型的结构变量treas，以上字符串储存在编译器储存常量的地方。结构本身只储存了两个地址，在我们的系统中共占16字节。尤其是，struct pnames结构不用为字符串分配任何存储空间。它使用的是储存在别处的字符串（如，字符串常量或数组中的字符串）。简而言之，在pnames结构变量中的指针应该只用来在程序中管理那些已分配和在别处分配的字符串。

我们看看这种限制在什么情况下出问题。考虑下面的代码:

struct names accountant;

struct pnames attorney;

puts("Enter the last name of your accountant:");

scanf("%s", accountant.last);

puts("Enter the last name of your attorney:");

scanf("%s", attorney.last); /\* 这里有一个潜在的危险 \*/

就语法而言，这段代码没问题。但是，用户的输入储存到哪里去了？对于会计师（accountant），他的名储存在accountant结构变量的last成员中，该结构中有一个储存字符串的数组。对于律师（attorney），scanf()把字符串放到attorney.last表示的地址上。由于这是未经初始化的变量，地址可以是任何值，因此程序可以把名放在任何地方。如果走运的话，程序不会出问题，至少暂时不会出问题，否则这一操作会导致程序崩溃。实际上，如果程序能正常运行并不是好事，因为这意味着一个未被觉察的危险潜伏在程序中。

因此，如果要用结构储存字符串，用字符数组作为成员比较简单。用指向 char 的指针也行，但是误用会导致严重的问题。

## 14.7.7 结构、指针和malloc()

如果使用malloc()分配内存并使用指针储存该地址，那么在结构中使用指针处理字符串就比较合理。这种方法的优点是，可以请求malloc()为字符串分配合适的存储空间。可以要求用4字节储存"Joe"和用18字节储存"Rasolofomasoandro"。用这种方法改写程序清单14.9并不费劲。主要是更改结构声明（用指针代替数组）和提供一个新版本的getinfo()函数。新的结

构声明如下:

```c
struct namect {

char * fname; // 用指针代替数组

char * lname;

int letters;

};
```

新版本的getinfo()把用户的输入读入临时数组中，调用malloc()函数分配存储空间，并把字符串拷贝到新分配的存储空间中。对名和姓都要这样做:

```c
void getinfo (struct namect * pst)
{
char temp[SLEN];
printf("Please enter your first name.\n");
s_gets(temp, SLEN);
// 分配内存储存名
pst->fname = (char *) malloc(strlen(temp) + 1);
// 把名拷贝到已分配的内存
strcpy(pst->fname, temp);
printf("Please enter your last name.\n");
s_gets(temp, SLEN);
```

```txt
pst->lname = (char *) malloc(strlen(temp) + 1);

strcpy(pst->lname, temp);

}
```

要理解这两个字符串都未储存在结构中，它们储存在 malloc()分配的内存块中。然而，结构中储存着这两个字符串的地址，处理字符串的函数通常都要使用字符串的地址。因此，不用修改程序中的其他函数。

第12章建议，应该成对使用malloc()和free()。因此，还要在程序中添加一个新的函数cleanup()，用于释放程序动态分配的内存。如程序清单14.10所示。

程序清单**14.10 names3.c**程序

```c
// names3.c -- 使用指针和 malloc()
#include <stdio.h>
#include <string.h> // 提供 strcpy()、strlen() 的原型
#include <stdlib.h> // 提供 malloc()、free() 的原型
#define SLEN 81
struct namect {
char * fname; // 使用指针
char * lname;
int letters;
};
```

```c
void getinfo(struct namect *);      // 分配内存
void makeinfo(struct namect *);
void showinfo(const struct namect *);
void cleanup(struct namect *);      // 调用该函数时释放内存
char * s_gets(char * st, int n);
int main(void)
{
struct namect person;
getinfo(&person);
makeinfo(&person);
showinfo(&person);
cleanup(&person);
return 0;
}
void getinfo(struct namect * pst)
{
char temp[SLEN];
printf("Please enter your first name.\n");
s_gets(temp, SLEN);
```