```c
if (head == NULL)
printf("No data entered. ");
else
printf("Here is the movie list:\n");
current = head;
while (current != NULL)
{
printf("Movie: %s Rating: %d\n",
current->title, current->rating);
current = current->next;
}
/* 完成任务，释放已分配的内存 */
current = head;
while (current != NULL)
{
current = head;
head = current->next;
free(current);
}
```

```c
printf("Bye!\n");
return 0;
}
char * s_gets(char * st, int n)
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
continue; // 处理剩余输入行
}
return ret_val;
}
```

该程序用链表执行两个任务。第 1 个任务是，构造一个链表，把用户输入的数据储存在链表中。第 2个任务是，显示链表。显示链表的任务比较简单，所以我们先来讨论它。

## 1.显示链表

显示链表从设置一个指向第1个结构的指针（名为current）开始。由于头指针（名为head）已经指向链表中的第1个结构，所以可以用下面的代码来完成:

```txt
current = head;
```

然后，可以使用指针表示法访问结构的成员:

```txt
printf("Movie: %s Rating: %d\n", current->title, current->rating);
```

下一步是根据储存在该结构中next成员中的信息，重新设置current指针指向链表中的下一个结构。代码如下:

```txt
current = current->next;
```

完成这些之后，再重复整个过程。当显示到链表中最后一个项时，current 将被设置为 NULL，因为这是链表最后一个结构中next成员的值。

```c
while (current != NULL)
{
printf("Movie: %s Rating: %d\n", current->title, current->rating);
current = current->next;
}
```

遍历链表时，为何不直接使用head指针，而要重新创建一个新指针（current）？因为如果使用head会改变head中的值，程序就找不到链表的开

始处。

## 2.创建链表

创建链表涉及下面3步:

（1）使用malloc()为结构分配足够的空间；
（2）储存结构的地址；
（3）把当前信息拷贝到结构中。

如无必要不用创建一个结构，所以程序使用临时存储区（input数组）获取用户输入的电影名。如果用户通过键盘模拟EOF或输入一行空行，将退出下面的循环:

$$
\text {while (s\_gets(input, TSIZE) != NULL \&\& input[0] != '\0')}
$$

如果用户进行输入，程序就分配一个结构的空间，并将其地址赋给指针变量current:

$$
\text {current} = (\text {struct film} *) \text {malloc(sizeof(struct film))};
$$

链表中第1 个结构的地址应储存在指针变量head中。随后每个结构的地址应储存在其前一个结构的next成员中。因此，程序要知道它处理的是否是第1个结构。最简单的方法是在程序开始时，把head指针初始化为NULL。然后，程序可以使用head的值进行判断:

$$
\text {if (head == NULL) / * 第1个结构*}
$$

$$
\text {head} = \text {current};
$$

$$
\text {else} / * \text {subsequent structures} *
$$

$$
\text {prev-} > \text {next} = \text {current};
$$

在上面的代码中，指针prev指向上一次分配的结构。

接下来，必须为结构成员设置合适的值。尤其是，把next成员设置为NULL，表明当前结构是链表的最后一个结构。还要把input数组中的电影名拷贝到title成员中，而且要给rating成员提供一个值。如下代码所示:

```c
current->next = NULL;

strcpy(current->title, input);

puts("Enter your rating <0-10>:");

scanf("%d", &current->rating);
```

由于s\_gets()限制了只能输入TSIZE-1个字符，所以用strcpy()函数把input数组中的字符串拷贝到title成员很安全。

最后，要为下一次输入做好准备。尤其是，要设置 prev 指向当前结构。因为在用户输入下一部电影且程序为新结构分配空间后，当前结构将成为新结构的上一个结构，所以程序在循环末尾这样设置该指针:

```txt
prev = current;
```

程序是否能正常运行？下面是该程序的一个运行示例:

Enter first movie title:

## Spirited Away

Enter your rating <0-10>:

9

Enter next movie title (empty line to stop):

## The Duelists

Enter your rating <0-10>:

8

Enter next movie title (empty line to stop):

**Devil Dog: The Mound of Hound**

Enter your rating <0-10>:

1

Enter next movie title (empty line to stop):

Here is the movie list:

Movie: Spirited Away Rating: 9

Movie: The Duelists Rating: 8

Movie: Devil Dog: The Mound of Hound Rating: 1

Bye!

## 3.释放链表

在许多环境中，程序结束时都会自动释放malloc()分配的内存。但是，最好还是成对调用malloc()和free()。因此，程序在清理内存时为每个已分配的结构都调用了free()函数:

```c
current = head;

while (current != NULL)
{
current = head;
```

```txt
head = current->next;

free(current);

}
```

## 17.2.2 反思

films2.c 程序还有些不足。例如，程序没有检查 malloc()是否成功请求到内存，也无法删除链表中的项。这些不足可以弥补。例如，添加代码检查malloc()的返回值是否是NULL（返回NULL说明未获得所需内存）。如果程序要删除链表中的项，还要编写更多的代码。

这种用特定方法解决特定问题，并且在需要时才添加相关功能的编程方式通常不是最好的解决方案。另一方面，通常都无法预料程序要完成的所有任务。随着编程项目越来越大，一个程序员或编程团队事先计划好一切模式，越来越不现实。很多成功的大型程序都是由成功的小型程序逐步发展而来。

如果要修改程序，首先应该强调最初的设计，并简化其他细节。程序清单 17.2 中的程序示例没有遵循这个原则，它把概念模型和代码细节混在一起。例如，该程序的概念模型是在一个链表中添加项，但是程序却把一些细节（如，malloc()和 current->next 指针）放在最明显的位置，没有突出接口。如果程序能以某种方式强调给链表添加项，并隐藏具体的处理细节（如调用内存管理函数和设置指针）会更好。把用户接口和代码细节分开的程序，更容易理解和更新。学习下面的内容就可以实现这些目标。

## 17.3 抽象数据类型（ADT）

在编程时，应该根据编程问题匹配合适的数据类型。例如，用int类型代表你有多少双鞋，用float或 double 类型代表每双鞋的价格。在前面的电影示例中，数据构成了链表，每个链表项由电影名（C 字符串）和评级（一个int类型值）。C中没有与之匹配的基本类型，所以我们定义了一个结构代表单独的项，然后设计了一些方法把一系列结构构成一个链表。本质上，我们使用 C语言的功能设计了一种符合程序要求的新数据类型。但是，我们的做法并不系统。现在，我们用更系统的方法来定义数据类型。

什么是类型？类型特指两类信息:属性和操作。例如，int 类型的属性是它代表一个整数值，因此它共享整数的属性。允许对int类型进行算术操作是:改变int类型值的符号、两个int类型值相加、相减、相乘、相除、求模。当声明一个int类型的变量时，就表明了只能对该变量进行这些操作。

注意整数属性

C的int类型背后是一个更抽象的整数概念。数学家已经用正式的抽象方式定义了整数的属性。例如，假设N和M是整数，那么N+M=M+N；假设S、Q也是整数，如果N+M=S，而且N+Q=S，那么M=Q。可以认为数学家提供了整数的抽象概念，而C则实现了这一抽象概念。注意，实现整数的算术运算是表示整数必不可少的部分。如果只是储存值，并未在算术表达式中使用，int类型就没那么有用了。还要注意的是，C并未很好地实现整数。例如，整数是无穷大的数，但是2字节的int类型只能表示65536个整数。因此，不要混淆抽象概念和具体的实现。

假设要定义一个新的数据类型。首先，必须提供储存数据的方法，例如设计一个结构。其次，必须提供操控数据的方法。例如，考虑films2.c程序（程序清单17.2）。该程序用链接的结构来储存信息，而且通过代码实现了如何添加和显示信息。尽管如此，该程序并未清楚地表明正在创建一个新类型。我们应该怎么做？

计算机科学领域已开发了一种定义新类型的好方法，用3个步骤完成从抽象到具体的过程。

1.提供类型属性和相关操作的抽象描述。这些描述既不能依赖特定的实现，也不能依赖特定的编程语言。这种正式的抽象描述被称为抽象数据类型（ADT）。
2.开发一个实现 ADT 的编程接口。也就是说，指明如何储存数据和执行所需操作的函数。例如在 C中，可以提供结构定义和操控该结构的函数原型。这些作用于用户定义类型的函数相当于作用于 C基本类型的内置运算符。需要使用该新类型的程序员可以使用这个接口进行编程。
3.编写代码实现接口。这一步至关重要，但是使用该新类型的程序员无需了解具体的实现细节。

我们再次以前面的电影项目为例来熟悉这个过程，并用新方法重新完成这个示例。

## 17.3.1 建立抽象

从根本上看，电影项目所需的是一个项链表。每一项包含电影名和评级。你所需的操作是把新项添加到链表的末尾和显示链表中的内容。我们把需要处理这些需求的抽象类型叫作链表。链表具有哪些属性？首先，链表应该能储存一系列的项。也就是说，链表能储存多个项，而且这些项以某种方式排列，这样才能描述链表的第1项、第2项或最后一项。其次，链表类型应该提供一些操作，如在链表中添加新项。下面是链表的一些有用的操作:

初始化一个空链表；

在链表末尾添加一个新项；

确定链表是否为空；

确定链表是否已满；

确定链表中的项数；

访问链表中的每一项执行某些操作，如显示该项。

对该电影项目而言，暂时不需要其他操作。但是一般的链表还应包含以下操作:

在链表的任意位置插入一个项；

移除链表中的一个项；

在链表中检索一个项（不改变链表）；

用另一个项替换链表中的一个项；

在链表中搜索一个项。

非正式但抽象的链表定义是:链表是一个能储存一系列项且可以对其进行所需操作的数据对象。该定义既未说明链表中可以储存什么项，也未指定是用数组、结构还是其他数据形式来储存项，而且并未规定用什么方法来实现操作（如，查找链表中元素的个数）。这些细节都留给实现完成。

为了让示例尽量简单，我们采用一种简化的链表作为抽象数据类型。它只包含电影项目中的所需属性。该类型总结如下:

类型名: 简单链表

类型属性: 可以储存一系列项

类型操作: 初始化链表为空

确定链表为空

确定链表已满

确定链表中的项数

在链表末尾添加项

遍历链表，处理链表中的项

清空链表

下一步是为开发简单链表ADT开发一个C接口。

## 17.3.2 建立接口

这个简单链表的接口有两个部分。第1部分是描述如何表示数据，第2部分是描述实现ADT操作的函数。例如，要设计在链表中添加项的函数和报告链表中项数的函数。接口设计应尽量与ADT的描述保持一致。因此，应该用某种通用的Item类型而不是一些特殊类型，如int或struct film。可以用C的typedef功能来定义所需的Item类型:

#define TSIZE 45 /\* 储存电影名的数组大小 \*/

```txt
struct film

{

char title[TSIZE];

int rating;

};

typedef struct film Item;
```

然后，就可以在定义的其余部分使用 Item 类型。如果以后需要其他数据形式的链表，可以重新定义Item类型，不必更改其余的接口定义。

定义了 Item 之后，现在必须确定如何储存这种类型的项。实际上这一步属于实现步骤，但是现在决定好可以让示例更简单些。在films2.c程序中用链接的结构处理得很好，所以，我们在这里也采用相同的方法:

```c
typedef struct node
{
Item item;
struct node * next;
} Node;
typedef Node * List;
```

在链表的实现中，每一个链节叫作节点（node）。每个节点包含形成链表内容的信息和指向下一个节点的指针。为了强调这个术语，我们把node作为节点结构的标记名，并使用typedef把Node作为struct node结构的类型名。最后，为了管理链表，还需要一个指向链表开始处的指针，我们使用typedef把List作为该类型的指针名。因此，下面的声明:

List movies;

创建了该链表所需类型的指针movies。

这是否是定义List类型的唯一方法？不是。例如，还可以添加一个变量记录项数:

```c
typedef struct list
{
Node *head; /*指向链表头的指针 */
int size; /*链表中的项数 */
} List; /*List的另一种定义 */
```

可以像稍后的程序示例中那样，添加第2 个指针储存链表的末尾。现在，我们还是使用 List类型的第1种定义。这里要着重理解下面的声明创建了一个链表，而不一个指向节点的指针或一个结构:

List movies;

movies代表的确切数据应该是接口层次不可见的实现细节。

例如，程序启动后应把头指针初始化为NULL。但是，不要使用下面这样的代码:

```txt
movies = NULL;
```

为什么？因为稍后你会发现List类型的结构实现更好，所以应这样初始化:

```txt
movies.next = NULL;
movies.size = 0;
```

使用List的人都不用担心这些细节，只要能使用下面的代码就行:

InitializeList(movies);

使用该类型的程序员只需知道用InitializeList()函数来初始化链表，不必了解List类型变量的实现细节。这是数据隐藏的一个示例，数据隐藏是一种从编程的更高层次隐藏数据表示细节的艺术。

为了指导用户使用，可以在函数原型前面提供以下注释:

/\* 操作:初始化一个链表 \*/

/\* 前提条件:plist指向一个链表\*/

/\* 后置条件:该链表初始化为空 \*/

void InitializeList(List \* plist);

这里要注意3点。第1，注释中的“前提条件”（precondition）是调用该函数前应具备的条件。例如，需要一个待初始化的链表。第2，注释中的“后置条件”（postcondition）是执行完该函数后的情况。第3，该函数的参数是一个指向链表的指针，而不是一个链表。所以应该这样调用该函数:

InitializeList(&movies);

由于按值传递参数，所以该函数只能通过指向该变量的指针才能更改主调程序传入的变量。这里，由于语言的限制使得接口和抽象描述略有区别。

C 语言把所有类型和函数的信息集合成一个软件包的方法是:把类型定义和函数原型（包括前提条件和后置条件注释）放在一个头文件中。该文件应该提供程序员使用该类型所需的所有信息。程序清单 17.3给出了一个简单链表类型的头文件。该程序定义了一个特定的结构作为Item类型，然后根据Item定义了Node，再根据Node定义了List。然后，把表示链表操作的函数设计为接受Item类型和List类型的参数。如果函数要修改一个参数，那么该参数的类型应是指向相应类型的指针，而不是该类型。在头文件中，把组成函数名的每个单词的首字母大写，以这种方式表明这些函数是接口包的一部分。另外，该文件使用第16章介绍的#ifndef指令，防止多次包含一个文件。如果编译器不支持C99的bool类型，可以用下面的代码:

enum bool {false, true}; /\* 把bool定义为类型，false和true是该类型的值 \*/

替换下面的头文件:

#include &lt;stdbool.h&gt; /\* C99特性 \*/

程序清单**17.3 list.h**接口头文件

/\* list.h -- 简单链表类型的头文件 \*/

#ifndef LIST\_H\_

#define LIST\_H\_

#include &lt;stdbool.h&gt; /\* C99特性 \*/

/\* 特定程序的声明 \*/

#define TSIZE 45 /\* 储存电影名的数组大小 \*/

struct film

{

char title[TSIZE];

int rating;

/\* 一般类型定义 \*/

typedef struct film Item;

typedef struct node

{

Item item;

struct node \* next;

} Node;

typedef Node \* List;

/\* 函数原型 \*/

/\* 操作: 初始化一个链表 \*/

/\* 前提条件: plist指向一个链表 \*/

/\* 后置条件: 链表初始化为空 \*/

void InitializeList(List \* plist);

/\* 操作: 确定链表是否为空定义，plist指向一个已初始化的链表 \*/

/\* 后置条件: 如果链表为空，该函数返回true；否则返回false \*/

bool ListIsEmpty(const List \*plist);

/\* 操作: 确定链表是否已满，plist指向一个已初始化的链表 \*/

/\* 后置条件: 如果链表已满，该函数返回真；否则返回假 \*/

bool ListIsFull(const List \*plist);

/\* 操作: 确定链表中的项数, plist指向一个已初始化的链表 \*/

/\* 后置条件: 该函数返回链表中的项数 \*/

unsigned int ListItemCount(const List \*plist);

/\* 操作: 在链表的末尾添加项 \*/

/\* 前提条件: item是一个待添加至链表的项, plist指向一个已初始化的链表 \*/

/\* 后置条件: 如果可以，该函数在链表末尾添加一个项，且返回true；否则返回false \*/

bool AddItem(Item item, List \* plist);

/\* 操作: 把函数作用于链表中的每一项 \*/

/\* plist指向一个已初始化的链表 \*/

/\* pfun指向一个函数，该函数接受一个Item类型的参数，且无返回值 \*/

/\* 后置条件: pfun指向的函数作用于链表中的每一项一次 \*/

void Traverse(const List \*plist, void(\*pfun)(Item item));

/\* 操作: 释放已分配的内存（如果有的话） \*/

/\* plist指向一个已初始化的链表 \*/

/\* 后置条件: 释放了为链表分配的所有内存，链表设置为空 \*/

void EmptyTheList(List \* plist); #endif

只有InitializeList()、AddItem()和EmptyTheList()函数要修改链表，因此从技术角度看，这些函数需要一个指针参数。然而，如果某些函数接受 List 类型的变量作为参数，而其他函数却接受 List类型的地址作为参数，用户会很困惑。因此，为了减轻用户的负担，所有的函数均使用指针参数。

头文件中的一个函数原型比其他原型复杂:

/\* 操作: 把函数作用于链表中的每一项 \*/

/\* plist指向一个已初始化的链表 \*/

/\* pfun指向一个函数，该函数接受一个Item类型的参数，且无返回值 \*/

/\* 后置条件: pfun指向的函数作用于链表中的每一项一次 \*/

void Traverse(const List \*plist, void(\*pfun)(Item item));

参数pfun是一个指向函数的指针，它指向的函数接受item值且无返回值。第14章中介绍过，可以把函数指针作为参数传递给另一个函数，然后该函数就可以使用这个被指针指向的函数。例如，该例中可以让pfun指向显示链表项的函数。然后把Traverse()函数把该函数作用于链表中的每一项，显示链表中的内容。

## 17.3.3 使用接口

我们的目标是，使用这个接口编写程序，但是不必知道具体的实现细节（如，不知道函数的实现细节）。在编写具体函数之前，我们先编写电影程序的一个新版本。由于接口要使用List和Item类型，所以该程序也应使用这些类型。下面是编写该程序的一个伪代码方案。

创建一个List类型的变量。

创建一个Item类型的变量。

初始化链表为空。

当链表未满且有输入时:

把输入读取到Item类型的变量中。

在链表末尾添加项。

访问链表中的每个项并显示它们。

程序清单 17.4 中的程序按照以上伪代码来编写，其中还加入了一些错误检查。注意该程序利用了list.h（程序清单 17.3）中描述的接口。另外，还需注意，链表中含有 showmovies()函数的代码，它与Traverse()的原型一致。因此，程序可以把指针showmovies传递给Traverse()，这样Traverse()可以把showmovies()函数应用于链表中的每一项（回忆一下，函数名是指向该函数的指针）。

程序清单**17.4 films3.c**程序

/\* films3.c -- 使用抽象数据类型（ADT）风格的链表 \*/

/\* 与list.c一起编译 \*/

#include &lt;stdio.h&gt;

#include &lt;stdlib.h&gt; /\* 提供exit()的原型 \*/

#include "list.h" /\* 定义List、Item \*/

void showmovies(Item item);

char \* s\_gets(char \* st, int n);

```c
int main(void)
{
List movies;
Item temp;
/* 初始化 */
InitializeList(&movies);
if (ListIsFull(&movies))
{
fprintf(stderr, "No memory available! Bye!\n");
exit(1);
}
/* 获取用户输入并储存 */
puts("Enter first movie title:");
while (s_gets(temp.title, TSIZE) != NULL && temp.title[0] != '\0')
{
puts("Enter your rating <0-10>:");
scanf("%d", &temp.rating);
while (getchar() != '\n')
```

```c
continue;

if (AddItem(temp, &movies) == false)
{
fprintf(stderr, "Problem allocating memory\n");
break;
}
if (ListIsFull(&movies))
{
puts("The list is now full.");
break;
}
puts("Enter next movie title (empty line to stop):");
}
/* 显示 */
if (ListIsEmpty(&movies))
printf("No data entered. ");
else
{
printf("Here is the movie list:\n");
```

```c
Traverse(&movies, showmovies);
}
printf("You entered %d movies.\n", ListItemCount(&movies));
/* 清理 */
EmptyTheList(&movies);
printf("Bye!\n");
return 0;
}
void showmovies(Item item)
{
printf("Movie: %s Rating: %d\n", item.title,
item.rating);
}
char * s_gets(char * st, int n)
{
char * ret_val;
char * find;
ret_val = fgets(st, n, stdin);
if (ret_val)
```

```c
{
find = strchr(st, '\n');      // 查找换行符
if (find)                          // 如果地址不是NULL,
*find = '\0';          // 在此处放置一个空字符
else
while  (getchar() !=  '\n')
continue;                 // 处理输入行的剩余内容
}
return  ret_val;
}
```

## 17.3.4 实现接口

当然，我们还是必须实现List接口。C方法是把函数定义统一放在list.c文件中。然后，整个程序由 list.h（定义数据结构和提供用户接口的原型）、list.c（提供函数代码实现接口）和 films3.c （把链表接口应用于特定编程问题的源代码文件）组成。程序清单17.5演示了list.c的一种实现。要运行该程序，必须把films3.c和list.c一起编译和链接（可以复习一下第9章关于编译多文件程序的内容）。list.h、list.c和films3.c组成了整个程序（见图17.5）。

程序清单**17.5 list.c**实现文件

/\* list.c -- 支持链表操作的函数 \*/

#include &lt;stdio.h&gt;

#include &lt;stdlib.h&gt;

#include "list.h"

/\* 局部函数原型 \*/

static void CopyToNode(Item item, Node \* pnode);

/\* 接口函数 \*/

/\* 把链表设置为空 \*/

void InitializeList(List \* plist)

\*plist = NULL;

}

/\* 如果链表为空，返回true \*/

bool ListIsEmpty(const List \* plist)

{

if (\*plist == NULL)

return true;

else

return false;

}

/\* 如果链表已满，返回true \*/

```c
bool ListIsFull(const List * plist)
{
Node * pt;
bool  full;
pt = (Node *)malloc(sizeof(Node));
if (pt == NULL)
full = true;
else
full = false;
free(pt);
return  full;
}
/* 返回节点的数量 */
unsigned int ListItemCount(const List * plist)
{
unsigned  int  count = 0;
Node * pnode = *plist;  /* 设置链表的开始 */
while (pnode != NULL)
{
```

```c
++count;

pnode = pnode->next;  /* 设置下一个节点 */

}

return count;

}

/* 创建储存项的节点，并将其添加至由plist指向的链表末尾（较慢的实现） */

bool AddItem(Item item, List * plist)

{

Node * pnew;

Node * scan = *plist;

pnew = (Node *) malloc(sizeof(Node));

if (pnew == NULL)

return false;    /* 失败时退出函数 */

CopyToNode(item, pnew);

pnew->next = NULL;

if (scan == NULL)          /* 空链表，所以把 */
*plist = pnew;      /* pnew放在链表的开头 */

else
```

```c
{
while (scan->next != NULL)
scan = scan->next; /* 找到链表的末尾 */
scan->next = pnew; /* 把pnew添加到链表的末尾 */
}
return true;
}
/* 访问每个节点并执行pfun指向的函数 */
void Traverse(const List * plist, void(*pfun)(Item item))
{
Node * pnode = *plist; /* 设置链表的开始 */
while (pnode != NULL)
{
(*pfun)(pnode->item); /* 把函数应用于链表中的项 */
pnode = pnode->next; /* 前进到下一项 */
}
}
/* 释放由malloc()分配的内存 */
/* 设置链表指针为NULL */
```

```c
void EmptyTheList(List * plist)
{
Node * psave;
while (*plist != NULL)
{
psave = (*plist)->next;      /* 保存下一个节点的地址   */
free(*plist);                  /* 释放当前节点          */
*plist = psave;              /* 前进至下一个节点     */
}
}
/* 局部函数定义 */
/* 把一个项拷贝到节点中 */
static void CopyToNode(Item item, Node * pnode)
{
pnode->item = item;  /* 拷贝结构 */
}
```

```c
list.h
/* list.h--简单链表类型的头文件 */
/* 特定的程序声明 */
#define TSIZE 45/* 储存电影名的数组大小 */
struct film
{
    char title[TSIZE];
    int rating;
};
.
.
.
void Traverse (List 1, void (* pfun)(Item item) );
```

```c
list.c
/* list.c--支持链表操作的函数 */
#include<stdio.h>
#include<stdlib.h>
#include "list.h"
.
.
.
/* 把一个项拷贝到节点中 */
static void CopyToNode (Item item, Node * pnode)
{
pnode->item = item; /* 拷贝结构 */
}
```

```c
films3.c
/* films3.c--使用抽象数据类型(ADT)风格的链表 */
#include <stdio.h>
#include <stdlib.h>/*提供exit()的原型*/
#include "list.h"
void showmovies(Item item);

int main(void)
{
.
.
.
}
}
```

图17.5 电影程序的3个部分

## 1.程序的一些注释

list.c文件有几个需要注意的地方。首先，该文件演示了什么情况下使用内部链接函数。如第12章所述，具有内部链接的函数只能在其声明所在的文件夹可见。在实现接口时，有时编写一个辅助函数（不作为正式接口的一部分）很方便。例如，使用CopyToNode()函数把一个Item类型的值拷贝到Item类型的变量中。由于该函数是实现的一部分，但不是接口的一部分，所以我们使用 static 存储类别说明符把它隐藏在list.c文件中。接下来，讨论其他函数。

InitializeList()函数将链表初始化为空。在我们的实现中，这意味着把List类型的变量设置为NULL。前面提到过，这要求把指向List类型变量的指针传递给该函数。

ListIsEmpty()函数很简单，但是它的前提条件是，当链表为空时，链表变量被设置为NULL。因此，在首次调用 ListIsEmpty()函数之前初始化链表非常重要。另外，如果要扩展接口添加删除项的功能，那么当最后一个项被删除时，应该确保该删除函数重置链表为空。对链表而言，链表的大小取决于可用内存量。ListIsFull()函数尝试为新项分配空间。如果分配失败，说明链表已满；如果分配成功，则必须释放刚才分配的内存供真正的项所用。

ListItemCount()函数使用常用的链表算法遍历链表，同时统计链表中的项:

```c
unsigned int ListItemCount(const List * plist)
{
unsigned  int  count = 0;
Node * pnode = *plist;  /* 设置链表的开始 */
while (pnode != NULL)
{
++count;
```

```c
pnode = pnode->next;  /* 设置下一个节点 */
}
return count;
}
AddItem()函数是这些函数中最复杂的:
bool AddItem(Item item, List * plist)
{
Node * pnew;
Node * scan = *plist;
pnew = (Node *) malloc(sizeof(Node));
if (pnew == NULL)
return false;                 /* 失败时退出函数 */
CopyToNode(item, pnew);
pnew->next = NULL;
if (scan == NULL)             /* 空链表，所以把 */
*plist = pnew;              /* pnew放在链表的开头 */
else
{
while (scan->next != NULL)
```

```txt
scan = scan->next; /* 找到链表的末尾 */

scan->next = pnew;      /* 把pnew添加到链表的末尾 */

}
return  true;

}
```

AddItem()函数首先为新节点分配空间。如果分配成功，该函数使用CopyToNode()把项拷贝到新节点中。然后把该节点的next成员设置为NULL。这表明该节点是链表中的最后一个节点。最后，完成创建节点并为其成员赋正确的值之后，该函数把该节点添加到链表的末尾。如果该项是添加到链表的第 1 个项，需要把头指针设置为指向第1项（记住，头指针的地址是传递给AddItem()函数的第2个参数，所以\*plist就是头指针的值）。否则，代码继续在链表中前进，直到发现被设置为NULL的next成员。此时，该节点就是当前的最后一个节点，所以，函数重置它的next成员指向新节点。

要养成良好的编程习惯，给链表添加项之前应调用ListIsFull()函数。但是，用户可能并未这样做，所以在AddItem()函数内部检查malloc()是否分配成功。而且，用户还可能在调用ListIsFull()和调用AddItem()函数之间做其他事情分配了内存，所以最好还是检查malloc()是否分配成功。

Traverse()函数与ListItemCount()函数类似，不过它还把一个指针函数作用于链表中的每一项。

```c
void Traverse (const List * plist, void (* pfun)(Item item) )
{
Node * pnode = *plist; /* 设置链表的开始 */
while (pnode != NULL)
```