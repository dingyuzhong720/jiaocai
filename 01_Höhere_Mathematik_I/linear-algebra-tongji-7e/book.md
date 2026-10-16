# 工程数学 线性代数 第七版（同济）

MinerU 4.0.12 Advanced；FULL 视图保留页眉、页脚、页码和边栏。

“十二五”中国香港航空科技创业基地项目

“十二五”普通高等教育本科国家级规划教材

## 工程数学 线性代数

第七版

同济大学数学科学学院 编

中国教育出版传媒集团

高等教育出版社

---

[No text]

“十二五”普通高等教育本科国家级规划教材

# 工程数学

# 线性代数

![](raw/pages_0001-0032/images/page_1_image_4.jpg)

同济大学数学科学学院 编

中国教育出版传媒集团

高等教育出版社·北京

---

## 目录

## 第1章 行列式 …… 1

§ 1 二阶与三阶行列式 …… 1
§ 2 全排列和对换 …… 4
§ 3 n 阶行列式的定义 …… 6
§ 4 行列式的性质 …… 7
§ 5 行列式按行(列)展开 …… 15

习题一 20

## 第 2 章 矩阵及其运算 …… 24

§ 1 线性方程组和矩阵…… 24
§ 2 矩阵的运算…… 29
§ 3 逆矩阵…… 39
§ 4 克拉默法则…… 44
§ 5 矩阵分块法……46

习题二 52

## 第3章 矩阵的初等变换与线性方程组 56

§ 1 矩阵的初等变换……56
§ 2 矩阵的秩……66
§ 3 线性方程组的解……71

习题三 78

## 第 4 章 向量组的线性相关性 …… 82

§ 1 向量组及其线性组合……82

考研电子书网站:www.pdf2book.com

I

---

目录

§ 2 向量组的线性相关性……87

§ 3 向量组的秩…… 91

§ 4 向量空间 …… 95

§ 5 线性方程组的解的结构 …… 101

习题四 109

## 第 5 章 相似矩阵及二次型 …… 114

§ 1 向量的内积、长度及正交性…… 114

§ 2 方阵的特征值与特征向量 …… 120

§ 3 相似矩阵 …… 124

§ 4 对称矩阵的对角化 …… 127

§ 5 二次型及其标准形 …… 131

§ 6 用配方法化二次型成标准形 …… 135

§ 7 正定二次型 …… 136

习题五 138

## \*第6章 线性空间与线性变换 …… 142

§ 1 线性空间的定义与性质 …… 142

§ 2 维数、基与坐标…… 146

§ 3 基变换与坐标变换 …… 148

§ 4 线性变换 …… 150

§ 5 线性变换的矩阵表示式 …… 153

习题六 157

## 部分习题参考答案 160

II

---

## 第1章

## 行列式

行列式是线性代数中常用的工具.本章主要介绍 $n$ 阶行列式的定义、性质及其计算方法.

## § 1 二阶与三阶行列式

## 一、二元线性方程组与二阶行列式

用消元法解二元线性方程组

$$
\left\{ \begin{array}{l} a _ {1 1} x _ {1} + a _ {1 2} x _ {2} = b _ {1}, \\ a _ {2 1} x _ {1} + a _ {2 2} x _ {2} = b _ {2}. \end{array} \right. \tag {1}
$$

为消去未知数 $x_{2}$, 以 $a_{22}$ 与 $a_{12}$ 分别乘上述两方程的两端, 然后两个方程相减, 得

$$
(a _ {1 1} a _ {2 2} - a _ {1 2} a _ {2 1}) x _ {1} = b _ {1} a _ {2 2} - a _ {1 2} b _ {2};
$$

类似地,消去 $x_{1}$ ,得

$$
(a _ {1 1} a _ {2 2} - a _ {1 2} a _ {2 1}) x _ {2} = a _ {1 1} b _ {2} - b _ {1} a _ {2 1}.
$$

当 $a_{11}a_{22} - a_{12}a_{21}\neq 0$ 时，求得方程组(1)的解为

$$
x _ {1} = \frac {b _ {1} a _ {2 2} - a _ {1 2} b _ {2}}{a _ {1 1} a _ {2 2} - a _ {1 2} a _ {2 1}}, \quad x _ {2} = \frac {a _ {1 1} b _ {2} - b _ {1} a _ {2 1}}{a _ {1 1} a _ {2 2} - a _ {1 2} a _ {2 1}}. \tag {2}
$$

(2)式中的分子、分母都是四个数分两对相乘再相减而得,其中分母 $a_{11}a_{22}-a_{12}a_{21}$ 是由方程组(1)的四个系数确定的,把这四个数按它们在方程组(1)中的位置,排成二行二列(横排称行、竖排称列)的数表

$$
\begin{array}{l} \begin{array}{c c} \boldsymbol {a} _ {1 1} & \boldsymbol {a} _ {1 2} \\ & , \end{array} \tag {3} \\ a _ {2 1} \quad a _ {2 2} \\ \end{array}
$$

考研电子书网站:www.pdf2book.com

1

---

第1章 行列式

表达式 $a_{11}a_{22} - a_{12}a_{21}$ 称为数表(3)所确定的二阶行列式，并记作

$$
\left| \begin{array}{l l} a _ {1 1} & a _ {1 2} \\ a _ {2 1} & a _ {2 2} \end{array} \right| \tag {4}
$$

数 ${a}_{ij}\left( {i,j = 1,2}\right)$ 称为行列式(4)的元素或元. 元素 ${a}_{ij}$ 的第一个下标 $i$ 称为行标, 表明该元素位于第 $i$ 行；第二个下标 $j$ 称为列标,表明该元素位于第 $j$ 列. 位于第 $i$ 行第 $j$ 列的元素称为行列式(4)的(i,j)元.

上述二阶行列式的定义,可用对角线法则来记忆.参看图1.1,把 $a_{11}$ 到 $a_{22}$ 的实连线称为主对角线, $a_{12}$ 到 $a_{21}$ 的虚连线称为副对角线,于是二阶行列式便是主对角线上的两元素之积减去副对角线上两元素之积所得的差.

![](raw/pages_0001-0032/images/page_5_image_5.jpg)

图1.1

利用二阶行列式的概念,(2)式中 $x_{1},x_{2}$ 的分子也可写成二阶行列式,即

$$
b _ {1} a _ {2 2} - a _ {1 2} b _ {2} = \left| \begin{array}{c c} b _ {1} & a _ {1 2} \\ b _ {2} & a _ {2 2} \end{array} \right|, \quad a _ {1 1} b _ {2} - b _ {1} a _ {2 1} = \left| \begin{array}{c c} a _ {1 1} & b _ {1} \\ a _ {2 1} & b _ {2} \end{array} \right|.
$$

若记

$$
D = \left| \begin{array}{l l} a _ {1 1} & a _ {1 2} \\ a _ {2 1} & a _ {2 2} \end{array} \right|, \quad D _ {1} = \left| \begin{array}{l l} b _ {1} & a _ {1 2} \\ b _ {2} & a _ {2 2} \end{array} \right|, \quad D _ {2} = \left| \begin{array}{l l} a _ {1 1} & b _ {1} \\ a _ {2 1} & b _ {2} \end{array} \right|,
$$

则(2)式可写成

$$
x _ {1} = \frac {D _ {1}}{D} = \frac {\left| \begin{array}{l l} b _ {1} & a _ {1 2} \\ b _ {2} & a _ {2 2} \end{array} \right|}{\left| \begin{array}{l l} a _ {1 1} & a _ {1 2} \\ a _ {2 1} & a _ {2 2} \end{array} \right|}, \quad x _ {2} = \frac {D _ {2}}{D} = \frac {\left| \begin{array}{l l} a _ {1 1} & b _ {1} \\ a _ {2 1} & b _ {2} \end{array} \right|}{\left| \begin{array}{l l} a _ {1 1} & a _ {1 2} \\ a _ {2 1} & a _ {2 2} \end{array} \right|}.
$$

注意这里的分母 $D$ 是由方程组(1)的系数所确定的二阶行列式(称系数行列式), $x_{1}$ 的分子 $D_{1}$ 是用常数项 $b_{1}, b_{2}$ 替换 $D$ 中第 1 列的元素 $a_{11}, a_{21}$ 所得的二阶行列式, $x_{2}$ 的分子 $D_{2}$ 是用常数项 $b_{1}, b_{2}$ 替换 $D$ 中第 2 列的元素 $a_{12}, a_{22}$ 所得的二阶行列式.

例 1 求解二元线性方程组 公众号:旗胜考研

$$
\left\{ \begin{array}{l} 3 x _ {1} - 2 x _ {2} = 1 2, \\ 2 x _ {1} + x _ {2} = 1. \end{array} \right.
$$

解 由于

$$
\begin{array}{l} D \vDash \left| \begin{array}{c c} 3 & - 2 \\ 2 & 1 \end{array} \right| = 3 - (- 4) = 7 \neq 0, \\ D _ {1} = \left| \begin{array}{c c} 1 2 & - 2 \\ 1 & 1 \end{array} \right| = 1 2 - (- 2) = 1 4, \\ \end{array}
$$

2

---

§1 二阶与三阶行列式

$$
D _ {2} = \left| \begin{array}{c c} 3 & 1 2 \\ 2 & 1 \end{array} \right| = 3 - 2 4 = - 2 1,
$$

因此

$$
x _ {1} = \frac {D _ {1}}{D} = \frac {1 4}{7} = 2, \quad x _ {2} = \frac {D _ {2}}{D} = \frac {- 2 1}{7} = - 3.
$$

## 二、三阶行列式

定义1 设有9个数排成3行3列的数表

$$
\begin{array}{l} a _ {1 1} \quad a _ {1 2} \quad a _ {1 3} \\ a _ {2 1} \quad a _ {2 2} \quad a _ {2 3}, \tag {5} \\ a _ {3 1} \quad a _ {3 2} \quad a _ {3 3} \\ \end{array}
$$

记

$$
\begin{array}{l} \left| \begin{array}{c c c} a _ {1 1} & a _ {1 2} & a _ {1 3} \\ a _ {2 1} & a _ {2 2} & a _ {2 3} \\ a _ {3 1} & a _ {3 2} & a _ {3 3} \end{array} \right| \\ = a _ {1 1} a _ {2 2} a _ {3 3} + a _ {1 2} a _ {2 3} a _ {3 1} + a _ {1 3} a _ {2 1} a _ {3 2} - a _ {1 1} a _ {2 3} a _ {3 2} - a _ {1 2} a _ {2 1} a _ {3 3} - a _ {1 3} a _ {2 2} a _ {3 1}, \tag {6} \\ \end{array}
$$

(6)式称为数表(5)所确定的三阶行列式.

上述定义表明三阶行列式含6项，每项均为不同行不同列的三个元素的乘积再冠以正负号，其规律遵循图1.2所示的对角线法则:图中有三条实线看做是平行于主对角线的连线，三条虚线看做是平行于副对角线的连线，实线上三元素的乘积冠正号，虚线上三元素的乘积冠负号。

![](raw/pages_0001-0032/images/page_6_image_11.jpg)

<details>
<summary>text_image</summary>

a₁₁ a₁₂ a₁₃
a₂₁ a₂₂ a₂₃
a₃₁ a₃₂ a₃₃
</details>

图1.2

类似于二元线性方程组与二阶行列式,考虑三元线性方程组时,若方程组的系数行列式非零,也可用三阶行列式来表示未知数 $x_{1},x_{2},x_{3}$ （见第2章§4）.

例2 计算三阶行列式

$$
D = \left| \begin{array}{c c c} 1 & 2 & - 4 \\ - 2 & 2 & 1 \\ - 3 & 4 & - 2 \end{array} \right|.
$$

解 按对角线法则,有

$$
\begin{array}{l} D = 1 \times 2 \times (- 2) + 2 \times 1 \times (- 3) + (- 4) \times (- 2) \times 4 - 1 \times 1 \times 4 - 2 \times (- 2) \times (- 2) - (- 4) \times 2 \times (- 3) \\ = - 4 - 6 + 3 2 - 4 - 8 - 2 4 = - 1 4. \\ \end{array}
$$

考研电子书网站:www.pdf2book.com

3

---

第1章 行列式

例3 求解方程

$$
\left| \begin{array}{c c c} 1 & 1 & 1 \\ 2 & 3 & x \\ 4 & 9 & x ^ {2} \end{array} \right| = 0.
$$

解 方程左端的三阶行列式

$$
D = 3 x ^ {2} + 4 x + 1 8 - 9 x - 2 x ^ {2} - 1 2 = x ^ {2} - 5 x + 6,
$$

由 $x^{2} - 5x + 6 = 0$ 解得 $x = 2$ 或 $x = 3$.

对角线法则只适用于二阶与三阶行列式,为研究四阶及更高阶行列式,下面先介绍有关全排列的知识,然后引出 n 阶行列式的概念.

## § 2 全排列和对换

## 一、排列及其逆序数

把 $n$ 个不同的元素（如取自然数 $\{1,2,\dots ,n\}$ )排成一行，叫做这 $n$ 个元素的全排列（也简称 $n$ 元排列），所有 $n$ 元排列构成的集合记为 $S_{n}$. $S_{n}$ 中所含元素的个数即 $n$ 元排列的个数，记为 $\left|S_n\right|$，可计算如下:

从 $n$ 个元素中任取一个放在第一个位置上，有 $n$ 种取法；

从剩下的 n-1 个元素中任取一个放在第二个位置上,有 n-1 种取法;

这样继续下去,直到最后只剩下一个元素放在第 n 个位置上,只有 1 种取法.于是

$$
\mid S _ {n} \mid = n \times (n - 1) \times \dots \times 3 \times 2 \times 1 = n!
$$

例如用1,2,3三个数字作排列,排列总数 $|S_{3}|=3\times2\times1=6$ ,它们是

$$
1 2 3, 2 3 1, 3 1 2, 1 3 2, 2 1 3, 3 2 1.
$$

对于 $n$ 个不同的元素, 先规定各元素之间有一个标准次序 (例如 $n$ 个不同的自然数, 可规定由小到大为标准次序), 于是在这 $n$ 个元素的任一排列中, 当某一对元素的先后次序与标准次序不同时, 就说它构成 1 个逆序. 一个排列中所有逆序的总数叫做这个排列的逆序数. 将排列 $p_1 p_2 \cdots p_n$ 的逆序数记为 $t(p_1 p_2 \cdots p_n)$.

逆序数为奇数的排列叫做奇排列,逆序数为偶数的排列叫做偶排列.

下面来讨论计算排列的逆序数的方法.

不失一般性,不妨设 n 个元素为 1 至 n 这 n 个自然数,并规定由小到大为标准次序.设  $p_{1}p_{2}\cdots p_{n}$  为这 n 个自然数的一个排列,考虑元素  $p_{i}(i=1,2,\cdots,n)$ ,如果比  $p_{i}$  大的且排在  $p_{i}$  前面的元素有  $t_{i}$  个,就说  $p_{i}$  这个元素的逆序数是  $t_{i}$ .全体元素的逆序数之

4

---

§2 全排列和对换

总和

$$
t = t _ {1} + t _ {2} + \dots + t _ {n} = \sum_ {i = 1} ^ {n} t _ {i}
$$

即是这个排列的逆序数.

例 4 求排列 32514 的逆序数.

解 在排列 32514 中:

3 排在首位,逆序数  $t_{1}=0$ ;
2 的前面比 2 大的数有一个(3)，故逆序数  $t_{2}=1$ ;
5 是最大数, 逆序数  $t_{3}=0$ ;

1 的前面比 1 大的数有三个  $(3,2,5)$ ，故逆序数  $t_{4}=3$ ;
4 的前面比 4 大的数有一个(5)，故逆序数 $t_5 = 1$，于是这个排列的逆序数为

$$
t = \sum_ {i = 1} ^ {5} t _ {i} = 0 + 1 + 0 + 3 + 1 = 5.
$$

## 二、对换

在排列中,将任意两个元素对调,其余的元素不动,这种作出新排列的操作叫做对换.将相邻两个元素对换,叫做相邻对换.

定理 1 一个排列中的任意两个元素对换，排列改变奇偶性.

证 仍不妨设元素为从1开始的自然数(从小到大为标准次序).先证相邻对换的情形.

设排列为 $a_1a_2\cdots a_labb_1b_2\cdots b_m$，对换 $a$ 与 $b$，变为 $a_1a_2\cdots a_lbab_1b_2\cdots b_m$。显然，$a_1, a_2, \cdots, a_l; b_1, b_2, \cdots, b_m$ 这些元素的逆序数经过对换并不改变，而 $a, b$ 两元素的逆序数改变为:当 $a < b$ 时，经对换后 $a$ 的逆序数增加 1 而 $b$ 的逆序数不变；当 $a > b$ 时，经对换后 $a$ 的逆序数不变而 $b$ 的逆序数减少 1。所以排列 $a_1a_2\cdots a_labb_1b_2\cdots b_m$ 与排列 $a_1a_2\cdots a_lbab_1b_2\cdots b_m$ 的奇偶性不同。

再证一般对换的情形.

设排列为 $a_1a_2\cdots a_lab_1b_2\cdots b_mbc_1c_2\cdots c_n$，把它作 $m$ 次相邻对换，变成 $a_1a_2\cdots a_labb_1b_2\cdots b_mc_1c_2\cdots c_n$，再作 $m+1$ 次相邻对换，变成 $a_1a_2\cdots a_lbb_1b_2\cdots b_mac_1c_2\cdots c_n$。总之，经 $2m+1$ 次相邻对换，排列 $a_1a_2\cdots a_lab_1b_2\cdots b_mbc_1c_2\cdots c_n$ 变成排列 $a_1a_2\cdots a_lbb_1b_2\cdots b_mac_1c_2\cdots c_n$，所以这两个排列的奇偶性相反。证毕

推论 奇排列对换成标准排列的对换次数为奇数，偶排列对换成标准排列的对换次数为偶数.

证 由定理1知对换的次数就是排列奇偶性的变化次数,而标准排列是偶排列(逆序数为0),因此知推论成立.证毕

考研电子书网站:www.pdf2book.com

5

---

第1章 行列式

## § 3 n 阶行列式的定义

为了给出 $n$ 阶行列式的定义, 先来研究三阶行列式的结构. 三阶行列式定义为

$$
\begin{array}{l} \left| \begin{array}{c c c} a _ {1 1} & a _ {1 2} & a _ {1 3} \\ a _ {2 1} & a _ {2 2} & a _ {2 3} \\ a _ {3 1} & a _ {3 2} & a _ {3 3} \end{array} \right| \\ = a _ {1 1} a _ {2 2} a _ {3 3} + a _ {1 2} a _ {2 3} a _ {3 1} + a _ {1 3} a _ {2 1} a _ {3 2} - a _ {1 1} a _ {2 3} a _ {3 2} - a _ {1 2} a _ {2 1} a _ {3 3} - a _ {1 3} a _ {2 2} a _ {3 1}. \tag {6} \\ \end{array}
$$

容易看出:

(i) (6)式右边的每一项都恰是三个元素的乘积, 这三个元素位于不同的行、不同的列. 因此, (6)式右端的任一项除正负号外可以写成 $a_{1p_1} a_{2p_2} a_{3p_3}$. 这里第一个下标(行标)排成标准次序 123, 而第二个下标(列标)排成 $p_1 p_2 p_3$, 它是 1, 2, 3 三个数的某个排列. 这样的排列共有 6 种, 对应 (6)式右端共含 6 项.

(ii) 各项的正负号与列标的排列对照.

带正号的三项列标排列是 123,231,312;

带负号的三项列标排列是 132,213,321.

经计算可知前三个排列都是偶排列,而后三个排列都是奇排列.因此各项所带的正负号可以表示为 $(-1)^{t}$ ,其中t为列标排列的逆序数.

总之,三阶行列式可以写成

$$
\left| \begin{array}{c c c} a _ {1 1} & a _ {1 2} & a _ {1 3} \\ a _ {2 1} & a _ {2 2} & a _ {2 3} \\ a _ {3 1} & a _ {3 2} & a _ {3 3} \end{array} \right| = \sum_ {p _ {1} p _ {2} p _ {3} \in S _ {3}} (- 1) ^ {t (p _ {1} p _ {2} p _ {3})} a _ {1 p _ {1}} a _ {2 p _ {2}} a _ {3 p _ {3}},
$$

其中 $t(p_1p_2p_3)$ 为排列 $p_1p_2p_3$ 的逆序数，$\Sigma$ 表示对1,2,3三个数的所有排列 $p_1p_2p_3$ 取和.

仿此,可以把行列式推广到一般情形.

定义 2 设有  $n^{2}$  个数, 排成 n 行 n 列的数表

$$
\begin{array}{c c c c c} & a _ {1 1} & a _ {1 2} & \dots & a _ {1 n} \\ & a _ {2 1} & a _ {2 2} & \dots & a _ {2 n} \\ & \vdots & \vdots & & \vdots \\ , & a _ {n 1} & a _ {n 2} & \dots & a _ {n n} \end{array} ,
$$

作出表中位于不同行不同列的 $n$ 个数的乘积，并冠以符号 $(-1)^{t(p_1p_2\cdots p_n)}$ ，得到形如

$$
\left(- 1\right) ^ {t (p _ {1} p _ {2} \dots p _ {n})} a _ {1 p _ {1}} a _ {2 p _ {2}} \dots a _ {n p _ {n}} \tag {7}
$$

6

---

§4 行列式的性质

的项,其中 $p_{1}p_{2}\cdots p_{n}$ 为自然数 $1,2,\cdots,n$ 的一个排列, $t(p_{1}p_{2}\cdots p_{n})$ 为这个排列的逆序数.由于这样的排列共有n!个,因而形如(7)式的项共有n!项.所有这n!项的代数和

$$
\sum_ {p _ {1} p _ {2} \dots p _ {n} \in S _ {n}} (- 1) ^ {t (p _ {1} p _ {2} \dots p _ {n})} a _ {1 p _ {1}} a _ {2 p _ {2}} \dots a _ {n p _ {n}}
$$

称为 n 阶行列式, 记作

$$
D = \left| \begin{array}{c c c c} a _ {1 1} & a _ {1 2} & \dots & a _ {1 n} \\ a _ {2 1} & a _ {2 2} & \dots & a _ {2 n} \\ \vdots & \vdots & & \vdots \\ a _ {n 1} & a _ {n 2} & \dots & a _ {n n} \end{array} \right|,
$$

简记作  $\det(a_{ij})$ ，其中数  $a_{ij}$  为行列式 D 的  $(i,j)$  元.

按此定义的二阶、三阶行列式，与 §1 中用对角线法则定义的二阶、三阶行列式显然是一致的。当 $n = 1$ 时，一阶行列式 $|a| = a$，注意不要与绝对值记号相混淆。

主对角线以下(上)的元素都为0的行列式叫做上(下)三角形行列式;特别地,主对角线以下和以上的元素都为0的行列式叫做对角行列式.

例 5 证明:(1) 下三角形行列式

$$
D = \left| \begin{array}{c c c c} a _ {1 1} & & & \\ a _ {2 1} & a _ {2 2} & & 0 \\ \vdots & \vdots & \ddots & \\ a _ {n 1} & a _ {n 2} & \dots & a _ {n n} \end{array} \right| = a _ {1 1} a _ {2 2} \dots a _ {n n};
$$

(2) 对角行列式

$$
\left| \begin{array}{c c c c} \lambda_ {1} & & & \\ & \lambda_ {2} & & \\ & & \ddots & \\ & & & \lambda_ {n} \end{array} \right| = \lambda_ {1} \lambda_ {2} \dots \lambda_ {n}.
$$

证（1）由于当 $j > i$ 时，$a_{ij} = 0$，故 $D$ 中可能不为0的元素 $a_{ip_i}$，其下标应有 $p_i \leqslant i$，即 $p_1 \leqslant 1, p_2 \leqslant 2, \dots, p_n \leqslant n$，而 $p_1 + p_2 + \dots + p_n = 1 + 2 + \dots + n$，因此 $p_1 = 1, p_2 = 2, \dots, p_n = n$，所以 $D$ 中可能不为0的项只有一项 $(-1)^{t(12 \dots n)} a_{11} a_{22} \dots a_{nn}$. 此项的符号 $(-1)^{t(12 \dots n)} = (-1)^0 = 1$，所以

$$
D = a _ {1 1} a _ {2 2} \dots a _ {n n}.
$$

(2) 由(1)即得.

## § 4 行列式的性质

记

考研电子书网站:www.pdf2book.com

7

延伸阅读

---

第1章 行列式

$$
D = \left| \begin{array}{c c c c} a _ {1 1} & a _ {1 2} & \dots & a _ {1 n} \\ a _ {2 1} & a _ {2 2} & \dots & a _ {2 n} \\ \vdots & \vdots & & \vdots \\ a _ {n 1} & a _ {n 2} & \dots & a _ {n n} \end{array} \right|, \quad D ^ {\mathrm{T}} = \left| \begin{array}{c c c c} a _ {1 1} & a _ {2 1} & \dots & a _ {n 1} \\ a _ {1 2} & a _ {2 2} & \dots & a _ {n 2} \\ \vdots & \vdots & & \vdots \\ a _ {1 n} & a _ {2 n} & \dots & a _ {n n} \end{array} \right|,
$$

行列式  $D^{T}$  称为行列式 D 的转置行列式.

## 性质1 行列式与它的转置行列式相等.

证 记  $D=\det(a_{ij})$  的转置行列式  $D^{\mathrm{T}}=\det(b_{ij})$ ，即  $D^{\mathrm{T}}$  的  $(i,j)$  元为  $b_{ij}$ ，则  $b_{ij}=a_{ji}(i,j=1,2,\cdots,n)$ ，按定义

$$
D ^ {\mathrm{T}} = \sum (- 1) ^ {t} b _ {1 p _ {1}} b _ {2 p _ {2}} \dots b _ {n p _ {n}} = \sum (- 1) ^ {t} a _ {p _ {1} 1} a _ {p _ {2} 2} \dots a _ {p _ {n} n}.
$$

下证 ${D} = {D}^{\mathrm{T}}$ .

对于行列式 $D$ 的任一项

$$
(- 1) ^ {t} a _ {1 p _ {1}} \dots a _ {i p _ {i}} \dots a _ {j p _ {j}} \dots a _ {n p _ {n}},
$$

其中 $12 \cdots i \cdots j \cdots n$ 为标准排列, $t$ 为排列 $p_1 p_2 \cdots p_i \cdots p_j \cdots p_n$ 的逆序数, 对换元素 $a_{ip_i}$ 与 $a_{jp_j}$ 成

$$
(- 1) ^ {t} a _ {1 p _ {1}} \dots a _ {j p _ {j}} \dots a _ {i p _ {i}} \dots a _ {n p _ {n}},
$$

这时,这一项的值不变,而行标排列与列标排列同时作了一次相应的对换.设新的行标排列 $12\cdots j\cdots i\cdots n$ 的逆序数为r,则r为奇数;设新的列标排列 $p_{1}p_{2}\cdots p_{j}\cdots p_{i}\cdots p_{n}$ 的逆序数为 $t_{1}$ ,则

$$
(- 1) ^ {t _ {1}} = - (- 1) ^ {t}.
$$

故

$$
(- 1) ^ {t} = - (- 1) ^ {t _ {1}} = (- 1) ^ {r} (- 1) ^ {t _ {1}} = (- 1) ^ {r + t _ {1}},
$$

于是

$$
(- 1) ^ {t} a _ {1 p _ {1}} \dots a _ {i p _ {i}} \dots a _ {j p _ {j}} \dots a _ {n p _ {n}} = (- 1) ^ {r + t _ {1}} a _ {1 p _ {1}} \dots a _ {j p _ {j}} \dots a _ {i p _ {i}} \dots a _ {n p _ {n}}.
$$

这就表明,对换乘积中两元素的次序,从而行标排列与列标排列同时作了相应的对换,则行标排列与列标排列的逆序数之和并不改变奇偶性.经一次对换是如此,经多次对换当然还是如此.于是,经过若干次对换,使

列标排列  $p_{1}p_{2}\cdots p_{n}$  （逆序数为 t）变为标准排列（逆序数为 0）；

行标排列则相应地从标准排列变为某个新的排列, 设此新排列为  $q_{1}q_{2}\cdots q_{n}$ , 其逆序数为 s, 则有

$$
(- 1) ^ {t} a _ {1 p _ {1}} a _ {2 p _ {2}} \dots a _ {n p _ {n}} = (- 1) ^ {s} a _ {q _ {1} 1} a _ {q _ {2} 2} \dots a _ {q _ {n} n}.
$$

又,如果上式左边乘积的第 $i$ 个元素 $a_{ip_i}$ 为 $a_{ij}$,那么它必定是上式右边乘积的第 $j$ 个元素,即 $a_{ip_i} = a_{ij} = a_{q_jj}$.可见排列 $q_1q_2\cdots q_n$ 由排列 $p_1p_2\cdots p_n$ 惟一确定.

综上可知: 对于 D 中任一项  $(-1)^{\prime}a_{1p_{1}}a_{2p_{2}}\cdots a_{np_{n}}$ ，总有且仅有  $D^{T}$  中的某一项

8

---

§4 行列式的性质

$(-1)^{s}a_{q_{1}1}a_{q_{2}2}\cdots a_{q_{n}n}$ 与之对应并相等；反之，对于 $D^{T}$ 中的任一项 $(-1)^{t}a_{p_{1}1}a_{p_{2}2}\cdots a_{p_{n}n}$ ，也总有且仅有D中的某一项 $(-1)^{s}a_{1q_{1}}a_{2q_{2}}\cdots a_{nq_{n}}$ 与之对应并相等，于是D与 $D^{T}$ 中的项可以一一对应并相等，从而 $D=D^{T}$ .证毕

由此性质可知,行列式中的行与列具有同等的地位,行列式的性质凡是对行成立的对列也同样成立,反之亦然.

性质 2 对换行列式的两行(列), 行列式变号.

证 设行列式

$$
D _ {1} = \left| \begin{array}{c c c c} b _ {1 1} & b _ {1 2} & \dots & b _ {1 n} \\ b _ {2 1} & b _ {2 2} & \dots & b _ {2 n} \\ \vdots & \vdots & & \vdots \\ b _ {n 1} & b _ {n 2} & \dots & b _ {n n} \end{array} \right|
$$

是由行列式 $D = \det (a_{ij})$ 对换 $i,j$ 两行得到的，即当 $k\neq i,j$ 时， $b_{kp} = a_{kp}$ ；当 $k = i,j$ 时， $b_{ip} = a_{jp},b_{jp} = a_{ip}$ ，于是

$$
\begin{array}{l} D _ {1} = \sum (- 1) ^ {t} b _ {1 p _ {1}} \dots b _ {i p _ {i}} \dots b _ {j p _ {j}} \dots b _ {n p _ {n}} = \sum (- 1) ^ {t} a _ {1 p _ {1}} \dots a _ {j p _ {i}} \dots a _ {i p _ {j}} \dots a _ {n p _ {n}} \\ = \sum (- 1) ^ {\prime} a _ {1 p _ {1}} \dots a _ {i p _ {j}} \dots a _ {j p _ {i}} \dots a _ {n p _ {n}}, \\ \end{array}
$$

其中 $12\cdots i\cdots j\cdots n$ 为标准排列，$t$ 为排列 $p_1p_2\cdots p_i\cdots p_j\cdots p_n$ 的逆序数.设排列 $p_1p_2\cdots p_j\cdots p_i\cdots p_n$ 的逆序数为 $t_1$ ，则 $(-1)' = -(1)^{t_1}$ ，故

$$
D _ {1} = - \sum (- 1) ^ {t _ {1}} a _ {1 p _ {1}} \dots a _ {i p _ {j}} \dots a _ {j p _ {i}} \dots a _ {n p _ {n}} = - D.
$$

证毕

以 $r_i$ 表示行列式的第 $i$ 行, 以 $c_i$ 表示第 $i$ 列. 对换 $i, j$ 两行记作 $r_i \leftrightarrow r_j$, 对换 $i, j$ 两列记作 $c_i \leftrightarrow c_j$.

推论 若行列式有两行(列)完全相同,则此行列式等于零.

证 把这两行对换,有 D = -D, 故 D = 0.

证毕

性质3 行列式的某一行(列)中所有的元素都乘同一数 $k$, 等于用数 $k$ 乘此行列式. 第 $i$ 行(或列)乘 $k$, 记作 $r_i \times k$ (或 $c_i \times k$).

推论1 行列式中某一行(列)的所有元素的公因子可以提到行列式记号的外面. 即

$$
\left| \begin{array}{c c c c} a _ {1 1} & a _ {1 2} & \dots & a _ {1 n} \\ \vdots & \vdots & & \vdots \\ k a _ {i 1} & k a _ {i 2} & \dots & k a _ {i n} \\ \vdots & \vdots & & \vdots \\ a _ {n 1} & a _ {n 2} & \dots & a _ {n n} \end{array} \right| = k \left| \begin{array}{c c c c} a _ {1 1} & a _ {1 2} & \dots & a _ {1 n} \\ \vdots & \vdots & & \vdots \\ a _ {i 1} & a _ {i 2} & \dots & a _ {i n} \\ \vdots & \vdots & & \vdots \\ a _ {n 1} & a _ {n 2} & \dots & a _ {n n} \end{array} \right|.
$$

推论 2 行列式中如果有两行(列)元素成比例, 则此行列式等于零.

考研电子书网站:www.pdf2book.com

9

---

第1章 行列式

性质 4 若行列式的某一行(列)的元素都是两数之和,例如第 i 行的元素都是两数之和:

$$
D = \left| \begin{array}{c c c c} a _ {1 1} & a _ {1 2} & \dots & a _ {1 n} \\ \vdots & \vdots & & \vdots \\ a _ {i 1} + a _ {i 1} ^ {\prime} & a _ {i 2} + a _ {i 2} ^ {\prime} & \dots & a _ {i n} + a _ {i n} ^ {\prime} \\ \vdots & \vdots & & \vdots \\ a _ {n 1} & a _ {n 2} & \dots & a _ {n n} \end{array} \right|,
$$

则 $D$ 等于下列两个行列式之和:

$$
D = \left| \begin{array}{c c c c} a _ {1 1} & a _ {1 2} & \dots & a _ {1 n} \\ \vdots & \vdots & & \vdots \\ a _ {i 1} & a _ {i 2} & \dots & a _ {i n} \\ \vdots & \vdots & & \vdots \\ a _ {n 1} & a _ {n 2} & \dots & a _ {n n} \end{array} \right| + \left| \begin{array}{c c c c} a _ {1 1} & a _ {1 2} & \dots & a _ {1 n} \\ \vdots & \vdots & & \vdots \\ a _ {i 1} ^ {\prime} & a _ {i 2} ^ {\prime} & \dots & a _ {i n} ^ {\prime} \\ \vdots & \vdots & & \vdots \\ a _ {n 1} & a _ {n 2} & \dots & a _ {n n} \end{array} \right|.
$$

性质5 把行列式的某一行(列)的各元素乘同一数然后加到另一行(列)对应的元素上去,行列式不变.

例如以数 $k$ 乘第 $i$ 行加到第 $j$ 行上（记作 $r_j + kr_i$），有

$$
\left| \begin{array}{c c c c} a _ {1 1} & a _ {1 2} & \dots & a _ {1 n} \\ \vdots & \vdots & & \vdots \\ a _ {i 1} & a _ {i 2} & \dots & a _ {i n} \\ \vdots & \vdots & & \vdots \\ a _ {j 1} & a _ {j 2} & \dots & a _ {j n} \\ \vdots & \vdots & & \vdots \\ a _ {n 1} & a _ {n 2} & \dots & a _ {n n} \end{array} \right| \stackrel {{r _ {j} + k r _ {i}}} {{=}} \left| \begin{array}{c c c c} a _ {1 1} & a _ {1 2} & \dots & a _ {1 n} \\ \vdots & \vdots & & \vdots \\ a _ {i 1} & a _ {i 2} & \dots & a _ {i n} \\ \vdots & \vdots & & \vdots \\ a _ {j 1} + k a _ {i 1} & a _ {j 2} + k a _ {i 2} & \dots & a _ {j n} + k a _ {i n} \\ \vdots & \vdots & & \vdots \\ a _ {n 1} & a _ {n 2} & \dots & a _ {n n} \end{array} \right| (i \neq j).
$$

(以数 k 乘第 i 列加到第 j 列上, 记作  $c_{j} + kc_{i}$ .)

以上诸性质请读者证明之.

上述性质 4 表明: 当某一行(或列)的元素为两数之和时, 行列式关于该行(或列)可分解为两个行列式. 若 n 阶行列式每个元素都表示成两数之和, 则它可分解成  $2^{n}$  个行列式. 例如二阶行列式

$$
\left| \begin{array}{c c} a + x & b + y \\ c + z & d + w \end{array} \right| = \left| \begin{array}{c c} a & b + y \\ c & d + w \end{array} \right| + \left| \begin{array}{c c} x & b + y \\ z & d + w \end{array} \right| = \left| \begin{array}{c c} a & b \\ c & d \end{array} \right| + \left| \begin{array}{c c} a & y \\ c & w \end{array} \right| + \left| \begin{array}{c c} x & b \\ z & d \end{array} \right| + \left| \begin{array}{c c} x & y \\ z & w \end{array} \right|.
$$

性质2,3,5介绍了行列式关于行和关于列的三种运算，即 $r_i \leftrightarrow r_j, r_i \times k, r_i + kr_j$ 和 $c_i \leftrightarrow c_j, c_i \times k, c_i + kc_j$ ，利用这些运算可简化行列式的计算，特别是利用运算 $r_i + kr_j$ （或 $c_i + kc_j$）可以把行列式中许多元素化为0.计算行列式常用的一种方法就是利用运算 $r_i +$

10

---

§4 行列式的性质

$k{r}_{j}$ 把行列式化为上三角形行列式,从而算得行列式的值.请看以下几个例题.

例6 计算 $n$ 阶行列式

$$
D = \left| \begin{array}{c c c c} & & & a _ {1 n} \\ 0 & & a _ {2, n - 1} & a _ {2 n} \\ & \ddots & \vdots & \vdots \\ a _ {n 1} & \dots & a _ {n, n - 1} & a _ {n n} \end{array} \right|; \quad (2) \left| \begin{array}{c c c c} & & & \lambda_ {1}. \\ & & \lambda_ {2} \\ & \ddots \\ \lambda_ {n} \end{array} \right| \tag {1}
$$

解（1）应注意 $D$ 不是上(下)三角形行列式，但可以通过行的对换化为上三角形行列式.先把 $D$ 的第 $n$ 行依次与第 $n - 1$ 行……第1行对换（共 $n - 1$ 次对换），得行列式 $D_{1}$.由性质 $2, D_{1} = (-1)^{n - 1}D$ ，或 $D = (-1)^{n - 1}D_{1}$，这里

$$
D _ {1} = \left| \begin{array}{c c c c c} a _ {n 1} & a _ {n 2} & \dots & a _ {n, n - 1} & a _ {n n} \\ 0 & 0 & \dots & 0 & a _ {1 n} \\ \vdots & \vdots & & \vdots & \vdots \\ 0 & a _ {n - 1, 2} & \dots & a _ {n - 1, n - 1} & a _ {n - 1, n} \end{array} \right|,
$$

再把 $D_{1}$ 的第 $n$ 行依次与第 $n - 1$ 行……第2行对换（共 $n - 2$ 次对换），得一新的行列式……循此，$D$ 经过共

$$
(n - 1) + (n - 2) + \dots + 1 = \frac {1}{2} n (n - 1)
$$

次行的对换成为上三角形行列式

$$
\left| \begin{array}{c c c c} a _ {n 1} & a _ {n 2} & \dots & a _ {n n} \\ & a _ {n - 1, 2} & \dots & a _ {n - 1, n} \\ & & \ddots & \vdots \\ & 0 & & a _ {1 n} \end{array} \right|,
$$

于是 $D = (-1)^{n - 1}D_{1} = \dots = (-1)^{\frac{1}{2} n(n - 1)}a_{1n}a_{2,n - 1}\dots a_{n1};$

(2) 由(1)得

$$
\left| \begin{array}{c c c c} & & & \lambda_ {1} \\ & & \lambda_ {2} \\ & \ddots & \\ \lambda_ {n} & & \end{array} \right| = (- 1) ^ {\frac {n (n - 1)}{2}} \lambda_ {1} \lambda_ {2} \dots \lambda_ {n}.
$$

例7 计算

$$
D = \left| \begin{array}{c c c c} 3 & 1 & - 1 & 2 \\ - 5 & 1 & 3 & - 4 \\ 2 & 0 & 1 & - 1 \\ 1 & - 5 & 3 & - 3 \end{array} \right|.
$$

考研电子书网站:www.pdf2book.com

11

---

第1章 行列式

解 $D\xrightarrow{c_1\leftrightarrow c_2} -\left|\begin{array}{cccc}1 & 3 & -1 & 2\\ 1 & -5 & 3 & -4\\ 0 & 2 & 1 & -1\\ -5 & 1 & 3 & -3 \end{array}\right| \xrightarrow[r_4 + 5r_1]{r_2 - r_1} -\left|\begin{array}{ccc}1 & 3 & -1 & 2\\ 0 & -8 & 4 & -6\\ 0 & 2 & 1 & -1\\ 0 & 16 & -2 & 7 \end{array}\right|$

$$
\begin{array}{l} \underline {{\underline {{r _ {2} \leftrightarrow r _ {3}}}}} \left| \begin{array}{c c c c} 1 & 3 & - 1 & 2 \\ 0 & 2 & 1 & - 1 \\ 0 & - 8 & 4 & - 6 \\ 0 & 1 6 & - 2 & 7 \end{array} \right| \underline {{\underline {{r _ {3} + 4 r _ {2}}}}} \left| \begin{array}{c c c c} 1 & 3 & - 1 & 2 \\ 0 & 2 & 1 & - 1 \\ 0 & 0 & 8 & - 1 0 \\ 0 & 0 & - 1 0 & 1 5 \end{array} \right| \\ = 1 0 \left| \begin{array}{c c c c} 1 & 3 & - 1 & 2 \\ 0 & 2 & 1 & - 1 \\ 0 & 0 & 4 & - 5 \\ 0 & 0 & - 2 & 3 \end{array} \right| \stackrel {r _ {4} + \frac {1}{2} r _ {3}} {=} 1 0 \left| \begin{array}{c c c c} 1 & 3 & - 1 & 2 \\ 0 & 2 & 1 & - 1 \\ 0 & 0 & 4 & - 5 \\ 0 & 0 & 0 & \frac {1}{2} \end{array} \right| = 1 0 \times 4 = 4 0. \\ \end{array}
$$

在上述解法中,先用了运算 $c_{1} \leftrightarrow c_{2}$, 其目的是把 $a_{11}$ 换成 1, 从而利用运算 $r_{i} - a_{i1} r_{1}$, 即可把 $a_{i1} (i = 2,3,4)$ 变为 0. 如果不先作 $c_{1} \leftrightarrow c_{2}$, 则由于原式中 $a_{11} = 3$, 需用运算 $r_{i} - \frac{a_{i1}}{3} r_{1}$ 把 $a_{i1}$ 变为 0, 这样计算时就比较麻烦. 第二步把 $r_{2} - r_{1}$ 和 $r_{4} + 5r_{1}$ 写在一起, 这是两次运算, 并把第一次运算结果的书写省略了.

例8 计算

$$
D = \left| \begin{array}{c c c c} 3 & 1 & 1 & 1 \\ 1 & 3 & 1 & 1 \\ 1 & 1 & 3 & 1 \\ 1 & 1 & 1 & 3 \end{array} \right|.
$$

解 这个行列式的特点是各列 4 个数之和都是 6. 今把第 2,3,4 行同时加到第 1 行, 提出公因子 6, 然后各行减去第一行:

$$
D \xlongequal {r _ {1} + r _ {2} + r _ {3} + r _ {4}} \left| \begin{array}{l l l l} 6 & 6 & 6 & 6 \\ 1 & 3 & 1 & 1 \\ 1 & 1 & 3 & 1 \\ 1 & 1 & 1 & 3 \end{array} \right| = 6 \left| \begin{array}{l l l l} 1 & 1 & 1 & 1 \\ 1 & 3 & 1 & 1 \\ 1 & 1 & 3 & 1 \\ 1 & 1 & 1 & 3 \end{array} \right| \xlongequal [ r _ {4} - r _ {1} ] {r _ {2} - r _ {1}} 6 \left| \begin{array}{l l l l} 1 & 1 & 1 & 1 \\ 0 & 2 & 0 & 0 \\ 0 & 0 & 2 & 0 \\ 0 & 0 & 0 & 2 \end{array} \right| = 4 8.
$$

例9 计算

$$
D = \left| \begin{array}{c c c c} a & b & c & d \\ a & a + b & a + b + c & a + b + c + d \\ a & 2 a + b & 3 a + 2 b + c & 4 a + 3 b + 2 c + d \\ a & 3 a + b & 6 a + 3 b + c & 1 0 a + 6 b + 3 c + d \end{array} \right|.
$$

12

---

§4 行列式的性质

解 从第 4 行开始, 后行减前行,

$$
D \frac {r _ {4} - r _ {3}}{r _ {2} - r _ {1}} \left| \begin{array}{c c c c} a & b & c & d \\ 0 & a & a + b & a + b + c \\ 0 & a & 2 a + b & 3 a + 2 b + c \\ 0 & a & 3 a + b & 6 a + 3 b + c \end{array} \right| \xlongequal {r _ {4} - r _ {3}} \left| \begin{array}{c c c c} a & b & c & d \\ 0 & a & a + b & a + b + c \\ 0 & 0 & a & 2 a + b \\ 0 & 0 & a & 3 a + b \end{array} \right|
$$

$$
\underline {{\underline {{r _ {4} - r _ {3}}}}} \left| \begin{array}{c c c c} a & b & c & d \\ 0 & a & a + b & a + b + c \\ 0 & 0 & a & 2 a + b \\ 0 & 0 & 0 & a \end{array} \right| = a ^ {4}.
$$

上述诸例中都用到把几个运算写在一起的省略写法,这里要注意各个运算的次序一般不能颠倒,这是由于后一次运算是作用在前一次运算结果上的.例如

$$
\begin{array}{l} \left| \begin{array}{c c} a & b \\ c & d \end{array} \right| \stackrel {{r _ {1} + r _ {2}}} {{=}} \left| \begin{array}{c c} a + c & b + d \\ c & d \end{array} \right| \stackrel {{r _ {2} - r _ {1}}} {{=}} \left| \begin{array}{c c} a + c & b + d \\ - a & - b \end{array} \right|, \\ \left| \begin{array}{l l} a & b \\ c & d \end{array} \right| \stackrel {{r _ {2} - r _ {1}}} {{=}} \left| \begin{array}{c c} a & b \\ c - a & d - b \end{array} \right| \stackrel {{r _ {1} + r _ {2}}} {{=}} \left| \begin{array}{c c} c & d \\ c - a & d - b \end{array} \right|, \\ \end{array}
$$

可见当两次运算次序不同时所得结果不同.忽视后一次运算是作用在前一次运算的结果上,就会出错,例如

$$
\left| \begin{array}{l l} a & b \\ c & d \end{array} \right| \frac {r _ {1} + r _ {2}}{\overline {{r _ {2} - r _ {1}}}} \left| \begin{array}{l l} a + c & b + d \\ c - a & d - b \end{array} \right|,
$$

这样的运算是错误的,出错的原因在于第二次运算找错了对象.

此外还要注意运算 $r_i + r_j$ 与 $r_j + r_i$ 的区别，$r_i + kr_j$ 是约定的行列式运算记号，不能写作 $kr_j + r_i$（这里不能套用加法的交换律）.

上述诸例都是利用运算 $r_i + kr_j$ 把行列式化为上三角形行列式，用归纳法不难证明（这里不证）任何 $n$ 阶行列式总能利用运算 $r_i + kr_j$ 化为上三角形行列式，或化为下三角形行列式（这时要先把 $a_{1n}, a_{2n}, \cdots, a_{n-1,n}$ 化为0). 类似地，利用列运算 $c_i + kc_j$ ，也可把行列式化为上三角形行列式或下三角形行列式.

例10 设

$$
D = \left| \begin{array}{c c c c c c} a _ {1 1} & \dots & a _ {1 k} & & & \\ \vdots & & \vdots & & 0 & \\ a _ {k 1} & \dots & a _ {k k} & & & \\ c _ {1 1} & \dots & c _ {1 k} & b _ {1 1} & \dots & b _ {1 n} \\ \vdots & & \vdots & \vdots & & \vdots \\ c _ {n 1} & \dots & c _ {n k} & b _ {n 1} & \dots & b _ {n n} \end{array} \right|,
$$

考研电子书网站:www.pdf2book.com

13

---

第 1 章 行列式

$$
D _ {1} = \det (a _ {i j}) = \left| \begin{array}{c c c} a _ {1 1} & \dots & a _ {1 k} \\ \vdots & & \vdots \\ a _ {k 1} & \dots & a _ {k k} \end{array} \right|, \quad D _ {2} = \det (b _ {i j}) = \left| \begin{array}{c c c} b _ {1 1} & \dots & b _ {1 n} \\ \vdots & & \vdots \\ b _ {n 1} & \dots & b _ {n n} \end{array} \right|,
$$

证明: $D=D_{1}D_{2}.$

证 对 $D_{1}$ 作运算 $r_i + \lambda r_j$ ，把 $D_{1}$ 化为下三角形行列式，设为

$$
D _ {1} = \left| \begin{array}{c c c} p _ {1 1} & & 0 \\ \vdots & \ddots & \\ p _ {k 1} & \dots & p _ {k k} \end{array} \right| = p _ {1 1} \dots p _ {k k},
$$

对 $D_{2}$ 作运算 $c_{i} + \lambda c_{j}$, 把 $D_{2}$ 化为下三角形行列式, 设为

$$
D _ {2} = \left| \begin{array}{c c c} q _ {1 1} & & 0 \\ \vdots & \ddots & \\ q _ {n 1} & \dots & q _ {n n} \end{array} \right| = q _ {1 1} \dots q _ {n n}.
$$

于是,对 D 的前 k 行作运算  $r_{i}+\lambda r_{j}$ , 再对后 n 列作运算  $c_{i}+\lambda c_{j}$ , 把 D 化为下三角形行列式

$$
D = \left| \begin{array}{c c c c c c} p _ {1 1} & & & & & \\ \vdots & \ddots & & & 0 & \\ p _ {k 1} & \dots & p _ {k k} & & \\ c _ {1 1} & \dots & c _ {1 k} & q _ {1 1} & & \\ \vdots & & \vdots & \vdots & \ddots & \\ c _ {n 1} & \dots & c _ {n k} & q _ {n 1} & \dots & q _ {n n} \end{array} \right|,
$$

故

$$
D = p _ {1 1} \dots p _ {k k} q _ {1 1} \dots q _ {n n} = D _ {1} D _ {2}.
$$

例11 计算 $2n$ 阶行列式

$$
D _ {2 n} = \left| \begin{array}{c c c c c c} a & & & & & b \\ & \ddots & & & \ddots \\ & & a & b & & \\ & & c & d & & \\ & \ddots & & & \ddots \\ c & & & & & d \\ \hline & & & & 2 n \end{array} \right|,
$$

其中未写出的元素为0.

解 把 $D_{2n}$ 中的第 $2n$ 行依次与第 $2n - 1$ 行……第2行对换（作 $2n - 2$ 次相邻两行

14

---

§ 5 行列式按行(列)展开

的对换),再把第 $2n$ 列依次与第 $2n - 1$ 列……第2列对换,得

$$
D _ {2 n} = (- 1) ^ {2 (2 n - 2)} \left| \begin{array}{c c c c c c c c} a & b & 0 & & \dots & & & 0 \\ c & d & 0 & & \dots & & & 0 \\ 0 & 0 & a & & & & & b \\ & & & \ddots & & & \ddots \\ \vdots & \vdots & & & a & b & \\ & & & & c & d \\ & & & \ddots & & & \ddots \\ 0 & 0 & c & & & & d \end{array} \right|, \underbrace {} _ {2 (n - 1)}
$$

根据例 10 的结果,有

$$
D _ {2 n} = D _ {2} D _ {2 (n - 1)} = (a d - b c) D _ {2 (n - 1)}.
$$

以此作递推公式,即得

$$
D _ {2 n} = (a d - b c) ^ {2} D _ {2 (n - 2)} = \dots = (a d - b c) ^ {n - 1} D _ {2} = (a d - b c) ^ {n}.
$$

## § 5 行列式按行(列)展开

一般说来,低阶行列式的计算比高阶行列式的计算要简便,于是,我们自然地考虑用低阶行列式来表示高阶行列式的问题.为此,先引进余子式和代数余子式的概念.

在 $n$ 阶行列式中, 把 $(i,j)$ 元 $a_{ij}$ 所在的第 $i$ 行和第 $j$ 列划去后, 留下来的 $n-1$ 阶行列式叫做 $(i,j)$ 元 $a_{ij}$ 的余子式, 记作 $M_{ij}$; 记

$$
A _ {i j} = (- 1) ^ {i + j} M _ {i j},
$$

$A_{ij}$ 叫做 $(i,j)$ 元 $a_{ij}$ 的代数余子式.

例如四阶行列式

$$
D = \left| \begin{array}{c c c c} a _ {1 1} & a _ {1 2} & a _ {1 3} & a _ {1 4} \\ a _ {2 1} & a _ {2 2} & a _ {2 3} & a _ {2 4} \\ a _ {3 1} & a _ {3 2} & a _ {3 3} & a _ {3 4} \\ a _ {4 1} & a _ {4 2} & a _ {4 3} & a _ {4 4} \end{array} \right|
$$

中(3,2)元 $a_{32}$ 的余子式和代数余子式分别为

$$
M _ {3 2} = \left| \begin{array}{l l l} a _ {1 1} & a _ {1 3} & \dot {a} _ {1 4} \\ a _ {2 1} & a _ {2 3} & a _ {2 4} \\ a _ {4 1} & a _ {4 3} & a _ {4 4} \end{array} \right|, \quad A _ {3 2} = (- 1) ^ {3 + 2} M _ {3 2} = - M _ {3 2}.
$$

考研电子书网站:www.pdf2book.com

15

---

第1章 行列式

引理 一个 $n$ 阶行列式, 如果其中第 $i$ 行所有元素除 $(i,j)$ 元 $a_{ij}$ 外都为零, 那么这个行列式等于 $a_{ij}$ 与它的代数余子式的乘积, 即

$$
D = a _ {i j} A _ {i j}.
$$

证 先证 $i = j = 1$ 的情形. 此时

$$
D = \left| \begin{array}{c c c c} a _ {1 1} & 0 & \dots & 0 \\ a _ {2 1} & a _ {2 2} & \dots & a _ {2 n} \\ \vdots & \vdots & & \vdots \\ a _ {n 1} & a _ {n 2} & \dots & a _ {n n} \end{array} \right|,
$$

这是例10中当 $k = 1$ 时的特殊情形，按例10的结论，即有

$$
D = a _ {1 1} M _ {1 1},
$$

又

$$
A _ {1 1} = (- 1) ^ {1 + 1} M _ {1 1} = M _ {1 1},
$$

从而

$$
D = a _ {1 1} A _ {1 1}.
$$

再证一般情形.此时

$$
D = \left| \begin{array}{c c c c c} a _ {1 1} & \dots & a _ {1 j} & \dots & a _ {1 n} \\ \vdots & & \vdots & & \vdots \\ 0 & \dots & a _ {i j} & \dots & 0 \\ \vdots & & \vdots & & \vdots \\ a _ {n 1} & \dots & a _ {n j} & \dots & a _ {n n} \end{array} \right|.
$$

为了利用前面的结果，把 $D$ 的行列作如下调换:把 $D$ 的第 $i$ 行依次与第 $i - 1$ 行、第 $i - 2$ 行……第1行对换，这样数 $a_{ij}$ 就换成 $(1,j)$ 元，对换的次数为 $i - 1$.再把第$j$ 列依次与第 $j - 1$ 列、第 $j - 2$ 列……第1列对换，这样数 $a_{ij}$ 就换成(1,1)元，对换的次数为 $j - 1$.总之，经 $i + j - 2$ 次对换，把数 $a_{ij}$ 换成(1,1)元，所得的行列式 $D_{1} = (-1)^{i + j - 2}D = (-1)^{i + j}D$ ，而 $D_{1}$ 中(1,1)元的余子式就是 $D$ 中 $(i,j)$ 元的余子式 $M_{ij}$.

由于 $D_{1}$ 的(1,1)元为 $a_{ij}$, 第1行其余元素都为0, 利用前面的结果, 有

$$
D _ {1} = a _ {i j} M _ {i j},
$$

于是

$$
D = (- 1) ^ {i + j} D _ {1} = (- 1) ^ {i + j} a _ {i j} M _ {i j} = a _ {i j} A _ {i j}.
$$

证毕

定理 2 行列式等于它的任一行(列)的各元素与其对应的代数余子式乘积之和, 即

$$
D = a _ {i 1} A _ {i 1} + a _ {i 2} A _ {i 2} + \dots + a _ {i n} A _ {i n} \quad (i = 1, 2, \dots , n)
$$

或

16

---

§ 5 行列式按行(列)展开

$$
D = a _ {1 j} A _ {1 j} + a _ {2 j} A _ {2 j} + \dots + a _ {n j} A _ {n j} \quad (j = 1, 2, \dots , n).
$$

证 $D = \left| \begin{array}{cccc}a_{11} & a_{12} & \dots & a_{1n}\\ \vdots & \vdots &  & \vdots \\ a_{i1} + 0 + \dots +0 & 0 + a_{i2} + \dots +0 & \dots & 0 + \dots +0 + a_{in}\\ \vdots & \vdots &  & \vdots \\ a_{n1} & a_{n2} & \dots & a_{nn} \end{array} \right|$

$$
= \left| \begin{array}{c c c c} a _ {1 1} & a _ {1 2} & \dots & a _ {1 n} \\ \vdots & \vdots & & \vdots \\ a _ {i 1} & 0 & \dots & 0 \\ \vdots & \vdots & & \vdots \\ a _ {n 1} & a _ {n 2} & \dots & a _ {n n} \end{array} \right| + \left| \begin{array}{c c c c} a _ {1 1} & a _ {1 2} & \dots & a _ {1 n} \\ \vdots & \vdots & & \vdots \\ 0 & a _ {i 2} & \dots & 0 \\ \vdots & \vdots & & \vdots \\ a _ {n 1} & a _ {n 2} & \dots & a _ {n n} \end{array} \right| + \dots + \left| \begin{array}{c c c c} a _ {1 1} & a _ {1 2} & \dots & a _ {1 n} \\ \vdots & \vdots & & \vdots \\ 0 & 0 & \dots & a _ {i n} \\ \vdots & \vdots & & \vdots \\ a _ {n 1} & a _ {n 2} & \dots & a _ {n n} \end{array} \right|,
$$

根据引理,即得

$$
D = a _ {i 1} A _ {i 1} + a _ {i 2} A _ {i 2} + \dots + a _ {i n} A _ {i n} \quad (i = 1, 2, \dots , n).
$$

类似地,若按列证明,可得

$$
D = a _ {1 j} A _ {1 j} + a _ {2 j} A _ {2 j} + \dots + a _ {n j} A _ {n j} \quad (j = 1, 2, \dots , n). \quad \text {证毕}
$$

这个定理叫做行列式按行(列)展开法则.利用这一法则并结合行列式的性质,可以简化行列式的计算.

例 7(续) 用行列式按行(列)展开法则计算例 7 中的行列式

$$
D = \left| \begin{array}{c c c c} 3 & 1 & - 1 & 2 \\ - 5 & 1 & 3 & - 4 \\ 2 & 0 & 1 & - 1 \\ 1 & - 5 & 3 & - 3 \end{array} \right|.
$$

解 保留 $a_{33}$, 把第 3 行其余元素变为 0, 然后按第 3 行展开,

$$
\begin{array}{l} D \xlongequal [ c _ {4} + c _ {3} ] {c _ {1} - 2 c _ {3}} \left| \begin{array}{c c c c} 5 & 1 & - 1 & 1 \\ - 1 1 & 1 & 3 & - 1 \\ 0 & 0 & 1 & 0 \\ - 5 & - 5 & 3 & 0 \end{array} \right| = (- 1) ^ {3 + 3} \left| \begin{array}{c c c} 5 & 1 & 1 \\ - 1 1 & 1 & - 1 \\ - 5 & - 5 & 0 \end{array} \right| \\ \underline {{\underline {{r _ {2} + r _ {1}}}}} \left| \begin{array}{c c c} 5 & 1 & 1 \\ - 6 & 2 & 0 \\ - 5 & - 5 & 0 \end{array} \right| = (- 1) ^ {1 + 3} \left| \begin{array}{c c} - 6 & 2 \\ - 5 & - 5 \end{array} \right| \underline {{\underline {{c _ {1} - c _ {2}}}}} \left| \begin{array}{c c} - 8 & 2 \\ 0 & - 5 \end{array} \right| = 4 0. \\ \end{array}
$$

例 12 证明范德蒙德(Vandermonde)行列式

考研电子书网站:www.pdf2book.com

17

---

第1章 行列式

$$
D _ {n} = \left| \begin{array}{c c c c} 1 & 1 & \dots & 1 \\ x _ {1} & x _ {2} & \dots & x _ {n} \\ x _ {1} ^ {2} & x _ {2} ^ {2} & \dots & x _ {n} ^ {2} \\ \vdots & \vdots & & \vdots \\ x _ {1} ^ {n - 1} & x _ {2} ^ {n - 1} & \dots & x _ {n} ^ {n - 1} \end{array} \right| = \prod_ {n \geqslant i > j \geqslant 1} (x _ {i} - x _ {j}), \tag {8}
$$

其中记号“$\Pi$”表示全体同类因子的乘积.

证 用数学归纳法. 因为

$$
D _ {2} = \left| \begin{array}{c c} 1 & 1 \\ x _ {1} & x _ {2} \end{array} \right| = x _ {2} - x _ {1} = \prod_ {2 \geqslant i > j \geqslant 1} (x _ {i} - x _ {j}),
$$

所以当 $n = 2$ 时(8)式成立.现在假设(8)式对于 $n - 1$ 阶范德蒙德行列式成立，要证(8)式对 $n$ 阶范德蒙德行列式也成立.

为此,设法把 $D_{n}$ 降阶:从第n行开始,后行减去前行的 $x_{1}$ 倍,有

$$
D _ {n} = \left| \begin{array}{c c c c c} 1 & 1 & 1 & \dots & 1 \\ 0 & x _ {2} - x _ {1} & x _ {3} - x _ {1} & \dots & x _ {n} - x _ {1} \\ 0 & x _ {2} (x _ {2} - x _ {1}) & x _ {3} (x _ {3} - x _ {1}) & \dots & x _ {n} (x _ {n} - x _ {1}) \\ \vdots & \vdots & \vdots & & \vdots \\ 0 & x _ {2} ^ {n - 2} (x _ {2} - x _ {1}) & x _ {3} ^ {n - 2} (x _ {3} - x _ {1}) & \dots & x _ {n} ^ {n - 2} (x _ {n} - x _ {1}) \end{array} \right|,
$$

按第1列展开，并把每列的公因子 $(x_{i} - x_{1})$ 提出，就有

$$
D _ {n} = (x _ {2} - x _ {1}) (x _ {3} - x _ {1}) \dots (x _ {n} - x _ {1}) \left| \begin{array}{c c c c} 1 & 1 & \dots & 1 \\ x _ {2} & x _ {3} & \dots & x _ {n} \\ \vdots & \vdots & & \vdots \\ x _ {2} ^ {n - 2} & x _ {3} ^ {n - 2} & \dots & x _ {n} ^ {n - 2} \end{array} \right|,
$$

上式右端的行列式是 $n - 1$ 阶范德蒙德行列式，按归纳法假设，它等于所有 $(x_{i} - x_{j})$ 因子的乘积，其中 $n\geqslant i > j\geqslant 2.$ 故

$$
D _ {n} = \left(x _ {2} - x _ {1}\right) \left(x _ {3} - x _ {1}\right) \dots \left(x _ {n} - x _ {1}\right) \prod_ {n \geqslant i > j \geqslant 2} \left(x _ {i} - x _ {j}\right) = \prod_ {n \geqslant i > j \geqslant 1} \left(x _ {i} - x _ {j}\right). \quad \text {证毕}
$$

例11和例12都是计算 $n$ 阶行列式. 计算 $n$ 阶行列式, 常要使用数学归纳法, 在比较简单的情形 (如例11), 可省略归纳法的叙述格式, 但归纳法的主要步骤是不可能省略的. 这主要步骤是: 导出递推公式 (例11中导出 $D_{2n} = (ad - bc)D_{2(n - 1)}$) 及检验 $n = 1$ 时结论成立 (例11中最后用到 $D_{2} = ad - bc$).

下面来推导行列式的另一重要性质,并将它作为定理2的推论.

设有 $n$ 阶行列式 $D = \det(a_{ij})$, 我们已得到它的按第 $j$ 行展开式

$$
D = a _ {j 1} A _ {j 1} + a _ {j 2} A _ {j 2} + \dots + a _ {j n} A _ {j n}.
$$

18

---

§5 行列式按行(列)展开

因诸 $A_{jk}(k = 1,2,\dots ,n)$ 都是先划去了 $D$ 中第 $j$ 行再经计算而得，所以当第 $j$ 行元素依次取为 $b_{1},b_{2},\dots ,b_{n}$ 时就有

$$
D _ {j} = \left| \begin{array}{c c c c} a _ {1 1} & a _ {1 2} & \dots & a _ {1 n} \\ \vdots & \vdots & & \vdots \\ a _ {j - 1, 1} & a _ {j - 1, 2} & \dots & a _ {j - 1, n} \\ b _ {1} & b _ {2} & \dots & b _ {n} \\ a _ {j + 1, 1} & a _ {j + 1, 2} & \dots & a _ {j + 1, n} \\ \vdots & \vdots & & \vdots \\ a _ {n 1} & a _ {n 2} & \dots & a _ {n n} \end{array} \right| = b _ {1} A _ {j 1} + b _ {2} A _ {j 2} + \dots + b _ {n} A _ {j n}. \tag {9}
$$

这里 $D_{j}$ 表示除第 $j$ 行外其余各行均与 $D$ 相同的行列式.

特别地, 当 $b_{1}, b_{2}, \cdots, b_{n}$ 依次取为 $D = \det(a_{ij})$ 的第 $i$ 行 ($i \neq j$) 各元素时, 上式仍成立. 但此时因 $D_{j}$ 中第 $j$ 行与第 $i$ 行两行相同, 故 $D_{j} = 0$, 从而有

$$
a _ {i 1} A _ {j 1} + a _ {i 2} A _ {j 2} + \dots + a _ {i n} A _ {j n} = 0 \quad (i \neq j).
$$

对列作相仿的讨论可知

$$
\left| \begin{array}{c c c c c c c} a _ {1 1} & \dots & a _ {1, j - 1} & b _ {1} & a _ {1, j + 1} & \dots & a _ {1 n} \\ \vdots & & \vdots & \vdots & \vdots & & \vdots \\ a _ {n 1} & \dots & a _ {n, j - 1} & b _ {n} & a _ {n, j + 1} & \dots & a _ {n n} \end{array} \right| = b _ {1} A _ {1 j} + b _ {2} A _ {2 j} + \dots + b _ {n} A _ {n j}. \tag {10}
$$

特别地，有

$$
a _ {1 i} A _ {1 j} + a _ {2 i} A _ {2 j} + \dots + a _ {n i} A _ {n j} = 0 \quad (i \neq j).
$$

这样得到了下述推论:

推论 行列式某一行(列)的元素与另一行(列)的对应元素的代数余子式乘积之和等于零. 即

$$
a _ {i 1} A _ {j 1} + a _ {i 2} A _ {j 2} + \dots + a _ {i n} A _ {j n} = 0, \quad i \neq j
$$

或

$$
a _ {1 i} A _ {1 j} + a _ {2 i} A _ {2 j} + \dots + a _ {n i} A _ {n j} = 0, \quad i \neq j.
$$

综合定理 2 及其推论,有关于代数余子式的重要性质:

$$
\sum_ {k = 1} ^ {n} a _ {k i} A _ {k j} = \left\{ \begin{array}{l l} D, & \text {当} i = j, \\ 0, & \text {当} i \neq j \end{array} \right.
$$

或

$$
\sum_ {k = 1} ^ {n} a _ {i k} A _ {j k} = \left\{ \begin{array}{l l} D, & \text {当} i = j, \\ 0, & \text {当} i \neq j. \end{array} \right.
$$

例13 设

考研电子书网站:www.pdf2book.com

19

---

第1章 行列式

$$
D = \left| \begin{array}{c c c c} 3 & - 5 & 2 & 1 \\ 1 & 1 & 0 & - 5 \\ - 1 & 3 & 1 & 3 \\ 2 & - 4 & - 1 & - 3 \end{array} \right|,
$$

D 的  $(i,j)$  元的余子式和代数余子式依次记作  $M_{ij}$  和  $A_{ij}$ ，求

$$
A _ {1 1} + A _ {1 2} + A _ {1 3} + A _ {1 4} \quad \text {及} \quad M _ {1 1} + M _ {2 1} + M _ {3 1} + M _ {4 1}.
$$

解 按(9)式可知 $A_{11} + A_{12} + A_{13} + A_{14}$ 等于用1,1,1,1代替 $D$ 的第1行所得的行列式，即

$$
\begin{array}{l} A _ {1 1} + A _ {1 2} + A _ {1 3} + A _ {1 4} \\ = \left| \begin{array}{c c c c} 1 & 1 & 1 & 1 \\ 1 & 1 & 0 & - 5 \\ - 1 & 3 & 1 & 3 \\ 2 & - 4 & - 1 & - 3 \end{array} \right| \frac {r _ {4} + r _ {3}}{\overline {{r _ {3} - r _ {1}}}} \left| \begin{array}{c c c c} 1 & 1 & 1 & 1 \\ 1 & 1 & 0 & - 5 \\ - 2 & 2 & 0 & 2 \\ 1 & - 1 & 0 & 0 \end{array} \right| \\ = \left| \begin{array}{r r r} 1 & 1 & - 5 \\ - 2 & 2 & 2 \\ 1 & - 1 & 0 \end{array} \right| \stackrel {{c _ {2} + c _ {1}}} {{=}} \left| \begin{array}{r r r} 1 & 2 & - 5 \\ - 2 & 0 & 2 \\ 1 & 0 & 0 \end{array} \right| = \left| \begin{array}{c c} 2 & - 5 \\ 0 & 2 \end{array} \right| = 4. \\ \end{array}
$$

按(10)式可知

$$
\begin{array}{l} M _ {1 1} + M _ {2 1} + M _ {3 1} + M _ {4 1} = A _ {1 1} - A _ {2 1} + A _ {3 1} - A _ {4 1} \\ = \left| \begin{array}{r r r r} 1 & - 5 & 2 & 1 \\ - 1 & 1 & 0 & - 5 \\ 1 & 3 & 1 & 3 \\ - 1 & - 4 & - 1 & - 3 \end{array} \right| \stackrel {r _ {4} + r _ {3}} {=} \left| \begin{array}{r r r r} 1 & - 5 & 2 & 1 \\ - 1 & 1 & 0 & - 5 \\ 1 & 3 & 1 & 3 \\ 0 & - 1 & 0 & 0 \end{array} \right| \\ = (- 1) \left| \begin{array}{c c c} 1 & 2 & 1 \\ - 1 & 0 & - 5 \\ 1 & 1 & 3 \end{array} \right| \stackrel {r _ {1} - 2 r _ {3}} {=} - \left| \begin{array}{c c c} - 1 & 0 & - 5 \\ - 1 & 0 & - 5 \\ 1 & 1 & 3 \end{array} \right| = 0. \\ \end{array}
$$

## 习题一

1. 利用对角线法则计算下列三阶行列式:

(1) $\begin{vmatrix}2&0&1\\1&-4&-1\\-1&8&3\end{vmatrix};$

(2) $\begin{vmatrix}a&b&c\\b&c&a\\c&a&b\end{vmatrix};$

20

---

习题一

(3) $\begin{vmatrix}1&1&1\\a&b&c\\a^{2}&b^{2}&c^{2}\end{vmatrix};$

(4) $\begin{vmatrix}x & y & x+y \\ y & x+y & x \\ x+y & x & y\end{vmatrix}.$

2. 按自然数从小到大为标准次序, 求下列排列的逆序数:

(1) 1234;

(2) 4132;

(3) 3421;

(4) 2413;

(5)  $13\cdots(2n-1)24\cdots(2n)$ ;

(6)  $13\cdots(2n-1)(2n)(2n-2)\cdots2.$

3. 写出四阶行列式中含有因子  $a_{11}a_{23}$  的项.

4. 计算下列行列式:

(1) $\begin{vmatrix}4&1&2&4\\1&2&0&2\\10&5&2&0\\0&1&1&7\end{vmatrix};$

(2) $\begin{vmatrix}2&1&4&1\\3&-1&2&1\\1&2&3&2\\5&0&6&2\end{vmatrix};$

(3) $\begin{vmatrix}-ab&ac&ae\\bd&-cd&de\\bf&cf&-ef\end{vmatrix};$

(4) $\begin{vmatrix}1&1&1\\a&b&c\\b+c&c+a&a+b\end{vmatrix};$

(5) $\begin{vmatrix}a&1&0&0\\-1&b&1&0\\0&-1&c&1\\0&0&-1&d\end{vmatrix};$

(6) $\begin{vmatrix}1&2&3&4\\1&3&4&1\\1&4&1&2\\1&1&2&3\end{vmatrix}.$

5. 求解下列方程:

(1) $\begin{vmatrix}x+1&2&-1\\2&x+1&1\\-1&1&x+1\end{vmatrix}=0;$

(2) $\begin{vmatrix}1&1&1&1\\x&a&b&c\\x^{2}&a^{2}&b^{2}&c^{2}\\x^{3}&a^{3}&b^{3}&c^{3}\end{vmatrix}=0,$ 其中a,b,c互不相等.

6. 证明:

(1) $\begin{vmatrix}a^{2}&ab&b^{2}\\ 2a&a+b&2b\\ 1&1&1\end{vmatrix}=(a-b)^{3};$

(2) $\begin{vmatrix} ax+by & ay+bz & az+bx \\ ay+bz & az+bx & ax+by \\ az+bx & ax+by & ay+bz \end{vmatrix} = (a^3 + b^3) \begin{vmatrix} x & y & z \\ y & z & x \\ z & x & y \end{vmatrix};$

(3) $\begin{vmatrix}a^{2}&(a+1)^{2}&(a+2)^{2}&(a+3)^{2}\\b^{2}&(b+1)^{2}&(b+2)^{2}&(b+3)^{2}\\c^{2}&(c+1)^{2}&(c+2)^{2}&(c+3)^{2}\\d^{2}&(d+1)^{2}&(d+2)^{2}&(d+3)^{2}\end{vmatrix}=0;$

(4) $\begin{vmatrix}1&1&1&1\\a&b&c&d\\a^{2}&b^{2}&c^{2}&d^{2}\\a^{4}&b^{4}&c^{4}&d^{4}\end{vmatrix}=(a-b)(a-c)(a-d)(b-c)(b-d)(c-d)(a+b+c+d);$

考研电子书网站:www.pdf2book.com

21

---

第1章 行列式

(5)

$$
\left| \begin{array}{c c c c} x & - 1 & 0 & 0 \\ 0 & x & - 1 & 0 \\ 0 & 0 & x & - 1 \\ a _ {0} & a _ {1} & a _ {2} & a _ {3} \end{array} \right| = a _ {3} x ^ {3} + a _ {2} x ^ {2} + a _ {1} x + a _ {0}.
$$

7. 设 $n$ 阶行列式 $D = \det(a_{ij})$, 把 $D$ 上下翻转、逆时针旋转 $90^{\circ}$ 或依副对角线翻转, 依次得

$$
D _ {1} = \left| \begin{array}{c c c c} a _ {n 1} & a _ {n 2} & \dots & a _ {n n} \\ \vdots & \vdots & & \vdots \\ a _ {2 1} & a _ {2 2} & \dots & a _ {2 n} \\ a _ {1 1} & a _ {1 2} & \dots & a _ {1 n} \end{array} \right|, D _ {2} = \left| \begin{array}{c c c c} a _ {1 n} & a _ {2 n} & \dots & a _ {n n} \\ \vdots & \vdots & & \vdots \\ a _ {1 2} & a _ {2 2} & \dots & a _ {n 2} \\ a _ {1 1} & a _ {2 1} & \dots & a _ {n 1} \end{array} \right|, D _ {3} = \left| \begin{array}{c c c c} a _ {n n} & \dots & a _ {2 n} & a _ {1 n} \\ \vdots & & \vdots & \vdots \\ a _ {n 2} & \dots & a _ {2 2} & a _ {1 2} \\ a _ {n 1} & \dots & a _ {2 1} & a _ {1 1} \end{array} \right|,
$$

证明 $D_{1} = D_{2} = (-1)^{\frac{n(n - 1)}{2}}D, D_{3} = D.$

8. 计算下列行列式 $(D_{k}$ 为 k 阶行列式):

(1) $D_{n} = \left| \begin{array}{cccc}a & & & & 1\\ & a & & & \\ & & \ddots & & \\ 1 & & & & a \end{array} \right|$ ,其中对角线上元素都是 $a$ ，未写出的元素都是0；

(2) $D_{n}=\left|\begin{array}{cccc}x&a&\cdots&a\\a&a&\cdots&a\\\vdots&\vdots&&\vdots\\a&a&\cdots&x\end{array}\right|$ ;

(3) $D_{n+1}=\begin{vmatrix}a^{n}&(a-1)^{n}&\cdots&(a-n)^{n}\\a^{n-1}&(a-1)^{n-1}&\cdots&(a-n)^{n-1}\\ \vdots&\vdots&&\vdots\\ a&a-1&\cdots&a-n\\ 1&1&\cdots&1\end{vmatrix};$

(4) $D_{2n} = \left| \begin{array}{cccc}a_n &  &  &  &  & b_n\\  & \ddots &  &  & \ddots &  \\  &  & a_1 & b_1 &  &  \\  &  & c_1 & d_1 &  &  \\  & \ddots &  &  & \ddots &  \\ c_n &  &  &  &  & d_n \end{array} \right|$ 其中未写出的元素都是0；

(5) $D_{n}=\left|\begin{array}{cccc}1+a_{1}&a_{1}&\cdots&a_{1}\\a_{2}&1+a_{2}&\cdots&a_{2}\\ \vdots&\vdots&&\vdots\\a_{n}&a_{n}&\cdots&1+a_{n}\end{array}\right|;$

22

---

习题一

(6) $D_{n}=\det(a_{ij})$ , 其中  $a_{ij}=|i-j|$ ;
(7) $D_{n}=\left|\begin{array}{cccc}1+a_{1}&1&\cdots&1\\1&1+a_{2}&\cdots&1\\\vdots&\vdots&&\vdots\\1&1&\cdots&1+a_{n}\end{array}\right|$ ，其中 $a_{1}a_{2}\cdots a_{n}\neq0.$

9. 设 $D = \left| \begin{array}{cccc} 3 & 1 & -1 & 2 \\ -5 & 1 & 3 & -4 \\ 2 & 0 & 1 & -1 \\ 1 & -5 & 3 & -3 \end{array} \right|$, $D$ 的 $(i,j)$ 元的代数余子式记作 $A_{ij}$, 求

$$
A _ {3 1} + 3 A _ {3 2} - 2 A _ {3 3} + 2 A _ {3 4}.
$$

![](raw/pages_0001-0032/images/page_26_image_6.jpg)

![](raw/pages_0001-0032/images/page_26_image_7.jpg)

考研电子书网站:www.pdf2book.com

23

---

# 第2章

# 矩阵及其运算

本章将介绍代数学中的重要工具——矩阵，并讨论矩阵的各种运算以及矩阵的分块表示法.

## § 1 线性方程组和矩阵

## 一、线性方程组

设有 $n$ 个未知数 $m$ 个方程的线性方程组

$$
\left\{ \begin{array}{l} a _ {1 1} x _ {1} + a _ {1 2} x _ {2} + \dots + a _ {1 n} x _ {n} = b _ {1}, \\ a _ {2 1} x _ {1} + a _ {2 2} x _ {2} + \dots + a _ {2 n} x _ {n} = b _ {2}, \\ \dots \dots \\ a _ {m 1} x _ {1} + a _ {m 2} x _ {2} + \dots + a _ {m n} x _ {n} = b _ {m}, \end{array} \right. \tag {1}
$$

其中  $a_{ij}$  是第 i 个方程的第 j 个未知数的系数， $b_{i}$  是第 i 个方程的常数项， $i=1,2,\cdots,m$ ;  $j=1,2,\cdots,n$ ，当常数项  $b_{1},b_{2},\cdots,b_{m}$  不全为零时，线性方程组(1)叫做 n 元非齐次线性方程组，当  $b_{1},b_{2},\cdots,b_{m}$  全为零时，(1)式成为

$$
\left\{ \begin{array}{l} a _ {1 1} x _ {1} + a _ {1 2} x _ {2} + \dots + a _ {1 n} x _ {n} = 0, \\ a _ {2 1} x _ {1} + a _ {2 2} x _ {2} + \dots + a _ {2 n} x _ {n} = 0, \\ \dots \dots \\ a _ {m 1} x _ {1} + a _ {m 2} x _ {2} + \dots + a _ {m n} x _ {n} = 0, \end{array} \right. \tag {2}
$$

叫做 n 元齐次线性方程组.

n 元线性方程组往往简称为线性方程组或方程组.

对于 n 元齐次线性方程组(2),  $x_{1}=x_{2}=\cdots=x_{n}=0$  一定是它的解, 这个解叫做齐次

24

---

§1 线性方程组和矩阵

线性方程组(2)的零解.如果一组不全为零的数是(2)的解,则它叫做齐次线性方程组 (2)的非零解.齐次线性方程组(2)一定有零解,但不一定有非零解.

例如

$$
\text {①} \left\{ \begin{array}{l} x - y = 0, \\ x + y = 2; \end{array} \right. \quad \text {②} \left\{ \begin{array}{l} x - y = 0, \\ x + y = 1, \\ x + y = 2; \end{array} \right. \quad \text {③} \left\{ \begin{array}{l} x _ {1} - x _ {2} = 0, \\ 2 x _ {1} - 2 x _ {2} = 0, \\ 3 x _ {1} - 3 x _ {2} = 0 \end{array} \right.
$$

就是三个二元线性方程组,并且③是齐次方程组.

下面讨论这三个方程组的解. 方程组①: 易知其有惟一解 $x = y = 1$; 方程组②: 显然不存在数 $x$ 和 $y$ 使 $x + y = 1$ 和 $x + y = 2$ 同时成立, 故方程组②无解; 方程组③: 设 $s$ 为任一数, 那么 $x_{1} = x_{2} = s$ 是③的解, 从而方程组③有无限多个解.

这样看来,对于线性方程组需要讨论以下问题:(1) 它是否有解?(2) 在有解时它的解是否惟一?(3) 如果有多个解,如何求出它的所有解?

对于线性方程组(1)，上述诸问题的答案完全取决于它的 $mn$ 个系数 $a_{ij}$ ($i=1,2,\cdots,m$; $j=1,2,\cdots,n$) 和右端的常数项 $b_1, b_2, \cdots, b_m$ 所构成的 $m$ 行 $n+1$ 列的矩形数表

$$
\begin{array}{c c c c c} a _ {1 1} & a _ {1 2} & \dots & a _ {1 n} & b _ {1} \\ a _ {2 1} & a _ {2 2} & \dots & a _ {2 n} & b _ {2} \\ \vdots & \vdots & & \vdots & \vdots \\ a _ {m 1} & a _ {m 2} & \dots & a _ {m n} & b _ {m} \end{array} ,
$$

这里横排称为行,竖排称为列;而对于齐次线性方程组(2)的相应问题的答案也完全取决于它的mn个系数 $a_{ij}(i=1,2,\cdots,m;j=1,2,\cdots,n)$ 所构成的m行n列的矩形数表

$$
\begin{array}{c c c c} a _ {1 1} & a _ {1 2} & \dots & a _ {1 n} \\ a _ {2 1} & a _ {2 2} & \dots & a _ {2 n} \\ \vdots & \vdots & & \vdots \\ a _ {m 1} & a _ {m 2} & \dots & a _ {m n} \end{array} .
$$

由此我们引入矩阵的概念.

## 二、矩阵的定义

定义1 由 $mn$ 个数 $a_{ij}$ $(i = 1,2,\dots ,m;j = 1,2,\dots ,n)$ 排成的 $m$ 行 $n$ 列的数表

$$
\begin{array}{c c c c} a _ {1 1} & a _ {1 2} & \dots & a _ {1 n} \\ a _ {2 1} ^ {\prime} & a _ {2 2} & \dots & a _ {2 n} \\ \vdots & \vdots & & \vdots \\ a _ {m 1} & a _ {m 2} & \dots & a _ {m n} \end{array}
$$

考研电子书网站:www.pdf2book.com

25

---

第2章 矩阵及其运算

称为 $m$ 行 $n$ 列矩阵, 简称 $m \times n$ 矩阵. 为表示它是一个整体, 总是加一个括弧, 并用大写黑体字母表示它, 记作

$$
\boldsymbol {A} = \left( \begin{array}{c c c c} a _ {1 1} & a _ {1 2} & \dots & a _ {1 n} \\ a _ {2 1} & a _ {2 2} & \dots & a _ {2 n} \\ \vdots & \vdots & & \vdots \\ a _ {m 1} & a _ {m 2} & \dots & a _ {m n} \end{array} \right),
$$

这 $m \times n$ 个数称为矩阵 $\mathbf{A}$ 的元素, 简称为元, 数 $a_{ij}$ 位于矩阵 $\mathbf{A}$ 的第 $i$ 行第 $j$ 列, 称为矩阵 $\mathbf{A}$ 的 $(i,j)$ 元. 以数 $a_{ij}$ 为 $(i,j)$ 元的矩阵可简记作 $(a_{ij})$ 或 $(a_{ij})_{m \times n}$. $m \times n$ 矩阵 $\mathbf{A}$ 也记作 $A_{m \times n}$.

元素是实数的矩阵称为实矩阵,元素是复数的矩阵称为复矩阵,本书中的矩阵除特别说明外,都指实矩阵. 公众号: 旗胜考研

行数与列数都等于 $n$ 的矩阵称为 $\underline{n}$ 阶矩阵或 $\underline{n}$ 阶方阵. $n$ 阶矩阵 $A$ 也记作 $A_{n}$.

只有一行的矩阵

$$
A = (a _ {1} a _ {2} \dots a _ {n})
$$

称为行矩阵,又称行向量.为避免元素间的混淆,行矩阵也记作

$$
A = (a _ {1}, a _ {2}, \dots , a _ {n}).
$$

只有一列的矩阵

$$
\boldsymbol {B} = \left( \begin{array}{c} b _ {1} \\ b _ {2} \\ \vdots \\ b _ {m} \end{array} \right)
$$

称为列矩阵,又称列向量.

两个矩阵的行数相等、列数也相等时, 就称它们是同型矩阵. 如果 $A = (a_{ij})$ 与 $B = (b_{ij})$ 是同型矩阵, 并且它们的对应元素相等, 即

$$
a _ {i j} = b _ {i j} \quad (i = 1, 2, \dots , m; j = 1, 2, \dots , n),
$$

那么就称矩阵 A 与矩阵 B 相等, 记作

$$
A = B.
$$

元素都是零的矩阵称为零矩阵,记作 O. 注意不同型的零矩阵是不同的.

例1 对于非齐次线性方程组

$$
\left\{ \begin{array}{l} a _ {1 1} x _ {1} + a _ {1 2} x _ {2} + \dots + a _ {1 n} x _ {n} = b _ {1}, \\ a _ {2 1} x _ {1} + a _ {2 2} x _ {2} + \dots + a _ {2 n} x _ {n} = b _ {2}, \\ \dots \dots \\ a _ {m 1} x _ {1} + a _ {m 2} x _ {2} + \dots + a _ {m n} x _ {n} = b _ {m}, \end{array} \right. \tag {1}
$$

26

---

§1 线性方程组和矩阵

有如下几个有用的矩阵:

$$
\boldsymbol {A} = (a _ {i j}), \quad \boldsymbol {x} = \left( \begin{array}{c} x _ {1} \\ x _ {2} \\ \vdots \\ x _ {n} \end{array} \right), \quad \boldsymbol {b} = \left( \begin{array}{c} b _ {1} \\ b _ {2} \\ \vdots \\ b _ {m} \end{array} \right), \quad \boldsymbol {B} = \left( \begin{array}{c c c c c} a _ {1 1} & a _ {1 2} & \dots & a _ {1 n} & b _ {1} \\ a _ {2 1} & a _ {2 2} & \dots & a _ {2 n} & b _ {2} \\ \vdots & \vdots & & \vdots & \vdots \\ a _ {m 1} & a _ {m 2} & \dots & a _ {m n} & b _ {m} \end{array} \right),
$$

其中 A 称为系数矩阵, x 称为未知数矩阵, b 称为常数项矩阵, B 称为增广矩阵.

矩阵的应用非常广泛,下面再举几例.

例 2 某工厂向三个商店(编号 1,2,3)发送四种产品(编号 I, II, III, IV)的数量可列成矩阵

$$
\begin{array}{c c c c c} \text {商店} & \text {产品} \\ & \mathrm{I} & \mathrm{II} & \mathrm{III} & \mathrm{IV} \\ 1 & \left( \begin{array}{l l l l} a _ {1 1} & a _ {1 2} & a _ {1 3} & a _ {1 4} \\ a _ {2 1} & a _ {2 2} & a _ {2 3} & a _ {2 4} \\ a _ {3 1} & a _ {3 2} & a _ {3 3} & a _ {3 4} \end{array} \right), \end{array}
$$

其中 $a_{ij}$ 为工厂向第 $i$ 家商店发送第 $j$ 种产品的数量.

这四种产品的单价及单件质量也可列成矩阵

$$
\boldsymbol {B} = \begin{array}{c c c} {\text {产品}} & {\text {单价}} & {\text {单件质量}} \\ {\mathrm{I}} & {\left( \begin{array}{c c} {b _ {1 1}} & {b _ {1 2}} \\ {b _ {2 1}} & {b _ {2 2}} \\ {b _ {3 1}} & {b _ {3 2}} \\ {b _ {4 1}} & {b _ {4 2}} \end{array} \right),} \\ {\mathrm{II}} & & \\ {\mathrm{III}} & & \\ {\mathrm{IV}} & & \end{array}
$$

其中 $b_{i1}$ 为第 $i$ 种产品的单价，$b_{i2}$ 为第 $i$ 种产品的单件质量.

例 3 四个城市间的单向航线如图 2.1 所示. 若令

$a_{ij} = \left\{ \begin{array}{l}1, \text{从 } i \text{ 市到 } j \text{ 市有 1 条单向航线,}\\ 0, \text{从 } i \text{ 市到 } j \text{ 市没有单向航线,} \end{array} \right.$

则图 2.1 可用矩阵表示为

$$
\boldsymbol {A} = (\boldsymbol {a} _ {i j}) = \left( \begin{array}{c c c c} 0 & 1 & 1 & 1 \\ 1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ 1 & 0 & 1 & 0 \end{array} \right).
$$

![](raw/pages_0001-0032/images/page_30_image_15.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph LR
  1["1"] --> 4["4"]
  2["2"] --> 3["3"]
  3["3"] --> 1["1"]
  1["1"] --> 2["2"]
  4["4"] --> 3["3"]
```
</details>

图2.1

一般地,若干个点之间的单向通道都可用这样的矩阵表示.

例 4 n 个变量  $x_{1}, x_{2}, \cdots, x_{n}$  与 m 个变量  $y_{1}, y_{2}, \cdots, y_{m}$  之间的关系式

![](raw/pages_0001-0032/images/page_30_image_19.jpg)

考研电子书网站:www.pdf2book.com

27

---

第2章 矩阵及其运算

$$
\left\{ \begin{array}{l} y _ {1} = a _ {1 1} x _ {1} + a _ {1 2} x _ {2} + \dots + a _ {1 n} x _ {n}, \\ y _ {2} = a _ {2 1} x _ {1} + a _ {2 2} x _ {2} + \dots + a _ {2 n} x _ {n}, \\ \dots \dots \\ y _ {m} = a _ {m 1} x _ {1} + a _ {m 2} x _ {2} + \dots + a _ {m n} x _ {n} \end{array} \right. \tag {3}
$$

表示一个从变量 $x_{1}, x_{2}, \cdots, x_{n}$ 到变量 $y_{1}, y_{2}, \cdots, y_{m}$ 的线性变换，其中 $a_{ij}$ 为常数。线性变换(3)的系数 $a_{ij}$ 构成矩阵 $\mathbf{A} = (a_{ij})_{m \times n}$。

给定了线性变换(3)，它的系数所构成的矩阵(称为系数矩阵)也就确定了.反之，如果给出一个矩阵作为线性变换的系数矩阵，则线性变换也就确定了.在这个意义上，线性变换和矩阵之间存在着一一对应的关系.

例如线性变换

$$
\left\{ \begin{array}{l} y _ {1} = \lambda_ {1} x _ {1}, \\ y _ {2} = \lambda_ {2} x _ {2}, \\ \dots \dots \\ y _ {n} = \lambda_ {n} x _ {n} \end{array} \right.
$$

对应 $n$ 阶方阵

$$
\boldsymbol {A} = \left( \begin{array}{c c c c} \lambda_ {1} & 0 & \dots & 0 \\ 0 & \lambda_ {2} & \dots & 0 \\ \vdots & \vdots & & \vdots \\ 0 & 0 & \dots & \lambda_ {n} \end{array} \right).
$$

这个方阵的特点是:从左上角到右下角的直线(叫做对角线)以外的元素都是0.这种方阵称为对角矩阵.对角矩阵也记作

$$
\Lambda = \mathrm{diag} (\lambda_ {1}, \lambda_ {2}, \dots , \lambda_ {n});
$$

当  $\lambda_{1}=\lambda_{2}=\cdots=\lambda_{n}=1$  时的线性变换叫做恒等变换，它对应的 n 阶方阵

$$
\boldsymbol {E} = \left( \begin{array}{c c c c} 1 & 0 & \dots & 0 \\ 0 & 1 & \dots & 0 \\ \vdots & \vdots & & \vdots \\ 0 & 0 & \dots & 1 \end{array} \right)
$$

叫做 $n$ 阶单位矩阵. 这个方阵的特点是: 对角线上的元素都是 1, 其他元素都是 0. 即单位矩阵 $\pmb{E}$ 的 $(i,j)$ 元 $\delta_{ij}$ 为

$$
\delta_ {i j} = \left\{ \begin{array}{l l} 1, \text {当} i = j, \\ 0, \text {当} i \neq j \end{array} \right. (i, j = 1, 2, \dots , n).
$$

由于矩阵和线性变换之间存在一一对应的关系,因此可以利用矩阵来研究线性变换,也可以利用线性变换来解释矩阵的含义.

28

---

§2 矩阵的运算

例如矩阵 $\begin{pmatrix}1&0\\0&0\end{pmatrix}$ 所对应的线性变换

$$
\left\{ \begin{array}{l} x _ {1} = x, \\ y _ {1} = 0 \end{array} \right.
$$

可看作是 $xOy$ 平面上把向量 $\overrightarrow{OP} = \begin{pmatrix} x \\ y \end{pmatrix}$ 变换为向量 $\overrightarrow{OP_1} = \begin{pmatrix} x_1 \\ y_1 \end{pmatrix} = \begin{pmatrix} x \\ 0 \end{pmatrix}$ 的变换（或看作把点 $P$ 变换为点 $P_1$ 的变换，参看图2.2），由于向量 $\overrightarrow{OP_1}$ 是向量 $\overrightarrow{OP}$ 在 $x$ 轴上的投影向量（即点 $P_1$ 是点 $P$ 在 $x$ 轴上的投影），因此这是一个投影变换。

![](raw/pages_0033-0064/images/page_32_image_4.jpg)

<details>
<summary>text_image</summary>

y
P
O
P₁ x
</details>

图2.2

又如矩阵 $\begin{pmatrix}\cos\varphi&-\sin\varphi\\ \sin\varphi&\cos\varphi\end{pmatrix}$ 对应的线性变换

$$
\left\{ \begin{array}{l} x _ {1} = x \cos \varphi - y \sin \varphi , \\ y _ {1} = x \sin \varphi + y \cos \varphi \end{array} \right.
$$

把 $xOy$ 平面上的向量 $\overrightarrow{OP} = \begin{pmatrix} x \\ y \end{pmatrix}$ 变换为向量 $\overrightarrow{OP_1} = \begin{pmatrix} x_1 \\ y_1 \end{pmatrix}$. 设 $\overrightarrow{OP}$ 的长度为 $r$, 辐角为 $\theta$, 即设 $x = r\cos \theta, y = r\sin \theta$, 那么

$$
x _ {1} = r (\cos \varphi \cos \theta - \sin \varphi \sin \theta) = r \cos (\theta + \varphi),
$$

$$
y _ {1} = r (\sin \varphi \cos \theta + \cos \varphi \sin \theta) = r \sin (\theta + \varphi),
$$

表明 $\overrightarrow{OP_{1}}$ 的长度为r而辐角为 $\theta+\varphi$ .因此,这是把向量 $\overrightarrow{OP}$ （依逆时针方向）旋转 $\varphi$ 角(即把点P以原点为中心逆时针旋转 $\varphi$ 角)的旋转变换(参看图2.3).

![](raw/pages_0033-0064/images/page_32_image_12.jpg)

<details>
<summary>text_image</summary>

y
P₁
φ
θ
O
x
P
</details>

图2.3

## § 2 矩阵的运算

## 一、矩阵的加法

定义 2 设有两个  $m \times n$  矩阵  $A = (a_{ij})$  和  $B = (b_{ij})$ ，那么矩阵 A 与 B 的和记作  $A + B$ ，规定为

29

---

第2章 矩阵及其运算

$$
\boldsymbol {A} + \boldsymbol {B} = \left( \begin{array}{c c c c} a _ {1 1} + b _ {1 1} & a _ {1 2} + b _ {1 2} & \dots & a _ {1 n} + b _ {1 n} \\ a _ {2 1} + b _ {2 1} & a _ {2 2} + b _ {2 2} & \dots & a _ {2 n} + b _ {2 n} \\ \vdots & \vdots & & \vdots \\ a _ {m 1} + b _ {m 1} & a _ {m 2} + b _ {m 2} & \dots & a _ {m n} + b _ {m n} \end{array} \right).
$$

应该注意, 只有当两个矩阵是同型矩阵时, 这两个矩阵才能进行加法运算.

矩阵加法满足下列运算规律(设 A, B, C 都是  $m \times n$  矩阵):

(i)  $A + B = B + A$ ;
(ii)  $(A+B)+C=A+(B+C)$ .

设矩阵 $A = (a_{ij})$ ，记

$$
- A = (- a _ {i j}),
$$

-A 称为矩阵 A 的负矩阵, 显然有

$$
A + (- A) = O,
$$

由此规定矩阵的减法为

$$
A - B = A + (- B).
$$

## 二、数与矩阵相乘

定义 3 数  $\lambda$  与矩阵 A 的乘积记作  $\lambda A$  或  $A\lambda$ ，规定为

$$
\lambda A = A \lambda = \left( \begin{array}{c c c c} \lambda a _ {1 1} & \lambda a _ {1 2} & \dots & \lambda a _ {1 n} \\ \lambda a _ {2 1} & \lambda a _ {2 2} & \dots & \lambda a _ {2 n} \\ \vdots & \vdots & & \vdots \\ \lambda a _ {m 1} & \lambda a _ {m 2} & \dots & \lambda a _ {m n} \end{array} \right).
$$

数乘矩阵满足下列运算规律(设 A, B 为  $m \times n$  矩阵,  $\lambda$ ,  $\mu$  为数):

(i)  $(\lambda\mu)A=\lambda(\mu A)$ ;

(ii)  $(\lambda + \mu)A = \lambda A + \mu A;$

(iii) $\lambda (\mathbf{A} + \mathbf{B}) = \lambda \mathbf{A} + \lambda \mathbf{B}$.

矩阵加法与数乘矩阵统称为矩阵的线性运算.

## 三、矩阵与矩阵相乘

设有两个线性变换

$$
\left\{ \begin{array}{l} y _ {1} = a _ {1 1} x _ {1} + a _ {1 2} x _ {2} + a _ {1 3} x _ {3}, \\ y _ {2} = a _ {2 1} x _ {1} + a _ {2 2} x _ {2} + a _ {2 3} x _ {3}, \end{array} \right. \tag {4}
$$

30

---

§2 矩阵的运算

$$
\left\{ \begin{array}{l} x _ {1} = b _ {1 1} t _ {1} + b _ {1 2} t _ {2}, \\ x _ {2} = b _ {2 1} t _ {1} + b _ {2 2} t _ {2}, \\ x _ {3} = b _ {3 1} t _ {1} + b _ {3 2} t _ {2}, \end{array} \right. \tag {5}
$$

若想求出从 $t_1, t_2$ 到 $y_1, y_2$ 的线性变换，可将(5)代入(4)，便得

$$
\left\{ \begin{array}{l} y _ {1} = (a _ {1 1} b _ {1 1} + a _ {1 2} b _ {2 1} + a _ {1 3} b _ {3 1}) t _ {1} + (a _ {1 1} b _ {1 2} + a _ {1 2} b _ {2 2} + a _ {1 3} b _ {3 2}) t _ {2}, \\ y _ {2} = (a _ {2 1} b _ {1 1} + a _ {2 2} b _ {2 1} + a _ {2 3} b _ {3 1}) t _ {1} + (a _ {2 1} b _ {1 2} + a _ {2 2} b _ {2 2} + a _ {2 3} b _ {3 2}) t _ {2}. \end{array} \right. \tag {6}
$$

线性变换(6)可看成是先作线性变换(5)再作线性变换(4)的结果.我们把线性变换(6)叫做线性变换(4)与(5)的乘积,相应地,把(6)所对应的矩阵定义为(4)与(5)所对应的矩阵的乘积,即

$$
\left( \begin{array}{l l l} a _ {1 1} & a _ {1 2} & a _ {1 3} \\ a _ {2 1} & a _ {2 2} & a _ {2 3} \end{array} \right) \left( \begin{array}{l l} b _ {1 1} & b _ {1 2} \\ b _ {2 1} & b _ {2 2} \\ b _ {3 1} & b _ {3 2} \end{array} \right) = \left( \begin{array}{l l} a _ {1 1} b _ {1 1} + a _ {1 2} b _ {2 1} + a _ {1 3} b _ {3 1} & a _ {1 1} b _ {1 2} + a _ {1 2} b _ {2 2} + a _ {1 3} b _ {3 2} \\ a _ {2 1} b _ {1 1} + a _ {2 2} b _ {2 1} + a _ {2 3} b _ {3 1} & a _ {2 1} b _ {1 2} + a _ {2 2} b _ {2 2} + a _ {2 3} b _ {3 2} \end{array} \right).
$$

一般地,我们有

定义 4 设  $\boldsymbol{A}=(a_{ij})$  是一个  $m \times s$  矩阵,  $\boldsymbol{B}=(b_{ij})$  是一个  $s \times n$  矩阵, 那么规定矩阵 A 与矩阵 B 的乘积是一个  $m \times n$  矩阵  $\boldsymbol{C}=(c_{ij})$ , 其中

$$
c _ {i j} = a _ {i 1} b _ {1 j} + a _ {i 2} b _ {2 j} + \dots + a _ {i s} b _ {s j} = \sum_ {k = 1} ^ {s} a _ {i k} b _ {k j} \quad (i = 1, 2, \dots , m; j = 1, 2, \dots , n), \tag {7}
$$

并把此乘积记作

$$
\boldsymbol {C} = \boldsymbol {A} \boldsymbol {B}.
$$

按此定义,一个  $1 \times s$  行矩阵与一个  $s \times 1$  列矩阵的乘积是一个 1 阶方阵,也就是一个数

$$
(a _ {i 1}, a _ {i 2}, \dots , a _ {i s}) \left( \begin{array}{c} b _ {1 j} \\ b _ {2 j} \\ \vdots \\ b _ {s j} \end{array} \right) = a _ {i 1} b _ {1 j} + a _ {i 2} b _ {2 j} + \dots + a _ {i s} b _ {s j} = \sum_ {k = 1} ^ {s} a _ {i k} b _ {k j} = c _ {i j},
$$

由此表明乘积矩阵 AB = C 的  $(i, j)$  元  $c_{ij}$  就是 A 的第 i 行与 B 的第 j 列的乘积.

必须注意: 只有当第一个矩阵(左矩阵)的列数等于第二个矩阵(右矩阵)的行数时, 两个矩阵才能相乘.

例5 求矩阵

$$
\boldsymbol {A} = \left( \begin{array}{c c c c} 4 & - 1 & 2 & 1 \\ 1 & 1 & 0 & 3 \\ 0 & 3 & 1 & 4 \end{array} \right) \quad \text {与} \quad \boldsymbol {B} = \left( \begin{array}{c c} 1 & 2 \\ 0 & 1 \\ 3 & 0 \\ - 1 & 2 \end{array} \right)
$$

考研电子书网站:www.pdf2book.com

31

---

第2章 矩阵及其运算

的乘积 ${AB}$ .

解 因为 A 是  $3 \times 4$  矩阵, B 是  $4 \times 2$  矩阵, A 的列数等于 B 的行数, 所以矩阵 A 与 B 可以相乘, 其乘积 AB = C 是一个  $3 \times 2$  矩阵. 按公式(7)有

$$
\begin{array}{l} \boldsymbol {C} = \boldsymbol {A} \boldsymbol {B} = \left( \begin{array}{c c c c} 4 & - 1 & 2 & 1 \\ 1 & 1 & 0 & 3 \\ 0 & 3 & 1 & 4 \end{array} \right) \left( \begin{array}{c c} 1 & 2 \\ 0 & 1 \\ 3 & 0 \\ - 1 & 2 \end{array} \right) \\ = \left( \begin{array}{c c} 4 \times 1 + (- 1) \times 0 + 2 \times 3 + 1 \times (- 1) & 4 \times 2 + (- 1) \times 1 + 2 \times 0 + 1 \times 2 \\ 1 \times 1 + 1 \times 0 + 0 \times 3 + 3 \times (- 1) & 1 \times 2 + 1 \times 1 + 0 \times 0 + 3 \times 2 \\ 0 \times 1 + 3 \times 0 + 1 \times 3 + 4 \times (- 1) & 0 \times 2 + 3 \times 1 + 1 \times 0 + 4 \times 2 \end{array} \right) \\ = \left( \begin{array}{c c} 9 & 9 \\ - 2 & 9 \\ - 1 & 1 1 \end{array} \right). \\ \end{array}
$$

例6 求矩阵

$$
\boldsymbol {A} = \left( \begin{array}{c c} {- 2} & {4} \\ {1} & {- 2} \end{array} \right) \quad \text {与} \quad \boldsymbol {B} = \left( \begin{array}{c c} {2} & {4} \\ {- 3} & {- 6} \end{array} \right)
$$

的乘积 $AB$ 及 $BA$.

解 按公式(7)，有

$$
\begin{array}{l} \boldsymbol {A} \boldsymbol {B} = \left( \begin{array}{c c} - 2 & 4 \\ 1 & - 2 \end{array} \right) \left( \begin{array}{c c} 2 & 4 \\ - 3 & - 6 \end{array} \right) = \left( \begin{array}{c c} - 1 6 & - 3 2 \\ 8 & 1 6 \end{array} \right), \\ \boldsymbol {B} \boldsymbol {A} = \left( \begin{array}{c c} 2 & 4 \\ - 3 & - 6 \end{array} \right) \left( \begin{array}{c c} - 2 & 4 \\ 1 & - 2 \end{array} \right) = \left( \begin{array}{c c} 0 & 0 \\ 0 & 0 \end{array} \right). \\ \end{array}
$$

在例5中，$\pmb{A}$ 是 $3 \times 4$ 矩阵，$\pmb{B}$ 是 $4 \times 2$ 矩阵，乘积 $\pmb{AB}$ 有意义而 $\pmb{BA}$ 却没有意义。由此可知，在矩阵的乘法中必须注意矩阵相乘的顺序。$\pmb{AB}$ 是 $\pmb{A}$ 左乘 $\pmb{B}$（$\pmb{B}$ 被 $\pmb{A}$ 左乘）的乘积，$\pmb{BA}$ 是 $\pmb{A}$ 右乘 $\pmb{B}$ 的乘积，$\pmb{AB}$ 有意义时，$\pmb{BA}$ 可能没有意义。又若 $\pmb{A}$ 是 $m \times n$ 矩阵，$\pmb{B}$ 是 $n \times m$ 矩阵，则 $\pmb{AB}$ 与 $\pmb{BA}$ 都有意义，但 $\pmb{AB}$ 是 $m$ 阶方阵，$\pmb{BA}$ 是 $n$ 阶方阵，当 $m \neq n$ 时 $\pmb{AB} \neq \pmb{BA}$。即使 $m = n$，即 $\pmb{A}, \pmb{B}$ 是同阶方阵，如例6，$\pmb{A}$ 与 $\pmb{B}$ 都是2阶方阵，从而 $\pmb{AB}$ 与 $\pmb{BA}$ 也都是2阶方阵，但 $\pmb{AB}$ 与 $\pmb{BA}$ 仍然可以不相等。总之，矩阵的乘法不满足交换律，即在一般情形下，$\pmb{AB} \neq \pmb{BA}$。

对于两个 n 阶方阵 A, B, 若 AB = BA, 则称方阵 A 与 B 是可交换的.

例6还表明,矩阵 $A\neq O,B\neq O$ ,但却有BA=O.这就提醒读者要特别注意:若有两个矩阵A,B满足AB=O,不能得出A=O或B=O的结论;若 $A\neq O$ 而 $A(X-Y)=O$ ,也不能得出X=Y的结论.

矩阵的乘法虽不满足交换律,但仍满足下列结合律和分配律(假设运算都是可

32

---

§2 矩阵的运算

行的):

(i)  $(AB)C=A(BC)$ ;
(ii)  $\lambda(\boldsymbol{A}\boldsymbol{B})=(\lambda\boldsymbol{A})\boldsymbol{B}=\boldsymbol{A}(\lambda\boldsymbol{B})$  (其中  $\lambda$  为数);
(iii)  $A(B+C)=AB+AC,(B+C)A=BA+CA.$

对于单位矩阵 E, 容易验证

$$
E _ {m} A _ {m \times n} = A _ {m \times n}, \quad A _ {m \times n} E _ {n} = A _ {m \times n},
$$

或简写成

$$
E A = A E = A.
$$

可见单位矩阵 E 在矩阵乘法中的作用类似于数 1 在数的乘法中的作用.

矩阵

$$
\lambda E = \left( \begin{array}{c c c c} \lambda & & & \\ & \lambda & & \\ & & \ddots & \\ & & & \lambda \end{array} \right)
$$

称为纯量矩阵.由 $(\lambda E)A=\lambda A,A(\lambda E)=\lambda A$ ，可知纯量矩阵 $\lambda E$ 与矩阵A的乘积等于数 $\lambda$ 与A的乘积.当A为n阶方阵时，有

$$
(\lambda E _ {n}) A _ {n} = \lambda A _ {n} = A _ {n} (\lambda E _ {n}),
$$

表明纯量矩阵  $\lambda E$  与任何同阶方阵都是可交换的.

有了矩阵的乘法,就可以定义方阵的幂.设 A 是 n 阶方阵,定义

$$
A ^ {1} = A, \quad A ^ {2} = A ^ {1} A ^ {1}, \quad \dots , \quad A ^ {k + 1} = A ^ {k} A ^ {1},
$$

其中 $k$ 为正整数, 这就是说, $\pmb{A}^{k}$ 就是 $k$ 个 $\pmb{A}$ 连乘 (约定 $\pmb{A}^{0} = \pmb{E}$).

由于矩阵乘法适合结合律,所以方阵的幂满足以下运算规律:

$$
\boldsymbol {A} ^ {k} \boldsymbol {A} ^ {l} = \boldsymbol {A} ^ {k + l}, \quad (\boldsymbol {A} ^ {k}) ^ {l} = \boldsymbol {A} ^ {k l},
$$

其中 $k, l$ 为非负整数. 又因矩阵乘法一般不满足交换律, 所以对于两个 $n$ 阶矩阵 $\pmb{A}$ 与 $\pmb{B}$, 一般说来 $(\pmb{AB})^k \neq \pmb{A}^k \pmb{B}^k (k \geqslant 2)$, 但当 $\pmb{A}$ 与 $\pmb{B}$ 可交换时, 有 $(\pmb{AB})^k = \pmb{A}^k \pmb{B}^k$. 类似可知, 当 $\pmb{A}, \pmb{B}$ 可交换时, $(\pmb{A} + \pmb{B})^2 = \pmb{A}^2 + 2\pmb{A}\pmb{B} + \pmb{B}^2, (\pmb{A} - \pmb{B})(\pmb{A} + \pmb{B}) = \pmb{A}^2 - \pmb{B}^2$ 等公式成立.

矩阵的乘法有着多方面的应用,下面举两个例子:

例 2(续) 前已得到两个矩阵:

$$
A = \begin{array}{l} \text {商店} \\ 1 \\ 2 \\ 3 \end{array} \left( \begin{array}{c c c c} a _ {1 1} & a _ {1 2} & a _ {1 3} & a _ {1 4} \\ a _ {2 1} & a _ {2 2} & a _ {2 3} & a _ {2 4} \\ a _ {3 1} & a _ {3 2} & a _ {3 3} & a _ {3 4} \end{array} \right) \quad \text {和} \quad B = \begin{array}{l} \text {产品 单价 单件质量} \\ I \\ I I \\ I I I \\ I V \end{array} \left( \begin{array}{c c} b _ {1 1} & b _ {1 2} \\ b _ {2 1} & b _ {2 2} \\ b _ {3 1} & b _ {3 2} \\ b _ {4 1} & b _ {4 2} \end{array} \right).
$$

考研电子书网站:www.pdf2book.com

33

---

第2章 矩阵及其运算

记 C=AB, 那么

$$
c _ {i 1} = a _ {i 1} b _ {1 1} + a _ {i 2} b _ {2 1} + a _ {i 3} b _ {3 1} + a _ {i 4} b _ {4 1}
$$

是该工厂向第 $i$ 家商店所发产品的总价 $(i = 1,2,3)$

$$
c _ {i 2} = a _ {i 1} b _ {1 2} + a _ {i 2} b _ {2 2} + a _ {i 3} b _ {3 2} + a _ {i 4} b _ {4 2}
$$

是该工厂向第 $i$ 家商店所发产品的总质量 $(i = 1,2,3)$，因此可形象地写为

$$
C = A B = 2 \left( \begin{array}{c c c c} a _ {1 1} & a _ {1 2} & a _ {1 3} & a _ {1 4} \\ a _ {2 1} & a _ {2 2} & a _ {2 3} & a _ {2 4} \\ a _ {3 1} & a _ {3 2} & a _ {3 3} & a _ {3 4} \end{array} \right) _ {3 \times 4} \quad \begin{array}{l l l} \text {单价} & \text {单件质量} \\ \mathrm{I} & b _ {1 1} & b _ {1 2} \\ \mathrm{II} & b _ {2 1} & b _ {2 2} \\ \mathrm{III} & b _ {3 1} & b _ {3 2} \\ \mathrm{IV} & b _ {4 1} & b _ {4 2} \end{array} _ {4 \times 2}
$$

总价 · 总质量

$$
= 2 \left( \begin{array}{c c c} c _ {1 1} & & c _ {1 2} \\ c _ {2 1} & & c _ {2 2} \\ c _ {3 1} & & c _ {3 2} \end{array} \right) _ {3 \times 2}.
$$

进一步,如果  $D=\begin{pmatrix}1&1&1\\0&-1&1\end{pmatrix}$ ,且

$$
\boldsymbol {H} = \boldsymbol {D} (\boldsymbol {A B}) = \boldsymbol {D C} = \left( \begin{array}{c c c} 1 & 1 & 1 \\ 0 & - 1 & 1 \end{array} \right) \left( \begin{array}{c c} c _ {1 1} & c _ {1 2} \\ c _ {2 1} & c _ {2 2} \\ c _ {3 1} & c _ {3 2} \end{array} \right) = \left( \begin{array}{c c} h _ {1 1} & h _ {1 2} \\ h _ {2 1} & h _ {2 2} \end{array} \right),
$$

那么  $h_{11}$  和  $h_{12}$  分别是该厂向三个商店发出产品的总价和总质量,  $h_{21}$  和  $h_{22}$  分别是第 3 家商店超出第 2 家商店的价款和质量.

例7 上节例1中 $n$ 元线性方程组

$$
\left\{ \begin{array}{l} a _ {1 1} x _ {1} + a _ {1 2} x _ {2} + \dots + a _ {1 n} x _ {n} = b _ {1}, \\ a _ {2 1} x _ {1} + a _ {2 2} x _ {2} + \dots + a _ {2 n} x _ {n} = b _ {2}, \\ \dots \dots \\ a _ {m 1} x _ {1} + a _ {m 2} x _ {2} + \dots + a _ {m n} x _ {n} = b _ {m}, \end{array} \right. \tag {1}
$$

利用矩阵乘法可写成矩阵形式

$$
A _ {m \times n} x _ {n \times 1} = b _ {m \times 1}, \tag {$1^{\prime$}}
$$

其中  $\boldsymbol{A}=(a_{ij})$  为系数矩阵,  $x=\begin{pmatrix}x_{1}\\x_{2}\\\vdots\\x_{n}\end{pmatrix}$  为未知数矩阵,  $b=\begin{pmatrix}b_{1}\\b_{2}\\\vdots\\b_{m}\end{pmatrix}$  为常数项矩阵. 特别地, 当

34

---

§2 矩阵的运算

$b = 0$ 时得到 $m$ 个方程的 $n$ 元齐次线性方程组的矩阵形式

$$
A _ {m \times n} x _ {n \times 1} = 0 _ {m \times 1}.
$$

又,上节例4中的线性变换

$$
\left\{ \begin{array}{l} y _ {1} = a _ {1 1} x _ {1} + a _ {1 2} x _ {2} + \dots + a _ {1 n} x _ {n}, \\ y _ {2} = a _ {2 1} x _ {1} + a _ {2 2} x _ {2} + \dots + a _ {2 n} x _ {n}, \\ \dots \dots \\ y _ {m} = a _ {m 1} x _ {1} + a _ {m 2} x _ {2} + \dots + a _ {m n} x _ {n}, \end{array} \right. \tag {3}
$$

利用矩阵的乘法,可记作

$$
y = A x, \tag {$3^{\prime$}}
$$

其中

$$
\boldsymbol {A} = (a _ {i j}), \quad \boldsymbol {x} = \left( \begin{array}{c} x _ {1} \\ x _ {2} \\ \vdots \\ x _ {n} \end{array} \right), \quad \boldsymbol {y} = \left( \begin{array}{c} y _ {1} \\ y _ {2} \\ \vdots \\ y _ {m} \end{array} \right).
$$

这里,列向量(列矩阵)x 表示 n 个变量  $x_{1}, x_{2}, \cdots, x_{n}$ , 列向量 y 表示 m 个变量  $y_{1}, y_{2}, \cdots, y_{m}$ . 线性变换  $(3')$  把 x 变成 y, 相当于用矩阵 A 左乘 x 得到 y.

例如,由第2章§1可知,用矩阵 $A=\begin{pmatrix}\cos\varphi&-\sin\varphi\\\sin\varphi&\cos\varphi\end{pmatrix}$ 左乘向量 $\overrightarrow{OP}=\begin{pmatrix}x\\y\end{pmatrix}$ ,相当于把向量 $\overrightarrow{OP}$ 按逆时针方向旋转 $\varphi$ 角(参看图2.3).进一步还可推知,用 $A^{n}=\begin{pmatrix}\cos\varphi&-\sin\varphi\\\sin\varphi&\cos\varphi\end{pmatrix}^{n}$ 左乘向量 $\overrightarrow{OP}$ ,相当于把向量 $\overrightarrow{OP}$ 按逆时针方向旋转n个 $\varphi$ 角,即旋转 $n\varphi$ 角,而旋转 $n\varphi$ 角的变换所对应的矩阵为 $\begin{pmatrix}\cos n\varphi&-\sin n\varphi\\\sin n\varphi&\cos n\varphi\end{pmatrix}$ ,亦即成立

$$
\left( \begin{array}{c c} \cos \varphi & - \sin \varphi \\ \sin \varphi & \cos \varphi \end{array} \right) ^ {n} = \left( \begin{array}{c c} \cos n \varphi & - \sin n \varphi \\ \sin n \varphi & \cos n \varphi \end{array} \right).
$$

上式也可以按矩阵幂的定义来证明.

## 四、矩阵的转置

定义 5 把矩阵 A 的行换成同序数的列得到一个新矩阵, 叫做 A 的转置矩阵, 记作  $A^{T}$ .

例如矩阵

$$
A = \left( \begin{array}{c c c} 1 & 2 & 0 \\ 3 & - 1 & 1 \end{array} \right)
$$

考研电子书网站:www.pdf2book.com

35

---

第2章 矩阵及其运算

的转置矩阵为

$$
\boldsymbol {A} ^ {\mathrm{T}} = \left( \begin{array}{c c} 1 & 3 \\ 2 & - 1 \\ 0 & 1 \end{array} \right).
$$

矩阵的转置也是一种运算,满足下述运算规律(假设运算都是可行的):

(i)  $(\boldsymbol{A}^{\mathrm{T}})^{\mathrm{T}}=\boldsymbol{A};$
(ii)  $(\boldsymbol{A}+\boldsymbol{B})^{\mathrm{T}}=\boldsymbol{A}^{\mathrm{T}}+\boldsymbol{B}^{\mathrm{T}};$
(iii)  $(\lambda A)^{\mathrm{T}}=\lambda A^{\mathrm{T}};$
(iv) $(\mathbf{AB})^{\mathrm{T}} = \mathbf{B}^{\mathrm{T}}\mathbf{A}^{\mathrm{T}}.$

这里仅证明（iv). 设 $A = (a_{ij})_{m \times s}, B = (b_{ij})_{s \times n}$, 记 $AB = C = (c_{ij})_{m \times n}, B^{\mathrm{T}} A^{\mathrm{T}} = D = (d_{ij})_{n \times m}$. 于是按公式(7)，有

$$
c _ {j i} = \sum_ {k = 1} ^ {s} a _ {j k} b _ {k i},
$$

而  $B^{T}$  的第 i 行为  $(b_{1i}, b_{2i}, \cdots, b_{si})$ ,  $A^{T}$  的第 j 列为  $(a_{j1}, a_{j2}, \cdots, a_{js})^{T}$ , 因此

$$
d _ {i j} = \sum_ {k = 1} ^ {s} b _ {k i} a _ {j k} = \sum_ {k = 1} ^ {s} a _ {j k} b _ {k i},
$$

所以

$$
d _ {i j} = c _ {j i} \quad (i = 1, 2, \dots , n; j = 1, 2, \dots , m),
$$

即  $D=C^{T}$ ，亦即

$$
\boldsymbol {B} ^ {\mathrm{T}} \boldsymbol {A} ^ {\mathrm{T}} = (\boldsymbol {A B}) ^ {\mathrm{T}}.
$$

证毕

例8 已知

$$
\boldsymbol {A} = \left( \begin{array}{c c c} 2 & 0 & - 1 \\ 1 & 3 & 2 \end{array} \right), \quad \boldsymbol {B} = \left( \begin{array}{c c c} 1 & 7 & - 1 \\ 4 & 2 & 3 \\ 2 & 0 & 1 \end{array} \right),
$$

求 $(\boldsymbol{AB})^{\mathrm{T}}$ .

解法1 因为

$$
\boldsymbol {A} \boldsymbol {B} = \left( \begin{array}{c c c} 2 & 0 & - 1 \\ 1 & 3 & 2 \end{array} \right) \left( \begin{array}{c c c} 1 & 7 & - 1 \\ 4 & 2 & 3 \\ 2 & 0 & 1 \end{array} \right) = \left( \begin{array}{c c c} 0 & 1 4 & - 3 \\ 1 7 & 1 3 & 1 0 \end{array} \right),
$$

所以

$$
(\boldsymbol {A} \boldsymbol {B}) ^ {\mathrm{T}} = \left( \begin{array}{c c} 0 & 1 7 \\ 1 4 & 1 3 \\ - 3 & 1 0 \end{array} \right).
$$

36

---

§2 矩阵的运算

解法 2  $(\boldsymbol{A}\boldsymbol{B})^{\mathrm{T}}=\boldsymbol{B}^{\mathrm{T}}\boldsymbol{A}^{\mathrm{T}}=\begin{pmatrix}1&4&2\\7&2&0\\-1&3&1\end{pmatrix}\begin{pmatrix}2&1\\0&3\\-1&2\end{pmatrix}=\begin{pmatrix}0&17\\14&13\\-3&10\end{pmatrix}.$

设 $\mathbf{A}$ 为 $n$ 阶方阵, 如果满足 $\mathbf{A}^{\mathrm{T}} = \mathbf{A}$, 即

$$
a _ {i j} = a _ {j i} \quad (i, j = 1, 2, \dots , n),
$$

那么 A 称为对称矩阵. 对称矩阵的特点是: 它的元素以对角线为对称轴对应相等.

例 9 设列矩阵  $\boldsymbol{X}=(x_{1},x_{2},\cdots,x_{n})^{\mathrm{T}}$  满足  $X^{T}X=1,E$  为 n 阶单位矩阵, H=E-2XX $^{T}$ , 证明 H 是对称矩阵, 且  $HH^{T}=E$ .

证明前先提醒读者注意: $X^{T}X=x_{1}^{2}+x_{2}^{2}+\cdots+x_{n}^{2}$ 是1阶方阵,也就是一个数,而 $XX^{T}$ 是n阶方阵.

证 因为

$$
\boldsymbol {H} ^ {\mathrm{T}} = \left(\boldsymbol {E} - 2 \boldsymbol {X} \boldsymbol {X} ^ {\mathrm{T}}\right) ^ {\mathrm{T}} = \boldsymbol {E} ^ {\mathrm{T}} - 2 \left(\boldsymbol {X} \boldsymbol {X} ^ {\mathrm{T}}\right) ^ {\mathrm{T}} = \boldsymbol {E} - 2 \boldsymbol {X} \boldsymbol {X} ^ {\mathrm{T}} = \boldsymbol {H},
$$

所以 H 是对称矩阵.

$$
\begin{array}{l} \boldsymbol {H} \boldsymbol {H} ^ {\mathrm{T}} = \boldsymbol {H} ^ {2} = (\boldsymbol {E} - 2 \boldsymbol {X} \boldsymbol {X} ^ {\mathrm{T}}) ^ {2} = \boldsymbol {E} - 4 \boldsymbol {X} \boldsymbol {X} ^ {\mathrm{T}} + 4 (\boldsymbol {X} \boldsymbol {X} ^ {\mathrm{T}}) (\boldsymbol {X} \boldsymbol {X} ^ {\mathrm{T}}) \\ = E - 4 X X ^ {\mathrm{T}} + 4 X (X ^ {\mathrm{T}} X) X ^ {\mathrm{T}} = E - 4 X X ^ {\mathrm{T}} + 4 X X ^ {\mathrm{T}} = E. \\ \end{array}
$$

## 五、方阵的行列式

定义 6 由 n 阶方阵 A 的元素所构成的行列式(各元素的位置不变), 称为方阵 A 的行列式, 记作  $\det A$  或  $|A|$ .

应该注意,方阵与行列式是两个不同的概念,n阶方阵是 $n^{2}$ 个数按一定方式排成的数表,而n阶行列式则是这些数(也就是数表A)按一定的运算法则所确定的一个数.

由 A 确定  $\left|A\right|$  的这个运算满足下述运算规律(设 A, B 为 n 阶方阵,  $\lambda$  为数):

(i)  $\left|A^{T}\right|=\left|A\right|$  (行列式性质1),
(ii)  $\left|\lambda A\right|=\lambda^{n}\left|A\right|$ ,
(iii)  $\left|AB\right|=\left|A\right|\left|B\right|$ .

我们仅证明(iii)，且仅就 $n = 2$ 的情形写出证明，$n \geqslant 3$ 的情形类似可证. 设 $A = (a_{ij}), B = (b_{ij})$. 记四阶行列式

$$
D = \left| \begin{array}{c c c c} a _ {1 1} & a _ {1 2} & 0 & 0 \\ a _ {2 1} & a _ {2 2} & 0 & 0 \\ - 1 & 0 & b _ {1 1} & b _ {1 2} \\ 0 & - 1 & b _ {2 1} & b _ {2 2} \end{array} \right| = \left| \begin{array}{c c} A & O \\ - E & B \end{array} \right|,
$$

由第1章例10可知 $D = |\mathbf{A}||\mathbf{B}|$. 今在 $D$ 中以 $b_{11}$ 乘第1列, $b_{21}$ 乘第2列都加到第3列上; 再以 $b_{12}$ 乘第1列, $b_{22}$ 乘第2列都加到第4列上, 即

考研电子书网站:www.pdf2book.com

37

---

第2章 矩阵及其运算

$$
\begin{array}{l} D \xlongequal {c _ {3} + b _ {1 1} c _ {1} + b _ {2 1} c _ {2}} \left| \begin{array}{c c c c} a _ {1 1} & a _ {1 2} & a _ {1 1} b _ {1 1} + a _ {1 2} b _ {2 1} & 0 \\ a _ {2 1} & a _ {2 2} & a _ {2 1} b _ {1 1} + a _ {2 2} b _ {2 1} & 0 \\ - 1 & 0 & . & 0 \\ 0 & - 1 & & 0 \end{array} \right| b _ {1 2} \\ \frac {c _ {4} + b _ {1 2} c _ {1} + b _ {2 2} c _ {2}}{\text {一}} \left| \begin{array}{c c c c} a _ {1 1} & a _ {1 2} & a _ {1 1} b _ {1 1} + a _ {1 2} b _ {2 1} & a _ {1 1} b _ {1 2} + a _ {1 2} b _ {2 2} \\ a _ {2 1} & a _ {2 2} & a _ {2 1} b _ {1 1} + a _ {2 2} b _ {2 1} & a _ {2 1} b _ {1 2} + a _ {2 2} b _ {2 2} \\ - 1 & 0 & 0 & 0 \\ 0 & - 1 & 0 & 0 \end{array} \right| = \left| \begin{array}{c c} A & X \\ - E & O \end{array} \right|, \\ \end{array}
$$

其中2阶矩阵 $X = (x_{ij})$ ，因 $x_{ij} = a_{i1}b_{1j} + a_{i2}b_{2j}$ ，由公式(7)知 $X = AB.$ 再对上式最后一个行列式作两次行对换: $r_1\leftrightarrow r_3,r_2\leftrightarrow r_4$ ，得

$$
D = (- 1) ^ {2} \left| \begin{array}{c c} - E & O \\ A & X \end{array} \right| = (- 1) ^ {2} | - E | | X | = (- 1) ^ {2} (- 1) ^ {2} | X | = | X | = | A B |.
$$

于是

$$
\left| \boldsymbol {A} \boldsymbol {B} \right| = \left| \boldsymbol {A} \right| \left| \boldsymbol {B} \right|.
$$

证毕

由(iii)可知,对于 n 阶矩阵 A,B,一般来说  $AB \neq BA$ ,但总有

$$
\left| \boldsymbol {A} \boldsymbol {B} \right| = \left| \boldsymbol {B} \boldsymbol {A} \right|.
$$

例10 行列式 $|\mathbf{A}|$ 的各个元素的代数余子式 $A_{ij}$ 所构成的矩阵

$$
\boldsymbol {A} ^ {*} = \left( \begin{array}{c c c c} A _ {1 1} & A _ {2 1} & \dots & A _ {n 1} \\ A _ {1 2} & A _ {2 2} & \dots & A _ {n 2} \\ \vdots & \vdots & & \vdots \\ A _ {1 n} & A _ {2 n} & \dots & A _ {n n} \end{array} \right),
$$

称为矩阵 A 的伴随矩阵. 试证

$$
A A ^ {*} = A ^ {*} A = | A | E.
$$

证 设 $A = (a_{ij})$ ，记 $AA^{*} = (b_{ij})$ ，则

$$
b _ {i j} = a _ {i 1} A _ {j 1} + a _ {i 2} A _ {j 2} + \dots + a _ {i n} A _ {j n} = \left\{ \begin{array}{c l} {| A |,} & {\text {当} i = j,} \\ {0,} & {\text {当} i \neq j,} \end{array} \right.
$$

故

$$
\boldsymbol {A} \boldsymbol {A} ^ {*} = \left( \begin{array}{c c c c} | \boldsymbol {A} | & & & \\ & | \boldsymbol {A} | & & \\ & & \ddots & \\ & & & | \boldsymbol {A} | \end{array} \right) = | \boldsymbol {A} | \boldsymbol {E}.
$$

类似地,有

$$
A ^ {*} A = | A | E.
$$

38

---

§3 逆矩阵

## § 3 逆 矩 阵

## 一、逆矩阵的定义、性质和求法

在数的乘法中,对不等于零的数 a 总存在惟一的数 b,使 ab=ba=1,此数 b 即是 a 的倒数,即  $b=\frac{1}{a}=a^{-1}$ . 利用倒数,数的除法可转化为乘积的形式:  $x\div a=x\cdot\frac{1}{a}=x\cdot a^{-1}$ , 这里  $a\neq0$ . 把这一思想应用到矩阵的运算中我们引入逆矩阵的定义.

定义7 对于 $n$ 阶矩阵 $\mathbf{A}$, 如果有一个 $n$ 阶矩阵 $\mathbf{B}$, 使

$$
\boldsymbol {A} \boldsymbol {B} = \boldsymbol {B} \boldsymbol {A} = \boldsymbol {E},
$$

则称矩阵 A 是可逆的, 并把矩阵 B 称为 A 的逆矩阵.

如果矩阵 A 是可逆的,那么 A 的逆矩阵是惟一的.这是因为:若 B,C 都是 A 的逆矩阵,则有

$$
\boldsymbol {B} = \boldsymbol {B} \boldsymbol {E} = \boldsymbol {B} (\boldsymbol {A C}) = (\boldsymbol {B A}) \boldsymbol {C} = \boldsymbol {E C} = \boldsymbol {C},
$$

所以 $\pmb{A}$ 的逆矩阵是惟一的.

$\pmb{A}$ 的逆矩阵记作 $A^{-1}$. 即若 $AB = BA = E$, 则 $B = A^{-1}$.

定理1 若矩阵 $A$ 可逆, 则 $|A| \neq 0$.

证 $A$ 可逆, 即有 $A^{-1}$, 使 $AA^{-1} = E$. 故 $|A| \cdot |A^{-1}| = |E| = 1$, 所以 $|A| \neq 0$. 证毕定理2 若 $|A| \neq 0$, 则矩阵 $A$ 可逆, 且

$$
\boldsymbol {A} ^ {- 1} = \frac {1}{| \boldsymbol {A} |} \boldsymbol {A} ^ {*}, \tag {8}
$$

其中 $A^{*}$ 为矩阵 $\pmb{A}$ 的伴随矩阵.

证 由例10知

$$
A A ^ {*} = A ^ {*} A = | A | E,
$$

因 $|A| \neq 0$ ，故有

$$
A \frac {1}{| A |} A ^ {*} = \frac {1}{| A |} A ^ {*} A = E,
$$

所以,按逆矩阵的定义,即知 A 可逆,且有

$$
A ^ {- 1} = \frac {1}{| A |} A ^ {*}.
$$

证毕

当 $|A| = 0$ 时, $A$ 称为奇异矩阵, 否则称非奇异矩阵. 由上面两定理可知: $A$ 是可逆矩阵的充分必要条件是 $|A| \neq 0$, 即可逆矩阵就是非奇异矩阵.

考研电子书网站:www.pdf2book.com

39

---

第2章 矩阵及其运算

由定理 2, 可得下述推论.

推论 设 A, B 为 n 阶矩阵, 若 AB = E (或 BA = E), 则 A 可逆且  $B = A^{-1}$ .

证 $|A||B| = |E| = 1$ ，故 $|A|\neq 0$ ，因而 $A^{-1}$ 存在，于是

$$
\boldsymbol {B} = \boldsymbol {E} \boldsymbol {B} = (\boldsymbol {A} ^ {- 1} \boldsymbol {A}) \dot {\boldsymbol {B}} = \boldsymbol {A} ^ {- 1} (\boldsymbol {A B}) = \boldsymbol {A} ^ {- 1} \boldsymbol {E} = \boldsymbol {A} ^ {- 1}.
$$

证毕

逆矩阵满足下述运算规律:

(i) 若 A 可逆, 则  $A^{-1}$  亦可逆, 且  $(A^{-1})^{-1}=A$ ;
(ii) 若 A 可逆, 数  $\lambda \neq 0$ , 则  $\lambda A$  可逆, 且  $(\lambda A)^{-1} = \frac{1}{\lambda} A^{-1}$ ;
（iii）若 A, B 为同阶矩阵且均可逆，则 AB 亦可逆，且

$$
(A B) ^ {- 1} = B ^ {- 1} A ^ {- 1}.
$$

证 $(\mathbf{AB})(\mathbf{B}^{-1}\mathbf{A}^{-1}) = \mathbf{A}(\mathbf{BB}^{-1})\mathbf{A}^{-1} = \mathbf{A}\mathbf{E}\mathbf{A}^{-1} = \mathbf{A}\mathbf{A}^{-1} = \mathbf{E}$, 由推论, 即有 $\mathbf{AB}$ 可逆且 $(\mathbf{AB})^{-1} = \mathbf{B}^{-1}\mathbf{A}^{-1}$. 证毕

(iv) 若 A 可逆, 则  $A^{T}$  亦可逆, 且  $(\boldsymbol{A}^{\mathrm{T}})^{-1} = (\boldsymbol{A}^{-1})^{\mathrm{T}}$ .

证 $A^{\mathrm{T}}(A^{-1})^{\mathrm{T}} = (A^{-1}A)^{\mathrm{T}} = E^{\mathrm{T}} = E,$

所以

$$
(A ^ {T}) ^ {- 1} = (A ^ {- 1}) ^ {T}.
$$

证毕

当 A 可逆时, 还可定义

$$
\boldsymbol {A} ^ {- k} = \left(\boldsymbol {A} ^ {- 1}\right) ^ {k},
$$

其中 $k$ 为正整数. 这样, 当 $\pmb{A}$ 可逆, $\lambda, \mu$ 为整数时, 有

$$
A ^ {\lambda} A ^ {\mu} = A ^ {\lambda + \mu}, \quad (A ^ {\lambda}) ^ {\mu} = A ^ {\lambda \mu}.
$$

例 11 求 2 阶可逆矩阵  $A=\begin{pmatrix}a&b\\c&d\end{pmatrix}$  的逆矩阵.

解 $|A| = ad - bc, A^* = \begin{pmatrix} d & -b \\ -c & a \end{pmatrix},$

利用逆矩阵公式(8)，有

$$
A ^ {- 1} = \frac {1}{| A |} A ^ {*} = \frac {1}{a d - b c} \left( \begin{array}{c c} d & - b \\ - c & a \end{array} \right).
$$

例 12 求方阵  $A=\begin{pmatrix}1&2&3\\ 2&2&1\\ 3&4&3\end{pmatrix}$  的逆矩阵.

解 求得 $|A| = 2 \neq 0$，知 $A^{-1}$ 存在。再计算 $|A|$ 的余子式

$$
\begin{array}{l} M _ {1 1} ^ {\prime} = 2, \quad M _ {1 2} = 3, \quad M _ {1 3} = 2, \\ M _ {2 1} = - 6, \quad M _ {2 2} = - 6, \quad M _ {2 3} = - 2, \\ M _ {3 1} = - 4, \quad M _ {3 2} = - 5, \quad M _ {3 3} = - 2, \\ \end{array}
$$

40

---

§3 逆矩阵

得

$$
\boldsymbol {A} ^ {*} = \left( \begin{array}{c c c} M _ {1 1} & - M _ {2 1} & M _ {3 1} \\ - M _ {1 2} & M _ {2 2} & - M _ {3 2} \\ M _ {1 3} & - M _ {2 3} & M _ {3 3} \end{array} \right) = \left( \begin{array}{c c c} 2 & 6 & - 4 \\ - 3 & - 6 & 5 \\ 2 & 2 & - 2 \end{array} \right),
$$

所以

$$
A ^ {- 1} = \frac {1}{| A |} A ^ {*} = \left( \begin{array}{c c c} 1 & 3 & - 2 \\ - \frac {3}{2} & - 3 & \frac {5}{2} \\ 1 & 1 & - 1 \end{array} \right).
$$

## 二、逆矩阵的初步应用

可逆矩阵在线性代数中占有重要地位,它的应用是多方面的,下面举几个例子.

例13 设

$$
\boldsymbol {A} = \left( \begin{array}{c c c} 1 & 2 & 3 \\ 2 & 2 & 1 \\ 3 & 4 & 3 \end{array} \right), \quad \boldsymbol {B} = \left( \begin{array}{c c} 2 & 1 \\ 5 & 3 \end{array} \right), \quad \boldsymbol {C} = \left( \begin{array}{c c} 1 & 3 \\ 2 & 0 \\ 3 & 1 \end{array} \right),
$$

求矩阵 $X$ 使其满足

$$
A X B = C.
$$

解 若 $A^{-1}, B^{-1}$ 存在, 则用 $A^{-1}$ 左乘上式, $B^{-1}$ 右乘上式, 有

$$
A ^ {- 1} A X B B ^ {- 1} = A ^ {- 1} C B ^ {- 1},
$$

即

$$
X = A ^ {- 1} C B ^ {- 1}.
$$

由例12知 $|A| \neq 0$，而 $|B| = 1$，故知 $A, B$ 都可逆，且

$$
\boldsymbol {A} ^ {- 1} = \left( \begin{array}{c c c} 1 & 3 & - 2 \\ - \frac {3}{2} & - 3 & \frac {5}{2} \\ 1 & 1 & - 1 \end{array} \right), \quad \boldsymbol {B} ^ {- 1} = \left( \begin{array}{c c} 3 & - 1 \\ - 5 & 2 \end{array} \right),
$$

于是

$$
\begin{array}{l} \boldsymbol {X} = \boldsymbol {A} ^ {- 1} \boldsymbol {C} \boldsymbol {B} ^ {- 1} = \left( \begin{array}{c c c} 1 & 3 & - 2 \\ - \frac {3}{2} & - 3 & \frac {5}{2} \\ 1 & 1 & - 1 \end{array} \right) \left( \begin{array}{c c} 1 & 3 \\ 2 & 0 \\ 3 & 1 \end{array} \right) \left( \begin{array}{c c} 3 & - 1 \\ - 5 & 2 \end{array} \right) \\ = \left( \begin{array}{c c} 1 & 1 \\ 0 & - 2 \\ 0 & 2 \end{array} \right) \left( \begin{array}{c c} 3 & - 1 \\ - 5 & 2 \end{array} \right) = \left( \begin{array}{c c} - 2 & 1 \\ 1 0 & - 4 \\ - 1 0 & 4 \end{array} \right). \\ \end{array}
$$

考研电子书网站:www.pdf2book.com

41

---

第2章 矩阵及其运算

例14 设 $P = \begin{pmatrix} 1 & 2 \\ 1 & 4 \end{pmatrix}, A = \begin{pmatrix} 1 & 0 \\ 0 & 2 \end{pmatrix}, AP = P\Lambda$，求 $A^n$.

解  $\left|P\right|=2,\quad P^{-1}=\frac{1}{2}\begin{pmatrix}4&-2\\-1&1\end{pmatrix},$

$$
A = P \Lambda P ^ {- 1}, \quad A ^ {2} = P \Lambda P ^ {- 1} P \Lambda \dot {P} ^ {- 1} = P \Lambda^ {2} P ^ {- 1}, \quad \dots , \quad A ^ {n} = P \Lambda^ {n} P ^ {- 1},
$$

而

$$
\boldsymbol {A} = \left( \begin{array}{c c} 1 & 0 \\ 0 & 2 \end{array} \right), \quad \boldsymbol {A} ^ {2} = \left( \begin{array}{c c} 1 & 0 \\ 0 & 2 \end{array} \right) \left( \begin{array}{c c} 1 & 0 \\ 0 & 2 \end{array} \right) = \left( \begin{array}{c c} 1 & 0 \\ 0 & 2 ^ {2} \end{array} \right), \quad \dots , \quad \boldsymbol {A} ^ {n} = \left( \begin{array}{c c} 1 & 0 \\ 0 & 2 ^ {n} \end{array} \right),
$$

故

$$
\begin{array}{l} \boldsymbol {A} ^ {n} = \left( \begin{array}{l l} 1 & 2 \\ 1 & 4 \end{array} \right) \left( \begin{array}{l l} 1 & 0 \\ 0 & 2 ^ {n} \end{array} \right) \frac {1}{2} \left( \begin{array}{c c} 4 & - 2 \\ - 1 & 1 \end{array} \right) = \frac {1}{2} \left( \begin{array}{c c} 1 & 2 ^ {n + 1} \\ 1 & 2 ^ {n + 2} \end{array} \right) \left( \begin{array}{c c} 4 & - 2 \\ - 1 & 1 \end{array} \right) \\ = \frac {1}{2} \left( \begin{array}{l l} 4 - 2 ^ {n + 1} & 2 ^ {n + 1} - 2 \\ 4 - 2 ^ {n + 2} & 2 ^ {n + 2} - 2 \end{array} \right) = \left( \begin{array}{c c} 2 - 2 ^ {n} & 2 ^ {n} - 1 \\ 2 - 2 ^ {n + 1} & 2 ^ {n + 1} - 1 \end{array} \right). \\ \end{array}
$$

设  $\varphi(x)=a_{0}+a_{1}x+\cdots+a_{m}x^{m}$  为 x 的 m 次多项式, A 为 n 阶矩阵, 记

$$
\varphi (\mathbf {A}) = a _ {0} \mathbf {E} + a _ {1} \mathbf {A} + \dots + a _ {m} \mathbf {A} ^ {m},
$$

$\varphi(A)$ 称为矩阵A的m次多项式.

因为矩阵 $A^k, A'$ 和 $\pmb{E}$ 都是可交换的，所以矩阵 $\pmb{A}$ 的两个多项式 $\varphi(A)$ 和 $f(A)$ 也是可交换的，即总有

$$
\varphi (\boldsymbol {A}) f (\boldsymbol {A}) = f (\boldsymbol {A}) \varphi (\boldsymbol {A}),
$$

从而关于 $A$ 的多项式可以像数 $x$ 的多项式一样相乘或分解因式.例如

$$
(E + A) (2 E - A) = 2 E + A - A ^ {2},
$$

$$
(E - A) ^ {3} = E - 3 A + 3 A ^ {2} - A ^ {3}.
$$

我们常用例14中计算 $A^k$ 的方法来计算 $\pmb{A}$ 的多项式 $\varphi(A)$，这就是

(i) 若 $A = P\Lambda P^{-1}$, 则 $A^{k} = P\Lambda^{k}P^{-1}$, 从而

$$
\varphi (\boldsymbol {A}) = a _ {0} \boldsymbol {E} + a _ {1} \boldsymbol {A} + \dots + a _ {m} \boldsymbol {A} ^ {m} = P a _ {0} \boldsymbol {E} \boldsymbol {P} ^ {- 1} + P a _ {1} \boldsymbol {\Lambda} \boldsymbol {P} ^ {- 1} + \dots + P a _ {m} \boldsymbol {\Lambda} ^ {m} \boldsymbol {P} ^ {- 1} = P \varphi (\boldsymbol {\Lambda}) \boldsymbol {P} ^ {- 1}.
$$

(ii) 若  $\boldsymbol{\Lambda}=\mathrm{diag}(\lambda_{1},\lambda_{2},\cdots,\lambda_{n})$  为对角矩阵，则  $\boldsymbol{\Lambda}^{k}=\mathrm{diag}(\lambda_{1}^{k},\lambda_{2}^{k},\cdots,\lambda_{n}^{k})$ ，从而

$$
\varphi (\Lambda) = a _ {0} E + a _ {1} \Lambda + \dots + a _ {m} \Lambda^ {m}
$$

$$
= a _ {0} \left( \begin{array}{c c c c} 1 & & & \\ & 1 & & \\ & & \ddots & \\ & & & 1 \end{array} ,\right) + a _ {1} \left( \begin{array}{c c c c} \lambda_ {1} & & & \\ & \lambda_ {2} & & \\ & & \ddots & \\ & & & \lambda_ {n} \end{array} \right) + \dots + a _ {m} \left( \begin{array}{c c c c} \lambda_ {1} ^ {m} & & & \\ & \lambda_ {2} ^ {m} & & \\ & & \ddots & \\ & & & \lambda_ {n} ^ {m} \end{array} \right)
$$

42

---

§3 逆矩阵

$$
= \left( \begin{array}{c c c c} \varphi (\lambda_ {1}) & & & \\ & \varphi (\lambda_ {2}) & & \\ & & \ddots & \\ & & & \varphi (\lambda_ {n}) \end{array} \right).
$$

上式表明当  $\Lambda=\mathrm{diag}(\lambda_{1},\lambda_{2},\cdots,\lambda_{n})$  为 n 阶对角矩阵时， $\varphi(\Lambda)$  也是 n 阶对角矩阵，且它的第 i 个对角元为  $\varphi(\lambda_{i})$ ，归结为数的多项式计算  $(i=1,2,\cdots,n)$ ，这给计算  $\varphi(\Lambda)$  以及经由 (i) 来计算  $\varphi(A)$  带来很大的方便。请看下例，在第 5 章中将进一步讨论这个问题。

例15 设 $P = \begin{pmatrix} -1 & 1 & 1 \\ 1 & 0 & 2 \\ 1 & 1 & -1 \end{pmatrix}, \Lambda = \begin{pmatrix} 1 & & \\ & 2 & \\ & & -3 \end{pmatrix}, \mathbf{A}\mathbf{P} = \mathbf{P}\mathbf{A}$, 求 $\varphi(\mathbf{A}) = \mathbf{A}^3 + 2\mathbf{A}^2 - 3\mathbf{A}$.

解  $\left|P\right|= \begin{vmatrix}-1 & 1 & 1 \\ 1 & 0 & 2 \\ 1 & 1 & -1 \end{vmatrix} \xlongequal{r_{1}+r_{3}} \begin{vmatrix}0 & 2 & 0 \\ 1 & 0 & 2 \\ 1 & 1 & -1 \end{vmatrix}=6,$

故 P 可逆, 从而

$$
\boldsymbol {A} = \boldsymbol {P} \boldsymbol {\Lambda} \boldsymbol {P} ^ {- 1}, \quad \varphi (\boldsymbol {A}) = \boldsymbol {P} \varphi (\boldsymbol {\Lambda}) \boldsymbol {P} ^ {- 1}.
$$

而 $\varphi(1) = 0, \varphi(2) = 10, \varphi(-3) = 0$，故 $\varphi(A) = \mathrm{diag}(0, 10, 0)$.

$$
\begin{array}{l} \varphi (\boldsymbol {A}) = \boldsymbol {P} \varphi (\boldsymbol {\Lambda}) \boldsymbol {P} ^ {- 1} = \left( \begin{array}{c c c} - 1 & 1 & 1 \\ 1 & 0 & 2 \\ 1 & 1 & - 1 \end{array} \right) \left( \begin{array}{c c c} 0 & & \\ & 1 0 & \\ & & 0 \end{array} \right) \frac {1}{| \boldsymbol {P} |} \boldsymbol {P} ^ {*} \\ = \frac {1 0}{6} \left( \begin{array}{c c c} 0 & 1 & 0 \\ 0 & 0 & 0 \\ 0 & 1 & 0 \end{array} \right) \left( \begin{array}{c c c} A _ {1 1} & A _ {2 1} & A _ {3 1} \\ A _ {1 2} & A _ {2 2} & A _ {3 2} \\ A _ {1 3} & A _ {2 3} & A _ {3 3} \end{array} \right) = \frac {5}{3} \left( \begin{array}{c c c} A _ {1 2} & A _ {2 2} & A _ {3 2} \\ 0 & 0 & 0 \\ A _ {1 2} & A _ {2 2} & A _ {3 2} \end{array} \right), \\ \end{array}
$$

而

$$
A _ {1 2} = - \left| \begin{array}{c c} 1 & 2 \\ 1 & - 1 \end{array} \right| = 3, \quad A _ {2 2} = \left| \begin{array}{c c} - 1 & 1 \\ 1 & - 1 \end{array} \right| = 0, \quad A _ {3 2} = - \left| \begin{array}{c c} - 1 & 1 \\ 1 & 2 \end{array} \right| = 3,
$$

于是

$$
\varphi (A) = 5 \left( \begin{array}{c c c} 1 & 0 & 1 \\ 0 & 0 & 0 \\ 1 & 0 & 1 \end{array} \right).
$$

考研电子书网站:www.pdf2book.com

43

---

第2章 矩阵及其运算

## § 4 克拉默法则

在第1章例1中,我们利用二阶行列式求解了由两个二元线性方程组成的方程组.现在进行推广,介绍求解由n个n元线性方程组成的方程组的克拉默法则.

克拉默法则 设有 n 个未知数  $x_{1}, x_{2}, \cdots, x_{n}$  的 n 个线性方程的方程组

$$
\left\{ \begin{array}{l} a _ {1 1} x _ {1} + a _ {1 2} x _ {2} + \dots + a _ {1 n} x _ {n} = b _ {1}, \\ a _ {2 1} x _ {1} + a _ {2 2} x _ {2} + \dots + a _ {2 n} x _ {n} = b _ {2}, \\ \dots \dots \\ a _ {n 1} x _ {1} + a _ {n 2} x _ {2} + \dots + a _ {n n} x _ {n} = b _ {n}, \end{array} \right. \tag {9}
$$

如果线性方程组(9)的系数矩阵 $A$ 的行列式不等于零，即

$$
| \boldsymbol {A} | = \left| \begin{array}{c c c c} a _ {1 1} & a _ {1 2} & \dots & a _ {1 n} \\ a _ {2 1} & a _ {2 2} & \dots & a _ {2 n} \\ \vdots & \vdots & & \vdots \\ a _ {n 1} & a _ {n 2} & \dots & a _ {n n} \end{array} \right| \neq 0,
$$

那么方程组(9)有惟一解

$$
x _ {1} = \frac {\left| A _ {1} \right|}{\left| A \right|}, \quad x _ {2} = \frac {\left| A _ {2} \right|}{\left| A \right|}, \quad \dots , \quad x _ {n} = \frac {\left| A _ {n} \right|}{\left| A \right|},
$$

其中  $A_{j}(j=1,2,\cdots,n)$  是把系数矩阵 A 中第 j 列的元素用方程组右端的常数项代替后所得到的 n 阶矩阵，即

$$
\boldsymbol {A} _ {j} = \left( \begin{array}{c c c c c c c} a _ {1 1} & \dots & a _ {1, j - 1} & b _ {1} & a _ {1, j + 1} & \dots & a _ {1 n} \\ \vdots & & \vdots & \vdots & \vdots & & \vdots \\ a _ {n 1} & \dots & a _ {n, j - 1} & b _ {n} & a _ {n, j + 1} & \dots & a _ {n n} \end{array} \right).
$$

证 把方程组(9)写成矩阵方程

$$
A x = b,
$$

这里 $A = (a_{ij})_{n\times n}$ 为 $n$ 阶矩阵，因 $\left|A\right|\neq 0$ ，故 $A^{-1}$ 存在

令 $x = A^{-1}b$ ，有

$$
A x = A A ^ {- 1} b = b,
$$

表明  $x=A^{-1}b$  是方程组(9)的解.

由 Ax=b，有  $A^{-1}Ax=A^{-1}b$ ，即  $x=A^{-1}b$ ，根据逆矩阵的惟一性，知  $x=A^{-1}b$  是方程组 (9) 的惟一解.

由逆矩阵公式 $A^{-1} = \frac{1}{|A|} A^*$，有 $x = A^{-1}b = \frac{1}{|A|} A^* b$，即

44

---

§ 4 克拉默法则

$$
\left( \begin{array}{c} x _ {1} \\ x _ {2} \\ \vdots \\ x _ {n} \end{array} \right) = \frac {1}{| \boldsymbol {A} |} \left( \begin{array}{c c c c} A _ {1 1} & A _ {2 1} & \dots & A _ {n 1} \\ A _ {1 2} & A _ {2 2} & \dots & A _ {n 2} \\ \vdots & \vdots & & \vdots \\ A _ {1 n} & A _ {2 n} & \dots & A _ {n n} \end{array} \right) \left( \begin{array}{c} b _ {1} \\ b _ {2} \\ \vdots \\ b _ {n} \end{array} \right) = \frac {1}{| \boldsymbol {A} |} \left( \begin{array}{c} b _ {1} A _ {1 1} + b _ {2} A _ {2 1} + \dots + b _ {n} A _ {n 1} \\ b _ {1} A _ {1 2} + b _ {2} A _ {2 2} + \dots + b _ {n} A _ {n 2} \\ \vdots \\ b _ {1} A _ {1 n} + b _ {2} A _ {2 n} + \dots + b _ {n} A _ {n n} \end{array} \right),
$$

亦即

$$
x _ {j} = \frac {1}{| A |} (b _ {1} A _ {1 j} + b _ {2} A _ {2 j} + \dots + b _ {n} A _ {n j}) = \frac {1}{| A |} | A _ {j} | \quad (j = 1, 2, \dots , n). \quad \text {证毕}
$$

克拉默法则可视为行列式的一个应用,而所给出的证明又可看作逆矩阵的一个应用.它解决的是方程个数与未知数个数相等并且系数行列式不等于零的线性方程组.所以它既是第1章例1中用二阶行列式求解方程组的推广,又是下一章中求解一般线性方程组的一个特殊的情形.

例16 分别用克拉默法则和逆矩阵方法求解线性方程组

$$
\left\{ \begin{array}{l} x _ {1} - x _ {2} - x _ {3} = 2, \\ 2 x _ {1} - x _ {2} - 3 x _ {3} = 1, \\ 3 x _ {1} + 2 x _ {2} - 5 x _ {3} = 0. \end{array} \right.
$$

解 （1）用克拉默法则. 因方程组的系数矩阵的行列式  $\left|A\right|= \begin{vmatrix}1 & -1 & -1 \\ 2 & -1 & -3 \\ 3 & 2 & -5 \end{vmatrix}=3 \neq$

0, 由克拉默法则, 它有惟一解, 并且

$$
x _ {1} = \frac {1}{| A |} \left| \begin{array}{c c c} 2 & - 1 & - 1 \\ 1 & - 1 & - 3 \\ 0 & 2 & - 5 \end{array} \right| \stackrel {r _ {1} \leftrightarrow r _ {2}} {=} - \frac {1}{3} \left| \begin{array}{c c c} 1 & - 1 & - 3 \\ 2 & - 1 & - 1 \\ 0 & 2 & - 5 \end{array} \right| \stackrel {r _ {2} - 2 r _ {1}} {\overline {{r _ {3} - 2 r _ {2}}}} - \frac {1}{3} \left| \begin{array}{c c c} 1 & - 1 & - 3 \\ 0 & 1 & 5 \\ 0 & 0 & - 1 5 \end{array} \right| = 5,
$$

$$
x _ {2} = \frac {1}{| A |} \left| \begin{array}{l l l} 1 & 2 & - 1 \\ 2 & 1 & - 3 \\ 3 & 0 & - 5 \end{array} \right| \frac {r _ {2} - 2 r _ {1}}{\overline {{r _ {3} - 3 r _ {1}}}} \frac {1}{3} \left| \begin{array}{c c c} 1 & 2 & - 1 \\ 0 & - 3 & - 1 \\ 0 & - 6 & - 2 \end{array} \right| = 0,
$$

$$
x _ {3} = \frac {1}{| A |} \left| \begin{array}{c c c} 1 & - 1 & 2 \\ 2 & - 1 & 1 \\ 3 & 2 & 0 \end{array} \right| \frac {r _ {2} - 2 r _ {1}}{\overline {{r _ {3} - 3 r _ {1}}}} \frac {1}{3} \left| \begin{array}{c c c} 1 & - 1 & 2 \\ 0 & 1 & - 3 \\ 0 & 5 & - 6 \end{array} \right| = \frac {1}{3} \left| \begin{array}{c c} 1 & - 3 \\ 5 & - 6 \end{array} \right| = 3.
$$

(2) 用逆矩阵方法. 因  $\left|A\right|=3\neq0$ , 故 A 可逆, 于是

$$
\boldsymbol {x} = \boldsymbol {A} ^ {- 1} \boldsymbol {b} = \left( \begin{array}{c c c} 1 & - 1 & - 1 \\ 2 & - 1 & - 3 \\ 3 & 2 & - 5 \end{array} \right) ^ {- 1} \left( \begin{array}{c} 2 \\ 1 \\ 0 \end{array} \right) = \frac {1}{3} \left( \begin{array}{c c c} 1 1 & - 7 & 2 \\ 1 & - 2 & 1 \\ 7 & - 5 & 1 \end{array} \right) \left( \begin{array}{c} 2 \\ 1 \\ 0 \end{array} \right) = \frac {1}{3} \left( \begin{array}{c} 1 5 \\ 0 \\ 9 \end{array} \right) = \left( \begin{array}{c} 5 \\ 0 \\ 3 \end{array} \right),
$$

即有

考研电子书网站:www.pdf2book.com

45

---

第2章 矩阵及其运算

$$
\left\{ \begin{array}{l} x _ {1} = 5, \\ x _ {2} = 0, \\ x _ {3} = 3. \end{array} \right.
$$

## § 5 矩阵分块法

对于行数和列数较多的矩阵 A, 运算时常采用分块法, 使大矩阵的运算化成小矩阵的运算. 将矩阵 A 用若干条纵线和横线分成许多个小矩阵, 每一个小矩阵称为 A 的子块, 以子块为元素的形式上的矩阵称为分块矩阵.

例如将 $3 \times 4$ 矩阵

$$
\boldsymbol {A} = \left( \begin{array}{c c c c} a _ {1 1} & a _ {1 2} & a _ {1 3} & a _ {1 4} \\ a _ {2 1} & a _ {2 2} & a _ {2 3} & a _ {2 4} \\ a _ {3 1} & a _ {3 2} & a _ {3 3} & a _ {3 4} \end{array} \right)
$$

分成子块的分法很多,下面举出三种分块形式:

(i) $\begin{pmatrix}a_{11}&a_{12}&a_{13}&a_{14}\\a_{21}&a_{22}&a_{23}&a_{24}\\ \hline a_{31}&a_{32}&a_{33}&a_{34}\end{pmatrix},$

(ii) $\left( \begin{array}{c|cc:c}a_{11} & a_{12} & a_{13} & a_{14}\\ a_{21} & a_{22} & a_{23} & a_{24}\\ \hline a_{31} & a_{32} & a_{33} & a_{34} \end{array} \right),$

(iii) $\begin{pmatrix}a_{11}&a_{12}&a_{13}&a_{14}\\a_{21}&a_{22}&a_{23}&a_{24}\\a_{31}&a_{32}&a_{33}&a_{34}\end{pmatrix}.$

分法(i)可记为

$$
\boldsymbol {A} = \left( \begin{array}{c c} \boldsymbol {A} _ {1 1} & \boldsymbol {A} _ {1 2} \\ \boldsymbol {A} _ {2 1} & \boldsymbol {A} _ {2 2} \end{array} \right),
$$

其中

$$
\boldsymbol {A} _ {1 1} = \left( \begin{array}{l l} a _ {1 1} & a _ {1 2} \\ a _ {2 1} & a _ {2 2} \end{array} \right), \quad \boldsymbol {A} _ {1 2} = \left( \begin{array}{l l} a _ {1 3} & a _ {1 4} \\ a _ {2 3} & a _ {2 4} \end{array} \right), \quad \boldsymbol {A} _ {2 1} = (a _ {3 1}, a _ {3 2}), \quad \boldsymbol {A} _ {2 2} = (a _ {3 3}, a _ {3 4}),
$$

即 $A_{11}, A_{12}, A_{21}, A_{22}$ 为 $\pmb{A}$ 的子块，而 $\pmb{A}$ 形式上成为以这些子块为元的分块矩阵。分法(ii)及(iii)的分块矩阵请读者写出。

本章 §2 证明公式 $|AB| = |A||B|$ 时出现的矩阵 $\begin{pmatrix} A & O \\ -E & B \end{pmatrix}$ 及 $\begin{pmatrix} A & AB \\ -E & O \end{pmatrix}$ 正是分块矩阵, 在那里是把四个矩阵拼成一个大矩阵, 这与把大矩阵分成多个小矩阵是同一个概念的两个方面. 公众号: 旗胜考研

分块矩阵的运算规则与普通矩阵的运算规则相类似,分别说明如下:

(i) 设矩阵 A 与 B 的行数相同、列数相同, 采用相同的分块法, 有

46

---

§5 矩阵分块法

$$
\boldsymbol {A} = \left( \begin{array}{c c c c} \boldsymbol {A} _ {1 1} & \boldsymbol {A} _ {1 2} & \dots & \boldsymbol {A} _ {1 r} \\ \boldsymbol {A} _ {2 1} & \boldsymbol {A} _ {2 2} & \dots & \boldsymbol {A} _ {2 r} \\ \vdots & \vdots & & \vdots \\ \boldsymbol {A} _ {s 1} & \boldsymbol {A} _ {s 2} & \dots & \boldsymbol {A} _ {s r} \end{array} \right), \quad \boldsymbol {B} = \left( \begin{array}{c c c c} \boldsymbol {B} _ {1 1} & \boldsymbol {B} _ {1 2} & \dots & \boldsymbol {B} _ {1 r} \\ \boldsymbol {B} _ {2 1} & \boldsymbol {B} _ {2 2} & \dots & \boldsymbol {B} _ {2 r} \\ \vdots & \vdots & & \vdots \\ \boldsymbol {B} _ {s 1} & \boldsymbol {B} _ {s 2} & \dots & \boldsymbol {B} _ {s r} \end{array} \right),
$$

其中 $A_{ij}$ 与 $\pmb{B}_{ij}$ 的行数相同、列数相同，那么

$$
\boldsymbol {A} + \boldsymbol {B} = \left( \begin{array}{c c c c} \boldsymbol {A} _ {1 1} + \boldsymbol {B} _ {1 1} & \boldsymbol {A} _ {1 2} + \boldsymbol {B} _ {1 2} & \dots & \boldsymbol {A} _ {1 r} + \boldsymbol {B} _ {1 r} \\ \boldsymbol {A} _ {2 1} + \boldsymbol {B} _ {2 1} & \boldsymbol {A} _ {2 2} + \boldsymbol {B} _ {2 2} & \dots & \boldsymbol {A} _ {2 r} + \boldsymbol {B} _ {2 r} \\ \vdots & \vdots & & \vdots \\ \boldsymbol {A} _ {s 1} + \boldsymbol {B} _ {s 1} & \boldsymbol {A} _ {s 2} + \boldsymbol {B} _ {s 2} & \dots & \boldsymbol {A} _ {s r} + \boldsymbol {B} _ {s r} \end{array} \right).
$$

(ii) 设  $A = \begin{pmatrix} A_{11} & A_{12} & \cdots & A_{1r} \\ A_{21} & A_{22} & \cdots & A_{2r} \\ \vdots & \vdots & & \vdots \\ A_{s1} & A_{s2} & \cdots & A_{sr} \end{pmatrix}, \lambda$  为数, 那么

$$
\lambda \boldsymbol {A} = \left( \begin{array}{c c c c} \lambda \boldsymbol {A} _ {1 1} & \lambda \boldsymbol {A} _ {1 2} & \dots & \lambda \boldsymbol {A} _ {1 r} \\ \lambda \boldsymbol {A} _ {2 1} & \lambda \boldsymbol {A} _ {2 2} & \dots & \lambda \boldsymbol {A} _ {2 r} \\ \vdots & \vdots & & \vdots \\ \lambda \boldsymbol {A} _ {s 1} & \lambda \boldsymbol {A} _ {s 2} & \dots & \lambda \boldsymbol {A} _ {s r} \end{array} \right).
$$

(iii) 设 A 为  $m \times l$  矩阵, B 为  $l \times n$  矩阵, 分块成

$$
\boldsymbol {A} = \left( \begin{array}{c c c c} \boldsymbol {A} _ {1 1} & \boldsymbol {A} _ {1 2} & \dots & \boldsymbol {A} _ {1 t} \\ \boldsymbol {A} _ {2 1} & \boldsymbol {A} _ {2 2} & \dots & \boldsymbol {A} _ {2 t} \\ \vdots & \vdots & & \vdots \\ \boldsymbol {A} _ {s 1} & \boldsymbol {A} _ {s 2} & \dots & \boldsymbol {A} _ {s t} \end{array} \right), \quad \boldsymbol {B} = \left( \begin{array}{c c c c} \boldsymbol {B} _ {1 1} & \boldsymbol {B} _ {1 2} & \dots & \boldsymbol {B} _ {1 r} \\ \boldsymbol {B} _ {2 1} & \boldsymbol {B} _ {2 2} & \dots & \boldsymbol {B} _ {2 r} \\ \vdots & \vdots & & \vdots \\ \boldsymbol {B} _ {t 1} & \boldsymbol {B} _ {t 2} & \dots & \boldsymbol {B} _ {t r} \end{array} \right),
$$

其中 $A_{i1}, A_{i2}, \cdots, A_{it}$ 的列数分别等于 $B_{1j}, B_{2j}, \cdots, B_{tj}$ 的行数，那么

$$
\boldsymbol {A B} = \left( \begin{array}{c c c c} \boldsymbol {C} _ {1 1} & \boldsymbol {C} _ {1 2} & \dots & \boldsymbol {C} _ {1 r} \\ \boldsymbol {C} _ {2 1} & \boldsymbol {C} _ {2 2} & \dots & \boldsymbol {C} _ {2 r} \\ \vdots & \vdots & & \vdots \\ \boldsymbol {C} _ {s 1} & \boldsymbol {C} _ {s 2} & \dots & \boldsymbol {C} _ {s r} \end{array} \right),
$$

其中

$$
\boldsymbol {C} _ {i j} = \sum_ {k = 1} ^ {t} \boldsymbol {A} _ {i k} \boldsymbol {B} _ {k j} \quad (i = 1, 2, \dots , s; j = 1, 2, \dots , r).
$$

例17 设

47

---

第2章 矩阵及其运算

$$
\boldsymbol {A} = \left( \begin{array}{r r r r} 1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ - 1 & 2 & 1 & 0 \\ 1 & 1 & 0 & 1 \end{array} \right), \quad \boldsymbol {B} = \left( \begin{array}{r r r r} 1 & 0 & 1 & 0 \\ - 1 & 2 & 0 & 1 \\ 1 & 0 & 4 & 1 \\ - 1 & - 1 & 2 & 0 \end{array} \right),
$$

求AB.

解 把 $A, B$ 分块成

$$
\begin{array}{l} \boldsymbol {A} = \left( \begin{array}{c c c c} 1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ \hdashline - 1 & 2 & 1 & 0 \\ 1 & 1 & 0 & 1 \end{array} \right) = \left( \begin{array}{c c} \boldsymbol {E} & \boldsymbol {O} \\ \boldsymbol {A} _ {1} & \boldsymbol {E} \end{array} \right), \\ \boldsymbol {B} = \left( \begin{array}{c c c c} 1 & 0 & 1 & 0 \\ - 1 & 2 & 0 & 1 \\ \hdashline 1 & 0 & 4 & 1 \\ - 1 & - 1 & 2 & 0 \end{array} \right) = \left( \begin{array}{c c} \boldsymbol {B} _ {1 1} & \boldsymbol {E} \\ \boldsymbol {B} _ {2 1} & \boldsymbol {B} _ {2 2} \end{array} \right), \\ \end{array}
$$

则

$$
\boldsymbol {A} \boldsymbol {B} = \left( \begin{array}{c c} \boldsymbol {E} & \boldsymbol {O} \\ \boldsymbol {A} _ {1} & \boldsymbol {E} \end{array} \right) \left( \begin{array}{c c} \boldsymbol {B} _ {1 1} & \boldsymbol {E} \\ \boldsymbol {B} _ {2 1} & \boldsymbol {B} _ {2 2} \end{array} \right) = \left( \begin{array}{c c} \boldsymbol {B} _ {1 1} & \boldsymbol {E} \\ \boldsymbol {A} _ {1} \boldsymbol {B} _ {1 1} + \boldsymbol {B} _ {2 1} & \boldsymbol {A} _ {1} + \boldsymbol {B} _ {2 2} \end{array} \right),
$$

而

$$
\boldsymbol {A} _ {1} \boldsymbol {B} _ {1 1} + \boldsymbol {B} _ {2 1} = \left( \begin{array}{c c} - 1 & 2 \\ 1 & 1 \end{array} \right) \cdot \left( \begin{array}{c c} 1 & 0 \\ - 1 & 2 \end{array} \right) + \left( \begin{array}{c c} 1 & 0 \\ - 1 & - 1 \end{array} \right) = \left( \begin{array}{c c} - 3 & 4 \\ 0 & 2 \end{array} \right) + \left( \begin{array}{c c} 1 & 0 \\ - 1 & - 1 \end{array} \right) = \left( \begin{array}{c c} - 2 & 4 \\ - 1 & 1 \end{array} \right),
$$

$$
\boldsymbol {A} _ {1} + \boldsymbol {B} _ {2 2} = \left( \begin{array}{c c} - 1 & 2 \\ 1 & 1 \end{array} \right) + \left( \begin{array}{c c} 4 & 1 \\ 2 & 0 \end{array} \right) = \left( \begin{array}{c c} 3 & 3 \\ 3 & 1 \end{array} \right),
$$

于是

$$
\boldsymbol {A} \boldsymbol {B} = \left( \begin{array}{c c c c} 1 & 0 & 1 & 0 \\ - 1 & 2 & 0 & 1 \\ \hdashline - 2 & 4 & 3 & 3 \\ - 1 & 1 & 3 & 1 \end{array} \right).
$$

$$
\text {(iv)} \text {设} \boldsymbol {A} = \left( \begin{array}{c c c c} \boldsymbol {A} _ {1 1} & \boldsymbol {A} _ {1 2} & \dots & \boldsymbol {A} _ {1 r} \\ \boldsymbol {A} _ {2 1} & \boldsymbol {A} _ {2 2} & \dots & \boldsymbol {A} _ {2 r} \\ \vdots & \vdots & & \vdots \\ \boldsymbol {A} _ {s 1} & \boldsymbol {A} _ {s 2} & \ddots & \boldsymbol {A} _ {s r} \end{array} \right), \text {则} \boldsymbol {A} ^ {\mathrm{T}} = \left( \begin{array}{c c c c} \boldsymbol {A} _ {1 1} ^ {\mathrm{T}} & \boldsymbol {A} _ {2 1} ^ {\mathrm{T}} & \dots & \boldsymbol {A} _ {s 1} ^ {\mathrm{T}} \\ \boldsymbol {A} _ {1 2} ^ {\mathrm{T}} & \boldsymbol {A} _ {2 2} ^ {\mathrm{T}} & \dots & \boldsymbol {A} _ {s 2} ^ {\mathrm{T}} \\ \vdots & \vdots & & \vdots \\ \boldsymbol {A} _ {1 r} ^ {\mathrm{T}} & \boldsymbol {A} _ {2 r} ^ {\mathrm{T}} & \dots & \boldsymbol {A} _ {s r} ^ {\mathrm{T}} \end{array} \right).
$$

（v）设 $\pmb{A}$ 为 $n$ 阶方阵，若 $\pmb{A}$ 的分块矩阵只有在对角线上有非零子块，其余子块都为零矩阵，且在对角线上的子块都是方阵，即

48

---

§5 矩阵分块法

$$
A = \left( \begin{array}{c c c} A _ {1} & & O \\ & A _ {2} & \\ & & \ddots \\ O & & A _ {s} \end{array} \right),
$$

其中  $A_{i}$  ( $i=1,2,\cdots,s$ ) 都是方阵, 那么称 A 为分块对角矩阵.

分块对角矩阵的行列式具有性质

$$
\left| \boldsymbol {A} \right| = \left| \boldsymbol {A} _ {1} \right| \left| \boldsymbol {A} _ {2} \right| \dots \left| \boldsymbol {A} _ {s} \right|.
$$

由此性质可知, 若  $\left|A_{i}\right|\neq0\left(i=1,2,\cdots,s\right)$ , 则  $\left|A\right|\neq0$ , 并有

$$
\boldsymbol {A} _ {\cdot} ^ {- 1} = \left( \begin{array}{c c c c} \boldsymbol {A} _ {1} ^ {- 1} & & & \boldsymbol {O} \\ & \boldsymbol {A} _ {2} ^ {- 1} & & \\ & & \ddots & \\ & & & \ddots \\ \boldsymbol {O} & & & \boldsymbol {A} _ {s} ^ {- 1} \end{array} \right).
$$

例18 设 $A = \begin{pmatrix} 5 & 0 & 0 \\ 0 & 3 & 1 \\ 0 & 2 & 1 \end{pmatrix}$, 求 $A^{-1}$.

解因

$$
\boldsymbol {A} = \left( \begin{array}{c c c} 5 & 0 & 0 \\ \hdashline 0 & 3 & 1 \\ 0 & 2 & 1 \end{array} \right) = \left( \begin{array}{c c} \boldsymbol {A} _ {1} & \boldsymbol {O} \\ \boldsymbol {O} & \boldsymbol {A} _ {2} \end{array} \right),
$$

$$
\boldsymbol {A} _ {1} = (5), \quad \boldsymbol {A} _ {1} ^ {- 1} = \left(\frac {1}{5}\right); \quad \boldsymbol {A} _ {2} = \left( \begin{array}{c c} 3 & 1 \\ 2 & 1 \end{array} \right), \quad \boldsymbol {A} _ {2} ^ {- 1} = \left( \begin{array}{c c} 1 & - 1 \\ - 2 & 3 \end{array} \right),
$$

所以

$$
\boldsymbol {A} ^ {- 1} = \left( \begin{array}{c c c} \frac {1}{5} & 0 & 0 \\ \hline 0 & 1 & - 1 \\ 0 & - 2 & 3 \end{array} \right).
$$

对矩阵分块时,有两种分块法应予特别重视,这就是按列分块和按行分块.

$m \times n$ 矩阵 $A$ 有 $n$ 列, 称为矩阵 $A$ 的 $n$ 个列向量, 若第 $j$ 列记作

$$
\boldsymbol {a} _ {j} = \left( \begin{array}{c} \boldsymbol {a} _ {1 j} \\ \boldsymbol {a} _ {2 j} \\ \vdots \\ \boldsymbol {a} _ {m j} \end{array} \right),
$$

则 $A$ 可按列分块为

考研电子书网站:www.pdf2book.com

49

---

第2章 矩阵及其运算

$$
A = (a _ {1}, a _ {2}, \dots , a _ {n});
$$

$m \times n$ 矩阵 A 有 m 行, 称为矩阵 A 的 m 个行向量. 若第 i 行记作

$$
\boldsymbol {\alpha} _ {i} ^ {\mathrm{T}} = (a _ {i 1}, a _ {i 2}, \dots , a _ {i n}) ①,
$$

则 $\mathbf{A}$ 可按行分块为

$$
\boldsymbol {A} = \left( \begin{array}{c} \boldsymbol {\alpha} _ {1} ^ {\mathrm{T}} \\ \boldsymbol {\alpha} _ {2} ^ {\mathrm{T}} \\ \vdots \\ \boldsymbol {\alpha} _ {m} ^ {\mathrm{T}} \end{array} \right).
$$

对于矩阵 $A = (a_{ij})_{m \times s}$ 与矩阵 $B = (b_{ij})_{s \times n}$ 的乘积矩阵 $AB = C = (c_{ij})_{m \times n}$, 若把 $A$ 按行分成 $m$ 块, 把 $B$ 按列分成 $n$ 块, 便有

$$
\boldsymbol {A} \boldsymbol {B} = \left( \begin{array}{c} \boldsymbol {\alpha} _ {1} ^ {\mathrm{T}} \\ \boldsymbol {\alpha} _ {2} ^ {\mathrm{T}} \\ \vdots \\ \boldsymbol {\alpha} _ {m} ^ {\mathrm{T}} \end{array} \right) (\boldsymbol {b} _ {1}, \boldsymbol {b} _ {2}, \dots , \boldsymbol {b} _ {n}) = \left( \begin{array}{c c c c} \boldsymbol {\alpha} _ {1} ^ {\mathrm{T}} \boldsymbol {b} _ {1} & \boldsymbol {\alpha} _ {1} ^ {\mathrm{T}} \boldsymbol {b} _ {2} & \dots & \boldsymbol {\alpha} _ {1} ^ {\mathrm{T}} \boldsymbol {b} _ {n} \\ \boldsymbol {\alpha} _ {2} ^ {\mathrm{T}} \boldsymbol {b} _ {1} & \boldsymbol {\alpha} _ {2} ^ {\mathrm{T}} \boldsymbol {b} _ {2} & \dots & \boldsymbol {\alpha} _ {2} ^ {\mathrm{T}} \boldsymbol {b} _ {n} \\ \vdots & \vdots & & \vdots \\ \boldsymbol {\alpha} _ {m} ^ {\mathrm{T}} \boldsymbol {b} _ {1} & \boldsymbol {\alpha} _ {m} ^ {\mathrm{T}} \boldsymbol {b} _ {2} & \dots & \boldsymbol {\alpha} _ {m} ^ {\mathrm{T}} \boldsymbol {b} _ {n} \end{array} \right) = (c _ {i j}) _ {m \times n},
$$

其中

$$
c _ {i j} = \boldsymbol {\alpha} _ {i} ^ {\mathrm{T}} \boldsymbol {b} _ {j} = (a _ {i 1}, a _ {i 2}, \dots , a _ {i s}) \left( \begin{array}{c} b _ {1 j} \\ b _ {2 j} \\ \vdots \\ b _ {s j} \end{array} \right) = \sum_ {k = 1} ^ {s} a _ {i k} b _ {k j},
$$

由此可进一步领会矩阵相乘的定义.

例 19 证明矩阵 A = O 的充分必要条件是方阵  $A^{T}A = O$ .

证 条件的必要性是显然的,下面证明条件的充分性.

设  $\boldsymbol{A}=(a_{ij})_{m\times n}$ ，把 A 按列分块为  $\boldsymbol{A}=(\boldsymbol{a}_{1},\boldsymbol{a}_{2},\cdots,\boldsymbol{a}_{n})$ ，则

$$
\boldsymbol {A} ^ {\mathrm{T}} \boldsymbol {A} = \left( \begin{array}{c} \boldsymbol {a} _ {1} ^ {\mathrm{T}} \\ \boldsymbol {a} _ {2} ^ {\mathrm{T}} \\ \vdots \\ \boldsymbol {a} _ {n} ^ {\mathrm{T}} \end{array} \right) (\boldsymbol {a} _ {1}, \boldsymbol {a} _ {2}, \dots , \boldsymbol {a} _ {n}) = \left( \begin{array}{c c c c} \boldsymbol {a} _ {1} ^ {\mathrm{T}} \boldsymbol {a} _ {1} & \boldsymbol {a} _ {1} ^ {\mathrm{T}} \boldsymbol {a} _ {2} & \dots & \boldsymbol {a} _ {1} ^ {\mathrm{T}} \boldsymbol {a} _ {n} \\ \boldsymbol {a} _ {2} ^ {\mathrm{T}} \boldsymbol {a} _ {1} & \boldsymbol {a} _ {2} ^ {\mathrm{T}} \boldsymbol {a} _ {2} & \dots & \boldsymbol {a} _ {2} ^ {\mathrm{T}} \boldsymbol {a} _ {n} \\ \vdots & \vdots & & \vdots \\ \boldsymbol {a} _ {n} ^ {\mathrm{T}} \boldsymbol {a} _ {1} & \boldsymbol {a} _ {n} ^ {\mathrm{T}} \boldsymbol {a} _ {2} & \dots & \boldsymbol {a} _ {n} ^ {\mathrm{T}} \boldsymbol {a} _ {n} \end{array} \right),
$$

即 $A^{\mathrm{T}}A$ 的 $(i,j)$ 元为 $\pmb{a}_i^{\mathrm{T}}\pmb{a}_j$ ，因 $A^{\mathrm{T}}A = O$ ，故

$$
\boldsymbol {a} _ {i} ^ {\mathrm{T}} \boldsymbol {a} _ {j} = 0 \quad (i, j = 1, 2, \dots , n),
$$

特殊地,有

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 今后列向量(列矩阵)常用小写黑体字母表示,如 a,α,x 等,而行向量(行矩阵)则用列向量的转置表示,如  $a^{T},\alpha^{T},x^{T}$  等.</span></small>

50

---

§5 矩阵分块法

$$
\boldsymbol {a} _ {j} ^ {\mathrm{T}} \boldsymbol {a} _ {j} = 0 \quad (j = 1, 2, \dots , n),
$$

而

$$
\boldsymbol {a} _ {j} ^ {\mathrm{T}} \boldsymbol {a} _ {j} = (  \boldsymbol {a} _ {1 j}, \boldsymbol {a} _ {2 j}, \dots , \boldsymbol {a} _ {m j}) \left( \begin{array}{c} \boldsymbol {a} _ {1 j} \\ \boldsymbol {a} _ {2 j} \\ \vdots \\ \boldsymbol {a} _ {m j} \end{array} \right) = \boldsymbol {a} _ {1 j} ^ {2} + \boldsymbol {a} _ {2 j} ^ {2} + \dots + \boldsymbol {a} _ {m j} ^ {2},
$$

由 $a_{1j}^{2} + a_{2j}^{2} + \dots +a_{mj}^{2} = 0$ ，再因 $a_{ij}$ 为实数，得

$$
a _ {1 j} = a _ {2 j} = \dots = a _ {m j} = 0 \quad (j = 1, 2, \dots , n),
$$

即

$$
A = 0.
$$

本例阐明了矩阵 $A$ 与方阵 $\mathbf{A}^{\mathrm{T}}\mathbf{A}$ 之间的一种关系. 特别地, 当 $A = a$ 为列向量时, 由于 $\mathbf{a}^{\mathrm{T}}\mathbf{a}$ 为 $1 \times 1$ 矩阵, 即 $\mathbf{a}^{\mathrm{T}}\mathbf{a}$ 是一个数, 这时, 本例的结论可叙述为: 列向量 $a = 0$ 的充分必要条件是 $\mathbf{a}^{\mathrm{T}}\mathbf{a} = 0$.

利用矩阵的按列(按行)分块,还可以给出线性方程组的另一矩阵表示形式.

重新回到线性方程组

$$
\left\{ \begin{array}{l} a _ {1 1} x _ {1} + a _ {1 2} x _ {2} + \dots + a _ {1 n} x _ {n} = b _ {1}, \\ a _ {2 1} x _ {1} + a _ {2 2} x _ {2} + \dots + a _ {2 n} x _ {n} = b _ {2}, \\ \dots \dots \\ a _ {m 1} x _ {1} + a _ {m 2} x _ {2} + \dots + a _ {m n} x _ {n} = b _ {m}, \end{array} \right. \tag {1}
$$

它的矩阵乘积形式为

$$
A _ {m \times n} x _ {n \times 1} = b _ {m \times 1}. \tag {$1^{\prime$}}
$$

若  $x_{1}=\xi_{11},x_{2}=\xi_{21},\cdots,x_{n}=\xi_{n1}$  为方程组(1)的解，则  $x=\xi=\begin{pmatrix}\xi_{11}\\ \xi_{21}\\\vdots\\\xi_{n1}\end{pmatrix}$  称为方程组( $1'$ )的解

向量.

(1') 式中, 把 A 按列分块, 把 x 按行分块, 由分块矩阵的乘法有

$$
(\boldsymbol {a} _ {1}, \boldsymbol {a} _ {2}, \dots , \boldsymbol {a} _ {n}) \left( \begin{array}{c} x _ {1} \\ x _ {2} \\ \vdots \\ x _ {n} \end{array} \right) = \boldsymbol {b},
$$

即

$$
x _ {1} \boldsymbol {a} _ {1} + x _ {2} \boldsymbol {a} _ {2} + \dots + x _ {n} \boldsymbol {a} _ {n} = \boldsymbol {b}. \tag {10}
$$

考研电子书网站:www.pdf2book.com

51

---

第 2 章 矩阵及其运算

其实把方程组(1)表示成

$$
\left( \begin{array}{c} a _ {1 1} \\ a _ {2 1} \\ \vdots \\ a _ {m 1} \end{array} \right) x _ {1} + \left( \begin{array}{c} a _ {1 2} \\ a _ {2 2} \\ \vdots \\ a _ {m 2} \end{array} \right) x _ {2} + \dots + \left( \begin{array}{c} a _ {1 n} \\ a _ {2 n} \\ \vdots \\ a _ {m n} \end{array} \right) x _ {n} = \left( \begin{array}{c} b _ {1} \\ b _ {2} \\ \vdots \\ b _ {m} \end{array} \right),
$$

也即是(10)式.

(1')和(10)是线性方程组(1)的两种变形.今后,它们与(1)将混同使用而不加区分,解与解向量亦不加区别.

## 习题二

1. 计算下列乘积:

(1) $\begin{pmatrix}4&3&1\\1&-2&3\\5&7&0\end{pmatrix}\begin{pmatrix}7\\2\\1\end{pmatrix};$

(2) (1,2,3) $\begin{pmatrix}3\\2\\1\end{pmatrix}$ ;

(3) $\begin{pmatrix}2\\1\\3\end{pmatrix}(-1,2);$

(4) $\begin{pmatrix}2&1&4&0\\1&-1&3&4\end{pmatrix}\begin{pmatrix}1&3&1\\0&-1&2\\1&-3&1\\4&0&-2\end{pmatrix};$

(5) \((x\_{1}, x\_{2}, x\_{3})\left( \begin{array}{ccc}a\_{11} & a\_{12} & a\_{13}\\ a\_{12} & a\_{22} & a\_{23}\\ a\_{13} & a\_{23} & a\_{33} \end{array} \right)\left( \begin{array}{c}x\_{1}\\ x\_{2}\\ x\_{3} \end{array} \right).\]

2. 设  $A = \begin{pmatrix} 1 & 1 & 1 \\ 1 & 1 & -1 \\ 1 & -1 & 1 \end{pmatrix}$ ,  $B = \begin{pmatrix} 1 & 2 & 3 \\ -1 & -2 & 4 \\ 0 & 5 & 1 \end{pmatrix}$ , 求 3AB - 2A 及  $A^{T}B$ .

3. 已知两个线性变换

$$
\left\{ \begin{array}{l} x _ {1} = 2 y _ {1} + y _ {3}, \\ x _ {2} = - 2 y _ {1} + 3 y _ {2} + 2 y _ {3}, \\ x _ {3} = 4 y _ {1} + y _ {2} + 5 y _ {3}, \end{array} \right. \quad \left\{ \begin{array}{l} y _ {1} = - 3 z _ {1} + z _ {2}, \\ y _ {2} = 2 z _ {1} + z _ {3}, \\ y _ {3} = - z _ {2} + 3 z _ {3}, \end{array} \right.
$$

求从  $z_{1}, z_{2}, z_{3}$  到  $x_{1}, x_{2}, x_{3}$  的线性变换.

4. 设  $A = \begin{pmatrix} 1 & 2 \\ 1 & 3 \end{pmatrix}$ ,  $B = \begin{pmatrix} 1 & 0 \\ 1 & 2 \end{pmatrix}$ , 问:

(1) AB = BA 吗?
(2) $(A+B)^{2}=A^{2}+2AB+B^{2}$  吗?
(3) $(A+B)(A-B)=A^{2}-B^{2}$  吗?

5. 举反例说明下列命题是错误的:

(1) 若  $A^{2}=O$ ，则 A=O；

52

---

习题二

(2) 若  $A^{2}=A$ ，则 A=O 或 A=E；
(3) 若 AX = AY，且  $A \neq O$ ，则 X = Y.

6. (1) 设  $A = \begin{pmatrix} 1 & 0 \\ \lambda & 1 \end{pmatrix}$ ，求  $A^{2}, A^{3}, \cdots, A^{k}$ ;

(2) 设  $A = \begin{pmatrix} \lambda & 1 & 0 \\ 0 & \lambda & 1 \\ 0 & 0 & \lambda \end{pmatrix}$ ，求  $A^{4}$ .

7. (1) 设  $A = \begin{pmatrix} 3 & 1 \\ 1 & -3 \end{pmatrix}$ ，求  $A^{50}$  和  $A^{51}$ ;

(2) 设  $a=\begin{pmatrix}2\\1\\-3\end{pmatrix},b=\begin{pmatrix}1\\2\\4\end{pmatrix},A=ab^{T},$  求  $A^{100}.$

8.（1）设 $A, B$ 为 $n$ 阶矩阵，且 $A$ 为对称矩阵，证明 $\pmb{B}^{\mathrm{T}}\pmb{AB}$ 也是对称矩阵；
(2) 设 A, B 都是 n 阶对称矩阵, 证明 AB 是对称矩阵的充分必要条件是 AB = BA;
(3) 设 A 为 n 阶方阵, 若满足  $A^{T} = -A$ , 即  $a_{ij} = -a_{ji}$  ( $i, j = 1, 2, \cdots, n$ ), 则称 A 为反对称矩阵 (亦称为反称矩阵). 设 A, B 都是 n 阶反对称矩阵, 证明 AB 是反对称矩阵的充分必要条件是 AB = -BA.

9. 求下列矩阵的逆矩阵:

(1) $\begin{pmatrix}1&2\\2&5\end{pmatrix};$

(2) $\begin{pmatrix}\cos\theta&-\sin\theta\\ \sin\theta&\cos\theta\end{pmatrix};$

(3) $\begin{pmatrix}1&2&-1\\3&4&-2\\5&-4&1\end{pmatrix};$

(4) $\begin{pmatrix}a_{1}&&0\\&a_{2}&\\&&\ddots\\0&&a_{n}\end{pmatrix}(a_{1}a_{2}\cdots a_{n}\neq0).$

10. 已知线性变换

$$
\left\{ \begin{array}{l} x _ {1} = 2 y _ {1} + 2 y _ {2} + y _ {3}, \\ x _ {2} = 3 y _ {1} + y _ {2} + 5 y _ {3}, \\ x _ {3} = 3 y _ {1} + 2 y _ {2} + 3 y _ {3}, \end{array} \right.
$$

求从变量 $x_{1}, x_{2}, x_{3}$ 到变量 $y_{1}, y_{2}, y_{3}$ 的线性变换.

11. 设 $J$ 是元素全为 1 的 $n (n \geqslant 2)$ 阶方阵. 证明 $E - J$ 是可逆方阵, 且 $(E - J)^{-1} = E - \frac{1}{n - 1} J$, 这里 $E$ 是与 $J$ 同阶的单位矩阵.

12. 设  $A^{k}=O$  (k 为正整数), 证明

$$
(E - A) ^ {- 1} = E + A + A ^ {2} + \dots + A ^ {k - 1}.
$$

13. 设方阵 $A$ 满足 $A^2 - A - 2E = O$，证明 $A$ 及 $A + 2E$ 都可逆，并求 $A^{-1}$ 及 $(A + 2E)^{-1}$.

14. 解下列矩阵方程:

(1) $\begin{pmatrix}2&5\\1&3\end{pmatrix}X=\begin{pmatrix}4&-6\\2&1\end{pmatrix};$
(2) $X\begin{pmatrix}2&1&-1\\2&1&0\\1&-1&1\end{pmatrix}=\begin{pmatrix}1&-1&3\\4&3&2\end{pmatrix};$

考研电子书网站:www.pdf2book.com

53

---

第2章 矩阵及其运算

(3) $\begin{pmatrix}1&4\\-1&2\end{pmatrix}X\begin{pmatrix}2&0\\-1&1\end{pmatrix}=\begin{pmatrix}3&1\\0&-1\end{pmatrix};$
(4) $AXB=C$, 其中 $A=\begin{pmatrix}2&1\\5&4\end{pmatrix}, B=\begin{pmatrix}1&3&3\\1&4&3\\1&3&4\end{pmatrix}, C=\begin{pmatrix}1&0&-1\\1&-2&0\end{pmatrix}.$

15. 分别应用克拉默法则和逆矩阵解下列线性方程组:

(1) $\left\{ \begin{array}{l}x_{1} + 2x_{2} + 3x_{3} = 1,\\ 2x_{1} + 2x_{2} + 5x_{3} = 2,\\ 3x_{1} + 5x_{2} + x_{3} = 3; \end{array} \right.$

(2) $\left\{ \begin{array}{l}x_{1} + x_{2} + x_{3} = 2,\\ x_{1} + 2x_{2} + 4x_{3} = 3,\\ x_{1} + 3x_{2} + 9x_{3} = 5. \end{array} \right.$

16. 设 $A$ 为3阶矩阵, $|A| = \frac{1}{2}$, 求 $|(2A)^{-1} - 5A^*$|.

17. 设  $A = \begin{pmatrix} 0 & 3 & 3 \\ 1 & 1 & 0 \\ -1 & 2 & 3 \end{pmatrix}$ ,  $A\dot{B} = A + 2B$ , 求 B.

18. 设  $A=\begin{pmatrix}1&0&1\\0&2&0\\1&0&1\end{pmatrix}$ ，且  $AB+E=A^{2}+B$ ，求 B.

19. 设 $A = \mathrm{diag}(1, -2, 1), A^{*}BA = 2BA - 8E$，求 $B$.

20. 已知矩阵 $A$ 的伴随矩阵 $A^{*} = \mathrm{diag}(1,1,1,8)$, 且 $ABA^{-1} = BA^{-1} + 3E$, 求 $B$.

21. 设 $P^{-1}AP = \Lambda$，其中 $P = \begin{pmatrix} -1 & -4 \\ 1 & 1 \end{pmatrix}, A = \begin{pmatrix} -1 & 0 \\ 0 & 2 \end{pmatrix}$，求 $A^{11}$.

22. 设 $AP = PA$，其中 $P = \begin{pmatrix} 1 & 1 & 1 \\ 1 & 0 & -2 \\ 1 & -1 & 1 \end{pmatrix}, A = \begin{pmatrix} -1 & & \\ & 1 & \\ & & 5 \end{pmatrix}$，求 $\varphi(A) = A^8(5E - 6A + A^2)$.

23. 设矩阵 $A$ 可逆, 证明其伴随矩阵 $A^{*}$ 也可逆, 且 $(A^{*})^{-1} = (A^{-1})^{*}$.

24. 设 $n$ 阶矩阵 $\pmb{A}$ 的伴随矩阵为 $\pmb{A}^{*}$, 证明:

(1) 若  $\left|A\right|=0$ ，则  $\left|A^{*}\right|=0$ ; (2)  $\left|A^{*}\right|=\left|A\right|^{n-1}$ .

25. 计算  $\begin{pmatrix}1&2&1&0\\0&1&0&1\\0&0&2&1\\0&0&0&3\end{pmatrix}\begin{pmatrix}1&0&3&1\\0&1&2&-1\\0&0&-2&3\\0&0&0&-3\end{pmatrix}.$
26. 设  $A = \begin{pmatrix} 3 & 4 & 0 & 0 \\ 4 & -3 & 0 & 0 \\ 0 & 0 & 2 & 0 \\ 0 & 0 & 2 & 2 \end{pmatrix}$ ，求  $|A^{8}|$  及  $A^{4}$ .
27. 设 $n$ 阶矩阵 $\mathbf{A}$ 及 $s$ 阶矩阵 $\mathbf{B}$ 都可逆, 求 $\begin{pmatrix} O & A \\ B & O \end{pmatrix}^{-1}$.

54

---

习题二

28. 求下列矩阵的逆矩阵:

(1) $\begin{pmatrix}5&2&0&0\\2&1&0&0\\0&0&8&3\\0&0&5&2\end{pmatrix};$

(2) $\begin{pmatrix}0&0&\frac{1}{5}\\2&1&0\\4&3&0\end{pmatrix}.$

![](raw/pages_0033-0064/images/page_58_image_4.jpg)

考研电子书网站:www.pdf2book.com

55

---

## 第3章

# 矩阵的初等变换与线性方程组

本章先引进矩阵的初等变换,建立矩阵的秩的概念,并利用初等变换讨论矩阵的秩的性质;然后利用矩阵的秩讨论线性方程组无解、有惟一解或有无限多解的充分必要条件,并介绍用初等变换解线性方程组的方法.

## § 1 矩阵的初等变换

矩阵的初等变换是矩阵的一种十分重要的运算,它在解线性方程组、求逆矩阵及矩阵理论的探讨中都可起重要的作用.为引进矩阵的初等变换,先来分析用消元法解线性方程组的例子.

引例 求解线性方程组

$$
\left\{ \begin{array}{l l} 2 x _ {1} - x _ {2} - x _ {3} + x _ {4} = 2, & ① \\ x _ {1} + x _ {2} - 2 x _ {3} + x _ {4} = 4, & ② \\ 4 x _ {1} - 6 x _ {2} + 2 x _ {3} - 2 x _ {4} = 4, & ③ \\ 3 x _ {1} + 6 x _ {2} - 9 x _ {3} + 7 x _ {4} = 9. & ④ \end{array} \right. \tag {1}
$$

解

$$
\text {①} \xrightarrow [ ③ \div 2 ]{\text {①} \leftrightarrow \text {②}} \left\{ \begin{array}{l l} x _ {1} + x _ {2} - 2 x _ {3} + x _ {4} = 4, & ① \\ 2 x _ {1} - x _ {2} - x _ {3} + x _ {4} = 2, & ② \\ 2 x _ {1} - 3 x _ {2} + x _ {3} - x _ {4} = 2, & ③ \\ 3 x _ {1} + 6 x _ {2} - 9 x _ {3} + 7 x _ {4} = 9 & ④ \end{array} \right. \tag {B_{1}}
$$

56

---

§ 1 矩阵的初等变换

$$
\xrightarrow [ ④ - 3 ① ]{\text {②} - ③} \left\{ \begin{array}{r l} x _ {1} & + x _ {2} - 2 x _ {3} + x _ {4} = 4, \\ & 2 x _ {2} - 2 x _ {3} + 2 x _ {4} = 0, \\ & - 5 x _ {2} + 5 x _ {3} - 3 x _ {4} = - 6, \\ & 3 x _ {2} - 3 x _ {3} + 4 x _ {4} = - 3 \end{array} \quad ① \right. \tag {B_{2}}
$$

$$
\xrightarrow [ \begin{array}{l} ③ + 5 ② \\ ④ - 3 ② \end{array} ]{\text {②} \times \frac {1}{2}} \left\{ \begin{array}{c l} x _ {1} + x _ {2} - 2 x _ {3} + x _ {4} = 4, & ① \\ x _ {2} - x _ {3} + x _ {4} = 0, & ② \\ 2 x _ {4} = - 6, & ③ \\ x _ {4} = - 3 & ④ \end{array} \right. \tag {B_{3}}
$$

$$
\xrightarrow [ ④ - 2 ③ ]{③ \leftrightarrow ④} \left\{ \begin{array}{c c} x _ {1} + x _ {2} - 2 x _ {3} + x _ {4} = 4, & ① \\ x _ {2} - x _ {3} + x _ {4} = 0, & ② \\ x _ {4} = - 3, & ③ \\ 0 = 0. & ④ \end{array} \right. \tag {B_{4}}
$$

这里，$(1) \rightarrow (B_{1})$ 是为消去 $x_{1}$ 作准备。$(B_{1}) \rightarrow (B_{2})$ 是保留①中的 $x_{1}$，消去②、③、④中的 $x_{1}. (B_{2}) \rightarrow (B_{3})$ 是保留②中的 $x_{2}$ 并把它的系数变为 1，然后消去③、④中的 $x_{2}$，在此同时恰好把 $x_{3}$ 也消去了。$(B_{3}) \rightarrow (B_{4})$ 是消去 $x_{4}$，在此同时恰好把常数也消去了，得到恒等式 $0 = 0$（若常数项不能消去，就将得到矛盾方程 $0 = 1$，则说明方程组无解）。至此消元完毕。

$(B_{4})$ 是4个未知数3个有效方程的方程组，应有一个自由未知数，由于方程组 $(B_{4})$ 呈阶梯形，可把每个台阶的第一个未知数（即 $x_{1}, x_{2}, x_{4}$ 选为非自由未知数，剩下的 $x_{3}$ 选为自由未知数。这样，就只需用“回代”的方法便能求出解:由③得 $x_{4} = -3$；将 $x_{4} = -3$ 代入②，得 $x_{2} = x_{3} + 3$；以 $x_{4} = -3, x_{2} = x_{3} + 3$ 代入①，得 $x_{1} = x_{3} + 4$。于是解得

$$
\left\{ \begin{array}{l} x _ {1} = x _ {3} + 4, \\ x _ {2} = x _ {3} + 3, \\ x _ {4} = - 3, \end{array} \right.
$$

其中 $x_{3}$ 可任意取值.或令 $x_{3} = c$ ，方程组的解可记作

$$
\boldsymbol {x} _ {i} = \left( \begin{array}{c} x _ {1} \\ x _ {2} \\ x _ {3} \\ x _ {4} \end{array} \right) = \left( \begin{array}{c} c + 4 \\ c + 3 \\ c \\ - 3 \end{array} \right),
$$

即

考研电子书网站:www.pdf2book.com

57

---

第3章 矩阵的初等变换与线性方程组

![](raw/pages_0033-0064/images/page_61_image_1.jpg)

自问自答

$$
\boldsymbol {x} = c \left( \begin{array}{c} 1 \\ 1 \\ 1 \\ 0 \end{array} \right) + \left( \begin{array}{c} 4 \\ 3 \\ 0 \\ - 3 \end{array} \right), \tag {2}
$$

其中 $c$ 为任意常数.

在上述消元过程中,始终把方程组看作一个整体,即不是着眼于某一个方程的变形,而是着眼于整个方程组变成另一个方程组.其中用到三种变换,即:(i)交换方程次序(①与②相互替换);(ii)以不等于0的数乘某个方程(以①×k替换①);(iii)一个方程加上另一个方程的k倍(以①+k②替换①).由于这三种变换都是可逆的,即

若 $(A)\xrightarrow{\textcircled{i}\leftrightarrow\textcircled{j}}(B)$ ，则 $(B)\xrightarrow{\textcircled{i}\leftrightarrow\textcircled{j}}(A)$ ;

若 $(A)\xrightarrow{\textcircled{i}\times k}(B)$ ，则 $(B)\xrightarrow{\textcircled{i}\times\frac{1}{k}}(A)$ ;

若 $(A)\xrightarrow{\textcircled{i}+k\textcircled{j}}(B)$ ，则 $(B)\xrightarrow{\textcircled{i}-k\textcircled{j}}(A)$ .

因此变换前的方程组与变换后的方程组是同解的,这三种变换都是方程组的同解变换,所以最后求得的解(2)是方程组(1)的全部解.

在上述变换过程中,实际上只对方程组的系数和常数项进行运算,未知数并未参与运算.因此,如果记方程组(1)的增广矩阵为

$$
\boldsymbol {B} = (\boldsymbol {A}, \boldsymbol {b}) = \left( \begin{array}{c c c c c} 2 & - 1 & - 1 & 1 & 2 \\ 1 & 1 & - 2 & 1 & 4 \\ 4 & - 6 & 2 & - 2 & 4 \\ 3 & 6 & - 9 & 7 & 9 \end{array} \right),
$$

那么上述对方程组的变换完全可以转换为对矩阵 B 的变换. 把方程组的上述三种同解变换移植到矩阵上, 就得到矩阵的三种初等行变换.

定义 1 下面三种变换称为矩阵的初等行变换:

(i) 对换两行(对换 i, j 两行, 记作  $r_{i} \leftrightarrow r_{j}$ );
(ii) 以数 $k (k \neq 0)$ 乘某一行中的所有元(第 $i$ 行乘 $k$, 记作 $r_i \times k$);
（iii）把某一行所有元的 $k$ 倍加到另一行对应的元上去(第 $j$ 行的 $k$ 倍加到第 $i$ 行上，记作 $r_i + kr_j$).

把定义中的“行”换成“列”，即得矩阵的初等列变换的定义（所用记号是把“r”换成“c”）.

矩阵的初等行变换与初等列变换,统称初等变换.

显然,三种初等变换都是可逆的,且其逆变换是同一类型的初等变换:变换  $r_{i} \leftrightarrow r_{j}$  的逆变换就是其本身;变换  $r_{i} \times k$  的逆变换为  $r_{i} \times \frac{1}{k}$  (或记作  $r_{i} \div k$ );变换  $r_{i} + kr_{j}$  的逆变

58

---

§ 1 矩阵的初等变换

换为 $r_i + (-k)r_j$ （或记作 $r_i - kr_j$）.

如果矩阵 $A$ 经有限次初等行变换变成矩阵 $\pmb{B}$, 就称矩阵 $\pmb{A}$ 与 $\pmb{B}$ 行等价, 记作 $A \stackrel{r}{\sim} B$; 如果矩阵 $A$ 经有限次初等列变换变成矩阵 $\pmb{B}$, 就称矩阵 $\pmb{A}$ 与 $\pmb{B}$ 列等价, 记作 $A \stackrel{c}{\sim} B$; 如果矩阵 $A$ 经有限次初等变换变成矩阵 $\pmb{B}$, 就称矩阵 $\pmb{A}$ 与 $\pmb{B}$ 等价, 记作 $A \sim B$.

矩阵之间的等价关系具有下列性质:

(i) 反身性 $A \sim A$;
(ii) 对称性 若 $A \sim B$, 则 $B \sim A$;
(iii) 传递性 若 $A \sim B, B \sim C$, 则 $A \sim C$.

下面用矩阵的初等行变换来解方程组(1)，其过程可与方程组(1)的消元过程一一对照:

$$
\begin{array}{l} \boldsymbol {B} = \left( \begin{array}{c c c c c} 2 & - 1 & - 1 & 1 & 2 \\ 1 & 1 & - 2 & 1 & 4 \\ 4 & - 6 & 2 & - 2 & 4 \\ 3 & 6 & - 9 & 7 & 9 \end{array} \right) \\ \overbrace {r _ {3} \times \frac {1}{2}} ^ {r _ {1} \leftrightarrow r _ {2}} \left( \begin{array}{c c c c c} 1 & 1 & - 2 & 1 & 4 \\ 2 & - 1 & - 1 & 1 & 2 \\ 2 & - 3 & 1 & - 1 & 2 \\ 3 & 6 & - 9 & 7 & 9 \end{array} \right) = \boldsymbol {B} _ {1} \\ \frac {r _ {2} - r _ {3}}{r _ {3} - 2 r _ {1}} \left( \begin{array}{c c c c c} 1 & 1 & - 2 & 1 & 4 \\ 0 & 2 & - 2 & 2 & 0 \\ 0 & - 5 & 5 & - 3 & - 6 \\ 0 & 3 & - 3 & 4 & - 3 \end{array} \right) = \boldsymbol {B} _ {2} \\ \frac {r _ {2} \times \frac {1}{2}}{r _ {4} - 3 r _ {2}} \left( \begin{array}{c c c c c} 1 & 1 & - 2 & 1 & 4 \\ 0 & 1 & - 1 & 1 & 0 \\ 0 & 0 & 0 & 2 & - 6 \\ 0 & 0 & 0 & 1 & - 3 \end{array} \right) = \boldsymbol {B} _ {3} \\ \underbrace {r _ {3} \leftrightarrow r _ {4}} _ {r _ {4} - 2 r _ {3}} \left( \begin{array}{c c c c c} 1 & 1 & - 2 & 1 & 4 \\ 0 & 1 & - 1 & 1 & 0 \\ 0 & 0 & 0 & 1 & - 3 \\ 0 & 0 & 0 & 0 & 0 \end{array} \right) = B _ {4}. \\ \end{array}
$$

由方程组 $(B_{4})$ 得到解(2)的回代过程，也可用矩阵的初等行变换来完成，即

$$
\boldsymbol {B} _ {4} \xrightarrow [ r _ {2} - r _ {3} ]{r _ {1} - r _ {2}} \left( \begin{array}{c c c c c} 1 & 0 & - 1 & 0 & 4 \\ 0 & 1 & - 1 & 0 & 3 \\ 0 & 0 & 0 & 1 & - 3 \\ 0 & 0 & 0 & 0 & 0 \end{array} \right) = \boldsymbol {B} _ {5},
$$

考研电子书网站:www.pdf2book.com

59

---

第3章 矩阵的初等变换与线性方程组

$B_{5}$  对应方程组

$$
\left\{ \begin{array}{l} x _ {1} - x _ {3} = 4, \\ x _ {2} - x _ {3} = 3, \\ x _ {4} = - 3, \end{array} \right.
$$

取 $x_{3}$ 为自由未知数，并令 $x_{3} = c$ ，即得

$$
\boldsymbol {x} = \left( \begin{array}{c} x _ {1} \\ x _ {2} \\ x _ {3} \\ x _ {4} \end{array} \right) = \left( \begin{array}{c} c + 4 \\ c + 3 \\ c \\ - 3 \end{array} \right) = c \left( \begin{array}{c} 1 \\ 1 \\ 1 \\ 0 \end{array} \right) + \left( \begin{array}{c} 4 \\ 3 \\ 0 \\ - 3 \end{array} \right), \tag {2}
$$

其中 $c$ 为任意常数.

矩阵 $B_{4}$ 和 $B_{5}$ 的特点是:都可画出一条从第一行某元左方的竖线开始到最后一列某元下方的横线结束的阶梯线,它的左下方的元全为0;每段竖线的高度为一行,竖线的右方的第一个元为非零元,称为该非零行的首非零元,简称首元.具有这样特点的矩阵称为行阶梯形矩阵.为明确起见给出如下定义:

定义 2 （1）非零矩阵若满足(i) 非零行在零行的上面；(ii) 非零行的首元所在列在上一行(如果存在的话)的首元所在列的右面, 则称此矩阵为行阶梯形矩阵;

(2) 若 A 是行阶梯形矩阵, 并且还满足: (i) 非零行的首元为 1; (ii) 首元所在的列的其他元均为 0, 则称 A 为行最简形矩阵.

于是 $B_{4}$ 和 $B_{5}$ 都是行阶梯形矩阵，且 $B_{5}$ 还是行最简形矩阵

用归纳法不难证明(这里不证):对于任何非零矩阵 $A_{m\times n}$ ，总可经有限次初等行变换把它变为行阶梯形矩阵和行最简形矩阵.

利用初等行变换,把一个矩阵化为行阶梯形矩阵和行最简形矩阵,是一种很重要的运算.由引例可知,要解线性方程组只需把增广矩阵化为行最简形矩阵.

由行最简形矩阵 $B_{5}$, 即可写出方程组的解 (2); 反之, 由方程组的解 (2) 也可写出矩阵 $B_{5}$. 由此可猜想到, 一个矩阵的行最简形矩阵是惟一确定的 (行阶梯形矩阵中非零行的行数也是惟一确定的).

对行最简形矩阵再施以初等列变换,可变成一种形状更简单的矩阵,称为标准形.例如

$$
\boldsymbol {B} _ {5} = \left( \begin{array}{c c c c c} 1 & 0 & - 1 & 0 & 4 \\ 0 & 1 & - 1 & 0 & 3 \\ 0 & 0 & 0 ^ {\prime} & 1 & - 3 \\ 0 & 0 & 0 & 0 & 0 \end{array} \right) \overbrace {c _ {5} - 4 c _ {1} - 3 c _ {2} + 3 c _ {3}} ^ {c _ {3} \leftrightarrow c _ {4}} \left( \begin{array}{c c c c c} 1 & 0 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 & 0 \\ 0 & 0 & 1 & 0 & 0 \\ 0 & 0 & 0 & 0 & 0 \end{array} \right) = \boldsymbol {F},
$$

矩阵 F 称为矩阵 B 的标准形, 其特点是: F 的左上角是一个单位矩阵, 其余元全为 0.

60

---

§ 1 矩阵的初等变换

对于 $m \times n$ 矩阵 $\mathbf{A}$, 总可经过初等变换把它化为标准形

$$
\boldsymbol {F} = \left( \begin{array}{c c} \boldsymbol {E} _ {r} & \boldsymbol {O} \\ \boldsymbol {O} & \boldsymbol {O} \end{array} \right) _ {m \times n},
$$

此标准形由 $m, n, r$ 三个数完全确定，其中 $r$ 就是行阶梯形矩阵中非零行的行数。所有与 $\pmb{A}$ 等价的矩阵组成一个集合，标准形 $\pmb{F}$ 是这个集合中形状最简单的矩阵。

矩阵的初等变换是矩阵的一种最基本的运算,为探讨它的应用,需要研究它的性质,下面介绍它的一个最基本的性质.

定理1 设 $A$ 与 $\pmb{B}$ 为 $m \times n$ 矩阵, 那么

(i)  $A \sim B$  的充分必要条件是存在 m 阶可逆矩阵 P, 使 PA = B;
(ii) $A \stackrel{c}{\sim} B$ 的充分必要条件是存在 $n$ 阶可逆矩阵 $Q$, 使 $AQ = B$;
(iii) $A \sim B$ 的充分必要条件是存在 $m$ 阶可逆矩阵 $P$ 及 $n$ 阶可逆矩阵 $Q$, 使 $PAQ = B$.

为证明定理1,我们引进初等矩阵的知识.

定义 3 由单位矩阵 E 经过一次初等变换得到的矩阵称为初等矩阵.

三种初等变换对应有三种初等矩阵.

(i) 把单位矩阵中第 $i, j$ 两行对换（或第 $i, j$ 两列对换），得初等矩阵

$$
\boldsymbol {E} (i, j) = \left( \begin{array}{c c c c c c c c} 1 & & & & & & \\ & \ddots & & & & & \\ & & 1 & & & & \\ & & 0 & \dots & 1 & & \\ & & & 1 & & \\ & & \vdots & \ddots & \vdots & \\ & & & & 1 & \\ & & 1 & \dots & 0 & \\ & & & & & 1 \\ & & & & & & \ddots \\ & & & & & & 1 \end{array} \right) \begin{array}{l} \leftarrow \text {第} i \text {行} \\ , \\ \leftarrow \text {第} j \text {行} \end{array}
$$

用 $m$ 阶初等矩阵 $\pmb{E}_m(i,j)$ 左乘矩阵 $\pmb {A} = (a_{ij})_{m\times n}$ ，得

$$
\boldsymbol {E} _ {m} (i, j) \boldsymbol {A} = \left( \begin{array}{c c c c} a _ {1 1} & a _ {1 2} & \dots & a _ {1 n} \\ \vdots & \vdots & & \vdots \\ a _ {j 1} & a _ {j 2} & \dots & a _ {j n} \\ \vdots & \vdots & & \vdots \\ a _ {i 1} ^ {\prime} & a _ {i 2} & \dots & a _ {i n} \\ \vdots & \vdots & & \vdots \\ a _ {m 1} & a _ {m 2} & \dots & a _ {m n} \end{array} \right) \xleftarrow {\text {第} i \text {行}}.
$$

考研电子书网站:www.pdf2book.com

61

---

第 3 章 矩阵的初等变换与线性方程组

其结果相当于对矩阵 $\pmb{A}$ 施行第一种初等行变换:把 $\pmb{A}$ 的第 $i$ 行与第 $j$ 行对换 $(r_i \leftrightarrow r_j)$. 类似地，以 $n$ 阶初等矩阵 $E_n(i, j)$ 右乘矩阵 $\pmb{A}$，其结果相当于对矩阵 $\pmb{A}$ 施行第一种初等列变换:把 $\pmb{A}$ 的第 $i$ 列与第 $j$ 列对换 $(c_i \leftrightarrow c_j)$.

(ii) 以数 $k (k \neq 0)$ 乘单位矩阵的第 $i$ 行（或第 $i$ 列），得初等矩阵

$$
\boldsymbol {E} (i (k)) = \left( \begin{array}{c c c c c c} 1 & & & & & \\ & \ddots & & & & \\ & & 1 & & & \\ & & & k & & \\ & & & & 1 & \\ & & & & & \ddots \\ & & & & & 1 \end{array} \right) \leftarrow \text {第} i \text {行},
$$

可以验知:以  $E_{m}(i(k))$  左乘矩阵 A, 其结果相当于以数 k 乘 A 的第 i 行  $(r_{i} \times k)$ ; 以  $E_{n}(i(k))$  右乘矩阵 A, 其结果相当于以数 k 乘 A 的第 i 列  $(c_{i} \times k)$ .

（iii）以 $k$ 乘单位矩阵的第 $j$ 行加到第 $i$ 行上或以 $k$ 乘单位矩阵的第 $i$ 列加到第 $j$ 列上，得初等矩阵

$$
E (i j (k)) = \left( \begin{array}{c c c c c c} 1 & & & & & \\ & \ddots & & & & \\ & & 1 & \dots & k & \\ & & & \ddots & \vdots & \\ & & & & 1 & \\ & & & & & \ddots \\ & & & & & 1 \end{array} \right) \xleftarrow {\text {第} i \text {行}} \xleftarrow {\text {第} j \text {行}}.
$$

可以验知:以  $E_{m}(ij(k))$  左乘矩阵 A, 其结果相当于把 A 的第 j 行乘 k 加到第 i 行上  $(r_{i}+kr_{j})$ ; 以  $E_{n}(ij(k))$  右乘矩阵 A, 其结果相当于把 A 的第 i 列乘 k 加到第 j 列上  $(c_{j}+kc_{i})$ .

归纳上面的讨论,可得

性质1 设 $A$ 是一个 $m \times n$ 矩阵, 对 $A$ 施行一次初等行变换, 相当于在 $A$ 的左边乘相应的 $m$ 阶初等矩阵; 对 $A$ 施行一次初等列变换, 相当于在 $A$ 的右边乘相应的 $n$ 阶初等矩阵.

$$
\begin{array}{r l} & {\text {显然初等矩阵都是可逆的,且其逆矩阵是同一类型的初等矩阵:} E (i, j) ^ {- 1} = E (i, j),} \\ & {E (i (k)) ^ {- 1} = E \left(i \left(\frac {1}{k}\right)\right), E (i j (k)) ^ {- 1} = E (i j (- k)).} \end{array}
$$

性质 2 方阵 A 可逆的充分必要条件是存在有限个初等矩阵  $P_{1}, P_{2}, \cdots, P_{l}$ ，使

$$
A = P _ {1} P _ {2} \dots P _ {l}.
$$

证 先证充分性. 设  $A=P_{1}P_{2}\cdots P_{l}$ ，因初等矩阵可逆，有限个可逆矩阵的乘积仍可逆. 故 A 可逆.

62

---

§1 矩阵的初等变换

再证必要性. 设 n 阶方阵 A 可逆, 它经有限次初等行变换成为行最简形矩阵 B. 由性质 1, 知有初等矩阵  $Q_{1}, Q_{2}, \cdots, Q_{l}$  使

$$
Q _ {1} \dots Q _ {2} Q _ {1} A = B.
$$

因 $A,Q_{1},Q_{2},\cdots,Q_{l}$ 均可逆,故B也可逆,从而B的非零行数为n,即B有n个首元1,但B总共只有n个列,故B=E.于是

$$
\boldsymbol {A} = \boldsymbol {Q} _ {1} ^ {- 1} \boldsymbol {Q} _ {2} ^ {- 1} \dots \boldsymbol {Q} _ {l} ^ {- 1} \boldsymbol {B} = \boldsymbol {Q} _ {1} ^ {- 1} \boldsymbol {Q} _ {2} ^ {- 1} \dots \boldsymbol {Q} _ {l} ^ {- 1} \boldsymbol {E} = \boldsymbol {Q} _ {1} ^ {- 1} \boldsymbol {Q} _ {2} ^ {- 1} \dots \boldsymbol {Q} _ {l} ^ {- 1} = \boldsymbol {P} _ {1} \boldsymbol {P} _ {2} \dots \boldsymbol {P} _ {l},
$$

这里  $P_{i}=Q_{i}^{-1}$  为初等矩阵, 即 A 是若干个初等矩阵的乘积.

证毕

下面应用初等矩阵的知识来证明定理1.

定理1的证明:

(i) 依据 $A \sim B$ 的定义和初等矩阵的性质, 有

$A \sim B \Leftrightarrow A$  经有限次初等行变换变成 B

$\Leftrightarrow$ 存在有限个 $m$ 阶初等矩阵 $\pmb{P}_1, \pmb{P}_2, \dots, \pmb{P}_l$, 使 $\pmb{P}_l \dots \pmb{P}_2 \pmb{P}_1 \pmb{A} = \pmb{B}$

$\Leftrightarrow$ 存在 $m$ 阶可逆矩阵 $\pmb{P}$, 使 $PA = B$.

类似可证明(ii)和(iii).

证毕

定理 1 把矩阵的初等变换与矩阵的乘法联系了起来,从而可以依据矩阵乘法的运算规律得到初等变换的运算规律,也可以利用矩阵的初等变换去研究矩阵的乘法.下面先给出定理 1 的一个推论,然后介绍一种利用初等变换求逆矩阵的方法.

推论 方阵 A 可逆的充分必要条件是  $A \sim E$ .

证 $A$ 可逆 $\Leftrightarrow$ 存在可逆矩阵 $P$, 使 $PA = E$

$$
\Leftrightarrow A \stackrel {r} {\sim} E.
$$

证毕

定理 1 表明, 如果  $A \sim B$ , 即 A 经一系列初等行变换变为 B, 则有可逆矩阵 P, 使 PA = B. 那么, 如何去求出这个可逆矩阵 P?

由于 $PA = B \Leftrightarrow \begin{cases} PA = B, \\ PE = P \end{cases} \Leftrightarrow P(A, E) = (B, P) \Leftrightarrow (A, E) \sim (B, P)$, 因此, 如果对矩阵 $(A, E)$ 作初等行变换, 那么当把 $A$ 变为 $B$ 时, $E$ 就变为 $P$. 于是就得到所求的可逆矩阵 $P$.

例1 设 $A = \begin{pmatrix} 2 & -1 & -1 \\ 1 & 1 & -2 \\ 4 & -6 & 2 \end{pmatrix}$ 的行最简形矩阵为 $F$, 求 $F$ 及一个可逆矩阵 $P$, 使 $PA = F$.

解 把 A 用初等行变换化成行最简形矩阵, 即为 F. 但需求出 P, 故按上段所述, 对  $(A, E)$  作初等行变换把 A 化成行最简形矩阵, 便同时得到 F 和 P. 运算如下:

考研电子书网站:www.pdf2book.com

63

---

第 3 章 矩阵的初等变换与线性方程组

$$
(\boldsymbol {A}, \boldsymbol {E}) = \left( \begin{array}{c c c c c c} 2 & - 1 & - 1 & 1 & 0 & 0 \\ 1 & 1 & - 2 & 0 & 1 & 0 \\ 4 & - 6 & 2 & 0 & 0 & 1 \end{array} \right) \xrightarrow [ r _ {2} - 2 r _ {1} ]{r _ {1} \leftrightarrow r _ {2}} \left( \begin{array}{c c c c c c} 1 & 1 & - 2 & 0 & 1 & 0 \\ 0 & - 3 & 3 & 1 & - 2 & 0 \\ 0 & - 4 & 4 & - 2 & 0 & 1 \end{array} \right)
$$

$$
\overbrace {r _ {3} + 4 r _ {2}} ^ {r _ {2} - r _ {3}} \left( \begin{array}{c c c c c c} 1 & 0 & - 1 & - 3 & 3 & 1 \\ 0 & 1 & - 1 & 3 & - 2 & - 1 \\ 0 & 0 & 0 & 1 0 & - 8 & - 3 \end{array} \right),
$$

故  $F=\begin{pmatrix}1&0&-1\\0&1&-1\\0&0&0\end{pmatrix}$  为 A 的行最简形矩阵, 而使 PA=F 的可逆矩阵

$$
\boldsymbol {P} = \left( \begin{array}{c c c} - 3 & 3 & 1 \\ . 3 & - 2 & - 1 \\ 1 0 & - 8 & - 3 \end{array} \right).
$$

注 上述解中所得 $(\pmb{F},\pmb{P})$ ，可继续作初等行变换 $r_3\times k,r_1 + kr_3,r_2 + kr_3$ ，则 $\pmb{F}$ 不变而$\pmb{P}$ 变.由此可知本例中使 $PA = F$ 的可逆矩阵 $\pmb{P}$ 不是惟一的.

例2 设 $A = \begin{pmatrix} 0 & -2 & 1 \\ 3 & 0 & -2 \\ -2 & 3 & 0 \end{pmatrix}$, 证明 $A$ 可逆, 并求 $A^{-1}$.

解 如同例1, 初等行变换把 $(A, E)$ 化成 $(F, P)$, 其中 $F$ 为 $A$ 的行最简形矩阵. 如果 $F = E$, 由定理1之推论知 $A$ 可逆, 并由 $PA = E$, 知 $P = A^{-1}$. 运算如下:

$$
\begin{array}{l} (A, E) = \left( \begin{array}{c c c c c c} 0 & - 2 & 1 & 1 & 0 & 0 \\ 3 & 0 & - 2 & 0 & 1 & 0 \\ - 2 & 3 & 0 & 0 & 0 & 1 \end{array} \right) \\ \underbrace {r _ {3} \times 3} _ {r _ {1} \leftrightarrow r _ {2}} \left( \begin{array}{c c c c c c} 3 & 0 & - 2 & 0 & 1 & 0 \\ 0 & - 2 & 1 & 1 & 0 & 0 \\ 0 & 9 & - 4 & 0 & 2 & 3 \end{array} \right) \underbrace {r _ {3} \times 2} _ {r _ {3} + 9 r _ {2}} \left( \begin{array}{c c c c c c} 3 & 0 & - 2 & 0 & 1 & 0 \\ 0 & - 2 & 1 & 1 & 0 & 0 \\ 0 & 0 & 1 & 9 & 4 & 6 \end{array} \right) \\ \overbrace {r _ {2} - r _ {3}} ^ {r _ {1} + 2 r _ {3}} \left( \begin{array}{c c c c c c} 3 & 0 & 0 & 1 8 & 9 & 1 2 \\ 0 & - 2 & 0 & - 8 & - 4 & - 6 \\ 0 & 0 & 1 & 9 & 4 & 6 \end{array} \right) \overbrace {r _ {2} \times \left(- \frac {1}{2}\right)} ^ {r _ {1} \times \frac {1}{3}} \left( \begin{array}{c c c c c c} 1 & 0 & 0 & 6 & 3 & 4 \\ 0 & 1 & 0 & 4 & 2 & 3 \\ 0 & 0 & 1 & 9 & 4 & 6 \end{array} \right), \\ \end{array}
$$

因 $A \sim^{r} E$，故 $A$ 可逆，且 $A^{-1} = \begin{pmatrix} 6 & 3 & 4 \\ 4 & 2 & 3 \\ 9 & 4 & 6 \end{pmatrix}$.

例3 求解矩阵方程 $AX = B$，其中 $A = \begin{pmatrix} 2 & 1 & -3 \\ 1 & 2 & -2 \\ -1 & 3 & 2 \end{pmatrix}, B = \begin{pmatrix} 1 & -1 \\ 2 & 0 \\ -2 & 5 \end{pmatrix}$.

64

---

§1 矩阵的初等变换

解 设可逆矩阵 P 使 PA = F 为行最简形矩阵, 则

$$
\boldsymbol {P} (\boldsymbol {A}, \boldsymbol {B}) = (\boldsymbol {F}, \boldsymbol {P B}),
$$

因此对矩阵 $(A, B)$ 作初等行变换把 $A$ 变为 $F$, 同时把 $B$ 变为 $PB$. 若 $F = E$, 则 $A$ 可逆, 且 $P = A^{-1}$, 这时所给方程有惟一解 $X = PB = A^{-1}B$. 由

$$
\begin{array}{l} (A, B) = \left( \begin{array}{c c c c c} 2 & 1 & - 3 & 1 & - 1 \\ 1 & 2 & - 2 & 2 & 0 \\ - 1 & 3 & 2 & - 2 & 5 \end{array} \right) \overset {r _ {1} \leftrightarrow r _ {2}} {\underset {r _ {3} + r _ {1}} {\overset {r _ {2} - 2 r _ {1}} {\longrightarrow}}} \left( \begin{array}{c c c c c} 1 & 2 & - 2 & 2 & 0 \\ 0 & - 3 & 1 & - 3 & - 1 \\ 0 & 5 & 0 & 0 & 5 \end{array} \right) \\ \underset {r _ {3} + 3 r _ {2}} {\overset {r _ {3} \leftrightarrow r _ {2}} {\longrightarrow}} \left( \begin{array}{c c c c c} 1 & 2 & - 2 & 2 & 0 \\ 0 & 1 & 0 & 0 & 1 \\ 0.. & 0 & 1 & - 3 & 2 \end{array} \right) \overset {r _ {1} - 2 r _ {2} + 2 r _ {3}} {\longrightarrow} \left( \begin{array}{c c c c c} 1 & 0 & 0 & - 4 & 2 \\ 0 & 1 & 0 & 0 & 1 \\ 0 & 0 & 1 & - 3 & 2 \end{array} \right), \\ \end{array}
$$

可见 $A \sim E$，因此 $A$ 可逆，且

$$
\boldsymbol {X} = \boldsymbol {A} ^ {- 1} \boldsymbol {B} = \left( \begin{array}{c c} - 4 & 2 \\ 0 & 1 \\ - 3 & 2 \end{array} \right)
$$

即为所给方程的惟一解.

例2和例3是一种用初等行变换求 $A^{-1}$ 或 $A^{-1}B$ 的方法，当 $\pmb{A}$ 为3阶或更高阶的矩阵时，求 $A^{-1}$ 或 $A^{-1}B$ 通常都用此方法.这是当 $\pmb{A}$ 为可逆矩阵时，求解方程$AX = B$ 的方法（求 $A^{-1}$ 也就是求方程 $AX = E$ 的解).这方法就是把方程 $AX = B$ 的增广矩阵 $(A,B)$ 化为行最简形矩阵，从而求得方程的解.特别地，求解线性方程组$Ax = b$ （ $A$ 为可逆矩阵）时把增广矩阵 $(A,b)$ 化为行最简形矩阵，其最后一列就是解向量，从而得到了一个求解线性方程组的新途径.

例4 求解线性方程组

$$
\left\{ \begin{array}{l l} x _ {1} - x _ {2} - x _ {3} = 2, \\ 2 x _ {1} - x _ {2} - 3 x _ {3} = 1, \\ 3 x _ {1} + 2 x _ {2} - 5 x _ {3} = 0. \end{array} \right.
$$

解 记此方程组为 Ax=b，则增广矩阵

$$
\begin{array}{l} (\boldsymbol {A}, \boldsymbol {b}) = \left( \begin{array}{c c c c} 1 & - 1 & - 1 & 2 \\ 2 & - 1 & - 3 & 1 \\ 3 & 2 & - 5 & 0 \end{array} \right) \xrightarrow [ r _ {3} - 3 r _ {1} ]{r _ {2} - 2 r _ {1}} \left( \begin{array}{c c c c} 1 & - 1 & - 1 & 2 \\ 0 & 1 & - 1 & - 3 \\ 0 & 5 & - 2 & - 6 \end{array} \right) \\ \begin{array}{c} \frac {r _ {1} + r _ {2}}{r _ {3} - 5 r _ {2}} \left( \begin{array}{c c c c} 1 & 0 & - 2 & - 1 \\ 0 & 1 & - 1 & - 3 \\ 0 & 0 & 1 & 3 \end{array} \right) \frac {r _ {1} + 2 r _ {3}}{r _ {2} + r _ {3}} \left( \begin{array}{c c c c} 1 & 0 & 0 & 5 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 1 & 3 \end{array} \right). \end{array} \\ \end{array}
$$

考研电子书网站:www.pdf2book.com

65

举一反三

图

---

第3章 矩阵的初等变换与线性方程组

因 $A \sim E$，故 $A$ 可逆，于是方程组有解，且解为

$$
\boldsymbol {x} = \boldsymbol {A} ^ {- 1} \boldsymbol {b} = \left( \begin{array}{c} 5 \\ 0 \\ 3 \end{array} \right).
$$

此方程组我们已在第2章例16中分别用克拉默法则和逆矩阵求解过.比较这三种方法,显然这里介绍的方法最为方便和快捷.

## § 2 矩阵的秩

为了更好地理解矩阵的秩的概念,重新讨论上节引例中增广矩阵 B 及其行阶梯形矩阵  $B_{4}$  和  $B_{5}$ :

$$
\boldsymbol {B} = \left( \begin{array}{c c c c c} 2 & - 1 & - 1 & 1 & 2 \\ 1 & 1 & - 2 & 1 & 4 \\ 4 & - 6 & 2 & - 2 & 4 \\ 3 & 6 & - 9 & 7 & 9 \end{array} \right) \stackrel {{r}} {{\sim}} \left( \begin{array}{c c c c c} 1 & 1 & - 2 & 1 & 4 \\ 0 & 1 & - 1 & 1 & 0 \\ 0 & 0 & 0 & 1 & - 3 \\ 0 & 0 & 0 & 0 & 0 \end{array} \right) = \boldsymbol {B} _ {4}
$$

$$
\sim \left( \begin{array}{c c c c c} 1 & 0 & - 1 & 0 & 4 \\ 0 & 1 & - 1 & 0 & 3 \\ 0 & 0 & 0 & 1 & - 3 \\ 0 & 0 & 0 & 0 & 0 \end{array} \right) = \boldsymbol {B} _ {5},
$$

我们发现 $B_{4}$ 和 $B_{5}$ 都恰好有3个非零行.自然要问:每一个与 $\pmb{B}$ 行等价的行阶梯形矩阵是否都恰好有3个非零行？回答是肯定的.为阐明这一问题先引入矩阵子式的概念

定义 4 在  $m \times n$  矩阵 A 中, 任取 k 行与 k 列  $(k \leqslant m, k \leqslant n)$ , 位于这些行列交叉处的  $k^{2}$  个元素, 不改变它们在 A 中所处的位置次序而得的 k 阶行列式, 称为矩阵 A 的 k 阶子式.

$m \times n$ 矩阵 A 的 k 阶子式共有 $C_{m}^{k} \cdot C_{n}^{k}$ 个. 公众号:旗胜考研

现在来观察行阶梯形矩阵 $B_{4}$ 的子式. 取 $B_{4}$ 的第1、第2、第3行和第1、第2、第4列, 得到三阶非零子式 $\left| \begin{array}{lll} 1 & 1 & 1 \\ 0 & 1 & 1 \\ 0 & 0 & 1 \end{array} \right|$; 而它的任一四阶子式都将因含有零行而成为0. 换言之, $B_{4}$ 中非零子式的最高阶数是3. 同样 $B_{5}$ 中非零子式的最高阶数也是3.

非零子式在矩阵的初等行变换中的意义可以表述成如下的引理:

引理 设 $A \sim B$，则 $A$ 与 $B$ 中非零子式的最高阶数相等.

证 先证 B 是 A 经过一次初等行变换而得的情形.

66

---

§2 矩阵的秩

设 $D$ 是 $\pmb{A}$ 中的 $r$ 阶非零子式. 当 $\pmb{A} \xrightarrow{r_i \leftrightarrow r_j} \pmb{B}$ 或 $\pmb{A} \xrightarrow{r_i \times k} \pmb{B}$ 时, 在 $\pmb{B}$ 中总能找到与 $D$ 相对应的 $r$ 阶子式 $D_1$, 由于 $D_1 = D$ 或 $D_1 = -D$ 或 $D_1 = kD$, 因此 $D_1 \neq 0$.

当 $A \xrightarrow{r_i + kr_j} B$ 时, 因为对于作变换 $r_i \leftrightarrow r_j$ 时结论成立, 所以只需考虑 $A \xrightarrow{r_1 + kr_2} B$ 这一特殊情形. 分两种情形讨论: ① $D$ 不包含 $A$ 的第 1 行, 这时 $D$ 也是 $B$ 的 $r$ 阶非零子式; ② $D$ 包含 $A$ 的第 1 行, 这时把 $B$ 中与 $D$ 对应的 $r$ 阶子式 $D_1$ 记作

$$
D _ {1} = \left| \begin{array}{c} r _ {1} + k r _ {2} \\ r _ {p} \\ \vdots \\ r _ {q} \end{array} \right| = \left| \begin{array}{c} r _ {1} \\ r _ {p} \\ \vdots \\ r _ {q} \end{array} \right| + k \left| \begin{array}{c} r _ {2} \\ r _ {p} \\ \vdots \\ r _ {q} \end{array} \right| = D + k D _ {2},
$$

若 $p = 2$ ，则 $D_{1} = D\neq 0$ ；若 $p\neq 2$ ，则 $D_{2}$ 也是 $\pmb{B}$ 的 $r$ 阶子式，由 $D_{1} - kD_{2} = D\neq 0$ ，知 $D_{1}$ 与 $D_{2}$ 不同时为0.总之， $\pmb{B}$ 中存在 $r$ 阶非零子式 $D_{1}$ 或 $D_{2}$

记 $\pmb{A}$ 和 $\pmb{B}$ 中非零子式的最高阶数分别为 $s$ 和 $t$, 那么上述表明 $s \leqslant t$. 因 $\pmb{A}$ 经一次初等行变换成为 $\pmb{B}, \pmb{B}$ 也就可经一次初等行变换成为 $\pmb{A}$, 故又有 $t \leqslant s$, 于是 $s = t$.

经一次初等行变换结论成立,即可知经有限次初等行变换结论也成立. 证毕

现在可以回答本节一开始提出的问题了.

设 $\pmb{C}$ 是任一与 $\pmb{B}$ 行等价的行阶梯形矩阵，由引理，$\pmb{C}$ 中非零子式的最高阶数应与 $B_{4}$ 中非零子式的最高阶数相同，即 $\pmb{C}$ 有且仅有3个非零行.

值得注意的是上面的讨论中,关心的并不是非零子式(作为行列式)本身,而是它的阶数,尤其是非零子式的最高阶数.由此给出矩阵的秩的定义:

定义5 设在矩阵 $\pmb{A}$ 中有一个不等于0的 $r$ 阶子式 $D$, 且所有 $r + 1$ 阶子式(如果存在的话)全等于0, 那么 $D$ 称为矩阵 $\pmb{A}$ 的最高阶非零子式, 数 $r$ 称为矩阵 $\pmb{A}$ 的秩, 记作 $R(\pmb{A})$. 规定零矩阵的秩等于0.

由行列式的性质可知, 在 A 中当所有  $r+1$  阶子式全等于 0 时, 所有高于  $r+1$  阶的子式也全等于 0, 因此把 r 阶非零子式称为最高阶非零子式, 而 A 的秩  $R(A)$  就是 A 的非零子式的最高阶数.

由于 $R(A)$ 是 $\pmb{A}$ 的非零子式的最高阶数，因此，若矩阵 $\pmb{A}$ 中有某个 $s$ 阶子式不为0，则 $R(A) \geqslant s$；若 $\pmb{A}$ 中所有 $t$ 阶子式全为0，则 $R(A) < t$.

显然, 若 A 为  $m \times n$  矩阵, 则  $0 \leqslant R(A) \leqslant \min\{m, n\}$ .

由于行列式与其转置行列式相等, 因此  $A^{T}$  的子式与 A 的子式对应相等, 从而  $R(A^{\mathrm{T}})=R(A)$ .

对于 $n$ 阶矩阵 $\pmb{A}$, 由于 $\pmb{A}$ 的 $n$ 阶子式只有一个 $|\pmb{A}|$, 故当 $|\pmb{A}| \neq 0$ 时 $R(\pmb{A}) = n$, 当 $|\pmb{A}| = 0$ 时 $R(\pmb{A}) < n$. 可见可逆矩阵的秩等于矩阵的阶数, 不可逆矩阵的秩小于矩阵的

考研电子书网站:www.pdf2book.com

67

---

第3章 矩阵的初等变换与线性方程组

阶数.因此，可逆矩阵又称满秩矩阵.

矩阵的初等变换作为一种运算,其深刻意义在于它不改变矩阵的秩,即有

定理2 若 $A \sim B$，则 $R(A) = R(B)$.

证 由引理, 只需证明 $\pmb{A}$ 经初等列变换变成 $\pmb{B}$ 的情形, 这时 $\pmb{A}^{\mathrm{T}}$ 经初等行变换变为 $\pmb{B}^{\mathrm{T}}$, 由引理知 $R(\pmb{A}^{\mathrm{T}}) = R(\pmb{B}^{\mathrm{T}})$, 又 $R(\pmb{A}) = R(\pmb{A}^{\mathrm{T}}), R(\pmb{B}) = R(\pmb{B}^{\mathrm{T}})$, 因此 $R(\pmb{A}) = R(\pmb{B})$.

总之,若 A 经有限次初等变换变为 B（即  $A \sim B$ ），则  $R(A) = R(B)$ . 证毕

由于 $A \sim B$ 的充分必要条件是有可逆矩阵 $P, Q$, 使 $PAQ = B$, 因此可得

推论 若可逆矩阵 P, Q 使 PAQ = B，则  $R(A) = R(B)$ .

对于一般的矩阵, 当行数与列数较高时, 按定义求秩是很麻烦的. 然而对于行阶梯形矩阵, 如前所示, 它的秩就等于非零行的行数, 一看便知毋需计算. 因此依据定理 2 把矩阵化为行阶梯形矩阵来求秩是方便而有效的方法.

例 5 求矩阵 A 和 B 的秩, 其中

$$
\boldsymbol {A} = \left( \begin{array}{c c c} 1 & 2 & 3 \\ 2 & 3 & - 5 \\ 4 & 7 & 1 \end{array} \right), \quad \boldsymbol {B} = \left( \begin{array}{c c c c c} 3 & 2 & 0 & 5 & 0 \\ 3 & - 2 & 3 & 6 & - 1 \\ 2 & 0 & 1 & 5 & - 3 \\ 1 & 6 & - 4 & - 1 & 4 \end{array} \right).
$$

解 在 A 中, 容易看出一个 2 阶子式  $\begin{vmatrix}1 & 2 \\ 2 & 3\end{vmatrix} \neq 0$ , A 的 3 阶子式只有一个  $|A|$ , 经计算可知  $|A| = 0$ , 因此  $R(A) = 2$ .

对 $\pmb{B}$ 作初等行变换变成行阶梯形矩阵

$$
\begin{array}{l} \boldsymbol {B} = \left( \begin{array}{c c c c c} 3 & 2 & 0 & 5 & 0 \\ 3 & - 2 & 3 & 6 & - 1 \\ 2 & 0 & 1 & 5 & - 3 \\ 1 & 6 & - 4 & - 1 & 4 \end{array} \right) \overbrace {\substack {r _ {3} - 2 r _ {1} \\ r _ {4} - 3 r _ {1}}} ^ {r _ {1} \leftrightarrow r _ {4}} \left( \begin{array}{c c c c c} 1 & 6 & - 4 & - 1 & 4 \\ 0 & - 4 & 3 & 1 & - 1 \\ 0 & - 1 2 & 9 & 7 & - 1 1 \\ 0 & - 1 6 & 1 2 & 8 & - 1 2 \end{array} \right) \\ \overbrace {r _ {4} - 4 r _ {2}} ^ {r _ {3} - 3 r _ {2}} \left( \begin{array}{c c c c c} 1 & 6 & - 4 & - 1 & 4 \\ 0 & - 4 & 3 & 1 & - 1 \\ 0 & 0 & 0 & 4 & - 8 \\ 0 & 0 & 0 & 4 & - 8 \end{array} \right) \stackrel {{r _ {4} - r _ {3}}} {{\sim}} \left( \begin{array}{c c c c c} 1 & 6 & - 4 & - 1 & 4 \\ 0 & - 4 & 3 & 1 & - 1 \\ 0 & 0 & 0 & 4 & - 8 \\ 0 & 0 & 0 & 0 & 0 \end{array} \right), \\ \end{array}
$$

因为行阶梯形矩阵有3个非零行,所以 $R(B)=3$ .

例6 设 $A = \begin{pmatrix} 1 & -2 & 2 & -1 \\ 2 & -4 & 8 & 0 \\ -2 & 4 & -2 & 3 \\ 3 & -6 & 0 & -6 \end{pmatrix}, b = \begin{pmatrix} 1 \\ 2 \\ 3 \\ 4 \end{pmatrix}$, 求矩阵 $A$ 及矩阵 $B = (A, b)$ 的秩.

68

---

§2 矩阵的秩

解 对 B 作初等行变换变为行阶梯形矩阵, 设 B 的行阶梯形矩阵为  $\widetilde{B} = (\widetilde{A}, \widetilde{b})$ , 则  $\widetilde{A}$  就是 A 的行阶梯形矩阵, 故从  $\widetilde{B} = (\widetilde{A}, \widetilde{b})$  中可同时看出  $R(A)$  及  $R(B)$ .

$$
\begin{array}{l} \boldsymbol {B} = \left( \begin{array}{c c c c c} 1 & - 2 & 2 & - 1 & 1 \\ 2 & - 4 & 8 & 0 & 2 \\ - 2 & 4 & - 2 & 3 & 3 \\ 3 & - 6 & 0 & - 6 & 4 \end{array} \right) \overbrace {r _ {4} - 3 r _ {1}} ^ {r _ {2} - 2 r _ {1}} \left( \begin{array}{c c c c c} 1 & - 2 & 2 & - 1 & 1 \\ 0 & 0 & 4 & 2 & 0 \\ 0 & 0 & 2 & 1 & 5 \\ 0 & 0 & - 6 & - 3 & 1 \end{array} \right) \\ \overbrace {r _ {4} + 3 r _ {2}} ^ {r _ {2} \times \frac {1}{2}} \left( \begin{array}{c c c c c} 1 & - 2 & 2 & - 1 & 1 \\ 0 & 0 & 2 & 1 & 0 \\ 0 & 0 & 0 & 0 & 5 \\ 0 & 0 & 0 & 0 & 1 \end{array} \right) \overbrace {r _ {4} - r _ {3}} ^ {r _ {3} \times \frac {1}{5}} \left( \begin{array}{c c c c c} 1 & - 2 & 2 & - 1 & 1 \\ 0 & 0 & 2 & 1 & 0 \\ 0 & 0 & 0 & 0 & 1 \\ 0 & 0 & 0 & 0 & 0 \end{array} \right), \\ \end{array}
$$

因此

$$
R (\boldsymbol {A}) = 2, R (\boldsymbol {B}) = 3.
$$

从矩阵 B 的行阶梯形矩阵可知, 本例中的 A 与 b 所对应的线性方程组 Ax=b 是无解的, 这是因为行阶梯形矩阵的第 3 行表示矛盾方程 0=1.

例7 设

$$
\boldsymbol {A} = \left( \begin{array}{c c c c} 1 & 2 & - 1 & 1 \\ 3 & 2 & \lambda & - 1 \\ 5 & 6 & 3 & \mu \end{array} \right),
$$

已知  $R(A)=2$ ，求  $\lambda$  与  $\mu$  的值.

解 $A \xrightarrow{r_2 - 3r_1} \begin{pmatrix} 1 & 2 & -1 & 1 \\ 0 & -4 & \lambda + 3 & -4 \\ 0 & -4 & 8 & \mu - 5 \end{pmatrix} \xrightarrow{r_3 - r_2} \begin{pmatrix} 1 & 2 & -1 & 1 \\ 0 & -4 & \lambda + 3 & -4 \\ 0 & 0 & 5 - \lambda & \mu - 1 \end{pmatrix},$

因 $R(A) = 2$ ，故

$$
\left\{ \begin{array}{l l} 5 - \lambda = 0, \\ \mu - 1 = 0, \end{array} \right. \quad \text {即} \quad \left\{ \begin{array}{l l} \lambda = 5, \\ \mu = 1. \end{array} \right.
$$

下面讨论矩阵的秩的性质.前面我们已经提出了矩阵秩的一些最基本的性质,归纳起来有

① $0 \leqslant R(A_{m \times n}) \leqslant \min \{m, n\}$.
②  $R(A^{\mathrm{T}})=R(A)$ .
③ 若 $A \sim B$，则 $R(A) = R(B)$.
④ 若 P, Q 可逆, 则  $R(PAQ) = R(A)$ .

下面再介绍几个常用的矩阵秩的性质:

⑤  $\max\left\{R(A), R(B)\right\} \leqslant R(A, B) \leqslant R(A) + R(B)$ ,

![](raw/pages_0065-0096/images/page_72_image_20.jpg)

考研电子书网站:www.pdf2book.com

69

---

第3章 矩阵的初等变换与线性方程组

特别地, 当 B=b 为非零列向量时, 有

$$
R (A) \leqslant R (A, b) \leqslant R (A) + 1.
$$

证 因为 $A$ 的最高阶非零子式总是 $(A, B)$ 的非零子式, 所以 $R(A) \leqslant R(A, B)$. 同理有 $R(B) \leqslant R(A, B)$. 两式合起来, 即为

$$
\max \left\{R (A), R (B) \right\} \leqslant R (A, B).
$$

设 $R(A) = r, R(B) = t$. 把 $A^{\mathrm{T}}$ 和 $B^{\mathrm{T}}$ 分别作初等行变换化为行阶梯形矩阵 $\widetilde{A}$ 和 $\widetilde{B}$. 因由性质 $2, R(A^{\mathrm{T}}) = r, R(B^{\mathrm{T}}) = t$, 故 $\widetilde{A}$ 和 $\widetilde{B}$ 中分别含 $r$ 个和 $t$ 个非零行, 从而 $\binom{\widetilde{A}}{\widetilde{B}}$ 中只含 $r + t$ 个非零行, 并且 $\binom{A^{\mathrm{T}}}{B^{\mathrm{T}}} \stackrel{r}{\sim} \binom{\widetilde{A}}{\widetilde{B}}$. 于是

$$
R (\boldsymbol {A}, \boldsymbol {B}) = R \binom{\boldsymbol {A} ^ {\mathrm{T}}}{\boldsymbol {B} ^ {\mathrm{T}}} ^ {\mathrm{T}} = R \binom{\boldsymbol {A} ^ {\mathrm{T}}}{\boldsymbol {B} ^ {\mathrm{T}}} = R \binom{\widetilde {\boldsymbol {A}}}{\widetilde {\boldsymbol {B}}} \leqslant r + t = R (\boldsymbol {A}) + R (\boldsymbol {B}). \quad \text {证毕}
$$

例如令

$$
\boldsymbol {A} = \left( \begin{array}{c c} 1 & 0 \\ 0 & 1 \\ 0 & 0 \end{array} \right), \quad \boldsymbol {B} = \left( \begin{array}{c} 0 \\ 0 \\ 1 \end{array} \right), \quad \boldsymbol {C} = \left( \begin{array}{c} 1 \\ 1 \\ 0 \end{array} \right),
$$

则

$$
\begin{array}{l} R (\boldsymbol {A}, \boldsymbol {B}) = R \left( \begin{array}{c c c} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{array} \right) = 3 = R (\boldsymbol {A}) + R (\boldsymbol {B}), \\ R (\boldsymbol {A}, \boldsymbol {C}) = R \left( \begin{array}{c c c} 1 & 0 & 1 \\ 0 & 1 & 1 \\ 0 & 0 & 0 \end{array} \right) = 2 <   R (\boldsymbol {A}) + R (\boldsymbol {C}). \\ \end{array}
$$

⑥  $R(A+B) \leqslant R(A) + R(B)$ .

证 不妨设 A, B 为  $n \times m$  矩阵. 对矩阵  $\begin{pmatrix} A + B \\ B \end{pmatrix}$  作初等行变换  $r_{i} - r_{n+i} \quad (i = 1, 2, \cdots, n)$  即得

$$
\binom {A + B} {B} \stackrel {{r}} {{\sim}} \binom {A} {B},
$$

于是

$$
R (\boldsymbol {A} + \boldsymbol {B}) \leqslant R \binom{\boldsymbol {A} + \boldsymbol {B}}{\boldsymbol {B}} = R \binom{\boldsymbol {A}}{\boldsymbol {B}} = R (\boldsymbol {A} ^ {\mathrm{T}}, \boldsymbol {B} ^ {\mathrm{T}}) ^ {\mathrm{T}} = R (\boldsymbol {A} ^ {\mathrm{T}}, \boldsymbol {B} ^ {\mathrm{T}})
$$

$$
\stackrel {\text {由⑤}} {\leqslant} R \left(\boldsymbol {A} ^ {\mathrm{T}}\right) + R \left(\boldsymbol {B} ^ {\mathrm{T}}\right) = R (\boldsymbol {A}) + R (\boldsymbol {B}). \quad \text {证毕}
$$

70

---

§3 线性方程组的解

后面我们还要介绍两条常用的性质,现先罗列于下:

⑦  $R(\boldsymbol{A}\boldsymbol{B}) \leqslant \min\{R(\boldsymbol{A}), R(\boldsymbol{B})\}$  (见下节定理7).
⑧ 若 $A_{m \times n} B_{n \times l} = O$，则 $R(A) + R(B) \leqslant n$（见下章例23）.

例 8 设 A 为 n 阶矩阵, 证明  $R(A+E)+R(A-E)\geqslant n$ .

证 因 $(A+E)+(E-A)=2E$ ，由性质⑥，有

$$
R (\boldsymbol {A} + \boldsymbol {E}) + R (\boldsymbol {E} - \boldsymbol {A}) \geqslant R (2 \boldsymbol {E}) = n,
$$

而 $R(\pmb {E} - \pmb {A}) = R(\pmb {A} - \pmb {E})$ ，所以

$$
R (A + E) + R (A - E) \geqslant n.
$$

例9 证明: 若 $A_{m \times n} B_{n \times l} = C$, 且 $R(A) = n$, 则 $R(B) = R(C)$.

证 因 $R(A) = n$，知 $A$ 的行最简形矩阵为 $\begin{pmatrix} E_n \\ O \end{pmatrix}_{m \times n}$，并有 $m$ 阶可逆矩阵 $P$，使 $PA = \begin{pmatrix} E_n \\ O \end{pmatrix}$. 于是

$$
P C = P A B = \binom{E _ {n}}{O} B = \binom{B}{O}.
$$

由矩阵秩的性质④, 知  $R(C)=R(PC)$ , 而  $R\begin{pmatrix}B\\O\end{pmatrix}=R(B)$ , 故

$$
R (\boldsymbol {C}) = R (\boldsymbol {B}).
$$

本例中的矩阵 A 的秩等于它的列数, 这样的矩阵称为列满秩矩阵. 类似地, 若矩阵 A 的秩等于它的行数, 就称它为行满秩矩阵. 当 A 为方阵时, 列满秩矩阵就成为满秩矩阵, 也就是可逆矩阵. 因此, 本例的结论当 A 为方阵这一特殊情形时就是矩阵秩的性质④.

本例另一种重要的特殊情形是 $C = O$ ，这时结论为

设 AB = O, 若 A 为列满秩矩阵, 则 B = O.

这是因为,按本例的结论,这时有  $R(B)=0$ , 故 B=O.

## § 3 线性方程组的解

设有 $n$ 个未知数 $m$ 个方程的线性方程组

$$
\left\{ \begin{array}{l} a _ {1 1} x _ {1} + a _ {1 2} x _ {2} + \dots + a _ {1 n} x _ {n} = b _ {1}, \\ a _ {2 1} x _ {1} + a _ {2 2} x _ {2} + \dots + a _ {2 n} x _ {n} = b _ {2}, \\ \dots \dots \\ a _ {m 1} x _ {1} + a _ {m 2} x _ {2} + \dots + a _ {m n} x _ {n} = b _ {m}, \end{array} \right. \tag {3}
$$

考研电子书网站:www.pdf2book.com

71

---

第 3 章 矩阵的初等变换与线性方程组

第2章中已经说明，(3)式可以写成以向量 $\pmb{x}$ 为未知元的形式

$$
\boldsymbol {A} \boldsymbol {x} = \boldsymbol {b}. \tag {4}
$$

线性方程组(3)如果有解,就称它是相容的;如果无解,就称它不相容.利用系数矩阵A和增广矩阵 $B=(A,b)$ 的秩,可以方便地讨论线性方程组是否有解(即是否相容)以及有解时解是否惟一等问题,其结论是

定理3 对 $n$ 元线性方程组(3)，即 $Ax = b$

(i) 无解的充分必要条件是  $R(A) < R(A, b)$ ;
(ii) 有惟一解的充分必要条件是  $R(A)=R(A,b)=n$ ;
(iii) 有无限多解的充分必要条件是  $R(A)=R(A,b)<n.$

证 只需证明条件的充分性, 因为 (i), (ii), (iii) 中条件的必要性依次是 (ii) (iii), (i) (iii), (i) (ii) 中条件的充分性的逆否命题.

设 $R(A) = r$ 为叙述方便，不妨设 $\pmb {B} = (\pmb {A},\pmb {b})$ 的行最简形矩阵为

$$
\widetilde {\boldsymbol {B}} = \left( \begin{array}{c c c c c c c c} 1 & 0 & \dots & 0 & b _ {1 1} & \dots & b _ {1, n - r} & d _ {1} \\ 0 & 1 & \dots & 0 & b _ {2 1} & \dots & b _ {2, n - r} & d _ {2} \\ \vdots & \vdots & & \vdots & \vdots & & \vdots & \vdots \\ 0 & 0 & \dots & 1 & b _ {r 1} & \dots & b _ {r, n - r} & d _ {r} \\ 0 & 0 & \dots & 0 & 0 & \dots & 0 & d _ {r + 1} \\ 0 & 0 & \dots & 0 & 0 & \dots & 0 & 0 \\ \vdots & \vdots & & \vdots & \vdots & & \vdots & \vdots \\ 0 & 0 & \dots & 0 & 0 & \dots & 0 & 0 \end{array} \right).
$$

(i) 若 $R(A) < R(B)$, 则 $\widetilde{B}$ 中的 $d_{r+1} = 1$, 于是 $\widetilde{B}$ 的第 $r+1$ 行对应矛盾方程 $0 = 1$, 故方程组(3)无解.
(ii) 若 $R(A) = R(B) = r = n$，则 $\widetilde{B}$ 中的 $d_{r+1} = 0$（或 $d_{r+1}$ 不出现），且 $b_{ij}$ 都不出现，于是 $\widetilde{B}$ 对应方程组

$$
\left\{ \begin{array}{l} x _ {1} = d _ {1}, \\ x _ {2} = d _ {2}, \\ \dots \dots \\ x _ {n} = d _ {n}, \end{array} \right.
$$

故方程组(3)有惟一解.

(iii) 若 $R(A) = R(B) = r < n$，则 $\widetilde{B}$ 中的 $d_{r+1} = 0$（或 $d_{r+1}$ 不出现），$\widetilde{B}$ 对应方程组

$$
\left\{ \begin{array}{l} x _ {1} = - b _ {1 1} x _ {r + 1} - \dots - b _ {1, n - r} x _ {n} + d _ {1}, \\ x _ {2} = - b _ {2 1} x _ {r + 1} - \dots - b _ {2, n - r} x _ {n} + d _ {2}, \\ \dots \dots \\ x _ {r} = - b _ {r 1} x _ {r + 1} - \dots - b _ {r, n - r} x _ {n} + d _ {r}, \end{array} \right. \tag {5}
$$

72

---

§3 线性方程组的解

令自由未知数  $x_{r+1}=c_{1},x_{r+2}=c_{2},\cdots,x_{n}=c_{n-r}$ ，即得方程组(3)的含 n-r 个参数的解

$$
\left( \begin{array}{c} x _ {1} \\ \vdots \\ x _ {r} \\ x _ {r + 1} \\ \vdots \\ x _ {n} \end{array} \right) = \left( \begin{array}{c} - b _ {1 1} c _ {1} - \dots - b _ {1, n - r} c _ {n - r} + d _ {1} \\ \vdots \\ - b _ {r 1} c _ {1} - \dots - b _ {r, n - r} c _ {n - r} + d _ {r} \\ c _ {1} \\ \vdots \\ c _ {n - r} \end{array} \right),
$$

即

$$
\left( \begin{array}{c} x _ {1} \\ \vdots \\ x _ {r} \\ x _ {r + 1} \\ \vdots \\ x _ {n} \end{array} \right) = c _ {1} \left( \begin{array}{c} - b _ {1 1} \\ \vdots \\ - b _ {r 1} \\ 1 \\ \vdots \\ 0 \end{array} \right) + \dots + c _ {n - r} \left( \begin{array}{c} - b _ {1, n - r} \\ \vdots \\ - b _ {r, n - r} \\ 0 \\ \vdots \\ 1 \end{array} \right) + \left( \begin{array}{c} d _ {1} \\ \vdots \\ d _ {r} \\ 0 \\ \vdots \\ 0 \end{array} \right), \tag {6}
$$

由于参数  $c_{1}, c_{2}, \cdots, c_{n-r}$  可任意取值，故方程组(3)有无限多解。此时，(6)式所对应的表达式即称为方程组(3)的通解。证毕

例10 求解齐次线性方程组

$$
\left\{ \begin{array}{l} x _ {1} + 2 x _ {2} + 2 x _ {3} + x _ {4} = 0, \\ 2 x _ {1} + x _ {2} - 2 x _ {3} - 2 x _ {4} = 0, \\ x _ {1} - x _ {2} - 4 x _ {3} - 3 x _ {4} = 0. \end{array} \right.
$$

解 对系数矩阵 A 施行初等行变换变为行最简形矩阵

$$
\begin{array}{l} \boldsymbol {A} = \left( \begin{array}{c c c c} 1 & 2 & 2 & 1 \\ 2 & 1 & - 2 & - 2 \\ 1 & - 1 & - 4 & - 3 \end{array} \right) \xrightarrow [ r _ {3} - r _ {1} ]{r _ {2} - 2 r _ {1}} \left( \begin{array}{c c c c} 1 & 2 & 2 & 1 \\ 0 & - 3 & - 6 & - 4 \\ 0 & - 3 & - 6 & - 4 \end{array} \right) \\ \overbrace {r _ {2} \times \left(- \frac {1}{3}\right)} ^ {r _ {3} - r _ {2}} \left( \begin{array}{c c c c} 1 & 2 & 2 & 1 \\ 0 & 1 & 2 & \frac {4}{3} \\ 0 & 0 & 0 & 0 \end{array} \right) \stackrel {r _ {1} - 2 r _ {2}} {\sim} \left( \begin{array}{c c c c} 1 & 0 & - 2 & - \frac {5}{3} \\ 0 & 1 & 2 & \frac {4}{3} \\ 0 & 0 & 0 & 0 \end{array} \right), \\ \end{array}
$$

即得与原方程组同解的方程组

$$
\left\{ \begin{array}{l} x _ {1} - 2 x _ {3} - \frac {5}{3} x _ {4} = 0, \\ x _ {2} + 2 x _ {3} + \frac {4}{3} x _ {4} = 0, \end{array} \right.
$$

由此即得

考研电子书网站:www.pdf2book.com

73

---

第 3 章 矩阵的初等变换与线性方程组

$$
\left\{ \begin{array}{l l} x _ {1} = 2 x _ {3} + \frac {5}{3} x _ {4}, \\ x _ {2} = - 2 x _ {3} - \frac {4}{3} x _ {4}. \end{array} \right. \quad (x _ {3}, x _ {4} \text {可任意取值}).
$$

令 $x_{3} = c_{1}, x_{4} = c_{2}$, 把它写成通常的参数形式

$$
\left\{ \begin{array}{l} x _ {1} = 2 c _ {1} + \frac {5}{3} c _ {2}, \\ x _ {2} = - 2 c _ {1} - \frac {4}{3} c _ {2}, \\ x _ {3} = c _ {1}, \\ x _ {4} = c _ {2}, \end{array} \right.
$$

其中 $c_{1}, c_{2}$ 为任意实数，或写成向量形式

$$
\left( \begin{array}{c} x _ {1} \\ x _ {2} \\ x _ {3} \\ x _ {4} \end{array} \right) = \left( \begin{array}{c} 2 c _ {1} + \frac {5}{3} c _ {2} \\ - 2 c _ {1} - \frac {4}{3} c _ {2} \\ c _ {1} \\ c _ {2} \end{array} \right) = c _ {1} \left( \begin{array}{c} 2 \\ - 2 \\ 1 \\ 0 \end{array} \right) + c _ {2} \left( \begin{array}{c} \frac {5}{3} \\ - \frac {4}{3} \\ 0 \\ 1 \end{array} \right) \quad (c _ {1}, c _ {2} \in \mathbb {R}).
$$

例11 求解非齐次线性方程组

$$
\left\{ \begin{array}{l} x _ {1} - 2 x _ {2} + 3 x _ {3} - x _ {4} = 1, \\ 3 x _ {1} - x _ {2} + 5 x _ {3} - 3 x _ {4} = 2, \\ 2 x _ {1} + x _ {2} + 2 x _ {3} - 2 x _ {4} = 3. \end{array} \right.
$$

解 对增广矩阵 $\pmb{B}$ 施行初等行变换

$$
\begin{array}{l} \boldsymbol {B} = \left( \begin{array}{c c c c c} 1 & - 2 & 3 & - 1 & 1 \\ 3 & - 1 & 5 & - 3 & . 2 \\ 2 & 1 & 2 & - 2 & 3 \end{array} \right) \\ \underset {r _ {3} - 2 r _ {1}} {\overset {r _ {2} - 3 r _ {1}} {\sim}} \left( \begin{array}{c c c c c} 1 & - 2 & 3 & - 1 & 1 \\ 0 & 5 & - 4 & 0 & - 1 \\ 0 & ^ \prime 5 & - 4 & 0 & 1 \end{array} \right) \overset {r _ {3} - r _ {2}} {\sim} \left( \begin{array}{c c c c c} 1 & - 2 & 3 & - 1 & 1 \\ 0 & 5 & - 4 & 0 & - 1 \\ 0 & 0 & 0 & 0 & 2 \end{array} \right), \\ \end{array}
$$

可见 $R(A) = 2, R(B) = 3$，故方程组无解.

例12 求解非齐次线性方程组

$$
\left\{ \begin{array}{l} x _ {1} + x _ {2} - 3 x _ {3} - x _ {4} = 1, \\ 3 x _ {1} - x _ {2} - 3 x _ {3} + 4 x _ {4} = 4, \\ x _ {1} + 5 x _ {2} - 9 x _ {3} - 8 x _ {4} = 0. \end{array} \right.
$$

74

---

§3 线性方程组的解

解 对增广矩阵 $\pmb{B}$ 施行初等行变换

$$
\boldsymbol {B} = \left( \begin{array}{r r r r r} 1 & 1 & - 3 & - 1 & 1 \\ 3 & - 1 & - 3 & 4 & 4 \\ 1 & 5 & - 9 & - 8 & 0 \end{array} \right) \overset {r _ {2} - 3 r _ {1}} {\underset {r _ {3} - r _ {1}} {\sim}} \left( \begin{array}{r r r r r} 1 & 1 & - 3 & - 1 & 1 \\ 0 & - 4 & 6 & 7 & 1 \\ 0 & 4 & - 6 & - 7 & - 1 \end{array} \right)
$$

$$
\overbrace {r _ {2} \times \left(- \frac {1}{4}\right)} ^ {r _ {3} + r _ {2}} \left( \begin{array}{c c c c c} 1 & 1 & - 3 & - 1 & 1 \\ 0 & 1 & - \frac {3}{2} & - \frac {7}{4} & - \frac {1}{4} \\ 0 & 0 & 0 & 0 & 0 \end{array} \right) \stackrel {{r _ {1} - r _ {2}}} {{\sim}} \left( \begin{array}{c c c c c} 1 & 0 & - \frac {3}{2} & \frac {3}{4} & \frac {5}{4} \\ 0 & 1 & - \frac {3}{2} & - \frac {7}{4} & - \frac {1}{4} \\ 0 & 0 & 0 & 0 & 0 \end{array} \right),
$$

即得

$$
\left\{ \begin{array}{l} x _ {1} = \frac {3}{2} x _ {3} - \frac {3}{4} x _ {4} + \frac {5}{4}, \\ x _ {2} = \frac {3}{2} x _ {3} + \frac {7}{4} x _ {4} - \frac {1}{4}, \\ x _ {3} = x _ {3}, \\ x _ {4} = x _ {4}, \end{array} \right.
$$

亦即

$$
\left( \begin{array}{c} x _ {1} \\ x _ {2} \\ x _ {3} \\ x _ {4} \end{array} \right) = c _ {1} \left( \begin{array}{c} \frac {3}{2} \\ \frac {3}{2} \\ 1 \\ 0 \end{array} \right) + c _ {2} \left( \begin{array}{c} - \frac {3}{4} \\ \frac {7}{4} \\ 0 \\ 1 \end{array} \right) + \left( \begin{array}{c} \frac {5}{4} \\ - \frac {1}{4} \\ 0 \\ 0 \end{array} \right) \quad (c _ {1}, c _ {2} \in \mathbb {R}).
$$

例13 设线性方程组

$$
\left\{ \begin{array}{c c c} (1 + \lambda) x _ {1} & + x _ {2} & + x _ {3} = 0, \\ x _ {1} + (1 + \lambda) x _ {2} & + x _ {3} = 3, \\ x _ {1} & + x _ {2} + (1 + \lambda) x _ {3} = \lambda , \end{array} \right.
$$

问 $\lambda$ 取何值时, 此方程组(1)有惟一解; (2)无解; (3)有无限多解? 并在有无限多解时求其通解.

解法 1 对增广矩阵  $\boldsymbol{B}=(\boldsymbol{A},\boldsymbol{b})$  作初等行变换把它变为行阶梯形矩阵,有

$$
\boldsymbol {B} = \left( \begin{array}{c c c c} 1 + \lambda & 1 & 1 & 0 \\ 1 & 1 + \lambda & 1 & 3 \\ 1 & 1 & 1 + \lambda & \lambda \end{array} \right) \stackrel {r _ {1} \leftrightarrow r _ {3}} {\sim} \left( \begin{array}{c c c c} 1 & 1 & 1 + \lambda & \lambda \\ 1 & 1 + \lambda & 1 & 3 \\ 1 + \lambda & 1 & 1 & 0 \end{array} \right)
$$

考研电子书网站:www.pdf2book.com

75

---

第3章 矩阵的初等变换与线性方程组

$$
\overbrace {r _ {3} - (1 + \lambda) r _ {1}} ^ {r _ {2} - r _ {1}} \left( \begin{array}{c c c c} 1 & 1 & 1 + \lambda & \lambda \\ 0 & \lambda & - \lambda & 3 - \lambda \\ 0 & - \lambda & - \lambda (2 + \lambda) & - \lambda (1 + \lambda) \end{array} \right)
$$

$$
\sim_ {r _ {3} + r _ {2}} \left( \begin{array}{c c c c} 1 & 1 & 1 + \lambda & \lambda \\ 0 & \lambda & - \lambda & 3 - \lambda \\ 0 & 0 & - \lambda (3 + \lambda) & (1 - \lambda) (3 + \lambda) \end{array} \right).
$$

(1) 当  $\lambda \neq 0$  且  $\lambda \neq -3$  时,  $R(A) = R(B) = 3$ , 方程组有惟一解;

(2) 当  $\lambda=0$  时,  $R(A)=1$ ,  $R(B)=2$ , 方程组无解;

(3) 当  $\lambda = -3$  时,  $R(A) = R(B) = 2$ , 方程组有无限多解, 这时

$$
\boldsymbol {B} \stackrel {{r}} {{\sim}} \left( \begin{array}{c c c c} 1 & 1 & - 2 & - 3 \\ 0 & - 3 & 3 & 6 \\ 0 & 0 & 0 & 0 \end{array} \right) \stackrel {{r}} {{\sim}} \left( \begin{array}{c c c c} 1 & 0 & - 1 & - 1 \\ 0 & 1 & - 1 & - 2 \\ 0 & 0 & 0 & 0 \end{array} \right),
$$

由此便得通解

$$
\left\{ \begin{array}{l l} x _ {1} = x _ {3} - 1, \\ x _ {2} = x _ {3} - 2 \end{array} \right. \quad (x _ {3} \text {可任意取值}),
$$

即

$$
\left( \begin{array}{c} x _ {1} \\ x _ {2} \\ x _ {3} \end{array} \right) = c \left( \begin{array}{c} 1 \\ 1 \\ 1 \end{array} \right) + \left( \begin{array}{c} - 1 \\ - 2 \\ 0 \end{array} \right) \quad (c \in \mathbb {R}).
$$

解法2 因系数矩阵 $A$ 为3阶方阵，故有 $R(A) \leqslant R(A, b)_{3 \times 4} \leqslant 3.$ 于是由定理3，知方程有惟一解的充分必要条件是 $A$ 的秩 $R(A) = 3$ ，即 $|A| \neq 0.$ 而

$$
\left| \boldsymbol {A} \right| = \left| \begin{array}{c c c} 1 + \lambda & 1 & 1 \\ 1 & 1 + \lambda & 1 \\ 1 & 1 & 1 + \lambda \end{array} \right| = (3 + \lambda) \left| \begin{array}{c c c} 1 & 1 & 1 \\ 1 & 1 + \lambda & 1 \\ 1 & 1 & 1 + \lambda \end{array} \right|
$$

$$
= (3 + \lambda) \left| \begin{array}{l l l} 1 & 1 & 1 \\ 0 & \lambda & 0 \\ 0 & 0 & \lambda \end{array} \right| = (3 + \lambda) \lambda^ {2},
$$

因此, 当  $\lambda \neq 0$  且  $\lambda \neq -3$  时, 方程组有惟一解.

当 $\lambda = 0$ 时，

$$
\boldsymbol {B} = \left( \begin{array}{c c c c} 1 & 1 & 1 & 0 \\ \dot {1} & 1 & 1 & 3 \\ 1 & 1 & 1 & 0 \end{array} \right) \sim \left( \begin{array}{c c c c} 1 & 1 & 1 & 0 \\ 0 & 0 & 0 & 1 \\ 0 & 0 & 0 & 0 \end{array} \right),
$$

知  $R(A)=1, R(B)=2$ ，故方程组无解.

76

---

§3 线性方程组的解

当 $\lambda = -3$ 时，

$$
\boldsymbol {B} = \left( \begin{array}{r r r r} - 2 & 1 & 1 & 0 \\ 1 & - 2 & 1 & 3 \\ 1 & 1 & - 2 & - 3 \end{array} \right) \stackrel {{r}} {{\sim}} \left( \begin{array}{r r r r} 1 & 0 & - 1 & - 1 \\ 0 & 1 & - 1 & - 2 \\ 0 & 0 & 0 & 0 \end{array} \right),
$$

知 $R(A) = R(B) = 2$ ，故方程组有无限多解，且通解为

$$
\left( \begin{array}{c} x _ {1} \\ x _ {2} \\ x _ {3} \end{array} \right) = c \left( \begin{array}{c} 1 \\ 1 \\ 1 \end{array} \right) + \left( \begin{array}{c} - 1 \\ - 2 \\ 0 \end{array} \right) \quad (c \in \mathbb {R}).
$$

比较解法1与解法2, 显见解法2较简单. 但解法2的方法只适用于系数矩阵为方阵的情形.

对含参数的矩阵作初等变换时,例如在本例中对矩阵 B 作初等变换时,由于  $\lambda + 1, \lambda + 3$  等因式可以等于 0,故不宜作诸如  $r_{2} - \frac{1}{\lambda + 1} r_{1}, r_{2} \times (\lambda + 1), r_{3} \times \frac{1}{\lambda + 3}$  这样的变换.如果作了这种变换,则需对  $\lambda + 1 = 0$  (或  $\lambda + 3 = 0$ ) 的情形另作讨论.因此,对含参数的矩阵作初等变换较不方便.

由定理3容易得出线性方程组理论中两个最基本的定理，这就是

定理4 $n$ 元齐次线性方程组 $Ax = 0$ 有非零解的充分必要条件是 $R(A) < n$.

定理5 线性方程组 $Ax = b$ 有解的充分必要条件是 $R(A) = R(A, b)$.

显然,定理 4 是定理 3(iii) 的特殊情形,而定理 5 就是定理 3(i).

为了下一章论述的需要,下面把定理5推广到矩阵方程.

定理6 矩阵方程 $AX = B$ 有解的充分必要条件是 $R(A) = R(A,B)$.

证 设 $\pmb{A}$ 为 $m \times n$ 矩阵, $\pmb{B}$ 为 $m \times l$ 矩阵, 则 $\pmb{X}$ 为 $n \times l$ 矩阵. 把 $\pmb{X}$ 和 $\pmb{B}$ 按列分块, 记为

$$
X = (X _ {1}, X _ {2}, \dots , X _ {l}), \quad B = (\beta_ {1}, \beta_ {2}, \dots , \beta_ {l}),
$$

则矩阵方程 $AX = B$ 等价于 $l$ 个方程

$$
\boldsymbol {A} \boldsymbol {X} _ {i} = \boldsymbol {\beta} _ {i} \quad (i = 1, 2, \dots , l).
$$

又, 设 $R(A) = r$, 且 $\pmb{A}$ 的行最简形矩阵为 $\widetilde{\pmb{A}}$, 则 $\widetilde{\pmb{A}}$ 有 $r$ 个非零行, 且 $\widetilde{\pmb{A}}$ 的后 $m - r$ 行全为零行. 再设

$$
(A, B) = (A, \boldsymbol {\beta} _ {1}, \boldsymbol {\beta} _ {2}, \dots , \boldsymbol {\beta} _ {l}) \stackrel {r} {\sim} (\widetilde {A}, \widetilde {\boldsymbol {\beta}} _ {1}, \widetilde {\boldsymbol {\beta}} _ {2}, \dots , \widetilde {\boldsymbol {\beta}} _ {l}),
$$

从而

$$
(A, \pmb {\beta} _ {i}) \stackrel {r} {\sim} (\widetilde {A}, \widetilde {\pmb {\beta}} _ {i}) \quad (i = 1, 2, \dots , l).
$$

由上述讨论并依据定理5,可得

$$
\begin{array}{l} A X = B \text {有解} \Leftrightarrow A X _ {i} = \beta_ {i} \text {有解} (i = 1, 2, \dots , l) \\ \Leftrightarrow R (\boldsymbol {A}, \boldsymbol {\beta} _ {i}) = R (\boldsymbol {A}) \quad (i = 1, 2, \dots , l) \\ \Leftrightarrow \tilde {\boldsymbol {\beta}} _ {i} \text {的后} m - r \text {个元全为零} (i = 1, 2, \dots , l) \\ \end{array}
$$

考研电子书网站:www.pdf2book.com

77

---

第 3 章 矩阵的初等变换与线性方程组

$$
\begin{array}{l} \Leftrightarrow \left(\tilde {\boldsymbol {\beta}} _ {1}, \tilde {\boldsymbol {\beta}} _ {2}, \dots , \tilde {\boldsymbol {\beta}} _ {l}\right) \text {的后} m - r \text {行全为零行} \\ \Leftrightarrow R (\boldsymbol {A}, \boldsymbol {B}) = r = R (\boldsymbol {A}). \\ \end{array}
$$

证毕

利用定理 6, 容易得出矩阵的秩的性质⑦, 即

定理7 设 $AB = C$ ，则 $R(C) \leqslant \min \{R(A), R(B)\}$.

证 因 $AB = C$ ，知矩阵方程 $AX = C$ 有解 $X = B$ ，于是据定理6有 $R(A) = R(A,C)$ .而 $R(C)\leqslant R(A,C)$ ，因此 $R(C)\leqslant R(A)$

又  $B^{T}A^{T}=C^{T}$ ，由上段证明知有  $R(C^{T})\leqslant R(B^{T})$ ，即  $R(C)\leqslant R(B)$ .

综合便得  $R(C) \leqslant \min\{R(A), R(B)\}$ .

证毕

定理 6 和定理 7 的应用, 我们在下一章中讨论.

## 习题三

1. 用初等行变换把下列矩阵化为行最简形矩阵:

(1) $\begin{pmatrix}1&0&2&-1\\2&0&3&1\\3&0&4&3\end{pmatrix};$

(2) $\begin{pmatrix}0&2&-3&1\\0&3&-4&3\\0&4&-7&-1\end{pmatrix};$

(3) $\begin{pmatrix}1&-1&3&-4&3\\3&-3&5&-4&1\\2&-2&3&-2&0\\3&-3&4&-2&-1\end{pmatrix};$

(4) $\begin{pmatrix}2&3&1&-3&-7\\1&2&0&-2&-4\\3&-2&8&3&0\\2&-3&7&4&3\end{pmatrix}.$

2. 设 $A = \begin{pmatrix} 1 & 2 & 3 & 4 \\ 2 & 3 & 4 & 5 \\ 5 & 4 & 3 & 2 \end{pmatrix}$, 求一个可逆矩阵 $P$, 使 $PA$ 为行最简形矩阵.
3. 设  $A = \begin{pmatrix} -5 & 3 & 1 \\ 2 & -1 & 1 \end{pmatrix}$ ，求:

(1) 可逆矩阵 P, 使 PA 为行最简形矩阵;
(2) 一个可逆矩阵 Q, 使  $QA^{T}$  为行最简形矩阵.

4. 试利用矩阵的初等变换, 求下列方阵的逆矩阵:

(1) $\begin{pmatrix}3&2&1\\3&1&5\\3&2&3\end{pmatrix};$

(2) $\begin{pmatrix}3&-2&0&-1\\0&2&2&1\\1&-2&-3&-2\\0&1&2&1\end{pmatrix}.$

5. 试利用矩阵的初等行变换, 求解第 2 章习题二第 15 题之(2).

78

---

习题三

6.(1) 设  $A=\begin{pmatrix}4&1&-2\\ 2&2&1\\ 3&1&-1\end{pmatrix}, B=\begin{pmatrix}1&-3\\ 2&2\\ 3&-1\end{pmatrix}$ ，求 X 使 AX=B;

(2) 设  $A=\begin{pmatrix}0&2&1\\2&-1&3\\-3&3&-4\end{pmatrix}, B=\begin{pmatrix}1&2&3\\2&-3&1\end{pmatrix}$ ，求 X 使 XA=B;

(3) 设  $A=\begin{pmatrix}1&-1&0\\0&1&-1\\-1&0&1\end{pmatrix},AX=2X+A$ , 求 X.

7. 在秩是 $r$ 的矩阵中, 有没有等于0的 $r - 1$ 阶子式? 有没有等于0的 $r$ 阶子式?

8. 从矩阵 A 中划去一行得到矩阵 B, 问 A, B 的秩的关系怎样?

9. 求作一个秩是 4 的方阵, 它有 2 行是

$$
(1, 0, 1, 0, 0), (1, - 1, 0, 0, 0).
$$

10. 求下列矩阵的秩:

(1) $\begin{pmatrix}3&1&0&2\\1&-1&2&-1\\1&3&-4&4\end{pmatrix};$  (2) $\begin{pmatrix}3&2&-1&-3&-1\\2&-1&3&1&-3\\7&0&5&-1&-8\end{pmatrix};$  (3) $\begin{pmatrix}2&1&8&3&7\\2&-3&0&7&-5\\3&-2&5&8&0\\1&0&3&2&0\end{pmatrix}.$

11. 设 $A, B$ 都是 $m \times n$ 矩阵, 证明 $A \sim B$ 的充分必要条件是 $R(A) = R(B)$.

12. 设  $A=\begin{pmatrix}1&-2&3k\\-1&2k&-3\\k&-2&3\end{pmatrix}$ ，问 k 为何值，可使

(1)  $R(A)=1;$  (2)  $R(A)=2;$  (3)  $R(A)=3.$

13. 讨论 n 阶  $(n \geqslant 2)$  方阵  $A = \begin{pmatrix} a & b & \cdots & b \\ b & a & \cdots & b \\ \vdots & \vdots & & \vdots \\ b & b & \cdots & a \end{pmatrix}$  的秩的情况.

14. 求解下列齐次线性方程组:

(1) $\left\{ \begin{array}{l}x_{1} + x_{2} + 2x_{3} - x_{4} = 0,\\ 2x_{1} + x_{2} + x_{3} - x_{4} = 0,\\ 2x_{1} + 2x_{2} + x_{3} + 2x_{4} = 0; \end{array} \right.$ (2) $\left\{ \begin{array}{l}x_{1} + 2x_{2} + x_{3} - x_{4} = 0,\\ 3x_{1} + 6x_{2} - x_{3} - 3x_{4} = 0,\\ 5x_{1} + 10x_{2} + x_{3} - 5x_{4} = 0; \end{array} \right.$ (3) $\left\{ \begin{array}{l}2x_{1} + 3x_{2} - x_{3} - 7x_{4} = 0,\\ 3x_{1} + x_{2} + 2x_{3} - 7x_{4} = 0,\\ 4x_{1} + x_{2} - 3x_{3} + 6x_{4} = 0,\\ x_{1} - 2x_{2} + 5x_{3} - 5x_{4} = 0; \end{array} \right.$ (4) $\left\{ \begin{array}{l}3x_{1} + 4x_{2} - 5x_{3} + 7x_{4} = 0,\\ 2x_{1} - 3x_{2} + 3x_{3} - 2x_{4} = 0,\\ 4x_{1} + 11x_{2} - 13x_{3} + 16x_{4} = 0,\\ 7x_{1} - 2x_{2} + x_{3} + 3x_{4} = 0. \end{array} \right.$

15. 求解下列非齐次线性方程组:

考研电子书网站:www.pdf2book.com

79

---

第3章 矩阵的初等变换与线性方程组

(1) $\left\{ \begin{array}{l}4x_{1} + 2x_{2} - x_{3} = 2,\\ 3x_{1} - x_{2} + 2x_{3} = 10,\\ 11x_{1} + 3x_{2} = 8; \end{array} \right.$

(2) $\left\{\begin{aligned}&2x+3y+z=4,\\&x-2y+4z=-5,\\&3x+8y-2z=13,\\&4x-y+9z=-6;\end{aligned}\right.$

(3) $\left\{\begin{aligned}&2x+y-z+w=1,\\ &4x+2y-2z+w=2,\\ &2x+y-z-w=1;\end{aligned}\right.$

(4) $\left\{\begin{aligned}&2x+y-z+w=1,\\ &3x-2y+z-3w=4,\\ &x+4y-3z+5w=-2.\end{aligned}\right.$

16. 写出一个以

$$
\boldsymbol {x} = c _ {1} \left( \begin{array}{r} 2 \\ - 3 \\ 1 \\ 0 \end{array} \right) + c _ {2} \left( \begin{array}{r} - 2 \\ 4 \\ 0 \\ 1 \end{array} \right)
$$

为通解的齐次线性方程组.

17. 设有线性方程组

$$
\left( \begin{array}{c c c} 1 & \lambda - 1 & - 2 \\ 0 & \lambda - 2 & \lambda + 1 \\ 0 & 0 & 2 \lambda + 1 \end{array} \right) \left( \begin{array}{c} x _ {1} \\ x _ {2} \\ x _ {3} \end{array} \right) = \left( \begin{array}{c} 1 \\ 3 \\ 5 \end{array} \right),
$$

问  $\lambda$  为何值时(1)有惟一解;(2)无解;(3)有无限多解?并在有无限多解时求其通解.

18.  $\lambda$  取何值时, 非齐次线性方程组

$$
\left\{ \begin{array}{l} \lambda x _ {1} + x _ {2} + x _ {3} = 1, \\ x _ {1} + \lambda x _ {2} + x _ {3} = \lambda , \\ x _ {1} + x _ {2} + \lambda x _ {3} = \lambda^ {2} \end{array} \right.
$$

(1) 有惟一解；(2) 无解；(3) 有无限多解？并在有无限多解时求其通解.

19. 非齐次线性方程组

$$
\left\{ \begin{array}{r l} - 2 x _ {1} + x _ {2} + x _ {3} = - 2, \\ x _ {1} - 2 x _ {2} + x _ {3} = \lambda , \\ x _ {1} + x _ {2} - 2 x _ {3} = \lambda^ {2} \end{array} \right.
$$

当 $\lambda$ 取何值时有解？并求出它的通解.公众号:旗胜考研

20. 设

$$
\left\{ \begin{array}{c c c} (2 - \lambda) x _ {1} + & 2 x _ {2} - & 2 x _ {3} = \quad 1, \\ 2 x _ {1} + (5 - \lambda) x _ {2} - & 4 x _ {3} = \quad 2, \\ - 2 x _ {1} - & 4 x _ {2} + (5 - \lambda) x _ {3} = - \lambda - 1, \end{array} \right.
$$

问 $\lambda$ 为何值时, 此方程组有惟一解、无解或有无限多解? 并在有无限多解时求其通解.

21. 证明 $R(A) = 1$ 的充分必要条件是存在非零列向量 $\pmb{a}$ 及非零行向量 $\pmb{b}^{\mathrm{T}}$, 使 $A = ab^{\mathrm{T}}$.
22. 证明秩为 $r (r \geqslant 1)$ 的矩阵 $\mathbf{A}$ 可表示为 $r$ 个秩为 1 的矩阵之和.
23. 设 A 为列满秩矩阵, AB = C, 证明线性方程 Bx = 0 与 Cx = 0 同解.

80

---

习题三

24. 设 A 为  $m \times n$  矩阵, 证明方程  $AX = E_{m}$  有解的充分必要条件是  $R(A) = m$ .

![](raw/pages_0065-0096/images/page_84_image_2.jpg)

考研电子书网站:www.pdf2book.com

81

---

The quick brown fox jumps over the lazy dog.

# 第4章

# 向量组的线性相关性

![](raw/pages_0065-0096/images/page_85_image_3.jpg)

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

![](raw/pages_0097-0128/images/page_116_image_20.jpg)

考研电子书网站:www.pdf2book.com

113

---

The quick brown fox jumps over the lazy dog.

# 第5章

# 相似矩阵及二次型

本章主要讨论方阵的特征值与特征向量、方阵的相似对角化和二次型的化简等问题.

## § 1 向量的内积、长度及正交性

定义1 设有 $n$ 维向量

$$
\boldsymbol {x} = \left( \begin{array}{c} x _ {1} \\ x _ {2} \\ \vdots \\ x _ {n} \end{array} \right), \quad \boldsymbol {y} = \left( \begin{array}{c} y _ {1} \\ y _ {2} \\ \vdots \\ y _ {n} \end{array} \right),
$$

令

$$
(x, y) = x _ {1} y _ {1} + x _ {2} y _ {2} + \dots + x _ {n} y _ {n},
$$

$(x,y)$ 称为向量 $x$ 与 $y$ 的内积.

内积是两个向量之间的一种运算,其结果是一个实数,用矩阵记号表示,当 x 与 y 都是列向量时,有

$$
(x, y) = x ^ {T} y.
$$

内积具有下列性质(其中 x,y,z 为 n 维向量, $\lambda$  为实数):

(i)  $(x,y)=(y,x)$ ,
(ii)  $(\lambda x, y) = \lambda(x, y)$ ,
(iii)  $(x+y,z)=(x,z)+\left(\dot{y},z\right)$ ,
(iv) 当 x=0 时, $(x,x)=0$ ; 当  $x\neq0$  时, $(x,x)>0$ .

这些性质可根据内积定义直接证明,请读者给出相关证明.利用这些性质,还可证

114

---

§ 1 向量的内积、长度及正交性

明施瓦茨(Schwarz)不等式(这里不证)

$$
(x, y) ^ {2} \leqslant (x, x) (y, y).
$$

在解析几何中,我们曾引进向量的数量积

$$
\boldsymbol {x} \cdot \boldsymbol {y} = | \boldsymbol {x} | | \boldsymbol {y} | \cos \theta ,
$$

且在直角坐标系中,有数量积的计算公式

$$
(x _ {1}, x _ {2}, x _ {3}) \cdot (y _ {1}, y _ {2}, y _ {3}) = x _ {1} y _ {1} + x _ {2} y _ {2} + x _ {3} y _ {3},
$$

$n$ 维向量的内积是数量积的一种推广, 但 $n$ 维向量没有 3 维向量那样直观的长度和夹角的概念, 因此只能按数量积的直角坐标计算公式来推广. 并且反过来, 利用内积来定义 $n$ 维向量的长度和夹角.

定义2 令

$$
\| x \| = \sqrt {(x , x)} = \sqrt {x _ {1} ^ {2} + x _ {2} ^ {2} + \cdots + x _ {n} ^ {2}},
$$

$\| x\|$ 称为 $n$ 维向量 $\pmb{x}$ 的长度（或范数）.

向量的长度具有下述性质:

(i) 非负性 当 $x \neq 0$ 时, $\| x \| > 0$; 当 $x = 0$ 时, $\| x \| = 0$,
(ii) 齐次性  $\|\lambda x\| = |\lambda| \|x\|$ ,

可见这里所定义的向量长度具有解析几何中向量长度的基本属性.

当 $\| x\| = 1$ 时，称 $x$ 为单位向量.若 $a\neq 0$ ，取 $x = \frac{1}{\|a\|} a$ ，则 $x$ 是一个单位向量.由向量 $a$ 得到 $x$ 的过程称为把向量 $a$ 单位化

由施瓦茨不等式,有

$$
- 1 \leqslant \frac {(x , y)}{\| x \| \| y \|} \leqslant 1 \quad (\text {当} \| x \| \| y \| \neq 0 \text {时}),
$$

于是有下面的定义:

当 $x \neq 0, y \neq 0$ 时，

$$
\theta = \arccos \frac {(x , y)}{\| x \| \| y \|}
$$

称为 n 维向量 x 与 y 的夹角.

当 $(x,y)=0$ 时,称向量x与y正交.显然,零向量与任何向量都正交.

所谓正交向量组,是指一组两两正交的非零向量.下面讨论正交向量组的性质:

定理 1 若 n 维向量  $a_{1}, a_{2}, \cdots, a_{r}$  是一组两两正交的非零向量，则  $a_{1}, a_{2}, \cdots, a_{r}$  线性无关.

证 设有  $\lambda_{1},\lambda_{2},\cdots,\lambda_{r}$  使

$$
\lambda_ {1} \boldsymbol {a} _ {1} + \lambda_ {2} \boldsymbol {a} _ {2} + \dots + \lambda_ {r} \boldsymbol {a} _ {r} = \boldsymbol {0},
$$

以 $a_1$ 与上式两端作内积，因当 $i \geqslant 2$ 时，$(a_1, a_i) = 0$，故得

![](raw/pages_0097-0128/images/page_118_image_29.jpg)

考研电子书网站:www.pdf2book.com

115

---

第 5 章 相似矩阵及二次型

$$
\lambda_ {1} (\boldsymbol {a} _ {1}, \boldsymbol {a} _ {1}) = 0,
$$

因  $a_{1} \neq 0$ ，故  $(a_{1}, a_{1}) = \|a_{1}\|^{2} \neq 0$ ，从而必有  $\lambda_{1} = 0$ 。类似可证  $\lambda_{2} = 0, \cdots, \lambda_{r} = 0$ 。于是向量组  $a_{1}, a_{2}, \cdots, a_{r}$  线性无关。证毕

例1 已知3维向量空间 $\mathbb{R}^3$ 中两个向量

$$
\boldsymbol {a} _ {1} = \left( \begin{array}{c} 1 \\ 1 \\ 1 \end{array} \right), \quad \boldsymbol {a} _ {2} = \left( \begin{array}{c} 1 \\ - 2 \\ 1 \end{array} \right)
$$

正交,试求一个非零向量 $a_{3}$ ,使 $a_{1},a_{2},a_{3}$ 两两正交.

解记

$$
\boldsymbol {A} = \binom{\boldsymbol {a} _ {1} ^ {\mathrm{T}}}{\boldsymbol {a} _ {2} ^ {\mathrm{T}}} = \left( \begin{array}{c c c} 1 & 1 & 1 \\ 1 & - 2 & 1 \end{array} \right),
$$

$a_{3}$  应满足齐次线性方程组 Ax=0，即

$$
\left( \begin{array}{c c c} 1 & 1 & 1 \\ 1 & - 2 & 1 \end{array} \right) \left( \begin{array}{c} x _ {1} \\ x _ {2} \\ x _ {3} \end{array} \right) = \binom{0}{0},
$$

由

$$
A \stackrel {r} {\sim} \left( \begin{array}{c c c} 1 & 1 & 1 \\ 0 & - 3 & 0 \end{array} \right) \stackrel {r} {\sim} \left( \begin{array}{c c c} 1 & 0 & 1 \\ 0 & 1 & 0 \end{array} \right),
$$

得 $\left\{\begin{aligned}x_{1}&=-x_{3}\\ x_{2}&=0\end{aligned}\right.$ ，从而有基础解系 $\begin{pmatrix}-1\\ 0\\ 1\end{pmatrix}$ .取 $a_{3}=\begin{pmatrix}-1\\ 0\\ 1\end{pmatrix}$ 即合所求.

定义 3 设 n 维向量  $\xi_{1}, \xi_{2}, \cdots, \xi_{r}$  是向量空间  $V (V \subseteq \mathbb{R}^{n})$  的一个基，若  $\xi_{1}, \xi_{2}, \cdots, \xi_{r}$  两两正交，且都是单位向量，则称  $\xi_{1}, \xi_{2}, \cdots, \xi_{r}$  是 V 的一个标准正交基.

例如

$$
\boldsymbol {\xi} _ {1} = \left( \begin{array}{c} \frac {1}{\sqrt {2}} \\ \frac {1}{\sqrt {2}} \\ 0 \\ 0 \end{array} \right), \quad \boldsymbol {\xi} _ {2} = \left( \begin{array}{c} \frac {1}{\sqrt {2}} \\ - \frac {1}{\sqrt {2}} \\ 0 \\ 0 \end{array} \right), \quad \boldsymbol {\xi} _ {3} = \left( \begin{array}{c} 0 \\ 0 \\ \frac {1}{\sqrt {2}} \\ \frac {1}{\sqrt {2}} \end{array} \right), \quad \boldsymbol {\xi} _ {4} = \left( \begin{array}{c} 0 \\ 0 \\ \frac {1}{\sqrt {2}} \\ - \frac {1}{\sqrt {2}} \end{array} \right)
$$

就是  $R^{4}$  的一个标准正交基.

若  $\xi_{1},\xi_{2},\cdots,\xi_{r}$  是 V 的一个标准正交基,那么 V 中任一向量 a 应能由  $\xi_{1},\xi_{2},\cdots,\xi_{r}$  线性表示,设表示式为

116

---

§1 向量的内积、长度及正交性

$$
\boldsymbol {a} = \lambda_ {1} \boldsymbol {\xi} _ {1} + \lambda_ {2} \boldsymbol {\xi} _ {2} + \dots + \lambda_ {r} \boldsymbol {\xi} _ {r},
$$

为求其中的系数  $\lambda_{i}(i=1,2,\cdots,r)$ ，可用  $\xi_{i}^{T}$  左乘上式，有

$$
\boldsymbol {\xi} _ {i} ^ {\mathrm{T}} \boldsymbol {a} = \lambda_ {i} \boldsymbol {\xi} _ {i} ^ {\mathrm{T}} \boldsymbol {\xi} _ {i} = \lambda_ {i},
$$

即

$$
\lambda_ {i} = \boldsymbol {\xi} _ {i} ^ {\mathrm{T}} \boldsymbol {a} = (\boldsymbol {a}, \boldsymbol {\xi} _ {i}),
$$

这就是向量在标准正交基下的坐标的计算公式.利用这个公式能方便地求得向量的坐标,因此,我们在给向量空间取基时常常取标准正交基.

设 $a_1, a_2, \cdots, a_r$ 是向量空间 $V$ 的一个基, 要求 $V$ 的一个标准正交基. 这也就是要找一组两两正交的单位向量 $\xi_1, \xi_2, \cdots, \xi_r$, 使 $\xi_1, \xi_2, \cdots, \xi_r$ 与 $a_1, a_2, \cdots, a_r$ 等价. 这样一个问题, 称为把基 $a_1, a_2, \cdots, a_r$ 标准正交化.

我们可以用以下办法把 $a_{1},a_{2},\cdots,a_{r}$ 标准正交化:取

$$
\boldsymbol {b} _ {1} = \boldsymbol {a} _ {1},
$$

$$
\boldsymbol {b} _ {2} = \boldsymbol {a} _ {2} - \frac {(\boldsymbol {a} _ {2} , \boldsymbol {b} _ {1})}{(\boldsymbol {b} _ {1} , \boldsymbol {b} _ {1})} \boldsymbol {b} _ {1},
$$

...

$$
\boldsymbol {b} _ {r} = \boldsymbol {a} _ {r} - \frac {(\boldsymbol {a} _ {r} , \boldsymbol {b} _ {1})}{(\boldsymbol {b} _ {1} , \boldsymbol {b} _ {1})} \boldsymbol {b} _ {1} - \frac {(\boldsymbol {a} _ {r} , \boldsymbol {b} _ {2})}{(\boldsymbol {b} _ {2} , \boldsymbol {b} _ {2})} \boldsymbol {b} _ {2} - \dots - \frac {(\boldsymbol {a} _ {r} , \boldsymbol {b} _ {r - 1})}{(\boldsymbol {b} _ {r - 1} , \boldsymbol {b} _ {r - 1})} \boldsymbol {b} _ {r - 1},
$$

容易验证 $b_{1},b_{2},\cdots,b_{r}$ 两两正交，且 $b_{1},b_{2},\cdots,b_{r}$ 与 $a_{1},a_{2},\cdots,a_{r}$ 等价.

然后把它们单位化,即取

$$
\xi_ {1} = \frac {1}{\| \boldsymbol {b} _ {1} \|} \boldsymbol {b} _ {1}, \quad \xi_ {2} = \frac {1}{\| \boldsymbol {b} _ {2} \|} \boldsymbol {b} _ {2}, \quad \dots , \quad \xi_ {r} = \frac {1}{\| \boldsymbol {b} _ {r} \|} \boldsymbol {b} _ {r},
$$

就是 V 的一个标准正交基.

上述从线性无关向量组  $a_{1}, a_{2}, \cdots, a_{r}$  导出正交向量组  $b_{1}, b_{2}, \cdots, b_{r}$  的过程称为施密特(Schmidt)正交化. 它不仅满足  $b_{1}, b_{2}, \cdots, b_{r}$  与  $a_{1}, a_{2}, \cdots, a_{r}$  等价, 还满足: 对任何  $k (1 \leqslant k \leqslant r)$ , 向量组  $b_{1}, b_{2}, \cdots, b_{k}$  与  $a_{1}, a_{2}, \cdots, a_{k}$  等价.

例2 设 $a_1 = \begin{pmatrix} 1 \\ 2 \\ -1 \end{pmatrix}, a_2 = \begin{pmatrix} -1 \\ 3 \\ 1 \end{pmatrix}, a_3 = \begin{pmatrix} 4 \\ -1 \\ 0 \end{pmatrix}$, 试用施密特正交化把这组向量标准正交化.

解 取

$$
\boldsymbol {b} _ {1} = \boldsymbol {a} _ {1},
$$

$$
\boldsymbol {b} _ {2} = \boldsymbol {a} _ {2} - \frac {(\boldsymbol {a} _ {2} , \boldsymbol {b} _ {1})}{\| \boldsymbol {b} _ {1} \| ^ {2}} \boldsymbol {b} _ {1} = \left( \begin{array}{c} - 1 \\ 3 \\ 1 \end{array} \right) - \frac {4}{6} \left( \begin{array}{c} 1 \\ 2 \\ - 1 \end{array} \right) = \frac {5}{3} \left( \begin{array}{c} - 1 \\ 1 \\ 1 \end{array} \right),
$$

考研电子书网站:www.pdf2book.com

117

---

第 5 章 相似矩阵及二次型

$$
\boldsymbol {b} _ {3} = \boldsymbol {a} _ {3} - \frac {(\boldsymbol {a} _ {3} , \boldsymbol {b} _ {1})}{\| \boldsymbol {b} _ {1} \| ^ {2}} \boldsymbol {b} _ {1} - \frac {(\boldsymbol {a} _ {3} , \boldsymbol {b} _ {2})}{\| \boldsymbol {b} _ {2} \| ^ {2}} \boldsymbol {b} _ {2} = \left( \begin{array}{c} 4 \\ - 1 \\ 0 \end{array} \right) - \frac {1}{3} \left( \begin{array}{c} 1 \\ 2 \\ - 1 \end{array} \right) + \frac {5}{3} \left( \begin{array}{c} - 1 \\ 1 \\ 1 \end{array} \right) = 2 \left( \begin{array}{c} 1 \\ 0 \\ 1 \end{array} \right).
$$

再把它们单位化,取

$$
\boldsymbol {\xi} _ {1} = \frac {\boldsymbol {b} _ {1}}{\| \boldsymbol {b} _ {1} \|} = \frac {1}{\sqrt {6}} \left( \begin{array}{c} 1 \\ 2 \\ - 1 \end{array} \right), \quad \boldsymbol {\xi} _ {2} = \frac {\boldsymbol {b} _ {2}}{\| \boldsymbol {b} _ {2} \|} = \frac {1}{\sqrt {3}} \left( \begin{array}{c} - 1 \\ 1 \\ 1 \end{array} \right), \quad \boldsymbol {\xi} _ {3} = \frac {\boldsymbol {b} _ {3}}{\| \boldsymbol {b} _ {3} \|} = \frac {1}{\sqrt {2}} \left( \begin{array}{c} 1 \\ 0 \\ 1 \end{array} \right),
$$

$\xi_{1},\xi_{2},\xi_{3}$  即合所求.

本例中各向量如图 5.1 所示. 用解析几何的术语解释如下:

$b_{2}=a_{2}-c_{2}$ ，而 $c_{2}$ 为 $a_{2}$ 在 $b_{1}$ 上的投影向量，即

$$
\boldsymbol {c} _ {2} = \left(\boldsymbol {a} _ {2}, \frac {\boldsymbol {b} _ {1}}{\| \boldsymbol {b} _ {1} \|}\right) \frac {\boldsymbol {b} _ {1}}{\| \boldsymbol {b} _ {1} \|} = \frac {(\boldsymbol {a} _ {2} , \boldsymbol {b} _ {1})}{\| \boldsymbol {b} _ {1} \| ^ {2}} \boldsymbol {b} _ {1}.
$$

$b_{3}=a_{3}-c_{3}$ ，而 $c_{3}$ 为 $a_{3}$ 在平行于 $b_{1},b_{2}$ 的平面上的投影向量，由于 $b_{1}\perp b_{2}$ ，故 $c_{3}$ 等于 $a_{3}$ 分别在 $b_{1},b_{2}$ 上的投影向量 $c_{31}$ 及 $c_{32}$ 之和，即

![](raw/pages_0097-0128/images/page_121_image_9.jpg)

<details>
<summary>text_image</summary>

a₃
b₃
c₃₂
c₃₁
c₃
c₂
a₂
b₂
a₁ b₁
</details>

图5.1

$$
c _ {3} = c _ {3 1} + c _ {3 2} = \frac {(a _ {3} , b _ {1})}{\| b _ {1} \| ^ {2}} b _ {1} + \frac {(a _ {3} , b _ {2})}{\| b _ {2} \| ^ {2}} b _ {2}.
$$

例 3 已知  $a_{1}=\begin{pmatrix}1\\ 1\\ 1\end{pmatrix}$ ，求一组非零向量  $a_{2},a_{3}$ ，使  $a_{1},a_{2},a_{3}$  两两正交.

解 $a_2, a_3$ 应满足方程 $a_1^{\mathrm{T}} x = 0$，即

$$
x _ {1} + x _ {2} + x _ {3} = 0,
$$

它的基础解系为

$$
\boldsymbol {\xi} _ {1} = \left( \begin{array}{c} - 1 \\ 1 \\ 0 \end{array} \right), \quad \boldsymbol {\xi} _ {2} = \left( \begin{array}{c} - 1 \\ 0 \\ 1 \end{array} \right),
$$

把基础解系正交化,亦即取 公众号: 旗胜考研

$$
\begin{array}{l} \boldsymbol {a} _ {2} = \boldsymbol {\xi} _ {1} = \left( \begin{array}{c} - 1 \\ 1 \\ 0 \end{array} \right), \\ \boldsymbol {a} _ {3} = \boldsymbol {\xi} _ {2} - \frac {(\boldsymbol {\xi} _ {2} , \boldsymbol {\xi} _ {1})}{(\boldsymbol {\xi} _ {1} , \boldsymbol {\xi} _ {1})} \boldsymbol {\xi} _ {1} = \left( \begin{array}{c} - 1 \\ 0 \\ 1 \end{array} \right) - \frac {1}{2} \left( \begin{array}{c} - 1 \\ 1 \\ 0 \end{array} \right) = \frac {1}{2} \left( \begin{array}{c} - 1 \\ - 1 \\ 2 \end{array} \right), \\ \end{array}
$$

图

几何直观

118

---

§1 向量的内积、长度及正交性

因 $a_2, a_3$ 是 $\xi_1, \xi_2$ 的线性组合，故它们仍与 $a_1$ 正交，于是 $a_2, a_3$ 即合所求.

定义4 如果 $n$ 阶矩阵 $\pmb{A}$ 满足

$$
\boldsymbol {A} ^ {\mathrm{T}} \boldsymbol {A} = \boldsymbol {E} (\text {即} \boldsymbol {A} ^ {- 1} = \boldsymbol {A} ^ {\mathrm{T}}),
$$

那么称 A 为正交矩阵.

上式用 A 的列向量表示, 即是

$$
\left( \begin{array}{c} \boldsymbol {a} _ {1} ^ {\mathrm{T}} \\ \boldsymbol {a} _ {2} ^ {\mathrm{T}} \\ \vdots \\ \boldsymbol {a} _ {n} ^ {\mathrm{T}} \end{array} \right) (\boldsymbol {a} _ {1}, \boldsymbol {a} _ {2}, \dots , \boldsymbol {a} _ {n}) = \boldsymbol {E},
$$

这也就是 $n^2$ 个关系式

$$
\boldsymbol {a} _ {i} ^ {\mathrm{T}} \boldsymbol {a} _ {j} = \left\{ \begin{array}{l l} 1, \text {当} i = j, \\ 0, \text {当} i \neq j \end{array} \right. (i, j = 1, 2, \dots , n),
$$

这就说明:方阵 A 为正交矩阵的充分必要条件是 A 的列向量都是单位向量,且两两正交.

因为  $A^{T}A=E$  与  $AA^{T}=E$  等价, 所以上述结论对 A 的行向量亦成立.

由此可见，$n$ 阶正交矩阵 $\pmb{A}$ 的 $n$ 个列(行)向量构成向量空间 $\mathbb{R}^n$ 的一个标准正交基.

例 4 验证矩阵

$$
\boldsymbol {P} = \left( \begin{array}{c c c c} \frac {1}{2} & - \frac {1}{2} & \frac {1}{2} & - \frac {1}{2} \\ \frac {1}{2} & - \frac {1}{2} & - \frac {1}{2} & \frac {1}{2} \\ \frac {1}{\sqrt {2}} & \frac {1}{\sqrt {2}} & 0 & 0 \\ 0 & 0 & \frac {1}{\sqrt {2}} & \frac {1}{\sqrt {2}} \end{array} \right)
$$

是正交矩阵.

证 P 的每个列向量都是单位向量,且两两正交,所以 P 是正交矩阵.

正交矩阵有下述性质:

(i) 若 A 为正交矩阵, 则  $A^{-1}=A^{T}$  也是正交矩阵, 且  $|A|=1$  或 -1;
(ii) 若 A 和 B 都是正交矩阵, 则 AB 也是正交矩阵.

这些性质都可根据正交矩阵的定义直接证得,请读者证明之.

定义 5 若 P 为正交矩阵, 则线性变换 y = Px 称为正交变换.

设 y = Px 为正交变换, 则有

$$
\| y \| = \sqrt {y ^ {\mathrm{T}} y} = \sqrt {x ^ {\mathrm{T}} P ^ {\mathrm{T}} P x} = \sqrt {x ^ {\mathrm{T}} x} = \| x \|\cdot
$$

考研电子书网站:www.pdf2book.com

119

---

第 5 章 相似矩阵及二次型

由于  $\|x\|$  表示向量的长度, 相当于线段的长度, 因此  $\|y\| = \|x\|$  说明经正交变换线段长度保持不变(从而三角形的形状保持不变), 这是正交变换的优良特性.

## § 2 方阵的特征值与特征向量

工程技术中的一些问题,如振动问题和稳定性问题,常可归结为求一个方阵的特征值和特征向量的问题.数学中诸如方阵的对角化及解微分方程组等问题,也都要用到特征值的理论.

定义6 设 $A$ 是 $n$ 阶矩阵, 如果数 $\lambda$ 和 $n$ 维非零列向量 $x$ 使关系式

$$
\boldsymbol {A} \boldsymbol {x} = \lambda \boldsymbol {x} \tag {1}
$$

成立,那么这样的数  $\lambda$  称为矩阵 A 的特征值,非零向量 x 称为 A 的对应于特征值  $\lambda$  的特征向量.

(1)式也可写成

$$
(A - \lambda E) x = 0,
$$

这是 $n$ 个未知数 $n$ 个方程的齐次线性方程组, 它有非零解的充分必要条件是系数行列式

$$
\left| \boldsymbol {A} - \lambda \boldsymbol {E} \right| = 0,
$$

即

$$
\left| \begin{array}{c c c c} a _ {1 1} - \lambda & a _ {1 2} & \dots & a _ {1 n} \\ a _ {2 1} & a _ {2 2} - \lambda & \dots & a _ {2 n} \\ \vdots & \vdots & & \vdots \\ a _ {n 1} & a _ {n 2} & \dots & a _ {n n} - \lambda \end{array} \right| = 0.
$$

上式是以 $\lambda$ 为未知数的一元 $n$ 次方程, 称为矩阵 $\pmb{A}$ 的特征方程, 其左端 $|\pmb{A} - \lambda \pmb{E}|$ 是 $\lambda$ 的 $n$ 次多项式, 记作 $f(\lambda)$, 称为矩阵 $\pmb{A}$ 的特征多项式. 显然, $\pmb{A}$ 的特征值就是特征方程的解. 特征方程在复数范围内恒有解, 其个数为方程的次数 (重根按重数计算), 因此, $n$ 阶矩阵 $\pmb{A}$ 在复数范围内有 $n$ 个特征值.

设 n 阶矩阵  $\boldsymbol{A}=(a_{ij})$  的特征值为  $\lambda_{1},\lambda_{2},\cdots,\lambda_{n}$ ，不难证明①

(i)  $\lambda_{1}+\lambda_{2}+\cdots+\lambda_{n}=a_{11}+a_{22}+\cdots+a_{nn}$  （其中  $a_{11}+a_{22}+\cdots+a_{nn}$  称为 A 的迹，记为  $\mathrm{tr}(A)$ ）；
(ii)  $\lambda_{1}\lambda_{2}\cdots\lambda_{n}=|A|$ .

由(ii)可知 A 是可逆矩阵的充分必要条件是它的 n 个特征值全不为零.

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">①  $f(\lambda)=(\lambda_{1}-\lambda)(\lambda_{2}-\lambda)\cdots(\lambda_{n}-\lambda)$ ，其中  $\lambda^{0}$  和  $\lambda^{n-1}$  的系数依次为  $\lambda_{1}\lambda_{2}\cdots\lambda_{n}$  和  $(-1)^{n-1}(\lambda_{1}+\lambda_{2}+\cdots+\lambda_{n})$ ，故只需证明多项式  $|A-\lambda E|$  中  $\lambda^{0}$  和  $\lambda^{n-1}$  的系数依次为  $|A|$  和  $(-1)^{n-1}(a_{11}+a_{22}+\cdots+a_{nn})$ .</span></small>

![](raw/pages_0097-0128/images/page_123_image_20.jpg)

证明拓展

120

---

§2 方阵的特征值与特征向量

设 $\lambda = \lambda_{i}$ 为矩阵 $A$ 的一个特征值，则由方程

$$
(A - \lambda_ {i} E) x = 0
$$

可求得非零解 $x = p_{i}$, 那么 $p_{i}$ 便是 $\pmb{A}$ 的对应于特征值 $\lambda_{i}$ 的特征向量. (若 $\lambda_{i}$ 为实数, 则 $p_{i}$ 可取实向量; 若 $\lambda_{i}$ 为复数, 则 $p_{i}$ 为复向量.)

例 5 求矩阵  $A=\begin{pmatrix}3&-1\\-1&3\end{pmatrix}$  的特征值和特征向量.

解 $A$ 的特征多项式为

$$
\left| \boldsymbol {A} - \lambda \boldsymbol {E} \right| = \left| \begin{array}{c c} 3 - \lambda & - 1 \\ - 1 & 3 - \lambda \end{array} \right| = (3 - \lambda) ^ {2} - 1 = 8 - 6 \lambda + \lambda^ {2} = (4 - \lambda) (2 - \lambda),
$$

所以 A 的特征值为  $\lambda_{1}=2,\lambda_{2}=4.$

当  $\lambda_{1}=2$  时, 对应的特征向量应满足

$$
\left( \begin{array}{c c} 3 - 2 & - 1 \\ - 1 & 3 - 2 \end{array} \right) \binom{x _ {1}}{x _ {2}} = \binom{0}{0},
$$

即

$$
\left( \begin{array}{c c} 1 & - 1 \\ - 1 & 1 \end{array} \right) \binom{x _ {1}}{x _ {2}} = \binom{0}{0},
$$

解得 $x_{1} = x_{2}$ ，所以对应的特征向量可取为

$$
\boldsymbol {p} _ {1} = \binom{1}{1}.
$$

当 $\lambda_{2} = 4$ 时，由

$$
\left( \begin{array}{c c} 3 - 4 & - 1 \\ - 1 & 3 - 4 \end{array} \right) \binom{x _ {1}}{x _ {2}} = \binom{0}{0},
$$

即

$$
\left( \begin{array}{c c} - 1 & - 1 \\ - 1 & - 1 \end{array} \right) \binom{x _ {1}}{x _ {2}} = \binom{0}{0},
$$

解得 $x_{1} = -x_{2}$ ，所以对应的特征向量可取为

$$
\boldsymbol {p} _ {2} = \binom{- 1}{1}.
$$

显然, 若  $p_{i}$  (i=1,2) 是矩阵  $A'$  的对应于特征值  $\lambda_{i}$  的特征向量, 则  $k p_{i}$  ( $k \neq 0$ ) 也是对应于  $\lambda_{i}$  的特征向量.

例6 求矩阵

考研电子书网站:www.pdf2book.com

121

---

第5章 相似矩阵及二次型

$$
\boldsymbol {A} = \left( \begin{array}{c c c} - 1 & 1 & 0 \\ - 4 & 3 & 0 \\ 1 & 0 & 2 \end{array} \right)
$$

的特征值和特征向量.

解 $A$ 的特征多项式为

$$
\left| \boldsymbol {A} - \lambda \boldsymbol {E} \right| = \left| \begin{array}{c c c} - 1 - \lambda & 1 & 0 \\ - 4 & 3 - \lambda & 0 \\ 1 & 0 & 2 - \lambda \end{array} \right| = (2 - \lambda) (1 - \lambda) ^ {2},
$$

所以 A 的特征值为  $\lambda_{1}=2,\lambda_{2}=\lambda_{3}=1$ .

当  $\lambda_{1}=2$  时, 解方程  $(A-2E)x=0$ . 由

$$
\dot {\boldsymbol {A}} - 2 \boldsymbol {E} = \left( \begin{array}{c c c} - 3 & 1 & 0 \\ - 4 & 1 & 0 \\ 1 & 0 & 0 \end{array} \right) \sim \left( \begin{array}{c c c} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 0 \end{array} \right),
$$

得基础解系

$$
\boldsymbol {p} _ {1} = \left( \begin{array}{c} 0 \\ 0 \\ 1 \end{array} \right),
$$

所以 $kp_{1} (k \neq 0)$ 是对应于 $\lambda_{1} = 2$ 的全部特征向量.

当 $\lambda_{2} = \lambda_{3} = 1$ 时，解方程 $(A - E)x = 0.$ 由

$$
\boldsymbol {A} - \boldsymbol {E} = \left( \begin{array}{c c c} {- 2} & {1} & {0} \\ {- 4} & {2} & {0} \\ {1} & {0} & {1} \end{array} \right) \stackrel {{r}} {{\sim}} \left( \begin{array}{c c c} {1} & {0} & {1} \\ {0} & {1} & {2} \\ {0} & {0} & {0} \end{array} \right),
$$

得基础解系

$$
\boldsymbol {p} _ {2} = \left( \begin{array}{c} - 1 \\ - 2 \\ 1 \end{array} \right),
$$

所以 $kp_{2} (k \neq 0)$ 是对应于 $\lambda_{2} = \lambda_{3} = 1$ 的全部特征向量.

例 7 设  $\lambda$  是方阵 A 的特征值, 证明:

(1) $\lambda^{2}$ 是 $A^{2}$ 的特征值;
(2) 当 A 可逆时,  $\frac{1}{\lambda}$  是  $A^{-1}$  的特征值.

证 因 $\lambda$ 是 $A$ 的特征值, 故有 $p \neq 0$ 使 $Ap = \lambda p$. 于是

(1) 因为  $A^{2}p = A(Ap) = A(\lambda p) = \lambda(Ap) = \lambda^{2}p$ ，所以  $\lambda^{2}$  是  $A^{2}$  的特征值.

(2) 当 A 可逆时, 由  $Ap = \lambda p$ , 有  $p = \lambda A^{-1}p$ , 因  $p \neq 0$ , 知  $\lambda \neq 0$ , 故

122

---

§2 方阵的特征值与特征向量

$$
A ^ {- 1} p = \frac {1}{\lambda} p,
$$

所以 $\frac{1}{\lambda}$ 是 $A^{-1}$ 的特征值.

按此例类推,不难证明:若  $\lambda$  是 A 的特征值,则  $\lambda^{k}$  是  $A^{k}$  的特征值; $\varphi(\lambda)$  是  $\varphi(A)$  的特征值(其中  $\varphi(\lambda)=a_{0}+a_{1}\lambda+\cdots+a_{m}\lambda^{m}$  是  $\lambda$  的多项式, $\varphi(A)=a_{0}E+a_{1}A+\cdots+a_{m}A^{m}$  是矩阵 A 的多项式).这是特征值的一个重要性质.

例8 设3阶矩阵 $\pmb{A}$ 的特征值为 $1, -1, 2$，求 $A^{*} + 3A - 2E$ 的特征值.

解 因 $\pmb{A}$ 的特征值全不为0, 知 $\pmb{A}$ 可逆, 故 $A^{*} = |A|A^{-1}$, 而 $|A| = \lambda_{1}\lambda_{2}\lambda_{3} = -2$, 所以

$$
A ^ {*} + 3 A - 2 E = - 2 A ^ {- 1} + 3 A - 2 E.
$$

把上式记作 $\varphi(A)$, 有 $\varphi(\lambda) = -\frac{2}{\lambda} + 3\lambda - 2$. 这里, $\varphi(A)$ 虽不是矩阵多项式, 但也具有矩阵多项式的特性, 从而可得 $\varphi(A)$ 的特征值为 $\varphi(1) = -1, \varphi(-1) = -3, \varphi(2) = 3$.

下面介绍特征向量的一些性质.

定理 2 设  $\lambda_{1}, \lambda_{2}, \cdots, \lambda_{m}$  是方阵 A 的 m 个特征值,  $p_{1}, p_{2}, \cdots, p_{m}$  依次是与之对应的特征向量, 如果  $\lambda_{1}, \lambda_{2}, \cdots, \lambda_{m}$  各不相等, 则  $p_{1}, p_{2}, \cdots, p_{m}$  线性无关.

证 用数学归纳法.

当 $m = 1$ 时，因特征向量 $\pmb{p}_1\neq \mathbf{0}$ ，故只含一个向量的向量组 $\pmb{p}_{1}$ 线性无关.

假设当 m=k-1 时结论成立, 要证当 m=k 时结论也成立. 即假设向量组  $p_{1}, p_{2}, \cdots, p_{k-1}$  线性无关, 要证向量组  $p_{1}, p_{2}, \cdots, p_{k}$  线性无关. 为此, 设有

$$
x _ {1} \boldsymbol {p} _ {1} + x _ {2} \boldsymbol {p} _ {2} + \dots + x _ {k - 1} \boldsymbol {p} _ {k - 1} + x _ {k} \boldsymbol {p} _ {k} = \mathbf {0}, \tag {2}
$$

用 $\mathbf{A}$ 左乘上式，得

$$
x _ {1} A p _ {1} + x _ {2} A p _ {2} + \dots + x _ {k - 1} A p _ {k - 1} + x _ {k} A p _ {k} = 0,
$$

即

$$
x _ {1} \lambda_ {1} p _ {1} + x _ {2} \lambda_ {2} p _ {2} + \dots + x _ {k - 1} \lambda_ {k - 1} p _ {k - 1} + x _ {k} \lambda_ {k} p _ {k} = 0. \tag {3}
$$

(3)式减去(2)式的 $\lambda_{k}$ 倍，得

$$
x _ {1} (\lambda_ {1} - \lambda_ {k}) p _ {1} + x _ {2} (\lambda_ {2} - \lambda_ {k}) p _ {2} + \dots + x _ {k - 1} (\lambda_ {k - 1} - \lambda_ {k}) p _ {k - 1} = 0.
$$

按归纳假设  $p_{1}, p_{2}, \cdots, p_{k-1}$  线性无关，故  $x_{i}(\lambda_{i}-\lambda_{k}) = 0 (i=1,2,\cdots,k-1)$ . 而  $\lambda_{i}-\lambda_{k} \neq 0 (i=1,2,\cdots,k-1)$ ，于是得  $x_{i}=0 (i=1,2,\cdots,k-1)$ ，代入(2)式得  $x_{k}p_{k}=0$ ，而  $p_{k} \neq 0$ ，得  $x_{k}=0$ . 因此，向量组  $p_{1}, p_{2}, \cdots, p_{k}$  线性无关. 证毕

推论 设  $\lambda_{1}$  和  $\lambda_{2}$  是方阵 A 的两个不同特征值,  $\xi_{1}, \xi_{2}, \cdots, \xi_{s}$  和  $\eta_{1}, \eta_{2}, \cdots, \eta_{t}$  分别是对应于  $\lambda_{1}$  和  $\lambda_{2}$  的线性无关的特征向量, 则  $\xi_{1}, \xi_{2}, \cdots, \xi_{s}, \eta_{1}, \eta_{2}, \cdots, \eta_{t}$  线性无关. (证明留作习题.)

上述推论表明:对应于两个不同特征值的线性无关的特征向量组,合起来仍是线

考研电子书网站:www.pdf2book.com

123

---

第5章 相似矩阵及二次型

性无关的.这一结论对 $m(m\geqslant 2)$ 个特征值的情形也成立.

例9 设 $\lambda_{1}$ 和 $\lambda_{2}$ 是矩阵 $A$ 的两个不同的特征值, 对应的特征向量依次为 $p_{1}$ 和 $p_{2}$, 证明 $p_{1} + p_{2}$ 不是 $A$ 的特征向量.

证 按题设, 有 $A\pmb{p}_{1} = \lambda_{1}\pmb{p}_{1}, A\pmb{p}_{2} = \lambda_{2}\pmb{p}_{2}$, 故

$$
A (\boldsymbol {p} _ {1} + \boldsymbol {p} _ {2}) = \lambda_ {1} \boldsymbol {p} _ {1} + \lambda_ {2} \boldsymbol {p} _ {2}.
$$

用反证法, 假设  $p_{1} + p_{2}$  是 A 的特征向量, 则应存在数  $\lambda$ , 使  $A(p_{1} + p_{2}) = \lambda(p_{1} + p_{2})$ , 于是

$$
\lambda \left(\boldsymbol {p} _ {1} + \boldsymbol {p} _ {2}\right) = \lambda_ {1} \boldsymbol {p} _ {1} + \lambda_ {2} \boldsymbol {p} _ {2},
$$

即

$$
(\lambda_ {1} - \lambda) \boldsymbol {p} _ {1} + (\lambda_ {2} - \lambda) \boldsymbol {p} _ {2} = \mathbf {0},
$$

因 $\lambda_1 \neq \lambda_2$，按定理 2 知 $p_1, p_2$ 线性无关，故由上式得 $\lambda_1 - \lambda = \lambda_2 - \lambda = 0$，即 $\lambda_1 = \lambda_2$，与题设矛盾。因此 $p_1 + p_2$ 不是 $A$ 的特征向量。

## § 3 相似矩阵

定义7 设 $A, B$ 都是 $n$ 阶矩阵, 若有可逆矩阵 $\pmb{P}$, 使

$$
P ^ {- 1} A P = B,
$$

则称 B 是 A 的相似矩阵, 或说矩阵 A 与 B 相似. 对 A 进行运算  $P^{-1}AP$  称为对 A 进行相似变换, 可逆矩阵 P 称为把 A 变成 B 的相似变换矩阵.

定理3 若 $n$ 阶矩阵 $\pmb{A}$ 与 $\pmb{B}$ 相似, 则 $\pmb{A}$ 与 $\pmb{B}$ 的特征多项式相同, 从而 $\pmb{A}$ 与 $\pmb{B}$ 的特征值亦相同.

证 因 $\pmb{A}$ 与 $\pmb{B}$ 相似, 即有可逆矩阵 $\pmb{P}$, 使 $P^{-1}AP = B$. 故

$$
\begin{array}{l} \left| \boldsymbol {B} - \lambda \boldsymbol {E} \right| = \left| \boldsymbol {P} ^ {- 1} \boldsymbol {A} \boldsymbol {P} - \boldsymbol {P} ^ {- 1} (\lambda \boldsymbol {E}) \boldsymbol {P} \right| = \left| \boldsymbol {P} ^ {- 1} (\boldsymbol {A} - \lambda \boldsymbol {E}) \boldsymbol {P} \right| \\ = | \boldsymbol {P} ^ {- 1} | | \boldsymbol {A} - \lambda \boldsymbol {E} | | \boldsymbol {P} | = | \boldsymbol {A} - \lambda \boldsymbol {E} |. \quad \text {证毕} \\ \end{array}
$$

推论 若 $n$ 阶矩阵 $A$ 与对角矩阵

$$
\boldsymbol {\Lambda} = \left( \begin{array}{c c c c} \lambda_ {1} & & & \\ & \lambda_ {2} & & \\ & & \ddots & \\ & & & \lambda_ {n} \end{array} \right)
$$

相似, 则  $\lambda_{1}, \lambda_{2}, \cdots, \lambda_{n}$  即是 A 的 n 个特征值.

证 因  $\lambda_{1}, \lambda_{2}, \cdots, \lambda_{n}$  即是 A 的 n 个特征值，由定理 3 知  $\lambda_{1}, \lambda_{2}, \cdots, \lambda_{n}$  也就是 A 的 n 个特征值.
证毕

124

---

§3 相似矩阵

在第2章中我们曾得出结论: 若  $A = PBP^{-1}$ ，则  $A^{k} = PB^{k}P^{-1}.A$  的多项式

$$
\varphi (A) = P \varphi (B) P ^ {- 1}.
$$

特别地,若有可逆矩阵 P 使  $P^{-1}AP=\Lambda$  为对角矩阵,即若 A 相似于对角矩阵  $\Lambda$ ,则

$$
A ^ {k} = P \Lambda^ {k} P ^ {- 1}, \quad \varphi (A) = P \varphi (\Lambda) P ^ {- 1}.
$$

而对于对角矩阵 $\Lambda$ ，有

$$
\boldsymbol {\Lambda} ^ {k} = \left( \begin{array}{c c c c} \lambda_ {1} ^ {k} & & & \\ & \lambda_ {2} ^ {k} & & \\ & & \ddots & \\ & & & \lambda_ {n} ^ {k} \end{array} \right), \quad \varphi (\boldsymbol {\Lambda}) = \left( \begin{array}{c c c c} \varphi (\lambda_ {1}) & & & \\ & \varphi (\lambda_ {2}) & & \\ & & \ddots & \\ & & & \varphi (\lambda_ {n}) \end{array} \right),
$$

由此可方便地计算 A 的多项式  $\varphi(A)$ .

下面我们要讨论的主要问题是: 对 n 阶矩阵 A, 是否存在相似变换矩阵 P, 使  $P^{-1}AP = \Lambda$  为对角矩阵, 如果这样的 P 存在, 则称矩阵 A 可对角化.

假设已经找到可逆矩阵 $P$，使 $P^{-1}AP = \Lambda$ 为对角矩阵。把 $P$ 用其列向量表示为

$$
\boldsymbol {P} = (\boldsymbol {p} _ {1}, \boldsymbol {p} _ {2}, \dots , \boldsymbol {p} _ {n}),
$$

由 $P^{-1}AP = \Lambda$ ，得 $AP = P\Lambda$ ，即

$$
A (\boldsymbol {p} _ {1}, \boldsymbol {p} _ {2}, \dots , \boldsymbol {p} _ {n}) = (\boldsymbol {p} _ {1}, \boldsymbol {p} _ {2}, \dots , \boldsymbol {p} _ {n}) \left( \begin{array}{c c c c} \lambda_ {1} & & & \\ & \lambda_ {2} & & \\ & & \ddots & \\ & & & \lambda_ {n} \end{array} \right) = (\lambda_ {1} \boldsymbol {p} _ {1}, \lambda_ {2} \boldsymbol {p} _ {2}, \dots , \lambda_ {n} \boldsymbol {p} _ {n}),
$$

于是有

$$
A p _ {i} = \lambda_ {i} p _ {i} \quad (i = 1, 2, \dots , n).
$$

可见  $\lambda_{i}$  是 A 的特征值, 而 P 的列向量  $p_{i}$  就是 A 的对应于特征值  $\lambda_{i}$  的特征向量. 由于 P 可逆, 所以 A 有 n 个线性无关的特征向量  $p_{1}, p_{2}, \cdots, p_{n}$ .

反之, 若 A 有 n 个线性无关的特征向量  $p_{1}, p_{2}, \cdots, p_{n}$ ，其中  $p_{i}$  对应于特征值  $\lambda_{i}$ ，则矩阵  $P = (p_{1}, p_{2}, \cdots, p_{n})$  可逆，且 AP = PA，这里  $\Lambda = \text{diag}(\lambda_{1}, \lambda_{2}, \cdots, \lambda_{n})$ 。于是  $P^{-1}AP = \Lambda$ ，即 A 与对角矩阵相似。

由上面的讨论即有

定理 4 n 阶矩阵 A 与对角矩阵相似（即 A 可对角化）的充分必要条件是 A 有 n 个线性无关的特征向量.

联系定理 2, 可得

推论 如果 $n$ 阶矩阵 $\pmb{A}$ 的 $n$ 个特征值互不相等, 则 $\pmb{A}$ 与对角矩阵相似.

当 A 的特征方程有重根时, 就不一定有 n 个线性无关的特征向量, 从而不一定能

考研电子书网站:www.pdf2book.com

125

---

第5章 相似矩阵及二次型

对角化.例如在例6中 $\pmb{A}$ 的特征方程有重根，确实找不到3个线性无关的特征向量，因此例6中的 $\pmb{A}$ 不可对角化.

例10 设矩阵

$$
\boldsymbol {A} = \left( \begin{array}{c c c} - 2 & 1 & 1 \\ 0 & 2 & 0 \\ - 4 & 1 & 3 \end{array} \right),
$$

问 A 能否对角化？若能，则求可逆矩阵 P 和对角矩阵  $\Lambda$ ，使  $P^{-1}AP = \Lambda$ .

解 先求 A 的特征值.

$$
\begin{array}{l} \left| \boldsymbol {A} - \lambda \boldsymbol {E} \right| = \left| \begin{array}{c c c} - 2 - \lambda & 1 & 1 \\ 0 & 2 - \lambda & 0 \\ - 4 & 1. & 3 - \lambda \end{array} \right| = (2 - \lambda) \left| \begin{array}{c c} - 2 - \lambda & 1 \\ - 4 & 3 - \lambda \end{array} \right| \\ = (2 - \lambda) (\lambda^ {2} - \lambda - 2) = - (\lambda + 1) (\lambda - 2) ^ {2}, \\ \end{array}
$$

所以 A 的特征值为  $\lambda_{1} = -1, \lambda_{2} = \lambda_{3} = 2.$

再求 A 的特征向量.

当  $\lambda_{1}=-1$  时, 解方程  $(A+E)x=0$ . 由

$$
\boldsymbol {A} + \boldsymbol {E} = \left( \begin{array}{c c c} - 1 & 1 & 1 \\ 0 & 3 & 0 \\ - 4 & 1 & 4 \end{array} \right) \stackrel {{r}} {{\sim}} \left( \begin{array}{c c c} 1 & 0 & - 1 \\ 0 & 1 & 0 \\ 0 & 0 & 0 \end{array} \right),
$$

得对应的特征向量

$$
\boldsymbol {p} _ {1} = \left( \begin{array}{c} 1 \\ 0 \\ 1 \end{array} \right);
$$

当 $\lambda_{2} = \lambda_{3} = 2$ 时，解方程 $(A - 2E)x = 0.$ 由

$$
\boldsymbol {A} - 2 \boldsymbol {E} = \left( \begin{array}{c c c} {- 4} & {1} & {1} \\ {0} & {0} & {0} \\ {- 4} & {1} & {1} \end{array} \right) \stackrel {{r}} {{\sim}} \left( \begin{array}{c c c} {- 4} & {1} & {1} \\ {0} & {0} & {0} \\ {0} & {0} & {0} \end{array} \right),
$$

得对应的线性无关特征向量

$$
\boldsymbol {p} _ {2} = \left( \begin{array}{c} 0 \\ 1 \\ - 1 \end{array} \right), \quad \boldsymbol {p} _ {3} = \left( \begin{array}{c} 1 \\ 0 \\ 4 \end{array} \right).
$$

由定理2的推论,知 $p_{1},p_{2},p_{3}$ 线性无关,再由定理4知A可对角化;并且若记

$$
\boldsymbol {P} = (\boldsymbol {p} _ {1}, \boldsymbol {p} _ {2}, \boldsymbol {p} _ {3}) = \left( \begin{array}{c c c} 1 & 0 & 1 \\ 0 & 1 & 0 \\ 1 & - 1 & 4 \end{array} \right),
$$

126

---

§ 4 对称矩阵的对角化

则有

$$
P ^ {- 1} A P = \mathrm{diag} (- 1, 2, 2).
$$

要注意上式中对角矩阵的对角元的排列次序应与 P 中列向量的排列次序一致.

例11 设

$$
\boldsymbol {A} = \left( \begin{array}{c c c} 0 & 0 & 1 \\ 1 & 1 & t \\ 1 & 0 & 0 \end{array} \right),
$$

问 $t$ 为何值时, 矩阵 $\pmb{A}$ 可对角化?

解 由

$$
\left| \boldsymbol {A} - \lambda \boldsymbol {E} \right| = \left| \begin{array}{c c c} - \lambda & 0 & 1 \\ 1 & 1 - \lambda & t \\ 1 & 0 & - \lambda \end{array} \right| = (1 - \lambda) \left| \begin{array}{c c} - \lambda & 1 \\ 1 & - \lambda \end{array} \right| = - (\lambda - 1) ^ {2} (\lambda + 1),
$$

得 $\lambda_{1} = -1, \lambda_{2} = \lambda_{3} = 1$.

当单根 $\lambda_{1} = -1$ 时, 可求得线性无关的特征向量恰有 1 个, 故矩阵 $A$ 可对角化的充分必要条件是对应重根 $\lambda_{2} = \lambda_{3} = 1$, 有 2 个线性无关的特征向量, 即方程 $(A - E)x = 0$ 有 2 个线性无关的解, 亦即系数矩阵 $A - E$ 的秩 $R(A - E) = 1$. 由

$$
\boldsymbol {A} - \boldsymbol {E} = \left( \begin{array}{c c c} {- 1} & {0} & {1} \\ {1} & {0} & {t} \\ {1} & {0} & {- 1} \end{array} \right) \stackrel {{r}} {{\sim}} \left( \begin{array}{c c c} {1} & {0} & {- 1} \\ {0} & {0} & {t + 1} \\ {0} & {0} & {0} \end{array} \right),
$$

要 $R(A - E) = 1$ ，得 $t + 1 = 0$ ，即 $t = -1$

因此, 当 t = -1 时, 矩阵 A 可对角化.

## § 4 对称矩阵的对角化

一个 $n$ 阶矩阵具备什么条件才能有 $n$ 个线性无关的特征向量, 从而可对角化? 这是一个较复杂的问题. 我们对此不进行一般性的讨论, 而仅讨论当 $\pmb{A}$ 为对称矩阵的情形.

先介绍两个关于对称矩阵的特征值和特征向量的性质.

## 性质 1 对称矩阵的特征值为实数.

证 先介绍一个记号. 设复数矩阵 $X = (x_{ij}), \overline{x}_{ij}$ 为 $x_{ij}$ 的共轭复数, 记 $\overline{X} = (\overline{x}_{ij})$, 即 $\overline{X}$ 是由 $X$ 的对应元素的共轭复数构成的矩阵.

设复数  $\lambda$  为对称矩阵 A 的特征值, 复向量 x 为对应的特征向量, 即  $Ax = \lambda x, x \neq 0$ .

考研电子书网站:www.pdf2book.com

127

---

第5章 相似矩阵及二次型

用 $\overline{\lambda}$ 表示 $\lambda$ 的共轭复数, 而 $A$ 为实矩阵, 有 $A = \overline{A}$, 故 $A\overline{x} = \overline{A}\overline{x} = \overline{Ax} = \overline{\lambda x} = \overline{\lambda}\overline{x}$. 于是有

$$
\overline {{x}} ^ {\mathrm{T}} A x = \overline {{x}} ^ {\mathrm{T}} (A x) = \overline {{x}} ^ {\mathrm{T}} \lambda x = \lambda \overline {{x}} ^ {\mathrm{T}} x
$$

及

$$
\overline {{x}} ^ {\mathrm{T}} A x = (\overline {{x}} ^ {\mathrm{T}} A ^ {\mathrm{T}}) x = (A \overline {{x}}) ^ {\mathrm{T}} x = (\overline {{\lambda}} \overline {{x}}) ^ {\mathrm{T}} x = \overline {{\lambda}} \overline {{x}} ^ {\mathrm{T}} x,
$$

两式相减, 得

$$
(\lambda - \overline {{\lambda}}) \overline {{x}} ^ {\mathrm{T}} x = 0,
$$

但因 $x \neq 0$，所以

$$
\overline {{x}} ^ {\mathrm{T}} x = \sum_ {i = 1} ^ {n} \overline {{x}} _ {i} x _ {i} = \sum_ {i = 1} ^ {n} \left| x _ {i} \right| ^ {2} \neq 0,
$$

故 $\lambda -\overline{\lambda} = 0$ ，即 $\lambda = \overline{\lambda}$ ，这就说明 $\lambda$ 是实数.

证毕

显然,当特征值  $\lambda_{i}$  为实数时,齐次线性方程组

$$
(A - \lambda_ {i} E) x = 0
$$

是实系数方程组, 由  $\left|A-\lambda_{i}E\right|=0$  知必有实的基础解系, 所以对应的特征向量可以取实向量.

性质2 设 $\lambda_{1}, \lambda_{2}$ 是对称矩阵 $A$ 的两个特征值, $p_{1}, p_{2}$ 是对应的特征向量. 若 $\lambda_{1} \neq \lambda_{2}$, 则 $p_{1}$ 与 $p_{2}$ 正交.

证 $\lambda_{1}p_{1} = Ap_{1},\lambda_{2}p_{2} = Ap_{2},\lambda_{1}\neq \lambda_{2}.$

因 $\mathbf{A}$ 为对称矩阵，故 $\lambda_1\pmb{p}_1^{\mathrm{T}} = (\lambda_1\pmb{p}_1)^{\mathrm{T}} = (\pmb {A}\pmb{p}_1)^{\mathrm{T}} = \pmb{p}_1^{\mathrm{T}}\pmb{A}^{\mathrm{T}} = \pmb{p}_1^{\mathrm{T}}\pmb{A}$，于是

$$
\lambda_ {1} \boldsymbol {p} _ {1} ^ {\mathrm{T}} \boldsymbol {p} _ {2} = \boldsymbol {p} _ {1} ^ {\mathrm{T}} \boldsymbol {A} \boldsymbol {p} _ {2} = \boldsymbol {p} _ {1} ^ {\mathrm{T}} (\lambda_ {2} \boldsymbol {p} _ {2}) = \lambda_ {2} \boldsymbol {p} _ {1} ^ {\mathrm{T}} \boldsymbol {p} _ {2},
$$

即

$$
(\lambda_ {1} - \lambda_ {2}) \boldsymbol {p} _ {1} ^ {\mathrm{T}} \boldsymbol {p} _ {2} = 0.
$$

但 $\lambda_1 \neq \lambda_2$，故 $p_1^T p_2 = 0$，即 $p_1$ 与 $p_2$ 正交。

证毕

定理5 设 $A$ 为 $n$ 阶对称矩阵, 则必有正交矩阵 $P$, 使 $P^{-1}AP = P^{\mathrm{T}}AP = A$, 其中 $\Lambda$ 是以 $A$ 的 $n$ 个特征值为对角元的对角矩阵.

此定理不予证明.

性质3 设 $A$ 为 $n$ 阶对称矩阵, $\lambda$ 是 $A$ 的特征方程的 $k$ 重根, 则矩阵 $A - \lambda E$ 的秩 $R(A - \lambda E) = n - k$, 从而对应特征值 $\lambda$ 恰有 $k$ 个线性无关的特征向量.

证 按定理 5 知对称矩阵 A 与对角矩阵  $\boldsymbol{\Lambda}=\mathrm{diag}(\lambda_{1},\lambda_{2},\cdots,\lambda_{n})$  相似，从而  $A-\lambda E$  与  $\boldsymbol{\Lambda}-\lambda E=\mathrm{diag}(\lambda_{1}-\lambda,\lambda_{2}-\lambda,\cdots,\lambda_{n}-\lambda)$  相似。当  $\lambda$  是 A 的 k 重特征根时， $\lambda_{1},\lambda_{2},\cdots,\lambda_{n}$  这 n 个特征值中有 k 个等于  $\lambda'$ ，有 n-k 个不等于  $\lambda$ ，从而对角矩阵  $A-\lambda E$  的对角元恰有 k 个等于 0，于是  $R(\boldsymbol{\Lambda}-\lambda\boldsymbol{E})=n-k$ 。而  $R(\boldsymbol{A}-\lambda\boldsymbol{E})=R(\boldsymbol{\Lambda}-\lambda\boldsymbol{E})$ ，所以  $R(\boldsymbol{A}-\lambda\boldsymbol{E})=n-k$ 。

证毕

128

---

§4 对称矩阵的对角化

依据定理5及性质3,我们有下述把 $n$ 阶对称矩阵 $\pmb{A}$ 对角化的步骤:

(i) 求出 A 的全部互不相等的特征值  $\lambda_{1}, \lambda_{2}, \cdots, \lambda_{s}$ ，它们的重数依次为  $k_{1}, k_{2}, \cdots, k_{s}$  ( $k_{1} + k_{2} + \cdots + k_{s} = n$ ).

（ii）对每个 $k_{i}$ 重特征值 $\lambda_{i}$，求方程 $(A - \lambda_{i}E)x = 0$ 的基础解系，得 $k_{i}$ 个线性无关的特征向量。再把它们正交化、单位化，得 $k_{i}$ 个两两正交的单位特征向量。因 $k_{1} + k_{2} + \dots + k_{s} = n$，故总共可得 $n$ 个两两正交的单位特征向量。

（iii）把这 $n$ 个两两正交的单位特征向量构成正交矩阵 $\pmb{P}$，便有 $\pmb{P}^{-1}\pmb{A}\pmb{P} = \pmb{P}^{\mathrm{T}}\pmb{A}\pmb{P} = \pmb{\Lambda}$. 注意 $\pmb{\Lambda}$ 中对角元的排列次序应与 $\pmb{P}$ 中列向量的排列次序相对应.

例12 设

$$
\boldsymbol {A} = \left( \begin{array}{c c c} 0 & - 1 & 1 \\ - 1 & 0 & 1 \\ 1 & 1 & 0 \end{array} \right),
$$

求一个正交矩阵 P, 使  $P^{-1}AP = \Lambda$  为对角矩阵.

解 由

$$
\begin{array}{l} \left| \boldsymbol {A} - \lambda \boldsymbol {E} \right| = \left| \begin{array}{r r r} - \lambda & - 1 & 1 \\ - 1 & - \lambda & 1 \\ 1 & 1 & - \lambda \end{array} \right| \stackrel {{r _ {1} - r _ {2}}} {{=}} \left| \begin{array}{c c c} 1 - \lambda & \lambda - 1 & 0 \\ - 1 & - \lambda & 1 \\ 1 & 1 & - \lambda \end{array} \right| \stackrel {{c _ {2} + c _ {1}}} {{=}} \left| \begin{array}{c c c} 1 - \lambda & 0 & 0 \\ - 1 & - 1 - \lambda & 1 \\ 1 & 2 & - \lambda \end{array} \right| \\ = (1 - \lambda) (\lambda^ {2} + \lambda - 2) = - (\lambda - 1) ^ {2} (\lambda + 2), \\ \end{array}
$$

求得 A 的特征值为  $\lambda_{1} = -2, \lambda_{2} = \lambda_{3} = 1$ .

对应 $\lambda_{1} = -2$ ，解方程 $(A + 2E)x = 0$ ，由

$$
\boldsymbol {A} + 2 \boldsymbol {E} = \left( \begin{array}{r r r} 2 & - 1 & 1 \\ - 1 & 2 & 1 \\ 1 & 1 & 2 \end{array} \right) \stackrel {{r}} {{\sim}} \left( \begin{array}{c c c} 1 & 0 & 1 \\ 0 & 1 & 1 \\ 0 & 0 & 0 \end{array} \right),
$$

得基础解系  $\xi_{1}=\begin{pmatrix}-1\\-1\\1\end{pmatrix}$ . 将  $\xi_{1}$  单位化, 得  $p_{1}=\frac{1}{\sqrt{3}}\begin{pmatrix}-1\\-1\\1\end{pmatrix}$ .

对应 $\lambda_{2} = \lambda_{3} = 1$ ，解方程 $(A - E)x = 0$ ，由

$$
\boldsymbol {A} - \boldsymbol {E} = \left( \begin{array}{c c c} - 1 & - 1 & 1 \\ - 1 & - 1 & 1 \\ 1 & 1 & - 1 \end{array} \right) \stackrel {{r}} {{\sim}} \left( \begin{array}{c c c} 1 & 1 & - 1 \\ 0 & 0 & 0 \\ 0 & 0 & 0 \end{array} \right),
$$

得基础解系  $\boldsymbol{\xi}_{2}=\begin{pmatrix}-1\\1\\0\end{pmatrix},\boldsymbol{\xi}_{3}=\begin{pmatrix}1\\0\\1\end{pmatrix}.$

将 $\pmb{\xi}_2, \pmb{\xi}_3$ 正交化: 取 $\pmb{\eta}_2 = \pmb{\xi}_2$,

考研电子书网站:www.pdf2book.com

129

---

第 5 章 相似矩阵及二次型

$$
\boldsymbol {\eta} _ {3} = \boldsymbol {\xi} _ {3} - \frac {(\boldsymbol {\xi} _ {3} , \boldsymbol {\eta} _ {2})}{\| \boldsymbol {\eta} _ {2} \| ^ {2}} \boldsymbol {\eta} _ {2} = \left( \begin{array}{c} 1 \\ 0 \\ 1 \end{array} \right) + \frac {1}{2} \left( \begin{array}{c} - 1 \\ 1 \\ 0 \end{array} \right) = \frac {1}{2} \left( \begin{array}{c} 1 \\ 1 \\ 2 \end{array} \right).
$$

再将  $\eta_{2},\eta_{3}$  单位化, 得  $p_{2}=\frac{1}{\sqrt{2}}\begin{pmatrix}-1\\1\\0\end{pmatrix},p_{3}=\frac{1}{\sqrt{6}}\begin{pmatrix}1\\1\\2\end{pmatrix}.$

将 $p_{1},p_{2},p_{3}$ 构成正交矩阵

$$
\boldsymbol {P} = (\boldsymbol {p} _ {1}, \boldsymbol {p} _ {2}, \boldsymbol {p} _ {3}) = \left( \begin{array}{c c c} - \frac {1}{\sqrt {3}} & - \frac {1}{\sqrt {2}} & \frac {1}{\sqrt {6}} \\ - \frac {1}{\sqrt {3}} & \frac {1}{\sqrt {2}} & \frac {1}{\sqrt {6}} \\ \frac {1}{\sqrt {3}} & 0 & \frac {2}{\sqrt {6}} \end{array} \right),
$$

有

$$
\boldsymbol {P} ^ {- 1} \boldsymbol {A} \boldsymbol {P} = \boldsymbol {P} ^ {\mathrm{T}} \boldsymbol {A} \boldsymbol {P} = \boldsymbol {\Lambda} = \left( \begin{array}{c c c} - 2 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{array} \right).
$$

例 13 设  $A=\begin{pmatrix}2&-1\\-1&2\end{pmatrix}$ ，求  $A^{n}$ .

解 因 A 对称, 故 A 可对角化, 即有可逆矩阵 P 及对角矩阵 A, 使  $P^{-1}AP = A$ . 于是  $A = P\Lambda P^{-1}$ , 从而  $A^{n} = P\Lambda^{n}P^{-1}$ . 由

$$
\left| \boldsymbol {A} - \lambda \boldsymbol {E} \right| = \left| \begin{array}{c c} 2 - \lambda & - 1 \\ - 1 & 2 - \lambda \end{array} \right| = \lambda^ {2} - 4 \lambda + 3 = (\lambda - 1) (\lambda - 3),
$$

得 A 的特征值  $\lambda_{1}=1,\lambda_{2}=3$ . 于是

$$
\boldsymbol {\Lambda} = \left( \begin{array}{c c} 1 & 0 \\ 0 & 3 \end{array} \right), \quad \boldsymbol {\Lambda} ^ {n} = \left( \begin{array}{c c} 1 & 0 \\ 0 & 3 ^ {n} \end{array} \right).
$$

对应  $\lambda_{1}=1$ ，由  $A-E=\begin{pmatrix}1&-1\\ -1&1\end{pmatrix}\stackrel{r}{\sim}\begin{pmatrix}1&-1\\ 0&0\end{pmatrix}$ ，得  $\xi_{1}=\begin{pmatrix}1\\ 1\end{pmatrix}$ ;

对应  $\lambda_{2}=3$ ，由  $A-3E=\begin{pmatrix}-1&-1\\-1&-1\end{pmatrix}\stackrel{r}{\sim}\begin{pmatrix}1&1\\0&0\end{pmatrix}$ ，得  $\xi_{2}=\begin{pmatrix}1\\-1\end{pmatrix}$ .

并有  $\boldsymbol{P}=(\boldsymbol{\xi}_{1},\boldsymbol{\xi}_{2})=\begin{pmatrix}1&1\\ 1&-1\end{pmatrix}$ ，再求出  $P^{-1}=\frac{1}{2}\begin{pmatrix}1&1\\ 1&-1\end{pmatrix}$ .于是

$$
\boldsymbol {A} ^ {n} = \boldsymbol {P} \boldsymbol {\Lambda} ^ {n} \boldsymbol {P} ^ {- 1} = \frac {1}{2} \left( \begin{array}{c c} 1 & 1 \\ 1 & - 1 \end{array} \right) \left( \begin{array}{c c} 1 & 0 \\ 0 & 3 ^ {n} \end{array} \right) \left( \begin{array}{c c} 1 & 1 \\ 1 & - 1 \end{array} \right) = \frac {1}{2} \left( \begin{array}{c c} 1 + 3 ^ {n} & 1 - 3 ^ {n} \\ 1 - 3 ^ {n} & 1 + 3 ^ {n} \end{array} \right).
$$

130

![](raw/pages_0129-0160/images/page_133_image_17.jpg)

---

§ 5 二次型及其标准形

## § 5 二次型及其标准形

在解析几何中,为了便于研究二次曲线

$$
a x ^ {2} + b x y + c y ^ {2} = 1 \tag {4}
$$

的几何性质,可以选择适当的坐标旋转变换

$$
\left\{ \begin{array}{l} x = x ^ {\prime} \cos \theta - y ^ {\prime} \sin \theta , \\ y = x ^ {\prime} \sin \theta + y ^ {\prime} \cos \theta , \end{array} \right.
$$

把方程(4)化为标准形

$$
m x ^ {\prime 2} + n y ^ {r 2} = 1.
$$

(4)式的左边是一个二次齐次多项式,从代数学的观点看,化标准形的过程就是通过变量的线性变换化简一个二次齐次多项式,使它只含有平方项.这样一个问题,在许多理论问题或实际问题中常会遇到.现在我们把这类问题一般化,讨论n个变量的二次齐次多项式的化简问题.

定义 8 含有 n 个变量  $x_{1}, x_{2}, \cdots, x_{n}$  的二次齐次函数

$$
f \left(x _ {1}, x _ {2}, \dots , x _ {n}\right) = a _ {1 1} x _ {1} ^ {2} + a _ {2 2} x _ {2} ^ {2} + \dots + a _ {n n} x _ {n} ^ {2} + 2 a _ {1 2} x _ {1} x _ {2} + 2 a _ {1 3} x _ {1} x _ {3} + \dots + 2 a _ {n - 1, n} x _ {n - 1} x _ {n} \tag {5}
$$

称为二次型.

当 $j > i$ 时，取 $a_{ji} = a_{ij}$，则 $2a_{ij}x_{i}x_{j} = a_{ij}x_{i}x_{j} + a_{ji}x_{j}x_{i}$，于是(5)式可写成

$$
\begin{array}{l} f = a _ {1 1} x _ {1} ^ {2} + a _ {1 2} x _ {1} x _ {2} + \dots + a _ {1 n} x _ {1} x _ {n} + a _ {2 1} x _ {2} x _ {1} + a _ {2 2} x _ {2} ^ {2} + \dots + a _ {2 n} x _ {2} x _ {n} + \dots + a _ {n 1} x _ {n} x _ {1} + a _ {n 2} x _ {n} x _ {2} + \dots + a _ {n n} x _ {n} ^ {2} \\ = \sum_ {i, j = 1} ^ {n} a _ {i j} x _ {i} x _ {j}. \tag {6} \\ \end{array}
$$

当 $a_{ij}$ 为复数时, $f$ 称为复二次型; 当 $a_{ij}$ 为实数时, $f$ 称为实二次型. 这里, 我们仅讨论实二次型.

若二次型只含有平方项,则称为标准二次型(简称标准形);若二次型形如 $f=y_{1}^{2}+y_{2}^{2}+\cdots+y_{p}^{2}-y_{p+1}^{2}-y_{p+2}^{2}-\cdots-y_{r}^{2}$ ，则称为规范二次型(简称规范形).

利用矩阵,二次型(6)可表示为

$$
f = x _ {1} \left(a _ {1 1} x _ {1} + a _ {1 2} x _ {2} + \dots + a _ {1 n} x _ {n}\right) + x _ {2} \left(a _ {2 1} x _ {1} + a _ {2 2} x _ {2} + \dots + a _ {2 n} x _ {n}\right) + \dots + x _ {n} \left(a _ {n 1} x _ {1} + a _ {n 2} x _ {2} + \dots + a _ {n n} x _ {n}\right)
$$

$$
= (x _ {1}, x _ {2}, \dots , x _ {n}) \left( \begin{array}{c} a _ {1 1} x _ {1} + a _ {1 2} x _ {2} + \dots + a _ {1 n} x _ {n} \\ a _ {2 1} x _ {1} + a _ {2 2} x _ {2} + \dots + a _ {2 n} x _ {n} \\ \vdots \\ a _ {n 1} x _ {1} + a _ {n 2} x _ {2} + \dots + a _ {n n} x _ {n} \end{array} \right)
$$

考研电子书网站:www.pdf2book.com

131

---

第5章 相似矩阵及二次型

$$
= (x _ {1}, x _ {2}, \dots , x _ {n}) \left( \begin{array}{c c c c} a _ {1 1} & a _ {1 2} & \dots & a _ {1 n} \\ a _ {2 1} & a _ {2 2} & \dots & a _ {2 n} \\ \vdots & \vdots & & \vdots \\ a _ {n 1} & a _ {n 2} & \dots & a _ {n n} \end{array} \right) \left( \begin{array}{c} x _ {1} \\ x _ {2} \\ \vdots \\ x _ {n} \end{array} \right),
$$

记

$$
\boldsymbol {A} = \left( \begin{array}{c c c c} a _ {1 1} & a _ {1 2} & \dots & a _ {1 n} \\ a _ {2 1} & a _ {2 2} & \dots & a _ {2 n} \\ \vdots & \vdots & & \vdots \\ a _ {n 1} & a _ {n 2} & \dots & a _ {n n} \end{array} \right), \quad \boldsymbol {x} = \left( \begin{array}{c} x _ {1} \\ x _ {2} \\ \vdots \\ x _ {n} \end{array} \right),
$$

则二次型可用矩阵记作

$$
f = \boldsymbol {x} ^ {\mathrm{T}} \boldsymbol {A} \boldsymbol {x}, \tag {7}
$$

其中 A 为对称矩阵.

例如,二次型 $f=x^{2}-3z^{2}-4xy+yz$ 用矩阵记号写出来,就是

$$
f = (x, y, z) \left( \begin{array}{c c c} 1 & - 2 & 0 \\ - 2 & 0 & \frac {1}{2} \\ 0 & \frac {1}{2} & - 3 \end{array} \right) \left( \begin{array}{c} x \\ y \\ z \end{array} \right).
$$

任给一个二次型,就惟一地确定一个对称矩阵;反之,任给一个对称矩阵,也可惟一地确定一个二次型.这样,二次型与对称矩阵之间存在一一对应的关系.因此,我们把对称矩阵A叫做二次型f的矩阵,也把f叫做对称矩阵A的二次型.对称矩阵A的秩就叫做二次型f的秩.

对二次型,我们讨论的主要问题是:是否存在可逆的线性变换(若存在,如何寻找):

$$
\left\{ \begin{array}{l} x _ {1} = c _ {1 1} y _ {1} + c _ {1 2} y _ {2} + \dots + c _ {1 n} y _ {n}, \\ x _ {2} = c _ {2 1} y _ {1} + c _ {2 2} y _ {2} + \dots + c _ {2 n} y _ {n}, \\ \dots \dots \\ x _ {n} = c _ {n 1} y _ {1} + c _ {n 2} y _ {2} + \dots + c _ {n n} y _ {n}, \end{array} \right. \tag {8}
$$

使原二次型变成标准形.

记 $C = (c_{ij})$ ，把可逆变换(8)记作

$$
x = C y,
$$

代入(7)式,有 $f=x^{T}Ax=(Cy)^{T}ACy=y^{T}(C^{T}AC)y$ .

定义9 设 $A$ 和 $B$ 是 $n$ 阶矩阵, 若有可逆矩阵 $C$, 使 $B = C^{\mathrm{T}}AC$, 则称矩阵 $A$ 与 $B$ 合同.

132

---

§ 5 二次型及其标准形

显然, 若 A 为对称矩阵, 则  $B = C^{T} AC$  也为对称矩阵, 且  $R(B) = R(A)$ . 事实上,

$$
\boldsymbol {B} ^ {\mathrm{T}} = (\boldsymbol {C} ^ {\mathrm{T}} \boldsymbol {A} \boldsymbol {C}) ^ {\mathrm{T}} = \boldsymbol {C} ^ {\mathrm{T}} \boldsymbol {A} ^ {\mathrm{T}} \boldsymbol {C} = \boldsymbol {C} ^ {\mathrm{T}} \boldsymbol {A} \boldsymbol {C} = \boldsymbol {B},
$$

即 $\pmb{B}$ 为对称矩阵. 又因 $B = C^{\mathrm{T}}AC$ ，而 $C$ 可逆，从而 $C^{\mathrm{T}}$ 也可逆，由矩阵秩的性质即知 $R(B) = R(A)$.

由此可知,经可逆变换 x = Cy 后,二次型 f 的矩阵由 A 变为与 A 合同的矩阵  $C^{T}AC$ ,且二次型的秩不变.

要使二次型 $f$ 经可逆变换 $\pmb {x} = \pmb{C}\pmb{y}$ 变成标准形，这就是要使

$$
\mathbf {y} ^ {\mathrm{T}} \boldsymbol {C} ^ {\mathrm{T}} \boldsymbol {A} \boldsymbol {C} \mathbf {y} = k _ {1} y _ {1} ^ {2} + k _ {2} y _ {2} ^ {2} + \dots + k _ {n} y _ {n} ^ {2} = (y _ {1}, y _ {2}, \dots , y _ {n}) \left( \begin{array}{c c c c} k _ {1} & & & \\ & k _ {2} & & \\ & & \ddots & \\ & & & k _ {n} \end{array} \right) \left( \begin{array}{c} y _ {1} \\ y _ {2} \\ \vdots \\ y _ {n} \end{array} \right),
$$

也就是要使 $C^{\mathrm{T}}AC$ 成为对角矩阵. 因此, 我们的主要问题就是: 对于对称矩阵 $A$, 是否存在可逆矩阵 $C$, 使 $C^{\mathrm{T}}AC$ 为对角矩阵. 这个问题称为把对称矩阵 $A$ 合同对角化.

由上节定理5知,任给对称矩阵A,总有正交矩阵P,使 $P^{-1}AP=\Lambda$ ,即 $P^{T}AP=\Lambda$ .把此结论应用于二次型,即有

定理6 任给二次型 $f = \sum_{i,j=1}^{n} a_{ij} x_i x_j$ ($a_{ij} = a_{ji}$)，总有正交变换 $x = Py$，使 $f$ 化为标准形

$$
f = \lambda_ {1} y _ {1} ^ {2} + \lambda_ {2} y _ {2} ^ {2} + \dots + \lambda_ {n} y _ {n} ^ {2},
$$

其中  $\lambda_{1},\lambda_{2},\cdots,\lambda_{n}$  是 f 的矩阵  $A=(a_{ij})$  的特征值.

推论 任给 $n$ 元二次型 $f(x) = x^{\mathrm{T}}Ax$ ($A^{\mathrm{T}} = A$), 总有可逆变换 $x = Cz$, 使 $f(Cz)$ 为规范形.

证 按定理6,有

$$
f (\boldsymbol {P} \boldsymbol {y}) = \boldsymbol {y} ^ {\mathrm{T}} \boldsymbol {\Lambda} \boldsymbol {y} = \lambda_ {1} y _ {1} ^ {2} + \lambda_ {2} y _ {2} ^ {2} + \dots + \lambda_ {n} y _ {n} ^ {2}.
$$

设二次型 $f$ 的秩为 $r$, 则特征值 $\lambda_{i}$ 中恰有 $r$ 个不为 0, 无妨设 $\lambda_{1}, \lambda_{2}, \cdots, \lambda_{r}$ 不等于 0, $\lambda_{r+1} = \lambda_{r+2} = \cdots = \lambda_{n} = 0$. 令

$$
\boldsymbol {K} = \left( \begin{array}{c c c c} k _ {1} & & & \\ & k _ {2} & & \\ & & \ddots & \\ & & & k _ {n} \end{array} \right),
$$

其中

$$
k _ {i} = \left\{ \begin{array}{c c} \frac {1}{\sqrt {| \lambda_ {i} |}}, i \leqslant r, \\ 1, & i > r, \end{array} \right.
$$

考研电子书网站:www.pdf2book.com

133

---

第5章 相似矩阵及二次型

则 K 可逆, 变换 y = Kz 把  $f(Py)$  化为

$$
f (\boldsymbol {P} \boldsymbol {K} z) = z ^ {\mathrm{T}} \boldsymbol {K} ^ {\mathrm{T}} \boldsymbol {P} ^ {\mathrm{T}} \boldsymbol {A} \boldsymbol {P} \boldsymbol {K} z = z ^ {\mathrm{T}} \boldsymbol {K} ^ {\mathrm{T}} \boldsymbol {\Lambda} \boldsymbol {K} z,
$$

而

$$
\boldsymbol {K} ^ {\mathrm{T}} \boldsymbol {\Lambda} \boldsymbol {K} = \operatorname{diag} \left(\frac {\lambda_ {1}}{| \lambda_ {1} |}, \frac {\lambda_ {2}}{| \lambda_ {2} |}, \dots , \frac {\lambda_ {r}}{| \lambda_ {r} |}, 0, \dots , 0\right).
$$

记 $C = PK$ ，即知可逆变换 $\pmb {x} = \pmb{Cz}$ 把 $f$ 化成规范形

$$
f (\boldsymbol {C} z) = \frac {\lambda_ {1}}{| \lambda_ {1} |} z _ {1} ^ {2} + \frac {\lambda_ {2}}{| \lambda_ {2} |} z _ {2} ^ {2} + \dots + \frac {\lambda_ {r}}{| \lambda_ {r} |} z _ {r} ^ {2}.
$$

证毕

例14 求一个正交变换 $x = Py$ ，把二次型

$$
f = - 2 x _ {1} x _ {2} + 2 x _ {1} x _ {3} + 2 x _ {2} x _ {3}
$$

化为标准形.

解 二次型 $f$ 的矩阵为

$$
\boldsymbol {A} = \left( \begin{array}{c c c} 0 & - 1 & 1 \\ - 1 & 0 & 1 \\ 1 & 1 & 0 \end{array} \right),
$$

这与例 12 所给矩阵相同. 按例 12 的结果, 有正交矩阵

$$
\boldsymbol {P} = \left( \begin{array}{c c c} - \frac {1}{\sqrt {3}} & - \frac {1}{\sqrt {2}} & \frac {1}{\sqrt {6}} \\ - \frac {1}{\sqrt {3}} & \frac {1}{\sqrt {2}} & \frac {1}{\sqrt {6}} \\ \frac {1}{\sqrt {3}} & 0 & \frac {2}{\sqrt {6}} \end{array} \right),
$$

使

$$
\boldsymbol {P} ^ {\mathrm{T}} \boldsymbol {A} \boldsymbol {P} = \boldsymbol {\Lambda} = \left( \begin{array}{c c c} - 2 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{array} \right),
$$

于是有正交变换

$$
\left( \begin{array}{c} x _ {1} \\ x _ {2} \\ x _ {3} ^ {\prime} \end{array} \right) = \left( \begin{array}{c c c} - \frac {1}{\sqrt {3}} & - \frac {1}{\sqrt {2}} & \frac {1}{\sqrt {6}} \\ - \frac {1}{\sqrt {3}} & \frac {1}{\sqrt {2}} & \frac {1}{\sqrt {6}} \\ \frac {1}{\sqrt {3}} & 0 & \frac {2}{\sqrt {6}} \end{array} \right) \left( \begin{array}{c} y _ {1} \\ y _ {2} \\ y _ {3} \end{array} \right),
$$

把二次型 $f$ 化成标准形

134

---

§6 用配方法化二次型成标准形

$$
f = - 2 y _ {1} ^ {2} + y _ {2} ^ {2} + y _ {3} ^ {2}.
$$

如果要把二次型 $f$ 化成规范形，只需令

$$
\left\{ \begin{array}{l} y _ {1} = \frac {1}{\sqrt {2}} z _ {1}, \\ y _ {2} = \quad z _ {2}, \\ y _ {3} = \quad z _ {3}, \end{array} \right.
$$

即得 $f$ 的规范形

$$
f = - z _ {1} ^ {2} + z _ {2} ^ {2} + z _ {3} ^ {2}.
$$

## § 6 用配方法化二次型成标准形

用正交变换化二次型成标准形,具有保持几何形状不变的优点.如果不限于用正交变换,那么还可以有多种方法(对应有多个可逆的线性变换)把二次型化成标准形.这里只介绍拉格朗日配方法,下面举例来说明这种方法.

例15 化二次型

$$
f = x _ {1} ^ {2} + 2 x _ {2} ^ {2} + 5 x _ {3} ^ {2} + 2 x _ {1} x _ {2} + 2 x _ {1} x _ {3} + 6 x _ {2} x _ {3}
$$

成标准形,并求所用的变换矩阵.

解 由于 $f$ 中含变量 $x_{1}$ 的平方项, 故把含 $x_{1}$ 的项归并起来, 配方可得

$$
\begin{array}{l} f = x _ {1} ^ {2} + 2 x _ {1} x _ {2} + 2 x _ {1} x _ {3} + 2 x _ {2} ^ {2} + 5 x _ {3} ^ {2} + 6 x _ {2} x _ {3} \\ = \left(x _ {1} + x _ {2} + x _ {3}\right) ^ {2} - x _ {2} ^ {2} - x _ {3} ^ {2} - 2 x _ {2} x _ {3} + 2 x _ {2} ^ {2} + 5 x _ {3} ^ {2} + 6 x _ {2} x _ {3} \\ = \left(x _ {1} + x _ {2} + x _ {3}\right) ^ {2} + x _ {2} ^ {2} + 4 x _ {2} x _ {3} + 4 x _ {3} ^ {2}, \\ \end{array}
$$

上式右端除第一项外已不再含 $x_{1}$. 继续配方, 可得

$$
f = \left(x _ {1} + x _ {2} + x _ {3}\right) ^ {2} + \left(x _ {2} + 2 x _ {3}\right) ^ {2}.
$$

令 $\left\{\begin{aligned}y_{1}&=x_{1}+x_{2}+x_{3},\\ y_{2}&=x_{2}+2x_{3},\\ y_{3}&=x_{3},\end{aligned}\right.\quad\left\{\begin{aligned}x_{1}&=y_{1}-y_{2}+y_{3},\\ x_{2}&=y_{2}-2y_{3},\\ x_{3}&=y_{3},\end{aligned}\right.$ 就把f化成标准形(规范形) $f=y_{1}^{2}+y_{2}^{2}$ ，所用

变换矩阵为

$$
\boldsymbol {C} = \left( \begin{array}{c c c} 1 & - 1 & 1 \\ 0 & 1 & - 2 \\ 0 & 0 & 1 \end{array} \right) \quad (| \boldsymbol {C} | = 1 \neq 0).
$$

例16 化二次型

$$
f = 2 x _ {1} x _ {2} + 2 x _ {1} x _ {3} - 6 x _ {2} x _ {3}
$$

成规范形,并求所用的变换矩阵.

考研电子书网站:www.pdf2book.com

135

---

第 5 章 相似矩阵及二次型

解 在 $f$ 中不含平方项. 由于含有 $x_{1}x_{2}$ 乘积项, 故令

$$
\left\{ \begin{array}{l} x _ {1} = y _ {1} + y _ {2}, \\ x _ {2} = y _ {1} - y _ {2}, \\ x _ {3} = y _ {3}, \end{array} \right.
$$

代入可得

$$
f = 2 y _ {1} ^ {2} - 2 y _ {2} ^ {2} - 4 y _ {1} y _ {3} + 8 y _ {2} y _ {3}.
$$

再配方,得

$$
f = 2 (y _ {1} - y _ {3}) ^ {2} - 2 (y _ {2} - 2 y _ {3}) ^ {2} + 6 y _ {3} ^ {2}.
$$

令 $\left\{\begin{aligned}z_{1}&=\sqrt{2}\left(y_{1}-y_{3}\right),\\ z_{2}&=\sqrt{2}\left(y_{2}-2y_{3}\right),\\ z_{3}&=\sqrt{6}y_{3},\end{aligned}\right.$  即 $\left\{\begin{aligned}y_{1}&=\frac{1}{\sqrt{2}}z_{1}+\frac{1}{\sqrt{6}}z_{3},\\ y_{2}&=\frac{1}{\sqrt{2}}z_{2}+\frac{2}{\sqrt{6}}z_{3},\\ y_{3}&=\frac{1}{\sqrt{6}}z_{3},\end{aligned}\right.$  就把f化成规范形

$$
f = z _ {1} ^ {2} - z _ {2} ^ {2} + z _ {3} ^ {2},
$$

所用变换矩阵为

$$
\boldsymbol {C} = \left( \begin{array}{c c c} 1 & 1 & 0 \\ 1 & - 1 & 0 \\ 0 & 0 & 1 \end{array} \right) \left( \begin{array}{c c c} \frac {1}{\sqrt {2}} & 0 & \frac {1}{\sqrt {6}} \\ 0 & \frac {1}{\sqrt {2}} & \frac {2}{\sqrt {6}} \\ 0 & 0 & \frac {1}{\sqrt {6}} \end{array} \right) = \left( \begin{array}{c c c} \frac {1}{\sqrt {2}} & \frac {1}{\sqrt {2}} & \frac {3}{\sqrt {6}} \\ \frac {1}{\sqrt {2}} & - \frac {1}{\sqrt {2}} & - \frac {1}{\sqrt {6}} \\ 0 & 0 & \frac {1}{\sqrt {6}} \end{array} \right) (| \boldsymbol {C} | = - \frac {1}{\sqrt {6}} \neq 0).
$$

一般地,任何二次型都可用上面两例的方法找到可逆变换,把二次型化成标准形(或规范形).

## § 7 正定二次型

二次型的标准形显然不是惟一的,只是标准形中所含项数是确定的(即是二次型的秩).不仅如此,在限定变换为实变换时,标准形中正系数的个数是不变的(从而负系数的个数也不变),也就是有

定理7 设二次型 $f = x^{\mathrm{T}}Ax$ 的秩为 $r$, 且有两个可逆变换

$$
x = C y \quad {\text {及}} \quad x = P z
$$

136

---

§7 正定二次型

使

$$
f = k _ {1} y _ {1} ^ {2} + k _ {2} y _ {2} ^ {2} + \dots + k _ {r} y _ {r} ^ {2} \quad (k _ {i} \neq 0)
$$

及

$$
f = \lambda_ {1} z _ {1} ^ {2} + \lambda_ {2} z _ {2} ^ {2} + \dots + \lambda_ {r} z _ {r} ^ {2} \quad (\lambda_ {i} \neq 0),
$$

则  $k_{1}, k_{2}, \cdots, k_{r}$  中正数的个数与  $\lambda_{1}, \lambda_{2}, \cdots, \lambda_{r}$  中正数的个数相等.

这个定理称为惯性定理,这里不予证明.

二次型的标准形中正系数的个数称为二次型的正惯性指数,负系数的个数称为负惯性指数.若二次型f的正惯性指数为p,秩为r,则f的规范形便可确定为

$$
f = y _ {1} ^ {2} + y _ {2} ^ {2} + \dots + y _ {p} ^ {2} - y _ {p + 1} ^ {2} - \dots - y _ {r} ^ {2}.
$$

科学技术上用得较多的二次型是正惯性指数为 $n$ 或负惯性指数为 $n$ 的 $n$ 元二次型, 我们有下述定义.

定义 10 设二次型 $f(x) = x^{\mathrm{T}}Ax$，若对任何 $x \neq 0$，都有 $f(x) > 0$（显然 $f(0) = 0$），则称 $f$ 为正定二次型，并称对称矩阵 $A$ 是正定的；如果对任何 $x \neq 0$ 都有 $f(x) < 0$，则称 $f$ 为负定二次型，并称对称矩阵 $A$ 是负定的。

定理8 $n$ 元二次型 $f = x^{\mathrm{T}}Ax$ 为正定的充分必要条件是:它的标准形的 $n$ 个系数全为正，即它的规范形的 $n$ 个系数全为1，亦即它的正惯性指数等于 $n$. 公众号:旗胜考研

证 设可逆变换 $x = Cy$ 使

$$
f (\boldsymbol {x}) = f (\boldsymbol {C y}) = \sum_ {i = 1} ^ {n} k _ {i} y _ {i} ^ {2}.
$$

先证充分性. 设  $k_{i}>0\ (i=1,2,\cdots,n)$ . 任给  $x\neq0$ , 则  $y=C^{-1}x\neq0$ , 故

$$
f (\boldsymbol {x}) = \sum_ {i = 1} ^ {n} k _ {i} y _ {i} ^ {2} > 0.
$$

再证必要性.用反证法.假设有 $k_{s} \leqslant 0$, 则当 $y = e_{s}$ (单位坐标向量)时, $f(Ce_{s}) = k_{s} \leqslant 0$. 显然 $Ce_{s} \neq 0$, 这与 $f$ 为正定相矛盾.这就证明了 $k_{i} > 0 (i = 1,2,\dots,n)$. 证毕

推论 对称矩阵 A 为正定的充分必要条件是: A 的特征值全为正.

定理9 对称矩阵 $A$ 为正定的充分必要条件是: $A$ 的各阶顺序主子式都为正, 即

$$
a _ {1 1} > 0, \quad \left| \begin{array}{c c} a _ {1 1} & a _ {1 2} \\ a _ {2 1} & a _ {2 2} \end{array} \right| > 0, \dots , \quad \left| \begin{array}{c c c c} a _ {1 1} & a _ {1 2} & \dots & a _ {1 n} \\ a _ {2 1} & a _ {2 2} & \dots & a _ {2 n} \\ \vdots & \vdots & & \vdots \\ a _ {n 1} & a _ {n 2} & \dots & a _ {n n} \end{array} \right| > 0,
$$

对称矩阵 A 为负定的充分必要条件是: 奇数阶顺序主子式为负, 而偶数阶顺序主子式为正, 即

概念异同

考研电子书网站:www.pdf2book.com

137

---

第5章 相似矩阵及二次型

$$
\left(- 1\right) ^ {r} \left| \begin{array}{c c c c} a _ {1 1} & a _ {1 2} & \dots & a _ {1 r} \\ a _ {2 1} & a _ {2 2} & \dots & a _ {2 n} \\ \vdots & \vdots & & \vdots \\ a _ {r 1} & a _ {r 2} & \dots & a _ {r r} \end{array} \right| > 0 \quad (r = 1, 2, \dots , n).
$$

这个定理称为赫尔维茨定理,这里不予证明.

例 17 判定二次型  $f = -5x^{2} - 6y^{2} - 4z^{2} + 4xy + 4xz$  的正定性.

解 $f$ 的矩阵为

$$
A = \left( \begin{array}{c c c} {- 5} & {2} & {2} \\ {2} & {- 6} & {0} \\ {2} & {0} & {- 4} \end{array} \right),
$$

其中

$$
a _ {1 1} = - 5 <   0, \quad \left| \begin{array}{c c} a _ {1 1} & a _ {1 2} \\ a _ {2 1} & a _ {2 2} \end{array} \right| = \left| \begin{array}{c c} - 5 & 2 \\ 2 & - 6 \end{array} \right| = 2 6 > 0, \quad | A | = - 8 0 <   0,
$$

根据定理9知 $f$ 为负定.

设 $f(x,y)$ 是二元正定二次型，则 $f(x,y) = c$ （$c > 0$ 为常数）的图形是以原点为中心的椭圆.当把 $c$ 看作任意常数时则是一族椭圆，这族椭圆随着 $c\to 0$ 而收缩到原点.当 $f$ 为三元正定二次型时， $f(x,y,z) = c$ （$c > 0$）的图形是一族椭球.

## 习题五

1. 设  $a=\begin{pmatrix}1\\0\\-2\end{pmatrix},b=\begin{pmatrix}-4\\2\\3\end{pmatrix}$ ，c 与 a 正交，且  $b=\lambda a+c$ ，求  $\lambda$  和 c.

2. 试把下列向量组施密特正交化,然后再单位化:

$$
(a _ {1}, a _ {2}, a _ {3}) = \left( \begin{array}{c c c} 1 & 1 & 1 \\ 1 & 2 & 4 \\ 1 & 3 & 9 \end{array} \right);
$$

$$
(a _ {1}, a _ {2}, a _ {3}) = \left( \begin{array}{r r r} 1 & 1 & - 1 \\ 0 & - 1 & 1 \\ - 1 & 0 & 1 \\ 1 & 1 & 0 \end{array} \right). \tag {2}
$$

3. 下列矩阵是不是正交矩阵？并说明理由:

$$
\left( \begin{array}{c c c} 1 & - \frac {1}{2} & \frac {1}{3} \\ - \frac {1}{2} & 1 & \frac {1}{2} \\ \frac {1}{3} & \frac {1}{2} & - 1 \end{array} \right); \tag {1}
$$

$$
\left( \begin{array}{c c c} \frac {1}{9} & - \frac {8}{9} & - \frac {4}{9} \\ - \frac {8}{9} & \frac {1}{9} & - \frac {4}{9} \\ - \frac {4}{9} & - \frac {4}{9} & \frac {7}{9} \end{array} \right). \tag {2}
$$

138

---

习题五

4.（1）设 $x$ 为 $n$ 维列向量，$x^{\mathrm{T}}x = 1$，令 $H = E - 2xx^{\mathrm{T}}$，证明 $H$ 是对称的正交矩阵；

(2) 设 A, B 都是正交矩阵, 证明 AB 也是正交矩阵.

5. 设 $a_1, a_2, a_3$ 为两两正交的单位向量组，$b_1 = -\frac{1}{3} a_1 + \frac{2}{3} a_2 + \frac{2}{3} a_3, b_2 = \frac{2}{3} a_1 + \frac{2}{3} a_2 - \frac{1}{3} a_3, b_3 = -\frac{2}{3} a_1 + \frac{1}{3} a_2 - \frac{2}{3} a_3$，证明 $b_1, b_2, b_3$ 也是两两正交的单位向量组。

6. 求下列矩阵的特征值和特征向量:

(1) $\begin{pmatrix}2&-1&2\\5&-3&3\\-1&0&-2\end{pmatrix};$

(2) $\begin{pmatrix}1&2&3\\2&1&3\\3&3&6\end{pmatrix};$

(3) $\begin{pmatrix}0&0&0&1\\0&0&1&0\\0&1&0&0\\1&0&0&0\end{pmatrix}.$

7. 设 A 为 n 阶矩阵, 证明  $A^{T}$  与 A 的特征值相同.

8. 设 $n$ 阶矩阵 $A, B$ 满足 $R(A) + R(B) < n$, 证明 $A$ 与 $B$ 有公共的特征值和公共的特征向量.

9. 设 $A^2 - 3A + 2E = O$，证明 $A$ 的特征值只能取 1 或 2.

10. 设 A 为正交矩阵, 且  $\left|A\right| = -1$ , 证明  $\lambda = -1$  是 A 的特征值.

11. 设 $\lambda \neq 0$ 是 $m$ 阶矩阵 $A_{m \times n} B_{n \times m}$ 的特征值, 证明 $\lambda$ 也是 $n$ 阶矩阵 $BA$ 的特征值.

12. 已知 3 阶矩阵 A 的特征值为 1, 2, 3, 求  $\left|A^{3}-5A^{2}+7A\right|$ .

13. 已知 3 阶矩阵 A 的特征值为 1,2,-3, 求  $\left|A^{*}+3A+2E\right|$ .

14. 设 A, B 都是 n 阶矩阵, 且 A 可逆, 证明 AB 与 BA 相似.

15. 设矩阵  $A=\begin{pmatrix}2&0&1\\3&1&x\\4&0&5\end{pmatrix}$  可相似对角化, 求 x.

16. 已知  $p=\begin{pmatrix}1\\1\\-1\end{pmatrix}$  是矩阵  $A=\begin{pmatrix}2&-1&2\\5&a&3\\-1&b&-2\end{pmatrix}$  的一个特征向量，

(1) 求参数 a, b 及特征向量 p 所对应的特征值；

(2) 问 A 能不能相似对角化？并说明理由.

17. 设  $A=\begin{pmatrix}1&4&2\\0&-3&4\\0&4&3\end{pmatrix}$ ，求  $A^{100}$ .

18. 在某国, 每年有比例为 $p$ 的农村居民移居城镇, 有比例为 $q$ 的城镇居民移居农村. 假设该国总人口数不变, 且上述人口迁移的规律也不变. 把 $n$ 年后农村人口和城镇人口占总人口的比例依次记为 $x_{n}$ 和 $y_{n} (x_{n} + y_{n} = 1)$.

(1) 求关系式  $\begin{pmatrix} x_{n+1} \\ y_{n+1} \end{pmatrix} = A \begin{pmatrix} x_n \\ y_n \end{pmatrix}$  中的矩阵 A;

(2) 设目前农村人口与城镇人口相等, 即  $\begin{pmatrix} x_{0} \\ y_{0} \end{pmatrix} = \begin{pmatrix} 0.5 \\ 0.5 \end{pmatrix}$ , 求  $\begin{pmatrix} x_{n} \\ y_{n} \end{pmatrix}$ .

考研电子书网站:www.pdf2book.com

139

---

第 5 章 相似矩阵及二次型

19. 试求一个正交的相似变换矩阵, 将下列对称矩阵化为对角矩阵:

(1) $\begin{pmatrix}2&-2&0\\-2&1&-2\\0&-2&0\end{pmatrix};$  (2) $\begin{pmatrix}2&2&-2\\2&5&-4\\-2&-4&5\end{pmatrix}.$

20. 设矩阵  $A = \begin{pmatrix} 1 & -2 & -4 \\ -2 & x & -2 \\ -4 & -2 & 1 \end{pmatrix}$  与  $\Lambda = \begin{pmatrix} 5 & & \\ & -4 & \\ & & y \end{pmatrix}$  相似，求 x, y；并求一个正交矩阵 P，使  $P^{-1}AP = \Lambda$ .

21. 设 3 阶矩阵 A 的特征值为  $\lambda_{1}=2, \lambda_{2}=-2, \lambda_{3}=1$ ，对应的特征向量依次为

$$
\boldsymbol {p} _ {1} = \left( \begin{array}{c} 0 \\ 1 \\ 1 \end{array} \right), \quad \boldsymbol {p} _ {2} = \left( \begin{array}{c} 1 \\ 1 \\ 1 \end{array} \right), \quad \boldsymbol {p} _ {3} = \left( \begin{array}{c} 1 \\ 1 \\ 0 \end{array} \right),
$$

求 A.

22. 设 3 阶对称矩阵 A 的特征值为  $\lambda_{1}=1,\lambda_{2}=-1,\lambda_{3}=0$ ，对应  $\lambda_{1},\lambda_{2}$  的特征向量依次为

$$
\boldsymbol {p} _ {1} = \left( \begin{array}{c} 1 \\ 2 \\ 2 \end{array} \right), \quad \boldsymbol {p} _ {2} = \left( \begin{array}{c} 2 \\ 1 \\ - 2 \end{array} \right),
$$

求A.

23. 设 3 阶对称矩阵 A 的特征值为  $\lambda_{1}=6, \lambda_{2}=\lambda_{3}=3$ ，与特征值  $\lambda_{1}=6$  对应的特征向量为  $p_{1}=(1,1,1)^{\mathrm{T}}$ ，求 A.

24. 设  $\boldsymbol{a}=(a_{1},a_{2},\cdots,a_{n})^{\mathrm{T}}, a_{1}\neq0, A=\boldsymbol{a}\boldsymbol{a}^{\mathrm{T}}$

(1) 证明  $\lambda=0$  是 A 的 n-1 重特征值；
(2) 求 A 的非零特征值及 n 个线性无关的特征向量.

25. 设 A, B 均为 n 阶方阵, 证明  $\mathrm{tr}(AB)=\mathrm{tr}(BA)$ .

26. (1) 设  $A = \begin{pmatrix} 3 & -2 \\ -2 & 3 \end{pmatrix}$ ，求  $\varphi(A) = A^{10} - 5A^{9}$ ;

(2) 设  $A = \begin{pmatrix} 2 & 1 & 2 \\ 1 & 2 & 2 \\ 2 & 2 & 1 \end{pmatrix}$ ，求  $\varphi(A) = A^{10} - 6A^{9} + 5A^{8}$ .

27. 用矩阵记号表示下列二次型:

(1)  $f = x^{2} + 4xy + 4y^{2} + 2xz + z^{2} + 4yz;$

(2) $f = x^{2} + y^{2} - 7z^{2} - 2xy - 4xz - 4yz$;

(3) $f = x_{1}^{2} + x_{2}^{2} + x_{3}^{2} - 2x_{1}x_{2} + 6x_{2}x_{3}.$

28. 写出下列二次型的矩阵:

(1) $f(\boldsymbol{x}) = \boldsymbol{x}^{\mathrm{T}}\begin{pmatrix} 2 & 1 \\ 3 & 1 \end{pmatrix} \boldsymbol{x}$;

(2) $f(\boldsymbol{x}) = \boldsymbol{x}^{\mathrm{T}}\begin{pmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \\ 7 & 8 & 9 \end{pmatrix}\boldsymbol{x}.$

140

---

习题五

29. 求一个正交变换化下列二次型成标准形:

(1) $f=2x_{1}^{2}+3x_{2}^{2}+3x_{3}^{2}+4x_{2}x_{3};$

(2) $f = x_{1}^{2} + x_{3}^{2} + 2x_{1}x_{2} - 2x_{2}x_{3}.$

30. 求一个正交变换把二次曲面的方程

$$
3 x ^ {2} + 5 y ^ {2} + 5 z ^ {2} + 4 x y - 4 x z - 1 0 y z = 1
$$

化成标准方程.

31. 证明:二次型 $f = x^{\mathrm{T}}Ax$ 在 $\| x \| = 1$ 时的最大值为矩阵 $A$ 的最大特征值.

32. 用配方法化下列二次型成规范形,并写出所用变换的矩阵:

(1) $f(x_{1},x_{2},x_{3}) = x_{1}^{2} + 3x_{2}^{2} + 5x_{3}^{2} + 2x_{1}x_{2} - 4x_{1}x_{3};$
(2) $f(x_{1},x_{2},x_{3})=x_{1}^{2}+2x_{3}^{2}+2x_{1}x_{3}+2x_{2}x_{3};$
(3) $f(x_{1},x_{2},x_{3})=2x_{1}^{2}+x_{2}^{2}+4x_{3}^{2}+2x_{1}x_{2}-2x_{2}x_{3}.$

33. 设 $f = x_{1}^{2} + x_{2}^{2} + 5x_{3}^{2} + 2ax_{1}x_{2} - 2x_{1}x_{3} + 4x_{2}x_{3}$ 为正定二次型, 求 $a$.

34. 判定下列二次型的正定性:

(1) $f = -2x_{1}^{2} - 6x_{2}^{2} - 4x_{3}^{2} + 2x_{1}x_{2} + 2x_{1}x_{3}$;

(2) $f = x_{1}^{2} + 3x_{2}^{2} + 9x_{3}^{2} - 2x_{1}x_{2} + 4x_{1}x_{3}.$

35. 证明对称矩阵 A 为正定的充分必要条件是: 存在可逆矩阵 U, 使  $A = U^{T}U$ , 即 A 与单位矩阵 E 合同.

考研电子书网站:www.pdf2book.com

141

---

The quick brown fox jumps over the lazy dog.

## \* 第6章

## 线性空间与线性变换

向量空间又称线性空间,是线性代数中一个最基本的概念.在第4章中,我们把有序数组叫做向量,并介绍过向量空间的概念.在这一章中,我们要把这些概念推广,使向量及向量空间的概念更具一般性.当然,推广后的向量概念也就更加抽象化了.

## § 1 线性空间的定义与性质

定义1 设 $V$ 是一个非空集合, $\mathbb{R}$ 为实数域. 如果在 $V$ 中定义了一个加法, 即对于任意两个元素 $\alpha, \beta \in V$, 总有惟一的一个元素 $\gamma \in V$ 与之对应, 称为 $\alpha$ 与 $\beta$ 的和, 记作 $\gamma = \alpha + \beta$; 在 $V$ 中又定义了一个数与元素的乘法 (简称数乘), 即对于任一数 $\lambda \in \mathbb{R}$ 与任一元素 $\alpha \in V$, 总有惟一的一个元素 $\delta \in V$ 与之对应, 称为 $\lambda$ 与 $\alpha$ 的数量乘积, 记作 $\delta = \lambda \alpha$, 并且这两种运算满足以下八条运算规律 (设 $\alpha, \beta, \gamma \in V, \lambda, \mu \in \mathbb{R}$):

(i)  $\alpha+\beta=\beta+\alpha;$
(ii)  $(\alpha+\beta)+\gamma=\alpha+(\beta+\gamma)$ ;
(iii) 在 V 中存在零元素0, 对任何  $\alpha \in V$ , 都有  $\alpha + 0 = \alpha$ ;
(iv) 对任何  $\alpha \in V$ ，都有  $\alpha$  的负元素  $\beta \in V$ ，使  $\alpha + \beta = 0$ ;
(v)  $1\alpha=\alpha;$
(vi)  $\lambda(\mu\alpha)=(\lambda\mu)\alpha;$
(vii)  $(\lambda + \mu)\alpha = \lambda\alpha + \mu\alpha;$
(viii)  $\lambda(\boldsymbol{\alpha}+\boldsymbol{\beta})=\lambda\boldsymbol{\alpha}+\lambda\boldsymbol{\beta}$ ,

那么, $V$ 就称为(实数域 $\mathbb{R}$ 上的)线性空间(或向量空间), 借助几何语言, $V$ 中的元素不论其本来的性质如何, 可统称为向量.

简言之,凡满足上述八条规律的加法及数乘运算,就称为线性运算;凡定义了线性运算的集合,就称向量空间,其中的元素就称为向量.

142

---

§1 线性空间的定义与性质

这八条规律中,规律(i)与(ii)是我们熟知的加法的交换律和结合律,而规律(iii)和(iv)则保证了加法有逆运算,即

$$
\text {若} \alpha + \beta = \gamma , \beta \text {的负元素为} \delta , \text {则} \gamma + \delta = \alpha ;
$$

规律(vi)、(vii)、(viii)是数乘的结合律和分配律,而规律(v)则保证了非零数乘有逆运算,即

$$
\text {当} \lambda \neq 0 \text {时,若} \lambda \alpha = \beta , \text {则} \frac {1}{\lambda} \beta = \alpha .
$$

在第 4 章中, 我们把有序数组称为向量, 并对它定义了加法和数乘运算, 容易验证这些运算满足上述八条规律. 最后, 把对于运算为封闭的有序数组的集合称为向量空间. 显然, 那些只是现在定义的特殊情形. 比较起来, 现在的定义有了很大的推广:

1. 向量不一定是有序数组；

2. 向量空间中的运算只要求满足上述八条运算规律,当然也就不一定是有序数组的加法及数乘运算.

下面举一些例子.

例1 次数不超过 $n$ 的多项式的全体，记作 $P[x]_n$ ，即

$$
P [ x ] _ {n} = \left\{a _ {n} x ^ {n} + a _ {n - 1} x ^ {n - 1} + \dots + a _ {1} x + a _ {0} \mid a _ {n}, a _ {n - 1}, \dots , a _ {1}, a _ {0} \in \mathbb {R} \right\},
$$

对于通常的多项式加法、数乘多项式的乘法构成向量空间.这是因为:通常的多项式加法、数乘多项式的乘法两种运算显然满足线性运算规律,故只要验证 $P[x]_{n}$ 对运算封闭:

$$
(a _ {n} x ^ {n} + \dots + a _ {1} x + a _ {0}) + (b _ {n} x ^ {n} + \dots + b _ {1} x + b _ {0}) = (a _ {n} + b _ {n}) x ^ {n} + \dots + (a _ {1} + b _ {1}) x + (a _ {0} + b _ {0}) \in P [ x ] _ {n},
$$

$$
\lambda \left(a _ {n} x ^ {n} + \dots + a _ {1} x + a _ {0}\right) = (\lambda a _ {n}) x ^ {n} + \dots + (\lambda a _ {1}) x + (\lambda a _ {0}) \in P [ x ] _ {n},
$$

所以 $P[x]_n$ 是一个向量空间.

例2 $n$ 次多项式的全体

$$
Q [ x ] _ {n} = \left\{a _ {n} x ^ {n} + a _ {n - 1} x ^ {n - 1} + \dots + a _ {1} x + a _ {0} \mid a _ {n}, a _ {n - 1}, \dots , a _ {1}, a _ {0} \in \mathbb {R}, \text {且} a _ {n} \neq 0 \right\}
$$

对于通常的多项式加法和数乘运算不构成向量空间.这是因为

$$
0 p = 0 x ^ {n} + 0 x ^ {n - 1} + \dots + 0 x + 0 \notin Q [ x ] _ {n},
$$

即 $Q[x]_n$ 对运算不封闭.

例3 正弦函数的集合

$$
S [ x ] = \{A \sin (x + B) \mid A, B \in \mathbb {R} \}
$$

对于通常的函数加法及数乘函数的乘法构成向量空间.这是因为:通常的函数加法及数乘运算显然满足线性运算规律,故只要验证 $S[x]$ 对运算封闭:

$$
\begin{array}{l} s _ {1} + s _ {2} = A _ {1} \sin (x + B _ {1}) + A _ {2} \sin (x + B _ {2}) \\ = (a _ {1} \cos x + b _ {1} \sin x) + (a _ {2} \cos x + b _ {2} \sin x) \\ = (a _ {1} + a _ {2}) \cos x + (b _ {1} + b _ {2}) \sin x = A \sin (x + B) \in S [ x ], \\ \end{array}
$$

考研电子书网站:www.pdf2book.com

143

---

\*第6章 线性空间与线性变换

$$
\lambda s _ {1} = \lambda A _ {1} \sin (x + B _ {1}) = (\lambda A _ {1}) \sin (x + B _ {1}) \in S [ x ],
$$

所以 $S[x]$ 是一个向量空间.

检验一个集合是否构成向量空间,当然不能只检验对运算的封闭性(如上面两例).若所定义的加法和数乘运算不是通常的实数的加、乘运算,则就应仔细检验是否满足八条线性运算规律.

例4 $n$ 个有序实数组成的数组的全体

$$
S ^ {n} = \left\{\left(x _ {1}, x _ {2}, \dots , x _ {n}\right) ^ {\mathrm{T}} \mid x _ {1}, x _ {2}, \dots , x _ {n} \in \mathbb {R} \right\}
$$

对于通常的有序数组的加法及如下定义的数乘

$$
\lambda \circ (x _ {1}, x _ {2}, \dots , x _ {n}) ^ {\mathrm{T}} = (0, 0, \dots , 0) ^ {\mathrm{T}}
$$

不构成向量空间.

可以验证 $S^n$ 对运算封闭. 但因 $1 \circ x = 0$, 不满足线性运算的规律 (v), 即所定义的运算不是线性运算, 所以 $S^n$ 不是向量空间.

比较 $S^n$ 与 $\mathbb{R}^n$, 作为集合它们是一样的, 但由于在其中所定义的运算不同, 以至 $\mathbb{R}^n$ 构成向量空间而 $S^n$ 不是向量空间. 由此可见, 向量空间的概念是集合与运算二者的结合. 一般来说, 同一个集合, 若定义两种不同的线性运算, 就构成不同的向量空间; 若定义的运算不是线性运算, 就不能构成向量空间. 所以, 所定义的线性运算是向量空间的本质, 而其中的元素是什么并不重要.

为了对线性运算的理解更具有一般性,请看下例.

例 5 正实数的全体, 记作  $R^{+}$ , 在其中定义加法及数乘运算为

$$
a \oplus b = a b \quad (a, b \in \mathbb {R} ^ {+}),
$$

$$
\lambda \circ a = a ^ {\lambda} \quad (\lambda \in \mathbb {R}, a \in \mathbb {R} ^ {+}),
$$

验证  $R^{+}$ 对上述加法与数乘运算构成线性空间.

证 实际上要验证十条:

对加法封闭: 对任意的  $a, b \in R^{+}$ ，有  $a \oplus b = ab \in R^{+}$ ;

对数乘封闭: 对任意的  $\lambda \in R, a \in R^{+}$ ，有  $\lambda \circ a = a^{\lambda} \in R^{+}$ .

(i)  $a \oplus b = ab = ba = b \oplus a;$
(ii)  $(a \oplus b) \oplus c = (ab) \oplus c = (ab)c = a(bc) = a \oplus (b \oplus c)$ ;
(iii)  $R^{+}$  中存在零元素 1, 对任何  $a \in R^{+}$ , 有  $a \oplus 1 = a \cdot 1 = a$ ;
(iv) 对任何 $a \in \mathbb{R}^+$, 有负元素 $a^{-1} \in \mathbb{R}^+$, 使 $a \oplus a^{-1} = aa^{-1} = 1$;
(v)  $1 \circ a = a^{1} = a;$
(vi)  $\lambda\circ(\mu\circ a)=\lambda\circ a^{\mu}=\left(^{\prime}\dot{a}^{\mu}\right)^{\lambda}=a^{\lambda\mu}=\left(\lambda\mu\right)\circ a;$
(vii) $(\lambda + \mu) \circ a = a^{\lambda + \mu} = a^{\lambda}a^{\mu} = a^{\lambda} \oplus a^{\mu} = \lambda \circ a \oplus \mu \circ a;$
(viii) $\lambda \circ (a \oplus b) = \lambda \circ (ab) = (ab)^{\lambda} = a^{\lambda}b^{\lambda} = a^{\lambda} \oplus b^{\lambda} = \lambda \circ a \oplus \lambda \circ b,$

144

---

§1 线性空间的定义与性质

因此，$\mathbb{R}^{+}$对于所定义的运算构成线性空间.

下面讨论线性空间的性质.

## 1. 零向量是惟一的.

证 设 $\mathbf{0}_1, \mathbf{0}_2$ 是线性空间 $V$ 中的两个零向量，即对任何 $\alpha \in V$，有 $\alpha + \mathbf{0}_1 = \alpha$，$\alpha + \mathbf{0}_2 = \alpha$。于是特别有

$$
\mathbf {0} _ {2} + \mathbf {0} _ {1} = \mathbf {0} _ {2}, \quad \mathbf {0} _ {1} + \mathbf {0} _ {2} = \mathbf {0} _ {1},
$$

所以

$$
\mathbf {0} _ {1} = \mathbf {0} _ {1} + \mathbf {0} _ {2} = \mathbf {0} _ {2} + \mathbf {0} _ {1} = \mathbf {0} _ {2}.
$$

证毕

2. 任一向量的负向量是惟一的, $\alpha$ 的负向量记作- $\alpha$.

证 设 $\beta, \gamma$ 是 $\alpha$ 的负向量，即 $\alpha + \beta = 0, \alpha + \gamma = 0$. 于是

$$
\boldsymbol {\beta} = \boldsymbol {\beta} + \mathbf {0} = \boldsymbol {\beta} + (\alpha + \gamma) = (\alpha + \boldsymbol {\beta}) + \gamma = \mathbf {0} + \gamma = \gamma .
$$

证毕

3. $0\alpha = 0, (-1)\alpha = -\alpha, \lambda 0 = 0.$

证 $\alpha + 0\alpha = 1\alpha + 0\alpha = (1 + 0)\alpha = 1\alpha = \alpha,$

两端同时加上 $\alpha$ 的负向量，即得 $0\alpha = 0$

$$
\alpha + (- 1) \alpha = 1 \alpha + (- 1) \alpha = [ 1 + (- 1) ] \alpha = 0 \alpha = 0,
$$

所以

$$
(- 1) \alpha = - \alpha ;
$$

$$
\lambda \mathbf {0} = \lambda [ \alpha + (- 1) \alpha ] = \lambda \alpha + (- \lambda) \alpha = [ \lambda + (- \lambda) ] \alpha = 0 \alpha = \mathbf {0}.
$$

证毕

4. 如果  $\lambda\alpha=0$ ，则  $\lambda=0$  或  $\alpha=0$ .

证 若 $\lambda \neq 0$ ，在 $\lambda \alpha = 0$ 两端乘 $\frac{1}{\lambda}$ 得

$$
\frac {1}{\lambda} (\lambda \alpha) = \frac {1}{\lambda} \mathbf {0} = \mathbf {0},
$$

而

$$
\frac {1}{\lambda} (\lambda \alpha) = \left(\frac {1}{\lambda} \lambda\right) \alpha = 1 \alpha = \alpha ,
$$

所以

$$
\alpha = 0.
$$

证毕

在第 4 章中, 我们提出过子空间的定义, 今稍作修正.

定义 2 设 V 是一个线性空间, L 是 V 的一个非空子集, 如果 L 对于 V 中所定义的加法和数乘两种运算也构成一个线性空间, 则称 L 为 V 的子空间.

考研电子书网站:www.pdf2book.com

145

---

\*第6章 线性空间与线性变换

一个非空子集要满足什么条件才构成子空间？因 $L$ 是 $V$ 的一部分，$V$ 中的运算对于 $L$ 而言，规律(i)、(ii)、(v)、(vi)、(vii)、(viii)显然是满足的，因此只要 $L$ 对运算封闭且满足规律(iii)、(iv)即可.但由线性空间的性质知，若 $L$ 对运算封闭，则即能满足规律(iii)、(iv).因此我们有

定理1 线性空间 $V$ 的非空子集 $L$ 构成子空间的充分必要条件是: $L$ 对于 $V$ 中的线性运算封闭.

## § 2 维数、基与坐标

在第4章中,我们用线性运算来讨论n维数组向量之间的关系,介绍了一些重要概念,如线性组合、线性相关与线性无关等.这些概念以及有关的性质只涉及线性运算,因此,对于一般的线性空间中的向量仍然适用.以后我们将直接引用这些概念和性质.

在第 4 章中我们已经提出了基与维数的概念, 这当然也适用于一般的线性空间. 这是线性空间的主要特性, 特再叙述如下:

定义 3 在线性空间 V 中, 如果存在 n 个向量  $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{n}$ , 满足

(i)  $\alpha_{1},\alpha_{2},\cdots,\alpha_{n}$  线性无关；
(ii) V 中任一向量  $\alpha$  总可由  $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{n}$  线性表示，

那么  $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{n}$  就称为线性空间 V 的一个基，n 称为线性空间 V 的维数。只含一个零向量的线性空间没有基，规定它的维数为 0。

维数为 n 的线性空间称为 n 维线性空间, 记作  $V_{n}$ .

这里要指出:线性空间的维数可以是无穷.对于无穷维的线性空间,本书不作讨论.

对于 n 维线性空间  $V_{n}$ ，若知  $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{n}$  为  $V_{n}$  的一个基，则  $V_{n}$  可表示为

$$
V _ {n} = \left\{x _ {1} \boldsymbol {\alpha} _ {1} + x _ {2} \boldsymbol {\alpha} _ {2} + \dots + x _ {n} \boldsymbol {\alpha} _ {n} \mid x _ {1}, x _ {2}, \dots , x _ {n} \in \mathbb {R} \right\} = \operatorname{Span} \left\{\boldsymbol {\alpha} _ {1}, \boldsymbol {\alpha} _ {2}, \dots , \boldsymbol {\alpha} _ {n} \right\},
$$

即  $V_{n}$  是基所生成的线性空间, 这就较清楚地显示出线性空间  $V_{n}$  的构造.

若  $\alpha_{1},\alpha_{2},\cdots,\alpha_{n}$  为  $V_{n}$  的一个基，则对任何  $\alpha\in V_{n}$ ，都有惟一的一组有序数  $x_{1},x_{2},\cdots,x_{n}$ ，使

$$
\boldsymbol {\alpha} = x _ {1} \boldsymbol {\alpha} _ {1} + x _ {2} \boldsymbol {\alpha} _ {2} + \dots + x _ {n} \boldsymbol {\alpha} _ {n};
$$

反之，任给一组有序数 $x_{1}, x_{2}, \cdots, x_{n}$，总有惟一的向量

$$
\dot {\boldsymbol {\alpha}} = x _ {1} \boldsymbol {\alpha} _ {1} + x _ {2} \boldsymbol {\alpha} _ {2} + \dots + x _ {n} \boldsymbol {\alpha} _ {n} \in V _ {n}.
$$

这样  $V_{n}$  的向量  $\alpha$  与有序数组  $(x_{1}, x_{2}, \cdots, x_{n})^{\mathrm{T}}$  之间存在着一一对应的关系, 因此可以用这组有序数来表示向量  $\alpha$ . 于是我们有

146

---

§2 维数、基与坐标

定义 4 设  $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{n}$  是线性空间  $V_{n}$  的一个基. 对于任一向量  $\alpha \in V_{n}$ ，总有且仅有一组有序数  $x_{1}, x_{2}, \cdots, x_{n}$  使

$$
\boldsymbol {\alpha} = x _ {1} \boldsymbol {\alpha} _ {1} + x _ {2} \boldsymbol {\alpha} _ {2} + \dots + x _ {n} \boldsymbol {\alpha} _ {n},
$$

$x_{1},x_{2},\cdots,x_{n}$  这组有序数就称为向量  $\alpha$  在  $\alpha_{1},\alpha_{2},\cdots,\alpha_{n}$  这个基中的坐标，并记作

$$
\boldsymbol {x} = (x _ {1}, x _ {2}, \dots , x _ {n}) ^ {\mathrm{T}}.
$$

例6 在线性空间 $P[x]_4$ 中, $p_1 = 1, p_2 = x, p_3 = x^2, p_4 = x^3, p_5 = x^4$ 就是它的一个基.任一不超过4次的多项式

$$
p = a _ {4} x ^ {4} + a _ {3} x ^ {3} + a _ {2} x ^ {2} + a _ {1} x + a _ {0}
$$

都可表示为

$$
\boldsymbol {p} = a _ {0} \boldsymbol {p} _ {1} + a _ {1} \boldsymbol {p} _ {2} + a _ {2} \boldsymbol {p} _ {3} + a _ {3} \boldsymbol {p} _ {4} + a _ {4} \boldsymbol {p} _ {5},
$$

因此 $\pmb{p}$ 在这个基中的坐标为 $(a_0, a_1, a_2, a_3, a_4)^{\mathrm{T}}$.

若另取一个基 $q_{1} = 1, q_{2} = 1 + x, q_{3} = 2x^{2}, q_{4} = x^{3}, q_{5} = x^{4}$, 则

$$
\begin{array}{l} p = a _ {0} + a _ {1} x + a _ {2} x ^ {2} + a _ {3} x ^ {3} + a _ {4} x ^ {4} \\ = (a _ {0} - a _ {1}) + a _ {1} (1 + x) + \frac {a _ {2}}{2} 2 x ^ {2} + a _ {3} x ^ {3} + a _ {4} x ^ {4} \\ = (a _ {0} - a _ {1}) q _ {1} + a _ {1} q _ {2} + \frac {1}{2} a _ {2} q _ {3} + a _ {3} q _ {4} + a _ {4} q _ {5}, \\ \end{array}
$$

因此 p 在这个基中的坐标为  $\left(a_{0}-a_{1},a_{1},\frac{1}{2}a_{2},a_{3},a_{4}\right)^{\mathrm{T}}$ .

建立了坐标以后,就把抽象的向量  $\alpha$  与具体的数组向量  $(x_{1}, x_{2}, \cdots, x_{n})^{\mathrm{T}}$  联系起来了,并且还可把  $V_{n}$  中抽象的线性运算与  $R^{n}$  中数组向量的线性运算联系起来.

设  $\alpha,\beta\in V_{n}$ ，有  $\alpha=x_{1}\alpha_{1}+x_{2}\alpha_{2}+\cdots+x_{n}\alpha_{n},\beta=y_{1}\alpha_{1}+y_{2}\alpha_{2}+\cdots+y_{n}\alpha_{n}$ ，于是

$$
\alpha + \beta = (x _ {1} + y _ {1}) \alpha_ {1} + (x _ {2} + y _ {2}) \alpha_ {2} + \dots + (x _ {n} + y _ {n}) \alpha_ {n},
$$

$$
\lambda \alpha = (\lambda x _ {1}) \alpha_ {1} + (\lambda x _ {2}) \alpha_ {2} + \dots + (\lambda x _ {n}) \alpha_ {n},
$$

即 $\alpha +\beta$ 的坐标是

$$
(x _ {1} + y _ {1}, x _ {2} + y _ {2}, \dots , x _ {n} + y _ {n}) ^ {\mathrm{T}} = (x _ {1}, x _ {2}, \dots , x _ {n}) ^ {\mathrm{T}} + (y _ {1}, y _ {2}, \dots , y _ {n}) ^ {\mathrm{T}},
$$

$\lambda \alpha$ 的坐标是

$$
\left(\lambda x _ {1}, \lambda x _ {2}, \dots , \lambda x _ {n}\right) ^ {\mathrm{T}} = \lambda \left(x _ {1}, x _ {2}, \dots , x _ {n}\right) ^ {\mathrm{T}}.
$$

总之, 设在 $n$ 维线性空间 $V_{n}$ 中取定一个基 $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{n}$, 则 $V_{n}$ 中的向量 $\alpha$ 与 $\mathbb{R}^{n}$ 中 $n$ 维数组向量空间的向量 $(x_{1}, x_{2}, \cdots, x_{n})^{\mathrm{T}}$ 之间就有一个一一对应的关系, 且这个对应关系具有下述性质:

设  $\boldsymbol{\alpha}\leftrightarrow(x_{1},x_{2},\cdots,x_{n})^{\mathrm{T}},\boldsymbol{\beta}\leftrightarrow(y_{1},y_{2},\cdots,y_{n})^{\mathrm{T}}$ ，则

(i)  $\boldsymbol{\alpha}+\boldsymbol{\beta}\leftrightarrow(x_{1},x_{2},\cdots,x_{n})^{\mathrm{T}}+(y_{1},y_{2},\cdots,y_{n})^{\mathrm{T}},$

考研电子书网站:www.pdf2book.com

147

---

\*第6章 线性空间与线性变换

(ii)  $\lambda\alpha\leftrightarrow\lambda(x_{1},x_{2},\cdots,x_{n})^{\mathrm{T}}.$

也就是说, 这个对应关系保持线性组合的对应. 因此, 我们可以说 $V_{n}$ 与 $\mathbb{R}^{n}$ 有相同的结构, 我们称 $V_{n}$ 与 $\mathbb{R}^{n}$ 同构.

一般地, 设 V 与 U 是两个线性空间, 如果在它们的向量之间有一一对应关系, 且这个对应关系保持线性组合的对应, 那么就说线性空间 V 与 U 同构.

显然,任何 n 维线性空间都与  $R^{n}$  同构,即维数相等的线性空间都同构.从而可知线性空间的结构完全被它的维数所决定.

同构的概念除向量一一对应外,主要是保持线性运算的对应关系.因此, $V_{n}$ 中的抽象的线性运算就可转化为 $R^{n}$ 中的线性运算,并且 $R^{n}$ 中凡是只涉及线性运算的性质就都适用于 $V_{n}$.但 $R^{n}$ 中超出线性运算的性质,在 $V_{n}$ 中就不一定具备,例如 $R^{n}$ 中的内积概念在 $V_{n}$ 中就不一定有意义.

## § 3 基变换与坐标变换

由例 6 可见, 同一向量在不同的基中有不同的坐标, 那么, 不同的基与不同的坐标之间有怎样的关系呢?

设  $\alpha_{1},\alpha_{2},\cdots,\alpha_{n}$  及  $\beta_{1},\beta_{2},\cdots,\beta_{n}$  是线性空间  $V_{n}$  中的两个基，

$$
\left\{ \begin{array}{l} \boldsymbol {\beta} _ {1} = p _ {1 1} \boldsymbol {\alpha} _ {1} + p _ {2 1} \boldsymbol {\alpha} _ {2} + \dots + p _ {n 1} \boldsymbol {\alpha} _ {n}, \\ \boldsymbol {\beta} _ {2} = p _ {1 2} \boldsymbol {\alpha} _ {1} + p _ {2 2} \boldsymbol {\alpha} _ {2} + \dots + p _ {n 2} \boldsymbol {\alpha} _ {n}, \\ \dots \dots \\ \boldsymbol {\beta} _ {n} = p _ {1 n} \boldsymbol {\alpha} _ {1} + p _ {2 n} \boldsymbol {\alpha} _ {2} + \dots + p _ {n n} \boldsymbol {\alpha} _ {n}, \end{array} \right. \tag {1}
$$

把  $\alpha_{1},\alpha_{2},\cdots,\alpha_{n}$  这 n 个有序向量记作  $(\boldsymbol{\alpha}_{1},\boldsymbol{\alpha}_{2},\cdots,\boldsymbol{\alpha}_{n})$ ，记 n 阶矩阵  $\boldsymbol{P}=(p_{ij})$ ，利用向量和矩阵的形式，(1) 式可表示为

$$
(\boldsymbol {\beta} _ {1}, \boldsymbol {\beta} _ {2}, \dots , \boldsymbol {\beta} _ {n}) = (\boldsymbol {\alpha} _ {1}, \boldsymbol {\alpha} _ {2}, \dots , \boldsymbol {\alpha} _ {n}) \boldsymbol {P}. \tag {2}
$$

(1)式或(2)式称为基变换公式,矩阵P称为由基 $\alpha_{1},\alpha_{2},\cdots,\alpha_{n}$ 到基 $\beta_{1},\beta_{2},\cdots,\beta_{n}$ 的过渡矩阵.由于 $\beta_{1},\beta_{2},\cdots,\beta_{n}$ 线性无关,故过渡矩阵P可逆.

定理 2 设  $V_{n}$  中的向量  $\alpha$  在基  $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{n}$  中的坐标为  $(x_{1}, x_{2}, \cdots, x_{n})^{\mathrm{T}}$ ，在基  $\beta_{1}, \beta_{2}, \cdots, \beta_{n}$  中的坐标为  $(x_{1}', x_{2}', \cdots, x_{n}')^{\mathrm{T}}$ 。若两个基满足关系式(2)，则有坐标变换公式

$$
\left( \begin{array}{c} x _ {1} \\ x _ {2} \\ \vdots \\ x _ {n} \end{array} \right) = \boldsymbol {P} \left( \begin{array}{c} x _ {1} ^ {\prime} \\ x _ {2} ^ {\prime} \\ \vdots \\ x _ {n} ^ {\prime} \end{array} \right) \quad \text {或} \quad \left( \begin{array}{c} x _ {1} ^ {\prime} \\ x _ {2} ^ {\prime} \\ \vdots \\ x _ {n} ^ {\prime} \end{array} \right) = \boldsymbol {P} ^ {- 1} \left( \begin{array}{c} x _ {1} \\ x _ {2} \\ \vdots \\ x _ {n} \end{array} \right). \tag {3}
$$

148

---

§3 基变换与坐标变换

证因

$$
(\boldsymbol {\alpha} _ {1}, \boldsymbol {\alpha} _ {2}, \dots , \boldsymbol {\alpha} _ {n}) \left( \begin{array}{c} x _ {1} \\ x _ {2} \\ \vdots \\ x _ {n} \end{array} \right) = \boldsymbol {\alpha} = (\boldsymbol {\beta} _ {1}, \boldsymbol {\beta} _ {2}, \dots , \boldsymbol {\beta} _ {n}) \left( \begin{array}{c} x _ {1} ^ {\prime} \\ x _ {2} ^ {\prime} \\ \vdots \\ x _ {n} ^ {\prime} \end{array} \right) = (\boldsymbol {\alpha} _ {1}, \boldsymbol {\alpha} _ {2}, \dots , \boldsymbol {\alpha} _ {n}) P \left( \begin{array}{c} x _ {1} ^ {\prime} \\ x _ {2} ^ {\prime} \\ \vdots \\ x _ {n} ^ {\prime} \end{array} \right),
$$

由于  $\alpha_{1},\alpha_{2},\cdots,\alpha_{n}$  线性无关,故即有关系式(3).

证毕

这个定理的逆命题也成立. 即若任一向量的两种坐标满足坐标变换公式(3), 则两个基满足基变换公式(2).

例7 在 $P[x]_3$ 中取两个基

$$
\boldsymbol {\alpha} _ {1} = x ^ {3} + 2 x ^ {2} - x, \quad \boldsymbol {\alpha} _ {2} = x ^ {3} - x ^ {2} + x + 1, \quad \boldsymbol {\alpha} _ {3} = - x ^ {3} + 2 x ^ {2} + x + 1, \quad \boldsymbol {\alpha} _ {4} = - x ^ {3} - x ^ {2} + 1
$$

及

$$
\boldsymbol {\beta} _ {1} = 2 x ^ {3} + x ^ {2} + 1, \quad \boldsymbol {\beta} _ {2} = x ^ {2} + 2 x + 2, \quad \boldsymbol {\beta} _ {3} = - 2 x ^ {3} + x ^ {2} + x + 2, \quad \boldsymbol {\beta} _ {4} = x ^ {3} + 3 x ^ {2} + x + 2.
$$

求坐标变换公式.

解 将 $\beta_{1},\beta_{2},\beta_{3},\beta_{4}$ 用 $\alpha_{1},\alpha_{2},\alpha_{3},\alpha_{4}$ 表示.由

$$
(\boldsymbol {\alpha} _ {1}, \boldsymbol {\alpha} _ {2}, \boldsymbol {\alpha} _ {3}, \boldsymbol {\alpha} _ {4}) = (x ^ {3}, x ^ {2}, x, 1) \boldsymbol {A}, \quad (\boldsymbol {\beta} _ {1}, \boldsymbol {\beta} _ {2}, \boldsymbol {\beta} _ {3}, \boldsymbol {\beta} _ {4}) = (x ^ {3}, x ^ {2}, x, 1) \boldsymbol {B},
$$

其中

$$
\boldsymbol {A} = \left( \begin{array}{r r r r} 1 & 1 & - 1 & - 1 \\ 2 & - 1 & 2 & - 1 \\ - 1 & 1 & 1 & 0 \\ 0 & 1 & 1 & 1 \end{array} \right), \quad \boldsymbol {B} = \left( \begin{array}{r r r r} 2 & 0 & - 2 & 1 \\ 1 & 1 & 1 & 3 \\ 0 & 2 & 1 & 1 \\ 1 & 2 & 2 & 2 \end{array} \right),
$$

得

$$
(\boldsymbol {\beta} _ {1}, \boldsymbol {\beta} _ {2}, \boldsymbol {\beta} _ {3}, \boldsymbol {\beta} _ {4}) = (\boldsymbol {\alpha} _ {1}, \boldsymbol {\alpha} _ {2}, \boldsymbol {\alpha} _ {3}, \boldsymbol {\alpha} _ {4}) \boldsymbol {A} ^ {- 1} \boldsymbol {B},
$$

故坐标变换公式为

$$
\left( \begin{array}{c} x _ {1} ^ {\prime} \\ x _ {2} ^ {\prime} \\ x _ {3} ^ {\prime} \\ x _ {4} ^ {\prime} \end{array} \right) = \boldsymbol {B} ^ {- 1} \boldsymbol {A} \left( \begin{array}{c} x _ {1} \\ x _ {2} \\ x _ {3} \\ x _ {4} \end{array} \right).
$$

用矩阵的初等行变换求  $B^{-1}A$ : 把矩阵  $(B,A)$  中的 B 变成 E, 则 A 即变成  $B^{-1}A$ . 计算如下:

$$
(\boldsymbol {B}, \boldsymbol {A}) = \left( \begin{array}{c c c c c c c c} 2 & 0 & - 2 & 1 & 1 & 1 & - 1 & - 1 \\ 1 & 1, & 1 & 3 & 2 & - 1 & 2 & - 1 \\ 0 & 2 & 1 & 1 & - 1 & 1 & 1 & 0 \\ 1 & 2 & 2 & 2 & 0 & 1 & 1 & 1 \end{array} \right)
$$

考研电子书网站:www.pdf2book.com

149

---

\*第6章 线性空间与线性变换

$$
\underbrace {r _ {1} - 2 r _ {2}} _ {r _ {4} - r _ {2}} \left( \begin{array}{c c c c c c c c} 0 & - 2 & - 4 & - 5 & - 3 & 3 & - 5 & 1 \\ 1 & 1 & 1 & 3 & 2 & - 1 & 2 & - 1 \\ 0 & 2 & 1 & 1 & - 1 & 1 & 1 & 0 \\ 0 & 1 & 1 & - 1 & - 2 & 2 & - 1 & 2 \end{array} \right)
$$

$$
\left( \begin{array}{c c c c c c c c} 0 & 0 & - 2 & - 7 & - 7 & 7 & - 7 & 5 \\ 1 & 0 & 0 & 4 & 4 & - 3 & 3 & - 3 \\ 0 & 0 & - 1 & 3 & 3 & - 3 & 3 & - 4 \\ 0 & 1 & 1 & - 1 & - 2 & 2 & - 1 & 2 \end{array} \right)
$$

$$
\underbrace {r _ {1} - 2 r _ {3}} _ {r _ {4} + r _ {3}} \left( \begin{array}{c c c c c c c c} 0 & 0 & 0 & - 1 3 & - 1 3 & 1 3 & - 1 3 & 1 3 \\ 1 & 0 & 0 & 4 & 4 & - 3 & 3 & - 3 \\ 0 & 0 & - 1 & 3 & 3 & - 3 & 3 & - 4 \\ 0 & 1 & 0 & 2 & 1 & - 1 & 2 & - 2 \end{array} \right)
$$

$$
\underbrace {r _ {1} \times \left(- \frac {1}{1 3}\right)} _ {r _ {2} - 4 r _ {1}} \left( \begin{array}{c c c c c c c c} 0 & 0 & 0 & 1 & 1 & - 1 & 1 & - 1 \\ 1 & 0 & 0 & 0 & 0 & 1 & - 1 & 1 \\ 0 & 0 & - 1 & 0 & 0 & 0 & 0 & - 1 \\ 0 & 1 & 0 & 0 & - 1 & 1 & 0 & 0 \end{array} \right)
$$

$$
\underbrace { \begin{array}{c} r _ {1} \leftrightarrow r _ {2} \\ r _ {3} \times (- 1) \\ r _ {2} \leftrightarrow r _ {4} \end{array} } _ {r _ {2} \leftrightarrow r _ {4}} \left( \begin{array}{c c c c c c c c} 1 & 0 & 0 & 0 & 0 & 1 & - 1 & 1 \\ 0 & 1 & 0 & 0 & - 1 & 1 & 0 & 0 \\ 0 & 0 & 1 & 0 & 0 & 0 & 0 & 1 \\ 0 & 0 & 0 & 1 & 1 & - 1 & 1 & - 1 \end{array} \right),
$$

于是坐标变换公式为

$$
\left( \begin{array}{c} x _ {1} ^ {\prime} \\ x _ {2} ^ {\prime} \\ x _ {3} ^ {\prime} \\ x _ {4} ^ {\prime} \end{array} \right) = \left( \begin{array}{c c c c} 0 & 1 & - 1 & 1 \\ - 1 & 1 & 0 & 0 \\ 0 & 0 & 0 & 1 \\ 1 & - 1 & 1 & - 1 \end{array} \right) \left( \begin{array}{c} x _ {1} \\ x _ {2} \\ x _ {3} \\ x _ {4} \end{array} \right).
$$

## § 4 线性变换

定义 5 设有两个非空集合 A, B, 如果对于 A 中任一元素  $\alpha$ , 按照一定的规则, 总

150

---

§4 线性变换

有 B 中一个确定的元素  $\beta$  和它对应, 那么, 这个对应规则称为从集合 A 到集合 B 的映射. 我们常用字母表示一个映射, 譬如把上述映射记作 T, 并记

$$
\beta = T (\alpha) \quad \text {或} \quad \beta = T \alpha (\alpha \in A). \tag {4}
$$

设 $\alpha_{1} \in A, T(\alpha_{1}) = \beta_{1}$, 就说映射 $T$ 把元素 $\alpha_{1}$ 变为 $\beta_{1}, \beta_{1}$ 称为 $\alpha_{1}$ 在映射 $T$ 下的像, $\alpha_{1}$ 称为 $\beta_{1}$ 在映射 $T$ 下的原像. $A$ 称为映射 $T$ 的定义域, 像的全体所构成的集合称为像集, 记作 $T(A)$, 即

$$
T (A) = \{\beta = T (\alpha) \mid \alpha \in A \},
$$

显然 $T(A)\subseteq B$

映射的概念是函数概念的推广.例如,设二元函数 $z=f(x,y)$ 的定义域为平面区域G,函数值域为Z,那么,函数关系f就是一个从定义域G到实数域R的映射;函数值 $f(x_{0},y_{0})=z_{0}$ 就是元素 $(x_{0},y_{0})$ 的像, $(x_{0},y_{0})$ 就是 $z_{0}$ 的原像,Z就是像集.

定义6 设 $V_{n}, U_{m}$ 分别是 $n$ 维和 $m$ 维线性空间, $T$ 是一个从 $V_{n}$ 到 $U_{m}$ 的映射, 如果映射 $T$ 满足

(i) 任给 $\alpha_{1}, \alpha_{2} \in V_{n}$ （从而 $\alpha_{1} + \alpha_{2} \in V_{n}$），有

$$
T (\boldsymbol {\alpha} _ {1} + \boldsymbol {\alpha} _ {2}) = T (\boldsymbol {\alpha} _ {1}) + T (\boldsymbol {\alpha} _ {2}),
$$

(ii) 任给 $\alpha \in V_{n}, \lambda \in \mathbb{R}$ （从而 $\lambda \alpha \in V_{n}$），有

$$
T (\lambda \alpha) = \lambda T (\alpha),
$$

那么 T 就称为从  $V_{n}$  到  $U_{m}$  的线性映射.

简言之,线性映射就是保持线性组合的对应的映射.

例如,关系式

$$
\left( \begin{array}{c} y _ {1} \\ y _ {2} \\ \vdots \\ y _ {m} \end{array} \right) = \left( \begin{array}{c c c c} a _ {1 1} & a _ {1 2} & \dots & a _ {1 n} \\ a _ {2 1} & a _ {2 2} & \dots & a _ {2 n} \\ \vdots & \vdots & & \vdots \\ a _ {m 1} & a _ {m 2} & \dots & a _ {m n} \end{array} \right) \left( \begin{array}{c} x _ {1} \\ x _ {2} \\ \vdots \\ x _ {n} \end{array} \right)
$$

就确定了一个从 $\mathbb{R}^n$ 到 $\mathbb{R}^m$ 的映射，并且是个线性映射(参见后面的例10).

特别地,在定义6中,如果 $U_{m}=V_{n}$ ,那么T是一个从线性空间 $V_{n}$ 到其自身的线性映射,称为线性空间 $V_{n}$ 中的线性变换.

下面我们只讨论线性空间  $V_{n}$  中的线性变换.

例8 在线性空间 $P[x]_3$ 中，

(1) 如果微分运算 D 表示对 x 求导的运算  $\frac{d}{dx}$ ，那么 D 是一个线性变换。这是因为任取  $p = a_{3}x^{3} + a_{2}x^{2} + a_{1}x + a_{0} \in P[x]_{3}$ ，则  $Dp = 3a_{3}x^{2} + 2a_{2}x + a_{1}$ ;

$q=b_{3}x^{3}+b_{2}x^{2}+b_{1}x+b_{0}\in P[x]_{3}$ ，则 $Dq=3b_{3}x^{2}+2b_{2}x+b_{1}$

从而有

考研电子书网站:www.pdf2book.com

151

---

\*第6章 线性空间与线性变换

$$
\begin{array}{l} \mathrm{D} (\boldsymbol {p} + \boldsymbol {q}) = \mathrm{D} \left[ \left(a _ {3} + b _ {3}\right) x ^ {3} + \left(a _ {2} + b _ {2}\right) x ^ {2} + \left(a _ {1} + b _ {1}\right) x + \left(a _ {0} + b _ {0}\right) \right] \\ = 3 \left(a _ {3} + b _ {3}\right) x ^ {2} + 2 \left(a _ {2} + b _ {2}\right) x + \left(a _ {1} + b _ {1}\right) \\ = (3 a _ {3} x ^ {2} + 2 a _ {2} x + a _ {1}) + (3 b _ {3} x ^ {2} + 2 b _ {2} x + b _ {1}) = \mathrm{D} p + \mathrm{D} q; \\ \mathrm{D} (\lambda p) = \mathrm{D} \left(\lambda a _ {3} x ^ {3} + \lambda a _ {2} x ^ {2} + \lambda a _ {1} x + \lambda a _ {0}\right) = \lambda \left(3 a _ {3} x ^ {2} + 2 a _ {2} x + a _ {1}\right) = \lambda \mathrm{D} p. \\ \end{array}
$$

(2) 如果  $T(\boldsymbol{p}) = a_{0}$ ，那么 T 也是一个线性变换。这是因为

$$
T (\boldsymbol {p} + \boldsymbol {q}) = a _ {0} + b _ {0} = T (\boldsymbol {p}) + T (\boldsymbol {q});
$$

$$
T (\lambda \boldsymbol {p}) = \lambda a _ {0} = \lambda T (\boldsymbol {p}).
$$

（3）如果 $T_{1}(\pmb {p}) = 1$ ，那么 $T_{1}$ 是个变换，但不是线性变换.这是因为 $T_{1}(\pmb {p} + \pmb {q}) = 1$ ，而$T_{1}(\pmb {p}) + T_{1}(\pmb {q}) = 1 + 1 = 2,$ 故

$$
T _ {1} (\boldsymbol {p} + \boldsymbol {q}) \neq T _ {1} (\boldsymbol {p}) + T _ {1} (\boldsymbol {q}).
$$

例9 关系式

$$
T \binom{x}{y} = \left( \begin{array}{c c} \cos \varphi & - \sin \varphi \\ \sin \varphi & \cos \varphi \end{array} \right) \binom{x}{y}
$$

确定了 $xOy$ 平面上的一个变换 $T$, 说明变换 $T$ 的几何意义(参见第2章图2.3).

解 记 $\left\{\begin{aligned}x&=r\cos\theta,\\ y&=r\sin\theta,\end{aligned}\right.$ 于是

$$
T \binom{x}{y} = \binom {x \cos \varphi - y \sin \varphi}{x \sin \varphi + y \cos \varphi} = \binom {r \cos \theta \cos \varphi - r \sin \theta \sin \varphi}{r \cos \theta \sin \varphi + r \sin \theta \cos \varphi} = \binom {r \cos (\theta + \varphi)} {r \sin (\theta + \varphi)},
$$

这表示变换 $T$ 把任一向量按逆时针方向旋转 $\varphi$ 角（由例10可知这个变换是一个线性变换）.

线性变换具有下述基本性质:

(i)  $T0=0, T(-\alpha)=-T\alpha.$
(ii) 若  $\beta=k_{1}\alpha_{1}+k_{2}\alpha_{2}+\cdots+k_{m}\alpha_{m}$ ，则

$$
T \boldsymbol {\beta} = k _ {1} T \boldsymbol {\alpha} _ {1} + k _ {2} T \boldsymbol {\alpha} _ {2} + \dots + k _ {m} T \boldsymbol {\alpha} _ {m}.
$$

(iii) 若  $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{m}$  线性相关，则  $T\alpha_{1}, T\alpha_{2}, \cdots, T\alpha_{m}$  亦线性相关.

这些性质请读者证明之. 注意性质(iii)的逆命题是不成立的, 即当  $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{m}$  线性无关时,  $T\alpha_{1}, T\alpha_{2}, \cdots, T\alpha_{m}$  不一定线性无关.

(iv) 线性变换 T 的像集  $T(V_{n})$  是一个线性空间, 称为线性变换 T 的像空间.

证 设 $\beta_{1},\beta_{2}\in T(V_{n})$ ，则有 $\alpha_{1},\alpha_{2}\in V_{n}$ ，使 $T\pmb{\alpha}_{1} = \pmb{\beta}_{1},T\pmb{\alpha}_{2} = \pmb{\beta}_{2}$ ，从而

$$
\boldsymbol {\beta} _ {1} + \boldsymbol {\beta} _ {2} = T \boldsymbol {\alpha} _ {1} + T \boldsymbol {\alpha} _ {2} = T (\boldsymbol {\alpha} _ {1} + \boldsymbol {\alpha} _ {2}) \in T (V _ {n}) \quad (\text {因} \boldsymbol {\alpha} _ {1} + \boldsymbol {\alpha} _ {2} \in V _ {n}),
$$

$$
\lambda \boldsymbol {\beta} _ {1} = \lambda T \boldsymbol {\alpha} _ {1} = T (\lambda \boldsymbol {\alpha} _ {1}) \in T (V _ {n}) \quad (\text {因} \lambda \boldsymbol {\alpha} _ {1} \in V _ {n}),
$$

由上述证明知它对  $V_{n}$  中的线性运算封闭, 故它是一个线性空间.

证毕

(v) 使 $T\alpha = 0$ 的 $\alpha$ 的全体

152

---

§5 线性变换的矩阵表示式

$$
N _ {T} = \{\alpha \mid \alpha \in V _ {n}, T \alpha = 0 \}
$$

也是一个线性空间. $N_{T}$ 称为线性变换 T 的核.

证 $N_{T} \subseteq V_{n}$, 且易见 $T(\mathbf{0}) = \mathbf{0}$, 故 $\mathbf{0} \in N_{T}, N_{T} \neq \emptyset$.

若  $\alpha_{1},\alpha_{2}\in N_{T}$ ，即  $T\alpha_{1}=0,T\alpha_{2}=0$ ，则  $T(\alpha_{1}+\alpha_{2})=T\alpha_{1}+T\alpha_{2}=0$ ，所以  $\alpha_{1}+\alpha_{2}\in N_{T}$ ;

若  $\alpha_{1}\in N_{T},\lambda\in R$  , 则  $T(\lambda\alpha_{1})=\lambda T\alpha_{1}=\lambda0=0$  , 所以  $\lambda\alpha_{1}\in N_{T}$

以上表明 $N_{T}$ 对 $V_{n}$ 中的线性运算封闭，所以 $N_{T}$ 是一个线性空间. 证毕

例10 设有 $n$ 阶矩阵

$$
\boldsymbol {A} = \left( \begin{array}{c c c c} a _ {1 1} & a _ {1 2} & \dots & a _ {1 n} \\ a _ {2 1} & a _ {2 2} & \dots & a _ {2 n} \\ \vdots & \vdots & & \vdots \\ a _ {n 1} & a _ {n 2} & \dots & a _ {n n} \end{array} \right) = (\boldsymbol {\alpha} _ {1}, \boldsymbol {\alpha} _ {2}, \dots , \boldsymbol {\alpha} _ {n}),
$$

其中

$$
\boldsymbol {\alpha} _ {i} = \left( \begin{array}{c} a _ {1 i} \\ a _ {2 i} \\ \vdots \\ a _ {n i} \end{array} \right),
$$

定义  $R^{n}$  中的变换  $y = T(x)$  为

$$
T (\boldsymbol {x}) = \boldsymbol {A} \boldsymbol {x} \quad (\boldsymbol {x} \in \mathbb {R} ^ {n}),
$$

则 T 为线性变换.

证 设 $a, b \in \mathbb{R}^n$，则

$$
T (\boldsymbol {a} + \boldsymbol {b}) = \boldsymbol {A} (\boldsymbol {a} + \boldsymbol {b}) = \boldsymbol {A} \boldsymbol {a} + \boldsymbol {A} \boldsymbol {b} = T (\boldsymbol {a}) + T (\boldsymbol {b}),
$$

$$
T (\lambda \boldsymbol {a}) = \boldsymbol {A} (\lambda \boldsymbol {a}) = \lambda \boldsymbol {A} \boldsymbol {a} = \lambda T (\boldsymbol {a}).
$$

故 T 是线性变换.

又，T 的像空间就是由  $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{n}$  所生成的向量空间

$$
T (\mathbb {R} ^ {n}) = \{x _ {1} a _ {1} + x _ {2} a _ {2} + \dots + x _ {n} a _ {n} \mid x _ {1}, x _ {2}, \dots , x _ {n} \in \mathbb {R} \},
$$

T 的核  $N_{T}$  就是齐次线性方程组 Ax=0 的解空间.

## § 5 线性变换的矩阵表示式

上节例 10 中, 关系式

$$
T (\boldsymbol {x}) = \boldsymbol {A} \boldsymbol {x} \quad (\boldsymbol {x} \in \mathbb {R} ^ {n})
$$

简单明了地表示出 $\mathbb{R}^n$ 中的一个线性变换. 我们自然希望 $\mathbb{R}^n$ 中任何一个线性变换都能

考研电子书网站:www.pdf2book.com

153

---

\*第6章 线性空间与线性变换

用这样的关系式来表示.为此,考虑到  $\alpha_{1}=Ae_{1},\alpha_{2}=Ae_{2},\cdots,\alpha_{n}=Ae_{n}$  （ $e_{1},e_{2},\cdots,e_{n}$  为单位坐标向量）,即

$$
\boldsymbol {\alpha} _ {i} = T (\boldsymbol {e} _ {i}) \quad (i = 1, 2, \dots , n),
$$

可见如果线性变换 T 有关系式  $T(x)=Ax$ ，那么矩阵 A 应以  $T(e_{i})$  为列向量。反之，如果一个线性变换 T 使  $T(e_{i})=\alpha_{i}\quad(i=1,2,\cdots,n)$ ，那么 T 必有关系式

$$
\begin{array}{l} T (\boldsymbol {x}) = T [ (\boldsymbol {e} _ {1}, \boldsymbol {e} _ {2}, \dots , \boldsymbol {e} _ {n}) \boldsymbol {x} ] = T (x _ {1} \boldsymbol {e} _ {1} + x _ {2} \boldsymbol {e} _ {2} + \dots + x _ {n} \boldsymbol {e} _ {n}). \\ = x _ {1} T (e _ {1}) + x _ {2} T (e _ {2}) + \dots + x _ {n} T (e _ {n}) \\ = (T (\boldsymbol {e} _ {1}), T (\boldsymbol {e} _ {2}), \dots , T (\boldsymbol {e} _ {n})) \boldsymbol {x} = (\boldsymbol {\alpha} _ {1}, \boldsymbol {\alpha} _ {2}, \dots , \boldsymbol {\alpha} _ {n}) \boldsymbol {x} = A \boldsymbol {x}. \\ \end{array}
$$

总之，$\mathbb{R}^n$ 中任何线性变换 $T$ ，都能用关系式

$$
T (\boldsymbol {x}) = \boldsymbol {A} \boldsymbol {x} \quad (\boldsymbol {x} \in \mathbb {R} ^ {n})
$$

表示,其中  $A=(T(\boldsymbol{e}_{1}),T(\boldsymbol{e}_{2}),\cdots,T(\boldsymbol{e}_{n}))$ .

把上面的讨论推广到一般的线性空间,我们有

定义 7 设 T 是线性空间  $V_{n}$  中的线性变换, 在  $V_{n}$  中取定一个基  $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{n}$ , 如果这个基在变换 T 下的像(用这个基线性表示)为

$$
\left\{ \begin{array}{l} T (\boldsymbol {\alpha} _ {1}) = a _ {1 1} \boldsymbol {\alpha} _ {1} + a _ {2 1} \boldsymbol {\alpha} _ {2} + \dots + a _ {n 1} \boldsymbol {\alpha} _ {n}, \\ T (\boldsymbol {\alpha} _ {2}) = a _ {1 2} \boldsymbol {\alpha} _ {1} + a _ {2 2} \boldsymbol {\alpha} _ {2} + \dots + a _ {n 2} \boldsymbol {\alpha} _ {n}, \\ \dots \dots \\ T (\boldsymbol {\alpha} _ {n}) = a _ {1 n} \boldsymbol {\alpha} _ {1} + a _ {2 n} \boldsymbol {\alpha} _ {2} + \dots + a _ {n n} \boldsymbol {\alpha} _ {n}, \end{array} \right.
$$

记  $T(\boldsymbol{\alpha}_{1},\boldsymbol{\alpha}_{2},\cdots,\boldsymbol{\alpha}_{n})=(T(\boldsymbol{\alpha}_{1}),T(\boldsymbol{\alpha}_{2}),\cdots,T(\boldsymbol{\alpha}_{n}))$ ，上式可表示为

$$
T (\alpha_ {1}, \alpha_ {2}, \dots , \alpha_ {n}) = (\alpha_ {1}, \alpha_ {2}, \dots , \alpha_ {n}) A, \tag {5}
$$

其中

$$
\boldsymbol {A} = \left( \begin{array}{c c c c} a _ {1 1} & a _ {1 2} & \dots & a _ {1 n} \\ a _ {2 1} & a _ {2 2} & \dots & a _ {2 n} \\ \vdots & \vdots & & \vdots \\ a _ {n 1} & a _ {n 2} & \dots & a _ {n n} \end{array} \right),
$$

那么 A 就称为线性变换 T 在基  $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{n}$  下的矩阵.

显然,矩阵 A 由基的像  $T(\boldsymbol{\alpha}_{1})$ ,  $T(\boldsymbol{\alpha}_{2})$ ,  $\cdots$ ,  $T(\boldsymbol{\alpha}_{n})$  惟一确定.

如果给出一个矩阵 A 作为线性变换 T 在基  $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{n}$  下的矩阵, 也就是给出了这个基在变换 T 下的像, 那么根据变换 T 保持线性关系的特性, 我们来推导变换 T 必须满足的关系式.

将 $V_{n}$ 中的任意元素记为 $\alpha' = \sum_{i=1}^{n} x_{i} \alpha_{i}$, 有

$$
T \left(\sum_ {i = 1} ^ {n} x _ {i} \pmb {\alpha} _ {i}\right) = \sum_ {i = 1} ^ {n} x _ {i} T (\pmb {\alpha} _ {i})
$$

154

---

§ 5 线性变换的矩阵表示式

$$
= (T (\boldsymbol {\alpha} _ {1}), T (\boldsymbol {\alpha} _ {2}), \dots , T (\boldsymbol {\alpha} _ {n})) \left( \begin{array}{c} x _ {1} \\ x _ {2} \\ \vdots \\ x _ {n} \end{array} \right) = (\boldsymbol {\alpha} _ {1}, \boldsymbol {\alpha} _ {2}, \dots , \boldsymbol {\alpha} _ {n}) A \left( \begin{array}{c} x _ {1} \\ x _ {2} \\ \vdots \\ x _ {n} \end{array} \right),
$$

即

$$
T \left[ (\boldsymbol {\alpha} _ {1}, \boldsymbol {\alpha} _ {2}, \dots , \boldsymbol {\alpha} _ {n}) \left( \begin{array}{c} x _ {1} \\ x _ {2} \\ \vdots \\ x _ {n} \end{array} \right) \right] = (\boldsymbol {\alpha} _ {1}, \boldsymbol {\alpha} _ {2}, \dots , \boldsymbol {\alpha} _ {n}) A \left( \begin{array}{c} x _ {1} \\ x _ {2} \\ \vdots \\ x _ {n} \end{array} \right). \tag {6}
$$

这个关系式惟一地确定一个变换 $T$，可以验证所确定的变换 $T$ 是以 $\pmb{A}$ 为矩阵的线性变换。总之，以 $\pmb{A}$ 为矩阵的线性变换 $T$ 由关系式(6)惟一确定。

定义7和上面一段讨论表明,在 $V_{n}$ 中取定一个基以后,由线性变换 $T$ 可惟一地确定一个矩阵 $\pmb{A}$, 由一个矩阵 $\pmb{A}$ 也可惟一地确定一个线性变换 $T$, 这样, 在线性变换与矩阵之间就有一一对应的关系.

由关系式(6)，可见若  $\alpha$  在基  $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{n}$  下的坐标为

$$
\boldsymbol {x} = \left( \begin{array}{c} x _ {1} \\ x _ {2} \\ \vdots \\ x _ {n} \end{array} \right),
$$

则  $T(\boldsymbol{\alpha})$  在基  $\alpha_{1},\alpha_{2},\cdots,\alpha_{n}$  下的坐标就为  $Ax=A\begin{pmatrix}x_{1}\\x_{2}\\\vdots\\x_{n}\end{pmatrix}$ .

例11 在 $P[x]_3$ 中, 取基

$$
\boldsymbol {p} _ {1} = x ^ {3}, \quad \boldsymbol {p} _ {2} = x ^ {2}, \quad \boldsymbol {p} _ {3} = x, \quad \boldsymbol {p} _ {4} = 1,
$$

求微分运算 D 的矩阵.

解

$$
\left\{ \begin{array}{l} \mathrm{D} \boldsymbol {p} _ {1} = 3 x ^ {2} = 0 \boldsymbol {p} _ {1} + 3 \boldsymbol {p} _ {2} + 0 \boldsymbol {p} _ {3} + 0 \boldsymbol {p} _ {4}, \\ \mathrm{D} \boldsymbol {p} _ {2} = 2 x = 0 \boldsymbol {p} _ {1} + 0 \boldsymbol {p} _ {2} + 2 \boldsymbol {p} _ {3} + 0 \boldsymbol {p} _ {4}, \\ \mathrm{D} \boldsymbol {p} _ {3} = 1 = 0 \boldsymbol {p} _ {1} + 0 \boldsymbol {p} _ {2} + 0 \boldsymbol {p} _ {3} + 1 \boldsymbol {p} _ {4}, \\ \mathrm{D} \boldsymbol {p} _ {4} = 0 = 0 \boldsymbol {p} _ {1} + 0 \boldsymbol {p} _ {2} + 0 \boldsymbol {p} _ {3} + 0 \boldsymbol {p} _ {4}, \end{array} \right.
$$

所以D在这组基下的矩阵为

考研电子书网站:www.pdf2book.com

155

---

\*第6章 线性空间与线性变换

$$
\boldsymbol {A} = \left( \begin{array}{c c c c} 0 & 0 & 0 & 0 \\ 3 & 0 & 0 & 0 \\ 0 & 2 & 0 & 0 \\ \dot {0} & 0 & 1 & 0 \end{array} \right).
$$

例12 在 $\mathbb{R}^3$ 中, $T$ 表示将向量投影到 $xOy$ 平面的线性变换, 即

$$
T (x i + y j + z k) = x i + y j.
$$

(1) 取基为 i, j, k, 求 T 的矩阵;
(2) 取基为  $\alpha=i,\beta=j,\gamma=i+j+k$ ，求 T 的矩阵.

解 (1) $\left\{ \begin{array}{l}Ti = i,\\ Tj = j,\\ Tk = 0, \end{array} \right.$

即

$$
T (\boldsymbol {i}, \boldsymbol {j}, \boldsymbol {k}) = (\boldsymbol {i}, \boldsymbol {j}, \boldsymbol {k}) \left( \begin{array}{c c c} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 0 \end{array} \right).
$$

(2) $\left\{ \begin{array}{l} T\alpha = i = \alpha, \\ T\beta = j = \beta, \\ T\gamma = i + j = \alpha + \beta, \end{array} \right.$

即

$$
T (\boldsymbol {\alpha}, \boldsymbol {\beta}, \boldsymbol {\gamma}) = (\boldsymbol {\alpha}, \boldsymbol {\beta}, \boldsymbol {\gamma}) \left( \begin{array}{c c c} 1 & 0 & 1 \\ 0 & 1 & 1 \\ 0 & 0 & 0 \end{array} \right).
$$

由上例可见,同一个线性变换在不同的基下有不同的矩阵.一般地,我们有

定理 3 设线性空间  $V_{n}$  中取定两个基

$$
\alpha_ {1}, \alpha_ {2}, \dots , \alpha_ {n}; \quad \beta_ {1}, \beta_ {2}, \dots , \beta_ {n},
$$

由基  $\alpha_{1},\alpha_{2},\cdots,\alpha_{n}$  到基  $\beta_{1},\beta_{2},\cdots,\beta_{n}$  的过渡矩阵为 P, $V_{n}$  中的线性变换 T 在这两个基下的矩阵依次为 A 和 B，那么  $B=P^{-1}AP$ .

证 按定理的假设,有

$$
(\boldsymbol {\beta} _ {1}, \boldsymbol {\beta} _ {2}, \dots , \boldsymbol {\beta} _ {n}) = (\boldsymbol {\alpha} _ {1}, \boldsymbol {\alpha} _ {2}, \dots , \boldsymbol {\alpha} _ {n}) \boldsymbol {P},
$$

$\pmb{P}$ 可逆;及

$$
\begin{array}{l} T (\boldsymbol {\alpha} _ {1}, \boldsymbol {\alpha} _ {2}, \dots , \boldsymbol {\alpha} _ {n}) = (\boldsymbol {\alpha} _ {1}, \boldsymbol {\alpha} _ {2}, \dots , \boldsymbol {\alpha} _ {n}) \boldsymbol {A}, \\ T (\boldsymbol {\beta} _ {1}, \boldsymbol {\beta} _ {2}, \dots , \boldsymbol {\beta} _ {n}) = (\boldsymbol {\beta} _ {1}, \boldsymbol {\beta} _ {2}, \dots , \boldsymbol {\beta} _ {n}) \boldsymbol {B}, \\ \end{array}
$$

于是

$$
(\boldsymbol {\beta} _ {1}, \boldsymbol {\beta} _ {2}, \dots , \boldsymbol {\beta} _ {n}) \boldsymbol {B} = T (\boldsymbol {\beta} _ {1}, \boldsymbol {\beta} _ {2}, \dots , \boldsymbol {\beta} _ {n}) = T [ (\boldsymbol {\alpha} _ {1}, \boldsymbol {\alpha} _ {2}, \dots , \boldsymbol {\alpha} _ {n}) \boldsymbol {P} ]
$$

156

---

习题六

$$
\begin{array}{l} = \left[ T \left(\alpha_ {1}, \alpha_ {2}, \dots , \alpha_ {n}\right) \right] P = \left(\alpha_ {1}, \alpha_ {2}, \dots , \alpha_ {n}\right) A P \\ = (\boldsymbol {\beta} _ {1}, \boldsymbol {\beta} _ {2}, \dots , \boldsymbol {\beta} _ {n}) \boldsymbol {P} ^ {- 1} \boldsymbol {A} \boldsymbol {P}, \\ \end{array}
$$

因为 $\beta_{1},\beta_{2},\cdots,\beta_{n}$ 线性无关,所以

$$
\boldsymbol {B} = \boldsymbol {P} ^ {- 1} \boldsymbol {A} \boldsymbol {P}.
$$

证毕

这定理表明 A 与 B 相似,且两个基之间的过渡矩阵 P 就是相似变换矩阵.

例 13 设  $V_{2}$  中的线性变换 T 在基  $\alpha_{1}, \alpha_{2}$  下的矩阵为

$$
\boldsymbol {A} = \left( \begin{array}{c c} a _ {1 1} & a _ {1 2} \\ a _ {2 1} & a _ {2 2} \end{array} \right),
$$

求 T 在基  $\alpha_{2}, \alpha_{1}$  下的矩阵.

解  $(\boldsymbol{\alpha}_{2},\boldsymbol{\alpha}_{1})=(\boldsymbol{\alpha}_{1},\boldsymbol{\alpha}_{2})\begin{pmatrix}0&1\\1&0\end{pmatrix},$

即  $P=\begin{pmatrix}0&1\\ 1&0\end{pmatrix}$ ，求得  $P^{-1}=\begin{pmatrix}0&1\\ 1&0\end{pmatrix}$ ，于是 T 在基  $(\boldsymbol{\alpha}_{2},\boldsymbol{\alpha}_{1})$  下的矩阵为

$$
\boldsymbol {B} = \left( \begin{array}{c c} 0 & 1 \\ 1 & 0 \end{array} \right) \left( \begin{array}{c c} a _ {1 1} & a _ {1 2} \\ a _ {2 1} & a _ {2 2} \end{array} \right) \left( \begin{array}{c c} 0 & 1 \\ 1 & 0 \end{array} \right) = \left( \begin{array}{c c} a _ {2 1} & a _ {2 2} \\ a _ {1 1} & a _ {1 2} \end{array} \right) \left( \begin{array}{c c} 0 & 1 \\ 1 & 0 \end{array} \right) = \left( \begin{array}{c c} a _ {2 2} & a _ {2 1} \\ a _ {1 2} & a _ {1 1} \end{array} \right).
$$

定义 8 线性变换 T 的像空间  $T(V_{n})$  的维数, 称为线性变换 T 的秩.

显然,若 A 是 T 的矩阵,则 T 的秩就是  $R(A)$ .

若 T 的秩为 r，则 T 的核  $N_{T}$  的维数为 n-r.

## 习题六

1. 验证:

(1) 2 阶矩阵的全体  $S_{1}$ ;
(2) 主对角线上的元素之和等于 0 的 2 阶矩阵的全体  $S_{2}$ ;
(3) 2 阶对称矩阵的全体  $S_{3}$ ,

对于矩阵的加法和数乘运算构成线性空间,并写出各个空间的一个基.

2. 验证: 与向量 $(0,0,1)^{T}$ 不平行的全体3维数组向量, 对于数组向量的加法和数乘运算不构成线性空间.

3. 在线性空间 $P[x]_3$ 中, 下列向量组是否为一个基?

(1) I:  $1 + x, x + x^{2}, 1 + x^{3}, 2 + 2x + x^{2} + x^{3}$ ;
(2) Ⅱ:  $-1+x,1-x^{2},-2+2x+x^{2},x^{3}.$

4. 在  $R^{3}$  中求向量  $\boldsymbol{\alpha}=(7,3,1)^{\mathrm{T}}$  在基

$$
\boldsymbol {\alpha} _ {1} = (1, 3, 5) ^ {\mathrm{T}}, \quad \boldsymbol {\alpha} _ {2} = (6, 3, 2) ^ {\mathrm{T}}, \quad \boldsymbol {\alpha} _ {3} = (3, 1, 0) ^ {\mathrm{T}}
$$

深入探究

157

---

\*第6章 线性空间与线性变换

中的坐标.

5. 在 $\mathbb{R}^3$ 中, 取两个基

$$
\boldsymbol {\alpha} _ {1} = (1, 2, 1) ^ {\mathrm{T}}, \quad \boldsymbol {\alpha} _ {2} = (2, 3, 3) ^ {\mathrm{T}}, \quad \boldsymbol {\alpha} _ {3} = (3, 7, - 2) ^ {\mathrm{T}};
$$

$$
\boldsymbol {\beta} _ {1} = (3, 1, 4) ^ {\mathrm{T}}, \quad \boldsymbol {\beta} _ {2} = (5, 2, 1) ^ {\mathrm{T}}, \quad \boldsymbol {\beta} _ {3} = (1, 1, - 6) ^ {\mathrm{T}},
$$

试求坐标变换公式.

6. 在 $\mathbb{R}^4$ 中取两个基

$$
\left\{ \begin{array}{l} \boldsymbol {e} _ {1} = (1, 0, 0, 0) ^ {\mathrm{T}}, \\ \boldsymbol {e} _ {2} = (0, 1, 0, 0) ^ {\mathrm{T}}, \\ \boldsymbol {e} _ {3} = (0, 0, 1, 0) ^ {\mathrm{T}}, \\ \boldsymbol {e} _ {4} = (0, 0, 0, 1) ^ {\mathrm{T}}, \end{array} \right. \quad \left\{ \begin{array}{l} \boldsymbol {\alpha} _ {1} = (2, 1, - 1, 1) ^ {\mathrm{T}}, \\ \boldsymbol {\alpha} _ {2} = (0, 3, 1, 0) ^ {\mathrm{T}}, \\ \boldsymbol {\alpha} _ {3} = (5, 3, 2, 1) ^ {\mathrm{T}}, \\ \boldsymbol {\alpha} _ {4} = (6, 6, 1, 3) ^ {\mathrm{T}}. \end{array} \right.
$$

(1) 求由前一个基到后一个基的过渡矩阵；
(2) 求向量 $(x_{1}, x_{2}, x_{3}, x_{4})^{T}$ 在后一个基中的坐标；
(3) 求在两个基中有相同坐标的向量.

7. 设线性空间 $S_{1}$ （习题六第1题(1))中向量

$$
\boldsymbol {a} _ {1} = \left( \begin{array}{c c} 1 & 2 \\ 1 & 0 \end{array} \right), \quad \boldsymbol {a} _ {2} = \left( \begin{array}{c c} - 1 & - 1 \\ 1 & 1 \end{array} \right), \quad \boldsymbol {b} _ {1} = \left( \begin{array}{c c} 1 & 3 \\ 3 & 1 \end{array} \right), \quad \boldsymbol {b} _ {2} = \left( \begin{array}{c c} 2 & - 1 \\ 4 & 1 \end{array} \right),
$$

(1) 问  $b_{1}$  能否由  $a_{1}, a_{2}$  线性表示？ $b_{2}$  能否由  $a_{1}, a_{2}$  线性表示？
(2) 求由向量组  $a_{1}, a_{2}, b_{1}, b_{2}$  所生成的向量空间 L 的维数和一个基.

8. 说明 $xOy$ 平面上变换 $T\begin{pmatrix} x \\ y \end{pmatrix} = A\begin{pmatrix} x \\ y \end{pmatrix}$ 的几何意义, 其中

(1)  $A = \begin{pmatrix} -1 & 0 \\ 0 & 1 \end{pmatrix};$

(2)  $A = \begin{pmatrix} 0 & 0 \\ 0 & 1 \end{pmatrix}$ ;

(3)  $A = \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix}$ ;

(4)  $A=\begin{pmatrix}0&1\\-1&0\end{pmatrix}.$

9. $n$ 阶对称矩阵的全体 $V$ 对于矩阵的线性运算构成一个 $\frac{n(n + 1)}{2}$ 维线性空间. 给出 $n$ 阶可逆矩阵 $P$, 以 $A$ 表示 $V$ 中的任一元素, 试证合同变换

$$
T (\boldsymbol {A}) = \boldsymbol {P} ^ {\mathrm{T}} \boldsymbol {A} \boldsymbol {P}
$$

是 V 中的线性变换.

10. 函数集合

$$
V _ {3} = \left\{\left(a _ {2} x ^ {2} + a _ {1} x + a _ {0}\right) \mathrm{e} ^ {x} \mid a _ {2}, a _ {1}, a _ {0} \in \mathbb {R} \right\}
$$

对于函数的线性运算构成3维线性空间.在 $V_{3}$ 中取一个基

$$
\alpha_ {1} = x ^ {2} \mathrm{e} ^ {x}, \quad \alpha_ {2} = x \mathrm{e} ^ {x}, \quad \alpha_ {3} = \mathrm{e} ^ {x},
$$

求微分运算 D 在这个基下的矩阵.

11.2 阶对称矩阵的全体

$$
V _ {3} = \left\{\left( \begin{array}{c c} x _ {1} & x _ {2} \\ x _ {2} & x _ {3} \end{array} \right) \Bigg | x _ {1}, x _ {2}, x _ {3} \in \mathbb {R} \right\}
$$

对于矩阵的线性运算构成3维线性空间.在 $V_{3}$ 中取一个基

158

---

习题六

$$
\boldsymbol {A} _ {1} = \left( \begin{array}{c c} 1 & 0 \\ 0 & 0 \end{array} \right), \quad \boldsymbol {A} _ {2} = \left( \begin{array}{c c} 0 & 1 \\ 1 & 0 \end{array} \right), \quad \boldsymbol {A} _ {3} = \left( \begin{array}{c c} 0 & 0 \\ 0 & 1 \end{array} \right),
$$

在 $V_{3}$ 中定义合同变换

$$
T (\boldsymbol {A}) = \left( \begin{array}{c c} 1 & 0 \\ 1 & 1 \end{array} \right) \boldsymbol {A} \left( \begin{array}{c c} 1 & 1 \\ 0 & 1 \end{array} \right),
$$

求 T 在基  $A_{1}, A_{2}, A_{3}$  下的矩阵.

12. 次数不超过 2 的全体实系数多项式对于多项式的线性运算构成一个线性空间 $V$. 在 $V$ 上定义变换 $T(a_0 + a_1x + a_2x^2) = \left(a_0 + \frac{1}{2}a_2\right) + \left(a_1 - \frac{1}{2}a_2\right)x + \frac{1}{2}a_2x^2$.

(1) 试证 T 是 V 中的线性变换；
(2) 求 T 在基  $1, x, x^{2}$  下的矩阵；
(3) 设 W 为 V 的子空间, 且满足对任意  $p(x) \in W$ , 总有  $T(p(x)) = p(x)$ , 求子空间 W 的维数的最大值.
13. 已知 n 维线性空间 V 中的线性变换 T 在 V 的某个基  $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{n}$  下的矩阵为 A，若  $A^{2} = A$ ，证明:存在线性空间 V 的一个基  $\beta_{1}, \beta_{2}, \cdots, \beta_{n}$ ，使得 T 在这个基下的矩阵为对角矩阵.

考研电子书网站:www.pdf2book.com

159

---

## 部分习题参考答案

## 习题一

1. (1) -4; (2) $3abc - a^3 - b^3 - c^3$; (3) $(a - b)(b - c)(c - a)$; (4) $-2(x^3 + y^3)$.
2. (1) 0; (2) 4; (3) 5; (4) 3; (5) $\frac{n(n - 1)}{2}$; (6) $n(n - 1)$.

3.  $-a_{11}a_{23}a_{32}a_{44}, a_{11}a_{23}a_{34}a_{42}.$

4. (1) 0; (2) 0; (3) 4abcdef; (4) 0; (5) abcd+ab+cd+ad+1; (6) 16.

5. (1) $x = -3$ 或 $x = \pm \sqrt{3}$; (2) $x = a, x = b$ 或 $x = c$.

8. (1) $a^{n-2}(a^2 - 1)$; (2) $[x + (n - 1)a](x - a)^{n-1}$; (3) $\prod_{n+1 \geqslant i > j \geqslant 1} (i - j)$;
(4)  $\prod_{i=1}^{n}(a_{i}d_{i}-b_{i}c_{i})$ ; (5)  $1+a_{1}+\cdots+a_{n}$ ; (6)  $(-1)^{n-1}(n-1)2^{n-2}$ ;
(7) $a_{1}a_{2}\cdots a_{n}\left(1+\sum_{i=1}^{n}\frac{1}{a_{i}}\right).$

9. 24.

## 习题二

1. (1)  $\begin{pmatrix}35 \\6 \\49\end{pmatrix}$ ; (2) 10; (3)  $\begin{pmatrix}-2 & 4 \\-1 & 2 \\-3 & 6\end{pmatrix}$ ; (4)  $\begin{pmatrix}6 & -7 & 8 \\20 & -5 & -6\end{pmatrix}$ ;
(5) $a_{11}x_1^2 + a_{22}x_2^2 + a_{33}x_3^2 + 2a_{12}x_1x_2 + 2a_{13}x_1x_3 + 2a_{23}x_2x_3.$

160

---

部分习题参考答案

2. $3\boldsymbol{A}\boldsymbol{B} - 2\boldsymbol{A} = \begin{pmatrix} -2 & 13 & 22\\ -2 & -17 & 20\\ 4 & 29 & -2 \end{pmatrix},\boldsymbol{A}^{\mathrm{T}}\boldsymbol {B} = \begin{pmatrix} 0 & 5 & 8\\ 0 & -5 & 6\\ 2 & 9 & 0 \end{pmatrix}.$

3. $\left\{ \begin{array}{l}x_{1} = -6z_{1} + z_{2} + 3z_{3},\\ x_{2} = 12z_{1} - 4z_{2} + 9z_{3},\\ x_{3} = -10z_{1} - z_{2} + 16z_{3}. \end{array} \right.$

5. (1) 取  $A = \begin{pmatrix} 1 & 1 \\ -1 & -1 \end{pmatrix} \neq O$  而  $A^{2} = O$ ;

(2) 取  $A = \begin{pmatrix} 1 & 0 \\ 0 & 0 \end{pmatrix}$ ，有  $A \neq O, A \neq E$  而  $A^{2} = A$ ;

(3) 取  $A=\begin{pmatrix}1&0\\0&0\end{pmatrix},X=\begin{pmatrix}1&0\\0&0\end{pmatrix},Y=\begin{pmatrix}1&0\\0&1\end{pmatrix}$ ，有  $X \neq Y$  而 AX = AY.

6. (1) $A^2 = \begin{pmatrix} 1 & 0 \\ 2\lambda & 1 \end{pmatrix}, A^3 = \begin{pmatrix} 1 & 0 \\ 3\lambda & 1 \end{pmatrix}, \dots, A^k = \begin{pmatrix} 1 & 0 \\ k\lambda & 1 \end{pmatrix}$;

(2) $\begin{pmatrix}\lambda^{4}&4\lambda^{3}&6\lambda^{2}\\0&\lambda^{4}&4\lambda^{3}\\0&0&\lambda^{4}\end{pmatrix}.$

7. (1) $10^{25}E, 10^{25}\left( \begin{array}{cc}3 & 1\\ 1 & -3 \end{array} \right);\quad (2) - 8^{99}\left( \begin{array}{ccc}2 & 4 & 8\\ 1 & 2 & 4\\ -3 & -6 & -12 \end{array} \right).$

9. (1) $\begin{pmatrix}5 & -2 \\ -2 & 1\end{pmatrix}; \quad (2)\begin{pmatrix}\cos\theta & \sin\theta \\ -\sin\theta & \cos\theta\end{pmatrix};$

(3) $\begin{pmatrix}-2&1&0\\-\frac{13}{2}&3&-\frac{1}{2}\\-16&7&-1\end{pmatrix};$  (4) $\begin{pmatrix}\frac{1}{a_{1}}&&0\\&&\frac{1}{a_{2}}&&\\&&\ddots&&\\0&&\frac{1}{a_{n}}\end{pmatrix}.$

10.  $\left\{\begin{aligned}y_{1}&=-7x_{1}-4x_{2}+9x_{3},\\ y_{2}&=6x_{1}+3x_{2}-7x_{3},\\ y_{3}&=3x_{1}+2x_{2}-4x_{3}.\end{aligned}\right.$

13. $A^{-1} = \frac{1}{2} (A - E), (A + 2E)^{-1} = \frac{1}{4} (3E - A)$.

14. (1) $X = \begin{pmatrix} 2 & -23 \\ 0 & 8 \end{pmatrix}$; (2) $X = \begin{pmatrix} -2 & 2 & 1 \\ -\frac{8}{3} & 5 & -\frac{2}{3} \end{pmatrix}$; (3) $X = \begin{pmatrix} 1 & 1 \\ \frac{1}{4} & 0 \end{pmatrix}$;

(4) $X=\frac{1}{3}\left(\begin{array}{ccc}23&-7&-13\\-22&5&14\end{array}\right).$

考研电子书网站:www.pdf2book.com

161

---

部分习题参考答案

15. (1)  $\left\{\begin{aligned}x_{1}&=1,\\ x_{2}&=0,\\ x_{3}&=0;\end{aligned}\right.$  (2)  $\left\{\begin{aligned}x_{1}&=2,\\ x_{2}&=-\frac{1}{2},\\ x_{3}&=\frac{1}{2}.\end{aligned}\right.$
16. -16.
17. $\begin{pmatrix}0&3&3\\-1&2&3\\1&1&0\end{pmatrix}.$
18.  $B = A + E = \begin{pmatrix} 2 & 0 & 1 \\ 0 & 3 & 0 \\ 1 & 0 & 2 \end{pmatrix}.$
19.  $B=2A=2\mathrm{diag}(1,-2,1)$ .
20. $B = \mathrm{diag}(6,6,6, - 1)$
21. $\frac{1}{3}\left( \begin{array}{cc}1 + 2^{13} & 4 + 2^{13}\\ -1 - 2^{11} & -4 - 2^{11} \end{array} \right) = \left( \begin{array}{cc}2731 & 2732\\ -683 & -684 \end{array} \right).$
22.  $4\begin{pmatrix}1&1&1\\1&1&1\\1&1&1\end{pmatrix}.$
25. $\begin{pmatrix}1&2&5&2\\0&1&2&-4\\0&0&-4&3\\0&0&0&-9\end{pmatrix}.$
26. $|A^8| = 10^{16}, A^4 = \begin{pmatrix} 5^4 & 0 & 0 & 0 \\ 0 & 5^4 & 0 & 0 \\ 0 & 0 & 2^4 & 0 \\ 0 & 0 & 2^6 & 2^4 \end{pmatrix}$.
27. $\left( \begin{array}{cc}O & B^{-1}\\ A^{-1} & O \end{array} \right).$
28. (1) $\begin{pmatrix} 1 & -2 & 0 & 0 \\ -2 & 5 & 0 & 0 \\ 0 & 0 & 2 & -3 \\ 0 & 0 & -5 & 8 \end{pmatrix},$. (2) $\frac{1}{2}\begin{pmatrix} 0 & 3 & -1 \\ 0 & -4 & 2 \\ 10 & 0 & 0 \end{pmatrix}.$

162

---

部分习题参考答案

## 习题三

1. (1) $\begin{pmatrix} 1 & 0 & 0 & 5 \\ 0 & 0 & 1 & -3 \\ 0 & 0 & 0 & 0 \end{pmatrix}$; (2) $\begin{pmatrix} 0 & 1 & 0 & 5 \\ 0 & 0 & 1 & 3 \\ 0 & 0 & 0 & 0 \end{pmatrix}$;

(3) $\begin{pmatrix}1&-1&0&2&-3\\0&0&1&-2&2\\0&0&0&0&0\\0&0&0&0&.0\end{pmatrix};$  (4) $\begin{pmatrix}1&0&2&0&-2\\0&1&-1&0&3\\0&0&0&1&4\\0&0&0&0&0\end{pmatrix}.$

2.  $P = \begin{pmatrix} -3 & 2 & 0 \\ 2 & -1 & 0 \\ 7 & -6 & 1 \end{pmatrix}$ ,  $PA = \begin{pmatrix} 1 & 0 & -1 & -2 \\ 0 & 1 & 2 & 3 \\ 0 & 0 & 0 & 0 \end{pmatrix}$ .

3. (1) $P = \begin{pmatrix} 1 & 3 \\ 2 & 5 \end{pmatrix}$, $PA = \begin{pmatrix} 1 & 0 & 4 \\ 0 & 1 & 7 \end{pmatrix}$; (2) $Q = \begin{pmatrix} 1 & 2 & 0 \\ 3 & 5 & 0 \\ -4 & -7 & 1 \end{pmatrix}$, $QA^{\mathrm{T}} = \begin{pmatrix} 1 & 0 \\ 0 & 1 \\ 0 & 0 \end{pmatrix}$.

4. (1) $\begin{pmatrix} \frac{7}{6} & \frac{2}{3} & -\frac{3}{2} \\ -1 & -1 & 2 \\ -\frac{1}{2} & 0 & \frac{1}{2} \end{pmatrix}$; (2) $\begin{pmatrix} 1 & 1 & -2 & -4 \\ 0 & 1 & 0 & -1 \\ -1 & -1 & 3 & 6 \\ 2 & 1 & -6 & -10 \end{pmatrix}$.

5. $\begin{pmatrix}x_{1}\\x_{2}\\x_{3}\end{pmatrix}=\begin{pmatrix}2\\-\frac{1}{2}\\\frac{1}{2}\end{pmatrix}.$

6. (1) $\begin{pmatrix} 10 & 2 \\ -15 & -3 \\ 12 & 4 \end{pmatrix}$; (2) $\begin{pmatrix} 2 & -1 & -1 \\ -4 & 7 & 4 \end{pmatrix}$; (3) $\begin{pmatrix} 0 & 1 & -1 \\ -1 & 0 & 1 \\ 1 & -1 & 0 \end{pmatrix}$.

7. 都可能有.

8. $R(\mathbf{A})\geqslant R(\mathbf{B})\geqslant R(\mathbf{A}) - 1.$

考研电子书网站:www.pdf2book.com

163

---

部分习题参考答案

9. $\begin{pmatrix}1&0&1&0&0\\1&-1&0&0&0\\0&0&1&0&0\\0&0&0&1&0\\0&0&0&0&0\end{pmatrix}.$

10. (1) R=2; (2) R=3; (3) R=3.
12. (1) $k = 1$; (2) $k = -2$; (3) $k \neq 1$ 且 $k \neq -2$.

14. (1) $\begin{pmatrix} x_1 \\ x_2 \\ x_3 \\ x_4 \end{pmatrix} = c \begin{pmatrix} \frac{4}{3} \\ -3 \\ \frac{4}{3} \\ 1 \end{pmatrix} (c \in \mathbb{R})$; (2) $\begin{pmatrix} x_1 \\ x_2 \\ x_3 \\ x_4 \end{pmatrix} = c_1 \begin{pmatrix} -2 \\ 1 \\ 0 \\ 0 \end{pmatrix} + c_2 \begin{pmatrix} 1 \\ 0 \\ 0 \\ 1 \end{pmatrix} (c_1, c_2 \in \mathbb{R})$;

(3) $\begin{pmatrix} x_1 \\ x_2 \\ x_3 \\ x_4 \end{pmatrix} = c \begin{pmatrix} -\frac{1}{2} \\ \frac{7}{2} \\ \frac{5}{2} \\ 1 \end{pmatrix} (c \in \mathbb{R})$; (4) $\begin{pmatrix} x_1 \\ x_2 \\ x_3 \\ x_4 \end{pmatrix} = c_1 \begin{pmatrix} \frac{3}{17} \\ \frac{19}{17} \\ 1 \\ 0 \end{pmatrix} + c_2 \begin{pmatrix} -\frac{13}{17} \\ -\frac{20}{17} \\ 0 \\ 1 \end{pmatrix} (c_1, c_2 \in \mathbb{R})$.

15.（1）无解；（2） $\begin{pmatrix}x\\y\\z\end{pmatrix}=c\begin{pmatrix}-2\\1\\1\end{pmatrix}+\begin{pmatrix}-1\\2\\0\end{pmatrix}\quad(c\in\mathbb{R})$ ;

(3) $\begin{pmatrix} x \\ y \\ z \\ w \end{pmatrix} = c_1 \begin{pmatrix} -\frac{1}{2} \\ 1 \\ 0 \\ 0 \end{pmatrix} + c_2 \begin{pmatrix} \frac{1}{2} \\ 0 \\ 1 \\ 0 \end{pmatrix} + \begin{pmatrix} \frac{1}{2} \\ 0 \\ 0 \\ 0 \end{pmatrix}$ ($c_1, c_2 \in \mathbb{R}$);
(4) $\begin{pmatrix} x \\ y \\ z \\ w \end{pmatrix} = c_1 \begin{pmatrix} \frac{1}{7} \\ \frac{5}{7} \\ 1 \\ 0 \end{pmatrix} + c_2 \begin{pmatrix} \frac{1}{7} \\ -\frac{9}{7} \\ 0 \\ 1 \end{pmatrix} + \begin{pmatrix} \frac{6}{7} \\ -\frac{5}{7} \\ 0 \\ 0 \end{pmatrix}$ ($c_1, c_2 \in \mathbb{R}$).

164

---

部分习题参考答案

16. $\left\{ \begin{array}{l}x_{1} - 2x_{3} + 2x_{4} = 0,\\ x_{2} + 3x_{3} - 4x_{4} = 0. \end{array} \right.$

17. (1) $\lambda \neq -\frac{1}{2}$ 且 $\lambda \neq 2$; (2) $\lambda = -\frac{1}{2}$;

(3) $\lambda = 2, \begin{pmatrix} x_1 \\ x_2 \\ x_3 \end{pmatrix} = c \begin{pmatrix} -1 \\ 1 \\ 0 \end{pmatrix} + \begin{pmatrix} 3 \\ 0 \\ 1 \end{pmatrix} (c \in \mathbb{R}).$

18. (1) $\lambda \neq 1$, 且 $\lambda \neq -2$; (2) $\lambda = -2$;

(3) $\lambda = 1$, $\begin{pmatrix} x_1 \\ x_2 \\ x_3 \end{pmatrix} = c_1 \begin{pmatrix} -1 \\ 1 \\ 0 \end{pmatrix} + c_2 \begin{pmatrix} -1 \\ 0 \\ 1 \end{pmatrix} + \begin{pmatrix} 1 \\ 0 \\ 0 \end{pmatrix}$ ($c_1, c_2 \in \mathbb{R}$).

19. $\lambda = 1$ 时有解 $\begin{pmatrix} x_1 \\ x_2 \\ x_3 \end{pmatrix} = c \begin{pmatrix} 1 \\ 1 \\ 1 \end{pmatrix} + \begin{pmatrix} 1 \\ 0 \\ 0 \end{pmatrix}, \lambda = -2$ 时有解 $\begin{pmatrix} x_1 \\ x_2 \\ x_3 \end{pmatrix} = c \begin{pmatrix} 1 \\ 1 \\ 1 \end{pmatrix} + \begin{pmatrix} 2 \\ 2 \\ 0 \end{pmatrix} (c \in \mathbb{R})$.

20. $\lambda \neq 1$ ，且 $\lambda \neq 10$ 时有惟一解； $\lambda = 10$ 时无解； $\lambda = 1$ 时有无限多解，解为

$$
\left( \begin{array}{c} x _ {1} \\ x _ {2} \\ x _ {3} \end{array} \right) = c _ {1} \left( \begin{array}{c} - 2 \\ 1 \\ 0 \end{array} \right) + c _ {2} \left( \begin{array}{c} 2 \\ 0 \\ 1 \end{array} \right) + \left( \begin{array}{c} 1 \\ 0 \\ 0 \end{array} \right) (c _ {1}, c _ {2} \in \mathbb {R}).
$$

## 习题四

3.（1）线性相关；（2）线性无关.

4. $a = 2$ 或 $a = -1$.

6.  $b = c a_{1} - (1 + c) a_{2}, c \in R$ .

7. 若  $a_{1}=\begin{pmatrix}1\\0\end{pmatrix},a_{2}=\begin{pmatrix}0\\0\end{pmatrix};b_{1}=\begin{pmatrix}0\\0\end{pmatrix},b_{2}=\begin{pmatrix}0\\1\end{pmatrix}$ ，则  $a_{1}+b_{1},a_{2}+b_{2}$  线性无关.

11.（1）线性无关；（2）线性无关；（3）线性相关.

13. (1) $2, \pmb{a}_{1}, \pmb{a}_{2}$; (2) $2, \pmb{a}_{1}, \pmb{a}_{2}$.

14. (1) $a_{1}, a_{2}, a_{3}$ 为最大无关组, $a_{4} = \frac{8}{5} a_{1} - a_{2} + 2a_{3}$;

(2) $a_{1},a_{2},a_{3}$ 为最大无关组, $a_{4}=a_{1}+3a_{2}-a_{3},a_{5}=-a_{2}+a_{3}.$

15. a=2, b=5.

考研电子书网站:www.pdf2book.com

165

---

部分习题参考答案

16. $R_{D} = 3$

20. (1)  $B=\begin{pmatrix}0&0&0\\1&0&3\\0&1&-1\end{pmatrix};$  (2)  $|A|=0.$

21. $V_{1}$ 是, $V_{2}$ 不是.

23.  $v_{1}=2a_{1}+3a_{2}-a_{3},v_{2}=3a_{1}-3a_{2}-2a_{3}.$

24. (1) $\begin{pmatrix}2&3&4\\0&-1&0\\-1&0&-1\end{pmatrix};$  (2) $\begin{pmatrix}-8\\-1\\5\end{pmatrix}.$

25. (1) $\xi_{1} = \begin{pmatrix} 0 \\ 1 \\ 0 \\ 4 \end{pmatrix}$, $\xi_{2} = \begin{pmatrix} -4 \\ 0 \\ 1 \\ -3 \end{pmatrix}$; (2) $\xi_{1} = \begin{pmatrix} 1 \\ 7 \\ 0 \\ 19 \end{pmatrix}$, $\xi_{2} = \begin{pmatrix} 0 \\ 0 \\ 1 \\ 2 \end{pmatrix}$;

(3) $(\boldsymbol{\xi}_{1},\boldsymbol{\xi}_{2},\cdots,\boldsymbol{\xi}_{n-1})=\begin{pmatrix}1&&&\\&1&&\\&&\ddots&&\\&&&1\\-n&-n+1&\cdots&-2\end{pmatrix}.$

26. $\begin{pmatrix}1&0\\5&2\\8&1\\0&1\end{pmatrix}.$

27.  $\left\{\begin{aligned}x_{1}-2x_{2}+x_{3}&=0,\\ 2x_{1}-3x_{2}+x_{4}&=0.\end{aligned}\right.$

28. (1) $\mathrm{I}:\pmb{\xi}_1 = \begin{pmatrix} -1 \\ 1 \\ 0 \\ 1 \end{pmatrix},\pmb{\xi}_2 = \begin{pmatrix} 0 \\ 0 \\ 1 \\ 0 \end{pmatrix};\mathrm{II}:\pmb{\xi}_1 = \begin{pmatrix} 1 \\ 1 \\ 0 \\ -1 \end{pmatrix},\pmb{\xi}_2 = \begin{pmatrix} -1 \\ 0 \\ 1 \\ 1 \end{pmatrix};$ (2) $x = c\left( \begin{array}{c} -1\\ 1\\ 2\\ 1 \end{array} \right)(c\in \mathbb{R}).$

31. (1) $\boldsymbol{\eta} = \begin{pmatrix} -8 \\ 13 \\ 0 \\ 2 \end{pmatrix}, \boldsymbol{\xi} = \begin{pmatrix} -1 \\ 1 \\ 1 \\ 0 \end{pmatrix}$; (2) $\boldsymbol{\eta} = \begin{pmatrix} -17 \\ 0 \\ 14 \\ 0 \end{pmatrix}, \boldsymbol{\xi}_1 = \begin{pmatrix} -9 \\ 1 \\ 7 \\ 0 \end{pmatrix}, \boldsymbol{\xi}_2 = \begin{pmatrix} -4 \\ 0 \\ \frac{7}{2} \\ 1 \end{pmatrix}$.

166

---

部分习题参考答案

32.  $x=c\begin{pmatrix}3\\4\\5\\6\end{pmatrix}+\begin{pmatrix}2\\3\\4\\5\end{pmatrix}\quad(c\in\mathbb{R}).$

33. (1) $\alpha = -4$ 且 $\beta \neq 0$; (2) $\alpha \neq -4$;

(3)  $\alpha = -4$ , 且  $\beta = 0, b = ca_{1} - (2c + 1)a_{2} + a_{3} \quad (c \in \mathbb{R})$ .

35.  $x=c\begin{pmatrix}1\\-2\\1\\0\end{pmatrix}+\begin{pmatrix}1\\1\\1\\1\end{pmatrix}\quad(c\in\mathbb{R}).$

## 习题五

1. $\lambda = -2, c = (-2, 2, -1)^{\mathrm{T}}$.

2. (1)  $p_{1}=\frac{1}{\sqrt{3}}\begin{pmatrix}1\\1\\1\end{pmatrix},p_{2}=\frac{1}{\sqrt{2}}\begin{pmatrix}-1\\0\\1\end{pmatrix},p_{3}=\frac{1}{\sqrt{6}}\begin{pmatrix}1\\-2\\1\end{pmatrix};$

(2) $p_{1}=\frac{1}{\sqrt{3}}\left(\begin{array}{c}1\\0\\-1\\1\end{array}\right),p_{2}=\frac{1}{\sqrt{15}}\left(\begin{array}{c}1\\-3\\2\\1\end{array}\right),p_{3}=\frac{1}{\sqrt{35}}\left(\begin{array}{c}-1\\3\\3\\4\end{array}\right).$

3.（1）不是； （2）是

6. (1)  $\lambda = -1$  为三重根,  $p = \begin{pmatrix} 1 \\ 1 \\ -1 \end{pmatrix}$ ;

(2) $\lambda_{1} = -1, \lambda_{2} = 9, \lambda_{3} = 0, \boldsymbol{p}_{1} = \begin{pmatrix} -1 \\ 1 \\ 0 \end{pmatrix}, \boldsymbol{p}_{2} = \begin{pmatrix} 1 \\ 1 \\ 2 \end{pmatrix}, \boldsymbol{p}_{3} = \begin{pmatrix} -1 \\ -1 \\ 1 \end{pmatrix};$

(3) $\lambda_{1} = \lambda_{2} = 1, \lambda_{3} = \lambda_{4} = -1, (\boldsymbol{p}_{1}, \boldsymbol{p}_{2}, \boldsymbol{p}_{3}, \boldsymbol{p}_{4}) = \begin{pmatrix} 1 & 0 & 0 & -1 \\ 0 & 1 & -1 & 0 \\ 0 & 1 & 1 & 0 \\ 1 & 0 & 0 & 1 \end{pmatrix}$.

167

---

部分习题参考答案

12. 18.

13. 25.

15. x = 3.

16. (1) $a = -3, b = 0, \lambda = -1$; (2) 不能.

17. $A^{100} = \left( \begin{array}{ccc}1 & 0 &  & 5^{100} - 1\\ 0 & 5^{100} &  & 0\\ 0 & 0 &  & 5^{100} \end{array} \right).$

18. (1)  $A = \begin{pmatrix} 1 - p & q \\ p & 1 - q \end{pmatrix}$ ;

(2) $\begin{pmatrix}x_{n}\\y_{n}\end{pmatrix}=A^{n}\begin{pmatrix}x_{0}\\y_{0}\end{pmatrix}=\frac{1}{2(p+q)}\begin{pmatrix}2q+(p-q)r^{n}\\2p+(q-p)r^{n}\end{pmatrix}$ ，其中r=1-p-q.

19. (1) $P = \frac{1}{3} \begin{pmatrix} 1 & 2 & 2 \\ 2 & 1 & -2 \\ 2 & -2 & 1 \end{pmatrix}, P^{-1} A P = \begin{pmatrix} -2 &  &  \\  & 1 &  \\  &  & 4 \end{pmatrix}$;

(2) $P = \begin{pmatrix} \frac{1}{3} & 0 & \frac{4}{3\sqrt{2}} \\ \frac{2}{3} & \frac{1}{\sqrt{2}} & -\frac{1}{3\sqrt{2}} \\ -\frac{2}{3} & \frac{1}{\sqrt{2}} & \frac{1}{3\sqrt{2}} \end{pmatrix}, P^{-1}AP = \begin{pmatrix} 10 &  &  \\  & 1 &  \\  &  & 1 \end{pmatrix}.$

20. $x = 4, y = 5, \boldsymbol{P} = \begin{pmatrix} \frac{1}{\sqrt{2}} & \frac{2}{3} & \frac{1}{3\sqrt{2}} \\ 0 & \frac{1}{3} & -\frac{4}{3\sqrt{2}} \\ -\frac{1}{\sqrt{2}} & \frac{2}{3} & \frac{1}{3\sqrt{2}} \end{pmatrix}$.

21.  $A=\begin{pmatrix}-2&3&-3\\-4&5&-3\\-4&4&-2\end{pmatrix}.$

22.  $A=\frac{1}{3}\begin{pmatrix}-1&0&2\\0&1&2\\2&2&0\end{pmatrix}.$

23.  $A = \begin{pmatrix} 4 & 1 & 1 \\ 1 & 4 & 1 \\ 1 & 1 & 4 \end{pmatrix}.$

168

---

部分习题参考答案

24. (2)  $\lambda_{1}=\sum_{i=1}^{n}a_{i}^{2},\lambda_{2}=\lambda_{3}=\cdots=\lambda_{n}=0,(p_{1},p_{2},\cdots,p_{n})=\begin{pmatrix}a_{1}&-a_{2}&\cdots&-a_{n}\\a_{2}&a_{1}&\cdots&a_{n-1}\\ \vdots&\vdots&&\vdots\\a_{n}&a_{n-1}&\cdots&a_{1}\end{pmatrix}.$

26. (1) $-2\left( \begin{array}{cc}1 & 1\\ 1 & 1 \end{array} \right);$ (2) $2\left( \begin{array}{ccc}1 & 1 & -2\\ 1 & 1 & -2\\ -2 & -2 & 4 \end{array} \right).$

27. (1) $f = (x, y, z) \begin{pmatrix} 1 & 2 & 1 \\ 2 & 4 & 2 \\ 1 & 2 & 1 \end{pmatrix} \begin{pmatrix} x \\ y \\ z \end{pmatrix}$;

(2) $f=(x,y,z)\begin{pmatrix}1&-1&-2\\-1&1&-2\\-2&-2&-7\end{pmatrix}\begin{pmatrix}x\\y\\z\end{pmatrix};$

(3) $f = (x_{1}, x_{2}, x_{3}) \begin{pmatrix} 1 & -1 & 0 \\ -1 & 1 & 3 \\ 0 & 3 & 1 \end{pmatrix} \begin{pmatrix} x_{1} \\ x_{2} \\ x_{3} \end{pmatrix}$.

28. (1) $\begin{pmatrix}2&2\\ 2&1\end{pmatrix};$  (2) $\begin{pmatrix}1&3&5\\ 3&5&7\\ 5&7&9\end{pmatrix}.$

29. (1) $\begin{pmatrix} x_1 \\ x_2 \\ x_3 \end{pmatrix} = \begin{pmatrix} 1 & 0 & 0 \\ 0 & \frac{1}{\sqrt{2}} & \frac{1}{\sqrt{2}} \\ 0 & \frac{1}{\sqrt{2}} & -\frac{1}{\sqrt{2}} \end{pmatrix} \begin{pmatrix} y_1 \\ y_2 \\ y_3 \end{pmatrix}, f = 2y_1^2 + 5y_2^2 + y_3^2;$

(2) $\begin{pmatrix}x_{1}\\x_{2}\\x_{3}\end{pmatrix}=\begin{pmatrix}\frac{1}{\sqrt{3}}&\frac{1}{\sqrt{2}}&-\frac{1}{\sqrt{6}}\\ \frac{1}{\sqrt{3}}&0&\frac{2}{\sqrt{6}}\\ -\frac{1}{\sqrt{3}}&\frac{1}{\sqrt{2}}&\frac{1}{\sqrt{6}}\end{pmatrix}\begin{pmatrix}y_{1}\\y_{2}\\y_{3}\end{pmatrix},f=2y_{1}^{2}+y_{2}^{2}-y_{3}^{2}.$

169

---

部分习题参考答案

30. $\begin{pmatrix} x \\ y \\ z \end{pmatrix} = \begin{pmatrix} 0 & \frac{4}{3\sqrt{2}} & \frac{1}{3} \\ \frac{1}{\sqrt{2}} & -\frac{1}{3\sqrt{2}} & \frac{2}{3} \\ \frac{1}{\sqrt{2}} & \frac{1}{3\sqrt{2}} & -\frac{2}{3} \end{pmatrix} \begin{pmatrix} u \\ v \\ w \end{pmatrix}, 2v^2 + 11w^2 = 1.$

32. (1) $f(Cy) = y_1^2 + y_2^2 - y_3^2, C = \begin{pmatrix} 1 & -\frac{1}{\sqrt{2}} & 3 \\ 0 & \frac{1}{\sqrt{2}} & -1 \\ 0 & 0 & 1 \end{pmatrix} \left( |C| = \frac{1}{\sqrt{2}} \right)$;

(2) $f(Cy) = y_1^2 - y_2^2 + y_3^2, C = \begin{pmatrix} 1 & 1 & -1 \\ 0 & 1 & 0 \\ 0 & -1 & 1 \end{pmatrix} (|C| = 1)$;

(3) $f(\boldsymbol{C}\boldsymbol{y}) = y_1^2 + y_2^2 + y_3^2, \boldsymbol{C} = \frac{1}{\sqrt{2}} \begin{pmatrix} 1 & -1 & -1 \\ 0 & 2 & 2 \\ 0 & 0 & 1 \end{pmatrix} (|\boldsymbol{C}| = \sqrt{2}).$

33.  $-\frac{4}{5}<a<0.$

34.（1）负定；（2）正定.

## 习题六

1. 各个线性空间的基可取为

(1)  $\alpha_{1}=\begin{pmatrix}1&0\\0&0\end{pmatrix},\alpha_{2}=\begin{pmatrix}0&1\\0&0\end{pmatrix},\alpha_{3}=\begin{pmatrix}0&0\\1&0\end{pmatrix},\alpha_{4}=\begin{pmatrix}0&0\\0&1\end{pmatrix};$
(2)  $\alpha_{1}=\begin{pmatrix}1&0\\0&-1\end{pmatrix},\alpha_{2}=\begin{pmatrix}0&1\\0&0\end{pmatrix},\alpha_{3}=\begin{pmatrix}0&0\\1&0\end{pmatrix};$
(3)  $\alpha_{1}=\begin{pmatrix}1&0\\0&0\end{pmatrix},\alpha_{2}=\begin{pmatrix}0&0\\0&1\end{pmatrix},\alpha_{3}=\begin{pmatrix}0&1\\1&0\end{pmatrix}.$

3.（1）不是；（2）是

4. $(1,-2,6)^{\mathrm{T}}$

5. 设 $\alpha$ 在 $\alpha_{1}, \alpha_{2}, \alpha_{3}$ 下的坐标是 $(x_{1}, x_{2}, x_{3})^{\mathrm{T}}$, 在 $\beta_{1}, \beta_{2}, \beta_{3}$ 下的坐标是 $(x_{1}', x_{2}', x_{3}')^{\mathrm{T}}$, 有

170

---

部分习题参考答案

$$
\left( \begin{array}{c} x _ {1} ^ {\prime} \\ x _ {2} ^ {\prime} \\ x _ {3} ^ {\prime} \end{array} \right) = \left( \begin{array}{c c c} 1 3 & 1 9 & 4 3 \\ - 9 & - 1 3 & - 3 0 \\ 7 & 1 0 & 2 4 \end{array} \right) \left( \begin{array}{c} x _ {1} \\ x _ {2} \\ x _ {3} \end{array} \right), \quad \text {或} \quad \left( \begin{array}{c} x _ {1} \\ x _ {2} \\ x _ {3} \end{array} \right) = \left( \begin{array}{c c c} - 1 2 & - 2 6 & - 1 1 \\ 6 & 1 1 & 3 \\ 1 & 3 & 2 \end{array} \right) \left( \begin{array}{c} x _ {1} ^ {\prime} \\ x _ {2} ^ {\prime} \\ x _ {3} ^ {\prime} \end{array} \right).
$$

$$
6. (1) \boldsymbol {P} = \left( \begin{array}{r r r r} 2 & 0 & 5 & 6 \\ 1 & 3 & 3 & 6 \\ - 1 & 1 & 2 & 1 \\ 1 & 0 & 1 & 3 \end{array} \right); \quad (2) \left( \begin{array}{c} x _ {1} ^ {\prime} \\ x _ {2} ^ {\prime} \\ x _ {3} ^ {\prime} \\ x _ {4} ^ {\prime} \end{array} \right) = \frac {1}{2 7} \left( \begin{array}{c c c c} 1 2 & 9 & - 2 7 & - 3 3 \\ 1 & 1 2 & - 9 & - 2 3 \\ 9 & 0 & 0 & - 1 8 \\ - 7 & - 3 & 9 & 2 6 \end{array} \right) \left( \begin{array}{c} x _ {1} \\ x _ {2} \\ x _ {3} \\ x _ {4} \end{array} \right);
$$

(3)  $k(1,1,1,-1)^{\mathrm{T}}$  ( $k \in R$ ).

7.（1）能，不能；（2）维数为3，基可选为 $a_{1},a_{2},b_{2}$

8.（1）关于 y 轴对称；（2）投影到 y 轴；（3）关于直线 y=x 对称；公众号:旗胜考研
（4）顺时针方向旋转  $90^{\circ}$ .

10. $\begin{pmatrix}1&0&0\\2&1&0\\0&1&1\end{pmatrix}.$

11. $\begin{pmatrix}1&0&0\\1&1&0\\1&2&1\end{pmatrix}.$

12. (2) $\begin{pmatrix}1&0&\frac{1}{2}\\0&1&-\frac{1}{2}\\0&0&\frac{1}{2}\end{pmatrix};$  (3) 2.

171

---

## 2000 年中国高校科学技术奖二等奖

## 第八届全国高校出版社优秀畅销书一等奖

高等数学 第七版 上册
高等数学 第七版 下册
高等数学附册 学习辅导与习题选解 同济·第七版
高等数学习题全解指南 上册 同济·第七版
高等数学习题全解指南 下册 同济·第七版
工程数学——线性代数 第七版
线性代数附册 学习辅导与习题全解 同济·第七版
工程数学——概率统计简明教程 第三版
▷ 概率统计简明教程附册 学习辅导与习题全解 同济·第三版
工程数学——新编统计学教程

定价 26.80 元
