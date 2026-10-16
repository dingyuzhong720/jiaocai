# 第22章 曲面积分

原始 PDF 第 267–292 页。

## 第二十二章曲面积分

## §1 第一型曲面积分

## 一、第一型曲面积分的概念

类似于第一型曲线积分, 当质量分布在某一曲面块 S（设密度函数  $\rho(x,y,z)$  在 S 上连续）时, 曲面块 S 的质量为

$$
\lim _ {\| T \| \to 0} \sum_ {i = 1} ^ {n} \rho (\xi_ {i}, \eta_ {i}, \zeta_ {i}) \Delta S _ {i},
$$

其中  $T=\{S_{1},S_{2},\cdots,S_{n}\}$  为曲面块的分割， $\Delta S_{i}$  表示小曲面块  $S_{i}$  的面积， $(\xi_{i},\eta_{i},\zeta_{i})$  为  $S_{i}$  中任意一点， $\|T\|$  为分割 T 的细度，即为诸  $S_{i}$  中的直径的最大值.

定义1 设 S 是空间中可求面积的曲面,  $f(x,y,z)$  为定义在 S 上的函数. 对曲面 S 作分割 T, 它把 S 分成 n 个小曲面块  $S_{i} (i=1,2,\cdots,n)$ , 以  $\Delta S_{i}$  记小曲面块  $S_{i}$  的面积, 分割 T 的细度  $\|T\|=\max_{1\leqslant i\leqslant n}\{S_{i}$  的直径, 在  $S_{i}$  上任取一点  $(\xi_{i},\eta_{i},\zeta_{i}) (i=1,2,\cdots,n)$ , 若极限

$$
\lim _ {\parallel T \parallel \to 0} \sum_ {i = 1} ^ {n} f (\xi_ {i}, \eta_ {i}, \zeta_ {i}) \Delta S _ {i}
$$

存在,且与分割 T 及  $(\xi_{i},\eta_{i},\zeta_{i})$  ( $i=1,2,\cdots,n$ ) 的取法无关,则称此极限为  $f(x,y,z)$  在 S 上的第一型曲面积分,记作

$$
\iint_ {S} f (x, y, z) \mathrm{d} S. \tag {1}
$$

于是前面讲到的曲面块的质量可由第一型曲面积分(1)求得.

特别地, 当  $f(x,y,z) \equiv 1$  时, 曲面积分  $\iint_{S} dS$  就是曲面块 S 的面积.

第一型曲面积分的性质完全类似于第一型曲线积分,读者可仿照第二十章§1自行写出.

## 二、第一型曲面积分的计算

第一型曲面积分可化为二重积分来计算.

定理 22.1 设有光滑曲面

259

---

第二十二章 曲面积分

$$
S: z = z (x, y), (x, y) \in D,
$$

$f(x,y,z)$ 为 $S$ 上的连续函数，则

$$
\iint_ {S} f (x, y, z) \mathrm{d} S = \iint_ {D} f (x, y, z (x, y)) \sqrt {1 + z _ {x} ^ {2} + z _ {y} ^ {2}} \mathrm{d} x \mathrm{d} y. \tag {2}
$$

定理22.1的证明与第二十章定理20.1的证明相仿,这里不再重复了.

例 1 计算  $\iint_{S}\frac{dS}{z}$ ，其中 S 是球面  $x^{2}+y^{2}+z^{2}=a^{2}$ 
被平面  $z = h (0 < h < a)$  所截的顶部(图 22-1).

解 曲面 $S$ 的方程为

$$
z = \sqrt {a ^ {2} - x ^ {2} - y ^ {2}},
$$

定义域 $D$ 为圆域 $x^{2} + y^{2}\leqslant a^{2} - h^{2}$ .由于

$$
\sqrt {1 + z _ {x} ^ {2} + z _ {y} ^ {2}} = \frac {a}{\sqrt {a ^ {2} - x ^ {2} - y ^ {2}}},
$$

![](../../raw/pages_0257-0288/images/page_267_image_10.jpg)

<details>
<summary>text_image</summary>

z
h
O
a
y
x
</details>

图22-1

所以由公式(2)求得

$$
\begin{array}{l} \iint_ {S} \frac {\mathrm{d} S}{z} = \iint_ {D} \frac {a}{a ^ {2} - x ^ {2} - y ^ {2}} \mathrm{d} x \mathrm{d} y = \int_ {0} ^ {2 \pi} \mathrm{d} \theta \int_ {0} ^ {\sqrt {a ^ {2} - h ^ {2}}} \frac {a}{a ^ {2} - r ^ {2}} r \mathrm{d} r \\ = 2 \pi a \int_ {0} ^ {\sqrt {a ^ {2} - h ^ {2}}} \frac {r}{a ^ {2} - r ^ {2}} \mathrm{d} r = - \pi a \ln (a ^ {2} - r ^ {2}) \Bigg | _ {0} ^ {\sqrt {a ^ {2} - h ^ {2}}} \\ = 2 \pi a \ln \frac {a}{h}. \\ \end{array}
$$

例 2 计算  $\iint_{S}(x^{2}+y^{2}+z^{2})\mathrm{d}S$ ，其中

(1) $S: x^{2} + y^{2} + z^{2} = a^{2}$; (2) $S: x^{2} + y^{2} + z^{2} = 2az$.

解 (1) $\iint_{S} (x^{2} + y^{2} + z^{2}) \, \mathrm{d}S = \iint_{S} a^{2} \, \mathrm{d}S = 4\pi a^{2} \cdot a^{2} = 4\pi a^{4}$.

(2) $\iint_{S} (x^{2} + y^{2} + z^{2}) \, \mathrm{d}S = \iint_{S} 2az \, \mathrm{d}S = \iint_{S_{1}} 2az \, \mathrm{d}S + \iint_{S_{2}} 2az \, \mathrm{d}S,$

其中

$$
\begin{array}{l} S _ {1}: z _ {1} = a + \sqrt {a ^ {2} - (x ^ {2} + y ^ {2})}, (x, y) \in D, \\ S _ {2}: z _ {2} = a - \sqrt {a ^ {2} - (x ^ {2} + y ^ {2})}, (x, y) \in D, \\ D: x ^ {2} + y ^ {2} \leqslant a ^ {2}. \\ \end{array}
$$

由于 $\sqrt{1 + \left(\frac{\partial z_1}{\partial x}\right)^2 + \left(\frac{\partial z_1}{\partial y}\right)^2} = \sqrt{1 + \left(\frac{\partial z_2}{\partial x}\right)^2 + \left(\frac{\partial z_2}{\partial y}\right)^2} = \frac{a}{\sqrt{a^2 - (x^2 + y^2)}}$ ，因此

$$
\iint_ {S _ {1}} 2 a z \mathrm{d} S = \iint_ {D} 2 a (a + \sqrt {a ^ {2} - (x ^ {2} + y ^ {2})} \frac {a}{\sqrt {a ^ {2} - (x ^ {2} + y ^ {2})}} \mathrm{d} x \mathrm{d} y,
$$

260

---

§ 1 第一型曲面积分

$$
\iint_ {S _ {2}} 2 a z \mathrm{d} S = \iint_ {D} 2 a (a - \sqrt {a ^ {2} - (x ^ {2} + y ^ {2})} \frac {a}{\sqrt {a ^ {2} - (x ^ {2} + y ^ {2})}} \mathrm{d} x \mathrm{d} y,
$$

$$
\begin{array}{l} \iint_ {S} \left(x ^ {2} + y ^ {2} + z ^ {2}\right) \mathrm{d} S = 4 \iint_ {D} \frac {a ^ {3}}{\sqrt {a ^ {2} - \left(x ^ {2} + y ^ {2}\right)}} \mathrm{d} x \mathrm{d} y \\ = 4 a ^ {3} \int_ {0} ^ {2 \pi} \mathrm{d} \theta \int_ {0} ^ {a} \frac {r \mathrm{d} r}{\sqrt {a ^ {2} - r ^ {2}}} = 8 a ^ {3} \pi (- \sqrt {a ^ {2} - r ^ {2}}) \Bigg | _ {0} ^ {a} = 8 a ^ {4} \pi , \quad \square \\ \end{array}
$$

对于由参量形式表示的光滑曲面

$$
S: \left\{ \begin{array}{l} x = x (u, v), \\ y = y (u, v), \\ z = z (u, v), \end{array} \right. \quad (u, v) \in D,
$$

则在 $S$ 上第一型曲面积分的计算公式为

$$
\iint_ {S} f (x, y, z) \mathrm{d} S = \iint_ {D} f (x (u, v), y (u, v), z (u, v)) \sqrt {E G - F ^ {2}} \mathrm{d} u \mathrm{d} v, \tag {3}
$$

其中

$$
E = x _ {u} ^ {2} + y _ {u} ^ {2} + z _ {u} ^ {2},
$$

$$
F = x _ {u} x _ {v} + y _ {u} y _ {v} + z _ {u} z _ {v},
$$

$$
G = x _ {v} ^ {2} + y _ {v} ^ {2} + z _ {v} ^ {2}.
$$

这里还要求雅可比行列式 $\frac{\partial(x,y)}{\partial(u,v)},\frac{\partial(y,z)}{\partial(u,v)},\frac{\partial(z,x)}{\partial(u,v)}$ 中至少有一个不等于零.

例3 计算 $\iint_{S} z \, \mathrm{d}S$，其中 $S$ 为螺旋面（图22-2）的一部分

$$
S \colon \left\{ \begin{array}{l l} x = u \cos v, \\ y = u \sin v, & (u, v) \in D, \\ z = v, \end{array} \right.
$$

$$
D: \left\{ \begin{array}{l} 0 \leqslant u \leqslant a, \\ 0 \leqslant v \leqslant 2 \pi . \end{array} \right.
$$

解 由于

$$
E = x _ {u} ^ {2} + y _ {u} ^ {2} + z _ {u} ^ {2}
$$

$$
= \cos^ {2} v + \sin^ {2} v = 1,
$$

$$
F = x _ {u} x _ {v} + y _ {u} y _ {v} + z _ {u} z _ {v}
$$

$$
= - u \sin v \cos v + u \sin v \cos v = 0,
$$

$$
G = x _ {v} ^ {2} + y _ {v} ^ {2} + z _ {v} ^ {2}
$$

$$
= u ^ {2} \sin^ {2} v + u ^ {2} \cos^ {2} v + 1 = 1 + u ^ {2},
$$

因此由公式(3)可以求得

$$
\begin{array}{l} \iint_ {S} z \mathrm{d} S = \iint_ {D} v \sqrt {1 + u ^ {2}} \mathrm{d} u \mathrm{d} v = \int_ {0} ^ {2 \pi} v \mathrm{d} v \int_ {0} ^ {a} \sqrt {1 + u ^ {2}} \mathrm{d} u \\ = 2 \pi^ {2} \left[ \frac {u}{2} \sqrt {1 + u ^ {2}} + \frac {1}{2} \ln (u + \sqrt {1 + u ^ {2}}) \right] \Bigg | _ {0} ^ {a} \\ = \pi^ {2} \left[ a \sqrt {1 + a ^ {2}} + \ln (a + \sqrt {1 + a ^ {2}}) \right]. \\ \end{array}
$$

![](../../raw/pages_0257-0288/images/page_268_image_24.jpg)

<details>
<summary>text_image</summary>

(a,0,0)
2π
O
x
y
z
</details>

图22-2

与重积分相同,利用第一型曲面积分可以求曲面块的质心、转动惯量、引力等,作为练习,请读者自行写出这些公式,这里不赘述了.

261

---

第二十二章 曲面积分

## 习题 22.1

1. 计算下列第一型曲面积分:

(1) $\iint_{S}(x + y + z)\mathrm{d}S$ ，其中 $S$ 为上半球面 $x^{2} + y^{2} + z^{2} = a^{2},z\geqslant 0;$
(2) $\iint_{S}(x^{2} + y^{2})\mathrm{d}S$ ，其中 $S$ 为立体 $\sqrt{x^2 + y^2}\leqslant z\leqslant 1$ 的边界曲面；
(3) $\iint_{S} \frac{\mathrm{d}S}{x^2 + y^2}$, 其中 $S$ 为柱面 $x^2 + y^2 = R^2$ 被平面 $z = 0, z = H$ 所截取的部分;
(4) $\iint_{S} xyz \, \mathrm{d}S$, 其中 $S$ 为平面 $x + y + z = 1$ 在第一卦限中的部分.

2. 求均匀曲面 $x^{2} + y^{2} + z^{2} = a^{2}, x \geqslant 0, y \geqslant 0, z \geqslant 0$ 的质心.

3. 求密度为  $\rho$  的均匀球面  $x^{2} + y^{2} + z^{2} = a^{2} \quad (z \geqslant 0)$  对于 z 轴的转动惯量.

4. 计算 $\iint_{S} z^2 \, \mathrm{d}S$，其中 $S$ 为圆锥表面的一部分

$$
S: \left\{ \begin{array}{l} x = r \cos \varphi \sin \theta , \\ y = r \sin \varphi \sin \theta , \\ z = r \cos \theta , \end{array} \right. \quad D: \left\{ \begin{array}{l} 0 \leqslant r \leqslant a, \\ 0 \leqslant \varphi \leqslant 2 \pi , \end{array} \right.
$$

这里 $\theta$ 为常数 $\left(0 < \theta < \frac{\pi}{2}\right)$.

## § 2 第二型曲面积分

## 一、曲面的侧

为了给曲面确定方向,先要阐明曲面的侧的概念.

设连通曲面 $S$ 上到处都有连续变动的切平面（或法线），$M$ 为曲面 $S$ 上的一点，曲面在 $M$ 处的法线有两个方向:当取定其中一个指向为正方向时，则另一个指向就是负方向。设 $M_0$ 为 $S$ 上任一点，$L$ 为 $S$ 上任一经过点 $M_0$，且不超出 $S$ 边界的闭曲线。又设 $M$ 为动点，它在 $M_0$ 处与 $M_0$ 有相同的法线方向，且有如下特性:当 $M$ 从 $M_0$ 出发沿 $L$ 连续移动，这时作为曲面上的点 $M$，它的法线方向也连续地变动。最后当 $M$ 沿 $L$ 回到 $M_0$ 时，若这时 $M$ 的法线方向仍与 $M_0$ 的法线方向相一致，则说这曲面 $S$ 是双侧曲面①；若与 $M_0$ 的法线方向相反，则说 $S$ 是单侧曲面。

我们通常碰到的曲面大多是双侧曲面. 单侧曲面的一个典型例子是默比乌斯 (Möbius) 带. 它的构造方法如下: 取一矩形长纸带 ABCD（如图 22-3(a)），将其一端

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 事实上, 可以证明, 只需对 $S$ 中某一点 $M_0$, 对通过 $M_0$ 且又不超出 $S$ 的边界的任何闭曲线 $L$ 上具有上述特性, 则 $S$ 是双侧曲面.</span></small>

262

---

§ 2 第二型曲面积分

扭转 $180^{\circ}$ 后与另一端黏合在一起（即让 $A$ 与 $C$ 重合，$B$ 与 $D$ 重合。如图22-3(b)所示）。读者可以考察这个带状曲面是单侧的。事实上，可在曲面上任取一条与其边界相平行的闭曲线 $L$，动点 $M$ 从 $L$ 上的点 $M_0$ 出发，其法线方向与 $M_0$ 的法线方向相一致，当 $M$ 沿 $L$ 连续变动一周回到 $M_0$ 时，由图22-3(b)看到，这时 $M$ 的法线方向却与 $M_0$ 的法线方向相反。对默比乌斯带还可更简单地说明它的单侧特性，即沿这个带子上任一处出发涂以一种颜色，则可以不越过边界而将它全部涂遍（即把原纸带的两面都涂上同样的颜色）。

![](../../raw/pages_0257-0288/images/page_270_image_2.jpg)

<details>
<summary>text_image</summary>

B
A
C
D
</details>

(a)

![](../../raw/pages_0257-0288/images/page_270_image_4.jpg)

<details>
<summary>text_image</summary>

BD
M₀
AC
</details>

(b)

图22-3

通常由 $z = z(x,y)$ 所表示的曲面都是双侧曲面，当以其法线正方向与 $z$ 轴正向的夹角成锐角的一侧（也称为上侧）为正侧时，则另一侧（也称下侧）为负侧.当 $S$ 为封闭曲面时，通常规定曲面的外侧为正侧，内侧为负侧

## 二、第二型曲面积分的概念

先观察一个流量计算问题. 设某流体以一定的流速

$$
\boldsymbol {v} = (P (x, y, z), Q (x, y, z), R (x, y, z))
$$

从给定的曲面 S 的负侧流向正侧(图 22-4)，其中 P, Q, R 为所讨论范围上的连续函数，求单位时间内流经曲面 S 的总流量 E.

设在曲面 $S$ 的正侧上任一点 $(x,y,z)$ 处的单位法向量为

$$
\boldsymbol {n} = (\cos \alpha , \cos \beta , \cos \gamma).
$$

这里  $\alpha,\beta,\gamma$  是 x,y,z 的函数, 则单位时间内流经小曲面  $S_{i}$  的流量近似地等于

$$
\begin{array}{l} \boldsymbol {v} (\xi_ {i}, \eta_ {i}, \zeta_ {i}) \cdot \boldsymbol {n} (\xi_ {i}, \eta_ {i}, \zeta_ {i}) \Delta S _ {i} \\ = \left[ P (\xi_ {i}, \eta_ {i}, \zeta_ {i}) \cos \alpha_ {i} + Q (\xi_ {i}, \eta_ {i}, \zeta_ {i}) \cos \beta_ {i} + \right. \\ R (\xi_ {i}, \eta_ {i}, \zeta_ {i}) \cos \gamma_ {i} ] \Delta S _ {i}, \\ \end{array}
$$

![](../../raw/pages_0257-0288/images/page_270_image_16.jpg)

<details>
<summary>text_image</summary>

S
S_i n v
(ξ_i, η_i, ζ_i)
</details>

图22-4

其中 $(\xi_{i},\eta_{i},\zeta_{i})$ 是 $S_{i}$ 上任意取定的一点， $\cos \alpha_{i},\cos \beta_{i},\cos \gamma_{i}$ 是 $S_{i}$ 的

正侧上法线的方向余弦，又 $\Delta S_{i}\cos \alpha_{i},\Delta S_{i}\cos \beta_{i},\Delta S_{i}\cos \gamma_{i}$ 分别是 $S_{i}$ 的正侧在坐标面$yz,zx$ 和 $xy$ 上投影区域的面积的近似值，并分别记作 $\Delta S_{i_yz},\Delta S_{i_{zx}},\Delta S_{i_{xy}}$ ，于是单位时间内由小曲面 $S_{i}$ 的负侧流向正侧的流量也近似地等于

$$
P (\xi_ {i}, \eta_ {i}, \zeta_ {i}) \Delta S _ {i _ {y z}} + Q (\xi_ {i}, \eta_ {i}, \zeta_ {i}) \Delta S _ {i _ {z x}} + R (\xi_ {i}, \eta_ {i}, \zeta_ {i}) \Delta S _ {i _ {x y}},
$$

故单位时间内由曲面 $S$ 的负侧流向正侧的总流量

$$
E = \lim _ {\| T \| \to 0} \sum_ {i = 1} ^ {n} \left\{P (\xi_ {i}, \eta_ {i}, \zeta_ {i}) \Delta S _ {i _ {y z}} + Q (\xi_ {i}, \eta_ {i}, \zeta_ {i}) \Delta S _ {i _ {z x}} + R (\xi_ {i}, \eta_ {i}, \zeta_ {i}) \Delta S _ {i _ {x y}} \right\}.
$$

263

---

第二十二章 曲面积分

这种与曲面的侧有关的和式极限就是所要讨论的第二型曲面积分.

定义1 设 P, Q, R 为定义在双侧曲面 S 上的函数，在 S 所指定的一侧作分割 T，它把 S 分为 n 个小曲面  $S_{1}, S_{2}, \cdots, S_{n}$ ，分割 T 的细度  $\|T\| = \max_{1 \leqslant i \leqslant n} \{S_{i} \text{ 的直径}\}$ ，以  $\Delta S_{i_{yz}}$ ， $\Delta S_{i_{zx}}, \Delta S_{i_{xy}}$  分别表示  $S_{i}$  在三个坐标面上的投影区域的面积，它们的符号由  $S_{i}$  的方向来确定。若  $S_{i}$  的法线正向与 z 轴正向成锐角时， $S_{i}$  在 xy 平面的投影区域的面积  $\Delta S_{i_{xy}}$  为正。反之，若  $S_{i}$  法线正向与 z 轴正向成钝角时，它在 xy 平面的投影区域的面积  $\Delta S_{i_{xy}}$  为负。在各个小曲面  $S_{i}$  上任取一点  $(\xi_{i}, \eta_{i}, \zeta_{i})$ 。若

$$
\lim _ {\| T \| \to 0} \sum_ {i = 1} ^ {n} P (\xi_ {i}, \eta_ {i}, \zeta_ {i}) \Delta S _ {i _ {y z}} + \lim _ {\| T \| \to 0} \sum_ {i = 1} ^ {n} Q (\xi_ {i}, \eta_ {i}, \zeta_ {i}) \Delta S _ {i _ {z x}} + \lim _ {\| T \| \to 0} \sum_ {i = 1} ^ {n} R (\xi_ {i}, \eta_ {i}, \zeta_ {i}) \Delta S _ {i _ {x y}}
$$

存在，且与曲面 $S$ 的分割 $T$ 和 $(\xi_{i},\eta_{i},\zeta_{i})$ 在 $S_{i}$ 上的取法无关，则称此极限为函数 $P,Q,$ $R$ 在曲面 $S$ 所指定的一侧上的第二型曲面积分，记作

$$
\iint_ {S} P (x, y, z) \mathrm{d} y \mathrm{d} z + Q (x, y, z) \mathrm{d} z \mathrm{d} x + R (x, y, z) \mathrm{d} x \mathrm{d} y \tag {1}
$$

或

$$
\iint_ {S} P (x, y, z) \mathrm{d} y \mathrm{d} z + \iint_ {S} Q (x, y, z) \mathrm{d} z \mathrm{d} x + \iint_ {S} R (x, y, z) \mathrm{d} x \mathrm{d} y.
$$

据此定义,某流体以速度  $\boldsymbol{v}=(P,Q,R)$  在单位时间内从曲面 S 的负侧流向正侧的总流量

$$
E = \iint_ {S} P (x, y, z) \mathrm{d} y \mathrm{d} z + Q (x, y, z) \mathrm{d} z \mathrm{d} x + R (x, y, z) \mathrm{d} x \mathrm{d} y.
$$

又若,空间的磁场强度为

$$
(P (x, y, z), Q (x, y, z), R (x, y, z)),
$$

则通过曲面 S 的磁通量(磁力线总数)

$$
H = \iint_ {S} P (x, y, z) \mathrm{d} y \mathrm{d} z + Q (x, y, z) \mathrm{d} z \mathrm{d} x + R (x, y, z) \mathrm{d} x \mathrm{d} y.
$$

若以-S 表示曲面 S 的另一侧, 由定义易得

$$
\begin{array}{l} \iint_ {- S} P \mathrm{d} y \mathrm{d} z + Q \mathrm{d} z \mathrm{d} x + R \mathrm{d} x \mathrm{d} y \\ = - \iint_ {S} P \mathrm{d} y \mathrm{d} z + Q \mathrm{d} z \mathrm{d} x + R \mathrm{d} x \mathrm{d} y. \\ \end{array}
$$

与第二型曲线积分一样,第二型曲面积分也有如下一些性质:

1. 若  $\iint_{S} P_{i} dy dz + Q_{i} dz dx + R_{i} dx dy \quad (i = 1, 2, \cdots, k)$  存在，则有

$$
\begin{array}{l} \iint_ {S} \left(\sum_ {i = 1} ^ {k} c _ {i} P _ {i}\right) \mathrm{d} y \mathrm{d} z + \left(\sum_ {i = 1} ^ {k} c _ {i} Q _ {i}\right) \mathrm{d} z \mathrm{d} x + \left(\sum_ {i = 1} ^ {k} c _ {i} R _ {i}\right) \mathrm{d} x \mathrm{d} y \\ = \sum_ {i = 1} ^ {k} c _ {i} \iint_ {S} P _ {i} \mathrm{d} y \mathrm{d} z + Q _ {i} \mathrm{d} z \mathrm{d} x + R _ {i} \mathrm{d} x \mathrm{d} y, \\ \end{array}
$$

264

---

§ 2 第二型曲面积分

其中  $c_{i}$  ( $i=1,2,\cdots,k$ ) 是常数.

2. 若曲面 S 是由两两无公共内点的曲面块  $S_{1}, S_{2}, \cdots, S_{k}$  所组成，且

$$
\iint_ {S _ {i}} P \mathrm{d} y \mathrm{d} z + Q \mathrm{d} z \mathrm{d} x + R \mathrm{d} x \mathrm{d} y \quad (i = 1, 2, \dots , k)
$$

存在,则有

$$
\begin{array}{l} \iint_ {S} P \mathrm{d} y \mathrm{d} z + Q \mathrm{d} z \mathrm{d} x + R \mathrm{d} x \mathrm{d} y \\ = \sum_ {i = 1} ^ {k} \iint_ {S _ {i}} P \mathrm{d} y \mathrm{d} z + Q \mathrm{d} z \mathrm{d} x + R \mathrm{d} x \mathrm{d} y. \\ \end{array}
$$

## 三、第二型曲面积分的计算

第二型曲面积分也是把它化为二重积分来计算.

定理 22.2 设 R 是定义在光滑曲面

$$
S \colon z = z (x, y), \quad (x, y) \in D _ {x y}
$$

上的连续函数,以 S 的上侧为正侧(这时 S 的法线方向与 z 轴正向成锐角),则有

$$
\iint_ {S} R (x, y, z) \mathrm{d} x \mathrm{d} y = \iint_ {D _ {x y}} R (x, y, z (x, y)) \mathrm{d} x \mathrm{d} y. \tag {2}
$$

证 由第二型曲面积分定义

$$
\begin{array}{l} \iint_ {S} R (x, y, z) \mathrm{d} x \mathrm{d} y = \lim _ {\| T \| \to 0} \sum_ {i = 1} ^ {n} R (\xi_ {i}, \eta_ {i}, \zeta_ {i}) \Delta S _ {i _ {x y}} \\ = \lim _ {d \to 0} \sum_ {i = 1} ^ {n} R (\xi_ {i}, \eta_ {i}, z (\xi_ {i}, \eta_ {i})) \Delta S _ {i _ {x y}}, \\ \end{array}
$$

这里 $d = \max \{S_{i_{xy}}$ 的直径}. 显然由 $\| T \| = \max \{S_i$ 的直径 $\} \to 0$ 立刻可推得 $d \to 0$. 由于 $R$ 在 $S$ 上连续, $z$ 在 $D_{xy}$ 上连续（曲面光滑！), 据复合函数的连续性, $R(x,y,z(x,y))$ 也是 $D_{xy}$ 上的连续函数. 由二重积分的定义

$$
\iint_ {D _ {x y}} R (x, y, z (x, y)) \mathrm{d} x \mathrm{d} y = \lim _ {d \to 0} \sum_ {i = 1} ^ {n} R (\xi_ {i}, \eta_ {i}, z (\xi_ {i}, \eta_ {i})) \Delta S _ {i _ {x y}}.
$$

所以

$$
\iint_ {S} R (x, y, z) \mathrm{d} x \mathrm{d} y = \iint_ {D _ {x y}} R (x, y, z (x, y)) \mathrm{d} x \mathrm{d} y.
$$

类似地, 当 P 在光滑曲面

$$
S \colon x = x (y, z), \quad (y, z) \in D _ {y z}
$$

上连续时,有

$$
\iint_ {S} P (x, y, z) \mathrm{d} y \mathrm{d} z = \iint_ {D _ {y z}} P (x (y, z), y, z) \mathrm{d} y \mathrm{d} z, \tag {3}
$$

这里 $S$ 是以 $S$ 的法线方向与 $x$ 轴的正向成锐角的那一侧为正侧. 当 $Q$ 在光滑曲面

$$
S \colon y = y (z, x), \quad (z, x) \in D _ {z x}
$$

上连续时,有

$$
\iint_ {S} Q (x, y, z) \mathrm{d} z \mathrm{d} x = \iint_ {D _ {z x}} Q (x, y (z, x), z) \mathrm{d} z \mathrm{d} x, \tag {4}
$$

265

---

第二十二章 曲面积分

这里 $S$ 是以 $S$ 的法线方向与 $y$ 轴的正向成锐角的那一侧为正侧.

例 1 计算  $\iint_{S} xyz \, dx \, dy$ ,

其中 S 是球面  $x^{2}+y^{2}+z^{2}=1$  在  $x\geqslant0, y\geqslant0$  部分并取球面外侧（图 22-5）.

解 曲面 S 在第一、五卦限部分的方程分别为

$$
S _ {1}: z _ {1} = \sqrt {1 - x ^ {2} - y ^ {2}},
$$

$$
S _ {2}: z _ {2} = - \sqrt {1 - x ^ {2} - y ^ {2}},
$$

![](../../raw/pages_0257-0288/images/page_273_image_7.jpg)

<details>
<summary>text_image</summary>

z
S₁
O
y
x
S₂
</details>

图22-5

它们在 xy 平面上的投影区域都是单位圆在第一象限部分. 依题意, 积分是沿  $S_{1}$  的上侧和  $S_{2}$  的下侧进行, 所以

$$
\begin{array}{l} \iint_ {S} x y z \mathrm{d} x \mathrm{d} y = \iint_ {S _ {1}} x y z \mathrm{d} x \mathrm{d} y + \iint_ {S _ {2}} x y z \mathrm{d} x \mathrm{d} y \\ = \iint_ {D _ {x y}} x y \sqrt {1 - x ^ {2} - y ^ {2}} \mathrm{d} x \mathrm{d} y - \iint_ {D _ {x y}} (- x y \sqrt {1 - x ^ {2} - y ^ {2}}) \mathrm{d} x \mathrm{d} y \\ = 2 \iint_ {D _ {x y}} x y \sqrt {1 - x ^ {2} - y ^ {2}} \mathrm{d} x \mathrm{d} y \\ = 2 \int_ {0} ^ {\frac {\pi}{2}} \mathrm{d} \theta \int_ {0} ^ {1} r ^ {3} \cos \theta \sin \theta \sqrt {1 - r ^ {2}} \mathrm{d} r = \frac {2}{1 5}. \\ \end{array}
$$

如果光滑曲面 S 由参量方程给出:

$$
S \colon \left\{ \begin{array}{l} x = x (u, v), \\ y = y (u, v), \\ z = z (u, v), \end{array} \right. \quad (u, v) \in D.
$$

若在 $D$ 上各点它们的函数行列式

$$
\frac {\partial (y , z)}{\partial (u , v)}, \quad \frac {\partial (z , x)}{\partial (u , v)}, \quad \frac {\partial (x , y)}{\partial (u , v)}
$$

不同时为零,则分别有

$$
\iint_ {S} P \mathrm{d} y \mathrm{d} z = \pm \iint_ {D} P (x (u, v), y (u, v), z (u, v)) \frac {\partial (y , z)}{\partial (u , v)} \mathrm{d} u \mathrm{d} v, \tag {5}
$$

$$
\iint_ {S} Q \mathrm{d} z \mathrm{d} x = \pm \iint_ {D} Q (x (u, v), y (u, v), z (u, v)) \frac {\partial (z , x)}{\partial (u , v)} \mathrm{d} u \mathrm{d} v, \tag {6}
$$

$$
\iint_ {S} R \mathrm{d} x \mathrm{d} y = \pm \iint_ {D} R (x (u, v), y (u, v), z (u, v)) \frac {\partial (x , y)}{\partial (u , v)} \mathrm{d} u \mathrm{d} v. \tag {7}
$$

注 （5），（6），（7）三式中的正负号分别对应曲面 S 的两个侧，特别当法向  $\left(\frac{\partial(y,z)}{\partial(u,v)},\frac{\partial(z,x)}{\partial(u,v)},\frac{\partial(x,y)}{\partial(u,v)}\right)$  对应于曲面 S 所选定的正向一侧时，取正号，否则取负号.

例2 计算

$$
\iint_ {S} x ^ {3} \mathrm{d} y \mathrm{d} z,
$$

其中 S 为椭球面  $\frac{x^{2}}{a^{2}}+\frac{y^{2}}{b^{2}}+\frac{z^{2}}{c^{2}}=1$  的上半部并选取外侧.

解 把曲面表示为参量方程

266

---

§ 2 第二型曲面积分

$$
x = a \sin \varphi \cos \theta , y = b \sin \varphi \sin \theta , z = c \cos \varphi \quad \left(0 \leqslant \varphi \leqslant \frac {\pi}{2}, 0 \leqslant \theta \leqslant 2 \pi\right).
$$

由(5)式有

$$
\iint_ {S} x ^ {3} \mathrm{d} y \mathrm{d} z = \pm \iint_ {D _ {\varphi \theta}} a ^ {3} \sin^ {3} \varphi \cos^ {3} \theta \cdot A \mathrm{d} \varphi \mathrm{d} \theta , \tag {8}
$$

其中

$$
A = \frac {\partial (y , z)}{\partial (\varphi , \theta)} = \left| \begin{array}{c c} b \cos \varphi \sin \theta & b \sin \varphi \cos \theta \\ - c \sin \varphi & 0 \end{array} \right| = b c \sin^ {2} \varphi \cos \theta ,
$$

积分是在 S 的上侧进行. 由上述的注, (8) 式右端取正号 (因为此时法向中  $\frac{\partial(x,y)}{\partial(\varphi,\theta)} = ab\sin\varphi\cos\varphi \geqslant 0$  对应 S 的正侧), 即

$$
\begin{array}{l} \iint_ {S} x ^ {3} \mathrm{d} y \mathrm{d} z = \iint_ {D _ {\varphi \theta}} a ^ {3} \sin^ {3} \varphi \cos^ {3} \theta \cdot b c \sin^ {2} \varphi \cos \theta \mathrm{d} \varphi \mathrm{d} \theta \\ = a ^ {3} b c \int_ {0} ^ {\frac {\pi}{2}} \sin^ {5} \varphi \mathrm{d} \varphi \int_ {0} ^ {2 \pi} \cos^ {4} \theta \mathrm{d} \theta = \frac {2}{5} \pi a ^ {3} b c. \\ \end{array}
$$

![](../../raw/pages_0257-0288/images/page_274_image_8.jpg)

## 四、两类曲面积分的联系

与曲线积分一样,当曲面的侧确定之后,可以建立两种类型曲面积分的联系.

设 S 为光滑曲面, 并以上侧为正侧, R 为 S 上的连续函数, 曲面积分在 S 的正侧进行. 因而有

$$
\iint_ {S} R (x, y, z) \mathrm{d} x \mathrm{d} y = \lim _ {\| T \| \to 0} \sum_ {i = 1} ^ {n} R (\xi_ {i}, \eta_ {i}, \zeta_ {i}) \Delta S _ {i _ {x y}}. \tag {9}
$$

由曲面面积公式(第二十一章 §6)

$$
\Delta S _ {i} = \iint_ {S _ {i _ {x y}}} \frac {1}{\cos \gamma} \mathrm{d} x \mathrm{d} y,
$$

其中 $\gamma$ 是曲面 $S_{i}$ 的法线方向与 $z$ 轴正向的交角，它是定义在 $S_{i_{xy}}$ 上的函数。因为积分沿曲面正侧进行，所以 $\gamma$ 是锐角。又由 $S$ 是光滑的，所以 $\cos \gamma$ 在闭区域 $S_{i_{xy}}$ 上连续。应用中值定理，在 $S_{i_{xy}}$ 内必存在一点，使这点的法线方向与 $z$ 轴正向的夹角 $\gamma_{i}^{*}$ 满足等式

$$
\Delta S _ {i} = \frac {1}{\cos \gamma_ {i} ^ {*}} \Delta S _ {i _ {x y}}
$$

或

$$
\Delta S _ {i _ {x y}} = \cos \gamma_ {i} ^ {*} \cdot \Delta S _ {i}.
$$

于是

$$
R (\xi_ {i}, \eta_ {i}, \zeta_ {i}) \Delta S _ {i _ {x y}} = R (\xi_ {i}, \eta_ {i}, \zeta_ {i}) \cos \gamma_ {i} ^ {*} \Delta S _ {i}.
$$

$n$ 个部分相加后得

$$
\sum_ {i = 1} ^ {n} R (\xi_ {i}, \eta_ {i}, \zeta_ {i}) \Delta S _ {i _ {x y}} = \sum_ {i = 1} ^ {n} R (\xi_ {i}, \eta_ {i}, \zeta_ {i}) \cos \gamma_ {i} ^ {*} \Delta S _ {i}. \tag {10}
$$

现以 $\cos \gamma_{i}$ 表示曲面 $S_{i}$ 在点 $(x_{i},y_{i},z_{i})$ 的法线方向与 $z$ 轴正向夹角的余弦，则由 $\cos \gamma$ 的连续性，可推得当 $\| T\| \to 0$ 时，(10)式右端极限存在.因此由(9)式得到

$$
\iint_ {S} R (x, y, z) \mathrm{d} x \mathrm{d} y = \iint_ {S} R (x, y, z) \cos \gamma \mathrm{d} S. \tag {11}
$$

267

---

第二十二章 曲面积分

这里注意当改变曲面的侧时, 左边积分改变符号, 右边积分中角  $\gamma$  改为  $\gamma \pm \pi$ . 因而  $\cos \gamma$  也改变符号, 所以右边积分也相应改变了符号. 同理可证:

$$
\iint_ {S} P (x, y, z) \mathrm{d} y \mathrm{d} z = \iint_ {S} P (x, y, z) \cos \alpha \mathrm{d} S, \tag {12}
$$

$$
\iint_ {S} Q (x, y, z) \mathrm{d} z \mathrm{d} x = \iint_ {S} Q (x, y, z) \cos \beta \mathrm{d} S,
$$

其中 $\alpha, \beta$ 分别是 $S$ 上的法线方向与 $x$ 轴正向和与 $y$ 轴正向的夹角. 一般地有

$$
\begin{array}{l} \iint_ {S} P (x, y, z) \mathrm{d} y \mathrm{d} z + Q (x, y, z) \mathrm{d} z \mathrm{d} x + R (x, y, z) \mathrm{d} x \mathrm{d} y \\ = \iint_ {S} [ P (x, y, z) \cos \alpha + Q (x, y, z) \cos \beta + R (x, y, z) \cos \gamma ] \mathrm{d} S. \tag {13} \\ \end{array}
$$

这样,在确定了余弦函数  $\cos\alpha,\cos\beta,\cos\gamma$  之后,由(11),(12)或(13)式便建立了两种不同类型曲面积分的联系.

定理 22.3 设 S 为光滑曲面, 正侧法向量为  $(\cos \alpha, \cos \beta, \cos \gamma)$ ,  $P(x, y, z)$ ,  $Q(x, y, z)$ ,  $R(x, y, z)$  在 S 上连续, 则

$$
\begin{array}{l} \iint_ {S} P (x, y, z) \mathrm{d} y \mathrm{d} z + Q (x, y, z) \mathrm{d} z \mathrm{d} x + R (x, y, z) \mathrm{d} x \mathrm{d} y \\ = \iint_ {S} (P (x, y, z) \cos \alpha + Q (x, y, z) \cos \beta + R (x, y, z) \cos \gamma) \mathrm{d} S. \\ \end{array}
$$

定理 22.4 设 P, Q, R 是定义在光滑曲面  $S: z = z(x, y), (x, y) \in D$  上的连续函数，以 S 的上侧为正侧，则

$$
\begin{array}{l} \iint_ {S} P (x, y, z) \mathrm{d} y \mathrm{d} z + Q (x, y, z) \mathrm{d} z \mathrm{d} x + R (x, y, z) \mathrm{d} x \mathrm{d} y \\ = \iint_ {D} (P (x, y, z (x, y)) (- z _ {x}) + Q (x, y, z (x, y)) (- z _ {y}) + R (x, y, z (x, y))) \mathrm{d} x \mathrm{d} y. \\ \end{array}
$$

证 由于

$$
\cos \alpha = \frac {- z _ {x}}{\sqrt {1 + z _ {x} ^ {2} + z _ {y} ^ {2}}}, \cos \beta = \frac {- z _ {y}}{\sqrt {1 + z _ {x} ^ {2} + z _ {y} ^ {2}}}, \cos \gamma = \frac {1}{\sqrt {1 + z _ {x} ^ {2} + z _ {y} ^ {2}}}, \mathrm{d} S = \sqrt {1 + z _ {x} ^ {2} + z _ {y} ^ {2}} \mathrm{d} x \mathrm{d} y,
$$

因此

$$
\begin{array}{l} \iint_ {S} P (x, y, z) \mathrm{d} y \mathrm{d} z + Q (x, y, z) \mathrm{d} z \mathrm{d} x + R (x, y, z) \mathrm{d} x \mathrm{d} y \\ = \iint_ {S} (P (x, y, z) \cos \alpha + Q (x, y, z) \cos \beta + R (x, y, z) \cos \gamma) \mathrm{d} S \\ = \iint_ {D} (P (x, y, z (x, y)) (- z _ {x}) + Q (x, y, z (x, y)) (- z _ {y}) + \\ R (x, y, z (x, y)) \mathrm{d} x \mathrm{d} y. \\ \end{array}
$$

例 3 计算  $\iint_{S}(2x+z)\mathrm{d}y\mathrm{d}z+z\mathrm{d}x\mathrm{d}y$ ，其中  $S=\left\{(x,y,z)\mid z=x^{2}+y^{2},z\in[0,1]\right\}$ ，取上侧.

268

---

§ 3 高斯公式与斯托克斯公式

解 $z_{x} = 2x, z_{y} = 2y,$

$$
\begin{array}{l} I = \iint_ {D} \left(\left(2 x + x ^ {2} + y ^ {2}\right) (- 2 x) + x ^ {2} + y ^ {2}\right) \mathrm{d} x \mathrm{d} y = \iint_ {D} \left(y ^ {2} - 3 x ^ {2}\right) \mathrm{d} x \mathrm{d} y \\ = - \iint_ {D} 2 x ^ {2} \mathrm{d} x \mathrm{d} y = - 2 \int_ {0} ^ {2 \pi} \mathrm{d} \theta \int_ {0} ^ {1} r ^ {2} \cos^ {2} \theta r \mathrm{d} r = - \frac {\pi}{2}, \\ \end{array}
$$

其中由于 $x(x^{2} + y^{2})$ 是 $x$ 的奇函数， $\iint_{D}x(x^{2} + y^{2})\mathrm{d}x\mathrm{d}y = 0$ ；又由对称性，

$$
\iint_ {D} x ^ {2} \mathrm{d} x \mathrm{d} y = \iint_ {D} y ^ {2} \mathrm{d} x \mathrm{d} y.
$$

## 习题 22.2

1. 计算下列第二型曲面积分:

(1) $\iint_{S} y(x - z) \, \mathrm{d}y \, \mathrm{d}z + x^2 \, \mathrm{d}z \, \mathrm{d}x + (y^2 + xz) \, \mathrm{d}x \, \mathrm{d}y$，其中 $S$ 为由 $x = y = z = 0, x = y = z = a$ 六个平面所围的立方体表面并取外侧为正向；
(2) $\iint_{S}(x + y)\mathrm{d}y\mathrm{d}z + (y + z)\mathrm{d}z\mathrm{d}x + (z + x)\mathrm{d}x\mathrm{d}y$ ，其中 $S$ 是以原点为中心，边长为2的立方体表面并取外侧为正向；
(3) $\iint_{S} xy \, \mathrm{d}y \, \mathrm{d}z + yz \, \mathrm{d}z \, \mathrm{d}x + xz \, \mathrm{d}x \, \mathrm{d}y$，其中 $S$ 是由平面 $x = y = z = 0$ 和 $x + y + z = 1$ 所围的四面体表面并取外侧为正向；
(4) $\iint_{S} yz \, \mathrm{d}z \, \mathrm{d}x$，其中 $S$ 是球面 $x^{2} + y^{2} + z^{2} = 1$ 的上半部分并取外侧为正向；
(5) $\iint_{S} x^{2} \, \mathrm{d}y \, \mathrm{d}z + y^{2} \, \mathrm{d}z \, \mathrm{d}x + z^{2} \, \mathrm{d}x \, \mathrm{d}y$，其中 $S$ 是球面 $(x - a)^{2} + (y - b)^{2} + (z - c)^{2} = R^{2}$ 并取外侧为正向.

2. 设某流体的流速为  $\boldsymbol{v}=(k,y,0)$ ，求单位时间内从球面  $x^{2}+y^{2}+z^{2}=4$  的内部流过球面的流量.

3. 计算第二型曲面积分

$$
I = \iint_ {S} f (x) \mathrm{d} y \mathrm{d} z + g (y) \mathrm{d} z \mathrm{d} x + h (z) \mathrm{d} x \mathrm{d} y,
$$

其中 $S$ 是平行六面体 $0 \leqslant x \leqslant a, 0 \leqslant y \leqslant b, 0 \leqslant z \leqslant c$ 的表面并取外侧为正向，$f(x), g(y), h(z)$ 为 $S$ 上的连续函数.

4. 设磁场强度为 $E(x, y, z) = (x^2, y^2, z^2)$，求从球内出发通过上半球面 $x^2 + y^2 + z^2 = a^2$，$z \geqslant 0$ 的磁通量.

## § 3 高斯公式与斯托克斯公式

## 一、高斯公式

格林公式建立了沿封闭曲线的曲线积分与二重积分的关系,沿空间闭曲面的曲面

269

---

第二十二章 曲面积分

积分和三重积分之间也有类似的关系,这就是本段所要讨论的高斯(Gauss)公式.

定理 22.5 设空间区域 V 由分片光滑的双侧封闭曲面 S 围成. 若函数 P, Q, R 在 V 上连续, 且有一阶连续偏导数, 则

$$
\iiint_ {V} \left(\frac {\partial P}{\partial x} + \frac {\partial Q}{\partial y} + \frac {\partial R}{\partial z}\right) \mathrm{d} x \mathrm{d} y \mathrm{d} z
$$

$$
= \oiint_ {S} P \mathrm{d} y \mathrm{d} z + Q \mathrm{d} z \mathrm{d} x + R \mathrm{d} x \mathrm{d} y ^ {(1)}, \tag {1}
$$

其中 S 取外侧。(1)式称为高斯公式.

证 下面只证

$$
\iiint_ {V} \frac {\partial R}{\partial z} \mathrm{d} x \mathrm{d} y \mathrm{d} z = \oiint_ {S} R \mathrm{d} x \mathrm{d} y.
$$

读者可类似地证明

$$
\iiint_ {V} \frac {\partial P}{\partial x} \mathrm{d} x \mathrm{d} y \mathrm{d} z = \oiint_ {S} P \mathrm{d} y \mathrm{d} z,
$$

$$
\iiint_ {V} \frac {\partial Q}{\partial y} \mathrm{d} x \mathrm{d} y \mathrm{d} z = \oiint_ {S} Q \mathrm{d} z \mathrm{d} x.
$$

这些结果相加便得到了高斯公式(1).

先设 $V$ 是一个 $xy$ 型区域，即其边界曲面 $S$ 由曲面

$$
S _ {2}: z = z _ {2} (x, y), (x, y) \in D _ {x y},
$$

$$
S _ {1}: z = z _ {1} (x, y), (x, y) \in D _ {x y}
$$

及垂直于 $D_{xy}$ 的边界的柱面 $S_{3}$ 组成（图22-6），其中 $z_{1}(x,y)\leqslant z_{2}(x,y)$ .于是按三重积分的计算方法有

![](../../raw/pages_0257-0288/images/page_277_image_16.jpg)

<details>
<summary>text_image</summary>

z
S₂
S₃
S₁
O
y
x
Dₓᵧ
</details>

图22-6

$$
\iiint_ {V} \frac {\partial R}{\partial z} \mathrm{d} x \mathrm{d} y \mathrm{d} z
$$

$$
= \iint_ {D _ {x y}} \mathrm{d} x \mathrm{d} y \int_ {z _ {1} (x, y)} ^ {z _ {2} (x, y)} \frac {\partial R}{\partial z} \mathrm{d} z
$$

$$
= \iint_ {D _ {x y}} (R (x, y, z _ {2} (x, y)) - R (x, y, z _ {1} (x, y)) \mathrm{d} x \mathrm{d} y
$$

$$
= \iint_ {D _ {x y}} R (x, y, z _ {2} (x, y)) \mathrm{d} x \mathrm{d} y - \iint_ {D _ {x y}} R (x, y, z _ {1} (x, y)) \mathrm{d} x \mathrm{d} y
$$

$$
= \iint_ {S _ {2}} R (x, y, z) \mathrm{d} x \mathrm{d} y - \iint_ {S _ {1}} R (x, y, z) \mathrm{d} x \mathrm{d} y
$$

$$
= \iint_ {S _ {2}} R (x, y, z) \mathrm{d} x \mathrm{d} y + \iint_ {- S _ {1}} R (x, y, z) \mathrm{d} x \mathrm{d} y,
$$

其中 $S_{1}, S_{2}$ 都取上侧. 又由于 $S_{3}$ 在 $xy$ 平面上投影区域的面积为零, 所以

① 若 S 为封闭曲面, 则曲面积分的积分号用  $\oiint$  表示.

270

---

§ 3 高斯公式与斯托克斯公式

$$
\iint_ {S _ {3}} R (x, y, z) \mathrm{d} x \mathrm{d} y = 0.
$$

因此

$$
\begin{array}{l} \iiint_ {V} \frac {\partial R}{\partial z} \mathrm{d} x \mathrm{d} y \mathrm{d} z = \iint_ {S _ {2}} R \mathrm{d} x \mathrm{d} y + \iint_ {- S _ {1}} R \mathrm{d} x \mathrm{d} y + \iint_ {S _ {3}} R \mathrm{d} x \mathrm{d} y \\ = \oiint_ {S} R \mathrm{d} x \mathrm{d} y. \\ \end{array}
$$

对于不是 xy 型区域的情形,则用有限个光滑曲面将它分割成若干个 xy 型区域来讨论.详细的推导与格林公式相似,这里不再细说了.

高斯公式可用来简化某些曲面积分的计算.

例1 计算

$$
\oiint_ {S} y (x - z) \mathrm{d} y \mathrm{d} z + x ^ {2} \mathrm{d} z \mathrm{d} x + (y ^ {2} + x z) \mathrm{d} x \mathrm{d} y,
$$

其中 S 是边长为 a 的正立方体表面并取外侧(即上节习题 1(1)).

解 应用高斯公式,所求曲面积分等于

$$
\begin{array}{l} = \iiint_ {V} (y + x) \mathrm{d} x \mathrm{d} y \mathrm{d} z = \int_ {0} ^ {a} \mathrm{d} z \int_ {0} ^ {a} \mathrm{d} y \int_ {0} ^ {a} (y + x) \mathrm{d} x \\ = a \int_ {0} ^ {a} \left(a y + \frac {1}{2} a ^ {2}\right) \mathrm{d} y = a ^ {4}. \\ \end{array}
$$

$$
\iiint_ {V} \left[ \frac {\partial}{\partial x} (y (x - z)) + \frac {\partial}{\partial y} (x ^ {2}) + \frac {\partial}{\partial z} (y ^ {2} + x z) \right] \mathrm{d} x \mathrm{d} y \mathrm{d} z
$$

若高斯公式中 $P = x, Q = y, R = z$，则有

$$
\iiint_ {V} (1 + 1 + 1) \mathrm{d} x \mathrm{d} y \mathrm{d} z = \oiint_ {S} x \mathrm{d} y \mathrm{d} z + y \mathrm{d} z \mathrm{d} x + z \mathrm{d} x \mathrm{d} y.
$$

于是得到应用第二型曲面积分计算空间区域 $V$ 的体积公式

$$
\Delta V = \frac {1}{3} \oiint_ {S} x \mathrm{d} y \mathrm{d} z + y \mathrm{d} z \mathrm{d} x + z \mathrm{d} x \mathrm{d} y.
$$

## 二、斯托克斯公式

斯托克斯(Stokes)公式是建立沿空间双侧曲面 S 的积分与沿 S 的边界曲线 L 的积分之间的联系.

在讲下述定理之前,先对双侧曲面 S 的侧与其边界曲线 L 的方向作如下规定:设有人站在 S 上指定的一侧,若沿 L 行走,指定的侧总在人的左方,则人前进的方向为边界线 L 的正向;若沿 L 行走,指定的侧总在人的右方,则人前进的方向为边界线 L 的负向,这个规定方法也称为右手法则,如图 22-7 所示.

![](../../raw/pages_0257-0288/images/page_278_image_19.jpg)

<details>
<summary>text_image</summary>

正向
L
S
L
负向
S
</details>

图22-7

271

---

第二十二章 曲面积分

定理22.6 设光滑曲面 $S$ 的边界 $L$ 是按段光滑的连续曲线. 若函数 $P, Q, R$ 在 $S$ （连同 $L$ )上连续，且有一阶连续偏导数，则

$$
\begin{array}{l} \iint_ {S} \left(\frac {\partial R}{\partial y} - \frac {\partial Q}{\partial z}\right) \mathrm{d} y \mathrm{d} z + \left(\frac {\partial P}{\partial z} - \frac {\partial R}{\partial x}\right) \mathrm{d} z \mathrm{d} x + \left(\frac {\partial Q}{\partial x} - \frac {\partial P}{\partial y}\right) \mathrm{d} x \mathrm{d} y \\ = \oint_ {L} P \mathrm{d} x + Q \mathrm{d} y + R \mathrm{d} z, \tag {2} \\ \end{array}
$$

其中 S 的侧与 L 的方向按右手法则确定.

证 先证

$$
\iint_ {S} \frac {\partial P}{\partial z} \mathrm{d} z \mathrm{d} x - \frac {\partial P}{\partial y} \mathrm{d} x \mathrm{d} y = \oint_ {L} P \mathrm{d} x, \tag {3}
$$

其中曲面 $S$ 由方程 $z = z(x,y)$ 确定，它的正侧法线方向数为 $(-z_{x}, - z_{y},1)$ ，方向余弦为$(\cos \alpha ,\cos \beta ,\cos \gamma)$ ，所以

$$
\frac {\partial z}{\partial x} = - \frac {\cos \alpha}{\cos \gamma}, \quad \frac {\partial z}{\partial y} = - \frac {\cos \beta}{\cos \gamma}.
$$

若 $S$ 在 $xy$ 平面上投影区域为 $D_{xy}, L$ 在 $xy$ 平面上的投影曲线记为 $\Gamma$. 现由第二型曲线积分定义及格林公式有

$$
\begin{array}{l} \oint_ {L} P (x, y, z) \mathrm{d} x = \oint_ {\Gamma} P (x, y, z (x, y)) \mathrm{d} x \\ = - \iint_ {D _ {x y}} \frac {\partial}{\partial y} P (x, y, z (x, y)) \mathrm{d} x \mathrm{d} y. \\ \end{array}
$$

因为

$$
\frac {\partial}{\partial y} P (x, y, z (x, y)) = \frac {\partial P}{\partial y} + \frac {\partial P}{\partial z} \frac {\partial z}{\partial y},
$$

所以

$$
- \iint_ {D _ {x y}} \frac {\partial}{\partial y} P (x, y, z (x, y)) \mathrm{d} x \mathrm{d} y = - \iint_ {S} \left(\frac {\partial P}{\partial y} + \frac {\partial P}{\partial z} \frac {\partial z}{\partial y}\right) \mathrm{d} x \mathrm{d} y.
$$

由于 $\frac{\partial z}{\partial y}=-\frac{\cos\beta}{\cos\gamma}$ ，从而

$$
\begin{array}{l} - \iint_ {S} \left(\frac {\partial P}{\partial y} + \frac {\partial P}{\partial z} \frac {\partial z}{\partial y}\right) \mathrm{d} x \mathrm{d} y = - \iint_ {S} \left(\frac {\partial P}{\partial y} - \frac {\partial P}{\partial z} \frac {\cos \beta}{\cos \gamma}\right) \mathrm{d} x \mathrm{d} y \\ = - \iint_ {S} \left(\frac {\partial P}{\partial y} \cos \gamma - \frac {\partial P}{\partial z} \cos \beta\right) \frac {\mathrm{d} x \mathrm{d} y}{\cos \gamma} \\ = - \iint_ {S} \left(\frac {\partial P}{\partial y} \cos \gamma - \frac {\partial P}{\partial z} \cos \beta\right) \mathrm{d} S \\ = \iint_ {S} \frac {\partial P}{\partial z} \mathrm{d} z \mathrm{d} x - \frac {\partial P}{\partial y} \mathrm{d} x \mathrm{d} y. \\ \end{array}
$$

综合上述结果,便得所要证明的(3)式.

同样对于曲面 S 表示为  $x = x(y, z)$  和  $y = y(z, x)$  时，可证得

$$
\iint_ {S} \frac {\partial Q}{\partial x} \mathrm{d} x \mathrm{d} y - \frac {\partial Q}{\partial z} \mathrm{d} y \mathrm{d} z = \oint_ {L} Q \mathrm{d} y \tag {4}
$$

和

272

---

§ 3 高斯公式与斯托克斯公式

$$
\iint_ {S} \frac {\partial R}{\partial y} \mathrm{d} y \mathrm{d} z - \frac {\partial R}{\partial x} \mathrm{d} z \mathrm{d} x = \oint_ {L} R \mathrm{d} z. \tag {5}
$$

将(3)，(4)，(5)三式相加即得(2)式.

如果曲面 $S$ 不能以 $z = z(x,y)$ 的形式给出，则可用一些光滑曲线把 $S$ 分割为若干小块，使每一小块能用这种形式来表示.因而这时(2)式也能成立.

公式(2)称为斯托克斯公式.

为了便于记忆,斯托克斯公式也常写成如下形式:

$$
\iint_ {S} \left| \begin{array}{c c c} \mathrm{d} y \mathrm{d} z & \mathrm{d} z \mathrm{d} x & \mathrm{d} x \mathrm{d} y \\ \frac {\partial}{\partial x} & \frac {\partial}{\partial y} & \frac {\partial}{\partial z} \\ P & Q & R \end{array} \right| = \oint_ {L} P \mathrm{d} x + Q \mathrm{d} y + R \mathrm{d} z.
$$

例2 计算

$$
I = \oint_ {L} (y ^ {2} - z ^ {2}) \mathrm{d} x + (z ^ {2} - x ^ {2}) \mathrm{d} y + (x ^ {2} - y ^ {2}) \mathrm{d} z,
$$

其中 $L$ 是立方体 $[0, a] \times [0, a] \times [0, a]$ 的表面与平面 $x + y + z = \frac{3a}{2}$ 的交线，从 $z$ 轴正向看去取逆时针方向（图22-8）.

解 令 S 为  $x+y+z=\frac{3a}{2}$  被 L 所围的一块, 取上侧, 由斯托克斯公式,

![](../../raw/pages_0257-0288/images/page_280_image_11.jpg)

<details>
<summary>text_image</summary>

z
a
S
O
a
y
x
</details>

图22-8

$$
\begin{array}{l} I = \iint_ {S} \left| \begin{array}{c c c} \mathrm{d} y \mathrm{d} z & \mathrm{d} z \mathrm{d} x & \mathrm{d} x \mathrm{d} y \\ \frac {\partial}{\partial x} & \frac {\partial}{\partial y} & \frac {\partial}{\partial z} \\ y ^ {2} - z ^ {2} & z ^ {2} - x ^ {2} & x ^ {2} - y ^ {2} \end{array} \right| \\ = \iint_ {S} (- 2 y - 2 z) \mathrm{d} y \mathrm{d} z + (- 2 z - 2 x) \mathrm{d} z \mathrm{d} x + (- 2 x - 2 y) \mathrm{d} x \mathrm{d} y \\ = \frac {1}{\sqrt {3}} \iint_ {S} - 4 (x + y + z) \mathrm{d} S \\ = - 2 \sqrt {3} a \iint_ {S} \mathrm{d} S = - \frac {9}{2} a ^ {3}. \\ \end{array}
$$

由斯托克斯公式,可导出空间曲线积分与路线无关的条件.为此先介绍一下空间单连通区域的概念.

区域 $V$ 称为单连通区域, 如果 $V$ 内任一封闭曲线皆可以不经过 $V$ 以外的点而连续收缩于属于 $V$ 的一点. 如球体是单连通区域. 非单连通区域称为复连通区域. 如环状区域不是单连通区域, 而是复连通区域.

与平面曲线积分相仿,空间曲线积分与路线的无关性也有下面相应的定理.

定理22.7 设 $\Omega \subset \mathbf{R}^3$ 为空间单连通区域. 若函数 $P, Q, R$ 在 $\Omega$ 上连续, 且有一阶连续偏导数, 则以下四个条件是等价的:

(i) 对于  $\Omega$  内任一按段光滑的封闭曲线 L, 有

273

---

第二十二章 曲面积分

$$
\oint_ {L} P \mathrm{d} x + Q \mathrm{d} y + R \mathrm{d} z = 0;
$$

(ii) 对于  $\Omega$  内任一按段光滑的曲线 L, 曲线积分

$$
\int_ {L} P \mathrm{d} x + Q \mathrm{d} y + R \mathrm{d} z
$$

与路线无关；

(iii)  $Pdx + Qdy + Rdz$  是  $\Omega$  内某一函数 u 的全微分, 即

$$
\mathrm{d} u = P \mathrm{d} x + Q \mathrm{d} y + R \mathrm{d} z; \tag {6}
$$

(iv) $\frac{\partial P}{\partial y} = \frac{\partial Q}{\partial x}, \frac{\partial Q}{\partial z} = \frac{\partial R}{\partial y}, \frac{\partial R}{\partial x} = \frac{\partial P}{\partial z}$ 在 $\Omega$ 内处处成立.

这个定理的证明与定理 21.12 相仿, 这里不重复了.

例 3 验证曲线积分

$$
\int_ {L} (y + z) \mathrm{d} x + (z + x) \mathrm{d} y + (x + y) \mathrm{d} z
$$

与路线无关,并求被积表达式的原函数  $u(x,y,z)$ .

解 由于

$$
P = y + z, \quad Q = z + x, \quad R = x + y,
$$

$$
\frac {\partial P}{\partial y} = \frac {\partial Q}{\partial x} = \frac {\partial Q}{\partial z} = \frac {\partial R}{\partial y} = \frac {\partial R}{\partial x} = \frac {\partial P}{\partial z} = 1,
$$

所以曲线积分与路线无关.

现在求

$$
u (x, y, z) = \int_ {M _ {0} M} (y + z) \mathrm{d} x + (z + x) \mathrm{d} y + (x + y) \mathrm{d} z.
$$

![](../../raw/pages_0257-0288/images/page_281_image_18.jpg)

<details>
<summary>text_image</summary>

z
M(x,y,z)
O
M₀(x₀,y₀,z₀)
y
x
M₁
M₂
</details>

图22-9

取 $M_{0}M$ 如图22-9，从 $M_{0}$ 沿平行于x轴的直线到 $M_{1}(x,y_{0},z_{0})$ ，

再沿平行于 $y$ 轴的直线到 $M_{2}(x,y,z_{0})$ ，最后沿平行于 $z$ 轴的直线到 $M(x,y,z)$ .于是

$$
\begin{array}{l} u (x, y, z) = \int_ {x _ {0}} ^ {x} (y _ {0} + z _ {0}) \mathrm{d} s + \int_ {y _ {0}} ^ {y} (z _ {0} + x) \mathrm{d} t + \int_ {z _ {0}} ^ {z} (x + y) \mathrm{d} r \\ = (y _ {0} + z _ {0}) x - (y _ {0} + z _ {0}) x _ {0} + (z _ {0} + x) y - \\ (z _ {0} + x) y _ {0} + (x + y) z - (x + y) z _ {0} \\ = x y + x z + y z + c, \\ \end{array}
$$

其中 $c = -x_0y_0 - x_0z_0 - y_0z_0$ 是一个常数.若取 $M_0$ 为原点，则得

$$
u (x, y, z) = x y + x z + y z.
$$

## 习题 22.3

1. 应用高斯公式计算下列曲面积分:

(1) $\iint_{S} yz \, \mathrm{d}y \, \mathrm{d}z + zx \, \mathrm{d}z \, \mathrm{d}x + xy \, \mathrm{d}x \, \mathrm{d}y$，其中 $S$ 是单位球面 $x^2 + y^2 + z^2 = 1$ 的外侧；
(2) $\iint_{S} x^{2} \, \mathrm{d}y \, \mathrm{d}z + y^{2} \, \mathrm{d}z \, \mathrm{d}x + z^{2} \, \mathrm{d}x \, \mathrm{d}y$，其中 $S$ 是立方体 $0 \leqslant x, y, z \leqslant a$ 表面的外侧；
(3) $\iint_{S} x^{2} \, \mathrm{d}y \, \mathrm{d}z + y^{2} \, \mathrm{d}z \, \mathrm{d}x + z^{2} \, \mathrm{d}x \, \mathrm{d}y$，其中 $S$ 是锥面 $x^{2} + y^{2} = z^{2}$ 与平面 $z = h$ 所围空间区域

274

---

§ 3 高斯公式与斯托克斯公式

$(0 \leqslant z \leqslant h)$  的表面, 方向取外侧;

(4) $\iint_{S} x^3 \, \mathrm{d}y \, \mathrm{d}z + y^3 \, \mathrm{d}z \, \mathrm{d}x + z^3 \, \mathrm{d}x \, \mathrm{d}y$，其中 $S$ 是单位球面 $x^2 + y^2 + z^2 = 1$ 的外侧；
(5) $\iint_{S} x \, \mathrm{d}y \, \mathrm{d}z + y \, \mathrm{d}z \, \mathrm{d}x + z \, \mathrm{d}x \, \mathrm{d}y$，其中 $S$ 是上半球面 $z = \sqrt{a^2 - x^2 - y^2}$ 的外侧.

2. 应用高斯公式计算三重积分

$$
\iiint_ {V} (x y + y z + z x) \mathrm{d} x \mathrm{d} y \mathrm{d} z,
$$

其中 $V$ 是由 $x \geqslant 0, y \geqslant 0, 0 \leqslant z \leqslant 1$ 与 $x^{2} + y^{2} \leqslant 1$ 所确定的空间区域.

3. 应用斯托克斯公式计算下列曲线积分:

(1) $\oint_{L}(y^{2} + z^{2})\mathrm{d}x + (x^{2} + z^{2})\mathrm{d}y + (x^{2} + y^{2})\mathrm{d}z$ ，其中 $L$ 为 $x + y + z = 1$ 与三坐标面的交线，它的走向使所围平面区域上侧在曲线的左侧；
(2) $\oint_{L} x^{2} y^{3} \mathrm{~d} x + \mathrm{d} y + z \mathrm{~d} z$，其中 $L$ 为 $y^{2} + z^{2} = 1, x = y$ 所交的椭圆的正向；
(3) $\oint_{L}(z - y)\mathrm{d}x + (x - z)\mathrm{d}y + (y - x)\mathrm{d}z$ ，其中 $L$ 为以 $A(a,0,0),B(0,a,0),C(0,0,a)$ 为顶点的三角形沿ABCA的方向.

4. 求下列全微分的原函数:

(1)  $yzdx + xzdy + xydz;$
(2) $(x^{2}-2yz)\mathrm{d}x+(y^{2}-2xz)\mathrm{d}y+(z^{2}-2xy)\mathrm{d}z.$

5. 验证下列线积分与路线无关,并计算其值:

(1)  $\int_{(1,1,1)}^{(2,3,-4)}x\mathrm{d}x + y^{2}\mathrm{d}y - z^{3}\mathrm{d}z;$
(2) $\int_{(x_1,y_1,z_1)}^{(x_2,y_2,z_2)}\frac{x\mathrm{d}x + y\mathrm{d}y + z\mathrm{d}z}{\sqrt{x^2 + y^2 + z^2}}$ ，其中 $(x_{1},y_{1},z_{1}),(x_{2},y_{2},z_{2})$ 在球面 $x^{2} + y^{2} + z^{2} = a^{2}$ 上.

6. 证明:由曲面 $S$ 所包围的立体 $V$ 的体积 $\Delta V$ 为

$$
\Delta V = \frac {1}{3} \oiint_ {S} (x \cos \alpha + y \cos \beta + z \cos \gamma) \mathrm{d} S,
$$

其中  $\cos\alpha,\cos\beta,\cos\gamma$  为曲面 S 的外法线方向余弦.

7. 证明:若 S 为封闭曲面，l 为任何固定方向，则

$$
\oiint_ {S} \cos (\widehat {\boldsymbol {n}}, \boldsymbol {l}) \mathrm{d} S = 0,
$$

其中 n 为曲面 S 的外法线方向.

8. 证明公式

$$
\iiint_ {V} \frac {\mathrm{d} x \mathrm{d} y \mathrm{d} z}{r} = \frac {1}{2} \oiint_ {S} \cos (\widehat {\boldsymbol {r}}, \boldsymbol {n}) \mathrm{d} S,
$$

其中 $S$ 是包围 $V$ 的曲面，$\pmb{n}$ 是 $S$ 的外法线方向，$r = \sqrt{x^2 + y^2 + z^2}$，$\pmb{r} = (x, y, z)$.

9. 若 $L$ 是平面 $x \cos \alpha + y \cos \beta + z \cos \gamma - p = 0$ 上的闭曲线，它所包围区域的面积为 $S$，求

$$
\oint_ {L} \left| \begin{array}{c c c} \mathrm{d} x & \mathrm{d} y & \mathrm{d} z \\ \cos \alpha & \cos \beta & \cos \gamma \\ x & y & z \end{array} \right|,
$$

其中 L 依正向进行.

275

---

第二十二章 曲面积分

## \* §4 场论初步

## 一、场的概念

若对全空间或其中某一区域 $V$ 中每一点 $M$, 都有一个数量 (或向量) 与之对应, 则称在 $V$ 上给定了一个数量场 (或向量场).

温度场和密度场都是数量场. 在空间中引进了直角坐标系后, 空间中点 $M$ 的位置可由坐标确定. 因此, 给定了某个数量场就等于给定了一个数量函数 $u(x, y, z)$. 在以下讨论中, 我们总是设 $u(x, y, z)$ 对每个变量都有连续偏导数. 若这些偏导数不同时等于零, 则满足方程

$$
u (x, y, z) = c (c \text {为常数})
$$

的所有的点通常是一个曲面. 在这曲面上函数 $u$ 都取同一值, 因此常称它为等值面. 例如温度场中的等温面等.

向量场可以重力场或速度场为例. 当引进直角坐标系后, 向量场就与向量函数 $A(x, y, z)$ 相对应. 设 $A$ 在三个坐标轴上的投影分别为

$$
P (x, y, z), Q (x, y, z), R (x, y, z),
$$

则

$$
A (x, y, z) = (P (x, y, z), Q (x, y, z), R (x, y, z)),
$$

这里 P, Q, R 为所定义区域上的数量函数，并假定它们有连续偏导数.

设 $L$ 为向量场中一条曲线. 若 $L$ 上每点 $M$ 处的切线方向都与向量函数 $A$ 在该点的方向一致, 即

$$
\frac {\mathrm{d} x}{P} = \frac {\mathrm{d} y}{Q} = \frac {\mathrm{d} z}{R},
$$

则称曲线 L 为向量场 A 的向量场线. 例如电力线、磁力线等都是向量场线.

需要注意,场的性质是它自己的属性,和坐标系的引进无关.引入或选择某种坐标系是为了便于通过数学方法来研究它的性质.下面所讨论的场的一些概念虽然是在所选用的坐标系下建立的,但都可以证明它们和坐标系的选取无关.

## 二、梯度场

在第十七章 §3 中我们已经介绍了梯度的概念, 它是由数量函数 $u(x,y,z)$ 所定义的向量函数

$$
\textbf {g r a d} u = \left(\frac {\partial u}{\partial x}, \frac {\partial u}{\partial y}, \frac {\partial u}{\partial z}\right) ,
$$

而且 $\operatorname{grad} u$ 的方向就是使 $\frac{\partial u}{\partial l}$ 达到最大值的方向, 它的大小就是 $u$ 在这个方向上的方向导数值. 因此我们可以定义数量场 $u$ 在点 $M$ 处的梯度 $\operatorname{grad} u$ 为这样的向量, 它的方向是在 $M$ 处最大的方向导数的方向, 而它的大小是在 $M$ 处最大方向导数值. 由于方向导

276

---

\* §4 场论初步 |||

数的定义与坐标系选取无关,因此梯度定义也是与坐标系选取无关的向量.由梯度给出的向量场,称为梯度场.

又因为数量场 $u(x,y,z)$ 的等值面 $u(x,y,z) = c$ 的法线方向为

$$
\left(\frac {\partial u}{\partial x}, \frac {\partial u}{\partial y}, \frac {\partial u}{\partial z}\right)  ,
$$

所以 grad u 的方向与等值面正交, 即等值面的法线方向.

引进符号向量

$$
\nabla = \left(\frac {\partial}{\partial x}, \frac {\partial}{\partial y}, \frac {\partial}{\partial z}\right).
$$

当把它作为运算符号来看待时①,梯度可写作

$$
\text {grad} u = \nabla u.
$$

关于梯度,有以下一些基本性质:

1. 若 $u, v$ 是数量函数, 则

$$
\nabla (u + v) = \nabla u + \nabla v.
$$

2. 若 $u, v$ 是数量函数, 则

$$
\nabla (u v) = u (\nabla v) + (\nabla u) v.
$$

特别地有

$$
\nabla u ^ {2} = 2 u (\nabla u).
$$

3. 若 $r = (x, y, z)$, $\varphi = \varphi(x, y, z)$, 则

$$
\mathrm{d} \varphi = \mathrm{d} \boldsymbol {r} \cdot \nabla \varphi .
$$

4. 若 $f = f(u)$, $u = u(x, y, z)$, 则

$$
\nabla f = f ^ {\prime} (u) \nabla u.
$$

5. 若  $f=f(u_{1}, u_{2}, \cdots, u_{m})$ ,  $u_{i}=u_{i}(x, y, z)$  ( $i=1,2,\cdots,m$ ), 则

$$
\nabla f = \sum_ {i = 1} ^ {m} \frac {\partial f}{\partial u _ {i}} \nabla u _ {i}.
$$

这些公式读者可利用定义来直接验证.

例1 设质量为 $m$ 的质点位于原点, 质量为 1 的质点位于 $M(x, y, z)$, 记 $OM = r = \sqrt{x^2 + y^2 + z^2}$, 求 $\frac{m}{r}$ 的梯度.

解

$$
\nabla \frac {m}{r} = - \frac {m}{r ^ {2}} \bigg (\frac {x}{r}, \frac {y}{r}, \frac {z}{r} \bigg).
$$

若以 $r_0$ 表示 $\overrightarrow{OM}$ 上的单位向量 $\left(\frac{x}{r},\frac{y}{r},\frac{z}{r}\right)$，则有

$$
\nabla \frac {m}{r} = - \frac {m}{r ^ {2}} \boldsymbol {r} _ {0}.
$$

它表示两质点间的引力,方向朝着原点,大小是与质量的乘积成比例,与两点间的距离的平方成反比.这说明了引力场是数量函数 $\frac{m}{r}$ 的梯度场.因此我们常称 $\frac{m}{r}$ 为引力势.☐

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">①  $\nabla$ 常称为哈密顿(Hamilton)算符,读作“Nabla”.</span></small>

277

---

第二十二章 曲面积分

## 三、散度场

设

$$
A (x, y, z) = (P (x, y, z), Q (x, y, z), R (x, y, z))
$$

为空间区域 $V$ 上的向量函数，对 $V$ 上每一点 $(x,y,z)$，定义数量函数

$$
D (x, y, z) = \frac {\partial P}{\partial x} + \frac {\partial Q}{\partial y} + \frac {\partial R}{\partial z},
$$

称它为向量函数 A 在  $(x, y, z)$  处的散度, 记作

$$
D (x, y, z) = \operatorname{div} A (x, y, z) ①.
$$

设 $n_0 = (\cos \alpha, \cos \beta, \cos \gamma)$ 为曲面的单位法向量，则 $\mathrm{d}S = n_0\mathrm{d}S$ 就称为曲面的面积元素向量.于是高斯公式可写成如下向量形式:

$$
\iiint_ {V} \mathrm{div} \boldsymbol {A} \mathrm{d} V = \oint_ {S} \boldsymbol {A} \cdot \mathrm{d} \boldsymbol {S}. \tag {1}
$$

在 $V$ 中任取一点 $M_0$ ，对(1)式中的三重积分应用中值定理，得

$$
\iiint_ {V} \mathrm{div} A \mathrm{d} V = \mathrm{div} A (M ^ {*}) \cdot \Delta V = \oiint_ {S} A \cdot \mathrm{d} S,
$$

其中 $M^{*}$ 为 $V$ 中某一点，于是有

$$
\mathrm{div}   A (  M ^ {*}  ) = \frac {\oint_ {S} \boldsymbol {A} \cdot \mathrm{d} \boldsymbol {S}}{\Delta V}.
$$

令 $V$ 收缩到点 $M_0$ （记成 $V\to M_0$ ），则 $M^{*}$ 也趋向点 $M_0$ ，因此

$$
\operatorname{div} \boldsymbol {A} (M _ {0}) = \lim _ {V \to M _ {0}} \frac {\oiint_ {S} \boldsymbol {A} \cdot \mathrm{d} S}{\Delta V}. \tag {2}
$$

这个等式可以看作是散度的另一种定义形式.(2)式右边的分子、分母都与坐标系的选取无关,因此它的极限也与坐标系选取无关,所以散度 div A 与坐标系选取无关.由向量场 A 的散度 divA 所构成的数量场,称为散度场.

散度的物理意义:联系本章§2中提到流速为A的不可压缩流体,经过封闭曲面S的流量是

$$
\oiint_ {S} \boldsymbol {A} \cdot \mathrm{d} \boldsymbol {S}.
$$

于是(2)式表明 $\operatorname{div} A(M_0)$ 是流量对体积 $V$ 的变化率, 并称它为 $A$ 在点 $M_0$ 的流量密度. 若 $\operatorname{div} A(M_0) > 0$, 说明在每一单位时间内有一定数量的流体流出这一点, 则称这一点为源. 相反, 若 $\operatorname{div} A(M_0) < 0$, 说明流体在这一点被吸收, 则称这点为汇. 若在向量场 $A$ 中每一点皆有

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① div 是 divergence(散度) 一词的缩写.</span></small>

278

---

\* § 4 场论初步 |||

$$
\operatorname{div} \boldsymbol {A} = 0,
$$

则称 A 为无源场.

由前面引进的算符 $\nabla$ ，向量场A的散度的向量形式是

$$
\operatorname{div} \boldsymbol {A} = \nabla \cdot \boldsymbol {A}.
$$

关于散度,容易由定义直接推得以下一些基本性质:

1. 若 u, v 是向量函数, 则

$$
\nabla \cdot (\boldsymbol {u} + \boldsymbol {v}) = \nabla \cdot \boldsymbol {u} + \nabla \cdot \boldsymbol {v}.
$$

2. 若  $\varphi$  是数量函数, F 是向量函数, 则

$$
\nabla \cdot (\varphi \boldsymbol {F}) = \varphi \nabla \cdot \boldsymbol {F} + \boldsymbol {F} \cdot \nabla \varphi .
$$

3. 若  $\varphi=\varphi(x,y,z)$  是一数量函数, 则

$$
\nabla \cdot \nabla \varphi = \frac {\partial^ {2} \varphi}{\partial x ^ {2}} + \frac {\partial^ {2} \varphi}{\partial y ^ {2}} + \frac {\partial^ {2} \varphi}{\partial z ^ {2}}.
$$

算符 $\nabla$ 的内积 $\nabla\cdot\nabla$ 常记作 $\Delta^{①}$ ，于是有

$$
\nabla \cdot \nabla \varphi = \Delta \varphi .
$$

例 2 求例 1 中引力场  $F = -\frac{m}{r^{2}} \left( \frac{x}{r}, \frac{y}{r}, \frac{z}{r} \right)$  所产生的散度场.

解 因为 $r^2 = x^2 + y^2 + z^2$，所以

$$
\boldsymbol {F} = - \frac {m}{(x ^ {2} + y ^ {2} + z ^ {2}) ^ {3 / 2}} (x, y, z),
$$

$$
\begin{array}{l} \nabla \cdot \boldsymbol {F} = - m \left[ \frac {\partial}{\partial x} \left(\frac {x}{\left(x ^ {2} + y ^ {2} + z ^ {2}\right) ^ {3 / 2}}\right) + \frac {\partial}{\partial y} \left(\frac {y}{\left(x ^ {2} + y ^ {2} + z ^ {2}\right) ^ {3 / 2}}\right) + \right. \\ \frac {\partial}{\partial z} \left(\frac {z}{\left(x ^ {2} + y ^ {2} + z ^ {2}\right) ^ {3 / 2}}\right) \Bigg ] \\ = 0. \\ \end{array}
$$

因此引力场 F 内每一点处的散度都为零(原点除外).

## 四、旋度场

设

$$
A (x, y, z) = (P (x, y, z), Q (x, y, z), R (x, y, z))
$$

为空间区域 V 上的向量函数. 对 V 上每一点  $(x, y, z)$ ，定义向量函数

$$
\boldsymbol {F} (x, y, z) = \left(\frac {\partial R}{\partial y} - \frac {\partial Q}{\partial z}, \frac {\partial P}{\partial z} - \frac {\partial R}{\partial x}, \frac {\partial Q}{\partial x} - \frac {\partial P}{\partial y}\right),
$$

称它为向量函数 A 在  $(x, y, z)$  处的旋度, 记作

①  $\Delta = \nabla \cdot \nabla = \frac{\partial^{2}}{\partial x^{2}} + \frac{\partial^{2}}{\partial y^{2}} + \frac{\partial^{2}}{\partial z^{2}}$  称为拉普拉斯算符.

279

---

第二十二章 曲面积分

$$
\boldsymbol {F} (x, y, z) = \mathbf {r o t} \boldsymbol {A} ^ {(1)}.
$$

设 $(\cos\alpha_{t},\cos\beta_{t},\cos\gamma_{t})$ 是曲线L的正向上的单位切线向量 $t_{0}$ 的方向余弦，向量 $\mathrm{d}s=(\cos\alpha_{t},\cos\beta_{t},\cos\gamma_{t})\mathrm{d}s=t_{0}\mathrm{d}l$ 称为弧长元素向量.于是斯托克斯公式可写成如下向量形式:

$$
\iint_ {S} \mathbf {r o t} \boldsymbol {A} \cdot \mathrm{d} \boldsymbol {S} = \oint_ {L} \boldsymbol {A} \cdot \mathrm{d} \boldsymbol {s}. \tag {3}
$$

为了说明旋度与坐标系的选取无关,我们在场 V 中任意取一点  $M_{0}$ , 通过  $M_{0}$  作平面  $\pi$  垂直于曲面 S 的法向量  $n_{0}$  (图 22-10), 且在  $\pi$  上围绕  $M_{0}$  作任一封闭曲线 L, 记 L 所围区域为 D, 则由 (3) 式有

![](../../raw/pages_0257-0288/images/page_287_image_5.jpg)

<details>
<summary>text_image</summary>

n₀
M₀
D
L
π
</details>

图22-10

$$
\iint_ {S} \mathbf {r o t} \boldsymbol {A} \cdot \mathrm{d} \boldsymbol {S} = \iint_ {S} \mathbf {r o t} \boldsymbol {A} \cdot \boldsymbol {n} _ {0} \mathrm{d} S = \oint_ {L} \boldsymbol {A} \cdot \mathrm{d} s. \tag {4}
$$

对左端曲面积分应用中值定理可得

$$
\iint_ {D} \mathbf {r o t}   A \cdot \boldsymbol {n} _ {0} \mathrm{d} S = (\mathbf {r o t}   A \cdot \boldsymbol {n} _ {0}) _ {M ^ {*}} \mu (  D  ) = \oint_ {L} A \cdot \mathrm{d} s,
$$

其中 $\mu(D)$ 为区域 $D$ 的面积, $M^{*}$ 为 $D$ 中的某一点. 因此

$$
(\mathbf {r o t}   A \cdot n _ {0}) _ {M ^ {*}} = \frac {\oint_ {L} A \cdot \mathrm{d} s}{\mu (D)}.
$$

现让 D 收缩到点  $M_{0}$  （记作  $D \rightarrow M_{0}$ ）时，于是  $M^{*}$  趋于  $M_{0}$ ，因此有

$$
(\mathbf {r o t} \boldsymbol {A} \cdot \boldsymbol {n} _ {0}) _ {M _ {0}} = \lim _ {D \to M _ {0}} \frac {\oint_ {L} \boldsymbol {A} \cdot \mathrm{d} s}{\mu (D)}. \tag {5}
$$

(5)式左边为 rot A 在法线方向上的投影,因此它也确定了 rot A 的本身,所以(5)也可以作为旋度的另一种定义形式.由于(5)式右边的极限与坐标系的选取无关,故 rot A 也与坐标系选取无关.

由向量函数 A 的旋度 rot A 所定义的向量场, 称为旋度场.

在流量问题中,我们称

$$
\oint_ {L} \boldsymbol {A} \cdot \mathrm{d} \boldsymbol {s}
$$

为沿闭曲线 L 的环流量, 它表示流速为 A 的不可压缩流体在单位时间内沿曲线 L 的流体总量, 反映了流体沿 L 时的旋转强弱程度. 当 rot A = 0 时, 沿任意封闭曲线的环流量为零, 即流体流动时不成旋涡, 这时称向量场 A 为无旋场.

公式(4)表明向量场在曲面边界线上的切线投影对弧长的曲线积分等于向量场的

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① rot 是 rotation(旋度)一词的缩写,有的书也用 curl 表示旋度,为便于记忆,rot A 可形式地写成</span></small>

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">$\mathbf{rot}A = \left| \begin{array}{ccc}i & j & k\\ \frac{\partial}{\partial x} & \frac{\partial}{\partial y} & \frac{\partial}{\partial z}\\ P & Q & R \end{array} \right|.$</span></small>

280

---

\* § 4 场论初步

旋度的法线投影在曲面上对面积的曲面积分. 它的物理意义可以说成是: 流体的速度场的旋度的法线投影在曲面上对面积的曲面积分等于流体在曲面边界上的环流量.

为了更好地认识旋度的物理意义及这一名称的来源,我们讨论刚体绕定轴旋转的问题.设一刚体以角速度  $\omega$  绕某轴旋转,则角速度向量  $\omega$  方向沿着旋转轴,其指向与旋转方向的关系符合右手法则,即右手拇指指向角速度  $\omega$  的方向,其他四指指向旋转方向.若取定旋转轴上一点 O 作为原点(图 22-11),刚体上任意一点 P 的线速度 v 可表示为

$$
\boldsymbol {v} = \boldsymbol {\omega} \times \boldsymbol {r},
$$

其中  $r=\overrightarrow{OP}$  是 P 的径向量. 设 P 的坐标为  $(x,y,z)$ ，便有  $\boldsymbol{r}=(x,y,z)$ ，又设  $\boldsymbol{\omega}=(\omega_{x},\omega_{y},\omega_{z})$ . 于是

![](../../raw/pages_0289-0320/images/page_288_image_5.jpg)

<details>
<summary>text_image</summary>

v
P
r
ω
O
</details>

图22-11

$$
\boldsymbol {v} = \left(\omega_ {y} z - \omega_ {z} y, \omega_ {z} x - \omega_ {x} z, \omega_ {x} y - \omega_ {y} x\right),
$$

所以 $\mathbf{rot}v = (2\omega_{x}, 2\omega_{y}, 2\omega_{z}) = 2\omega$

或  $\omega=\frac{1}{2}\mathrm{rot}v.$

这等式表明线速度向量 v 的旋度除去一个常数因子  $\frac{1}{2}$  外, 就是旋转的角速度向量  $\omega$ . 可见 v 的旋度与  $\omega$  成正比, 这也说明了旋度这个名称的来源.

应用算符 $\nabla$ 表示 $A$ 的旋度是

$$
\mathrm{rot} A = \nabla \times A.
$$

旋度有如下一些基本性质:

1. 若 u, v 是向量函数, 则

$$
\begin{array}{l} \nabla \times (\boldsymbol {u} + \boldsymbol {v}) = \nabla \times \boldsymbol {u} + \nabla \times \boldsymbol {v}, \\ \nabla (\boldsymbol {u} \cdot \boldsymbol {v}) = \boldsymbol {u} \times (\nabla \times \boldsymbol {v}) + \boldsymbol {v} \times (\nabla \times \boldsymbol {u}) + (\boldsymbol {u} \cdot \nabla) \boldsymbol {v} + (\boldsymbol {v} \cdot \nabla) \boldsymbol {u}, \\ \nabla \cdot (\boldsymbol {u} \times \boldsymbol {v}) = \boldsymbol {v} \cdot \nabla \times \boldsymbol {u} - \boldsymbol {u} \cdot \nabla \times \boldsymbol {v}, \\ \nabla \times (\boldsymbol {u} \times \boldsymbol {v}) = (\boldsymbol {v} \cdot \nabla) \boldsymbol {u} - (\boldsymbol {u} \cdot \nabla) \boldsymbol {v} + (\nabla \cdot \boldsymbol {v}) \boldsymbol {u} - (\nabla \cdot \boldsymbol {u}) \boldsymbol {v}. \\ \end{array}
$$

2. 若 $\varphi$ 是数量函数, $A$ 是向量函数, 则

$$
\nabla \times (\varphi \boldsymbol {A}) = \varphi (\nabla \times \boldsymbol {A}) + \nabla \varphi \times \boldsymbol {A}.
$$

3. 若  $\varphi$  是数量函数, A 是向量函数, 则

$$
\begin{array}{l} \nabla \cdot (\nabla \times \boldsymbol {A}) = 0, \\ \nabla \times \nabla \varphi = \mathbf {0}, \\ \nabla \times (\nabla \times \boldsymbol {A}) = \nabla (\nabla \cdot \boldsymbol {A}) - \nabla^ {2} \boldsymbol {A} = \nabla (\nabla \cdot \boldsymbol {A}) - \Delta \boldsymbol {A}. \\ \end{array}
$$

这些等式读者都可通过梯度、散度、旋度等定义来直接验证.

## 五、管量场与有势场

若一个向量场 A 的散度恒为零, 即 div A = 0, 我们曾称 A 为无源场. 从高斯公式知, 此时沿任何封闭曲面的曲面积分都等于零. 我们把场 A 称作管量场. 这是因为, 若在向量场 A 中作一向量管 (图 22-12), 即由向量线围成

![](../../raw/pages_0289-0320/images/page_288_image_23.jpg)

<details>
<summary>text_image</summary>

S₁
S₂
S₃
</details>

图22-12

281

---

第二十二章 曲面积分

的管状的曲面,用断面  $S_{1}, S_{2}$  截它,以  $S_{3}$  表示所截出的管的表面,我们就得到了由  $S_{1}, S_{2}, S_{3}$  所围成的封闭曲面 S.于是由(1)式得出

$$
\oiint_ {S} \boldsymbol {A} \cdot \mathrm{d} \boldsymbol {S} = \iint_ {S _ {1} \text {外侧}} \boldsymbol {A} \cdot \mathrm{d} \boldsymbol {S} + \iint_ {S _ {2} \text {外侧}} \boldsymbol {A} \cdot \mathrm{d} \boldsymbol {S} + \iint_ {S _ {3} \text {外侧}} \boldsymbol {A} \cdot \mathrm{d} \boldsymbol {S} = 0.
$$

而向量线与曲面 $S_{3}$ 的法线正交，所以

$$
\iint_ {S _ {3} \text {外侧}} \boldsymbol {A} \cdot \mathrm{d} \boldsymbol {S} = 0,
$$

即

$$
\begin{array}{l} \iint_ {S _ {1} \text {外侧}} \boldsymbol {A} \cdot \mathrm{d} \boldsymbol {S} + \iint_ {S _ {2} \text {外侧}} \boldsymbol {A} \cdot \mathrm{d} \boldsymbol {S} = 0, \\ \iint_ {S _ {1} \text {内侧}} \boldsymbol {A} \cdot \mathrm{d} \boldsymbol {S} = \iint_ {S _ {2} \text {外侧}} \boldsymbol {A} \cdot \mathrm{d} \boldsymbol {S}. \\ \end{array}
$$

这等式说明了流体通过向量管的任意断面的流量是相同的,所以我们把场 A 称为管量场. 如例 2, 由  $\frac{m}{r}$  的梯度  $\nabla\frac{m}{r}$  所成的引力场 F 是一个管量场.

若一个向量场 $A$ 的旋度恒为零, 即 $\operatorname{rot} A = 0$, 我们在前面称 $A$ 为无旋场. 从斯托克斯公式知, 这时在空间单连通区域内沿任何封闭曲线的曲线积分都等于零, 这种场也称为有势场. 这是因为当 $\operatorname{rot} A = 0$ 时, 由定理22.7推得此时空间曲线积分与路线无关, 且存在某函数 $u(x, y, z)$, 使得

$$
\mathrm{d} u = P \mathrm{d} x + Q \mathrm{d} y + R \mathrm{d} z,
$$

即

$$
\text {grad} u = (P, Q, R).
$$

通常称 $u$ 为势函数. 因此, 若某向量场 $\pmb{A}$ 的旋度为零, 则必存在某个势函数 $u$, 使得 $\operatorname{grad} u = A$. 这也是一个向量场是某个数量场的梯度场的充要条件. 在例1中, 引力势 $u = \frac{m}{r}$ 就是势函数. 所以

$$
\nabla u = \boldsymbol {F} = - \frac {m}{r ^ {2}} \Big (\frac {x}{r}, \frac {y}{r}, \frac {z}{r} \Big)  .
$$

因为 $\nabla \times \nabla u = 0$ 恒成立，所以 $\nabla \times F = 0.$ 它也是引力场 $F$ 是有势场的充要条件.

若一个向量场 A 既是管量场, 又是有势场, 则称这个向量场为调和场. 上述例 2 中讲到的引力场 F 就是调和场. 若 A 是一个调和场, 必有

$$
\nabla \cdot \boldsymbol {A} = 0, \qquad \nabla u = \boldsymbol {A}.
$$

显然

$$
\nabla \cdot \nabla u = \nabla^ {2} u = \Delta u = 0,
$$

即必有势函数 $u$ 满足

$$
\frac {\partial^ {2} u}{\partial x ^ {2}} + \frac {\partial^ {2} u}{\partial y ^ {2}} + \frac {\partial^ {2} u}{\partial z ^ {2}} = 0.
$$

这时称函数 u 为调和函数.

282

---

第二十二章总练习题

## 习题 22.4

1. 若 $r = \sqrt{x^2 + y^2 + z^2}$, 计算 $\nabla r, \nabla r^2, \nabla \frac{1}{r}, \nabla f(r), \nabla r^n (n \geqslant 3)$.

2. 求 $u = x^{2} + 2y^{2} + 3z^{2} + 2xy - 4x + 2y - 4z$ 在点 $O(0,0,0), A(1,1,1), B(-1,-1,-1)$ 处的梯度，并求梯度为零之点.

3. 证明本节第二段关于梯度的一些基本性质1—5.

4. 计算下列向量场 A 的散度与旋度:

(1) $A = (y^2 + z^2, z^2 + x^2, x^2 + y^2)$; (2) $A = (x^2yz, xy^2z, xyz^2)$;
(3)  $A=\left(\frac{x}{yz},\frac{y}{zx},\frac{z}{xy}\right)$ .

5. 证明本节第三段关于散度的一些基本性质 1—3.

6. 证明本节第四段关于旋度的一些基本性质1—3（可应用算符 $\nabla$ 推演）.

7. 证明:场 $A = (yz(2x + y + z),xz(x + 2y + z),xy(x + y + 2z))$ 是有势场并求其势函数.

8. 若流体流速 $A = (x^2, y^2, z^2)$，求单位时间内穿过 $\frac{1}{8}$ 球面 $x^2 + y^2 + z^2 = 1, x > 0, y > 0, z > 0$ 的流量.

9. 设流速  $A = (-y, x, c)$  (c 为常数)，求环流量:

(1) 沿圆周  $x^{2} + y^{2} = 1, z = 0$ ; (2) 沿圆周  $(x - 2)^{2} + y^{2} = 1, z = 0$ .

## 第二十二章总练习题

1. 设  $P = x^{2} + 5\lambda y + 3yz, Q = 5x + 3\lambda xz - 2, R = (\lambda + 2)xy - 4z.$

(1) 计算  $\int_{L} P \, dx + Q \, dy + R \, dz$ ，其中 L 为螺旋线  $x = a \cos t, y = a \sin t, z = ct (0 \leqslant t \leqslant 2\pi)$ ;
(2) 设  $\boldsymbol{A} = (P, Q, R)$ ，求 rot A;
(3) 问在什么条件下 A 为有势场？并求势函数.

2. 证明:若 $\Delta u = \frac{\partial^2 u}{\partial x^2} + \frac{\partial^2 u}{\partial y^2} + \frac{\partial^2 u}{\partial z^2}$，$S$ 为包围区域 $V$ 的曲面的外侧，则

(1)  $\iiint_{V}\Delta u\,dx\,dy\,dz = \iint_{S}\frac{\partial u}{\partial n}\,dS;$
(2) $\iint_{S} u \frac{\partial u}{\partial \boldsymbol{n}} \mathrm{d} S = \iiint_{V} \nabla \cdot \nabla u \, \mathrm{d} x \, \mathrm{d} y \, \mathrm{d} z + \iiint_{V} u \Delta u \, \mathrm{d} x \, \mathrm{d} y \, \mathrm{d} z,$

其中 u 在区域 V 及其界面 S 上有二阶连续偏导数,  $\frac{\partial u}{\partial n}$  为沿曲面 S 外法线方向的方向导数.

3. 设 $S$ 为光滑闭曲面, $V$ 为 $S$ 所围的区域. 函数 $u(x,y,z)$ 在 $V$ 与 $S$ 上具有二阶连续偏导数, 函数 $\omega(x,y,z)$ 偏导连续. 证明:

(1)  $\iiint_{V}\omega\frac{\partial u}{\partial x}dx\,dydz=\oiint_{S}u\omega\,dydz-\iiint_{V}u\frac{\partial\omega}{\partial x}\,dx\,dydz;$
(2)  $\iiint_{V}\omega\Delta u\,dx\,dy\,dz = \oint\limits_{S}\omega\frac{\partial u}{\partial n}\,dS - \iiint_{V}\nabla u \cdot \nabla\omega\,dx\,dy\,dz.$

4. 设 $A = \frac{r}{|r|^3}$, $S$ 为一封闭曲面, $r = (x, y, z)$. 证明当原点在曲面 $S$ 的外、上、内时, 分别有

283

---

第二十二章 曲面积分

$$
\oiint_ {S} \boldsymbol {A} \cdot \mathrm{d} \boldsymbol {S} = 0, 2 \pi , 4 \pi .
$$

5. 计算 $I = \iint_{S} xz \, \mathrm{d}y \, \mathrm{d}z + yx \, \mathrm{d}z \, \mathrm{d}x + zy \, \mathrm{d}x \, \mathrm{d}y$，其中 $S$ 是柱面 $x^2 + y^2 = 1$ 在 $-1 \leqslant z \leqslant 1$ 和 $x \geqslant 0$ 的部分。曲面侧的法向与 $x$ 轴正向成锐角。

6. 证明公式:

$$
\begin{array}{l} \iint_ {D} f (m \sin \varphi \cos \theta + n \sin \varphi \sin \theta + p \cos \varphi) \sin \varphi \mathrm{d} \theta \mathrm{d} \varphi \\ = 2 \pi \int_ {- 1} ^ {1} f (u \sqrt {m ^ {2} + n ^ {2} + p ^ {2}}) \mathrm{d} u, \\ \end{array}
$$

这里 $D = \{(\theta, \varphi) | 0 \leqslant \theta \leqslant 2\pi, 0 \leqslant \varphi \leqslant \pi\}, m^2 + n^2 + p^2 > 0, f(t)$ 在 $|t| < \sqrt{m^2 + n^2 + p^2}$ 时为连续函数.

![](../../raw/pages_0289-0320/images/page_291_image_6.jpg)

## 第二十二章综合自测题

284
