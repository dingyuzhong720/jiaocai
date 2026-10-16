# 第5章 相似矩阵及二次型

原始 PDF 第 118–145 页。

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

![](../../raw/pages_0097-0128/images/page_118_image_29.jpg)

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

![](../../raw/pages_0097-0128/images/page_121_image_9.jpg)

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

![](../../raw/pages_0097-0128/images/page_123_image_20.jpg)

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

![](../../raw/pages_0129-0160/images/page_133_image_17.jpg)

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
