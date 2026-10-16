# 第15章 傅里叶级数

原始 PDF 第 68–89 页。

第十五章傅里叶级数

## § 1 傅里叶级数

本章讨论在数学与工程技术中都有着广泛应用的一类函数项级数,即由三角函数列所产生的三角级数.

## 一、三角级数·正交函数系

在科学实验与工程技术的某些现象中,常会碰到一种周期运动.最简单的周期运动,可用正弦函数

$$
y = A \sin (\omega x + \varphi) \tag {1}
$$

来描写. 由(1)所表达的周期运动也称为简谐振动, 其中 A 为振幅,  $\varphi$  为初相角,  $\omega$  为角频率, 于是简谐振动 y 的周期是  $T = \frac{2\pi}{\omega}$ . 较为复杂的周期运动, 则常是几个简谐振动

$$
y _ {k} = A _ {k} \sin (k \omega x + \varphi_ {k}), \quad k = 1, 2, \dots , n
$$

的叠加

$$
y = \sum_ {k = 1} ^ {n} y _ {k} = \sum_ {k = 1} ^ {n} A _ {k} \sin (k \omega x + \varphi_ {k}). \tag {2}
$$

由于简谐振动  $y_{k}$  的周期为  $\frac{T}{k}\left(T=\frac{2\pi}{\omega}\right), k=1,2,\cdots,n$ ，所以函数(2)的周期为 T。对无穷多个简谐振动进行叠加就得到函数项级数

$$
A _ {0} + \sum_ {n = 1} ^ {\infty} A _ {n} \sin (n \omega x + \varphi_ {n}). \tag {3}
$$

若级数(3)收敛,则它所描述的是更为一般的周期运动现象.对于级数(3),我们只要讨论  $\omega=1$  (如果  $\omega\neq1$ , 可用  $\omega x$  代换 x) 的情形.由于

$$
\sin (n x + \varphi_ {n}) = \sin \varphi_ {n} \cos n x + \cos \varphi_ {n} \sin n x,
$$

所以

$$
\begin{array}{l} A _ {0} + \sum_ {n = 1} ^ {\infty} A _ {n} \sin (n x + \varphi_ {n}) \\ = A _ {0} + \sum_ {n = 1} ^ {\infty} (A _ {n} \sin \varphi_ {n} \cos n x + A _ {n} \cos \varphi_ {n} \sin n x). \tag {$3^{\prime$}} \\ \end{array}
$$

60

---

§ 1 傅里叶级数

记 $A_{0} = \frac{a_{0}}{2},\quad A_{n}\sin \varphi_{n} = a_{n},\quad A_{n}\cos \varphi_{n} = b_{n},\quad n = 1,2,\dots ,$

则级数 $(3^{\prime})$ 可写成

$$
\frac {a _ {0}}{2} + \sum_ {n = 1} ^ {\infty} (a _ {n} \cos n x + b _ {n} \sin n x). \tag {4}
$$

它是由三角函数列(也称为三角函数系)

$$
1, \cos x, \sin x, \cos 2 x, \sin 2 x, \dots , \cos n x, \sin n x, \dots \tag {5}
$$

所产生的一般形式的三角级数.

容易验证,若三角级数(4)收敛,则它的和一定是一个以 $2\pi$ 为周期的函数.

关于三角级数(4)的收敛性有如下定理.

定理15.1 若级数

$$
\frac {\mid a _ {0} \mid}{2} + \sum_ {n = 1} ^ {\infty} (\mid a _ {n} \mid + \mid b _ {n} \mid)
$$

收敛,则级数(4)在整个数轴上绝对收敛且一致收敛.

证 对任何实数 $x$ ，由于

$$
\mid a _ {n} \cos n x + b _ {n} \sin n x \mid \leqslant \mid a _ {n} \mid + \mid b _ {n} \mid ,
$$

应用魏尔斯特拉斯 $M$ 判别法(定理13.5)就能推得本定理的结论.

![](../../raw/pages_0065-0096/images/page_68_image_15.jpg)

为进一步研究三角级数(4)的收敛性,我们先探讨三角函数系(5)具有哪些特性.

首先容易看出,三角函数系(5)中所有函数具有共同的周期 $2\pi$ .

其次,在三角函数系(5)中,任何两个不相同的函数的乘积在 $[-π,π]$ 上的积分都等于零,即

$$
\int_ {- \pi} ^ {\pi} \cos n x \mathrm{d} x = \int_ {- \pi} ^ {\pi} \sin n x \mathrm{d} x = 0, \tag {6}
$$

$$
\left. \begin{array}{l} \int_ {- \pi} ^ {\pi} \cos m x \cos n x \mathrm{d} x = 0 \quad (m \neq n), \\ \int_ {- \pi} ^ {\pi} \sin m x \sin n x \mathrm{d} x = 0 \quad (m \neq n), \\ \int_ {- \pi} ^ {\pi} \cos m x \sin n x \mathrm{d} x = 0. \end{array} \right\} \tag {7}
$$

而(5)中任何一个函数的平方在 $[-π,π]$ 上的积分都不等于零,即

$$
\left. \begin{array}{l} \int_ {- \pi} ^ {\pi} \cos^ {2} n x \mathrm{d} x = \int_ {- \pi} ^ {\pi} \sin^ {2} n x \mathrm{d} x = \pi , \\ \int_ {- \pi} ^ {\pi} 1 ^ {2} \mathrm{d} x = 2 \pi . \end{array} \right\} \tag {8}
$$

若两个函数 $\varphi$ 与 $\psi$ 在 $[a,b]$ 上可积，且

$$
\int_ {a} ^ {b} \varphi (x) \psi (x) \mathrm{d} x = 0,
$$

则称函数 $\varphi$ 与 $\psi$ 在 $[a, b]$ 上是正交的. 由此, 三角函数系(5)在 $[- \pi, \pi]$ 上具有正交性, 或称(5)是正交函数系.

## 二、以 $2\pi$ 为周期的函数的傅里叶级数

应用三角函数系(5)的正交性,我们讨论三角级数(4)的和函数f与级数(4)的系

61

---

第十五章 傅里叶级数

数  $a_{0}, a_{n}, b_{n}$  之间的关系.

定理15.2 若在整个数轴上

$$
f (x) = \frac {a _ {0}}{2} + \sum_ {n = 1} ^ {\infty} (a _ {n} \cos n x + b _ {n} \sin n x) \tag {9}
$$

且等式右边级数一致收敛,则有如下关系式:

$$
a _ {n} = \frac {1}{\pi} \int_ {- \pi} ^ {\pi} f (x) \cos n x \mathrm{d} x, \quad n = 0, 1, 2, \dots , \tag {10}
$$

$$
b _ {n} = \frac {1}{\pi} \int_ {- \pi} ^ {\pi} f (x) \sin n x \mathrm{d} x, \quad n = 1, 2, \dots .
$$

证 由定理条件,函数f在 $[-π,π]$ 上连续且可积.对(9)式逐项积分得

$$
\begin{array}{l} \int_ {- \pi} ^ {\pi} f (x) \mathrm{d} x \\ = \frac {a _ {0}}{2} \int_ {- \pi} ^ {\pi} \mathrm{d} x + \sum_ {n = 1} ^ {\infty} \left(a _ {n} \int_ {- \pi} ^ {\pi} \cos n x \mathrm{d} x + b _ {n} \int_ {- \pi} ^ {\pi} \sin n x \mathrm{d} x\right). \\ \end{array}
$$

由关系式(6)知,上式右边括号内的积分都等于零.所以

$$
\int_ {- \pi} ^ {\pi} f (x) \mathrm{d} x = \frac {a _ {0}}{2} \cdot 2 \pi = a _ {0} \pi ,
$$

即得

$$
a _ {0} = \frac {1}{\pi} \int_ {- \pi} ^ {\pi} f (x) \mathrm{d} x,
$$

现以 $\cos kx$ 乘(9)式两边（ $k$ 为正整数），得

$$
f (x) \cos k x = \frac {a _ {0}}{2} \cos k x + \sum_ {n = 1} ^ {\infty} (a _ {n} \cos n x \cos k x + b _ {n} \sin n x \cos k x). \tag {11}
$$

从第十三章 §1 习题4知道,由级数(9)一致收敛,可推出级数(11)也一致收敛.于是对级数(11)逐项求积,有

$$
\begin{array}{l} \int_ {- \pi} ^ {\pi} f (x) \cos k x \mathrm{d} x \\ = \frac {a _ {0}}{2} \int_ {- \pi} ^ {\pi} \cos k x \mathrm{d} x + \sum_ {n = 1} ^ {\infty} \left(a _ {n} \int_ {- \pi} ^ {\pi} \cos n x \cos k x \mathrm{d} x + b _ {n} \int_ {- \pi} ^ {\pi} \sin n x \cos k x \mathrm{d} x\right). \\ \end{array}
$$

由三角函数的正交性,右边除了以  $a_{k}$  为系数的那一项积分

$$
\int_ {- \pi} ^ {\pi} \cos^ {2} k x \mathrm{d} x = \pi
$$

外,其他各项积分都等于0,于是得出

$$
\int_ {- \pi} ^ {\pi} f (x) \cos k x \mathrm{d} x = a _ {k} \pi (k = 1, 2, \dots),
$$

即

$$
a _ {k} = \frac {1}{\pi} \int_ {- \pi} ^ {\pi} f (x) \cos k x \mathrm{d} x (k = 1, 2, \dots).
$$

同理,(9)式两边乘以  $\sin kx$ , 并逐项求积, 可得

$$
b _ {k} = \frac {1}{\pi} \int_ {- \pi} ^ {\pi} f (x) \sin k x \mathrm{d} x (k = 1, 2, \dots).
$$

62

---

§ 1 傅里叶级数

一般地说, 若 f 是以  $2\pi$  为周期且在  $[-\pi, \pi]$  上可积的函数, 则按公式(10)计算出的  $a_{n}$  和  $b_{n}$  称为函数 f (关于三角函数系) 的傅里叶系数, 以 f 的傅里叶系数为系数的三角级数(9)称为 f (关于三角函数系) 的傅里叶级数, 记作

$$
f (x) \sim \frac {a _ {0}}{2} + \sum_ {n = 1} ^ {\infty} (a _ {n} \cos n x + b _ {n} \sin n x). \tag {12}
$$

这里记号“\~”表示上式右边是左边函数的傅里叶级数. 由定理15.2知道: 若(9)式右边的三角级数在整个数轴上一致收敛于其和函数f, 则此三角级数就是f的傅里叶级数, 即此时(12)式中的记号“\~”可换为等号. 然而, 若从以 $2\pi$ 为周期且在 $[-\pi,\pi]$ 上可积的函数f出发, 按公式(10)求出其傅里叶系数并得到傅里叶级数(12), 这时还需讨论此级数是否收敛, 以及如果收敛, 是否收敛于f本身. 这就是下一段所要叙述的内容.

## 三、收敛定理

下面的定理称为傅里叶级数收敛定理.

定理15.3 若以 $2\pi$ 为周期的函数 $f$ 在 $[- \pi, \pi]$ 上按段光滑，则在每一点 $x \in [-\pi, \pi]$，$f$ 的傅里叶级数（12）收敛于 $f$ 在点 $x$ 的左、右极限的算术平均值，即

$$
\frac {f (x + 0) + f (x - 0)}{2} = \frac {a _ {0}}{2} + \sum_ {n = 1} ^ {\infty} (a _ {n} \cos n x + b _ {n} \sin n x),
$$

其中 $a_{n}, b_{n}$ 为 $f$ 的傅里叶系数.

下面先对定理中的某些概念作解释,然后举例说明如何运用这个定理把函数展开成傅里叶级数.关于收敛定理的证明将在§3中进行.

我们知道,若f的导函数在 $[a,b]$ 上连续,则称f在 $[a,b]$ 上光滑.但若定义在 $[a,b]$ 上除了至多有有限个第一类间断点的函数f的导函数在 $[a,b]$ 上除了至多有限个点外都存在且连续,在这有限个点上导函数 $f'$ 的左、右极限存在,则称f在 $[a,b]$ 上按段光滑.

根据上述定义,若函数f在 $[a,b]$ 上按段光滑,则有如下重要性质:

$1^{\circ}f$ 在 $[a,b]$ 上可积.

$2^{\circ}$ 在 $[a,b]$ 上每一点都存在 $f(x\pm 0)$，且有

$$
\lim _ {t \to 0 ^ {+}} \frac {f (x + t) - f (x + 0)}{t} = f ^ {\prime} (x + 0), \tag {13}
$$

$$
\lim _ {t \to 0 ^ {+}} \frac {f (x - t) - f (x - 0)}{- t} = f ^ {\prime} (x - 0).
$$

$3^{\circ}$ 补充定义 $f'$ 在 $[a,b]$ 上那些至多有限个不存在点上的值后（仍记为 $f'$），$f'$ 在 $[a,b]$ 上可积.

从几何图形上讲,在区间 $[a,b]$ 上按段光滑函数,是由有限个光滑弧段所组成,它至多有有限个第一类间断点与角点(图15-1).

收敛定理指出，$f$ 的傅里叶级数在点 $x$ 处收敛于这一点上 $f$ 的左、右极限的算术平均值 $\frac{f(x + 0) + f(x - 0)}{2}$; 而当 $f$ 在点 $x$ 连续时，则有 $\frac{f(x + 0) + f(x - 0)}{2} = f(x)$，即此时 $f$ 的傅里叶级数收敛于 $f(x)$. 于是有下面推论.

63

---

第十五章 傅里叶级数

推论 若 $f$ 是以 $2\pi$ 为周期的连续函数, 且在 $[- \pi, \pi]$ 上按段光滑, 则 $f$ 的傅里叶级数在 $(- \infty, + \infty)$ 上收敛于 $f$.

根据收敛定理的假设, $f$ 是以 $2\pi$ 为周期的函数,所以系数公式(10)中的积分区间 $[-π,π]$ 可以改为长度为 $2π$ 的任何区间,而不影响 $a_{n},b_{n}$ 的值:

![](../../raw/pages_0065-0096/images/page_71_chart_3.jpg)

<details>
<summary>line</summary>

| X | Y |
| --- | --- |
| a | ~0.2 |
| x1 | ~0.6 |
| x2 | ~0.3 |
| x2 (open circle) | ~0.7 |
| x3 | ~0.9 |
| x3 (filled circle) | ~0.5 |
| x4 | ~0.3 |
| b | ~0.8 |
</details>

图15-1

$$
a _ {n} = \frac {1}{\pi} \int_ {c} ^ {c + 2 \pi} f (x) \cos n x \mathrm{d} x, n = 0, 1, 2, \dots ,
$$

$$
b _ {n} = \frac {1}{\pi} \int_ {c} ^ {c + 2 \pi} f (x) \sin n x \mathrm{d} x, n = 1, 2, \dots , \tag {$10^{\prime$}}
$$

其中 c 为任何实数.

注意:在具体讨论函数的傅里叶级数展开式时，常只给出函数 $f$ 在 $(- \pi, \pi]$ （或 $[- \pi, \pi)$ ）上的解析表达式，但读者应理解为它是定义在整个数轴上以 $2\pi$ 为周期的函数。即在 $(- \pi, \pi]$ 以外的部分按函数在 $(- \pi, \pi]$ 上的对应关系作周期延拓。如 $f$ 为 $(- \pi, \pi]$ 上的解析表达式，那么周期延拓后的函数为

$$
\hat {f} (x) = \left\{ \begin{array}{l} f (x), x \in (- \pi , \pi ], \\ f (x - 2 k \pi), x \in ((2 k - 1) \pi , (2 k + 1) \pi ], \quad k = \pm 1, \pm 2, \dots , \end{array} \right.
$$

如图 15-2 所示. 因此我们说函数 f 的傅里叶级数就是指函数  $\hat{f}$  的傅里叶级数.

![](../../raw/pages_0065-0096/images/page_71_chart_11.jpg)

<details>
<summary>line</summary>

| X | Y |
| --- | --- |
| \(-3\pi\) | ~0.2 |
| \(-\pi\) | ~0.2 |
| \(\pi\) | ~0.2 |
| \(3\pi\) | ~0.2 |
| \(5\pi\) | ~0.2 |
</details>

图15-2 实线与虚线的全体表示 $y = \hat{f}(x)$

例1 设

$$
f (x) = \left\{ \begin{array}{l l} x, & 0 \leqslant x \leqslant \pi , \\ 0, & - \pi <   x <   0, \end{array} \right.
$$

求 f 的傅里叶级数展开式.

解 函数 f 及其周期延拓后的图像如图 15-3 所示. 显然 f 是按段光滑的, 故由定理 15.3 (收敛定理), 它可以展开成傅里叶级数. 由于

![](../../raw/pages_0065-0096/images/page_71_chart_17.jpg)

<details>
<summary>line</summary>

| X | Y |
| --- | --- |
| \(-3\pi\) | 0 |
| \(-2\pi\) | 0 |
| \(-\pi\) | \(0, \pi\) |
| \(\pi\) | 0 |
| \(2\pi\) | 0 |
| \(3\pi\) | \(0, \pi\) |
| \(4\pi\) | \(0, \pi\) |
</details>

图15-3

64

---

§ 1 傅里叶级数

$$
a _ {0} = \frac {1}{\pi} \int_ {- \pi} ^ {\pi} f (x) \mathrm{d} x = \frac {1}{\pi} \int_ {0} ^ {\pi} x \mathrm{d} x = \frac {\pi}{2}.
$$

当 $n \geqslant 1$ 时，

$$
\begin{array}{l} a _ {n} = \frac {1}{\pi} \int_ {- \pi} ^ {\pi} f (x) \cos n x \mathrm{d} x = \frac {1}{\pi} \int_ {0} ^ {\pi} x \cos n x \mathrm{d} x \\ = \frac {1}{n \pi} x \sin n x \Bigg | _ {0} ^ {\pi} - \frac {1}{n \pi} \int_ {0} ^ {\pi} \sin n x \mathrm{d} x = \frac {1}{n ^ {2} \pi} \cos n x \Bigg | _ {0} ^ {\pi} \\ = \frac {1}{n ^ {2} \pi} (\cos n \pi - 1) = \left\{ \begin{array}{l l} - \frac {2}{n ^ {2} \pi}, & \text {当} n \text {为奇数时,} \\ 0, & \text {当} n \text {为偶数时,} \end{array} \right. \\ \end{array}
$$

$$
\begin{array}{l} b _ {n} = \frac {1}{\pi} \int_ {- \pi} ^ {\pi} f (x) \sin n x \mathrm{d} x = \frac {1}{\pi} \int_ {0} ^ {\pi} x \sin n x \mathrm{d} x \\ = - \frac {1}{n \pi} x \cos n x \Bigg | _ {0} ^ {\pi} + \frac {1}{n \pi} \int_ {0} ^ {\pi} \cos n x \mathrm{d} x \\ = \frac {(- 1) ^ {n + 1}}{n} + \frac {1}{n ^ {2} \pi} \sin n x \Bigg | _ {0} ^ {\pi} \\ = \frac {(- 1) ^ {n + 1}}{n}. \\ \end{array}
$$

所以在开区间 $(-π, π)$ 上，

$$
f (x) = \frac {\pi}{4} - \left(\frac {2}{\pi} \cos x - \sin x\right) - \frac {1}{2} \sin 2 x - \left(\frac {2}{9 \pi} \cos 3 x - \frac {1}{3} \sin 3 x\right) - \dots .
$$

在  $x=\pm\pi$  时, 上式右边收敛于

$$
\frac {f (\pi - 0) + f (- \pi + 0)}{2} = \frac {\pi + 0}{2} = \frac {\pi}{2}.
$$

于是，在 $[-π,π]$ 上f的傅里叶级数的图像如图15-4所示(注意它与图15-3的差别).

![](../../raw/pages_0065-0096/images/page_72_chart_10.jpg)

<details>
<summary>scatter</summary>

| X | Y (Series 1) | Y (Series 2) |
| --- | --- | --- |
| \(-3\pi\) | 0 | ~\(0.5\pi\) |
| \(-2\pi\) | 0 | — |
| \(-\pi\) | 0 | ~\(0.5\pi\) |
| \(0\) | 0 | — |
| \(\pi\) | 0 | ~\(0.5\pi\) |
| \(2\pi\) | 0 | — |
| \(3\pi\) | 0 | ~\(0.5\pi\) |
| \(4\pi\) | 0 | — |
| \(5\pi\) | 0 | ~\(0.5\pi\) |
</details>

图15-4

例 2 把下列函数展开成傅里叶级数:

$$
f (x) = \left\{ \begin{array}{l l} x ^ {2}, & 0 <   x <   \pi , \\ 0, & x = \pi , \\ - x ^ {2}, & \pi <   x \leqslant 2 \pi . \end{array} \right.
$$

解 $f$ 及其周期延拓的图形如图15-5所示. 显然 $f$ 是按段光滑的, 因此可以展开成傅里叶级数.

在 $(10')$ 式中令c=0来计算傅里叶系数如下:

65

---

第十五章 傅里叶级数

![](../../raw/pages_0065-0096/images/page_73_image_1.jpg)

<details>
<summary>text_image</summary>

-3π -2π -π
O π 2π 3π
x
y
</details>

图15-5

$$
a _ {0} = \frac {1}{\pi} \int_ {0} ^ {2 \pi} f (x) \mathrm{d} x = \frac {1}{\pi} \int_ {0} ^ {\pi} x ^ {2} \mathrm{d} x + \frac {1}{\pi} \int_ {\pi} ^ {2 \pi} (- x ^ {2}) \mathrm{d} x = \frac {\pi^ {2}}{3} - \frac {7 \pi^ {2}}{3} = - 2 \pi^ {2},
$$

$$
\begin{array}{l} a _ {n} = \frac {1}{\pi} \int_ {0} ^ {2 \pi} f (x) \cos n x \mathrm{d} x = \frac {1}{\pi} \int_ {0} ^ {\pi} x ^ {2} \cos n x \mathrm{d} x + \frac {1}{\pi} \int_ {\pi} ^ {2 \pi} (- x ^ {2}) \cos n x \mathrm{d} x \\ = \frac {1}{\pi} \left[ \left(\frac {x ^ {2}}{n} - \frac {2}{n ^ {3}}\right) \sin n x + \frac {2 x}{n ^ {2}} \cos n x \right] \Bigg | _ {0} ^ {\pi} - \frac {1}{\pi} \left[ \left(\frac {x ^ {2}}{n} - \frac {2}{n ^ {3}}\right) \sin n x + \frac {2 x}{n ^ {2}} \cos n x \right] \Bigg | _ {\pi} ^ {2 \pi} \\ = \frac {4}{n ^ {2}} \left[ (- 1) ^ {n} - 1 \right], \\ \end{array}
$$

$$
\begin{array}{l} b _ {n} = \frac {1}{\pi} \int_ {0} ^ {2 \pi} f (x) \sin n x \mathrm{d} x = \frac {1}{\pi} \int_ {0} ^ {\pi} x ^ {2} \sin n x \mathrm{d} x + \frac {1}{\pi} \int_ {\pi} ^ {2 \pi} (- x ^ {2}) \sin n x \mathrm{d} x \\ = \frac {1}{\pi} \left[ \left(- \frac {x ^ {2}}{n} + \frac {2}{n ^ {3}}\right) \cos n x + \frac {2 x}{n ^ {2}} \sin n x \right] \Bigg | _ {0} ^ {\pi} - \frac {1}{\pi} \left[ \left(- \frac {x ^ {2}}{n} + \frac {2}{n ^ {3}}\right) \cos n x + \frac {2 x}{n ^ {2}} \sin n x \right] \Bigg | _ {\pi} ^ {2 \pi} \\ = \frac {2}{\pi} \left\{\frac {\pi^ {2}}{n} + \left(\frac {\pi^ {2}}{n} - \frac {2}{n ^ {3}}\right) [ 1 - (- 1) ^ {n} ] \right\}. \\ \end{array}
$$

所以当  $x \in (0, \pi) \cup (\pi, 2\pi)$  时，

$$
\begin{array}{l} f (x) = - \pi^ {2} + \sum_ {n = 1} ^ {\infty} \left\{\frac {4}{n ^ {2}} [ (- 1) ^ {n} - 1 ] \cos n x + \frac {2}{\pi} \left[ \frac {\pi^ {2}}{n} + \left(\frac {\pi^ {2}}{n} - \frac {2}{n ^ {3}}\right) (1 - (- 1) ^ {n}) \right] \sin n x \right\} \\ = - \pi^ {2} - 8 \left(\cos x + \frac {1}{3 ^ {2}} \cos 3 x + \frac {1}{5 ^ {2}} \cos 5 x + \dots\right) + \frac {2}{\pi} \left\{\left(3 \pi^ {2} - 4\right) \sin x + \right. \\ \frac {\pi^ {2}}{2} \sin 2 x + \left(\frac {3 \pi^ {2}}{3} - \frac {4}{3 ^ {3}}\right) \sin 3 x + \frac {\pi^ {2}}{4} \sin 4 x + \dots \Bigg \}. \\ \end{array}
$$

当 $x = \pi$ 时，由于

$$
\frac {f (\pi - 0) + f (\pi + 0)}{2} = 0,
$$

所以

$$
0 = - \pi^ {2} + 8 \left(\frac {1}{1 ^ {2}} + \frac {1}{3 ^ {2}} + \frac {1}{5 ^ {2}} + \dots\right). \tag {14}
$$

66

---

§ 1 傅里叶级数

当 x=0 或  $2\pi$  时, 由于

$$
\frac {1}{2} (f (0 - 0) + f (0 + 0)) = \frac {1}{2} (- 4 \pi^ {2} + 0) = - 2 \pi^ {2},
$$

因此

$$
- 2 \pi^ {2} = - \pi^ {2} - 8 \left(\frac {1}{1 ^ {2}} + \frac {1}{3 ^ {2}} + \frac {1}{5 ^ {2}} + \dots\right). \tag {15}
$$

由(14)式或(15)式都可得出

$$
\frac {\pi^ {2}}{8} = \frac {1}{1 ^ {2}} + \frac {1}{3 ^ {2}} + \frac {1}{5 ^ {2}} + \dots .
$$

例 3 在电子技术中经常用到矩形波,用傅里叶级数展开后,就可以将矩形波看成

一系列不同频率的简谐振动的叠加，在电工学中称为谐波分析。设 $f(x)$ 是周期为 $2\pi$ 的矩形波函数（图15-6），在 $[- \pi, \pi)$ 上的表达式为

$$
f (x) = \left\{ \begin{array}{c l} - \frac {\pi}{4}, & - \pi \leqslant x <   0, \\ 0, & x = 0, \\ \frac {\pi}{4}, & 0 <   x <   \pi . \end{array} \right.
$$

求该矩形波函数的傅里叶展开式.

![](../../raw/pages_0065-0096/images/page_74_chart_11.jpg)

<details>
<summary>line</summary>

| X | Y |
| --- | --- |
| 0 | \(\pi/4\) |
| \(\pm\pi\) | \(-\pi/4\) |
| 0 | 0 |
| \(\pm\pi\) | \(\pi/4\) |
</details>

图15-6

解 由于 $f(x)$ 在 $(- \pi, \pi)$ 上是奇函数，所以

$$
a _ {0} = \frac {1}{\pi} \int_ {- \pi} ^ {\pi} f (x) \mathrm{d} x = 0,
$$

$$
a _ {n} = \frac {1}{\pi} \int_ {- \pi} ^ {\pi} f (x) \cos n x \mathrm{d} x = 0,
$$

$$
b _ {n} = \frac {1}{\pi} \int_ {- \pi} ^ {\pi} f (x) \sin n x \mathrm{d} x = \frac {2}{\pi} \int_ {0} ^ {\pi} \frac {\pi}{4} \sin n x \mathrm{d} x = \frac {1}{2 n} [ 1 - (- 1) ^ {n} ].
$$

于是当  $x \neq k\pi, k = 0, \pm1, \pm2, \cdots$  时，

$$
f (x) = \sin x + \frac {1}{3} \sin 3 x + \dots + \frac {1}{2 n - 1} \sin (2 n - 1) x + \dots ;
$$

当  $x=k\pi, k=0, \pm1, \pm2, \cdots$  时，级数收敛于 0（实际上级数每一项都为 0）。其收敛过程如图 15-7 所示。

![](../../raw/pages_0065-0096/images/page_74_chart_20.jpg)

<details>
<summary>line</summary>

| Point | Description |
| --- | --- |
| \(-\pi\) | Origin (x, y) |
| O | Intersection point at (0,0) |
| \(-\pi/4\) | Local minimum on x-axis |
| \(\pi/4\) | Local maximum on x-axis |
| \(\pi/2\) | Local maximum on x-axis |
| n=1 | Intermediate point on x-axis |
| n=2 | Intermediate point on x-axis |
| n=7 | Intermediate point on x-axis |
</details>

图15-7

67

---

第十五章 傅里叶级数

## 习题 15.1

1. 在指定区间上把下列函数展开成傅里叶级数:

(1)  $f(x)=x$ , (i)  $-\pi<x<\pi$ , (ii)  $0<x<2\pi$ ;
(2)  $f(x) = x^{2}$ , (i)  $-\pi < x < \pi$ , (ii)  $0 < x < 2\pi$ ;

(3) $f(x) = \begin{cases} ax, & -\pi < x \leqslant 0, \\ bx, & 0 < x < \pi \end{cases} \quad (a \neq b, a \neq 0, b \neq 0)$.

2. 设 $f$ 是以 $2\pi$ 为周期的可积函数, 证明对任何实数 $c$, 有

$$
a _ {n} = \frac {1}{\pi} \int_ {c} ^ {c + 2 \pi} f (x) \cos n x \mathrm{d} x = \frac {1}{\pi} \int_ {- \pi} ^ {\pi} f (x) \cos n x \mathrm{d} x, n = 0, 1, 2, \dots ,
$$

$$
b _ {n} = \frac {1}{\pi} \int_ {c} ^ {c + 2 \pi} f (x) \sin n x \mathrm{d} x = \frac {1}{\pi} \int_ {- \pi} ^ {\pi} f (x) \sin n x \mathrm{d} x, n = 1, 2, \dots .
$$

3. 把函数

$$
f (x) = \left\{ \begin{array}{l l} - \frac {\pi}{4}, & - \pi <   x <   0, \\ \frac {\pi}{4}, & 0 \leqslant x <   \pi \end{array} \right.
$$

展开成傅里叶级数,并由它推出

(1)  $\frac{\pi}{4}=1-\frac{1}{3}+\frac{1}{5}-\frac{1}{7}+\cdots;$

(2)  $\frac{\pi}{3}=1+\frac{1}{5}-\frac{1}{7}-\frac{1}{11}+\frac{1}{13}+\frac{1}{17}+\cdots;$

(3)  $\frac{\sqrt{3}}{6}\pi=1-\frac{1}{5}+\frac{1}{7}-\frac{1}{11}+\frac{1}{13}-\frac{1}{17}+\cdots.$

4. 设函数 $f(x)$ 满足条件 $f(x + \pi) = -f(x)$. 问此函数在 $(- \pi, \pi)$ 上的傅里叶级数具有什么特性.

5. 设函数 $f(x)$ 满足条件 $f(x + \pi) = f(x)$. 问此函数在 $(-\pi, \pi)$ 上的傅里叶级数具有什么特性.

6. 试证函数系 $\cos nx, n = 0, 1, 2, \cdots$ 和 $\sin nx, n = 1, 2, \cdots$ 都是 $[0, \pi]$ 上的正交函数系，但它们合起来的(5)式不是 $[0, \pi]$ 上的正交函数系.

7. 求下列函数的傅里叶级数展开式:

(1)  $f(x) = \frac{\pi - x}{2}, 0 < x < 2\pi$ ;
(2)  $f(x) = \sqrt{1 - \cos x}, -\pi \leqslant x \leqslant \pi;$
(3)  $f(x) = ax^{2} + bx + c$ , (i)  $0 < x < 2\pi$ , (ii)  $-\pi < x < \pi$ ;
(4)  $f(x) = \operatorname{ch} x, -\pi < x < \pi$ ;
(5)  $f(x) = \operatorname{sh} x, -\pi < x < \pi.$

8. 求函数 $f(x) = \frac{1}{12} (3x^2 - 6\pi x + 2\pi^2)$, $0 < x < 2\pi$ 的傅里叶级数展开式，并应用它推出 $\frac{\pi^2}{6} = \sum \frac{1}{n^2}$.

9. 设 $f$ 为 $[- \pi, \pi]$ 上的光滑函数，且 $f(-\pi) = f(\pi). a_n, b_n$ 为 $f$ 的傅里叶系数，$a'_n, b'_n$ 为 $f$ 的导函数 $f'$ 的傅里叶系数。证明:

$$
a _ {0} ^ {\prime} = 0, \quad a _ {n} ^ {\prime} = n b _ {n}, \quad b _ {n} ^ {\prime} = - n a _ {n} \quad (n = 1, 2, \dots).
$$

10. 证明: 若三角级数

$$
\frac {a _ {0}}{2} + \sum_ {n = 1} ^ {\infty} (a _ {n} \cos n x + b _ {n} \sin n x)
$$

中的系数 $a_{n}, b_{n}$ 满足关系

68

---

§ 2 以 2l 为周期的函数的展开式

$$
\sup _ {n} \left\{\mid n ^ {3} a _ {n} \mid , \mid n ^ {3} b _ {n} \mid \right\} \leqslant M,
$$

M 为常数, 则上述三角级数收敛, 且其和函数具有连续的导函数.

## § 2 以 2l 为周期的函数的展开式

在上节的收敛定理中, 假设函数 $f$ 是以 $2\pi$ 为周期的, 或是定义在 $(- \pi, \pi]$ 上然后作以 $2\pi$ 为周期延拓的函数. 本节讨论以 $2l$ 为周期的函数的傅里叶级数展开式及偶函数、奇函数的傅里叶级数展开式.

## 一、以 $2l$ 为周期的函数的傅里叶级数

设 $f$ 是以 $2l$ 为周期的函数，通过变量置换

$$
\frac {\pi x}{l} = t \quad \text {或} \quad x = \frac {l t}{\pi}
$$

可以把 $f$ 变换成以 $2\pi$ 为周期的 $t$ 的函数 $F(t) = f\left(\frac{lt}{\pi}\right)$. 若 $f$ 在 $[-l, l]$ 上可积，则 $F$ 在 $[- \pi, \pi]$ 上也可积，这时函数 $F$ 的傅里叶级数展开式是

$$
F (t) \sim \frac {a _ {0}}{2} + \sum_ {n = 1} ^ {\infty} (a _ {n} \cos n t + b _ {n} \sin n t), \tag {1}
$$

其中

$$
a _ {n} = \frac {1}{\pi} \int_ {- \pi} ^ {\pi} F (t) \cos n t \mathrm{d} t, \quad n = 0, 1, 2, \dots , \tag {2}
$$

$$
b _ {n} = \frac {1}{\pi} \int_ {- \pi} ^ {\pi} F (t) \sin n t \mathrm{d} t, \quad n = 1, 2, \dots .
$$

因为 $t = \frac{\pi x}{l}$，所以 $F(t) = f\left(\frac{lt}{\pi}\right) = f(x)$. 于是由（1）与（2）式分别得

$$
f (x) \sim \frac {a _ {0}}{2} + \sum_ {n = 1} ^ {\infty} \left(a _ {n} \cos \frac {n \pi x}{l} + b _ {n} \sin \frac {n \pi x}{l}\right) \tag {3}
$$

与

$$
a _ {n} = \frac {1}{l} \int_ {- l} ^ {l} f (x) \cos \frac {n \pi x}{l} \mathrm{d} x, \quad n = 0, 1, 2, \dots , \tag {4}
$$

$$
b _ {n} = \frac {1}{l} \int_ {- l} ^ {l} f (x) \sin \frac {n \pi x}{l} \mathrm{d} x, \quad n = 1, 2, \dots .
$$

这里(4)式是以2l为周期的函数f的傅里叶系数,(3)式是f的傅里叶级数.

若函数 $f$ 在 $[-l, l]$ 上按段光滑，则同样可由收敛定理知道

$$
\frac {f (x + 0) + f (x - 0)}{2} = \frac {a _ {0}}{2} + \sum_ {n = 1} ^ {\infty} \left(a _ {n} \cos \frac {n \pi x}{l} + b _ {n} \sin \frac {n \pi x}{l}\right). \tag {5}
$$

例1 把函数

$$
f (x) = \left\{ \begin{array}{l l} 0, & - 5 \leqslant x <   0, \\ 3, & 0 \leqslant x <   5 \end{array} \right.
$$

69

---

第十五章 傅里叶级数

展开成傅里叶级数.

解 由于 f 在  $(-5,5)$  上按段光滑, 因此可以展开成傅里叶级数. 根据 (4) 式, 有

$$
\begin{array}{l} a _ {n} = \frac {1}{5} \int_ {- 5} ^ {0} 0 \cdot \cos \frac {n \pi x}{5} \mathrm{d} x + \frac {1}{5} \int_ {0} ^ {5} 3 \cos \frac {n \pi x}{5} \mathrm{d} x \\ = \frac {3}{5} \cdot \frac {5}{n \pi} \sin \left. \frac {n \pi x}{5} \right| _ {0} ^ {5} = 0, \quad n = 1, 2, \dots , \\ a _ {0} = \frac {1}{5} \int_ {- 5} ^ {5} f (x) \mathrm{d} x = \frac {1}{5} \int_ {0} ^ {5} 3 \mathrm{d} x = 3, \\ b _ {n} = \frac {1}{5} \int_ {0} ^ {5} 3 \sin \frac {n \pi x}{5} \mathrm{d} x = \frac {3}{5} \left[ - \frac {5}{n \pi} \cos \frac {n \pi x}{5} \right] \Bigg | _ {0} ^ {5} = \frac {3 (1 - \cos n \pi)}{n \pi} \\ = \left\{ \begin{array}{c l} \frac {6}{(2 k - 1) \pi}, & n = 2 k - 1, k = 1, 2, \dots , \\ 0, & n = 2 k, k = 1, 2, \dots . \end{array} \right. \\ \end{array}
$$

代入(5)式,得

$$
\begin{array}{l} f (x) = \frac {3}{2} + \sum_ {k = 1} ^ {\infty} \frac {6}{(2 k - 1) \pi} \sin \frac {(2 k - 1) \pi x}{5} \\ = \frac {3}{2} + \frac {6}{\pi} \left(\sin \frac {\pi x}{5} + \frac {1}{3} \sin \frac {3 \pi x}{5} + \frac {1}{5} \sin \frac {5 \pi x}{5} + \dots\right). \\ \end{array}
$$

这里 $x \in (-5,0) \cup (0,5)$. 当 $x = 0$ 和 $\pm 5$ 时级数收敛于 $\frac{3}{2}$.

□

## 二、偶函数与奇函数的傅里叶级数

设 $f$ 是以 $2l$ 为周期的偶函数, 或是定义在 $[-l, l]$ 上的偶函数, 则在 $[-l, l]$ 上, $f(x) \cos nx$ 是偶函数, $f(x) \sin nx$ 是奇函数. 因此, $f$ 的傅里叶系数 (4) 是

$$
\left. \begin{array}{l} a _ {n} = \frac {1}{l} \int_ {- l} ^ {l} f (x) \cos \frac {n \pi x}{l} \mathrm{d} x \\ = \frac {2}{l} \int_ {0} ^ {l} f (x) \cos \frac {n \pi x}{l} \mathrm{d} x, \quad n = 0, 1, 2, \dots , \\ b _ {n} = \frac {1}{l} \int_ {- l} ^ {l} f (x) \sin \frac {n \pi x}{l} \mathrm{d} x = 0, \quad n = 1, 2, \dots . \end{array} \right\} \tag {6}
$$

于是f的傅里叶级数只含有余弦函数的项,即

$$
f (x) \sim \frac {a _ {0}}{2} + \sum_ {n = 1} ^ {\infty} a _ {n} \cos \frac {n \pi x}{l}, \tag {7}
$$

其中 $a_{n}$ 如(6)式所示.(7)式右边的级数称为余弦级数.

同理, 若 f 是以 2l 为周期的奇函数, 或是定义在  $[-l, l]$  上的奇函数, 则可推得

$$
\left. \begin{array}{l} a _ {n} = \frac {1}{l} \int_ {- l} ^ {l} f (x) \cos \frac {n \pi x}{l} \mathrm{d} x = 0, \quad n = 0, 1, 2, \dots , \\ b _ {n} = \frac {2}{l} \int_ {0} ^ {l} f (x) \sin \frac {n \pi x}{l} \mathrm{d} x, \quad n = 1, 2, \dots . \end{array} \right\} \tag {8}
$$

所以当f为奇函数时,它的傅里叶级数只含有正弦函数的项,即

$$
f (x) \sim \sum_ {n = 1} ^ {\infty} b _ {n} \sin \frac {n \pi x}{l}, \tag {9}
$$

70

---

§ 2 以 2l 为周期的函数的展开式

其中  $b_{n}$  如(8)式所示。(9)式右边的级数称为正弦级数.

若 $l = \pi$ ，则偶函数 $f$ 所展开成的余弦级数为

$$
f (x) \sim \frac {a _ {0}}{2} + \sum_ {n = 1} ^ {\infty} a _ {n} \cos n x, \tag {10}
$$

其中

$$
a _ {n} = \frac {2}{\pi} \int_ {0} ^ {\pi} f (x) \cos n x \mathrm{d} x, \quad n = 0, 1, 2, \dots ; \tag {11}
$$

奇函数 $f$ 所展开成的正弦级数为

$$
f (x) \sim \sum_ {n = 1} ^ {\infty} b _ {n} \sin n x, \tag {12}
$$

其中

$$
b _ {n} = \frac {2}{\pi} \int_ {0} ^ {\pi} f (x) \sin n x \mathrm{d} x. \tag {13}
$$

在实际应用中,有时需把定义在 $[0,\pi]$ 上(或一般地,在 $[0,l]$ 上)的函数展开成余弦级数或正弦级数.为此,先把定义在 $[0,\pi]$ 上的函数作偶式延拓或作奇式延拓到 $[-\pi,\pi]$ 上(如图15-8(a)或(b)).然后求延拓后函数的傅里叶级数,即得(10)或(12)形式.但显然可见,对于定义在 $[0,\pi]$ 上的函数,将它展开成余弦级数或正弦级数时,可以直接由(11)式或(13)式计算出它的傅里叶系数.

![](../../raw/pages_0065-0096/images/page_78_chart_11.jpg)

<details>
<summary>contour</summary>

| X | Y |
| --- | --- |
| \(-\pi\) | ~0.8 |
| 0 | 0 |
| \(\pi\) | ~0.8 |
</details>

(a) 偶式延拓

![](../../raw/pages_0065-0096/images/page_78_image_13.jpg)

<details>
<summary>text_image</summary>

-π
O
π x
y
</details>

(b) 奇式延拓

图15-8

例2 设函数

$$
f (x) = \left| \sin x \right|, - \pi \leqslant x <   \pi ,
$$

求 f 的傅里叶级数展开式.

解 $f$ 是 $[- \pi, \pi]$ 上的偶函数, 图15-9是这函数及其周期延拓的图形. 由于 $f$ 是按段光滑函数, 因此可以展开成傅里叶级数, 而且这个级数为余弦级数. 由(10)式(这时可把其中“$\sim$”改为“=”）知

$$
\left| \sin x \right| = \frac {a _ {0}}{2} + \sum_ {n = 1} ^ {\infty} a _ {n} \cos n x,
$$

其中

71

---

第十五章 傅里叶级数

![](../../raw/pages_0065-0096/images/page_79_image_1.jpg)

<details>
<summary>text_image</summary>

-2π
-π
O
π
2π
3π
x
y
</details>

图15-9

$$
\begin{array}{l} a _ {0} = \frac {2}{\pi} \int_ {0} ^ {\pi} \sin x \mathrm{d} x = \frac {4}{\pi}, \\ a _ {1} = \frac {2}{\pi} \int_ {0} ^ {\pi} \sin x \cos x \mathrm{d} x = 0, \\ a _ {n} = \frac {2}{\pi} \int_ {0} ^ {\pi} | \sin x | \cos n x \mathrm{d} x = \frac {2}{\pi} \int_ {0} ^ {\pi} \sin x \cos n x \mathrm{d} x \\ = \frac {2}{\pi} \int_ {0} ^ {\pi} \frac {1}{2} [ \sin (1 - n) x + \sin (1 + n) x ] \mathrm{d} x \\ = \frac {1}{\pi} \frac {2}{n ^ {2} - 1} [ \cos (n - 1) \pi - 1 ] \quad (n \neq 1) \\ = \left\{ \begin{array}{c l} 0, & n = 3, 5, \dots , \\ - \frac {4}{\pi} \frac {1}{n ^ {2} - 1}, & n = 2, 4, \dots . \end{array} \right. \\ \end{array}
$$

因此

$$
\begin{array}{l} \left| \sin x \right| = \frac {2}{\pi} - \frac {1}{\pi} \sum_ {m = 1} ^ {\infty} \frac {4}{4 m ^ {2} - 1} \cos 2 m x \\ = \frac {2}{\pi} \left(1 - 2 \sum_ {m = 1} ^ {\infty} \frac {\cos 2 m x}{4 m ^ {2} - 1}\right), - \infty <   x <   + \infty. \\ \end{array}
$$

当 $x = 0$ 时，有

$$
0 = \frac {2}{\pi} \bigg (1 - 2 \sum_ {m = 1} ^ {\infty} \frac {1}{4 m ^ {2} - 1} \bigg).
$$

由此可得

$$
\frac {1}{2} = \frac {1}{1 \cdot 3} + \frac {1}{3 \cdot 5} + \dots + \frac {1}{(2 m - 1) (2 m + 1)} + \dots .
$$

例 3 把定义在 $[0,\pi]$ 上的函数

$$
f (x) = \left\{ \begin{array}{l l} 1, & 0 \leqslant x <   h, \\ \frac {1}{2}, & x = h, \\ 0, & h <   x \leqslant \pi \end{array} \right.
$$

(其中  $0 < h < \pi$ ) 展开成正弦级数.

解 函数 f 如图 15-10 所示, 它是按段光滑函数, 因而可以展开成正弦级数 (12), 其系数

$$
b _ {n} = \frac {2}{\pi} \int_ {0} ^ {\pi} f (x) \sin n x \mathrm{d} x = \frac {2}{\pi} \int_ {0} ^ {h} \sin n x \mathrm{d} x
$$

72

---

§ 2 以 2l 为周期的函数的展开式

$$
= \frac {2}{\pi} \Big (\frac {- \cos n x}{n} \Big) \Bigg | _ {0} ^ {h} = \frac {2}{n \pi} (1 - \cos n h).
$$

所以

$$
f (x) = \frac {2}{\pi} \sum_ {n = 1} ^ {\infty} \frac {(1 - \cos n h)}{n} \sin n x, \quad 0 <   x <   h, \quad h <   x <   \pi .
$$

当 $x = 0$ 时，级数的和为0；当 $x = h$ 时，有

$$
\frac {2}{\pi} \sum_ {n = 1} ^ {\infty} \frac {(1 - \cos n h)}{n} \sin n h = \frac {1 + 0}{2} = \frac {1}{2}.
$$

本题中若 $h = \pi$ ，则有

$$
\begin{array}{l} f (x) = \frac {2}{\pi} \sum_ {n = 1} ^ {\infty} \frac {1 - (- 1) ^ {n}}{n} \sin n x \\ = \frac {4}{\pi} \left(\sin x + \frac {1}{3} \sin 3 x + \frac {1}{5} \sin 5 x + \dots\right), 0 <   x <   \pi, \\ \end{array}
$$

而且当 $x = 0, \pi$ 时，级数收敛于0.

![](../../raw/pages_0065-0096/images/page_80_chart_9.jpg)

<details>
<summary>scatter</summary>

| X | Y |
| --- | --- |
| 0 | 1 |
| h | 0 |
| h | ~0.5 |
</details>

图15-10

![](../../raw/pages_0065-0096/images/page_80_chart_11.jpg)

<details>
<summary>scatter</summary>

| X | Y |
| --- | --- |
| -6 | 2 |
| -6 | -2 |
| -2 | 2 |
| -2 | -2 |
| 0 | 0 |
| 2 | 2 |
| 2 | -2 |
| 6 | 2 |
| 6 | -2 |
| 12 | 2 |
</details>

图15-11

例4 把 $f(x) = x$ 在 $(0,2)$ 上展开成:

(i) 正弦级数；
(ii) 余弦级数.

解 （i）为了要把 f 展开为正弦级数, 对 f 作奇式周期延拓(图 15-11), 并由公式 (8)有

$$
a _ {n} = 0, \quad n = 0, 1, 2, \dots ,
$$

$$
b _ {n} = \frac {2}{2} \int_ {0} ^ {2} x \sin \frac {n \pi x}{2} \mathrm{d} x = - \frac {4}{n \pi} \cos n \pi = \frac {4}{n \pi} (- 1) ^ {n + 1}, \quad n = 1, 2, \dots .
$$

所以当 $x \in (0,2)$ 时，由公式(9)及收敛定理得到

$$
\begin{array}{l} f (x) = x = \sum_ {n = 1} ^ {\infty} \frac {4}{n \pi} (- 1) ^ {n + 1} \sin \frac {n \pi x}{2} \tag {14} \\ = \frac {4}{\pi} \left(\sin \frac {\pi x}{2} - \frac {1}{2} \sin \frac {2 \pi x}{2} + \frac {1}{3} \sin \frac {3 \pi x}{2} + \dots\right). \\ \end{array}
$$

但当 x=0,2 时,右边级数收敛于 0.

(ii) 为了要把 $f$ 展开为余弦级数, 对 $f$ 作偶式周期延拓 (图15-12).

由公式(6)得 $f$ 的傅里叶系数为

$$
b _ {n} = 0, \quad n = 1, 2, \dots ,
$$

$$
a _ {0} = \int_ {0} ^ {2} x \mathrm{d} x = 2,
$$

73

---

第十五章 傅里叶级数

![](../../raw/pages_0065-0096/images/page_81_chart_1.jpg)

<details>
<summary>line</summary>

| X | Y |
| --- | --- |
| -6 | 2 |
| -4 | 0 |
| -2 | 2 |
| 0 | 0 |
| 2 | 2 |
| 4 | 0 |
| 6 | 2 |
</details>

图15-12

$$
\begin{array}{l} a _ {n} = \frac {2}{2} \int_ {0} ^ {2} x \cos \frac {n \pi x}{2} \mathrm{d} x = \frac {4}{n ^ {2} \pi^ {2}} (\cos n \pi - 1) \\ = \frac {4}{n ^ {2} \pi^ {2}} \big [ (- 1) ^ {n} - 1 \big ], \quad n = 1, 2, \dots \\ \end{array}
$$

或

$$
a _ {2 k - 1} = \frac {- 8}{(2 k - 1) ^ {2} \pi^ {2}}, \quad a _ {2 k} = 0 (k = 1, 2, \dots).
$$

所以当 $x \in (0,2)$ 时，由公式(7)及收敛定理得到

$$
\begin{array}{l} f (x) = x = 1 + \sum_ {k = 1} ^ {\infty} \frac {- 8}{(2 k - 1) ^ {2} \pi^ {2}} \cos \frac {(2 k - 1) \pi x}{2} \\ = 1 - \frac {8}{\pi^ {2}} \left(\cos \frac {\pi x}{2} + \frac {1}{3 ^ {2}} \cos \frac {3 \pi x}{2} + \frac {1}{5 ^ {2}} \cos \frac {5 \pi x}{2} + \dots\right). \tag {15} \\ \end{array}
$$

读者由例 4 可以看到,同样一个函数在同样的区间上可以用正弦级数表示,也可以用余弦级数表示,甚至作适当延拓后,可以用更一般的形式(5)来表示.

## 习题 15.2

1. 求下列周期函数的傅里叶级数展开式:

(1)  $f(x)=\left|\cos x\right|$  (周期  $\pi$ );

(2) $f(x) = x - [x]$ （周期1）；

(3)  $f(x) = \sin^{4} x$  (周期  $\pi$ );

(4) $f(x) = \operatorname{sgn}(\cos x)$ （周期 $2\pi$）.

2. 求函数

$$
f (x) = \left\{ \begin{array}{l l} x, & 0 \leqslant x \leqslant 1, \\ 1, & 1 <   x <   2, \\ 3 - x, & 2 \leqslant x \leqslant 3 \end{array} \right.
$$

的傅里叶级数并讨论其敛散性.

3. 将函数 $f(x) = \frac{\pi}{2} - x$ 在 $[0, \pi]$ 上展开成余弦级数.

4. 将函数 $f(x) = \cos \frac{x}{2}$ 在 $[0, \pi]$ 上展开成正弦级数.

5. 把函数

$$
f (x) = \left\{ \begin{array}{l l} 1 - x, & 0 <   x \leqslant 2, \\ x - 3, & 2 <   x <   4 \end{array} \right.
$$

在 $(0,4)$ 上展开成余弦级数.

74

---

§ 3 收敛定理的证明

6. 把函数 $f(x) = (x - 1)^2$ 在(0,1)上展开成余弦级数，并推出

$$
\pi^ {2} = 6 \bigg (1 + \frac {1}{2 ^ {2}} + \frac {1}{3 ^ {2}} + \dots \bigg).
$$

7. 求下列函数的傅里叶级数展开式:

(1)  $f(x) = \arcsin(\sin x)$ ;

(2) $f(x) = \arcsin (\cos x)$.

8. 试问如何把定义在 $\left[0, \frac{\pi}{2}\right]$ 上的可积函数 $f$ 延拓到区间 $(- \pi, \pi)$ 上，使它们的傅里叶级数为如下的形式:

(1) $\sum_{n=1}^{\infty} a_{2n-1} \cos (2n - 1)x$;

(2) $\sum_{n=1}^{\infty} b_{2n-1} \sin (2n-1)x$.

## § 3 收敛定理的证明

为了证明傅里叶级数的收敛定理,先证明下面两个预备定理.

预备定理 1(贝塞尔(Bessel)不等式) 若函数 f 在  $[-π, π]$  上可积, 则

$$
\frac {a _ {0} ^ {2}}{2} + \sum_ {n = 1} ^ {\infty} (a _ {n} ^ {2} + b _ {n} ^ {2}) \leqslant \frac {1}{\pi} \int_ {- \pi} ^ {\pi} f ^ {2} (x) \mathrm{d} x, \tag {1}
$$

其中  $a_{n}, b_{n}$  为 f 的傅里叶系数。(1) 式称为贝塞尔不等式.

证令

$$
S _ {m} (x) = \frac {a _ {0}}{2} + \sum_ {n = 1} ^ {m} (a _ {n} \cos n x + b _ {n} \sin n x).
$$

考察积分

$$
\begin{array}{l} \int_ {- \pi} ^ {\pi} \left[ f (x) - S _ {m} (x) \right] ^ {2} \mathrm{d} x \\ = \int_ {- \pi} ^ {\pi} f ^ {2} (x) \mathrm{d} x - 2 \int_ {- \pi} ^ {\pi} f (x) S _ {m} (x) \mathrm{d} x + \int_ {- \pi} ^ {\pi} S _ {m} ^ {2} (x) \mathrm{d} x. \tag {2} \\ \end{array}
$$

由于

$$
\begin{array}{l} \int_ {- \pi} ^ {\pi} f (x) S _ {m} (x) \mathrm{d} x \\ = \frac {a _ {0}}{2} \int_ {- \pi} ^ {\pi} f (x) \mathrm{d} x + \sum_ {n = 1} ^ {m} \left(a _ {n} \int_ {- \pi} ^ {\pi} f (x) \cos n x \mathrm{d} x + b _ {n} \int_ {- \pi} ^ {\pi} f (x) \sin n x \mathrm{d} x\right). \\ \end{array}
$$

根据傅里叶系数公式(§1,公式(10))可得

$$
\int_ {- \pi} ^ {\pi} f (x) S _ {m} (x) \mathrm{d} x = \frac {\pi}{2} a _ {0} ^ {2} + \pi \sum_ {n = 1} ^ {m} (a _ {n} ^ {2} + b _ {n} ^ {2}). \tag {3}
$$

对于 $S_{m}^{2}(x)$ 的积分，应用三角函数的正交性，有

$$
\begin{array}{l} \int_ {- \pi} ^ {\pi} S _ {m} ^ {2} (x)   \mathrm{d} x \\ = \int_ {- \pi} ^ {\pi} \left[ \frac {a _ {0}}{2} + \sum_ {n = 1} ^ {m} (a _ {n} \cos n x + b _ {n} \sin n x) \right] ^ {2} \mathrm{d} x \\ \end{array}
$$

75

---

第十五章 傅里叶级数

$$
\begin{array}{l} = \left(\frac {a _ {0}}{2}\right) ^ {2} \int_ {- \pi} ^ {\pi} \mathrm{d} x + \sum_ {n = 1} ^ {m} \left[ a _ {n} ^ {2} \int_ {- \pi} ^ {\pi} \cos^ {2} n x \mathrm{d} x + b _ {n} ^ {2} \int_ {- \pi} ^ {\pi} \sin^ {2} n x \mathrm{d} x \right] \\ = \frac {\pi a _ {0} ^ {2}}{2} + \pi \sum_ {n = 1} ^ {m} (a _ {n} ^ {2} + b _ {n} ^ {2}). \tag {4} \\ \end{array}
$$

将(3)式、(4)式代入(2)式,可得

$$
\begin{array}{l} 0 \leqslant \int_ {- \pi} ^ {\pi} \left[ f (x) - S _ {m} (x) \right] ^ {2} \mathrm{d} x \\ = \int_ {- \pi} ^ {\pi} f ^ {2} (x) \mathrm{d} x - \frac {\pi a _ {0} ^ {2}}{2} - \pi \sum_ {n = 1} ^ {m} (a _ {n} ^ {2} + b _ {n} ^ {2}). \\ \end{array}
$$

因而

$$
\frac {a _ {0} ^ {2}}{2} + \sum_ {n = 1} ^ {m} (a _ {n} ^ {2} + b _ {n} ^ {2}) \leqslant \frac {1}{\pi} \int_ {- \pi} ^ {\pi} [ f (x) ] ^ {2} \mathrm{d} x
$$

对任何正整数 $m$ 成立. 而 $\frac{1}{\pi} \int_{-\pi}^{\pi} [f(x)]^2 \, \mathrm{d}x$ 为有限值, 所以正项级数

$$
\frac {a _ {0} ^ {2}}{2} + \sum_ {n = 1} ^ {\infty} (a _ {n} ^ {2} + b _ {n} ^ {2})
$$

的部分和数列有界,因而它收敛且有不等式(1)成立.

□

推论 1 若 f 为可积函数, 则

$$
\left. \begin{array}{l} \lim _ {n \to \infty} \int_ {- \pi} ^ {\pi} f (x) \cos n x \mathrm{d} x = 0, \\ \lim _ {n \to \infty} \int_ {- \pi} ^ {\pi} f (x) \sin n x \mathrm{d} x = 0. \end{array} \right\} \tag {5}
$$

因为(1)式的左边级数收敛,所以当  $n \to \infty$  时,通项  $a_{n}^{2} + b_{n}^{2} \to 0$ ,亦即有  $a_{n} \to 0$  与  $b_{n} \to 0$ ,这就是(5)式.这个推论也称为黎曼-勒贝格定理.

推论 2 若 f 为可积函数, 则

$$
\left. \begin{array}{l} \lim _ {n \to \infty} \int_ {0} ^ {\pi} f (x) \sin \left(n + \frac {1}{2}\right) x \mathrm{d} x = 0, \\ \lim _ {n \to \infty} \int_ {- \pi} ^ {0} f (x) \sin \left(n + \frac {1}{2}\right) x \mathrm{d} x = 0. \end{array} \right\} \tag {6}
$$

证 由于

$$
\sin \left(n + \frac {1}{2}\right) x = \cos \frac {x}{2} \sin n x + \sin \frac {x}{2} \cos n x,
$$

所以

$$
\begin{array}{l} \int_ {0} ^ {\pi} f (x) \sin \left(n + \frac {1}{2}\right) x \mathrm{d} x \\ = \int_ {0} ^ {\pi} \left[ f (x) \cos \frac {x}{2} \right] \sin n x \mathrm{d} x + \int_ {0} ^ {\pi} \left[ f (x) \sin \frac {x}{2} \right] \cos n x \mathrm{d} x \\ = \int_ {- \pi} ^ {\pi} F _ {1} (x) \sin n x \mathrm{d} x + \int_ {- \pi} ^ {\pi} F _ {2} (x) \cos n x \mathrm{d} x, \tag {7} \\ \end{array}
$$

其中

76

---

§ 3 收敛定理的证明

$$
F _ {1} (x) = \left\{ \begin{array}{c l} f (x) \cos \frac {x}{2}, & 0 \leqslant x \leqslant \pi , \\ 0, & - \pi \leqslant x <   0, \end{array} \right.
$$

$$
F _ {2} (x) = \left\{ \begin{array}{c l} f (x) \sin \frac {x}{2}, & 0 \leqslant x \leqslant \pi , \\ 0, & - \pi \leqslant x <   0. \end{array} \right.
$$

显见 $F_{1}$ 与 $F_{2}$ 和 $f$ 一样在 $[- \pi, \pi]$ 上可积. 由推论1,(7)式右端两积分的极限在 $n \to \infty$ 时都等于零, 所以左边的极限为零.

同样可以证明

$$
\lim _ {n \to \infty} \int_ {- \pi} ^ {0} f (x) \sin \left(n + \frac {1}{2}\right) x \mathrm{d} x = 0.
$$

预备定理2 若 $f(x)$ 是以 $2\pi$ 为周期的函数，且在 $[- \pi, \pi]$ 上可积，则它的傅里叶级数部分和 $S_{n}(x)$ 可写成

$$
S _ {n} (x) = \frac {1}{\pi} \int_ {- \pi} ^ {\pi} f (x + t) \frac {\sin \left(n + \frac {1}{2}\right) t}{2 \sin \frac {t}{2}} \mathrm{d} t, \tag {8}
$$

当 $t = 0$ 时，被积函数中的不定式由极限

$$
\lim _ {t \to 0} \frac {\sin \left(n + \frac {1}{2}\right) t}{2 \sin \frac {t}{2}} = n + \frac {1}{2}
$$

来确定.

证 在傅里叶级数部分和

$$
S _ {n} (x) = \frac {a _ {0}}{2} + \sum_ {k = 1} ^ {n} (a _ {k} \cos k x + b _ {k} \sin k x)
$$

中,用傅里叶系数公式代入,可得

$$
\begin{array}{l} S _ {n} (x) = \frac {1}{2 \pi} \int_ {- \pi} ^ {\pi} f (u) \mathrm{d} u + \frac {1}{\pi} \sum_ {k = 1} ^ {n} \left[ \left(\int_ {- \pi} ^ {\pi} f (u) \cos k u \mathrm{d} u\right) \cos k x + \left(\int_ {- \pi} ^ {\pi} f (u) \sin k u \mathrm{d} u\right) \sin k x \right] \\ = \frac {1}{\pi} \int_ {- \pi} ^ {\pi} f (u) \left[ \frac {1}{2} + \sum_ {k = 1} ^ {n} (\cos k u \cos k x + \sin k u \sin k x) \right] \mathrm{d} u \\ = \frac {1}{\pi} \int_ {- \pi} ^ {\pi} f (u) \left[ \frac {1}{2} + \sum_ {k = 1} ^ {n} \cos k (u - x) \right] \mathrm{d} u. \\ \end{array}
$$

令 $u = x + t$ ，得

$$
S _ {n} (x) = \frac {1}{\pi} \int_ {- \pi - x} ^ {\pi - x} f (x + t) \left[ \frac {1}{2} + \sum_ {k = 1} ^ {n} \cos k t \right] \mathrm{d} t.
$$

由上面这个积分看到,被积函数是周期为  $2\pi$  的函数,因此在  $[-\pi-x,\pi-x]$  上的积分等于  $[-\pi,\pi]$  上的积分,再由第十二章 §3 的(21)式,即

$$
\frac {1}{2} + \sum_ {k = 1} ^ {n} \cos k t = \frac {\sin \left(n + \frac {1}{2}\right) t}{2 \sin \frac {t}{2}}, \tag {9}
$$

77

---

第十五章 傅里叶级数

就得到

$$
S _ {n} (x) = \frac {1}{\pi} \int_ {- \pi} ^ {\pi} f (x + t) \frac {\sin \left(n + \frac {1}{2}\right) t}{2 \sin \frac {t}{2}} \mathrm{d} t.
$$

(8)式也称为f的傅里叶级数部分和的积分表示式.

现在证明定理 15.3(收敛定理), 重述如下:

若以 $2\pi$ 为周期的函数 $f$ 在 $[- \pi, \pi]$ 上按段光滑，则在每一点 $x \in [-\pi, \pi]$，$f$ 的傅里叶级数（本章 §1 的 (12) 式）收敛于 $f$ 在点 $x$ 的左、右极限的算术平均值，即

$$
\frac {f (x + 0) + f (x - 0)}{2} = \frac {a _ {0}}{2} + \sum_ {n = 1} ^ {\infty} \left(a _ {n} \cos n x + b _ {n} \sin n x\right),
$$

其中  $a_{n}, b_{n}$  为 f 的傅里叶系数.

证 只要证明在每一点 x 处下述极限成立:

$$
\lim _ {n \to \infty} \left[ \frac {f (x + 0) + f (x - 0)}{2} - S _ {n} (x) \right] = 0,
$$

即

$$
\lim _ {n \to \infty} \left[ \frac {f (x + 0) + f (x - 0)}{2} - \frac {1}{\pi} \int_ {- \pi} ^ {\pi} f (x + t) \frac {\sin \left(n + \frac {1}{2}\right) t}{2 \sin \frac {t}{2}} \mathrm{d} t \right] = 0,
$$

或证明同时有

$$
\lim _ {n \to \infty} \left[ \frac {f (x + 0)}{2} - \frac {1}{\pi} \int_ {0} ^ {\pi} f (x + t) \frac {\sin \left(n + \frac {1}{2}\right) t}{2 \sin \frac {t}{2}} \mathrm{d} t \right] = 0 \tag {10}
$$

与

$$
\lim _ {n \to \infty} \left[ \frac {f (x - 0)}{2} - \frac {1}{\pi} \int_ {- \pi} ^ {0} f (x + t) \frac {\sin \left(n + \frac {1}{2}\right) t}{2 \sin \frac {t}{2}} \mathrm{d} t \right] = 0. \tag {11}
$$

现在先证明(10)式. 对(9)式积分有

$$
\frac {1}{\pi} \int_ {- \pi} ^ {\pi} \frac {\sin \left(n + \frac {1}{2}\right) t}{2 \sin \frac {t}{2}} \mathrm{d} t = \frac {1}{\pi} \int_ {- \pi} ^ {\pi} \left(\frac {1}{2} + \sum_ {k = 1} ^ {n} \cos k t\right) \mathrm{d} t = 1.
$$

由于上式左边为偶函数,因此两边乘以 $f(x+0)$ 后得到

$$
\frac {f (x + 0)}{2} = \frac {1}{\pi} \int_ {0} ^ {\pi} f (x + 0) \frac {\sin \left(n + \frac {1}{2}\right) t}{2 \sin \frac {t}{2}} \mathrm{d} t.
$$

从而(10)式可改写为

78

---

§ 3 收敛定理的证明

$$
\lim _ {n \to \infty} \frac {1}{\pi} \int_ {0} ^ {\pi} [ f (x + 0) - f (x + t) ] \frac {\sin \left(n + \frac {1}{2}\right) t}{2 \sin \frac {t}{2}} \mathrm{d} t = 0. \tag {12}
$$

令

$$
\begin{array}{l} \varphi (t) = - \frac {f (x + t) - f (x + 0)}{2 \sin \frac {t}{2}} \\ = - \left[ \frac {f (x + t) - f (x + 0)}{t} \right] \frac {\frac {t}{2}}{\sin \frac {t}{2}}, \quad t \in (0, \pi ]. \\ \end{array}
$$

由本章 §1 的(13)式得

$$
\lim _ {t \to 0 ^ {+}} \varphi (t) = - f ^ {\prime} (x + 0) \cdot 1 = - f ^ {\prime} (x + 0).
$$

再令 $\varphi(0) = -f'(x + 0)$，则函数 $\varphi$ 在点 $t = 0$ 右连续。因为 $\varphi$ 在 $[0, \pi]$ 上至多只有有限个第一类间断点，所以 $\varphi$ 在 $[0, \pi]$ 上可积。根据预备定理1的推论2，

$$
\begin{array}{l} \lim _ {n \to \infty} \frac {1}{\pi} \int_ {0} ^ {\pi} [ f (x + 0) - f (x + t) ] \frac {\sin \left(n + \frac {1}{2}\right) t}{2 \sin \frac {t}{2}} \mathrm{d} t \\ = \lim _ {n \to \infty} \frac {1}{\pi} \int_ {0} ^ {\pi} \varphi (t) \sin \left(n + \frac {1}{2}\right) t \mathrm{d} t = 0. \\ \end{array}
$$

这就证得(12)式成立,从而(10)式成立.

用同样方法可证(11)式也成立.

## 习题 15.3①

1. 设 $f$ 以 $2\pi$ 为周期且具有二阶连续的导函数, 证明 $f$ 的傅里叶级数在 $(-\infty, +\infty)$ 上一致收敛于 $f$.
2. 设 $f$ 为 $[- \pi, \pi]$ 上的可积函数. 证明: 若 $f$ 的傅里叶级数在 $[- \pi, \pi]$ 上一致收敛于 $f$, 则成立帕塞瓦尔 (Parseval) 等式:

$$
\frac {1}{\pi} \int_ {- \pi} ^ {\pi} [ f (x) ] ^ {2} \mathrm{d} x = \frac {a _ {0} ^ {2}}{2} + \sum_ {n = 1} ^ {\infty} (a _ {n} ^ {2} + b _ {n} ^ {2}),
$$

这里 $a_{n}, b_{n}$ 为 $f$ 的傅里叶系数.

3. 帕塞瓦尔等式对于在 $[- \pi, \pi]$ 上满足收敛定理条件的函数也成立（证略）。请应用这个结果证明下列各式:

(1) $\frac{\pi^2}{8} = \sum_{n=1}^{\infty} \frac{1}{(2n-1)^2}$ (提示:应用 §1 习题3 的展开式导出);
(2) $\frac{\pi^2}{6} = \sum_{n=1}^{\infty} \frac{1}{n^2}$ (提示: 应用 §1 习题 1(1)(i) 的展开式导出);

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 本节习题均为选做题.</span></small>

79

---

第十五章 傅里叶级数

(3) $\frac{\pi^4}{90} = \sum_{n=1}^{\infty} \frac{1}{n^4}$ (提示: 应用 §1 习题 1(2)(i) 的展开式导出).

4. 证明: 若 $f, g$ 均为 $[- \pi, \pi]$ 上的可积函数, 且它们的傅里叶级数在 $[- \pi, \pi]$ 上分别一致收敛于 $f$ 和 $g$, 则

$$
\frac {1}{\pi} \int_ {- \pi} ^ {\pi} f (x) g (x) \mathrm{d} x = \frac {a _ {0} \alpha_ {0}}{2} + \sum_ {n = 1} ^ {\infty} (a _ {n} \alpha_ {n} + b _ {n} \beta_ {n}),
$$

其中 $a_{n}, b_{n}$ 为 $f$ 的傅里叶系数，$\alpha_{n}, \beta_{n}$ 为 $g$ 的傅里叶系数.

5. 证明: 若 $f$ 及其导函数 $f'$ 均在 $[- \pi, \pi]$ 上可积, $\int_{-\pi}^{\pi} f(x) \mathrm{d}x = 0, f(-\pi) = f(\pi)$, 且成立帕塞瓦尔等式, 则

$$
\int_ {- \pi} ^ {\pi} \left| f ^ {\prime} (x) \right| ^ {2} \mathrm{d} x \geqslant \int_ {- \pi} ^ {\pi} \left| f (x) \right| ^ {2} \mathrm{d} x.
$$

## 第十五章总练习题

1. 试求三角多项式

$$
T _ {n} (x) = \frac {A _ {0}}{2} + \sum_ {k = 1} ^ {n} (A _ {k} \cos k x + B _ {k} \sin k x)
$$

的傅里叶级数展开式.

2. 设 f 为  $[-π, π]$  上的可积函数， $a_{0}, a_{k}, b_{k}$  ( $k=1,2,\cdots,n$ ) 为 f 的傅里叶系数. 试证明:当

$$
A _ {0} = a _ {0}, \quad A _ {k} = a _ {k}, \quad B _ {k} = b _ {k} (k = 1, 2, \dots , n)
$$

时,积分

$$
\int_ {- \pi} ^ {\pi} \left[ f (x) - T _ {n} (x) \right] ^ {2} \mathrm{d} x
$$

取最小值,且最小值为

$$
\int_ {- \pi} ^ {\pi} [ f (x) ] ^ {2} \mathrm{d} x - \pi \left[ \frac {a _ {0} ^ {2}}{2} + \sum_ {k = 1} ^ {n} (a _ {k} ^ {2} + b _ {k} ^ {2}) \right].
$$

上述  $T_{n}(x)$  是第 1 题中的三角多项式,  $A_{0}, A_{k}, B_{k}$  为它的傅里叶系数.

3. 设 f 是以  $2\pi$  为周期, 且具有二阶连续可微的函数,

$$
b _ {n} = \frac {1}{\pi} \int_ {- \pi} ^ {\pi} f (x) \sin n x \mathrm{d} x, \quad b _ {n} ^ {\prime \prime} = \frac {1}{\pi} \int_ {- \pi} ^ {\pi} f ^ {\prime \prime} (x) \sin n x \mathrm{d} x.
$$

若级数 $\sum b_{n}^{\prime \prime}$ 绝对收敛，则

$$
\sum_ {n = 1} ^ {\infty} \sqrt {| b _ {n} |} \leqslant \frac {1}{2} \big (2 + \sum_ {n = 1} ^ {\infty} | b _ {n} ^ {\prime \prime} | \big) .
$$

4. 设周期为 $2\pi$ 的可积函数 $\varphi(x)$ 与 $\psi(x)$ 满足以下关系式:

(1)  $\varphi(-x)=\psi(x)$ ;

(2) $\varphi(-x) = -\psi(x)$.

试问  $\varphi$  的傅里叶系数  $a_{n}, b_{n}$  与  $\psi$  的傅里叶系数  $\alpha_{n}, \beta_{n}$  有什么关系？

5. 设定义在 $[a, b]$ 上的连续函数列 $\{\varphi_n\}$ 满足关系

$$
\int_ {a} ^ {b} \varphi_ {n} (x) \varphi_ {m} (x) \mathrm{d} x = \left\{ \begin{array}{l l} 0, & n \neq m, \\ 1, & n = m. \end{array} \right.
$$

对于在 $[a, b]$ 上的可积函数 $f$, 定义

$$
a _ {n} = \int_ {a} ^ {b} f (x) \varphi_ {n} (x) \mathrm{d} x, \quad n = 1, 2, \dots .
$$

80

---

第十五章总练习题

11

证明: $\sum_{n = 1}^{\infty}a_n^2$ 收敛，且有不等式

$$
\sum_ {n = 1} ^ {\infty} a _ {n} ^ {2} \leqslant \int_ {a} ^ {b} \left[ f (x) \right] ^ {2} \mathrm{d} x.
$$

![](../../raw/pages_0065-0096/images/page_88_image_4.jpg)

## 第十五章综合自测题

81
