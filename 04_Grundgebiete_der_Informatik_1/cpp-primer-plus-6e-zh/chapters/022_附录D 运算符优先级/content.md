# 附录D 运算符优先级

原始 PDF 第 867–869 页。

## 附录 D 运算符优先级

运算符优先级决定了运算符用于值的顺序。C++运算符分为18个优先级组，如表D.1所示。第1组中的运算符的优先级最高，第2组中运算符的优先级次之，依此类推。如果两个运算符被用于同一个操作数，则首先应用优先级高的运算符。如果两个运算符的优先级相同，则C++使用结合性规则来决定哪个运算符结合得更为紧密。同一组中运算符的优先级和结合性相同，不管是从左到右（表中L-R）还是从右到左（表中R-L）结合。从左到右的结合性意味着首先应用最左边的运算符，而从右到左的结合性则意味着首先应用最右边的运算符。

表 D.1 C++运算符的优先级和结合性

<table><tr><td>运算符</td><td>结合性</td><td>含义</td></tr><tr><td colspan="3">优先级第1组</td></tr><tr><td>::</td><td></td><td>作用域解析运算符</td></tr><tr><td colspan="3">优先级第2组</td></tr><tr><td>(表达式)</td><td></td><td>分组</td></tr><tr><td>0-</td><td>L-R</td><td>函数调用</td></tr><tr><td>0-</td><td></td><td>值构造,即-type(expr)</td></tr><tr><td>[-]</td><td></td><td>数组下标</td></tr><tr><td>-&gt;</td><td></td><td>间接成员运算符</td></tr><tr><td></td><td></td><td>直接成员运算符</td></tr><tr><td>const_cast</td><td></td><td>专用的类型转换</td></tr><tr><td>dynamic_cast</td><td></td><td>专用的类型转换</td></tr><tr><td>reinterpret_cast</td><td></td><td>专用的类型转换</td></tr><tr><td>static_cast</td><td></td><td>专用的类型转换</td></tr><tr><td>typeid</td><td></td><td>类型标识</td></tr><tr><td>++</td><td></td><td>加1运算符,后缀</td></tr><tr><td></td><td></td><td>减1运算符,后缀</td></tr></table>

优先级第3组（全是一元运算符）

| ! | R-L | 逻辑非 |
| --- | --- | --- |
|  |  | 位非 |
| + |  | 一元加号(正号) |
|  |  | 一元减号(负号) |
| ++ |  | 加1运算符,前缀 |
|  |  | 减1运算符,前缀 |
| &amp; |  | 地址 |
| * |  | 解除引用(间接值) |
| () |  | 类型转换,-即(type)expr |
| sizeof |  | 长度,以字节为单位 |
| new |  | 动态分配内存 |
| new [ ] |  | 动态分配数组 |
| delete |  | 动态释放内存 |
| delete [ ] |  | 动态释放数组 |

---

850

C++ Primer Plus（第6版）中文版

续表

<table><tr><td>运算符</td><td>结合性</td><td>含 义</td></tr><tr><td colspan="3">优先级第4组</td></tr><tr><td>.*</td><td>L-R</td><td>成员解除引用</td></tr><tr><td>-&gt;*</td><td></td><td>间接成员解除引用</td></tr><tr><td colspan="3">优先级第5组(全是二元运算符)</td></tr><tr><td>*</td><td>L-R</td><td>乘</td></tr><tr><td>/</td><td></td><td>除</td></tr><tr><td>^</td><td></td><td>模(余数)</td></tr><tr><td colspan="3">优先级第6组(全是二元运算符)</td></tr><tr><td>+</td><td>L-R</td><td>加</td></tr><tr><td>-</td><td></td><td>减</td></tr><tr><td colspan="3">优先级第7组</td></tr><tr><td>&lt;&lt;</td><td>L-R</td><td>左移</td></tr><tr><td>&gt;&gt;</td><td></td><td>右移</td></tr><tr><td colspan="3">优先级第8组</td></tr><tr><td>&lt;</td><td>L-R</td><td>小于</td></tr><tr><td>&lt;=</td><td></td><td>小于或等于</td></tr><tr><td>&gt;=</td><td></td><td>大于或等于</td></tr><tr><td>&gt;</td><td></td><td>大于</td></tr><tr><td colspan="3">优先级第9组</td></tr><tr><td>==</td><td>L-R</td><td>等于</td></tr><tr><td>!=</td><td></td><td>不等于</td></tr><tr><td colspan="3">优先级第10组(一元运算符)</td></tr><tr><td>&amp;</td><td>L-R</td><td>按位AND</td></tr><tr><td colspan="3">优先级第11组</td></tr><tr><td>^</td><td>L-R</td><td>按位XOF(异或)</td></tr><tr><td colspan="3">优先级第12组</td></tr><tr><td>|</td><td>L-R</td><td>按位OR</td></tr><tr><td colspan="3">优先级第13组</td></tr><tr><td>&amp;&amp;</td><td>L-R</td><td>逻辑AND</td></tr><tr><td colspan="3">优先级第14组</td></tr><tr><td>||</td><td>L-R</td><td>逻辑OR</td></tr><tr><td colspan="3">优先级第15组</td></tr><tr><td>:?</td><td>R-L</td><td>条件</td></tr><tr><td colspan="3">优先级第16组</td></tr><tr><td>=</td><td>R-L</td><td>简单赋值</td></tr><tr><td>*=</td><td></td><td>乘并赋值</td></tr><tr><td>/=</td><td></td><td>除并赋值</td></tr><tr><td>%=</td><td></td><td>求模并赋值</td></tr><tr><td>+=</td><td></td><td>加并赋值</td></tr><tr><td>-=</td><td></td><td>减并赋值</td></tr><tr><td>&amp;=</td><td></td><td>按位AND并赋值</td></tr><tr><td>^=</td><td></td><td>按位XOR并赋值</td></tr><tr><td>|=</td><td></td><td>按位OR并赋值</td></tr><tr><td>&lt;&lt;=</td><td></td><td>左移并赋值</td></tr><tr><td>&gt;&gt;=</td><td></td><td>右移并赋值</td></tr></table>

---

附录 D 运算符优先级

851

续表

<table><tr><td>运算符</td><td>结合性</td><td>含义</td></tr><tr><td colspan="3">优先级第17组</td></tr><tr><td>throw</td><td>L-R</td><td>引发异常</td></tr><tr><td colspan="3">优先级第18组</td></tr><tr><td>,</td><td>L-R</td><td>将两个表达式合并成一个</td></tr></table>

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
