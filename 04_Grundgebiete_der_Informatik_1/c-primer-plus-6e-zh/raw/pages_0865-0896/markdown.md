块作用域的变量通常都具有自动存储期。当程序进入定义这些变量的块时，为这些变量分配内存；当退出这个块时，释放刚才为变量分配的内存。这种做法相当于把自动变量占用的内存视为一个可重复使用的工作区或暂存区。例如，一个函数调用结束后，其变量占用的内存可用于储存下一个被调用函数的变量。

变长数组稍有不同，它们的存储期从声明处到块的末尾，而不是从块的开始处到块的末尾。

我们到目前为止使用的局部变量都是自动类别。例如，在下面的代码中，变量number和index在每次调用bore()函数时被创建，在离开函数时被销毁:

```c
void bore(int number)
{
int index;
for (index = 0; index < number; index++)
puts("They don't make them the way they used to.\n");
return 0;
}
```

然而，块作用域变量也能具有静态存储期。为了创建这样的变量，要把变量声明在块中，且在声明前面加上关键字static:

```txt
void more(int number)
{
int index;
```

```txt
static int ct = 0;

...
return 0;
}
```

这里，变量ct储存在静态内存中，它从程序被载入到程序结束期间都存在。但是，它的作用域定义在more()函数块中。只有在执行该函数时，程序才能使用ct访问它所指定的对象（但是，该函数可以给其他函数提供该存储区的地址以便间接访问该对象，例如通过指针形参或返回值）。

C 使用作用域、链接和存储期为变量定义了多种存储方案。本书不涉及并发程序设计，所以不再赘述这方面的内容。已分配存储期在本章后面介绍。因此，剩下5种存储类别:自动、寄存器、静态块作用域、静态外部链接、静态内部链接，如表12.1所列。现在，我们已经介绍了作用域、链接和存储期，接下来将详细讨论这些存储类别。

表12.1 5种存储类别

| 存储类别 | 存储期 | 作用域 | 链接 | 声明方式 |
| --- | --- | --- | --- | --- |
| 自动 | 自动 | 块 | 无 | 块内 |
| 寄存器 | 自动 | 块 | 无 | 块内,使用关键字register |
| 静态外部链接 | 静态 | 文件 | 外部 | 所有函数外 |
| 静态内部链接 | 静态 | 文件 | 内部 | 所有函数外,使用关键字static |
| 静态无链接 | 静态 | 块 | 无 | 块内,使用关键字static |

## 12.1.4 自动变量

属于自动存储类别的变量具有自动存储期、块作用域且无链接。默认情况下，声明在块或函数头中的任何变量都属于自动存储类别。为了更清楚地表达你的意图（例如，为了表明有意覆盖一个外部变量定义，或者强调不要把该变量改为其他存储类别），可以显式使用关键字auto，如下所示:

```txt
int main(void)
```

```sql
{
auto   int  plox;
```

关键字auto是存储类别说明符（storage-class specifier）。auto关键字在C++中的用法完全不同，如果编写C/C++兼容的程序，最好不要使用auto作为存储类别说明符。

块作用域和无链接意味着只有在变量定义所在的块中才能通过变量名访问该变量（当然，参数用于传递变量的值和地址给另一个函数，但是这是间接的方法）。另一个函数可以使用同名变量，但是该变量是储存在不同内存位置上的另一个变量。

变量具有自动存储期意味着，程序在进入该变量声明所在的块时变量存在，程序在退出该块时变量消失。原来该变量占用的内存位置现在可做他用。

接下来分析一下嵌套块的情况。块中声明的变量仅限于该块及其包含的块使用。

```lisp
int loop(int n)
{
int m; // m 的作用域
scanf("%d", &m);
{
int i; // m 和 i 的作用域
for (i = m; i < n; i++)
puts("i is local to a sub-block\n");
```

```txt
}
return m; // m 的作用域，i 已经消失
}
```

在上面的代码中，i仅在内层块中可见。如果在内层块的前面或后面使用i，编译器会报错。通常，在设计程序时用不到这个特性。然而，如果这个变量仅供该块使用，那么在块中就近定义该变量也很方便。这样，可以在靠近使用变量的地方记录其含义。另外，这样的变量只有在使用时才占用内存。变量n和 m 分别定义在函数头和外层块中，它们的作用域是整个函数，而且在调用函数到函数结束期间都一直存在。

如果内层块中声明的变量与外层块中的变量同名会怎样？内层块会隐藏外层块的定义。但是离开内层块后，外层块变量的作用域又回到了原来的作用域。程序清单12.1演示了这一过程。

程序清单12.1 hiding.c程序

```c
// hiding.c -- 块中的变量
#include <stdio.h>
int main()
{
int x = 30;          // 原始的 x
printf("x in outer block: %d at %p\n", x, &x);
{
int x = 77;          // 新的 x，隐藏了原始的 x
printf("x in inner block: %d at %p\n", x, &x);
```

```c
}
printf("x in outer block: %d at %p\n", x, &x);
while (x++ < 33)          // 原始的 x
{
int x = 100;            // 新的 x，隐藏了原始的 x
x++;
printf("x in while loop: %d at %p\n", x, &x);
}
printf("x in outer block: %d at %p\n", x, &x);
return 0;
}
```

下面是该程序的输出:

```txt
x in outer block: 30 at 0x7fff5fbff8c8
x in inner block: 77 at 0x7fff5fbff8c4
x in outer block: 30 at 0x7fff5fbff8c8
x in while loop: 101 at 0x7fff5fbff8c0
x in while loop: 101 at 0x7fff5fbff8c0
x in while loop: 101 at 0x7fff5fbff8c0
x in outer block: 34 at 0x7fff5fbff8c8
```

首先，程序创建了变量x并初始化为30，如第1条printf()语句所示。然后，定义了一个新的变量x，并设置为77，如第2条printf()语句所示。根据显示的地址可知，新变量隐藏了原始的x。第3条printf()语句位于第1个内层块后面，显示的是原始的x的值，这说明原始的x既没有消失也不曾改变。

也许该程序最难懂的是while循环。while循环的测试条件中使用的是原始的x:

$$
\text {while} (\mathrm{x} + + <   3 3)
$$

在该循环中，程序创建了第3个x变量，该变量只定义在while循环中。所以，当执行到循环体中的x++时，递增为101的是新的x，然后printf()语句显示了该值。每轮迭代结束，新的x变量就消失。然后循环的测试条件使用并递增原始的x，再次进入循环体，再次创建新的x。在该例中，这个x被创建和销毁了3次。注意，该循环必须在测试条件中递增x，因为如果在循环体中递增x，那么递增的是循环体中创建的x，而非测试条件中使用的原始x。

我们使用的编译器在创建while循环体中的x时，并未复用内层块中x占用的内存，但是有些编译器会这样做。

该程序示例的用意不是鼓励读者要编写类似的代码（根据C的命名规则，要想出别的变量名并不难），而是为了解释在内层块中定义变量的具体情况。

## 1.没有花括号的块

前面提到一个C99特性:作为循环或if语句的一部分，即使不使用花括号（{}），也是一个块。更完整地说，整个循环是它所在块的子块（subblock），循环体是整个循环块的子块。与此类似，if 语句是一个块，与其相关联的子语句是if语句的子块。这些规则会影响到声明的变量和这些变量的作用域。程序清单12.2演示了for循环中该特性的用法。

程序清单**12.2 forc99.c**程序

// forc99.c -- 新的 C99 块规则

```c
#include <stdio.h>

int main()
{
int n = 8;
printf(" Initially, n = %d at %p\n", n, &n);
for (int n = 1; n < 3; n++)
printf(" loop 1: n = %d at %p\n", n, &n);
printf("After loop 1, n = %d at %p\n", n, &n);
for (int n = 1; n < 3; n++)
{
printf(" loop 2 index n = %d at %p\n", n, &n);
int n = 6;
printf(" loop 2: n = %d at %p\n", n, &n);
n++;
}
printf("After loop 2, n = %d at %p\n", n, &n);
return 0;
}
```

假设编译器支持C语言的这个新特性，该程序的输出如下:

```txt
Initially, n = 8 at 0x7fff5fbff8c8
```

```txt
loop 1: n = 1 at 0x7fff5fbff8c4
```

```txt
loop 1: n = 2 at 0x7fff5fbff8c4
```

```txt
After loop 1, n = 8 at 0x7fff5fbff8c8
```

```txt
loop 2 index n = 1 at 0x7fff5fbff8c0
```

```txt
loop 2: n = 6 at 0x7fff5fbff8bc
```

```txt
loop 2 index n = 2 at 0x7fff5fbff8c0
```

```txt
loop 2: n = 6 at 0x7fff5fbff8bc
```

```txt
After loop 2, n = 8 at 0x7fff5fbff8c8
```

第1个for循环头中声明的n，其作用域作用至循环末尾，而且隐藏了原始的n。但是，离开循环后，原始的n又起作用了。

第2个for循环头中声明的n作为循环的索引，隐藏了原始的n。然后，在循环体中又声明了一个n，隐藏了索引n。结束一轮迭代后，声明在循环体中的n消失，循环头使用索引n进行测试。当整个循环结束时，原始的 n 又起作用了。再次提醒读者注意，没必要在程序中使用相同的变量名。如果用了，各变量的情况如上所述。

## 注意支持C99和C11

有些编译器并不支持C99/C11的这些作用域规则（Microsoft Visual Studio 2012就是其中之一）。有些编译会提供激活这些规则的选项。例如，撰写本书时，gcc默认支持了C99的许多特性，但是要用 $- s t d = c 9 9$ 选项激活程序清单12.2中使用的特性:

```txt
gcc -std=c99 forc99.c
```

与此类似，gcc或clang都要使用 $-s t d = c \bot x 或 -s t d = c \bot \bot$ 选项，才支持C11特性。

## 2.自动变量的初始化

自动变量不会初始化，除非显式初始化它。考虑下面的声明:

```c
int main(void)
{
intrepid;
int tents = 5;
```

tents变量被初始化为5，但是repid变量的值是之前占用分配给repid的空间中的任意值（如果有的话），别指望这个值是0。可以用非常量表达式（non-constant expression）初始化自动变量，前提是所用的变量已在前面定义过:

```c
int main(void)
{
int ruth = 1;
```

int rance = 5 \* ruth; // 使用之前定义的变量

## 12.1.5 寄存器变量

变量通常储存在计算机内存中。如果幸运的话，寄存器变量储存在CPU的寄存器中，或者概括地说，储存在最快的可用内存中。与普通变量相比，访问和处理这些变量的速度更快。由于寄存器变量储存在寄存器而非内存中，所以无法获取寄存器变量的地址。绝大多数方面，寄存器变量和自动变量都一样。也就是说，它们都是块作用域、无链接和自动存储期。使用存储类别说明符register便可声明寄存器变量:

```c
int main(void)
{
register int quick;
```

我们刚才说“如果幸运的话”，是因为声明变量为register类别与直接命令相比更像是一种请求。编译器必须根据寄存器或最快可用内存的数量衡量你的请求，或者直接忽略你的请求，所以可能不会如你所愿。在这种情况下，寄存器变量就变成普通的自动变量。即使是这样，仍然不能对该变量使用地址运算符。

在函数头中使用关键字register，便可请求形参是寄存器变量:

void macho(register int n)

可声明为register的数据类型有限。例如，处理器中的寄存器可能没有足够大的空间来储存double类型的值。

## 12.1.6 块作用域的静态变量

静态变量（static variable）听起来自相矛盾，像是一个不可变的变量。实际上，静态的意思是该变量在内存中原地不动，并不是说它的值不变。具有文件作用域的变量自动具有（也必须是）静态存储期。前面提到过，可以创建具有静态存储期、块作用域的局部变量。这些变量和自动变量一样，具有相同的作用域，但是程序离开它们所在的函数后，这些变量不会消失。也就是说，这种变量具有块作用域、无链接，但是具有静态存储期。计算机在多次函数调用之间会记录它们的值。在块中（提供块作用域和无链接）以存储类别说明符static（提供静态存储期）声明这种变量。程序清单12.3演示了一个这样的例子。

程序清单12.3 loc\_stat.c程序

```c
/* loc_stat.c -- 使用局部静态变量 */
#include <stdio.h>

void trystat(void);

int main(void)
{
int count;
for (count = 1; count <= 3; count++)
{
printf("Here comes iteration %d:\n", count);
trystat();
}
return 0;
}
void trystat(void)
{
int fade = 1;
static int stay = 1;
printf("fade = %d and stay = %d\n", fade++, stay++);
```

}

注意，trystat()函数先打印再递增变量的值。该程序的输出如下:

```python
Here comes iteration 1:
fade = 1 and stay = 1
Here comes iteration 2:
fade = 1 and stay = 2
Here comes iteration 3:
fade = 1 and stay = 3
```

静态变量stay保存了它被递增1后的值，但是fade变量每次都是1。这表明了初始化的不同:每次调用trystat()都会初始化fade，但是stay只在编译strstat()时被初始化一次。如果未显式初始化静态变量，它们会被初始化为0。

下面两个声明很相似:

int fade = 1;

static int stay = 1;

第1条声明确实是trystat()函数的一部分，每次调用该函数时都会执行这条声明。这是运行时行为。第2条声明实际上并不是trystat()函数的一部分。如果逐步调试该程序会发现，程序似乎跳过了这条声明。这是因为静态变量和外部变量在程序被载入内存时已执行完毕。把这条声明放在trystat()函数中是为了告诉编译器只有trystat()函数才能看到该变量。这条声明并未在运行时执行。

不能在函数的形参中使用static:

int wontwork(static int flu); // 不允许

“局部静态变量”是描述具有块作用域的静态变量的另一个术语。阅读一些老的 C文献时会发现，这种存储类别被称为内部静态存储类别（internal static storage class）。这里的内部指的是函数内部，而非内部链接。

## 12.1.7 外部链接的静态变量

外部链接的静态变量具有文件作用域、外部链接和静态存储期。该类别有时称为外部存储类别（external storage class），属于该类别的变量称为外部变量（external variable）。把变量的定义性声明（defining declaration）放在在所有函数的外面便创建了外部变量。当然，为了指出该函数使用了外部变量，可以在函数中用关键字extern再次声明。如果一个源代码文件使用的外部变量定义在另一个源代码文件中，则必须用extern在该文件中声明该变量。如下所示:

```txt
int Errupt;                      /* 外部定义的变量 */
double Up[100];              /* 外部定义的数组 */
extern char Coal;             /* 如果Coal被定义在另一个文件， */
/*则必须这样声明*/
void next(void);
int main(void)
{
extern int Errupt;      /* 可选的声明*/
extern double Up[];     /* 可选的声明*/
...
```

```txt
}
void next(void)
{
...
}
```

注意，在main()中声明Up数组时（这是可选的声明）不用指明数组大小，因为第1次声明已经提供了数组大小信息。main()中的两条 extern 声明完全可以省略，因为外部变量具有文件作用域，所以Errupt和Up从声明处到文件结尾都可见。它们出现在那里，仅为了说明main()函数要使用这两个变量。

如果省略掉函数中的extern关键字，相当于创建了一个自动变量。去掉下面声明中的extern:

extern int Errupt;

便成为:

int Errupt;

这使得编译器在 main()中创建了一个名为 Errupt 的自动变量。它是一个独立的局部变量，与原来的外部变量Errupt不同。该局部变量仅main()中可见，但是外部变量Errupt对于该文件的其他函数（如 next()）也可见。简而言之，在执行块中的语句时，块作用域中的变量将“隐藏”文件作用域中的同名变量。如果不得已要使用与外部变量同名的局部变量，可以在局部变量的声明中使用 auto 存储类别说明符明确表达这种意图。

外部变量具有静态存储期。因此，无论程序执行到main()、next()还是其他函数，数组Up及其值都一直存在。

下面 3 个示例演示了外部和自动变量的一些使用情况。示例 1 中有一个外部变量 Hocus。该变量对main()和magic()均可见。

```txt
/* 示例1 */
int Hocus;
int magic();
int main(void)
{
extern int Hocus; // Hocus 之前已声明为外部变量
...
}
int magic()
{
extern int Hocus; // 与上面的Hocus 是同一个变量
...
}
```

示例2中有一个外部变量Hocus，对两个函数均可见。这次，在默认情况下对magic()可见。

/\*示例2 \*/

int Hocus;

int magic();

```txt
int main(void)
{
extern int Hocus; // Hocus之前已声明为外部变量
...
}
int magic()
{
//并未在该函数中声明Hocus，但是仍可使用该变量
...
}
```

在示例3中，创建了4个独立的变量。main()中的Hocus变量默认是自动变量，属于main()私有。magic()中的Hocus变量被显式声明为自动，只有magic()可用。外部变量Houcus对main()和magic()均不可见，但是对该文件中未创建局部Hocus变量的其他函数可见。最后，Pocus是外部变量，magic()可见，但是main()不可见，因为Pocus被声明在main()后面。

/\* 示例 3 \*/

```txt
int Hocus;

int magic();

int  main(void)

{
```

```txt
int Hocus; // 声明Hocus，默认是自动变量
...
}
int Pocus;
int magic()
{
auto int Hocus; //把局部变量Hocus显式声明为自动变量
...
}
```

这 3 个示例演示了外部变量的作用域是:从声明处到文件结尾。除此之外，还说明了外部变量的生命期。外部变量Hocus和Pocus在程序运行中一直存在，因为它们不受限于任何函数，不会在某个函数返回后就消失。

## 1.初始化外部变量

外部变量和自动变量类似，也可以被显式初始化。与自动变量不同的是，如果未初始化外部变量，它们会被自动初始化为 0。这一原则也适用于外部定义的数组元素。与自动变量的情况不同，只能使用常量表达式初始化文件作用域变量:

```txt
int x = 10; // 没问题，10是常量
```

```txt
int y = 3 + 20; // 没问题，用于初始化的是常量表达式
```

```javascript
size_t z = sizeof(int); //没问题，用于初始化的是常量表达式
```

```txt
int x2 = 2 * x; // 不行，x 是变量
```

（只要不是变长数组，sizeof表达式可被视为常量表达式。）

## 2.使用外部变量

下面来看一个使用外部变量的示例。假设有两个函数main()和critic()，它们都要访问变量units。可以把units声明在这两个函数的上面，如程序清单12.4所示（注意:该例的目的是演示外部变量的工作原理，并非它的典型用法）。

程序清单12.4 global.c程序

```c
/* global.c  -- 使用外部变量 */
#include <stdio.h>
int units = 0;      /* 外部变量 */
void critic(void);
int main(void)
{
extern int units;  /* 可选的重复声明 */
printf("How many pounds to a firkin of butter?\n");
scanf("%d", &units);
while (units != 56)
critic();
printf("You must have looked it up!\n");
return 0;
```

```c
}
void critic(void)
{
/* 删除了可选的重复声明 */
printf("No luck, my friend. Try again.\n");
scanf("%d", &units);
}
```

下面是该程序的输出示例:

```txt
How many pounds to a firkin of butter?
```

**14**

```txt
No luck, my friend. Try again.
```

**56**

```txt
You must have looked it up!
```

注意，critic()是如何读取 units的第2 个值的。当while循环结束时，main()也知道units的新值。所以main()函数和critic()都可以通过标识符units访问相同的变量。用C的术语来描述是， units具有文件作用域、外部链接和静态存储期。

把units定义在所有函数定义外面（即外部），units便是一个外部变量，对units定义下面的所有函数均可见。因此，critics()可以直接使用units变量。

类似地，main()也可直接访问units。但是，main()中确实有如下声明:

extern int units;

本例中，以上声明主要是为了指出该函数要使用这个外部变量。存储类别说明符extern告诉编译器，该函数中任何使用units的地方都引用同一个定义在函数外部的变量。再次强调，main()和critic()使用的都是外部定义的units。

## 3.外部名称

C99和C11标准都要求编译器识别局部标识符的前63个字符和外部标识符的前31个字符。这修订了以前的标准，即编译器识别局部标识符前31个字符和外部标识符前6个字符。你所用的编译器可能还执行以前的规则。外部变量名比局部变量名的规则严格，是因为外部变量名还要遵循局部环境规则，所受的限制更多。

## 4.定义和声明

下面进一步介绍定义变量和声明变量的区别。考虑下面的例子:

int tern = 1; /\* tern被定义 \*/

main() {

extern int tern; /\* 使用在别处定义的tern \*/

这里，tern被声明了两次。第1次声明为变量预留了存储空间，该声明构成了变量的定义。第2次声明只告诉编译器使用之前已创建的tern变量，所以这不是定义。第1次声明被称为定义式声明（defining declaration），第2次声明被称为引用式声明（referencing declaration）。关键字extern表明该声明不是定义，因为它指示编译器去别处查询其定义。

假设这样写:

```c
extern int tern;

int main(void)
{
```

编译器会假设 tern 实际的定义在该程序的别处，也许在别的文件中。该声明并不会引起分配存储空间。因此，不要用关键字extern创建外部定义，只用它来引用现有的外部定义。

外部变量只能初始化一次，且必须在定义该变量时进行。假设有下面的代码:

```c
// file_one.c

char permis = 'N';

...

// file_two.c

extern char permis = 'Y'; /* 错误 */
```

file\_two中的声明是错误的，因为file\_one.c中的定义式声明已经创建并初始化了permis。

## 12.1.8 内部链接的静态变量

该存储类别的变量具有静态存储期、文件作用域和内部链接。在所有函数外部（这点与外部变量相同），用存储类别说明符static定义的变量具有这种存储类别:

```txt
static int svil = 1; // 静态变量，内部链接
int main(void)
```

```txt
{
```

这种变量过去称为外部静态变量（external static variable），但是这个术语有点自相矛盾（这些变量具有内部链接）。但是，没有合适的新简称，所以只能用内部链接的静态变量（static variable with internal linkage）。普通的外部变量可用于同一程序中任意文件中的函数，但是内部链接的静态变量只能用于同一个文件中的函数。可以使用存储类别说明符 extern，在函数中重复声明任何具有文件作用域的变量。这样的声明并不会改变其链接属性。考虑下面的代码:

```javascript
int traveler = 1; // 外部链接
```

```txt
static int stayhome = 1; // 内部链接
```

```txt
int   main()
{
```

```txt
extern int traveler; // 使用定义在别处的 traveler
```

```txt
extern int stayhome; // 使用定义在别处的 stayhome
```

```txt
...
```

对于该程序所在的翻译单元，trveler和stayhome都具有文件作用域，但是只有traveler可用于其他翻译单元（因为它具有外部链接）。这两个声明都使用了extern关键字，指明了main()中使用的这两个变量的定义都在别处，但是这并未改变stayhome的内部链接属性。

## 12.1.9 多文件

只有当程序由多个翻译单元组成时，才体现区别内部链接和外部链接的重要性。接下来简要介绍一下。

复杂的C程序通常由多个单独的源代码文件组成。有时，这些文件可能要共享一个外部变量。C通过在一个文件中进行定义式声明，然后在其他文件中进行引用式声明来实现共享。也就是说，除了一个定义式声明外，其他声明都要使用extern关键字。而且，只有定义式声明才能初始化变量。

注意，如果外部变量定义在一个文件中，那么其他文件在使用该变量之前必须先声明它（用 extern关键字）。也就是说，在某文件中对外部变量进行定义式声明只是单方面允许其他文件使用该变量，其他文件在用extern声明之前不能直接使用它。

过去，不同的编译器遵循不同的规则。例如，许多 UNIX系统允许在多个文件中不使用 extern 关键字声明变量，前提是只有一个带初始化的声明。编译器会把文件中一个带初始化的声明视为该变量的定义。

## 12.1.10 存储类别说明符

读者可能已经注意到了，关键字static和extern的含义取决于上下文。C语言有6个关键字作为存储类别说明符:auto、register、static、extern、\_Thread\_local和typedef。typedef关键字与任何内存存储无关，把它归于此类有一些语法上的原因。尤其是，在绝大多数情况下，不能在声明中使用多个存储类别说明符，所以这意味着不能使用多个存储类别说明符作为typedef的一部分。唯一例外的是\_Thread\_local，它可以和static或extern一起使用。

auto说明符表明变量是自动存储期，只能用于块作用域的变量声明中。由于在块中声明的变量本身就具有自动存储期，所以使用auto主要是为了明确表达要使用与外部变量同名的局部变量的意图。

register 说明符也只用于块作用域的变量，它把变量归为寄存器存储类别，请求最快速度访问该变量。同时，还保护了该变量的地址不被获取。

用 static 说明符创建的对象具有静态存储期，载入程序时创建对象，当程序结束时对象消失。如果static 用于文件作用域声明，作用域受限于该文件。如果 static 用于块作用域声明，作用域则受限于该块。因此，只要程序在运行对象就存在并保留其值，但是只有在执行块内的代码时，才能通过标识符访问。块作用域的静态变量无链接。文件作用域的静态变量具有内部链接。

extern 说明符表明声明的变量定义在别处。如果包含 extern 的声明具有文件作用域，则引用的变量必须具有外部链接。如果包含 extern 的声明具有块作用域，则引用的变量可能具有外部链接或内部链接，这接取决于该变量的定义式声明。

小结:存储类别

自动变量具有块作用域、无链接、自动存储期。它们是局部变量，属于其定义所在块（通常指函数）私有。寄存器变量的属性和自动变量相同，但是编译器会使用更快的内存或寄存器储存它们。不能获取寄存器变量的地址。

具有静态存储期的变量可以具有外部链接、内部链接或无链接。在同一个文件所有函数的外部声明的变量是外部变量，具有文件作用域、外部链接和静态存储期。如果在这种声明前面加上关键字static，那么其声明的变量具有文件作用域、内部链接和静态存储期。如果在函数中用 static 声明一个变量，则该变量具有块作用域、无链接、静态存储期。

具有自动存储期的变量，程序在进入该变量的声明所在块时才为其分配内存，在退出该块时释放之前分配的内存。如果未初始化，自动变量中是垃圾值。程序在编译时为具有静态存储期的变量分配内存，并在程序的运行过程中一直保留这块内存。如果未初始化，这样的变量会被设置为0。

具有块作用域的变量是局部的，属于包含该声明的块私有。具有文件作用域的变量对文件（或翻译单元）中位于其声明后面的所有函数可见。具有外部链接的文件作用域变量，可用于该程序的其他翻译单元。具有内部链接的文件作用域变量，只能用于其声明所在的文件内。

下面用一个简短的程序使用了5种存储类别。该程序包含两个文件（程序清单12.5和程序清单12.6），所以必须使用多文件编译（参见第9章或参看编译器的指导手册）。该示例仅为了让读者熟悉5种存储类别的用法，并不是提供设计模型，好的设计可以不需要使用文件作用域变量。

程序清单12.5 parta.c程序

```c
// parta.c --- 不同的存储类别
// 与 partb.c 一起编译
#include <stdio.h>
void report_count();
void accumulate(int k);
int count = 0;          // 文件作用域，外部链接
int main(void)
{
int value;           // 自动变量
register int i;   // 寄存器变量
printf("Enter a positive integer (0 to quit): ");
while (scanf("%d", &value) == 1 && value > 0)
{
++count;      // 使用文件作用域变量
for (i = value; i >= 0; i--)
accumulate(i);
```

```c
printf("Enter a positive integer (0 to quit): ");
}
report_count();
return 0;
}
void report_count()
{
printf("Loop executed %d times\n", count);
}
```

程序清单**12.6 partb.c**程序

// partb.c -- 程序的其余部分

// 与 parta.c 一起编译

#include &lt;stdio.h&gt;

extern int count; // 引用式声明，外部链接

static int total = 0; // 静态定义，内部链接

void accumulate(int k); // 函数原型

void accumulate(int k)// k 具有块作用域，无链接

static int subtotal = 0; // 静态，无链接

```txt
if (k <= 0)
{
printf("loop cycle: %d\n", count);
printf("subtotal: %d; total: %d\n", subtotal, total);
subtotal = 0;
}
else
{
subtotal += k;
total += k;
}
}
```

在该程序中，块作用域的静态变量subtotal统计每次while循环传入accumulate()函数的总数，具有文件作用域、内部链接的变量 total 统计所有传入 accumulate()函数的总数。当传入负值时， accumulate()函数报告total和subtotal的值，并在报告后重置subtotal为0。由于parta.c调用了 accumulate()函数，所以必须包含 accumulate()函数的原型。而 partb.c 只包含了accumulate()函数的定义，并未在文件中调用该函数，所以其原型为可选（即省略原型也不影响使用）。该函数使用了外部变量count 统计main()中的while循环迭代的次数（顺带一提，对于该程序，没必要使用外部变量把 parta.c 和 partb.c的代码弄得这么复杂）。在 parta.c 中，main()和report\_count()共享count。

下面是程序的运行示例:

Enter a positive integer (0 to quit): 5

loop cycle: 1

subtotal: 15; total: 15

Enter a positive integer (0 to quit): 10

loop cycle: 2

subtotal: 55; total: 70

Enter a positive integer (0 to quit): 2

loop cycle: 3

subtotal: 3; total: 73

Enter a positive integer (0 to quit): 0

Loop executed 3 times

## 12.1.11 存储类别和函数

函数也有存储类别，可以是外部函数（默认）或静态函数。C99 新增了第 3 种类别——内联函数，将在第16章中介绍。外部函数可以被其他文件的函数访问，但是静态函数只能用于其定义所在的文件。假设一个文件中包含了以下函数原型:

double gamma(double); /\* 该函数默认为外部函数 \*/

static double beta(int, int);

extern double delta(double, int);

在同一个程序中，其他文件中的函数可以调用gamma()和delta()，但是不能调用beta()，因为以static存储类别说明符创建的函数属于特定模块私有。这样做避免了名称冲突的问题，由于beta()受限于它所在的文件，所以在其他文件中可以使用与之同名的函数。

通常的做法是:用 extern 关键字声明定义在其他文件中的函数。这样做是为了表明当前文件中使用的函数被定义在别处。除非使用static关键字，否则一般函数声明都默认为extern。

## 12.1.12 存储类别的选择

对于“使用哪种存储类别”的回答绝大多数是“自动存储类别”，要知道默认类别就是自动存储类别。初学者会认为外部存储类别很不错，为何不把所有的变量都设置成外部变量，这样就不必使用参数和指针在函数间传递信息了。然而，这背后隐藏着一个陷阱。如果这样做，A()函数可能违背你的意图，私下修改B()函数使用的变量。多年来，无数程序员的经验表明，随意使用外部存储类别的变量导致的后果远远超过了它所带来的便利。

唯一例外的是const数据。因为它们在初始化后就不会被修改，所以不用担心它们被意外篡改:

$$
\text {const int DAYS} = 7;
$$

$$
\text {const char} * \text {MSGS[3]} = \{\text {"Yes", "No", Maybe"} \};
$$

保护性程序设计的黄金法则是:“按需知道”原则。尽量在函数内部解决该函数的任务，只共享那些需要共享的变量。除自动存储类别外，其他存储类别也很有用。不过，在使用某类别之前先要考虑一下是否有必要这样做。

## 12.2 随机数函数和静态变量

学习了不同存储类别的概念后，我们来看几个相关的程序。首先，来看一个使用内部链接的静态变量的函数:随机数函数。ANSI C库提供了rand()函数生成随机数。生成随机数有多种算法，ANSI C允许C实现针对特定机器使用最佳算法。然而，ANSI C标准还提供了一个可移植的标准算法，在不同系统中生成相同的随机数。实际上，rand()是“伪随机数生成器”，意思是可预测生成数字的实际序列。但是，数字在其取值范围内均匀分布。

为了看清楚程序内部的情况，我们使用可移植的ANSI版本，而不是编译器内置的rand()函数。可移植版本的方案开始于一个“种子”数字。该函数使用该种子生成新的数，这个新数又成为新的种子。然后，新种子可用于生成更新的种子，以此类推。该方案要行之有效，随机数函数必须记录它上一次被调用时所使用的种子。这里需要一个静态变量。程序清单12.7演示了版本0（稍后给出版本1）。

程序清单**12.7 rand0.c**函数文件

```c
/* rand0.c --生成随机数*/
/* 使用 ANSI C 可移植算法 */
static unsigned long int next = 1;  /* 种子  */
unsigned   int   rand0(void)
{
/* 生成伪随机数的魔术公式 */
next = next * 1103515245 + 12345;
return (unsigned   int) (next / 65536) % 32768;
```

```txt
}
```

在程序清单12.7中，静态变量next的初始值是1，其值在每次调用rand0()函数时都会被修改（通过魔术公式）。该函数是用于返回一个0～32767之间的值。注意，next是具有内部链接的静态变量（并非无链接）。这是为了方便稍后扩展本例，供同一个文件中的其他函数共享。

程序清单12.8是测试rand0()函数的一个简单的驱动程序。

程序清单**12.8 r\_drive0.c**驱动程序

/\* r\_drive0.c -- 测试 rand0()函数 \*/

/\* 与 rand0.c 一起编译\*/

```c
#include <stdio.h>

extern unsigned int rand0(void);

int main(void)

{

int count;

for (count = 0; count < 5; count++)

printf("%d\n", rand0());

return 0;

}
```

该程序也需要多文件编译。程序清单 12.7 和程序清单 12.8 分别使用一个文件。程序清单 12.8 中的extern关键字提醒读者rand0()被定义在其他文件中，在这个文件中不要求写出该函数原型。输出如下:

程序输出的数字看上去是随机的，再次运行程序后，输出如下:

看来，这两次的输出完全相同，这体现了“伪随机”的一个方面。每次主程序运行，都开始于相同的种子1。可以引入另一个函数srand1()重置种子来解决这个问题。关键是要让next成为只供rand1()和srand1()访问的内部链接静态变量（srand1()相当于C库中的srand()函数）。把srand1()加入rand1()所在的文件中。程序清单12.9给出了修改后的文件。

程序清单**12.9 s\_and\_r.c**文件程序

/\* s\_and\_r.c -- 包含 rand1() 和 srand1() 的文件 \*/

/\* 使用 ANSI C 可移植算法 \*/

static unsigned long int next = 1; /\* 种子 \*/