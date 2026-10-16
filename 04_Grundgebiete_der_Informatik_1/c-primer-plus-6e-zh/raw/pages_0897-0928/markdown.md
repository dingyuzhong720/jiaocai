```c
int rand1(void)
{
/*生成伪随机数的魔术公式*/
next = next * 1103515245 + 12345;
return (unsigned int) (next / 65536) % 32768;
}
void srand1(unsigned int seed)
{
next = seed;
}
```

注意，next是具有内部链接的文件作用域静态变量。这意味着rand1()和srand1()都可以使用它，但是其他文件中的函数无法访问它。使用程序清单12.10的驱动程序测试这两个函数。

程序清单**12.10 r\_drive1.c**驱动程序

/\* r\_drive1.c -- 测试 rand1() 和 srand1() \*/

/\* 与 s\_and\_r.c 一起编译 \*/

#include &lt;stdio.h&gt;

#include &lt;stdlib.h&gt;

extern void srand1(unsigned int x);

extern int rand1(void);

```c
int main(void)
{
int count;
unsigned seed;
printf("Please enter your choice for seed.\n");
while (scanf("%u", &seed) == 1)
{
srand1(seed); /* 重置种子 */
for (count = 0; count < 5; count++)
printf("%d\n", rand1());
printf("Please enter next seed (q to quit):\n");
}
printf("Done\n");
return 0;
}
```

编译两个文件，运行该程序后，其输出如下:

```csv
1
16838
5758
```

10113
17515
31051
**513**
20067
23475
8955
20841
15324
q
Done

Please enter next seed (q to quit):

Please enter next seed (q to quit):

设置seed的值为1，输出的结果与前面程序相同。但是设置seed的值为513后就得到了新的结果。

注意 自动重置种子

如果 C 实现允许访问一些可变的量（如，时钟系统），可以用这些值（可能会被截断）初始化种子值。例如，ANSI C有一个time()函数返回系统时间。虽然时间单元因系统而异，但是重点是该返回值是一个可进行运算的类型，而且其值随着时间变化而变化。time()返回值的类型名是time\_t，具体类型与系统有关。这没关系，我们可以使用强制类型转换:

#include &lt;time.h&gt; /\* 提供time()的ANSI原型\*/

srand1((unsigned int) time(0)); /\* 初始化种子 \*/

一般而言，time()接受的参数是一个 time\_t 类型对象的地址，而时间值就储存在传入的地址上。当然，也可以传入空指针（0）作为参数，这种情况下，只能通过返回值机制来提供值。

可以把这个技巧应用于标准的ANSI C函数srand()和rand()中。如果使用这些函数，要在文件中包含stdlib.c头文件。实际上，既然已经明白了srand1()和rand1()如何使用内部链接的静态变量，你也可以使用编译器提供的版本。我们将在下一个示例中这样做。

## 12.3 掷骰子

我们将要模拟一个非常流行的游戏——掷骰子。骰子的形式多种多样，最普遍的是使用两个6面骰子。在一些冒险游戏中，会使用5种骰子:4面、6面、8面、12面和20面。聪明的古希腊人证明了只有5种正多面体，它们的所有面都具有相同的形状和大小。各种不同类型的骰子就是根据这些正多面体发展而来。也可以做成其他面数的，但是其所有的面不会都相等，因此各个面朝上的几率就不同。

计算机计算不用考虑几何的限制，所以可以设计任意面数的电子骰子。我们先从6面开始。

我们想获得1～6的随机数。然而，rand()生成的随机数在0～ RAND\_MAX之间。RAND\_MAX被定义在stdlib.h中，其值通常是INT\_MAX。因此，需要进行一些调整，方法如下。

1.把随机数求模6，获得的整数在0～5之间。
2.结果加1，新值在1～6之间。
3.为方便以后扩展，把第1步中的数字6替换成骰子面数。

下面的代码实现了这3个步骤:

#include &lt;stdlib.h&gt; /\* 提供rand()的原型 \*/

```txt
int rollem(int sides)
{
int roll;
roll = rand() % sides + 1;
return roll;
```

```txt
}
```

我们还想用一个函数提示用户选择任意面数的骰子，并返回点数总和。如程序清单12.11所示。

程序清单12.11 diceroll.c程序

```c
/* diceroll.c -- 掷骰子模拟程序 */

/* 与 mandydice.c 一起编译 */

#include "diceroll.h"

#include <stdio.h>

#include <stdlib.h>          /* 提供库函数 rand()的原型 */
int roll_count = 0;           /* 外部链接 */

static int rollem(int sides)   /* 该函数属于该文件私有 */

{

int  roll;

roll = rand() % sides + 1;

++roll_count;                 /* 计算函数调用次数 */

return  roll;

}

int  roll_n_dice(int dice, int sides)

{
```

```c
int d;

int total = 0;

if (sides < 2)

{
printf("Need at least 2 sides.\n");
return -2;
}

if (dice < 1)
{
printf("Need at least 1 die.\n");
return -1;
}

for (d = 0; d < dice; d++)
total += rollem(sides);
return total;
}
```

该文件加入了新元素。第一，rollem()函数属于该文件私有，它是roll\_n\_dice()的辅助函数。第二，为了演示外部链接的特性，该文件声明了一个外部变量roll\_count。该变量统计调用rollem()函数的次数。这样设计有点蹩脚，仅为了演示外部变量的特性。第三，该文件包含以下预处理指令:

#include "diceroll.h"

如果使用标准库函数，如 rand()，要在当前文件中包含标准头文件（对rand()而言要包含stdlib.h），而不是声明该函数。因为头文件中已经包含了正确的函数原型。我们效仿这一做法，把roll\_n\_dice()函数的原型放在diceroll.h头文件中。把文件名放在双引号中而不是尖括号中，指示编译器在本地查找文件，而不是到编译器存放标准头文件的位置去查找文件。“本地查找”的含义取决于具体的实现。一些常见的实现把头文件与源代码文件或工程文件（如果编译器使用它们的话）放在相同的目录或文件夹中。程序清单12.12是头文件中的内容。

程序清单**12.12 diceroll.h**文件

//diceroll.h

extern int roll\_count;

int roll\_n\_dice(int dice, int sides);

该头文件中包含一个函数原型和一个 extern 声明。由于 direroll.c 文件包含了该文件， direroll.c实际上包含了roll\_count的两个声明:

extern int roll\_count; // 头文件中的声明（引用式声明）

int roll\_count = 0; // 源代码文件中的声明（定义式声明）

这样做没问题。一个变量只能有一个定义式声明，但是带 extern 的声明是引用式声明，可以有多个引用式声明。

使用 roll\_n\_dice()函数的程序都要包含 diceroll.c 头文件。包含该头文件后，程序便可使用roll\_n\_dice()函数和roll\_count变量。如程序清单12.13所示。

程序清单**12.13 manydice.c**文件

/\* manydice.c -- 多次掷骰子的模拟程序 \*/

/\* 与 diceroll.c 一起编译\*/

#include &lt;stdio.h&gt;

#include &lt;stdlib.h&gt; /\* 为库函数 srand() 提供原型 \*/

#include &lt;time.h&gt; /\* 为 time() 提供原型 \*/

#include "diceroll.h" /\* 为roll\_n\_dice()提供原型，为roll\_count变量提供声明 \*/

```c
int main(void)
{
int dice, roll;
int sides;
int status;
```

srand((unsigned int) time(0)); /\* 随机种子 \*/

printf("Enter the number of sides per die, 0 to stop.\n");

while (scanf("%d", &sides) == 1 && sides > 0)

printf("How many dice?\n");

if ((status = scanf("%d", &dice)) != 1)

{

```c
if (status == EOF)
break;          /* 退出循环 */
else
{
printf("You should have entered an integer.");
printf(" Let's begin again.\n");
while (getchar() != '\n')
continue;      /* 处理错误的输入 */
printf("How many sides? Enter 0 to stop.\n");
continue;            /* 进入循环的下一轮迭代 */
}
}
roll = roll_n_dice(dice, sides);
printf("You have rolled a %d using %d %d-sided dice.\n",
roll, dice, sides);
printf("How many sides? Enter 0 to stop.\n");
}
printf("The rollem() function was called %d times.\n",
roll_count);       /* 使用外部变量 */
```

```c
printf("GOOD FORTUNE TO YOU!\n");
return 0;
}
```

要与包含程序清单12.11的文件一起编译该文件。可以把程序清单12.11、12.12和12.13都放在同一文件夹或目录中。运行该程序，下面是一个输出示例:

Enter the number of sides per die, 0 to stop.

6

How many dice?

2

You have rolled a 12 using 2 6-sided dice.

How many sides? Enter 0 to stop.

6

How many dice?

2

You have rolled a 4 using 2 6-sided dice.

How many sides? Enter 0 to stop.

6

How many dice?

2

You have rolled a 5 using 2 6-sided dice.

How many sides? Enter 0 to stop.

0

The rollem() function was called 6 times.

GOOD FORTUNE TO YOU!

因为该程序使用了srand()随机生成随机数种子，所以大多数情况下，即使输入相同也很难得到相同的输出。注意，manydice.c中的main()访问了定义在diceroll.c中的roll\_count变量。

有3种情况可以导致外层while循环结束:side小于1、输入类型不匹配（此时scanf()返回0）、遇到文件结尾（返回值是EOF）。为了读取骰子的点数，该程序处理文件结尾的方式（退出while循环）与处理类型不匹配（进入循环的下一轮迭代）的情况不同。

可以通过多种方式使用roll\_n\_dice()。sides等于2时，程序模仿掷硬币，“正面朝上”为2，“反面朝上”为1（或者反过来表示也行）。很容易修改该程序单独显示点数的结果，或者构建一个骰子模拟器。如果要掷多次骰子（如在一些角色扮演类游戏中），可以很容易地修改程序以输出类似的结果:

Enter the number of sets; enter q to stop.

**18**

How many sides and how many dice?

**6 3**

Here are 18 sets of 3 6-sided throws.

12 10 6 9 8 14 8 15 9 14 12 17 11 7 10

13 8 14

How many sets? Enter q to stop.

q

rand1()或 rand()（不是 rollem()）还可以用来创建一个猜数字程序，让计算机选定一个数字，你来猜。读者感兴趣的话可以自己编写这个程序。

## 12.4 分配内存:malloc()和free()

我们前面讨论的存储类别有一个共同之处:在确定用哪种存储类别后，根据已制定好的内存管理规则，将自动选择其作用域和存储期。然而，还有更灵活地选择，即用库函数分配和管理内存。

首先，回顾一下内存分配。所有程序都必须预留足够的内存来储存程序使用的数据。这些内存中有些是自动分配的。例如，以下声明:

float x;

char place[] = "Dancing Oxen Creek";

为一个float类型的值和一个字符串预留了足够的内存，或者可以显式指定分配一定数量的内存:

int plates[100];

该声明预留了100个内存位置，每个位置都用于储存int类型的值。声明还为内存提供了一个标识符。因此，可以使用x或place识别数据。回忆一下，静态数据在程序载入内存时分配，而自动数据在程序执行块时分配，并在程序离开该块时销毁。

C 能做的不止这些。可以在程序运行时分配更多的内存。主要的工具是malloc()函数，该函数接受一个参数:所需的内存字节数。malloc()函数会找到合适的空闲内存块，这样的内存是匿名的。也就是说， malloc()分配内存，但是不会为其赋名。然而，它确实返回动态分配内存块的首字节地址。因此，可以把该地址赋给一个指针变量，并使用指针访问这块内存。因为char表示1字节，malloc()的返回类型通常被定义为指向char的指针。然而，从ANSI C标准开始，C使用一个新的类型:指向void的指针。该类型相当于一个“通用指针”。malloc()函数可用于返回指向数组的指针、指向结构的指针等，所以通常该函数的返回值会被强制转换为匹配的类型。在ANSI C中，应该坚持使用强制类型转换，提高代码的可读性。然而，把指向 void的指针赋给任意类型的指针完全不用考虑类型匹配的问题。如果 malloc()分配内存失败，将返回空指针。

我们试着用 malloc()创建一个数组。除了用 malloc()在程序运行时请求一块内存，还需要一个指针记录这块内存的位置。例如，考虑下面的代码:

$$
\text {double} * \text {ptd};
$$

$$
\mathrm{ptd} = (\text {double} *) \text {malloc} (3 0 * \text {sizeof} (\text {double}));
$$

以上代码为30个double类型的值请求内存空间，并设置ptd指向该位置。注意，指针ptd被声明为指向一个double类型，而不是指向内含30个double类型值的块。回忆一下，数组名是该数组首元素的地址。因此，如果让ptd指向这个块的首元素，便可像使用数组名一样使用它。也就是说，可以使用表达式ptd[0]访问该块的首元素，ptd[1]访问第2个元素，以此类推。根据前面所学的知识，可以使用数组名来表示指针，也可以用指针来表示数组。

现在，我们有3种创建数组的方法。

声明数组时，用常量表达式表示数组的维度，用数组名访问数组的元素。可以用静态内存或自动内存创建这种数组。

声明变长数组（C99新增的特性）时，用变量表达式表示数组的维度，用数组名访问数组的元素。具有这种特性的数组只能在自动内存中创建。

声明一个指针，调用malloc()，将其返回值赋给指针，使用指针访问数组的元素。该指针可以是静态的或自动的。

使用第2种和第3种方法可以创建动态数组（dynamic array）。这种数组和普通数组不同，可以在程序运行时选择数组的大小和分配内存。例如，假设n是一个整型变量。在C99之前，不能这样做:

double item[n]; /\* C99之前:n不允许是变量 \*/

但是，可以这样做:

$$
\mathrm{ptd} = (\text {double} *) \text {malloc} (\mathrm{n} * \text {sizeof} (\text {double})); / * \text {可以} * /
$$

如你所见，这比变长数组更灵活。

通常，malloc()要与free()配套使用。free()函数的参数是之前malloc()返回的地址，该函数释放之前malloc()分配的内存。因此，动态分配内存的存储期从调用malloc()分配内存到调用free()释放内存为止。设想malloc()和free()管理着一个内存池。每次调用malloc()分配内存给程序使用，每次调用free()把内存归还内存池中，这样便可重复使用这些内存。free()的参数应该是一个指针，指向由 malloc()分配的一块内存。不能用 free()释放通过其他方式（如，声明一个数组）分配的内存。malloc()和free()的原型都在stdlib.h头文件中。

使用malloc()，程序可以在运行时才确定数组大小。如程序清单12.14所示，它把内存块的地址赋给指针 ptd，然后便可以使用数组名的方式使用ptd。另外，如果内存分配失败，可以调用 exit()函数结束程序，其原型在stdlib.h中。EXIT\_FAILURE的值也被定义在stdlib.h中。标准提供了两个返回值以保证在所有操作系统中都能正常工作:EXIT\_SUCCESS（或者，相当于0）表示普通的程序结束， EXIT\_FAILURE 表示程序异常中止。一些操作系统（包括 UNIX、Linux 和 Windows）还接受一些表示其他运行错误的整数值。

程序清单**12.14 dyn\_arr.c**程序

```c
/* dyn_arr.c -- 动态分配数组 */

#include <stdio.h>

#include <stdlib.h> /* 为 malloc()、free()提供原型 */
int main(void)

{
```

```c
double * ptd;

int max;

int number;

int i = 0;

puts("What is the maximum number of type double entries?");
if (scanf("%d", &max) != 1)

{

puts("Number not correctly entered -- bye-.");

exit(EXIT_FAILURE);

}

ptd = (double *) malloc(max * sizeof(double));

if (ptd == NULL)

{

puts("Memory allocation failed. Goodbye-.");

exit(EXIT_FAILURE);

}

/* ptd 现在指向有max个元素的数组 */

puts("Enter the values (q to quit):");

while (i < max && scanf("%lf", &ptd[i]) == 1)
```

```txt
++i;

printf("Here are your %d entries:\n", number = i);

for (i = 0; i < number; i++)

{
printf("%7.2f ", ptd[i]);

if (i % 7 == 6)

putchar('\n');

}

if (i % 7 != 0)

putchar('\n');

puts("Done.");

free(ptd);

return 0;

}
```

下面是该程序的运行示例。程序通过交互的方式让用户先确定数组的大小，我们设置数组大小为 5。虽然我们后来输入了6个数，但程序也只处理前5个数。

What is the maximum number of entries?

5

Enter the values (q to quit):

**20 30 35 25 40 80**

Here are your 5 entries:

20.00 30.00 35.00 25.00 40.00

Done.

该程序通过以下代码获取数组的大小:

```c
if (scanf("%d", &max) != 1)
{
puts("Number not correctly entered -- bye.");
exit(EXIT_FAILURE);
}
```

接下来，分配足够的内存空间以储存用户要存入的所有数，然后把动态分配的内存地址赋给指针ptd:

```txt
ptd = (double *) malloc(max * sizeof(double));
```

在C中，不一定要使用强制类型转换(double \*)，但是在C++中必须使用。所以，使用强制类型转换更容易把C程序转换为C++程序。

malloc()可能分配不到所需的内存。在这种情况下，该函数返回空指针，程序结束:

```txt
if (ptd == NULL)
{
puts("Memory allocation failed. Goodbye.");
```

```lisp
exit(EXIT_FAILURE);

}
```

如果程序成功分配内存，便可把ptd视为一个有max个元素的数组名。

注意，free()函数位于程序的末尾，它释放了malloc()函数分配的内存。free()函数只释放其参数指向的内存块。一些操作系统在程序结束时会自动释放动态分配的内存，但是有些系统不会。为保险起见，请使用free()，不要依赖操作系统来清理。

使用动态数组有什么好处？从本例来看，使用动态数组给程序带来了更多灵活性。假设你已经知道，在大多数情况下程序所用的数组都不会超过100个元素，但是有时程序确实需要10000个元素。要是按照平时的做法，你不得不为这种情况声明一个内含 10000 个元素的数组。基本上这样做是在浪费内存。如果需要10001个元素，该程序就会出错。这种情况下，可以使用一个动态数组调整程序以适应不同的情况。

## 12.4.1 free()的重要性

静态内存的数量在编译时是固定的，在程序运行期间也不会改变。自动变量使用的内存数量在程序执行期间自动增加或减少。但是动态分配的内存数量只会增加，除非用 free()进行释放。例如，假设有一个创建数组临时副本的函数，其代码框架如下:

```txt
...

int main()
{
double glad[2000];
int i;
```

```c
...
for (i = 0; i < 1000; i++)
gobble(glad, 2000);

...
}
void gobble(double ar[], int n)
{
double * temp = (double *) malloc( n * sizeof(double));
.../* free(temp); // 假设忘记使用free() */
}
```

第1次调用gobble()时，它创建了指针temp，并调用malloc()分配了16000字节的内存（假设double为8 字节）。假设如代码注释所示，遗漏了free()。当函数结束时，作为自动变量的指针temp也会消失。但是它所指向的16000字节的内存却仍然存在。由于temp指针已被销毁，所以无法访问这块内存，它也不能被重复使用，因为代码中没有调用free()释放这块内存。

第2次调用gobble()时，它又创建了指针temp，并调用malloc()分配了16000字节的内存。第1次分配的16000字节内存已不可用，所以malloc()分配了另外一块16000字节的内存。当函数结束时，该内存块也无法被再访问和再使用。

循环要执行1000次，所以在循环结束时，内存池中有1600万字节被占用。实际上，也许在循环结束之前就已耗尽所有的内存。这类问题被称为内存泄漏（memory leak）。在函数末尾处调用free()函数可避免这类问题发生。

## 12.4.2 calloc()函数

分配内存还可以使用calloc()，典型的用法如下:

long \* newmem;

newmem = (long \*)calloc(100, sizeof (long));

和malloc()类似，在ANSI之前，calloc()也返回指向char的指针；在ANSI之后，返回指向void的指针。如果要储存不同的类型，应使用强制类型转换运算符。calloc()函数接受两个无符号整数作为参数（ANSI规定是size\_t类型）。第1个参数是所需的存储单元数量，第2个参数是存储单元的大小（以字节为单位）。在该例中，long为4字节，所以，前面的代码创建了100个4字节的存储单元，总共400字节。

用sizeof(long)而不是4，提高了代码的可移植性。这样，在其他long不是4字节的系统中也能正常工作。

calloc()函数还有一个特性:它把块中的所有位都设置为0（注意，在某些硬件系统中，不是把所有位都设置为0来表示浮点值0）。

free()函数也可用于释放calloc()分配的内存。

动态内存分配是许多高级程序设计技巧的关键。我们将在第17章中详细讲解。有些编译器可能还提供其他内存管理函数，有些可以移植，有些不可以。读者可以抽时间看一下。

## 12.4.3 动态内存分配和变长数组

变长数组（VLA）和调用 malloc()在功能上有些重合。例如，两者都可用于创建在运行时确定大小的数组:

```txt
int vlamal()
{
```

```c
int n;

int * pi;

scanf("%d", &n);

pi = (int *) malloc (n * sizeof(int));

int ar[n];// 变长数组

pi[2] = ar[2] = -5;

...

}
```

不同的是，变长数组是自动存储类型。因此，程序在离开变长数组定义所在的块时（该例中，即vlamal()函数结束时），变长数组占用的内存空间会被自动释放，不必使用 free()。另一方面，用malloc()创建的数组不必局限在一个函数内访问。例如，可以这样做:被调函数创建一个数组并返回指针，供主调函数访问，然后主调函数在末尾调用free()释放之前被调函数分配的内存。另外，free()所用的指针变量可以与 malloc()的指针变量不同，但是两个指针必须储存相同的地址。但是，不能释放同一块内存两次。

对多维数组而言，使用变长数组更方便。当然，也可以用 malloc()创建二维数组，但是语法比较繁琐。如果编译器不支持变长数组特性，就只能固定二维数组的维度，如下所示:

```txt
int n = 5;
int m = 6;
int ar2[n][m]; // n×m的变长数组（VLA）
int (*p2)[6]; // C99之前的写法
```

$$
\mathrm{p} 2 = (\text {int} (*) [ 6 ]) \operatorname{malloc} (\mathrm{n} * 6 * \text {sizeof(int)}); / / \mathrm{n} \times 6 \text {数组}
$$

$$
\mathrm{ar} 2 [ 1 ] [ 2 ] = \mathrm{p} 2 [ 1 ] [ 2 ] = 1 2;
$$

先复习一下指针声明。由于malloc()函数返回一个指针，所以p2必须是一个指向合适类型的指针。第1个指针声明:

$$
\text {int} (^ {*} \mathrm{p2}) [ 6 ]; / / \mathrm{C99之前的写法}
$$

表明p2指向一个内含6个int类型值的数组。因此，p2[i]代表一个由6个整数构成的元素，p2[i][j]代表一个整数。

第2个指针声明用一个变量指定p3所指向数组的大小。因此，p3代表一个指向变长数组的指针，这行代码不能在C90标准中运行。

## 12.4.4 存储类别和动态内存分配

存储类别和动态内存分配有何联系？我们来看一个理想化模型。可以认为程序把它可用的内存分为 3部分:一部分供具有外部链接、内部链接和无链接的静态变量使用；一部分供自动变量使用；一部分供动态内存分配。

静态存储类别所用的内存数量在编译时确定，只要程序还在运行，就可访问储存在该部分的数据。该类别的变量在程序开始执行时被创建，在程序结束时被销毁。

然而，自动存储类别的变量在程序进入变量定义所在块时存在，在程序离开块时消失。因此，随着程序调用函数和函数结束，自动变量所用的内存数量也相应地增加和减少。这部分的内存通常作为栈来处理，这意味着新创建的变量按顺序加入内存，然后以相反的顺序销毁。

动态分配的内存在调用 malloc()或相关函数时存在，在调用 free()后释放。这部分的内存由程序员管理，而不是一套规则。所以内存块可以在一个函数中创建，在另一个函数中销毁。正是因为这样，这部分的内存用于动态内存分配会支离破碎。也就是说，未使用的内存块分散在已使用的内存块之间。另外，使用动态内存通常比使用栈内存慢。

总而言之，程序把静态对象、自动对象和动态分配的对象储存在不同的区域。

程序清单12.15 where.c程序

```c
// where.c -- 数据被储存在何处?

#include <stdio.h>

#include <stdlib.h>

#include <string.h>

int static_store = 30;

const char *pcg="String Literal";

int main()
{
int auto_store = 40;

char auto_string [] = "Auto char Array";
int *pi;

char *pcl;

pi = (int *) malloc(sizeof(int));
```

```c
*pi = 35;
pcl = (char *) malloc(strlen("Dynamic String") + 1);
strcpy(pcl, "Dynamic String");
printf("static_store: %d at %p\n", static_store, &static_store);
printf(" auto_store: %d at %p\n", auto_store, &auto_store);
printf(" *pi: %d at %p\n", *pi, pi);
printf(" %s at %p\n", pcg, pcg);
printf(" %s at %p\n", auto_string, auto_string);
printf(" %s at %p\n", pcl, pcl);
printf(" %s at %p\n", "Quoted String", "Quoted String");
free(pi);
free(pcl);
return 0;
}
在我们的系统中，该程序的输入如下：
static_store: 30 at 00378000
auto_store: 40 at 0049FB8C
*pi: 35 at 008E9BA0
String Literal at 00375858
```

Auto char Array at 0049FB74

Dynamic String at 008E9BD0

Quoted String at 00375908

如上所示，静态数据（包括字符串字面量）占用一个区域，自动数据占用另一个区域，动态分配的数据占用第3个区域（通常被称为内存堆或自由内存）。

## 12.5 ANSI C类型限定符

我们通常用类型和存储类别来描述一个变量。C90 还新增了两个属性:恒常性（constancy）和易变性（volatility）。这两个属性可以分别用关键字const 和 volatile 来声明，以这两个关键字创建的类型是限定类型（qualified type）。C99标准新增了第3个限定符:restrict，用于提高编译器优化。C11标准新增了第4个限定符:\_Atomic。C11提供一个可选库，由stdatomic.h管理，以支持并发程序设计，而且\_Atomic是可选支持项。

C99 为类型限定符增加了一个新属性:它们现在是幂等的（idempotent）！这个属性听起来很强大，其实意思是可以在一条声明中多次使用同一个限定符，多余的限定符将被忽略:

const const const int n = 6; // 与 const int n = 6;相同

有了这个新属性，就可以编写类似下面的代码:

typedef const int zip;

const zip q = 8;

## 12.5.1 const类型限定符

第4章和第10章中介绍过const。以const关键字声明的对象，其值不能通过赋值或递增、递减来修改。在ANSI兼容的编译器中，以下代码:

const int nochange; /\* 限定nochange的值不能被修改 \*/

nochange = 12; /\* 不允许 \*/

编译器会报错。但是，可以初始化const变量。因此，下面的代码没问题:

const int nochange = 12; /\* 没问题 \*/

该声明让nochange成为只读变量。初始化后，就不能再改变它的值。

可以用const关键字创建不允许修改的数组:

$$
\text {const int days1[12]} = \{3 1, 2 8, 3 1, 3 0, 3 1, 3 0, 3 1, 3 1, 3 0, 3 1, 3 0, 3 1 \};
$$

## 1.在指针和形参声明中使用const

声明普通变量和数组时使用 const 关键字很简单。指针则复杂一些，因为要区分是限定指针本身为const还是限定指针指向的值为const。下面的声明:

const float \* pf; /\* pf 指向一个float类型的const值 \*/

创建了 pf 指向的值不能被改变，而 pt 本身的值可以改变。例如，可以设置该指针指向其他 const值。相比之下，下面的声明:

float \* const pt; /\* pt 是一个const指针 \*/

创建的指针pt本身的值不能更改。pt必须指向同一个地址，但是它所指向的值可以改变。下面的声明:

const float \* const ptr;

表明ptr既不能指向别处，它所指向的值也不能改变。

还可以把const放在第3个位置:

float const \* pfc; // 与const float \* pfc;相同

如注释所示，把const放在类型名之后、\*之前，说明该指针不能用于改变它所指向的值。简而言之， const放在\*左侧任意位置，限定了指针指向的数据不能改变；const放在\*的右侧，限定了指针本身不能改变。

const 关键字的常见用法是声明为函数形参的指针。例如，假设有一个函数要调用 display()显示一个数组的内容。要把数组名作为实际参数传递给该函数，但是数组名是一个地址。该函数可能会更改主调函数中的数据，但是下面的原型保证了数据不会被更改:

void display(const int array[], int limit);

在函数原型和函数头，形参声明const int array[]与const int \* array相同，所以该声明表明不能更改array指向的数据。

ANSI C库遵循这种做法。如果一个指针仅用于给函数访问值，应将其声明为一个指向const限定类型的指针。如果要用指针更改主调函数中的数据，就不使用const关键字。例如，ANSI C中的strcat()原型如下:

char \*strcat(char \* restrict s1, const char \* restrict s2);

回忆一下，strcat()函数在第1个字符串的末尾添加第2个字符串的副本。这更改了第1个字符串，但是未更改第1个字符串。上面的声明体现了这一点。

## 2.对全局数据使用const

前面讲过，使用全局变量是一种冒险的方法，因为这样做暴露了数据，程序的任何部分都能更改数据。如果把数据设置为 const，就可避免这样的危险，因此用 const 限定符声明全局数据很合理。可以创建const变量、const数组和const结构（结构是一种复合数据类型，将在下一章介绍）。

然而，在文件间共享const数据要小心。可以采用两个策略。第一，遵循外部变量的常用规则，即在一个文件中使用定义式声明，在其他文件中使用引用式声明（用extern关键字）:

/\* file1.c -- 定义了一些外部const变量 \*/

const double PI = 3.14159;

const char \* MONTHS[12] = { "January", "February", "March", "April", "May",

"June", "July","August", "September", "October",

"November", "December" };

/\* file2.c -- 使用定义在别处的外部const变量 \*/

extern const double PI;

extern const \* MONTHS [];

另一种方案是，把const变量放在一个头文件中，然后在其他文件中包含该头文件:

/\* constant.h --定义了一些外部const变量\*/

static const double PI = 3.14159;

static const char \* MONTHS[12] ={"January", "February", "March", "April", "May",

"June", "July","August", "September", "October",

"November", "December"};

/\* file1.c --使用定义在别处的外部const变量\*/

#include "constant.h"

/\* file2.c --使用定义在别处的外部const变量\*/

#include "constant.h"

这种方案必须在头文件中用关键字static声明全局const变量。如果去掉static，那么在file1.c和file2.c中包含constant.h将导致每个文件中都有一个相同标识符的定义式声明，C标准不允许这样做（然而，有些编译器允许）。实际上，这种方案相当于给每个文件提供了一个单独的数据副本[1]。由于每个副本只对该文件可见，所以无法用这些数据和其他文件通信。不过没关系，它们都是完全相同（每个文件都包含相同的头文件）的const数据（声明时使用了const关键字），这不是问题。

头文件方案的好处是，方便你偷懒，不用惦记着在一个文件中使用定义式声明，在其他文件中使用引用式声明。所有的文件都只需包含同一个头文件即可。但它的缺点是，数据是重复的。对于前面的例子而言，这不算什么问题，但是如果const数据包含庞大的数组，就不能视而不见了。

## 12.5.2 volatile类型限定符

volatile 限定符告知计算机，代理（而不是变量所在的程序）可以改变该变量的值。通常，它被用于硬件地址以及在其他程序或同时运行的线程中共享数据。例如，一个地址上可能储存着当前的时钟时间，无论程序做什么，地址上的值都随时间的变化而改变。或者一个地址用于接受另一台计算机传入的信息。

volatile的语法和const一样:

olatile int loc1;/\* loc1 是一个易变的位置 \*/

volatile int \* ploc; /\* ploc 是一个指向易变的位置的指针 \*/

以上代码把loc1声明为volatile变量，把ploc声明为指向volatile变量的指针。

读者可能认为volatile是个可有可无的概念，为何ANSI委员把volatile关键字放入标准？原因是它涉及编译器的优化。例如，假设有下面的代码:

$$
\text {vall} = \mathrm{x};
$$

/\* 一些不使用 x 的代码\*/

$$
\mathrm{val2} = \mathrm{x}
$$