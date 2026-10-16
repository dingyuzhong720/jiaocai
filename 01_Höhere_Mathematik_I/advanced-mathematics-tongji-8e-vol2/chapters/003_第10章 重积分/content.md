# 第10章 重积分

原始 PDF 第 137–186 页。

# 第十章

# 重积分

本章和下一章是多元函数积分学的内容.在一元函数积分学中我们知道,定积分是某种确定形式的和的极限.这种和的极限的概念推广到定义在区域、曲线及曲面上的多元函数的情形,便得到重积分、曲线积分及曲面积分的概念.本章将介绍重积分(包括二重积分和三重积分)的概念、计算方法以及它们的一些应用.

## 第一节 二重积分的概念与性质

## 一、二重积分的概念

## 1. 曲顶柱体的体积

设有一立体,它的底是xOy面上的闭区域 $D^{①}$ ,它的侧面是以D的边界曲线为准

线而母线平行于 $z$ 轴的柱面, 它的顶是曲面 $z = f(x, y)$, 这里 $f(x, y) \geqslant 0$ 且在 $D$ 上连续 (图10-1). 这种立体叫做曲顶柱体. 现在我们来讨论如何定义并计算上述曲顶柱体的体积 $V$.

我们知道,平顶柱体的高是不变的,它的体积可以用公式

$$
\text {体积} = \text {高} \times \text {底面积}
$$

来定义和计算.关于曲顶柱体,当点 $(x,y)$ 在区域D上变

![](../../raw/pages_0129-0160/images/page_136_image_11.jpg)

<details>
<summary>text_image</summary>

z
z=f(x,y)
O
y
D
x
</details>

图10-1

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 为简便起见,本章以后除特别说明者外,都假定平面闭区域和空间闭区域是有界的,且平面闭区域有有限面积,空间闭区域有有限体积.</span></small>

130

---

第一节 二重积分的概念与性质

动时,高度 $f(x,y)$ 是个变量,因此它的体积不能直接用上式来定义和计算.但如果回忆起第五章中求曲边梯形面积的问题,就不难想到,那里所采用的解决办法,原则上可以用来解决目前的问题.

首先,用一组曲线网把 D 分成 n 个小闭区域

$$
\Delta \sigma_ {1}, \Delta \sigma_ {2}, \dots , \Delta \sigma_ {n}.
$$

分别以这些小闭区域的边界曲线为准线,作母线平行于z轴的柱面,这些柱面把原来的曲顶柱体分为n个细曲顶柱体.当这些小闭区域的直径①很小时,由于 $f(x,y)$ 连续,对同一个小闭区域来说, $f(x,y)$ 变化很小,这时细曲顶柱体可近似看做平顶柱体.我们

在每个  $\Delta\sigma_{i}$  （这个小闭区域的面积也记作  $\Delta\sigma_{i}$ ）中任取一点  $(\xi_{i},\eta_{i})$ ，以  $f(\xi_{i},\eta_{i})$  为高而底为  $\Delta\sigma_{i}$  的平顶柱体（图10-2）的体积为

$$
f (\xi_ {i}, \eta_ {i}) \Delta \sigma_ {i} \quad (i = 1, 2, \dots , n).
$$

这 $n$ 个平顶柱体体积之和

$$
\sum_ {i = 1} ^ {n} f (\xi_ {i}, \eta_ {i}) \Delta \sigma_ {i}
$$

可以认为是整个曲顶柱体体积的近似值.令 n 个小闭区域的直径中的最大值(记作  $\lambda$ ) 趋于零,取上述和的极限,所得的极限便自然地定义为所论曲顶柱体的体积 V,即

$$
V = \lim _ {\lambda \to 0} \sum_ {i = 1} ^ {n} f (\xi_ {i}, \eta_ {i}) \Delta \sigma_ {i}.
$$

![](../../raw/pages_0129-0160/images/page_137_image_11.jpg)

<details>
<summary>text_image</summary>

z
z=f(x,y)
O
y
D
Δσᵢ
x
(ξᵢ, ηᵢ)
</details>

图10-2

## 2. 平面薄片的质量

设有一平面薄片占有 $xOy$ 面上的闭区域 $D$, 它在点 $(x, y)$ 处的面密度为 $\mu(x, y)$, 这里 $\mu(x, y) > 0$ 且在 $D$ 上连续. 现在要计算该薄片的质量 $m$.

我们知道,如果薄片是均匀的,即面密度是常数,那么薄片的质量可以用公式

$$
\mathrm{质量} = \mathrm{面密度} \times \mathrm{面积}
$$

来计算. 现在面密度  $\mu(x,y)$  是变量, 薄片的质量就不能直接用上式来计算. 但是上面用来处理曲顶柱体体积问题的方法完全适用于本问题.

由于  $\mu(x,y)$  连续, 把薄片分成许多小块后, 只要小块所占的小闭区域  $\Delta\sigma_{i}$  的直径很小, 这些小块就可以近似地看做均匀薄片. 在  $\Delta\sigma_{i}$  上任取一点  $(\xi_{i},\eta_{i})$ , 则

$$
\mu (\xi_ {i}, \eta_ {i}) \Delta \sigma_ {i} \quad (i = 1, 2, \dots , n)
$$

可看做第 $i$ 个小块的质量的近似值(图10-3).通过求和、取极限，便得出

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 一个闭区域的直径是指区域上任意两点间距离的最大者.</span></small>

131

---

第十章 重积分

$$
m = \lim _ {\lambda \to 0} \sum_ {i = 1} ^ {n} \mu (\xi_ {i}, \eta_ {i}) \Delta \sigma_ {i}.
$$

上面两个问题的实际意义虽然不同,但所求量都归结为同一形式的和的极限.在物理、力学、几何和工程技术中,有许多物理量或几何量都可归结为这一形式的和的极限.因此我们要一般地研究这种和的极限,并抽象出下述二重积分的定义:

![](../../raw/pages_0129-0160/images/page_138_image_3.jpg)

<details>
<summary>text_image</summary>

(ξᵢ, ηᵢ)
Δσᵢ
O
x
y
</details>

图10-3

定义 设 $f(x, y)$ 是有界闭区域 $D$ 上的有界函数. 将闭区域 $D$ 任意分成 $n$ 个小闭区域

$$
\Delta \sigma_ {1}, \Delta \sigma_ {2}, \dots , \Delta \sigma_ {n},
$$

其中  $\Delta\sigma_{i}$  表示第 i 个小闭区域,也表示它的面积.在每个  $\Delta\sigma_{i}$  上任取一点  $(\xi_{i},\eta_{i})$ ,作乘积  $f(\xi_{i},\eta_{i})\Delta\sigma_{i}\quad(i=1,2,\cdots,n)$ ,并作和  $\sum_{i=1}^{n}f(\xi_{i},\eta_{i})\Delta\sigma_{i}$ .如果当各小闭区域的直径中的最大值  $\lambda\to0$  时,这和的极限总存在,且与闭区域 D 的分法及点  $(\xi_{i},\eta_{i})$  的取法无关,那么称此极限为函数  $f(x,y)$  在闭区域 D 上的二重积分,记作  $\iint_{D}f(x,y)\mathrm{d}\sigma$ ,即

$$
\iint_ {D} f (x, y) \mathrm{d} \sigma = \lim _ {\lambda \to 0} \sum_ {i = 1} ^ {n} f (\xi_ {i}, \eta_ {i}) \Delta \sigma_ {i}. \tag {1-1}
$$

其中 $f(x,y)$ 叫做被积函数, $f(x,y)\mathrm{d}\sigma$ 叫做被积表达式, $\mathrm{d}\sigma$ 叫做面积元素, $x$ 与 $y$ 叫做积分变量, $D$ 叫做积分区域, $\sum_{i=1}^{n} f(\xi_i, \eta_i) \Delta \sigma_i$ 叫做积分和.

在二重积分的定义中对闭区域 $D$ 的划分是任意的, 如果在直角坐标系中用平行于坐标轴的直线网来划分 $D$, 那么除了包含边界点的一些小闭区域外①, 其余的小闭区域都是矩形闭区域. 设矩形闭区域 $\Delta \sigma_{i}$ 的边长为 $\Delta x_{j}$ 和 $\Delta y_{k}$, 则 $\Delta \sigma_{i} = \Delta x_{j} \cdot \Delta y_{k}$. 因此在直角坐标系中, 有时也把面积元素 $\mathrm{d}\sigma$ 记作 $\mathrm{d}x\mathrm{d}y$, 而把二重积分记作

$$
\iint_ {D} f (x, y) \mathrm{d} x \mathrm{d} y,
$$

其中 $\mathrm{d}x\mathrm{d}y$ 叫做直角坐标系中的面积元素.

这里我们要指出, 当 $f(x, y)$ 在闭区域 $D$ 上连续时, (1-1) 式右端的和的极限必定存在, 也就是说, 函数 $f(x, y)$ 在 $D$ 上的二重积分必定存在, 即函数 $f(x, y)$ 在 $D$ 上必定可积. 以后我们总假定函数 $f(x, y)$ 在闭区域 $D$ 上可积.

由二重积分的定义可知,曲顶柱体的体积是函数 $f(x,y)$ 在底D上的二重积分

$$
V = \iint_ {D} f (x, y)   \mathrm{d} \sigma  ,
$$

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 求和的极限时,这些小闭区域所对应的项的和的极限为零,因此这些小闭区域可以略去不计.</span></small>

132

---

第一节 二重积分的概念与性质

平面薄片的质量是它的面密度 $\mu (x,y)$ 在薄片所占闭区域 $D$ 上的二重积分

$$
m = \iint_ {D} \mu (x, y) \mathrm{d} \sigma .
$$

一般地, 如果 $f(x, y) \geqslant 0$, 被积函数 $f(x, y)$ 可以解释为曲顶柱体的顶在点 $(x, y)$ 处的竖坐标, 所以二重积分的几何意义就是柱体的体积. 如果 $f(x, y)$ 是负的, 柱体就在 $xOy$ 面的下方, 二重积分的绝对值仍等于柱体的体积, 但二重积分的值是负的. 如果 $f(x, y)$ 在 $D$ 的若干部分区域上是正的, 而在其他的部分区域上是负的, 那么, $f(x, y)$ 在 $D$ 上的二重积分就等于 $xOy$ 面上方的柱体体积减去 $xOy$ 面下方的柱体体积所得之差.

## 二、二重积分的性质

比较定积分与二重积分的定义可以想到,二重积分与定积分有类似的性质,现叙述于下:

性质1 设 $\alpha$ 与 $\beta$ 为常数, 则

$$
\iint_ {D} [ \alpha f (x, y) + \beta g (x, y) ] \mathrm{d} \sigma = \alpha \iint_ {D} f (x, y) \mathrm{d} \sigma + \beta \iint_ {D} g (x, y) \mathrm{d} \sigma .
$$

性质 2 如果闭区域 D 被有限条曲线分为有限个部分闭区域,那么在 D 上的二重积分等于在各部分闭区域上的二重积分的和.

例如 $D$ 分为两个闭区域 $D_{1}$ 与 $D_{2}$, 则

$$
\iint_ {D} f (x, y) \mathrm{d} \sigma = \iint_ {D _ {1}} f (x, y) \mathrm{d} \sigma + \iint_ {D _ {2}} f (x, y) \mathrm{d} \sigma .
$$

这个性质表示二重积分对于积分区域具有可加性.

性质3 如果在 $D$ 上, $f(x,y) = 1, \sigma$ 为 $D$ 的面积, 那么

$$
\sigma = \iint_ {D} 1 \cdot \mathrm{d} \sigma = \iint_ {D} \mathrm{d} \sigma.
$$

这性质的几何意义是很明显的,因为高为1的平顶柱体的体积在数值上就等于柱体的底面积.

性质4 如果在 $D$ 上，$f(x,y) \leqslant g(x,y)$，那么有

$$
\iint_ {D} f (x, y) \mathrm{d} \sigma \leqslant \iint_ {D} g (x, y) \mathrm{d} \sigma .
$$

特殊地,由于

$$
- \left| f (x, y) \right| \leqslant f (x, y) \leqslant \left| f (x, y) \right|,
$$

又有

$$
\left| \iint_ {D} f (x, y)   \mathrm{d} \sigma \right| \leqslant \iint_ {D} | f (x, y) |   \mathrm{d} \sigma.
$$

133

---

第十章 重积分

性质5 设 $M$ 和 $m$ 分别是 $f(x, y)$ 在闭区域 $D$ 上的最大值和最小值, $\sigma$ 是 $D$ 的面积, 则有

$$
m \sigma \leqslant \iint_ {D} f (x, y)   \mathrm{d} \sigma \leqslant M \sigma.
$$

上述不等式是对于二重积分估值的不等式. 因为 $m \leqslant f(x, y) \leqslant M$, 所以由性质 4 有

$$
\iint_ {D} m \mathrm{d} \sigma \leqslant \iint_ {D} f (x, y) \mathrm{d} \sigma \leqslant \iint_ {D} M \mathrm{d} \sigma ,
$$

再应用性质 1 和性质 3, 便得此估值不等式.

性质6(二重积分的中值定理) 设函数 $f(x, y)$ 在闭区域 $D$ 上连续, $\sigma$ 是 $D$ 的面积, 则在 $D$ 上至少存在一点 $(\xi, \eta)$, 使得

$$
\iint_ {D} f (x, y) \mathrm{d} \sigma = f (\xi , \eta) \sigma .
$$

证 显然 $\sigma \neq 0$ .把性质5中不等式各除以 $\sigma$ ，有

$$
m \leqslant \frac {1}{\sigma} \iint_ {D} f (x, y)   \mathrm{d} \sigma \leqslant M.
$$

这就是说,确定的数值 $\frac{1}{\sigma}\iint_{D}f(x,y)\mathrm{d}\sigma$ 是介于函数 $f(x,y)$ 的最大值M与最小值m之间的.根据在闭区域上连续函数的介值定理,在D上至少存在一点 $(\xi,\eta)$ ,使得函数在该点的值与这个确定的数值相等,即

$$
\frac {1}{\sigma} \iint_ {D} f (x, y) \mathrm{d} \sigma = f (\xi , \eta).
$$

上式两端各乘  $\sigma$ ，就得所需要证明的公式.

例1 估计二重积分 $I = \iint_{D} (x + y + 10) \, \mathrm{d}\sigma$ 的值，其中 $D = \{(x, y) | (x - 2)^2 + (y - 1)^2 \leqslant 2\}$.

解 按照二重积分的性质 5, 估计二重积分的值, 关键是要确定被积函数 $f(x, y)$ 在积分区域 $D$ 上的最大值和最小值. 本例中, 被积函数 $f(x, y) = x + y + 10$ 的图形是一张平面. 容易知道, 它在 $D$ 上的最大值、最小值均在 $D$ 的边界上取得, 所以, 只需考虑它在 $D$ 的边界上的取值情形.

$D$ 的边界曲线 $L$ 的参数方程为

$$
\left\{ \begin{array}{l l} x = 2 + \sqrt {2} \cos t, \\ y = 1 + \sqrt {2} \sin t, \end{array} \right. \quad t \in [ 0, 2 \pi ].
$$

因此在 $L$ 上, 有

$$
f (x, y) = \sqrt {2} (\cos t + \sin t) + 1 3 = 2 \sin \left(t + \frac {\pi}{4}\right) + 1 3,
$$

![](../../raw/pages_0129-0160/images/page_140_image_19.jpg)

例题精讲

10-1

134

---

第一节 二重积分的概念与性质

便得

$$
1 1 \leqslant f (x, y) \leqslant 1 5.
$$

区域 D 的面积  $\sigma=2\pi$ ，于是

$$
2 2 \pi \leqslant I \leqslant 3 0 \pi .
$$

例2 设 $f(x, y)$ 在闭区域 $D$ 上连续，$D$ 关于 $x$ 轴和 $y$ 轴均对称，记 $D_{1} = \{(x, y) | (x, y) \in D, x \geqslant 0, y \geqslant 0\}$，二重积分 $I = \iint_{D} f(x, y) \, \mathrm{d}\sigma = 4 \iint_{D_{1}} f(x, y) \, \mathrm{d}\sigma$ 成立的条件是下列条件中的哪一个？

(1) $f(x,y)$ 关于 $x$ 是奇函数, 关于 $y$ 是偶函数, 即

$$
f (- x, y) = - f (x, y), \quad f (x, - y) = f (x, y), \quad (x, y) \in D;
$$

(2) $f(-x,y)=f(x,y),f(x,-y)=f(x,y),(x,y)\in D;$
(3)  $f(-x,y)=f(x,y)$ ,  $f(x,-y)=-f(x,y)$ ,  $(x,y)\in D;$
(4) $f(-x, y) = -f(x, y)$, $f(x, -y) = -f(x, y)$, $(x, y) \in D$.

解（2）中的函数 $f(x,y)$ 关于 $x$ 、关于 $y$ 均是偶函数，而积分区域 $D$ 关于 $y$ 轴、$x$ 轴均对称，由二重积分对于积分区域的可加性和几何意义，可知题中给出的积分等式成立，其余三种条件下，积分等式均不成立。例如条件(1)和(4)，$f(x,y)$ 关于 $x$ 是奇函数，而积分区域 $D$ 关于 $y$ 轴对称，即知 $I = 0$；同理，条件(3)，$f(x,y)$ 关于 $y$ 是奇函数，而积分区域 $D$ 关于 $x$ 轴对称，即知 $I = 0$。

## 习题10-1

1. 设有一平面薄板(不计其厚度)占有 xOy 面上的闭区域 D, 薄板上分布有面密度为  $\mu = \mu(x, y)$  的电荷, 且  $\mu(x, y)$  在 D 上连续, 试用二重积分表达该薄板上的全部电荷 Q.
2. 设 $I_{1} = \iint_{D_{1}} (x^{2} + y^{2})^{3} \mathrm{d}\sigma$，其中 $D_{1} = \{(x, y) | -1 \leqslant x \leqslant 1, -2 \leqslant y \leqslant 2\}$; 又 $I_{2} = \iint_{D_{2}} (x^{2} + y^{2})^{3} \mathrm{d}\sigma$，其中 $D_{2} = \{(x, y) | 0 \leqslant x \leqslant 1, 0 \leqslant y \leqslant 2\}$. 试利用二重积分的几何意义说明 $I_{1}$ 与 $I_{2}$ 之间的关系.

3. 利用二重积分定义证明:

(1) $\iint_{D} \mathrm{d}\sigma = \sigma$ （其中 $\sigma$ 为 $D$ 的面积）；
(2) $\iint_{D}kf(x,y)\mathrm{d}\sigma=k\iint_{D}f(x,y)\mathrm{d}\sigma$ （其中k为常数）；
(3) $\iint_{D} f(x, y) \mathrm{d}\sigma = \iint_{D_1} f(x, y) \mathrm{d}\sigma + \iint_{D_2} f(x, y) \mathrm{d}\sigma$，其中 $D = D_1 \cup D_2, D_1, D_2$ 为两个无公共内点的闭区域.

4. 试确定积分区域 D, 使二重积分  $\iint_{D}(1-2x^{2}-y^{2})\mathrm{d}x\mathrm{d}y$  达到最大值.

释疑解难 10-1

135

---

第十章 重积分

5. 根据二重积分的性质, 比较下列积分的大小:

(1) $\iint_{D}(x + y)^{2}\mathrm{d}\sigma$ 与 $\iint_{D}(x + y)^{3}\mathrm{d}\sigma$ ，其中积分区域 $D$ 是由 $x$ 轴、$y$ 轴与直线 $x + y = 1$ 所围成；
(2) $\iint_{D}(x + y)^{2}\mathrm{d}\sigma$ 与 $\iint_{D}(x + y)^3\mathrm{d}\sigma$ ，其中积分区域 $D$ 是由圆周 $(x - 2)^{2} + (y - 1)^{2} = 2$ 所围成；
(3) $\iint_{D} \ln (x + y) \, \mathrm{d}\sigma$ 与 $\iint_{D} [\ln (x + y)]^2 \, \mathrm{d}\sigma$, 其中 $D$ 是三角形闭区域, 三顶点分别为 $(1,0),(1,1),(2,0)$;
(4) $\iint_{D} \ln(x + y) \, \mathrm{d}\sigma$ 与 $\iint_{D} [\ln(x + y)]^2 \, \mathrm{d}\sigma$, 其中 $D = \{(x, y) \mid 3 \leqslant x \leqslant 5, 0 \leqslant y \leqslant 1\}$.

6. 计算 $\iint_{D}(2 + y\cos x + xy\sin y)\mathrm{d}\sigma$ ，其中 $D = \{(x,y)\left|x^{2} + y^{2}\leqslant 1\}$

7. 利用二重积分的性质估计下列积分的值:

(1) $I = \iint_{D} xy(x + y) \, \mathrm{d}\sigma$，其中 $D = \{(x, y) \mid 0 \leqslant x \leqslant 1, 0 \leqslant y \leqslant 1\}$;
(2) $I = \iint_{D} \sin^{2} x \sin^{2} y \, \mathrm{d}\sigma$，其中 $D = \{(x, y) \mid 0 \leqslant x \leqslant \pi, 0 \leqslant y \leqslant \pi\}$;
(3) $I = \iint_{D}(x + y + 1)\mathrm{d}\sigma$，其中 $D = \{(x,y) \mid 0 \leqslant x \leqslant 1, 0 \leqslant y \leqslant 2\}$;
(4) $I = \iint_{D} (x^{2} + 4y^{2} + 9)\mathrm{d}\sigma$, 其中 $D = \{(x, y) \mid x^{2} + y^{2} \leqslant 4\}$.

## 第二节 二重积分的计算法

按照二重积分的定义来计算二重积分,对少数特别简单的被积函数和积分区域来说是可行的,但对一般的函数和区域来说,这不是一种切实可行的方法.本节介绍一种计算二重积分的方法,这种方法是把二重积分化为两次定积分来计算.

## 一、利用直角坐标计算二重积分

下面用几何观点来讨论二重积分 $\iint_{D} f(x, y) \, \mathrm{d}\sigma$ 的计算问题. 在讨论中我们假定 $f(x, y) \geqslant 0$.

设积分区域 $D$ 可以用不等式

$$
\varphi_ {1} (x) \leqslant y \leqslant \varphi_ {2} (x), \quad a \leqslant x \leqslant b
$$

来表示(图10-4)，其中函数 $\varphi_1(x),\varphi_2(x)$ 在区间 $[a,b]$ 上连续.

按照二重积分的几何意义,二重积分  $\iint_{D} f(x, y) \, d\sigma$  的值等于以 D 为底,曲面  $z = f(x, y)$  为顶的曲顶柱体(图 10-5)的体积.下面我们应用第六章中计算“平行截面面

136

---

第二节 二重积分的计算法

积为已知的立体的体积”的方法来计算这个曲顶柱体的体积.

![](../../raw/pages_0129-0160/images/page_143_image_2.jpg)

图10-4

![](../../raw/pages_0129-0160/images/page_143_image_4.jpg)

<details>
<summary>text_image</summary>

z
z=f(x,y)
A(x₀)
y=φ₂(x)
y=φ₁(x)
O
a
x₀
b
x
</details>

图10-5

先计算截面面积.为此,在区间 $[a,b]$ 上任意取定一点 $x_{0}$ ,作平行于yOz面的平面 $x=x_{0}$ .这平面截曲顶柱体所得的截面是一个以区间 $\left[\varphi_{1}(x_{0}),\varphi_{2}(x_{0})\right]$ 为底、曲线 $z=f(x_{0},y)$ 为曲边的曲边梯形(图10-5中阴影部分),所以这截面的面积为

$$
A (x _ {0}) = \int_ {\varphi_ {1} (x _ {0})} ^ {\varphi_ {2} (x _ {0})} f (x _ {0}, y) \mathrm{d} y.
$$

一般地, 过区间  $[a, b]$  上任一点 x 且平行于 yOz 面的平面截曲顶柱体所得截面的面积为

$$
A (x) = \int_ {\varphi_ {1} (x)} ^ {\varphi_ {2} (x)} f (x, y)   \mathrm{d} y.
$$

于是,应用计算平行截面面积为已知的立体体积的方法,得曲顶柱体体积为

$$
V = \int_ {a} ^ {b} A (x)   \mathrm{d} x = \int_ {a} ^ {b} \left[ \int_ {\varphi_ {1} (x)} ^ {\varphi_ {2} (x)} f (x, y)   \mathrm{d} y \right]   \mathrm{d} x.
$$

这个体积也就是所求二重积分的值,从而有等式

$$
\iint_ {D} f (x, y) \mathrm{d} \sigma = \int_ {a} ^ {b} \left[ \int_ {\varphi_ {1} (x)} ^ {\varphi_ {2} (x)} f (x, y) \mathrm{d} y \right] \mathrm{d} x. \tag {2-1}
$$

上式右端的积分叫做先对 $y$ 、后对 $x$ 的二次积分. 就是说, 先把 $x$ 看做常数, 把 $f(x, y)$ 只看做 $y$ 的函数, 并对 $y$ 计算从 $\varphi_1(x)$ 到 $\varphi_2(x)$ 的定积分; 然后把算得的结果 (是 $x$ 的函数) 再对 $x$ 计算在区间 $[a, b]$ 上的定积分. 这个先对 $y$ 、后对 $x$ 的二次积分也常记作

$$
\int_ {a} ^ {b} \mathrm{d} x \int_ {\varphi_ {1} (x)} ^ {\varphi_ {2} (x)} f (x, y) \mathrm{d} y.
$$

因此,等式(2-1)也写成

$$
\iint_ {D} f (x, y) \mathrm{d} \sigma = \int_ {a} ^ {b} \mathrm{d} x \int_ {\varphi_ {1} (x)} ^ {\varphi_ {2} (x)} f (x, y) \mathrm{d} y, \tag {$2-1^{\prime$}}
$$

这就是把二重积分化为先对 y、后对 x 的二次积分的公式.

在上述讨论中,我们假定 $f(x,y)\geqslant0$ ,但实际上公式(2-1)的成立并不受此条件限制.

137

---

第十章 重积分

类似地,如果积分区域 D 可以用不等式

$$
\psi_ {1} (y) \leqslant x \leqslant \psi_ {2} (y), \quad c \leqslant y \leqslant d
$$

来表示(图 10-6)，其中函数  $\psi_{1}(y)$ ,  $\psi_{2}(y)$  在区间  $[c,d]$  上连续，那么就有

$$
\iint_ {D} f (x, y) \mathrm{d} \sigma = \int_ {c} ^ {d} \left[ \int_ {\psi_ {1} (y)} ^ {\psi_ {2} (y)} f (x, y) \mathrm{d} x \right] \mathrm{d} y. \tag {2-2}
$$

上式右端的积分叫做先对 $x$ 、后对 $y$ 的二次积分，这个积分也常记作

$$
\int_ {c} ^ {d} \mathrm{d} y \int_ {\psi_ {1} (y)} ^ {\psi_ {2} (y)} f (x, y) \mathrm{d} x.
$$

因此,等式(2-2)也写成

$$
\iint_ {D} f (x, y) \mathrm{d} \sigma = \int_ {c} ^ {d} \mathrm{d} y \int_ {\psi_ {1} (y)} ^ {\psi_ {2} (y)} f (x, y) \mathrm{d} x, \tag {$2-2^{\prime$}}
$$

这就是把二重积分化为先对 x、后对 y 的二次积分的公式.

![](../../raw/pages_0129-0160/images/page_144_image_10.jpg)

图10-6

以后我们称图10-4所示的积分区域为 $X$ 型区域，图10-6所示的积分区域为 $Y$ 型区域.应用公式(2-1)时，积分区域必须是 $X$ 型区域，$X$ 型区域 $D$ 的特点是:穿过 $D$ 内部且平行于 $y$ 轴的直线与 $D$ 的边界相交不多于两点；而用公式(2-2)时，积分区域必须是 $Y$ 型区域，$Y$ 型区域 $D$ 的特点是:穿过 $D$ 内部且平行于 $x$ 轴的直线与 $D$ 的边界相交不多于两点.如果积分区域 $D$ 如图10-7那样，既有一部分使穿过 $D$ 内部且平行于 $y$ 轴的直线与 $D$ 的边界相交多于两点，又有一部分使穿过 $D$ 内部且平行于 $x$ 轴的直线与 $D$ 的边界相交多于两点，那么 $D$ 既不是 $X$ 型区域，又不是 $Y$ 型区域.对于这种情形，可以把 $D$ 分成几部分，使每个部分是 $X$ 型区域或是 $Y$ 型区域.例如，在图10-7中，把 $D$ 分成三部分，它们都是 $X$ 型区域，从而在这三部分上的二重积分都可应用公式(2-1).各部分上的二重积分求得后，根据二重积分的性质2,它们的和就是在 $D$ 上的二重积分.

如果积分区域 $D$ 既是 $X$ 型的，可用不等式 $\varphi_{1}(x) \leqslant y \leqslant \varphi_{2}(x), a \leqslant x \leqslant b$ 表示，又是 $Y$ 型的，可用不等式 $\psi_{1}(y) \leqslant x \leqslant \psi_{2}(y), c \leqslant y \leqslant d$ 表示（图10-8），那么由公式(2-1')及(2-2')就得

138

---

第二节 二重积分的计算法

$$
\int_ {a} ^ {b} \mathrm{d} x \int_ {\varphi_ {1} (x)} ^ {\varphi_ {2} (x)} f (x, y) \mathrm{d} y = \int_ {c} ^ {d} \mathrm{d} y \int_ {\psi_ {1} (y)} ^ {\psi_ {2} (y)} f (x, y) \mathrm{d} x. \tag {2-3}
$$

上式表明, 这两个不同次序的二次积分相等, 因为它们都等于同一个二重积分

$$
\iint_ {D} f (x, y) \mathrm{d} \sigma .
$$

将二重积分化为二次积分时,确定积分限是一个关键.积分限是根据积分区域D来确定的,先画出积分区域D的图形.假如积分区域D是X型的,如图10-9所示,在区间 $[a,b]$ 上任意取定一个x值,积分区域上以这个x值为横坐标的点在一段直线上,这段直线平行于y轴,该线段上点的纵坐标从 $\varphi_{1}(x)$ 变到 $\varphi_{2}(x)$ ,这就是公式(2-1)中先把x看做常量而对y积分时的下限和上限.因为上面的x值是在 $[a,b]$ 上任意取定的,所以再把x看做变量而对x积分时,积分区间就是 $[a,b]$ .

![](../../raw/pages_0129-0160/images/page_145_image_5.jpg)

<details>
<summary>text_image</summary>

y
I
II
III
O
x
</details>

图10-7

![](../../raw/pages_0129-0160/images/page_145_image_7.jpg)

<details>
<summary>text_image</summary>

y
d
D
c
O
a
b
x
</details>

图10-8

![](../../raw/pages_0129-0160/images/page_145_image_9.jpg)

<details>
<summary>text_image</summary>

y
φ₂(x)
D
φ₁(x)
O a x b x
</details>

图10-9

例 1 计算  $\iint_{D} xy \, d\sigma$ ，其中 D 是由直线 y = 1, x = 2 及 y = x 所围成的闭区域.

解法一 首先画出积分区域 $D$ （图10-10）. $D$ 是 $X$ 型的，$D$ 上的点的横坐标的变动范围是区间[1,2].在区间[1,2]上任意取定一个 $x$ 值，则 $D$ 上以这个 $x$ 值为横坐标的点在一段直线上，这段直线平行于 $y$ 轴，该线段上点的纵坐标从 $y = 1$ 变到 $y = x$.利用公式(2-1)得

$$
\iint_ {D} x y \mathrm{d} \sigma = \int_ {1} ^ {2} \left[ \int_ {1} ^ {x} x y \mathrm{d} y \right] \mathrm{d} x = \int_ {1} ^ {2} \left[ x \cdot \frac {y ^ {2}}{2} \right] _ {1} ^ {x} \mathrm{d} x = \int_ {1} ^ {2} \left(\frac {x ^ {3}}{2} - \frac {x}{2}\right) \mathrm{d} x = \left[ \frac {x ^ {4}}{8} - \frac {x ^ {2}}{4} \right] _ {1} ^ {2} = \frac {9}{8}.
$$

解法二 如图10-11, 积分区域 $D$ 是 $Y$ 型的, $D$ 上的点的纵坐标的变动范围是区间[1,2]. 在区间[1,2]上任意取定一个 $y$ 值, 则 $D$ 上以这个 $y$ 值为纵坐标的点在一段直线上, 这段直线平行于 $x$ 轴, 该线段上点的横坐标从 $x = y$ 变到 $x = 2$. 于是, 利用公式(2-2)得

$$
\iint_ {D} x y \mathrm{d} \sigma = \int_ {1} ^ {2} \left[ \int_ {y} ^ {2} x y \mathrm{d} x \right] \mathrm{d} y = \int_ {1} ^ {2} \left[ y \cdot \frac {x ^ {2}}{2} \right] _ {y} ^ {2} \mathrm{d} y = \int_ {1} ^ {2} \left(2 y - \frac {y ^ {3}}{2}\right) \mathrm{d} y = \left[ y ^ {2} - \frac {y ^ {4}}{8} \right] _ {1} ^ {2} = \frac {9}{8}.
$$

139

---

第十章 重积分

![](../../raw/pages_0129-0160/images/page_146_image_1.jpg)

<details>
<summary>text_image</summary>

y
y=x
D
y=1
O 1 x 2 x
</details>

图 10-10

![](../../raw/pages_0129-0160/images/page_146_image_3.jpg)

<details>
<summary>text_image</summary>

y
2
x=y
y
D
x=2
1
O
x
</details>

图10-11

例2 计算 $\iint_{D} y \sqrt{1 + x^2 - y^2} \, \mathrm{d}\sigma$，其中 $D$ 是由直线 $y = x, x = -1$ 和 $y = 1$ 所围成的闭区域.

解 画出积分区域 $D$ 如图10-12所示. $D$ 既是 $X$ 型的, 又是 $Y$ 型的. 若利用公式(2-1), 得

$$
\begin{array}{l} \iint_ {D} y \sqrt {1 + x ^ {2} - y ^ {2}} \mathrm{d} \sigma = \int_ {- 1} ^ {1} \left[ \int_ {x} ^ {1} y \sqrt {1 + x ^ {2} - y ^ {2}} \mathrm{d} y \right] \mathrm{d} x = - \frac {1}{3} \int_ {- 1} ^ {1} \left[ (1 + x ^ {2} - y ^ {2}) ^ {\frac {3}{2}} \right] _ {x} ^ {1} \mathrm{d} x \\ = - \frac {1}{3} \int_ {- 1} ^ {1} (| x | ^ {3} - 1) \mathrm{d} x = - \frac {2}{3} \int_ {0} ^ {1} (x ^ {3} - 1) \mathrm{d} x = \frac {1}{2}. \\ \end{array}
$$

若利用公式(2-2)(图 10-13)，就有

$$
\iint_ {D} y \sqrt {1 + x ^ {2} - y ^ {2}} \mathrm{d} \sigma = \int_ {- 1} ^ {1} y \left[ \int_ {- 1} ^ {y} \sqrt {1 + x ^ {2} - y ^ {2}} \mathrm{d} x \right] \mathrm{d} y,
$$

其中关于 $x$ 的积分计算比较麻烦. 所以这里用公式(2-1)计算较为方便.

![](../../raw/pages_0129-0160/images/page_146_image_11.jpg)

<details>
<summary>text_image</summary>

y
1
D
y=x
-1 x O 1 x
</details>

图10-12

![](../../raw/pages_0129-0160/images/page_146_image_13.jpg)

<details>
<summary>text_image</summary>

y
1
y
D
y=x
-1 O 1 x
-1
</details>

图10-13

例3 计算 $\iint_{D} xy \, \mathrm{d}\sigma$，其中 $D$ 是由抛物线 $y^2 = x$ 及直线 $y = x - 2$ 所围成的闭区域.

解 画出积分区域 $D$ 如图10-14所示. $D$ 既是 $X$ 型的, 又是 $Y$ 型的. 若利用公式(2-2), 则得

$$
\iint_ {D} x y \mathrm{d} \sigma = \int_ {- 1} ^ {2} \left[ \int_ {y ^ {2}} ^ {y + 2} x y \mathrm{d} x \right] \mathrm{d} y = \int_ {- 1} ^ {2} \left[ \frac {x ^ {2}}{2} y \right] _ {y ^ {2}} ^ {y + 2} \mathrm{d} y = \frac {1}{2} \int_ {- 1} ^ {2} \left[ y (y + 2) ^ {2} - y ^ {5} \right] \mathrm{d} y
$$

140

---

第二节 二重积分的计算法

$$
= \frac {1}{2} \left[ \frac {y ^ {4}}{4} + \frac {4}{3} y ^ {3} + 2 y ^ {2} - \frac {y ^ {6}}{6} \right] _ {- 1} ^ {2} = \frac {4 5}{8}.
$$

若利用公式(2-1)来计算,则由于在区间[0,1]及[1,4]上表示 $\varphi_{1}(x)$ 的式子不同,所以要用经过交点(1,-1)且平行于y轴的直线x=1把区域D分成 $D_{1}$ 和 $D_{2}$ 两部分(图10-15),其中

$$
D _ {1} = \{(x, y) | - \sqrt {x} \leqslant y \leqslant \sqrt {x}, 0 \leqslant x \leqslant 1 \}, \quad D _ {2} = \{(x, y) | x - 2 \leqslant y \leqslant \sqrt {x}, 1 \leqslant x \leqslant 4 \}.
$$

![](../../raw/pages_0129-0160/images/page_147_image_4.jpg)

<details>
<summary>text_image</summary>

y
2
x=y²
y
D
O
x=y+2
-1
(1, -1)
(4, 2)
</details>

图10-14

![](../../raw/pages_0129-0160/images/page_147_image_6.jpg)

<details>
<summary>text_image</summary>

y
y=√x
D₁
D₂
O
x 1
y=x-2
x 4 x
(4, 2)
y=-√x
(1, -1)
</details>

图10-15

![](../../raw/pages_0129-0160/images/page_147_image_8.jpg)

因此,根据二重积分的性质2,就有

$$
\iint_ {D} x y \mathrm{d} \sigma = \iint_ {D _ {1}} x y \mathrm{d} \sigma + \iint_ {D _ {2}} x y \mathrm{d} \sigma = \int_ {0} ^ {1} \left[ \int_ {- \sqrt {x}} ^ {\sqrt {x}} x y \mathrm{d} y \right] \mathrm{d} x + \int_ {1} ^ {4} \left[ \int_ {x - 2} ^ {\sqrt {x}} x y \mathrm{d} y \right] \mathrm{d} x.
$$

由此可见,这里用公式(2-1)来计算需要化为两个二次积分.

上述几个例子说明,在化二重积分为二次积分时,为了计算简便,需要选择恰当的

二次积分的次序.这时,既要考虑积分区域D的形状,又要考虑被积函数 $f(x,y)$ 的特性.

例 4 求两个底圆半径都等于 R 的直交圆柱面所围成的立体的体积.

解 设这两个圆柱面的方程分别为

$$
x ^ {2} + y ^ {2} = R ^ {2} \quad {\text {及}} \quad x ^ {2} + z ^ {2} = R ^ {2}.
$$

利用立体关于坐标平面的对称性, 只要算出它在第 I 卦限部分(图 10-16(a)) 的体积  $V_{1}$ , 然后再乘 8 就行了.

所求立体在第Ⅰ卦限部分可以看成是一个曲顶柱体,它的底为

$$
D = \{(x, y) \mid 0 \leqslant y \leqslant \sqrt {R ^ {2} - x ^ {2}}, 0 \leqslant x \leqslant R \},
$$

如图 10-16(b) 所示. 它的顶是柱面  $z=\sqrt{R^{2}-x^{2}}$ . 于是,

$$
V _ {1} = \iint_ {D} \sqrt {R ^ {2} - x ^ {2}}   \mathrm{d} \sigma .
$$

![](../../raw/pages_0129-0160/images/page_147_image_22.jpg)

<details>
<summary>text_image</summary>

z
O
D
R
y
x
R
</details>

(a)

![](../../raw/pages_0129-0160/images/page_147_image_24.jpg)

<details>
<summary>text_image</summary>

y
y=\u221a(R²-x²)
D
O	x	R	x
</details>

(b)

图10-16

141

---

第十章 重积分

利用公式(2-1)，得

$$
\begin{array}{l} V _ {1} = \iint_ {D} \sqrt {R ^ {2} - x ^ {2}} \mathrm{d} \sigma = \int_ {0} ^ {R} \left[ \int_ {0} ^ {\sqrt {R ^ {2} - x ^ {2}}} \sqrt {R ^ {2} - x ^ {2}} \mathrm{d} y \right] \mathrm{d} x \\ = \int_ {0} ^ {R} \left[ \sqrt {R ^ {2} - x ^ {2}} y \right] _ {0} ^ {\sqrt {R ^ {2} - x ^ {2}}} \mathrm{d} x = \int_ {0} ^ {R} \left(R ^ {2} - x ^ {2}\right) \mathrm{d} x = \frac {2}{3} R ^ {3}. \\ \end{array}
$$

从而所求立体的体积为

$$
V = 8 V _ {1} = \frac {1 6}{3} R ^ {3}.
$$

## 二、利用极坐标计算二重积分

有些二重积分,积分区域 D 的边界曲线用极坐标方程来表示比较方便,且被积函数用极坐标变量  $\rho,\theta$  表达比较简单.这时,就可以考虑利用极坐标来计算二重积分  $\iint_{D}f(x,y)\mathrm{d}\sigma$ .

按二重积分的定义

$$
\iint_ {D} f (x, y) \mathrm{d} \sigma = \lim _ {\lambda \to 0} \sum_ {i = 1} ^ {n} f (\xi_ {i}, \eta_ {i}) \Delta \sigma_ {i},
$$

下面我们来研究这个和的极限在极坐标系中的形式.

假定从极点 $O$ 出发且穿过闭区域 $D$ 内部的射线与 $D$ 的边界曲线相交不多于两点.我们用以极点为中心的一族同心圆: $\rho =$ 常数以及从极点出发的一族射线: $\theta =$ 常数，

把 D 分成 n 个小闭区域(图10-17).除了包含边界点的一些小闭区域外,小闭区域的面积  $\Delta\sigma_{i}$  可计算如下:

$$
\begin{array}{l} \Delta \sigma_ {i} = \frac {1}{2} \left(\rho_ {i} + \Delta \rho_ {i}\right) ^ {2} \cdot \Delta \theta_ {i} - \frac {1}{2} \rho_ {i} ^ {2} \cdot \Delta \theta_ {i} \\ = \frac {1}{2} \left(2 \rho_ {i} + \Delta \rho_ {i}\right) \Delta \rho_ {i} \cdot \Delta \theta_ {i} \\ = \frac {\rho_ {i} + (\rho_ {i} + \Delta \rho_ {i})}{2} \cdot \Delta \rho_ {i} \cdot \Delta \theta_ {i} = \bar {\rho_ {i}} \cdot \Delta \rho_ {i} \cdot \Delta \theta_ {i}, \\ \end{array}
$$

![](../../raw/pages_0129-0160/images/page_148_image_13.jpg)

<details>
<summary>text_image</summary>

ρ=ρᵢ+Δρᵢ
ρ=ρᵢ
θ=θᵢ+Δθᵢ
θ=θᵢ
Δσᵢ
Δρᵢ
Δθᵢ
D
O
A
</details>

图10-17

其中 $\bar{\rho}_i$ 表示相邻两圆弧的半径的平均值. 在这小闭区域内取圆周 $\rho = \bar{\rho}_i$ 上的一点 $(\bar{\rho}_i, \bar{\theta}_i)$, 设该点的直角坐标为 $(\xi_i, \eta_i)$, 则由直角坐标与极坐标之间的关系有 $\xi_i = \bar{\rho}_i \cos \bar{\theta}_i$, $\eta_i = \bar{\rho}_i \sin \bar{\theta}_i$. 于是

$$
\lim _ {\lambda \rightarrow 0} \sum_ {i = 1} ^ {n} f (\xi_ {i}, \eta_ {i}) \Delta \sigma_ {i} = \lim _ {\lambda \rightarrow 0} \sum_ {i = 1} ^ {n} f (\bar {\rho} _ {i} \cos \bar {\theta} _ {i}, \bar {\rho} _ {i} \sin \bar {\theta} _ {i}) \bar {\rho} _ {i} \cdot \Delta \rho_ {i} \cdot \Delta \theta_ {i},
$$

即

142

---

第二节 二重积分的计算法

$$
\iint_ {D} f (x, y) \mathrm{d} \sigma = \iint_ {D} f (\rho \cos \theta , \rho \sin \theta) \rho \mathrm{d} \rho \mathrm{d} \theta .
$$

这里我们把点 $(\rho, \theta)$ 看做是在同一平面上的点 $(x, y)$ 的极坐标表示，所以上式右端的积分区域仍然记作 $D$。因为在直角坐标系中 $\iint_{D} f(x, y) \mathrm{d}\sigma$ 也常记作 $\iint_{D} f(x, y) \mathrm{d}x \mathrm{d}y$，所以上式又可写成

$$
\iint_ {D} f (x, y) \mathrm{d} x \mathrm{d} y = \iint_ {D} f (\rho \cos \theta , \rho \sin \theta) \rho \mathrm{d} \rho \mathrm{d} \theta . \tag {2-4}
$$

这就是二重积分的变量从直角坐标变换为极坐标的变换公式,其中  $\rho d\rho d\theta$  就是极坐标系中的面积元素.

公式(2-4)表明,要把二重积分中的变量从直角坐标变换为极坐标,只要把被积函数中的x与y分别换成 $\rho\cos\theta$ 与 $\rho\sin\theta$ ,并把直角坐标系中的面积元素dxdy换成极坐标系中的面积元素 $\rho d\rho d\theta$ .

极坐标系中的二重积分,同样可以化为二次积分来计算.

设积分区域 $D$ 可以用不等式

$$
\varphi_ {1} (\theta) \leqslant \rho \leqslant \varphi_ {2} (\theta), \quad \alpha \leqslant \theta \leqslant \beta
$$

来表示(图 10-18)，其中函数  $\varphi_{1}(\theta)$ ,  $\varphi_{2}(\theta)$  在区间  $[\alpha, \beta]$  上连续.

![](../../raw/pages_0129-0160/images/page_149_image_10.jpg)

<details>
<summary>text_image</summary>

ρ=φ₂(θ)
D
ρ=φ₁(θ)
β
α
O
A
</details>

(a)

![](../../raw/pages_0129-0160/images/page_149_image_12.jpg)

<details>
<summary>text_image</summary>

ρ=φ₂(θ)
D
ρ=φ₁(θ)
β
α
O
A
</details>

(b)

图10-18

先在区间 $[\alpha, \beta]$ 上任意取定一个 $\theta$ 值. 对应于这个 $\theta$ 值, $D$ 上的点 (图10-19中这些点在线段 $EF$ 上) 的极径 $\rho$ 从 $\varphi_1(\theta)$ 变到 $\varphi_2(\theta)$. 又 $\theta$ 是在 $[\alpha, \beta]$ 上任意取定的, 所以 $\theta$ 的变化范围是区间 $[\alpha, \beta]$. 这样就可看出, 极坐标系中的二重积分化为二次积分的公式为

$$
\iint_ {D} f (\rho \cos \theta , \rho \sin \theta) \rho \mathrm{d} \rho \mathrm{d} \theta = \int_ {\alpha} ^ {\beta} \left[ \int_ {\varphi_ {1} (\theta)} ^ {\varphi_ {2} (\theta)} f (\rho \cos \theta , \rho \sin \theta) \rho \mathrm{d} \rho \right] \mathrm{d} \theta . \tag {2-5}
$$

上式也写成

$$
\iint_ {D} f (\rho \cos \theta , \rho \sin \theta) \rho \mathrm{d} \rho \mathrm{d} \theta = \int_ {\alpha} ^ {\beta} \mathrm{d} \theta \int_ {\varphi_ {1} (\theta)} ^ {\varphi_ {2} (\theta)} f (\rho \cos \theta , \rho \sin \theta) \rho \mathrm{d} \rho . \tag {$2-5^{\prime$}}
$$

如果积分区域 $D$ 是图10-20所示的曲边扇形，那么可以把它看做图10-18(a)中当 $\varphi_1(\theta) \equiv 0, \varphi_2(\theta) = \varphi(\theta)$ 时的特例.这时闭区域 $D$ 可以用不等式

143

---

第十章 重积分

$$
0 \leqslant \rho \leqslant \varphi (\theta), \quad \alpha \leqslant \theta \leqslant \beta
$$

来表示,而公式 $(2-5')$ 成为

$$
\iint_ {D} f (\rho \cos \theta , \rho \sin \theta) \rho \mathrm{d} \rho \mathrm{d} \theta = \int_ {\alpha} ^ {\beta} \mathrm{d} \theta \int_ {0} ^ {\varphi (\theta)} f (\rho \cos \theta , \rho \sin \theta) \rho \mathrm{d} \rho .
$$

如果积分区域 $D$ 如图10-21所示, 极点在 $D$ 的内部, 那么可以把它看做图10-20中当 $\alpha = 0$ 且 $\beta = 2\pi$ 时的特例. 这时闭区域 $D$ 可以用不等式

$$
0 \leqslant \rho \leqslant \varphi (\theta), \quad 0 \leqslant \theta \leqslant 2 \pi
$$

来表示,而公式 $(2-5')$ 成为

$$
\iint_ {D} f (\rho \cos \theta , \rho \sin \theta) \rho \mathrm{d} \rho \mathrm{d} \theta = \int_ {0} ^ {2 \pi} \mathrm{d} \theta \int_ {0} ^ {\varphi (\theta)} f (\rho \cos \theta , \rho \sin \theta) \rho \mathrm{d} \rho .
$$

![](../../raw/pages_0129-0160/images/page_150_image_8.jpg)

<details>
<summary>text_image</summary>

D
F
E
β
θ
α
O
φ₁(θ)
φ₂(θ)
A
</details>

图10-19

![](../../raw/pages_0129-0160/images/page_150_image_10.jpg)

<details>
<summary>text_image</summary>

ρ=φ(θ)
D
β
α
O
A
</details>

图10-20

![](../../raw/pages_0129-0160/images/page_150_image_12.jpg)

<details>
<summary>text_image</summary>

ρ=φ(θ)
D
O
A
</details>

图10-21

由二重积分的性质3,闭区域D的面积 $\sigma$ 可以表示为

$$
\sigma = \iint_ {D} \mathrm{d} \sigma.
$$

在极坐标系中,面积元素  $d\sigma=\rho d\rho d\theta$ , 上式成为

$$
\sigma = \iint_ {D} \rho \mathrm{d} \rho \mathrm{d} \theta .
$$

如果闭区域 D 如图 10-18(a) 所示, 那么由公式  $(2-5')$  有

$$
\sigma = \iint_ {D} \rho \mathrm{d} \rho \mathrm{d} \theta = \int_ {\alpha} ^ {\beta} \mathrm{d} \theta \int_ {\varphi_ {1} (\theta)} ^ {\varphi_ {2} (\theta)} \rho \mathrm{d} \rho = \frac {1}{2} \int_ {\alpha} ^ {\beta} [ \varphi_ {2} ^ {2} (\theta) - \varphi_ {1} ^ {2} (\theta) ] \mathrm{d} \theta.
$$

特别地,如果闭区域 D 如图 10-20 所示,那么  $\varphi_{1}(\theta)=0,\varphi_{2}(\theta)=\varphi(\theta)$ .于是

$$
\sigma = \frac {1}{2} \int_ {\alpha} ^ {\beta} \varphi^ {2} (\theta) \mathrm{d} \theta .
$$

例 5 计算  $\iint_{D} e^{-x^{2}-y^{2}} dx dy$ ，其中 D 是由圆心在原点、半径为 a 的圆周所围成的闭区域.

解 在极坐标系中,闭区域 D 可表示为

$$
0 \leqslant \rho \leqslant a, \quad 0 \leqslant \theta \leqslant 2 \pi .
$$

由公式(2-4)及(2-5)有

144

---

第二节 二重积分的计算法

$$
\begin{array}{l} \iint_ {D} \mathrm{e} ^ {- x ^ {2} - y ^ {2}} \mathrm{d} x \mathrm{d} y = \iint_ {D} \mathrm{e} ^ {- p ^ {2}} \rho \mathrm{d} \rho \mathrm{d} \theta = \int_ {0} ^ {2 \pi} \left[ \int_ {0} ^ {a} \mathrm{e} ^ {- p ^ {2}} \rho \mathrm{d} \rho \right] \mathrm{d} \theta \\ = \int_ {0} ^ {2 \pi} \left[ - \frac {1}{2} \mathrm{e} ^ {- p ^ {2}} \right] _ {0} ^ {a} \mathrm{d} \theta = \frac {1}{2} (1 - \mathrm{e} ^ {- a ^ {2}}) \int_ {0} ^ {2 \pi} \mathrm{d} \theta = \pi (1 - \mathrm{e} ^ {- a ^ {2}}). \\ \end{array}
$$

本题如果用直角坐标计算,因为积分  $\int e^{-x^{2}} dx$  不能用初等函数表示,所以算不出来.现在我们利用上面的结果来计算工程上常用的反常积分  $\int_{0}^{+\infty} e^{-x^{2}} dx$ .

设

$$
D _ {1} = \{(x, y) | x ^ {2} + y ^ {2} \leqslant R ^ {2}, x \geqslant 0, y \geqslant 0 \},
$$

$$
D _ {2} = \{(x, y) | x ^ {2} + y ^ {2} \leqslant 2 R ^ {2}, x \geqslant 0, y \geqslant 0 \},
$$

$$
S = \{(x, y) \mid 0 \leqslant x \leqslant R, 0 \leqslant y \leqslant R \}.
$$

显然 $D_{1} \subset S \subset D_{2}$ (图10-22). 由于 $\mathrm{e}^{-x^2 - y^2} > 0$，从而在这些闭区域上的二重积分之间有不等式

$$
\iint_ {D _ {1}} \mathrm{e} ^ {- x ^ {2} - y ^ {2}} \mathrm{d} x \mathrm{d} y <   \iint_ {S} \mathrm{e} ^ {- x ^ {2} - y ^ {2}} \mathrm{d} x \mathrm{d} y <   \iint_ {D _ {2}} \mathrm{e} ^ {- x ^ {2} - y ^ {2}} \mathrm{d} x \mathrm{d} y.
$$

![](../../raw/pages_0129-0160/images/page_151_image_9.jpg)

<details>
<summary>text_image</summary>

y
S
D₁
D₂
O
R √2R x
</details>

图10-22

因为

$$
\iint_ {S} \mathrm{e} ^ {- x ^ {2} - y ^ {2}} \mathrm{d} x \mathrm{d} y = \int_ {0} ^ {R} \mathrm{e} ^ {- x ^ {2}} \mathrm{d} x \cdot \int_ {0} ^ {R} \mathrm{e} ^ {- y ^ {2}} \mathrm{d} y = \left(\int_ {0} ^ {R} \mathrm{e} ^ {- x ^ {2}} \mathrm{d} x\right) ^ {2},
$$

又应用上面已得的结果有

$$
\iint_ {D _ {1}} \mathrm{e} ^ {- x ^ {2} - y ^ {2}} \mathrm{d} x \mathrm{d} y = \frac {\pi}{4} (1 - \mathrm{e} ^ {- R ^ {2}}), \quad \iint_ {D _ {2}} \mathrm{e} ^ {- x ^ {2} - y ^ {2}} \mathrm{d} x \mathrm{d} y = \frac {\pi}{4} (1 - \mathrm{e} ^ {- 2 R ^ {2}}),
$$

于是上面的不等式可写成

$$
\frac {\pi}{4} (1 - \mathrm{e} ^ {- R ^ {2}}) <   \left(\int_ {0} ^ {R} \mathrm{e} ^ {- x ^ {2}} \mathrm{d} x\right) ^ {2} <   \frac {\pi}{4} (1 - \mathrm{e} ^ {- 2 R ^ {2}}).
$$

令 $R\to +\infty$ ，上式两端趋于同一极限 $\frac{\pi}{4}$ ，从而

$$
\int_ {0} ^ {+ \infty} \mathrm{e} ^ {- x ^ {2}} \mathrm{d} x = \frac {\sqrt {\pi}}{2}.
$$

例 6 求球体  $x^{2}+y^{2}+z^{2}\leqslant4a^{2}$  被圆柱面  $x^{2}+y^{2}=2ax\quad(a>0)$  所截得的（含在圆柱面内的部分）立体的体积（图 10-23）.

解 由对称性，

$$
V = 4 \iint_ {D} \sqrt {4 a ^ {2} - x ^ {2} - y ^ {2}}   \mathrm{d} x \mathrm{d} y,
$$

其中 D 为半圆周  $y=\sqrt{2ax-x^{2}}$  及 x 轴所围成的闭区域. 在极坐标系中, 闭区域 D 可用不

145

---

第十章 重积分

等式

$$
0 \leqslant \rho \leqslant 2 a \cos \theta , \quad 0 \leqslant \theta \leqslant \frac {\pi}{2}
$$

来表示.于是

$$
\begin{array}{l} V = 4 \iint_ {D} \sqrt {4 a ^ {2} - \rho^ {2}} \rho \mathrm{d} \rho \mathrm{d} \theta = 4 \int_ {0} ^ {\frac {\pi}{2}} \mathrm{d} \theta \int_ {0} ^ {2 a \cos \theta} \sqrt {4 a ^ {2} - \rho^ {2}} \rho \mathrm{d} \rho \\ = \frac {3 2}{3} a ^ {3} \int_ {0} ^ {\frac {\pi}{2}} (1 - \sin^ {3} \theta) \mathrm{d} \theta = \frac {3 2}{3} a ^ {3} \left(\frac {\pi}{2} - \frac {2}{3}\right). \\ \end{array}
$$

![](../../raw/pages_0129-0160/images/page_152_image_5.jpg)

<details>
<summary>text_image</summary>

z
O
y
D
2a
x
</details>

(a)

![](../../raw/pages_0129-0160/images/page_152_image_7.jpg)

<details>
<summary>text_image</summary>

ρ=2acos θ
D
θ
O
a
2a
A
</details>

(b)

图10-23

## \* 三、二重积分的换元法

上一目得到的二重积分的变量从直角坐标变换为极坐标的变换公式, 是二重积分换元法的一种特殊情形. 在那里, 我们把平面上同一个点 M, 既用直角坐标  $(x, y)$  表示, 又用极坐标  $(\rho, \theta)$  表示, 它们间的关系为

$$
\left\{ \begin{array}{l} x = \rho \cos \theta , \\ y = \rho \sin \theta . \end{array} \right. \tag {2-6}
$$

也就是说,由(2-6)式联系的点 $(x,y)$ 和点 $(\rho ,\theta)$ 看成是同一个平面上的同一个点,只是采用不同的坐标罢了.现在,我们采用另一种观点来加以解释.把(2-6)式看成是从直角坐标平面 $\rho O\theta$ 到直角坐标平面 $xOy$ 的一种变换,即对于 $\rho O\theta$ 平面上的一点$M^{\prime}(\rho ,\theta)$,通过变换(2-6),变成 $xOy$ 平面上的一点 $M(x,y)$.在两个平面各自限定的某个范围内,这种变换还是一对一的(即是一一映射).下面就采用这种观点来讨论二重积分换元法的一般情形.

定理 设 $f(x, y)$ 在 $xOy$ 平面上的闭区域 $D$ 上连续, 若变换

$$
T: x = x (u, v), y = y (u, v) \tag {2-7}
$$

将 $uOv$ 平面上的闭区域 $D'$ 变为 $xOy$ 平面上的 $D$, 且满足

(1) $x(u, v), y(u, v)$ 在 $D'$ 上具有一阶连续偏导数；

146

---

第二节 二重积分的计算法

(2) 在  $D'$  上雅可比式  $J(u,v)=\frac{\partial(x,y)}{\partial(u,v)}\neq0;$
(3) 变换  $T:D'\rightarrow D$  是一对一的，

则有

$$
\iint_ {D} f (x, y) \mathrm{d} x \mathrm{d} y = \iint_ {D ^ {\prime}} f [ x (u, v), y (u, v) ] | J (u, v) | \mathrm{d} u \mathrm{d} v. \tag {2-8}
$$

公式(2-8)称为二重积分的换元公式.

证 显然, 在定理的假设下, (2-8) 式两端的二重积分都存在. 由于二重积分与积分区域的分法无关, 我们用平行于坐标轴的直线网来分割 $D'$, 使得除去包含边界点的小闭区域外, 其余的小闭区域都为边长是 $h$ 的正方形闭区域. 任取一个这样得到的正方形闭区域, 设其顶点为 $M_1'(u, v), M_2'(u + h, v), M_3'(u + h, v + h), M_4'(u, v + h)$, 其面积为 $\Delta \sigma' = h^2$ (图 10-24(a)). 正方形闭区域 $M_1'M_2'M_3'M_4'$ 经变换 (2-7) 变成 $xOy$ 平面上的一个曲边四边形 $M_1M_2M_3M_4$, 它的四个顶点的坐标是

$$
\begin{array}{l} M _ {1}: x _ {1} = x (u, v), y _ {1} = y (u, v); \\ M _ {2}: x _ {2} = x (u + h, v) = x (u, v) + x _ {u} (u, v) h + o (h), \\ y _ {2} = y (u + h, v) = y (u, v) + y _ {u} (u, v) h + o (h); \\ M _ {3}: x _ {3} = x (u + h, v + h) = x (u, v) + x _ {u} (u, v) h + x _ {v} (u, v) h + o (h), \\ y _ {3} = y (u + h, v + h) = y (u, v) + y _ {u} (u, v) h + y _ {v} (u, v) h + o (h); \\ M _ {4}: x _ {4} = x (u, v + h) = x (u, v) + x _ {v} (u, v) h + o (h), \\ y _ {4} = y (u, v + h) = y (u, v) + y _ {v} (u, v) h + o (h), \\ \end{array}
$$

其面积为 $\Delta \sigma$ （图10-24(b)). 可以证明，曲边四边形 $M_{1}M_{2}M_{3}M_{4}$ 的面积与直边四边形 $M_{1}M_{2}M_{3}M_{4}$ （四个顶点用直线相连）的面积当 $h \to 0$ 时只相差高阶无穷小. 又由上面这些坐标表示式可知，若不计高阶无穷小，则有

$$
x _ {2} - x _ {1} = x _ {3} - x _ {4}, \quad y _ {2} - y _ {1} = y _ {3} - y _ {4}, \quad x _ {4} - x _ {1} = x _ {3} - x _ {2}, \quad y _ {4} - y _ {1} = y _ {3} - y _ {2},
$$

![](../../raw/pages_0129-0160/images/page_153_image_11.jpg)

<details>
<summary>text_image</summary>

v
Δσ'
M₄ M₃' M₁' M₂'
v+h
v
O u u+h u
</details>

(a)

![](../../raw/pages_0129-0160/images/page_153_image_13.jpg)

<details>
<summary>text_image</summary>

y
Δσ
M₄
M₃
M₁
M₂
O
x
</details>

(b)

图10-24

147

---

第十章 重积分

这表示, 直边四边形 $M_{1}M_{2}M_{3}M_{4}$ 的对边的长度可看做两两相等. 因此, 若不计高阶无穷小, 曲边四边形 $M_{1}M_{2}M_{3}M_{4}$ 可看做平行四边形, 于是它的面积 $\Delta\sigma$ 近似等于 $\triangle M_{1}M_{2}M_{3}$ 的面积的 2 倍. 根据解析几何, $\triangle M_{1}M_{2}M_{3}$ 的面积的 2 倍等于行列式

$$
\left| \begin{array}{c c} x _ {2} - x _ {1} & x _ {3} - x _ {2} \\ y _ {2} - y _ {1} & y _ {3} - y _ {2} \end{array} \right|
$$

的绝对值,由于

$$
x _ {2} - x _ {1} = x _ {u} (u, v) h + o (h), \quad x _ {3} - x _ {2} = x _ {v} (u, v) h + o (h),
$$

$$
y _ {2} - y _ {1} = y _ {u} (u, v) h + o (h), \quad y _ {3} - y _ {2} = y _ {v} (u, v) h + o (h),
$$

因此上面的行列式与行列式

$$
\left| \begin{array}{l l} x _ {u} (u, v) h & x _ {v} (u, v) h \\ y _ {u} (u, v) h & y _ {v} (u, v) h \end{array} \right| = \left| \begin{array}{l l} x _ {u} (u, v) & x _ {v} (u, v) \\ y _ {u} (u, v) & y _ {v} (u, v) \end{array} \right| h ^ {2}
$$

只相差一个比 $h^2$ 高阶的无穷小.于是

$$
\Delta \sigma = \left| \frac {\partial (x , y)}{\partial (u , v)} \right| \Delta \sigma^ {\prime} + o (\Delta \sigma^ {\prime}) \quad (h \rightarrow 0).
$$

把 $f(x,y) = f[x(u,v),y(u,v)]$ 的两端分别与上式两端相乘，得

$$
f (x, y) \Delta \sigma = f [ x (u, v), y (u, v) ] \left| \frac {\partial (x , y)}{\partial (u , v)} \right| \Delta \sigma^ {\prime} + f [ x (u, v), y (u, v) ] \cdot o (\Delta \sigma^ {\prime}).
$$

上式对一切小正方形闭区域取和并令 $h \to 0$ 求极限, 由于上式右端第二项的和的极限为零, 于是得公式(2-8). 定理证毕.

这里我们指出,如果雅可比式  $J(u,v)$  只在  $D'$  内个别点上,或一条曲线上为零,而在其他点上不为零,那么换元公式(2-8)仍成立.

在变换为极坐标  $x=\rho\cos\theta, y=\rho\sin\theta$  的特殊情形下, 雅可比式

$$
J = \left| \begin{array}{c c} \frac {\partial x}{\partial \rho} & \frac {\partial x}{\partial \theta} \\ \frac {\partial y}{\partial \rho} & \frac {\partial y}{\partial \theta} \end{array} \right| = \left| \begin{array}{c c} \cos \theta & - \rho \sin \theta \\ \sin \theta & \rho \cos \theta \end{array} \right| = \rho ,
$$

它仅在 $\rho = 0$ 处为零，故不论闭区域 $D'$ 是否含有极点，换元公式仍成立.即有

$$
\iint_ {D} f (x, y) \mathrm{d} x \mathrm{d} y = \iint_ {D ^ {\prime}} f (\rho \cos \theta , \rho \sin \theta) \rho \mathrm{d} \rho \mathrm{d} \theta ,
$$

这里 $D'$ 是 $D$ 在直角坐标平面 $\rho O\theta$ 上的对应区域.在上一目内所证得的相同的公式中用的是 $D$ 而不是 $D'$, 当积分区域 $D$ 用极坐标表示时, 其形式就与上式右端的形式完全等同了.

例7 计算 $\iint_{D} \mathrm{e}^{\frac{y - x}{y + x}} \, \mathrm{d}x \, \mathrm{d}y$，其中 $D$ 是由 $x$ 轴、$y$ 轴和直线 $x + y = 2$ 所围成的闭区域.

148

---

第二节 二重积分的计算法

解 令 $u = y - x, v = y + x$，则 $x = \frac{v - u}{2}, y = \frac{v + u}{2}$.

作变换 $x = \frac{v - u}{2}, y = \frac{v + u}{2}$，则 $xOy$ 平面上的闭区域 $D$ 和它在 $uOv$ 平面上的对应区域 $D'$ 如图10-25所示.

![](../../raw/pages_0129-0160/images/page_155_image_3.jpg)

<details>
<summary>text_image</summary>

y
x+y=2
D
O
x
</details>

(a)

![](../../raw/pages_0129-0160/images/page_155_image_5.jpg)

<details>
<summary>text_image</summary>

v
v=2
D'
u=-v
u=v
O
u
</details>

(b)

图10-25

雅可比式为

$$
J = \frac {\partial (x , y)}{\partial (u , v)} = \left| \begin{array}{c c} - \frac {1}{2} & \frac {1}{2} \\ \frac {1}{2} & \frac {1}{2} \end{array} \right| = - \frac {1}{2}.
$$

利用公式(2-8)，得

$$
\iint_ {D} \mathrm{e} ^ {\frac {y - x}{y + x}} \mathrm{d} x \mathrm{d} y = \iint_ {D ^ {\prime}} \mathrm{e} ^ {\frac {u}{v}} \left| - \frac {1}{2} \right| \mathrm{d} u \mathrm{d} v = \frac {1}{2} \int_ {0} ^ {2} \mathrm{d} v \int_ {- v} ^ {v} \mathrm{e} ^ {\frac {u}{v}} \mathrm{d} u = \frac {1}{2} \int_ {0} ^ {2} (\bar {\mathrm{e}} - \mathrm{e} ^ {- 1}) v \mathrm{d} v = \mathrm{e} - \mathrm{e} ^ {- 1}.
$$

例8 求由直线 $x + y = c, x + y = d, y = ax, y = bx$ ($0 < c < d, 0 < a < b$) 所围成的闭区域 $D$ (图10-26(a)) 的面积.

![](../../raw/pages_0129-0160/images/page_155_image_13.jpg)

<details>
<summary>text_image</summary>

y
d
y=bx
C
D
O
c
x
y=ax
d
</details>

(a)

![](../../raw/pages_0129-0160/images/page_155_image_15.jpg)

<details>
<summary>text_image</summary>

v
b
D'
a
O
c
d
u
</details>

(b)

图10-26

解 所求面积为

149

---

第十章 重积分

$$
\iint_ {D} \mathrm{d} x \mathrm{d} y.
$$

上述二重积分直接化为二次积分计算比较麻烦.现采用换元法.令 $u = x + y, v = \frac{y}{x}$, 则 $x = \frac{u}{1 + v}, y = \frac{uv}{1 + v}$. 在这变换下, $D$ 的边界 $x + y = c, x + y = d, y = ax, y = bx$ 依次与 $u = c, u = d, v = a, v = b$ 对应.后者构成与 $D$ 对应的闭区域 $D'$ 的边界.于是

$$
D ^ {\prime} = \{(u, v) \mid c \leqslant u \leqslant d, a \leqslant v \leqslant b \},
$$

如图 10-26(b) 所示. 又雅可比式

$$
J = \frac {\partial (x , y)}{\partial (u , v)} = \frac {u}{(1 + v) ^ {2}} \neq 0, \quad (u, v) \in D ^ {\prime}.
$$

从而所求面积为

$$
\iint_ {D} \mathrm{d} x \mathrm{d} y = \iint_ {D ^ {\prime}} \frac {u}{(1 + v) ^ {2}} \mathrm{d} u \mathrm{d} v = \int_ {a} ^ {b} \frac {\mathrm{d} v}{(1 + v) ^ {2}} \int_ {c} ^ {d} u \mathrm{d} u = \frac {(b - a) (d ^ {2} - c ^ {2})}{2 (1 + a) (1 + b)}.
$$

例9 计算 $\iint_{D} \sqrt{1 - \frac{x^2}{a^2} - \frac{y^2}{b^2}} \, \mathrm{d}x \, \mathrm{d}y$，其中 $D$ 为椭圆 $\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1$ 所围成的闭区域.

解 作广义极坐标变换

$$
\left\{ \begin{array}{l} x = a \rho \cos \theta , \\ y = b \rho \sin \theta , \end{array} \right.
$$

其中 $a > 0, b > 0, \rho \geqslant 0, 0 \leqslant \theta \leqslant 2\pi$. 在这个变换下，与 $D$ 对应的闭区域为 $D' = \{(\rho, \theta) | 0 \leqslant \rho \leqslant 1, 0 \leqslant \theta \leqslant 2\pi\}$，雅可比式

$$
J = \frac {\partial (x , y)}{\partial (\rho , \theta)} = a b \rho .
$$

J 在  $D'$  内仅在  $\rho=0$  处为零, 故换元公式仍成立, 从而有

$$
\iint_ {D} \sqrt {1 - \frac {x ^ {2}}{a ^ {2}} - \frac {y ^ {2}}{b ^ {2}}} \mathrm{d} x \mathrm{d} y = \iint_ {D ^ {\prime}} \sqrt {1 - \rho^ {2}} a b \rho \mathrm{d} \rho \mathrm{d} \theta = \frac {2}{3} \pi a b.
$$

## 习题10-2

1. 计算下列二重积分:

(1) $\iint_{D}(x^{2} + y^{2})\mathrm{d}\sigma$ ，其中 $D = \{(x,y)\mid |x|\leqslant 1,|y|\leqslant 1\}$
(2) $\iint_{D}(3x + 2y)\mathrm{d}\sigma$ ，其中 $D$ 是由两坐标轴及直线 $x + y = 2$ 所围成的闭区域；
(3) $\iint_{D} (x^3 + 3x^2y + y^3) \, \mathrm{d}\sigma$, 其中 $D = \{(x, y) \mid 0 \leqslant x \leqslant 1, 0 \leqslant y \leqslant 1\}$;

150

---

第二节 二重积分的计算法

(4) $\iint_{D} x\cos (x + y)\mathrm{d}\sigma$，其中 $D$ 是顶点分别为 $(0,0), (\pi, 0)$ 和 $(\pi, \pi)$ 的三角形闭区域；
(5) $\iint_{D} \sqrt{|y - x^2|} \, \mathrm{d}x \, \mathrm{d}y$, 其中 $D = \{(x, y) | 0 \leqslant x \leqslant 1, 0 \leqslant y \leqslant 1\}$.

2. 画出积分区域,并计算下列二重积分:

(1) $\iint_{D} x\sqrt{y} \, \mathrm{d}\sigma$，其中 $D$ 是由两条抛物线 $y = \sqrt{x}, y = x^2$ 所围成的闭区域；
(2) $\iint_{D} xy^{2} \, \mathrm{d}\sigma$, 其中 $D$ 是由圆周 $x^{2} + y^{2} = 4$ 及 $y$ 轴所围成的右半闭区域;
(3) $\iint_{D} \mathrm{e}^{x + y} \, \mathrm{d}\sigma$, 其中 $D = \{(x, y) \mid |x| + |y| \leqslant 1\}$;
(4) $\iint_{D} (x^{2} + y^{2} - x) \, \mathrm{d}\sigma$, 其中 $D$ 是由直线 $y = 2, y = x$ 及 $y = 2x$ 所围成的闭区域.

3. 如果二重积分 $\iint_{D} f(x, y) \, \mathrm{d}x \, \mathrm{d}y$ 的被积函数 $f(x, y)$ 是两个函数 $f_1(x)$ 及 $f_2(y)$ 的乘积，即 $f(x, y) = f_1(x) \cdot f_2(y)$，积分区域 $D = \{(x, y) \mid a \leqslant x \leqslant b, c \leqslant y \leqslant d\}$，证明这个二重积分等于两个定积分的乘积，即

$$
\iint_ {D} f _ {1} (x) \cdot f _ {2} (y) \mathrm{d} x \mathrm{d} y = \left[ \int_ {a} ^ {b} f _ {1} (x) \mathrm{d} x \right] \cdot \left[ \int_ {c} ^ {d} f _ {2} (y) \mathrm{d} y \right].
$$

4. 化二重积分

$$
I = \iint_ {D} f (x, y) \mathrm{d} \sigma
$$

为二次积分(分别列出对两个变量先后次序不同的两个二次积分),其中积分区域 D 是

(1) 由直线 y = x 及抛物线  $y^{2} = 4x$  所围成的闭区域；
(2) 由 x 轴及半圆周  $x^{2}+y^{2}=r^{2}\quad(y\geqslant0)$  所围成的闭区域；
(3) 由直线 y=x, x=2 及双曲线  $y=\frac{1}{x}$  (x>0) 所围成的闭区域；
(4) 环形闭区域  $\{(x,y)\mid1\leqslant x^{2}+y^{2}\leqslant4\}$ .

5. 设 $f(x, y)$ 在 $D$ 上连续，其中 $D$ 是由直线 $y = x, y = a$ 及 $x = b$ ($b > a$) 所围成的闭区域，证明

$$
\int_ {a} ^ {b} \mathrm{d} x \int_ {a} ^ {x} f (x, y) \mathrm{d} y = \int_ {a} ^ {b} \mathrm{d} y \int_ {y} ^ {b} f (x, y) \mathrm{d} x.
$$

6. 交换下列二次积分的积分次序:

(1) $\int_0^1\mathrm{d}y\int_0^y f(x,y)\mathrm{d}x;$

(2) $\int_0^2\mathrm{d}y\int_{y^2}^{2y}f(x,y)\mathrm{d}x;$

(3) $\int_0^1\mathrm{d}y\int_{-\sqrt{1 - y^2}}^{\sqrt{1 - y^2}}f(x,y)\mathrm{d}x;$

(4) $\int_{1}^{2}\mathrm{d}x\int_{2 - x}^{\sqrt{2x - x^2}}f(x,y)\mathrm{d}y;$

(5) $\int_{1}^{\mathrm{e}}\mathrm{d}x\int_{0}^{\ln x}f(x,y)\mathrm{d}y;$

(6) $\int_0^\pi \mathrm{d}x\int_{-\sin \frac{x}{2}}^{\sin x}f(x,y)\mathrm{d}y.$

7. 设平面薄片所占的闭区域 $D$ 由直线 $x + y = 2, y = x$ 和 $x$ 轴所围成，它的面密度 $\mu(x, y) = x^2 + y^2$ 求该薄片的质量.

8. 计算由四个平面 $x = 0, y = 0, x = 1, y = 1$ 所围成的柱体被平面 $z = 0$ 及 $2x + 3y + z = 6$ 截得的立体

151

---

第十章 重积分

的体积.

9. 求由平面 $x = 0, y = 0, x + y = 1$ 所围成的柱体被平面 $z = 0$ 及抛物面 $x^{2} + y^{2} = 6 - z$ 截得的立体的体积.

10. 求由曲面 $z = x^{2} + 2y^{2}$ 及 $z = 6 - 2x^{2} - y^{2}$ 所围成的立体的体积.

11. 画出积分区域, 把积分  $\iint_{D} f(x, y) \, dx \, dy$  表示为极坐标形式的二次积分, 其中积分区域 D 是

(1)  $\{(x,y)\mid x^{2}+y^{2}\leqslant a^{2}\}(a>0)$ ;

(2) $\{(x, y) \mid x^2 + y^2 \leqslant 2x\}$;

(3) $\{(x, y) \mid a^2 \leqslant x^2 + y^2 \leqslant b^2\}$, 其中 $0 < a < b$;

(4) $\{(x, y) \mid 0 \leqslant y \leqslant 1 - x, 0 \leqslant x \leqslant 1\}$.

12. 化下列二次积分为极坐标形式的二次积分:

(1) $\int_0^1\mathrm{d}x\int_0^1 f(x,y)\mathrm{d}y;$

(2) $\int_0^2\mathrm{d}x\int_{x}^{\sqrt{3} x}f(\sqrt{x^2 + y^2})\mathrm{d}y;$

(3) $\int_0^1\mathrm{d}x\int_{1 - x}^{\sqrt{1 - x^2}}f(x,y)\mathrm{d}y;$

(4) $\int_0^1\mathrm{d}x\int_0^{x^2}f(x,y)\mathrm{d}y.$

13. 把下列积分化为极坐标形式,并计算积分值:

(1) $\int_{0}^{2a}\mathrm{d}x\int_{0}^{\sqrt{2ax - x^2}}(x^2 +y^2)\mathrm{d}y;$

(2) $\int_{0}^{a}\mathrm{d}x\int_{0}^{x}\sqrt{x^{2} + y^{2}}\mathrm{d}y;$

(3) $\int_0^1\mathrm{d}x\int_{x^2}^x (x^2 +y^2)^{-\frac{1}{2}}\mathrm{d}y;$

(4) $\int_{0}^{a}\mathrm{d}y\int_{0}^{\sqrt{a^{2} - y^{2}}}(x^{2} + y^{2})\mathrm{d}x.$

14. 利用极坐标计算下列各题:

(1) $\iint_{D} \mathrm{e}^{x^2 + y^2} \, \mathrm{d}\sigma$, 其中 $D$ 是由圆周 $x^2 + y^2 = 4$ 所围成的闭区域;

(2) $\iint_{D} \ln (1 + x^2 + y^2) \, \mathrm{d}\sigma$，其中 $D$ 是由圆周 $x^2 + y^2 = 1$ 及坐标轴所围成的在第一象限内的闭区域；

(3) $\iint_{D} \arctan \frac{y}{x} \mathrm{d}\sigma$，其中 $D$ 是由圆周 $x^{2} + y^{2} = 4, x^{2} + y^{2} = 1$ 及直线 $y = 0, y = x$ 所围成的在第一象限内的闭区域.

15. 选用适当的坐标计算下列各题:

(1) $\iint_{D} \frac{x^2}{y^2} \mathrm{d}\sigma$，其中 $D$ 是由直线 $x = 2, y = x$ 及曲线 $xy = 1$ 所围成的闭区域；

(2) $\iint_{D} \sqrt{\frac{1 - x^2 - y^2}{1 + x^2 + y^2}} \, \mathrm{d}\sigma$, 其中 $D$ 是由圆周 $x^2 + y^2 = 1$ 及坐标轴所围成的在第一象限内的闭区域;

(3) $\iint_{D}(x^{2} + y^{2})\mathrm{d}\sigma$ ，其中 $D$ 是由直线 $y = x,y = x + a,y = a,y = 3a$ （$a > 0$）所围成的闭区域；

(4) $\iint_{D} \sqrt{x^2 + y^2} \, \mathrm{d}\sigma$, 其中 $D$ 是圆环形闭区域 $\{(x, y) \mid a^2 \leqslant x^2 + y^2 \leqslant b^2\}$;

(5) $\iint_{D} \sqrt{a^2 - x^2 - y^2} \, \mathrm{d}\sigma$, 其中 $D$ 是圆形闭区域 $\{(x, y) | x^2 + y^2 \leqslant ax \mid (a > 0)$.

16. 设平面薄片所占的闭区域 $D$ 由螺线 $\rho = 2\theta$ 上一段弧 $\left(0 \leqslant \theta \leqslant \frac{\pi}{2}\right)$ 与直线 $\theta = \frac{\pi}{2}$ 所围成, 它的

152

---

第二节 二重积分的计算法

面密度为  $\mu(x,y)=x^{2}+y^{2}$ . 求这薄片的质量(图 10-27).

17. 求由平面 $y = 0, y = kx (k > 0), z = 0$ 以及球心在原点、半径为 $R$ 的上半球面所围成的在第 I 卦限内的立体的体积(图 10-28).

![](../../raw/pages_0129-0160/images/page_159_image_3.jpg)

<details>
<summary>text_image</summary>

θ=π/2
ρ=2θ
D
θ
O
A
</details>

图10-27

![](../../raw/pages_0129-0160/images/page_159_image_5.jpg)

<details>
<summary>text_image</summary>

z
O
α=arctan k
D
y
x
</details>

图10-28

18. 计算以 $xOy$ 面上的圆周 $x^{2} + y^{2} = ax (a > 0)$ 围成的闭区域为底，而以曲面 $z = x^{2} + y^{2}$ 为顶的曲顶柱体的体积.

\* 19. 作适当的变换,计算下列二重积分:

(1) $\iint_{D}(x - y)^{2}\sin^{2}(x + y)\mathrm{d}x\mathrm{d}y$ ，其中 $D$ 是平行四边形闭区域，它的四个顶点是 $(\pi ,0),(2\pi ,\pi)$ ，$(\pi ,2\pi)$ 和 $(0,\pi)$ ；
(2) $\iint_{D} x^{2} y^{2} \, \mathrm{d}x \, \mathrm{d}y$，其中 $D$ 是由两条双曲线 $xy = 1$ 和 $xy = 2$，直线 $y = x$ 和 $y = 4x$ 所围成的在第一象限内的闭区域；
(3) $\iint_{D} \mathrm{e}^{\frac{y}{x + y}} \mathrm{d}x \, \mathrm{d}y$，其中 $D$ 是由 $x$ 轴、$y$ 轴和直线 $x + y = 1$ 所围成的闭区域；
(4) $\iint_{D} \left( \frac{x^2}{a^2} + \frac{y^2}{b^2} \right) \, \mathrm{d}x \, \mathrm{d}y$，其中 $D = \left\{ (x, y) \mid \frac{x^2}{a^2} + \frac{y^2}{b^2} \leqslant 1 \right\}$.

\*20. 求由下列曲线所围成的闭区域 $D$ 的面积:

(1) D 是由曲线  $xy=4, xy=8, xy^{3}=5, xy^{3}=15$  所围成的第一象限部分的闭区域；

(2) D 是由曲线  $y=x^{3}, y=4x^{3}, x=y^{3}, x=4y^{3}$  所围成的第一象限部分的闭区域.

\* 21. 设闭区域 $D$ 是由直线 $x + y = 1, x = 0, y = 0$ 所围成，求证 $\iint_{D} \cos \left( \frac{x - y}{x + y} \right) \mathrm{d}x \mathrm{~d}y = \frac{1}{2} \sin 1.$

\* 22. 选取适当的变换,证明下列等式:

(1) $\iint_{D} f(x + y) \, \mathrm{d}x \, \mathrm{d}y = \int_{-1}^{1} f(u) \, \mathrm{d}u$，其中闭区域 $D = \{(x, y) \mid |x| + |y| \leqslant 1\}$;
(2) $\iint_{D} f(ax + by + c) \, \mathrm{d}x \, \mathrm{d}y = 2\int_{-1}^{1} \sqrt{1 - u^2} f(u \sqrt{a^2 + b^2} + c) \, \mathrm{d}u$，其中 $D = \{(x, y) | x^2 + y^2 \leqslant 1\}$，且 $a^2 + b^2 \neq 0$.

153

---

第十章 重积分

## 第三节 三重积分

## 一、三重积分的概念

定积分及二重积分作为和的极限的概念,可以很自然地推广到三重积分.

定义 设 $f(x, y, z)$ 是空间有界闭区域 $\Omega$ 上的有界函数. 将 $\Omega$ 任意分成 $n$ 个小闭区域

$$
\Delta V _ {1}, \Delta V _ {2}, \dots , \Delta V _ {n},
$$

其中  $\Delta V_{i}$  表示第 i 个小闭区域,也表示它的体积.在每个  $\Delta V_{i}$  上任取一点  $(\xi_{i},\eta_{i},\zeta_{i})$ ,作乘积  $f(\xi_{i},\eta_{i},\zeta_{i})\Delta V_{i}\quad(i=1,2,\cdots,n)$ ,并作和  $\sum_{i=1}^{n}f(\xi_{i},\eta_{i},\zeta_{i})\Delta V_{i}$ .如果当各小闭区域直径中的最大值  $\lambda\to0$  时,这和的极限总存在,且与闭区域  $\Omega$  的分法及点  $(\xi_{i},\eta_{i},\zeta_{i})$  的取法无关,那么称此极限为函数  $f(x,y,z)$  在闭区域  $\Omega$  上的三重积分.记作  $\iiint_{\Omega}f(x,y,z)\mathrm{d}V$ ,即

$$
\iiint_ {\Omega} f (x, y, z) \mathrm{d} V = \lim _ {\lambda \to 0} \sum_ {i = 1} ^ {n} f (\xi_ {i}, \eta_ {i}, \zeta_ {i}) \Delta V _ {i}, \tag {3-1}
$$

其中 $f(x,y,z)$ 叫做被积函数， $\mathrm{d}V$ 叫做体积元素， $\Omega$ 叫做积分区域

在直角坐标系中,如果用平行于坐标面的平面来划分  $\Omega$ ,那么除了包含  $\Omega$  的边界点的一些不规则小闭区域外,得到的小闭区域  $\Delta V_{i}$  为长方体.设长方体小闭区域  $\Delta V_{i}$  的边长为  $\Delta x_{j}, \Delta y_{k}$  与  $\Delta z_{l}$ ,则  $\Delta V_{i} = \Delta x_{j} \Delta y_{k} \Delta z_{l}$ .因此在直角坐标系中,有时也把体积元素 dV 记作 dx dy dz,而把三重积分记作

$$
\iiint_ {\Omega} f (x, y, z) \mathrm{d} x \mathrm{d} y \mathrm{d} z,
$$

其中 $dxdydz$ 叫做直角坐标系中的体积元素.

当函数 $f(x,y,z)$ 在闭区域 $\Omega$ 上连续时，(3-1)式右端的和的极限必定存在，也就是函数 $f(x,y,z)$ 在闭区域 $\Omega$ 上的三重积分必定存在，即函数 $f(x,y,z)$ 在 $\Omega$ 上必定可积.以后我们总假定函数 $f(x,y,z)$ 在闭区域 $\Omega$ 上是可积的.三重积分的性质与第一节中所叙述的二重积分的性质类似，这里不再重复了.

如果 $f(x,y,z)$ 表示某物体在点 $(x,y,z)$ 处的密度，$\Omega$ 是该物体所占有的空间闭区域，$f(x,y,z)$ 在 $\Omega$ 上连续，那么 $\sum_{i=1}^{n} f(\xi_i, \eta_i, \zeta_i) \Delta V_i$ 是该物体的质量 $m$ 的近似值，这个和当 $\lambda \to 0$ 时的极限就是该物体的质量 $m$，所以

154

---

第三节 三重积分

$$
m = \iiint_ {\Omega} f (x, y, z)   \mathrm{d} V.
$$

## 二、三重积分的计算

计算三重积分的基本方法是将三重积分化为三次积分来计算.下面按利用不同的坐标来分别讨论将三重积分化为三次积分的方法,且只限于叙述方法.

## 1. 利用直角坐标计算三重积分

假设平行于 $z$ 轴且穿过闭区域 $\Omega$ 内部的直线与闭区域 $\Omega$ 的边界曲面 $S$ 相交不多

于两点. 把闭区域  $\Omega$  投影到 xOy 面上, 得一平面闭区域  $D_{xy}$  (图 10-29). 以  $D_{xy}$  的边界为准线作母线平行于 z 轴的柱面. 这柱面与曲面 S 的交线从 S 中分出上、下两部分, 它们的方程分别为

$$
S _ {1}: z = z _ {1} (x, y), \quad S _ {2}: z = z _ {2} (x, y),
$$

其中 $z_{1}(x,y)$ 与 $z_{2}(x,y)$ 都是 $D_{xy}$ 上的连续函数，且$z_{1}(x,y)\leqslant z_{2}(x,y)$ .过 $D_{xy}$ 内任一点 $(x,y)$ 作平行于 $z$ 轴的直线，这直线通过曲面 $S_{1}$ 穿入 $\Omega$ 内，然后通过曲面 $S_{2}$ 穿出 $\Omega$ 外，穿入点与穿出点的竖坐标分别为$z_{1}(x,y)$ 与 $z_{2}(x,y)$

![](../../raw/pages_0161-0192/images/page_161_image_9.jpg)

<details>
<summary>text_image</summary>

z=z₂(x,y)
S₂
z₂
Ω
z₁
S₁
z=z₁(x,y)
O
a
y
Dₓᵧ
(x,y)
y=y₂(x)
b
x
y=y₁(x)
</details>

图10-29

在这种情形下,积分区域  $\Omega$  可表示为

$$
\Omega = \{(x, y, z) \mid z _ {1} (x, y) \leqslant z \leqslant z _ {2} (x, y), (x, y) \in D _ {x y} \}.
$$

先将 x, y 看做定值, 将  $f(x, y, z)$  只看做 z 的函数, 在区间  $[z_{1}(x, y), z_{2}(x, y)]$  上对 z 积分. 积分的结果是 x, y 的函数, 记为  $F(x, y)$ , 即

$$
F (x, y) = \int_ {z _ {1} (x, y)} ^ {z _ {2} (x, y)} f (x, y, z)   \mathrm{d} z.
$$

然后计算 $F(x,y)$ 在闭区域 $D_{xy}$ 上的二重积分

$$
\iint_ {D _ {x y}} F (x, y) \mathrm{d} \sigma = \iint_ {D _ {x y}} \left[ \int_ {z _ {1} (x, y)} ^ {z _ {2} (x, y)} f (x, y, z) \mathrm{d} z \right] \mathrm{d} \sigma .
$$

假如闭区域

$$
D _ {x y} = \{(x, y) | y _ {1} (x) \leqslant y \leqslant y _ {2} (x), a \leqslant x \leqslant b \},
$$

把这个二重积分化为二次积分,于是得到三重积分的计算公式

$$
\iiint_ {\Omega} f (x, y, z) \mathrm{d} V = \int_ {a} ^ {b} \mathrm{d} x \int_ {y _ {1} (x)} ^ {y _ {2} (x)} \mathrm{d} y \int_ {z _ {1} (x, y)} ^ {z _ {2} (x, y)} f (x, y, z) \mathrm{d} z. \tag {3-2}
$$

公式(3-2)把三重积分化为先对z、次对y、最后对x的三次积分.

如果平行于 $x$ 轴或 $y$ 轴且穿过闭区域 $\Omega$ 内部的直线与 $\Omega$ 的边界曲面 $S$ 相交不多

155

---

第十章 重积分

于两点,也可把闭区域 $\Omega$ 投影到 $yOz$ 面上或 $zOx$ 面上,这样便可把三重积分化为按其他顺序的三次积分.如果平行于坐标轴且穿过闭区域 $\Omega$ 内部的直线与边界曲面 $S$ 的交点多于两个,也可像处理二重积分那样,把 $\Omega$ 分成若干部分,使 $\Omega$ 上的三重积分化为各部分闭区域上的三重积分的和.

例1 计算三重积分 $\iiint_{\Omega} x \, \mathrm{d}x \, \mathrm{d}y \, \mathrm{d}z$，其中 $\Omega$ 为三个坐标面及平面 $x + 2y + z = 1$ 所围成的闭区域.

解 作闭区域  $\Omega$  如图 10-30 所示.

将  $\Omega$  投影到 xOy 面上, 得投影区域  $D_{xy}$  为三角形闭区域 OAB. 直线 OA, OB 及 AB 的方程依次为 y = 0, x = 0 及  $x + 2y = 1$ , 所以

$$
D _ {x y} = \left\{(x, y)   \Big |   0 \leqslant y \leqslant \frac {1 - x}{2}, 0 \leqslant x \leqslant 1 \right\}.
$$

在  $D_{xy}$  内任取一点  $(x,y)$ ，过此点作平行于 z 轴的直线，该直线通过平面 z=0 穿入  $\Omega$  内，然后通过平面 z=1-x-2y 穿出  $\Omega$  外.

![](../../raw/pages_0161-0192/images/page_162_image_7.jpg)

<details>
<summary>text_image</summary>

z
C(0,0,1)
O
B(1,½,0)
y
Dxy
A(1,0,0)
x
</details>

图10-30

于是,由公式(3-2)得

$$
\begin{array}{l} \iiint_ {\Omega} x \mathrm{d} x \mathrm{d} y \mathrm{d} z = \int_ {0} ^ {1} \mathrm{d} x \int_ {0} ^ {\frac {1 - x}{2}} \mathrm{d} y \int_ {0} ^ {1 - x - 2 y} x \mathrm{d} z = \int_ {0} ^ {1} x \mathrm{d} x \int_ {0} ^ {\frac {1 - x}{2}} (1 - x - 2 y) \mathrm{d} y \\ = \frac {1}{4} \int_ {0} ^ {1} (x - 2 x ^ {2} + x ^ {3}) \mathrm{d} x = \frac {1}{4 8}. \\ \end{array}
$$

有时,我们计算一个三重积分也可以化为先计算一个二重积分、再计算一个定积分,即有下述计算公式.

设空间闭区域

$$
\Omega = \{(x, y, z) \mid (x, y) \in D _ {z}, c _ {1} \leqslant z \leqslant c _ {2} \},
$$

其中 $D_{z}$ 是竖坐标为 $z$ 的平面截闭区域 $\Omega$ 所得到的一个平面闭区域（图10-31），则有

$$
\iiint_ {\Omega} f (x, y, z) \mathrm{d} V = \int_ {c _ {1}} ^ {c _ {2}} \mathrm{d} z \iint_ {D _ {z}} f (x, y, z) \mathrm{d} x \mathrm{d} y. \tag {3-3}
$$

![](../../raw/pages_0161-0192/images/page_162_image_16.jpg)

<details>
<summary>text_image</summary>

z
c₂
Ω
z
Dₓ
c₁
O
y
x
</details>

图10-31

例2 计算三重积分 $\iiint_{\Omega} z^2 \, \mathrm{d}x \, \mathrm{d}y \, \mathrm{d}z$，其中 $\Omega$ 是由椭球面 $\frac{x^2}{a^2} + \frac{y^2}{b^2} + \frac{z^2}{c^2} = 1$ 所围成的空间闭区域.

解 空间闭区域 $\Omega$ 可表示为

156

---

第三节 三重积分

$$
\left\{(x, y, z) \left| \frac {x ^ {2}}{a ^ {2}} + \frac {y ^ {2}}{b ^ {2}} \leqslant 1 - \frac {z ^ {2}}{c ^ {2}}, - c \leqslant z \leqslant c \right. \right\},
$$

如图 10-32 所示. 由公式(3-3)得

$$
\begin{array}{l} \iiint_ {\Omega} z ^ {2} \mathrm{d} x \mathrm{d} y \mathrm{d} z = \int_ {- c} ^ {c} z ^ {2} \mathrm{d} z \iint_ {D _ {z}} \mathrm{d} x \mathrm{d} y \\ = \pi a b \int_ {- c} ^ {c} \left(1 - \frac {z ^ {2}}{c ^ {2}}\right) z ^ {2} \mathrm{d} z = \frac {4}{1 5} \pi a b c ^ {3}. \\ \end{array}
$$

## 2. 利用柱面坐标计算三重积分

设 $M(x,y,z)$ 为空间内一点，并设点 $M$ 在 $xOy$ 面上的投影 $P$ 的极坐标为 $(\rho, \theta)$，则这样的三个数 $\rho, \theta, z$ 就叫做点 $M$ 的柱面坐标（图10-33），这里规定 $\rho, \theta, z$ 的变化范围为

$$
\begin{array}{l} 0 \leqslant \rho <   + \infty , \\ 0 \leqslant \theta \leqslant 2 \pi , \\ - \infty <   z <   + \infty . \\ \end{array}
$$

三组坐标面分别为

$\rho=$ 常数, 即以 z 轴为轴的圆柱面;

θ=常数,即过z轴的半平面;

z=常数,即与xOy面平行的平面.

显然,点 M 的直角坐标与柱面坐标的关系为

$$
\left\{ \begin{array}{l} x = \rho \cos \theta , \\ y = \rho \sin \theta , \\ z = z. \end{array} \right. \tag {3-4}
$$

现在要把三重积分 $\iiint_{\Omega} f(x, y, z) \mathrm{d}V$ 中的变量变换为柱面坐标. 为此, 用三组坐标面 $\rho =$ 常数, $\theta =$ 常数, $z =$ 常数把 $\Omega$ 分成许多小闭区域, 除了含 $\Omega$ 的边界点的一些不规则小闭区域外, 这种小闭区域都是柱体. 今考虑由 $\rho, \theta$ 和 $z$ 各取得微小增量 $\mathrm{d}\rho, \mathrm{d}\theta$ 和 $\mathrm{d}z$ 所成的柱体的体积 (图10-34). 这个体积等于高与底面积的乘积. 现在高为 $\mathrm{d}z$ 、底面积在不计高阶无穷小时为 $\rho \mathrm{d}\rho \mathrm{d}\theta$ （即极坐标系中的面积元素）, 于是得

$$
\mathrm{d} V = \rho \mathrm{d} \rho \mathrm{d} \theta \mathrm{d} z,
$$

![](../../raw/pages_0161-0192/images/page_163_image_15.jpg)

<details>
<summary>text_image</summary>

z
c
z - D₂
O
a
D₀
b
y
x
</details>

图10-32

![](../../raw/pages_0161-0192/images/page_163_image_17.jpg)

<details>
<summary>text_image</summary>

z
M(x,y,z)
z
O
y
P(ρ,θ)
θ
x
</details>

图10-33

![](../../raw/pages_0161-0192/images/page_163_image_19.jpg)

<details>
<summary>text_image</summary>

z
ρdθ
dρ
dz
ρ
O
y
x
dθ
</details>

图10-34

这就是柱面坐标系中的体积元素.再注意到关系式(3-4)，就有

157

---

第十章 重积分

$$
\iiint_ {\Omega} f (x, y, z) \mathrm{d} x \mathrm{d} y \mathrm{d} z = \iiint_ {\Omega} F (\rho , \theta , z) \rho \mathrm{d} \rho \mathrm{d} \theta \mathrm{d} z, \tag {3-5}
$$

其中  $F(\rho,\theta,z)=f(\rho\cos\theta,\rho\sin\theta,z)$ . (3-5) 式就是把三重积分的变量从直角坐标变换为柱面坐标的公式. 至于变量变换为柱面坐标后的三重积分的计算, 则可化为三次积分来进行. 化为三次积分时, 积分限是根据  $\rho,\theta$  和 z 在积分区域  $\Omega$  中的变化范围来确定的, 下面通过例子来说明.

例3 利用柱面坐标计算三重积分 $\iiint_{\Omega} z \, \mathrm{d}x \, \mathrm{d}y \, \mathrm{d}z$，其中 $\Omega$ 是由曲面 $z = x^2 + y^2$ 与平面 $z = 4$ 所围成的闭区域.

解 把闭区域  $\Omega$  投影到 xOy 面上, 得半径为 2 的圆形闭区域

$$
D _ {x y} = \{(\rho , \theta) | 0 \leqslant \rho \leqslant 2, 0 \leqslant \theta \leqslant 2 \pi \}.
$$

在 $D_{xy}$ 内任取一点 $(\rho, \theta)$, 过此点作平行于 $z$ 轴的直线, 此直线通过曲面 $z = x^2 + y^2$ 穿入 $\Omega$ 内, 然后通过平面 $z = 4$ 穿出 $\Omega$ 外. 因此闭区域 $\Omega$ 可用不等式

$$
\rho^ {2} \leqslant z \leqslant 4, \quad 0 \leqslant \rho \leqslant 2, \quad 0 \leqslant \theta \leqslant 2 \pi
$$

来表示.于是

$$
\begin{array}{l} \iiint_ {\Omega} z \mathrm{d} x \mathrm{d} y \mathrm{d} z = \iiint_ {\Omega} z \rho \mathrm{d} \rho \mathrm{d} \theta \mathrm{d} z = \int_ {0} ^ {2 \pi} \mathrm{d} \theta \int_ {0} ^ {2} \rho \mathrm{d} \rho \int_ {\rho^ {2}} ^ {4} z \mathrm{d} z \\ = \frac {1}{2} \int_ {0} ^ {2 \pi} \mathrm{d} \theta \int_ {0} ^ {2} \rho (1 6 - \rho^ {4}) \mathrm{d} \rho = \frac {1}{2} \cdot 2 \pi \left[ 8 \rho^ {2} - \frac {1}{6} \rho^ {6} \right] _ {0} ^ {2} = \frac {6 4}{3} \pi . \\ \end{array}
$$

## \*3. 利用球面坐标计算三重积分

设 $M(x,y,z)$ 为空间内一点，则点 $M$ 也可用这样三个有次序的数 $r, \varphi$ 和 $\theta$ 来确定，其中 $r$ 为原点 $O$ 与点 $M$ 间的距离，$\varphi$ 为有向线段 $\overrightarrow{OM}$ 与 $z$ 轴正向所夹的角，$\theta$ 为从 $z$ 轴

正向来看自 $x$ 轴按逆时针方向转到有向线段 $\overrightarrow{OP}$ 的角，这里 $P$ 为点 $M$ 在 $xOy$ 面上的投影（图10-35).这样的三个数 $r,\varphi$ 和 $\theta$ 叫做点 $M$ 的球面坐标，这里 $r,\varphi$ 和 $\theta$ 的变化范围为

$$
\begin{array}{l} 0 \leqslant r <   + \infty , \\ 0 \leqslant \varphi \leqslant \pi , \\ 0 \leqslant \theta \leqslant 2 \pi . \\ \end{array}
$$

![](../../raw/pages_0161-0192/images/page_164_image_14.jpg)

<details>
<summary>text_image</summary>

z
M
r
φ
z
O
x
θ
A
y
P
y
x
</details>

图10-35

三组坐标面分别为

r=常数,即以原点为球心的球面;

$\varphi=$ 常数, 即以原点为顶点、z轴为轴的圆锥面;

θ=常数,即过z轴的半平面.

![](../../raw/pages_0161-0192/images/page_164_image_20.jpg)

释疑解难

10-2

![](../../raw/pages_0161-0192/images/page_164_image_23.jpg)

例题精讲

10-3

158

---

第三节 三重积分

设点 $M$ 在 $xOy$ 面上的投影为 $P$, 点 $P$ 在 $x$ 轴上的投影为 $A$, 则 $OA = x, AP = y, PM = z$. 又

$$
O P = r \sin \varphi , \quad z = r \cos \varphi .
$$

因此,点 M 的直角坐标与球面坐标的关系为

$$
\left\{ \begin{array}{l} x = O P \cos \theta = r \sin \varphi \cos \theta , \\ y = O P \sin \theta = r \sin \varphi \sin \theta , \\ z = r \cos \varphi . \end{array} \right. \tag {3-6}
$$

为了把三重积分中的变量从直角坐标变换为球面坐标,用三组坐标面 r=常数, $\varphi=$ 常数, $\theta=$ 常数把积分区域  $\Omega$  分成许多小闭区域.考虑由 r, $\varphi$  和  $\theta$  各取得微小增量 dr, $d\varphi$  和  $d\theta$  所成的六面体的体积(图 10-36).不计高阶无穷小,可把这个六面体看做长方体,其经线方向的长为  $rd\varphi$ ,纬线方向的宽为  $r\sin\varphi d\theta$ ,向径方向的高为 dr,于是得

![](../../raw/pages_0161-0192/images/page_165_image_6.jpg)

<details>
<summary>text_image</summary>

z
dr
rsin φdθ
r sin φ
r
φ
dφ
O
x
y
θ
dθ
</details>

图10-36

$$
\mathrm{d} V = r ^ {2} \sin \varphi \mathrm{d} r \mathrm{d} \varphi \mathrm{d} \theta ,
$$

这就是球面坐标系中的体积元素.再注意到关系式(3-6)，就有

$$
\iiint_ {\Omega} f (x, y, z) \mathrm{d} x \mathrm{d} y \mathrm{d} z = \iiint_ {\Omega} F (r, \varphi , \theta) r ^ {2} \sin \varphi \mathrm{d} r \mathrm{d} \varphi \mathrm{d} \theta , \tag {3-7}
$$

其中 $F(r, \varphi, \theta) = f(r\sin \varphi \cos \theta, r\sin \varphi \sin \theta, r\cos \varphi)$. (3-7)式就是把三重积分的变量从直角坐标变换为球面坐标的公式.

要计算变量变换为球面坐标后的三重积分, 可把它化为对 r、对  $\varphi$  及对  $\theta$  的三次积分.

若积分区域  $\Omega$  的边界曲面是一个包围原点在内的闭曲面, 其球面坐标方程为  $r = r(\varphi, \theta)$ , 则

$$
I = \iiint_ {\Omega} F (r, \varphi , \theta) r ^ {2} \sin \varphi \mathrm{d} r \mathrm{d} \varphi \mathrm{d} \theta = \int_ {0} ^ {2 \pi} \mathrm{d} \theta \int_ {0} ^ {\pi} \mathrm{d} \varphi \int_ {0} ^ {r (\varphi , \theta)} F (r, \varphi , \theta) r ^ {2} \sin \varphi \mathrm{d} r.
$$

当积分区域  $\Omega$  为球面 r=a 所围成时, 则

$$
I = \int_ {0} ^ {2 \pi} \mathrm{d} \theta \int_ {0} ^ {\pi} \mathrm{d} \varphi \int_ {0} ^ {a} F (r, \varphi , \theta) r ^ {2} \sin \varphi \mathrm{d} r.
$$

特别地，当 $F(r,\varphi ,\theta) = 1$ 时，由上式即得球的体积

$$
V = \int_ {0} ^ {2 \pi} \mathrm{d} \theta \int_ {0} ^ {\pi} \sin \varphi \mathrm{d} \varphi \int_ {0} ^ {a} r ^ {2} \mathrm{d} r = 2 \pi \cdot 2 \cdot \frac {a ^ {3}}{3} = \frac {4}{3} \pi a ^ {3},
$$

这是我们所熟知的结果.

例 4 求半径为 a 的球面与半顶角为  $\alpha$  的内接锥面所围成的立体(图 10-37)的体积.

解 设球面通过原点 O, 球心在 z 轴上, 又内接锥面的顶点在原点 O, 其轴与 z 轴

159

---

第十章 重积分

重合, 则球面方程为 $r = 2a\cos \varphi$, 锥面方程为 $\varphi = \alpha$. 因为立体所占有的空间闭区域 $\Omega$ 可用不等式

$$
0 \leqslant r \leqslant 2 a \cos \varphi , \quad 0 \leqslant \varphi \leqslant \alpha , \quad 0 \leqslant \theta \leqslant 2 \pi
$$

来表示,所以

$$
\begin{array}{l} V = \iiint_ {\Omega} r ^ {2} \sin \varphi \mathrm{d} r \mathrm{d} \varphi \mathrm{d} \theta = \int_ {0} ^ {2 \pi} \mathrm{d} \theta \int_ {0} ^ {\alpha} \mathrm{d} \varphi \int_ {0} ^ {2 a \cos \varphi} r ^ {2} \sin \varphi \mathrm{d} r \\ = 2 \pi \int_ {0} ^ {\alpha} \sin \varphi \mathrm{d} \varphi \int_ {0} ^ {2 a \cos \varphi} r ^ {2} \mathrm{d} r = \frac {1 6 \pi a ^ {3}}{3} \int_ {0} ^ {\alpha} \cos^ {3} \varphi \sin \varphi \mathrm{d} \varphi \\ = \frac {4 \pi a ^ {3}}{3} (1 - \cos^ {4} \alpha). \\ \end{array}
$$

![](../../raw/pages_0161-0192/images/page_166_image_5.jpg)

<details>
<summary>text_image</summary>

z
2a
M
r
φ
α
O
y
x
</details>

图10-37

## 习题10-3

1. 化三重积分 $I = \iiint_{\Omega} f(x, y, z) \, \mathrm{d}x \, \mathrm{d}y \, \mathrm{d}z$ 为三次积分，其中积分区域 $\Omega$ 分别是

(1) 由双曲抛物面 xy=z 及平面  $x+y-1=0, z=0$  所围成的闭区域；
(2) 由曲面  $z = x^{2} + y^{2}$  及平面 z = 1 所围成的闭区域；
(3) 由曲面  $z=x^{2}+2y^{2}$  及  $z=2-x^{2}$  所围成的闭区域；
(4) 由曲面 $cz = xy (c > 0), \frac{x^2}{a^2} + \frac{y^2}{b^2} = 1, z = 0$ 所围成的在第I卦限内的闭区域.

2. 设有一物体占有空间闭区域 $\Omega = \{(x, y, z) \mid 0 \leqslant x \leqslant 1, 0 \leqslant y \leqslant 1, 0 \leqslant z \leqslant 1\}$, 在点 $(x, y, z)$ 处的密度为 $\rho(x, y, z) = x + y + z$, 计算该物体的质量.
3. 如果三重积分 $\iiint_{\Omega} f(x, y, z) \, \mathrm{d}x \, \mathrm{d}y \, \mathrm{d}z$ 的被积函数 $f(x, y, z)$ 是三个函数 $f_1(x), f_2(y), f_3(z)$ 的乘积，即 $f(x, y, z) = f_1(x)f_2(y)f_3(z)$，积分区域 $\Omega = \{(x, y, z) \mid a \leqslant x \leqslant b, c \leqslant y \leqslant d, l \leqslant z \leqslant m\}$，证明这个三重积分等于三个定积分的乘积，即

$$
\iiint_ {\Omega} f _ {1} (x) f _ {2} (y) f _ {3} (z) \mathrm{d} x \mathrm{d} y \mathrm{d} z = \int_ {a} ^ {b} f _ {1} (x) \mathrm{d} x \int_ {c} ^ {d} f _ {2} (y) \mathrm{d} y \int_ {l} ^ {m} f _ {3} (z) \mathrm{d} z.
$$

4. 计算 $\iiint_{\Omega} xy^2 z^3 \, \mathrm{d}x \, \mathrm{d}y \, \mathrm{d}z$，其中 $\Omega$ 是由曲面 $z = xy$ 与平面 $y = x, x = 1$ 和 $z = 0$ 所围成的闭区域.

5. 计算 $\iiint_{\Omega} \frac{\mathrm{d}x \, \mathrm{d}y \, \mathrm{d}z}{(1 + x + y + z)^3}$, 其中 $\Omega$ 为平面 $x = 0, y = 0, z = 0, x + y + z = 1$ 所围成的四面体.

6. 计算 $\iiint_{\Omega} xyz \, \mathrm{d}x \, \mathrm{d}y \, \mathrm{d}z$，其中 $\Omega$ 为球面 $x^2 + y^2 + z^2 = 1$ 及三个坐标面所围成的在第 I 卦限内的闭区域.

7. 计算 $\iiint_{\Omega} xz \, \mathrm{d}x \, \mathrm{d}y \, \mathrm{d}z$，其中 $\Omega$ 是由平面 $z = 0, z = y, y = 1$ 以及抛物柱面 $y = x^2$ 所围成的闭区域。

8. 计算 $\iiint_{\Omega} z \, \mathrm{d}x \, \mathrm{d}y \, \mathrm{d}z$，其中 $\Omega$ 是由锥面 $z = \frac{h}{R} \sqrt{x^2 + y^2}$ 与平面 $z = h (R > 0, h > 0)$ 所围成的闭区域.

160

---

第四节 重积分的应用

9. 利用柱面坐标计算下列三重积分:

(1) $\iiint_{\Omega} z \, \mathrm{d}V$，其中 $\Omega$ 是由曲面 $z = \sqrt{2 - x^2 - y^2}$ 及 $z = x^2 + y^2$ 所围成的闭区域；
(2) $\iiint_{\Omega}(x^{2}+y^{2})\mathrm{d}V$ ,其中 $\Omega$ 是由曲面 $x^{2}+y^{2}=2z$ 及平面z=2所围成的闭区域.

\*10. 利用球面坐标计算下列三重积分:

(1) $\iiint_{\Omega} (x^2 + y^2 + z^2) \, \mathrm{d}V$，其中 $\Omega$ 是由球面 $x^2 + y^2 + z^2 = 1$ 所围成的闭区域；
(2) $\iiint_{\Omega} z \, \mathrm{d}V$，其中闭区域 $\Omega = \{(x, y, z) | x^2 + y^2 + (z - a)^2 \leqslant a^2, x^2 + y^2 \leqslant z^2\}$.

11. 选用适当的坐标计算下列三重积分:

(1) $\iiint_{\Omega} xy \, \mathrm{d}V$, 其中 $\Omega$ 为柱面 $x^2 + y^2 = 1$ 及平面 $z = 1, z = 0, x = 0, y = 0$ 所围成的在第 I 卦限内的闭区域;
\* (2) $\iiint_{\Omega} \sqrt{x^2 + y^2 + z^2} \, \mathrm{d}V$, 其中 $\Omega$ 是由球面 $x^2 + y^2 + z^2 = z$ 所围成的闭区域;
(3) $\iiint_{\Omega} (x^2 + y^2) \, \mathrm{d}V$，其中 $\Omega$ 是由曲面 $4z^2 = 25(x^2 + y^2)$ 及平面 $z = 5$ 所围成的闭区域；
\* (4) $\iiint_{\Omega} (x^2 + y^2) \, \mathrm{d}V$, 其中闭区域 $\Omega = \{(x, y, z) | 0 < a \leqslant \sqrt{x^2 + y^2 + z^2} \leqslant A, z \geqslant 0\}$;
(5) $\iiint_{\Omega} (y^2 + z^2) \, \mathrm{d}V$，其中 $\Omega$ 是由抛物面 $x = y^2 + z^2$ 与圆锥面 $x = 2 - \sqrt{y^2 + z^2}$ 所围成的闭区域.

12. 利用三重积分计算下列由曲面所围成的立体的体积:

(1) $z=6-x^{2}-y^{2}$ 及 $z=\sqrt{x^{2}+y^{2}}$;
\* (2) $x^{2} + y^{2} + z^{2} = 2az$ ($a > 0$) 及 $x^{2} + y^{2} = z^{2}$ (含有 $z$ 轴的部分);
(3) $z=\sqrt{x^{2}+y^{2}}$ 及 $z=x^{2}+y^{2}$;
(4) $z=\sqrt{5-x^{2}-y^{2}}$ 及 $x^{2}+y^{2}=4z.$

\* 13. 求球体 $r \leqslant a$ 位于锥面 $\varphi = \frac{\pi}{3}$ 和 $\varphi = \frac{2}{3}\pi$ 之间的部分的体积.
14. 求上、下分别为球面  $x^{2}+y^{2}+z^{2}=2$  和抛物面  $z=x^{2}+y^{2}$  所围立体的体积.
\* 15. 球心在原点、半径为 $R$ 的球, 在其上任意一点的密度的大小与这点到球心的距离成正比, 求这球的质量.

## 第四节 重积分的应用

由前面的讨论可知,曲顶柱体的体积、平面薄片的质量可用二重积分计算,空间物体的质量可用三重积分计算.本节中我们将把定积分应用中的元素法推广到重积分的应用中,利用重积分的元素法来讨论重积分在几何、物理上的一些其他应用.

161

---

第十章 重积分

## 一、曲面的面积

设曲面 $S$ 由方程

$$
z = f (x, y)
$$

给出, D 为曲面 S 在 xOy 面上的投影区域, 函数  $f(x,y)$  在 D 上具有连续偏导数  $f_{x}(x,y)$  和  $f_{y}(x,y)$ . 要计算曲面 S 的面积 A.

在闭区域 D 上任取一直径很小的闭区域  $d\sigma$  （这小闭区域的面积也记作  $d\sigma$ ）. 在

$\mathrm{d}\sigma$ 上取一点 $P(x,y)$，曲面 $S$ 上对应地有一点 $M(x,y,f(x,y))$，点 $M$ 在 $xOy$ 面上的投影即点 $P$. 点 $M$ 处曲面 $S$ 的切平面设为 $T$（图10-38）. 以小闭区域 $\mathrm{d}\sigma$ 的边界为准线作母线平行于 $z$ 轴的柱面，这柱面在曲面 $S$ 上截下一小片曲面，在切平面 $T$ 上截下一小片平面. 由于 $\mathrm{d}\sigma$ 的直径很小，切平面 $T$ 上的那一小片平面的面积 $\mathrm{d}A$ 可以近似代替相应的那小片曲面的面积. 设点 $M$ 处曲面 $S$ 上的法线（方向朝上）与 $z$ 轴所成的角为 $\gamma$，则

![](../../raw/pages_0161-0192/images/page_168_image_7.jpg)

<details>
<summary>text_image</summary>

z
T
M
dA
S
O
y
P
dσ
x
γ
</details>

图10-38

$$
\mathrm{d} A = \frac {\mathrm{d} \sigma}{\cos \gamma} ①.
$$

因为

① 设两平面 $\Pi_1, \Pi_2$ 的夹角为 $\theta$（取锐角），$\Pi_1$ 上的闭区域 $D$ 在 $\Pi_2$ 上的投影区域为 $D_0$，则 $D$ 的面积 $A$ 与 $D_0$ 的面积 $\sigma$ 之间有关系

$$
A = \frac {\sigma}{\cos \theta}.
$$

事实上,先假定 D 是矩形闭区域,且其一边平行于平面  $\Pi_{1},\Pi_{2}$  的交线 l, 边长为 a, 另一边长为 b (图10-39), 则  $D_{0}$  也是矩形闭区域, 且边长分别为 a 及  $b\cos\theta$ , 从而

$$
\sigma = a b \cos \theta = A \cos \theta ,
$$

即

$$
A = \frac {\sigma}{\cos \theta}.
$$

在一般情况, 可把 D 分成上述类型的 m 个小矩形闭区域(不计含边界点的不规则部分), 则小矩形闭区域的面积  $A_{k}$  及其投影区域的面积

$\sigma_{k}$ 之间符合 $A_{k} = \frac{\sigma_{k}}{\cos\theta}$ （$k = 1,2,\dots ,m$），从而 $\sum_{k = 1}^{m}A_{k} = \frac{\sum_{k = 1}^{m}\sigma_{k}}{\cos\theta}$. 使各小闭区域的直径中的最大者趋于零，取极限便得 $A = \frac{\sigma}{\cos\theta}$.

![](../../raw/pages_0161-0192/images/page_168_image_19.jpg)

<details>
<summary>text_image</summary>

Π₁
a b
l
θ
a σ
bcos θ
Π₂
</details>

图10-39

162

---

第四节 重积分的应用

$$
\cos \gamma = \frac {1}{\sqrt {1 + f _ {x} ^ {2} (x , y) + f _ {y} ^ {2} (x , y)}},
$$

所以

$$
\mathrm{d} A = \sqrt {1 + f _ {x} ^ {2} (x , y) + f _ {y} ^ {2} (x , y)} \mathrm{d} \sigma .
$$

这就是曲面 $S$ 的面积元素, 以它为被积表达式在闭区域 $D$ 上积分, 得

$$
A = \iint_ {D} \sqrt {1 + f _ {x} ^ {2} (x , y) + f _ {y} ^ {2} (x , y)}   \mathrm{d} \sigma .
$$

上式也可写成

$$
A = \iint_ {D} \sqrt {1 + \left(\frac {\partial z}{\partial x}\right) ^ {2} + \left(\frac {\partial z}{\partial y}\right) ^ {2}} \mathrm{d} x \mathrm{d} y.
$$

这就是计算曲面面积的公式.

设曲面的方程为 $x = g(y,z)$ 或 $y = h(z,x)$，可分别把曲面投影到 $yOz$ 面上（投影区域记作 $D_{yz}$）或 $zOx$ 面上（投影区域记作 $D_{zx}$），类似地可得

$$
A = \iint_ {D _ {y z}} \sqrt {1 + \left(\frac {\partial x}{\partial y}\right) ^ {2} + \left(\frac {\partial x}{\partial z}\right) ^ {2}} \mathrm{d} y \mathrm{d} z,
$$

或

$$
A = \iint_ {D _ {z x}} \sqrt {1 + \left(\frac {\partial y}{\partial z}\right) ^ {2} + \left(\frac {\partial y}{\partial x}\right) ^ {2}} \mathrm{d} z \mathrm{d} x.
$$

例 1 求半径为 a 的球的表面积.

解 取上半球面方程为 $z = \sqrt{a^2 - x^2 - y^2}$，则它在 $xOy$ 面上的投影区域 $D = \{(x, y) | x^2 + y^2 \leqslant a^2\}$.

由 $\frac{\partial z}{\partial x} = \frac{-x}{\sqrt{a^2 - x^2 - y^2}},\frac{\partial z}{\partial y} = \frac{-y}{\sqrt{a^2 - x^2 - y^2}}$ 得

$$
\sqrt {1 + \left(\frac {\partial z}{\partial x}\right) ^ {2} + \left(\frac {\partial z}{\partial y}\right) ^ {2}} = \frac {a}{\sqrt {a ^ {2} - x ^ {2} - y ^ {2}}}.
$$

因为这函数在闭区域 $D$ 上无界, 我们不能直接应用曲面面积公式. 所以先取区域 $D_{1} = \{(x, y) | x^{2} + y^{2} \leqslant b^{2}\}$ ($0 < b < a$) 为积分区域, 算出相应于 $D_{1}$ 上的球面面积 $A_{1}$ 后, 令 $b \to a$ 取 $A_{1}$ 的极限①就得半球面的面积.

$$
A _ {1} = \iint_ {D _ {1}} \frac {a}{\sqrt {a ^ {2} - x ^ {2} - y ^ {2}}} \mathrm{d} x \mathrm{d} y,
$$

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 这极限就是函数 $\frac{a}{\sqrt{a^2 - x^2 - y^2}}$ 在闭区域 $D$ 上的所谓反常二重积分.</span></small>

163

图

例题精讲

10-4

---

第十章 重积分

利用极坐标,得

$$
A _ {1} = \iint_ {D _ {1}} \frac {a}{\sqrt {a ^ {2} - \rho^ {2}}} \rho \mathrm{d} \rho \mathrm{d} \theta = a \int_ {0} ^ {2 \pi} \mathrm{d} \theta \int_ {0} ^ {b} \frac {\rho \mathrm{d} \rho}{\sqrt {a ^ {2} - \rho^ {2}}} = 2 \pi a \int_ {0} ^ {b} \frac {\rho \mathrm{d} \rho}{\sqrt {a ^ {2} - \rho^ {2}}} = 2 \pi a (a - \sqrt {a ^ {2} - b ^ {2}}).
$$

图

释疑解难

10-3

于是

$$
\lim _ {b \to a} A _ {1} = \lim _ {b \to a} 2 \pi a (a - \sqrt {a ^ {2} - b ^ {2}}) = 2 \pi a ^ {2}.
$$

这就是半个球面的面积,因此整个球面的面积为

$$
A = 4 \pi a ^ {2}.
$$

例 2 设有一颗地球同步轨道通信卫星,距地面的高度为 h=36 000 km,运行的角速度与地球自转的角速度相同.试计算该通信卫星的覆盖面积与地球表面积的比值(地球半径 R=6 400 km).

解 取地心为坐标原点, 地心到通信卫星中心的连线为 z 轴, 建立坐标系, 如图 10-40 所示.

通信卫星覆盖的曲面 $\Sigma$ 是上半球面被半顶角为 $\alpha$ 的圆锥面所截得的部分. $\Sigma$ 的方程为

$$
z = \sqrt {R ^ {2} - x ^ {2} - y ^ {2}}, \quad x ^ {2} + y ^ {2} \leqslant R ^ {2} \sin^ {2} \alpha .
$$

于是通信卫星的覆盖面积为

$$
\begin{array}{l} A = \iint_ {D _ {x y}} \sqrt {1 + \left(\frac {\partial z}{\partial x}\right) ^ {2} + \left(\frac {\partial z}{\partial y}\right) ^ {2}} \mathrm{d} x \mathrm{d} y \\ = \iint_ {D _ {x y}} \frac {R}{\sqrt {R ^ {2} - x ^ {2} - y ^ {2}}} \mathrm{d} x \mathrm{d} y. \\ \end{array}
$$

![](../../raw/pages_0161-0192/images/page_170_image_16.jpg)

<details>
<summary>text_image</summary>

z
α
O
y
x
</details>

图10-40

其中 $D_{xy}$ 是曲面 $\Sigma$ 在 $xOy$ 面上的投影区域，$D_{xy} = \{(x,y) | x^2 + y^2 \leqslant R^2 \sin^2 \alpha\}$.

利用极坐标,得

$$
A = \int_ {0} ^ {2 \pi} \mathrm{d} \theta \int_ {0} ^ {R \sin \alpha} \frac {R}{\sqrt {R ^ {2} - \rho^ {2}}} \rho \mathrm{d} \rho = 2 \pi R \int_ {0} ^ {R \sin \alpha} \frac {\rho}{\sqrt {R ^ {2} - \rho^ {2}}} \mathrm{d} \rho = 2 \pi R ^ {2} (1 - \cos \alpha).
$$

由于  $\cos\alpha=\frac{R}{R+h}$ ，代入上式得

$$
A = 2 \pi R ^ {2} \left(1 - \frac {R}{R + h}\right) = 2 \pi R ^ {2} \cdot \frac {h}{R + h}.
$$

由此得这颗通信卫星的覆盖面积与地球表面积之比为

$$
\frac {A}{4 \pi R ^ {2}} = \frac {h}{2 (R + h)} = \frac {3 6 \times 1 0 ^ {3}}{2 (3 6 + 6 . 4) \times 1 0 ^ {3}} \approx 42.5 \%.
$$

由以上结果可知,卫星覆盖了全球三分之一以上的面积,故使用三颗相隔 $\frac{2}{3}\pi$ 角度的通信卫星就可以覆盖几乎地球全部表面.

164

---

第四节 重积分的应用

\* 利用曲面的参数方程求曲面的面积

若曲面 $S$ 由参数方程

$$
\left\{ \begin{array}{l} x = x (u, v), \\ y = y (u, v), \quad (u, v) \in D \\ z = z (u, v) \end{array} \right.
$$

给出,其中 D 是一个平面有界闭区域,又  $x(u,v)$ ,  $y(u,v)$ ,  $z(u,v)$  在 D 上具有连续的一阶偏导数,且

$$
\frac {\partial (x , y)}{\partial (u , v)}, \quad \frac {\partial (y , z)}{\partial (u , v)}, \quad \frac {\partial (z , x)}{\partial (u , v)}
$$

不全为零,则曲面 S 的面积

$$
A = \iint_ {D} \sqrt {E G - F ^ {2}}   \mathrm{d} u \mathrm{d} v,
$$

其中

$$
E = x _ {u} ^ {2} + y _ {u} ^ {2} + z _ {u} ^ {2}, \quad F = x _ {u} x _ {v} + y _ {u} y _ {v} + z _ {u} z _ {v}, \quad G = x _ {v} ^ {2} + y _ {v} ^ {2} + z _ {v} ^ {2}.
$$

下面我们对例 2 用球面的参数方程按上述公式来进行计算.

$\Sigma$ 的参数方程为

$$
\left\{ \begin{array}{l} x = R \sin \varphi \cos \theta , \\ y = R \sin \varphi \sin \theta , \quad (\varphi , \theta) \in D _ {\varphi \theta}. \\ z = R \cos \varphi , \end{array} \right.
$$

这里 $D_{\varphi \theta} = \{(\varphi ,\theta)\mid 0\leqslant \varphi \leqslant \alpha ,0\leqslant \theta \leqslant 2\pi \}$

由于 $\sqrt{EG - F^2} = R^2\sin \varphi$ ，于是

$$
\begin{array}{l} A = \iint_ {D _ {\varphi \theta}} \sqrt {E G - F ^ {2}} \mathrm{d} \varphi \mathrm{d} \theta = \iint_ {D _ {\varphi \theta}} R ^ {2} \sin \varphi \mathrm{d} \varphi \mathrm{d} \theta \\ = R ^ {2} \int_ {0} ^ {2 \pi} \mathrm{d} \theta \int_ {0} ^ {\alpha} \sin \varphi \mathrm{d} \varphi = 2 \pi R ^ {2} (1 - \cos \alpha) = 2 \pi R ^ {2} \frac {h}{R + h}. \\ \end{array}
$$

## 二、质心

先讨论平面薄片的质心.

设在 xOy 平面上有 n 个质点, 它们分别位于点  $(x_{1}, y_{1}), (x_{2}, y_{2}), \cdots, (x_{n}, y_{n})$  处, 质量分别为  $m_{1}, m_{2}, \cdots, m_{n}$ . 由力学知道, 该质点系的质心的坐标为

$$
\overline {{x}} = \frac {M _ {y}}{M} = \frac {\sum_ {i = 1} ^ {n} m _ {i} x _ {i}}{\sum_ {i = 1} ^ {n} m _ {i}}, \quad \overline {{y}} = \frac {M _ {x}}{M} = \frac {\sum_ {i = 1} ^ {n} m _ {i} y _ {i}}{\sum_ {i = 1} ^ {n} m _ {i}},
$$

165

---

第十章 重积分

其中 $M = \sum_{i=1}^{n} m_i$ 为该质点系的总质量，

$$
M _ {y} = \sum_ {i = 1} ^ {n} m _ {i} x _ {i}, \quad M _ {x} = \sum_ {i = 1} ^ {n} m _ {i} y _ {i},
$$

分别为该质点系对 y 轴和 x 轴的静矩.

设有一平面薄片, 占有 $xOy$ 面上的闭区域 $D$, 在点 $(x,y)$ 处的面密度为 $\mu(x,y)$, 假定 $\mu(x,y)$ 在 $D$ 上连续. 现在要找该薄片的质心的坐标.

在闭区域 $D$ 上任取一直径很小的闭区域 $\mathrm{d}\sigma$ （这小闭区域的面积也记作 $\mathrm{d}\sigma$ ），$(x,y)$ 是这小闭区域上的一个点.因为 $\mathrm{d}\sigma$ 的直径很小，且 $\mu (x,y)$ 在 $D$ 上连续，所以薄片中相应于 $\mathrm{d}\sigma$ 的部分的质量近似等于 $\mu (x,y)\mathrm{d}\sigma$ ，这部分质量可近似看做集中在点$(x,y)$ 上，于是可写出静矩元素 $\mathrm{d}M_y$ 及 $\mathrm{d}M_x$ :

$$
\mathrm{d} M _ {y} = x \mu (x, y) \mathrm{d} \sigma , \quad \mathrm{d} M _ {x} = y \mu (x, y) \mathrm{d} \sigma .
$$

以这些元素为被积表达式,在闭区域 D 上积分,便得

$$
M _ {y} = \iint_ {D} x \mu (x, y) \mathrm{d} \sigma , \quad M _ {x} = \iint_ {D} y \mu (x, y) \mathrm{d} \sigma .
$$

又由第一节知道,薄片的质量为

$$
M = \iint_ {D} \mu (x, y) \mathrm{d} \sigma .
$$

所以,薄片的质心的坐标为

$$
\overline {{x}} = \frac {M _ {y}}{M} = \frac {\iint_ {D} x \mu (x , y) \mathrm{d} \sigma}{\iint_ {D} \mu (x , y) \mathrm{d} \sigma}, \quad \overline {{y}} = \frac {M _ {x}}{M} = \frac {\iint_ {D} y \mu (x , y) \mathrm{d} \sigma}{\iint_ {D} \mu (x , y) \mathrm{d} \sigma}.
$$

如果薄片是均匀的,即面密度为常量,那么上式中可把 $\mu$ 提到积分记号外面,并从分子、分母中约去,这样便得均匀薄片的质心的坐标为

$$
\overline {{x}} = \frac {1}{A} \iint_ {D} x \mathrm{d} \sigma , \quad \overline {{y}} = \frac {1}{A} \iint_ {D} y \mathrm{d} \sigma , \tag {4-1}
$$

其中 $A = \iint_{D} \mathrm{d}\sigma$ 为闭区域 $D$ 的面积. 这时薄片的质心完全由闭区域 $D$ 的形状所决定. 我们把均匀平面薄片的质心叫做这平面薄片所占的平面图形的形心. 因此, 平面图形 $D$ 的形心的坐标, 就可用公式(4-1)计算.

例3 求位于两圆 $\rho = 2\sin \theta$ 和 $\rho = 4\sin \theta$ 之间的均匀薄片的质心(图10-41).

解 因为闭区域 D 关于 y 轴对称, 所以质心  $C(\bar{x}, \bar{y})$  必位于 y 轴上, 于是  $\bar{x} = 0$ . 再按公式

$$
\bar {y} = \frac {1}{A} \iint_ {D} y \mathrm{d} \sigma
$$

166

---

第四节 重积分的应用

计算 $\overline{y}$. 由于闭区域 $D$ 位于半径为 1 与半径为 2 的两圆之间, 所以它的面积等于这两个圆的面积之差, 即 $A = 3\pi$. 再利用极坐标计算积分

$$
\begin{array}{l} \iint_ {D} y \mathrm{d} \sigma = \iint_ {D} \rho^ {2} \sin \theta \mathrm{d} \rho \mathrm{d} \theta = \int_ {0} ^ {\pi} \sin \theta \mathrm{d} \theta \int_ {2 \sin \theta} ^ {4 \sin \theta} \rho^ {2} \mathrm{d} \rho \\ = \frac {5 6}{3} \int_ {0} ^ {\pi} \sin^ {4} \theta \mathrm{d} \theta = 7 \pi . \\ \end{array}
$$

因此  $\bar{y}=\frac{7\pi}{3\pi}=\frac{7}{3}$ ，所求质心是  $C\left(0,\frac{7}{3}\right)$ .

![](../../raw/pages_0161-0192/images/page_173_image_4.jpg)

<details>
<summary>text_image</summary>

y
4
D
C
2
O
x
</details>

图10-41

类似地,占有空间有界闭区域  $\Omega$ 、在点  $(x,y,z)$  处的密度为  $\rho(x,y,z)$  （假定  $\rho(x,y,z)$  在  $\Omega$  上连续）的物体的质心坐标是

$$
\bar {x} = \frac {1}{M} \iiint_ {\Omega} x \rho (x, y, z) \mathrm{d} V, \quad \bar {y} = \frac {1}{M} \iiint_ {\Omega} y \rho (x, y, z) \mathrm{d} V, \quad \bar {z} = \frac {1}{M} \iiint_ {\Omega} z \rho (x, y, z) \mathrm{d} V,
$$

其中 $M = \iiint_{\Omega} \rho(x, y, z) \, \mathrm{d}V.$

\* 例 4 求均匀半球体的质心.

解 取半球体的对称轴为 z 轴, 原点取在球心上, 又设球半径为 a, 则半球体所占空间闭区域

$$
\Omega = \{(x, y, z) | x ^ {2} + y ^ {2} + z ^ {2} \leqslant a ^ {2}, z \geqslant 0 \}.
$$

显然,质心在z轴上,故 $\bar{x}=\bar{y}=0$ .

$$
\bar {z} = \frac {1}{M} \iiint_ {\Omega} z \rho \mathrm{d} V = \frac {1}{V} \iiint_ {\Omega} z \mathrm{d} V,
$$

其中  $V=\frac{2}{3}\pi a^{3}$  为半球体的体积.

$$
\begin{array}{l} \iiint_ {\Omega} z \mathrm{d} V = \iiint_ {\Omega} r \cos \varphi \cdot r ^ {2} \sin \varphi \mathrm{d} r \mathrm{d} \varphi \mathrm{d} \theta = \int_ {0} ^ {2 \pi} \mathrm{d} \theta \int_ {0} ^ {\frac {\pi}{2}} \cos \varphi \sin \varphi \mathrm{d} \varphi \int_ {0} ^ {a} r ^ {3} \mathrm{d} r \\ = 2 \pi \cdot \left[ \frac {\sin^ {2} \varphi}{2} \right] _ {0} ^ {\frac {\pi}{2}} \cdot \frac {a ^ {4}}{4} = \frac {\pi a ^ {4}}{4}. \\ \end{array}
$$

因此, $\bar{z}=\frac{3}{8}a$ ,质心为 $\left(0,0,\frac{3}{8}a\right)$ .

## 三、转动惯量

先讨论平面薄片的转动惯量.

设在 $xOy$ 平面上有 $n$ 个质点, 它们分别位于点

$$
(x _ {1}, y _ {1}), \quad (x _ {2}, y _ {2}), \quad \dots , \quad (x _ {n}, y _ {n})
$$

167

---

第十章 重积分

处,质量分别为  $m_{1}, m_{2}, \cdots, m_{n}$ . 由力学知道,该质点系对于 x 轴以及对于 y 轴的转动惯量依次为

$$
I _ {x} = \sum_ {i = 1} ^ {n} y _ {i} ^ {2} m _ {i}, \quad I _ {y} = \sum_ {i = 1} ^ {n} x _ {i} ^ {2} m _ {i}.
$$

设有一薄片, 占有 $xOy$ 面上的闭区域 $D$, 在点 $(x, y)$ 处的面密度为 $\mu(x, y)$, 假定 $\mu(x, y)$ 在 $D$ 上连续. 现在要求该薄片对于 $x$ 轴的转动惯量 $I_x$ 以及对于 $y$ 轴的转动惯量 $I_y$.

应用元素法. 在闭区域 $D$ 上任取一直径很小的闭区域 $\mathrm{d}\sigma$ （这小闭区域的面积也记作 $\mathrm{d}\sigma$, $(x,y)$ 是该小闭区域上的一个点. 因为 $\mathrm{d}\sigma$ 的直径很小, 且 $\mu(x,y)$ 在 $D$ 上连续, 所以薄片中相应于 $\mathrm{d}\sigma$ 部分的质量近似等于 $\mu(x,y)\mathrm{d}\sigma$, 这部分质量可近似看做集中在点 $(x,y)$ 上, 于是可写出薄片对于 $x$ 轴以及对于 $y$ 轴的转动惯量元素

$$
\mathrm{d} I _ {x} = y ^ {2} \mu (x, y) \mathrm{d} \sigma , \quad \mathrm{d} I _ {y} = x ^ {2} \mu (x, y) \mathrm{d} \sigma .
$$

以这些元素为被积表达式,在闭区域 D 上积分,便得

$$
I _ {x} = \iint_ {D} y ^ {2} \mu (x, y) \mathrm{d} \sigma , \quad I _ {y} = \iint_ {D} x ^ {2} \mu (x, y) \mathrm{d} \sigma .
$$

例 5 求半径为 a 的均匀半圆薄片（面密度为常量  $\mu$ ）对于其直径边的转动惯量.

解 取坐标系如图 10-42 所示, 则薄片所占闭区域

$$
D = \{(x, y) \mid x ^ {2} + y ^ {2} \leqslant a ^ {2}, y \geqslant 0 \},
$$

![](../../raw/pages_0161-0192/images/page_174_image_11.jpg)

<details>
<summary>text_image</summary>

-a
O
a
x
y
</details>

图10-42

而所求转动惯量即半圆薄片对于 $x$ 轴的转动惯量 $I_{x}$.

$$
\begin{array}{l} I _ {x} = \iint_ {D} \mu y ^ {2} \mathrm{d} \sigma = \mu \iint_ {D} \rho^ {3} \sin^ {2} \theta \mathrm{d} \rho \mathrm{d} \theta = \mu \int_ {0} ^ {\pi} \mathrm{d} \theta \int_ {0} ^ {a} \rho^ {3} \sin^ {2} \theta \mathrm{d} \rho \\ = \mu \cdot \frac {a ^ {4}}{4} \int_ {0} ^ {\pi} \sin^ {2} \theta \mathrm{d} \theta = \frac {1}{4} \mu a ^ {4} \cdot \frac {\pi}{2} = \frac {1}{4} M a ^ {2}, \\ \end{array}
$$

其中 $M = \frac{1}{2}\pi a^2\mu$ 为半圆薄片的质量.

类似地,占有空间有界闭区域  $\Omega$ 、在点  $(x,y,z)$  处的密度为  $\rho(x,y,z)$  （假定  $\rho(x,y,z)$  在  $\Omega$  上连续）的物体对于 x 轴、y 轴和 z 轴的转动惯量为

$$
\begin{array}{l} I _ {x} = \iiint_ {\Omega} (y ^ {2} + z ^ {2}) \rho (x, y, z) \mathrm{d} V, \\ I _ {y} = \iiint_ {\Omega} (z ^ {2} + x ^ {2}) \rho (x, y, z) \mathrm{d} V, \\ I _ {z} = \iiint_ {\Omega} (x ^ {2} + y ^ {2}) \rho (x, y, z) \mathrm{d} V. \\ \end{array}
$$

\* 例6 求密度为 $\rho$ 的均匀球对于过球心的一条轴 $l$ 的转动惯量.

168

---

第四节 重积分的应用

解 取球心为坐标原点,z 轴与轴 l 重合,又设球的半径为 a,则球所占空间闭区域

$$
\Omega = \{(x, y, z) \mid x ^ {2} + y ^ {2} + z ^ {2} \leqslant a ^ {2} \}.
$$

所求转动惯量即球对于 $z$ 轴的转动惯量为

$$
\begin{array}{l} I _ {z} = \iiint_ {\Omega} (x ^ {2} + y ^ {2}) \rho \mathrm{d} V \\ = \rho \iiint_ {\Omega} \left(r ^ {2} \sin^ {2} \varphi \cos^ {2} \theta + r ^ {2} \sin^ {2} \varphi \sin^ {2} \theta\right) r ^ {2} \sin \varphi \mathrm{d} r \mathrm{d} \varphi \mathrm{d} \theta \\ = \rho \iiint_ {\Omega} r ^ {4} \sin^ {3} \varphi \mathrm{d} r \mathrm{d} \varphi \mathrm{d} \theta = \rho \int_ {0} ^ {2 \pi} \mathrm{d} \theta \int_ {0} ^ {\pi} \sin^ {3} \varphi \mathrm{d} \varphi \int_ {0} ^ {a} r ^ {4} \mathrm{d} r \\ = \rho \cdot 2 \pi \cdot \frac {a ^ {5}}{5} \int_ {0} ^ {\pi} \sin^ {3} \varphi \mathrm{d} \varphi = \frac {2}{5} \pi a ^ {5} \rho \cdot \frac {4}{3} = \frac {2}{5} a ^ {2} M, \\ \end{array}
$$

其中  $M=\frac{4}{3}\pi a^{3}\rho$  为球的质量.

## 四、引力

下面讨论空间一物体对于物体外一点 $P_0(x_0, y_0, z_0)$ 处单位质量的质点的引力问题.

设物体占有空间有界闭区域 $\Omega$，它在点 $(x, y, z)$ 处的密度为 $\rho(x, y, z)$，并假定 $\rho(x, y, z)$ 在 $\Omega$ 上连续。在物体内任取一直径很小的闭区域 $\mathrm{d}V$（这闭区域的体积也记作 $\mathrm{d}V$），$(x, y, z)$ 为这一小块中的一点。把这一小块物体的质量 $\rho \mathrm{d}V$ 近似地看做集中在点 $(x, y, z)$ 处。于是按两质点间的引力公式，可得这一小块物体对位于 $P_0(x_0, y_0, z_0)$ 处的单位质量的质点的引力近似地为

$$
\begin{array}{l} \mathrm{d} \boldsymbol {F} = (\mathrm{d} F _ {x}, \mathrm{d} F _ {y}, \mathrm{d} F _ {z}) \\ = \left(G \frac {\rho (x , y , z) (x - x _ {0})}{r ^ {3}} \mathrm{d} V, G \frac {\rho (x , y , z) (y - y _ {0})}{r ^ {3}} \mathrm{d} V, G \frac {\rho (x , y , z) (z - z _ {0})}{r ^ {3}} \mathrm{d} V\right), \\ \end{array}
$$

其中 $\mathrm{d}F_{x},\mathrm{d}F_{y},\mathrm{d}F_{z}$ 为引力元素 $\mathrm{d}F$ 在三个坐标轴上的分量， $r = \sqrt{(x - x_0)^2 + (y - y_0)^2 + (z - z_0)^2},G$ 为引力常量.将 $\mathrm{d}F_x,\mathrm{d}F_y,\mathrm{d}F_z$ 在 $\Omega$ 上分别积分，即得

$$
\begin{array}{l} \mathbb {F} = (F _ {x}, F _ {y}, F _ {z}) \\ = \left(\iiint_ {\Omega} \frac {G \rho (x , y , z) (x - x _ {0})}{r ^ {3}} \mathrm{d} V, \iiint_ {\Omega} \frac {G \rho (x , y , z) (y - y _ {0})}{r ^ {3}} \mathrm{d} V, \iiint_ {\Omega} \frac {G \rho (x , y , z) (z - z _ {0})}{r ^ {3}} \mathrm{d} V\right). \\ \end{array}
$$

如果考虑平面薄片对薄片外一点 $P_{0}(x_{0},y_{0},z_{0})$ 处单位质量的质点的引力，设平面薄片占有 $xOy$ 平面上的有界闭区域 $D$ ，其面密度为 $\mu (x,y)$ ，那么只要将上式中的密度$\rho (x,y,z)$ 换成面密度 $\mu (x,y)$ ，将 $\Omega$ 上的三重积分换成 $D$ 上的二重积分，就可得到相

169

---

第十章 重积分

应的计算公式.

例7 设半径为 $R$ 的质量均匀的球占有空间闭区域 $\Omega = \{(x, y, z) | x^2 + y^2 + z^2 \leqslant R^2\}$. 求它对位于 $M_0(0, 0, a) (a > R)$ 处的单位质量的质点的引力.

解 设球的密度为  $\rho_{0}$ ，由球的对称性及质量分布的均匀性知  $F_{x}=F_{y}=0$ ，所求引力沿 z 轴的分量为

$$
\begin{array}{l} F _ {z} = \iiint_ {\Omega} G \rho_ {0} \frac {z - a}{\left[ x ^ {2} + y ^ {2} + (z - a) ^ {2} \right] ^ {\frac {3}{2}}} \mathrm{d} V \\ = G \rho_ {0} \int_ {- R} ^ {R} (z - a) \mathrm{d} z \iint_ {x ^ {2} + y ^ {2} \leqslant R ^ {2} - z ^ {2}} \frac {\mathrm{d} x \mathrm{d} y}{\left[ x ^ {2} + y ^ {2} + (z - a) ^ {2} \right] ^ {\frac {3}{2}}} \\ = G \rho_ {0} \int_ {- R} ^ {R} (z - a) \mathrm{d} z \int_ {0} ^ {2 \pi} \mathrm{d} \theta \int_ {0} ^ {\sqrt {R ^ {2} - z ^ {2}}} \frac {\rho \mathrm{d} \rho}{\left[ \rho^ {2} + (z - a) ^ {2} \right] ^ {\frac {3}{2}}} \\ = 2 \pi G \rho_ {0} \int_ {- R} ^ {R} (z - a) \left(\frac {1}{a - z} - \frac {1}{\sqrt {R ^ {2} - 2 a z + a ^ {2}}}\right) \mathrm{d} z \\ = 2 \pi G \rho_ {0} \left[ - 2 R + \frac {1}{a} \int_ {- R} ^ {R} (z - a) \mathrm{d} \sqrt {R ^ {2} - 2 a z + a ^ {2}} \right] \\ = 2 \pi G \rho_ {0} \left(- 2 R + 2 R - \frac {2 R ^ {3}}{3 a ^ {2}}\right) = - G \cdot \frac {4 \pi R ^ {3}}{3} \rho_ {0} \cdot \frac {1}{a ^ {2}} = - G \frac {M}{a ^ {2}}, \\ \end{array}
$$

其中 $M = \frac{4\pi R^3}{3}\rho_0$ 为球的质量.上述结果表明:质量均匀的球对球外一质点的引力如同球的质量集中于球心时两质点间的引力.

## 习题10-4

1. 求球面 $x^{2} + y^{2} + z^{2} = a^{2}$ 含在圆柱面 $x^{2} + y^{2} = ax$ 内部的那部分面积.
2. 求锥面 $z = \sqrt{x^2 + y^2}$ 被柱面 $z^2 = 2x$ 所割下部分的曲面面积.
3. 求底圆半径相等的两个直交圆柱面 $x^{2} + y^{2} = R^{2}$ 及 $x^{2} + z^{2} = R^{2}$ 所围立体的表面积.
4. 设 $\Sigma$ 为一确定球面 $x^{2} + y^{2} + z^{2} = R^{2}$ （$R$ 为正的常数），另有一球心在 $\Sigma$ 上、半径为 $r$ 的球面 $\Sigma_{1}$，问 $r$ 取何值时，球面 $\Sigma_{1}$ 在球面 $\Sigma$ 内部的那部分面积最大？

5. 设薄片所占的闭区域 $D$ 如下, 求均匀薄片的质心:

(1) D 由  $y=\sqrt{2px}$ ,  $x=x_{0}$ , y=0 所围成;
(2) D 是半椭圆形闭区域  $\left\{(x,y)\left|\frac{x^{2}}{a^{2}}+\frac{y^{2}}{b^{2}}\leqslant1,y\geqslant0\right.\right\}$ ;
(3) $D$ 是界于两个圆 $\rho = a\cos \theta, \rho = b\cos \theta (0 < a < b)$ 之间的闭区域.

170

---

\* 第五节 含参变量的积分

6. 设平面薄片所占的闭区域 $D$ 由抛物线 $y = x^2$ 及直线 $y = x$ 所围成, 它在点 $(x, y)$ 处的面密度 $\mu(x, y) = x^2y$, 求该薄片的质心.

7. 设有一等腰直角三角形薄片, 腰长为 $a$, 各点处的面密度等于该点到直角顶点的距离的平方, 求这薄片的质心.

8. 利用三重积分计算下列由曲面所围立体的质心(设密度  $\rho=1$ ):

(1)  $z^{2}=x^{2}+y^{2},z=1;$

$^{*}$ (2)  $z=\sqrt{A^{2}-x^{2}-y^{2}}$ ,  $z=\sqrt{a^{2}-x^{2}-y^{2}}$  (A>a>0), z=0;

(3) $z=x^{2}+y^{2},x+y=a,x=0,y=0,z=0.$

\*9. 设球占有闭区域 $\Omega = \{(x, y, z) \mid x^2 + y^2 + z^2 \leqslant 2Rz\}$, 它在内部各点处的密度的大小等于该点到坐标原点的距离的平方. 试求这球的质心.

10. 设均匀薄片(面密度为常数 1)所占闭区域 D 如下, 求指定的转动惯量:

(1) $D=\left\{(x,y)\left|\frac{x^{2}}{a^{2}}+\frac{y^{2}}{b^{2}}\leqslant1\right.\right\}$ , 求  $I_{y}$ ;

(2) D 由抛物线  $y^{2}=\frac{9}{2}x$  与直线 x=2 所围成, 求  $I_{x}$  和  $I_{y}$ ;

(3) D 为矩形闭区域  $\{(x,y)\mid0\leqslant x\leqslant a,0\leqslant y\leqslant b\}$ ，求  $I_{x}$  和  $I_{y}$ .

11. 已知均匀矩形板(面密度为常量 $\mu$ )的长和宽分别为 b 和 h, 计算此矩形板对于通过其形心且分别与一边平行的两轴的转动惯量.

12. 一均匀物体(密度 $\rho$ 为常量)占有的闭区域 $\Omega$ 由曲面 $z=x^{2}+y^{2}$ 和平面z=0, $|x|=a$ , $|y|=a$ 所围成,

(1) 求物体的体积;

(2) 求物体的质心;

(3) 求物体关于 z 轴的转动惯量.

13. 求半径为 $a$ 、高为 $h$ 的均匀圆柱体对于过中心而平行于母线的轴的转动惯量（设密度 $\rho = 1$）.

14. 设面密度为常量 $\mu$ 的质量均匀的半圆环形薄片占有闭区域 $D = \{(x, y, 0) \mid R_1 \leqslant \sqrt{x^2 + y^2} \leqslant R_2, x \geqslant 0\}$, 求它对位于 $z$ 轴上点 $M_0(0, 0, a) (a > 0)$ 处单位质量的质点的引力 $\pmb{F}$.

15. 设均匀柱体密度为 $\rho_0$，占有闭区域 $\Omega = \{(x, y, z) | x^2 + y^2 \leqslant R^2, 0 \leqslant z \leqslant h\}$，求它对位于点 $M_0(0, 0, a) (a > h)$ 处的单位质量的质点的引力。

## \* 第五节 含参变量的积分

设 $f(x,y)$ 是矩形（闭区域）$R = [a,b]\times [c,d]$ ①上的连续函数.在 $[a,b]$ 上任意取定 $x$ 的一个值，于是 $f(x,y)$ 是变量 $y$ 在 $[c,d]$ 上的一个一元连续函数，从而积分

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① $[a,b]\times [c,d] = \{(x,y)\mid x\in [a,b],y\in [c,d]\}$ ，称为 $[a,b]$ 和 $[c,d]$ 的直积.</span></small>

171

---

第十章 重积分

$$
\int_ {c} ^ {d} f (x, y) \mathrm{d} y
$$

存在, 这个积分的值依赖于取定的 $x$ 值. 当 $x$ 的值改变时, 一般说来这个积分的值也跟着改变. 这个积分确定一个定义在 $[a, b]$ 上的 $x$ 的函数, 把它记作 $\varphi(x)$, 即

$$
\varphi (x) = \int_ {c} ^ {d} f (x, y) \mathrm{d} y \quad (a \leqslant x \leqslant b). \tag {5-1}
$$

这里变量 $x$ 在积分过程中是一个常量, 通常称它为参变量, 因此 (5-1) 式右端是一个含参变量 $x$ 的积分, 这积分确定 $x$ 的一个函数 $\varphi(x)$, 下面讨论关于 $\varphi(x)$ 的一些性质.

定理1 如果函数 $f(x,y)$ 在矩形 $R = [a,b]\times [c,d]$ 上连续，那么由积分(5-1)确定的函数 $\varphi (x)$ 在 $[a,b]$ 上也连续.

证 设 $x$ 和 $x + \Delta x$ 是 $[a, b]$ 上的两点，则

$$
\varphi (x + \Delta x) - \varphi (x) = \int_ {c} ^ {d} [ f (x + \Delta x, y) - f (x, y) ] \mathrm{d} y. \tag {5-2}
$$

由于 $f(x,y)$ 在闭区域 $R$ 上连续，从而一致连续.因此对于任意取定的 $\varepsilon >0$ ，存在 $\delta >0$ 使得对于 $R$ 内的任意两点 $(x_{1},y_{1})$ 及 $(x_{2},y_{2})$ ，只要它们之间的距离小于 $\delta$ ，即

$$
\sqrt {(x _ {2} - x _ {1}) ^ {2} + (y _ {2} - y _ {1}) ^ {2}} <   \delta ,
$$

就有

$$
\left| f (x _ {2}, y _ {2}) - f (x _ {1}, y _ {1}) \right| <   \varepsilon .
$$

因为点 $(x + \Delta x, y)$ 与 $(x, y)$ 的距离等于 $|\Delta x|$，所以当 $|\Delta x| < \delta$ 时，就有

$$
\left| f (x + \Delta x, y) - f (x, y) \right| <   \varepsilon ,
$$

于是由(5-2)式有

$$
\mid \varphi (x + \Delta x) - \varphi (x) \mid \leqslant \int_ {c} ^ {d} \mid f (x + \Delta x, y) - f (x, y) \mid \mathrm{d} y <   \varepsilon (d - c).
$$

所以 $\varphi (x)$ 在 $[a,b]$ 上连续.

既然函数 $\varphi(x)$ 在 $[a, b]$ 上连续, 那么它在 $[a, b]$ 上的积分存在, 这个积分可以写为

$$
\int_ {a} ^ {b} \varphi (x)   \mathrm{d} x = \int_ {a} ^ {b} \left[ \int_ {c} ^ {d} f (x, y)   \mathrm{d} y \right] \mathrm{d} x = \int_ {a} ^ {b} \mathrm{d} x \int_ {c} ^ {d} f (x, y)   \mathrm{d} y.
$$

右端积分是函数 $f(x,y)$ 先对 $y$ 后对 $x$ 的二次积分.当 $f(x,y)$ 在矩形 $R$ 上连续时，$f(x,y)$ 在 $R$ 上的二重积分 $\iint_{R} f(x,y) \, \mathrm{d}x \, \mathrm{d}y$ 是存在的，这个二重积分化为二次积分来计算时，如果先对 $y$ 后对 $x$ 积分，就是上面的这个二次积分.但二重积分 $\iint_{R} f(x,y) \, \mathrm{d}x \, \mathrm{d}y$ 也可化为先对 $x$ 后对 $y$ 的二次积分 $\int_{c}^{d} \left[ \int_{a}^{b} f(x,y) \, \mathrm{d}x \right] \, \mathrm{d}y$ ，因此有下面的定理2.

172

---

\* 第五节 含参变量的积分

定理2 如果函数 $f(x,y)$ 在矩形 $R = [a,b]\times [c,d]$ 上连续，那么

$$
\int_ {a} ^ {b} \left[ \int_ {c} ^ {d} f (x, y) \mathrm{d} y \right] \mathrm{d} x = \int_ {c} ^ {d} \left[ \int_ {a} ^ {b} f (x, y) \mathrm{d} x \right] \mathrm{d} y. \tag {5-3}
$$

公式(5-3)也可写成

$$
\int_ {a} ^ {b} \mathrm{d} x \int_ {c} ^ {d} f (x, y) \mathrm{d} y = \int_ {c} ^ {d} \mathrm{d} y \int_ {a} ^ {b} f (x, y) \mathrm{d} x. \tag {$5-3^{\prime$}}
$$

下面考虑由积分(5-1)确定的函数  $\varphi(x)$  的微分问题.

定理3 如果函数 $f(x,y)$ 及其偏导数 $f_{x}(x,y)$ 都在矩形 $R = [a,b]\times [c,d]$ 上连续，那么由积分(5-1)确定的函数 $\varphi (x)$ 在 $[a,b]$ 上可微分，并且

$$
\varphi^ {\prime} (x) = \frac {\mathrm{d}}{\mathrm{d} x} \int_ {c} ^ {d} f (x, y) \mathrm{d} y = \int_ {c} ^ {d} f _ {x} (x, y) \mathrm{d} y. \tag {5-4}
$$

证 因为 $\varphi'(x) = \lim_{\Delta x \to 0} \frac{\varphi(x + \Delta x) - \varphi(x)}{\Delta x}$, 为了求 $\varphi'(x)$, 先利用公式 (5-2) 作出增量之比

$$
\frac {\varphi (x + \Delta x) - \varphi (x)}{\Delta x} = \int_ {c} ^ {d} \frac {f (x + \Delta x , y) - f (x , y)}{\Delta x} \mathrm{d} y. \tag {5-5}
$$

由拉格朗日中值定理以及 $f_{x}(x,y)$ 的一致连续性,可得

$$
\frac {f (x + \Delta x , y) - f (x , y)}{\Delta x} = f _ {x} (x + \theta \Delta x, y) = f _ {x} (x, y) + \eta (x, y, \Delta x), \tag {5-6}
$$

其中 $0 < \theta < 1, |\eta|$ 可小于任意给定的正数 $\varepsilon$，只要 $|\Delta x|$ 小于某个正数 $\delta$. 因此

$$
\left| \int_ {c} ^ {d} \eta (x, y, \Delta x) \mathrm{d} y \right| <   \int_ {c} ^ {d} \varepsilon \mathrm{d} y = \varepsilon (d - c) \quad (\mid \Delta x \mid <   \delta),
$$

这就是说

$$
\lim _ {\Delta x \to 0} \int_ {c} ^ {d} \eta (x, y, \Delta x)   \mathrm{d} y = 0.
$$

由(5-5)及(5-6)有

$$
\frac {\varphi (x + \Delta x) - \varphi (x)}{\Delta x} = \int_ {c} ^ {d} f _ {x} (x, y) \mathrm{d} y + \int_ {c} ^ {d} \eta (x, y, \Delta x) \mathrm{d} y,
$$

令  $\Delta x \rightarrow 0$  取上式的极限, 即得公式(5-4).

在积分(5-1)中积分限 c 与 d 都是常数.但在实际应用中还会遇到对于参变量 x 的不同的值,积分限也不同的情形,即以下的积分

$$
\Phi (x) = \int_ {\alpha (x)} ^ {\beta (x)} f (x, y) \mathrm{d} y. \tag {5-7}
$$

下面我们考虑这种更为广泛地依赖于参变量的积分的某些性质.

定理4 如果函数 $f(x,y)$ 在矩形 $R = [a,b]\times [c,d]$ 上连续，函数 $\alpha (x)$ 与 $\beta (x)$ 在区间 $[a,b]$ 上连续，且

$$
c \leqslant \alpha (x) \leqslant d, \quad c \leqslant \beta (x) \leqslant d \quad (a \leqslant x \leqslant b),
$$

173

---

第十章 重积分

那么由积分(5-7)确定的函数  $\Phi(x)$  在  $[a,b]$  上也连续.

证 设 $x$ 和 $x + \Delta x$ 是 $[a, b]$ 上的两点, 则

$$
\Phi (x + \Delta x) - \Phi (x) = \int_ {\alpha (x + \Delta x)} ^ {\beta (x + \Delta x)} f (x + \Delta x, y) \mathrm{d} y - \int_ {\alpha (x)} ^ {\beta (x)} f (x, y) \mathrm{d} y.
$$

因为

$$
\begin{array}{l} \int_ {\alpha (x + \Delta x)} ^ {\beta (x + \Delta x)} f (x + \Delta x, y) \mathrm{d} y \\ = \int_ {\alpha (x + \Delta x)} ^ {\alpha (x)} f (x + \Delta x, y) \mathrm{d} y + \int_ {\alpha (x)} ^ {\beta (x)} f (x + \Delta x, y) \mathrm{d} y + \int_ {\beta (x)} ^ {\beta (x + \Delta x)} f (x + \Delta x, y) \mathrm{d} y, \\ \end{array}
$$

所以

$$
\begin{array}{l} \Phi (x + \Delta x) - \Phi (x) \\ = \int_ {\alpha (x + \Delta x)} ^ {\alpha (x)} f (x + \Delta x, y) \mathrm{d} y + \int_ {\beta (x)} ^ {\beta (x + \Delta x)} f (x + \Delta x, y) \mathrm{d} y + \int_ {\alpha (x)} ^ {\beta (x)} [ f (x + \Delta x, y) - f (x, y) ] \mathrm{d} y. \tag {5-8} \\ \end{array}
$$

当 $\Delta x\to 0$ 时，上式右端最后一个积分的积分限不变，根据证明定理1时同样的理由，这个积分趋于零.又

$$
\begin{array}{l} \left| \int_ {\alpha (x + \Delta x)} ^ {\alpha (x)} f (x + \Delta x, y) \mathrm{d} y \right| \leqslant M | \alpha (x + \Delta x) - \alpha (x) |, \\ \left| \int_ {\beta (x)} ^ {\beta (x + \Delta x)} f (x + \Delta x, y) \mathrm{d} y \right| \leqslant M | \beta (x + \Delta x) - \beta (x) |, \\ \end{array}
$$

其中 $M$ 是 $|f(x,y)|$ 在矩形 $R$ 上的最大值. 根据 $\alpha(x)$ 与 $\beta(x)$ 在 $[a,b]$ 上连续的假定，由以上两式可见，当 $\Delta x \to 0$ 时，(5-8)式右端的前两个积分都趋于零. 于是，当 $\Delta x \to 0$ 时，

$$
\Phi (x + \Delta x) - \Phi (x) \rightarrow 0 \quad (a \leqslant x \leqslant b),
$$

所以函数  $\Phi(x)$  在  $[a,b]$  上连续.

关于函数 $\Phi(x)$ 的微分, 有下述定理:

定理5 如果函数 $f(x,y)$ 及其偏导数 $f_{x}(x,y)$ 都在矩形 $R = [a,b]\times [c,d]$ 上连续，函数 $\alpha (x)$ 与 $\beta (x)$ 都在区间 $[a,b]$ 上可微，且

$$
c \leqslant \alpha (x) \leqslant d, \quad c \leqslant \beta (x) \leqslant d \quad (a \leqslant x \leqslant b),
$$

那么由积分(5-7)确定的函数 $\Phi (x)$ 在 $[a,b]$ 上可微，且

$$
\begin{array}{l} \Phi^ {\prime} (x) = \frac {\mathrm{d}}{\mathrm{d} x} \int_ {\alpha (x)} ^ {\beta (x)} f (x, y) \mathrm{d} y \\ = \int_ {\alpha (x)} ^ {\beta (x)} f _ {x} (x, y) \mathrm{d} y + f [ x, \beta (x) ] \beta^ {\prime} (x) - f [ x, \alpha (x) ] \alpha^ {\prime} (x). \tag {5-9} \\ \end{array}
$$

证 由(5-8)式有

$$
\frac {\Phi (x + \Delta x) - \Phi (x)}{\Delta x}
$$

174

---

\* 第五节 含参变量的积分

$$
= \int_ {\alpha (x)} ^ {\beta (x)} \frac {f (x + \Delta x , y) - f (x , y)}{\Delta x} \mathrm{d} y + \frac {1}{\Delta x} \int_ {\beta (x)} ^ {\beta (x + \Delta x)} f (x + \Delta x, y) \mathrm{d} y - \frac {1}{\Delta x} \int_ {\alpha (x)} ^ {\alpha (x + \Delta x)} f (x + \Delta x, y) \mathrm{d} y. \tag {5-10}
$$

当 $\Delta x\to 0$ 时，上式右端的第一个积分的积分限不变，根据证明定理3时同样的理由，有

$$
\int_ {\alpha (x)} ^ {\beta (x)} \frac {f (x + \Delta x , y) - f (x , y)}{\Delta x} \mathrm{d} y \rightarrow \int_ {\alpha (x)} ^ {\beta (x)} f _ {x} (x, y) \mathrm{d} y.
$$

对于(5-10)式右端的第二项,应用积分中值定理得

$$
\frac {1}{\Delta x} \int_ {\beta (x)} ^ {\beta (x + \Delta x)} f (x + \Delta x, y) \mathrm{d} y = \frac {1}{\Delta x} [ \beta (x + \Delta x) - \beta (x) ] f (x + \Delta x, \eta),
$$

其中  $\eta$  在  $\beta(x)$  与  $\beta(x+\Delta x)$  之间. 当  $\Delta x\to0$  时,

$$
\frac {1}{\Delta x} [ \beta (x + \Delta x) - \beta (x) ] \rightarrow \beta^ {\prime} (x), f (x + \Delta x, \eta) \rightarrow f [ x, \beta (x) ].
$$

于是

$$
\frac {1}{\Delta x} \int_ {\beta (x)} ^ {\beta (x + \Delta x)} f (x + \Delta x, y)   \mathrm{d} y \longrightarrow f [ x, \beta (x) ] \beta^ {\prime} (x).
$$

类似地可证, 当  $\Delta x \rightarrow 0$  时,

$$
\frac {1}{\Delta x} \int_ {\alpha (x)} ^ {\alpha (x + \Delta x)} f (x + \Delta x, y) \mathrm{d} y \longrightarrow f [ x, \alpha (x) ] \alpha^ {\prime} (x).
$$

因此，令 $\Delta x\to 0$ ，取(5-10)式的极限便得公式(5-9).

公式(5-9)称为莱布尼茨公式.

例1 设 $\Phi(x) = \int_{x}^{x^2} \frac{\sin(xy)}{y} \, \mathrm{d}y$，求 $\Phi'(x)$.

解 应用莱布尼茨公式, 得

$$
\begin{array}{l} \Phi^ {\prime} (x) = \int_ {x} ^ {x ^ {2}} \cos (x y) \mathrm{d} y + \frac {\sin x ^ {3}}{x ^ {2}} \cdot 2 x - \frac {\sin x ^ {2}}{x} \cdot 1 \\ = \left[ \frac {\sin (x y)}{x} \right] _ {x} ^ {x ^ {2}} + \frac {2 \sin x ^ {3}}{x} - \frac {\sin x ^ {2}}{x} = \frac {3 \sin x ^ {3} - 2 \sin x ^ {2}}{x}. \\ \end{array}
$$

例2 求 $I = \int_0^1\frac{x^b - x^a}{\ln x}\mathrm{d}x$ （ $0 <   a <   b$ ）.

解 因为

$$
\int_ {a} ^ {b} x ^ {y} \mathrm{d} y = \left[ \frac {x ^ {y}}{\ln x} \right] _ {a} ^ {b} = \frac {x ^ {b} - x ^ {a}}{\ln x},
$$

所以

$$
I = \int_ {0} ^ {1} \mathrm{d} x \int_ {a} ^ {b} x ^ {y} \mathrm{d} y.
$$

175

---

第十章 重积分

这里函数 $f(x,y) = x^{y}$ 在矩形 $R = [0,1]\times [a,b]$ 上连续，根据定理2，可交换积分次序，由此有

$$
I = \int_ {a} ^ {b} \mathrm{d} y \int_ {0} ^ {1} x ^ {y} \mathrm{d} x = \int_ {a} ^ {b} \left[ \frac {x ^ {y + 1}}{y + 1} \right] _ {0} ^ {1} \mathrm{d} y = \int_ {a} ^ {b} \frac {1}{y + 1} \mathrm{d} y = \ln \frac {b + 1}{a + 1}.
$$

例3 计算定积分 $I = \int_{0}^{1}\frac{\ln(1 + x)}{1 + x^2}\mathrm{d}x.$

解 考虑含参变量 $\alpha$ 的积分所确定的函数

$$
\varphi (\alpha) = \int_ {0} ^ {1} \frac {\ln (1 + \alpha x)}{1 + x ^ {2}} \mathrm{d} x.
$$

显然，$\varphi(0) = 0, \varphi(1) = I.$ 根据公式(5-4)得

$$
\varphi^ {\prime} (\alpha) = \int_ {0} ^ {1} \frac {x}{(1 + \alpha x) (1 + x ^ {2})} \mathrm{d} x.
$$

把被积函数分解为部分分式,得到

$$
\frac {x}{(1 + \alpha x) (1 + x ^ {2})} = \frac {1}{1 + \alpha^ {2}} \left(\frac {- \alpha}{1 + \alpha x} + \frac {x}{1 + x ^ {2}} + \frac {\alpha}{1 + x ^ {2}}\right).
$$

于是

$$
\begin{array}{l} \varphi^ {\prime} (\alpha) = \frac {1}{1 + \alpha^ {2}} \left(\int_ {0} ^ {1} \frac {- \alpha \mathrm{d} x}{1 + \alpha x} + \int_ {0} ^ {1} \frac {x \mathrm{d} x}{1 + x ^ {2}} + \int_ {0} ^ {1} \frac {\alpha \mathrm{d} x}{1 + x ^ {2}}\right) \\ = \frac {1}{1 + \alpha^ {2}} \left[ - \ln (1 + \alpha) + \frac {1}{2} \ln 2 + \alpha \cdot \frac {\pi}{4} \right], \\ \end{array}
$$

上式在 $[0,1]$ 上对 $\alpha$ 积分,得到

$$
\varphi (1) - \varphi (0) = - \int_ {0} ^ {1} \frac {\ln (1 + \alpha)}{1 + \alpha^ {2}} \mathrm{d} \alpha + \frac {1}{2} \ln 2 \int_ {0} ^ {1} \frac {\mathrm{d} \alpha}{1 + \alpha^ {2}} + \frac {\pi}{4} \int_ {0} ^ {1} \frac {\alpha}{1 + \alpha^ {2}} \mathrm{d} \alpha,
$$

即

$$
I = - I + \frac {\ln 2}{2} \cdot \frac {\pi}{4} + \frac {\pi}{4} \cdot \frac {\ln 2}{2} = - I + \frac {\pi}{4} \ln 2.
$$

从而

$$
I = \frac {\pi}{8} \ln 2.
$$

## \*习题10-5

1. 求下列含参变量的积分所确定的函数的极限:

(1) $\lim_{x\to 0}\int_{x}^{1 + x}\frac{\mathrm{d}y}{1 + x^2 + y^2};$

(2) $\lim_{x\to 0}\int_{-1}^{1}\sqrt{x^2 + y^2}\mathrm{d}y;$

(3) $\lim_{x\to 0}\int_{0}^{2}y^{2}\cos (xy)\mathrm{d}y.$

176

---

总习题十

2. 求下列函数的导数:

(1) $\varphi (x) = \int_{\sin x}^{\cos x}(y^2\sin x - y^3)\mathrm{d}y;$

(2) $\varphi (x) = \int_0^x\frac{\ln(1 + xy)}{y}\mathrm{d}y;$

(3) $\varphi(x) = \int_{x^2}^{x^3}\arctan\frac{y}{x}\mathrm{d}y;$

(4) $\varphi (x) = \int_{x}^{x^2}\mathrm{e}^{-xy^2}\mathrm{d}y.$

3. 设 $F(x) = \int_{0}^{x}(x + y)f(y)\mathrm{d}y$，其中 $f(y)$ 为可微的函数，求 $F''(x)$.

4. 应用对参数的微分法, 计算下列积分:

(1) $I = \int_{0}^{\frac{\pi}{2}}\ln \frac{1 + a\cos x}{1 - a\cos x}\cdot \frac{\mathrm{d}x}{\cos x} (|a| < 1);$

(2) $I = \int_{0}^{\frac{\pi}{2}}\ln (\cos^{2}x + a^{2}\sin^{2}x)\mathrm{d}x$ (a>0).

5. 计算下列积分:

(1) $\int_0^1\frac{\arctan x}{x}\frac{\mathrm{d}x}{\sqrt{1 - x^2}};$

(2) $\int_0^1\sin \left(\ln \frac{1}{x}\right)\frac{x^b - x^a}{\ln x}\mathrm{d}x$ （ $0 <   a <   b$ ）.

## 总习题十

1. 填空:

(1) 积分  $\int_{0}^{2} dx \int_{x}^{2} e^{-y^{2}} dy$  的值是 \_\_\_\_;
(2) 设闭区域  $D = \{(x, y) \mid x^{2} + y^{2} \leqslant R^{2}\}$ ，则  $\iint_{D} \left( \frac{x^{2}}{a^{2}} + \frac{y^{2}}{b^{2}} \right) \, dx \, dy =$ \_\_\_\_ .

2. 以下各题中给出了四个结论,从中选出一个正确的结论:

（1）设有空间闭区域 $\Omega_{1} = \{(x,y,z)\mid x^{2} + y^{2} + z^{2}\leqslant R^{2},z\geqslant 0\} ,\Omega_{2} = \{(x,y,z)\mid x^{2} + y^{2} + z^{2}\leqslant R^{2},$ $x\geqslant 0,y\geqslant 0,z\geqslant 0\}$ ，则有（ ）；

(A) $\iiint_{\Omega_1} x \, \mathrm{d}V = 4 \iiint_{\Omega_2} x \, \mathrm{d}V$

(B) $\iiint_{\Omega_1} y \mathrm{~d} V = 4 \iiint_{\Omega_2} y \mathrm{~d} V$

(C) $\iiint_{\Omega_1} z \, \mathrm{d}V = 4 \iiint_{\Omega_2} z \, \mathrm{d}V$

(D) $\iiint_{\Omega_1} xyz \, \mathrm{d}V = 4 \iiint_{\Omega_2} xyz \, \mathrm{d}V$

（2）设有平面闭区域 $D = \{(x,y)\mid -a\leqslant x\leqslant a,x\leqslant y\leqslant a\}$ ， $D_{1} = \{(x,y)\mid 0\leqslant x\leqslant a,x\leqslant y\leqslant a\}$ ，则$\iint_{D}(xy + \cos x\sin y)\mathrm{d}x\mathrm{d}y = (\quad)$

(A) $2\iint_{D_{1}}\cos x\sin y\mathrm{d}x\mathrm{d}y$

(B) $2\iint_{D_1}xy\mathrm{d}x\mathrm{d}y$

(C) $4\iint_{D_1}(xy + \cos x\sin y)\mathrm{d}x\mathrm{d}y$

(D) 0

(3) 设  $f(x)$  为连续函数,  $F(t)=\int_{1}^{t}\mathrm{d}y\int_{y}^{t}f(x)\mathrm{d}x$ , 则  $F'(2)=(\quad)$ .

(A) $2f(2)$

(B) $f(2)$

(C) $-f(2)$

(D) 0

3. 计算下列二重积分:

(1) $\iint_{D}(1 + x)\sin y\mathrm{d}\sigma$ ，其中 $D$ 是顶点分别为 $(0,0),(1,0),(1,2)$ 和 $(0,1)$ 的梯形闭区域；

177

---

第十章 重积分

(2) $\iint_{D} (x^{2}-y^{2}) \, \mathrm{d}\sigma$, 其中 $D = \{(x,y) \mid 0 \leqslant y \leqslant \sin x, 0 \leqslant x \leqslant \pi\}$;
(3) $\iint_{D} \sqrt{R^2 - x^2 - y^2} \, \mathrm{d}\sigma$，其中 $D$ 是圆周 $x^2 + y^2 = Rx$ 所围成的闭区域；
(4) $\iint_{D}(y^{2} + 3x - 6y + 9)\mathrm{d}\sigma$ ，其中 $D = \{(x,y)\mid x^2 +y^2\leqslant R^2\}$

4. 交换下列二次积分的次序:

(1) $\int_0^4\mathrm{d}y\int_{-\sqrt{4 - y}}^{\frac{1}{2} (y - 4)}f(x,y)\mathrm{d}x;$
(2) $\int_0^1\mathrm{d}y\int_0^{2y}f(x,y)\mathrm{d}x + \int_1^3\mathrm{d}y\int_0^{3 - y}f(x,y)\mathrm{d}x;$
(3) $\int_{0}^{1}\mathrm{d}x\int_{\sqrt{x}}^{1+\sqrt{1-x^{2}}}f(x,y)\mathrm{d}y.$

5. 证明:

$$
\int_ {0} ^ {a} \mathrm{d} y \int_ {0} ^ {y} \mathrm{e} ^ {m (a - x)} f (x) \mathrm{d} x = \int_ {0} ^ {a} (a - x) \mathrm{e} ^ {m (a - x)} f (x) \mathrm{d} x.
$$

6. 把积分 $\iint_{D} f(x, y) \, \mathrm{d}x \, \mathrm{d}y$ 表示为极坐标形式的二次积分, 其中积分区域 $D = \{(x, y) \mid x^2 \leqslant y \leqslant 1, -1 \leqslant x \leqslant 1\}$.

7. 设 $f(x, y)$ 在闭区域 $D = \{(x, y) \mid x^2 + y^2 \leqslant y, x \geqslant 0\}$ 上连续，且

$$
f (x, y) = \sqrt {1 - x ^ {2} - y ^ {2}} - \frac {8}{\pi} \iint_ {D} f (x, y) \mathrm{d} x \mathrm{d} y,
$$

求 $f(x,y)$ .

8. 把积分 $\iiint_{\Omega} f(x, y, z) \, \mathrm{d}x \, \mathrm{d}y \, \mathrm{d}z$ 化为三次积分, 其中积分区域 $\Omega$ 是由曲面 $z = x^2 + y^2, y = x^2$ 及平面 $y = 1, z = 0$ 所围成的闭区域.

9. 计算下列三重积分:

(1) $\iiint_{\Omega} xy^2 \, \mathrm{d}V$，其中 $\Omega$ 是由 $z = 0, x + y - z = 0, x - y - z = 0$ 和 $x = 1$ 所围成的闭区域；
(2) $\iiint_{\Omega} z^2 \, \mathrm{d}x \, \mathrm{d}y \, \mathrm{d}z$，其中 $\Omega$ 是两个球:$x^2 + y^2 + z^2 \leqslant R^2$ 和 $x^2 + y^2 + z^2 \leqslant 2Rz (R > 0)$ 的公共部分；
(3) $\iiint_{\Omega} \frac{z \ln (x^2 + y^2 + z^2 + 1)}{x^2 + y^2 + z^2 + 1} \mathrm{d}V$，其中 $\Omega$ 是由球面 $x^2 + y^2 + z^2 = 1$ 所围成的闭区域；

(4) $\iiint_{\Omega} (y^2 + z^2) \, \mathrm{d}V$, 其中 $\Omega$ 是由 $xOy$ 面上曲线 $y^2 = 2x$ 绕 $x$ 轴旋转而成的曲面与平面 $x = 5$ 所围成的闭区域.

\* 10. 设函数 $f(x)$ 连续且恒大于零，

$$
F (t) = \frac {\iiint_ {\Omega (t)} f (x ^ {2} + y ^ {2} + z ^ {2}) \mathrm{d} V}{\iint_ {D (t)} f (x ^ {2} + y ^ {2}) \mathrm{d} \sigma}, \quad G (t) = \frac {\iint_ {D (t)} f (x ^ {2} + y ^ {2}) \mathrm{d} \sigma}{\int_ {- t} ^ {t} f (x ^ {2}) \mathrm{d} x},
$$

178

---

总习题十

其中 $\Omega(t) = \{(x, y, z) \mid x^2 + y^2 + z^2 \leqslant t^2\}$, $D(t) = \{(x, y) \mid x^2 + y^2 \leqslant t^2\}$.

(1) 讨论  $F(t)$  在区间  $(0, +\infty)$  内的单调性；
(2) 证明当 t>0 时,  $F(t)>\frac{2}{\pi}G(t)$ .

11. 求平面 $\frac{x}{a}+\frac{y}{b}+\frac{z}{c}=1$ 被三坐标面所割出的有限部分的面积.
12. 在均匀的半径为 R 的半圆形薄片的直径上, 要接上一个一边与直径等长的同样材料的均匀矩形薄片, 为了使整个均匀薄片的质心恰好落在圆心上, 问接上去的均匀矩形薄片另一边的长度应是多少?
13. 求由抛物线  $y=x^{2}$  及直线 y=1 所围成的均匀薄片（面密度为常数  $\mu$ ）对于直线 y=-1 的转动惯量.
14. 设在 $xOy$ 面上有一质量为 $M$ 的质量均匀的半圆形薄片，占有平面闭区域 $D = \{(x, y) \mid x^2 + y^2 \leqslant R^2, y \geqslant 0\}$，过圆心 $O$ 垂直于薄片的直线上有一质量为 $m$ 的质点 $P, OP = a$。求半圆形薄片对质点 $P$ 的引力。
15. 求质量分布均匀的半个旋转椭球体 $\Omega = \left\{(x, y, z) \left| \frac{x^2 + y^2}{a^2} + \frac{z^2}{b^2} \leqslant 1, z \geqslant 0 \right.\right\}$ 的质心.
\* 16. 一球形行星的半径为 $R$, 其质量为 $M$, 其密度呈球对称分布, 并向着球心线性增加. 若行星表面的密度为零, 则行星中心的密度是多少?

第十章释疑解难

![](../../raw/pages_0161-0192/images/page_185_image_13.jpg)

第十章例题精讲

![](../../raw/pages_0161-0192/images/page_185_image_15.jpg)

179
