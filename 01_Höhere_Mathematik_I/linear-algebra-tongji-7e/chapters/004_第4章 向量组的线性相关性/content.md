# 第4章 向量组的线性相关性

原始 PDF 第 86–117 页。

The quick brown fox jumps over the lazy dog.

# 第4章

# 向量组的线性相关性

![](../../raw/pages_0065-0096/images/page_85_image_3.jpg)

向量组的线性相关性是线性代数的一个核心概念,本章将介绍向量组的线性相关性、向量组的秩及其应用.

## § 1 向量组及其线性组合

在解析几何中,我们把“既有大小又有方向的量”叫做向量,并把可随意平行移动的有向线段作为向量的几何形象.在引进坐标系以后,这种向量就有了坐标表达式——三个有次序的实数.代数中将三个有次序的实数定义为3维向量,现在将3维向量进行推广.

第 2 章中我们已经介绍过向量的概念,现再叙述如下:

定义 1 n 个有次序的数  $a_{1}, a_{2}, \cdots, a_{n}$  所组成的数组称为 n 维向量，这 n 个数称为该向量的 n 个分量，第 i 个数  $a_{i}$  称为第 i 个分量.

分量全为实数的向量称为实向量, 分量中有复数的向量称为复向量. 本书中除特别指明外, 一般只讨论实向量.

$n$ 维向量可写成一行, 也可写成一列. 按第2章中的规定, 分别称为行向量和列向量, 也就是行矩阵和列矩阵, 并规定行向量与列向量都按矩阵的运算规则进行运算. 因此, $n$ 维列向量

$$
\boldsymbol {a} = \left( \begin{array}{c} \boldsymbol {a} _ {1} \\ \boldsymbol {a} _ {2} \\ \vdots \\ \boldsymbol {a} _ {n} \end{array} \right)
$$

与 $n$ 维行向量

82

---

§1 向量组及其线性组合

$$
\boldsymbol {a} ^ {\mathrm{T}} = (a _ {1}, a _ {2}, \dots , a _ {n})
$$

总看作两个不同的向量.

本书中,列向量用黑体小写字母 $a, b, \alpha, \beta$ 等表示,行向量则用 $a^{\mathrm{T}}, b^{\mathrm{T}}, \alpha^{\mathrm{T}}, \beta^{\mathrm{T}}$ 等表示.所讨论的向量在没有指明是行向量还是列向量时,都当作列向量.

当 $n \leqslant 3$ 时, $n$ 维向量可以把有向线段作为几何形象, 但当 $n > 3$ 时, $n$ 维向量就不再有这种几何形象, 只是沿用一些几何术语罢了.

几何中，“空间”通常是作为点的集合，即构成“空间”的元素是点，这样的空间叫做点空间。我们把3维向量的全体所组成的集合

$$
\mathbb {R} ^ {3} = \{\boldsymbol {r} \mid \boldsymbol {r} = (x, y, z) ^ {\mathrm{T}}, x, y, z \in \mathbb {R} \}
$$

叫做 3 维向量空间. 在点空间取定坐标系以后, 空间中的点 $P(x, y, z)$ 与 3 维向量 $r = (x, y, z)^{\mathrm{T}}$ 之间有一一对应的关系, 因此, 向量空间可以类比为取定了坐标系的点空间. 在讨论向量的运算时, 我们把向量看作有向线段; 在讨论向量集时, 则把向量 $r$ 看作以 $r$ 为向径的点 $P$, 从而把点 $P$ 的轨迹作为向量集的图形. 例如点集

$$
\Pi = \{P (x, y, z) \mid a x + b y + c z = d \}
$$

是一个平面 $(a, b, c$ 不全为0)，于是向量集

$$
\{\boldsymbol {r} \mid \boldsymbol {r} = (x, y, z) ^ {\mathrm{T}}, a x + b y + c z = d \}
$$

也叫做向量空间  $R^{3}$  中的平面, 并把  $\Pi$  作为它的图形.

类似地， $n$ 维向量的全体所组成的集合记为

$$
\mathbb {R} ^ {n} = \left\{\boldsymbol {x} \mid \boldsymbol {x} = (x _ {1}, x _ {2}, \dots , x _ {n}) ^ {\mathrm{T}}, x _ {1}, x _ {2}, \dots , x _ {n} \in \mathbb {R} \right\}.
$$

若干个同维数的列向量(或同维数的行向量)所组成的集合叫做向量组.例如一个 $m \times n$ 矩阵的全体列向量是一个含n个m维列向量的向量组,它的全体行向量是一个含m个n维行向量的向量组.

下面我们先讨论只含有限个向量的向量组.

矩阵的列向量组和行向量组都是只含有限个向量的向量组；反之，一个含有限个向量的向量组总可以构成一个矩阵。例如:

m 个 n 维列向量所组成的向量组  $A: a_{1}, a_{2}, \cdots, a_{m}$  构成一个  $n \times m$  矩阵

$$
A = (a _ {1}, a _ {2}, \dots , a _ {m});
$$

m 个 n 维行向量所组成的向量组  $B: \beta_{1}^{T}, \beta_{2}^{T}, \cdots, \beta_{m}^{T}$ ，构成一个  $m \times n$  矩阵

$$
\boldsymbol {B} = \left( \begin{array}{c} \boldsymbol {\beta} _ {1} ^ {\mathrm{T}} \\ \boldsymbol {\beta} _ {2} ^ {\mathrm{T}}, \\ \vdots \\ \boldsymbol {\beta} _ {m} ^ {\mathrm{T}} \end{array} \right).
$$

总之，含有限个向量的有序向量组可以与矩阵一一对应.

83

---

第4章 向量组的线性相关性

定义 2 给定向量组  $A: a_{1}, a_{2}, \cdots, a_{m}$ ，对于任何一组实数  $k_{1}, k_{2}, \cdots, k_{m}$ ，表达式

$$
k _ {1} \boldsymbol {a} _ {1} + k _ {2} \boldsymbol {a} _ {2} + \dots + k _ {m} \boldsymbol {a} _ {m}
$$

称为向量组 A 的一个线性组合, $k_{1}, k_{2}, \cdots, k_{m}$ 称为这个线性组合的系数.

给定向量组  $A:a_{1},a_{2},\cdots,a_{m}$  和向量 b，若存在一组数  $\lambda_{1},\lambda_{2},\cdots,\lambda_{m}$ ，使

$$
\boldsymbol {b} = \lambda_ {1} \boldsymbol {a} _ {1} + \lambda_ {2} \boldsymbol {a} _ {2} + \dots + \lambda_ {m} \boldsymbol {a} _ {m},
$$

则向量 b 是向量组 A 的线性组合, 这时称向量 b 能由向量组 A 线性表示.

向量 b 能由向量组 A 线性表示,也就是方程组

$$
x _ {1} \boldsymbol {a} _ {1} + x _ {2} \boldsymbol {a} _ {2} + \dots + x _ {m} \boldsymbol {a} _ {m} = \boldsymbol {b}
$$

有解.由上章定理5,立即可得

定理 1 向量 b 能由向量组  $A: a_{1}, a_{2}, \cdots, a_{m}$  线性表示的充分必要条件是矩阵  $A = (a_{1}, a_{2}, \cdots, a_{m})$  的秩等于矩阵  $B = (a_{1}, a_{2}, \cdots, a_{m}, b)$  的秩.

定义3 设有两个向量组 $A: a_{1}, a_{2}, \cdots, a_{m}$ 及 $B: b_{1}, b_{2}, \cdots, b_{l}$, 若向量组 $B$ 中的每个向量都能由向量组 $A$ 线性表示, 则称向量组 $B$ 能由向量组 $A$ 线性表示. 若向量组 $A$ 与向量组 $B$ 能相互线性表示, 则称这两个向量组等价.

把向量组 A 和 B 所构成的矩阵依次记作  $\boldsymbol{A} = (\boldsymbol{a}_{1}, \boldsymbol{a}_{2}, \cdots, \boldsymbol{a}_{m})$  和  $\boldsymbol{B} = (\boldsymbol{b}_{1}, \boldsymbol{b}_{2}, \cdots, \boldsymbol{b}_{l})$ ，向量组 B 能由向量组 A 线性表示，即对每个向量  $b_{j} (j=1,2,\cdots,l)$ ，存在数  $k_{1j}, k_{2j}, \cdots, k_{mj}$ ，使

$$
\boldsymbol {b} _ {j} = k _ {1 j} \boldsymbol {a} _ {1} + k _ {2 j} \boldsymbol {a} _ {2} + \dots + k _ {m j} \boldsymbol {a} _ {m} = (\boldsymbol {a} _ {1}, \boldsymbol {a} _ {2}, \dots , \boldsymbol {a} _ {m}) \left( \begin{array}{c} k _ {1 j} \\ k _ {2 j} \\ \vdots \\ k _ {m j} \end{array} \right),
$$

从而

$$
(\boldsymbol {b} _ {1}, \boldsymbol {b} _ {2}, \dots , \boldsymbol {b} _ {l}) = (\boldsymbol {a} _ {1}, \boldsymbol {a} _ {2}, \dots , \boldsymbol {a} _ {m}) \left( \begin{array}{c c c c} k _ {1 1} & k _ {1 2} & \dots & k _ {1 l} \\ k _ {2 1} & k _ {2 2} & \dots & k _ {2 l} \\ \vdots & \vdots & & \vdots \\ k _ {m 1} & k _ {m 2} & \dots & k _ {m l} \end{array} \right),
$$

这里,矩阵 $K_{m\times l}=(k_{ij})$ 称为这一线性表示的系数矩阵.

由此可知, 若  $C_{m \times n} = A_{m \times l} B_{l \times n}$ , 则矩阵 C 的列向量组能由矩阵 A 的列向量组线性表示, B 为这一表示的系数矩阵

$$
(\boldsymbol {c} _ {1}, \boldsymbol {c} _ {2}, \dots , \boldsymbol {c} _ {n}) = (\boldsymbol {a} _ {1}, \boldsymbol {a} _ {2}, \dots , \boldsymbol {a} _ {l}) \left( \begin{array}{c c c c} b _ {1 1} & b _ {1 2} & \dots & b _ {1 n} \\ b _ {2 1} & b _ {2 2} & \dots & b _ {2 n} \\ \vdots & \vdots & & \vdots \\ b _ {l 1} & b _ {l 2} & \dots & b _ {l n} \end{array} \right);
$$

84

---

§1 向量组及其线性组合

同时， $C$ 的行向量组能由 $\pmb{B}$ 的行向量组线性表示， $\pmb{A}$ 为这一表示的系数矩阵

$$
\left( \begin{array}{c} \boldsymbol {\gamma} _ {1} ^ {\mathrm{T}} \\ \boldsymbol {\gamma} _ {2} ^ {\mathrm{T}} \\ \vdots \\ \boldsymbol {\gamma} _ {m} ^ {\mathrm{T}} \end{array} \right) = \left( \begin{array}{c c c c} a _ {1 1} & a _ {1 2} & \dots & a _ {1 l} \\ a _ {2 1} & a _ {2 2} & \dots & a _ {2 l} \\ \vdots & \vdots & & \vdots \\ a _ {m 1} & a _ {m 2} & \dots & a _ {m l} \end{array} \right) \left( \begin{array}{c} \boldsymbol {\beta} _ {1} ^ {\mathrm{T}} \\ \boldsymbol {\beta} _ {2} ^ {\mathrm{T}} \\ \vdots \\ \boldsymbol {\beta} _ {l} ^ {\mathrm{T}} \end{array} \right).
$$

设矩阵 $A$ 与 $\pmb{B}$ 行等价, 即矩阵 $A$ 经初等行变换变成矩阵 $\pmb{B}$, 则 $\pmb{B}$ 的每个行向量都是 $A$ 的行向量组的线性组合, 即 $\pmb{B}$ 的行向量组能由 $A$ 的行向量组线性表示. 由于初等变换可逆, 知矩阵 $\pmb{B}$ 亦可经初等行变换变为 $A$, 从而 $A$ 的行向量组也能由 $\pmb{B}$ 的行向量组线性表示. 于是 $A$ 的行向量组与 $\pmb{B}$ 的行向量组等价.

类似可知,若矩阵 A 与 B 列等价,则 A 的列向量组与 B 的列向量组等价.

按定义3, 向量组 $B: b_{1}, b_{2}, \cdots, b_{l}$ 能由向量组 $A: a_{1}, a_{2}, \cdots, a_{m}$ 线性表示, 其含义是存在矩阵 $K_{m \times l}$, 使 $(b_{1}, b_{2}, \cdots, b_{l}) = (a_{1}, a_{2}, \cdots, a_{m}) K$, 也就是矩阵方程

$$
(a _ {1}, a _ {2}, \dots , a _ {m}) X = (b _ {1}, b _ {2}, \dots , b _ {l})
$$

有解.由上章定理6,立即可得

定理 2 向量组  $B:b_{1},b_{2},\cdots,b_{l}$  能由向量组  $A:a_{1},a_{2},\cdots,a_{m}$  线性表示的充分必要条件是矩阵  $A=(a_{1},a_{2},\cdots,a_{m})$  的秩等于矩阵  $(A,B)=(a_{1},a_{2},\cdots,a_{m},b_{1},b_{2},\cdots,b_{l})$  的秩，即  $R(A)=R(A,B)$ .

推论 向量组  $A:a_{1},a_{2},\cdots,a_{m}$  与向量组  $B:b_{1},b_{2},\cdots,b_{l}$  等价的充分必要条件是

$$
R (\boldsymbol {A}) = R (\boldsymbol {B}) = R (\boldsymbol {A}, \boldsymbol {B}),
$$

其中 A 和 B 是向量组 A 和 B 所构成的矩阵.

证 因向量组 $A$ 与向量组 $B$ 能相互线性表示, 依据定理2, 知它们等价的充分必要条件是

$$
R (\boldsymbol {A}) = R (\boldsymbol {A}, \boldsymbol {B}) \quad \text {且} \quad R (\boldsymbol {B}) = R (\boldsymbol {B}, \boldsymbol {A}),
$$

而 $R(A,B) = R(B,A)$，合起来即得充分必要条件为

$$
R (\boldsymbol {A}) = R (\boldsymbol {B}) = R (\boldsymbol {A}, \boldsymbol {B}).
$$

证毕

例1 设

$$
\boldsymbol {a} _ {1} = \left( \begin{array}{c} 1 \\ 1 \\ 2 \\ 2 \end{array} \right), \quad \boldsymbol {a} _ {2} = \left( \begin{array}{c} 1 \\ 2 \\ 1 \\ 3 \end{array} \right), \quad \boldsymbol {a} _ {3} = \left( \begin{array}{c} 1 \\ - 1 \\ 4 \\ 0 \end{array} \right), \quad \boldsymbol {b} = \left( \begin{array}{c} 1 \\ 0 \\ 3 \\ 1 \end{array} \right),
$$

证明向量 b 能由向量组  $a_{1}, a_{2}, a_{3}$  线性表示，并求出表示式.

解 根据定理 1, 要证矩阵  $\boldsymbol{A} = (\boldsymbol{a}_{1}, \boldsymbol{a}_{2}, \boldsymbol{a}_{3})$  与  $\boldsymbol{B} = (\boldsymbol{A}, \boldsymbol{b})$  的秩相等. 为此, 把 B 化成行最简形矩阵:

考研电子书网站:www.pdf2book.com

85

---

第 4 章 向量组的线性相关性

$$
\boldsymbol {B} = \left( \begin{array}{c c c c} 1 & 1 & 1 & 1 \\ 1 & 2 & - 1 & 0 \\ 2 & 1 & 4 & 3 \\ 2 & 3 & 0 & 1 \end{array} \right) \underbrace {\frac {r _ {2} - r _ {1}}{r _ {3} - 2 r _ {1}}} _ {r _ {4} - 2 r _ {1}} \left( \begin{array}{c c c c} 1 & 1 & 1 & 1 \\ 0 & 1 & - 2 & - 1 \\ 0 & - 1 & 2 & 1 \\ 0 & 1 & - 2 & - 1 \end{array} \right) \sim \left( \begin{array}{c c c c} 1 & 0 & 3 & 2 \\ 0 & 1 & - 2 & - 1 \\ 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 \end{array} \right),
$$

可见, $R(A)=R(B)$ ,因此,向量b能由向量组 $a_{1},a_{2},a_{3}$ 线性表示.

由上述行最简形矩阵, 可得方程 $(a_{1}, a_{2}, a_{3}) \begin{pmatrix} x_{1} \\ x_{2} \\ x_{3} \end{pmatrix} = b$ 的通解为

$$
\left( \begin{array}{c} x _ {1} \\ x _ {2} \\ x _ {3} \end{array} \right) = c \left( \begin{array}{c} - 3 \\ 2 \\ 1 \end{array} \right) + \left( \begin{array}{c} 2 \\ - 1 \\ 0 \end{array} \right) = \left( \begin{array}{c} - 3 c + 2 \\ 2 c - 1 \\ c \end{array} \right),
$$

其中 $c$ 可任意取值, 从而得表示式

$$
\boldsymbol {b} = (\boldsymbol {a} _ {1}, \boldsymbol {a} _ {2}, \boldsymbol {a} _ {3}) \left( \begin{array}{l} x _ {1} \\ x _ {2} \\ x _ {3} \end{array} \right) = (- 3 c + 2) \boldsymbol {a} _ {1} + (2 c - 1) \boldsymbol {a} _ {2} + c \boldsymbol {a} _ {3}.
$$

例2 设

$$
\boldsymbol {a} _ {1} = \left( \begin{array}{c} 1 \\ - 1 \\ 1 \\ - 1 \end{array} \right), \quad \boldsymbol {a} _ {2} = \left( \begin{array}{c} 3 \\ 1 \\ 1 \\ 3 \end{array} \right), \quad \boldsymbol {b} _ {1} = \left( \begin{array}{c} 2 \\ 0 \\ 1 \\ 1 \end{array} \right), \quad \boldsymbol {b} _ {2} = \left( \begin{array}{c} 1 \\ 1 \\ 0 \\ 2 \end{array} \right), \quad \boldsymbol {b} _ {3} = \left( \begin{array}{c} 3 \\ - 1 \\ 2 \\ 0 \end{array} \right),
$$

证明向量组  $a_{1}, a_{2}$  与向量组  $b_{1}, b_{2}, b_{3}$  等价.

证 记 $A = (a_{1}, a_{2}), B = (b_{1}, b_{2}, b_{3})$. 根据定理 2 的推论, 只要证 $R(A) = R(B) = R(A, B)$. 为此把矩阵 $(A, B)$ 化成行阶梯形矩阵:

$$
(A, B) = \left( \begin{array}{r r r r r} 1 & 3 & 2 & 1 & 3 \\ - 1 & 1 & 0 & 1 & - 1 \\ 1 & 1 & 1 & 0 & 2 \\ - 1 & 3 & 1 & 2 & 0 \end{array} \right) \stackrel {{r}} {{\sim}} \left( \begin{array}{r r r r r} 1 & 3 & 2 & 1 & 3 \\ 0 & 4 & 2 & 2 & 2 \\ 0 & - 2 & - 1 & - 1 & - 1 \\ 0 & 6 & 3 & 3 & 3 \end{array} \right) \stackrel {{r}} {{\sim}} \left( \begin{array}{r r r r r} 1 & 3 & 2 & 1 & 3 \\ 0 & 2 & 1 & 1 & 1 \\ 0 & 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 & 0 \end{array} \right),
$$

可见, $R(A)=2,R(A,B)=2.$

容易看出矩阵 $\pmb{B}$ 中有不等于0的2阶子式，故 $R(B)\geqslant 2.$ 又

$$
R (\boldsymbol {B}) \leqslant R (\boldsymbol {A}, \boldsymbol {B}) = 2,
$$

于是知 $R(\pmb {B}) = 2.$ 因此，

$$
R (\boldsymbol {A}) = R (\boldsymbol {B}) = R (\boldsymbol {A}, \boldsymbol {B}),
$$

故向量组 $a_1, a_2$ 与向量组 $b_1, b_2, b_3$ 等价.

86

---

§2 向量组的线性相关性

定理 3 设向量组  $B: b_{1}, b_{2}, \cdots, b_{l}$  能由向量组  $A: a_{1}, a_{2}, \cdots, a_{m}$  线性表示，则  $R(b_{1}, b_{2}, \cdots, b_{l}) \leqslant R(a_{1}, a_{2}, \cdots, a_{m})$ .

证 记  $\boldsymbol{A}=(\boldsymbol{a}_{1},\boldsymbol{a}_{2},\cdots,\boldsymbol{a}_{m}),\boldsymbol{B}=(\boldsymbol{b}_{1},\boldsymbol{b}_{2},\cdots,\boldsymbol{b}_{l})$ . 按定理的条件, 根据定理 2 有  $R(\boldsymbol{A})=R(\boldsymbol{A},\boldsymbol{B})$ , 而  $R(\boldsymbol{B})\leqslant R(\boldsymbol{A},\boldsymbol{B})$ , 因此

$$
R (\boldsymbol {B}) \leqslant R (\boldsymbol {A}).
$$

证毕

前面我们把定理1与上章定理5对应, 把定理2与上章定理6对应, 而定理3可与上章定理7对应. 事实上, 按定理3的条件, 知有矩阵K, 使B=AK, 从而根据上章定理7, 即有 $R(B)\leqslant R(A)$ .

上述各定理之间的对应,其基础是向量组与矩阵的对应,从而有下述对应:

向量组  $B:b_{1},b_{2},\cdots,b_{l}$  能由向量组  $A:a_{1},a_{2},\cdots,a_{m}$  线性表示

$\Leftrightarrow$ 有矩阵 $\pmb{K}$, 使 $\pmb{B} = \pmb{A}\pmb{K}$

$\Leftrightarrow$ 方程 $AX = B$ 有解.

上述对应的三种叙述都可对应到充分必要条件: $R(A)=R(A,B)$ ，并都有必要条件: $R(A)\geqslant R(B)$ .

例3 设 $n$ 维向量组 $A: a_1, a_2, \cdots, a_m$ 构成 $n \times m$ 矩阵 $A = (a_1, a_2, \cdots, a_m)$, $n$ 阶单位矩阵 $E = (e_1, e_2, \cdots, e_n)$ 的列向量叫做 $n$ 维单位坐标向量. 证明: $n$ 维单位坐标向量组 $e_1, e_2, \cdots, e_n$ 能由向量组 $A$ 线性表示的充分必要条件是 $R(A) = n$.

证 根据定理 2, 向量组  $e_{1}, e_{2}, \cdots, e_{n}$  能由向量组 A 线性表示的充分必要条件是  $R(A) = R(A, E)$ .

而 $R(A, E) \geqslant R(E) = n$，又矩阵 $(A, E)$ 含 $n$ 行，知 $R(A, E) \leqslant n$，合起来有 $R(A, E) = n$. 因此条件 $R(A) = R(A, E)$ 就是 $R(A) = n$.

本例所证结论用矩阵语言可叙述为

对矩阵 $A_{n\times m}$ ，存在矩阵 $\pmb{K}_{m\times n}$ ，使 $\pmb {AK} = \pmb{E}_n$ 的充分必要条件是 $R(A) = n.$

也可叙述为

矩阵方程 $A_{n \times m} X = E_n$ 有解的充分必要条件是 $R(A) = n$ （参见第3章习题三第24题）.

## § 2 向量组的线性相关性

定义 4 给定向量组  $A: a_{1}, a_{2}, \cdots, a_{m}$ ，若存在不全为零的数  $k_{1}, k_{2}, \cdots, k_{m}$ ，使

$$
k _ {1} \boldsymbol {a} _ {1} + k _ {2} \boldsymbol {a} _ {2} + \dots + k _ {m} \boldsymbol {a} _ {m} = \boldsymbol {0},
$$

则称向量组 A 是线性相关的, 否则称它线性无关.

考研电子书网站:www.pdf2book.com

87

---

第4章 向量组的线性相关性

对于只含一个向量 $a$ 的向量组, 当 $a = 0$ 时是线性相关的, 当 $a \neq 0$ 时是线性无关的. 对于含两个向量 $a_1, a_2$ 的向量组, 它线性相关的充分必要条件是 $a_1, a_2$ 的分量对应成比例, 其几何意义是两向量共线. 三个向量线性相关的几何意义是三向量共面.

向量组  $A: a_{1}, a_{2}, \cdots, a_{m} (m \geqslant 2)$  线性相关的充分必要条件是在向量组 A 中至少有一个向量能由其余 m-1 个向量线性表示. 这是因为

若向量组 A 线性相关, 则有不全为 0 的数  $k_{1}, k_{2}, \cdots, k_{m}$  使  $k_{1}a_{1} + k_{2}a_{2} + \cdots + k_{m}a_{m} = 0$ . 因  $k_{1}, k_{2}, \cdots, k_{m}$  不全为 0, 不妨设  $k_{1} \neq 0$ , 于是便有

$$
\boldsymbol {a} _ {1} = - \frac {1}{k _ {1}} (k _ {2} \boldsymbol {a} _ {2} + k _ {3} \boldsymbol {a} _ {3} + \dots + k _ {m} \boldsymbol {a} _ {m}),
$$

即  $a_{1}$  能由  $a_{2}, a_{3}, \cdots, a_{m}$  线性表示.

如果向量组 A 中有某个向量能由其余 m-1 个向量线性表示, 不妨设  $a_{m}$  能由  $a_{1}, a_{2}, \cdots, a_{m-1}$  线性表示, 即有  $\lambda_{1}, \lambda_{2}, \cdots, \lambda_{m-1}$  使  $a_{m} = \lambda_{1}a_{1} + \lambda_{2}a_{2} + \cdots + \lambda_{m-1}a_{m-1}$ , 于是

$$
\lambda_ {1} \boldsymbol {a} _ {1} + \lambda_ {2} \boldsymbol {a} _ {2} + \dots + \lambda_ {m - 1} \boldsymbol {a} _ {m - 1} + (- 1) \boldsymbol {a} _ {m} = \boldsymbol {0},
$$

因为  $\lambda_{1}, \lambda_{2}, \cdots, \lambda_{m-1}, -1$  这 m 个数不全为 0（至少  $-1 \neq 0$ ），所以向量组 A 线性相关.

向量组  $A:a_{1},a_{2},\cdots,a_{m}$  构成矩阵  $\boldsymbol{A}=(\boldsymbol{a}_{1},\boldsymbol{a}_{2},\cdots,\boldsymbol{a}_{m})$ ，向量组 A 线性相关，就是齐次线性方程组

$$
x _ {1} \boldsymbol {a} _ {1} + x _ {2} \boldsymbol {a} _ {2} + \dots + x _ {m} \boldsymbol {a} _ {m} = \boldsymbol {0},
$$

即 Ax=0 有非零解.由上章定理 4, 立即可得

定理 4 向量组  $A: a_{1}, a_{2}, \cdots, a_{m}$  线性相关的充分必要条件是它所构成的矩阵  $A = (a_{1}, a_{2}, \cdots, a_{m})$  的秩小于向量个数 m；向量组 A 线性无关的充分必要条件是  $R(A) = m$ .

例 4 试讨论 n 维单位坐标向量组的线性相关性.

解 $n$ 维单位坐标向量组构成的矩阵

$$
E = (e _ {1}, e _ {2}, \dots , e _ {n})
$$

是 $n$ 阶单位矩阵. 由 $|\pmb{E}| = 1 \neq 0$, 知 $R(\pmb{E}) = n$, 即 $R(\pmb{E})$ 等于向量组中向量的个数, 故由定理4知此向量组是线性无关的.

例5 已知

$$
\boldsymbol {a} _ {1} = \left( \begin{array}{c} 1 \\ 1 \\ 1 \end{array} \right), \quad \boldsymbol {a} _ {2} = \left( \begin{array}{c} 0 \\ 2 \\ 5 \end{array} \right), \quad \boldsymbol {a} _ {3} = \left( \begin{array}{c} 2 \\ 4 \\ 7 \end{array} \right),
$$

试讨论向量组  $a_{1}, a_{2}, a_{3}$  及向量组  $a_{1}, a_{2}$  的线性相关性.

解 对矩阵 $(\pmb{a}_1, \pmb{a}_2, \pmb{a}_3)$ 施行初等行变换变成行阶梯形矩阵，即可同时看出矩阵 $(\pmb{a}_1, \pmb{a}_2, \pmb{a}_3)$ 及 $(\pmb{a}_1, \pmb{a}_2)$ 的秩，利用定理4即可得出结论.

$$
(\boldsymbol {a} _ {1}, \boldsymbol {a} _ {2}, \boldsymbol {a} _ {3}) = \left( \begin{array}{c c c} 1 & 0 & 2 \\ 1 & 2 & 4 \\ 1 & 5 & 7 \end{array} \right) \xrightarrow [ r _ {3} - r _ {1} ]{r _ {2} - r _ {1}} \left( \begin{array}{c c c} 1 & 0 & 2 \\ 0 & 2 & 2 \\ 0 & 5 & 5 \end{array} \right) \xrightarrow {r _ {3} - \frac {5}{2} r _ {2}} \left( \begin{array}{c c c} 1 & 0 & 2 \\ 0 & 2 & 2 \\ 0 & 0 & 0 \end{array} \right),
$$

88

---

§2 向量组的线性相关性

可见 $R(\pmb{a}_1, \pmb{a}_2, \pmb{a}_3) = 2$，故向量组 $\pmb{a}_1, \pmb{a}_2, \pmb{a}_3$ 线性相关；同时可见 $R(\pmb{a}_1, \pmb{a}_2) = 2$，故向量组 $\pmb{a}_1, \pmb{a}_2$ 线性无关.

例6 已知向量组 $a_1, a_2, a_3$ 线性无关，$b_1 = a_1 + a_2, b_2 = a_2 + a_3, b_3 = a_3 + a_1$，试证向量组 $b_1, b_2, b_3$ 线性无关.

证法1 设有 $x_{1}, x_{2}, x_{3}$ 使

$$
x _ {1} \boldsymbol {b} _ {1} + x _ {2} \boldsymbol {b} _ {2} + x _ {3} \boldsymbol {b} _ {3} = \boldsymbol {0},
$$

即

$$
x _ {1} (a _ {1} + a _ {2}) + x _ {2} (a _ {2} + a _ {3}) + x _ {3} (a _ {3} + a _ {1}) = 0,
$$

亦即

$$
(x _ {1} + x _ {3}) a _ {1} + (x _ {1} + x _ {2}) a _ {2} + (x _ {2} + x _ {3}) a _ {3} = 0,
$$

因 $a_1, a_2, a_3$ 线性无关，故有

$$
\left\{ \begin{array}{l} x _ {1} + x _ {3} = 0, \\ x _ {1} + x _ {2} = 0, \\ x _ {2} + x _ {3} = 0, \end{array} \right.
$$

由于此方程组的系数矩阵

$$
\boldsymbol {K} = \left( \begin{array}{c c c} 1 & 0 & 1 \\ 1 & 1 & 0 \\ 0 & 1 & 1 \end{array} \right)
$$

的行列式 $|\mathbf{K}| = 2 \neq 0$，故方程组只有零解 $x_{1} = x_{2} = x_{3} = 0$，所以向量组 $\pmb{b}_{1}, \pmb{b}_{2}, \pmb{b}_{3}$ 线性无关.

证法2 把已知的三个向量等式写成一个矩阵等式

$$
(\boldsymbol {b} _ {1}, \boldsymbol {b} _ {2}, \boldsymbol {b} _ {3}) = (\boldsymbol {a} _ {1}, \boldsymbol {a} _ {2}, \boldsymbol {a} _ {3}) \left( \begin{array}{c c c} 1 & 0 & 1 \\ 1 & 1 & 0 \\ 0 & 1 & 1 \end{array} \right),
$$

记作 $B = AK$. 设 $Bx = 0$, 以 $B = AK$ 代入得 $A(Kx) = 0$. 因为矩阵 $A$ 的列向量组线性无关, 根据向量组线性无关的定义, 知 $Kx = 0$. 又因 $|K| = 2 \neq 0$, 知方程 $Kx = 0$ 只有零解 $x = 0$. 所以矩阵 $B$ 的列向量组 $b_1, b_2, b_3$ 线性无关.

证法3 把已知条件合写成

$$
(\boldsymbol {b} _ {1}, \boldsymbol {b} _ {2}, \boldsymbol {b} _ {3}) = (\boldsymbol {a} _ {1}, \boldsymbol {a} _ {2}, \boldsymbol {a} _ {3}) \left( \begin{array}{c c c} 1 & 0 & 1 \\ 1 & 1 & 0 \\ 0 & 1 & 1 \end{array} \right),
$$

记作 $B = AK$. 因 $|\pmb{K}| = 2 \neq 0$, 知 $\pmb{K}$ 可逆, 根据上章所述矩阵秩的性质④知 $R(\pmb{B}) = R(\pmb{A})$.

因为 A 的列向量组线性无关, 根据定理 4 知  $R(A)=3$ , 从而  $R(B)=3$ , 再由定理 4

考研电子书网站:www.pdf2book.com

89

---

第4章 向量组的线性相关性

知 B 的 3 个列向量线性无关, 即  $b_{1}, b_{2}, b_{3}$  线性无关.

本例给出三种证法,这三种证法都是常用的.证法1是按线性相关性的定义,通过向量的运算得到以K为系数矩阵的齐次方程组,再把问题转化为它只有零解;证法2和证法3都首先把已知三个向量等式合并成矩阵等式,立即得到矩阵K;之后,证法2把证明向量组线性无关转化为证明齐次方程组没有非零解,因而去考察方程组Bx=0,证法3用了矩阵的秩的有关知识,还用了定理4,从而可以不涉及线性方程组而直接证得结论.

线性相关性是向量组的一个重要性质,下面介绍与之有关的一些简单的结论.

定理 5 （1）若向量组  $A:a_{1},a_{2},\cdots,a_{m}$  线性相关，则向量组  $B:a_{1},a_{2},\cdots,a_{m},a_{m+1}$  也线性相关。反之，若向量组 B 线性无关，则向量组 A 也线性无关。

(2) $m$ 个 $n$ 维向量组成的向量组; 当维数 $n$ 小于向量个数 $m$ 时一定线性相关. 特别地, $n + 1$ 个 $n$ 维向量一定线性相关.

（3）设向量组  $A:a_{1},a_{2},\cdots,a_{m}$  线性无关，而向量组  $B:a_{1},a_{2},\cdots,a_{m},b$  线性相关，则向量 b 必能由向量组 A 线性表示，且表示式是惟一的.

证 这些结论都可利用定理 4 来证明.

（1）记 $A=(a_{1},a_{2},\cdots,a_{m}),B=(a_{1},a_{2},\cdots,a_{m},a_{m+1})$ ，有 $R(B)\leqslant R(A)+1$ 。因向量组A线性相关，故根据定理4，有 $R(A)<m$ ，从而 $R(B)\leqslant R(A)+1<m+1$ ，因此根据定理4知向量组B线性相关。

(2) m 个 n 维向量  $a_{1}, a_{2}, \cdots, a_{m}$  构成矩阵  $A_{n \times m} = (a_{1}, a_{2}, \cdots, a_{m})$ ，有  $R(A) \leqslant n$ 。当 n < m 时，有  $R(A) < m$ ，故 m 个向量  $a_{1}, a_{2}, \cdots, a_{m}$  线性相关。

（3）记 $A=(a_{1},a_{2},\cdots,a_{m}),B=(a_{1},a_{2},\cdots,a_{m},b)$ ，有 $R(A)\leqslant R(B)$ 。因向量组A线性无关，有 $R(A)=m$ ；因向量组B线性相关，有 $R(B)<m+1$ 。所以 $m\leqslant R(B)<m+1$ ，即有 $R(B)=m$ 。

由  $R(A)=R(B)=m$ ，根据上章定理3，知方程组

$$
(a _ {1}, a _ {2}, \dots , a _ {m}) x = b
$$

有惟一解, 即向量 b 能由向量组 A 线性表示, 且表示式是惟一的.

证毕

结论(1)是对向量组增加1个向量而言的,增加多个向量结论也仍然成立.即设向量组A是向量组B的一部分(这时称向量组A是向量组B的部分组),于是结论(1)可一般地叙述为:一个向量组若有线性相关的部分组,则该向量组线性相关.特别地,含零向量的向量组必线性相关.一个向量组若线性无关,则它的任何部分组都线性无关.

例 7 设向量组  $a_{1}, a_{2}, a_{3}$  线性相关, 向量组  $a_{2}, a_{3}, a_{4}$  线性无关, 证明:

(1) $a_{1}$ 能由 $a_{2},a_{3}$ 线性表示；

(2) $a_{4}$ 不能由 $a_{1},a_{2},a_{3}$ 线性表示.

90

---

§3 向量组的秩

证（1）因 $a_2, a_3, a_4$ 线性无关，由定理5(1)知 $a_2, a_3$ 线性无关，而 $a_1, a_2, a_3$ 线性相关，由定理5(3)知 $a_1$ 能由 $a_2, a_3$ 线性表示.

（2）用反证法.假设 $a_4$ 能由 $a_1, a_2, a_3$ 线性表示，而由(1)知 $a_1$ 能由 $a_2, a_3$ 线性表示，因此 $a_4$ 能由 $a_2, a_3$ 线性表示，这与 $a_2, a_3, a_4$ 线性无关矛盾.故 $a_4$ 不能由 $a_1, a_2, a_3$ 线性表示.

## § 3 向量组的秩

在上两节的讨论中,向量组只局限于含有限个向量.现在我们将去掉这一限制:向量组可以含无限多个向量.

例如

$$
A: \binom{0}{0}, \binom{1}{1}, \binom{2}{2}, \dots , \binom{k}{k}, \dots
$$

与

$$
B: \left( \begin{array}{l} 0 \\ 0 \end{array} \right), \left( \begin{array}{l} 1 \\ 2 \end{array} \right), \left( \begin{array}{l} 2 \\ 3 \end{array} \right), \dots , \left( \begin{array}{l} k \\ k + 1 \end{array} \right), \dots
$$

就是这样的向量组.因为它们都是2维向量组,由定理5之(2),知向量组A或向量组B中任意三个向量都是线性相关的;但进一步从线性无关部分组所含向量的个数来看就不一样了:向量组B中有含两个向量的线性无关部分组,如 $\binom{1}{2},\binom{2}{3}$ ;但向量组A中任何含两个向量的部分组都是线性相关的,换言之,A组中只有最多含一个向量的线性无关部分组,而B组中却有最多含两个向量的线性无关部分组.

上一章中,我们引入了矩阵的最高阶非零子式,并把它的阶数定义为矩阵的秩,它在前两节向量组线性表示和线性相关性的讨论中起了十分重要的作用.现在,按向量组与矩阵的对应,特别把含最多个向量的线性无关部分组与最高阶的非零子式相对应,就可将秩的概念引进向量组.

定义 5 设有向量组 A, 如果在 A 中能选出 r 个向量  $a_{1}, a_{2}, \cdots, a_{r}$ , 满足

(i) 向量组  $A_{0}: a_{1}, a_{2}, \cdots, a_{r}$  线性无关；

（ii）向量组 A 中任意  $r+1$  个向量（如果 A 中有  $r+1$  个向量的话）都线性相关，那么称向量组  $A_{0}$  是向量组 A 的一个最大线性无关向量组（简称最大无关组），最大无关组所含向量的个数 r 称为向量组 A 的秩，记作  $R_{A}$ .

只含零向量的向量组没有最大无关组,规定它的秩为0.

考研电子书网站:www.pdf2book.com

91

---

第4章 向量组的线性相关性

根据定义 5, 本节一开始给出的向量组 A 的秩  $R_{A}=1$ ,  $\begin{pmatrix}1\\1\end{pmatrix}$  是它的一个最大无关组; 向量组 B 的秩  $R_{B}=2$ ,  $\begin{pmatrix}1\\2\end{pmatrix}$ ,  $\begin{pmatrix}2\\3\end{pmatrix}$  是它的一个最大无关组, 显然两者的最大无关组都不惟一(甚至都有无限多个).

若向量组 $A$ 线性无关, 则 $A$ 自身就是它的最大无关组, 而其秩就等于它所含向量的个数.

向量组 A 和它自己的最大无关组  $A_{0}$  是等价的. 这是因为向量组  $A_{0}$  是向量组 A 的一个部分组, 故向量组  $A_{0}$  总能由向量组 A 线性表示 (A 中每个向量都能由向量组 A 线性表示); 而由定义 5 的条件 (ii) 知, 对于 A 中任一向量  $a, r+1$  个向量  $a_{1}, a_{2}, \cdots, a_{r}, a$  线性相关, 而  $a_{1}, a_{2}, \cdots, a_{r}$  线性无关, 根据定理 5 (3) 知 a 能由  $a_{1}, a_{2}, \cdots, a_{r}$  线性表示, 即向量组 A 能由向量组  $A_{0}$  线性表示. 所以向量组 A 与向量组  $A_{0}$  等价. n 维向量组 A 可能含有许多个甚至无限多个向量, 但  $A_{0}$  至多含 n 个向量.

上述结论的逆命题也是成立的,即能与向量组自身等价的线性无关部分组一定是最大无关组,现把它作为定理3的推论叙述如下:

推论(最大无关组的等价定义) 设向量组  $A_{0}: a_{1}, a_{2}, \cdots, a_{r}$  是向量组 A 的一个部分组, 且满足

(i) 向量组  $A_{0}$  线性无关；

(ii) 向量组 A 的任一向量都能由向量组  $A_{0}$  线性表示，

那么向量组  $A_{0}$  便是向量组 A 的一个最大无关组.

证 只要证向量组 A 中任意  $r+1$  个向量线性相关. 设  $b_{1}, b_{2}, \cdots, b_{r+1}$  是 A 中任意  $r+1$  个向量, 由条件(ii)知这  $r+1$  个向量能由向量组  $A_{0}$  线性表示, 从而根据定理 3, 有

$$
R (\boldsymbol {b} _ {1}, \boldsymbol {b} _ {2}, \dots , \boldsymbol {b} _ {r + 1}) \leqslant R (\boldsymbol {a} _ {1}, \boldsymbol {a} _ {2}, \dots , \boldsymbol {a} _ {r}) = r,
$$

再据定理4知 $r + 1$ 个向量 $\pmb{b}_1, \pmb{b}_2, \dots, \pmb{b}_{r+1}$ 线性相关. 因此向量组 $A_0$ 满足定义5所规定的最大无关组的条件. 证毕

下面给出分别按定义 5 和它的等价定义求向量组的秩的例题.

例 8 全体 n 维向量构成的向量组记作  $R^{n}$ ，求  $R^{n}$  的一个最大无关组及  $R^{n}$  的秩.

解 在例 4 中, 我们证明了 n 维单位坐标向量构成的向量组

$$
E: \boldsymbol {e} _ {1}, \boldsymbol {e} _ {2}, \dots , \boldsymbol {e} _ {n}
$$

是线性无关的,又根据定理5的结论(2),知 $\mathbb{R}^n$ 中的任意 $n + 1$ 个向量都线性相关,因此向量组 $E$ 是 $\mathbb{R}^n$ 的一个最大无关组,且 $\mathbb{R}^n$ 的秩等于 $n$.

显然, $\mathbb{R}^n$ 的最大无关组很多, 任何 $n$ 个线性无关的 $n$ 维向量都是 $\mathbb{R}^n$ 的最大无关组.

92

---

§3 向量组的秩

例9 设齐次线性方程组

$$
\left\{ \begin{array}{l} x _ {1} + 2 x _ {2} + x _ {3} - 2 x _ {4} = 0, \\ 2 x _ {1} + 3 x _ {2} - x _ {4} = 0, \\ x _ {1} - x _ {2} - 5 x _ {3} + 7 x _ {4} = 0 \end{array} \right.
$$

的全体解向量构成的向量组为 S, 求 S 的秩.

解 先解方程,为此把系数矩阵 A 化成行最简形矩阵:

$$
\boldsymbol {A} = \left( \begin{array}{c c c c} 1 & 2 & 1 & - 2 \\ 2 & 3 & 0 & - 1 \\ 1 & - 1 & - 5 & 7 \end{array} \right) \overbrace {r _ {3} - r _ {1}} ^ {r _ {2} - 2 r _ {1}} \left( \begin{array}{c c c c} 1 & 2 & 1 & - 2 \\ 0 & - 1 & - 2 & 3 \\ 0 & - 3 & - 6 & 9 \end{array} \right) \overbrace {r _ {2} \times (- 1)} ^ {r _ {1} + 2 r _ {2}} \left( \begin{array}{c c c c} 1 & 0 & - 3 & 4 \\ 0 & 1 & 2 & - 3 \\ 0 & 0 & 0 & 0 \end{array} \right),
$$

得

$$
\left\{ \begin{array}{l} x _ {1} = 3 x _ {3} - 4 x _ {4}, \\ x _ {2} = - 2 x _ {3} + 3 x _ {4}, \end{array} \right.
$$

令自由未知数 $x_{3} = c_{1}, x_{4} = c_{2}$, 得通解

$$
\left( \begin{array}{c} x _ {1} \\ x _ {2} \\ x _ {3} \\ x _ {4} \end{array} \right) = c _ {1} \left( \begin{array}{c} 3 \\ - 2 \\ 1 \\ 0 \end{array} \right) + c _ {2} \left( \begin{array}{c} - 4 \\ 3 \\ 0 \\ 1 \end{array} \right) \quad (c _ {1}, c _ {2} \in \mathbb {R}),
$$

把上式记作 $x = c_{1}\pmb{\xi}_{1} + c_{2}\pmb{\xi}_{2}$ ，知

$$
S = \left\{\boldsymbol {x} \mid \boldsymbol {x} = c _ {1} \boldsymbol {\xi} _ {1} + c _ {2} \boldsymbol {\xi} _ {2}, c _ {1}, c _ {2} \in \mathbb {R} \right\},
$$

即 $S$ 能由向量组 $\pmb{\xi}_1, \pmb{\xi}_2$ 线性表示. 又因 $\pmb{\xi}_1, \pmb{\xi}_2$ 的四个分量显然不成比例, 故 $\pmb{\xi}_1, \pmb{\xi}_2$ 线性无关. 因此根据最大无关组的等价定义知 $\pmb{\xi}_1, \pmb{\xi}_2$ 是 $S$ 的最大无关组, 从而 $R_S = 2$.

对于只含有限个 n 维向量的向量组  $A: a_{1}, a_{2}, \cdots, a_{m}$ ，它可以构成矩阵  $\boldsymbol{A} = (\boldsymbol{a}_{1}, \boldsymbol{a}_{2}, \cdots, \boldsymbol{a}_{m})$ 。把定义 5 与上章矩阵的最高阶非零子式及矩阵的秩的定义作比较，容易想到向量组 A 的秩就等于矩阵 A 的秩，即有

定理 6 矩阵的秩等于它的列向量组的秩,也等于它的行向量组的秩.

证 设 $A = (a_{1}, a_{2}, \cdots, a_{m}), R(A) = r$，并设 $r$ 阶子式 $D_{r} \neq 0$. 根据定理4，由 $D_{r} \neq 0$ 知 $D_{r}$ 所在的 $r$ 列构成的 $n \times r$ 矩阵的秩为 $r$，故此 $r$ 列线性无关；又由 $A$ 中所有 $r + 1$ 阶子式均为零，知 $A$ 中任意 $r + 1$ 个列向量构成的 $n \times (r + 1)$ 矩阵的秩 $< r + 1$，故此 $r + 1$ 列线性相关. 因此 $D_{r}$ 所在的 $r$ 列是 $A$ 的列向量组的一个最大无关组，所以列向量组的秩等于 $r$.

类似可证矩阵 A 的行向量组的秩也等于  $R(A)$ .

证毕

今后向量组  $a_{1}, a_{2}, \cdots, a_{m}$  的秩也记作  $R(a_{1}, a_{2}, \cdots, a_{m})$ .

从上述证明中可见: 若  $D_{r}$  是矩阵 A 的一个最高阶非零子式, 则  $D_{r}$  所在的 r 列即

考研电子书网站:www.pdf2book.com

93

---

第4章 向量组的线性相关性

是 $\pmb{A}$ 的列向量组的一个最大无关组, $D_{r}$ 所在的 $r$ 行即是 $\pmb{A}$ 的行向量组的一个最大无关组.这一事实在下面的例题中得到应用.

例10 设矩阵

$$
\boldsymbol {A} = \left( \begin{array}{c c c c c} 2 & - 1 & - 1 & 1 & 2 \\ 1 & 1 & - 2 & 1 & 4 \\ 4 & - 6 & 2 & - 2 & 4 \\ 3 & 6 & - 9 & 7 & 9 \end{array} \right),
$$

求矩阵 A 的列向量组的一个最大无关组, 并把不属于最大无关组的列向量用最大无关组线性表示.

解 对 A 施行初等行变换变为行阶梯形矩阵(参看第 3 章 §1 引例)

$$
A \stackrel {r} {\sim} \left( \begin{array}{c c c c c} 1 & 1 & - 2 & 1 & 4 \\ 0 & 1 & - 1 & 1 & 0 \\ 0 & 0 & 0 & 1 & - 3 \\ 0 & 0 & 0 & 0 & 0 \end{array} \right),
$$

知 $R(A) = 3$ ，故列向量组的最大无关组合3个向量.而三个非零行的首元在第1,2,4三列，故 $\pmb{a}_1,\pmb{a}_2,\pmb{a}_4$ 为列向量组的一个最大无关组

为把 $a_3, a_5$ 用 $a_1, a_2, a_4$ 线性表示，把 $A$ 再变成行最简形矩阵

$$
\boldsymbol {A} \stackrel {{r}} {{\sim}} \left( \begin{array}{c c c c c} 1 & 0 & - 1 & 0 & 4 \\ 0 & 1 & - 1 & 0 & 3 \\ 0 & 0 & 0 & 1 & - 3 \\ 0 & 0 & 0 & 0 & 0 \end{array} \right),
$$

把上述行最简形矩阵记作 $B = (b_{1}, b_{2}, b_{3}, b_{4}, b_{5})$，则方程 $Ax = 0$ 与 $Bx = 0$ 同解，即方程

$$
x _ {1} \boldsymbol {a} _ {1} + x _ {2} \boldsymbol {a} _ {2} + x _ {3} \boldsymbol {a} _ {3} + x _ {4} \boldsymbol {a} _ {4} + x _ {5} \boldsymbol {a} _ {5} = \mathbf {0}
$$

与

$$
x _ {1} \boldsymbol {b} _ {1} + x _ {2} \boldsymbol {b} _ {2} + x _ {3} \boldsymbol {b} _ {3} + x _ {4} \boldsymbol {b} _ {4} + x _ {5} \boldsymbol {b} _ {5} = \mathbf {0}
$$

同解.现在

$$
\begin{array}{l} \boldsymbol {b} _ {3} = \left( \begin{array}{c} - 1 \\ - 1 \\ 0 \\ 0 \end{array} \right) = (- 1) \left( \begin{array}{c} 1 \\ 0 \\ 0 \\ 0 \end{array} \right) + (- 1) \left( \begin{array}{c} 0 \\ 1 \\ 0 \\ 0 \end{array} \right) = - \boldsymbol {b} _ {1} - \boldsymbol {b} _ {2}, \\ \boldsymbol {b} _ {5} = 4 \boldsymbol {b} _ {1} + 3 \boldsymbol {b} _ {2} - 3 \boldsymbol {b} _ {4}, \\ \end{array}
$$

此即 $x_{1} = -1, x_{2} = -1, x_{3} = -1, x_{4} = 0, x_{5} = 0$ 与 $x_{1} = 4, x_{2} = 3, x_{3} = 0, x_{4} = -3, x_{5} = -1$ 是 $Bx = 0$ 的解，因此也是 $Ax = 0$ 的解.

94

---

§4 向量空间

故也有

$$
\boldsymbol {a} _ {3} = - \boldsymbol {a} _ {1} - \boldsymbol {a} _ {2}, \quad \boldsymbol {a} _ {5} = 4 \boldsymbol {a} _ {1} + 3 \boldsymbol {a} _ {2} - 3 \boldsymbol {a} _ {4}.
$$

依据向量组的秩的定义及定理6可知前面介绍的定理1、定理2、定理3、定理4中出现的矩阵的秩都可改为向量组的秩.例如定理2可叙述为

定理 2' 向量组  $b_{1}, b_{2}, \cdots, b_{l}$  能由向量组  $a_{1}, a_{2}, \cdots, a_{m}$  线性表示的充分必要条件是

$$
R (\boldsymbol {a} _ {1}, \boldsymbol {a} _ {2}, \dots , \boldsymbol {a} _ {m}) = R (\boldsymbol {a} _ {1}, \boldsymbol {a} _ {2}, \dots , \boldsymbol {a} _ {m}, \boldsymbol {b} _ {1}, \boldsymbol {b} _ {2}, \dots , \boldsymbol {b} _ {l}).
$$

这里记号  $R(a_{1},a_{2},\cdots,a_{m})$  既可理解为矩阵的秩,也可理解成向量组的秩.

前面我们建立定理1、定理2、定理3时，限制向量组只含有限个向量，现在我们要去掉这一限制，把定理1、定理2、定理3推广到一般情形。推广的方法是利用向量组的最大无关组作过渡。下面仅推广定理9，定理1和定理2的推广请读者自行完成。

定理 3' 若向量组 B 能由向量组 A 线性表示, 则  $R_{B} \leqslant R_{A}$ .

证 设 $R_{A} = s, R_{B} = t$，并设向量组 $A$ 和 $B$ 的最大无关组依次为

$$
A _ {0}: \pmb {a} _ {1}, \pmb {a} _ {2}, \dots , \pmb {a} _ {s} \quad \text {和} \quad B _ {0}: \pmb {b} _ {1}, \pmb {b} _ {2}, \dots , \pmb {b} _ {t},
$$

由于向量组 $B_{0}$ 能由向量组 $B$ 线性表示，向量组 $B$ 能由向量组 $A$ 线性表示，向量组 $A$ 能由向量组 $A_{0}$ 线性表示，因此向量组 $B_{0}$ 能由向量组 $A_{0}$ 线性表示，根据定理3，有

$$
R (\boldsymbol {b} _ {1}, \boldsymbol {b} _ {2}, \dots , \boldsymbol {b} _ {i}) \leqslant R (\boldsymbol {a} _ {1}, \boldsymbol {a} _ {2}, \dots , \boldsymbol {a} _ {s}),
$$

即 $t \leqslant s$.

证毕

今后,定理3与定理3'将不加区别,都称定理3.定理1和2与推广后的定理也不加区别.

例11 设向量组 $B$ 能由向量组 $A$ 线性表示, 且它们的秩相等, 证明向量组 $A$ 与向量组 $B$ 等价.

证 设向量组 $A$ 和 $B$ 合并成向量组 $C$, 根据定理 2, 因向量组 $B$ 能由向量组 $A$ 表示, 故 $R_A = R_C$, 又已知 $R_B = R_A$, 故有 $R_A = R_B = R_C$. 根据定理 2 的推论, 知向量组 $A$ 与向量组 $B$ 等价.

## § 4 向量空间

本章 §1 中把 $n$ 维向量的全体所构成的集合 $\mathbb{R}^n$ 叫做 $n$ 维向量空间. 下面介绍向量空间的有关知识.

定义6 设 $V$ 为 $n$ 维向量的集合, 如果集合 $V$ 非空, 且集合 $V$ 对于向量的加法及

考研电子书网站:www.pdf2book.com

95

---

第4章 向量组的线性相关性

数乘两种运算封闭,那么就称集合 V 为向量空间.

所谓封闭,是指在集合 V 中可以进行向量的加法及数乘两种运算.具体地说,就是:若  $a \in V, b \in V$ , 则  $a + b \in V$ ; 若  $a \in V, \lambda \in R$ , 则  $\lambda a \in V$ .

例12 3维向量的全体 $\mathbb{R}^3$ 是一个向量空间. 因为任意两个3维向量之和仍然是3维向量, 数 $\lambda$ 乘3维向量也仍然是3维向量, 它们都属于 $\mathbb{R}^3$. 我们可以用有向线段形象地表示3维向量, 从而向量空间 $\mathbb{R}^3$ 可形象地看作以坐标原点为起点的有向线段的全体. 由于以原点为起点的有向线段与其终点一一对应, 因此 $\mathbb{R}^3$ 也可看作取定坐标原点的点空间.

类似地, $n$ 维向量的全体 $\mathbb{R}^n$ 也是一个向量空间. 不过当 $n > 3$ 时, 它没有直观的几何意义.

例13 集合

$$
V = \{\boldsymbol {x} \mid \boldsymbol {x} = (0, x _ {2}, \dots , x _ {n}) ^ {\mathrm{T}}, x _ {2}, x _ {3}, \dots , x _ {n} \in \mathbb {R} \}
$$

是一个向量空间.因为若  $\boldsymbol{a}=(0,a_{2},\cdots,a_{n})^{\mathrm{T}}\in V,\boldsymbol{b}=(0,b_{2},\cdots,b_{n})^{\mathrm{T}}\in V,\lambda\in\mathbb{R}$ ，则

$$
\begin{array}{l} \boldsymbol {a} + \boldsymbol {b} = (0, a _ {2} + b _ {2}, \dots , a _ {n} + b _ {n}) ^ {\mathrm{T}} \in V, \\ \lambda \boldsymbol {a} = (0, \lambda a _ {2}, \dots , \lambda a _ {n}) ^ {\mathrm{T}} \in V. \\ \end{array}
$$

例14 集合

$$
V = \{\boldsymbol {x} \mid \boldsymbol {x} = (1, x _ {2}, \dots , x _ {n}) ^ {\mathrm{T}}, x _ {2}, x _ {3}, \dots , x _ {n} \in \mathbb {R} \}
$$

不是向量空间,因为若  $\boldsymbol{a}=(1,a_{2},\cdots,a_{n})^{\mathrm{T}}\in V$ ,则

$$
2 \boldsymbol {a} = (2, 2 a _ {2}, \dots , 2 a _ {n}) ^ {\mathrm{T}} \notin V.
$$

例15 $n$ 元齐次线性方程组的解集

$$
S = \{\boldsymbol {x} \mid \boldsymbol {A} \boldsymbol {x} = \boldsymbol {0} \}
$$

是一个向量空间（称为齐次线性方程组的解空间）. 因为若 $\xi_{1} \in S, \xi_{2} \in S, \lambda \in \mathbb{R}$, 则 $A(\xi_{1} + \xi_{2}) = A\xi_{1} + A\xi_{2} = 0 + 0 = 0$, 即 $\xi_{1} + \xi_{2} \in S; A(\lambda \xi_{1}) = \lambda (A\xi_{1}) = \lambda 0 = 0$, 即 $\lambda \xi_{1} \in S$.

例16 非齐次线性方程组的解集

$$
S = \{\boldsymbol {x} \mid \boldsymbol {A} \boldsymbol {x} = \boldsymbol {b} \}
$$

不是向量空间.因为当 $S$ 为空集时，$S$ 不是向量空间；当 $S$ 非空时，若 $\pmb{\eta} \in S$，则 $A(2\pmb{\eta}) = 2b \neq b$，故 $2\pmb{\eta} \notin S$.

例 17 设 a, b 为两个已知的 n 维向量, 集合

$$
V = \{\lambda a + \mu b \mid \lambda , \mu \in \mathbb {R} \}
$$

是一个向量空间. 因为若 $x_{1} = \lambda_{1}a + \mu_{1}b, x_{2} = \lambda_{2}a + \mu_{2}b, k \in \mathbb{R}$, 则有

$$
\begin{array}{l} \boldsymbol {x} _ {1} + \dot {\boldsymbol {x}} _ {2} = (\lambda_ {1} + \lambda_ {2}) \boldsymbol {a} + (\mu_ {1} + \mu_ {2}) \boldsymbol {b} \in V, \\ k x _ {1} = (k \lambda_ {1}) a + (k \mu_ {1}) b \in V. \\ \end{array}
$$

这个向量空间称为由向量 $a, b$ 所生成的向量空间，也可记为 $\operatorname{Span}\{a, b\}$.

96

---

§4 向量空间

一般地，由向量组  $a_{1}, a_{2}, \cdots, a_{m}$  所生成的向量空间为

$$
L = \{\lambda_ {1} \boldsymbol {a} _ {1} + \lambda_ {2} \boldsymbol {a} _ {2} + \dots + \lambda_ {m} \boldsymbol {a} _ {m} | \lambda_ {1}, \lambda_ {2}, \dots , \lambda_ {m} \in \mathbb {R} \},
$$

可记为  $\operatorname{Span}\left\{a_{1},a_{2},\cdots,a_{m}\right\}$ .

例 18 设向量组  $a_{1}, a_{2}, \cdots, a_{m}$  与向量组  $b_{1}, b_{2}, \cdots, b_{s}$  等价，记

$$
L _ {1} = \{\lambda_ {1} a _ {1} + \lambda_ {2} a _ {2} + \dots + \lambda_ {m} a _ {m} | \lambda_ {1}, \lambda_ {2}, \dots , \lambda_ {m} \in \mathbb {R} \},
$$

$$
L _ {2} = \{\mu_ {1} \boldsymbol {b} _ {1} + \mu_ {2} \boldsymbol {b} _ {2} + \dots + \mu_ {s} \boldsymbol {b} _ {s} \mid \mu_ {1}, \mu_ {2}, \dots , \mu_ {s} \in \mathbb {R} \},
$$

试证 $L_{1} = L_{2}$

证 设 $x \in L_1$，则 $x$ 可由 $a_1, a_2, \cdots, a_m$ 线性表示。因 $a_1, a_2, \cdots, a_m$ 可由 $b_1, b_2, \cdots, b_s$ 线性表示，故 $x$ 可由 $b_1, b_2, \cdots, b_s$ 线性表示，所以 $x \in L_2$。这就是说，若 $x \in L_1$，则 $x \in L_2$，因此 $L_1 \subseteq L_2$.

类似地可证: 若  $x \in L_{2}$ ，则  $x \in L_{1}$ ，因此  $L_{2} \subseteq L_{1}$ .

因为  $L_{1} \subseteq L_{2}, L_{2} \subseteq L_{1}$ ，所以  $L_{1} = L_{2}$ .

定义 7 设有向量空间  $V_{1}$  及  $V_{2}$ ，若  $V_{1} \subseteq V_{2}$ ，就称  $V_{1}$  是  $V_{2}$  的子空间.

例如任何由 $n$ 维向量所组成的向量空间 $V$, 总有 $V \subseteq \mathbb{R}^n$, 这样的向量空间总是 $\mathbb{R}^n$ 的子空间. 据此可知, 例13、例15、例17中的向量空间均是 $\mathbb{R}^n$ 的子空间.

定义 8 设 V 为向量空间, 如果 r 个向量  $a_{1}, a_{2}, \cdots, a_{r} \in V$ , 且满足

(i)  $a_{1}, a_{2}, \cdots, a_{r}$  线性无关；
(ii) V 中任一向量都可由  $a_{1}, a_{2}, \cdots, a_{r}$  线性表示，

那么向量组  $a_{1}, a_{2}, \cdots, a_{r}$  称为向量空间 V 的一个基，r 称为向量空间 V 的维数，记为  $\dim V = r$ ，并称 V 为 r 维向量空间.

如果向量空间 V 没有基,那么 V 的维数为 0.0 维向量空间只含一个零向量 0.

若把向量空间 V 看作向量组, 则由最大无关组的等价定义可知, V 的基就是向量组的最大无关组, V 的维数就是向量组的秩.

例如, 由例8知, 任何 $n$ 个线性无关的 $n$ 维向量都可以是向量空间 $\mathbb{R}^n$ 的一个基, 且由此可知 $\mathbb{R}^n$ 的维数为 $n$, 所以我们把 $\mathbb{R}^n$ 称为 $n$ 维向量空间.

又如,向量空间

$$
V = \{(0, x _ {2}, \dots , x _ {n}) ^ {\mathrm{T}} | x _ {2}, x _ {3}, \dots , x _ {n} \in \mathbb {R} \}
$$

的一个基可取为  $\boldsymbol{e}_{2}=(0,1',0,\cdots,0)^{\mathrm{T}},\cdots,\boldsymbol{e}_{n}=(0,\cdots,0,1)^{\mathrm{T}}$ . 并由此可知它是 n-1 维向量空间.

设由向量组  $a_{1}, a_{2}, \cdots, a_{m}$  所生成的向量空间

$$
L = \{\lambda_ {1} a _ {1} + \lambda_ {2} a _ {2} + \dots + \lambda_ {m} a _ {m} \mid \lambda_ {1}, \lambda_ {2}, \dots , \lambda_ {m} \in \mathbb {R} \},
$$

显然向量空间 L 与向量组  $a_{1}, a_{2}, \cdots, a_{m}$  等价，所以向量组  $a_{1}, a_{2}, \cdots, a_{m}$  的最大无关组就是 L 的一个基，向量组  $a_{1}, a_{2}, \cdots, a_{m}$  的秩就是 L 的维数.

若向量组  $a_{1}, a_{2}, \cdots, a_{r}$  是向量空间 V 的一个基，则 V 可表示为

考研电子书网站:www.pdf2book.com

97

---

第4章 向量组的线性相关性

$$
V = \{\lambda_ {1} \boldsymbol {a} _ {1} + \lambda_ {2} \boldsymbol {a} _ {2} + \dots + \lambda_ {r} \boldsymbol {a} _ {r} \mid \lambda_ {1}, \lambda_ {2}, \dots , \lambda_ {r} \in \mathbb {R} \},
$$

即 V 是基所生成的向量空间  $Span\{a_{1}, a_{2}, \cdots a_{r}\}$ ，这就较清楚地显示出向量空间 V 的构造.

例如齐次线性方程组的解空间 $S = \{x \mid Ax = 0\}$, 若能找到解空间的一个基 $\xi_1, \xi_2, \dots, \xi_{n-r}$, 则解空间可表示为

$$
S = \left\{c _ {1} \pmb {\xi} _ {1} + c _ {2} \pmb {\xi} _ {2} + \dots + c _ {n - r} \pmb {\xi} _ {n - r} \mid c _ {1}, c _ {2}, \dots , c _ {n - r} \in \mathbb {R} \right\}.
$$

定义9 如果在向量空间 V 中取定一个基  $a_{1}, a_{2}, \cdots, a_{r}$ ，那么 V 中任一向量 x 可惟一地表示为

$$
\boldsymbol {x} = \lambda_ {1} \boldsymbol {a} _ {1} + \lambda_ {2} \boldsymbol {a} _ {2} + \dots + \lambda_ {r} \boldsymbol {a} _ {r},
$$

这个有序数组  $\lambda_{1},\lambda_{2},\cdots,\lambda_{r}$  称为向量 x 在基  $a_{1},a_{2},\cdots,a_{r}$  下的坐标，并记作  $(\lambda_{1},\lambda_{2},\cdots,\lambda_{r})^{\mathrm{T}}$ .

特别地, 在 n 维向量空间  $R^{n}$  中取单位坐标向量组  $e_{1}, e_{2}, \cdots, e_{n}$  为基, 则以  $x_{1}, x_{2}, \cdots, x_{n}$  为分量的向量 x 可表示为

$$
\boldsymbol {x} = x _ {1} \boldsymbol {e} _ {1} + x _ {2} \boldsymbol {e} _ {2} + \dots + x _ {n} \boldsymbol {e} _ {n},
$$

可见向量在基 $e_{1},e_{2},\cdots,e_{n}$ 下的坐标就是该向量的分量.因此, $e_{1},e_{2},\cdots,e_{n}$ 叫做 $R^{n}$ 中的自然基.

例19 设

$$
\boldsymbol {A} = (\boldsymbol {a} _ {1}, \boldsymbol {a} _ {2}, \boldsymbol {a} _ {3}) = \left( \begin{array}{r r r} 2 & 2 & - 1 \\ 2 & - 1 & 2 \\ - 1 & 2 & 2 \end{array} \right), \quad \boldsymbol {B} = (\boldsymbol {b} _ {1}, \boldsymbol {b} _ {2}) = \left( \begin{array}{r r} 1 & 4 \\ 0 & 3 \\ - 4 & 2 \end{array} \right).
$$

验证 $a_1, a_2, a_3$ 是 $\mathbb{R}^3$ 的一个基，并求 $b_1, b_2$ 在这个基下的坐标.

解 要证  $a_{1}, a_{2}, a_{3}$  是  $R^{3}$  的一个基, 只要证  $a_{1}, a_{2}, a_{3}$  线性无关, 即只要证  $A \sim E$ .

设 $b_{1} = x_{11}a_{1} + x_{21}a_{2} + x_{31}a_{3}, b_{2} = x_{12}a_{1} + x_{22}a_{2} + x_{32}a_{3}$，即

$$
(\boldsymbol {b} _ {1}, \boldsymbol {b} _ {2}) = (\boldsymbol {a} _ {1}, \boldsymbol {a} _ {2}, \boldsymbol {a} _ {3}) \left( \begin{array}{c c} x _ {1 1} & x _ {1 2} \\ x _ {2 1} & x _ {2 2} \\ x _ {3 1} & x _ {3 2} \end{array} \right),
$$

记作 B = AX.

对矩阵 $(A, B)$ 施行初等行变换，若 $A$ 能变为 $E$，则 $a_1, a_2, a_3$ 为 $\mathbb{R}^3$ 的一个基，且当 $A$ 变为 $E$ 时，$B$ 变为 $X = A^{-1}B$.

$$
(A, B) = \left( \begin{array}{r r r r r} 2 & 2 & - 1 & 1 & 4 \\ 2 & - 1 & 2 & 0 & 3 \\ - 1 & 2 & 2 & - 4 & 2 \end{array} \right) ^ {\frac {1}{3} \underbrace {(r _ {1} + r _ {2} + r _ {3})} _ {r _ {2} - 2 r _ {1}}} \left( \begin{array}{r r r r r} 1 & 1 & 1 & - 1 & 3 \\ 0 & - 3 & 0 & 2 & - 3 \\ 0 & 3 & 3 & - 5 & 5 \end{array} \right)
$$

98

---

§4 向量空间

$$
\frac {r _ {2} \div (- 3)}{r _ {3} \div 3} \left( \begin{array}{c c c c c} 1 & 1 & 1 & - 1 & 3 \\ 0 & 1 & 0 & - \frac {2}{3} & 1 \\ 0 & 1 & 1 & - \frac {5}{3} & \frac {5}{3} \end{array} \right) \overbrace {r _ {3} - r _ {2}} ^ {r _ {1} - r _ {3}} \left( \begin{array}{c c c c c} 1 & 0 & 0 & \frac {2}{3} & \frac {4}{3} \\ 0 & 1 & 0 & - \frac {2}{3} & 1 \\ 0 & 0 & 1 & - 1 & \frac {2}{3} \end{array} \right).
$$

因有 $A \sim E$，故 $a_1, a_2, a_3$ 为 $\mathbb{R}^3$ 的一个基，且

$$
(\boldsymbol {b} _ {1}, \boldsymbol {b} _ {2}) = (\boldsymbol {a} _ {1}, \boldsymbol {a} _ {2}, \boldsymbol {a} _ {3}) \left( \begin{array}{c c} \frac {2}{3} & \frac {4}{3} \\ - \frac {2}{3} & 1 \\ - 1 & \frac {2}{3} \end{array} \right),
$$

即 $b_{1}, b_{2}$ 在基 $a_{1}, a_{2}, a_{3}$ 中的坐标依次为

$$
\frac {2}{3}, - \frac {2}{3}, - 1 \quad \text {和} \quad \frac {4}{3}, 1, \frac {2}{3}.
$$

定义 10 在向量空间 V 中取定两个基  $a_{1}, a_{2}, \cdots, a_{n}$  与  $b_{1}, b_{2}, \cdots, b_{n}$ . 设  $b_{i} = p_{1i}a_{1} + p_{2i}a_{2} + \cdots + p_{ni}a_{n}$  ( $i = 1, 2, \cdots, n$ ), 则

$$
\left\{ \begin{array}{l} \boldsymbol {b} _ {1} = p _ {1 1} \boldsymbol {a} _ {1} + p _ {2 1} \boldsymbol {a} _ {2} + \dots + p _ {n 1} \boldsymbol {a} _ {n}, \\ \boldsymbol {b} _ {2} = p _ {1 2} \boldsymbol {a} _ {1} + p _ {2 2} \boldsymbol {a} _ {2} + \dots + p _ {n 2} \boldsymbol {a} _ {n}, \\ \dots \dots \\ \dot {\boldsymbol {b}} _ {n} = p _ {1 n} \boldsymbol {a} _ {1} + p _ {2 n} \boldsymbol {a} _ {2} + \dots + p _ {n n} \boldsymbol {a} _ {n}, \end{array} \right.
$$

利用矩阵,也可形式地写为

$$
(\boldsymbol {b} _ {1}, \boldsymbol {b} _ {2}, \dots , \boldsymbol {b} _ {n}) = (\boldsymbol {a} _ {1}, \boldsymbol {a} _ {2}, \dots , \boldsymbol {a} _ {n}) \boldsymbol {P},
$$

这里

$$
\boldsymbol {P} = \left( \begin{array}{c c c c} p _ {1 1} & p _ {1 2} & \dots & p _ {1 n} \\ p _ {2 1} & p _ {2 2} & \dots & p _ {2 n} \\ \vdots & \vdots & & \vdots \\ p _ {n 1} & p _ {n 2} & \dots & p _ {n n} \end{array} \right),
$$

此式即称为基变换公式,矩阵 P 称为从基  $a_{1}, a_{2}, \cdots, a_{n}$  到基  $b_{1}, b_{2}, \cdots, b_{n}$  的过渡矩阵.

定义11 设 $a_1, a_2, \cdots, a_n$ 与 $b_1, b_2, \cdots, b_n$ 是向量空间 $V$ 的两个基. $\forall \alpha \in V$, 设 $\alpha$ 在基 $a_1, a_2, \cdots, a_n$ 下的坐标为 $x$, 在基 $b_1, b_2, \cdots, b_n$ 下的坐标为 $y$, 即

$$
\boldsymbol {\alpha} = x _ {1} \boldsymbol {a} _ {1} + x _ {2} \boldsymbol {a} _ {2} + \dots + x _ {n} \boldsymbol {a} _ {n} = (\boldsymbol {a} _ {1}, \boldsymbol {a} _ {2}, \dots , \boldsymbol {a} _ {n}) \boldsymbol {x}, \quad \boldsymbol {x} = \left( \begin{array}{c} x _ {1} \\ x _ {2} \\ \vdots \\ x _ {n} \end{array} \right),
$$

考研电子书网站:www.pdf2book.com

99

---

第4章 向量组的线性相关性

$$
\boldsymbol {\alpha} = y _ {1} \boldsymbol {b} _ {1} + y _ {2} \boldsymbol {b} _ {2} + \dots + y _ {n} \boldsymbol {b} _ {n} = (\boldsymbol {b} _ {1}, \boldsymbol {b} _ {2}, \dots , \boldsymbol {b} _ {n}) \boldsymbol {y}, \quad \boldsymbol {y} = \left( \begin{array}{c} y _ {1} \\ y _ {2} \\ \vdots \\ y _ {n} \end{array} \right).
$$

若从  $a_{1}, a_{2}, \cdots, a_{n}$  到  $b_{1}, b_{2}, \cdots, b_{n}$  的过渡矩阵为 P，则

$$
\boldsymbol {\alpha} = (\boldsymbol {b} _ {1}, \boldsymbol {b} _ {2}, \dots , \boldsymbol {b} _ {n}) \boldsymbol {y} = (\boldsymbol {a} _ {1}, \boldsymbol {a} _ {2}, \dots , \boldsymbol {a} _ {n}) \boldsymbol {P} \boldsymbol {y},
$$

从而 x = Py，此即称为坐标变换公式。

例20 在 $\mathbb{R}^3$ 中取定一个基 $a_1, a_2, a_3$，再取一个新基 $b_1, b_2, b_3$，设 $A = (a_1, a_2, a_3)$，$B = (b_1, b_2, b_3)$. 求从基 $a_1, a_2, a_3$ 到基 $b_1, b_2, b_3$ 的过渡矩阵 $P$，并求向量 $\alpha (\alpha \in \mathbb{R}^3)$ 在两个基下的坐标变换公式.

解 因

$$
(\boldsymbol {a} _ {1}, \boldsymbol {a} _ {2}, \boldsymbol {a} _ {3}) = (\boldsymbol {e} _ {1}, \boldsymbol {e} _ {2}, \boldsymbol {e} _ {3}) \boldsymbol {A}, \quad (\boldsymbol {e} _ {1}, \boldsymbol {e} _ {2}, \boldsymbol {e} _ {3}) = (\boldsymbol {a} _ {1}, \boldsymbol {a} _ {2}, \boldsymbol {a} _ {3}) \boldsymbol {A} ^ {- 1}.
$$

故

$$
(\boldsymbol {b} _ {1}, \boldsymbol {b} _ {2}, \boldsymbol {b} _ {3}) = (\boldsymbol {e} _ {1}, \boldsymbol {e} _ {2}, \boldsymbol {e} _ {3}) \boldsymbol {B} = (\boldsymbol {a} _ {1}, \boldsymbol {a} _ {2}, \boldsymbol {a} _ {3}) \boldsymbol {A} ^ {- 1} \boldsymbol {B},
$$

即基变换公式为

$$
(\boldsymbol {b} _ {1}, \boldsymbol {b} _ {2}, \boldsymbol {b} _ {3}) = (\boldsymbol {a} _ {1}, \boldsymbol {a} _ {2}, \boldsymbol {a} _ {3}) \boldsymbol {P},
$$

其中矩阵  $P=A^{-1}B$  即为从旧基到新基的过渡矩阵. 公众号:旗胜考研

设向量 $\alpha$ 在旧基和新基下的坐标分别为 $y_{1}, y_{2}, y_{3}$ 和 $z_{1}, z_{2}, z_{3}$，即

$$
\boldsymbol {\alpha} = (\boldsymbol {a} _ {1}, \boldsymbol {a} _ {2}, \boldsymbol {a} _ {3}) \left( \begin{array}{l} y _ {1} \\ y _ {2} \\ y _ {3} \end{array} \right), \quad \boldsymbol {\alpha} = (\boldsymbol {b} _ {1}, \boldsymbol {b} _ {2}, \boldsymbol {b} _ {3}) \left( \begin{array}{l} z _ {1} \\ z _ {2} \\ z _ {3} \end{array} \right),
$$

故  $A\begin{pmatrix}y_{1}\\y_{2}\\y_{3}\end{pmatrix}=B\begin{pmatrix}z_{1}\\z_{2}\\z_{3}\end{pmatrix}$ ，得  $\begin{pmatrix}z_{1}\\z_{2}\\z_{3}\end{pmatrix}=B^{-1}A\begin{pmatrix}y_{1}\\y_{2}\\y_{3}\end{pmatrix}$ ，即

$$
\left( \begin{array}{c} z _ {1} \\ z _ {2} \\ z _ {3} \end{array} \right) = \boldsymbol {P} ^ {- 1} \left( \begin{array}{c} y _ {1} \\ y _ {2} \\ y _ {3} \end{array} \right),
$$

这就是从旧坐标到新坐标的坐标变换公式.

例21 设 $\mathbb{R}^3$ 的两个基I和II为

$$
\mathrm{I}: \boldsymbol {a} _ {1} = \left( \begin{array}{l} 1 \\ 0 \\ 0 \end{array} \right), \boldsymbol {a} _ {2} = \left( \begin{array}{l} 1 \\ 1 \\ 0 \end{array} \right), \boldsymbol {a} _ {3} = \left( \begin{array}{l} 1 \\ 1 \\ 1 \end{array} \right); \quad \mathrm{II}: \boldsymbol {b} _ {1} = \left( \begin{array}{l} 1 \\ 2 \\ 1 \end{array} \right), \boldsymbol {b} _ {2} = \left( \begin{array}{l} 2 \\ 3 \\ 3 \end{array} \right), \boldsymbol {b} _ {3} = \left( \begin{array}{l} 3 \\ 7 \\ 1 \end{array} \right),
$$

(1) 求由基Ⅰ到基Ⅱ的过渡矩阵；

100

---

§ 5 线性方程组的解的结构

(2) 设向量 c 在基Ⅰ下的坐标为 -2, 1, 2, 求 c 在基Ⅱ下的坐标.

解（1）由基I到基Ⅱ的过渡矩阵 $P = A^{-1}B$ ，其中 $A = (a_{1},a_{2},a_{3}),B = (b_{1},b_{2},b_{3})$ .用矩阵的初等行变换把矩阵 $(A,B)$ 中的 $A$ 变成 $\pmb{E}$ ，则 $\pmb{B}$ 相应地变成 $A^{-1}B$

$$
\begin{array}{l} (A, B) = (a _ {1}, a _ {2}, a _ {3}, b _ {1}, b _ {2}, b _ {3}) \\ = \left( \begin{array}{c c c c c c} 1 & 1 & 1 & 1 & 2 & 3 \\ 0 & 1 & 1 & 2 & 3 & 7 \\ 0 & 0 & 1 & 1 & 3 & 1 \end{array} \right) \stackrel {{r}} {{\sim}} \left( \begin{array}{c c c c c c} 1 & 0 & 0 & - 1 & - 1 & - 4 \\ 0 & 1 & 0 & 1 & 0 & 6 \\ 0 & 0 & 1 & 1 & 3 & 1 \end{array} \right) \\ \end{array}
$$

于是,过渡矩阵  $P=\begin{pmatrix}-1&-1&-4\\1&0&6\\1&3&1\end{pmatrix}$ .

(2) 易求得  $P^{-1}=\begin{pmatrix}-18&-11&-6\\5&3&2\\3&2&1\end{pmatrix}$ ，故向量 c 在基Ⅱ下的坐标（向量）为

$$
\boldsymbol {P} ^ {- 1} \left( \begin{array}{c} - 2 \\ 1 \\ 2 \end{array} \right) = \left( \begin{array}{c c c} - 1 8 & - 1 1 & - 6 \\ 5 & 3 & 2 \\ 3 & 2 & 1 \end{array} \right) \left( \begin{array}{c} - 2 \\ 1 \\ 2 \end{array} \right) = \left( \begin{array}{c} 1 3 \\ - 3 \\ - 2 \end{array} \right),
$$

即向量 $c$ 在基Ⅱ下的坐标为13,-3,-2.

## § 5 线性方程组的解的结构

在上一章中,我们已经介绍了用矩阵的初等行变换解线性方程组的方法,并建立了两个重要定理,即

（1）n 个未知数的齐次线性方程组 Ax=0 有非零解的充分必要条件是系数矩阵的秩  $R(A)<n$ .
(2) $n$ 个未知数的非齐次线性方程组 $Ax = b$ 有解的充分必要条件是系数矩阵 $A$ 的秩等于增广矩阵 $\pmb{B}$ 的秩, 且当 $R(A) = R(B) = n$ 时方程组有惟一解, 当 $R(A) = R(B) = r < n$ 时方程组有无限多个解.

下面我们用向量组线性相关性的理论来讨论线性方程组的解.

## 一、齐次线性方程组

设有齐次线性方程组

考研电子书网站:www.pdf2book.com

101

---

第4章 向量组的线性相关性

$$
\left\{ \begin{array}{l} a _ {1 1} x _ {1} + a _ {1 2} x _ {2} + \dots + a _ {1 n} x _ {n} = 0, \\ a _ {2 1} x _ {1} + a _ {2 2} x _ {2} + \dots + a _ {2 n} x _ {n} = 0, \\ \dots \dots \\ a _ {m 1} x _ {1} + a _ {m 2} x _ {2} + \dots + a _ {m n} x _ {n} = 0, \end{array} \right. \tag {1}
$$

记

$$
\boldsymbol {A} = \left( \begin{array}{c c c c} a _ {1 1} & a _ {1 2} & \dots & a _ {1 n} \\ a _ {2 1} & a _ {2 2} & \dots & a _ {2 n} \\ \vdots & \vdots & & \vdots \\ a _ {m 1} & a _ {m 2} & \dots & a _ {m n} \end{array} \right), \quad \boldsymbol {x} = \left( \begin{array}{c} x _ {1} \\ x _ {2} \\ \vdots \\ x _ {n} \end{array} \right),
$$

则(1)式可写成

$$
\boldsymbol {A} \boldsymbol {x} = \boldsymbol {0}. \tag {2}
$$

若

$$
\boldsymbol {x} = \boldsymbol {\xi} _ {1} = \left( \begin{array}{c} \boldsymbol {\xi} _ {1 1} \\ \boldsymbol {\xi} _ {2 1} \\ \vdots \\ \boldsymbol {\xi} _ {n 1} \end{array} \right)
$$

是方程组(1)的解向量,它也就是方程(2)的解.

由本章例 15 知, 方程组(1)的解集 $S = \{x \mid Ax = 0\}$ 是一个向量空间. 只要找到向量空间的一个基, 就能精确描述该空间.

设 $S_0: \xi_1, \xi_2, \cdots, \xi_t$ 为 $S$ 的一个基，则 $x = k_1\xi_1 + k_2\xi_2 + \cdots + k_t\xi_t (k_1, k_2, \cdots, k_t \in \mathbb{R})$ 就是方程(2)的通解.

齐次线性方程组的解空间的一个基称为该齐次线性方程组的基础解系.由上面的讨论可知,要求齐次线性方程组的通解,只需求出它的基础解系.

上一章我们用初等行变换的方法求线性方程组的通解,下面我们用同一方法来求齐次线性方程组的基础解系.

设方程组(1)的系数矩阵 $\pmb{A}$ 的秩为 $r$ ，并不妨设 $\pmb{A}$ 的前 $r$ 个列向量线性无关，于是$\pmb{A}$ 的行最简形矩阵为.

$$
\boldsymbol {B} = \left( \begin{array}{c c c c c c} 1 & \dots & 0 & b _ {1 1} & \dots & b _ {1, n - r} \\ \vdots & & \vdots & \vdots & & \vdots \\ 0 & \dots & 1 & b _ {r 1} & \dots & b _ {r, n - r} \\ 0 & & & \dots & & 0 \\ \vdots & & & & & \vdots \\ 0 & & & \dots & & 0 \end{array} \right),
$$

102

---

§5 线性方程组的解的结构

与 $\pmb{B}$ 对应，即有方程组

$$
\left\{ \begin{array}{l} x _ {1} = - b _ {1 1} x _ {r + 1} - \dots - b _ {1, n - r} x _ {n}, \\ \dots \dots \\ x _ {r} = - b _ {r 1} x _ {r + 1} - \dots - b _ {r, n - r} x _ {n}, \end{array} \right. \tag {3}
$$

把 $x_{r + 1}, x_{r + 2}, \dots, x_n$ 作为自由未知数，并令它们依次等于 $c_1, c_2, \dots, c_{n - r}$，可得方程组（1）的通解

$$
\left( \begin{array}{c} x _ {1} \\ \vdots \\ x _ {r} \\ x _ {r + 1} \\ x _ {r + 2} \\ \vdots \\ x _ {n} \end{array} \right) = c _ {1} \left( \begin{array}{c} - b _ {1 1} \\ \vdots \\ - b _ {r 1} \\ 1 \\ 0 \\ \vdots \\ 0 \end{array} \right) + c _ {2} \left( \begin{array}{c} - b _ {1 2} \\ \vdots \\ - b _ {r 2} \\ 0 \\ 1 \\ \vdots \\ 0 \end{array} \right) + \dots + c _ {n - r} \left( \begin{array}{c} - b _ {1, n - r} \\ \vdots \\ - b _ {r, n - r} \\ 0 \\ 0 \\ \vdots \\ 1 \end{array} \right).
$$

把上式记作

$$
x = c _ {1} \xi_ {1} + c _ {2} \xi_ {2} + \dots + c _ {n - r} \xi_ {n - r},
$$

可知解空间 $S$ 中的任一向量 $\pmb{x}$ 能由 $\pmb{\xi}_{1},\pmb{\xi}_{2},\dots ,\pmb{\xi}_{n - r}$ 线性表示，又因为矩阵 $(\pmb{\xi}_1,$ $\pmb{\xi}_2,\dots ,\pmb{\xi}_{n - r})$ 中有 $n - r$ 阶子式 $|E_{n - r}|\neq 0$ ，故 $R(\pmb {\xi}_1,\pmb {\xi}_2,\dots ,\pmb {\xi}_{n - r}) = n - r$ ，所以 $\pmb {\xi}_1,\pmb {\xi}_2,\dots ,\pmb {\xi}_{n - r}$ 线性无关.根据基的定义，即知 $\pmb {\xi}_1,\pmb {\xi}_2,\dots ,\pmb {\xi}_{n - r}$ 是解空间 $S$ 的一个基，即 $\pmb {\xi}_1,\pmb {\xi}_2,\dots ,\pmb {\xi}_{n - r}$ 是方程组(1)的基础解系.

在上面的讨论中,我们先求出齐次线性方程组的通解,再从通解求得基础解系.其实我们也可先求基础解系,再写出通解.这只需在得到方程组(3)以后,令自由未知数 $x_{r+1},x_{r+2},\cdots,x_{n}$ 取下列n-r组数

$$
\left( \begin{array}{c} 1 \\ 0 \\ \vdots \\ 0 \end{array} \right), \quad \left( \begin{array}{c} 0 \\ 1 \\ \vdots \\ 0 \end{array} \right), \quad \dots , \quad \left( \begin{array}{c} 0 \\ 0 \\ \vdots \\ 1 \end{array} \right),
$$

由(3)即可得 $\begin{pmatrix}x_{1}\\x_{2}\\\vdots\\x_{r}\end{pmatrix}$ 依次为

考研电子书网站:www.pdf2book.com

103

---

第4章 向量组的线性相关性

$$
\left( \begin{array}{c} - b _ {1 1} \\ - b _ {2 1} \\ \vdots \\ - b _ {r 1} \end{array} \right), \quad \left( \begin{array}{c} - b _ {1 2} \\ - b _ {2 2} \\ \vdots \\ - b _ {r 2} \end{array} \right), \quad \dots , \quad \left( \begin{array}{c} - b _ {1, n - r} \\ - b _ {2, n - r} \\ \vdots \\ - b _ {r, n - r} \end{array} \right),
$$

合起来便得基础解系

$$
\boldsymbol {\xi} _ {1} = \left( \begin{array}{c} - b _ {1 1} \\ - b _ {2 1} \\ \vdots \\ - b _ {r 1} \\ 1 \\ 0 \\ \vdots \\ 0 \end{array} \right), \quad \boldsymbol {\xi} _ {2} = \left( \begin{array}{c} - b _ {1 2} \\ - b _ {2 2} \\ \vdots \\ - b _ {r 2} \\ 0 \\ 1 \\ \vdots \\ 0 \end{array} \right), \quad \dots , \quad \boldsymbol {\xi} _ {n - r} = \left( \begin{array}{c} - b _ {1, n - r} \\ - b _ {2, n - r} \\ \vdots \\ - b _ {r, n - r} \\ 0 \\ 0 \\ \vdots \\ 1 \end{array} \right).
$$

依据以上的讨论,还可推得

定理7 设 $m \times n$ 矩阵 $\pmb{A}$ 的秩 $R(A) = r$，则 $n$ 元齐次线性方程组 $Ax = 0$ 的解空间 $S$ 的维数 $\dim S = n - r$（即该齐次线性方程组的自由未知数的个数）.

当 $R(A) = n$ 时, 方程(1)只有零解, 没有基础解系 (此时解空间 $S$ 只含一个零向量); 当 $R(A) = r < n$ 时, 由定理7可知方程组(1)的基础解系含 $n - r$ 个向量. 因此, 由最大无关组的性质可知, 方程组(1)的任何 $n - r$ 个线性无关的解都可构成它的基础解系. 并由此可知齐次线性方程组的基础解系并不是惟一的, 它的通解的形式也不是惟一的.

例22 求齐次线性方程组

$$
\left\{ \begin{array}{c} x _ {1} + x _ {2} - x _ {3} - x _ {4} = 0, \\ 2 x _ {1} - 5 x _ {2} + 3 x _ {3} + 2 x _ {4} = 0, \\ 7 x _ {1} - 7 x _ {2} + 3 x _ {3} + x _ {4} = 0 \end{array} \right.
$$

的基础解系与通解.

解 对系数矩阵 A 作初等行变换变为行最简形矩阵,有

$$
\boldsymbol {A} = \left( \begin{array}{c c c c} 1 & 1 & - 1 & - 1 \\ 2 & - 5 & 3 & 2 \\ 7 & - 7 & 3 & 1 \end{array} \right) \xrightarrow [ r _ {3} - 7 r _ {1} ]{r _ {2} - 2 r _ {1}} \left( \begin{array}{c c c c} 1 & 1 & - 1 & - 1 \\ 0 & - 7 & 5 & 4 \\ 0 & - 1 4 & 1 0 & 8 \end{array} \right)
$$

104

---

§ 5 线性方程组的解的结构

$$
\underbrace {r _ {3} - 2 r _ {2}} _ {\text {r} _ {1} - r _ {2}} \left( \begin{array}{c c c c} 1 & 1 & - 1 & - 1 \\ 0 & - 7 & 5 & 4 \\ 0 & 0 & 0 & 0 \end{array} \right) \underbrace {r _ {2} \times \left(- \frac {1}{7}\right)} _ {\text {r} _ {1} - r _ {2}} \left( \begin{array}{c c c c} 1 & 0 & - \frac {2}{7} & - \frac {3}{7} \\ 0 & 1 & - \frac {5}{7} & - \frac {4}{7} \\ 0 & 0 & 0 & 0 \end{array} \right),
$$

便得

$$
\left\{ \begin{array}{l} x _ {1} = \frac {2}{7} x _ {3} + \frac {3}{7} x _ {4}, \\ x _ {2} = \frac {5}{7} x _ {3} + \frac {4}{7} x _ {4}, \end{array} \right. \tag {*}.
$$

令 $\begin{pmatrix}x_{3}\\x_{4}\end{pmatrix}$ 取 $\begin{pmatrix}1\\0\end{pmatrix}$ 及 $\begin{pmatrix}0\\1\end{pmatrix}$ ，则对应的 $\begin{pmatrix}x_{1}\\x_{2}\end{pmatrix}$ 为 $\begin{pmatrix}\frac{2}{7}\\ \frac{5}{7}\end{pmatrix}$ 及 $\begin{pmatrix}\frac{3}{7}\\ \frac{4}{7}\end{pmatrix}$ ，即得基础解系

$$
\boldsymbol {\xi} _ {1} = \left( \begin{array}{c} \frac {2}{7} \\ \frac {5}{7} \\ 1 \\ 0 \end{array} \right), \quad \boldsymbol {\xi} _ {2} = \left( \begin{array}{c} \frac {3}{7} \\ \frac {4}{7} \\ 0 \\ 1 \end{array} \right),
$$

并由此写出通解

$$
\left( \begin{array}{c} x _ {1} \\ x _ {2} \\ x _ {3} \\ x _ {4} \end{array} \right) = c _ {1} \left( \begin{array}{c} \frac {2}{7} \\ \frac {5}{7} \\ 1 \\ 0 \end{array} \right) + c _ {2} \left( \begin{array}{c} \frac {3}{7} \\ \frac {4}{7} \\ 0 \\ 1 \end{array} \right) \quad (c _ {1}, c _ {2} \in \mathbb {R}).
$$

上一章中线性方程组的解法是从（\*）式写出通解（从通解的表达式即可得基础解系），现在从（\*）式先取基础解系，再写出通解，两种解法其实没有多少差别。

根据 $(*)$ 式,如果取 $\begin{pmatrix}x_{3}\\x_{4}\end{pmatrix}$ 为 $\begin{pmatrix}1\\1\end{pmatrix}$ 及 $\begin{pmatrix}1\\-1\end{pmatrix}$ ,对应的 $\begin{pmatrix}x_{1}\\x_{2}\end{pmatrix}$ 为

$$
\left( \begin{array}{c} {{\frac {5}{7}}} \\ {{\frac {9}{7}}} \end{array} \right) \quad \text {及} \quad \left( \begin{array}{c} {{- \frac {1}{7}}} \\ {{\frac {1}{7}}} \end{array} \right),
$$

即得不同的基础解系

考研电子书网站:www.pdf2book.com

105

---

第4章 向量组的线性相关性

$$
\boldsymbol {\eta} _ {1} = \left( \begin{array}{c} \frac {5}{7} \\ \frac {9}{7}. \\ 1 \\ 1 \end{array} \right), \quad \boldsymbol {\eta} _ {2} = \left( \begin{array}{c} - \frac {1}{7} \\ \frac {1}{7} \\ 1 \\ - 1 \end{array} \right),
$$

从而得通解

$$
\left( \begin{array}{c} x _ {1} \\ x _ {2} \\ x _ {3} \\ x _ {4} \end{array} \right) = k _ {1} \left( \begin{array}{c} \frac {5}{7} \\ \frac {9}{7} \\ 1 \\ 1 \end{array} \right) + k _ {2} \left( \begin{array}{c} - \frac {1}{7} \\ \frac {1}{7} \\ 1 \\ - 1 \end{array} \right) \quad (k _ {1}, k _ {2} \in \mathbb {R}).
$$

显然 $\pmb{\xi}_1, \pmb{\xi}_2$ 与 $\pmb{\eta}_1, \pmb{\eta}_2$ 是等价的，两个通解虽然形式不一样，但都含两个任意常数，且都可表示方程组的任一解.

上述解法中,由于行最简形矩阵的结构,将 $x_{3},x_{4}$ 选为自由未知数最方便.如果要选 $x_{1},x_{2}$ 为自由未知数,那么就不能采用上述化系数矩阵为行最简形矩阵的“标准程序”,而要稍作变化,具体如下:

$$
\boldsymbol {A} = \left( \begin{array}{c c c c} 1 & 1 & - 1 & - 1 \\ 2 & - 5 & 3 & 2 \\ 7 & - 7 & 3 & 1 \end{array} \right) \underbrace {\frac {r _ {2} + 2 r _ {1}}{r _ {3} + r _ {1}}} _ {r _ {1} \times (- 1)} \left( \begin{array}{c c c c} - 1 & - 1 & 1 & 1 \\ 4 & - 3 & 1 & 0 \\ 8 & - 6 & 2 & 0 \end{array} \right) \underbrace {\frac {r _ {3} - 2 r _ {2}}{r _ {1} - r _ {2}}} _ {} \left( \begin{array}{c c c c} - 5 & 2 & 0 & 1 \\ 4 & - 3 & 1 & 0 \\ 0 & 0 & 0 & 0 \end{array} \right),
$$

上式最后一个矩阵虽不是行最简形矩阵,但也具备行最简形矩阵的功能.按照这个矩阵,取 $x_{1},x_{2}$ 为自由未知数,便可写出通解

$$
\left\{ \begin{array}{l l} x _ {3} = - 4 x _ {1} + 3 x _ {2}, \\ x _ {4} = 5 x _ {1} - 2 x _ {2} \end{array} \right. \quad (x _ {1}, x _ {2} \text {可任意取值}),
$$

即

$$
\left( \begin{array}{c} x _ {1} \\ x _ {2} \\ x _ {3} \\ x _ {4} \end{array} \right) = c _ {1} \left( \begin{array}{c} 1 \\ 0 \\ - 4 \\ 5 \end{array} \right) + c _ {2} \left( \begin{array}{c} 0 \\ 1 \\ 3 \\ - 2 \end{array} \right) \quad (c _ {1}, c _ {2} \in \mathbb {R}),
$$

而对应的基础解系为

$$
\left( \begin{array}{c} 1 \\ 0 \\ - 4 \\ 5 \end{array} \right), \quad \left( \begin{array}{c} 0 \\ 1 \\ 3 \\ - 2 \end{array} \right).
$$

106

---

§5 线性方程组的解的结构

定理 7 不仅是线性方程组各种解法的理论基础,而且在讨论向量组的线性相关性时也很有用.

例23 设 $A_{m \times n} B_{n \times l} = O$，证明 $R(A) + R(B) \leqslant n$.

证 记  $\boldsymbol{B}=(\boldsymbol{b}_{1},\boldsymbol{b}_{2},\cdots,\boldsymbol{b}_{l})$ ，则

$$
A (b _ {1}, b _ {2}, \dots , b _ {l}) = (0, 0, \dots , 0),
$$

即

$$
A b _ {i} = 0 \quad (i = 1, 2, \dots , l),
$$

表明矩阵 B 的 l 个列向量都是齐次方程组 Ax=0 的解. 记方程组 Ax=0 的解空间为 S, 由  $b_{i} \in S$ , 知有  $R(\boldsymbol{b}_{1}, \boldsymbol{b}_{2}, \cdots, \boldsymbol{b}_{l}) \leqslant \dim S$ , 而由定理 7 有  $\dim S = n - R(A)$ , 故  $R(A) + R(B) \leqslant n$ .

例24 设 $n$ 元齐次线性方程组 $Ax = 0$ 与 $Bx = 0$ 同解，证明 $R(A) = R(B)$.

证 由于方程组 Ax=0 与 Bx=0 有相同的解空间, 设为 S, 则由定理 7 即有  $\dim S = n - R(A) = n - R(B)$ . 因此  $R(A) = \dot{R}(B)$ .

例25 证明 $R(\mathbf{A}^{\mathrm{T}}\mathbf{A}) = R(\mathbf{A}).$

证 根据例24的结论,只需证明齐次方程组 $Ax = 0$ 与 $(A^{\mathrm{T}}A)x = 0$ 同解:

若 $x$ 满足 $Ax = 0$ ，则有 $A^{\mathrm{T}}(Ax) = 0$ ，即 $(A^{\mathrm{T}}A)x = 0;$

若 $x$ 满足 $(A^{\mathrm{T}}A)x = 0$ ，则 $x^{\mathrm{T}}(A^{\mathrm{T}}A)x = 0$ ，即 $(Ax)^{\mathrm{T}}(Ax) = 0$ ，从而 $Ax = 0$ （参见第2章例19).

综上可知方程组 $Ax = 0$ 与 $(A^{\mathrm{T}}A)x = 0$ 同解，因此 $R(A^{\mathrm{T}}A) = R(A)$.

## 二、非齐次线性方程组

设有非齐次线性方程组

$$
\left\{ \begin{array}{l} a _ {1 1} x _ {1} + a _ {1 2} x _ {2} + \dots + a _ {1 n} x _ {n} = b _ {1}, \\ a _ {2 1} x _ {1} + a _ {2 2} x _ {2} + \dots + a _ {2 n} x _ {n} = b _ {2}, \\ \dots \dots \\ a _ {m 1} x _ {1} + a _ {m 2} x _ {2} + \dots + a _ {m n} x _ {n} = b _ {m}, \end{array} \right. \tag {4}
$$

它也可写作向量方程

$$
A x = b, \tag {5}
$$

向量方程(5)的解也就是方程组(4)的解向量,它具有

性质1 设 $x = \eta_{1}$ 及 $x = \eta_{2}$ 都是向量方程(5)的解, 则 $x = \eta_{1} - \eta_{2}$ 为对应的齐次线性方程组

$$
A x = 0 \tag {6}
$$

的解.

证因

$$
A (\boldsymbol {\eta} _ {1} - \boldsymbol {\eta} _ {2}) = A \boldsymbol {\eta} _ {1} - A \boldsymbol {\eta} _ {2} = b - b = 0,
$$

考研电子书网站:www.pdf2book.com

107

---

第4章 向量组的线性相关性

即  $x=\eta_{1}-\eta_{2}$  满足方程(6).

证毕

性质2 设 $x = \eta$ 是方程(5)的解, $x = \xi$ 是方程(6)的解, 则 $x = \xi + \eta$ 仍是方程(5)的解.

证因

$$
A (\xi + \eta) = A \xi + A \eta = 0 + b = b,
$$

即  $x=\xi+\eta$  满足方程(5).

证毕

于是,如果求得方程(5)的一个解  $\eta^{*}$  (称为特解),那么方程(5)的通解为

$$
\boldsymbol {x} = k _ {1} \boldsymbol {\xi} _ {1} + k _ {2} \boldsymbol {\xi} _ {2} + \dots + k _ {n - r} \boldsymbol {\xi} _ {n - r} + \boldsymbol {\eta} ^ {*} \quad (k _ {1}, k _ {2}, \dots , k _ {n - r} \in \mathbb {R}),
$$

其中  $\xi_{1},\xi_{2},\cdots,\xi_{n-r}$  是方程(6)的基础解系.

事实上,由性质2知上式右端向量总是方程(5)的解;反过来,设 $x^{0}$ 为方程(5)的任一解,由性质1知 $x^{0}-\eta^{*}$ 是方程(6)的解,从而可由其基础解系线性表示为

$$
x ^ {0} - \eta^ {*} = k _ {1} ^ {0} \xi_ {1} + k _ {2} ^ {0} \xi_ {2} + \dots + k _ {n - r} ^ {0} \xi_ {n - r},
$$

即

$$
x ^ {0} = \eta^ {*} + k _ {1} ^ {0} \xi_ {1} + k _ {2} ^ {0} \xi_ {2} + \dots + k _ {n - r} ^ {0} \xi_ {n - r}.
$$

至此我们已得到了非齐次线性方程组的解的结构:

非齐次方程组的通解 $=$ 对应的齐次方程组的通解 $+$ 非齐次方程组的一个特解.

例26 求解方程组

$$
\left\{ \begin{array}{l} x _ {1} - x _ {2} - x _ {3} + x _ {4} = 0, \\ x _ {1} - x _ {2} + x _ {3} - 3 x _ {4} = 1, \\ x _ {1} - x _ {2} - 2 x _ {3} + 3 x _ {4} = - \frac {1}{2}. \end{array} \right.
$$

解 对增广矩阵 $\pmb{B}$ 施行初等行变换:

$$
\boldsymbol {B} = \left( \begin{array}{c c c c c} 1 & - 1 & - 1 & 1 & 0 \\ 1 & - 1 & 1 & - 3 & 1 \\ 1 & - 1 & - 2 & 3 & \frac {1}{2} \end{array} \right) \xrightarrow [ r _ {3} - r _ {1} ]{r _ {2} - r _ {1}} \left( \begin{array}{c c c c c} 1 & - 1 & - 1 & 1 & 0 \\ 0 & 0 & 2 & - 4 & 1 \\ 0 & 0 & - 1 & 2 & \frac {1}{2} \end{array} \right)
$$

$$
\overbrace {r _ {2} \times \frac {1}{2}} ^ {r _ {1} - r _ {3}} \left( \begin{array}{c c c c c} 1 & - 1 & 0 & - 1 & \frac {1}{2} \\ 0 & 0 & 1 & - 2 & \frac {1}{2} \\ 0 & 0 & 0 & 0 & 0 \end{array} \right),
$$

可见 $R(A) = R(B) = 2$ ，故方程组有解，并有

$$
\left\{ \begin{array}{l} x _ {1} = x _ {2} + x _ {4} + \frac {1}{2}, \\ x _ {3} = 2 x _ {4} + \frac {1}{2}. \end{array} \right.
$$

108

---

习题四

取 $x_{2} = x_{4} = 0$ ，则 $x_{1} = x_{3} = \frac{1}{2}$ 即得方程组的一个解

$$
\boldsymbol {\eta} ^ {*} = \left( \begin{array}{c} \frac {1}{2} \\ 0 \\ \frac {1}{2} \\ 0 \end{array} \right),
$$

在对应的齐次线性方程组 $\left\{\begin{aligned}x_{1}&=x_{2}+x_{4},\\ x_{3}&=2x_{4}\end{aligned}\right.$ 中，取 $\begin{pmatrix}x_{2}\\ x_{4}\end{pmatrix}$ 为 $\begin{pmatrix}1\\ 0\end{pmatrix}$ 及 $\begin{pmatrix}0\\ 1\end{pmatrix}$ ，则 $\begin{pmatrix}x_{1}\\ x_{3}\end{pmatrix}$ 为 $\begin{pmatrix}1\\ 0\end{pmatrix}$ 及 $\begin{pmatrix}1\\ 2\end{pmatrix}$ ，
即得对应的齐次线性方程组的基础解系

$$
\boldsymbol {\xi} _ {1} = \left( \begin{array}{c} 1 \\ 1 \\ 0 \\ 0 \end{array} \right), \quad \boldsymbol {\xi} _ {2} = \left( \begin{array}{c} 1 \\ 0 \\ 2 \\ 1 \end{array} \right),
$$

于是所求通解为

$$
\left( \begin{array}{c} x _ {1} \\ x _ {2} \\ x _ {3} \\ x _ {4} \end{array} \right) = c _ {1} \left( \begin{array}{c} 1 \\ 1 \\ 0 \\ 0 \end{array} \right) + c _ {2} \left( \begin{array}{c} 1 \\ 0 \\ 2 \\ 1 \end{array} \right) + \left( \begin{array}{c} \frac {1}{2} \\ 0 \\ \frac {1}{2} \\ 0 \end{array} \right) \quad (c _ {1}, c _ {2} \in \mathbb {R}).
$$

## 习题四

1. 已知向量组

$$
A: \boldsymbol {a} _ {1} = \left( \begin{array}{c} 0 \\ 1 \\ 2 \\ 3 \end{array} \right), \boldsymbol {a} _ {2} = \left( \begin{array}{c} 3 \\ 0 \\ 1 \\ 2 \end{array} \right), \boldsymbol {a} _ {3} = \left( \begin{array}{c} 2 \\ 3 \\ 0 \\ 1 \end{array} \right); \quad B: \boldsymbol {b} _ {1} = \left( \begin{array}{c} 2 \\ 1 \\ 1 \\ 2 \end{array} \right), \boldsymbol {b} _ {2} = \left( \begin{array}{c} 0 \\ - 2 \\ 1 \\ 1 \end{array} \right), \boldsymbol {b} _ {3} = \left( \begin{array}{c} 4 \\ 4 \\ 1 \\ 3 \end{array} \right),
$$

证明向量组 B 能由向量组 A 线性表示,但向量组 A 不能由向量组 B 线性表示.

2. 已知向量组

$$
A: \boldsymbol {a} _ {1} = \left( \begin{array}{c} 0 \\ 1 \\ 1 \end{array} \right), \boldsymbol {a} _ {2} = \left( \begin{array}{c} 1 \\ 1 \\ 0 \end{array} \right); \quad B: \boldsymbol {b} _ {1} = \left( \begin{array}{c} - 1 \\ 0 \\ 1 \end{array} \right), \boldsymbol {b} _ {2} = \left( \begin{array}{c} 1 \\ 2 \\ 1 \end{array} \right), \boldsymbol {b} _ {3} = \left( \begin{array}{c} 3 \\ 2 \\ - 1 \end{array} \right),
$$

考研电子书网站:www.pdf2book.com

109

---

第 4 章 向量组的线性相关性

证明向量组 A 与向量组 B 等价.

3. 判定下列向量组是线性相关还是线性无关:

(1) $\begin{pmatrix}-1\\3\\1\end{pmatrix},\begin{pmatrix}2\\1\\0\end{pmatrix},\begin{pmatrix}1\\4\\1\end{pmatrix};$

(2) $\begin{pmatrix}2\\3\\0\end{pmatrix},\begin{pmatrix}-1\\4\\0\end{pmatrix},\begin{pmatrix}0\\0\\2\end{pmatrix}.$

4. 问 $a$ 取什么值时下列向量组线性相关？

$$
\boldsymbol {a} _ {1} = \left( \begin{array}{c} a \\ 1 \\ 1 \end{array} \right), \boldsymbol {a} _ {2} = \left( \begin{array}{c} 1 \\ a \\ - 1 \end{array} \right), \boldsymbol {a} _ {3} = \left( \begin{array}{c} 1 \\ - 1 \\ a \end{array} \right).
$$

5. 设矩阵 $A = a a^{\mathrm{T}} + b b^{\mathrm{T}}$，这里 $a, b$ 为 $n$ 维列向量。证明:

(1)  $R(A) \leqslant 2;$
(2) 当 a, b 线性相关时,  $R(A) \leqslant 1$ .
6. 设  $a_{1}, a_{2}$  线性无关,  $a_{1} + b, a_{2} + b$  线性相关, 求向量 b 用  $a_{1}, a_{2}$  线性表示的表示式.
7. 设  $a_{1}, a_{2}$  线性相关,  $b_{1}, b_{2}$  也线性相关, 问  $a_{1} + b_{1}, a_{2} + b_{2}$  是否一定线性相关? 试举例说明之.
8. 举例说明下列各命题是错误的:

(1) 若向量组  $a_{1}, a_{2}, \cdots, a_{m}$  是线性相关的，则  $a_{1}$  可由  $a_{2}, \cdots, a_{m}$  线性表示；

(2) 若有不全为 0 的数  $\lambda_{1}, \lambda_{2}, \cdots, \lambda_{m}$ ，使

$$
\lambda_ {1} \boldsymbol {a} _ {1} + \lambda_ {2} \boldsymbol {a} _ {2} + \dots + \lambda_ {m} \boldsymbol {a} _ {m} + \lambda_ {1} \boldsymbol {b} _ {1} + \lambda_ {2} \boldsymbol {b} _ {2} + \dots + \lambda_ {m} \boldsymbol {b} _ {m} = \mathbf {0}
$$

成立，则 $a_{1},a_{2},\cdots,a_{m}$ 线性相关， $b_{1},b_{2},\cdots,b_{m}$ 亦线性相关；

(3) 若只有当  $\lambda_{1}, \lambda_{2}, \cdots, \lambda_{m}$  全为 0 时, 等式

$$
\lambda_ {1} a _ {1} + \lambda_ {2} a _ {2} + \dots + \lambda_ {m} a _ {m} + \lambda_ {1} b _ {1} + \lambda_ {2} b _ {2} + \dots + \lambda_ {m} b _ {m} = 0
$$

才能成立,则  $a_{1},a_{2},\cdots,a_{m}$  线性无关, $b_{1},b_{2},\cdots,b_{m}$  亦线性无关;

(4) 若  $a_{1}, a_{2}, \cdots, a_{m}$  线性相关,  $b_{1}, b_{2}, \cdots, b_{m}$  亦线性相关, 则有不全为 0 的数  $\lambda_{1}, \lambda_{2}, \cdots, \lambda_{m}$ , 使

$$
\lambda_ {1} a _ {1} + \lambda_ {2} a _ {2} + \dots + \lambda_ {m} a _ {m} = 0, \lambda_ {1} b _ {1} + \lambda_ {2} b _ {2} + \dots + \lambda_ {m} b _ {m} = 0
$$

同时成立.

9. 设 $b_{1} = a_{1} + a_{2}, b_{2} = a_{2} + a_{3}, b_{3} = a_{3} + a_{4}, b_{4} = a_{4} + a_{1}$，证明向量组 $b_{1}, b_{2}, b_{3}, b_{4}$ 线性相关.

10. 设  $b_{1}=a_{1}, b_{2}=a_{1}+a_{2}, \cdots, b_{r}=a_{1}+a_{2}+\cdots+a_{r}$ ，且向量组  $a_{1}, a_{2}, \cdots, a_{r}$  线性无关，证明向量组  $b_{1}, b_{2}, \cdots, b_{r}$  线性无关.

11. 设向量组  $a_{1}, a_{2}, a_{3}$  线性无关, 判断向量组  $b_{1}, b_{2}, b_{3}$  的线性相关性:

(1) $b_{1}=a_{1}+a_{2},b_{2}=2a_{2}+3a_{3},b_{3}=5a_{1}+3a_{2};$
(2) $b_{1}=a_{1}+2a_{2}+3a_{3},b_{2}=2a_{1}+2a_{2}+4a_{3},b_{3}=3a_{1}+a_{2}+3a_{3};$
(3) $b_{1}=a_{1}-a_{2},b_{2}=2a_{2}+a_{3},b_{3}=a_{1}+a_{2}+a_{3}.$

12. 设向量组  $B:b_{1}, b_{2}, \cdots, b_{r}$  能由向量组  $A:a_{1}, a_{2}, \cdots, a_{s}$  线性表示为

$$
(\dot {\boldsymbol {b}} _ {1}, \boldsymbol {b} _ {2}, \dots , \boldsymbol {b} _ {r}) = (\boldsymbol {a} _ {1}, \boldsymbol {a} _ {2}, \dots , \boldsymbol {a} _ {s}) \boldsymbol {K},
$$

其中 K 为  $s \times r$  矩阵, 且向量组 A 线性无关. 证明向量组 B 线性无关的充分必要条件是矩阵 K 的秩  $R(K) = r$ .

110

---

习题四

13. 求下列向量组的秩, 并求一个最大无关组:

(1)  $a_{1}=\left(\begin{array}{c}1\\2\\-1\\4\end{array}\right),a_{2}=\left(\begin{array}{c}9\\100\\10\\4\end{array}\right),a_{3}=\left(\begin{array}{c}-2\\-4\\2\\-8\end{array}\right);$

(2) $\boldsymbol{a}_{1}=\begin{pmatrix}1\\2\\1\\3\end{pmatrix},\boldsymbol{a}_{2}=\begin{pmatrix}4\\-1\\-5\\-6\end{pmatrix},\boldsymbol{a}_{3}=\begin{pmatrix}1\\-3\\-4\\-7\end{pmatrix}.$

14. 利用初等行变换求下列矩阵的列向量组的一个最大无关组, 并把其余列向量用最大无关组线性表示:

(1) $\begin{pmatrix}25&31&17&43\\75&94&53&132\\75&94&54&134\\25&32&20&48\end{pmatrix};$

(2) $\begin{pmatrix}1&1&2&2&1\\0&2&1&5&-1\\2&0&3&-1&3\\1&1&0&4&-1\end{pmatrix}.$

15. 设向量组  $\begin{pmatrix} a \\ 3 \\ 1 \end{pmatrix}$ ,  $\begin{pmatrix} 2 \\ b \\ 3 \end{pmatrix}$ ,  $\begin{pmatrix} 1 \\ 2 \\ 1 \end{pmatrix}$ ,  $\begin{pmatrix} 2 \\ 3 \\ 1 \end{pmatrix}$  的秩为 2, 求 a, b.

16. 设向量组 $A: \pmb{a}_1, \pmb{a}_2$；向量组 $B: \pmb{a}_1, \pmb{a}_2, \pmb{a}_3$；向量组 $C: \pmb{a}_1, \pmb{a}_2, \pmb{a}_4$ 的秩为 $R_A = R_B = 2, R_C = 3$，求向量组 $D: \pmb{a}_1, \pmb{a}_2, 2\pmb{a}_3 - 3\pmb{a}_4$ 的秩。

17. 设有 n 维向量组  $A: a_{1}, a_{2}, \cdots, a_{n}$ ，证明它们线性无关的充分必要条件是:任一 n 维向量都可由它们线性表示.

18. 设向量组  $a_{1}, a_{2}, \cdots, a_{m}$  线性相关，且  $a_{1} \neq 0$ ，证明存在某个向量  $a_{k} (2 \leqslant k \leqslant m)$ ，使  $a_{k}$  能由  $a_{1}, a_{2}, \cdots, a_{k-1}$  线性表示.

19. 设  $\left\{\begin{aligned}\boldsymbol{\beta}_{1}&=\quad\boldsymbol{\alpha}_{2}+\boldsymbol{\alpha}_{3}+\cdots+\boldsymbol{\alpha}_{n},\\ \boldsymbol{\beta}_{2}&=\boldsymbol{\alpha}_{1}\quad+\boldsymbol{\alpha}_{3}+\cdots+\boldsymbol{\alpha}_{n},\\ \cdots\cdots\\ \boldsymbol{\beta}_{n}&=\boldsymbol{\alpha}_{1}+\boldsymbol{\alpha}_{2}+\cdots+\boldsymbol{\alpha}_{n-1},\end{aligned}\right.$  证明向量组  $\alpha_{1},\alpha_{2},\cdots,\alpha_{n}$  与向量组  $\beta_{1},\beta_{2},\cdots,\beta_{n}$  等价.

20. 已知 3 阶矩阵 A 与 3 维列向量 x 满足  $A^{3}x = 3Ax - A^{2}x$ ，且向量组 x, Ax,  $A^{2}x$  线性无关.

（1）记 $y = Ax, z = Ay, P = (x, y, z)$，求3阶矩阵 $B$，使 $AP = PB$；（2）求 $|A|$.

21. 设

$$
V _ {1} = \left\{\left(x _ {1}, x _ {2}, \dots , x _ {n}\right) ^ {\mathrm{T}} \mid x _ {1}, x _ {2}, \dots , x _ {n} \in \mathbb {R}, \text {满足} x _ {1} + x _ {2} + \dots + x _ {n} = 0 \right\},
$$

$$
V _ {2} = \left\{\left(x _ {1}, x _ {2}, \dots , x _ {n}\right) ^ {\mathrm{T}} \mid x _ {1}, x _ {2}, \dots , x _ {n} \in \mathbb {R}, \text {满足} x _ {1} + x _ {2} + \dots + x _ {n} = 1 \right\},
$$

问 $V_{1}, V_{2}$ 是不是向量空间？为什么？

22. 由 $a_1 = (1,1,0,0)^{\mathrm{T}}, a_2 = (1,0,1,1)^{\mathrm{T}}$ 所生成的向量空间记作 $L_1$, 由 $b_1 = (2,-1,3,3)^{\mathrm{T}}, b_2 = (0,1,-1,-1)^{\mathrm{T}}$ 所生成的向量空间记作 $L_2$, 试证 $L_1 = L_2$.

23. 验证 $\boldsymbol{a}_1 = (1, -1, 0)^{\mathrm{T}}, \boldsymbol{a}_2 = (2, 1, 3)^{\mathrm{T}}, \boldsymbol{a}_3 = (3, 1, 2)^{\mathrm{T}}$ 为 $\mathbb{R}^3$ 的一个基，并把 $\boldsymbol{v}_1 = (5, 0, 7)^{\mathrm{T}}, \boldsymbol{v}_2 = (-9, -8, -13)^{\mathrm{T}}$ 用这个基线性表示.

24. 已知 $\mathbb{R}^3$ 的两个基为

$$
\boldsymbol {a} _ {1} = \left( \begin{array}{c} 1 \\ 1 \\ 1 \end{array} \right), \boldsymbol {a} _ {2} = \left( \begin{array}{c} 1 \\ 0 \\ - 1 \end{array} \right), \boldsymbol {a} _ {3} = \left( \begin{array}{c} 1 \\ 0 \\ 1 \end{array} \right) \quad \text {及} \quad \boldsymbol {b} _ {1} = \left( \begin{array}{c} 1 \\ 2 \\ 1 \end{array} \right), \boldsymbol {b} _ {2} = \left( \begin{array}{c} 2 \\ 3 \\ 4 \end{array} \right), \boldsymbol {b} _ {3} = \left( \begin{array}{c} 3 \\ 4 \\ 3 \end{array} \right),
$$

考研电子书网站:www.pdf2book.com

111

---

第4章 向量组的线性相关性

(1) 求由基  $a_{1}, a_{2}, a_{3}$  到基  $b_{1}, b_{2}, b_{3}$  的过渡矩阵 P;
(2) 设向量 x 在前一基中的坐标为  $(1,1,3)^{\mathrm{T}}$ ，求它在后一基中的坐标.

25. 求下列齐次线性方程组的基础解系:

(1) $\left\{ \begin{array}{l}x_{1} - 8x_{2} + 10x_{3} + 2x_{4} = 0,\\ 2x_{1} + 4x_{2} + 5x_{3} - x_{4} = 0,\\ 3x_{1} + 8x_{2} + 6x_{3} - 2x_{4} = 0; \end{array} \right.$
(2) $\left\{ \begin{array}{l} 2x_{1} - 3x_{2} - 2x_{3} + x_{4} = 0, \\ 3x_{1} + 5x_{2} + 4x_{3} - 2x_{4} = 0, \\ 8x_{1} + 7x_{2} + 6x_{3} - 3x_{4} = 0; \end{array} \right.$
(3) $nx_{1} + (n - 1)x_{2} + \dots + 2x_{n - 1} + x_{n} = 0.$

26. 设 $A = \begin{pmatrix} 2 & -2 & 1 & 3 \\ 9 & -5 & 2 & 8 \end{pmatrix}$, 求一个 $4 \times 2$ 矩阵 $B$, 使 $AB = O$, 且 $R(B) = 2$.

27. 求一个齐次线性方程组, 使它的基础解系为

$$
\boldsymbol {\xi} _ {1} = (0, 1, 2, 3) ^ {\mathrm{T}}, \quad \boldsymbol {\xi} _ {2} = (3, 2, 1, 0) ^ {\mathrm{T}}.
$$

28. 设四元齐次线性方程组

$$
\mathrm{I}: \left\{ \begin{array}{l} x _ {1} + x _ {2} = 0, \\ x _ {2} - x _ {4} = 0; \end{array} \right. \quad \mathrm{II}: \left\{ \begin{array}{l} x _ {1} - x _ {2} + x _ {3} = 0, \\ x _ {2} - x _ {3} + x _ {4} = 0, \end{array} \right.
$$

求:(1) 方程组 I 与 II 的基础解系;(2) I 与 II 的公共解.

29. 设 $n$ 阶矩阵 $\mathbf{A}$ 满足 $\mathbf{A}^2 = \mathbf{A}, \mathbf{E}$ 为 $n$ 阶单位矩阵, 证明

$$
R (\boldsymbol {A}) + R (\boldsymbol {A} - \boldsymbol {E}) = n.
$$

提示: 利用矩阵秩的性质⑥和⑧.

30. 设 $A$ 为 $n$ 阶矩阵 $(n \geqslant 2)$, $A^{*}$ 为 $A$ 的伴随矩阵, 证明

$$
R \left(\boldsymbol {A} ^ {*}\right) = \left\{ \begin{array}{l l} n, & \text {当} R (\boldsymbol {A}) = n, \\ 1, & \text {当} R (\boldsymbol {A}) = n - 1, \\ 0, & \text {当} R (\boldsymbol {A}) \leqslant n - 2. \end{array} \right.
$$

31. 求下列非齐次线性方程组的一个解及对应的齐次线性方程组的基础解系:

(1) $\left\{ \begin{array}{l}x_{1} + x_{2} = 5,\\ 2x_{1} + x_{2} + x_{3} + 2x_{4} = 1,\\ 5x_{1} + 3x_{2} + 2x_{3} + 2x_{4} = 3; \end{array} \right.$

(2) $\left\{ \begin{array}{l}x_{1} - 5x_{2} + 2x_{3} - 3x_{4} = 11,\\ 5x_{1} + 3x_{2} + 6x_{3} - x_{4} = -1,\\ 2x_{1} + 4x_{2} + 2x_{3} + x_{4} = -6. \end{array} \right.$

32. 设四元非齐次线性方程组的系数矩阵的秩为 3, 已知 $\eta_{1}, \eta_{2}, \eta_{3}$ 是它的三个解向量, 且

$$
\boldsymbol {\eta} _ {1} = \left( \begin{array}{c} 2 \\ 3 \\ 4 \\ 5 \end{array} \right), \quad \boldsymbol {\eta} _ {2} + \boldsymbol {\eta} _ {3} = \left( \begin{array}{c} 1 \\ 2 \\ 3 \\ 4 \end{array} \right),
$$

求该方程组的通解.

33. 设有向量组 $A: \boldsymbol{a}_1 = \begin{pmatrix} \alpha \\ 2 \\ 10 \end{pmatrix}, \boldsymbol{a}_2 = \begin{pmatrix} -2 \\ 1 \\ 5 \end{pmatrix}, \boldsymbol{a}_3 = \begin{pmatrix} -1 \\ 1 \\ 4 \end{pmatrix}$ 及向量 $\boldsymbol{b} = \begin{pmatrix} 1 \\ \beta \\ -1 \end{pmatrix}$, 问 $\alpha, \beta$ 为何值时:

(1) 向量 b 不能由向量组 A 线性表示；

112

---

习题四

(2) 向量 b 能由向量组 A 线性表示, 且表示式惟一;
(3) 向量 b 能由向量组 A 线性表示, 且表示式不惟一, 并求一般表示式.

34. 设

$$
\boldsymbol {a} = \left( \begin{array}{l} a _ {1} \\ a _ {2} \\ a _ {3} \end{array} \right), \quad \boldsymbol {b} = \left( \begin{array}{l} b _ {1} \\ b _ {2} \\ b _ {3} \end{array} \right), \quad \boldsymbol {c} = \left( \begin{array}{l} c _ {1} \\ c _ {2} \\ c _ {3} \end{array} \right) \quad (a _ {i} ^ {2} + b _ {i} ^ {2} \neq 0, i = 1, 2, 3),
$$

证明三直线 $\left\{\begin{aligned}l_{1}:a_{1}x+b_{1}y+c_{1}&=0,\\ l_{2}:a_{2}x+b_{2}y+c_{2}&=0,\end{aligned}\right.$ 相交于一点的充分必要条件为:向量组a,b线性无关,且向量组a,b,c
 $l_{3}:a_{3}x+b_{3}y+c_{3}=0$

线性相关.

35. 设矩阵 $A = (a_{1}, a_{2}, a_{3}, a_{4})$，其中 $a_{2}, a_{3}, a_{4}$ 线性无关，$a_{1} = 2a_{2} - a_{3}$，向量 $b = a_{1} + a_{2} + a_{3} + a_{4}$，求方程 $Ax = b$ 的通解。
36. 设  $\eta^{*}$  是非齐次线性方程组 Ax=b 的一个解,  $\xi_{1}, \xi_{2}, \cdots, \xi_{n-r}$  是对应的齐次线性方程组的一个基础解系. 证明:

(1)  $\eta^{*}, \xi_{1}, \xi_{2}, \cdots, \xi_{n-r}$  线性无关；
(2)  $\eta^{*}, \eta^{*} + \xi_{1}, \eta^{*} + \xi_{2}, \cdots, \eta^{*} + \xi_{n-r}$  线性无关.

37. 设  $\eta_{1}, \eta_{2}, \cdots, \eta_{s}$  是非齐次线性方程组 Ax=b 的 s 个解， $k_{1}, k_{2}, \cdots, k_{s}$  为实数，满足  $k_{1} + k_{2} + \cdots + k_{s} = 1$ . 证明

$$
x = k _ {1} \eta_ {1} + k _ {2} \eta_ {2} + \dots + k _ {s} \eta_ {s}
$$

也是它的解.

38. 设非齐次线性方程组 Ax=b 的系数矩阵的秩为  $r, \eta_{1}, \eta_{2}, \cdots, \eta_{n-r+1}$  是它的  $n-r+1$  个线性无关的解（由题 36 知它确有  $n-r+1$  个线性无关的解）。试证它的任一解可表示为

$$
x = k _ {1} \boldsymbol {\eta} _ {1} + k _ {2} \boldsymbol {\eta} _ {2} + \dots + k _ {n - r + 1} \boldsymbol {\eta} _ {n - r + 1} \quad (\text {其中} k _ {1} + k _ {2} + \dots + k _ {n - r + 1} = 1).
$$

第 4 章自测题

![](../../raw/pages_0097-0128/images/page_116_image_20.jpg)

考研电子书网站:www.pdf2book.com

113
