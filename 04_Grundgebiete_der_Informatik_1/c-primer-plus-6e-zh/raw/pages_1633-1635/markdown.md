season = (enum sample) 3; /\* C和C++都可以\*/

season++; /\* C可以，在C++中是一个错误 \*/

另外，在C++中，不使用关键字enum也可以声明枚举变量:

enum sample {sage, thyme, salt, pepper};

sample season; /\* C++可以，在C中不可以 \*/

与结构和联合的情况类似，如果一个变量和enum类型的同名会导致名称冲突。

## B.9.6 指向void的指针

C++可以把任意类型的指针赋给指向void的指针，这点与C相同。但是不同的是，只有使用显式强制类型转换才能把指向void的指针赋给其他类型的指针。下面的代码说明了这一点:

int ar[5] = {4, 5, 6,7, 8};

int \* pi;

void \* pv;

pv = ar; /\* C和C++都可以 \*/

pi = pv; /\* C可以，C++不可以 \*/

pi = (int \* ) pv; /\* C和C++都可以 \*/

C++与C的另一个区别是，C++可以把派生类对象的地址赋给基类指针，但是在C中没有这里涉及的特性。

## B.9.7 布尔类型

在C++中，布尔类型是bool，而且ture和false都是关键字。在C中，布尔类型是\_Bool，但是要包含stdbool.h头文件才可以使用bool、true和false。

## B.9.8 可选拼写

在C++中，可以用or来代替||，还有一些其他的可选拼写，它们都是关键字。在C99和C11中，这些可选拼写都被定义为宏，要包含iso646.h才能使用它们。

## B.9.9 宽字符支持

在C++中，wchar\_t是内置类型，而且wchar\_t是关键字。在C99和C11中，wchar\_t类型被定义在多个头文件中（stddef.h、stdlib.h、wchar.h、wctype.h）。与此类似，char16\_t和char32\_t都是C++11的关键字，但是在C11中它们都定义在uchar.h头文件中。

C++通过iostream头文件提供宽字符I/O支持（wchar\_t、char16\_t和char32\_t），而 C99通过wchar.h头文件提供一种完全不同的I/O支持包。

## B.9.10 复数类型

C++在complex头文件中提供一个复数类来支持复数类型。C有内置的复数类型，并通过complex.h头文件来支持。这两种方法区别很大，不兼容。C更关心数值计算社区提出的需求。

## B.9.11 内联函数

C99支持了C++的内联函数特性。但是，C99的实现更加灵活。在C++中，内联函数默认是内部链接。在 C++中，如果一个内联函数多次出现在多个文件中，该函数的定义必须相同，而且要使用相同的语言记号。例如，不允许在一个文件的定义中使用int类型形参，而在另一个文件的定义中使用int32\_t类型形参。即使用typedef把int32\_t定义为int也不能这样做。但是在C中可以这样做。另外，在第15章中介绍过，C允许混合使用内联定义和外部定义，而C++不允许。

## B.9.12 C++11中没有的C99/C11特性

虽然在过去C或多或少可以看作是C++的子集，但是C99标准增加了一些C++没有的新特性。下面列出了一些只有C99/C11中才有的特性:

指定初始化器；

复合初始化器（Compound initializer）；

受限指针（Restricted pointer）（即，restric指针）；

变长数组；

伸缩型数组成员；

带可变数量参数的宏。

注意

以上所列只是在特定时期内的情况，随着时间的推移和 C、C++的不断发展，列表中的项会有所增减。例如，C++14新增的一个特性就与C99的变长数组类似。

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">[1].也称为世界标准时间，简称UTC，从英文“Coordinated Universal Time”/法文“Temps Universel Cordonné”而来。中国内地的时间与UTC的时差为+8，也就是UTC+8。——译者注</span></small>

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">[2].fwide()函数用于设置流的定向，根据mode的不同值来执行不同的工作。译者注</span></small>