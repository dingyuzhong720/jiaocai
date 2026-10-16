printf("ch = %c, i = %d, fl = %2.2f\n", ch, i, fl); /\* 第10行 \*/

$$
\mathrm{ch} = \mathrm{ch} + 1;
$$

/\* 第11行 \*/

$$
\mathrm{i} = \mathrm{fl} + 2 * \mathrm{ch};
$$

/\* 第12行 \*/

$$
\mathrm{fl} = 2. 0 * \mathrm{ch} + \mathrm{i};
$$

/\* 第13行 \*/

printf("ch = %c, i = %d, fl = %2.2f\n", ch, i, fl); /\* 第14行 \*/

$$
\mathrm{ch} = 1 1 0 7;
$$

/\* 第15行 \*/

$$
\operatorname{printf} \left(\text {Now} \mathrm{ch} = \% \mathrm{c} \backslash \mathrm{n} ^ {\prime \prime}, \mathrm{ch}\right);
$$

/\* 第16行 \*/

$$
\mathrm{ch} = 8 0. 8 9;
$$

/\* 第17行 \*/

$$
\operatorname{printf} \left(\text {Now} \mathrm{ch} = \% \mathrm{c} \backslash \mathrm{n} ^ {\prime \prime}, \mathrm{ch}\right);
$$

/\* 第18行 \*/

$$
\begin{array}{l} \text {return} \quad 0; \\ \} \end{array}
$$

运行convert.c后输出如下:

$$
\mathrm{ch} = \mathrm{C}, \mathrm{i} = 6 7, \mathrm{fl} = 6 7. 0 0
$$

$$
\mathrm{ch} = \mathrm{D}, \mathrm{i} = 2 0 3, \mathrm{fl} = 3 3 9. 0 0
$$

$$
\text {Now} \quad \mathrm{ch} = \mathrm{S}
$$

$$
\text {Now} \quad \mathrm{ch} = \mathrm{P}
$$

在我们的系统中，char是8位，int是32位。程序的分析如下。

第9行和第10行:字符'C'被作为1字节的ASCII值储存在ch中。整数变量i接受由'C'转换的整数，即按4字节储存67。最后，fl接受由67转换的浮点数67.00。

第11行和第14行:字符变量'C'被转换成整数67，然后加1。计算结果是4字节整数68，被截断成1字节储存在ch中。根据%c转换说明打印时，68被解释成'D'的ASCII码。

第12行和第14行:ch的值被转换成4字节的整数（68），然后2乘以ch。为了和fl相加，乘积整数（136）被转换成浮点数。计算结果（203.00f）被转换成int类型，并储存在i中。

第13行和第14行:ch的值（'D'，或68）被转换成浮点数，然后2乘以ch。为了做加法，i的值（203）被转换为浮点类型。计算结果（339.00）被储存在fl中。

第15行和第16行:演示了类型降级的示例。把ch设置为一个超出其类型范围的值，忽略额外的位后，最终ch的值是字符S的ASCII码。或者，更确切地说，ch的值是1107 % 265，即83。

第17行和第18行:演示了另一个类型降级的示例。把ch设置为一个浮点数，发生截断后，ch的值是字符P的ASCII码。

## 5.5.1 强制类型转换运算符

通常，应该避免自动类型转换，尤其是类型降级。但是如果能小心使用，类型转换也很方便。我们前面讨论的类型转换都是自动完成的。然而，有时需要进行精确的类型转换，或者在程序中表明类型转换的意图。这种情况下要用到强制类型转换（cast），即在某个量的前面放置用圆括号括起来的类型名，该类型名即是希望转换成的目标类型。圆括号和它括起来的类型名构成了强制类型转换运算符（cast operator），其通用形式是:

(type)

用实际需要的类型（如，long）替换type即可。

考虑下面两行代码，其中mice是int类型的变量。第2行包含两次int强制类型转换。

$$
\mathrm{mice} = 1. 6 + 1. 7;
$$

$$
\mathrm{mice} = (\mathrm{int}) 1. 6 + (\mathrm{int}) 1. 7;
$$

第1 行使用自动类型转换。首先，1.6和1.7相加得3.3。然后，为了匹配int 类型的变量，3.3被类型转换截断为整数3。第2行，1.6和1.7在相加之前都被转换成整数（1），所以把1+1的和赋给变量mice。本质上，两种类型转换都好不到哪里去，要考虑程序的具体情况再做取舍。

一般而言，不应该混合使用类型（因此有些语言直接不允许这样做），但是偶尔这样做也是有用的。C语言的原则是避免给程序员设置障碍，但是程序员必须承担使用的风险和责任。

总结 C的一些运算符

下面是我们学过的一些运算符。

赋值运算符:

= 将其右侧的值赋给左侧的变量

算术运算符:

\+ 将其左侧的值与右侧的值相加

将其左侧的值减去右侧的值

作为一元运算符，改变其右侧值的符号

\* 将其左侧的值乘以右侧的值

/ 将其左侧的值除以右侧的值，如果两数都是整数，计算结果将被截断

% 当其左侧的值除以右侧的值时，取其余数（只能应用于整数）

++ 对其右侧的值加1（前缀模式），或对其左侧的值加1（后缀模式）

对其右侧的值减1（前缀模式），或对其左侧的值减1（后缀模式）

其他运算符:

sizeof 获得其右侧运算对象的大小（以字节为单位），运算对象可以是一个被圆括号括起来的类型说明符，如sizeof(float)，或者是一个具体的变量名、数组名等，如sizeof foo

(类型名) 强制类型转换运算符将其右侧的值转换成圆括号中指定的类型，如(float)9把整数9转换成浮点数9.0

## 5.6 带参数的函数

现在，相信读者已经熟悉了带参数的函数。要掌握函数，还要学习如何编写自己的函数（在此之前，读者可能要复习一下程序清单2.3中的butler()函数，该函数不带任何参数）。程序清单5.15中有一个pound()函数，打印指定数量的#号（该符号也叫作编号符号或井号）。该程序还演示了类型转换的应用。

程序清单5.15 pound.c程序

```c
/* pound.c -- 定义一个带一个参数的函数 */
#include <stdio.h>

void pound(int n);// ANSI函数原型声明

int main(void)
{
int times = 5;

char ch = '!';      // ASCII码是33

float f = 6.0f;

pound(times);          // int类型的参数

pound(ch);               // 和pound((int)ch);相同
pound(f);               // 和pound((int)f);相同

return 0;
}
```

```txt
void pound(int n)      // ANSI风格函数头
{
    // 表明该函数接受一个int类型的参数
while (n-- > 0)
printf("#");
printf("\n");
}
```

运行该程序后，输出如下:

```txt
######
```

```txt
########
```

```txt
########
```

首先，看程序的函数头:

```lisp
void pound(int n)
```

如果函数不接受任何参数，函数头的圆括号中应该写上关键字 void。由于该函数接受一个 int 类型的参数，所以圆括号中包含一个int类型变量n的声明。参数名应遵循C语言的命名规则。

声明参数就创建了被称为形式参数（formal argument或formal parameter，简称形参）的变量。该例中，形式参数是 int 类型的变量 n。像pound(10)这样的函数调用会把 10 赋给 n。在该程序中，调用pound(times)就是把 times 的值（5）赋给 n。我们称函数调用传递的值为实际参数（actual argument或actual parameter），简称实参。所以，函数调用pound(10)把实际参数10传递给函数，然后该函数把10赋给形式参数（变量n）。也就是说，main()中的变量times的值被拷贝给pound()中的新变量n。

## 注意实参和形参

在英文中，argument和parameter经常可以互换使用，但是C99标准规定了:对于actual argument或actual parameter使用术语argument（译为实参）；对于formal argument或formal parameter使用术语parameter（译为形参）。为遵循这一规定，我们可以说形参是变量，实参是函数调用提供的值，实参被赋给相应的形参。因此，在程序清单5.15中，times是pound()的实参，n是pound()的形参。类似地，在函数调用pound(times + 4)中，表达式times + 4的值是该函数的实参。

变量名是函数私有的，即在函数中定义的函数名不会和别处的相同名称发生冲突。如果在pound()中用times代替n，那么这个times与main()中的times不同。也就是说，程序中出现了两个同名的变量，但是程序可以区分它们。

现在，我们来学习函数调用。第1 个函数调用是pound(times)，times的值5被赋给n。因此， printf()函数打印了5个井号和1个换行符。第2个函数调用是pound(ch)。这里，ch是char类型，被初始化为!字符，在ASCII中ch的数值是33。但是pound()函数的参数类型是int，与char不匹配。程序开头的函数原型在这里发挥了作用。原型（prototype）即是函数的声明，描述了函数的返回值和参数。pound()函数的原型说明了两点:

该函数没有返回值（函数名前面有void关键字）；

该函数有一个int类型的参数。

该例中，函数原型告诉编译器pound()需要一个int类型的参数。相应地，当编译器执行到pound(ch)表达式时，会把参数ch自动转换成int类型。在我们的系统中，该参数从1字节的33变成4字节的33，所以现在33的类型满足函数的要求。与此类似，最后一次调用是pound(f)，使得float类型的变量被转换成合适的类型。

在ANSI C之前，C使用的是函数声明，而不是函数原型。函数声明只指明了函数名和返回类型，没有指明参数类型。为了向下兼容，C现在仍然允许这样的形式:

void pound(); /\* ANSI C乊前的函数声明 \*/

如果用这条函数声明代替pound.c程序中的函数原型会怎样？第 1 次函数调用，pound(times)没问题，因为times是int类型。第2次函数调用，pound(ch)也没问题，因为即使缺少函数原型，C也会把char和short类型自动升级为int类型。第3次函数调用，pound(f)会失败，因为缺少函数原型，float会被自动升级为 double，这没什么用。虽然程序仍然能运行，但是输出的内容不正确。在函数调用中显式使用强制类型转换，可以修复这个问题:

pound ((int)f); // 把f强制类型转换为正确的类型

注意，如果f的值太大，超过了int类型表示的范围，这样做也不行。

## 5.7 示例程序

程序清单5.16演示了本章介绍的几个概念，这个程序对某些人很有用。程序看起来很长，但是所有的计算都在程序的后面几行中。我们尽量使用大量的注释，让程序看上去清晰明了。请通读该程序，稍后我们会分析几处要点。

程序清单5.16 running.c程序

```c
// running.c -- A useful program for runners
#include <stdio.h>
const int S_PER_M = 60;          // 1分钟的秒数
const int S_PER_H = 3600;         // 1小时的分钟数
const double M_PER_K = 0.62137;    // 1公里的英里数
int main(void)
{
double distk, distm;   // 跑过的距离（分别以公里和英里为单位）
double rate;           // 平均速度（以英里/小时为单位）
int min, sec;        // 跑步用时（以分钟和秒为单位）
int time;               // 跑步用时（以秒为单位）
double mtime;            // 跑1英里需要的时间，以秒为单位
int mmin, msec;       // 跑1英里需要的时间，以分钟和秒为单位
printf("This program converts your time for a metric race\n");
```

printf("to a time for running a mile and to your average\n");

printf("speed in miles per hour.\n");

printf("Please enter, in kilometers, the distance run.\n");

scanf("%lf", &distk); // %lf表示读取一个double类型的值

printf("Next enter the time in minutes and seconds.\n");

printf("Begin by entering the minutes.\n");

scanf("%d", &min);

printf("Now enter the seconds.\n");

scanf("%d", &sec);

time = S\_PER\_M \* min + sec; // 把时间转换成秒

distm = M\_PER\_K \* distk; // 把公里转换成英里

rate = distm / time \* S\_PER\_H; // 英里/秒×秒/小时 = 英里/小时

mtime = (double) time / distm; // 时间/距离 = 跑1英里所用的时间

mmin = (int) mtime / S\_PER\_M; // 求出分钟数

msec = (int) mtime % S\_PER\_M; // 求出剩余的秒数

printf("You ran %1.2f km (%1.2f miles) in %d min, %d sec.\n",

distk, distm, min, sec);

printf("That pace corresponds to running a mile in %d min, ",

```txt
mmin);

printf("%d sec.\nYour average speed was %1.2f mph.\n", msec,
rate);

return 0;

}
```

程序清单5.16使用了min\_sec程序（程序清单5.9）中的方法把时间转换成分钟和秒，除此之外还使用了类型转换。为什么要进行类型转换？因为程序在秒转换成分钟的部分需要整型参数，但是在公里转换成英里的部分需要浮点运算。我们使用强制类型转换运算符进行了显式转换。

实际上，我们曾经利用自动类型转换编写这个程序，即使用int类型的mtime来强制时间计算转换成整数形式。但是，在测试的11个系统中，这个版本的程序在1个系统上无法运行，这是由于编译器（版本比较老）没有遵循C规则。而使用强制类型转换就没有问题。对读者而言，强制类型转换强调了转换类型的意图，对编译器而言也是如此。

下面是程序清单5.16的输出示例:

```txt
This program converts your time for a metric race to a time for running a mile and to your average speed in miles per hour.
Please enter, in kilometers, the distance run.
```

## 10.0

Next enter the time in minutes and seconds.

Begin by entering the minutes.

**36**

Now enter the seconds.

**23**

You ran 10.00 km (6.21 miles) in 36 min, 23 sec.

That pace corresponds to running a mile in 5 min, 51 sec.

Your average speed was 10.25 mph.

## 5.8 关键概念

C 通过运算符提供多种操作。每个运算符的特性包括运算对象的数量、优先级和结合律。当两个运算符共享一个运算对象时，优先级和结合律决定了先进行哪项运算。每个 C表达式都有一个值。如果不了解运算符的优先级和结合律，写出的表达式可能不合法或者表达式的值与预期不符。这会影响你成为一名优秀的程序员。

虽然C允许编写混合数值类型的表达式，但是算术运算要求运算对象都是相同的类型。因此，C会进行自动类型转换。尽管如此，不要养成依赖自动类型转换的习惯，应该显式选择合适的类型或使用强制类型转换。这样，就不用担心出现不必要的自动类型转换。

## 5.9 本章小结

C 语言有许多运算符，如本章讨论的赋值运算符和算术运算符。一般而言，运算符需要一个或多个运算对象才能完成运算生成一个值。只需要一个运算对象的运算符（如负号和 sizeof）称为一元运算符，需要两个运算对象的运算符（如加法运算符和乘法运算符）称为二元运算符。

表达式由运算符和运算对象组成。在C语言中，每个表达式都有一个值，包括赋值表达式和比较表达式。运算符优先级规则决定了表达式中各项的求值顺序。当两个运算符共享一个运算对象时，先进行优先级高的运算。如果运算符的优先级相等，由结合律（从左往右或从右往左）决定求值顺序。

大部分语句都以分号结尾。最常用的语句是表达式语句。用花括号括起来的一条或多条语句构成了复合语句（或称为块）。while语句是一种迭代语句，只要测试条件为真，就重复执行循环体中的语句。

在C语言中，许多类型转换都是自动进行的。当char和short类型出现在表达式里或作为函数的参数（函数原型除外）时，都会被升级为int类型；float类型在函数参数中时，会被升级为double类型。在K&R C（不是ANSI C）下，表达式中的float也会被升级为double类型。当把一种类型的值赋给另一种类型的变量时，值将被转换成与变量的类型相同。当把较大类型转换成较小类型时（如，long转换成short，或 double 转换成 float），可能会丢失数据。根据本章介绍的规则，在混合类型的运算中，较小类型会被转换成较大类型。

定义带一个参数的函数时，便在函数定义中声明了一个变量，或称为形式参数。然后，在函数调用中传入的值会被赋给这个变量。这样，在函数中就可以使用该值了。

## 5.10 复习题

复习题的参考答案在附录A中。

1.假设所有变量的类型都是int，下列各项变量的值是多少:

$$
\mathrm{a.x} = (2 + 3) * 6;
$$

$$
\mathrm{b.x} = (1 2 + 6) / 2 * 3;
$$

$$
\mathrm{c.y} = \mathrm{x} = (2 + 3) / 4;
$$

$$
\mathrm{d.y} = 3 + 2 ^ {*} (\mathrm{x} = 7 / 2);
$$

2.假设所有变量的类型都是int，下列各项变量的值是多少:

$$
\mathrm{a.x} = (\mathrm{int}) 3. 8 + 3. 3;
$$

$$
\mathrm{b.x} = (2 + 3) * 1 0. 5;
$$

$$
\mathrm{c.x} = 3 / 5 * 2 2. 0;
$$

$$
\mathrm{d.x} = 2 2. 0 * 3 / 5;
$$

3.对下列各表达式求值:

$$
\mathrm{a}. 3 0. 0 / 4. 0 * 5. 0;
$$

$$
\mathrm{b}. 3 0. 0 / (4. 0 * 5. 0);
$$

$$
\mathrm{c}. 3 0 / 4 * 5;
$$

$$
\mathrm{d}. 3 0 * 5 / 4;
$$

$$
\mathrm{e}. 3 0 / 4. 0 * 5;
$$

$$
\mathrm{f}. 3 0 / 4 * 5. 0;
$$

4.请找出下面的程序中的错误。

```c
int main(void)
{
int i = 1,
float n;
printf("Watch out! Here come a bunch of fractions!\n");
while (i < 30)
n = 1/i;
printf("%f", n);
printf("That's all, folks!\n");
return;
}
```

5.这是程序清单 5.9 的另一个版本。从表面上看，该程序只使用了一条scanf()语句，比程序清单5.9简单。请找出不如原版之处。

```c
#include <stdio.h>

#define S_TO_M 60

int main(void)

{

int sec, min, left;
```

```c
printf("This program converts seconds to minutes and ");
printf("seconds.\n");
printf("Just enter the number of seconds.\n");
printf("Enter 0 to end the program.\n");
while (sec > 0) {
scanf("%d", &sec);
min = sec/S_TO_M;
left = sec % S_TO_M;
printf("%d sec is %d min, %d sec. \n", sec, min, left);
printf("Next input?\n");
}
printf("Bye!\n");
return 0;
}
```

6.下面的程序将打印出什么内容？

```c
#include <stdio.h>

#define FORMAT "%s! C is cool!\n"

int main(void)

{
```

```c
int num = 10;

printf(FORMAT,FORMAT);

printf("%d\n", ++num);

printf("%d\n", num++);
printf("%d\n", num--);

printf("%d\n", num);

return 0;

}
```

7.下面的程序将打印出什么内容？

```c
#include <stdio.h>

int main(void)
{
char c1, c2;
int diff;

float num;

c1 = 'S';

c2 = 'O';

diff = c1 - c2;

num = diff;
```

```txt
printf("%c%c%c:%d %3.2f\n", c1, c2, c1, diff, num);
return 0;
}
```

8.下面的程序将打印出什么内容？

```c
#include <stdio.h>

#define TEN 10

int main(void)

{

int n = 0;

while (n++ < TEN)

printf("%5d", n);

printf("\n");

return 0;

}
```

9.修改上一个程序，使其可以打印字母a～g。

10.假设下面是完整程序中的一部分，它们分别打印什么？

```txt
a.

int x = 0;

while (++x < 3)
```

```lisp
printf("%4d", x);
```

b.

```txt
int x = 100;
```

```txt
while (x++ < 103)
```

```txt
printf("%4d\n",x);
```

```txt
printf("%4d\n",x);
```

c.

```javascript
char ch = 's';
```

```txt
while (ch < 'w')
```

{

```txt
printf("%c", ch);
```

```txt
ch++;
```

}

```javascript
printf("%c\n",ch);
```

11.下面的程序会打印出什么？

```c
#define MESG "COMPUTER BYTES DOG"
```

```c
#include <stdio.h>
```

```txt
int main(void)
```

{

```txt
int n = 0;

while ( n < 5 )

printf("%s\n", MESG);

n++;

printf("That's all.\n");

return 0;

}
```

12.分别编写一条语句，完成下列各任务（或者说，使其具有以下副作用）:

a.将变量x的值增加10
b.将变量x的值增加1
c.将a与b之和的两倍赋给c
d.将a与b的两倍之和赋给c

13.分别编写一条语句，完成下列各任务:

a.将变量x的值减少1
b.将n除以k的余数赋给m
c.q除以b减去a，并将结果赋给p
d.a与b之和除以c与d的乘积，并将结果赋给x

## 5.11 编程练习

1.编写一个程序，把用分钟表示的时间转换成用小时和分钟表示的时间。使用#define或const创建一个表示60的符号常量或const变量。通过while循环让用户重复输入值，直到用户输入小于或等于0的值才停止循环。
2.编写一个程序，提示用户输入一个整数，然后打印从该数到比该数大10的所有整数（例如，用户输入5，则打印5～15的所有整数，包括5和15）。要求打印的各值之间用一个空格、制表符或换行符分开。
3.编写一个程序，提示用户输入天数，然后将其转换成周数和天数。例如，用户输入18，则转换成2周4天。以下面的格式显示结果:

18 days are 2 weeks, 4 days.

通过while循环让用户重复输入天数，当用户输入一个非正值时（如0或-20），循环结束。
4.编写一个程序，提示用户输入一个身高（单位:厘米），并分别以厘米和英寸为单位显示该值，允许有小数部分。程序应该能让用户重复输入身高，直到用户输入一个非正值。其输出示例如下:

Enter a height in centimeters: 182

182.0 cm = 5 feet, 11.7 inches

Enter a height in centimeters (<=0 to quit): 168.7

168.0 cm = 5 feet, 6.4 inches

Enter a height in centimeters (<=0 to quit): 0

5.修改程序addemup.c（程序清单5.13），你可以认为addemup.c是计算20天里赚多少钱的程序（假设第1天赚\$1、第2天赚\$2、第3天赚\$3，以此类推）。修改程序，使其可以与用户交互，根据用户输入的数进行计算（即，用读入的一个变量来代替20）。

6.修改编程练习5的程序，使其能计算整数的平方和（可以认为第1天赚\$1、第2天赚\$4、第3天赚\$9，以此类推，这看起来很不错）。C没有平方函数，但是可以用n \* n来表示n的平方。
7.编写一个程序，提示用户输入一个double类型的数，并打印该数的立方值。自己设计一个函数计算并打印立方值。main()函数要把用户输入的值传递给该函数。
8.编写一个程序，显示求模运算的结果。把用户输入的第1个整数作为求模运算符的第2个运算对象，该数在运算过程中保持不变。用户后面输入的数是第1个运算对象。当用户输入一个非正值时，程序结束。其输出示例如下:

This program computes moduli.

Enter an integer to serve as the second operand: 256

Now enter the first operand: 438

438 % 256 is 182

Enter next number for first operand (<= 0 to quit): 1234567

1234567 % 256 is 135

Enter next number for first operand (<= 0 to quit): 0

Done

9.编写一个程序，要求用户输入一个华氏温度。程序应读取double类型的值作为温度值，并把该值作为参数传递给一个用户自定义的函数

Temperatures()。该函数计算摄氏温度和开氏温度，并以小数点后面两位数字的精度显示3种温度。要使用不同的温标来表示这3个温度值。下面是华氏温度转摄氏温度的公式:

$$
\text {摄氏温度} = 5. 0 / 9. 0 * (\text {华氏温度} - 3 2. 0)
$$

开氏温标常用于科学研究，0表示绝对零，代表最低的温度。下面是摄氏温度转开氏温度的公式:

$$
\text {开氏温度} = \text {摄氏温度} + 2 7 3. 1 6
$$

Temperatures()函数中用const创建温度转换中使用的变量。在main()函数中使用一个循环让用户重复输入温度，当用户输入 q 或其他非数字时，循环结束。scanf()函数返回读取数据的数量，所以如果读取数字则返回1，如果读取q则不返回1。可以使用==运算符将scanf()的返回值和1作比较，测试两值是否相等。

[1].根据C标准，声明不是语句。这与C++有所不同。——译者注
[2].在C语言中，赋值和函数调用都是表达式。没有所谓的“赋值语句”和“函数调用语句”，这些语句实际上都是表达式语句。本书将“assignment statement”均译为“赋值表达式语句”，以提醒读者注意。——译者注

# 第6章 C控制语句:循环

本章介绍以下内容:

关键字:for、while、do while

运算符:<、>、>=、<=、!=、==、+=、\*=、-=、/=、%=

函数:fabs()

C语言有3种循环:for、while、do while

使用关系运算符构建控制循环的表达式

其他运算符

循环常用的数组

编写有返回值的函数

大多数人都希望自己是体格强健、天资聪颖、多才多艺的能人。虽然有时事与愿违，但至少我们用 C能写出这样的程序。诀窍是控制程序流。对于计算机科学（是研究计算机，不是用计算机做研究）而言，一门语言应该提供以下3种形式的程序流:

执行语句序列；

如果满足某些条件就重复执行语句序列（循环

通过测试选择执行哪一个语句序列（分支）。

读者对第一种形式应该很熟悉，前面学过的程序中大部分都是由语句序列组成。while循环属于第二种形式。本章将详细讲解while循环和其他两种循环:for和do while。第三种形式用于在不同的执行方案之间进行选择，让程序更“智能”，且极大地提高了计算机的用途。不过，要等到下一章才介绍这部分的内容。本章还将介绍数组，可以把新学的知识应用在数组上。另外，本章还将继续介绍函数的相关内容。首先，我们从while循环开始学习。

## 6.1 再探while循环

经过上一章的学习，读者已经熟悉了 while 循环。这里，我们用一个程序来回顾一下，程序清单 6.1根据用户从键盘输入的整数进行求和。程序利用了scanf()的返回值来结束循环。

程序清单6.1 summing.c程序

```c
/* summing.c -- 根据用户键入的整数求和 */
#include <stdio.h>

int main(void)
{
long num;
long sum = 0L;          /* 把sum初始化为0 */
int status;
printf("Please enter an integer to be summed ");
printf("(q to quit): ");
status = scanf("%ld", &num);
while (status == 1)    /*== 的意思是“等于” */
{
sum = sum + num;
printf("Please enter next integer (q to quit): ");
```

```txt
status = scanf("%ld", &num);

}
printf("Those integers sum to %ld.\n", sum);
return 0;
}
```

该程序使用long类型以储存更大的整数。尽管C编译器会把0自动转换为合适的类型，但是为了保持程序的一致性，我们把sum初始化为0L（long类型的0），而不是0（int类型的0）。

该程序的运行示例如下:

```txt
Please enter an integer to be summed (q to quit): 44
Please enter next integer (q to quit): 33
Please enter next integer (q to quit): 88
Please enter next integer (q to quit): 121
Please enter next integer (q to quit): q
Those integers sum to 286.
```

## 6.1.1 程序注释

先看while循环，该循环的测试条件是如下表达式:

```python
status == 1
```

==运算符是C的相等运算符（equality operator），该表达式判断status是否等于1。不要把status== 1与status = 1混淆，后者是把1赋给status。根据测试条件status == 1，只要status等于1，循环就会重复。每次循环，num的当前值都被加到sum上，这样sum的值始终是当前整数之和。当status的值不为1时，循环结束。然后程序打印sum的最终值。

要让程序正常运行，每次循环都要获取num的一个新值，并重置status。程序利用scanf()的两个不同的特性来完成。首先，使用scanf()读取num的一个新值；然后，检查scanf()的返回值判断是否成功获取值。第4章中介绍过，scanf()返回成功读取项的数量。如果scanf()成功读取一个整数，就把该数存入num并返回1，随后返回值将被赋给status（注意，用户输入的值储存在num中，不是status中）。这样做同时更新了num和status的值，while循环进入下一次迭代。如果用户输入的不是数字（如， q），scanf()会读取失败并返回0。此时，status的值就是0，循环结束。因为输入的字符q不是数字，所以它会被放回输入队列中（实际上，不仅仅是 $\mathbf { q } ,$ ，任何非数值的数据都会导致循环终止，但是提示用户输入q退出程序比提示用户输入一个非数字字符要简单）。

如果 scanf()在转换值之前出了问题（例如，检测到文件结尾或遇到硬件问题），会返回一个特殊值EOF（其值通常被定义为-1）。这个值也会引起循环终止。

如何告诉循环何时停止？该程序利用 scanf()的双重特性避免了在循环中交互输入时的这个棘手的问题。例如，假设scanf()没有返回值，那么每次循环只会改变num的值。虽然可以使用num的值来结束循环，比如把num > 0（num大于0）或num ！= 0（num不等于0）作为测试条件，但是这样用户就不能输入某些值，如-3或0。也可以在循环中添加代码，例如每次循环时询问用户“是否继续循环？&lt;y/n&gt;”，然后判断用户是否输入 $\cdot y$ 。这个方法有些笨拙，而且还减慢了输入的速度。使用scanf()的返回值，轻松地避免了这些问题。

现在，我们来看看该程序的结构。总结如下:

把sum初始化为0

提示用户输入数据

读取用户输入的数据

当输入的数据为整数时，

输入添加给sum，

提示用户进行输入，

然后读取下一个输入

输入完成后，打印sum的值

顺带一提，这叫作伪代码（pseudocode），是一种用简单的句子表示程序思路的方法，它与计算机语言的形式相对应。伪代码有助于设计程序的逻辑。确定程序的逻辑无误之后，再把伪代码翻译成实际的编程代码。使用伪代码的好处之一是，可以把注意力集中在程序的组织和逻辑上，不用在设计程序时还要分心如何用编程语言来表达自己的想法。例如，可以用缩进来代表一块代码，不用考虑C的语法要用花括号把这部分代码括起来。

总之，因为while循环是入口条件循环，程序在进入循环体之前必须获取输入的数据并检查status的值，所以在 while 前面要有一个 scanf()。要让循环继续执行，在循环内需要一个读取数据的语句，这样程序才能获取下一个status的值，所以在while循环末尾还要有一个scanf()，它为下一次迭代做好了准备。可以把下面的伪代码作为while循环的标准格式:

获得第1个用于测试的值

当测试为真时

处理值

获取下一个值

## 6.1.2 C风格读取循环

根据伪代码的设计思路，程序清单6.1可以用Pascal、BASIC或FORTRAN来编写。但是C更为简洁，下面的代码:

```c
status = scanf("%ld", &num);

while (status == 1)
{
/* 循环行为 */
status = scanf("%ld", &num);
}
```

可以用这些代码替换:

```txt
while (scanf("%ld", &num) == 1)
{
/*循环行为*/
}
```

第二种形式同时使用scanf()的两种不同的特性。首先，如果函数调用成功，scanf()会把一个值存入num。然后，利用scanf()的返回值（0或1，不是num的值）控制while循环。因为每次迭代都会判断循环的条件，所以每次迭代都要调用scanf()读取新的num值来做判断。换句话说，C的语法特性让你可以用下面的精简版本替换标准版本:

当获取值和判断值都成功

处理该值

接下来，我们正式地学习while语句。