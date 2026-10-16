用圆括号把宏的参数和整个替换体括起来。这样能确保被括起来的部分在下面这样的表达式中正确地展开:

$$
\text { forks } = 2 * \text { MAX(guests } + 3, \text { last });
$$

用大写字母表示宏函数的名称。该惯例不如用大写字母表示宏常量应用广泛。但是，大写字母可以提醒程序员注意，宏可能产生的副作用。

如果打算使用宏来加快程序的运行速度，那么首先要确定使用宏和使用函数是否会导致较大差异。在程序中只使用一次的宏无法明显减少程序的运行时间。在嵌套循环中使用宏更有助于提高效率。许多系统提供程序分析器以帮助程序员压缩程序中最耗时的部分。

假设你开发了一些方便的宏函数，是否每写一个新程序都要重写这些宏？如果使用#include指令，就不用这样做了。

## 16.5 文件包含:#include

当预处理器发现#include 指令时，会查看后面的文件名并把文件的内容包含到当前文件中，即替换源文件中的#include指令。这相当于把被包含文件的全部内容输入到源文件#include指令所在的位置。#include指令有两种形式:

#include &lt;stdio.h&gt; ←文件名在尖括号中

#include "mystuff.h" ←文件名在双引号中

在 UNIX 系统中，尖括号告诉预处理器在标准系统目录中查找该文件。双引号告诉预处理器首先在当前目录中（或文件名中指定的其他目录）查找该文件，如果未找到再查找标准系统目录:

#include &lt;stdio.h&gt; ←查找系统目录

#include "hot.h" ←查找当前工作目录

#include "/usr/biff/p.h" ←查找/usr/biff目录

集成开发环境（IDE）也有标准路径或系统头文件的路径。许多集成开发环境提供菜单选项，指定用尖括号时的查找路径。在 UNIX 中，使用双引号意味着先查找本地目录，但是具体查找哪个目录取决于编译器的设定。有些编译器会搜索源代码文件所在的目录，有些编译器则搜索当前的工作目录，还有些搜索项目文件所在的目录。

ANSI C不为文件提供统一的目录模型，因为不同的计算机所用的系统不同。一般而言，命名文件的方法因系统而异，但是尖括号和双引号的规则与系统无关。

为什么要包含文件？因为编译器需要这些文件中的信息。例如，stdio.h文件中通常包含EOF、NULL、getchar()和 putchar()的定义。getchar()和putchar()被定义为宏函数。此外，该文件中还包含C的其他I/O函数。

C语言习惯用.h后缀表示头文件，这些文件包含需要放在程序顶部的信息。头文件经常包含一些预处理器指令。有些头文件（如stdio.h）由系统提供，当然你也可以创建自己的头文件。

包含一个大型头文件不一定显著增加程序的大小。在大部分情况下，头文件的内容是编译器生成最终代码时所需的信息，而不是添加到最终代码中的材料。

## 16.5.1 头文件示例

假设你开发了一个存放人名的结构，还编写了一些使用该结构的函数。可以把不同的声明放在头文件中。程序清单16.6演示了一个这样的例子。

程序清单16.6 names\_st.h头文件

```c
// names_st.h -- names_st 结构的头文件
// 常量
#include <string.h>
#define SLEN 32
// 结构声明
struct names_st
{
char first[SLEN];
char last[SLEN];
};
// 类型定义
```

typedef struct names\_st names;

// 函数原型

void get\_names(names \*);

void show\_names(const names \*);

char \* s\_gets(char \* st, int n);

该头文件包含了一些头文件中常见的内容:#define指令、结构声明、typedef和函数原型。注意，这些内容是编译器在创建可执行代码时所需的信息，而不是可执行代码。为简单起见，这个特殊的头文件过于简单。通常，应该用#ifndef和#define防止多重包含头文件。我们稍后介绍这些内容。

可执行代码通常在源代码文件中，而不是在头文件中。例如，程序清单16.7中有头文件中函数原型的定义。该程序包含了names\_st.h头文件，所以编译器知道names类型。

程序清单**16.7 name\_st.c**源文件

// names\_st.c -- 定义 names\_st.h中的函数

#include &lt;stdio.h&gt;

#include "names\_st.h" // 包含头文件

// 函数定义

void get\_names(names \* pn)

printf("Please enter your first name: ");

s\_gets(pn->first, SLEN);

```c
printf("Please enter your last name: ");
s_gets(pn->last, SLEN);
}
void show_names(const names * pn)
{
printf("%s %s", pn->first, pn->last);
}
char * s_gets(char * st, int n)
{
char * ret_val;
char * find;
ret_val = fgets(st, n, stdin);
if (ret_val)
{
find = strchr(st, '\n'); // 查找换行符
if (find) // 如果地址不是NULL,
*find = '\0'; // 在此处放置一个空字符
else
while (getchar() != '\n')
```

```txt
continue;          // 处理输入行中的剩余字符
}
return ret_val;
}
```

get\_names()函数通过s\_gets()函数调用了fgets()函数，避免了目标数组溢出。程序清单16.8使用了程序清单16.6的头文件和程序清单16.7的源文件。

程序清单16.8 useheader.c程序

```c
// useheader.c -- 使用 names_st 结构
#include <stdio.h>
#include "names_st.h"
// 记住要链接 names_st.c
int main(void)
{
names candidate;
get_names(&candidate);
printf("Let's welcome ");
show_names(&candidate);
printf(" to this program!\n");
return 0;
```

}

下面是该程序的输出:

Please enter your first name: Ian

Please enter your last name: Smersh

Let's welcome Ian Smersh to this program!

该程序要注意下面几点。

两个源代码文件都使用names\_st类型结构，所以它们都必须包含names\_st.h头文件。

必须编译和链接names\_st.c和useheader.c源代码文件。

声明和指令放在nems\_st.h头文件中，函数定义放在names\_st.c源代码文件中。

## 16.5.2 使用头文件

浏览任何一个标准头文件都可以了解头文件的基本信息。头文件中最常用的形式如下。

明示常量—— 例如，stdio.h中定义的EOF、NULL和BUFSIZE（标准I/O缓冲区大小）。

宏函数——例如，getc(stdin)通常用getchar()定义，而getc()经常用于定义较复杂的宏，头文件ctype.h通常包含ctype系列函数的宏定义。

函数声明——例如，string.h头文件（一些旧的系统中是strings.h）包含字符串函数系列的函数声明。在ANSI C和后面的标准中，函数声明都是函数原型形式。

结构模版定义——标准I/O函数使用FILE结构，该结构中包含了文件和

与文件缓冲区相关的信息。FILE结构在头文件stdio.h中。

类型定义——标准 I/O 函数使用指向 FILE 的指针作为参数。通常，stdio.h 用#define 或typedef把FILE定义为指向结构的指针。类似地，size\_t和time\_t类型也定义在头文件中。

许多程序员都在程序中使用自己开发的标准头文件。如果开发一系列相关的函数或结构，那么这种方法特别有价值。

另外，还可以使用头文件声明外部变量供其他文件共享。例如，如果已经开发了共享某个变量的一系列函数，该变量报告某种状况（如，错误情况），这种方法就很有效。这种情况下，可以在包含这些函数声明的源代码文件定义一个文件作用域的外部链接变量:

然后，可以在与源代码文件相关联的头文件中进行引用式声明:

extern int status; // 在头文件中

这行代码会出现在包含了该头文件的文件中，这样使用该系列函数的文件都能使用这个变量。虽然源代码文件中包含该头文件后也包含了该声明，但是只要声明的类型一致，在一个文件中同时使用定义式声明和引用式声明没问题。

需要包含头文件的另一种情况是，使用具有文件作用域、内部链接和const 限定符的变量或数组。const 防止值被意外修改，static 意味着每个包含该头文件的文件都获得一份副本。因此，不需要在一个文件中进行定义式声明，在其他文件中进行引用式声明。

#include和#define指令是最常用的两个C预处理器特性。接下来，我们介绍一些其他指令。

## 16.6 其他指令

程序员可能要为不同的工作环境准备C程序和C库包。不同的环境可能使用不同的代码类型。预处理器提供一些指令，程序员通过修改#define的值即可生成可移植的代码。#undef指令取消之前的#define定义。#if、#ifdef、#ifndef、#else、#elif和#endif指令用于指定什么情况下编写哪些代码。#line指令用于重置行和文件信息，#error指令用于给出错误消息，#pragma指令用于向编译器发出指令。

## 16.6.1 #undef指令

#undef指令用于“取消”已定义的#define指令。也就是说，假设有如下定义:

#define LIMIT 400

然后，下面的指令:

#undef LIMIT

将移除上面的定义。现在就可以把LIMIT重新定义为一个新值。即使原来没有定义LIMIT，取消LIMIT的定义仍然有效。如果想使用一个名称，又不确定之前是否已经用过，为安全起见，可以用#undef 指令取消该名字的定义。

## 16.6.2 从C预处理器角度看已定义

处理器在识别标识符时，遵循与C相同的规则:标识符可以由大写字母、小写字母、数字和下划线字符组成，且首字符不能是数字。当预处理器在预处理器指令中发现一个标识符时，它会把该标识符当作已定义的或未定义的。这里的已定义表示由预处理器定义。如果标识符是同一个文件中由前面的#define指令创建的宏名，而且没有用#undef 指令关闭，那么该标识符是已定义的。如果标识符不是宏，假设是一个文件作用域的C变量，那么该标

识符对预处理器而言就是未定义的。

已定义宏可以是对象宏，包括空宏或类函数宏:

#define LIMIT 1000 // LIMIT是已定义的

#define GOOD // GOOD 是已定义的

#define A(X) ((-(X))\*(X)) // A 是已定义的

int q; // q 不是宏，因此是未定义的

#undef GOOD // GOOD 取消定义，是未定义的

注意，#define宏的作用域从它在文件中的声明处开始，直到用#undef指令取消宏为止，或延伸至文件尾（以二者中先满足的条件作为宏作用域的结束）。另外还要注意，如果宏通过头文件引入，那么#define在文件中的位置取决于#include指令的位置。

稍后将介绍几个预定义宏，如\_\_DATE\_\_和\_\_FILE\_\_。这些宏一定是已定义的，而且不能取消定义。

## 16.6.3 条件编译

可以使用其他指令创建条件编译（conditinal compilation）。也就是说，可以使用这些指令告诉编译器根据编译时的条件执行或忽略信息（或代码）块。

## 1.#ifdef、#else和#endif指令

我们用一个简短的示例来演示条件编译的情况。考虑下面的代码:

#ifdef MAVIS

#include "horse.h"// 如果已经用#define定义了 MAVIS，则执行下面的指令

#define STABLES 5

#else

#include "cow.h" //如果没有用#define定义 MAVIS，则执行下面的指令

#define STABLES 15

#endif

这里使用的较新的编译器和 ANSI 标准支持的缩进格式。如果使用旧的编译器，必须左对齐所有的指令或至少左对齐#号，如下所示:

#ifdef MAVIS

#include "horse.h" // 如果已经用#define定义了 MAVIS，则执行下面的指令

#define STABLES 5

#else

#include "cow.h" //如果没有用#define定义 MAVIS，则执行下面的指令

#define STABLES 15

#endif

#ifdef指令说明，如果预处理器已定义了后面的标识符（MAVIS），则执行#else或#endif指令之前的所有指令并编译所有C代码（先出现哪个指令就执行到哪里）。如果预处理器未定义MAVIS，且有 #else指令，则执行#else和#endif指令之间的所有代码。

#ifdef #else很像C的if else。两者的主要区别是，预处理器不识别用于标记块的花括号（{}），因此它使用#else（如果需要）和#endif（必须存在）来标记指令块。这些指令结构可以嵌套。也可以用这些指令标记C语句块，如程序清单16.9所示。

程序清单16.9 ifdef.c程序

```c
/* ifdef.c -- 使用条件编译 */
#include <stdio.h>
#define JUST_CHECKING
#define LIMIT 4
int main(void)
{
int i;
int total = 0;
for (i = 1; i <= LIMIT; i++)
{
total += 2 * i*i + 1;
#ifdef JUST_CHECKING
printf("i=%d, running total = %d\n", i, total);
#endif
}
printf("Grand total = %d\n", total);
```

```scss
return 0;
}
```

编译并运行该程序后，输出如下:

```txt
i=1, running total = 3
i=2, running total = 12
i=3, running total = 31
i=4, running total = 64
Grand total = 64
```

如果省略JUST\_CHECKING定义（把它放在C注释中，或者使用#undef指令取消它的定义）并重新编译该程序，只会输出最后一行。可以用这种方法在调试程序。定义JUST\_CHECKING并合理使用#ifdef，编译器将执行用于调试的程序代码，打印中间值。调试结束后，可移除JUST\_CHECKING定义并重新编译。如果以后还需要使用这些信息，重新插入定义即可。这样做省去了再次输入额外打印语句的麻烦。#ifdef还可用于根据不同的C实现选择合适的代码块。

## 2.#ifndef指令

#ifndef指令与#ifdef指令的用法类似，也可以和#else、#endif一起使用，但是它们的逻辑相反。#ifndef指令判断后面的标识符是否是未定义的，常用于定义之前未定义的常量。如下所示:

```c
/* arrays.h */
#ifndef SIZE
#define SIZE 100
```

#endif

（旧的实现可能不允许使用缩进的#define）

通常，包含多个头文件时，其中的文件可能包含了相同宏定义。#ifndef指令可以防止相同的宏被重复定义。在首次定义一个宏的头文件中用#ifndef指令激活定义，随后在其他头文件中的定义都被忽略。

#ifndef指令还有另一种用法。假设有上面的arrays.h头文件，然后把下面一行代码放入一个头文件中:

#include "arrays.h"

SIZE被定义为100。但是，如果把下面的代码放入该头文件:

#define SIZE 10

#include "arrays.h"

SIZE则被设置为10。这里，当执行到#include "arrays.h"这行，处理array.h中的代码时，由于SIZE是已定义的，所以跳过了#define SIZE 100这行代码。鉴于此，可以利用这种方法，用一个较小的数组测试程序。测试完毕后，移除#define SIZE 10并重新编译。这样，就不用修改头文件数组本身了。

#ifndef指令通常用于防止多次包含一个文件。也就是说，应该像下面这样设置头文件:

/\* things.h \*/

#ifndef THINGS\_H\_

#define THINGS\_H\_

/\* 省略了头文件中的其他内容\*/

#endif

假设该文件被包含了多次。当预处理器首次发现该文件被包含时，THINGS\_H\_是未定义的，所以定义了THINGS\_H\_，并接着处理该文件的其他部分。当预处理器第2次发现该文件被包含时，THINGS\_H\_是已定义的，所以预处理器跳过了该文件的其他部分。

为何要多次包含一个文件？最常见的原因是，许多被包含的文件中都包含着其他文件，所以显式包含的文件中可能包含着已经包含的其他文件。这有什么问题？在被包含的文件中有某些项（如，一些结构类型的声明）只能在一个文件中出现一次。C标准头文件使用#ifndef技巧避免重复包含。但是，这存在一个问题:如何确保待测试的标识符没有在别处定义。通常，实现的供应商使用这些方法解决这个问题:用文件名作为标识符、使用大写字母、用下划线字符代替文件名中的点字符、用下划线字符做前缀或后缀（可能使用两条下划线）。例如，查看stdio.h头文件，可以发现许多类似的代码:

#ifndef \_STDIO\_H

#define \_STDIO\_H

// 省略了文件的内容

#endif

你也可以这样做。但是，由于标准保留使用下划线作为前缀，所以在自己的代码中不要这样写，避免与标准头文件中的宏发生冲突。程序清单16.10修改了程序清单16.6中的头文件，使用#ifndef避免文件被重复包含。

程序清单**16.10 names.c**程序

// names.h --修订后的 names\_st 头文件，避免重复包含

#ifndef NAMES\_H\_

```c
#define NAMES_H_
// 明示常量
#define SLEN 32
// 结构声明
struct names_st
{
char first[SLEN];
char last[SLEN];
};
// 类型定义
typedef struct names_st names;
// 函数原型
void get_names(names *);
void show_names(const names *);
char * s_gets(char * st, int n);
#endif
```

用程序清单16.11的程序测试该头文件没问题，但是如果把清单16.10中的#ifndef保护删除后，程序就无法通过编译。

程序清单**16.11 doubincl.c**程序

```c
// doubincl.c -- 包含头文件两次
#include <stdio.h>
#include "names.h"
#include "names.h"  // 不小心第2次包含头文件
int main()
{
names winner = { "Less", "Ismoor" };
printf("The winner is %s %s.\n", winner.first,
winner.last);
return 0;
}
```

## 3.#if和#elif指令

#if指令很像C语言中的if。#if后面跟整型常量表达式，如果表达式为非零，则表达式为真。可以在指令中使用C的关系运算符和逻辑运算符:

```c
#if SYS == 1

#include "ibm.h"

#endif
```

可以按照if else的形式使用#elif（早期的实现不支持#elif）。例如，可以这样写:

```python
#if SYS == 1
```

```c
#include "ibmpc.h"
#elif SYS == 2
#include "vax.h"
#elif SYS == 3
#include "mac.h"
#else
#include "general.h"
#endif
```

较新的编译器提供另一种方法测试名称是否已定义，即用#if defined (VAX)代替#ifdef VAX。

这里，defined是一个预处理运算符，如果它的参数是用#defined定义过，则返回1；否则返回0。这种新方法的优点是，它可以和#elif一起使用。下面用这种形式重写前面的示例:

```txt
#if defined (IBMPC)
#include "ibmpc.h"
#elif defined (VAX)
#include "vax.h"
#elif defined (MAC)
#include "mac.h"
#else
```

#include "general.h"

#endif

如果在VAX机上运行这几行代码，那么应该在文件前面用下面的代码定义VAX:

#define VAX

条件编译还有一个用途是让程序更容易移植。改变文件开头部分的几个关键的定义，即可根据不同的系统设置不同的值和包含不同的文件。

## 16.6.4 预定义宏

C标准规定了一些预定义宏，如表16.1所列。

表16.1 预定义宏

| 宏 | 含义 |
| --- | --- |
| __DATE__ | 预处理的日期("Mmm dd yyyy"形式的字符串字面量,如Nov 23 2013) |
| __FILE__ | 表示当前源代码文件名的字符串字面量 |
| __LINE__ | 表示当前源代码文件中行号的整型常量 |
| __STDC__ | 设置为1时,表明实现遵循C标准 |
| __STDC_HOSTED__ | 本机环境设置为1;否则设置为0 |
| __STDC_VERSION__ | 支持C99标准,设置为199901L;支持C11标准,设置为201112L |
| __TIME__ | 翻译代码的时间,格式为“hh:mm:ss” |

C99 标准提供一个名为\_ \_func\_ \_的预定义标识符，它展开为一个代表函数名的字符串（该函数包含该标识符）。那么，\_ \_func\_ \_必须具有函数作用域，而从本质上看宏具有文件作用域。因此，\_ \_func\_ \_是C语言的预定义标识符，而不是预定义宏。

程序清单16.12 中使用了一些预定义宏和预定义标识符。注意，其中一些是C99 新增的，所以不支持C99的编译器可能无法识别它们。如果使用GCC，必须设置-std=c99或-std=c11。

程序清单16.12 predef.c程序

```c
// predef.c -- 预定义宏和预定义标识符
#include <stdio.h>

void why_me();

int main()
{
printf("The file is %s.\n", __FILE__);
printf("The date is %s.\n", __DATE__);
printf("The time is %s.\n", __TIME__);
printf("The version is %ld.\n", __STDC_VERSION__);
printf("This is line %d.\n", __LINE__);
printf("This function is %s\n", __func__);
why_me();
return 0;
}
void why_me()
{
printf("This function is %s\n", __func__);
printf("This is line %d.\n", __LINE__;
```

}

下面是该程序的输出:

The file is predef.c.

The date is Sep 23 2013.

The time is 22:01:09.

The version is 201112.

This is line 11.

This function is main

This function is why\_me

This is line 21.

## 16.6.5 #line和#error

#line指令重置\_ \_LINE\_ \_和\_ \_FILE\_ \_宏报告的行号和文件名。可以这样使用#line:

#line 1000 // 把当前行号重置为1000

#line 10 "cool.c" // 把行号重置为10，把文件名重置为cool.c

#error 指令让预处理器发出一条错误消息，该消息包含指令中的文本。如果可能的话，编译过程应该中断。可以这样使用#error指令:

#if \_ \_STDC\_VERSION\_ \_ != 201112L

#error Not C11

#endif

编译以上代码生成后，输出如下:

\$ gcc newish.c

newish.c:14:2: error: #error Not C11

\$ gcc -std=c11 newish.c

\$

如果编译器只支持旧标准，则会编译失败，如果支持C11标准，就能成功编译。

## 16.6.6 #pragma

在现在的编译器中，可以通过命令行参数或IDE菜单修改编译器的一些设置。#pragma把编译器指令放入源代码中。例如，在开发C99时，标准被称为C9X，可以使用下面的编译指示（pragma）让编译器支持C9X:

#pragma c9x on

一般而言，编译器都有自己的编译指示集。例如，编译指示可能用于控制分配给自动变量的内存量，或者设置错误检查的严格程度，或者启用非标准语言特性等。C99 标准提供了 3 个标准编译指示，但是超出了本书讨论的范围。

C99还提供\_Pragma预处理器运算符，该运算符把字符串转换成普通的编译指示。例如:

Pragma("nonstandardtreatmenttypeB on")

等价于下面的指令:

#pragma nonstandardtreatmenttypeB on

由于该运算符不使用#符号，所以可以把它作为宏展开的一部分:

#define PRAGMA(X) \_Pragma(#X)

然后，可以使用类似下面的代码:

LIMRG ( ON )

顺带一提，下面的定义看上去没问题，但实际上无法正常运行:

#define LIMRG(X) \_Pragma(STDC CX\_LIMITED\_RANGE #X)

问题在于这行代码依赖字符串的串联功能，而预处理过程完成之后才会串联字符串。

\_Pragma 运算符完成“解字符串”（destringizing）的工作，即把字符串中的转义序列转换成它所代表的字符。因此，

Pragma("use\_bool \"true \"false")

变成了:

#pragma use\_bool "true "false

## 16.6.7 泛型选择（C11）

在程序设计中，泛型编程（generic programming）指那些没有特定类型，但是一旦指定一种类型，就可以转换成指定类型的代码。例如，C++在模板中可以创建泛型算法，然后编译器根据指定的类型自动使用实例化代码。C没有这种功能。然而，C11新增了一种表达式，叫作泛型选择表达式（generic selection expression），可根据表达式的类型（即表达式的类型是int、double 还是其他类型）选择一个值。泛型选择表达式不是预处理器指令，但是在一些泛型编程中它常用作#define宏定义的一部分。

下面是一个泛型选择表达式的示例:

Generic(x, int: 0, float: 1, double: 2, default: 3)

\_Generic是C11的关键字。\_Generic后面的圆括号中包含多个用逗号分隔的项。第1个项是一个表达式，后面的每个项都由一个类型、一个冒号和一个值组成，如float: 1。第1个项的类型匹配哪个标签，整个表达式的值是该标签后面的值。例如，假设上面表达式中x是int类型的变量，x的类型匹配int:标签，那么整个表达式的值就是0。如果没有与类型匹配的标签，表达式的值就是default:标签后面的值。泛型选择语句与 switch 语句类似，只是前者用表达式的类型匹配标签，而后者用表达式的值匹配标签。

下面是一个把泛型选择语句和宏定义组合的例子:

```txt
#define MYTYPE(X) _Generic((X),\
int: "int",\
float : "float",\
double: "double",\
default: "other"\
)
```

宏必须定义为一条逻辑行，但是可以用\把一条逻辑行分隔成多条物理行。在这种情况下，对泛型选择表达式求值得字符串。例如，对MYTYPE(5)求值得"int"，因为值5的类型与int:标签匹配。程序清单16.13演示了这种用法。

程序清单**16.13 mytype.c**程序

```c
// mytype.c

#include <stdio.h>
```

#define MYTYPE(X) \_Generic((X),\

```javascript
int: "int",\
float : "float",\
double: "double",\
default: "other"\
)
int main(void)
{
int d = 5;
```

printf("%s\n", MYTYPE(d)); // d 是int类型

```c
printf("%s\n", MYTYPE(2.0*d)); // 2.0 * d 是double类型
printf("%s\n", MYTYPE(3L));      // 3L 是long类型
printf("%s\n", MYTYPE(&d));     // &d 的类型是 int *
return 0;
}
```

下面是该程序的输出:

```ignorefile
int
double
other
```

other

MYTYPE()最后两个示例所用的类型与标签不匹配，所以打印默认的字符串。可以使用更多类型标签来扩展宏的能力，但是该程序主要是为了演示\_Generic的基本工作原理。

对一个泛型选择表达式求值时，程序不会先对第一个项求值，它只确定类型。只有匹配标签的类型后才会对表达式求值。

可以像使用独立类型（“泛型”）函数那样使用\_Generic 定义宏。本章后面介绍 math 库时会给出一个示例。

## 16.7 内联函数（C99）

通常，函数调用都有一定的开销，因为函数的调用过程包括建立调用、传递参数、跳转到函数代码并返回。使用宏使代码内联，可以避免这样的开销。C99还提供另一种方法:内联函数（inline function）。读者可能顾名思义地认为内联函数会用内联代码替换函数调用。其实C99和C11标准中叙述的是:“把函数变成内联函数建议尽可能快地调用该函数，其具体效果由实现定义”。因此，把函数变成内联函数，编译器可能会用内联代码替换函数调用，并（或）执行一些其他的优化，但是也可能不起作用。

创建内联函数的定义有多种方法。标准规定具有内部链接的函数可以成为内联函数，还规定了内联函数的定义与调用该函数的代码必须在同一个文件中。因此，最简单的方法是使用函数说明符 inline 和存储类别说明符static。通常，内联函数应定义在首次使用它的文件中，所以内联函数也相当于函数原型。如下所示:

```c
#include <stdio.h>

inline static void eatline()  // 内联函数定义/原型
{
while (getchar() != '\n')
continue;
}
int main()
{
```

```txt
eatline();                      // 函数调用
...
}
```

编译器查看内联函数的定义（也是原型），可能会用函数体中的代码替换 eatline()函数调用。也就是说，效果相当于在函数调用的位置输入函数体中的代码:

```c
#include <stdio.h>

inline static void eatline() //内联函数定义/原型
{
while (getchar() != '\n')
continue;
}
int main()
{
...
while (getchar() != '\n') //替换函数调用
continue;
...
}
```

由于并未给内联函数预留单独的代码块，所以无法获得内联函数的地址

（实际上可以获得地址，不过这样做之后，编译器会生成一个非内联函数）。另外，内联函数无法在调试器中显示。

内联函数应该比较短小。把较长的函数变成内联并未节约多少时间，因为执行函数体的时间比调用函数的时间长得多。

编译器优化内联函数必须知道该函数定义的内容。这意味着内联函数定义与函数调用必须在同一个文件中。鉴于此，一般情况下内联函数都具有内部链接。因此，如果程序有多个文件都要使用某个内联函数，那么这些文件中都必须包含该内联函数的定义。最简单的做法是，把内联函数定义放入头文件，并在使用该内联函数的文件中包含该头文件即可。

```c
// eatline.h

#ifndef EATLINE_H_

#define EATLINE_H_

inline static void eatline()

{

while (getchar() != '\n')

continue;

}

#endif
```

一般都不在头文件中放置可执行代码，内联函数是个特例。因为内联函数具有内部链接，所以在多个文件中定义同一个内联函数不会产生什么问题。

与C++不同的是，C还允许混合使用内联函数定义和外部函数定义（具

有外部链接的函数定义）。例如，一个程序中使用下面3个文件:

```lisp
//file1.c

...

inline static double square(double);

double square(double x) { return x * x; }

int main()
{
double q = square(1.3);

...

//file2.c

...

double square(double x) { return (int) (x*x); }

void spam(double v)
{

double kv = square(v);

...

//file3.c

...

inline double square(double x) { return (int) (x * x + 0.5); }
```

```txt
void masp(double w)
{
double kw = square(w);
...
```

如上述代码所示，3个文件中都定义了square()函数。file1.c文件中是inline static定义；file2.c 文件中是普通的函数定义（因此具有外部链接）；file3.c 文件中是 inline 定义，省略了static。

3个文件中的函数都调用了square()函数，这会发生什么情况？。file1.c文件中的main()使用square()的局部static定义。由于该定义也是inline定义，所以编译器有可能优化代码，也许会内联该函数。file2.c 文件中，spam()函数使用该文件中 square()函数的定义，该定义具有外部链接，其他文件也可见。file3.c文件中，编译器既可以使用该文件中square()函数的内联定义，也可以使用file2.c文件中的外部链接定义。如果像file3.c那样，省略file1.c文件inline定义中的static，那么该inline定义被视为可替换的外部定义。

注意GCC在C99之前就使用一些不同的规则实现了内联函数，所以GCC可以根据当前编译器的标记来解释inline。

## 16.8 \_Noreturn函数（C11）

C99新增inline关键字时，它是唯一的函数说明符（关键字extern和static是存储类别说明符，可应用于数据对象和函数）。C11新增了第2个函数说明符\_Noreturn，表明调用完成后函数不返回主调函数。exit()函数是\_Noreturn 函数的一个示例，一旦调用exit()，它不会再返回主调函数。注意，这与void返回类型不同。void类型的函数在执行完毕后返回主调函数，只是它不提供返回值。

\_Noreturn的目的是告诉用户和编译器，这个特殊的函数不会把控制返回主调程序。告诉用户以免滥用该函数，通知编译器可优化一些代码。