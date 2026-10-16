例如,方程

$$
3 x - 4 y + z - 9 = 0
$$

表示一个平面, $n=(3,-4,1)$ 是这平面的一个法向量.

对于一些特殊的三元一次方程,应该熟悉它们的图形的特点.

当 D=0 时, 方程(3-4)成为  $Ax+By+Cz=0$ , 它表示一个通过原点的平面.

当 $A = 0$ 时，方程(3-4)成为 $By + Cz + D = 0$ ，法向量 $\pmb {n} = (0,B,C)$ 垂直于 $x$ 轴，方程表示一个平行于(或包含) $x$ 轴的平面.

同样,方程 $Ax+Cz+D=0$ 和 $Ax+By+D=0$ 分别表示一个平行于(或包含)y轴和z轴的平面.

当 $A = B = 0$ 时，方程(3-4)成为 $Cz + D = 0$ 或 $z = -\frac{D}{C}$，法向量 $\pmb{n} = (0,0,C)$ 同时垂直于 $x$ 轴和 $y$ 轴，方程表示一个平行于（或重合于）$xOy$ 面的平面.

同样,方程  $Ax+D=0$  和  $By+D=0$  分别表示一个平行于(或重合于) yOz 面和 zOx 面的平面.

例 3 求通过 x 轴和点  $(4, -3, -1)$  的平面的方程.

解 由于平面通过 x 轴, 从而它的法向量垂直于 x 轴, 于是法向量在 x 轴上的投影为零, 即 A=0; 又由平面通过 x 轴, 它必通过原点, 于是 D=0. 因此可设这平面的方程为

$$
B y + C z = 0.
$$

又因这平面通过点 $(4,-3,-1)$ ，所以有

$$
- 3 B - C = 0, \quad \text {或} \quad C = - 3 B.
$$

以此代入所设方程并除以  $B(B \neq 0)$ ，便得所求的平面方程为

$$
y - 3 z = 0.
$$

例 4 设一平面与 x 轴、y 轴和 z 轴的交点依次为  $P(a,0,0)$ ,  $Q(0,b,0)$ ,  $R(0,0,c)$  三点（图 8-32），求这平面的方程（其中  $a \neq 0, b \neq 0, c \neq 0$ ）.

解 设所求平面的方程为

$$
A x + B y + C z + D = 0.
$$

因为 $P(a,0,0), Q(0,b,0)$ 和 $R(0,0,c)$ 三点都在这平面上，所以点 $P, Q$ 和 $R$ 的坐标都满足方程(3-4)，即有

$$
\left\{ \begin{array}{l} a A + D = 0, \\ b B + D = 0, \\ c C + D = 0, \end{array} \right.
$$

解得

![](images/page_32_image_23.jpg)

<details>
<summary>text_image</summary>

z
R
O
Q
y
P
x
</details>

图8-32

$$
A = - \frac {D}{a}, \quad B = - \frac {D}{b}, \quad C = - \frac {D}{c}.
$$

以此代入(3-4)并除以 $D(D \neq 0)$, 便得所求的平面方程为

$$
\frac {x}{a} + \frac {y}{b} + \frac {z}{c} = 1. \tag {3-7}
$$

方程(3-7)叫做平面的截距式方程,而a,b和c依次叫做平面在x轴、y轴和z轴上的截距.

## 四、两平面的夹角

两平面的法向量的夹角(通常指锐角或直角)称为两平面的夹角.

设平面 $\Pi_1$ 和 $\Pi_2$ 的法向量依次为 $n_1 = (A_1, B_1, C_1)$ 和 $n_2 = (A_2, B_2, C_2)$，则平面 $\Pi_1$ 和 $\Pi_2$ 的夹角 $\theta$（图8-33）应是 $(\widehat{n_1, n_2})$ 和 $(-n_1, n_2) = \pi - (\widehat{n_1, n_2})$ 两者中的锐角或直角，因此，$\cos \theta = |\cos (\widehat{n_1, n_2})|$. 按两向量夹角余弦的坐标表示式，平面 $\Pi_1$ 和平面 $\Pi_2$ 的夹角 $\theta$ 可由

$$
\cos \theta = \frac {\mid A _ {1} A _ {2} + B _ {1} B _ {2} + C _ {1} C _ {2} \mid}{\sqrt {A _ {1} ^ {2} + B _ {1} ^ {2} + C _ {1} ^ {2}} \sqrt {A _ {2} ^ {2} + B _ {2} ^ {2} + C _ {2} ^ {2}}} \tag {3-8}
$$

![](images/page_33_image_9.jpg)

<details>
<summary>text_image</summary>

n₁
θ
n₂
Π₂
θ
Π₁
</details>

图8-33

来确定.

从两向量垂直、平行的充分必要条件立即推得下列结论:

两平面  $\Pi_{1}$  和  $\Pi_{2}$  互相垂直相当于  $A_{1}A_{2}+B_{1}B_{2}+C_{1}C_{2}=0$ ;

两平面 $\Pi_1$ 和 $\Pi_2$ 互相平行或重合相当于 $\frac{A_1}{A_2} = \frac{B_1}{B_2} = \frac{C_1}{C_2}$.

例 5 求两平面  $x-y+2z-6=0$  和  $2x+y+z-5=0$  的夹角.

解 由公式(3-8)有

$$
\cos \theta = \frac {\mid 1 \times 2 + (- 1) \times 1 + 2 \times 1 \mid}{\sqrt {1 ^ {2} + (- 1) ^ {2} + 2 ^ {2}} \sqrt {2 ^ {2} + 1 ^ {2} + 1 ^ {2}}} = \frac {1}{2},
$$

因此,所求夹角  $\theta=\frac{\pi}{3}$ .

例6 一平面通过两点 $M_{1}(1,1,1)$ 和 $M_{2}(0,1,-1)$ 且垂直于平面 $x + y + z = 0$，求它的方程.

解 设所求平面的一个法向量为

$$
n = (A, B, C).
$$

因 $\overrightarrow{M_1M_2} = (-1,0, - 2)$ 在所求平面上，它必与 $n$ 垂直，所以有

$$
- A - 2 C = 0. \tag {3-9}
$$

又因所求的平面垂直于已知平面 $x + y + z = 0$ ，所以又有

$$
A + B + C = 0. \tag {3-10}
$$

由式(3-9)、式(3-10)得到

$$
A = - 2 C, \quad B = C.
$$

由平面的点法式方程可知,所求平面方程为

$$
A (x - 1) + B (y - 1) + C (z - 1) = 0.
$$

将 A = -2C 及 B = C 代入上式, 并约去 C ( $C \neq 0$ ), 便得

$$
- 2 (x - 1) + (y - 1) + (z - 1) = 0,
$$

即

$$
2 x - y - z = 0.
$$

这就是所求的平面方程.

例 7 设  $P_{0}(x_{0}, y_{0}, z_{0})$  是平面  $Ax + By + Cz + D = 0$  外一点，求  $P_{0}$  到这平面的距离（图 8-34）.

解 在平面上任取一点 $P_{1}(x_{1},y_{1},z_{1})$ ，并作一法向量 $\pmb{n}$ ，由图8-34，并考虑到 $\overrightarrow{P_1P_0}$ 与 $\pmb{n}$ 的夹角 $\theta$ 也可能是钝角，得所求的距离

![](images/page_34_image_15.jpg)

<details>
<summary>text_image</summary>

n
θ
P₀
P₁
N
</details>

图8-34

$$
d = | \overrightarrow {P _ {1} P _ {0}} | | \cos \theta | = \frac {| \overrightarrow {P _ {1} P _ {0}} \cdot n |}{| n |}.
$$

而

$$
\boldsymbol {n} = (A, B, C), \quad \overrightarrow {P _ {1} P _ {0}} = (x _ {0} - x _ {1}, y _ {0} - y _ {1}, z _ {0} - z _ {1}),
$$

得

$$
\frac {\overrightarrow {P _ {1} P _ {0}} \cdot \boldsymbol {n}}{| \boldsymbol {n} |} = \frac {A (x _ {0} - x _ {1}) + B (y _ {0} - y _ {1}) + C (z _ {0} - z _ {1})}{\sqrt {A ^ {2} + B ^ {2} + C ^ {2}}} = \frac {A x _ {0} + B y _ {0} + C z _ {0} - (A x _ {1} + B y _ {1} + C z _ {1})}{\sqrt {A ^ {2} + B ^ {2} + C ^ {2}}}.
$$

因为 $Ax_{1} + By_{1} + Cz_{1} + D = 0$ ，所以

$$
\frac {\overrightarrow {P _ {1} P _ {0}} \cdot \boldsymbol {n}}{| \boldsymbol {n} |} = \frac {A x _ {0} + B y _ {0} + C z _ {0} + D}{\sqrt {A ^ {2} + B ^ {2} + C ^ {2}}}.
$$

由此得点 $P_0(x_0, y_0, z_0)$ 到平面 $Ax + By + Cz + D = 0$ 的距离公式

$$
d = \frac {\mid A x _ {0} + B y _ {0} + C z _ {0} + D \mid}{\sqrt {A ^ {2} + B ^ {2} + C ^ {2}}}. \tag {3-11}
$$

例如,求点 $(2,1,1)$ 到平面 $x+y-z+1=0$ 的距离,可利用公式 $(3-11)$ ,便得

$$
d = \frac {\mid 1 \times 2 + 1 \times 1 - 1 \times 1 + 1 \mid}{\sqrt {1 ^ {2} + 1 ^ {2} + (- 1) ^ {2}}} = \frac {3}{\sqrt {3}} = \sqrt {3}.
$$

## 习题8-3

1. 求过点 $(3,0,-1)$ 且与平面 $3x - 7y + 5z - 12 = 0$ 平行的平面方程.
2. 求过点 $M_0(2,9,-6)$ 且与连接坐标原点及点 $M_0$ 的线段 $OM_0$ 垂直的平面方程.
3. 求过 $M_{1}(1,1,-1), M_{2}(-2,-2,2)$ 和 $M_{3}(1,-1,2)$ 三点的平面方程.
4. 指出下列各平面的特殊位置,并画出各平面:

(1) x=0;

(2) 3y-1=0;

(3) 2x-3y-6=0;

(4) $x - \sqrt{3} y = 0$;

(5) $y + z = 1$;

(6) x-2z=0;

(7) $6x+5y-z=0.$

5. 求平面  $2x-2y+z+5=0$  与各坐标面的夹角的余弦.
6. 设一平面过点 $M_0(1,2,-1)$ 且垂直于平面 $3x - 4y + z + 16 = 0$ 和 $4x - z + 6 = 0$, 试求这平面方程.
7. 求三平面  $x+3y+z=1,2x-y-z=0,-x+2y+2z=3$  的交点.
8. 分别按下列条件求平面方程:

(1) 平行于 zOx 面且经过点  $(2, -5, 3)$ ;
(2) 通过 z 轴和点  $(-3,1,-2)$ ;
(3) 平行于 x 轴且经过两点  $(4,0,-2)$  和  $(5,1,7)$ .

9. 求点(1,2,1)到平面  $x+2y+2z-10=0$  的距离.

## 第四节 空间直线及其方程

## 一、空间直线的一般方程

空间直线 $L$ 可以看做是两个平面 $\Pi_{1}$ 和 $\Pi_{2}$ 的交线（图8-35).如果两个相交的平面 $\Pi_{1}$ 和 $\Pi_{2}$ 的方程分别为 $A_{1}x + B_{1}y + C_{1}z + D_{1} = 0$ 和 $A_{2}x + B_{2}y + C_{2}z + D_{2} = 0$ ，那么直线 $L$ 上的任一点的坐标应同时满足这两个平面的方程，即应满足方程组

$$
\left\{ \begin{array}{l} A _ {1} x + B _ {1} y + C _ {1} z + D _ {1} = 0, \\ A _ {2} x + B _ {2} y + C _ {2} z + D _ {2} = 0. \end{array} \right. \tag {4-1}
$$

![](images/page_35_image_28.jpg)

<details>
<summary>text_image</summary>

z
Π₂
L
Π₁
O
y
x
</details>

图8-35

反过来,如果点 M 不在直线 L 上,那么它不可能同时在平面  $\Pi_{1}$  和  $\Pi_{2}$  上,所以它的坐标不满足方程组(4-1).因此,直线 L 可以用方程组(4-1)来表示.方程组(4-1)叫做空间直线的一般方程.

通过空间一直线 $L$ 的平面有无限多个, 只要在这无限多个平面中任意选取两个,

把它们的方程联立起来,所得的方程组就表示空间直线 L.

## 二、空间直线的对称式方程与参数方程

如果一个非零向量平行于一条已知直线,那么这个向量就叫做这条直线的方向向量.

由于过空间一点可作而且只能作一条直线平行于一已知直线,所以当直线 L 上一点  $M_{0}(x_{0},y_{0},z_{0})$  和它的一方向向量  $s=(m,n,p)$  为已知时,直线 L 的位置就完全确定了.下面我们来建立这条直线的方程.

设点 $M(x,y,z)$ 是直线 $L$ 上的任一点，则向量 $\overrightarrow{M_0M}$ 与 $L$ 的方向向量 $s$ 平行（图8-36).所以两向量的对应坐标成比例，由于 $\overrightarrow{M_0M} = (x - x_0,y - y_0,z - z_0),s = (m,n,$ $p)$ ，从而有

![](images/page_36_image_6.jpg)

<details>
<summary>text_image</summary>

z
s
M₀ M L
O y
x
</details>

图8-36

$$
\frac {x - x _ {0}}{m} = \frac {y - y _ {0}}{n} = \frac {z - z _ {0}}{p}. \tag {4-2}
$$

反过来,如果点 M 不在直线 L 上,那么由于  $\overrightarrow{M_{0}M}$  与 s 不平行,这两向量的对应坐标就不成比例.因此方程组(4-2)就是直线 L 的方程,叫做直线的对称式方程或点向式方程.

直线的任一方向向量 s 的坐标 m, n 和 p 叫做这条直线的一组方向数，而向量 s 的方向余弦叫做该直线的方向余弦.

由直线的对称式方程容易导出直线的参数方程.如设

$$
\frac {x - x _ {0}}{m} = \frac {y - y _ {0}}{n} = \frac {z - z _ {0}}{p} = t,
$$

则

$$
\left\{ \begin{array}{l} x = x _ {0} + m t, \\ y = y _ {0} + n t, \\ z = z _ {0} + p t. \end{array} \right. \tag {4-3}
$$

① 当 $m, n$ 和 $p$ 中有一个为零，例如 $m = 0$ ，而 $n$ 与 $p \neq 0$ 时，这个方程组应理解为

$$
\left\{ \begin{array}{l} x - x _ {0} = 0, \\ \frac {y - y _ {0}}{n} = \frac {z - z _ {0}}{p}; \end{array} \right.
$$

当 $m, n$ 和 $p$ 中有两个为零，例如 $m = n = 0$ ，而 $p \neq 0$ 时，这个方程组应理解为

$$
\left\{ \begin{array}{l} x - x _ {0} = 0, \\ y - y _ {0} = 0. \end{array} \right.
$$

方程组(4-3)就是直线的参数方程.

例1 用对称式方程及参数方程表示直线

$$
\left\{ \begin{array}{l} x + y + z + 1 = 0, \\ 2 x - y + 3 z + 4 = 0. \end{array} \right. \tag {4-4}
$$

解 先找出这条直线上的一点 $(x_0, y_0, z_0)$. 例如, 可以取 $x_0 = 1$, 代入方程组 (4-4), 得

$$
\left\{ \begin{array}{l} y _ {0} + z _ {0} = - 2, \\ y _ {0} - 3 z _ {0} = 6. \end{array} \right.
$$

解这个二元一次方程组, 得

$$
y _ {0} = 0, \quad z _ {0} = - 2,
$$

即 $(1,0,-2)$ 是这条直线上的一点.

下面再找出这条直线的方向向量 $s$. 因为两平面的交线与这两平面的法向量 $\pmb{n}_{1} = (1,1,1), \pmb{n}_{2} = (2, -1,3)$ 都垂直，所以可取

$$
s = \boldsymbol {n} _ {1} \times \boldsymbol {n} _ {2} = \left| \begin{array}{c c c} i & j & k \\ 1 & 1 & 1 \\ 2 & - 1 & 3 \end{array} \right| = 4 i - j - 3 k.
$$

因此,所给直线的对称式方程为

$$
\frac {x - 1}{4} = \frac {y}{- 1} = \frac {z + 2}{- 3}.
$$

令 $\frac{x-1}{4}=\frac{y}{-1}=\frac{z+2}{-3}=t$ ，得所给直线的参数方程为

$$
\left\{ \begin{array}{l} x = 1 + 4 t, \\ y = - t, \\ z = - 2 - 3 t. \end{array} \right.
$$

## 三、两直线的夹角

两直线的方向向量的夹角(通常指锐角或直角)叫做两直线的夹角.

设直线 $L_{1}$ 和 $L_{2}$ 的方向向量依次为 $s_1 = (m_1, n_1, p_1)$ 和 $s_2 = (m_2, n_2, p_2)$，则 $L_{1}$ 和 $L_{2}$ 的夹角 $\varphi$ 应是 $(\widehat{s_1, s_2})$ 和 $(- \widehat{s_1, s_2}) = \pi - (\widehat{s_1, s_2})$ 两者中的锐角或直角，因此 $\cos \varphi = |\cos (\widehat{s_1, s_2})|$. 按两向量的夹角的余弦公式，直线 $L_{1}$ 和直线 $L_{2}$ 的夹角 $\varphi$ 可由

$$
\cos \varphi = \frac {\mid m _ {1} m _ {2} + n _ {1} n _ {2} + p _ {1} p _ {2} \mid}{\sqrt {m _ {1} ^ {2} + n _ {1} ^ {2} + p _ {1} ^ {2}} \sqrt {m _ {2} ^ {2} + n _ {2} ^ {2} + p _ {2} ^ {2}}} \tag {4-5}
$$

来确定.

从两向量垂直、平行的充分必要条件立即推得下列结论:

两直线  $L_{1}$  和  $L_{2}$  互相垂直相当于  $m_{1}m_{2}+n_{1}n_{2}+p_{1}p_{2}=0$ ;

两直线  $L_{1}$  和  $L_{2}$  互相平行或重合相当于  $\frac{m_{1}}{m_{2}} = \frac{n_{1}}{n_{2}} = \frac{p_{1}}{p_{2}}$ .

例 2 求直线  $L_{1}:\frac{x-1}{1}=\frac{y}{-4}=\frac{z+3}{1}$  和  $L_{2}:\frac{x}{2}=\frac{y+2}{-2}=\frac{z}{-1}$  的夹角.

解 直线 $L_{1}$ 的方向向量为 $s_1 = (1, -4, 1)$, 直线 $L_{2}$ 的方向向量为 $s_2 = (2, -2, -1)$. 设直线 $L_{1}$ 和 $L_{2}$ 的夹角为 $\varphi$, 则由公式(4-5)有

$$
\cos \varphi = \frac {\mid 1 \times 2 + (- 4) \times (- 2) + 1 \times (- 1) \mid}{\sqrt {1 ^ {2} + (- 4) ^ {2} + 1 ^ {2}} \sqrt {2 ^ {2} + (- 2) ^ {2} + (- 1) ^ {2}}} = \frac {1}{\sqrt {2}},
$$

所以

$$
\varphi = \frac {\pi}{4}.
$$

## 四、直线与平面的夹角

当直线与平面不垂直时,直线和它在平面上的投影直线的夹角 $\varphi\left(0\leqslant\varphi<\frac{\pi}{2}\right)$ 称为直线与平面的夹角(图8-37),当直线与平面垂直时,规定直线与平面的夹角为 $\frac{\pi}{2}$ .

![](images/page_38_image_11.jpg)

<details>
<summary>text_image</summary>

Geometric diagram showing a plane intersected by two lines with angle φ marked at the intersection point.
</details>

图8-37

设直线的方向向量为 $s = (m, n, p)$，平面的法向量为 $n = (A, B, C)$，直线与平面的夹角为 $\varphi$，那么 $\varphi = \left|\frac{\pi}{2} - (\widehat{s, n})\right|$，因此 $\sin \varphi = |\cos (\widehat{s, n})|$。按两向量夹角余弦的坐标表示式，有

$$
\sin \varphi = \frac {\mid A m + B n + C p \mid}{\sqrt {A ^ {2} + B ^ {2} + C ^ {2}} \sqrt {m ^ {2} + n ^ {2} + p ^ {2}}} . \tag {4-6}
$$

因为直线与平面垂直相当于直线的方向向量与平面的法向量平行,所以,直线与平面垂直相当于

$$
\frac {A}{m} = \frac {B}{n} = \frac {C}{p}. \tag {4-7}
$$

因为直线与平面平行或直线在平面上相当于直线的方向向量与平面的法向量垂直,所以,直线与平面平行或直线在平面上相当于

$$
A m + B n + C p = 0. \tag {4-8}
$$

例3 求过点 $(1, -2, 4)$ 且与平面 $2x - 3y + z - 4 = 0$ 垂直的直线的方程.

解 因为所求直线垂直于已知平面,所以可以取已知平面的法向量 $(2,-3,1)$ 作为所求直线的方向向量.由此可得所求直线的方程为

$$
\frac {x - 1}{2} = \frac {y + 2}{- 3} = \frac {z - 4}{1}.
$$

## 五、杂例

例 4 求与两平面 x-4z=3 和 2x-y-5z=1 的交线平行且过点  $(-3,2,5)$  的直线的方程.

解法一 因为所求直线与两平面的交线平行,也就是直线的方向向量 s 一定同时与两平面的法向量  $n_{1}, n_{2}$  垂直,所以可以取

$$
s = \boldsymbol {n} _ {1} \times \boldsymbol {n} _ {2} = \left| \begin{array}{c c c} i & j & k \\ 1 & 0 & - 4 \\ 2 & - 1 & - 5 \end{array} \right| = - (4 i + 3 j + k),
$$

因此所求直线的方程为

$$
\frac {x + 3}{4} = \frac {y - 2}{3} = \frac {z - 5}{1}.
$$

解法二 过点 $(-3,2,5)$ 且与平面x-4z=3平行的平面的方程为

$$
x - 4 z = - 2 3,
$$

过点 $(-3,2,5)$ 且与平面2x-y-5z=1平行的平面的方程为

$$
2 x - y - 5 z = - 3 3,
$$

所求直线为上述两平面的交线,故其方程为

$$
\left\{ \begin{array}{l} x - 4 z = - 2 3, \\ 2 x - y - 5 z = - 3 3. \end{array} \right.
$$

例 5 求直线 $\frac{x-2}{1}=\frac{y-3}{1}=\frac{z-4}{2}$ 与平面 $2x+y+z-6=0$ 的交点.

解 所给直线的参数方程为

$$
x = 2 + t, \quad y = 3 + t, \quad z = 4 + 2 t,
$$

代入平面方程中,得

$$
2 (2 + t) + (3 + t) + (4 + 2 t) - 6 = 0.
$$

解以上方程, 得 t = -1. 把求得的 t 值代入直线的参数方程中, 即得所求交点的坐标为

$$
x = 1, \quad y = 2, \quad z = 2.
$$

例6 求过点(2,1,3)且与直线 $\frac{x + 1}{3} = \frac{y - 1}{2} = \frac{z}{-1}$ 垂直相交的直线的方程.

解 先作一平面过点(2,1,3)且垂直于已知直线,那么这平面的方程应为

$$
3 (x - 2) + 2 (y - 1) - (z - 3) = 0. \tag {4-9}
$$

再求已知直线与这平面的交点.已知直线的参数方程为

$$
x = - 1 + 3 t, \quad y = 1 + 2 t, \quad z = - t. \tag {4-10}
$$

把(4-10)代入(4-9)中,求得 $t=\frac{3}{7}$ ,从而求得交点为 $\left(\frac{2}{7},\frac{13}{7},-\frac{3}{7}\right)$ .

以点(2,1,3)为起点,点 $\left(\frac{2}{7},\frac{13}{7},-\frac{3}{7}\right)$ 为终点的向量

$$
\left(\frac {2}{7} - 2, \frac {1 3}{7} - 1, - \frac {3}{7} - 3\right) = - \frac {6}{7} (2, - 1, 4)
$$

是所求直线的一个方向向量,故所求直线的方程为

$$
\frac {x - 2}{2} = \frac {y - 1}{- 1} = \frac {z - 3}{4}.
$$

有时用平面束的方程解题比较方便,现在我们来介绍它的方程.

设直线 $L$ 由方程组

$$
\left\{ \begin{array}{l l} A _ {1} x + B _ {1} y + C _ {1} z + D _ {1} = 0, & (4 - 1 1) \\ A _ {2} x + B _ {2} y + C _ {2} z + D _ {2} = 0 & (4 - 1 2) \end{array} \right.
$$

所确定,其中系数 $A_{1},B_{1},C_{1}$ 与 $A_{2},B_{2},C_{2}$ 不成比例.我们建立三元一次方程

$$
A _ {1} x + B _ {1} y + C _ {1} z + D _ {1} + \lambda (A _ {2} x + B _ {2} y + C _ {2} z + D _ {2}) = 0, \tag {4-13}
$$

其中  $\lambda$  为任意常数. 因为  $A_{1}, B_{1}, C_{1}$  与  $A_{2}, B_{2}, C_{2}$  不成比例, 所以对于任何一个  $\lambda$  值, 方程(4-13) 的系数:  $A_{1} + \lambda A_{2}, B_{1} + \lambda B_{2}, C_{1} + \lambda C_{2}$  不全为零, 从而方程(4-13) 表示一个平面, 若一点在直线 L 上, 则点的坐标必同时满足方程(4-11) 和(4-12), 因而也满足方程(4-13), 故方程(4-13) 表示通过直线 L 的平面, 且对应于不同的  $\lambda$  值, 方程(4-13) 表示通过直线 L 的不同的平面. 反之, 通过直线 L 的任何平面 (除平面(4-12) 外) 都包含在方程(4-13) 所表示的一族平面内. 通过定直线的所有平面的全体称为平面束, 而方程(4-13) 就作为通过直线 L 的平面束的方程 (实际上, 方程(4-13) 表示缺少平面(4-12) 的平面束).

例7 求直线 $\begin{cases} x + y - z - 1 = 0, \\ x - y + z + 1 = 0 \end{cases}$ 在平面 $x + y + z = 0$ 上的投影直线的方程.

解 过直线 $\left\{\begin{aligned}x+y-z-1&=0,\\ x-y+z+1&=0\end{aligned}\right.$ 的平面束的方程为

$$
(x + y - z - 1) + \lambda (x - y + z + 1) = 0,
$$

即

$$
(1 + \lambda) x + (1 - \lambda) y + (- 1 + \lambda) z + (- 1 + \lambda) = 0, \tag {4-14}
$$

其中 $\lambda$ 为待定常数.这平面与平面 $x + y + z = 0$ 垂直的条件是

$$
(1 + \lambda) \cdot 1 + (1 - \lambda) \cdot 1 + (- 1 + \lambda) \cdot 1 = 0,
$$

即

$$
\lambda + 1 = 0,
$$

由此得

$$
\lambda = - 1.
$$

代入(4-14)式,得投影平面的方程为

$$
2 y - 2 z - 2 = 0,
$$

即

$$
y - z - 1 = 0.
$$

所以投影直线的方程为

$$
\left\{ \begin{array}{l} y - z - 1 = 0, \\ x + y + z = 0. \end{array} \right.
$$

## 习题8-4

1. 求过点 $(4, -1, 3)$ 且平行于直线 $\frac{x - 3}{2} = \frac{y}{1} = \frac{z - 1}{5}$ 的直线方程.
2. 求过两点  $M_{1}(3,-2,1)$  和  $M_{2}(-1,0,2)$  的直线方程.
3. 用对称式方程及参数方程表示直线  $\left\{\begin{aligned} x-y+z &= 1, \\ 2x+y+z &= 4.\end{aligned}\right.$
4. 求过点(2,0,-3)且与直线 $\left\{\begin{aligned}x-2y+4z-7=0,\\ 3x+5y-2z+1=0\end{aligned}\right.$ 垂直的平面方程.
5. 求直线  $\left\{\begin{aligned}5x-3y+3z-9=0,\\ 3x-2y+z-1=0\end{aligned}\right.$  与直线  $\left\{\begin{aligned}2x+2y-z+23=0,\\ 3x+8y+z-18=0\end{aligned}\right.$  的夹角的余弦.
6. 证明直线 $\left\{\begin{aligned}x+2y-z=7,\\ -2x+y+z=7\end{aligned}\right.$ 与直线 $\left\{\begin{aligned}3x+6y-3z=8,\\ 2x-y-z=0\end{aligned}\right.$ 平行.
7. 求过点 $(1,0,-2)$ 且与平面 $3x+4y-z+6=0$ 平行，又与直线 $\frac{x-3}{1}=\frac{y+2}{4}=\frac{z}{1}$ 垂直的直线方程.
8. 求过点 $(3,1,-2)$ 且通过直线 $\frac{x-4}{5}=\frac{y+3}{2}=\frac{z}{1}$ 的平面方程.
9. 求直线  $\left\{\begin{aligned} x+y+3z=0, \\ x-y-z=0 \end{aligned}\right.$  与平面  $x-y-z+1=0$  的夹角.
10. 试确定下列各组中的直线和平面间的关系:

(1) $\frac{x + 3}{-2} = \frac{y + 4}{-7} = \frac{z}{3}$ 和 $4x - 2y - 2z = 3$;

(2) $\frac{x}{3}=\frac{y}{-2}=\frac{z}{7}$ 和 $3x-2y+7z=8;$

图

例题精讲

8-3

(3) $\frac{x - 2}{3} = \frac{y + 2}{1} = \frac{z - 3}{-4}$ 和 $x + y + z = 3$.

11. 求过点(1,2,1)且与两直线 $\left\{\begin{aligned}x+2y-z+1=0,\\ x-y+z-1=0\end{aligned}\right.$ 和 $\left\{\begin{aligned}2x-y+z=0,\\ x-y+z=0\end{aligned}\right.$ 都平行的平面的方程.

12. 求点 $(-1,2,0)$ 在平面 $x+2y-z+1=0$ 上的投影.

13. 求点  $P(3,-1,2)$  到直线  $\left\{\begin{aligned} x+y-z+1 &= 0, \\ 2x-y+z-4 &= 0 \end{aligned}\right.$  的距离.

14. 设 $M_0$ 是直线 $L$ 外一点, $M$ 是直线 $L$ 上任意一点, 且直线的方向向量为 $s$, 试证: 点 $M_0$ 到直线 $L$ 的距离

$$
d = \frac {\mid \overrightarrow {M _ {0} M} \times s \mid}{\mid s \mid}.
$$

15. 求直线  $\left\{\begin{aligned}&2x-4y+z=0,\\ &3x-y-2z-9=0\end{aligned}\right.$  在平面  $4x-y+z=1$  上的投影直线的方程.

16. 画出下列各平面所围成的立体的图形:

(1) x=0, y=0, z=0, x=2, y=1,  $3x+4y+2z-12=0$ ;
(2) x=0, z=0, x=1, y=2,  $z=\frac{y}{4}$ .

## 第五节 曲面及其方程

## 一、曲面研究的基本问题

在空间解析几何中,关于曲面的研究有下列两个基本问题:

(1) 已知一曲面作为点的几何轨迹时, 建立这曲面的方程;
(2) 已知坐标 x, y 和 z 间的一个方程时, 研究这方程所表示的曲面的形状.

在第三节中关于建立一种最简单的曲面——平面方程的例子就属于基本问题(1)，以下是建立另一种特殊曲面——球面方程的例子.

例 1 建立球心在点  $M_{0}(x_{0}, y_{0}, z_{0})$ 、半径为 R 的球面的方程.

解 设 $M(x,y,z)$ 是球面上的任一点(图8-38), 则

$$
\mid M _ {0} M \mid = R.
$$

由于

$$
\mid M _ {0} M \mid = \sqrt {\left(x - x _ {0}\right) ^ {2} + \left(y - y _ {0}\right) ^ {2} + \left(z - z _ {0}\right) ^ {2}},
$$

所以

![](images/page_42_image_25.jpg)

<details>
<summary>text_image</summary>

z
O
M₀
R
x
y
</details>

图8-38

$$
\sqrt {\left(x - x _ {0}\right) ^ {2} + \left(y - y _ {0}\right) ^ {2} + \left(z - z _ {0}\right) ^ {2}} = R,
$$

或

$$
\left(x - x _ {0}\right) ^ {2} + \left(y - y _ {0}\right) ^ {2} + \left(z - z _ {0}\right) ^ {2} = R ^ {2}. \tag {5-1}
$$

这就是球面上的点的坐标所满足的方程. 而不在球面上的点的坐标都不满足这方程. 所以方程(5-1)就是以 $M_0(x_0, y_0, z_0)$ 为球心、$R$ 为半径的球面方程.

如果球心在原点,那么  $x_{0}=y_{0}=z_{0}=0$ , 从而球面方程为

$$
x ^ {2} + y ^ {2} + z ^ {2} = R ^ {2}.
$$

下面举一个由已知方程研究它所表示的曲面的例子.

例2 方程 $x^{2} + y^{2} + z^{2} - 2x + 4y = 0$ 表示怎样的曲面？

解 通过配方,原方程可以改写成

$$
(x - 1) ^ {2} + (y + 2) ^ {2} + z ^ {2} = 5.
$$

与(5-1)式比较, 就知道原方程表示球心在点  $M_{0}(1,-2,0)$ 、半径  $R=\sqrt{5}$  的球面.

一般地,设有三元二次方程

$$
A x ^ {2} + A y ^ {2} + A z ^ {2} + D x + E y + F z + G = 0,
$$

这个方程的特点是缺 $xy, yz, zx$ 各项，而且平方项系数相同，只要将方程经过配方可以化成方程(5-1)的形式，则它的图形就是一个球面.

下一目中讨论旋转曲面,也是基本问题(1)的例子;而第三、四目中分别讨论柱面、二次曲面,则是基本问题(2)的例子.

## 二、旋转曲面

以一条平面曲线绕其平面上的一条直线旋转一周所成的曲面叫做旋转曲面,旋转曲线和定直线依次叫做旋转曲面的母线和轴.

设在 yOz 坐标面上有一已知曲线 C, 它的方程为

$$
f (y, z) = 0,
$$

把这曲线绕 $z$ 轴旋转一周，就得到一个以 $z$ 轴为轴的旋转曲面（图8-39).它的方程可以求得如下:

设 $M_{1}(0,y_{1},z_{1})$ 为曲线 $C$ 上的任一点，则有

$$
f (y _ {1}, z _ {1}) = 0. \tag {5-2}
$$

当曲线 $C$ 绕 $z$ 轴旋转时，点 $M_{1}$ 绕 $z$ 轴转到另一点 $M(x,y,z)$，这时 $z = z_{1}$ 保持不变，且点 $M$ 到 $z$ 轴的距离

$$
d = \sqrt {x ^ {2} + y ^ {2}} = | y _ {1} |.
$$

将 $z_{1} = z, y_{1} = \pm \sqrt{x^{2} + y^{2}}$ 代入(5-2)式，就有

$$
f (\pm \sqrt {x ^ {2} + y ^ {2}}, z) = 0, \tag {5-3}
$$

这就是所求旋转曲面的方程.

由此可知,在曲线 C 的方程  $f(y,z)=0$  中将 y 改成  $\pm\sqrt{x^{2}+y^{2}}$ , 便得曲线 C 绕 z 轴旋转所成的旋转曲面的方程.

同理,曲线 C 绕 y 轴旋转所成的旋转曲面的方程为

$$
f (y, \pm \sqrt {x ^ {2} + z ^ {2}}) = 0. \tag {5-4}
$$

例3 直线 $L$ 绕另一条与 $L$ 相交的直线旋转一周, 所得旋转曲面叫做圆锥面. 两直线的交点叫做圆锥面的顶点, 两直线的夹角 $\alpha \left(0 < \alpha < \frac{\pi}{2}\right)$ 叫做圆锥面的半顶角. 试建立顶点在坐标原点 $O$, 旋转轴为 $z$ 轴, 半顶角为 $\alpha$ 的圆锥面 (图8-40) 的方程.

![](images/page_44_image_6.jpg)

<details>
<summary>text_image</summary>

z
M₁(0, y₁, z₁)
M(x, y, z)
C
O
y
x
</details>

图8-39

![](images/page_44_image_8.jpg)

<details>
<summary>text_image</summary>

z
M₁(0, y₁, z₁)
α
M(x, y, z)
O
y
x
</details>

图8-40

解 在 yOz 坐标面上, 直线 L 的方程为

$$
z = y \cot \alpha , \tag {5-5}
$$

因为旋转轴为 z 轴, 所以只要将方程(5-5)中的 y 改成  $\pm\sqrt{x^{2}+y^{2}}$ , 便得到这圆锥面的方程

$$
z = \pm \sqrt {x ^ {2} + y ^ {2}} \cot \alpha
$$

或

$$
z ^ {2} = a ^ {2} (x ^ {2} + y ^ {2}), \tag {5-6}
$$

其中 $a = \cot \alpha$.

显然,圆锥面上任一点 M 的坐标一定满足方程(5-6).如果点 M 不在圆锥面上,那么直线 OM 与 z 轴的夹角就不等于  $\alpha$ ,于是点 M 的坐标就不满足方程(5-6).

例4 将 $zOx$ 坐标面上的双曲线

$$
\frac {x ^ {2}}{a ^ {2}} - \frac {z ^ {2}}{c ^ {2}} = 1
$$

分别绕 z 轴和 x 轴旋转一周, 求所生成的旋转曲面的方程.

解 绕 z 轴旋转所成的旋转曲面叫做旋转单叶双曲面(图 8-41)，它的方程为

$$
\frac {x ^ {2} + y ^ {2}}{a ^ {2}} - \frac {z ^ {2}}{c ^ {2}} = 1.
$$

绕 x 轴旋转所成的旋转曲面叫做旋转双叶双曲面(图 8-42)，它的方程为

$$
\frac {x ^ {2}}{a ^ {2}} - \frac {y ^ {2} + z ^ {2}}{c ^ {2}} = 1.
$$

![](images/page_45_image_4.jpg)

<details>
<summary>text_image</summary>

z
y
O
x
</details>

图8-41

![](images/page_45_image_6.jpg)

<details>
<summary>text_image</summary>

z
y
O
x
</details>

图8-42

## 三、柱面

我们先分析一个具体的例子.

例5 方程 $x^{2} + y^{2} = R^{2}$ 表示怎样的曲面？

解 方程 $x^{2} + y^{2} = R^{2}$ 在 $xOy$ 面上表示圆心在原点 $O$、半径为 $R$ 的圆. 在空间直角坐标系中, 这方程不含竖坐标 $z$, 即不论空间点的竖坐标 $z$ 怎样, 只要它的横坐标 $x$ 和纵坐标 $y$ 能满足这方程, 那么这些点就在这曲面上. 这就是说, 凡是通过 $xOy$ 面内圆 $x^{2} + y^{2} = R^{2}$ 上一点 $M(x, y, 0)$, 且平行于 $z$ 轴的直线 $l$ 都在这曲面上, 因此, 这曲面可以看做是由平行于 $z$ 轴的直线 $l$ 沿 $xOy$ 面上的圆 $x^{2} + y^{2} = R^{2}$ 移动而形成的. 这曲面叫做圆柱面 (图 8-43), $xOy$ 面上的圆 $x^{2} + y^{2} = R^{2}$ 叫做它的准线, 这平行于 $z$ 轴的直线 $l$ 叫做它的母线.

![](images/page_45_image_12.jpg)

<details>
<summary>text_image</summary>

z
x²+y²=R²
l
O'
M
y
x
</details>

图8-43

一般地, 直线 L 沿定曲线 C 平行移动形成的轨迹叫做柱面, 定曲线 C 叫做柱面的准线, 动直线 L 叫做柱面的母线.

上面我们看到,不含 z 的方程  $x^{2}+y^{2}=R^{2}$  在空间直角坐标系中表示圆柱面,它的母线平行于 z 轴,它的准线是 xOy 面上的圆  $x^{2}+y^{2}=R^{2}$ .

类似地,方程  $y^{2}=2x$  表示母线平行于 z 轴的柱面,它的准线是 xOy 面上的抛物线

$y^{2}=2x$ , 该柱面叫做抛物柱面(图8-44).

又如,方程 x-y=0 表示母线平行于 z 轴的柱面,其准线是 xOy 面上的直线 x-y=0,所以它是过 z 轴的平面(图 8-45).

![](images/page_46_image_3.jpg)

<details>
<summary>text_image</summary>

z
y
y²=2x
O
x
</details>

图8-44

![](images/page_46_image_5.jpg)

<details>
<summary>text_image</summary>

z
x-y=0
O
y
x
</details>

图 8-45

一般地, 只含 $x, y$ 而缺 $z$ 的方程 $F(x, y) = 0$ 在空间直角坐标系中表示母线平行于 $z$ 轴的柱面, 其准线是 $xOy$ 面上的曲线 $C: F(x, y) = 0$ (图8-46).

类似可知, 只含 x, z 而缺 y 的方程  $G(x, z) = 0$  和只含 y, z 而缺 x 的方程  $H(y, z) = 0$  分别表示母线平行于 y 轴和 x 轴的柱面.

例如, 方程 x-z=0 表示母线平行于 y 轴的柱面, 其准线是 zOx 面上的直线 x-z=0. 所以它是过 y 轴的平面(图 8-47).

![](images/page_46_image_10.jpg)

<details>
<summary>text_image</summary>

z
F(x, y)=0
O
C
y
x
</details>

图8-46

![](images/page_46_image_12.jpg)

<details>
<summary>text_image</summary>

x-z=0
z
O
y
x
</details>

图8-47

## 四、二次曲面

与平面解析几何中规定的二次曲线相类似,我们把三元二次方程  $F(x,y,z)=0$  所表示的曲面称为二次曲面,把平面称为一次曲面.

二次曲面有九种,适当选取空间直角坐标系,可得它们的标准方程.下面就九种二

次曲面的标准方程来讨论二次曲面的形状.

(1) 椭圆锥面  $\frac{x^{2}}{a^{2}}+\frac{y^{2}}{b^{2}}=z^{2}$

以垂直于 $z$ 轴的平面 $z = t$ 截此曲面，当 $t = 0$ 时得一点 $(0,0,0)$；当 $t \neq 0$ 时，得平面 $z = t$ 上的椭圆

$$
\frac {x ^ {2}}{(a t) ^ {2}} + \frac {y ^ {2}}{(b t) ^ {2}} = 1.
$$

当 $t$ 变化时，上式表示一族长短轴比例不变的椭圆，当 $|t|$ 从大到小并变为0时，这族椭圆从大到小并缩为一点.综合上述讨论，可得椭圆锥面(1)的形状如图8-48所示

平面 z=t 与曲面  $F(x,y,z)=0$  的交线称为截痕. 通过综合截痕的变化来了解曲面形状的方法称为截痕法.

我们还可以用伸缩变形的方法来得出椭圆锥面(1)的形状.

先说明 $xOy$ 平面上的图形伸缩变形的方法. 在 $xOy$ 平面上, 把点 $M(x, y)$ 变为点 $M'(x, \lambda y)$, 从而把点 $M$ 的轨迹 $C$ 变为点 $M'$ 的轨迹 $C'$, 称为把图形 $C$ 沿 $y$ 轴方向伸缩 $\lambda$ 倍变成图形 $C'$. 假如 $C$ 为曲线 $F(x, y) = 0$, 点 $M(x_1, y_1) \in C$, 点 $M$ 变为点 $M'(x_2, y_2)$, 其中 $x_2 = x_1, y_2 = \lambda y_1$, 即 $x_1 = x_2, y_1 = \frac{1}{\lambda} y_2$, 因点 $M \in C$, 有 $F(x_1, y_1) = 0$, 故 $F\left(x_2, \frac{1}{\lambda} y_2\right) = 0$, 因此点 $M'(x_2, y_2)$ 的轨迹 $C'$ 的方程为 $F\left(x, \frac{1}{\lambda} y\right) = 0$. 例如把圆 $x^2 + y^2 = a^2$ 沿 $y$ 轴方向伸缩 $\frac{b}{a}$ 倍, 就变为椭圆 $\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1$ (图8-49).

![](images/page_47_image_9.jpg)

<details>
<summary>text_image</summary>

z
O
y
x
1
</details>

图8-48

![](images/page_47_image_11.jpg)

<details>
<summary>text_image</summary>

y
a
M
b
M'
O
a
x
</details>

图8-49

类似地,把空间图形沿 y 轴方向伸缩  $\frac{b}{a}$  倍,圆锥面  $\frac{x^{2}+y^{2}}{a^{2}}=z^{2}$  (图 8-40) 就变为椭圆锥面  $\frac{x^{2}}{a^{2}}+\frac{y^{2}}{b^{2}}=z^{2}$  (图 8-48).

利用圆锥面(旋转曲面)的伸缩变形来得出椭圆锥面的形状,这种方法是研究曲面形状的一种较方便的方法.

(2) 椭球面  $\frac{x^{2}}{a^{2}}+\frac{y^{2}}{b^{2}}+\frac{z^{2}}{c^{2}}=1$

把 zOx 面上的椭圆  $\frac{x^{2}}{a^{2}} + \frac{z^{2}}{c^{2}} = 1$  绕 z 轴旋转，所得曲面称为旋转椭球面，其方程为

$$
\frac {x ^ {2} + y ^ {2}}{a ^ {2}} + \frac {z ^ {2}}{c ^ {2}} = 1.
$$

再把旋转椭球面沿 y 轴方向伸缩  $\frac{b}{a}$  倍, 便得椭球面(2)的形状如图 8-50 所示.

当 $a = b = c$ 时，椭球面(2)成为 $x^{2} + y^{2} + z^{2} = a^{2}$，这是球心在原点、半径为 $a$ 的球面。显然，球面是旋转椭球面的特殊情形，旋转椭球面是椭球面的特殊情形。把球面 $x^{2} + y^{2} + z^{2} = a^{2}$ 沿 $z$ 轴方向伸缩 $\frac{c}{a}$ 倍，即得旋转椭球面 $\frac{x^2 + y^2}{a^2} +\frac{z^2}{c^2} = 1$；再沿 $y$ 轴方向伸缩 $\frac{b}{a}$ 倍，即得椭球面(2)。

![](images/page_48_image_7.jpg)

<details>
<summary>text_image</summary>

z
y
O
x
</details>

图8-50

(3) 单叶双曲面  $\frac{x^{2}}{a^{2}}+\frac{y^{2}}{b^{2}}-\frac{z^{2}}{c^{2}}=1$

把 $zOx$ 面上的双曲线 $\frac{x^2}{a^2} -\frac{z^2}{c^2} = 1$ 绕 $z$ 轴旋转，得旋转单叶双曲面 $\frac{x^2 + y^2}{a^2} -\frac{z^2}{c^2} = 1$ （图8-41).把此旋转曲面沿 $y$ 轴方向伸缩 $\frac{b}{a}$ 倍，即得单叶双曲面(3).

(4) 双叶双曲面  $\frac{x^{2}}{a^{2}}-\frac{y^{2}}{b^{2}}-\frac{z^{2}}{c^{2}}=1$

把 $zOx$ 面上的双曲线 $\frac{x^2}{a^2} -\frac{z^2}{c^2} = 1$ 绕 $x$ 轴旋转，得旋转双叶双曲面 $\frac{x^2}{a^2} -\frac{y^2 + z^2}{c^2} = 1$ （图8-42），把此旋转曲面沿 $y$ 轴方向伸缩 $\frac{b}{c}$ 倍，即得双叶双曲面(4).

(5) 椭圆抛物面  $\frac{x^{2}}{a^{2}}+\frac{y^{2}}{b^{2}}=z$

把 $zOx$ 面上的抛物线 $\frac{x^2}{a^2} = z$ 绕 $z$ 轴旋转, 所得曲面叫做旋转抛物面, 如图8-51所示. 把此旋转曲面沿 $y$ 轴方向伸缩 $\frac{b}{a}$ 倍, 即得椭圆抛物面(5).

(6) 双曲抛物面  $\frac{x^{2}}{a^{2}} - \frac{y^{2}}{b^{2}} = z$

双曲抛物面又称马鞍面,我们用截痕法来讨论它的形状.

用平面 x=t 截此曲面, 所得截痕 l 为平面 x=t 上的抛物线

$$
- \frac {y ^ {2}}{b ^ {2}} = z - \frac {t ^ {2}}{a ^ {2}},
$$

此抛物线开口朝下,其顶点坐标为

$$
x = t, \quad y = 0, \quad z = \frac {t ^ {2}}{a ^ {2}}.
$$

当 $t$ 变化时，$l$ 的形状不变，位置只作平移，而 $l$ 的顶点的轨迹 $L$ 为平面 $y = 0$ 上的抛物线

$$
z = \frac {x ^ {2}}{a ^ {2}}.
$$

因此,以 l 为母线,L 为准线,母线 l 的顶点在准线 L 上滑动,且母线作平行移动,这样得到的曲面便是双曲抛物面(6),如图 8-52 所示.

![](images/page_49_image_10.jpg)

<details>
<summary>natural_image</summary>

3D geometric diagram of a hemisphere in Cartesian coordinate system (x, y, z axes labeled), showing no text or symbols beyond axis labels.
</details>

图8-51

![](images/page_49_image_12.jpg)

<details>
<summary>text_image</summary>

z
y
O
x
</details>

图8-52

还有三种二次曲面是以三种二次曲线为准线的柱面

$$
\frac {x ^ {2}}{a ^ {2}} + \frac {y ^ {2}}{b ^ {2}} = 1, \quad \frac {x ^ {2}}{a ^ {2}} - \frac {y ^ {2}}{b ^ {2}} = 1, \quad x ^ {2} = a y,
$$

依次称为椭圆柱面、双曲柱面、抛物柱面. 柱面的形状在第三目中已经讨论过, 这里不再赘述.

## 习题8-5

1. 一球面过原点及 $A(4,0,0), B(1,3,0)$ 和 $C(0,0,-4)$ 三点，求球面的方程及球心的坐标和半径.
2. 已知一球面的球心在点  $P_{0}(3,-5,2)$  且与平面  $\Pi:2x-y+3z+9=0$  相切，求该球面方程.

3. 方程  $x^{2}+y^{2}+z^{2}-2x+4y+2z=0$  表示什么曲面？

4. 求与坐标原点 $O$ 及点 $(2,3,4)$ 的距离之比为 $1:2$ 的点的全体所组成的曲面的方程, 它表示怎样的曲面?

5. 将 $zOx$ 坐标面上的抛物线 $z^2 = 5x$ 绕 $x$ 轴旋转一周, 求所生成的旋转曲面的方程.

6. 将 $zOx$ 坐标面上的圆 $x^{2} + z^{2} = 9$ 绕 $z$ 轴旋转一周, 求所生成的旋转曲面的方程.

7. 将 $xOy$ 坐标面上的双曲线 $4x^{2} - 9y^{2} = 36$ 分别绕 $x$ 轴及 $y$ 轴旋转一周, 求所生成的旋转曲面的方程.

8. 画出下列各方程所表示的曲面:

(1) $\left(x-\frac{a}{2}\right)^{2}+y^{2}=\left(\frac{a}{2}\right)^{2};$

(2) $-\frac{x^{2}}{4}+\frac{y^{2}}{9}=1;$

(3) $\frac{x^2}{9} + \frac{z^2}{4} = 1$;

(4) $y^{2}-z=0;$

(5) $z=2-x^{2}.$

9. 指出下列方程在平面解析几何中和在空间解析几何中分别表示什么图形:

(1) x=2;

(2) $y = x + 1$;

(3) $x^{2} + y^{2} = 4$;

(4) $x^{2} - y^{2} = 1$.

10. 说明下列旋转曲面是怎样形成的:

(1) $\frac{x^2}{4} + \frac{y^2}{9} + \frac{z^2}{9} = 1$;

(2) $x^{2} - \frac{y^{2}}{4} +z^{2} = 1;$

(3) $x^{2} - y^{2} - z^{2} = 1$;

(4) $(z - a)^2 = x^2 + y^2$.

11. 画出下列方程所表示的曲面:

(1) $4x^{2}+y^{2}-z^{2}=4;$

(2) $x^{2} - y^{2} - 4z^{2} = 4$;

(3) $\frac{z}{3} = \frac{x^2}{4} + \frac{y^2}{9}$.

12. 画出下列各曲面所围立体的图形:

(1) z=0, z=3, x-y=0,  $x-\sqrt{3}y=0$ ,  $x^{2}+y^{2}=1$  （在第Ⅰ卦限内）;

(2) $x = 0, y = 0, z = 0, x^2 + y^2 = R^2, y^2 + z^2 = R^2$ （在第I卦限内）.

## 第六节 空间曲线及其方程

## 一、空间曲线的一般方程

在第三节中,我们已经知道空间曲线可以看做两个曲面的交线.设

$$
F (x, y, z) = 0 \quad {\text {和}} \quad G (x, y, z) = 0
$$

是两个曲面的方程,则方程组

$$
\left\{ \begin{array}{l} F (x, y, z) = 0, \\ G (x, y, z) = 0. \end{array} \right. \tag {6-1}
$$

就是这两个曲面的交线 C 的方程, 方程组(6-1)也叫做空间曲线 C 的一般方程.

例1 方程组 $\begin{cases} x^2 + y^2 = 1, \\ 2x + 3z = 6 \end{cases}$ 表示怎样的曲线？

解 方程组中第一个方程表示母线平行于 $z$ 轴的圆柱面, 其准线是 $xOy$ 面上的圆, 圆心在原点 $O$, 半径为 1. 方程组中第二个方程表示一个母线平行于 $y$ 轴的柱面, 由于它的准线是 $zOx$ 面上的直线, 因此它是一个平面. 方程组就表示上述平面与圆柱面的交线, 如图 8-53 所示.

例2 方程组 $\left\{ \begin{array}{l} z = \sqrt{a^2 - x^2 - y^2}, \\ \left( x - \frac{a}{2} \right)^2 + y^2 = \left( \frac{a}{2} \right)^2 \end{array} \right.$ 表示怎样的曲线？

解 方程组中第一个方程表示球心在坐标原点 $O$, 半径为 $a$ 的上半球面. 第二个方程表示母线平行于 $z$ 轴的圆柱面, 它的准线是 $xOy$ 面上的圆, 这圆的圆心在点 $\left(\frac{a}{2}, 0\right)$, 半径为 $\frac{a}{2}$. 方程组就表示上述半球面与圆柱面的交线, 如图 8-54 所示.

![](images/page_51_image_4.jpg)

<details>
<summary>text_image</summary>

z
O
y
x
</details>

图8-53

![](images/page_51_image_6.jpg)

<details>
<summary>text_image</summary>

z
O
x
y
</details>

图8-54

## 二、空间曲线的参数方程

空间曲线 $C$ 的方程除了一般方程之外，也可以用参数形式表示，只要将 $C$ 上动点的坐标 $x, y$ 和 $z$ 表示为参数 $t$ 的函数

$$
\left\{ \begin{array}{l} x = x (t), \\ y = y (t), \\ z = z (t). \end{array} \right. \tag {6-2}
$$

当给定 $t = t_{1}$ 时，就得到曲线 $C$ 上的一个点 $(x_{1},y_{1},z_{1})$；随着 $t$ 的变动便可得曲线 $C$ 上的全部点。方程组(6-2)叫做空间曲线的参数方程。

例3 如果空间一点 $M$ 在圆柱面 $x^{2} + y^{2} = a^{2}$ 上以角速度 $\omega$ 绕 $z$ 轴旋转, 同时又以线速度 $v$ 沿平行于 $z$ 轴的正方向上升 (其中 $\omega$ 和 $v$ 都是常数), 那么点 $M$ 构成的图形叫做螺旋线. 试建立其参数方程.

解 取时间 $t$ 为参数. 设当 $t = 0$ 时, 动点位于 $x$ 轴上的一点 $A(a,0,0)$ 处. 经过时间 $t$, 动点由 $A$ 运动到 $M(x,y,z)$ (图8-55). 记 $M$ 在 $xOy$ 面上的投影为 $M', M'$ 的坐标为 $(x,y,0)$ .由于动点在圆柱面上以角速度 $\omega$ 绕z轴旋转,所以经过时间 $t,\angle AOM^{\prime}=\omega t$ .从而

$$
x = \mid O M ^ {\prime} \mid \cos \angle A O M ^ {\prime} = a \cos \omega t,
$$

$$
y = \mid O M ^ {\prime} \mid \sin \angle A O M ^ {\prime} = a \sin \omega t.
$$

由于动点同时以线速度 v 沿平行于 z 轴的正方向上升，所以

$$
z = M ^ {\prime} M = v t.
$$

因此螺旋线的参数方程为

$$
\left\{ \begin{array}{l} x = a \cos \omega t, \\ y = a \sin \omega t, \\ z = v t. \end{array} \right.
$$

![](images/page_52_image_8.jpg)

<details>
<summary>text_image</summary>

z
h
ωt
O M
A
M'
x
y
</details>

图8-55

也可以用其他变量作参数.例如令 $\theta = \omega t$ ，则螺旋线的参数方程可写为

$$
\left\{ \begin{array}{l} x = a \cos \theta , \\ y = a \sin \theta , \\ z = b \theta . \end{array} \right.
$$

这里 $b = \frac{v}{\omega}$ 而参数为 $\theta$.

螺旋线是实践中常用的曲线.例如,平头螺丝钉的外缘曲线就是螺旋线.当我们拧紧平头螺丝钉时,它的外缘曲线上的任一点M,一方面绕螺丝钉的轴旋转,另一方面又沿平行于轴线的方向前进,点M就走出一段螺旋线.

螺旋线有一个重要性质: 当  $\theta$  从  $\theta_{0}$  变到  $\theta_{0} + \alpha$  时, z 由  $b\theta_{0}$  变到  $b\theta_{0} + b\alpha$ . 这说明当  $OM'$  转过角  $\alpha$  时, 点 M 沿螺旋线上升了高度  $b\alpha$ , 即上升的高度与  $OM'$  转过的角度成正比. 特别是当  $OM'$  转过一周, 即  $\alpha = 2\pi$  时, 点 M 就上升固定的高度  $h = 2\pi b$ . 这个高度  $h = 2\pi b$  在工程技术上叫做螺距.

\* 曲面的参数方程

下面顺便介绍一下曲面的参数方程.曲面的参数方程通常是含两个参数的方程，形如

$$
\left\{ \begin{array}{l} x = x (s, t), \\ y = y (s, t), \\ z = z (s, t). \end{array} \right. \tag {6-3}
$$

例如空间曲线 $\Gamma$

$$
\left\{ \begin{array}{l l} x = \varphi (t), \\ y = \psi (t), & (\alpha \leqslant t \leqslant \beta) \\ z = \omega (t) \end{array} \right.
$$

绕 z 轴旋转, 所得旋转曲面的方程为

$$
\left\{ \begin{array}{l} x = \sqrt {\left[ \varphi (t) \right] ^ {2} + \left[ \psi (t) \right] ^ {2}} \cos \theta , \\ y = \sqrt {\left[ \varphi (t) \right] ^ {2} + \left[ \psi (t) \right] ^ {2}} \sin \theta , \quad \alpha \leqslant t \leqslant \beta , 0 \leqslant \theta \leqslant 2 \pi . \\ z = \omega (t), \end{array} \right. \tag {6-4}
$$

这是因为, 固定一个 t, 得  $\Gamma$  上一点  $M_{1}(\varphi(t), \psi(t), \omega(t))$ , 点  $M_{1}$  绕 z 轴旋转, 得空间的一个圆, 该圆在平面  $z = \omega(t)$  上, 其半径为点  $M_{1}$  到 z 轴的距离  $\sqrt{[\varphi(t)]^{2} + [\psi(t)]^{2}}$ , 因此, 固定 t 的方程 (6-4) 就是该圆的参数方程. 再令 t 在  $[\alpha, \beta]$  内变动, 方程 (6-4) 便是旋转曲面的方程.

例如直线

$$
\left\{ \begin{array}{l} x = 1, \\ y = t, \\ z = 2 t \end{array} \right.
$$

绕 z 轴旋转所得旋转曲面(图 8-56)的方程为

$$
\left\{ \begin{array}{l} x = \sqrt {1 + t ^ {2}} \cos \theta , \\ y = \sqrt {1 + t ^ {2}} \sin \theta , \\ z = 2 t \end{array} \right.
$$

![](images/page_53_image_8.jpg)

<details>
<summary>text_image</summary>

z
M₁
O
y
x
</details>

图8-56

$\left( \text{上式消去 } t \text{ 和 } \theta, \text{得曲面的直角坐标方程为 } x^{2} + y^{2} = 1 + \frac{z^{2}}{4} \right).$

又如球面 $x^{2} + y^{2} + z^{2} = a^{2}$ 可看成 $zOx$ 面上的半圆周

$$
\left\{ \begin{array}{l l} x = a \sin \varphi , \\ y = 0, & 0 \leqslant \varphi \leqslant \pi \\ z = a \cos \varphi , \end{array} \right.
$$

绕 z 轴旋转所得(图 8-57)，故球面方程为

$$
\left\{ \begin{array}{l l} x = a \sin \varphi \cos \theta , \\ y = a \sin \varphi \sin \theta , & 0 \leqslant \varphi \leqslant \pi , 0 \leqslant \theta \leqslant 2 \pi . \\ z = a \cos \varphi , \end{array} \right.
$$

![](images/page_53_image_15.jpg)

<details>
<summary>text_image</summary>

z
M₁
O
y
x
</details>

图8-57

## 三、空间曲线在坐标面上的投影

设空间曲线 C 的一般方程为  $(6-1)$ ，现在来研究由方程组  $(6-1)$  消去变量 z 后（如果可能的话）所得的方程

$$
H (x, y) = 0. \tag {6-5}
$$

由于方程(6-5)是由方程组(6-1)消去 $z$ 后所得的结果, 因此当 $x, y$ 和 $z$ 满足方程组(6-1)时, 前两个坐标 $x, y$ 必定满足方程(6-5), 这说明曲线 $C$ 上的所有点都在由方程(6-5)所表示的曲面上.

由上节知道,方程(6-5)表示一个母线平行于z轴的柱面.由上面的讨论可知,这柱面必定包含曲线C.以曲线C为准线、母线平行于z轴(即垂直于xOy面)的柱面叫做曲线C关于xOy面的投影柱面,投影柱面与xOy面的交线叫做空间曲线C在xOy面上的投影曲线,或简称投影.因此,方程(6-5)所表示的柱面必定包含投影柱面,而方程

$$
\left\{ \begin{array}{l} H (x, y) = 0, \\ z = 0 \end{array} \right.
$$

所表示的曲线必定包含空间曲线 C 在 xOy 面上的投影.

同理,消去方程组(6-1)中的变量x或变量y,再分别和x=0或y=0联立,我们就可得到包含曲线C在yOz面或zOx面上的投影的曲线方程:

$$
\left\{ \begin{array}{l l} R (  y, z) = 0  , \\ x = 0  , \end{array} \right. \quad \text {或} \quad \left\{ \begin{array}{l l} T (  x, z) = 0  , \\ y = 0. \end{array} \right.
$$

例4 已知两球面的方程为

$$
x ^ {2} + y ^ {2} + z ^ {2} = 1 \tag {6-6}
$$

和

$$
x ^ {2} + (y - 1) ^ {2} + (z - 1) ^ {2} = 1, \tag {6-7}
$$

求它们的交线 C 在 xOy 面上的投影的方程.

解 先求包含交线 $C$ 而母线平行于 $z$ 轴的柱面方程. 因此要由方程(6-6)、(6-7)消去 $z$, 为此可先从(6-6)式减去(6-7)式并化简, 得到

$$
y + z = 1.
$$

再以 $z = 1 - y$ 代入方程(6-6)或(6-7)即得所求的柱面方程为

$$
x ^ {2} + 2 y ^ {2} - 2 y = 0.
$$

容易看出,这就是交线 C 关于 xOy 面的投影柱面方程,于是两球面的交线在 xOy 面上的投影的方程是

$$
\left\{ \begin{array}{l} x ^ {2} + 2 y ^ {2} - 2 y = 0, \\ z = 0. \end{array} \right.
$$

在重积分和曲面积分的计算中,往往需要确定一个立体或曲面在坐标面上的投影,这时要利用投影柱面和投影曲线.

例5 设一个立体由上半球面 $z = \sqrt{4 - x^2 - y^2}$ 和锥面 $z = \sqrt{3(x^2 + y^2)}$ 所围成（图8-58），求它在 $xOy$ 面上的投影.

解 半球面和锥面的交线为

$$
C: \left\{ \begin{array}{l} z = \sqrt {4 - x ^ {2} - y ^ {2}}, \\ z = \sqrt {3 (x ^ {2} + y ^ {2})}. \end{array} \right.
$$

由上列方程组消去 $z$ ，得到 $x^{2} + y^{2} = 1.$ 这是一个母线平行于 $z$ 轴的圆柱面，容易看出，这恰好是交线 $C$ 关于$xOy$ 面的投影柱面，因此交线 $C$ 在 $xOy$ 面上的投影曲线为

$$
\left\{ \begin{array}{l} x ^ {2} + y ^ {2} = 1, \\ z = 0. \end{array} \right.
$$

这是 xOy 面上的一个圆, 于是所求立体在 xOy 面上的投影, 就是该圆在 xOy 面上所围的部分

$$
x ^ {2} + y ^ {2} \leqslant 1.
$$

![](images/page_55_image_5.jpg)

<details>
<summary>text_image</summary>

z
O
y
x²+y²≤1
x
</details>

图8-58

![](images/page_55_image_7.jpg)

## 习题8-6

1. 画出下列曲线在第Ⅰ卦限内的图形:

(1) $\left\{\begin{aligned}x=1,\\ y=2;\end{aligned}\right.$

(2) $\left\{ \begin{array}{l} z = \sqrt{4 - x^2 - y^2}, \\ x - y = 0; \end{array} \right.$

(3) $\left\{ \begin{array}{l}x^{2} + y^{2} = a^{2},\\ x^{2} + z^{2} = a^{2}. \end{array} \right.$

2. 指出下列方程组在平面解析几何中与在空间解析几何中分别表示什么图形:

(1) $\left\{ \begin{array}{l} y = 5x + 1, \\ y = 2x - 3; \end{array} \right.$

(2) $\left\{\begin{aligned}\frac{x^{2}}{4}+\frac{y^{2}}{9}=1,\\ y=3.\end{aligned}\right.$

3. 分别求母线平行于 $x$ 轴及 $y$ 轴而且通过曲线 $\left\{ \begin{array}{l} 2x^{2} + y^{2} + z^{2} = 16, \\ x^{2} + z^{2} - y^{2} = 0 \end{array} \right.$ 的柱面方程.

4. 求下列两曲面的交线在 $xOy$ 面上的投影的方程:

(1) 球面  $x^{2}+y^{2}+z^{2}=9$  与平面  $x+z=1$ ;
(2) 椭球面  $x^{2}+y^{2}+4z^{2}=1$  与圆锥面  $z^{2}=x^{2}+y^{2}$ .

5. 将下列曲线的一般方程化为参数方程:

(1) $\left\{\begin{aligned}x^{2}+y^{2}+z^{2}&=9,\\ y&=x;\end{aligned}\right.$

(2) $\left\{ \begin{array}{l}(x - 1)^2 + y^2 + (z + 1)^2 = 4, \\ z = 0. \end{array} \right.$

6. 求螺旋线  $\left\{\begin{aligned} x &= a \cos \theta, \\ y &= a \sin \theta, \\ z &= b \theta \end{aligned}\right.$  在三个坐标面上的投影曲线的直角坐标方程.

7. 求上半球 $0 \leqslant z \leqslant \sqrt{a^2 - x^2 - y^2}$ 与圆柱体 $x^2 + y^2 \leqslant ax (a > 0)$ 的公共部分在 $xOy$ 面和 $zOx$ 面上的投影.
8. 求旋转抛物面  $z = x^{2} + y^{2} (0 \leqslant z \leqslant 4)$  在三坐标面上的投影.

## 总习题八

1. 填空:

（1）设在坐标系 $[O;i,j,k]$ 中点A和点M的坐标依次为 $(x_{0},y_{0},z_{0})$ 和 $(x,y,z)$ ，则在 $[A;i,j,k]$ 坐标系中，点M的坐标为\_\_\_\_，向量 $\overrightarrow{OM}$ 的坐标为\_\_\_\_；
(2) 设数  $\lambda_{1}, \lambda_{2}, \lambda_{3}$  不全为 0，使  $\lambda_{1}a + \lambda_{2}b + \lambda_{3}c = 0$ ，则 a, b, c 三个向量是 \_\_\_\_ 的；
(3) 设  $\boldsymbol{a}=(2,1,2)$ ,  $\boldsymbol{b}=(4,-1,10)$ ,  $c=b-\lambda a$ , 且  $a \perp c$ , 则  $\lambda=$ \_\_\_\_ ;
(4) 设  $\left|a\right|=3,\left|b\right|=4,\left|c\right|=5$  ,且满足  $a+b+c=0$  ,则  $\left|a\times b+b\times c+c\times a\right|=$  \_\_\_\_.

2. 下列两题中给出了四个结论, 从中选出一个正确的结论:

（1）设直线 L 的方程为  $\left\{\begin{aligned} x-y+z &= 1, \\ 2x+y+z &= 4, \end{aligned}\right.$  则 L 的参数方程为（）；

(A) $\left\{\begin{aligned}x&=1-2t,\\ y&=1+t,\\ z&=1+3t\end{aligned}\right.$

(B) $\left\{ \begin{array}{l}x = 1 - 2t,\\ y = -1 + t,\\ z = 1 + 3t \end{array} \right.$

(C) $\left\{ \begin{array}{l}x = 1 - 2t,\\ y = 1 - t,\\ z = 1 + 3t \end{array} \right.$

(D) $\left\{ \begin{array}{l}x = 1 - 2t,\\ y = -1 - t,\\ z = 1 + 3t \end{array} \right.$

(2) 下列结论中, 错误的是().

(A) $z + 2x^{2} + y^{2} = 0$ 表示椭圆抛物面

(B) $x^{2} + 2y^{2} = 1 + 3z^{2}$ 表示双叶双曲面

(C)  $x^{2}+y^{2}-(z-1)^{2}=0$  表示圆锥面

(D) $y^{2}=5x$ 表示抛物柱面

$$
\overrightarrow {A D} + \overrightarrow {B E} + \overrightarrow {C F} = 0.
$$

3. 在 y 轴上求与点 A(1,-3,7) 和点 B(5,7,-5) 等距离的点.
4. 已知 $\triangle ABC$ 的顶点为 $A(3,2,-1), B(5,-4,7)$ 和 $C(-1,1,2)$, 求从顶点 $C$ 所引中线的长度.
5. 设 $\triangle ABC$ 的三边 $\overrightarrow{BC} = a, \overrightarrow{CA} = b, \overrightarrow{AB} = c$, 三边中点依次为 $D, E, F$, 试用向量 $a, b, c$ 表示 $\overrightarrow{AD}, \overrightarrow{BE}, \overrightarrow{CF}$, 并证明
6. 试用向量证明: 梯形两腰中点的连线平行于底边, 且其长度等于上、下两底边长度之和的一半.
7. 设 $|a + b| = |a - b|$, $a = (3, -5, 8)$, $b = (-1, 1, z)$, 求 $z$.
8. 设 $|a| = \sqrt{3}$, $|b| = 1$, $(\widehat{a, b}) = \frac{\pi}{6}$, 求向量 $a + b$ 与 $a - b$ 的夹角.
9. 设 $(a+3b)\perp(7a-5b),(a-4b)\perp(7a-2b)$ ，求 $(\widehat{a,b})$ .
10. 设向量 $a = (1, -2, 2), b = (-2, 1, 2)$，若存在向量 $c$，使 $a \times c = b$，试求向量 $c$；若向量 $c$ 不止一个，试找出模最小的那个 $c$.
11. 设 $|a| = 4$, $|b| = 3$, $(\widehat{a, b}) = \frac{\pi}{6}$, 求以 $a + 2b$ 和 $a - 3b$ 为边的平行四边形的面积.
12. 设 $a = (2, -3, 1), b = (1, -2, 3), c = (2, 1, 2)$，向量 $r$ 满足 $r \perp a, r \perp b, \operatorname{Prj}_c r = 14$，求 $r$.
13. 设 $a = (-1, 3, 2), b = (2, -3, -4), c = (-3, 12, 6)$，证明三向量 $a, b, c$ 共面，并用 $a$ 和 $b$ 表

示c.

14. 已知动点 $M(x, y, z)$ 到 $xOy$ 面的距离与点 $M$ 到点 $(1, -1, 2)$ 的距离相等, 求点 $M$ 的轨迹的方程.

15. 指出下列旋转曲面的一条母线和旋转轴:

(1) $z = 2(x^{2} + y^{2})$;

(2) $\frac{x^2}{36} + \frac{y^2}{9} + \frac{z^2}{36} = 1$;

(3) $z^2 = 3(x^2 + y^2)$;

(4) $x^{2} - \frac{y^{2}}{4} -\frac{z^{2}}{4} = 1.$

16. 求通过点 $A(3,0,0)$ 和 $B(0,0,1)$ 且与 $xOy$ 面成 $\frac{\pi}{3}$ 角的平面的方程.

17. 设一平面垂直于平面 $z = 0$，并通过从点 $(1, -1, 1)$ 到直线 $\left\{ \begin{array}{l} y - z + 1 = 0, \\ x = 0 \end{array} \right.$ 的垂线，求此平面的方程.

18. 求过点 $(-1,0,4)$, 且平行于平面 $3x - 4y + z - 10 = 0$, 又与直线 $\frac{x + 1}{1} = \frac{y - 3}{1} = \frac{z}{2}$ 相交的直线的方程.

19. 一直线 $l$ 过点 $A(-3,5,-9)$ 且与两直线 $l_{1}: \begin{cases} y = 3x + 5, \\ z = 2x - 3, \end{cases} l_{2}: \begin{cases} y = 4x - 7, \\ z = 5x + 10 \end{cases}$ 相交，求此直线方程.

20. 已知点 $A(1,0,0)$ 及点 $B(0,2,1)$, 试在 $z$ 轴上求一点 $C$, 使 $\triangle ABC$ 的面积最小.

21. 求曲线  $\left\{\begin{aligned}z&=2-x^{2}-y^{2},\\ z&(x-1)^{2}+(y-1)^{2}\end{aligned}\right.$  在三个坐标面上的投影曲线的方程.

22. 求锥面 $z = \sqrt{x^2 + y^2}$ 与柱面 $z^2 = 2x$ 所围立体在三个坐标面上的投影.

23. 画出下列各曲面所围立体的图形:

(1) 抛物柱面  $2y^{2}=x$ ，平面 z=0 及  $\frac{x}{4}+\frac{y}{2}+\frac{z}{2}=1$ ;

(2) 抛物柱面  $x^{2}=1-z$ ，平面 y=0, z=0 及  $x+y=1$ ;

(3) 圆锥面  $z = \sqrt{x^{2} + y^{2}}$  及旋转抛物面  $z = 2 - x^{2} - y^{2}$ ;

(4) 旋转抛物面  $x^{2}+y^{2}=z$ ，柱面  $y^{2}=x$ ，平面 z=0 及 x=1.

第八章释疑解难

![](images/page_57_image_21.jpg)

第八章例题精讲

![](images/page_57_image_23.jpg)

# 第九章

# 多元函数微分法及其应用

上册中我们讨论的函数都只有一个自变量,这种函数叫做一元函数.但在很多实际问题中往往牵涉多方面的因素,反映到数学上,就是一个变量依赖于多个变量的情形.这就提出了多元函数以及多元函数的微分和积分问题.本章将在一元函数微分学的基础上,讨论多元函数的微分法及其应用.讨论中我们以二元函数为主,因为从一元函数到二元函数会产生新的问题,而从二元函数到二元以上的多元函数则可以类推.

## 第一节 多元函数的基本概念

## 一、平面点集 $^{*}n$ 维空间

在讨论一元函数时,一些概念、理论和方法都是基于  $R^{1}$  中的点集、两点间的距离、区间和邻域等概念.为了将一元函数微积分推广到多元的情形,首先需要将上述一些概念加以推广,同时还需涉及一些其他概念.为此先引入平面点集的一些基本概念,将有关概念从  $R^{1}$  中的情形推广到  $R^{2}$  中;然后引入 n 维空间,以便推广到一般的  $R^{n}$  中.

## 1. 平面点集

由平面解析几何知道, 当在平面上引入了一个直角坐标系后, 平面上的点 $P$ 与有序二元实数组 $(x, y)$ 之间就建立了一一对应. 于是, 我们常把有序实数组 $(x, y)$ 与平面上的点 $P$ 视作是等同的. 这种建立了坐标系的平面称为坐标平面. 二元有序实数组 $(x, y)$ 的全体, 即 $\mathbf{R}^2 = \mathbf{R} \times \mathbf{R} = \{(x, y) | x, y \in \mathbf{R}\}$ 就表示坐标平面.

坐标平面上具有某种性质 $P$ 的点的集合, 称为平面点集, 记作

$$
E = \{(x, y) \mid (x, y) \text {具有性质} P \}.
$$

例如,平面上以原点为中心、r为半径的圆内所有点的集合是

$$
C = \{(x, y) \mid x ^ {2} + y ^ {2} <   r ^ {2} \}.
$$

如果以点 $P$ 表示 $(x,y)$ ， $|OP|$ 表示点 $P$ 到原点 $O$ 的距离，那么集合 $C$ 也可表成

$$
C = \{P \mid | O P | <   r \}.
$$

现在我们来引入  $R^{2}$  中邻域的概念.

设 $P_{0}(x_{0},y_{0})$ 是 $xOy$ 平面上的一个点，$\delta$ 是某一正数.与点 $P_{0}(x_{0},y_{0})$ 距离小于 $\delta$ 的点 $P(x,y)$ 的全体，称为点 $P_{0}$ 的 $\delta$ 邻域，记作 $U(P_{0},\delta)$，即

$$
U (P _ {0}, \delta) = \{P | | P P _ {0} | <   \delta \},
$$

也就是

$$
U (P _ {0}, \delta) = \{(x, y) | \sqrt {(x - x _ {0}) ^ {2} + (y - y _ {0}) ^ {2}} <   \delta \}.
$$

点 $P_0$ 的去心 $\delta$ 邻域，记作 $\stackrel{\circ}{U}(P_0,\delta)$ ，即

$$
\stackrel {\circ} {U} (P _ {0}, \delta) = \{P \mid 0 <   | P P _ {0} | <   \delta \}.
$$

在几何上， $U(P_{0},\delta)$  就是 xOy 平面上以点  $P_{0}(x_{0},y_{0})$  为中心、 $\delta>0$  为半径的圆内部的点  $P(x,y)$  的全体.

如果不需要强调邻域的半径 $\delta$ ，则用 $U(P_0)$ 表示点 $P_0$ 的某个邻域，点 $P_0$ 的去心邻域记作 $\mathring{U}(P_0)$

下面利用邻域来描述点和点集之间的关系.

任意一点 $P \in \mathbb{R}^2$ 与任意一个点集 $E \subset \mathbb{R}^2$ 之间必有以下三种关系中的一种:

(1) 内点: 如果存在点 P 的某个邻域  $U(P)$ ，使得  $U(P) \subset E$ ，那么称 P 为 E 的内点（如图 9-1 中， $P_{1}$  为 E 的内点）；

(2) 外点: 如果存在点 P 的某个邻域  $U(P)$ ，使得  $U(P) \cap E = \varnothing$ ，那么称 P 为 E 的外点（如图 9-1 中， $P_{2}$  为 E 的外点）；

(3) 边界点: 如果点 P 的任一邻域内既含有属于 E 的点, 又含有不属于 E 的点, 那么称 P 为 E 的边界点 (如图 9-1 中,  $P_{3}$  为 E 的边界点).

![](images/page_59_image_20.jpg)

<details>
<summary>text_image</summary>

P₁
E
P₃
P₂
</details>

图9-1

E 的边界点的全体,称为 E 的边界,记作  $\partial E$ .

$E$ 的内点必属于 $E; E$ 的外点必定不属于 $E$; 而 $E$ 的边界点可能属于 $E$, 也可能不属于 $E$.

任意一点 $P$ 与一个点集 $E$ 之间除了上述三种关系之外, 还有另一种关系, 这就是下面定义的聚点.

聚点:如果对于任意给定的  $\delta>0$ , 点 P 的去心邻域  $\stackrel{\circ}{U}(P,\delta)$  内总有 E 中的点, 那么称 P 是 E 的聚点.

由聚点的定义可知, 点集 E 的聚点 P 本身, 可以属于 E, 也可以不属于 E.

例如,设平面点集

$$
E = \{(x, y) \mid 1 <   x ^ {2} + y ^ {2} \leqslant 2 \}.
$$

满足 $1 < x^{2} + y^{2} < 2$ 的一切点 $(x, y)$ 都是 $E$ 的内点；满足 $x^{2} + y^{2} = 1$ 的一切点 $(x, y)$ 都是 $E$ 的边界点，它们都不属于 $E$；满足 $x^{2} + y^{2} = 2$ 的一切点 $(x, y)$ 也是 $E$ 的边界点，它们都属于 $E$；点集 $E$ 以及它的边界 $\partial E$ 上的一切点都是 $E$ 的聚点。

根据点集所属点的特征,再来定义一些重要的平面点集.

开集:如果点集 E 的点都是 E 的内点,那么称 E 为开集.

闭集:如果点集 E 的边界  $\partial E \subset E$ , 那么称 E 为闭集.

例如，集合 $\{(x,y)\mid1<x^{2}+y^{2}<2\}$ 是开集；集合 $\{(x,y)\mid1\leqslant x^{2}+y^{2}\leqslant2\}$ 是闭集；而集合 $\{(x,y)\mid1<x^{2}+y^{2}\leqslant2\}$ 既非开集，也非闭集.

连通集:如果点集 E 内任何两点,都可用折线连接起来,且该折线上的点都属于 E,那么称 E 为连通集.

区域(或开区域):连通的开集称为区域或开区域.

闭区域: 开区域连同它的边界一起所构成的点集称为闭区域.

例如,集合 $\{(x,y)\mid1<x^{2}+y^{2}<2\}$ 是区域,而集合 $\{(x,y)\mid1\leqslant x^{2}+y^{2}\leqslant2\}$ 是闭区域.

有界集:对于平面点集 E, 如果存在某一正数 r, 使得

$$
E \subset U (O, r),
$$

其中 O 是坐标原点,那么称 E 为有界集.

无界集:一个集合如果不是有界集,就称这个集合为无界集.

例如,集合 $\{(x,y)\mid1\leqslant x^{2}+y^{2}\leqslant2\}$ 是有界闭区域,集合 $\{(x,y)\mid x+y>0\}$ 是无界开区域,集合 $\{(x,y)\mid x+y\geqslant0\}$ 是无界闭区域.

## \*2. $n$ 维空间

设 n 为取定的一个正整数, 我们用  $R^{n}$  表示 n 元有序实数组  $(x_{1}, x_{2}, \cdots, x_{n})$  的全体所构成的集合, 即

$$
\mathbf {R} ^ {n} = \mathbf {R} \times \mathbf {R} \times \dots \times \mathbf {R} = \left\{\left(x _ {1}, x _ {2}, \dots , x _ {n}\right) \mid x _ {i} \in \mathbf {R}, i = 1, 2, \dots , n \right\}.
$$

$R^{n}$ 中的元素 $(x_{1},x_{2},\cdots,x_{n})$ 有时也用单个字母x来表示,即 $x=(x_{1},x_{2},\cdots,x_{n})$ .当所有的 $x_{i}\quad(i=1,2,\cdots,n)$ 都为零时,称这样的元素为 $R^{n}$ 中的零元,记为0或0.在解析几何中,通过直角坐标系, $R^{2}$ （或 $R^{3}$ ）中的元素分别与平面(或空间)中的点或向量建立一一对应,因而 $R^{n}$ 中的元素 $x=(x_{1},x_{2},\cdots,x_{n})$ 也称为 $R^{n}$ 中的一个点或一个n维向量, $x_{i}$ 称为点x的第i个坐标或n维向量x的第i个分量.特别地, $R^{n}$ 中的零元0称为 $R^{n}$ 中的坐标原点或n维零向量.

为了在集合 $\mathbb{R}^n$ 中的元素之间建立联系，在 $\mathbb{R}^n$ 中定义线性运算如下:

设  $\boldsymbol{x}=(x_{1},x_{2},\cdots,x_{n}),\boldsymbol{y}=(y_{1},y_{2},\cdots,y_{n})$  为  $R^{n}$  中任意两个元素， $\lambda\in R$ ，规定

$$
x + y = (x _ {1} + y _ {1}, x _ {2} + y _ {2}, \dots , x _ {n} + y _ {n}),
$$

$$
\lambda x = (\lambda x _ {1}, \lambda x _ {2}, \dots , \lambda x _ {n}).
$$

这样定义了线性运算的集合  $R^{n}$  称为 n 维空间.

$\mathbf{R}^n$ 中点 $x = (x_{1}, x_{2}, \dots, x_{n})$ 和点 $y = (y_{1}, y_{2}, \dots, y_{n})$ 间的距离，记作 $\rho(x, y)$，规定

$$
\rho (x, y) = \sqrt {(x _ {1} - y _ {1}) ^ {2} + (x _ {2} - y _ {2}) ^ {2} + \cdots + (x _ {n} - y _ {n}) ^ {2}}.
$$

显然，n=1,2,3时，上述规定与数轴上、直角坐标系下平面及空间中两点间的距离一致.

$R^{n}$ 中元素 $x=(x_{1},x_{2},\cdots,x_{n})$ 与零元0之间的距离 $\rho(x,0)$ 记作 $\|x\|$ （在 $R^{1},R^{2}$ ， $R^{3}$ 中，通常将 $\|x\|$ 记作 $|x|$ ），即

$$
\| x \| = \sqrt {x _ {1} ^ {2} + x _ {2} ^ {2} + \cdots + x _ {n} ^ {2}}.
$$

采用这一记号,结合向量的线性运算,便得

$$
\| x - y \| = \sqrt {(x _ {1} - y _ {1}) ^ {2} + (x _ {2} - y _ {2}) ^ {2} + \cdots + (x _ {n} - y _ {n}) ^ {2}} = \rho (x, y).
$$

在 n 维空间  $R^{n}$  中定义了距离以后, 就可以定义  $R^{n}$  中变元的极限:

设  $\boldsymbol{x}=(x_{1},x_{2},\cdots,x_{n}),\boldsymbol{a}=(a_{1},a_{2},\cdots,a_{n})\in\mathbb{R}^{n}$ . 如果

$$
\| x - a \| \rightarrow 0,
$$

那么称变元 x 在  $R^{n}$  中趋于固定元 a，记作  $x \rightarrow a$ .

显然，

$$
x \rightarrow a \iff x _ {1} \rightarrow a _ {1}, x _ {2} \rightarrow a _ {2}, \dots , x _ {n} \rightarrow a _ {n}.
$$

在  $R^{n}$  中引入线性运算和距离,使得前面讨论过的有关平面点集的一系列概念,可以方便地引入到  $n (n \geqslant 3)$  维空间中来,例如,

设  $\boldsymbol{a}=(a_{1},a_{2},\cdots,a_{n})\in\mathbb{R}^{n},\delta$  是某一正数，则 n 维空间内的点集

$$
U (\boldsymbol {a}, \delta) = \{\boldsymbol {x} \mid \boldsymbol {x} \in \mathbb {R} ^ {n}, \rho (\boldsymbol {x}, \boldsymbol {a}) <   \delta \}
$$

就定义为 $\mathbb{R}^n$ 中点 $a$ 的 $\delta$ 邻域. 以邻域为基础, 可以定义点集的内点、外点、边界点和聚点以及开集、闭集、区域等一系列概念. 这里不再赘述.

## 二、多元函数的概念

在很多自然现象以及实际问题中,经常会遇到多个变量之间的依赖关系,举例如下:

例 1 圆柱体的体积 V 和它的底半径 r、高 h 之间具有关系

$$
V = \pi r ^ {2} h.
$$

这里, 当 r 和 h 在集合  $\{(r,h) \mid r>0, h>0\}$  内取定一对值  $(r,h)$  时, V 的对应值就随之确定.

例 2 一定量的理想气体的压强 p、体积 V 和绝对温度 T 之间具有关系

$$
p = \frac {R T}{V},
$$

其中 R 为常数. 这里, 当 V 和 T 在集合  $\{(V,T) \mid V>0, T>T_{0}\}$  内取定一对值  $(V,T)$  时, p 的对应值就随之确定.

例 3 设 R 是电阻  $R_{1}$  和  $R_{2}$  并联后的总电阻, 由电学知道, 它们之间具有关系

$$
R = \frac {R _ {1} R _ {2}}{R _ {1} + R _ {2}}.
$$

这里，当 $R_{1}$ 和 $R_{2}$ 在集合 $\{(R_1,R_2)\mid R_1 > 0,R_2 > 0\}$ 内取定一对值 $(R_{1},R_{2})$ 时，$R$ 的对应值就随之确定.

上面三个例子的具体意义虽各不相同,但它们却有共同的性质,抽出这些共性就可得出以下二元函数的定义.

定义1 设 $D$ 是 $\mathbf{R}^2$ 的一个非空子集, 称映射 $f: D \to \mathbf{R}$ 为定义在 $D$ 上的二元函数, 通常记为

$$
z = f (x, y), \quad (x, y) \in D
$$

或

$$
z = f (P), \quad P \in D,
$$

其中点集 D 称为该函数的定义域, x 和 y 称为自变量, z 称为因变量.

上述定义中,与自变量 x 和 y 的一对值(即二元有序实数组) $(x,y)$ 相对应的因变量 z 的值,也称为 f 在点 $(x,y)$ 处的函数值,记作 $f(x,y)$,即 $z=f(x,y)$. 函数值 $f(x,y)$ 的全体所构成的集合称为函数 f 的值域,记作 $f(D)$,即

$$
f (D) = \{z \mid z = f (x, y), (x, y) \in D \}.
$$

与一元函数的情形相仿, 记号 $f$ 与 $f(x, y)$ 的意义是有区别的, 但习惯上常用记号“$f(x, y), (x, y) \in D$”或“$z = f(x, y), (x, y) \in D$”来表示 $D$ 上的二元函数 $f$. 表示二元函数的记号 $f$ 也是可以任意选取的, 例如也可以记为 $z = \varphi(x, y), z = z(x, y)$ 等.

类似地, 可以定义三元函数 $u = f(x, y, z), (x, y, z) \in D$ 以及三元以上的函数. 一般地, 把定义1中的平面点集 $D$ 换成 $n$ 维空间 $\mathbb{R}^n$ 内的点集 $D$, 映射 $f: D \to \mathbb{R}$ 就称为定义在 $D$ 上的 $n$ 元函数, 通常记为

$$
u = f (x _ {1}, x _ {2}, \dots , x _ {n}), \quad (x _ {1}, x _ {2}, \dots , x _ {n}) \in D,
$$

或简记为

$$
u = f (x), \quad x = (x _ {1}, x _ {2}, \dots , x _ {n}) \in D,
$$

也可记为

$$
u = f (P), \quad P (x _ {1}, x _ {2}, \dots , x _ {n}) \in D.
$$

当 $n = 2$ 或 $n = 3$ 时，习惯上将点 $(x_{1}, x_{2})$ 与点 $(x_{1}, x_{2}, x_{3})$ 分别写成 $(x, y)$ 与 $(x, y, z)$. 这时，若用字母表示 $\mathbf{R}^{2}$ 或 $\mathbf{R}^{3}$ 中的点，即写成 $P(x, y)$ 或 $M(x, y, z)$，则相应的二元函数及三元函数也可简记为 $z = f(P)$ 及 $u = f(M)$.

当 $n = 1$ 时，$n$ 元函数就是一元函数；当 $n \geqslant 2$ 时，$n$ 元函数统称为多元函数.

关于多元函数的定义域,与一元函数相类似,我们作如下约定:在一般地讨论用算式表达的多元函数  $u=f(x)$  时,就以使这个算式有意义的变元 x 的值所组成的点集为这个多元函数的自然定义域.因而,对这类函数,它的定义域不再特别标出.例如,函数  $z=\ln(x+y)$  的定义域为

$$
\{(x, y) \mid x + y > 0 \}
$$

(图 9-2)，这是一个无界开区域。又如，函数  $z=\arcsin(x^{2}+y^{2})$  的定义域为

$$
\{(x, y) \mid x ^ {2} + y ^ {2} \leqslant 1 \}
$$

(图 9-3), 这是一个有界闭区域.

![](images/page_63_image_10.jpg)

<details>
<summary>text_image</summary>

x+y=0
O
x
y
</details>

图9-2

![](images/page_63_image_12.jpg)

<details>
<summary>text_image</summary>

x²+y²=1
O
x
y
</details>

图9-3

设函数 $z = f(x,y)$ 的定义域为 $D$. 对于任意取定的点 $P(x,y) \in D$, 对应的函数值为

$z=f(x,y)$ . 这样, 以 x 为横坐标、y 为纵坐标和  $z=f(x,y)$  为竖坐标在空间就确定一点  $M(x,y,z)$ . 当  $(x,y)$  遍取 D 上的一切点时, 得到一个空间点集

$$
\{(x, y, z) \mid z = f (x, y), (x, y) \in D \},
$$

这个点集称为二元函数 $z = f(x, y)$ 的图形（图9-4）. 通常我们也说二元函数的图形是一张曲面.

例如,由空间解析几何知道,线性函数  $z=ax+by+c$  的图形是一张平面,而函数  $z=x^{2}+y^{2}$  的图形是旋转抛物面.

![](images/page_63_image_19.jpg)

<details>
<summary>text_image</summary>

z
z=f(x,y)
M
O
y
x
P
D
x
</details>

图9-4