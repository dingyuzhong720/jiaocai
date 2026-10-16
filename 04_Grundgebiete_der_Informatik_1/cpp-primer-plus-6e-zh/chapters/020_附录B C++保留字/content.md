# 附录B C++保留字

原始 PDF 第 860–862 页。

# 附录 B C++保留字

C++保留了一些单词供自己和C++库使用。程序员不应将保留字用作声明中的标识符。保留字分三类:关键字、替代标记（alternative token）和C++库保留名称。

## B.1 C++关键字

关键字是组成编程语言词汇表的标识符，它们不能用于其他用途，如用作变量名。表 B.1 列出了 C++ 关键字，其中以粗体显示的关键字也是 ANSI C99 标准中的关键字，而以斜体显示的关键字是 C++11 新增的。

表 B.1 C++关键字

| alignas | -alignof | asm | auto- | bool- |
| --- | --- | --- | --- | --- |
| break | _case | catch | char | char16_t |
| char32_t | class | const | const_cast | constexpr |
| continue | decltype | default | delete | do |
| double- | dynamic_cast | else | enum | explicit |
| export | extern. | false | float | for |
| friend | goto | if | inline | int |
| long. | mutable | namespace | new | noexcept |
| nullptr | operator | private- | protected | public. |
| register- | reinterpret_cast | -return | short | signed |
| sizeof | static | static_assert | static_cast | struct |
| switch | -template | this | thread_local | throw |
| true | try | typedef | typeid | typename |
| union | unsigned | using | virtual | void |
| volatile | wchar_t | while |  |  |

## B.2 替代标记

除关键字外，C++还有一些运算符的字母替代表示，它们被称为替代标记。替代标记也被保留，表 B.2 列出了替代标记及其表示的运算符。

表 B.2 C++保留的替代标记及其含义

| 标记 | 含义 |
| --- | --- |
| and | &amp;&amp; |
| and_eq | &amp;= — |

---

附录 B C++保留字

843

续表

| 标记 | 含义 |
| --- | --- |
| bitand | &amp; |
| bitor | \| |
| compl | ~ |
| not | ! |
| not_eq | != |
| or | \|\| |
| or_eq | \|= |
| xor | ^ |
| xor_eq | ^= |

## B.3 C++库保留名称

编译器不允许程序员将关键字和替代标记用作名称。还有另一类禁止使用（但并非绝对不能用）的名称——保留名称，它们是保留给 C++ 库使用的名称。如果您将这种名称用作标识符，后果将是不确定的。也就是说，可能导致编译器错误、警告、程序不能正确运行或根本不会导致任何问题。

C++语言保留了库头文件中使用的宏名。如果程序包含某个头文件，则不应将该头文件（以及该头文件包含的头文件，依此类推）中定义的宏名用作其他目的。例如，如果您直接或间接地包含了头文件&lt;climits&gt;，则不应将CHAR\_BIT用作标识符，因为它已被用作该头文件中一个宏的名称。

C++语言保留了以两个下划线或下划线和大写字母打头的名称，还将以单个下划线打头的名称保留用作全局变量。因此，程序员不能在全局名称空间使用诸如\_\_gink、\_\_Lynx 和\_lynx 等名称。

C++语言保留了在库头文件中被声明为链接性为外部的名称。对于函数，这包括函数的特征标（名称和参数列表）。例如，假设有如下代码:

```cpp
#include <cmath>
using namespace std;
```

则函数特征标 tan（double）被保留。这意味着您的程序不应声明一个原型如下所示的函数:

```txt
int tan{double};  // don't do it
```

该原型确实与库函数  $\tan()$  的原型不同，因为后者的返回类型为 double，但特征标部分确实相同。然而，定义下面的原型是可以的:

```txt
char * tan(char *);  // ok
```

这是因为虽然其名称与库函数  $\tan()$  相同，但特征标不同。

## B.4 有特殊含义的标识符

C++社区讨厌新增关键字，因为它们可能与现有代码发生冲突。这就是标准委员会改变关键字 auto 的用法，并赋予其他关键字（如 virtual 和 delete）新用法的原因所在。C++11 提供了另一种避免新增关键字的机制，即使用具有特殊含义的标识符。这些标识符不是关键字，但用于实现语言功能。编译器根据上下文来判断它们是常规标识符还是用于实现语言功能:

```lisp
class F
{
    int final;                     // #1
public:
...
    virtual void unfold() {...} = final;  // #2
};
```

---

844

C++ Primer Plus（第6版）中文版

在上述代码中，语句#1中的final是一个常规标识符，而语句#2中的final使用了一种语言功能。这两种用法彼此不会冲突。

另外，C++还有很多经常出现在程序中，但不被保留的标识符。这包括头文件名、库函数名和 main（必不可少的函数的名称，程序从该函数开始执行）。只要不发生名称空间冲突，就可将这些标识符用于其他目的，但没有理由这样做。也就是说，完全可以编写下面的代码，但常识告诉您不应这样做:

```cpp
// allowable but silly
#include <iostream>
int iostream(int a);
int main ()
{
    std::
cout << iostream(5) << '\n';
    return 0;
}

int iostream(int a)
{
    int main = a + 1;
    int cout = a -1;
    return main*cout;
}
```
