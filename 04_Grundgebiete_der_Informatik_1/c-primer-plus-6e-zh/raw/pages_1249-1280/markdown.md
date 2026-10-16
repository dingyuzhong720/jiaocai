## 16.9 C库

最初，并没有官方的C库。后来，基于UNIX的C实现成为了标准。ANSI C委员会主要以这个标准为基础，开发了一个官方的标准库。在意识到C语言的应用范围不断扩大后，该委员会重新定义了这个库，使之可以应用于其他系统。

我们讨论过一些标准库中的 I/O 函数、字符函数和字符串函数。本章将介绍更多函数。不过，首先要学习如何使用库。

## 16.9.1 访问C库

如何访问C库取决于实现，因此你要了解当前系统的一般情况。首先，可以在多个不同的位置找到库函数。例如，getchar()函数通常作为宏定义在stdio.h头文件中，而strlen()通常在库文件中。其次，不同的系统搜索这些函数的方法不同。下面介绍3种可能的方法。

## 1.自动访问

在一些系统中，只需编译程序，就可使用一些常用的库函数。

记住，在使用函数之前必须先声明函数的类型，通过包含合适的头文件即可完成。在描述库函数的用户手册中，会指出使用某函数时应包含哪个头文件。但是在一些旧系统上，可能必须自己输入函数声明。再次提醒读者，用户手册中指明了函数类型。另外，附录B“参考资料”中根据头文件分组，总结了ANSI C库函数。

过去，不同的实现使用的头文件名不同。ANSI C标准把库函数分为多个系列，每个系列的函数原型都放在一个特定的头文件中。

## 2.文件包含

如果函数被定义为宏，那么可以通过#include 指令包含定义宏函数的文件。通常，类似的宏都放在合适名称的头文件中。例如，许多系统（包括所有的ANSI C系统）都有ctype.h文件，该文件中包含了一些确定字符性质（如大写、数字等）的宏。

## 3.库包含

在编译或链接程序的某些阶段，可能需要指定库选项。即使在自动检查标准库的系统中，也会有不常用的函数库。必须通过编译时选项显式指定这些库。注意，这个过程与包含头文件不同。头文件提供函数声明或原型，而库选项告诉系统到哪里查找函数代码。虽然这里无法涉及所有系统的细节，但是可以提醒读者应该注意什么。

## 16.9.2 使用库描述

篇幅有限，我们无法讨论完整的库。但是，可以看几个具有代表性的示例。首先，了解函数文档。

可以在多个地方找到函数文档。你所使用的系统可能有在线手册，集成开发环境通常都有在线帮助。C实现的供应商可能提供描述库函数的纸质版用户手册，或者把这些材料放在CD-ROM中或网上。有些出版社也出版C库函数的参考手册。这些材料中，有些是一般材料，有些则是针对特定实现的。本书附录B中提供了一个库函数的总结。

阅读文档的关键是看懂函数头。许多内容随时间变化而变化。下面是旧的UNIX文档中，关于fread()的描述:

#include &lt;stdio.h&gt;

fread(ptr, sizeof(\*ptr), nitems, stream)

FILE \*stream;

首先，给出了应该包含的文件，但是没有给出fread()、ptr、sizeof(\*ptr)或nitems的类型。过去，默认类型都是int，但是从描述中可以看出ptr是一个指针（在早期的C中，指针被作为整数处理）。参数stream声明为指向FILE的指针。上面的函数声明中的第2个参数看上去像是sizeof运算符，而实际上这个参数的值应该是ptr所指向对象的大小。虽然用sizeof作为参数没什么问题，但是用int类型的值作为参数更符合语法。

后来，上面的描述变成了:

```c
#include <stdio.h>

int fread(ptr, size, nitems, stream;)

char *ptr;

int size, nitems;

FILE *stream;
```

现在，所有的类型都显式说明，ptr作为指向char的指针。

ANSI C90标准提供了下面的描述:

```c
#include <stdio.h>
```

size\_t fread(void \*ptr, size\_t size, size\_t nmemb, FILE \*stream);

首先，使用了新的函数原型格式。其次，改变了一些类型。size\_t 类型被定义为 sizeof 运算符的返回值类型——无符号整数类型，通常是unsigned int或unsigned long。stddef.h文件中包含了size\_t类型的typedef或#define定义。其他文件（包括stdio.h）通过包含stddef.h来包含这个定义。许多函数（包括fread()）的实际参数中都要使用sizeof运算符，形式参数的size\_t类型中正好匹配这种常见的情况。

另外，ANSI C把指向void的指针作为一种通用指针，用于指针指向不同类型的情况。例如，fread()的第1个参数可能是指向一个double类型数组的指针，也可能是指向其他类型结构的指针。如果假设实际参数是一个指向内含20个double类型元素数组的指针，且形式参数是指向void的指针，那么编译器会选用合适的类型，不会出现类型冲突的问题。

C99/C11标准在以上的描述中加入了新的关键字restric:

#include &lt;stdio.h&gt;

size\_t fread(void \* restrict ptr, size\_t size,size\_t nmemb, FILE \* restrict stream);

接下来，我们讨论一些特殊的函数。

## 16.10 数学库

数学库中包含许多有用的数学函数。math.h头文件提供这些函数的原型。表16.2中列出了一些声明在 math.h 中的函数。注意，函数中涉及的角度都以弧度为单位（1 弧度 $180/\pi=57.296$ 度）。参考资料 V“新增C99和C11标准的ANSI C库”列出了C99和C11标准的所有函数。

表16.2 ANSI C标准的一些数学函数

| 原型 | 描述 |
| --- | --- |
| double acos(double x) | 返回余弦值为x的角度(0~π弧度) |
| double asin(double x) | 返回正弦值为x的角度(-π/2~π/2弧度) |
| double atan(double x) | 返回正切值为x的角度(-π/2~π/2弧度) |
| double atan2(double y, double x) | 返回正弦值为y/x的角度(-π~π弧度) |
| double cos(double x) | 返回x的余弦值,x的单位为弧度 |
| double sin(double x) | 返回x的正弦值,x的单位为弧度 |
| double tan(double x) | 返回x的正切值,x的单位为弧度 |
| double exp(double x) | 返回x的指数函数的值($e^x$) |
| double log(double x) | 返回x的自然对数值 |
| double log10(double x) | 返回x的以10为底的对数值 |
| double pow(double x, doubley) | 返回x的y次幂 |
| double sqrt(double x) | 返回x的平方值 |
| double cbrt(double x) | 返回x的立方值 |
| double ceil(double x) | 返回不小于x的最小整数值 |
| double fabs(double x) | 返回x的绝对值 |
| double floor(double x) | 返回不大于x的最大整数值 |

## 16.10.1 三角问题

我们可以使用数学库解决一些常见的问题:把x/y坐标转换为长度和角度。例如，在网格上画了一条线，该线条水平穿过了4个单元（x的值），垂直穿过了3个单元（y的值）。那么，该线的长度（量）和方向是什么？根据数学的三角公式可知:

$$
\text {大小} = \text {square root} \left(\mathrm{x} ^ {2} + \mathrm{y} ^ {2}\right)
$$

数学库提供平方根函数和一对反正切函数，所以可以用C程序表示这个问题。平方根函数是sqrt()，接受一个double类型的参数，并返回参数的平方根，也是double类型。

atan()函数接受一个double类型的参数（即正切值），并返回一个角度（该角度的正切值就是参数值）。但是，当线的x值和y值均为-5时，atan()函数产生混乱。因为(-5)/(-5)得1，所以atan()返回45°，该值与x和y均为5时的返回值相同。也就是说，atan()无法区分角度相同但反向相反的线（实际上，atan()返回值的单位是弧度而不是度，稍后介绍两者的转换）。

当然，C库还提供了atan2()函数。它接受两个参数:x的值和y的值。这样，通过检查x和y的正负号就可以得出正确的角度值。atan2()和 atan()均返回弧度值。把弧度转换为度，只需将弧度值乘以180，再除以pi即可。pi的值通过计算表达式4\*atan(1)得到。程序清单16.13演示了这些步骤。另外，学习该程序还复习了结构和typedef相关的知识。

程序清单**16.14 rect\_pol.c**程序

```c
/* rect_pol.c -- 把直角坐标转换为极坐标 */
#include <stdio.h>
#include <math.h>
#define RAD_TO_DEG (180/(4 * atan(1)))
typedef struct polar_v {
double magnitude;
double angle;
} Polar_V;
```

```c
typedef struct rect_v {
double x;
double y;
} Rect_V;
Polar_V rect_to_polar(Rect_V);
int main(void)
{
Rect_V input;
Polar_V result;
puts("Enter x and y coordinates; enter q to quit:");
while (scanf("%lf %lf", &input.x, &input.y) == 2)
{
result = rect_to_polar(input);
printf("magnitude = %0.2f, angle = %0.2f\n",
result.magnitude, result.angle);
}
puts("Bye.");
return 0;
}
```

```c
Polar_V rect_to_polar(Rect_V rv)
{
Polar_V pv;
pv.magnitude = sqrt(rv.x * rv.x + rv.y * rv.y);
if (pv.magnitude == 0)
pv.angle = 0.0;
else
pv.angle = RAD_TO_DEG * atan2(rv.y, rv.x);
return pv;
}
```

下面是运行该程序后的一个输出示例:

Enter x and y coordinates; enter q to quit:

**10 10**

magnitude = 14.14, angle = 45.00

**-12 -5**

magnitude = 13.00, angle = -157.38

q

Bye.

如果编译时出现下面的消息:

Undefined: \_sqrt

或

'sqrt': unresolved external

或者其他类似的消息，表明编译器链接器没有找到数学库。UNIX系统会要求使用-lm标记（flag）指示链接器搜索数学库:

cc rect\_pol.c –lm

注意，-lm标记在命令行的末尾。因为链接器在编译器编译C文件后才开始处理。在Linux中使用GCC编译器可能要这样写:

gcc rect\_pol.c -lm

## 16.10.2 类型变体

基本的浮点型数学函数接受double类型的参数，并返回double类型的值。当然，也可以把float或 long double 类型的参数传递给这些函数，它们仍然能正常工作，因为这些类型的参数会被转换成double类型。这样做很方便，但并不是最好的处理方式。如果不需要双精度，那么用float类型的单精度值来计算会更快些。而且把long double类型的值传递给double类型的形参会损失精度，形参获得的值可能不是原来的值。为了解决这些潜在的问题，C标准专门为float类型和long double类型提供了标准函数，即在原函数名前加上f或l前缀。因此，sqrtf()是sqrt()的float版本，sqrtl()是sqrt()的long double版本。

利用C11 新增的泛型选择表达式定义一个泛型宏，根据参数类型选择最合适的数学函数版本。程序清单16.15演示了两种方法。

程序清单**16.15 generic.c**程序

// generic.c -- 定义泛型宏

```c
#include <stdio.h>

#include <math.h>

#define RAD_TO_DEG (180/(4 * atanl(1)))
// 泛型平方根函数
#define SQRT(X) _Generic((X),\
long double: sqrtl, \
default: sqrt, \
float: sqrtf)(X)
// 泛型正弦函数，角度的单位为度
#define SIN(X) _Generic((X),\
long double: sinl((X)/RAD_TO_DEG),\
default:   sin((X)/RAD_TO_DEG),\
float:    sinf((X)/RAD_TO_DEG)\
)

int main(void)
{

float x = 45.0f;

double xx = 45.0;

long double xxx = 45.0L;
```

```c
long double y = SQRT(x);
long double yy = SQRT(xx);
long double yyy = SQRT(xxx);
printf("%.17Lf\n", y);      // 匹配 float
printf("%.17Lf\n", yy);     // 匹配 default
printf("%.17Lf\n", yyy);   // 匹配 long double
int i = 45;
yy = SQRT(i);                     // 匹配 default
printf("%.17Lf\n", yy);
yyy = SIN(xxx);                 // 匹配 long double
printf("%.17Lf\n", yyy);
return 0;
}
下面是该程序的输出:
6.70820379257202148
6.70820393249936942
6.70820393249936909
6.70820393249936942
0.70710678118654752
```

如上所示，SQRT(i)和SQRT(xx)的返回值相同，因为它们的参数类型分别是int和double，所以只能与default标签对应。

有趣的一点是，如何让\_Generic 宏的行为像一个函数。SIN()的定义也许提供了一个方法:每个带标号的值都是函数调用，所以\_Generic表达式的值是一个特定的函数调用，如sinf((X)/RAD\_TO\_DEG)，用传入SIN()的参数替换X。

SQRT()的定义也许更简洁。\_Generic表达式的值就是函数名，如sinf。函数的地址可以代替该函数名，所以\_Generic表达式的值是一个指向函数的指针。然而，紧随整个\_Generic表达式之后的是(X)，函数指针(参数)表示函数指针。因此，这是一个带指定的参数的函数指针。

简而言之，对于 SIN()，函数调用在泛型选择表达式内部；而对于SQRT()，先对泛型选择表达式求值得一个指针，然后通过该指针调用它所指向的函数。

## 16.10.3 tgmath.h库（C99）

C99标准提供的tgmath.h头文件中定义了泛型类型宏，其效果与程序清单16.15类似。如果在math.h中为一个函数定义了3种类型（float、double和long double）的版本，那么tgmath.h文件就创建一个泛型类型宏，与原来 double版本的函数名同名。例如，根据提供的参数类型，定义 sqrt()宏展开为sqrtf()、sqrt()或 sqrtl()函数。换言之，sqrt()宏的行为和程序清单 16.15 中的SQRT()宏类似。

如果编译器支持复数运算，就会支持complex.h头文件，其中声明了与复数运算相关的函数。例如，声明有 csqrtf()、csqrt()和 csqrtl()，这些函数分别返回 float complex、double complex和long double complex类型的复数平方根。如果提供这些支持，那么tgmath.h中的sqrt()宏也能展开为相应的复数平方根函数。

如果包含了tgmath.h，要调用sqrt()函数而不是sqrt()宏，可以用圆括号把

被调用的函数名括起来:

```c
#include <tgmath.h>
```

```txt
...
```

```txt
float x = 44.0;
```

```txt
double y;
```

<div class="docvortex-algorithm" style="white-space: pre-wrap; font-family:monospace;">
$y = \text{sqrt}(x); \quad // \text{调用宏，所以是} \text{sqrt}(x)$
</div>

<div class="docvortex-algorithm" style="white-space: pre-wrap; font-family:monospace;">
$y=(\text{sqrt})(x); \quad // \text{调用函数 sqrt()}$
</div>

这样做没问题，因为类函数宏的名称必须用圆括号括起来。圆括号只会影响操作顺序，不会影响括起来的表达式，所以这样做得到的仍然是函数调用的结果。实际上，在讨论函数指针时提到过，由于C语言奇怪而矛盾的函数指针规则，还也可以使用(\*sqrt)()的形式来调用sqrt()函数。

不借助C标准以外的机制，C11新增的\_Generic表达式是实现tgmath.h最简单的方式。

## 16.11 通用工具库

通用工具库包含各种函数，包括随机数生成器、查找和排序函数、转换函数和内存管理函数。第12章介绍过rand()、srand()、malloc()和free()函数。在ANSI C标准中，这些函数的原型都在stdlib.h头文件中。附录B参考资料V列出了该系列的所有函数。现在，我们来进一步讨论其中的几个函数。

## 16.11.1 exit()和atexit()函数

在前面的章节中我们已经在程序示例中用过 exit()函数。而且，在main()返回系统时将自动调用exit()函数。ANSI 标准还新增了一些不错的功能，其中最重要的是可以指定在执行 exit()时调用的特定函数。atexit()函数通过退出时注册被调用的函数提供这种功能，atexit()函数接受一个函数指针作为参数。程序清单16.16演示了它的用法。

程序清单16.16 byebye.c程序

```c
/* byebye.c -- atexit()示例 */

#include <stdio.h>

#include <stdlib.h>

void sign_off(void);

void too_bad(void);

int main(void)

{

int n;

atexit(sign_off);      /* 注册 sign_off()函数 */
```

```c
puts("Enter an integer:");
if (scanf("%d", &n) != 1)
{
puts("That's no integer!");
atexit(too_bad); /* 注册 too_bad()函数 */
exit(EXIT_FAILURE);
}
printf("%d is %s.\n", n, (n % 2 == 0) ? "even" : "odd");
return 0;
}
void sign_off(void)
{
puts("Thus terminates another magnificent program from");
puts("SeeSaw Software!");
}
void too_bad(void)
{
puts("SeeSaw Software extends its heartfelt condolences");
puts("to you upon the failure of your program.");
```

}

下面是该程序的一个运行示例:

Enter an integer:

## 212

212 is even.

Thus terminates another magnificent program from

SeeSaw Software!

如果在IDE中运行，可能看不到最后两行。下面是另一个运行示例:

Enter an integer:

## what?

That's no integer!

SeeSaw Software extends its heartfelt condolences

to you upon the failure of your program.

Thus terminates another magnificent program from

SeeSaw Software!

在IDE中运行，可能看不到最后4行。

接下来，我们讨论atexit()和exit()的参数。

## 1.atexit()函数的用法

这个函数使用函数指针。要使用 atexit()函数，只需把退出时要调用的函数地址传递给 atexit()即可。函数名作为函数参数时相当于该函数的地址，所以该程序中把sign\_off或too\_bad作为参数。然后，atexit()注册函数列表中的函数，当调用exit()时就会执行这些函数。ANSI保证，在这个列表中至少可以放 32 个函数。最后调用 exit()函数时，exit()会执行这些函数（执行顺序与列表中的函数顺序相反，即最后添加的函数最先执行）。

注意，输入失败时，会调用sign\_off()和too\_bad()函数；但是输入成功时只会调用sign\_off()。因为只有输入失败时，才会进入if语句中注册too\_bad()。另外还要注意，最先调用的是最后一个被注册的函数。

atexit()注册的函数（如sign\_off()和too\_bad()）应该不带任何参数且返回类型为void。通常，这些函数会执行一些清理任务，例如更新监视程序的文件或重置环境变量。

注意，即使没有显式调用exit()，还是会调用sign\_off()，因为main()结束时会隐式调用exit()。

## 2.exit()函数的用法

exit()执行完atexit()指定的函数后，会完成一些清理工作:刷新所有输出流、关闭所有打开的流和关闭由标准I/O函数tmpfile()创建的临时文件。然后exit()把控制权返回主机环境，如果可能的话，向主机环境报告终止状态。通常，UNIX程序使用0表示成功终止，用非零值表示终止失败。UNIX返回的代码并不适用于所有的系统，所以ANSI C为了可移植性的要求，定义了一个名为EXIT\_FAILURE的宏表示终止失败。类似地，ANSI C还定义了EXIT\_SUCCESS表示成功终止。不过，exit()函数也接受0表示成功终止。在ANSI C中，在非递归的main()中使用exit()函数等价于使用关键字return。尽管如此，在main()以外的函数中使用exit()也会终止整个程序。

## 16.11.2 qsort()函数

对较大型的数组而言，“快速排序”方法是最有效的排序算法之一。该算法由C.A.R.Hoare于1962年开发。它把数组不断分成更小的数组，直到变成单元素数组。首先，把数组分成两部分，一部分的值都小于另一部分的值。这个过程一直持续到数组完全排序好为止。

快速排序算法在C实现中的名称是qsort()。qsort()函数排序数组的数据对象，其原型如下:

void qsort(void \*base, size\_t nmemb, size\_t size,

int (\*compar)(const void \*, const void \*));

第1个参数是指针，指向待排序数组的首元素。ANSI C允许把指向任何数据类型的指针强制转换成指向void的指针，因此，qsort()的第1个实际参数可以引用任何类型的数组。

第2个参数是待排序项的数量。函数原型把该值转换为size\_t类型。前面提到过，size\_t定义在标准头文件中，是sizeof运算符返回的整数类型。

由于qsort()把第1个参数转换为void指针，所以qsort()不知道数组中每个元素的大小。为此，函数原型用第 3 个参数补偿这一信息，显式指明待排序数组中每个元素的大小。例如，如果排序 double类型的数组，那么第3个参数应该是sizeof(double)。

最后，qsort()还需要一个指向函数的指针，这个被指针指向的比较函数用于确定排序的顺序。该函数应接受两个参数:分别指向待比较两项的指针。如果第1项的值大于第2项，比较函数则返回正数；如果两项相同，则返回0；如果第1项的值小于第2项，则返回负数。qsort()根据给定的其他信息计算出两个指针的值，然后把它们传递给比较函数。

qsort()原型中的第4个函数确定了比较函数的形式:

int (\*compar)(const void \*, const void \*)

这表明 qsort()最后一个参数是一个指向函数的指针，该函数返回 int 类型的值且接受两个指向const void的指针作为参数，这两个指针指向待比较

项。

程序清单16.17和后面的讨论解释了如何定义一个比较函数，以及如何使用qsort()。该程序创建了一个内含随机浮点值的数组，并排序了这个数组。

程序清单16.17 qsorter.c程序

```c
/* qsorter.c -- 用 qsort()排序一组数字 */
#include <stdio.h>
#include <stdlib.h>
#define NUM 40
void fillarray(double ar [], int n);
void showarray(const double ar [], int n);
int mycomp(const void * p1, const void * p2);
int main(void)
{
double vals[NUM];
fillarray(vals, NUM);
puts("Random list:");
showarray(vals, NUM);
qsort(vals, NUM, sizeof(double), mycomp);
puts("\nSorted list:");
```

```c
showarray(vals, NUM);

return 0;

}

void fillarray(double ar [], int n)

{

int index;

for (index = 0; index < n; index++)

ar[index] = (double) rand() / ((double) rand() + 0.1);

}

void showarray(const double ar [], int n)

{

int index;

for (index = 0; index < n; index++)

{

printf("%9.4f", ar[index]);

if (index % 6 == 5)

putchar('\n');

}

if (index % 6 != 0)
```

```c
putchar('\n');
}
/* 按从小到大的顺序排序 */
int mycomp(const void * p1, const void * p2)
{
/* 要使用指向double的指针来访问这两个值 */
const double * a1 = (const double *) p1;
const double * a2 = (const double *) p2;
if (*a1 < *a2)
return -1;
else if (*a1 == *a2)
return 0;
else
return 1;
}
```

下面是该程序的运行示例:

Random list:

```txt
0.0001 1.6475 2.4332 0.0693 0.7268 0.7383  
24.0357 0.1009 87.1828 5.7361 0.6079 0.6330
```

| 1.6058 | 0.1406 | 0.5933 | 1.1943 | 5.5295 | 2.2426 |
| --- | --- | --- | --- | --- | --- |
| 0.8364 | 2.7127 | 0.2514 | 0.9593 | 8.9635 | 0.7139 |
| 0.6249 | 1.6044 | 0.8649 | 2.1577 | 0.5420 | 15.0123 |
| 1.7931 | 1.6183 | 1.9973 | 2.9333 | 12.8512 | 1.3034 |
| 0.3032 | 1.1406 | 18.7880 | 0.9887 |  |  |

Sorted list:

| 0.0001 | 0.0693 | 0.1009 | 0.1406 | 0.2514 | 0.3032 |
| --- | --- | --- | --- | --- | --- |
| 0.5420 | 0.5933 | 0.6079 | 0.6249 | 0.6330 | 0.7139 |
| 0.7268 | 0.7383 | 0.8364 | 0.8649 | 0.9593 | 0.9887 |
| 1.1406 | 1.1943 | 1.3034 | 1.6044 | 1.6058 | 1.6183 |
| 1.6475 | 1.7931 | 1.9973 | 2.1577 | 2.2426 | 2.4332 |
| 2.7127 | 2.9333 | 5.5295 | 5.7361 | 8.9635 | 12.8512 |
| 15.0123 | 18.7880 | 24.0357 | 87.1828 |  |  |

接下来分析两点:qsort()的用法和mycomp()的定义。

## 1.qsort()的用法

qsort()函数排序数组的数据对象。该函数的ANSI原型如下:

void qsort (void \*base, size\_t nmemb, size\_t size,

int (\*compar)(const void \*, const void \*));

第1个参数值指向待排序数组首元素的指针。在该程序中，实际参数是double类型的数组名vals，因此指针指向该数组的首元素。根据该函数的原型，参数 vals 会被强制转换成指向 void 的指针。由于ANSI C允许把指向任何数据类型的指针强制转换成指向void的指针，所以qsort()的第1个实际参数可以引用任何类型的数组。

第2个参数是待排序项的数量。在程序清单16.17中是NUM，即数组元素的数量。函数原型把该值转换为size\_t类型。

第3个参数是数组中每个元素占用的空间大小，本例中为sizeof(double)。

最后一个参数是mycomp，这里函数名即是函数的地址，该函数用于比较元素。

## 2.mycomp()的定义

前面提到过，qsort()的原型中规定了比较函数的形式:

int (\*compar)(const void \*, const void \*)

这表明 qsort()最后一个参数是一个指向函数的指针，该函数返回 int 类型的值且接受两个指向const void的指针作为参数。程序中mycomp()使用的就是这个原型:

int mycomp(const void \* p1, const void \* p2);

记住，函数名作为参数时即是指向该函数的指针。因此，mycomp与compar原型相匹配。

qsort()函数把两个待比较元素的地址传递给比较函数。在该程序中，把待比较的两个double类型值的地址赋给p1和p2。注意，qsort()的第1个参数引用整个数组，比较函数中的两个参数引用数组中的两个元素。这里存在一个问题。为了比较指针所指向的值，必须解引用指针。因为值是 double 类型，所以要把指针解引用为 double 类型的值。然而，qsort()要求指针指向void。要解决这个问题，必须在比较函数的内部声明两个类型正确的指针，并初始化它们分别指向作为参数传入的值:

```c
/* 按从小到大的顺序排序值 */
int mycomp(const void * p1, const void * p2)
{
/* 使用指向double类型的指针访问值 */
const double * a1 = (const double *) p1;
const double * a2 = (const double *) p2;
if (*a1 < *a2)
return -1;
else if (*a1 == *a2)
return 0;
else
return 1;
}
```

简而言之，为了让该方法具有通用性，qsort()和比较函数使用了指向void 的指针。因此，必须把数组中每个元素的大小明确告诉qsort()，并且在比较函数的定义中，必须把该函数的指针参数转换为对具体应用而言类型正确的指针。

注意C和C++中的void\*

C和C++对待指向void的指针有所不同。在这两种语言中，都可以把任何类型的指针赋给void类型的指针。例如，程序清单16.17中，qsort()的函数调用中把double\*指针赋给void\*指针。但是，C++要求在把void\*指针赋给任何类型的指针时必须进行强制类型转换。而C没有这样的要求。例如，程序清单16.17中的mycomp()函数，就使用了这样的强制类型转换:

```txt
const double * a1 = (const double *) p1;
```

这种强制类型转换，在C中是可选的，但在C++中是必须的。因为两种语言都使用强制类型转换，所以遵循C++的要求也无不妥。将来如果要把该程序转成C++，就不必更改这部分的代码。

下面再来看一个比较函数的例子。假设有下面的声明:

```txt
struct names {

char first[40];

char last[40];

};

struct names staff[100];
```

如何调用qsort()？模仿程序清单16.17中qsort()的函数调用，应该是这样:

```javascript
qsort(staff, 100, sizeof(struct names), comp);
```

这里 comp 是比较函数的函数名。那么，应如何编写这个函数？假设要先按姓排序，如果同姓再按名排序，可以这样编写该函数:

```c
#include <string.h>

int comp(const void * p1, const void * p2) /* 该函数的形式必须是这样 */
```

```c
{
/* 得到正确类型的指针 */
const struct names *ps1 = (const struct names *) p1;
const struct names *ps2 = (const struct names *) p2;
int res;
res = strcmp(ps1->last, ps2->last); /* 比较姓 */
if (res != 0)
return res;
else /* 如果同姓，则比较名 */
return strcmp(ps1->first, ps2->first);
}
```

该函数使用 strcmp()函数进行比较。strcmp()的返回值与比较函数的要求相匹配。注意，通过指针访问结构成员时必须使用->运算符。

## 16.12 断言库

assert.h 头文件支持的断言库是一个用于辅助调试程序的小型库。它由assert()宏组成，接受一个整型表达式作为参数。如果表达式求值为假（非零），assert()宏就在标准错误流（stderr）中写入一条错误信息，并调用abort()函数终止程序（abort()函数的原型在stdlib.h头文件中）。assert()宏是为了标识出程序中某些条件为真的关键位置，如果其中的一个具体条件为假，就用 assert()语句终止程序。通常，assert()的参数是一个条件表达式或逻辑表达式。如果 assert()中止了程序，它首先会显示失败的测试、包含测试的文件名和行号。

## 16.12.1 assert的用法

程序清单16.18演示了一个使用assert的小程序。在求平方根之前，该程序断言z是否大于或等于0。程序还错误地减去一个值而不是加上一个值，故意让z得到不合适的值。

程序清单16.18 assert.c程序

```c
/* assert.c -- 使用 assert() */

#include <stdio.h>

#include <math.h>

#include <assert.h>

int main()
{
double x, y, z;

puts("Enter a pair of numbers (0 0 to quit): ");
```

while (scanf("%lf%lf", &x, &y) == 2

&& (x != 0 || y != 0))

{

z = x \* x - y \* y; /\* 应该用 + \*/

assert(z >= 0);

printf("answer is %f\n", sqrt(z));

puts("Next pair of numbers: ");

}

puts("Done");

return 0;

}

下面是该程序的运行示例:

Enter a pair of numbers (0 0 to quit):

**4 3**

answer is 2.645751

Next pair of numbers:

**5 3**

answer is 4.000000

Next pair of numbers:

## 3 5

Assertion failed: (z >= 0), function main, file /Users/assert.c, line 14.

具体的错误提示因编译器而异。让人困惑的是，这条消息可能不是指明z >= 0，而是指明没有满足z >=0的条件。

用if语句也能完成类似的任务:

```txt
if (z < 0)
{
puts("z less than 0");
abort();
}
```

但是，使用 assert()有几个好处:它不仅能自动标识文件和出问题的行号，还有一种无需更改代码就能开启或关闭 assert()的机制。如果认为已经排除了程序的 bug，就可以把下面的宏定义写在包含assert.h的位置前面:

#define NDEBUG

并重新编译程序，这样编译器就会禁用文件中的所有 assert()语句。如果程序又出现问题，可以移除这条#define指令（或者把它注释掉），然后重新编译程序，这样就重新启用了assert()语句。

## 16.12.2 \_Static\_assert（C11）

assert()表达式是在运行时进行检查。C11新增了一个特性:

\_Static\_assert声明，可以在编译时检查assert()表达式。因此，assert()可以导致正在运行的程序中止，而\_Static\_assert()可以导致程序无法通过编译。

\_Static\_assert()接受两个参数。第1个参数是整型常量表达式，第2个参数是一个字符串。如果第 1 个表达式求值为 0（或\_False），编译器会显示字符串，而且不编译该程序。看看程序清单16.19的小程序，然后查看assert()和\_Static\_assert()的区别。

程序清单16.19 statasrt.c程序

```c
// statasrt.c
#include <stdio.h>
#include <limits.h>
_Static_assert(CHAR_BIT == 16, "16-bit char falsely assumed");
int main(void)
{
puts("char is 16 bits.");
return 0;
}
下面是在命令行编译的示例:
$ clang statasrt.c
statasrt.c:4:1: error: static_assert failed "16-bit char falsely assumed"
_Static_assert(CHAR_BIT == 16, "16-bit char falsely assumed");
^~~~~~~~~~~~~~~~
1 error generated.
$
```

根据语法，\_Static\_assert()被视为声明。因此，它可以出现在函数中，或者在这种情况下出现在函数的外部。

Static\_assert要求它的第1个参数是整型常量表达式，这保证了能在编译期求值（sizeof表达式被视为整型常量）。不能用程序清单16.18中的assert代替\_Static\_assert，因为assert中作为测试表达式的z > 0不是常量表达式，要到程序运行时才求值。当然，可以在程序清单16.19的main()函数中使用$\begin{array} { r l r } { { \sf a s s e r t } ( { \mathrm { C H A R \_ B I T } } } & { { } = } & { 1 6 ) } \end{array}$ ，但这会在编译和运行程序后才生成一条错误信息，很没效率。

## 16.13 string.h库中的memcpy()和memmove()

不能把一个数组赋给另一个数组，所以要通过循环把数组中的每个元素赋给另一个数组相应的元素。有一个例外的情况是:使用strcpy()和strncpy()函数来处理字符数组。memcpy()和memmove()函数提供类似的方法处理任意类型的数组。下面是这两个函数的原型:

void \*memcpy(void \* restrict s1, const void \* restrict s2, size\_t n);

void \*memmove(void \*s1, const void \*s2, size\_t n);

这两个函数都从 s2 指向的位置拷贝 n 字节到 s1 指向的位置，而且都返回 s1 的值。所不同的是， memcpy()的参数带关键字restrict，即memcpy()假设两个内存区域之间没有重叠；而memmove()不作这样的假设，所以拷贝过程类似于先把所有字节拷贝到一个临时缓冲区，然后再拷贝到最终目的地。如果使用 memcpy()时，两区域出现重叠会怎样？其行为是未定义的，这意味着该函数可能正常工作，也可能失败。编译器不会在本不该使用memcpy()时禁止你使用，作为程序员，在使用该函数时有责任确保两个区域不重叠。

由于这两个函数设计用于处理任何数据类型，所有它们的参数都是两个指向 void 的指针。C 允许把任何类型的指针赋给void \*类型的指针。如此宽容导致函数无法知道待拷贝数据的类型。因此，这两个函数使用第 3 个参数指明待拷贝的字节数。注意，对数组而言，字节数一般与元素个数不同。如果要拷贝数组中10个double类型的元素，要使用10\*sizeof(double)，而不是10。

程序清单16.20中的程序使用了这两个函数。该程序假设double类型是int类型的两倍大小。另外，该程序还使用了C11的\_Static\_assert特性测试断言。

程序清单**16.20 mems.c**程序