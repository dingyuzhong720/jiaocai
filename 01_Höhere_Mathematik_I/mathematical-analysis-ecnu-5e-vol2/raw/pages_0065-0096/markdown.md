## \* §3 复变量的指数函数·欧拉公式

先讲复数项级数. 设级数

$$
u _ {1} + u _ {2} + \dots + u _ {n} + \dots \tag {1}
$$

中每一项都是复数  $u_{n}=a_{n}+ib_{n}$  （ $a_{n},b_{n}$  为实数，i 为虚部单位）（ $n=1,2,\cdots$ ），则（1）式可写成

$$
\left(a _ {1} + \mathrm{i} b _ {1}\right) + \left(a _ {2} + \mathrm{i} b _ {2}\right) + \dots + \left(a _ {n} + \mathrm{i} b _ {n}\right) + \dots . \tag {2}
$$

以 $S_{n}$ 表示(2)的第 $n$ 个部分和，并记

$$
R _ {n} = \sum_ {k = 1} ^ {n} a _ {k}, \quad I _ {n} = \sum_ {k = 1} ^ {n} b _ {k},
$$

则有

$$
S _ {n} = R _ {n} + \mathrm{i} I _ {n}.
$$

若 $\lim_{n\to \infty}R_n$ 与 $\lim_{n\to \infty}I_n$ 存在, 则称级数(1)收敛, 若用 $A, B$ 分别表示这两个极限值, 则级数(1)的和记为 $A + \mathrm{i}B$. 据此, 级数(1)收敛的充要条件是: 级数

$$
\sum_ {n = 1} ^ {\infty} a _ {n} \quad \text {与} \quad \sum_ {n = 1} ^ {\infty} b _ {n}
$$

都收敛.

级数(1)各项 $u_{n}$ 的模为

$$
\mid u _ {n} \mid = \sqrt {a _ {n} ^ {2} + b _ {n} ^ {2}}, \quad n = 1, 2, \dots .
$$

若级数

$$
\left| u _ {1} \right| + \left| u _ {2} \right| + \dots + \left| u _ {n} \right| + \dots
$$

收敛,则称级数(1)绝对收敛.由关系式

$$
\mid a _ {n} \mid \leqslant \mid u _ {n} \mid , \quad \mid b _ {n} \mid \leqslant \mid u _ {n} \mid , \quad n = 1, 2, \dots
$$

可证得:若级数(1)绝对收敛,则级数(1)必收敛.

设  $c_{n}$  ( $n=0,1,2,\cdots$ ) 为复数, z 为复变量, 则称级数

$$
c _ {0} + c _ {1} z + c _ {2} z ^ {2} + \dots + c _ {n} z ^ {n} + \dots \tag {3}
$$

为复数项幂级数. 若在 $z = z_0$ 处级数(3)收敛, 则称它在点 $z_0$ 收敛. 所有使级数(3)收敛的全体复数构成复数项幂级数(3)的收敛域. 记

$$
\rho = \varlimsup_ {n \to \infty} \sqrt [ n ]{\left| c _ {n} \right|},
$$

这时和 §1 实数项幂级数一样可证明: 级数(3)对一切满足  $\left|z\right|<\frac{1}{\rho}$  的 z 不仅收敛, 而且绝对收敛; 对一切  $\left|z\right|>\frac{1}{\rho}$  的 z, 级数(3)是发散的. 现以  $R=\frac{1}{\rho}$  表示复数项幂级数(3)的收敛半径 (当  $\rho=0$  时,  $R=+\infty$ ; 当  $\rho=+\infty$  时, R=0), 则级数(3)的收敛范围是复平面上的以原点为中心, R 为半径的圆.

例如级数

$$
1 + z + \frac {z ^ {2}}{2 !} + \dots + \frac {z ^ {n}}{n !} + \dots , \tag {4}
$$

由于

$$
\lim _ {n \to \infty} \sqrt [ n ]{\left| c _ {n} \right|} = \lim _ {n \to \infty} \sqrt [ n ]{\frac {1}{n !}} = 0,
$$

故级数(4)的收敛半径 $R=+\infty$ ，即(4)在整个复平面上都是收敛的，当z为实变量x时，(4)的和函数为实变量的指数函数 $e^{x}$ 。因此，我们也把级数(4)的和函数定义为复变量z的指数函数 $e^{z}$ ，即

$$
\mathrm{e} ^ {z} = 1 + z + \frac {z ^ {2}}{2 !} + \dots + \frac {z ^ {n}}{n !} + \dots . \tag {5}
$$

用同样的方法可定义复变量的正弦函数与余弦函数:

$$
\sin z = z - \frac {z ^ {3}}{3 !} + \frac {z ^ {5}}{5 !} + \dots + (- 1) ^ {n - 1} \frac {z ^ {2 n - 1}}{(2 n - 1) !} + \dots , \tag {6}
$$

$$
\cos z = 1 - \frac {z ^ {2}}{2 !} + \frac {z ^ {4}}{4 !} + \dots + (- 1) ^ {n} \frac {z ^ {2 n}}{(2 n) !} + \dots . \tag {7}
$$

它们的收敛域都是整个复平面.

以 $iz$ 代替(5)式中的 $z$, 可得

$$
\begin{array}{l} \mathrm{e} ^ {\mathrm{i} z} = 1 + \mathrm{i} z + \frac {(\mathrm{i} z) ^ {2}}{2 !} + \dots + \frac {(\mathrm{i} z) ^ {n}}{n !} + \dots \\ = 1 + \mathrm{i} z - \frac {z ^ {2}}{2 !} - \mathrm{i} \frac {z ^ {3}}{3 !} + \frac {z ^ {4}}{4 !} + \mathrm{i} \frac {z ^ {5}}{5 !} + \dots \\ = \left(1 - \frac {z ^ {2}}{2 !} + \frac {z ^ {4}}{4 !} + \dots\right) + \mathrm{i} \left(z - \frac {z ^ {3}}{3 !} + \frac {z ^ {5}}{5 !} + \dots\right). \\ \end{array}
$$

联系(6)式与(7)式,就有

$$
\mathrm{e} ^ {\mathrm{i} z} = \cos z + \mathrm{i} \sin z.
$$

当 z 为实变量 x 时, 则得

$$
\mathrm{e} ^ {\mathrm{i} x} = \cos x + \mathrm{i} \sin x, - \infty <   x <   + \infty.
$$

它称为欧拉公式. 这个公式给出了(实变量)指数函数与三角函数之间的关系.

由于任一复数 z 都可写作  $r(\cos \theta + i \sin \theta)$  （r 为 z 的模，即  $|z| = r, \theta = \arg z$  为 z 的辐角），那么由欧拉公式可得复数的指数形式

$$
z = r (\cos \theta + \mathrm{i} \sin \theta) = r \mathrm{e} ^ {\mathrm{i} \theta}.
$$

与实幂级数一样,由级数的乘法运算可得

$$
\mathrm{e} ^ {z _ {1} + z _ {2}} = \mathrm{e} ^ {z _ {1}} \mathrm{e} ^ {z _ {2}}.
$$

将 $z = x + \mathrm{i}y$ 代入上式，则有

$$
\mathrm{e} ^ {z} = \mathrm{e} ^ {x + \mathrm{i} y} = \mathrm{e} ^ {x} \mathrm{e} ^ {\mathrm{i} y} = \mathrm{e} ^ {x} (\cos y + \mathrm{i} \sin y).
$$

## 习题 14.3

1. 证明棣莫弗 (de Moivre) 公式

$$
\cos n x + \mathrm{i} \sin n x = (\cos x + \mathrm{i} \sin x) ^ {n}.
$$

2. 应用欧拉公式与棣莫弗公式证明:

(1) $\mathrm{e}^{x\cos \alpha}\cos (x\sin \alpha) = \sum_{n = 0}^{\infty}\frac{x^n}{n!}\cos n\alpha ;$ (2) $\mathrm{e}^{x\cos \alpha}\sin (x\sin \alpha) = \sum_{n = 0}^{\infty}\frac{x^n}{n!}\sin n\alpha .$

## 第十四章总练习题

1. 证明: 当  $\left|x\right|<\frac{1}{2}$  时,

$$
\frac {1}{1 - 3 x + 2 x ^ {2}} = 1 + 3 x + 7 x ^ {2} + \dots + (2 ^ {n} - 1) x ^ {n - 1} + \dots .
$$

2. 求下列函数的幂级数展开式:

(1)  $f(x)=(1+x)\ln(1+x)$ ;

(2) $f(x)=\sin^{3}x;$

(3) $f(x) = \int_{0}^{x} \cos t^2 \, dt.$

3. 确定下列幂级数的收敛域,并求其和函数:

(1)  $\sum_{n=1}^{\infty} n^{2} x^{n-1}$ ;

(2) $\sum_{n=0}^{\infty} \frac{2n+1}{2^{n+1}} x^{2n}$;

(3)  $\sum_{n=1}^{\infty} n(x - 1)^{n-1}$ ;

(4) $\sum_{n=1}^{\infty}(-1)^{n-1}\frac{x^{2n+1}}{(2n)^2 - 1}.$

4. 应用幂级数性质求下列级数的和:

(1)  $\sum_{n=1}^{\infty}\frac{n}{(n+1)!};$

(2) $\sum_{n=0}^{\infty} \frac{(-1)^n}{3n+1}$.

5. 设函数

$$
f (x) = \sum_ {n = 1} ^ {\infty} \frac {x ^ {n}}{n ^ {2}}
$$

定义在 $[0,1]$ 上,证明它在 $(0,1)$ 上满足下述方程:

$$
f (x) + f (1 - x) + \ln x \ln (1 - x) = f (1).
$$

6. 利用函数的幂级数展开式求下列不定式极限:

(1)  $\lim_{x\to\infty}\left[x-x^{2}\ln\left(1+\frac{1}{x}\right)\right]$ ;

(2) $\lim_{x\to 0}\frac{x - \arcsin x}{\sin^3x}.$

![](images/page_66_image_21.jpg)

第十四章综合自测题

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

![](images/page_68_image_15.jpg)

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

推论 若 $f$ 是以 $2\pi$ 为周期的连续函数, 且在 $[- \pi, \pi]$ 上按段光滑, 则 $f$ 的傅里叶级数在 $(- \infty, + \infty)$ 上收敛于 $f$.

根据收敛定理的假设, $f$ 是以 $2\pi$ 为周期的函数,所以系数公式(10)中的积分区间 $[-π,π]$ 可以改为长度为 $2π$ 的任何区间,而不影响 $a_{n},b_{n}$ 的值:

![](images/page_71_chart_3.jpg)

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

![](images/page_71_chart_11.jpg)

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

![](images/page_71_chart_17.jpg)

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

![](images/page_72_chart_10.jpg)

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

![](images/page_73_image_1.jpg)

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

![](images/page_74_chart_11.jpg)

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

![](images/page_74_chart_20.jpg)

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

![](images/page_78_chart_11.jpg)

<details>
<summary>contour</summary>

| X | Y |
| --- | --- |
| \(-\pi\) | ~0.8 |
| 0 | 0 |
| \(\pi\) | ~0.8 |
</details>

(a) 偶式延拓

![](images/page_78_image_13.jpg)

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

![](images/page_79_image_1.jpg)

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

![](images/page_80_chart_9.jpg)

<details>
<summary>scatter</summary>

| X | Y |
| --- | --- |
| 0 | 1 |
| h | 0 |
| h | ~0.5 |
</details>

图15-10

![](images/page_80_chart_11.jpg)

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

![](images/page_81_chart_1.jpg)

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

证明: $\sum_{n = 1}^{\infty}a_n^2$ 收敛，且有不等式

$$
\sum_ {n = 1} ^ {\infty} a _ {n} ^ {2} \leqslant \int_ {a} ^ {b} \left[ f (x) \right] ^ {2} \mathrm{d} x.
$$

![](images/page_88_image_4.jpg)

## 第十五章综合自测题

## §1 平面点集与多元函数

多元函数是一元函数的推广,因此它保留着一元函数的许多性质,但也由于自变量由一个增加到多个,产生了某些新的性质,读者对这些性质尤其要加以注意.对于多元函数,我们将着重讨论二元函数.在掌握了二元函数的有关理论与研究方法之后,我们可以把它们推广到一般的多元函数中去.

一元函数的定义域是实数轴上的点集,二元函数的定义域将是坐标平面上的点集.因此,在讨论二元函数之前,有必要先了解有关平面点集的一些基本概念.

## 一、平面点集

由平面解析几何知道,当在平面上确定了一个坐标系(今后如不特别指出,都假定是直角坐标系)之后,所有有序实数对 $^{①}(x,y)$ 与平面上所有的点之间建立了一一对应.因此,今后将把“数对”与“平面上的点”这两种说法看作是完全等同的.这种确定了坐标系的平面,称为坐标平面.

坐标平面上满足某种条件 P 的点的集合称为平面点集, 并记作

$$
E = \{(x, y) \mid (x, y) \text {满足条件} P \}.
$$

例如,全平面上的点所组成的点集是

$$
\mathbf {R} ^ {2} = \{(x, y) | - \infty <   x <   + \infty , - \infty <   y <   + \infty \}. \tag {1}
$$

平面上以原点为中心、r 为半径的圆内所有的点的集合是

$$
C = \{(x, y) \mid x ^ {2} + y ^ {2} <   r ^ {2} \}. \tag {2}
$$

而集合

$$
S = \{(x, y) \mid a \leqslant x \leqslant b, c \leqslant y \leqslant d \} \tag {3}
$$

则为一矩形及其内部所有点的全体,为书写上的方便,也常把它记作 $[a,b]\times[c,d]^{②}$ .
平面点集

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 或简称“数对”.</span></small>

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">② 一般地，对于任意两个数集（或点集） $A, B$ ，记 $A \times B = \{(x, y) \mid x \in A, y \in B\}$，称为 $A$ 与 $B$ 的直积。例如 $A = \{(u, v) \mid u^2 + v^2 \leqslant 1\}, B = [0, 1]$，则 $A \times B = \{(u, v, w) \mid u^2 + v^2 \leqslant 1, 0 \leqslant w \leqslant 1\}$</span></small>

$$
\{(x, y) \mid (x - x _ {0}) ^ {2} + (y - y _ {0}) ^ {2} <   \delta^ {2} \}
$$

与

$$
\{(x, y) \mid | x - x _ {0} | <   \delta , | y - y _ {0} | <   \delta \}
$$

分别称为以点 $A(x_0,y_0)$ 为中心的 $\delta$ 圆邻域与 $\delta$ 方邻域（图16-1）.

![](images/page_90_image_5.jpg)

图16-1

由于点 $A$ 的任一个圆邻域总包含有点 $A$ 的某一个方邻域（反之亦然），因此通常用“点 $A$ 的 $\delta$ 邻域”或“点 $A$ 的邻域”泛指这两种形状的邻域，并以记号 $U(A; \delta)$ 或 $U(A)$ 来表示。点 $A$ 的空心邻域是指

$$
\{(x, y) \mid 0 <   (x - x _ {0}) ^ {2} + (y - y _ {0}) ^ {2} <   \delta^ {2} \}
$$

或 $\{(x,y)\mid |x - x_0| <   \delta ,|y - y_0| <   \delta ,(x,y)\neq (x_0,y_0)\}$

并用记号  $U^{\circ}(A;\delta)$  或  $U^{\circ}(A)$  来表示.

下面利用邻域来描述点和点集之间的关系.

任意一点  $A \in R^{2}$  与任意一个点集  $E \subset R^{2}$  之间必有以下三种关系之一:

(i) 内点——若存在点 $A$ 的某邻域 $U(A)$, 使得 $U(A) \subset E$, 则称点 $A$ 是点 $E$ 的内点. $E$ 的全体内点构成的集合称为 $E$ 的内部, 记作 $\operatorname{int} E$.
（ii）外点——若存在点 $A$ 的某邻域 $U(A)$，使得 $U(A) \cap E = \varnothing$，则称 $A$ 是点集 $E$ 的外点.
（iii）界点——若在点 A 的任何邻域内既含有属于 E 的点，又含有不属于 E 的点，则称 A 是集合 E 的界点。即对任何正数  $\delta$ ，恒有

$$
U (A; \delta) \cap E \neq \varnothing \text {且} U (A; \delta) \cap E ^ {c} \neq \varnothing ,
$$

其中 $E^{c} = \mathbf{R}^{2}\backslash E$ 是 $E$ 关于全平面的余集. $E$ 的全体界点构成 $E$ 的边界，记作 $\partial E$.

E 的内点必定属于 E, E 的外点必定不属于 E, E 的界点可能属于 E, 也可能不属于 E.

点 A 与点集 E 的上述关系是按“点 A 在 E 内或在 E 外”来区分的. 此外, 还可按在点 A 的近旁是否密集着 E 中无穷多个点而构成另一类关系:

(i) 聚点——若在点 A 的任何空心邻域  $U^{\circ}(A)$  内都含有 E 中的点，则称 A 是 E 的聚点，聚点本身可能属于 E，也可能不属于 E.

$A$ 是点集 $E$ 的聚点的定义等价于“点 $A$ 的任何邻域 $U(A)$ 包含有 $E$ 的无穷多个点”.

（ii）孤立点——若点 $A \in E$，但不是 $E$ 的聚点，即存在某一正数 $\delta$，使得 $U^{\circ}(A; \delta) \cap E = \varnothing$，则称点 $A$ 是 $E$ 的孤立点。

显然,孤立点一定是界点,内点和非孤立的界点一定是聚点,既不是聚点,又不是孤立点,则必为外点.

例1 设平面点集

$$
D = \{(x, y) \mid 1 \leqslant x ^ {2} + y ^ {2} <   4 \}. \tag {4}
$$

满足 $1 < x^{2} + y^{2} < 4$ 的一切点都是 $D$ 的内点，满足 $x^{2} + y^{2} = 1$ 的一切点是 $D$ 的界点，它们都属于 $D$ ，满足 $x^{2} + y^{2} = 4$ 的一切点也是 $D$ 的界点，但它们都不属于 $D$ ，点集 $D$ 连同它外圆边界上的一切点都是 $D$ 的聚点.

根据点集中所属点的特征,我们再来定义一些重要的平面点集.

开集——若平面点集所属的每一点都是 $E$ 的内点（即 $\operatorname{int} E = E$），则称 $E$ 为开集.

闭集——若平面点集 $E$ 的所有聚点都属于 $E$, 则称 $E$ 为闭集. 若点集 $E$ 没有聚点, 这时也称 $E$ 为闭集.

在前面列举的平面点集中，(2)所表示的点集 $C$ 是开集，(3)所表示的点集 $S$ 是闭集，(4)所表示的点集 $D$ 既非开集，又非闭集，而且(1)所表示的点集 $\mathbf{R}^2$ 既是开集又是闭集.此外，还约定空集 $\varnothing$ 既是开集又是闭集.可以证明，在一切平面点集中，只有 $\mathbf{R}^2$ 与 $\varnothing$ 是既开又闭的点集.

开域——若非空开集 E 具有连通性, 即 E 中任意两点之间都可用一条完全含于 E 的有限折线(由有限条直线段连接而成的折线)相连接, 则称 E 为开域(即开域就是非空连通开集).

闭域——开域连同其边界所成的点集称为闭域.

区域——开域、闭域,或者开域连同其一部分界点所成的点集,统称为区域.

在上述诸例中，(2)是开域，(3)是闭域，(1)既是开域又是闭域.

又如

$$
E = \{(x, y) \mid x y > 0 \} \tag {5}
$$

虽然是开集,但因Ⅰ、Ⅲ象限之间不具有连通性,所以它不是开域,也不是区域.

有界点集——对于平面点集 $E$ ，若存在某一正数 $r$ ，使得

$$
E \subset U (O; r),
$$

其中 O 是坐标原点(也可以是其他固定点), 则称 E 是有界点集. 否则就是无界点集. 上述(2)、(3)、(4)都是有界点集, (1)、(5)则是无界点集.

E 为有界点集的另一等价说法是: 存在矩形区域  $D = [a, b] \times [c, d] \supset E$ .

点集的有界性还可用点集的直径来反映,所谓点集 E 的直径,就是

$$
d (E) = \sup _ {P _ {1}, P _ {2} \in E} \rho (P _ {1}, P _ {2}),
$$

其中 $\rho(P_1, P_2)$ 表示 $P_1$ 与 $P_2$ 两点之间的距离，当 $P_1, P_2$ 的坐标分别为 $(x_1, y_1)$ 和 $(x_2, y_2)$ 时，则

$$
\rho (P _ {1}, P _ {2}) = \sqrt {(x _ {1} - x _ {2}) ^ {2} + (y _ {1} - y _ {2}) ^ {2}}.
$$

于是,当且仅当  $d(E)$  为有限值时 E 是有界点集.

根据距离概念,读者不难证明如下三角形不等式,即对  $R^{2}$  上任何三点  $P_{1}, P_{2}$  和  $P_{3}$ ,皆有

$$
\rho (P _ {1}, P _ {2}) \leqslant \rho (P _ {1}, P _ {3}) + \rho (P _ {2}, P _ {3}).
$$

例 2 证明: 对任何  $S \subset R^{2}$ ,  $\partial S$  恒为闭集.

证 如图16-2所示, 设 $x_0$ 为 $\partial S$ 的任一聚点, 要证 $x_0 \in \partial S$. 为此, 任给 $\varepsilon > 0$, 由聚点定义, 存在  $y \in U^{\circ}(x_{0}; \varepsilon) \cap \partial S$ . 又 y 是 S 的界点, 所以对任意  $U(y; \delta) \subset U(x_{0}; \varepsilon)$ ,  $U(y; \delta)$  上既有 S 的点, 又有非 S 的点. 于是  $U(x_{0}; \varepsilon)$  上也既有 S 的点, 又有非 S 的点, 由  $\varepsilon$  的任意性, 推知  $x_{0}$  是 S 的界点, 即  $x_{0} \in \partial S$ , 这就证明了  $\partial S$  是闭集. ☐

## 二、$\mathbf{R}^2$ 上的完备性定理

反映实数系完备性的几个等价定理,构成了一元函数极限理论的基础.现在把这些定理推广到  $R^{2}$ , 它们同

![](images/page_92_image_4.jpg)

<details>
<summary>text_image</summary>

U°(x₀;ε)
x₀
y
U(y;δ)
∂S
</details>

图16-2

样是二元函数极限理论的基础. 为此, 先给出平面点列的收敛性概念.

定义1 设 $\{P_n\} \subset \mathbf{R}^2$ 为平面点列, $P_0 \in \mathbf{R}^2$ 为一固定点. 若对任给的正数 $\varepsilon$, 存在正整数 $N$, 使得当 $n > N$ 时, 有 $P_n \in U(P_0; \varepsilon)$, 则称点列 $\{P_n\}$ 收敛于点 $P_0$, 记作

$$
\lim _ {n \to \infty} P _ {n} = P _ {0} \quad \text {或} \quad P _ {n} \to P _ {0}, n \to \infty .
$$

在坐标平面中，以 $(x_{n},y_{n})$ 与 $(x_0,y_0)$ 分别表示 $P_{n}$ 与 $P_{0}$ 时， $\lim_{n\to \infty}P_n = P_0$ 显然等价于$\lim_{n\to \infty}x_n = x_0,\lim_{n\to \infty}y_n = y_0.$ 同样地，当以 $\rho_{n} = \rho (P_{n},P_{0})$ 表示点 $P_{n}$ 与 $P_{0}$ 之间距离时， $\lim_{\bar{n}\to \infty}P_n =$ $P_{0}$ 也就等价于 $\lim_{n\to \infty}\rho_n = 0.$ 由于点列极限这两种等价形式都是数列极限，因此立即得到下述关于平面点列的收敛原理.

定理 16.1(柯西准则) 平面点列  $\{P_{n}\}$  收敛的充要条件是: 任给正数  $\varepsilon$ , 存在正整数 N, 使得当 n > N 时, 对一切正整数 p, 都有

$$
\rho (P _ {n}, P _ {n + p}) <   \varepsilon . \tag {6}
$$

证 [必要性] 设 $\lim_{n\to \infty}P_n = P_0$ ，则由三角形不等式

$$
\rho (P _ {n}, P _ {n + p}) \leqslant \rho (P _ {n}, P _ {0}) + \rho (P _ {n + p}, P _ {0})
$$

及点列收敛定义,对所给  $\varepsilon$ , 存在正整数 N, 当 n > N (也有  $n + p > N$ ) 时, 恒有

$$
\rho (P _ {n}, P _ {0}) <   \frac {\varepsilon}{2}, \quad \rho (P _ {n + p}, P _ {0}) <   \frac {\varepsilon}{2}.
$$

应用三角形不等式,立刻得到(6)式.

[充分性] 当(6)式成立时,则同时有

$$
\begin{array}{l} \mid x _ {n + p} - x _ {n} \mid \leqslant \rho (P _ {n}, P _ {n + p}) <   \varepsilon , \\ \mid y _ {n + p} - y _ {n} \mid \leqslant \rho (P _ {n}, P _ {n + p}) <   \varepsilon . \\ \end{array}
$$

这说明数列 $\{x_{n}\}$ 和 $\{y_{n}\}$ 都满足柯西收敛准则（定理2.11），所以它们都收敛.设 $\lim_{n\to \infty}x_n = x_0,\lim_{n\to \infty}y_n = y_0.$ 从而由点列收敛概念推得 $\{P_n\}$ 收敛于点 $P_0(x_0,y_0)$ （本节习题6）.

定理 16.2(闭域套定理) 设  $\{D_{n}\}$  是  $R^{2}$  中的闭域列, 它满足:

(i)  $D_{n} \supset D_{n+1}, n=1,2,\cdots;$
(ii)  $d_{n}=d(D_{n}),\lim_{n\to\infty}d_{n}=0,$

则存在惟一的点  $P_{0} \in D_{n}, n = 1, 2, \cdots$ .

证 任取点列 $P_{n} \in D_{n}, n = 1,2,\dots$. 由于 $D_{n+p} \subset D_{n}$, 因此 $P_{n}, P_{n+p} \in D_{n}$, 从而有 (图16-3)

$$
\rho (P _ {n}, P _ {n + p}) \leqslant d _ {n} \rightarrow 0, n \rightarrow \infty .
$$

由定理 16.1 知道存在  $P_{0} \in R^{2}$ ，使得

$$
\lim _ {n \to \infty} P _ {n} = P _ {0}.
$$

任意取定 n, 对任何正整数 p, 有

$$
P _ {n + p} \in D _ {n + p} \subset D _ {n}.
$$

再令 $p \to \infty$，由于 $D_{n}$ 是闭域，从而必定是闭集（本节习题4）。因此 $P_{0}$ 作为 $D_{n}$ 的聚点必定属于 $D_{n}$，即

$$
P _ {0} = \lim _ {p \to \infty} P _ {n + p} \in D _ {n}, n = 1, 2, \dots .
$$

最后证明  $P_{0}$  的惟一性. 若还有  $P_{0}^{\prime} \in D_{n}, n = 1, 2, \cdots$ , 则由

![](images/page_93_image_8.jpg)

<details>
<summary>text_image</summary>

y
Dₙ
Dₙ₊ₚ
Pₙ
Pₙ₊ₚ
O
x
</details>

图16-3

$$
\rho (P _ {0}, P _ {0} ^ {\prime}) \leqslant \rho (P _ {0}, P _ {n}) + \rho (P _ {0} ^ {\prime}, P _ {n}) \leqslant 2 d _ {n} \rightarrow 0, n \rightarrow \infty
$$

得到  $\rho(P_{0}, P_{0}^{\prime}) = 0$ ，即  $P_{0} = P_{0}^{\prime}$ .

闭域套定理显然是 R 中闭区间套定理(定理 7.1)的直接推广.

推论 对上述闭域套 $\{D_n\}$, 任给 $\varepsilon > 0$, 存在 $N \in \mathbf{N}_+$, 当 $n > N$ 时, 有 $D_n \subset U(P_0; \varepsilon)$.

另外, 把  $\{D_{n}\}$  改为闭集套时, 定理 16.2 仍然成立.

定理 16.3(聚点定理) 设  $E \subset R^{2}$  为有界无限点集, 则 E 在  $R^{2}$  中至少有一个聚点.

证 现用闭域套定理来证明. 由于 $E$ 是平面有界集合, 因此存在一个闭正方形 $D_{1}$ 包含它. 连接正方形对边中点, 把 $D_{1}$ 分成四个小的闭正方形, 则在这四个小闭正方形中, 至少有一个小闭正方形含有 $E$ 中无限多个点. 记这个小闭正方形为 $D_{2}$. 再对正方形 $D_{2}$ 如上法分成四个更小的闭正方形, 其中又至少有一个小闭正方形含有 $E$ 的无限多个点. 如此下去得到一个闭正方形序列 (图 16-4):

![](images/page_93_image_17.jpg)

<details>
<summary>text_image</summary>

D₁
E
</details>

图16-4

$$
D _ {1} \supset D _ {2} \supset D _ {3} \supset \dots .
$$

容易看到这个闭正方形序列 $\{D_{n}\}$ 的边长随着n趋向于无限而趋向于零.于是由闭域套定理,存在一点 $M_{0}\in D_{n},n=1,2,\cdots$ .

现在证明 $M_0$ 就是 $E$ 的聚点. 任取 $M_0$ 的 $\varepsilon$ 邻域 $U(M_0; \varepsilon)$, 当 $n$ 充分大之后, 正方形的边长可小于 $\varepsilon / 2$, 即有 $D_n \subset U(M_0; \varepsilon)$. 又由 $D_n$ 的取法知道 $U(M_0; \varepsilon)$ 中含有 $E$ 的无限多个点, 这就表明 $M_0$ 是 $E$ 的聚点.

与一元情形类似,定理 16.3 与定理 16.3'等价.

定理 16.3' 有界无限点列  $\{P_{n}\} \subset R^{2}$  必存在收敛子列  $\{P_{n_{k}}\}$ .

证明留给读者.

定理 16.4(有限覆盖定理) 设  $D \subset R^{2}$  为一有界闭域,  $\{\Delta_{\alpha}\}$  为一开域族, 它覆盖了 D (即  $D \subset \bigcup_{\alpha} \Delta_{\alpha}$ ), 则在  $\{\Delta_{\alpha}\}$  中必存在有限个开域  $\Delta_{1}, \Delta_{2}, \cdots, \Delta_{n}$ , 它们同样覆盖了 D (即  $D \subset \bigcup_{i=1}^{n} \Delta_{i}$ ).

本定理的证明与 R 中的有限覆盖定理(定理 7.3)相仿,在此从略.

在更一般的情况下,可将定理16.4中的D改设为有界闭集,而 $\Delta_{\alpha}\subset R^{2}$ 为一族开

集,此时定理结论依然成立.

## 三、二元函数

函数(或映射)是两个集合之间的一种确定的对应关系. R 到 R 的映射是一元函数, 而  $R^{2}$  到 R 的映射是二元函数.

定义2 设平面点集 $D \subset \mathbb{R}^2$，若按照某对应法则 $f, D$ 中每一点 $P(x, y)$ 都有惟一确定的实数 $z$ 与之对应，则称 $f$ 为定义在 $D$ 上的二元函数（或称 $f$ 为 $D$ 到 $\mathbf{R}$ 的一个映射），记作

$$
\begin{array}{c}f: D \rightarrow \mathbf {R},\\P \longmapsto z,\end{array}\tag {7}
$$

且称 $D$ 为 $f$ 的定义域. $P \in D$ 所对应的 $z$ 为 $f$ 在点 $P$ 的函数值, 记作 $z = f(P)$ 或 $z = f(x, y)$. 全体函数值的集合为 $f$ 的值域, 记作 $f(D) \subset \mathbf{R}$. 通常还把 $P$ 的坐标 $x$ 与 $y$ 称为 $f$ 的自变量, 而把 $z$ 称为因变量.

在映射意义下,上述  $z=f(P)$  称为 P 的象,P 称为 z 的原象.当把  $(x,y)\in D$  和它所对应的象  $z=f(x,y)$  一起组成三维数组  $(x,y,z)$  时,三维欧氏空间  $R^{3}$  中的点集

$$
S = \{(x, y, z) \mid z = f (x, y), (x, y) \in D \} \subset \mathbf {R} ^ {3}
$$

便是二元函数 $f$ 的图像. 通常 $z = f(x, y)$ 的图像是一空间曲面, $f$ 的定义域 $D$ 便是该曲面在 $xOy$ 平面上的投影.

为方便起见,由(7)式所确定的二元函数也记作

$$
z = f (x, y), \quad (x, y) \in D
$$

或 $z = f(P),\quad P\in D,$

且当它的定义域 $D$ 不会被误解的情况下，也简单地说“函数 $z = f(x,y)$”或“函数 $f$ ”.

例3 函数 $z = 2x + 5y$ 的图像是 $\mathbf{R}^3$ 中一个平面，其定义域是 $\mathbf{R}^2$ ，值域是 $\mathbf{R}$ □

例4 函数 $z = \sqrt{1 - (x^2 + y^2)}$ 的定义域是 $xOy$ 平面上的单位圆域 $\{(x, y) | x^2 + y^2 \leqslant 1\}$, 值域为区间 $[0, 1]$, 它的图像是以原点为中心的单位球面的上半部分（图16-5）.

例 5 z=xy 是定义在整个 xOy 平面上的函数, 它的图像是过原点的双曲抛物面 (图 16-6).

![](images/page_94_image_17.jpg)

<details>
<summary>text_image</summary>

z
y
O
x
</details>

图16-5

![](images/page_94_image_19.jpg)

<details>
<summary>text_image</summary>

z
y
O
x
</details>

图16-6

例6 $z = \left[\sqrt{x^2 + y^2}\right]$ 是定义在 $\mathbf{R}^2$ 上的函数，值域是全体非负整数，它的图形如图

16-7 所示.

若二元函数的值域是有界数集,则称该函数为有界函数,如例4中的函数;若值域是无界数集,则称该函数为无界函数,如例3、例5、例6中的函数.

与一元函数相类似，$f$ 在 $D$ 上无界的充要条件是存在 $\{P_k\} \subset D$，使 $\lim_{k\to \infty}f(P_k) = \infty$，这里 $D\subset \mathbf{R}^2$.

## 四、$n$ 元函数

![](images/page_95_image_5.jpg)

<details>
<summary>text_image</summary>

z
2
O
y
x
</details>

图16-7

所有有序实数组 $(x_{1},x_{2},\cdots,x_{n})$ 的全体称为n维向量

空间,简称 n 维空间,记作  $R^{n}$ . 其中每个有序实数组  $(x_{1}, x_{2}, \cdots, x_{n})$  称为  $R^{n}$  中的一个点, n 个实数  $x_{1}, x_{2}, \cdots, x_{n}$  是这个点的坐标.

设 E 为  $R^{n}$  中的点集, 若有某个对应法则 f, 使 E 中每一点  $P(x_{1}, x_{2}, \cdots, x_{n})$  都有惟一的一个实数 y 与之对应, 则称 f 为定义在 E 上的 n 元函数 (或称 f 为  $E \subset R^{n}$  到 R 的一个映射), 记作

$$
f \colon E \to \mathbf {R},
$$

$$
(x _ {1}, x _ {2}, \dots , x _ {n}) \mapsto y. \tag {8}
$$

也常把 $n$ 元函数简写成

$$
y = f (x _ {1}, x _ {2}, \dots , x _ {n}), \quad (x _ {1}, x _ {2}, \dots , x _ {n}) \in E
$$

或

$$
y = f (P), \quad P \in E. \tag {9}
$$

对于后一种被称为“点函数”的写法,它可使多元函数与一元函数在形式上尽量保持一致,以便仿照一元函数的办法来处理多元函数中的许多问题,同时还可把二元函数的某些论断推广到  $n(\geqslant3)$  元函数.

## 习题 16.1

1. 判断下列平面点集中哪些是开集、闭集、有界集、区域，并分别指出它们的聚点与界点:

(1) $[a, b) \times [c, d)$;

(2)  $\{(x,y) | xy \neq 0\}$ ;

(3)  $\{(x,y) \mid xy = 0\}$ ;

(4) $\{(x, y) | y > x^2\}$;

(5)  $\{(x,y)\mid x<2,y<2,x+y>2\}$ ;

(6)  $\{(x,y)\mid x^{2}+y^{2}=1 \text{ 或 } y=0,0\leqslant x\leqslant1\}$ ;

(7)  $\{(x,y)\mid x^{2}+y^{2}\leqslant1$  或  $y=0,1\leqslant x\leqslant2\}$ ;

(8) $\{(x,y)\mid x,y\text{均为整数}\}$ ;

(9)  $\{(x,y)\mid y=\sin\frac{1}{x},x>0\}$ .

2. 试问集合 $\{(x, y) \mid 0 < |x - a| < \delta, 0 < |y - b| < \delta\}$ 与集合 $\{(x, y) \mid |x - a| < \delta, |y - b| < \delta, (x, y) \neq (a, b)\}$ 是否相同？

3. 证明: 当且仅当存在各点互不相同的点列  $\{P_{n}\} \subset E, P_{n} \neq P_{0}, \lim_{n \to \infty} P_{n} = P_{0}$  时,  $P_{0}$  是 E 的聚点.

4. 证明: 闭域必为闭集. 举例说明反之不真.

5. 对任何点集  $S \subset R^{2}$ ，导集  $S^{d}$  亦为闭集.

6. 证明: 点列  $\left\{P_{n}(x_{n},y_{n})\right\}$  收敛于  $P_{0}(x_{0},y_{0})$  的充要条件是  $\lim_{n\to\infty}x_{n}=x_{0}$  和  $\lim_{n\to\infty}y_{n}=y_{0}$ .