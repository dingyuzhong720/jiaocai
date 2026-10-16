得

$$
\frac {y ^ {2}}{C ^ {2}} - \frac {2 y v}{C} = 1,
$$

以 yv=x 代入上式, 得

$$
y ^ {2} = 2 C \left(x + \frac {C}{2}\right).
$$

这是以 x 轴为对称轴、焦点在原点的抛物线.

## \*二、可化为齐次的方程

方程

$$
\frac {\mathrm{d} y}{\mathrm{d} x} = \frac {a x + b y + c}{a _ {1} x + b _ {1} y + c _ {1}} \tag {3-3}
$$

当 $c = c_{1} = 0$ 时是齐次的，否则不是齐次的.在非齐次的情形，可用下列变换把它化为齐次方程:令

$$
x = X + h, \quad y = Y + k,
$$

其中 $h$ 及 $k$ 是待定的常数.于是

$$
\mathrm{d} x = \mathrm{d} X, \quad \mathrm{d} y = \mathrm{d} Y,
$$

从而方程(3-3)成为

$$
\frac {\mathrm{d} Y}{\mathrm{d} X} = \frac {a X + b Y + a h + b k + c}{a _ {1} X + b _ {1} Y + a _ {1} h + b _ {1} k + c _ {1}}.
$$

如果方程组

$$
\left\{ \begin{array}{l} a h + b k + c = 0, \\ a _ {1} h + b _ {1} k + c _ {1} = 0 \end{array} \right.
$$

的系数行列式 $\begin{vmatrix}a&b\\ a_{1}&b_{1}\end{vmatrix}\neq0$ ,即 $\frac{a_{1}}{a}\neq\frac{b_{1}}{b}$ ,那么可以定出h及k使它们满足上述方程组.这样,方程(3-3)便化为齐次方程

$$
\frac {\mathrm{d} Y}{\mathrm{d} X} = \frac {a X + b Y}{a _ {1} X + b _ {1} Y}.
$$

求出这齐次方程的通解后,在通解中以 x-h 代 X,y-k 代 Y,便得方程(3-3)的通解.

当 $\frac{a_1}{a} = \frac{b_1}{b}$ 时，$h$ 及 $k$ 无法求得，因此上述方法不能应用.但这时令 $\frac{a_1}{a} = \frac{b_1}{b} = \lambda$ ，从而方程(3-3)可写成

$$
\frac {\mathrm{d} y}{\mathrm{d} x} = \frac {a x + b y + c}{\lambda (a x + b y) + c _ {1}}.
$$

引入新变量  $v=ax+by$ ，则

$$
\frac {\mathrm{d} v}{\mathrm{d} x} = a + b   \frac {\mathrm{d} y}{\mathrm{d} x} \quad \text {或} \quad \frac {\mathrm{d} y}{\mathrm{d} x} = \frac {1}{b} \left(\frac {\mathrm{d} v}{\mathrm{d} x} - a\right).
$$

于是方程(3-3)成为

$$
\frac {1}{b} \left(\frac {\mathrm{d} v}{\mathrm{d} x} - a\right) = \frac {v + c}{\lambda v + c _ {1}},
$$

这是可分离变量的方程.

以上所介绍的方法可以应用于更一般的方程

$$
\frac {\mathrm{d} y}{\mathrm{d} x} = f \left(\frac {a x + b y + c}{a _ {1} x + b _ {1} y + c _ {1}}\right).
$$

例3 解方程

$$
(2 x + y - 4) \mathrm{d} x + (x + y - 1) \mathrm{d} y = 0.
$$

解 所给方程属方程(3-3)的类型. 令 $x = X + h, y = Y + k$, 则 $\mathrm{dx} = \mathrm{d}X, \mathrm{dy} = \mathrm{d}Y$, 代入原方程得

$$
(2 X + Y + 2 h + k - 4) \mathrm{d} X + (X + Y + h + k - 1) \mathrm{d} Y = 0.
$$

解方程组

$$
\left\{ \begin{array}{l} 2 h + k - 4 = 0, \\ h + k - 1 = 0. \end{array} \right.
$$

得 $h = 3, k = -2$. 令 $x = X + 3, y = Y - 2$, 原方程成为

$$
(2 X + Y) \mathrm{d} X + (X + Y) \mathrm{d} Y = 0,
$$

或

$$
\frac {\mathrm{d} Y}{\mathrm{d} X} = - \frac {2 X + Y}{X + Y} = - \frac {2 + \frac {Y}{X}}{1 + \frac {Y}{X}},
$$

这是齐次方程.

令 $\frac{Y}{X}=u$ ，则 $Y=Xu,\frac{dY}{dX}=u+X\frac{du}{dX}$ ，于是方程变为

$$
u + X \frac {\mathrm{d} u}{\mathrm{d} X} = - \frac {2 + u}{1 + u},
$$

或

$$
X \frac {\mathrm{d} u}{\mathrm{d} X} = - \frac {2 + 2 u + u ^ {2}}{1 + u}.
$$

分离变量得

$$
- \frac {u + 1}{u ^ {2} + 2 u + 2} \mathrm{d} u = \frac {\mathrm{d} X}{X}.
$$

积分得

$$
\ln C _ {1} - \frac {1}{2} \ln (u ^ {2} + 2 u + 2) = \ln | X |,
$$

于是

$$
\frac {C _ {1}}{\sqrt {u ^ {2} + 2 u + 2}} = | X |,
$$

或

$$
C _ {2} = X ^ {2} (u ^ {2} + 2 u + 2) \quad (C _ {2} = C _ {1} ^ {2}),
$$

即

$$
Y ^ {2} + 2 X Y + 2 X ^ {2} = C _ {2}.
$$

以 $X = x - 3, Y = y + 2$ 代入上式并化简，得

$$
2 x ^ {2} + 2 x y + y ^ {2} - 8 x - 2 y = C \quad (C = C _ {2} - 1 0).
$$

## 习题7-3

1. 求下列齐次方程的通解:

(1) $xy'-y-\sqrt{y^{2}-x^{2}}=0;$
(2) $x\frac{dy}{dx}=y\ln\frac{y}{x};$
(3) $(x^{2}+y^{2})dx-xydy=0;$
(4) $(x^{3}+y^{3})\mathrm{d}x-3xy^{2}\mathrm{d}y=0;$
(5) $\left(2x\sin\frac{y}{x}+3y\cos\frac{y}{x}\right)\mathrm{d}x-3x\cos\frac{y}{x}\mathrm{d}y=0;$
(6) $(1 + 2\mathrm{e}^{x / y})\mathrm{d}x + 2\mathrm{e}^{x / y}\left(1 - \frac{x}{y}\right)\mathrm{d}y = 0.$

2. 求下列齐次方程满足所给初值条件的特解:

(1) $(y^{2}-3x^{2})\mathrm{d}y+2xy\mathrm{d}x=0,y\mid_{x=0}=1;$
(2) $y' = \frac{x}{y} + \frac{y}{x}, y \mid_{x=1} = 2;$
(3) $(x^{2}+2xy-y^{2})\mathrm{d}x+(y^{2}+2xy-x^{2})\mathrm{d}y=0,y\mid_{x=1}=1;$
(4) $x\frac{\mathrm{dy}}{\mathrm{dx}} = y + x\sec \frac{y}{x},y\mid_{x = 1} = \frac{\pi}{4}.$

3. 设有连接点 $O(0,0)$ 和 $A(1,1)$ 的一段向上凸的曲线弧 $\widehat{OA}$, 对于 $\widehat{OA}$ 上任一点 $P(x,y)$, 曲线弧 $\widehat{OP}$ 与直线段 $\overline{OP}$ 所围图形的面积为 $x^2$, 求曲线弧 $\widehat{OA}$ 的方程.

\* 4. 化下列方程为齐次方程,并求出通解:

(1) $(2x-5y+3)\mathrm{d}x-(2x+4y-6)\mathrm{d}y=0;$
(2) $(x-y-1)\mathrm{d}x+(4y+x-1)\mathrm{d}y=0;$
(3) $(3y-7x+7)\mathrm{d}x+(7y-3x+3)\mathrm{d}y=0;$
(4) $(x+y)\mathrm{d}x+(3x+3y-4)\mathrm{d}y=0,$

## 第四节 一阶线性微分方程

## 一、线性方程

方程

$$
\frac {\mathrm{d} y}{\mathrm{d} x} + P (x) y = Q (x) \tag {4-1}
$$

叫做一阶线性微分方程,因为它对于未知函数 y 及其导数是一次方程.如果  $Q(x) \equiv 0$ , 那么方程(4-1)称为齐次的;如果  $Q(x) \neq 0$ ,那么方程(4-1)称为非齐次的.

设(4-1)为非齐次线性方程.为了求出非齐次线性方程(4-1)的解,我们先把 $Q(x)$ 换成零而写出方程

$$
\frac {\mathrm{d} y}{\mathrm{d} x} + P (x) y = 0. \tag {4-2}
$$

方程(4-2)叫做对应于非齐次线性方程(4-1)的齐次线性方程.方程(4-2)是可分离变量的,分离变量后得

$$
\frac {\mathrm{d} y}{y} = - P (x) \mathrm{d} x,
$$

两端积分,得

$$
\ln | y | = - \int P (x)   \mathrm{d} x + C _ {1},
$$

或

$$
y = C \mathrm{e} ^ {- \int P (x) \mathrm{d} x} \quad (C = \pm \mathrm{e} ^ {C _ {1}}),
$$

这是对应的齐次线性方程(4-2)的通解①.

现在我们使用所谓常数变易法来求非齐次线性方程(4-1)的通解.这方法是把(4-2)的通解中的 $C$ 换成 $x$ 的未知函数 $u(x)$ ，即作变换

$$
y = u \mathrm{e} ^ {- \int P (x) \mathrm{d} x}, \tag {4-3}
$$

于是

$$
\frac {\mathrm{d} y}{\mathrm{d} x} = u ^ {\prime} \mathrm{e} ^ {- \int P (x) \mathrm{d} x} - u P (x) \mathrm{e} ^ {- \int P (x) \mathrm{d} x}. \tag {4-4}
$$

将(4-3)和(4-4)代入方程(4-1)得

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 这里记号  $\int P(x)dx$  表示  $P(x)$  的某个确定的原函数.</span></small>

$$
u ^ {\prime} \mathrm{e} ^ {- \int P (x) \mathrm{d} x} - u P (x) \mathrm{e} ^ {- \int P (x) \mathrm{d} x} + P (x) u \mathrm{e} ^ {- \int P (x) \mathrm{d} x} = Q (x),
$$

即

$$
u ^ {\prime} \mathrm{e} ^ {- \int P (x) \mathrm{d} x} = Q (x), u ^ {\prime} = Q (x) \mathrm{e} ^ {\int P (x) \mathrm{d} x}.
$$

两端积分,得

$$
u = \int Q (x) \mathrm{e} ^ {\int P (x) \mathrm{d} x} \mathrm{d} x + C.
$$

把上式代入(4-3)，便得非齐次线性方程(4-1)的通解

$$
y = \mathrm{e} ^ {- \int P (x) \mathrm{d} x} \left[ \int Q (x) \mathrm{e} ^ {\int P (x) \mathrm{d} x} \mathrm{d} x + C \right]. \tag {4-5}
$$

将(4-5)式改写成两项之和

$$
y = C \mathrm{e} ^ {- \int P (x) \mathrm{d} x} + \mathrm{e} ^ {- \int P (x) \mathrm{d} x} \int Q (x) \mathrm{e} ^ {\int P (x) \mathrm{d} x} \mathrm{d} x,
$$

上式右端第一项是对应的齐次线性方程(4-2)的通解,第二项是非齐次线性方程(4-1)的一个特解(在(4-1)的通解(4-5)中取C=0便得到这个特解).由此可知,一阶非齐次线性方程的通解等于对应的齐次方程的通解与非齐次方程的一个特解之和.

例1 求方程

$$
\frac {\mathrm{d} y}{\mathrm{d} x} - \frac {2 y}{x + 1} = (x + 1) ^ {\frac {5}{2}}
$$

的通解.

解 这是一个非齐次线性方程. 先求对应的齐次方程的通解.

$$
\frac {\mathrm{d} y}{\mathrm{d} x} - \frac {2}{x + 1} y = 0,
$$

$$
\frac {\mathrm{d} y}{y} = \frac {2 \mathrm{d} x}{x + 1},
$$

$$
\ln | y | = 2 \ln | x + 1 | + C _ {1},
$$

$$
y = C (x + 1) ^ {2} (C = \pm \mathrm{e} ^ {C _ {1}}).
$$

用常数变易法, 把 C 换成 u, 即令

$$
y = u (x + 1) ^ {2}, \tag {4-6}
$$

那么

$$
\frac {\mathrm{d} y}{\mathrm{d} x} = u ^ {\prime} (x + 1) ^ {2} + 2 u (x + 1),
$$

代入所给非齐次方程,得

$$
u ^ {\prime} = (x + 1) ^ {\frac {1}{2}}.
$$

两端积分,得

![](images/page_324_image_26.jpg)

释疑解难

7-3

$$
u = \frac {2}{3} (x + 1) ^ {\frac {3}{2}} + C.
$$

再把上式代入(4-6)式,即得所求方程的通解为

$$
y = (x + 1) ^ {2} \left[ \frac {2}{3} (x + 1) ^ {\frac {3}{2}} + C \right].
$$

例 2 有一个电路如图 7-5 所示, 其中电源电动势为  $E = E_{m} \sin \omega t$  ( $E_{m}, \omega$  都是常量), 电阻 R 和电感 L 都是常量. 求电流  $i(t)$ .

解 （i）列方程 由电学知道, 当电流变化时,
L 上有感应电动势  $-L \frac{di}{dt}$ . 由回路电压定律得出

$$
E - L \frac {\mathrm{d} i}{\mathrm{d} t} - i R = 0,
$$

即

$$
\frac {\mathrm{d} i}{\mathrm{d} t} + \frac {R}{L} i = \frac {E}{L}.
$$

把  $E=E_{m}\sin\omega t$  代入上式, 得

$$
\frac {\mathrm{d} i}{\mathrm{d} t} + \frac {R}{L} i = \frac {E _ {\mathrm{m}}}{L} \sin \omega t. \tag {4-7}
$$

未知函数 $i(t)$ 应满足方程(4-7). 此外, 设开关 S 闭合的时刻为 $t = 0$, 这时 $i(t)$ 还应该满足初值条件

$$
i \mid_ {t = 0} = 0. \tag {4-8}
$$

(ii) 解方程 方程(4-7)是一个非齐次线性方程. 可以先求出对应的齐次方程的通解, 然后用常数变易法求非齐次方程的通解. 但是, 也可以直接应用通解公式(4-5)来求解. 这里 $P(t) = \frac{R}{L}, Q(t) = \frac{E_{\mathrm{m}}}{L} \sin \omega t$, 代入公式(4-5), 得

$$
i (t) = \mathrm{e} ^ {- \frac {R}{L} t} \left(\int \frac {E _ {\mathrm{m}}}{L} \mathrm{e} ^ {\frac {R}{L} t} \sin \omega t \mathrm{d} t + C\right).
$$

应用分部积分法,得

$$
\int \mathrm{e} ^ {\frac {R}{L} t} \sin \omega t \mathrm{d} t = \frac {\mathrm{e} ^ {\frac {R}{L} t}}{R ^ {2} + \omega^ {2} L ^ {2}} (R L \sin \omega t - \omega L ^ {2} \cos \omega t),
$$

将上式代入前式并化简,得方程(4-7)的通解

$$
i (t) = \frac {E _ {\mathrm{m}}}{R ^ {2} + \omega^ {2} L ^ {2}} (R \sin \omega t - \omega L \cos \omega t) + C \mathrm{e} ^ {- \frac {R}{L} t},
$$

其中 C 为任意常数.

将初值条件(4-8)代入上式,得

![](images/page_325_image_21.jpg)

<details>
<summary>text_image</summary>

R
L
E
S
</details>

图7-5

$$
C = \frac {\omega L E _ {\mathrm{m}}}{R ^ {2} + \omega^ {2} L ^ {2}},
$$

因此,所求函数  $i(t)$  为

$$
i (t) = \frac {\omega L E _ {\mathrm{m}}}{R ^ {2} + \omega^ {2} L ^ {2}} \mathrm{e} ^ {- \frac {R}{L} t} + \frac {E _ {\mathrm{m}}}{R ^ {2} + \omega^ {2} L ^ {2}} (R \sin \omega t - \omega L \cos \omega t). \tag {4-9}
$$

为了便于说明(4-9)式所反映的物理现象,下面把 $i(t)$ 中第二项的形式稍加改变.令

$$
\cos \varphi = \frac {R}{\sqrt {R ^ {2} + \omega^ {2} L ^ {2}}}, \quad \sin \varphi = \frac {\omega L}{\sqrt {R ^ {2} + \omega^ {2} L ^ {2}}},
$$

于是(4-9)式可写成

$$
i (t) = \frac {\omega L E _ {\mathrm{m}}}{R ^ {2} + \omega^ {2} L ^ {2}} \mathrm{e} ^ {- \frac {R}{L} t} + \frac {E _ {\mathrm{m}}}{\sqrt {R ^ {2} + \omega^ {2} L ^ {2}}} \sin (\omega t - \varphi),
$$

其中

$$
\varphi = \arctan \frac {\omega L}{R}.
$$

当 t 增大时, 上式右端第一项(叫做暂态电流)逐渐衰减而趋于零; 第二项(叫做稳态电流)是正弦函数, 它的周期和电动势的周期相同而相角落后  $\varphi$ .

在上节中,对于齐次方程  $y' = f \left( \frac{y}{x} \right)$ , 我们通过变量代换 y = xu, 把它化为变量可分离的方程, 然后分离变量, 经积分求得通解. 在本节中, 对于一阶非齐次线性方程

$$
y ^ {\prime} + P (x) y = Q (x),
$$

我们通过解对应的齐次线性方程找到变量代换

$$
y = u \mathrm{e} ^ {- \int P (x) \mathrm{d} x},
$$

利用这一代换,把非齐次线性方程化为变量可分离的方程,然后经积分求得通解.

利用变量代换(因变量的变量代换或自变量的变量代换)把一个微分方程化为变量可分离的方程,或化为已经知其求解步骤的方程,这是解微分方程最常用的方法.下面再举一个例子.

例3 解方程 $\frac{\mathrm{dy}}{\mathrm{dx}} = \frac{1}{x + y}$.

解 若把所给方程变形为

$$
\frac {\mathrm{d} x}{\mathrm{d} y} = x + y,
$$

即为一阶线性方程,则按一阶线性方程的解法可求得通解.

也可用变量代换来解所给方程. 令 $x + y = u$，则 $y = u - x, \frac{\mathrm{d}y}{\mathrm{d}x} = \frac{\mathrm{d}u}{\mathrm{d}x} - 1.$ 代入原方程，得

$$
\frac {\mathrm{d} u}{\mathrm{d} x} - 1 = \frac {1}{u}, \quad \frac {\mathrm{d} u}{\mathrm{d} x} = \frac {u + 1}{u}.
$$

分离变量得

$$
\frac {u}{u + 1} \mathrm{d} u = \mathrm{d} x,
$$

两端积分得

$$
u - \ln | u + 1 | = x + C _ {1}.
$$

以  $u=x+y$  代入上式, 即得

$$
y - \ln | x + y + 1 | = C _ {1},
$$

或

$$
x = C \mathrm{e} ^ {y} - y - 1 \quad (C = \pm \mathrm{e} ^ {- C _ {1}}).
$$

在以上求解过程中, 假定了 $u + 1 \neq 0$, 即 $x + y + 1 \neq 0$. 事实上, $x + y + 1 = 0$ 也是方程的解. 为了补充这个失去的解, 在 $C = \pm \mathrm{e}^{C_1} \neq 0$ 中, 补充 $C = 0$, 即

$$
x = C \mathrm{e} ^ {y} - y - 1,
$$

其中 C 为任意常数.

## \* 二、伯努利方程

方程

$$
\frac {\mathrm{d} y}{\mathrm{d} x} + P (x) y = Q (x) y ^ {n} \quad (n \neq 0, 1) \tag {4-10}
$$

叫做伯努利(Bernoulli)方程.当 $n = 0$ 或 $n = 1$ 时，这是线性微分方程.当 $n\neq 0$ ，且 $n\neq 1$ 时，这方程不是线性的，但是通过变量的代换，便可把它化为线性的.事实上，以 $\gamma^n$ 除方程(4-10)的两端，得

$$
y ^ {- n} \frac {\mathrm{d} y}{\mathrm{d} x} + P (x) y ^ {1 - n} = Q (x). \tag {4-11}
$$

容易看出,上式左端第一项与 $\frac{\mathrm{d}}{\mathrm{d}x}(y^{1-n})$ 只差一个常数因子1-n,因此我们引入新的因变量

$$
z = y ^ {1 - n},
$$

那么

$$
\frac {\mathrm{d} z}{\mathrm{d} x} = (1 - n) y ^ {- n} \frac {\mathrm{d} y}{\mathrm{d} x}.
$$

用(1-n)乘方程(4-11)的两端,再通过上述代换便得线性方程

$$
\frac {\mathrm{d} z}{\mathrm{d} x} + (1 - n) P (x) z = (1 - n) Q (x).
$$

求出这方程的通解后,以  $y^{1-n}$  代换 z 便得到伯努利方程的通解.

例4 求方程

$$
\frac {\mathrm{d} y}{\mathrm{d} x} + \frac {y}{x} = a (\ln x) y ^ {2}
$$

的通解.

解 以 $y^{2}$ 除方程的两端, 得

$$
y ^ {- 2} \frac {\mathrm{d} y}{\mathrm{d} x} + \frac {1}{x} y ^ {- 1} = a \ln x,
$$

即

$$
- \frac {\mathrm{d} (y ^ {- 1})}{\mathrm{d} x} + \frac {1}{x} y ^ {- 1} = a \ln x.
$$

令 $z = y^{-1}$ ，则上述方程成为

$$
\frac {\mathrm{d} z}{\mathrm{d} x} - \frac {1}{x} z = - a \ln x.
$$

这是一个线性方程,它的通解为

$$
z = x \left[ C - \frac {a}{2} (\ln x) ^ {2} \right].
$$

以 $y^{-1}$ 代 $z$ ，得所求方程的通解为

$$
y x \left[ C - \frac {a}{2} (\ln x) ^ {2} \right] = 1.
$$

## 习题7-4

1. 求下列微分方程的通解:

(1) $\frac{\mathrm{dy}}{\mathrm{dx}} + y = \mathrm{e}^{-x}$;

(2) $xy' + y = x^2 + 3x + 2$;

(3)  $y' + y \cos x = e^{-\sin x}$ ;

(4) $y' + y \tan x = \sin 2x$;

(5) $(x^{2}-1)y'+2xy-\cos x=0;$

(6) $\frac{d\rho}{d\theta}+3\rho=2;$

(7) $\frac{\mathrm{dy}}{\mathrm{dx}} + 2xy = 4x$;

(8)  $y \ln y \, dx + (x - \ln y) \, dy = 0;$

(9) $(x-2)\frac{\mathrm{d}y}{\mathrm{d}x}=y+2(x-2)^{3};$

(10) $(y^{2}-6x)\frac{\mathrm{d}y}{\mathrm{d}x}+2y=0.$

2. 求下列微分方程满足所给初值条件的特解:

(1) $\frac{\mathrm{dy}}{\mathrm{dx}} - y\tan x = \sec x,y\big|_{x = 0} = 0;$

(2) $\frac{\mathrm{dy}}{\mathrm{dx}} + \frac{y}{x} = \frac{\sin x}{x}, y\big|_{x = \pi} = 1;$

(3) $\frac{\mathrm{d}y}{\mathrm{d}x} + y\cot x = 5\mathrm{e}^{\cos x}, y\mid_{x = \frac{\pi}{2}} = -4;$

(4) $\frac{\mathrm{dy}}{\mathrm{dx}} + 3y = 8, y\big|_{x=0} = 2;$

(5) $\frac{\mathrm{dy}}{\mathrm{dx}} + \frac{2 - 3x^2}{x^3} y = 1, y \mid_{x=1} = 0;$

(6) $x(1 + x^{2})y^{\prime} + y = 1 + x^{2},y\mid_{x = 1} = 0.$

3. 若曲线通过原点, 并且它在点 $(x, y)$ 处的切线斜率等于 $2x + y$, 求这曲线的方程.

4. 设有一质量为 $m$ 的质点做直线运动. 从速度等于零的时刻起, 有一个与运动方向一致、大小与时间成正比 (比例系数为 $k_{1}$) 的力作用于它, 此外还受一与速度成正比 (比例系数为 $k_{2}$) 的阻力作用. 求质点运动的速度与时间的函数关系.

5. 设有一个由电阻 $R = 10 \Omega$、电感 $L = 2 \mathrm{H}$ 和电源电压 $E = 20 \sin 5 t \mathrm{~V}$ 串联组成的电路。开关 S 合上后，电路中有电流通过。求电流 $i$ 与时间 $t$ 的函数关系。

6. 验证形如 $yf(xy) \, \mathrm{d}x + xg(xy) \, \mathrm{d}y = 0$ 的微分方程可经变量代换 $v = xy$ 化为可分离变量的方程，并求其通解.

7. 用适当的变量代换将下列方程化为可分离变量的方程, 然后求出通解:

(1) $\frac{\mathrm{dy}}{\mathrm{dx}} = (x + y)^2$;

(2) $\frac{\mathrm{dy}}{\mathrm{dx}} = \frac{1}{x - y} + 1$;

(3)  $xy' + y = y (\ln x + \ln y)$ ;

(4) $y' = y^2 + 2(\sin x - 1)y + \sin^2 x - 2\sin x - \cos x + 1$;

(5)  $y(xy+1)\mathrm{d}x+x(1+xy+x^{2}y^{2})\mathrm{d}y=0.$

\*8. 求下列伯努利方程的通解:

(1)  $\frac{dy}{dx} + y = y^{2} (\cos x - \sin x)$ ;

(2) $\frac{\mathrm{dy}}{\mathrm{dx}} - 3xy = xy^2$;

(3) $\frac{dy}{dx}+\frac{1}{3}y=\frac{1}{3}(1-2x)y^{4};$

(4) $\frac{\mathrm{dy}}{\mathrm{dx}} - y = xy^5$;

(5)  $x \, dy - [y + xy^{3}(1 + \ln x)] \, dx = 0.$

## 第五节 可降阶的高阶微分方程

从这一节起我们将讨论二阶及二阶以上的微分方程,即所谓高阶微分方程.对于有些高阶微分方程,我们可以通过代换将它化成较低阶的方程来求解.以二阶微分方程

$$
y ^ {\prime \prime} = f (x, y, y ^ {\prime}) \tag {5-1}
$$

而论,如果我们能设法作代换把它从二阶降至一阶,那么就有可能应用前面几节中所讲的方法来求出它的解了.

下面介绍三种容易降阶的高阶微分方程的求解方法.

## 一、 $y^{(n)}=f(x)$ 型的微分方程

微分方程

$$
y ^ {(n)} = f (x) \tag {5-2}
$$

的右端仅含有自变量 $x$. 容易看出, 只要把 $y^{(n-1)}$ 作为新的未知函数, 那么 (5-2) 式就是

新未知函数的一阶微分方程.两边积分,就得到一个n-1阶的微分方程

$$
y ^ {(n - 1)} = \int f (x)   \mathrm{d} x + C _ {1}.
$$

同理可得

$$
y ^ {(n - 2)} = \int \left[ \int f (x) \mathrm{d} x + C _ {1} \right] \mathrm{d} x + C _ {2}.
$$

依此法继续进行,接连积分 n 次,便得方程(5-2)的含有 n 个任意常数的通解.

例1 求微分方程

$$
y ^ {\prime \prime \prime} = \mathrm{e} ^ {2 x} - \cos x
$$

的通解.

解 对所给方程接连积分三次, 得

$$
\begin{array}{l} y ^ {\prime \prime} = \frac {1}{2} \mathrm{e} ^ {2 x} - \sin x + C, \\ y ^ {\prime} = \frac {1}{4} \mathrm{e} ^ {2 x} + \cos x + C x + C _ {2}, \\ y = \frac {1}{8} \mathrm{e} ^ {2 x} + \sin x + C _ {1} x ^ {2} + C _ {2} x + C _ {3} \quad \left(C _ {1} = \frac {C}{2}\right), \\ \end{array}
$$

这就是所求的通解.

例 2 质量为 m 的质点受力 F 的作用沿 x 轴做直线运动. 设力  $F = F(t)$  在开始时刻 t = 0 时  $F(0) = F_{0}$ ，随着时间 t 的增大，力 F 均匀地减小，直到 t = T 时， $F(T) = 0$ . 如果开始时质点位于原点，且初速度为零，求这质点的运动规律.

解 设  $x=x(t)$  表示在时刻 t 时质点的位置, 根据牛顿第二定律, 质点运动的微分方程为

$$
m \frac {\mathrm{d} ^ {2} x}{\mathrm{d} t ^ {2}} = F (t). \tag {5-3}
$$

由题设,力  $F(t)$  随 t 增大而均匀地减小,且 t=0 时, $F(0)=F_{0}$ ,所以  $F(t)=F_{0}-kt$ ;又当 t=T 时, $F(T)=0$ ,从而

$$
F (t) = F _ {0} \left(1 - \frac {t}{T}\right).
$$

于是方程(5-3)可以写成

$$
\frac {\mathrm{d} ^ {2} x}{\mathrm{d} t ^ {2}} = \frac {F _ {0}}{m} \left(1 - \frac {t}{T}\right). \tag {5-4}
$$

其初值条件为

$$
x \mid_ {t = 0} = 0, \quad \frac {\mathrm{d} x}{\mathrm{d} t} \Bigg | _ {t = 0} = 0.
$$

把(5-4)式两端积分,得

$$
\frac {\mathrm{d} x}{\mathrm{d} t} = \frac {F _ {0}}{m} \int \left(1 - \frac {t}{T}\right) \mathrm{d} t,
$$

即

$$
\frac {\mathrm{d} x}{\mathrm{d} t} = \frac {F _ {0}}{m} \left(t - \frac {t ^ {2}}{2 T}\right) + C _ {1}. \tag {5-5}
$$

将条件 $\frac{dx}{dt}\bigg|_{t=0}=0$ 代入(5-5)式,得

$$
C _ {1} = 0,
$$

于是(5-5)式成为

$$
\frac {\mathrm{d} x}{\mathrm{d} t} = \frac {F _ {0}}{m} \left(t - \frac {t ^ {2}}{2 T}\right). \tag {5-6}
$$

把(5-6)式两端积分,得

$$
x = \frac {F _ {0}}{m} \left(\frac {t ^ {2}}{2} - \frac {t ^ {3}}{6 T}\right) + C _ {2},
$$

将条件 $x\mid_{t = 0} = 0$ 代入上式，得

$$
C _ {2} = 0.
$$

于是所求质点的运动规律为

$$
x = \frac {F _ {0}}{m} \left(\frac {t ^ {2}}{2} - \frac {t ^ {3}}{6 T}\right), \quad 0 \leqslant t \leqslant T.
$$

## 二、 $y''=f(x,y')$ 型的微分方程

方程

$$
y ^ {\prime \prime} = f (x, y ^ {\prime}) \tag {5-7}
$$

的右端不显含未知函数 $y$. 如果我们设 $y' = p$, 那么

$$
y ^ {\prime \prime} = \frac {\mathrm{d} p}{\mathrm{d} x} = p ^ {\prime},
$$

而方程(5-7)就成为

$$
p ^ {\prime} = f (x, p).
$$

这是一个关于变量 $x, p$ 的一阶微分方程. 设其通解为

$$
p = \varphi (x, C _ {1})  ,
$$

但是 $p = \frac{\mathrm{dy}}{\mathrm{dx}}$ ，因此又得到一个一阶微分方程

$$
\frac {\mathrm{d} y}{\mathrm{d} x} = \varphi (x, C _ {1}).
$$

对它进行积分,便得方程(5-7)的通解为

$$
y = \int \varphi (x, C _ {1}) \mathrm{d} x + C _ {2}.
$$

例3 求微分方程

$$
(1 + x ^ {2}) y ^ {\prime \prime} = 2 x y ^ {\prime}
$$

满足初值条件

$$
y \mid_ {x = 0} = 1, \quad y ^ {\prime} \mid_ {x = 0} = 3
$$

的特解.

解 所给方程是 $y'' = f(x, y')$ 型的. 设 $y' = p$，代入方程并分离变量后，有

$$
\frac {\mathrm{d} p}{p} = \frac {2 x}{1 + x ^ {2}} \mathrm{d} x.
$$

两端积分,得

$$
\ln | p | = \ln (1 + x ^ {2}) + C,
$$

即

$$
p = y ^ {\prime} = C _ {1} (1 + x ^ {2}) \quad (C _ {1} = \pm \mathrm{e} ^ {c}).
$$

由条件 $y^{\prime}\mid_{x = 0} = 3$ ，得

$$
C _ {1} = 3,
$$

所以

$$
y ^ {\prime} = 3 (1 + x ^ {2}).
$$

两端再积分,得

$$
y = x ^ {3} + 3 x + C _ {2}.
$$

又由条件 $y\mid_{x = 0} = 1$ ，得

$$
C _ {2} = 1,
$$

于是所求的特解为

$$
y = x ^ {3} + 3 x + 1.
$$

例 4 设有一均匀、柔软的绳索,两端固定,绳索仅受重力的作用而下垂.试问该绳索在平衡状态时是怎样的曲线?

解 设绳索的最低点为 $A$. 取 $y$ 轴通过点 $A$ 铅直向上, 并取 $x$ 轴水平向右. 且 $|OA|$ 等于某个定值 (这个定值将在以后说明). 设绳索曲线的方程为 $y = \varphi(x)$. 考察绳索上点 $A$ 到另一点 $M(x, y)$ 间的一段弧 $\widehat{AM}$, 设其长为 $s$. 假定绳索的线密度为 $\rho$, 则弧 $\widehat{AM}$ 所受重力为 $\rho g s$. 由于绳索是柔软的, 因而在点 $A$ 处的张力沿水平的切线方向, 其大小设为 $H$; 在点 $M$ 处的张力沿该点处的切线方向, 设其倾角为 $\theta$, 其大小为 $T$ (图7-6). 因作用于弧段 $\widehat{AM}$ 的外力相互平衡, 把作用于弧 $\widehat{AM}$ 上的力沿铅直及水平两方向分解, 得

$$
T \sin \theta = \rho g s, \quad T \cos \theta = H.
$$

将此两式相除,得

$$
\tan \theta = \frac {1}{a} s \quad \left(a = \frac {H}{\rho g}\right).
$$

由于 $\tan \theta = y'$, $s = \int_{0}^{x} \sqrt{1 + y'^2} \, \mathrm{d}x$, 代入上式即得

$$
y ^ {\prime} = \frac {1}{a} \int_ {0} ^ {x} \sqrt {1 + y ^ {\prime 2}}   \mathrm{d} x.
$$

![](images/page_333_image_6.jpg)

<details>
<summary>text_image</summary>

y
T
θ
M
H
A
ρgs
O
x
</details>

图7-6

将上式两端对 x 求导, 便得  $y=\varphi(x)$  满足的微分方程

$$
y ^ {\prime \prime} = \frac {1}{a} \sqrt {1 + y ^ {\prime 2}}. \tag {5-8}
$$

取原点 O 到点 A 的距离为定值 a，即  $\left|OA\right|=a$ ，那么初值条件为

$$
y \mid_ {x = 0} = a, \quad y ^ {\prime} \mid_ {x = 0} = 0.
$$

下面来解方程(5-8).

方程(5-8)属于 $y''=f(x,y')$ 的类型.设 $y'=p$，则 $y''=\frac{dp}{dx}$，代入方程(5-8)，并分离变量，得

$$
\frac {\mathrm{d} p}{\sqrt {1 + p ^ {2}}} = \frac {\mathrm{d} x}{a}.
$$

两端积分,得

$$
\ln (p + \sqrt {1 + p ^ {2}}) = \frac {x}{a} + C _ {1}. \tag {5-9}
$$

把条件  $y'\mid_{x=0}=p\mid_{x=0}=0$  代入(5-9)式, 得

$$
C _ {1} = 0,
$$

于是(5-9)式成为

$$
\ln (p + \sqrt {1 + p ^ {2}}) = \frac {x}{a},
$$

解得

$$
p = \frac {1}{2} \left(\mathrm{e} ^ {\frac {x}{a}} - \mathrm{e} ^ {- \frac {x}{a}}\right),
$$

即

$$
y ^ {\prime} = \frac {1}{2} (\mathrm{e} ^ {\frac {x}{a}} - \mathrm{e} ^ {- \frac {x}{a}}).
$$

积分上式两端,便得

$$
y = \frac {a}{2} (\mathrm{e} ^ {\frac {x}{a}} + \mathrm{e} ^ {- \frac {x}{a}}) + C _ {2}. \tag {5-10}
$$

将条件  $y|_{x=0}=a$  代入(5-10)式, 得

$$
C _ {2} = 0.
$$

于是该绳索的形状可由曲线方程

$$
y = \frac {a}{2} (\mathrm{e} ^ {\frac {x}{a}} + \mathrm{e} ^ {- \frac {x}{a}})
$$

来表示.这曲线叫做悬链线.

## 三、 $y''=f(y,y')$ 型的微分方程

方程

$$
y ^ {\prime \prime} = f (y, y ^ {\prime}) \tag {5-11}
$$

中不明显地含自变量 $x$，为了求出它的解。我们令 $y' = p$，并利用复合函数的求导法则把 $y''$ 化为对 $y$ 的导数，即

$$
y ^ {\prime \prime} = \frac {\mathrm{d} p}{\mathrm{d} x} = \frac {\mathrm{d} p}{\mathrm{d} y} \cdot \frac {\mathrm{d} y}{\mathrm{d} x} = p \frac {\mathrm{d} p}{\mathrm{d} y}.
$$

这样,方程(5-11)就成为

$$
p \frac {\mathrm{d} p}{\mathrm{d} y} = f (y, p).
$$

这是一个关于变量 $y, p$ 的一阶微分方程. 设它的通解为

$$
y ^ {\prime} = p = \varphi (y, C _ {1}),
$$

分离变量并积分,便得方程(5-11)的通解为

$$
\int \frac {\mathrm{d} y}{\varphi (y , C _ {1})} = x + C _ {2},
$$

例5 求微分方程

$$
y y ^ {\prime \prime} - y ^ {2} = 0 \tag {5-12}
$$

的通解.

解 方程(5-12)不明显地含自变量 $x$，设

$$
y ^ {\prime} = p,
$$

则 $y'' = p\frac{\mathrm{d}p}{\mathrm{d}y}$ ，代入方程(5-12)，得

$$
y p \frac {\mathrm{d} p}{\mathrm{d} y} - p ^ {2} = 0.
$$

在 $y \neq 0, p \neq 0$ 时，约去 $p$ 并分离变量，得

$$
\frac {\mathrm{d} p}{p} = \frac {\mathrm{d} y}{y}.
$$

两端积分,得

$$
\ln | p | = \ln | y | + C,
$$

即

$$
p = C _ {1} y \quad \text {或} \quad y ^ {\prime} = C _ {1} y \quad (  C _ {1} = \pm \mathrm{e} ^ {C})  .
$$

再分离变量并两端积分,便得方程(5-12)的通解为

$$
\ln | y | = C _ {1} x + C _ {2} ^ {\prime},
$$

或

$$
y = C _ {2} \mathrm{e} ^ {C _ {1} x} \quad (  C _ {2} = \pm \mathrm{e} ^ {C _ {2} ^ {\prime}}  ).
$$

例 6 一个离地面很高的物体,受地球引力的作用由静止开始落向地面.求它落到地面时的速度和所需的时间(不计空气阻力).

解 取连接地心与该物体的直线为 y 轴, 其方向铅直向上, 取地心为原点 O (图 7-7).

设地球的半径为 R，物体的质量为 m，物体开始下落时与地心的距离为  $l(l > R)$ ，在时刻 t 物体所在位置为  $y = \varphi(t)$ ，于是速度为  $v(t) = \frac{\mathrm{d}y}{\mathrm{d}t}$ 。根据万有引力定律，即得微分方程

$$
m \frac {\mathrm{d} ^ {2} y}{\mathrm{d} t ^ {2}} = - \frac {G m M}{y ^ {2}},
$$

![](images/page_335_image_14.jpg)

<details>
<summary>text_image</summary>

y
l
R
O
</details>

图7-7

即

$$
\frac {\mathrm{d} ^ {2} y}{\mathrm{d} t ^ {2}} = - \frac {G M}{y ^ {2}}, \tag {5-13}
$$

其中 $M$ 为地球的质量, $G$ 为引力常量. 因为当 $y = R$ 时, $\frac{\mathrm{d}^2y}{\mathrm{d}t^2} = -g$ (这里置负号是由于物体运动加速度的方向与 $y$ 轴的正向相反的缘故), 所以 $g = \frac{GM}{R^2}, GM = gR^2$. 于是方程 (5-13) 成为

$$
\frac {\mathrm{d} ^ {2} y}{\mathrm{d} t ^ {2}} = - \frac {g R ^ {2}}{y ^ {2}}. \tag {5-14}
$$

初值条件是

$$
y \mid_ {t = 0} = l, \quad y ^ {\prime} \mid_ {t = 0} = 0.
$$

先求物体到达地面时的速度.由 $\frac{dy}{dt}=v$ ,得

$$
\frac {\mathrm{d} ^ {2} y}{\mathrm{d} t ^ {2}} = \frac {\mathrm{d} v}{\mathrm{d} t} = \frac {\mathrm{d} v}{\mathrm{d} y} \cdot \frac {\mathrm{d} y}{\mathrm{d} t} = v \frac {\mathrm{d} v}{\mathrm{d} y},
$$

代入方程(5-14)并分离变量,得

$$
v \mathrm{d} v = - \frac {g R ^ {2}}{y ^ {2}} \mathrm{d} y.
$$

两端积分,得

$$
v ^ {2} = \frac {2 g R ^ {2}}{\gamma} + C _ {1}.
$$

把初值条件代入上式,得

$$
C _ {1} = - \frac {2 g R ^ {2}}{l},
$$

于是

$$
v ^ {2} = 2 g R ^ {2} \left(\frac {1}{y} - \frac {1}{l}\right),
$$

$$
v = - R \sqrt {2 g \left(\frac {1}{y} - \frac {1}{l}\right)}. \tag {5-15}
$$

这里取负号是由于物体运动的方向与 $y$ 轴的正向相反的缘故. 在(5-15)式中令 $y = R$ 就得到物体到达地面时的速度为

$$
v = - \sqrt {\frac {2 g R (l - R)}{l}}.
$$

下面来求物体落到地面所需的时间.由(5-15)式有

$$
\frac {\mathrm{d} y}{\mathrm{d} t} = v = - R \sqrt {2 g \left(\frac {1}{y} - \frac {1}{l}\right)},
$$

分离变量得

$$
\mathrm{d} t = - \frac {1}{R} \sqrt {\frac {l}{2 g}} \sqrt {\frac {y}{l - y}} \mathrm{d} y.
$$

两端积分(对右端积分利用置换  $y=l\cos^{2}u$ )，得

$$
t = \frac {1}{R} \sqrt {\frac {l}{2 g}} \left(\sqrt {l y - y ^ {2}} + l \arccos \sqrt {\frac {y}{l}}\right) + C _ {2}. \tag {5-16}
$$

由条件 $y|_{t=0}=l$ , 得

$$
C _ {2} = 0.
$$

于是(5-16)式成为

$$
t = \frac {1}{R} \sqrt {\frac {l}{2 g}} \left(\sqrt {l y - y ^ {2}} + l \arccos \sqrt {\frac {y}{l}}\right).
$$

在上式中令 $y = R$ ,便得到物体到达地面所需的时间为

$$
t = \frac {1}{R} \sqrt {\frac {l}{2 g}} \left(\sqrt {l R - R ^ {2}} + l \arccos \sqrt {\frac {R}{l}}\right).
$$

## 习题7-5

1. 求下列各微分方程的通解:

(1) $y''=x+\sin x;$

(2) $y'''=xe^{x}$;

(3) $y''=\frac{1}{1+x^{2}}$;

(4) $y''=1+y'^{2}$;

(5) $y''=y'+x;$

(6)  $xy''+y'=0;$

(7)  $yy''+2y'^{2}=0;$

(8) $y^{3}y''-1=0;$

(9) $y''=\frac{1}{\sqrt{y}}$;

(10)  $y''=y'^{3}+y'$

2. 设 $f(x)$ 具有二阶连续导数, 满足:

$$
f ^ {\prime 2} (x) = f (x) + \int_ {0} ^ {x} \left[ f ^ {\prime} (t) \right] ^ {3} \mathrm{d} t,
$$

且 $f'(0)=1$ , 求  $f(x)$ .

3. 求下列各微分方程满足所给初值条件的特解:

(1) $y^{3}y^{\prime \prime} + 1 = 0, y \mid_{x=1} = 1, y^{\prime} \mid_{x=1} = 0;$

(2) $y''-ay'^{2}=0,y\mid_{x=0}=0,y'\mid_{x=0}=-1;$

(3) $y''' = e^{ax}, y \mid_{x=1} = y' \mid_{x=1} = y'' \mid_{x=1} = 0;$

(4) $y'' = e^{2y}, y \mid_{x=0} = y' \mid_{x=0} = 0;$

(5) $y'' = 3\sqrt{y}, y \mid_{x=0} = 1, y' \mid_{x=0} = 2;$

(6) $y'' + y'^2 = 1, y \mid_{x=0} = 0, y' \mid_{x=0} = 0.$

4. 试求 $y'' = x$ 的经过点 $M(0,1)$ 且在此点与直线 $y = \frac{x}{2} + 1$ 相切的积分曲线.

5. 设有一质量为 $m$ 的物体在空中由静止开始下落, 如果空气阻力 $R = cv$ (其中 $c$ 为常数, $v$ 为物体运动的速度), 试求物体下落的距离 $s$ 与时间 $t$ 的函数关系.

## 第六节 高阶线性微分方程

本节和以下两节,我们将讨论在实际问题中应用得较多的所谓高阶线性微分方程.讨论时以二阶线性微分方程为主.

## 一、二阶线性微分方程举例

例 1 设有一个弹簧, 它的上端固定, 下端挂一个质量为 m 的物体. 当物体处于静止状态时, 作用在物体上的重力与弹性力大小相等、方向相反. 这个位置就是物体的平衡位置. 如图 7-8 所示, 取 x 轴铅直向下, 并取物体的平衡位置为坐标原点.

如果使物体具有一个初始速度 $v_{0} \neq 0$ ，那么物体便离开平衡位置，并在平衡位置附近做上下振动.在振动过程中,物体的位置 x 随时间 t 变化,即 x 与 t 之间存在函数关系:  $x = x(t)$ .要确定物体的振动规律,就要求出函数  $x = x(t)$ .

由力学知道,弹簧使物体回到平衡位置的弹性恢复力f(它不包括在平衡位置时和重力mg相平衡的那一部分弹性力)和物体离开平衡位置的位移x成正比:

$$
f = - c x,
$$

其中 c 为弹簧的弹性系数, 负号表示弹性恢复力的方向和物体位移的方向相反.

![](images/page_338_image_5.jpg)

<details>
<summary>text_image</summary>

O
x
x
</details>

图7-8

另外,物体在运动过程中还受到阻尼介质(如空气、油等)的阻力的作用,使得振动逐渐趋向停止.由实验知道,阻力R的方向总与运动方向相反,当运动速度不大时,其大小与物体运动的速度成正比,设比例系数为 $\mu$ ,则有

$$
R = - \mu \frac {\mathrm{d} x}{\mathrm{d} t}.
$$

根据上述关于物体受力情况的分析,由牛顿第二定律得

$$
m \frac {\mathrm{d} ^ {2} x}{\mathrm{d} t ^ {2}} = - c x - \mu \frac {\mathrm{d} x}{\mathrm{d} t}.
$$

移项,并记

$$
2 n = \frac {\mu}{m}, \quad k ^ {2} = \frac {c}{m},
$$

则上式化为

$$
\frac {\mathrm{d} ^ {2} x}{\mathrm{d} t ^ {2}} + 2 n \frac {\mathrm{d} x}{\mathrm{d} t} + k ^ {2} x = 0. \tag {6-1}
$$

这就是在有阻尼的情况下,物体自由振动的微分方程.

如果物体在振动过程中,还受到铅直干扰力

$$
F = H \sin p t
$$

的作用,那么有

$$
\frac {\mathrm{d} ^ {2} x}{\mathrm{d} t ^ {2}} + 2 n \frac {\mathrm{d} x}{\mathrm{d} t} + k ^ {2} x = h \sin p t,\tag {6-2}
$$

其中  $h=\frac{H}{m}$ . 这就是强迫振动的微分方程.

例 2 设有一个由电阻 R、自感 L、电容 C 和电源 E 串联组成的电路, 其中 R, L 及 C 为常数,  $E = E_{m} \sin \omega t$ , 这里  $E_{m}$  及  $\omega$  也是常数(图 7-9).

设电路中的电流为 $i(t)$ ，电容器极板上的电荷量为 $q(t)$ ，两极板间的电压为 $u_{C}$

自感电动势为  $E_{L}$ . 由电学知道

$$
i = \frac {\mathrm{d} q}{\mathrm{d} t}, \quad u _ {c} = \frac {q}{C}, \quad E _ {L} = - L \frac {\mathrm{d} i}{\mathrm{d} t},
$$

根据回路电压定律,得

$$
E - L \frac {\mathrm{d} i}{\mathrm{d} t} - \frac {q}{C} - R i = 0,
$$

即

$$
LC\frac{\mathrm{d}^2u_c}{\mathrm{d}t^2} +RC\frac{\mathrm{d}u_c}{\mathrm{d}t} +u_c = E_\mathrm{m}\sin \omega t,
$$

或写成

![](images/page_339_image_8.jpg)

<details>
<summary>text_image</summary>

R
i
L
C
+q A B -q S
E
</details>

图7-9

$$
\frac {\mathrm{d} ^ {2} u _ {c}}{\mathrm{d} t ^ {2}} + 2 \beta \frac {\mathrm{d} u _ {c}}{\mathrm{d} t} + \omega_ {0} ^ {2} u _ {c} = \frac {E _ {\mathrm{m}}}{L C} \sin \omega t. \tag {6-3}
$$

式中  $\beta=\frac{R}{2L},\omega_{0}=\frac{1}{\sqrt{LC}}$ . 这就是串联电路的振荡方程.

如果电容器经充电后撤去外电源 $(E=0)$ ，那么方程 $(6-3)$ 成为

$$
\frac {\mathrm{d} ^ {2} u _ {c}}{\mathrm{d} t ^ {2}} + 2 \beta \frac {\mathrm{d} u _ {c}}{\mathrm{d} t} + \omega_ {0} ^ {2} u _ {c} = 0. \tag {6-4}
$$

例 1 和例 2 虽然是两个不同的实际问题,但是仔细观察一下所得出的方程(6-2)和(6-3),就会发现它们可以归结为同一个形式

$$
\frac {\mathrm{d} ^ {2} y}{\mathrm{d} x ^ {2}} + P (x) \frac {\mathrm{d} y}{\mathrm{d} x} + Q (x) y = f (x), \tag {6-5}
$$

而方程(6-1)和方程(6-4)都是方程(6-5)的特殊情形: $f(x)\equiv0$ .在工程技术的其他许多问题中,也会遇到上述类型的微分方程.

方程(6-5)叫做二阶线性微分方程. 当方程右端 $f(x)\equiv0$ 时, 方程叫做齐次的; 当 $f(x)\neq0$ 时, 方程叫做非齐次的.

于是方程(6-2)、(6-3)都是二阶非齐次线性微分方程,方程(6-1)、(6-4)都是二阶齐次线性微分方程.

要进一步讨论例 1 和例 2 中的问题, 就需要解二阶线性微分方程. 为此, 下面来讨论二阶线性微分方程的解的一些性质, 这些性质可以推广到 n 阶线性方程

$$
y ^ {(n)} + a _ {1} (x) y ^ {(n - 1)} + \dots + a _ {n - 1} (x) y ^ {\prime} + a _ {n} (x) y = f (x).
$$

## 二、线性微分方程的解的结构

先讨论二阶齐次线性方程

$$
y ^ {\prime \prime} + P (x) y ^ {\prime} + Q (x) y = 0. \tag {6-6}
$$

定理1 如果函数 $y_{1}(x)$ 与 $y_{2}(x)$ 是方程(6-6)的两个解，那么

$$
y = C _ {1} y _ {1} (x) + C _ {2} y _ {2} (x) \tag {6-7}
$$

也是(6-6)的解,其中 $C_{1},C_{2}$ 是任意常数.

证 将(6-7)式代入(6-6)式左端, 得

$$
\begin{array}{l} \left[ C _ {1} y _ {1} ^ {\prime \prime} + C _ {2} y _ {2} ^ {\prime \prime} \right] + P (x) \left[ C _ {1} y _ {1} ^ {\prime} + C _ {2} y _ {2} ^ {\prime} \right] + Q (x) \left[ C _ {1} y _ {1} + C _ {2} y _ {2} \right] \\ = C _ {1} \left[ y _ {1} ^ {\prime \prime} + P (x) y _ {1} ^ {\prime} + Q (x) y _ {1} \right] + C _ {2} \left[ y _ {2} ^ {\prime \prime} + P (x) y _ {2} ^ {\prime} + Q (x) y _ {2} \right]. \\ \end{array}
$$

由于 $y_{1}$ 与 $y_{2}$ 是方程(6-6)的解，上式右端方括号中的表达式都恒等于零，因而整个式子恒等于零，所以(6-7)式是方程(6-6)的解.

解(6-7)从形式上来看含有 $C_1$ 与 $C_2$ 两个任意常数, 但它不一定是方程(6-6)的通解. 例如, 设 $y_1(x)$ 是(6-6)的一个解, 则 $y_2(x) = 2y_1(x)$ 也是(6-6)的解. 这时(6-7)式成为 $y = C_1y_1(x) + 2C_2y_1(x)$, 可以把它改写成 $y = Cy_1(x)$, 其中 $C = C_1 + 2C_2$. 这显然不是(6-6)的通解. 那么在什么情况下(6-7)式才是方程(6-6)的通解呢? 要解决这个问题, 还得引入一个新的概念, 即所谓函数组的线性相关与线性无关.

设  $y_{1}(x)$ ,  $y_{2}(x)$ ,  $\cdots$ ,  $y_{n}(x)$  为定义在区间 I 上的 n 个函数, 如果存在 n 个不全为零的常数  $k_{1}, k_{2}, \cdots, k_{n}$ , 使得当  $x \in I$  时有恒等式

$$
k _ {1} y _ {1} + k _ {2} y _ {2} + \dots + k _ {n} y _ {n} \equiv 0
$$

成立,那么称这 n 个函数在区间 I 上线性相关;否则称线性无关.

例如, 函数  $1, \cos^{2}x, \sin^{2}x$  在整个数轴上是线性相关的. 因为取  $k_{1}=1, k_{2}=k_{3}=-1$ ，就有恒等式

$$
1 - \cos^ {2} x - \sin^ {2} x \equiv 0.
$$

又如, 函数  $1, x, x^{2}$  在任何区间  $(a, b)$  内是线性无关的. 因为如果  $k_{1}, k_{2}, k_{3}$  不全为零, 那么在该区间内至多只有两个 x 值能使二次三项式

$$
k _ {1} + k _ {2} x + k _ {3} x ^ {2}
$$

为零;要使它恒等于零,必须 $k_{1},k_{2},k_{3}$ 全为零.

应用上述概念可知,对于两个函数的情形,它们线性相关与否,只要看它们的比是否为常数:如果比为常数,那么它们就线性相关;否则就线性无关.

有了一组函数线性相关或线性无关的概念后,我们有如下关于二阶齐次线性微分方程(6-6)的通解结构的定理.

定理 2 如果  $y_{1}(x)$  与  $y_{2}(x)$  是方程(6-6)的两个线性无关的特解,那么

$$
y = C _ {1} y _ {1} (x) + C _ {2} y _ {2} (x) \quad (C _ {1}, C _ {2} \text {是任意常数})
$$

就是方程(6-6)的通解.

例如,方程  $y''+y=0$  是二阶齐次线性方程(这里  $P(x)\equiv0,Q(x)\equiv1$ ). 容易验证,  $y_{1}=\cos x$  与  $y_{2}=\sin x$  是所给方程的两个解, 且  $\frac{y_{2}}{y_{1}}=\frac{\sin x}{\cos x}=\tan x \neq$  常数, 即它们是线性无关

的.因此方程  $y''+y=0$  的通解为

$$
y = C _ {1} \cos x + C _ {2} \sin x.
$$

又如，方程 $(x - 1)y'' - xy' + y = 0$ 也是二阶齐次线性方程（这里 $P(x) = -\frac{x}{x - 1}, Q(x) = \frac{1}{x - 1}$. 容易验证 $y_{1} = x, y_{2} = \mathrm{e}^{x}$ 是所给方程的两个解，且 $\frac{y_2}{y_1} = \frac{\mathrm{e}^x}{x} \neq$ 常数，即它们是线性无关的. 因此方程的通解为

$$
y = C _ {1} x + C _ {2} \mathrm{e} ^ {x}.
$$

定理 2 不难推广到 n 阶齐次线性方程.

推论 如果  $y_{1}(x)$ ,  $y_{2}(x)$ ,  $\cdots$ ,  $y_{n}(x)$  是 n 阶齐次线性方程

$$
y ^ {(n)} + a _ {1} (x) y ^ {(n - 1)} + \dots + a _ {n - 1} (x) y ^ {\prime} + a _ {n} (x) y = 0
$$

的 n 个线性无关的解,那么,此方程的通解为

$$
y = C _ {1} y _ {1} (x) + C _ {2} y _ {2} (x) + \dots + C _ {n} y _ {n} (x),
$$

其中  $C_{1}, C_{2}, \cdots, C_{n}$  为任意常数.

下面讨论二阶非齐次线性方程(6-5). 我们把方程(6-6)叫做与非齐次方程(6-5)对应的齐次方程.

在第四节中我们已经看到,一阶非齐次线性微分方程的通解由两部分构成:一部分是对应的齐次方程的通解,另一部分是非齐次方程本身的一个特解.实际上,不仅一阶非齐次线性微分方程的通解具有这样的结构,而且二阶及更高阶的非齐次线性微分方程的通解也具有同样的结构.

定理3 设 $y^{*}(x)$ 是二阶非齐次线性方程

$$
y ^ {\prime \prime} + P (x) y ^ {\prime} + Q (x) y = f (x) \tag {6-5}
$$

的一个特解. $Y(x)$ 是与(6-5)对应的齐次方程(6-6)的通解, 则

$$
y = Y (x) + y ^ {*} (x) \tag {6-8}
$$

是二阶非齐次线性微分方程(6-5)的通解.

证 把(6-8)式代入方程(6-5)的左端,得

$$
\begin{array}{l} (Y ^ {\prime \prime} + y ^ {* \prime \prime}) + P (x) (Y ^ {\prime} + y ^ {* \prime}) + Q (x) (Y + y ^ {*}) \\ = [ Y ^ {\prime \prime} + P (x) Y ^ {\prime} + Q (x) Y ] + [ y ^ {* \prime \prime} + P (x) y ^ {* \prime} + Q (x) y ^ {*} ], \\ \end{array}
$$

由于 $Y$ 是方程(6-6)的解，$y^{*}$ 是(6-5)的解，可知第一个括号内的表达式恒等于零，第二个恒等于 $f(x)$. 这样，$y = Y + y^{*}$ 使(6-5)的两端恒等. 即(6-8)式是方程(6-5)的解.

由于对应的齐次方程(6-6)的通解 $Y = C_{1}y_{1} + C_{2}y_{2}$ 中含有两个任意常数，所以 $y = Y + y^{*}$ 中也含有两个任意常数，从而它就是二阶非齐次线性方程(6-5)的通解.

例如,方程  $y''+y=x^{2}$  是二阶非齐次线性微分方程.已知  $Y=C_{1}\cos x+C_{2}\sin x$  是对应的齐次方程  $y''+y=0$  的通解;又容易验证  $y^{*}=x^{2}-2$  是所给方程的一个特解.因此

$$
y = C _ {1} \cos x + C _ {2} \sin x + x ^ {2} - 2
$$

是所给方程的通解.

非齐次线性微分方程(6-5)的特解有时可用下述定理来帮助求出.

定理 4 设非齐次线性方程(6-5)的右端 $f(x)$ 是两个函数之和, 即

$$
y ^ {\prime \prime} + P (x) y ^ {\prime} + Q (x) y = f _ {1} (x) + f _ {2} (x), \tag {6-9}
$$

而 $y_{1}^{*}(x)$ 与 $y_{2}^{*}(x)$ 分别是方程

$$
y ^ {\prime \prime} + P (x) y ^ {\prime} + Q (x) y = f _ {1} (x)
$$

与

$$
y ^ {\prime \prime} + P (x) y ^ {\prime} + Q (x) y = f _ {2} (x)
$$

的特解, 则  $y_{1}^{*}(x)+y_{2}^{*}(x)$  就是原方程的特解.

证 将 $y = y_1^* + y_2^*$ 代入方程(6-9)的左端, 得

$$
\begin{array}{l} \left(y _ {1} ^ {*} + y _ {2} ^ {*}\right) ^ {\prime \prime} + P (x) \left(y _ {1} ^ {*} + y _ {2} ^ {*}\right) ^ {\prime} + Q (x) \left(y _ {1} ^ {*} + y _ {2} ^ {*}\right) \\ = \left[ y _ {1} ^ {* \prime \prime} + P (x) y _ {1} ^ {* \prime} + Q (x) y _ {1} ^ {*} \right] + \left[ y _ {2} ^ {* \prime \prime} + P (x) y _ {2} ^ {* \prime} + Q (x) y _ {2} ^ {*} \right] \\ = f _ {1} (x) + f _ {2} (x). \\ \end{array}
$$

因此 $y_{1}^{*} + y_{2}^{*}$ 是方程(6-9)的一个特解.

这一定理通常称为线性微分方程的解的叠加原理.

定理 3 和定理 4 也可推广到 n 阶非齐次线性方程, 这里不再赘述.

## \* 三、常数变易法

在第四节中,为解一阶非齐次线性方程,我们用了常数变易法.这方法的特点是:如果  $C y_{1}(x)$  是齐次线性方程的通解,那么,可以利用变换  $y = u y_{1}(x)$  (这变换是把齐次方程的通解中的任意常数 C 换成未知函数  $u(x)$  而得到的)去解非齐次线性方程.这一方法也适用于解高阶线性方程.下面就二阶线性方程来作讨论.

如果已知齐次方程(6-6)的通解为

$$
Y (x) = C _ {1} y _ {1} (x) + C _ {2} y _ {2} (x),
$$

那么,可以用如下的常数变易法去求非齐次方程(6-5)的通解.令

$$
y = y _ {1} (x) v _ {1} + y _ {2} (x) v _ {2}, \tag {6-10}
$$

要确定未知函数 $v_{1}(x)$ 及 $v_{2}(x)$ 使(6-10)式所表示的函数满足非齐次方程(6-5).为此，对(6-10)式求导，得

$$
y ^ {\prime} = y _ {1} v _ {1} ^ {\prime} + y _ {2} v _ {2} ^ {\prime} + y _ {1} ^ {\prime} v _ {1} + y _ {2} ^ {\prime} v _ {2}.
$$

由于两个未知函数 $v_{1}, v_{2}$ 只需使(6-10)式所表示的函数满足一个关系式(6-5)，所以可规定它们再满足一个关系式。从 $y'$ 的上述表示式可看出，为了使 $y''$ 的表示式中不含 $v_{1}''$ 和 $v_{2}''$，可设

$$
y _ {1} v _ {1} ^ {\prime} + y _ {2} v _ {2} ^ {\prime} = 0, \tag {6-11}
$$

从而

$$
y ^ {\prime} = y _ {1} ^ {\prime} v _ {1} + y _ {2} ^ {\prime} v _ {2},
$$

再求导,得

$$
y ^ {\prime \prime} = y _ {1} ^ {\prime} v _ {1} ^ {\prime} + y _ {2} ^ {\prime} v _ {2} ^ {\prime} + y _ {1} ^ {\prime \prime} v _ {1} + y _ {2} ^ {\prime \prime} v _ {2}.
$$

把 $y, y', y''$ 代入方程(6-5)，得

$$
y _ {1} ^ {\prime} v _ {1} ^ {\prime} + y _ {2} ^ {\prime} v _ {2} ^ {\prime} + y _ {1} ^ {\prime \prime} v _ {1} + y _ {2} ^ {\prime \prime} v _ {2} + P (y _ {1} ^ {\prime} v _ {1} + y _ {2} ^ {\prime} v _ {2}) + Q (y _ {1} v _ {1} + y _ {2} v _ {2}) = f,
$$

整理得

$$
y _ {1} ^ {\prime} v _ {1} ^ {\prime} + y _ {2} ^ {\prime} v _ {2} ^ {\prime} + (y _ {1} ^ {\prime \prime} + P y _ {1} ^ {\prime} + Q y _ {1}) v _ {1} + (y _ {2} ^ {\prime \prime} + P y _ {2} ^ {\prime} + Q y _ {2}) v _ {2} = f.
$$

注意到  $y_{1}$  及  $y_{2}$  是齐次方程(6-6)的解, 故上式即为

$$
y _ {1} ^ {\prime} v _ {1} ^ {\prime} + y _ {2} ^ {\prime} v _ {2} ^ {\prime} = f. \tag {6-12}
$$

联立方程(6-11)与(6-12)，在系数行列式

$$
W = \left| \begin{array}{c c} y _ {1} & y _ {2} \\ y _ {1} ^ {\prime} & y _ {2} ^ {\prime} \end{array} \right| = y _ {1} y _ {2} ^ {\prime} - y _ {1} ^ {\prime} y _ {2} \neq 0
$$

时,可解得

$$
v _ {1} ^ {\prime} = - \frac {y _ {2} f}{W}, \quad v _ {2} ^ {\prime} = \frac {y _ {1} f}{W}.
$$

对上两式积分(假定 $f(x)$ 连续), 得

$$
v _ {1} = C _ {1} + \int \left(- \frac {y _ {2} f}{W}\right) \mathrm{d} x, \quad v _ {2} = C _ {2} + \int \frac {y _ {1} f}{W} \mathrm{d} x.
$$

于是得非齐次方程(6-5)的通解为

$$
y = C _ {1} y _ {1} + C _ {2} y _ {2} - y _ {1} \int \frac {y _ {2} f}{W} \mathrm{d} x + y _ {2} \int \frac {y _ {1} f}{W} \mathrm{d} x.
$$

例3 已知齐次方程 $(x - 1)y'' - xy' + y = 0$ 的通解为 $Y(x) = C_1x + C_2\mathrm{e}^x$ ，求非齐次方程$(x - 1)y'' - xy' + y = (x - 1)^2$ 的通解.

解 把所给方程写成标准形式

$$
y ^ {\prime \prime} - \frac {x}{x - 1} y ^ {\prime} + \frac {1}{x - 1} y = x - 1.
$$

令 $y = xv_{1} + \mathrm{e}^{x}v_{2}$ 按照

$$
\left\{ \begin{array}{l} y _ {1} v _ {1} ^ {\prime} + y _ {2} v _ {2} ^ {\prime} = 0, \\ y _ {1} ^ {\prime} v _ {1} ^ {\prime} + y _ {2} ^ {\prime} v _ {2} ^ {\prime} = f. \end{array} \right.
$$

有

$$
\left\{ \begin{array}{l} x v _ {1} ^ {\prime} + \mathrm{e} ^ {x} v _ {2} ^ {\prime} = 0, \\ v _ {1} ^ {\prime} + \mathrm{e} ^ {x} v _ {2} ^ {\prime} = x - 1, \end{array} \right.
$$

解得

$$
v _ {1} ^ {\prime} = - 1, \quad v _ {2} ^ {\prime} = x \mathrm{e} ^ {- x}.
$$

积分,得

$$
v _ {1} = C _ {1} - x, \quad v _ {2} = C _ {2} - (x + 1) \mathrm{e} ^ {- x}.
$$

于是所求非齐次方程的通解为

$$
y = C _ {1} x + C _ {2} \mathrm{e} ^ {x} - (  x ^ {2} + x + 1)  .
$$

如果只知齐次方程(6-6)的一个不恒为零的解 $y_{1}(x)$ ，那么，利用变换 $y = uy_{1}(x)$ ，可把非齐次方程(6-5)化为一阶线性方程.

事实上,把

$$
y = y _ {1} u, \quad y ^ {\prime} = y _ {1} u ^ {\prime} + y _ {1} ^ {\prime} u, \quad y ^ {\prime \prime} = y _ {1} u ^ {\prime \prime} + 2 y _ {1} ^ {\prime} u ^ {\prime} + y _ {1} ^ {\prime \prime} u
$$

代入方程(6-5)，得

$$
y _ {1} u ^ {\prime \prime} + 2 y _ {1} ^ {\prime} u ^ {\prime} + y _ {1} ^ {\prime \prime} u + P (y _ {1} u ^ {\prime} + y _ {1} ^ {\prime} u) + Q y _ {1} u = f,
$$

即

$$
y _ {1} u ^ {\prime \prime} + (2 y _ {1} ^ {\prime} + P y _ {1}) u ^ {\prime} + (y _ {1} ^ {\prime \prime} + P y _ {1} ^ {\prime} + Q y _ {1}) u = f,
$$

由于 $y_{1}^{\prime \prime} + Py_{1}^{\prime} + Qy_{1}\equiv 0$ ，故上式为

$$
y _ {1} u ^ {\prime \prime} + (2 y _ {1} ^ {\prime} + P y _ {1}) u ^ {\prime} = f.
$$

令 $u' = z$ ，上式即化为一阶线性方程

$$
y _ {1} z ^ {\prime} + (2 y _ {1} ^ {\prime} + P y _ {1}) z = f. \tag {6-13}
$$

把方程(6-5)化为方程(6-13)以后,按一阶线性方程的解法,设求得方程(6-13)的通解为

$$
z = C _ {2} Z (x) + z ^ {*} (x),
$$

积分得

$$
u = C _ {1} + C _ {2} U (x) + u ^ {*} (x) \quad (\text {其中} U ^ {\prime} (x) = Z (x), u ^ {* ^ {\prime}} (x) = z ^ {*} (x)),
$$

上式两端同乘 $y_{1}(x)$ ，便得方程(6-5)的通解

$$
y = C _ {1} y _ {1} (x) + C _ {2} U (x) y _ {1} (x) + u ^ {*} (x) y _ {1} (x).
$$

上述方法显然也适用于求齐次方程(6-6)的通解.

例 4 已知  $y_{1}(x)=\mathrm{e}^{x}$  是齐次方程  $y''-2y'+y=0$  的解, 求非齐次方程  $y''-2y'+y=\frac{1}{x}\mathrm{e}^{x}$  的通解.

解 令 $y = \mathrm{e}^{x}u$，则 $y' = \mathrm{e}^{x}(u' + u)$，$y'' = \mathrm{e}^{x}(u'' + 2u' + u)$，代入非齐次方程，得

$$
\mathrm{e} ^ {x} (u ^ {\prime \prime} + 2 u ^ {\prime} + u) - 2 \mathrm{e} ^ {x} (u ^ {\prime} + u) + \mathrm{e} ^ {x} u = \frac {1}{x} \mathrm{e} ^ {x},
$$

即

$$
\mathrm{e} ^ {x} u ^ {\prime \prime} = \frac {1}{x} \mathrm{e} ^ {x}, \quad u ^ {\prime \prime} = \frac {1}{x}.
$$

这里不需再作变换去化为一阶线性方程, 只要直接积分, 便得

$$
u ^ {\prime} = C + \ln | x |,
$$

再积分得

$$
u = C _ {1} + C x + x \ln | x | - x,
$$

即

$$
u = C _ {1} + C _ {2} x + x \ln | x | (C _ {2} = C - 1).
$$

于是所求通解为

$$
y = C _ {1} \mathrm{e} ^ {x} + C _ {2} x \mathrm{e} ^ {x} + x \mathrm{e} ^ {x} \ln | x |.
$$

## 习题7-6

1. 下列函数组在其定义区间内哪些是线性无关的？

(1) $x, x^2$;

(2) x, 2x;

(3) $e^{2x}, 3e^{2x}$,

(4) $e^{-x},e^{x};$

(5) $\cos 2x, \sin 2x$;

(6) $\mathrm{e}^{x^2}, x\mathrm{e}^{x^2}$;

(7)  $\sin 2x, \cos x \sin x;$

(8)  $e^{x}\cos 2x, e^{x}\sin 2x;$

(9) $\ln x, x \ln x$;

(10)  $e^{ax}, e^{bx} (a \neq b).$

2. 验证  $y_{1}=\cos\omega x$  及  $y_{2}=\sin\omega x$  都是方程  $y''+\omega^{2}y=0$  的解，并写出该方程的通解.
3. 验证 $y_{1} = \mathrm{e}^{x^{2}}$ 及 $y_{2} = x\mathrm{e}^{x^{2}}$ 都是方程 $y'' - 4xy' + (4x^{2} - 2)y = 0$ 的解，并写出该方程的通解.
4. 验证:

(1) $y = C_1 \mathrm{e}^x + C_2 \mathrm{e}^{2x} + \frac{1}{12} \mathrm{e}^{5x}$ ($C_1, C_2$ 是任意常数) 是方程 $y'' - 3y' + 2y = \mathrm{e}^{5x}$ 的通解；

(2) $y = C_{1} \cos 3x + C_{2} \sin 3x + \frac{1}{32} (4x \cos x + \sin x)$ ($C_{1}, C_{2}$ 是任意常数) 是方程 $y'' + 9y = x \cos x$ 的通解；

(3) $y = C_{1}x^{2} + C_{2}x^{2}\ln x$ ($C_{1}, C_{2}$ 是任意常数) 是方程 $x^{2}y'' - 3xy' + 4y = 0$ 的通解；

(4) $y = C_1x^5 + \frac{C_2}{x} - \frac{x^2}{9}\ln x$ ($C_1, C_2$ 是任意常数) 是方程 $x^2y'' - 3xy' - 5y = x^2\ln x$ 的通解；

(5) $y = \frac{1}{x} (C_1\mathrm{e}^x + C_2\mathrm{e}^{-x}) + \frac{\mathrm{e}^x}{2} (C_1, C_2 \text{是任意常数})$ 是方程 $xy'' + 2y' - xy = \mathrm{e}^x$ 的通解；

(6) $y = C_{1}e^{x} + C_{2}e^{-x} + C_{3}\cos x + C_{4}\sin x - x^{2}$ ($C_1, C_2, C_3, C_4$ 是任意常数) 是方程 $y^{(4)} - y = x^2$ 的通解.

\* 5. 已知 $y_{1}(x) = \mathrm{e}^{x}$ 是齐次线性方程

$$
(2 x - 1) y ^ {\prime \prime} - (2 x + 1) y ^ {\prime} + 2 y = 0
$$

的一个解,求此方程的通解.

\* 6. 已知 $y_{1}(x) = x$ 是齐次线性方程 $x^{2}y'' - 2xy' + 2y = 0$ 的一个解, 求非齐次线性方程 $x^{2}y'' - 2xy' +$

$2y=2x^{3}$ 的通解.

\*7. 已知齐次线性方程 $y'' + y = 0$ 的通解为 $Y(x) = C_1 \cos x + C_2 \sin x$，求非齐次线性方程 $y'' + y = \sec x$ 的通解.

\* 8. 已知齐次线性方程 $x^{2}y'' - xy' + y = 0$ 的通解为 $Y(x) = C_{1}x + C_{2}x\ln |x|$，求非齐次线性方程 $x^{2}y'' - xy' + y = x$ 的通解.

## 第七节 常系数齐次线性微分方程

先讨论二阶常系数齐次线性微分方程的解法,再把二阶方程的解法推广到 n 阶方程.

在二阶齐次线性微分方程

$$
y ^ {\prime \prime} + P (x) y ^ {\prime} + Q (x) y = 0 \tag {7-1}
$$

中,如果  $y'$ , y 的系数  $P(x)$ ,  $Q(x)$  均为常数, 即(7-1)式成为

$$
y ^ {\prime \prime} + p y ^ {\prime} + q y = 0, \tag {7-2}
$$

其中 p, q 是常数, 那么称 (7-2) 为二阶常系数齐次线性微分方程. 如果 p, q 不全为常数, 称 (7-1) 为二阶变系数齐次线性微分方程.

由上节讨论可知,要找微分方程(7-2)的通解,可以先求出它的两个解 $y_{1},y_{2}$ ,如果它们之比不为常数,即 $y_{1}$ 与 $y_{2}$ 线性无关,那么 $y=C_{1}y_{1}+C_{2}y_{2}$ 就是方程(7-2)的通解.

当 $r$ 为常数时, 指数函数 $y = \mathrm{e}^{rx}$ 和它的各阶导数都只相差一个常数因子. 由于指数函数有这个特点, 因此我们用 $y = \mathrm{e}^{rx}$ 来尝试, 看能否选取适当的常数 $r$, 使 $y = \mathrm{e}^{rx}$ 满足方程(7-2).

将  $y=e^{rx}$  求导①, 得到

$$
y ^ {\prime} = r \mathrm{e} ^ {r x}, \quad y ^ {\prime \prime} = r ^ {2} \mathrm{e} ^ {r x}
$$

把  $y, y'$  和  $y''$  代入方程(7-2)，得

$$
(r ^ {2} + p r + q) \mathrm{e} ^ {r x} = 0.
$$

由于  $e^{rx} \neq 0$ ，所以

$$
r ^ {2} + p r + q = 0. \tag {7-3}
$$

① 当 $r$ 为复数 $a + bi, x$ 为实变量时，导数公式 $\frac{\mathrm{d}}{\mathrm{d}x}\mathrm{e}^{rx} = r\mathrm{e}^{rx}$ 仍成立.事实上，对欧拉公式

$$
\mathrm{e} ^ {(a + b \mathrm{i}) x} = \mathrm{e} ^ {a x} (\cos b x + \mathrm{i} \sin b x)
$$

两端求导,得

$$
\begin{array}{l} \frac {\mathrm{d}}{\mathrm{d} x} \mathrm{e} ^ {(a + b \mathrm{i}) x} = a \mathrm{e} ^ {a x} (\cos b x + \mathrm{i} \sin b x) + \mathrm{e} ^ {a x} (- b \sin b x + \mathrm{i} b \cos b x) \\ = (a + b \mathrm{i}) \mathrm{e} ^ {a x} (\cos b x + \mathrm{i} \sin b x) = (a + b \mathrm{i}) \mathrm{e} ^ {(a + b \mathrm{i}) x}. \\ \end{array}
$$

由此可见, 只要 r 满足代数方程(7-3), 函数  $y = e^{rx}$  就是微分方程(7-2)的解, 我们把代数方程(7-3)叫做微分方程(7-2)的特征方程.

特征方程(7-3)是一个二次代数方程,其中 $r^{2},r$ 的系数及常数项恰好依次是微分方程(7-2)中 $y^{\prime\prime},y^{\prime}$ 及y的系数.

特征方程(7-3)的两个根 $r_1, r_2$ 可以用公式

$$
r _ {1, 2} = \frac {- p \pm \sqrt {p ^ {2} - 4 q}}{2}
$$

求出. 它们有三种不同的情形:

(i) 当 $p^2 - 4q > 0$ 时, $r_1, r_2$ 是两个不相等的实根

$$
r _ {1} = \frac {- p + \sqrt {p ^ {2} - 4 q}}{2}, \quad r _ {2} = \frac {- p - \sqrt {p ^ {2} - 4 q}}{2};
$$

(ii) 当 $p^2 - 4q = 0$ 时, $r_1, r_2$ 是两个相等的实根

$$
r _ {1} = r _ {2} = - \frac {p}{2};
$$

(iii) 当  $p^{2}-4q<0$  时,  $r_{1}, r_{2}$  是一对共轭复根

$$
r _ {1} = \alpha + \beta \mathrm{i}, \quad r _ {2} = \alpha - \beta \mathrm{i},
$$

其中

$$
\alpha = - \frac {p}{2}, \quad \beta = \frac {\sqrt {4 q - p ^ {2}}}{2}.
$$

相应地,微分方程(7-2)的通解也有三种不同的情形.分别讨论如下:

(i) 特征方程有两个不相等的实根:  $r_{1} \neq r_{2}$

由上面的讨论知道, $y_{1}=e^{r_{1}x},y_{2}=e^{r_{2}x}$ 是微分方程(7-2)的两个解,并且 $\frac{y_{2}}{y_{1}}=\frac{e^{r_{2}x}}{e^{r_{1}x}}=e^{(r_{2}-r_{1})x}$ 不是常数,因此微分方程(7-2)的通解为

$$
y = C _ {1} \mathrm{e} ^ {r _ {1} x} + C _ {2} \mathrm{e} ^ {r _ {2} x}.
$$

(ii) 特征方程有两个相等的实根:  $r_{1}=r_{2}$

这时, 只得到微分方程(7-2)的一个解

$$
y _ {1} = \mathrm{e} ^ {r _ {1} x}.
$$

为了得出微分方程(7-2)的通解,还需求出另一个解 $y_{2}$ ,并且要求 $\frac{y_{2}}{y_{1}}$ 不是常数.设 $\frac{y_{2}}{y_{1}}=u(x)$ ,即 $y_{2}=e^{r_{1}x}u(x)$ .下面来求 $u(x)$ .将 $y_{2}$ 求导,得

$$
\begin{array}{l} y _ {2} ^ {\prime} = \mathrm{e} ^ {r _ {1} x} (u ^ {\prime} + r _ {1} u), \\ y _ {2} ^ {\prime \prime} = \mathrm{e} ^ {r _ {1} x} (u ^ {\prime \prime} + 2 r _ {1} u ^ {\prime} + r _ {1} ^ {2} u), \\ \end{array}
$$

将 $y_{2}, y_{2}^{\prime}$ 和 $y_{2}^{\prime \prime}$ 代入微分方程(7-2)，得

$$
\mathrm{e} ^ {r _ {1} x} \left[ (u ^ {\prime \prime} + 2 r _ {1} u ^ {\prime} + r _ {1} ^ {2} u) + p (u ^ {\prime} + r _ {1} u) + q u \right] = 0,
$$

约去  $e^{r_{1}x}$ ，并合并同类项，得

$$
u ^ {\prime \prime} + (2 r _ {1} + p) u ^ {\prime} + (r _ {1} ^ {2} + p r _ {1} + q) u = 0.
$$

由于 $r_1$ 是特征方程(7-3)的二重根.因此 $r_1^2 +pr_1 + q = 0$ ，且 $2r_{1} + p = 0$ ，于是得

$$
u ^ {\prime \prime} = 0.
$$

因为这里只要得到一个不为常数的解,所以不妨选取 u=x, 由此得到微分方程(7-2)的另一个解

$$
y _ {2} = x \mathrm{e} ^ {r _ {1} x}.
$$

从而微分方程(7-2)的通解为

$$
y = C _ {1} \mathrm{e} ^ {r _ {1} x} + C _ {2} x \mathrm{e} ^ {r _ {1} x},
$$

即

$$
y = (C _ {1} + C _ {2} x) \mathrm{e} ^ {r _ {1} x}.
$$

(iii) 特征方程有一对共轭复根:  $r_{1}=\alpha+\beta i, r_{2}=\alpha-\beta i (\beta \neq 0)$

这时， $y_{1}=\mathrm{e}^{(\alpha+\beta\mathrm{i})x},y_{2}=\mathrm{e}^{(\alpha-\beta\mathrm{i})x}$ 是微分方程(7-2)的两个解，但它们是复值函数形式.为了得出实值函数形式的解，先利用欧拉公式 $e^{i\theta}=\cos\theta+i\sin\theta$ 把 $y_{1},y_{2}$ 改写为

$$
y _ {1} = \mathrm{e} ^ {(\alpha + \beta \mathrm{i}) x} = \mathrm{e} ^ {\alpha x} \cdot \mathrm{e} ^ {\beta x \mathrm{i}} = \mathrm{e} ^ {\alpha x} (\cos \beta x + \mathrm{i} \sin \beta x),
$$

$$
y _ {2} = \mathrm{e} ^ {(\alpha - \beta \mathrm{i}) x} = \mathrm{e} ^ {\alpha x} \cdot \mathrm{e} ^ {- \beta x \mathrm{i}} = \mathrm{e} ^ {\alpha x} (\cos \beta x - \mathrm{i} \sin \beta x).
$$

由于复值函数  $y_{1}$  与  $y_{2}$  之间成共轭关系, 因此, 取它们的和除以 2 就得到它们的实部, 取它们的差除以 2i 就得到它们的虚部. 由于方程 (7-2) 的解符合叠加原理, 所以实值函数

$$
\bar {y} _ {1} = \frac {1}{2} (y _ {1} + y _ {2}) = \mathrm{e} ^ {\alpha x} \cos \beta x, \quad \bar {y} _ {2} = \frac {1}{2 \mathrm{i}} (y _ {1} - y _ {2}) = \mathrm{e} ^ {\alpha x} \sin \beta x
$$

还是微分方程(7-2)的解,且 $\frac{\bar{y}_{1}}{\bar{y}_{2}}=\frac{e^{\alpha x}\cos\beta x}{e^{\alpha x}\sin\beta x}=\cot\beta x$ 不是常数,所以微分方程(7-2)的通解为

$$
y = \mathrm{e} ^ {\alpha x} (C _ {1} \cos \beta x + C _ {2} \sin \beta x).
$$

综上所述,求二阶常系数齐次线性微分方程

$$
y ^ {\prime \prime} + p y ^ {\prime} + q y = 0 \tag {7-2}
$$

的通解的步骤如下:

第一步 写出微分方程(7-2)的特征方程

$$
r ^ {2} + p r + q = 0. \tag {7-3}
$$

第二步 求出特征方程(7-3)的两个根 $r_1, r_2$.

第三步 根据特征方程(7-3)的两个根的不同情形,按照下列表格写出微分方程(7-2)的通解:

| 特征方程 $r^{2} + pr + q = 0$ 的两个根 $r_{1}, r_{2}$ | 微分方程 $y'' + py' + qy = 0$ 的通解 |
| --- | --- |
| 两个不相等的实根 $r_{1}, r_{2}$ | $y = C_{1} e^{r_{1}x} + C_{2} e^{r_{2}x}$ |
| 两个相等的实根 $r_{1} = r_{2}$ | $y = (C_{1} + C_{2}x) e^{r_{1}x}$ |
| 一对共轭复根 $r_{1,2} = \alpha \pm \beta i$ | $y = e^{\alpha x} (C_{1} \cos \beta x + C_{2} \sin \beta x)$ |

例 1 求微分方程  $y''-2y'-3y=0$  的通解.

解 所给微分方程的特征方程为

$$
r ^ {2} - 2 r - 3 = 0,
$$

其根 $r_1 = -1, r_2 = 3$ 是两个不相等的实根，因此所求通解为

$$
y = C _ {1} \mathrm{e} ^ {- x} + C _ {2} \mathrm{e} ^ {3 x}.
$$

例2 求方程 $\frac{\mathrm{d}^2s}{\mathrm{d}t^2} + 2\frac{\mathrm{d}s}{\mathrm{d}t} + s = 0$ 满足初值条件 $s|_{t=0} = 4, s'|_{t=0} = -2$ 的特解.

解 所给方程的特征方程为

$$
r ^ {2} + 2 r + 1 = 0,
$$

其根 $r_1 = r_2 = -1$ 是两个相等的实根，因此所求微分方程的通解为

$$
s = (C _ {1} + C _ {2} t) \mathrm{e} ^ {- t}.
$$

将条件 $s\mid_{t = 0} = 4$ 代入通解，得 $C_1 = 4$ ，从而

$$
s = (4 + C _ {2} t) \mathrm{e} ^ {- t}.
$$

将上式对 t 求导, 得

$$
s ^ {\prime} = (C _ {2} - 4 - C _ {2} t) \mathrm{e} ^ {- t}.
$$

再把条件 $s' \mid_{t=0} = -2$ 代入上式, 得 $C_2 = 2$. 于是所求特解为

$$
s = (4 + 2 t) \mathrm{e} ^ {- t}.
$$

例 3 求微分方程  $y''-2y'+5y=0$  的通解.

解 所给方程的特征方程为

$$
r ^ {2} - 2 r + 5 = 0,
$$

其根  $r_{1,2}=1\pm2i$  为一对共轭复根. 因此所求通解为

$$
y = \mathrm{e} ^ {x} (C _ {1} \cos 2 x + C _ {2} \sin 2 x).
$$

例 4 在第六节例 1 中, 设物体只受弹性恢复力 f 的作用, 且在初始时刻 t=0 的位置为  $x=x_{0}$ , 初始速度为  $\frac{dx}{dt}\bigg|_{t=0}=v_{0}$ . 求反映物体运动规律的函数  $x=x(t)$ .

解 由于不计阻力 R, 即假设  $-\mu \frac{dx}{dt} = 0$ , 所以方程 (6-1) 成为

$$
\frac {\mathrm{d} ^ {2} x}{\mathrm{d} t ^ {2}} + k ^ {2} x = 0, \tag {7-4}
$$

方程(7-4)叫做无阻尼自由振动的微分方程.

反映物体运动规律的函数 $x = x(t)$ 是满足微分方程(7-4)及初值条件

$$
x \mid_ {t = 0} = x _ {0}, \left. \frac {\mathrm{d} x}{\mathrm{d} t} \right| _ {t = 0} = v _ {0}
$$

的特解.

方程(7-4)的特征方程为 $r^{2}+k^{2}=0$ ，其根 $r=\pm ki$ 是一对共轭复根，所以方程(7-4)的通解为

$$
x = C _ {1} \cos k t + C _ {2} \sin k t.
$$

应用初值条件,定出  $C_{1}=x_{0}, C_{2}=\frac{v_{0}}{k}$ . 因此,所求的特解为

$$
x = x _ {0} \cos k t + \frac {v _ {0}}{k} \sin k t. \tag {7-5}
$$

为了便于说明特解所反映的振动现象,我们令

$$
x _ {0} = A \sin \varphi , \quad \frac {v _ {0}}{k} = A \cos \varphi \quad (0 \leqslant \varphi <   2 \pi),
$$

于是(7-5)式成为

$$
x = A \sin (k t + \varphi), \tag {7-6}
$$

其中

$$
A = \sqrt {x _ {0} ^ {2} + \frac {v _ {0} ^ {2}}{k ^ {2}}}, \quad \tan \varphi = \frac {k x _ {0}}{v _ {0}}.
$$

函数(7-6)的图形如图7-10所示(图中假定 $x_{0}>0,v_{0}>0$ ).

![](images/page_350_chart_17.jpg)

<details>
<summary>line</summary>

| Parameter | Value |
| --- | --- |
| Amplitude (at peak) | A |
| Amplitude (at trough) | -A |
| Period (T) | T |
</details>

图7-10

函数(7-6)所反映的运动就是简谐振动.这个振动的振幅为A,初相为 $\varphi$ ,周期为 $T=\frac{2\pi}{k}$ ,角频率为k.由于 $k=\sqrt{\frac{c}{m}}$ （见第六节例1),它与初值条件无关,而完全由振动系统(在本例中就是弹簧和物体所组成的系统)本身所确定.因此,k又叫做系统的固有频率.固有频率是反映振动系统特性的一个重要参数.

例 5 在第六节例 1 中, 设物体受弹簧的恢复力 f 和阻力 R 的作用, 且在初始时刻 t=0 的位置  $x=x_{0}$ , 初始速度  $\frac{dx}{dt}\bigg|_{t=0}=v_{0}$ , 求反映物体运动规律的函数  $x=x(t)$ .

解 这就是要找满足有阻尼的自由振动方程

$$
\frac {\mathrm{d} ^ {2} x}{\mathrm{d} t ^ {2}} + 2 n \frac {\mathrm{d} x}{\mathrm{d} t} + k ^ {2} x = 0 \tag {7-7}
$$

及初值条件

$$
x \mid_ {t = 0} = x _ {0}, \quad \frac {\mathrm{d} x}{\mathrm{d} t} \Big | _ {t = 0} = v _ {0}
$$

的特解.

方程(7-7)的特征方程为 $r^{2}+2nr+k^{2}=0$ ，其根为

$$
r = \frac {- 2 n \pm \sqrt {4 n ^ {2} - 4 k ^ {2}}}{2} = - n \pm \sqrt {n ^ {2} - k ^ {2}}.
$$

以下按 $n < k, n > k$ 及 $n = k$ 三种不同情形分别进行讨论.

(i) 小阻尼情形: n < k

特征方程的根 $r = -n \pm \omega \mathrm{i}$ ($\omega = \sqrt{k^2 - n^2}$) 是一对共轭复根, 所以方程(7-7)的通解为

$$
x = \mathrm{e} ^ {- n t} (C _ {1} \cos \omega t + C _ {2} \sin \omega t).
$$

应用初值条件定出 $C_1 = x_0, C_2 = \frac{v_0 + nx_0}{\omega}$，因此所求特解为

$$
x = \mathrm{e} ^ {- n t} \left(x _ {0} \cos \omega t + \frac {v _ {0} + n x _ {0}}{\omega} \sin \omega t\right). \tag {7-8}
$$

如例 4 中所做的那样,令

$$
x _ {0} = A \sin \varphi , \quad \frac {v _ {0} + n x _ {0}}{\omega} = A \cos \varphi \quad (0 \leqslant \varphi <   2 \pi), \tag {7-9}
$$

那么(7-8)式又可写成

$$
x = A \mathrm{e} ^ {- n t} \sin (\omega t + \varphi), \tag {7-10}
$$

其中

$$
\omega = \sqrt {k ^ {2} - n ^ {2}}, \quad A = \sqrt {x _ {0} ^ {2} + \frac {\left(v _ {0} + n x _ {0}\right) ^ {2}}{\omega^ {2}}}, \quad \tan \varphi = \frac {x _ {0} \omega}{v _ {0} + n x _ {0}}.
$$

从(7-10)式看出,物体的运动是周期为 $T=\frac{2\pi}{\omega}$ 的振动.但与简谐振动不同,它的振幅 $Ae^{-nt}$ 随时间t的增大而逐渐减小.因此,物体随时间t的增大而趋于平衡位置.

函数(7-10)的图形如图7-11所示(图中假定 $x_{0}=0,v_{0}>0$ ).

(ii) 大阻尼情形: n > k