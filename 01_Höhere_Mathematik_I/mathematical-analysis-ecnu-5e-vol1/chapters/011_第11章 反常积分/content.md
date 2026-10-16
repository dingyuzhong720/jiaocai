# 第11章 反常积分

原始 PDF 第 258–273 页。

## 第十一章反常积分

## § 1 反常积分概念

## 一、问题提出

在讨论定积分时有两个最基本的限制:积分区间的有穷性和被积函数的有界性.但在很多实际问题中往往需要突破这些限制,考虑无穷区间上的“积分”,或是无界函数的“积分”,这便是本章的主题.

例 1(第二宇宙速度问题) 在地球表面垂直发射火箭(图 11-1), 要使火箭克服地球引力无限远离地球, 试问初速度  $v_{0}$  至少要多大?

设地球半径为 R，火箭质量为 m，地面上的重力加速度为 g。按万有引力定律，在距地心  $x(\geqslant R)$  处火箭所受的引力为

$$
F = \frac {m g R ^ {2}}{x ^ {2}}.
$$

于是火箭从地面上升到距离地心为  $r (>R)$  处需做的功为

$$
\int_ {R} ^ {r} \frac {m g R ^ {2}}{x ^ {2}} \mathrm{d} x = m g R ^ {2} \bigg (\frac {1}{R} - \frac {1}{r} \bigg).
$$

![](../../raw/pages_0257-0288/images/page_257_image_9.jpg)

<details>
<summary>text_image</summary>

x
r
x
R
O
</details>

图11-1

当  $r \rightarrow +\infty$  时, 其极限 mgR 就是火箭无限远离地球需做的功. 我们很自然地会把这极限写作上限为  $+\infty$  的“积分”:

$$
\int_ {R} ^ {+ \infty} \frac {m g R ^ {2}}{x ^ {2}} \mathrm{d} x = \lim _ {r \to + \infty} \int_ {R} ^ {r} \frac {m g R ^ {2}}{x ^ {2}} \mathrm{d} x = m g R.
$$

最后,由机械能守恒定律可求得初速度  $v_{0}$  至少应使

$$
\frac {1}{2} m v _ {0} ^ {2} = m g R.
$$

用  $g=9.81\ m/s^{2}, R=6.371\times10^{6}\ m$  代入, 便得

$$
v _ {0} = \sqrt {2 g R} \approx 1 1. 2 (\mathrm{km/s}).
$$

例 2 圆柱形桶的内壁高为 h，内半径为 R，桶底有一半径为 r 的小孔（图11-2）。试问从盛满水开始打开小孔直至流完桶中的水，共需多少时间？

247

---

第十一章 反常积分

从物理学知道,在不计摩擦力的情形下,当桶内水位高度为h-x时,水从孔中流出的流速(单位时间内流过单位截面积的流量)为

$$
v = \sqrt {2 g (h - x)},
$$

其中 g 为重力加速度.

设在很小一段时间 dt 内, 桶中液面降低的微小量为 dx, 它们之间应满足

$$
\pi R ^ {2} \mathrm{d} x = v \pi r ^ {2} \mathrm{d} t,
$$

由此则有

$$
\mathrm{d} t = \frac {R ^ {2}}{r ^ {2} \sqrt {2 g (h - x)}} \mathrm{d} x, x \in [ 0, h).
$$

所以流完一桶水所需时间在形式上亦可写成“积分”:

$$
t _ {f} = \int_ {0} ^ {h} \frac {R ^ {2}}{r ^ {2} \sqrt {2 g (h - x)}} \mathrm{d} x.
$$

但是在这里因为被积函数是 $[0, h)$ 上的无界函数，所以它的确切含义应该是

$$
\begin{array}{l} t _ {f} = \lim _ {u \to h ^ {-}} \int_ {0} ^ {u} \frac {R ^ {2}}{r ^ {2} \sqrt {2 g (h - x)}} \mathrm{d} x \\ = \lim _ {u \to h ^ {-}} \sqrt {\frac {2}{g}} \cdot \frac {R ^ {2}}{r ^ {2}} (\sqrt {h} - \sqrt {h - u}) \\ = \sqrt {\frac {2 h}{g}} \left(\frac {R}{r}\right) ^ {2}. \\ \end{array}
$$

![](../../raw/pages_0257-0288/images/page_258_image_12.jpg)

<details>
<summary>text_image</summary>

O
R
x
Δx
h
r
</details>

图11-2

相对于以前所讲的定积分(不妨称之为正常积分)而言,例1和例2分别提出了两类反常积分.

## 二、两类反常积分的定义

定义1 设函数 $f$ 定义在无穷区间 $[a, +\infty)$ 上，且在任何有限区间 $[a, u]$ 上可积。如果存在极限

$$
\lim _ {u \to + \infty} \int_ {a} ^ {u} f (x)   \mathrm{d} x = J, \tag {1}
$$

则称此极限 J 为函数 f 在  $[a, +\infty)$  上的无穷限反常积分（简称无穷积分），记作

$$
J = \int_ {a} ^ {+ \infty} f (x) \mathrm{d} x, \tag {$1^{\prime$}}
$$

并称 $\int_{a}^{+\infty}f(x)\mathrm{d}x$ 收敛.如果极限(1)不存在，为方便起见，亦称 $\int_{a}^{+\infty}f(x)\mathrm{d}x$ 发散.

类似地,可定义f在 $(-∞,b]$ 上的无穷积分:

$$
\int_ {- \infty} ^ {b} f (x) \mathrm{d} x = \lim _ {u \to - \infty} \int_ {u} ^ {b} f (x) \mathrm{d} x. \tag {2}
$$

对于 $f$ 在 $(-\infty, +\infty)$ 上的无穷积分，用前面两种无穷积分来定义:

$$
\int_ {- \infty} ^ {+ \infty} f (x) \mathrm{d} x = \int_ {- \infty} ^ {a} f (x) \mathrm{d} x + \int_ {a} ^ {+ \infty} f (x) \mathrm{d} x, \tag {3}
$$

248

---

§ 1 反常积分概念

其中 $a$ 为任一实数. 当且仅当等号右边两个无穷积分都收敛时, 它才是收敛的.

注1 无穷积分(3)的收敛性与收敛时的值,都和实数 a 的选取无关.

注2 由于无穷积分(3)是由(1)、(2)两类无穷积分来定义的,因此,f在任何有限区间 $[v,u]\subset(-\infty,+\infty)$ 上,首先必须是可积的.

注3 $\int_{a}^{+\infty}f(x)\mathrm{d}x$ 收敛的几何意义是:若 $f$ 在 $[a, + \infty)$ 上为非负连续函数，则图11-3中介于曲线 $y = f(x)$，直线$x = a$ 以及 $x$ 轴之间那一块向右无限延伸的阴影区域有面积 $J$.

![](../../raw/pages_0257-0288/images/page_259_image_5.jpg)

<details>
<summary>text_image</summary>

y
y=f(x)
O
a
x
</details>

图11-3

例3 讨论无穷积分

$$
\int_ {1} ^ {+ \infty} \frac {\mathrm{d} x}{x ^ {p}} \tag {4}
$$

的敛散性.

解 由于

$$
\int_ {1} ^ {u} \frac {\mathrm{d} x}{x ^ {p}} = \left\{ \begin{array}{l l} \frac {1}{1 - p} (u ^ {1 - p} - 1), & p \neq 1, \\ \ln u, & p = 1, \end{array} \right.
$$

$$
\lim _ {u \to + \infty} \int_ {1} ^ {u} \frac {\mathrm{d} x}{x ^ {p}} = \left\{ \begin{array}{l l} \frac {1}{p - 1}, & p > 1, \\ + \infty , & p \leqslant 1. \end{array} \right.
$$

因此无穷积分(4)当p>1时收敛,其值为 $\frac{1}{p-1}$ ;而当 $p\leqslant$ 1时发散于 $+\infty$ .

从图 11-4 看到, 例 3 的结论是很直观的: p 的值越大, 曲线  $y=\frac{1}{x^{p}}$  当 x>1 时越靠近 x 轴, 从而曲线下方的阴影区域存在有限面积的可能性也就越大.

![](../../raw/pages_0257-0288/images/page_259_chart_15.jpg)

<details>
<summary>area</summary>

| Category | Description |
| --- | --- |
| Curve 1 | p < 1 |
| Curve 2 | p = 1 |
| Curve 3 | p > 1 |
| Curve 4 | p < 1 |
| Curve 5 | p = 1 |
| Curve 6 | p > 1 |
</details>

图11-4

例4 讨论下列无穷积分的敛散性:

1) $\int_{2}^{+\infty}\frac{\mathrm{d}x}{x(\ln x)^p};$

2） $\int_{-\infty}^{+\infty}\frac{\mathrm{d}x}{1 + x^2}.$

解 1）由于无穷积分是通过变限定积分的极限来定义的,因此有关定积分的换元积分法和分部积分法一般都可引用到无穷积分中来.对于本例来说,就有

$$
\int_ {2} ^ {+ \infty} \frac {\mathrm{d} x}{x (\ln x) ^ {p}} = \int_ {\ln 2} ^ {+ \infty} \frac {\mathrm{d} t}{t ^ {p}}.
$$

从例 3 知道,该无穷积分当 p>1 时收敛,当  $p \leqslant 1$  时发散.

2）任取实数 a，讨论如下两个无穷积分:

$$
\int_ {- \infty} ^ {a} {\frac {\mathrm{d} x}{1 + x ^ {2}}} \quad {\text {和}} \quad \int_ {a} ^ {+ \infty} {\frac {\mathrm{d} x}{1 + x ^ {2}}}.
$$

由于

249

---

第十一章 反常积分

$$
\lim _ {u \to - \infty} \int_ {u} ^ {a} \frac {\mathrm{d} x}{1 + x ^ {2}} = \lim _ {u \to - \infty} (\arctan a - \arctan u) = \arctan a + \frac {\pi}{2},
$$

$$
\lim _ {v \to + \infty} \int_ {a} ^ {v} \frac {\mathrm{d} x}{1 + x ^ {2}} = \lim _ {v \to + \infty} (\arctan v - \arctan a) = \frac {\pi}{2} - \arctan a,
$$

因此这两个无穷积分都收敛.由定义1,

$$
\int_ {- \infty} ^ {+ \infty} \frac {\mathrm{d} x}{1 + x ^ {2}} = \int_ {- \infty} ^ {a} \frac {\mathrm{d} x}{1 + x ^ {2}} + \int_ {a} ^ {+ \infty} \frac {\mathrm{d} x}{1 + x ^ {2}} = \pi .
$$

注 由于上述结果与 a 无关, 因此若取 a=0, 则可使计算过程更简洁些.

定义 2 设函数 f 定义在区间  $(a, b]$  上, 在点 a 的任一右邻域上无界, 但在任何内闭区间  $[u, b] \subset (a, b]$  上有界且可积. 如果存在极限

$$
\lim _ {u \to a ^ {+}} \int_ {u} ^ {b} f (x) \mathrm{d} x = J, \tag {5}
$$

则称此极限为无界函数 $f$ 在 $(a,b]$ 上的反常积分，记作

$$
J = \int_ {a} ^ {b} f (x) \mathrm{d} x, \tag {$5^{\prime$}}
$$

并称反常积分 $\int_{a}^{b}f(x)\mathrm{d}x$ 收敛.如果极限(5)不存在，这时也说反常积分 $\int_{a}^{b}f(x)\mathrm{d}x$ 发散.

在定义2中,被积函数f在点a近旁是无界的,这时点a称为f的瑕点,而无界函数反常积分 $\int_{a}^{b}f(x)\mathrm{d}x$ 又称为瑕积分.

类似地,可定义瑕点为 b 时的瑕积分:

$$
\int_ {a} ^ {b} f (x) \mathrm{d} x = \lim _ {u \to b ^ {-}} \int_ {a} ^ {u} f (x) \mathrm{d} x.
$$

其中 $f$ 在 $[a, b)$ 有定义，在点 $b$ 的任一左邻域上无界，但在任何 $[a, u] \subset [a, b)$ 上可积.

若 $f$ 的瑕点 $c \in (a, b)$, 则定义瑕积分

$$
\begin{array}{l} \int_ {a} ^ {b} f (x) \mathrm{d} x = \int_ {a} ^ {c} f (x) \mathrm{d} x + \int_ {c} ^ {b} f (x) \mathrm{d} x \\ = \lim _ {u \to c ^ {-}} \int_ {a} ^ {u} f (x) \mathrm{d} x + \lim _ {v \to c ^ {+}} \int_ {v} ^ {b} f (x) \mathrm{d} x. \tag {6} \\ \end{array}
$$

其中 $f$ 在 $[a, c) \cup (c, b]$ 上有定义，在点 $c$ 的任一邻域上无界，但在任何 $[a, u] \subset [a, c)$ 和 $[v, b] \subset (c, b]$ 上都可积。当且仅当(6)式右边两个瑕积分都收敛时，左边的瑕积分才是收敛的。

又若 a, b 两点都是 f 的瑕点，而 f 在任何  $[u, v] \subset (a, b)$  上可积，这时定义瑕积分

$$
\begin{array}{l} \int_ {a} ^ {b} f (x) \mathrm{d} x = \int_ {a} ^ {c} f (x) \mathrm{d} x + \int_ {c} ^ {b} f (x) \mathrm{d} x \\ = \lim _ {u \to a ^ {+}} \int_ {u} ^ {c} f (x) \mathrm{d} x + \lim _ {v \to b ^ {-}} \int_ {c} ^ {v} f (x) \mathrm{d} x, \tag {7} \\ \end{array}
$$

其中 c 为  $(a, b)$  上任一实数. 同样地, 当且仅当 (7) 式右边两个瑕积分都收敛时, 左边的瑕积分才是收敛的.

例 5 计算瑕积分  $\int_{0}^{1}\frac{dx}{\sqrt{1-x^{2}}}$  的值.

250

---

§ 1 反常积分概念

解 被积函数 $f(x) = \frac{1}{\sqrt{1 - x^2}}$ 在 $[0,1)$ 上连续，从而在任何 $[0,u] \subset [0,1)$ 上可积，$x = 1$ 为其瑕点.依定义2求得

$$
\int_ {0} ^ {1} \frac {\mathrm{d} x}{\sqrt {1 - x ^ {2}}} = \lim _ {u \to 1 ^ {-}} \int_ {0} ^ {u} \frac {\mathrm{d} x}{\sqrt {1 - x ^ {2}}} = \lim _ {u \to 1 ^ {-}} \arcsin u = \frac {\pi}{2}.
$$

例6 讨论瑕积分

$$
\int_ {0} ^ {1} \frac {\mathrm{d} x}{x ^ {q}} (q > 0) \tag {8}
$$

的收敛性.

解 被积函数在 $(0,1]$ 上连续,x=0为其瑕点.由于

$$
\int_ {u} ^ {1} \frac {\mathrm{d} x}{x ^ {q}} = \left\{ \begin{array}{l l} \frac {1}{1 - q} (1 - u ^ {1 - q}), & q \neq 1, \\ - \ln u, & q = 1 \end{array} \right. (0 <   u <   1),
$$

故当 $0 < q < 1$ 时，瑕积分(8)收敛，且

$$
\int_ {0} ^ {1} \frac {\mathrm{d} x}{x ^ {q}} = \lim _ {u \to 0 ^ {+}} \int_ {u} ^ {1} \frac {\mathrm{d} x}{x ^ {q}} = \frac {1}{1 - q};
$$

而当 $q \geqslant 1$ 时，瑕积分(8)发散于 $+\infty$

上述结论在图 11-4 中同样能获得直观的反映.

如果把例 3 与例 6 联系起来,考察反常积分

$$
\int_ {0} ^ {+ \infty} \frac {\mathrm{d} x}{x ^ {p}} (p > 0). \tag {9}
$$

我们定义

$$
\int_ {0} ^ {+ \infty} \frac {\mathrm{d} x}{x ^ {p}} = \int_ {0} ^ {1} \frac {\mathrm{d} x}{x ^ {p}} + \int_ {1} ^ {+ \infty} \frac {\mathrm{d} x}{x ^ {p}},
$$

它当且仅当右边的瑕积分和无穷积分都收敛时才收敛.但由例3与例6的结果可知,这两个反常积分不能同时收敛,故反常积分(9)对任何实数p都是发散的.

## 习题 11.1

1. 讨论下列无穷积分是否收敛？若收敛，则求其值:

(1) $\int_{0}^{+\infty} x \mathrm{e}^{-x^2} \, \mathrm{d}x$;

(2) $\int_{-\infty}^{+\infty} x \mathrm{e}^{-x^2} \, \mathrm{d}x$;

(3) $\int_{0}^{+\infty}\frac{1}{\sqrt{\mathrm{e}^x}}\mathrm{d}x;$

(4) $\int_{1}^{+\infty}\frac{\mathrm{d}x}{x^2(1 + x)};$

(5) $\int_{-\infty}^{+\infty}\frac{\mathrm{d}x}{4x^2 + 4x + 5};$

(6) $\int_{0}^{+\infty}\mathrm{e}^{-x}\sin x\mathrm{d}x;$

(7) $\int_{-\infty}^{+\infty}\mathrm{e}^x\sin x\mathrm{d}x;$

(8) $\int_{0}^{+\infty}\frac{\mathrm{d}x}{\sqrt{1 + x^2}}.$

2. 讨论下列瑕积分是否收敛？若收敛，则求其值:

(1) $\int_{a}^{b}\frac{\mathrm{d}x}{(x - a)^p};$

(2) $\int_{0}^{1}\frac{\mathrm{d}x}{1 - x^2};$

251

---

第十一章 反常积分

(3) $\int_0^2\frac{\mathrm{d}x}{\sqrt{|x - 1|}};$

(4) $\int_0^1\frac{x}{\sqrt{1 - x^2}}\mathrm{d}x;$

(5) $\int_0^1\ln x\mathrm{d}x$

(6) $\int_0^1\sqrt{\frac{x}{1 - x}}\mathrm{d}x;$

(7) $\int_0^1\frac{\mathrm{d}x}{\sqrt{x - x^2}};$

(8) $\int_{0}^{1}\frac{\mathrm{d}x}{x(\ln x)^p}.$

3. 举例说明: 瑕积分  $\int_{a}^{b} f(x) \, dx$  收敛时,  $\int_{a}^{b} f^{2}(x) \, dx$  不一定收敛.

4. 举例说明: $\int_{a}^{+\infty}f(x)\mathrm{d}x$ 收敛且f在 $[a,+\infty)$ 上连续时，不一定有 $\lim_{x\to+\infty}f(x)=0$ .

5. 证明: 若 $\int_{a}^{+\infty} f(x) \, \mathrm{d}x$ 收敛, 且存在极限 $\lim_{x \to +\infty} f(x) = A$, 则 $A = 0$.

6. 证明: 若 $f$ 在 $[a, +\infty)$ 上可导, 且 $\int_{a}^{+\infty} f(x) \mathrm{d}x$ 与 $\int_{a}^{+\infty} f'(x) \mathrm{d}x$ 都收敛, 则 $\lim_{x \to +\infty} f(x) = 0$.

## § 2 无穷积分的性质与敛散判别

## 一、无穷积分的性质

由定义知道,无穷积分  $\int_{a}^{+\infty}f(x)\mathrm{d}x$  收敛与否,取决于函数  $F(u)=\int_{a}^{u}f(x)\mathrm{d}x$  在  $u\to+\infty$  时是否存在极限.因此可由函数极限的柯西准则导出无穷积分收敛的柯西准则.

定理11.1 无穷积分 $\int_{a}^{+\infty} f(x) \, \mathrm{d}x$ 收敛的充要条件是: 任给 $\varepsilon > 0$, 存在 $G \geqslant a$, 只要 $u_{1}, u_{2} > G$, 便有

$$
\left| \int_ {a} ^ {u _ {2}} f (x) \mathrm{d} x - \int_ {a} ^ {u _ {1}} f (x) \mathrm{d} x \right| = \left| \int_ {u _ {1}} ^ {u _ {2}} f (x) \mathrm{d} x \right| <   \varepsilon .
$$

此外,还可根据函数极限的性质与定积分的性质,导出无穷积分的一些相应性质.

性质1 若 $\int_{a}^{+\infty}f_1(x)\mathrm{d}x$ 与 $\int_{a}^{+\infty}f_2(x)\mathrm{d}x$ 都收敛， $k_{1},k_{2}$ 为任意常数，则 $\int_{a}^{+\infty}[k_{1}f_{1}(x) + k_{2}f_{2}(x)]\mathrm{d}x$ 也收敛，且

$$
\int_ {a} ^ {+ \infty} \left[ k _ {1} f _ {1} (x) + k _ {2} f _ {2} (x) \right] \mathrm{d} x = k _ {1} \int_ {a} ^ {+ \infty} f _ {1} (x) \mathrm{d} x + k _ {2} \int_ {a} ^ {+ \infty} f _ {2} (x) \mathrm{d} x. \tag {1}
$$

性质2 若 $f$ 在任何有限区间 $[a, u]$ 上可积，$a < b$，则 $\int_{a}^{+\infty} f(x) \mathrm{d}x$ 与 $\int_{b}^{+\infty} f(x) \mathrm{d}x$ 同敛态（即同时收敛或同时发散），且有

$$
\int_ {a} ^ {+ \infty} f (x) \mathrm{d} x = \int_ {a} ^ {b} f (x) \mathrm{d} x + \int_ {b} ^ {+ \infty} f (x) \mathrm{d} x, \tag {2}
$$

其中右边第一项是定积分.

性质 2 相当于定积分的积分区间可加性, 由它又可导出  $\int_{a}^{+\infty} f(x) \, dx$  收敛的另一充

252

---

§ 2 无穷积分的性质与敛散判别

要条件:任给  $\varepsilon > 0$ , 存在  $G \geqslant a$ , 当 u > G 时, 总有

$$
\left| \int_ {u} ^ {+ \infty} f (x)   \mathrm{d} x \right| <   \varepsilon .
$$

事实上，这可由

$$
\int_ {a} ^ {+ \infty} f (x) \mathrm{d} x = \int_ {a} ^ {u} f (x) \mathrm{d} x + \int_ {u} ^ {+ \infty} f (x) \mathrm{d} x
$$

结合无穷积分的收敛定义而得.

性质3 若 $f$ 在任何有限区间 $[a, u]$ 上可积，且有 $\int_{a}^{+\infty}|f(x)|\mathrm{d}x$ 收敛，则 $\int_{a}^{+\infty}f(x)\mathrm{d}x$ 亦必收敛，并有

$$
\left| \int_ {a} ^ {+ \infty} f (x) \mathrm{d} x \right| \leqslant \int_ {a} ^ {+ \infty} | f (x) | \mathrm{d} x. \tag {3}
$$

证 由 $\int_{a}^{+\infty}|f(x)|\mathrm{d}x$ 收敛，根据柯西准则（必要性），任给 $\varepsilon >0$ ，存在 $G\geqslant a$ ，当$u_{2} > u_{1} > G$ 时，总有

$$
\left| \int_ {u _ {1}} ^ {u _ {2}} | f (x) | \mathrm{d} x \right| = \int_ {u _ {1}} ^ {u _ {2}} | f (x) | \mathrm{d} x <   \varepsilon .
$$

利用定积分的绝对值不等式,又有

$$
\left| \int_ {u _ {1}} ^ {u _ {2}} f (x)   \mathrm{d} x \right| \leqslant \int_ {u _ {1}} ^ {u _ {2}} | f (x) |   \mathrm{d} x <   \varepsilon .
$$

再由柯西准则(充分性)，证得 $\int_{a}^{+\infty}f(x)\mathrm{d}x$ 收敛.

又因  $\left|\int_{a}^{u}f(x)\mathrm{d}x\right|\leqslant\int_{a}^{u}|f(x)|\mathrm{d}x(u>a)$ ，令  $u\to+\infty$  取极限，立刻得到不等式 (3).

当 $\int_{a}^{+\infty}|f(x)|\mathrm{d}x$ 收敛时，称 $\int_{a}^{+\infty}f(x)\mathrm{d}x$ 为绝对收敛.性质3指出:绝对收敛的无穷积分，它自身也一定收敛.但是它的逆命题一般不成立，今后将举例说明收敛的无穷积分不一定绝对收敛.

我们称收敛而不绝对收敛者为条件收敛.

## 二、非负函数无穷积分的敛散判别法

首先给出非负函数无穷积分的比较判别法.

设 $f$ 是定义在 $[a, +\infty)$ 上的非负函数，且在任何有限区间 $[a, u]$ 上可积。由于 $\int_{a}^{u} f(x) \mathrm{d}x$ 关于上限 $u$ 是单调递增的，因此 $\int_{a}^{+\infty} f(x) \mathrm{d}x$ 收敛的充要条件是 $\int_{a}^{u} f(x) \mathrm{d}x$ 在 $[a, +\infty)$ 上存在上界。根据这一分析，便立即导出下述比较判别法（请读者自己写出证明）。

定理11.2（比较原则）设定义在 $[a, +\infty)$ 上的两个非负函数 $f$ 和 $g$ 都在任何有限区间 $[a, u]$ 上可积，且满足

$$
f (x) \leqslant g (x), x \in [ a, + \infty),
$$

则当 $\int_{a}^{+\infty}g(x)\mathrm{d}x$ 收敛时， $\int_{a}^{+\infty}f(x)\mathrm{d}x$ 必收敛（或当 $\int_{a}^{+\infty}f(x)\mathrm{d}x$ 发散时， $\int_{a}^{+\infty}g(x)\mathrm{d}x$

253

---

第十一章 反常积分

必发散).

例 1 讨论 $\int_{0}^{+\infty}\frac{\sin x}{1+x^{2}}dx$ 的敛散性.

解 由于 $\left|\frac{\sin x}{1 + x^2}\right| \leqslant \frac{1}{1 + x^2}, x \in [0, +\infty)$, 以及 $\int_0^{+\infty} \frac{\mathrm{d}x}{1 + x^2} = \frac{\pi}{2}$ 收敛 (§ 1 例 4), 根据比较原则知 $\int_0^{+\infty} \frac{\sin x}{1 + x^2} \mathrm{d}x$ 绝对收敛.

上述比较原则的极限形式如下.

推论1 若 $f$ 和 $g$ 都在任何有限区间 $[a, u]$ 上可积，当 $x \in [a, +\infty)$ 时，$f(x) \geqslant 0$，$g(x) > 0$，且 $\lim_{x \to +\infty} \frac{f(x)}{g(x)} = c$，则有:

(i) 当 $0 < c < +\infty$ 时，$\int_{a}^{+\infty} f(x) \, \mathrm{d}x$ 与 $\int_{a}^{+\infty} g(x) \, \mathrm{d}x$ 同敛态；
(ii) 当 $c = 0$ 时，由 $\int_{a}^{+\infty} g(x) \, \mathrm{d}x$ 收敛可推知 $\int_{a}^{+\infty} f(x) \, \mathrm{d}x$ 也收敛；
(iii) 当 $c = +\infty$ 时, 由 $\int_{a}^{+\infty} g(x) \mathrm{d}x$ 发散可推知 $\int_{a}^{+\infty} f(x) \mathrm{d}x$ 也发散.

特别地,如果选用 $\int_{1}^{+\infty}\frac{dx}{x^{p}}$ 作为比较对象,则我们有如下两个推论(称为柯西判别法).

推论 2 设 f 定义于  $[a, +\infty) (a > 0)$ ，且在任何有限区间  $[a, u]$  上可积，则有:

(i) 当 $0 \leqslant f(x) \leqslant \frac{1}{x^p}, x \in [a, +\infty)$, 且 $p > 1$ 时, $\int_{a}^{+\infty} f(x) \, \mathrm{d}x$ 收敛;
(ii) 当 $f(x) \geqslant \frac{1}{x^p}, x \in [a, +\infty)$, 且 $p \leqslant 1$ 时, $\int_{a}^{+\infty} f(x) \mathrm{d}x$ 发散.

推论3 设 $f$ 是定义于 $[a, +\infty)$ 上的非负函数，在任何有限区间 $[a, u]$ 上可积，且

$$
\lim _ {x \to + \infty} x ^ {p} f (x) = \lambda .
$$

则有

(i) 当 $p > 1, 0 \leqslant \lambda < +\infty$ 时，$\int_{a}^{+\infty} f(x) \, \mathrm{d}x$ 收敛；
(ii) 当 $p \leqslant 1, 0 < \lambda \leqslant +\infty$ 时，$\int_{a}^{+\infty} f(x) \mathrm{d}x$ 发散.

例 2 讨论下列无穷限积分的敛散性:

1) $\int_{1}^{+\infty} x^{\alpha} \mathrm{e}^{-x} \, \mathrm{d}x$;

2) $\int_{0}^{+\infty}\frac{x^2}{\sqrt{x^5 + 1}}\mathrm{d}x.$

解 本例中两个被积函数都是非负的.

1）由于对任何实数 $\alpha$ ，都有

$$
\lim _ {x \to + \infty} x ^ {2} \cdot x ^ {\alpha} \mathrm{e} ^ {- x} = \lim _ {x \to + \infty} \frac {x ^ {\alpha + 2}}{\mathrm{e} ^ {x}} = 0,
$$

因此根据上述推论  $3(p=2,\lambda=0)$ ，推知 1) 对任何实数  $\alpha$  都是收敛的.

254

---

§ 2 无穷积分的性质与敛散判别

2）由于

$$
\lim _ {x \to + \infty} x ^ {\frac {1}{2}} \cdot \frac {x ^ {2}}{\sqrt {x ^ {5} + 1}} = 1,
$$

因此根据上述推论 $3\left(p = \frac{1}{2},\lambda = 1\right)$ ，推知2)是发散的.

对于 $\int_{-\infty}^{b}f(x)\mathrm{d}x$ 的比较判别亦可类似地进行.

## 三、一般无穷积分的敛散判别法

这里来介绍两个判别一般无穷积分敛散的判别法.

定理 11.3(狄利克雷判别法) 若  $F(u)=\int_{a}^{u}f(x)\mathrm{d}x$  在  $[a,+\infty)$  上有界,  $g(x)$  在  $[a,+\infty)$  上当  $x\to+\infty$  时单调趋于 0, 则  $\int_{a}^{+\infty}f(x)g(x)\mathrm{d}x$  收敛.

证 由条件设 $\left|\int_{a}^{u}f(x)\mathrm{d}x\right| \leqslant M, u \in [a, +\infty)$. 任给 $\varepsilon > 0$，由于 $\lim_{x \to +\infty} g(x) = 0$，因此存在 $G \geqslant a$，当 $x > G$ 时，有

$$
\mid g (x) \mid <   \frac {\varepsilon}{4 M}.
$$

又因 $g$ 为单调函数, 利用积分第二中值定理 (定理 9.11) 的推论, 对于任何 $u_{2} > u_{1} > G$, 存在 $\xi \in [u_{1}, u_{2}]$, 使得

$$
\int_ {u _ {1}} ^ {u _ {2}} f (x) g (x) \mathrm{d} x = g (u _ {1}) \int_ {u _ {1}} ^ {\xi} f (x) \mathrm{d} x + g (u _ {2}) \int_ {\xi} ^ {u _ {2}} f (x) \mathrm{d} x.
$$

于是有

$$
\begin{array}{l} \left| \int_ {u _ {1}} ^ {u _ {2}} f (x) g (x) \mathrm{d} x \right| \leqslant | g (u _ {1}) | \cdot \left| \int_ {u _ {1}} ^ {\xi} f (x) \mathrm{d} x \right| + | g (u _ {2}) | \cdot \left| \int_ {\xi} ^ {u _ {2}} f (x) \mathrm{d} x \right| \\ = \mid g (u _ {1}) \mid \cdot \left| \int_ {a} ^ {\xi} f (x)   \mathrm{d} x - \int_ {a} ^ {u _ {1}} f (x)   \mathrm{d} x \right| + \\ \mid g (u _ {2}) \mid \cdot \left| \int_ {a} ^ {u _ {2}} f (x)   \mathrm{d} x - \int_ {a} ^ {\xi} f (x)   \mathrm{d} x \right| \\ <   \frac {\varepsilon}{4 M} \cdot 2 M + \frac {\varepsilon}{4 M} \cdot 2 M = \varepsilon . \\ \end{array}
$$

根据柯西准则,证得  $\int_{a}^{+\infty}f(x)g(x)\mathrm{d}x$  收敛.

定理 11.4(阿贝尔(Abel)判别法) 若  $\int_{a}^{+\infty} f(x) dx$  收敛,  $g(x)$  在  $[a, +\infty)$  上单调有界, 则  $\int_{a}^{+\infty} f(x) g(x) dx$  收敛.

这定理同样可用积分第二中值定理来证明,但又可利用狄利克雷判别法更方便地获得证明(留作习题).

例3 讨论 $\int_{1}^{+\infty}\frac{\sin x}{x^p}\mathrm{d}x$ 与 $\int_{1}^{+\infty}\frac{\cos x}{x^p}\mathrm{d}x(p > 0)$ 的敛散性.

255

---

第十一章 反常积分

解 这里只讨论前一个无穷积分,后者有完全相同的结论.下面分两种情形来讨论:

(i) 当 $p > 1$ 时, $\int_{1}^{+\infty} \frac{\sin x}{x^p} \mathrm{d}x$ 绝对收敛. 这是因为

$$
\left| \frac {\sin x}{x ^ {p}} \right| \leqslant \frac {1}{x ^ {p}}, x \in [ 1, + \infty),
$$

而 $\int_{1}^{+\infty}\frac{\mathrm{d}x}{x^p}$ 当 $p > 1$ 时收敛，故由比较原则推知 $\int_{1}^{+\infty}\left|\frac{\sin x}{x^p}\right|\mathrm{d}x$ 收敛.

(ii) 当 $0 < p \leqslant 1$ 时, $\int_{1}^{+\infty} \frac{\sin x}{x^p} \mathrm{d}x$ 条件收敛. 这是因为对任意 $u \geqslant 1$, 有 $\left|\int_{1}^{u} \sin x \mathrm{d}x\right| = |\cos 1 - \cos u| \leqslant 2$, 而 $\frac{1}{x^p}$ 当 $p > 0$ 时单调趋于 $0 (x \to +\infty)$, 故由狄利克雷判别法推知 $\int_{1}^{+\infty} \frac{\sin x}{x^p} \mathrm{d}x$ 当 $p > 0$ 时总是收敛的.

另一方面,由于

$$
\left| \frac {\sin x}{x ^ {p}} \right| \geqslant \frac {\sin^ {2} x}{x} = \frac {1}{2 x} - \frac {\cos 2 x}{2 x}, x \in [ 1, + \infty),
$$

其中 $\int_{1}^{+\infty}\frac{\cos 2x}{2x}\mathrm{d}x = \frac{1}{2}\int_{2}^{+\infty}\frac{\cos t}{t}\mathrm{d}t$ 满足狄利克雷判别条件，是收敛的.而 $\int_{1}^{+\infty}\frac{\mathrm{d}x}{2x}$ 是发散的，因此当 $0 < p\leqslant 1$ 时该无穷积分不是绝对收敛的，所以它是条件收敛的. □

例 4 证明下列无穷积分都是条件收敛的:

$$
\int_ {1} ^ {+ \infty} \sin x ^ {2} \mathrm{d} x, \int_ {1} ^ {+ \infty} \cos x ^ {2} \mathrm{d} x, \int_ {1} ^ {+ \infty} x \sin x ^ {4} \mathrm{d} x.
$$

证 前两个无穷积分经换元 $t = x^2$ 得到

$$
\int_ {1} ^ {+ \infty} \sin x ^ {2} \mathrm{d} x = \int_ {1} ^ {+ \infty} \frac {\sin t}{2 \sqrt {t}} \mathrm{d} t,
$$

$$
\int_ {1} ^ {+ \infty} \cos x ^ {2} \mathrm{d} x = \int_ {1} ^ {+ \infty} \frac {\cos t}{2 \sqrt {t}} \mathrm{d} t.
$$

由例 3 知它们是条件收敛的.

对于第三个无穷积分,经换元  $t=x^{2}$  得

$$
\int_ {1} ^ {+ \infty} x \sin x ^ {4} \mathrm{d} x = \frac {1}{2} \int_ {1} ^ {+ \infty} \sin t ^ {2} \mathrm{d} t,
$$

它也是条件收敛的.

从例 4 中三个无穷积分的收敛性可以看到, 当  $x \to +\infty$  时被积函数即使不趋于零, 甚至是无界的, 无穷积分仍有可能收敛.

例5 若 $f(x)$ 在 $[a, +\infty)$ 上单调，且 $\int_{a}^{+\infty} f(x) \mathrm{d}x$ 收敛，则当 $x \to +\infty$ 时，$f(x)$ 趋于0.

证 如果 $f(x)$ 在 $[a, +\infty)$ 上单调递增，则或者 $\lim_{x \to +\infty} f(x) = +\infty$，或者存在实数 $A$ 使得 $\lim_{x \to +\infty} f(x) = A$.

256

---

§ 2 无穷积分的性质与敛散判别

（1）若 $\lim_{x\to +\infty}f(x) = +\infty$ ，则存在 $M > 0$ ，对任何 $x\geqslant M$ ，有 $f(x) > 1.$ 于是对任何 $u > M$ ，有

$$
\begin{array}{l} \int_ {a} ^ {u} f (x) \mathrm{d} x = \int_ {a} ^ {M} f (x) \mathrm{d} x + \int_ {M} ^ {u} f (x) \mathrm{d} x \\ \geqslant \int_ {a} ^ {M} f (x)   \mathrm{d} x + u - M \rightarrow + \infty (u \rightarrow + \infty), \\ \end{array}
$$

这与无穷积分 $\int_{a}^{+\infty}f(x)\mathrm{d}x$ 收敛相矛盾.

（2）若 $\lim_{x\to +\infty}f(x) = A$ 且 $A > 0$ ，则存在 $M > 0$ ，对任何 $x\geqslant M$ ，有 $f(x) > \frac{A}{2}$ .于是对任何 $u>$ $M$ ，有

$$
\begin{array}{l} \int_ {a} ^ {u} f (x) \mathrm{d} x = \int_ {a} ^ {M} f (x) \mathrm{d} x + \int_ {M} ^ {u} f (x) \mathrm{d} x \\ \geqslant \int_ {a} ^ {M} f (x) \mathrm{d} x + (u - M) \cdot \frac {A}{2} \rightarrow + \infty (u \rightarrow + \infty), \\ \end{array}
$$

这与无穷积分 $\int_{a}^{+\infty}f(x)\mathrm{d}x$ 收敛相矛盾.若 $A < 0$ ，类似地也会得到这样的矛盾

因此  $\lim_{x\to+\infty}f(x)=0.$

当 $f(x)$ 在 $[a,+\infty)$ 上单调递减时,类似可证.

![](../../raw/pages_0257-0288/images/page_267_image_9.jpg)

## 习题 11.2

1. 证明定理 11.2 及其推论 1.

2. 设 $f$ 与 $g$ 是定义在 $[a, +\infty)$ 上的函数，对任何 $u > a$ ，它们在 $[a, u]$ 上都可积。证明:若 $\int_{a}^{+\infty} f^{2}(x) \mathrm{d}x$ 与 $\int_{a}^{+\infty} g^{2}(x) \mathrm{d}x$ 收敛，则 $\int_{a}^{+\infty} f(x) g(x) \mathrm{d}x$ 与 $\int_{a}^{+\infty} [f(x) + g(x)]^{2} \mathrm{d}x$ 也都收敛。

3. 设 $f, g, h$ 是定义在 $[a, +\infty)$ 上的三个连续函数，且成立不等式 $h(x) \leqslant f(x) \leqslant g(x)$. 证明:

(1) 若  $\int_{a}^{+\infty} h(x) \, dx$  与  $\int_{a}^{+\infty} g(x) \, dx$  都收敛，则  $\int_{a}^{+\infty} f(x) \, dx$  也收敛；
(2) 又若  $\int_{a}^{+\infty} h(x) \, dx = \int_{a}^{+\infty} g(x) \, dx = A$ ，则  $\int_{a}^{+\infty} f(x) \, dx = A$ .

4. 讨论下列无穷积分的敛散性:

(1) $\int_{0}^{+\infty}\frac{\mathrm{d}x}{\sqrt[3]{x^4 + 1}};$

(2) $\int_{1}^{+\infty}\frac{x}{1 - \mathrm{e}^x}\mathrm{d}x;$

(3) $\int_{0}^{+\infty}\frac{\mathrm{d}x}{1 + \sqrt{x}};$

(4) $\int_{1}^{+\infty}\frac{x\arctan x}{1 + x^3}\mathrm{d}x;$

(5) $\int_{1}^{+\infty}\frac{\ln(1 + x)}{x^n}\mathrm{d}x;$

(6) $\int_{0}^{+\infty}\frac{x^m}{1 + x^n}\mathrm{d}x(n,m\geqslant 0)$.

5. 讨论下列无穷积分为绝对收敛还是条件收敛:

(1) $\int_{1}^{+\infty}\frac{\sin\sqrt{x}}{x}\mathrm{d}x;$

(2) $\int_{0}^{+\infty}\frac{\operatorname{sgn}(\sin x)}{1 + x^2}\mathrm{d}x;$

(3) $\int_{0}^{+\infty}\frac{\sqrt{x}\cos x}{100 + x}\mathrm{d}x;$

(4) $\int_{\mathrm{e}}^{+\infty}\frac{\ln(\ln x)}{\ln x}\sin x\mathrm{d}x.$

257

---

第十一章 反常积分

6. 举例说明:$\int_{a}^{+\infty} f(x) \, \mathrm{d}x$ 收敛时，$\int_{a}^{+\infty} f^2(x) \, \mathrm{d}x$ 不一定收敛；$\int_{a}^{+\infty} f(x) \, \mathrm{d}x$ 绝对收敛时，$\int_{a}^{+\infty} f^2(x) \, \mathrm{d}x$ 也不一定收敛.

7. 证明: 若 $\int_{a}^{+\infty} f(x) \, \mathrm{d}x$ 绝对收敛, 且 $\lim_{x \to +\infty} f(x) = 0$, 则 $\int_{a}^{+\infty} f^2(x) \, \mathrm{d}x$ 必定收敛.

8. 证明: 若 $f$ 是 $[a, +\infty)$ 上的单调函数, 且 $\int_{a}^{+\infty} f(x) \mathrm{d}x$ 收敛, 则 $f(x) = o\left(\frac{1}{x}\right), x \to +\infty$.

9. 证明: 若 $f$ 在 $[a, +\infty)$ 上一致连续, 且 $\int_{a}^{+\infty} f(x) \mathrm{d}x$ 收敛, 则 $\lim_{x \to +\infty} f(x) = 0$.

10. 利用狄利克雷判别法证明阿贝尔判别法.

## § 3 瑕积分的性质与敛散判别

类似于无穷积分的柯西收敛准则以及其后的三个性质,瑕积分同样可由函数极限
 $\lim_{u\to a^{+}}\int_{u}^{b}f(x)\mathrm{d}x=\int_{a}^{b}f(x)\mathrm{d}x$  的原意写出相应的命题.

定理11.5 瑕积分 $\int_{a}^{b} f(x) \, \mathrm{d}x$ (瑕点为 $a$) 收敛的充要条件是: 任给 $\varepsilon > 0$, 存在 $\delta > 0$, 只要 $u_{1}, u_{2} \in (a, a + \delta)$, 总有

$$
\left| \int_ {u _ {1}} ^ {b} f (x) \mathrm{d} x - \int_ {u _ {2}} ^ {b} f (x) \mathrm{d} x \right| = \left| \int_ {u _ {1}} ^ {u _ {2}} f (x) \mathrm{d} x \right| <   \varepsilon .
$$

性质1 设函数 $f_{1}$ 与 $f_{2}$ 的瑕点同为 $x = a, k_{1}, k_{2}$ 为常数，则当瑕积分 $\int_{a}^{b} f_{1}(x) \mathrm{d}x$ 与 $\int_{a}^{b} f_{2}(x) \mathrm{d}x$ 都收敛时，瑕积分 $\int_{a}^{b} [k_{1} f_{1}(x) + k_{2} f_{2}(x)] \mathrm{d}x$ 必定收敛，并有

$$
\int_ {a} ^ {b} \left[ k _ {1} f _ {1} (x) + k _ {2} f _ {2} (x) \right] \mathrm{d} x = k _ {1} \int_ {a} ^ {b} f _ {1} (x) \mathrm{d} x + k _ {2} \int_ {a} ^ {b} f _ {2} (x) \mathrm{d} x. \tag {1}
$$

性质2 设函数 $f$ 的瑕点为 $x = a, c \in (a, b)$ 为任一常数. 则瑕积分 $\int_{a}^{b} f(x) \mathrm{d}x$ 与 $\int_{a}^{c} f(x) \mathrm{d}x$ 同敛态，并有

$$
\int_ {a} ^ {b} f (x) \mathrm{d} x = \int_ {a} ^ {c} f (x) \mathrm{d} x + \int_ {c} ^ {b} f (x) \mathrm{d} x, \tag {2}
$$

其中 $\int_{c}^{b}f(x)\mathrm{d}x$ 为定积分.

性质3 设函数 $f$ 的瑕点为 $x = a, f$ 在 $(a, b]$ 的任一内闭区间 $[u, b]$ 上可积. 则当 $\int_{a}^{b} |f(x)| \mathrm{d}x$ 收敛时, $\int_{a}^{b} f(x) \mathrm{d}x$ 也必定收敛, 并有

$$
\left| \int_ {a} ^ {b} f (x) \mathrm{d} x \right| \leqslant \int_ {a} ^ {b} | f (x) | \mathrm{d} x. \tag {3}
$$

同样地，当 $\int_{a}^{b}|f(x)|\mathrm{d}x$ 收敛时，称 $\int_{a}^{b}f(x)\mathrm{d}x$ 为绝对收敛.又称收敛而不绝对收敛的瑕积分是条件收敛的.

258

---

§ 3 瑕积分的性质与敛散判别

判别非负函数瑕积分收敛的比较原则及其推论如下:

定理11.6（比较原则）设定义在 $(a,b]$ 上的两个函数 $f$ 与 $g$ ，瑕点同为 $x = a$ ，在任何 $[u,b] \subset (a,b]$ 上都可积，且满足

$$
0 \leqslant f (x) \leqslant g (x), x \in (a, b ].
$$

则当 $\int_{a}^{b}g(x)\mathrm{d}x$ 收敛时， $\int_{a}^{b}f(x)\mathrm{d}x$ 必定收敛（或者，当 $\int_{a}^{b}f(x)\mathrm{d}x$ 发散时， $\int_{a}^{b}g(x)\mathrm{d}x$ 亦必发散）.

推论1 又若 $f(x) \geqslant 0, g(x) > 0$，且 $\lim_{x \to a^+} \frac{f(x)}{g(x)} = c$，则有:

(i) 当 $0 < c < +\infty$ 时，$\int_{a}^{b} f(x) \, \mathrm{d}x$ 与 $\int_{a}^{b} g(x) \, \mathrm{d}x$ 同敛态；
(ii) 当 $c = 0$ 时，由 $\int_{a}^{b} g(x) \, \mathrm{d}x$ 收敛可推知 $\int_{a}^{b} f(x) \, \mathrm{d}x$ 也收敛；
(iii) 当 $c = +\infty$ 时, 由 $\int_{a}^{b} g(x) \mathrm{d}x$ 发散可推知 $\int_{a}^{b} f(x) \mathrm{d}x$ 也发散.

特别地,如果选用 $\int_{a}^{b}\frac{dx}{(x-a)^{p}}$ 作为比较对象,则我们有如下两个推论(称为柯西判别法).

推论2 设 $f$ 定义在 $(a, b]$ 上，$a$ 为其瑕点，且在任何 $[u, b] \subset (a, b]$ 上可积，则有:

(i) 当 $0 \leqslant f(x) \leqslant \frac{1}{(x - a)^p}$, 且 $0 < p < 1$ 时, $\int_{a}^{b} f(x) \mathrm{d}x$ 收敛;
(ii) 当 $f(x) \geqslant \frac{1}{(x - a)^p}$，且 $p \geqslant 1$ 时，$\int_{a}^{b} f(x) \, \mathrm{d}x$ 发散.

推论3 设 $f$ 是定义在 $(a, b]$ 上的非负函数, $a$ 为其瑕点, 且在任何 $[u, b] \subset (a, b]$ 上可积. 如果

$$
\lim _ {x \to a ^ {+}} (x - a) ^ {p} f (x) = \lambda ,
$$

则有:

(i) 当 $0 < p < 1, 0 \leqslant \lambda < +\infty$ 时，$\int_{a}^{b} f(x) \, \mathrm{d}x$ 收敛；
(ii) 当  $p \geqslant 1, 0 < \lambda \leqslant +\infty$  时， $\int_{a}^{b} f(x) \, dx$  发散.

对于一般瑕积分,也有相应的狄利克雷判别法和阿贝尔判别法.

定理11.7（狄利克雷判别法）设 $a$ 为 $f(x)$ 的瑕点，函数 $F(u) = \int_{u}^{b} f(x) \, \mathrm{d}x$ 在 $(a, b]$ 上有界，函数 $g(x)$ 在 $(a, b]$ 上单调且 $\lim_{x \to a^+} g(x) = 0$，则瑕积分 $\int_{a}^{b} f(x) g(x) \, \mathrm{d}x$ 收敛.

定理 11.8(阿贝尔判别法) 设 a 为  $f(x)$  的瑕点, 瑕积分  $\int_{a}^{b} f(x) \, dx$  收敛, 函数  $g(x)$  在  $(a, b]$  上单调且有界, 则瑕积分  $\int_{a}^{b} f(x) g(x) \, dx$  收敛.

例 1 判别下列瑕积分的敛散性:

259

---

第十一章 反常积分

1) $\int_0^1\frac{\ln x}{\sqrt{x}}\mathrm{d}x;$

2) $\int_{1}^{2}\frac{\sqrt{x}}{\ln x}\mathrm{d}x.$

解 本例两个瑕积分的被积函数在各自的积分区间上分别保持同号—— $\frac{\ln x}{\sqrt{x}}$ 在 $(0,1]$ 上恒为负， $\frac{\sqrt{x}}{\ln x}$ 在 $(1,2]$ 上恒为正——所以它们的瑕积分收敛与绝对收敛是同一回事.

1）此瑕积分的瑕点为 $x = 0$ .由上述推论3，当取 $p = \frac{3}{4} < 1$ 时，有

$$
\lambda = \lim _ {x \to 0 ^ {+}} x ^ {\frac {3}{4}} \cdot \left| \frac {\ln x}{\sqrt {x}} \right| = - \lim _ {x \to 0 ^ {+}} \frac {\ln x}{x ^ {- \frac {1}{4}}} = \lim _ {x \to 0 ^ {+}} (4 x ^ {\frac {1}{4}}) = 0,
$$

所以瑕积分 1) 收敛.

2）此瑕积分的瑕点为 $x = 1$ .当取 $p = 1$ 时，由

$$
\lambda = \lim _ {x \to 1 ^ {+}} (x - 1) \cdot \frac {\sqrt {x}}{\ln x} = \lim _ {x \to 1 ^ {+}} \frac {x - 1}{\ln x} = 1,
$$

推知该瑕积分发散.

最后举一个既是无穷积分又是瑕积分的例子.

例 2 讨论反常积分

$$
\Phi (\alpha) = \int_ {0} ^ {+ \infty} \frac {x ^ {\alpha - 1}}{1 + x} \mathrm{d} x
$$

的收敛性.

解 把反常积分  $\Phi(\alpha)$  写成

$$
\Phi (\alpha) = \int_ {0} ^ {1} \frac {x ^ {\alpha - 1}}{1 + x} \mathrm{d} x + \int_ {1} ^ {+ \infty} \frac {x ^ {\alpha - 1}}{1 + x} \mathrm{d} x = I (\alpha) + J (\alpha).
$$

(i) 先讨论 $I(\alpha)$. 当 $\alpha - 1 \geqslant 0$, 即 $\alpha \geqslant 1$ 时它是定积分; 当 $\alpha < 1$ 时它是瑕积分, 瑕点为 $x = 0$. 由于

$$
\lim _ {x \to 0 ^ {+}} x ^ {1 - \alpha} \cdot \frac {x ^ {\alpha - 1}}{1 + x} = 1,
$$

根据定理11.6推论3，当 $0 < p = 1 - \alpha < 1$ ，即 $\alpha > 0$ 且 $\lambda = 1$ 时，瑕积分 $I(\alpha)$ 收敛；当 $p = 1 - \alpha \geqslant 1$ ，即 $\alpha \leqslant 0$ 且 $\lambda = 1$ 时，$I(\alpha)$ 发散.

(ii) 再讨论  $J(\alpha)$ ，它是无穷积分。由于

$$
\lim _ {x \to + \infty} x ^ {2 - \alpha} \cdot \frac {x ^ {\alpha - 1}}{1 + x} = \lim _ {x \to + \infty} \frac {x}{1 + x} = 1,
$$

根据定理11.2推论3，当 $p = 2 - \alpha > 1$ ，即 $\alpha < 1$ 且 $\lambda = 1$ 时，$J(\alpha)$ 收敛；而当 $p = 2 - \alpha \leqslant 1$ ，即 $\alpha \geqslant 1$ 且 $\lambda = 1$ 时，$J(\alpha)$ 发散.

综上所述,把讨论结果列如下表:

| $\alpha$ | $\alpha \leqslant 0$ | $0 < \alpha < 1$ | $\alpha \geqslant 1$ |
| --- | --- | --- | --- |
| $I(\alpha)$ | 发散 | 收敛 | 定积分 |

260

---

第十一章总练习题

续表

| $\alpha$ | $\alpha \leqslant 0$ | $0 < \alpha < 1$ | $\alpha \geqslant 1$ |
| --- | --- | --- | --- |
| $J(\alpha)$ | 收敛 | 收敛 | 发散 |
| $\Phi(\alpha)$ | 发散 | 收敛 | 发散 |

由此可见,反常积分  $\Phi(\alpha)$  只有当  $0<\alpha<1$  时才是收敛的.

## 习题 11.3

1. 写出性质 3 的证明.
2. 写出定理 11.6 及其推论 1 的证明.
3. 讨论下列瑕积分的敛散性:

(1) $\int_0^2\frac{\mathrm{d}x}{(x - 1)^2};$
(2) $\int_{0}^{\pi}\frac{\sin x}{x^{3 / 2}}\mathrm{d}x;$
(3) $\int_{0}^{1}\frac{\mathrm{d}x}{\sqrt{x}\ln x};$
(4) $\int_{0}^{1}\frac{\ln x}{1 - x}\mathrm{d}x;$
(5) $\int_0^1\frac{\arctan x}{1 - x^3}\mathrm{d}x;$
(6) $\int_{0}^{\pi /2}\frac{1 - \cos x}{x^m}\mathrm{d}x;$
(7) $\int_{0}^{1}\frac{1}{x^{\alpha}}\sin \frac{1}{x}\mathrm{d}x;$
(8) $\int_{0}^{+\infty}\mathrm{e}^{-x}\ln x\mathrm{d}x.$

4. 计算下列瑕积分的值（其中 $n$ 为正整数）:

(1)  $\int_{0}^{1}(\ln x)^{n}\mathrm{d}x;$

(2) $\int_{0}^{1}\frac{x^n}{\sqrt{1 - x}}\mathrm{d}x.$

5. 证明瑕积分 $J = \int_{0}^{\pi /2}\ln (\sin x)\mathrm{d}x$ 收敛，且 $J = -\frac{\pi}{2}\ln 2$. (提示:利用 $\int_0^{\pi /2}\ln (\sin x)\mathrm{d}x = \int_{0}^{\pi /2}\ln (\cos x)\mathrm{d}x$，并将它们相加.)
6. 利用上题结果, 证明:

(1) $\int_{0}^{\pi}\theta \ln (\sin \theta)\mathrm{d}\theta = -\frac{\pi^2}{2}\ln 2;$
(2) $\int_{0}^{\pi}\frac{\theta\sin\theta}{1 - \cos\theta}\mathrm{d}\theta = 2\pi \ln 2.$

7. 写出定理 11.7 和 11.8 的证明.

## 第十一章总练习题

1. 证明下列等式:

(1) $\int_{0}^{1}\frac{x^{p - 1}}{x + 1}\mathrm{d}x = \int_{1}^{+\infty}\frac{x^{-p}}{x + 1}\mathrm{d}x,p > 0;$
(2) $\int_{0}^{+\infty}\frac{x^{p - 1}}{x + 1}\mathrm{d}x = \int_{0}^{+\infty}\frac{x^{-p}}{x + 1}\mathrm{d}x,0 < p < 1.$

261

---

第十一章 反常积分

2. 证明下列不等式:

(1) $\frac{\pi}{2\sqrt{2}} < \int_{0}^{1}\frac{\mathrm{d}x}{\sqrt{1 - x^4}} < \frac{\pi}{2};$
(2) $\frac{1}{2}\left(1 - \frac{1}{\mathrm{e}}\right) < \int_{0}^{+\infty}\mathrm{e}^{-x^2}\mathrm{d}x < 1 + \frac{1}{2\mathrm{e}}.$

3. 计算下列反常积分的值:

(1) $\int_{0}^{+\infty}\mathrm{e}^{-ax}\cos bx\mathrm{d}x(a > 0);$

(2) $\int_{0}^{+\infty}\mathrm{e}^{-ax}\sin bx\mathrm{d}x(a > 0);$

(3) $\int_{0}^{+\infty}\frac{\ln x}{1 + x^2}\mathrm{d}x;$

(4) $\int_{0}^{\pi /2}\ln (\tan \theta)\mathrm{d}\theta .$

4. 讨论反常积分 $\int_{0}^{+\infty}\frac{\sin bx}{x^{\lambda}}\mathrm{d}x (b\neq 0),\lambda$ 取何值时绝对收敛或条件收敛.

5. 证明: 设 $f$ 在 $[0, +\infty)$ 上连续, $0 < a < b$.

(1) 若  $\lim_{x\to+\infty}f(x)=k$  , 则

$$
\int_ {0} ^ {+ \infty} \frac {f (a x) - f (b x)}{x} \mathrm{d} x = [ f (0) - k ] \ln \frac {b}{a};
$$

(2) 若  $\int_{a}^{+\infty}\frac{f(x)}{x}dx$  收敛, 则

$$
\int_ {0} ^ {+ \infty} \frac {f (a x) - f (b x)}{x} \mathrm{d} x = f (0) \ln \frac {b}{a}.
$$

6. 证明下述命题:

（1）设 $f$ 为 $[a, +\infty)$ 上的非负连续函数. 若 $\int_{a}^{+\infty} x f(x) \mathrm{d}x$ 收敛，则 $\int_{a}^{+\infty} f(x) \mathrm{d}x$ 也收敛.
（2）设 $f$ 为 $[a, +\infty)$ 上的连续可微函数，且当 $x \to +\infty$ 时，$f(x)$ 递减地趋于0，则 $\int_{a}^{+\infty} f(x) \mathrm{d}x$ 收敛的充要条件为 $\int_{a}^{+\infty} x f'(x) \mathrm{d}x$ 收敛.

7. 设 $f(x)$ 在 $[1, +\infty)$ 上二阶连续可微，对于任何 $x \in [1, +\infty)$ 有 $f(x) > 0$，且 $\lim_{x \to +\infty} f''(x) = +\infty$. 证明:无穷积分 $\int_{1}^{+\infty} \frac{1}{f(x)} \mathrm{d}x$ 收敛.

![](../../raw/pages_0257-0288/images/page_272_image_21.jpg)

## 第十一章综合自测题

262
