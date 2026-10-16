# 第14章 幂级数

原始 PDF 第 49–67 页。

## 第十四章幂级数

## §1 幂级数

本章将讨论由幂函数序列 $\{a_{n}(x - x_{0})^{n}\}$ 所产生的函数项级数

$$
\sum_ {n = 0} ^ {\infty} a _ {n} (x - x _ {0}) ^ {n} = a _ {0} + a _ {1} (x - x _ {0}) + a _ {2} (x - x _ {0}) ^ {2} + \dots + a _ {n} (x - x _ {0}) ^ {n} + \dots , \tag {1}
$$

它称为幂级数,是一类最简单的函数项级数,从某种意义上说,它也可以看作是多项式函数的延伸.幂级数在理论和实际上都有很多应用,特别在应用它表示函数方面,使我们对它的作用有许多新的认识.

下面将着重讨论 $x_0 = 0$ ，即

$$
\sum_ {n = 0} ^ {\infty} a _ {n} x ^ {n} = a _ {0} + a _ {1} x + a _ {2} x ^ {2} + \dots + a _ {n} x ^ {n} + \dots \tag {2}
$$

的情形,因为只要把(2)中的 x 换成  $x-x_{0}$ , 就得到(1).

## 一、幂级数的收敛区间

首先讨论幂级数(2)的收敛性问题. 显然任意一个幂级数(2)在 $x = 0$ 处总是收敛的. 除此之外, 它还在哪些点收敛? 我们有下面重要的定理.

定理14.1（阿贝尔定理）若幂级数(2)在 $x = \overline{x}\neq 0$ 处收敛，则对满足不等式 $|x|$ $< |\overline{x} |$ 的任何 $x$ ，幂级数(2)收敛而且绝对收敛；若幂级数(2)在 $x = \overline{x}$ 处发散，则对满足不等式 $|x| > |\overline{x} |$ 的任何 $x$ ，幂级数(2)发散.

证 设级数 $\sum_{n=0}^{\infty} a_n \bar{x}^n$ 收敛, 从而数列 $\{a_n \bar{x}^n\}$ 收敛于零且有界, 即存在某正数 $M$, 使得

$$
\mid a _ {n} \overline {{x}} ^ {n} \mid <   M \quad (n = 0, 1, 2, \dots).
$$

另一方面，对任意一个满足不等式 $|x| < |\bar{x}|$ 的 $x$ ，设

$$
r = \left| \frac {x}{\overline {{x}}} \right| <   1,
$$

则有

$$
\left| a _ {n} x ^ {n} \right| = \left| a _ {n} \bar {x} ^ {n} \cdot \frac {x ^ {n}}{\bar {x} ^ {n}} \right| = \left| a _ {n} \bar {x} ^ {n} \right| \cdot \left| \frac {x}{\bar {x}} \right| ^ {n} <   M r ^ {n}.
$$

41

---

第十四章 幂级数

由于级数 $\sum_{n=0}^{\infty} M r^{n}$ 收敛, 故幂级数(2) 当 $|x| < |\bar{x}|$ 时绝对收敛.

现在证明定理的第二部分. 设幂级数(2)在 $x = \bar{x}$ 处发散, 如果存在某一个 $x_0$, 它满足不等式 $|x_0| > |\bar{x}|$, 且使级数 $\sum_{n=0}^{\infty} a_n x_0^n$ 收敛. 则由定理第一部分知道, 幂级数(2)应在 $x = \bar{x}$ 处绝对收敛, 这与假设相矛盾, 所以对一切满足不等式 $|x| > |\bar{x}|$ 的 $x$, 幂级数(2)都发散.

由此定理知道:幂级数(2)的收敛域是以原点为中心的区间.若以2R表示区间的长度,则称R为幂级数的收敛半径.实际上,它就是使得幂级数(2)收敛的那些收敛点的绝对值的上确界.所以

当 $R = 0$ 时，幂级数(2)仅在 $x = 0$ 处收敛；

当 $R = +\infty$ 时，幂级数(2)在 $(-\infty, +\infty)$ 上收敛；

当 $0 < R < +\infty$ 时，幂级数(2)在 $(-R, R)$ 上收敛；对一切满足不等式 $|x| > R$ 的 $x$ ，幂级数(2)都发散；至于在 $x = \pm R$ 处，则幂级数(2)可能收敛也可能发散.

我们称 $(-R,R)$ 为幂级数(2)的收敛区间.

怎样求得幂级数(2)的收敛半径,有如下定理.

定理 14.2 对于幂级数(2)，若

$$
\lim _ {n \to \infty} \sqrt [ n ]{\left| a _ {n} \right|} = \rho , \tag {3}
$$

则当

(i)  $0 < \rho < +\infty$  时, 幂级数(2)的收敛半径  $R = \frac{1}{\rho}$ ;
(ii)  $\rho=0$  时, 幂级数(2)的收敛半径  $R=+\infty$ ;
(iii)  $\rho = +\infty$  时, 幂级数(2)的收敛半径 R = 0.

证 对于幂级数 $\sum_{n=0}^{\infty}\left|a_n x^n\right|$, 由于

$$
\lim _ {n \to \infty} \sqrt [ n ]{\left| a _ {n} x ^ {n} \right|} = \lim _ {n \to \infty} \sqrt [ n ]{\left| a _ {n} \right|} \left| x \right| = \rho \left| x \right|,
$$

根据级数的根式判别法，当 $\rho |x| < 1$ 时，$\sum_{n=0}^{\infty} |a_n x^n|$ 收敛；当 $\rho |x| > 1$ 时，$\sum_{n=0}^{\infty} |a_n x^n|$ 发散。于是当 $0 < \rho < +\infty$ 时，由 $\rho |x| < 1$ 得幂级数（2）的收敛半径 $R = \frac{1}{\rho}$。当 $\rho = 0$ 时，对任何 $x$ 皆有 $\rho |x| < 1$，所以 $R = +\infty$。当 $\rho = +\infty$ 时，则对除 $x = 0$ 外的任何 $x$ 皆有 $\rho |x| > 1$，所以 $R = 0$。

在第十二章 §2 第二段曾经指出: 若  $\lim_{n\to\infty}\frac{\left|a_{n+1}\right|}{\left|a_n\right|}=\rho$ ，则有  $\lim_{n\to\infty}\sqrt[n]{\left|a_n\right|}=\rho$ 。因此，我们也常用级数的比式判别法来推出幂级数(2)的收敛半径。

例1 考察级数 $\sum_{n=1}^{\infty} \frac{x^n}{n^2}$, 由于

$$
\frac {a _ {n + 1}}{a _ {n}} = \frac {n ^ {2}}{(n + 1) ^ {2}} \rightarrow 1 (n \rightarrow \infty),
$$

42

---

§ 1 幂级数

所以它的收敛半径 $R = 1$ ，即收敛区间为 $(-1,1)$ ；当 $x = \pm 1$ 时，有 $\left|\frac{(\pm 1)^n}{n^2}\right| = \frac{1}{n^2}$ ，由于级数 $\sum_{n=1}^{\infty} \frac{1}{n^2}$ 收敛，所以级数 $\sum_{n=1}^{\infty} \frac{x^n}{n^2}$ 在 $x = \pm 1$ 时也收敛. 于是这个级数的收敛域为 $[-1,1]$.

例2 考察级数

$$
x + \frac {x ^ {2}}{2} + \dots + \frac {x ^ {n}}{n} + \dots , \tag {4}
$$

由于

$$
R = \lim _ {n \to \infty} \frac {a _ {n}}{a _ {n + 1}} = \lim _ {n \to \infty} \frac {n + 1}{n} = 1,
$$

所以幂级数(4)的收敛区间是 $(-1,1)$ .但级数(4)当x=1时发散,x=-1时收敛,从而推得级数(4)的收敛域是半开区间 $[-1,1)$ .☐

照此方法,读者不难验证级数

$$
\sum_ {n = 0} ^ {\infty} \frac {x ^ {n}}{n !} \quad \text {与} \quad \sum_ {n = 0} ^ {\infty} n! x ^ {n}
$$

的收敛半径分别为  $R = +\infty$  与 R = 0.

定理 14.3(柯西-阿达马(Cauchy-Hadamard)定理) 对于幂级数(2)，设

$$
\rho = \varlimsup_ {n \to \infty} \sqrt [ n ]{\left| a _ {n} \right|}, \tag {5}
$$

则当

(i)  $0 < \rho < +\infty$  时, 收敛半径  $R = \frac{1}{\rho}$ ;
(ii)  $\rho=0$  时,  $R=+\infty$ ;
(iii)  $\rho = +\infty$  时, R = 0.

注意:由于上极限(5)总是存在的,因而任一幂级数总能由(5)式得到它的收敛半径.

定理 14.3 的证明与定理 14.2 相仿,读者可自行根据定理 12.8 推论 2 推出.

例3 考察级数

$$
1 + \frac {x}{3} + \frac {x ^ {2}}{2 ^ {2}} + \frac {x ^ {3}}{3 ^ {3}} + \frac {x ^ {4}}{2 ^ {4}} + \dots + \frac {x ^ {2 n - 1}}{3 ^ {2 n - 1}} + \frac {x ^ {2 n}}{2 ^ {2 n}} + \dots ,
$$

由于

$$
\overline {{\lim _ {n \to \infty}}} \sqrt [ n ]{a _ {n}} = \frac {1}{2},
$$

所以收敛半径 R=2。由于  $x=\pm2$  时，这两个数项级数都发散。故级数的收敛域为  $(-2,2)$ 。

例 4 求  $\sum_{n=1}^{\infty}\frac{x^{2n}}{n-3^{2n}}$  的收敛域.

解 这是一个缺项幂级数,可以用定理 14.3 求收敛半径,也可以用下面的方法来求.

因为当 $\lim_{n\to \infty}\sqrt[n]{\frac{x^{2n}}{|n - 3^{2n}|}} = \frac{1}{9}\lim_{n\to \infty}\sqrt[n]{\frac{x^{2n}}{1 - \frac{n}{3^{2n}}}} = \frac{x^2}{9} < 1$ ，即 $|x| < 3$ 时级数收敛，所以原级数的收敛半径为 $R = 3$ .又当 $x = \pm 3$ 时，相应的级数都是 $\sum_{n = 1}^{\infty}\frac{3^{2n}}{n - 3^{2n}}$ ，而 $\lim_{n\to \infty}\frac{3^{2n}}{n - 3^{2n}} = -1\neq 0,$

43

---

第十四章 幂级数

级数 $\sum_{n=1}^{\infty} \frac{3^{2n}}{n - 3^{2n}}$ 发散.因此原级数的收敛域为 $(-3,3)$.

下面讨论幂级数(2)的一致收敛性问题.

定理 14.4 若幂级数(2)的收敛半径为 R (>0)，则幂级数(2)在它的收敛区间  $(-R, R)$  内任一闭区间  $[a, b]$  上都一致收敛.

证 设 $\bar{x} = \max \{|a|, |b|\} \in (-R, R)$，那么对于 $[a, b]$ 上任一点 $x$，都有

$$
\mid a _ {n} x ^ {n} \mid \leqslant \mid a _ {n} \overline {{x}} ^ {n} \mid .
$$

由于级数(2)在点 $\bar{x}$ 绝对收敛,应用优级数判别法推得级数(2)在 $[a,b]$ 上一致收敛.

定理14.5 若幂级数(2)的收敛半径为 $R (>0)$，且在 $x = R$（或 $x = -R$）时收敛，则级数(2)在 $[0, R]$（或 $[-R, 0]$）上一致收敛。

证 设级数(2)在 x=R 时收敛,对于  $x \in [0, R]$  有

$$
\sum_ {n = 0} ^ {\infty} a _ {n} x ^ {n} = \sum_ {n = 0} ^ {\infty} a _ {n} R ^ {n} \left(\frac {x}{R}\right) ^ {n}.
$$

已知级数 $\sum_{n=0}^{\infty} a_n R^n$ 收敛, 函数列 $\left\{\left(\frac{x}{R}\right)^n\right\}$ 在 $[0, R]$ 上递减且一致有界, 即

$$
1 \geqslant \frac {x}{R} \geqslant \left(\frac {x}{R}\right) ^ {2} \geqslant \dots \geqslant \left(\frac {x}{R}\right) ^ {n} \geqslant \dots \geqslant 0.
$$

故由阿贝尔判别法(定理13.6)，级数(2)在 $[0,R]$ 上一致收敛.

关于一般幂级数(1)的收敛性问题,也可仿照上述的办法来确定它的收敛区间和收敛半径.

例5 考察级数

$$
\sum_ {n = 1} ^ {\infty} \frac {(x - 1) ^ {n}}{2 ^ {n} n} = \frac {x - 1}{2} + \frac {(x - 1) ^ {2}}{2 ^ {2} \cdot 2} + \dots + \frac {(x - 1) ^ {n}}{2 ^ {n} \cdot n} + \dots , \tag {6}
$$

由于

$$
\frac {\frac {1}{2 ^ {n + 1} (n + 1)}}{\frac {1}{2 ^ {n} \cdot n}} = \frac {n}{2 (n + 1)} \rightarrow \frac {1}{2} \quad (n \rightarrow \infty),
$$

因此级数(6)的收敛半径 R=2，因而它的收敛区间为  $\left|x-1\right|<2$ ，即  $(-1,3)$ 。当 x=-1 时，级数(6)为收敛级数

$$
\sum_ {n = 1} ^ {\infty} \frac {(- 2) ^ {n}}{2 ^ {n} \cdot n} = - 1 + \frac {1}{2} - \frac {1}{3} + \dots + (- 1) ^ {n} \frac {1}{n} + \dots ;
$$

当 $x = 3$ 时，级数(6)为发散级数

$$
\sum_ {n = 1} ^ {\infty} \frac {2 ^ {n}}{2 ^ {n} n} = \sum \frac {1}{n} = 1 + \frac {1}{2} + \frac {1}{3} + \dots + \frac {1}{n} + \dots .
$$

于是级数(6)的收敛域为[-1,3).

## 二、幂级数的性质

首先由定理13.12立刻可得

44

---

§ 1 幂级数

定理 14.6 （i）幂级数(2)的和函数是 $(-R,R)$ 上的连续函数；（ii）若幂级数(2)在收敛区间的左(右)端点上收敛，则其和函数也在这一端点上右(左)连续.

在讨论幂级数的逐项求导与逐项求积之前,先要确定幂级数(2)在收敛区间 $(-R,R)$ 上逐项求导与逐项求积后所得到的幂级数

$$
a _ {1} + 2 a _ {2} x + 3 a _ {3} x ^ {2} + \dots + n a _ {n} x ^ {n - 1} + \dots \tag {7}
$$

与

$$
a _ {0} x + \frac {a _ {1}}{2} x ^ {2} + \frac {a _ {2}}{3} x ^ {3} + \dots + \frac {a _ {n}}{n + 1} x ^ {n + 1} + \dots \tag {8}
$$

的收敛区间.

定理 14.7 幂级数(2)与幂级数(7)、(8)具有相同的收敛区间.

证 这里只要证明(2)与(7)具有相同的收敛区间就可以了,因为对(8)逐项求导就得到(2).

设 $x_0$ 为幂级数(2)在其收敛区间 $(-R,R)$ 内任一不为零的点.由阿贝尔定理（定理14.1）的证明知道，存在正数 $M$ 与 $r(r < 1)$，对一切正整数 $n$，都有

$$
\left| a _ {n} x _ {0} ^ {n} \right| <   M r ^ {n}.
$$

于是

$$
\mid n a _ {n} x _ {0} ^ {n - 1} \mid = \left| \frac {n}{x _ {0}} \right| \mid a _ {n} x _ {0} ^ {n} \mid <   \frac {M}{\mid x _ {0} \mid} n r ^ {n},
$$

由级数的比式判别法知道,级数  $\sum_{n=0}^{\infty}nr^{n}$  收敛.根据级数的比较原则及上述不等式,推知幂级数(7)在点  $x_{0}$  是绝对收敛的(当然也是收敛的!).由于  $x_{0}$  为  $(-R,R)$  上任一点,这就证得幂级数(7)在  $(-R,R)$  上收敛.

现在证明幂级数(7)对一切满足不等式 $|x| > R$ 的 $x$ 都不收敛.如若不然，幂级数(7)在点 $x_0(|x_0| > R)$ 收敛，则有一数 $\bar{x}$，使得 $|x_0| > |\bar{x}| > R$.由阿贝尔定理，幂级数(7)在 $x = \bar{x}$ 处绝对收敛.但是，取 $n\geqslant |\bar{x} |$ 时，就有

$$
\mid n a _ {n} \bar {x} ^ {n - 1} \mid = \frac {n}{\mid \bar {x} \mid} \mid a _ {n} \bar {x} ^ {n} \mid \geqslant \mid a _ {n} \bar {x} ^ {n} \mid ,
$$

由比较原则得幂级数(2)在 $x = \bar{x}$ 处绝对收敛.这与所设幂级数(2)的收敛区间为$(-R,R)$ 相矛盾.这就证明了幂级数(7)的收敛区间也是 $(-R,R)$.

定理14.8 设幂级数(2)在收敛区间 $(-R, R)$ 上的和函数为 $f$, 若 $x$ 为 $(-R, R)$ 上任意一点, 则

(i) $f$ 在点 $x$ 可导，且

$$
f ^ {\prime} (x) = \sum_ {n = 1} ^ {\infty} n a _ {n} x ^ {n - 1};
$$

(ii) $f$ 在0与 $x$ 之间的这个区间上可积，且

$$
\int_ {0} ^ {x} f (t) \mathrm{d} t = \sum_ {n = 0} ^ {\infty} \frac {a _ {n}}{n + 1} x ^ {n + 1}.
$$

定理 14.8 指出幂级数在收敛区间内可逐项求导与逐项求积.

证 由定理14.7知,级数(2),(7),(8)具有相同的收敛半径 $R$. 因此,对任意一点 $x \in (-R, R)$, 总存在正数 $r$, 使得 $|x| < r < R$, 根据定理14.4, 级数(2),(7)在 $[-r, r]$ 上一

45

---

第十四章 幂级数

致收敛. 再由第十三章 §2 的逐项求导与逐项求积定理, 就得到所要证明的结论 (i) 与 (ii).

由定理14.8的(i)可得:

推论1 记 $f$ 为幂级数(2)在收敛区间 $(-R, R)$ 上的和函数，则在 $(-R, R)$ 上 $f$ 具有任何阶导数，且可逐项求导任何次，即

$$
f ^ {\prime} (x) = a _ {1} + 2 a _ {2} x + 3 a _ {3} x ^ {2} + \dots + n a _ {n} x ^ {n - 1} + \dots ,
$$

$$
f ^ {\prime \prime} (x) = 2 a _ {2} + 3 \cdot 2 a _ {3} x + \dots + n (n - 1) a _ {n} x ^ {n - 2} + \dots ,
$$

... ... ... ... ... ... ...

$$
f ^ {(n)} (x) = n! a _ {n} + (n + 1) n (n - 1) \dots 2 a _ {n + 1} x + \dots ,
$$

......

推论2 记 $f$ 为幂级数(2)在点 $x = 0$ 某邻域上的和函数, 则幂级数(2)的系数与 $f$ 在 $x = 0$ 处的各阶导数有如下关系:

$$
a _ {0} = f (0), \quad a _ {n} = \frac {f ^ {(n)} (0)}{n !} (n = 1, 2, \dots).
$$

这个推论还表明,若幂级数(2)在 $(-R,R)$ 上有和函数f,则幂级数(2)由f在点x=0处的各阶导数所惟一确定.

## 三、幂级数的运算

在讨论幂级数的运算之前,先说明两个幂级数

$\sum_{n=0}^{\infty} a_n x^n = a_0 + a_1 x + \cdots + a_n x^n + \cdots$ (2)

$$
\sum_ {n = 0} ^ {\infty} b _ {n} x ^ {n} = b _ {0} + b _ {1} x + \dots + b _ {n} x ^ {n} + \dots \tag {9}
$$

相等的意义.

定义1 若幂级数(2)与(9)在点 $x = 0$ 的某邻域内有相同的和函数, 则称这两个幂级数在该邻域内相等.

定理 14.9 若幂级数(2)与(9)在点 x=0 的某邻域内相等, 则它们同次幂项的系数相等, 即

$$
a _ {n} = b _ {n} (n = 0, 1, 2, \dots).
$$

这个定理的结论可直接由定理14.8的推论2得到.

根据这个定理还可推得:若幂级数(2)的和函数为奇(偶)函数,则(2)式不出现偶(奇)次幂的项.

定理14.10 若幂级数(2)与(9)的收敛半径分别为 $R_{a}$ 和 $R_{b}$，则有

$$
\lambda \sum_ {n = 0} ^ {\infty} a _ {n} x ^ {n} = \sum_ {n = 0} ^ {\infty} \lambda a _ {n} x ^ {n}, | x | <   R _ {a},
$$

$$
\sum_ {n = 0} ^ {\infty} a _ {n} x ^ {n} \pm \sum_ {n = 0} ^ {\infty} b _ {n} x ^ {n} = \sum_ {n = 0} ^ {\infty} (a _ {n} \pm b _ {n}) x ^ {n}, | x | <   R,
$$

$$
\left(\sum_ {n = 0} ^ {\infty} a _ {n} x ^ {n}\right) \left(\sum_ {n = 0} ^ {\infty} b _ {n} x ^ {n}\right) = \sum_ {n = 0} ^ {\infty} c _ {n} x ^ {n}, | x | <   R,
$$

46

---

§ 1 幂级数

式中  $\lambda$  为常数,  $R = \min\left\{R_{a}, R_{b}\right\}$ ,  $c_{n} = \sum_{k=0}^{n} a_{k} b_{n-k}$ .

定理的证明可由数项级数的相应性质推出.

例6 几何级数在收敛域 $(-1,1)$ 上有

$$
f (x) = \frac {1}{1 - x} = 1 + x + x ^ {2} + \dots + x ^ {n} + \dots . \tag {10}
$$

对级数(10)在 $(-1,1)$ 上逐项求导得

$$
f ^ {\prime} (x) = \frac {1}{(1 - x) ^ {2}} = 1 + 2 x + 3 x ^ {2} + \dots + n x ^ {n - 1} + \dots , \tag {11}
$$

$$
f ^ {\prime \prime} (x) = \frac {2 !}{(1 - x) ^ {3}} = 2 + 3 \cdot 2 x + \dots + n (n - 1) x ^ {n - 2} + \dots . \tag {12}
$$

级数(10)在 $[0,x]$ (x<1)上逐项求积分可得

$$
\int_ {0} ^ {x} \frac {\mathrm{d} t}{1 - t} = \sum_ {n = 0} ^ {\infty} \int_ {0} ^ {x} t ^ {n} \mathrm{d} t,
$$

所以

$$
\ln \frac {1}{1 - x} = x + \frac {x ^ {2}}{2} + \frac {x ^ {3}}{3} + \dots + \frac {x ^ {n + 1}}{n + 1} + \dots (\mid x \mid <   1). \tag {13}
$$

上式对 x = -1 也成立(参见本节习题 3).

从这个例子可以看到:由已知级数(10)的和函数,通过逐项求导或逐项求积可间接地求得级数(11)、(12)或(13)的和函数.

例7 求级数 $\sum_{n=1}^{\infty}(-1)^{n-1}n^2 x^n$ 的和函数.

解 易知级数的收敛域为 $(-1,1)$ . 下面利用逐项求积分的方法来求级数的和函数. 设

$$
S (x) = \sum_ {n = 1} ^ {\infty} (- 1) ^ {n - 1} n ^ {2} x ^ {n} = x \sum_ {n = 1} ^ {\infty} (- 1) ^ {n - 1} n ^ {2} x ^ {n - 1} = x \cdot g (x), x \in (- 1, 1).
$$

对 $g(x) = \sum_{n=1}^{\infty} (-1)^{n-1} n^2 x^{n-1}$ 积分, 得

$$
\int_ {0} ^ {x} g (t) \mathrm{d} t = \sum_ {n = 1} ^ {\infty} (- 1) ^ {n - 1} n ^ {2} \int_ {0} ^ {x} t ^ {n - 1} \mathrm{d} t = \sum_ {n = 1} ^ {\infty} (- 1) ^ {n - 1} n x ^ {n} = x \sum_ {n = 1} ^ {\infty} (- 1) ^ {n - 1} n x ^ {n - 1} = x h (x).
$$

再对  $h(x)$  积分, 得

$$
\int_ {0} ^ {x} h (t) \mathrm{d} t = \sum_ {n = 1} ^ {\infty} (- 1) ^ {n - 1} n \int_ {0} ^ {x} t ^ {n - 1} \mathrm{d} t = \sum_ {n = 1} ^ {\infty} (- 1) ^ {n - 1} x ^ {n} = \frac {x}{1 + x}, x \in (- 1, 1).
$$

因此，

$$
h (x) = \left(\frac {x}{1 + x}\right) ^ {\prime} = \frac {1}{(1 + x) ^ {2}},
$$

$$
g (x) = (x h (x)) ^ {\prime} = \left[ \frac {x}{(1 + x) ^ {2}} \right] ^ {\prime} = \frac {1 - x}{(1 + x) ^ {3}},
$$

$$
S (x) = x g (x) = \frac {x - x ^ {2}}{(1 + x) ^ {3}} \quad x \in (- 1, 1).
$$

47

---

第十四章 幂级数

## 习题 14.1

1. 求下列幂级数的收敛半径与收敛区域:

(1) $\sum_{n=1}^{\infty} nx^{n}$;

(2) $\sum_{n=1}^{\infty} \frac{x^n}{n^2 \cdot 2^n}$;

(3) $\sum_{n=0}^{\infty} \frac{(n!)^{2}}{(2n)!} x^{n}$;

(4)  $\sum_{n=0}^{\infty} r^{n^{2}} x^{n} \quad (0 < r < 1)$ ;

(5)  $\sum_{n=1}^{\infty}\frac{(x-2)^{2n-1}}{(2n-1)!};$

(6) $\sum_{n=1}^{\infty} \frac{3^n + (-2)^n}{n} (x+1)^n$;

(7)  $\sum_{n=1}^{\infty}\left(1+\frac{1}{2}+\cdots+\frac{1}{n}\right)x^{n};$

(8) $\sum_{n=0}^{\infty} \frac{x^{n^2}}{2^n}$.

2. 应用逐项求导或逐项求积方法求下列幂级数的和函数(应同时指出它们的定义域):

(1)  $x+\frac{x^{3}}{3}+\frac{x^{5}}{5}+\cdots+\frac{x^{2n+1}}{2n+1}+\cdots;$

(2) $1 \cdot 2x + 2 \cdot 3x^{2} + \cdots + n (n + 1)x^{n} + \cdots$;

(3) $\sum_{n=1}^{\infty} n^{2} x^{n}$.

3. 证明:设 $f(x) = \sum_{n=0}^{\infty} a_n x^n$ 当 $|x| < R$ 时收敛，若 $\sum_{n=0}^{\infty} \frac{a_n}{n+1} R^{n+1}$ 也收敛，则

$$
\int_ {0} ^ {R} f (x) \mathrm{d} x = \sum_ {n = 0} ^ {\infty} \frac {a _ {n}}{n + 1} R ^ {n + 1}
$$

(注意:这里不管  $\sum_{n=0}^{\infty}a_{n}x^{n}$  在 x = R 是否收敛). 应用这个结果证明:

$$
\int_ {0} ^ {1} \frac {1}{1 + x} \mathrm{d} x = \ln 2 = \sum_ {n = 1} ^ {\infty} (- 1) ^ {n - 1} \frac {1}{n}.
$$

4. 证明:

(1) $y = \sum_{n=0}^{\infty} \frac{x^{4n}}{(4n)!}$ 满足方程 $y^{(4)} = y$;
(2) $y = \sum_{n=0}^{\infty} \frac{x^n}{(n!)^2}$ 满足方程 $xy'' + y' - y = 0$.

5. 证明: 设 f 为幂级数(2)在 $(-R,R)$ 上的和函数, 若 f 为奇函数, 则级数(2)仅出现奇次幂的项, 若 f 为偶函数, 则(2)仅出现偶次幂的项.

6. 证明: 若 $\sum_{n=0}^{\infty} a_n x^n$ 的收敛半径是 $R(0 < R < +\infty)$, 则 $\sum_{n=0}^{\infty} a_n x^{2n}$ 的收敛半径是 $\sqrt{R}$.

7. 设  $\sum_{n=0}^{\infty} a_{n} x^{n}$  的收敛半径是  $R(0 < R < +\infty)$ . 证明: 对给定的  $M > \frac{1}{R}$ , 存在 K > 0, 使得  $\left|a_{n}\right| \leqslant KM^{n}, \forall n = 1, 2, \cdots$ .

8. 求下列幂级数的收敛域:

(1) $\sum_{n=0}^{\infty} \frac{x^n}{a^n + b^n}\quad (a > 0, b > 0)$;

(2) $\sum_{n=0}^{\infty}\left(1 + \frac{1}{n}\right)^{n^2}x^n.$

9. 证明定理 14.3 并求下列幂级数的收敛半径:

(1)  $\sum_{n=1}^{\infty}\frac{\left[3+(-1)^{n}\right]^{n}}{n}x^{n};$

(2) $a + bx + ax^2 +bx^3 +\dots$ （ $0 <   a <   b$ ）.

48

---

§ 2 函数的幂级数展开

10. 求下列幂级数的收敛半径及其和函数:

(1)  $\sum_{n=1}^{\infty}\frac{x^{n}}{n(n+1)}$ ;

(2) $\sum_{n=1}^{\infty} \frac{x^n}{n(n+1)(n+2)}$;

(3) $\sum_{n=2}^{\infty} \frac{(n-1)^{2}}{n+1} x^{n}$ (提示: $(n-1)^{2} = [(n+1)-2]^{2} = (n+1)^{2}-4(n+1)+4$).

11. 设  $a_{0}, a_{1}, a_{2}, \cdots$  为等差数列 ( $a_{0} \neq 0$ ). 试求:

（1）幂级数  $\sum_{n=0}^{\infty}a_{n}x^{n}$  的收敛半径；（2）数项级数  $\sum_{n=0}^{\infty}\frac{a_{n}}{2^{n}}$  的和.

## § 2 函数的幂级数展开

## 一、泰勒级数

在第六章 §3 的泰勒定理中曾指出, 若函数 $f$ 在点 $x_0$ 的某邻域上存在直至 $n+1$ 阶的连续导数, 则

$$
\begin{array}{l} f (x) = f (x _ {0}) + f ^ {\prime} (x _ {0}) (x - x _ {0}) + \frac {f ^ {\prime \prime} (x _ {0})}{2 !} (x - x _ {0}) ^ {2} + \dots + \\ \frac {f ^ {(n)} (x _ {0})}{n !} (x - x _ {0}) ^ {n} + R _ {n} (x), \tag {1} \\ \end{array}
$$

这里 $R_{n}(x)$ 为拉格朗日型余项

$$
R _ {n} (x) = \frac {f ^ {(n + 1)} (\xi)}{(n + 1) !} (x - x _ {0}) ^ {n + 1}, \tag {2}
$$

其中  $\xi$  在 x 与  $x_{0}$  之间, 称(1)为 f 在  $x_{0}$  处的泰勒公式.

如果在(1)中抹去余项 $R_{n}(x)$ ，那么在点 $x_{0}$ 附近f可用(1)式右边的多项式来近似代替，如果函数f在 $x_{0}$ 处存在任意阶的导数，这时称级数

$$
\begin{array}{l} f (x _ {0}) + f ^ {\prime} (x _ {0}) (x - x _ {0}) + \frac {f ^ {\prime \prime} (x _ {0})}{2 !} (x - x _ {0}) ^ {2} + \dots + \\ \frac {f ^ {(n)} (x _ {0})}{n !} (x - x _ {0}) ^ {n} + \dots \tag {3} \\ \end{array}
$$

为函数 f 在  $x_{0}$  处的泰勒级数. 对于级数(3)是否能在点  $x_{0}$  附近确切地表达 f, 或说 f 在  $x_{0}$  处的泰勒级数在点  $x_{0}$  附近的和函数是否就是 f, 这就是本节所要讨论的问题.

先看一个例子.

例1 由于函数

$$
f (x) = \left\{ \begin{array}{l l} \mathrm{e} ^ {- \frac {1}{x ^ {2}}}, & x \neq 0, \\ 0, & x = 0 \end{array} \right.
$$

在 x=0 处的任何阶导数都等于 0（第六章 §4 第一段末尾），即

$$
f ^ {(n)} (0) = 0, \quad n = 1, 2, \dots ,
$$

因此 $f$ 在 $x = 0$ 处的泰勒级数为

49

---

第十四章 幂级数

$$
0 + 0 \cdot x + \frac {0}{2 !} x ^ {2} + \dots + \frac {0}{n !} x ^ {n} + \dots .
$$

显然它在 $(-∞,+∞)$ 上收敛,且其和函数 $S(x)=0$ .由此看到,对一切 $x≠0$ 都有 $f(x)≠S(x)$ .

这个例子说明,具有任意阶导数的函数,其泰勒级数并不都能收敛于该函数本身.下面定理指出:具备什么条件的函数f,它的泰勒级数才能收敛于f本身.

定理 14.11 设 f 在点  $x_{0}$  具有任意阶导数, 那么 f 在区间  $(x_{0}-r, x_{0}+r)$  上等于它的泰勒级数的和函数的充分必要条件是: 对一切满足不等式  $\left|x-x_{0}\right|<r$  的 x, 有

$$
\lim _ {n \to \infty} R _ {n} (x) = 0,
$$

这里  $R_{n}(x)$  是 f 在  $x_{0}$  处的泰勒公式余项.

读者可自行由第六章 §3 泰勒定理推出本定理的证明.

如果 f 能在点  $x_{0}$  的某邻域内等于其泰勒级数的和函数, 则称函数 f 在点  $x_{0}$  的这一邻域内可以展开成泰勒级数, 并称等式

$$
\begin{array}{l} f (x) = f (x _ {0}) + f ^ {\prime} (x _ {0}) (x - x _ {0}) + \frac {f ^ {\prime \prime} (x _ {0})}{2 !} (x - x _ {0}) ^ {2} + \dots + \\ \frac {f ^ {(n)} (x _ {0})}{n !} (x - x _ {0}) ^ {n} + \dots \tag {4} \\ \end{array}
$$

的右边为 f 在  $x_{0}$  处的泰勒展开式, 或称幂级数展开式.

由定理14.8之推论2已知:若f为幂级数 $\sum_{n=0}^{\infty}a_{n}x^{n}$ 在收敛区间 $(-R,R)$ 上的和函数,则 $\sum_{n=0}^{\infty}a_{n}x^{n}$ 就是f在 $(-R,R)$ 上的泰勒展开式,即幂级数展开式是惟一的.

在实际应用上,主要讨论函数在  $x_{0}=0$  处的展开式,这时(3)式可以写作

$$
f (0) + \frac {f ^ {\prime} (0)}{1 !} x + \frac {f ^ {\prime \prime} (0)}{2 !} x ^ {2} + \dots + \frac {f ^ {(n)} (0)}{n !} x ^ {n} + \dots ,
$$

称为 f 的麦克劳林级数.

从定理 14.11 知道,余项对确定函数能否展开为幂级数是极为重要的.为了便于下面的讨论,我们重新写出当  $x_{0}=0$  时的积分型余项、拉格朗日型余项和柯西型余项,它们分别是

$$
R _ {n} (x) = \frac {1}{n !} \int_ {0} ^ {x} f ^ {(n + 1)} (t) (x - t) ^ {n} \mathrm{d} t,
$$

$R_{n}(x)=\frac{1}{(n+1)!}f^{(n+1)}(\xi)x^{n+1},\quad\xi$  在0与x之间，

$$
R _ {n} (x) = \frac {1}{n !} f ^ {(n + 1)} (\theta x) (1 - \theta) ^ {n} x ^ {n + 1}, \quad 0 \leqslant \theta \leqslant 1.
$$

## 二、初等函数的幂级数展开式

例2 求 $k$ 次多项式函数

$$
f (x) = c _ {0} + c _ {1} x + c _ {2} x ^ {2} + \dots + c _ {k} x ^ {k}
$$

的展开式.

解 由于

50

---

§ 2 函数的幂级数展开

$$
f ^ {(n)} (0) = \left\{ \begin{array}{l l} n! c _ {n}, & n \leqslant k, \\ 0, & n > k, \end{array} \right.
$$

总有 $\lim_{n\to \infty}R_n(x) = 0.$ 因而

$$
\begin{array}{l} f (x) = f (0) + f ^ {\prime} (0) x + \frac {f ^ {\prime \prime} (0)}{2 !} x ^ {2} + \dots + \frac {f ^ {(k)} (0)}{k !} x ^ {k} \\ = c _ {0} + c _ {1} x + c _ {2} x ^ {2} + \dots + c _ {k} x ^ {k}, \\ \end{array}
$$

即多项式函数的幂级数展开式就是它本身.

![](../../raw/pages_0033-0064/images/page_58_image_5.jpg)

例 3 求函数  $f(x)=\mathrm{e}^{x}$  的展开式.

解 由于 $f^{(n)}(x) = \mathrm{e}^x, f^{(n)}(0) = 1 (n = 1,2,\dots)$. 所以 $f$ 的拉格朗日型余项为 $R_{n}(x) = \frac{\mathrm{e}^{\theta x}}{(n + 1)!} x^{n + 1} (0\leqslant \theta \leqslant 1)$. 显见

$$
\mid R _ {n} (x) \mid \leqslant \frac {\mathrm{e} ^ {\mid x \mid}}{(n + 1) !} \mid x \mid^ {n + 1}.
$$

它对任何实数 x, 都有

$$
\lim _ {n \to \infty} \frac {\mathrm{e} ^ {| x |}}{(n + 1) !} | x | ^ {n + 1} = 0.
$$

因而 $\lim_{n\to \infty}R_n(x) = 0.$ 由定理14.11得到

$$
\mathrm{e} ^ {x} = 1 + \frac {1}{1 !} x + \frac {1}{2 !} x ^ {2} + \dots + \frac {1}{n !} x ^ {n} + \dots , \quad x \in (- \infty , + \infty).
$$

![](../../raw/pages_0033-0064/images/page_58_image_13.jpg)

例 4 函数  $f(x)=\sin x$ . 由于

$$
f ^ {(n)} (x) = \sin \left(x + \frac {n \pi}{2}\right), \quad n = 1, 2, \dots .
$$

现在考察正弦函数的拉格朗日型余项 $R_{n}(x)$ ，由于

$$
\begin{array}{l} \mid R _ {n} (x) \mid = \left| \frac {\sin \left(\xi + (n + 1) \frac {\pi}{2}\right)}{(n + 1) !} x ^ {n + 1} \right| \\ \leqslant \frac {\mid x \mid^ {n + 1}}{(n + 1) !} \rightarrow 0 (n \rightarrow \infty), \\ \end{array}
$$

所以  $f(x)=\sin x$  在  $(-∞,+∞)$  上能展开为麦克劳林级数

$$
\sin x = x - \frac {x ^ {3}}{3 !} + \frac {x ^ {5}}{5 !} + \dots + (- 1) ^ {n + 1} \frac {x ^ {2 n - 1}}{(2 n - 1) !} + \dots .
$$

同样可证(或逐项求导)，在 $(-∞,+∞)$ 上有

$$
\cos x = 1 - \frac {x ^ {2}}{2 !} + \frac {x ^ {4}}{4 !} + \dots + (- 1) ^ {n} \frac {x ^ {2 n}}{(2 n) !} + \dots .
$$

![](../../raw/pages_0033-0064/images/page_58_image_22.jpg)

$\sin x$  的麦克劳林展开式的部分和逼近过程见图 14-1.

例5 函数 $f(x) = \ln (1 + x)$ 的各阶导数是

$$
f ^ {(n)} (x) = (- 1) ^ {n - 1} \frac {(n - 1) !}{(1 + x) ^ {n}}.
$$

从而

$$
f ^ {(n)} (0) = (- 1) ^ {n - 1} (n - 1)!,
$$

所以 $f$ 的麦克劳林级数是

51

---

第十四章 幂级数

![](../../raw/pages_0033-0064/images/page_59_chart_1.jpg)

<details>
<summary>line</summary>

| x | y (n=1) | y (n=2) | y (n=3) | y (n=4) | y (n=5) |
| --- | --- | --- | --- | --- | --- |
| 0 | 0 | — | — | — | — |
| \(\pi/2\) | ~0.9 | — | — | — | — |
| \(\pi\) | — | 0 | ~0.5 | — | — |
| \(3\pi/2\) | — | — | ~0.9 | — | — |
| \(5\pi/2\) | — | — | — | 0 | — |
| \(7\pi/2\) | — | — | — | — | 0 |
| \(2\pi\) | — | — | — | — | ~1.2 |
</details>

图14-1

$$
x - \frac {x ^ {2}}{2} + \frac {x ^ {3}}{3} - \frac {x ^ {4}}{4} + \dots + (- 1) ^ {n - 1} \frac {x ^ {n}}{n} + \dots , \tag {5}
$$

用比式判别法容易求得级数(5)的收敛半径 $R = 1$ ，且当 $x = 1$ 时收敛，当 $x = -1$ 时发散，故级数(5)的收敛域是 $(-1,1]$. 现在讨论在这收敛区间上它的余项的极限情形.

当 $0 \leqslant x \leqslant 1$ 时用拉格朗日型余项，有

$$
\begin{array}{l} \left| R _ {n} (x) \right| = \left| \frac {1}{(n + 1) !} (- 1) ^ {n} \frac {n !}{(1 + \xi) ^ {n + 1}} x ^ {n + 1} \right| \\ = \left| \frac {(- 1) ^ {n}}{n + 1} \left(\frac {x}{1 + \xi}\right) ^ {n + 1} \right| \\ \leqslant \frac {1}{n + 1} \rightarrow 0 (n \rightarrow \infty). \\ \end{array}
$$

对于-1<x<0的情形,拉格朗日型余项不易估计,改用柯西型余项.有

$$
\begin{array}{l} \mid R _ {n} (x) \mid = \left| \frac {1}{n !} (- 1) ^ {n} \frac {n !}{(1 + \theta x) ^ {n + 1}} (1 - \theta) ^ {n} x ^ {n + 1} \right| \\ = \frac {1}{1 + \theta x} \left(\frac {1 - \theta}{1 + \theta x}\right) ^ {n} | x | ^ {n + 1}, \quad 0 \leqslant \theta \leqslant 1. \\ \end{array}
$$

因为 $-1 < x < 0$ ，故有 $1 - \theta \leqslant 1 + \theta x.$ 即 $0 \leqslant \frac{1 - \theta}{1 + \theta x} \leqslant 1$ ，所以

$$
\mid R _ {n} (x) \mid \leqslant \frac {\mid x \mid^ {n + 1}}{1 - \mid x \mid} \rightarrow 0 (n \rightarrow \infty).
$$

这就证得在 $(-1,1]$ 上 $\ln(1+x)$ 等于其麦克劳林级数(5).

将(5)式中 x 换成 x-1 后就得到函数  $f(x)=\ln x$  在 x=1 处的泰勒展开式:

$$
\ln x = (x - 1) - \frac {(x - 1) ^ {2}}{2} + \frac {(x - 1) ^ {3}}{3} + \dots + (- 1) ^ {n - 1} \frac {(x - 1) ^ {n}}{n} + \dots .
$$

它的收敛域为 $(0,2]$ .

例 6 讨论二项式函数  $f(x)=(1+x)^{\alpha}$  的展开式.

当  $\alpha$  为正整数时,由二项式定理直接展开,就得到 f 的展开式,这已在前面例 2 中讨论过.

下面讨论  $\alpha$  不等于正整数时的情形, 这时

$$
\begin{array}{l} f ^ {(n)} (x) = \alpha (\alpha - 1) \dots (\alpha - n + 1) (1 + x) ^ {\alpha - n}, \quad n = 1, 2, \dots , \\ f ^ {(n)} (0) = \alpha (\alpha - 1) \dots (\alpha - n + 1), \quad n = 1, 2, \dots . \\ \end{array}
$$

于是 $f(x)$ 的麦克劳林级数是

52

---

§ 2 函数的幂级数展开

$$
1 + \alpha x + \frac {\alpha (\alpha - 1)}{2 !} x ^ {2} + \dots + \frac {\alpha (\alpha - 1) \cdots (\alpha - n + 1)}{n !} x ^ {n} + \dots . \tag {6}
$$

运用比式判别法,可得(6)的收敛半径 R=1. 下面来证明  $f(x)=(1+x)^{\alpha}$  的麦克劳林级数(6)在  $(-1,1)$  上收敛于  $(1+x)^{\alpha}$ . 这里同样可以用证明余项趋于零的方法来得到这个结论,但我们希望给读者提供另一种处理类似问题的方法.

设级数(6)的和函数是 $g(x)$ ，即

$$
g (x) = 1 + \alpha x + \frac {\alpha (\alpha - 1)}{2 !} x ^ {2} + \dots + \frac {\alpha (\alpha - 1) \cdots (\alpha - n + 1)}{n !} x ^ {n} + \dots , x \in (- 1, 1).
$$

从 $(1+x)((1+x)^{\alpha})'= \alpha(1+x)^{\alpha}$ 得到启发,对 $g(x)$ 逐项求导,得

$$
g ^ {\prime} (x) = \alpha \left[ 1 + \frac {(\alpha - 1)}{1} x + \frac {(\alpha - 1) (\alpha - 2)}{2 !} x ^ {2} + \dots + \frac {(\alpha - 1) \cdots (\alpha - n + 1)}{(n - 1) !} x ^ {n - 1} + \dots \right],
$$

两边同乘 $(1+x)$ ，则右边 $x^{n}$ 项的系数为

$$
\begin{array}{l} \frac {(\alpha - 1) \cdots (\alpha - n + 1)}{(n - 1) !} + \frac {(\alpha - 1) \cdots (\alpha - n)}{n !} = \frac {(\alpha - 1) \cdots (\alpha - n + 1)}{(n - 1) !} \left(1 + \frac {\alpha - n}{n}\right) \\ = \frac {\alpha (\alpha - 1) \cdots (\alpha - n + 1)}{n !} \quad (n = 1, 2, \dots), \\ \end{array}
$$

于是有

$$
(1 + x) g ^ {\prime} (x) = \alpha g (x), x \in (- 1, 1).
$$

令 $F(x) = \frac{g(x)}{(1 + x)^{\alpha}},$

则  $F(0)=g(0)=1$ ,

$$
F ^ {\prime} (x) = \frac {(1 + x) ^ {\alpha} g ^ {\prime} (x) - \alpha (1 + x) ^ {\alpha - 1} g (x)}{(1 + x) ^ {2 \alpha}} = \frac {(1 + x) g ^ {\prime} (x) - \alpha g (x)}{(1 + x) ^ {\alpha + 1}} = 0.
$$

从而 $F(x) = F(0) = 1, x \in (-1, 1)$，即

$$
g (x) = (1 + x) ^ {\alpha}, x \in (- 1, 1).
$$

所以在 $(-1,1)$ 上，

$$
(1 + x) ^ {\alpha} = 1 + \alpha x + \frac {\alpha (\alpha - 1)}{2 !} x ^ {2} + \dots + \frac {\alpha (\alpha - 1) \cdots (\alpha - n + 1)}{n !} x ^ {n} + \dots . \tag {7}
$$

对于收敛区间端点的情形,它与  $\alpha$  的取值有关,其结果如下(推导参见菲赫金哥尔茨著《微积分学教程》第二卷第二分册):

当  $\alpha \leqslant -1$  时, 收敛域为  $(-1, 1)$ ;

当 $-1<\alpha<0$ 时,收敛域为 $(-1,1]$ ;

当  $\alpha>0$  时, 收敛域为  $[-1,1]$ .

当(7)式中  $\alpha = -1$  时就得到

$$
\frac {1}{1 + x} = 1 - x + x ^ {2} + \dots + (- 1) ^ {n} x ^ {n} + \dots , \quad (- 1, 1). \tag {8}
$$

当  $\alpha = -\frac{1}{2}$  时得到

$$
\frac {1}{\sqrt {1 + x}} = 1 - \frac {1}{2} x + \frac {1 \cdot 3}{2 \cdot 4} x ^ {2} - \frac {1 \cdot 3 \cdot 5}{2 \cdot 4 \cdot 6} x ^ {3} + \dots , \quad (- 1, 1 ]. \tag {9}
$$

□

53

---

第十四章 幂级数

一般地说, 只有少数比较简单的函数, 其幂级数展开式能直接从定义出发, 并根据定理 14.11 求得. 更多的情况是从已知的展开式出发, 通过变量代换、四则运算或逐项求导、逐项求积等方法, 间接地求得函数的幂级数展开式.

例 7 将  $x^{2}$  与  $-x^{2}$  分别代入(8)式与(9)式, 可得

$$
\frac {1}{1 + x ^ {2}} = 1 - x ^ {2} + x ^ {4} + \dots + (- 1) ^ {n} x ^ {2 n} + \dots , \quad (- 1, 1), \tag {10}
$$

$$
\frac {1}{\sqrt {1 - x ^ {2}}} = 1 + \frac {1}{2} x ^ {2} + \frac {1 \cdot 3}{2 \cdot 4} x ^ {4} + \frac {1 \cdot 3 \cdot 5}{2 \cdot 4 \cdot 6} x ^ {6} + \dots , \quad (- 1, 1). \tag {11}
$$

对于(10)式、(11)式分别逐项求积可得函数  $\arctan x$  与  $\arcsin x$  的展开式:

$$
\begin{array}{l} \arctan x = \int_ {0} ^ {x} \frac {\mathrm{d} t}{1 + t ^ {2}} \\ = x - \frac {x ^ {3}}{3} + \frac {x ^ {5}}{5} + \dots + (- 1) ^ {n} \frac {x ^ {2 n + 1}}{2 n + 1} + \dots , [ - 1, 1 ], \\ \end{array}
$$

$$
\begin{array}{l} \arcsin x = \int_ {0} ^ {x} \frac {\mathrm{d} t}{\sqrt {1 - t ^ {2}}} \\ = x + \frac {1}{2} \frac {x ^ {3}}{3} + \frac {1 \cdot 3}{2 \cdot 4} \frac {x ^ {5}}{5} + \frac {1 \cdot 3 \cdot 5}{2 \cdot 4 \cdot 6} \frac {x ^ {7}}{7} + \dots , [ - 1, 1 ]. \\ \end{array}
$$

由此可见,熟悉某些初等函数的展开式,对于一些函数的幂级数展开是极为方便的.特别是前面介绍的例3至例7的结果,对于用间接方法求幂级数展开式特别有用.

例 8 求函数 $(1-x)\ln(1-x)$ 在 x=0 处的幂级数展开式.

解 利用 $\ln (1 + x) = \sum_{n=1}^{\infty} (-1)^{n-1} \frac{x^n}{n}$, 得

$$
\begin{array}{l} (1 - x) \ln (1 - x) = (1 - x) \left(- \sum_ {n = 1} ^ {\infty} \frac {x ^ {n}}{n}\right) = - \sum_ {n = 1} ^ {\infty} \frac {x ^ {n}}{n} + \sum_ {n = 1} ^ {\infty} \frac {x ^ {n + 1}}{n}\left. \right) \\ = - x - \sum_ {n = 2} ^ {\infty} \frac {x ^ {n}}{n} + \sum_ {n = 2} ^ {\infty} \frac {x ^ {n}}{n - 1} \\ = - x + \sum_ {n = 2} ^ {\infty} \frac {x ^ {n}}{n (n - 1)}, x \in (- 1, 1). \\ \end{array}
$$

$(1 - x)\ln (1 - x)$ 在 $x = -1$ 处连续，在 $x = 1$ 处没有定义，而级数 $\sum_{n=2}^{\infty}\frac{x^n}{n(n-1)}$ 的收敛域为 $[-1,1]$，所以

$$
(1 - x) \ln (1 - x) = - x + \sum_ {n = 2} ^ {\infty} \frac {x ^ {n}}{n (n - 1)}, \quad x \in [ - 1, 1).
$$

注 上式右边的幂级数在 $[-1,1]$ 上都收敛，且在x=1时收敛于0，而 $(1-x)\cdot\ln(1-x)$ 只是它在 $[-1,1)$ 上的和函数。所以可以进一步写成

$$
- x + \sum_ {n = 2} ^ {\infty} \frac {x ^ {n}}{n (n - 1)} = \left\{ \begin{array}{c c} (1 - x) \ln (1 - x), & x \in [ - 1, 1), \\ 0, & x = 1. \end{array} \right.
$$

用类似的方法可得

$$
\ln \frac {1 + x}{1 - x} = 2 \sum_ {n = 0} ^ {\infty} \frac {x ^ {2 n + 1}}{2 n + 1}, \quad x \in (- 1, 1). \tag {12}
$$

54

---

§ 2 函数的幂级数展开

例 9 计算 ln 2 的近似值,精确到 0.0001.

解 可以在展开式  $\ln(1+x)=\sum_{n=1}^{\infty}(-1)^{n-1}\frac{x^{n}}{n}$  中令 x=1，得  $\ln2=\sum_{n=1}^{\infty}\frac{(-1)^{n-1}}{n}$ ，这是一个交错级数，需要计算 1 万项的和才能达到 0.0001 的精度，收敛太慢！为此在 (12) 式中令  $\frac{1+x}{1-x}=2$ ，即  $x=\frac{1}{3}$  代入 (12) 式，有

$$
\ln 2 = 2 \left(\frac {1}{3} + \frac {1}{3} \cdot \frac {1}{3 ^ {3}} + \dots + \frac {1}{2 n + 1} \cdot \frac {1}{3 ^ {2 n + 1}} + \dots\right).
$$

估计余项如下:

$$
\begin{array}{l} 0 <   R _ {n} = 2 \bigg (\frac {1}{2 n + 1} \cdot \frac {1}{3 ^ {2 n + 1}} + \frac {1}{2 n + 3} \cdot \frac {1}{3 ^ {2 n + 3}} + \dots \bigg) \\ <   \frac {2}{(2 n + 1) \cdot 3 ^ {2 n + 1}} \left(1 + \frac {1}{3 ^ {2}} + \frac {1}{3 ^ {4}} + \dots\right) \\ = \frac {2}{(2 n + 1) \cdot 3 ^ {2 n + 1}} \cdot \frac {1}{1 - \frac {1}{3 ^ {2}}} = \frac {1}{4 (2 n + 1) \cdot 3 ^ {2 n - 1}}, \\ \end{array}
$$

取 $n = 4$ ，就有 $0 < R_{4} < \frac{1}{4 \cdot 9 \cdot 3^{7}} = \frac{1}{78732} < 0.0001.$ 因此得到

$$
\begin{array}{l} \ln 2 \approx 2 \left(\frac {1}{3} + \frac {1}{3} \cdot \frac {1}{3 ^ {3}} + \frac {1}{5} \cdot \frac {1}{3 ^ {5}} + \frac {1}{7} \cdot \frac {1}{3 ^ {7}}\right) \\ \approx 2 (0. 3 3 3 3 3 + 0. 0 1 2 3 5 + 0. 0 0 0 8 2 + 0. 0 0 0 0 7) \\ = 0. 6 9 3 1. \\ \end{array}
$$

作为本节的结束,最后举例说明怎样用幂级数形式表示某些非初等函数.在本章开头就已经提到幂级数的这种特有的功能.

例 10 用间接方法求非初等函数

$$
F (x) = \int_ {0} ^ {x} \mathrm{e} ^ {- t ^ {2}} \mathrm{d} t
$$

的幂级数展开式.

解 以 $-x^{2}$ 代替例3中 $e^{x}$ 展开式的x,得

$$
\begin{array}{l} \mathrm{e} ^ {- x ^ {2}} = 1 - \frac {x ^ {2}}{1 !} + \frac {x ^ {4}}{2 !} - \frac {x ^ {6}}{3 !} + \dots + \frac {(- 1) ^ {n} x ^ {2 n}}{n !} + \dots , \\ - \infty <   x <   + \infty. \\ \end{array}
$$

再逐项求积就得到 $F(x)$ 在 $(-\infty, +\infty)$ 上的展开式

$$
\begin{array}{l} F (x) = \int_ {0} ^ {x} \mathrm{e} ^ {- t ^ {2}} \mathrm{d} t \\ = x - \frac {1}{1 !} \frac {x ^ {3}}{3} + \frac {1}{2 !} \frac {x ^ {5}}{5} - \frac {1}{3 !} \frac {x ^ {7}}{7} + \dots + \frac {(- 1) ^ {n}}{n !} \frac {x ^ {2 n + 1}}{2 n + 1} + \dots . \\ \end{array}
$$

![](../../raw/pages_0033-0064/images/page_62_image_16.jpg)

用上述级数的部分和逐项逼近  $F(x)$  的过程, 如图 14-2 所示.

55

---

第十四章 幂级数

![](../../raw/pages_0033-0064/images/page_63_chart_1.jpg)

<details>
<summary>line</summary>

| Curve | Description |
| --- | --- |
| n=0 | Linear function passing through origin |
| n=1 | Non-linear curve passing through origin |
| n=3 | Non-linear curve passing through origin |
| n=5 | Non-linear curve passing through origin |
| y=F(x) | Function curve passing through origin |
</details>

图14-2

## 习题 14.2

1. 设函数 $f$ 在区间 $(a, b)$ 上的各阶导数一致有界，即存在正数 $M$ ，对一切 $x \in (a, b)$，有

$$
\left| f ^ {(n)} (x) \right| \leqslant M, \quad n = 1, 2, \dots .
$$

证明: 对  $(a, b)$  上任一点 x 与  $x_{0}$  有

$$
f (x) = \sum_ {n = 0} ^ {\infty} \frac {f ^ {(n)} (x _ {0})}{n !} (x - x _ {0}) ^ {n} \quad (f ^ {(0)} (x) = f (x), 0! = 1).
$$

2. 利用已知函数的幂级数展开式, 求下列函数在 x=0 处的幂级数展开式, 并确定它收敛于该函数的区间:

(1) $\mathrm{e}^{x^2}$;

(2) $\frac{x^{10}}{1 - x}$;

(3) $\frac{x}{\sqrt{1 - 2x}};$

(4) $\sin^2 x$;

(5) $\frac{\mathrm{e}^x}{1 - x}$;

(6) $\frac{x}{1 + x - 2x^2}$;

(7) $\int_{0}^{x}\frac{\sin t}{t}\mathrm{d}t;$

(8) $(1 + x)\mathrm{e}^{-x}$;

(9) $\ln \left(x + \sqrt{1 + x^2}\right)$.

3. 求下列函数在 $x = 1$ 处的泰勒展开式:

(1) $f(x) = 3 + 2x - 4x^{2} + 7x^{3}$;

(2) $f(x) = \frac{1}{x}$;

(3) $f(x) = \sqrt{x^3}$.

4. 求下列函数的麦克劳林级数展开式:

(1) $\frac{x}{(1 - x)(1 - x^2)}$;

(2) $x \arctan x - \ln \sqrt{1 + x^2}$.

5. 试将 $f(x) = \ln x$ 按 $\frac{x - 1}{x + 1}$ 的幂展开成幂级数.

56

由
这

---

\* §3 复变量的指数函数·欧拉公式

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

57

---

第十四章 幂级数

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

58

---

第十四章总练习题

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

![](../../raw/pages_0065-0096/images/page_66_image_21.jpg)

第十四章综合自测题

59
