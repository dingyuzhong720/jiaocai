## B.3 参考资料III:基本类型和存储类别

## B.3.1 总结:基本数据类型

C语言的基本数据类型分为两大类:整数类型和浮点数类型。不同的种类提供了不同的范围和精度。

## 1.关键字

创建基本数据类型要用到8个关键字:int、long、short、unsigned、char、float、double、signed（ANSI C）。

## 2.有符号整数

有符号整数可以具有正值或负值。

int是所有系统中基本整数类型。

long或long int可储存的整数应大于或等于int可储存的最大数；long至少是32位。

short或short int整数应小于或等于int可储存的最大数；short至少是16位。通常，long比short大。例如，在PC中的C DOS编译器提供16位的short和int、32位的long。这完全取决于系统。

C99标准提供了long long类型，至少和long一样大，至少是64位。

## 3.无符号整数

无符号整数只有 0 和正值，这使得该类型能表示的正数范围更大。在所需的类型前面加上关键字unsigned:unsigned int、unsigned long、unsigned short、unsigned long long。单独的unsigned相当于unsigned int。

## 4.字符

字符是如A、&、+这样的印刷符号。根据定义，char类型的变量占用1字节的内存。过去，char类型的大小通常是8位。然而，C在处理更大的字符集时，char类型可以是16位，或者甚至是32位。

这种类型的关键字是char。一些实现使用有符号的char，但是其他实现使用无符号的char。ANSI C允许使用关键字signed 和 unsigned指定所需类型。从技术层面上看，char、unsigned char和signed char是3种不同的类型，但是char类型与其他两种类型的表示方法相同。

## 5.布尔类型（C99）

Bool是C99新增的布尔类型。它一个无符号整数类型，只能储存0（表示假）或1（表示真）。包含stdbool.c头文件后，可以用bool表示\_Bool、ture表示1、false表示0，让代码与C++兼容。

## 6.实浮点数和复浮点数类型

C99识别两种浮点数类型:实浮点数和复浮点数。浮点类型由这两种类型构成。

实浮点数可以是正值或负值。C识别3种实浮点类型。

float是系统中的基本浮点类型。它至少可以精确表示6位有效数字，通常float为32位。

double（可能）表示更大的浮点数。它能表示比 float更多的有效数字和更大的指数。它至少能精确表示10位有效数字。通常，double为64位。

long double（可能）表示更大的浮点数。它能表示比double更多的有效数字和更大的指数。

复数由两部分组成:实部和虚部。C99 规定一个复数在内部用一个有两个元素的数组表示，第 1 个元素表示实部，第2个元素表示虚部。有3种复浮点数类型。

float \_Complex表示实部和虚部都是float类型的值。

double \_Complex表示实部虚部都是double类型的值。

long double \_Complex表示实部和虚部都是long double类型的值。

每种情况，前缀部分的类型都称为相应的实数类型（corresponding real type）。例如，double是double\_Complex相应的实数类型。

C99中，复数类型在独立环境中是可选的，这样的环境中不需要操作系统也可运行C程序。在C11中，复数类型在独立环境和主机环境都是可选的。

有 3 种虚数类型。它们在独立环境中和主机环境中（C 程序在一种操作系统下运行的环境）都是可选的。虚数只有虚部。这3种类型如下。

float \_Imaginary表示虚部是float类型的值。

double \_Imaginary表示虚部是double类型的值。

long double \_Imaginary表示虚部是long double类型的值。

可以用实数和I值来初始化复数。I定义在complex.h头文件中，表示i（即-1的平方根）。

#include &lt;complex.h&gt; // I定义在该头文件中

double \_Complex z = 3.0;

double \_Complex w = 4.0 \* I; // 实部 = 0.0，虚部 = 4.0

double Complex u = 6.0 – 8.0 \* I; //实部= 6.0，虚部 = -8.0

前面章节讨论过，complex.h库包含一些返回复数实部和虚部的函数。

**B.3.2** 总结:如何声明一个简单变量

1.选择所需的类型。
2.选择一个合适的变量名。
3.使用这种声明格式:type-specifiervariable-name;
type-specifier由一个或多个类型关键字组成，下面是一些例子:

int erest;

unsigned short cash;

4.声明多个同类型变量时，使用逗号分隔符隔开各变量名:

char ch, init, ans;

5.可以在声明的同时初始化变量:

float mass = 6.0E24;

总结:存储类别

关键字:auto、extern、static、register、\_Thread\_local（C11）

一般注解:

变量的存储类别取决于它的作用域、链接和存储期。存储类别由声明变量的位置和与之关联的关键字决定。定义在所有函数外部的变量具有文件作用域、外部链接、静态存储期。声明在函数中的变量是自动变量，除非该变量前面使用了其他关键字。它们具有块作用域、无链接、自动存储期。以static关键字声明在函数中的变量具有块作用域、无链接、静态存储期。以static关键字声明在函数外部的变量具有文件作用域、内部链接、静态存储期。

C11 新增了一个存储类别说明符:\_Thread\_local。以该关键字声明的对象具有线程存储期，意思是在线程中声明的对象在该线程运行期间一直存

在，且在线程开始时被初始化。因此，这种对象属于线程私有。

属性:

下面总结了这些存储类别的属性:

| 存储类别 | 存储期 | 作用域 | 链接 | 如何声明 |
| --- | --- | --- | --- | --- |
| 自动 | 自动 | 块 | 无 | 在块中 |
| 寄存器 | 自动 | 块 | 无 | 在块中,使用关键字register |

续表

| 存储类别 | 存储期 | 作用域 | 链接 | 如何声明 |
| --- | --- | --- | --- | --- |
| 静态、外部链接 | 静态 | 文件 | 外部 | 在所有函数外部 |
| 静态、内部链接 | 静态 | 文件 | 内部 | 在所有函数外部,使用关键字static |
| 静态、无链接 | 静态 | 块 | 无 | 在块中,使用关键字static |
| 线程、外部链接 | 线程 | 文件 | 外部 | 在所有块的外部,使用关键字_Thread_local |
| 线程、内部链接 | 线程 | 文件 | 内部 | 在所有块的外部,使用关键字static和_Thread_local |
| 线程、无链接 | 线程 | 块 | 无 | 在块中,使用关键字static和_Thread_local |

注意，关键字extern只能用来再次声明在别处已定义过的变量。在函数外部定义变量，该变量具有外部链接属性。

除了以上介绍的存储类别，C 还提供了动态分配内存。这种内存通过调用 malloc()函数系列中的一个函数来分配。这种函数返回一个可用于访问内存的指针。调用 free()函数或结束程序可以释放动态分配的内存。任何可以访问指向该内存指针的函数均可访问这块内存。例如，一个函数可以把这个指针的值返回给另一个函数，那么另一个函数也可以访问该指针所指向的内存。

## B.3.3 总结:限定符

关键字

使用下面关键字限定变量:

const、volatile、restrict

## 一般注释

限定符用于限制变量的使用方式。不能改变初始化以后的 const 变量。编译器不会假设 volatile变量不被某些外部代理（如，一个硬件更新）改变。restrict 限定的指针是访问它所指向内存的唯一方式（在特定作用域中）。

属性

const int joy = 101;声明创建了变量joy，它的值被初始化为101。

volatile unsigned int incoming;声明创建了变量incoming，该变量在程序中两次出现之间，其值可能会发生改变。

const int \* ptr = &joy;声明创建了指针ptr，该指针不能用来改变变量joy的值，但是它可以指向其他位置。

int \* const ptr = &joy;声明创建了指针ptr，不能改变该指针的值，即ptr只能指向joy，但是可以用它来改变joy的值。

void simple (const char \* s);声明表明形式参数s被传递给simple()的值初始化后，simple()不能改变s指向的值。

void supple(int \* const pi);与void supple(int pi[const]);等价。这两个声明都表明supple()函数不会改变形参pi。

void interleave(int \* restrict p1, int \* restrict p2, int n);声明表明p1和p2是访问它们所指向内存的唯一方法，这意味着这两个块不能重叠。

## B.4 参考资料IV:表达式、语句和程序流

## B.4.1 总结:表达式和语句

在C语言中，对表达式可以求值，通过语句可以执行某些行为。

表达式

表达式由运算符和运算对象组成。最简单的表达式是一个常量或一个不带运算符的变量，如 22 或beebop。稍复杂些的例子是55 + 22和vap = 2 \* $( \mathrm{vip} + ( \mathrm{vup} = 4 ) )$ 。

语句

大部分语句都以分号结尾。以分号结尾的表达式都是语句，但这样的语句不一定有意义。语句分为简单语句和复合语句。简单语句以分号结尾，如下所示:

```txt
toes = 12; // 赋值表达式语句
```

printf("%d\n", toes); // 函数调用表达式语句

//空语句，什么也不做

（注意，在C语言中，声明不是语句。）

用花括号括起来的一条或多条语句是复合语句或块。如下面的while语句所示:

```c
while (years < 100)

{
wisdom = wisdom + 1;

printf("%d %d\n", years, wisdom);
```

```txt
years = years + 1;
}
```

## B.4.2 总结:while语句

关键字

while语句的关键字是while。

一般注释

while语句创建了一个循环，在expression为假之前重复执行。while语句是一个入口条件循环，在下一轮迭代之前先确定是否要再次循环。因此可能一次循环也不执行。statement可以是一个简单语句或复合语句。

形式

while ( expression )

statement

当expression为假（或0）之前，重复执行statement部分。

示例

while (n++ < 100)

printf(" %d %d\n",n, 2\*n+1);

while (fargo < 1000)

{

fargo = fargo + step;

step = 2 \* step;

}

## B.4.3 总结:for语句

关键字

for语句的关键字是for。

一般注释

for语句使用3个控制表达式控制循环过程，分别用分号隔开。initialize表达式在执行for语句之前只执行一次；然后对test表达式求值，如果表达式为真（或非零），执行循环一次；接着对update表达式求值，并再次检查test表达式。for语句是一种入口条件循环，即在执行循环之前就决定了是否执行循环。因此，for循环可能一次都不执行。statement部分可以是一条简单语句或复合语句。

形式:

for ( initialize; test; update )

statement

在test为假或0之前，重复执行statement部分。

C99允许在for循环头中包含声明。变量的作用域和生命期被限制在for循环中。

示例:

for (n = 0; n < 10 ; n++)

printf(" %d %d\n", n, 2 \* n + 1);

for (int k = 0; k < 10 ; ++k) // C99

printf("%d %d\n", k, 2 \* k+1);

## B.4.4 总结:do while语句

关键字

do while语句的关键字是do和while。

一般注解:

do while语句创建一个循环，在expression为假或0之前重复执行循环体中的内容。do while语句是一种出口条件循环，即在执行完循环体后才根据测试条件决定是否再次执行循环。因此，该循环至少必须执行一次。

statement部分可是一条简单语句或复合语句。

形式:

do

statement

while ( expression );

在test为假或0之前，重复执行statement部分。

示例:

do

scanf("%d", &number);

while (number != 20);

## B.4.5 总结:if语句

小结:用**if**语句进行选择

关键字:**if**、**else**

一般注解:

下面各形式中，statement可以是一条简单语句或复合语句。表达式为真说明其值是非零值。

形式1:

if (expression)

statement

如果expression为真，则执行statement部分。

形式2:

if (expression)

statement1

else

statement2

如果expression为真，执行statement1部分；否则，执行statement2部分。

形式3:

if (expression1)

statement1

else if (expression2)

statement2

else

statement3

如果expression1为真，执行statement1部分；如果expression2为真，执行statement2部分；否则，执行statement3部分。

示例:

```lisp
if (legs == 4)

printf("It might be a horse.\n");

else if (legs > 4)

printf("It is not a horse.\n");

else      /* 如果legs < 4 */

{

legs++;

printf("Now it has one more leg.\n");

}
```

## B.4.6 带多重选择的switch语句

关键字:**switch**

一般注解:

程序控制根据expression的值跳转至相应的case标签处。然后，程序流执行剩下的所有语句，除非执行到break语句进行重定向。expression和case标签都必须是整数值（包括char类型），标签必须是常量或完全由常量组成的表达式。如果没有case标签与expression的值匹配，控制则转至标有default的语句（如果有的话）；否则，控制将转至紧跟在switch语句后面的语句。控制转至特定标签后，将执行switch语句中其后的所有语句，除非到达switch末尾，或执行到break语句。

形式:

```txt
switch ( expression )
{
case label1 : statement1//使用break跳出switch
case label2 : statement2
default     : statement3
}
```

可以有多个标签语句，default语句可选。

示例:

```txt
switch (value)
{
case 1 : find_sum(ar, n);
break;
case 2 : show_array(ar, n);
break;
case 3 : puts("Goodbye!");
```

```lisp
break;

default : puts("Invalid choice, try again.");
break;

}

switch (letter)

{

case 'a' :

case 'e' : printf("%d is a vowel\n", letter);

case 'c' :

case 'n' : printf("%d is in \"cane\"\n", letter);

default : printf("Have a nice day.\n");
}
```

如果letter的值是'a'或'e'，就打印这3条消息；如果letter的值是'c'或'n'，则只打印后两条消息；letter是其他值时，值打印最后一条消息。

## B.4.7 总结:程序跳转

关键字:**break**、**continue**、**goto**

一般注解:

这3种语句都能使程序流从程序的一处跳转至另一处。

break语句:

所有的循环和switch语句都可以使用break语句。它使程序控制跳出当前循环或switch语句的剩余部分，并继续执行跟在循环或switch后面的语句。

示例:

```txt
while ((ch = getchar()) != EOF)
{
putchar(ch);
if (ch == ' ')
break;          // 结束循环
chcount++;
}
continue语句:
```

所有的循环都可以使用continue语句，但是switch语句不行。continue语句使程序控制跳出循环的剩余部分。对于while或for循环，程序执行到continue语句后会开始进入下一轮迭代。对于do while循环，对出口条件求值后，如有必要会进入下一轮迭代。

示例:

```txt
while ((ch = getchar()) != EOF)
{
if (ch == ' ')
continue; // 跳转至测试条件
```

```txt
putchar(ch);

chcount++;

}
```

以上程序段打印用户输入的内容并统计非空格字符

goto语句:

goto语句使程序控制跳转至相应标签语句。冒号用于分隔标签和标签语句。标签名遵循变量命名规则。标签语句可以出现在goto的前面或后面。

形式:

goto label ;

label : statement

示例:

```javascript
top : ch = getchar();
if (ch != 'y')
goto top;
```

## B.5 参考资料V:新增C99和C11的ANSI C库

ANSI C库把函数分成不同的组，每个组都有相关联的头文件。本节将概括地介绍库函数，列出头文件并简要描述相关的函数。文中会较详细地介绍某些函数（例如，一些I/O函数）。欲了解完整的函数说明，请参考具体实现的文档或参考手册，或者试试这个在线参考:

http://www.acm.uiuc.edu/webmonkeys/book/c\_guide/。

## B.5.1 断言:assert.h

assert.h 头文件中把 assert()定义为一个宏。在包含 assert.h 头文件之前定义宏标识符NDEBUG，可以禁用assert()宏。通常用一个关系表达式或逻辑表达式作为assert()的参数，如果运行正常，那么程序在执行到该点时，作为参数的表达式应该为真。表B.5.1描述了assert()宏。

表B.5.1 断言宏

| 原型 | 描述 |
| --- | --- |
| void assert(int exprs); | 如果 exprs 为 0(或真),宏什么也不做。如果 exprs 为 0(或假),assert() 就显示该表达式和其所在的行号和文件名。然后,assert() 调用 abort() |

C11新增了static\_assert宏，展开为\_Static\_assert。\_Static\_assert是一个关键字，被认为是一种声明形式。它以这种方式提供一个编译时检查:

\_Static\_assert( 常量表达式,字符串字面量);

如果对常量表达式求值为0，编译器会给出一条包含字符串字面量的错误消息；否则，没有任何效果。

## B.5.2 复数:complex.h（C99）

C99 标准支持复数计算，C11 进一步支持了这个功能。实现除提供\_Complex 类型外还可以选择是否提供\_Imaginary类型。在C11中，可以选择是否提供这两种类型。C99规定，实现必须提供\_Complex类型，但是\_Imaginary类型为可选，可以提供或不提供。附录B的参考资料VIII中进一步讨论了C如何支持复数。complex.h头文件中定义了表B.5.2所列的宏。

表B.5.2 complex.h宏

| 宏 | 描述 |
| --- | --- |
| complex | 展开为类型关键字_Complex |
| _Complex_I | 展开为 const float _Complex 类型的表达式,其值的平方是-1 |
| imaginary | 如果支持虚数类型,展开为类型关键字_Imaginary |
| _Imaginary_I | 如果支持虚数类型,展开为 const float _Imaginary 类型的表达式,其值的平方是-1 |
| I | 展开为_Complex_I 或_Imaginary_I |

对于实现复数方面，C和C++不同。C通过complex.h头文件支持，而C++通过complex头文件支持。而且，C++使用类来定义复数类型。

可以使用STDC CX\_LIMITED\_RANGE编译指令来表明是使用普通的数学公式（设置为on时），还是要特别注意极值（设置为off时）:

```c
#include <complex.h>
```

#pragma STDC CX\_LIMITED\_RANGE on

库函数分为3种:double、float、long double。表B.5.3列出了double版本的函数。float和long double版本只需要在函数名后面分别加上f和l。即csinf()就是csin()的float版本，而csinl()是csin()的long double版本。另外要注意，角度的单位是弧度。

表B.5.3 复数函数

| 原型 | 描述 |
| --- | --- |
| double complex cacos(double complex z); | 返回z的复数反余弦 |
| double complex casin(double complex z); | 返回z的复数反正弦 |
| double complex catan(double complex z); | 返回z的复数反正切 |
| double complex ccos(double complex z); | 返回z的复数余弦 |
| double complex csin(double complex z); | 返回z的复数正弦 |
| double complex ctan(double complex z); | 返回z的复数正切 |
| double complex cacosh(double complex z); | 返回z的复数反双曲余弦 |
| double complex casinh(double complex z); | 返回z的复数反双曲正弦 |
| double complex catanh(double complex z); | 返回z的复数反双曲正切 |
| double complex ccosh(double complex z); | 返回z的复数双曲余弦 |
| double complex csinh(double complex z); | 返回z的复数双曲正弦 |
| double complex ctanh(double complex z); | 返回z的复数双曲正切 |
| double complex cexp(double complex z); | 返回e的z次幂复数值 |
| double complex clog(double complex z); | 返回z的自然对数(以e为底)的复数值 |
| double cabs(double complex z); | 返回z的绝对值(或大小) |
| double complex cpows(double complex z, double complex y); | 返回z的y次幂 |
| double complex csqrt(double complex z); | 返回z的复数平方根 |

续表

| 原型 | 描述 |
| --- | --- |
| double carg(double complex z); | 以弧度为单位返回z的相位角(或幅角) |
| double cimag(double complex z); | 以实数形式返回z的虚部 |
| double complex conj(double complex z); | 返回z的共轭复数 |
| double complex cproj(double complex z); | 返回z在黎曼球面上的投影 |
| double complex CMPLX(double x,double y); | 返回实部为x、虚部为y的复数(C11) |
| double creal(double complex z); | 以实数形式返回z的实部 |

## B.5.3 字符处理:ctype.h

这些函数都接受int类型的参数，这些参数可以表示为unsigned char类型的值或EOF。使用其他值的效果是未定义的。在表B.5.4中，“真”表示“非0值”。对一些定义的解释取决于当前的本地设置，这些由locale.h中的函数来控制。该表显示了在解释本地化的“C”时要用到的一些函数。

表B.5.4 字符处理函数

| 原型 | 描述 |
| --- | --- |
| int isalnum(int c); | 如果c是字母或数字,则返回真 |
| int isalpha(int c); | 如果c是字母,则返回真 |
| int isblank(int c); | 如果c是空格或水平制表符,则返回真(C99) |
| int iscntrl(int c); | 如果c是控制字符(如Ctrl+B),则返回真 |
| int isdigit(int c); | 如果c是数字,则返回真 |
| int isgraph(int c); | 如果c是非空格打印字符,则返回真 |
| int islower(int c); | 如果c是小写字符,则返回真 |
| int isprint(int c); | 如果c是打印字符,则返回真 |
| int ispunct(int c); | 如果c是标点字符(除了空格、字母、数字以外的字符),则返回真 |
| int isspace(int c); | 如果c是空白字符(空格、换行符、换页符、回车符、垂直或水平制表符,或者其他实现定义的字符),则返回真 |
| int isupper(int c); | 如果c是大写字符,则返回真 |
| int isxdigit(int c); | 如果c是十六进制数字字符,则返回真 |
| int tolower(int c); | 如果c是大写字符,则返回其小写字符;否则返回c |
| int toupper(int c); | 如果c是小写字符,则返回其大写字符;否则返回c |

## B.5.4 错误报告:errno.h

errno.h头文件支持较老式的错误报告机制。该机制提供一个标识符（或有时称为宏）ERRNO可访问的外部静态内存位置。一些库函数把一个值放进这个位置用于报告错误，然后包含该头文件的程序就可以通过查看ERRNO的值检查是否报告了一个特定的错误。ERRNO机制被认为不够艺术，而且设置ERRNO值也不需要数学函数了。标准提供了3个宏值表示特殊的错误，但是有些实现会提供更多。表B.5.5列出了这些标准宏。

表B.5.5 errno.h宏

| 宏 | 含义 |
| --- | --- |
| EDOM | 函数调用中的域错误(参数越界) |
| ERANGE | 函数返回值的范围错误(返回值越界) |
| EILSEQ | 宽字符转换错误 |

## B.5.5 浮点环境:fenv.h（C99）

C99标准通过fenv.h头文件提供访问和控制浮点环境。

浮点环境（floating-point environment）由一组状态标志（status flag）和控制模式（control mode）组成。在浮点计算中发生异常情况时（如，被零除），可以“抛出一个异常”。这意味着该异常情况设置了一个浮点环境标志。控制模式值可以进行一些控制，例如控制舍入的方向。fenv.h头文件定义了一组宏表示多种异常情况和控制模式，并提供了与环境交互的函数原型。头文件还提供了一个编译指令来启用或禁用访问浮点环境的功能。

下面的指令开启访问浮点环境:

```c
#pragma STDC FENV_ACCESS on
```

下面的指令关闭访问浮点环境:

```c
#pragma STDC FENV_ACCESS off
```

应该把该编译指示放在所有外部声明之前或者复合块的开始处。在遇到下一个编译指示之前、或到达文件末尾（外部指令）、或到达复合语句的末尾（块指令），当前编译指示一直有效。

头文件定义了两种类型，如表B.5.6所示。

表B.5.6 fenv.h类型

| 类型 | 表示 |
| --- | --- |
| fenv_t | 整个浮点环境 |
| fexcept_t | 浮点状态标志集合 |

头文件定义了一些宏，表示一些可能发生的浮点异常情况控制状态。其他实现可能定义更多的宏，但是必须以FE\_开头，后面跟大写字母。表B.5.7列出了一些标准异常宏。

表B.5.7 fenv.h中的标准异常宏

| 宏 | 含义 |
| --- | --- |
| FE_DIVBYZERO | 抛出被零除异常 |
| FE_INEXACT | 抛出不精确值异常 |
| FE_INVALID | 抛出无效值异常 |
| FE_OVERFLOW | 抛出上溢异常 |
| FE_UNDERFLOW | 抛出下溢异常 |
| FE_ALL_EXCEPT | 实现支持的所有浮点异常的按位或 |
| FE_DOWNWARD | 向下舍入 |
| FE_TONEAREST | 向最近的舍入 |
| FE_TOWARDZERO | 趋0舍入 |
| FE_UPWARD | 向上舍入 |
| FE_DFL_ENV | 表示默认环境,类型是const fenv_t * |

表B.5.8中列出了fenv.h头文件中的标准函数原型。注意，常用的参数值和返回值与表B.5.7中的宏相对应。例如，FE\_UPWARD是fesetround()的一个合适参数。

表B.5.8 fenv.h中的标准函数原型

| 原型 | 描述 |
| --- | --- |
| void feclearexcept(int excepts); | 清理excepts表示的异常 |
| void fegetexceptflag(fexcept_t *flagp, int excepts); | 把excepts指明的浮点状态标志储存在flagp指向的对象中 |
| void feraiseexcept(int excepts); | 抛出excepts指定的异常 |
| void fesetexceptflag(const fexcept_t *flagp, intexcepts); | 把excepts指明的浮点状态标志设置为flagp的值;在此之前,fegetexceptflag()调用应该设置flagp的值 |
| int fetestexcept(int excepts); | 测试excepts指定的状态标志;该函数返回指定状态标志的按位或 |
| int fegetround(void); | 返回当前的舍入方向 |
| int fesetround(int round); | 把舍入方向设置为round的值;当且仅当设置成功时,函数返回0 |
| void fegetenv(fenv_t *envp); | 把当前环境储存至envp指向的位置中 |
| int feholdexcept(fenv_t *envp); | 把当前浮点环境储存至envp指向的位置中,清除浮点状态标志,然后如果可能的话就设置非停模式(nonstop mode),在这种模式中即使发生异常也继续执行。当且仅当执行成功时,函数返回0 |
| void fesetenv(const fenv_t *envp); | 建立envp表示的浮点环境;envp应指向一个之前通过调用fegetenv()、feholdexcept()或浮点环境宏设置的数据对象 |
| void feupdateenv(const fenv_t *envp); | 函数在自动存储区中储存当前抛出的异常,建立envp指向的对象表示的浮点环境,然后抛出已储存的浮点异常;envp应指向一个之前通过调用fegetenv()、feholdexcept()或浮点环境宏设置的数据对象 |

## B.5.6 浮点特性:float.h

float.h头文件中定义了一些表示各种限制和形参的宏。表B.5.9列出了这些宏，C11新增的宏以斜体并缩进标出。许多宏都涉及下面的浮点表示模型:

$$
x = s b ^ {e} \sum_ {k = 1} ^ {p} f _ {k} ^ {b ^ {- k}}
$$

如果第1个数 $\mathbf { f } _ { 1 } ^ { \mathrm { ~ . ~ } }$ 是非0（且x是非0），该数字被称为标准化浮点数。附录B的参考资料VIII中将更详细地解释一些宏。

表B.5.9 float.h宏

| 宏 | 含义 |
| --- | --- |
| FLT_ROUNDS | 默认舍入方案 |
| FLT_EVAL_METHOD | 浮点表达式求值的默认方案 |
| FLT_HAS_SUBNORM | 存在或缺少 float 类型的反常值 |
| DBL_HAS_SUBNORM | 存在或缺少 double 类型的反常值 |
| LDBL_HAS_SUBNORM | 存在或缺少 long double 类型的反常值 |
| FLT_RADIX1 | 指数表示法中使用的进制数 (b),最小值为 2 |

1 FLT\_RADIX用于表示3种浮点数类型的基数。——译者注

续表

| 宏 | 含义 |
| --- | --- |
| FLT_MANT_DIG | 以FLT_RADIX进制表示的float类型数的位数(模型中的p) |
| DBL_MANT_DIG | 以FLT_RADIX进制表示的double类型数的位数(模型中的p) |
| LDBL_MANT_DIG | 以FLT_RADIX进制表示的long double类型数的位数(模型中的p) |
| FLT_DECIMAL_DIG | 在b进制和十进制相互转换不损失精度的前提下,float类型的十进制数的位数(最小值是6) |
| DBL_DECIMAL_DIG | 在b进制和十进制相互转换不损失精度的前提下,double类型的十进制数的位数(最小值是10) |
| LDBL_DECIMAL_DIG | 在b进制和十进制相互转换不损失精度的前提下,long double类型的十进制数的位数(最小值是10) |
| DECIMAL_DIG | 在b进制与十进制相互转换不损失精度的前提下,浮点类型十进制数的最大个数(最小值为10) |
| FLT_DIG | 在不损失精度的前提下,float类型可表示的十进制数位数(最小值为6) |
| DBL_DIG | 在不损失精度的前提下,double类型可表示的十进制数位数(最小值为10) |
| LDBL_DIG | 在不损失精度的前提下,long double类型可表示的十进制数位数(最小值为10) |
| FLT_MIN_EXP | float类型e表示法,指数的最小负正整数值 |
| DBL_MIN_EXP | double类型e表示法,指数的最小负正整数值 |
| LDBL_MIN_EXP | long double类型e表示法,指数的最小负正整数值 |
| FLT_MIN_10_EXP | 用10的x次幂表示规范化float类型数时,x的最小负整数值(不超过-37) |
| DBL_MIN_10_EXP | 用10的x次幂表示规范化double类型数时,x的最小负整数值(不超过-37) |
| LDBL_MIN_10_EXP | 用10的x次幂表示规范化long double类型数时,x的最小负整数值(不超过-37) |
| FLT_MAX_EXP | float类型e表示法,指数的最大正整数值 |
| DBL_MAX_EXP | double类型e表示法,指数的最大正整数值 |
| LDBL_MAX_EXP | long double类型e表示法,指数的最大正整数值 |
| FLT_MAX_10_EXP | 用10的x次幂表示规范化float类型数时,x的最大正整数值(至少+37) |
| DBL_MAX_10_EXP | 用10的x次幂表示规范化double类型数时,x的最大正整数值(至少+37) |
| LDBL_MAX_10_EXP | 用10的x次幂表示规范化long double类型数时,x的最大正整数值(至少+37) |
| FLT_MAX | float类型的最大有限值(至少1E+37) |
| DBL_MAX | doble类型的最大有限值(至少1E+37) |
| LDBL_MAX | long double类型的最大有限值(至少1E+37) |
| FLT_EPSILON | float类型比1大的最小值与1的差值(不超过1E-9) |
| DBL_EPSILON | double类型比1大的最小值与1的差值(不超过1E-9) |
| LDBL_EPSILON | long double类型比1大的最小值与1的差值(不超过1E-9) |
| FLT_MIN | 标准化float类型的最小正值(不超过1E-37) |
| DBL_MIN | 标准化double类型的最小正值(不超过1E-37) |
| LDBL_MIN | 标准化long double类型的最小正值(不超过1E-37) |
| FLT_TRUE_MIN | float类型的最小正值(不超过1E-37) |
| DBL_TRUE_MIN | double类型的最小正值(不超过1E-37) |
| LDBL_TRUE_MIN | long double类型的最小正值(不超过1E-37) |

## B.5.7 整数类型的格式转换:inttypes.h

该头文件定义了一些宏可用作转换说明来扩展整数类型。参考资料VI“扩展的整数类型”将进一步讨论。该头文件还声明了这个类型:imaxdiv\_t。这是一个结构类型，表示idivmax()函数的返回值。

该头文件中还包含 stdint.h，并声明了一些使用最大长度整数类型的函数，这种整数类型在stdint.h中声明为intmax。表B.5.10列出了这些函数。

表B.5.10 使用最大长度整数的函数

| 原型 | 描述 |
| --- | --- |
| intmax_t imaxabs(intmax_t j); | 返回j的绝对值 |
| imaxdiv_t imaxdiv(intmax_t numer, intmax_t denom); | 单独计算numer/denom的商和余数,并把两个计算结果储存在返回的结构中 |
| intmax_t strtoimax(const char * restrict nptr, char ** restrict endptr, int base); | 相当于strtol()函数,但是该函数把字符串转换成intmax_t类型并返回该值 |
| uintmax_t strtoumax(const char * restrict nptr, char ** restrict endptr, int base); | 相当于strtoul()函数,但是该函数但是该函数把字符串转换成intmax_t类型并返回该值 |
| intmax_t wcstoimax(const wchar_t * restrict nptr, wchar_t ** restrict endptr, int base); | strtoimax()函数的wchar_t类型的版本 |
| uintmax_t wcstoumax(const wchar_t * restrict nptr, wchar_t ** restrict endptr, int base); | strtoumax()函数的wchar_t类型的版本 |

## B.5.8 可选拼写:iso646.h

该头文件提供了11个宏，扩展了指定的运算符，如表B.5.11所列。

表B.5.11 可选拼写

| 宏 | 运算符 | 宏 | 运算符 | 宏 | 运算符 |
| --- | --- | --- | --- | --- | --- |
| and | &amp;&amp; | and_eq | &amp;= | bitand | &amp; |
| bitor | \| | compl | ~ | not | ! |
| not | != | or | \|\| | or_eq | \|= |
| xor | ^ | xor_eq | ^= |  |  |

## B.5.9 本地化:locale.h

本地化是一组设置，用于控制一些特定的设置项，如表示小数点的符号。本地值储存在struct lconv类型的结构中，定义在 locale.h 头文件中。可以用一个字符串来指定本地化，该字符串指定了一组结构成员的特殊值。默认的本地化由字符串 $\mathbf { C }$ 指定。表 B.5.12 列出了本地化函数，后面做了简要说明。

表B.5.12 本地化函数

| 原型 | 描述 |
| --- | --- |
| char * setlocale(int category,const char * locale); | 该函数把某些值设置为本地和 locale 指定的值。category 的值决定要设置哪些本地值(参见 B.5.13)。如果成功设置本地化,该函数将返回一个在新本地化中与指定类别相关联的指针;如果不能完成本地化请求,则返回空指针 |
| struct lconv*localeconv(void); | 返回一个指向 struct lconv 类型结构的指针,该结构中储存着当前的本地值 |

setlocale()函数的locale形参所需的值可能是默认值 $\mathbf { C }$ ，也可能是""，表示实现定义的本地环境。实现可以定义更多的本地化设置。category形参的值可能由表B.5.13中所列的宏表示。

表B.5.13 category宏

| 原型 | 描述 |
| --- | --- |
| NULL | 本地化设置不变,返回指向当前本地化的指针 |
| LC_ALL | 改变所有的本地值 |
| LC_COLLATE | 改变 strcoll()和 strxfrm()所用的排列顺序的本地值 |
| LC_CTYPE | 改变字符处理函数和多字节函数的本地值 |
| LC_MONETARY | 改变货币格式信息的本地值 |
| LC_NUMERIC | 改变十进制小数点符号和格式化 I/O 使用的非货币格式本地值 |
| LC_TIME | 改变 strftime()所用的时间格式本地值 |

表B.5.14列出了struct lconv结构所需的成员。

表B.5.14 struct lcconv所需的成员

| 成员变量 | 描述 |
| --- | --- |
| char *decimal_point | 非货币值的小数点字符 |
| char *thousands_sep | 非货币值中小数点前面的千位分隔符 |
| char *grouping | 一个字符串,表示非货币量中每组数字的大小 |
| char *int_curr_symbol | 国际货币符号 |
| char *currency_symbol | 本地货币符号 |
| char *mon_decimal_point | 货币值的小数点符号 |
| char *mon_thousands_sep | 货币值的千位分隔符 |
| char *mon_grouping | 一个字符串,表示货币量中每组数字的大小 |
| char *positive_sign | 指明非负格式化货币值的字符串 |
| char *negative_sign | 指明负格式化货币值的字符串 |
| char int_frac_digits | 国际格式化货币值中,小数点后面的数字个数 |
| char frac_digits | 本地格式化货币值中,小数点后面的数字个数 |
| char p_cs_precedes | 如果该值为1,则 currency_symbol 在非负格式化货币值的前面;如果该值为0,则 currency_symbol 在非负格式化货币值的后面 |

续表

| 成员变量 | 描述 |
| --- | --- |
| char p_sep_by_space | 如果该值为1,则用空格把currency_symbol和非负格式化货币值隔开;如果该值为0,则不用空格分隔currency_symbol和非负格式化货币值 |
| char n_cs_precedes | 如果该值为1,则currency_symbol在负格式化货币值的前面;如果该值为0,则currency_symbol在负格式化货币值的后面 |
| char n_sep_by_space | 如果该值为1,则用空格把currency_symbol和负格式化货币值隔开;如果该值为0,则不用空格分隔currency_symbol和负格式化货币值 |
| char p_sign_posn | 其值表示positive_sign字符串的位置:0表示用圆括号把数值和货币符号括起来1表示字符串在数值和货币符号前面2表示字符串在数值和货币符号后面3表示直接把字符串放在货币前面4表示字符串紧跟在货币符号后面 |
| char n_sign_posn | 其值表示negative_sign字符串的位置,含义与p_sign_posn相同 |
| char int_p_cs_precedes | 如果该值为1,则int_currency_symbol在非负格式化货币值的前面;如果该值为0,则int_currency_symbol在非负格式化货币值的后面 |
| char int_p_sep_by_space | 如果该值为1,则用空格把int_currency_symbol和非负格式化货币值隔开;如果该值为0,则不用空格分隔int_currency_symbol和非负格式化货币值 |
| char int_n_cs_precedes | 如果该值为1,则int_currency_symbol在负格式化货币值的前面;如果该值为0,则int_currency_symbol在负格式化货币值的后面 |
| char int_n_sep_by_space | 如果该值为1,则用空格把int_currency_symbol和负格式化货币值隔开;如果该值为0,则不用空格分隔int_currency_symbol和负格式化货币值 |
| char int_p_sign_posn | 其值表示positive_sign相对于非负国际格式化货币值的位置 |
| char int_n_sign_posn | 其值表示negative_sign相对于负国际格式化货币值的位置 |

## B.5.10 数学库:math.h

C99为math.h头文件定义了两种类型:float\_t和double\_t。这两种类型分别与float和double类型至少等宽，是计算float和double时效率最高的类型。

该头文件还定义了一些宏，如表B.5.15所列。该表中除了HUGE\_VAL外，都是C99新增的。在参考资料VIII:“C99数值计算增强”中会进一步详细介绍。

表B.5.15 math.h宏

| 宏 | 描述 |
| --- | --- |
| HUGE_VAL | 正双精度常量,不一定能用浮点数表示;在过去,函数的计算结果超过了可表示的最大值时,就用它作为函数的返回值 |
| HUGE_VALF | 与 HUGE_VAL 类似,适用于 float 类型 |
| HUGE_VALL | 与 HUGE_VAL 类似,适用于 long double 类型 |
| INFINITY | 如果允许的话,展开为一个表示无符号或正无穷大的常量 float 表达式;否则,展开为一个在编译时溢出的正浮点常量 |

续表

| 宏 | 描述 |
| --- | --- |
| NAN | 当且仅当实现支持float类型的NaN时才被定义(NaN是Not-a-Number的缩写,表示“非数”,用于处理计算中的错误情况,如除以0.0或求负数的平方根) |
| FP_INFINITE | 分类数,表示一个无穷大的浮点值 |
| FP_NAN | 分类数,表示一个不是数的浮点值 |
| FP_NORMAL | 分类数,表示一个正常的浮点值 |
| FP_SUBNORMAL | 分类数,表示一个低于正常浮点值的值(精度被降低) |
| FP_ZERO | 分类数,表示0的浮点值 |
| FP_FAST_FMA | (可选)如果已定义,对于double类型的运算对象,该宏表明fma()函数与先乘法运算后加法运算的速度相当或更快 |
| FP_FAST_FMAF | (可选)如果已定义,对于double类型的运算对象,该宏表明fmaf()函数与先乘法运算后加法运算的速度相当或更快 |
| FP_FAST_FMAL | (可选)如果已定义,对于long double类型的运算对象,该宏表明fmal()函数与先乘法运算后加法运算的速度相当或更快 |
| FP_ILOGBO | 整型常量表达式,表示ilogn(0)的返回值 |
| FP_ILOGBNAN | 整型常量表达式,表示ilogn(NaN)的返回值 |
| MATH_ERRNO | 展开为整型常量1 |
| MATH_ERREXCEPT | 展开为整型常量2 |
| math_errhandling | 值为MATH_ERRNO、MATH_ERREXCEPT或这两个值的按位或 |

数学函数通常使用double类型的值。C99新增了这些函数的float和long double版本，其函数名为分别在原函数名后添加f后缀和l后缀。例如，C语言现在提供这些函数原型:

double sin(double);

float sinf(float);

long double sinl(long double);

篇幅有限，表B.5.16仅列出了数学库中这些函数的double版本。该表引用了FLT\_RADIX，该常量定义在float.h中，代表内部浮点表示法中幂的底数。最常用的值是2。

表B.5.16 ANSI C标准数学函数

| 原型 | 描述 |
| --- | --- |
| int classify(real-floating x); | C99 宏,返回适合 x 的浮点分类值 |
| int isfinite(real-floating x); | C99 宏,当且仅当 x 为有穷时返回一个非 0 值 |
| int isfin(real-floatingx); | C99 宏,当且仅当 x 为无穷时返回一个非 0 值 |
| int isnan(real-floatingx); | C99 宏,当且仅当 x 为 NaN 时返回一个非 0 值 |
| int isnormal(real-floatingx); | C99 宏,当且仅当 x 为正常数时返回一个非 0 值 |
| int signbit(real-floating x); | C99 宏,当且仅当 x 的符号为负时返回一个非 0 值 |
| double acos(double x); | 返回余弦为 x 的角度(0~π弧度) |
| double asin(double x); | 返回正弦为 x 的角度(-π/2~π/2 弧度) |
| double atan(double x); | 返回正切为 x 的角度(-π/2~π/2 弧度) |

续表

| 原型 | 描述 |
| --- | --- |
| double atan2(double y, double x); | 返回正切为y/x的角度(-π~π弧度) |
| double cos(double x); | 返回x(弧度)的余弦值 |
| double sin(double x); | 返回x(弧度)的正弦值 |
| double tan(double x); | 返回x(弧度)的正切值 |
| double cosh(double x); | 返回x的双曲余弦值 |
| double sinh(double x); | 返回x的双曲正弦值 |
| double tanh(double x); | 返回x的双曲切值 |
| double exp(double x); | 返回e的x次幂($e^x$) |
| double exp2(double x); | 返回2的x次幂($2^x$) |
| double expm1(double x); | 返回$e^x - 1$(C99) |
| double frexp(double v, int *pt_e); | 把v的值分成两部分,一个是返回的规范化小数;一个是2的幂,储存在pt_e指向的位置上 |
| int ilogb(double x); | 以signed int类型返回x的指数(C99) |
| double ldexp(double x, int p); | 返回x乘以2的p次幂(即$x * 2^p$) |
| double log(double x); | 返回x的自然对数 |
| double log10(double x); | 返回以10为底x的对数 |
| double log1p(double x); | 返回log(1 + x)(C99) |
| double log2(double x); | 返回以2为底x的对数(C99) |
| double logb(double x); | 返回FLT_RADIX(系统内部浮点表示法中幂的底数)为底x的有符号对数(C99) |
| double modf(double x, double *p); | 把x分成整数部分和小数部分,两部分的符号相同,返回小数部分,并把整数部分储存在p所指向的位置上 |
| double scalbn(double x, int n); | 返回x × FLT_RADIX$^n$(C99) |
| double scalbln(double x, long n); | 返回x × FLT_RADIX$^n$(C99) |
| double cbrt(double x); | 返回x的立方根(C99) |
| double hypot(double x, double y); | 返回x平方与y平方之和的平方根(C99) |
| double pow(double x, double y); | 返回x的y次幂 |
| double sqrt(double x); | 返回x的平方根 |
| double erf(double x); | 返回x的误差函数(C99) |
| double lgamma(double x); | 返回x的伽马函数绝对值的自然对数(C99) |
| double tgamma(double x); | 返回x的伽马函数(C99) |
| double ceil(double x); | 返回不小于x的最小整数值 |
| double fabs(double x); | 返回x的绝对值 |
| double floor(double x); | 返回不大于x的最大值 |
| double nearbyint(double x); | 以浮点格式把x四舍五入为最接近的整数;使用浮点环境指定的舍入规则(C99) |

续 表

| 原型 | 描述 |
| --- | --- |
| double rint(double x); | 与 nearbyint() 类似,但是该函数会抛出“不精确”异常 |
| long int lrint(double x); | 以 long int 格式把 x 舍入为最接近的整数;使用浮点环境指定的舍入规则(C99) |
| long long int llrint(double x); | 以 long long int 格式把 x 舍入为最接近的整数;使用浮点环境指定的舍入规则(C99) |
| double round(double x); | 以浮点格式把 x 舍入为最接近的整数,总是四舍五入 |
| long int lround(double x); | 与 round() 类似,但是该函数返回值的类型是 long int |
| long long int llround(double x); | 与 round() 类似,但是该函数返回值的类型是 long long int |
| double trunc(double x); | 以浮点格式把 x 舍入为最接近的整数,其结果的绝对值不大于 x 的绝对值(C99) |
| int fmod(double x, double y); | 返回 x/y 的小数部分,如果 y 不是 0,则其计算结果的符号与 x 相同,而且该结果的绝对值要小于 y 的绝对值 |
| double remainder(double x, double y); | 返回 x 除以 y 的余数,IEC 60559 定义为 x - n*y,n 取与 x/y 最接近的整数;如果 (n - x/y) 的绝对值是 1/2,n 取偶数 |
| double remquo(double x, double y, int *quo); | 返回与 remainder() 相同的值;把 x/y 的整数大小求模 $2^k$ 的值储存在 quo 所指向的位置中,符号与 x/y 的符号相同,其中 k 为整数,至少是 3,具体值因实现而异(C99) |
| double copysign(double x, double y); | 返回 x 的大小和 y 的符号(C99) |
| double nan(const char *tagp); | 返回以 double 类型表示的 quiet NaN';nan("n-char-seq") 与 strtod("NAN(n-char-seq)", (char **)NULL) 等价;nan("")与 strtod("NAN()", (char**)NULL)等价。如果不支持 quiet NaN,则返回 0 |
| double nextafter(double x, double y); | 返回 x 在 y 方向上可表示的最接近的 double 类型值;如果 x 等于 y,则返回 x(C99) |
| double nexttoward(double x, long double y); | 与 nextafter() 类似,但该函数的第 2 个参数是 long double 类型;如果 x 等于 y,则返回转换为 double 类型的 y(C99) |
| double fdim(double x, double y); | 如果 x 大于 y,则返回 x - y 的值;如果 x 小于或等于 y,则返回 0(C99) |
| double fmax(double x, double y); | 返回参数的最大值,如果一个参数是 NaN、另一个参数是数值,则返回数值(C99) |
| double fmin(double x, double y); | 返回参数的最小值,如果一个参数是 NaN、另一个参数是数值,则返回数值(C99) |
| double fma(double x, double y, double z); | 返回三元运算 (x*y)+z 的大小,只在最后舍入一次(C99) |
| int isgreater(real-floating x, real-floating y); | C99 宏,返回 (x)>(y) 的值,如果有参数是 NaN,不会抛出“无效”浮点异常 |
| int isgreaterequal(real-floating x,real-floating y); | C99 宏,返回 (x)>(y) 的值,如果有参数是 NaN,不会抛出无效浮点异常 |

1 NaN 分为两类:quite NaN 和 singaling NaN。两者的区别是:quite NaN 的尾数部分最高位定义为1，而singaling NaN最高位定义为0。——译者注

续表

| 原型 | 描述 |
| --- | --- |
| intisless(real-floating x, real-floatingy); | C99 宏,返回(x)&lt;(y)的值,如果有参数是 NaN,不会抛出无效浮点异常 |
| int islessequal(real-floating x, real-floating y); | C99 宏,返回(x)&lt;=(y)的值,如果有参数是 NaN,不会抛出无效浮点异常 |
| int islessgreater(real-floating x, real-floating y); | C99 宏,返回(x)&lt;(y)\|\| (x)>(y)的值,如果有参数是 NaN,不会抛出无效浮点异常 |
| int isunordered(real-floating x, real-floating y); | 如果参数不按顺序排列(至少有一个参数是 NaN),函数返回 1;否则,返回 0 |

## B.5.11 非本地跳转:setjmp.h

setjmp.h 头文件可以让你不遵循通常的函数调用、函数返回顺序。setjmp()函数把当前执行环境的信息（例如，指向当前指令的指针）储存在jmp\_buf类型（定义在setjmp.h头文件中的数组类型）的变量中，然后longjmp()函数把执行转至这个环境中。这些函数主要是用来处理错误条件，并不是通常程序流控制的一部分。表B.5.17列出了这些函数。

表B.5.17 setjmp.h中的函数

| 原型 | 描述 |
| --- | --- |
| int setjmp(jmp_buf env); | 把调用环境储存在数组env中,如果是直接调用,则返回0;如果是通过longjmp()调用,则返回非0 |
| void longjmp(jmp_buf env,int val); | 恢复最近的setjmp()调用(设置env数组)储存的环境;完成后,程序继续像调用setjmp()那样执行该函数,返回val(但是该函数不允许返回0,会将其转换成1) |

## B.5.12 信号处理:signal.h

信号（signal）是在程序执行期间可以报告的一种情况，可以用正整数表示。raise()函数发送（或抛出）一个信号，signal()函数设置特定信号的响应。

标准定义了一个整数类型:sig\_atomic\_t，专门用于在处理信号时指定原子对象。也就是说，更新原子类型是不可分割的过程。

标准提供的宏列于表B.5.18中，它们表示可能的信号，可用作raise()和signal()的参数。当然，实现也可以添加更多的值。

表B.5.18 信号宏