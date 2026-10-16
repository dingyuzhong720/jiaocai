原因是> mywords在输入之前已导致原mywords的长度被截断为0。

总之，在UNIX、Linux或Windows/DOS系统中使用两个重定向运算符（<和>）时，要遵循以下原则。

重定向运算符连接一个可执行程序（包括标准操作系统命令）和一个数据文件，不能用于连接一个数据文件和另一个数据文件，也不能用于连接一个程序和另一个程序。

使用重定向运算符不能读取多个文件的输入，也不能把输出定向至多个文件。

通常，文件名和运算符之间的空格不是必须的，除非是偶尔在UNIX shell、Linux shell或Windows命令行提示模式中使用的有特殊含义的字符。例如，我们用过的echo\_eof<words。

以上介绍的都是正确的例子，下面来看一下错误的例子，addup和count是两个可执行程序，fish和beets是两个文本文件:

fish > beets ←违反第1条规则

addup < count ←违反第1条规则

addup < fish < beets ←违反第2条规则

count > beets fish ←违反第2条规则

UNIX、Linux或Windows/DOS 还有>>运算符，该运算符可以把数据添加到现有文件的末尾，而 | 运算符能把一个文件的输出连接到另一个文件的输入。欲了解所有相关运算符的内容，请参阅 UNIX 的相关书籍，如UNIX Primer Plus，Third Edition（Wilson、Pierce和Wessler合著）。

## 4.注释

重定位让你能使用键盘输入程序文件。要完成这一任务，程序要测试文件的末尾。例如，第 7 章演示的统计单词程序（程序清单7.7），计算单词个数直至遇到第1个|字符。把ch的char类型改成int类型，把循环测试中的|替换成EOF，便可用该程序来计算文本文件中的单词量。

重定向是一个命令行概念，因为我们要在命令行输入特殊的符号发出指令。如果不使用命令行环境，也可以使用重定向。首先，一些集成开发环境提供了菜单选项，让用户指定重定向。其次，对于 Windows系统，可以打开命令提示窗口，并在命令行运行可执行文件。Microsoft Visual Studio的默认设置是把可执行文件放在项目文件夹的子文件夹，称为Debug。文件名和项目名的基本名相同，文件名的扩展名为.exe。默认情况下，Xcode在给项目命名后才能命名可执行文件，并将其放在Debug文件夹中。在UNIX系统中，可以通过Terminal工具运行可执行文件。从使用上看，Terminal比命令行编译器（GCC或Clang）简单。

如果用不了重定向，可以用程序直接打开文件。程序清单8.3演示了一个注释较少的示例。我们学到第13章时再详细讲解。待读取的文件应该与可执行文件位于同一目录。

程序清单**8.3 file\_eof.c**程序

```c
// file_eof.c --打开一个文件并显示该文件
#include <stdio.h>
#include <stdlib.h>          // 为了使用exit()
int main()
{
int ch;

FILE * fp;
```

```c
char fname[50];                      // 储存文件名
printf("Enter the name of the file: ");
scanf("%s", fname);
fp = fopen(fname, "r");      // 打开待读取文件
if (fp == NULL)                  // 如果失败
{
printf("Failed to open file. Bye\n");
exit(1);                          // 退出程序
}
// getc(fp)从打开的文件中获取一个字符
while ((ch = getc(fp)) != EOF)
putchar(ch);
fclose(fp);                     // 关闭文件
return 0;
}
```

小结:如何重定向输入和输出

绝大部分C系统都可以使用重定向，可以通过操作系统重定向所有程序，或只在C编译器允许的情况下重定向C程序。假设prog是可执行程序名，file1和file2是文件名。

把输出重定向至文件:>

```txt
prog>file1
```

把输入重定向至文件:<

```txt
prog <file2
```

组合重定向:

```txt
prog <file2 >file1
```

```txt
prog >file1 <file2
```

这两种形式都是把file2作为输入、file1作为输出。

留白:

一些系统要求重定向运算符左侧有一个空格，右侧没有空格。而其他系统（如，UNIX）允许在重定位运算符两侧有空格或没有空格。

## 8.5 创建更友好的用户界面

大部分人偶尔会写一些中看不中用的程序。还好，C提供了大量工具让输入更顺畅，处理过程更顺利。不过，学习这些工具会导致新的问题。本节的目标是，指导读者解决这些问题并创建更友好的用户界面，让交互数据输入更方便，减少错误输入的影响。

## 8.5.1 使用缓冲输入

缓冲输入用起来比较方便，因为在把输入发送给程序之前，用户可以编辑输入。但是，在使用输入的字符时，它也会给程序员带来麻烦。前面示例中看到的问题是，缓冲输入要求用户按下Enter键发送输入。这一动作也传送了换行符，程序必须妥善处理这个麻烦的换行符。我们以一个猜谜程序为例。用户选择一个数字，程序猜用户选中的数字是多少。该程序使用的方法单调乏味，先不要在意算法，我们关注的重点在输入和输出。查看程序清单8.4，这是猜谜程序的最初版本，后面我们会改进。

程序清单8.4 guess.c程序

```c
/* guess.c -- 一个拖沓且错误的猜数字程序 */

#include <stdio.h>

int main(void)

{

int guess = 1;

printf("Pick an integer from 1 to 100. I will try to guess );

printf("it.\nRespond with a y if my guess is right and with");
```

```c
printf("\nan n if it is wrong.\n");
printf("Uh...is your number %d?\n", guess);
while (getchar() != 'y')      /* 获取响应，与 y 做对比 */
printf("Well, then, is it %d?\n", ++guess);
printf("I knew I could do it!\n");
return 0;
}
```

下面是程序的运行示例:

Pick an integer from 1 to 100. I will try to guess it.

Respond with a y if my guess is right and with an n if it is wrong.

Uh...is your number 1?

## n

Well, then, is it 2?

Well, then, is it 3?

## n

Well, then, is it 4?

Well, then, is it 5?

## y

I knew I could do it!

撇开这个程序糟糕的算法不谈，我们先选择一个数字。注意，每次输入n 时，程序打印了两条消息。这是由于程序读取n作为用户否定了数字1，然后还读取了一个换行符作为用户否定了数字2。

一种解决方案是，使用while循环丢弃输入行最后剩余的内容，包括换行符。这种方法的优点是，能把no和no way这样的响应视为简单的n。程序清单8.4的版本会把no当作两个响应。下面用循环修正

char response;这个问题:

```txt
while (getchar() != 'y')    /* 获取响应，与 y 做对比*/
{
printf("Well, then, is it %d?\n", ++guess);
while (getchar() != '\n')
continue;          /* 跳过剩余的输入行 */
}
```

使用以上循环后，该程序的输出示例如下:

```txt
Pick an integer from 1 to 100. I will try to guess it.
Respond with a y if my guess is right and with
an n if it is wrong.
Uh...is your number 1?
n
```

Well, then, is it 2?

**no**

Well, then, is it 3?

**no sir**

Well, then, is it 4?

**forget it**

Well, then, is it 5?

y

I knew I could do it!

这的确是解决了换行符的问题。但是，该程序还是会把f被视为n。我们用if语句筛选其他响应。首先，添加一个char类型的变量储存响应:

修改后的循环如下:

while ((response = getchar()) != 'y') /\* 获取响应 \*/

if (response == 'n')

printf("Well, then, is it %d?\n", ++guess);

else

printf("Sorry, I understand only y or n.\n");

while (getchar() != '\n')

continue; /\* 跳过剩余的输入行 \*/

}

现在，程序的运行示例如下:

Pick an integer from 1 to 100. I will try to guess it.

Respond with a y if my guess is right and with

an n if it is wrong.

Uh...is your number 1?

n

Well, then, is it 2?

**no**

Well, then, is it 3?

**no sir**

Well, then, is it 4?

**forget it**

Sorry, I understand only y or n.

n

Well, then, is it 5?

y

I knew I could do it!

在编写交互式程序时，应该事先预料到用户可能会输入错误，然后设计程序处理用户的错误输入。在用户出错时通知用户再次输入。

当然，无论你的提示写得多么清楚，总会有人误解，然后抱怨这个程序设计得多么糟糕。

## 8.5.2 混合数值和字符输入

假设程序要求用 getchar()处理字符输入，用 scanf()处理数值输入，这两个函数都能很好地完成任务，但是不能把它们混用。因为 getchar()读取每个字符，包括空格、制表符和换行符；而 scanf()在读取数字时则会跳过空格、制表符和换行符。

我们通过程序清单8.5来解释这种情况导致的问题。该程序读入一个字符和两个数字，然后根据输入的两个数字指定的行数和列数打印该字符。

程序清单8.5 showchar1.c程序

```c
/* showchar1.c -- 有较大 I/O 问题的程序 */
#include <stdio.h>
void display(char cr, int lines, int width);
int main(void)
{
int ch;                 /* 待打印字符 */
int rows, cols;       /* 行数和列数 */
printf("Enter a character and two integers:\n");
while ((ch = getchar()) != '\n')
```

```txt
{
scanf("%d %d", &rows, &cols);
display(ch, rows, cols);
printf("Enter another character and two integers;\n");
printf("Enter a newline to quit.\n");
}
printf("Bye.\n");
return 0;
}
void display(char cr, int lines, int width)
{
int row, col;
for (row = 1; row <= lines; row++)
{
for (col = 1; col <= width; col++)
putchar(cr);
putchar('\n');/* 结束一行并开始新的一行 */
}
}
```

注意，该程序以 int 类型读取字符（这样做可以检测 EOF），但是却以char 类型把字符传递给display()函数。因为char比int小，一些编译器会给出类型转换的警告。可以忽略这些警告，或者用下面的强制类型转换消除警告:

display(char(ch), rows, cols);

在该程序中，main()负责获取数据，display()函数负责打印数据。下面是该程序的一个运行示例，看看有什么问题:

Enter a character and two integers:

**c 2 3**

ccc

ccc

Enter another character and two integers;

Enter a newline to quit.

Bye.

该程序开始时运行良好。你输入c 2 3，程序打印c字符2行3列。然后，程序提示输入第2组数据，还没等你输入数据程序就退出了！这是什么情况？又是换行符在捣乱，这次是输入行中紧跟在 3 后面的换行符。scanf()函数把这个换行符留在输入队列中。和 scanf()不同，getchar()不会跳过换行符，所以在进入下一轮迭代时，你还没来得及输入字符，它就读取了换行符，然后将其赋给ch。而ch是换行符正式终止循环的条件。

要解决这个问题，程序要跳过一轮输入结束与下一轮输入开始之间的所有换行符或空格。另外，如果该程序不在getchar()测试时，而在scanf()阶段终止程序会更好。修改后的版本如程序清单8.6所示。

程序清单8.6 showchar2.c程序

```c
/* showchar2.c -- 按指定的行列打印字符 */
#include <stdio.h>
void display(char cr, int lines, int width);
int main(void)
{
int ch; /* 待打印字符*/
int rows, cols; /* 行数和列数 */
printf("Enter a character and two integers:\n");
while ((ch = getchar()) != '\n')
{
if (scanf("%d %d", &rows, &cols) != 2)
break;
display(ch, rows, cols);
while (getchar() != '\n')
continue;
printf("Enter another character and two integers;\n");
printf("Enter a newline to quit.\n");
}
```

```c
printf("Bye.\n");

return 0;

}

void display(char cr, int lines, int width)
{

int row, col;

for (row = 1; row <= lines; row++)

{

for (col = 1; col <= width; col++)

putchar(cr);

putchar('\n'); /* 结束一行并开始新的一行 */
}

}
```

while循环实现了丢弃scanf()输入后面所有字符（包括换行符）的功能，为循环的下一轮读取做好了准备。该程序的运行示例如下:

```sql
Enter a character and two integers:
c 1 2
cc
Enter another character and two integers;
```

Enter a newline to quit.

**! 3 6**

!!!!!!

!!!!!!

!!!!!!

Enter another character and two integers;

Enter a newline to quit.

Bye.

在if语句中使用一个break语句，可以在scanf()的返回值不等于2时终止程序，即如果一个或两个输入值不是整数或者遇到文件结尾就终止程序。

## 8.6 输入验证

在实际应用中，用户不一定会按照程序的指令行事。用户的输入和程序期望的输入不匹配时常发生，这会导致程序运行失败。作为程序员，除了完成编程的本职工作，还要事先预料一些可能的输入错误，这样才能编写出能检测并处理这些问题的程序。

例如，假设你编写了一个处理非负数整数的循环，但是用户很可能输入一个负数。你可以使用关系表达式来排除这种情况:

```txt
long n;
scanf("%ld", &n);      // 获取第1个值
while (n >= 0)          // 检测不在范围内的值
{
// 处理n
scanf("%ld", &n);  // 获取下一个值
}
```

另一类潜在的陷阱是，用户可能输入错误类型的值，如字符 q。排除这种情况的一种方法是，检查scanf()的返回值。回忆一下，scanf()返回成功读取项的个数。因此，下面的表达式当且仅当用户输入一个整数时才为真:

```scala
scanf("%ld", &n) == 1
```

结合上面的while循环，可改进为:

```txt
long n;
while (scanf("%ld", &n) == 1 && n >= 0)
```

```json
{
//处理n
}
```

while循环条件可以描述为“当输入是一个整数且该整数为正时”。

对于最后的例子，当用户输入错误类型的值时，程序结束。然而，也可以让程序友好些，提示用户再次输入正确类型的值。在这种情况下，要处理有问题的输入。如果scanf()没有成功读取，就会将其留在输入队列中。这里要明确，输入实际上是字符流。可以使用getchar()函数逐字符地读取输入，甚至可以把这些想法都结合在一个函数中，如下所示:

```txt
long get_long(void)
{
long input;
char ch;
while (scanf("%ld", &input) != 1)
{
while ((ch = getchar()) != '\n')
putchar(ch); // 处理错误的输入
printf(" is not an integer.\nPlease enter an ");
printf("integer value, such as 25, -178, or 3: ");
}
```

```txt
return   input;
}
```

该函数要把一个int类型的值读入变量input中。如果读取失败，函数则进入外层while循环体。然后内层循环逐字符地读取错误的输入。注意，该函数丢弃该输入行的所有剩余内容。还有一个方法是，只丢弃下一个字符或单词，然后该函数提示用户再次输入。外层循环重复运行，直到用户成功输入整数，此时scanf()的返回值为1。

在用户输入整数后，程序可以检查该值是否有效。考虑一个例子，要求用户输入一个上限和一个下限来定义值的范围。在该例中，你可能希望程序检查第1个值是否大于第2个值（通常假设第1个值是较小的那个值），除此之外还要检查这些值是否在允许的范围内。例如，当前的档案查找一般不会接受 1958 年以前和2014年以后的查询任务。这个限制可以在一个函数中实现。

假设程序中包含了stdbool.h 头文件。如果当前系统不允许使用\_Bool，把bool替换成int，把true 替换成 1，把 false 替换成 0 即可。注意，如果输入无效，该函数返回 true，所以函数名为bad\_limits():

```c
bool bad_limits(long begin, long end,long low, long high)
{
bool not_good = false;
if (begin > end)
{
printf("%ld isn't smaller than %ld.\n", begin, end);
not_good = true;
```

```c
}
if (begin < low || end < low)
{
printf("Values must be %ld or greater.\n", low);
not_good = true;
}
if (begin > high || end > high)
{
printf("Values must be %ld or less.\n", high);
not_good = true;
}
return not_good;
}
```

程序清单8.7使用了上面的两个函数为一个进行算术运算的函数提供整数，该函数计算特定范围内所有整数的平方和。程序限制了范围的上限是10000000，下限是-10000000。

程序清单**8.7 checking.c**程序

// checking.c -- 输入验证

```c
#include <stdio.h>

#include <stdbool.h>
```

// 验证输入是一个整数

long get\_long(void);

// 验证范围的上下限是否有效

bool bad\_limits(long begin, long end,

long low, long high);

// 计算a～b之间的整数平方和

double sum\_squares(long a, long b);

int main(void)

{

const long MIN = -10000000L; // 范围的下限

const long MAX = +10000000L; // 范围的上限

long start; // 用户指定的范围最小值

long stop; // 用户指定的范围最大值

double answer;

printf("This program computes the sum of the squares of "

"integers in a range.\nThe lower bound should not "

"be less than -10000000 and\nthe upper bound "

"should not be more than +10000000.\nEnter the "

"limits (enter 0 for both limits to quit):\n"

```c
"lower limit: ");

start = get_long();

printf("upper limit: ");

stop = get_long();

while (start != 0 || stop != 0)
{
if (bad_limits(start, stop, MIN, MAX))
printf("Please try again.\n");
else
{
answer = sum_squares(start, stop);
printf("The sum of the squares of the integers ");
printf("from %ld to %ld is %g\n",
start, stop, answer);
}
printf("Enter the limits (enter 0 for both "
"limits to quit):\n");
printf("lower limit: ");
start = get_long();
```

```c
printf("upper limit: ");
stop = get_long();
}
printf("Done.\n");
return 0;
}
long get_long(void)
{
long input;
char ch;
while (scanf("%ld", &input) != 1)
{
while ((ch = getchar()) != '\n')
putchar(ch);          // 处理错误输入
printf(" is not an integer.\nPlease enter an ");
printf("integer value, such as 25, -178, or 3: ");
}
return input;
}
```

```c
double sum_squares(long a, long b)
{
double total = 0;
long i;
for (i = a; i <= b; i++)
total += (double) i * (double) i;
return total;
}
bool bad_limits(long begin, long end,
long low, long high)
{
bool not_good = false;
if (begin > end)
{
printf("%ld isn't smaller than %ld.\n", begin, end);
not_good = true;
}
if (begin < low || end < low)
{
```

```c
printf("Values must be %ld or greater.\n", low);
not_good = true;
}
if (begin > high || end > high)
{
printf("Values must be %ld or less.\n", high);
not_good = true;
}
return not_good;
}
```

下面是该程序的输出示例:

This program computes the sum of the squares of integers in a range.

The lower bound should not be less than -10000000 and the upper bound should not be more than +10000000.

Enter the limits (enter 0 for both limits to quit):

lower limit: low

low is not an integer.

Please enter an integer value, such as 25, -178, or 3: 3

upper limit: a big number

a big number is not an integer.

Please enter an integer value, such as 25, -178, or 3: 12 The sum of the squares of the integers from 3 to 12 is 645

Enter the limits (enter 0 for both limits to quit):

lower limit: 80

upper limit: 10

80 isn't smaller than 10.

Please try again.

Enter the limits (enter 0 for both limits to quit):

lower limit: 0

upper limit: 0

Done.

## 8.6.1 分析程序

虽然checking.c程序的核心计算部分（sum\_squares()函数）很短，但是输入验证部分比以往程序示例要复杂。接下来分析其中的一些要素，先着重讨论程序的整体结构。

程序遵循模块化的编程思想，使用独立函数（模块）来验证输入和管理显示。程序越大，使用模块化编程就越重要。

main()函数管理程序流，为其他函数委派任务。它使用 get\_long()获取值、while 循环处理值、badlimits()函数检查值是否有效、sum\_squres()函数处理实际的计算:

```c
start = get_long();

printf("upper limit:"])

stop = get_long();

while (start != 0 || stop != 0)
{
if (bad_limits(start, stop, MIN, MAX))
printf("Please try again.\n");
else
{
answer = sum_squares(start, stop);
printf("The sum of the squares of the integers ");
printf("from %ld to %ld is %g\n", start, stop, answer);
}
printf("Enter the limits (enter 0 for both "
"limits to quit):\n");
printf("lower limit: ");
start = get_long();
```

```lisp
printf("upper  limit:  ");
stop  =  get_long();
}
```

## 8.6.2 输入流和数字

在编写处理错误输入的代码时（如程序清单8.7），应该很清楚C是如何处理输入的。考虑下面的输入:

## is 28 12.4

在我们眼中，这就像是一个由字符、整数和浮点数组成的字符串。但是对 C程序而言，这是一个字节流。第1个字节是字母i的字符编码，第2个字节是字母s的字符编码，第3个字节是空格字符的字符编码，第4个字节是数字2的字符编码，等等。所以，如果get\_long()函数处理这一行输入，第1个字符是非数字，那么整行输入都会被丢弃，包括其中的数字，因为这些数字只是该输入行中的其他字符:

```txt
while ((ch = getchar()) != '\n')
```

putchar(ch); // 处理错误的输入

虽然输入流由字符组成，但是也可以设置scanf()函数把它们转换成数值。例如，考虑下面的输入:

## 42

如果在scanf()函数中使用%c转换说明，它只会读取字符4并将其储存在char类型的变量中。如果使用%s转换说明，它会读取字符4和字符2这两个字符，并将其储存在字符数组中。如果使用%d转换说明，scanf()同样会读取两个字符，但是随后会计算出它们对应的整数值:4×10+2，即42，然后将表示该整数的二进制数储存在 int 类型的变量中。如果使用%f 转换说明，scanf()也会读取两个字符，计算出它们对应的数值42.0，用内部的浮点表示法表示该值，并将结果储存在float类型的变量中。

简而言之，输入由字符组成，但是scanf()可以把输入转换成整数值或浮点数值。使用转换说明（如%d或%f）限制了可接受输入的字符类型，而getchar()和使用%c的scanf()接受所有的字符。

## 8.7 菜单浏览

许多计算机程序都把菜单作为用户界面的一部分。菜单给用户提供方便的同时，却给程序员带来了一些麻烦。我们看看其中涉及了哪些问题。

菜单给用户提供了一份响应程序的选项。假设有下面一个例子:

Enter the letter of your choice:

a. advice

b. bell

c. count

q. quit

理想状态是，用户输入程序所列选项之一，然后程序根据用户所选项完成任务。作为一名程序员，自然希望这一过程能顺利进行。因此，第1个目标是:当用户遵循指令时程序顺利运行；第2个目标是:当用户没有遵循指令时，程序也能顺利运行。显而易见，要实现第 2 个目标难度较大，因为很难预料用户在使用程序时的所有错误情况。

现在的应用程序通常使用图形界面，可以点击按钮、查看对话框、触摸图标，而不是我们示例中的命令行模式。但是，两者的处理过程大致相同:给用户提供选项、检查并执行用户的响应、保护程序不受误操作的影响。除了界面不同，它们底层的程序结构也几乎相同。但是，使用图形界面更容易通过限制选项控制输入。

## 8.7.1 任务

我们来更具体地分析一个菜单程序需要执行哪些任务。它要获取用户的响应，根据响应选择要执行的动作。另外，程序应该提供返回菜单的选项。C 的 switch 语句是根据选项决定行为的好工具，用户的每个选择都可以对应一个特定的case标签。使用while语句可以实现重复访问菜单的功能。因此，我们写出以下伪代码:

获取选项

当选项不是'q'时

转至相应的选项并执行

获取下一个选项

## 8.7.2 使执行更顺利

当你决定实现这个程序时，就要开始考虑如何让程序顺利运行（顺利运行指的是，处理正确输入和错误输入时都能顺利运行）。例如，你能做的是让“获取选项”部分的代码筛选掉不合适的响应，只把正确的响应传入switch。这表明需要为输入过程提供一个只返回正确响应的函数。结合while循环和switch语句，其程序结构如下:

```c
#include <stdio.h>

char get_choice(void);

void count(void);

int main(void)
{
int choice;

while ((choice = get_choice()) != 'q')
{
switch (choice)
{
case 'a': printf("Buy low, sell high.\n");
```

```txt
break;

case 'b': putchar('\a'); /* ANSI */

break;

case 'c': count();

break;

default: printf("Program error!\n");

break;

}

}

return 0;

}
```

定义get\_choice()函数只能返回'a'、'b'、'c'和'q'。get\_choice()的用法和getchar()相同，两个函数都是获取一个值，并与终止值（该例中是'q'）作比较。我们尽量简化实际的菜单选项，以便读者把注意力集中在程序结构上。稍后再讨论 count()函数。default 语句可以方便调试。如果get\_choice()函数没能把返回值限制为菜单指定的几个选项值，default语句有助于发现问题所在。

get\_choice()函数

下面的伪代码是设计这个函数的一种方案:

显示选项

获取用户的响应

当响应不合适时

提示用户再次输入

获取用户的响应

下面是一个简单而笨拙的实现:

```txt
char    get_choice(void)
{
```

int ch;

```txt
printf("Enter the letter of your choice:\n");
```

```javascript
printf("a. advice b. bell\n");
```

```javascript
printf("c. count q. quit\n");
```

```javascript
ch = getchar();
```

```txt
while ((ch < 'a' || ch > 'c') && ch != 'q')
{
```

```lua
printf("Please respond with a, b, c, or q.\n");
```

```txt
ch = getchar();
}
```

```txt
return  ch;
}
```

缓冲输入依旧带来些麻烦，程序把用户每次按下 Return 键产生的换行