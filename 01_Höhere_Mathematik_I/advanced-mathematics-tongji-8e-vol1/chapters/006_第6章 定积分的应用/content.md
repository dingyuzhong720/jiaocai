# 第6章 定积分的应用

原始 PDF 第 284–305 页。

## 第六章

## 定积分的应用

本章中我们将应用前面学过的定积分理论来分析和解决一些几何、物理中的问题,其目的不仅在于建立计算这些几何、物理量的公式,更重要的还在于介绍运用元素法将一个量表达成为定积分的分析方法.

## 第一节 定积分的元素法

在定积分的应用中,经常采用所谓元素法.为了说明这种方法,我们先回顾一下第五章中讨论过的曲边梯形的面积问题.

设 $f(x)$ 在区间 $[a, b]$ 上连续且 $f(x) \geqslant 0$，求以曲线 $y = f(x)$ 为曲边、底为 $[a, b]$ 的曲边梯形的面积 $A$. 把这个面积 $A$ 表示为定积分

$$
A = \int_ {a} ^ {b} f (x) \mathrm{d} x
$$

的步骤是

（1）用任意一组分点把区间 $[a, b]$ 分成长度为 $\Delta x_{i} (i = 1,2,\dots,n)$ 的 $n$ 个小区间，相应地把曲边梯形分成 $n$ 个窄曲边梯形，第 $i$ 个窄曲边梯形的面积设为 $\Delta A_{i}$，于是有

$$
A = \sum_ {i = 1} ^ {n} \Delta A _ {i};
$$

(2) 计算  $\Delta A_{i}$  的近似值

$$
\Delta A _ {i} \approx f (\xi_ {i}) \Delta x _ {i} \quad (x _ {i - 1} \leqslant \xi_ {i} \leqslant x _ {i});
$$

(3) 求和, 得 A 的近似值

$$
A \approx \sum_ {i = 1} ^ {n} f (\xi_ {i}) \Delta x _ {i};
$$

(4) 求极限, 记  $\lambda = \max\{\Delta x_{1}, \Delta x_{2}, \cdots, \Delta x_{n}\}$ , 得

267

---

第六章 定积分的应用

$$
A = \lim _ {\lambda \to 0} \sum_ {i = 1} ^ {n} f (\xi_ {i}) \Delta x _ {i} = \int_ {a} ^ {b} f (x) \mathrm{d} x.
$$

在上述问题中我们注意到,所求量(即面积 A)与区间  $[a, b]$  有关.如果把区间  $[a, b]$  分成许多部分区间,那么所求量相应地分成许多部分量(即  $\Delta A_{i}$ ),而所求量等于所有部分量之和(即  $A = \sum_{i=1}^{n} \Delta A_{i}$ ),这一性质称为所求量对于区间  $[a, b]$  具有可加性.此外,以  $f(\xi_{i}) \Delta x_{i}$  近似代替部分量  $\Delta A_{i}$  时,要求它们只相差一个比  $\Delta x_{i}$  高阶的无穷小,以使和式  $\sum_{i=1}^{n} f(\xi_{i}) \Delta x_{i}$  的极限是 A 的精确值,从而 A 可以表示为定积分

$$
A = \int_ {a} ^ {b} f (x)   \mathrm{d} x.
$$

在引出 A 的积分表达式的四个步骤中, 主要的是第二步, 这一步是要确定  $\Delta A_{i}$  的近似值  $f(\xi_{i})\Delta x_{i}$ , 使得

$$
A = \lim _ {\lambda \to 0} \sum_ {i = 1} ^ {n} f (\xi_ {i}) \Delta x _ {i} = \int_ {a} ^ {b} f (x) \mathrm{d} x.
$$

在实用上,为了简便起见,省略下标 i,用  $\Delta A$  表示任一小区间  $[x, x + dx]$  上的窄曲边梯形的面积,这样,

$$
A = \sum \Delta A.
$$

取 $[x,x+dx]$ 的左端点x为 $\xi$ ，以点x处的函数值 $f(x)$ 为高、dx为底的矩形的面积 $f(x)\mathrm{d}x$ 为 $\Delta A$ 的近似值（如图6-1阴影部分所示），即

$$
\Delta A \approx f (x)   \mathrm{d} x.
$$

上式右端 $f(x)\mathrm{d}x$ 叫做面积元素，记为 $\mathrm{dA} = f(x)\mathrm{dx}$ 于是

$$
A \approx \sum f (x) \mathrm{d} x,
$$

![](../../raw/pages_0257-0288/images/page_284_image_12.jpg)

<details>
<summary>text_image</summary>

y
y=f(x)
f(x)
dA
x x+dx
O a b x
</details>

图6-1

因此

$$
A = \lim \sum f (x)   \mathrm{d} x = \int_ {a} ^ {b} f (x)   \mathrm{d} x.
$$

一般地,如果某一实际问题中的所求量 U 符合下列条件:

(1) U 是与一个变量 x 的变化区间  $[a, b]$  有关的量；
(2) U 对于区间  $[a, b]$  具有可加性, 就是说, 如果把区间  $[a, b]$  分成许多部分区间, 那么 U 相应地分成许多部分量, 而 U 等于所有部分量之和;
(3) 部分量  $\Delta U_{i}$  的近似值可表示为  $f(\xi_{i})\Delta x_{i}$ ,

那么就可考虑用定积分来表达这个量 $U$. 通常写出这个量 $U$ 的积分表达式的步骤是

1）根据问题的具体情况，选取一个变量例如 x 为积分变量，并确定它的变化区间

268

---

第二节 定积分在几何学上的应用

$[a,b]$ ;

2）设想把区间 $[a, b]$ 分成 $n$ 个小区间，取其中任一小区间并记作 $[x, x + \mathrm{d}x]$，求出相应于这个小区间的部分量 $\Delta U$ 的近似值。如果 $\Delta U$ 能近似地表示为 $[a, b]$ 上的一个连续函数在 $x$ 处的值 $f(x)$ 与 $\mathrm{d}x$ 的乘积①，就把 $f(x) \mathrm{d}x$ 称为量 $U$ 的元素且记作 $\mathrm{d}U$，即

$$
\mathrm{d} U = f (x) \mathrm{d} x;
$$

3）以所求量 $U$ 的元素 $f(x)\mathrm{d}x$ 为被积表达式，在区间 $[a,b]$ 上作定积分，得

$$
U = \int_ {a} ^ {b} f (x)   \mathrm{d} x.
$$

这就是所求量 U 的积分表达式.

这个方法通常叫做元素法.下面两节中我们将应用这个方法来讨论几何、物理中的一些问题.

## 第二节 定积分在几何学上的应用

## 一、平面图形的面积

## 1. 直角坐标情形

在第五章中我们已经知道,由曲线  $y=f(x)\quad(f(x)\geqslant0)$  及直线 x=a,x=b (a<b) 与 x 轴所围成的曲边梯形的面积 A 是定积分

$$
A = \int_ {a} ^ {b} f (x)   \mathrm{d} x,
$$

其中被积表达式 $f(x)\mathrm{d}x$ 就是直角坐标下的面积元素,它表示高为 $f(x)$ 、底为 dx 的一个矩形面积.

应用定积分,不但可以计算曲边梯形面积,还可以计算一些比较复杂的平面图形的面积.

例 1 计算由两条抛物线:  $y^{2}=x, y=x^{2}$  所围成的图形的面积.

解 这两条抛物线所围成的图形如图 6-2 所示.为了具体定出图形的所在范围,先求出这两条抛物线的交点.为此,解方程组

![](../../raw/pages_0257-0288/images/page_285_chart_17.jpg)

<details>
<summary>area</summary>

| Point | X | Y |
| --- | --- | --- |
| Intersection (x+dx) | 1 | 1 |
</details>

图6-2

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 这里  $\Delta U$  与  $f(x)\mathrm{d}x$  相差一个比 dx 高阶的无穷小.</span></small>

269

---

第六章 定积分的应用

$$
\left\{ \begin{array}{l} y ^ {2} = x, \\ y = x ^ {2}, \end{array} \right.
$$

得到两个解

$$
x = 0, y = 0 \quad {\text {及}} \quad x = 1, y = 1.
$$

即这两抛物线的交点为(0,0)及(1,1)，从而知道这图形在直线 $x = 0$ 与 $x = 1$ 之间.

取横坐标 $x$ 为积分变量, 它的变化区间为 $[0,1]$. 相应于 $[0,1]$ 上的任一小区间 $[x, x + \mathrm{d}x]$ 的窄条的面积近似于高为 $\sqrt{x} - x^2$、底为 $\mathrm{d}x$ 的窄矩形的面积, 从而得到面积元素

$$
\mathrm{d} A = (\sqrt {x} - x ^ {2}) \mathrm{d} x.
$$

以 $(\sqrt{x}-x^{2})\mathrm{d}x$ 为被积表达式,在闭区间[0,1]上作定积分,便得所求面积为

$$
A = \int_ {0} ^ {1} (\sqrt {x} - x ^ {2}) \mathrm{d} x = \left[ \frac {2}{3} x ^ {\frac {3}{2}} - \frac {x ^ {3}}{3} \right] _ {0} ^ {1} = \frac {1}{3}.
$$

例 2 计算抛物线  $y^{2}=2x$  与直线 y=x-4 所围成的图形的面积.

解 这个图形如图 6-3 所示.为了定出这图形所在的范围,先求出所给抛物线和直线的交点.解方程组

$$
\left\{ \begin{array}{l} y ^ {2} = 2 x, \\ y = x - 4, \end{array} \right.
$$

得交点(2,-2)和(8,4)，从而知道这图形在直线 $y = -2$ 及 $y = 4$ 之间.

现在,选取纵坐标 y 为积分变量,它的变化区间为  $[-2,4]$  (读者可以思考一下,取横坐标 x 为积分

![](../../raw/pages_0257-0288/images/page_286_chart_14.jpg)

<details>
<summary>contour</summary>

| Point | x-coordinate | y-coordinate |
| --- | --- | --- |
| Intersection of y=x-4 and y=dy | 8 | 4 |
| Intersection of y=dy and y=x-4 | 2 | -2 |
</details>

图6-3

变量,有什么不方便的地方).相应于 $[-2,4]$ 上任一小区间 $[y,y+dy]$ 的窄条面积近似于高为dy、底为 $(y+4)-\frac{1}{2}y^{2}$ 的窄矩形的面积,从而得到面积元素

$$
\mathrm{d} A = \left(y + 4 - \frac {1}{2} y ^ {2}\right) \mathrm{d} y.
$$

以 $\left(y+4-\frac{1}{2}y^{2}\right)dy$ 为被积表达式,在闭区间 $[-2,4]$ 上作定积分,便得所求的面积为

$$
A = \int_ {- 2} ^ {4} \left(y + 4 - \frac {1}{2} y ^ {2}\right) \mathrm{d} y = \left[ \frac {y ^ {2}}{2} + 4 y - \frac {y ^ {3}}{6} \right] _ {- 2} ^ {4} = 1 8.
$$

由例 2 可以看到, 积分变量选得适当, 可使计算方便.

例3 求椭圆 $\frac{x^2}{a^2} +\frac{y^2}{b^2} = 1$ 所围成的图形的面积.

270

---

第二节 定积分在几何学上的应用

解 该椭圆关于两坐标轴都对称(图6-4)，所以椭圆所围成的图形的面积为

$$
A = 4 A _ {1},
$$

其中  $A_{1}$  为该椭圆在第一象限部分与两坐标轴所围图形的面积, 因此

$$
A = 4 A _ {1} = 4 \int_ {0} ^ {a} y \mathrm{d} x.
$$

利用椭圆的参数方程

$$
\left\{ \begin{array}{l l} x = a \cos t, \\ y = b \sin t \end{array} \right. \quad \left(0 \leqslant t \leqslant \frac {\pi}{2}\right),
$$

应用定积分换元法,令  $x = a \cos t$ , 则

$$
y = b \sin t, \quad \mathrm{d} x = - a \sin t \mathrm{d} t.
$$

![](../../raw/pages_0257-0288/images/page_287_image_9.jpg)

<details>
<summary>text_image</summary>

y
b
O x x+dx a x
</details>

图6-4

当 $x$ 由0变到 $a$ 时，$t$ 由 $\frac{\pi}{2}$ 变到0，所以

$$
\begin{array}{l} A = 4 \int_ {\frac {\pi}{2}} ^ {0} b \sin t (- a \sin t) \mathrm{d} t = - 4 a b \int_ {\frac {\pi}{2}} ^ {0} \sin^ {2} t \mathrm{d} t \\ = 4 a b \int_ {0} ^ {\frac {\pi}{2}} \sin^ {2} t \mathrm{d} t = 4 a b \cdot \frac {1}{2} \cdot \frac {\pi}{2} = \pi a b. \\ \end{array}
$$

当 a=b 时, 就得到大家所熟悉的圆面积的公式  $A=\pi a^{2}$ .

## 2. 极坐标情形

某些平面图形,用极坐标来计算它们的面积比较方便.

设由曲线 $\rho = \rho (\theta)$ 及射线 $\theta = \alpha ,\theta = \beta$ 围成一图形（简称为曲边扇形），现在要计算它的面积(图6-5).这里， $\rho (\theta)$ 在 $[\alpha ,\beta ]$ 上连续，且 $\rho (\theta)\geqslant 0,0 <   \beta -\alpha \leqslant 2\pi .$

由于当  $\theta$  在  $[\alpha, \beta]$  上变动时, 极径  $\rho = \rho(\theta)$  也随之变动, 因此所求图形的面积不能直接利用扇形面积的公式  $A = \frac{1}{2} R^{2} \theta$  来计算.

![](../../raw/pages_0257-0288/images/page_287_image_18.jpg)

<details>
<summary>text_image</summary>

ρ=ρ(θ)
dθ
α β θ θ+dθ
O A
</details>

图6-5

取极角 $\theta$ 为积分变量，它的变化区间为 $[\alpha, \beta]$. 相应于任一小区间 $[\theta, \theta + \mathrm{d}\theta]$ 的窄曲边扇形的面积可以用半径为 $\rho = \rho(\theta)$、中心角为 $\mathrm{d}\theta$ 的扇形的面积来近似代替，从而得到这窄曲边扇形面积的近似值，即曲边扇形的面积元素

$$
\mathrm{d} A = \frac {1}{2} [ \rho (\theta) ] ^ {2} \mathrm{d} \theta .
$$

以 $\frac{1}{2} [\rho (\theta)]^2\mathrm{d}\theta$ 为被积表达式，在闭区间 $[\alpha ,\beta ]$ 上作定积分，便得所求曲边扇形的面

271

---

第六章 定积分的应用

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

![](../../raw/pages_0289-0320/images/page_288_image_10.jpg)

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

![](../../raw/pages_0289-0320/images/page_288_image_18.jpg)

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

272

---

第二节 定积分在几何学上的应用

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

![](../../raw/pages_0289-0320/images/page_289_image_9.jpg)

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

![](../../raw/pages_0289-0320/images/page_289_image_16.jpg)

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

273

---

第六章 定积分的应用

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

![](../../raw/pages_0289-0320/images/page_290_image_15.jpg)

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

274

---

第二节 定积分在几何学上的应用

$$
= \pi a ^ {3} \int_ {0} ^ {2 \pi} (1 - 3 \cos t + 3 \cos^ {2} t - \cos^ {3} t) \mathrm{d} t = 5 \pi^ {2} a ^ {3}.
$$

所述图形绕 $y$ 轴旋转而成的旋转体的体积可看成平面图形OABC与OBC（图6-12)分别绕 $y$ 轴旋转而成的旋转体的体积之差.因此所求的体积为

$$
\begin{array}{l} V _ {y} = \int_ {0} ^ {2 a} \pi x _ {2} ^ {2} (y) \mathrm{d} y - \int_ {0} ^ {2 a} \pi x _ {1} ^ {2} (y) \mathrm{d} y \\ = \pi \int_ {2 \pi} ^ {\pi} a ^ {2} (t - \sin t) ^ {2} \cdot a \sin t \mathrm{d} t - \pi \int_ {0} ^ {\pi} a ^ {2} (t - \sin t) ^ {2} \cdot a \sin t \mathrm{d} t \\ = - \pi a ^ {3} \int_ {0} ^ {2 \pi} (t - \sin t) ^ {2} \sin t \mathrm{d} t = 6 \pi^ {3} a ^ {3}. \\ \end{array}
$$

![](../../raw/pages_0289-0320/images/page_291_image_4.jpg)

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

![](../../raw/pages_0289-0320/images/page_291_chart_6.jpg)

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

#

例题精讲

6-2

275

---

第六章 定积分的应用

![](../../raw/pages_0289-0320/images/page_292_image_1.jpg)

<details>
<summary>text_image</summary>

A(x)
O a x x+dx b x
</details>

图6-13

![](../../raw/pages_0289-0320/images/page_292_image_3.jpg)

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

![](../../raw/pages_0289-0320/images/page_292_image_9.jpg)

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

我们知道,圆的周长可以利用圆的内接正多边形的周长当边数无限增多时的极限来确定.现在用类似的方法来建立平面的连续曲线弧长的概念,从而应用定积分来计

276

---

第二节 定积分在几何学上的应用

算弧长.

设 A, B 是曲线弧的两个端点. 在弧  $\widehat{AB}$  上依次任取分点  $A = M_{0}, M_{1}, M_{2}, \cdots, M_{i-1}$ ,

$M_{i},\cdots,M_{n-1},M_{n}=B$ ，并依次连接相邻的分点得一折线（图6-16）。当分点的数目无限增加且每个小段 $\widehat{M_{i-1}M_{i}}$ 都缩向一点时，如果此折线的长 $\sum_{i=1}^{n}|M_{i-1}M_{i}|$ 的极限存在，那么称此极限为曲线弧 $\widehat{AB}$ 的弧长，并称此曲线弧 $\widehat{AB}$ 是可求长的。

对光滑的曲线弧(参看第165页上的脚注),有如下结论:

![](../../raw/pages_0289-0320/images/page_293_chart_5.jpg)

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

277

---

第六章 定积分的应用

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

![](../../raw/pages_0289-0320/images/page_294_chart_15.jpg)

<details>
<summary>area</summary>

| X | Y |
| --- | --- |
| a | 2/3 |
| b | 3/2 |
</details>

图6-17

![](../../raw/pages_0289-0320/images/page_294_image_17.jpg)

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

278

---

第二节 定积分在几何学上的应用

从而,所求弧长

$$
s = \int_ {0} ^ {2 \pi} 2 a \sin \frac {\theta}{2} \mathrm{d} \theta = 2 a \left[ - 2 \cos \frac {\theta}{2} \right] _ {0} ^ {2 \pi} = 8 a.
$$

例 13 求阿基米德螺线  $\rho = a\theta (a > 0)$  相应于  $0 \leqslant \theta \leqslant 2\pi$  一段(图 6-19) 的弧长.

解 弧长元素为

$$
\mathrm{d} s = \sqrt {a ^ {2} \theta^ {2} + a ^ {2}} \mathrm{d} \theta = a \sqrt {1 + \theta^ {2}} \mathrm{d} \theta ,
$$

![](../../raw/pages_0289-0320/images/page_295_image_6.jpg)

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

![](../../raw/pages_0289-0320/images/page_295_image_10.jpg)

例题精讲

6-3

## 习题6-2

1. 求图 6-20 中各阴影部分的面积.

![](../../raw/pages_0289-0320/images/page_295_image_15.jpg)

<details>
<summary>text_image</summary>

y
y=√x
y=x
O
x
</details>

(1)

![](../../raw/pages_0289-0320/images/page_295_image_17.jpg)

<details>
<summary>text_image</summary>

y
y=e
y=e^x
O
x
</details>

(2)

![](../../raw/pages_0289-0320/images/page_295_image_19.jpg)

<details>
<summary>text_image</summary>

y
y=2x
y=3-x²
O
x
</details>

(3)

![](../../raw/pages_0289-0320/images/page_295_image_21.jpg)

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

279

---

第六章 定积分的应用

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

![](../../raw/pages_0289-0320/images/page_296_chart_25.jpg)

<details>
<summary>area</summary>

| X | Y |
| --- | --- |
| 1 | 0 |
| \(\xi\) | 1 |
| e | 1 |
</details>

图6-21

![](../../raw/pages_0289-0320/images/page_296_image_27.jpg)

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

![](../../raw/pages_0289-0320/images/page_296_image_29.jpg)

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

280

---

第二节 定积分在几何学上的应用

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

![](../../raw/pages_0289-0320/images/page_297_image_16.jpg)

<details>
<summary>text_image</summary>

y
O
R
x
</details>

图6-24

![](../../raw/pages_0289-0320/images/page_297_image_18.jpg)

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

281

---

第六章 定积分的应用

![](../../raw/pages_0289-0320/images/page_298_image_1.jpg)

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

![](../../raw/pages_0289-0320/images/page_298_image_3.jpg)

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

解 在上述移动过程中,电场对这单位正电荷的作用力是变的.取 r 为积分变量,它的变化区间为  $[a, b]$ .设

![](../../raw/pages_0289-0320/images/page_298_image_18.jpg)

图6-28

282

---

第三节 定积分在物理学上的应用

$[r, r + \mathrm{d}r]$ 为 $[a, b]$ 上的任一小区间. 当单位正电荷从 $r$ 移动到 $r + \mathrm{d}r$ 时, 电场力对它所做的功近似于 $\frac{kq}{r^2}\mathrm{d}r$, 即功元素为

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

![](../../raw/pages_0289-0320/images/page_299_image_8.jpg)

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

283

---

第六章 定积分的应用

$$
W = \int_ {a} ^ {b} \frac {k}{x} \mathrm{d} x = k \left[ \ln x \right] _ {a} ^ {b} = k \ln \frac {b}{a}.
$$

下面再举一个计算功的例子,它虽不是一个变力做功问题,但也可用积分来计算.

例 3 一圆柱形的贮水桶高为 5 m, 底圆半径为 3 m, 桶内盛满了水. 试问要把桶内的水全部吸出需做多少功?

解 作 $x$ 轴如图6-30所示.取深度 $x$ （单位为 $\mathrm{m}$ ）为积分变量，它的变化区间为[0,5].相应于[0,5]上任一小区间 $[x,x + \mathrm{d}x]$ 的一薄层水的高度为 $\mathrm{dx}$，若重力加速度 $g$ 取 $9.8\mathrm{m / s^2}$，则这薄层水所受重力为 $9.8\pi \cdot 3^{2}\mathrm{dx}$ kN.把这薄层水吸出桶外需做的功近似地为

$$
\mathrm{d} W = 8 8. 2 \pi x \mathrm{d} x,
$$

![](../../raw/pages_0289-0320/images/page_300_image_6.jpg)

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

![](../../raw/pages_0289-0320/images/page_300_image_15.jpg)

图6-31

解 桶的一个端面是圆片,所以现在要计算的是当水平面通过圆心时,铅直放置的一个半圆片的一侧所受到的水压力.

284

---

第三节 定积分在物理学上的应用

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

![](../../raw/pages_0289-0320/images/page_301_image_12.jpg)

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

285

---

第六章 定积分的应用

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

286

---

总习题六

m 的质点 M, 试求这细棒对质点 M 的引力.

11. 设有一半径为 $R$ 、圆心角为 $\varphi$ 的圆弧形细棒，其线密度为常数 $\mu$. 在圆心处有一质量为 $m$ 的质点 $M$. 试求这细棒对质点 $M$ 的引力.

## 总习题六

1. 填空:

(1) 曲线  $y = x^{3} - 5x^{2} + 6x$  与 x 轴所围成的图形的面积 A = \_\_\_\_;
(2) 曲线  $y=\frac{\sqrt{x}}{3}(3-x)$  上相应于  $1 \leqslant x \leqslant 3$  的一段弧的长度 s= \_\_\_\_.

2. 以下三题中均给出了四个结论,从中选出一个正确的结论:

（1）设 x 轴上有一长度为 l、线密度为常数  $\mu$  的细棒，在与细棒右端的距离为 a 处有一质量为 m 的质点 M（图 6-33），已知引力常量为 G，则质点 M 与细棒之间的引力的大小为（）；

![](../../raw/pages_0289-0320/images/page_303_image_10.jpg)

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

![](../../raw/pages_0289-0320/images/page_303_image_22.jpg)

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

287

---

第六章 定积分的应用

P, 所对应的面积 A 和 B 恒相等, 求曲线 C 的方程.

6. 设抛物线  $y=ax^{2}+bx+c$  ( $a\neq0$ ) 通过点(0,0)，且当  $x\in[0,1]$  时， $y\geqslant0$ 。试确定 a,b,c 的值，使得抛物线  $y=ax^{2}+bx+c$  与直线 x=1，y=0 所围图形的面积为  $\frac{4}{9}$ ，且使该图形绕 x 轴旋转而成的旋转体的体积最小。
7. 过坐标原点作曲线  $y=\ln x$  的切线, 该切线与曲线  $y=\ln x$  及 x 轴围成平面图形 D.

![](../../raw/pages_0289-0320/images/page_304_image_5.jpg)

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

![](../../raw/pages_0289-0320/images/page_304_image_22.jpg)

第六章释疑解难

![](../../raw/pages_0289-0320/images/page_304_image_24.jpg)

第六章例题精讲

288
