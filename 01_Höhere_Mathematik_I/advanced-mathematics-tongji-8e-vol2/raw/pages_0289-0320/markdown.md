$$
\int_ {0} ^ {1} \frac {\sin x}{x} \mathrm{d} x \approx 1 - \frac {1}{3 \times 3 !} + \frac {1}{5 \times 5 !},
$$

算得

$$
\int_ {0} ^ {1} \frac {\sin x}{x} \mathrm{d} x \approx 0. 9 4 6 1.
$$

## 二、微分方程的幂级数解法

这里,我们简单介绍一阶微分方程和二阶齐次线性微分方程的幂级数解法.

为求一阶微分方程

$$
\frac {\mathrm{d} y}{\mathrm{d} x} = f (x, y) \tag {5-1}
$$

满足初值条件 $y\mid_{x = x_0} = y_0$ 的特解，如果其中函数 $f(x,y)$ 是 $(x - x_0),(y - y_0)$ 的多项式

$$
f (x, y) = a _ {0 0} + a _ {1 0} (x - x _ {0}) + a _ {0 1} (y - y _ {0}) + \dots + a _ {l m} (x - x _ {0}) ^ {l} (y - y _ {0}) ^ {m}.
$$

那么可以设所求特解可展开为 $x - x_0$ 的幂级数:

$$
y = y _ {0} + a _ {1} (x - x _ {0}) + a _ {2} (x - x _ {0}) ^ {2} + \dots + a _ {n} (x - x _ {0}) ^ {n} + \dots , \tag {5-2}
$$

其中 $a_1, a_2, \dots, a_n, \dots$ 是待定的系数. 把(5-2)代入(5-1)中, 便得一恒等式, 比较所得恒等式两端 $x - x_0$ 的同次幂的系数, 就可定出常数 $a_1, a_2, \dots$, 以这些常数为系数的级数(5-2)在其收敛区间内就是方程(5-1)满足初值条件 $y|_{x = x_0} = y_0$ 的特解.

例6 求方程 $\frac{\mathrm{dy}}{\mathrm{dx}} = -y - x$ 满足 $y|_{x=0} = 2$ 的特解.

解 这时, $x_{0}=0,y_{0}=2$ . 故设方程的特解为

$$
y = 2 + a _ {1} x + a _ {2} x ^ {2} + \dots + a _ {n} x ^ {n} + \dots .
$$

由此，得  $y' = a_{1} + 2a_{2}x + \cdots + na_{n}x^{n-1} + \cdots$

将 y 及  $y'$  的幂级数展开式代入方程, 得

$$
a _ {1} + 2 a _ {2} x + \dots + n a _ {n} x ^ {n - 1} + \dots = - 2 - (a _ {1} + 1) x - a _ {2} x ^ {2} - \dots - a _ {n} x ^ {n} - \dots .
$$

上式为恒等式, 比较上式两端 x 的同次幂的系数, 得

$$
a _ {1} = - 2, \quad 2 a _ {2} = - (a _ {1} + 1), \quad 3 a _ {3} = - a _ {2}, \quad \dots , \quad n a _ {n} = - a _ {n - 1}, \quad \dots .
$$

故 $a_1 = -2, a_2 = \frac{1}{2}, a_3 = -\frac{1}{3!}, \cdots$ 由数学归纳法可得

$$
a _ {n} = (- 1) ^ {n} \frac {1}{n !} \quad (n \geqslant 2).
$$

于是,得

$$
y = 2 - 2 x + \frac {1}{2 !} x ^ {2} - \frac {1}{3 !} x ^ {3} + \dots + (- 1) ^ {n} \frac {1}{n !} x ^ {n} + \dots
$$

$$
\begin{array}{l} = 1 - x + \left[ 1 - x + \frac {1}{2 !} x ^ {2} - \frac {1}{3 !} x ^ {3} + \dots + (- 1) ^ {n} \frac {1}{n !} x ^ {n} + \dots \right] \\ = 1 - x + \mathrm{e} ^ {- x}. \\ \end{array}
$$

这就是所求的特解.

事实上,所给方程是一阶线性的,容易求得它的通解为  $y = C e^{-x} + 1 - x$ , 由条件  $y \mid_{x=0} = 2$  确定常数 C = 1, 即得方程的特解  $y = e^{-x} + 1 - x$ .

关于二阶齐次线性方程

$$
y ^ {\prime \prime} + P (x) y ^ {\prime} + Q (x) y = 0 \tag {5-3}
$$

用幂级数求解的问题,我们先叙述一个定理:

定理 如果方程(5-3)中的系数 $P(x)$ 与 $Q(x)$ 可在 $-R < x < R$ 内展开为 $x$ 的幂级数, 那么在 $-R < x < R$ 内方程(5-3)必有形如

$$
y = \sum_ {n = 0} ^ {\infty} a _ {n} x ^ {n}
$$

的解.

这定理的证明从略.

例7 求微分方程

$$
y ^ {\prime \prime} - x y = 0
$$

满足初值条件

$$
y \mid_ {x = 0} = 0, \quad y ^ {\prime} \mid_ {x = 0} = 1
$$

的特解.

解 这里 $P(x) = 0, Q(x) = -x$ 在整个数轴上满足定理的条件. 因此所求的解可在整个数轴上展开成 $x$ 的幂级数

$$
y = a _ {0} + a _ {1} x + a _ {2} x ^ {2} + \dots + a _ {n} x ^ {n} + \dots = \sum_ {n = 0} ^ {\infty} a _ {n} x ^ {n}. \tag {5-4}
$$

由条件  $y|_{x=0}=0$  , 得  $a_{0}=0$ . 对级数 (5-4) 逐项求导, 有

$$
y ^ {\prime} = a _ {1} + 2 a _ {2} x + 3 a _ {3} x ^ {2} + \dots + n a _ {n} x ^ {n - 1} + \dots = \sum_ {n = 1} ^ {\infty} n a _ {n} x ^ {n - 1},
$$

由条件 $y^{\prime}|_{x = 0} = 1$ ，得 $a_1 = 1.$ 于是所求特解 $y$ 及 $y^{\prime}$ 的展开式成为

$$
y = x + a _ {2} x ^ {2} + a _ {3} x ^ {3} + \dots + a _ {n} x ^ {n} + \dots = x + \sum_ {n = 2} ^ {\infty} a _ {n} x ^ {n}, \tag {5-5}
$$

$$
y ^ {\prime} = 1 + 2 a _ {2} x + 3 a _ {3} x ^ {2} + \dots + n a _ {n} x ^ {n - 1} + \dots = 1 + \sum_ {n = 2} ^ {\infty} n a _ {n} x ^ {n - 1}. \tag {5-6}
$$

对级数(5-6)逐项求导,得

$$
y ^ {\prime \prime} = 2 a _ {2} + 3 \times 2 a _ {3} x + \dots + n (n - 1) a _ {n} x ^ {n - 2} + \dots = \sum_ {n = 2} ^ {\infty} n (n - 1) a _ {n} x ^ {n - 2}. \tag {5-7}
$$

把(5-5)和(5-7)代入所给方程,并按 $x$ 的升幂集项,得

$$
2 a _ {2} + 3 \times 2 a _ {3} x + (4 \times 3 a _ {4} - 1) x ^ {2} + (5 \times 4 a _ {5} - a _ {2}) x ^ {3} +
$$

$$
(6 \times 5 a _ {6} - a _ {3}) x ^ {4} + \dots + [ (n + 2) (n + 1) a _ {n + 2} - a _ {n - 1} ] x ^ {n} + \dots = 0.
$$

因为上式是恒等式,所以上式左端各项的系数必全为零,于是有

$$
a _ {2} = 0, \quad a _ {3} = 0, \quad a _ {4} = \frac {1}{4 \times 3}, \quad a _ {5} = 0, \quad a _ {6} = 0, \quad \dots ,
$$

一般地

$$
a _ {n + 2} = \frac {a _ {n - 1}}{(n + 2) (n + 1)} \quad (n = 3, 4, \dots).
$$

从这递推公式可以推得

$$
a _ {7} = \frac {a _ {4}}{7 \times 6} = \frac {1}{7 \times 6 \times 4 \times 3}, \quad a _ {8} = \frac {a _ {5}}{8 \times 7} = 0, \quad a _ {9} = \frac {a _ {6}}{9 \times 8} = 0,
$$

$$
a _ {1 0} = \frac {a _ {7}}{1 0 \times 9} = \frac {1}{1 0 \times 9 \times 7 \times 6 \times 4 \times 3}, \dots ,
$$

一般地

$$
a _ {3 m - 1} = a _ {3 m} = 0,
$$

$$
a _ {3 m + 1} = \frac {1}{(3 m + 1) \times (3 m) \times \cdots \times 7 \times 6 \times 4 \times 3} \quad (m = 1, 2, \dots).
$$

于是所求的特解为

$$
\begin{array}{l} y = x + \frac {x ^ {4}}{4 \times 3} + \frac {x ^ {7}}{7 \times 6 \times 4 \times 3} + \frac {x ^ {1 0}}{1 0 \times 9 \times 7 \times 6 \times 4 \times 3} + \dots + \\ \frac {x ^ {3 m + 1}}{(3 m + 1) \times (3 m) \times \cdots \times 1 0 \times 9 \times 7 \times 6 \times 4 \times 3} + \dots \\ \end{array}
$$

## 三、欧拉公式

设有复数项级数为

$$
(u _ {1} + v _ {1} \mathrm{i}) + (u _ {2} + v _ {2} \mathrm{i}) + \dots + (u _ {n} + v _ {n} \mathrm{i}) + \dots , \tag {5-8}
$$

其中  $u_{n}$  与  $v_{n}$  ( $n=1,2,3,\cdots$ ) 为实常数或实函数. 如果实部所成的级数

$$
u _ {1} + u _ {2} + \dots + u _ {n} + \dots \tag {5-9}
$$

收敛于和 u，并且虚部所成的级数

$$
v _ {1} + v _ {2} + \dots + v _ {n} + \dots \tag {5-10}
$$

收敛于和 v, 那么就说级数 (5-8) 收敛且其和为  $u + vi$ .

如果级数(5-8)各项的模所构成的级数

$$
\sqrt {u _ {1} ^ {2} + v _ {1} ^ {2}} + \sqrt {u _ {2} ^ {2} + v _ {2} ^ {2}} + \dots + \sqrt {u _ {n} ^ {2} + v _ {n} ^ {2}} + \dots
$$

收敛,那么称级数(5-8)绝对收敛.如果级数(5-8)绝对收敛,由于

$$
\mid u _ {n} \mid \leqslant \sqrt {u _ {n} ^ {2} + v _ {n} ^ {2}}, \mid v _ {n} \mid \leqslant \sqrt {u _ {n} ^ {2} + v _ {n} ^ {2}} \quad (n = 1, 2, 3, \dots),
$$

那么级数(5-9)与(5-10)绝对收敛,从而级数(5-8)收敛.

考察复数项级数

$$
1 + z + \frac {1}{2 !} z ^ {2} + \dots + \frac {1}{n !} z ^ {n} + \dots \quad (z = x + y i). \tag {5-11}
$$

可以证明级数(5-11)在整个复平面上是绝对收敛的.在 $x$ 轴上 $(z = x)$ 它表示指数函数$\mathrm{e}^x$ ，在整个复平面上我们用它来定义复变量指数函数，记作 $\mathbf{e}^z$ .于是 $\mathbf{e}^z$ 定义为

$$
\mathrm{e} ^ {z} = 1 + z + \frac {1}{2 !} z ^ {2} + \dots + \frac {1}{n !} z ^ {n} + \dots \quad (| z | <   \infty). \tag {5-12}
$$

当 x=0 时, z 为纯虚数 yi, (5-12) 式成为

$$
\begin{array}{l} \mathrm{e} ^ {y \mathrm{i}} = 1 + y \mathrm{i} + \frac {1}{2 !} (y \mathrm{i}) ^ {2} + \frac {1}{3 !} (y \mathrm{i}) ^ {3} + \dots + \frac {1}{n !} (y \mathrm{i}) ^ {n} + \dots \\ = 1 + y \mathrm{i} - \frac {1}{2 !} y ^ {2} - \frac {1}{3 !} y ^ {3} \mathrm{i} + \frac {1}{4 !} y ^ {4} + \frac {1}{5 !} y ^ {5} \mathrm{i} - \dots \\ = \left(1 - \frac {1}{2 !} y ^ {2} + \frac {1}{4 !} y ^ {4} - \dots\right) + \left(y - \frac {1}{3 !} y ^ {3} + \frac {1}{5 !} y ^ {5} - \dots\right) i \\ = \cos y + \mathrm{i} \sin y. \\ \end{array}
$$

把 y 换写为 x, 上式变为

$$
\mathrm{e} ^ {x \mathrm{i}} = \cos x + \mathrm{i} \sin x, \tag {5-13}
$$

这就是欧拉(Euler)公式.

应用公式(5-13)，复数z可以表示为指数形式:

$$
z = \rho (\cos \theta + \mathrm{i} \sin \theta) = \rho \mathrm{e} ^ {\mathrm{i} \theta}, \tag {5-14}
$$

其中  $\rho = |z|$  是 z 的模,  $\theta = \arg z$  是 z 的辐角(图 12-5).

在(5-13)式中把 $x$ 换成 $-x$, 又有

$$
\mathrm{e} ^ {- x \mathrm{i}} = \cos x - \mathrm{i} \sin x.
$$

把上式与(5-13)相加或相减,得

$$
\left\{ \begin{array}{l} \cos x = \frac {\mathrm{e} ^ {x \mathrm{i}} + \mathrm{e} ^ {- x \mathrm{i}}}{2}, \\ \sin x = \frac {\mathrm{e} ^ {x \mathrm{i}} - \mathrm{e} ^ {- x \mathrm{i}}}{2 \mathrm{i}}. \end{array} \right. \tag {5-15}
$$

这两个式子也叫做欧拉公式.(5-13)式或(5-15)式揭示了三角函数与复变量指数函数之间的一种联系.

最后,根据定义式(5-12),并利用幂级数的乘法,我们不难验证

$$
\mathrm{e} ^ {z _ {1} + z _ {2}} = \mathrm{e} ^ {z _ {1}} \cdot \mathrm{e} ^ {z _ {2}}.
$$

![](images/page_291_image_22.jpg)

<details>
<summary>text_image</summary>

y
z=x+yi
ρ
θ
O
x
x
</details>

图12-5

特殊地,取 $z_{1}$ 为实数 $x,z_{2}$ 为纯虚数yi,则有

$$
\mathrm{e} ^ {x + y \mathrm{i}} = \mathrm{e} ^ {x} \cdot \mathrm{e} ^ {y \mathrm{i}} = \mathrm{e} ^ {x} (\cos y + \mathrm{i} \sin y).
$$

这就是说,复变量指数函数  $e^{z}$  在  $z=x+yi$  处的值是模为  $e^{x}$ 、辐角为 y 的复数.

## 习题12-5

1. 利用函数的幂级数展开式求下列各数的近似值:

(1)  $\ln 3$  (误差不超过 0.0001); (2)  $\sqrt{e}$  (误差不超过 0.001);
(3)  $\sqrt[9]{522}$  (误差不超过0.00001); (4)  $\cos 2^{\circ}$  (误差不超过0.0001).

2. 利用被积函数的幂级数展开式求下列定积分的近似值:

(1) $\int_{0}^{0.5}\frac{1}{1 + x^4}\mathrm{d}x$ （误差不超过0.0001）； (2) $\int_0^{0.5}\frac{\arctan x}{x}\mathrm{d}x$ （误差不超过0.001）.

3. 试用幂级数求下列各微分方程的解:

(1)  $y' - xy - x = 1$ ;

(2) $y''+xy'+y=0;$

(3) $(1-x)y'=x^{2}-y.$

4. 试用幂级数求下列方程满足所给初值条件的特解:

(1) $y' = y^2 + x^3, y \mid_{x=0} = \frac{1}{2};$

(2) $(1-x)y'+y=1+x,y\mid_{x=0}=0.$

5. 验证函数  $y(x)=1+\frac{x^{3}}{3!}+\frac{x^{6}}{6!}+\cdots+\frac{x^{3n}}{(3n)!}+\cdots$  ( $-\infty<x<+\infty$ ) 满足微分方程  $y''+y'+y=e^{x}$ ，并利用此结果求幂级数  $\sum_{n=0}^{\infty}\frac{x^{3n}}{(3n)!}$  的和函数.

6. 利用欧拉公式将函数  $e^{x}\cos x$  展开成 x 的幂级数.

## \* 第六节 函数项级数的一致收敛性及一致收敛级数的基本性质

## 一、函数项级数的一致收敛性

我们知道,有限个连续函数的和仍然是连续函数,有限个函数的和的导数及积分也分别等于它们的导数及积分的和.但是对于无穷多个函数的和是否也具有这些性质呢?换句话说,无穷多个连续函数的和 $s(x)$ 是否仍然是连续函数?无穷多个函数的导数及积分的和是否仍然分别等于它们的和函数的导数及积分呢?我们曾经指出,对于幂级数来说,回答是肯定的.但是,对于一般的函数项级数是否都是如此呢?下面来看一个例子.

例1 函数项级数

$$
x + (x ^ {2} - x) + (x ^ {3} - x ^ {2}) + \dots + (x ^ {n} - x ^ {n - 1}) + \dots
$$

的每一项都在[0,1]上连续,其前n项之和为 $s_{n}(x)=x^{n}$ ，因此和函数为

$$
s (x) = \lim _ {n \to \infty} s _ {n} (x) = \left\{ \begin{array}{l l} 0, & 0 \leqslant x <   1, \\ 1, & x = 1. \end{array} \right.
$$

这和函数 $s(x)$ 在 $x = 1$ 处间断.由此可见，函数项级数的每一项在 $[a,b]$ 上连续，并且级数在 $[a,b]$ 上收敛，其和函数不一定在 $[a,b]$ 上连续.也可以举出这样的例子，函数项级数的每一项的导数及积分所成的级数的和并不等于它们的和函数的导数及积分.这就提出了这样一个问题:对什么级数，能够从级数每一项的连续性得出它的和函数的连续性，从级数的每一项的导数及积分所成的级数之和得出原来级数的和函数的导数及积分呢？要回答这个问题，就需要引入下面的函数项级数的一致收敛性概念.

设函数项级数

$$
u _ {1} (x) + u _ {2} (x) + \dots + u _ {n} (x) + \dots
$$

在区间 $I$ 上收敛于和 $s(x)$. 也就是对于区间 $I$ 上的每一个值 $x_0$, 数项级数 $\sum_{n=1}^{\infty} u_n(x_0)$ 收敛于 $s(x_0)$, 即级数的部分和所成的数列

$$
s _ {n} (x _ {0}) = \sum_ {i = 1} ^ {n} u _ {i} (x _ {0}) \longrightarrow s (x _ {0}) \quad (n \longrightarrow \infty).
$$

按数列极限的定义,对于任意给定的正数  $\varepsilon$  以及区间 I 上的每一个值  $x_{0}$ , 都存在着一个正整数 N, 使得当 n > N 时, 有不等式

$$
\mid s (x _ {0}) - s _ {n} (x _ {0}) \mid <   \varepsilon ,
$$

即

$$
\mid r _ {n} (x _ {0}) \mid = \Big | \sum_ {i = n + 1} ^ {\infty} u _ {i} (x _ {0}) \Big | <   \varepsilon .
$$

这个数 $N$ 一般说来不仅依赖于 $\varepsilon$, 而且也依赖于 $x_0$, 我们记它为 $N(x_0, \varepsilon)$. 如果对于某一函数项级数能够找到这样一个正整数 $N$, 它只依赖于 $\varepsilon$ 而不依赖于 $x_0$, 也就是对区间 $I$ 上的每一个值 $x_0$ 都能适用的 $N(\varepsilon)$, 对这类级数我们给一个特殊的名称以区别于一般的收敛级数, 这就是下面的一致收敛的定义.

定义 设有函数项级数 $\sum_{n=1}^{\infty} u_n(x)$. 如果对于任意给定的正数 $\varepsilon$, 都存在着一个只依赖于 $\varepsilon$ 的正整数 $N$, 使得当 $n > N$ 时, 对区间 $I$ 上的一切 $x$, 都有不等式

$$
\mid r _ {n} (x) \mid = \mid s (x) - s _ {n} (x) \mid <   \varepsilon
$$

成立,那么称函数项级数  $\sum_{n=1}^{\infty}u_{n}(x)$  在区间 I 上一致收敛于和  $s(x)$ ，也称函数序列

$\{s_{n}(x)\}$  在区间 I 上一致收敛于  $s(x)$ .

以上函数项级数一致收敛的定义在几何上可解释为: 只要 n 充分大  $(n > N)$ ，在区间 I 上的所有曲线  $y = s_{n}(x)$  将位于曲线

$$
y = s (x) + \varepsilon \quad \text {与} \quad y = s (x) - \varepsilon
$$

之间(图 12-6).

![](images/page_294_image_5.jpg)

<details>
<summary>text_image</summary>

y
y=s(x)+ε
ε
ε
y=s_n(x)
y=s(x)
y=s(x)-ε
O
I
x
</details>

图12-6

例2 研究级数

$$
\frac {1}{x + 1} + \left(\frac {1}{x + 2} - \frac {1}{x + 1}\right) + \dots + \left(\frac {1}{x + n} - \frac {1}{x + n - 1}\right) + \dots
$$

在区间 $[0,+\infty)$ 上的一致收敛性.

解 级数的前 $n$ 项和 $s_n(x) = \frac{1}{x + n}$, 因此级数的和

$$
s (x) = \lim _ {n \to \infty} s _ {n} (x) = \lim _ {n \to \infty} \frac {1}{x + n} = 0 \quad (0 \leqslant x <   + \infty).
$$

于是,余项的绝对值

$$
\mid r _ {n} (x) \mid = \mid s (x) - s _ {n} (x) \mid = \frac {1}{x + n} \leqslant \frac {1}{n} \quad (0 \leqslant x <   + \infty).
$$

对于任给 $\varepsilon > 0$，取正整数 $N \geqslant \frac{1}{\varepsilon}$，则当 $n > N$ 时，对于区间 $[0, +\infty)$ 上的一切 $x$，有

$$
\mid r _ {n} (x) \mid <   \varepsilon .
$$

根据定义,所给级数在区间 $[0,+\infty)$ 上一致收敛于 $s(x)\equiv0$ .

例3 研究例1中的级数

$$
x + (x ^ {2} - x) + \dots + (x ^ {n} - x ^ {n - 1}) + \dots
$$

在区间 $(0,1)$ 内的一致收敛性.

解 这级数在区间(0,1)内处处收敛于和 $s(x) \equiv 0$, 但并不一致收敛. 事实上, 这个级数的部分和 $s_n(x) = x^n$, 对于任意一个正整数 $n$, 取 $x_n = \frac{1}{\sqrt[n]{2}}$, 于是

$$
s _ {n} (x _ {n}) = x _ {n} ^ {n} = \frac {1}{2},
$$

但 $s(x_{n}) = 0$ ，从而

$$
\mid r _ {n} (x _ {n}) \mid = \mid s (x _ {n}) - s _ {n} (x _ {n}) \mid = \frac {1}{2}.
$$

所以, 只要取 $\varepsilon < \frac{1}{2}$, 不论 $n$ 多么大, 在 $(0,1)$ 内总存在这样的点 $x_{n}$, 使得 $|r_{n}(x_{n})| > \varepsilon$, 因此所给级数在 $(0,1)$ 内不一致收敛. 这表明虽然函数序列 $s_{n}(x) = x^{n}$ 在 $(0,1)$ 内处处收敛于 $s(x) \equiv 0$，但 $s_n(x)$ 在 $(0,1)$ 内各点处收敛于零的“快慢”程度是不一致的，从图12-7中我们也可以看出这一情形。

可是对于任意正数 $r < 1$ ，这级数在 $[0, r]$ 上一致收敛. 这是因为当 $x = 0$ 时，显然

$$
\mid r _ {n} (x) \mid = x ^ {n} <   \varepsilon ;
$$

当 $0 < x \leqslant r$ 时，要使 $x^n < \varepsilon$ （不妨设 $\varepsilon < 1$），只要 $n \ln x < \ln \varepsilon$ 或 $n > \frac{\ln \varepsilon}{\ln x}$，而 $\frac{\ln \varepsilon}{\ln x}$ 在 $(0, r]$ 上的最大值为

![](images/page_295_chart_5.jpg)

<details>
<summary>contour</summary>

| n | Description |
| --- | --- |
| 1 | Curve starting at (0,0) and ending at (1,1) |
| 2 | Curve starting from (0,0) and ending at (1,1) |
| 4 | Curve starting from (0,0) and ending at (1,1) |
| 10 | Curve starting from (0,0) and ending at (1,1) |
| 30 | Curve starting from (0,0) and ending at (1,1) |
</details>

图12-7

$\frac{\ln\varepsilon}{\ln r}$ ，故取正整数 $N\geqslant \frac{\ln\varepsilon}{\ln r}$ ，则当 $n > N$ 时，对 $[0,r]$ 上的一切 $x$ 都有 $x^n <   \varepsilon$

上述例子也说明了一致收敛性与所讨论的区间有关.以上两例都是直接根据定义来判定级数的一致收敛性的,现在介绍一个在实用上较方便的判别法.

定理(魏尔斯特拉斯(Weierstrass)判别法) 如果函数项级数  $\sum_{n=1}^{\infty} u_{n}(x)$  在区间 I 上满足条件:

(1)  $\left|u_{n}(x)\right|\leqslant a_{n}\quad(n=1,2,3,\cdots);$
(2) 正项级数  $\sum_{n=1}^{\infty}a_{n}$  收敛，

那么函数项级数 $\sum_{n=1}^{\infty} u_n(x)$ 在区间 $I$ 上一致收敛.

证 由条件(2)，对任意给定的 $\varepsilon > 0$，根据柯西审敛原理（第一节第三目）存在正整数 $N$，使得当 $n > N$ 时，对任意的正整数 $p$，都有

$$
a _ {n + 1} + a _ {n + 2} + \dots + a _ {n + p} <   \frac {\varepsilon}{2}.
$$

由条件(1)，对任何 $x \in I$ ，都有

$$
\begin{array}{l} \mid u _ {n + 1} (x) + u _ {n + 2} (x) + \dots + u _ {n + p} (x) \mid \leqslant \mid u _ {n + 1} (x) \mid + \mid u _ {n + 2} (x) \mid + \dots + \mid u _ {n + p} (x) \mid \\ \leqslant a _ {n + 1} + a _ {n + 2} + \dots + a _ {n + p} <   \frac {\varepsilon}{2}, \\ \end{array}
$$

令 $p\to \infty$ ，则由上式得

$$
\mid r _ {n} (x) \mid \leqslant \frac {\varepsilon}{2} <   \varepsilon .
$$

因此函数项级数 $\sum_{n=1}^{\infty} u_n(x)$ 在区间 $I$ 上一致收敛.

例 4 证明级数

$$
\frac {\sin x}{1 ^ {2}} + \frac {\sin 2 ^ {2} x}{2 ^ {2}} + \dots + \frac {\sin n ^ {2} x}{n ^ {2}} + \dots
$$

在 $(-∞,+∞)$ 内一致收敛.

证 因为在 $(-∞,+∞)$ 内

$$
\left| \frac {\sin n ^ {2} x}{n ^ {2}} \right| \leqslant \frac {1}{n ^ {2}} \quad (n = 1, 2, 3, \dots),
$$

而 $\sum_{n=1}^{\infty} \frac{1}{n^{2}}$ 收敛, 故由魏尔斯特拉斯判别法, 所给级数在 $(- \infty, +\infty)$ 内一致收敛.

## 二、一致收敛级数的基本性质

一致收敛级数有如下基本性质:

定理1 如果级数 $\sum_{n=1}^{\infty} u_n(x)$ 的各项 $u_n(x)$ 在区间 $[a, b]$ 上都连续，且 $\sum_{n=1}^{\infty} u_n(x)$ 在区间 $[a, b]$ 上一致收敛于 $s(x)$，那么 $s(x)$ 在 $[a, b]$ 上也连续。

证 设 $x_0, x$ 为 $[a, b]$ 上任意两点. 由等式

$$
s (x) = s _ {n} (x) + r _ {n} (x), \quad s (x _ {0}) = s _ {n} (x _ {0}) + r _ {n} (x _ {0})
$$

得

$$
\begin{array}{l} \mid s (x) - s (x _ {0}) \mid = \mid s _ {n} (x) - s _ {n} (x _ {0}) + r _ {n} (x) - r _ {n} (x _ {0}) \mid \\ \leqslant \left| s _ {n} (x) - s _ {n} (x _ {0}) \right| + \left| r _ {n} (x) \right| + \left| r _ {n} (x _ {0}) \right|. \tag {6-1} \\ \end{array}
$$

因为级数 $\sum_{n=1}^{\infty} u_n(x)$ 一致收敛于 $s(x)$, 所以对任意给定的正数 $\varepsilon$, 必有正整数 $N = N(\varepsilon)$, 使得当 $n > N$ 时, 对 $[a, b]$ 上的一切 $x$, 都有

$$
\mid r _ {n} (x) \mid <   \frac {\varepsilon}{3}. \tag {6-2}
$$

当然,也有 $\left|r_{n}(x_{0})\right|<\frac{\varepsilon}{3}$ .选定满足大于N的n之后, $s_{n}(x)$ 是有限项连续函数之和,故 $s_{n}(x)$ 在点 $x_{0}$ 连续,从而必有一个 $\delta>0$ 存在,当 $\left|x-x_{0}\right|<\delta$ 时,总有

$$
\mid s _ {n} (x) - s _ {n} (x _ {0}) \mid <   \frac {\varepsilon}{3}. \tag {6-3}
$$

由(6-1)、(6-2)、(6-3)式可见，对任给 $\varepsilon >0$ ，必有 $\delta >0$ ，当 $|x - x_0| < \delta$ 时，有

$$
\mid s (x) - s (x _ {0}) \mid <   \varepsilon .
$$

所以 $s(x)$ 在点 $x_0$ 处连续，而 $x_0$ 在 $[a, b]$ 上是任意的，因此 $s(x)$ 在 $[a, b]$ 上连续.

定理2 如果级数 $\sum_{n=1}^{\infty} u_n(x)$ 的各项 $u_n(x)$ 在区间 $[a, b]$ 上连续，且 $\sum_{n=1}^{\infty} u_n(x)$ 在 $[a, b]$ 上一致收敛于 $s(x)$，那么级数 $\sum_{n=1}^{\infty} u_n(x)$ 在 $[a, b]$ 上可以逐项积分，即

$$
\int_ {x _ {0}} ^ {x} s (x) \mathrm{d} x = \int_ {x _ {0}} ^ {x} u _ {1} (x) \mathrm{d} x + \int_ {x _ {0}} ^ {x} u _ {2} (x) \mathrm{d} x + \dots + \int_ {x _ {0}} ^ {x} u _ {n} (x) \mathrm{d} x + \dots , \tag {6-4}
$$

其中 $a \leqslant x_0 < x \leqslant b$，并且上式右端的级数在 $[a, b]$ 上也一致收敛。

证 因为级数 $\sum_{n=1}^{\infty} u_n(x)$ 在 $[a, b]$ 上一致收敛，由定理 $1, s(x), r_n(x)$ 都在 $[a, b]$ 上连续，所以积分 $\int_{x_0}^{x} s(x) \mathrm{d}x, \int_{x_0}^{x} r_n(x) \mathrm{d}x$ 存在，从而有

$$
\left| \int_ {x _ {0}} ^ {x} s (x) \mathrm{d} x - \int_ {x _ {0}} ^ {x} s _ {n} (x) \mathrm{d} x \right| = \left| \int_ {x _ {0}} ^ {x} r _ {n} (x) \mathrm{d} x \right| \leqslant \int_ {x _ {0}} ^ {x} | r _ {n} (x) | \mathrm{d} x.
$$

又由级数的一致收敛性,对任给正数  $\varepsilon$ , 必有  $N=N(\varepsilon)$ , 使得当 n>N 时, 对  $[a,b]$  上的一切 x, 都有

$$
\mid r _ {n} (x) \mid <   \frac {\varepsilon}{b - a}.
$$

于是, 当 n > N 时有

$$
\left| \int_ {x _ {0}} ^ {x} s (x) \mathrm{d} x - \int_ {x _ {0}} ^ {x} s _ {n} (x) \mathrm{d} x \right| \leqslant \int_ {x _ {0}} ^ {x} | r _ {n} (x) | \mathrm{d} x <   \frac {\varepsilon}{b - a} (x - x _ {0}) \leqslant \varepsilon .
$$

根据极限的定义,有

$$
\int_ {x _ {0}} ^ {x} s (x) \mathrm{d} x = \lim _ {n \to \infty} \int_ {x _ {0}} ^ {x} s _ {n} (x) \mathrm{d} x = \lim _ {n \to \infty} \sum_ {i = 1} ^ {n} \int_ {x _ {0}} ^ {x} u _ {i} (x) \mathrm{d} x,
$$

即

$$
\int_ {x _ {0}} ^ {x} s (x) \mathrm{d} x = \sum_ {i = 1} ^ {\infty} \int_ {x _ {0}} ^ {x} u _ {i} (x) \mathrm{d} x.
$$

由于 $N$ 只依赖于 $\varepsilon$ 而与 $x_0, x$ 无关，所以级数 $\sum_{i=1}^{\infty} \int_{x_0}^{x} u_i(x) \mathrm{d}x$ 在 $[a, b]$ 上一致收敛.

定理3 如果级数 $\sum_{n=1}^{\infty} u_n(x)$ 在区间 $[a, b]$ 上收敛于和 $s(x)$，它的各项 $u_n(x)$ 都具有连续导数 $u_n'(x)$，并且级数 $\sum_{n=1}^{\infty} u_n'(x)$ 在 $[a, b]$ 上一致收敛，那么级数 $\sum_{n=1}^{\infty} u_n(x)$ 在 $[a, b]$ 上也一致收敛，且可逐项求导，即

$$
s ^ {\prime} (x) = u _ {1} ^ {\prime} (x) + u _ {2} ^ {\prime} (x) + \dots + u _ {n} ^ {\prime} (x) + \dots . \tag {6-5}
$$

证 先证等式(6-5). 由于 $\sum_{n=1}^{\infty} u_n'(x)$ 在 $[a, b]$ 上一致收敛, 设其和为 $\varphi(x)$, 即 $\sum_{n=1}^{\infty} u_n'(x) = \varphi(x)$, 欲证(6-5), 只需证 $\varphi(x) = s'(x)$ 就可以了.

根据定理1知, $\varphi(x)$ 在 $[a,b]$ 上连续,根据定理2,级数 $\sum_{n=1}^{\infty}u_{n}^{\prime}(x)$ 可逐项积分,故有

$$
\int_ {x _ {0}} ^ {x} \varphi (x) \mathrm{d} x = \sum_ {n = 1} ^ {\infty} \int_ {x _ {0}} ^ {x} u _ {n} ^ {\prime} (x) \mathrm{d} x = \sum_ {n = 1} ^ {\infty} \left[ u _ {n} (x) - u _ {n} (x _ {0}) \right],
$$

而

$$
\sum_ {n = 1} ^ {\infty} u _ {n} (x) = s (x), \quad \sum_ {n = 1} ^ {\infty} u _ {n} (x _ {0}) = s (x _ {0}),
$$

故

$$
\sum_ {n = 1} ^ {\infty} \left[ u _ {n} (x) - u _ {n} (x _ {0}) \right] = s (x) - s (x _ {0}),
$$

从而有

$$
\int_ {x _ {0}} ^ {x} \varphi (x) \mathrm{d} x = s (x) - s (x _ {0}),
$$

其中 $a \leqslant x_0 < x \leqslant b$. 上式两端求导, 即得关系式

$$
\varphi (x) = s ^ {\prime} (x).
$$

再证级数 $\sum_{n=1}^{\infty} u_n(x)$ 在 $[a, b]$ 上也一致收敛.

根据定理2,级数  $\sum_{n=1}^{\infty}\int_{x_{0}}^{x}u_{n}^{\prime}(x)\mathrm{d}x$  在  $[a,b]$  上一致收敛,而

$$
\sum_ {n = 1} ^ {\infty} \int_ {x _ {0}} ^ {x} u _ {n} ^ {\prime} (x) \mathrm{d} x = \sum_ {n = 1} ^ {\infty} u _ {n} (x) - \sum_ {n = 1} ^ {\infty} u _ {n} (x _ {0}),
$$

所以

$$
\sum_ {n = 1} ^ {\infty} u _ {n} (x) = \sum_ {n = 1} ^ {\infty} \int_ {x _ {0}} ^ {x} u _ {n} ^ {\prime} (x) \mathrm{d} x + \sum_ {n = 1} ^ {\infty} u _ {n} (x _ {0}),
$$

由此即得所要证的结论.

必须注意,级数一致收敛并不能保证可以逐项求导.例如,在例4中我们已证明了级数

$$
\frac {\sin x}{1 ^ {2}} + \frac {\sin 2 ^ {2} x}{2 ^ {2}} + \dots + \frac {\sin n ^ {2} x}{n ^ {2}} + \dots
$$

在任何区间 $[a, b]$ 上都是一致收敛的，但逐项求导后的级数

$$
\cos x + \cos 2 ^ {2} x + \dots + \cos n ^ {2} x + \dots ,
$$

其一般项不趋于零,所以对任意值 x 都是发散的,因此原级数不可以逐项求导.

下面我们来讨论幂级数的一致收敛性.

定理4 如果幂级数 $\sum_{n=0}^{\infty} a_n x^n$ 的收敛半径为 $R > 0$, 那么此级数在 $(-R, R)$ 内的任一闭区间 $[a, b]$ 上一致收敛.

证 记 $r = \max \{|a|, |b|\}$，则对 $[a, b]$ 上的一切 $x$，都有

$$
\mid a _ {n} x ^ {n} \mid \leqslant \mid a _ {n} r ^ {n} \mid \quad (n = 0, 1, 2, \dots),
$$

而 $0 < r < R$ ，根据第三节定理1级数 $\sum_{n=0}^{\infty} a_n r^n$ 绝对收敛，由魏尔斯特拉斯判别法即得所要证的结论.

进一步还可证明,如果幂级数  $\sum_{n=0}^{\infty}a_{n}x^{n}$  在收敛区间的端点收敛,那么一致收敛的区间可扩大到包含端点.

下面我们来证明在第三节中指出的关于幂级数在其收敛区间内的和函数的连续性、逐项可导、逐项可积的结论.

关于和函数的连续性及逐项可积的结论,由定理4和定理1、定理2立即可得.关于逐项可导的结论,我们重新叙述成如下定理并给出证明.

定理5 如果幂级数 $\sum_{n=0}^{\infty} a_n x^n$ 的收敛半径为 $R > 0$, 那么其和函数 $s(x)$ 在 $(-R, R)$ 内可导, 且有逐项求导公式

$$
s ^ {\prime} (x) = \left(\sum_ {n = 0} ^ {\infty} a _ {n} x ^ {n}\right) ^ {\prime} = \sum_ {n = 1} ^ {\infty} n a _ {n} x ^ {n - 1},
$$

逐项求导后所得到的幂级数与原级数有相同的收敛半径.

证 先证级数 $\sum_{n=1}^{\infty} na_n x^{n-1}$ 在 $(-R, R)$ 内收敛.

在 $(-R,R)$ 内任意取定x,再选定 $x_{1}$ ,使得 $|x|<x_{1}<R.$ 记 $q=\frac{|x|}{x_{1}}<1$ ,则

$$
\left| n a _ {n} x ^ {n - 1} \right| = n \left| \frac {x}{x _ {1}} \right| ^ {n - 1} \cdot \frac {1}{x _ {1}} \left| a _ {n} x _ {1} ^ {n} \right| = n q ^ {n - 1} \cdot \frac {1}{x _ {1}} \left| a _ {n} x _ {1} ^ {n} \right|,
$$

由比值审敛法可知级数 $\sum_{n=1}^{\infty} n q^{n-1}$ 收敛, 于是

$$
n q ^ {n - 1} \longrightarrow 0 \quad (n \longrightarrow \infty),
$$

故数列 $\{nq^{n - 1}\}$ 有界，必有 $M > 0$ ，使得

$$
n q ^ {n - 1} \cdot \frac {1}{x _ {1}} \leqslant M \quad (n = 1, 2, \dots).
$$

又 $0 < x_{1} < R$ ，级数 $\sum_{n=1}^{\infty}\left|a_{n}x_{1}^{n}\right|$ 收敛，由比较审敛法的推论即得级数 $\sum_{n=1}^{\infty}na_{n}x^{n-1}$ 收敛.

由定理4,级数 $\sum_{n=1}^{\infty} na_n x^{n-1}$ 在 $(-R, R)$ 内的任一闭区间 $[a, b]$ 上一致收敛, 故幂级数 $\sum_{n=1}^{\infty} a_n x^n$ 在 $[a, b]$ 上符合定理3的条件, 从而可逐项求导. 再由 $[a, b]$ 在 $(-R, R)$ 内的任意性, 即得幂级数 $\sum_{n=1}^{\infty} a_n x^n$ 在 $(-R, R)$ 内可逐项求导.

设幂级数 $\sum_{n=1}^{\infty} na_n x^{n-1}$ 的收敛半径为 $R'$, 上面已证得 $R \leqslant R'$. 将此幂级数在 $[0, x]$ ($|x| < R'$) 上逐项积分即得 $\sum_{n=1}^{\infty} a_n x^n$, 因逐项积分所得级数的收敛半径不会缩小, 所以

$R'\leqslant R$ , 于是  $R'=R$ . 定理 5 证毕.

## \*习题12-6

1. 已知函数序列  $s_{n}(x)=\sin\frac{x}{n}\quad(n=1,2,3,\cdots)$  在  $(-∞,+∞)$  上收敛于 0,

(1) 问  $N(\varepsilon, x)$  取多大, 能使当 n > N 时,  $s_{n}(x)$  与其极限之差的绝对值小于正数  $\varepsilon$ ;
(2) 证明 $s_n(x)$ 在任一有限区间 $[a, b]$ 上一致收敛.

2. 已知级数  $x^{2}+\frac{x^{2}}{1+x^{2}}+\frac{x^{2}}{(1+x^{2})^{2}}+\cdots$  在  $(-∞,+∞)$  上收敛.

(1) 求出该级数的和;
(2) 问 $N(\varepsilon, x)$ 取多大, 能使当 $n > N$ 时, 级数的余项 $r_n$ 的绝对值小于正数 $\varepsilon$;
(3) 分别讨论级数在区间  $[0,1]$ ,  $\left\lceil\frac{1}{2},1\right\rceil$  上的一致收敛性.

3. 按定义讨论下列级数在所给区间上的一致收敛性:

(1) $\sum_{n=1}^{\infty}(-1)^{n-1}\frac{x^2}{(1+x^2)^n}, (-\infty, +\infty)$;

(2) $\sum_{n=0}^{\infty}(1-x)x^{n}, (0,1)$.

4. 利用魏尔斯特拉斯判别法证明下列级数在所给区间上的一致收敛性:

(1) $\sum_{n=1}^{\infty} \frac{\cos nx}{2^n}, (-\infty, +\infty)$;

(2) $\sum_{n=1}^{\infty} \frac{\sin nx}{\sqrt[3]{n^4 + x^4}}, (-\infty, +\infty)$;

(3) $\sum_{n=1}^{\infty} x^{2} \mathrm{e}^{-nx}, [0, +\infty)$;

(4) $\sum_{n=1}^{\infty} \frac{e^{-nx}}{n!}, (-10, 10)$;

(5) $\sum_{n=1}^{\infty} \frac{(-1)^{n}(1 - e^{-nx})}{n^{2} + x^{2}}, [0, +\infty)$.

## 第七节 傅里叶级数

从本节开始,我们讨论由三角函数组成的函数项级数,即所谓三角级数,着重研究如何把函数展开成三角级数.

## 一、三角级数 三角函数系的正交性

在第一章中,我们介绍过周期函数的概念,周期函数反映了客观世界中的周期运动.

正弦函数是一种常见而简单的周期函数.例如描述简谐振动的函数

$$
y = A \sin (\omega t + \varphi)
$$

就是一个以 $\frac{2\pi}{\omega}$ 为周期的正弦函数,其中y表示动点的位置,t表示时间,A为振幅, $\omega$ 为角频率, $\varphi$ 为初相.

在实际问题中,除了正弦函数外,还会遇到非正弦函数的周期函数,它们反映了较

复杂的周期运动. 如电子技术中常用的周期为 T 的矩形波(图 12-8), 就是一个非正弦周期函数的例子.

如何深入研究非正弦周期函数呢？联系到前面介绍过的用函数的幂级数展开式表示与讨论函数，我们也

![](images/page_301_chart_5.jpg)

<details>
<summary>line</summary>

| Point | x | u |
| --- | --- | --- |
| 1 | ~-0.5 | E |
| 2 | ~-0.5 | E |
| 3 | ~-0.5 | E |
| 4 | ~-0.5 | E |
| 5 | ~-0.5 | E |
| 6 | ~-0.5 | E |
| 7 | ~-0.5 | E |
| 8 | ~-0.5 | E |
| 9 | ~-0.5 | E |
| 10 | ~-0.5 | E |
| 11 | ~-0.5 | E |
| 12 | ~-0.5 | E |
| 13 | ~-0.5 | E |
| 14 | ~-0.5 | E |
| 15 | ~-0.5 | E |
| 16 | ~-0.5 | E |
| 17 | ~-0.5 | E |
| 18 | ~-0.5 | E |
| 19 | ~-0.5 | E |
| 20 | ~-0.5 | E |
| 21 | ~-0.5 | E |
| 22 | ~-0.5 | E |
| 23 | ~-0.5 | E |
| 24 | ~-0.5 | E |
| 25 | ~-0.5 | E |
| 26 | ~-0.5 | E |
| 27 | ~-0.5 | E |
| 28 | ~-0.5 | E |
| 29 | ~-0.5 | E |
| 30 | ~-0.5 | E |
| 31 | ~-0.5 | E |
| 32 | ~-0.5 | E |
| 33 | ~-0.5 | E |
| 34 | ~-0.5 | E |
| 35 | ~-0.5 | E |
| 36 | ~-0.5 | E |
| 37 | ~-0.5 | E |
| 38 | ~-0.5 | E |
| 39 | ~-0.5 | E |
| 40 | ~-0.5 | E |
| 41 | ~-0.5 | E |
| 42 | ~-0.5 | E |
| 43 | ~-0.5 | E |
| 44 | ~-0.5 | E |
| 45 | ~-0.5 | E |
| 46 | ~-0.5 | E |
| 47 | ~-0.5 | E |
| 48 | ~-0.5 | E |
| 49 | ~-0.5 | E |
| 50 | ~-0.5 | E |
| 51 | ~-0.5 | E |
| 52 | ~-0.5 | E |
| 53 | ~-0.5 | E |
| 54 | ~-0.5 | E |
| 55 | ~-0.5 | E |
| 56 | ~-0.5 | E |
| 57 | ~-0.5 | E |
| 58 | ~-0.5 | E |
| 59 | ~-0.5 | E |
| 60 | ~-0.5 | E |
| 61 | ~-0.5 | E |
| 62 | ~-0.5 | E |
| 63 | ~-0.5 | E |
| 64 | ~-0.5 | E |
| 65 | ~-0.5 | E |
| 66 | ~-0.5 | E |
| 67 | ~-0.5 | E |
| 68 | ~-0.5 | E |
| 69 | ~-0.5 | E |
| 70 | ~-0.5 | E |
| 71 | ~-0.5 | E |
| 72 | ~-0.5 | E |
| 73 | ~-0.5 | E |
| 74 | ~-0.5 | E |
| 75 | ~-0.5 | E |
| 76 | ~-0.5 | E |
| 77 | ~-0.5 | E |
| 78 | ~-0.5 | E |
| 79 | ~-0.5 | E |
| 80 | ~-0.5 | E |
| 81 | ~-0.5 | E |
| 82 | ~-0.5 | E |
| 83 | ~-0.5 | E |
| 84 | ~-0.5 | E |
| 85 | ~-0.5 | E |
| 86 | ~-0.5 | E |
| 87 | ~-0.5 | E |
| 88 | ~-0.5 | E |
| 89 | ~-0.5 | E |
| 90 | ~-0.5 | E |
| 91 | ~-0.5 | E |
| 92 | ~-0.5 | E |
| 93 | ~-0.5 | E |
| 94 | ~-0.5 | E |
| 95 | ~-0.5 | E |
| 96 | ~-0.5 | E |
| 97 | ~-0.5 | E |
| 98 | ~-0.5 | E |
| 99 | ~-0.5 | E |
| 100 | ~-0.5 | E |
</details>

图12-8

想将周期函数展开成由简单的周期函数例如三角函数组成的级数.具体地说,将周期为  $T\left(T=\frac{2\pi}{\omega}\right)$  的周期函数用一系列以 T 为周期的正弦函数  $A_{n}\sin(n\omega t+\varphi_{n})$  组成的级数来表示,记为

$$
f (t) = A _ {0} + \sum_ {n = 1} ^ {\infty} A _ {n} \sin (n \omega t + \varphi_ {n}), \tag {7-1}
$$

其中  $A_{0}, A_{n}, \varphi_{n} (n=1,2,3,\cdots)$  都是常数.

将周期函数按上述方式展开,它的物理意义是很明确的,这就是把一个比较复杂的周期运动看成是许多不同频率的简谐振动的叠加.在电工学上,这种展开称为谐波分析,其中常数项 $A_{0}$ 称为 $f(t)$ 的直流分量, $A_{1}\sin(\omega t+\varphi_{1})$ 称为一次谐波(又叫做基波), $A_{2}\sin(2\omega t+\varphi_{2})$ , $A_{3}\sin(3\omega t+\varphi_{3})$ ,…依次称为二次谐波,三次谐波,等等.

为了以后讨论方便起见,我们将正弦函数 $A_{n}\sin(n\omega t+\varphi_{n})$ 按三角公式变形,得

$$
A _ {n} \sin (n \omega t + \varphi_ {n}) = A _ {n} \sin \varphi_ {n} \cos n \omega t + A _ {n} \cos \varphi_ {n} \sin n \omega t,
$$

并且令 $\frac{a_{0}}{2}=A_{0},a_{n}=A_{n}\sin\varphi_{n},b_{n}=A_{n}\cos\varphi_{n},\omega=\frac{\pi}{l}$ （即T=2l），则(7-1)式右端的级数就可以改写为

$$
\frac {a _ {0}}{2} + \sum_ {n = 1} ^ {\infty} \left(a _ {n} \cos \frac {n \pi t}{l} + b _ {n} \sin \frac {n \pi t}{l}\right). \tag {7-2}
$$

形如(7-2)式的级数叫做三角级数,其中 $a_{0},a_{n},b_{n}(n=1,2,3,\cdots)$ 都是常数.

令 $\frac{\pi t}{l} = x, (7 - 2)$ 式成为

$$
\frac {a _ {0}}{2} + \sum_ {n = 1} ^ {\infty} (a _ {n} \cos n x + b _ {n} \sin n x), \tag {7-3}
$$

这就把以 $2l$ 为周期的三角级数转换成以 $2\pi$ 为周期的三角级数.

下面我们讨论以  $2\pi$  为周期的三角级数(7-3).

如同讨论幂级数时一样,我们必须讨论三角级数(7-3)的收敛问题,以及给定周期为 $2\pi$ 的周期函数如何把它展开成三角级数(7-3).为此,我们首先介绍三角函数系的正交性.

所谓三角函数系

$$
1, \cos x, \sin x, \cos 2 x, \sin 2 x, \dots , \cos n x, \sin n x, \dots \tag {7-4}
$$

在区间 $[-π,π]$ 上正交,就是指在三角函数系(7-4)中任何不同的两个函数的乘积在区间 $[-π,π]$ 上的积分等于零,即

$$
\begin{array}{l} \int_ {- \pi} ^ {\pi} \cos n x \mathrm{d} x = 0 \quad (n = 1, 2, 3, \dots), \\ \int_ {- \pi} ^ {\pi} \sin n x \mathrm{d} x = 0 \quad (n = 1, 2, 3, \dots), \\ \int_ {- \pi} ^ {\pi} \sin k x \cos n x \mathrm{d} x = 0 \quad (k, n = 1, 2, 3, \dots), \\ \int_ {- \pi} ^ {\pi} \cos k x \cos n x \mathrm{d} x = 0 \quad (k, n = 1, 2, 3, \dots , k \neq n), \\ \int_ {- \pi} ^ {\pi} \sin k x \sin n x \mathrm{d} x = 0 \quad (k, n = 1, 2, 3, \dots , k \neq n). \\ \end{array}
$$

以上等式,都可以通过计算定积分来验证,现将第四式验证如下:

利用三角函数中积化和差的公式

$$
\cos k x \cos n x = \frac {1}{2} \big [ \cos (k + n) x + \cos (k - n) x \big ],
$$

当 $k \neq n$ 时, 有

$$
\begin{array}{l} \int_ {- \pi} ^ {\pi} \cos k x \cos n x \mathrm{d} x = \frac {1}{2} \int_ {- \pi} ^ {\pi} [ \cos (k + n) x + \cos (k - n) x ] \mathrm{d} x \\ = \frac {1}{2} \left[ \frac {\sin (k + n) x}{k + n} + \frac {\sin (k - n) x}{k - n} \right] _ {- \pi} ^ {\pi} \\ = 0 \quad (k, n = 1, 2, 3, \dots , k \neq n). \\ \end{array}
$$

其余等式请读者自行验证.

在三角函数系(7-4)中,两个相同函数的乘积在区间 $[-π,π]$ 上的积分不等于零,即

$$
\int_ {- \pi} ^ {\pi} 1 ^ {2} \mathrm{d} x = 2 \pi , \quad \int_ {- \pi} ^ {\pi} \sin^ {2} n x \mathrm{d} x = \pi , \quad \int_ {- \pi} ^ {\pi} \cos^ {2} n x \mathrm{d} x = \pi \quad (n = 1, 2, 3, \dots).
$$

## 二、函数展开成傅里叶级数

设 $f(x)$ 是周期为 $2\pi$ 的周期函数，且能展开成三角级数

$$
f (x) = \frac {a _ {0}}{2} + \sum_ {k = 1} ^ {\infty} (a _ {k} \cos k x + b _ {k} \sin k x). \tag {7-5}
$$

我们自然要问:系数 $a_{0},a_{1},b_{1},\cdots$ 与函数 $f(x)$ 之间存在着怎样的关系?换句话说,如何利用 $f(x)$ 把 $a_{0},a_{1},b_{1},\cdots$ 表达出来?为此,我们进一步假设(7-5)式右端的级数可以逐项积分.

先求 $a_0$ 对(7-5)式从 $-\pi$ 到 $\pi$ 积分，由于假设(7-5)式右端级数可逐项积分，因此有

$$
\int_ {- \pi} ^ {\pi} f (x) \mathrm{d} x = \int_ {- \pi} ^ {\pi} \frac {a _ {0}}{2} \mathrm{d} x + \sum_ {k = 1} ^ {\infty} \left[ a _ {k} \int_ {- \pi} ^ {\pi} \cos k x \mathrm{d} x + b _ {k} \int_ {- \pi} ^ {\pi} \sin k x \mathrm{d} x \right].
$$

根据三角函数系(7-4)的正交性,等式右端除第一项外,其余各项均为零,所以

$$
\int_ {- \pi} ^ {\pi} f (x) \mathrm{d} x = \frac {a _ {0}}{2} \cdot 2 \pi ,
$$

于是得

$$
a _ {0} = \frac {1}{\pi} \int_ {- \pi} ^ {\pi} f (x) \mathrm{d} x.
$$

其次求 $a_{n}$. 用 $\cos nx$ 乘(7-5)式两端, 再从 $-\pi$ 到 $\pi$ 积分, 我们得到

$$
\int_ {- \pi} ^ {\pi} f (x) \cos n x \mathrm{d} x = \frac {a _ {0}}{2} \int_ {- \pi} ^ {\pi} \cos n x \mathrm{d} x + \sum_ {k = 1} ^ {\infty} \left[ a _ {k} \int_ {- \pi} ^ {\pi} \cos k x \cos n x \mathrm{d} x + b _ {k} \int_ {- \pi} ^ {\pi} \sin k x \cos n x \mathrm{d} x \right].
$$

根据三角函数系(7-4)的正交性,等式右端除k=n的一项外,其余各项均为零,所以

$$
\int_ {- \pi} ^ {\pi} f (x) \cos n x \mathrm{d} x = a _ {n} \int_ {- \pi} ^ {\pi} \cos^ {2} n x \mathrm{d} x = a _ {n} \pi ,
$$

于是得

$$
a _ {n} = \frac {1}{\pi} \int_ {- \pi} ^ {\pi} f (x) \cos n x \mathrm{d} x \quad (n = 1, 2, 3, \dots).
$$

类似地,用  $\sin nx$  乘(7-5)式的两端,再从  $-\pi$  到  $\pi$  积分,可得

$$
b _ {n} = \frac {1}{\pi} \int_ {- \pi} ^ {\pi} f (x) \sin n x \mathrm{d} x \quad (n = 1, 2, 3, \dots).
$$

由于当 $n = 0$ 时，$a_{n}$ 的表达式正好给出 $a_0$ ，因此，已得结果可以合并写成

$$
\left. \begin{array}{l} a _ {n} = \frac {1}{\pi} \int_ {- \pi} ^ {\pi} f (x) \cos n x \mathrm{d} x \quad (n = 0, 1, 2, 3, \dots), \\ b _ {n} = \frac {1}{\pi} \int_ {- \pi} ^ {\pi} f (x) \sin n x \mathrm{d} x \quad (n = 1, 2, 3, \dots). \end{array} \right\} \tag {7-6}
$$

如果公式(7-6)中的积分都存在,这时它们定出的系数 $a_{0},a_{1},b_{1},\cdots$ 叫做函数 $f(x)$ 的傅里叶(Fourier)系数,将这些系数代入(7-5)式右端,所得的三角级数

$$
\frac {a _ {0}}{2} + \sum_ {n = 1} ^ {\infty} (a _ {n} \cos n x + b _ {n} \sin n x)
$$

叫做函数 $f(x)$ 的傅里叶级数.

一个定义在 $(-\infty, +\infty)$ 上周期为 $2\pi$ 的函数 $f(x)$，如果它在一个周期上可积，那么一定可以作出 $f(x)$ 的傅里叶级数。然而，函数 $f(x)$ 的傅里叶级数是否一定收敛？如果它收敛，它是否一定收敛于函数 $f(x)$？一般说来，这两个问题的答案都不是肯定的。那么，$f(x)$ 在怎样的条件下，它的傅里叶级数不仅收敛，而且收敛于 $f(x)$？也就是说，$f(x)$ 满足什么条件可以展开成傅里叶级数？这是我们面临的一个基本问题。

下面我们叙述一个收敛定理(不加证明),它给出关于上述问题的一个重要结论.

定理(收敛定理,狄利克雷(Dirichlet)充分条件) 设 $f(x)$ 是周期为 $2\pi$ 的周期函数,如果它满足

（1）在一个周期内连续或只有有限个第一类间断点，
(2) 在一个周期内至多只有有限个极值点，

那么 $f(x)$ 的傅里叶级数收敛，并且

当 $x$ 是 $f(x)$ 的连续点时，级数收敛于 $f(x)$；

当 $x$ 是 $f(x)$ 的间断点时，级数收敛于 $\frac{1}{2} [f(x^{-}) + f(x^{+})]$.

收敛定理告诉我们: 只要函数在  $[-π, π]$  上至多有有限个第一类间断点, 并且不做无限次振动, 函数的傅里叶级数在连续点处就收敛于该点的函数值, 在间断点处收敛于该点左极限与右极限的算术平均值. 可见, 函数展开成傅里叶级数的条件比展开成幂级数的条件低得多. 记

$$
C = \left\{x \Bigg | f (x) = \frac {1}{2} [ f (x ^ {-}) + f (x ^ {+}) ] \right\},
$$

在 $C$ 上就成立 $f(x)$ 的傅里叶级数展开式

$$
f (x) = \frac {a _ {0}}{2} + \sum_ {n = 1} ^ {\infty} (a _ {n} \cos n x + b _ {n} \sin n x), \quad x \in C. \tag {7-7}
$$

例1 设 $f(x)$ 是周期为 $2\pi$ 的周期函数, 它在 $[- \pi, \pi)$ 上的表达式为

$$
f (x) = \left\{ \begin{array}{l l} - 1, & - \pi \leqslant x <   0, \\ 1, & 0 \leqslant x <   \pi . \end{array} \right.
$$

将 $f(x)$ 展开成傅里叶级数，并作出级数的和函数的图形

解 所给函数满足收敛定理的条件, 它在点  $x=k\pi$  ( $k=0,\pm1,\pm2,\cdots$ ) 处不连续, 在其他点处连续, 从而由收敛定理知道  $f(x)$  的傅里叶级数收敛, 并且当  $x=k\pi$  时级数收敛于

$$
\frac {- 1 + 1}{2} = \frac {1 + (- 1)}{2} = 0,
$$

当  $x \neq k\pi$  时级数收敛于  $f(x)$ .

计算傅里叶系数如下:

$$
\begin{array}{l} a _ {n} = \frac {1}{\pi} \int_ {- \pi} ^ {\pi} f (x) \cos n x \mathrm{d} x = \frac {1}{\pi} \int_ {- \pi} ^ {0} (- 1) \cos n x \mathrm{d} x + \frac {1}{\pi} \int_ {0} ^ {\pi} 1 \cdot \cos n x \mathrm{d} x \\ = 0 \quad (n = 0, 1, 2, \dots); \\ b _ {n} = \frac {1}{\pi} \int_ {- \pi} ^ {\pi} f (x) \sin n x \mathrm{d} x = \frac {1}{\pi} \int_ {- \pi} ^ {0} (- 1) \sin n x \mathrm{d} x + \frac {1}{\pi} \int_ {0} ^ {\pi} 1 \cdot \sin n x \mathrm{d} x \\ = \frac {1}{\pi} \left[ \frac {\cos n x}{n} \right] _ {- \pi} ^ {0} + \frac {1}{\pi} \left[ - \frac {\cos n x}{n} \right] _ {0} ^ {\pi} \\ = \frac {1}{n \pi} [ 1 - \cos n \pi - \cos n \pi + 1 ] = \frac {2}{n \pi} [ 1 - (- 1) ^ {n} ] \\ = \left\{ \begin{array}{l l} \frac {4}{n \pi}, & n = 1, 3, 5, \dots , \\ 0, & n = 2, 4, 6, \dots . \end{array} \right. \\ \end{array}
$$

将求得的系数代入(7-7)式,就得到 $f(x)$ 的傅里叶级数展开式为

$$
\begin{array}{l} f (x) = \frac {4}{\pi} \left[ \sin x + \frac {1}{3} \sin 3 x + \dots + \frac {1}{2 k - 1} \sin (2 k - 1) x + \dots \right] \\ = \frac {4}{\pi} \sum_ {k = 1} ^ {\infty} \frac {1}{2 k - 1} \sin (2 k - 1) x \quad (- \infty <   x <   + \infty ; x \neq 0, \pm \pi , \pm 2 \pi , \dots). \\ \end{array}
$$

级数的和函数的图形如图 12-9 所示:

如果把例 1 中的函数理解为矩形波的波形函数(周期  $T=2\pi$ , 振幅 E=1, 自变量 x 表示时间), 那么上面所得到的展开式表明: 矩形波是由一系列不同频率的正弦波叠加而成的, 这些正弦波的频率依次为基波频率的奇数倍.

![](images/page_305_chart_8.jpg)

<details>
<summary>line</summary>

| X | Y |
| --- | --- |
| \(-2\pi\) | 1 |
| \(-\pi\) | 1 |
| 0 | 1 |
| \(\pi\) | 1 |
| \(2\pi\) | 1 |
</details>

图12-9

例 2 设  $f(x)$  是周期为  $2\pi$  的周期函数, 它在  $[-\pi, \pi)$  上的表达式为

$$
f (x) = \left\{ \begin{array}{l l} x, & - \pi \leqslant x <   0, \\ 0, & 0 \leqslant x <   \pi . \end{array} \right.
$$

将 $f(x)$ 展开成傅里叶级数,并作出级数的和函数的图形.

解 所给函数满足收敛定理的条件, 它在点  $x=(2k+1)\pi$  ( $k=0,\pm1,\pm2,\cdots$ ) 处不连续. 因此,  $f(x)$  的傅里叶级数在  $x=(2k+1)\pi$  处收敛于

$$
\frac {f (\pi^ {-}) + f (- \pi^ {+})}{2} = \frac {0 - \pi}{2} = - \frac {\pi}{2}.
$$

在连续点 $x (x \neq (2k + 1)\pi)$ 处收敛于 $f(x)$.

计算傅里叶系数如下:

例题精讲

12-8

$$
\begin{array}{l} a _ {n} = \frac {1}{\pi} \int_ {- \pi} ^ {\pi} f (x) \cos n x \mathrm{d} x = \frac {1}{\pi} \int_ {- \pi} ^ {0} x \cos n x \mathrm{d} x \\ = \frac {1}{\pi} \left[ \frac {x \sin n x}{n} + \frac {\cos n x}{n ^ {2}} \right] _ {- \pi} ^ {0} = \frac {1}{n ^ {2} \pi} (1 - \cos n \pi) \\ = \left\{ \begin{array}{l l} \frac {2}{n ^ {2} \pi}, & n = 1, 3, 5, \dots , \\ 0, & n = 2, 4, 6, \dots ; \end{array} \right. \\ a _ {0} = \frac {1}{\pi} \int_ {- \pi} ^ {\pi} f (x) \mathrm{d} x = \frac {1}{\pi} \int_ {- \pi} ^ {0} x \mathrm{d} x = \frac {1}{\pi} \left[ \frac {x ^ {2}}{2} \right] _ {- \pi} ^ {0} = - \frac {\pi}{2}; \\ b _ {n} = \frac {1}{\pi} \int_ {- \pi} ^ {\pi} f (x) \sin n x \mathrm{d} x = \frac {1}{\pi} \int_ {- \pi} ^ {0} x \sin n x \mathrm{d} x \\ = \frac {1}{\pi} \left[ - \frac {x \cos n x}{n} + \frac {\sin n x}{n ^ {2}} \right] _ {- \pi} ^ {0} \\ = - \frac {\cos n \pi}{n} = \frac {(- 1) ^ {n + 1}}{n} \quad (n = 1, 2, 3, \dots). \\ \end{array}
$$

将求得的系数代入(7-7)式,得到 $f(x)$ 的傅里叶级数展开式为

$$
\begin{array}{l} f (x) = - \frac {\pi}{4} + \left(\frac {2}{\pi} \cos x + \sin x\right) - \frac {1}{2} \sin 2 x + \left(\frac {2}{3 ^ {2} \pi} \cos 3 x + \frac {1}{3} \sin 3 x\right) - \\ \frac {1}{4} \sin 4 x + \left(\frac {2}{5 ^ {2} \pi} \cos 5 x + \frac {1}{5} \sin 5 x\right) - \dots \\ = - \frac {\pi}{4} + \frac {2}{\pi} \sum_ {k = 1} ^ {\infty} \frac {1}{(2 k - 1) ^ {2}} \cos (2 k - 1) x + \sum_ {n = 1} ^ {\infty} \frac {(- 1) ^ {n - 1}}{n} \sin n x \\ (- \infty <   x <   + \infty ; x \neq \pm \pi , \pm 3 \pi , \dots). \\ \end{array}
$$

级数的和函数的图形如图 12-10 所示:

![](images/page_306_chart_8.jpg)

<details>
<summary>line</summary>

| X-axis (x) | Y-axis (y) |
| --- | --- |
| \(-3\pi\) | 0 |
| \(-2\pi\) | 0 |
| \(-\pi\) | 0 |
| 0 | 0 |
| \(\pi/2\) | 0 |
| \(2\pi\) | 0 |
| \(3\pi\) | 0 |
</details>

图12-10

应该注意,如果函数 $f(x)$ 只在 $[-\pi,\pi]$ 上有定义,并且满足收敛定理的条件,那么 $f(x)$ 也可以展开成傅里叶级数.事实上,我们可在 $[-\pi,\pi)$ 或 $(-π,π]$ 外补充函数 $f(x)$ 的定义,使它拓广成周期为 $2π$ 的周期函数 $F(x)$.按这种方式拓广函数的定义域的过程称为周期延拓.再将 $F(x)$ 展开成傅里叶级数.最后限制x在 $(-π,π)$ 内,此时 $F(x)≡f(x)$ ,这样便得到 $f(x)$ 的傅里叶级数展开式.根据收敛定理,这级数在区间端点 $x=±π$ 处收敛于 $\frac{f(\pi^{-})+f(-\pi^{+})}{2}$ .

例3 将函数

$$
u (t) = E \left| \sin \frac {t}{2} \right|, \quad - \pi \leqslant t \leqslant \pi
$$

展开成傅里叶级数,其中 E 是正的常数.

解 所给函数在区间 $[-π, π]$ 上满足收敛定理的条件,并且拓广为周期函数时,

它在每一点 $x$ 处都连续（图12-11），因此拓广的周期函数的傅里叶级数在 $[- \pi, \pi]$ 上收敛于 $u(t)$.

计算傅里叶系数如下:

$$
\begin{array}{l} a _ {n} = \frac {1}{\pi} \int_ {- \pi} ^ {\pi} u (t) \cos n t \mathrm{d} t \\ = \frac {E}{\pi} \int_ {- \pi} ^ {\pi} \left| \sin \frac {t}{2} \right| \cos n t \mathrm{d} t, \\ \end{array}
$$

![](images/page_307_chart_9.jpg)

<details>
<summary>contour</summary>

| t | u |
| --- | --- |
| \(-2\pi\) | 0 |
| \(-\pi\) | ~E |
| 0 | 0 |
| \(\pi\) | ~E |
| \(2\pi\) | 0 |
</details>

图12-11

因为上列积分中被积函数为偶函数,所以

$$
\begin{array}{l} a _ {n} = \frac {2 E}{\pi} \int_ {0} ^ {\pi} \sin \frac {t}{2} \cos n t \mathrm{d} t = \frac {E}{\pi} \int_ {0} ^ {\pi} \left[ \sin \left(n + \frac {1}{2}\right) t - \sin \left(n - \frac {1}{2}\right) t \right] \mathrm{d} t \\ = \frac {E}{\pi} \left[ - \frac {\cos \left(n + \frac {1}{2}\right) t}{n + \frac {1}{2}} + \frac {\cos \left(n - \frac {1}{2}\right) t}{n - \frac {1}{2}} \right] _ {0} ^ {\pi} \\ = \frac {E}{\pi} \left(\frac {1}{n + \frac {1}{2}} - \frac {1}{n - \frac {1}{2}}\right) = - \frac {4 E}{(4 n ^ {2} - 1) \pi} \quad (n = 0, 1, 2, \dots). \\ b _ {n} = \frac {E}{\pi} \int_ {- \pi} ^ {\pi} \left| \sin \frac {t}{2} \right| \sin n t \mathrm{d} t = 0 \quad (n = 1, 2, 3, \dots). \\ \end{array}
$$

上式等于零是因为被积函数是奇函数.

将求得的系数代入(7-7)式, 得  $u(t)$  的傅里叶级数展开式为

$$
u (t) = \frac {4 E}{\pi} \left(\frac {1}{2} - \sum_ {n = 1} ^ {\infty} \frac {1}{4 n ^ {2} - 1} \cos n t\right) \quad (- \pi \leqslant t \leqslant \pi).
$$

## 三、正弦级数和余弦级数

一般说来,一个函数的傅里叶级数既含有正弦项,又含有余弦项(见例2).但是,也有一些函数的傅里叶级数只含有正弦项(见例1)或者只含有常数项和余弦项(见例3).这是什么原因呢？实际上，这些情况是与所给函数 $f(x)$ 的奇偶性有密切关系的.对于周期为 $2\pi$ 的函数 $f(x)$，它的傅里叶系数计算公式为

$$
a _ {n} = \frac {1}{\pi} \int_ {- \pi} ^ {\pi} f (x) \cos n x \mathrm{d} x \quad (n = 0, 1, 2, \dots),
$$

$$
b _ {n} = \frac {1}{\pi} \int_ {- \pi} ^ {\pi} f (x) \sin n x \mathrm{d} x \quad (n = 1, 2, 3, \dots).
$$

由于奇函数在对称区间上的积分为零,偶函数在对称区间上的积分等于半区间上积分的2倍,因此,

当 $f(x)$ 为奇函数时, $f(x)\cos nx$ 是奇函数, $f(x)\sin nx$ 是偶函数,故

$$
\left. \begin{array}{l} a _ {n} = 0 \quad (n = 0, 1, 2, \dots), \\ b _ {n} = \frac {2}{\pi} \int_ {0} ^ {\pi} f (x) \sin n x \mathrm{d} x \quad (n = 1, 2, 3, \dots). \end{array} \right\} \tag {7-8}
$$

即知奇函数的傅里叶级数是只含有正弦项的正弦级数

$$
\sum_ {n = 1} ^ {\infty} b _ {n} \sin n x. \tag {7-9}
$$

当 $f(x)$ 为偶函数时，$f(x)\cos nx$ 是偶函数，$f(x)\sin nx$ 是奇函数，故

$$
\left. \begin{array}{l} a _ {n} = \frac {2}{\pi} \int_ {0} ^ {\pi} f (x) \cos n x \mathrm{d} x \quad (n = 0, 1, 2, \dots), \\ b _ {n} = 0 \quad (n = 1, 2, 3, \dots). \end{array} \right\} \tag {7-10}
$$

即知偶函数的傅里叶级数是只含常数项和余弦项的余弦级数

$$
\frac {a _ {0}}{2} + \sum_ {n = 1} ^ {\infty} a _ {n} \cos n x. \tag {7-11}
$$

例 4 设  $f(x)$  是周期为  $2\pi$  的周期函数, 它在  $[-\pi, \pi)$  上的表达式为  $f(x) = x$ . 将  $f(x)$  展开成傅里叶级数, 并作出级数的和函数的图形.

解 首先,所给函数满足收敛定理的条件,它在点

$$
x = (2 k + 1) \pi \quad (k = 0, \pm 1, \pm 2, \dots)
$$

处不连续,因此 $f(x)$ 的傅里叶级数在点 $x=(2k+1)\pi$ 处收敛于

$$
\frac {f (\pi^ {-}) + f (- \pi^ {+})}{2} = \frac {\pi + (- \pi)}{2} = 0,
$$

在连续点 $x (x \neq (2k + 1)\pi)$ 处收敛于 $f(x)$.

其次,若不计 $x=(2k+1)\pi(k=0,\pm1,\pm2,\cdots)$ ，则 $f(x)$ 是周期为 $2\pi$ 的奇函数.显然,此时(7-8)式仍成立.按公式(7-8)有 $a_{n}=0(n=0,1,2,\cdots)$ ，而

$$
b _ {n} = \frac {2}{\pi} \int_ {0} ^ {\pi} f (x) \sin n x \mathrm{d} x = \frac {2}{\pi} \int_ {0} ^ {\pi} x \sin n x \mathrm{d} x = \frac {2}{\pi} \left[ - \frac {x \cos n x}{n} + \frac {\sin n x}{n ^ {2}} \right] _ {0} ^ {\pi}
$$

$$
= - \frac {2}{n} \cos n \pi = \frac {2}{n} (- 1) ^ {n + 1} \quad (n = 1, 2, 3, \dots).
$$

将求得的 $b_{n}$ 代入正弦级数(7-9)，得 $f(x)$ 的傅里叶级数展开式为

$$
\begin{array}{l} f (x) = 2 \left(\sin x - \frac {1}{2} \sin 2 x + \frac {1}{3} \sin 3 x - \dots + \frac {(- 1) ^ {n + 1}}{n} \sin n x + \dots\right) \\ = 2 \sum_ {n = 1} ^ {\infty} \frac {(- 1) ^ {n + 1}}{n} \sin n x \quad (- \infty <   x <   + \infty ; x \neq \pm \pi , \pm 3 \pi , \dots). \\ \end{array}
$$

级数的和函数的图形如图 12-12 所示:

![](images/page_309_chart_5.jpg)

<details>
<summary>line</summary>

| Point | x-coordinate | y-coordinate |
| --- | --- | --- |
| 1 | \(-3\pi\) | \(\pi\) |
| 2 | \(-2\pi\) | \(\pi\) |
| 3 | \(-\pi\) | \(\pi\) |
| 4 | \(\pi\) | \(\pi\) |
| 5 | \(2\pi\) | \(\pi\) |
| 6 | \(3\pi\) | \(\pi\) |
</details>

图12-12

例 5 设  $f(x)$  是周期为  $2\pi$  的周期函数, 它在  $[-\pi, \pi)$  上的表达式为  $f(x) = |x|$ , 将  $f(x)$  展开成傅里叶级数.

解 所给函数满足收敛定理的条件, 它在整个数轴上连续, 因此  $f(x)$  的傅里叶级数处处收敛于  $f(x)$ .

因为 $f(x)$ 是偶函数,所以按公式(7-10),有 $b_{n}=0\quad(n=1,2,3,\cdots)$ ,而

$$
\begin{array}{l} a _ {n} = \frac {2}{\pi} \int_ {0} ^ {\pi} f (x) \cos n x \mathrm{d} x = \frac {2}{\pi} \int_ {0} ^ {\pi} x \cos n x \mathrm{d} x \\ = \frac {2}{\pi} \left[ \frac {x \sin n x}{n} + \frac {\cos n x}{n ^ {2}} \right] _ {0} ^ {\pi} = \frac {2}{\pi n ^ {2}} (\cos n \pi - 1) \\ = \left\{ \begin{array}{l l} - \frac {4}{\pi n ^ {2}}, & n = 1, 3, 5, \dots , \\ 0, & n = 2, 4, 6, \dots ; \end{array} \right. \\ a _ {0} = \frac {2}{\pi} \int_ {0} ^ {\pi} f (x) \mathrm{d} x = \frac {2}{\pi} \int_ {0} ^ {\pi} x \mathrm{d} x = \pi . \\ \end{array}
$$

将求得的系数 $a_{n}$ 代入余弦级数(7-11)，得 $f(x)$ 的傅里叶级数展开式为

$$
\begin{array}{l} f (x) = \frac {\pi}{2} - \frac {4}{\pi} \left(\cos x + \frac {1}{3 ^ {2}} \cos 3 x + \frac {1}{5 ^ {2}} \cos 5 x + \dots + \frac {1}{(2 k - 1) ^ {2}} \cos (2 k - 1) x + \dots\right) \\ = \frac {\pi}{2} - \frac {4}{\pi} \sum_ {k = 1} ^ {\infty} \frac {1}{(2 k - 1) ^ {2}} \cos (2 k - 1) x \quad (- \infty <   x <   + \infty). \\ \end{array}
$$

在实际应用(如研究某种波动问题,热的传导、扩散问题)中,有时还需要把定义

在区间 $[0,\pi]$ 上的函数 $f(x)$ 展开成正弦级数或余弦级数.

根据前面讨论的结果,这类展开问题可以按如下的方法解决:设函数 $f(x)$ 定义在区间 $[0,\pi]$ 上并且满足收敛定理的条件,我们在开区间 $(-π,0)$ 内补充函数 $f(x)$ 的定义,得到定义在 $(-π,\pi]$ 上的函数 $F(x)$,使它在 $(-π,\pi)$ 上成为奇函数①(偶函数).按这种方式拓广函数定义域的过程称为奇延拓(偶延拓).然后将奇延拓(偶延拓)后的函数展开成傅里叶级数,这个级数必定是正弦级数(余弦级数).再限制x在 $(0,\pi]$ 上,此时 $F(x)\equiv f(x)$,这样便得到 $f(x)$ 的正弦级数(余弦级数)展开式.

例如将函数

$$
\varphi (x) = x \quad (0 \leqslant x \leqslant \pi)
$$

作奇延拓,再作周期延拓,便成例4中的函数,按例4的结果,有

$$
x = 2 \sum_ {n = 1} ^ {\infty} \frac {(- 1) ^ {n + 1}}{n} \sin n x \quad (0 \leqslant x <   \pi);
$$

将 $\varphi (x)$ 作偶延拓，再作周期延拓，便成例5中的函数，按例5的结果，有

$$
x = \frac {\pi}{2} - \frac {4}{\pi} \sum_ {k = 1} ^ {\infty} \frac {1}{(2 k - 1) ^ {2}} \cos (2 k - 1) x \quad (0 \leqslant x \leqslant \pi).
$$

例6 将函数

$$
f (x) = \left\{ \begin{array}{l l} \cos x, & 0 \leqslant x <   \frac {\pi}{2}, \\ 0, & \frac {\pi}{2} \leqslant x \leqslant \pi \end{array} \right.
$$

分别展开成正弦级数和余弦级数.

解 先展开成正弦级数.为此对函数 $f(x)$ 作奇延拓(图12-13).按公式(7-8)有

$$
\begin{array}{l} b _ {n} = \frac {2}{\pi} \int_ {0} ^ {\pi} f (x) \sin n x \mathrm{d} x = \frac {2}{\pi} \int_ {0} ^ {\frac {\pi}{2}} \cos x \sin n x \mathrm{d} x \\ = \frac {1}{\pi} \int_ {0} ^ {\frac {\pi}{2}} \left[ \sin (n - 1) x + \sin (n + 1) x \right] \mathrm{d} x \\ = \frac {1}{\pi} \left[ - \frac {1}{n - 1} \cos (n - 1) x - \frac {1}{n + 1} \cos (n + 1) x \right] _ {0} ^ {\frac {\pi}{2}} \\ = \frac {1}{\pi} \left(\frac {1}{n - 1} + \frac {1}{n + 1} - \frac {1}{n - 1} \cos \frac {n - 1}{2} \pi - \frac {1}{n + 1} \cos \frac {n + 1}{2} \pi\right) \\ = \frac {1}{\pi} \left(\frac {2 n}{n ^ {2} - 1} - \frac {1}{n - 1} \sin \frac {n \pi}{2} + \frac {1}{n + 1} \sin \frac {n \pi}{2}\right) \\ \end{array}
$$

![](images/page_310_chart_14.jpg)

<details>
<summary>contour</summary>

| Point | X | Y |
| --- | --- | --- |
| Top-left | 0 | 1 |
| Bottom-left | \(-\pi/2\) | -1 |
| Center | 0 | 0 |
| Right-pointing edge | \(\pi/2\) | 0 |
</details>

图12-13

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 补充 $f(x)$ 的定义使它在 $(-π, π)$ 上成为奇函数时，若 $f(0) ≠ 0$，则规定 $F(0) = 0$.</span></small>

$$
= \frac {2}{\pi (n ^ {2} - 1)} (n - \sin \frac {n \pi}{2}).
$$

以上计算对 n=1 不适合, $b_{1}$  需另行计算:

$$
b _ {1} = \frac {2}{\pi} \int_ {0} ^ {\pi} f (x) \sin x \mathrm{d} x = \frac {2}{\pi} \int_ {0} ^ {\frac {\pi}{2}} \cos x \sin x \mathrm{d} x = \frac {1}{\pi}.
$$

将求得的 $b_{n}$ 代入(7-9)式，得 $f(x)$ 的正弦级数展开式为

$$
f (x) = \frac {1}{\pi} [ \sin x + 2 \sum_ {n = 2} ^ {\infty} \frac {1}{n ^ {2} - 1} (n - \sin \frac {n \pi}{2}) \sin n x ] \quad (0 <   x \leqslant \pi).
$$

在端点 x=0 处级数收敛到零, 它不等于  $f(0)$ .

再展开成余弦级数.为此对函数 $f(x)$ 作偶延拓(图12-14).

按公式(7-10)有

$$
\begin{array}{l} a _ {n} = \frac {2}{\pi} \int_ {0} ^ {\pi} f (x) \cos n x \mathrm{d} x = \frac {2}{\pi} \int_ {0} ^ {\frac {\pi}{2}} \cos x \cos n x \mathrm{d} x \\ = \frac {1}{\pi} \int_ {0} ^ {\frac {\pi}{2}} \left[ \cos (n - 1) x + \cos (n + 1) x \right] \mathrm{d} x \\ = \frac {1}{\pi} \left[ \frac {1}{n - 1} \sin \frac {n - 1}{2} \pi + \frac {1}{n + 1} \sin \frac {n + 1}{2} \pi \right] \\ = \frac {2}{\pi (n ^ {2} - 1)} \sin \frac {n - 1}{2} \pi = \left\{ \begin{array}{l l} 0, & n = 2 k - 1, \\ \frac {2 (- 1) ^ {k - 1}}{\pi (4 k ^ {2} - 1)}, & n = 2 k. \end{array} \right. \\ \end{array}
$$

![](images/page_311_image_10.jpg)

<details>
<summary>text_image</summary>

-π
-π/2
O
1
π/2
π x
y
</details>

图12-14

以上计算对 n=1 不适合, $a_{1}$  需另行计算:

$$
a _ {1} = \frac {2}{\pi} \int_ {0} ^ {\frac {\pi}{2}} \cos^ {2} x \mathrm{d} x = \frac {1}{\pi} \int_ {0} ^ {\frac {\pi}{2}} (1 + \cos 2 x) \mathrm{d} x = \frac {1}{2}.
$$

将求得的 $a_{n}$ 代入(7-11)式, 得 $f(x)$ 的余弦级数展开式为

$$
f (x) = \frac {1}{\pi} + \frac {1}{2} \cos x + \frac {2}{\pi} \sum_ {k = 1} ^ {\infty} \frac {(- 1) ^ {k - 1}}{4 k ^ {2} - 1} \cos 2 k x \quad (0 \leqslant x \leqslant \pi).
$$

利用函数的傅里叶级数展开式,有时可得一些特殊级数的和,例如按例5的结果,有

$$
\mid x \mid = \frac {\pi}{2} - \frac {4}{\pi} \sum_ {k = 1} ^ {\infty} \frac {1}{(2 k - 1) ^ {2}} \cos (2 k - 1) x \quad (- \pi \leqslant x \leqslant \pi),
$$

在上式中令 x=0, 便得

$$
\sum_ {k = 1} ^ {\infty} \frac {1}{(2 k - 1) ^ {2}} = \frac {\pi^ {2}}{8}.
$$

设

$$
\begin{array}{l} \sigma = 1 + \frac {1}{2 ^ {2}} + \frac {1}{3 ^ {2}} + \frac {1}{4 ^ {2}} + \dots + \frac {1}{n ^ {2}} + \dots , \\ \sigma_ {1} = 1 + \frac {1}{3 ^ {2}} + \frac {1}{5 ^ {2}} + \dots + \frac {1}{(2 n - 1) ^ {2}} + \dots \left(= \frac {\pi^ {2}}{8}\right), \\ \sigma_ {2} = \frac {1}{2 ^ {2}} + \frac {1}{4 ^ {2}} + \frac {1}{6 ^ {2}} + \dots + \frac {1}{(2 n) ^ {2}} + \dots , \\ \sigma_ {3} = 1 - \frac {1}{2 ^ {2}} + \frac {1}{3 ^ {2}} - \frac {1}{4 ^ {2}} + \dots + (- 1) ^ {n - 1} \frac {1}{n ^ {2}} + \dots . \\ \end{array}
$$

因为

$$
\sigma_ {2} = \frac {\sigma}{4} = \frac {\sigma_ {1} + \sigma_ {2}}{4},
$$

所以

$$
\sigma_ {2} = \frac {\sigma_ {1}}{3} = \frac {\pi^ {2}}{2 4}, \quad \sigma = \sigma_ {1} + \sigma_ {2} = \frac {\pi^ {2}}{8} + \frac {\pi^ {2}}{2 4} = \frac {\pi^ {2}}{6},
$$

又

$$
\sigma_ {3} = 2 \sigma_ {1} - \sigma = \frac {\pi^ {2}}{4} - \frac {\pi^ {2}}{6} = \frac {\pi^ {2}}{1 2}.
$$

## 习题12-7

1. 下列周期函数 $f(x)$ 的周期为 $2\pi$，试将 $f(x)$ 展开成傅里叶级数，如果 $f(x)$ 在 $[-\pi, \pi)$ 上的表达式为

(1)  $f(x)=3x^{2}+1$  ( $-\pi\leqslant x<\pi$ );
(2) $f(x) = \mathrm{e}^{2x} (-\pi \leqslant x < \pi)$;
(3) $f(x)=\left\{\begin{aligned}&bx, & -\pi \leqslant x<0,\\ &ax, & 0 \leqslant x<\pi\quad(a,b\text{为常数，且}a>b>0).\end{aligned}\right.$

2. 将下列函数 $f(x)$ 展开成傅里叶级数:

(1) $f(x)=2\sin\frac{x}{3}\quad(-\pi\leqslant x\leqslant\pi)$;
(2) $f(x)=\left\{\begin{aligned}e^{x},&-\pi\leqslant x<0,\\ 1,&0\leqslant x\leqslant\pi;\end{aligned}\right.$
(3) $f(x) = x \sin x \quad (-\pi \leqslant x \leqslant \pi)$.

3. 将函数 $f(x) = \cos \frac{x}{2} (-\pi \leqslant x \leqslant \pi)$ 展开成傅里叶级数.

4. 设 $f(x)$ 是周期为 $2\pi$ 的周期函数, 它在 $[-\pi, \pi)$ 上的表达式为

$$
f (x) = \left\{ \begin{array}{l l} - \frac {\pi}{2}, & - \pi \leqslant x <   - \frac {\pi}{2}, \\ x, & - \frac {\pi}{2} \leqslant x <   \frac {\pi}{2}, \\ \frac {\pi}{2}, & \frac {\pi}{2} \leqslant x <   \pi , \end{array} \right.
$$

将 $f(x)$ 展开成傅里叶级数.

5. 将函数 $f(x) = \frac{\pi - x}{2} (0 \leqslant x \leqslant \pi)$ 展开成正弦级数.
6. 将函数 $f(x) = 2x^{2} (0 \leqslant x \leqslant \pi)$ 分别展开成正弦级数和余弦级数.
7. 设周期函数  $f(x)$  的周期为  $2\pi$ . 证明:

(1) 若  $f(x-\pi)=-f(x)$ ，则  $f(x)$  的傅里叶系数  $a_{0}=0, a_{2k}=0, b_{2k}=0 \quad (k=1,2,\cdots)$ ;

(2) 若  $f(x-\pi)=f(x)$ ，则  $f(x)$  的傅里叶系数  $a_{2k+1}=0, b_{2k+1}=0$  ( $k=0,1,2,\cdots$ ).

## 第八节 一般周期函数的傅里叶级数

## 一、周期为 $2l$ 的周期函数的傅里叶级数

上节所讨论的周期函数都是以 $2\pi$ 为周期的,但是实际问题中所遇到的周期函数,它的周期不一定是 $2\pi$.例如上节中提到的矩形波,它的周期是 $T = \frac{2\pi}{\omega}$.因此,本节我们讨论周期为 $2l$ 的周期函数的傅里叶级数.根据上节讨论的结果,经过自变量的变量代换,可得下面的定理:

定理 设周期为 $2l$ 的周期函数 $f(x)$ 满足收敛定理的条件, 则它的傅里叶级数展开式为

$$
f (x) = \frac {a _ {0}}{2} + \sum_ {n = 1} ^ {\infty} \left(a _ {n} \cos \frac {n \pi x}{l} + b _ {n} \sin \frac {n \pi x}{l}\right) \quad (x \in C), \tag {8-1}
$$

其中

$$
\begin{array}{l} \left. \begin{array}{l} a _ {n} = \frac {1}{l} \int_ {- l} ^ {l} f (x) \cos \frac {n \pi x}{l} \mathrm{d} x \quad (n = 0, 1, 2, \dots), \\ b _ {n} = \frac {1}{l} \int_ {- l} ^ {l} f (x) \sin \frac {n \pi x}{l} \mathrm{d} x \quad (n = 1, 2, 3, \dots), \end{array} \right\} \tag {8-2} \\ C = \left\{x   \Big |   f (  x  ) = \frac {1}{2} [ f (  x ^ {-}  ) + f (  x ^ {+}  )   ] \right\}. \\ \end{array}
$$

当 $f(x)$ 为奇函数时，

$$
f (x) = \sum_ {n = 1} ^ {\infty} b _ {n} \sin \frac {n \pi x}{l} \quad (x \in C), \tag {8-3}
$$

其中

$$
b _ {n} = \frac {2}{l} \int_ {0} ^ {l} f (x) \sin \frac {n \pi x}{l} \mathrm{d} x \quad (n = 1, 2, 3, \dots). \tag {8-4}
$$

当 $f(x)$ 为偶函数时，

$$
f (x) = \frac {a _ {0}}{2} + \sum_ {n = 1} ^ {\infty} a _ {n} \cos \frac {n \pi x}{l} \quad (x \in C), \tag {8-5}
$$

其中

$$
a _ {n} = \frac {2}{l} \int_ {0} ^ {l} f (x) \cos \frac {n \pi x}{l} \mathrm{d} x \quad (n = 0, 1, 2, \dots). \tag {8-6}
$$

证 作变量代换 $z = \frac{\pi x}{l}$, 于是区间 $-l \leqslant x \leqslant l$ 就变换成 $-\pi \leqslant z \leqslant \pi$. 设函数 $f(x) = f\left(\frac{lz}{\pi}\right) = F(z)$, 从而 $F(z)$ 是周期为 $2\pi$ 的周期函数, 并且它满足收敛定理的条件, 将 $F(z)$ 展开成傅里叶级数

$$
F (z) = \frac {a _ {0}}{2} + \sum_ {n = 1} ^ {\infty} \left(a _ {n} \cos n z + b _ {n} \sin n z\right),
$$

其中

$$
a _ {n} = \frac {1}{\pi} \int_ {- \pi} ^ {\pi} F (z) \cos n z \mathrm{d} z, \quad b _ {n} = \frac {1}{\pi} \int_ {- \pi} ^ {\pi} F (z) \sin n z \mathrm{d} z.
$$

在以上式子中令 $z = \frac{\pi x}{l}$，并注意到 $F(z) = f(x)$，于是有

$$
f (x) = \frac {a _ {0}}{2} + \sum_ {n = 1} ^ {\infty} \left(a _ {n} \cos \frac {n \pi x}{l} + b _ {n} \sin \frac {n \pi x}{l}\right),
$$

而且

$$
a _ {n} = \frac {1}{l} \int_ {- l} ^ {l} f (x) \cos \frac {n \pi x}{l} \mathrm{d} x, \quad b _ {n} = \frac {1}{l} \int_ {- l} ^ {l} f (x) \sin \frac {n \pi x}{l} \mathrm{d} x.
$$

类似地,可以证明定理的其余部分.

例1 设 $f(x)$ 是周期为4的周期函数, 它在[-2,2)上的表达式为

$$
f (x) = \left\{ \begin{array}{l l} 0, & - 2 \leqslant x <   0, \\ h, & 0 \leqslant x <   2 \end{array} \right. \quad (\text {常数} h \neq 0).
$$

将 $f(x)$ 展开成傅里叶级数,并作出级数的和函数的图形.

解 这时 $l = 2$ ，按公式(8-2)有

$$
\begin{array}{l} a _ {n} = \frac {1}{2} \int_ {0} ^ {2} h \cos \frac {n \pi x}{2} \mathrm{d} x = \left[ \frac {h}{n \pi} \sin \frac {n \pi x}{2} \right] _ {0} ^ {2} = 0 \quad (n \neq 0); \\ a _ {0} = \frac {1}{2} \int_ {- 2} ^ {0} 0 \mathrm{d} x + \frac {1}{2} \int_ {0} ^ {2} h \mathrm{d} x = h; \\ b _ {n} = \frac {1}{2} \int_ {0} ^ {2} h \sin \frac {n \pi x}{2} \mathrm{d} x = \left[ - \frac {h}{n \pi} \cos \frac {n \pi x}{2} \right] _ {0} ^ {2} \\ \end{array}
$$

$$
= \frac {h}{n \pi} (1 - \cos n \pi) = \left\{ \begin{array}{l l} \frac {2 h}{n \pi}, & n = 1, 3, 5, \dots , \\ 0, & n = 2, 4, 6, \dots . \end{array} \right.
$$

将求得的系数 $a_{n}, b_{n}$ 代入(8-1)式, 得

$$
\begin{array}{l} f (x) = \frac {h}{2} + \frac {2 h}{\pi} \left(\sin \frac {\pi x}{2} + \frac {1}{3} \sin \frac {3 \pi x}{2} + \frac {1}{5} \sin \frac {5 \pi x}{2} + \dots + \frac {1}{2 n - 1} \sin \frac {(2 n - 1) \pi x}{2} + \dots\right) \\ (- \infty <   x <   + \infty ; x \neq 0, \pm 2, \pm 4, \dots) \\ \end{array}
$$

级数的和函数的图形如图 12-15 所示.

例2 将如图12-16所示的函数

$$
M (x) = \left\{ \begin{array}{l l} \frac {p x}{2}, & 0 \leqslant x <   \frac {l}{2}, \\ \frac {p (l - x)}{2}, & \frac {l}{2} \leqslant x \leqslant l \end{array} \right.
$$

分别展开成正弦级数和余弦级数.

![](images/page_315_chart_8.jpg)

<details>
<summary>line</summary>

| X | Y |
| --- | --- |
| -2 | 1 |
| -2 | 0 |
| 0 | 0 |
| 0 | 1 |
| 2 | 1 |
| 2 | 0 |
| 2 | 0 |
</details>

图12-15

![](images/page_315_chart_10.jpg)

<details>
<summary>line</summary>

| X | Y |
| --- | --- |
| 0 | 0 |
| l/2 | pl/4 |
| l | 0 |
</details>

图12-16

解 $M(x)$ 是定义在 $[0, l]$ 上的函数, 要将它展开成正弦级数, 必须对 $M(x)$ 进行奇延拓. 按公式(8-4)计算延拓后的函数的傅里叶系数

$$
\begin{array}{l} b _ {n} = \frac {2}{l} \int_ {0} ^ {l} M (x) \sin \frac {n \pi x}{l} \mathrm{d} x \\ = \frac {2}{l} \left[ \int_ {0} ^ {\frac {l}{2}} \frac {p x}{2} \sin \frac {n \pi x}{l} \mathrm{d} x + \int_ {\frac {l}{2}} ^ {l} \frac {p (l - x)}{2} \sin \frac {n \pi x}{l} \mathrm{d} x \right]. \\ \end{array}
$$

对上式右端的第二项,令 t=l-x,则

$$
\begin{array}{l} b _ {n} = \frac {p}{l} \left[ \int_ {0} ^ {\frac {l}{2}} x \sin \frac {n \pi x}{l} \mathrm{d} x + \int_ {\frac {l}{2}} ^ {0} t \sin \frac {n \pi (l - t)}{l} (- \mathrm{d} t) \right] \\ = \frac {p}{l} \left[ \int_ {0} ^ {\frac {l}{2}} x \sin \frac {n \pi x}{l} \mathrm{d} x + (- 1) ^ {n + 1} \int_ {0} ^ {\frac {l}{2}} t \sin \frac {n \pi t}{l} \mathrm{d} t \right]. \\ \end{array}
$$

当 $n = 2k$ 为偶数时，$b_{2k} = 0$；当 $n = 2k - 1$ 为奇数时，

$$
b _ {2 k - 1} = \frac {2 p}{l} \int_ {0} ^ {\frac {l}{2}} x \sin \frac {(2 k - 1) \pi x}{l} \mathrm{d} x = \frac {2 p l}{(2 k - 1) ^ {2} \pi^ {2}} \sin \frac {2 k - 1}{2} \pi .
$$

$$
= \frac {2 p l (- 1) ^ {k - 1}}{(2 k - 1) ^ {2} \pi^ {2}}.
$$

将求得的 $b_{n}$ 代入(8-3)式, 得 $M(x)$ 的正弦级数展开式为

$$
M (x) = \frac {2 p l}{\pi^ {2}} \sum_ {k = 1} ^ {\infty} \frac {(- 1) ^ {k - 1}}{(2 k - 1) ^ {2}} \sin \frac {(2 k - 1) \pi x}{l} \quad (0 \leqslant x \leqslant l).
$$

再求 $M(x)$ 的余弦级数展开式. 为此对 $M(x)$ 作偶延拓, 再作周期延拓. 注意到延拓所得周期函数的周期为 $l$, 知 $M(x)$ 可展开成周期为 $l$ 的余弦级数. 按公式 (8-6) 将 (8-6) 中的 $l$ 换成 $\frac{l}{2}$ 计算傅里叶系数:

$$
\begin{array}{l} a _ {n} = \frac {4}{l} \int_ {0} ^ {\frac {l}{2}} M (x) \cos \frac {2 n \pi x}{l} \mathrm{d} x = \frac {4}{l} \int_ {0} ^ {\frac {l}{2}} \frac {p x}{2} \cos \frac {2 n \pi x}{l} \mathrm{d} x \\ = \frac {2 p}{l} \left[ \frac {l}{2 n \pi} x \sin \frac {2 n \pi x}{l} + \left(\frac {l}{2 n \pi}\right) ^ {2} \cos \frac {2 n \pi x}{l} \right] _ {0} ^ {\frac {l}{2}} \\ = \frac {p l}{2 n ^ {2} \pi^ {2}} (\cos n \pi - 1) = \left\{ \begin{array}{l l} - \frac {p l}{n ^ {2} \pi^ {2}}, & n = 1, 3, 5, \dots , \\ 0, & n = 2, 4, 6, \dots . \end{array} \right. \\ a _ {0} = \frac {4}{l} \int_ {0} ^ {\frac {l}{2}} \frac {p x}{2} \mathrm{d} x = \frac {p l}{4}. \\ \end{array}
$$

将求得的 $a_{n}$ 代入(8-5)式，得

$$
M (x) = \frac {p l}{8} - \frac {p l}{\pi^ {2}} \sum_ {k = 1} ^ {\infty} \frac {1}{(2 k - 1) ^ {2}} \cos \frac {2 (2 k - 1) \pi x}{l} \quad (0 \leqslant x \leqslant l).
$$

## \*二、傅里叶级数的复数形式

傅里叶级数还可以用复数形式表示.在电子技术中,经常应用这种形式.

设周期为 $2l$ 的周期函数 $f(x)$ 的傅里叶级数为

$$
\frac {a _ {0}}{2} + \sum_ {n = 1} ^ {\infty} \left(a _ {n} \cos \frac {n \pi x}{l} + b _ {n} \sin \frac {n \pi x}{l}\right), \tag {8-7}
$$

其中系数 $a_{n}$ 与 $b_{n}$ 为

$$
\left. \begin{array}{l} a _ {n} = \frac {1}{l} \int_ {- l} ^ {l} f (x) \cos \frac {n \pi x}{l} \mathrm{d} x \quad (n = 0, 1, 2, \dots), \\ b _ {n} = \frac {1}{l} \int_ {- l} ^ {l} f (x) \sin \frac {n \pi x}{l} \mathrm{d} x \quad (n = 1, 2, 3, \dots). \end{array} \right\} \tag {8-8}
$$

利用欧拉公式

$$
\cos t = \frac {\mathrm{e} ^ {t i} + \mathrm{e} ^ {- t i}}{2}, \quad \sin t = \frac {\mathrm{e} ^ {t i} - \mathrm{e} ^ {- t i}}{2 \mathrm{i}},
$$

把(8-7)式化为

$$
\begin{array}{l} \frac {a _ {0}}{2} + \sum_ {n = 1} ^ {\infty} \left[ \frac {a _ {n}}{2} \left(\mathrm{e} ^ {\frac {n \pi x}{l} \mathrm{i}} + \mathrm{e} ^ {- \frac {n \pi x}{l} \mathrm{i}}\right) - \frac {b _ {n} \mathrm{i}}{2} \left(\mathrm{e} ^ {\frac {n \pi x}{l} \mathrm{i}} - \mathrm{e} ^ {- \frac {n \pi x}{l} \mathrm{i}}\right) \right] \\ = \frac {a _ {0}}{2} + \sum_ {n = 1} ^ {\infty} \left[ \frac {a _ {n} - b _ {n} \mathrm{i}}{2} \mathrm{e} ^ {\frac {n \pi x}{l} \mathrm{i}} + \frac {a _ {n} + b _ {n} \mathrm{i}}{2} \mathrm{e} ^ {- \frac {n \pi x}{l} \mathrm{i}} \right]. \tag {8-9} \\ \end{array}
$$

记

$$
\frac {a _ {0}}{2} = c _ {0}, \quad \frac {a _ {n} - b _ {n} \mathrm{i}}{2} = c _ {n}, \quad \frac {a _ {n} + b _ {n} \mathrm{i}}{2} = c _ {- n} \quad (n = 1, 2, 3, \dots), \tag {8-10}
$$

则(8-9)式就表示为

$$
c _ {0} + \sum_ {n = 1} ^ {\infty} (c _ {n} \mathrm{e} ^ {\frac {n \pi x}{l} \mathrm{i}} + c _ {- n} \mathrm{e} ^ {- \frac {n \pi x}{l} \mathrm{i}}) = (c _ {n} \mathrm{e} ^ {\frac {n \pi x}{l} \mathrm{i}}) _ {n = 0} + \sum_ {n = 1} ^ {\infty} (c _ {n} \mathrm{e} ^ {\frac {n \pi x}{l} \mathrm{i}} + c _ {- n} \mathrm{e} ^ {- \frac {n \pi x}{l} \mathrm{i}}).
$$

即得傅里叶级数的复数形式为

$$
\sum_ {n = - \infty} ^ {\infty} c _ {n} \mathrm{e} ^ {\frac {n \pi x}{l} \mathrm{i}}. \tag {8-11}
$$

为得出系数 $c_{n}$ 的表达式，把(8-8)式代入(8-10)式，得

$$
\begin{array}{l} c _ {0} = \frac {a _ {0}}{2} = \frac {1}{2 l} \int_ {- l} ^ {l} f (x) \mathrm{d} x; \\ c _ {n} = \frac {a _ {n} - b _ {n} \mathrm{i}}{2} = \frac {1}{2} \left[ \frac {1}{l} \int_ {- l} ^ {l} f (x) \cos \frac {n \pi x}{l} \mathrm{d} x - \frac {\mathrm{i}}{l} \int_ {- l} ^ {l} f (x) \sin \frac {n \pi x}{l} \mathrm{d} x \right] \\ = \frac {1}{2 l} \int_ {- l} ^ {l} f (x) \left(\cos \frac {n \pi x}{l} - \mathrm{i} \sin \frac {n \pi x}{l}\right) \mathrm{d} x \\ = \frac {1}{2 l} \int_ {- l} ^ {l} f (x) \mathrm{e} ^ {- \frac {n \pi x}{l} \mathrm{i}} \mathrm{d} x \quad (n = 1, 2, 3, \dots); \\ \end{array}
$$

$$
c _ {- n} = \frac {a _ {n} + b _ {n} \mathrm{i}}{2} = \frac {1}{2 l} \int_ {- l} ^ {l} f (x) \mathrm{e} ^ {\frac {n \pi x}{l} \mathrm{i}} \mathrm{d} x \quad (n = 1, 2, 3, \dots).
$$

将已得的结果合并写为

$$
c _ {n} = \frac {1}{2 l} \int_ {- l} ^ {l} f (x) \mathrm{e} ^ {- \frac {n \pi x}{l} \mathrm{i}} \mathrm{d} x \quad (n = 0, \pm 1, \pm 2, \dots). \tag {8-12}
$$

这就是傅里叶系数的复数形式.

傅里叶级数的两种形式本质上是一样的,但复数形式比较简洁,且只用一个算式计算系数.

例 3 把宽为  $\tau$ 、高为 h、周期为 T 的矩形波(图 12-17)展开成复数形式的傅里叶级数.

![](images/page_317_chart_17.jpg)

<details>
<summary>line</summary>

| Time (t) | Value (u) |
| --- | --- |
| 0 | 0 |
| ~0.15 | h |
| ~0.35 | h |
| ~0.45 | 0 |
| \(-T/2\) | 0 |
| \(-\tau/2\) | 0 |
| \(+\tau/2\) | h |
| \(\tau/2\) | h |
| \(T/2\) | 0 |
| ~\(T/3\) | h |
| ~\(T/4\) | h |
</details>

图12-17

解 在一个周期 $\left[-\frac{T}{2}, \frac{T}{2}\right)$ 内矩形波的函数表达式为

$$
u (t) = \left\{ \begin{array}{l l} 0, & - \frac {T}{2} \leqslant t <   - \frac {\tau}{2}, \\ h, & - \frac {\tau}{2} \leqslant t <   \frac {\tau}{2}, \\ 0, & \frac {\tau}{2} \leqslant t <   \frac {T}{2}. \end{array} \right.
$$

按公式(8-12)有

$$
\begin{array}{l} c _ {n} = \frac {1}{T} \int_ {- T / 2} ^ {T / 2} u (t) \mathrm{e} ^ {- \frac {2 n \pi t}{T} \mathrm{i}} \mathrm{d} t = \frac {1}{T} \int_ {- \tau / 2} ^ {\tau / 2} h \mathrm{e} ^ {- \frac {2 n \pi t}{T} \mathrm{i}} \mathrm{d} t \\ = \frac {h}{T} \left[ \frac {- T}{2 n \pi \mathrm{i}} \mathrm{e} ^ {- \frac {2 n \pi t}{T} \mathrm{i}} \right] _ {- \tau / 2} ^ {\tau / 2} = \frac {h}{n \pi} \sin \frac {n \pi \tau}{T} \quad (n = \pm 1, \pm 2, \dots), \\ c _ {0} = \frac {1}{T} \int_ {- T / 2} ^ {T / 2} u (t) \mathrm{d} t = \frac {1}{T} \int_ {- \tau / 2} ^ {\tau / 2} h \mathrm{d} t = \frac {h \tau}{T}, \\ \end{array}
$$

将求得的 $c_{n}$ 代入级数(8-11)，得

$$
u(t) = \frac{h\tau}{T} +\frac{h}{\pi}\sum_{\substack{n = -\infty \\ n\neq 0}}^{\infty}\frac{1}{n}\sin \frac{n\pi\tau}{T}\mathrm{e}^{\frac{2n\pi t}{T} \mathrm{i}}\quad \left(-\infty <  t <   + \infty ;t\neq nT\pm \frac{\tau}{2},n = 0,\pm 1, \pm 2,\dots\right).
$$

## 习题12-8

1. 将下列各周期函数展开成傅里叶级数(下面给出函数在一个周期内的表达式):

(1) $f(x) = 1 - x^2 \left( -\frac{1}{2} \leqslant x < \frac{1}{2} \right)$;

(2) $f(x)=\begin{cases}x,&-1\leqslant x<0,\\1,&0\leqslant x<\frac{1}{2},\\-1&\frac{1}{2}\leqslant x<1;\end{cases}$

(3) $f(x)=\begin{cases}2x+1,&-3\leqslant x<0,\\1,&0\leqslant x<3.\end{cases}$

2. 将下列函数分别展开成正弦级数和余弦级数:

(1) $f(x)=\left\{\begin{aligned}x,&0\leqslant x<\frac{l}{2},\\ l-x,&\frac{l}{2}\leqslant x\leqslant l;\end{aligned}\right.$

(2) $f(x) = x^{2}$ $(0\leqslant x\leqslant 2)$

\*3. 设 $f(x)$ 是周期为 2 的周期函数, 它在 $[-1, 1)$ 上的表达式为 $f(x) = \mathrm{e}^{-x}$. 试将 $f(x)$ 展开成复数形式的傅里叶级数.

\* 4. 设 $u\left( t\right)$ 是周期为 $T$ 的周期函数. 已知它的傅里叶级数的复数形式为 (参阅本节例题)

$$
u(t) = \frac{h\tau}{T} +\frac{h}{\pi}\sum_{\substack{n = -\infty \\ n\neq 0}}^{\infty}\frac{1}{n}\sin \frac{n\pi\tau}{T}\mathrm{e}^{\frac{2n\pi t}{T}\mathrm{i}}\quad (-\infty <  t <   + \infty),
$$

试写出 $u(t)$ 的傅里叶级数的实数形式（即三角形式）.

## 总习题十二

1. 填空:

（1）对级数 $\sum_{n=1}^{\infty} u_n, \lim_{n \to \infty} u_n = 0$ 是它收敛的 \_\_\_\_ 条件，不是它收敛的 \_\_\_\_ 条件；
(2) 部分和数列  $\{s_{n}\}$  有界是正项级数  $\sum_{n=1}^{\infty} u_{n}$  收敛的 \_\_\_\_ 条件；
(3) 若级数  $\sum_{n=1}^{\infty}u_{n}$  绝对收敛, 则级数  $\sum_{n=1}^{\infty}u_{n}$  必定 \_\_\_\_; 若级数  $\sum_{n=1}^{\infty}u_{n}$  条件收敛, 则级数  $\sum_{n=1}^{\infty}|u_{n}|$  必定 \_\_\_\_.

2. 下题中给出了四个结论,从中选出一个正确的结论:

设 $f(x)$ 是以 $2\pi$ 为周期的周期函数，它在 $[- \pi, \pi)$ 上的表达式为 $|x|$，则 $f(x)$ 的傅里叶级数为（）.

(A) $\frac{\pi}{2} - \frac{4}{\pi} \left[ \cos x + \frac{1}{3^2} \cos 3x + \frac{1}{5^2} \cos 5x + \cdots + \frac{1}{(2n-1)^2} \cos (2n-1)x + \cdots \right]$
(B)  $\frac{2}{\pi}\left[\frac{1}{2^{2}}\sin 2x+\frac{1}{4^{2}}\sin 4x+\frac{1}{6^{2}}\sin 6x+\cdots+\frac{1}{(2n)^{2}}\sin 2nx+\cdots\right]$
(C)  $\frac{4}{\pi}\left[\cos x+\frac{1}{3^{2}}\cos 3x+\frac{1}{5^{2}}\cos 5x+\cdots+\frac{1}{(2n-1)^{2}}\cos(2n-1)x+\cdots\right]$
(D)  $\frac{1}{\pi}\left[\frac{1}{2^{2}}\cos2x+\frac{1}{4^{2}}\cos4x+\frac{1}{6^{2}}\cos6x+\cdots+\frac{1}{(2n)^{2}}\cos2nx+\cdots\right]$

3. 判定下列级数的收敛性:

(1)  $\sum_{n=1}^{\infty}\frac{1}{n\sqrt[n]{n}};$
(2) $\sum_{n=1}^{\infty}\frac{(n!)^{2}}{2n^{2}};$
(3) $\sum_{n=1}^{\infty} \frac{n \cos^{2} \frac{n\pi}{3}}{2^{n}};$
(4)  $\sum_{n=2}^{\infty}\frac{1}{\ln^{10}n};$
(5) $\sum_{n=1}^{\infty} \frac{a^n}{n^s} \quad (a > 0, s > 0)$.

4. 设正项级数 $\sum_{n=1}^{\infty} u_n$ 和 $\sum_{n=1}^{\infty} v_n$ 都收敛, 证明级数 $\sum_{n=1}^{\infty} (u_n + v_n)^2$ 也收敛.

5. 设级数 $\sum_{n=1}^{\infty} u_n$ 收敛, 且 $\lim_{n \to \infty} \frac{v_n}{u_n} = 1$. 问级数 $\sum_{n=1}^{\infty} v_n$ 是否也收敛? 试说明理由.

6. 讨论下列级数的绝对收敛性与条件收敛性:

(1) $\sum_{n=1}^{\infty}(-1)^{n}\frac{1}{n^{p}}$;

(2) $\sum_{n=1}^{\infty}(-1)^{n+1}\frac{\sin\frac{\pi}{n+1}}{\pi^{n+1}};$