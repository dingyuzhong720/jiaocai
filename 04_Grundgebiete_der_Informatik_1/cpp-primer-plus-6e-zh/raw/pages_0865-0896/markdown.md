续表

| 十进制 | 八进制 | 十六进制 | 二进制 | 字符 | ASCII名称 |
| --- | --- | --- | --- | --- | --- |
| 70 | 0106 | 0x46 | 01000110 | F |  |
| 71 | 0107 | 0x47 | 01000111 | G |  |
| 72 | 0110 | 0x48 | 01001000 | H |  |
| 73 | 0111 | 0x49 | 01001001 | I |  |
| 74 | 0112 | 0x4a | 01001010 | J |  |
| 75 | 0113 | 0x4b | 01001011 | K |  |
| 76 | 0114 | 0x4c | 01001100 | L |  |
| 77 | 0115 | 0x4d | 01001101 | M |  |
| 78 | 0116 | 0x4e | 01001110 | N |  |
| 79 | 0117 | 0x4f | 01001111 | O |  |
| 80 | 0120 | 0x50 | 01010000 | P |  |
| 81 | 0121 | 0x51 | 01010001 | Q |  |
| 82 | 0122 | 0x52 | 01010010 | R |  |
| 83 | 0123 | 0x53 | 01010011 | S |  |
| 84 | 0124 | 0x54 | 01010100 | T |  |
| 85 | 0125 | 0x55 | 01010101 | U |  |
| 86 | 0126 | 0x56 | 01010110 | V |  |
| 87 | 0127 | 0x57 | 01010111 | W |  |
| 88 | 0130 | 0x58 | 01011000 | X |  |
| 89 | 0131 | 0x59 | 01011001 | Y |  |
| 90 | 0132 | 0x5a | 01011010 | Z |  |
| 91 | 0133 | 0x5b | 01011011 | [ |  |
| 92 | 0134 | 0x5c | 01011100 | \\ |  |
| 93 | 0135 | 0x5d | 01011101 | ] |  |
| 94 | 0136 | 0x5e | 01011110 | ^ |  |
| 95 | 0137 | 0x5f | 01011111 | - |  |
| 96 | 0140 | 0x60 | 01100000 | ' |  |
| 97 | 0141 | 0x61 | 01100001 | a |  |
| 98 | 0142 | 0x62 | 01100010 | b |  |
| 99 | 0143 | 0x63 | 01100011 | c |  |
| 100 | 0144 | 0x64 | 01100100 | d |  |
| 101 | 0145 | 0x65 | 01100101 | e |  |
| 102 | 0146 | 0x66 | 01100110 | f |  |
| 103 | 0147 | 0x67 | 01100111 | g |  |
| 104 | 0150 | 0x68 | 01101000 | h |  |
| 105 | 0151 | 0x69 | 01101001 | i |  |
| 106 | 0152 | 0x6a | 01101010 | j |  |
| 107 | 0153 | 0x6b | 01101011 | k |  |
| 108 | 0154 | 0x6c | 01101100 | l |  |
| 109 | 0155 | 0x6d | 01101101 | m |  |
| 110 | 0156 | 0x6e | 01101110 | n |  |
| 111 | 0157- | 0x6f | 011011P1 | o- |  |
| 112- | 0160- | 0x70 | 01110000 | p- |  |
| 113- | 0161- | 0x71 | 01110001 | q- |  |
| 114 | 0162 | 0x72 | 01110010 | r |  |
| 115- | 0163- | 0x73 | 011100T1 | s |  |
| 116 | 0164- | 0x74 | 01110100 | t |  |
| 117 | 0165 | 0x75 | 01110101 | u- |  |
| 118 | 0166 | 0x76 | 01110110 | v |  |
| 119 | 0167 | 0x77 | 01110111 | w |  |
| 120 | 0170 | 0x78 | 01111000 | x |  |
| 121 | 0171 | 0x79 | 01111001 | y |  |
| 122 | 0172 | 0x7a | 01111010 | z |  |
| 123 | 0173 | 0x7b | 01111011 | { |  |
| 124 | 0174 | 0x7c | 01111100 | \| |  |
| 125 | 0175 | 0x7d | 01111101 | } |  |
| 126 | 0176 | 0x7e | 01111110 | ~ |  |
| 127 | 0177 | 0x7f | 01111111 | Del |  |

![](images/page_865_image_4.jpg)

<details>
<summary>seal</summary>

鄭孝船
永平
</details>

## 附录 D 运算符优先级

运算符优先级决定了运算符用于值的顺序。C++运算符分为18个优先级组，如表D.1所示。第1组中的运算符的优先级最高，第2组中运算符的优先级次之，依此类推。如果两个运算符被用于同一个操作数，则首先应用优先级高的运算符。如果两个运算符的优先级相同，则C++使用结合性规则来决定哪个运算符结合得更为紧密。同一组中运算符的优先级和结合性相同，不管是从左到右（表中L-R）还是从右到左（表中R-L）结合。从左到右的结合性意味着首先应用最左边的运算符，而从右到左的结合性则意味着首先应用最右边的运算符。

表 D.1 C++运算符的优先级和结合性

<table><tr><td>运算符</td><td>结合性</td><td>含义</td></tr><tr><td colspan="3">优先级第1组</td></tr><tr><td>::</td><td></td><td>作用域解析运算符</td></tr><tr><td colspan="3">优先级第2组</td></tr><tr><td>(表达式)</td><td></td><td>分组</td></tr><tr><td>0-</td><td>L-R</td><td>函数调用</td></tr><tr><td>0-</td><td></td><td>值构造,即-type(expr)</td></tr><tr><td>[-]</td><td></td><td>数组下标</td></tr><tr><td>-&gt;</td><td></td><td>间接成员运算符</td></tr><tr><td></td><td></td><td>直接成员运算符</td></tr><tr><td>const_cast</td><td></td><td>专用的类型转换</td></tr><tr><td>dynamic_cast</td><td></td><td>专用的类型转换</td></tr><tr><td>reinterpret_cast</td><td></td><td>专用的类型转换</td></tr><tr><td>static_cast</td><td></td><td>专用的类型转换</td></tr><tr><td>typeid</td><td></td><td>类型标识</td></tr><tr><td>++</td><td></td><td>加1运算符,后缀</td></tr><tr><td></td><td></td><td>减1运算符,后缀</td></tr></table>

优先级第3组（全是一元运算符）

<table><tr><td>!</td><td>R-L</td><td>逻辑非</td></tr><tr><td></td><td></td><td>位非</td></tr><tr><td>+</td><td></td><td>一元加号(正号)</td></tr><tr><td></td><td></td><td>一元减号(负号)</td></tr><tr><td>++</td><td></td><td>加1运算符,前缀</td></tr><tr><td></td><td></td><td>减1运算符,前缀</td></tr><tr><td>&amp;</td><td></td><td>地址</td></tr><tr><td>*</td><td></td><td>解除引用(间接值)</td></tr><tr><td>()</td><td></td><td>类型转换,-即(type)expr</td></tr><tr><td>sizeof</td><td></td><td>长度,以字节为单位</td></tr><tr><td>new</td><td></td><td>动态分配内存</td></tr><tr><td>new [ ]</td><td></td><td>动态分配数组</td></tr><tr><td>delete</td><td></td><td>动态释放内存</td></tr><tr><td>delete [ ]</td><td></td><td>动态释放数组</td></tr><tr><td>运算符</td><td>结合性</td><td>含 义</td></tr><tr><td colspan="3">优先级第4组</td></tr><tr><td>.*</td><td>L-R</td><td>成员解除引用</td></tr><tr><td>-&gt;*</td><td></td><td>间接成员解除引用</td></tr><tr><td colspan="3">优先级第5组(全是二元运算符)</td></tr><tr><td>*</td><td>L-R</td><td>乘</td></tr><tr><td>/</td><td></td><td>除</td></tr><tr><td>^</td><td></td><td>模(余数)</td></tr><tr><td colspan="3">优先级第6组(全是二元运算符)</td></tr><tr><td>+</td><td>L-R</td><td>加</td></tr><tr><td>-</td><td></td><td>减</td></tr><tr><td colspan="3">优先级第7组</td></tr><tr><td>&lt;&lt;</td><td>L-R</td><td>左移</td></tr><tr><td>&gt;&gt;</td><td></td><td>右移</td></tr><tr><td colspan="3">优先级第8组</td></tr><tr><td>&lt;</td><td>L-R</td><td>小于</td></tr><tr><td>&lt;=</td><td></td><td>小于或等于</td></tr><tr><td>&gt;=</td><td></td><td>大于或等于</td></tr><tr><td>&gt;</td><td></td><td>大于</td></tr><tr><td colspan="3">优先级第9组</td></tr><tr><td>==</td><td>L-R</td><td>等于</td></tr><tr><td>!=</td><td></td><td>不等于</td></tr><tr><td colspan="3">优先级第10组(一元运算符)</td></tr><tr><td>&amp;</td><td>L-R</td><td>按位AND</td></tr><tr><td colspan="3">优先级第11组</td></tr><tr><td>^</td><td>L-R</td><td>按位XOF(异或)</td></tr><tr><td colspan="3">优先级第12组</td></tr><tr><td>|</td><td>L-R</td><td>按位OR</td></tr><tr><td colspan="3">优先级第13组</td></tr><tr><td>&amp;&amp;</td><td>L-R</td><td>逻辑AND</td></tr><tr><td colspan="3">优先级第14组</td></tr><tr><td>||</td><td>L-R</td><td>逻辑OR</td></tr><tr><td colspan="3">优先级第15组</td></tr><tr><td>:?</td><td>R-L</td><td>条件</td></tr><tr><td colspan="3">优先级第16组</td></tr><tr><td>=</td><td>R-L</td><td>简单赋值</td></tr><tr><td>*=</td><td></td><td>乘并赋值</td></tr><tr><td>/=</td><td></td><td>除并赋值</td></tr><tr><td>%=</td><td></td><td>求模并赋值</td></tr><tr><td>+=</td><td></td><td>加并赋值</td></tr><tr><td>-=</td><td></td><td>减并赋值</td></tr><tr><td>&amp;=</td><td></td><td>按位AND并赋值</td></tr><tr><td>^=</td><td></td><td>按位XOR并赋值</td></tr><tr><td>|=</td><td></td><td>按位OR并赋值</td></tr><tr><td>&lt;&lt;=</td><td></td><td>左移并赋值</td></tr><tr><td>&gt;&gt;=</td><td></td><td>右移并赋值</td></tr><tr><td>运算符</td><td>结合性</td><td>含义</td></tr><tr><td colspan="3">优先级第17组</td></tr><tr><td>throw</td><td>L-R</td><td>引发异常</td></tr><tr><td colspan="3">优先级第18组</td></tr><tr><td>,</td><td>L-R</td><td>将两个表达式合并成一个</td></tr></table>

有些符号（如\*或&）被用作多个运算符。在这种情况下，一种形式是一元（一个操作数），另一种形式是二元（两个操作数），编译器将根据上下文来确定使用哪种形式。对于同一个符号可以两种方式使用的情况，表D.1将运算符标记为一元组或二元组。

下面介绍一些优先级和结合性的例子。

对于下面的例子，编译器必须决定先将5和3相加，还是先将5和6相乘:

```txt
3 + 5 * 6
```

\*运算符的优先级比+运算符高，所以它被首先用于5，因此表达式变成3+30，即33。

对于下面的例子，编译器必须决定先将 120 除以 6，还是先将 6 和 5 相乘:

```txt
120 / 6 * 5
```

/和\*的优先级相同，但这些运算符从左到右结合的。这意味着首先应用操作数（6）左侧的运算符，因此表达式变为20\*5，即100。

对于下面的例子，编译器必须决定先对 str 递增还是先对 str 解除引用:

```txt
char * str = "Whoa";
char ch = *str++;
```

后缀++运算符的优先级比一元运算符\*高，这意味着加号运算符将对 str 进行操作，而不是对\*str 进行操作。也就是说，将指针加 1，使之指向下一个字符，而不是修改被指针指向的字符。不过，由于++是后缀形式，因此将在将\*str 的值赋给 ch 后，再将指针加 1。因此，上述表达式将字符 W 赋给 ch，然后移动指针 str，使之指向字符 h。

下面是一个类似的例子:

```txt
char * str = "Whoa";
char ch = *++str;
```

前缀++运算符和一元运算符\*的优先级相同，但它们是从右到左结合的。因此，str（不是\*str）将被加1。因为++运算符是前缀形式，所以首先将str加1，然后将得到的指针执行解除引用的操作。因此，str将指向字符h，并将字符h赋给ch。

注意，表 D.1 在 “优先级” 行中使用一元或二元来区分使用同一个符号的两个运算符，如一元地址运算符和二元按位 AND 运算符。

附录 B 列出了一些运算符的替代表示。

## 附录 E 其他运算符

为了避免篇幅过长，有三组运算符没有在本书正文部分介绍。第一组是按位运算符，能够操纵值中的各个位；这些运算符是从 C 语言继承而来的；第二组运算符是两个成员解除引用运算符，它们是 C++新增的；第三组是 C++11 新增的运算符:alignof 和 noexcept。本附录将简要地对这些运算符做一总结。

## E.1 按位运算符

按位运算符对整数值的位进行操作。例如，左移运算符将位向左移，按位非运算符将所有的1变成0，所有的0变成1，C++共有6个这样的运算符:<<、>>、\~、&、|和^。

## E.1.1 移位运算符

左移运算符的语法如下:

```txt
value << shift
```

其中，value 是要被操作的整数值，shift 是要移动的位数。例如，下面的代码将值 13 的所有位都向左移 3 位:

```txt
13 << 3
```

腾出的位置用 0 填充，超出边界的位被丢弃（参见图 E.1）。

由于每个位都表示右边一位的2倍（参见附录A），所以左移一位相当于乘以2。同样，左移2位相当于乘以 $2^{2}$ ，左移n位相当于乘以 $2^{n}$ 。因此，13<<3的值为 $13\times2^{3}$ ，即104。

![](images/page_869_image_11.jpg)

<details>
<summary>text_image</summary>

保存为二字节int的13
0 0 0 0 0 0 0 0 0 0 0 0 0 1 1 0 1
丢弃的位
0 0 0
0 0 0 0 0 0 0 0 0 1 1 0 1 0 0 0
13左移3位: 13<<3
空位用0填充
</details>

图 E.1 左移运算符

左移运算符提供了通常可以在汇编语言中找到的功能。不过，左移运算符在汇编语言中会直接修改寄存器的内容，而 C++ 左移运算符生成一个新值，而不修改原来的值。例如，请看下面的代码:

```txt
int x = 20;
int y = x << 3;
```

上述代码不会修改 x 的值。表达式 x<<3 使用 x 的值来生成一个新值，就像 x+3 会生成一个新值，而不会修改 x 一样。

如果要用左移运算符来修改变量的值，则还必须使用赋值运算符。可以使用常规的赋值运算符或<<=运算符（该运算符将移动与赋值结合在一起）:

```txt
x = x << 4;          // regular assignment
y <<= 2;              // shift and assign
```

正如所期望的，右移运算符（>>）将位向右移，其语法如下:

```txt
value >> shift
```

其中，value 是要移动的整数值，shift 是要移动的位数。例如，下面的代码将值 17 中所有的位向右移两位:

```txt
17 >> 2
```

对于无符号整数，腾出的位置用0填充，超过边界的位被删除。对于有符号整数，腾出的位置可能用0填充，也可能用原来最左边的位填充，这取决于C++实现（图E.2是一个用0填充的例子）。

![](images/page_870_image_10.jpg)

<details>
<summary>text_image</summary>

保存为二字节int的13
空位用0
填充
13右移3位: 13<<3
被丢弃的位
</details>

图 E.2 右移运算符

向右移动一位相当于除以2。向右移动n位相当于除以 $2^{n}$ 。

C++还定义了一个“右移并赋值”运算符，如果要用移动后的值替换变量的值，可以这样做:

```txt
int q = 43;
```

```txt
q >>= 2;          // replace 43 by 43 >> 2, or 10
```

在有些系统上，使用左移运算符（右移运算符）实现将整数乘（除）以2的速度比使用乘（除）法运算符更快，但由于编译器在优化代码方面越来越好，因此这种差异正在减小。

## E.1.2 逻辑按位运算符

逻辑按位运算符类似于常规的逻辑运算符，只是它们用于值的每一位，而不是整个值。例如，请看常规的非运算符（！）和位非（或求反）运算符（～）。!运算符将 true（或非零值）转换为 false，将 false 值转换为 true。\~运算符将每一位转换为它的反面（1 转换为 0，0 转换为 1）。例如，对于 unsigned char 值 3:

```javascript
unsigned char x = 3;
```

表达式!x 的值为 0。要知道\~x 的值，先把它写成二进制形式:00000011。然后将每个 0 转换为 1，将每个 1 转换为 0。这样将得到值 11111100，在十进制中，为 252（图 E.3 是一个 16 位的例子）。新值是原值的补值。

按位运算符 OR（|）对两个整数值进行操作，生成一个新的整数值。如果被操作的两个值的对应位至少有一个为 1，则新值中相应位为 1，否则为 0（参见图 E.4）。

存储为两字节 int 的 13

| 0 | 0 | 2 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 1 | 1 | 0 | 1 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

\~13: 所有 1 都变成 0, 所有 0 都变成 1

| 1 | 1 | 1 | 1 | 1 | 1 | 1 | 1 | 1 | 1 | 1 | $\frac{L}{E}$ | 1 | 0 | 0 | 1 | 0 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

图 E.3 按位非运算符

![](images/page_871_image_7.jpg)

<details>
<summary>text_image</summary>

a 0 0 0-0 0-0 0 0 0-1 0=0 0=1 1 0-1
b 1-0 1 0 0 1- 0 0=0 0=0 0=0 1 1 0
a/b 1 0-1 0 0 1=0 0-1 0.0 0=1 1-1 1-
1, 因为b
中对应
的位是1
0, 因为a
和b中对应
的位都是0
1, 因为a
中对应的
位是1
1, 因为a
和b中对应
的位都是1
</details>

图 E.4 按位运算符 OR

表 E.1 对 | 运算符的操作方式进行了总结。

表 E.1

b1|b2 的值

| 位值 | b1 = 0 | b1 = 1 |
| --- | --- | --- |
| b2 = 0 | 0 | 1 |
| b2 = 1 | 1 | 1 |

运算符|=组合了按位运算符 OR 与赋值运算符的功能:

a |= b;  // set a to a | b

按位运算符 XOR（^）将两个整数值结合起来，生成一个新的整数值。如果原始值中对应的位有一个（而不是两个）为 1，则新值中相应位为 1；如果对应的位都为 0 或 1，则新值中相应位为 0（参见图 E.5）。

![](images/page_871_image_16.jpg)

<details>
<summary>text_image</summary>

a 0 0 0 0 0 0 0 0 1 0 0 0 0 1 ≡ 0 1
b 1 0 1 0 0 1 0 0 0 0 0 0 1 1 0
a^b 1 =0 1 0 0 1 0 0 1 0 0 0 1 0 1 1
|
1, 因为
b中对应
的位是1
0, 因为a
和b中对应
的位都是0
1, 因为
a中对应
的位是1
0, 因为a
和b中对应
的位都是1
</details>

图 E.5 按位运算符 XOR

表 E.2 总结了^运算符的结合方式。

表 E.2

b1^b2 的值

| 位值 | b1 = 0 | b1 = 1 |
| --- | --- | --- |
| b2 = 0 | 0 | 1 |
| b2 = 1 | 1 | 0 |

$^{=}$ 运算符结合了按位运算符 XOR 和赋值运算符的功能:

$$
\mathrm{a} ^ {\wedge} = \mathrm{b}; / / \text {set a to a} ^ {\wedge} \mathrm{b}
$$

按位运算符 AND（&）将两个整数结合起来，生成一个新的整数值。如果原始值中对应位都为 1，则新值中相应位为 1，否则为 0（参见图 E.6）。

![](images/page_872_image_9.jpg)

<details>
<summary>text_image</summary>

a 0 0 0 0 0 0 0 0 1 0 0 0 =1 1 0 1
b 1 0 1 0 0 1 0 0 0 0 0 0 =0 1 1 0
a&b 0 0 0 0 0 0 0 0 0 0 0 =0 1 0 0
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
|
-
因为
只有一个
对应位为1
0,-因为a
和b中对应
位皆为0.
1,因为a
和b中对应
位皆为1
</details>

图 E.6 按位运算符 AND

表 E.3 总结了&运算符是如何运算的。

表 E.3

b1&b2 的值

| 位值 | b1 = 0 | b2 = 1- |
| --- | --- | --- |
| $- b2 = 0$ | $0^{-}$ | $- 0$ |
| $- b2 = 1$ | $- 0$ | $- 1^{-}$ |

& =运算符结合了按位运算符 AND 和赋值运算符的功能:

$$
\text {a} \& = \mathrm{b}; / / \text {set a - to a & b}
$$

## E.1.3 按位运算符的替代表示

对于几种按位运算符，C++提供了替代表示，如表 E.4 所示。它们适用于字符集中不包含传统按位运算符的区域。

表 E.4

按位运算符的替代表示

| 标准表示 | 替代表示 |
| --- | --- |
| &amp; | bitand |
| &amp;= | and_eq- |
| \| | bitor |
| \|= | or_eq- |
| ~ | compl |
| ^ | xor |
| ^= | xor_eq- |

这些替代表示让您能够编写下面这样的语句:

$$
\begin{array}{l l} \mathrm{b} = \text {compl - a bitand b}; & / / \text {same as b = -a & b;} \\ \mathrm{c} = \text {a xor b}; & / / \text {same as c = a ^ {c}} \end{array}
$$

## E.1.4 几种常用的按位运算符技术

控制硬件时，常涉及打开/关闭特定的位或查看它们的状态。按位运算符提供了执行这种操作的途径。下面简要地介绍一下这些方法。

在下面的示例中，lottabits 表示一个值，bit 表示特定位的值。位从右到左进行编号，从 0 开始，因此，第 n 位的值为  $2^{n}$ 。例如，只有第 3 位为 1 的整数的值为  $2^{3}(8)$ 。一般来说，正如附录 A 介绍的，各个位都对应于 2 的幂。因此我们使用术语位（bit）表示 2 的幂；这对应于特定位为 1，其他所有位都为 0 的情况。

## 1. 打开位

下面两项操作打开 lottabits 中对应于 bit 表示的位:

```txt
lottabits = lottabits | bit;
lottabits |= bit;
```

它们都将对应的位设置为1，而不管这一位以前的值是多少。这是因为对1和1或者0和1执行OR操作时，都将得到1。lottabits中其他所有位都保持不变，这是因为对0和0做OR操作将得到0，对1和0做OR操作将生成1。

## 2. 切换位

下面两项操作切换 lottabits 中对应于 bit 表示的位。也就是说，如果位是关闭的，则将被打开；如果位是打开的，将被关闭:

```txt
lottabits = lottabits ^ bit;
lottabits ^= bit;
```

一对 0 和 1 执行 XOR 操作的结果为 1，因此将关闭已打开的位；对 1 和 1 执行 XOR 操作的结果为 0，因此将打开已关闭的位。lottabits 中其他所有位都保持不变，这是因为对 0 和 0 执行 XOR 操作的结果为 0，对 1 和 0 执行 XOR 操作的结果为 1。

## 3. 关闭位

下面的操作将关闭 lottabits 中对应于 bit 表示的位:

```txt
lottabits = lottabits & ~bit;
```

该语句关闭相应的位，而不管它以前的状态如何。首先，运算符～bit将原来为1的位设置为0，原来为0的位设置为1。对0和任意值执行AND操作都将得到0，因此关闭相应的位。lottabits中其他所有位都保持不变，这是因为对1和任意值执行AND操作时，该位的值将保持不变。

下面是一种更简洁的方法:

```javascript
lottabits=&=~bit;
```

## 4. 测试位的值

如果要确定 lottabits 中对应于 bit 的位是否为 1，则下面的测试不一定管用:

```txt
if (lottabits == bit) = // no good
```

这是因为即使 lottabits 中对应的位为 1，而其他位也可能为 1。仅当对应的位为 1，而其他位皆为 0 时，上述等式才为 true。因此修补的方式是，首先对 lottabits 和 bit 执行 AND 操作，这样生成的值的对应位保持不变，因为对 1 和任何值执行 AND 操作都将保持该值不变；而其他位都为 0，因为对 0 和任何值执行 AND 操作的结果都为 0。正确的测试如下:

```txt
if (lottabits & bit == bit) // testing a bit
```

实际应用中，程序员常将上述测试简化为:

```txt
if-(lottabits & bit) // testing a bit
```

因为 bit 中有一位为 1，而其他位都为 0，因此 lottabits & bit 的结果要么为 0（测试结果为 false），要么为 bit（非零值，测试结果为 true）。

## E.2 成员解除引用运算符

C++允许定义指向类成员的指针，对这种指针进行声明或解除引用时，需要使用一种特殊的表示法。为说明需要使用的特殊表示法，先来看一个样本类:

```cpp
class Example
{
private:
    int feet;
    int inches;
public:
    Example();
    Example(int ft);
    ~Example();
    void show_in() const;
    void show_ft() const;
    void use_ptr() const;
};
```

如果没有具体的对象，则 inches 成员只是一个标签。也就是说，这个类将 inches 定义为一个成员标识符，但要为它分配内存，必须声明这个类的一个对象:

```txt
Example ob;  // now ob.inches exists
```

因此，可以结合使用标识符 inches 和特定的对象，来引用实际的内存单元（对于成员函数，可以省略对象名，但对象被认为是指针指向的对象）。

C++允许这样定义一个指向标识符 inches 的成员指针:

```rust
int Example::*pt = &Example::inches;
```

这种指针与常规指针有所差别。常规指针指向特定的内存单元，而 pt 指针并不指向特定的内存单元，因为声明中没有指出具体的对象。指针 pt 指的是 inches 成员在任意 Example 对象中的位置。和标识符 inches 一样，pt 被设计为与对象标识符一起使用。实际上，表达式\*pt 对标识符 inches 的角色做了假设，因此，可以使用对象标识符来指定要访问的对象，使用 pt 指针来指定该对象的 inches 成员。例如，类方法可以使用下面的代码:

```cpp
int Example::*pt = &Example::inches;
Example ob1;
Example ob2;
Example *pq = new Example;
cout << ob1.*pt << endl; // display inches member of ob1
cout << ob2.*pt << endl; // display inches member of ob2
cout << po->*pt << endl; // display inches member of *po
```

其中，\*和->\*都是成员解除引用运算符（member dereferencing operator）。声明对象（如 obl）后，obl.\*pi 指的将是 obl 对象的 inches 成员。同样，pq->\*pt 指的是 pq 指向的对象的 inches 成员。

改变上述示例中使用的对象，将改变使用的 inches 成员。不过也可以修改 pt 指针本身。由于 feet 的类型与 inches 相同，因此可以将 pt 重新设置为指向 feet 成员（而不指向 inches 成员），这样 ob1.\*pt 将是 ob1 的 feet 成员:

```cpp
pt = &Example::feet;      // reset pt
cout << ob1.*pt << endl;  // display feet member of ob1
```

实际上，\*pt 相当于一个成员名，因此可用于标识（相同类型的）其他成员。

也可以使用成员指针来标识成员函数，其语法稍微复杂点。对于不带任何参数、返回值为 void 的函数，声明一个指向该函数的指针的代码如下:

```txt
void (*pf).(); // pf points to a function
```

声明指向成员函数的指针时，必须指出该函数所属的类。例如，下面的代码声明了一个指向 Example 类方法的指针:

```cpp
void (Example::*pf)() const; // pf points to an Example member function
```

这表明 pf 可用于可使用 Example 方法的地方。注意，Example:: \*pf 必须放在括号中，可以将特定成员函数的地址赋给该指针:

```rust
pf = &Example::show_inches;
```

注意，和普通函数指针的赋值情况不同，这里必须使用地址运算符。完成赋值操作后，便可以使用一个对象来调用该成员函数:

```cpp
Example ob3.(20);
(ob3.*pf)(); // invoke show_inches() using the ob3 object
```

必须将 ob3.\*pf 放在括号中，以明确地指出，该表达式表示的是一个函数名。

由于 show\_feet() 的原型与 show\_inches() 相同，因此也可以使用 pf 来访问 show\_feet() 方法:

```cpp
pf = &Example::show_feet;
{ob3.*pf}(); -- // apply.show_feet() to the ob3 object
```

程序清单 E.1 中的类定义包含一个 use\_ptr() 方法，该方法使用成员指针来访问 Example 类的数据成员和函数成员。

程序清单 E.1 memb\_pt.cpp

```cpp
// memb_pt.cpp --- dereferencing pointers to class members
#include <iostream>
using namespace std;

class Example
{
private:
    int feet;
    int_inches;
public:
    Example();
    Example(int ft);
    ~Example();
    void show_in() const;
    void show_ft() const;
    void use_ptr() const;
};

Example::Example()
{
    feet = 0;
    inches = 0;
}

Example::Example(int ft)
{
    feet = ft;
```

```cpp
inches =-12 * feet;
}

Example::~Example()
{
}
void Example::show_in() const
{
    cout << inches << " inches\n";
}

void Example::show_ft() const
{
    cout << feet << " feet\n";
}

void Example::use_ptr() const
{
    Example yard(3);
    int Example::*pt;
    pt = &Example::inches;
    cout << "Set pt to &Example::inches:\n";
    cout << "this->pt: " << this->*pt << endl;
    cout << "yard.*pt: " << yard.*pt << endl;
    pt = &Example::feet;
    cout << "Set pt to &Example::feet:\n";
    cout << "this->pt: " << this->*pt << endl;
    cout << "yard.*pt: " << yard.*pt << endl;
    void (Example::*pf)() const;
    pf = &Example::show_in;
    cout << "Set pf to &Example::show_in:\n";
    cout << "Using (this->*pf)(): ";
    (this->*pf)();
    cout << "Using (yard.*pf)(): ";
    (yard.*pf)();
}

int main(){
{
    Example car(15);
    Example van(20);
    Example garage;

    cout << "car_use_ptr() output:\n";
    car.use_ptr();
    cout << "\nvan.use_ptr() output:\n";
    van.use_ptr();
    return 0;
}
```

下面是程序清单 E.1 中程序的运行情况:

```txt
car.use_ptr()-output:
Set pt to &Example::inches:
this->pt: 180
```

```txt
yard.*pt: 36
Set pt to &Example::feet:
this->pt: 15
yard.*pt: 3
Set pf to &Example::show_in:
Using (this->*pf)(): 180 inches
Using (yard.*pf)(): 36 inches

van.use_ptr() output:
Set pt to &Example::inches:
this->pt: 240
yard.*pt: 36
Set pt to &Example::feet:
this->pt: 20
yard.*pt: 3
Set pf to &Example::show_in:
Using (this->*pf)(): 240 inches
Using (yard.*pf)(): 36 inches
```

这个例子在编译期间给指针赋值。在更复杂的类中，可以使用指向数据成员和方法的成员指针，以便在运行阶段确定与指针关联的成员。

## E.3 alignof (C++11)

计算机系统可能限制数据在内存中的存储方式。例如，一个系统可能要求 double 值存储在编号为偶数的内存单元中，而另一个系统可能要求其起始地址为 8 个整数倍。运算符 alignof 将类型作为参数，并返回一个整数，指出要求的对齐方式。例如，对齐要求可能决定结构中信息的组织方式，如程序清单 E.2 所示。

程序清单 E.2 align.cpp

```cpp
// align.cpp -- checking alignment
#include <iostream>
using namespace std;
struct things1
{
    char ch;
    int a;
    double x;
};
struct things2
{

    int a;
    double x;
    char ch;
};

int main()
{
    things1 th1;
    things2 th2;
    cout << "char alignment: " << alignof(char) << endl;
```

```txt
cout << "int alignment: " << alignof(int) << endl;
cout << "double alignment: " << alignof(double) << endl;
cout << "things1 alignment: " << alignof(things1) << endl;
cout << "things2 alignment: " << alignof(things2) << endl;
cout << "things1 size: " << sizeof(things1) << endl;
cout << "things2 size: " << sizeof(things2) << endl;
return 0;
}
```

下面是该程序在一个系统中的输出:

```yaml
char alignment: 1
int alignment: 4
double alignment: 8
things1 alignment: 8
things2 alignment: 8
things1 size: 16
things2 size: 24
```

两个结构的对齐要求都是8。这意味着结构长度将是8的整数倍，这样创建结构数组时，每个元素的起始位置都是8的整数倍。在程序清单E.2中，每个结构的所有成员只占用13位，但结构要求占用的位数为8的整数倍，这意味着需要填充一些位。在每个结构中，double成员的对齐要求为8的整数倍，但在结构thing1和thing2中，成员的排列顺序不同，这导致thing2需要更多的内部填充，以便其边界处于正确的位置。

## E.4 noexcept (C++11-)

关键字 noexcept 用于指出函数不会引发异常。它也可用作运算符，判断操作数（表达式）是否可能引发异常；如果操作数可能引发异常，则返回 false，否则返回 true。例如，请看下面的声明:

```txt
int hilt(int);
int halt(int) noexcept;
```

表达式 noexcept(hilt) 的结果为 false，因为 hilt() 的声明未保证不会引发异常，但 noexcept(halt) 的结果为 true。

## 附录 F 模板类 string

本附录的技术性较强，但如果您只想了解模板类 string 的功能，可以将重点放在对各种 string 类方法的描述上。

string 类是基于下述模板定义的:

```cpp
template<class charT, class traits = char_traits<charT>,
            class Allocator = allocator<charT> >
class basic_string {...};
```

其中，chatT 是存储在字符串中的类型；traits 参数是一个类，它定义了类型要被表示为字符串时，所必须具备的特征。例如，它必须有 length() 方法，该方法返回被表示为 charT 数组的字符串的长度。这种数组结尾用 charT(0) 值（广义的空值字符）表示。（表达式 charT(0) 将 0 转换为 charT 类型。它可以像类型为 char 时那样为零，也可以是 charT 的一个构造函数创建的对象）。这个类还包含用于对值进行比较等操作的方法。Allocator 参数是用于处理字符串内存分配的类。默认的 allocator&lt;char&gt;模板按标准方式使用 new 和 delete。

有 4 种预定义的具体化:

```c
typedef basic_string<char> string;
typedef basic_string<char16_t> u16string;
typedef basic_string<char32_t> u32string;
typedef basic_string<wchar_t> wstring;
```

上述具体化又使用下面的具体化:

```erb
char_traits<char>
allocator<char>
char_traits<char16_t>
allocator<char_16>
char_traits<char_32>
allocator<char_32>
char_traits<wchar_t>
allocator<wchar_t>
```

除 char 和 wchar\_t 外，还可以通过定义 traits 类和使用 basic\_string 模板来为其他一些类型创建一个 string 类。

## F.1 13 种类型和一个常量

模板 basic\_string 定义了几种类型，供以后定义方法时使用:

```cpp
typedef traits
typedef typename traits::char_type
typedef Allocator
typedef typename Allocator::size_type
typedef typename Allocator::difference_type
typedef typename Allocator::reference
typedef typename Allocator::const_reference
typedef typename Allocator::pointer
typedef typename Allocator::const_pointer
```

traits 是对应于特定类型（如 char\_traits&lt;char&gt;）的模板参数；traits\_type 将成为该特定类型的 typedef。下述表示法意味着 char\_type 是 traits 表示的类中定义的一个类型名:

```rust
typedef typename traits::char_type value_type;
```

关键字 typename 告诉编译器，表达式 trait::char\_type 是一种类型。例如，对于 string 具体化，value\_type 为 char。

size\_type 与 size\_of 的用法相似，只是它根据存储的类型返回字符串的长度。对于 string 具体化，将根据 char 返回字符串的长度，在这种情况下，size\_type 与 size\_of 等效。size\_type 是一种无符号类型。

difference\_type 用于度量字符串中两个元素之间的距离（单位为元素的长度）。通常，它是底层类型 size\_type 有符号版本。

对于 char 具体化来说，pointer 的类型为 char \*，而 reference 的类型为 char & 类型。然而，如果要为自己设计的类型创建具体化，则这些类型（pointer 和 reference）可以指向类，与基本指针和引用有相同的特征。

为将标准模板库（STL）算法用于字符串，该模板定义了一些迭代器类型:

```cpp
typedef (models random access iterator)          iterator;
typedef (models random access iterator)          const_iterator;
typedef std::reverse_iterator<iterator>       reverse_iterator;
typedef std::reverse_iterator<const_iterator>  const_reverse_iterator;
```

该模板还定义了一个静态常量:

```txt
static const size_type npos = -1;
```

由于 size\_type 是无符号的，因此将 -1 赋给 npos 相当于将最大的无符号值赋给它，这个值比可能的最大数组索引大 1。

## F.2 数据信息、构造函数及其他

可以根据其效果来描述构造函数。由于类的私有部分可能依赖于实现，因此可根据公用接口中可用的数据来描述这些效果。表 F.1 列出了一些方法，它们的返回值可用来描述构造函数和其他方法的效果。注意，其中的大部分术语来自 STL。

表 F.1 一些 string 数据方法

| 方法 | 返回值 |
| --- | --- |
| begin() | 指向字符串第一个字符的迭代器 |
| cbegin() | 一个 const_iterator,指向字符串中的第一个字符(C++11) |
| end() | 为超尾值的迭代器 |
| cend() | 为超尾值的 const_iterator(C++11) |
| rbegin() | 为超尾值的反转迭代器 |
| crbegin() | 为超尾值的反转 const_iterator(C++11) |
| rend() | 指向第一个字符的反转迭代器 |
| crend() | 指向第一个字符的反转 const_iterator(C++11) |
| size() | 字符串中的元素数,等于 begin()到 end()之间的距离 |
| length() | 与 size()相同 |
| capacity() | 给字符串分配的元素数。这可能大于实际的字符数,capacity()-size()的值表示在字符串末尾附加多少字符后需要分配更多的内存 |
| max_size() | 字符串的最大长度 |
| data() | 一个指向数组第一个元素的 const charT*指针,其第一个 size()元素等于*this 控制的字符串中对应的元素,其下一个元素为 charT 类型的 charT(0)字符(字符串末尾标记)。当 string 对象本身被修改后,该指针可能无效 |
| c_str() | 一个指向数组第一个元素的 const charT*指针,其第一个 size()元素等于*this 控制的字符串中对应的元素,其下一个元素是 charT 类型的 charT(0)字符(字符串尾标识)。当 string 对象本身被修改后,该指针可能无效 |
| get_allocator() | 用于为字符串 object 分配内存的 allocator 对象的副本 |

请注意 begin()、rend()、data() 和 c\_str() 之间的差别。它们都与字符串的第一个字符相关，但相关的方式不同。begin() 和 rend() 方法返回一个迭代器，正如第 16 章讨论的，这是一种广义指针。具体地说，begin() 返回一个正向迭代器模型，而 rend() 返回反转迭代器的一个副本。这两种方法都引用了 string 对象管理的字符串（由于 string 类使用动态内存分配，因此实际的 string 内容不一定位于对象中，因此，我们使用术语“管理”来描述对象和字符串之间的关系）。可以将返回迭代器的方法用于基于迭代器的 STL 算法中。例如，可以使用 STL reverse() 函数来反转字符串的内容:

```txt
string word;
cin >> word;
reverse(word.begin(), word.end());
```

而 data() 和 c\_str() 方法返回常规指针。另外，返回的指针将指向存储字符串字符的数组的第一个元素。该数组可能（但不一定）是 string 对象管理的字符串的副本（string 对象采用的内部表示可以是数组，但不一定非得是数组）。由于返回的指针可能指向原始数据，而原始数据是 const，因此不能用它们来修改数据。另外，当字符串被修改后，将不能保证这些指针是有效的，这表明它们可能指向原始数据。data() 和 c\_str() 的区别在于，c\_str() 指向的数组以空值字符（或与之等价的其他字符）结束，而 data() 只是确保实际的字符串字符是存在的。因此，c\_str() 方法期望接受一个 C-风格字符串参数:

```txt
string file("tofu.man");
ofstream outFile(file.c_str());
```

同样，data()和 size()可用作这种函数的参数，即接受指向数组元素的指针和表示要处理的元素数目的值:

```rust
string vampire("Do not stake me, oh my darling!");
int vlad = byte_check(vampire.data(), vampire.size());
```

C++实现可能将 string 对象的字符串表示为动态分配的 C-风格字符串，并使用 char\* 指针来实现正向迭代器。在这种情况下，实现可能让 begin()、data() 和 c\_str() 都返回同样的指针，但返回指向 3 个不同的数据对象的引用也是合法的（虽然更复杂）。

在 C++11 中，模板类 basic\_string 有 11 个构造函数（在 C++98 中只有 6 个）和一个析构函数:

```cpp
explicit basic_string(const Allocator& a = Allocator());
basic_string(const charT* s, const Allocator& a = Allocator());
basic_string(const charT* s, size_type n, const Allocator& a = Allocator());
basic_string(const basic_string& str);
basic_string(const basic_string& str, const Allocator&);
basic_string(const basic_string& str, size_type pos,
    size_type n = npos, const Allocator& a = Allocator());
basic_string(basic_string&& str) noexcept;
basic_string(const basic_string&& str, const Allocator&);
basic_string(size_type n, charT c, const Allocator& a = Allocator());
template<class InputIterator>
basic_string(InputIterator begin, InputIterator end,
```

```txt
const Allocator& a = Allocator());
basic_string(initializer_list<charT>, const Allocator& = Allocator());
~basic_string();
```

有些新增的构造函数以不同的方式处理参数。例如， $C++98$  包含如下复制构造函数:

```txt
basic_string(const basic_string& str, size_type pos = 0,
    size_type n = npos, const Allocator& a = Allocator());
```

而 C++11 用三个构造函数取代了它——上述列表中的第 2\~4 个，这提高了编码效率。真正新增的只有移动构造函数（使用右值引用的构造函数，这在第 18 章讨论过）以及使用 initializer\_list 参数的构造函数。

注意到大多数构造函数构造函数都有一个下面这样的参数:

```txt
const Allocator& a = Allocator()
```

Allocator 是用于管理内存的 allocator 类的模板参数名；Allocator() 是这个类的默认构造函数。因此，在默认情况下，构造函数将使用 allocator 对象的默认版本，但它们使得能够选择使用 allocator 对象的其他版本。下面分别介绍这些构造函数。

## E.2.1 默认构造函数

默认构造函数的原型如下:

```javascript
explicit basic_string(const Allocator& a = Allocator());
```

通常，接受 allocator 类的默认参数，并使用该构造函数来创建空字符串:

```dart
string bean;
wstring theory;
```

调用该默认构造函数后，将存在下面的关系:

data()方法返回一个非空指针，可以将该指针加上0;
- size()方法返回0;
- capacity()的返回值不确定。

将 data() 返回的值赋给指针 str 后，第一个条件意味着 str + 0 是有效的。

## F.2.2 使用 C-风格字符串的构造函数

使用 C-风格字符串的构造函数让您能够将 string 对象初始化为一个 C-风格字符串；从更普遍的意义上看，它使得能够将 charT 具体化初始化为一个 charT 数组:

```javascript
basic_string(const charT* s, const Allocator& a = Allocator());
```

为确定要复制的字符数，该构造函数将 traits::length() 方法用于 s 指向的数组（s 不能为空指针）。例如，下面的语句使用指定的字符串来初始化 toast 对象:

```txt
string toast("Here's looking at you, kid.");
```

char 类型的 traits::length() 方法将使用空值字符来确定要复制多少个字符。

该构造函数被调用后，将存在下面的关系:

- data()方法返回一个指针，该指针指向数组s的一个副本的第一个元素；
- size()方法返回的值等于 trains::length()的值;
- capacity()方法返回一个至少等于 size()的值。

## F.2.3 使用部分 C-风格字符串的构造函数

使用部分 C-风格字符串的构造函数让您能够使用 C-风格字符串的一部分来初始化 string 对象；从更广泛的意义上说，该构造函数使得能够使用 charT 数组的一部分来初始化 charT 具体化:

```javascript
basic_string(const charT* s, size_type n, const Allocator& a = Allocator());
```

该构造函数将 s 指向的数组中的 n 个字符复制到构造的对象中。请注意，如果 s 包含的字符数少于 n，则复

制过程将不会停止。如果 n 大于 s 的长度，该构造函数将把字符串后面的内存内容解释为 charT 类型的数据。

该构造函数要求 s 不能是空值指针，同时 n<npos（npos 是一个静态类常量，它是字符串可能包含的最大元素数目）。如果 n 等于 npos，该构造函数将引发一个 out\_of\_range 异常（由于 n 的类型为 size\_type，而 npos 是 size\_type 的最大值，因此 n 不能大于 npos）；否则，在该构造函数被调用后，将存在下面的关系:

● data()方法返回一个指针，该指针指向数组 s 的副本的第一个元素；
- size()方法返回 n;
- capacity()方法返回一个至少等于 size()的值。

## F.2.4 使用左值引用的构造函数

复制构造函数类似于下面这样:

```cpp
basic_string(const basic_string& str);
```

它使用一个 string 参数初始化一个新的 string 对象:

```txt
string mel("I'm ok!");
string ida(mel);
```

其中，ida 将是 mel 管理的字符串副本。

下一个构造函数要求您指定一个分配器:

```c
basic_string(const basic_string& str, const Allocator&);
```

调用这两个构造函数中的任何一个后，将存在如下关系:

- data()方法返回一个指针，该指针指向分配的数组副本，该数组的第一个元素是 str.data()指向的；
- size()方法返回 str.size()的值;
- capacity()方法返回一个至少等于 size()的值。

再下一个构造函数让您能够指定多项内容:

```txt
basic_string(const basic_string& str, size_type pos, size_type n = npos,
    const Allocator& a = Allocator());
```

第二个参数（pos）指定了源字符串中的位置，将从这个位置开始进行复制:

```txt
string att("Telephone home.");
string et(att, 4);
```

位置编号从 0 开始，因此，位置 4 是字符 p。所以，et 被初始化为 “phone home”。

```c
第 3 个参数 n 是可选的，它指定要复制的最大字符数目，因此下面的语句将 pt 初始化为字符串 “phone”:
string att("Telephone home.");
string pt(att, 4, 5);
```

然而，该构造函数不能跨越源字符串的结尾，例如，下面的语句将在复制句点后停止:

```txt
string pt(att, 4, 200)
```

因此，该构造函数实际复制的字符数量等于 n 和 str.size()-pos 中较小的一个。

该构造函数要求 pos 不大于 str.size()，也就是说，被复制的初始位置必须位于源字符串中。如果情况并非如此，该构造函数将引发 out\_of\_range 异常；否则，该构造函数被调用后，copy\_len 将是 n 和 str.size()-pos 中较小的一个，并存在下面的关系:

- data()方法返回一个指向字符串的指针，该字符串包含copy\_len个元素，这些元素是从str的pos位置开始复制而得到的；
size()方法返回 copy\_len;
- capacity()方法返回一个不小于 size()的值。

## F.2.5 使用右值引用的构造函数（C++11）

C++11 给 string 类添加了移动语义。正如第 18 章介绍的，这意味着添加一个移动构造函数，它使用右

值引用而不是左值引用:

basic\_string(basic\_string&& str) noexcept;

在实参为临时对象时将调用这个构造函数:

```c
string one("din");      // C-style string constructor
string two(one);         // copy constructor - one is an lvalue
string three(one+two);  // move constructor, sum is an rvalue
```

正如第 18 章讨论的，three 将获取 operator + () 创建的对象的所有权，而不是将该对象复制给 three，再销毁原始对象。

第二个使用右值引用的构造函数让您能够指定分配器:

```c
basic_string(const basic_string&& str, const Allocator&);
```

调用这两个构造函数中的任何一个后，将存在如下关系:

- data()方法返回一个指针，该指针指向分配的数组副本，该数组的第一个元素是 str.data()指向的；
- size()方法返回 str.size()的值;
- capacity()方法返回一个至少等于 size()的值。

## F.2.6 使用一个字符的 n 个副本的构造函数

使用一个字符的 n 个副本的构造函数创建一个由 n 个 c 组成的 string 对象:

```txt
basic_string(size_type n, charT c, const Allocator& a = Allocator());
```

该构造函数要求 n<npos。如果 n 等于 npos，该构造函数将引发 out\_of\_range 异常；否则，该构造函数被调用后，将存在下面的关系:

- data()方法返回一个指向字符串第一个元素的指针，该字符串由 n 个元素组成，其中每个元素的值都为 c;
- size()方法返回 n;
- capacity()方法返回不小于 size()的值。

## F.2.7 使用区间的构造函数

使用区间的构造函数使用一个用迭代器定义的、STL-风格的区间:

```txt
template<class InputIterator>
basic_string(InputIterator begin, InputIterator end,
                    const Allocator& a = Allocator());
```

begin 迭代器指向源字符串中要复制的第一个元素，end 指向要复制的最后一个元素的后面。

这种构造函数可用于数组、字符串或STL容器:

```txt
char cole[40] = "Old King Cole was a merry old soul.";
string title(cole + 4, cole + 8);
vector<char> input;
char ch;
while (cin.get(ch) && ch != '\n')
    input.push_back(ch);
string str_input(input.begin(), input.end());
```

在第一种用法中，InputIterator 的类型为 const char \*；在第二种用法中，InputIterator 的类型为 vector&lt;char&gt;::iterator。

调用该构造函数后，将存在下面的关系:

- data()方法返回一个指向字符串的第一个元素的指针，该字符串是通过复制区间[begin, end)中的元素得到的；
- size()方法返回 begin 到 end 之间的距离（度量距离时，使用的单位为对迭代器解除引用得到的数

据类型的长度);

\- capacity()方法返回一个不小于 size()的值。

## F.2.8 使用初始化列表的构造函数（C++11）

这个构造函数接受一个 initializer\_list&lt;charT&gt;参数:

```txt
basic_string(initializer_list<charT> il, const Allocator& a = Allocator());
```

可将一个用大括号括起的字符列表作为参数:

```javascript
string slow({'s', 'n', 'a', 'i', 'l'});
```

这并非初始化 string 的最方便方式，但让 string 的接口类似于 STL 容器类。

initializer\_list 类包含成员函数 begin() 和 end()，调用该构造函数的影响与调用使用区间的构造函数相同:

```javascript
basic_string(il.begin(), il.end(), a);
```

## F.2.9 内存杂记

有些方法用于处理内存，如清除内存的内容、调整字符串长度或容量。表 F.2 列出了一些与内存相关的方法。

表 F.2 一些与内存有关的方法

| 方法 | 作用 |
| --- | --- |
| void resize(size_type n) | 如果n>npos,将引发out_of_range异常;否则,将字符串的长度改为n,如果n |
| void resize(size_type n, charT c) | 如果n>npos,将引发out_of_range异常;否则,将字符串长度改为n,如果n |
| void reserve(size_type res_arg = 0) | 将capacity()设置为大于或等于res_arg。由于这将重新分配字符串,因此以前的引用、迭代器和指针将无效 |
| void shrink_to_fit() | 请求让capacity()的值与size()相同,这是C++11新增的 |
| void clear() noexcept | 删除字符串中所有的字符 |
| bool empty()const noexcept | 如果size()==0,-则返回true |

## F.3 字符串存取

有 4 种方法可以访问各个字符，其中两种方法使用[]运算符，另外两种方法使用 at() 方法:

```txt
reference operator[](size_type pos);
const_reference operator[](size_type pos) const;
reference at(size_type n);
const_reference at(size_type-n) const;
```

第一个 operator[]() 方法使得能够使用数组表示法来访问字符串的元素，可用于检索或更改值。第二个 operator[]() 方法可用于 const 对象，但只能用于检索值:

```javascript
string word("tack");
cout << word[0];    // display the t = _
word[3] = 't';     // overwrite the k with a t
const ward("garlic");
cout << ward[2];    // display the r
```

at()方法提供了相似的访问功能，只是索引是通过函数参数提供的:

```txt
string word("tack");
cout << word.at(0);    // display the t
```

差别在于（除语法差别外）:at()方法执行边界检查，如果 pos>=size()，将引发 out\_of\_range 异常。pos 的类型为 size\_type，是无符号的，因此 pos 的值不能为负；而 operator[]() 方法不进行边界检查，因此，如果 pos>=size()，则其行为将是不确定的（如果 pos==size()，const 版本将返回空值字符的等价物）。

因此，可以在安全性（使用 at() 检测异常）和执行速度（使用数组表示）之间进行选择。

还有一个这样的函数，它返回原始字符串的子字符串:

```txt
basic_string substr(size_type pos = 0, size_type n = npos) const;
```

它返回一个字符串——这是从 pos 开始，复制 n 个字符（或到字符串尾部）得到的。例如，下面的代码将 pet 初始化为 “donkey”:

```javascript
string message("Maybe the donkey will learn to sing.");
string pet(message.substr(10, 6));
```

C++11 新增了如下四个存取方法:

```cpp
const charT& front() const;
charT& front();
const charT& back() const;
charT& back();
```

其中 front() 方法访问 string 的第一个元素，相当于 operator[] (0); back() 方法访问 string 的最后一个元素，相当于 operator[] (size() - 1)。

## F.4 基本赋值

在 C++11 中，有 5 个重载的赋值方法，在 C++98 的基础上增加了两个:

```c
basic_string& operator=(const basic_string& str);
basic_string& operator=(const charT* s);
basic_string& operator=(charT c);
basic_string& operator=(basic_string&& str) noexcept;  // C++11
basic_string& operator=(initializer_list<charT>);      // C++11
```

第一个方法将一个 string 对象赋给另一个；第二个方法将 C-风格字符串赋给 string 对象；第三个方法将一个字符赋给 string 对象；第四个方法使用移动语义，将一个右值 string 对象赋给一个 string 对象；第五个方法让您能够使用初始化列表进行赋值。因此，下面的操作都是可能的:

```txt
string name("George Wash");
string pres, veep, source, join, awkward;
pres = name;
veep = "Road Runner";
source = 'X';
join = name + source;   // now with move semantics!
awkward = {'C','l','o','u','s','e','a','u'};
```

## F.5 字符串搜索

string 类提供了 6 种搜索函数，其中每个函数都有 4 个原型。下面简要地介绍它们。

## F.5.1 find()系列

在 C++11 中，find() 的原型如下:

```c
size_type find (const basic_string& str, size_type pos = 0) const noexcept;
size_type find (const charT* s, size_type pos = 0) const;
size_type find (const charT* s, size_type pos, size_type n) const;
size_type find (charT c, size_type pos = 0) const noexcept;
```

第一个返回 str 在调用对象中第一次出现时的起始位置。搜索从 pos 开始，如果没有找到子字符串，将返回 npos。

下面的代码在一个字符串中查找字符串 “hat” 的位置:

```txt
string longer("That is a funny hat.");
string shorter("hat");
size_type loc1 = longer.find(shorter);          // sets loc1 to 1
size_type loc2 = longer.find(shorter, loc1 + 1); // sets loc2 to 16
```

由于第二条搜索语句从位置 2 开始（That 中的 a），因此它找到的第一个 hat 位于字符串尾部。要测试是否失败，可使用 string::npos 值:

```typescript
if (loc1 == string::npos)
    cout << "Not found\n";
```

第二个方法完成同样的工作，但它使用字符数组而不是 string 对象作为子字符串:

```javascript
size_type loc3 = longer.find("is");          //sets loc3 to 5
```

第三个方法完成相同的工作，但它只使用字符串 s 的前 n 个字符。这与使用 basic\_string（const charT \*s, size\_type n）构造函数，然后将得到的对象用作第一种格式的 find() 的 string 参数的效果完全相同。例如，下面的代码搜索子字符串 “fun”:

```txt
size_type loc4 = longer.find("funds", 3);          //sets loc4 to 10
```

第四个方法的功能与第一个相同，但它使用一个字符而不是 string 对象作为子字符串:

```txt
size_type loc5 = longer.find('a');          //sets loc5 to 2
```

## F.5.2 rfind( )系列

rfind()方法的原型如下:

```txt
size_type rfind(const basic_string& str,
            size_type pos = npos) const noexcept;
size_type rfind(const charT* s, size_type pos = npos) const;
size_type rfind(const charT* s, size_type pos, size_type n) const;
size_type rfind(charT c, size_type pos = npos) const noexcept;
```

这些方法与相应 find() 方法的工作方式相似，但它们搜索字符串最后一次出现的位置，该位置位于 pos 之前（包括 pos）。如果没有找到，该方法将返回 npos。

下面的代码从字符串末尾开始查找子字符串 “hat” 的位置:

```txt
string longer("That is a funny hat.");
string shorter("hat");
size_type loc1 = longer.rfind(shorter);          // sets loc1 to 16
size_type loc2 = longer.rfind(shorter, loc1 - 1); // sets loc2 to 1
```

## F.5.3 find\_first\_of()系列

find\_first\_of()方法的原型如下:

```txt
size_type find_first_of(const basic_string& str,
                    size_type pos = 0) const noexcept;
```

```c
size_type find_first_of(const-charT* s, size_type pos, size_type n) const;
size_type find_first_of(const-charT* s, size_type pos = 0) const;
size_type find_first_of(charT c, size_type pos = 0) const noexcept;
```

这些方法与对应 find() 方法的工作方式相似，但它们不是搜索整个子字符串，而是搜索子字符串中的字符首次出现的位置。

```c
string longer("That is a funny hat.");
string shorter("fluke");
size_type loc1 = longer.find_first_of(shorter);  // sets loc1 to 10
size_type loc2 = longer.find_first_of("fat");    // sets loc2 to-2
```

在 longer 中，首次出现的 fluke 中的字符是 funny 中的 f，而首次出现的 fat 中的字符是 That 中的 a。

## F.5.4 find\_last\_of()系列

find\_last\_of()方法的原型如下:

```txt
size_type find_last_of (const basic_string& str,
            size_type pos = npos) const noexcept;
size_type find_last_of (const charT* s, size_type-pos, size_type_n) const;
size_type find_last_of (const charT* s, size_type pos = npos) const;
size_type find_last_of (charT_c, size_type pos= npos) const noexcept;
```

这些方法与对应 rfind() 方法的工作方式相似，但它们不是搜索整个子字符串，而是搜索子字符串中的字符出现的最后位置。

下面的代码在一个字符串中查找字符串 “hat” 和 “any” 中字母最后出现的位置:

```txt
string longer("That is a funny hat.");
string shorter("hat");
size_type loc1 = longer.find_last_of(shorter);  // sets loc1 to 18
size_type loc2 = longer.find_last_of("any");   // sets loc2 to 17
```

在 longer 中，最后出现的 hat 中的字符是 hat 中的 t，而最后出现的 any 中的字符是 hat 中的 a。

## F.5.5 find\_first\_not\_of()系列

find\_first\_not\_of()方法的原型如下:

```txt
size_type find_first_not_of(const basic_string& str,
                    size_type pos = 0) const noexcept;
size_type find_first_not_of(const charT* s, size_type pos,
                    size_type n) const;
size_type find_first_not_of(const charT* s, size_type pos = 0) const;
size_type find_first_not_of(charT c, size_type pos = 0) const noexcept;
```

这些方法与对应 find\_first\_of() 方法的工作方式相似，但它们搜索第一个不位于子字符串中的字符。

下面的代码在字符串中查找第一个没有出现在 “This” 和 “Thatch” 中的字母:

```txt
string longer("That is a funny hat.");
string shorter("This");
size_type loc1 = longer.find_first_not_of(shorter);  // sets loc1 to 2
size_type loc2 = longer.find_first_not_of("Thatch"); // sets loc2 to 4
```

在 longer 中，That 中的 a 是第一个在 This 中没有出现的字符，而字符串 longer 中的第一个空格是第一个没有在 Thatch 中出现的字符。

## F.5.6 find\_last\_not\_of()系列

find\_last\_not\_of()方法的原型如下:

```c
size_type find_last_not_of (const basic_string& str,
                    size_type pos = npos) const noexcept;
size_type find_last_not_of (const charT* s, size_type pos,
                    size_type n) const;
size_type find_last_not_of (const charT* s,
                    size_type pos_ = npos) const;
size_type find_last_not_of (charT c, size_type pos = npos) const noexcept;
```

这些方法与对应 find\_last\_of() 方法的工作方式相似，但它们搜索的是最后一个没有在子字符串中出现的字符。

下面的代码在字符串中查找最后一个没有出现在“That.”中的字符:

```txt
string_longer("That.is.a funny hat.");
string_shorter("That.");
size_type loc1 = longer.find_last_not_of(shorter); // sets_loc1 to 15;
size_type loc2 = -longer.find_last_not_of(shorter, 10); // sets_loc2 to 10;
```

在 longer 中，最后的空格是最后一个没有出现在 shorter 中的字符，而 longer 字符串中的 f 是搜索到位置 10 时，最后一个没有出现在 shorter 中的字符。

## F.6 比较方法和函数

string 类提供了用于比较 2 个字符串的方法和函数。下面是方法的原型:

```c
int compare(const basic_string& str) const noexcept;

int compare(size_type pos1, size_type n1,
    const basic_string& str) const;
int compare(size_type.pos1, size_type n1,
    const basic_string& str,
    size_type pos2, size_type n2) const;
int compare(const charT* s) const;
int compare(size_type pos1, size_type n1, const charT* s) const;
int compare(size_type pos1, size_type n1,
    const charT* s, size_type n2.)const;
```

这些方法使用traits::compare()方法，后者是为用于字符串的字符类型定义的。如果根据traits::compare()提供的顺序，第一个字符串位于第二个字符串之前，则第一个方法将返回一个小于0的值；如果这两个字符串相同，则它将返回0；如果第一个字符串位于第二个字符串的后面，则它将返回一个大于0的值。如果较长的字符串的前半部分与较短的字符串相同，则较短的字符串将位于较长的字符串之前。

```c
string s1("bellflower");
string s2("bell");
string s3("cat");
int a13 = s1-compare(s3); // a13 is < 0
int a12 = s1-compare(s2); // a12 is > 0
```

第二个方法与第一个方法相似，但它进行比较时，只使用第一个字符串中从位置 pos1 开始的 n1 个字符。

下面的示例将字符串 s1 的前 4 个字符同字符串 s2 进行比较:

```txt
string-s1("bellflower");
string s2("bell");
int a2 = s1.compare(0, 4, s2); // a2 is 0
```

第三个方法与第一个方法相似，但它使用第一个字符串中从pos1位置开始的n1个字符和第二个字符串

中从 pos2 位置开始的 n2 个字符进行比较。例如，下面的语句将对 stout 中的 out 和 about 中的 out 进行比较:

```txt
string st1("stout boar");
string st2("mad about ewe");
int a3 = st1.compare(2, 3, st2, 6, 3);  // a3 is 0
```

第四个方法与第一个方法相似，但它将一个字符数组而不是 string 对象作为第二个字符串。

第五和六个方法与第三个方法相似，但将一个字符串数组而不是 string 对象作为第二个字符串。

非成员比较函数是重载的关系运算符:

```txt
operator==()
operator<()
operator<=()
operator>()
operator>=()
operator!=()
```

每一个运算符都被重载，使之将 string 对象与 string 对象进行比较、将 string 对象与 C-风格字符串进行比较、将 C-风格字符串与 string 对象进行比较。它们都是根据 compare() 方法定义的，因此提供了一种在表示方面更为方便的比较方式。

## F.7 字符串修改方法

string 类提供了多个用于修改字符串的方法，其中绝大多数都拥有大量的重载版本，因此可用于 string 对象、字符串数组、单个字符和迭代器区间。

## F.7.1 用于追加和相加的方法

可以使用重载的+=运算符或 append()方法将一个字符串追加到另一个字符串的后面。如果得到的字符串长于最大字符串长度，将引发 length\_error 异常。+=运算符使得能够将 string 对象、字符串数组或单个字符追加到 string 对象的后面:

```c
basic_string& operator+=(const basic_string& str);
basic_string& operator+=(const charT* s);
basic_string& operator+=(charT c);
```

append()方法也使得能够将 string 对象、字符串数组或单个字符追加到 string 对象的后面。此外，通过指定初始位置和追加的字符数，或者通过指定区间，还可以追加 string 对象的一部分。通过指定要使用字符串中的多少个字符，可以追加字符串的一部分。追加字符的版本使得能够指定要复制该字符的多少个实例。下面是各种 append()方法的原型:

```cpp
basic_string& append(const basic_string& str);
basic_string& append(const basic_string& str, size_type pos,
                    size_type n);
template<class InputIterator>
  basic_string& append(InputIterator first, InputIterator last);
basic_string& append(const charT* s);
basic_string& append(const charT* s, size_type n);
basic_string& append(size_type n, charT c);  // append n copies of c
void push_back(charT c);                  // appends 1 copy of c
```

下面是几个示例:

```txt
string test("The");
test.append("ory");  // test is "Theory"
test.append(3,!!');  // test is "Theory!!!"
```

operator+()函数被重载，以便能够拼接字符串。该重载函数不修改字符串，而是创建一个新的字符串，该字符串是通过将第二个字符串追加到第一个字符串后面得到的。加法函数不是成员函数，它们使得能够将 string 对象和 string 对象、string 对象和字符串数组、字符串数组和 string 对象、string 对象和字符以及字符和 string 对象相加。下面是一些例子:

```txt
string st1("red");
string st2("rain");
string st3 = st1 + "uce";  // st3 is "reduce"
string st4 = 't' + st2;    // st4 is "train"
string st5 = st1 + st2;    // st5 is "redrain"
```

## F.7.2 其他赋值方法

除了基本的赋值运算符外，string 类还提供了 assign() 方法，该方法使得能够将整个字符串、字符串的一部分或由相同字符组成的字符序列赋给 string 对象。下面是各种 assign() 方法的原型:

```cpp
basic_string& assign(const basic_string& str);
basic string& assign(basic_string&& str) noexcept;  // C++11
basic_string& assign(const basic_string& str, size_type pos,
                    size_type n);
basic_string& assign(const charT* s, size_type n);
basic_string& assign(const charT* s);
basic_string& assign(size_type n, charT c); // assign n copies of c
template<class InputIterator>
  basic_string& assign(InputIterator first, InputIterator last);
basic_string& assign(initializer_list<charT>);  // C++11
```

下面是几个例子:

```rust
string test;
string stuff("set tubs clones ducks");
test.assign(stuff, 1, 5);    // test is "et tu"
test.assign(6, '#");          // test is "########"
```

接受右值引用作为参数的 assign() 方法是 C++11 新增的，它支持移动语义；另一个新增的 assign() 方法让您能够将 initializer\_list 赋给 string 对象。

## F.7.3 插入方法

insert()方法使得能够将 string 对象、字符串数组或几个字符插入到 string 对象中。这个方法与 append() 方法相似，但它还接受另一个指定插入位置的参数，该参数可以是位置，也可以是迭代器。数据将被插入到插入点的前面。有几种方法返回一个指向得到的字符串的引用。如果 pos1 超过了目标字符串结尾，或者 pos2 超过了要插入的字符串结尾，该方法将引发 out\_of\_range 异常。如果得到的字符串长于最大长度，该方法将引发 length\_error 异常。下面是各种 insert() 方法的原型:

```c
basic_string& insert(size_type pos1, const basic_string& str);
basic_string& insert(size_type pos1, const basic_string& str,
            size_type-pos2, size_type n);
basic_string& insert(size_type-pos, const charT* s, size_type n);
basic_string& insert(size_type-pos, const charT* s);
basic_string& insert(size_type pos, size_type n, charT c);
iterator insert(const_iterator p, charT -c);
iterator insert(const_iterator p, size_type n, charT -c);
template<class InputIterator>
    void insert(iterator p, InputIterator first, InputIterator last);
iterator insert(const_iterator p, initializer_list<charT>); // C++11
```

例如，下面的代码将字符串 “former” 字符串插入到 “The banker.” 中 b 的前面:

```javascript
string st3("The banker.");
st3.insert(4, "former ");
```

而下面的代码将字符串 “waltzed”（不包括！，它是第9个字符）插入到 “The former banker.” 末尾的句号之前:

```javascript
st3.insert(st3.size() - 1, " waltzed!", 8);
```

## F.7.4 清除方法

erase()方法从字符串中删除字符，其原型如下:

```c
basic_string& erase(size_type pos = 0, size_type n = npos);
iterator erase(const_iterator position);
iterator erase(const_iterator first, iterator last);
void pop_back();
```

第一种格式将从 pos 位置开始，删除 n 个字符或删除到字符串尾。第二种格式删除迭代器位置引用的字符，并返回指向下一个元素的迭代器；如果后面没有其他元素，则返回 end()。第三种格式删除区间[first, last) 中的字符，即从 first（包括）到 last（不包括）之间的字符；它返回最后一个迭代器，该迭代器指向最后一个被删除的元素后面的一个元素。最后，方法 pop\_back() 删除字符串中的最后一个字符。

## F.7.5 替换方法

各种 replace()方法都指定了要替换的字符串部分和用于替换的内容。可以使用初始位置和字符数目或迭代器区间来指定要替换的部分。替换内容可以是 string 对象、字符串数组，也可以是特定字符的多个实例。对于用于替换的 string 对象和数组，可以通过指定特定部分（使用位置和计数或只使用计数）或迭代器区间做进一步的修改。下面是各种 replace()方法的原型:

```c
basic_string& replace(size_type pos1, size_type n1, const basic_string& str);
basic_string& replace(size_type pos1, size_type n1, const basic_string& str,
            size_type pos2, size_type n2);
basic_string& replace(size_type pos, size_type n1, const charT* s,
            size_type n2);
basic_string& replace(size_type pos, size_type n1, const charT* s);
basic_string& replace(size_type pos, size_type n1, size_type n2, charT c);
basic_string& replace(const_iterator i1, const_iterator i2,
            const basic_string& str);
basic_string& replace(const_iterator i1, const_iterator i2,
            const charT* s, size_type n);
basic_string& replace(const_iterator i1, const_iterator i2,
            const charT* s);
basic_string& replace(const_iterator i1, const_iterator i2,
            size_type n, charT c);
template<class InputIterator>
    basic_string& replace(const_iterator i1, const_iterator i2,
        InputIterator j1, InputIterator j2);
basic_string& replace(const_iteraor i1, const_iteraor i2,
        initializer){list<charT> il);
```

下面是一个例子:

```java
string test("Take a right turn at Main Street.");
test.replace(7,5,"left"); // replace right with left
```

注意，您可以使用 find()来找出要在 replace()中使用的位置:

```cpp
string s1 = "old";
string s2 = "mature";
string s3 = "The old man and the sea";
string::size_type pos = s3.find(s1);
if (pos != string::npos)
    s3.replace(pos, s1.size(), s2);
```

上述代码将 old 替换为 mature。

## F.7.6 其他修改方法:copy()和 swap()

copy()方法将 string 对象或其中的一部分复制到指定的字符串数组中:

```txt
size_type copy(charT* s, size_type n, size_type pos = 0) const;
```

其中，s 指向目标数组，n 是要复制的字符数，pos 指出从 string 对象的什么位置开始复制。复制将一直进行下去，直到复制了 n 个字符或到达 string 对象的最后一个字符。函数返回复制的字符数，该方法不追加空值字符，同时由程序员负责检查数组的长度是否足够存储复制的内容。

警告:copy()方法不追加空值字符，也不检查目标数组的长度是否足够。

swap()方法使用一个时间恒定的算法来交换两个 string 对象的内容:

```txt
void swap(basic_string& str);
```

## F.8 输出和输入

string 类重载了<<运算符来显示 string 对象，该运算符返回 istream 对象的引用，因此可以拼接输出:

```txt
string claim("The string class has many features.");
cout << claim << endl;
```

string 类重载了>>运算符，使得能够将输入读入到字符串中:

```vhdl
string=who;
cin >> who;
```

到达文件尾、读取字符串允许的最大字符数或遇到空白字符后，输入将终止（空白的定义取决于字符集以及 charT 表示的类型）。

有两个 getline()函数，第一个的原型如下:

```cpp
template<class charT, class traits, class Allocator>
  basic_istream<charT,traits>& getline(basic_istream<charT,traits>& is,
              basic_string<charT,traits,Allocator>& str, charT delim);
```

这个函数将输入流 is 中的字符读入到字符串 str 中，直到遇到定界字符 delim、到达文件尾或者到达字符串的最大长度。delim 字符将被读取（从输入流中删除），但不被存储。第二个版本没有第三个参数，同时使用换行符（或其广义形式），而不是 delim:

```cpp
string str1, str2;
getline(cin, str1);      // read to end-of-line
getline(cin, str2, '.');  // read to period
```

# 附录G 标准模板库方法和函数

标准模板库（STL）旨在提供通用算法的高效实现，它通过通用函数（可用于满足特定算法要求的任何容器）和方法（可用于特定容器类实例）来表达这些算法。本附录假设您对 STL 有一定的了解（如通过阅读第 16 章）。例如，本章假设您了解迭代器和构造函数。

## G.1 STL 和 C++11

C++11 对 C++ 语言做了大量修改，本书无法全面介绍，同样 C++11 对 STL 也做了大量修改，本附录无法全面介绍。然而，可以对新增的内容做一总结。

C++11 给 STL 新增了多个元素。首先，它新增了多个容器；其次，给旧容器新增了多项功能；第三，在算法系列中新增了一些模板函数。本附录介绍了所有这些变化，对前两类变化有大致了解将很有帮助。

## G.1.1 新增的容器

C++11 新增了如下容器:array、forward\_list、unordered\_st 以及无序关联容器 unordered\_multiset、unordered\_map 和 unordered\_multimap。

array 容器一旦声明，其长度就是固定的，它使用静态（栈）内存，而不是动态分配的内存。提供它旨在替代数组；array 受到的限制比 vector 多，但效率更高。

容器 list 是一种双向链表，除两端的节点外，每个节点都链接到它前面和后面的节点。forward\_list 是一种单向链表，除最后一个节点外，每个节点都链接到下一个节点。相对于 list，它更紧凑，但受到的限制更多。

与 set 和其他关联容器一样，无序关联容器让您能够使用键快速检索数据，差别在于关联容器使用的底层数据结构为树，而无序关联容器使用的是哈希表。

## G.1.2 对 C++98 容器所做的修改

C++11 对容器类的方法做了三项主要修改。

首先，新增的右值引用使得能够给容器提供移动语义（参见第18章）。因此，STL现在给容器提供了移动构造函数和移动赋值运算符，这些方法将右值引用作为参数。

其次，由于新增了模板类 initilizer\_list（参见第 18 章），因此新增了将 initilizer\_list 作为参数的构造函数和赋值运算符。这使得可以编写类似于下面的代码:

```javascript
vector<int> vi{100, 99, 97, 98};
vi = {96, 99, 94, 95, 102};
```

第三，新增的可变参数模板（variadic template）和函数参数包（parameter pack）使得可以提供就地创建（emplacement）方法。这意味着什么呢？与移动语义一样，就地创建旨在提高效率。请看下面的代码段:

```cpp
class Items
{
    double x;
    double y;
    int m;
```

```txt
public:
    Items();                                // #1
    Items (double xx, double yy, int mm); // #2
    ...
};
...
vector<Items> vt(10);
...
vt.push_back(Items(8.2, 2.8, 3));  //
```

调用 insert() 将导致内存分配函数在 vt 末尾创建一个默认 Items 对象。接下来，构造函数 Items() 创建一个临时 Items 对象，该对象被复制到 vt 的开头，然后被删除。在 C++11 中，您可以这样做:

```javascript
vi.emplace_back(8.2, 2.8, 3);
```

方法 emplace\_back() 是一个可变参数模板，将一个函数参数包作为参数:

```txt
template <class... Args> void emplace_back(Args&&... args);
```

上述三个实参（8.2、2.8 和 3）将被封装到参数 args 中。参数 args 被传递给内存分配函数，而内存分配函数将其展开，并使用接受三个参数的 Items 构造函数（#2），而不是默认构造函数（#1）。也就是说，它使用 Items(args...），这里将展开为 Items(8.2, 2.8, 3)。因此，将在矢量中就地创建所需的对象，而不是创建一个临时对象，再将其复制到矢量中。

STL 在多个就地创建方法中使用了这种技术。

## G.2 大部分容器都有的成员

所有容器都定义了表 G1 列出的类型。在这个表中，x 为容器类型，如 vector&lt;int&gt;；T 为存储在容器中的类型，如 int。表 G1 中的示例阐明了含义

表 G.1

为所有容器定义的类型

| 类型 | 值 |
| --- | --- |
| x::value-type | T,元素类型 |
| x::reference | T &amp; |
| x::const_reference | const T &amp; |
| x::iterator | 指向 T-的迭代器类型,行为与 T*相似 |
| x::const_iterator- | 指向 const.T 的迭代器类型,行为与 const T *相似 |
| x::different_type | 用于表示两个迭代器之间距离的符号整型,如两个指针的差 |
| x::size_type | 无符号整型 size_type 可以表示数据对象的长度、元素数目和下标 |

类定义使用typedef定义这些成员。可以使用这些类型来声明适当的变量。例如，下面的代码使用迂回的方式，将由string对象组成的矢量中的第一个“bonus”替换为“bogus”，以演示如何使用成员类型来声明变量。

```cpp
using_namespace std;
vector<string> input;
string temp;
while (cin >> temp && temp- != "quit")
    input.push_back(temp);
vector<string>::iterator want=
```