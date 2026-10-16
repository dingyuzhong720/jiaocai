# 第3章 矩阵的初等变换与线性方程组

原始 PDF 第 60–85 页。

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

![](../../raw/pages_0033-0064/images/page_61_image_1.jpg)

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

![](../../raw/pages_0065-0096/images/page_72_image_20.jpg)

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

![](../../raw/pages_0065-0096/images/page_84_image_2.jpg)

考研电子书网站:www.pdf2book.com

81
