wctype()函数的有效参数名即是宽字符分类函数名去掉 isw 前缀。例如，wctype("alpha")表示的是 iswalpha()函数判断的字符类别。因此，调用iswctype(wc, wctype("alpha"))相当于调用iswalpha(wc)，唯一的区别是前者使用LC\_CTYPE类别进行分类。

该库还有4个与转换相关的函数。其中有两个函数分别与ctype.h库中toupper()和tolower()相对应。第3个函数是一个可扩展的版本，通过本地化的LC\_CTYPE设置确定字符是大写还是小写。第4个函数为第3个函数提供合适的分类参数。表B.5.54列出了这些函数。

表B.5.54 宽字符转换函数

| 原型 | 描述 |
| --- | --- |
| wint_t towlower(wint_t wc); | 如果wc是大写字符,返回其小写形式;否则返回wc |
| wint_t towupper(wint_t wc); | 如果wc是小写字符,返回其大写形式;否则返回wc |
| wint_t towctrans(wint_t wc, wctrans_t desc); | 如果desc等于wctrans("lower")的返回值,函数返回wc的小写形式(由LC_CTYPE设置确定);如果dest等于wctrans("upper")的返回值,函数返回wc的大写形式(由LC_CTYPE设置确定) |
| wctrans_t wctrans(const char*property); | 如果参数是"lower"或"upper",函数返回一个wctrans_t类型的值,可用作towctrans()的参数并反映LC_CTYPE设置,否则函数返回0 |

## B.6 参考资料VI:扩展的整数类型

第3章介绍过，C99的inttypes.h头文件为不同的整数类型提供一套系统的别名。这些名称与标准名称相比，能更清楚地描述类型的性质。例如，int类型可能是16位、32位或64位，但是int32\_t类型一定是32位。

更精确地说，inttypes.h头文件定义的一些宏可用于scanf()和printf()函数中读写这些类型的整数。inttypes.h头文件包含的stdlib.h头文件提供实际的类型定义。格式化宏可以与其他字符串拼接起来形成合适格式化的字符串。

该头文件中的类型都使用typedef定义。例如，32位系统的int可能使用这样的定义:

typedef int int32\_t;

用#define指令定义转换说明。例如，使用之前定义的int32\_t的系统可以这样定义:

#define PRId32 "d" // 输出说明符

#define SCNd32 "d" // 输入说明符

使用这些定义，可以声明扩展的整型变量、输入一个值和显示该值:

int32\_t cd\_sales; // 32位整数类型

scanf("%" SCNd32, &cd\_sales);

printf("CD sales = %10" PRId32 " units\n", cd\_sales);

如果需要，可以把字符串拼接起得到最终的格式字符串。因此，上面的代码可以这样写:

int cd\_sales; // 32位整数类型

scanf("%d", &cd\_sales);

printf("CD sales = %10d units\n", cd\_sales);

如果把原始代码移植到16位int的系统中，该系统可能把int32\_t定义为long，把PRId32定义为"ld"。但是，仍可以使用相同的代码，只要知道系统使用的是32位整型即可。

该参考资料的其余部分列出了扩展类型、转换说明以及表示类型限制的宏。

## B.6.1 精确宽度类型

typedef标识了一组精确宽度的类型，通用形式是intN\_t（有符号类型）和uintN\_t（无符号类型），其中N表示位数（即类型的宽度）。但是要注意，不是所有的系统都支持所有的这些类型。例如，最小可用内存大小是16位的系统就不支持int8\_t和uint8\_t类型。格式宏可以使用d或i表示有符号类型，所以PRIi8和SCNi8都有效。对于无符号类型，可以使用o、x或u以获得%o、%x或%X转换说明来代替%u。例如，可以使用PRIX32以十六进制格式打印uint32\_t类型的值。表B.6.1列出了精确宽度类型、格式说明符和最小值、最大值。

表B.6.1 精确宽度类型

| 类型名 | printf()说明符 | scanf()说明符 | 最小值 | 最大值 |
| --- | --- | --- | --- | --- |
| int8_t | PRId8 | SCNd8 | INT8_MIN | INT8_MAX |
| int16_t | PRId16 | SCNd16 | INT16_MIN | INT16_MAX |
| int32_t | PRId32 | SCNd32 | INT32_MIN | INT32_MAX |
| int64_t | PRId64 | SCNd64 | INT64_MIN | INT64_MAX |
| uint8_t | PRIu8 | SCNu8 | 0 | UINT8_MAX |
| uint16_t | PRIu16 | SCNu16 | 0 | UINT16_MAX |
| uint32_t | PRIu32 | SCNu32 | 0 | UINT32_MAX |
| uint64_t | PRIu64 | SCNu64 | 0 | UINT64_MAX |

## B.6.2 最小宽度类型

最小宽度类型保证一种类型的大小至少是某位。这些类型一定存在。例如，不支持 8 位单元的系统可以把int\_least\_8定义为16位类型。表B.6.2列出了最小宽度类型、格式说明符和最小值、最大值。

表B.6.2 最小宽度类型

| 类型名 | printf()说明符 | scanf()说明符 | 最小值 | 最大值 |
| --- | --- | --- | --- | --- |
| int_least8_t | PRILEASTd8 | SCNLEASTd8 | INT_LEAST8_MIN | INT_LEAST8_MAX |
| int_least16_t | PRILEASTd16 | SCNLEASTd16 | INT_LEAST16_MIN | INT_LEAST16_MAX |
| int_least32_t | PRILEASTd32 | SCNLEASTd32 | INT_LEAST32_MIN | INT_LEAST32_MAX |
| int_least64_t | PRILEASTd64 | SCNLEASTd64 | INT_LEAST64_MIN | INT_LEAST64_MAX |
| uint_least8_t | PRILEASTu8 | SCNLEASTu8 | 0 | UINT_LEAST8_MAX |
| uint_least16_t | PRILEASTu16 | SCNLEASTu16 | 0 | UINT_LEAST16_MAX |
| uint_least32_t | PRILEASTu32 | SCNLEASTu32 | 0 | UINT_LEAST32_MAX |
| uint_least64_t | PRILEASTu64 | SCNLEASTu64 | 0 | UINT_LEAST64_MAX |

## B.6.3 最快最小宽度类型

对于特定的系统，用特定的整型更快。例如，在某些实现中int\_least16\_t可能是short，但是系统在进行算术运算时用int类型会更快些。因此，inttypes.h还定义了表示为某位数的最快类型。这些类型一定存在。在某些情况下，可能并未明确指定哪种类型最快，此时系统会简单地选择其中的一种。表B.6.3列出了最快最小宽度类型、格式说明符和最小值、最大值。

表B.6.3 最快最小宽度类型

| 类型名 | printf()说明符 | scanf()说明符 | 最小值 | 最大值 |
| --- | --- | --- | --- | --- |
| int_fast8_t | PRIFASTd8 | SCNFASTd8 | INT_FAST8_MIN | INT_FAST8_MAX |
| int_fast16_t | PRIFASTd16 | SCNFASTd16 | INT_FAST16_MIN | INT_FAST16_MAX |
| int_fast32_t | PRIFASTd32 | SCNFASTd32 | INT_FAST32_MIN | INT_FAST32_MAX |
| int_fast64_t | PRIFASTd64 | SCNFASTd64 | INT_FAST64_MIN | INT_FAST64_MAX |
| uint_fast8_t | PRIFASTu8 | SCNFASTu8 | 0 | UINT_FAST8_MAX |
| uint_fast16_t | PRIFASTu16 | SCNFASTu16 | 0 | UINT_FAST16_MAX |
| uint_fast32_t | PRIFASTu32 | SCNFASTu32 | 0 | UINT_FAST32_MAX |
| uint_fast64_t | PRIFASTu64 | SCNFASTu64 | 0 | UINT_FAST64_MAX |

## B.6.4 最大宽度类型

有些情况下要使用最大整数类型，表B.6.4列出了这些类型。实际上，由于系统可能会提供比所需类型更大宽度的类型，因此这些类型的宽度可能比long long或unsigned long long更大。

表B.6.4 最大宽度类型

| 类型名 | printf()说明符 | scanf()说明符 | 最小值 | 最大值 |
| --- | --- | --- | --- | --- |
| intmax_t | PRIdMAX | SCNdMAX | INTMAX_MIN | INTMAX_MAX |
| uintmax_t | PRIuMAX | SCBuMAX | 0 | UINTMAX_MAX |

## B.6.5 可储存指针值的整型

inttypes.h头文件（通过包含stdint.h即可包含该头文件）定义了两种整数类型，可精确地储存指针值，见表B.6.5。

表B.6.5 可储存指针值的整数类型

| 类型名 | printf()说明符 | scanf()说明符 | 最小值 | 最大值 |
| --- | --- | --- | --- | --- |
| intptr_t | PRIdPTR | SCNdPTR | INTPTR_MIN | INTPTR_MAX |
| uintptr_t | PRIuPTR | SCBuPTR | 0 | UINTPTR_MAX |

## B.6.6 扩展的整型常量

在整数后面加上L后缀可表示long类型的常量，如445566L。如何表示int32\_t类型的常量？要使用inttypes.h头文件中定义的宏。例如，表达式INT32\_C(445566)展开为一个int32\_t类型的常量。从本质上看，这种宏相当于把当前类型强制转换成底层类型，即特殊实现中表示int32\_t类型的基本类型。

宏名是把相应类型名中的\_C 用\_t 替换，再把名称中所有的字母大写。例如，要把 1000 设置为unit\_least64\_t类型的常量，可以使用表达式UNIT\_LEAST64\_C(1000)。

## B.7 参考资料VII:扩展字符支持

C 语言最初并不是作为国际编程语言设计的，其字符的选择或多或少是基于标准的美国键盘。但是，随着后来C在世界范围内越来越流行，不得不扩展来支持不同且更大的字符集。这部分参考资料概括介绍了一些相关内容。

## B.7.1 三字符序列

有些键盘没有C中使用的所有符号，因此C提供了一些由三个字符组成的序列（即三字符序列）作为这些符号的替换表示。如表B.7.1所示。

表B.7.1 三字符序列

| 三字符序列 | 符号 | 三字符序列 | 符号 | 三字符序列 | 符号 |
| --- | --- | --- | --- | --- | --- |
| ??= | # | ??( | [ | ??/ | \\ |
| ??) | ] | ??' | ^ | ??&lt; | { |
| ??! | \| | ???> | } | ??- | ~ |

C替换了源代码文件中的这些三字符序列，即使它们在双引号中也是如此。因此，下面的代码:

```txt
??=include <stdio.h>

??=define LIM 100

int main()

??

int q??(LIM??);

printf("More to come.??/n");

...
```

```txt
??>
```

会变成这样:

```c
#include <stdio.h>

#define LIM 100

int main()
{
int q[LIM];
printf("More to come.\n");
...
}
```

当然，要在编译器中设置相关选项才能激活这个特性。

## B.7.2 双字符

意识到三字符系统很笨拙，C99提供了双字符（digraph），可以使用它们来替换某些标准C标点符号。

表B.7.2 双字符

| 双字符 | 符号 | 双字符 | 符号 | 双字符 | 符号 |
| --- | --- | --- | --- | --- | --- |
| &lt;: | [ | :> | ] | &lt;% | { |
| %> | } | %: | # | %:%: | ## |

与三字符不同的是，不会替换双引号中的双字符。因此，下面的代码:

```txt
%:include <stdio.h>

%:define LIM 100
```

```c
int main()
<%
int q<:LIM:>;
printf("More to come.:>");
...
%>
会变成这样:
#include <stdio.h>
#define LIM 100
int main()
{
int q[LIM];
printf("More to come.:>");
// :>是字符串的一部分
...
}
// :>与 }相同
```

## B.7.3 可选拼写:iso646.h

使用三字符序列可以把||运算符写成??!??!，这看上去比较混乱。C99 通过iso646.h头文件（参考资料V中的表B.5.11）提供了可展开为运算符的宏。C标准把这些宏称为可选拼写（alternative spelling）。

如果包含了iso646.h头文件，以下代码:

$$
\text {if} (\mathrm{x} = = \mathrm{M1} \text {or} \mathrm{x} = = \mathrm{M2})
$$

$$
\mathrm {x and\_eq 0XFF};
$$

可展开为下面的代码:

$$
\text {if} (\mathrm{x} = = \mathrm{M1} \| \mathrm{x} = = \mathrm{M2})
$$

$$
\mathrm{x} \& = 0 \mathrm{XFF};
$$

## B.7.4 多字节字符

C 标准把多字节字符描述为一个或多个字节的序列，表示源环境或执行环境中的扩展字符集成员。源环境指的是编写源代码的环境，执行环境指的是用户运行已编译程序的环境。这两个环境不同。例如，可以在一个环境中开发程序，在另一个环境中运行该程序。扩展字符集是C语言所需的基本字符集的超集。

有些实现会提供扩展字符集，方便用户通过键盘输入与基本字符集不对应的字符。这些字符可用于字符串字面量和字符常量中，也可出现在文件中。有些实现会提供与基本字符集等效的多字节字符，可替换三字符和双字符。

例如，德国的一个实现也许会允许用户在字符串中使用日耳曼元音变音字符:

一般而言，程序可使用的扩展字符集因本地化设置而异。

## B.7.5 通用字符名（UCN）

多字节字符可以用在字符串中，但是不能用在标识符中。C99新增了通用字符名（UCN），允许用户在标识名中使用扩展字符集中的字符。系统扩展了转义序列的概念，允许编码ISO/IEC 10646标准中的字符。该标准由国际标准化组织（ISO）和国际电工技术委员会（IEC）共同制定，为大量的字符提供数值码。10646标准和统一码（Unicode）关系密切。

有两种形式的UCN序列。第1种形式是\u hexquard，其中hexquard是一个4位的十六进制数序列（如，\u00F6）。第 2种形式是\U hexquardhexquard，如\U0000AC01。因为十六进制每一位上的数对应4位，\u形式可用于16位整数表示的编码，\U形式可用于32位整数表示的编码。

如果系统实现了UCN，而且包含了扩展字符集中所需的字符，就可以在字符串、字符常量和标识符中使用UCN:

$$
\text {wchar\_t value} \backslash \mathrm{u00F6} \backslash \mathrm{u00F8} = \mathrm{L} ^ {\prime} \backslash \mathrm{u00f6} ^ {\prime};
$$

统一码和**ISO 10646**

统一码为表示不同的字符集提供了一种解决方案，可以根据类型为大量字符和符号制定标准的编号系统。例如，ASCII码被合并为统一码的子集，因此美国拉丁字符（如A～Z）在这两个系统中的编码相同。但是，统一码还合并了其他拉丁字符（如，欧洲语言中使用的一些字符）和其他语言中的字符，包括希腊文、西里尔字母、希伯来文、切罗基文、阿拉伯文、泰文、孟加拉文和形意文字（如中文和日文）。到目前为止，统一码表示的符号超过了 110000个，而且仍在发展中。欲了解更多细节，请查阅统一码联合站点:www.unicode.org。

统一码为每个字符分配一个数字，这个数字称为代码点（code point）。典型的统一码代码点类似:U-222B。U表示该字符是统一字符，222B是表示该字符的一个十六进制数，在这种情况下，表示积分号。

国际标准化组织（ISO）组建了一个团队开发ISO 10646和标准编码的多语言文本。ISO 10646团队和统一码团队从1991年开始合作，一直保持两个标准的相互协调。

## B.7.6 宽字符

C99为使用宽字符提供更多支持，通过wchar.h和wctype.h库包含了更多大型字符集。这两个头文件把wchar\_t定义为一种整型类型，其确切的类型依赖实现。该类型用于储存扩展字符集中的字符，扩展字符集是是基本字符集的超集。根据定义，char类型足够处理基本字符集，而wchar\_t类型则需要更多位才能储存更大范围的编码值。例如，char 可能是 8 位字节，wchar\_t可能是 16 位的 unsigned short。

用L前缀标识宽字符常量和字符串字面量，用%lc和%ls显示宽字符数据:

```c
wchar_t wch = L'I';
wchar_t w_arr[20] = L"am wide!";
printf("%lc %ls\n", wch, w_arr);
```

例如，如果把wchar\_t实现为2字节单元，'I'的1字节编码应储存在wch的低位字节。不是标准字符集中的字符可能需要两个字节储存字符编码。例如，可以使用通用字符编码表示超出 char 类型范围的字符编码:

```javascript
wchar_t w = L'\u00E2'; /* 16位编码值 */
```

内含 wchar\_t 类型值的数组可用于储存宽字符串，每个元素储存一个宽字符编码。编码值为 0 的wchar\_t值是空字符的wchar\_t类型等价字符。该字符被称为空宽字符（null wide character），用于表示宽字符串的结尾。

可以使用%lc和%ls读取宽字符:

```txt
wchar_t wch1;

wchar_t w_arr[20];

puts("Enter your grade:

scanf("%lc", &wch1);
```

puts("Enter your first name:");

scanf("%ls",w\_arr);

wchar\_t头文件为宽字符提供更多支持，特别是提供了宽字符I/O函数、宽字符转换函数和宽字符串控制函数。例如，可以用fwprintf()和wprintf()函数输出，用fwscanf()和wscanf()函数输入。与一般输入/输出函数的主要区别是，这些函数需要宽字符格式字符串，处理的是宽字符输入/输出流。例如，下面的代码把信息作为宽字符显示:

wchar\_t \* pw = L"Points to a wide-character string";

int dozen = 12;

wprintf(L"Item %d: %ls\n", dozen, pw);

类似地，还有getwchar()、putwchar()、fgetws()和fputws()函数。wchar\_t头文件定义了一个WEOF宏，与EOF在面向字节的I/O中起的作用相同。该宏要求其值是一个与任何有效字符都不对应的值。因为wchar\_t类型的值都有可能是有效字符，所以wchar\_t库定义了一个wint\_t类型，包含了所有wchar\_t类型的值和WEOF的值。

该库中还有与string.h库等价的函数。例如，wcscpy(ws1, ws2)把ws1指定的宽字符串拷贝到ws2指向的宽字符数组中。类似地，wcscmp()函数比较宽字符串，等等。

wctype.h头文件新增了字符分类函数，例如，如果iswdigit()函数的宽字符参数是数字，则返回真；如果iswblank()函数的参数是空白，则返回真。空白的标准值是空格和水平制表符，分别写作L''和L'\t'。

C11标准通过uchar.h头文件为宽字符提供更多支持，为匹配两种常用的统一码格式，定义了两个新类型。第1种类型是char16\_t，可储存一个16位编码，是可用的最小无符号整数类型，用于hexquard UCN形式和统一码UTF-16编码方案。

$$
\mathrm{char16\_t} = ^ {\prime} \backslash \mathrm{u00F6} ^ {\prime};
$$

第2种类型是char32\_t，可储存一个32位编码，最小的可用无符号整数类型，。可用于hexquard UCN形式和统一码UTF-32编码方案

$$
\mathrm {char32\_t = '\U0000AC01';}
$$

前缀u和U分别表示char16\_t和char32\_t字符串。

$$
\text {char16\_t ws16[11]} = \mathrm{u}" \text {Tannh} \backslash \mathrm{u00E4user}";
$$

$$
\text {char32\_t ws32[13] = U''caf\U000000E9 au lait''};
$$

注意，这两种类型比wchar\_t类型更具体。例如，在一个系统中，wchar\_t可以储存32位编码，但是在另一个系统中也许只能储存16位的编码。另外，这两种新类型都与C++兼容。

## B.7.7 宽字符和多字节字符

宽字符和多字节字符是处理扩展字符集的两种不同的方法。例如，多字节字符可能是一个字节、两个字节、三个字节或更多字节，而所有的宽字符都只有一个宽度。多字节字符可能使用移位状态（移位状态是一个字节，确定如何解释后续字节）；而宽字符没有移位状态。可以把多字节字符的文件读入使用标准输入函数的普通char类型数组，把宽字节的文件读入使用宽字符输入函数的宽字节数组。

C99 在wchar.h库中提供了一些函数，用于多字节和宽字节之间的转换。mbrtowc()函数把多字节字符转换为宽字符，wcrtomb()函数把宽字符转换为多字节字符。类似地，mbstrtowcs()函数把多字节字符串转换为宽字节字符串，wcstrtombs()函数把宽字节字符串转换为多字节字符串。

C11在uchar.h库中提供了一些函数，用于多字节和char16\_t之间的转换，以及多字节和char32\_t之间的转换。

## B.8 参考资料VIII:C99/C11数值计算增强

过去，FORTRAN是数值科学计算和工程计算的首选语言。C90使C的计算方法更接近于FORTRAN。例如，float.h中使用的浮点特性规范都是基于FORTRAN标准委员会开发的模型。C99和C11标准继续增强了C的计算能力。例如，C99新增的变长数组（C11成为可选的特性），比传统的C数组更符合FORTRAN的用法（如果实现不支持变长数组，C11指定了\_STDC\_NO\_VLA\_\_宏的值为1）。

## B.8.1 IEC浮点标准

国际电工技术委员会（IEC）已经发布了一套浮点计算的标准（IEC 60559）。该标 准包括了浮点数的格式、精度、NaN、无穷值、舍入规则、转换、异常以及推荐的函数和算法等。C99纳入了该标准，将其作为C实现浮点计算的指导标准。C99新增的大部分浮点工具（如，fenv.h头文件和一些新的数学函数）都基于此。另外，float.h头文件定义了一些与IEC浮点模型相关的宏。

## 1.浮点模型

下面简要介绍一下浮点模型。标准把浮点数x看作是一个基数的某次幂乘以一个分数，而不是C语言的E记数法（例如，可以把876.54写成0.87654E3）。正式的浮点表示更为复杂:

$$
x = s b ^ {e} \sum_ {k = 1} ^ {p} f _ {k} ^ {b ^ {- k}}
$$

简单地说，这种表示法把一个数表示为有效数（significand）与b的e次幂的乘积。

下面是各部分的含义。

s代表符号（±1）。

b代表基数。最常见的值是2，因为浮点处理器通常使用二进制数学。

e代表整数指数（不要与自然对数中使用的数值常量e混淆），限制最小值和最大值。这些值依赖于留出储存指数的位数。

$\mathbf { f } _ { \mathrm { k } ^ { ' } }$ 代表基数为b时可能的数字。例如，基数为2时，可能的数字是0和1；在十六进制中，可能的数字是0～F。

p代表精度，基数为b时，表示有效数的位数。其值受限于预留储存有效数字的位数。

明白这种表示法的关键是理解float.h和fenv.h的内容。下面，举两个例子解释内部如何表示浮点数。

首先，假设一个浮点数的基数b为10，精度p为5。那么，根据上面的表示法，24.51应写成:

$$
(+ 1) 1 0 ^ {3} (2 / 1 0 + 4 / 1 0 0 + 5 / 1 0 0 0 + 1 / 1 0 0 0 0 + 0 / 1 0 0 0 0 0)
$$

假设计算机可储存十进制数（0～9），那么可以储存符号、指数3和5个f<sub>k</sub>值:2、4、5、1、0（这里， $\mathbf { f } _ { 1 }$ 是2， $\mathbf { f } _ { 2 } \mathbf { \boldsymbol { \mathrm { i } } }$ 是4，等等）。因此，有效数是0.24510，乘以 $1 0 ^ { 3 } !$ 得24.51。

接下来，假设符号为正，基数b是2，p是7（即，用7位二进制数表示），指数是5，待储存的有效数是1011001。下面，根据上面的公式构造该数:

$$
\begin{array}{l} \mathrm{x} = (+ 1) 2 ^ {5} (1 / 2 + 0 / 4 + 1 / 8 + 1 / 1 6 + 0 / 3 2 + 0 / 6 4 + 1 / 1 2 8) \\ = 3 2 (1 / 2 + 0 / 4 + 1 / 8 + 1 / 1 6 + 0 / 3 2 + 0 / 6 4 + 1 / 1 2 8) \\ = 1 6 + 0 + 4 + 2 + 0 + 0 + 1 / 4 = 2 2. 2 5 \\ \end{array}
$$

float.h中的许多宏都与该浮点表示相关。例如，对于一个float类型的值，表示基数的FLT\_RADIX是b，表示有效数位数（基数为b时）的FLT\_MANT\_DIG是p。

## 2.正常值和低于正常的值

正常浮点值（normalized floating-point value）的概念非常重要，下面简要介绍一下。为简单起见，先假设系统使用十进制（b = FLT\_RADIX = 10）和浮点值的精度为 $5\ (p =  FLT\_MAXT\_DIG  = 5)$ （标准要求的精度更高）。考虑下面表示31.841的方式:

指数 = 3，有效数 = .31841（.31841E3）

指数 = 4，有效数 = .03184（.03184E4）

显而易见，第1种方法精度最高，因为在有效数中使用了所有的5位可用位。规范化浮点非零值是第1位有效位为非零的值，这也是通常储存浮点数的方式。

现在，假设最小指数（FLT\_MIN\_EXP）是-10，那么最小的规范值是:

指数 = -10，有效数 = .10000（.10000E-10）

通常，乘以或除以10意味着使指数增大或减小，但是在这种情况下，如果除以10，却无法再减小指数。但是，可以改变有效数获得这种表示:

指数 = -10，有效数 = .01000（.01000E-10）

这个数被称为低于正常的（subnormal），因为该数并未使用有效数的全精度。例如，0.12343E-10除以10得.01234E-10，损失了一位的信息。

对于这个特例，0.1000E-10 是最小的非零正常值（FLT\_MIN），最小的非零低于正常值是0.00001E-10（FLT\_TRUE\_MIN）。

float.h中的宏FLT\_HAS\_SUBNURM、DBL\_HAS\_SUBNORM和LDBL\_HAS\_SUBNORM表征实现如何处理低于正常的值。下面是这些宏可能会用到的值及其含义:

-1 不确定（尚未统一）

0 不存在（例如，实现可能会用0替换低于正常的值）

1 存在

math.h库提供一些方法，包括fpclassify()和isnormal()宏，可以识别程序何时生成低于正常的值，这样会损失一些精度。

## 3.求值方案

float.h 中的宏 FLT\_EVAL\_METHOD 确定了实现采用何种浮点表达式的求值方案，如下所示（有些实现还会提供其他负值选项）。

-1 不确定

0 对在所有浮点类型范围和精度内的操作、常量求值

1 对在 double 类型的精度内和 float、double 类型的范围内的操作、常量求值，对

longdouble范围内的long double类型的操作、常量求值

2 对所有浮点类型范围内和long double类型精度内的操作和常量求值

例如，假设程序中要把两个float类型的值相乘，并把乘积赋给第3个float类型变量。对于选项1（即K&R C采用的方案），这两个float类型的值将被扩展为double类型，使用double类型完成乘法计算，然后在赋值计算结果时再把乘积转为float类型。

如果选择0（即ANSI C采用的方案），实现将直接使用这两个float类型的值相乘，然后赋值乘积。这样做比选项1快，但是会稍微损失一点精度。

## 4.舍入

float.h中的宏FLT\_ROUNDS确定了系统如何处理舍入，其指定值所对应的舍入方案如下所示。

-1 不确定
0 趋零截断
1 舍入到最接近的值
2 趋向正无穷
3 趋向负无穷

系统可以定义其他值，对应其他舍入方案。

一些系统提供控制舍入的方案，在这种情况下，fenv.h中的festround()函数提供编程控制。

如果只是计算制作37个蛋糕需要多少面粉，这些不同的舍入方案可能并不重要，但是对于金融和科学计算而言，这很重要。显然，把较高精度的浮点值转换成较低精度值时需要使用舍入方案。例如，把double类型的计算结果赋给float类型的变量。另外，在改变进制时，也会用到舍入方案。不同进制下精确表示的分数不同。例如，考虑下面的代码:

$$
\text {float} \mathrm{x} = 0. 8;
$$

在十进制下，8/10或4/5都可以精确表示0.8。但是大部分计算机系统都以二进制储存结果，在二进制下，4/5表示为一个无限循环小数:

0.1100110011001100...

因此，在把0.8储存在x中时，将其舍入为一个近似值，其具体值取决于使用的舍入方案。

尽管如此，有些实现可能不满足 IEC 60559 的要求。例如，底层硬件可能无法满足要求。因此，C99定义了两个可用作预处理器指令的宏，检查实现是否符合规范。第 1 个宏是\_ \_STDC\_IEC\_559\_ \_，如果实现遵循IEC 60559浮点规范，该宏被定义为常量1。第2个宏是\_

\_STDC\_IEC\_559\_COMPLEX\_ \_，如果实现遵循IEC 60559兼容复数运算，该宏被定义为常量1。

如果实现中未定义这两个宏，则不能保证遵循IEC 60559。

## B.8.2 fenv.h头文件

fenv.h 头文件提供一些与浮点环境交互的方法。也就是说，允许用户设置浮点控制模式值（该值管理如何执行浮点运算）并确定浮点状态标志（或异常）的值（报告运算效果的信息）。例如，控制模式设置可指定舍入的方案；如果运算出现浮点溢出则设置一个状态标志。设置状态标志的操作叫作抛出异常。

状态标志和控制模式只有在硬件支持的前提下才能发挥作用。例如，如果硬件没有这些选项，则无法更改舍入方案。

使用下面的编译指示开启支持:

#pragma STDC FENV\_ACCESS ON

这意味着程序到包含该编译指示的块末尾一直支持，或者如果该编译指示是外部的，则支持到该文件或翻译单元的末尾。使用下面的编译指示关闭支持:

#pragma STDC FENV\_ACCESS OFF

使用下面的编译指示可恢复编译器的默认设置，具体设置取决于实现:

#pragma STDC FENV\_ACCESS DEFAULT

如果涉及关键的浮点运算，这个功能非常重要。但是，一般用户使用的程度有限，所以本附录不再深入讨论。

## B.8.3 STDC FP\_CONTRACT编译指示

一些浮点数处理器可以把有多个运算符的浮点表达式合并成一个运算。例如，处理器只需一步就求出下面表达式的值:

$$
\mathbf{x}^* \mathbf{y} - \mathbf{z}
$$

这加快了运算速度，但是减少了运算的可预测性。STDC FP\_CONTRACT 编译指示允许用户开启或关闭这个特性。默认状态取决于实现。

为特定运算关闭合并特性，然后再开启，可以这样做:

#pragma STDC FP\_CONTRACT OFF

$$
\mathrm{val} = \mathrm{x} ^ {*} \mathrm{y-z};
$$

## B.8.4 math.h库增补

大部分C90数学库中都声明了double类型参数和double类型返回值的函数，例如:

double sin(double);

double sqrt(double);

C99和C11库为所有这些函数都提供了float类型和long double类型的函数。这些函数的名称由原来函数名加上f或l后缀构成，例如:

float sinf(float); /\* sin()的float版本 \*/

long double sinl(long double); /\* sin()的long double版本 \*/

有了这些不同精度的函数系列，用户可以根据具体情况选择最效率的类型和函数组合。

C99还新增了一些科学、工程和数学运算中常用的函数。表B.5.16列出了所有数学函数的double版本。在许多情况下，这些函数的返回值都可以使用现有的函数计算得出，但是新函数计算得更快更精确。例如，loglp(x)表示的值与与log(1 + x)相同，但是loglp(x)使用了不同的算法，对于较小的x值而言计算更精确。因此，可以使用log()函数作普通运算，但是对于精确要求较高且x值较小时，用loglp()函数更好。

除这些函数以外，数学库中还定义了一些常量和与数字分类、舍入相关的函数。例如，可以把值分为无穷值、非数（NaN）、正常值、低于正常的值、真零。[NaN是一个特别的值，用于表示一个不是数的值。例如，asin(2.0)返回NaN，因为定义了asin()函数的参数必须是-1～1范围内的值。低于正常的值是比使用全精度表示的最小值还要小的数。]还有一些专用的比较函数，如果一个或多个参数是非正常值时，函数的行为与标准的关系运算符不同。

使用C99的分类方案可以检测计算的规律性。例如，math.h中的isnormal()宏，如果其参数是一个正常的数，则返回真。下面的代码使用该宏在num不正常时结束循环:

#include &lt;math.h&gt; // 为了使用isnormal()

..

float num = 1.7e-19;

float numprev = num;

```txt
while (isnormal(num)) // 当num为全精度的float类型值
{
numprev = num;
num /= 13.7f;
}
```

简而言之，数学库为更好地控制如何计算浮点数，提供了扩展支持。

## B.8.5 对复数的支持

复数是有实部和虚部的数。实部是普通的实数，如浮点类型表示的数。虚部表示一个虚数。虚数是-1的平方根的倍数。在数学中，复数通常写作类似4.2 + 2.0i的形式，其中i表示-1的平方根。

C99支持3种复数类型（在C11中为可选）:

```txt
float _Complex

double _Complex

long double _Compplex
```

例如，储存float \_Complex类型的值时，使用与两个float类型元素的数组相同的内存布局，实部值储存在第1个元素中，虚部值储存在第2个元素中。

C99和C11还支持下面3种虚类型:

```txt
float _Imaginary

double _Imaginary

long double _Imaginary
```

包含了complex.h头文件，就可以用complex代替\_Complex，用imaginary代替\_Imaginary。

为复数类型定义的算术运算遵循一般的数学规则。例如，(a+b\*I)\* (c+d\*I)即是(a\*c-b\*d)+(b\*c+a\*d)\*I。

complex.h头文件定义了一些宏和接受复数参数并返回复数的函数。特别是，宏I表示-1的平方根。因此，可以编写这样的代码:

$$
\text {double complex} c 1 = 4. 2 + 2. 0 * I;
$$

$$
\text {float imaginary} \mathrm{c2=-3.0*I};
$$

C11提供了另一种方法，通过CMPLX()宏给复数赋值。例如，如果re和im都是double类型的值，可以这样做:

$$
\text {double complex c3} = \text {CMPLX} (\text {re, im});
$$

这种方法的目的是，宏在处理不常见的情况（如，im是无穷大或非数）时比直接赋值好。

complex.h头文件提供了一些复数函数的原型，其中许多复数函数都有对应math.h中的函数，其函数名即是对应函数名前加上c前缀。例如，csin()返回其复数参数的复正弦。其他函数与特定的复数特性相关。例如，creal()函数返回一个复数的实部，cimag()函数返回一个复数的虚部。也就是说，给定一个double conplex类型的z，下面的代码为真:

$$
\mathrm{z} = \operatorname{creal} (\mathrm{z}) + \operatorname{cimag} (\mathrm{z}) * \mathrm{I};
$$

如果熟悉复数，需要使用复数，请详细阅读complex.h中的内容。

下面的示例演示了对复数的一些支持:

// complex.c -- 复数

```c
#include <stdio.h>

#include <complex.h>

void show_cmlx(complex double cv);

int main(void)

{
complex double v1 = 4.0 + 3.0*I;

double re, im;

complex double v2;

complex double sum, prod, conjug;

printf("Enter the real part of a complex number: ");
scanf("%lf", &re);

printf("Enter the imaginary part of a complex number: ");
scanf("%lf", &im);

// CMPLX()是C11中的一个特性

// v2 = CMPLX(re, im);

v2 = re + im * I;

printf("v1: ");
show_cmlx(v1);

putchar('\n');
```

```c
printf("v2: ");
show_cmlx(v2);
putchar('\n');
sum = v1 + v2;
prod = v1 * v2;
conjug =conj(v1);
printf("sum: ");
show_cmlx(sum);
putchar('\n');
printf("product: ");
show_cmlx(prod);
putchar('\n');
printf("complex conjugate of v1: ");
show_cmlx(conjug);
putchar('\n');
return 0;
}
void show_cmlx(complex double cv)
{
```

```lua
printf(("(.2f, %.2fi)", creal(cv), cimag(cv));

return;

}
```

如果使用C++，会发现C++的complex头文件提供一种基于类的方式处理复数，这与C的complex.h头文件使用的方法不同。

## B.9 参考资料IX:C和C++的区别

在很大程度上，C++是C的超集，这意味着一个有效的C程序也是一个有效的C++程序。C和C++的主要区别是，C++支持许多附加特性。但是，C++中有许多规则与 C 稍有不同。这些不同使得 C 程序作为C++程序编译时可能以不同的方式运行或根本不能运行。本节着重讨论这些区别。如果使用C++的编译器编译C程序，就知道这些不同之处。虽然C和C++的区别对本书的示例影响很小，但如果把C代码作为C++程序编译的话，会导致产生错误的消息。

C99标准的发布使得问题更加复杂，因为有些情况下使得C更接近C++。例如，C99标准允许在代码中的任意处进行声明，而且可以识别//注释指示符。在其他方面，C99使其与C++的差异变大。例如，新增了变长数组和关键字restrict。C11缩小了与C++的差异。例如，引进了char16\_t类型，新增了关键字\_Alignas，新增了alignas宏与C++的关键字匹配。C11仍处于起步阶段，许多编译器开发商甚至都没有完全支持C99。我们要了解C90、C99、C11之间的区别，还要了解C++11与这些标准之间的区别，以及每个标准与C标准之间的区别。这部分主要讨论C99、C11和C++之间的区别。当然，C++也正在发展，因此，C和C++的异同也在不断变化。

## B.9.1 函数原型

在C++中，函数原型必不可少，但是在C中是可选的。这一区别在声明一个函数时让函数名后面的圆括号为空，就可以看出来。在C中，空圆括号说明这是前置原型，但是在C++中则说明该函数没有参数。也就是说，在C++中，int slice();和int slice(void);相同。例如，下面旧风格的代码在C中可以接受，但是在C++中会产生错误:

```txt
int slice();
int main()
{
```

```txt
...
slice(20, 50);
}
...
int slice(int a, int b)
{
...
}
```

在C中，编译器假定用户使用旧风格声明函数。在C++中，编译器假定slice()与slice(void)相同，且未声明slice(int, int)函数。

另外，C++允许用户声明多个同名函数，只要它们的参数列表不同即可。

## B.9.2 char常量

C把char常量视为int类型，而C++将其视为char类型。例如，考虑下面的语句:

```javascript
char ch = 'A';
```

在C中，常量'A'被储存在int大小的内存块中，更精确地说，字符编码被储存为一个int类型的值。相同的数值也储存在变量ch中，但是在ch中该值只占内存的1字节。

在C++中，'A'和ch都占用1字节。它们的区别不会影响本书中的示例。但是，有些C程序利用char常量被视为int类型这一特性，用字符来表示整数值。例如，如果一个系统中的int是4字节，就可以这样编写C代码:

int x = 'ABCD'; /\*对于int是4字节的系统，该语句出现在C程序中没问题，但是出现在C++程序中会出错 \*/

'ABCD'表示一个4字节的int类型值，其中第1个字节储存A的字符编码，第2个字节储存B的字符编码，以此类推。注意，'ABCD'和"ABCD"不同。前者只是书写int类型值的一种方式，而后者是一个字符串，它对应一个5字节内存块的地址。

考虑下面的代码:

```matlab
int x = 'ABCD';

char c = 'ABCD';

printf("%d %d %c %c\n", x, 'ABCD', c, 'ABCD');
```

在我们的系统中，得到的输出如下:

1094861636 1094861636 D D

该例说明，如果把'ABCD'视为int类型，它是一个4字节的整数值。但是，如果将其视为char类型，程序只使用最后一个字节。在我们的系统中，尝试用%s转换说明打印'ABCD'会导致程序奔溃，因为'ABCD'的数值（1094861636）已超出该类型可表示的范围。

可以这样使用的原因是C提供了一种方法可单独设置int类型中的每个字节，因为每个字符都对应一个字节。但是，由于要依赖特定的字符编码，所以更好的方法是使用十六进制的整型常量，因为每两位十六进制数对应一个字节。第15章详细介绍过相关内容（C的早期版本不提供十六进制记法，这也许是多字符常量技术首先得到发展的原因）。

## B.9.3 const限定符

在C中，全局的const具有外部链接，但是在C++中，具有内部链接。也就是说，下面C++的声明:

const double PI = 3.14159;

相当于下面C中的声明:

static const double PI = 3.14159;

假设这两条声明都在所有函数的外部。C++规则的意图是为了在头文件更加方便地使用 const。如果const变量是内部链接，每个包含该头文件的文件都会获得一份const变量的备份。如果const变量是外部链接，就必须在一个文件中进行定义式声明，然后在其他文件中使用关键字 extern 进行引用式声明。

顺带一提，C++可以使用关键字extern使一个const值具有外部链接。所以两种语言都可以创建内部链接和外部链接的const变量。它们的区别在于默认使用哪种链接。

另外，在C++中，可以用const来声明普通数组的大小:

const int ARSIZE = 100;

double loons[ARSIZE]; /\* 在C++中，与double loons[100];相同 \*/

当然，也可以在C99中使用相同的声明，不过这样的声明会创建一个变长数组。

在C++中，可以使用const值来初始化其他const变量，但是在C中不能这样做:

const double RATE = 0.06; // C++和C都可以

const double STEP = 24.5; // C++和C都可以

const double LEVEL= RATE \* STEP; // C++可以，C不可以

## B.9.4 结构和联合

声明一个有标记的结构或联合后，就可以在C++中使用这个标记作为类型名:

```c
struct duo
{
int a;
int b;
};
struct duo m; /* C和C++都可以 */
duo n; /* C不可以，C++可以*/
```

结果是结构名会与变量名冲突。例如，下面的程序可作为C程序编译，但是作为C++程序编译时会失败。因为C++把printf()语句中的duo解释成结构类型而不是外部变量:

```c
#include <stdio.h>

float duo = 100.3;

int main(void)

{

struct duo { int a; int b;};

struct duo y = { 2, 4};

printf ("%f\n", duo); /* 在C中没问题，但是在C++不行 */
return 0;
```

```txt
}
```

在C和C++中，都可以在一个结构的内部声明另一个结构:

```c
struct box

{

struct point {int x; int y; } upperleft;

struct point lowerright;

};
```

在C中，随后可以使用任意使用这些结构，但是在C++中使用嵌套结构时要使用一个特殊的符号:

struct box ad; /\* C和 C++都可以 \*/

struct point dot; /\* C可以，C++不行 \*/

box::point dot; /\* C不行，C++可以 \*/

## B.9.5 枚举

C++使用枚举比C严格。特别是，只能把enum常量赋给enum变量，然后把变量与其他值作比较。不经过显式强制类型转换，不能把int类型值赋给enum变量，而且也不能递增一个enum变量。下面的代码说明了这些问题:

enum sample {sage, thyme, salt, pepper};

enum sample season;

season = sage; /\* C和C++都可以 \*/

season = 2; /\* 在C中会发出警告，在C++中是一个错误 \*/