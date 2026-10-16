# 第7章 微分方程

原始 PDF 第 306–441 页。

## 第七章

## 微分方程

函数是客观事物的内部联系在数量方面的反映,利用函数关系又可以对客观事物的规律性进行研究.因此如何寻求函数关系,在实践中具有重要意义.在许多问题中,往往不能直接找出所需要的函数关系,但是根据问题所提供的情况,有时可以列出含有要找的函数及其导数的关系式.这样的关系式就是所谓微分方程.微分方程建立以后,对它进行研究,求出未知函数,这就是解微分方程.本章主要介绍微分方程的一些基本概念和几种常用的微分方程的解法.

## 第一节 微分方程的基本概念

下面我们通过几何、力学及物理学中的几个具体例题来说明微分方程的基本概念.

例1 一曲线通过点(1,2)，且在该曲线上任一点 $M(x,y)$ 处的切线的斜率为 $2x$，求这曲线的方程.

解 设所求曲线的方程为  $y=\varphi(x)$ . 根据导数的几何意义, 可知未知函数  $y=\varphi(x)$  应满足关系式

$$
\frac {\mathrm{d} y}{\mathrm{d} x} = 2 x. \tag {1-1}
$$

此外,未知函数  $y=\varphi(x)$  还应满足下列条件:

$$
x = 1 \text {时}, \quad y = 2. \tag {1-2}
$$

把(1-1)式两端积分, 得  $y=\int2x\,dx$  即

$$
y = x ^ {2} + C, \tag {1-3}
$$

其中 C 是任意常数.

289

---

第七章 微分方程

把条件“x=1时,y=2”代入(1-3)式,得

$$
2 = 1 ^ {2} + C,
$$

由此定出 $C = 1$ .把 $C = 1$ 代入(1-3)式，即得所求曲线方程

$$
y = x ^ {2} + 1. \tag {1-4}
$$

例 2 列车沿直线以  $20 \, m/s$  （相当于  $72 \, km/h$ ）的速度行驶，当制动时列车获得加速度  $-0.4 \, m/s^{2}$ . 问开始制动后多少时间列车才能停住以及列车在这段时间里行驶了多少路程？

解 设列车在开始制动后 t s 时行驶了 s m. 根据题意, 反映制动阶段列车运动规律的函数  $s = s(t)$  应满足关系式

$$
\frac {\mathrm{d} ^ {2} s}{\mathrm{d} t ^ {2}} = - 0. 4. \tag {1-5}
$$

此外,未知函数  $s=s(t)$  还应满足下列条件:

$$
t = 0 \text {时,} \quad s = 0, \quad v = \frac {\mathrm{d} s}{\mathrm{d} t} = 2 0. \tag {1-6}
$$

把(1-5)式两端积分一次,得

$$
v = \frac {\mathrm{d} s}{\mathrm{d} t} = - 0. 4 t + C _ {1}, \tag {1-7}
$$

再积分一次,得

$$
s = - 0. 2 t ^ {2} + C _ {1} t + C _ {2}, \tag {1-8}
$$

这里  $C_{1}, C_{2}$  都是任意常数.

把条件“t=0 时，v=20”代入(1-7)式，得

$$
2 0 = C _ {1},
$$

把条件“t=0 时,s=0”代入(1-8)式,得

$$
0 = C _ {2}.
$$

把 $C_1, C_2$ 的值代入(1-7)及(1-8)式，得

$$
v = - 0. 4 t + 2 0, \tag {1-9}
$$

$$
s = - 0. 2 t ^ {2} + 2 0 t. \tag {1-10}
$$

在(1-9)式中令 $v = 0$ ，得到列车从开始制动到完全停住所需的时间

$$
t = \frac {2 0}{0 . 4} = 5 0 (\mathrm{s}).
$$

再把 $t = 50$ 代入(1-10)式，得到列车在制动阶段行驶的路程

$$
s = - 0. 2 \times 5 0 ^ {2} + 2 0 \times 5 0 = 5 0 0 (\mathrm{m}).
$$

上述两个例子中的关系式(1-1)和(1-5)都含有未知函数的导数,它们都是微分方程.一般地,凡表示未知函数、未知函数的导数与自变量之间的关系的方程,叫做微

290

---

第一节 微分方程的基本概念

分方程,有时也简称方程.

微分方程中所出现的未知函数的最高阶导数的阶数, 叫做微分方程的阶. 例如, 方程(1-1)是一阶微分方程, 方程(1-5)是二阶微分方程. 又如, 方程

$$
x ^ {3} y ^ {\prime \prime \prime} + x ^ {2} y ^ {\prime \prime} - 4 x y ^ {\prime} = 3 x ^ {2}
$$

是三阶微分方程,方程

$$
y ^ {(4)} - 4 y ^ {\prime \prime \prime} + 1 0 y ^ {\prime \prime} - 1 2 y ^ {\prime} + 5 y = \sin 2 x
$$

是四阶微分方程.

一般地，$n$ 阶微分方程的形式是

$$
F (x, y, y ^ {\prime}, \dots , y ^ {(n)}) = 0. \tag {1-11}
$$

这里必须指出,在方程(1-11)中, $y^{(n)}$ 是必须出现的,而 $x,y,y',\cdots,y^{(n-1)}$ 等则可以不出现.例如n阶微分方程

$$
y ^ {(n)} + 1 = 0
$$

中，除 $y^{(n)}$ 外，$y$ 的其他阶导数和自变量 $x$ 都没有出现

如果能从方程(1-11)中解出最高阶导数,那么可得微分方程

$$
y ^ {(n)} = f (x, y, y ^ {\prime}, \dots , y ^ {(n - 1)}). \tag {1-12}
$$

以后我们讨论的微分方程都是已解出最高阶导数的方程或能解出最高阶导数的方程.

由前面的例子我们看到,在研究某些实际问题时,首先要建立微分方程,然后找出满足微分方程的函数(解微分方程),就是说,找出这样的函数,把这函数代入微分方程能使该方程成为恒等式.这个函数就叫做该微分方程的解.确切地说,设函数 $y=\varphi(x)$ 在区间I上有n阶连续导数,如果在区间I上,

$$
f [ x, \varphi (x), \varphi^ {\prime} (x), \dots , \varphi^ {(n)} (x) ] \equiv 0,
$$

那么函数  $y=\varphi(x)$  就叫做微分方程 (1-11) 在区间 I 上的解.

例如,函数(1-3)和(1-4)都是微分方程(1-1)的解,函数(1-8)和(1-10)都是微分方程(1-5)的解.

如果微分方程的解中含有任意常数,且任意常数的个数与微分方程的阶数相同①,这样的解叫做微分方程的通解.例如,函数(1-3)是方程(1-1)的解,它含有1个任意常数,而方程(1-1)是一阶的,所以函数(1-3)是方程(1-1)的通解.又如,函数(1-8)是方程(1-5)的解,它含有2个任意常数,而方程(1-5)是二阶的,所以函数(1-8)是方程(1-5)的通解.

由于通解中含有任意常数,所以它还不能完全确定地反映函数所代表的某一个客观事物的规律性.要完全确定地反映客观事物的规律性,必须确定这些常数的值.为

![](../../raw/pages_0289-0320/images/page_307_image_21.jpg)

释疑解难

7-1

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 这里所说的任意常数是相互独立的, 就是说, 它们不能合并而使得任意常数的个数减少(参看本章第六节关于函数组的线性相关性).</span></small>

291

---

第七章 微分方程

此,要根据问题的实际情况,提出确定这些常数的条件.例如,例1中的条件(1-2)及例2中的条件(1-6)便是这样的条件.

设微分方程中的未知函数为  $y=\varphi(x)$ ，如果微分方程是一阶的，通常用来确定任意常数的条件是

$$
x = x _ {0} \text {时}, \quad y = y _ {0},
$$

或写成

$$
y \mid_ {x = x _ {0}} = y _ {0},
$$

其中 $x_0, y_0$ 都是给定的值；如果微分方程是二阶的，通常用来确定任意常数的条件是

$$
x = x _ {0} \text {时}, \quad y = y _ {0}, \quad y ^ {\prime} = y _ {0} ^ {\prime},
$$

或写成

$$
y \mid_ {x = x _ {0}} = y _ {0}, \quad y ^ {\prime} \mid_ {x = x _ {0}} = y _ {0} ^ {\prime},
$$

其中 $x_0, y_0$ 和 $y_0'$ 都是给定的值. 上述这种条件叫做初值条件.

确定了通解中的任意常数以后, 就得到微分方程的特解. 例如(1-4)式是方程(1-1)满足条件(1-2)的特解,(1-10)式是方程(1-5)满足条件(1-6)的特解.

求微分方程  $y' = f(x, y)$  满足初值条件  $y \mid_{x=x_{0}} = y_{0}$  的特解这样一个问题，叫做一阶微分方程的初值问题，记作

$$
\left\{ \begin{array}{l} y ^ {\prime} = f (x, y), \\ y \mid_ {x = x _ {0}} = y _ {0}. \end{array} \right. \tag {1-13}
$$

微分方程的解的图形是一条曲线,叫做微分方程的积分曲线.初值问题(1-13)的几何意义,就是求微分方程的通过点 $(x_{0},y_{0})$ 的那条积分曲线.二阶微分方程的初值问题

$$
\left\{ \begin{array}{l} y ^ {\prime \prime} = f (x, y, y ^ {\prime}), \\ y \mid_ {x = x _ {0}} = y _ {0}, y ^ {\prime} \mid_ {x = x _ {0}} = y _ {0} ^ {\prime} \end{array} \right.
$$

的几何意义,是求微分方程的通过点 $(x_{0},y_{0})$ 且在该点处的切线斜率为 $y_{0}^{\prime}$ 的那条积分曲线.

例 3 验证: 函数

$$
x = C _ {1} \cos k t + C _ {2} \sin k t \tag {1-14}
$$

是微分方程

$$
\frac {\mathrm{d} ^ {2} x}{\mathrm{d} t ^ {2}} + k ^ {2} x = 0 \tag {1-15}
$$

的解.

解 求出所给函数(1-14)的导数

$$
\frac {\mathrm{d} x}{\mathrm{d} t} = - k C _ {1} \sin k t + k C _ {2} \cos k t, \tag {1-16}
$$

292

---

第一节 微分方程的基本概念

$$
\frac {\mathrm{d} ^ {2} x}{\mathrm{d} t ^ {2}} = - k ^ {2} C _ {1} \cos k t - k ^ {2} C _ {2} \sin k t = - k ^ {2} (C _ {1} \cos k t + C _ {2} \sin k t).
$$

把 $\frac{\mathrm{d}^2x}{\mathrm{d}t^2}$ 及 $x$ 的表达式代入方程(1-15)，得

$$
- k ^ {2} (C _ {1} \cos k t + C _ {2} \sin k t) + k ^ {2} (C _ {1} \cos k t + C _ {2} \sin k t) \equiv 0.
$$

函数(1-14)及其二阶导数代入方程(1-15)后成为一个恒等式,因此函数(1-14)是微分方程(1-15)的解.

例 4 已知函数(1-14)当  $k \neq 0$  时是微分方程(1-15)的通解, 求满足初值条件

$$
x \mid_ {t = 0} = A, \quad \frac {\mathrm{d} x}{\mathrm{d} t} \bigg | _ {t = 0} = 0
$$

的特解.

解 将条件“t=0 时, x=A”代入(1-14)式得

$$
C _ {1} = A.
$$

将条件“t=0 时, $\frac{dx}{dt}=0$ ”代入(1-16)式,得

$$
C _ {2} = 0.
$$

把 $C_1, C_2$ 的值代入(1-14)式, 就得所求的特解

$$
x = A \cos k t.
$$

## 习题 7-1

1. 试说出下列各微分方程的阶数:

(1) $x(y')^2 - 2yy' + x = 0$;

(2) $x^{2}y^{\prime \prime} - xy^{\prime} + y = 0;$

(3)  $xy''' + 2y'' + x^{2}y = 0;$

(4) $(7x-6y)\mathrm{d}x+(x+y)\mathrm{d}y=0;$

(5) $L\frac{\mathrm{d}^{2}Q}{\mathrm{d}t^{2}}+R\frac{\mathrm{d}Q}{\mathrm{d}t}+\frac{Q}{C}=0;$

(6) $\frac{\mathrm{d}\rho}{\mathrm{d}\theta} + \rho = \sin^2\theta.$

2. 指出下列各题中的函数是不是所给微分方程的解:

(1) $xy' = 2y, y = 5x^2$;
(2)  $y'' + y = 0, y = 3 \sin x - 4 \cos x;$
(3) $y''-2y'+y=0,y=x^{2}e^{x};$
(4) $y''-(\lambda_1+\lambda_2)y'+\lambda_1\lambda_2y=0,y=C_1e^{\lambda_1x}+C_2e^{\lambda_2x}.$

3. 在下列各题中, 验证所给二元方程所确定的函数为所给微分方程的解:

(1) $(x-2y)y'=2x-y,x^{2}-xy+y^{2}=C;$
(2) $(xy-x)y''+xy'^{2}+yy'-2y'=0,y=\ln(xy).$

4. 在下列各题中, 确定函数关系式中所含的参数, 使函数满足所给的初值条件:

293

---

第七章 微分方程

(1) $x^{2} - y^{2} = C, y \mid_{x=0} = 5$;
(2) $y = (C_1 + C_2x)\mathrm{e}^{2x},y\mid_{x = 0} = 0,y' \mid_{x = 0} = 1;$
(3) $y = C_1 \sin(x - C_2), y \mid_{x = \pi} = 1, y' \mid_{x = \pi} = 0.$

5. 写出由下列条件确定的曲线所满足的微分方程:

(1) 曲线在点 $(x,y)$ 处的切线的斜率等于该点横坐标的平方；
(2) 曲线上点  $P(x,y)$  处的法线与 x 轴的交点为 Q，且线段 PQ 被 y 轴平分；
(3) 曲线上点  $P(x,y)$  处的切线与 y 轴的交点为 Q，线段 PQ 的长度为 a，且曲线通过点  $(a,0)$ .

6. 用微分方程表示一物理命题: 某种气体的压强 p 对于温度 T 的变化率与压强成正比, 与温度的平方成反比.

7. 一个半球体形状的雪堆, 其体积融化率与半球面面积 A 成正比, 比例系数 k > 0. 假设在融化过程中雪堆始终保持半球体形状, 已知半径为  $r_{0}$  的雪堆在开始融化的 3 h 内, 融化了其体积的  $\frac{7}{8}$ , 问雪堆全部融化需要多少时间?

## 第二节 可分离变量的微分方程

本节至第四节,我们讨论一阶微分方程

$$
y ^ {\prime} = f (x, y) \tag {2-1}
$$

的一些解法.

一阶微分方程有时也写成如下的对称形式:

$$
P (x, y) \mathrm{d} x + Q (x, y) \mathrm{d} y = 0. \tag {2-2}
$$

在方程(2-2)中,变量 x 与 y 对称,它既可看作是以 x 为自变量 y 为因变量的方程

$$
\frac {\mathrm{d} y}{\mathrm{d} x} = - \frac {P (x , y)}{Q (x , y)}
$$

（这时 $Q(x,y)\neq 0$），也可看作是以 $y$ 为自变量 $x$ 为因变量的方程

$$
\frac {\mathrm{d} x}{\mathrm{d} y} = - \frac {Q (x , y)}{P (x , y)}
$$

(这时  $P(x,y) \neq 0$ ).

在第一节的例 1 中, 我们遇到一阶微分方程

$$
\frac {\mathrm{d} y}{\mathrm{d} x} = 2 x,
$$

或

$$
\mathrm{d} y = 2 x \mathrm{d} x.
$$

把上式两端积分就得到这个方程的通解

294

---

第二节 可分离变量的微分方程

$$
y = x ^ {2} + C.
$$

但是并不是所有的一阶微分方程都能这样求解.例如,对于一阶微分方程

$$
\frac {\mathrm{d} y}{\mathrm{d} x} = 2 x y ^ {2}, \tag {2-3}
$$

就不能像上面那样用直接对两端积分的方法求出它的通解.这是什么缘故呢？原因是方程(2-3)的右端含有与 $x$ 存在函数关系的变量 $y$ ，积分

$$
\int 2 x y ^ {2} \mathrm{d} x
$$

求不出来, 这是困难所在. 为了解决这个困难, 在方程(2-3)的两端同时乘 $\frac{dx}{y^{2}}$ , 使方程(2-3)变为

$$
\frac {\mathrm{d} y}{y ^ {2}} = 2 x \mathrm{d} x,
$$

这样,变量 x 与 y 已分离在等式的两端,然后两端积分得

$$
- \frac {1}{y} = x ^ {2} + C,
$$

或

$$
y = - \frac {1}{x ^ {2} + C}, \tag {2-4}
$$

其中 C 是任意常数.

可以验证,函数(2-4)确实满足一阶微分方程(2-3),且含有一个任意常数,所以它是方程(2-3)的通解.

一般地,如果一个一阶微分方程能写成

$$
g (y) \mathrm{d} y = f (x) \mathrm{d} x \tag {2-5}
$$

的形式,就是说,能把微分方程写成一端只含 y 的函数和 dy,另一端只含 x 的函数和 dx,那么原方程就称为可分离变量的微分方程.

假定方程(2-5)中的函数 $g(y)$ 和 $f(x)$ 是连续的.设 $y = \varphi (x)$ 是方程(2-5)的解，将它代入(2-5)中得到恒等式

$$
g [ \varphi (x) ] \varphi^ {\prime} (x) \mathrm{d} x = f (x) \mathrm{d} x.
$$

将上式两端积分,并由  $y=\varphi(x)$  引进变量 y, 得

$$
\int g (y) \mathrm{d} y = \int f (x) \mathrm{d} x.
$$

设 $G(y)$ 及 $F(x)$ 依次为 $g(y)$ 及 $f(x)$ 的原函数，于是有

$$
G (y) = F (x) + C. \tag {2-6}
$$

因此，方程(2-5)的解满足关系式(2-6).反之，如果 $y = \Phi (x)$ 是由关系式(2-6)所确

295

---

第七章 微分方程

定的隐函数,那么在  $g(y) \neq 0$  的条件下,  $y = \Phi(x)$  也是方程(2-5)的解,事实上,由隐函数的求导法可知,当  $g(y) \neq 0$  时,

$$
\Phi^ {\prime} (x) = \frac {F ^ {\prime} (x)}{G ^ {\prime} (y)} = \frac {f (x)}{g (y)},
$$

这就表示函数 $y = \Phi(x)$ 满足方程(2-5). 所以, 如果已分离变量的方程(2-5)中, $g(y)$ 和 $f(x)$ 是连续的, 且 $g(y) \neq 0$, 那么(2-5)式两端积分后得到的关系式(2-6), 就用隐式给出了方程(2-5)的解, (2-6)式就叫做微分方程(2-5)的隐式解. 又由于关系式(2-6)中含有任意常数, 因此(2-6)式所确定的隐函数是方程(2-5)的通解, 所以(2-6)式叫做微分方程(2-5)的隐式通解 (当 $f(x) \neq 0$ 时, (2-6)式所确定的隐函数 $x = \Psi(y)$ 也可认为是方程(2-5)的解).

例1 求微分方程

$$
\frac {\mathrm{d} y}{\mathrm{d} x} = 2 x y \tag {2-7}
$$

的通解.

解 方程(2-7)是可分离变量的,分离变量后得

$$
\frac {\mathrm{d} y}{y} = 2 x \mathrm{d} x,
$$

两端积分

$$
\int \frac {\mathrm{d} y}{y} = \int 2 x \mathrm{d} x,
$$

得

$$
\ln | y | = x ^ {2} + C _ {1},
$$

从而

$$
y = \pm \mathrm{e} ^ {x ^ {2} + C _ {1}} = \pm \mathrm{e} ^ {C _ {1}} \mathrm{e} ^ {x ^ {2}}.
$$

因 $\pm \mathrm{e}^{c_1}$ 是任意非零常数，又 $y\equiv 0$ 也是方程(2-7)的解，故得方程(2-7)的通解

$$
y = C \mathrm{e} ^ {x ^ {2}},
$$

其中 C 为任意常数.

例 2 放射性元素铀由于不断地有原子放射出微粒子而变成其他元素,铀的含量就不断减少,这种现象叫做衰变.由原子物理学知道,铀的衰变速度与当时未衰变的铀原子的含量 M 成正比.已知 t=0 时铀的含量为  $M_{0}$ , 求在衰变过程中铀含量  $M(t)$  随时间 t 变化的规律.

解 铀的衰变速度就是  $M(t)$  对时间 t 的导数  $\frac{dM}{dt}$ . 由于铀的衰变速度与其含量成正比, 故得微分方程

296

---

第二节 可分离变量的微分方程

$$
\frac {\mathrm{d} M}{\mathrm{d} t} = - \lambda M, \tag {2-8}
$$

其中  $\lambda (\lambda > 0)$  是常数, 叫做衰变系数,  $\lambda$  前置负号是由于当 t 增加时 M 单调减少, 即  $\frac{dM}{dt} < 0$  的缘故.

按题意,初值条件为

$$
M \mid_ {t = 0} = M _ {0}.
$$

方程(2-8)是可分离变量的.分离变量后得

$$
\frac {\mathrm{d} M}{M} = - \lambda \mathrm{d} t.
$$

两端积分

$$
\int \frac {\mathrm{d} M}{M} = \int (- \lambda) \mathrm{d} t,
$$

以  $\ln C$  表示任意常数, 考虑到 M > 0, 得

$$
\ln M = - \lambda t + \ln C,
$$

即

$$
M = C \mathrm{e} ^ {- \lambda t}.
$$

这就是方程(2-8)的通解.以初值条件代入上式,得

$$
M _ {0} = C \mathrm{e} ^ {0} = C,
$$

所以

$$
M = M _ {0} \mathrm{e} ^ {- \lambda t},
$$

这就是所求铀的衰变规律.由此可见,铀的含量随时间的增加而按指数规律衰减(图7-1).

例 3 跳伞人从跳伞塔跳下后, 假设降落伞同时打开, 且所受空气阻力与速度成正比, 并设降落伞离开跳伞塔时  $(t=0)$  速度为零, 求降落伞下落速度与时间的函数关系.

![](../../raw/pages_0289-0320/images/page_313_chart_19.jpg)

<details>
<summary>line</summary>

| Time (t) | Value (M) |
| --- | --- |
| 0 | M0 |
| >0 | <M0 |
</details>

图7-1

解 设降落伞下落速度为  $v(t)$ . 降落伞在空中下落

时,同时受到重力 P 与阻力 R 的作用(图 7-2).重力大小为 mg,方向与 v 一致;阻力大小为 kv (k 为比例系数),方向与 v 相反,从而降落伞所受外力为

$$
F = m g - k v.
$$

根据牛顿第二运动定律

$$
F = m a
$$

297

---

第七章 微分方程

(其中 a 为加速度), 得函数  $v(t)$  应满足的方程为

$$
m \frac {\mathrm{d} v}{\mathrm{d} t} = m g - k v. \tag {2-9}
$$

按题意,初值条件为

$$
v \mid_ {t = 0} = 0.
$$

方程(2-9)是可分离变量的.分离变量后得

$$
\frac {\mathrm{d} v}{m g - k v} = \frac {\mathrm{d} t}{m},
$$

两端积分

$$
\int \frac {\mathrm{d} v}{m g - k v} = \int \frac {\mathrm{d} t}{m},
$$

考虑到 mg-kv>0, 得

$$
- \frac {1}{k} \ln (m g - k v) = \frac {t}{m} + C _ {1},
$$

即

$$
m g - k v = \mathrm{e} ^ {- \frac {k}{m} t - k C _ {1}},
$$

或

$$
v = \frac {m g}{k} + C \mathrm{e} ^ {- \frac {k}{m} t} \quad \left(C = - \frac {\mathrm{e} ^ {- k C _ {1}}}{k}\right), \tag {2-10}
$$

这就是方程(2-9)的通解.

将初值条件 $v\mid_{t = 0} = 0$ 代入(2-10)式，得

$$
C = - \frac {m g}{k}.
$$

于是所求的特解为

$$
v = \frac {m g}{k} (1 - \mathrm{e} ^ {- \frac {k}{m} t}). \tag {2-11}
$$

由(2-11)可以看出,随着时间 t 的增大,速度 v 逐渐接近于常数  $\frac{mg}{k}$ ,且不会超过  $\frac{mg}{k}$ ,也就是说,跳伞后开始阶段是加速运动,但以后逐渐接近于等速运动.

例 4 有高为 1 m 的半球形容器, 水从它的底部小孔流出, 小孔横截面面积为  $1 \, cm^{2}$  (图 7-3). 开始时容器内盛满了水, 求水从小孔流出过程中容器里水面的高度 h (水面与孔口中心间的距离) 随时间 t 变化的规律, 并求水流完所需的时间.

解 由力学知道,水从孔口流出的流量(即通过孔口横截面的水的体积 V 对时间 t 的变化率)Q 可用下列公式计算:

![](../../raw/pages_0289-0320/images/page_314_image_23.jpg)

<details>
<summary>text_image</summary>

R=kv
P=mg
</details>

图7-2

298

---

第二节 可分离变量的微分方程

$$
Q = \frac {\mathrm{d} V}{\mathrm{d} t} = k S \sqrt {2 g h}, \tag {2-12}
$$

其中 k 为流量系数,由实验测得 k=0.62, S 为孔口横截面面积, g 为重力加速度.

另一方面,设在微小时间间隔 $[t,t+dt]$ 内,水面高度由h降至 $h+\mathrm{d}h\left(\mathrm{d}h<0\right)$ ,则又可得到

$$
\mathrm{d} V = - \pi r ^ {2} \mathrm{d} h, \tag {2-13}
$$

其中 r 是时刻 t 时的水面半径(图 7-3)，右端置负号是由于 dh<0 而 dV>0 的缘故. 又因

$$
r = \sqrt {1 ^ {2} - (1 - h) ^ {2}} = \sqrt {2 h - h ^ {2}},
$$

所以(2-13)式变成

$$
\mathrm{d} V = - \pi (2 h - h ^ {2}) \mathrm{d} h. \tag {2-14}
$$

比较(2-12)和(2-14)两式,得

$$
k S \sqrt {2 g h} \mathrm{d} t = - \pi (2 h - h ^ {2}) \mathrm{d} h, \tag {2-15}
$$

这就是未知函数  $h=h(t)$  应满足的微分方程.

![](../../raw/pages_0289-0320/images/page_315_image_12.jpg)

<details>
<summary>text_image</summary>

h
h+dh
r
O
h
1 m
</details>

图7-3

此外,开始时容器内的水是满的,所以未知函数  $h=h(t)$  还应满足下列初值条件:

$$
h \mid_ {t = 0} = 1. \tag {2-16}
$$

方程(2-15)是可分离变量的.分离变量后得

$$
\mathrm{d} t = - \frac {\pi}{k S \sqrt {2 g}} (2 h ^ {\frac {1}{2}} - h ^ {\frac {3}{2}}) \mathrm{d} h.
$$

两端积分,得

$$
t = - \frac {\pi}{k S \sqrt {2 g}} \left(\frac {4}{3} h ^ {\frac {3}{2}} - \frac {2}{5} h ^ {\frac {5}{2}} + C\right), \tag {2-17}
$$

其中 C 是任意常数.

把初值条件(2-16)代入(2-17)式,得

$$
C = - \frac {4}{3} + \frac {2}{5} = - \frac {1 4}{1 5}.
$$

把所得的 C 值代入(2-17)式并化简,就得

$$
t = \frac {1 4 \pi}{1 5 k S \sqrt {2 g}} \left(1 - \frac {1 0}{7} h ^ {\frac {3}{2}} + \frac {3}{7} h ^ {\frac {5}{2}}\right).
$$

以 $k = 0.62, S = 10^{-4} \mathrm{~m}^2, g = 9.8 \mathrm{~m/s}^2$ 代入上式，计算后可得

$$
t = 1. 0 6 8 \times 1 0 ^ {4} \left(1 - \frac {1 0}{7} h ^ {\frac {3}{2}} + \frac {3}{7} h ^ {\frac {5}{2}}\right) \mathrm{s}.
$$

上式表达了水从小孔流出的过程中容器内水面高度 h 与时间 t 之间的函数关系.由此可知水流完所需的时间为

299

---

第七章 微分方程

$$
t = 1. 0 6 8 \times 1 0 ^ {4} \mathrm{s} = 2 \mathrm{h} 5 8 \mathrm{min}.
$$

图

释疑解难

7-2

这里还要指出,在例4中我们是通过对微小量dV的分析得到微分方程(2-15)的.这种微小量分析的方法,也是建立微分方程的一种常用方法.

## 习题 7-2

1. 求下列微分方程的通解:

(1)  $xy'-y\ln y=0;$

(2) $3x^{2} + 5x - 5y' = 0$;

(3)  $\sqrt{1-x^{2}}y'=\sqrt{1-y^{2}}$ ;

(4) $y' - xy' = a(y^2 + y')$;

(5)  $\sec^{2}x \tan y dx + \sec^{2}y \tan x dy = 0;$

(6) $\frac{\mathrm{dy}}{\mathrm{dx}} = 10^{x + y}$;

(7) $(\mathrm{e}^{x + y} - \mathrm{e}^x)\mathrm{d}x + (\mathrm{e}^{x + y} + \mathrm{e}^y)\mathrm{d}y = 0;$

(8)  $\cos x \sin y dx + \sin x \cos y dy = 0;$

(9) $(y+1)^{2}\frac{\mathrm{d}y}{\mathrm{d}x}+x^{3}=0;$

(10) $y\mathrm{d}x + (x^2 - 4x)\mathrm{d}y = 0.$

2. 求下列微分方程满足所给初值条件的特解:

(1)  $y' = e^{2x - y}$ ,  $y \mid_{x=0} = 0;$

(2)  $\cos x \sin y \, dy = \cos y \sin x \, dx, y \mid_{x=0} = \frac{\pi}{4};$

(3)  $y'\sin x = y \ln y, y \mid_{x = \frac{\pi}{2}} = e;$

(4)  $\cos y\mathrm{d}x+(1+\mathrm{e}^{-x})\sin y\mathrm{d}y=0,y\mid_{x=0}=\frac{\pi}{4};$

(5)  $x \, dy + 2y \, dx = 0, y \mid_{x=2} = 1;$

(6) $\frac{1}{\rho}\frac{\mathrm{d}\rho}{\mathrm{d}\theta}+\frac{\rho^{2}+1}{\rho^{2}-1}\cot\theta=0,\rho\mid_{\theta=\frac{\pi}{6}}=3;$

(7) $x^{2}(1+y'^{2})=a^{2},y\mid_{x=a}=0$ ,其中a>0.

3. 有一盛满了水的圆锥形漏斗, 高为 $10 \mathrm{~cm}$, 顶角为 $60^{\circ}$, 漏斗下面有面积为 $0.5 \mathrm{~cm}^{2}$ 的孔, 求水面高度变化的规律及水流完所需的时间.

4. 质量为 1 g 的质点受外力作用做直线运动, 这外力和时间成正比, 和质点运动的速度成反比. 在  $t = 10 \, s$  时, 速度等于  $50 \, cm/s$ , 外力为  $4 \, g \cdot cm/s^{2}$ , 问从运动开始经过了  $1 \, min$  后的速度是多少?

5. 镭的衰变有如下的规律: 镭的衰变速度与它的现存量 R 成正比. 由经验材料得知, 镭经过 1600 年后, 只余原始量  $R_{0}$  的一半. 试求镭的现存量 R 与时间 t 的函数关系.

6. 一曲线通过点(2,3)，它在两坐标轴间的任一切线线段均被切点所平分，求这曲线方程.

7. 小船从河边点 O 处出发驶向对岸(两岸为平行直线). 设船速为 a, 小船航行的方向始终与河岸垂直, 又设河宽为 h, 河中任一点处的水流速度与该点到两岸距离的乘积成正比(比例系数为 k). 求小船的航行路线.

300

---

第三节 齐次方程

## 第三节 齐次方程

## 一、齐次方程

如果一阶微分方程可化成

$$
\frac {\mathrm{d} y}{\mathrm{d} x} = \varphi \left(\frac {y}{x}\right) \tag {3-1}
$$

的形式,那么就称这方程为齐次方程,例如

$$
(x y - y ^ {2}) \mathrm{d} x - (x ^ {2} - 2 x y) \mathrm{d} y = 0
$$

是齐次方程,因为它可化成

$$
\frac {\mathrm{d} y}{\mathrm{d} x} = \frac {x y - y ^ {2}}{x ^ {2} - 2 x y},
$$

即

$$
\frac {\mathrm{d} y}{\mathrm{d} x} = \frac {\frac {y}{x} - \left(\frac {y}{x}\right) ^ {2}}{1 - 2 \left(\frac {y}{x}\right)}.
$$

在齐次方程

$$
\frac {\mathrm{d} y}{\mathrm{d} x} = \varphi \left(\frac {y}{x}\right)
$$

中,引进新的未知函数

$$
u = \frac {y}{x}, \tag {3-2}
$$

就可把它化为可分离变量的方程. 因为由(3-2)有

$$
y = u x, \quad \frac {\mathrm{d} y}{\mathrm{d} x} = u + x \frac {\mathrm{d} u}{\mathrm{d} x},
$$

代入方程(3-1)，便得方程

$$
u + x \frac {\mathrm{d} u}{\mathrm{d} x} = \varphi (u),
$$

即

$$
x \frac {\mathrm{d} u}{\mathrm{d} x} = \varphi (u) - u.
$$

分离变量,得

301

---

第七章 微分方程

$$
\frac {\mathrm{d} u}{\varphi (u) - u} = \frac {\mathrm{d} x}{x}.
$$

两端积分,得

$$
\int \frac {\mathrm{d} u}{\varphi (u) - u} = \int \frac {\mathrm{d} x}{x}.
$$

求出积分后,再以 $\frac{y}{x}$ 代替u,便得所给齐次方程的通解.

例1 解方程

$$
y ^ {2} + x ^ {2} \frac {\mathrm{d} y}{\mathrm{d} x} = x y \frac {\mathrm{d} y}{\mathrm{d} x}.
$$

解 原方程可写成

$$
\frac {\mathrm{d} y}{\mathrm{d} x} = \frac {y ^ {2}}{x y - x ^ {2}} = \frac {\left(\frac {y}{x}\right) ^ {2}}{\frac {y}{x} - 1},
$$

因此是齐次方程.令 $\frac{y}{x}=u$ ,则

$$
y = x u, \quad \frac {\mathrm{d} y}{\mathrm{d} x} = u + x \frac {\mathrm{d} u}{\mathrm{d} x},
$$

于是原方程变为

$$
u + x \frac {\mathrm{d} u}{\mathrm{d} x} = \frac {u ^ {2}}{u - 1},
$$

即

$$
x \frac {\mathrm{d} u}{\mathrm{d} x} = \frac {u}{u - 1}.
$$

分离变量,得

$$
\left(1 - \frac {1}{u}\right) \mathrm{d} u = \frac {\mathrm{d} x}{x}.
$$

两端积分,得

$$
u - \ln | u | + C _ {1} = \ln | x |,
$$

或写为

$$
\ln | x u | = u + C _ {1}.
$$

以 $\frac{y}{x}$ 代上式中的u,便得所给方程的通解为

$$
\ln | y | = \frac {y}{x} + C _ {1} \quad \text {或} \quad y = C \mathrm{e} ^ {\frac {y}{x}} (C = \pm \mathrm{e} ^ {C _ {1}}).
$$

302

---

第三节 齐次方程

例 2 探照灯的聚光镜的镜面是一张旋转曲面, 它的形状由 xOy 坐标面上的一条曲线 L 绕 x 轴旋转而成. 按聚光镜性能的要求, 在其旋转轴 (x 轴) 上一点 O 处发出的一切光线, 经它反射后都与旋转轴平行. 求曲线 L 的方程.

解 将光源所在之 $O$ 点取作坐标原点（图7-4），且曲线 $L$ 位于 $y \geqslant 0$ 范围内.

![](../../raw/pages_0289-0320/images/page_319_image_3.jpg)

<details>
<summary>text_image</summary>

y
T
L
M
α
S
α
A
O
P
N
x
</details>

图7-4

设点 $M(x,y)$ 为 $L$ 上的任一点，点 $O$ 发出的某条光线

经点 $M$ 反射后是一条与 $x$ 轴平行的直线 $MS$. 又设过点 $M$ 的切线 $AT$ 与 $x$ 轴的夹角为 $\alpha$. 根据题意, $\angle SMT = \alpha$. 另一方面, $\angle OMA$ 是入射角的余角, $\angle SMT$ 是反射角的余角, 于是由光学中的反射定律有 $\angle OMA = \angle SMT = \alpha$. 从而 $AO = OM$, 但 $AO = AP - OP = PM\cot \alpha - OP = \frac{y}{y'} - x$, 而 $OM = \sqrt{x^2 + y^2}$. 于是得微分方程

$$
\frac {y}{y ^ {\prime}} - x = \sqrt {x ^ {2} + y ^ {2}}.
$$

把 $x$ 看作因变量, $y$ 看作自变量, 当 $y > 0$ 时, 上式即为

$$
\frac {\mathrm{d} x}{\mathrm{d} y} = \frac {x}{y} + \sqrt {\left(\frac {x}{y}\right) ^ {2} + 1},
$$

这是齐次方程. 令 $\frac{x}{y} = v$，则 $x = yv, \frac{\mathrm{d}x}{\mathrm{d}y} = v + y\frac{\mathrm{d}v}{\mathrm{d}y}$，代入上式，得

$$
v + y \frac {\mathrm{d} v}{\mathrm{d} y} = v + \sqrt {v ^ {2} + 1},
$$

即

$$
y \frac {\mathrm{d} v}{\mathrm{d} y} = \sqrt {v ^ {2} + 1}.
$$

分离变量,得

$$
\frac {\mathrm{d} v}{\sqrt {v ^ {2} + 1}} = \frac {\mathrm{d} y}{y}.
$$

积分,得

$$
\ln (v + \sqrt {v ^ {2} + 1}) = \ln y - \ln C,
$$

或

$$
v + \sqrt {v ^ {2} + 1} = \frac {y}{C}.
$$

由

$$
\left(\frac {y}{C} - v\right) ^ {2} = v ^ {2} + 1,
$$

303

---

第七章 微分方程

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

304

---

第三节 齐次方程

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

305

---

第七章 微分方程

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

306

---

第四节 一阶线性微分方程

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

307

---

第七章 微分方程

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

![](../../raw/pages_0321-0352/images/page_324_image_26.jpg)

释疑解难

7-3

308

---

第四节 一阶线性微分方程

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

![](../../raw/pages_0321-0352/images/page_325_image_21.jpg)

<details>
<summary>text_image</summary>

R
L
E
S
</details>

图7-5

309

---

第七章 微分方程

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

310

---

第四节 一阶线性微分方程

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

311

---

第七章 微分方程

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

312

---

第五节 可降阶的高阶微分方程

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

313

---

第七章 微分方程

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

314

---

第五节 可降阶的高阶微分方程

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

315

---

第七章 微分方程

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

316

---

第五节 可降阶的高阶微分方程

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

![](../../raw/pages_0321-0352/images/page_333_image_6.jpg)

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

317

---

第七章 微分方程

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

318

---

第五节 可降阶的高阶微分方程

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

![](../../raw/pages_0321-0352/images/page_335_image_14.jpg)

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

319

---

第七章 微分方程

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

320

---

第六节 高阶线性微分方程

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

如果使物体具有一个初始速度 $v_{0} \neq 0$ ，那么物体便离开平衡位置，并在平衡位置附

321

---

第七章 微分方程

近做上下振动.在振动过程中,物体的位置 x 随时间 t 变化,即 x 与 t 之间存在函数关系:  $x = x(t)$ .要确定物体的振动规律,就要求出函数  $x = x(t)$ .

由力学知道,弹簧使物体回到平衡位置的弹性恢复力f(它不包括在平衡位置时和重力mg相平衡的那一部分弹性力)和物体离开平衡位置的位移x成正比:

$$
f = - c x,
$$

其中 c 为弹簧的弹性系数, 负号表示弹性恢复力的方向和物体位移的方向相反.

![](../../raw/pages_0321-0352/images/page_338_image_5.jpg)

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

322

---

第六节 高阶线性微分方程

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

![](../../raw/pages_0321-0352/images/page_339_image_8.jpg)

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

323

---

第七章 微分方程

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

324

---

第六节 高阶线性微分方程

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

325

---

第七章 微分方程

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

326

---

第六节 高阶线性微分方程

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

327

---

第七章 微分方程

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

328

---

第六节 高阶线性微分方程

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

329

---

第七章 微分方程

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

330

---

第七节 常系数齐次线性微分方程

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

331

---

第七章 微分方程

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

332

---

第七节 常系数齐次线性微分方程

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

333

---

第七章 微分方程

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

![](../../raw/pages_0321-0352/images/page_350_chart_17.jpg)

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

334

---

第七节 常系数齐次线性微分方程

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

335

---

第七章 微分方程

特征方程的根 $r_1 = -n + \sqrt{n^2 - k^2}, r_2 = -n - \sqrt{n^2 - k^2}$ 是两个不相等的负实根，所以方程(7-7)的通解为

$$
x = C _ {1} \mathrm{e} ^ {- (n - \sqrt {n ^ {2} - k ^ {2}}) t} + C _ {2} \mathrm{e} ^ {- (n + \sqrt {n ^ {2} - k ^ {2}}) t}, \tag {7-11}
$$

其中任意常数  $C_{1}, C_{2}$  可以由初值条件来确定.

从(7-11)式看出,使x=0的t值最多只有一个,即物体最多越过平衡位置一次,因此物体已不再有振动现象.又当 $t\to+\infty$ 时, $x\to0$ .因此,物体随时间t的增大而趋于平衡位置.

函数(7-11)的图形如图7-12所示(图中假定 $x_{0}>0,v_{0}>0$ ).

![](../../raw/pages_0353-0384/images/page_352_image_6.jpg)

<details>
<summary>text_image</summary>

x
O
T
t
</details>

图7-11

![](../../raw/pages_0353-0384/images/page_352_chart_8.jpg)

<details>
<summary>line</summary>

| Time (t) | Value (x) |
| --- | --- |
| 0 | ~High |
| Peak | ~Highest |
| End | ~Low |
</details>

图7-12

(iii) 临界阻尼情形: n = k

特征方程的根  $r_{1}=r_{2}=-n$  是两个相等的实根, 所以方程(7-7)的通解为

$$
x = \mathrm{e} ^ {- n t} (  C _ {1} + C _ {2} t)  ,
$$

其中任意常数 $C_1$ 及 $C_2$ 可由初值条件来确定. 由上式可看出, 在临界阻尼情形使 $x = 0$ 的 $t$ 值也最多只有一个, 因此物体也不再有振动现象. 又由于

$$
\lim _ {t \to + \infty} t \mathrm{e} ^ {- n t} = \lim _ {t \to + \infty} \frac {t}{\mathrm{e} ^ {n t}} = \lim _ {t \to + \infty} \frac {1}{n \mathrm{e} ^ {n t}} = 0,
$$

从而可以看出, 当  $t \to +\infty$  时,  $x \to 0$ . 因此, 在临界阻尼情形, 物体也随时间 t 的增大而趋于平衡位置.

上面讨论二阶常系数齐次线性微分方程所用的方法以及方程的通解的形式,可推广到 n 阶常系数齐次线性微分方程上去,对此我们不再详细讨论,只简单地叙述于下:

n 阶常系数齐次线性微分方程的一般形式是

$$
y ^ {(n)} + p _ {1} y ^ {(n - 1)} + p _ {2} y ^ {(n - 2)} + \dots + p _ {n - 1} y ^ {\prime} + p _ {n} y = 0, \tag {7-12}
$$

其中  $p_{1}, p_{2}, \cdots, p_{n-1}, p_{n}$  都是常数.

有时我们用记号 D（叫做微分算子）表示对 x 求导的运算  $\frac{d}{dx}$ ，把  $\frac{dy}{dx}$  记作 Dy，把  $\frac{d^{n}y}{dx^{n}}$  记作  $D^{n}y$ ，并把方程(7-12)记作

336

---

第七节 常系数齐次线性微分方程

$$
(\mathrm{D} ^ {n} + p _ {1} \mathrm{D} ^ {n - 1} + \dots + p _ {n - 1} \mathrm{D} + p _ {n}) y = 0. \tag {7-13}
$$

记

$$
L (\mathrm{D}) = \mathrm{D} ^ {n} + p _ {1} \mathrm{D} ^ {n - 1} + \dots + p _ {n - 1} \mathrm{D} + p _ {n},
$$

$L(\mathrm{D})$ 叫做微分算子 $\mathrm{D}$ 的 $n$ 次多项式.于是方程(7-13)可记作

$$
L (\mathrm{D}) y = 0.
$$

如同讨论二阶常系数齐次线性微分方程那样，令 $y = \mathrm{e}^{rx}$. 由于 $\mathrm{De}^{rx} = r\mathrm{e}^{rx}, \dots, \mathrm{D}^n\mathrm{e}^{rx} = r^n\mathrm{e}^{rx}$，故 $L(\mathrm{D})\mathrm{e}^{rx} = L(r)\mathrm{e}^{rx}$. 因此把 $y = \mathrm{e}^{rx}$ 代入方程(7-13)，得

$$
L (r) \mathrm{e} ^ {r x} = 0.
$$

由此可见,如果选取 r 是 n 次代数方程  $L(r)=0$  即

$$
r ^ {n} + p _ {1} r ^ {n - 1} + p _ {2} r ^ {n - 2} + \dots + p _ {n - 1} r + p _ {n} = 0 \tag {7-14}
$$

的根,那么作出的函数  $y=e^{rx}$  就是方程(7-13)的一个解.

方程(7-14)叫做方程(7-13)的特征方程.

根据特征方程的根,可以写出其对应的微分方程的解如下:

| 特征方程的根 | 微分方程通解中的对应项 |
| --- | --- |
| 单实根 r | 给出一项:$Ce^{rx}$ |
| 一对单复根 $r_{1,2} = \alpha \pm \beta i$ | 给出两项:$e^{\alpha x}(C_1 \cos \beta x + C_2 \sin \beta x)$ |
| k 重实根 r | 给出 k 项:$e^{rx}(C_1 + C_2 x + \cdots + C_k x^{k-1})$ |
| 一对 k 重复根 $r_{1,2} = \alpha \pm \beta i$ | 给出 2k 项:$e^{\alpha x}[(C_1 + C_2 x + \cdots + C_k x^{k-1}) \cos \beta x + (D_1 + D_2 x + \cdots + D_k x^{k-1}) \sin \beta x]$ |

从代数学知道, $n$ 次代数方程有 $n$ 个根(重根按重数计算),而特征方程的每一个根都对应着通解中的一项,且每项各含一个任意常数,这样就得到 $n$ 阶常系数齐次线性微分方程的通解

$$
y = C _ {1} y _ {1} + C _ {2} y _ {2} + \dots + C _ {n} y _ {n}.
$$

例 6 求方程  $y^{(4)}-2y'''+5y''=0$  的通解.

解 这里的特征方程为

$$
r ^ {4} - 2 r ^ {3} + 5 r ^ {2} = 0,
$$

即

$$
r ^ {2} (r ^ {2} - 2 r + 5) = 0.
$$

它的根是 $r_1 = r_2 = 0$ 和 $r_{3,4} = 1\pm 2\mathrm{i}$ .因此所给微分方程的通解为

$$
y = C _ {1} + C _ {2} x + \mathrm{e} ^ {x} (C _ {3} \cos 2 x + C _ {4} \sin 2 x).
$$

例7 求方程 $\frac{\mathrm{d}^4w}{\mathrm{d}x^4} +\beta^4 w = 0$ 的通解，其中 $\beta >0$

337

---

第七章 微分方程

解 这里的特征方程为

$$
r ^ {4} + \beta^ {4} = 0.
$$

由于

$$
r ^ {4} + \beta^ {4} = r ^ {4} + 2 r ^ {2} \beta^ {2} + \beta^ {4} - 2 r ^ {2} \beta^ {2} = (r ^ {2} + \beta^ {2}) ^ {2} - 2 r ^ {2} \beta^ {2} = (r ^ {2} - \sqrt {2} \beta r + \beta^ {2}) (r ^ {2} + \sqrt {2} \beta r + \beta^ {2}),
$$

所以特征方程可以写为

$$
(r ^ {2} - \sqrt {2} \beta r + \beta^ {2}) (r ^ {2} + \sqrt {2} \beta r + \beta^ {2}) = 0.
$$

它的根为 $r_{1,2} = \frac{\beta}{\sqrt{2}} (1\pm \mathrm{i}),r_{3,4} = -\frac{\beta}{\sqrt{2}} (1\pm \mathrm{i})$ ，因此所给方程的通解为

$$
w = \mathrm{e} ^ {\frac {\beta}{\sqrt {2}} x} \left(C _ {1} \cos \frac {\beta}{\sqrt {2}} x + C _ {2} \sin \frac {\beta}{\sqrt {2}} x\right) + \mathrm{e} ^ {- \frac {\beta}{\sqrt {2}} x} \left(C _ {3} \cos \frac {\beta}{\sqrt {2}} x + C _ {4} \sin \frac {\beta}{\sqrt {2}} x\right).
$$

## 习题 7-7

1. 下题中给出了四个结论,从中选一个正确的结论:

在下列微分方程中, 以  $y = C_{1} e^{-x} + C_{2} \cos x + C_{3} \sin x$  ( $C_{1}, C_{2}, C_{3}$  为任意常数) 为通解的常系数齐次线性微分方程是().

(A)  $y''' + y'' - y' - y = 0$

(B) $y^{\prime \prime \prime} + y^{\prime \prime} + y^{\prime} + y = 0$

(C)  $y'''-y''-y'+y=0$

(D)  $y'''-y''-y'-y=0$

2. 求下列微分方程的通解:

(1)  $y'' + y' - 2y = 0;$

(2) $y''-4y'=0;$

(3)  $y''+y=0;$

(4) $y''+6y'+13y=0;$

(5) $4\frac{d^{2}x}{dt^{2}}-20\frac{dx}{dt}+25x=0;$

(6)  $y''-4y'+5y=0;$

(7)  $y^{(4)} - y = 0;$

(8) $y^{(4)}+2y''+y=0;$

(9)  $y^{(4)} - 2y''' + y'' = 0;$

(10) $y^{(4)} + 5y'' - 36y = 0.$

3. 求下列微分方程满足所给初值条件的特解:

(1)  $y''-4y'+3y=0, y \mid_{x=0}=6, y' \mid_{x=0}=10;$

(2) $4y''+4y'+y=0,y\mid_{x=0}=2,y'\mid_{x=0}=0;$

(3) $y''-3y'-4y=0,y\mid_{x=0}=0,y'\mid_{x=0}=-5;$

(4) $y'' + 4y' + 29y = 0, y \mid_{x=0} = 0, y' \mid_{x=0} = 15;$

(5)  $y''+25y=0, y \mid_{x=0}=2, y' \mid_{x=0}=5;$

(6) $y''-4y'+13y=0,y\mid_{x=0}=0,y'\mid_{x=0}=3.$

338

---

第八节 常系数非齐次线性微分方程

4. 一个单位质量的质点在数轴上运动, 开始时质点在原点 O 处且速度为  $v_{0}$ , 在运动过程中, 它

受到一个力的作用,这个力的大小与质点到原点的距离成正比(比例系数 $k_{1}>0$ )而方向与初速度一致.又介质的阻力与速度成正比(比例系数 $k_{2}>0$ ).求反映这质点的运动规律的函数.

5. 在图 7-13 所示的电路中先将开关 S 拨向 A, 达到稳定状态后再将开关 S 拨向 B, 求电压  $u_{C}(t)$  及电流  $i(t)$ . 已知 E = 20 V,  $C = 0.5 \times 10^{-6}$  F, L = 0.1 H, R = 2000 Ω.

6. 设圆柱形浮筒的底面直径为 0.5 m, 将它铅直放在水中,
当稍向下压后突然放开, 浮筒在水中上下振动的周期为 2 s, 求浮筒的质量.

![](../../raw/pages_0353-0384/images/page_355_image_5.jpg)

<details>
<summary>text_image</summary>

A B
S
C
R
E L
</details>

图 7-13

## 第八节 常系数非齐次线性微分方程

本节着重讨论二阶常系数非齐次线性微分方程的解法,并对 n 阶方程的解法作必要的说明.

二阶常系数非齐次线性微分方程的一般形式是

$$
y ^ {\prime \prime} + p y ^ {\prime} + q y = f (x), \tag {8-1}
$$

其中 p, q 是常数.

由第六节定理 3 可知, 求二阶常系数非齐次线性微分方程的通解, 归结为求对应的齐次方程

$$
y ^ {\prime \prime} + p y ^ {\prime} + q y = 0 \tag {8-2}
$$

的通解和非齐次方程(8-1)本身的一个特解.由于二阶常系数齐次线性微分方程的通解的求法已在第七节得到解决,所以这里只需讨论求二阶常系数非齐次线性微分方程的一个特解 $y^{*}$ 的方法.

本节只介绍当方程(8-1)中的 $f(x)$ 取两种常见形式时求 $y^{*}$ 的方法.这种方法的特点是不用积分就可求出 $y^{*}$ 来,它叫做待定系数法. $f(x)$ 的两种形式是

(1) $f(x)=\mathrm{e}^{\lambda x}P_{m}(x)$ ，其中 $\lambda$ 是常数， $P_{m}(x)$ 是x的一个m次多项式

$$
P _ {m} (x) = a _ {0} x ^ {m} + a _ {1} x ^ {m - 1} + \dots + a _ {m - 1} x + a _ {m};
$$

(2) $f(x)=\mathrm{e}^{\lambda x}\left[P_{l}(x)\cos\omega x+Q_{n}(x)\sin\omega x\right]$ ，其中 $\lambda,\omega$ 是常数， $\omega\neq0,P_{l}(x),Q_{n}(x)$ 分别是x的l次、n次多项式，且仅有一个可为零.

下面分别介绍 $f(x)$ 为上述两种形式时 $y^{*}$ 的求法.

## 一、 $f(x) = \mathrm{e}^{\lambda x}P_m(x)$ 型

我们知道,方程(8-1)的特解 $y^{*}$ 是使(8-1)成为恒等式的函数.怎样的函数能使

339

---

第七章 微分方程

(8-1) 成为恒等式呢？因为(8-1)式右端 $f(x)$ 是多项式 $P_{m}(x)$ 与指数函数 $\mathrm{e}^{\lambda x}$ 的乘积，而多项式与指数函数乘积的导数仍然是多项式与指数函数的乘积，因此，我们推测 $y^{*} = R(x)\mathrm{e}^{\lambda x}$ （其中 $R(x)$ 是某个多项式）可能是方程(8-1)的特解. 把 $y^{*}, y^{*'}$ 及 $y^{*''}$ 代入方程(8-1)，然后考虑能否选取适当的多项式 $R(x)$，使 $y^{*} = R(x)\mathrm{e}^{\lambda x}$ 满足方程(8-1). 为此，将

$$
\begin{array}{l} y ^ {*} = R (x) \mathrm{e} ^ {\lambda x}, \\ y ^ {* \prime} = \mathrm{e} ^ {\lambda x} [ \lambda R (x) + R ^ {\prime} (x) ], \\ y ^ {* \prime \prime} = \mathrm{e} ^ {\lambda x} \left[ \lambda^ {2} R (x) + 2 \lambda R ^ {\prime} (x) + R ^ {\prime \prime} (x) \right] \\ \end{array}
$$

代入方程(8-1)并消去 $e^{\lambda x}$ ，得

$$
R ^ {\prime \prime} (x) + (2 \lambda + p) R ^ {\prime} (x) + \left(\lambda^ {2} + p \lambda + q\right) R (x) = P _ {m} (x). \tag {8-3}
$$

(i) 如果 $\lambda$ 不是(8-2)式的特征方程 $r^2 + pr + q = 0$ 的根, 即 $\lambda^2 + p\lambda + q \neq 0$, 由于 $P_m(x)$ 是一个 $m$ 次多项式, 要使(8-3)的两端恒等, 那么可令 $R(x)$ 为另一个 $m$ 次多项式 $R_m(x)$:

$$
R _ {m} (x) = b _ {0} x ^ {m} + b _ {1} x ^ {m - 1} + \dots + b _ {m - 1} x + b _ {m},
$$

代入(8-3)式, 比较等式两端 x 同次幂的系数, 就得到以  $b_{0}, b_{1}, \cdots, b_{m}$  作为未知数的  $m+1$  个方程的联立方程组. 从而可以定出这些  $b_{i} (i=0,1,\cdots,m)$ , 并得到所求的特解  $y^{*}=R_{m}(x)\mathrm{e}^{\lambda x}$ .

(ii) 如果 $\lambda$ 是特征方程 $r^2 + pr + q = 0$ 的单根, 即 $\lambda^2 + p\lambda + q = 0$, 但 $2\lambda + p \neq 0$, 要使 (8-3) 的两端恒等, 那么 $R'(x)$ 必须是 $m$ 次多项式. 此时可令

$$
R (x) = x R _ {m} (x),
$$

并且可用同样的方法来确定  $R_{m}(x)$  的系数  $b_{i}$  ( $i=0,1,2,\cdots,m$ ).

（iii）如果 $\lambda$ 是特征方程 $r^2 + pr + q = 0$ 的重根，即 $\lambda^2 + p\lambda + q = 0$ ，且 $2\lambda + p = 0$ ，要使(8-3)的两端恒等，那么 $R''(x)$ 必须是 $m$ 次多项式.此时可令

$$
R (x) = x ^ {2} R _ {m} (x),
$$

并用同样的方法来确定  $R_{m}(x)$  中的系数.

综上所述,我们有如下结论:

如果 $f(x) = \mathrm{e}^{\lambda x}P_m(x)$，那么二阶常系数非齐次线性微分方程(8-1)具有形如

$$
y ^ {*} = x ^ {k} R _ {m} (x) \mathrm{e} ^ {\lambda x} \tag {8-4}
$$

的特解, 其中  $R_{m}(x)$  是与  $P_{m}(x)$  同次 (m 次) 的多项式, 而 k 按  $\lambda$  不是特征方程的根、是特征方程的单根或是特征方程的重根依次取为 0,1 或 2.

上述结论可推广到 n 阶常系数非齐次线性微分方程,但要注意(8-4)式中的 k 是特征方程含根  $\lambda$  的重复次数(即若  $\lambda$  不是特征方程的根,则 k 取为 0;若  $\lambda$  是特征方程的 s 重根,则 k 取为 s).

340

---

第八节 常系数非齐次线性微分方程

例1 求微分方程 $y'' - 2y' - 3y = 3x + 1$ 的一个特解.

解 这是二阶常系数非齐次线性微分方程,且函数 $f(x)$ 是 $\mathrm{e}^{\lambda x}P_{m}(x)$ 型(其中 $\lambda = 0, P_{m}(x) = 3x + 1$).

与所给方程对应的齐次方程为

$$
y ^ {\prime \prime} - 2 y ^ {\prime} - 3 y = 0,
$$

它的特征方程为

$$
r ^ {2} - 2 r - 3 = 0.
$$

由于这里  $\lambda=0$  不是特征方程的根, 所以应设特解为

$$
y ^ {*} = b _ {0} x + b _ {1}.
$$

把它代入所给方程,得

$$
- 3 b _ {0} x - 2 b _ {0} - 3 b _ {1} = 3 x + 1,
$$

比较等式两端 x 同次幂的系数, 得

$$
\left\{ \begin{array}{l} - 3 b _ {0} = 3, \\ - 2 b _ {0} - 3 b _ {1} = 1. \end{array} \right.
$$

由此求得 $b_{0} = -1, b_{1} = \frac{1}{3}$. 于是求得一个特解为

$$
y ^ {*} = - x + \frac {1}{3}.
$$

例 2 求微分方程  $y''-5y'+6y=xe^{2x}$  的通解.

解 所给方程也是二阶常系数非齐次线性微分方程, 且 $f(x)$ 呈 $\mathrm{e}^{\lambda x}P_{m}(x)$ 型 (其中 $\lambda = 2, P_{m}(x) = x$).

与所给方程对应的齐次方程为

$$
y ^ {\prime \prime} - 5 y ^ {\prime} + 6 y = 0,
$$

它的特征方程

$$
r ^ {2} - 5 r + 6 = 0
$$

有两个实根 $r_1 = 2, r_2 = 3$. 于是与所给方程对应的齐次方程的通解为

$$
Y = C _ {1} \mathrm{e} ^ {2 x} + C _ {2} \mathrm{e} ^ {3 x}.
$$

由于  $\lambda=2$  是特征方程的单根, 所以应设  $y^{*}$  为

$$
y ^ {*} = x (b _ {0} x + b _ {1}) \mathrm{e} ^ {2 x}.
$$

把它代入所给方程,得

$$
- 2 b _ {0} x + 2 b _ {0} - b _ {1} = x.
$$

比较等式两端 x 同次幂的系数, 得

$$
\left\{ \begin{array}{l} - 2 b _ {0} = 1, \\ 2 b _ {0} - b _ {1} = 0. \end{array} \right.
$$

341

---

第七章 微分方程

解得 $b_{0} = -\frac{1}{2}, b_{1} = -1.$ 因此求得一个特解为

$$
y ^ {*} = x \left(- \frac {1}{2} x - 1\right) \mathrm{e} ^ {2 x}.
$$

从而所求的通解为

$$
y = C _ {1} \mathrm{e} ^ {2 x} + C _ {2} \mathrm{e} ^ {3 x} - \frac {1}{2} (x ^ {2} + 2 x) \mathrm{e} ^ {2 x}.
$$

## 二、 $f(x) = \mathrm{e}^{\lambda x}[P_l(x)\cos \omega x + Q_n(x)\sin \omega x]$ 型

应用欧拉公式

$$
\cos \theta = \frac {1}{2} (\mathrm{e} ^ {\mathrm{i} \theta} + \mathrm{e} ^ {- \mathrm{i} \theta}), \quad \sin \theta = \frac {1}{2 \mathrm{i}} (\mathrm{e} ^ {\mathrm{i} \theta} - \mathrm{e} ^ {- \mathrm{i} \theta}),
$$

把 $f(x)$ 表示成复变指数函数的形式,有

$$
\begin{array}{l} f (x) = \mathrm{e} ^ {\lambda x} \left(P _ {l} \cos \omega x + Q _ {n} \sin \omega x\right) = \mathrm{e} ^ {\lambda x} \left(P _ {l} \frac {\mathrm{e} ^ {\omega x \mathrm{i}} + \mathrm{e} ^ {- \omega x \mathrm{i}}}{2} + Q _ {n} \frac {\mathrm{e} ^ {\omega x \mathrm{i}} - \mathrm{e} ^ {- \omega x \mathrm{i}}}{2 \mathrm{i}}\right) \\ = \left(\frac {P _ {l}}{2} + \frac {Q _ {n}}{2 \mathrm{i}}\right) \mathrm{e} ^ {(\lambda + \omega \mathrm{i}) x} + \left(\frac {P _ {l}}{2} - \frac {Q _ {n}}{2 \mathrm{i}}\right) \mathrm{e} ^ {(\lambda - \omega \mathrm{i}) x} = P (x) \mathrm{e} ^ {(\lambda + \omega \mathrm{i}) x} + \overline {{P}} (x) \mathrm{e} ^ {(\lambda - \omega \mathrm{i}) x}, \\ \end{array}
$$

其中

$$
P (x) = \frac {P _ {l}}{2} + \frac {Q _ {n}}{2 \mathrm{i}} = \frac {P _ {l}}{2} - \frac {Q _ {n}}{2} \mathrm{i}, \quad \overline {{P}} (x) = \frac {P _ {l}}{2} - \frac {Q _ {n}}{2 \mathrm{i}} = \frac {P _ {l}}{2} + \frac {Q _ {n}}{2} \mathrm{i}
$$

是互成共轭的 $m$ 次多项式（即它们对应项的系数是共轭复数），而 $m = \max \{l, n\}$.

应用上一目的结果,对于 $f(x)$ 中的第一项 $P(x)\mathrm{e}^{(\lambda+\omega\mathrm{i})x}$ ，可求出一个m次多项式 $R_{m}(x)$ ，使得 $y_{1}^{*}=x^{k}R_{m}\mathrm{e}^{(\lambda+\omega\mathrm{i})x}$ 为方程

$$
y ^ {\prime \prime} + p y ^ {\prime} + q y = P (x) \mathrm{e} ^ {(\lambda + \omega \mathrm{i}) x}
$$

的特解, 其中 $k$ 按 $\lambda + \omega \mathrm{i}$ 不是特征方程的根或是特征方程的单根依次取 0 或 1. 由于 $f(x)$ 的第二项 $\overline{P}(x) \mathrm{e}^{(\lambda - \omega \mathrm{i}) x}$ 与第一项 $P(x) \mathrm{e}^{(\lambda + \omega \mathrm{i}) x}$ 成共轭, 所以与 $y_{1}^{*}$ 成共轭的函数 $y_{2}^{*} = x^{k} \overline{R}_{m} \mathrm{e}^{(\lambda - \omega \mathrm{i}) x}$ 必然是方程

$$
y ^ {\prime \prime} + p y ^ {\prime} + q y = \overline {{P}} (x) \mathrm{e} ^ {(\lambda - \omega \mathrm{i}) x}
$$

的特解,这里  $\overline{R}_{m}$  表示与  $R_{m}$  成共轭的 m 次多项式.于是,根据第六节定理 4,方程(8-1)具有形如

$$
y ^ {*} = x ^ {k} R _ {m} \mathrm{e} ^ {(\lambda + \omega \mathrm{i}) x} + x ^ {k} \overline {{R}} _ {m} \mathrm{e} ^ {(\lambda - \omega \mathrm{i}) x}
$$

的特解.上式可写为

$$
\begin{array}{l} y ^ {*} = x ^ {k} \mathrm{e} ^ {\lambda x} \left(R _ {m} \mathrm{e} ^ {\omega x \mathrm{i}} + \overline {{R}} _ {m} \mathrm{e} ^ {- \omega x \mathrm{i}}\right) \\ = x ^ {k} \mathrm{e} ^ {\lambda x} \left[ R _ {m} (\cos \omega x + \mathrm{i} \sin \omega x) + \overline {{R}} _ {m} (\cos \omega x - \mathrm{i} \sin \omega x) \right], \\ \end{array}
$$

342

---

第八节 常系数非齐次线性微分方程

由于括号内的两项是互成共轭的,相加后即无虚部,所以可以写成实函数的形式

$$
y ^ {*} = x ^ {k} \mathrm{e} ^ {\lambda x} \left[ R _ {m} ^ {(1)} (x) \cos \omega x + R _ {m} ^ {(2)} (x) \sin \omega x \right].
$$

综上所述,我们有如下结论:

如果 $f(x) = \mathrm{e}^{\lambda x}[P_l(x)\cos \omega x + Q_n(x)\sin \omega x]$，那么二阶常系数非齐次线性微分方程(8-1)的特解可设为

$$
y ^ {*} = x ^ {k} \mathrm{e} ^ {\lambda x} \left[ R _ {m} ^ {(1)} (x) \cos \omega x + R _ {m} ^ {(2)} (x) \sin \omega x \right], \tag {8-5}
$$

其中 $R_{m}^{(1)}(x), R_{m}^{(2)}(x)$ 是 $m$ 次多项式，$m = \max \{l, n\}$，而 $k$ 按 $\lambda + \omega \mathrm{i}$（或 $\lambda - \omega \mathrm{i}$）不是特征方程的根或是特征方程的单根依次取0或1.

上述结论可推广到 $n$ 阶常系数非齐次线性微分方程, 但要注意 (8-5) 式中的 $k$ 是特征方程中含根 $\lambda + \omega \mathrm{i}$ (或 $\lambda - \omega \mathrm{i}$) 的重复次数.

例3 求微分方程 $y'' + y = x \cos 2x$ 的一个特解.

解 所给方程是二阶常系数非齐次线性方程, 且 $f(x)$ 属于 $\mathrm{e}^{\lambda x}[P_l(x)\cos \omega x + Q_n(x)\sin \omega x]$ 型 (其中 $\lambda = 0, \omega = 2, P_l(x) = x, Q_n(x) = 0$).

与所给方程对应的齐次方程为

$$
y ^ {\prime \prime} + y = 0,
$$

它的特征方程为

$$
r ^ {2} + 1 = 0.
$$

由于这里  $\lambda + \omega i = 2i$  不是特征方程的根, 所以应设特解为

$$
y ^ {*} = (a x + b) \cos 2 x + (c x + d) \sin 2 x.
$$

把它代入所给方程,得

$$
(- 3 a x - 3 b + 4 c) \cos 2 x - (3 c x + 3 d + 4 a) \sin 2 x = x \cos 2 x.
$$

比较等式两端同类项的系数,得

$$
\left\{ \begin{array}{l} - 3 a = 1, \\ - 3 b + 4 c = 0, \\ - 3 c = 0, \\ - 3 d - 4 a = 0, \end{array} \right.
$$

由此解得

$$
a = - \frac {1}{3}, \quad b = 0, \quad c = 0, \quad d = \frac {4}{9}.
$$

于是求得一个特解为

$$
y ^ {*} = - \frac {1}{3} x \cos 2 x + \frac {4}{9} \sin 2 x.
$$

343

---

第七章 微分方程

例 4 求微分方程  $y''-y=e^{x}\cos2x$  的一个特解.

解 这是二阶常系数非齐次线性方程, 且 $f(x)$ 属 $\mathrm{e}^{\lambda x}[P_l(x)\cos \omega x + Q_n(x)\sin \omega x]$ 型 (这里 $\lambda = 1, \omega = 2, P_l(x) = 1, Q_n(x) = 0$).

特征方程为  $r^{2}-1=0$ ，由于  $\lambda+\omega i=1+2i$  不是特征方程的根，所以应设特解为

$$
y ^ {*} = \mathrm{e} ^ {x} (a \cos 2 x + b \sin 2 x).
$$

求导得

$$
y ^ {* \prime} = \mathrm{e} ^ {x} \left[ (a + 2 b) \cos 2 x + (- 2 a + b) \sin 2 x \right],
$$

$$
y ^ {* \prime \prime} = \mathrm{e} ^ {x} \left[ (- 3 a + 4 b) \cos 2 x + (- 4 a - 3 b) \sin 2 x \right].
$$

代入所给方程,得

$$
4 \mathrm{e} ^ {x} [ (- a + b) \cos 2 x - (a + b) \sin 2 x ] = \mathrm{e} ^ {x} \cos 2 x,
$$

比较等式两端同类项的系数,有

$$
\left\{ \begin{array}{l} - a + b = \frac {1}{4}, \\ a + b = 0, \end{array} \right.
$$

解得 $a = -\frac{1}{8}, \quad b = \frac{1}{8}.$

因此所给方程的一个特解为

$$
y ^ {*} = \frac {1}{8} \mathrm{e} ^ {x} (\sin 2 x - \cos 2 x).
$$

例 5 在第六节例 1 中, 设物体受弹性恢复力 f 和铅直干扰力 F 的作用. 试求物体的运动规律.

解 这里需要求出无阻尼强迫振动方程

$$
\frac {\mathrm{d} ^ {2} x}{\mathrm{d} t ^ {2}} + k ^ {2} x = h \sin p t \tag {8-6}
$$

的通解.

对应的齐次微分方程(即无阻尼自由振动方程)为

$$
\frac {\mathrm{d} ^ {2} x}{\mathrm{d} t ^ {2}} + k ^ {2} x = 0, \tag {8-7}
$$

它的特征方程 $r^2 + k^2 = 0$ 的根为 $r = \pm ki$. 故方程(8-7)的通解为

$$
X = C _ {1} \cos k t + C _ {2} \sin k t.
$$

令 $C_1 = A\sin \varphi, C_2 = A\cos \varphi$，则方程(8-7)的通解又可写成

$$
X = A \sin (k t + \varphi),
$$

其中, $A,\varphi$ 为任意常数.

方程(8-6)右端的函数

344

---

第八节 常系数非齐次线性微分方程

$$
f (t) = h \sin p t
$$

与 $f(t) = \mathrm{e}^{\lambda t}[P_l(t)\cos \omega t + Q_n(t)\sin \omega t]$ 相比较，有 $\lambda = 0,\omega = p,P_{l}(t) = 0,Q_{n}(t) = h.$ 现在分别就 $p\neq k$ 和 $p = k$ 两种情形讨论如下:

(i) 如果 $p \neq k$，则 $\lambda \pm \omega \mathrm{i} = \pm p\mathrm{i}$ 不是特征方程的根，故设

$$
x ^ {*} = a _ {1} \cos p t + b _ {1} \sin p t.
$$

代入方程(8-6)求得

$$
a _ {1} = 0, \quad b _ {1} = \frac {h}{k ^ {2} - p ^ {2}},
$$

于是

$$
x ^ {*} = \frac {h}{k ^ {2} - p ^ {2}} \sin p t.
$$

从而当 $p \neq k$ 时, 方程(8-6)的通解为

$$
x = X + x ^ {*} = A \sin (k t + \varphi) + \frac {h}{k ^ {2} - p ^ {2}} \sin p t.
$$

上式表示,物体的运动由两部分组成,这两部分都是简谐振动.上式第一项表示自由振动,第二项所表示的振动叫做强迫振动.强迫振动是干扰力引起的,它的角频率即是干扰力的角频率p;当干扰力的角频率p与振动系统的固有频率k相差很小时,它的振幅 $\left|\frac{h}{k^{2}-p^{2}}\right|$ 可以很大.

(ii) 如果 $p = k$ 那么 $\lambda \pm \omega \mathrm{i} = \pm p\mathrm{i}$ 是特征方程的根. 故设

$$
x ^ {*} = t (a _ {1} \cos k t + b _ {1} \sin k t).
$$

代入方程(8-6)求得

$$
a _ {1} = - \frac {h}{2 k}, \quad b _ {1} = 0.
$$

于是

$$
x ^ {*} = - \frac {h}{2 k} t \cos k t.
$$

从而当 p=k 时, 方程(8-6)的通解为

$$
x = X + x ^ {*} = A \sin (k t + \varphi) - \frac {h}{2 k} t \cos k t.
$$

上式右端第二项表明,强迫振动的振幅 $\frac{h}{2k}t$ 随时间t的增大而无限增大.这就发生所谓共振现象.为了避免共振现象,应使干扰力的角频率p不要靠近振动系统的固有频率k.反之,如果要利用共振现象,那么应使p=k或使p与k尽量靠近.

有阻尼的强迫振动问题可作类似的讨论,这里从略了.

345

---

第七章 微分方程

## 习题7-8

1. 求下列各微分方程的通解:

(1) $2y''+y'-y=2e^{x}$;

(2) $y''+a^{2}y=e^{x}$;

(3) $2y''+5y'=5x^{2}-2x-1;$

(4)  $y''+3y'+2y=3xe^{-x}$ ;

(5) $y''-2y'+5y=e^{x}\sin 2x;$

(6) $y''-6y'+9y=(x+1)e^{3x}$;

(7)  $y''+5y'+4y=3-2x;$

(8) $y''+4y=x\cos x;$

(9)  $y'' + y = e^{x} + \cos x;$

(10)  $y''-y=\sin^{2}x.$

2. 求下列各微分方程满足已给初值条件的特解:

(1) $y'' + y + \sin 2x = 0, y \mid_{x=\pi} = 1, y' \mid_{x=\pi} = 1;$
(2) $y''-3y'+2y=5,y\mid_{x=0}=1,y'\mid_{x=0}=2;$
(3) $y''-10y'+9y=e^{2x},y\mid_{x=0}=\frac{6}{7},y'\mid_{x=0}=\frac{33}{7};$
(4)  $y''-y=4xe^{x}, y \mid_{x=0}=0, y' \mid_{x=0}=1;$
(5) $y''-4y'=5,y\mid_{x=0}=1,y'\mid_{x=0}=0.$

3. 已知二阶常系数齐次线性微分方程 $y'' + my' + ny = 0$ 的通解为 $y = (C_1 + C_2x)e^x$，求 $m, n$ 的值，并求非齐次方程 $y'' + my' + ny = x$ 满足初值条件 $y(0) = 2, y'(0) = 0$ 的特解.

4. 大炮以仰角  $\alpha$ 、初速度  $v_{0}$  发射炮弹，若不计空气阻力，求弹道曲线.

5. 在 RLC 含源串联电路中, 电动势为 E 的电源对电容器 C 充电. 已知  $E = 20 \, V, C = 0.2 \, \mu F, L = 0.1 \, H, R = 1000 \, \Omega$ , 试求合上开关 S 后的电流  $i(t)$  及电压  $u_{c}(t)$ .

6. 设函数  $\varphi(x)$  连续, 且满足

$$
\varphi (x) = \mathrm{e} ^ {x} + \int_ {0} ^ {x} t \varphi (t) \mathrm{d} t - x \int_ {0} ^ {x} \varphi (t) \mathrm{d} t,
$$

求 $\varphi (x)$

## \* 第九节 欧拉方程

变系数的线性微分方程,一般说来都是不容易求解的.但是有些特殊的变系数线性微分方程,则可以通过变量代换化为常系数线性微分方程,因而容易求解,欧拉方程就是其中的一种.

形如

$$
x ^ {n} y ^ {(n)} + p _ {1} x ^ {n - 1} y ^ {(n - 1)} + \dots + p _ {n - 1} x y ^ {\prime} + p _ {n} y = f (x) \tag {9-1}
$$

的方程(其中 $p_{1},p_{2},\cdots,p_{n}$ 为常数)，叫做欧拉方程.

346

---

\* 第九节 欧拉方程

作变换  $x=e^{t}$  或  $t=\ln x$ ，将自变量 x 换成  $t^{①}$ ，我们有

$$
\begin{array}{l} \frac {\mathrm{d} y}{\mathrm{d} x} = \frac {\mathrm{d} y}{\mathrm{d} t} \cdot \frac {\mathrm{d} t}{\mathrm{d} x} = \frac {1}{x} \frac {\mathrm{d} y}{\mathrm{d} t}, \\ \frac {\mathrm{d} ^ {2} y}{\mathrm{d} x ^ {2}} = \frac {1}{x ^ {2}} \left(\frac {\mathrm{d} ^ {2} y}{\mathrm{d} t ^ {2}} - \frac {\mathrm{d} y}{\mathrm{d} t}\right), \\ \frac {\mathrm{d} ^ {3} y}{\mathrm{d} x ^ {3}} = \frac {1}{x ^ {3}} \left(\frac {\mathrm{d} ^ {3} y}{\mathrm{d} t ^ {3}} - 3 \frac {\mathrm{d} ^ {2} y}{\mathrm{d} t ^ {2}} + 2 \frac {\mathrm{d} y}{\mathrm{d} t}\right). \\ \end{array}
$$

如果采用记号 D 表示对 t 求导的运算  $\frac{d}{dt}$ ，那么上述计算结果可以写成

$$
\begin{array}{l} x y ^ {\prime} = \mathrm{D} y, \\ x ^ {2} y ^ {\prime \prime} = \frac {\mathrm{d} ^ {2} y}{\mathrm{d} t ^ {2}} - \frac {\mathrm{d} y}{\mathrm{d} t} = \left(\frac {\mathrm{d} ^ {2}}{\mathrm{d} t ^ {2}} - \frac {\mathrm{d}}{\mathrm{d} t}\right) y = (\mathrm{D} ^ {2} - \mathrm{D}) y = \mathrm{D} (\mathrm{D} - 1) y, \\ x ^ {3} y ^ {\prime \prime \prime} = \frac {\mathrm{d} ^ {3} y}{\mathrm{d} t ^ {3}} - 3 \frac {\mathrm{d} ^ {2} y}{\mathrm{d} t ^ {2}} + 2 \frac {\mathrm{d} y}{\mathrm{d} t} = (\mathrm{D} ^ {3} - 3 \mathrm{D} ^ {2} + 2 \mathrm{D}) y = \mathrm{D} (\mathrm{D} - 1) (\mathrm{D} - 2) y, \\ \end{array}
$$

一般地,有

$$
x ^ {k} y ^ {(k)} = \mathrm{D(D-1)} \dots (\mathrm{D-k+1}) y.
$$

把它代入欧拉方程(9-1)，便得一个以 $t$ 为自变量的常系数线性微分方程.在求出这个方程的解后，把 $t$ 换成 $\ln x$ ，即得原方程的解

例 求欧拉方程  $x^{3}y''' + x^{2}y'' - 4xy' = 3x^{2}$  的通解.

解 作变换 $x = \mathrm{e}^t$ 或 $t = \ln x$ ，原方程化为

$$
\mathrm{D} (\mathrm{D} - 1) (\mathrm{D} - 2) y + \mathrm{D} (\mathrm{D} - 1) y - 4 \mathrm{D} y = 3 \mathrm{e} ^ {2 t},
$$

即

$$
\mathrm{D} ^ {3} y - 2 \mathrm{D} ^ {2} y - 3 \mathrm{D} y = 3 \mathrm{e} ^ {2 t},
$$

或

$$
\frac {\mathrm{d} ^ {3} y}{\mathrm{d} t ^ {3}} - 2 \frac {\mathrm{d} ^ {2} y}{\mathrm{d} t ^ {2}} - 3 \frac {\mathrm{d} y}{\mathrm{d} t} = 3 \mathrm{e} ^ {2 t}. \tag {9-2}
$$

方程(9-2)所对应的齐次方程为

$$
\frac {\mathrm{d} ^ {3} y}{\mathrm{d} t ^ {3}} - 2 \frac {\mathrm{d} ^ {2} y}{\mathrm{d} t ^ {2}} - 3 \frac {\mathrm{d} y}{\mathrm{d} t} = 0, \tag {9-3}
$$

其特征方程为

$$
r ^ {3} - 2 r ^ {2} - 3 r = 0,
$$

它有三个根: $r_1 = 0, r_2 = -1, r_3 = 3.$ 于是方程(9-3)的通解为

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 这里仅在 $x > 0$ 范围内求解. 如果要在 $x < 0$ 的范围内求解, 那么可作变换 $x = -\mathrm{e}^{t}$ 或 $t = \ln(-x)$, 所得结果与 $x > 0$ 的结果相类似.</span></small>

347

---

第七章 微分方程

$$
Y = C _ {1} + C _ {2} \mathrm{e} ^ {- t} + C _ {3} \mathrm{e} ^ {3 t} = C _ {1} + \frac {C _ {2}}{x} + C _ {3} x ^ {3}.
$$

根据上节第一目,特解的形式为

$$
y ^ {*} = b \mathrm{e} ^ {2 t} = b x ^ {2},
$$

代入原方程,求得  $b=-\frac{1}{2}$ , 即

$$
y ^ {*} = - \frac {x ^ {2}}{2}.
$$

于是,所给欧拉方程的通解为①

$$
y = C _ {1} + \frac {C _ {2}}{x} + C _ {3} x ^ {3} - \frac {1}{2} x ^ {2}.
$$

## \*习题7-9

求下列欧拉方程的通解:

1.  $x^{2}y''+xy'-y=0.$

2. $y'' - \frac{y'}{x} + \frac{y}{x^2} = \frac{2}{x}.$

3.  $x^{3}y'''+3x^{2}y''-2xy'+2y=0.$

4.  $x^{2}y''-2xy'+2y=\ln^{2}x-2\ln x.$

5.  $x^{2}y''+xy'-4y=x^{3}$

6. $x^{2}y^{\prime \prime} - xy^{\prime} + 4y = x\sin (\ln x)$

7.  $x^{2}y''-3xy'+4y=x+x^{2}\ln x.$

8. $x^{3}y^{\prime \prime \prime} + 2xy^{\prime} - 2y = x^{2}\ln x + 3x.$

## \* 第十节 常系数线性微分方程组解法举例

前面讨论的是由一个微分方程求解一个未知函数的情形,但在研究某些实际问题时,还会遇到由几个微分方程联立起来共同确定几个具有同一自变量的函数的情形.这些联立的微分方程称为微分方程组.

如果微分方程组中的每一个微分方程都是常系数线性微分方程,那么,这种微分方程组就叫做常系数线性微分方程组.

对于常系数线性微分方程组,我们可以用下述方法求它的解:

第一步 从方程组中消去一些未知函数及其各阶导数,得到只含有一个未知函数的高阶常系数线性微分方程.

第二步 解此高阶微分方程,求出满足该方程的未知函数.

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 这是在 $x > 0$ 范围内所求得的通解.容易验证,在 $x <   0$ 范围内，它也是所给方程的通解</span></small>

348

---

\* 第十节 常系数线性微分方程组解法举例

第三步 把已求得的函数代入原方程组,一般说来,不必经过积分就可求出其余的未知函数.

例1 解微分方程组

$$
\left\{ \begin{array}{l} \frac {\mathrm{d} y}{\mathrm{d} x} = 3 y - 2 z, \\ \frac {\mathrm{d} z}{\mathrm{d} x} = 2 y - z. \end{array} \right. \tag {10-2}
$$

解 这是含有两个未知函数 $y(x), z(x)$ 的由两个一阶常系数线性方程组成的方程组.

设法消去未知函数 $y$. 由(10-2)式得

$$
y = \frac {1}{2} \left(\frac {\mathrm{d} z}{\mathrm{d} x} + z\right). \tag {10-3}
$$

对上式两端求导,有

$$
\frac {\mathrm{d} y}{\mathrm{d} x} = \frac {1}{2} \left(\frac {\mathrm{d} ^ {2} z}{\mathrm{d} x ^ {2}} + \frac {\mathrm{d} z}{\mathrm{d} x}\right). \tag {10-4}
$$

把(10-3)、(10-4)两式代入(10-1)式并化简,得

$$
\frac {\mathrm{d} ^ {2} z}{\mathrm{d} x ^ {2}} - 2 \frac {\mathrm{d} z}{\mathrm{d} x} + z = 0.
$$

这是一个二阶常系数线性微分方程,它的通解是

$$
z = (C _ {1} + C _ {2} x) \mathrm{e} ^ {x}. \tag {10-5}
$$

再把(10-5)式代入(10-3)式,得

$$
y = \frac {1}{2} (2 C _ {1} + C _ {2} + 2 C _ {2} x) \mathrm{e} ^ {x}. \tag {10-6}
$$

将(10-5)、(10-6)联立起来,就得到所给方程组的通解.

如果我们要得到方程组满足初值条件

$$
y \mid_ {x = 0} = 1, \quad z \mid_ {x = 0} = 0
$$

的特解,只需将此条件代入(10-6)和(10-5)式,得

$$
\left\{ \begin{array}{l} 1 = \frac {1}{2} (2 C _ {1} + C _ {2}), \\ 0 = C _ {1}. \end{array} \right.
$$

由此求得

$$
C _ {1} = 0, \quad C _ {2} = 2.
$$

于是所给微分方程组满足上述初值条件的特解为

$$
\left\{ \begin{array}{l} y = (1 + 2 x) \mathrm{e} ^ {x}, \\ z = 2 x \mathrm{e} ^ {x}. \end{array} \right.
$$

349

---

第七章 微分方程

在讨论常系数线性微分方程(或方程组)时,常采用第七节中引入的记号D表示对自变量x求导的运算 $\frac{d}{dx}$ .

例 2 解微分方程组

$$
\left\{ \begin{array}{l} \frac {\mathrm{d} ^ {2} x}{\mathrm{d} t ^ {2}} + \frac {\mathrm{d} y}{\mathrm{d} t} - x = \mathrm{e} ^ {t}, \\ \frac {\mathrm{d} ^ {2} y}{\mathrm{d} t ^ {2}} + \frac {\mathrm{d} x}{\mathrm{d} t} + y = 0. \end{array} \right.
$$

解 用记号 D 表示 $\frac{\mathrm{d}}{\mathrm{d}t}$, 则方程组可记作

$$
\left\{ \begin{array}{l l} (\mathrm{D} ^ {2} - 1) x + \mathrm{D} y = \mathrm{e} ^ {t}, & (1 0 - 7) \\ \mathrm{D} x + (\mathrm{D} ^ {2} + 1) y = 0. & (1 0 - 8) \end{array} \right.
$$

我们可以类似于解代数方程组那样消去一个未知数,例如为消去 x, 可作如下运算:

$$
(1 0 - 7) - \mathrm{D} (1 0 - 8): - x - \mathrm{D} ^ {3} y = \mathrm{e} ^ {t}, \tag {10-9}
$$

$$
(1 0 - 8) + \mathrm{D} (1 0 - 9): (- \mathrm{D} ^ {4} + \mathrm{D} ^ {2} + 1) y = \mathrm{De} ^ {t},
$$

即

$$
(- \mathrm{D} ^ {4} + \mathrm{D} ^ {2} + 1) y = \mathrm{e} ^ {t}. \tag {10-10}
$$

(10-10)式为四阶非齐次线性方程,其特征方程为

$$
- r ^ {4} + r ^ {2} + 1 = 0,
$$

解得特征根为

$$
r _ {1, 2} = \pm \alpha = \pm \sqrt {\frac {1 + \sqrt {5}}{2}}, \quad r _ {3, 4} = \pm \beta \mathrm{i} = \pm \mathrm{i} \sqrt {\frac {\sqrt {5} - 1}{2}},
$$

容易求得一个特解 $y^{*} = \mathrm{e}^{t}$，于是得(10-10)的通解为

$$
y = C _ {1} \mathrm{e} ^ {- \alpha t} + C _ {2} \mathrm{e} ^ {\alpha t} + C _ {3} \cos \beta t + C _ {4} \sin \beta t + \mathrm{e} ^ {t}. \tag {10-11}
$$

再求 $x$. 由(10-9)式, 即有

$$
x = - \mathrm{D} ^ {3} y - \mathrm{e} ^ {t},
$$

以(10-11)式代入上式,即得

$$
x = \alpha^ {3} C _ {1} \mathrm{e} ^ {- \alpha t} - \alpha^ {3} C _ {2} \mathrm{e} ^ {\alpha t} - \beta^ {3} C _ {3} \sin \beta t + \beta^ {3} C _ {4} \cos \beta t - 2 \mathrm{e} ^ {t}. \tag {10-12}
$$

将(10-11)和(10-12)两个函数联立,就是所求方程组的通解.

这里要注意,在求得一个未知函数以后,再求另一个未知函数时,一般不再积分(积分就会出现新的任意常数,从(10-11)、(10-12)两式可知两式中的任意常数之间有着确定的关系).

350

---

\* 第十节 常系数线性微分方程组解法举例

我们也可用行列式解上述方程组.由(10-7)和(10-8),有

$$
\left| \begin{array}{c c} \mathrm{D} ^ {2} - 1 & \mathrm{D} \\ \mathrm{D} & \mathrm{D} ^ {2} + 1 \end{array} \right| y = \left| \begin{array}{c c} \mathrm{D} ^ {2} - 1 & \mathrm{e} ^ {t} \\ \mathrm{D} & 0 \end{array} \right|,
$$

即

$$
(\mathrm{D} ^ {4} - \mathrm{D} ^ {2} - 1) y = - \mathrm{e} ^ {t}.
$$

这与(10-10)式是一样的.但再求 $x$ 时，不宜再次应用行列式.如再应用行列式，得

$$
\left| \begin{array}{c c} \mathrm{D} ^ {2} - 1 & \mathrm{D} \\ \mathrm{D} & \mathrm{D} ^ {2} + 1 \end{array} \right| x = \left| \begin{array}{c c} \mathrm{e} ^ {t} & \mathrm{D} \\ 0 & \mathrm{D} ^ {2} + 1 \end{array} \right|,
$$

即

$$
(\mathrm{D} ^ {4} - \mathrm{D} ^ {2} - 1) x = 2 \mathrm{e} ^ {\iota},
$$

解得

$$
x = A _ {1} \mathrm{e} ^ {- \alpha t} + A _ {2} \mathrm{e} ^ {\alpha t} + A _ {3} \cos \beta t + A _ {4} \sin \beta t - 2 \mathrm{e} ^ {t},
$$

则必须说明 $A_{1}, A_{2}, A_{3}, A_{4}$ 与 $C_{1}, C_{2}, C_{3}, C_{4}$ 之间的关系.

注意这里的“系数行列式”

$$
\left| \begin{array}{c c} \mathrm{D} ^ {2} - 1 & \mathrm{D} \\ \mathrm{D} & \mathrm{D} ^ {2} + 1 \end{array} \right| = \mathrm{D} ^ {4} - \mathrm{D} ^ {2} - 1
$$

是 D 的四次多项式, 这就标志着微分方程组是四阶的, 它的通解中一定恰含四个任意常数.

## \*习题7-10

1. 求下列微分方程组的通解:

(1) $\left\{ \begin{array}{l} \frac{\mathrm{d}y}{\mathrm{d}x} = z, \\ \frac{\mathrm{d}z}{\mathrm{d}x} = y; \end{array} \right.$

(2) $\left\{ \begin{array}{l} \frac{\mathrm{d}^2 x}{\mathrm{d}t^2} = y, \\ \frac{\mathrm{d}^2 y}{\mathrm{d}t^2} = x; \end{array} \right.$

(3) $\left\{ \begin{array}{l} \frac{\mathrm{d}x}{\mathrm{d}t} + \frac{\mathrm{d}y}{\mathrm{d}t} = -x + y + 3, \\ \frac{\mathrm{d}x}{\mathrm{d}t} - \frac{\mathrm{d}y}{\mathrm{d}t} = x + y - 3; \end{array} \right.$

(4) $\left\{ \begin{array}{l} \frac{\mathrm{d}x}{\mathrm{d}t} + 5x + y = \mathrm{e}^t, \\ \frac{\mathrm{d}y}{\mathrm{d}t} - x - 3y = \mathrm{e}^{2t}; \end{array} \right.$

(5) $\left\{ \begin{array}{l} \frac{\mathrm{d}x}{\mathrm{d}t} + 2x + \frac{\mathrm{d}y}{\mathrm{d}t} + y = t, \\ 5x + \frac{\mathrm{d}y}{\mathrm{d}t} + 3y = t^2; \end{array} \right.$

(6) $\left\{ \begin{array}{l} \frac{\mathrm{d}x}{\mathrm{d}t} - 3x + 2\frac{\mathrm{d}y}{\mathrm{d}t} + 4y = 2\sin t, \\ 2\frac{\mathrm{d}x}{\mathrm{d}t} + 2x + \frac{\mathrm{d}y}{\mathrm{d}t} - y = \cos t. \end{array} \right.$

2. 求下列微分方程组满足所给初值条件的特解:

351

---

第七章 微分方程

(1) $\left\{ \begin{array}{l} \frac{\mathrm{d}x}{\mathrm{d}t} = y, x \mid_{t=0} = 0, \\ \frac{\mathrm{d}y}{\mathrm{d}t} = -x, y \mid_{t=0} = 1; \end{array} \right.$
(2) $\left\{ \begin{array}{l} \frac{\mathrm{d}^2x}{\mathrm{d}t^2} + 2\frac{\mathrm{d}y}{\mathrm{d}t} - x = 0, x \mid_{t=0} = 1, \\ \frac{\mathrm{d}x}{\mathrm{d}t} + y = 0, y \mid_{t=0} = 0; \end{array} \right.$
(3) $\left\{ \begin{array}{l}\frac{\mathrm{d}x}{\mathrm{d}t} + 3x - y = 0, x \mid_{t=0} = 1, \\ \frac{\mathrm{d}y}{\mathrm{d}t} - 8x + y = 0, y \mid_{t=0} = 4; \end{array} \right.$
(4) $\left\{ \begin{array}{l} 2 \frac{\mathrm{d}x}{\mathrm{d}t} - 4x + \frac{\mathrm{d}y}{\mathrm{d}t} - y = \mathrm{e}^t, x \mid_{t=0} = \frac{3}{2}, \\ \frac{\mathrm{d}x}{\mathrm{d}t} + 3x + y = 0, y \mid_{t=0} = 0; \end{array} \right.$
(5) $\left\{ \begin{array}{l} \frac{\mathrm{d}x}{\mathrm{d}t} + 2x - \frac{\mathrm{d}y}{\mathrm{d}t} = 10\cos t, x \mid_{t=0} = 2, \\ \frac{\mathrm{d}x}{\mathrm{d}t} + \frac{\mathrm{d}y}{\mathrm{d}t} + 2y = 4\mathrm{e}^{-2t}, y \mid_{t=0} = 0; \end{array} \right.$
(6) $\left\{ \begin{array}{l} \frac{\mathrm{d}x}{\mathrm{d}t} - x + \frac{\mathrm{d}y}{\mathrm{d}t} + 3y = \mathrm{e}^{-t} - 1, x \mid_{t=0} = \frac{48}{49}, \\ \frac{\mathrm{d}x}{\mathrm{d}t} + 2x + \frac{\mathrm{d}y}{\mathrm{d}t} + y = \mathrm{e}^{2t} + t, y \mid_{t=0} = \frac{95}{98}. \end{array} \right.$

## 总习题七

1. 填空:

(1)  $xy''' + 2x^{2}y'^{2} + x^{3}y = x^{4} + 1$  是 \_\_\_\_ 阶微分方程；
(2) 一阶线性微分方程  $y' + P(x)y = Q(x)$  的通解为 \_\_\_\_；
(3) 与积分方程 $y = \int_{x_0}^{x} f(x, y) \, \mathrm{d}x$ 等价的微分方程初值问题是 \_\_\_\_;
(4) 已知 $y = 1, y = x, y = {x}^{2}$ 是某二阶非齐次线性微分方程的三个解,则该方程的通解为\_\_\_\_.

2. 以下两题中给出了四个结论,从中选出一个正确的结论:

（1）设非齐次线性微分方程  $y' + P(x)y = Q(x)$  有两个不同的解  $y_{1}(x)$  与  $y_{2}(x)$ ，C 为任意常数，则该方程的通解是（）；

(A) $C[y_{1}(x) - y_{2}(x)]$

(B) $y_{1}(x) + C[y_{1}(x) - y_{2}(x)]$

352

---

总习题七

(C) $C[y_{1}(x) + y_{2}(x)]$

(D) $y_{1}(x) + C[y_{1}(x) + y_{2}(x)]$

(2) 具有特解  $y_{1}=e^{-x}, y_{2}=2xe^{-x}, y_{3}=3e^{x}$  的三阶常系数齐次线性微分方程是().

(A) $y'''-y''-y'+y=0$

(B) $y''' + y'' - y' - y = 0$

(C)  $y'''-6y''+11y'-6y=0$

(D) $y'''-2y''-y'+2y=0$

3. 求以下列各式所表示的函数为通解的微分方程:

(1) $(x+C)^{2}+y^{2}=1$ （其中C为任意常数）;
(2) $y=C_{1}e^{x}+C_{2}e^{2x}$ （其中 $C_{1},C_{2}$ 为任意常数）.

4. 求下列微分方程的通解:

(1) $xy'+y=2\sqrt{xy}$;

(2)  $xy'\ln x+y=ax(\ln x+1)$ ;

(3)  $\frac{dy}{dx}=\frac{y}{2(\ln y-x)};$

$^{*}$ (4)  $\frac{dy}{dx} + xy - x^{3}y^{3} = 0;$

(5) $y''+y'^{2}+1=0;$

(6) $yy'' - y'^2 - 1 = 0$;

(7) $y''+2y'+5y=\sin 2x;$

(8) $y''' + y'' - 2y' = x(e^x + 4)$;

$^{*}$ (9) $(y^{4}-3x^{2})\mathrm{d}y+xy\mathrm{d}x=0;$

(10) $y' + x = \sqrt{x^2 + y}$.

5. 求下列微分方程满足所给初值条件的特解:

$^{*}$ (1)  $y^{3}\mathrm{d}x+2(x^{2}-xy^{2})\mathrm{d}y=0,x=1$  时 y=1;

(2) $y''-ay'^{2}=0,x=0$ 时 $y=0,y'=-1;$
(3) $2y''-\sin 2y=0,x=0$ 时 $y=\frac{\pi}{2},y'=1;$
(4) $y''+2y'+y=\cos x,x=0$ 时 $y=0,y'=\frac{3}{2}$.

6. 已知某曲线经过点(1,1)，它的切线在纵轴上的截距等于切点的横坐标，求它的方程.

7. 已知某车间的容积为  $5400 \, m^{3}$ ，其中的空气含 0.12% 的  $CO_{2}$ （以容积计算）。现以含  $CO_{2}$  0.04% 的新鲜空气输入，问每分应输入多少，才能在 30 min 后使车间空气中  $CO_{2}$  的含量不超过 0.06%？（假定输入的新鲜空气与原有空气很快混合均匀后，以相同的流量排出。）

8. 设可导函数 $\varphi(x)$ 满足

$$
\varphi (x) \cos x + 2 \int_ {0} ^ {x} \varphi (t) \sin t \mathrm{d} t = x + 1,
$$

求  $\varphi(x)$ .

9. 设光滑曲线 $y = \varphi(x)$ 过原点，且当 $x > 0$ 时 $\varphi(x) > 0$. 对应于 $[0, x]$ 一段曲线的弧长为 $e^x - 1$，求 $\varphi(x)$.

10. 设 $y_{1}(x), y_{2}(x)$ 是二阶齐次线性方程 $y'' + p(x)y' + q(x)y = 0$ 的两个解，令

$$
W (x) = \left| \begin{array}{l l} y _ {1} (x) & y _ {2} (x) \\ y _ {1} ^ {\prime} (x) & y _ {2} ^ {\prime} (x) \end{array} \right| = y _ {1} (x) y _ {2} ^ {\prime} (x) - y _ {1} ^ {\prime} (x) y _ {2} (x),
$$

证明:(1)  $W(x)$  满足方程  $W' + p(x)W = 0;$

(2) $W(x)=W(x_{0})\mathrm{e}^{-\int_{x_{0}}^{x}p(t)\mathrm{d}t}.$

\* 11. 求下列欧拉方程的通解:

353

---

第七章 微分方程

(1)  $x^{2}y''+3xy'+y=0;$

(2) $x^{2}y^{\prime \prime} - 4xy^{\prime} + 6y = x.$

\* 12. 求下列常系数线性微分方程组的通解:

(1) $\left\{ \begin{array}{l} \frac{\mathrm{d}x}{\mathrm{d}t} + 2\frac{\mathrm{d}y}{\mathrm{d}t} + y = 0, \\ 3\frac{\mathrm{d}x}{\mathrm{d}t} + 2x + 4\frac{\mathrm{d}y}{\mathrm{d}t} + 3y = t; \end{array} \right.$

(2) $\left\{ \begin{array}{l} \frac{\mathrm{d}^2x}{\mathrm{d}t^2} + 2\frac{\mathrm{d}x}{\mathrm{d}t} + x + \frac{\mathrm{d}y}{\mathrm{d}t} + y = 0, \\ \frac{\mathrm{d}x}{\mathrm{d}t} + x + \frac{\mathrm{d}^2y}{\mathrm{d}t^2} + 2\frac{\mathrm{d}y}{\mathrm{d}t} + y = e^t. \end{array} \right.$

![](../../raw/pages_0353-0384/images/page_370_image_6.jpg)

第七章释疑解难

354

---

## 附录I

## 初等数学几个内容简介

## (一) 三角函数公式

1. 两角和差公式

$$
\sin (\alpha + \beta) = \sin \alpha \cos \beta + \cos \alpha \sin \beta
$$

$$
\sin (\alpha - \beta) = \sin \alpha \cos \beta - \cos \alpha \sin \beta
$$

$$
\cos (\alpha + \beta) = \cos \alpha \cos \beta - \sin \alpha \sin \beta
$$

$$
\cos (\alpha - \beta) = \cos \alpha \cos \beta + \sin \alpha \sin \beta
$$

$$
\tan (\alpha + \beta) = \frac {\tan \alpha + \tan \beta}{1 - \tan \alpha \tan \beta}
$$

$$
\tan (\alpha - \beta) = \frac {\tan \alpha - \tan \beta}{1 + \tan \alpha \tan \beta}
$$

2. 和差化积公式

$$
\sin \alpha + \sin \beta = 2 \sin \frac {\alpha + \beta}{2} \cos \frac {\alpha - \beta}{2}
$$

$$
\sin \alpha - \sin \beta = 2 \cos \frac {\alpha + \beta}{2} \sin \frac {\alpha - \beta}{2}
$$

$$
\cos \alpha + \cos \beta = 2 \cos \frac {\alpha + \beta}{2} \cos \frac {\alpha - \beta}{2}
$$

$$
\cos \alpha - \cos \beta = - 2 \sin \frac {\alpha + \beta}{2} \sin \frac {\alpha - \beta}{2}
$$

3. 积化和差公式

$$
\sin \alpha \cos \beta = \frac {1}{2} [ \sin (\alpha + \beta) + \sin (\alpha - \beta) ]
$$

$$
\cos \alpha \sin \beta = \frac {1}{2} [ \sin (\alpha + \beta) - \sin (\alpha - \beta) ]
$$

$$
\cos \alpha \cos \beta = \frac {1}{2} [ \cos (\alpha + \beta) + \cos (\alpha - \beta) ]
$$

355

---

附录 I 初等数学几个内容简介

$$
\sin \alpha \sin \beta = - \frac {1}{2} [ \cos (\alpha + \beta) - \cos (\alpha - \beta) ]
$$

4. 倍角公式

$$
\sin 2 \alpha = 2 \sin \alpha \cos \alpha = \frac {2 \tan \alpha}{1 + \tan^ {2} \alpha}
$$

$$
\cos 2 \alpha = \cos^ {2} \alpha - \sin^ {2} \alpha = 2 \cos^ {2} \alpha - 1 = 1 - 2 \sin^ {2} \alpha = \frac {1 - \tan^ {2} \alpha}{1 + \tan^ {2} \alpha}
$$

$$
\tan 2 \alpha = \frac {2 \tan \alpha}{1 - \tan^ {2} \alpha}
$$

5. 半角公式

$$
\sin \frac {\alpha}{2} = \pm \sqrt {\frac {1 - \cos \alpha}{2}}
$$

$$
\cos \frac {\alpha}{2} = \pm \sqrt {\frac {1 + \cos \alpha}{2}}
$$

$$
\tan \frac {\alpha}{2} = \frac {\sin \alpha}{1 + \cos \alpha} = \frac {1 - \cos \alpha}{\sin \alpha} = \pm \sqrt {\frac {1 - \cos \alpha}{1 + \cos \alpha}}
$$

$\left(正、负号由 \frac{\alpha}{2} 所在的象限决定.\right)$

## (二) 反三角函数

三角函数作为一种从它们各自的定义域到值域的映射,都不是单射. 然而,如果对其定义域作某种限制,也可以使每一个三角函数都成为单射,从而就存在反函数,这样得到的反函数就是通常所说的反三角函数,它们的定义以及性质如下:

正弦函数 $y = \sin x, x \in \left[-\frac{\pi}{2}, \frac{\pi}{2}\right]$ 的反函数称为反正弦函数，记作 $y = \arcsin x$，即 $x = \sin y$，这里 $x$ 是自变量，$y$ 是因变量.

因为 $\frac{1}{2} = \sin \frac{\pi}{6}$ ，所以 $\arcsin \frac{1}{2} = \frac{\pi}{6}$ ；类似地，有

$$
\frac {\sqrt {2}}{2} = \sin \frac {\pi}{4} \Rightarrow \arcsin \frac {\sqrt {2}}{2} = \frac {\pi}{4};
$$

$$
\frac {\sqrt {3}}{2} = \sin \frac {\pi}{3} \Rightarrow \arcsin \frac {\sqrt {3}}{2} = \frac {\pi}{3};
$$

$$
- 1 = \sin \left(- \frac {\pi}{2}\right) \Rightarrow \arcsin (- 1) = - \frac {\pi}{2},
$$

等等. 反正弦函数 $y = \arcsin x$ 的定义域为 $[-1, 1]$，值域为 $\left[-\frac{\pi}{2}, \frac{\pi}{2}\right]$，它在闭区间

356

---

附录 I 初等数学几个内容简介

[-1,1]上是有界的、单调增加的，且为奇函数，函数的图形如图1(a)所示.

余弦函数 $y = \cos x, x \in [0, \pi]$ 的反函数称为反余弦函数，记作 $y = \arccos x$，即 $x = \cos y$. 反余弦函数 $y = \arccos x$ 的定义域为 $[-1, 1]$，值域为 $[0, \pi]$，它在闭区间 $[-1, 1]$ 上是有界的、单调减少的，函数的图形如图1(b)所示.

正切函数 $y = \tan x, x \in \left(-\frac{\pi}{2}, \frac{\pi}{2}\right)$ 的反函数称为反正切函数，记作 $y = \arctan x$，即 $x = \tan y$. 反正切函数 $y = \arctan x$ 的定义域为 $(-\infty, +\infty)$，值域为 $\left(-\frac{\pi}{2}, \frac{\pi}{2}\right)$，它在 $(-\infty, +\infty)$ 内是有界的、单调增加的，且为奇函数，函数的图形如图1(c)所示.

余切函数 $y = \cot x = \frac{\cos x}{\sin x}, x \in (0, \pi)$ 的反函数称为反余切函数，记作 $y = \operatorname{arccot} x$，即 $x = \cot y$. 反余切函数 $y = \operatorname{arccot} x$ 的定义域为 $(-\infty, +\infty)$，值域为 $(0, \pi)$，它在 $(-\infty, +\infty)$ 内是有界的、单调减少的，函数的图形如图1(d)所示.

![](../../raw/pages_0353-0384/images/page_373_image_5.jpg)

图1

## (三) 极坐标

在平面上取定一点 $O$ ，从点 $O$ 引一条射线 $OA$ ，再选定一个长度单位和角的正方向

（通常取逆时针方向），这样，平面上任意一点 $M$ 的位置就可用两个数 $\rho$ 和 $\theta$ 来确定，确定的方法是（图2）:$\rho = |OM|$，因此 $\rho \geqslant 0; \theta = \angle AOM, 0 \leqslant \theta < 2\pi.$ 这样规定的数 $\rho$ 和 $\theta$ 叫做点 $M$ 的极坐标，且以有序实数对 $(\rho, \theta)$ 表示，$\rho$ 称为点 $M$ 的极径，$\theta$ 称为点 $M$ 的极角，$O$ 称为极点，$OA$ 称

![](../../raw/pages_0353-0384/images/page_373_image_10.jpg)

<details>
<summary>text_image</summary>

P
M
ρ
θ
O
A
</details>

图2

357

---

附录 I 初等数学几个内容简介

为极轴. 这样建立的坐标系称为极坐标系.

当点 M 在极点时, 极径  $\rho=0$ , 极角  $\theta$  可取任意值. 在极坐标系中, 除了极点 O 以外, 平面上任一点 M 与有序实数对  $(\rho,\theta)$  之间建立了一一对应关系. 但在实际应用中,

有时为了方便起见,在极坐标中,允许 $\rho$ 和 $\theta$ 可取一切实数.这时,设有两个任意实数 $\rho$ 和 $\theta$,先作射线OP,使 $\angle AOP=\theta$,如果 $\rho>0$,在OP上作一点M,使 $|OM|=\rho$;如果 $\rho<0$,在P向O的延长线上,作一点M,使 $|OM|=|\rho|$ (图3).这样,对于任意一对实数 $\rho$ 和 $\theta$,总可以在平面上确定唯一的一点M,( $\rho,\theta$ )仍称为点M的极坐标.由此可知,有序实数对 $(\rho,\theta)$ 与

![](../../raw/pages_0353-0384/images/page_374_image_4.jpg)

<details>
<summary>text_image</summary>

|ρ|
O
θ
P
A
M
</details>

图3

$(\rho,\theta+2k\pi)$  或  $(- \rho, \theta + (2k+1)\pi)$  表示同一个点，这里 k 取任意整数.

与直角坐标系一样,在极坐标系中,把曲线看作适合某种条件的点的集合,用曲线上的点的极坐标  $\rho,\theta$  的关系式  $\varphi(\rho,\theta)=0$  表示的方程,就是曲线的极坐标方程.

当极坐标系中的极点与直角坐标系中的原点重合, 极轴与 x 轴正半轴重合, 两种

坐标系的长度单位一致时(图4)，极坐标与直角坐标可以互换.

由直角坐标到极坐标的变换公式为

$$
x = \rho \cos \theta , \quad y = \rho \sin \theta .
$$

由极坐标到直角坐标的变换公式为

$$
\rho^ {2} = x ^ {2} + y ^ {2}, \quad \tan \theta = \frac {y}{x} \quad (x \neq 0).
$$

![](../../raw/pages_0353-0384/images/page_374_image_14.jpg)

<details>
<summary>text_image</summary>

y
y
P
ρ
θ
O
x
x
</details>

图4

下面给出常用曲线的极坐标方程:

1. 圆心在极点, 半径为 r 的圆的方程为  $\rho = r$ .
2. 圆心为 $(a,0)$ ，半径为 a 的圆的方程为  $\rho=2a\cos\theta$ .
3. 圆心为  $\left(a,\frac{\pi}{2}\right)$ ，半径为 a 的圆的方程为  $\rho=2a\sin\theta$ .
4. 过极点, 倾角为  $\alpha$  的直线方程为  $\theta = \alpha (\rho \in \mathbb{R})$ .
5. 过点 $(a,0)$ 且垂直于极轴的直线方程为 $\rho \cos \theta = a$.
6. 过点 $\left(a,\frac{\pi}{2}\right)$ 且平行于极轴的直线方程为 $\rho\sin\theta=a$ .

## (四) 参数方程

在平面直角坐标系中,如果曲线上任意一点的坐标 x,y 都是某个变量 t 的函数

358

---

附录1 初等数学几个内容简介

$\left\{\begin{aligned}x&=\varphi(t),\\ y&=\psi(t),\end{aligned}\right.$  并且对于 t 的每一个允许的取值，由方程组确定的点  $(x,y)$  都在这条曲线上，那么这个方程就叫做曲线的参数方程，变量 t 叫做参数.

下面给出常用曲线的参数方程:

1. 以 $(a, b)$ 为圆心，$r$ 为半径的圆的参数方程为

$$
\left\{ \begin{array}{l} x = a + r \cos \theta , \\ y = b + r \sin \theta , \end{array} \right.
$$

其中  $\theta$  为参数.

2. 椭圆 $\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1 (a > b > 0)$ 的参数方程为

$$
\left\{ \begin{array}{l} x = a \cos \theta , \\ y = b \sin \theta . \end{array} \right.
$$

3. 双曲线 $\frac{x^{2}}{a^{2}}-\frac{y^{2}}{b^{2}}=1(a>b>0)$ 的参数方程为

$$
\left\{ \begin{array}{l} x = a \sec \theta , \\ y = b \tan \theta . \end{array} \right.
$$

4. 抛物线 $y^{2}=2px$ 的参数方程为

$$
\left\{ \begin{array}{l} x = 2 p t ^ {2}, \\ y = 2 p t. \end{array} \right.
$$

## (五) 二阶和三阶行列式

给出二元线性方程组

$$
\left\{ \begin{array}{l} a _ {1 1} x _ {1} + a _ {1 2} x _ {2} = b _ {1}, \\ a _ {2 1} x _ {1} + a _ {2 2} x _ {2} = b _ {2}, \end{array} \right. \tag {1}
$$

求这方程组的解.

用大家熟知的消元法,分别消去方程组(1)中的 $x_{2}$ 及 $x_{1}$ ,得

$$
\left\{ \begin{array}{l} (a _ {1 1} a _ {2 2} - a _ {1 2} a _ {2 1}) x _ {1} = b _ {1} a _ {2 2} - a _ {1 2} b _ {2}, \\ (a _ {1 1} a _ {2 2} - a _ {1 2} a _ {2 1}) x _ {2} = a _ {1 1} b _ {2} - b _ {1} a _ {2 1}. \end{array} \right. \tag {2}
$$

下面引入二阶行列式,然后利用二阶行列式来进一步讨论上述问题.

设已知四个数排成正方形表

$$
\left( \begin{array}{c c} a _ {1 1} & a _ {1 2} \\ a _ {2 1} & a _ {2 2} \end{array} \right),
$$

则数 $a_{11}a_{22} - a_{12}a_{21}$ 称为对应于这个表的二阶行列式，用记号

359

---

附录 I 初等数学几个内容简介

$$
\left| \begin{array}{l l} a _ {1 1} & a _ {1 2} \\ a _ {2 1} & a _ {2 2} \end{array} \right| \tag {3}
$$

表示,因此

$$
\left| \begin{array}{c c} a _ {1 1} & a _ {1 2} \\ a _ {2 1} & a _ {2 2} \end{array} \right| = a _ {1 1} a _ {2 2} - a _ {1 2} a _ {2 1}.
$$

数 $a_{11}, a_{12}, a_{21}, a_{22}$ 叫做行列式(3)的元素，横排叫做行，竖排叫做列。元素 $a_{ij}$ 中的第一个指标 $i$ 和第二个指标 $j$ 依次表示该元素所在的行数和列数。例如，元素 $a_{21}$ 在行列式(3)中位于第二行和第一列。

现在,方程组(2)可利用行列式来表示.设

$$
D = \left| \begin{array}{l l} a _ {1 1} & a _ {1 2} \\ a _ {2 1} & a _ {2 2} \end{array} \right| = a _ {1 1} a _ {2 2} - a _ {1 2} a _ {2 1},
$$

$$
D _ {1} = \left| \begin{array}{l l} b _ {1} & a _ {1 2} \\ b _ {2} & a _ {2 2} \end{array} \right| = b _ {1} a _ {2 2} - a _ {1 2} b _ {2},
$$

$$
D _ {2} = \left| \begin{array}{c c} a _ {1 1} & b _ {1} \\ a _ {2 1} & b _ {2} \end{array} \right| = a _ {1 1} b _ {2} - b _ {1} a _ {2 1},
$$

则方程组(2)可写成

$$
\left\{ \begin{array}{l} D x _ {1} = D _ {1}, \\ D x _ {2} = D _ {2}. \end{array} \right. \tag {$2^{\prime$}}
$$

我们注意到, D 就是方程组(1)中  $x_{1}$  及  $x_{2}$  的系数构成的行列式, 因此称为系数行列式, 而  $D_{1}$  和  $D_{2}$  分别是用方程组(1)右端的常数项代替 D 的第一列和第二列而形成的.

若 $D \neq 0$ ，则方程组(2)的解为

$$
x _ {1} = \frac {D _ {1}}{D}, \quad x _ {2} = \frac {D _ {2}}{D}. \tag {4}
$$

把(4)中 $x_{1}$ 及 $x_{2}$ 的值代入方程组(1)，便可证实 $x_{1}$ 及 $x_{2}$ 的这对值也是方程组(1)的解.另一方面，(2)是由(1)导出的，因此(1)的解一定是(2)的解.现在(2)只有一组解(4)，所以(4)是方程组(1)的唯一解.由此得出结论:

在 $D \neq 0$ 的条件下, 方程组(1)有唯一的解

$$
x _ {1} = \frac {D _ {1}}{D}, \quad x _ {2} = \frac {D _ {2}}{D}.
$$

例1 解方程组

$$
\left\{ \begin{array}{l} 2 x + 3 y = 8, \\ x - 2 y = - 3. \end{array} \right.
$$

360

---

附录1 初等数学几个内容简介

解 $D = \begin{vmatrix} 2 & 3 \\ 1 & -2 \end{vmatrix} = 2 \times (-2) - 3 \times 1 = -7,$

$$
D _ {1} = \left| \begin{array}{c c} 8 & 3 \\ - 3 & - 2 \end{array} \right| = 8 \times (- 2) - 3 \times (- 3) = - 7,
$$

$$
D _ {2} = \left| \begin{array}{c c} 2 & 8 \\ 1 & - 3 \end{array} \right| = 2 \times (- 3) - 8 \times 1 = - 1 4.
$$

因 $D = -7 \neq 0$ ，故所给方程组有唯一解

$$
x = \frac {D _ {1}}{D} = \frac {- 7}{- 7} = 1, \quad y = \frac {D _ {2}}{D} = \frac {- 1 4}{- 7} = 2.
$$

下面介绍三阶行列式概念.

设已知9个数排成正方形表

$$
\left( \begin{array}{c c c} a _ {1 1} & a _ {1 2} & a _ {1 3} \\ a _ {2 1} & a _ {2 2} & a _ {2 3} \\ a _ {3 1} & a _ {3 2} & a _ {3 3} \end{array} \right),
$$

则数 $a_{11}a_{22}a_{33} + a_{12}a_{23}a_{31} + a_{13}a_{21}a_{32} - a_{13}a_{22}a_{31} - a_{12}a_{21}a_{33} - a_{11}a_{23}a_{32}$ 称为对应于这个表的三阶行列式，用记号

$$
\left| \begin{array}{c c c} a _ {1 1} & a _ {1 2} & a _ {1 3} \\ a _ {2 1} & a _ {2 2} & a _ {2 3} \\ a _ {3 1} & a _ {3 2} & a _ {3 3} \end{array} \right|
$$

表示,因此

$$
\begin{array}{l} \left| \begin{array}{c c c} a _ {1 1} & a _ {1 2} & a _ {1 3} \\ a _ {2 1} & a _ {2 2} & a _ {2 3} \\ a _ {3 1} & a _ {3 2} & a _ {3 3} \end{array} \right| \\ = a _ {1 1} a _ {2 2} a _ {3 3} + a _ {1 2} a _ {2 3} a _ {3 1} + a _ {1 3} a _ {2 1} a _ {3 2} - a _ {1 3} a _ {2 2} a _ {3 1} - a _ {1 2} a _ {2 1} a _ {3 3} - a _ {1 1} a _ {2 3} a _ {3 2}. \tag {5} \\ \end{array}
$$

关于三阶行列式的元素、行、列等概念,与二阶行列式的相应概念类似,不再重复.

(5)式右端相当复杂,我们可以借助图5得出它的计算法则(通常称为对角线法则):

行列式中从左上角到右下角的直线称为主对角线,从右上角到左下角的直线称为次对角线.主对角线上元素的乘积以及位于主对角线的平行线上的元素与对角上的元素的乘积,前面都取正号.次对角线上元素的乘积以及位于次对角线

![](../../raw/pages_0353-0384/images/page_377_image_16.jpg)

<details>
<summary>text_image</summary>

Diagram showing two configurations of graph structures with plus and minus signs, each containing a central node and connected edges.
</details>

图5

361

---

附录Ⅰ 初等数学几个内容简介

的平行线上的元素与对角上的元素的乘积,前面都取负号.

例 2  $\begin{vmatrix}2&1&2\\-4&3&1\\2&3&5\end{vmatrix}$

$$
\begin{array}{l} = 2 \times 3 \times 5 + 1 \times 1 \times 2 + 2 \times (- 4) \times 3 - 2 \times 3 \times 2 - 1 \times (- 4) \times 5 - 2 \times 1 \times 3 \\ = 3 0 + 2 - 2 4 - 1 2 + 2 0 - 6 = 1 0. \\ \end{array}
$$

利用交换律及结合律,可把(5)式改写如下:

$$
\left| \begin{array}{l l l} a _ {1 1} & a _ {1 2} & a _ {1 3} \\ a _ {2 1} & a _ {2 2} & a _ {2 3} \\ a _ {3 1} & a _ {3 2} & a _ {3 3} \end{array} \right| = a _ {1 1} (a _ {2 2} a _ {3 3} - a _ {2 3} a _ {3 2}) - a _ {1 2} (a _ {2 1} a _ {3 3} - a _ {2 3} a _ {3 1}) + a _ {1 3} (a _ {2 1} a _ {3 2} - a _ {2 2} a _ {3 1}).
$$

把上式右端三个括号中的式子表示为二阶行列式,则有

$$
\left| \begin{array}{l l l} a _ {1 1} & a _ {1 2} & a _ {1 3} \\ a _ {2 1} & a _ {2 2} & a _ {2 3} \\ a _ {3 1} & a _ {3 2} & a _ {3 3} \end{array} \right| = a _ {1 1} \left| \begin{array}{l l} a _ {2 2} & a _ {2 3} \\ a _ {3 2} & a _ {3 3} \end{array} \right| - a _ {1 2} \left| \begin{array}{l l} a _ {2 1} & a _ {2 3} \\ a _ {3 1} & a _ {3 3} \end{array} \right| + a _ {1 3} \left| \begin{array}{l l} a _ {2 1} & a _ {2 2} \\ a _ {3 1} & a _ {3 2} \end{array} \right|.
$$

上式称为三阶行列式按第一行的展开式.

例 3 将例 2 中的行列式按第一行展开并计算它的值.

解  $\begin{vmatrix}2&1&2\\ -4&3&1\\ 2&3&5\end{vmatrix}=2\begin{vmatrix}3&1\\ 3&5\end{vmatrix}-\begin{vmatrix}-4&1\\ 2&5\end{vmatrix}+2\begin{vmatrix}-4&3\\ 2&3\end{vmatrix}$

$$
= 2 \times 1 2 - (- 2 2) + 2 \times (- 1 8) = 2 4 + 2 2 - 3 6 = 1 0.
$$

## 习题

1. 利用二阶行列式解下列方程组:

(1) $\left\{\begin{aligned}5x-y=2,\\ 3x+2y=9;\end{aligned}\right.$

(2) $\left\{\begin{aligned}3x+4y=2,\\ 2x+3y=7.\end{aligned}\right.$

2. 利用对角线法则, 计算下列各行列式:

(1) $\begin{vmatrix}2&0&1\\1&-4&-1\\-1&8&3\end{vmatrix};$

(2) $\begin{vmatrix}4&-2&4\\10&2&12\\1&2&2\end{vmatrix};$

(3) $\begin{vmatrix}3&4&2\\ 7&5&1\\ 3&2&4\end{vmatrix};$

(4) $\begin{vmatrix}1&1&1\\ 1&1+a&1\\ 1&1&1+b\end{vmatrix}.$

362

---

附录 I 初等数学几个内容简介

3. 将下列行列式按第一行展开并计算它们的值:

(1) $\begin{vmatrix}1&2&3\\ 3&1&2\\ 2&3&1\end{vmatrix};$

(2) $\begin{vmatrix}-1&2&2\\2&-1&2\\2&2&-1\end{vmatrix}.$

4. 证明下列等式:

(1) $\begin{vmatrix}a_{11}&a_{12}&a_{13}\\a_{21}&a_{22}&a_{23}\\a_{31}&a_{32}&a_{33}\end{vmatrix}=-a_{21}\begin{vmatrix}a_{12}&a_{13\\a_{32}&a_{33}\end{vmatrix}+a_{22}\begin{vmatrix}a_{11}&a_{13\\a_{31}&a_{33}\end{vmatrix}-a_{23}\begin{vmatrix}a_{11}&a_{12\\a_{31}&a_{32}\end{vmatrix};$

(2) $\begin{vmatrix}a_{11}&a_{12}&a_{13}\\a_{21}&a_{22}&a_{23}\\a_{31}&a_{32}&a_{33}\end{vmatrix}=a_{31}\begin{vmatrix}a_{12}&a_{13}\\a_{22}&a_{23}\end{vmatrix}-a_{32}\begin{vmatrix}a_{11}&a_{13}\\a_{21}&a_{23}\end{vmatrix}+a_{33}\begin{vmatrix}a_{11}&a_{12}\\a_{21}&a_{22}\end{vmatrix}.$

注:上面这两个等式分别称为三阶行列式按第二行和按第三行的展开式.

## 答案

1. (1) x=1, y=3; (2) x=-22, y=17.
2. (1) -4; (2) 8; (3) -48; (4) ab.
3. (1) 18; (2) 27.

4. 略.

363

---

## 附录Ⅱ

## 基本初等函数的图形

幂函数

![](../../raw/pages_0353-0384/images/page_380_image_3.jpg)

$y = x^{\mu}$

指数函数

![](../../raw/pages_0353-0384/images/page_380_chart_6.jpg)

<details>
<summary>contour</summary>

| Region | Description |
| --- | --- |
| Left Curve | 0 < a < 1 |
| Right Curve | a > 1 |
</details>

$y = a^{x}$

对数函数

![](../../raw/pages_0353-0384/images/page_380_chart_9.jpg)

<details>
<summary>line</summary>

| X | Y (Curve 1) | Y (Curve 2) |
| --- | --- | --- |
| 0 | High | Low |
| 1 | 0 | 0 |
| >1 | Increasing | Decreasing |
</details>

$y = \log_a x$

三角函数

![](../../raw/pages_0353-0384/images/page_380_chart_12.jpg)

<details>
<summary>contour</summary>

| X | Y |
| --- | --- |
| \(-2\pi\) | ~-0.5 |
| \(-3\pi/2\) | 1 |
| \(-\pi\) | 0 |
| \(-\pi/2\) | ~-0.8 |
| O | 0 |
| \(\pi/2\) | 1 |
| \(\pi\) | 0 |
| \(3\pi/2\) | ~-0.8 |
| \(2\pi\) | ~0.5 |
</details>

$y = \sin x$

364

---

附录Ⅱ 基本初等函数的图形

![](../../raw/pages_0353-0384/images/page_381_chart_1.jpg)

<details>
<summary>contour</summary>

| X | Y |
| --- | --- |
| \(-3\pi/2\) | 0 |
| \(-\pi\) | ~-0.8 |
| \(-\pi/2\) | 0 |
| O | 1 |
| \(\pi/2\) | 0 |
| \(3\pi/2\) | ~-0.8 |
| \(2\pi\) | 0 |
| \(5\pi/2\) | ~-0.8 |
</details>

$y = \cos x$

![](../../raw/pages_0353-0384/images/page_381_chart_3.jpg)

<details>
<summary>contour</summary>

| X | Y |
| --- | --- |
| \(-3\pi/2\) | 0 |
| \(-\pi/2\) | 0 |
| O | 0 |
| \(\pi/2\) | 0 |
| \(3\pi/2\) | 0 |
| \(5\pi/2\) | 0 |
</details>

$y = \tan x$

![](../../raw/pages_0353-0384/images/page_381_chart_5.jpg)

<details>
<summary>contour</summary>

| X | Y |
| --- | --- |
| \(-2\pi\) | >0 |
| \(-3\pi/2\) | 0 |
| \(-\pi\) | >0 |
| \(-\pi/2\) | 0 |
| O | >0 |
| \(\pi/2\) | 0 |
| \(\pi\) | >0 |
| \(3\pi/2\) | 0 |
| \(2\pi\) | >0 |
</details>

$y = \cot x$

![](../../raw/pages_0353-0384/images/page_381_chart_7.jpg)

<details>
<summary>contour</summary>

| X-axis | Y-axis |
| --- | --- |
| \(-3\pi/2\) | 0 |
| \(-\pi\) | 0 |
| \(-\pi/2\) | 0 |
| O | 0 |
| \(\pi/2\) | 0 |
| \(\pi\) | 0 |
| \(3\pi/2\) | 0 |
| \(-3\pi/2\) | 1 |
| \(-\pi\) | 1 |
| \(-\pi/2\) | 1 |
| \(\pi/2\) | 1 |
| \(\pi\) | 1 |
| \(3\pi/2\) | 1 |
</details>

$y = \sec x$

![](../../raw/pages_0353-0384/images/page_381_chart_9.jpg)

<details>
<summary>contour</summary>

| x | y |
| --- | --- |
| \(-\pi\) | 1 |
| \(-\pi/2\) | 1 |
| \(\pi/2\) | 1 |
| \(\pi\) | 1 |
| \(3\pi/2\) | 1 |
| \(2\pi\) | 1 |
</details>

$y = \csc x$

365

---

附录Ⅱ 基本初等函数的图形

反三角函数

![](../../raw/pages_0353-0384/images/page_382_chart_2.jpg)

<details>
<summary>contour</summary>

| X | Y |
| --- | --- |
| -1 | ~-0.5 |
| 0 | 0 |
| 1 | ~0.5 |
</details>

$y = \arcsin x$

![](../../raw/pages_0353-0384/images/page_382_chart_4.jpg)

<details>
<summary>contour</summary>

| X | Y |
| --- | --- |
| -1 | ~\(\pi\) |
| 0 | \(\pi/2\) |
| 1 | 0 |
</details>

$y = \arccos x$

![](../../raw/pages_0353-0384/images/page_382_chart_6.jpg)

<details>
<summary>contour</summary>

| X | Y |
| --- | --- |
| 0 | 0 |
| \(-\pi/2\) | \(-\pi/2\) |
| \(\pi/2\) | \(\pi/2\) |
</details>

$y = \arctan x$

![](../../raw/pages_0353-0384/images/page_382_chart_8.jpg)

<details>
<summary>line</summary>

| X | Y |
| --- | --- |
| 0 | \(\pi\) |
| ~0.5 | \(\pi/2\) |
</details>

$y = \operatorname{arccot} x$

366

---

# 附录Ⅲ

# 几种常用的曲线

(1) 三次抛物线

![](../../raw/pages_0353-0384/images/page_383_image_3.jpg)

<details>
<summary>text_image</summary>

y
O
x
</details>

$$
y = a x ^ {3}
$$

(2) 半立方抛物线

![](../../raw/pages_0353-0384/images/page_383_image_6.jpg)

<details>
<summary>text_image</summary>

y
O
x
</details>

$$
y ^ {2} = a x ^ {3}
$$

(3) 概率曲线

![](../../raw/pages_0353-0384/images/page_383_image_9.jpg)

<details>
<summary>text_image</summary>

y
O
x
</details>

$$
y = \mathrm{e} ^ {- x ^ {2}}
$$

(4) 箕舌线

![](../../raw/pages_0353-0384/images/page_383_image_12.jpg)

<details>
<summary>text_image</summary>

y
a
a
O
x
</details>

$$
y = \frac {8 a ^ {3}}{x ^ {2} + 4 a ^ {2}}
$$

367

---

附录Ⅲ 几种常用的曲线

(5) 蔓叶线

![](../../raw/pages_0385-0416/images/page_384_image_2.jpg)

<details>
<summary>text_image</summary>

y
a, a
O
x
</details>

$$
y ^ {2} (2 a - x) = x ^ {3}
$$

(6) 笛卡儿叶形线

![](../../raw/pages_0385-0416/images/page_384_image_5.jpg)

<details>
<summary>text_image</summary>

y
a O x
a
</details>

$$
x ^ {3} + y ^ {3} - 3 a x y = 0
$$

$$
x = \frac {3 a t}{1 + t ^ {3}}, y = \frac {3 a t ^ {2}}{1 + t ^ {3}}
$$

(7) 星形线(内摆线的一种)

![](../../raw/pages_0385-0416/images/page_384_image_9.jpg)

<details>
<summary>text_image</summary>

y
a
a
O
a
x
</details>

$$
x ^ {\frac {2}{3}} + y ^ {\frac {2}{3}} = a ^ {\frac {2}{3}}
$$

$$
\left\{ \begin{array}{l} x = a \cos^ {3} \theta \\ y = a \sin^ {3} \theta \end{array} \right.
$$

(8) 摆线

![](../../raw/pages_0385-0416/images/page_384_image_13.jpg)

<details>
<summary>text_image</summary>

y
a
θ
a
O
x
a
a
</details>

$$
\left\{ \begin{array}{l} x = a (\theta - \sin \theta) \\ y = a (1 - \cos \theta) \end{array} \right.
$$

(9) 心形线(外摆线的一种)

![](../../raw/pages_0385-0416/images/page_384_image_16.jpg)

<details>
<summary>text_image</summary>

a
a
O
x
y
</details>

$$
x ^ {2} + y ^ {2} + a x = a \sqrt {x ^ {2} + y ^ {2}}
$$

$$
\rho = a (1 - \cos \theta)
$$

(10) 阿基米德螺线

![](../../raw/pages_0385-0416/images/page_384_image_20.jpg)

<details>
<summary>text_image</summary>

Hand-drawn mathematical diagram showing a solid curve and dashed spiral path in a Cartesian coordinate system with labeled axes A and O.
</details>

$$
\rho = a \theta
$$

368

---

附录Ⅲ 几种常用的曲线

(11) 对数螺线

![](../../raw/pages_0385-0416/images/page_385_image_2.jpg)

<details>
<summary>text_image</summary>

ρ=e^{αθ}
A
</details>

(12) 双曲螺线

![](../../raw/pages_0385-0416/images/page_385_image_4.jpg)

<details>
<summary>text_image</summary>

a
O
ρθ = a
A
</details>

(13) 伯努利双纽线

![](../../raw/pages_0385-0416/images/page_385_image_6.jpg)

<details>
<summary>text_image</summary>

(x²+y²)² = 2a²xy
ρ² = a² sin 2θ
</details>

(14) 伯努利双纽线

![](../../raw/pages_0385-0416/images/page_385_image_8.jpg)

<details>
<summary>text_image</summary>

(x²+y²)² = a²(x²-y²)
ρ² = a²cos 2θ
</details>

(15) 三叶玫瑰线

![](../../raw/pages_0385-0416/images/page_385_image_10.jpg)

<details>
<summary>text_image</summary>

3
a
O
1
A
a
a
2
ρ = a cos 3θ
</details>

(16) 三叶玫瑰线

![](../../raw/pages_0385-0416/images/page_385_image_12.jpg)

<details>
<summary>text_image</summary>

3
a
1
O
A
a
2
ρ=asin 3θ
</details>

369

---

附录Ⅲ 几种常用的曲线

(17) 四叶玫瑰线

![](../../raw/pages_0385-0416/images/page_386_image_2.jpg)

<details>
<summary>text_image</summary>

4
a
1
a
O
a
3
a
2
A
</details>

$\rho = a \sin 2 \theta$

(18) 四叶玫瑰线

![](../../raw/pages_0385-0416/images/page_386_image_5.jpg)

<details>
<summary>text_image</summary>

4
a
3
O
a
a
1
A
2
</details>

$\rho = a\cos 2\theta$

370

---

# 附录IV

# 积分表

## (一) 含有 $ax + b$ 的积分

1. $\int \frac{\mathrm{d}x}{ax + b} = \frac{1}{a}\ln |ax + b| + C.$
2. $\int (ax + b)^{\mu}\mathrm{d}x = \frac{1}{a(\mu + 1)} (ax + b)^{\mu +1} + C (\mu \neq -1).$
3. $\int \frac{x}{ax + b}\mathrm{d}x = \frac{1}{a^2} (ax + b - b\ln |ax + b|) + C.$
4. $\int \frac{x^2}{ax + b}\mathrm{d}x = \frac{1}{a^3}\left[\frac{1}{2} (ax + b)^2 -2b(ax + b) + b^2\ln |ax + b|\right] + C.$
5. $\int \frac{\mathrm{d}x}{x(ax + b)} = -\frac{1}{b}\ln \left|\frac{ax + b}{x}\right| + C.$
6. $\int \frac{\mathrm{d}x}{x^2(ax + b)} = -\frac{1}{bx} +\frac{a}{b^2}\ln \left|\frac{ax + b}{x}\right| + C.$
7. $\int \frac{x}{(ax + b)^2}\mathrm{d}x = \frac{1}{a^2}\left(\ln |ax + b| + \frac{b}{ax + b}\right) + C.$
8. $\int \frac{x^2}{(ax + b)^2}\mathrm{d}x = \frac{1}{a^3}\left(ax + b - 2b\ln |ax + b| - \frac{b^2}{ax + b}\right) + C.$
9. $\int \frac{\mathrm{d}x}{x(ax + b)^2} = \frac{1}{b(ax + b)} -\frac{1}{b^2}\ln \left|\frac{ax + b}{x}\right| + C.$

## (二) 含有 $\sqrt{ax + b}$ 的积分

10. $\int \sqrt{ax + b} \, \mathrm{d}x = \frac{2}{3a} \sqrt{(ax + b)^3} + C.$

371

---

附录IV 积分表

11. $\int x\sqrt{ax + b}\mathrm{d}x = \frac{2}{15a^2}(3ax - 2b)\sqrt{(ax + b)^3} +C.$
12. $\int x^{2}\sqrt{ax + b}\mathrm{d}x = \frac{2}{105a^{3}} (15a^{2}x^{2} - 12abx + 8b^{2})\sqrt{(ax + b)^{3}} +C.$
13. $\int \frac{x}{\sqrt{ax + b}}\mathrm{d}x = \frac{2}{3a^2} (ax - 2b)\sqrt{ax + b} +C.$
14. $\int \frac{x^2}{\sqrt{ax + b}}\mathrm{d}x = \frac{2}{15a^3}(3a^2 x^2 -4abx + 8b^2)\sqrt{ax + b} +C.$

15. $\int \frac{\mathrm{d}x}{x\sqrt{ax + b}} = \left\{ \begin{array}{l}\frac{1}{\sqrt{b}}\ln \left|\frac{\sqrt{ax + b} - \sqrt{b}}{\sqrt{ax + b} + \sqrt{b}}\right| + C (b > 0),\\ \frac{2}{\sqrt{-b}}\arctan \sqrt{\frac{ax + b}{-b}} +C (b <   0). \end{array} \right.$

16. $\int \frac{\mathrm{d}x}{x^2\sqrt{ax + b}} = -\frac{\sqrt{ax + b}}{bx} -\frac{a}{2b}\int \frac{\mathrm{d}x}{x\sqrt{ax + b}}.$

17. $\int \frac{\sqrt{ax + b}}{x}\mathrm{d}x = 2\sqrt{ax + b} +b\int \frac{\mathrm{d}x}{x\sqrt{ax + b}}.$

18. $\int \frac{\sqrt{ax + b}}{x^2}\mathrm{d}x = -\frac{\sqrt{ax + b}}{x} +\frac{a}{2}\int \frac{\mathrm{d}x}{x\sqrt{ax + b}}.$

## (三) 含有 $x^{2} \pm a^{2}$ 的积分

19. $\int \frac{\mathrm{d}x}{x^2 + a^2} = \frac{1}{a}\arctan \frac{x}{a} + C.$

20. $\int \frac{\mathrm{d}x}{(x^2 + a^2)^n} = \frac{x}{2(n - 1)a^2(x^2 + a^2)^{n - 1}} +\frac{2n - 3}{2(n - 1)a^2}\int \frac{\mathrm{d}x}{(x^2 + a^2)^{n - 1}}.$

21. $\int \frac{\mathrm{d}x}{x^2 - a^2} = \frac{1}{2a}\ln \left|\frac{x - a}{x + a}\right| + C.$

## (四) 含有 $ax^{2} + b (a > 0)$ 的积分

22. $\int \frac{\mathrm{d}x}{ax^2 + b} = \left\{ \begin{array}{l}\frac{1}{\sqrt{ab}}\arctan \sqrt{\frac{a}{b}} x + C (b > 0),\\ \frac{1}{2\sqrt{-ab}}\ln \left|\frac{\sqrt{a}x - \sqrt{-b}}{\sqrt{a}x + \sqrt{-b}}\right| + C (b <   0). \end{array} \right.$

23. $\int \frac{x}{ax^2 + b}\mathrm{d}x = \frac{1}{2a}\ln |ax^2 +b| + C.$

372

---

附录IV 积分表

24. $\int \frac{x^2}{ax^2 + b}\mathrm{d}x = \frac{x}{a} -\frac{b}{a}\int \frac{\mathrm{d}x}{ax^2 + b}.$
25. $\int \frac{\mathrm{d}x}{x(ax^2 + b)} = \frac{1}{2b}\ln \frac{x^2}{|ax^2 + b|} + C.$
26. $\int \frac{\mathrm{d}x}{x^2(ax^2 + b)} = -\frac{1}{bx} -\frac{a}{b}\int \frac{\mathrm{d}x}{ax^2 + b}.$
27. $\int \frac{\mathrm{d}x}{x^3(ax^2 + b)} = \frac{a}{2b^2}\ln \frac{|ax^2 + b|}{x^2} -\frac{1}{2bx^2} +C.$
28. $\int \frac{\mathrm{d}x}{(ax^2 + b)^2} = \frac{x}{2b(ax^2 + b)} +\frac{1}{2b}\int \frac{\mathrm{d}x}{ax^2 + b}.$

(五) 含有  $ax^{2}+bx+c$  (a>0) 的积分

29. $\int \frac{\mathrm{d}x}{ax^2 + bx + c} = \left\{ \begin{array}{l}\frac{2}{\sqrt{4ac - b^2}}\arctan \frac{2ax + b}{\sqrt{4ac - b^2}} +C (b^2 < 4ac),\\ \frac{1}{\sqrt{b^2 - 4ac}}\ln \left|\frac{2ax + b - \sqrt{b^2 - 4ac}}{2ax + b + \sqrt{b^2 - 4ac}}\right| + C (b^2 >4ac). \end{array} \right.$
30. $\int \frac{x}{ax^2 + bx + c}\mathrm{d}x = \frac{1}{2a}\ln |ax^2 +bx + c| - \frac{b}{2a}\int \frac{\mathrm{d}x}{ax^2 + bx + c}.$
(六) 含有  $\sqrt{x^{2}+a^{2}}$  (a>0) 的积分
31. $\int \frac{\mathrm{d}x}{\sqrt{x^2 + a^2}} = \operatorname{arsh}\frac{x}{a} + C_1 = \ln (x + \sqrt{x^2 + a^2}) + C.$
32. $\int \frac{\mathrm{d}x}{\sqrt{(x^2 + a^2)^3}} = \frac{x}{a^2\sqrt{x^2 + a^2}} + C.$
33. $\int \frac{x}{\sqrt{x^2 + a^2}}\mathrm{d}x = \sqrt{x^2 + a^2} +C.$
34. $\int \frac{x}{\sqrt{(x^2 + a^2)^3}}\mathrm{d}x = -\frac{1}{\sqrt{x^2 + a^2}} +C.$
35. $\int \frac{x^2}{\sqrt{x^2 + a^2}}\mathrm{d}x = \frac{x}{2}\sqrt{x^2 + a^2} -\frac{a^2}{2}\ln (x + \sqrt{x^2 + a^2}) + C.$
36. $\int \frac{x^2}{\sqrt{(x^2 + a^2)^3}}\mathrm{d}x = -\frac{x}{\sqrt{x^2 + a^2}} +\ln (x + \sqrt{x^2 + a^2}) + C.$
37. $\int \frac{\mathrm{d}x}{x\sqrt{x^2 + a^2}} = \frac{1}{a}\ln \frac{\sqrt{x^2 + a^2} - a}{|x|} + C.$

373

---

附录IV 积分表

38. $\int \frac{\mathrm{d}x}{x^2\sqrt{x^2 + a^2}} = -\frac{\sqrt{x^2 + a^2}}{a^2x} + C.$
39. $\int \sqrt{x^2 + a^2}\mathrm{d}x = \frac{x}{2}\sqrt{x^2 + a^2} +\frac{a^2}{2}\ln (x + \sqrt{x^2 + a^2}) + C.$
40. $\int \sqrt{(x^2 + a^2)^3} \, \mathrm{d}x = \frac{x}{8} (2x^2 + 5a^2) \sqrt{x^2 + a^2} + \frac{3}{8} a^4 \ln (x + \sqrt{x^2 + a^2}) + C.$
41. $\int x\sqrt{x^2 + a^2}\mathrm{d}x = \frac{1}{3}\sqrt{(x^2 + a^2)^3} +C.$
42. $\int x^{2}\sqrt{x^{2} + a^{2}}\mathrm{d}x = \frac{x}{8}\left(2x^{2} + a^{2}\right)\sqrt{x^{2} + a^{2}} -\frac{a^{4}}{8}\ln (x + \sqrt{x^{2} + a^{2}}) + C.$
43. $\int \frac{\sqrt{x^2 + a^2}}{x}\mathrm{d}x = \sqrt{x^2 + a^2} +a\ln \frac{\sqrt{x^2 + a^2} - a}{|x|} +C.$
44. $\int \frac{\sqrt{x^2 + a^2}}{x^2}\mathrm{d}x = -\frac{\sqrt{x^2 + a^2}}{x} +\ln (x + \sqrt{x^2 + a^2}) + C.$

(七) 含有 $\sqrt{x^2 - a^2} (a > 0)$ 的积分

45. $\int \frac{\mathrm{d}x}{\sqrt{x^2 - a^2}} = \frac{x}{|x|}$ arch $\frac{|x|}{a} + C_1 = \ln |x + \sqrt{x^2 - a^2}| + C.$
46. $\int \frac{\mathrm{d}x}{\sqrt{(x^2 - a^2)^3}} = -\frac{x}{a^2\sqrt{x^2 - a^2}} + C.$
47. $\int \frac{x}{\sqrt{x^2 - a^2}}\mathrm{d}x = \sqrt{x^2 - a^2} +C.$
48. $\int \frac{x}{\sqrt{(x^2 - a^2)^3}}\mathrm{d}x = -\frac{1}{\sqrt{x^2 - a^2}} +C.$
49. $\int \frac{x^2}{\sqrt{x^2 - a^2}}\mathrm{d}x = \frac{x}{2}\sqrt{x^2 - a^2} +\frac{a^2}{2}\ln |x + \sqrt{x^2 - a^2}| + C.$
50. $\int \frac{x^2}{\sqrt{(x^2 - a^2)^3}}\mathrm{d}x = -\frac{x}{\sqrt{x^2 - a^2}} +\ln |x + \sqrt{x^2 - a^2}| + C.$
51. $\int \frac{\mathrm{d}x}{x\sqrt{x^2 - a^2}} = \frac{1}{a}\arccos \frac{a}{|x|} + C.$
52. $\int \frac{\mathrm{d}x}{x^2\sqrt{x^2 - a^2}} = \frac{\sqrt{x^2 - a^2}}{a^2x} + C.$
53. $\int \sqrt{x^2 - a^2} \, \mathrm{d}x = \frac{x}{2} \sqrt{x^2 - a^2} - \frac{a^2}{2} \ln |x + \sqrt{x^2 - a^2}| + C.$

374

---

附录IV 积分表

54. $\int \sqrt{(x^2 - a^2)^3} \, \mathrm{d}x = \frac{x}{8} (2x^2 - 5a^2) \sqrt{x^2 - a^2} + \frac{3}{8} a^4 \ln |x + \sqrt{x^2 - a^2}| + C.$
55. $\int x\sqrt{x^2 - a^2}\mathrm{d}x = \frac{1}{3}\sqrt{(x^2 - a^2)^3} +C.$
56. $\int x^{2}\sqrt{x^{2} - a^{2}}\mathrm{d}x = \frac{x}{8} (2x^{2} - a^{2})\sqrt{x^{2} - a^{2}} -\frac{a^{4}}{8}\ln |x + \sqrt{x^{2} - a^{2}}| + C.$
57. $\int \frac{\sqrt{x^2 - a^2}}{x}\mathrm{d}x = \sqrt{x^2 - a^2} -a\arccos \frac{a}{|x|} +C.$
58. $\int \frac{\sqrt{x^2 - a^2}}{x^2}\mathrm{d}x = -\frac{\sqrt{x^2 - a^2}}{x} +\ln |x + \sqrt{x^2 - a^2}| + C.$

(八) 含有  $\sqrt{a^{2}-x^{2}}\quad(a>0)$  的积分

59. $\int \frac{\mathrm{d}x}{\sqrt{a^2 - x^2}} = \arcsin \frac{x}{a} + C.$

60. $\int \frac{\mathrm{d}x}{\sqrt{(a^2 - x^2)^3}} = \frac{x}{a^2\sqrt{a^2 - x^2}} + C.$

61. $\int \frac{x}{\sqrt{a^2 - x^2}}\mathrm{d}x = -\sqrt{a^2 - x^2} +C.$

62. $\int \frac{x}{\sqrt{(a^2 - x^2)^3}}\mathrm{d}x = \frac{1}{\sqrt{a^2 - x^2}} +C.$

63. $\int \frac{x^2}{\sqrt{a^2 - x^2}}\mathrm{d}x = -\frac{x}{2}\sqrt{a^2 - x^2} +\frac{a^2}{2}\arcsin \frac{x}{a} +C.$

64. $\int \frac{x^2}{\sqrt{(a^2 - x^2)^3}}\mathrm{d}x = \frac{x}{\sqrt{a^2 - x^2}} -\arcsin \frac{x}{a} +C.$

65. $\int \frac{\mathrm{d}x}{x\sqrt{a^2 - x^2}} = \frac{1}{a}\ln \frac{a - \sqrt{a^2 - x^2}}{|x|} + C.$

66. $\int \frac{\mathrm{d}x}{x^2\sqrt{a^2 - x^2}} = -\frac{\sqrt{a^2 - x^2}}{a^2x} +C.$

67. $\int \sqrt{a^2 - x^2} \, \mathrm{d}x = \frac{x}{2} \sqrt{a^2 - x^2} + \frac{a^2}{2} \arcsin \frac{x}{a} + C.$

68. $\int \sqrt{(a^2 - x^2)^3} \, \mathrm{d}x = \frac{x}{8} (5a^2 - 2x^2) \sqrt{a^2 - x^2} + \frac{3}{8} a^4 \arcsin \frac{x}{a} + C.$

69. $\int x\sqrt{a^2 - x^2}\mathrm{d}x = -\frac{1}{3}\sqrt{(a^2 - x^2)^3} +C.$

375

---

附录IV 积分表

70. $\int x^{2}\sqrt{a^{2} - x^{2}}\mathrm{d}x = \frac{x}{8}(2x^{2} - a^{2})\sqrt{a^{2} - x^{2}} +\frac{a^{4}}{8}\arcsin \frac{x}{a} +C.$
71. $\int \frac{\sqrt{a^2 - x^2}}{x}\mathrm{d}x = \sqrt{a^2 - x^2} +a\ln \frac{a - \sqrt{a^2 - x^2}}{|x|} +C.$
72. $\int \frac{\sqrt{a^2 - x^2}}{x^2}\mathrm{d}x = -\frac{\sqrt{a^2 - x^2}}{x} -\arcsin \frac{x}{a} +C.$

(九) 含有  $\sqrt{\pm ax^{2}+bx+c}$  (a>0) 的积分

73. $\int \frac{\mathrm{d}x}{\sqrt{ax^2 + bx + c}} = \frac{1}{\sqrt{a}}\ln \left|2ax + b + 2\sqrt{a}\sqrt{ax^2 + bx + c}\right| + C.$
74. $\int \sqrt{ax^2 + bx + c} \, \mathrm{d}x = \frac{2ax + b}{4a} \sqrt{ax^2 + bx + c} + \frac{4ac - b^2}{8\sqrt{a^3}} \ln \left| 2ax + b + 2\sqrt{a} \sqrt{ax^2 + bx + c} \right| + C.$
75. $\int \frac{x}{\sqrt{ax^2 + bx + c}}\mathrm{d}x = \frac{1}{a}\sqrt{ax^2 + bx + c} -\frac{b}{2\sqrt{a^3}}\ln \left|2ax + b + 2\sqrt{a}\sqrt{ax^2 + bx + c}\right| + C.$
76. $\int \frac{\mathrm{d}x}{\sqrt{c + bx - ax^2}} = \frac{1}{\sqrt{a}}\arcsin \frac{2ax - b}{\sqrt{b^2 + 4ac}} + C.$
77. $\int \sqrt{c + bx - ax^2} \, \mathrm{d}x = \frac{2ax - b}{4a}\sqrt{c + bx - ax^2} +\frac{b^2 + 4ac}{8\sqrt{a^3}}\arcsin \frac{2ax - b}{\sqrt{b^2 + 4ac}} +C.$
78. $\int \frac{x}{\sqrt{c + bx - ax^2}}\mathrm{d}x = -\frac{1}{a}\sqrt{c + bx - ax^2} +\frac{b}{2\sqrt{a^3}}\arcsin \frac{2ax - b}{\sqrt{b^2 + 4ac}} +C.$

(十) 含有  $\sqrt{\pm\frac{x-a}{x-b}}$  或  $\sqrt{(x-a)(b-x)}$  的积分

79. $\int \sqrt{\frac{x - a}{x - b}}\mathrm{d}x = (x - b)\sqrt{\frac{x - a}{x - b}} +(b - a)\ln (\sqrt{|x - a|} +\sqrt{|x - b|}) + C.$
80. $\int \sqrt{\frac{x - a}{b - x}}\mathrm{d}x = (x - b)\sqrt{\frac{x - a}{b - x}} +(b - a)\arcsin \sqrt{\frac{x - a}{b - a}} +C.$
81. $\int \frac{\mathrm{d}x}{\sqrt{(x - a)(b - x)}} = 2\arcsin \sqrt{\frac{x - a}{b - a}} + C \quad (a < b)$.
82. $\int \sqrt{(x - a)(b - x)}\mathrm{d}x = \frac{2x - a - b}{4}\sqrt{(x - a)(b - x)} +\frac{(b - a)^2}{4}\arcsin \sqrt{\frac{x - a}{b - a}} +C(a <   b).$

(十一) 含有三角函数的积分

83. $\int \sin x\mathrm{d}x = -\cos x + C.$

376

---

附录IV 积分表

84. $\int \cos x\mathrm{d}x = \sin x + C.$
85. $\int \tan x\mathrm{d}x = -\ln |\cos x| + C.$
86. $\int \cot x\mathrm{d}x = \ln |\sin x| + C.$
87. $\int \sec x\mathrm{d}x = \ln \left|\tan \left(\frac{\pi}{4} +\frac{x}{2}\right)\right| + C = \ln |\sec x + \tan x| + C.$
88. $\int \csc x\mathrm{d}x = \ln \left|\tan \frac{x}{2}\right| + C = \ln |\csc x - \cot x| + C.$
89. $\int \sec^2 x\mathrm{d}x = \tan x + C.$
90. $\int \csc^2 x\mathrm{d}x = -\cot x + C.$
91. $\int \sec x\tan x\mathrm{d}x = \sec x + C.$
92. $\int \csc x\cot x\mathrm{d}x = -\csc x + C.$
93. $\int \sin^2 x\mathrm{d}x = \frac{x}{2} -\frac{1}{4}\sin 2x + C.$
94. $\int \cos^2 x\mathrm{d}x = \frac{x}{2} +\frac{1}{4}\sin 2x + C.$
95. $\int \sin^n x\mathrm{d}x = -\frac{1}{n}\sin^{n - 1}x\cos x + \frac{n - 1}{n}\int \sin^{n - 2}x\mathrm{d}x.$
96. $\int \cos^n x\mathrm{d}x = \frac{1}{n}\cos^{n - 1}x\sin x + \frac{n - 1}{n}\int \cos^{n - 2}x\mathrm{d}x.$
97. $\int \frac{\mathrm{d}x}{\sin^n x} = -\frac{1}{n-1} \cdot \frac{\cos x}{\sin^{n-1} x} + \frac{n-2}{n-1} \int \frac{\mathrm{d}x}{\sin^{n-2} x}.$
98. $\int \frac{\mathrm{d}x}{\cos^n x} = \frac{1}{n - 1}\cdot \frac{\sin x}{\cos^{n - 1}x} +\frac{n - 2}{n - 1}\int \frac{\mathrm{d}x}{\cos^{n - 2}x}.$
99. $\int \cos^m x\sin^n x\mathrm{d}x = \frac{1}{m + n}\cos^{m - 1}x\sin^{n + 1}x + \frac{m - 1}{m + n}\int \cos^{m - 2}x\sin^n x\mathrm{d}x$
100. $\int \sin ax\cos bx\mathrm{d}x = -\frac{1}{2(a + b)}\cos (a + b)x - \frac{1}{2(a - b)}\cos (a - b)x + C.$
101. $\int \sin ax\sin bx\mathrm{d}x = -\frac{1}{2(a + b)}\sin (a + b)x + \frac{1}{2(a - b)}\sin (a - b)x + C.$

$$
= - \frac {1}{m + n} \cos^ {m + 1} x \sin^ {n - 1} x + \frac {n - 1}{m + n} \int \cos^ {m} x \sin^ {n - 2} x \mathrm{d} x.
$$

377

---

附录IV. 积分表

102. $\int \cos ax\cos bx\mathrm{d}x = \frac{1}{2(a + b)}\sin (a + b)x + \frac{1}{2(a - b)}\sin (a - b)x + C.$
103. $\int \frac{\mathrm{d}x}{a + b\sin x} = \frac{2}{\sqrt{a^2 - b^2}}\arctan \frac{a\tan\frac{x}{2} + b}{\sqrt{a^2 - b^2}} +C(a^2 >b^2).$
104. $\int \frac{\mathrm{d}x}{a + b\sin x} = \frac{1}{\sqrt{b^2 - a^2}}\ln \left|\frac{a\tan\frac{x}{2} + b - \sqrt{b^2 - a^2}}{a\tan\frac{x}{2} + b + \sqrt{b^2 - a^2}}\right| + C(a^2 <  b^2).$
105. $\int \frac{\mathrm{d}x}{a + b\cos x} = \frac{2}{a + b}\sqrt{\frac{a + b}{a - b}}\arctan \left(\sqrt{\frac{a - b}{a + b}}\tan \frac{x}{2}\right) + C(a^2 >b^2).$
106. $\int \frac{\mathrm{d}x}{a + b\cos x} = \frac{1}{a + b}\sqrt{\frac{a + b}{b - a}}\ln \left|\frac{\tan\frac{x}{2} + \sqrt{\frac{a + b}{b - a}}}{\tan\frac{x}{2} - \sqrt{\frac{a + b}{b - a}}}\right| + C(a^2 < b^2).$
107. $\int \frac{\mathrm{d}x}{a^2\cos^2 x + b^2\sin^2 x} = \frac{1}{ab}\arctan \left(\frac{b}{a}\tan x\right) + C.$
108. $\int \frac{\mathrm{d}x}{a^2\cos^2 x - b^2\sin^2 x} = \frac{1}{2ab}\ln \left|\frac{b\tan x + a}{b\tan x - a}\right| + C.$
109. $\int x\sin ax\mathrm{d}x = \frac{1}{a^2}\sin ax - \frac{1}{a} x\cos ax + C.$
110. $\int x^{2}\sin ax\mathrm{d}x = -\frac{1}{a} x^{2}\cos ax + \frac{2}{a^{2}} x\sin ax + \frac{2}{a^{3}}\cos ax + C.$
111. $\int x\cos ax\mathrm{d}x = \frac{1}{a^2}\cos ax + \frac{1}{a} x\sin ax + C.$
112. $\int x^{2}\cos ax\mathrm{d}x = \frac{1}{a} x^{2}\sin ax + \frac{2}{a^{2}} x\cos ax - \frac{2}{a^{3}}\sin ax + C.$

## (十二) 含有反三角函数的积分(其中 a>0)

113. $\int \arcsin \frac{x}{a} \, \mathrm{d}x = x \arcsin \frac{x}{a} + \sqrt{a^2 - x^2} + C.$

114. $\int x\arcsin \frac{x}{a}\mathrm{d}x = \left(\frac{x^2}{2} -\frac{a^2}{4}\right)\arcsin \frac{x}{a} +\frac{x}{4}\sqrt{a^2 - x^2} +C.$

115. $\int x^{2}\arcsin \frac{x}{a}\mathrm{d}x = \frac{x^{3}}{3}\arcsin \frac{x}{a} +\frac{1}{9} (x^{2} + 2a^{2})\sqrt{a^{2} - x^{2}} +C.$

116. $\int \arccos \frac{x}{a} \mathrm{d}x = x \arccos \frac{x}{a} - \sqrt{a^2 - x^2} + C.$

378

---

附录IV 积分表

117. $\int x\arccos \frac{x}{a}\mathrm{d}x = \left(\frac{x^2}{2} -\frac{a^2}{4}\right)$ arccos $\frac{x}{a} -\frac{x}{4}\sqrt{a^2 - x^2} +C.$
118. $\int x^{2}\arccos \frac{x}{a}\mathrm{d}x = \frac{x^{3}}{3}\arccos \frac{x}{a} -\frac{1}{9}(x^{2} + 2a^{2})\sqrt{a^{2} - x^{2}} +C.$
119. $\int \arctan \frac{x}{a} \mathrm{d}x = x \arctan \frac{x}{a} - \frac{a}{2} \ln (a^2 + x^2) + C.$
120. $\int x\arctan \frac{x}{a}\mathrm{d}x = \frac{1}{2} (a^2 +x^2)\arctan \frac{x}{a} -\frac{a}{2} x + C.$
121. $\int x^{2}\arctan \frac{x}{a}\mathrm{d}x = \frac{x^{3}}{3}\arctan \frac{x}{a} -\frac{a}{6} x^{2} + \frac{a^{3}}{6}\ln (a^{2} + x^{2}) + C.$

## (十三) 含有指数函数的积分

122. $\int a^{x}\mathrm{d}x = \frac{1}{\ln a} a^{x} + C.$
123. $\int \mathrm{e}^{ax}\mathrm{d}x = \frac{1}{a}\mathrm{e}^{ax} + C.$
124. $\int x\mathrm{e}^{ax}\mathrm{d}x = \frac{1}{a^2} (ax - 1)\mathrm{e}^{ax} + C.$
125. $\int x^{n}\mathrm{e}^{ax}\mathrm{d}x = \frac{1}{a} x^{n}\mathrm{e}^{ax} - \frac{n}{a}\int x^{n - 1}\mathrm{e}^{ax}\mathrm{d}x.$
126. $\int x a^{x} \mathrm{~d} x = \frac{x}{\ln a} a^{x} - \frac{1}{(\ln a)^{2}} a^{x} + C.$
127. $\int x^{n}a^{x}\mathrm{d}x = \frac{1}{\ln a} x^{n}a^{x} - \frac{n}{\ln a}\int x^{n - 1}a^{x}\mathrm{d}x.$
128. $\int \mathrm{e}^{ax}\sin bx\mathrm{d}x = \frac{1}{a^2 + b^2}\mathrm{e}^{ax}(a\sin bx - b\cos bx) + C.$
129. $\int \mathrm{e}^{ax}\cos bx\mathrm{d}x = \frac{1}{a^2 + b^2}\mathrm{e}^{ax}(b\sin bx + a\cos bx) + C.$
130. $\int \mathrm{e}^{ax}\sin^n bx\mathrm{d}x = \frac{1}{a^2 + b^2n^2}\mathrm{e}^{ax}\sin^{n - 1}bx(a\sin bx - nb\cos bx) + \frac{n(n - 1)b^2}{a^2 + b^2n^2}\int \mathrm{e}^{ax}\sin^{n - 2}bx\mathrm{d}x.$
131. $\int \mathrm{e}^{ax}\cos^n bx\mathrm{d}x = \frac{1}{a^2 + b^2n^2}\mathrm{e}^{ax}\cos^{n - 1}bx(a\cos bx + nb\sin bx) + \frac{n(n - 1)b^2}{a^2 + b^2n^2}\int \mathrm{e}^{ax}\cos^{n - 2}bx\mathrm{d}x.$

## (十四) 含有对数函数的积分

132. $\int \ln x\mathrm{d}x = x\ln x - x + C.$

379

---

附录IV 积分表

133. $\int \frac{\mathrm{d}x}{x\ln x} = \ln |\ln x| + C.$
134. $\int x^{n}\ln x\mathrm{d}x = \frac{1}{n + 1} x^{n + 1}\left(\ln x - \frac{1}{n + 1}\right) + C.$
135. $\int (\ln x)^n\mathrm{d}x = x(\ln x)^n -n\int (\ln x)^{n - 1}\mathrm{d}x.$
136. $\int x^{m}(\ln x)^{n}\mathrm{d}x = \frac{1}{m + 1} x^{m + 1}(\ln x)^{n} - \frac{n}{m + 1}\int x^{m}(\ln x)^{n - 1}\mathrm{d}x.$

## (十五) 含有双曲函数的积分

137.  $\int sh x dx = ch x + C.$
138.  $\int ch x dx = sh x + C.$
139. $\int \operatorname{th} x \, \mathrm{d}x = \ln \operatorname{ch} x + C.$
140.  $\int sh^{2}x dx = -\frac{x}{2} + \frac{1}{4} sh 2x + C.$
141. $\int \mathrm{ch}^2 x\mathrm{d}x = \frac{x}{2} +\frac{1}{4}\mathrm{sh}2x + C.$

## (十六) 定积分

142. $\int_{-\pi}^{\pi}\cos nx\mathrm{d}x = \int_{-\pi}^{\pi}\sin nx\mathrm{d}x = 0.$
143. $\int_{-\pi}^{\pi}\cos mx\sin nx\mathrm{d}x = 0.$
144. $\int_{-\pi}^{\pi}\cos mx\cos nx\mathrm{d}x = \left\{ \begin{array}{ll}0, & m\neq n,\\ \pi , & m = n. \end{array} \right.$
145. $\int_{-\pi}^{\pi}\sin mx\sin nx\mathrm{d}x = \left\{ \begin{array}{ll}0, & m\neq n,\\ \pi , & m = n. \end{array} \right.$
146. $\int_0^\pi \sin mx\sin nx\mathrm{d}x = \int_0^\pi \cos mx\cos nx\mathrm{d}x = \left\{ \begin{array}{ll}0, & m\neq n,\\ \frac{\pi}{2}, & m = n. \end{array} \right.$
147. $I_{n} = \int_{0}^{\frac{\pi}{2}}\sin^{n}x\mathrm{d}x = \int_{0}^{\frac{\pi}{2}}\cos^{n}x\mathrm{d}x,$

$$
I _ {n} = \frac {n - 1}{n} I _ {n - 2}
$$

380

---

附录IV 积分表

$$
= \left\{ \begin{array}{l l} { \frac {n - 1}{n} \cdot \frac {n - 3}{n - 2} \cdot \dots \cdot \frac {4}{5} \cdot \frac {2}{3} (n \text {为大于1的正奇数}), I _ {1} = 1,} \\ { \frac {n - 1}{n} \cdot \frac {n - 3}{n - 2} \cdot \dots \cdot \frac {3}{4} \cdot \frac {1}{2} \cdot \frac {\pi}{2} (n \text {为正偶数}), \qquad I _ {0} = \frac {\pi}{2}.} \end{array} \right.
$$

381

---

## 部分习题参考答案与提示

## 第一章

## 习题1- 1（第15页）

1. (1) $\left[-\frac{2}{3}, +\infty\right)$; (2) $(- \infty, -1) \cup (-1, 1) \cup (1, +\infty)$; (3) $[-1, 0) \cup (0, 1]$;
(4) $(-2, 2)$; (5) $[0, +\infty)$; (6) $\mathbf{R} \setminus \left\{\left(k + \frac{1}{2}\right)\pi - 1 \mid k \in \mathbf{Z}\right\}$; (7) $[2, 4]$;
(8) $(-∞,0)∪(0,3]$ ; (9) $(-1,+∞)$ ; (10) $(-∞,0)∪(0,+∞)$ .

2. 略.

3. $\varphi \left(\frac{\pi}{6}\right) = \frac{1}{2},\varphi \left(\frac{\pi}{4}\right) = \frac{\sqrt{2}}{2},\varphi \left(-\frac{\pi}{4}\right) = \frac{\sqrt{2}}{2},\varphi (-2) = 0$ ，图略

4. (1)、(2) $f(x)$ 均在 R 上有界.

5. 略.

6.（1）当 $a > 0$ 时，$f(x)$ 在 $\left(-\infty, -\frac{b}{2a}\right)$ 内单调减少，在 $\left(-\frac{b}{2a}, +\infty\right)$ 内单调增加；当 $a < 0$ 时，$f(x)$ 在 $\left(-\infty, -\frac{b}{2a}\right)$ 内单调增加，在 $\left(-\frac{b}{2a}, +\infty\right)$ 内单调减少；

(2) 当  $b > \frac{ad}{c}$  时， $f(x)$  分别在  $\left(-\infty, -\frac{d}{c}\right)$  及  $\left(-\frac{d}{c}, +\infty\right)$  内单调减少；
当  $b < \frac{ad}{c}$  时， $f(x)$  分别在  $\left(-\infty, -\frac{d}{c}\right)$  及  $\left(-\frac{d}{c}, +\infty\right)$  内单调增加；

382

---

部分习题参考答案与提示

当 $b = \frac{ad}{c}$ 时，$f(x) = \frac{a}{c}$，无单调性.

7—8. 略.

9.（1）偶函数；（2）既非奇函数又非偶函数；（3）偶函数；
（4）奇函数；（5）既非奇函数又非偶函数；（6）偶函数.

10.（1）是周期函数,周期  $l=2\pi$ ; （2）是周期函数,周期  $l=\frac{\pi}{2}$ ;

(3) 是周期函数, 周期 l=2; (4) 不是周期函数;

(5) 是周期函数, 周期  $l=\pi$ .

11. (1) $y = x^3 - 1$; (2) $y = \frac{1 - x}{1 + x}$; (3) $y = \frac{-dx + b}{cx - a}$;

(4) $y = \frac{1}{3}\arcsin \frac{x}{2}; \quad (5)y = e^{x - 1} - 2; \quad (6)y = \log_2\frac{x}{1 - x}.$

12. (1) $y = \sin^2 x, y_1 = \frac{1}{4}, y_2 = \frac{3}{4}$;

(2) $y = \sin 2x, y_1 = \frac{\sqrt{2}}{2}, y_2 = 1$;

(3) $y = \sqrt{1 + x^2}, y_1 = \sqrt{2}, y_2 = \sqrt{5}$;

(4)  $y=e^{x^{2}}, y_{1}=1, y_{2}=e;$

(5) $y=e^{2x},y_{1}=e^{2},y_{2}=e^{-2}.$

13. (1) $[-1, 1]$; (2) $\bigcup_{n \in \mathbb{Z}} [2n\pi, (2n + 1)\pi]$; (3) $[-a, 1 - a]$;

(4) 若  $a \in \left(0, \frac{1}{2}\right]$ ，则  $D = [a, 1 - a]$ ; 若  $a > \frac{1}{2}$ ，则  $D = \varnothing$ .

14. $f[g(x)] = \left\{ \begin{array}{ll}1, & x <   0,\\ 0, & x = 0,\\ -1, & x > 0; \end{array} \right.$ $g[f(x)] = \left\{ \begin{array}{ll}\mathrm{e}, & |x| <   1,\\ 1, & |x| = 1,\text{图略}.\\ \mathrm{e}^{-1}, & |x| > 1, \end{array} \right.$

15. $L = \frac{S_0}{h} +\frac{2 - \cos 40^\circ}{\sin 40^\circ} h,h\in (0,\sqrt{S_0\tan 40^\circ})$

16.  $S(t)=\left\{\begin{aligned}&\frac{1}{2}t^{2},&0\leqslant t\leqslant1,\\ &-\frac{1}{2}t^{2}+2t-1,&1<t\leqslant2,\\ &1,&t>2.\end{aligned}\right.$

17. $F = 1.8C + 32$ 或 $C = \frac{5}{9} (F - 32)$

383

---

部分习题参考答案与提示

(1) $90^{\circ}\mathrm{F} = 32.2^{\circ}\mathrm{C}, -5^{\circ}\mathrm{C} = 23^{\circ}\mathrm{F}$; (2) $-40^{\circ}\mathrm{F} = -40^{\circ}\mathrm{C}$.

18.  $y=\left\{\begin{aligned}x^{2}, & 0<x<10,\\ -\frac{4}{5}x^{2}+18x, & 10\leqslant x\leqslant15,\\ -18x+360, & 15<x<20.\end{aligned}\right.$

## 习题1-2（第25页）

1.（1）收敛，0；（2）收敛，0；（3）收敛，2；（4）收敛，1；（5）发散；

(6) 收敛,0; (7) 发散; (8) 发散.

2.（1）必要条件；（2）一定发散；

(3) 不一定收敛,例如数列  $\{(-1)^{n}\}$  有界,但发散.

3.（1）错误，反例略；（2）错误，反例略；（3）正确，理由略；（4）正确，理由略.

\*4. $\lim_{n\to \infty}x_n = 0, N = \left[\frac{1}{\varepsilon}\right], 1000.$

\*5—\*8. 略.

## 习题1-3（第32页）

1. (1) 0; (2) -1; (3) 不存在, 因为 $f(0^{+}) \neq f(0^{-})$.

2.（1）错；（2）对；（3）错；（4）错；（5）对；（6）对.

3.(1)对；(2)对；(3)对；(4)错；(5)对；(6)对；(7)对；(8)错.

4.  $\lim_{x\to0^{-}}f(x)=\lim_{x\to0^{+}}f(x)=1,\lim_{x\to0}f(x)=1;$

$\lim_{x\to 0^{-}}\varphi (x) = -1,\lim_{x\to 0^{+}}\varphi (x) = 1,\lim_{x\to 0}\varphi (x)$ 不存在.

\*5—\*6. 略.

\*7. $\delta = 0.000$ 2. 提示: 因为 $x \to 2$, 所以不妨设 $1 < x < 3$.

\*8. $X \geqslant \sqrt{397}$.

\*9—\*12. 略.

## 习题 1-4（第 36 页）

1. 两个无穷小的商不一定是无穷小,例如: $\alpha = 4x, \beta = 2x$, 当 $x \to 0$ 时都是无穷小, 但 $\frac{\alpha}{\beta}$ 当 $x \to 0$ 时不是无穷小.

\*2. 略.

\*3. $0 < |x| < \frac{1}{10^4 + 2}$.

384

---

部分习题参考答案与提示

4. (1) 2, 提示: 应用本节定理 1; (2) 1, 提示: 应用本节定理 1.
5. 略.
6.  $y = x \cos x$  在  $(-\infty, +\infty)$  内无界, 但当  $x \to +\infty$  时, 此函数不是无穷大.

\*7. 略.

8. 水平渐近线 y=0，铅直渐近线  $x=-\sqrt{2}, x=\sqrt{2}$ .

## 习题1-5（第43页）

1. (1) -9; (2) 0; (3) 0; (4)  $\frac{1}{2}$ ; (5) 2x; (6) 2; (7)  $\frac{1}{2}$ ;
(8) 0; (9)  $\frac{2}{3}$ ; (10) 2; (11) 2; (12)  $\frac{1}{2}$ ; (13)  $\frac{1}{5}$ ; (14) -1.

2. (1) $\infty$; (2) $\infty$; (3) $\infty$.

3. (1) 0; (2) 0.

4.（1）错，例如 $a_{n} = \frac{1}{n}, b_{n} = \frac{n}{n + 1}, n \in \mathbb{N}_{+}$

(2) 错, 例如  $b_{n}=\frac{n+1}{n}, c_{n}=n, n \in N_{+}$ ;
(3) 错, 例如  $a_{n}=\frac{1}{n^{2}}, c_{n}=n, n \in N_{+}$ ;
（4）对，因为，假若 $\lim_{n\to \infty}b_nc_n$ 存在，则 $\lim_{n\to \infty}c_n = \lim_{n\to \infty}b_nc_n\cdot \lim_{n\to \infty}\frac{1}{b_n}$ 也存在，与已知条件矛盾.

5.（1）对，因为，假若 $\lim_{x\to x_0}[f(x) + g(x)]$ 存在，则 $\lim_{x\to x_0}g(x) = \lim_{x\to x_0}[f(x) + g(x)] - \lim_{x\to x_0}f(x)$ 也存在，与已知条件矛盾；

(2) 错, 例如  $f(x)=\operatorname{sgn} x$ ,  $g(x)=-\operatorname{sgn} x$  当  $x \to 0$  时的极限都不存在, 但  $f(x)+g(x) \equiv 0$  当  $x \to 0$  时的极限存在;

(3) 错, 例如 $f(x) = x, \lim_{x \to 0} f(x) = 0, g(x) = \sin \frac{1}{x}, \lim_{x \to 0} g(x)$ 不存在, 但 $\lim_{x \to 0} [f(x) \cdot g(x)] = \lim_{x \to 0} \left( x \sin \frac{1}{x} \right) = 0$;

（4）错，例如 $f(x) = g(x) = \operatorname{sgn} x$ 当 $x \to 0$ 时的极限都不存在，但 $\lim_{x \to 0} f(x) \cdot g(x) = 1.6 - ^*$ 略.

## 习题1-6（第50页）

1. (1) $\omega$; (2) 3; (3) $\frac{2}{5}$; (4) 1; (5) 2; (6) $x$.

385

---

部分习题参考答案与提示

2. (1) $\frac{1}{\mathrm{e}}$; (2) $\mathrm{e}^2$; (3) $\mathrm{e}^2$; (4) $\mathrm{e}^{-k}$.

\*3. 略.

4.（1）提示: $1<\sqrt{1+\frac{1}{n}}<1+\frac{1}{n}$ ;

(2) 提示: $\frac{n}{n + \pi} \leqslant n\left(\frac{1}{n^2 + \pi} + \frac{1}{n^2 + 2\pi} + \cdots + \frac{1}{n^2 + n\pi}\right) \leqslant \frac{n^2}{n^2 + \pi}$;

(3) 提示: 当 x > 0 时,  $1 < \sqrt[n]{1 + x} < 1 + x$ , 当 -1 < x < 0 时,  $1 + x < \sqrt[n]{1 + x} < 1$ ;

(4) 提示: 当 x > 0 时,  $1 - x < x \left[ \frac{1}{x} \right] \leqslant 1$ .

5. 提示: 数列  $\{x_{n}\}$  单调增加且有界,  $\lim_{n\to\infty}x_{n}=2$ .

6. 提示: 数列  $\{x_{n}\}$  单调减少且有界,  $\lim_{n\to\infty}x_{n}=0$ .

## 习题1-7（第53页）

1. 当 $x \to 0$ 时, $x^2 - x^3$ 是比 $2x - x^2$ 高阶的无穷小.

2. 当 $x \to 0$ 时, $(1 - \cos x)^2$ 是比 $\sin^2 x$ 高阶的无穷小.

3.（1）同阶，不等价；（2）等价无穷小.

4. 略.

5. (1) $\frac{3}{2}$; (2) $0 (m < n), 1 (m = n), \infty (m > n)$; (3) $\frac{1}{2}$; (4) -3.

6. 略.

## 习题1-8（第58页）

1. $x = -1, 0, 1, 2$ 均为 $f(x)$ 的间断点，除 $x = 0$ 外它们均为 $f(x)$ 的可去间断点。补充定义 $f(-1) = f(2) = 0$，修改定义，使 $f(1) = 2$.

2. (1)  $f(x)$  在  $[0,2]$  上连续, 图略;

(2) $f(x)$ 在 $(-∞,-1)$ 与 $(-1,+∞)$ 内连续,x=-1为跳跃间断点,图略.

3.（1）x=1 为可去间断点，x=2 为第二类间断点；

(2) x=0 和  $x=k\pi+\frac{\pi}{2}$  为可去间断点,  $x=k\pi$  ( $k \neq 0$ ) 为第二类间断点;

(3) x=0 为第二类间断点；

(4) x=1 为第一类间断点.

4.  $f(x)=\left\{\begin{aligned}x,&\quad|x|<1,\\ 0,&\quad|x|=1,\\ -x,&\quad|x|>1.\end{aligned}\right.$  x=1 和 x=-1 为第一类间断点.

386

---

部分习题参考答案与提示

5.（1）对，因为 $\left|\left|f(x)\right|-\left|f(a)\right|\right|\leqslant\left|f(x)-f(a)\right|$ ，由此可推出结论；

(2) 错, 例如  $f(x)=\left\{\begin{aligned}&1,&x\in\mathbf{Q},\\ &-1,&x\in\mathbf{R}\backslash\mathbf{Q},\end{aligned}\right.\quad\forall a\in\mathbf{R}.$

\*6—8. 略.

## 习题1-9（第63页）

1. 连续区间: $(-∞, -3)$ ， $(-3, 2)$ ， $(2, +∞)$ ;

$$
\lim _ {x \to 0} f (x) = \frac {1}{2}, \quad \lim _ {x \to - 3} f (x) = - \frac {8}{5}, \quad \lim _ {x \to 2} f (x) = \infty .
$$

2. 略.

3. (1) $\sqrt{5}$; (2) 1; (3) 0; (4) $\frac{1}{2}$; (5) 2; (6) $\cos \alpha$; (7) 1; (8) $-\frac{1}{3}$.

4. (1) 1; (2) 0; (3)  $\sqrt{e}$ ; (4)  $e^{3}$ ; (5)  $e^{-\frac{3}{2}}$ ; (6)  $\frac{1}{2}$ ; (7)  $\frac{1}{e}$ ; (8) -6;

(9) $\frac{1}{2}$ ; (10) 不存在.

5.（1）错，例如 $\varphi (x) = \operatorname {sgn}x,f(x) = \mathrm{e}^{x},\varphi [f(x)]\equiv 1$ 在 $\mathbb{R}$ 上处处连续；

(2) 错, 例如 $\varphi(x)=\begin{cases}1,&x\in\mathbf{Q},\\-1,&x\in\mathbf{Q}^{c},\end{cases}\left[\varphi(x)\right]^{2}\equiv1$ 在 $\mathbb{R}$ 上处处连续;

(3) 对, 例如 $\varphi(x)$ 同 (2), $f(x)=|x|+1$, $f[\varphi(x)] \equiv 2$ 在 $\mathbb{R}$ 上处处连续;

(4) 对, 若 $F(x) = \frac{\varphi(x)}{f(x)}$ 在 $\mathbb{R}$ 上连续, 则 $\varphi(x) = F(x)f(x)$ 也在 $\mathbb{R}$ 上连续, 与已知条件矛盾.

6. a = 1.

## 习题 1-10（第 67 页）

1—4. 略.

5. 提示: 在  $(-∞, +∞)$  内找出三个子区间, 使  $f(x) = x^{3} + 2x^{2} - 4x - 1$  在每个子区间的两端异号.

6. 提示: $m \leqslant \frac{f(x_1) + f(x_2) + \cdots + f(x_n)}{n} \leqslant M$, 其中 $m, M$ 分别为 $f(x)$ 在 $[x_1, x_n]$ 上的最小值及最大值.

\*7. 提示: 证明 $f(x)$ 在 $[a, b]$ 上连续.

\*8. 略.

\*9. 若 $f(a^{+})$ 及 $f(b^{-})$ 存在, 则 $f(x)$ 在 $(a, b)$ 内一致连续.

387

---

部分习题参考答案与提示

## 总习题一（第68页）

1.（1）必要，充分；（2）必要，充分；（3）必要，充分；（4）充分必要.

2.1.

3. (1) (B); (2) (B).

4. (1) $(- \infty, 0]$; (2) $[1, e]$; (3) $[0, \tan 1]$; (4) $\bigcup_{n \in \mathbb{Z}} \left[2n\pi - \frac{\pi}{2}, 2n\pi + \frac{\pi}{2}\right]$.

5. $f[f(x)] = f(x), g[g(x)] = 0, f[g(x)] = 0, g[f(x)] = g(x)$.

6. 略.

7.  $V=\frac{R^{3}}{24\pi^{2}}(2\pi-\alpha)^{2}\sqrt{4\pi\alpha-\alpha^{2}}$   $(0<\alpha<2\pi)$ .

\*8. 略.

9. (1) $\infty$; (2) $\frac{1}{2}$; (3) e; (4) $\frac{1}{2}$; (5) $\sqrt[3]{abc}$; (6) 1; (7) $\frac{1}{a}$; (8) -2.

10. a = 0.

11. x=1 是第一类间断点.

12—13. 略.

14.（1）略；（2） $y=2x+1$ ；（3）铅直渐近线 $x=-\frac{1}{e}$ ，斜渐近线 $y=x+\frac{1}{e}$ .

## 第二章

## 习题2-1（第81页）

1.  $\frac{d\theta}{dt}\bigg|_{t=t_{0}}$ .

2.  $\frac{dT}{dt}.$

3. (1) $C'(100) = 80$ 元/件；(2) $C(101) - C(100) = 79.9$ 元 $\approx 80$ 元，边际成本 $C'(x)$ 近似于产量达到 $x$ 单位时再增加1个单位产品所需的成本.

4. $\frac{(-1)^{n - 1}}{n(n + 1)}$.

5. 略.

388

---

部分习题参考答案与提示

6. (1) $-f'(x_0)$; (2) $f'(0)$; (3) $2f'(x_0)$.

7. (B).

8. (A).

9. (1) $4x^{3}$; (2) $\frac{2}{3} x^{-\frac{1}{3}}$; (3) $1.6x^{0.6}$; (4) $-\frac{1}{2} x^{-\frac{3}{2}}$; (5) $-\frac{2}{x^{3}}$; (6) $\frac{16}{5} x^{\frac{11}{5}}$;

(7) $\frac{1}{6} x^{-\frac{5}{6}}$.

10. ${12}\mathrm{\;m}/\mathrm{s}$ .

11. 略.

12. $k_{1} = y^{\prime}\mid_{x = \frac{2}{3}\pi} = -\frac{1}{2},k_{2} = y^{\prime}\mid_{x = \pi} = -1.$

13. 切线方程为 $\frac{\sqrt{3}}{2}x+y-\frac{1}{2}\left(1+\frac{\sqrt{3}}{3}\pi\right)=0$ , 法线方程为 $\frac{2\sqrt{3}}{3}x-y+\frac{1}{2}-\frac{2\sqrt{3}}{9}\pi=0$ .

14.  $x-y+1=0.$

15. (2,4).

16.（1）在 x=0 处连续，不可导；（2）在 x=0 处连续且可导.

17. a=2, b=-1.

18. $f_{+}^{\prime}(0) = 0, f_{-}^{\prime}(0) = -1, f^{\prime}(0)$ 不存在.

19.  $f'(x)=\left\{\begin{aligned}&\cos x,&x<0,\\ &1,&x\geqslant0.\end{aligned}\right.$

20. 略.

## 习题 2-2（第 92 页）

1. 略.

2. (1) $3x^{2} - \frac{28}{x^{5}} + \frac{2}{x^{2}}$; (2) $15x^{2} - 2^{x}\ln 2 + 3e^{x}$; (3) $\sec x(2\sec x + \tan x)$;

(4) $\cos 2x$;

(5)  $x(2\ln x+1)$ ;

(6) $3\mathrm{e}^{x}(\cos x - \sin x)$;

(7) $\frac{1 - \ln x}{x^2}$;

(8) $\frac{\mathrm{e}^x(x - 2)}{x^3}$;

(9) $2x\ln x\cos x+x\cos x-x^{2}\ln x\sin x;$

(10)  $\frac{1+\sin t+\cos t}{(1+\cos t)^{2}}.$

3. (1) $y' \left| _{x = \frac{\pi}{6}} = \frac{\sqrt{3} + 1}{2}, y' \right|_{x = \frac{\pi}{4}} = \sqrt{2}$; (2) $\frac{\sqrt{2}}{4} \left(1 + \frac{\pi}{2}\right)$; (3) $f'(0) = \frac{3}{25}, f'(2) = \frac{17}{15}$.

4. (1) $v(t) = v_0 - gt$; (2) $t = \frac{v_0}{g}$.

389

---

部分习题参考答案与提示

5. 切线方程为 2x-y=0，法线方程为  $x+2y=0$ .

6. (1) $8(2x + 5)^{3}$; (2) $3\sin (4 - 3x)$; (3) $-6xe^{-3x^2}$; (4) $\frac{2x}{1 + x^2}$;

(5) $\sin 2x$; (6) $-\frac{x}{\sqrt{a^2 - x^2}}$; (7) $2x\sec^2 (x^2)$; (8) $\frac{\mathrm{e}^x}{1 + \mathrm{e}^{2x}}$;

(9) $\frac{2\arcsin x}{\sqrt{1 - x^2}}$; (10) $-\tan x$.

7. (1) $-\frac{1}{\sqrt{x - x^2}}$; (2) $\frac{x}{\sqrt{(1 - x^2)^3}}$;

(3) $-\frac{1}{2}\mathrm{e}^{-\frac{x}{2}}(\cos3x+6\sin3x);$  (4) $\frac{|x|}{x^{2}\sqrt{x^{2}-1}};$

(5) $-\frac{2}{x(1 + \ln x)^2}$; (6) $\frac{2x\cos 2x - \sin 2x}{x^2}$;

(7) $\frac{1}{2\sqrt{x - x^2}}$; (8) $\frac{1}{\sqrt{a^2 + x^2}}$;

(9) sec x; (10)  $\csc x.$

8. (1) $\frac{2\arcsin\frac{x}{2}}{\sqrt{4 - x^2}}$; (2) $\csc x$;

(3) $\frac{\ln x}{x\sqrt{1 + \ln^2x}}$; (4) $\frac{\mathrm{e}^{\arctan\sqrt{x}}}{2\sqrt{x}(1 + x)}$;

(5) $n\sin^{n - 1}x\cos (n + 1)x;$ (6） $-\frac{1}{1 + x^2};$

(7) $\frac{\pi}{2\sqrt{1 - x^2} (\arccos x)^2}$; (8) $\frac{1}{x \ln x \cdot \ln (\ln x)}$;

(9) $\frac{1}{\sqrt{1 - x^2 + 1 - x^2}}$; (10) $-\frac{1}{(1 + x)\sqrt{2x(1 - x)}}$.

9. $\frac{f(x)f'(x) + g(x)g'(x)}{\sqrt{f^2(x) + g^2(x)}}.$

10. (1) $2xf'(x^2)$; (2) $\sin 2x[f'(\sin^2 x) - f'(\cos^2 x)]$;

(3) $\frac{\mathrm{e}^x f'( \mathrm{e}^x) - f'(x)f(\mathrm{e}^x)}{\mathrm{e}^{f(x)}}.$

11. (1)  $\mathrm{e}^{-x}\left(-x^{2}+4x-5\right)$ ; (2)  $\sin 2x\sin(x^{2})+2x\sin^{2}x\cos(x^{2})$ ;

(3) $\frac{4}{4 + x^2}\arctan \frac{x}{2};$ (4) $\frac{1 - n\ln x}{x^{n + 1}};$

390

---

部分习题参考答案与提示

(5) $\frac{4}{\mathrm{e}^{2t} + \mathrm{e}^{-2t} + 2}$ 或 $\frac{1}{\mathrm{ch}^2 t}$;

(6) $\frac{1}{x^2} \tan \frac{1}{x}$;

(7) $\frac{1}{x^2}\sin \frac{2}{x} \cdot e^{-\sin^2\frac{1}{x}};$

(8) $\frac{2\sqrt{x} + 1}{4\sqrt{x}\sqrt{x + \sqrt{x}}};$

(9) $\arcsin \frac{x}{2}$;

(10) $y' = \begin{cases} \frac{2}{1 + t^2}, & |t| < 1, \\ -\frac{2}{1 + t^2}, & |t| > 1. \end{cases}$

\*12. (1) sh(sh x) · ch x;

(2) $\mathrm{e}^{\mathrm{ch}x}(\mathrm{ch}x + \mathrm{sh}^2 x)$;

(3) $\frac{1}{x\mathrm{ch}^{2}(\ln x)}$ ;

(4) $(3\mathrm{sh}x+2)\mathrm{sh}x\mathrm{ch}x;$

(5) $-\frac{2x}{\mathrm{ch}^{2}(1-x^{2})};$

(6) $\frac{2x}{\sqrt{x^4 + 2x^2 + 2}};$

(7) $\frac{2\mathrm{e}^{2x}}{\sqrt{\mathrm{e}^{4x} - 1}};$

(8) $\frac{1}{1 + 2\mathrm{sh}^2x}$;

(9) $\mathrm{th}^3 x$;

(10) $\frac{2}{(x + 1)^2}\mathrm{sh}\left(2\cdot \frac{x - 1}{x + 1}\right)$.

13. $f(x)g(x)$ 在 $x_0$ 处可导，其导数为 $f'(x_0)g(x_0)$.

14. 略.

## 习题 2-3（第 97 页）

1. (1) $4 - \frac{1}{x^2}$;

(2) $4e^{2x-1}$ ;

(3)  $-2\sin x-x\cos x;$

(4) $-2\mathrm{e}^{-t}\cos t;$

(5) $-\frac{a^{2}}{(a^{2}-x^{2})^{3/2}};$

(6) $-\frac{2(1 + x^2)}{(1 - x^2)^2}$;

(7)  $2\sec^{2}x\tan x;$

(8) $\frac{6x(2x^3 - 1)}{(x^3 + 1)^3}$;

(9)  $2 \arctan x + \frac{2x}{1 + x^{2}};$

(10) $\frac{\mathrm{e}^x(x^2 - 2x + 2)}{x^3}$;

(11) $2xe^{x^{2}}(3+2x^{2})$;

(12) $-\frac{x}{(1 + x^2)^{3 / 2}}.$

2.  $f'''(2)=207\ 360.$

3. (1) $2f'(x^2) + 4x^2 f''(x^2)$;

(2) $\frac{f''(x)f(x)-[f'(x)]^2}{[f(x)]^2}$.

391

---

部分习题参考答案与提示

4. 略.

5. $\frac{\mathrm{d}^2s}{\mathrm{d}t^2} = -A\omega^2\sin \omega t.$

6. 略.

7. $\frac{\mathrm{d}^2x}{\mathrm{d}t^2} = f(x)f'(x)$.

8. $a = 0, b = c = 1$.

9. (1) $-4\mathrm{e}^{x}\cos x$; (2) $2^{50}\left(-x^{2}\sin 2x + 50x\cos 2x + \frac{1225}{2}\sin 2x\right)$.

\* 10. (1) $n!$; (2) $2^{n-1} \sin \left[ 2x + (n-1)\frac{\pi}{2} \right]$; (3) $(-1)^{n}\frac{(n-2)!}{x^{n-1}} (n \geqslant 2)$; (4) $\mathrm{e}^{x}(x+n)$.

\*11. $(-1)^{n - 1}\frac{n!}{n - 2} (n\geqslant 3)$

## 习题 2-4（第 106 页）

1. (1) $\frac{y}{y - x}$; (2) $\frac{ay - x^2}{y^2 - ax}$; (3) $\frac{\mathrm{e}^{x + y} - y}{x - \mathrm{e}^{x + y}}$; (4) $-\frac{\mathrm{e}^y}{1 + x\mathrm{e}^y}$.

2. 切线方程为 $x + y - \frac{\sqrt{2}}{2} a = 0$，法线方程为 $x - y = 0$.

3. 点  $M(-1,-2)$  处有水平切线，点  $N(2,1)$  处有铅直切线.

4. (1) $-\frac{b^4}{a^2y^3}$; (2) $-2\csc^2 (x + y)\cot^3 (x + y)$; (3) $\frac{\mathrm{e}^{2y}(3 - y)}{(2 - y)^3}$; (4) $\frac{1}{[2 + \ln(x - y)]^3(x - y)}$.

5. (1) $\left(\frac{x}{1 + x}\right)^x\left(\ln \frac{x}{1 + x} + \frac{1}{1 + x}\right)$;

(2) $\frac{1}{5} \sqrt[5]{\frac{x - 5}{\sqrt[5]{x^2 + 2}}} \left[ \frac{1}{x - 5} - \frac{2x}{5(x^2 + 2)} \right]$;

(3) $\frac{\sqrt{x + 2}(3 - x)^4}{(x + 1)^5}\left[\frac{1}{2(x + 2)} -\frac{4}{3 - x} -\frac{5}{x + 1}\right]$;

(4) $\frac{1}{2}\sqrt{x\sin x\sqrt{1 - e^x}}\left[\frac{1}{x} +\cot x - \frac{e^x}{2(1 - e^x)}\right].$

6. (1) $\frac{3b}{2a} t$; (2) $\frac{\cos \theta - \theta \sin \theta}{1 - \sin \theta - \theta \cos \theta}$.

392

---

部分习题参考答案与提示

7. $\sqrt{3} - 2.$

8.（1）切线方程为 $2\sqrt{2} x + y - 2 = 0$ ，法线方程为 $\sqrt{2} x - 4y - 1 = 0$
(2) 切线方程为  $4x + 3y - 12a = 0$ ，法线方程为  $3x - 4y + 6a = 0$ .

9. (1) $\frac{1}{t^3}$; (2) $-\frac{b}{a^2\sin^3 t}$; (3) $\frac{4}{9} e^{3t}$; (4) $\frac{1}{f''(t)}$.

\*10. (1) $-\frac{3}{8t^5} (1 + t^2)$; (2) $\frac{t^4 - 1}{8t^3}$.

11.  $144\pi m^{2}/s$ .

12.  $\frac{16}{25\pi} \approx 0.204 \, m/min.$

13. ${0.64}\mathrm{\;{cm}}/\mathrm{{min}}$ .

## 习题 2-5（第 117 页）

1. 当 $\Delta x = 1$ 时, $\Delta y = 18$, $\mathrm{dy} = 11$; 当 $\Delta x = 0.1$ 时, $\Delta y = 1.161$, $\mathrm{dy} = 1.1$; 当 $\Delta x = 0.01$ 时, $\Delta y = 0.110601$, $\mathrm{dy} = 0.11$.

2. (a)  $\Delta y > 0, dy > 0, \Delta y - dy > 0;$  (b)  $\Delta y > 0, dy > 0, \Delta y - dy < 0;$
(c)  $\Delta y < 0, dy < 0, \Delta y - dy < 0;$  (d)  $\Delta y < 0, dy < 0, \Delta y - dy > 0.$

3. (1) $\left(-\frac{1}{x^2} + \frac{\sqrt{x}}{x}\right) \mathrm{d}x$; (2) $(\sin 2x + 2x \cos 2x) \mathrm{d}x$;

(3) $(x^{2}+1)^{-\frac{3}{2}}dx;$  (4) $\frac{2\ln(1-x)}{x-1}dx;$

(5) $2x(1+x)\mathrm{e}^{2x}\mathrm{d}x;$ (6) $\mathrm{e}^{-x}\left[\sin(3-x)-\cos(3-x)\right]\mathrm{d}x;$

(7) $\mathrm{dy} = \left\{ \begin{array}{l}\frac{\mathrm{dx}}{\sqrt{1 - x^2}}, - 1 <   x <   0,\\ -\frac{\mathrm{dx}}{\sqrt{1 - x^2}},0 <   x <   1; \end{array} \right.$ (8) $8x\tan (1 + 2x^{2})\sec^{2}(1 + 2x^{2})\mathrm{dx};$

(9) $-\frac{2x}{1+x^{4}}dx;$  (10) $A\omega\cos(\omega t+\varphi)\mathrm{d}t.$

4. (1) $2x + C$; (2) $\frac{3}{2} x^2 + C$; (3) $\sin t + C$; (4) $-\frac{1}{\omega} \cos \omega x + C$;
(5) $\ln (1 + x) + C$; (6) $-\frac{1}{2}\mathrm{e}^{-2x} + C$; (7) $2\sqrt{x} + C$; (8) $\frac{1}{3}\tan 3x + C$.

5. 约为 $\frac{8f}{3l}\Delta f.$

6. 约减少  $43.63 \, cm^{2}$ ，约增加  $104.72 \, cm^{2}$ .

393

---

部分习题参考答案与提示

7. (1) 0.874 75; (2) -0.965 09.

8. (1) ${30}^{ \circ  }{47}^{\prime \prime }$ ; (2) ${60}^{ \circ  }{2}^{\prime }$ .

9.  $\tan 45'\approx0.013\ 09,\ln 1.002\approx0.002.$

10. (1) 9.9867; (2) 2.0052.

\*11. 0.667%.

\*12. $\delta_{\alpha} = 0.00056\mathrm{rad} = 1'55''$ .提示:先求出圆心角 $\alpha$ 与弦长 $l$ 的函数关系式

## 总习题二（第119页）

1.（1）充分，必要；（2）充分必要；（3）充分必要.

2. $n!$.

3. (D).

4.  $\frac{dm}{dx}\bigg|_{x=x_{0}}$ .

5. $-\frac{1}{x^{2}}$

6. (1) $f_{-}^{\prime}(0) = f_{+}^{\prime}(0) = f^{\prime}(0) = 1$; (2) $f_{-}^{\prime}(0) = 1, f_{+}^{\prime}(0) = 0, f^{\prime}(0)$ 不存在.

7. 在 x=0 处连续, 不可导.

8. (1) $\frac{\cos x}{|\cos x|}$; (2) $\frac{1}{1 + x^2}$; (3) $\sin x \cdot \ln \tan x$; (4) $\frac{\mathrm{e}^x}{\sqrt{1 + \mathrm{e}^{2x}}}$;

(5) $x^{\frac{1}{x}-2}(1-\ln x)$ .

9. (1)  $-2\cos 2x \cdot \ln x - \frac{2\sin 2x}{x} - \frac{\cos^{2}x}{x^{2}}$ ; (2)  $\frac{3x}{(1-x^{2})^{5/2}}$ .

\* 10. (1) $\frac{1}{m}\left(\frac{1}{m} - 1\right) \cdots \left(\frac{1}{m} - n + 1\right)\left(1 + x\right)^{\frac{1}{m} - n}$; (2) $(-1)^n \frac{2 \cdot n!}{(1 + x)^{n+1}}$.

11.  $y''(0)=\frac{1}{e^{2}}$ .

12. $\frac{1}{2}$ .

13. (1) $\frac{\mathrm{dy}}{\mathrm{dx}} = -\tan \theta, \frac{\mathrm{d}^2y}{\mathrm{dx}^2} = \frac{1}{3a}\sec^4\theta \csc \theta;$ (2) $\frac{\mathrm{dy}}{\mathrm{dx}} = \frac{1}{t}, \frac{\mathrm{d}^2y}{\mathrm{dx}^2} = -\frac{1 + t^2}{t^3}.$

14. 切线方程为  $x+2y-4=0$ ，法线方程为 2x-y-3=0.

15. 切线方程为 $y = 2x - 12$. 提示: 先求 $f(1), f'(1)$, 再利用周期性, 求 $f(6), f'(6)$.

16. $y = H\left[2\left(\frac{x}{L}\right)^{3} + 3\left(\frac{x}{L}\right)^{2}\right].$

394

---

部分习题参考答案与提示

17. -2.8 km/h.
18. 1.007.
19. 约需加长 2.23 cm.

## 第三章

## 习题3-1（第129页）

1—4. 略.

5. 有分别位于区间(1,2)，(2,3)及(3,4)内的三个根.

6—\*13. 略.

14. 提示: 令 $\varphi(x)=f(x)\mathrm{e}^{-x}$, 先证明 $\varphi(x)$ 为常数.

\*15. 略.

## 习题3-2（第133页）

1. (1) 1; (2) 2; (3) 2; (4) $-\frac{3}{5}$; (5) $-\frac{1}{8}$; (6) $\frac{m}{n} a^{m-n}$;
(7) 1; (8) 3; (9) 1; (10) 1; (11)  $\frac{1}{2}$ ; (12)  $+\infty$ ;
(13) $-\frac{1}{2}$ ; (14) $e^{2}$ ; (15) 1; (16) 1.

2—3. 略.

\*4. 连续.

## 习题 3-3（第 140 页）

1. $f(x) = -56 + 21(x - 4) + 37(x - 4)^{2} + 11(x - 4)^{3} + (x - 4)^{4}$.
2. $f(x) = x^{6} - 9x^{5} + 30x^{4} - 45x^{3} + 30x^{2} - 9x + 1.$
3. $\sqrt{x} = 2 + \frac{1}{4} (x - 4) - \frac{1}{64} (x - 4)^2 + \frac{1}{512} (x - 4)^3 - \frac{15(x - 4)^4}{4!16[4 + \theta(x - 4)]^{\frac{7}{2}}} (0 < \theta < 1)$.
4. $\ln x = \ln 2 + \frac{1}{2} (x - 2) - \frac{1}{2^3} (x - 2)^2 +\frac{1}{3\cdot 2^3} (x - 2)^3 -\dots +(-1)^{n - 1}\frac{1}{n\cdot 2^n} (x - 2)^n +o((x - 2)^n).$
5.  $\frac{1}{x}=-\left[1+(x+1)+(x+1)^{2}+\cdots+(x+1)^{n}\right]+\left(-1\right)^{n+1}\frac{(x+1)^{n+1}}{\left[-1+\theta(x+1)\right]^{n+2}}\quad(0<\theta<1).$

395

---

部分习题参考答案与提示

6. $\tan x = x + \frac{1}{3} x^3 + o(x^3)$.

7.  $xe^{x}=x+x^{2}+\frac{x^{3}}{2!}+\cdots+\frac{x^{n}}{(n-1)!}+o(x^{n})$

8. $\sqrt{\mathrm{e}} \approx 1.645$.

9. (1)  $\sqrt[3]{30} \approx 3.10724, |R_{3}| < 1.88 \times 10^{-5}$ ;

(2) $\sin 18^{\circ} \approx 0.3090, |R_{3}| < 1.3 \times 10^{-4}$.

\*10. (1) $\frac{3}{2}$; (2) $\frac{1}{6}$; (3) $-\frac{1}{12}$; (4) $\frac{1}{2}$.

11. 略.

## 习题 3-4（第 147 页）

1. 单调减少.

2. 单调增加.

3.（1）在 $(-∞,-1]$ ， $[3,+∞)$ 内单调增加，在 $[-1,3]$ 上单调减少；

(2) 在 $(0,2]$ 内单调减少, 在 $[2,+\infty)$ 内单调增加;

(3) 在 $(-∞,0)$ ， $\left(0,\frac{1}{2}\right]$ ， $[1,+∞)$ 内单调减少，在 $\left[\frac{1}{2},1\right]$ 上单调增加；

(4) 在 $(-∞,+∞)$ 内单调增加；

(5) 在 $\left(-\infty,\frac{1}{2}\right]$ 内单调减少，在 $\left[\frac{1}{2},+\infty\right)$ 内单调增加；

(6) 在 $\left(-\infty,\frac{2}{3}a\right]$ ， $[a,+\infty)$ 内单调增加，在 $\left[\frac{2}{3}a,a\right]$ 上单调减少；

(7) 在 $[0,n]$ 上单调增加, 在 $[n,+\infty)$ 内单调减少;

(8) 在  $\left[\frac{k\pi}{2}, \frac{k\pi}{2} + \frac{\pi}{3}\right]$  上单调增加，在  $\left[\frac{k\pi}{2} + \frac{\pi}{3}, \frac{k\pi}{2} + \frac{\pi}{2}\right]$  上单调减少 ( $k \in Z$ ).

4. (D).

5. 略.

6. 当  $a > \frac{1}{e}$  时没有实根, 当  $0 < a < \frac{1}{e}$  时有两个实根, 当  $a = \frac{1}{e}$  时只有 x = e 一个实根.

7. 不一定. $f(x) = x + \sin x$ 在 $(- \infty, +\infty)$ 内单调, 但 $f'(x)$ 在 $(- \infty, +\infty)$ 内不单调.

8. 略.

9. (1) 是凸的;

(2) 在 $(-∞,0]$ 内是凸的，在 $[0,+∞)$ 内是凹的；

(3) 是凹的； (4) 是凹的.

396

---

部分习题参考答案与提示

10.（1）拐点 $\left(\frac{5}{3},\frac{20}{27}\right)$ ，在 $\left(-\infty,\frac{5}{3}\right]$ 内是凸的，在 $\left[\frac{5}{3},+\infty\right)$ 内是凹的；

(2) 拐点 $\left(2,\frac{2}{\mathrm{e}^{2}}\right)$ ，在 $(-∞,2]$ 内是凸的，在 $[2,+∞)$ 内是凹的；

(3) 没有拐点,处处是凹的;

(4) 拐点 $(-1,\ln2),(1,\ln2)$ ，在 $(-∞,-1],[1,+∞)$ 内是凸的，在 $[-1,1]$ 上是凹的；

(5) 拐点 $\left(\frac{1}{2}, e^{\arctan\frac{1}{2}}\right)$ ，在 $\left(-\infty, \frac{1}{2}\right]$ 内是凹的，在 $\left[\frac{1}{2}, +\infty\right)$ 内是凸的；

(6) 拐点 $(1,-7)$ ，在 $(0,1]$ 内是凸的，在 $[1,+\infty)$ 内是凹的.

11. 略.

\*12. 拐点:  $(-1,-1)$ ,  $\left(2-\sqrt{3},\frac{1-\sqrt{3}}{4(2-\sqrt{3})}\right)$ ,  $\left(2+\sqrt{3},\frac{1+\sqrt{3}}{4(2+\sqrt{3})}\right)$ .

13.  $a=-\frac{3}{2}, b=\frac{9}{2}.$

14.  $a=1, b=-3, c=-24, d=16.$

15.  $k=\pm\frac{\sqrt{2}}{8}$ .

\*16. $(x_{0},f(x_{0}))$ 为拐点.

## 习题3-5（第157页）

1.（1）极大值 $f(-1)=17$ ，极小值 $f(3)=-47$ ;

(2) 极小值  $f(0)=0;$

(3) 极大值  $f(\pm1)=1$ , 极小值  $f(0)=0$ ;

(4) 极大值 $f\left(\frac{3}{4}\right)=\frac{5}{4}$;

(5) 极大值 $f\left(\frac{12}{5}\right)=\frac{1}{10}\sqrt{205}$;

(6) 极大值  $f(0)=4$ ，极小值  $f(-2)=\frac{8}{3}$ ;

(7) 极大值 $f\left(\frac{\pi}{4} + 2k\pi\right) = \frac{\sqrt{2}}{2}\mathrm{e}^{\frac{\pi}{4} + 2k\pi}$，极小值 $f\left(\frac{\pi}{4} + (2k + 1)\pi\right) = -\frac{\sqrt{2}}{2}\mathrm{e}^{\frac{\pi}{4} + (2k + 1)\pi}$ ($k \in \mathbb{Z}$)；

(8) 极大值  $f(e)=e^{\frac{1}{e}}$ ; (9) 没有极值; (10) 没有极值.

2. 略.

397

---

部分习题参考答案与提示

3. $a = 2, f\left(\frac{\pi}{3}\right) = \sqrt{3}$ 为极大值.
4. 略,
5. 极小值 $f(0) = 4$.
6.（1）最大值 $f(4)=80$ ，最小值 $f(-1)=-5$ ;
(2) 最大值  $f(3)=11$ , 最小值  $f(2)=-14$ ;
(3) 最大值  $f\left(\frac{3}{4}\right)=1.25$ ，最小值  $f(-5)=-5+\sqrt{6}$ .
7. 当 x=1 时函数有最大值 -29.
8.（1）当 $x = -3$ 时函数有最小值27；（2）当 $x = 1$ 时函数有最大值 $\frac{1}{2}$.
9.  $\frac{1}{e}$ .
10. 长为  $10 \, m$ ，宽为  $5 \, m$ .
11.  $r=\sqrt[3]{\frac{V}{2\pi}}$ ,  $h=2\sqrt[3]{\frac{V}{2\pi}}$ ; d:h=1:1.
12. 底宽为  $\sqrt{\frac{40}{4+\pi}} = 2.367 \, (\text{m})$ .
13. 当  $\alpha = \arctan \mu = \arctan 0.25 \approx 14^{\circ} 2'$  时, 可使力 F 最小.
14. 杆长为 1.4 m.
15.  $\varphi=\frac{2\sqrt{6}}{3}\pi.$
16. 当 $\varphi = 54^{\circ}13'$ 时, 屋架可吊到最大高度 $7.506\mathrm{m}$, 而柱子高只有 $6\mathrm{m}$, 所以能吊得上去. 提示: 设吊臂对地面的倾角为 $\varphi$ 时, 屋架吊起的高度为 $h$, 建立 $h$ 与 $\varphi$ 间的函数关系式, 然后求出 $h$ 的最大值.
17. 7 200 元.
18.60元.

## 习题3-6（第163页）

1. 在 $(-∞,-2]$ 内单调减少，在 $[-2,+∞)$ 内单调增加；在 $(-∞,-1],[1,+∞)$ 内是凹的，在 $[-1,1]$ 上是凸的；拐点 $\left(-1,-\frac{6}{5}\right),(1,2)$ .

2. 对称于原点; 在 $(- \infty, -1], [1, +\infty)$ 内单调减少, 在 $[-1, 1]$ 上单调增加; 在 $(- \infty, -\sqrt{3}], [0, \sqrt{3}]$ 上是凸的, 在 $[- \sqrt{3}, 0], [\sqrt{3}, +\infty)$ 内是凹的; 拐点

398

---

部分习题参考答案与提示

$\left(-\sqrt{3}, -\frac{\sqrt{3}}{4}\right), (0, 0), \left(\sqrt{3}, \frac{\sqrt{3}}{4}\right)$; 水平渐近线 $y = 0$.

3. 在 $(- \infty, 1]$ 内单调增加，在 $[1, +\infty)$ 内单调减少；在 $\left(-\infty, 1 - \frac{\sqrt{2}}{2}\right], \left[1 + \frac{\sqrt{2}}{2}, +\infty\right)$ 内是凹的，在 $\left[1 - \frac{\sqrt{2}}{2}, 1 + \frac{\sqrt{2}}{2}\right]$ 上是凸的；拐点 $\left(1 - \frac{\sqrt{2}}{2}, \frac{1}{\sqrt{\mathrm{e}}}\right), \left(1 + \frac{\sqrt{2}}{2}, \frac{1}{\sqrt{\mathrm{e}}}\right)$；水平渐近线 $y = 0$.

4. 在 $(- \infty, 0)$, $\left(0, \frac{\sqrt[3]{4}}{2}\right]$ 内单调减少, 在 $\left[\frac{\sqrt[3]{4}}{2}, +\infty\right)$ 内单调增加; 在 $(- \infty, -1], (0, +\infty)$ 内是凹的, 在 $[-1, 0)$ 内是凸的; 拐点 $(-1, 0)$; 铅直渐近线 $x = 0$.

5. 定义域为 $\left\{x \mid x \in \mathbb{R} \text{ 且 } x \neq \left(\frac{k}{2} + \frac{1}{4}\right) \pi (k \in \mathbb{Z})\right\}$; 周期为 $2\pi$; 图形对称于 $y$ 轴; 在 $[0, \pi]$ 部分: 在 $\left[0, \frac{\pi}{4}\right), \left(\frac{\pi}{4}, \frac{3\pi}{4}\right), \left(\frac{3\pi}{4}, \pi\right]$ 内单调增加; 在 $\left[0, \frac{\pi}{4}\right)$ 内是凹的, 在 $\left(\frac{\pi}{4}, \frac{\pi}{2}\right]$ 内是凸的, 在 $\left[\frac{\pi}{2}, \frac{3\pi}{4}\right)$ 内是凹的, 在 $\left(\frac{3\pi}{4}, \pi\right]$ 内是凸的; 拐点 $\left(\frac{\pi}{2}, 0\right)$; 铅直渐近线 $x = \frac{\pi}{4}, x = \frac{3\pi}{4}$.

## 习题3-7（第172页）

1. $K = 2$

2. $K = |\cos x|, \rho = |\sec x|$.

3. $K = 2, \rho = \frac{1}{2}$.

4. $K = \left|\frac{2}{3a\sin 2t_0}\right|.$

5. $\left(\frac{\sqrt{2}}{2}, -\frac{\ln 2}{2}\right)$ 处曲率半径有最小值 $\frac{3\sqrt{3}}{2}$.

\*6. 略.

7. 约 1246 N. 提示: 沿曲线运动的物体所受的向心力为  $F = \frac{mv^{2}}{\rho}$ ，这里 m 为物体的质量, v 为它的速率,  $\rho$  为运动轨迹的曲率半径.

8. 约 45 400 N. 参看上题提示.

9. 略.

399

---

部分习题参考答案与提示

\*10. $\left(\xi -\frac{\pi - 10}{4}\right)^2 +\left(\eta -\frac{9}{4}\right)^2 = \frac{125}{16}.$

\* 11. $\left\{\begin{aligned}\alpha&=\frac{3y^{2}}{2p}+p,\\ \beta&=-\frac{y^{3}}{p^{2}}\end{aligned}\right.$ 或 $27p\beta^{2}=8(\alpha-p)^{3}.$

## 习题 3-8 (第 177 页)

1. $0.18 < \xi < 0.19$.
2. -0.20<ξ<-0.19.
3. $0.32 < \xi < 0.33$.
4. ${2.50} < \xi  < {2.51}$ .

## 总习题三（第177页）

1. 2.
2. (1) (B); (2) (D).
3.  $f(x)=\left|x\right|,x\in[-1,1].$
4. ka.

5—9. 略.

10. (1) 2; (2)  $\frac{1}{2}$ ; (3)  $e^{-\frac{2}{\pi}}$ ; (4)  $a_{1}a_{2}\cdots a_{n}$ .
11. (1) $x^{3} \ln x = (x - 1) + \frac{5}{2!}(x - 1)^{2} + \frac{11}{3!}(x - 1)^{3} + \frac{6}{4!}(x - 1)^{4} - \frac{6}{5!\xi^{2}}(x - 1)^{5}$, 其中 $\xi$ 介于 1 与 $x$ 之间;

(2)  $\arctan x = x - \frac{x^{3}}{3} + o(x^{4})$ ;
(3)  $e^{\sin x}=1+x+\frac{1}{2}x^{2}+o(x^{3})$ ;
(4) $\ln \cos x = -\frac{1}{2} x^2 - \frac{1}{12} x^4 - \frac{1}{45} x^6 + o(x^6)$.

12. 略.
13. $a = \mathrm{e}^{\mathrm{e}}$ ，最小值 $1 - \frac{1}{\dot{\mathrm{e}}}$
14. (1,2) 和  $(-1,-2)$ .
15. 2ab.

400

---

部分习题参考答案与提示

16.  $\sqrt[3]{3}$ .
17. $\left(\frac{\pi}{2},1\right)$ 处曲率半径有最小值1.
18. ${2.414} < \xi  < {2.415}$ .
\*19. 提示: 可以先用一次洛必达法则.
20. 提示: 记 $x_0 = (1 - t)x_1 + tx_2$, 先证 $f(x) \geqslant f(x_0) + f'(x_0)(x - x_0)$, 然后在上式中分别令 $x = x_1$ 及 $x = x_2$, 可得两个不等式, 由此推出结论.
21.  $a=\frac{4}{3}, b=-\frac{1}{3}.$

## 第四章

## 习题4-1（第187页）

1. 略.

2. (1) $-\frac{1}{x} + C;$

(2) $\frac{2}{5} x^{\frac{5}{2}} + C$;

(3) $2\sqrt{x}+C;$

(4) $\frac{3}{10} x^{\frac{10}{3}} + C$;

(5) $-\frac{2}{3}x^{-\frac{3}{2}}+C;$

(6) $\frac{m}{m + n} x^{\frac{m + n}{m}} + C;$

(7) $\frac{5}{4} x^4 + C$;

(8) $\frac{x^3}{3} - \frac{3}{2} x^2 + 2x + C$;

(9) $\sqrt{\frac{2h}{g}} + C$;

(10) $\frac{x^5}{5} + \frac{2}{3} x^3 + x + C$;

(11) $\frac{x^3}{3} + \frac{2}{5} x^{\frac{5}{2}} - \frac{2}{3} x^{\frac{3}{2}} - x + C$;

(12) $2\sqrt{x}-\frac{4}{3}x^{\frac{3}{2}}+\frac{2}{5}x^{\frac{5}{2}}+C;$

(13) $2\mathrm{e}^{x}+3\ln|x|+C;$

(14) 3arctan x-2arcsin  $x+C$ ;

(15)  $e^{x}-2\sqrt{x}+C;$

(16) $\frac{3^x\mathrm{e}^x}{\ln 3 + 1} +C;$

(17) $2x-\frac{5\left(\frac{2}{3}\right)^{x}}{\ln2-\ln3}+C;$

(18) $\tan x - \sec x + C$;

(19) $\frac{x + \sin x}{2} + C$;

(20) $\frac{1}{2} \tan x + C$;

401

---

部分习题参考答案与提示

(21)  $\sin x - \cos x + C;$ 

(22)  $-(\cot x + \tan x) + C;$
(23)  $-\cot x-x+C;$ 

(24)  $-\cos\theta+\theta+C;$
(25) $x - \arctan x + C$; (26) $x^3 - x + \arctan x + C$.

3. (1) $y = \frac{1}{3} (x^3 - 6x^2 + 12x - 8)$; (2) $x = \frac{1}{t} + 2t - 2$.

4. (1) $s = 20t - \frac{1}{2}kt^2$; (2) $t = \frac{20}{k}, s = \frac{200}{k}$; (3) $k = 4$.

答: 刹车加速度为  $-4 \, m/s^{2}$ .

5.  $y = \ln x + 1.$

6. (1) 27 m; (2)  $\sqrt[3]{360} \approx 7.11 \, (\text{s})$ .

7. 略.

## 习题4-2（第202页）

1. (1) $\frac{1}{a}$; (2) $\frac{1}{7}$; (3) $\frac{1}{2}$; (4) $\frac{1}{10}$; (5) $-\frac{1}{2}$; (6) $\frac{1}{12}$; (7) $\frac{1}{2}$;
(8) -2; (9)  $-\frac{2}{3}$ ; (10)  $\frac{1}{5}$ ; (11)  $-\frac{1}{5}$ ; (12)  $\frac{1}{3}$ ; (13) -1;
(14) -1.

2. (1) $\frac{1}{5} e^{5t} + C$; (2) $-\frac{1}{8}(3 - 2x)^4 + C$;
(3) $-\frac{1}{2} \ln |1 - 2x| + C;$ (4) $-\frac{1}{2} (2 - 3x)^{\frac{2}{3}} + C;$
(5) $-\frac{1}{a}\cos ax-be^{\frac{x}{b}}+C;$  (6) $-2\cos\sqrt{t}+C;$
(7) $-\frac{1}{2}e^{-x^{2}}+C;$ 

(8) $\frac{1}{2}\sin(x^{2})+C;$

(9) $-\frac{1}{3}(2-3x^{2})^{\frac{1}{2}}+C;$ 

(10) $-\frac{3}{4}\ln|1-x^{4}|+C;$

(11) $\frac{1}{2} \ln (x^2 + 2x + 5) + C$; (12) $-\frac{1}{3\omega} \cos^3 (\omega t + \varphi) + C$;

(13) $\frac{1}{2\cos^2 x} + C$; (14) $\frac{3}{2}\sqrt[3]{(\sin x - \cos x)^2} + C$;

(15) $\frac{1}{11}\tan^{11}x + C$; (16) $\ln |\ln \ln x| + C$;

(17) $-\frac{1}{\arcsin x}+C;$  (18) $-\frac{10^{2\arccos x}}{2\ln 10}+C;$

402

---

部分习题参考答案与提示

(19) $-\ln \left|\cos \sqrt{1 + x^2}\right| + C;$
(21) $-\frac{1}{x\ln x}+C;$
(23) $\frac{1}{2} (\ln \tan x)^2 + C;$
(25) $\frac{t}{2} + \frac{1}{4\omega}\sin 2(\omega t + \varphi) + C;$
(27) $\frac{1}{3}\sin \frac{3x}{2} +\sin \frac{x}{2} +C;$
(29) $\frac{1}{3}\sec^3 x - \sec x + C;$
(31) $\frac{1}{2}\arcsin \frac{2x}{3} + \frac{1}{4}\sqrt{9 - 4x^2} + C;$
(33) $\frac{1}{2\sqrt{2}}\ln \left|\frac{\sqrt{2}x - 1}{\sqrt{2}x + 1}\right| + C;$
(35) $\frac{2}{3}\ln |x - 2| + \frac{1}{3}\ln |x + 1| + C;$
(37) $\arccos \frac{1}{|x|} + C;$
(39) $\sqrt{x^2 - 9} - 3\arccos \frac{3}{|x|} + C;$
(41) $\arcsin x - \frac{x}{1 + \sqrt{1 - x^2}} + C;$
(43) $\frac{1}{2}\ln (x^2 + 2x + 3) - \sqrt{2}\arctan \frac{x + 1}{\sqrt{2}} + C;$

(20) $(\arctan \sqrt{x})^2 + C$;
(22) $\ln |\tan x| + C$;
(24)  $\sin x - \frac{\sin^{3}x}{3} + C;$
(26) $\frac{1}{2}\cos x - \frac{1}{10}\cos 5x + C;$
(28) $\frac{1}{4}\sin 2x - \frac{1}{24}\sin 12x + C;$
(30) arctan  $e^{x}+C$ ;
(32) $\frac{x^2}{2} - \frac{9}{2}\ln (x^2 + 9) + C$;
(34) $\frac{1}{3}\ln \left|\frac{x - 2}{x + 1}\right| + C;$
(36) $\frac{a^2}{2}\left(\arcsin \frac{x}{a} -\frac{x}{a^2}\sqrt{a^2 - x^2}\right) + C;$
(38) $\frac{x}{\sqrt{1 + x^2}} + C;$
(40)  $\sqrt{2x}-\ln(1+\sqrt{2x})+C;$
(42) $\frac{1}{2} (\arcsin x + \ln |x + \sqrt{1 - x^2}|) + C;$
(44) $\frac{1}{2}\left[\frac{x + 1}{x^2 + 1} + \ln (x^2 + 1) + \arctan x\right] + C.$

## 习题 4-3（第 207 页）

1.  $-x\cos x+\sin x+C.$
2. $x(\ln x - 1) + C$.
3.  $x \arcsin x + \sqrt{1 - x^{2}} + C.$
4. $-\mathrm{e}^{-x}(x + 1) + C.$
5. $\frac{1}{3} x^3\ln x - \frac{1}{9} x^3 + C.$
6. $\frac{\mathrm{e}^{-x}}{2} (\sin x - \cos x) + C.$

403

---

部分习题参考答案与提示

7. $-\frac{2}{17}\mathrm{e}^{-2x}\left(\cos \frac{x}{2} + 4\sin \frac{x}{2}\right) + C.$
8. $2x \sin \frac{x}{2} + 4 \cos \frac{x}{2} + C.$
9. $\frac{1}{3} x^3\arctan x - \frac{1}{6} x^2 +\frac{1}{6}\ln (1 + x^2) + C.$
10. $-\frac{1}{2} x^{2} + x\tan x + \ln |\cos x| + C.$
11. $x^{2}\sin x + 2x\cos x - 2\sin x + C.$
12. $-\frac{\mathrm{e}^{-2t}}{2}\left(t + \frac{1}{2}\right) + C.$
13.  $x\ln^{2}x-2x\ln x+2x+C.$
14.  $-\frac{1}{4}x\cos2x+\frac{1}{8}\sin2x+C.$
15. $\frac{x^3}{6} +\frac{1}{2} x^2\sin x + x\cos x - \sin x + C.$
16. $\frac{1}{2} (x^2 - 1)\ln (x - 1) - \frac{1}{4} x^2 - \frac{1}{2} x + C.$
17. $-\frac{1}{2}\left(x^{2} - \frac{3}{2}\right)\cos 2x + \frac{x}{2}\sin 2x + C.$
18. $-\frac{1}{x} (\ln^3 x + 3\ln^2 x + 6\ln x + 6) + C.$
19. $3\mathrm{e}^{3\sqrt{x}}(\sqrt[3]{x^2} - 2\sqrt[3]{x} + 2) + C.$
20. $\frac{x}{2} (\cos \ln x + \sin \ln x) + C.$
21. $x(\arcsin x)^{2} + 2\sqrt{1 - x^{2}}\arcsin x - 2x + C.$
22. $\frac{1}{2}\mathrm{e}^{x} - \frac{1}{5}\mathrm{e}^{x}\sin 2x - \frac{1}{10}\mathrm{e}^{x}\cos 2x + C.$
23. $\frac{1}{2} x^2\left(\ln^2 x - \ln x + \frac{1}{2}\right) + C.$
24. $\frac{2}{3} (\sqrt{3x + 9} -1)\mathrm{e}^{\sqrt{3x + 9}} + C.$

习题4-4（第213页）

1. $\frac{1}{3} x^3 -\frac{3}{2} x^2 +9x - 27\ln |x + 3| + C.$

404

---

部分习题参考答案与提示

2. $\ln \left| {x - 2}\right|  + \ln \left| {x + 5}\right|  + C$ .
3. $\frac{1}{2} \ln (x^2 - 2x + 5) + \arctan \frac{x - 1}{2} + C.$
4. $\ln |x| - \frac{1}{2}\ln (x^2 + 1) + C.$
5. $\ln |x + 1| - \frac{1}{2}\ln (x^2 - x + 1) + \sqrt{3}\arctan \frac{2x - 1}{\sqrt{3}} + C.$
6. $\frac{1}{x + 1} +\frac{1}{2}\ln |x^2 -1| + C.$
7. $2\ln |x + 2| - \frac{1}{2}\ln |x + 1| - \frac{3}{2}\ln |x + 3| + C.$
8. $\frac{1}{3} x^3 +\frac{1}{2} x^2 +x + 8\ln |x| - 4\ln |x + 1| - 3\ln |x - 1| + C.$
9. $\ln |x| - \frac{1}{2}\ln |x + 1| - \frac{1}{4}\ln (x^2 + 1) - \frac{1}{2}\arctan x + C.$
10. $\frac{1}{4}\ln \left|\frac{x - 1}{x + 1}\right| - \frac{1}{2}\arctan x + C.$
11. $-\frac{1}{2}\ln \frac{x^2 + 1}{x^2 + x + 1} + \frac{\sqrt{3}}{3}\arctan \frac{2x + 1}{\sqrt{3}} + C.$
12. arctan  $x-\frac{1}{x^{2}+1}+C.$
13. $-\frac{x + 1}{x^2 + x + 1} -\frac{4}{\sqrt{3}}\arctan \frac{2x + 1}{\sqrt{3}} +C.$
14. $\frac{1}{2\sqrt{3}}\arctan \frac{2\tan x}{\sqrt{3}} +C.$
15. $\frac{1}{\sqrt{2}} \arctan \frac{\tan \frac{x}{2}}{\sqrt{2}} + C.$
16. $\frac{2}{\sqrt{3}}\arctan \frac{2\tan\frac{x}{2} + 1}{\sqrt{3}} + C.$
17. $\ln \left|1 + \tan \frac{x}{2}\right| + C.$
18. $\frac{1}{\sqrt{5}} \arctan \frac{3 \tan \frac{x}{2} + 1}{\sqrt{5}} + C.$

405

---

部分习题参考答案与提示

19. $\frac{3}{2}\sqrt[3]{(1 + x)^2} - 3\sqrt[3]{x + 1} + 3\ln \left|1 + \sqrt[3]{1 + x}\right| + C.$
20. $\frac{1}{2} x^2 -\frac{2}{3}\sqrt{x^3} +x - 4\sqrt{x} +4\ln (\sqrt{x} +1) + C.$
21. $x - 4\sqrt{x + 1} + 4\ln (\sqrt{1 + x} + 1) + C.$
22. $2\sqrt{x} - 4\sqrt[4]{x} + 4\ln (\sqrt[4]{x} + 1) + C.$
23. $\ln \left|\frac{\sqrt{1 - x} - \sqrt{1 + x}}{\sqrt{1 - x} + \sqrt{1 + x}}\right| + 2\arctan \sqrt{\frac{1 - x}{1 + x}} + C$ 或 $\ln \frac{1 - \sqrt{1 - x^2}}{|x|} - \arcsin x + C.$
24.  $-\frac{3}{2}\sqrt[3]{\frac{x+1}{x-1}}+C.$

## 习题4-5（第216页）

1. $\frac{1}{2} \ln \left| 2x + \sqrt{4x^2 - 9} \right| + C.$

2. $\frac{1}{2}\arctan \frac{x + 1}{2} + C.$

3. $\ln \left[(x - 2) + \sqrt{5 - 4x + x^2}\right] + C.$

4. $\frac{x}{2}\sqrt{2x^2 + 9} +\frac{9\sqrt{2}}{4}\ln (\sqrt{2} x + \sqrt{2x^2 + 9}) + C.$

5. $\frac{x}{2}\sqrt{3x^2 - 2} -\frac{\sqrt{3}}{3}\ln \left|\sqrt{3} x + \sqrt{3x^2 - 2}\right| + C.$

6. $\frac{\mathrm{e}^{2x}}{5} (\sin x + 2\cos x) + C.$

7. $\left(\frac{x^2}{2} - 1\right)\arcsin \frac{x}{2} + \frac{x}{4}\sqrt{4 - x^2} + C.$

8.  $\frac{x}{18(x^{2}+9)}+\frac{1}{54}\arctan\frac{x}{3}+C.$

9. $-\frac{1\cos x}{2\sin^2x} +\frac{1}{2}\ln \left|\tan \frac{x}{2}\right| + C.$

10. $-\frac{\mathrm{e}^{-2x}}{13} (2\sin 3x + 3\cos 3x) + C.$

11. $-\frac{\sin 8x}{16} +\frac{\sin 2x}{4} +C.$
12.  $x\ln^{3}x-3x\ln^{2}x+6x\ln x-6x+C.$

406

---

部分习题参考答案与提示

13. $-\frac{1}{x} - \ln \left|\frac{1 - x}{x}\right| + C.$
14.  $2\sqrt{x-1}-2\arctan\sqrt{x-1}+C.$
15. $\frac{x}{2(1 + x^2)} +\frac{1}{2}\arctan x + C.$

16. $\arccos \frac{1}{|x|} + C.$

17. $\frac{1}{9} \left( \ln |2 + 3x| + \frac{2}{2 + 3x} \right) + C.$

18.  $\frac{\cos^{5}x\sin x}{6}+\frac{5\cos^{3}x\sin x}{24}+\frac{5}{32}(2x+\sin 2x)+C.$

19. $\frac{x(x^2 - 1)\sqrt{x^2 - 2}}{4} -\frac{1}{2}\ln |x + \sqrt{x^2 - 2}| + C.$

20. $\frac{1}{\sqrt{21}}\ln \left|\frac{\sqrt{3}\tan\frac{x}{2} + \sqrt{7}}{\sqrt{3}\tan\frac{x}{2} - \sqrt{7}}\right| + C.$

21. $\frac{\sqrt{2x - 1}}{x} + 2\arctan \sqrt{2x - 1} + C.$

22. $\arcsin x + \sqrt{1 - x^2} + C.$

23. $\frac{1}{2}\ln |x^2 - 2x - 1| + \frac{3}{\sqrt{2}}\ln \left|\frac{x - 1 - \sqrt{2}}{x - 1 + \sqrt{2}}\right| + C.$

24. $-\sqrt{1 + x - x^2} +\frac{1}{2}\arcsin \frac{2x - 1}{\sqrt{5}} +C.$

25. $\frac{1}{12} x^3 -\frac{25}{16} x + \frac{125}{32}\arctan \frac{2x}{5} +C.$

## 总习题四（第216页）

1. (1) $(x^{3} - 3x^{2} + 6x - 6)\mathrm{e}^{x} + C;$ (2) $\frac{1}{2}\ln (x^2 -6x + 13) + 4\arctan \frac{x - 3}{2} +C.$

2. (1) (B); (2) (C).

3. $x^{2}\cos x - 4x\sin x - 6\cos x + C.$

4. (1) $\frac{1}{2} \ln \frac{\left| e^{x} - 1 \right|}{e^{x} + 1} + C$;
(3) $\frac{1}{6a^3}\ln \left|\frac{a^3 + x^3}{a^3 - x^3}\right| + C;$
(2) $\frac{1}{2(1 - x)^2} - \frac{1}{1 - x} + C;$
(4) $\ln |x + \sin x| + C$;

407

---

部分习题参考答案与提示

(5) $\ln x (\ln \ln x - 1) + C$;
(6) $\frac{1}{2}\arctan \sin^2 x + C$;
(7) $\frac{1}{3} \tan^3 x - \tan x + x + C$;
(8) $\frac{1}{8}\left(\frac{1}{3}\cos 6x - \frac{1}{2}\cos 4x - \cos 2x\right) + C;$
(9) $\frac{1}{4} \ln |x| - \frac{1}{24} \ln (x^6 + 4) + C$;
(10) $a\arcsin \frac{x}{a} -\sqrt{a^2 - x^2} +C;$
(11) $\ln \left|x + \frac{1}{2} +\sqrt{x(x + 1)}\right| + C;$
(12) $\frac{1}{4}x^{2}+\frac{x}{4}\sin2x+\frac{1}{8}\cos2x+C;$
(13) $\frac{1}{a^2 + b^2}\mathrm{e}^{ax}(a\cos bx + b\sin bx) + C;$
(14)  $\ln\frac{\sqrt{1+e^{x}}-1}{\sqrt{1+e^{x}}+1}+C;$
(15) $\frac{\sqrt{x^2 - 1}}{x} + C$;
(16) $\frac{1}{3a^4}\left[\frac{3x}{\sqrt{a^2 - x^2}} + \frac{x^3}{\sqrt{(a^2 - x^2)^3}}\right] + C;$
(17) $-\frac{\sqrt{(1 + x^2)^3}}{3x^3} +\frac{\sqrt{1 + x^2}}{x} +C;$
(18) $(4-2x)\cos\sqrt{x}+4\sqrt{x}\sin\sqrt{x}+C;$
(19) $x \ln (1 + x^2) - 2x + 2\arctan x + C$;
(20) $\frac{\sin x}{2\cos^2 x} - \frac{1}{2}\ln |\sec x + \tan x| + C;$
(21) $(x + 1)\arctan \sqrt{x} -\sqrt{x} +C;$
(22)  $\sqrt{2}\ln\left(\left|\csc\frac{x}{2}\right|-\left|\cot\frac{x}{2}\right|\right)+C;$
(23) $\frac{x^4}{8(1 + x^8)} + \frac{1}{8}\arctan x^4 + C;$
(24) $\frac{x^4}{4} + \ln \frac{\sqrt[4]{x^4 + 1}}{x^4 + 2} + C$;
(25) $\frac{1}{32} \ln \left| \frac{2 + x}{2 - x} \right| + \frac{1}{16} \arctan \frac{x}{2} + C$;
(26) $\frac{2}{1 + \tan\frac{x}{2}} + x + C$ 或 $\sec x + x - \tan x + C;$
(27)  $x\tan\frac{x}{2}+C;$
(28) $\mathrm{e}^{\sin x}(x - \sec x) + C$;
(29) $\ln \frac{x}{\left(\sqrt[6]{x} + 1\right)^6} + C;$
(30) $\frac{1}{1 + \mathrm{e}^x} + \ln \frac{\mathrm{e}^x}{1 + \mathrm{e}^x} + C;$
(31) $\arctan (\mathrm{e}^x -\mathrm{e}^{-x}) + C;$
(32) $\frac{x\mathrm{e}^x}{\mathrm{e}^x + 1} -\ln (1 + \mathrm{e}^x) + C;$
(33) $x\ln^2 (x + \sqrt{1 + x^2}) - 2\sqrt{1 + x^2}\ln (x + \sqrt{1 + x^2}) + 2x + C;$
(34) $\frac{x\ln x}{\sqrt{1 + x^2}} -\ln (x + \sqrt{1 + x^2}) + C;$
(35) $\frac{1}{4} (\arcsin x)^2 +\frac{x}{2}\sqrt{1 - x^2}\arcsin x - \frac{x^2}{4} +C;$
(36) $-\frac{1}{3}\sqrt{1 - x^2} (x^2 + 2)\arccos x - \frac{1}{9} x(x^2 + 6) + C;$

408

---

部分习题参考答案与提示

(37) $-\ln |\csc x + 1| + C;$
(38) $\ln |\tan x| - \frac{1}{2\sin^2x} + C;$
(39) $\frac{1}{3}\ln (2 + \cos x) - \frac{1}{2}\ln (1 + \cos x) + \frac{1}{6}\ln (1 - \cos x) + C;$
(40) $\frac{1}{2} (\sin x - \cos x) - \frac{1}{2\sqrt{2}}\ln \left|\frac{\tan\frac{x}{2} - 1 + \sqrt{2}}{\tan\frac{x}{2} - 1 - \sqrt{2}}\right| + C.$

## 第五章

## 习题 5-1（第 230 页）

\* 1. $\frac{1}{3} (b^3 - a^3) + b - a$.

\*2. (1) $\frac{1}{2} (b^2 - a^2)$; (2) e-1.

3. 略.

4. (1)  $\frac{1}{2}t^{2}$ ; (2) 21; (3)  $\frac{5}{2}$ ; (4)  $\frac{9\pi}{2}$ .

5. a=0, b=1.

6. 略.

7. $\ln 2 \approx 0.6931$.

8. (1) 6; (2) -2; (3) -3; (4) 5.

9. 略.

10. (1) $6 \leqslant \int_{1}^{4} (x^{2} + 1) \, \mathrm{d}x \leqslant 51$; (2) $\pi \leqslant \int_{\frac{\pi}{4}}^{\frac{5}{4}\pi} (1 + \sin^{2} x) \, \mathrm{d}x \leqslant 2\pi$;
(3) $\frac{\pi}{9} \leqslant \int_{\frac{1}{\sqrt{3}}}^{\sqrt{3}} x \arctan x \, \mathrm{d}x \leqslant \frac{2}{3} \pi;$ (4) $-2 \mathrm{e}^{2} \leqslant \int_{2}^{0} \mathrm{e}^{x^{2} - x} \, \mathrm{d}x \leqslant -2 \mathrm{e}^{-\frac{1}{4}}.$

11. 提示: 设  $\int_{0}^{1}f(x)\mathrm{d}x=a$  , 有  $\int_{0}^{1}[f(x)-a]^{2}\mathrm{d}x\geqslant0$

12. 略.

13. (1) $\int_{0}^{1} x^{2} \mathrm{~d} x$ 较大； (2) $\int_{1}^{2} x^{3} \mathrm{~d} x$ 较大； (3) $\int_{1}^{2} \ln x \mathrm{~d} x$ 较大；

409

---

部分习题参考答案与提示

(4) $\int_{0}^{1}xdx$ 较大；(5) $\int_{0}^{1}e^{x}dx$ 较大.

## 习题5-2（第238页）

1. $0, \frac{\sqrt{2}}{2}$.

2. $\cot t$.

3.  $\frac{\cos x}{\sin x-1}.$

4. 当 $x = 0$ 时.

5. (1) $2x\sqrt{1 + x^4}$; (2) $\frac{3x^2}{\sqrt{1 + x^{12}}} - \frac{2x}{\sqrt{1 + x^8}}$; (3) $(\sin x - \cos x) \cdot \cos (\pi \sin^2 x)$.

6.  $\frac{1}{\sqrt{2}}$ .

7. $-\frac{5}{8}$.

8. (C).

9. (1) $a\left(a^{2} - \frac{a}{2} + 1\right)$; (2) $\frac{21}{8}$; (3) $\frac{271}{6}$; (4) $\frac{\pi}{6}$; (5) $\frac{\pi}{3}$; (6) $\frac{\pi}{3a}$; (7) $\frac{\pi}{6}$; (8) $\frac{\pi}{4} + 1$; (9) $-1$; (10) $1 - \frac{\pi}{4}$; (11) 4; (12) $\frac{8}{3}$.

10. 略.

11. 提示: 应用三角学中的积化和差公式.

12. (1) 1; (2) 2.

13. $\Phi(x) = \begin{cases} \frac{1}{3} x^3, & x \in [0,1), \\ \frac{1}{2} x^2 - \frac{1}{6}, & x \in [1,2], \end{cases}$ $\Phi(x)$ 在(0,2)内连续.

14. $\Phi (x) = \left\{ \begin{array}{ll}0, & x <   0,\\ \frac{1}{2} (1 - \cos x), & 0\leqslant x\leqslant \pi ,\\ 1, & x > \pi . \end{array} \right.$

15. 略.

16.（1）略；（2） $x = (-1)^{k}\sqrt{2k}$ （ $k\in \mathbf{N}_{+}$ ）.

17. 1.

410

---

部分习题参考答案与提示

## 习题 5-3（第 248 页）

1. (1) 0; (2) $\frac{51}{512}$; (3) $\frac{1}{4}$; (4) $\pi - \frac{4}{3}$; (5) $\frac{\pi}{6} - \frac{\sqrt{3}}{8}$;

(6) $\frac{\pi}{2}$; (7) $\sqrt{2} (\pi + 2)$; (8) $1 - \frac{\pi}{4}$; (9) $\frac{\pi}{16} a^4$;
(10) $\sqrt{2} - \frac{2\sqrt{3}}{3}$; (11) $\frac{1}{6}$; (12) $2 + 2\ln \frac{2}{3}$; (13) $1 - 2\ln 2$;
(14) $(\sqrt{3} - 1)a$; (15) $1 - \mathrm{e}^{-\frac{1}{2}}$; (16) $2(\sqrt{3} - 1)$; (17) $\frac{\pi}{2}$;
(18) $\frac{\pi}{4} + \frac{1}{2}$; (19) 0; (20) $\frac{3}{2}\pi$; (21) $\frac{\pi^3}{324}$; (22) 0;
(23) $\frac{2}{3}$ ; (24) $\frac{4}{3}$ ; (25) $2\sqrt{2}$ ; (26)4.

2—6. 略.

7.  $\frac{e+1}{2}$ .

8. (1) $1 - \frac{2}{\mathrm{e}}$; (2) $\frac{1}{4} (\mathrm{e}^2 + 1)$; (3) $-\frac{2\pi}{\omega^2}$; (4) $\left(\frac{1}{4} - \frac{\sqrt{3}}{9}\right)\pi + \frac{1}{2}\ln \frac{3}{2}$;

(5)  $4(2\ln 2-1)$ ; (6)  $\frac{\pi}{4}-\frac{1}{2}$ ; (7)  $\frac{1}{5}(e^{\pi}-2)$ ; (8)  $2-\frac{3}{4\ln 2}$ ;
(9) $\frac{\pi^3}{6} - \frac{\pi}{4}$; (10) $\frac{1}{2} (\mathrm{e}\sin 1 - \mathrm{e}\cos 1 + 1)$; (11) $2\left(1 - \frac{1}{\mathrm{e}}\right)$;
(12) $\left\{\begin{aligned}\frac{1\cdot3\cdot5\cdot\cdots\cdot m}{2\cdot4\cdot6\cdot\cdots\cdot(m+1)}\cdot\frac{\pi}{2},&m\text{为奇数,}\\ \frac{2\cdot4\cdot6\cdot\cdots\cdot m}{1\cdot3\cdot5\cdot\cdots\cdot(m+1)},&m\text{为偶数;}\end{aligned}\right.$
(13) $J_{m}=\left\{\begin{aligned}\frac{1\cdot3\cdot5\cdot\cdots\cdot(m-1)}{2\cdot4\cdot6\cdot\cdots\cdot m}\cdot\frac{\pi^{2}}{2},&m \text{为偶数,}\\ \frac{2\cdot4\cdot6\cdot\cdots\cdot(m-1)}{1\cdot3\cdot5\cdot\cdots\cdot m}\pi,&m \text{为大于1的奇数,}\end{aligned}\right.$ 
$J_{1}=\pi.$

## 习题 5-4（第 255 页）

1. (1) $\frac{1}{3}$; (2) 发散; (3) $\frac{1}{a}$; (4) $\frac{\pi}{4}$; (5) $\frac{\omega}{p^2 + \omega^2}$;

411

---

部分习题参考答案与提示

(6) $\pi$; (7) 1; (8) 发散; (9) $\frac{8}{3}$; (10) $\frac{\pi}{2}$.

2. $\frac{1}{4}\ln 3$.

3. 当 $k > 1$ 时, 收敛于 $\frac{1}{(k - 1)(\ln 2)^{k - 1}}$; 当 $k \leqslant 1$ 时, 发散; 当 $k = 1 - \frac{1}{\ln \ln 2}$ 时, 取得最小值.

4.  $n!$ .

5. -1.

## \*习题5-5（第263页）

1.（1）收敛；（2）收敛；（3）收敛；（4）发散；

(5) 收敛； (6) 发散； (7) 收敛； (8) 收敛.

2. 略.

3. (1) $\frac{1}{n}\Gamma\left(\frac{1}{n}\right), n > 0$; (2) $\Gamma(p + 1), p > -1$; (3) $\frac{1}{|n|}\Gamma\left(\frac{m + 1}{n}\right), \frac{m + 1}{n} > 0$.

4—5. 略.

## 总习题五（第263页）

1.（1）必要，充分；（2）充分必要； $^{*}$ （3）收敛；（4）不一定；（5） $xf(-x^{2})$ .

2. (1) (B); (2) (A).

3.（1）表示曲线  $y=f(x)$ ,  $y=g(x)$  和直线 x=a, x=b 所围图形的面积；

(2) 表示曲线  $y=f(x)$  和直线 y=0, x=a, x=b 所围曲边梯形绕 x 轴旋转所得旋转体的体积；

(3) 表示 $\left[t_{1},t_{2}\right]$ 这段时间内流入水池的水量；

(4) 表示 $\left[T_{1},T_{2}\right]$ 这段时期内该国人口增加的数量；

(5) 表示该公司经营该种产品自第 1 001 件至第 2 000 件所得利润.

\*4. (1) $\frac{2}{3}(2\sqrt{2}-1)$; (2) $\frac{1}{p+1}$.

5. (1) $af(a)$; (2) $\frac{\pi^2}{4}$.

6—7. 略.

8. 提示: $1 - x^{p} < \frac{1}{1 + x^{p}} < 1$.

412

---

部分习题参考答案与提示

9. 提示:(1) 对任意实数 $t, \int_{a}^{b} f^{2}(x) \mathrm{d}x + 2t \int_{a}^{b} f(x) g(x) \mathrm{d}x + t^{2} \int_{a}^{b} g^{2}(x) \mathrm{d}x \geqslant 0;$

(2) 利用柯西-施瓦茨不等式.

10. 提示: 利用柯西-施瓦茨不等式.

11. (1) $\frac{\pi}{2}$; (2) $\frac{\pi}{8} \ln 2$, 提示: 令 $x = \frac{\pi}{4} - u$; (3) $\frac{\pi}{4}$; (4) $2(\sqrt{2} - 1)$;

(5) $\frac{\pi}{2\sqrt{2}}$; (6) $\frac{\pi}{2}$; (7) $\frac{\pi^2}{2} + 2\pi - 4$; (8) $\mathrm{e}^{-2}\left(\frac{\pi}{2} - \arctan \mathrm{e}^{-1}\right)$;

(9) $\frac{\pi}{2} + \ln (2 + \sqrt{3})$; (10) $\begin{cases} \frac{1}{3} x^3 - \frac{2}{3}, & \text{当 } x < -1, \\ x, & \text{当 } -1 \leqslant x \leqslant 1, \\ \frac{1}{4} x^4 + \frac{3}{4}, & \text{当 } x > 1. \end{cases}$

12—13. 略.

14.  $1+\ln(1+e^{-1})$ .

15—\*17. 略.

\*18.（1）收敛；（2）收敛；（3）收敛，提示:先分部积分，再判别；（4）收敛.

\*19. (1) $-\frac{\pi}{2} \ln 2$，提示:$\int_{\frac{\pi}{4}}^{\frac{\pi}{2}} \ln \sin x \, \mathrm{d}x = \int_{0}^{\frac{\pi}{4}} \ln \cos x \, \mathrm{d}x$；

(2) $\frac{\pi}{4}$ , 提示: 令  $x=\frac{1}{t}$ .

## 第六章

## 习题 6-2 (第 279 页)

1. (1) $\frac{1}{6}$; (2) 1; (3) $\frac{32}{3}$; (4) $\frac{32}{3}$.

2. (1) $2\pi + \frac{4}{3}, 6\pi - \frac{4}{3}$; (2) $\frac{3}{2} - \ln 2$; (3) $e + \frac{1}{e} - 2$; (4) $b - a$.

3. $\frac{9}{4}$.

4. $\frac{16}{3} p^2$.

413

---

部分习题参考答案与提示

5. $a = \frac{4}{3}, b = \frac{5}{12}$.

6. (1) $\pi a^2$; (2) $\frac{3}{8}\pi a^2$; (3) $18\pi a^2$.

7. $3\pi a^{2}$

8. $\frac{a^2}{4} (\mathrm{e}^{2\pi} - \mathrm{e}^{-2\pi})$

9. (1) $\frac{5}{4}\pi$; (2) $\frac{\pi}{6} + \frac{1 - \sqrt{3}}{2}$.

10.  $\frac{e}{2}$ .

11.  $\xi=\sqrt{e}.$

12. 当 $p = -\frac{4}{5}, q = 3$ 时, $A$ 达到最大值 $\frac{225}{32}$.

13.  $\frac{128}{7}\pi,\frac{64}{5}\pi.$

14.  $\frac{32}{105}\pi a^{3}.$

15. 略.

16. (1) $\frac{3}{10}\pi$; (2) $\frac{\pi^3}{4} - 2\pi$; (3) $160\pi^2$; (4) $7\pi^2 a^3$.

17. $2\pi^2 a^2 b$.

18.  $\frac{1}{6}\pi h\left[2(ab+AB)+aB+bA\right].$

19.  $\frac{4\sqrt{3}}{3}R^{3}.$

20. 略.

21. (1) $2\pi^2$; (2) $6\pi^2$.

22. (1) $V_{1} = \frac{4\pi}{5}(32 - a^{5}), V_{2} = \pi a^{4}$; (2) 当 $a = 1$ 时, $V_{1} + V_{2}$ 取得最大值 $\frac{129}{5}\pi$.

23. $1 + \frac{1}{2}\ln \frac{3}{2}$.

24. $\frac{8}{9}\left[\left(\frac{5}{2}\right)^{\frac{3}{2}} - 1\right].$

25. $\frac{y}{2p}\sqrt{p^2 + y^2} +\frac{p}{2}\ln \frac{y + \sqrt{p^2 + y^2}}{p}.$

414

---

部分习题参考答案与提示

26. 6a.
27. $\frac{a}{2}\pi^2$.
28. $\left(\left(\frac{2}{3}\pi -\frac{\sqrt{3}}{2}\right)a,\frac{3}{2} a\right)$.
29.  $\frac{\sqrt{1+a^{2}}}{a}(e^{a\varphi}-1)$ .
30.  $\ln \frac{3}{2} + \frac{5}{12}.$

## 习题6-3（第286页）

1. $0.18k \mathrm{~J}$.
2. ${800\pi }\ln 2\mathrm{\;J}$ .
3.（1）略；（2） $9.72 \times 10^{5} \mathrm{~kJ}$.
4. $\frac{27}{7}kc^{\frac{2}{3}}a^{\frac{7}{3}}$ （其中 $k$ 为比例常数）.
5. $(\sqrt{2}-1)$  cm.
6. 57 697.5 kJ.
7. 略.
8. ${14373}\mathrm{{kN}}$ .
9. $1.65 \mathrm{~N}$.
10. 取 $y$ 轴通过细直棒, 则 $F_{y} = Gm\mu \left(\frac{1}{a} - \frac{1}{\sqrt{a^{2} + l^{2}}}\right), F_{x} = -\frac{Gm\mu l}{a\sqrt{a^{2} + l^{2}}}.$
11. 引力的大小为 $\frac{2Gm\mu}{R}\sin\frac{\varphi}{2}$ ，方向为M指向圆弧的中点.

## 总习题六（第287页）

1. (1)  $\frac{37}{12}$ ; (2)  $2\sqrt{3}-\frac{4}{3}$ .
2. (1) (A); (2) (D); (3) (B).
3. $\frac{5}{4} \mathrm{~m}$.
4. $\frac{\pi - 1}{4} a^2$.

415

---

部分习题参考答案与提示

5. $x = \frac{3}{4}\sqrt{\frac{y}{2}}$ 或 $y = \frac{32}{9} x^2 (x\geqslant 0)$
6. $a = -\frac{5}{3}, b = 2, c = 0.$
7. (1) $\frac{1}{2} e - 1$; (2) $\frac{\pi}{6}(5e^2 - 12e + 3)$.
8.  $\frac{1}{e^{2}}$ .
9. $\frac{512}{7}\pi$.
10. $4\pi^2$
11. $\sqrt{6} + \ln (\sqrt{2} + \sqrt{3})$.
12. $\frac{4}{3}\pi r^4 g$.
13.  $\frac{1}{2}\rho gab(2h+b\sin\alpha)$ .
14. $F_{x} = \frac{3}{5} Ga^{2}, F_{y} = \frac{3}{5} Ga^{2}$ (G为引力常量).
15. (1) $\sqrt{1 + r + r^2} a \mathrm{~m}$; (2) $\frac{1}{\sqrt{1 - r}} a \mathrm{~m}$.

## 第七章

## 习题 7-1 (第 293 页)

1.（1）一阶；（2）二阶；（3）三阶；（4）一阶；（5）二阶；（6）一阶.
2.（1）是；（2）是；（3）不是；（4）是.
3. 略.
4. (1) $y^{2} - x^{2} = 25$; (2) $y = xe^{2x}$; (3) $y = -\cos x$.
5. (1) $y' = x^2$; (2) $yy' + 2x = 0$; (3) $x^2(1 + y'^2) = a^2, y|_{x=a} = 0$.
6.  $\frac{dp}{dT}=k\frac{p}{T^{2}}$ , k为比例系数.
7. 6 h.

416

---

部分习题参考答案与提示

## 习题7-2（第300页）

1. (1) $y = \mathrm{e}^{Cx}$; (2) $y = \frac{1}{2} x^2 + \frac{1}{5} x^3 + C$; (3) $\arcsin y = \arcsin x + C$;

(4) $\frac{1}{y} = a\ln |x + a - 1| + C;\quad (5)\tan x\tan y = C;\quad (6)10^{-y} + 10^{x} = C;$

(7) $(\mathrm{e}^{x} + 1)(\mathrm{e}^{y} - 1) = C$ (8) $\sin x\sin y = C$ (9) $3x^{4} + 4(y + 1)^{3} = C$

(10) $(x-4)y^{4}=Cx.$

2. (1)  $e^{y}=\frac{1}{2}(e^{2x}+1)$ ; (2)  $\cos x-\sqrt{2}\cos y=0$ ; (3)  $\ln y=\tan\frac{x}{2}$ ;

(4) $(1+e^{x})\sec y=2\sqrt{2}$ ; (5) $x^{2}y=4$ ; (6) $\rho+\frac{1}{\rho}=\frac{5}{3\sin\theta}$ ;

(7) $y = \pm \left( \sqrt{a^2 - x^2} + a \ln \frac{a - \sqrt{a^2 - x^2}}{x} \right).$

3.  $t = -0.0305 h^{\frac{5}{2}} + 9.64$ , 水流完所需的时间约为 10 s.
4.  $v=\sqrt{72\ 500}\approx269.3\ (cm/s)$ .
5.  $R = R_{0} e^{-0.000433t}$ ，时间以年为单位.
6. xy = 6.
7. 取 $O$ 为原点, 河岸朝顺水方向为 $x$ 轴, $y$ 轴指向对岸, 则所求航线为

$$
x = \frac {k}{a} \left(\frac {h}{2} y ^ {2} - \frac {1}{3} y ^ {3}\right).
$$

## 习题 7-3（第 306 页）

1. (1) $y + \sqrt{y^2 - x^2} = Cx^2 (x > 0), y - \sqrt{y^2 - x^2} = C (x < 0)$;

(2)  $\ln \frac{y}{x} = Cx + 1;$  (3)  $y^{2} = x^{2}(2\ln |x| + C)$ ;
(4) $x^{3} - 2y^{3} = Cx$; (5) $x^{2} = C\sin^{3}\frac{y}{x}$; (6) $x + 2ye^{\frac{x}{y}} = C$.

2. (1) $y^{3} = y^{2} - x^{2}$; (2) $y^{2} = 2x^{2} (\ln x + 2)$; (3) $\frac{x + y}{x^{2} + y^{2}} = 1$; (4) $\sin \frac{y}{x} = \ln x + \frac{\sqrt{2}}{2}$.

3. $y = x(1 - 4\ln x)$.

\*4. (1) $(4y - x - 3)(y + 2x - 3)^{2} = C$; (2) $\ln [4y^{2} + (x - 1)^{2}] + \arctan \frac{2y}{x - 1} = C$;
(3) $(y-x+1)^{2}(y+x-1)^{5}=C$ ; (4) $x+3y+2\ln|x+y-2|=C.$

417

---

部分习题参考答案与提示

## 习题 7-4 (第 312 页)

1. (1) $y = \mathrm{e}^{-x}(x + C)$; (2) $y = \frac{1}{3} x^2 + \frac{3}{2} x + 2 + \frac{C}{x}$;
(3) $y = (x + C)e^{-\sin x}$; (4) $y = C\cos x - 2\cos^2 x$;
(5) $y = \frac{\sin x + C}{x^2 - 1}$; (6) $3\rho = 2 + Ce^{-3\theta}$;
(7) $y = 2 + C\mathrm{e}^{-x^2}$; (8) $2x\ln y = \ln^2 y + C$;
(9) $y = (x - 2)^3 + C(x - 2)$; (10) $x = Cy^3 + \frac{1}{2} y^2$.
2. (1) $y = \frac{x}{\cos x}$; (2) $y = \frac{\pi - 1 - \cos x}{x}$;
(3)  $y \sin x + 5e^{\cos x} = 1;$ 

(4)  $y = \frac{2}{3}(4 - e^{-3x})$ ;
(5) $2y = x^{3} - x^{3}\mathrm{e}^{x - 2 - 1}$; (6) $y = \frac{\sqrt{1 + x^2}}{x}\ln \frac{x + \sqrt{1 + x^2}}{1 + \sqrt{2}}.$

3.  $y=2(e^{x}-x-1)$ .

4.  $v=\frac{k_{1}}{k_{2}}t-\frac{k_{1}m}{k_{2}^{2}}\left(1-\mathrm{e}^{-\frac{k_{2}}{m}t}\right)$ .

5.  $i=e^{-5t}+\sqrt{2}\sin\left(5t-\frac{\pi}{4}\right)$  A.

6. $\ln |x| + \int \frac{g(v)\mathrm{d}v}{v[f(v) - g(v)]} = C$ ，求出后将 $v = xy$ 代回，得通解

7. (1) $y = -x + \tan (x + C)$; (2) $(x - y)^2 = -2x + C$; (3) $y = \frac{1}{x} e^{Cx}$;
(4) $y = 1 - \sin x - \frac{1}{x + C}$; (5) $2x^{2}y^{2}\ln |y| - 2xy - 1 = Cx^{2}y^{2}$.

\*8. (1) $\frac{1}{y} = -\sin x + Ce^x$; (2) $\frac{3}{2} x^2 + \ln \left| 1 + \frac{3}{y} \right| = C$; (3) $\frac{1}{y^3} = Ce^x - 1 - 2x$;
(4) $\frac{1}{y^4} = -x + \frac{1}{4} + C\mathrm{e}^{-4x}$; (5) $\frac{x^2}{y^2} = -\frac{2}{3} x^3\left(\frac{2}{3} + \ln x\right) + C.$

## 习题 7-5 (第 321 页)

1. (1) $y = \frac{1}{6} x^3 - \sin x + C_1 x + C_2$;

(2)  $y = (x - 3)e^{x} + C_{1}x^{2} + C_{2}x + C_{3};$

418

---

部分习题参考答案与提示

(3) $y = x \arctan x - \frac{1}{2} \ln (1 + x^2) + C_1 x + C_2$;
(4)  $y = -\ln \left| \cos \left( x + C_{1} \right) \right| + C_{2}$ ;
(5) $y = C_{1} \mathrm{e}^{x} - \frac{1}{2} x^{2} - x + C_{2}$;
(6) $y = C_{1} \ln |x| + C_{2}$;
(7) $y^{3}=C_{1}x+C_{2};$
(8) $C_{1}y^{2}-1=(C_{1}x+C_{2})^{2};$
(9) $x + C_{2} = \pm \left[\frac{2}{3} (\sqrt{y} +C_{1})^{\frac{3}{2}} - 2C_{1}\sqrt{\sqrt{y} + C_{1}}\right];$
(10)  $y = \arcsin(C_{2}e^{x}) + C_{1}.$

2.  $f(x)=2\ln \sec\left(\frac{x}{2}+\frac{\pi}{4}\right)+1-\ln 2.$

3. (1) $y = \sqrt{2x - x^2}$; (2) $y = -\frac{1}{a}\ln(ax + 1)$;

(3) $y = \frac{1}{a^3} e^{ax} - \frac{e^a}{2a} x^2 + \frac{e^a}{a^2} (a-1)x + \frac{e^a}{2a^3} (2a-a^2-2)$;
(4)  $y=\ln \sec x;$  (5)  $y=\left(\frac{1}{2}x+1\right)^{4};$  (6)  $y=\ln\left(e^{x}+e^{-x}\right)-\ln2.$

4. $y = \frac{x^3}{6} + \frac{x}{2} + 1$.

5. $s = \frac{mg}{c}\left(t + \frac{m}{c}\mathrm{e}^{-\frac{c}{m} t} - \frac{m}{c}\right)$.

## 习题7-6（第329页）

1.（1）线性无关；（2）线性相关；（3）线性相关；（4）线性无关；
(5) 线性无关；(6) 线性无关；(7) 线性相关；(8) 线性无关；
(9) 线性无关；(10) 线性无关.

2. $y = C_{1}\cos \omega x + C_{2}\sin \omega x.$

3. $y = (C_{1} + C_{2}x)\mathrm{e}^{x^{2}}$

4. 略.

\* 5. $y = C_1 \mathrm{e}^x + C_2 (2x + 1)$.

\* 6. $y = C_{1}x + C_{2}x^{2} + x^{3}$.

\*7. $y = C_{1}\cos x + C_{2}\sin x + x\sin x + \cos x\ln |\cos x|$.

\* 8. $y = C_{1}x + C_{2}x\ln |x| + \frac{1}{2} x\ln^{2} |x|$.

419

---

部分习题参考答案与提示

## 习题 7-7 (第 338 页)

1. (B).

2. (1) $y = C_{1} \mathrm{e}^{x} + C_{2} \mathrm{e}^{-2x}$;
(2) $y = C_{1} + C_{2}\mathrm{e}^{4x}$;
(3) $y = C_{1}\cos x + C_{2}\sin x;$
(4) $y = \mathrm{e}^{-3x}(C_1\cos 2x + C_2\sin 2x)$;
(5) $x = (C_1 + C_2t)\mathrm{e}^{\frac{5}{2} t}$;
(6) $y = \mathrm{e}^{2x}(C_1\cos x + C_2\sin x)$;
(7) $y = C_{1}e^{x} + C_{2}e^{-x} + C_{3}\cos x + C_{4}\sin x;$
(8) $y = (C_1 + C_2x)\cos x + (C_3 + C_4x)\sin x;$
(9) $y = C_{1} + C_{2}x + (C_{3} + C_{4}x)e^{x}$;
(10) $y = C_{1} \mathrm{e}^{2x} + C_{2} \mathrm{e}^{-2x} + C_{3} \cos 3x + C_{4} \sin 3x.$

3. (1) $y = 4\mathrm{e}^{x} + 2\mathrm{e}^{3x}$;
(2) $y = (2 + x)\mathrm{e}^{-\frac{x}{2}}$;
(3) $y = \mathrm{e}^{-x} - \mathrm{e}^{4x}$;
(4)  $y = 3e^{-2x} \sin 5x;$
(5) $y = 2\cos 5x + \sin 5x$;
(6) $y = \mathrm{e}^{2x}\sin 3x.$
4. $x = \frac{v_0}{\sqrt{k_2^2 + 4k_1}} (1 - \mathrm{e}^{-\sqrt{k_2^2 + 4k_1}t})\mathrm{e}^{(-\frac{k_2}{2} +\frac{\sqrt{k_2^2 + 4k_1}}{2})t}.$
5. $u_{C}(t) = \frac{10}{9} (19\mathrm{e}^{-10^{3}t} - \mathrm{e}^{-1.9\times 10^{4}t})\mathrm{V},i(t) = \frac{19}{18}\times 10^{-2}(-\mathrm{e}^{-10^{3}t} + \mathrm{e}^{-1.9\times 10^{4}t})$ A.
6. 195 kg.

## 习题 7-8（第 346 页）

1. (1) $y = C_{1} \mathrm{e}^{\frac{x}{2}} + C_{2} \mathrm{e}^{-x} + \mathrm{e}^{x}$;

(2) $y = C_{1}\cos ax + C_{2}\sin ax + \frac{\mathrm{e}^{x}}{1 + a^{2}}$;
(3) $y = C_{1} + C_{2}\mathrm{e}^{-\frac{5}{2} x} + \frac{1}{3} x^{3} - \frac{3}{5} x^{2} + \frac{7}{25} x;$
(4) $y = C_{1} \mathrm{e}^{-x} + C_{2} \mathrm{e}^{-2x} + \left(\frac{3}{2} x^{2} - 3x\right) \mathrm{e}^{-x}$;
(5) $y = \mathrm{e}^{x}(C_{1}\cos 2x + C_{2}\sin 2x) - \frac{1}{4} x\mathrm{e}^{x}\cos 2x;$
(6) $y = (C_1 + C_2x)\mathrm{e}^{3x} + \frac{x^2}{2}\left(\frac{1}{3} x + 1\right)\mathrm{e}^{3x};$
(7) $y = C_{1} \mathrm{e}^{-x} + C_{2} \mathrm{e}^{-4x} + \frac{11}{8} - \frac{1}{2} x;$
(8) $y = C_{1}\cos 2x + C_{2}\sin 2x + \frac{1}{3} x\cos x + \frac{2}{9}\sin x;$

420

---

部分习题参考答案与提示

(9) $y = C_{1}\cos x + C_{2}\sin x + \frac{\mathrm{e}^{x}}{2} +\frac{x}{2}\sin x;$

(10) $y = C_{1}e^{x} + C_{2}e^{-x} - \frac{1}{2} + \frac{1}{10}\cos 2x$, 提示: $\sin^2 x = \frac{1}{2}(1 - \cos 2x)$.

2. (1) $y = -\cos x - \frac{1}{3}\sin x + \frac{1}{3}\sin 2x$;

(2) $y = -5\mathrm{e}^{x} + \frac{7}{2}\mathrm{e}^{2x} + \frac{5}{2};$

(3) $y = \frac{1}{2} (\mathrm{e}^{9x} + \mathrm{e}^x) - \frac{1}{7}\mathrm{e}^{2x}$;

(4) $y = e^{x} - e^{-x} + e^{x}(x^{2} - x)$;

(5) $y = \frac{11}{16} + \frac{5}{16}\mathrm{e}^{4x} - \frac{5}{4} x.$

3. $m = -2, n = 1, y = -x\mathrm{e}^{x} + x + 2.$

4. 取炮口为原点, 炮弹前进的水平方向为 x 轴, 铅直向上为 y 轴建立直角坐标系, 弹道曲线为

$$
\left\{ \begin{array}{l} x = v _ {0} \cos \alpha \cdot t, \\ y = v _ {0} \sin \alpha \cdot t - \frac {1}{2} g t ^ {2}. \end{array} \right.
$$

5.  $u_{c}(t)=20\left\{1-\mathrm{e}^{-5\times10^{3}t}\left[\cos(5\times10^{3}t)+\sin(5\times10^{3}t)\right]\right\}$  V,

$$
i (t) = 4 \times 1 0 ^ {- 2} \mathrm{e} ^ {- 5 \times 1 0 ^ {3} t} \sin (5 \times 1 0 ^ {3} t) \mathrm{A}.
$$

提示:电路方程参见第六节例2.

6.  $\varphi(x)=\frac{1}{2}(\cos x+\sin x+\mathrm{e}^{x})$ .

## \*习题7-9（第348页）

1. $y = C_{1}x + \frac{C_{2}}{x}$.
2.  $y = x(C_{1} + C_{2} \ln |x|) + x \ln^{2} |x|$ .
3. $y = C_{1}x + C_{2}x\ln |x| + C_{3}x^{-2}$
4. $y = C_{1}x + C_{2}x^{2} + \frac{1}{2} (\ln^{2}x + \ln x) + \frac{1}{4}$.
5. $y = C_{1}x^{2} + C_{2}x^{-2} + \frac{1}{5} x^{3}$

6. $y = x[C_{1}\cos (\sqrt{3}\ln x) + C_{2}\sin (\sqrt{3}\ln x)] + \frac{1}{2} x\sin (\ln x).$

421

---

部分习题参考答案与提示

7. $y = C_{1}x^{2} + C_{2}x^{2}\ln x + x + \frac{1}{6} x^{2}\ln^{3}x.$
8. $y = C_{1}x + x \left[ C_{2}\cos(\ln x) + C_{3}\sin(\ln x) \right] + \frac{1}{2} x^{2} (\ln x - 2) + 3x \ln x.$

## \*习题7-10（第351页）

1. (1) $\left\{ \begin{array}{l} y = C_1 e^x + C_2 e^{-x}, \\ z = C_1 e^x - C_2 e^{-x}; \end{array} \right.$

(2) $\left\{ \begin{array}{l} x = C_1 \mathrm{e}^t + C_2 \mathrm{e}^{-t} + C_3 \cos t + C_4 \sin t, \\ y = C_1 \mathrm{e}^t + C_2 \mathrm{e}^{-t} - C_3 \cos t - C_4 \sin t; \end{array} \right.$

(3) $\left\{ \begin{array}{l}x = 3 + C_1\cos t + C_2\sin t,\\ y = -C_1\sin t + C_2\cos t; \end{array} \right.$

(4) $\left\{ \begin{array}{l}x = C_1\mathrm{e}^{(-1 + \sqrt{15})t} + C_2\mathrm{e}^{(-1 - \sqrt{15})t} + \frac{2}{11}\mathrm{e}^t +\frac{1}{6}\mathrm{e}^{2t},\\ y = (-4 - \sqrt{15})C_1\mathrm{e}^{(-1 + \sqrt{15})t} - (4 - \sqrt{15})C_2\mathrm{e}^{(-1 - \sqrt{15})t} - \frac{\mathrm{e}^t}{11} -\frac{7}{6}\mathrm{e}^{2t}; \end{array} \right.$

(5) $\left\{ \begin{array}{l} x = \frac{C_1 - 3C_2}{5}\sin t - \frac{3C_1 + C_2}{5}\cos t - t^2 + t + 3, \\ y = C_1\cos t + C_2\sin t + 2t^2 - 3t - 4; \end{array} \right.$

(6) $\left\{ \begin{array}{l}x = C_1\mathrm{e}^{-5t} + C_2\mathrm{e}^{-\frac{t}{3}} + \frac{8\sin t + \cos t}{65},\\ y = -\frac{4}{3} C_1\mathrm{e}^{-5t} + C_2\mathrm{e}^{-\frac{t}{3}} + \frac{61\sin t - 33\cos t}{130}. \end{array} \right.$

2. (1)  $\left\{\begin{aligned}x&=\sin t,\\ y&=\cos t;\end{aligned}\right.$  (2)  $\left\{\begin{aligned}x&=\cos t,\\ y&=\sin t;\end{aligned}\right.$  (3)  $\left\{\begin{aligned}x&=e^{t},\\ y&=4e^{t};\end{aligned}\right.$

(4) $\left\{\begin{aligned}x=2\cos t-4\sin t-\frac{1}{2}\mathrm{e}^{t},\\ y=14\sin t-2\cos t+2\mathrm{e}^{t};\end{aligned}\right.$

(5) $\left\{ \begin{array}{l}x = 4\cos t + 3\sin t - 2\mathrm{e}^{-2t} - 2\mathrm{e}^{-t}\sin t,\\ y = \sin t - 2\cos t + 2\mathrm{e}^{-t}\cos t; \end{array} \right.$

(6) $\left\{ \begin{array}{l} x = \frac{12}{17} \mathrm{e}^{-\frac{7}{5} t} + \frac{5}{17} \mathrm{e}^{2t} + \frac{3}{7} t - \frac{1}{49}, \\ y = \frac{18}{17} \mathrm{e}^{-\frac{7}{5} t} - \frac{1}{17} \mathrm{e}^{2t} + \frac{1}{2} \mathrm{e}^{-t} + \frac{1}{7} t - \frac{26}{49}. \end{array} \right.$

422

---

部分习题参考答案与提示

## 总习题七（第352页）

1. (1) 3; (2) $y = \mathrm{e}^{-\int P(x)\mathrm{d}x}\left(\int Q(x)\mathrm{e}^{\int P(x)\mathrm{d}x}\mathrm{d}x + C\right)$;
(3) $y' = f(x, y), y \mid_{x = x_0} = 0; \quad (4) y = C_1(x - 1) + C_2(x^2 - 1) + 1.$
2. (1) (B); (2) (B).
3. (1) $y^{2}(y'^{2} + 1) = 1$; (2) $y'' - 3y' + 2y = 0$.
4. (1) $x - \sqrt{xy} = C$; (2) $y = ax + \frac{C}{\ln x}$;

(3) $x = Cy^{-2} + \ln y - \frac{1}{2};$ \* (4) $y^{-2} = Ce^{x^2} + x^2 + 1$;

(5) $y = \ln |\cos (x + C_1)| + C_2;$ (6) $y = \frac{1}{2C_1} (\mathrm{e}^{C_1x + C_2} + \mathrm{e}^{-C_1x - C_2})$;

(7) $y = \mathrm{e}^{-x}(C_1\cos 2x + C_2\sin 2x) - \frac{4}{17}\cos 2x + \frac{1}{17}\sin 2x;$

(8) $y = C_{1} + C_{2}\mathrm{e}^{x} + C_{3}\mathrm{e}^{-2x} + \left(\frac{1}{6} x^{2} - \frac{4}{9} x\right)\mathrm{e}^{x} - x^{2} - x;$

\* (9) $x^{2} = Cy^{6} + y^{4}$; (10) $\sqrt{(x^2 + y)^3} = x^3 + \frac{3}{2}xy + C$.

5. $^{*}$ (1)  $x(1+2\ln|y|)-y^{2}=0;$ 

(2)  $y=-\frac{1}{a}\ln(ax+1);$
(3)  $y = 2 \arctan e^{x}$ ;

(4)  $y = x e^{-x} + \frac{1}{2} \sin x.$

6.  $y = x - x \ln x.$

7. 约  $250 \, m^{3}$ .

8.  $\varphi(x)=\cos x+\sin x.$

9.  $\varphi(x)=\sqrt{e^{2x}-1}-\arctan\sqrt{e^{2x}-1}.$

10. 略.

\* 11. (1) $y = \frac{1}{x} (C_1 + C_2\ln |x|)$; (2) $y = C_1x^2 + C_2x^3 + \frac{1}{2} x$.

\*12. (1) $\left\{ \begin{array}{l} x = (C_1 + C_2t)e^{-t} + \frac{1}{2} t, \\ y = -(C_1 + C_2 + C_2t)e^{-t} - \frac{1}{2}; \end{array} \right.$

(2) $\left\{ \begin{array}{l}x = C_1 + C_2\mathrm{e}^{-t} + C_3\mathrm{e}^{-2t} - \frac{1}{6}\mathrm{e}^t,\\ y = C_4\mathrm{e}^{-t} - C_1 + C_3\mathrm{e}^{-2t} + \frac{1}{3}\mathrm{e}^t. \end{array} \right.$

423

---

## 郑重声明

高等教育出版社依法对本书享有专有出版权。任何未经许可的复制、销售行为均违反《中华人民共和国著作权法》，其行为人将承担相应的民事责任和行政责任；构成犯罪的，将被依法追究刑事责任。为了维护市场秩序，保护读者的合法权益，避免读者误用盗版书造成不良后果，我社将配合行政执法部门和司法机关对违法犯罪的单位和个人进行严厉打击。社会各界人士如发现上述侵权行为，希望及时举报，我社将奖励举报有功人员。

反盗版举报电话 （010）58581999 58582371

反盗版举报邮箱 dd@hep.com.cn

通信地址 北京市西城区德外大街4号 高等教育出版社法律事务部

邮政编码 100120

## 读者意见反馈

为收集对教材的意见建议,进一步完善教材编写并做好服务工作,读者可将对本教材的意见建议通过如下渠道反馈至我社。

咨询电话 400-810-0598

反馈邮箱 hepsci@pub.hep.cn

通信地址 北京市朝阳区惠新东街4号富盛大厦1座
高等教育出版社理科事业部

邮政编码 100029

## 防伪查询说明

用户购书后刮开封底防伪涂层,使用手机微信等软件扫描二维码,会跳转至防伪查询网页,获得所购图书详细信息。

防伪客服电话 (010) 58582300
