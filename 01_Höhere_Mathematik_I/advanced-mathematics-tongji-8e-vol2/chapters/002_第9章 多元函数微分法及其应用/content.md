# 第9章 多元函数微分法及其应用

原始 PDF 第 59–136 页。

# 第九章

# 多元函数微分法及其应用

上册中我们讨论的函数都只有一个自变量,这种函数叫做一元函数.但在很多实际问题中往往牵涉多方面的因素,反映到数学上,就是一个变量依赖于多个变量的情形.这就提出了多元函数以及多元函数的微分和积分问题.本章将在一元函数微分学的基础上,讨论多元函数的微分法及其应用.讨论中我们以二元函数为主,因为从一元函数到二元函数会产生新的问题,而从二元函数到二元以上的多元函数则可以类推.

## 第一节 多元函数的基本概念

## 一、平面点集 $^{*}n$ 维空间

在讨论一元函数时,一些概念、理论和方法都是基于  $R^{1}$  中的点集、两点间的距离、区间和邻域等概念.为了将一元函数微积分推广到多元的情形,首先需要将上述一些概念加以推广,同时还需涉及一些其他概念.为此先引入平面点集的一些基本概念,将有关概念从  $R^{1}$  中的情形推广到  $R^{2}$  中;然后引入 n 维空间,以便推广到一般的  $R^{n}$  中.

## 1. 平面点集

由平面解析几何知道, 当在平面上引入了一个直角坐标系后, 平面上的点 $P$ 与有序二元实数组 $(x, y)$ 之间就建立了一一对应. 于是, 我们常把有序实数组 $(x, y)$ 与平面上的点 $P$ 视作是等同的. 这种建立了坐标系的平面称为坐标平面. 二元有序实数组 $(x, y)$ 的全体, 即 $\mathbf{R}^2 = \mathbf{R} \times \mathbf{R} = \{(x, y) | x, y \in \mathbf{R}\}$ 就表示坐标平面.

坐标平面上具有某种性质 $P$ 的点的集合, 称为平面点集, 记作

52

---

第一节 多元函数的基本概念

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

![](../../raw/pages_0033-0064/images/page_59_image_20.jpg)

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

53

---

第九章 多元函数微分法及其应用

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

$R^{n}$ 中的元素 $(x_{1},x_{2},\cdots,x_{n})$ 有时也用单个字母x来表示,即 $x=(x_{1},x_{2},\cdots,x_{n})$ .当所有的 $x_{i}\quad(i=1,2,\cdots,n)$ 都为零时,称这样的元素为 $R^{n}$ 中的零元,记为0或0.在解析几何中,通过直角坐标系, $R^{2}$ （或 $R^{3}$ ）中的元素分别与平面(或空间)中的点或向量建立一一对应,因而 $R^{n}$ 中的元素 $x=(x_{1},x_{2},\cdots,x_{n})$ 也称为 $R^{n}$ 中的一个点或一个n维向

54

---

第一节 多元函数的基本概念

量, $x_{i}$ 称为点x的第i个坐标或n维向量x的第i个分量.特别地, $R^{n}$ 中的零元0称为 $R^{n}$ 中的坐标原点或n维零向量.

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

55

---

第九章 多元函数微分法及其应用

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

56

---

第一节 多元函数的基本概念

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

![](../../raw/pages_0033-0064/images/page_63_image_10.jpg)

<details>
<summary>text_image</summary>

x+y=0
O
x
y
</details>

图9-2

![](../../raw/pages_0033-0064/images/page_63_image_12.jpg)

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

![](../../raw/pages_0033-0064/images/page_63_image_19.jpg)

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

57

---

第九章 多元函数微分法及其应用

## 三、多元函数的极限

先讨论二元函数 $z = f(x,y)$ 当 $(x,y)\to (x_0,y_0)$，即 $P(x,y)\rightarrow P_0(x_0,y_0)$ 时的极限

这里 $P \to P_0$ 表示点 $P$ 以任何方式趋于点 $P_0$, 也就是点 $P$ 与点 $P_0$ 间的距离趋于零, 即

$$
\mid P P _ {0} \mid = \sqrt {\left(x - x _ {0}\right) ^ {2} + \left(y - y _ {0}\right) ^ {2}} \rightarrow 0.
$$

与一元函数的极限概念类似,如果在  $P(x,y)\rightarrow P_{0}(x_{0},y_{0})$  的过程中,对应的函数值  $f(x,y)$  无限接近于一个确定的常数 A,那么就说 A 是函数  $f(x,y)$  当  $(x,y)\rightarrow(x_{0},y_{0})$  时的极限.下面用“ $\varepsilon-\delta$ ”语言描述这个极限概念.

定义2 设二元函数 $f(P) = f(x, y)$ 的定义域为 $D, P_0(x_0, y_0)$ 是 $D$ 的聚点. 如果存在常数 $A$，对于任意给定的正数 $\varepsilon$，总存在正数 $\delta$，使得当点 $P(x, y) \in D \cap \overset{\circ}{U}(P_0, \delta)$ 时，都有

$$
\mid f (P) - A \mid = \mid f (x, y) - A \mid <   \varepsilon
$$

成立,那么就称常数 A 为函数  $f(x,y)$  当  $(x,y)\rightarrow(x_{0},y_{0})$  时的极限,记作

$$
\lim _ {(x, y) \to (x _ {0}, y _ {0})} f (  x  , y  ) = A \quad \text {或} \quad f (  x  , y  ) \to A   \left(  (  x  , y  ) \to (  x _ {0}  , y _ {0}  )  \right),
$$

也记作

$$
\lim _ {P \to P _ {0}} f (  P) = A \quad \text {或} \quad f (  P) \to A \quad (  P \to P _ {0}  ).
$$

为了区别于一元函数的极限,我们把二元函数的极限叫做二重极限.

例4 设 $f(x,y) = (x^{2} + y^{2})\sin \frac{1}{x^{2} + y^{2}}$ ，求证:

$$
\lim _ {(x, y) \to (0, 0)} f (x, y) = 0.
$$

证 这里函数 $f(x, y)$ 的定义域为 $D = \mathbb{R}^2 \setminus \{(0, 0)\}$，点 $O(0, 0)$ 为 $D$ 的聚点。因为

$$
\mid f (x, y) - 0 \mid = \left| (x ^ {2} + y ^ {2}) \sin \frac {1}{x ^ {2} + y ^ {2}} - 0 \right| \leqslant x ^ {2} + y ^ {2},
$$

可见， $\forall \varepsilon >0$ ，取 $\delta = \sqrt{\varepsilon}$ ，则当

$$
0 <   \sqrt {(x - 0) ^ {2} + (y - 0) ^ {2}} <   \delta ,
$$

即 $P(x,y)\in D\cap \mathring{U} (O,\delta)$ 时，总有

$$
\mid f (x, y) - 0 \mid <   \varepsilon
$$

成立,所以

$$
\lim _ {(x, y) \to (0, 0)} f (x, y) = 0.
$$

必须注意,所谓二重极限存在,是指  $P(x,y)$  以任何方式趋于  $P_{0}(x_{0},y_{0})$  时,  $f(x,y)$  都无限接近于 A. 因此, 如果  $P(x,y)$  以某一特殊方式, 例如沿着一条定直线或

58

---

第一节 多元函数的基本概念

定曲线趋于 $P_0(x_0, y_0)$ 时，即使 $f(x, y)$ 无限接近于某一确定值，我们还不能由此断定函数的极限存在。但是反过来，如果当 $P(x, y)$ 以不同的方式趋于 $P_0(x_0, y_0)$ 时，$f(x, y)$ 趋于不同的值，那么就可以断定这函数的极限不存在。下面用例子来说明这种情形。

考察函数

$$
f (x, y) = \left\{ \begin{array}{l l} \frac {x y}{x ^ {2} + y ^ {2}}, & x ^ {2} + y ^ {2} \neq 0, \\ 0, & x ^ {2} + y ^ {2} = 0. \end{array} \right.
$$

显然, 当点  $P(x,y)$  沿 x 轴趋于点  $(0,0)$  时,

$$
\lim_{\substack{(x,y)\to (0,0)\\ y = 0}}f(x,y) = \lim_{x\to 0}f(x,0) = \lim_{x\to 0}0 = 0;
$$

又当点  $P(x,y)$  沿 y 轴趋于点  $(0,0)$  时，

$$
\lim_{\substack{(x,y)\to (0,0)\\ x = 0}}f(x,y) = \lim_{y\to 0}f(0,y) = \lim_{y\to 0}0 = 0.
$$

虽然点 $P(x,y)$ 以上述两种特殊方式（沿 $x$ 轴或沿 $y$ 轴）趋于原点时函数的极限存在并且相等，但是 $\lim_{(x,y)\to (0,0)}f(x,y)$ 并不存在.这是因为当点 $P(x,y)$ 沿着直线 $y = kx$ 趋于点(0,0)时，有

$$
\lim_{\substack{(x,y)\to (0,0)\\ y = kx}}\frac{xy}{x^2 + y^2} = \lim_{x\to 0}\frac{kx^2}{x^2 + k^2x^2} = \frac{k}{1 + k^2},
$$

显然它是随着 k 的值的不同而改变的.

以上关于二元函数的极限概念, 可相应地推广到 n 元函数  $u = f(P)$ , 即  $u = f(x_{1}, x_{2}, \cdots, x_{n})$  上去.

关于多元函数的极限运算,有与一元函数类似的运算法则.

例 5 求  $\lim_{(x,y)\to(0,2)}\frac{\sin(xy)}{x}$ .

解 这里函数 $\frac{\sin(xy)}{x}$ 的定义域为 $D = \{(x, y) \mid x \neq 0, y \in \mathbb{R}\}, P_0(0, 2)$ 为 $D$ 的聚点.

由积的极限运算法则,得

$$
\lim _ {(x, y) \to (0, 2)} \frac {\sin (x y)}{x} = \lim _ {(x, y) \to (0, 2)} \left[ \frac {\sin (x y)}{x y} \cdot y \right] = \lim _ {x y \to 0} \frac {\sin (x y)}{x y} \cdot \lim _ {y \to 2} y = 1 \times 2 = 2.
$$

## 四、多元函数的连续性

明白了函数极限的概念,就不难说明多元函数的连续性.

定义3 设二元函数 $f(P) = f(x, y)$ 的定义域为 $D, P_0(x_0, y_0)$ 为 $D$ 的聚点，且 $P_0 \in$

例题精讲
9-1

59

---

第九章 多元函数微分法及其应用

## D. 如果

$$
\lim _ {(x, y) \to (x _ {0}, y _ {0})} f (x, y) = f (x _ {0}, y _ {0}),
$$

那么称函数 $f(x,y)$ 在点 $P_0(x_0,y_0)$ 连续.

设函数 $f(x,y)$ 在D上有定义，D内的每一点都是函数定义域的聚点.如果函数 $f(x,y)$ 在D的每一点都连续，那么就称函数 $f(x,y)$ 在D上连续，或者称 $f(x,y)$ 是D上的连续函数.

以上关于二元函数的连续性概念, 可相应地推广到 n 元函数  $f(P)$  上去.

下面,我们把一元基本初等函数看成二元函数的特例(即另一个自变量不出现),来讨论它的连续性.先看一个例子.

例6 设 $f(x,y) = \sin x$ ，证明 $f(x,y)$ 是 $\mathbb{R}^2$ 上的连续函数.

证 设 $P_0(x_0, y_0) \in \mathbb{R}^2$. $\forall \varepsilon > 0$, 由于 $\sin x$ 在 $x_0$ 处连续, 故 $\exists \delta > 0$, 当 $|x - x_0| < \delta$ 时, 有

$$
\mid \sin x - \sin x _ {0} \mid <   \varepsilon .
$$

以上述 $\delta$ 作 $P_0$ 的 $\delta$ 邻域 $U(P_0, \delta)$，则当 $P(x, y) \in U(P_0, \delta)$ 时，显然

$$
\mid x - x _ {0} \mid \leqslant \rho (P, P _ {0}) <   \delta ,
$$

从而

$$
\mid f (x, y) - f (x _ {0}, y _ {0}) \mid = \mid \sin x - \sin x _ {0} \mid <   \varepsilon ,
$$

即 $f(x,y) = \sin x$ 在点 $P_0(x_0,y_0)$ 连续.由 $P_{0}$ 的任意性知，$\sin x$ 作为 $x,y$ 的二元函数在 $\mathbf{R}^2$ 上连续.

类似的讨论可知,一元基本初等函数看成二元函数或二元以上的多元函数时,它们在各自的定义域内都是连续的.

定义4 设函数 $f(x, y)$ 的定义域为 $D, P_0(x_0, y_0)$ 是 $D$ 的聚点. 如果函数 $f(x, y)$ 在点 $P_0(x_0, y_0)$ 不连续, 那么称 $P_0(x_0, y_0)$ 为函数 $f(x, y)$ 的间断点.

例如,前面讨论过的函数

$$
f (x, y) = \left\{ \begin{array}{c l} \frac {x y}{x ^ {2} + y ^ {2}}, & x ^ {2} + y ^ {2} \neq 0, \\ 0, & x ^ {2} + y ^ {2} = 0, \end{array} \right.
$$

其定义域 $D = \mathbb{R}^2$ ，点 $O(0,0)$ 是 $D$ 的聚点. $f(x,y)$ 当 $(x,y)\rightarrow (0,0)$ 时的极限不存在，所以点 $O(0,0)$ 是该函数的一个间断点；又如函数

$$
f (x, y) = \sin \frac {1}{x ^ {2} + y ^ {2} - 1},
$$

其定义域为

$$
D = \{(x, y) \mid x ^ {2} + y ^ {2} \neq 1 \},
$$

60

---

第一节 多元函数的基本概念

圆周 $C = \{(x,y)\mid x^2 +y^2 = 1\}$ 上的点都是 $D$ 的聚点，而 $f(x,y)$ 在 $C$ 上没有定义，当然$f(x,y)$ 在 $C$ 上各点都不连续，所以圆周 $C$ 上各点都是该函数的间断点.

前面已经指出:一元函数中关于极限的运算法则,对于多元函数仍然适用.根据多元函数的极限运算法则,可以证明多元连续函数的和、差、积仍为连续函数;连续函数的商在分母不为零处仍连续;多元连续函数的复合函数也是连续函数.

与一元初等函数相类似,多元初等函数是指可用一个式子表示的多元函数,这个式子是由常数及具有不同自变量的一元基本初等函数经过有限次的四则运算和复合运算而得到的.例如, $\frac{x+x^{2}-y^{2}}{1+y^{2}},\sin(x+y),e^{x^{2}+y^{2}+z^{2}}$ 等都是多元初等函数.

根据上面指出的连续函数的和、差、积、商的连续性以及连续函数的复合函数的连续性,再利用基本初等函数的连续性,我们进一步可以得出如下结论:

一切多元初等函数在其定义区域内是连续的.所谓定义区域是指包含在定义域内的区域或闭区域.

由多元初等函数的连续性,如果要求它在点 $P_{0}$ 处的极限,而该点又在此函数的定义区域内,那么此极限值就是函数在该点的函数值,即

$$
\lim _ {P \to P _ {0}} f (P) = f (P _ {0}).
$$

例7 求 $\lim_{(x,y)\to (1,2)}\frac{x + y}{xy}$.

解 函数 $f(x, y) = \frac{x + y}{xy}$ 是初等函数, 它的定义域为

$$
D = \{(x, y) \mid x \neq 0, y \neq 0 \}.
$$

$P_{0}(1,2)$ 为 $D$ 的内点，故存在 $P_{0}$ 的某一邻域 $U(P_0)\subset D$ ，而任何邻域都是区域，所以$U(P_0)$ 是 $f(x,y)$ 的一个定义区域，因此

$$
\lim _ {(x, y) \to (1, 2)} \frac {x + y}{x y} = f (1, 2) = \frac {3}{2}.
$$

一般地, 求  $\lim_{P\to P_{0}}f(P)$  时, 如果  $f(P)$  是初等函数, 且  $P_{0}$  是  $f(P)$  的定义域的内点, 那么  $f(P)$  在点  $P_{0}$  处连续, 于是

$$
\lim _ {P \to P _ {0}} f (P) = f (P _ {0}).
$$

例8 求 $\lim_{(x,y)\to (0,0)}\frac{\sqrt{xy + 1} - 1}{xy}$

解 $\lim_{(x,y)\to (0,0)}\frac{\sqrt{xy + 1} - 1}{xy} = \lim_{(x,y)\to (0,0)}\frac{xy + 1 - 1}{xy(\sqrt{xy + 1} + 1)} = \lim_{(x,y)\to (0,0)}\frac{1}{\sqrt{xy + 1} + 1} = \frac{1}{2}.$

以上运算的最后一步用到了二元函数 $\frac{1}{\sqrt{xy+1}+1}$ 在点(0,0)的连续性.

61

---

第九章 多元函数微分法及其应用

与闭区间上一元连续函数的性质相类似,在有界闭区域上连续的多元函数具有如下性质:

性质1(有界性与最大值最小值定理) 在有界闭区域 $D$ 上的多元连续函数, 必定在 $D$ 上有界, 且能取得它的最大值和最小值.

性质1就是说,若 $f(P)$ 在有界闭区域D上连续,则必定存在常数M>0,使得对一切 $P\in D$ ,有 $\left|f(P)\right|\leqslant M$ ;且存在 $P_{1},P_{2}\in D$ ,使得

$$
f (P _ {1}) = \max \left\{f (P) \mid P \in D \right\}, \quad f (P _ {2}) = \min \left\{f (P) \mid P \in D \right\}.
$$

性质 2(介值定理) 在有界闭区域 D 上的多元连续函数必取得介于最大值和最小值之间的任何值.

\*性质3(一致连续性定理) 在有界闭区域 $D$ 上的多元连续函数必定在 $D$ 上一致连续.

性质3就是说,若 $f(P)$ 在有界闭区域D上连续,则对于任意给定的正数 $\varepsilon$ ,总存在正数 $\delta$ ,使得对于D上的任意两点 $P_{1},P_{2}$ ,只要当 $|P_{1}P_{2}|<\delta$ 时,都有

$$
\mid f (P _ {1}) - f (P _ {2}) \mid <   \varepsilon
$$

成立.

## 习题9-1

1. 判定下列平面点集中哪些是开集、闭集、区域、有界集、无界集，并分别指出它们的聚点所成的点集（称为导集）和边界.

(1)  $\{(x,y)\mid x\neq0,y\neq0\}$ ;

(2) $\{(x,y)\mid1<x^{2}+y^{2}\leqslant4\}$ ;

(3)  $\{(x,y)\mid y>x^{2}\}$ ;

(4) $\{(x, y) \mid x^2 + (y - 1)^2 \geqslant 1\} \cap \{(x, y) \mid x^2 + (y - 2)^2 \leqslant 4\}$.

2. 已知函数 $f(x, y) = x^2 + y^2 - xy \tan \frac{x}{y}$，试求 $f(tx, ty)$.

3. 试证函数 $F(x, y) = \ln x \cdot \ln y$ 满足关系式

$$
F (x y, u v) = F (x, u) + F (x, v) + F (y, u) + F (y, v).
$$

4. 已知函数 $f(u, v, w) = u^w + w^{u + v}$，试求 $f(x + y, x - y, xy)$.

5. 求下列各函数的定义域:

(1) $z = \ln (y^2 - 2x + 1)$;

(2) $z = \frac{1}{\sqrt{x + y}} +\frac{1}{\sqrt{x - y}};$

(3) $z=\sqrt{x-\sqrt{y}}$;

(4) $z = \ln (y - x) + \frac{\sqrt{x}}{\sqrt{1 - x^2 - y^2}};$

(5) $u = \sqrt{R^2 - x^2 - y^2 - z^2} + \frac{1}{\sqrt{x^2 + y^2 + z^2 - r^2}}$ ($R > r > 0$);

(6) $u = \arccos \frac{z}{\sqrt{x^2 + y^2}}.$

62

---

第二节 偏导数

6. 求下列各极限:

(1) $\lim_{(x,y)\to (0,1)}\frac{1 - xy}{x^2 + y^2};$

(2) $\lim_{(x,y)\to (1,0)}\frac{\ln(x + e^y)}{\sqrt{x^2 + y^2}};$

(3)  $\lim_{(x,y)\to(0,0)}\frac{2-\sqrt{xy+4}}{xy};$

(4) $\lim_{(x,y)\to (0,0)}\frac{xy}{\sqrt{2 - e^{xy}} - 1};$

(5) $\lim_{(x,y)\to (2,0)}\frac{\tan(xy)}{y};$

(6) $\lim_{(x,y)\to (0,0)}\frac{1 - \cos(x^2 + y^2)}{(x^2 + y^2)e^{x^2y^2}}.$

\*7. 证明下列极限不存在:

(1)  $\lim_{(x,y)\to(0,0)}\frac{x+y}{x-y};$

(2)  $\lim_{(x,y)\to(0,0)}\frac{x^{2}y^{2}}{x^{2}y^{2}+(x-y)^{2}};$

(3) $\lim_{(x,y)\to (0,0)}\frac{xy}{x + y};$

(4) $\lim_{(x,y)\to (0,0)}\frac{1 - \cos(x + y)}{(x + y)xy}.$

8. 函数 $z = \frac{y^2 + 2x}{y^2 - 2x}$ 在何处是间断的？

\*9. 证明 $\lim_{(x,y)\to (0,0)}\frac{xy}{\sqrt{x^2 + y^2}} = 0.$

\*10. 设 $F(x, y) = f(x)$, $f(x)$ 在点 $x_0$ 处连续, 证明: 对任意 $y_0 \in \mathbb{R}$, $F(x, y)$ 在点 $(x_0, y_0)$ 处连续.

## 第二节 偏导数

## 一、偏导数的定义及其计算法

在研究一元函数时,我们从研究函数的变化率引入了导数的概念.对于多元函数同样需要讨论它的变化率.但多元函数的自变量不止一个,因变量与自变量的关系要比一元函数复杂得多.在这一节里,我们首先考虑多元函数关于其中一个自变量的变化率.以二元函数 $z=f(x,y)$ 为例,如果只有自变量x变化,而自变量y固定(即看做常量),这时它就是x的一元函数,这函数对x的导数,就称为二元函数 $z=f(x,y)$ 对x的偏导数,即有如下定义:

定义 设函数 $z = f(x, y)$ 在点 $(x_0, y_0)$ 的某一邻域内有定义，当 $y$ 固定在 $y_0$ 而 $x$ 在 $x_0$ 处有增量 $\Delta x$ 时，相应的函数有增量

$$
f (x _ {0} + \Delta x, y _ {0}) - f (x _ {0}, y _ {0}),
$$

如果

$$
\lim _ {\Delta x \to 0} \frac {f (x _ {0} + \Delta x , y _ {0}) - f (x _ {0} , y _ {0})}{\Delta x} \tag {2-1}
$$

存在,那么称此极限为函数  $z=f(x,y)$  在点  $(x_{0},y_{0})$  处对 x 的偏导数,记作

63

---

第九章 多元函数微分法及其应用

$$
\frac {\partial z}{\partial x} \Bigg | _ {x = x _ {0}, y = y _ {0}}, \quad \frac {\partial f}{\partial x} \Bigg | _ {x = x _ {0}, y = y _ {0}}, \quad z _ {x} \Bigg | _ {x = x _ {0}, y = y _ {0}} \quad \text {或} \quad f _ {x} (x _ {0}, y _ {0}). ①
$$

例如,极限(2-1)可以表示为

$$
f _ {x} (x _ {0}, y _ {0}) = \lim _ {\Delta x \to 0} \frac {f (x _ {0} + \Delta x , y _ {0}) - f (x _ {0} , y _ {0})}{\Delta x}. \tag {2-2}
$$

类似地, 函数  $z=f(x,y)$  在点  $(x_{0},y_{0})$  处对 y 的偏导数定义为

$$
\lim _ {\Delta y \to 0} \frac {f (x _ {0} , y _ {0} + \Delta y) - f (x _ {0} , y _ {0})}{\Delta y}, \tag {2-3}
$$

记作

$$
\frac {\partial z}{\partial y} \Bigg | _ x = x _ {0}, \quad \frac {\partial f}{\partial y} \Bigg | _ {x = x _ {0}, \quad z _ {y}} \Bigg | _ {x = x _ {0} \atop y = y _ {0}} \quad \text {或} \quad f _ {y} (x _ {0}, y _ {0}).
$$

如果函数 $z = f(x,y)$ 在区域 $D$ 内每一点 $(x,y)$ 处对 $x$ 的偏导数都存在，那么这个偏导数就是 $x,y$ 的函数，它就称为函数 $z = f(x,y)$ 对自变量 $x$ 的偏导函数，记作

$$
\frac {\partial z}{\partial x}, \quad \frac {\partial f}{\partial x}, \quad z _ {x} \quad \text {或} \quad f _ {x} (x, y).
$$

类似地,可以定义函数  $z=f(x,y)$  对自变量 y 的偏导函数,记作

$$
\frac {\partial z}{\partial y}, \quad \frac {\partial f}{\partial y}, \quad z _ {y} \quad \text {或} \quad f _ {y} (x, y).
$$

由偏导函数的概念可知， $f(x,y)$  在点 $(x_{0},y_{0})$ 处对 x 的偏导数 $f_{x}(x_{0},y_{0})$ 显然就是偏导函数 $f_{x}(x,y)$ 在点 $(x_{0},y_{0})$ 处的函数值； $f_{y}(x_{0},y_{0})$ 就是偏导函数 $f_{y}(x,y)$ 在点 $(x_{0},y_{0})$ 处的函数值。就像一元函数的导函数一样，以后在不至于混淆的地方也把偏导函数简称为偏导数。

至于实际求 $z = f(x, y)$ 的偏导数，并不需要用新的方法，因为这里只有一个自变量在变动，另一个自变量是看做固定的，所以仍旧是一元函数的微分法问题。求 $\frac{\partial f}{\partial x}$ 时，只要把 $y$ 暂时看做常量而对 $x$ 求导数；求 $\frac{\partial f}{\partial y}$ 时，只要把 $x$ 暂时看做常量而对 $y$ 求导数。

偏导数的概念还可推广到二元以上的函数.例如三元函数 $u = f(x,y,z)$ 在点 $(x,y,z)$ 处对 $x$ 的偏导数定义为

$$
f _ {x} (x, y, z) = \lim _ {\Delta x \to 0} \frac {f (x + \Delta x , y , z) - f (x , y , z)}{\Delta x},
$$

其中 $(x,y,z)$ 是函数 $u = f(x,y,z)$ 的定义域的内点. 它们的求法也仍旧是一元函数的微分法问题.

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 偏导数记号 $z_{x}, f_{x}$ 也记成 $z_{x}^{\prime}, f_{x}^{\prime}$, 下面高阶偏导数的记号也有类似的情形.</span></small>

64

---

第二节 偏导数

例1 求 $z = x^{2} + 3xy + y^{2}$ 在点(1,2)处的偏导数.

解 把 y 看做常量, 得

$$
\frac {\partial z}{\partial x} = 2 x + 3 y;
$$

把 x 看做常量, 得

$$
\frac {\partial z}{\partial y} = 3 x + 2 y.
$$

将 $(1,2)$ 代入上面的结果,就得

$$
\frac{\partial z}{\partial x}\bigg|_{\substack{x = 1\\ y = 2}} = 2\times 1 + 3\times 2 = 8,\quad \frac{\partial z}{\partial y}\bigg|_{\substack{x = 1\\ y = 2}} = 3\times 1 + 2\times 2 = 7.
$$

例 2 求  $z=x^{2}\sin 2y$  的偏导数.

解  $\frac{\partial z}{\partial x}=2x\sin 2y,\quad\frac{\partial z}{\partial y}=2x^{2}\cos 2y.$

例3 设 $z = x^{y}$ ($x > 0, x \neq 1$), 求证: $\frac{x}{y} \frac{\partial z}{\partial x} + \frac{1}{\ln x} \frac{\partial z}{\partial y} = 2z$.

证 因为 $\frac{\partial z}{\partial x}=yx^{y-1},\frac{\partial z}{\partial y}=x^{y}\ln x.$ 所以

$$
\frac {x}{y} \frac {\partial z}{\partial x} + \frac {1}{\ln x} \frac {\partial z}{\partial y} = \frac {x}{y} y x ^ {y - 1} + \frac {1}{\ln x} x ^ {y} \ln x = x ^ {y} + x ^ {y} = 2 z.
$$

例 4 求  $r=\sqrt{x^{2}+y^{2}+z^{2}}$  的偏导数.

解 把 y 和 z 都看做常量, 得

$$
\frac {\partial r}{\partial x} = \frac {x}{\sqrt {x ^ {2} + y ^ {2} + z ^ {2}}} = \frac {x}{r}.
$$

由于所给函数关于自变量的对称性①,所以

$$
\frac {\partial r}{\partial y} = \frac {y}{r}, \quad \frac {\partial r}{\partial z} = \frac {z}{r}.
$$

例 5 已知理想气体的状态方程 pV = RT (R 为常量), 求证:

$$
\frac {\partial p}{\partial V} \cdot \frac {\partial V}{\partial T} \cdot \frac {\partial T}{\partial p} = - 1.
$$

证 因为

$$
p = \frac {R T}{V}, \quad \frac {\partial p}{\partial V} = - \frac {R T}{V ^ {2}};
$$

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 这就是说,当函数表达式中任意两个自变量对调后,仍表示原来的函数.</span></small>

65

---

第九章 多元函数微分法及其应用

$$
\begin{array}{l} V = \frac {R T}{p}, \quad \frac {\partial V}{\partial T} = \frac {R}{p}; \\ T = \frac {p V}{R}, \quad \frac {\partial T}{\partial p} = \frac {V}{R}, \\ \end{array}
$$

所以

$$
\frac {\partial p}{\partial V} \cdot \frac {\partial V}{\partial T} \cdot \frac {\partial T}{\partial p} = - \frac {R T}{V ^ {2}} \cdot \frac {R}{p} \cdot \frac {V}{R} = - \frac {R T}{p V} = - 1.
$$

我们知道,对一元函数来说, $\frac{dy}{dx}$ 可看做函数的微分dy与自变量的微分dx之商.而上式表明,偏导数的记号是一个整体记号,不能看做分子与分母之商.

二元函数 $z = f(x,y)$ 在点 $(x_0,y_0)$ 的偏导数有下述几何意义.

设 $M_0(x_0, y_0, f(x_0, y_0))$ 为曲面 $z = f(x, y)$ 上的一点，过 $M_0$ 作平面 $y = y_0$，截此曲面得一曲线，此曲线在平面 $y = y_0$ 上的方程为 $z = f(x, y_0)$，则导数 $\frac{\mathrm{d}}{\mathrm{d}x} f(x, y_0) \Bigg|_{x = x_0}$，即偏导数 $f_x(x_0, y_0)$，就是这曲线在点 $M_0$ 处的切线 $M_0 T_x$ 对 $x$ 轴的斜率（图9-5）。同样，偏导数 $f_y(x_0, y_0)$ 的几何意义是曲面被平面 $x = x_0$ 所截得的曲线在点 $M_0$ 处的切线 $M_0 T_y$ 对 $y$ 轴的斜率。

![](../../raw/pages_0065-0096/images/page_72_image_7.jpg)

<details>
<summary>text_image</summary>

z=f(x₀,y)
M₀
Tₓ
y₀
x₀
O
z=f(x,y₀)
y
</details>

图9-5

我们已经知道,如果一元函数在某点具有导数,那么它在该点必定连续.但对于多元函数来说,即使各偏导数在某点都存在,也不能保证函数在该点连续.这是因为各偏导数存在只能保证点P沿着平行于坐标轴的方向趋于 $P_{0}$ 时,函数值 $f(P)$ 趋于 $f(P_{0})$ ,但不能保证点P按任何方式趋于 $P_{0}$ 时,函数值 $f(P)$ 都趋于 $f(P_{0})$ .例如,函数

$$
z = f (x, y) = \left\{ \begin{array}{l l} \frac {x y}{x ^ {2} + y ^ {2}}, & x ^ {2} + y ^ {2} \neq 0, \\ 0, & x ^ {2} + y ^ {2} = 0 \end{array} \right.
$$

在点(0,0)处对 $x$ 的偏导数为

$$
f _ {x} (0, 0) = \lim _ {\Delta x \to 0} \frac {f (0 + \Delta x , 0) - f (0 , 0)}{\Delta x} = \lim _ {\Delta x \to 0} 0 = 0;
$$

释疑解难

9-1

同样有

$$
f _ {y} (0, 0) = \lim _ {\Delta y \to 0} \frac {f (0 , 0 + \Delta y) - f (0 , 0)}{\Delta y} = \lim _ {\Delta y \to 0} 0 = 0.
$$

66

---

第二节 偏导数

但是在第一节中已经知道这函数在点 $(0,0)$ 并不连续.

## 二、高阶偏导数

设函数 $z = f(x,y)$ 在区域 $D$ 内具有偏导数

$$
\frac {\partial z}{\partial x} = f _ {x} (x, y), \quad \frac {\partial z}{\partial y} = f _ {y} (x, y),
$$

于是在 $D$ 内 $f_{x}(x,y), f_{y}(x,y)$ 都是 $x, y$ 的函数. 如果这两个函数的偏导数也存在, 那么称它们是函数 $z = f(x,y)$ 的二阶偏导数. 按照对变量求导次序的不同有下列四个二阶偏导数:

$$
\begin{array}{l} \frac {\partial}{\partial x} \left(\frac {\partial z}{\partial x}\right) = \frac {\partial^ {2} z}{\partial x ^ {2}} = f _ {x x} (x, y), \quad \frac {\partial}{\partial y} \left(\frac {\partial z}{\partial x}\right) = \frac {\partial^ {2} z}{\partial x \partial y} = f _ {x y} (x, y), \\ \frac {\partial}{\partial x} \Bigg (\frac {\partial z}{\partial y} \Bigg) = \frac {\partial^ {2} z}{\partial y \partial x} = f _ {y x} (x, y), \quad \frac {\partial}{\partial y} \Bigg (\frac {\partial z}{\partial y} \Bigg) = \frac {\partial^ {2} z}{\partial y ^ {2}} = f _ {y y} (x, y). \\ \end{array}
$$

其中第二、三两个偏导数称为混合偏导数. 同样可得三阶、四阶……以及 n 阶偏导数. 二阶及二阶以上的偏导数统称为高阶偏导数.

例6 设 $z = x^{3}y^{2} - 3xy^{3} - xy + 1$，求 $\frac{\partial^2z}{\partial x^2}, \frac{\partial^2z}{\partial y\partial x}, \frac{\partial^2z}{\partial x\partial y}, \frac{\partial^2z}{\partial y^2}$ 及 $\frac{\partial^3z}{\partial x^3}$.

解 $\frac{\partial z}{\partial x} = 3x^{2}y^{2} - 3y^{3} - y,$ $\frac{\partial z}{\partial y} = 2x^3 y - 9xy^2 -x;$

$$
\frac {\partial^ {2} z}{\partial x ^ {2}} = 6 x y ^ {2}, \quad \frac {\partial^ {2} z}{\partial y \partial x} = 6 x ^ {2} y - 9 y ^ {2} - 1, \quad \frac {\partial^ {2} z}{\partial x \partial y} = 6 x ^ {2} y - 9 y ^ {2} - 1, \quad \frac {\partial^ {2} z}{\partial y ^ {2}} = 2 x ^ {3} - 1 8 x y;
$$

$$
\frac {\partial^ {3} z}{\partial x ^ {3}} = 6 y ^ {2}.
$$

我们看到例6中两个二阶混合偏导数相等, 即 $\frac{\partial^2 z}{\partial y \partial x} = \frac{\partial^2 z}{\partial x \partial y}$. 这不是偶然的, 事实上, 有下述定理.

定理 如果函数 $z = f(x, y)$ 的两个二阶混合偏导数 $\frac{\partial^2 z}{\partial y \partial x}$ 及 $\frac{\partial^2 z}{\partial x \partial y}$ 在区域 $D$ 内连续，那么在该区域内这两个二阶混合偏导数必相等.

换句话说,二阶混合偏导数在连续的条件下与求导的次序无关.这定理的证明从略.

对于二元以上的函数,也可以类似地定义高阶偏导数,而且高阶混合偏导数在偏导数连续的条件下也与求导的次序无关.

例7 验证函数 $z = \ln \sqrt{x^2 + y^2}$ 满足方程

67

---

第九章 多元函数微分法及其应用

$$
\frac {\partial^ {2} z}{\partial x ^ {2}} + \frac {\partial^ {2} z}{\partial y ^ {2}} = 0.
$$

证 因为 $z = \ln \sqrt{x^2 + y^2} = \frac{1}{2}\ln (x^2 +y^2)$ ，所以

$$
\frac {\partial z}{\partial x} = \frac {x}{x ^ {2} + y ^ {2}}, \quad \frac {\partial z}{\partial y} = \frac {y}{x ^ {2} + y ^ {2}},
$$

$$
\frac {\partial^ {2} z}{\partial x ^ {2}} = \frac {(x ^ {2} + y ^ {2}) - x \cdot 2 x}{(x ^ {2} + y ^ {2}) ^ {2}} = \frac {y ^ {2} - x ^ {2}}{(x ^ {2} + y ^ {2}) ^ {2}}, \quad \frac {\partial^ {2} z}{\partial y ^ {2}} = \frac {(x ^ {2} + y ^ {2}) - y \cdot 2 y}{(x ^ {2} + y ^ {2}) ^ {2}} = \frac {x ^ {2} - y ^ {2}}{(x ^ {2} + y ^ {2}) ^ {2}}.
$$

因此

$$
\frac {\partial^ {2} z}{\partial x ^ {2}} + \frac {\partial^ {2} z}{\partial y ^ {2}} = \frac {y ^ {2} - x ^ {2}}{(x ^ {2} + y ^ {2}) ^ {2}} + \frac {x ^ {2} - y ^ {2}}{(x ^ {2} + y ^ {2}) ^ {2}} = 0.
$$

例8 证明函数 $u = \frac{1}{r}$ 满足方程

$$
\frac {\partial^ {2} u}{\partial x ^ {2}} + \frac {\partial^ {2} u}{\partial y ^ {2}} + \frac {\partial^ {2} u}{\partial z ^ {2}} = 0,
$$

其中  $r=\sqrt{x^{2}+y^{2}+z^{2}}$ .

证 $\frac{\partial u}{\partial x} = -\frac{1}{r^2}\frac{\partial r}{\partial x} = -\frac{1}{r^2}\cdot \frac{x}{r} = -\frac{x}{r^3},$

$$
\frac {\partial^ {2} u}{\partial x ^ {2}} = - \frac {1}{r ^ {3}} + \frac {3 x}{r ^ {4}} \cdot \frac {\partial r}{\partial x} = - \frac {1}{r ^ {3}} + \frac {3 x ^ {2}}{r ^ {5}}.
$$

因为函数关于自变量的对称性,所以

$$
\frac {\partial^ {2} u}{\partial y ^ {2}} = - \frac {1}{r ^ {3}} + \frac {3 y ^ {2}}{r ^ {5}}, \quad \frac {\partial^ {2} u}{\partial z ^ {2}} = - \frac {1}{r ^ {3}} + \frac {3 z ^ {2}}{r ^ {5}}.
$$

因此

$$
\frac {\partial^ {2} u}{\partial x ^ {2}} + \frac {\partial^ {2} u}{\partial y ^ {2}} + \frac {\partial^ {2} u}{\partial z ^ {2}} = - \frac {3}{r ^ {3}} + \frac {3 (x ^ {2} + y ^ {2} + z ^ {2})}{r ^ {5}} = - \frac {3}{r ^ {3}} + \frac {3 r ^ {2}}{r ^ {5}} = 0.
$$

例 7 和例 8 中的两个方程都叫做拉普拉斯(Laplace)方程, 它是数学物理方程中一种很重要的方程.

## 习题9-2

1. 设 $f(x,y)=\mathrm{e}^{\sqrt{x^{2+y^{4}}} }$, 求 $f_{x}(0,0)$, $f_{y}(0,0)$.
2. 求下列函数的偏导数:

(1) $z = x^{3}y - y^{3}x$;

(2) $s = \frac{u^2 + v^2}{uv}$;

(3) $z = \sqrt{\ln(xy)}$;

(4)  $z=\sin(xy)+\cos^{2}(xy)$ ;

68

---

第三节 全微分

(5)  $z=\ln\tan\frac{x}{y};$

(6) $z = (1 + xy)^y$;

(7) $u = x^{\frac{y}{z}}$;

(8)  $u = \arctan(x - y)^{z}$ .

3. 设 $T = 2\pi \sqrt{\frac{l}{g}}$, 求证 $l\frac{\partial T}{\partial l} + g\frac{\partial T}{\partial g} = 0$.

4. 设  $z = e^{-\left(\frac{1}{x} + \frac{1}{y}\right)}$ ，求证  $x^{2} \frac{\partial z}{\partial x} + y^{2} \frac{\partial z}{\partial y} = 2z.$

5. 设 $f(x,y)=x+(y-1)\arcsin\sqrt{\frac{x}{y}}$ ，求 $f_{x}(x,1)$ .

6. 求曲线  $\left\{\begin{aligned} z &= \frac{x^{2} + y^{2}}{4}, \\ y &= 4 \end{aligned}\right.$  在点(2,4,5)处的切线对于 x 轴的倾角.

7. 求下列函数的 $\frac{\partial^{2}z}{\partial x^{2}},\frac{\partial^{2}z}{\partial y^{2}}$ 和 $\frac{\partial^{2}z}{\partial x\partial y}$:

(1) $z = x^{4} + y^{4} - 4x^{2}y^{2}$;

(2)  $z = \arctan \frac{y}{x}$ ;

(3)  $z = y^{x}$ .

8. 设 $f(x, y, z) = xy^2 + yz^2 + zx^2$，求 $f_{xx}(0, 0, 1), f_{xz}(1, 0, 2), f_{yz}(0, -1, 0)$ 及 $f_{zx}(2, 0, 1)$.

9. 设 $z = x \ln (xy)$, 求 $\frac{\partial^3 z}{\partial x^2 \partial y}$ 及 $\frac{\partial^3 z}{\partial x \partial y^2}$.

10. 验证:

(1) $y=e^{-kn^{2}t}\sin nx$ 满足 $\frac{\partial y}{\partial t}=k\frac{\partial^{2}y}{\partial x^{2}};$

(2) $r = \sqrt{x^2 + y^2 + z^2}$ 满足 $\frac{\partial^2r}{\partial x^2} + \frac{\partial^2r}{\partial y^2} + \frac{\partial^2r}{\partial z^2} = \frac{2}{r}$.

## 第三节 全微分

## 一、全微分的定义

由偏导数的定义知道,二元函数对某个自变量的偏导数表示当另一个自变量固定时,因变量相对于该自变量的变化率.根据一元函数微分学中增量与微分的关系,可得

$$
f (x + \Delta x, y) - f (x, y) \approx f _ {x} (x, y) \Delta x,
$$

$$
f (x, y + \Delta y) - f (x, y) \approx f _ {y} (x, y) \Delta y.
$$

上面两式的左端分别叫做二元函数对 x 和对 y 的偏增量,而右端分别叫做二元函数对

x 和对 y 的偏微分.
在实际问题中,有时需要研究多元函数中各个自变量都取得增量时因变量所获得的增量,即所谓全增量的问题.下面以二元函数为例进行讨论.
设函数  $z=f(x,y)$  在点  $P(x,y)$  的某邻域内有定义, $P'(x+\Delta x,y+\Delta y)$  为这邻域内的

69

---

第九章 多元函数微分法及其应用

任意一点,则称这两点的函数值之差 $f(x+\Delta x,y+\Delta y)-f(x,y)$ 为函数在点P对应于自变量增量 $\Delta x$ 和 $\Delta y$ 的全增量,记作 $\Delta z$ ,即

$$
\Delta z = f (x + \Delta x, y + \Delta y) - f (x, y). \tag {3-1}
$$

一般说来,计算全增量  $\Delta z$  比较复杂.与一元函数的情形一样,我们希望用自变量的增量  $\Delta x,\Delta y$  的线性函数来近似地代替函数的合增量 A, 从而

定义 设函数  $z=f(x,y)$  在点  $(x,y)$  的某邻域内有定义, 如果函数在点  $(x,y)$  的全增量

可表示为

$$
\Delta z = f (x + \Delta x, y + \Delta y) - f (x, y)
$$

$$
\Delta z = A \Delta x + B \Delta y + o (\rho), \tag {3-2}
$$

其中 $A$ 和 $B$ 不依赖于 $\Delta x$ 和 $\Delta y$ 而仅与 $x$ 和 $y$ 有关, $\rho = \sqrt{(\Delta x)^2 + (\Delta y)^2}$, 那么称函数 $z = f(x,y)$ 在点 $(x,y)$ 可微分, 而 $A\Delta x + B\Delta y$ 称为函数 $z = f(x,y)$ 在点 $(x,y)$ 的全微分, 记作 $\mathrm{d}z$, 即

$$
\mathrm{d} z = A \Delta x + B \Delta y.
$$

如果函数在区域 D 内各点处都可微分,那么称这函数在 D 内可微分.
在第二节中曾指出,多元函数在其上的位式为

2. 证明函数在某点的偏导数存在, 并不能保证函数在该点连续. 但是, 由上述定义可知, 如果函数 $z = f(x, y)$ 在点 $(x, y)$ 可微分, 那么这函数在该点必定连续. 事实上, 这时由 (3-2) 式可得

从而①

$$
\lim _ {\rho \to 0} \Delta z = 0,
$$

$\lim_{(\Delta x,\Delta y)\to (0,0)}f(x + \Delta x,y + \Delta y) = \lim_{\rho \to 0}[f(x,y) + \Delta z] = f(x,y).$ 因此函数 $z = f(x,y)$ 在点 $(x,y)$ 处连续.

下面讨论函数  $z=f(x,y)$  在点  $(x,y)$  可微分的条件.

定理1(必要条件) 如果函数 $z = f(x, y)$ 在点 $(x, y)$ 可微分, 那么该函数在点 $(x, y)$ 的偏导数 $\frac{\partial z}{\partial x}$ 与 $\frac{\partial z}{\partial y}$ 必定存在, 且函数 $z = f(x, y)$ 在点 $(x, y)$ 的全微分为

$$
\mathrm{d} z = \frac {\partial z}{\partial x} \Delta x + \frac {\partial z}{\partial y} \Delta y. \tag {3-3}
$$

证 设函数 $z = f(x, y)$ 在点 $P(x, y)$ 可微分. 于是, 对于点 $P$ 的某个邻域内的任意一点 $P'(x + \Delta x, y + \Delta y)$, (3-2) 式总成立. 特别当 $\Delta y = 0$ 时 (3-2) 式也应成立, 这时 $\rho = |\Delta x|$, 所以 (3-2) 式成为

$$
f (x + \Delta x, y) - f (x, y) = A \cdot \Delta x + o (\mid \Delta x \mid).
$$

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 这里, $\rho\rightarrow0$ 与 $(\Delta x,\Delta y)\rightarrow(0,0)$ 等价.</span></small>

70

---

第三节 全微分

上式两端各除以  $\Delta x$ ，再令  $\Delta x \rightarrow 0$  而取极限，就得

$$
\lim _ {\Delta x \to 0} \frac {f (x + \Delta x , y) - f (x , y)}{\Delta x} = A,
$$

从而偏导数 $\frac{\partial z}{\partial x}$ 存在,且等于A.同样可证 $\frac{\partial z}{\partial y}=B.$ 所以(3-3)式成立.证毕.

我们知道,一元函数在某点的导数存在是微分存在的充分必要条件.但对于多元函数来说,情形就不同了.当函数的各偏导数都存在时,虽然能形式地写出 $\frac{\partial z}{\partial x}\Delta x+\frac{\partial z}{\partial y}\Delta y$ ,但它与 $\Delta z$ 之差并不一定是较 $\rho$ 高阶的无穷小,因此它不一定是函数的全微分.换句话说,各偏导数的存在只是全微分存在的必要条件而不是充分条件.例如,函数

$$
z = f (x, y) = \left\{ \begin{array}{l l} \frac {x y}{\sqrt {x ^ {2} + y ^ {2}}}, & x ^ {2} + y ^ {2} \neq 0, \\ 0, & x ^ {2} + y ^ {2} = 0 \end{array} \right.
$$

在点(0,0)处有 $f_{x}(0,0)=0$ 及 $f_{y}(0,0)=0$ ，所以

$$
\Delta z - [ f _ {x} (0, 0) \cdot \Delta x + f _ {y} (0, 0) \cdot \Delta y ] = \frac {\Delta x \cdot \Delta y}{\sqrt {(\Delta x) ^ {2} + (\Delta y) ^ {2}}},
$$

如果考虑点 $P^{\prime}(\Delta x,\Delta y)$ 沿着直线 $y = x$ 趋于(0,0)，那么

$$
\frac {\frac {\Delta x \cdot \Delta y}{\sqrt {(\Delta x) ^ {2} + (\Delta y) ^ {2}}}}{\rho} = \frac {\Delta x \cdot \Delta y}{(\Delta x) ^ {2} + (\Delta y) ^ {2}} = \frac {\Delta x \cdot \Delta x}{(\Delta x) ^ {2} + (\Delta x) ^ {2}} = \frac {1}{2},
$$

它不能随  $\rho\rightarrow0$  而趋于 0, 这表示  $\rho\rightarrow0$  时,

$$
\Delta z - [ f _ {x} (0, 0) \Delta x + f _ {y} (0, 0) \Delta y ]
$$

并不是较 $\rho$ 高阶的无穷小，因此函数在点(0,0)处的全微分并不存在，即函数在点(0,0)处是不可微分的.

由定理 1 及这个例子可知, 偏导数存在是可微分的必要条件而不是充分条件. 但是, 如果再假定函数的各个偏导数连续, 那么可以证明函数是可微分的, 即有下面的定理.

定理2(充分条件) 如果函数 $z = f(x,y)$ 的偏导数 $\frac{\partial z}{\partial x},\frac{\partial z}{\partial y}$ 在点 $(x,y)$ 连续①,那么函数在该点可微分.

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 多元函数的偏导数在一点连续是指: 偏导数在该点的某个邻域内存在, 于是偏导数在这个邻域内有定义, 进而这个偏导函数在该点连续.</span></small>

71

---

第九章 多元函数微分法及其应用

证 由假定, 函数的偏导数 $\frac{\partial z}{\partial x}$ 与 $\frac{\partial z}{\partial y}$ 在点 $P(x, y)$ 的某邻域内存在. 设点 $(x + \Delta x, y + \Delta y)$ 为该邻域内任意一点, 考察函数的全增量

$$
\begin{array}{l} \Delta z = f (x + \Delta x, y + \Delta y) - f (x, y) \\ = [ f (x + \Delta x, y + \Delta y) - f (x, y + \Delta y) ] + [ f (x, y + \Delta y) - f (x, y) ]. \\ \end{array}
$$

在第一个方括号内的表达式,由于  $y+\Delta y$  不变,因而可以看做是 x 的一元函数  $f(x,y+\Delta y)$  的增量.于是,应用拉格朗日中值定理,得到

$$
f (x + \Delta x, y + \Delta y) - f (x, y + \Delta y) = f _ {x} (x + \theta_ {1} \Delta x, y + \Delta y) \Delta x \quad (0 <   \theta_ {1} <   1).
$$

又依假设， $f_{x}(x,y)$ 在点 $(x,y)$ 连续，所以上式可写为

$$
f (x + \Delta x, y + \Delta y) - f (x, y + \Delta y) = f _ {x} (x, y) \Delta x + \varepsilon_ {1} \Delta x, \tag {3-4}
$$

其中  $\varepsilon_{1}$  为  $\Delta x$  与  $\Delta y$  的函数，且当  $\Delta x \to 0, \Delta y \to 0$  时， $\varepsilon_{1} \to 0$ .

同理可证第二个方括号内的表达式可写为

$$
f (x, y + \Delta y) - f (x, y) = f _ {y} (x, y) \Delta y + \varepsilon_ {2} \Delta y, \tag {3-5}
$$

其中  $\varepsilon_{2}$  为  $\Delta y$  的函数, 且当  $\Delta y \to 0$  时,  $\varepsilon_{2} \to 0$ .

由(3-4)、(3-5)两式可见,在偏导数连续的假定下,全增量 $\Delta z$ 可以表示为

$$
\Delta z = f _ {x} (x, y) \Delta x + f _ {y} (x, y) \Delta y + \varepsilon_ {1} \Delta x + \varepsilon_ {2} \Delta y. \tag {3-6}
$$

容易看出

$$
\left| \frac {\varepsilon_ {1} \Delta x + \varepsilon_ {2} \Delta y}{\rho} \right| \leqslant | \varepsilon_ {1} | + | \varepsilon_ {2} |,
$$

它是随着 $(\Delta x,\Delta y)\rightarrow(0,0)$ 即 $\rho\rightarrow0$ 而趋于零的.

这就证明了 $z = f(x,y)$ 在点 $P(x,y)$ 是可微分的.

以上关于二元函数全微分的定义及可微分的必要条件和充分条件,可以完全类似地推广到三元和三元以上的多元函数.

习惯上,我们将自变量的增量  $\Delta x$  与  $\Delta y$  分别记作 dx 与 dy,并分别称为自变量 x 与 y 的微分.这样,函数  $z=f(x,y)$  的全微分就可写为

$$
\mathrm{d} z = \frac {\partial z}{\partial x} \mathrm{d} x + \frac {\partial z}{\partial y} \mathrm{d} y, \tag {3-7}
$$

通常把二元函数的全微分等于它的两个偏微分之和这个结论称为二元函数的微分符合叠加原理.

叠加原理也适用于二元以上的函数.例如,如果三元函数 $u=f(x,y,z)$ 可微分,那么它的全微分就等于它的三个偏微分之和,即

$$
\mathrm{d} u = \frac {\partial u}{\partial x} \mathrm{d} x + \frac {\partial u}{\partial y} \mathrm{d} y + \frac {\partial u}{\partial z} \mathrm{d} z.
$$

图

释疑解难

9-2

72

---

第三节 全微分

例 1 计算函数  $z=x^{2}y+y^{2}$  的全微分.

解 因为 $\frac{\partial z}{\partial x} = 2xy, \frac{\partial z}{\partial y} = x^2 + 2y$，所以

$$
\mathrm{d} z = 2 x y \mathrm{d} x + (x ^ {2} + 2 y) \mathrm{d} y.
$$

例 2 计算函数  $z=e^{xy}$  在点(2,1)处的全微分.

解 因为

$$
\frac {\partial z}{\partial x} = y \mathrm{e} ^ {x y}, \frac {\partial z}{\partial y} = x \mathrm{e} ^ {x y}; \left. \frac {\partial z}{\partial x} \right| _ {x = 2 \atop y = 1} = \mathrm{e} ^ {2}, \left. \frac {\partial z}{\partial y} \right| _ {x = 2 \atop y = 1} = 2 \mathrm{e} ^ {2},
$$

所以

$$
\mathrm{d}z\Bigg|_{\substack{x = 2\\ y = 1}} = \mathrm{e}^{2}\mathrm{d}x + 2\mathrm{e}^{2}\mathrm{d}y.
$$

例 3 计算函数  $u = x + \sin \frac{y}{2} + e^{yz}$  的全微分.

解 因为 $\frac{\partial u}{\partial x} = 1, \frac{\partial u}{\partial y} = \frac{1}{2}\cos \frac{y}{2} + ze^{yz}, \frac{\partial u}{\partial z} = ye^{yz}$, 所以

$$
\mathrm{d} u = \mathrm{d} x + \left(\frac {1}{2} \cos \frac {y}{2} + z \mathrm{e} ^ {y z}\right) \mathrm{d} y + y \mathrm{e} ^ {y z} \mathrm{d} z.
$$

## \* 二、全微分在近似计算中的应用

由二元函数全微分的定义及关于全微分存在的充分条件可知, 当二元函数  $z=f(x,y)$  在点  $P(x,y)$  的两个偏导数  $f_{x}(x,y)$ ,  $f_{y}(x,y)$  连续, 并且  $\left|\Delta x\right|$ ,  $\left|\Delta y\right|$  都较小时, 就有近似等式

$$
\Delta z \approx \mathrm{d} z = f _ {x} (x, y) \Delta x + f _ {y} (x, y) \Delta y. \tag {3-8}
$$

上式也可以写成

$$
f (x + \Delta x, y + \Delta y) \approx f (x, y) + f _ {x} (x, y) \Delta x + f _ {y} (x, y) \Delta y. \tag {3-9}
$$

与一元函数的情形相类似,可以利用(3-8)式或(3-9)式对二元函数作近似计算和误差估计,举例于下.

例 4 有一圆柱体受压后发生形变, 它的半径由 20 cm 增大到 20.05 cm, 高度由 100 cm 减少到 99 cm. 求此圆柱体体积变化的近似值.

解 设圆柱体的半径、高和体积依次为 r, h 和 V, 则有

$$
V = \pi r ^ {2} h.
$$

记 $r, h$ 和 $V$ 的增量依次为 $\Delta r, \Delta h$ 和 $\Delta V$. 应用公式(3-8)，有

$$
\Delta V \approx \mathrm{d} V = V _ {r} \Delta r + V _ {h} \Delta h = 2 \pi r h \Delta r + \pi r ^ {2} \Delta h.
$$

把 $r = 20, h = 100, \Delta r = 0.05, \Delta h = -1$ 代入，得

$$
\Delta V \approx 2 \pi \times 2 0 \times 1 0 0 \times 0. 0 5 + \pi \times 2 0 ^ {2} \times (- 1) = - 2 0 0 \pi (\mathrm{cm} ^ {3}).
$$

73

---

第九章 多元函数微分法及其应用

即此圆柱体在受压后体积约减少了 $200\pi \mathrm{cm}^3$

例 5 计算  $1.04^{2.02}$  的近似值.

解 设函数 $f(x, y) = x^y$. 显然, 要计算的值就是函数在 $x = 1.04, y = 2.02$ 时的函数值 $f(1.04, 2.02)$.

取 $x = 1, y = 2, \Delta x = 0.04, \Delta y = 0.02$. 由于

$$
f _ {x} (x, y) = y x ^ {y - 1}, \quad f _ {y} (x, y) = x ^ {y} \ln x,
$$

$$
f (1, 2) = 1, \quad f _ {x} (1, 2) = 2, \quad f _ {y} (1, 2) = 0,
$$

所以,应用公式(3-9)便有

$$
1. 0 4 ^ {2. 0 2} \approx 1 + 2 \times 0. 0 4 + 0 \times 0. 0 2 = 1. 0 8.
$$

例6 利用单摆摆动测定重力加速度 $g$ 的公式是

$$
g = \frac {4 \pi^ {2} l}{T ^ {2}}.
$$

现测得单摆摆长 l 与振动周期 T 分别为  $l=(100\pm0.1)\mathrm{cm}, T=(2\pm0.004)\mathrm{s}$ . 问由于测定 l 与 T 的误差而引起 g 的绝对误差和相对误差各为多少①?

解 如果把测量 $l$ 与 $T$ 时所产生的误差当作 $|\Delta l|$ 与 $|\Delta T|$, 那么利用上述计算公式所产生的误差就是二元函数 $g = \frac{4\pi^2 l}{T^2}$ 的全增量的绝对值 $|\Delta g|$. 由于 $|\Delta l|, |\Delta T|$ 都很小, 因此我们可以用 $\mathrm{dg}$ 来近似地代替 $\Delta g$. 这样就得到 $g$ 的误差为

$$
\begin{array}{l} \mid \Delta g \mid \approx \mid \mathrm{d} g \mid = \left| \frac {\partial g}{\partial l} \Delta l + \frac {\partial g}{\partial T} \Delta T \right| \\ \leqslant \left| \frac {\partial g}{\partial l} \right| \cdot \delta_ {l} + \left| \frac {\partial g}{\partial T} \right| \cdot \delta_ {T} = 4 \pi^ {2} \left(\frac {1}{T ^ {2}} \delta_ {l} + \frac {2 l}{T ^ {3}} \delta_ {T}\right), \\ \end{array}
$$

其中 $\delta_{l}$ 与 $\delta_T$ 分别为 $l$ 与 $T$ 的绝对误差. 把 $l = 100\mathrm{cm}, T = 2\mathrm{s}, \delta_l = 0.1\mathrm{cm}, \delta_T = 0.004\mathrm{s}$ 代入上式, 得 $g$ 的绝对误差约为

$$
\delta_ {g} = 4 \pi^ {2} \left(\frac {0 . 1}{2 ^ {2}} + \frac {2 \times 1 0 0}{2 ^ {3}} \times 0. 0 0 4\right) = 0. 5 \pi^ {2} \approx 4. 9 3 (\mathrm{cm/s} ^ {2}).
$$

从而 $g$ 的相对误差约为

$$
\frac {\delta_ {g}}{g} = \frac {0 . 5 \pi^ {2}}{\frac {4 \pi^ {2} \times 1 0 0}{2 ^ {2}}} = 0. 5 \%.
$$

从上面的例子可以看到,对于一般的二元函数  $z=f(x,y)$ , 如果自变量 x,y 的绝对误差分别为  $\delta_{x},\delta_{y}$ , 即

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 按第二章第五节的说明,这里的绝对误差和相对误差各指相应的误差限.</span></small>

74

---

第三节 全微分

$$
\mid \Delta x \mid \leqslant \delta_ {x}, \quad \mid \Delta y \mid \leqslant \delta_ {y},
$$

那么 $z$ 的误差

$$
\begin{array}{l} \mid \Delta z \mid \approx \mid \mathrm{d} z \mid = \left| \frac {\partial z}{\partial x} \Delta x + \frac {\partial z}{\partial y} \Delta y \right| \\ \leqslant \left| \frac {\partial z}{\partial x} \right| \cdot | \Delta x | + \left| \frac {\partial z}{\partial y} \right| \cdot | \Delta y | \leqslant \left| \frac {\partial z}{\partial x} \right| \delta_ {x} + \left| \frac {\partial z}{\partial y} \right| \delta_ {y}, \\ \end{array}
$$

从而得到 $z$ 的绝对误差约为

$$
\delta_ {z} = \left| \frac {\partial z}{\partial x} \right| \delta_ {x} + \left| \frac {\partial z}{\partial y} \right| \delta_ {y}, \tag {3-10}
$$

$z$ 的相对误差约为

$$
\frac {\delta_ {z}}{| z |} = \left| \frac {\frac {\partial z}{\partial x}}{z} \right| \delta_ {x} + \left| \frac {\frac {\partial z}{\partial y}}{z} \right| \delta_ {y}. \tag {3-11}
$$

## 习题9-3

1. 求下列函数的全微分:

(1) $z = xy + \frac{x}{y};$

(2) $z=e^{\frac{y}{x}}$;

(3) $z = \frac{y}{\sqrt{x^2 + y^2}};$

(4)  $u = x^{yz}.$

2. 求函数  $z=\ln(1+x^{2}+y^{2})$  当 x=1, y=2 时的全微分.

3. 求函数 $z = \frac{y}{x}$ 当 $x = 2, y = 1, \Delta x = 0.1, \Delta y = -0.2$ 时的全增量和全微分.

4. 求函数  $z=e^{xy}$  当 x=1, y=1,  $\Delta x=0.15$ ,  $\Delta y=0.1$  时的全微分.

5. 考虑二元函数 $f(x, y)$ 的下面四条性质:

(1) $f(x,y)$ 在点 $(x_0,y_0)$ 连续；
(2) $f_{x}(x,y), f_{y}(x,y)$ 在点 $(x_0, y_0)$ 连续；
(3) $f(x,y)$ 在点 $(x_{0},y_{0})$ 可微分；
(4) $f_{x}(x_{0},y_{0}),f_{y}(x_{0},y_{0})$ 存在.

若用“ $P \Rightarrow Q$ ”表示可由性质 P 推出性质 Q，则下列四个选项中正确的是（）.

(A) (2) $\Rightarrow$ (3) $\Rightarrow$ (1)

(B) (3) $\Rightarrow$ (2) $\Rightarrow$ (1)

(C) (3) $\Rightarrow$ (4) $\Rightarrow$ (1)

(D) (3) $\Rightarrow$ (1) $\Rightarrow$ (4)

\*6. 计算 $\sqrt{1.02^3 + 1.97^3}$ 的近似值.

\*7. 计算 $1.97^{1.05}$ 的近似值 $(\ln 2 = 0.693)$.

\*8. 已知边长为 $x = 6 \mathrm{~m}$ 与 $y = 8 \mathrm{~m}$ 的矩形, 如果 $x$ 边增加 $5 \mathrm{~cm}$ 而 $y$ 边减少 $10 \mathrm{~cm}$, 问这个矩形的对角线的近似变化怎样?

\*9. 设有一无盖圆柱形容器, 容器的壁与底的厚度均为 $0.1 \mathrm{~cm}$, 内高为 $20 \mathrm{~cm}$, 内半径为 $4 \mathrm{~cm}$. 求这个容器外壳体积的近似值.

75

---

第九章 多元函数微分法及其应用

\* 10. 设有直角三角形, 测得其两直角边的长分别为 $(7 \pm 0.1) \mathrm{cm}$ 和 $(24 \pm 0.1) \mathrm{cm}$. 试求利用上述两值来计算斜边长度时的绝对误差.

\*11. 测得一块三角形土地的两边边长分别为 $(63 \pm 0.1) \mathrm{~m}$ 和 $(78 \pm 0.1) \mathrm{~m}$, 这两边的夹角为 $60^{\circ} \pm 1^{\circ}$. 试求这块三角形土地面积的近似值, 并求其绝对误差和相对误差.

\* 12. 利用全微分证明:两数之和的绝对误差等于它们各自的绝对误差之和.

\*13. 利用全微分证明:乘积的相对误差等于各因子的相对误差之和,商的相对误差等于被除数及除数的相对误差之和.

## 第四节 多元复合函数的求导法则

本节要将一元函数微分学中复合函数的求导法则推广到多元复合函数的情形.多元复合函数的求导法则在多元函数微分学中也起着重要作用.

下面按照多元复合函数不同的复合情形,分三种情形讨论.

## 1. 一元函数与多元函数复合的情形

定理1 如果函数 $u = \varphi(t)$ 及 $v = \psi(t)$ 都在点 $t$ 可导，函数 $z = f(u, v)$ 在对应点 $(u, v)$ 具有连续偏导数，那么复合函数 $z = f[\varphi(t), \psi(t)]$ 在点 $t$ 可导，且有

$$
\frac {\mathrm{d} z}{\mathrm{d} t} = \frac {\partial z}{\partial u} \frac {\mathrm{d} u}{\mathrm{d} t} + \frac {\partial z}{\partial v} \frac {\mathrm{d} v}{\mathrm{d} t}. \tag {4-1}
$$

证 设 $t$ 获得增量 $\Delta t$, 这时 $u = \varphi(t), v = \psi(t)$ 的对应增量为 $\Delta u, \Delta v$, 由此, 函数 $z = f(u, v)$ 相应地获得增量 $\Delta z$. 按假定, 函数 $z = f(u, v)$ 在点 $(u, v)$ 具有连续偏导数, 这时函数的全增量 $\Delta z$ 可表示为

$$
\Delta z = \frac {\partial z}{\partial u} \Delta u + \frac {\partial z}{\partial v} \Delta v + \varepsilon_ {1} \Delta u + \varepsilon_ {2} \Delta v,
$$

这里，当 $\Delta u\to 0,\Delta v\to 0$ 时， $\varepsilon_1\rightarrow 0,\varepsilon_2\rightarrow 0.$ ①

将上式两端各除以  $\Delta t$ ，得

$$
\frac {\Delta z}{\Delta t} = \frac {\partial z}{\partial u} \frac {\Delta u}{\Delta t} + \frac {\partial z}{\partial v} \frac {\Delta v}{\Delta t} + \varepsilon_ {1} \frac {\Delta u}{\Delta t} + \varepsilon_ {2} \frac {\Delta v}{\Delta t}.
$$

因为当 $\Delta t\to 0$ 时， $\Delta u\rightarrow 0,\Delta v\rightarrow 0,\frac{\Delta u}{\Delta t}\longrightarrow \frac{\mathrm{d}u}{\mathrm{d}t},\frac{\Delta v}{\Delta t}\longrightarrow \frac{\mathrm{d}v}{\mathrm{d}t}$ ，所以

$$
\lim _ {\Delta t \to 0} \frac {\Delta z}{\Delta t} = \frac {\partial z}{\partial u} \frac {\mathrm{d} u}{\mathrm{d} t} + \frac {\partial z}{\partial v} \frac {\mathrm{d} v}{\mathrm{d} t}.
$$

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 在偏导数连续的条件下,这一公式成立的证明参见本章第三节定理2的证明.</span></small>

76

---

第四节 多元复合函数的求导法则

这就证明了复合函数 $z = f[\varphi (t),\psi (t)]$ 在点 $t$ 可导，且其导数可用公式(4-1)计算.证毕.

用同样的方法, 可把定理推广到复合函数的中间变量多于两个的情形. 例如, 设  $z=f(u,v,w)$ ,  $u=\varphi(t)$ ,  $v=\psi(t)$ ,  $w=\omega(t)$  复合而得复合函数

$$
z = f [ \varphi (t), \psi (t), \omega (t) ],
$$

则在与定理相类似的条件下,这个复合函数在点 t 可导,且其导数可用下列公式计算:

$$
\frac {\mathrm{d} z}{\mathrm{d} t} = \frac {\partial z}{\partial u} \frac {\mathrm{d} u}{\mathrm{d} t} + \frac {\partial z}{\partial v} \frac {\mathrm{d} v}{\mathrm{d} t} + \frac {\partial z}{\partial w} \frac {\mathrm{d} w}{\mathrm{d} t}. \tag {4-2}
$$

公式(4-1)及(4-2)中的导数 $\frac{dz}{dt}$ 称为全导数.

## 2. 多元函数与多元函数复合的情形

定理2 如果函数 $u = \varphi(x, y)$ 及 $v = \psi(x, y)$ 都在点 $(x, y)$ 具有对 $x$ 及对 $y$ 的偏导数，函数 $z = f(u, v)$ 在对应点 $(u, v)$ 具有连续偏导数，那么复合函数 $z = f[\varphi(x, y), \psi(x, y)]$ 在点 $(x, y)$ 的两个偏导数都存在，且有

$$
\frac {\partial z}{\partial x} = \frac {\partial z}{\partial u} \frac {\partial u}{\partial x} + \frac {\partial z}{\partial v} \frac {\partial v}{\partial x}, \tag {4-3}
$$

$$
\frac {\partial z}{\partial y} = \frac {\partial z}{\partial u} \frac {\partial u}{\partial y} + \frac {\partial z}{\partial v} \frac {\partial v}{\partial y}. \tag {4-4}
$$

事实上,这里求 $\frac{\partial z}{\partial x}$ 时,将y看做常量,因此 $u=\varphi(x,y)$ 及 $v=\psi(x,y)$ 仍可看做一元函数而应用定理1.但由于复合函数 $z=f\left[\varphi(x,y),\psi(x,y)\right]$ 以及 $u=\varphi(x,y)$ 和 $v=\psi(x,y)$ 都是x,y的二元函数,所以应把(4-1)式中的d改为 $\partial$ ,再把t换成x,这样便由(4-1)式得(4-3)式.同理由(4-1)式可得(4-4)式.

类似地, 设  $u=\varphi(x,y)$ ,  $v=\psi(x,y)$  及  $w=\omega(x,y)$  都在点  $(x,y)$  具有对 x 及对 y 的偏导数, 函数  $z=f(u,v,w)$  在对应点  $(u,v,w)$  具有连续偏导数, 则复合函数

$$
z = f [ \varphi (x, y), \psi (x, y), \omega (x, y) ]
$$

在点 $(x,y)$ 的两个偏导数都存在，且可用下列公式计算:

$$
\frac {\partial z}{\partial x} = \frac {\partial z}{\partial u} \frac {\partial u}{\partial x} + \frac {\partial z}{\partial v} \frac {\partial v}{\partial x} + \frac {\partial z}{\partial w} \frac {\partial w}{\partial x}, \tag {4-5}
$$

$$
\frac {\partial z}{\partial y} = \frac {\partial z}{\partial u} \frac {\partial u}{\partial y} + \frac {\partial z}{\partial v} \frac {\partial v}{\partial y} + \frac {\partial z}{\partial w} \frac {\partial w}{\partial y}. \tag {4-6}
$$

## 3. 其他情形

定理3 如果函数 $u = \varphi (x,y)$ 在点 $(x,y)$ 具有对 $x$ 及对 $y$ 的偏导数，函数 $v = \psi (y)$

77

---

第九章 多元函数微分法及其应用

在点 $y$ 可导，函数 $z = f(u, v)$ 在对应点 $(u, v)$ 具有连续偏导数，那么复合函数 $z = f[\varphi(x, y), \psi(y)]$ 在点 $(x, y)$ 的两个偏导数都存在，且有

$$
\frac {\partial z}{\partial x} = \frac {\partial z}{\partial u} \frac {\partial u}{\partial x}, \tag {4-7}
$$

$$
\frac {\partial z}{\partial y} = \frac {\partial z}{\partial u} \frac {\partial u}{\partial y} + \frac {\partial z}{\partial v} \frac {\mathrm{d} v}{\mathrm{d} y}. \tag {4-8}
$$

上述情形实际上是情形2的一种特例, 即在情形2中, 如变量 v 与 x 无关, 从而  $\frac{\partial v}{\partial x}=0$ ; 在 v 对 y 求导时, 由于  $v=\psi(y)$  是一元函数, 故  $\frac{\partial v}{\partial y}$  换成了  $\frac{dv}{dy}$ , 这就得出上述结果.

在情形3中,还会遇到这样的情形:复合函数的某些中间变量本身又是复合函数的自变量.例如,设 $z=f(u,x,y)$ 具有连续偏导数,而 $u=\varphi(x,y)$ 具有偏导数,则复合函数 $z=f\left[\varphi(x,y),x,y\right]$ 可看做情形2中当v=x,w=y的特殊情形.因此

$$
\frac {\partial v}{\partial x} = 1, \quad \frac {\partial w}{\partial x} = 0, \quad \frac {\partial v}{\partial y} = 0, \quad \frac {\partial w}{\partial y} = 1.
$$

从而复合函数 $z = f[\varphi (x,y),x,y]$ 具有对自变量 $x$ 及 $y$ 的偏导数，且由公式(4-5）、(4-6)得

$$
\frac {\partial z}{\partial x} = \frac {\partial f}{\partial u} \frac {\partial u}{\partial x} + \frac {\partial f}{\partial x}, \quad \frac {\partial z}{\partial y} = \frac {\partial f}{\partial u} \frac {\partial u}{\partial y} + \frac {\partial f}{\partial y}.
$$

注意 这里 $\frac{\partial z}{\partial x}$ 与 $\frac{\partial f}{\partial x}$ 是不同的，$\frac{\partial z}{\partial x}$ 是把复合函数 $z = f[\varphi(x, y), x, y]$ 中的 $y$ 看做不变而对 $x$ 的偏导数，$\frac{\partial f}{\partial x}$ 是把 $f(u, x, y)$ 中的 $u$ 及 $y$ 看做不变而对 $x$ 的偏导数。$\frac{\partial z}{\partial y}$ 与 $\frac{\partial f}{\partial y}$ 也有类似的区别.

例1 设 $z = \mathrm{e}^{u}\sin v$，而 $u = xy, v = x + y$. 求 $\frac{\partial z}{\partial x}$ 和 $\frac{\partial z}{\partial y}$.

解 $\frac{\partial z}{\partial x} = \frac{\partial z}{\partial u}\frac{\partial u}{\partial x} +\frac{\partial z}{\partial v}\frac{\partial v}{\partial x} = e^{u}\sin v\cdot y + e^{u}\cos v\cdot 1 = e^{xy}[y\sin (x + y) + \cos (x + y)]$

$$
\frac {\partial z}{\partial y} = \frac {\partial z}{\partial u} \frac {\partial u}{\partial y} + \frac {\partial z}{\partial v} \frac {\partial v}{\partial y} = \mathrm{e} ^ {u} \sin v \cdot x + \mathrm{e} ^ {u} \cos v \cdot 1 = \mathrm{e} ^ {x y} [ x \sin (x + y) + \cos (x + y) ].
$$

例2 设 $u = f(x, y, z) = \mathrm{e}^{x^2 + y^2 + z^2}$, 而 $z = x^2 \sin y$. 求 $\frac{\partial u}{\partial x}$ 和 $\frac{\partial u}{\partial y}$.

解 $\frac{\partial u}{\partial x} = \frac{\partial f}{\partial x} +\frac{\partial f}{\partial z}\frac{\partial z}{\partial x} = 2xe^{x^2 +y^2 +z^2} + 2ze^{x^2 +y^2 +z^2}\cdot 2x\sin y = 2x(1 + 2x^2\sin^2 y)e^{x^2 +y^2 +x^4\sin^2 y}.$

$$
\frac {\partial u}{\partial y} = \frac {\partial f}{\partial y} + \frac {\partial f}{\partial z} \frac {\partial z}{\partial y} = 2 y \mathrm{e} ^ {x ^ {2} + y ^ {2} + z ^ {2}} + 2 z \mathrm{e} ^ {x ^ {2} + y ^ {2} + z ^ {2}} \cdot x ^ {2} \cos y = 2 (y + x ^ {4} \sin y \cos y) \mathrm{e} ^ {x ^ {2} + y ^ {2} + x ^ {4} \sin^ {2} y}.
$$

例3 设 $z = f(u, v, t) = uv + \sin t$，而 $u = \mathrm{e}^t, v = \cos t$. 求全导数 $\frac{\mathrm{d}z}{\mathrm{d}t}$.

78

---

第四节 多元复合函数的求导法则

解 $\frac{\mathrm{d}z}{\mathrm{d}t} = \frac{\partial f}{\partial u}\frac{\mathrm{d}u}{\mathrm{d}t} +\frac{\partial f}{\partial v}\frac{\mathrm{d}v}{\mathrm{d}t} +\frac{\partial f}{\partial t} = v\mathrm{e}^t -u\sin t + \cos t$

$$
= \mathrm{e} ^ {t} \cos t - \mathrm{e} ^ {t} \sin t + \cos t = \mathrm{e} ^ {t} (\cos t - \sin t) + \cos t.
$$

例4设 $w = f(x + y + z,xyz)$ ， $f$ 具有二阶连续偏导数，求 $\frac{\partial w}{\partial x}$ 及 $\frac{\partial^2w}{\partial x\partial z}$

解 令 $u = x + y + z, v = xyz$，则 $w = f(u, v)$.

因所给函数由 $w = f(u, v)$ 及 $u = x + y + z, v = xyz$ 复合而成，根据复合函数求导法则，有

$$
\frac {\partial w}{\partial x} = \frac {\partial f}{\partial u} \frac {\partial u}{\partial x} + \frac {\partial f}{\partial v} \frac {\partial v}{\partial x} = f _ {u} + y z f _ {v},
$$

$$
\frac {\partial^ {2} w}{\partial x \partial z} = \frac {\partial}{\partial z} (f _ {u} + y z f _ {v}) = \frac {\partial f _ {u}}{\partial z} + y f _ {v} + y z \frac {\partial f _ {v}}{\partial z}.
$$

求 $\frac{\partial f_{u}}{\partial z}$ 及 $\frac{\partial f_{v}}{\partial z}$ 时,应注意 $f_{u}(u,v)$ 及 $f_{v}(u,v)$ 中u,v是中间变量,根据复合函数求导法则,有

$$
\frac {\partial f _ {u}}{\partial z} = \frac {\partial f _ {u}}{\partial u} \frac {\partial u}{\partial z} + \frac {\partial f _ {u}}{\partial v} \frac {\partial v}{\partial z} = f _ {u u} + x y f _ {u v},
$$

$$
\frac {\partial f _ {v}}{\partial z} = \frac {\partial f _ {v}}{\partial u} \frac {\partial u}{\partial z} + \frac {\partial f _ {v}}{\partial v} \frac {\partial v}{\partial z} = f _ {v u} + x y f _ {v v},
$$

于是

$$
\frac {\partial^ {2} w}{\partial x \partial z} = f _ {u u} + x y f _ {u v} + y f _ {v} + y z f _ {v u} + x y ^ {2} z f _ {v v} = f _ {u u} + y (x + z) f _ {u v} + x y ^ {2} z f _ {v v} + y f _ {v}.
$$

有时,为表达简便起见,引入以下记号:

$$
f _ {1} ^ {\prime} (u, v) = f _ {u} (u, v), \quad f _ {2} ^ {\prime} (u, v) = f _ {v} (u, v), \quad f _ {1 2} ^ {\prime \prime} (u, v) = f _ {u v} (u, v),
$$

这里,下标1表示对第一个变量u求偏导数,下标2表示对第二个变量v求偏导数.同理有 $f_{11}^{\prime\prime},f_{22}^{\prime\prime},f_{21}^{\prime\prime}$ 等.利用这种记号,例4的结果可表示成

$$
\frac {\partial w}{\partial x} = f _ {1} ^ {\prime} + y z f _ {2} ^ {\prime},
$$

$$
\frac {\partial^ {2} w}{\partial x \partial z} = f _ {1 1} ^ {\prime \prime} + y (x + z) f _ {1 2} ^ {\prime \prime} + x y ^ {2} z f _ {2 2} ^ {\prime \prime} + y f _ {2} ^ {\prime}.
$$

例 5 设  $u=f(x,y)$  的所有二阶偏导数连续, 把下列表达式转换为极坐标系中的形式:

(1) $\left(\frac{\partial u}{\partial x}\right)^2 +\left(\frac{\partial u}{\partial y}\right)^2;$

(2) $\frac{\partial^2 u}{\partial x^2} + \frac{\partial^2 u}{\partial y^2}$.

解 由直角坐标与极坐标间的关系式

79

---

第九章 多元函数微分法及其应用

$$
x = \rho \cos \theta , \quad y = \rho \sin \theta ,
$$

可把函数  $u=f(x,y)$  换成极坐标  $\rho$  及  $\theta$  的函数:

$$
u = f (x, y) = f (\rho \cos \theta , \rho \sin \theta) = F (\rho , \theta).
$$

现在要将式子 $\left(\frac{\partial u}{\partial x}\right)^2 +\left(\frac{\partial u}{\partial y}\right)^2$ 及 $\frac{\partial^2u}{\partial x^2} +\frac{\partial^2u}{\partial y^2}$ 用 $\rho ,\theta$ 及函数 $u = F(\rho ,\theta)$ 对 $\rho ,\theta$ 的偏导数来表达.为此，要求出 $u = f(x,y)$ 的偏导数 $\frac{\partial u}{\partial x},\frac{\partial u}{\partial y},\frac{\partial^2u}{\partial x^2}$ 及 $\frac{\partial^2u}{\partial y^2}$.这里 $u = f(x,y)$ 要看做由 $u = F(\rho ,\theta)$ 及

$$
\rho = \sqrt {x ^ {2} + y ^ {2}}, \quad \theta = \arctan \frac {y}{x} ①
$$

复合而成,应用复合函数求导法则,得

$$
\frac {\partial u}{\partial x} = \frac {\partial u}{\partial \rho} \frac {\partial \rho}{\partial x} + \frac {\partial u}{\partial \theta} \frac {\partial \theta}{\partial x} = \frac {\partial u}{\partial \rho} \frac {x}{\rho} - \frac {\partial u}{\partial \theta} \frac {\gamma}{\rho^ {2}} = \frac {\partial u}{\partial \rho} \cos \theta - \frac {\partial u}{\partial \theta} \frac {\sin \theta}{\rho},
$$

$$
\frac {\partial u}{\partial y} = \frac {\partial u}{\partial \rho} \frac {\partial \rho}{\partial y} + \frac {\partial u}{\partial \theta} \frac {\partial \theta}{\partial y} = \frac {\partial u}{\partial \rho} \frac {y}{\rho} + \frac {\partial u}{\partial \theta} \frac {x}{\rho^ {2}} = \frac {\partial u}{\partial \rho} \sin \theta + \frac {\partial u}{\partial \theta} \frac {\cos \theta}{\rho}.
$$

两式平方后相加,得

$$
\left(\frac {\partial u}{\partial x}\right) ^ {2} + \left(\frac {\partial u}{\partial y}\right) ^ {2} = \left(\frac {\partial u}{\partial \rho}\right) ^ {2} + \frac {1}{\rho^ {2}} \left(\frac {\partial u}{\partial \theta}\right) ^ {2}.
$$

再求二阶偏导数,得

$$
\begin{array}{l} \frac {\partial^ {2} u}{\partial x ^ {2}} = \frac {\partial}{\partial \rho} \left(\frac {\partial u}{\partial x}\right) \cdot \frac {\partial \rho}{\partial x} + \frac {\partial}{\partial \theta} \left(\frac {\partial u}{\partial x}\right) \cdot \frac {\partial \theta}{\partial x} \\ = \left[ \frac {\partial}{\partial \rho} \left(\frac {\partial u}{\partial \rho} \cos \theta - \frac {\partial u}{\partial \theta} \frac {\sin \theta}{\rho}\right) \right] \cdot \cos \theta - \left[ \frac {\partial}{\partial \theta} \left(\frac {\partial u}{\partial \rho} \cos \theta - \frac {\partial u}{\partial \theta} \frac {\sin \theta}{\rho}\right) \right] \cdot \frac {\sin \theta}{\rho} \\ = \frac {\partial^ {2} u}{\partial \rho^ {2}} \cos^ {2} \theta - \frac {\partial^ {2} u}{\partial \rho \partial \theta} \frac {\sin 2 \theta}{\rho} + \frac {\partial^ {2} u}{\partial \theta^ {2}} \frac {\sin^ {2} \theta}{\rho^ {2}} + \frac {\partial u}{\partial \theta} \frac {\sin 2 \theta}{\rho^ {2}} + \frac {\partial u}{\partial \rho} \frac {\sin^ {2} \theta}{\rho}. \\ \end{array}
$$

同理可得

$$
\frac {\partial^ {2} u}{\partial y ^ {2}} = \frac {\partial^ {2} u}{\partial \rho^ {2}} \sin^ {2} \theta + \frac {\partial^ {2} u}{\partial \rho \partial \theta} \frac {\sin 2 \theta}{\rho} + \frac {\partial^ {2} u}{\partial \theta^ {2}} \frac {\cos^ {2} \theta}{\rho^ {2}} - \frac {\partial u}{\partial \theta} \frac {\sin 2 \theta}{\rho^ {2}} + \frac {\partial u}{\partial \rho} \frac {\cos^ {2} \theta}{\rho}.
$$

① 当点 $P(x,y)$ 在第一、四象限时，规定 $\theta$ 的取值范围为 $-\frac{\pi}{2} < \theta < \frac{\pi}{2}$，则

$$
\theta = \arctan \frac {y}{x};
$$

当点  $P(x,y)$  在第二、三象限时，规定  $\theta$  的取值范围为  $\frac{\pi}{2}<\theta<\frac{3}{2}\pi$ ，则

$$
\theta = \arctan \frac {y}{x} + \pi ,
$$

此时以下推导仍成立.

80

---

第四节 多元复合函数的求导法则

两式相加,得

$$
\frac {\partial^ {2} u}{\partial x ^ {2}} + \frac {\partial^ {2} u}{\partial y ^ {2}} = \frac {\partial^ {2} u}{\partial \rho^ {2}} + \frac {1}{\rho} \frac {\partial u}{\partial \rho} + \frac {1}{\rho^ {2}} \frac {\partial^ {2} u}{\partial \theta^ {2}} = \frac {1}{\rho^ {2}} \left[ \rho \frac {\partial}{\partial \rho} \left(\rho \frac {\partial u}{\partial \rho}\right) + \frac {\partial^ {2} u}{\partial \theta^ {2}} \right].
$$

全微分形式不变性 设函数 $z = f(u,v)$ 具有连续偏导数，则有全微分

$$
\mathrm{d} z = \frac {\partial z}{\partial u} \mathrm{d} u + \frac {\partial z}{\partial v} \mathrm{d} v.
$$

如果 $u$ 和 $v$ 又是中间变量, 即 $u = \varphi(x, y), v = \psi(x, y)$, 且这两个函数也具有连续偏导数, 那么复合函数

$$
z = f [ \varphi (x, y), \psi (x, y) ]
$$

的全微分为

$$
\mathrm{d} z = \frac {\partial z}{\partial x} \mathrm{d} x + \frac {\partial z}{\partial y} \mathrm{d} y,
$$

其中 $\frac{\partial z}{\partial x}$ 及 $\frac{\partial z}{\partial y}$ 分别由公式(4-3)及(4-4)给出.把公式(4-3)及(4-4)中的 $\frac{\partial z}{\partial x}$ 及 $\frac{\partial z}{\partial y}$ 代入上式,得

$$
\begin{array}{l} \mathrm{d} z = \left(\frac {\partial z}{\partial u} \frac {\partial u}{\partial x} + \frac {\partial z}{\partial v} \frac {\partial v}{\partial x}\right) \mathrm{d} x + \left(\frac {\partial z}{\partial u} \frac {\partial u}{\partial y} + \frac {\partial z}{\partial v} \frac {\partial v}{\partial y}\right) \mathrm{d} y \\ = \frac {\partial z}{\partial u} \left(\frac {\partial u}{\partial x} \mathrm{d} x + \frac {\partial u}{\partial y} \mathrm{d} y\right) + \frac {\partial z}{\partial v} \left(\frac {\partial v}{\partial x} \mathrm{d} x + \frac {\partial v}{\partial y} \mathrm{d} y\right) = \frac {\partial z}{\partial u} \mathrm{d} u + \frac {\partial z}{\partial v} \mathrm{d} v. \\ \end{array}
$$

由此可见,无论 u 和 v 是自变量还是中间变量,函数  $z=f(u,v)$  的全微分形式是一样的.这个性质叫做全微分形式不变性.

例 6 利用全微分形式不变性解本节的例 1.

解 $\mathrm{dz} = \mathrm{d}\left(\mathrm{e}^{u}\sin v\right) = \mathrm{e}^{u}\sin v\mathrm{d}u + \mathrm{e}^{u}\cos v\mathrm{d}v,$

因

$$
\mathrm{d} u = \mathrm{d} (x y) = y \mathrm{d} x + x \mathrm{d} y, \mathrm{d} v = \mathrm{d} (x + y) = \mathrm{d} x + \mathrm{d} y,
$$

代入后归并含 dx 及 dy 的项, 得

$$
\mathrm{d} z = \left(\mathrm{e} ^ {u} \sin v \cdot y + \mathrm{e} ^ {u} \cos v\right) \mathrm{d} x + \left(\mathrm{e} ^ {u} \sin v \cdot x + \mathrm{e} ^ {u} \cos v\right) \mathrm{d} y,
$$

即

$$
\frac {\partial z}{\partial x} \mathrm{d} x + \frac {\partial z}{\partial y} \mathrm{d} y = \mathrm{e} ^ {x y} [ y \sin (x + y) + \cos (x + y) ] \mathrm{d} x + \mathrm{e} ^ {x y} [ x \sin (x + y) + \cos (x + y) ] \mathrm{d} y.
$$

比较上式两端的 dx 和 dy 的系数, 就同时得到两个偏导数  $\frac{\partial z}{\partial x}$  和  $\frac{\partial z}{\partial y}$ , 它们与例 1 的结果一样.

## 习题9-4

1. 设 $z = u^{2} + v^{2}$, 而 $u = x + y, v = x - y$, 求 $\frac{\partial z}{\partial x}, \frac{\partial z}{\partial y}$.

![](../../raw/pages_0065-0096/images/page_87_image_23.jpg)

释疑解难

9-3

81

---

第九章 多元函数微分法及其应用

2. 设 $z = u^{2}\ln v$，而 $u = \frac{x}{y}, v = 3x - 2y$，求 $\frac{\partial z}{\partial x}, \frac{\partial z}{\partial y}$.
3. 设  $z = e^{x - 2y}$ ，而  $x = \sin t, y = t^{3}$ ，求  $\frac{dz}{dt}$ .
4. 设  $z=\arcsin(x-y)$ ，而  $x=3t, y=4t^{3}$ ，求  $\frac{dz}{dt}$ .
5. 设  $z=\arctan(xy)$ ，而  $y=e^{x}$ ，求  $\frac{dz}{dx}$ .
6. 设 $u = \frac{\mathrm{e}^{ax}(y - z)}{a^2 + 1}$，而 $y = a\sin x, z = \cos x$，求 $\frac{\mathrm{d}u}{\mathrm{d}x}$.
7. 设 $z = \arctan \frac{x}{y}$, 而 $x = u + v, y = u - v$, 验证 $\frac{\partial z}{\partial u} + \frac{\partial z}{\partial v} = \frac{u - v}{u^2 + v^2}$.
8. 求下列函数的一阶偏导数（其中f具有一阶连续偏导数）:

(1)  $u=f(x^{2}-y^{2},\mathrm{e}^{xy})$ ;

(2) $u = f\left(\frac{x}{y}, \frac{y}{z}\right)$;

(3)  $u=f(x,xy,xyz)$ .

9. 设  $z=xy+xF(u)$ ，而  $u=\frac{y}{x}$ ， $F(u)$  为可导函数，证明  $x\frac{\partial z}{\partial x}+y\frac{\partial z}{\partial y}=z+xy$ .

10. 设  $z=\frac{y}{f(x^{2}-y^{2})}$ ，其中  $f(u)$  为可导函数，验证  $\frac{1}{x}\frac{\partial z}{\partial x}+\frac{1}{y}\frac{\partial z}{\partial y}=\frac{z}{y^{2}}$ .

11. 设函数 $f(x, y, z)$ 满足 $f(tx, ty, tz) = t^n f(x, y, z)$ ( $t$ 为任意实数)，则称函数 $f$ 为 $n$ 次齐次函数。证明:$n$ 次齐次函数 $f$ 满足关系式

$$
xf_{x} + yf_{y} + zf_{z} = nf(x,y,z),
$$

其中函数f具有一阶连续偏导数.

12. 设 $z = f(x^{2} + y^{2})$，其中 $f$ 具有二阶导数，求 $\frac{\partial^2 z}{\partial x^2}, \frac{\partial^2 z}{\partial x \partial y}, \frac{\partial^2 z}{\partial y^2}$.

\*13. 求下列函数的 $\frac{\partial^2 z}{\partial x^2}, \frac{\partial^2 z}{\partial x \partial y}, \frac{\partial^2 z}{\partial y^2}$ （其中 $f$ 具有二阶连续偏导数）:

(1)  $z=f(xy,y)$ ;

(2) $z = f\left(x, \frac{x}{y}\right)$;

(3)  $z=f(xy^{2},x^{2}y)$ ;

(4) $z = f(\sin x, \cos y, \mathrm{e}^{x + y})$.

\* 14. 设 $u = f(x, y)$ 的所有二阶偏导数连续, 而

$$
x = \frac {s - \sqrt {3} t}{2}, \quad y = \frac {\sqrt {3} s + t}{2},
$$

证明

$$
\left(\frac {\partial u}{\partial x}\right) ^ {2} + \left(\frac {\partial u}{\partial y}\right) ^ {2} = \left(\frac {\partial u}{\partial s}\right) ^ {2} + \left(\frac {\partial u}{\partial t}\right) ^ {2} \quad \text {及} \quad \frac {\partial^ {2} u}{\partial x ^ {2}} + \frac {\partial^ {2} u}{\partial y ^ {2}} = \frac {\partial^ {2} u}{\partial s ^ {2}} + \frac {\partial^ {2} u}{\partial t ^ {2}}.
$$

82

---

第五节 隐函数的求导公式

## 第五节 隐函数的求导公式

## 一、一个方程的情形

在第二章第四节中我们已经提出了隐函数的概念,并且指出了不经过显化直接由方程

$$
F (x, y) = 0 \tag {5-1}
$$

求它所确定的隐函数的导数的方法. 现在介绍隐函数存在定理, 并根据多元复合函数的求导法来导出隐函数的导数公式.

隐函数存在定理1 设函数 $F(x, y)$ 在点 $P(x_0, y_0)$ 的某一邻域内具有连续偏导数，且 $F(x_0, y_0) = 0, F_y(x_0, y_0) \neq 0$，则方程 $F(x, y) = 0$ 在点 $(x_0, y_0)$ 的某一邻域内恒能唯一确定一个连续且具有连续导数的函数 $y = f(x)$，它满足条件 $y_0 = f(x_0)$，并有

$$
\frac {\mathrm{d} y}{\mathrm{d} x} = - \frac {F _ {x}}{F _ {y}}. \tag {5-2}
$$

公式(5-2)就是隐函数的求导公式.

这个定理我们不证.现仅就公式(5-2)作如下推导:

将方程(5-1)所确定的函数 $y = f(x)$ 代入(5-1)，得恒等式

$$
F (x, f (x)) \equiv 0,
$$

其左端可以看做是 $x$ 的一个复合函数, 求这个函数的全导数, 由于恒等式两端求导后仍然恒等, 即得

$$
\frac {\partial F}{\partial x} + \frac {\partial F}{\partial y} \frac {\mathrm{d} y}{\mathrm{d} x} = 0,
$$

因为 $F_{y}$ 连续，且 $F_{y}(x_{0},y_{0})\neq 0$ ，所以存在 $(x_0,y_0)$ 的一个邻域，在这个邻域内 $F_{y}\neq 0$ ，于是得

$$
\frac {\mathrm{d} y}{\mathrm{d} x} = - \frac {F _ {x}}{F _ {y}}.
$$

如果 $F(x,y)$ 的二阶偏导数也都连续，我们可以把等式(5-2)的两端看做 $x$ 的复合函数而再一次求导，即得

$$
\begin{array}{l} \frac {\mathrm{d} ^ {2} y}{\mathrm{d} x ^ {2}} = \frac {\partial}{\partial x} \left(- \frac {F _ {x}}{F _ {y}}\right) + \frac {\partial}{\partial y} \left(- \frac {F _ {x}}{F _ {y}}\right) \frac {\mathrm{d} y}{\mathrm{d} x} \\ = - \frac {F _ {x x} F _ {y} - F _ {y x} F _ {x}}{F _ {y} ^ {2}} - \frac {F _ {x y} F _ {y} - F _ {y y} F _ {x}}{F _ {y} ^ {2}} \left(- \frac {F _ {x}}{F _ {y}}\right) = - \frac {F _ {x x} F _ {y} ^ {2} - 2 F _ {x y} F _ {x} F _ {y} + F _ {y y} F _ {x} ^ {2}}{F _ {y} ^ {3}}. \\ \end{array}
$$

83

---

第九章 多元函数微分法及其应用

例1 验证方程 $x^{2} + y^{2} - 1 = 0$ 在点(0,1)的某一邻域内能唯一确定一个有连续导数，当 $x = 0, y = 1$ 时的隐函数 $y = f(x)$，并求这函数的一阶与二阶导数在 $x = 0$ 的值.

解 设 $F(x, y) = x^2 + y^2 - 1$，则 $F_x = 2x, F_y = 2y, F_x(0, 1) = 0, F_y(0, 1) = 2 \neq 0$. 因此由定理1可知，方程 $x^2 + y^2 - 1 = 0$ 在点 $(0, 1)$ 的某邻域内能唯一确定一个有连续导数，当 $x = 0, y = 1$ 时的函数 $y = f(x)$.

下面求这函数的一阶及二阶导数.

$$
\begin{array}{l} \frac{\mathrm{d}y}{\mathrm{d}x} = -\frac{F_x}{F_y} = -\frac{x}{y},\quad \frac{\mathrm{d}y}{\mathrm{d}x}\bigg|_{\substack{x = 0\\ y = 1}} = 0; \\ \frac {\mathrm{d} ^ {2} y}{\mathrm{d} x ^ {2}} = - \frac {y - x y ^ {\prime}}{y ^ {2}} = - \frac {y - x \left(- \frac {x}{y}\right)}{y ^ {2}} = - \frac {y ^ {2} + x ^ {2}}{y ^ {3}} = - \frac {1}{y ^ {3}}, \quad \left. \frac {\mathrm{d} ^ {2} y}{\mathrm{d} x ^ {2}} \right| _ {x = 0 \atop y = 1} = - 1. \\ \end{array}
$$

隐函数存在定理还可以推广到多元函数.既然一个二元方程(5-1)可以确定一个一元隐函数,那么一个三元方程

$$
F (x, y, z) = 0 \tag {5-3}
$$

就有可能确定一个二元隐函数.

与定理1一样, 我们同样可以由三元函数  $F(x,y,z)$  的性质来断定由方程  $F(x,y,z)=0$  所确定的二元函数  $z=f(x,y)$  的存在以及这个函数的性质. 这就是下面的定理.

隐函数存在定理2 设函数 $F(x, y, z)$ 在点 $P(x_0, y_0, z_0)$ 的某一邻域内具有连续偏导数，且 $F(x_0, y_0, z_0) = 0, F_z(x_0, y_0, z_0) \neq 0$，则方程 $F(x, y, z) = 0$ 在点 $(x_0, y_0, z_0)$ 的某一邻域内恒能唯一确定一个连续且具有连续偏导数的函数 $z = f(x, y)$，它满足条件 $z_0 = f(x_0, y_0)$，并有

$$
\frac {\partial z}{\partial x} = - \frac {F _ {x}}{F _ {z}}, \quad \frac {\partial z}{\partial y} = - \frac {F _ {y}}{F _ {z}}. \tag {5-4}
$$

这个定理我们不证.与定理1类似,仅就公式(5-4)作如下推导:

由于 $F[x,y,f(x,y)]\equiv 0$ ，将上式两端分别对 $x$ 和 $y$ 求导，应用复合函数求导法则得

$$
F _ {x} + F _ {z} \frac {\partial z}{\partial x} = 0, \quad F _ {y} + F _ {z} \frac {\partial z}{\partial y} = 0.
$$

因为 $F_{z}$ 连续，且 $F_{z}(x_{0},y_{0},z_{0})\neq 0$ ，所以存在点 $(x_0,y_0,z_0)$ 的一个邻域，在这个邻域内$F_{z}\neq 0$ ，于是得

$$
\frac {\partial z}{\partial x} = - \frac {F _ {x}}{F _ {z}}, \quad \frac {\partial z}{\partial y} = - \frac {F _ {y}}{F _ {z}}.
$$

84

---

第五节 隐函数的求导公式

例2 设 $x^{2} + y^{2} + z^{2} - 4z = 0$ ，求 $\frac{\partial^2z}{\partial x^2}$

解 设 $F(x, y, z) = x^2 + y^2 + z^2 - 4z$，则 $F_x = 2x, F_z = 2z - 4$. 当 $z \neq 2$ 时，应用公式 (5-4)，得

$$
\frac {\partial z}{\partial x} = \frac {x}{2 - z}.
$$

再一次对 $x$ 求偏导数, 得

$$
\frac {\partial^ {2} z}{\partial x ^ {2}} = \frac {(2 - z) + x \frac {\partial z}{\partial x}}{(2 - z) ^ {2}} = \frac {(2 - z) + x \cdot \frac {x}{2 - z}}{(2 - z) ^ {2}} = \frac {(2 - z) ^ {2} + x ^ {2}}{(2 - z) ^ {3}}.
$$

![](../../raw/pages_0065-0096/images/page_91_image_6.jpg)

## 二、方程组的情形

下面我们将隐函数存在定理作另一方面的推广.我们不仅增加方程中变量的个数,而且增加方程的个数.例如,考虑方程组

$$
\left\{ \begin{array}{l} F (x, y, u, v) = 0, \\ G (x, y, u, v) = 0. \end{array} \right. \tag {5-5}
$$

这时,在四个变量中,一般只能有两个变量独立变化,因此方程组(5-5)就有可能确定两个二元函数.在这种情况下,我们可以由函数F,G的性质来断定由方程组(5-5)所确定的两个二元函数的存在以及它们的性质.我们有下面的定理.

隐函数存在定理3 设 $F(x, y, u, v), G(x, y, u, v)$ 在点 $P(x_0, y_0, u_0, v_0)$ 的某一邻域内具有对各个变量的连续偏导数，又 $F(x_0, y_0, u_0, v_0) = 0, G(x_0, y_0, u_0, v_0) = 0$，且偏导数所组成的函数行列式（或称雅可比（Jacobi）式）

$$
J = \frac {\partial (F , G)}{\partial (u , v)} = \left| \begin{array}{c c} \frac {\partial F}{\partial u} & \frac {\partial F}{\partial v} \\ \frac {\partial G}{\partial u} & \frac {\partial G}{\partial v} \end{array} \right|
$$

在点 $P(x_0, y_0, u_0, v_0)$ 不等于零，则方程组 $F(x, y, u, v) = 0, G(x, y, u, v) = 0$ 在点 $(x_0, y_0, u_0, v_0)$ 的某一邻域内恒能唯一确定一组连续且具有连续偏导数的函数 $u = u(x, y), v = v(x, y)$，它们满足条件 $u_0 = u(x_0, y_0), v_0 = v(x_0, y_0)$，并有

$$
\frac {\partial u}{\partial x} = - \frac {1}{J} \frac {\partial (F , G)}{\partial (x , v)} = - \frac {\left| \begin{array}{c c} F _ {x} & F _ {v} \\ G _ {x} & G _ {v} \end{array} \right|}{\left| \begin{array}{c c} F _ {u} & F _ {v} \\ G _ {u} & G _ {v} \end{array} \right|},
$$

85

---

第九章 多元函数微分法及其应用

$$
\frac {\partial v}{\partial x} = - \frac {1}{J} \frac {\partial (F , G)}{\partial (u , x)} = - \frac {\left| \begin{array}{l l} F _ {u} & F _ {x} \\ G _ {u} & G _ {x} \end{array} \right|}{\left| \begin{array}{l l} F _ {u} & F _ {v} \\ G _ {u} & G _ {v} \end{array} \right|}, \tag {5-6}
$$

$$
\frac {\partial u}{\partial y} = - \frac {1}{J} \frac {\partial (F , G)}{\partial (y , v)} = - \frac {\left| \begin{array}{c c} F _ {y} & F _ {v} \\ G _ {y} & G _ {v} \end{array} \right|}{\left| \begin{array}{c c} F _ {u} & F _ {v} \\ G _ {u} & G _ {v} \end{array} \right|},
$$

$$
\frac {\partial v}{\partial y} = - \frac {1}{J} \frac {\partial (F , G)}{\partial (u , y)} = - \frac {\left| \begin{array}{l l} F _ {u} & F _ {y} \\ G _ {u} & G _ {y} \end{array} \right|}{\left| \begin{array}{l l} F _ {u} & F _ {v} \\ G _ {u} & G _ {v} \end{array} \right|}.
$$

这个定理我们不证.与前两个定理类似,下面仅就公式(5-6)作如下推导:

由于

$$
F [ x, y, u (x, y), v (x, y) ] \equiv 0, \quad G [ x, y, u (x, y), v (x, y) ] \equiv 0,
$$

将恒等式两端分别对 $x$ 求导，应用复合函数求导法则得

$$
\left\{ \begin{array}{l} F _ {x} + F _ {u} \frac {\partial u}{\partial x} + F _ {v} \frac {\partial v}{\partial x} = 0, \\ G _ {x} + G _ {u} \frac {\partial u}{\partial x} + G _ {v} \frac {\partial v}{\partial x} = 0. \end{array} \right.
$$

这是关于 $\frac{\partial u}{\partial x}$ 和 $\frac{\partial v}{\partial x}$ 的线性方程组，由假设可知在点 $P(x_{0},y_{0},u_{0},v_{0})$ 的一个邻域内，系数行列式

$$
J = \left| \begin{array}{c c} F _ {u} & F _ {v} \\ G _ {u} & G _ {v} \end{array} \right| \neq 0,
$$

从而可解出 $\frac{\partial u}{\partial x}, \frac{\partial v}{\partial x}$, 得

$$
\frac {\partial u}{\partial x} = - \frac {1}{J} \frac {\partial (F , G)}{\partial (x , v)}, \quad \frac {\partial v}{\partial x} = - \frac {1}{J} \frac {\partial (F , G)}{\partial (u , x)}.
$$

同理,可得

$$
\frac {\partial u}{\partial y} = - \frac {1}{J} \frac {\partial (F , G)}{\partial (y , v)}, \quad \frac {\partial v}{\partial y} = - \frac {1}{J} \frac {\partial (F , G)}{\partial (u , y)}.
$$

例3 设 $xu - yv = 0, yu + xv = 1$，求 $\frac{\partial u}{\partial x}, \frac{\partial u}{\partial y}, \frac{\partial v}{\partial x}$ 和 $\frac{\partial v}{\partial y}$.

86

---

第五节 隐函数的求导公式

解 此题可直接利用公式(5-6)，但也可依照推导公式(5-6)的方法来求解.下面我们用后一种方法来做.

将所给方程的两端对 x 求导并移项, 得

$$
\left\{ \begin{array}{l} x \frac {\partial u}{\partial x} - y \frac {\partial v}{\partial x} = - u, \\ y \frac {\partial u}{\partial x} + x \frac {\partial v}{\partial x} = - v. \end{array} \right.
$$

在 $J = \left| \begin{array}{cc}x & -y\\ y & x \end{array} \right| = x^{2} + y^{2}\neq 0$ 的条件下，

$$
\frac {\partial u}{\partial x} = \frac {\left| \begin{array}{c c} - u & - y \\ - v & x \end{array} \right|}{\left| \begin{array}{c c} x & - y \\ y & x \end{array} \right|} = - \frac {x u + y v}{x ^ {2} + y ^ {2}}, \quad \frac {\partial v}{\partial x} = \frac {\left| \begin{array}{c c} x & - u \\ y & - v \end{array} \right|}{\left| \begin{array}{c c} x & - y \\ y & x \end{array} \right|} = \frac {y u - x v}{x ^ {2} + y ^ {2}}.
$$

将所给方程的两端对 $y$ 求导. 用同样方法在 $J = x^{2} + y^{2} \neq 0$ 的条件下可得

$$
\frac {\partial u}{\partial y} = \frac {x v - y u}{x ^ {2} + y ^ {2}}, \quad \frac {\partial v}{\partial y} = - \frac {x u + y v}{x ^ {2} + y ^ {2}}.
$$

例4 设函数 $x = x(u, v), y = y(u, v)$ 在点 $(u, v)$ 的某一邻域内连续且有连续偏导数，又

$$
\frac {\partial (x , y)}{\partial (u , v)} \neq 0.
$$

(1) 证明方程组

$$
\left\{ \begin{array}{l} x = x (u, v), \\ y = y (u, v) \end{array} \right. \tag {5-7}
$$

在点 $(x,y,u,v)$ 的某一邻域内唯一确定一组连续且具有连续偏导数的反函数 $u = u(x,y)$, $v = v(x,y)$.

(2) 求反函数  $u = u(x, y)$ ,  $v = v(x, y)$  对 x, y 的偏导数.

解（1）将方程组(5-7)改写成

$$
\left\{ \begin{array}{l} F (x, y, u, v) \equiv x - x (u, v) = 0, \\ G (x, y, u, v) \equiv y - y (u, v) = 0. \end{array} \right.
$$

则按假设

$$
J = \frac {\partial (F , G)}{\partial (u , v)} = \frac {\partial (x , y)}{\partial (u , v)} \neq 0.
$$

由隐函数存在定理 3, 即得所要证的结论.

(2) 将方程组(5-7)所确定的反函数  $u=u(x,y)$ ,  $v=v(x,y)$  代入(5-7), 即得

87

---

第九章 多元函数微分法及其应用

$$
\left\{ \begin{array}{l} x \equiv x [ u (x, y), v (x, y) ], \\ y \equiv y [ u (x, y), v (x, y) ]. \end{array} \right.
$$

将上述恒等式两端分别对 x 求偏导数, 得

$$
\left\{ \begin{array}{l} 1 = \frac {\partial x}{\partial u} \frac {\partial u}{\partial x} + \frac {\partial x}{\partial v} \frac {\partial v}{\partial x}, \\ 0 = \frac {\partial y}{\partial u} \frac {\partial u}{\partial x} + \frac {\partial y}{\partial v} \frac {\partial v}{\partial x}. \end{array} \right.
$$

由于 $J \neq 0$ ，故可解得

$$
\frac {\partial u}{\partial x} = \frac {1}{J} \frac {\partial y}{\partial v}, \quad \frac {\partial v}{\partial x} = - \frac {1}{J} \frac {\partial y}{\partial u}.
$$

释疑解难

9-4

同理,可得

$$
\frac {\partial u}{\partial y} = - \frac {1}{J} \frac {\partial x}{\partial v}, \quad \frac {\partial v}{\partial y} = \frac {1}{J} \frac {\partial x}{\partial u}.
$$

## 习题9-5

1. 设  $\sin y + e^{x} - xy^{2} = 0$ , 求  $\frac{dy}{dx}$ .

2. 设  $\ln\sqrt{x^{2}+y^{2}}=\arctan\frac{y}{x}$ ，求  $\frac{dy}{dx}$ .

3. 设 $x + 2y + z - 2\sqrt{xyz} = 0$，求 $\frac{\partial z}{\partial x}$ 及 $\frac{\partial z}{\partial y}$.

4. 设 $\frac{x}{z}=\ln\frac{z}{y}$ ，求 $\frac{\partial z}{\partial x}$ 及 $\frac{\partial z}{\partial y}$ .

5. 设 $2\sin (x + 2y - 3z) = x + 2y - 3z$，证明 $\frac{\partial z}{\partial x} + \frac{\partial z}{\partial y} = 1$.

6. 设 $x = x(y, z), y = y(x, z), z = z(x, y)$ 都是由方程 $F(x, y, z) = 0$ 所确定的具有连续偏导数的函数，证明 $\frac{\partial x}{\partial y} \cdot \frac{\partial y}{\partial z} \cdot \frac{\partial z}{\partial x} = -1$.

7. 设  $\Phi(u,v)$  具有连续偏导数, 证明由方程  $\Phi(cx-az, cy-bz)=0$  所确定的函数  $z=f(x,y)$  满足  $a\frac{\partial z}{\partial x}+b\frac{\partial z}{\partial y}=c$ .

8. 设  $z=z(x,y)$  是由方程  $2xz-2xyz+\ln(xyz)=0$  所确定的隐函数, 求 dz.

\* 9. 设 $\mathrm{e}^z - xyz = 0$, 求 $\frac{\partial^2 z}{\partial x^2}$.

\* 10. 设 $z^3 - 3xyz = a^3$, 求 $\frac{\partial^2 z}{\partial x \partial y}$.

11. 求由下列方程组所确定的函数的导数或偏导数:

88

---

第六节 多元函数微分学的几何应用

(1) 设  $\left\{\begin{aligned} z &= x^{2} + y^{2}, \\ x^{2} + 2y^{2} + 3z^{2} &= 20, \end{aligned}\right.$  求  $\frac{dy}{dx}, \frac{dz}{dx};$
(2) 设  $\left\{\begin{aligned} x+y+z &= 0, \\ x^{2}+y^{2}+z^{2} &= 1, \end{aligned}\right.$  求  $\frac{dx}{dz}, \frac{dy}{dz};$
(3) 设  $\left\{\begin{aligned} u &= f(ux, v + y), \\ v &= g(u - x, v^{2}y), \end{aligned}\right.$  其中 f, g 具有一阶连续偏导数，求  $\frac{\partial u}{\partial x}, \frac{\partial v}{\partial x}$ ;
(4) 设  $\left\{\begin{aligned} x &= e^{u} + u \sin v, \\ y &= e^{u} - u \cos v, \end{aligned}\right.$  求  $\frac{\partial u}{\partial x}, \frac{\partial u}{\partial y}, \frac{\partial v}{\partial x}, \frac{\partial v}{\partial y}.$

12. 设 $y = f(x, t)$，而 $t = t(x, y)$ 是由方程 $F(x, y, t) = 0$ 所确定的函数，其中 $f, F$ 都具有一阶连续偏导数。试证明

$$
\frac {\mathrm{d} y}{\mathrm{d} x} = \frac {\frac {\partial f}{\partial x} \frac {\partial F}{\partial t} - \frac {\partial f}{\partial t} \frac {\partial F}{\partial x}}{\frac {\partial f}{\partial t} \frac {\partial F}{\partial y} + \frac {\partial F}{\partial t}}.
$$

## 第六节 多元函数微分学的几何应用

本节先介绍一元向量值函数及其导数,再讨论多元函数微分学的几何应用.

## 一、一元向量值函数及其导数

由空间解析几何知道,空间曲线  $\Gamma$  的参数方程为

$$
\left\{ \begin{array}{l} x = \varphi (t), \\ y = \psi (t), \quad t \in [ \alpha , \beta ]. \\ z = \omega (t), \end{array} \right. \tag {6-1}
$$

方程(6-1)也可以写成向量形式.若记

$$
r = x i + y j + z k, \quad f (t) = \varphi (t) i + \psi (t) j + \omega (t) k,
$$

则方程(6-1)就成为向量方程

$$
r = f (t), \quad t \in [ \alpha , \beta ]. \tag {6-2}
$$

方程(6-2)确定了一个映射 $f:[\alpha, \beta] \to \mathbb{R}^3$. 由于这个映射将每一个 $t \in [\alpha, \beta]$ 映成一个向量 $f(t) \in \mathbb{R}^3$, 故称这映射为一元向量值函数. 一般地, 有如下定义.

定义1 设数集 $D \subset \mathbb{R}$, 则称映射 $f: D \to \mathbb{R}^n$ 为一元向量值函数, 通常记为

$$
r = f (t), \quad t \in D,
$$

其中数集 D 称为函数的定义域, t 称为自变量, r 称为因变量.

一元向量值函数是普通一元函数的推广. 现在, 自变量 t 依然取实数值, 但因变量

89

---

第九章 多元函数微分法及其应用

r 不取实数值, 而取值为 n 维向量.

在本教材中, 只讨论一元向量值函数, 并对因变量的取值以 n=3 的情形作为代表, 即 r 的取值为 3 维向量. 为简单起见, 以下将一元向量值函数简称为向量值函数, 并把普通的实值函数称为数量函数.

在 $\mathbf{R}^3$ 中, 若向量值函数 $f(t)$, $t \in D$ 的三个分量函数依次为 $f_1(t)$, $f_2(t)$, $f_3(t)$, $t \in D$, 则向量值函数 $f(t)$ 可表示为

$$
\boldsymbol {f} (t) = f _ {1} (t) \boldsymbol {i} + f _ {2} (t) \boldsymbol {j} + f _ {3} (t) \boldsymbol {k}, \quad t \in D \tag {6-3}
$$

或

$$
f (t) = (f _ {1} (t), f _ {2} (t), f _ {3} (t)), \quad t \in D. \tag {$6-3^{\prime$}}
$$

设(变)向量 r 的起点取在坐标系的原点 O 处, 终点在 M 处, 即  $r = \overrightarrow{OM}$  (图 9-6). 当 t 改变时, r 跟着改变, 从而终点 M 也随之改变. 终点 M 的轨迹(记作曲线  $\Gamma$ ) 称为向量值函数  $\boldsymbol{r} = \boldsymbol{f}(t) \quad (t \in D)$  的终端曲线, 曲线  $\Gamma$  也称为向量值函数  $\boldsymbol{r} = \boldsymbol{f}(t) \quad (t \in D)$  的图形.

由于向量值函数 $r = f(t) (t \in D)$ 与空间曲线 $\Gamma$ 是一一对应的, 因此

![](../../raw/pages_0097-0128/images/page_96_image_9.jpg)

<details>
<summary>text_image</summary>

z
M
Γ
r
O
x
y
</details>

图9-6

$$
\boldsymbol {r} = \boldsymbol {f} (t) = (f _ {1} (t), f _ {2} (t), f _ {3} (t)), \quad t \in D \tag {6-4}
$$

称为曲线  $\Gamma$  的向量方程.

根据  $R^{3}$  中的向量的线性运算及向量的模的概念, 可以类似于定义数量函数的极限、连续、导数等概念的形式来定义向量值函数的相应概念, 现简述如下:

定义2 设向量值函数 $f(t)$ 在点 $t_0$ 的某一去心邻域内有定义, 如果存在一个常向量 $r_0$, 对于任意给定的正数 $\varepsilon$, 总存在正数 $\delta$, 使得当 $t$ 满足 $0 < |t - t_0| < \delta$ 时, 对应的函数值 $f(t)$ 都满足不等式

$$
\mid f (t) - r _ {0} \mid <   \varepsilon ,
$$

那么常向量 $r_0$ 就叫做向量值函数 $f(t)$ 当 $t \to t_0$ 时的极限，记作

$$
\lim _ {t \to t _ {0}} f (  t  ) = r _ {0} \quad \text {或} \quad f (  t  ) \longrightarrow r _ {0}  ,   t \longrightarrow t _ {0}.
$$

容易证明:向量值函数 $f(t)$ 当 $t\to t_{0}$ 时的极限存在的充分必要条件是: $f(t)$ 的三个分量函数 $f_{1}(t)$ , $f_{2}(t)$ , $f_{3}(t)$ 当 $t\to t_{0}$ 时的极限都存在;在函数 $f(t)$ 当 $t\to t_{0}$ 时的极限存在时,其极限

$$
\lim _ {t \to t _ {0}} f (t) = \left(\lim _ {t \to t _ {0}} f _ {1} (t), \lim _ {t \to t _ {0}} f _ {2} (t), \lim _ {t \to t _ {0}} f _ {3} (t)\right). \tag {6-5}
$$

设向量值函数 $f(t)$ 在点 $t_{0}$ 的某一邻域内有定义,若

$$
\lim _ {t \to t _ {0}} f (t) = f (t _ {0}),
$$

90

---

第六节 多元函数微分学的几何应用

则称向量值函数 $f(t)$ 在 $t_{0}$ 连续.

向量值函数 $f(t)$ 在 $t_{0}$ 连续的充分必要条件是: $f(t)$ 的三个分量函数 $f_{1}(t), f_{2}(t), f_{3}(t)$ 都在 $t_{0}$ 连续.

设向量值函数 $f(t), t \in D$. 若 $D_1 \subset D$, $f(t)$ 在 $D_1$ 中的每一点处都连续, 则称 $f(t)$ 在 $D_1$ 上连续, 并称 $f(t)$ 是 $D_1$ 上的连续函数.

下面给出向量值函数的导数(或导向量)的定义.

定义3 设向量值函数 $r = f(t)$ 在点 $t_0$ 的某一邻域内有定义, 如果

$$
\lim _ {\Delta t \to 0} \frac {\Delta r}{\Delta t} = \lim _ {\Delta t \to 0} \frac {f (t _ {0} + \Delta t) - f (t _ {0})}{\Delta t}
$$

存在,那么就称这个极限向量为向量值函数  $r=f(t)$  在  $t_{0}$  处的导数或导向量,记作  $f'(t_{0})$  或  $\frac{dr}{dt}\bigg|_{t=t_{0}}$ .

设向量值函数 $r = f(t), t \in D$. 若 $D_{1} \subset D, f(t)$ 在 $D_{1}$ 中的每一点 $t$ 处都存在导向量 $f'(t)\left(\text{或}\frac{\mathrm{d}r}{\mathrm{d}t}\right)$, 则称 $f(t)$ 在 $D_{1}$ 上可导.

向量值函数 $f(t)$ 在 $t_0$ 可导（即存在导数）的充分必要条件是: $f(t)$ 的三个分量函数 $f_1(t), f_2(t), f_3(t)$ 都在 $t_0$ 可导；当 $f(t)$ 在 $t_0$ 可导时，其导数

$$
f ^ {\prime} (t _ {0}) = f _ {1} ^ {\prime} (t _ {0}) i + f _ {2} ^ {\prime} (t _ {0}) j + f _ {3} ^ {\prime} (t _ {0}) k. \tag {6-6}
$$

向量值函数的导数运算法则与数量函数的导数运算法则的形式相同,现列出如下:

设  $\boldsymbol{u}(t), \boldsymbol{v}(t)$  是可导的向量值函数, C 是常向量, c 是任一常数,  $\varphi(t)$  是可导的数量函数, 则

(1)  $\frac{d}{dt}C=0;$
(2) $\frac{\mathrm{d}}{\mathrm{d}t}\left[c\boldsymbol{u}(t)\right] = c\boldsymbol{u}'(t);$
(3) $\frac{\mathrm{d}}{\mathrm{d}t}[\boldsymbol{u}(t)\pm \boldsymbol{v}(t)] = \boldsymbol{u}'(t)\pm \boldsymbol{v}'(t);$
(4) $\frac{\mathrm{d}}{\mathrm{d}t}[\varphi(t)\boldsymbol{u}(t)] = \varphi'(t)\boldsymbol{u}(t) + \varphi(t)\boldsymbol{u}'(t);$
(5) $\frac{\mathrm{d}}{\mathrm{d}t}[\boldsymbol{u}(t)\cdot \boldsymbol{v}(t)] = \boldsymbol{u}'(t)\cdot \boldsymbol{v}(t) + \boldsymbol{u}(t)\cdot \boldsymbol{v}'(t);$
(6) $\frac{\mathrm{d}}{\mathrm{d}t}[\boldsymbol{u}(t)\times\boldsymbol{v}(t)]=\boldsymbol{u}'(t)\times\boldsymbol{v}(t)+\boldsymbol{u}(t)\times\boldsymbol{v}'(t);$
(7) $\frac{\mathrm{d}}{\mathrm{d}t}\boldsymbol{u}[\varphi (t)] = \varphi '(t)\boldsymbol{u}'[\varphi (t)]$.

91

---

第九章 多元函数微分法及其应用

仿照对数量函数的导数运算法则的证明方法,或对向量函数的分量运用对应的数量函数的导数运算法则,可以证明以上法则,读者可作为练习自行证明.

下面,讨论向量值函数  $r = f(t)$  的导向量的几何意义.

设空间曲线 $\Gamma$ 是向量值函数 $r = f(t), t \in D$ 的终端曲线，向量 $\overrightarrow{OM} = f(t_0), \overrightarrow{ON} = f(t_0 + \Delta t)$，如图9-7所示。又设导向量 $f'(t_0)$ 不是零向量。

当  $\Delta t > 0$  时, 向量  $\Delta r = f(t_{0} + \Delta t) - f(t_{0})$  的方向与 t 增大时点 M 移动的走向(以下简称 t 的增长方向)一致; 当

![](../../raw/pages_0097-0128/images/page_98_image_5.jpg)

<details>
<summary>text_image</summary>

z
M
f'(t₀)
Γ
f(t₀)
Δr
N
Δr
Δt
f(t₀+Δt)
O
x
y
</details>

图9-7

$\Delta t < 0$ 时，向量 $\Delta r = f(t_0 + \Delta t) - f(t_0)$ 的方向与 $t$ 的增长方向相反.但不论 $\Delta t > 0$ 或 $\Delta t < 0$ 向量 $\frac{\Delta r}{\Delta t} = \frac{1}{\Delta t}\Delta r$ 的方向总与 $t$ 的增长方向一致.于是，导向量 $f^{\prime}(t_{0}) = \lim_{\Delta t\to 0}\frac{\Delta r}{\Delta t}$ 是向量值函数 $r = f(t)$ 的终端曲线 $\Gamma$ 在点 $M$ 处的一个切向量，其方向与 $t$ 的增长方向一致.

设向量值函数  $r=f(t)$  是沿空间光滑曲线运动的质点 M 的位置向量，则向量值函数  $r=f(t)$  的导向量有以下的物理意义:

$v(t)=\frac{dr}{dt}$ 是质点 M 的速度向量, 其方向与曲线相切;

$a(t) = \frac{\mathrm{d}\boldsymbol{v}}{\mathrm{d}t} = \frac{\mathrm{d}^2\boldsymbol{r}}{\mathrm{d}t^2}$ 是质点 $M$ 的加速度向量.

例1 设 $f(t) = (\cos t)i + (\sin t)j + tk$，求 $\lim_{t\to \frac{\pi}{4}}f(t)$.

解 $\lim_{t\to \frac{\pi}{4}}f(t) = \left(\lim_{t\to \frac{\pi}{4}}\cos t\right)i + \left(\lim_{t\to \frac{\pi}{4}}\sin t\right)\boldsymbol {j} + \left(\lim_{t\to \frac{\pi}{4}}t\right)\boldsymbol {k} = \frac{\sqrt{2}}{2}\boldsymbol {i} + \frac{\sqrt{2}}{2}\boldsymbol {j} + \frac{\pi}{4}\boldsymbol {k}.$

例2 设空间曲线 $\Gamma$ 的向量方程为

$$
r = f (t) = (t ^ {2} + 1, 4 t - 3, 2 t ^ {2} - 6 t), \quad t \in \mathbf {R},
$$

求曲线  $\Gamma$  在与 t=2 相应的点处的单位切向量.

解 $f^{\prime}(t) = (2t,4,4t - 6),\quad t\in \mathbf{R},$

$$
f ^ {\prime} (2) = (4, 4, 2), \quad | f ^ {\prime} (2) | = \sqrt {4 ^ {2} + 4 ^ {2} + 2 ^ {2}} = 6.
$$

由导向量的几何意义知, 曲线  $\Gamma$  在与 t=2 相应的点处的一个单位切向量是  $\left(\frac{2}{3},\frac{2}{3},\frac{1}{3}\right)$ , 其方向与 t 的增长方向一致; 另一个单位切向量是  $\left(-\frac{2}{3},-\frac{2}{3},-\frac{1}{3}\right)$ , 其方向与 t 的增长方向相反.

例3 一个人在悬挂式滑翔机上由于快速上升气流而沿位置向量为 $r = f(t) = (3\cos t)i + (3\sin t)j + t^2 k$ 的路径螺旋式向上.求

92

---

第六节 多元函数微分学的几何应用

(1) 滑翔机在任意时刻 t 的速度向量和加速度向量;
(2) 滑翔机在任意时刻 t 的速率;
(3) 滑翔机的加速度与速度正交的时刻.

解 (1) $r = f(t) = (3\cos t)i + (3\sin t)j + t^2 k,$

$$
v = \frac {\mathrm{d} r}{\mathrm{d} t} = (- 3 \sin t) i + (3 \cos t) j + 2 t k,
$$

$$
\boldsymbol {a} = \frac {\mathrm{d} ^ {2} \boldsymbol {r}}{\mathrm{d} t ^ {2}} = (- 3 \cos t) \boldsymbol {i} - (3 \sin t) \boldsymbol {j} + 2 \boldsymbol {k}.
$$

(2) 速率是速度v的大小, 即

$$
\mid \boldsymbol {v} \mid = \sqrt {\left(- 3 \sin t\right) ^ {2} + \left(3 \cos t\right) ^ {2} + \left(2 t\right) ^ {2}} = \sqrt {9 + 4 t ^ {2}}.
$$

这一结果表明:滑翔机沿其路径升高时,运动得越来越快.

（3）由  $v \cdot a = 9 \sin t \cos t - 9 \sin t \cos t + 4t = 0$ ，得 t = 0。这表明:加速度与速度正交的唯一时刻是在 t = 0。

## 二、空间曲线的切线与法平面

设空间曲线  $\Gamma$  的参数方程为

$$
\left\{ \begin{array}{l} x = \varphi (t), \\ y = \psi (t), \quad t \in [ \alpha , \beta ]. \\ z = \omega (t), \end{array} \right. \tag {6-7}
$$

这里假定(6-7)式的三个函数都在 $[\alpha,\beta]$ 上可导,且三个导数不同时为零.

现在要求曲线  $\Gamma$  在其上一点  $M(x_{0}, y_{0}, z_{0})$  处的切线及法平面方程.

设与点 $M$ 对应的参数为 $t_0$, 记 $f(t) = (\varphi(t), \psi(t), \omega(t))$, $t \in [\alpha, \beta]$. 由向量值函数的导向量的几何意义知, 向量 $T = f'(t_0) = (\varphi'(t_0), \psi'(t_0), \omega'(t_0))$ 就是曲线 $\Gamma$ 在点 $M$ 处的一个切向量, 从而曲线 $\Gamma$ 在点 $M$ 处的切线方程为

$$
\frac {x - x _ {0}}{\varphi^ {\prime} (t _ {0})} = \frac {y - y _ {0}}{\psi^ {\prime} (t _ {0})} = \frac {z - z _ {0}}{\omega^ {\prime} (t _ {0})}. \tag {6-8}
$$

通过点 M 且与切线垂直的平面称为曲线  $\Gamma$  在点 M 处的法平面, 它是通过点  $M(x_{0}, y_{0}, z_{0})$  且以  $T = f'(t_{0})$  为法向量的平面, 因此法平面方程为

$$
\varphi^ {\prime} (t _ {0}) (x - x _ {0}) + \psi^ {\prime} (t _ {0}) (y - y _ {0}) + \omega^ {\prime} (t _ {0}) (z - z _ {0}) = 0. \tag {6-9}
$$

例 4 求曲线  $x=t, y=t^{2}, z=t^{3}$  在点  $(1,1,1)$  处的切线及法平面方程.

解 因为 $x_{t}^{\prime} = 1, y_{t}^{\prime} = 2t, z_{t}^{\prime} = 3t^{2}$, 而点 $(1,1,1)$ 所对应的参数 $t_0 = 1$, 所以

$$
T = (1, 2, 3).
$$

于是,切线方程为

93

---

第九章 多元函数微分法及其应用

$$
\frac {x - 1}{1} = \frac {y - 1}{2} = \frac {z - 1}{3},
$$

法平面方程为

$$
(x - 1) + 2 (y - 1) + 3 (z - 1) = 0,
$$

即

$$
x + 2 y + 3 z = 6.
$$

现在我们再来讨论空间曲线  $\Gamma$  的方程以另外两种形式给出的情形.

如果空间曲线 $\Gamma$ 的方程以

$$
\left\{ \begin{array}{l} y = \varphi (x), \\ z = \psi (x) \end{array} \right.
$$

的形式给出,取 x 为参数,它就可以表示为参数方程的形式

$$
\left\{ \begin{array}{l} x = x, \\ y = \varphi (x), \\ z = \psi (x). \end{array} \right.
$$

若 $\varphi (x),\psi (x)$ 都在 $x = x_0$ 处可导，则根据上面的讨论可知， $T = (1,\varphi '(x_0),\psi '(x_0))$ ，因此曲线 $\Gamma$ 在点 $M(x_0,y_0,z_0)$ 处的切线方程为

$$
\frac {x - x _ {0}}{1} = \frac {y - y _ {0}}{\varphi^ {\prime} (x _ {0})} = \frac {z - z _ {0}}{\psi^ {\prime} (x _ {0})}, \tag {6-10}
$$

在点 $M(x_0,y_0,z_0)$ 处的法平面方程为

$$
(x - x _ {0}) + \varphi^ {\prime} (x _ {0}) (y - y _ {0}) + \psi^ {\prime} (x _ {0}) (z - z _ {0}) = 0. \tag {6-11}
$$

设空间曲线 $\Gamma$ 的方程以

$$
\left\{ \begin{array}{l} F (x, y, z) = 0, \\ G (x, y, z) = 0 \end{array} \right. \tag {6-12}
$$

的形式给出, $M(x_{0},y_{0},z_{0})$ 是曲线 $\Gamma$ 上的一个点.又设F,G有对各个变量的连续偏导数,且

$$
\frac {\partial (F , G)}{\partial (y , z)} \bigg | _ {(x _ {0}, y _ {0}, z _ {0})} \neq 0.
$$

这时方程组(6-12)在点 $M(x_0, y_0, z_0)$ 的某一邻域内确定了一组函数 $y = \varphi(x)$, $z = \psi(x)$. 要求曲线 $\Gamma$ 在点 $M$ 处的切线方程和法平面方程, 只要求出 $\varphi'(x_0), \psi'(x_0)$, 然后代入(6-10)、(6-11)两式就行了. 为此, 我们在恒等式

$$
F [ x, \varphi (x), \psi (x) ] \equiv 0, \quad G [ x, \varphi (x), \psi (x) ] \equiv 0
$$

两端分别对 $x$ 求全导数, 得

94

---

第六节 多元函数微分学的几何应用

$$
\left\{ \begin{array}{l} \frac {\partial F}{\partial x} + \frac {\partial F}{\partial y} \frac {\mathrm{d} y}{\mathrm{d} x} + \frac {\partial F}{\partial z} \frac {\mathrm{d} z}{\mathrm{d} x} = 0, \\ \frac {\partial G}{\partial x} + \frac {\partial G}{\partial y} \frac {\mathrm{d} y}{\mathrm{d} x} + \frac {\partial G}{\partial z} \frac {\mathrm{d} z}{\mathrm{d} x} = 0. \end{array} \right.
$$

由假设可知,在点 M 的某个邻域内

$$
J = \frac {\partial (F , G)}{\partial (y , z)} \neq 0,
$$

故可解得

$$
\frac {\mathrm{d} y}{\mathrm{d} x} = \varphi^ {\prime} (x) = \frac {\left| \begin{array}{l l} F _ {z} & F _ {x} \\ G _ {z} & G _ {x} \end{array} \right|}{\left| \begin{array}{l l} F _ {y} & F _ {z} \\ G _ {y} & G _ {z} \end{array} \right|}, \quad \frac {\mathrm{d} z}{\mathrm{d} x} = \psi^ {\prime} (x) = \frac {\left| \begin{array}{l l} F _ {x} & F _ {y} \\ G _ {x} & G _ {y} \end{array} \right|}{\left| \begin{array}{l l} F _ {y} & F _ {z} \\ G _ {y} & G _ {z} \end{array} \right|}.
$$

于是 $T = (1, \varphi'(x_0), \psi'(x_0))$ 是曲线 $\Gamma$ 在点 $M$ 处的一个切向量，这里

$$
\varphi^ {\prime} (x _ {0}) = \frac {\left| \begin{array}{c c} F _ {z} & F _ {x} \\ G _ {z} & G _ {x} \end{array} \right| _ {M}}{\left| \begin{array}{c c} F _ {y} & F _ {z} \\ G _ {y} & G _ {z} \end{array} \right| _ {M}}, \quad \psi^ {\prime} (x _ {0}) = \frac {\left| \begin{array}{c c} F _ {x} & F _ {y} \\ G _ {x} & G _ {y} \end{array} \right| _ {M}}{\left| \begin{array}{c c} F _ {y} & F _ {z} \\ G _ {y} & G _ {z} \end{array} \right| _ {M}},
$$

分子、分母中带下标 $M$ 的行列式表示行列式在点 $M(x_0, y_0, z_0)$ 的值. 把上面的切向量 $T$ 乘 $\left| \begin{array}{cc} F_y & F_z \\ G_y & G_z \end{array} \right|_M$, 得

$$
\boldsymbol {T} _ {1} = \left(\left| \begin{array}{c c} F _ {y} & F _ {z} \\ G _ {y} & G _ {z} \end{array} \right| _ {M}, \left| \begin{array}{c c} F _ {z} & F _ {x} \\ G _ {z} & G _ {x} \end{array} \right| _ {M}, \left| \begin{array}{c c} F _ {x} & F _ {y} \\ G _ {x} & G _ {y} \end{array} \right| _ {M}\right),
$$

这也是曲线 $\Gamma$ 在点 $M$ 处的一个切向量. 由此可写出曲线 $\Gamma$ 在点 $M(x_0, y_0, z_0)$ 处的切线方程为

$$
\frac {x - x _ {0}}{\left| \begin{array}{c c} F _ {y} & F _ {z} \\ G _ {y} & G _ {z} \end{array} \right| _ {M}} = \frac {y - y _ {0}}{\left| \begin{array}{c c} F _ {z} & F _ {x} \\ G _ {z} & G _ {x} \end{array} \right| _ {M}} = \frac {z - z _ {0}}{\left| \begin{array}{c c} F _ {x} & F _ {y} \\ G _ {x} & G _ {y} \end{array} \right| _ {M}}, \tag {6-13}
$$

曲线 $\Gamma$ 在点 $M(x_0, y_0, z_0)$ 处的法平面方程为

$$
\left| \begin{array}{c c} F _ {y} & F _ {z} \\ G _ {y} & G _ {z} \end{array} \right| _ {M} (x - x _ {0}) + \left| \begin{array}{c c} F _ {z} & F _ {x} \\ G _ {z} & G _ {x} \end{array} \right| _ {M} (y - y _ {0}) + \left| \begin{array}{c c} F _ {x} & F _ {y} \\ G _ {x} & G _ {y} \end{array} \right| _ {M} (z - z _ {0}) = 0. \tag {6-14}
$$

如果 $\frac{\partial(F,G)}{\partial(y,z)}\bigg|_M = 0$ 而 $\frac{\partial(F,G)}{\partial(z,x)}\bigg|_M,\frac{\partial(F,G)}{\partial(x,y)}\bigg|_M$ 中至少有一个不等于零，那么我们可得同样的结果.

95

---

第九章 多元函数微分法及其应用

例 5 求曲线  $x^{2}+y^{2}+z^{2}=6, x+y+z=0$  在点  $(1,-2,1)$  处的切线及法平面方程.

解 这里可直接利用公式(6-13)及(6-14)来解,但下面我们依照推导公式的方法来做.

将所给方程的两端对 x 求导并移项, 得

$$
\left\{ \begin{array}{l} y \frac {\mathrm{d} y}{\mathrm{d} x} + z \frac {\mathrm{d} z}{\mathrm{d} x} = - x, \\ \frac {\mathrm{d} y}{\mathrm{d} x} + \frac {\mathrm{d} z}{\mathrm{d} x} = - 1. \end{array} \right.
$$

由此得

$$
\begin{array}{l} \frac {\mathrm{d} y}{\mathrm{d} x} = \frac {\left| \begin{array}{c c} - x & z \\ - 1 & 1 \end{array} \right|}{\left| \begin{array}{c c} y & z \\ 1 & 1 \end{array} \right|} = \frac {z - x}{y - z}, \quad \frac {\mathrm{d} z}{\mathrm{d} x} = \frac {\left| \begin{array}{c c} y & - x \\ 1 & - 1 \end{array} \right|}{\left| \begin{array}{c c} y & z \\ 1 & 1 \end{array} \right|} = \frac {x - y}{y - z}. \\ \frac {\mathrm{d} y}{\mathrm{d} x} \bigg | _ {(1, - 2, 1)} = 0, \quad \frac {\mathrm{d} z}{\mathrm{d} x} \bigg | _ {(1, - 2, 1)} = - 1. \\ \end{array}
$$

从而

$$
T = (1, 0, - 1).
$$

故所求切线方程为

$$
\frac {x - 1}{1} = \frac {y + 2}{0} = \frac {z - 1}{- 1},
$$

法平面方程为

$$
(x - 1) + 0 \cdot (y + 2) - (z - 1) = 0,
$$

即

$$
x - z = 0.
$$

## 三、曲面的切平面与法线

我们先讨论由隐式给出曲面方程

$$
F (x, y, z) = 0 \tag {6-15}
$$

的情形,然后把由显式给出的曲面方程  $z=f(x,y)$  作为它的特殊情形.

设曲面 $\Sigma$ 由方程(6-15)给出，$M(x_0, y_0, z_0)$ 是曲面 $\Sigma$ 上的一点，并设函数 $F(x, y, z)$ 的偏导数在该点连续且不同时为零。在曲面 $\Sigma$ 上，通过点 $M$ 任意引一条曲线 $\Gamma$（图9-8），假定曲线 $\Gamma$ 的参数方程为

![](../../raw/pages_0097-0128/images/page_102_image_20.jpg)

<details>
<summary>text_image</summary>

z
n
T
M
Γ
Σ
O
y
x
</details>

图9-8

图

释疑解难

9-5

96

---

第六节 多元函数微分学的几何应用

$$
x = \varphi (t), y = \psi (t), z = \omega (t) \quad (\alpha \leqslant t \leqslant \beta), \tag {6-16}
$$

$t=t_{0}$  对应于点  $M(x_{0},y_{0},z_{0})$  且  $\varphi'(t_{0}),\psi'(t_{0}),\omega'(t_{0})$  不全为零，则由(6-8)式可得这曲线的切线方程为

$$
\frac {x - x _ {0}}{\varphi^ {\prime} (t _ {0})} = \frac {y - y _ {0}}{\psi^ {\prime} (t _ {0})} = \frac {z - z _ {0}}{\omega^ {\prime} (t _ {0})}.
$$

我们现在要证明,在曲面 $\Sigma$ 上通过点 $M$ 且在点 $M$ 处具有切线的任何曲线,它们在点 $M$ 处的切线都在同一个平面上.事实上,因为曲线 $\Gamma$ 完全在曲面 $\Sigma$ 上,所以有恒等式

$$
F [ \varphi (t), \psi (t), \omega (t) ] \equiv 0,
$$

又因为 $F(x,y,z)$ 在点 $(x_0,y_0,z_0)$ 处有连续偏导数，且 $\varphi'(t_0),\psi'(t_0)$ 和 $\omega'(t_0)$ 存在，所以这恒等式左端的复合函数在 $t = t_0$ 时有全导数，且这全导数等于零:

$$
\frac {\mathrm{d}}{\mathrm{d} t} F [ \varphi (t), \psi (t), \omega (t) ] \Big | _ {t = t _ {0}} = 0,
$$

即有

$$
F _ {x} (x _ {0}, y _ {0}, z _ {0}) \varphi^ {\prime} (t _ {0}) + F _ {y} (x _ {0}, y _ {0}, z _ {0}) \psi^ {\prime} (t _ {0}) + F _ {z} (x _ {0}, y _ {0}, z _ {0}) \omega^ {\prime} (t _ {0}) = 0. \tag {6-17}
$$

引入向量

$$
\boldsymbol {n} = (F _ {x} (x _ {0}, y _ {0}, z _ {0}), F _ {y} (x _ {0}, y _ {0}, z _ {0}), F _ {z} (x _ {0}, y _ {0}, z _ {0})) ,
$$

则(6-17)式表示曲线(6-16)在点 $M$ 处的切向量

$$
\boldsymbol {T} = (\varphi^ {\prime} (t _ {0}), \psi^ {\prime} (t _ {0}), \omega^ {\prime} (t _ {0}))
$$

与向量 $n$ 垂直. 因为曲线 (6-16) 是曲面上通过点 $M$ 的任意一条曲线, 它们在点 $M$ 的切线都与同一个向量 $n$ 垂直, 所以曲面上通过点 $M$ 的一切曲线在点 $M$ 的切线都在同一个平面上 (图 9-8). 这个平面称为曲面 $\Sigma$ 在点 $M$ 的切平面. 这切平面的方程是

$$
F _ {x} \left(x _ {0}, y _ {0}, z _ {0}\right) \left(x - x _ {0}\right) + F _ {y} \left(x _ {0}, y _ {0}, z _ {0}\right) \left(y - y _ {0}\right) + F _ {z} \left(x _ {0}, y _ {0}, z _ {0}\right) \left(z - z _ {0}\right) = 0. \tag {6-18}
$$

通过点 $M(x_0,y_0,z_0)$ 且垂直于切平面(6-18)的直线称为曲面在该点的法线.法线方程是

$$
\frac {x - x _ {0}}{F _ {x} (x _ {0} , y _ {0} , z _ {0})} = \frac {y - y _ {0}}{F _ {y} (x _ {0} , y _ {0} , z _ {0})} = \frac {z - z _ {0}}{F _ {z} (x _ {0} , y _ {0} , z _ {0})}. \tag {6-19}
$$

垂直于曲面上切平面的向量称为曲面的法向量.向量

$$
\boldsymbol {n} = (F _ {x} (x _ {0}, y _ {0}, z _ {0}), F _ {y} (x _ {0}, y _ {0}, z _ {0}), F _ {z} (x _ {0}, y _ {0}, z _ {0}))
$$

就是曲面 $\Sigma$ 在点 $M$ 处的一个法向量.

现在来考虑曲面方程

$$
z = f (x, y). \tag {6-20}
$$

令

$$
F (x, y, z) = f (x, y) - z,
$$

97

---

第九章 多元函数微分法及其应用

可见

$$
F _ {x} (x, y, z) = f _ {x} (x, y), \quad F _ {y} (x, y, z) = f _ {y} (x, y), \quad F _ {z} (x, y, z) = - 1.
$$

于是，当函数 $f(x,y)$ 的偏导数 $f_{x}(x,y),f_{y}(x,y)$ 在点 $(x_0,y_0)$ 连续时，曲面(6-20)在点$M(x_0,y_0,z_0)$ 处的法向量为

$$
\boldsymbol {n} = (f _ {x} (x _ {0}, y _ {0}), f _ {y} (x _ {0}, y _ {0}), - 1),
$$

切平面方程为

$$
f _ {x} (x _ {0}, y _ {0}) (x - x _ {0}) + f _ {y} (x _ {0}, y _ {0}) (y - y _ {0}) - (z - z _ {0}) = 0,
$$

或

$$
z - z _ {0} = f _ {x} (x _ {0}, y _ {0}) (x - x _ {0}) + f _ {y} (x _ {0}, y _ {0}) (y - y _ {0}), \tag {6-21}
$$

而法线方程为

$$
\frac {x - x _ {0}}{f _ {x} (x _ {0} , y _ {0})} = \frac {y - y _ {0}}{f _ {y} (x _ {0} , y _ {0})} = \frac {z - z _ {0}}{- 1}. \tag {6-22}
$$

这里顺便指出,方程(6-21)右端恰好是函数 $z=f(x,y)$ 在点 $(x_{0},y_{0})$ 的全微分,而左端是切平面上点的竖坐标的增量.因此,函数 $z=f(x,y)$ 在点 $(x_{0},y_{0})$ 的全微分,在几何上表示曲面 $z=f(x,y)$ 在点 $(x_{0},y_{0},z_{0})$ 处的切平面上点的竖坐标的增量.

如果用  $\alpha,\beta$  和  $\gamma$  表示曲面的法向量的方向角,并假定法向量的方向是向上的,即使得它与 z 轴的正向所夹的角  $\gamma$  是一锐角,那么法向量的方向余弦为

$$
\cos \alpha = \frac {- f _ {x}}{\sqrt {1 + f _ {x} ^ {2} + f _ {y} ^ {2}}}, \quad \cos \beta = \frac {- f _ {y}}{\sqrt {1 + f _ {x} ^ {2} + f _ {y} ^ {2}}}, \quad \cos \gamma = \frac {1}{\sqrt {1 + f _ {x} ^ {2} + f _ {y} ^ {2}}}.
$$

这里，把 $f_{x}(x_{0},y_{0})$ 和 $f_{y}(x_{0},y_{0})$ 分别简记为 $f_{x}$ 和 $f_{y}$.

例 6 求球面  $x^{2}+y^{2}+z^{2}=14$  在点  $(1,2,3)$  处的切平面及法线方程.

解 $F(x,y,z) = x^{2} + y^{2} + z^{2} - 14,$

$$
\boldsymbol {n} = (F _ {x}, F _ {y}, F _ {z}) = (2 x, 2 y, 2 z), \quad \boldsymbol {n} | _ {(1, 2, 3)} = (2, 4, 6).
$$

所以在点(1,2,3)处此球面的切平面方程为

$$
2 (x - 1) + 4 (y - 2) + 6 (z - 3) = 0,
$$

即

$$
x + 2 y + 3 z - 1 4 = 0.
$$

法线方程为

$$
\frac {x - 1}{1} = \frac {y - 2}{2} = \frac {z - 3}{3},
$$

即

$$
\frac {x}{1} = \frac {y}{2} = \frac {z}{3}.
$$

由此可见,法线经过原点(即球心).

98

---

第六节 多元函数微分学的几何应用

例 7 求旋转抛物面  $z=x^{2}+y^{2}-1$  在点  $(2,1,4)$  处的切平面及法线方程.

解 $f(x,y) = x^{2} + y^{2} - 1,$

$$
\boldsymbol {n} = (f _ {x}, f _ {y}, - 1) = (2 x, 2 y, - 1), \quad \boldsymbol {n} \mid_ {(2, 1, 4)} = (4, 2, - 1).
$$

所以在点 $(2,1,4)$ 处的切平面方程为

$$
4 (x - 2) + 2 (y - 1) - (z - 4) = 0,
$$

即

$$
4 x + 2 y - z - 6 = 0.
$$

法线方程为

$$
\frac {x - 2}{4} = \frac {y - 1}{2} = \frac {z - 4}{- 1}.
$$

## 习题9-6

1. 设 $f(t) = f_{1}(t)i + f_{2}(t)j + f_{3}(t)k$, $g(t) = g_{1}(t)i + g_{2}(t)j + g_{3}(t)k$, $\lim_{t\to t_0}f(t) = u$, $\lim_{t\to t_0}g(t) = v$, 证明

$$
\lim _ {t \to t _ {0}} [ f (t) \times g (t) ] = u \times v.
$$

2. 下列各题中, $r=f(t)$ 是空间中的质点 M 在时刻 t 的位置, 求质点 M 在时刻 $t_{0}$ 的速度向量和加速度向量以及在任意时刻 t 的速率:

(1)  $r = f(t) = (t + 1)i + (t^{2} - 1)j + 2tk, t_{0} = 1;$
(2) $r=f(t)=(2\cos t)i+(3\sin t)j+4tk,t_{0}=\frac{\pi}{2};$
(3) $r=f(t)=(2\ln(t+1))i+t^{2}j+\frac{1}{2}t^{2}k,t_{0}=1.$

3. 求曲线 $r = f(t) = (t - \sin t)i + (1 - \cos t)j + \left(4\sin \frac{t}{2}\right)k$ 在与 $t_0 = \frac{\pi}{2}$ 相应的点处的切线及法平面方程.

4. 求曲线  $x=\frac{t}{1+t}, y=\frac{1+t}{t}, z=t^{2}$  在对应于  $t_{0}=1$  的点处的切线及法平面方程.

5. 求曲线  $y^{2}=2mx, z^{2}=m-x$  在点  $(x_{0}, y_{0}, z_{0})$  处的切线及法平面方程.

6. 求曲线  $\left\{\begin{aligned} x^{2}+y^{2}+z^{2}-3x=0,\\ 2x-3y+5z-4=0\end{aligned}\right.$  在点(1,1,1)处的切线及法平面方程.

7. 求出曲线 $x = t, y = t^2, z = t^3$ 上的点，使在该点的切线平行于平面 $x + 2y + z = 4$.

8. 求曲面  $e^{z}-z+xy=3$  在点  $(2,1,0)$  处的切平面及法线方程.

9. 求曲面  $ax^{2}+by^{2}+cz^{2}=1$  在点  $(x_{0},y_{0},z_{0})$  处的切平面及法线方程.

10. 求椭球面  $x^{2}+2y^{2}+z^{2}=1$  上平行于平面  $x-y+2z=0$  的切平面方程.

11. 设曲面 $3x^{2} + y^{2} - z^{2} = 27$ 的切平面通过直线 $L: \begin{cases} 10x + 2y - 2z = 27, \\ x + y - z = 0. \end{cases}$ 求此切平面的方程.

99

---

第九章 多元函数微分法及其应用

12. 设 $L$ 是曲面 $\Sigma: z = y^2 + x^3y$ 上一条曲线的切线，切点为 $P(2,1,9), L$ 在 $xOy$ 面上的投影平行于 $x$ 轴，求切线 $L$ 的参数方程.

13. 求旋转椭球面 $3x^{2} + y^{2} + z^{2} = 16$ 上点 $(-1, -2, 3)$ 处的切平面与 $xOy$ 面的夹角的余弦.

14. 试证曲面 $\sqrt{x} +\sqrt{y} +\sqrt{z} = \sqrt{a}$ （ $a > 0$ )上任何点处的切平面在各坐标轴上的截距之和等于 $a$

15. 设  $\boldsymbol{u}(t)$ ,  $\boldsymbol{v}(t)$  是可导的向量值函数, 证明:

(1) $\frac{\mathrm{d}}{\mathrm{d}t}[\boldsymbol{u}(t)\pm \boldsymbol {v}(t)] = \boldsymbol{u}'(t)\pm \boldsymbol{v}'(t);$
(2) $\frac{\mathrm{d}}{\mathrm{d}t}[\boldsymbol{u}(t)\cdot \boldsymbol {v}(t)] = \boldsymbol{u}'(t)\cdot \boldsymbol {v}(t) + \boldsymbol {u}(t)\cdot \boldsymbol{v}'(t);$
(3) $\frac{\mathrm{d}}{\mathrm{d}t}[\boldsymbol{u}(t)\times\boldsymbol{v}(t)]=\boldsymbol{u}'(t)\times\boldsymbol{v}(t)+\boldsymbol{u}(t)\times\boldsymbol{v}'(t).\quad$

## 第七节 方向导数与梯度

## 一、方向导数

偏导数反映的是函数沿坐标轴方向的变化率.但许多物理现象告诉我们,只考虑

函数沿坐标轴方向的变化率是不够的.因此我们有必要来讨论函数沿任一指定方向的变化率问题.

设 $l$ 是 $xOy$ 平面上以 $P_0(x_0, y_0)$ 为始点的一条射线，$e_l = (\cos \alpha, \cos \beta)$ 是与 $l$ 同方向的单位向量（图9-9). 射线 $l$ 的参数方程为

$$
\left\{ \begin{array}{l l} x = x _ {0} + t \cos \alpha , \\ y = y _ {0} + t \cos \beta \end{array} \right. (t \geqslant 0).
$$

![](../../raw/pages_0097-0128/images/page_106_image_15.jpg)

<details>
<summary>text_image</summary>

y
P(x, y)
l
e₁
P₀(x₀, y₀)
O
x
</details>

图9-9

设函数 $z = f(x,y)$ 在点 $P_0(x_0,y_0)$ 的某个邻域

$U(P_{0})$ 内有定义, $P(x_{0}+t\cos\alpha,y_{0}+t\cos\beta)$ 为 l 上另一点,且 $P\in U(P_{0})$. 如果函数增量 $f(x_{0}+t\cos\alpha,y_{0}+t\cos\beta)-f(x_{0},y_{0})$ 与 P 到 $P_{0}$ 的距离 $|PP_{0}|=t$ 的比值

$$
\frac {f (x _ {0} + t \cos \alpha , y _ {0} + t \cos \beta) - f (x _ {0} , y _ {0})}{t}
$$

当 $P$ 沿着 $l$ 趋于 $P_{0}$ （即 $t\to 0^{+}$）时的极限存在，那么称此极限为函数 $f(x,y)$ 在点 $P_{0}$ 沿方向 $l$ 的方向导数，记作 $\frac{\partial f}{\partial l}\Bigg|_{(x_0,y_0)}$ ，即

$$
\left. \frac {\partial f}{\partial l} \right| _ {(x _ {0}, y _ {0})} = \lim _ {t \to 0 ^ {+}} \frac {f (x _ {0} + t \cos \alpha , y _ {0} + t \cos \beta) - f (x _ {0} , y _ {0})}{t}. \tag {7-1}
$$

100

---

第七节 方向导数与梯度

从方向导数的定义可知, 方向导数  $\frac{\partial f}{\partial l}\bigg|_{(x_{0},y_{0})}$  就是函数  $f(x,y)$  在点  $P_{0}(x_{0},y_{0})$  处沿方向 l 的变化率. 若函数  $f(x,y)$  在点  $P_{0}(x_{0},y_{0})$  的偏导数存在,  $e_{l}=i=(1,0)$ , 则

$$
\frac {\partial f}{\partial l} \Bigg | _ {(x _ {0}, y _ {0})} = \lim _ {t \to 0 ^ {+}} \frac {f (x _ {0} + t , y _ {0}) - f (x _ {0} , y _ {0})}{t} = f _ {x} (x _ {0}, y _ {0});
$$

又若 $e_l = j = (0,1)$ ，则

$$
\frac {\partial f}{\partial l} \Bigg | _ {(x _ {0}, y _ {0})} = \lim _ {t \to 0 ^ {+}} \frac {f (x _ {0} , y _ {0} + t) - f (x _ {0} , y _ {0})}{t} = f _ {y} (x _ {0}, y _ {0}).
$$

但反之，若 $e_l = i, \frac{\partial z}{\partial l}\bigg|_{(x_0,y_0)}$ 存在，则 $\frac{\partial z}{\partial x}\bigg|_{(x_0,y_0)}$ 未必存在.例如，$z = \sqrt{x^2 + y^2}$ 在点 $O(0,0)$ 处沿$l = i$ 方向的方向导数 $\frac{\partial z}{\partial l}\bigg|_{(0,0)} = 1$ ，而偏导数 $\frac{\partial z}{\partial x}\bigg|_{(0,0)}$ 不存在.

关于方向导数的存在及计算,我们有以下定理:

定理 如果函数 $f(x,y)$ 在点 $P_0(x_0,y_0)$ 可微分, 那么函数在该点沿任一方向 $l$ 的方向导数存在, 且有

$$
\left. \frac {\partial f}{\partial l} \right| _ {(x _ {0}, y _ {0})} = f _ {x} (x _ {0}, y _ {0}) \cos \alpha + f _ {y} (x _ {0}, y _ {0}) \cos \beta , \tag {7-2}
$$

其中  $\cos\alpha$  和  $\cos\beta$  是方向 l 的方向余弦.

证 由假设, $f(x,y)$ 在点 $(x_{0},y_{0})$ 可微分,故有

$$
f (x _ {0} + \Delta x, y _ {0} + \Delta y) - f (x _ {0}, y _ {0}) = f _ {x} (x _ {0}, y _ {0}) \Delta x + f _ {y} (x _ {0}, y _ {0}) \Delta y + o (\sqrt {(\Delta x) ^ {2} + (\Delta y) ^ {2}}).
$$

但点 $(x_{0}+\Delta x,y_{0}+\Delta y)$ 在以 $(x_{0},y_{0})$ 为始点的射线l上时，应有 $\Delta x=t\cos\alpha,\Delta y=t\cos\beta,$   $\sqrt{(\Delta x)^{2}+(\Delta y)^{2}}=t.$ 所以

$$
\lim _ {t \to 0 ^ {+}} \frac {f (x _ {0} + t \cos \alpha , y _ {0} + t \cos \beta) - f (x _ {0} , y _ {0})}{t} = f _ {x} (x _ {0}, y _ {0}) \cos \alpha + f _ {y} (x _ {0}, y _ {0}) \cos \beta.
$$

这就证明了方向导数存在,且其值为

$$
\left. \frac {\partial f}{\partial l} \right| _ {(x _ {0}, y _ {0})} = f _ {x} (x _ {0}, y _ {0}) \cos \alpha + f _ {y} (x _ {0}, y _ {0}) \cos \beta .
$$

例1 求函数 $z = x\mathrm{e}^{2y}$ 在点 $P(1,0)$ 处沿从点 $P(1,0)$ 到点 $Q(2,-1)$ 的方向的方向导数.

解 这里方向 $l$ 即向量 $\overrightarrow{PQ} = (1, -1)$ 的方向，与 $l$ 同向的单位向量为 $e_l = \left(\frac{1}{\sqrt{2}}, -\frac{1}{\sqrt{2}}\right)$.

因为函数可微分,且

$$
\frac {\partial z}{\partial x} \bigg | _ {(1, 0)} = \mathrm{e} ^ {2 y} \bigg | _ {(1, 0)} = 1, \quad \frac {\partial z}{\partial y} \bigg | _ {(1, 0)} = 2 x \mathrm{e} ^ {2 y} \bigg | _ {(1, 0)} = 2,
$$

101

---

第九章 多元函数微分法及其应用

故所求方向导数为

$$
\left. \frac {\partial z}{\partial l} \right| _ {(1, 0)} = 1 \times \frac {1}{\sqrt {2}} + 2 \times \left(- \frac {1}{\sqrt {2}}\right) = - \frac {\sqrt {2}}{2}.
$$

对于三元函数 $f(x,y,z)$ 来说，它在空间一点 $P_0(x_0,y_0,z_0)$ 沿方向 $\pmb{e}_l = (\cos \alpha, \cos \beta, \cos \gamma)$ 的方向导数为

$$
\left. \frac {\partial f}{\partial l} \right| _ {(z _ {0}, y _ {0}, z _ {0})} = \lim _ {t \rightarrow 0 ^ {+}} \frac {f \left(x _ {0} + t \cos \alpha , y _ {0} + t \cos \beta , z _ {0} + t \cos \gamma\right) - f \left(x _ {0} , y _ {0} , z _ {0}\right)}{t}. \tag {7-3}
$$

同样可以证明:如果函数 $f(x,y,z)$ 在点 $(x_{0},y_{0},z_{0})$ 可微分,那么函数在该点沿方向 $\boldsymbol{e}_{l}=(\cos\alpha,\cos\beta,\cos\gamma)$ 的方向导数为

$$
\left. \frac {\partial f}{\partial l} \right| _ {(x _ {0}, y _ {0}, z _ {0})} = f _ {x} (x _ {0}, y _ {0}, z _ {0}) \cos \alpha + f _ {y} (x _ {0}, y _ {0}, z _ {0}) \cos \beta + f _ {z} (x _ {0}, y _ {0}, z _ {0}) \cos \gamma . \tag {7-4}
$$

例 2 求  $f(x,y,z)=xy+yz+zx$  在点  $(1,1,2)$  沿方向 l 的方向导数, 其中 l 的方向角分别为  $60^{\circ}, 45^{\circ}, 60^{\circ}$ .

解 与 $l$ 同向的单位向量

$$
e _ {l} = (\cos 6 0 ^ {\circ}, \cos 4 5 ^ {\circ}, \cos 6 0 ^ {\circ}) = \left(\frac {1}{2}, \frac {\sqrt {2}}{2}, \frac {1}{2}\right).
$$

因为函数可微分,且

$$
f _ {x} (1, 1, 2) = (y + z) \mid_ {(1, 1, 2)} = 3,
$$

$$
f _ {y} (1, 1, 2) = (x + z) \mid_ {(1, 1, 2)} = 3,
$$

$$
f _ {z} (1, 1, 2) = (y + x) \mid_ {(1, 1, 2)} = 2.
$$

由公式(7-4)，得

$$
\left. \frac {\partial f}{\partial l} \right| _ {(1, 1, 2)} = 3 \times \frac {1}{2} + 3 \times \frac {\sqrt {2}}{2} + 2 \times \frac {1}{2} = \frac {1}{2} (5 + 3 \sqrt {2}).
$$

## 二、梯度

与方向导数有关联的一个概念是函数的梯度. 在二元函数的情形, 设函数 $f(x, y)$ 在平面区域 $D$ 内具有一阶连续偏导数, 则对于每一点 $P_0(x_0, y_0) \in D$, 都可定出一个向量

$$
f _ {x} (x _ {0}, y _ {0}) i + f _ {y} (x _ {0}, y _ {0}) j,
$$

这向量称为函数 $f(x,y)$ 在点 $P_0(x_0,y_0)$ 的梯度，记作 $\operatorname{grad} f(x_0,y_0)$ 或 $\nabla f(x_0,y_0)$，即

$$
\mathrm{grad} f (x _ {0}, y _ {0}) = \nabla f (x _ {0}, y _ {0}) = f _ {x} (x _ {0}, y _ {0}) i + f _ {y} (x _ {0}, y _ {0}) j,
$$

其中 $\nabla=\frac{\partial}{\partial x}i+\frac{\partial}{\partial y}j$ 称为（二维的）向量微分算子或Nabla算子， $\nabla f=\frac{\partial f}{\partial x}i+\frac{\partial f}{\partial y}j.$

102

---

第七节 方向导数与梯度

如果函数 $f(x,y)$ 在点 $P_0(x_0,y_0)$ 可微分，$e_l = (\cos \alpha, \cos \beta)$ 是与方向 $l$ 同向的单位向量，那么

$$
\begin{array}{l} \left. \frac {\partial f}{\partial l} \right| _ {(x _ {0}, y _ {0})} = f _ {x} (x _ {0}, y _ {0}) \cos \alpha + f _ {y} (x _ {0}, y _ {0}) \cos \beta \\ = \operatorname{grad} f (x _ {0}, y _ {0}) \cdot e _ {l} = | \operatorname{grad} f (x _ {0}, y _ {0}) | \cos \theta , \\ \end{array}
$$

其中  $\theta=(\mathbf{grad}f(x_{0},y_{0}),e_{l})$ .

这一关系式表明了函数在一点的梯度与函数在这点的方向导数间的关系.特别，由这关系可知:

（1）当 $\theta = 0$ ，即方向 $e_l$ 与梯度grad $f(x_0,y_0)$ 的方向相同时，函数 $f(x,y)$ 增加最快.此时，函数在这个方向的方向导数达到最大值，这个最大值就是梯度grad $f(x_0,y_0)$ 的模，即

$$
\left. \frac {\partial f}{\partial l} \right| _ {(x _ {0}, y _ {0})} = | \operatorname{grad} f (x _ {0}, y _ {0}) |\cdot
$$

这个结果也表示: 函数  $f(x,y)$  在一点的梯度 grad f 是这样一个向量, 它的方向是函数在这点的方向导数取得最大值的方向, 它的模就等于方向导数的最大值.

（2）当 $\theta = \pi$ ，即方向 $e_l$ 与梯度grad $f(x_0,y_0)$ 的方向相反时，函数 $f(x,y)$ 减少最快，函数在这个方向的方向导数达到最小值，即

$$
\left. \frac {\partial f}{\partial l} \right| _ {(x _ {0}, y _ {0})} = - | \mathbf {g r a d} f (x _ {0}, y _ {0}) |\.
$$

(3) 当  $\theta=\frac{\pi}{2}$ ，即方向  $e_{l}$  与梯度 grad  $f(x_{0},y_{0})$  的方向正交时，函数的变化率为零，即

$$
\frac {\partial f}{\partial l} \bigg | _ {(x _ {0}, y _ {0})} = | \mathbf {g r a d} f (x _ {0}, y _ {0}) | \cos \theta = 0.
$$

我们知道,一般说来二元函数  $z=f(x,y)$  在几何上表示一个曲面,这曲面被平面 z=c (c 是常数) 所截得的曲线 L 的方程为

$$
\left\{ \begin{array}{l} z = f (x, y), \\ z = c. \end{array} \right.
$$

这条曲线 L 在 xOy 面上的投影是一条平面曲线  $L^{*}$ （图 9-10），它在 xOy 平面直角坐标系中的方程为

$$
f (x, y) = c.
$$

对于曲线  $L^{*}$  上的一切点, 已给函数的函数值都是 c, 所以我们称平面曲线  $L^{*}$  为函数  $z = f(x, y)$  的等值线.

若 $f_{x}, f_{y}$ 不同时为零, 则等值线 $f(x, y) = c$ 上任一点 $P_{0}(x_{0}, y_{0})$ 处的一个单位法向

103

---

第九章 多元函数微分法及其应用

量为

$$
n = \frac {1}{\sqrt {f _ {x} ^ {2} (x _ {0} , y _ {0}) + f _ {y} ^ {2} (x _ {0} , y _ {0})}} (f _ {x} (x _ {0}, y _ {0}), f _ {y} (x _ {0}, y _ {0})) = \frac {\nabla f (x _ {0} , y _ {0})}{| \nabla f (x _ {0} , y _ {0}) |}.
$$

这表明函数 $f(x,y)$ 在一点 $(x_0,y_0)$ 的梯度 $\nabla f(x_0,y_0)$ 的方向就是等值线 $f(x,y) = c$ 在这点的法线方向 $\pmb{n}$，而梯度的模 $|\nabla f(x_0,y_0)|$ 就是沿这个法线方向的方向导数 $\frac{\partial f}{\partial n}$，于是有

$$
\nabla f (x _ {0}, y _ {0}) = \frac {\partial f}{\partial n} \boldsymbol {n}.
$$

![](../../raw/pages_0097-0128/images/page_110_image_5.jpg)

<details>
<summary>text_image</summary>

L*f(x, y)=c
L1:f(x, y)=c1
P0(x0, y0)
∇f(x0, y0)
L2:f(x, y)=c2 (c2>c1)
</details>

图9-10

上面讨论的梯度概念可以类似地推广到三元函数的情形. 设函数 $f(x, y, z)$ 在空间区域 $G$ 内具有一阶连续偏导数, 则对于每一点 $P_0(x_0, y_0, z_0) \in G$, 都可定出一个向量

$$
f _ {x} (x _ {0}, y _ {0}, z _ {0}) i + f _ {y} (x _ {0}, y _ {0}, z _ {0}) j + f _ {z} (x _ {0}, y _ {0}, z _ {0}) k,
$$

这向量称为函数 $f(x,y,z)$ 在点 $P_0(x_0,y_0,z_0)$ 的梯度，将它记作 $\operatorname{grad} f(x_0,y_0,z_0)$ 或 $\nabla f(x_0,y_0,z_0)$，即

$$
\text {grad} f (x _ {0}, y _ {0}, z _ {0}) = \nabla f (x _ {0}, y _ {0}, z _ {0}) = f _ {x} (x _ {0}, y _ {0}, z _ {0}) i + f _ {y} (x _ {0}, y _ {0}, z _ {0}) j + f _ {z} (x _ {0}, y _ {0}, z _ {0}) k,
$$

其中 $\nabla = \frac{\partial}{\partial x}\boldsymbol{i} + \frac{\partial}{\partial y}\boldsymbol{j} + \frac{\partial}{\partial z}\boldsymbol{k}$ 称为（三维的）向量微分算子或Nabla算子， $\nabla f = \frac{\partial f}{\partial x}\boldsymbol{i} + \frac{\partial f}{\partial y}\boldsymbol{j} + \frac{\partial f}{\partial z}\boldsymbol{k}$

经过与二元函数的情形完全类似的讨论可知,三元函数 $f(x,y,z)$ 在一点的梯度 $\nabla f$ 是这样一个向量,它的方向是函数 $f(x,y,z)$ 在这点的方向导数取得最大值的方向,它的模就等于方向导数的最大值.

如果引进曲面

$$
f (x, y, z) = c
$$

为函数 $f(x,y,z)$ 的等值面的概念，那么可得函数 $f(x,y,z)$ 在一点 $(x_0,y_0,z_0)$ 的梯度 $\nabla f(x_0,y_0,z_0)$ 的方向就是等值面 $f(x,y,z) = c$ 在这点的法向量 $\pmb{n}$，而梯度的模

104

---

第七节 方向导数与梯度

$\mid \nabla f(x_0,y_0,z_0)\mid$ 就是函数沿这个法向量的方向导数 $\frac{\partial f}{\partial n}$

例3 求 $\operatorname{grad} \frac{1}{x^2 + y^2}$.

解 这里 $f(x,y) = \frac{1}{x^2 + y^2}$. 因为

$$
\frac {\partial f}{\partial x} = - \frac {2 x}{(x ^ {2} + y ^ {2}) ^ {2}}, \quad \frac {\partial f}{\partial y} = - \frac {2 y}{(x ^ {2} + y ^ {2}) ^ {2}},
$$

所以

$$
\mathrm{grad} \frac {1}{x ^ {2} + y ^ {2}} = - \frac {2 x}{(x ^ {2} + y ^ {2}) ^ {2}} i - \frac {2 y}{(x ^ {2} + y ^ {2}) ^ {2}} j.
$$

例4 设 $f(x,y) = \frac{1}{2} (x^{2} + y^{2})$ ，点 $P_0(1,1)$ ，求:

(1) $f(x,y)$ 在点 $P_{0}$ 处增加最快的方向以及 $f(x,y)$ 沿这个方向的方向导数；
(2) $f(x,y)$ 在点 $P_{0}$ 处减少最快的方向以及 $f(x,y)$ 沿这个方向的方向导数；
(3) $f(x,y)$ 在点 $P_{0}$ 处的变化率为零的方向.

解（1） $f(x,y)$ 在点 $P_0$ 处沿 $\nabla f(1,1)$ 的方向增加最快，

$$
\nabla f (1, 1) = (x \boldsymbol {i} + y \boldsymbol {j}) \mid_ {(1, 1)} = \boldsymbol {i} + \boldsymbol {j},
$$

故所求方向可取为

$$
n = \frac {\nabla f (1 , 1)}{| \nabla f (1 , 1) |} = \frac {1}{\sqrt {2}} i + \frac {1}{\sqrt {2}} j,
$$

方向导数为

$$
\frac {\partial f}{\partial n} \big | _ {(1, 1)} = | \nabla f (1, 1) | = \sqrt {2}.
$$

(2) $f(x,y)$ 在点 $P_{0}$ 处沿 $-\nabla f(1,1)$ 的方向减少最快,这方向可取为

$$
n _ {1} = - n = - \frac {1}{\sqrt {2}} i - \frac {1}{\sqrt {2}} j,
$$

方向导数为

$$
\frac {\partial f}{\partial n _ {1}} \big | _ {(1, 1)} = - \mid \nabla f (1, 1) \mid = - \sqrt {2}.
$$

(3) $f(x,y)$ 在点 $P_0$ 处沿垂直于 $\nabla f(1,1)$ 的方向变化率为零，这方向是

$$
n _ {2} = - \frac {1}{\sqrt {2}}   i + \frac {1}{\sqrt {2}}   j \quad \text {或} \quad n _ {3} = \frac {1}{\sqrt {2}}   i - \frac {1}{\sqrt {2}}   j.
$$

例 5 设  $f(x,y,z)=x^{3}-xy^{2}-z$ ，点  $P_{0}(1,1,0)$ 。问  $f(x,y,z)$  在点  $P_{0}$  处沿什么方向变化最快，在这个方向的变化率是多少？

105

---

第九章 多元函数微分法及其应用

解 $\nabla f = f_{x}i + f_{y}j + f_{z}k = (3x^{2} - y^{2})i - 2xyj - k,\nabla f(1,1,0) = 2i - 2j - k.$

$f(x,y,z)$  在点  $P_{0}$  处沿  $\nabla f(1,1,0)$  的方向增加最快，沿  $-\nabla f(1,1,0)$  的方向减少最快，在这两个方向的变化率分别是

$$
\begin{array}{l} \mid \nabla f (1, 1, 0) \mid = \sqrt {2 ^ {2} + (- 2) ^ {2} + 1} = 3, \\ - | \nabla f (1, 1, 0) | = - 3. \\ \end{array}
$$

例 6 求曲面  $x^{2}+y^{2}+z=9$  在点  $P_{0}(1,2,4)$  的切平面和法线方程.

解 设 $f(x,y,z) = x^{2} + y^{2} + z.$ 由梯度与等值面的关系可知，梯度

$$
\nabla f \Big | _ {P _ {0}} = (2 x i + 2 y j + k) \Big | _ {(1, 2, 4)} = 2 i + 4 j + k
$$

的方向是等值面 $f(x,y,z)=9$ 在点 $P_{0}$ 的法线方向,因此切平面方程是

$$
2 (x - 1) + 4 (y - 2) + (z - 4) = 0,
$$

即

$$
2 x + 4 y + z = 1 4,
$$

曲面在点  $P_{0}$  处的法线方程是

$$
x = 1 + 2 t, \quad y = 2 + 4 t, z = 4 + t \quad (t \text {为任意常数}).
$$

下面我们简单地介绍数量场与向量场的概念.

如果对于空间区域 $G$ 内的任一点 $M$, 都有一个确定的数量 $f(M)$, 那么称在这空间区域 $G$ 内确定了一个数量场 (例如温度场、密度场等). 一个数量场可用一个数量函数 $f(M)$ 来确定. 如果与点 $M$ 相对应的是一个向量 $F(M)$, 那么称在这空间区域 $G$ 内确定了一个向量场 (例如力场、速度场等). 一个向量场可用一个向量值函数 $F(M)$ 来确定, 而

$$
\boldsymbol {F} (M) = P (M) \boldsymbol {i} + Q (M) \boldsymbol {j} + R (M) \boldsymbol {k},
$$

其中  $P(M)$ ,  $Q(M)$ ,  $R(M)$  是点 M 的数量函数.

若向量场 $F(M)$ 是某个数量函数 $f(M)$ 的梯度, 则称 $f(M)$ 是向量场 $F(M)$ 的一个势函数, 并称向量场 $F(M)$ 为势场. 由此可知, 由数量函数 $f(M)$ 产生的梯度场 $\operatorname{grad} f(M)$ 是一个势场. 但需注意, 任意一个向量场并不一定都是势场, 因为它不一定是某个数量函数的梯度.

例 7 试求数量场 $\frac{m}{r}$ 所产生的梯度场, 其中常数 $m > 0, r = \sqrt{x^2 + y^2 + z^2}$ 为原点 O 与点 $M(x, y, z)$ 间的距离.

解

$$
\frac {\partial}{\partial x} \left(\frac {m}{r}\right) = - \frac {m}{r ^ {2}} \frac {\partial r}{\partial x} = - \frac {m x}{r ^ {3}},
$$

同理

$$
\frac {\partial}{\partial y} \left(\frac {m}{r}\right) = - \frac {m y}{r ^ {3}}, \quad \frac {\partial}{\partial z} \left(\frac {m}{r}\right) = - \frac {m z}{r ^ {3}}.
$$

例题精讲
9-3

106

---

第七节 方向导数与梯度

从而

$$
\mathrm{grad} \frac {m}{r} = - \frac {m}{r ^ {2}} \left(\frac {x}{r} i + \frac {y}{r} j + \frac {z}{r} k\right).
$$

如果用 $e_r$ 表示与 $\overrightarrow{OM}$ 同方向的单位向量, 那么

$$
e _ {r} = \frac {x}{r} i + \frac {y}{r} j + \frac {z}{r} k,
$$

因此

$$
\mathrm{grad} \frac {m}{r} = - \frac {m}{r ^ {2}} e _ {r}.
$$

上式右端在力学上可解释为,位于原点 O 而质量为 m 的质点对位于点 M 而质量为 1 的质点的引力.这引力的大小与两质点的质量的乘积成正比、而与它们的距离平方成反比,这引力的方向由点 M 指向原点.因此数量场  $\frac{m}{r}$  的势场,即梯度场  $\frac{grad}{r}$ ,称为引力场,而函数  $\frac{m}{r}$  称为引力势.

## 习题9-7

1. 求函数 $z = x^{2} + y^{2}$ 在点(1,2)处沿从点(1,2)到点 $(2,2 + \sqrt{3})$ 的方向的方向导数.
2. 求函数 $z = \ln (x + y)$ 在抛物线 $y^{2} = 4x$ 上点(1,2)处，沿着这抛物线在该点处偏向 $x$ 轴正向的切线方向的方向导数.
3. 求函数 $z = 1 - \left(\frac{x^2}{a^2} + \frac{y^2}{b^2}\right)$ 在点 $\left(\frac{a}{\sqrt{2}}, \frac{b}{\sqrt{2}}\right)$ 处沿曲线 $\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1$ 在该点的内法线方向的方向导数.

4. 求函数 $u = xy^2 + z^3 - xyz$ 在点(1,1,2)处沿方向角为 $\alpha = \frac{\pi}{3}, \beta = \frac{\pi}{4}, \gamma = \frac{\pi}{3}$ 的方向的方向导数.

5. 求函数 u = xyz 在点  $(5,1,2)$  处沿从点  $(5,1,2)$  到点  $(9,4,14)$  的方向的方向导数.

6. 求函数 $u = x^{2} + y^{2} + z^{2}$ 在曲线 $x = t, y = t^2, z = t^3$ 上点(1,1,1)处，沿曲线在该点的切线正方向（对应于 $t$ 增大的方向）的方向导数.

7. 求函数 $u = x + y + z$ 在球面 $x^{2} + y^{2} + z^{2} = 1$ 上点 $(x_{0}, y_{0}, z_{0})$ 处，沿球面在该点的外法线方向的方向导数.

8. 设 $f(x, y, z) = x^{2} + 2y^{2} + 3z^{2} + xy + 3x - 2y - 6z$，求

$$
\operatorname{grad} f (0, 0, 0) \quad \text {及} \quad \operatorname{grad} f (1, 1, 1).
$$

9. 设函数 $u(x,y,z), v(x,y,z)$ 的各个偏导数都存在且连续, 证明:

(1)  $\nabla(cu)=c\nabla u$  (其中 c 为常数); (2)  $\nabla(u\pm v)=\nabla u\pm\nabla v;$

107

---

第九章 多元函数微分法及其应用

(3) $\nabla(uv) = v\nabla u + u\nabla v;$

(4) $\nabla \left(\frac{u}{v}\right) = \frac{v\nabla u - u\nabla v}{v^2}\quad (v\neq 0)$.

10. 求函数 $u = xy^2 z$ 在点 $P_0(1, -1, 2)$ 处变化最快的方向，并求沿这个方向的方向导数

## 第八节 多元函数的极值及其求法

## 一、多元函数的极值及最大值与最小值

在实际问题中,往往会遇到多元函数的最大值与最小值问题.与一元函数相类似,多元函数的最大值、最小值与极大值、极小值有密切联系,因此我们以二元函数为例,先来讨论多元函数的极值问题.

定义 设函数 $z = f(x, y)$ 的定义域为 $D, P_0(x_0, y_0)$ 为 $D$ 的内点. 若存在 $P_0$ 的某个邻域 $U(P_0) \subset D$, 使得对于该邻域内异于 $P_0$ 的任何点 $(x, y)$, 都有

$$
f (x, y) <   f (x _ {0}, y _ {0}),
$$

则称函数 $f(x,y)$ 在点 $(x_0,y_0)$ 有极大值 $f(x_0,y_0)$，点 $(x_0,y_0)$ 称为函数 $f(x,y)$ 的极大值点；若对于该邻域内异于 $P_0$ 的任何点 $(x,y)$，都有

$$
f (x, y) > f (x _ {0}, y _ {0}),
$$

则称函数 $f(x,y)$ 在点 $(x_{0},y_{0})$ 有极小值 $f(x_{0},y_{0})$ ，点 $(x_{0},y_{0})$ 称为函数 $f(x,y)$ 的极小值点.极大值与极小值统称为极值.使得函数取得极值的点称为极值点.

例1 函数 $z = 3x^{2} + 4y^{2}$ 在点 $(0,0)$ 处有极小值. 因为对于点 $(0,0)$ 的任一邻域内异于 $(0,0)$ 的点，函数值都为正，而在点 $(0,0)$ 处的函数值为零. 从几何上看这是显然的，因为点 $(0,0,0)$ 是开口朝上的椭圆抛物面 $z = 3x^{2} + 4y^{2}$ 的顶点.

例2 函数 $z = -\sqrt{x^2 + y^2}$ 在点 $(0,0)$ 处有极大值.因为在点 $(0,0)$ 处函数值为零，而对于点 $(0,0)$ 的任一邻域内异于 $(0,0)$ 的点，函数值都为负.点 $(0,0,0)$ 是位于 $xOy$ 平面下方的锥面 $z = -\sqrt{x^2 + y^2}$ 的顶点.

例3 函数 $z = xy$ 在点 $(0,0)$ 处既不取得极大值也不取得极小值.因为在点 $(0,0)$ 处的函数值为零，而在点 $(0,0)$ 的任一邻域内，总有使函数值为正的点，也有使函数值为负的点.

以上关于二元函数的极值概念,可推广到 n 元函数.设 n 元函数  $u=f(P)$  的定义域为 D,  $P_{0}$  为 D 的内点.若存在  $P_{0}$  的某个邻域  $U(P_{0})\subset D$ ,使得该邻域内异于  $P_{0}$  的任何点 P,都有

$$
f (P) <   f (P _ {0}) (\text {或} f (P) > f (P _ {0})) ,
$$

108

---

第八节 多元函数的极值及其求法

则称函数 $f(P)$ 在点 $P_{0}$ 有极大值(或极小值) $f(P_{0})$ .

二元函数的极值问题,一般可以利用偏导数来解决.下面两个定理就是关于这问题的结论.

定理1(必要条件) 设函数 $z = f(x, y)$ 在点 $(x_0, y_0)$ 具有偏导数，且在点 $(x_0, y_0)$ 处有极值，则有

$$
f _ {x} (x _ {0}, y _ {0}) = 0, \quad f _ {y} (x _ {0}, y _ {0}) = 0.
$$

证 不妨设 $z = f(x, y)$ 在点 $(x_0, y_0)$ 处有极大值. 依照极大值的定义, 在点 $(x_0, y_0)$ 的某邻域内异于 $(x_0, y_0)$ 的点 $(x, y)$ 都适合不等式

$$
f (x, y) <   f (x _ {0}, y _ {0}).
$$

特殊地，在该邻域内取 $y = y_0$ 而 $x \neq x_0$ 的点，也应适合不等式

$$
f (x, y _ {0}) <   f (x _ {0}, y _ {0}).
$$

这表明一元函数 $f(x,y_0)$ 在 $x = x_0$ 处取得极大值，因而必有

$$
f _ {x} (x _ {0}, y _ {0}) = 0.
$$

类似可证

$$
f _ {y} (x _ {0}, y _ {0}) = 0.
$$

从几何上看,这时如果曲面  $z=f(x,y)$  在点  $(x_{0},y_{0},z_{0})$  处有切平面,则切平面

$$
z - z _ {0} = f _ {x} (x _ {0}, y _ {0}) (x - x _ {0}) + f _ {y} (x _ {0}, y _ {0}) (y - y _ {0})
$$

成为平行于 xOy 坐标面的平面  $z-z_{0}=0$ .

类似地推得,如果三元函数  $u=f(x,y,z)$  在点  $(x_{0},y_{0},z_{0})$  具有偏导数,那么它在点  $(x_{0},y_{0},z_{0})$  具有极值的必要条件为

$$
f _ {x} (x _ {0}, y _ {0}, z _ {0}) = 0, \quad f _ {y} (x _ {0}, y _ {0}, z _ {0}) = 0, \quad f _ {z} (x _ {0}, y _ {0}, z _ {0}) = 0.
$$

仿照一元函数,凡是能使 $f_{x}(x,y)=0$ ,  $f_{y}(x,y)=0$ 同时成立的点 $(x_{0},y_{0})$ 称为函数 $z=f(x,y)$ 的驻点.从定理1可知,具有偏导数的函数的极值点必定是驻点.但函数的驻点不一定是极值点,例如,点(0,0)是函数z=xy的驻点,但函数在该点并无极值.

怎样判定一个驻点是否是极值点呢？下面的定理回答了这个问题.

定理2（充分条件）设函数 $z = f(x,y)$ 在点 $(x_0,y_0)$ 的某邻域内连续且有一阶及二阶连续偏导数，又 $f_{x}(x_{0},y_{0}) = 0,f_{y}(x_{0},y_{0}) = 0$ ，令

$$
f _ {x x} (x _ {0}, y _ {0}) = A, \quad f _ {x y} (x _ {0}, y _ {0}) = B, \quad f _ {y y} (x _ {0}, y _ {0}) = C,
$$

则 $f(x,y)$ 在 $(x_0,y_0)$ 处是否取得极值的条件如下:

(1) $AC - B^{2} > 0$ 时具有极值, 且当 $A < 0$ 时有极大值, 当 $A > 0$ 时有极小值;
(2) $AC - B^{2} < 0$ 时没有极值；
(3) $AC - B^{2} = 0$ 时可能有极值,也可能没有极值,还需另作讨论.

109

---

第九章 多元函数微分法及其应用

这个定理现在不证①. 利用定理1、定理2, 我们把具有二阶连续偏导数的函数 $z = f(x, y)$ 的极值的求法叙述如下:

第一步 解方程组

$$
f _ {x} (x, y) = 0, \quad f _ {y} (x, y) = 0,
$$

求得一切实数解,即可求得一切驻点.

第二步 对于每一个驻点 $(x_{0},y_{0})$ ，求出二阶偏导数的值A,B和C.

第三步 定出 $AC - B^2$ 的符号, 按定理 2 的结论判定 $f(x_0, y_0)$ 是不是极值、是极大值还是极小值.

例 4 求函数  $f(x,y)=x^{3}-y^{3}+3x^{2}+3y^{2}-9x$  的极值.

解 先解方程组

$$
\left\{ \begin{array}{l} f _ {x} (x, y) = 3 x ^ {2} + 6 x - 9 = 0, \\ f _ {y} (x, y) = - 3 y ^ {2} + 6 y = 0, \end{array} \right.
$$

求得驻点为(1,0),(1,2),(-3,0),(-3,2).

再求出二阶偏导数

$$
f _ {x x} (x, y) = 6 x + 6, \quad f _ {x y} (x, y) = 0, \quad f _ {y y} (x, y) = - 6 y + 6.
$$

在点(1,0)处,因为 $AC-B^{2}=12\times6>0$ ,又A>0,所以函数在(1,0)处有极小值 $f(1,0)=-5$ ;

在点(1,2)处,因为 $AC-B^{2}=12\times(-6)<0$ ,所以 $f(1,2)$ 不是极值;

在点 $(-3,0)$ 处，因为 $AC-B^{2}=-12\times6<0$ ，所以 $f(-3,0)$ 不是极值；

在点 $(-3,2)$ 处，因为 $AC-B^{2}=-12\times(-6)>0$ ，又A<0，所以函数在 $(-3,2)$ 处有极大值 $f(-3,2)=31$ .

讨论函数的极值问题时,如果函数在所讨论的区域内具有偏导数,那么由定理1可知,极值只可能在驻点处取得.然而,如果函数在个别点处的偏导数不存在,这些点当然不是驻点,但也可能是极值点.例如在例2中,函数 $z=-\sqrt{x^{2}+y^{2}}$ 在点(0,0)处的偏导数不存在,但该函数在点(0,0)处却具有极大值.因此,在考虑函数的极值问题时,除了考虑函数的驻点外,如果有偏导数不存在的点,那么对这些点也应当考虑.

与一元函数相类似,我们可以利用函数的极值来求函数的最大值和最小值.在第一节中已经指出,如果 $f(x,y)$ 在有界闭区域D上连续,那么 $f(x,y)$ 在D上必定能取得最大值和最小值.这种使函数取得最大值或最小值的点既可能在D的内部,也可能在D的边界上.我们假定,函数在D上连续、在D内可微分且只有有限个驻点,这时如果

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 证明见第九节第二目.</span></small>

110

---

第八节 多元函数的极值及其求法

函数在 $D$ 的内部取得最大值(最小值), 那么这个最大值(最小值)也是函数的极大值 (极小值). 因此, 在上述假定下, 求函数的最大值和最小值的一般方法是: 将函数 $f(x, y)$ 在 $D$ 内的所有驻点处的函数值及在 $D$ 的边界上的最大值和最小值相互比较, 其中最大的就是最大值, 最小的就是最小值. 但这种做法, 由于要求出 $f(x, y)$ 在 $D$ 的边界上的最大值和最小值, 所以往往相当复杂. 在通常遇到的实际问题中, 如果根据问题的性质, 知道函数 $f(x, y)$ 的最大值(最小值)一定在 $D$ 的内部取得, 而函数在 $D$ 内只有一个驻点, 那么可以肯定该驻点处的函数值就是函数 $f(x, y)$ 在 $D$ 上的最大值(最小值).

例 5 某厂要用铁板做成一个体积为  $2 \, m^{3}$  的有盖长方体水箱. 问当长、宽和高各取怎样的尺寸时, 才能使用料最省.

解 设水箱的长为 $x \mathrm{~m}$, 宽为 $y \mathrm{~m}$, 则其高应为 $\frac{2}{xy} \mathrm{~m}$. 此水箱所用材料的面积为 $A = 2\left(xy + y \cdot \frac{2}{xy} + x \cdot \frac{2}{xy}\right)$, 即

$$
A = 2 \left(x y + \frac {2}{x} + \frac {2}{y}\right) \quad (x > 0, y > 0).
$$

可见材料面积 $A = A(x,y)$ 是 $x$ 和 $y$ 的二元函数，这就是目标函数，下面求使这函数取得最小值的点 $(x,y)$.

令

$$
A _ {x} = 2 \left(y - \frac {2}{x ^ {2}}\right) = 0, \quad A _ {y} = 2 \left(x - \frac {2}{y ^ {2}}\right) = 0.
$$

解这方程组,得

$$
x = \sqrt [ 3 ]{2}, \quad y = \sqrt [ 3 ]{2}.
$$

根据题意可以知道,水箱所用材料面积的最小值一定存在,并在开区域  $D=\{(x,y)\mid x>0,y>0\}$  内取得.又函数在 D 内只有唯一的驻点  $(\sqrt[3]{2},\sqrt[3]{2})$ , 因此可断定当  $x=\sqrt[3]{2},y=\sqrt[3]{2}$  时,A 取得最小值.就是说,当水箱的长为  $\sqrt[3]{2}$  m、宽为  $\sqrt[3]{2}$  m、高为  $\frac{2}{\sqrt[3]{2}\cdot\sqrt[3]{2}}=\sqrt[3]{2}$  m 时,水箱所用的材料最省.

从这个例子还可看出,在体积一定的长方体中,以立方体的表面积为最小.

例 6 有一宽为 24 cm 的长方形铁板,把它两边折起来做成一断面为等腰梯形的水槽.问怎样折法才能使断面的面积最大?

解 设折起来的边长为 $x \mathrm{~cm}$, 倾角为 $\alpha$ (图9-11), 则梯形断面的下底长为 $(24 - 2x) \mathrm{~cm}$, 上底长为 $(24 - 2x + 2x \cos \alpha) \mathrm{~cm}$, 高为 $(x \sin \alpha) \mathrm{~cm}$, 所以断面面积

111

---

第九章 多元函数微分法及其应用

$$
A = \frac {1}{2} (2 4 - 2 x + 2 x \cos \alpha + 2 4 - 2 x) \cdot x \sin \alpha ,
$$

即

$$
A = 2 4 x \sin \alpha - 2 x ^ {2} \sin \alpha + x ^ {2} \sin \alpha \cos \alpha \quad \left(0 <   x <   1 2, 0 <   \alpha \leqslant \frac {\pi}{2}\right).
$$

可见断面面积 $A = A(x, \alpha)$, 这就是目标函数, 下面求使这函数取得最大值的点 $(x, \alpha)$. 令

$$
\left\{ \begin{array}{l} A _ {x} = 2 4 \sin \alpha - 4 x \sin \alpha + 2 x \sin \alpha \cos \alpha = 0, \\ A _ {\alpha} = 2 4 x \cos \alpha - 2 x ^ {2} \cos \alpha + x ^ {2} (\cos^ {2} \alpha - \sin^ {2} \alpha) = 0. \end{array} \right.
$$

由于 $\sin \alpha \neq 0, x \neq 0$ ，上述方程组可化为

$$
\left\{ \begin{array}{l} 1 2 - 2 x + x \cos \alpha = 0, \\ 2 4 \cos \alpha - 2 x \cos \alpha + x (\cos^ {2} \alpha - \sin^ {2} \alpha) = 0. \end{array} \right.
$$

解这方程组,得

$$
\alpha = \frac {\pi}{3}, \quad x = 8.
$$

![](../../raw/pages_0097-0128/images/page_118_image_10.jpg)

<details>
<summary>text_image</summary>

24
x
α
24-2x
x
α
</details>

图9-11

根据题意可知断面面积的最大值一定存在,并且在  $D=\left\{(x,\alpha)\mid0<x<12,0<\alpha\leqslant\frac{\pi}{2}\right\}$  内取得.通过计算得知  $\alpha=\frac{\pi}{2}$  时的函数值比  $\alpha=\frac{\pi}{3},x=8$  时的函数值小.又函数在 D 内只有一个驻点,因此可以断定,当  $x=8,\alpha=\frac{\pi}{3}$  时,就能使断面的面积最大.

## 二、条件极值 拉格朗日乘数法

上面所讨论的极值问题,对于函数的自变量,除了限制在函数的定义域内以外,并无其他条件,所以有时候称为无条件极值.但在实际问题中,有时会遇到对函数的自变量还有附加条件的极值问题.例如,求表面积为 $a^2$ 而体积为最大的长方体的体积问题.设长方体的三棱的长为 $x,y$ 与 $z$,则体积 $V = xyz$.又因假定表面积为 $a^2$,所以自变量 $x,y$ 与 $z$ 还必须满足附加条件 $2(xy + yz + xz) = a^2$.像这种对自变量有附加条件的极值称

112

---

第八节 多元函数的极值及其求法

为条件极值.对于有些实际问题,可以把条件极值化为无条件极值,然后利用第一目中的方法加以解决.例如上述问题,可由条件 $2(xy+yz+xz)=a^{2}$ ,将z表示成

$$
z = \frac {a ^ {2} - 2 x y}{2 (x + y)}.
$$

再把它代入 $V = xyz$ 中，于是问题就化为求

$$
V = \frac {x y}{2} \left(\frac {a ^ {2} - 2 x y}{x + y}\right)
$$

的无条件极值.例5也是属于把条件极值化为无条件极值的例子.

但在很多情形下,将条件极值化为无条件极值并不这样简单.另有一种直接寻求条件极值的方法,可以不必先把问题化到无条件极值的问题,这就是下面要介绍的拉格朗日乘数法.

现在先来寻求函数

$$
z = f (x, y) \tag {8-1}
$$

在条件

$$
\varphi (x, y) = 0 \tag {8-2}
$$

下取得极值的必要条件.

如果函数(8-1)在 $(x_0,y_0)$ 取得所求的极值，那么首先有

$$
\varphi (x _ {0}, y _ {0}) = 0. \tag {8-3}
$$

我们假定在 $(x_0, y_0)$ 的某一邻域内 $f(x, y)$ 与 $\varphi(x, y)$ 均有连续的一阶偏导数，而 $\varphi_y(x_0, y_0) \neq 0$. 由隐函数存在定理可知，方程(8-2)确定一个连续且具有连续导数的函数 $y = \psi(x)$，将其代入(8-1)式，结果得到一个变量 $x$ 的函数

$$
z = f [ x, \psi (x) ]. \tag {8-4}
$$

于是函数(8-1)在 $(x_{0},y_{0})$ 取得所求的极值,也就是相当于函数(8-4)在 $x=x_{0}$ 取得极值.由一元可导函数取得极值的必要条件知道

$$
\frac {\mathrm{d} z}{\mathrm{d} x} \Big | _ {x = x _ {0}} = f _ {x} (x _ {0}, y _ {0}) + f _ {y} (x _ {0}, y _ {0}) \frac {\mathrm{d} y}{\mathrm{d} x} \Big | _ {x = x _ {0}} = 0, \tag {8-5}
$$

而由(8-2)用隐函数求导公式,有

$$
\frac {\mathrm{d} y}{\mathrm{d} x} \Big | _ {x = x _ {0}} = - \frac {\varphi_ {x} (x _ {0} , y _ {0})}{\varphi_ {y} (x _ {0} , y _ {0})}.
$$

把上式代入(8-5)式,得

$$
f _ {x} (x _ {0}, y _ {0}) - f _ {y} (x _ {0}, y _ {0}) \frac {\varphi_ {x} (x _ {0} , y _ {0})}{\varphi_ {y} (x _ {0} , y _ {0})} = 0. \tag {8-6}
$$

(8-3)、(8-6)两式就是函数(8-1)在条件(8-2)下在 $(x_{0},y_{0})$ 取得极值的必要条件.

设 $\frac{f_y(x_0,y_0)}{\varphi_y(x_0,y_0)} = -\lambda$ ，上述必要条件就变为

113

---

第九章 多元函数微分法及其应用

$$
\left\{ \begin{array}{l} f _ {x} (x _ {0}, y _ {0}) + \lambda \varphi_ {x} (x _ {0}, y _ {0}) = 0, \\ f _ {y} (x _ {0}, y _ {0}) + \lambda \varphi_ {y} (x _ {0}, y _ {0}) = 0, \\ \varphi (x _ {0}, y _ {0}) = 0. \end{array} \right. \tag {8-7}
$$

若引进辅助函数

$$
L (x, y) = f (x, y) + \lambda \varphi (x, y),
$$

则不难看出，(8-7)中前两式就是

$$
L _ {x} (x _ {0}, y _ {0}) = 0, \quad L _ {y} (x _ {0}, y _ {0}) = 0.
$$

函数  $L(x,y)$  称为拉格朗日函数, 参数  $\lambda$  称为拉格朗日乘子.

由以上讨论,我们得到以下结论:

拉格朗日乘数法 要找函数 $z = f(x,y)$ 在附加条件 $\varphi (x,y) = 0$ 下的可能极值点，可以先作拉格朗日函数

$$
L (x, y) = f (x, y) + \lambda \varphi (x, y),
$$

其中  $\lambda$  为参数. 求其对 x 与 y 的一阶偏导数, 并使之为零, 然后与方程(8-2)联立起来:

$$
\left\{ \begin{array}{l} f _ {x} (x, y) + \lambda \varphi_ {x} (x, y) = 0, \\ f _ {y} (x, y) + \lambda \varphi_ {y} (x, y) = 0, \\ \varphi (x, y) = 0. \end{array} \right. \tag {8-8}
$$

由这方程组解出 $x, y$ 及 $\lambda$, 这样得到的 $(x, y)$ 就是函数 $f(x, y)$ 在附加条件 $\varphi(x, y) = 0$ 下的可能极值点.

这方法还可以推广到自变量多于两个而条件多于一个的情形.例如,要求函数

$$
u = f (x, y, z, t)
$$

在附加条件

$$
\varphi (x, y, z, t) = 0, \quad \psi (x, y, z, t) = 0 \tag {8-9}
$$

下的极值,可以先作拉格朗日函数

$$
L (x, y, z, t) = f (x, y, z, t) + \lambda \varphi (x, y, z, t) + \mu \psi (x, y, z, t),
$$

其中 $\lambda, \mu$ 均为参数, 求其一阶偏导数, 并使之为零, 然后与(8-9)中的两个方程联立起来求解, 这样得出的 $(x, y, z, t)$ 就是函数 $f(x, y, z, t)$ 在附加条件(8-9)下的可能极值点.

至于如何确定所求得的点是不是极值点,在实际问题中往往可根据问题本身的性质来判定.

例 7 求表面积为  $a^{2}$  而体积为最大的长方体的体积.

解 设长方体的三棱长为 $x, y$ 与 $z$, 则问题就是在条件

$$
\varphi (x, y, z) = 2 x y + 2 y z + 2 x z - a ^ {2} = 0 \tag {8-10}
$$

下,求函数

114

---

第八节 多元函数的极值及其求法

$$
V = x y z \quad (x > 0, y > 0, z > 0)
$$

的最大值.作拉格朗日函数

$$
L (x, y, z) = x y z + \lambda (2 x y + 2 y z + 2 x z - a ^ {2}),
$$

求其对 $x, y$ 与 $z$ 的偏导数，并使之为零，得到

$$
\left\{ \begin{array}{l} y z + 2 \lambda (y + z) = 0, \\ x z + 2 \lambda (x + z) = 0, \\ x y + 2 \lambda (y + x) = 0. \end{array} \right. \tag {8-11}
$$

再与(8-10)联立求解.

因为 $x, y$ 与 $z$ 都不等于零，所以由(8-11)可得

$$
\frac {x}{y} = \frac {x + z}{y + z}, \quad \frac {y}{z} = \frac {x + y}{x + z}.
$$

由以上两式解得

$$
x = y = z.
$$

将此代入(8-10)式,便得

$$
x = y = z = \frac {\sqrt {6}}{6} a,
$$

这是唯一可能的极值点.因为由问题本身可知最大值一定存在,所以最大值就在这个可能的极值点处取得.也就是说,表面积为 $a^{2}$ 的长方体中,以棱长为 $\frac{\sqrt{6}}{6}a$ 的立方体的体积为最大,最大体积 $V=\frac{\sqrt{6}}{36}a^{3}$ .

例8 求函数 $u = xyz$ 在附加条件

$$
\frac {1}{x} + \frac {1}{y} + \frac {1}{z} = \frac {1}{a} \quad (x > 0, y > 0, z > 0, a > 0) \tag {8-12}
$$

下的极值.

解 作拉格朗日函数

$$
L (x, y, z) = x y z + \lambda \left(\frac {1}{x} + \frac {1}{y} + \frac {1}{z} - \frac {1}{a}\right).
$$

令

$$
\left\{ \begin{array}{l} L _ {x} = y z - \frac {\lambda}{x ^ {2}} = 0, \\ L _ {y} = x z - \frac {\lambda}{y ^ {2}} = 0, \\ L _ {z} = x y - \frac {\lambda}{z ^ {2}} = 0. \end{array} \right. \tag {8-13}
$$

115

---

第九章 多元函数微分法及其应用

注意到以上三个方程左端的第一项都是三个变量 $x, y$ 与 $z$ 中某两个变量的乘积，将各方程两端同乘相应缺少的那个变量，使各方程左端的第一项都成为 $xyz$ ，然后将所得的三个方程左、右两端相加，得

$$
3 x y z - \lambda \left(\frac {1}{x} + \frac {1}{y} + \frac {1}{z}\right) = 0,
$$

把(8-12)代入上式,得

$$
xyz = \frac {\lambda}{3 a}.
$$

再把这个结果分别代入(8-13)中各式,便得x=y=z=3a.由此得到点 $(3a,3a,3a)$ 是函数u=xyz在条件(8-12)下唯一可能的极值点.把条件(8-12)确定的隐函数记作 $z=z(x,y)$ ,将目标函数看做 $u=xyz(x,y)=F(x,y)$ ,再应用二元函数极值的充分条件判断,可知点 $(3a,3a,3a)$ 是函数u=xyz在条件(8-12)下的极小值点.因此,目标函数u=xyz在条件(8-12)下在点 $(3a,3a,3a)$ 处取得极小值 $27a^{3}$ .

下面的问题涉及经济学中的一个最优价格的模型.

在生产和销售商品过程中,商品销售量、生产成本与销售价格是相互影响的.厂家要选择合理的销售价格,才能获得最大利润.这个价格称为最优价格.下面的例题就是讨论怎样确定电视机的最优价格.

例 9 设某电视机厂生产一台电视机的成本为 C, 每台电视机的销售价格为 p, 销售量为 x. 假设该厂的生产处于平衡状态, 即电视机的生产量等于销售量. 根据市场预测, 销售量 x 与销售价格 p 之间有下面的关系:

$$
x = M \mathrm{e} ^ {- a p} \quad (M > 0, a > 0), \tag {8-14}
$$

其中 M 为市场最大需求量, a 是价格系数. 同时, 生产部门根据对生产环节的分析, 对每台电视机的生产成本 C 有如下测算:

$$
C = C _ {0} - k \ln x \quad (k > 0, x > 1), \tag {8-15}
$$

其中  $C_{0}$  是只生产一台电视机时的成本, k 是规模系数.

根据上述条件,应如何确定电视机的售价p,才能使该厂获得最大利润?

解 设厂家获得的利润为 u, 每台电视机售价为 p, 每台生产成本为 C, 销售量为 x, 则

$$
u = (p - C) x.
$$

于是问题化为求利润函数 $u = (p - C)x$ 在附加条件(8-14)、(8-15)下的极值问题.

作拉格朗日函数

$$
L (x, p, C) = (p - C) x + \lambda (x - M \mathrm{e} ^ {- a p}) + \mu (C - C _ {0} + k \ln x).
$$

令

116

---

第八节 多元函数的极值及其求法

$$
\left\{ \begin{array}{l} L _ {x} = (p - C) + \lambda + k \frac {\mu}{x} = 0, \\ L _ {p} = x + \lambda a M \mathrm{e} ^ {- a p} = 0, \\ L _ {C} = - x + \mu = 0. \end{array} \right.
$$

将(8-14)代入(8-15)，得

$$
C = C _ {0} - k (\ln M - a p). \tag {8-16}
$$

由(8-14)及 $L_{p}=0$ 知 $\lambda a=-1$ ，即

$$
\lambda = - \frac {1}{a}. \tag {8-17}
$$

由 $L_{C} = 0$ 知 $x = \mu$ ，即

$$
\frac {x}{\mu} = 1. \tag {8-18}
$$

将(8-16)、(8-17)和(8-18)代入 $L_{x}=0$ ，得

$$
p - C _ {0} + k (\ln M - a p) - \frac {1}{a} + k = 0,
$$

由此得

$$
p ^ {*} = \frac {C _ {0} - k \ln M + \frac {1}{a} - k}{1 - a k}.
$$

因为由问题本身可知最优价格必定存在,所以这个  $p^{*}$  就是电视机的最优价格.只要确定了规模系数 k、价格系数 a,电视机的最优价格问题就解决了.

## 习题9-8

1. 已知函数 $f(x, y)$ 在点(0,0)的某个邻域内连续，且

$$
\lim _ {(x, y) \to (0, 0)} \frac {f (x , y) - x y}{(x ^ {2} + y ^ {2}) ^ {2}} = 1,
$$

则下述四个选项中正确的是( ).

(A) 点 $(0,0)$ 不是 $f(x,y)$ 的极值点
(B) 点 $(0,0)$ 是 $f(x,y)$ 的极大值点
(C) 点 $(0,0)$ 是 $f(x,y)$ 的极小值点
(D) 根据所给条件无法判断(0,0)是不是 $f(x,y)$ 的极值点

2. 求函数 $f(x, y) = 4(x - y) - x^2 - y^2$ 的极值.

3. 求函数  $f(x,y)=(6x-x^{2})(4y-y^{2})$  的极值.

4. 求两直线  $\left\{\begin{aligned} y &= 2x, \\ z &= x + 1 \end{aligned}\right.$  与  $\left\{\begin{aligned} y &= x + 3, \\ z &= x \end{aligned}\right.$  之间的最短距离.

117

---

第九章 多元函数微分法及其应用

5. 求函数 z=xy 在适合附加条件  $x+y=1$  下的极大值.
6. 从斜边长为 l 的一切直角三角形中, 求有最大周长的直角三角形.
7. 要造一个体积等于定数 $k$ 的长方体无盖水池, 应如何选择水池的尺寸, 方可使它的表面积最小.
8. 在平面 $xOy$ 上求一点, 使它到 $x = 0, y = 0$ 及 $x + 2y - 16 = 0$ 三直线的距离平方之和为最小.
9. 将周长为 2p 的矩形绕它的一边旋转而构成一个圆柱体. 问矩形的边长各为多少时, 才可使圆柱体的体积为最大?

10. 求内接于半径为 a 的球且有最大体积的长方体.

11. 抛物面  $z=x^{2}+y^{2}$  被平面  $x+y+z=1$  截成一椭圆, 求这椭圆上的点到原点的距离的最大值与最小值.
12. 设有一圆板占有平面闭区域  $\{(x,y) \mid x^{2}+y^{2}\leqslant1\}$ . 该圆板被加热, 以致在点  $(x,y)$  的温度是  $T=x^{2}+2y^{2}-x$ . 求该圆板的最热点和最冷点.
13. 形状为椭球  $4x^{2}+y^{2}+4z^{2}\leqslant16$  的空间探测器进入地球大气层, 其表面开始受热, 1 h 后在探测器的点  $(x,y,z)$  处的温度  $T=8x^{2}+4yz-16z+600$ , 求探测器表面最热的点.

## \* 第九节 二元函数的泰勒公式

## 一、二元函数的泰勒公式

在上册第三章,我们已经知道:若函数 $f(x)$ 在 $x_{0}$ 的某邻域内具有直到 $(n+1)$ 阶导数,则对该邻域内的任一x,有n阶泰勒公式

$$
f (x) = f (x _ {0}) + f ^ {\prime} (x _ {0}) (x - x _ {0}) + \frac {f ^ {\prime \prime} (x _ {0})}{2 !} (x - x _ {0}) ^ {2} + \dots + \frac {f ^ {(n)} (x _ {0})}{n !} (x - x _ {0}) ^ {n} +
$$

$$
\frac {f ^ {(n + 1)} (x _ {0} + \theta (x - x _ {0}))}{(n + 1) !} (x - x _ {0}) ^ {n + 1} \quad (0 <   \theta <   1)
$$

成立.利用一元函数的泰勒公式,我们可用n次多项式来近似表达函数 $f(x)$ ,且误差是当 $x\to x_{0}$ 时比 $(x-x_{0})^{n}$ 高阶的无穷小.对于多元函数来说,无论是为了理论的或实际计算的需要,也都有必要考虑用多个变量的多项式来近似表达一个给定的多元函数,并能具体地估算出误差的大小来.今以二元函数为例,设 $z=f(x,y)$ 在点 $(x_{0},y_{0})$ 的某一邻域内连续且有 $(n+1)$ 阶连续偏导数, $(x_{0}+h,y_{0}+k)$ 为此邻域内任一点,我们的问题就是要把函数 $f(x_{0}+h,y_{0}+k)$ 近似地表达为 $h=x-x_{0},k=y-y_{0}$ 的n次多项式,而由此所产生的误差是当 $\rho=\sqrt{h^{2}+k^{2}}\rightarrow0$ 时比 $\rho^{n}$ 高阶的无穷小.为了解决这个问题,就要把一元函数的泰勒中值定理推广到多元函数的情形.

定理 设 $z = f(x, y)$ 在点 $(x_0, y_0)$ 的某一邻域内连续且有 $(n + 1)$ 阶连续偏导数，

118

---

\* 第九节 二元函数的泰勒公式

$(x_{0}+h,y_{0}+k)$ 为此邻域内任一点,则有

$$
\begin{array}{l} f (x _ {0} + h, y _ {0} + k) = f (x _ {0}, y _ {0}) + \left(h \frac {\partial}{\partial x} + k \frac {\partial}{\partial y}\right) f (x _ {0}, y _ {0}) + \\ \frac {1}{2 !} \left(h \frac {\partial}{\partial x} + k \frac {\partial}{\partial y}\right) ^ {2} f (x _ {0}, y _ {0}) + \dots + \frac {1}{n !} \left(h \frac {\partial}{\partial x} + k \frac {\partial}{\partial y}\right) ^ {n} f (x _ {0}, y _ {0}) + \\ \frac {1}{(n + 1) !} \left(h \frac {\partial}{\partial x} + k \frac {\partial}{\partial y}\right) ^ {n + 1} f (x _ {0} + \theta h, y _ {0} + \theta k) \quad (0 <   \theta <   1). \\ \end{array}
$$

其中记号

$\left(h\frac{\partial}{\partial x} + k\frac{\partial}{\partial y}\right)f(x_0, y_0)$ 表示 $h f_{x}(x_{0}, y_{0}) + k f_{y}(x_{0}, y_{0})$

$\left(h\frac{\partial}{\partial x} + k\frac{\partial}{\partial y}\right)^{2}f(x_{0},y_{0})$ 表示 $h^2 f_{xx}(x_0,y_0) + 2hkf_{xy}(x_0,y_0) + k^2 f_{yy}(x_0,y_0),$

一般地,记号

$\left(h\frac{\partial}{\partial x} + k\frac{\partial}{\partial y}\right)^m f(x_0, y_0)$ 表示 $\sum_{p=0}^{m} C_m^p h^p k^{m-p} \frac{\partial^m f}{\partial x^p \partial y^{m-p}} \bigg|_{(x_0, y_0)}.$

证 为了利用一元函数的泰勒公式来进行证明,我们引入函数

$$
\Phi (t) = f (x _ {0} + h t, y _ {0} + k t) \quad (0 \leqslant t \leqslant 1).
$$

显然 $\Phi(0) = f(x_0, y_0), \Phi(1) = f(x_0 + h, y_0 + k)$. 由 $\Phi(t)$ 的定义及多元复合函数的求导法则, 可得

$$
\Phi^ {\prime} (t) = h f _ {x} (x _ {0} + h t, y _ {0} + k t) + k f _ {y} (x _ {0} + h t, y _ {0} + k t) = \left(h \frac {\partial}{\partial x} + k \frac {\partial}{\partial y}\right) f (x _ {0} + h t, y _ {0} + k t),
$$

$$
\begin{array}{l} \Phi^ {\prime \prime} (t) = h ^ {2} f _ {x x} (x _ {0} + h t, y _ {0} + k t) + 2 h k f _ {x y} (x _ {0} + h t, y _ {0} + k t) + k ^ {2} f _ {y y} (x _ {0} + h t, y _ {0} + k t) \\ = \left(h \frac {\partial}{\partial x} + k \frac {\partial}{\partial y}\right) ^ {2} f (x _ {0} + h t, y _ {0} + k t), \\ \end{array}
$$

...

$$
\Phi^ {(n + 1)} (t) = \sum_ {p = 0} ^ {n + 1} \mathrm{C} _ {n + 1} ^ {p} h ^ {p} k ^ {n + 1 - p} \frac {\partial^ {n + 1} f}{\partial x ^ {p} \partial y ^ {n + 1 - p}} \Bigg | _ {(x _ {0} + h t, y _ {0} + k t)} = \left(h \frac {\partial}{\partial x} + k \frac {\partial}{\partial y}\right) ^ {n + 1} f (x _ {0} + h t, y _ {0} + k t).
$$

利用一元函数的麦克劳林公式,得

$$
\Phi (1) = \Phi (0) + \Phi^ {\prime} (0) + \frac {1}{2 !} \Phi^ {\prime \prime} (0) + \dots + \frac {1}{n !} \Phi^ {(n)} (0) + \frac {1}{(n + 1) !} \Phi^ {(n + 1)} (\theta), \quad (0 <   \theta <   1).
$$

将  $\Phi(0)=f(x_{0},y_{0}),\Phi(1)=f(x_{0}+h,y_{0}+k)$  及上面求得的  $\Phi(t)$  直到 n 阶导数在 t=0 的值，以及  $\Phi^{(n+1)}(t)$  在  $t=\theta$  的值代入上式，即得

$$
f (x _ {0} + h, y _ {0} + k) = f (x _ {0}, y _ {0}) + \left(h \frac {\partial}{\partial x} + k \frac {\partial}{\partial y}\right) f (x _ {0}, y _ {0}) + \frac {1}{2 !} \left(h \frac {\partial}{\partial x} + k \frac {\partial}{\partial y}\right) ^ {2} f (x _ {0}, y _ {0}) + \dots +
$$

119

---

第九章 多元函数微分法及其应用

$$
\frac {1}{n !} \left(h \frac {\partial}{\partial x} + k \frac {\partial}{\partial y}\right) ^ {n} f (x _ {0}, y _ {0}) + R _ {n}, \tag {9-1}
$$

其中

$$
R _ {n} = \frac {1}{(n + 1) !} \left(h \frac {\partial}{\partial x} + k \frac {\partial}{\partial y}\right) ^ {n + 1} f (x _ {0} + \theta h, y _ {0} + \theta k) \quad (0 <   \theta <   1). \tag {9-2}
$$

定理证毕.

公式(9-1)称为二元函数 $f(x,y)$ 在点 $(x_{0},y_{0})$ 的n阶泰勒公式，而 $R_{n}$ 的表达式(9-2)称为拉格朗日余项.

由二元函数的泰勒公式可知,以(9-1)式右端h及k的n次多项式近似表达函数 $f(x_{0}+h,y_{0}+k)$ 时,其误差为 $|R_{n}|$ .由假设,函数的各 $(n+1)$ 阶偏导数都连续,故它们的绝对值在点 $(x_{0},y_{0})$ 的某一邻域内都不超过某一正常数M.于是,有下面的误差估计式:

$$
\begin{array}{l} \left| R _ {n} \right| \leqslant \frac {M}{(n + 1) !} (\left| h \right| + \left| k \right|) ^ {n + 1} = \frac {M}{(n + 1) !} \rho^ {n + 1} \left(\frac {| h |}{\rho} + \frac {| k |}{\rho}\right) ^ {n + 1} \\ \leqslant \frac {M}{(n + 1) !} (\sqrt {2}) ^ {n + 1} \rho^ {n + 1} ①, \tag {9-3} \\ \end{array}
$$

其中  $\rho=\sqrt{h^{2}+k^{2}}$ .

由(9-3)式可知,误差 $|R_{n}|$ 是当 $\rho\rightarrow0$ 时比 $\rho^{n}$ 高阶的无穷小.

当 n=0 时, 公式(9-1)成为

$$
\begin{array}{l} f (x _ {0} + h, y _ {0} + k) \\ = f (x _ {0}, y _ {0}) + h f _ {x} (x _ {0} + \theta h, y _ {0} + \theta k) + k f _ {y} (x _ {0} + \theta h, y _ {0} + \theta k). \tag {9-4} \\ \end{array}
$$

公式(9-4)称为二元函数的拉格朗日中值公式.由(9-4)式即可推得下述结论:

推论 如果函数 $f(x,y)$ 的偏导数 $f_{x}(x,y), f_{y}(x,y)$ 在某一区域内都恒等于零，那么函数 $f(x,y)$ 在该区域内为一常数.

例 求函数 $f(x, y) = \ln (1 + x + y)$ 在点(0,0)的三阶泰勒公式.

解 因为

$$
f _ {x} (x, y) = f _ {y} (x, y) = \frac {1}{1 + x + y},
$$

$$
f _ {x x} (x, y) = f _ {x y} (x, y) = f _ {y y} (x, y) = - \frac {1}{(1 + x + y) ^ {2}},
$$

$$
\frac {\partial^ {3} f}{\partial x ^ {p} \partial y ^ {3 - p}} = \frac {2 !}{(1 + x + y) ^ {3}} \quad (p = 0, 1, 2, 3),
$$

① 令 $\frac{|h|}{\rho} = \cos \alpha, \frac{|k|}{\rho} = \sin \alpha$，则 $\cos \alpha + \sin \alpha = \sqrt{2} \sin \left( \alpha + \frac{\pi}{4} \right) \leqslant \sqrt{2}$.

120

---

\* 第九节 二元函数的泰勒公式

$$
\frac {\partial^ {4} f}{\partial x ^ {p} \partial y ^ {4 - p}} = - \frac {3 !}{(1 + x + y) ^ {4}} \quad (p = 0, 1, 2, 3, 4),
$$

所以

$$
\begin{array}{l} \left(h \frac {\partial}{\partial x} + k \frac {\partial}{\partial y}\right) f (0, 0) = h f _ {x} (0, 0) + k f _ {y} (0, 0) = h + k, \\ \left(h \frac {\partial}{\partial x} + k \frac {\partial}{\partial y}\right) ^ {2} f (0, 0) = h ^ {2} f _ {x x} (0, 0) + 2 h k f _ {x y} (0, 0) + k ^ {2} f _ {y y} (0, 0) = - (h + k) ^ {2}, \\ \left(h \frac {\partial}{\partial x} + k \frac {\partial}{\partial y}\right) ^ {3} f (0, 0) = h ^ {3} f _ {x x x} (0, 0) + 3 h ^ {2} k f _ {x x y} (0, 0) + 3 h k ^ {2} f _ {x y y} (0, 0) + k ^ {3} f _ {y y y} (0, 0) = 2 (h + k) ^ {3}. \\ \end{array}
$$

又 $f(0,0) = 0$ ，并将 $h = x, k = y$ 代入，由三阶泰勒公式便得

$$
\ln (1 + x + y) = x + y - \frac {1}{2} (x + y) ^ {2} + \frac {1}{3} (x + y) ^ {3} + R _ {3},
$$

其中

$$
R _ {3} = \frac {1}{4 !} \left[ \left(h \frac {\partial}{\partial x} + k \frac {\partial}{\partial y}\right) ^ {f} (\theta h, \theta k) \right] _ {h = x, k = y} = - \frac {1}{4} \cdot \frac {(x + y) ^ {4}}{(1 + \theta x + \theta y) ^ {4}} \quad (0 <   \theta <   1).
$$

## 二、极值充分条件的证明

下面来证明第八节中的定理 2.

设函数 $z = f(x,y)$ 在点 $P_0(x_0,y_0)$ 的某邻域 $U_{1}(P_{0})$ 内连续且有一阶及二阶连续偏导数，又 $f_{x}(x_{0},y_{0}) = 0,f_{y}(x_{0},y_{0}) = 0.$

依二元函数的泰勒公式,对于任一 $(x_{0}+h,y_{0}+k)\in U_{1}(P_{0})$ 有

$$
\begin{array}{l} \Delta f = f (x _ {0} + h, y _ {0} + k) - f (x _ {0}, y _ {0}) \\ = \frac {1}{2} \left[ h ^ {2} f _ {x x} (x _ {0} + \theta h, y _ {0} + \theta k) + 2 h k f _ {x y} (x _ {0} + \theta h, y _ {0} + \theta k) + k ^ {2} f _ {y y} (x _ {0} + \theta h, y _ {0} + \theta k) \right] \quad (0 <   \theta <   1). \tag {9-5} \\ \end{array}
$$

(1) 设  $AC-B^{2}>0$ , 即

$$
f _ {x x} (x _ {0}, y _ {0}) f _ {y y} (x _ {0}, y _ {0}) - [ f _ {x y} (x _ {0}, y _ {0}) ] ^ {2} > 0. \tag {9-6}
$$

因 $f(x,y)$ 的二阶偏导数在 $U_{1}(P_{0})$ 内连续，由不等式(9-6)可知，存在点 $P_0$ 的邻域 $U_{2}(P_{0})\subset U_{1}(P_{0})$ ，使得对任一 $(x_0 + h,y_0 + k)\in U_2(P_0)$ 有

$$
f _ {x x} (x _ {0} + \theta h, y _ {0} + \theta k) f _ {y y} (x _ {0} + \theta h, y _ {0} + \theta k) - [ f _ {x y} (x _ {0} + \theta h, y _ {0} + \theta k) ] ^ {2} > 0. \tag {9-7}
$$

为书写简便起见，把 $f_{xx}(x,y), f_{xy}(x,y), f_{yy}(x,y)$ 在点 $(x_0 + \theta h, y_0 + \theta k)$ 处的值依次记为 $f_{xx}, f_{xy}, f_{yy}$. 由(9-7)式可知，当 $(x_0 + h, y_0 + k) \in U_2(P_0)$ 时，$f_{xx}$ 及 $f_{yy}$ 都不等于零且两者同号. 于是(9-5)式可写成

$$
\Delta f = \frac {1}{2 f _ {x x}} \left[ (h f _ {x x} + k f _ {x y}) ^ {2} + k ^ {2} (f _ {x x} f _ {y y} - f _ {x y} ^ {2}) \right].
$$

121

---

第九章 多元函数微分法及其应用

当 $h, k$ 不同时为零且 $(x_0 + h, y_0 + k) \in U_2(P_0)$ 时，上式右端方括号内的值为正，所以 $\Delta f$ 异于零且与 $f_{xx}$ 同号。又由 $f(x, y)$ 的二阶偏导数的连续性知 $f_{xx}$ 与 $A$ 同号，因此 $\Delta f$ 与 $A$ 同号。所以，当 $A > 0$ 时 $f(x_0, y_0)$ 为极小值，当 $A < 0$ 时 $f(x_0, y_0)$ 为极大值。

(2) 设  $AC-B^{2}<0$  , 即

$$
f _ {x x} (x _ {0}, y _ {0}) f _ {y y} (x _ {0}, y _ {0}) - [ f _ {x y} (x _ {0}, y _ {0}) ] ^ {2} <   0. \tag {9-8}
$$

先假定 $f_{xx}(x_0,y_0) = f_{yy}(x_0,y_0) = 0$ ，于是由(9-8)式可知这时 $f_{xy}(x_0,y_0)\neq 0.$ 现在分别令 $k = h$ 及 $k = -h$ ，则由(9-5)式分别得

$$
\Delta f = \frac {h ^ {2}}{2} [ f _ {x x} (x _ {0} + \theta_ {1} h, y _ {0} + \theta_ {1} h) + 2 f _ {x y} (x _ {0} + \theta_ {1} h, y _ {0} + \theta_ {1} h) + f _ {y y} (x _ {0} + \theta_ {1} h, y _ {0} + \theta_ {1} h) ]
$$

及

$$
\Delta f = \frac {h ^ {2}}{2} \left[ f _ {x x} (x _ {0} + \theta_ {2} h, y _ {0} - \theta_ {2} h) - 2 f _ {x y} (x _ {0} + \theta_ {2} h, y _ {0} - \theta_ {2} h) + f _ {y y} (x _ {0} + \theta_ {2} h, y _ {0} - \theta_ {2} h) \right],
$$

其中 $0 < \theta_{1}, \theta_{2} < 1$. 当 $h \to 0$ 时，以上两式中右端方括号内的式子分别趋于极限

$$
2 f _ {x y} (x _ {0}, y _ {0}) \quad \text {及} \quad - 2 f _ {x y} (x _ {0}, y _ {0}),
$$

从而当 h 充分接近零时,两式中方括号内的值有相反的符号,因此  $\Delta f$  可取不同符号的值,所以  $f(x_{0},y_{0})$  不是极值.

再证 $f_{xx}(x_0,y_0)$ 和 $f_{yy}(x_0,y_0)$ 不同时为零的情形.不妨假定 $f_{xx}(x_0,y_0)\neq 0.$ 先取 $k = 0$ ，于是由(9-5)式得

$$
\Delta f = \frac {1}{2} h ^ {2} f _ {x x} (x _ {0} + \theta h, y _ {0}).
$$

由此看出, 当 h 充分接近零时,  $\Delta f$  与  $f_{xx}(x_{0}, y_{0})$  同号.

但如果取

$$
h = - f _ {x y} (x _ {0}, y _ {0}) s, \quad k = f _ {x x} (x _ {0}, y _ {0}) s, \tag {9-9}
$$

其中 $s$ 是异于零但充分接近零的数, 则可发现, 当 $|s|$ 充分小时, $\Delta f$ 与 $f_{xx}(x_0, y_0)$ 异号. 事实上, 在(9-5)式中将 $h$ 及 $k$ 用(9-9)式给定的值代入, 得

$$
\Delta f = \frac {1}{2} s ^ {2} \left\{\left[ f _ {x y} (x _ {0}, y _ {0}) \right] ^ {2} f _ {x x} (x _ {0} + \theta h, y _ {0} + \theta k) - 2 f _ {x y} (x _ {0}, y _ {0}) f _ {x x} (x _ {0}, y _ {0}) f _ {x y} (x _ {0} + \theta h, y _ {0} + \theta k) + \right.
$$

$$
\left[ f _ {x x} (x _ {0}, y _ {0}) \right] ^ {2} f _ {y y} (x _ {0} + \theta h, y _ {0} + \theta k) \}. \tag {9-10}
$$

上式右端花括号内的式子当 $s \to 0$ 时趋于极限

$$
f _ {x x} (x _ {0}, y _ {0}) \left\{f _ {x x} (x _ {0}, y _ {0}) f _ {y y} (x _ {0}, y _ {0}) - [ f _ {x y} (x _ {0}, y _ {0}) ] ^ {2} \right\}.
$$

由不等式(9-8)，上式花括号内的值为负，因此当 $s$ 充分接近零时，(9-10)式右端（从而 $\Delta f$ ）与 $f_{xx}(x_0,y_0)$ 异号.

以上已经证得:在点 $(x_{0},y_{0})$ 的任意邻近, $\Delta f$ 可取不同符号的值,因此 $f(x_{0},y_{0})$ 不是极值.

122

---

\* 第十节 最小二乘法

## (3) 考察函数

$$
f (x, y) = x ^ {2} + y ^ {4} \quad {\text {及}} \quad g (x, y) = x ^ {2} + y ^ {3}.
$$

容易验证, 这两个函数都以  $(0,0)$  为驻点, 且在点  $(0,0)$  处都满足  $AC-B^{2}=0$ . 但  $f(x,y)$  在点  $(0,0)$  处有极小值, 而  $g(x,y)$  在点  $(0,0)$  处却没有极值.

## \*习题9-9

1. 求函数 $f(x, y) = 2x^{2} - xy - y^{2} - 6x - 3y + 5$ 在点(1, -2)的泰勒公式.
2. 求函数  $f(x,y)=\mathrm{e}^{x}\ln(1+y)$  在点  $(0,0)$  的三阶泰勒公式.
3. 求函数 $f(x, y) = \sin x \sin y$ 在点 $\left(\frac{\pi}{4}, \frac{\pi}{4}\right)$ 的二阶泰勒公式.
4. 利用函数 $f(x, y) = x^y$ 的三阶泰勒公式，计算 1.1^{1.02} 的近似值.
5. 求函数 $f(x, y) = \mathrm{e}^{x + y}$ 在点(0,0)的 $n$ 阶泰勒公式.

## \* 第十节 最小二乘法

许多工程问题,常常需要根据两个变量的几组实验数值——实验数据,来找出这两个变量间的函数关系的近似表达式.通常把这样得到的函数的近似表达式叫做经验公式.经验公式建立以后,就可以把生产或实验中所积累的某些经验,提高到理论上加以分析.下面通过举例介绍常用的一种建立经验公式的方法.

例 1 为了测定刀具的磨损速度,我们做这样的实验:经过一定时间(如每隔1 h),测量一次刀具的厚度,得到一组实验数据如下:

| 顺序编号i | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 时间ti/h | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 |
| 刀具厚度yi/mm | 27.0 | 26.8 | 26.5 | 26.3 | 26.1 | 25.7 | 25.3 | 24.8 |

试根据上面的实验数据建立 y 和 t 之间的经验公式  $y=f(t)$ . 也就是, 要找出一个能使上述数据大体适合的函数关系  $y=f(t)$ .

解 首先,要确定 $f(t)$ 的类型.为此,可按下面的方法处理.在直角坐标系中取t为横坐标,y为纵坐标,描出上述各对数据的对应点,如图9-12所示.从图上可以看出,这些点的连线大致接近于一条直线.于是,就可以认为 $y=f(t)$ 是线性函数,并设

$$
f (t) = a t + b,
$$

其中 a 和 b 是待定常数.

123

---

第九章 多元函数微分法及其应用

常数 a 和 b 如何确定呢？最理想的情形是选取这样的 a 和 b，能使直线  $y = at + b$  经过图 9-12 中所标出的各点。但在实际上这是不可能的。因为这些点本来就不在同一条直线上。因此，只能要求选取这样的 a, b，使得  $f(t) = at + b$  在  $t_{0}, t_{1}, t_{2}, \cdots, t_{7}$  处的函数值与实验数据  $y_{0}, y_{1}, y_{2}, \cdots, y_{7}$  相差都很小，就是要使偏差

$$
y _ {i} - f (t _ {i}) \quad (i = 0, 1, 2, \dots , 7)
$$

都很小.那么如何达到这一要求呢？能否设法使偏差的和

![](../../raw/pages_0129-0160/images/page_130_chart_4.jpg)

<details>
<summary>scatter</summary>

| t | y |
| --- | --- |
| 0 | 27 |
| 1 | ~26.8 |
| 2 | ~26.5 |
| 3 | ~26.3 |
| 4 | ~26.1 |
| 5 | ~25.7 |
| 6 | ~25.3 |
| 7 | ~24.8 |
</details>

图9-12

$$
\sum_ {i = 0} ^ {7} [ y _ {i} - f (t _ {i}) ]
$$

很小来保证每个偏差都很小呢？不能，因为偏差有正有负，在求和时，可能互相抵消.为了避免这种情形，可对偏差取绝对值再求和，只要

$$
\sum_ {i = 0} ^ {7} \mid y _ {i} - f (t _ {i}) \mid = \sum_ {i = 0} ^ {7} \mid y _ {i} - (a t _ {i} + b) \mid
$$

很小, 就可以保证每个偏差的绝对值都很小. 但是这个式子中有绝对值符号, 不便于进一步分析讨论. 由于任何实数的平方都是正数或零, 因此可以考虑选取常数 a 与 b, 使

$$
M = \sum_ {i = 0} ^ {7} \left[ y _ {i} - (a t _ {i} + b) \right] ^ {2}
$$

最小来保证每个偏差的绝对值都很小.这种根据偏差的平方和为最小的条件来选择常数 $a$ 与 $b$ 的方法叫做最小二乘法.这种确定常数 $a$ 与 $b$ 的方法是通常所采用的.

现在我们来研究,经验公式  $y=at+b$  中,a 和 b 符合什么条件时,可以使上述的 M 为最小.如果把 M 看成与自变量 a 和 b 相对应的因变量,那么问题就可归结为求函数  $M=M(a,b)$  在哪些点处取得最小值.由第八节中的讨论可知,上述问题可以通过求方程组

$$
\left\{ \begin{array}{l} M _ {a} (a, b) = 0, \\ M _ {b} (a, b) = 0 \end{array} \right.
$$

的解来解决,即令

$$
\left\{ \begin{array}{l} \frac {\partial M}{\partial a} = - 2 \sum_ {i = 0} ^ {7} [ y _ {i} - (a t _ {i} + b) ] t _ {i} = 0, \\ \frac {\partial M}{\partial b} = - 2 \sum_ {i = 0} ^ {7} [ y _ {i} - (a t _ {i} + b) ] = 0, \end{array} \right.
$$

亦即

124

---

\* 第十节 最小二乘法

$$
\left\{ \begin{array}{l} \sum_ {i = 0} ^ {7} t _ {i} \left[ y _ {i} - (a t _ {i} + b) \right] = 0, \\ \sum_ {i = 0} ^ {7} \left[ y _ {i} - (a t _ {i} + b) \right] = 0. \end{array} \right.
$$

将括号内各项进行整理合并,并把未知数 a 和 b 分离出来,便得

$$
\left\{ \begin{array}{l} a \sum_ {i = 0} ^ {7} t _ {i} ^ {2} + b \sum_ {i = 0} ^ {7} t _ {i} = \sum_ {i = 0} ^ {7} y _ {i} t _ {i}, \\ a \sum_ {i = 0} ^ {7} t _ {i} + 8 b = \sum_ {i = 0} ^ {7} y _ {i}. \end{array} \right. \tag {10-1}
$$

下面通过列表来计算 $\sum_{i=0}^{7} t_i$, $\sum_{i=0}^{7} t_i^2$, $\sum_{i=0}^{7} y_i$ 及 $\sum_{i=0}^{7} y_i t_i$.

<table><tr><td></td><td> $t_i$ </td><td> $t_i^2$ </td><td> $y_i$ </td><td> $y_it_i$ </td></tr><tr><td rowspan="8"></td><td>0</td><td>0</td><td>27.0</td><td>0</td></tr><tr><td>1</td><td>1</td><td>26.8</td><td>26.8</td></tr><tr><td>2</td><td>4</td><td>26.5</td><td>53.0</td></tr><tr><td>3</td><td>9</td><td>26.3</td><td>78.9</td></tr><tr><td>4</td><td>16</td><td>26.1</td><td>104.4</td></tr><tr><td>5</td><td>25</td><td>25.7</td><td>128.5</td></tr><tr><td>6</td><td>36</td><td>25.3</td><td>151.8</td></tr><tr><td>7</td><td>49</td><td>24.8</td><td>173.6</td></tr><tr><td>合计</td><td>28</td><td>140</td><td>208.5</td><td>717.0</td></tr></table>

代入方程组(10-1)，得到

$$
\left\{ \begin{array}{l} 1 4 0 a + 2 8 b = 7 1 7, \\ 2 8 a + 8 b = 2 0 8. 5. \end{array} \right.
$$

解此方程组,得到 a=-0.3036, b=27.125. 这样便得到所求经验公式为

$$
y = f (t) = - 0. 3 0 3 6 t + 2 7. 1 2 5. \tag {10-2}
$$

由(10-2)式算出的函数值 $f(t_{i})$ 与实测的 $y_{i}$ 有一定的偏差.现列表比较如下:

| ti/h | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 实测的yi/mm | 27.0 | 26.8 | 26.5 | 26.3 | 26.1 | 25.7 | 25.3 | 24.8 |
| 算得的f(ti)/mm | 27.125 | 26.821 | 26.518 | 26.214 | 25.911 | 25.607 | 25.303 | 25.000 |
| 偏差/mm | -0.125 | -0.021 | -0.018 | 0.086 | 0.189 | 0.093 | -0.003 | -0.200 |

偏差的平方和 M=0.108165，它的算术平方根  $\sqrt{M}=0.329\sqrt{M}$  称为均方误差，它的大小在一定程度上反映了用经验公式来近似表达原来函数关系的近似程度的好坏。

125

---

第九章 多元函数微分法及其应用

在例 1 中, 按实验数据描出的图形接近于一条直线. 在这种情形下, 就可认为函数关系是线性函数类型的, 从而问题可化为求解一个二元一次方程组, 计算比较方便. 还有一些实际问题, 经验公式的类型不是线性函数, 但可以设法把它化成线性函数的类型来讨论. 举例说明于下:

例 2 在研究某单分子化学反应速度时,得到下列数据:

| i | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| $\tau_{i}$ | 3 | 6 | 9 | 12 | 15 | 18 | 21 | 24 |
| $y_{i}$ | 57.6 | 41.9 | 31.0 | 22.7 | 16.6 | 12.2 | 8.9 | 6.5 |

其中  $\tau$  表示从实验开始算起的时间, y 表示时刻  $\tau$  反应物的量. 试根据上述数据定出经验公式  $y = f(\tau)$ .

解 由化学反应速度的理论知道, $y=f(\tau)$ 应是指数函数 $y=ke^{m\tau}$, 其中 k 和 m 是待定常数. 对这批数据, 先来验证这个结论. 为此, 在 $y=ke^{m\tau}$ 的两端取常用对数, 得

$$
\lg y = (m \lg e) \tau + \lg k.
$$

记 $m\lg e$ 即0.434 $3m = a,\lg k = b$ ，则上式可写为

$$
\lg y = a \tau + b,
$$

于是  $\lg y$  就是  $\tau$  的线性函数. 所以, 把表中各对数据  $(\tau_{i}, y_{i}) (i = 1, 2, \cdots, 8)$  所对应的点描在半对数坐标系上 (半对数坐标系的横轴上各点处所标明的数字与普通的直角坐标系相同, 而纵轴上各点处所标明的数字是这样的, 它的常用对数就是该点到原点的距离), 如图 9-13 所示. 从图上看出, 这些点的连线非常接近于一条直线, 这说明  $y = f(\tau)$  确实可以认为是指数函数.

下面来具体定出 $k$ 与 $m$ 的值.由于

$$
\lg y = a \tau + b,
$$

![](../../raw/pages_0129-0160/images/page_132_chart_12.jpg)

<details>
<summary>line</summary>

| t | y |
| --- | --- |
| ~3 | 60 |
| ~6 | 42 |
| ~9 | 32 |
| ~12 | 21 |
| ~15 | 13 |
| ~18 | 11 |
| ~21 | 8.5 |
| ~24 | 6 |
</details>

图9-13

所以可仿照例 1 中的讨论,通过求方程组

$$
\left\{ \begin{array}{l} a \sum_ {i = 1} ^ {8} \tau_ {i} ^ {2} + b \sum_ {i = 1} ^ {8} \tau_ {i} = \sum_ {i = 1} ^ {8} \tau_ {i} \lg y _ {i}, \\ a \sum_ {i = 1} ^ {8} \tau_ {i} + 8 b = \sum_ {i = 1} ^ {8} \lg y _ {i} \end{array} \right. \tag {10-3}
$$

的解, 把 a 与 b 确定出来.

下面通过列表来计算  $\sum_{i=1}^{8}\tau_{i},\quad\sum_{i=1}^{8}\tau_{i}^{2},\quad\sum_{i=1}^{8}\lg y_{i}$  及  $\sum_{i=1}^{8}\tau_{i}\lg y_{i}.$

126

---

总习题九

<table><tr><td></td><td> $\tau_{i}$ </td><td> $\tau_{i}^{2}$ </td><td> $y_{i}$ </td><td> $\lg y_{i}$ </td><td> $\tau_{i}\lg y_{i}$ </td></tr><tr><td rowspan="8"></td><td>3</td><td>9</td><td>57.6</td><td>1.7604</td><td>5.2812</td></tr><tr><td>6</td><td>36</td><td>41.9</td><td>1.6222</td><td>9.7332</td></tr><tr><td>9</td><td>81</td><td>31.0</td><td>1.4914</td><td>13.4226</td></tr><tr><td>12</td><td>144</td><td>22.7</td><td>1.3560</td><td>16.2720</td></tr><tr><td>15</td><td>225</td><td>16.6</td><td>1.2201</td><td>18.3015</td></tr><tr><td>18</td><td>324</td><td>12.2</td><td>1.0864</td><td>19.5552</td></tr><tr><td>21</td><td>441</td><td>8.9</td><td>0.9494</td><td>19.9374</td></tr><tr><td>24</td><td>576</td><td>6.5</td><td>0.8129</td><td>19.5096</td></tr><tr><td>合计</td><td>108</td><td>1836</td><td></td><td>10.2988</td><td>122.0127</td></tr></table>

将它们代入方程组(10-3) $\left(\text{其中取}\sum_{i=1}^{8}\lg y_{i}=10.3,\sum_{i=1}^{8}\tau_{i}\lg y_{i}=122\right)$ ，得

$$
\left\{ \begin{array}{l} 1 8 3 6 a + 1 0 8 b = 1 2 2, \\ 1 0 8 a + 8 b = 1 0. 3. \end{array} \right.
$$

解这个方程组,得

$$
\left\{ \begin{array}{l} a = 0. 4 3 4 3 m = - 0. 0 4 5, \\ b = \lg k = 1. 8 9 6 4, \end{array} \right.
$$

所以

$$
m = - 0. 1 0 3 6, \quad k = 7 8. 7 8.
$$

因此所求的经验公式为

$$
y = 7 8. 7 8 \mathrm{e} ^ {- 0. 1 0 3 6 \tau}.
$$

## \*习题9-10

1. 某种合金的含铅量百分比(%)为p,其熔解温度(℃)为 $\theta$ ,由实验测得p与 $\theta$ 的数据如下表:

| p/% | 36.9 | 46.7 | 63.7 | 77.8 | 84.0 | 87.5 |
| --- | --- | --- | --- | --- | --- | --- |
| θ/°C | 181 | 197 | 235 | 270 | 283 | 292 |

试用最小二乘法建立  $\theta$  与 p 之间的经验公式  $\theta = ap + b$ .

2. 已知一组实验数据为 $(x_{1},y_{1}),(x_{2},y_{2}),\cdots,(x_{n},y_{n})$ . 现若假定经验公式是

$$
y = a x ^ {2} + b x + c.
$$

试按最小二乘法建立 a, b, c 应满足的三元一次方程组.

## 总习题九

1. 在“充分”“必要”和“充分必要”三者中选择一个正确的填入下列空格内:

127

---

第九章 多元函数微分法及其应用

(1) $f(x,y)$ 在点 $(x,y)$ 可微分是 $f(x,y)$ 在该点连续的\_\_\_\_条件, $f(x,y)$ 在点 $(x,y)$ 连续是 $f(x,y)$ 在该点可微分的\_\_\_\_条件;

(2) $z = f(x, y)$ 在点 $(x, y)$ 的偏导数 $\frac{\partial z}{\partial x}$ 及 $\frac{\partial z}{\partial y}$ 存在是 $f(x, y)$ 在该点可微分的 \_\_\_\_ 条件, $z = f(x, y)$ 在点 $(x, y)$ 可微分是函数在该点的偏导数 $\frac{\partial z}{\partial x}$ 及 $\frac{\partial z}{\partial y}$ 存在的 \_\_\_\_ 条件;

(3) $z = f(x, y)$ 的偏导数 $\frac{\partial z}{\partial x}$ 及 $\frac{\partial z}{\partial y}$ 在点 $(x, y)$ 存在且连续是 $f(x, y)$ 在该点可微分的 \_\_\_\_ 条件；

（4）函数 $z = f(x,y)$ 的两个二阶混合偏导数 $\frac{\partial^2z}{\partial x\partial y}$ 及 $\frac{\partial^2z}{\partial y\partial x}$ 在区域 $D$ 内连续是这两个二阶混合偏导数在 $D$ 内相等的 \_\_\_\_ 条件.

2. 下题中给出了四个结论,从中选出一个正确的结论:

设函数 $f(x,y)$ 在点 $(0,0)$ 的某邻域内有定义，且 $f_{x}(0,0) = 3,f_{y}(0,0) = -1$ ，则有（ ）.

(A)  $dz \mid_{(0,0)} = 3dx - dy$
(B) 曲面  $z=f(x,y)$  在点  $(0,0,f(0,0))$  的一个法向量为  $(3,-1,1)$
(C) 曲线  $\left\{\begin{aligned}z=f(x,y),\\ y=0\end{aligned}\right.$  在点  $(0,0,f(0,0))$  的一个切向量为  $(1,0,3)$
(D) 曲线  $\left\{\begin{aligned}z=f(x,y),\\ y=0\end{aligned}\right.$  在点  $(0,0,f(0,0))$  的一个切向量为  $(3,0,1)$

3. 求函数 $f(x, y) = \frac{\sqrt{4x - y^2}}{\ln(1 - x^2 - y^2)}$ 的定义域，并求 $\lim_{(x, y) \to \left(\frac{1}{2}, 0\right)} f(x, y)$.

\* 4. 证明极限 $\lim_{(x,y)\to (0,0)}\frac{xy^2}{x^2 + y^4}$ 不存在.

5. 设 $f(x,y)=\left\{\begin{aligned}\frac{x^{2}y}{x^{2}+y^{2}},&x^{2}+y^{2}\neq0,\\ 0,&x^{2}+y^{2}=0.\end{aligned}\right.$ 求 $f_{x}(x,y)$ 及 $f_{y}(x,y)$.
6. 求下列函数的一阶和二阶偏导数:

(1) $z = \ln (x + y^2)$;

(2) $z = x^{y}$.

7. 求函数 $z = \frac{xy}{x^2 - y^2}$ 当 $x = 2, y = 1, \Delta x = 0.01, \Delta y = 0.03$ 时的全增量和全微分.

\*8. 设 $f(x, y) = \begin{cases} \frac{x^2y^2}{(x^2 + y^2)^{3/2}}, & x^2 + y^2 \neq 0, \\ 0, & x^2 + y^2 = 0. \end{cases}$ 证明:$f(x, y)$ 在点(0,0)处连续且偏导数存在，但不可微分.
9. 设 $u = x^{\gamma}$, 而 $x = \varphi(t)$, $y = \psi(t)$ 都是可微函数, 求 $\frac{\mathrm{d}u}{\mathrm{d}t}$.
10. 设  $z=f(u,v,w)$  具有连续偏导数, 而

128

---

总习题九

$$
u = \eta - \zeta , \quad v = \zeta - \xi , \quad w = \xi - \eta ,
$$

求 $\frac{\partial z}{\partial\xi},\frac{\partial z}{\partial\eta},\frac{\partial z}{\partial\zeta}.$

11. 设 $z = f(u, x, y), u = x\mathrm{e}^y$，其中 $f$ 具有连续的二阶偏导数，求 $\frac{\partial^2 z}{\partial x \partial y}$.

12. 设 $x = \mathrm{e}^{u}\cos v, y = \mathrm{e}^{u}\sin v, z = uv$. 试求 $\frac{\partial z}{\partial x}$ 和 $\frac{\partial z}{\partial y}$.

13. 求螺旋线  $x = a \cos \theta, y = a \sin \theta, z = b \theta$  在点  $(a, 0, 0)$  处的切线及法平面方程.

14. 在曲面 z=xy 上求一点, 使这点处的法线垂直于平面  $x+3y+z+9=0$ , 并写出该法线的方程.

15. 设 $e_l = (\cos \theta, \sin \theta)$, 求函数

$$
f (x, y) = x ^ {2} - x y + y ^ {2}
$$

在点(1,1)沿方向 $l$ 的方向导数，并分别确定角 $\theta$ ，使这个方向导数

(1)有最大值;(2)有最小值;(3)等于0.

16. 求函数 $u = x^{2} + y^{2} + z^{2}$ 在椭球面 $\frac{x^2}{a^2} + \frac{y^2}{b^2} + \frac{z^2}{c^2} = 1$ 上点 $M_0(x_0, y_0, z_0)$ 处沿外法线方向的方向导数.

17. 求平面 $\frac{x}{3} + \frac{y}{4} + \frac{z}{5} = 1$ 和柱面 $x^{2} + y^{2} = 1$ 的交线上与 $xOy$ 面距离最短的点.

18. 在第 I 卦限内作椭球面  $\frac{x^{2}}{a^{2}} + \frac{y^{2}}{b^{2}} + \frac{z^{2}}{c^{2}} = 1$  的切平面, 使该切平面与三坐标面所围成的四面体的体积最小. 求这切平面的切点, 并求此最小体积.

19. 某厂家生产的一种产品同时在两个市场销售, 售价分别为  $p_{1}$  和  $p_{2}$ , 销售量分别为  $q_{1}$  和  $q_{2}$ , 需求函数分别为

$$
q _ {1} = 2 4 - 0. 2 p _ {1}, \quad q _ {2} = 1 0 - 0. 0 5 p _ {2},
$$

总成本函数为

$$
C = 3 5 + 4 0 (q _ {1} + q _ {2}).
$$

试问:厂家如何确定两个市场的售价,能使其获得的总利润最大,最大总利润为多少?

20. 设有一小山, 取它的底面所在的平面为 $xOy$ 坐标面, 其底部所占的闭区域为 $D = \{(x, y) \mid x^2 + y^2 - xy \leqslant 75\}$, 小山的高度函数为 $h = f(x, y) = 75 - x^2 - y^2 + xy$.

（1）设 $M(x_0,y_0)\in D$ ，问 $f(x,y)$ 在该点沿平面上什么方向的方向导数最大，若记此方向导数的最大值为 $g(x_0,y_0)$ ，试写出 $g(x_0,y_0)$ 的表达式；
（2）现欲利用此小山开展攀岩活动，为此需要在山脚找一上山坡度最大的点作为攀岩的起点。也就是说，要在 $D$ 的边界线 $x^{2} + y^{2} - xy = 75$ 上找出(1)中的 $g(x,y)$ 达到最大值的点。试确定攀岩起点的位置。

第九章释疑解难

The image provided is a QR code. It does not contain any text, mathematical formulas, tables, or figures that can be processed according to the given instructions. Therefore, no OCR output can be generated from this image.

第九章例题精讲

The image provided is a QR code. It does not contain any text, mathematical formulas, tables, or figures that can be processed according to the given instructions. Therefore, no OCR output can be generated from this image.

129
