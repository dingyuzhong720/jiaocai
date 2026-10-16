积为

$$
A = \int_ {\alpha} ^ {\beta} \frac {1}{2} [ \rho (\theta) ] ^ {2} \mathrm{d} \theta .
$$

例 4 计算阿基米德螺线

$$
\rho = a \theta \quad (a > 0)
$$

上相应于  $\theta$  从 0 变到  $2\pi$  的一段弧与极轴所围成的图形(图 6-6)的面积.

解 在指定的这段螺线上, $\theta$ 的变化区间为 $[0,2\pi]$ .相应于 $[0,2\pi]$ 上任一小区间 $[\theta,\theta+d\theta]$ 的窄曲边扇形的面积近似于半径为 $a\theta$ 、圆心角为 $d\theta$ 的扇形的面积,从而得到面积元素

$$
\mathrm{d} A = \frac {1}{2} (a \theta) ^ {2} \mathrm{d} \theta.
$$

于是所求面积为

$$
A = \int_ {0} ^ {2 \pi} \frac {a ^ {2}}{2} \theta^ {2} \mathrm{d} \theta = \frac {a ^ {2}}{2} \left[ \frac {\theta^ {3}}{3} \right] _ {0} ^ {2 \pi} = \frac {4}{3} a ^ {2} \pi^ {3}.
$$

![](images/page_288_image_10.jpg)

<details>
<summary>text_image</summary>

θ
dθ
O
2πa
A
ρ=aθ
</details>

图6-6

例5 计算心形线

$$
\rho = a (1 + \cos \theta) \quad (a > 0)
$$

所围成的图形的面积.

解 心形线所围成的图形如图 6-7 所示. 这个图形对称于极轴, 因此所求图形的面积 A 是极轴以上部分图形面积  $A_{1}$  的 2 倍.

对于极轴以上部分的图形, $\theta$ 的变化区间为 $[0,\pi]$ .相应于 $[0,\pi]$ 上任一小区间 $[\theta,\theta+d\theta]$ 的窄曲边扇形的面积近似于半径为 $a(1+\cos\theta)$ 、圆心角为 $d\theta$ 的扇形的面积.从而得到面积元素

$$
\mathrm{d} A = \frac {1}{2} a ^ {2} (1 + \cos \theta) ^ {2} \mathrm{d} \theta ,
$$

![](images/page_288_image_18.jpg)

<details>
<summary>text_image</summary>

ρ=a(1+cos θ)
dθ
θ
O
2a A
</details>

图6-7

于是

例题精讲

6-1

图

释疑解难

6-1

$$
\begin{array}{l} A _ {1} = \int_ {0} ^ {\pi} \frac {1}{2} a ^ {2} (1 + \cos \theta) ^ {2} \mathrm{d} \theta = \frac {a ^ {2}}{2} \int_ {0} ^ {\pi} (1 + 2 \cos \theta + \cos^ {2} \theta) \mathrm{d} \theta \\ = \frac {a ^ {2}}{2} \int_ {0} ^ {\pi} \left(\frac {3}{2} + 2 \cos \theta + \frac {1}{2} \cos 2 \theta\right) \mathrm{d} \theta \\ = \frac {a ^ {2}}{2} \left[ \frac {3}{2} \theta + 2 \sin \theta + \frac {1}{4} \sin 2 \theta \right] _ {0} ^ {\pi} = \frac {3}{4} \pi a ^ {2}, \\ \end{array}
$$

因而所求面积为

$$
A = 2 A _ {1} = \frac {3}{2} \pi a ^ {2}.
$$

## 二、体积

## 1. 旋转体的体积

旋转体就是由一个平面图形绕这平面内一条直线旋转一周而成的立体.这直线叫做旋转轴.圆柱、圆锥、圆台、球可以分别看成是由矩形绕它的一条边、直角三角形绕它的直角边、直角梯形绕它的直角腰、半圆绕它的直径旋转一周而成的立体,所以它们都是旋转体.

上述旋转体都可以看作是由连续曲线  $y=f(x)$ ，直线 x=a, x=b 及 x 轴所围成的曲边梯形绕 x 轴旋转一周而成的立体。现在我们考虑用定积分来计算这种旋转体的体积。

取横坐标 x 为积分变量, 它的变化区间为  $[a, b]$ . 相应于  $[a, b]$  上的任一小区间  $[x, x + dx]$  的窄曲边梯形绕 x 轴旋转而成的薄片的体积近似于以  $f(x)$  为底半径、dx 为高的扁圆柱体的体积(图 6-8), 即体积元素

$$
\mathrm{d} V = \pi [ f (x) ] ^ {2} \mathrm{d} x.
$$

以  $\pi[f(x)]^{2}\mathrm{d}x$  为被积表达式, 在闭区间  $[a,b]$  上作定积分, 便得所求旋转体体积为

![](images/page_289_image_9.jpg)

<details>
<summary>text_image</summary>

y
y=f(x)
O
a
x
x+dx
b
x
</details>

图6-8

$$
V = \int_ {a} ^ {b} \pi [ f (x) ] ^ {2} \mathrm{d} x.
$$

例6 连接坐标原点 $O$ 及点 $P(h, r)$ 的直线、直线 $x = h$ 及 $x$ 轴围成一个直角三角形（图6-9). 将它绕 $x$ 轴旋转一周构成一个底半径为 $r$ 、高为 $h$ 的圆锥体. 计算这圆锥体的体积.

解 过原点 O 及点  $P(h,r)$  的直线方程为

$$
y = \frac {r}{h} x.
$$

取横坐标 x 为积分变量, 它的变化区间为  $[0, h]$ . 圆锥体中相应于  $[0, h]$  上任一小区间  $[x, x + dx]$  的薄片的体积近似于底半径为  $\frac{r}{h}x$ 、高为 dx 的扁圆柱体的体积, 即体积元素

![](images/page_289_image_16.jpg)

<details>
<summary>text_image</summary>

y
P(h,r)
r
O
x
x+αx
h
x
</details>

图6-9

$$
\mathrm{d} V = \pi \left[ \frac {r}{h} x \right] ^ {2} \mathrm{d} x.
$$

于是所求圆锥体的体积为

$$
V = \int_ {0} ^ {h} \pi \left(\frac {r}{h} x\right) ^ {2} \mathrm{d} x = \frac {\pi r ^ {2}}{h ^ {2}} \left[ \frac {x ^ {3}}{3} \right] _ {0} ^ {h} = \frac {\pi r ^ {2} h}{3}.
$$

例7 计算由椭圆

$$
\frac {x ^ {2}}{a ^ {2}} + \frac {y ^ {2}}{b ^ {2}} = 1
$$

所围成的图形绕 x 轴旋转一周而成的旋转体(叫做旋转椭球体)的体积.

解 这个旋转椭球体也可以看作是由半个椭圆

$$
y = \frac {b}{a} \sqrt {a ^ {2} - x ^ {2}}
$$

及 x 轴围成的图形绕 x 轴旋转一周而成的立体.

取 $x$ 为积分变量, 它的变化区间为 $[-a, a]$. 旋转椭球体中相应于 $[-a, a]$ 上任一小区间 $[x, x + \mathrm{d}x]$ 的薄片的体积, 近似于底半径为 $\frac{b}{a} \sqrt{a^2 - x^2}$, 高为 $\mathrm{d}x$ 的扁圆柱体的体积

(图 6-10), 即体积元素

$$
\mathrm{d} V = \frac {\pi b ^ {2}}{a ^ {2}} (a ^ {2} - x ^ {2}) \mathrm{d} x.
$$

于是所求旋转椭球体的体积为

$$
\begin{array}{l} V = \int_ {- a} ^ {a} \pi \frac {b ^ {2}}{a ^ {2}} (a ^ {2} - x ^ {2}) \mathrm{d} x = \frac {2 \pi b ^ {2}}{a ^ {2}} \int_ {0} ^ {a} (a ^ {2} - x ^ {2}) \mathrm{d} x \\ = 2 \pi \frac {b ^ {2}}{a ^ {2}} \left[ a ^ {2} x - \frac {x ^ {3}}{3} \right] _ {0} ^ {a} = \frac {4}{3} \pi a b ^ {2}. \\ \end{array}
$$

![](images/page_290_image_15.jpg)

<details>
<summary>text_image</summary>

y
b
O
x
a
x
x+dx
</details>

图6-10

当 a=b 时,旋转椭球体就成为半径为 a 的球,它的体积为  $\frac{4}{3}\pi a^{3}$ .

用与上面类似的方法可以推出:由曲线  $x=\varphi(y)$ ，直线 y=c, y=d (c<d) 与 y 轴所围成的曲边梯形，绕 y 轴旋转一周而成的旋转体(图 6-11) 的体积为

$$
V = \pi \int_ {c} ^ {d} [ \varphi (y) ] ^ {2} \mathrm{d} y,
$$

例8 计算由摆线 $x = a(t - \sin t), y = a(1 - \cos t)$ 相应于 $0 \leqslant t \leqslant 2\pi$ 的一拱与直线 $y = 0$ 所围成的图形分别绕 $x$ 轴、$y$ 轴旋转而成的旋转体的体积.

解 按旋转体的体积公式,所述图形绕 x 轴旋转而成的旋转体的体积为

$$
V _ {x} = \int_ {0} ^ {2 \pi a} \pi y ^ {2} (x) \mathrm{d} x = \pi \int_ {0} ^ {2 \pi} a ^ {2} (1 - \cos t) ^ {2} \cdot a (1 - \cos t) \mathrm{d} t
$$

$$
= \pi a ^ {3} \int_ {0} ^ {2 \pi} (1 - 3 \cos t + 3 \cos^ {2} t - \cos^ {3} t) \mathrm{d} t = 5 \pi^ {2} a ^ {3}.
$$

所述图形绕 $y$ 轴旋转而成的旋转体的体积可看成平面图形OABC与OBC（图6-12)分别绕 $y$ 轴旋转而成的旋转体的体积之差.因此所求的体积为

$$
\begin{array}{l} V _ {y} = \int_ {0} ^ {2 a} \pi x _ {2} ^ {2} (y) \mathrm{d} y - \int_ {0} ^ {2 a} \pi x _ {1} ^ {2} (y) \mathrm{d} y \\ = \pi \int_ {2 \pi} ^ {\pi} a ^ {2} (t - \sin t) ^ {2} \cdot a \sin t \mathrm{d} t - \pi \int_ {0} ^ {\pi} a ^ {2} (t - \sin t) ^ {2} \cdot a \sin t \mathrm{d} t \\ = - \pi a ^ {3} \int_ {0} ^ {2 \pi} (t - \sin t) ^ {2} \sin t \mathrm{d} t = 6 \pi^ {3} a ^ {3}. \\ \end{array}
$$

![](images/page_291_image_4.jpg)

<details>
<summary>text_image</summary>

y
d
x=φ(y)
c
O
x
</details>

图6-11

![](images/page_291_chart_6.jpg)

<details>
<summary>contour</summary>

| Point | Description |
| --- | --- |
| C | Intersection of x=x1(y) and x=x2(y) at (2a, 2a) |
| B | Intersection of x=x1(y) and x=x2(y) at \((\pi a, 2a)\) |
| A | Intersection of x=x2(y) and x=x1(y) at \(2\pi a\) |
</details>

图6-12

## 2. 平行截面面积为已知的立体的体积

从计算旋转体体积的过程中可以看出:如果一个立体不是旋转体,但却知道该立体上垂直于一定轴的各个截面的面积,那么,这个立体的体积也可以用定积分来计算.

如图6-13所示,取上述定轴为 $x$ 轴,并设该立体在过点 $x = a, x = b$ 且垂直于 $x$ 轴的两个平面之间.以 $A(x)$ 表示过点 $x$ 且垂直于 $x$ 轴的截面面积.假定 $A(x)$ 为已知的 $x$ 的连续函数.这时,取 $x$ 为积分变量,它的变化区间为 $[a, b]$;立体中相应于 $[a, b]$ 上任一小区间 $[x, x + \mathrm{d}x]$ 的一薄片的体积,近似于底面积为 $A(x)$、高为 $\mathrm{d}x$ 的扁柱体的体积,即体积元素

$$
\mathrm{d} V = A (x) \mathrm{d} x.
$$

以 $A(x)\mathrm{d}x$ 为被积表达式，在闭区间 $[a,b]$ 上作定积分，便得所求立体的体积

$$
V = \int_ {a} ^ {b} A (x)   \mathrm{d} x.
$$

例9 一平面经过半径为 $R$ 的圆柱体的底圆中心, 并与底面交成角 $\alpha$ (图6-14). 计算这平面截圆柱体所得立体的体积.

![](images/page_292_image_1.jpg)

<details>
<summary>text_image</summary>

A(x)
O a x x+dx b x
</details>

图6-13

![](images/page_292_image_3.jpg)

<details>
<summary>text_image</summary>

-R
O
α
x
R
α
y
x²+y²=R²
y
</details>

图6-14

解 取这平面与圆柱体的底面的交线为 $x$ 轴, 底面上过圆中心、且垂直于 $x$ 轴的直线为 $y$ 轴. 那么, 底圆的方程为 $x^{2} + y^{2} = R^{2}$. 立体中过 $x$ 轴上的点 $x$ 且垂直于 $x$ 轴的截面是一个直角三角形. 它的两条直角边的长分别为 $y$ 及 $y \tan \alpha$, 即 $\sqrt{R^{2} - x^{2}}$ 及 $\sqrt{R^{2} - x^{2}} \tan \alpha$. 因而截面积为 $A(x) = \frac{1}{2}(R^{2} - x^{2}) \tan \alpha$, 于是所求立体体积为

$$
\begin{array}{l} V = \int_ {- R} ^ {R} \frac {1}{2} (R ^ {2} - x ^ {2}) \tan \alpha \mathrm{d} x = \int_ {0} ^ {R} (R ^ {2} - x ^ {2}) \tan \alpha \mathrm{d} x \\ = \tan \alpha \left[ R ^ {2} x - \frac {1}{3} x ^ {3} \right] _ {0} ^ {R} = \frac {2}{3} R ^ {3} \tan \alpha . \\ \end{array}
$$

例 10 求以半径为 R 的圆为底、平行且等于底圆直径的线段为顶、高为 h 的正劈锥体的体积.

解 取底圆所在的平面为 $xOy$ 平面, 圆心 $O$ 为原点, 并使 $x$ 轴与正劈锥的顶平行 (图 6-15). 底圆的方程为 $x^{2} + y^{2} = R^{2}$. 过 $x$ 轴上的点 $x (-R \leqslant x \leqslant R)$ 作垂直于 $x$ 轴的平面, 截正劈锥体得等腰三角形. 这截面的面积为

![](images/page_292_image_9.jpg)

<details>
<summary>text_image</summary>

y
h
O
R
x
</details>

图6-15

$$
A (x) = h y = h \sqrt {R ^ {2} - x ^ {2}},
$$

于是所求正劈锥体的体积为

$$
\begin{array}{l} V = \int_ {- R} ^ {R} A (x) \mathrm{d} x = h \int_ {- R} ^ {R} \sqrt {R ^ {2} - x ^ {2}} \mathrm{d} x = 2 h \int_ {0} ^ {R} \sqrt {R ^ {2} - x ^ {2}} \mathrm{d} x \\ = 2 R ^ {2} h \int_ {0} ^ {\frac {\pi}{2}} \sin^ {2} \theta \mathrm{d} \theta = \frac {\pi R ^ {2} h}{2}. \\ \end{array}
$$

由此可知正劈锥体的体积等于同底同高的圆柱体体积的一半.

## 三、平面曲线的弧长

我们知道,圆的周长可以利用圆的内接正多边形的周长当边数无限增多时的极限来确定.现在用类似的方法来建立平面的连续曲线弧长的概念,从而应用定积分来计算弧长.

设 A, B 是曲线弧的两个端点. 在弧  $\widehat{AB}$  上依次任取分点  $A = M_{0}, M_{1}, M_{2}, \cdots, M_{i-1}$ ,

$M_{i},\cdots,M_{n-1},M_{n}=B$ ，并依次连接相邻的分点得一折线（图6-16）。当分点的数目无限增加且每个小段 $\widehat{M_{i-1}M_{i}}$ 都缩向一点时，如果此折线的长 $\sum_{i=1}^{n}|M_{i-1}M_{i}|$ 的极限存在，那么称此极限为曲线弧 $\widehat{AB}$ 的弧长，并称此曲线弧 $\widehat{AB}$ 是可求长的。

对光滑的曲线弧(参看第165页上的脚注),有如下结论:

![](images/page_293_chart_5.jpg)

<details>
<summary>line</summary>

| Point | X | Y |
| --- | --- | --- |
| A=M0 | ~0.15 | ~0.35 |
| M1 | ~0.25 | ~0.65 |
| M2 | ~0.35 | ~0.85 |
| B=Mn | ~0.75 | ~0.75 |
| Mn-1 | ~0.65 | ~0.95 |
</details>

图6-16

定理 光滑曲线弧是可求长的.

这个定理我们不加证明.由于光滑曲线弧是可求长的,故可应用定积分来计算弧长.下面我们利用定积分的元素法来讨论平面光滑曲线弧长的计算公式.

设曲线弧由参数方程

$$
\left\{ \begin{array}{l l} x = \varphi (t), \\ y = \psi (t) \end{array} \right. (\alpha \leqslant t \leqslant \beta)
$$

给出,其中  $\varphi(t),\psi(t)$  在  $[\alpha,\beta]$  上具有连续导数,且  $\varphi'(t),\psi'(t)$  不同时为零.现在来计算这曲线弧的长度.

取参数 $t$ 为积分变量, 它的变化区间为 $[\alpha, \beta]$. 相应于 $[\alpha, \beta]$ 上任一小区间 $[t, t + \mathrm{d}t]$ 的小弧段的长度 $\Delta s$ 近似等于对应的弦的长度 $\sqrt{(\Delta x)^2 + (\Delta y)^2}$, 因为

$$
\Delta x = \varphi (t + \mathrm{d} t) - \varphi (t) \approx \mathrm{d} x = \varphi^ {\prime} (t) \mathrm{d} t,
$$

$$
\Delta y = \psi (t + \mathrm{d} t) - \psi (t) \approx \mathrm{d} y = \psi^ {\prime} (t) \mathrm{d} t,
$$

所以, $\Delta s$ 的近似值(弧微分)即弧长元素为

$$
\mathrm{d} s = \sqrt {(\mathrm{d} x) ^ {2} + (\mathrm{d} y) ^ {2}} = \sqrt {\varphi^ {\prime 2} (t) (\mathrm{d} t) ^ {2} + \psi^ {\prime 2} (t) (\mathrm{d} t) ^ {2}} = \sqrt {\varphi^ {\prime 2} (t) + \psi^ {\prime 2} (t)} \mathrm{d} t.
$$

于是所求弧长为

$$
s = \int_ {\alpha} ^ {\beta} \sqrt {\varphi^ {\prime 2} (t) + \psi^ {\prime 2} (t)} \mathrm{d} t.
$$

当曲线弧由直角坐标方程

$$
y = f (x) \quad (a \leqslant x \leqslant b)
$$

给出,其中 $f(x)$ 在 $[a,b]$ 上具有一阶连续导数,这时曲线弧有参数方程

$$
\left\{ \begin{array}{l l} x = x, \\ y = f (x) \end{array} \right. \quad (a \leqslant x \leqslant b),
$$

从而所求的弧长为

$$
s = \int_ {a} ^ {b} \sqrt {1 + y ^ {\prime 2}}   \mathrm{d} x.
$$

当曲线弧由极坐标方程

$$
\rho = \rho (\theta) \quad (\alpha \leqslant \theta \leqslant \beta)
$$

给出,其中  $\rho(\theta)$  在  $[\alpha,\beta]$  上具有连续导数,则由直角坐标与极坐标的关系可得

$$
\left\{ \begin{array}{l} x = x (\theta) = \rho (\theta) \cos \theta , \\ y = y (\theta) = \rho (\theta) \sin \theta \end{array} \right. (\alpha \leqslant \theta \leqslant \beta),
$$

这就是以极角  $\theta$  为参数的曲线弧的参数方程. 于是, 弧长元素为

$$
\mathrm{d} s = \sqrt {x ^ {\prime 2} (\theta) + y ^ {\prime 2} (\theta)} \mathrm{d} \theta = \sqrt {\rho^ {2} (\theta) + \rho^ {\prime 2} (\theta)} \mathrm{d} \theta ,
$$

从而所求弧长为

$$
s = \int_ {\alpha} ^ {\beta} \sqrt {\rho^ {2} (\theta) + \rho^ {\prime 2} (\theta)} \mathrm{d} \theta .
$$

例11 计算曲线 $y = \frac{2}{3} x^{\frac{3}{2}}$ 上相应于 $a \leqslant x \leqslant b$ 的一段弧（图6-17）的长度.

解 因 $y' = x^{\frac{1}{2}}$，从而弧长元素

$$
\mathrm{d} s = \sqrt {1 + (x ^ {\frac {1}{2}}) ^ {2}}   \mathrm{d} x = \sqrt {1 + x}   \mathrm{d} x.
$$

因此,所求弧长为

$$
s = \int_ {a} ^ {b} \sqrt {1 + x} \mathrm{d} x = \left[ \frac {2}{3} (1 + x) ^ {\frac {3}{2}} \right] _ {a} ^ {b} = \frac {2}{3} \left[ (1 + b) ^ {\frac {3}{2}} - (1 + a) ^ {\frac {3}{2}} \right].
$$

![](images/page_294_chart_15.jpg)

<details>
<summary>area</summary>

| X | Y |
| --- | --- |
| a | 2/3 |
| b | 3/2 |
</details>

图6-17

![](images/page_294_image_17.jpg)

<details>
<summary>text_image</summary>

y
x=a(θ−sin θ)
{ y=a(1−cos θ)
2a
O
2πa
x
</details>

图6-18

例 12 计算摆线(图 6-18)

$$
\left\{ \begin{array}{l} x = a (\theta - \sin \theta), \\ y = a (1 - \cos \theta) \end{array} \right.
$$

的一拱 $(0\leqslant\theta\leqslant2\pi)$ 的长度.

解 弧长元素为

$$
\begin{array}{l} \mathrm{d} s = \sqrt {a ^ {2} (1 - \cos \theta) ^ {2} + a ^ {2} \sin^ {2} \theta} \mathrm{d} \theta \\ = a \sqrt {2 (1 - \cos \theta)} \mathrm{d} \theta = 2 a \sin \frac {\theta}{2} \mathrm{d} \theta . \\ \end{array}
$$

从而,所求弧长

$$
s = \int_ {0} ^ {2 \pi} 2 a \sin \frac {\theta}{2} \mathrm{d} \theta = 2 a \left[ - 2 \cos \frac {\theta}{2} \right] _ {0} ^ {2 \pi} = 8 a.
$$

例 13 求阿基米德螺线  $\rho = a\theta (a > 0)$  相应于  $0 \leqslant \theta \leqslant 2\pi$  一段(图 6-19) 的弧长.

解 弧长元素为

$$
\mathrm{d} s = \sqrt {a ^ {2} \theta^ {2} + a ^ {2}} \mathrm{d} \theta = a \sqrt {1 + \theta^ {2}} \mathrm{d} \theta ,
$$

![](images/page_295_image_6.jpg)

<details>
<summary>text_image</summary>

2πa
O
A
ρ=aθ
</details>

图6-19

于是所求弧长为

$$
s = a \int_ {0} ^ {2 \pi} \sqrt {1 + \theta^ {2}}   \mathrm{d} \theta = \frac {a}{2} \left[ 2 \pi \sqrt {1 + 4 \pi^ {2}} + \ln \left(2 \pi + \sqrt {1 + 4 \pi^ {2}}\right) \right].
$$

![](images/page_295_image_10.jpg)

例题精讲

6-3

## 习题6-2

1. 求图 6-20 中各阴影部分的面积.

![](images/page_295_image_15.jpg)

<details>
<summary>text_image</summary>

y
y=√x
y=x
O
x
</details>

(1)

![](images/page_295_image_17.jpg)

<details>
<summary>text_image</summary>

y
y=e
y=e^x
O
x
</details>

(2)

![](images/page_295_image_19.jpg)

<details>
<summary>text_image</summary>

y
y=2x
y=3-x²
O
x
</details>

(3)

![](images/page_295_image_21.jpg)

<details>
<summary>text_image</summary>

y
y=2x+3
y=x²
O
x
</details>

(4)

图6-20

2. 求由下列各组曲线所围成的图形的面积:

(1) $y = \frac{1}{2} x^2$ 与 $x^2 + y^2 = 8$ （两部分都要计算）；

(2) $y=\frac{1}{x}$ 与直线y=x及x=2;
(3) $y=e^{x},y=e^{-x}$ 与直线x=1;
(4)  $y=\ln x, y$  轴与直线  $y=\ln a, y=\ln b (b>a>0)$ .

3. 求抛物线  $y = -x^{2} + 4x - 3$  及其在点  $(0, -3)$  和  $(3, 0)$  处的切线所围成的图形的面积.

4. 求抛物线  $y^{2}=2px$  及其在点  $\left(\frac{p}{2},p\right)$  处的法线所围成的图形的面积.

5. 试求 $a, b$ 的值, 使得由曲线 $y = \cos x \left(0 \leqslant x \leqslant \frac{\pi}{2}\right)$ 与两坐标轴所围成的图形的面积被曲线 $y = a \sin x$ 与 $y = b \sin x$ 三等分.

6. 求由下列各曲线所围成的图形的面积:

(1) $\rho = 2a\cos \theta$;

(2) $x=a\cos^{3}t,\ y=a\sin^{3}t;$

(3) $\rho = 2a(2 + \cos \theta)$.

7. 求由摆线 $x = a(t - \sin t), y = a(1 - \cos t)$ 的一拱 $(0 \leqslant t \leqslant 2\pi)$ 与横轴所围成的图形的面积.

8. 求对数螺线  $\rho = ae^{\theta} (-\pi \leqslant \theta \leqslant \pi)$  及射线  $\theta = \pi$  所围成的图形的面积.

9. 求下列各曲线所围成图形的公共部分的面积:

(1)  $\rho=3\cos\theta$  及  $\rho=1+\cos\theta;$
(2) $\rho = \sqrt{2}\sin \theta$ 及 $\rho^2 = \cos 2\theta$.
10. 求位于曲线  $y=e^{x}$  下方、该曲线过原点的切线的左方以及 x 轴上方之间的图形的面积.
11. 在区间  $[1, e]$  上求一点  $\xi$ ，使得图 6-21 中所示的阴影部分的面积最小.
12. 已知抛物线 $y = px^2 + qx$ （其中 $p < 0, q > 0$）在第一象限内与直线 $x + y = 5$ 相切，且此抛物线与 $x$ 轴所围成的图形的面积为 $A$. 问 $p$ 和 $q$ 为何值时，$A$ 达到最大值，并求出此最大值.
13. 由 $y = x^3, x = 2, y = 0$ 所围成的图形分别绕 $x$ 轴及 $y$ 轴旋转，计算所得两个旋转体的体积.
14. 把星形线  $x^{2/3} + y^{2/3} = a^{2/3}$  所围成的图形绕 x 轴旋转（图6-22），计算所得旋转体的体积.
15. 用积分方法证明图 6-23 中球缺的体积为

$$
V = \pi H ^ {2} \left(R - \frac {H}{3}\right).
$$

![](images/page_296_chart_25.jpg)

<details>
<summary>area</summary>

| X | Y |
| --- | --- |
| 1 | 0 |
| \(\xi\) | 1 |
| e | 1 |
</details>

图6-21

![](images/page_296_image_27.jpg)

<details>
<summary>text_image</summary>

-a
O
-a
x
y
a
a
</details>

图6-22

![](images/page_296_image_29.jpg)

<details>
<summary>text_image</summary>

y
H
O
R
x
</details>

图6-23

16. 求下列已知曲线所围成的图形按指定的轴旋转所产生的旋转体的体积:

(1) $y=x^{2},x=y^{2}$ ,绕y轴;
(2)  $y=\arcsin x, x=1, y=0$ , 绕 x 轴;

(3) $x^{2}+(y-5)^{2}=16$ , 绕 x 轴;
(4) 摆线  $x = a(t - \sin t)$ ,  $y = a(1 - \cos t)$  的一拱, y = 0, 绕直线 y = 2a.

17. 求圆盘 $x^{2} + y^{2} \leqslant a^{2}$ 绕 $x = -b (b > a > 0)$ 旋转所成旋转体的体积.

18. 设有一截锥体, 其高为 $h$, 上、下底均为椭圆, 椭圆的轴长分别为 $2a, 2b$ 和 $2A, 2B$, 求这截锥体的体积.

19. 计算底面是半径为 $R$ 的圆, 而垂直于底面上一条固定直径的所有截面都是等边三角形的立体体积(图6-24).

20. 证明: 由平面图形 $0 \leqslant a \leqslant x \leqslant b, 0 \leqslant y \leqslant f(x)$ 绕 $y$ 轴旋转所成的旋转体的体积为

$$
V = 2 \pi \int_ {a} ^ {b} x f (x)   \mathrm{d} x.
$$

21. 利用题 20 的结论和方法, 计算曲线  $y = \sin x (0 \leqslant x \leqslant \pi)$  和 x 轴所围成的图形按下列方式所得旋转体的体积:

(1) 绕 y 轴旋转;

(2) 绕直线  $x = -\pi$  旋转.

22. 设由抛物线 $y = 2x^{2}$ 和直线 $x = a, x = 2$ 及 $y = 0$ 所围成的平面图形为 $D_{1}$，由抛物线 $y = 2x^{2}$ 和直线 $x = a$ 及 $y = 0$ 所围成的平面图形为 $D_{2}$，其中 $0 < a < 2$ （图6-25）.

(1) 试求  $D_{1}$  绕 x 轴旋转而成的旋转体体积  $V_{1}, D_{2}$  绕 y 轴旋转而成的旋转体体积  $V_{2}$ ;

(2) 问当 a 为何值时,  $V_{1} + V_{2}$  取得最大值? 试求此最大值.

23. 计算曲线  $y=\ln x$  上相应于  $\sqrt{3}\leqslant x\leqslant2\sqrt{2}$  的一段弧的长度.

![](images/page_297_image_16.jpg)

<details>
<summary>text_image</summary>

y
O
R
x
</details>

图6-24

![](images/page_297_image_18.jpg)

<details>
<summary>text_image</summary>

y
y=2x²
D₂
D₁
O
a
2
x
</details>

图6-25

24. 计算半立方抛物线  $y^{2}=\frac{2}{3}(x-1)^{3}$  被抛物线  $y^{2}=\frac{x}{3}$  截得的一段弧的长度.

25. 计算抛物线  $y^{2}=2px\quad(p>0)$  从顶点到这曲线上的一点  $M(x,y)$  的弧长.

26. 计算星形线  $x = a \cos^{3} t, y = a \sin^{3} t$  （图 6-26）的全长.

27. 将绕在圆(半径为 a)上的细线放开拉直, 使细线与圆周始终相切(图 6-27), 细线端点画出的轨迹叫做圆的渐伸线, 它的方程为

$$
x = a (\cos t + t \sin t), y = a (\sin t - t \cos t).
$$

计算该曲线上相应于 $0 \leqslant t \leqslant \pi$ 的一段弧的长度.

![](images/page_298_image_1.jpg)

<details>
<summary>text_image</summary>

y
a
{x=acos³t
{y=asin³t}
-a O a x
-a
</details>

图6-26

![](images/page_298_image_3.jpg)

<details>
<summary>text_image</summary>

x=a(cos t+tsin t)
y=a(sin t-tcos t)
</details>

图6-27

28. 在摆线  $x=a(t-\sin t)$ ,  $y=a(1-\cos t)$  上求分摆线第一拱成 1:3 的点的坐标.
29. 求对数螺线  $\rho=e^{a\theta}$  相应于  $0\leqslant\theta\leqslant\varphi$  的一段弧长.
30. 求曲线  $\rho\theta=1$  相应于  $\frac{3}{4}\leqslant\theta\leqslant\frac{4}{3}$  的一段弧长.

## 第三节 定积分在物理学上的应用

## 一、变力沿直线所做的功

从物理学知道,如果物体在做直线运动的过程中有一个不变的力 F 作用在该物体上,且这力的方向与物体运动的方向一致,那么,在物体移动了距离 s 时,力 F 对物体所做的功为

$$
W = F \cdot s.
$$

如果物体在运动过程中所受到的力是变化的,这就会遇到变力对物体做功的问题.下面通过具体例子说明如何计算变力所做的功.

例1 把一个带电荷量 $+q$ 的点电荷放在 $r$ 轴上坐标原点 $O$ 处, 它产生一个电场. 这个电场对周围的电荷有作用力. 由物理学知道, 如果有一个单位正电荷放在这个电场中距离原点 $O$ 为 $r$ 的地方, 那么电场对它的作用力的大小为

$$
F = k   \frac {q}{r ^ {2}} \quad (k   \text {是常数}).
$$

见图6-28, 当这个单位正电荷在电场中从 $r = a$ 处沿 $r$ 轴移动到 $r = b (a < b)$ 处时, 计算电场力 $F$ 对它所做的功.

解 在上述移动过程中,电场对这单位正电荷的作用力是变的.取 r 为积分变量,它的变化区间为  $[a, b]$ .设$[r, r + \mathrm{d}r]$ 为 $[a, b]$ 上的任一小区间. 当单位正电荷从 $r$ 移动到 $r + \mathrm{d}r$ 时, 电场力对它所做的功近似于 $\frac{kq}{r^2}\mathrm{d}r$, 即功元素为

![](images/page_298_image_18.jpg)

图6-28

$$
\mathrm{d} W = \frac {k q}{r ^ {2}} \mathrm{d} r,
$$

于是所求的功为

$$
W = \int_ {a} ^ {b} \frac {k q}{r ^ {2}} \mathrm{d} r = k q \left[ - \frac {1}{r} \right] _ {a} ^ {b} = k q \left(\frac {1}{a} - \frac {1}{b}\right).
$$

在计算静电场中某点的电位时,要考虑将单位正电荷从该点处 $(r=a)$ 移到无穷远处时电场力所做的功W.此时,电场力对单位正电荷所做的功就是反常积分

$$
W = \int_ {a} ^ {+ \infty} \frac {k q}{r ^ {2}} \mathrm{d} r = \left[ - \frac {k q}{r} \right] _ {a} ^ {+ \infty} = \frac {k q}{a}.
$$

例 2 在底面积为 S 的圆柱形容器中存有一定量的气体. 在等温条件下, 由于气体的膨胀, 把容器中的一个活塞(面积为 S)从点 a 处推移到点 b 处(图 6-29). 计算在移动过程中, 气体压力所做的功.

![](images/page_299_image_8.jpg)

<details>
<summary>text_image</summary>

O a x x+dx b x
S
</details>

图6-29

解 取坐标系如图 6-29 所示. 活塞的位置可以

用坐标 x 来表示. 由物理学知道, 一定量的气体在等温条件下, 压强 p 与体积 V 的乘积是常数 k, 即

$$
p V = k \quad {\text {或}} \quad p = {\frac {k}{V}}.
$$

因为 V = xS，所以

$$
p = \frac {k}{x S}.
$$

于是,作用在活塞上的力

$$
F = p \cdot S = \frac {k}{x S} \cdot S = \frac {k}{x}.
$$

在气体膨胀过程中,体积 V 是变化的,因而 x 也是变化的,所以作用在活塞上的力也是变化的.

取 $x$ 为积分变量, 它的变化区间为 $[a, b]$. 设 $[x, x + \mathrm{d}x]$ 为 $[a, b]$ 上任一小区间, 当活塞从 $x$ 移动到 $x + \mathrm{d}x$ 时, 变力 $F$ 所做的功近似于 $\frac{k}{x} \mathrm{~d} x$, 即功元素为

$$
\mathrm{d} W = \frac {k}{x} \mathrm{d} x,
$$

于是所求的功为

$$
W = \int_ {a} ^ {b} \frac {k}{x} \mathrm{d} x = k \left[ \ln x \right] _ {a} ^ {b} = k \ln \frac {b}{a}.
$$

下面再举一个计算功的例子,它虽不是一个变力做功问题,但也可用积分来计算.

例 3 一圆柱形的贮水桶高为 5 m, 底圆半径为 3 m, 桶内盛满了水. 试问要把桶内的水全部吸出需做多少功?

解 作 $x$ 轴如图6-30所示.取深度 $x$ （单位为 $\mathrm{m}$ ）为积分变量，它的变化区间为[0,5].相应于[0,5]上任一小区间 $[x,x + \mathrm{d}x]$ 的一薄层水的高度为 $\mathrm{dx}$，若重力加速度 $g$ 取 $9.8\mathrm{m / s^2}$，则这薄层水所受重力为 $9.8\pi \cdot 3^{2}\mathrm{dx}$ kN.把这薄层水吸出桶外需做的功近似地为

$$
\mathrm{d} W = 8 8. 2 \pi x \mathrm{d} x,
$$

![](images/page_300_image_6.jpg)

<details>
<summary>text_image</summary>

O
x
5 m
x+dx
3 m
x
</details>

图6-30

此即功元素.于是所求的功为

$$
W = \int_ {0} ^ {5} 8 8. 2 \pi x \mathrm{d} x = 8 8. 2 \pi \left[ \frac {x ^ {2}}{2} \right] _ {0} ^ {5} = 8 8. 2 \pi \cdot \frac {2 5}{2} \approx 3 4 6 2 (\mathrm{kJ}).
$$

## 二、水压力

从物理学知道,在水深为 h 处的压强为  $p=\rho gh$ , 这里  $\rho$  是水的密度, g 是重力加速度. 如果有一面积为 A 的平板水平地放置在水深为 h 处, 那么, 平板一侧所受的水压力为

$$
P = p \cdot A.
$$

如果平板铅直放置在水中,那么,由于水深不同的点处压强 p 不相等,平板一侧所受的水压力就不能用上述方法计算.下面举例说明它的计算方法.

例 4 一个横放着的圆柱形水桶, 桶内盛有半桶水(图 6-31(a)). 设桶的底半径为 R, 水的密度为  $\rho$ , 计算桶的一个端面上所受的压力.

![](images/page_300_image_15.jpg)

图6-31

解 桶的一个端面是圆片,所以现在要计算的是当水平面通过圆心时,铅直放置的一个半圆片的一侧所受到的水压力.

如图6-31(b)，在这个圆片上取过圆心且铅直向下的直线为 $x$ 轴，过圆心的水平线为 $y$ 轴.对这个坐标系来讲，所讨论的半圆的方程为 $x^{2} + y^{2} = R^{2}$ （$0 \leqslant x \leqslant R$）.取 $x$ 为积分变量，它的变化区间为 $[0, R]$.设 $[x, x + \mathrm{d}x]$ 为 $[0, R]$ 上的任一小区间，半圆片上相应于 $[x, x + \mathrm{d}x]$ 的窄条上各点处的压强近似于 $\rho gx$，这窄条的面积近似于 $2\sqrt{R^2 - x^2} \mathrm{d}x$。因此，这窄条一侧所受水压力的近似值，即压力元素为

$$
\mathrm{d} P = 2 \rho g x \sqrt {R ^ {2} - x ^ {2}} \mathrm{d} x.
$$

于是所求压力为

$$
\begin{array}{l} P = \int_ {0} ^ {R} 2 \rho g x \sqrt {R ^ {2} - x ^ {2}} \mathrm{d} x = - \rho g \int_ {0} ^ {R} (R ^ {2} - x ^ {2}) ^ {\frac {1}{2}} \mathrm{d} (R ^ {2} - x ^ {2}) \\ = - \rho g \left[ \frac {2}{3} (R ^ {2} - x ^ {2}) ^ {\frac {3}{2}} \right] _ {0} ^ {R} = \frac {2 \rho g}{3} R ^ {3}. \\ \end{array}
$$

## 三、引力

从物理学知道,质量分别为  $m_{1}, m_{2}$ , 相距为 r 的两质点间的引力的大小为

$$
F = G \frac {m _ {1} m _ {2}}{r ^ {2}},
$$

其中 G 为引力常量, 引力的方向沿着两质点的连线方向.

如要计算一根细棒对一个质点的引力,那么,由于细棒上各点与该质点的距离是变化的,且各点对该质点的引力的方向也是变化的,因此就不能用上述公式来计算.下面举例说明它的计算方法.

例 5 设有一长度为 l、线密度为  $\mu$  的均匀细直棒，在其中垂线上距棒 a 单位处有一质量为 m 的质点 M。试计算该棒对质点 M 的引力。

解 取坐标系如图6-32所示,使棒位于y轴上,质点M位于x轴上,棒的中点为原点O.取y为积分变量,它的变化区间为 $\left[-\frac{l}{2},\frac{l}{2}\right]$ .设 $[y,y+dy]$ 为 $\left[-\frac{l}{2},\frac{l}{2}\right]$ 上任一小区间,把细直棒上相应于 $[y,y+dy]$ 的一小段近似地看成质点,其质量为 $\mu dy$ ,与M相距 $r=\sqrt{a^{2}+y^{2}}$ .因此可以按照两质点间的引力计算公式求出这小段细直棒对质点M的引力 $\Delta F$ 的大小为

![](images/page_301_image_12.jpg)

<details>
<summary>text_image</summary>

y
l/2
y+dy
y
r
O
a
M
x
- l/2
</details>

图6-32

$$
\Delta F \approx G \frac {m \mu \mathrm{d} y}{a ^ {2} + y ^ {2}},
$$

从而求出 $\Delta F$ 在水平方向分力 $\Delta F_{x}$ 的近似值，即细直棒对质点 $M$ 的引力在水平方向分力 $F_{x}$ 的元素为

$$
\mathrm{d} F _ {x} = - G \frac {a m \mu \mathrm{d} y}{(a ^ {2} + y ^ {2}) ^ {\frac {3}{2}}}.
$$

于是得引力在水平方向分力为

$$
F _ {x} = - \int_ {- \frac {l}{2}} ^ {\frac {l}{2}} \frac {G a m \mu}{(a ^ {2} + y ^ {2}) ^ {\frac {3}{2}}} \mathrm{d} y = - \frac {2 G m \mu l}{a} \cdot \frac {1}{\sqrt {4 a ^ {2} + l ^ {2}}}.
$$

由对称性知,引力在铅直方向分力为  $F_{y}=0$ .

当细直棒的长度 $l$ 很大时, 可视 $l$ 趋于无穷. 此时, 引力的大小为 $\frac{2Gm\mu}{a}$, 方向与细直棒垂直且由 $M$ 指向细直棒.

## 习题6-3

1. 由实验知道, 弹簧在拉伸过程中, 需要的力 F (单位: N) 与伸长量 s (单位: cm) 成正比, 即
F=ks （k 是弹性系数）.

如果把弹簧由原长拉伸  $6 \, cm$ ，计算所做的功。

2. 直径为  $20 \, cm$ 、高为  $80 \, cm$  的圆筒内充满压强为  $10 \, N/cm^{2}$  的蒸汽。设温度保持不变，要使蒸汽体积缩小一半，问需要做多少功？

3.（1）证明:把质量为 $m$ 的物体从地球表面升高到 $h$ 处所做的功是

$$
W = \frac {m g R h}{R + h},
$$

其中 g 是重力加速度, R 是地球的半径;

(2) 一颗人造地球卫星的质量为 $173 \mathrm{~kg}$, 在高于地面 $630 \mathrm{~km}$ 处进入轨道. 问把这颗卫星从地面送到 $630 \mathrm{~km}$ 的高空处, 克服地球引力要做多少功? 已知 $g = 9.8 \mathrm{~m} / \mathrm{s}^{2}$, 地球半径 $R = 6370 \mathrm{~km}$.

4. 一物体按规律 $x = ct^3$ 做直线运动, 介质的阻力与速度的平方成正比. 计算物体由 $x = 0$ 移至 $x = a$ 时, 克服介质阻力所做的功.

5. 用铁锤将一铁钉击入木板, 设木板对铁钉的阻力与铁钉被击入木板的深度成正比, 在锤击第一次时, 将铁钉击入木板 1 cm. 如果铁锤每次锤击铁钉所做的功相等, 问锤击第二次时, 铁钉又被击入木板多少?

6. 设一圆锥形贮水池, 深 15 m, 口径 20 m, 盛满水, 今以泵将水吸尽, 问要做多少功?

7. 有一铅直放置的矩形闸门, 它的顶端与水面相平, 一条对角线将闸门分成两个三角形区域. 试证: 其中一个三角形区域上所受的水压力是另一个三角形区域上所受水压力的 2 倍.

8. 有一等腰梯形闸门, 它的两条底边各长 $10 \mathrm{~m}$ 和 $6 \mathrm{~m}$, 高为 $20 \mathrm{~m}$. 较长的底边与水面相齐. 计算闸门的一侧所受的水压力.

9. 一底为 $8 \mathrm{~cm}$ 、高为 $6 \mathrm{~cm}$ 的等腰三角形片, 铅直地沉没在水中, 顶在上, 底在下且与水面平行, 而顶离水面 $3 \mathrm{~cm}$, 试求它每面所受的压力.

10. 设有一长度为 l、线密度为  $\mu$  的均匀细直棒，在与棒的一端垂直距离为 a 单位处有一质量为

m 的质点 M, 试求这细棒对质点 M 的引力.

11. 设有一半径为 $R$ 、圆心角为 $\varphi$ 的圆弧形细棒，其线密度为常数 $\mu$. 在圆心处有一质量为 $m$ 的质点 $M$. 试求这细棒对质点 $M$ 的引力.

## 总习题六

1. 填空:

(1) 曲线  $y = x^{3} - 5x^{2} + 6x$  与 x 轴所围成的图形的面积 A = \_\_\_\_;
(2) 曲线  $y=\frac{\sqrt{x}}{3}(3-x)$  上相应于  $1 \leqslant x \leqslant 3$  的一段弧的长度 s= \_\_\_\_.

2. 以下三题中均给出了四个结论,从中选出一个正确的结论:

（1）设 x 轴上有一长度为 l、线密度为常数  $\mu$  的细棒，在与细棒右端的距离为 a 处有一质量为 m 的质点 M（图 6-33），已知引力常量为 G，则质点 M 与细棒之间的引力的大小为（）；

![](images/page_303_image_10.jpg)

图6-33

(A) $\int_{-l}^{0}\frac{Gm\mu}{(a - x)^2}\mathrm{d}x$

(B) $\int_0^l\frac{Gm\mu}{(a - x)^2}\mathrm{d}x$

(C) $2\int_{-\frac{1}{2}}^{0}\frac{Gm\mu}{(a - x)^{2}}\mathrm{d}x$

(D) $2\int_{0}^{\frac{l}{2}}\frac{Gm\mu}{(a - x)^{2}}\mathrm{d}x$

（2）设在区间 $[a, b]$ 上，$f(x) > 0, f'(x) > 0, f''(x) < 0.$ 令 $A_1 = \int_{a}^{b} f(x) \, \mathrm{d}x, A_2 = f(a)(b - a), A_3 = \frac{1}{2} [f(a) + f(b)] (b - a)$，则有（ ）；

(A)  $A_{1}<A_{2}<A_{3}$

(B) $A_{2} < A_{1} < A_{3}$

(C)  $A_{3}<A_{1}<A_{2}$

(D) $A_{2} < A_{3} < A_{1}$

（3）有半径不相等的两个木质球体，分别在中间钻出一个以球体直径为轴的圆柱形洞，使得剩下的两个环状立体的高都等于 $h$ （图6-34).假设对应木质球半径较大的环状立体为 $P$ ，另一个为 $Q$ .通过计算，正确的结论是（ ）.

![](images/page_303_image_22.jpg)

<details>
<summary>text_image</summary>

y
R
h
O r x
</details>

图6-34

(A) P 的体积大于 Q 的体积
(B) P 的体积等于 Q 的体积
(C) P 的体积小于 Q 的体积
(D) 在 h 的不同取值范围, P 与 Q 的体积有不同的大小关系

3. 一金属棒长 $3\mathrm{m}$, 离棒左端 $x\mathrm{m}$ 处的线密度为 $\mu(x) = \frac{1}{\sqrt{x + 1}}\mathrm{kg / m}$. 问 $x$ 为何值时, $[0, x]$ 一段的质量为全棒质量的一半?

4. 求由曲线  $\rho = a \sin \theta, \rho = a (\cos \theta + \sin \theta) (a > 0)$  所围图形公共部分的面积.
5. 如图 6-35 所示, 从下到上依次有三条曲线:  $y = x^{2}$ ,  $y = 2x^{2}$  和 C. 假设对曲线  $y = 2x^{2}$  上的任一点

P, 所对应的面积 A 和 B 恒相等, 求曲线 C 的方程.

6. 设抛物线  $y=ax^{2}+bx+c$  ( $a\neq0$ ) 通过点(0,0)，且当  $x\in[0,1]$  时， $y\geqslant0$ 。试确定 a,b,c 的值，使得抛物线  $y=ax^{2}+bx+c$  与直线 x=1，y=0 所围图形的面积为  $\frac{4}{9}$ ，且使该图形绕 x 轴旋转而成的旋转体的体积最小。
7. 过坐标原点作曲线  $y=\ln x$  的切线, 该切线与曲线  $y=\ln x$  及 x 轴围成平面图形 D.

![](images/page_304_image_5.jpg)

<details>
<summary>text_image</summary>

y
C
y=2x²
y=x²
A
P
B
O
x
</details>

图6-35

(1) 求平面图形 D 的面积 A;
(2) 求平面图形 D 绕直线 x = e 旋转一周所得旋转体的体积 V.

8. 设曲线 $C$ 为函数 $y = x\mathrm{e}^{-x}$ ($x \geqslant 0$) 的图形, $M(x_0, y_0)$ 为 $C$ 上的一个拐点, $MT$ 为曲线 $C$ 在点 $M$ 处的切线. 求由曲线 $C$、切线 $MT$ 和 $x$ 轴所围的向右无限延伸的平面图形的面积.
9. 求由曲线  $y=x^{\frac{3}{2}}$ ，直线 x=4 及 x 轴所围图形绕 y 轴旋转而成的旋转体的体积.
10. 求圆盘 $(x-2)^{2}+y^{2}\leqslant1$  绕 y 轴旋转而成的旋转体的体积.
11. 求抛物线  $y=\frac{1}{2}x^{2}$  被圆  $x^{2}+y^{2}=3$  所截下的有限部分的弧长.
12. 半径为 r 的球沉入水中, 球的上部与水面相切, 球的密度与水相同, 现将球从水中取出, 需做多少功?
13. 边长为 $a$ 和 $b$ 的矩形薄板, 与液面成 $\alpha$ 角斜沉于液体内, 长边平行于液面而位于深 $h$ 处, 设 $a > b$, 液体的密度为 $\rho$, 试求薄板每面所受的压力.
14. 设星形线  $x = a \cos^{3} t, y = a \sin^{3} t$  上每一点处的线密度的大小等于该点到原点距离的立方，在原点 O 处有一单位质点，求星形线在第一象限的弧段对这质点的引力.
15. 某建筑工程打地基时, 需用汽锤将桩打进土层. 汽锤每次击打, 都要克服土层对桩的阻力做功. 设土层对桩的阻力的大小与桩被打进地下的深度成正比 (比例系数为 $k, k > 0$). 汽锤第一次击打将桩打进地下 $a \mathrm{~m}$. 根据设计方案, 要求汽锤每次击打桩时所做的功与前一次击打时所做的功之比为常数 $r$ ($0 < r < 1$). 问

(1) 汽锤击打桩 3 次后, 可将桩打进地下多深?
(2) 若击打次数不限, 则汽锤至多能将桩打进地下多深?

![](images/page_304_image_22.jpg)

第六章释疑解难

![](images/page_304_image_24.jpg)

第六章例题精讲

## 第七章

## 微分方程

函数是客观事物的内部联系在数量方面的反映,利用函数关系又可以对客观事物的规律性进行研究.因此如何寻求函数关系,在实践中具有重要意义.在许多问题中,往往不能直接找出所需要的函数关系,但是根据问题所提供的情况,有时可以列出含有要找的函数及其导数的关系式.这样的关系式就是所谓微分方程.微分方程建立以后,对它进行研究,求出未知函数,这就是解微分方程.本章主要介绍微分方程的一些基本概念和几种常用的微分方程的解法.

## 第一节 微分方程的基本概念

下面我们通过几何、力学及物理学中的几个具体例题来说明微分方程的基本概念.

例1 一曲线通过点(1,2)，且在该曲线上任一点 $M(x,y)$ 处的切线的斜率为 $2x$，求这曲线的方程.

解 设所求曲线的方程为  $y=\varphi(x)$ . 根据导数的几何意义, 可知未知函数  $y=\varphi(x)$  应满足关系式

$$
\frac {\mathrm{d} y}{\mathrm{d} x} = 2 x. \tag {1-1}
$$

此外,未知函数  $y=\varphi(x)$  还应满足下列条件:

$$
x = 1 \text {时}, \quad y = 2. \tag {1-2}
$$

把(1-1)式两端积分, 得  $y=\int2x\,dx$  即

$$
y = x ^ {2} + C, \tag {1-3}
$$

其中 C 是任意常数.

把条件“x=1时,y=2”代入(1-3)式,得

$$
2 = 1 ^ {2} + C,
$$

由此定出 $C = 1$ .把 $C = 1$ 代入(1-3)式，即得所求曲线方程

$$
y = x ^ {2} + 1. \tag {1-4}
$$

例 2 列车沿直线以  $20 \, m/s$  （相当于  $72 \, km/h$ ）的速度行驶，当制动时列车获得加速度  $-0.4 \, m/s^{2}$ . 问开始制动后多少时间列车才能停住以及列车在这段时间里行驶了多少路程？

解 设列车在开始制动后 t s 时行驶了 s m. 根据题意, 反映制动阶段列车运动规律的函数  $s = s(t)$  应满足关系式

$$
\frac {\mathrm{d} ^ {2} s}{\mathrm{d} t ^ {2}} = - 0. 4. \tag {1-5}
$$

此外,未知函数  $s=s(t)$  还应满足下列条件:

$$
t = 0 \text {时,} \quad s = 0, \quad v = \frac {\mathrm{d} s}{\mathrm{d} t} = 2 0. \tag {1-6}
$$

把(1-5)式两端积分一次,得

$$
v = \frac {\mathrm{d} s}{\mathrm{d} t} = - 0. 4 t + C _ {1}, \tag {1-7}
$$

再积分一次,得

$$
s = - 0. 2 t ^ {2} + C _ {1} t + C _ {2}, \tag {1-8}
$$

这里  $C_{1}, C_{2}$  都是任意常数.

把条件“t=0 时，v=20”代入(1-7)式，得

$$
2 0 = C _ {1},
$$

把条件“t=0 时,s=0”代入(1-8)式,得

$$
0 = C _ {2}.
$$

把 $C_1, C_2$ 的值代入(1-7)及(1-8)式，得

$$
v = - 0. 4 t + 2 0, \tag {1-9}
$$

$$
s = - 0. 2 t ^ {2} + 2 0 t. \tag {1-10}
$$

在(1-9)式中令 $v = 0$ ，得到列车从开始制动到完全停住所需的时间

$$
t = \frac {2 0}{0 . 4} = 5 0 (\mathrm{s}).
$$

再把 $t = 50$ 代入(1-10)式，得到列车在制动阶段行驶的路程

$$
s = - 0. 2 \times 5 0 ^ {2} + 2 0 \times 5 0 = 5 0 0 (\mathrm{m}).
$$

上述两个例子中的关系式(1-1)和(1-5)都含有未知函数的导数,它们都是微分方程.一般地,凡表示未知函数、未知函数的导数与自变量之间的关系的方程,叫做微

分方程,有时也简称方程.

微分方程中所出现的未知函数的最高阶导数的阶数, 叫做微分方程的阶. 例如, 方程(1-1)是一阶微分方程, 方程(1-5)是二阶微分方程. 又如, 方程

$$
x ^ {3} y ^ {\prime \prime \prime} + x ^ {2} y ^ {\prime \prime} - 4 x y ^ {\prime} = 3 x ^ {2}
$$

是三阶微分方程,方程

$$
y ^ {(4)} - 4 y ^ {\prime \prime \prime} + 1 0 y ^ {\prime \prime} - 1 2 y ^ {\prime} + 5 y = \sin 2 x
$$

是四阶微分方程.

一般地，$n$ 阶微分方程的形式是

$$
F (x, y, y ^ {\prime}, \dots , y ^ {(n)}) = 0. \tag {1-11}
$$

这里必须指出,在方程(1-11)中, $y^{(n)}$ 是必须出现的,而 $x,y,y',\cdots,y^{(n-1)}$ 等则可以不出现.例如n阶微分方程

$$
y ^ {(n)} + 1 = 0
$$

中，除 $y^{(n)}$ 外，$y$ 的其他阶导数和自变量 $x$ 都没有出现

如果能从方程(1-11)中解出最高阶导数,那么可得微分方程

$$
y ^ {(n)} = f (x, y, y ^ {\prime}, \dots , y ^ {(n - 1)}). \tag {1-12}
$$

以后我们讨论的微分方程都是已解出最高阶导数的方程或能解出最高阶导数的方程.

由前面的例子我们看到,在研究某些实际问题时,首先要建立微分方程,然后找出满足微分方程的函数(解微分方程),就是说,找出这样的函数,把这函数代入微分方程能使该方程成为恒等式.这个函数就叫做该微分方程的解.确切地说,设函数 $y=\varphi(x)$ 在区间I上有n阶连续导数,如果在区间I上,

$$
f [ x, \varphi (x), \varphi^ {\prime} (x), \dots , \varphi^ {(n)} (x) ] \equiv 0,
$$

那么函数  $y=\varphi(x)$  就叫做微分方程 (1-11) 在区间 I 上的解.

例如,函数(1-3)和(1-4)都是微分方程(1-1)的解,函数(1-8)和(1-10)都是微分方程(1-5)的解.

如果微分方程的解中含有任意常数,且任意常数的个数与微分方程的阶数相同①,这样的解叫做微分方程的通解.例如,函数(1-3)是方程(1-1)的解,它含有1个任意常数,而方程(1-1)是一阶的,所以函数(1-3)是方程(1-1)的通解.又如,函数(1-8)是方程(1-5)的解,它含有2个任意常数,而方程(1-5)是二阶的,所以函数(1-8)是方程(1-5)的通解.

由于通解中含有任意常数,所以它还不能完全确定地反映函数所代表的某一个客观事物的规律性.要完全确定地反映客观事物的规律性,必须确定这些常数的值.为

![](images/page_307_image_21.jpg)

释疑解难

7-1

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 这里所说的任意常数是相互独立的, 就是说, 它们不能合并而使得任意常数的个数减少(参看本章第六节关于函数组的线性相关性).</span></small>

此,要根据问题的实际情况,提出确定这些常数的条件.例如,例1中的条件(1-2)及例2中的条件(1-6)便是这样的条件.

设微分方程中的未知函数为  $y=\varphi(x)$ ，如果微分方程是一阶的，通常用来确定任意常数的条件是

$$
x = x _ {0} \text {时}, \quad y = y _ {0},
$$

或写成

$$
y \mid_ {x = x _ {0}} = y _ {0},
$$

其中 $x_0, y_0$ 都是给定的值；如果微分方程是二阶的，通常用来确定任意常数的条件是

$$
x = x _ {0} \text {时}, \quad y = y _ {0}, \quad y ^ {\prime} = y _ {0} ^ {\prime},
$$

或写成

$$
y \mid_ {x = x _ {0}} = y _ {0}, \quad y ^ {\prime} \mid_ {x = x _ {0}} = y _ {0} ^ {\prime},
$$

其中 $x_0, y_0$ 和 $y_0'$ 都是给定的值. 上述这种条件叫做初值条件.

确定了通解中的任意常数以后, 就得到微分方程的特解. 例如(1-4)式是方程(1-1)满足条件(1-2)的特解,(1-10)式是方程(1-5)满足条件(1-6)的特解.

求微分方程  $y' = f(x, y)$  满足初值条件  $y \mid_{x=x_{0}} = y_{0}$  的特解这样一个问题，叫做一阶微分方程的初值问题，记作

$$
\left\{ \begin{array}{l} y ^ {\prime} = f (x, y), \\ y \mid_ {x = x _ {0}} = y _ {0}. \end{array} \right. \tag {1-13}
$$

微分方程的解的图形是一条曲线,叫做微分方程的积分曲线.初值问题(1-13)的几何意义,就是求微分方程的通过点 $(x_{0},y_{0})$ 的那条积分曲线.二阶微分方程的初值问题

$$
\left\{ \begin{array}{l} y ^ {\prime \prime} = f (x, y, y ^ {\prime}), \\ y \mid_ {x = x _ {0}} = y _ {0}, y ^ {\prime} \mid_ {x = x _ {0}} = y _ {0} ^ {\prime} \end{array} \right.
$$

的几何意义,是求微分方程的通过点 $(x_{0},y_{0})$ 且在该点处的切线斜率为 $y_{0}^{\prime}$ 的那条积分曲线.

例 3 验证: 函数

$$
x = C _ {1} \cos k t + C _ {2} \sin k t \tag {1-14}
$$

是微分方程

$$
\frac {\mathrm{d} ^ {2} x}{\mathrm{d} t ^ {2}} + k ^ {2} x = 0 \tag {1-15}
$$

的解.

解 求出所给函数(1-14)的导数

$$
\frac {\mathrm{d} x}{\mathrm{d} t} = - k C _ {1} \sin k t + k C _ {2} \cos k t, \tag {1-16}
$$

$$
\frac {\mathrm{d} ^ {2} x}{\mathrm{d} t ^ {2}} = - k ^ {2} C _ {1} \cos k t - k ^ {2} C _ {2} \sin k t = - k ^ {2} (C _ {1} \cos k t + C _ {2} \sin k t).
$$

把 $\frac{\mathrm{d}^2x}{\mathrm{d}t^2}$ 及 $x$ 的表达式代入方程(1-15)，得

$$
- k ^ {2} (C _ {1} \cos k t + C _ {2} \sin k t) + k ^ {2} (C _ {1} \cos k t + C _ {2} \sin k t) \equiv 0.
$$

函数(1-14)及其二阶导数代入方程(1-15)后成为一个恒等式,因此函数(1-14)是微分方程(1-15)的解.

例 4 已知函数(1-14)当  $k \neq 0$  时是微分方程(1-15)的通解, 求满足初值条件

$$
x \mid_ {t = 0} = A, \quad \frac {\mathrm{d} x}{\mathrm{d} t} \bigg | _ {t = 0} = 0
$$

的特解.

解 将条件“t=0 时, x=A”代入(1-14)式得

$$
C _ {1} = A.
$$

将条件“t=0 时, $\frac{dx}{dt}=0$ ”代入(1-16)式,得

$$
C _ {2} = 0.
$$

把 $C_1, C_2$ 的值代入(1-14)式, 就得所求的特解

$$
x = A \cos k t.
$$

## 习题 7-1

1. 试说出下列各微分方程的阶数:

(1) $x(y')^2 - 2yy' + x = 0$;

(2) $x^{2}y^{\prime \prime} - xy^{\prime} + y = 0;$

(3)  $xy''' + 2y'' + x^{2}y = 0;$

(4) $(7x-6y)\mathrm{d}x+(x+y)\mathrm{d}y=0;$

(5) $L\frac{\mathrm{d}^{2}Q}{\mathrm{d}t^{2}}+R\frac{\mathrm{d}Q}{\mathrm{d}t}+\frac{Q}{C}=0;$

(6) $\frac{\mathrm{d}\rho}{\mathrm{d}\theta} + \rho = \sin^2\theta.$

2. 指出下列各题中的函数是不是所给微分方程的解:

(1) $xy' = 2y, y = 5x^2$;
(2)  $y'' + y = 0, y = 3 \sin x - 4 \cos x;$
(3) $y''-2y'+y=0,y=x^{2}e^{x};$
(4) $y''-(\lambda_1+\lambda_2)y'+\lambda_1\lambda_2y=0,y=C_1e^{\lambda_1x}+C_2e^{\lambda_2x}.$

3. 在下列各题中, 验证所给二元方程所确定的函数为所给微分方程的解:

(1) $(x-2y)y'=2x-y,x^{2}-xy+y^{2}=C;$
(2) $(xy-x)y''+xy'^{2}+yy'-2y'=0,y=\ln(xy).$

4. 在下列各题中, 确定函数关系式中所含的参数, 使函数满足所给的初值条件:

(1) $x^{2} - y^{2} = C, y \mid_{x=0} = 5$;
(2) $y = (C_1 + C_2x)\mathrm{e}^{2x},y\mid_{x = 0} = 0,y' \mid_{x = 0} = 1;$
(3) $y = C_1 \sin(x - C_2), y \mid_{x = \pi} = 1, y' \mid_{x = \pi} = 0.$

5. 写出由下列条件确定的曲线所满足的微分方程:

(1) 曲线在点 $(x,y)$ 处的切线的斜率等于该点横坐标的平方；
(2) 曲线上点  $P(x,y)$  处的法线与 x 轴的交点为 Q，且线段 PQ 被 y 轴平分；
(3) 曲线上点  $P(x,y)$  处的切线与 y 轴的交点为 Q，线段 PQ 的长度为 a，且曲线通过点  $(a,0)$ .

6. 用微分方程表示一物理命题: 某种气体的压强 p 对于温度 T 的变化率与压强成正比, 与温度的平方成反比.

7. 一个半球体形状的雪堆, 其体积融化率与半球面面积 A 成正比, 比例系数 k > 0. 假设在融化过程中雪堆始终保持半球体形状, 已知半径为  $r_{0}$  的雪堆在开始融化的 3 h 内, 融化了其体积的  $\frac{7}{8}$ , 问雪堆全部融化需要多少时间?

## 第二节 可分离变量的微分方程

本节至第四节,我们讨论一阶微分方程

$$
y ^ {\prime} = f (x, y) \tag {2-1}
$$

的一些解法.

一阶微分方程有时也写成如下的对称形式:

$$
P (x, y) \mathrm{d} x + Q (x, y) \mathrm{d} y = 0. \tag {2-2}
$$

在方程(2-2)中,变量 x 与 y 对称,它既可看作是以 x 为自变量 y 为因变量的方程

$$
\frac {\mathrm{d} y}{\mathrm{d} x} = - \frac {P (x , y)}{Q (x , y)}
$$

（这时 $Q(x,y)\neq 0$），也可看作是以 $y$ 为自变量 $x$ 为因变量的方程

$$
\frac {\mathrm{d} x}{\mathrm{d} y} = - \frac {Q (x , y)}{P (x , y)}
$$

(这时  $P(x,y) \neq 0$ ).

在第一节的例 1 中, 我们遇到一阶微分方程

$$
\frac {\mathrm{d} y}{\mathrm{d} x} = 2 x,
$$

或

$$
\mathrm{d} y = 2 x \mathrm{d} x.
$$

把上式两端积分就得到这个方程的通解

$$
y = x ^ {2} + C.
$$

但是并不是所有的一阶微分方程都能这样求解.例如,对于一阶微分方程

$$
\frac {\mathrm{d} y}{\mathrm{d} x} = 2 x y ^ {2}, \tag {2-3}
$$

就不能像上面那样用直接对两端积分的方法求出它的通解.这是什么缘故呢？原因是方程(2-3)的右端含有与 $x$ 存在函数关系的变量 $y$ ，积分

$$
\int 2 x y ^ {2} \mathrm{d} x
$$

求不出来, 这是困难所在. 为了解决这个困难, 在方程(2-3)的两端同时乘 $\frac{dx}{y^{2}}$ , 使方程(2-3)变为

$$
\frac {\mathrm{d} y}{y ^ {2}} = 2 x \mathrm{d} x,
$$

这样,变量 x 与 y 已分离在等式的两端,然后两端积分得

$$
- \frac {1}{y} = x ^ {2} + C,
$$

或

$$
y = - \frac {1}{x ^ {2} + C}, \tag {2-4}
$$

其中 C 是任意常数.

可以验证,函数(2-4)确实满足一阶微分方程(2-3),且含有一个任意常数,所以它是方程(2-3)的通解.

一般地,如果一个一阶微分方程能写成

$$
g (y) \mathrm{d} y = f (x) \mathrm{d} x \tag {2-5}
$$

的形式,就是说,能把微分方程写成一端只含 y 的函数和 dy,另一端只含 x 的函数和 dx,那么原方程就称为可分离变量的微分方程.

假定方程(2-5)中的函数 $g(y)$ 和 $f(x)$ 是连续的.设 $y = \varphi (x)$ 是方程(2-5)的解，将它代入(2-5)中得到恒等式

$$
g [ \varphi (x) ] \varphi^ {\prime} (x) \mathrm{d} x = f (x) \mathrm{d} x.
$$

将上式两端积分,并由  $y=\varphi(x)$  引进变量 y, 得

$$
\int g (y) \mathrm{d} y = \int f (x) \mathrm{d} x.
$$

设 $G(y)$ 及 $F(x)$ 依次为 $g(y)$ 及 $f(x)$ 的原函数，于是有

$$
G (y) = F (x) + C. \tag {2-6}
$$

因此，方程(2-5)的解满足关系式(2-6).反之，如果 $y = \Phi (x)$ 是由关系式(2-6)所确定的隐函数,那么在  $g(y) \neq 0$  的条件下,  $y = \Phi(x)$  也是方程(2-5)的解,事实上,由隐函数的求导法可知,当  $g(y) \neq 0$  时,

$$
\Phi^ {\prime} (x) = \frac {F ^ {\prime} (x)}{G ^ {\prime} (y)} = \frac {f (x)}{g (y)},
$$

这就表示函数 $y = \Phi(x)$ 满足方程(2-5). 所以, 如果已分离变量的方程(2-5)中, $g(y)$ 和 $f(x)$ 是连续的, 且 $g(y) \neq 0$, 那么(2-5)式两端积分后得到的关系式(2-6), 就用隐式给出了方程(2-5)的解, (2-6)式就叫做微分方程(2-5)的隐式解. 又由于关系式(2-6)中含有任意常数, 因此(2-6)式所确定的隐函数是方程(2-5)的通解, 所以(2-6)式叫做微分方程(2-5)的隐式通解 (当 $f(x) \neq 0$ 时, (2-6)式所确定的隐函数 $x = \Psi(y)$ 也可认为是方程(2-5)的解).

例1 求微分方程

$$
\frac {\mathrm{d} y}{\mathrm{d} x} = 2 x y \tag {2-7}
$$

的通解.

解 方程(2-7)是可分离变量的,分离变量后得

$$
\frac {\mathrm{d} y}{y} = 2 x \mathrm{d} x,
$$

两端积分

$$
\int \frac {\mathrm{d} y}{y} = \int 2 x \mathrm{d} x,
$$

得

$$
\ln | y | = x ^ {2} + C _ {1},
$$

从而

$$
y = \pm \mathrm{e} ^ {x ^ {2} + C _ {1}} = \pm \mathrm{e} ^ {C _ {1}} \mathrm{e} ^ {x ^ {2}}.
$$

因 $\pm \mathrm{e}^{c_1}$ 是任意非零常数，又 $y\equiv 0$ 也是方程(2-7)的解，故得方程(2-7)的通解

$$
y = C \mathrm{e} ^ {x ^ {2}},
$$

其中 C 为任意常数.

例 2 放射性元素铀由于不断地有原子放射出微粒子而变成其他元素,铀的含量就不断减少,这种现象叫做衰变.由原子物理学知道,铀的衰变速度与当时未衰变的铀原子的含量 M 成正比.已知 t=0 时铀的含量为  $M_{0}$ , 求在衰变过程中铀含量  $M(t)$  随时间 t 变化的规律.

解 铀的衰变速度就是  $M(t)$  对时间 t 的导数  $\frac{dM}{dt}$ . 由于铀的衰变速度与其含量成正比, 故得微分方程

$$
\frac {\mathrm{d} M}{\mathrm{d} t} = - \lambda M, \tag {2-8}
$$

其中  $\lambda (\lambda > 0)$  是常数, 叫做衰变系数,  $\lambda$  前置负号是由于当 t 增加时 M 单调减少, 即  $\frac{dM}{dt} < 0$  的缘故.

按题意,初值条件为

$$
M \mid_ {t = 0} = M _ {0}.
$$

方程(2-8)是可分离变量的.分离变量后得

$$
\frac {\mathrm{d} M}{M} = - \lambda \mathrm{d} t.
$$

两端积分

$$
\int \frac {\mathrm{d} M}{M} = \int (- \lambda) \mathrm{d} t,
$$

以  $\ln C$  表示任意常数, 考虑到 M > 0, 得

$$
\ln M = - \lambda t + \ln C,
$$

即

$$
M = C \mathrm{e} ^ {- \lambda t}.
$$

这就是方程(2-8)的通解.以初值条件代入上式,得

$$
M _ {0} = C \mathrm{e} ^ {0} = C,
$$

所以

$$
M = M _ {0} \mathrm{e} ^ {- \lambda t},
$$

这就是所求铀的衰变规律.由此可见,铀的含量随时间的增加而按指数规律衰减(图7-1).

例 3 跳伞人从跳伞塔跳下后, 假设降落伞同时打开, 且所受空气阻力与速度成正比, 并设降落伞离开跳伞塔时  $(t=0)$  速度为零, 求降落伞下落速度与时间的函数关系.

![](images/page_313_chart_19.jpg)

<details>
<summary>line</summary>

| Time (t) | Value (M) |
| --- | --- |
| 0 | M0 |
| >0 | <M0 |
</details>

图7-1

解 设降落伞下落速度为  $v(t)$ . 降落伞在空中下落

时,同时受到重力 P 与阻力 R 的作用(图 7-2).重力大小为 mg,方向与 v 一致;阻力大小为 kv (k 为比例系数),方向与 v 相反,从而降落伞所受外力为

$$
F = m g - k v.
$$

根据牛顿第二运动定律

$$
F = m a
$$

(其中 a 为加速度), 得函数  $v(t)$  应满足的方程为

$$
m \frac {\mathrm{d} v}{\mathrm{d} t} = m g - k v. \tag {2-9}
$$

按题意,初值条件为

$$
v \mid_ {t = 0} = 0.
$$

方程(2-9)是可分离变量的.分离变量后得

$$
\frac {\mathrm{d} v}{m g - k v} = \frac {\mathrm{d} t}{m},
$$

两端积分

$$
\int \frac {\mathrm{d} v}{m g - k v} = \int \frac {\mathrm{d} t}{m},
$$

考虑到 mg-kv>0, 得

$$
- \frac {1}{k} \ln (m g - k v) = \frac {t}{m} + C _ {1},
$$

即

$$
m g - k v = \mathrm{e} ^ {- \frac {k}{m} t - k C _ {1}},
$$

或

$$
v = \frac {m g}{k} + C \mathrm{e} ^ {- \frac {k}{m} t} \quad \left(C = - \frac {\mathrm{e} ^ {- k C _ {1}}}{k}\right), \tag {2-10}
$$

这就是方程(2-9)的通解.

将初值条件 $v\mid_{t = 0} = 0$ 代入(2-10)式，得

$$
C = - \frac {m g}{k}.
$$

于是所求的特解为

$$
v = \frac {m g}{k} (1 - \mathrm{e} ^ {- \frac {k}{m} t}). \tag {2-11}
$$

由(2-11)可以看出,随着时间 t 的增大,速度 v 逐渐接近于常数  $\frac{mg}{k}$ ,且不会超过  $\frac{mg}{k}$ ,也就是说,跳伞后开始阶段是加速运动,但以后逐渐接近于等速运动.

例 4 有高为 1 m 的半球形容器, 水从它的底部小孔流出, 小孔横截面面积为  $1 \, cm^{2}$  (图 7-3). 开始时容器内盛满了水, 求水从小孔流出过程中容器里水面的高度 h (水面与孔口中心间的距离) 随时间 t 变化的规律, 并求水流完所需的时间.

解 由力学知道,水从孔口流出的流量(即通过孔口横截面的水的体积 V 对时间 t 的变化率)Q 可用下列公式计算:

![](images/page_314_image_23.jpg)

<details>
<summary>text_image</summary>

R=kv
P=mg
</details>

图7-2

$$
Q = \frac {\mathrm{d} V}{\mathrm{d} t} = k S \sqrt {2 g h}, \tag {2-12}
$$

其中 k 为流量系数,由实验测得 k=0.62, S 为孔口横截面面积, g 为重力加速度.

另一方面,设在微小时间间隔 $[t,t+dt]$ 内,水面高度由h降至 $h+\mathrm{d}h\left(\mathrm{d}h<0\right)$ ,则又可得到

$$
\mathrm{d} V = - \pi r ^ {2} \mathrm{d} h, \tag {2-13}
$$

其中 r 是时刻 t 时的水面半径(图 7-3)，右端置负号是由于 dh<0 而 dV>0 的缘故. 又因

$$
r = \sqrt {1 ^ {2} - (1 - h) ^ {2}} = \sqrt {2 h - h ^ {2}},
$$

所以(2-13)式变成

$$
\mathrm{d} V = - \pi (2 h - h ^ {2}) \mathrm{d} h. \tag {2-14}
$$

比较(2-12)和(2-14)两式,得

$$
k S \sqrt {2 g h} \mathrm{d} t = - \pi (2 h - h ^ {2}) \mathrm{d} h, \tag {2-15}
$$

这就是未知函数  $h=h(t)$  应满足的微分方程.

![](images/page_315_image_12.jpg)

<details>
<summary>text_image</summary>

h
h+dh
r
O
h
1 m
</details>

图7-3

此外,开始时容器内的水是满的,所以未知函数  $h=h(t)$  还应满足下列初值条件:

$$
h \mid_ {t = 0} = 1. \tag {2-16}
$$

方程(2-15)是可分离变量的.分离变量后得

$$
\mathrm{d} t = - \frac {\pi}{k S \sqrt {2 g}} (2 h ^ {\frac {1}{2}} - h ^ {\frac {3}{2}}) \mathrm{d} h.
$$

两端积分,得

$$
t = - \frac {\pi}{k S \sqrt {2 g}} \left(\frac {4}{3} h ^ {\frac {3}{2}} - \frac {2}{5} h ^ {\frac {5}{2}} + C\right), \tag {2-17}
$$

其中 C 是任意常数.

把初值条件(2-16)代入(2-17)式,得

$$
C = - \frac {4}{3} + \frac {2}{5} = - \frac {1 4}{1 5}.
$$

把所得的 C 值代入(2-17)式并化简,就得

$$
t = \frac {1 4 \pi}{1 5 k S \sqrt {2 g}} \left(1 - \frac {1 0}{7} h ^ {\frac {3}{2}} + \frac {3}{7} h ^ {\frac {5}{2}}\right).
$$

以 $k = 0.62, S = 10^{-4} \mathrm{~m}^2, g = 9.8 \mathrm{~m/s}^2$ 代入上式，计算后可得

$$
t = 1. 0 6 8 \times 1 0 ^ {4} \left(1 - \frac {1 0}{7} h ^ {\frac {3}{2}} + \frac {3}{7} h ^ {\frac {5}{2}}\right) \mathrm{s}.
$$

上式表达了水从小孔流出的过程中容器内水面高度 h 与时间 t 之间的函数关系.由此可知水流完所需的时间为

$$
t = 1. 0 6 8 \times 1 0 ^ {4} \mathrm{s} = 2 \mathrm{h} 5 8 \mathrm{min}.
$$

图

释疑解难

7-2

这里还要指出,在例4中我们是通过对微小量dV的分析得到微分方程(2-15)的.这种微小量分析的方法,也是建立微分方程的一种常用方法.

## 习题 7-2

1. 求下列微分方程的通解:

(1)  $xy'-y\ln y=0;$

(2) $3x^{2} + 5x - 5y' = 0$;

(3)  $\sqrt{1-x^{2}}y'=\sqrt{1-y^{2}}$ ;

(4) $y' - xy' = a(y^2 + y')$;

(5)  $\sec^{2}x \tan y dx + \sec^{2}y \tan x dy = 0;$

(6) $\frac{\mathrm{dy}}{\mathrm{dx}} = 10^{x + y}$;

(7) $(\mathrm{e}^{x + y} - \mathrm{e}^x)\mathrm{d}x + (\mathrm{e}^{x + y} + \mathrm{e}^y)\mathrm{d}y = 0;$

(8)  $\cos x \sin y dx + \sin x \cos y dy = 0;$

(9) $(y+1)^{2}\frac{\mathrm{d}y}{\mathrm{d}x}+x^{3}=0;$

(10) $y\mathrm{d}x + (x^2 - 4x)\mathrm{d}y = 0.$

2. 求下列微分方程满足所给初值条件的特解:

(1)  $y' = e^{2x - y}$ ,  $y \mid_{x=0} = 0;$

(2)  $\cos x \sin y \, dy = \cos y \sin x \, dx, y \mid_{x=0} = \frac{\pi}{4};$

(3)  $y'\sin x = y \ln y, y \mid_{x = \frac{\pi}{2}} = e;$

(4)  $\cos y\mathrm{d}x+(1+\mathrm{e}^{-x})\sin y\mathrm{d}y=0,y\mid_{x=0}=\frac{\pi}{4};$

(5)  $x \, dy + 2y \, dx = 0, y \mid_{x=2} = 1;$

(6) $\frac{1}{\rho}\frac{\mathrm{d}\rho}{\mathrm{d}\theta}+\frac{\rho^{2}+1}{\rho^{2}-1}\cot\theta=0,\rho\mid_{\theta=\frac{\pi}{6}}=3;$

(7) $x^{2}(1+y'^{2})=a^{2},y\mid_{x=a}=0$ ,其中a>0.

3. 有一盛满了水的圆锥形漏斗, 高为 $10 \mathrm{~cm}$, 顶角为 $60^{\circ}$, 漏斗下面有面积为 $0.5 \mathrm{~cm}^{2}$ 的孔, 求水面高度变化的规律及水流完所需的时间.

4. 质量为 1 g 的质点受外力作用做直线运动, 这外力和时间成正比, 和质点运动的速度成反比. 在  $t = 10 \, s$  时, 速度等于  $50 \, cm/s$ , 外力为  $4 \, g \cdot cm/s^{2}$ , 问从运动开始经过了  $1 \, min$  后的速度是多少?

5. 镭的衰变有如下的规律: 镭的衰变速度与它的现存量 R 成正比. 由经验材料得知, 镭经过 1600 年后, 只余原始量  $R_{0}$  的一半. 试求镭的现存量 R 与时间 t 的函数关系.

6. 一曲线通过点(2,3)，它在两坐标轴间的任一切线线段均被切点所平分，求这曲线方程.

7. 小船从河边点 O 处出发驶向对岸(两岸为平行直线). 设船速为 a, 小船航行的方向始终与河岸垂直, 又设河宽为 h, 河中任一点处的水流速度与该点到两岸距离的乘积成正比(比例系数为 k). 求小船的航行路线.

## 第三节 齐次方程

## 一、齐次方程

如果一阶微分方程可化成

$$
\frac {\mathrm{d} y}{\mathrm{d} x} = \varphi \left(\frac {y}{x}\right) \tag {3-1}
$$

的形式,那么就称这方程为齐次方程,例如

$$
(x y - y ^ {2}) \mathrm{d} x - (x ^ {2} - 2 x y) \mathrm{d} y = 0
$$

是齐次方程,因为它可化成

$$
\frac {\mathrm{d} y}{\mathrm{d} x} = \frac {x y - y ^ {2}}{x ^ {2} - 2 x y},
$$

即

$$
\frac {\mathrm{d} y}{\mathrm{d} x} = \frac {\frac {y}{x} - \left(\frac {y}{x}\right) ^ {2}}{1 - 2 \left(\frac {y}{x}\right)}.
$$

在齐次方程

$$
\frac {\mathrm{d} y}{\mathrm{d} x} = \varphi \left(\frac {y}{x}\right)
$$

中,引进新的未知函数

$$
u = \frac {y}{x}, \tag {3-2}
$$

就可把它化为可分离变量的方程. 因为由(3-2)有

$$
y = u x, \quad \frac {\mathrm{d} y}{\mathrm{d} x} = u + x \frac {\mathrm{d} u}{\mathrm{d} x},
$$

代入方程(3-1)，便得方程

$$
u + x \frac {\mathrm{d} u}{\mathrm{d} x} = \varphi (u),
$$

即

$$
x \frac {\mathrm{d} u}{\mathrm{d} x} = \varphi (u) - u.
$$

分离变量,得

$$
\frac {\mathrm{d} u}{\varphi (u) - u} = \frac {\mathrm{d} x}{x}.
$$

两端积分,得

$$
\int \frac {\mathrm{d} u}{\varphi (u) - u} = \int \frac {\mathrm{d} x}{x}.
$$

求出积分后,再以 $\frac{y}{x}$ 代替u,便得所给齐次方程的通解.

例1 解方程

$$
y ^ {2} + x ^ {2} \frac {\mathrm{d} y}{\mathrm{d} x} = x y \frac {\mathrm{d} y}{\mathrm{d} x}.
$$

解 原方程可写成

$$
\frac {\mathrm{d} y}{\mathrm{d} x} = \frac {y ^ {2}}{x y - x ^ {2}} = \frac {\left(\frac {y}{x}\right) ^ {2}}{\frac {y}{x} - 1},
$$

因此是齐次方程.令 $\frac{y}{x}=u$ ,则

$$
y = x u, \quad \frac {\mathrm{d} y}{\mathrm{d} x} = u + x \frac {\mathrm{d} u}{\mathrm{d} x},
$$

于是原方程变为

$$
u + x \frac {\mathrm{d} u}{\mathrm{d} x} = \frac {u ^ {2}}{u - 1},
$$

即

$$
x \frac {\mathrm{d} u}{\mathrm{d} x} = \frac {u}{u - 1}.
$$

分离变量,得

$$
\left(1 - \frac {1}{u}\right) \mathrm{d} u = \frac {\mathrm{d} x}{x}.
$$

两端积分,得

$$
u - \ln | u | + C _ {1} = \ln | x |,
$$

或写为

$$
\ln | x u | = u + C _ {1}.
$$

以 $\frac{y}{x}$ 代上式中的u,便得所给方程的通解为

$$
\ln | y | = \frac {y}{x} + C _ {1} \quad \text {或} \quad y = C \mathrm{e} ^ {\frac {y}{x}} (C = \pm \mathrm{e} ^ {C _ {1}}).
$$

例 2 探照灯的聚光镜的镜面是一张旋转曲面, 它的形状由 xOy 坐标面上的一条曲线 L 绕 x 轴旋转而成. 按聚光镜性能的要求, 在其旋转轴 (x 轴) 上一点 O 处发出的一切光线, 经它反射后都与旋转轴平行. 求曲线 L 的方程.

解 将光源所在之 $O$ 点取作坐标原点（图7-4），且曲线 $L$ 位于 $y \geqslant 0$ 范围内.

![](images/page_319_image_3.jpg)

<details>
<summary>text_image</summary>

y
T
L
M
α
S
α
A
O
P
N
x
</details>

图7-4

设点 $M(x,y)$ 为 $L$ 上的任一点，点 $O$ 发出的某条光线

经点 $M$ 反射后是一条与 $x$ 轴平行的直线 $MS$. 又设过点 $M$ 的切线 $AT$ 与 $x$ 轴的夹角为 $\alpha$. 根据题意, $\angle SMT = \alpha$. 另一方面, $\angle OMA$ 是入射角的余角, $\angle SMT$ 是反射角的余角, 于是由光学中的反射定律有 $\angle OMA = \angle SMT = \alpha$. 从而 $AO = OM$, 但 $AO = AP - OP = PM\cot \alpha - OP = \frac{y}{y'} - x$, 而 $OM = \sqrt{x^2 + y^2}$. 于是得微分方程

$$
\frac {y}{y ^ {\prime}} - x = \sqrt {x ^ {2} + y ^ {2}}.
$$

把 $x$ 看作因变量, $y$ 看作自变量, 当 $y > 0$ 时, 上式即为

$$
\frac {\mathrm{d} x}{\mathrm{d} y} = \frac {x}{y} + \sqrt {\left(\frac {x}{y}\right) ^ {2} + 1},
$$

这是齐次方程. 令 $\frac{x}{y} = v$，则 $x = yv, \frac{\mathrm{d}x}{\mathrm{d}y} = v + y\frac{\mathrm{d}v}{\mathrm{d}y}$，代入上式，得

$$
v + y \frac {\mathrm{d} v}{\mathrm{d} y} = v + \sqrt {v ^ {2} + 1},
$$

即

$$
y \frac {\mathrm{d} v}{\mathrm{d} y} = \sqrt {v ^ {2} + 1}.
$$

分离变量,得

$$
\frac {\mathrm{d} v}{\sqrt {v ^ {2} + 1}} = \frac {\mathrm{d} y}{y}.
$$

积分,得

$$
\ln (v + \sqrt {v ^ {2} + 1}) = \ln y - \ln C,
$$

或

$$
v + \sqrt {v ^ {2} + 1} = \frac {y}{C}.
$$

由

$$
\left(\frac {y}{C} - v\right) ^ {2} = v ^ {2} + 1,
$$