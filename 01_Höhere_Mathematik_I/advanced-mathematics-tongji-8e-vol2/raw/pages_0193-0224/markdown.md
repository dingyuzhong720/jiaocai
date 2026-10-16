(1) 它关于 z 轴的转动惯量  $I_{z}$ ;
(2) 它的质心.

## 第二节 对坐标的曲线积分

## 一、对坐标的曲线积分的概念与性质

变力沿曲线所做的功 设一个质点在 $xOy$ 面内受到力

$$
\boldsymbol {F} (x, y) = P (x, y) \boldsymbol {i} + Q (x, y) \boldsymbol {j}
$$

的作用,从点 A 沿光滑曲线弧 L 移动到点 B,其中函数  $P(x,y)$  与  $Q(x,y)$  在 L 上连

续.要计算在上述移动过程中变力 $F(x,y)$ 所做的功（图11-4）.

我们知道,如果力 F 是恒力,且质点从 A 沿直线移动到 B,那么恒力 F 所做的功 W 等于向量 F 与向量  $\overrightarrow{AB}$  的数量积,即

$$
W = \boldsymbol {F} \cdot \overrightarrow {A B}.
$$

现在  $F(x,y)$  是变力,且质点沿曲线 L 移动,功 W 不能直接按以上公式计算.然而第一节中用来处理曲线形构件质量问题的方法,原则上也适用于目前的问题.

![](images/page_192_chart_13.jpg)

<details>
<summary>scatter</summary>

| Point | x-coordinate | y-coordinate |
| --- | --- | --- |
| A=M0 | ~1.5 | ~2.5 |
| M1 | ~2.0 | ~3.5 |
| M2 | ~2.5 | ~4.0 |
| L | ~3.0 | ~4.5 |
| Mi-1 | ~4.5 | ~6.0 |
| Mi | ~5.5 | ~7.0 |
| Mn-1 | ~6.5 | ~7.5 |
| B=Mn | ~8.0 | ~8.0 |
</details>

图11-4

先用曲线弧 L 上的点  $M_{1}(x_{1},y_{1}), M_{2}(x_{2},y_{2}), \cdots, M_{n-1}(x_{n-1},y_{n-1})$  把 L 分成 n 个小弧段，取其中一个有向小弧段  $\widehat{M_{i-1}M_{i}}$  来分析:由于  $\widehat{M_{i-1}M_{i}}$  光滑而且很短，可以用有向线段

$$
\overrightarrow {M _ {i - 1} M _ {i}} = (\Delta x _ {i}) \boldsymbol {i} + (\Delta y _ {i}) \boldsymbol {j}
$$

来近似代替它,其中  $\Delta x_{i}=x_{i}-x_{i-1},\Delta y_{i}=y_{i}-y_{i-1}$ . 又由于函数  $P(x,y)$  与  $Q(x,y)$  在 L 上连续,可以用  $\widehat{M_{i-1}M_{i}}$  上任意取定的一点  $(\xi_{i},\eta_{i})$  处的力

$$
\boldsymbol {F} (\xi_ {i}, \eta_ {i}) = P (\xi_ {i}, \eta_ {i}) \boldsymbol {i} + Q (\xi_ {i}, \eta_ {i}) \boldsymbol {j}
$$

来近似代替这小弧段上各点处的力.这样,变力 $F(x,y)$ 沿有向小弧段 $\widehat{M_{i-1}M_i}$ 所做的功 $\Delta W_i$ 可以认为近似地等于恒力 $F(\xi_i,\eta_i)$ 沿 $\overrightarrow{M_{i-1}M_i}$ 所做的功:

$$
\Delta W _ {i} \approx F (\xi_ {i}, \eta_ {i}) \cdot \overrightarrow {M _ {i - 1} M _ {i}},
$$

即

$$
\Delta W _ {i} \approx P (\xi_ {i}, \eta_ {i}) \Delta x _ {i} + Q (\xi_ {i}, \eta_ {i}) \Delta y _ {i}.
$$

于是

$$
W = \sum_ {i = 1} ^ {n} \Delta W _ {i} \approx \sum_ {i = 1} ^ {n} \left[ P (\xi_ {i}, \eta_ {i}) \Delta x _ {i} + Q (\xi_ {i}, \eta_ {i}) \Delta y _ {i} \right].
$$

用 $\lambda$ 表示 $n$ 个小弧段的最大长度, 令 $\lambda \to 0$ 取上述和的极限, 所得到的极限自然地被认作变力 $F$ 沿有向曲线弧所做的功, 即

$$
W = \lim _ {\lambda \to 0} \sum_ {i = 1} ^ {n} \left[ P (\xi_ {i}, \eta_ {i}) \Delta x _ {i} + Q (\xi_ {i}, \eta_ {i}) \Delta y _ {i} \right].
$$

这种和的极限在研究其他问题时也会遇到.现在引进下面的定义:

定义 设 L 为 xOy 面内从点 A 到点 B 的一条有向光滑曲线弧, 函数  $P(x,y)$  与  $Q(x,y)$  在 L 上有界. 在 L 上沿 L 的方向任意插入一点列  $M_{1}(x_{1},y_{1}), M_{2}(x_{2},y_{2}), \cdots, M_{n-1}(x_{n-1},y_{n-1})$ , 把 L 分成 n 个有向小弧段

$$
\widehat {M _ {i - 1} M _ {i}} \quad (i = 1, 2, \dots , n; M _ {0} = A, M _ {n} = B).
$$

设  $\Delta x_{i}=x_{i}-x_{i-1},\Delta y_{i}=y_{i}-y_{i-1}$ ，点  $(\xi_{i},\eta_{i})$  为  $\widehat{M_{i-1}M_{i}}$  上任意取定的点，作乘积  $P(\xi_{i},\eta_{i})\Delta x_{i}$   $(i=1,2,\cdots,n)$ ，并作和  $\sum_{i=1}^{n}P(\xi_{i},\eta_{i})\Delta x_{i}$ ，如果当各小弧段长度的最大值  $\lambda\to0$  时，这和的极限总存在，且与曲线弧 L 的分法及点  $(\xi_{i},\eta_{i})$  的取法无关，那么称此极限为函数  $P(x,y)$  在有向曲线弧 L 上对坐标 x 的曲线积分，记作  $\int_{L}P(x,y)\mathrm{d}x$ 。类似地，如果  $\lim_{\lambda\to0}\sum_{i=1}^{n}Q(\xi_{i},\eta_{i})\Delta y_{i}$  总存在，且与曲线弧 L 的分法及点  $(\xi_{i},\eta_{i})$  的取法无关，那么称此极限为函数  $Q(x,y)$  在有向曲线弧 L 上对坐标 y 的曲线积分，记作  $\int_{L}Q(x,y)\mathrm{d}y$ 。即

$$
\begin{array}{l} \int_ {L} P (x, y) \mathrm{d} x = \lim _ {\lambda \to 0} \sum_ {i = 1} ^ {n} P (\xi_ {i}, \eta_ {i}) \Delta x _ {i}, \\ \int_ {L} Q (x, y) \mathrm{d} y = \lim _ {\lambda \to 0} \sum_ {i = 1} ^ {n} Q (\xi_ {i}, \eta_ {i}) \Delta y _ {i}, \\ \end{array}
$$

其中  $P(x,y)$ ,  $Q(x,y)$  叫做被积函数, L 叫做积分弧段.

以上两个积分也称为第二类曲线积分.

在第二目中我们将看到, 当  $P(x,y)$  与  $Q(x,y)$  在有向光滑曲线弧 L 上连续时, 对坐标的曲线积分  $\int_{L} P(x,y) \, dx$  及  $\int_{L} Q(x,y) \, dy$  都存在. 以后我们总假定  $P(x,y)$  与  $Q(x,y)$  在 L 上连续.

上述定义可以类似地推广到积分弧段为空间有向曲线弧 $\Gamma$ 的情形:

$$
\begin{array}{l} \int_ {\Gamma} P (x, y, z) \mathrm{d} x = \lim _ {\lambda \to 0} \sum_ {i = 1} ^ {n} P (\xi_ {i}, \eta_ {i}, \zeta_ {i}) \Delta x _ {i}, \\ \int_ {\Gamma} Q (x, y, z) \mathrm{d} y = \lim _ {\lambda \to 0} \sum_ {i = 1} ^ {n} Q (\xi_ {i}, \eta_ {i}, \zeta_ {i}) \Delta y _ {i}, \\ \end{array}
$$

$$
\int_ {\Gamma} R (x, y, z) \mathrm{d} z = \lim _ {\lambda \rightarrow 0} \sum_ {i = 1} ^ {n} R (\xi_ {i}, \eta_ {i}, \zeta_ {i}) \Delta z _ {i}.
$$

应用上经常出现的是

$$
\int_ {L} P (x, y) \mathrm{d} x + \int_ {L} Q (x, y) \mathrm{d} y
$$

这种合并起来的形式,为简便起见,把上式写成

$$
\int_ {L} P (x, y) \mathrm{d} x + Q (x, y) \mathrm{d} y,
$$

也可写成向量形式

$$
\int_ {L} \boldsymbol {F} (x, y) \cdot \mathrm{d} \boldsymbol {r},
$$

其中 $F(x,y) = P(x,y)i + Q(x,y)j$ 为向量值函数， $\mathrm{d}\pmb {r} = \mathrm{d}\pmb {x}\pmb {i} + \mathrm{d}\pmb {y}\pmb{j}$

例如,本目开始时讨论过的变力 F 所做的功可以表达成

$$
W = \int_ {L} P (x, y)   \mathrm{d} x + Q (x, y)   \mathrm{d} y,
$$

或

$$
W = \int_ {L} \boldsymbol {F} (x, y) \cdot \mathrm{d} \boldsymbol {r}.
$$

类似地,把

$$
\int_ {\Gamma} P (x, y, z) \mathrm{d} x + \int_ {\Gamma} Q (x, y, z) \mathrm{d} y + \int_ {\Gamma} R (x, y, z) \mathrm{d} z
$$

简写成

$$
\int_ {\Gamma} P (x, y, z) \mathrm{d} x + Q (x, y, z) \mathrm{d} y + R (x, y, z) \mathrm{d} z,
$$

或

$$
\int_ {\Gamma} A (x, y, z) \cdot \mathrm{d} r,
$$

其中 $A(x,y,z) = P(x,y,z)i + Q(x,y,z)\boldsymbol {j} + R(x,y,z)\boldsymbol {k},\mathrm{d}\boldsymbol {r} = \mathrm{d}x\boldsymbol {i} + \mathrm{d}y\boldsymbol {j} + \mathrm{d}z\boldsymbol{k}.$

如果 $L$ （或 $\Gamma$ )是分段光滑的，我们规定函数在有向曲线弧 $L$ （或 $\Gamma$ )上对坐标的曲线积分等于在光滑的各段上对坐标的曲线积分之和.

根据上述曲线积分的定义,可以导出对坐标的曲线积分的一些性质.为了表达简便起见,我们用向量形式表达,并假定其中的向量值函数在曲线 L 上连续①.

## 性质1 设 $\alpha$ 与 $\beta$ 为常数, 则

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 向量值函数 $F(x,y)$ 在曲线L上连续是指:对L上任意点 $M_{0}(x_{0},y_{0})$ ，当L上的动点 $M(x,y)$ 沿L趋于 $M_{0}$ 时，有 $|F(x,y)-F(x_{0},y_{0})|\rightarrow0$ 。若 $F(x,y)=P(x,y)i+Q(x,y)j$ ，则 $F(x,y)$ 在L上连续等价于 $P(x,y)$ 与 $Q(x,y)$ 均在L上连续。</span></small>

$$
\int_ {L} \left[ \alpha F _ {1} (x, y) + \beta F _ {2} (x, y) \right] \cdot \mathrm{d} r = \alpha \int_ {L} F _ {1} (x, y) \cdot \mathrm{d} r + \beta \int_ {L} F _ {2} (x, y) \cdot \mathrm{d} r.
$$

性质2 若有向曲线弧 $L$ 可分成两段光滑的有向曲线弧 $L_{1}$ 和 $L_{2}$，则

$$
\int_ {L} \boldsymbol {F} (x, y) \cdot \mathrm{d} \boldsymbol {r} = \int_ {L _ {1}} \boldsymbol {F} (x, y) \cdot \mathrm{d} \boldsymbol {r} + \int_ {L _ {2}} \boldsymbol {F} (x, y) \cdot \mathrm{d} \boldsymbol {r}.
$$

性质3 设 $L$ 是有向光滑曲线弧, $L^{-}$ 是 $L$ 的反向曲线弧, 则

$$
\int_ {L ^ {-}} \boldsymbol {F} (x, y) \cdot \mathrm{d} \boldsymbol {r} = - \int_ {L} \boldsymbol {F} (x, y) \cdot \mathrm{d} \boldsymbol {r}.
$$

证 把 $L$ 分成 $n$ 小段, 相应的 $L^{-}$也分成 $n$ 小段. 对于每一个小弧段来说, 当曲线弧的方向改变时, 有向弧段在坐标轴上的投影, 其绝对值不变, 但要改变符号, 因此性质3成立.

性质 3 表示, 当积分弧段的方向改变时, 对坐标的曲线积分要改变符号. 因此关于对坐标的曲线积分, 我们必须注意积分弧段的方向.

这一性质是对坐标的曲线积分所特有的,对弧长的曲线积分不具有这一性质.而对弧长的曲线积分所具有的性质3,对坐标的曲线积分也不具有类似的性质.

## 二、对坐标的曲线积分的计算法

定理 设 $P(x,y)$ 与 $Q(x,y)$ 在有向曲线弧 $L$ 上有定义且连续，$L$ 的参数方程为

$$
\left\{ \begin{array}{l} x = \varphi (t), \\ y = \psi (t), \end{array} \right.
$$

当参数 $t$ 单调地由 $\alpha$ 变到 $\beta$ 时，点 $M(x,y)$ 从 $L$ 的起点 $A$ 沿 $L$ 运动到终点 $B$ ，若$\varphi (t)$ 与 $\psi (t)$ 在以 $\alpha$ 及 $\beta$ 为端点的闭区间上具有一阶连续导数，且 $\varphi^{\prime 2}(t) + \psi^{\prime 2}(t)\neq 0,$ 则曲线积分 $\int_{L}P(x,y)\mathrm{d}x + Q(x,y)\mathrm{d}y$ 存在，且

$$
\begin{array}{l} \int_ {L} P (x, y) \mathrm{d} x + Q (x, y) \mathrm{d} y \\ = \int_ {\alpha} ^ {\beta} \left\{P [ \varphi (t), \psi (t) ] \varphi^ {\prime} (t) + Q [ \varphi (t), \psi (t) ] \psi^ {\prime} (t) \right\} \mathrm{d} t. \tag {2-1} \\ \end{array}
$$

证 在 $L$ 上取一点列

$$
A = M _ {0}, M _ {1}, M _ {2}, \dots , M _ {n - 1}, M _ {n} = B,
$$

它们对应于一列单调变化的参数值

$$
\alpha = t _ {0}, t _ {1}, t _ {2}, \dots , t _ {n - 1}, t _ {n} = \beta .
$$

根据对坐标的曲线积分的定义,有

$$
\int_ {L} P (x, y) \mathrm{d} x = \lim _ {\lambda \to 0} \sum_ {i = 1} ^ {n} P (\xi_ {i}, \eta_ {i}) \Delta x _ {i}.
$$

设点 $(\xi_{i},\eta_{i})$ 对应于参数值 $\tau_{i}$ ，即 $\xi_{i} = \varphi (\tau_{i}),\eta_{i} = \psi (\tau_{i})$ ，这里 $\tau_{i}$ 在 $t_{i - 1}$ 与 $t_i$ 之间.由于

$$
\Delta x _ {i} = x _ {i} - x _ {i - 1} = \varphi (t _ {i}) - \varphi (t _ {i - 1}),
$$

应用微分中值定理,有

$$
\Delta x _ {i} = \varphi^ {\prime} (\tau_ {i} ^ {\prime}) \Delta t _ {i},
$$

其中 $\Delta t_{i} = t_{i} - t_{i - 1},\tau_{i}^{\prime}$ 在 $t_{i - 1}$ 与 $t_i$ 之间.于是

$$
\int_ {L} P (x, y) \mathrm{d} x = \lim _ {\lambda \rightarrow 0} \sum_ {i = 1} ^ {n} P [ \varphi (\tau_ {i}), \psi (\tau_ {i}) ] \varphi^ {\prime} (\tau_ {i} ^ {\prime}) \Delta t _ {i}.
$$

因为函数  $\varphi'(t)$  在闭区间  $[\alpha,\beta]$  （或  $[\beta,\alpha]$ ）上连续，我们可以把上式中的  $\tau_{i}^{\prime}$  换成  $\tau_{i}^{①}$ ，从而

$$
\int_ {L} P (x, y) \mathrm{d} x = \lim _ {\lambda \rightarrow 0} \sum_ {i = 1} ^ {n} P [ \varphi (\tau_ {i}), \psi (\tau_ {i}) ] \varphi^ {\prime} (\tau_ {i}) \Delta t _ {i}.
$$

上式右端的和的极限就是定积分 $\int_{\alpha}^{\beta}P[\varphi (t),\psi (t)]\varphi '(t)\mathrm{d}t$ ，由于函数 $P[\varphi (t),\psi (t)]\varphi '(t)$ 连续，这个定积分是存在的，因此上式左端的曲线积分 $\int_{L}P(x,y)\mathrm{d}x$ 也存在，并且有

$$
\int_ {L} P (x, y) \mathrm{d} x = \int_ {\alpha} ^ {\beta} P [ \varphi (t), \psi (t) ] \varphi^ {\prime} (t) \mathrm{d} t.
$$

同理可证

$$
\int_ {L} Q (x, y) \mathrm{d} y = \int_ {\alpha} ^ {\beta} Q [ \varphi (t), \psi (t) ] \psi^ {\prime} (t) \mathrm{d} t,
$$

把以上两式相加,得

$$
\int_ {L} P (x, y) \mathrm{d} x + Q (x, y) \mathrm{d} y = \int_ {\alpha} ^ {\beta} \left\{P [ \varphi (t), \psi (t) ] \varphi^ {\prime} (t) + Q [ \varphi (t), \psi (t) ] \psi^ {\prime} (t) \right\} \mathrm{d} t,
$$

这里下限  $\alpha$  对应于 L 的起点, 上限  $\beta$  对应于 L 的终点.

公式(2-1)表明,计算对坐标的曲线积分

$$
\int_ {L} P (x, y) \mathrm{d} x + Q (x, y) \mathrm{d} y
$$

时, 只要把 $x, y, \mathrm{d}x, \mathrm{d}y$ 依次换为 $\varphi(t), \psi(t), \varphi'(t) \mathrm{d}t, \psi'(t) \mathrm{d}t$, 然后从 $L$ 的起点所对应的参数值 $\alpha$ 到 $L$ 的终点所对应的参数值 $\beta$ 作定积分就行了, 这里必须注意, 下限 $\alpha$ 对应于 $L$ 的起点, 上限 $\beta$ 对应于 $L$ 的终点, $\alpha$ 不一定小于 $\beta$.

如果 L 由方程  $y=\psi(x)$  或  $x=\varphi(y)$  给出, 可以看做参数方程的特殊情形, 例如, 当 L 由  $y=\psi(x)$  给出时, 公式(2-1)成为

$$
\int_ {L} P (x, y) \mathrm{d} x + Q (x, y) \mathrm{d} y = \int_ {a} ^ {b} \left\{P [ x, \psi (x) ] + Q [ x, \psi (x) ] \psi^ {\prime} (x) \right\} \mathrm{d} x,
$$

这里下限 a 对应 L 的起点, 上限 b 对应 L 的终点.

公式(2-1)可推广到空间曲线  $\Gamma$  由参数方程

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 它的证明要用到函数  $\varphi'(t)$  在闭区间上的一致连续性, 这里从略.</span></small>

$$
x = \varphi (t), \quad y = \psi (t), \quad z = \omega (t)
$$

给出的情形,这样便得到

$$
\begin{array}{l} \int_ {\Gamma} P (x, y, z) \mathrm{d} x + Q (x, y, z) \mathrm{d} y + R (x, y, z) \mathrm{d} z \\ = \int_ {\alpha} ^ {\beta} \left\{P [ \varphi (t), \psi (t), \omega (t) ] \varphi^ {\prime} (t) + Q [ \varphi (t), \psi (t), \omega (t) ] \psi^ {\prime} (t) + \right. \\ R [ \varphi (t), \psi (t), \omega (t) ] \omega^ {\prime} (t) \} \mathrm{d} t, \\ \end{array}
$$

这里下限  $\alpha$  对应  $\Gamma$  的起点, 上限  $\beta$  对应  $\Gamma$  的终点.

例1 计算 $\int_{L} xy \, \mathrm{d}x$，其中 $L$ 为抛物线 $y^2 = x$ 上从点 $A(1, -1)$ 到点 $B(1, 1)$ 的一段弧（图11-5）.

解法一 将所给积分化为对 $x$ 的定积分来计算. 由于 $y = \pm \sqrt{x}$ 不是单值函数, 所以要把 $L$ 分为 $AO$ 和 $OB$ 两部分. 在 $AO$ 上, $y = -\sqrt{x}, x$ 从 1 变到 0; 在 $OB$ 上, $y = \sqrt{x}, x$ 从 0 变到 1. 因此

$$
\begin{array}{l} \int_ {L} x y \mathrm{d} x = \int_ {A O} x y \mathrm{d} x + \int_ {O B} x y \mathrm{d} x \\ = \int_ {1} ^ {0} x (- \sqrt {x}) \mathrm{d} x + \int_ {0} ^ {1} x \sqrt {x} \mathrm{d} x = 2 \int_ {0} ^ {1} x ^ {\frac {3}{2}} \mathrm{d} x = \frac {4}{5}. \\ \end{array}
$$

解法二 将所给积分化为对 $y$ 的定积分来计算, 现在 $x = y^2, y$ 从-1变到1. 因此

$$
\int_ {L} x y \mathrm{d} x = \int_ {- 1} ^ {1} y ^ {2} y (y ^ {2}) ^ {\prime} \mathrm{d} y = 2 \int_ {- 1} ^ {1} y ^ {4} \mathrm{d} y = 2 \left[ \frac {y ^ {5}}{5} \right] _ {- 1} ^ {1} = \frac {4}{5}.
$$

例2 计算 $\int_{L} y^{2} \mathrm{~d} x$ 其中 $L$ 为(图11-6):

（1）半径为 a、圆心为原点、按逆时针方向绕行的上半圆周；
(2) 从点  $A(a,0)$  沿 x 轴到点  $B(-a,0)$  的直线段.

![](images/page_197_image_14.jpg)

<details>
<summary>text_image</summary>

y
y=√x
L
O
x
B(1,1)
y=-√x
A(1,-1)
</details>

图11-5

![](images/page_197_image_16.jpg)

<details>
<summary>text_image</summary>

y
B(-a,0) O A(a,0) x
</details>

图11-6

解 (1) $L$ 是参数方程

$$
x = a \cos \theta , \quad y = a \sin \theta
$$

当参数 $\theta$ 从0变到 $\pi$ 的曲线弧.因此

$$
\begin{array}{l} \int_ {L} y ^ {2} \mathrm{d} x = \int_ {0} ^ {\pi} a ^ {2} \sin^ {2} \theta (- a \sin \theta) \mathrm{d} \theta = a ^ {3} \int_ {0} ^ {\pi} (1 - \cos^ {2} \theta) \mathrm{d} (\cos \theta) \\ = a ^ {3} \left[ \cos \theta - \frac {\cos^ {3} \theta}{3} \right] _ {0} ^ {\pi} = - \frac {4}{3} a ^ {3}. \\ \end{array}
$$

(2) L 的方程为 y=0, x 从 a 变到 -a. 所以

$$
\int_ {L} y ^ {2} \mathrm{d} x = \int_ {a} ^ {- a} 0 \mathrm{d} x = 0.
$$

从例 2 看出,虽然两个曲线积分的被积函数相同,起点和终点也相同,但沿不同路径得出的积分值并不相等.

例 3 计算  $\int_{L} 2xy dx + x^{2} dy$ ，其中 L 为(图11-7):

(1) 抛物线  $y=x^{2}$  上从  $O(0,0)$  到  $B(1,1)$  的一段弧；
(2) 抛物线  $x=y^{2}$  上从  $O(0,0)$  到  $B(1,1)$  的一段弧；
（3）有向折线 OAB，这里 O, A, B 依次是点  $(0,0)$ ， $(1,0)$ ， $(1,1)$ .

![](images/page_198_image_12.jpg)

<details>
<summary>text_image</summary>

y
x=y²
B(1,1)
y=x²
O
A(1,0) x
</details>

图11-7

解（1）化为对 $x$ 的定积分. $L: y = x^2, x$ 从0变到1. 所以

$$
\int_ {L} 2 x y \mathrm{d} x + x ^ {2} \mathrm{d} y = \int_ {0} ^ {1} (2 x \cdot x ^ {2} + x ^ {2} \cdot 2 x) \mathrm{d} x = 4 \int_ {0} ^ {1} x ^ {3} \mathrm{d} x = 1.
$$

(2) 化为对 y 的定积分.  $L: x = y^{2}$ , y 从 0 变到 1. 所以

$$
\int_ {L} 2 x y \mathrm{d} x + x ^ {2} \mathrm{d} y = \int_ {0} ^ {1} (2 y ^ {2} \cdot y \cdot 2 y + y ^ {4}) \mathrm{d} y = 5 \int_ {0} ^ {1} y ^ {4} \mathrm{d} y = 1.
$$

(3) $\int_{L} 2xy\mathrm{d}x + x^{2}\mathrm{d}y = \int_{OA} 2xy\mathrm{d}x + x^{2}\mathrm{d}y + \int_{AB} 2xy\mathrm{d}x + x^{2}\mathrm{d}y,$

在 OA 上, y=0, x 从 0 变到 1, 所以

$$
\int_ {O A} 2 x y \mathrm{d} x + x ^ {2} \mathrm{d} y = \int_ {0} ^ {1} (2 x \cdot 0 + x ^ {2} \cdot 0) \mathrm{d} x = 0.
$$

在 AB 上, x=1, y 从 0 变到 1, 所以

$$
\int_ {A B} 2 x y \mathrm{d} x + x ^ {2} \mathrm{d} y = \int_ {0} ^ {1} (2 y \cdot 0 + 1) \mathrm{d} y = 1.
$$

从而

图

释疑解难

11-2

$$
\int_ {L} 2 x y \mathrm{d} x + x ^ {2} \mathrm{d} y = 0 + 1 = 1.
$$

从例 3 可以看出,虽然沿不同路径,曲线积分的值可以相等.

例4 计算 $\int_{\Gamma} x^3 \mathrm{d}x + 3zy^2 \mathrm{d}y - x^2 y \mathrm{d}z$，其中 $\Gamma$ 是从点 $A(3,2,1)$ 到点 $B(0,0,0)$ 的直线段 $AB$.

解 直线段 $AB$ 的方程是

$$
\frac {x}{3} = \frac {y}{2} = \frac {z}{1},
$$

化为参数方程得

$$
x = 3 t, \quad y = 2 t, \quad z = t, \quad t \text {从} 1 \text {变到} 0.
$$

所以

$$
\begin{array}{l} \int_ {\Gamma} x ^ {3} \mathrm{d} x + 3 z y ^ {2} \mathrm{d} y - x ^ {2} y \mathrm{d} z \\ = \int_ {1} ^ {0} \left[ (3 t) ^ {3} \cdot 3 + 3 t (2 t) ^ {2} \cdot 2 - (3 t) ^ {2} \cdot 2 t \right] \mathrm{d} t = 8 7 \int_ {1} ^ {0} t ^ {3} \mathrm{d} t = - \frac {8 7}{4}. \\ \end{array}
$$

例 5 设一个质点在点  $M(x,y)$  处受到力 F 的作用, F 的大小与点 M 到原点 O 的距离成正比, F 的方向恒指向原点. 此质点由点 A(a,0) 沿椭圆  $\frac{x^{2}}{a^{2}} + \frac{y^{2}}{b^{2}} = 1$  按逆时针方向移动到点 B(0,b), 求力 F 所做的功 W.

解 $\overrightarrow{OM} = x\mathbf{i} + y\mathbf{j},\quad |\overrightarrow{OM}| = \sqrt{x^2 + y^2}.$

由假设有 $F = -k(xi + yj)$，其中 $k > 0$ 是比例常数。于是

$$
W = \int_ {\widehat {A B}} \boldsymbol {F} \cdot \mathrm{d} \boldsymbol {r} = \int_ {\widehat {A B}} - k x \mathrm{d} x - k y \mathrm{d} y = - k \int_ {\widehat {A B}} x \mathrm{d} x + y \mathrm{d} y.
$$

利用椭圆的参数方程 $\left\{\begin{aligned}x&=a\cos t,\\ y&=b\sin t,\end{aligned}\right.$ 起点A、终点B分别对应参数 $t=0,t=\frac{\pi}{2}$ .于是

$$
\begin{array}{l} W = - k \int_ {0} ^ {\frac {\pi}{2}} (- a ^ {2} \cos t \sin t + b ^ {2} \sin t \cos t) \mathrm{d} t \\ = k (a ^ {2} - b ^ {2}) \int_ {0} ^ {\frac {\pi}{2}} \sin t \cos t \mathrm{d} t = \frac {k}{2} (a ^ {2} - b ^ {2}). \\ \end{array}
$$

## 三、两类曲线积分之间的联系

设有向曲线弧 L 的起点为 A, 终点为 B. 曲线弧 L 由参数方程

$$
\left\{ \begin{array}{l} x = \varphi (t), \\ y = \psi (t) \end{array} \right.
$$

给出,起点A与终点B分别对应参数 $\alpha$ 与 $\beta$ .不妨设 $\alpha<\beta$ （若 $\alpha>\beta$ ,可令s=-t,A,B对应 $s=-\alpha,s=-\beta$ ,就有 $(-α)<(-\beta)$ ,把下面的讨论对参数s进行即可），并设函数 $\varphi(t)$ 与 $\psi(t)$ 在闭区间 $[\alpha,\beta]$ 上具有一阶连续导数，且 $\varphi^{\prime2}(t)+\psi^{\prime2}(t)\neq0$ ,又函数 $P(x,y)$ 与 $Q(x,y)$ 在L上连续.于是,由对坐标的曲线积分计算公式(2-1)有

$$
\int_ {L} P (x, y) \mathrm{d} x + Q (x, y) \mathrm{d} y = \int_ {\alpha} ^ {\beta} \left\{P [ \varphi (t), \psi (t) ] \varphi^ {\prime} (t) + Q [ \varphi (t), \psi (t) ] \psi^ {\prime} (t) \right\} \mathrm{d} t.
$$

我们知道,向量  $\boldsymbol{\tau}=\varphi'(t)\boldsymbol{i}+\psi'(t)\boldsymbol{j}$  是曲线弧 L 在点  $M(\varphi(t),\psi(t))$  处的一个切向量,它的方向与参数 t 的增长方向一致,当  $\alpha<\beta$  时,这个方向就是有向曲线弧 L 的方向.以后,我们称这种方向与有向曲线弧的方向一致的切向量为有向曲线弧的切向量.于是,有向曲线弧 L 的切向量为

$$
\boldsymbol {\tau} = \varphi^ {\prime} (t) \boldsymbol {i} + \psi^ {\prime} (t) \boldsymbol {j},
$$

它的方向余弦为

$$
\cos \alpha = \frac {\varphi^ {\prime} (t)}{\sqrt {\varphi^ {\prime 2} (t) + \psi^ {\prime 2} (t)}}, \quad \cos \beta = \frac {\psi^ {\prime} (t)}{\sqrt {\varphi^ {\prime 2} (t) + \psi^ {\prime 2} (t)}}.
$$

由对弧长的曲线积分的计算公式可得

$$
\begin{array}{l} \int_ {L} \left[ P (x, y) \cos \alpha + Q (x, y) \cos \beta \right] \mathrm{d} s \\ = \int_ {\alpha} ^ {\beta} \left\{P [ \varphi (t), \psi (t) ] \frac {\varphi^ {\prime} (t)}{\sqrt {\varphi^ {\prime 2} (t) + \psi^ {\prime 2} (t)}} + \right. \\ Q [ \varphi (t), \psi (t) ] \frac {\psi^ {\prime} (t)}{\sqrt {\varphi^ {\prime 2} (t) + \psi^ {\prime 2} (t)}} \Bigg \} \sqrt {\varphi^ {\prime 2} (t) + \psi^ {\prime 2} (t)} \mathrm{d} t \\ = \int_ {\alpha} ^ {\beta} \left\{P [ \varphi (t), \psi (t) ] \varphi^ {\prime} (t) + Q [ \varphi (t), \psi (t) ] \psi^ {\prime} (t) \right\} \mathrm{d} t. \\ \end{array}
$$

由此可见,平面曲线弧 L 上的两类曲线积分之间有如下联系:

$$
\int_ {L} P \mathrm{d} x + Q \mathrm{d} y = \int_ {L} (P \cos \alpha + Q \cos \beta) \mathrm{d} s, \tag {2-2}
$$

其中 $\alpha (x,y)$ 与 $\beta (x,y)$ 为有向曲线弧 $L$ 在点 $(x,y)$ 处的切向量的方向角.

类似地可知,空间曲线弧  $\Gamma$  上的两类曲线积分之间有如下联系:

$$
\int_ {\Gamma} P \mathrm{d} x + Q \mathrm{d} y + R \mathrm{d} z = \int_ {\Gamma} (P \cos \alpha + Q \cos \beta + R \cos \gamma) \mathrm{d} s, \tag {2-3}
$$

其中 $\alpha (x,y,z),\beta (x,y,z),\gamma (x,y,z)$ 为有向曲线弧 $\Gamma$ 在点 $(x,y,z)$ 处的切向量的方向角.

两类曲线积分之间的联系也可用向量的形式表达.例如,空间曲线弧  $\Gamma$  上的两类曲线积分之间的联系可写成如下形式:

$$
\int_ {\Gamma} \boldsymbol {A} \cdot \mathrm{d} \boldsymbol {r} = \int_ {\Gamma} \boldsymbol {A} \cdot \boldsymbol {\tau} \mathrm{d} s \tag {2-4}
$$

或

$$
\int_ {\Gamma} A \cdot \mathrm{d} r = \int_ {\Gamma} A _ {\tau} \mathrm{d} s, \tag {$2-4^{\prime$}}
$$

其中  $\boldsymbol{A}=(P,Q,R)$ ,  $\boldsymbol{\tau}=(\cos\alpha,\cos\beta,\cos\gamma)$  为有向曲线弧  $\Gamma$  在点  $(x,y,z)$  处的单位切向量,  $\mathrm{d}\boldsymbol{r}=\boldsymbol{\tau}\mathrm{d}s=(\mathrm{d}x,\mathrm{d}y,\mathrm{d}z)$ , 称为有向曲线元,  $A_{\tau}$  为向量 A 在向量  $\tau$  上的投影.

## 习题11-2

1. 设 $L$ 为 $xOy$ 面内直线 $x = a$ 上的一段，证明:$\int_{L} P(x, y) \mathrm{d}x = 0.$

2. 设 $L$ 为 $xOy$ 面内 $x$ 轴上从点 $(a,0)$ 到点 $(b,0)$ 的一段直线，证明:$\int_{L} P(x,y) \mathrm{d}x = \int_{a}^{b} P(x,0) \mathrm{d}x.$

3. 计算下列对坐标的曲线积分:

(1) $\int_{L}(x^{2} - y^{2})\mathrm{d}x$ ，其中 $L$ 是抛物线 $y = x^{2}$ 上从点(0,0)到点(2,4)的一段弧；
(2) $\oint_{L} xy \, \mathrm{d}x$, 其中 $L$ 为圆周 $(x - a)^2 + y^2 = a^2$ ($a > 0$) 及 $x$ 轴所围成的在第一象限内的区域的整个边界（按逆时针方向绕行）；

(3) $\int_{L} y \mathrm{~d}x + x \mathrm{~d}y$，其中 $L$ 为圆周 $x = R \cos t, y = R \sin t$ 上对应 $t$ 从0到 $\frac{\pi}{2}$ 的一段弧；

(4) $\oint_{L} \frac{(x + y) \, \mathrm{d}x - (x - y) \, \mathrm{d}y}{x^2 + y^2}$, 其中 $L$ 为圆周 $x^2 + y^2 = a^2$ （按逆时针方向绕行）；

(5) $\int_{\Gamma} x^{2} \mathrm{~d}x + z \mathrm{~d}y - y \mathrm{~d}z$，其中 $\Gamma$ 为曲线 $x = k\theta, y = a \cos \theta, z = a \sin \theta$ 上对应 $\theta$ 从0到 $\pi$ 的一段弧；

(6) $\int_{\Gamma} x \mathrm{~d}x + y \mathrm{~d}y + (x + y - 1) \mathrm{~d}z$，其中 $\Gamma$ 是从点 $(1,1,1)$ 到点 $(2,3,4)$ 的一段直线；

(7) $\oint_{\Gamma} \mathrm{d}x - \mathrm{d}y + y \mathrm{~d}z$，其中 $\Gamma$ 为有向闭折线 $ABCA$，这里的 $A, B, C$ 依次为点 $(1,0,0), (0,1,0), (0,0,1)$；

(8) $\int_{L}(x^{2} - 2xy)\mathrm{d}x + (y^{2} - 2xy)\mathrm{d}y$ ，其中 $L$ 是抛物线 $y = x^{2}$ 上从点 $(-1,1)$ 到点(1,1)的一段弧.

4. 计算 $\int_{L}(x + y)\mathrm{d}x + (y - x)\mathrm{d}y$ ，其中 $L$ 是

(1) 抛物线  $y^{2}=x$  上从点 (1,1) 到点 (4,2) 的一段弧；
(2) 从点(1,1)到点(4,2)的直线段;
(3) 先沿直线从点 $(1,1)$ 到点 $(1,2)$ ，然后再沿直线到点 $(4,2)$ 的折线；
(4) 曲线  $x=2t^{2}+t+1, y=t^{2}+1$  上从点 (1,1) 到点 (4,2) 的一段弧.

5. 一力场由沿横轴正方向的恒力 F 所构成. 试求当一质量为 m 的质点沿圆周  $x^{2} + y^{2} = R^{2}$  按逆时针方向移过位于第一象限的那一段弧时场力所做的功.
6. 设 z 轴与重力的方向一致, 求质量为 m 的质点从位置  $(x_{1}, y_{1}, z_{1})$  沿直线移到  $(x_{2}, y_{2}, z_{2})$  时重力所做的功.

7. 把对坐标的曲线积分  $\int_{L} P(x, y) \, dx + Q(x, y) \, dy$  化成对弧长的曲线积分, 其中 L 为

(1) 在 xOy 面内沿直线从点  $(0,0)$  到点  $(1,1)$ ;
(2) 沿抛物线  $y=x^{2}$  从点  $(0,0)$  到点  $(1,1)$ ;
(3) 沿上半圆周  $x^{2}+y^{2}=2x$  从点  $(0,0)$  到点  $(1,1)$ .

8. 设 $\Gamma$ 为曲线 $x = t, y = t^2, z = t^3$ 上相应于 $t$ 从0变到1的曲线弧，把对坐标的曲线积分 $\int_{\Gamma} P \mathrm{d}x+$

$Qdy+Rdz$ 化成对弧长的曲线积分.

9. 设曲线 $\Gamma$ 为球面 $x^{2} + y^{2} + z^{2} = a^{2}$ 与平面 $x + y + z = 0$ 的交线，从 $z$ 轴的正向看取逆时针方向，

$$
I = \oint_ {\Gamma} z \mathrm{d} x + x \mathrm{d} y + y \mathrm{d} z,
$$

试利用两类曲线积分之间的关系证明: $|I|\leqslant2\pi a^{2}$

## 第三节 格林公式及其应用

## 一、格林公式

在一元函数积分学中,牛顿-莱布尼茨公式

$$
\int_ {a} ^ {b} F ^ {\prime} (x) \mathrm{d} x = F (b) - F (a)
$$

表示: $F'(x)$ 在区间 $[a,b]$ 上的积分可以通过它的原函数 $F(x)$ 在这个区间端点上的值来表达.

下面要介绍的格林(Green)公式告诉我们,在平面闭区域 D 上的二重积分可以通过沿闭区域 D 的边界曲线 L 上的曲线积分来表达.

现在先介绍平面单连通区域的概念.设 $D$ 为平面区域,若 $D$ 内任一闭曲线所围的部分都属于 $D$,则称 $D$ 为平面单连通区域,否则称为复连通区域.通俗地说,平面单连通区域就是不含有“洞”(包括点“洞”)的区域,复连通区域是含有“洞”(包括点“洞”)的区域.例如,平面上的圆形区域 $\{(x,y)\mid x^{2}+y^{2}<1\}$、上半平面 $\{(x,y)\mid y>0\}$ 都是单连通区域,圆环形区域 $\{(x,y)\mid 1<x^{2}+y^{2}<4\},\{(x,y)\mid 0<x^{2}+y^{2}<2\}$ 都是复连通区域.

对平面区域 $D$ 的边界曲线 $L$, 我们规定 $L$ 的正向如下: 当观察者沿 $L$ 的这个方向行走时, $D$ 内在他近处的那一部分总在他的左边. 例如, $D$ 是边界曲线 $L$ 及 $l$ 所围成的复连通区域 (图11-8), 作为 $D$ 的正向边界, $L$ 的正向是逆时针方向, 而 $l$ 的正向是顺时针方向.

定理1 设闭区域 $D$ 由分段光滑的曲线 $L$ 围成, 若函数 $P(x, y)$ 及 $Q(x, y)$ 在 $D$ 上具有一阶连续偏导数, 则有

$$
\iint_ {D} \left(\frac {\partial Q}{\partial x} - \frac {\partial P}{\partial y}\right) \mathrm{d} x \mathrm{d} y = \oint_ {L} P \mathrm{d} x + Q \mathrm{d} y, \tag {3-1}
$$

![](images/page_202_image_15.jpg)

<details>
<summary>text_image</summary>

D
l
L
</details>

图11-8

其中 L 是 D 的取正向的边界曲线.

公式(3-1)叫做格林公式.

证 先假设穿过区域 $D$ 内部且平行于坐标轴的直线与 $D$ 的边界曲线 $L$ 的交点恰好为两点, 即区域 $D$ 既是 $X$ 型又是 $Y$ 型的情形.

图11-9、图11-10所示的区域都属于这种情形.例如,图11-9所示的区域 $D$ 显然是 $X$ 型的,事实上 $D$ 又是 $Y$ 型的.若设有向曲线弧 $\widehat{FGAE}$ 为 $L_1':x = \psi_1(y)$, $\widehat{EBCF}$ 为 $L_2':x = \psi_2(y)$,则 $D$ 可表达成

$$
D = \{(x, y)   |   \psi_ {1} (y) \leqslant x \leqslant \psi_ {2} (y), c \leqslant y \leqslant d \},
$$

即 D 又是 Y 型的.

![](images/page_203_image_5.jpg)

<details>
<summary>text_image</summary>

y
d
F
L₂:y=φ₂(x)
G
C
D
A
B
E
c
O
a
b
x
</details>

图11-9

![](images/page_203_image_7.jpg)

<details>
<summary>text_image</summary>

y
d
L₁':x=ψ₁(y)
D
c
O a b x
L₂':x=ψ₂(y)
</details>

图11-10

设 $D$ 如图11-9所示, 于是 $D = \{(x, y) \mid \varphi_1(x) \leqslant y \leqslant \varphi_2(x), a \leqslant x \leqslant b\}$. 因为 $\frac{\partial P}{\partial y}$ 连续, 所以由二重积分的计算法有

$$
\iint_ {D} \frac {\partial P}{\partial y} \mathrm{d} x \mathrm{d} y = \int_ {a} ^ {b} \left\{\int_ {\varphi_ {1} (x)} ^ {\varphi_ {2} (x)} \frac {\partial P (x , y)}{\partial y} \mathrm{d} y \right\} \mathrm{d} x = \int_ {a} ^ {b} \left\{P [ x, \varphi_ {2} (x) ] - P [ x, \varphi_ {1} (x) ] \right\} \mathrm{d} x.
$$

另一方面，由对坐标的曲线积分的性质及计算法有

$$
\begin{array}{l} \oint_ {L} P \mathrm{d} x = \int_ {L _ {1}} P \mathrm{d} x + \int_ {B C} P \mathrm{d} x + \int_ {L _ {2}} P \mathrm{d} x + \int_ {G A} P \mathrm{d} x \\ = \int_ {L _ {1}} P \mathrm{d} x + \int_ {L _ {2}} P \mathrm{d} x = \int_ {a} ^ {b} P [ x, \varphi_ {1} (x) ] \mathrm{d} x + \int_ {b} ^ {a} P [ x, \varphi_ {2} (x) ] \mathrm{d} x \\ = \int_ {a} ^ {b} \left\{P [ x, \varphi_ {1} (x) ] - P [ x, \varphi_ {2} (x) ] \right\} \mathrm{d} x, \\ \end{array}
$$

因此，

$$
- \iint_ {D} \frac {\partial P}{\partial y} \mathrm{d} x \mathrm{d} y = \oint_ {L} P \mathrm{d} x. \tag {3-2}
$$

又由于 $D = \{(x,y)\mid \psi_1(y)\leqslant x\leqslant \psi_2(y),c\leqslant y\leqslant d\}$ ，故有

$$
\begin{array}{l} \iint_ {D} \frac {\partial Q}{\partial x} \mathrm{d} x \mathrm{d} y = \int_ {c} ^ {d} \left[ \int_ {\psi_ {1} (y)} ^ {\psi_ {2} (y)} \frac {\partial Q}{\partial x} \mathrm{d} x \right] \mathrm{d} y = \int_ {c} ^ {d} \left\{Q [ \psi_ {2} (y), y ] - Q [ \psi_ {1} (y), y ] \right\} \mathrm{d} y \\ = \int_ {L _ {2} ^ {\prime}} Q \mathrm{d} y + \int_ {L _ {1} ^ {\prime}} Q \mathrm{d} y = \oint_ {L} Q \mathrm{d} y. \tag {3-3} \\ \end{array}
$$

由于对区域 $D$ ，式(3-2)与(3-3)同时成立，合并后即得公式(3-1).对于如图11-10

所示的区域 D, 完全类似地可证(3-1)成立.

再考虑一般情形.如果闭区域 $D$ 不满足以上条件,那么可以在 $D$ 内引进一条或几条辅助曲线把 $D$ 分成有限个部分闭区域,使得每个部分闭区域都满足上述条件.例如,就图11-11所示的闭区域 $D$ 来说,它的边界曲线 $L$ 为MNPM,引进一条辅助线ABC,

把 D 分成  $D_{1}, D_{2}, D_{3}$  三部分. 应用公式(3-1)于每个部分, 得

$$
\iint_ {D _ {1}} \left(\frac {\partial Q}{\partial x} - \frac {\partial P}{\partial y}\right) \mathrm{d} x \mathrm{d} y = \oint_ {\widehat {M C B A M}} P \mathrm{d} x + Q \mathrm{d} y,
$$

$$
\iint_ {D _ {2}} \left(\frac {\partial Q}{\partial x} - \frac {\partial P}{\partial y}\right) \mathrm{d} x \mathrm{d} y = \oint_ {\widehat {A B P A}} P \mathrm{d} x + Q \mathrm{d} y,
$$

$$
\iint_ {D _ {3}} \left(\frac {\partial Q}{\partial x} - \frac {\partial P}{\partial y}\right) \mathrm{d} x \mathrm{d} y = \oint_ {\widehat {B C N B}} P \mathrm{d} x + Q \mathrm{d} y.
$$

![](images/page_204_image_7.jpg)

<details>
<summary>text_image</summary>

y
A
E₂ P
M
D₁ B
C
D₃ N
O x
</details>

图11-11

把这三个等式相加,注意到相加时沿辅助线来回的曲线积分相互抵消,便得

$$
\iint_ {D} \left(\frac {\partial Q}{\partial x} - \frac {\partial P}{\partial y}\right) \mathrm{d} x \mathrm{d} y = \oint_ {L} P \mathrm{d} x + Q \mathrm{d} y,
$$

其中 L 的方向对 D 来说为正方向. 一般地, 公式(3-1)对于由分段光滑曲线围成的闭区域都成立. 证毕.

注意,对于复连通区域 D,格林公式(3-1)右端应包括沿区域 D 的全部边界的曲线积分,且边界的方向对区域 D 来说都是正向.

下面说明格林公式的一个简单应用.

在公式(3-1)中取 $P = -y, Q = x$，即得

$$
2 \iint_ {D} \mathrm{d} x \mathrm{d} y = \oint_ {L} x \mathrm{d} y - y \mathrm{d} x.
$$

上式左端是闭区域 D 的面积 A 的 2 倍, 因此有

$$
A = \frac {1}{2} \oint_ {L} x \mathrm{d} y - y \mathrm{d} x. \tag {3-4}
$$

例1 计算 $\oint_{L} x^{2} y \mathrm{~d}x - xy^{2} \mathrm{~d}y$，其中 $L$ 为正向圆周 $x^{2} + y^{2} = a^{2}$.

解 令 $P = x^{2}y, Q = -xy^{2}$, 则

$$
\frac {\partial Q}{\partial x} - \frac {\partial P}{\partial y} = - y ^ {2} - x ^ {2}.
$$

因此,由公式(3-1)有

$$
\oint_ {L} x ^ {2} y \mathrm{d} x - x y ^ {2} \mathrm{d} y = - \iint_ {D} (x ^ {2} + y ^ {2}) \mathrm{d} x \mathrm{d} y = - \int_ {0} ^ {2 \pi} \mathrm{d} \theta \int_ {0} ^ {a} \rho^ {3} \mathrm{d} \rho = - \frac {\pi}{2} a ^ {4}.
$$

例2 计算 $\iint_{D} \mathrm{e}^{-y^2} \, \mathrm{d}x \, \mathrm{d}y$，其中 $D$ 是以 $O(0,0), A(1,1), B(0,1)$ 为顶点的三角形闭区域（图11-12）.

解 令 $P = 0, Q = x\mathrm{e}^{-y^2}$, 则

$$
\frac {\partial Q}{\partial x} - \frac {\partial P}{\partial y} = \mathrm{e} ^ {- y ^ {2}}.
$$

因此,由公式(3-1)有

$$
\begin{array}{l} \iint_ {D} \mathrm{e} ^ {- y ^ {2}} \mathrm{d} x \mathrm{d} y = \int_ {O A + A B + B O} x \mathrm{e} ^ {- y ^ {2}} \mathrm{d} y = \int_ {O A} x \mathrm{e} ^ {- y ^ {2}} \mathrm{d} y \\ = \int_ {0} ^ {1} x \mathrm{e} ^ {- x ^ {2}} \mathrm{d} x = \frac {1}{2} (1 - \mathrm{e} ^ {- 1}). \\ \end{array}
$$

![](images/page_205_image_6.jpg)

<details>
<summary>text_image</summary>

y
1
B
A
D
O
1
x
</details>

图11-12

例 3 求椭圆  $x = a \cos \theta, y = b \sin \theta$  所围成图形的面积 A.

解 根据公式(3-4)有

$$
A = \frac {1}{2} \oint_ {L} x \mathrm{d} y - y \mathrm{d} x = \frac {1}{2} \int_ {0} ^ {2 \pi} (a b \cos^ {2} \theta + a b \sin^ {2} \theta) \mathrm{d} \theta = \frac {1}{2} a b \int_ {0} ^ {2 \pi} \mathrm{d} \theta = \pi a b.
$$

例 4 计算  $\oint_{L}\frac{xdy-ydx}{x^{2}+y^{2}}$ ，其中 L 为一条不自相交①、分段光滑且不经过原点的连续闭曲线，L 的方向为逆时针方向.

解 令 $P = \frac{-y}{x^2 + y^2}, Q = \frac{x}{x^2 + y^2}$. 则当 $x^2 + y^2 \neq 0$ 时，有

$$
\frac {\partial Q}{\partial x} = \frac {y ^ {2} - x ^ {2}}{(x ^ {2} + y ^ {2}) ^ {2}} = \frac {\partial P}{\partial y}.
$$

记 L 所围成的闭区域为 D. 当  $(0,0) \notin D$  时, 由公式 (3-1) 便得

$$
\oint_ {L} \frac {x \mathrm{d} y - y \mathrm{d} x}{x ^ {2} + y ^ {2}} = 0;
$$

当 $(0,0)\in D$ 时,选取适当小的r>0,作位于D内的圆周l: $x^{2}+y^{2}=r^{2}$ .记L和l所围成的闭区域为 $D_{1}$ (图11-13).对复连通区域 $D_{1}$ 应用格林公式,得

$$
\oint_ {L} \frac {x \mathrm{d} y - y \mathrm{d} x}{x ^ {2} + y ^ {2}} - \oint_ {l} \frac {x \mathrm{d} y - y \mathrm{d} x}{x ^ {2} + y ^ {2}} = 0,
$$

![](images/page_205_image_18.jpg)

<details>
<summary>text_image</summary>

y
D₁
l
O
r
L
x
</details>

图11-13

其中 l 的方向取逆时针方向. 于是

$$
\oint_ {L} \frac {x \mathrm{d} y - y \mathrm{d} x}{x ^ {2} + y ^ {2}} = \oint_ {l} \frac {x \mathrm{d} y - y \mathrm{d} x}{x ^ {2} + y ^ {2}} = \int_ {0} ^ {2 \pi} \frac {r ^ {2} \cos^ {2} \theta + r ^ {2} \sin^ {2} \theta}{r ^ {2}} \mathrm{d} \theta = 2 \pi .
$$

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 对于连续曲线 $L: x = \varphi(t), y = \psi(t), \alpha \leqslant t \leqslant \beta$，如果除了 $t = \alpha, t = \beta$ 外，当 $t_1 \neq t_2$ 时，$(\varphi(t_1), \psi(t_1))$ 与 $(\varphi(t_2), \psi(t_2))$ 总是相异的，那么称 $L$ 是不自相交的曲线。</span></small>

## 二、平面上曲线积分与路径无关的条件

在物理、力学中要研究所谓势场,就是要研究场力所做的功与路径无关的情形.在

什么条件下场力所做的功与路径无关？这个问题在数学上就是要研究曲线积分与路径无关的条件.为了研究这个问题,先要明确什么叫做曲线积分 $\int_{L}Pdx+Qdy$ 与路径无关.

设 $G$ 是一个区域, $P(x,y)$ 以及 $Q(x,y)$ 在区域 $G$ 内具有一阶连续偏导数. 如果对于 $G$ 内任意指定的两个点 $A,B$ 以及 $G$ 内从点 $A$ 到点 $B$ 的任意两条曲线 $L_{1}, L_{2}$ (图11-14), 等式

![](images/page_206_image_5.jpg)

<details>
<summary>text_image</summary>

y
G
L₂
B
A
L₁
O
x
</details>

图11-14

$$
\int_ {L _ {1}} P \mathrm{d} x + Q \mathrm{d} y = \int_ {L _ {2}} P \mathrm{d} x + Q \mathrm{d} y
$$

恒成立,就说曲线积分 $\int_{L}P\mathrm{d}x + Q\mathrm{d}y$ 在 $G$ 内与路径无关,否则便说与路径有关.

在以上叙述中注意到,如果曲线积分与路径无关,那么

$$
\int_ {L _ {1}} P \mathrm{d} x + Q \mathrm{d} y = \int_ {L _ {2}} P \mathrm{d} x + Q \mathrm{d} y.
$$

由于

$$
\int_ {L _ {2}} P \mathrm{d} x + Q \mathrm{d} y = - \int_ {L _ {2} ^ {-}} P \mathrm{d} x + Q \mathrm{d} y,
$$

所以

$$
\int_ {L _ {1}} P \mathrm{d} x + Q \mathrm{d} y + \int_ {L _ {2} ^ {-}} P \mathrm{d} x + Q \mathrm{d} y = 0,
$$

从而

$$
\oint_ {L _ {1} + L _ {2} ^ {-}} P \mathrm{d} x + Q \mathrm{d} y = 0,
$$

这里 $L_{1} + L_{2}^{-}$ 是一条有向闭曲线. 因此, 在区域 $G$ 内由曲线积分与路径无关可推得在 $G$ 内沿闭曲线的曲线积分为零. 反过来, 如果在区域 $G$ 内沿任意闭曲线的曲线积分为零, 也可推得在 $G$ 内曲线积分与路径无关. 由此得出结论: 曲线积分 $\int_{L} P \mathrm{~d} x + Q \mathrm{~d} y$ 在 $G$ 内与路径无关相当于沿 $G$ 内任意闭曲线 $C$ 的曲线积分 $\oint_{C} P \mathrm{~d} x + Q \mathrm{~d} y$ 等于零.

定理2 设区域 $G$ 是一个单连通区域, 若函数 $P(x, y)$ 与 $Q(x, y)$ 在 $G$ 内具有一阶连续偏导数, 则曲线积分 $\int_{L} P \mathrm{~d}x + Q \mathrm{~d}y$ 在 $G$ 内与路径无关 (或沿 $G$ 内任意闭曲线的曲线积分为零) 的充分必要条件是

$$
\frac {\partial P}{\partial y} = \frac {\partial Q}{\partial x} \tag {3-5}
$$

在 $G$ 内恒成立.

证 先证条件(3-5)是充分的.在 $G$ 内任取一条闭曲线 $C$, 要证当条件(3-5)成立时有 $\oint_{C} P \mathrm{~d} x + Q \mathrm{~d} y = 0$. 因为 $G$ 是单连通的, 所以闭曲线 $C$ 所围成的闭区域 $D$ 全部在 $G$ 内, 于是(3-5)式在 $D$ 上恒成立. 应用格林公式, 有

$$
\iint_ {D} \left(\frac {\partial Q}{\partial x} - \frac {\partial P}{\partial y}\right) \mathrm{d} x \mathrm{d} y = \oint_ {C} P \mathrm{d} x + Q \mathrm{d} y.
$$

上式左端的二重积分等于零（因为被积函数 $\frac{\partial Q}{\partial x} -\frac{\partial P}{\partial y}$ 在 $D$ 上恒为零），从而右端的曲线积分也等于零.

再证条件(3-5)是必要的.现在要证的是:如果沿G内任意闭曲线的曲线积分为零,那么(3-5)式在G内恒成立.用反证法来证.假设上述论断不成立,那么G内至少有一点 $M_{0}$ ,使

$$
\left(\frac {\partial Q}{\partial x} - \frac {\partial P}{\partial y}\right) _ {M _ {0}} \neq 0.
$$

不妨假定

$$
\left(\frac {\partial Q}{\partial x} - \frac {\partial P}{\partial y}\right) _ {M _ {0}} = \eta > 0.
$$

由于 $\frac{\partial P}{\partial y}$ 与 $\frac{\partial Q}{\partial x}$ 在G内连续,可以在G内取得一个以 $M_{0}$ 为圆心、半径足够小的圆形闭区域K,使得在K上恒有

$$
\frac {\partial Q}{\partial x} - \frac {\partial P}{\partial y} \geqslant \frac {\eta}{2}.
$$

于是由格林公式及二重积分的性质就有

$$
\oint_ {\gamma} P \mathrm{d} x + Q \mathrm{d} y = \iint_ {K} \left(\frac {\partial Q}{\partial x} - \frac {\partial P}{\partial y}\right) \mathrm{d} x \mathrm{d} y \geqslant \frac {\eta}{2} \cdot \sigma ,
$$

这里 $\gamma$ 是 $K$ 的正向边界曲线, $\sigma$ 是 $K$ 的面积. 因为 $\eta > 0, \sigma > 0$, 从而

$$
\oint_ {\gamma} P \mathrm{d} x + Q \mathrm{d} y > 0.
$$

这结果与沿 $G$ 内任意闭曲线的曲线积分为零的假定相矛盾，可见 $G$ 内使(3-5)式不成立的点不可能存在，即(3-5)式在 $G$ 内处处成立.证毕.

在第二节第二目例3中我们看到，起点与终点相同的三个曲线积分 $\int_{L}2xy\mathrm{d}x + x^{2}\mathrm{d}y$相等.由定理2来看,这不是偶然的,因为这里 $\frac{\partial Q}{\partial x}=\frac{\partial P}{\partial y}=2x$ 在整个xOy面内恒成立,而整个xOy面是单连通区域,因此曲线积分 $\int_{L}2xydx+x^{2}dy$ 与路径无关.

在定理2中,要求区域G是单连通区域,且函数 $P(x,y)$ 与 $Q(x,y)$ 在G内具有一阶连续偏导数.如果这两个条件之一不能满足,那么定理的结论不能保证成立.例如,在例4中我们已经看到,当L所围成的区域含有原点时,虽然除去原点外,恒有 $\frac{\partial Q}{\partial x}=\frac{\partial P}{\partial y}$ ,但沿闭曲线的积分 $\oint_{L}Pdx+Qdy\neq0$ ,其原因在于区域内含有破坏函数P,Q及 $\frac{\partial Q}{\partial x}$ , $\frac{\partial P}{\partial y}$ 连续性条件的点O,这种点通常称为奇点.

## 三、二元函数的全微分求积

现在要讨论:函数  $P(x,y)$  与  $Q(x,y)$  满足什么条件时,表达式  $P(x,y)\mathrm{d}x+Q(x,y)\mathrm{d}y$  才是某个二元函数  $u(x,y)$  的全微分;当这样的二元函数存在时把它求出来.

定理3 设区域 $G$ 是一个单连通区域, 若函数 $P(x, y)$ 与 $Q(x, y)$ 在 $G$ 内具有一阶连续偏导数, 则 $P(x, y) \mathrm{d}x + Q(x, y) \mathrm{d}y$ 在 $G$ 内为某一函数 $u(x, y)$ 的全微分的充分必要条件是

$$
\frac {\partial P}{\partial y} = \frac {\partial Q}{\partial x} \tag {3-5}
$$

在 $G$ 内恒成立.

证 先证必要性. 假设存在着某一函数 $u(x, y)$, 使得

$$
\mathrm{d} u = P (x, y) \mathrm{d} x + Q (x, y) \mathrm{d} y,
$$

则必有

$$
\frac {\partial u}{\partial x} = P (x, y), \quad \frac {\partial u}{\partial y} = Q (x, y).
$$

从而

$$
\frac {\partial^ {2} u}{\partial x \partial y} = \frac {\partial P}{\partial y}, \quad \frac {\partial^ {2} u}{\partial y \partial x} = \frac {\partial Q}{\partial x}.
$$

由于 $P$ 与 $Q$ 具有一阶连续偏导数，所以 $\frac{\partial^2 u}{\partial x \partial y}$ 与 $\frac{\partial^2 u}{\partial y \partial x}$ 连续，因此 $\frac{\partial^2 u}{\partial x \partial y} = \frac{\partial^2 u}{\partial y \partial x}$，即 $\frac{\partial P}{\partial y} = \frac{\partial Q}{\partial x}$. 这就证明了条件(3-5)是必要的.

再证充分性. 设已知条件(3-5)在 $G$ 内恒成立, 则由定理2可知, 起点为 $M_0(x_0, y_0)$, 终点为 $M(x, y)$ 的曲线积分在区域 $G$ 内与路径无关, 于是可把这条曲线积

分写作

$$
\int_ {(x _ {0}, y _ {0})} ^ {(x, y)} P (x, y) \mathrm{d} x + Q (x, y) \mathrm{d} y.
$$

当起点 $M_0(x_0, y_0)$ 固定时，这个积分的值取决于终点 $M(x, y)$，因此，它与 $x$ 及 $y$ 构成函数关系，把这个函数记作 $u(x, y)$，即

$$
u (x, y) = \int_ {(x _ {0}, y _ {0})} ^ {(x, y)} P (x, y) \mathrm{d} x + Q (x, y) \mathrm{d} y ①. \tag {3-6}
$$

下面来证明这个函数 $u(x,y)$ 的全微分就是 $P(x,y)\mathrm{d}x + Q(x,y)\mathrm{d}y.$ 因为 $P(x,y)$ 与$Q(x,y)$ 都是连续的，因此只要证明

$$
\frac {\partial u}{\partial x} = P (x, y), \quad \frac {\partial u}{\partial y} = Q (x, y).
$$

按偏导数的定义,有

$$
\frac {\partial u}{\partial x} = \lim _ {\Delta x \to 0} \frac {u (x + \Delta x , y) - u (x , y)}{\Delta x}.
$$

由(3-6)式,得

$$
u (x + \Delta x, y) = \int_ {(x _ {0}, y _ {0})} ^ {(x + \Delta x, y)} P (x, y) \mathrm{d} x + Q (x, y) \mathrm{d} y.
$$

由于这里的曲线积分与路径无关,可以取先从点  $M_{0}$  到点 M,然后沿平行于 x 轴的直线段从点 M 到点 N 作为上式右端曲线积分的路径(图 11-15).这样就有

$$
\begin{array}{l} u (x + \Delta x, y) \\ = u (x, y) + \int_ {(x, y)} ^ {(x + \Delta x, y)} P (x, y) \mathrm{d} x + Q (x, y) \mathrm{d} y. \\ \end{array}
$$

从而

![](images/page_209_image_14.jpg)

<details>
<summary>text_image</summary>

y
M(x,y)
N(x+Δx,y)
M₀(x₀,y₀)
G
O
x
</details>

图11-15

$$
u (x + \Delta x, y) - u (x, y) = \int_ {(x, y)} ^ {(x + \Delta x, y)} P (x, y) \mathrm{d} x + Q (x, y) \mathrm{d} y.
$$

因为直线段 MN 的方程为 y=常数, 按对坐标的曲线积分的计算法, 上式成为

$$
u (x + \Delta x, y) - u (x, y) = \int_ {x} ^ {x + \Delta x} P (x, y) \mathrm{d} x.
$$

应用定积分中值定理,得

$$
u (x + \Delta x, y) - u (x, y) = P (x + \theta \Delta x, y) \Delta x \quad (0 \leqslant \theta \leqslant 1).
$$

上式两端除以 $\Delta x$，并令 $\Delta x \to 0$ 取极限。由于 $P(x, y)$ 的偏导数在 $G$ 内连续，$P(x, y)$ 本身也一定连续，于是得

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 为区别函数的自变量与积分变量, 可记</span></small>

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">$u(x,y) = \int_{(x_0,y_0)}^{(x,y)}P(s,t)\mathrm{d}s + Q(s,t)\mathrm{d}t.$</span></small>

$$
\frac {\partial u}{\partial x} = P (x, y).
$$

同理可证

$$
\frac {\partial u}{\partial y} = Q (x, y).
$$

这就证明了条件(3-5)是充分的.证毕.

由定理 2 及定理 3, 立即可得如下推论:

推论 设区域 $G$ 是一个单连通区域, 若函数 $P(x, y)$ 与 $Q(x, y)$ 在 $G$ 内具有一阶连续偏导数, 则曲线积分 $\int_{L} P \mathrm{~d} x + Q \mathrm{~d} y$ 在 $G$ 内与路径无关的充分必要条件是: 在 $G$ 内存在函数 $u(x, y)$, 使 $\mathrm{d} u = P \mathrm{~d} x + Q \mathrm{~d} y$.

根据上述定理,如果函数  $P(x,y)$  与  $Q(x,y)$  在单连通区域 G 内具有一阶连续偏导数,且满足条件(3-5),那么  $Pdx+Qdy$  是某个函数的全微分,这函数可用公式(3-6)来求出.因为公式(3-6)中的曲线积分与路径无关,为计算简便起见,可以选择平行于坐标轴的直线段连成的折线  $M_{0}RM$  或  $M_{0}SM$  作为积分路线(图11-16),当然要假定这些折线完全位于 G 内.

![](images/page_210_image_8.jpg)

<details>
<summary>text_image</summary>

y
S(x₀,y) M(x,y)
M₀(x₀,y₀) R(x,y₀)
O x
</details>

图11-16

在公式(3-6)中取 $M_{0}RM$ 为积分路线,得

$$
u (x, y) = \int_ {x _ {0}} ^ {x} P (x, y _ {0}) \mathrm{d} x + \int_ {y _ {0}} ^ {y} Q (x, y) \mathrm{d} y.
$$

在公式(3-6)中取 $M_0SM$ 为积分路线, 则函数 $u$ 也可表为

$$
u (x, y) = \int_ {y _ {0}} ^ {y} Q (x _ {0}, y) \mathrm{d} y + \int_ {x _ {0}} ^ {x} P (x, y) \mathrm{d} x.
$$

例 5 验证: $\frac{xdy-ydx}{x^{2}+y^{2}}$ 在右半平面(x>0)内是某个函数的全微分,并求出一个这样的函数.

解 在例 4 中已经知道,令

$$
P = \frac {- y}{x ^ {2} + y ^ {2}}, \quad Q = \frac {x}{x ^ {2} + y ^ {2}},
$$

就有

$$
\frac {\partial P}{\partial y} = \frac {y ^ {2} - x ^ {2}}{(x ^ {2} + y ^ {2}) ^ {2}} = \frac {\partial Q}{\partial x}
$$

在右半平面内恒成立,因此在右半平面内, $\frac{xdy-ydx}{x^{2}+y^{2}}$ 是某个函数的全微分.

取积分路线如图 11-17 所示, 利用公式(3-6) 得所求函数为

$$
\begin{array}{l} u (x, y) = \int_ {(1, 0)} ^ {(x, y)} \frac {x \mathrm{d} y - y \mathrm{d} x}{x ^ {2} + y ^ {2}} = \int_ {A B} \frac {x \mathrm{d} y - y \mathrm{d} x}{x ^ {2} + y ^ {2}} + \int_ {B C} \frac {x \mathrm{d} y - y \mathrm{d} x}{x ^ {2} + y ^ {2}} \\ = 0 + \int_ {0} ^ {y} \frac {x \mathrm{d} y}{x ^ {2} + y ^ {2}} = \left[ \arctan \frac {y}{x} \right] _ {0} ^ {y} = \arctan \frac {y}{x}. \\ \end{array}
$$

例 6 验证: 在整个 xOy 面内,  $xy^{2}dx + x^{2}ydy$  是某个函数的全微分, 并求出一个这样的函数.

解 现在 $P = xy^2, Q = x^2y$，且

$$
\frac {\partial P}{\partial y} = 2 x y = \frac {\partial Q}{\partial x}
$$

在整个 xOy 面内恒成立, 因此在整个 xOy 面内,  $xy^{2}dx + x^{2}ydy$  是某个函数的全微分. 取积分路线如图 11-18 所示, 利用公式 (3-6) 得所求函数为

$$
\begin{array}{l} u (x, y) = \int_ {(0, 0)} ^ {(x, y)} x y ^ {2} \mathrm{d} x + x ^ {2} y \mathrm{d} y = \int_ {O A} x y ^ {2} \mathrm{d} x + x ^ {2} y \mathrm{d} y + \int_ {A B} x y ^ {2} \mathrm{d} x + x ^ {2} y \mathrm{d} y \\ = 0 + \int_ {0} ^ {y} x ^ {2} y \mathrm{d} y = x ^ {2} \int_ {0} ^ {y} y \mathrm{d} y = \frac {x ^ {2} y ^ {2}}{2}. \\ \end{array}
$$

![](images/page_211_image_7.jpg)

<details>
<summary>text_image</summary>

y
C(x,y)
O A(1,0) B(x,0) x
</details>

图11-17

![](images/page_211_image_9.jpg)

<details>
<summary>text_image</summary>

y
B(x,y)
O
A(x,0)
x
</details>

图11-18

\* 全微分方程

利用二元函数的全微分求积,还可以用来求解下面一类一阶微分方程.

一个微分方程写成

$$
P (x, y) \mathrm{d} x + Q (x, y) \mathrm{d} y = 0 \tag {3-7}
$$

的形式后,如果它的左端恰好是某一个函数  $u(x,y)$  的全微分:

$$
\mathrm{d} u (x, y) = P (x, y) \mathrm{d} x + Q (x, y) \mathrm{d} y,
$$

那么方程(3-7)就叫做全微分方程.

容易知道,如果方程(3-7)的左端是函数 $u(x,y)$ 的全微分,那么

$$
u (x, y) = C
$$

就是全微分方程(3-7)的隐式通解,其中 C 是任意常数.

由定理3及公式(3-6)可知,当 $P(x,y)$ 与 $Q(x,y)$ 在单连通区域G内具有一阶连续偏导数时,方程(3-7)成为全微分方程的充分必要条件是

$$
\frac {\partial P}{\partial y} = \frac {\partial Q}{\partial x}
$$

在区域 $G$ 内恒成立，且当此条件满足时，全微分方程(3-7)的通解为

$$
u (x, y) \equiv \int_ {(x _ {0}, y _ {0})} ^ {(x, y)} P (x, y) \mathrm{d} x + Q (x, y) \mathrm{d} y = C, \tag {3-8}
$$

其中 $x_0$ 与 $y_0$ 是在区域 $G$ 内适当选定的点 $M_0$ 的坐标.

例7 求解方程

$$
(5 x ^ {4} + 3 x y ^ {2} - y ^ {3}) \mathrm{d} x + (3 x ^ {2} y - 3 x y ^ {2} + y ^ {2}) \mathrm{d} y = 0.
$$

解 设 $P(x,y) = 5x^{4} + 3xy^{2} - y^{3}, Q(x,y) = 3x^{2}y - 3xy^{2} + y^{2}$, 则

$$
\frac {\partial P}{\partial y} = 6 x y - 3 y ^ {2} = \frac {\partial Q}{\partial x},
$$

因此,所给方程是全微分方程.

取 $x_0 = 0, y_0 = 0$，根据公式(3-8)，有

$$
\begin{array}{l} u (x, y) = \int_ {(0, 0)} ^ {(x, y)} \left(5 x ^ {4} + 3 x y ^ {2} - y ^ {3}\right) \mathrm{d} x + \left(3 x ^ {2} y - 3 x y ^ {2} + y ^ {2}\right) \mathrm{d} y \\ = \int_ {0} ^ {x} 5 x ^ {4} \mathrm{d} x + \int_ {0} ^ {y} (3 x ^ {2} y - 3 x y ^ {2} + y ^ {2}) \mathrm{d} y = x ^ {5} + \frac {3}{2} x ^ {2} y ^ {2} - x y ^ {3} + \frac {1}{3} y ^ {3}. \\ \end{array}
$$

于是,方程的通解为

$$
x ^ {5} + \frac {3}{2} x ^ {2} y ^ {2} - x y ^ {3} + \frac {1}{3} y ^ {3} = C.
$$

除了利用公式(3-8)以外,还可以用下面的方法求解全微分方程.

以上面的方程为例.因为要求的方程通解为 $u(x,y) = C$ ，其中 $u(x,y)$ 满足

$$
\frac {\partial u}{\partial x} = 5 x ^ {4} + 3 x y ^ {2} - y ^ {3},
$$

故

$$
u (x, y) = \int (5 x ^ {4} + 3 x y ^ {2} - y ^ {3}) \mathrm{d} x = x ^ {5} + \frac {3}{2} x ^ {2} y ^ {2} - x y ^ {3} + \varphi (y),
$$

这里 $\varphi(y)$ 是以 $y$ 为自变量的待定函数. 由此, 得

$$
\frac {\partial u}{\partial y} = 3 x ^ {2} y - 3 x y ^ {2} + \varphi^ {\prime} (y).
$$

又 $u(x,y)$ 必须满足

$$
\frac {\partial u}{\partial y} = 3 x ^ {2} y - 3 x y ^ {2} + y ^ {2}.
$$

故

$$
3 x ^ {2} y - 3 x y ^ {2} + \varphi^ {\prime} (y) = 3 x ^ {2} y - 3 x y ^ {2} + y ^ {2}.
$$

从而

$$
\varphi^ {\prime} (y) = y ^ {2}, \quad \varphi (y) = \frac {1}{3} y ^ {3} + C.
$$

所以,所给方程的通解为

$$
x ^ {5} + \frac {3}{2} x ^ {2} y ^ {2} - x y ^ {3} + \frac {1}{3} y ^ {3} = C.
$$

## \* 四、曲线积分的基本定理

若曲线积分  $\int_{L} F \cdot dr$  在区域 G 内与积分路径无关, 则称向量场 F 为保守场.

下面的定理给出了平面曲线积分与路径无关的另一种形式的条件,并为计算保守场中的曲线积分提供了一种简便的方法.

定理4（曲线积分的基本定理）设 $F(x,y) = P(x,y)i + Q(x,y)j$ 是平面区域 $G$ 内的一个向量场，若 $P(x,y)$ 与 $Q(x,y)$ 都在 $G$ 内连续，且存在一个数量函数 $f(x,y)$，使得 $F = \nabla f$，则曲线积分 $\int_{L} F \cdot \mathrm{d}r$ 在 $G$ 内与路径无关，且

$$
\int_ {L} \boldsymbol {F} \cdot \mathrm{d} \boldsymbol {r} = f (B) - f (A), \tag {3-9}
$$

其中 L 是位于 G 内起点为 A、终点为 B 的任一分段光滑曲线.

证 设 $L$ 的向量方程为

$$
r = \varphi (t) i + \psi (t) j, \quad t \in [ \alpha , \beta ],
$$

起点 A 对应参数  $t=\alpha$ ，终点 B 对应参数  $t=\beta$ .

由假设， $f_{x}=P,f_{y}=Q,P,Q$  连续，从而f可微，且

$$
\frac {\mathrm{d} f}{\mathrm{d} t} = f _ {x} \frac {\mathrm{d} x}{\mathrm{d} t} + f _ {y} \frac {\mathrm{d} y}{\mathrm{d} t} = \nabla f \cdot \left(\frac {\mathrm{d} x}{\mathrm{d} t} i + \frac {\mathrm{d} y}{\mathrm{d} t} j\right) = F \cdot \frac {\mathrm{d} r}{\mathrm{d} t},
$$

于是

$$
\int_ {L} \boldsymbol {F} \cdot \mathrm{d} \boldsymbol {r} = \int_ {\alpha} ^ {\beta} \boldsymbol {F} \cdot \frac {\mathrm{d} \boldsymbol {r}}{\mathrm{d} t} \mathrm{d} t = \int_ {\alpha} ^ {\beta} \frac {\mathrm{d} f}{\mathrm{d} t} \mathrm{d} t = f [ \varphi (t), \psi (t) ] \Bigg | _ {\alpha} ^ {\beta} = f (B) - f (A),
$$

证毕.

定理 4 表明, 对于势场 F, 曲线积分  $\int_{L} F \cdot dr$  的值仅依赖于它的势函数 f 在路径 L 的两端点的值, 而不依赖于两点间的路径, 即积分  $\int_{L} F \cdot dr$  在 G 内与路径无关. 也就是说: 势场是保守场.

公式(3-9)是与微积分基本公式

$$
\int_ {a} ^ {b} f (x) \mathrm{d} x = F (b) - F (a)
$$

(其中  $F'(x)=f(x)$ ) 完全类似的向量微积分的相应公式, 称为曲线积分的基本公式.

## 习题11-3

1. 计算下列曲线积分,并验证格林公式的正确性:

(1) $\oint_{L}(2xy - x^{2})\mathrm{d}x + (x + y^{2})\mathrm{d}y$ ，其中 $L$ 是由抛物线 $y = x^{2}$ 和 $y^{2} = x$ 所围成的区域的正向边界曲线；
(2) $\oint_{L} (x^{2} - xy^{3}) \mathrm{d}x + (y^{2} - 2xy) \mathrm{d}y$，其中 $L$ 是四个顶点分别为 $(0,0)$，$(2,0)$，$(2,2)$ 和 $(0,2)$ 的正方形区域的正向边界.

2. 利用曲线积分,求下列曲线所围成的图形的面积:

(1) 星形线  $x = a \cos^{3} t, y = a \sin^{3} t;$
(2) 椭圆  $9x^{2}+16y^{2}=144$ ;
(3) 圆  $x^{2}+y^{2}=2ax.$

3. 计算曲线积分 $\oint_{L} \frac{y \, \mathrm{d}x - x \, \mathrm{d}y}{2(x^2 + y^2)}$, 其中 $L$ 为圆周 $(x-1)^2 + y^2 = 2, L$ 的方向为逆时针方向.

4. 确定正向闭曲线 $C$，使曲线积分 $\oint_{C} \left(x + \frac{y^3}{3}\right) \mathrm{d}x + \left(y + x - \frac{2}{3} x^3\right) \mathrm{d}y$ 达到最大值.

5. 设 n 边形的 n 个顶点按逆时针方向依次为  $M_{1}(x_{1}, y_{1}), M_{2}(x_{2}, y_{2}), \cdots, M_{n}(x_{n}, y_{n})$ . 试利用曲线积分证明此 n 边形的面积为

$$
A = \frac {1}{2} \big [ (x _ {1} y _ {2} - x _ {2} y _ {1}) + (x _ {2} y _ {3} - x _ {3} y _ {2}) + \dots + (x _ {n - 1} y _ {n} - x _ {n} y _ {n - 1}) + (x _ {n} y _ {1} - x _ {1} y _ {n}) \big ].
$$

6. 证明下列曲线积分在整个 xOy 面内与路径无关, 并计算积分值:

(1) $\int_{(1,1)}^{(2,3)} (x + y) \, \mathrm{d}x + (x - y) \, \mathrm{d}y$;
(2) $\int_{(1,2)}^{(3,4)} (6xy^2 - y^3) \, \mathrm{d}x + (6x^2y - 3xy^2) \, \mathrm{d}y$;
(3) $\int_{(1,0)}^{(2,1)} (2xy - y^4 + 3) \, \mathrm{d}x + (x^2 - 4xy^3) \, \mathrm{d}y.$

7. 利用格林公式, 计算下列曲线积分:

(1) $\oint_{L}(2x - y + 4)\mathrm{d}x + (5y + 3x - 6)\mathrm{d}y$ ，其中 $L$ 是三顶点分别为(0,0)，(3,0)和(3,2)的三角形正向边界；

(2) $\oint_{L} (x^{2}y\cos x + 2xy\sin x - y^{2}e^{x}) \, \mathrm{d}x + (x^{2}\sin x - 2ye^{x}) \, \mathrm{d}y$，其中 $L$ 为正向星形线 $x^{\frac{2}{3}} + y^{\frac{2}{3}} = a^{\frac{2}{3}}$ ($a > 0$);

(3) $\int_{L} (2xy^{3} - y^{2}\cos x) \, \mathrm{d}x + (1 - 2y\sin x + 3x^{2}y^{2}) \, \mathrm{d}y$，其中 $L$ 为在抛物线 $2x = \pi y^{2}$ 上由点 $(0,0)$ 到 $\left(\frac{\pi}{2}, 1\right)$ 的一段弧；

(4) $\int_{L}(x^{2} - y)\mathrm{d}x - (x + \sin^{2}y)\mathrm{d}y$ ，其中 $L$ 是在圆周 $y = \sqrt{2x - x^2}$ 上由点(0,0)到点(1,1)的一段弧.

8. 设有界闭区域 $D$ 由 $xOy$ 面上的分段光滑曲线 $L$ 所围成, 函数 $u = u(x, y)$ 在 $D$ 上具有连续的二

阶偏导数, $\frac{\partial u}{\partial n}$ 表示 $u(x,y)$ 沿L的外法向量的方向导数,证明

$$
\oint_ {L} \frac {\partial u}{\partial n} \mathrm{d} s = \iint_ {D} \left(\frac {\partial^ {2} u}{\partial x ^ {2}} + \frac {\partial^ {2} u}{\partial y ^ {2}}\right) \mathrm{d} \sigma ,
$$

其中 $L$ 取正向.

9. 验证下列 $P(x, y) \mathrm{d}x + Q(x, y) \mathrm{d}y$ 在整个 $xOy$ 面内是某一函数 $u(x, y)$ 的全微分，并求这样的一个 $u(x, y)$:

(1) $(x+2y)\mathrm{d}x+(2x+y)\mathrm{d}y;$

(2) $2xy\mathrm{d}x+x^{2}\mathrm{d}y;$

(3)  $4\sin x\sin 3y\cos xdx - 3\cos 3y\cos 2xdy;$

(4) $(3x^{2}y + 8xy^{2})\mathrm{d}x + (x^{3} + 8x^{2}y + 12ye^{y})\mathrm{d}y;$

(5) $(2x\cos y+y^{2}\cos x)\mathrm{d}x+(2y\sin x-x^{2}\sin y)\mathrm{d}y.$

10. 设有一变力在坐标轴上的投影为 $X = x^{2} + y^{2}, Y = 2xy - 8$，这变力确定了一个力场。证明质点在此场内移动时，场力所做的功与路径无关。

\*11. 判别下列方程中哪些是全微分方程？对于全微分方程，求出它的通解.

(1) $(3x^{2}+6xy^{2})\mathrm{d}x+(6x^{2}y+4y^{2})\mathrm{d}y=0;$

(2) $(a^{2}-2xy-y^{2})\mathrm{d}x-(x+y)^{2}\mathrm{d}y=0$  (a为常数);

(3)  $e^{y}dx+(xe^{y}-2y)dy=0;$

(4) $(x\cos y + \cos x)y' - y\sin x + \sin y = 0;$

(5) $(x^{2}-y)\mathrm{d}x-x\mathrm{d}y=0;$

(6) $y(x-2y)\mathrm{d}x-x^{2}\mathrm{d}y=0;$

(7) $(1+e^{2\theta})d\rho+2\rho e^{2\theta}d\theta=0;$

(8) $(x^{2}+y^{2})dx+xydy=0.$

12. 确定常数 $\lambda$, 使在右半平面 $x > 0$ 上的向量 $A(x, y) = 2xy(x^4 + y^2)^{\lambda}i - x^2(x^4 + y^2)^{\lambda}j$ 为某二元函数 $u(x, y)$ 的梯度, 并求 $u(x, y)$.

## 第四节 对面积的曲面积分

## 一、对面积的曲面积分的概念与性质

在本章第一节第一目的质量问题中,如果把曲线改为曲面①,并相应地把线密度  $\mu(x,y)$  改为面密度  $\mu(x,y,z)$ , 小段曲线的弧长  $\Delta s_{i}$  改为小块曲面的面积  $\Delta S_{i}$ , 而第 i 小段曲线上的一点  $(\xi_{i},\eta_{i})$  改为第 i 小块曲面上的一点  $(\xi_{i},\eta_{i},\zeta_{i})$ , 那么, 在面密度  $\mu(x,y,z)$  连续的前提下, 所求的质量 m 就是下列和的极限:

$$
m = \lim _ {\lambda \to 0} \sum_ {i = 1} ^ {n} \mu (\xi_ {i}, \eta_ {i}, \zeta_ {i}) \Delta S _ {i},
$$

其中  $\lambda$  表示 n 小块曲面的直径②的最大值.

这样的极限还会在其他问题中遇到. 抽去它们的具体意义, 就得出对面积的曲面

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 以后都假定曲面的边界曲线是分段光滑的闭曲线,且曲面有界.</span></small>

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">② 曲面的直径是指曲面上任意两点间距离的最大者.</span></small>

积分的概念.

定义 设曲面  $\Sigma$  是光滑的①, 函数  $f(x,y,z)$  在  $\Sigma$  上有界. 把  $\Sigma$  任意分成 n 小块  $\Delta S_{i}$  ( $\Delta S_{i}$  同时也代表第 i 小块曲面的面积), 设  $(\xi_{i},\eta_{i},\zeta_{i})$  是  $\Delta S_{i}$  上任意取定的一点, 作乘积  $f(\xi_{i},\eta_{i},\zeta_{i})\Delta S_{i}$  ( $i=1,2,3,\cdots,n$ ), 并作和  $\sum_{i=1}^{n}f(\xi_{i},\eta_{i},\zeta_{i})\Delta S_{i}$ , 如果当各小块曲面的直径的最大值  $\lambda\to0$  时, 这和的极限总存在, 且与曲面  $\Sigma$  的分法及点  $(\xi_{i},\eta_{i},\zeta_{i})$  的取法无关, 那么称此极限为函数  $f(x,y,z)$  在曲面  $\Sigma$  上对面积的曲面积分或第一类曲面积分, 记作  $\iint_{\Sigma}f(x,y,z)\mathrm{d}S$ , 即

$$
\iint_ {\Sigma} f (x, y, z) \mathrm{d} S = \lim _ {\lambda \to 0} \sum_ {i = 1} ^ {n} f (\xi_ {i}, \eta_ {i}, \zeta_ {i}) \Delta S _ {i},
$$

其中 $f(x,y,z)$ 叫做被积函数，$\Sigma$ 叫做积分曲面.

我们指出, 当 $f(x, y, z)$ 在光滑曲面 $\Sigma$ 上连续时, 对面积的曲面积分是存在的. 今后总假定 $f(x, y, z)$ 在 $\Sigma$ 上连续.

根据上述定义,面密度为连续函数  $\mu(x,y,z)$  的光滑曲面  $\Sigma$  的质量 m, 可表示为  $\mu(x,y,z)$  在  $\Sigma$  上对面积的曲面积分

$$
m = \iint_ {\Sigma} \mu (x, y, z)   \mathrm{d} S.
$$

如果 $\Sigma$ 是分片光滑的②, 我们规定函数在 $\Sigma$ 上对面积的曲面积分等于函数在光滑的各片曲面上对面积的曲面积分之和. 例如, 设 $\Sigma$ 可分成两片光滑曲面 $\Sigma_{1}$ 及 $\Sigma_{2}$ (记作 $\Sigma = \Sigma_{1} + \Sigma_{2}$), 就规定

$$
\iint_ {\Sigma_ {1} + \Sigma_ {2}} f (x, y, z) \mathrm{d} S = \iint_ {\Sigma_ {1}} f (x, y, z) \mathrm{d} S + \iint_ {\Sigma_ {2}} f (x, y, z) \mathrm{d} S.
$$

由对面积的曲面积分的定义可知,它具有与对弧长的曲线积分相类似的性质,这里不再赘述.

## 二、对面积的曲面积分的计算法

设积分曲面 $\Sigma$ 由方程 $z = z(x, y)$ 给出，$\Sigma$ 在 $xOy$ 面上的投影区域为 $D_{xy}$（图11-19），函数 $z = z(x, y)$ 在 $D_{xy}$ 上具有连续偏导数，被积函数 $f(x, y, z)$ 在 $\Sigma$ 上连续.

按对面积的曲面积分的定义,有

![](images/page_216_image_14.jpg)

<details>
<summary>text_image</summary>

z
Σ: z=z(x,y)
(ξᵢ, ηᵢ, ξᵢ)
ΔSᵢ
O
y
x
(ξᵢ, ηᵢ, 0)
Dₓᵧ
(Δσᵢ)ₓᵧ
</details>

图11-19

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 所谓曲面是光滑的, 就是说, 曲面上各点处都具有切平面, 且当点在曲面上连续移动时, 切平面也连续转动.</span></small>

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">② 分片光滑的曲面是指由有限个光滑曲面所组成的曲面.以后我们总假定曲面是光滑的或分片光滑的.</span></small>

$$
\iint_ {\Sigma} f (x, y, z) \mathrm{d} S = \lim _ {\lambda \rightarrow 0} \sum_ {i = 1} ^ {n} f (\xi_ {i}, \eta_ {i}, \zeta_ {i}) \Delta S _ {i}. \tag {4-1}
$$

设 $\Sigma$ 上第 $i$ 小块曲面 $\Delta S_{i}$ （它的面积也记作 $\Delta S_{i}$）在 $xOy$ 面上的投影区域为 $(\Delta \sigma_{i})_{xy}$（它的面积也记作 $(\Delta \sigma_{i})_{xy}$），则(4-1)式中的 $\Delta S_{i}$ 可表示为二重积分

$$
\Delta S _ {i} = \iint_ {(\Delta \sigma_ {i}) _ {x y}} \sqrt {1 + z _ {x} ^ {2} (x , y) + z _ {y} ^ {2} (x , y)} \mathrm{d} x \mathrm{d} y.
$$

利用二重积分的中值定理,上式又可写成

$$
\Delta S _ {i} = \sqrt {1 + z _ {x} ^ {2} (\xi_ {i} ^ {\prime} , \eta_ {i} ^ {\prime}) + z _ {y} ^ {2} (\xi_ {i} ^ {\prime} , \eta_ {i} ^ {\prime})} (\Delta \sigma_ {i}) _ {x y},
$$

其中 $(\xi_i', \eta_i', 0)$ 是小闭区域 $(\Delta \sigma_i)_{xy}$ 上的一点. 又因 $(\xi_i, \eta_i, \zeta_i)$ 是 $\Sigma$ 上的一点, 故 $\zeta_i = z(\xi_i, \eta_i)$, 这里 $(\xi_i, \eta_i, 0)$ 也是小闭区域 $(\Delta \sigma_i)_{xy}$ 上的点. 于是

$$
\sum_ {i = 1} ^ {n} f (\xi_ {i}, \eta_ {i}, \zeta_ {i}) \Delta S _ {i} = \sum_ {i = 1} ^ {n} f [ \xi_ {i}, \eta_ {i}, z (\xi_ {i}, \eta_ {i}) ] \sqrt {1 + z _ {x} ^ {2} (\xi_ {i} ^ {\prime} , \eta_ {i} ^ {\prime}) + z _ {y} ^ {2} (\xi_ {i} ^ {\prime} , \eta_ {i} ^ {\prime})} (\Delta \sigma_ {i}) _ {x y}.
$$

由于函数 $f[x,y,z(x,y)]$ 以及函数 $\sqrt{1 + z_x^2(x,y) + z_y^2(x,y)}$ 都在闭区域 $D_{xy}$ 上连续，可以证明，当 $\lambda \to 0$ 时，上式右端的极限与

$$
\sum_ {i = 1} ^ {n} f [ \xi_ {i}, \eta_ {i}, z (\xi_ {i}, \eta_ {i}) ] \sqrt {1 + z _ {x} ^ {2} (\xi_ {i} , \eta_ {i}) + z _ {y} ^ {2} (\xi_ {i} , \eta_ {i})} (\Delta \sigma_ {i}) _ {x y}
$$

的极限相等.这个极限在本目开始所给的条件下是存在的,它等于二重积分

$$
\iint_ {D _ {x y}} f [ x, y, z (x, y) ] \sqrt {1 + z _ {x} ^ {2} (x , y) + z _ {y} ^ {2} (x , y)} \mathrm{d} x \mathrm{d} y,
$$

因此左端的极限即曲面积分 $\iint_{\Sigma} f(x, y, z) \, \mathrm{d}S$ 也存在，且有

$$
\iint_ {\Sigma} f (x, y, z) \mathrm{d} S = \iint_ {D _ {x y}} f [ x, y, z (x, y) ] \sqrt {1 + z _ {x} ^ {2} (x , y) + z _ {y} ^ {2} (x , y)} \mathrm{d} x \mathrm{d} y. \tag {4-2}
$$

这就是把对面积的曲面积分化为二重积分的公式. 这公式是容易记忆的, 因为曲面 $\Sigma$ 的方程是 $z = z(x, y)$, 而曲面积分记号中的 $\mathrm{d}S$ 就是 $\sqrt{1 + z_x^2(x, y) + z_y^2(x, y)} \mathrm{d}x \mathrm{d}y$. 在计算时, 只要把变量 $z$ 换为 $z(x, y)$, $\mathrm{d}S$ 换为 $\sqrt{1 + z_x^2 + z_y^2} \mathrm{d}x \mathrm{d}y$, 再确定 $\Sigma$ 在 $xOy$ 面上的投影区域 $D_{xy}$, 这样就把对面积的曲面积分化为二重积分了.

如果积分曲面 $\Sigma$ 由方程 $x = x(y,z)$ 或 $y = y(z,x)$ 给出，也可类似地把对面积的曲面积分化为相应的二重积分.

例1 计算曲面积分 $\iint_{\Sigma} \frac{\mathrm{d}S}{z}$, 其中 $\Sigma$ 是球面 $x^2 + y^2 + z^2 = a^2$ 被平面 $z = h (0 < h < a)$ 截出的顶部（图11-20）.

![](images/page_217_image_17.jpg)

<details>
<summary>text_image</summary>

z
a
Σ
h
O
Dxy
a
y
x
a
</details>

图11-20

解 $\Sigma$ 的方程为

$$
z = \sqrt {a ^ {2} - x ^ {2} - y ^ {2}},
$$

$\Sigma$ 在 $xOy$ 面上的投影区域 $D_{xy}$ 为圆形闭区域 $\{(x,y)\mid x^2 +y^2\leqslant a^2 -h^2\}$. 又

$$
\sqrt {1 + z _ {x} ^ {2} + z _ {y} ^ {2}} = \frac {a}{\sqrt {a ^ {2} - x ^ {2} - y ^ {2}}}.
$$

根据公式(4-2)，有

$$
\iint_ {\Sigma} \frac {\mathrm{d} S}{z} = \iint_ {D _ {x y}} \frac {a \mathrm{d} x \mathrm{d} y}{a ^ {2} - x ^ {2} - y ^ {2}}.
$$

利用极坐标,得

$$
\iint_ {\Sigma} \frac {\mathrm{d} S}{z} = \iint_ {D _ {x y}} \frac {a \rho \mathrm{d} \rho \mathrm{d} \theta}{a ^ {2} - \rho^ {2}} = a \int_ {0} ^ {2 \pi} \mathrm{d} \theta \int_ {0} ^ {\sqrt {a ^ {2} - h ^ {2}}} \frac {\rho \mathrm{d} \rho}{a ^ {2} - \rho^ {2}} = 2 \pi a \left[ - \frac {1}{2} \ln (a ^ {2} - \rho^ {2}) \right] _ {0} ^ {\sqrt {a ^ {2} - h ^ {2}}} = 2 \pi a \ln \frac {a}{h}.
$$

例 2 计算  $\oiint_{\Sigma} xyz \, dS^{①}$ ，其中  $\Sigma$  是由平面 x=0, y=0, z=0 及  $x+y+z=1$  所围成的四面体的整个边界曲面（图 11-21）.

解 整个边界曲面 $\Sigma$ 在平面 $x = 0, y = 0, z = 0$ 及 $x + y + z = 1$ 上的部分依次记为 $\Sigma_{1}, \Sigma_{2}, \Sigma_{3}$ 及 $\Sigma_{4}$, 于是

$$
\oiint_ {\Sigma} x y z \mathrm{d} S = \iint_ {\Sigma_ {1}} x y z \mathrm{d} S + \iint_ {\Sigma_ {2}} x y z \mathrm{d} S + \iint_ {\Sigma_ {3}} x y z \mathrm{d} S + \iint_ {\Sigma_ {4}} x y z \mathrm{d} S.
$$

因为在  $\Sigma_{1}, \Sigma_{2}, \Sigma_{3}$  上，被积函数  $f(x, y, z) = xyz$  均为零，
所以

![](images/page_218_image_12.jpg)

<details>
<summary>text_image</summary>

z
1
O
Dxy
1
y
x
1
</details>

图11-21

$$
\iint_ {\Sigma_ {1}} x y z \mathrm{d} S = \iint_ {\Sigma_ {2}} x y z \mathrm{d} S = \iint_ {\Sigma_ {3}} x y z \mathrm{d} S = 0.
$$

在  $\Sigma_{4}$  上, z=1-x-y, 所以

$$
\sqrt {1 + z _ {x} ^ {2} + z _ {y} ^ {2}} = \sqrt {1 + (- 1) ^ {2} + (- 1) ^ {2}} = \sqrt {3},
$$

从而

$$
\oiint_ {\Sigma} x y z \mathrm{d} S = \iint_ {\Sigma_ {4}} x y z \mathrm{d} S = \iint_ {D _ {x y}} \sqrt {3} x y (1 - x - y) \mathrm{d} x \mathrm{d} y,
$$

其中 $D_{xy}$ 是 $\Sigma_4$ 在 $xOy$ 面上的投影区域，即由直线 $x = 0, y = 0$ 及 $x + y = 1$ 所围成的闭区域.因此

$$
\oiint_ {\Sigma} x y z \mathrm{d} S = \sqrt {3} \int_ {0} ^ {1} x \mathrm{d} x \int_ {0} ^ {1 - x} y (1 - x - y) \mathrm{d} y = \sqrt {3} \int_ {0} ^ {1} x \left[ (1 - x) \frac {y ^ {2}}{2} - \frac {y ^ {3}}{3} \right] _ {0} ^ {1 - x} \mathrm{d} x
$$

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 记号  $\oint_{\Sigma}$  表示在闭曲面  $\Sigma$  上积分.</span></small>

$$
= \sqrt {3} \int_ {0} ^ {1} x \cdot \frac {(1 - x) ^ {3}}{6} \mathrm{d} x = \frac {\sqrt {3}}{6} \int_ {0} ^ {1} (x - 3 x ^ {2} + 3 x ^ {3} - x ^ {4}) \mathrm{d} x = \frac {\sqrt {3}}{1 2 0}.
$$

## 习题11-4

1. 设有一分布着质量的曲面 $\Sigma$，在点 $(x, y, z)$ 处它的面密度为 $\mu(x, y, z)$，用对面积的曲面积分表示这曲面对于 $x$ 轴的转动惯量。

2. 按对面积的曲面积分的定义证明公式

$$
\iint_ {\Sigma} f (x, y, z) \mathrm{d} S = \iint_ {\Sigma_ {1}} f (x, y, z) \mathrm{d} S + \iint_ {\Sigma_ {2}} f (x, y, z) \mathrm{d} S,
$$

其中  $\Sigma$  是由  $\Sigma_{1}$  和  $\Sigma_{2}$  组成的.

3. 当 $\Sigma$ 是 $xOy$ 面内的一个闭区域时，曲面积分 $\iint_{\Sigma} f(x, y, z) \mathrm{d}S$ 与二重积分有什么关系？

4. 计算曲面积分 $\iint_{\Sigma} f(x, y, z) \, \mathrm{d}S$，其中 $\Sigma$ 为抛物面 $z = 2 - (x^2 + y^2)$ 在 $xOy$ 面上方的部分，$f(x, y, z)$ 分别如下:

(1) $f(x,y,z)=1;$

(2) $f(x,y,z)=x^{2}+y^{2};$

(3) $f(x,y,z)=3z.$

5. 计算 $\iint_{\Sigma} (x^2 + y^2) \, \mathrm{d}S$，其中 $\Sigma$ 是

（1）锥面 $z = \sqrt{x^2 + y^2}$ 及平面 $z = 1$ 所围成的区域的整个边界曲面；
(2) 锥面  $z^{2}=3(x^{2}+y^{2})$  被平面 z=0 和 z=3 所截得的部分.

6. 计算下列对面积的曲面积分:

(1) $\iint_{\Sigma} \left(z + 2x + \frac{4}{3}y\right) \, \mathrm{d}S$，其中 $\Sigma$ 为平面 $\frac{x}{2} + \frac{y}{3} + \frac{z}{4} = 1$ 在第 I 卦限中的部分；
(2) $\iint_{\Sigma}(2xy - 2x^2 - x + z)\mathrm{d}S$ ，其中 $\Sigma$ 为平面 $2x + 2y + z = 6$ 在第I卦限中的部分；
(3) $\iint_{\Sigma}(x + y + z)\mathrm{d}S$ ，其中 $\Sigma$ 为球面 $x^{2} + y^{2} + z^{2} = a^{2}$ 上 $z\geqslant h$ （ $0 <   h <   a$ )的部分；
(4) $\iint_{\Sigma}(xy + yz + zx)\mathrm{d}S$ ，其中 $\Sigma$ 为锥面 $z = \sqrt{x^2 + y^2}$ 被柱面 $x^{2} + y^{2} = 2ax$ 所截得的有限部分.

7. 求抛物面壳 $z = \frac{1}{2} (x^2 + y^2) (0 \leqslant z \leqslant 1)$ 的质量, 此壳的面密度为 $\mu = z$.

8. 求面密度为  $\mu_{0}$  的均匀半球壳  $x^{2} + y^{2} + z^{2} = a^{2} (z \geqslant 0)$  对于 z 轴的转动惯量.

## 第五节 对坐标的曲面积分

## 一、对坐标的曲面积分的概念与性质

我们对曲面作一些说明,这里假定曲面是光滑的.

通常我们遇到的曲面都是双侧的.例如由方程 $z = z(x,y)$ 表示的曲面,有上侧与下侧之分①;又例如,一张包围某一空间区域的闭曲面,有外侧与内侧之分.以后我们总假定所考虑的曲面是双侧的.

在讨论对坐标的曲面积分时,需要指定曲面的侧.我们可以通过曲面上法向量的方向来定出曲面的侧.例如,对于曲面 $z=z(x,y)$ ,如果取它的法向量n的方向朝上,我们就认为取定曲面的上侧;又如,对于闭曲面如果取它的法向量的方向朝外,我们就认为取定曲面的外侧.这种取定了法向量亦即选定了侧的曲面,就称为有向曲面.

设 $\Sigma$ 是有向曲面. 在 $\Sigma$ 上取一小块曲面 $\Delta S$, 把 $\Delta S$ 投影到 $xOy$ 面上得一投影区域, 这投影区域的面积记为 $(\Delta \sigma)_{xy}$. 假定 $\Delta S$ 上各点处的法向量与 $z$ 轴的夹角 $\gamma$ 的余弦 $\cos \gamma$ 有相同的符号 (即 $\cos \gamma$ 都是正的或都是负的). 我们规定 $\Delta S$ 在 $xOy$ 面上的投影 $(\Delta S)_{xy}$ 为

$$
(\Delta S) _ {x y} = \left\{ \begin{array}{l l} (\Delta \sigma) _ {x y}, & \cos \gamma > 0, \\ - (\Delta \sigma) _ {x y}, & \cos \gamma <   0, \\ 0, & \cos \gamma \equiv 0. \end{array} \right.
$$

其中 $\cos \gamma \equiv 0$ 也就是 $(\Delta \sigma)_{xy} = 0$ 的情形. $\Delta S$ 在 $xOy$ 面上的投影 $(\Delta S)_{xy}$ 实际就是 $\Delta S$ 在 $xOy$ 面上的投影区域的面积附以一定的正负号. 类似地可以定义 $\Delta S$ 在 $yOz$ 面及 $zOx$ 面上的投影 $(\Delta S)_{yz}$ 及 $(\Delta S)_{zx}$.

下面讨论一个例子,然后引进对坐标的曲面积分的概念.

流向曲面一侧的流量 设稳定流动②的不可压缩流体(假定密度为1)的速度场由

$$
\boldsymbol {v} (x, y, z) = P (x, y, z) \boldsymbol {i} + Q (x, y, z) \boldsymbol {j} + R (x, y, z) \boldsymbol {k}
$$

给出, $\Sigma$ 是速度场中的一片有向曲面,函数 $P(x,y,z)$ , $Q(x,y,z)$ 与 $R(x,y,z)$ 都在 $\Sigma$ 上连续,求在单位时间内流向 $\Sigma$ 指定侧的流体的质量,即流量 $\Phi$ .

如果流体流过平面上面积为 $A$ 的一个闭区域，且流体在这闭区域上各点处的流速为（常向量） $\pmb{v}$ ，又设 $\pmb{n}$ 为该平面的单位法向量（图11-22(a))，那么在单位时间内流过这个闭区域的流体组成一个底面积为 $A$ 、斜高为 $|\pmb{v}|$ 的斜柱体(图11-22(b)).

当 $(\widehat{\boldsymbol{v},\boldsymbol{n}}) = \theta <  \frac{\pi}{2}$ 时，斜柱体的体积为

$$
A \mid \boldsymbol {v} \mid \cos \theta = A \boldsymbol {v} \cdot \boldsymbol {n}.
$$

这也就是通过闭区域 $A$ 流向 $\pmb{n}$ 所指一侧的流量 $\Phi$;

当 $(\widehat{\boldsymbol{v},\boldsymbol{n}}) = \frac{\pi}{2}$ 时，显然流体通过闭区域 $A$ 流向 $\pmb{n}$ 所指一侧的流量 $\Phi$ 为零，而 $Av\cdot$

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 按惯例,这里假定 z 轴铅直向上.</span></small>

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">② 所谓稳定流动,就是说流速与时间 t 无关.</span></small>

$$
n = 0, \text {故} \Phi = A v \cdot n = 0;
$$

![](images/page_221_image_2.jpg)

<details>
<summary>text_image</summary>

v
θ
A
n
</details>

(a)

![](images/page_221_image_4.jpg)

<details>
<summary>natural_image</summary>

3D illustration of a cylinder with a dashed diameter line labeled A (no text or symbols beyond the label)
</details>

(b)

图11-22

当 $(\widehat{\boldsymbol{v},\boldsymbol{n}}) > \frac{\pi}{2}$ 时，$Av\cdot n < 0$ ，这时我们仍把 $Av\cdot n$ 称为流体通过闭区域 $A$ 流向 $\pmb{n}$ 所指一侧的流量，它表示流体通过闭区域 $A$ 实际上流向- $\pmb{n}$ 所指一侧，且流向- $\pmb{n}$ 所指一侧的流量为 $-Av\cdot n.$ 因此，不论 $(\widehat{\boldsymbol{v},\boldsymbol{n}})$ 为何值，流体通过闭区域 $A$ 流向 $\pmb{n}$ 所指一侧的流量 $\Phi$ 均为 $Av\cdot n$

由于现在所考虑的不是平面闭区域而是一片曲面,且流速 v 也不是常向量,因此所求流量不能直接用上述方法计算.然而过去在引出各类积分概念的例子中一再使用过的方法,也可用来解决目前的问题.

把曲面 $\Sigma$ 分成 $n$ 小块 $\Delta S_{i}$（$\Delta S_{i}$ 同时也代表第 $i$ 小块曲面的面积）。在 $\Sigma$ 是光滑的和 $\pmb{v}$ 是连续的前提下，只要 $\Delta S_{i}$ 的直径很小，我们就可以用 $\Delta S_{i}$ 上任一点 $(\xi_{i}, \eta_{i}, \zeta_{i})$ 处的流速

$$
\boldsymbol {v} _ {i} = \boldsymbol {v} (\xi_ {i}, \eta_ {i}, \zeta_ {i}) = P (\xi_ {i}, \eta_ {i}, \zeta_ {i}) \boldsymbol {i} + Q (\xi_ {i}, \eta_ {i}, \zeta_ {i}) \boldsymbol {j} + R (\xi_ {i}, \eta_ {i}, \zeta_ {i}) \boldsymbol {k}
$$

代替  $\Delta S_{i}$  上其他各点处的流速, 以该点  $(\xi_{i}, \eta_{i}, \zeta_{i})$  处曲面  $\Sigma$  的单位法向量

$$
n _ {i} = \cos \alpha_ {i} i + \cos \beta_ {i} j + \cos \gamma_ {i} k
$$

代替  $\Delta S_{i}$  上其他各点处的单位法向量（图11-23）。从而得到通过  $\Delta S_{i}$  流向指定侧的流量的近似值为

$$
\boldsymbol {v} _ {i} \cdot \boldsymbol {n} _ {i} \Delta S _ {i} \quad (i = 1, 2, \dots , n).
$$

于是,通过  $\Sigma$  流向指定侧的流量

![](images/page_221_image_16.jpg)

<details>
<summary>text_image</summary>

(ξᵢ,ηᵢ,ζᵢ)
ΔSᵢ
z
nᵢ
vᵢ
Σ
O
y
x
</details>

图 11-23

$$
\begin{array}{l} \Phi \approx \sum_ {i = 1} ^ {n} \boldsymbol {v} _ {i} \cdot \boldsymbol {n} _ {i} \Delta S _ {i} \\ = \sum_ {i = 1} ^ {n} \left[ P (\xi_ {i}, \eta_ {i}, \zeta_ {i}) \cos \alpha_ {i} + Q (\xi_ {i}, \eta_ {i}, \zeta_ {i}) \cos \beta_ {i} + R (\xi_ {i}, \eta_ {i}, \zeta_ {i}) \cos \gamma_ {i} \right] \Delta S _ {i}, \\ \end{array}
$$

但

$$
\cos \alpha_ {i} \cdot \Delta S _ {i} \approx (\Delta S _ {i}) _ {y z}, \quad \cos \beta_ {i} \cdot \Delta S _ {i} \approx (\Delta S _ {i}) _ {z x}, \quad \cos \gamma_ {i} \cdot \Delta S _ {i} \approx (\Delta S _ {i}) _ {x y},
$$

因此上式可以写成

$$
\Phi \approx \sum_ {i = 1} ^ {n} \left[ P (\xi_ {i}, \eta_ {i}, \zeta_ {i}) (\Delta S _ {i}) _ {y z} + Q (\xi_ {i}, \eta_ {i}, \zeta_ {i}) (\Delta S _ {i}) _ {z x} + R (\xi_ {i}, \eta_ {i}, \zeta_ {i}) (\Delta S _ {i}) _ {x y} \right].
$$

当各小块曲面的直径的最大值  $\lambda \rightarrow 0$  取上述和的极限, 就得到流量  $\Phi$  的精确值. 这样的极限还会在其他问题中遇到. 抽去它们的具体意义, 就得出下列对坐标的曲面积分的概念:

定义 设  $\Sigma$  为光滑的有向曲面, 函数  $R(x,y,z)$  在  $\Sigma$  上有界. 把  $\Sigma$  任意分成 n 块小曲面  $\Delta S_{i}$  ( $\Delta S_{i}$  同时又表示第 i 块小曲面的面积),  $\Delta S_{i}$  在 xOy 面上的投影为  $(\Delta S_{i})_{xy}$ ,  $(\xi_{i},\eta_{i},\zeta_{i})$  是  $\Delta S_{i}$  上任意取定的一点, 作乘积  $R(\xi_{i},\eta_{i},\zeta_{i})(\Delta S_{i})_{xy}$  ( $i=1,2,\cdots,n$ ), 并作和  $\sum_{i=1}^{n}R(\xi_{i},\eta_{i},\zeta_{i})(\Delta S_{i})_{xy}$ , 如果当各小块曲面的直径的最大值  $\lambda\to0$  时, 这和的极限总存在, 且与曲面  $\Sigma$  的分法及点  $(\xi_{i},\eta_{i},\zeta_{i})$  的取法无关, 那么称此极限为函数  $R(x,y,z)$  在有向曲面  $\Sigma$  上对坐标 x,y 的曲面积分, 记作  $\iint_{\Sigma}R(x,y,z)\mathrm{d}x\mathrm{d}y$ , 即

$$
\iint_ {\Sigma} R (x, y, z) \mathrm{d} x \mathrm{d} y = \lim _ {\lambda \to 0} \sum_ {i = 1} ^ {n} R (\xi_ {i}, \eta_ {i}, \zeta_ {i}) (\Delta S _ {i}) _ {x y},
$$

其中  $R(x,y,z)$  叫做被积函数,  $\Sigma$  叫做积分曲面.

类似地可以定义函数 $P(x,y,z)$ 在有向曲面 $\Sigma$ 上对坐标 $y,z$ 的曲面积分$\iint_{\Sigma}P(x,y,z)\mathrm{d}y\mathrm{d}z$ 及函数 $Q(x,y,z)$ 在有向曲面 $\Sigma$ 上对坐标 $z,x$ 的曲面积分$\iint_{\Sigma}Q(x,y,z)\mathrm{d}z\mathrm{d}x$ 分别为

$$
\iint_ {\Sigma} P (x, y, z) \mathrm{d} y \mathrm{d} z = \lim _ {\lambda \rightarrow 0} \sum_ {i = 1} ^ {n} P (\xi_ {i}, \eta_ {i}, \zeta_ {i}) (\Delta S _ {i}) _ {y z},
$$

$$
\iint_ {\Sigma} Q (x, y, z) \mathrm{d} z \mathrm{d} x = \lim _ {\lambda \rightarrow 0} \sum_ {i = 1} ^ {n} Q (\xi_ {i}, \eta_ {i}, \zeta_ {i}) (\Delta S _ {i}) _ {z x}.
$$

以上三个曲面积分也称为第二类曲面积分.

我们指出, 当  $P(x,y,z)$ ,  $Q(x,y,z)$  与  $R(x,y,z)$  在有向光滑曲面  $\Sigma$  上连续时, 对坐标的曲面积分是存在的, 以后总假定 P, Q 与 R 在  $\Sigma$  上连续.

在应用上出现较多的是

$$
\iint_ {\Sigma} P (x, y, z) \mathrm{d} y \mathrm{d} z + \iint_ {\Sigma} Q (x, y, z) \mathrm{d} z \mathrm{d} x + \iint_ {\Sigma} R (x, y, z) \mathrm{d} x \mathrm{d} y
$$

这种合并起来的形式.为简便起见,我们把它写成

$$
\iint_ {\Sigma} P (x, y, z) \mathrm{d} y \mathrm{d} z + Q (x, y, z) \mathrm{d} z \mathrm{d} x + R (x, y, z) \mathrm{d} x \mathrm{d} y.
$$

例如,上述流向  $\Sigma$  指定侧的流量  $\Phi$  可表示为

$$
\Phi = \iint_ {\Sigma} P (x, y, z) \mathrm{d} y \mathrm{d} z + Q (x, y, z) \mathrm{d} z \mathrm{d} x + R (x, y, z) \mathrm{d} x \mathrm{d} y.
$$

如果 $\Sigma$ 是分片光滑的有向曲面, 我们规定函数在 $\Sigma$ 上对坐标的曲面积分等于函数在各片光滑曲面上对坐标的曲面积分之和.

对坐标的曲面积分具有与对坐标的曲线积分相类似的一些性质.例如:

(1) 如果把  $\Sigma$  分成  $\Sigma_{1}$  和  $\Sigma_{2}$ ，那么

$$
\begin{array}{l} \iint_ {\Sigma} P \mathrm{d} y \mathrm{d} z + Q \mathrm{d} z \mathrm{d} x + R \mathrm{d} x \mathrm{d} y \\ = \iint_ {\Sigma_ {1}} P \mathrm{d} y \mathrm{d} z + Q \mathrm{d} z \mathrm{d} x + R \mathrm{d} x \mathrm{d} y + \iint_ {\Sigma_ {2}} P \mathrm{d} y \mathrm{d} z + Q \mathrm{d} z \mathrm{d} x + R \mathrm{d} x \mathrm{d} y. \tag {5-1} \\ \end{array}
$$

公式(5-1)可以推广到  $\Sigma$  分成  $\Sigma_{1}, \Sigma_{2}, \cdots, \Sigma_{n}$  几部分的情形.

(2) 设  $\Sigma$  是有向曲面,  $\Sigma^{-}$ 表示与  $\Sigma$  取相反侧的有向曲面, 则

$$
\begin{array}{l} \iint_ {\Sigma^ {-}} P (x, y, z) \mathrm{d} y \mathrm{d} z = - \iint_ {\Sigma} P (x, y, z) \mathrm{d} y \mathrm{d} z, \\ \iint_ {\Sigma^ {-}} Q (x, y, z) \mathrm{d} z \mathrm{d} x = - \iint_ {\Sigma} Q (x, y, z) \mathrm{d} z \mathrm{d} x, \tag {5-2} \\ \iint_ {\Sigma^ {-}} R (x, y, z) \mathrm{d} x \mathrm{d} y = - \iint_ {\Sigma} R (x, y, z) \mathrm{d} x \mathrm{d} y. \\ \end{array}
$$

(5-2)式表示,当积分曲面改变为相反侧时,对坐标的曲面积分要改变符号.因此关于对坐标的曲面积分,我们必须注意积分曲面所取的侧.

这些性质的证明从略.

## 二、对坐标的曲面积分的计算法

设积分曲面 $\Sigma$ 是由方程 $z = z(x,y)$ 所给出的曲面上侧，$\Sigma$ 在 $xOy$ 面上的投影区域为 $D_{xy}$，函数 $z = z(x,y)$ 在 $D_{xy}$ 上具有一阶连续偏导数，被积函数 $R(x,y,z)$ 在 $\Sigma$ 上连续.

按对坐标的曲面积分的定义,有

$$
\iint_ {\Sigma} R (x, y, z) \mathrm{d} x \mathrm{d} y = \lim _ {\lambda \to 0} \sum_ {i = 1} ^ {n} R (\xi_ {i}, \eta_ {i}, \zeta_ {i}) (\Delta S _ {i}) _ {x y}.
$$

因为  $\Sigma$  取上侧,  $\cos \gamma > 0$ , 所以

$$
(\Delta S _ {i}) _ {x y} = (\Delta \sigma_ {i}) _ {x y}.
$$

又因 $(\xi_{i},\eta_{i},\zeta_{i})$ 是 $\Sigma$ 上的一点，故 $\zeta_i = z(\xi_i,\eta_i)$ .从而有

$$
\sum_ {i = 1} ^ {n} R (\xi_ {i}, \eta_ {i}, \zeta_ {i}) (\Delta S _ {i}) _ {x y} = \sum_ {i = 1} ^ {n} R [ \xi_ {i}, \eta_ {i}, z (\xi_ {i}, \eta_ {i}) ] (\Delta \sigma_ {i}) _ {x y}.
$$