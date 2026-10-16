16. $\int x\ln (x - 1)\mathrm{d}x.$

17. $\int (x^{2} - 1)\sin 2x\mathrm{d}x.$

18. $\int \frac{\ln^3 x}{x^2} \, \mathrm{d}x$.

19. $\int \mathrm{e}^{\sqrt[3]{x}}\mathrm{d}x.$

20. $\int \cos \ln x\mathrm{d}x.$

21. $\int (\arcsin x)^{2}\mathrm{d}x.$

22. $\int \mathrm{e}^{x}\sin^{2}x\mathrm{d}x.$

23. $\int x\ln^2 x\mathrm{d}x.$

24. $\int \mathrm{e}^{\sqrt{3x + 9}}\mathrm{d}x.$

## 第四节 有理函数的积分

前面已经介绍了求不定积分的两个基本方法——换元积分法和分部积分法,下面简要地介绍有理函数的积分及可化为有理函数的积分.

## 一、有理函数的积分

两个多项式的商 $\frac{P(x)}{Q(x)}$ 称为有理函数,又称有理分式.我们总假定分子多项式 $P(x)$ 与分母多项式 $Q(x)$ 之间没有公因式.当分子多项式 $P(x)$ 的次数小于分母多项式 $Q(x)$ 的次数时,称这有理函数为真分式,否则称为假分式.

利用多项式的除法,总可以将一个假分式化成一个多项式与一个真分式之和的形式,例如第一节例15中的被积函数

$$
\frac {2 x ^ {4} + x ^ {2} + 3}{x ^ {2} + 1} = 2 x ^ {2} - 1 + \frac {4}{x ^ {2} + 1}.
$$

对于真分式 $\frac{P(x)}{Q(x)}$ ，如果分母可分解为两个多项式的乘积

$$
Q (x) = Q _ {1} (x) Q _ {2} (x),
$$

且 $Q_{1}(x)$ 与 $Q_{2}(x)$ 没有公因式，那么它可分拆成两个真分式之和

$$
\frac {P (x)}{Q (x)} = \frac {P _ {1} (x)}{Q _ {1} (x)} + \frac {P _ {2} (x)}{Q _ {2} (x)},
$$

上述步骤称为把真分式化成部分分式之和.如果 $Q_{1}(x)$ 或 $Q_{2}(x)$ 还能再分解成两个没有公因式的多项式的乘积，那么就可再分拆成更简单的部分分式.最后，有理函数的分解式中只出现多项式、 $\frac{P_1(x)}{(x - a)^k}$ 、 $\frac{P_2(x)}{(x^2 + px + q)^l}$ 等三类函数（这里 $p^2 -4q <   0,P_1(x)$ 为小于 $k$ 次的多项式， $P_{2}(x)$ 为小于 $2l$ 次的多项式).多项式的积分容易求得，后两类真分式的积分可参看第二节例3和例27.

下面举几个真分式的积分的例子.

例1 求 $\int \frac{x + 1}{x^2 - 5x + 6}\mathrm{d}x.$

解 被积函数的分母分解成 $(x-3)(x-2)$ ，故可设

$$
\frac {x + 1}{x ^ {2} - 5 x + 6} = \frac {A}{x - 3} + \frac {B}{x - 2},
$$

其中 A, B 为待定系数. 上式两端去分母后, 得

$$
x + 1 = A (x - 2) + B (x - 3),
$$

即

$$
x + 1 = (A + B) x - 2 A - 3 B.
$$

比较上式两端同次幂的系数,即有

$$
\left\{ \begin{array}{l} A + B = 1, \\ 2 A + 3 B = - 1, \end{array} \right.
$$

从而解得 A=4, B=-3. 于是

$$
\int \frac {x + 1}{x ^ {2} - 5 x + 6} \mathrm{d} x = \int \left(\frac {4}{x - 3} - \frac {3}{x - 2}\right) \mathrm{d} x = 4 \ln | x - 3 | - 3 \ln | x - 2 | + C.
$$

例2 求 $\int \frac{x + 2}{(2x + 1)(x^2 + x + 1)}\mathrm{d}x.$

解 设 $\frac{x + 2}{(2x + 1)(x^2 + x + 1)} = \frac{A}{2x + 1} +\frac{Bx + D}{x^2 + x + 1}$ ，则

$$
x + 2 = A (x ^ {2} + x + 1) + (B x + D) (2 x + 1),
$$

即

$$
x + 2 = (A + 2 B) x ^ {2} + (A + B + 2 D) x + A + D,
$$

比较上式两端同次幂的系数,即有

$$
\left\{ \begin{array}{l} A + 2 B = 0, \\ A + B + 2 D = 1, \\ A + D = 2, \end{array} \right.
$$

从而解得 $\left\{\begin{aligned}A=2,\\ B=-1,\\ D=0.\end{aligned}\right.$ 于是

$$
\begin{array}{l} \int \frac {x + 2}{(2 x + 1) (x ^ {2} + x + 1)} \mathrm{d} x \\ = \int \left(\frac {2}{2 x + 1} - \frac {x}{x ^ {2} + x + 1}\right) \mathrm{d} x = \ln | 2 x + 1 | - \frac {1}{2} \int \frac {(2 x + 1) - 1}{x ^ {2} + x + 1} \mathrm{d} x \\ = \ln | 2 x + 1 | - \frac {1}{2} \int \frac {\mathrm{d} (x ^ {2} + x + 1)}{x ^ {2} + x + 1} + \frac {1}{2} \int \frac {\mathrm{d} x}{\left(x + \frac {1}{2}\right) ^ {2} + \frac {3}{4}} \\ = \ln | 2 x + 1 | - \frac {1}{2} \ln (x ^ {2} + x + 1) + \frac {1}{\sqrt {3}} \arctan \frac {2 x + 1}{\sqrt {3}} + C. \\ \end{array}
$$

例3 求 $\int \frac{x - 3}{(x - 1)(x^2 - 1)}\mathrm{d}x.$

解 被积函数分母的两个因式 $x - 1$ 与 $x^{2} - 1$ 有公因式, 故需再分解成 $(x - 1)^{2}(x + 1)$. 设

$$
\frac {x - 3}{(x - 1) ^ {2} (x + 1)} = \frac {A x + B}{(x - 1) ^ {2}} + \frac {D}{x + 1},
$$

则

$$
x - 3 = (A x + B) (x + 1) + D (x - 1) ^ {2},
$$

即

$$
x - 3 = (A + D) x ^ {2} + (A + B - 2 D) x + B + D,
$$

比较上式两端同次幂的系数,即有

$$
\left\{ \begin{array}{l} A + D = 0, \\ A + B - 2 D = 1, \\ B + D = - 3, \end{array} \right.
$$

从而解得 $\left\{\begin{aligned}A=1,\\ B=-2,\\ D=-1.\end{aligned}\right.$ 于是

$$
\begin{array}{l} \int \frac {x - 3}{(x - 1) (x ^ {2} - 1)} \mathrm{d} x \\ = \int \frac {x - 3}{(x - 1) ^ {2} (x + 1)} \mathrm{d} x = \int \left[ \frac {x - 2}{(x - 1) ^ {2}} - \frac {1}{x + 1} \right] \mathrm{d} x \\ = \int \frac {x - 1 - 1}{(x - 1) ^ {2}} \mathrm{d} x - \ln | x + 1 | \\ = \ln | x - 1 | + \frac {1}{x - 1} - \ln | x + 1 | + C. \\ \end{array}
$$

## 二、可化为有理函数的积分举例

例 4 求  $\int\frac{1+\sin x}{\sin x(1+\cos x)}dx.$

解 由三角函数公式知道, $\sin x$ 与 $\cos x$ 都可以用 $\tan\frac{x}{2}$ 的有理式表示,即

$$
\sin x = 2 \sin \frac {x}{2} \cos \frac {x}{2} = \frac {2 \tan \frac {x}{2}}{\sec^ {2} \frac {x}{2}} = \frac {2 \tan \frac {x}{2}}{1 + \tan^ {2} \frac {x}{2}},
$$

$$
\cos x = \cos^ {2} \frac {x}{2} - \sin^ {2} \frac {x}{2} = \frac {1 - \tan^ {2} \frac {x}{2}}{\sec^ {2} \frac {x}{2}} = \frac {1 - \tan^ {2} \frac {x}{2}}{1 + \tan^ {2} \frac {x}{2}}.
$$

如果作代换 $u = \tan \frac{x}{2} (-\pi < x < \pi)$ ①, 那么

$$
\sin x = \frac {2 u}{1 + u ^ {2}}, \quad \cos x = \frac {1 - u ^ {2}}{1 + u ^ {2}},
$$

而 $x = 2\arctan u$ ，从而

$$
\mathrm{d} x = \frac {2}{1 + u ^ {2}} \mathrm{d} u.
$$

于是

$$
\begin{array}{l} \int \frac {1 + \sin x}{\sin x (1 + \cos x)} \mathrm{d} x \\ = \int \frac {\left(1 + \frac {2 u}{1 + u ^ {2}}\right) \frac {2 \mathrm{d} u}{1 + u ^ {2}}}{\frac {2 u}{1 + u ^ {2}} \left(1 + \frac {1 - u ^ {2}}{1 + u ^ {2}}\right)} = \frac {1}{2} \int \left(u + 2 + \frac {1}{u}\right) \mathrm{d} u \\ = \frac {1}{2} \left(\frac {u ^ {2}}{2} + 2 u + \ln | u |\right) + C = \frac {1}{4} \tan^ {2} \frac {x}{2} + \tan \frac {x}{2} + \frac {1}{2} \ln \left| \tan \frac {x}{2} \right| + C. \\ \end{array}
$$

本例所用的变量代换  $u=\tan\frac{x}{2}$  对三角函数有理式的积分都可以应用.

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 当 $x \in ((2k - 1)\pi, (2k + 1)\pi), k \in \mathbb{Z}$ 时，作代换 $u = \tan \frac{x - 2k\pi}{2} = \tan \frac{x}{2}, x = 2k\pi + 2\arctan u$ ，以下所得结果相同.</span></small>

![](images/page_227_image_14.jpg)

释疑解难

4-4

例5 求 $\int \frac{\sqrt{x - 1}}{x}\mathrm{d}x.$

解 为了去掉根号, 可以设  $\sqrt{x-1}=u$ , 于是  $x=u^{2}+1$ , dx=2udu, 从而所求积分为

$$
\begin{array}{l} \int \frac {\sqrt {x - 1}}{x} \mathrm{d} x = \int \frac {u}{u ^ {2} + 1} \cdot 2 u \mathrm{d} u = 2 \int \frac {u ^ {2}}{u ^ {2} + 1} \mathrm{d} u \\ = 2 \int \left(1 - \frac {1}{1 + u ^ {2}}\right) \mathrm{d} u = 2 (u - \arctan u) + C \\ = 2 (\sqrt {x - 1} - \arctan \sqrt {x - 1}) + C. \\ \end{array}
$$

例6 求 $\int \frac{\mathrm{d}x}{1 + \sqrt[3]{x + 2}}.$

解 为了去掉根号, 可以设  $\sqrt[3]{x+2}=u$ . 于是  $x=u^{3}-2$ ,  $dx=3u^{2}du$ , 从而所求积分为

$$
\begin{array}{l} \int \frac {\mathrm{d} x}{1 + \sqrt [ 3 ]{x + 2}} = \int \frac {3 u ^ {2}}{1 + u} \mathrm{d} u \\ = 3 \int \left(u - 1 + \frac {1}{1 + u}\right) \mathrm{d} u = 3 \left(\frac {u ^ {2}}{2} - u + \ln | 1 + u |\right) + C \\ = \frac {3}{2} \sqrt [ 3 ]{(x + 2) ^ {2}} - 3 \sqrt [ 3 ]{x + 2} + 3 \ln | 1 + \sqrt [ 3 ]{x + 2} | + C. \\ \end{array}
$$

例7 求 $\int \frac{\mathrm{d}x}{(1 + \sqrt[3]{x})\sqrt{x}}.$

解 被积函数中出现了两个根式 $\sqrt{x}$ 及 $\sqrt[3]{x}$, 为了能同时消去这两个根式, 可令 $x = u^6$, 于是 $\mathrm{dx} = 6u^5\mathrm{du}$, 从而所求积分为

$$
\begin{array}{l} \int \frac {\mathrm{d} x}{(1 + \sqrt [ 3 ]{x}) \sqrt {x}} = \int \frac {6 u ^ {5}}{(1 + u ^ {2}) u ^ {3}} \mathrm{d} u = 6 \int \frac {u ^ {2}}{1 + u ^ {2}} \mathrm{d} u \\ = 6 \int \left(1 - \frac {1}{1 + u ^ {2}}\right) \mathrm{d} u = 6 (u - \arctan u) + C \\ = 6 \left(\sqrt [ 6 ]{x} - \arctan \sqrt [ 6 ]{x}\right) + C. \\ \end{array}
$$

例8 求 $\int \frac{1}{x}\sqrt{\frac{1 + x}{x}}\mathrm{d}x.$

解 为了去掉根号, 可以设  $\sqrt{\frac{1+x}{x}} = u$ , 于是  $\frac{1+x}{x} = u^{2}$ ,  $x = \frac{1}{u^{2}-1}$ ,  $dx = -\frac{2udu}{(u^{2}-1)^{2}}$ , 从而所求积分为

$$
\int \frac {1}{x} \sqrt {\frac {1 + x}{x}} \mathrm{d} x = \int (u ^ {2} - 1) u \cdot \frac {- 2 u}{(u ^ {2} - 1) ^ {2}} \mathrm{d} u = - 2 \int \frac {u ^ {2}}{u ^ {2} - 1} \mathrm{d} u
$$

$$
\begin{array}{l} = - 2 \int \left(1 + \frac {1}{u ^ {2} - 1}\right) \mathrm{d} u = - 2 u - \ln \left| \frac {u - 1}{u + 1} \right| + C \\ = - 2 u + 2 \ln (u + 1) - \ln | u ^ {2} - 1 | + C \\ = - 2 \sqrt {\frac {1 + x}{x}} + 2 \ln \left(\sqrt {\frac {1 + x}{x}} + 1\right) + \ln | x | + C. \\ \end{array}
$$

以上四个例子表明,如果被积函数中含有简单根式 $\sqrt[n]{ax+b}$ 或 $\sqrt[n]{\frac{ax+b}{cx+d}}$ ，可以令这个简单根式为u.由于这样的变换具有反函数,且反函数是u的有理函数,因此原积分即可化为有理函数的积分.

## 习题4- 4

求下列不定积分:

1.  $\int\frac{x^{3}}{x+3}dx.$

2. $\int \frac{2x + 3}{x^2 + 3x - 10}\mathrm{d}x.$

3. $\int \frac{x + 1}{x^2 - 2x + 5}\mathrm{d}x.$

4. $\int \frac{\mathrm{d}x}{x(x^2 + 1)}.$

5. $\int \frac{3}{x^3 + 1}\mathrm{d}x.$

6. $\int \frac{x^2 + 1}{(x + 1)^2(x - 1)}\mathrm{d}x.$

7. $\int \frac{x\mathrm{d}x}{(x + 1)(x + 2)(x + 3)}.$

8. $\int \frac{x^5 + x^4 - 8}{x^3 - x}\mathrm{d}x.$

9. $\int \frac{\mathrm{d}x}{(x^2 + 1)(x^2 + x)}.$

10. $\int \frac{1}{x^4 - 1}\mathrm{d}x.$

11. $\int \frac{\mathrm{d}x}{(x^2 + 1)(x^2 + x + 1)}.$

12. $\int \frac{(x + 1)^2}{(x^2 + 1)^2}\mathrm{d}x.$

13.  $\int\frac{-x^{2}-2}{(x^{2}+x+1)^{2}}dx.$

14.  $\int\frac{dx}{3+\sin^{2}x}.$

15. $\int \frac{\mathrm{d}x}{3 + \cos x}$.

16.  $\int\frac{dx}{2+\sin x}.$

17. $\int \frac{\mathrm{d}x}{1 + \sin x + \cos x}$.

18.  $\int\frac{dx}{2\sin x-\cos x+5}.$

19. $\int \frac{\mathrm{d}x}{1 + \sqrt[3]{x + 1}}.$

20. $\int \frac{(\sqrt{x})^3 - 1}{\sqrt{x} + 1}\mathrm{d}x.$

21. $\int \frac{\sqrt{x + 1} - 1}{\sqrt{x + 1} + 1}\mathrm{d}x.$

22. $\int \frac{\mathrm{d}x}{\sqrt{x} + \sqrt[4]{x}}.$

23. $\int \sqrt{\frac{1 - x}{1 + x}}\frac{\mathrm{d}x}{x}.$

24. $\int \frac{\mathrm{d}x}{\sqrt[3]{(x + 1)^2(x - 1)^4}}.$

## 第五节 积分表的使用

通过前面的讨论可以看出,积分的计算要比导数的计算来得灵活、复杂.为了实用的方便,往往把常用的积分公式汇集成表,这种表叫做积分表.积分表是按照被积函数的类型来排列的.求积分时,可根据被积函数的类型直接地或经过简单的变形后,在表

内查得所需的结果.

本书末附录Ⅳ有一个简单的积分表,以供查阅.

我们先举几个可以直接从积分表中查得结果的积分例子.

例1 求 $\int \frac{x}{(3x + 4)^2}\mathrm{d}x.$

解 被积函数含有 $ax + b$ ，在积分表(一)中查得公式7

$$
\int \frac {x}{(a x + b) ^ {2}} \mathrm{d} x = \frac {1}{a ^ {2}} \left(\ln | a x + b | + \frac {b}{a x + b}\right) + C.
$$

现在 $a = 3, b = 4$ ，于是

$$
\int \frac {x}{(3 x + 4) ^ {2}} \mathrm{d} x = \frac {1}{9} \left(\ln | 3 x + 4 | + \frac {4}{3 x + 4}\right) + C.
$$

例2 求 $\int \frac{\mathrm{d}x}{5 - 4\cos x}$.

解 被积函数含有三角函数, 在积分表(十一)中查得关于积分  $\int\frac{dx}{a+b\cos x}$  的公式, 但是公式有两个, 要看  $a^{2}>b^{2}$  或  $a^{2}<b^{2}$  而决定采用哪一个.

现在 $a = 5, b = -4, a^2 > b^2$，所以用公式105

$$
\int \frac {\mathrm{d} x}{a + b \cos x} = \frac {2}{a + b} \sqrt {\frac {a + b}{a - b}} \arctan \left(\sqrt {\frac {a - b}{a + b}} \tan \frac {x}{2}\right) + C \quad (a ^ {2} > b ^ {2}).
$$

于是

$$
\begin{array}{l} \int \frac {\mathrm{d} x}{5 - 4 \cos x} = \frac {2}{5 + (- 4)} \sqrt {\frac {5 + (- 4)}{5 - (- 4)}} \arctan \left(\sqrt {\frac {5 - (- 4)}{5 + (- 4)}} \tan \frac {x}{2}\right) + C \\ = \frac {2}{3} \arctan \left(3 \tan \frac {x}{2}\right) + C. \\ \end{array}
$$

下面再举一个需要先进行变量代换,然后再查表求积分的例子.

例3 求 $\int \frac{\mathrm{d}x}{x\sqrt{4x^2 + 9}}.$

解 这个积分不能在表中直接查到,需要先进行变量代换.

令 $2x = u$ ，那么 $\sqrt{4x^2 + 9} = \sqrt{u^2 + 3^2}, x = \frac{u}{2}, \mathrm{d}x = \frac{1}{2} \mathrm{d}u.$ 于是

$$
\int \frac {\mathrm{d} x}{x \sqrt {4 x ^ {2} + 9}} = \int \frac {\frac {1}{2} \mathrm{d} u}{\frac {u}{2} \sqrt {u ^ {2} + 3 ^ {2}}} = \int \frac {\mathrm{d} u}{u \sqrt {u ^ {2} + 3 ^ {2}}}.
$$

被积函数中含有 $\sqrt{u^2 + 3^2}$，在积分表（六）中查到公式37

$$
\int \frac {\mathrm{d} x}{x \sqrt {x ^ {2} + a ^ {2}}} = \frac {1}{a} \ln \frac {\sqrt {x ^ {2} + a ^ {2}} - a}{| x |} + C.
$$

现在 $a = 3, x$ 相当于 $u$, 于是

$$
\int \frac {\mathrm{d} u}{u \sqrt {u ^ {2} + 3 ^ {2}}} = \frac {1}{3} \ln \frac {\sqrt {u ^ {2} + 3 ^ {2}} - 3}{| u |} + C.
$$

再把 u=2x 代入, 最后得到

$$
\int \frac {\mathrm{d} x}{x \sqrt {4 x ^ {2} + 9}} = \int \frac {\mathrm{d} u}{u \sqrt {u ^ {2} + 3 ^ {2}}} = \frac {1}{3} \ln \frac {\sqrt {u ^ {2} + 3 ^ {2}} - 3}{| u |} + C = \frac {1}{3} \ln \frac {\sqrt {4 x ^ {2} + 9} - 3}{2 | x |} + C.
$$

最后,举一个用递推公式求积分的例子.

例 4 求  $\int \sin^{4}x dx$ .

解 在积分表(十一)中查到公式 95

$$
\int \sin^ {n} x \mathrm{d} x = - \frac {\sin^ {n - 1} x \cos x}{n} + \frac {n - 1}{n} \int \sin^ {n - 2} x \mathrm{d} x.
$$

利用这个公式可以使被积函数中正弦的幂次减少2次, 只要重复使用这个公式, 可以使正弦的幂次继续减少, 直到求出最后结果为止, 这种公式叫做递推公式.

现在 $n = 4$ ，于是

$$
\int \sin^ {4} x \mathrm{d} x = - \frac {\sin^ {3} x \cos x}{4} + \frac {3}{4} \int \sin^ {2} x \mathrm{d} x.
$$

对积分  $\int\sin^{2}x dx$  用公式 93

$$
\int \sin^ {2} x \mathrm{d} x = \frac {x}{2} - \frac {1}{4} \sin 2 x + C,
$$

从而所求积分为

$$
\int \sin^ {4} x \mathrm{d} x = - \frac {\sin^ {3} x \cos x}{4} + \frac {3}{4} \left(\frac {x}{2} - \frac {1}{4} \sin 2 x\right) + C.
$$

一般说来,查积分表可以节省计算积分的时间,但是,只有掌握了前面学过的基本积分方法才能灵活地使用积分表,而且对一些比较简单的积分,应用基本积分方法来计算比查表更快些,例如,对 $\int\sin^{2}x\cos^{3}xdx$ ,用代换u=sin x很快就可得到结果.所以,求积分时究竟是直接计算,还是查表,或是两者结合使用,应该作具体分析,不能一概而论.

在本章结束之前,我们还要指出:对初等函数来说,在其定义区间上,它的原函数一定存在,但原函数不一定都是初等函数,如

$$
\int \mathrm{e} ^ {- x ^ {2}} \mathrm{d} x, \quad \int \frac {\sin x}{x} \mathrm{d} x, \quad \int \frac {\mathrm{d} x}{\ln x}, \quad \int \frac {\mathrm{d} x}{\sqrt {1 + x ^ {4}}},
$$

等等,它们的原函数就都不是初等函数.

## 习题 4-5

利用积分表计算下列不定积分:

1. $\int \frac{\mathrm{d}x}{\sqrt{4x^2 - 9}}.$

2. $\int \frac{1}{x^2 + 2x + 5} \, \mathrm{d}x.$

3. $\int \frac{\mathrm{d}x}{\sqrt{5 - 4x + x^2}}.$

4. $\int \sqrt{2x^2 + 9}\mathrm{d}x.$

5. $\int \sqrt{3x^2 - 2}\mathrm{d}x.$

6. $\int \mathrm{e}^{2x}\cos x\mathrm{d}x.$

7. $\int x\arcsin \frac{x}{2}\mathrm{d}x.$

8. $\int \frac{\mathrm{d}x}{(x^2 + 9)^2}$.

9. $\int \frac{\mathrm{d}x}{\sin^3 x}$.

10. $\int \mathrm{e}^{-2x}\sin 3x\mathrm{d}x.$

11.  $\int \sin 3x \sin 5x dx.$

12. $\int \ln^3 x\mathrm{d}x$

13. $\int \frac{1}{x^2(1 - x)}\mathrm{d}x.$

14. $\int \frac{\sqrt{x - 1}}{x}\mathrm{d}x.$

15. $\int \frac{1}{(1 + x^2)^2}\mathrm{d}x.$

16. $\int \frac{1}{x\sqrt{x^2 - 1}}\mathrm{d}x.$

17. $\int \frac{x}{(2 + 3x)^2}\mathrm{d}x.$

18. $\int \cos^6 x\mathrm{d}x$

19. $\int x^{2}\sqrt{x^{2} - 2}\mathrm{d}x.$

20. $\int \frac{1}{2 + 5\cos x}\mathrm{d}x.$

21. $\int \frac{\mathrm{d}x}{x^2\sqrt{2x - 1}}.$

22. $\int \sqrt{\frac{1 - x}{1 + x}}\mathrm{d}x.$

23. $\int \frac{x + 5}{x^2 - 2x - 1}\mathrm{d}x.$

24. $\int \frac{x\mathrm{d}x}{\sqrt{1 + x - x^2}}.$

25. $\int \frac{x^4}{25 + 4x^2}\mathrm{d}x.$

## 总习题四

1. 填空:

(1) $\int x^{3}e^{x}dx =$ \_\_\_\_;
(2) $\int \frac{x + 5}{x^2 - 6x + 13} \, \mathrm{d}x =$ \_\_\_\_.

2. 以下两题中给出了四个结论,从中选出一个正确的结论:

(1) 已知  $f'(x)=\frac{1}{x(1+2\ln x)}$ ，且  $f(1)=1$ ，则  $f(x)$  等于（）；

(A) $\ln (1 + 2\ln x) + 1$

(B) $\frac{1}{2} \ln (1 + 2 \ln x) + 1$

(C) $\frac{1}{2} \ln (1 + 2 \ln x) + \frac{1}{2}$

(D) $2\ln (1 + 2\ln x) + 1$

(2) 在下列等式中, 正确的结果是().

(A) $\int f'(x)\mathrm{d}x = f(x)$

(B) $\int \mathrm{d}f(x) = f(x)$

(C) $\frac{\mathrm{d}}{\mathrm{d}x}\int f(x)\mathrm{d}x = f(x)$

(D) $\mathrm{d}\int f(x)\mathrm{d}x = f(x)$

3. 已知 $\frac{\sin x}{x}$ 是 $f(x)$ 的一个原函数, 求 $\int x^3 f'(x) \mathrm{d}x$.

4. 求下列不定积分(其中 a, b 为常数):

(1) $\int \frac{\mathrm{d}x}{\mathrm{e}^x - \mathrm{e}^{-x}};$

(2) $\int \frac{x}{(1 - x)^3} \, \mathrm{d}x$;

(3) $\int \frac{x^2}{a^6 - x^6} \, \mathrm{d}x (a > 0)$;

(4) $\int \frac{1 + \cos x}{x + \sin x} \, \mathrm{d}x$;

(5) $\int \frac{\ln\ln x}{x}\mathrm{d}x;$

(6) $\int \frac{\sin x\cos x}{1 + \sin^4x}\mathrm{d}x;$

(7) $\int \tan^4 x\mathrm{d}x;$

(8) $\int \sin x\sin 2x\sin 3xdx;$

(9) $\int \frac{\mathrm{d}x}{x(x^6 + 4)}$;

(10) $\int \sqrt{\frac{a + x}{a - x}}\mathrm{d}x (a > 0);$

(11) $\int \frac{\mathrm{d}x}{\sqrt{x(1 + x)}};$

(12) $\int x\cos^2 x\mathrm{d}x$;

(13) $\int \mathrm{e}^{ax}\cos bx\mathrm{d}x;$

(14) $\int \frac{\mathrm{d}x}{\sqrt{1 + \mathrm{e}^x}};$

(15) $\int \frac{\mathrm{d}x}{x^2\sqrt{x^2 - 1}};$

(16) $\int \frac{\mathrm{d}x}{\left(a^2 - x^2\right)^{5 / 2}};$

(17) $\int \frac{\mathrm{d}x}{x^4\sqrt{1 + x^2}};$

(18) $\int \sqrt{x} \sin \sqrt{x} \, \mathrm{d}x$;

(19) $\int \ln (1 + x^2)\mathrm{d}x;$

(20) $\int \frac{\sin^2 x}{\cos^3 x} \, \mathrm{d}x$;

(21) $\int \arctan \sqrt{x} \, \mathrm{d}x$;

(22) $\int \frac{\sqrt{1 + \cos x}}{\sin x} \, \mathrm{d}x$;

(23) $\int \frac{x^3}{(1 + x^8)^2}\mathrm{d}x;$

(24) $\int \frac{x^{11}}{x^8 + 3x^4 + 2}\mathrm{d}x;$

(25) $\int\frac{dx}{16-x^{4}};$

(26) $\int \frac{\sin x}{1 + \sin x} \, \mathrm{d}x$;

(27) $\int \frac{x + \sin x}{1 + \cos x} \, \mathrm{d}x$;

(28) $\int \mathrm{e}^{\sin x}\frac{x\cos^3x - \sin x}{\cos^2x}\mathrm{d}x;$

(29) $\int \frac{\sqrt[3]{x}}{x(\sqrt{x} + \sqrt[3]{x})}\mathrm{d}x;$

(30) $\int \frac{\mathrm{d}x}{\left(1 + \mathrm{e}^x\right)^2}$;

(31) $\int \frac{\mathrm{e}^{3x} + \mathrm{e}^x}{\mathrm{e}^{4x} - \mathrm{e}^{2x} + 1}\mathrm{d}x;$

(32) $\int \frac{x\mathrm{e}^x}{(\mathrm{e}^x + 1)^2}\mathrm{d}x;$

(33) $\int \ln^2 (x + \sqrt{1 + x^2})\mathrm{d}x;$

(34) $\int \frac{\ln x}{(1 + x^2)^{\frac{3}{2}}}\mathrm{d}x;$

(35) $\int \sqrt{1 - x^2}\arcsin x\mathrm{d}x;$

(36) $\int \frac{x^3\arccos x}{\sqrt{1 - x^2}}\mathrm{d}x;$

(37) $\int \frac{\cot x}{1 + \sin x} \, \mathrm{d}x$;

(38) $\int \frac{\mathrm{d}x}{\sin^3 x \cos x}$;

(39) $\int \frac{\mathrm{d}x}{(2 + \cos x)\sin x};$

(40) $\int \frac{\sin x\cos x}{\sin x + \cos x}\mathrm{d}x.$

![](images/page_234_image_1.jpg)

第四章释疑解难

# 第五章

# 定积分

本章讨论积分学的另一个基本问题——定积分问题.我们先从几何与力学问题出发引进定积分的定义,然后讨论它的性质与计算方法.关于定积分的应用,将在第六章讨论.

## 第一节 定积分的概念与性质

## 一、定积分问题举例

## 1. 曲边梯形的面积

设 $y = f(x)$ 在区间 $[a, b]$ 上非负、连续. 由直线 $x = a, x = b, y = 0$ 及曲线 $y = f(x)$ 所围成的图形（图 5-1）称为曲边梯形，其中曲线弧称为曲边.

我们知道,已知矩形的高和底,它的面积可按公式

$$
\text {矩形面积} = \text {高} \times \text {底}
$$

来定义和计算.而曲边梯形在底边上各点处的高 $f(x)$ 在区间 $[a,b]$ 上是变动的,故它的面积不能直接按上述公式来定义和计算.然而,由

![](images/page_235_chart_10.jpg)

<details>
<summary>bar</summary>

| Interval | Description |
| --- | --- |
| \(\xi_1\) | Leftmost interval (between x_0 and x_1) |
| \(\xi_2\) | Second interval (between x_1 and x_2) |
| \(\xi_i\) | Third interval (between x_{i-1} and x_i) |
| \(\xi_n\) | Fourth interval (between x_{n-1} and x_n = b) |
</details>

图5-1

于曲边梯形的高 $f(x)$ 在区间 $[a, b]$ 上是连续变化的，在很小一段区间上它的变化很小，近似于不变。因此，如果把区间 $[a, b]$ 划分为许多小区间，在每个小区间上用其中某一点处的高来近似代替同一个小区间上的窄曲边梯形的变高，那么，每个窄曲边梯形就可近似地看成这样得到的窄矩形。我们就以所有这些窄矩形面积之和作为曲边梯形面积的近似值,并把区间 $[a,b]$ 无限细分下去,即使每个小区间的长度都趋于零,这时所有窄矩形面积之和的极限就可定义为曲边梯形的面积.这个定义同时也给出了计算曲边梯形面积的方法,现详述于下:

在区间 $[a, b]$ 中任意插入 $n - 1$ 个分点

$$
a = x _ {0} <   x _ {1} <   x _ {2} <   \dots <   x _ {n - 1} <   x _ {n} = b,
$$

把 $[a,b]$ 分成 $n$ 个小区间

$$
\left[ x _ {0}, x _ {1} \right], \quad \left[ x _ {1}, x _ {2} \right], \quad \dots , \quad \left[ x _ {n - 1}, x _ {n} \right],
$$

它们的长度依次为

$$
\Delta x _ {1} = x _ {1} - x _ {0}, \quad \Delta x _ {2} = x _ {2} - x _ {1}, \quad \dots , \quad \Delta x _ {n} = x _ {n} - x _ {n - 1}.
$$

经过每一个分点作平行于 y 轴的直线段, 把曲边梯形分成 n 个窄曲边梯形. 在每个小区间  $\left[x_{i-1}, x_{i}\right]$  上任取一点  $\xi_{i}$ , 以  $\left[x_{i-1}, x_{i}\right]$  为底、 $f(\xi_{i})$  为高的窄矩形近似替代第 i 个窄曲边梯形 ( $i=1,2,\cdots,n$ ), 把这样得到的 n 个窄矩形面积之和作为所求曲边梯形面积 A 的近似值, 即

$$
A \approx f (\xi_ {1}) \Delta x _ {1} + f (\xi_ {2}) \Delta x _ {2} + \dots + f (\xi_ {n}) \Delta x _ {n} = \sum_ {i = 1} ^ {n} f (\xi_ {i}) \Delta x _ {i}.
$$

为了保证所有小区间的长度都无限缩小,我们要求小区间长度中的最大者趋于零,如记  $\lambda=\max\left\{\Delta x_{1},\Delta x_{2},\cdots,\Delta x_{n}\right\}$ , 则上述条件可表示为  $\lambda\to0$ . 当  $\lambda\to0$  时(这时分段数 n 无限增多, 即  $n\to\infty$ ), 取上述和式的极限, 便得曲边梯形的面积

$$
A = \lim _ {\lambda \to 0} \sum_ {i = 1} ^ {n} f (\xi_ {i}) \Delta x _ {i}.
$$

## 2. 变速直线运动的路程

设某物体做直线运动,已知速度  $v=v(t)$  是时间间隔  $[T_{1}, T_{2}]$  上 t 的连续函数,且  $v(t) \geqslant 0$ , 计算在这段时间内物体所经过的路程 s.

我们知道,对于等速直线运动,有公式

路程 $=$ 速度 $\times$ 时间.

但是,在现在讨论的问题中,速度不是常量而是随时间变化的变量,因此,所求路程s不能直接按等速直线运动的路程公式来计算.然而,物体运动的速度函数 $v=v(t)$ 是连续变化的,在很短一段时间内,速度的变化很小,近似于等速.因此,如果把时间间隔分小,在小段时间内,以等速运动代替变速运动,那么,就可算出部分路程的近似值;再求和,得到整个路程的近似值;最后,通过对时间间隔无限细分的极限过程,这时所有部分路程的近似值之和的极限,就是所求变速直线运动的路程的精确值.

具体计算步骤如下:

在时间间隔 $\left[T_{1},T_{2}\right]$ 内任意插入若干个分点

$$
T _ {1} = t _ {0} <   t _ {1} <   t _ {2} <   \dots <   t _ {n - 1} <   t _ {n} = T _ {2},
$$

把 $\left[T_{1},T_{2}\right]$ 分成n个小时段

$$
\left[ t _ {0}, t _ {1} \right], \quad \left[ t _ {1}, t _ {2} \right], \quad \dots , \quad \left[ t _ {n - 1}, t _ {n} \right],
$$

各小时段时间的长依次为

$$
\Delta t _ {1} = t _ {1} - t _ {0}, \quad \Delta t _ {2} = t _ {2} - t _ {1}, \quad \dots , \quad \Delta t _ {n} = t _ {n} - t _ {n - 1}.
$$

相应地,在各段时间内物体经过的路程依次为

$$
\Delta s _ {1}, \quad \Delta s _ {2}, \quad \dots , \quad \Delta s _ {n}.
$$

在时间间隔 $\left[t_{i-1},t_{i}\right]$ 上任取一个时刻 $\tau_{i}\left(t_{i-1}\leqslant\tau_{i}\leqslant t_{i}\right)$ ，以 $\tau_{i}$ 时的速度 $v(\tau_{i})$ 来代替 $\left[t_{i-1},t_{i}\right]$ 上各个时刻的速度，得到部分路程 $\Delta s_{i}$ 的近似值，即

$$
\Delta s _ {i} \approx v (\tau_ {i}) \Delta t _ {i} (i = 1, 2, \dots , n).
$$

于是这 n 段部分路程的近似值之和就是所求变速直线运动路程 s 的近似值, 即

$$
s \approx v (\tau_ {1}) \Delta t _ {1} + v (\tau_ {2}) \Delta t _ {2} + \dots + v (\tau_ {n}) \Delta t _ {n} = \sum_ {i = 1} ^ {n} v (\tau_ {i}) \Delta t _ {i}.
$$

记  $\lambda=\max\left\{\Delta t_{1},\Delta t_{2},\cdots,\Delta t_{n}\right\}$ ，当  $\lambda\to0$  时，取上述和式的极限，即得变速直线运动的路程

$$
s = \lim _ {\lambda \to 0} \sum_ {i = 1} ^ {n} v (\tau_ {i}) \Delta t _ {i}.
$$

## 二、定积分的定义

从上面两个例子可以看到:所要计算的量,即曲边梯形的面积 A 及变速直线运动的路程 s 的实际意义虽然不同,前者是几何量,后者是物理量,但是它们都由一个函数及其自变量的变化区间所决定,如:

曲边梯形的高度  $y=f(x)$  及其底边上的点 x 的变化区间  $[a,b]$ ,

直线运动的速度  $v=v(t)$  及时间 t 的变化区间  $[T_{1}, T_{2}]$ .

其次,计算这些量的方法与步骤都是相同的,并且它们都归结为具有相同结构的一种特定和的极限,如

面积 $A = \lim_{\lambda \to 0}\sum_{i = 1}^{n}f(\xi_i)\Delta x_i,$

路程  $s=\lim_{\lambda\to0}\sum_{i=1}^{n}v(\tau_{i})\Delta t_{i}.$

抛开这些问题的具体意义,抓住它们在数量关系上共同的本质与特性加以概括,我们就可以抽象出下述定积分的定义:

定义 设函数 $f(x)$ 在 $[a, b]$ 上有界，在 $[a, b]$ 中任意插入若干个分点

$$
a = x _ {0} <   x _ {1} <   x _ {2} <   \dots <   x _ {n - 1} <   x _ {n} = b,
$$

把区间 $[a, b]$ 分成 $n$ 个小区间

$$
\left[ x _ {0}, x _ {1} \right], \quad \left[ x _ {1}, x _ {2} \right], \quad \dots , \quad \left[ x _ {n - 1}, x _ {n} \right],
$$

各个小区间的长度依次为

$$
\Delta x _ {1} = x _ {1} - x _ {0}, \quad \Delta x _ {2} = x _ {2} - x _ {1}, \quad \dots , \quad \Delta x _ {n} = x _ {n} - x _ {n - 1}.
$$

在每个小区间 $\left[x_{i-1},x_{i}\right]$ 上任取一点 $\xi_{i}\left(x_{i-1}\leqslant\xi_{i}\leqslant x_{i}\right)$ ，作函数值 $f(\xi_{i})$ 与小区间长度 $\Delta x_{i}$ 的乘积 $f(\xi_{i})\Delta x_{i}(i=1,2,\cdots,n)$ ，并作出和

$$
S = \sum_ {i = 1} ^ {n} f (\xi_ {i}) \Delta x _ {i}. \tag {1-1}
$$

记  $\lambda=\max\left\{\Delta x_{1},\Delta x_{2},\cdots,\Delta x_{n}\right\}$ ，如果当  $\lambda\to0$  时，这和的极限总存在，且与闭区间  $[a,b]$  的分法及点  $\xi_{i}$  的取法无关，那么称这个极限 I 为函数  $f(x)$  在区间  $[a,b]$  上的定积分（简称积分），记作  $\int_{a}^{b}f(x)\mathrm{d}x$ ，即

$$
\int_ {a} ^ {b} f (x) \mathrm{d} x = I = \lim _ {\lambda \rightarrow 0} \sum_ {i = 1} ^ {n} f (\xi_ {i}) \Delta x _ {i}, \tag {1-2}
$$

其中 $f(x)$ 叫做被积函数, $f(x)\mathrm{d}x$ 叫做被积表达式, $x$ 叫做积分变量, $a$ 叫做积分下限, $b$ 叫做积分上限, $[a,b]$ 叫做积分区间.

利用“$\varepsilon - \delta$”的说法，上述定积分的定义可以表述如下:

设有常数 I, 如果对于任意给定的正数  $\varepsilon$ , 总存在一个正数  $\delta$ , 使得对于区间  $[a, b]$  的任何分法, 不论  $\xi_{i}$  在  $[x_{i-1}, x_{i}]$  中怎样选取, 只要  $\lambda = \max\{\Delta x_{1}, \Delta x_{2}, \cdots, \Delta x_{n}\} < \delta$ , 总有

$$
\left| \sum_ {i = 1} ^ {n} f (\xi_ {i}) \Delta x _ {i} - I \right| <   \varepsilon
$$

成立,那么称 I 是  $f(x)$  在区间  $[a,b]$  上的定积分,记作  $\int_{a}^{b}f(x)\mathrm{d}x$ .

注意 当和式 $\sum_{i=1}^{n} f(\xi_i) \Delta x_i$ 的极限存在时, 其极限 $I$ 仅与被积函数 $f(x)$ 及积分区间 $[a, b]$ 有关. 如果既不改变被积函数 $f$, 也不改变积分区间 $[a, b]$, 而只把积分变量 $x$ 改写成其他字母, 例如 $t$ 或 $u$, 那么, 这时和的极限 $I$ 不变, 也就是定积分的值不变, 即

$$
\int_ {a} ^ {b} f (x) \mathrm{d} x = \int_ {a} ^ {b} f (t) \mathrm{d} t = \int_ {a} ^ {b} f (u) \mathrm{d} u.
$$

这就是说,定积分的值只与被积函数及积分区间有关,而与积分变量的记法无关.

和式 $\sum_{i=1}^{n} f(\xi_i) \Delta x_i$ 通常称为 $f(x)$ 的积分和. 如果 $f(x)$ 在 $[a, b]$ 上的定积分存在, 那么就说 $f(x)$ 在 $[a, b]$ 上可积.

对于定积分,有这样一个重要问题:函数 $f(x)$ 在 $[a,b]$ 上满足怎样的条件, $f(x)$ 在 $[a,b]$ 上一定可积?这个问题我们不作深入讨论,而只给出以下两个充分条件:

定理1 设 $f(x)$ 在区间 $[a, b]$ 上连续，则 $f(x)$ 在 $[a, b]$ 上可积.

定理2 设 $f(x)$ 在区间 $[a, b]$ 上有界，且只有有限个间断点，则 $f(x)$ 在 $[a, b]$ 上可积.

利用定积分的定义,前面所讨论的两个实际问题可以分别表述如下:

曲线 $y = f(x)(f(x)\geqslant 0),x$ 轴及两条直线 $x = a,x = b$ 所围成的曲边梯形的面积 $A$ 等于函数 $f(x)$ 在区间 $[a,b]$ 上的定积分，即

$$
A = \int_ {a} ^ {b} f (x)   \mathrm{d} x.
$$

物体以变速 $v = v(t)(v(t)\geqslant 0)$ 做直线运动，从时刻 $t = T_{1}$ 到时刻 $t = T_{2}$，这物体经过的路程 $s$ 等于函数 $v(t)$ 在区间 $[T_1,T_2]$ 上的定积分，即

$$
s = \int_ {T _ {1}} ^ {T _ {2}} v (t) \mathrm{d} t.
$$

下面讨论定积分的几何意义. 在 $[a, b]$ 上 $f(x) \geqslant 0$ 时, 我们已经知道, 定积分 $\int_{a}^{b} f(x) \mathrm{d}x$ 表示由曲线 $y = f(x)$, 两条直线 $x = a, x = b$ 与 $x$ 轴所围成的曲边梯形的面积; 在 $[a, b]$ 上 $f(x) \leqslant 0$ 时, 由曲线 $y = f(x)$, 两条直线 $x = a, x = b$ 与 $x$ 轴所围成的曲边梯形位于 $x$ 轴的下方, 定积分

$$
\int_ {a} ^ {b} f (x) \mathrm{d} x
$$

表示上述曲边梯形面积的负值；在 $[a, b]$ 上 $f(x)$ 既取得正值又取得负值时，函数 $f(x)$ 的图形某些部分在 $x$ 轴的上方，而其他部分在 $x$ 轴下方（图5-2），此时定积分 $\int_{a}^{b} f(x) \mathrm{d}x$ 表示 $x$ 轴上方图形面积减去 $x$ 轴下方图形面积所得之差.

![](images/page_239_image_10.jpg)

<details>
<summary>text_image</summary>

y
y=f(x)
a O b x
</details>

图5-2

最后,举一个按定义计算定积分的例子.

例1 利用定义计算定积分 $\int_0^1 x^2\mathrm{d}x.$

解 因为被积函数 $f(x) = x^2$ 在积分区间[0,1]上连续，而连续函数是可积的，所以积分与区间[0,1]的分法及点 $\xi_i$ 的取法无关。因此，为了便于计算，不妨把区间[0,1]分成 $n$ 等份，分点为 $x_i = \frac{i}{n}, i = 1, 2, \dots, n-1$。这样，每个小区间 $[x_{i-1}, x_i]$ 的长度 $\Delta x_i = \frac{1}{n}, i = 1, 2, \dots, n$。取 $\xi_i = x_i, i = 1, 2, \dots, n$。于是，得和式

$$
\sum_ {i = 1} ^ {n} f (\xi_ {i}) \Delta x _ {i} = \sum_ {i = 1} ^ {n} \xi_ {i} ^ {2} \Delta x _ {i} = \sum_ {i = 1} ^ {n} x _ {i} ^ {2} \Delta x _ {i} = \sum_ {i = 1} ^ {n} \left(\frac {i}{n}\right) ^ {2} \cdot \frac {1}{n} = \frac {1}{n ^ {3}} \sum_ {i = 1} ^ {n} i ^ {2}
$$

$$
= \frac {1}{n ^ {3}} \cdot \frac {1}{6} n (n + 1) (2 n + 1) ① = \frac {1}{6} \left(1 + \frac {1}{n}\right) \left(2 + \frac {1}{n}\right).
$$

当 $\lambda \to 0$ 即 $n\to \infty$ 时，取上式右端的极限.由定积分的定义，即得所要计算的积分为

$$
\int_ {0} ^ {1} x ^ {2} \mathrm{d} x = \lim _ {\lambda \rightarrow 0} \sum_ {i = 1} ^ {n} \xi_ {i} ^ {2} \Delta x _ {i} = \lim _ {n \rightarrow \infty} \frac {1}{6} \left(1 + \frac {1}{n}\right)\left(2 + \frac {1}{n}\right) = \frac {1}{3}.
$$

## 三、定积分的近似计算

从例 1 的计算过程中可以看到, 对于任一确定的正整数 n, 积分和

$$
\sum_ {i = 1} ^ {n} f (\xi_ {i}) \Delta x _ {i} = \frac {1}{6} \left(1 + \frac {1}{n}\right) \left(2 + \frac {1}{n}\right)
$$

都是定积分 $\int_0^1 x^2\mathrm{d}x$ 的近似值.当 $n$ 取不同值时，可得到定积分 $\int_0^1 x^2\mathrm{d}x$ 精度不同的近似值.一般说来， $n$ 取得越大，近似程度越好.

下面就一般情形,讨论定积分的近似计算问题.设 $f(x)$ 在 $[a,b]$ 上连续,这时定积分 $\int_{a}^{b}f(x)\mathrm{d}x$ 存在.如同例1,采取把区间 $[a,b]$ 等分的分法,即用分点 $a=x_{0},x_{1},x_{2},\cdots,x_{n}=b$ 将 $[a,b]$ 分成n个长度相等的小区间,每个小区间的长为

$$
\Delta x = \frac {b - a}{n},
$$

在小区间 $[x_{i - 1},x_i]$ 上，取 $\xi_{i} = x_{i - 1}$ ，应有

① 利用恒等式 $(n+1)^{3}=n^{3}+3n^{2}+3n+1$ ，得

$$
\left\{ \begin{array}{l} (n + 1) ^ {3} - n ^ {3} = 3 n ^ {2} + 3 n + 1, \\ n ^ {3} - (n - 1) ^ {3} = 3 (n - 1) ^ {2} + 3 (n - 1) + 1, \\ \dots \dots \\ 3 ^ {3} - 2 ^ {3} = 3 \times 2 ^ {2} + 3 \times 2 + 1, \\ 2 ^ {3} - 1 ^ {3} = 3 \times 1 ^ {2} + 3 \times 1 + 1. \end{array} \right.
$$

把这 $n$ 个等式两端分别相加，得

$$
(n + 1) ^ {3} - 1 = 3 (1 ^ {2} + 2 ^ {2} + \dots + n ^ {2}) + 3 (1 + 2 + \dots + n) + n.
$$

由于  $1+2+\cdots+n=\frac{1}{2}n(n+1)$ ，代入上式，得

$$
n ^ {3} + 3 n ^ {2} + 3 n = 3 (1 ^ {2} + 2 ^ {2} + \dots + n ^ {2}) + \frac {3}{2} n (n + 1) + n.
$$

整理后,得

$$
1 ^ {2} + 2 ^ {2} + \dots + n ^ {2} = \frac {1}{6} n (n + 1) (2 n + 1).
$$

$$
\int_ {a} ^ {b} f (x) \mathrm{d} x = \lim _ {n \to \infty} \frac {b - a}{n} \sum_ {i = 1} ^ {n} f (x _ {i - 1}),
$$

从而对于任一确定的正整数 $n$ ，有

$$
\int_ {a} ^ {b} f (x) \mathrm{d} x \approx \frac {b - a}{n} \sum_ {i = 1} ^ {n} f (x _ {i - 1}).
$$

记 $f(x_{i})=y_{i}\quad(i=0,1,2,\cdots,n)$ ，上式可记作

$$
\int_ {a} ^ {b} f (x) \mathrm{d} x \approx \frac {b - a}{n} (y _ {0} + y _ {1} + \dots + y _ {n - 1}). \tag {1-3}
$$

如果取  $\xi_{i}=x_{i}$ ，则可得近似公式

$$
\int_ {a} ^ {b} f (x) \mathrm{d} x \approx \frac {b - a}{n} (y _ {1} + y _ {2} + \dots + y _ {n}). \tag {1-4}
$$

以上求定积分近似值的方法称为矩形法, 公式(1-3)、(1-4)称为矩形法公式.

矩形法的几何意义是:用窄条矩形的面积作为窄条曲边梯形面积的近似值.整体上用台阶形的面积作为曲边梯形面积的近似值.如图5-3所示.

求定积分近似值的方法,常用的还有梯形法和抛物线法(又称辛普森(Simpson)法),简单介绍一下:

![](images/page_241_chart_11.jpg)

<details>
<summary>bar</summary>

| Interval | Value |
| --- | --- |
| 1 | ~0.5 |
| 2 | ~0.6 |
| 3 | ~0.7 |
| 4 | ~0.8 |
| 5 | ~0.9 |
| 6 | ~1.0 |
| 7 | ~1.1 |
| 8 | ~1.2 |
| 9 | ~1.3 |
| 10 | ~1.4 |
| 11 | ~1.5 |
| 12 | ~1.6 |
| 13 | ~1.7 |
| 14 | ~1.8 |
| 15 | ~1.9 |
| 16 | ~2.0 |
| 17 | ~2.1 |
| 18 | ~2.2 |
| 19 | ~2.3 |
| 20 | ~2.4 |
</details>

图5-3

和矩形法一样, 将区间  $[a, b]n$  等分. 设  $f(x_{i}) = y_{i}$ , 曲线  $y = f(x)$  上的点  $(x_{i}, y_{i})$  记作  $M_{i}$   $(i = 0, 1, 2, \cdots, n)$ .

梯形法的原理是: 将曲线  $y = f(x)$  上的小弧段  $\widehat{M_{i-1}M_i}$  用直线段  $\overline{M_{i-1}M_i}$  代替, 也就是把窄条曲边梯形用窄条梯形代替(图 5-4(a)), 由此得到定积分的近似值为

$$
\begin{array}{l} \int_ {a} ^ {b} f (x) \mathrm{d} x \approx \frac {b - a}{n} \left(\frac {y _ {0} + y _ {1}}{2} + \frac {y _ {1} + y _ {2}}{2} + \dots + \frac {y _ {n - 1} + y _ {n}}{2}\right) \\ = \frac {b - a}{n} \left(\frac {y _ {0} + y _ {n}}{2} + y _ {1} + y _ {2} + \dots + y _ {n - 1}\right). \tag {1-5} \\ \end{array}
$$

显然,梯形法公式(1-5)所得近似值就是矩形法公式(1-3)和(1-4)所得两个近似值的平均值.

抛物线法的原理是: 将曲线  $y = f(x)$  上的两个小弧段  $\widehat{M_{i-1}M_i}$  和  $\widehat{M_iM_{i+1}}$  合起来, 用过  $M_{i-1}, M_i, M_{i+1}$  三点的抛物线  $y = px^2 + qx + r (p \neq 0)$  代替 (图 5-4(b)). 经推导可得, 以此抛物线弧段为曲边、以  $[x_{i-1}, x_{i+1}]$  为底的曲边梯形面积为

$$
\frac {1}{6} (y _ {i - 1} + 4 y _ {i} + y _ {i + 1}) \cdot 2 \Delta x = \frac {b - a}{3 n} (y _ {i - 1} + 4 y _ {i} + y _ {i + 1}).
$$

![](images/page_242_image_1.jpg)

图5-4

取 n 为偶数, 得到定积分的近似值为

$$
\begin{array}{l} \int_ {a} ^ {b} f (x) \mathrm{d} x \approx \frac {b - a}{3 n} \left[ \left(y _ {0} + 4 y _ {1} + y _ {2}\right) + \left(y _ {2} + 4 y _ {3} + y _ {4}\right) + \dots + \left(y _ {n - 2} + 4 y _ {n - 1} + y _ {n}\right) \right] \\ = \frac {b - a}{3 n} [ y _ {0} + y _ {n} + 4 (y _ {1} + y _ {3} + \dots + y _ {n - 1}) + 2 (y _ {2} + y _ {4} + \dots + y _ {n - 2}) ]. \tag {1-6} \\ \end{array}
$$

例 2 按梯形法公式(1-5)和抛物线法公式(1-6)计算定积分  $\int_{0}^{1}\frac{4}{1+x^{2}}dx$  的近似值(取 n=10, 计算时取 5 位小数).

解 计算  $y_{i}$  并列表:

| i | $x_i$ | $y_i$ |
| --- | --- | --- |
| 0 | 0.0 | 4.000 00 |
| 1 | 0.1 | 3.960 40 |
| 2 | 0.2 | 3.846 15 |
| 3 | 0.3 | 3.669 72 |
| 4 | 0.4 | 3.448 28 |
| 5 | 0.5 | 3.200 00 |
| 6 | 0.6 | 2.941 18 |
| 7 | 0.7 | 2.684 56 |
| 8 | 0.8 | 2.439 02 |
| 9 | 0.9 | 2.209 94 |
| 10 | 1.0 | 2.000 00 |

按梯形法公式(1-5)求得近似值为

$$
S _ {1} = 3. 1 3 9 9 3,
$$

按抛物线法公式(1-6)求得近似值为

$$
S _ {2} = 3. 1 4 1 5 9.
$$

本例所给积分的精确值为

$$
\int_ {0} ^ {1} \frac {4}{1 + x ^ {2}} \mathrm{d} x = \pi = 3. 1 4 1 5 9 2 6 \dots ,
$$

用 $S_{2}$ 作为所给积分的近似值，误差小于 $10^{-5}$.

计算定积分的近似值的方法很多,这里不再作介绍.随着计算机应用的普及,定积分的近似计算已变得更为方便,现在已有很多现成的数学软件可用于定积分的近似计算.

## 四、定积分的性质

为了以后计算及应用方便起见,对定积分作以下两点补充规定:

(1) 当 b=a 时， $\int_{a}^{a}f(x)\mathrm{d}x=0;$

(2) 当 a > b 时， $\int_{a}^{b} f(x) \, dx = -\int_{b}^{a} f(x) \, dx,$

由上式可知,交换定积分的上、下限时,定积分的绝对值不变而符号相反.

下面讨论定积分的性质.下列各性质中积分上、下限的大小,如不特别指明,均不加限制,并假定各性质中所出现的被积函数在积分区间上都是可积的.

性质1 设 $\alpha$ 与 $\beta$ 均为常数, 则

$$
\int_ {a} ^ {b} [ \alpha f (x) + \beta g (x) ] \mathrm{d} x = \alpha \int_ {a} ^ {b} f (x) \mathrm{d} x + \beta \int_ {a} ^ {b} g (x) \mathrm{d} x.
$$

证 $\int_{a}^{b}\left[\alpha f(x) + \beta g(x)\right]\mathrm{d}x = \lim_{\lambda \to 0}\sum_{i = 1}^{n}\left[\alpha f(\xi_i) + \beta g(\xi_i)\right]\Delta x_i$

$$
= \lim _ {\lambda \rightarrow 0} \alpha \sum_ {i = 1} ^ {n} f (\xi_ {i}) \Delta x _ {i} + \lim _ {\lambda \rightarrow 0} \beta \sum_ {i = 1} ^ {n} g (\xi_ {i}) \Delta x _ {i}
$$

$$
= \alpha \int_ {a} ^ {b} f (x) \mathrm{d} x + \beta \int_ {a} ^ {b} g (x) \mathrm{d} x.
$$

性质 1 对于任意有限个函数的线性组合也是成立的.

性质 2 设 a<c<b, 则

$$
\int_ {a} ^ {b} f (x) \mathrm{d} x = \int_ {a} ^ {c} f (x) \mathrm{d} x + \int_ {c} ^ {b} f (x) \mathrm{d} x.
$$

证 因为函数 $f(x)$ 在区间 $[a, b]$ 上可积，所以不论把 $[a, b]$ 怎样分，积分和的极限总是不变的。因此，在分区间时，可以使 $c$ 永远是个分点。那么，$[a, b]$ 上的积分和等于 $[a, c]$ 上的积分和加 $[c, b]$ 上的积分和，记为

$$
\sum_ {[ a, b ]} f (\xi_ {i}) \Delta x _ {i} = \sum_ {[ a, c ]} f (\xi_ {i}) \Delta x _ {i} + \sum_ {[ c, b ]} f (\xi_ {i}) \Delta x _ {i}.
$$

令  $\lambda \rightarrow 0$ ，上式两端同时取极限，即得

$$
\int_ {a} ^ {b} f (x) \mathrm{d} x = \int_ {a} ^ {c} f (x) \mathrm{d} x + \int_ {c} ^ {b} f (x) \mathrm{d} x.
$$

这个性质表明定积分对于积分区间具有可加性.

按定积分的补充规定,我们有:不论a,b,c的相对位置如何,总有等式

$$
\int_ {a} ^ {b} f (x) \mathrm{d} x = \int_ {a} ^ {c} f (x) \mathrm{d} x + \int_ {c} ^ {b} f (x) \mathrm{d} x
$$

成立.例如,当a<b<c时,由于

$$
\int_ {a} ^ {c} f (x) \mathrm{d} x = \int_ {a} ^ {b} f (x) \mathrm{d} x + \int_ {b} ^ {c} f (x) \mathrm{d} x,
$$

于是得

$$
\int_ {a} ^ {b} f (x) \mathrm{d} x = \int_ {a} ^ {c} f (x) \mathrm{d} x - \int_ {b} ^ {c} f (x) \mathrm{d} x = \int_ {a} ^ {c} f (x) \mathrm{d} x + \int_ {c} ^ {b} f (x) \mathrm{d} x.
$$

性质3 如果在区间 $[a, b]$ 上 $f(x) \equiv 1$，那么

$$
\int_ {a} ^ {b} 1 \mathrm{d} x = \int_ {a} ^ {b} \mathrm{d} x = b - a.
$$

这个性质的证明请读者自己完成.

性质 4 如果在区间  $[a, b]$  上  $f(x) \geqslant 0$ ，那么

$$
\int_ {a} ^ {b} f (x) \mathrm{d} x \geqslant 0 \quad (a <   b).
$$

证 因为 $f(x) \geqslant 0$ ，所以

$$
f (\xi_ {i}) \geqslant 0 \quad (i = 1, 2, \dots , n).
$$

又由于  $\Delta x_{i} \geqslant 0 (i = 1, 2, \cdots, n)$ ，因此

$$
\sum_ {i = 1} ^ {n} f (\xi_ {i}) \Delta x _ {i} \geqslant 0,
$$

令  $\lambda=\max\left\{\Delta x_{1},\Delta x_{2},\cdots,\Delta x_{n}\right\}\rightarrow0$  ,便得要证的不等式.

推论1 如果在区间 $[a, b]$ 上 $f(x) \leqslant g(x)$, 那么.

$$
\int_ {a} ^ {b} f (x) \mathrm{d} x \leqslant \int_ {a} ^ {b} g (x) \mathrm{d} x \quad (a <   b).
$$

证 因为 $g(x) - f(x) \geqslant 0$ ，由性质4得

$$
\int_ {a} ^ {b} \left[ g (x) - f (x) \right] \mathrm{d} x \geqslant 0.
$$

再利用性质1,便得要证的不等式.

推论2 $\left|\int_{a}^{b}f(x)\mathrm{d}x\right| \leqslant \int_{a}^{b}|f(x)|\mathrm{d}x \quad (a < b).$

证 因为

$$
- \left| f (x) \right| \leqslant f (x) \leqslant \left| f (x) \right|,
$$

所以由推论1及性质1可得

$$
- \int_ {a} ^ {b} | f (x) | \mathrm{d} x \leqslant \int_ {a} ^ {b} f (x) \mathrm{d} x \leqslant \int_ {a} ^ {b} | f (x) | \mathrm{d} x,
$$

即

$$
\left| \int_ {a} ^ {b} f (x)   \mathrm{d} x \right| \leqslant \int_ {a} ^ {b} | f (x) |   \mathrm{d} x.
$$

性质5 设 $M$ 及 $m$ 分别是函数 $f(x)$ 在区间 $[a, b]$ 上的最大值及最小值，则

$$
m (b - a) \leqslant \int_ {a} ^ {b} f (x)   \mathrm{d} x \leqslant M (b - a) \quad (a <   b).
$$

证 因为 $m \leqslant f(x) \leqslant M$，所以由性质4的推论1，得

$$
\int_ {a} ^ {b} m \mathrm{d} x \leqslant \int_ {a} ^ {b} f (x) \mathrm{d} x \leqslant \int_ {a} ^ {b} M \mathrm{d} x.
$$

再由性质 1 及性质 3, 即得所要证的不等式.

这个性质说明,由被积函数在积分区间上的最大值及最小值,可以估计积分值的大致范围.例如,定积分 $\int_{\frac{1}{2}}^{1}x^{4}dx$ ,它的被积函数 $f(x)=x^{4}$ 在积分区间 $\left[\frac{1}{2},1\right]$ 上是单调增加的,于是有最小值 $m=\left(\frac{1}{2}\right)^{4}=\frac{1}{16}$ 、最大值 $M=(1)^{4}=1$ .由性质5,得

$$
\frac {1}{1 6} \times \left(1 - \frac {1}{2}\right) \leqslant \int_ {\frac {1}{2}} ^ {1} x ^ {4} \mathrm{d} x \leqslant 1 \times \left(1 - \frac {1}{2}\right),
$$

即

$$
\frac {1}{3 2} \leqslant \int_ {\frac {1}{2}} ^ {1} x ^ {4} \mathrm{d} x \leqslant \frac {1}{2}.
$$

性质6(定积分中值定理) 如果函数 $f(x)$ 在积分区间 $[a, b]$ 上连续, 那么在 $[a, b]$ 上至少存在一个点 $\xi$, 使下式成立:

$$
\int_ {a} ^ {b} f (x) \mathrm{d} x = f (\xi) (b - a) \quad (a \leqslant \xi \leqslant b).
$$

这个公式叫做积分中值公式①.

证 把性质 5 中的不等式各边除以 b-a, 得

$$
m \leqslant \frac {1}{b - a} \int_ {a} ^ {b} f (x)   \mathrm{d} x \leqslant M.
$$

这表明,确定的数值 $\frac{1}{b-a}\int_{a}^{b}f(x)\mathrm{d}x\in[m,M]$ .根据闭区间上连续函数的介值定理(第一章第十节定理3)的推论,在 $[a,b]$ 上至少存在一点 $\xi$ ,使得函数 $f(x)$ 在点 $\xi$ 处的值与这个确定的数值相等,即应有

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 可以证明  $\xi \in (a, b)$ ，参阅本章第二节例 6.</span></small>

$$
\frac {1}{b - a} \int_ {a} ^ {b} f (x)   \mathrm{d} x = f (\xi) \quad (a \leqslant \xi \leqslant b).
$$

两端各乘 b-a，即得所要证的等式.

显然,积分中值公式

$\int_{a}^{b}f(x)\mathrm{d}x = f(\xi)(b - a)$ （ $\xi$ 在 $a$ 与 $b$ 之间）

不论 $a < b$ 或 $a > b$ 都是成立的.

积分中值公式有如下的几何解释: 在区间  $[a, b]$  上至少存在一点  $\xi$ ，使得以区间  $[a, b]$  为底边、以曲线  $y = f(x)$  为曲边的曲边梯形的面积等于同一底边而高为  $f(\xi)$  的一个矩形的面积(图 5-5).

按积分中值公式所得

$$
f (\xi) = \frac {1}{b - a} \int_ {a} ^ {b} f (x) \mathrm{d} x
$$

![](images/page_246_chart_9.jpg)

<details>
<summary>area</summary>

| X | Y |
| --- | --- |
| a | \(f(\xi)\) |
| \(\xi\) | \(f(\xi)\) |
| b | \(f(\xi)\) |
</details>

图5-5

称为函数 $f(x)$ 在区间 $[a,b]$ 上的平均值.例如按图5-5, $f(\xi)$ 可看作图中曲边梯形的平均高度.又如物体以变速 $v(t)$ 做直线运动，在时间区间 $[T_{1},T_{2}]$ 上经过的路程为 $\int_{T_{1}}^{T_{2}}v(t)\mathrm{d}t$ ，因此，

$$
v (\xi) = \frac {1}{T _ {2} - T _ {1}} \int_ {T _ {1}} ^ {T _ {2}} v (t) \mathrm{d} t, \quad \xi \in [ T _ {1}, T _ {2} ]
$$

便是运动物体在 $\left[T_{1},T_{2}\right]$ 这段时间内的平均速度.

## 习题5-1

\* 1. 利用定积分的定义计算由抛物线 $y = x^2 + 1$、两直线 $x = a, x = b (b > a)$ 及 $x$ 轴所围成的图形的面积.

\*2. 利用定积分的定义计算下列积分:

(1) $\int_{a}^{b}x\mathrm{d}x(a<b)$ ;

(2) $\int_0^1\mathrm{e}^x\mathrm{d}x.$

3. 利用定积分的几何意义, 证明下列等式:

(1) $\int_{0}^{1}2xdx=1;$

(2) $\int_0^1\sqrt{1 - x^2}\mathrm{d}x = \frac{\pi}{4};$

(3) $\int_{-\pi}^{\pi}\sin xdx=0;$

(4) $\int_{-\frac{\pi}{2}}^{\frac{\pi}{2}}\cos x\mathrm{d}x = 2\int_{0}^{\frac{\pi}{2}}\cos x\mathrm{d}x.$

4. 利用定积分的几何意义, 求下列积分:

(1) $\int_{0}^{t} x \, \mathrm{d}x (t > 0)$;

(2) $\int_{-2}^{4}\left(\frac{x}{2} + 3\right)\mathrm{d}x;$

(3) $\int_{-1}^{2}|x|\mathrm{d}x;$

(4) $\int_{-3}^{3}\sqrt{9 - x^2}\mathrm{d}x.$

5. 设 $a < b$ ，问 $a, b$ 取什么值时，积分 $\int_{a}^{b}(x - x^2) \, \mathrm{d}x$ 取得最大值？

6. 试从定积分的几何意义,说明以下等式成立:

$$
\int_ {1} ^ {\mathrm{e}} \ln x \mathrm{d} x + \int_ {0} ^ {1} \mathrm{e} ^ {x} \mathrm{d} x = \mathrm{e}.
$$

7. 已知 $\ln 2 = \int_{0}^{1} \frac{1}{1 + x} \mathrm{d}x$，试用抛物线法公式(1-6)，求出 $\ln 2$ 的近似值（取 $n = 10$，计算时取4位小数）.

8. 设 $\int_{-1}^{1} 3f(x) \, \mathrm{d}x = 18, \int_{-1}^{3} f(x) \, \mathrm{d}x = 4, \int_{-1}^{3} g(x) \, \mathrm{d}x = 3.$ 求:

(1) $\int_{-1}^{1} f(x) \, \mathrm{d}x$;

(2) $\int_{1}^{3} f(x) \, \mathrm{d}x$;

(3) $\int_{3}^{-1}g(x)\mathrm{d}x;$

(4) $\int_{-1}^{3}\frac{1}{5}[4f(x) + 3g(x)]\mathrm{d}x.$

9. 证明定积分的性质:

(1) $\int_{a}^{b}kf(x)\mathrm{d}x = k\int_{a}^{b}f(x)\mathrm{d}x$ ( $k$ 是常数);

(2) $\int_{a}^{b} 1 \cdot \mathrm{d}x = \int_{a}^{b} \mathrm{d}x = b - a.$

10. 估计下列各积分的值:

(1) $\int_{1}^{4}(x^2 + 1)\mathrm{d}x$;

(2) $\int_{\frac{\pi}{4}}^{\frac{5}{4}\pi}(1 + \sin^2 x)\mathrm{d}x;$

(3) $\int_{\frac{1}{\sqrt{3}}}^{\sqrt{3}}x\arctan xdx;$

(4) $\int_{2}^{0}\mathrm{e}^{x^{2}-x}\mathrm{d}x.$

11. 设 $f(x)$ 在 $[0,1]$ 上连续，证明 $\int_0^1 f^2 (x)\mathrm{d}x\geqslant \left[\int_0^1 f(x)\mathrm{d}x\right]^2.$

12. 设 $f(x)$ 及 $g(x)$ 在 $[a, b]$ 上连续，证明:

(1) 若在  $[a, b]$  上， $f(x) \geqslant 0$ ，且  $f(x) \neq 0$ ，则  $\int_{a}^{b} f(x) \, dx > 0$ ;

(2) 若在  $[a, b]$  上， $f(x) \geqslant 0$ ，且  $\int_{a}^{b} f(x) \, dx = 0$ ，则在  $[a, b]$  上  $f(x) \equiv 0$ ;

(3) 若在 $[a, b]$ 上，$f(x) \leqslant g(x)$，且 $\int_{a}^{b} f(x) \, \mathrm{d}x = \int_{a}^{b} g(x) \, \mathrm{d}x$，则在 $[a, b]$ 上 $f(x) \equiv g(x)$.

13. 根据定积分的性质及第 12 题的结论,说明下列各对积分中哪一个的值较大:

(1) $\int_{0}^{1}x^{2}dx$ 还是 $\int_{0}^{1}x^{3}dx?$

(2) $\int_{1}^{2} x^{2} \mathrm{~d} x$ 还是 $\int_{1}^{2} x^{3} \mathrm{~d} x$?

(3) $\int_{1}^{2}\ln xdx$ 还是 $\int_{1}^{2}(\ln x)^{2}dx?$

(4) $\int_0^1 x\mathrm{d}x$ 还是 $\int_0^1\ln (1 + x)\mathrm{d}x?$

(5) $\int_{0}^{1}e^{x}dx$ 还是 $\int_{0}^{1}(1+x)\mathrm{d}x$ ?

## 第二节 微积分基本公式

在第一节中有一个应用定积分的定义计算积分的例子.从这个例子我们看到,被积函数虽然是简单的幂函数 $f(x)=x^{2}$ ,但直接按定义来计算它的定积分已经不是很容易的事.如果被积函数是其他复杂的函数,其困难就更大了.因此,我们必须寻求计算定积分的新方法.

下面先从实际问题中寻找解决问题的线索.为此,我们对变速直线运动中遇到的位置函数 $s(t)$ 及速度函数 $v(t)$ 之间的联系作进一步的研究.

## 一、变速直线运动中位置函数与速度函数之间的联系

有一物体在一直线上运动.在这直线上取定原点、正方向及长度单位,使它成一数轴.设时刻 t 时物体所在位置为  $s(t)$ , 速度为  $v(t)$  (为了讨论方便起见, 可以设  $v(t) \geqslant 0$ ).

从第一节知道:物体在时间间隔 $\left[T_{1},T_{2}\right]$ 内经过的路程可以用速度函数 $v(t)$ 在 $\left[T_{1},T_{2}\right]$ 上的定积分

$$
\int_ {T _ {1}} ^ {T _ {2}} v (t) \mathrm{d} t
$$

来表达;另一方面,这段路程又可以通过位置函数 $s(t)$ 在区间 $[T_{1},T_{2}]$ 上的增量

$$
s (T _ {2}) - s (T _ {1})
$$

来表达.由此可见,位置函数 $s(t)$ 与速度函数 $v(t)$ 之间有如下关系:

$$
\int_ {T _ {1}} ^ {T _ {2}} v (t) \mathrm{d} t = s (T _ {2}) - s (T _ {1}). \tag {2-1}
$$

因为 $s'(t) = v(t)$，即位置函数 $s(t)$ 是速度函数 $v(t)$ 的原函数，所以关系式(2-1)表示，速度函数 $v(t)$ 在区间 $[T_1, T_2]$ 上的定积分等于 $v(t)$ 的原函数 $s(t)$ 在区间 $[T_1, T_2]$ 上的增量

$$
s (T _ {2}) - s (T _ {1}).
$$

上述从变速直线运动的路程这个特殊问题中得出来的关系,在一定条件下具有普遍性.事实上,我们将在第三目中证明,如果函数 $f(x)$ 在区间 $[a,b]$ 上连续,那么, $f(x)$ 在区间 $[a,b]$ 上的定积分就等于 $f(x)$ 的原函数(设为 $F(x)$)在区间 $[a,b]$ 上的增量

$$
F (b) - F (a).
$$

## 二、积分上限的函数及其导数

设函数 $f(x)$ 在区间 $[a, b]$ 上可积，并且设 $x$ 为 $[a, b]$ 上的一点。我们来考察 $f(x)$ 在

部分区间 $[a, x]$ 上的定积分

$$
\int_ {a} ^ {x} f (x) \mathrm{d} x.
$$

首先,由于 $f(x)$ 在 $[a,x]$ 上仍旧可积,因此这个定积分存在.这里,x既表示定积分的上限,又表示积分变量.因为定积分与积分变量的记法无关,所以,为了明确起见,可以把积分变量改用其他符号,例如用t表示,则上面的定积分可以写成

$$
\int_ {a} ^ {x} f (t) \mathrm{d} t.
$$

如果上限 x 在区间  $[a, b]$  上任意变动, 那么对于每一个取定的 x 值, 定积分有一个对应值, 所以它在  $[a, b]$  上定义了一个函数, 记作  $\Phi(x)$ :

$$
\Phi (x) = \int_ {a} ^ {x} f (t) \mathrm{d} t \quad (a \leqslant x \leqslant b).
$$

这个函数  $\Phi(x)$  具有下面定理 1 所指出的重要性质.

定理1 如果函数 $f(x)$ 在区间 $[a, b]$ 上连续，那么积分上限的函数

$$
\Phi (x) = \int_ {a} ^ {x} f (t)   \mathrm{d} t
$$

在 $[a, b]$ 上可导，并且它的导数

$$
\Phi^ {\prime} (x) = \frac {\mathrm{d}}{\mathrm{d} x} \int_ {a} ^ {x} f (t)   \mathrm{d} t = f (x) \quad (a \leqslant x \leqslant b). \tag {2-2}
$$

证 若 $x \in (a, b)$, 设 $x$ 获得增量 $\Delta x$, 其绝对值足够地小, 使得 $x + \Delta x \in (a, b)$, 则 $\Phi(x)$ (图5-6, 图中 $\Delta x > 0$) 在 $x + \Delta x$ 处的函数值为

$$
\Phi (x + \Delta x) = \int_ {a} ^ {x + \Delta x} f (t)   \mathrm{d} t.
$$

由此得函数的增量

$$
\begin{array}{l} \Delta \Phi = \Phi (x + \Delta x) - \Phi (x) \\ = \int_ {a} ^ {x + \Delta x} f (t) \mathrm{d} t - \int_ {a} ^ {x} f (t) \mathrm{d} t \\ = \int_ {a} ^ {x} f (t) \mathrm{d} t + \int_ {x} ^ {x + \Delta x} f (t) \mathrm{d} t - \int_ {a} ^ {x} f (t) \mathrm{d} t \\ = \int_ {x} ^ {x + \Delta x} f (t)   \mathrm{d} t. \\ \end{array}
$$

再应用积分中值定理,即有等式

$$
\Delta \Phi = f (\xi)   \Delta x  ,
$$

这里，$\xi$ 在 $x$ 与 $x + \Delta x$ 之间. 把上式两端各除以 $\Delta x$ ，得函数增量与自变量增量的比值

$$
\frac {\Delta \Phi}{\Delta x} = f (\xi).
$$

由于假设 $f(x)$ 在 $[a,b]$ 上连续，而 $\Delta x\to 0$ 时， $\xi \rightarrow x$ ，因此 $\lim_{\Delta x\to 0}f(\xi) = f(x)$ .于是，令$\Delta x \to 0$ 对上式两端取极限时, 左端的极限也应该存在且等于 $f(x)$. 这就是说, 函数 $\Phi(x)$ 的导数存在, 并且

![](images/page_249_image_21.jpg)

<details>
<summary>text_image</summary>

y
y=f(x)
Φ(x)
f(ξ)
O a x ξ x+Δx b x
</details>

图5-6

$$
\Phi^ {\prime} (x) = f (x).
$$

若 $x = a$ ，取 $\Delta x > 0$ ，则同理可证 $\Phi_{+}^{\prime}(a) = f(a)$ ；若 $x = b$ ，取 $\Delta x < 0$ ，则同理可证$\Phi_{-}^{\prime}(b) = f(b)$

定理 1 证毕.

这个定理指出了一个重要结论:连续函数 $f(x)$ 取变上限x的定积分然后求导,其结果还原为 $f(x)$ 本身.联想到原函数的定义,就可以从定理1推知 $\Phi(x)$ 是连续函数 $f(x)$ 的一个原函数.因此,我们引出如下的原函数存在定理:

定理2 如果函数 $f(x)$ 在区间 $[a, b]$ 上连续，那么函数

$$
\Phi (x) = \int_ {a} ^ {x} f (t) \mathrm{d} t \tag {2-3}
$$

就是 $f(x)$ 在 $[a,b]$ 上的一个原函数.

这个定理的重要意义是:一方面肯定了连续函数的原函数是存在的,另一方面初步地揭示了积分学中的定积分与原函数之间的联系.因此,我们就有可能通过原函数来计算定积分.

## 三、牛顿-莱布尼茨公式

现在我们根据定理 2 来证明一个重要定理——微积分基本定理, 它给出了用原函数计算定积分的公式.

定理3（微积分基本定理）如果函数 $F(x)$ 是连续函数 $f(x)$ 在区间 $[a, b]$ 上的一个原函数，那么

$$
\int_ {a} ^ {b} f (x) \mathrm{d} x = F (b) - F (a). \tag {2-4}
$$

证 已知函数 $F(x)$ 是连续函数 $f(x)$ 的一个原函数, 又根据定理2知道, 积分上限的函数

$$
\Phi (x) = \int_ {a} ^ {x} f (t) \mathrm{d} t
$$

也是 $f(x)$ 的一个原函数.于是这两个原函数之差 $F(x) - \Phi (x)$ 在 $[a,b]$ 上必定是某一个常数 $C$ （第四章第一节），即

$$
F (x) - \Phi (x) = C \quad (a \leqslant x \leqslant b). \tag {2-5}
$$

在上式中令 $x = a$ ，得 $F(a) - \Phi (a) = C.$ 又由 $\Phi (x)$ 的定义式(2-3)及上节定积分的补充规定(1)可知 $\Phi (a) = 0$ ，因此， $C = F(a)$ .以 $F(a)$ 代入(2-5)式中的 $C$ ，以 $\int_{a}^{x}f(t)\mathrm{d}t$ 代入(2-5)式中的 $\Phi (x)$ ，可得

$$
\int_ {a} ^ {x} f (t) \mathrm{d} t = F (x) - F (a).
$$

在上式中令 x=b，就得到所要证明的公式(2-4).

由上节定积分的补充规定(2)可知,(2-4)式对a>b的情形同样成立.

为了方便起见,以后把  $F(b)-F(a)$  记成  $[F(x)]_{a}^{b}$ , 于是(2-4)式又可写成

$$
\int_ {a} ^ {b} f (x) \mathrm{d} x = [ F (x) ] _ {a} ^ {b}.
$$

公式(2-4)叫做牛顿(Newton)-莱布尼茨(Leibniz)公式①,也叫做微积分基本公式.这个公式进一步揭示了定积分与被积函数的原函数或不定积分之间的联系.它表明:一个连续函数在区间[a,b]上的定积分等于它的任一个原函数在区间[a,b]上的增量.这就给定积分提供了一个有效而简便的计算方法,大大简化了定积分的计算步骤.

下面我们举几个应用公式(2-4)来计算定积分的简单例子.

例1 计算第一节中的定积分 $\int_0^1 x^2\mathrm{d}x.$

解 由于 $\frac{x^3}{3}$ 是 $x^2$ 的一个原函数, 所以按牛顿-莱布尼茨公式, 有

$$
\int_ {0} ^ {1} x ^ {2} \mathrm{d} x = \left[ \frac {x ^ {3}}{3} \right] _ {0} ^ {1} = \frac {1 ^ {3}}{3} - \frac {0 ^ {3}}{3} = \frac {1}{3} - 0 = \frac {1}{3}.
$$

例 2 计算  $\int_{-1}^{\sqrt{3}}\frac{dx}{1+x^{2}}$ .

解 由于 $\arctan x$ 是 $\frac{1}{1 + x^2}$ 的一个原函数, 所以

$$
\int_ {- 1} ^ {\sqrt {3}} \frac {\mathrm{d} x}{1 + x ^ {2}} = [ \arctan x ] _ {- 1} ^ {\sqrt {3}} = \arctan \sqrt {3} - \arctan (- 1) = \frac {\pi}{3} - \left(- \frac {\pi}{4}\right) = \frac {7}{1 2} \pi .
$$

例3 计算 $\int_{-2}^{-1}\frac{\mathrm{d}x}{x}.$

解 当 $x < 0$ 时, $\frac{1}{x}$ 的一个原函数是 $\ln |x|$, 现在积分区间是 $[-2, -1]$, 所以按牛顿-莱布尼茨公式, 有

$$
\int_ {- 2} ^ {- 1} \frac {\mathrm{d} x}{x} = [ \ln | x | ] _ {- 2} ^ {- 1} = \ln 1 - \ln 2 = - \ln 2.
$$

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 牛顿(Isaac Newton,1643—1727) 英国数学家、物理学家,微积分的奠基者.牛顿的微积分学说最早的公开表述是在1687年出版的巨著《自然哲学之数学原理》中.</span></small>

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">莱布尼茨(Gottfried Wilhelm Leibniz,1646—1716) 德国数学家,微积分的另一个奠基者.微积分基本定理的陈述最早出现在莱布尼茨1677年的一篇手稿中.</span></small>

通过例3,我们应该特别注意:公式(2-4)中的函数 $F(x)$ 必须是 $f(x)$ 在该积分区间 $[a,b]$ 上的原函数.

例4 计算正弦曲线 $y = \sin x$ 在 $[0, \pi]$ 上与 $x$ 轴所围成的平面图形（图5-7）的面积.

解 这图形是曲边梯形的一个特例. 它的面积

![](images/page_252_image_4.jpg)

<details>
<summary>text_image</summary>

y
y=sin x
O
π
x
</details>

图5-7

$$
A = \int_ {0} ^ {\pi} \sin x \mathrm{d} x.
$$

由于- $\cos x$ 是 $\sin x$ 的一个原函数,所以

$$
A = \int_ {0} ^ {\pi} \sin x \mathrm{d} x = [ - \cos x ] _ {0} ^ {\pi} = - (- 1) - (- 1) = 2.
$$

例 5 汽车以 36 km/h 速度沿直线行驶, 到某处需要减速停车. 设汽车以等加速度  $a = -5 \, m/s^{2}$  刹车. 问从开始刹车到停车, 汽车驶过了多少距离?

解 首先要算出从开始刹车到停车经过的时间. 设开始刹车的时刻为 t=0, 此时汽车速度

$$
v _ {0} = 3 6 \mathrm{km/h} = \frac {3 6 \times 1 0 0 0}{3 6 0 0} \mathrm{m/s} = 1 0 \mathrm{m/s}.
$$

刹车后汽车减速行驶,其速度为

$$
v (t) = v _ {0} + a t = 1 0 - 5 t.
$$

当汽车停住时,速度  $v(t)=0$ , 故从

$$
v (t) = 1 0 - 5 t = 0
$$

解得

$$
t = \frac {1 0}{5} = 2 (\mathrm{s}).
$$

于是在这段时间内,汽车所驶过的距离为

$$
s = \int_ {0} ^ {2} v (t) \mathrm{d} t = \int_ {0} ^ {2} (1 0 - 5 t) \mathrm{d} t = \left[ 1 0 t - 5 \times \frac {t ^ {2}}{2} \right] _ {0} ^ {2} = 1 0 (\mathrm{m}),
$$

即在刹车后,汽车需驶过10 m才能停住.

例6 证明积分中值定理: 若函数 $f(x)$ 在闭区间 $[a, b]$ 上连续, 则在开区间 $(a, b)$ 内至少存在一点 $\xi$, 使

$$
\int_ {a} ^ {b} f (x) \mathrm{d} x = f (\xi) (b - a) (a <   \xi <   b).
$$

证 因 $f(x)$ 连续, 故它的原函数存在, 设为 $F(x)$, 即设在 $[a, b]$ 上 $F'(x) = f(x)$. 根据牛顿-莱布尼茨公式, 有

$$
\int_ {a} ^ {b} f (x) \mathrm{d} x = F (b) - F (a).
$$

显然函数 $F(x)$ 在区间 $[a, b]$ 上满足微分中值定理的条件，因此按微分中值定理，在开区间 $(a, b)$ 内至少存在一点 $\xi$，使

$$
F (b) - F (a) = F ^ {\prime} (\xi) (b - a), \quad \xi \in (a, b),
$$

故

$$
\int_ {a} ^ {b} f (x) \mathrm{d} x = f (\xi) (b - a), \quad \xi \in (a, b).
$$

本例的结论是上一节所述积分中值定理的改进.从本例的证明中不难看出积分中值定理与微分中值定理的联系.

下面再举几个应用公式(2-2)的例子.

例7 设 $f(x)$ 在 $[0, +\infty)$ 内连续且 $f(x) > 0$. 证明函数

$$
F (x) = \frac {\int_ {0} ^ {x} t f (t) \mathrm{d} t}{\int_ {0} ^ {x} f (t) \mathrm{d} t}
$$

在 $(0,+\infty)$ 内为单调增加函数.

证 由公式(2-2)，得

$$
\frac {\mathrm{d}}{\mathrm{d} x} \int_ {0} ^ {x} t f (t) \mathrm{d} t = x f (x), \quad \frac {\mathrm{d}}{\mathrm{d} x} \int_ {0} ^ {x} f (t) \mathrm{d} t = f (x).
$$

故

$$
F ^ {\prime} (x) = \frac {x f (x) \int_ {0} ^ {x} f (t) \mathrm{d} t - f (x) \int_ {0} ^ {x} t f (t) \mathrm{d} t}{\left[ \int_ {0} ^ {x} f (t) \mathrm{d} t \right] ^ {2}} = \frac {f (x) \int_ {0} ^ {x} (x - t) f (t) \mathrm{d} t}{\left[ \int_ {0} ^ {x} f (t) \mathrm{d} t \right] ^ {2}}.
$$

按假设, 当 0 < t < x 时  $f(t) > 0$ ,  $(x - t)f(t) > 0$ , 按例 6 所述积分中值定理可知

$$
\int_ {0} ^ {x} f (t) \mathrm{d} t > 0, \quad \int_ {0} ^ {x} (x - t) f (t) \mathrm{d} t > 0,
$$

所以  $F'(x)>0\ (x>0)$ ，从而  $F(x)$  在  $(0,+\infty)$  内为单调增加函数.

例8 求 $\lim_{x\to 0}\frac{\int_{\cos x}^{1}\mathrm{e}^{-t^2}\mathrm{d}t}{x^2}.$

解 易知这是一个 $\frac{0}{0}$ 型的未定式, 我们利用洛必达法则来计算. 分子可写成

$$
- \int_ {1} ^ {\cos x} \mathrm{e} ^ {- t ^ {2}} \mathrm{d} t,
$$

它是以  $\cos x$  为上限的积分,作为 x 的函数可看成是以  $u = \cos x$  为中间变量的复合函数,故由公式(2-2)有

![](images/page_254_image_1.jpg)

释疑解难

5-1

$$
\begin{array}{l} \frac {\mathrm{d}}{\mathrm{d} x} \int_ {\cos x} ^ {1} \mathrm{e} ^ {- t ^ {2}} \mathrm{d} t = - \frac {\mathrm{d}}{\mathrm{d} x} \int_ {1} ^ {\cos x} \mathrm{e} ^ {- t ^ {2}} \mathrm{d} t = - \frac {\mathrm{d}}{\mathrm{d} u} \int_ {1} ^ {u} \mathrm{e} ^ {- t ^ {2}} \mathrm{d} t \Big | _ {u = \cos x} \cdot (\cos x) ^ {\prime} \\ = - \mathrm{e} ^ {- \cos^ {2} x} \cdot (- \sin x) = \sin x \mathrm{e} ^ {- \cos^ {2} x}. \\ \end{array}
$$

因此

$$
\lim _ {x \to 0} \frac {\int_ {\cos x} ^ {1} e ^ {- t ^ {2}} d t}{x ^ {2}} = \lim _ {x \to 0} \frac {\sin x e ^ {- \cos^ {2} x}}{2 x} = \frac {1}{2 e}.
$$

## 习题 5-2

1. 试求函数 $y = \int_{0}^{x} \sin t \, \mathrm{d}t$ 当 $x = 0$ 及 $x = \frac{\pi}{4}$ 时的导数.
2. 求由参数表达式 $x = \int_{0}^{t} \sin u \, \mathrm{d}u, y = \int_{0}^{t} \cos u \, \mathrm{d}u$ 所确定的函数对 $x$ 的导数 $\frac{\mathrm{d}y}{\mathrm{d}x}$.
3. 求由  $\int_{0}^{y} e^{t} dt + \int_{0}^{x} \cos t dt = 0$  所确定的隐函数对 x 的导数  $\frac{dy}{dx}$ .
4. 当 $x$ 为何值时, 函数 $I(x) = \int_{0}^{x} t e^{-t^2} \mathrm{d}t$ 有极值?

5. 计算下列各导数:

(1) $\frac{\mathrm{d}}{\mathrm{d}x}\int_{0}^{x^2}\sqrt{1 + t^2}\mathrm{d}t;$

(2) $\frac{\mathrm{d}}{\mathrm{d}x}\int_{x^2}^{x^3}\frac{\mathrm{d}t}{\sqrt{1 + t^4}};$

(3) $\frac{\mathrm{d}}{\mathrm{d}x}\int_{\sin x}^{\cos x}\cos (\pi t^2)\mathrm{d}t.$

6. 证明 $f(x) = \int_{1}^{x} \sqrt{1 + t^3} \, \mathrm{d}t$ 在 $[-1, +\infty)$ 上是单调增加函数，并求 $(f^{-1})'(0)$.

7. 设 $f(x) = \int_{0}^{x}\left(\int_{\sin t}^{1}\sqrt{1 + u^4}\mathrm{d}u\right)\mathrm{d}t$, 求 $f''\left(\frac{\pi}{3}\right)$.

8. 设 $f(x)$ 具有三阶连续导数, $y = f(x)$ 的图形如图5-8所示. 问下列积分中的哪一个积分值为负?

(A) $\int_{-1}^{3} f(x) \, \mathrm{d}x$

(B) $\int_{-1}^{3} f'(x) \, \mathrm{d}x$

(C) $\int_{-1}^{3} f''(x) \, \mathrm{d}x$

(D) $\int_{-1}^{3} f'''(x) \, \mathrm{d}x$

9. 计算下列各定积分:

(1) $\int_{0}^{a}(3x^{2} - x + 1)\mathrm{d}x;$

(2) $\int_{1}^{2}\left(x^{2} + \frac{1}{x^{4}}\right)\mathrm{d}x;$

(3) $\int_{4}^{9}\sqrt{x}(1+\sqrt{x})dx;$

(4) $\int_{\frac{1}{\sqrt{3}}}\frac{\mathrm{d}x}{1 + x^2};$

![](images/page_254_chart_29.jpg)

<details>
<summary>contour</summary>

| X | Y |
| --- | --- |
| -1 | 0 |
| 0 | ~0.2 |
| 0.8 | ~0.8 |
| 1.2 | ~0.4 |
| 1.7 | ~0.6 |
| 3 | 0 |
</details>

图5-8

(5) $\int_{-\frac{1}{2}}^{\frac{1}{2}}\frac{\mathrm{d}x}{\sqrt{1 - x^2}};$

(6) $\int_0^{\sqrt{3} a}\frac{\mathrm{d}x}{a^2 + x^2};$

(7) $\int_0^1\frac{\mathrm{d}x}{\sqrt{4 - x^2}};$

(8) $\int_{-1}^{0}\frac{3x^4 + 3x^2 + 1}{x^2 + 1}\mathrm{d}x;$

(9) $\int_{-e - 1}^{-2}\frac{\mathrm{d}x}{1 + x};$

(10) $\int_{0}^{\frac{\pi}{4}}\tan^{2}\theta\mathrm{d}\theta;$

(11) $\int_{0}^{2\pi}\left|\sin x\right|dx;$

(12) $\int_0^2 f(x)\mathrm{d}x$ ，其中 $f(x) = \left\{ \begin{array}{ll}x + 1, & x\leqslant 1,\\ \frac{1}{2} x^2, & x > 1. \end{array} \right.$

10. 设 $k \in \mathbb{N}_{+}$. 试证下列各题:

(1) $\int_{-\pi}^{\pi}\cos kxdx=0;$

(2) $\int_{-\pi}^{\pi}\sin kxdx=0;$

(3) $\int_{-\pi}^{\pi}\cos^{2}kxdx=\pi;$

(4) $\int_{-\pi}^{\pi}\sin^2 kx\mathrm{d}x = \pi .$

11. 设 $k, l \in \mathbb{N}_{+}$, 且 $k \neq l$. 证明:

(1) $\int_{-\pi}^{\pi}\cos kx\sin lxdx=0;$

(2) $\int_{-\pi}^{\pi}\cos kx\cos lxdx=0;$

(3) $\int_{-\pi}^{\pi}\sin kx\sin lxdx=0.$

12. 求下列极限:

(1)  $\lim_{x\to0}\frac{\int_{0}^{x}\cos t^{2}dt}{x};$

(2) $\lim_{x\to 0}\frac{\left(\int_0^x\mathrm{e}^{t^2}\mathrm{d}t\right)^2}{\int_0^x t\mathrm{e}^{2t^2}\mathrm{d}t}.$

13. 设

$$
f (x) = \left\{ \begin{array}{l l} x ^ {2}, & x \in [ 0, 1), \\ x, & x \in [ 1, 2 ]. \end{array} \right.
$$

求  $\Phi(x)=\int_{0}^{x}f(t)\mathrm{d}t$  在  $[0,2]$  上的表达式，并讨论  $\Phi(x)$  在  $(0,2)$  内的连续性.

14. 设

$$
f (x) = \left\{ \begin{array}{l l} \frac {1}{2} \sin x, & 0 \leqslant x \leqslant \pi , \\ 0, & x <   0 \text {或} x > \pi . \end{array} \right.
$$

求  $\Phi(x)=\int_{0}^{x}f(t)\mathrm{d}t$  在  $(-∞,+∞)$  内的表达式.

15. 设 $f(x)$ 在 $[a, b]$ 上连续，在 $(a, b)$ 内可导且 $f'(x) \leqslant 0$,

$$
F (x) = \frac {1}{x - a} \int_ {a} ^ {x} f (t)   \mathrm{d} t.
$$

证明在 $(a,b)$ 内有 $F'(x)\leqslant0$ .

16. 以下积分上限的函数:

$$
S (x) = \int_ {0} ^ {x} \sin \frac {\pi t ^ {2}}{2} \mathrm{d} t, \quad x \in (- \infty , + \infty)
$$