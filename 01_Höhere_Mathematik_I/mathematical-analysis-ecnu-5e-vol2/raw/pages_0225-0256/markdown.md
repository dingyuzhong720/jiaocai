7. 为了使曲线积分

$$
\int_ {L} F (x, y) (y \mathrm{d} x + x \mathrm{d} y)
$$

与积分路线无关,可微函数  $F(x,y)$  应满足怎样的条件?

8. 计算曲线积分

$$
\int_ {\widehat {A M B}} \left[ \varphi (y) \mathrm{e} ^ {x} - m y \right] \mathrm{d} x + \left[ \varphi^ {\prime} (y) \mathrm{e} ^ {x} - m \right] \mathrm{d} y,
$$

其中 $\varphi(y)$ 和 $\varphi'(y)$ 为连续函数，$\widehat{AMB}$ 为连接点 $A(x_1, y_1)$ 和点 $B(x_2, y_2)$ 的任何路线，但与直线段 $AB$ 围成已知大小为 $S$ 的面积.

9. 设函数 $f(u)$ 具有一阶连续导数, 证明对任何光滑封闭曲线 $L$, 有

$$
\oint_ {L} f (  x y  )   (  y \mathrm{d} x   +   x \mathrm{d} y  )    =   0.
$$

10. 设函数 $u(x, y)$ 在由封闭的光滑曲线 $L$ 所围的区域 $D$ 上具有二阶连续偏导数，证明

$$
\iint_ {D} \left(\frac {\partial^ {2} u}{\partial x ^ {2}} + \frac {\partial^ {2} u}{\partial y ^ {2}}\right) \mathrm{d} \sigma = \oint_ {L} \frac {\partial u}{\partial \boldsymbol {n}} \mathrm{d} s,
$$

其中 $\frac{\partial u}{\partial n}$ 是 $u(x,y)$ 沿L外法线方向n的方向导数.

## § 4 二重积分的变量变换

## 一、二重积分的变量变换公式

在定积分的计算中,我们得到了如下结论:设 $f(x)$ 在区间 $[a,b]$ 上连续, $x=\varphi(t)$ 当t从 $\alpha$ 变到 $\beta$ 时,严格单调地从a变到b,且 $\varphi(t)$ 连续可微,则

$$
\int_ {a} ^ {b} f (x) \mathrm{d} x = \int_ {\alpha} ^ {\beta} f (\varphi (t)) \varphi^ {\prime} (t) \mathrm{d} t. \tag {1}
$$

当 $\alpha < \beta$ （即 $\varphi'(t) > 0$）时，记 $X = [a, b], Y = [\alpha, \beta]$，则 $X = \varphi(Y), Y = \varphi^{-1}(X)$. 利用这些记号，公式(1)又可写成

$$
\int_ {X} f (x) \mathrm{d} x = \int_ {\varphi^ {- 1} (X)} f (\varphi (t)) \varphi^ {\prime} (t) \mathrm{d} t. \tag {2}
$$

当  $\alpha>\beta$  （即  $\varphi'(t)<0$ ）时，(1) 式可写成

$$
\int_ {X} f (x) \mathrm{d} x = - \int_ {\varphi^ {- 1} (X)} f (\varphi (t)) \varphi^ {\prime} (t) \mathrm{d} t. \tag {3}
$$

故当 $\varphi (t)$ 为严格单调且连续可微时，(2)式和(3)式可统一写成如下的形式:

$$
\int_ {X} f (x) \mathrm{d} x = \int_ {\varphi^ {- 1} (X)} f (\varphi (t)) | \varphi^ {\prime} (t) | \mathrm{d} t. \tag {4}
$$

下面我们把公式(4)推广到二重积分的场合.为此,先给出下面的引理.

引理 设变换 $T: x = x(u, v), y = y(u, v)$ 将 $uv$ 平面上由按段光滑封闭曲线所围的闭区域 $\Delta$ 一对一地映成 $xy$ 平面上的闭区域 $D$, 函数 $x(u, v), y(u, v)$ 在 $\Delta$ 内分别具有一阶连续偏导数且它们的函数行列式

$$
J (u, v) = \frac {\partial (x , y)}{\partial (u , v)} \neq 0, \quad (u, v) \in \Delta ,
$$

则区域 $D$ 的面积

$$
\mu (D) = \iint_ {\Delta} | J (u, v) | \mathrm{d} u \mathrm{d} v. \tag {5}
$$

证 下面给出当 $y(u, v)$ 在 $\Delta$ 内具有二阶连续偏导数时的证明. 对 $y(u, v)$ 具有一阶连续偏导数条件下的证明在本章 §9 中给出.

由于 T 是一对一变换, 且  $J(u,v) \neq 0$ , 因而 T 把  $\Delta$  的内点变为 D 的内点, 所以  $\Delta$  的按段光滑边界曲线  $L_{\Delta}$  变换到 D 时, 其边界曲线  $L_{D}$  也是按段光滑的.

设曲线 $L_{\Delta}$ 的参数方程为

$$
u = u (t), \quad v = v (t) \quad (\alpha \leqslant t \leqslant \beta).
$$

由于 $L_{\Delta}$ 按段光滑，所以 $u^{\prime}(t), v^{\prime}(t)$ 在 $[\alpha, \beta]$ 上至多除去有限个第一类间断点外，在其他的点上都连续。因为 $L_{D} = T(L_{\Delta})$ ，所以 $L_{D}$ 的参数方程为

$$
\begin{array}{l} x = x (t) = x (u (t), v (t)), \quad (\alpha \leqslant t \leqslant \beta). \\ y = y (t) = y (u (t), v (t)) \\ \end{array}
$$

若规定 $t$ 从 $\alpha$ 变到 $\beta$ 时，对应于 $L_{D}$ 的正向，则根据格林公式，取 $P(x,y) = 0$ $Q(x,y) = x$ ，有

$$
\begin{array}{l} \mu (D) = \oint_ {L _ {D}} x \mathrm{d} y = \int_ {\alpha} ^ {\beta} x (t) y ^ {\prime} (t) \mathrm{d} t \\ = \int_ {\alpha} ^ {\beta} x (u (t), v (t)) \left[ \frac {\partial y}{\partial u} u ^ {\prime} (t) + \frac {\partial y}{\partial v} v ^ {\prime} (t) \right] \mathrm{d} t. \tag {6} \\ \end{array}
$$

另一方面，在 uv 平面上

$$
\begin{array}{l} \oint_ {L _ {\Delta}} x (u, v) \left[ \frac {\partial y}{\partial u} \mathrm{d} u + \frac {\partial y}{\partial v} \mathrm{d} v \right] \\ = \pm \int_ {\alpha} ^ {\beta} x (u (t), v (t)) \left[ \frac {\partial y}{\partial u} u ^ {\prime} (t) + \frac {\partial y}{\partial v} v ^ {\prime} (t) \right] \mathrm{d} t, \tag {7} \\ \end{array}
$$

其中正号及负号分别由 t 从  $\alpha$  变到  $\beta$  时, 是对应于  $L_{\Delta}$  的正方向或负方向所决定. 由 (6) 及 (7) 式得到

$$
\begin{array}{l} \mu (D) = \pm \oint_ {L _ {\Delta}} x (u, v) \left[ \frac {\partial y}{\partial u} \mathrm{d} u + \frac {\partial y}{\partial v} \mathrm{d} v \right] \\ = \pm \oint_ {L _ {\Delta}} x (u, v) \frac {\partial y}{\partial u} \mathrm{d} u + x (u, v) \frac {\partial y}{\partial v} \mathrm{d} v. \\ \end{array}
$$

令 $P(u,v) = x(u,v)\frac{\partial y}{\partial u},Q(u,v) = x(u,v)\frac{\partial y}{\partial v}$ ，在 $uv$ 平面上对上式应用格林公式，得到

$$
\mu (D) = \pm \iint_ {\Delta} \biggl (\frac {\partial Q}{\partial u} - \frac {\partial P}{\partial v} \biggr)   \mathrm{d} u \mathrm{d} v.
$$

由于函数 $y(u,v)$ 具有二阶连续偏导数，即有 $\frac{\partial^2y}{\partial u\partial v} = \frac{\partial^2y}{\partial v\partial u}$，因此，$\frac{\partial Q}{\partial u} - \frac{\partial P}{\partial v} = J(u,v)$，于是

$$
\mu (D) = \pm \iint_ {\Delta} J (u, v) \mathrm{d} u \mathrm{d} v.
$$

又因为 $\mu(D)$ 总是非负的，而 $J(u,v)$ 在 $\Delta$ 上不为零且连续，故其函数值在 $\Delta$ 上不变号，所以

$$
\mu (D) = \iint_ {\Delta} | J (u, v) | \mathrm{d} u \mathrm{d} v.
$$

定理21.13 设 $f(x, y)$ 在有界闭区域 $D$ 上可积，变换 $T: x = x(u, v), y = y(u, v)$ 将 $uv$ 平面由按段光滑封闭曲线所围成的闭区域 $\Delta$ 一对一地映成 $xy$ 平面上的闭区域 $D$，函数 $x(u, v), y(u, v)$ 在 $\Delta$ 内分别具有一阶连续偏导数且它们的函数行列式

$$
J (u, v) = \frac {\partial (x , y)}{\partial (u , v)} \neq 0, \quad (u, v) \in \Delta ,
$$

则 $\iint_{D} f(x, y) \, \mathrm{d}x \, \mathrm{d}y = \iint_{\Delta} f(x(u, v), y(u, v)) |J(u, v)| \, \mathrm{d}u \, \mathrm{d}v.$

证 用曲线网把  $\Delta$  分成 n 个小区域  $\Delta_{i}$ ，在变换 T 作用下，区域 D 也相应地被分成 n 个小区域  $D_{i}$ 。记  $\Delta_{i}$  及  $D_{i}$  的面积为  $\mu(\Delta_{i})$  及  $\mu(D_{i})$  ( $i=1,2,\cdots,n$ )。由引理及二重积分中值定理，有

$$
\mu (D _ {i}) = \iint_ {\Delta_ {i}} | J (u, v) | \mathrm{d} u \mathrm{d} v = | J (\bar {u} _ {i}, \bar {v} _ {i}) | \mu (\Delta_ {i}),
$$

其中 $(\bar{u}_{i},\bar{v}_{i})\in\Delta_{i}(i=1,2,\cdots,n)$ .

令  $\xi_{i}=x\left(\bar{u}_{i},\bar{v}_{i}\right)$ ,  $\eta_{i}=y\left(\bar{u}_{i},\bar{v}_{i}\right)$ ，则  $(\xi_{i},\eta_{i})\in D_{i}(i=1,2,\cdots,n)$ . 作二重积分  $\iint_{D}f(x,y)\mathrm{d}x\mathrm{d}y$  的积分和

$$
\begin{array}{l} \sigma = \sum_ {i = 1} ^ {n} f (\xi_ {i}, \eta_ {i}) \mu (D _ {i}) \\ = \sum_ {i = 1} ^ {n} f (x (\bar {u} _ {i}, \bar {v} _ {i}), y (\bar {u} _ {i}, \bar {v} _ {i})) | J (\bar {u} _ {i}, \bar {v} _ {i}) | \mu (\Delta_ {i}). \\ \end{array}
$$

上式右边的和式是  $\Delta$  上可积函数  $f(x(u,v),y(u,v))|J(u,v)|$  的积分和. 又由变换 T 的连续性可知, 当区域  $\Delta$  的分割  $T_{\Delta}:\{\Delta_{1},\Delta_{2},\cdots,\Delta_{n}\}$  的细度  $\|T_{\Delta}\|\to0$  时, 区域 D 相应的分割  $T_{D}:\{D_{1},D_{2},\cdots,D_{n}\}$  的细度  $\|T_{D}\|$  也趋于零. 因此得到

$$
\iint_ {D} f (x, y) \mathrm{d} x \mathrm{d} y = \iint_ {\Delta} f (x (u, v), y (u, v)) | J (u, v) | \mathrm{d} u \mathrm{d} v.
$$

例 1 求  $\iint_{D} e^{\frac{x-y}{x+y}} dx dy$ ，其中 D 是由 x=0, y=0,  $x+y=1$  所围区域（图 21-21）.

解 为了简化被积函数, 令 u = x - y,  $v = x + y$ . 为此作变换  $T: x = \frac{1}{2}(u + v)$ ,  $y = \frac{1}{2}(v - u)$ , 则

$$
J (u, v) = \left| \begin{array}{c c} {\frac {1}{2}} & {\frac {1}{2}} \\ {- \frac {1}{2}} & {\frac {1}{2}} \end{array} \right| = \frac {1}{2} > 0.
$$

在变换 T 的作用下, 区域 D 的原象  $\Delta$  如图 21-22 所示. 所以

$$
\begin{array}{l} \iint_ {D} \mathrm{e} ^ {\frac {x - y}{x + y}} \mathrm{d} x \mathrm{d} y = \iint_ {\Delta} \mathrm{e} ^ {\frac {u}{v}} \cdot \frac {1}{2} \mathrm{d} u \mathrm{d} v = \frac {1}{2} \int_ {0} ^ {1} \mathrm{d} v \int_ {- v} ^ {v} \mathrm{e} ^ {\frac {u}{v}} \mathrm{d} u \\ = \frac {1}{2} \int_ {0} ^ {1} v (\mathrm{e-e} ^ {- 1}) \mathrm{d} v = \frac {\mathrm{e-e} ^ {- 1}}{4}. \\ \end{array}
$$

![](images/page_227_image_2.jpg)

<details>
<summary>text_image</summary>

y
1
x+y=1
D
O
1
x
</details>

图21-21

![](images/page_227_image_4.jpg)

<details>
<summary>text_image</summary>

v
1
Δ
-1
O
1
u
</details>

图21-22

例2 求抛物线 $y^{2} = mx, y^{2} = nx$ 和直线 $y = \alpha x, y = \beta x$ 所围区域 $D$ 的面积 $\mu(D)$ ($0 < m < n, 0 < \alpha < \beta$).

解 $D$ 的面积

$$
\mu (D) = \iint_ {D} \mathrm{d} x \mathrm{d} y.
$$

为了简化积分区域,作变换

$$
x = \frac {u}{v ^ {2}}, \quad y = \frac {u}{v}.
$$

它把 $xy$ 平面上的区域 $D$ （图21-23中的阴影部分）对应到 $uv$ 平面上的矩形区域 $\Delta = [m, n] \times [\alpha, \beta]$. 由于

![](images/page_227_image_12.jpg)

<details>
<summary>text_image</summary>

y
y=βx
y=αx
y²=nx
D
O
x
y²=mx
</details>

图21-23

$$
J (u, v) = \left| \begin{array}{c c} {{\frac {1}{v ^ {2}}}} & {{- \frac {2 u}{v ^ {3}}}} \\ {{\frac {1}{v}}} & {{- \frac {u}{v ^ {2}}}} \end{array} \right| = \frac {u}{v ^ {4}} > 0, \quad (u, v) \in \Delta ,
$$

所以

$$
\begin{array}{l} \mu (D) = \iint_ {D} \mathrm{d} \sigma = \iint_ {\Delta} \frac {u}{v ^ {4}} \mathrm{d} u \mathrm{d} v \\ = \int_ {\alpha} ^ {\beta} \frac {\mathrm{d} v}{v ^ {4}} \cdot \int_ {m} ^ {n} u \mathrm{d} u = \frac {(n ^ {2} - m ^ {2}) (\beta^ {3} - \alpha^ {3})}{6 \alpha^ {3} \beta^ {3}}. \\ \end{array}
$$

## 二、用极坐标计算二重积分

当积分区域是圆域或圆域的一部分,或者被积函数的形式为  $f(x^{2}+y^{2})$  时,采用极坐标变换

$$
T: \left\{ \begin{array}{l l} x = r \cos \theta , \\ y = r \sin \theta , \end{array} \right. 0 \leqslant r <   + \infty , 0 \leqslant \theta \leqslant 2 \pi \tag {8}
$$

往往能达到简化积分区域或被积函数的目的. 此时, 变换 T 的函数行列式为

$$
J (r, \theta) = \left| \begin{array}{c c} \cos \theta & - r \sin \theta \\ \sin \theta & r \cos \theta \end{array} \right| = r.
$$

![](images/page_228_image_2.jpg)

<details>
<summary>text_image</summary>

y
ε
O
A
A'
x
Dε
B
B'
</details>

(a)

![](images/page_228_image_4.jpg)

<details>
<summary>text_image</summary>

θ
2π
2π-ε
E
F
Δε
C
O
ε
R
D
</details>

(b)

图21-24

容易知道,极坐标变换 T 把  $r\theta$  平面上的矩形  $[0,R]\times[0,2\pi]$  变换成 xy 平面上的圆域  $D=\{(x,y)\mid x^{2}+y^{2}\leqslant R^{2}\}$ . 但对应不是一对一的. 例如, xy 平面上原点 O(0,0) 与  $r\theta$  平面上直线 r=0 相对应, x 轴上线段 AA' 对应于  $r\theta$  平面上两条线段 CD 和 EF (图 21-24). 又当 r=0 时,  $J(r,\theta)=0$ , 因此不满足定理 21.13 的条件. 但是, 我们仍然有下面的结论.

定理 21.14 设  $f(x,y)$  满足定理 21.13 的条件, 且在极坐标变换 (8) 下, xy 平面上有界闭区域 D 与  $r\theta$  平面上区域  $\Delta$  对应, 则成立

$$
\iint_ {D} f (x, y) \mathrm{d} x \mathrm{d} y = \iint_ {\Delta} f (r \cos \theta , r \sin \theta) r \mathrm{d} r \mathrm{d} \theta . \tag {9}
$$

证 若 $D$ 为圆域 $\{(x,y) | x^2 + y^2 \leqslant R^2\}$, 则 $\Delta$ 为 $r\theta$ 平面上矩形区域 $[0, R] \times [0, 2\pi]$. 设 $D_{\varepsilon}$ 为在圆环 $\{(x,y) | 0 < \varepsilon^2 \leqslant x^2 + y^2 \leqslant R^2\}$ 中除去中心角为 $\varepsilon$ 的扇形 $BB'A'A$ 所得的区域（图21-24(a))，则在变换(8)下，$D_{\varepsilon}$ 对应于 $r\theta$ 平面上的矩形区域 $\Delta_{\varepsilon} = [\varepsilon, R] \times [0, 2\pi - \varepsilon]$ （图21-24(b)). 但极坐标变换(8)在 $D_{\varepsilon}$ 与 $\Delta_{\varepsilon}$ 之间是一对一变换，且在 $\Delta_{\varepsilon}$ 上函数行列式 $J(r, \theta) > 0$. 于是由定理21.13，有

$$
\iint_ {D _ {\varepsilon}} f (x, y) \mathrm{d} x \mathrm{d} y = \iint_ {\Delta_ {\varepsilon}} f (r \cos \theta , r \sin \theta) r \mathrm{d} r \mathrm{d} \theta .
$$

因为 $f(x,y)$ 在有界闭域 $D$ 上有界，在上式中令 $\varepsilon \to 0$ ，即得

$$
\iint_ {D} f (x, y) \mathrm{d} x \mathrm{d} y = \iint_ {\Delta} f (r \cos \theta , r \sin \theta) r \mathrm{d} r \mathrm{d} \theta .
$$

若 $D$ 是一般的有界闭区域, 则取足够大的 $R > 0$, 使 $D$ 包含在圆域 $D_{R} = \{(x, y) | x^{2} + y^{2} \leqslant R^{2}\}$ 内, 并且在 $D_{R}$ 上定义函数

$$
F (x, y) = \left\{ \begin{array}{l l} f (x, y), & (x, y) \in D, \\ 0, & (x, y) \notin D. \end{array} \right.
$$

函数  $F(x,y)$  在  $D_{R}$  内至多在有限条按段光滑曲线上间断, 因此, 对函数  $F(x,y)$ , 由前述有

$$
\iint_ {D _ {R}} F (x, y) \mathrm{d} x \mathrm{d} y = \iint_ {\Delta_ {R}} F (r \cos \theta , r \sin \theta) r \mathrm{d} r \mathrm{d} \theta ,
$$

其中 $\Delta_R$ 为 $r\theta$ 平面上矩形区域 $[0,R]\times [0,2\pi ]$ .由函数 $F(x,y)$ 的定义，即得(9)式. □

由定理 21.14 看到,用极坐标变换计算二重积分,除变量作相应的替换外,还须把“面积微元”dxdy 换成  $rdrd\theta$ .

下面介绍二重积分在极坐标系下如何化为累次积分计算.

(i) 若原点 $O \notin D$，且 $xy$ 平面上射线 $\theta =$ 常数与 $D$ 的边界至多交于两点（图21-25），则 $\Delta$ 必可表示成

$$
r _ {1} (\theta) \leqslant r \leqslant r _ {2} (\theta), \quad \alpha \leqslant \theta \leqslant \beta ,
$$

于是有

$$
\iint_ {D} f (x, y) \mathrm{d} x \mathrm{d} y = \int_ {\alpha} ^ {\beta} \mathrm{d} \theta \int_ {r _ {1} (\theta)} ^ {r _ {2} (\theta)} f (r \cos \theta , r \sin \theta) r \mathrm{d} r. \tag {10}
$$

类似地, 若 xy 平面上的圆 r=常数与 D 的边界至多交于两点(图 21-26), 则  $\Delta$  必可表示成

$$
\theta_ {1} (r) \leqslant \theta \leqslant \theta_ {2} (r), \quad r _ {1} \leqslant r \leqslant r _ {2},
$$

所以

$$
\iint_ {D} f (x, y) \mathrm{d} x \mathrm{d} y = \int_ {r _ {1}} ^ {r _ {2}} r \mathrm{d} r \int_ {\theta_ {1} (r)} ^ {\theta_ {2} (r)} f (r \cos \theta , r \sin \theta) \mathrm{d} \theta . \tag {11}
$$

![](images/page_229_image_13.jpg)

<details>
<summary>text_image</summary>

r=r₂(θ)
D
r=r₁(θ)
β
α
O
x
</details>

图21-25

![](images/page_229_image_15.jpg)

<details>
<summary>text_image</summary>

θ=θ₂(r)
D
θ=θ₁(r)
r₁
r₂
x
</details>

图21-26

(ii) 若原点为 $D$ 的内点(图21-27), $D$ 的边界的极坐标方程为 $r = r(\theta)$, 则 $\Delta$ 可表示成

$$
0 \leqslant r \leqslant r (\theta), \quad 0 \leqslant \theta \leqslant 2 \pi .
$$

所以

$$
\iint_ {D} f (x, y) \mathrm{d} x \mathrm{d} y = \int_ {0} ^ {2 \pi} \mathrm{d} \theta \int_ {0} ^ {r (\theta)} f (r \cos \theta , r \sin \theta) r \mathrm{d} r. \tag {12}
$$

(iii) 若原点 $O$ 在 $D$ 的边界上 (图21-28), 则 $\Delta$ 为

$$
0 \leqslant r \leqslant r (\theta), \quad \alpha \leqslant \theta \leqslant \beta ,
$$

于是

$$
\iint_ {D} f (x, y) \mathrm{d} x \mathrm{d} y = \int_ {\alpha} ^ {\beta} \mathrm{d} \theta \int_ {0} ^ {r (\theta)} f (r \cos \theta , r \sin \theta) r \mathrm{d} r. \tag {13}
$$

![](images/page_230_image_1.jpg)

<details>
<summary>text_image</summary>

r=r(θ)
D
O
x
y
</details>

图21-27

![](images/page_230_image_3.jpg)

<details>
<summary>text_image</summary>

y
r=r(θ)
D
β
O
α
x
</details>

图21-28

例3 计算

$$
I = \iint_ {D} \frac {\mathrm{d} \sigma}{\sqrt {1 - x ^ {2} - y ^ {2}}},
$$

其中 D 为圆域  $x^{2}+y^{2}\leqslant1$ .

解 由于原点为 D 的内点, 故由(12)式, 有

$$
\begin{array}{l} \iint_ {D} \frac {\mathrm{d} \sigma}{\sqrt {1 - x ^ {2} - y ^ {2}}} = \int_ {0} ^ {2 \pi} \mathrm{d} \theta \int_ {0} ^ {1} \frac {r}{\sqrt {1 - r ^ {2}}} \mathrm{d} r \\ = \int_ {0} ^ {2 \pi} \left[ - \sqrt {1 - r ^ {2}} \right] \Big | _ {0} ^ {1} \mathrm{d} \theta = \int_ {0} ^ {2 \pi} \mathrm{d} \theta = 2 \pi . \\ \end{array}
$$

例 4 求球体  $x^{2}+y^{2}+z^{2}\leqslant R^{2}$  被圆柱面  $x^{2}+y^{2}=Rx$  所割下部分的体积（称为维维安尼（Viviani）体）.

解 由所求立体的对称性(图21-29)，我们只要求出在第一卦限内的部分体积后乘以4，即得所求立体的体积. 在第一卦限内的立体是一个曲顶柱体，其底为 $xy$ 平面内由 $y \geqslant 0$ 和 $x^{2} + y^{2} \leqslant Rx$ 所确定的区域，曲顶的方程为

$$
z = \sqrt {R ^ {2} - x ^ {2} - y ^ {2}}.
$$

所以

![](images/page_230_image_14.jpg)

<details>
<summary>text_image</summary>

z
y
O
R
x
</details>

图21-29

$$
V = 4 \iint_ {D} \sqrt {R ^ {2} - x ^ {2} - y ^ {2}} \mathrm{d} \sigma ,
$$

其中 $D = \{(x,y) | y \geqslant 0, x^2 + y^2 \leqslant Rx\}$ （图21-30）. 用极坐标变换后，由（13）式，有

$$
\begin{array}{l} V = 4 \int_ {0} ^ {\frac {\pi}{2}} \mathrm{d} \theta \int_ {0} ^ {R \cos \theta} \sqrt {R ^ {2} - r ^ {2}} r \mathrm{d} r \\ = \frac {4}{3} R ^ {3} \int_ {0} ^ {\frac {\pi}{2}} (1 - \sin^ {3} \theta) \mathrm{d} \theta = \frac {4}{3} R ^ {3} \left(\frac {\pi}{2} - \frac {2}{3}\right). \\ \end{array}
$$

例5 计算 $I = \iint_{D} \mathrm{e}^{-(x^2 + y^2)} \, \mathrm{d}\sigma$，其中 $D$ 为圆域 $x^2 + y^2 \leqslant R^2$.

![](images/page_230_image_20.jpg)

<details>
<summary>text_image</summary>

r=Rcos θ
D
O
x
y
</details>

图21-30

解 利用极坐标变换,由公式(12),有

$$
I = \int_ {0} ^ {2 \pi} \mathrm{d} \theta \int_ {0} ^ {R} r \mathrm{e} ^ {- r ^ {2}} \mathrm{d} r = \pi (1 - \mathrm{e} ^ {- R ^ {2}}).
$$

由例 5 可见, 若不用极坐标变换计算, 而用直角坐标系下化为累次积分计算, 就会遇到计算  $\int e^{-y^{2}} dy$  的问题, 但我们不能把  $\int e^{-y^{2}} dy$  表示成初等函数.

与极坐标相类似,我们也可以作下面的广义极坐标变换:

$$
T: \left\{ \begin{array}{l l} x = a r \cos \theta , \\ y = b r \sin \theta , \end{array} \right. 0 \leqslant r <   + \infty , 0 \leqslant \theta \leqslant 2 \pi ,
$$

并计算得

$$
J (r, \theta) = \left| \begin{array}{c c} a \cos \theta & - a r \sin \theta \\ b \sin \theta & b r \cos \theta \end{array} \right| = a b r.
$$

对广义极坐标变换也有与定理 21.14 相应的定理, 这里不再赘述了.

例6 求椭球体

$$
\frac {x ^ {2}}{a ^ {2}} + \frac {y ^ {2}}{b ^ {2}} + \frac {z ^ {2}}{c ^ {2}} \leqslant 1
$$

的体积.

解 由对称性, 椭球体的体积 V 是第一卦限部分体积的 8 倍, 这一部分是以 z = c  $\sqrt{1 - \frac{x^{2}}{a^{2}} - \frac{y^{2}}{b^{2}}}$  为曲顶,  $D = \left\{(x, y) \mid 0 \leqslant y \leqslant b \sqrt{1 - \frac{x^{2}}{a^{2}}}, 0 \leqslant x \leqslant a\right\}$  为底的曲顶柱体, 所以

$$
V = 8 \iint_ {D} c \sqrt {1 - \frac {x ^ {2}}{a ^ {2}} - \frac {y ^ {2}}{b ^ {2}}} \mathrm{d} x \mathrm{d} y.
$$

应用广义极坐标变换,由于  $z=c\sqrt{1-r^{2}}$ , 因此

$$
\begin{array}{l} V = 8 \int_ {0} ^ {\frac {\pi}{2}} \mathrm{d} \theta \int_ {0} ^ {1} c \sqrt {1 - r ^ {2}} a b r \mathrm{d} r \\ = 8 a b c \int_ {0} ^ {\frac {\pi}{2}} \mathrm{d} \theta \int_ {0} ^ {1} r \sqrt {1 - r ^ {2}} \mathrm{d} r = \frac {4 \pi}{3} a b c. \\ \end{array}
$$

当 $a = b = c = R$ 时，得到球的体积为 $\frac{4\pi}{3} R^3$

## 习题 21.4

1. 对积分 $\iint_{D} f(x, y) \, \mathrm{d}x \, \mathrm{d}y$ 进行极坐标变换并写出变换后不同顺序的累次积分:

(1) 当 D 为由不等式  $a^{2} \leqslant x^{2} + y^{2} \leqslant b^{2}, y \geqslant 0$  所确定的区域；
(2)  $D = \left\{(x, y) \mid x^{2} + y^{2} \leqslant y, x \geqslant 0\right\}$ ;
(3)  $D=\left\{(x,y)\mid0\leqslant x\leqslant1,0\leqslant x+y\leqslant1\right\}$ .

2. 用极坐标计算下列二重积分:

(1) $\iint_{D} \sin \sqrt{x^2 + y^2} \, \mathrm{d}x \, \mathrm{d}y$, 其中 $D = \{(x, y) \mid \pi^2 \leqslant x^2 + y^2 \leqslant 4\pi^2\}$;

(2) $\iint_{D}(x + y)\mathrm{d}x\mathrm{d}y$ ，其中 $D = \{(x,y)\mid x^2 +y^2\leqslant x + y\}$
(3) $\iint_{D} |xy| \, \mathrm{d}x \, \mathrm{d}y$，其中 $D$ 为圆域 $x^2 + y^2 \leqslant a^2$;
(4) $\iint_{D} f'(x^2 + y^2) \, \mathrm{d}x \, \mathrm{d}y$, 其中 $D$ 为圆域 $x^2 + y^2 \leqslant R^2$.

3. 在下列积分中引入新变量 u, v 后, 试将它化为累次积分:

(1) $\int_{0}^{2}\mathrm{d}x\int_{1 - x}^{2 - x}f(x,y)\mathrm{d}y$ ，若 $u = x + y,v = x - y;$
(2) $\iint_{D} f(x, y) \, \mathrm{d}x \, \mathrm{d}y$，其中 $D = \{(x, y) \mid \sqrt{x} + \sqrt{y} \leqslant \sqrt{a}, x \geqslant 0, y \geqslant 0\}$，若 $x = u \cos^4 v, y = u \sin^4 v$;
(3) $\iint_{D} f(x, y) \, \mathrm{d}x \, \mathrm{d}y$，其中 $D = \{(x, y) \mid x + y \leqslant a, x \geqslant 0, y \geqslant 0\}$，若 $x + y = u, y = uv$.

4. 试作适当变换, 计算下列积分:

(1) $\iint_{D}(x + y)\sin (x - y)\mathrm{d}x\mathrm{d}y, D = \{(x,y) \mid 0 \leqslant x + y \leqslant \pi, 0 \leqslant x - y \leqslant \pi\}$;
(2) $\iint_{D} \mathrm{e}^{\frac{y}{x + y}} \, \mathrm{d}x \, \mathrm{d}y, D = \{(x, y) \mid x + y \leqslant 1, x \geqslant 0, y \geqslant 0\}$.

5. 求由下列曲面所围立体 V 的体积:

(1) V 是由  $z = x^{2} + y^{2}$  和  $z = x + y$  所围的立体；
(2) V 是由曲面  $z^{2}=\frac{x^{2}}{4}+\frac{y^{2}}{9}$  和  $2z=\frac{x^{2}}{4}+\frac{y^{2}}{9}$  所围的立体.

6. 求由下列曲线所围的平面图形面积:

(1)  $x + y = a, x + y = b, y = \alpha x, y = \beta x \quad (0 < a < b, 0 < \alpha < \beta)$ ;
(2) $\left(\frac{x^{2}}{a^{2}}+\frac{y^{2}}{b^{2}}\right)^{2}=x^{2}+y^{2}$ ;
(3) $(x^{2} + y^{2})^{2} = 2a^{2}(x^{2} - y^{2})$ $(x^{2} + y^{2}\geqslant a^{2})$

7. 设 $f(x, y)$ 为连续函数，且 $f(x, y) = f(y, x)$. 证明

$$
\int_ {0} ^ {1} \mathrm{d} x \int_ {0} ^ {x} f (x, y) \mathrm{d} y = \int_ {0} ^ {1} \mathrm{d} x \int_ {0} ^ {x} f (1 - x, 1 - y) \mathrm{d} y.
$$

8. 试作适当变换, 把下列二重积分化为单重积分:

(1) $\iint_{D} f\left(\sqrt{x^2 + y^2}\right) \, \mathrm{d}x \, \mathrm{d}y$，其中 $D$ 为圆域 $x^2 + y^2 \leqslant 1$；
(2) $\iint_{D} f\left(\sqrt{x^2 + y^2}\right) \, \mathrm{d}x \, \mathrm{d}y$，其中 $D = \{(x, y) \mid |y| \leqslant |x|, |x| \leqslant 1\}$;
(3) $\iint_{D} f(x + y) \, \mathrm{d}x \, \mathrm{d}y$，其中 $D = \{(x, y) \mid |x| + |y| \leqslant 1\}$;
(4) $\iint_{D} f(xy) \, \mathrm{d}x \, \mathrm{d}y$，其中 $D = \{(x, y) \mid x \leqslant y \leqslant 4x, 1 \leqslant xy \leqslant 2\}$.

## § 5 三重积分

## 一、三重积分的概念

类似于第一型曲线积分,求一个空间立体 V 的质量 M 就可导出三重积分.设密度函数为  $f(x,y,z)$ ,为了求 V 的质量,我们把 V 分割成 n 个小块  $V_{1}, V_{2}, \cdots, V_{n}$ ,在每个小块  $V_{i}$  上任取一点  $(\xi_{i}, \eta_{i}, \zeta_{i})$ ,则

$$
M = \lim _ {\parallel T \parallel \to 0} \sum_ {i = 1} ^ {n} f (\xi_ {i}, \eta_ {i}, \zeta_ {i}) \Delta V _ {i},
$$

其中 $\Delta V_{i}$ 为小块 $V_{i}$ 的体积，$\| T \| = \max_{1 \leqslant i \leqslant n} \{V_{i}$ 的直径}.

设 $f(x,y,z)$ 是定义在三维空间可求体积的有界闭区域 $V^{①}$ 上的有界函数. 现用若干光滑曲面所组成的曲面网 $T$ 来分割 $V$, 它把 $V$ 分成 $n$ 个小区域 $V_{1}, V_{2}, \cdots, V_{n}$. 记 $V_{i}$ 的体积为 $\Delta V_{i} (i = 1,2,\dots,n)$, $\| T \| = \max_{1 \leqslant i \leqslant n} \{V_{i}$ 的直径 $\}$. 在每个 $V_{i}$ 中任取一点 $(\xi_{i}, \eta_{i}, \zeta_{i})$, 作积分和

$$
\sum_ {i = 1} ^ {n} f (\xi_ {i}, \eta_ {i}, \zeta_ {i}) \Delta V _ {i}.
$$

定义1 设 $f(x, y, z)$ 为定义在三维空间可求体积的有界闭区域 $V$ 上的函数, $J$ 是一个确定的数. 若对任给的正数 $\varepsilon$, 总存在某一正数 $\delta$, 使得对于 $V$ 的任何分割 $T$, 只要 $\| T \| < \delta$, 属于分割 $T$ 的所有积分和都有

$$
\Big | \sum_ {i = 1} ^ {n} f (\xi_ {i}, \eta_ {i}, \zeta_ {i}) \Delta V _ {i} - J \Big | <   \varepsilon ,
$$

则称 $f(x,y,z)$ 在 $V$ 上可积，数 $J$ 称为函数 $f(x,y,z)$ 在 $V$ 上的三重积分，记作

$$
J = \iiint_ {V} f (  x  , y  , z  )   \mathrm{d} V \quad \text {或} \quad J = \iiint_ {V} f (  x  , y  , z  )   \mathrm{d} x \mathrm{d} y \mathrm{d} z  ,
$$

其中 $f(x,y,z)$ 称为被积函数，$x,y,z$ 称为积分变量，$V$ 称为积分区域.

当 $f(x,y,z)\equiv 1$ 时， $\iiint_{V}\mathrm{d}V$ 在几何上表示 $V$ 的体积.

三重积分具有与二重积分相应的可积条件和有关性质(参见§1),这里不一一细述了.例如,类似于二重积分,有

(i) 有界闭区域 V 上的连续函数必可积；

（ii）如果有界闭区域 $V$ 上的有界函数 $f(x,y,z)$ 的间断点集中在有限多个零体积（可类似于零面积那样来定义）的曲面上，则 $f(x,y,z)$ 在 $V$ 上必可积.

## 二、化三重积分为累次积分

定理21.15 若函数 $f(x,y,z)$ 在长方体 $V = [a,b]\times [c,d]\times [e,h]$ 上的三重积分存在，且对任意 $(x,y)\in D = [a,b]\times [c,d],g(x,y) = \int_{e}^{h}f(x,y,z)\mathrm{d}z$ 存在，则积分 $\iint_{D}g(x,y)\mathrm{d}x\mathrm{d}y$ 也存在，且

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 读者可仿照 §1 定义平面图形可求面积的方法建立空间立体可求体积的概念. 今后我们总假定 V 的边界由光滑曲面组成, 以保证积分区域是可求体积的.</span></small>

$$
\iiint_ {V} f (x, y, z) \mathrm{d} x \mathrm{d} y \mathrm{d} z = \iint_ {D} \mathrm{d} x \mathrm{d} y \int_ {e} ^ {h} f (x, y, z) \mathrm{d} z. \tag {1}
$$

证 用平行于坐标平面的平面作分割 T, 它把 V 分成有限多个小长方体

$$
V _ {i j k} = \left[ x _ {i - 1}, x _ {i} \right] \times \left[ y _ {j - 1}, y _ {j} \right] \times \left[ z _ {k - 1}, z _ {k} \right].
$$

设 $M_{ijk}, m_{ijk}$ 分别是 $f(x, y, z)$ 在 $V_{ijk}$ 上的上确界和下确界. 对任意

$$
(\xi_ {i}, \eta_ {j}) \in [ x _ {i - 1}, x _ {i} ] \times [ y _ {j - 1}, y _ {j} ],
$$

$$
m _ {i j k} \Delta z _ {k} \leqslant \int_ {z _ {k - 1}} ^ {z _ {k}} f (\xi_ {i}, \eta_ {j}, z) \mathrm{d} z \leqslant M _ {i j k} \Delta z _ {k}.
$$

现按下标 k 相加, 有

$$
\sum_ {k} \int_ {z _ {k - 1}} ^ {z _ {k}} f (\xi_ {i}, \eta_ {j}, z) \mathrm{d} z = \int_ {e} ^ {h} f (\xi_ {i}, \eta_ {j}, z) \mathrm{d} z = g (\xi_ {i}, \eta_ {j})
$$

以及

$$
\sum_ {i, j, k} m _ {i j k} \Delta x _ {i} \Delta y _ {j} \Delta z _ {k} \leqslant \sum_ {i, j} g (\xi_ {i}, \eta_ {j}) \Delta x _ {i} \Delta y _ {j} \leqslant \sum_ {i, j, k} M _ {i j k} \Delta x _ {i} \Delta y _ {j} \Delta z _ {k}. \tag {2}
$$

上述不等式两边是分割 $T$ 的下和与上和. 由 $f(x, y, z)$ 在 $V$ 上可积, 当 $\| T \| \to 0$ 时, 下和与上和具有相同的极限, 所以由(2)式得 $g(x, y)$ 关于 $D$ 对应 $T$ 的直线网格分割的下和与上和具有相同的极限. 由定理21.4有 $g(x, y)$ 在 $D$ 上可积, 且

$$
\iint_ {D} g (x, y) \mathrm{d} x \mathrm{d} y = \iiint_ {V} f (x, y, z) \mathrm{d} x \mathrm{d} y \mathrm{d} z.
$$

推论 若 $V = \{(x, y, z) \mid (x, y) \in D, z_1(x, y) \leqslant z \leqslant z_2(x, y)\} \subset [a, b] \times [c, d] \times [e, h]$，其中 $D$ 为 $V$ 在 $Oxy$ 平面上的投影，$z_1(x, y), z_2(x, y)$ 是 $D$ 上的连续函数，函数 $f(x, y, z)$ 在 $V$ 上的三重积分存在，且对任意 $(x, y) \in D$

$$
G (x, y) = \int_ {z _ {1} (x, y)} ^ {z _ {2} (x, y)} f (x, y, z) \mathrm{d} z
$$

亦存在,则积分  $\iint_{D} G(x,y) \, dx \, dy$  存在,且

$$
\iiint_ {V} f (x, y, z) \mathrm{d} x \mathrm{d} y \mathrm{d} z = \iint_ {D} G (x, y) \mathrm{d} x \mathrm{d} y = \iint_ {D} \mathrm{d} x \mathrm{d} y \int_ {z _ {1} (x, y)} ^ {z _ {2} (x, y)} f (x, y, z) \mathrm{d} z. \tag {3}
$$

(见图 21-31).

证 定义 $F(x,y,z) = \begin{cases} f(x,y,z), & (x,y,z) \in V, \\ 0, & (x,y,z) \in V_0 \setminus V, \end{cases}$ 其中 $V_0 = [a,b] \times [c,d] \times [e, h]$，对 $F(x,y,z)$ 用定理21.15，则有

$$
\begin{array}{l} \iiint_ {V} f (x, y, z) \mathrm{d} x \mathrm{d} y \mathrm{d} z = \iiint_ {V _ {0}} F (x, y, z) \mathrm{d} x \mathrm{d} y \mathrm{d} z \\ = \iint_ {[ a, b ] \times [ c, d ]} \mathrm{d} x \mathrm{d} y \int_ {e} ^ {h} F (x, y, z) \mathrm{d} z \\ = \iint_ {D} \mathrm{d} x \mathrm{d} y \int_ {z _ {1} (x, y)} ^ {z _ {2} (x, y)} f (x, y, z) \mathrm{d} z. \\ \end{array}
$$

![](images/page_235_image_1.jpg)

<details>
<summary>text_image</summary>

z=z₂(x,y)
V
z=z₁(x,y)
O
D
x
y
z
</details>

图21-31

![](images/page_235_image_3.jpg)

<details>
<summary>text_image</summary>

z
z=y
O
1
y=x
2
x
y
</details>

图21-32

例1 计算 $\iiint_{V} \frac{\mathrm{d}x \, \mathrm{d}y \, \mathrm{d}z}{x^2 + y^2}$, 其中 $V$ 为由平面 $x = 1, x = 2, z = 0, y = x$ 与 $z = y$ 所围区域（见图21-32）

解 设 $V$ 在 $xy$ 平面上投影为 $D$, 则 $V = \{(x, y, z) \mid z_1(x, y) \leqslant z \leqslant z_2(x, y), (x, y) \in D\}$, 其中 $D = \{(x, y) \mid 0 \leqslant y \leqslant x, 1 \leqslant x \leqslant 2\}$ 是 $x$ 型区域, $z_1(x, y) = 0, z_2(x, y) = y$. 于是

$$
\begin{array}{l} \iiint_ {V} \frac {\mathrm{d} x \mathrm{d} y \mathrm{d} z}{x ^ {2} + y ^ {2}} = \iint_ {D} \mathrm{d} x \mathrm{d} y \int_ {0} ^ {y} \frac {\mathrm{d} z}{x ^ {2} + y ^ {2}} \\ = \iint_ {D} \frac {y}{x ^ {2} + y ^ {2}} \mathrm{d} x \mathrm{d} y = \int_ {1} ^ {2} \mathrm{d} x \int_ {0} ^ {x} \frac {y \mathrm{d} y}{x ^ {2} + y ^ {2}} \\ = \int_ {1} ^ {2} \frac {1}{2} \ln (x ^ {2} + y ^ {2}) \Bigg | _ {0} ^ {x} \mathrm{d} x = \int_ {1} ^ {2} \frac {1}{2} \ln 2 \mathrm{d} x \\ = \frac {1}{2} \ln 2. \\ \end{array}
$$

例2 计算 $\iiint_{V} (x^2 + y^2 + z) \, \mathrm{d}x \, \mathrm{d}y \, \mathrm{d}z$，其中 $V$ 是由 $\begin{cases} z = y, \\ x = 0 \end{cases}$ 绕 $z$ 轴旋转一周而成的曲面与 $z = 1$ 所围的区域.

解 旋转面方程为 $z = \sqrt{x^2 + y^2}$, $V$ 在 $xy$ 平面上投影为 $D = \{(x, y) | x^2 + y^2 \leqslant 1\}$, $z_1(x, y) = \sqrt{x^2 + y^2}$, $z_2(x, y) = 1$, 于是

$$
\begin{array}{l} \iiint_ {V} (x ^ {2} + y ^ {2} + z) \mathrm{d} x \mathrm{d} y \mathrm{d} z = \iint_ {D} \mathrm{d} x \mathrm{d} y \int_ {\sqrt {x ^ {2} + y ^ {2}}} ^ {1} (x ^ {2} + y ^ {2} + z) \mathrm{d} z \\ = \iint_ {D} \left(x ^ {2} + y ^ {2}\right) \left(1 - \sqrt {x ^ {2} + y ^ {2}}\right) \mathrm{d} x \mathrm{d} y + \frac {1}{2} \iint_ {D} \left[ 1 - \left(x ^ {2} + y ^ {2}\right) \right] \mathrm{d} x \mathrm{d} y \\ = \int_ {0} ^ {2 \pi} \mathrm{d} \theta \int_ {0} ^ {1} r ^ {2} (1 - r) r \mathrm{d} r + \frac {1}{2} \int_ {0} ^ {2 \pi} \mathrm{d} \theta \int_ {0} ^ {1} (1 - r ^ {2}) r \mathrm{d} r \\ = \frac {\pi}{1 0} + \frac {\pi}{4} = \frac {7 \pi}{2 0}. \\ \end{array}
$$

类似分析可得到以下定理和推论.

定理21.16 若函数 $f(x,y,z)$ 在长方体 $V = [a,b]\times [c,d]\times [e,h]$ 上的三重积分存在，且对任何 $z\in [e,h]$，二重积分

$$
I (z) = \iint_ {D} f (x, y, z) \mathrm{d} x \mathrm{d} y
$$

存在,其中  $D=[a,b]\times[c,d]$ ,则积分

$$
\int_ {e} ^ {h} \mathrm{d} z \iint_ {D} f (x, y, z) \mathrm{d} x \mathrm{d} y
$$

也存在,且

$$
\iiint_ {V} f (x, y, z) \mathrm{d} x \mathrm{d} y \mathrm{d} z = \int_ {e} ^ {h} \mathrm{d} z \iint_ {D} f (x, y, z) \mathrm{d} x \mathrm{d} y.
$$

推论 若 $V \subset [a, b] \times [c, d] \times [e, h]$, 函数 $f(x, y, z)$ 在 $V$ 上的三重积分存在, 且对任意固定的 $z \in [e, h]$, 积分 $\varphi(z) = \iint_{D_z} f(x, y, z) \, \mathrm{d}x \, \mathrm{d}y$ 存在, 其中 $D_z$ 是截面 $\{(x, y) \mid (x, y, z) \in V\}$, 则 $\int_{e}^{h} \varphi(z) \, \mathrm{d}z$ 存在, 且

$$
\iiint_ {V} f (x, y, z) \mathrm{d} x \mathrm{d} y \mathrm{d} z = \int_ {e} ^ {h} \varphi (z) \mathrm{d} z = \int_ {e} ^ {h} \mathrm{d} z \iint_ {D _ {z}} f (x, y, z) \mathrm{d} x \mathrm{d} y.
$$

(见图 21-33).

注 类似于对二重积分转化为累次积分的几何解释, 对定理 21.15 和定理 21.16 及其推论所给出的方法也可以从几何上做出解释. 在定理 21.15 及其推论中, 把积分区域视为柱体的一部分 (见图 21-31), 投影 (柱体底面) 区域为 D, 柱体上、下曲面分别为  $z = z_{2}(x, y)$ ,  $z = z_{1}(x, y)$ ,  $(x, y) \in D$ . 三重积分相应转化为先对 z 再对 x, y 的累次积分形式 (先一后二). 在定理 21.16 及其推论中, 把积分区域视为介于两平行平面 z = e, z = h 之间的立体 (见图 21-33), 用垂直于 z 轴的面截积分区域所得截面为  $D_{z}$ . 此时三重积分相应转化为先对 x, y 变量在平

![](images/page_236_image_11.jpg)

<details>
<summary>text_image</summary>

z
h
z
V
e
Dz
O
x
y
</details>

图21-33

面区域 $D_{z}$ 上的含参二重积分，再对 $z \in [e, h]$ 求定积分的形式（先二后一）。具体采用哪一种形式可根据实际问题中积分区域与被积函数的特性加以选择。

例3 求

$$
I = \iiint_ {V} \left(\frac {x ^ {2}}{a ^ {2}} + \frac {y ^ {2}}{b ^ {2}} + \frac {z ^ {2}}{c ^ {2}}\right) \mathrm{d} x \mathrm{d} y \mathrm{d} z,
$$

其中 $V$ 是椭球体 $\frac{x^2}{a^2} +\frac{y^2}{b^2} +\frac{z^2}{c^2}\leqslant 1.$

解 由于

$$
I = \iiint_ {V} \frac {x ^ {2}}{a ^ {2}} \mathrm{d} x \mathrm{d} y \mathrm{d} z + \iiint_ {V} \frac {y ^ {2}}{b ^ {2}} \mathrm{d} x \mathrm{d} y \mathrm{d} z + \iiint_ {V} \frac {z ^ {2}}{c ^ {2}} \mathrm{d} x \mathrm{d} y \mathrm{d} z,
$$

其中 $\iiint_{V} \frac{x^2}{a^2} \mathrm{d}x \, \mathrm{d}y \, \mathrm{d}z = \int_{-a}^{a} \frac{x^2}{a^2} \mathrm{d}x \iint_{V_x} \mathrm{d}y \, \mathrm{d}z$，这里 $V_x$ 表示椭圆面

$$
\frac {y ^ {2}}{b ^ {2}} + \frac {z ^ {2}}{c ^ {2}} \leqslant 1 - \frac {x ^ {2}}{a ^ {2}} \text {或} \frac {y ^ {2}}{b ^ {2} \left(1 - \frac {x ^ {2}}{a ^ {2}}\right)} + \frac {z ^ {2}}{c ^ {2} \left(1 - \frac {x ^ {2}}{a ^ {2}}\right)} \leqslant 1.
$$

它的面积为

$$
\pi \bigg (b \sqrt {1 - \frac {x ^ {2}}{a ^ {2}}} \bigg) \left(c \sqrt {1 - \frac {x ^ {2}}{a ^ {2}}}\right) = \pi b c \bigg (1 - \frac {x ^ {2}}{a ^ {2}} \bigg).
$$

于是

$$
\iiint_ {V} \frac {x ^ {2}}{a ^ {2}} \mathrm{d} x \mathrm{d} y \mathrm{d} z = \int_ {- a} ^ {a} \frac {\pi b c}{a ^ {2}} x ^ {2} \left(1 - \frac {x ^ {2}}{a ^ {2}}\right) \mathrm{d} x = \frac {4}{1 5} \pi a b c.
$$

同理可得

$$
\iiint_ {V} \frac {y ^ {2}}{b ^ {2}} \mathrm{d} x \mathrm{d} y \mathrm{d} z = \frac {4}{1 5} \pi a b c, \iiint_ {V} \frac {z ^ {2}}{c ^ {2}} \mathrm{d} x \mathrm{d} y \mathrm{d} z = \frac {4}{1 5} \pi a b c.
$$

所以

$$
I = 3 \bigg (\frac {4}{1 5} \pi a b c \bigg) = \frac {4}{5} \pi a b c.
$$

![](images/page_237_image_10.jpg)

下面用定理21.16的推论计算例1.

例1中的区域 $V = \{(x,y,z)\mid 1\leqslant x\leqslant 2,(y,z)\in D_x\}$ ，其中 $D_{x} = \{(y,z)\mid 0\leqslant y\leqslant x,0\leqslant z\leqslant y\}$ （见图21-34）.

$$
\begin{array}{l} \iiint_ {V} \frac {\mathrm{d} x \mathrm{d} y \mathrm{d} z}{x ^ {2} + y ^ {2}} = \int_ {1} ^ {2} \mathrm{d} x \iint_ {D _ {x}} \frac {\mathrm{d} y \mathrm{d} z}{x ^ {2} + y ^ {2}} \\ = \int_ {1} ^ {2} \mathrm{d} x \int_ {0} ^ {x} \mathrm{d} y \int_ {0} ^ {y} \frac {\mathrm{d} z}{x ^ {2} + y ^ {2}} \\ = \int_ {1} ^ {2} \mathrm{d} x \int_ {0} ^ {x} \frac {y \mathrm{d} y}{x ^ {2} + y ^ {2}} = \frac {1}{2} \ln 2. \\ \end{array}
$$

![](images/page_237_image_14.jpg)

<details>
<summary>text_image</summary>

z
Dₓ
O
x
y
</details>

图21-34

## 三、三重积分换元法

和二重积分一样,某些类型的三重积分作适当的变量变换后能使计算方便.

设变换 $T: x = x(u, v, w), y = y(u, v, w), z = z(u, v, w)$，把 $uvw$ 空间中的区域 $V'$ 一对一地映成 $xyz$ 空间中的区域 $V$，并设函数 $x(u, v, w), y(u, v, w), z(u, v, w)$ 及它们的一阶偏导数在 $V'$ 内连续且函数行列式

$$
J (u, v, w) = \left| \begin{array}{c c c} \frac {\partial x}{\partial u} & \frac {\partial x}{\partial v} & \frac {\partial x}{\partial w} \\ \frac {\partial y}{\partial u} & \frac {\partial y}{\partial v} & \frac {\partial y}{\partial w} \\ \frac {\partial z}{\partial u} & \frac {\partial z}{\partial v} & \frac {\partial z}{\partial w} \end{array} \right| \neq 0, (u, v, w) \in V ^ {\prime}.
$$

于是与二重积分换元法一样,可以证明(用本章§9中证明二重积分类似的方法)成立下面的三重积分换元公式:

$$
\begin{array}{l} \iiint_ {V} f (x, y, z) \mathrm{d} x \mathrm{d} y \mathrm{d} z \\ = \iiint_ {V ^ {\prime}} f (x (u, v, w), y (u, v, w), z (u, v, w)) | J (u, v, w) | \mathrm{d} u \mathrm{d} v \mathrm{d} w, \tag {4} \\ \end{array}
$$

其中 $f(x,y,z)$ 在 $V$ 上可积.

下面介绍几个常用的变换公式:

## 1. 柱面坐标变换

$$
T: \left\{ \begin{array}{l l} x = r \cos \theta , & 0 \leqslant r <   + \infty , \\ y = r \sin \theta , & 0 \leqslant \theta \leqslant 2 \pi , \\ z = z, & - \infty <   z <   + \infty . \end{array} \right.
$$

由于变换 $T$ 的函数行列式

$$
J (r, \theta , z) = \left| \begin{array}{c c c} \cos \theta & - r \sin \theta & 0 \\ \sin \theta & r \cos \theta & 0 \\ 0 & 0 & 1 \end{array} \right| = r,
$$

按(4)式,三重积分的柱面坐标换元公式为

$$
\iiint_ {V} f (x, y, z) \mathrm{d} x \mathrm{d} y \mathrm{d} z = \iiint_ {V ^ {\prime}} f (r \cos \theta , r \sin \theta , z) r \mathrm{d} r \mathrm{d} \theta \mathrm{d} z, \tag {5}
$$

这里  $V'$  为 V 在柱面坐标变换下的原象.

与极坐标变换一样,柱面坐标变换并非是一对一的,并且当 r=0 时, $J(r,\theta,z)=0$ ,但我们仍可证明(5)式成立.

在柱面坐标系中，用 $r =$ 常数， $\theta =$ 常数， $z =$ 常数的平面分割 $V^{\prime}$ 时，变换后在 $xyz$ 直角坐标系中， $r =$ 常数是以 $z$ 轴为中心轴的圆柱面， $\theta =$ 常数是过 $z$ 轴的半平面， $z =$ 常数是垂直于 $z$ 轴的平面（图21-35）.

用柱面坐标计算三重积分,通常是找出 V 在 xy 平面上的投影区域 D,即当

$$
V = \{(x, y, z) \mid z _ {1} (x, y) \leqslant z \leqslant z _ {2} (x, y), (x, y) \in D \}
$$

时，

$$
\iiint_ {V} f (x, y, z) \mathrm{d} x \mathrm{d} y \mathrm{d} z = \iint_ {D} \mathrm{d} x \mathrm{d} y \int_ {z _ {1} (x, y)} ^ {z _ {2} (x, y)} f (x, y, z) \mathrm{d} z,
$$

其中二重积分部分应用极坐标计算.

例4 计算

$$
\iiint_ {V} (x ^ {2} + y ^ {2}) \mathrm{d} x \mathrm{d} y \mathrm{d} z,
$$

其中 $V$ 是由曲面 $2(x^{2} + y^{2}) = z$ 与 $z = 4$ 为界面的区域（图21-36）.

![](images/page_238_image_20.jpg)

<details>
<summary>text_image</summary>

z
z+Δz
r
r+Δr
z
ΔV′
O
y
θ
Δθ
x
</details>

图21-35

![](images/page_238_image_22.jpg)

<details>
<summary>text_image</summary>

z
4
O
√2
y
x
√2
</details>

图21-36

解 $V$ 在 $xy$ 平面上的投影区域 $D$ 为 $x^{2} + y^{2}\leqslant 2.$ 按柱坐标变换，区域 $V^{\prime}$ 可表为

$$
V ^ {\prime} = \{(r, \theta , z) \mid 2 r ^ {2} \leqslant z \leqslant 4, 0 \leqslant r \leqslant \sqrt {2}, 0 \leqslant \theta \leqslant 2 \pi \}.
$$

所以由公式(5)，有

$$
\begin{array}{l} \iiint_ {V} \left(x ^ {2} + y ^ {2}\right) \mathrm{d} x \mathrm{d} y \mathrm{d} z = \iiint_ {V ^ {\prime}} r ^ {3} \mathrm{d} r \mathrm{d} \theta \mathrm{d} z \\ = \int_ {0} ^ {2 \pi} \mathrm{d} \theta \int_ {0} ^ {\sqrt {2}} \mathrm{d} r \int_ {2 r ^ {2}} ^ {4} r ^ {3} \mathrm{d} z = \frac {8 \pi}{3}. \\ \end{array}
$$

## 2. 球坐标变换

$$
T: \left\{ \begin{array}{l l} x = r \sin \varphi \cos \theta , & 0 \leqslant r <   + \infty , \\ y = r \sin \varphi \sin \theta , & 0 \leqslant \varphi \leqslant \pi , \\ z = r \cos \varphi , & 0 \leqslant \theta \leqslant 2 \pi . \end{array} \right.
$$

由于

$$
\begin{array}{l} J (r, \varphi , \theta) = \left| \begin{array}{c c c} \sin \varphi \cos \theta & r \cos \varphi \cos \theta & - r \sin \varphi \sin \theta \\ \sin \varphi \sin \theta & r \cos \varphi \sin \theta & r \sin \varphi \cos \theta \\ \cos \varphi & - r \sin \varphi & 0 \end{array} \right| \\ = r ^ {2} \sin \varphi , \\ \end{array}
$$

当  $\varphi$  在  $[0, \pi]$  上取值时， $\sin \varphi \geqslant 0$ ，所以在球坐标变换下，按公式(4)，三重积分的球坐标换元公式为

$$
\begin{array}{l} \iiint_ {V} f (x, y, z) \mathrm{d} x \mathrm{d} y \mathrm{d} z \\ = \iiint_ {V} f (r \sin \varphi \cos \theta , r \sin \varphi \sin \theta , r \cos \varphi) r ^ {2} \sin \varphi \mathrm{d} r \mathrm{d} \varphi \mathrm{d} \theta , \tag {6} \\ \end{array}
$$

这里  $V'$  为 V 在球坐标变换 T 下的原象.

类似地,球坐标变换并不是一对一的,并且当 r=0 或  $\varphi=0$  或  $\pi$  时, $J(r,\varphi,\theta)=0$ . 但我们仍然可以证明(6)式成立.

在球坐标系中,用 r=常数, $\varphi=$ 常数, $\theta=$ 常数的平面分割  $V'$  时,变换后在 xyz 直角坐标系中,r=常数是以原点为心的球面, $\varphi=$ 常数是以原点为顶点、z 轴为中心轴的半圆锥面, $\theta=$ 常数是过 z 轴的半平面(图 21-37).

在球坐标系下,当区域  $V'$  为集合

$$
V ^ {\prime} = \{(r, \varphi , \theta) \mid r _ {1} (\varphi , \theta) \leqslant r \leqslant r _ {2} (\varphi , \theta), \varphi_ {1} (\theta) \leqslant \varphi \leqslant \varphi_ {2} (\theta), \theta_ {1} \leqslant \theta \leqslant \theta_ {2} \}
$$

时，(6)式可化为累次积分

$$
\begin{array}{l} \iiint_ {V} f (x, y, z) \mathrm{d} x \mathrm{d} y \mathrm{d} z \\ = \int_ {\theta_ {1}} ^ {\theta_ {2}} \mathrm{d} \theta \int_ {\varphi_ {1} (\theta)} ^ {\varphi_ {2} (\theta)} \mathrm{d} \varphi \int_ {r _ {1} (\varphi , \theta)} ^ {r _ {2} (\varphi , \theta)} f (r \sin \varphi \cos \theta , r \sin \varphi \sin \theta , r \cos \varphi) r ^ {2} \sin \varphi \mathrm{d} r. \tag {7} \\ \end{array}
$$

例 5 求由圆锥体  $z \geqslant \sqrt{x^{2} + y^{2}} \cot \beta$  和球体  $x^{2} + y^{2} + (z - a)^{2} \leqslant a^{2}$  所确定的立体体积

(图 21-38)，其中  $\beta\in\left(0,\frac{\pi}{2}\right)$  和  $a\;(>0)$  为常数.

![](images/page_240_image_2.jpg)

<details>
<summary>text_image</summary>

z
r+Δr
φ
Δφ
O
θ
Δθ
y
x
</details>

图21-37

![](images/page_240_image_4.jpg)

<details>
<summary>text_image</summary>

z
-a
β
O
y
x
</details>

图21-38

解 在球坐标变换下, 球面方程  $x^{2}+y^{2}+(z-a)^{2}=a^{2}$  可表示成  $r=2a\cos\varphi$ , 锥面方程  $z=\sqrt{x^{2}+y^{2}}\cot\beta$  可表示成  $\varphi=\beta$ . 因此

$$
V ^ {\prime} = \{(r, \varphi , \theta) \mid 0 \leqslant r \leqslant 2 a \cos \varphi , 0 \leqslant \varphi \leqslant \beta , 0 \leqslant \theta \leqslant 2 \pi \}.
$$

由公式(7)求得 $V$ 的体积为

$$
\iiint_ {V} \mathrm{d} V = \int_ {0} ^ {2 \pi} \mathrm{d} \theta \int_ {0} ^ {\beta} \mathrm{d} \varphi \int_ {0} ^ {2 a \cos \varphi} r ^ {2} \sin \varphi \mathrm{d} r = \frac {4}{3} \pi a ^ {3} (1 - \cos^ {4} \beta).
$$

除上述介绍的两种变换外,下面我们再举一个例子,进一步说明如何根据被积函数或积分区域的特点来选择其他不同的变换.

例6 求 $I = \iiint_{V} z \, \mathrm{d}x \, \mathrm{d}y \, \mathrm{d}z$，其中 $V$ 为由 $\frac{x^2}{a^2} + \frac{y^2}{b^2} + \frac{z^2}{c^2} \leqslant 1$ 与 $z \geqslant 0$ 所交区域.

解 作广义球坐标变换

$$
T: \left\{ \begin{array}{l} x = a r \sin \varphi \cos \theta , \\ y = b r \sin \varphi \sin \theta , \\ z = c r \cos \varphi , \end{array} \right.
$$

于是 $J = abcr^2\sin \varphi$ .在上述广义球坐标变换下， $V$ 的原象为

$$
V ^ {\prime} = \{(r, \varphi , \theta) \mid 0 \leqslant r \leqslant 1, 0 \leqslant \varphi \leqslant \frac {\pi}{2}, 0 \leqslant \theta \leqslant 2 \pi \}.
$$

由公式(7)，有

$$
\begin{array}{l} \iiint_ {V} z \mathrm{d} x \mathrm{d} y \mathrm{d} z = \iiint_ {V ^ {\prime}} a b c ^ {2} r ^ {3} \sin \varphi \cos \varphi \mathrm{d} r \mathrm{d} \varphi \mathrm{d} \theta \\ = \int_ {0} ^ {2 \pi} \mathrm{d} \theta \int_ {0} ^ {\frac {\pi}{2}} \mathrm{d} \varphi \int_ {0} ^ {1} a b c ^ {2} r ^ {3} \sin \varphi \cos \varphi \mathrm{d} r \\ = \frac {\pi a b c ^ {2}}{2} \int_ {0} ^ {\frac {\pi}{2}} \sin \varphi \cos \varphi \mathrm{d} \varphi = \frac {\pi a b c ^ {2}}{4}. \\ \end{array}
$$

## 习题 21.5

1. 计算下列积分:

(1) $\iiint_{V}(xy + z^2)\mathrm{d}x\mathrm{d}y\mathrm{d}z$ ，其中 $V = [-2,5]\times [-3,3]\times [0,1]$
(2) $\iiint_{V} x \cos y \cos z \, \mathrm{d}x \, \mathrm{d}y \, \mathrm{d}z$, 其中 $V = [0,1] \times \left[0, \frac{\pi}{2}\right] \times \left[0, \frac{\pi}{2}\right]$;
(3) $\iiint_{V} \frac{\mathrm{d}x \, \mathrm{d}y \, \mathrm{d}z}{(1 + x + y + z)^3}$, 其中 $V$ 是由 $x + y + z = 1$ 与三个坐标面所围成的区域;
(4) $\iiint_{V} y \cos (x + z) \, \mathrm{d}x \, \mathrm{d}y \, \mathrm{d}z$, 其中 $V$ 是由 $y = \sqrt{x}, y = 0, z = 0$ 及 $x + z = \frac{\pi}{2}$ 所围成的区域.

2. 试改变下列累次积分的顺序:

(1) $\int_0^1\mathrm{d}x\int_0^{1 - x}\mathrm{d}y\int_0^{x + y}f(x,y,z)\mathrm{d}z;$
(2) $\int_0^1\mathrm{d}x\int_0^1\mathrm{d}y\int_0^{x^2 +y^2}f(x,y,z)\mathrm{d}z.$

3. 计算下列三重积分与累次积分:

(1) $\iiint_{V} z^2 \, \mathrm{d}x \, \mathrm{d}y \, \mathrm{d}z$，其中 $V$ 由 $x^2 + y^2 + z^2 \leqslant r^2$ 和 $x^2 + y^2 + z^2 \leqslant 2rz$ 所确定；
(2) $\int_0^1\mathrm{d}x\int_0^{\sqrt{1 - x^2}}\mathrm{d}y\int_{\sqrt{x^2 + y^2}}^{\sqrt{2 - x^2 - y^2}}z^2\mathrm{d}z.$

4. 利用适当的坐标变换, 计算下列各曲面所围成的体积:

(1) $z = x^{2} + y^{2}, z = 2(x^{2} + y^{2}), y = x, y = x^{2}$;
(2) $\left(\frac{x}{a} + \frac{y}{b}\right)^2 + \left(\frac{z}{c}\right)^2 = 1$ ($x \geqslant 0, y \geqslant 0, z \geqslant 0, a > 0, b > 0, c > 0$).

5. 设球体 $x^{2} + y^{2} + z^{2} \leqslant 2x$ 上各点的密度等于该点到坐标原点的距离，求该球体的质量.

6. 证明定理 21.16 及其推论.
7. 设 $V = \left\{(x, y, z) \left| \frac{x^2}{a^2} + \frac{y^2}{b^2} + \frac{z^2}{c^2} \leqslant 1 \right. \right\}$，计算下列积分:

(1) $\iiint_{V} \sqrt{1 - \frac{x^2}{a^2} - \frac{y^2}{b^2} - \frac{z^2}{c^2}} \, \mathrm{d}x \, \mathrm{d}y \, \mathrm{d}z$;
(2)  $\iiint_{V}e\sqrt{\frac{x^{2}}{a^{2}}+\frac{y^{2}}{b^{2}}+\frac{z^{2}}{c^{2}}}dxdydz.$

## § 6 重积分的应用

重积分的应用除前面提到的可用以求空间立体的体积及空间物体的质量外,这里再举几个它在几何与力学方面的应用.

## 一、曲面的面积

设 $D$ 为可求面积的平面有界区域, 函数 $f(x, y)$ 在 $D$ 上具有连续的一阶偏导数, 讨论由方程

$$
z = f (x, y), (x, y) \in D
$$

所确定的曲面 S 的面积.

为了定义曲面 S 的面积, 对区域 D 作分割 T, 它把 D 分成 n 个小区域  $\sigma_{i}(i=1,2,\cdots,n)$ . 根据这个分割相应地将曲面 S 也分成 n 个小曲面片  $S_{i}(i=1,2,\cdots,n)$ . 在每个  $S_{i}$  上任取一点  $M_{i}$ , 作曲面在这一点的切平面  $\pi_{i}$ , 并在  $\pi_{i}$  上取出一小块  $A_{i}$ , 使得  $A_{i}$  与  $S_{i}$  在 xy 平面上的投影都是  $\sigma_{i}$ , 如图 21-39 所示. 现在点  $M_{i}$  附近, 用切平面  $A_{i}$  代替小曲面片  $S_{i}$ , 从而当  $\|T\|$  充分小时, 有

![](images/page_242_image_6.jpg)

<details>
<summary>text_image</summary>

z
ΔAᵢ
ΔSᵢ
O
y
x
D
Δσᵢ
z=f(x,y)
</details>

图21-39

$$
\Delta S = \sum_ {i = 1} ^ {n} \Delta S _ {i} \approx \sum_ {i = 1} ^ {n} \Delta A _ {i},
$$

这里 $\Delta S, \Delta S_{i}, \Delta A_{i}$ 分别表示曲面 $S$，小曲面片 $S_{i}$，小切平面块 $A_{i}$ 的面积。所以当 $\| T \| \to 0$ 时，可用和式 $\sum_{i=1}^{n} \Delta A_{i}$ 的极限作为 $S$ 的面积。

现在按照上述给出的曲面面积的概念,来建立曲面面积的计算公式.

首先计算 $A_{i}$ 的面积. 由于切平面 $\pi_{i}$ 的法向量就是曲面 $S$ 在点 $M_{i}(\xi_{i},\eta_{i},\zeta_{i})$ 处的法向量, 记它与 $z$ 轴的夹角为 $\gamma_{i}$, 则

$$
\mid \cos \gamma_ {i} \mid = \frac {1}{\sqrt {1 + f _ {x} ^ {2} (\xi_ {i} , \eta_ {i}) + f _ {y} ^ {2} (\xi_ {i} , \eta_ {i})}}.
$$

因为 $A_{i}$ 在 $xy$ 平面上的投影为 $\sigma_{i}$，所以

$$
\Delta A _ {i} = \frac {\Delta \sigma_ {i}}{| \cos \gamma_ {i} |} = \sqrt {1 + f _ {x} ^ {2} (\xi_ {i} , \eta_ {i}) + f _ {y} ^ {2} (\xi_ {i} , \eta_ {i})} \Delta \sigma_ {i}.
$$

其次，由于和数

$$
\sum_ {i = 1} ^ {n} \Delta A _ {i} = \sum_ {i = 1} ^ {n} \sqrt {1 + f _ {x} ^ {2} (\xi_ {i} , \eta_ {i}) + f _ {y} ^ {2} (\xi_ {i} , \eta_ {i})} \Delta \sigma_ {i}
$$

是连续函数 $\sqrt{1 + f_x^2(x,y) + f_y^2(x,y)}$ 在有界闭区域 $D$ 上的积分和.于是当 $\| T\| \to 0$ 时，就得到

$$
\begin{array}{l} \Delta S = \lim _ {\| T \| \to 0} \sum_ {i = 1} ^ {n} \sqrt {1 + f _ {x} ^ {2} (\xi_ {i} , \eta_ {i}) + f _ {y} ^ {2} (\xi_ {i} , \eta_ {i})} \Delta \sigma_ {i} \\ = \iint_ {D} \sqrt {1 + f _ {x} ^ {2} (x , y) + f _ {y} ^ {2} (x , y)} \mathrm{d} x \mathrm{d} y \tag {1} \\ \end{array}
$$

或

$$
\Delta S = \lim _ {\| T \| \rightarrow 0} \sum_ {i = 1} ^ {n} \frac {\Delta \sigma_ {i}}{| \cos \gamma_ {i} |} = \iint_ {D} \frac {\mathrm{d} x \mathrm{d} y}{| \cos (\boldsymbol {n} , z) |}, \tag {2}
$$

其中  $\cos(\hat{n},z)$  为曲面的法向量 n 与 z 轴正向夹角的余弦.

例 1 求圆锥  $z=\sqrt{x^{2}+y^{2}}$  在圆柱体  $x^{2}+y^{2}\leqslant x$  内那一部分的面积.

解 据曲面面积公式(1)，

$$
\Delta S = \iint_ {D} \sqrt {1 + z _ {x} ^ {2} + z _ {y} ^ {2}} \mathrm{d} x \mathrm{d} y,
$$

其中 $D$ 是 $x^{2} + y^{2}\leqslant x.$ 所求曲面方程为

$$
z = \sqrt {x ^ {2} + y ^ {2}},
$$

故

$$
z _ {x} = \frac {x}{\sqrt {x ^ {2} + y ^ {2}}}, z _ {y} = \frac {y}{\sqrt {x ^ {2} + y ^ {2}}}.
$$

因此

$$
\sqrt {1 + z _ {x} ^ {2} + z _ {y} ^ {2}} = \sqrt {1 + \frac {x ^ {2}}{x ^ {2} + y ^ {2}} + \frac {y ^ {2}}{x ^ {2} + y ^ {2}}} = \sqrt {2},
$$

所以

$$
\Delta S = \iint_ {D} \sqrt {2} \mathrm{d} x \mathrm{d} y = \sqrt {2} \Delta D = \frac {\sqrt {2}}{4} \pi .
$$

在上册的定积分应用中,曾用微元法给出过旋转面的面积公式,下面用二重积分给予严格证明.

例 2 设平面光滑曲线的方程为

$$
y = f (x), x \in [ a, b ] (f (x) > 0),
$$

求证:此曲线绕 x 轴旋转一周得到的旋转曲面的面积为

$$
S = 2 \pi \int_ {a} ^ {b} f (x) \sqrt {1 + f ^ {\prime 2} (x)}   \mathrm{d} x.
$$

证 由于上半旋转面方程为 $z = \sqrt{f^2(x) - y^2}$，因此

$$
z _ {x} = \frac {f (x) f ^ {\prime} (x)}{\sqrt {f ^ {2} (x) - y ^ {2}}}, z _ {y} = \frac {- y}{\sqrt {f ^ {2} (x) - y ^ {2}}},
$$

$$
\sqrt {1 + z _ {x} ^ {2} + z _ {y} ^ {2}} = \sqrt {\frac {f ^ {2} (x) + f ^ {2} (x) f ^ {2} (x)}{f ^ {2} (x) - y ^ {2}}},
$$

于是

$$
\begin{array}{l} S = 2 \int_ {a} ^ {b} \mathrm{d} x \int_ {- f (x)} ^ {f (x)} \sqrt {\frac {f ^ {2} (x) + f ^ {2} (x) f ^ {\prime 2} (x)}{f ^ {2} (x) - y ^ {2}}} \mathrm{d} y \\ = 4 \int_ {a} ^ {b} \mathrm{d} x \int_ {0} ^ {f (x)} f (x) \sqrt {\frac {1 + f ^ {\prime 2} (x)}{1 - y ^ {2} f ^ {- 2} (x)}} \mathrm{d} \left(\frac {y}{f (x)}\right) \\ = 4 \int_ {a} ^ {b} f (x) \sqrt {1 + f ^ {\prime 2} (x)} \mathrm{d} x \int_ {0} ^ {1} \frac {\mathrm{d} t}{\sqrt {1 - t ^ {2}}} \\ = 2 \pi \int_ {a} ^ {b} f (x) \sqrt {1 + f ^ {\prime 2} (x)} \mathrm{d} x. \\ \end{array}
$$

若空间曲面 $S$ 由参量方程

$$
x = x (u, v), y = y (u, v), z = z (u, v), (u, v) \in D ^ {\prime} \tag {3}
$$

确定,其中  $x(u,v)$ ,  $y(u,v)$ ,  $z(u,v)$  在  $D'$  上具有连续的一阶偏导数,且

$$
\frac {\partial (x , y)}{\partial (u , v)}, \qquad \frac {\partial (y , z)}{\partial (u , v)}, \qquad \frac {\partial (z , x)}{\partial (u , v)}
$$

中至少有一个不等于零,则曲面 S 在点  $(x,y,z)$  的法线方向数为

$$
\left(\frac {\partial (y , z)}{\partial (u , v)}, \frac {\partial (z , x)}{\partial (u , v)}, \frac {\partial (x , y)}{\partial (u , v)}\right),
$$

它与 z 轴的夹角的余弦的绝对值为

$$
\begin{array}{l} \mid \cos (\widehat {\boldsymbol {n}}, z) \mid = \left| \frac {\frac {\partial (x , y)}{\partial (u , v)}}{\sqrt {\left(\frac {\partial (y , z)}{\partial (u , v)}\right) ^ {2} + \left(\frac {\partial (z , x)}{\partial (u , v)}\right) ^ {2} + \left(\frac {\partial (x , y)}{\partial (u , v)}\right) ^ {2}}} \right| \\ = \left| \frac {\frac {\partial (x , y)}{\partial (u , v)}}{\sqrt {(x _ {u} ^ {2} + y _ {u} ^ {2} + z _ {u} ^ {2}) (x _ {v} ^ {2} + y _ {v} ^ {2} + z _ {v} ^ {2}) - (x _ {u} x _ {v} + y _ {u} y _ {v} + z _ {u} z _ {v}) ^ {2}}} \right| \\ = \left| \frac {\partial (x , y)}{\partial (u , v)} \right| \frac {1}{\sqrt {E G - F ^ {2}}}, \tag {4} \\ \end{array}
$$

其中

$$
\begin{array}{l} E = x _ {u} ^ {2} + y _ {u} ^ {2} + z _ {u} ^ {2}, \\ F = x _ {u} x _ {v} + y _ {u} y _ {v} + z _ {u} z _ {v}, \\ G = x _ {v} ^ {2} + y _ {v} ^ {2} + z _ {v} ^ {2}. \\ \end{array}
$$

当 $\frac{\partial(x,y)}{\partial(u,v)}\neq0$ 时，对(2)作变换 $x=x(u,v),y=y(u,v)$ ，则有

$$
\begin{array}{l} \Delta S = \iint_ {D} \frac {1}{| \cos (\widehat {\boldsymbol {n} , z}) |} \mathrm{d} x \mathrm{d} y \\ = \iint_ {D ^ {\prime}} \frac {1}{| \cos (\widehat {\boldsymbol {n} , z}) |} \left| \frac {\partial (x , y)}{\partial (u , v)} \right| \mathrm{d} u \mathrm{d} v. \\ \end{array}
$$

由(4)，得到由参量方程(3)所表示的曲面面积公式:

$$
\Delta S = \iint_ {D ^ {\prime}} \sqrt {E G - F ^ {2}} \mathrm{d} u \mathrm{d} v. \tag {5}
$$

例 3 求球面上两条纬线和两条经线之间的曲面的面积(图 21-40 中阴影部分).

解 设球面方程为

$$
\begin{array}{l} x = R \cos \psi \cos \varphi , \\ y = R \cos \psi \sin \varphi , \\ z = R \sin \psi , \\ \end{array}
$$

其中 R 为球的半径. 本例是求当  $\varphi_{1} \leqslant \varphi \leqslant \varphi_{2}, \psi_{1} \leqslant \psi \leqslant \psi_{2}$  时的球面部分面积. 由于

$$
\begin{array}{l} E = x _ {\psi} ^ {2} + y _ {\psi} ^ {2} + z _ {\psi} ^ {2} = R ^ {2}, \\ F = 0, G = R ^ {2} \cos^ {2} \psi , \\ \end{array}
$$

所以

$$
\sqrt {E G - F ^ {2}} = R ^ {2} \cos \psi .
$$

由公式(5)即得所求曲面的面积.

![](images/page_244_image_21.jpg)

<details>
<summary>text_image</summary>

z
ψ₂
ψ₁
O
φ₁
φ₂
y
x
</details>

图21-40

$$
\Delta S = \int_ {\varphi_ {1}} ^ {\varphi_ {2}} \mathrm{d} \varphi \int_ {\psi_ {1}} ^ {\psi_ {2}} R ^ {2} \cos \psi \mathrm{d} \psi = R ^ {2} (\varphi_ {2} - \varphi_ {1}) (\sin \psi_ {2} - \sin \psi_ {1}).
$$

在讨论曲线弧长时,我们曾用弧内接折线的长在其各段的长趋于零时的极限来定义.但是能否类似地用曲面的内接多面形的面积,在其各个面积的直径趋于零时的极限来定义呢?施瓦茨(Schwarz)曾举出一个反例说明这样的定义方法是不可行的.对此读者可参见有关的数学分析教程(如菲赫金哥尔茨《微积分学教程》中译本第三卷第二分册).

## 二、质心

设 $V$ 是密度函数为 $\rho(x, y, z)$ 的空间物体，$\rho(x, y, z)$ 在 $V$ 上连续。为求得 $V$ 的质心坐标公式，先对 $V$ 作分割 $T$，在属于分割 $T$ 的每一小块 $v_i$ 上任取一点 $(\xi_i, \eta_i, \zeta_i)$，于是小块 $v_i$ 的质量可以 $\rho(\xi_i, \eta_i, \zeta_i) \Delta v_i$ 近似代替。若把每一小块看作质量集中在 $(\xi_i, \eta_i, \zeta_i)$ 的质点时，整个物体就可用这 $n$ 个质点的质点系来近似代替。由于质点系的质心坐标公式为

$$
\overline {{x}} _ {n} = \frac {\sum_ {i = 1} ^ {n} \xi_ {i} \rho (\xi_ {i} , \eta_ {i} , \zeta_ {i}) \Delta v _ {i}}{\sum_ {i = 1} ^ {n} \rho (\xi_ {i} , \eta_ {i} , \zeta_ {i}) \Delta v _ {i}}, \quad \bar {y} _ {n} = \frac {\sum_ {i = 1} ^ {n} \eta_ {i} \rho (\xi_ {i} , \eta_ {i} , \zeta_ {i}) \Delta v _ {i}}{\sum_ {i = 1} ^ {n} \rho (\xi_ {i} , \eta_ {i} , \zeta_ {i}) \Delta v _ {i}}, \quad \bar {z} _ {n} = \frac {\sum_ {i = 1} ^ {n} \zeta_ {i} \rho (\xi_ {i} , \eta_ {i} , \zeta_ {i}) \Delta v _ {i}}{\sum_ {i = 1} ^ {n} \rho (\xi_ {i} , \eta_ {i} , \zeta_ {i}) \Delta v _ {i}}.
$$

当 $\| T\| \to 0$ 时，我们很自然地把 $\bar{x}_n,\bar{y}_n,\bar{z}_n$ 的极限 $\bar{x},\bar{y},\bar{z}$ 定义为 $V$ 的质心坐标，即

$$
\overline {{x}} = \frac {\iiint_ {V} x \rho (x , y , z) \mathrm{d} V}{\iiint_ {V} \rho (x , y , z) \mathrm{d} V}, \quad \bar {y} = \frac {\iiint_ {V} y \rho (x , y , z) \mathrm{d} V}{\iiint_ {V} \rho (x , y , z) \mathrm{d} V}, \quad \bar {z} = \frac {\iiint_ {V} z \rho (x , y , z) \mathrm{d} V}{\iiint_ {V} \rho (x , y , z) \mathrm{d} V}.
$$

当物体 V 的密度均匀即  $\rho$  为常数时, 则有

$$
\bar {x} = \frac {1}{\Delta V} \iiint_ {V} x \mathrm{d} V, \quad \bar {y} = \frac {1}{\Delta V} \iiint_ {V} y \mathrm{d} V, \quad \bar {z} = \frac {1}{\Delta V} \iiint_ {V} z \mathrm{d} V,
$$

这里  $\Delta V$  为 V 的体积.

读者同样可以得到,密度分布为  $\rho(x,y)$  的平面薄板 D 的质心坐标是

$$
\overline {{x}} = \frac {\iint_ {D} x \rho (x , y) \mathrm{d} \sigma}{\iint_ {D} \rho (x , y) \mathrm{d} \sigma}, \quad \overline {{y}} = \frac {\iint_ {D} y \rho (x , y) \mathrm{d} \sigma}{\iint_ {D} \rho (x , y) \mathrm{d} \sigma}.
$$

当平面薄板 D 的密度均匀时, 即  $\rho$  是常数时, 则有

$$
\overline {{x}} = \frac {1}{\Delta D} \iint_ {D} x \mathrm{d} \sigma , \quad \overline {{y}} = \frac {1}{\Delta D} \iint_ {D} y \mathrm{d} \sigma ,
$$

这里  $\Delta D$  为平面薄板 D 的面积.

例 4 求密度均匀的上半椭球体的质心.

解 设椭球体由不等式

$$
\frac {x ^ {2}}{a ^ {2}} + \frac {y ^ {2}}{b ^ {2}} + \frac {z ^ {2}}{c ^ {2}} \leqslant 1
$$

表示. 由对称性知  $\bar{x}=0,\bar{y}=0$ . 又由  $\rho$  为常数, 所以

$$
\bar {z} = \frac {\iiint_ {V} \rho z \mathrm{d} V}{\iiint_ {V} \rho \mathrm{d} V} = \frac {\iiint_ {V} z \mathrm{d} x \mathrm{d} y \mathrm{d} z}{\frac {2}{3} \pi a b c}.
$$

由 §5 例6 得

$$
\bar {z} = \frac {3 c}{8}.
$$

## 三、转动惯量

质点 A 对于轴 l 的转动惯量 J 是质点 A 的质量 m 和 A 与转动轴 l 的距离 r 的平方的乘积, 即  $J = mr^{2}$ .

现在讨论空间物体 V 的转动惯量问题. 我们仍然采用第二段中的办法, 把 V 看作由 n 个质点组成的质点系, 然后用取极限的方法求得 V 的转动惯量.

设  $\rho(x,y,z)$  为空间物体 V 的密度分布函数, 它在 V 上连续. 对 V 作分割 T, 在属于 T 的每一小块  $v_{i}$  上任取一点  $(\xi_{i},\eta_{i},\zeta_{i})$ , 于是  $v_{i}$  的质量可以  $\rho(\xi_{i},\eta_{i},\zeta_{i})\Delta v_{i}$  近似替代. 当以质点系  $\{(\xi_{i},\eta_{i},\zeta_{i}), i=1,2,\cdots,n\}$  近似替代 V 时, 质点系对于 x 轴的转动惯量则是

$$
J _ {x _ {n}} = \sum_ {i = 1} ^ {n} (\eta_ {i} ^ {2} + \zeta_ {i} ^ {2}) \rho (\xi_ {i}, \eta_ {i}, \zeta_ {i}) \Delta v _ {i}.
$$

当 $\| T\| \to 0$ 时，上述积分和的极限就是物体 $V$ 对于 $x$ 轴的转动惯量

$$
J _ {x} = \iiint_ {V} (y ^ {2} + z ^ {2}) \rho (x, y, z) \mathrm{d} V.
$$

类似可得物体 $V$ 对于 $y$ 轴与 $z$ 轴的转动惯量分别为

$$
J _ {y} = \iiint_ {V} (z ^ {2} + x ^ {2}) \rho (x, y, z) \mathrm{d} V,
$$

$$
J _ {z} = \iiint_ {V} (x ^ {2} + y ^ {2}) \rho (x, y, z) \mathrm{d} V.
$$

同理,物体 V 对于坐标平面的转动惯量分别为

$$
\begin{array}{l} J _ {x y} = \iiint_ {V} z ^ {2} \rho (x, y, z) \mathrm{d} V, \\ J _ {y z} = \iiint_ {V} x ^ {2} \rho (x, y, z) \mathrm{d} V, \\ J _ {z x} = \iiint_ {V} y ^ {2} \rho (x, y, z) \mathrm{d} V. \\ \end{array}
$$

据此,读者也容易建立平面薄板对于坐标轴的转动惯量:

$$
J _ {x} = \iint_ {D} y ^ {2} \rho (x, y) \mathrm{d} \sigma , \quad J _ {y} = \iint_ {D} x ^ {2} \rho (x, y) \mathrm{d} \sigma
$$

以及

$$
J _ {l} = \iint_ {D} r ^ {2} (x, y) \rho (x, y) \mathrm{d} \sigma ,
$$

这里 l 为转动轴,  $r(x,y)$  为 D 中点  $(x,y)$  到 l 的距离函数.

例 5 求密度均匀的圆环 D 对于垂直于圆环面中心轴的转动惯量(图21-41).

解 设圆环 D 为

$$
R _ {1} ^ {2} \leqslant x ^ {2} + y ^ {2} \leqslant R _ {2} ^ {2},
$$

密度为 $\rho$ ，则 $D$ 中任一点 $(x,y)$ 与转轴的距离平方为 $x^{2} + y^{2}$ .于是转动惯量

$$
\begin{array}{l} J = \iint_ {D} \rho (x ^ {2} + y ^ {2}) \mathrm{d} \sigma = \rho \int_ {0} ^ {2 \pi} \mathrm{d} \theta \int_ {R _ {1}} ^ {R _ {2}} r ^ {3} \mathrm{d} r \\ = \frac {\pi \rho}{2} (R _ {2} ^ {4} - R _ {1} ^ {4}) = \frac {m}{2} (R _ {2} ^ {2} + R _ {1} ^ {2}), \\ \end{array}
$$

其中 m 为圆环的质量.

例 6 求均匀圆盘 D 对于其直径的转动惯量(图 21-42).

解 设圆盘 $D$ 为 $x^{2} + y^{2}\leqslant R^{2}$ ，密度为 $\rho$ ，求对于 $y$ 轴的转动惯量.由于 $D$ 内任一点$(x,y)$ 与 $y$ 轴的距离为 $|x|$ ，故

$$
\begin{array}{l} J = \iint_ {D} \rho x ^ {2} \mathrm{d} \sigma = \rho \int_ {0} ^ {2 \pi} \mathrm{d} \theta \int_ {0} ^ {R} (r \cos \theta) ^ {2} r \mathrm{d} r \\ = \rho \int_ {0} ^ {2 \pi} \cos^ {2} \theta \mathrm{d} \theta \int_ {0} ^ {R} r ^ {3} \mathrm{d} r \\ = \frac {\rho \pi R ^ {4}}{4} = \frac {1}{4} m R ^ {2}, \\ \end{array}
$$

其中 m 为圆盘的质量.

![](images/page_247_image_10.jpg)

<details>
<summary>text_image</summary>

z
D
O
y
x
</details>

图21-41

![](images/page_247_image_12.jpg)

<details>
<summary>text_image</summary>

y
D
O
R
x
</details>

图21-42

例 7 设某球体的密度与球心的距离成正比, 求它对于切平面的转动惯量.

解 设球体由不等式 $x^{2} + y^{2} + z^{2}\leqslant R^{2}$ 表示，密度函数为 $k\sqrt{x^2 + y^2 + z^2}$ ，这里 $k$ 为比例常数.切平面方程为 $x = R$ ，则球体对于平面 $x = R$ 的转动惯量为

$$
\begin{array}{l} J = k \iiint_ {V} \sqrt {x ^ {2} + y ^ {2} + z ^ {2}} (R - x) ^ {2} \mathrm{d} x \mathrm{d} y \mathrm{d} z \\ = k \int_ {0} ^ {2 \pi} \mathrm{d} \theta \int_ {0} ^ {\pi} \mathrm{d} \varphi \int_ {0} ^ {R} (R - r \sin \varphi \cos \theta) ^ {2} r ^ {3} \sin \varphi \mathrm{d} r \\ = k R ^ {2} \int_ {0} ^ {2 \pi} \mathrm{d} \theta \int_ {0} ^ {R} r ^ {3} \mathrm{d} r \int_ {0} ^ {\pi} \sin \varphi \mathrm{d} \varphi - 2 k R \int_ {0} ^ {2 \pi} \cos \theta \mathrm{d} \theta \int_ {0} ^ {R} r ^ {4} \mathrm{d} r \int_ {0} ^ {\pi} \sin^ {2} \varphi \mathrm{d} \varphi + \\ k \int_ {0} ^ {2 \pi} \cos^ {2} \theta \mathrm{d} \theta \int_ {0} ^ {R} r ^ {5} \mathrm{d} r \int_ {0} ^ {\pi} \sin^ {3} \varphi \mathrm{d} \varphi \\ = \frac {1 1}{9} k \pi R ^ {6}. \\ \end{array}
$$

## 四、引力

求密度为  $\rho(x,y,z)$  的立体对立体外质量为 1 的质点 A 的引力.

设 A 的坐标为  $(\xi, \eta, \zeta)$ ，V 中点的坐标用  $(x, y, z)$  表示。我们使用微元法来求 V 对 A 的引力。V 中质量微元  $dm = \rho dV$  对 A 的引力在坐标轴上的投影为

$$
\mathrm{d} F _ {x} = k \frac {x - \xi}{r ^ {3}} \rho \mathrm{d} V, \mathrm{d} F _ {y} = k \frac {y - \eta}{r ^ {3}} \rho \mathrm{d} V, \mathrm{d} F _ {z} = k \frac {z - \zeta}{r ^ {3}} \rho \mathrm{d} V,
$$

其中 k 为引力系数，

$$
r = \sqrt {(x - \xi) ^ {2} + (y - \eta) ^ {2} + (z - \zeta) ^ {2}}
$$

是 A 到 dV 的距离, 于是力 F 在三个坐标轴上的投影分别为

$$
F _ {x} = k \iiint_ {V} \frac {x - \xi}{r ^ {3}} \rho \mathrm{d} V, \quad F _ {y} = k \iiint_ {V} \frac {y - \eta}{r ^ {3}} \rho \mathrm{d} V, \quad F _ {z} = k \iiint_ {V} \frac {z - \zeta}{r ^ {3}} \rho \mathrm{d} V,
$$

所以

$$
\boldsymbol {F} = F _ {x} \boldsymbol {i} + F _ {y} \boldsymbol {j} + F _ {z} \boldsymbol {k}.
$$

例 8 设球体 V 具有均匀的密度  $\rho$ ，求 V 对球外一点 A（质量为 1）的引力（引力系数为 k）.

解 设球体为 $x^{2} + y^{2} + z^{2}\leqslant R^{2}$ ，球外一点 $A$ 的坐标为 $(0,0,a)$ （ $R <   a$ ).显然有 $F_{x} = F_{y} = 0$ ，现在计算 $F_{z}$ .由上述公式，

$$
\begin{array}{l} F _ {z} = k \iiint_ {V} \frac {(z - a)}{\left[ x ^ {2} + y ^ {2} + (z - a) ^ {2} \right] ^ {3 / 2}} \rho \mathrm{d} x \mathrm{d} y \mathrm{d} z \\ = k \rho \int_ {- R} ^ {R} (z - a) \mathrm{d} z \iint_ {D _ {z}} \frac {\mathrm{d} x \mathrm{d} y}{\left[ x ^ {2} + y ^ {2} + (z - a) ^ {2} \right] ^ {3 / 2}}, \\ \end{array}
$$

其中 $D_{z} = \{(x,y) | x^{2} + y^{2} \leqslant R^{2} - z^{2}\}$. 用极坐标计算

$$
\begin{array}{l} F _ {z} = k \rho \int_ {- R} ^ {R} (z - a) \mathrm{d} z \int_ {0} ^ {2 \pi} \mathrm{d} \theta \int_ {0} ^ {\sqrt {R ^ {2} - z ^ {2}}} \frac {r}{\left[ r ^ {2} + (z - a) ^ {2} \right] ^ {3 / 2}} \mathrm{d} r \\ = 2 \pi k \rho \int_ {- R} ^ {R} \left(- 1 - \frac {z - a}{\sqrt {R ^ {2} - 2 a z + a ^ {2}}}\right) \mathrm{d} z \\ = - \frac {4}{3 a ^ {2}} \pi R ^ {3} \rho k. \\ \end{array}
$$

上面我们只讨论了重积分在力学中的应用. 实际上, 也可用第一型曲线积分(包括在下一章中将要讨论的第一型曲面积分)来计算空间曲线(曲面)的质心, 关于转动轴或坐标平面的转动惯量以及曲线(曲面)对其外一质点的引力. 这里就不再一一细述了, 读者可仿照上面的方法建立相应的计算公式.

## 习题 21.6

1. 求曲面 az = xy 包含在圆柱  $x^{2} + y^{2} = a^{2}$  内那部分的面积.
2. 求锥面  $z = \sqrt{x^{2} + y^{2}}$  被柱面  $z^{2} = 2x$  所截部分的曲面面积.
3. 求下列均匀密度的平面薄板质心:

(1) 半椭圆 $\frac{x^{2}}{a^{2}}+\frac{y^{2}}{b^{2}}\leqslant1,y\geqslant0;$

(2) 高为 h, 底分别为 a 和 b 的等腰梯形.

（注:以梯形长为 a 的底边的中点为原点，该底所在直线为 x 轴建立平面直角坐标系，并使梯形位于 x 轴上方。）

4. 求下列均匀密度物体的质心:

(1) $z \leqslant 1 - x^{2} - y^{2}, z \geqslant 0$;
(2) 由坐标面及平面  $x+2y-z=1$  所围的四面体.

5. 求下列均匀密度的平面薄板的转动惯量:

(1) 半径为 R 的圆关于其切线的转动惯量；
(2) 边长为 a 和 b、夹角为  $\varphi$  的平行四边形，关于底边 b 的转动惯量.

6. 计算下列引力:

(1) 均匀薄片  $x^{2} + y^{2} \leqslant R^{2}, z = 0$  对于轴上一点  $(0, 0, c)$  (c > 0) 处的单位质量的引力:
(2) 均匀柱体  $x^{2} + y^{2} \leqslant a^{2}, 0 \leqslant z \leqslant h$  对于点  $P(0, 0, c)$  (c > h) 处的单位质量的引力；
(3) 均匀密度的正圆锥体 (高为 $h$, 底面半径为 $R$) 对于在它的顶点处质量为 $m$ 的质点的引力.

(注:以圆锥底面圆心为原点,底面所在平面为 xy 平面建立空间直角坐标系,圆锥顶点在  $(0,0,h)$ .)

7. 求曲面

$$
\left\{ \begin{array}{l} x = (b + a \cos \psi) \cos \varphi , \\ y = (b + a \cos \psi) \sin \varphi , \\ z = a \sin \psi , \end{array} \right. \quad 0 \leqslant \varphi \leqslant 2 \pi , 0 \leqslant \psi \leqslant 2 \pi
$$

的面积,其中常数 a,b 满足  $0 \leqslant a \leqslant b$ .

8. 求螺旋面

$$
\left\{ \begin{array}{l} x = r \cos \varphi , \\ y = r \sin \varphi , \\ z = b \varphi , \end{array} \right. \quad 0 \leqslant r \leqslant a, 0 \leqslant \varphi \leqslant 2 \pi
$$

的面积.

9. 求边长为 a、密度均匀的立方体关于其任一棱边的转动惯量.

## \* §7 n 重积分

对于 n 重积分, 我们先介绍一个物理模型, 即两个物体  $V_{1}$  与  $V_{2}$  之间的引力问题.

设物体 $V_{1}$ 中点的坐标为 $(x_{1},y_{1},z_{1}), V_{2}$ 中点的坐标为 $(x_{2},y_{2},z_{2})$ ，它们的密度函数分别为连续函数 $\rho_{1}(x_{1},y_{1},z_{1})$ 与 $\rho_{2}(x_{2},y_{2},z_{2})$ ，且设它们之间的引力系数为1.我们用微元法求它们之间的引力.为此，在 $V_{1}$ 中取质量微元 $\rho_{1}\mathrm{d}x_{1}\mathrm{d}y_{1}\mathrm{d}z_{1}$ ，在 $V_{2}$ 中取质量微元 $\rho_{2}\mathrm{d}x_{2}\mathrm{d}y_{2}\mathrm{d}z_{2}$ .由万有引力定律知道， $V_{1}$ 的微元对 $V_{2}$ 的微元的吸引力在 $x$ 轴上的投影为

$$
\frac {\rho_ {1} \rho_ {2} (x _ {1} - x _ {2}) \mathrm{d} x _ {1} \mathrm{d} y _ {1} \mathrm{d} z _ {1} \mathrm{d} x _ {2} \mathrm{d} y _ {2} \mathrm{d} z _ {2}}{r ^ {3}},
$$

其中 $r = \sqrt{(x_1 - x_2)^2 + (y_1 - y_2)^2 + (z_1 - z_2)^2}$. 把两个物体的所有微元间的吸引力在 $x$ 轴上投影的量相加，就得到物体 $V_{1}$ 与 $V_{2}$ 间的引力在 $x$ 轴上投影的值. 它是一个六重积分，即

$$
F _ {x} = \iiint_ {V} \frac {\rho_ {1} (x _ {1} , y _ {1} , z _ {1}) \rho_ {2} (x _ {2} , y _ {2} , z _ {2}) (x _ {1} - x _ {2})}{r ^ {3}} \mathrm{d} x _ {1} \mathrm{d} y _ {1} \mathrm{d} z _ {1} \mathrm{d} x _ {2} \mathrm{d} y _ {2} \mathrm{d} z _ {2}.
$$

这个积分是在由六维数组 $(x_{1},y_{1},z_{1},x_{2},y_{2},z_{2})$ 构成的六维空间中的六维区域 $V = V_{1}\times V_{2}$ 上的积分.吸引力在 $y$ 和 $z$ 轴上的投影也同样可由六个自变量的积分形式来表示，这就是 $n$ 重积分 $(n = 6)$ 的一个例子.

建立 n 重积分概念,首先必须像定义平面图形面积一样定义 n 维空间区域的体积问题.最简单的 n 维区域——n 维长方体

$$
V = \left[ a _ {1}, b _ {1} \right] \times \left[ a _ {2}, b _ {2} \right] \times \dots \times \left[ a _ {n}, b _ {n} \right]
$$

的体积规定为 $(b_{1}-a_{1})(b_{2}-a_{2})\cdots(b_{n}-a_{n})$ . 在仿照可求面积概念那样建立 n 维区域的可求体积概念之后, 可以证明 n 维单纯形

$$
x _ {1} \geqslant 0, x _ {2} \geqslant 0, \dots , x _ {n} \geqslant 0, x _ {1} + x _ {2} + \dots + x _ {n} \leqslant h
$$

和 $n$ 维球体

$$
x _ {1} ^ {2} + x _ {2} ^ {2} + \dots + x _ {n} ^ {2} \leqslant R ^ {2}
$$

的体积是存在的.

设 n 元函数  $f(x_{1}, x_{2}, \cdots, x_{n})$  定义在 n 维可求体积的区域 V 上. 像二重积分概念那样, 通过对 V 的分割、近似求和、取极限的过程, 便得到 n 重积分的概念:

$$
I = \overbrace {\int_ {V} \cdots \int f (x _ {1} , x _ {2} , \cdots , x _ {n}) \mathrm{d} x _ {1} \cdots \mathrm{d} x _ {n}} ^ {n \text {个}}. \tag {1}
$$

与二重积分相仿,n 重积分也有如下一些结论:

若 $f(x_{1},\cdots,x_{n})$ 在 n 维有界闭区域 V 上连续，则 n 重积分(1)必存在.

计算 n 重积分的办法是把它化为重数较低的积分来计算. 如当积分区域是长方体  $\left[a_{1}, b_{1}\right] \times \left[a_{2}, b_{2}\right] \times \cdots \times \left[a_{n}, b_{n}\right]$  时, 则有

$$
I = \int_ {a _ {1}} ^ {b _ {1}} \mathrm{d} x _ {1} \int_ {a _ {2}} ^ {b _ {2}} \mathrm{d} x _ {2} \dots \int_ {a _ {n}} ^ {b _ {n}} f (x _ {1}, \dots , x _ {n}) \mathrm{d} x _ {n}.
$$

当 V 由不等式组  $a_{1} \leqslant x_{1} \leqslant b_{1}, a_{2}(x_{1}) \leqslant x_{2} \leqslant b_{2}(x_{1}), \cdots, a_{n}(x_{1}, \cdots, x_{n-1}) \leqslant x_{n} \leqslant b_{n}(x_{1}, \cdots, x_{n-1})$  表示时，则有

$$
I = \int_ {a _ {1}} ^ {b _ {1}} \mathrm{d} x _ {1} \int_ {a _ {2} (x _ {1})} ^ {b _ {2} (x _ {1})} \mathrm{d} x _ {2} \dots \int_ {a _ {n} (x _ {1}, \dots , x _ {n - 1})} ^ {b _ {n} (x _ {1}, \dots , x _ {n - 1})} f (x _ {1}, \dots , x _ {n}) \mathrm{d} x _ {n}.
$$

设变换

$$
T: \left\{ \begin{array}{l} x _ {1} = x _ {1} (\xi_ {1}, \xi_ {2}, \dots , \xi_ {n}), \\ x _ {2} = x _ {2} (\xi_ {1}, \xi_ {2}, \dots , \xi_ {n}), \\ \dots \dots \\ x _ {n} = x _ {n} (\xi_ {1}, \xi_ {2}, \dots , \xi_ {n}) \end{array} \right.
$$

把 n 维  $\xi_{1}\xi_{2}\cdots\xi_{n}$  空间区域  $V'$  一对一地映射成 n 维  $x_{1}x_{2}\cdots x_{n}$  空间中的区域 V，且在  $V'$  上函数行列式

$$
J = \frac {\partial (x _ {1} , x _ {2} , \cdots , x _ {n})}{\partial (\xi_ {1} , \xi_ {2} , \cdots , \xi_ {n})} = \left| \begin{array}{c c c c} \frac {\partial x _ {1}}{\partial \xi_ {1}} & \frac {\partial x _ {1}}{\partial \xi_ {2}} & \dots & \frac {\partial x _ {1}}{\partial \xi_ {n}} \\ \frac {\partial x _ {2}}{\partial \xi_ {1}} & \frac {\partial x _ {2}}{\partial \xi_ {2}} & \dots & \frac {\partial x _ {2}}{\partial \xi_ {n}} \\ \vdots & \vdots & & \vdots \\ \frac {\partial x _ {n}}{\partial \xi_ {1}} & \frac {\partial x _ {n}}{\partial \xi_ {2}} & \dots & \frac {\partial x _ {n}}{\partial \xi_ {n}} \end{array} \right|
$$

恒不为零,则成立下列 n 重积分的换元公式:

$$
\begin{array}{l} I = \overbrace {\int_ {V} \cdots \int f \left(x _ {1} , x _ {2} , \cdots , x _ {n}\right) \mathrm{d} x _ {1} \mathrm{d} x _ {2} \cdots \mathrm{d} x _ {n}} ^ {n \text {个}} \\ = \overbrace {\int \cdots \int} ^ {n \text {个}} f \left(x _ {1} \left(\xi_ {1}, \dots , \xi_ {n}\right), x _ {2} \left(\xi_ {1}, \dots , \xi_ {n}\right), \dots , x _ {n} \left(\xi_ {1}, \dots , \xi_ {n}\right)\right) | J | \mathrm{d} \xi_ {1} \mathrm{d} \xi_ {2} \dots \mathrm{d} \xi_ {n}. \\ \end{array}
$$

例 1 求 n 维单纯形  $T_{n}: x_{1} \geqslant 0, x_{2} \geqslant 0, \cdots, x_{n} \geqslant 0, x_{1} + x_{2} + \cdots + x_{n} \leqslant h$  的体积  $\Delta T_{n}$ .

解  $\Delta T_{n}=\overbrace{\int\cdots\int}_{T_{n}}^{n个}\mathrm{d}x_{1}\mathrm{d}x_{2}\cdots\mathrm{d}x_{n}.$  作变换

$$
x _ {1} = h \xi_ {1}, x _ {2} = h \xi_ {2}, \dots , x _ {n} = h \xi_ {n}.
$$

这时  $J=h^{n}$ ，因此有

$$
\Delta T _ {n} = h ^ {n} \overbrace {\int_ {D _ {1}} ^ {n \text {个}} \mathrm{d} \xi_ {1} \mathrm{d} \xi_ {2} \cdots \mathrm{d} \xi_ {n}} ^ {n}\left. \right) = h ^ {n} \alpha_ {n},
$$

其中

$$
D _ {1} = \left\{\left(\xi_ {1}, \xi_ {2}, \dots , \xi_ {n}\right) \mid \xi_ {1} + \xi_ {2} + \dots + \xi_ {n} \leqslant 1, \xi_ {1} \geqslant 0, \xi_ {2} \geqslant 0, \dots , \xi_ {n} \geqslant 0 \right\},
$$

$$
\alpha_ {n} = \int_ {0} ^ {1} \mathrm{d} \xi_ {n} \overbrace {\int \cdots \int} ^ {n - 1 \text {个}} \mathrm{d} \xi_ {1} \mathrm{d} \xi_ {2} \dots \mathrm{d} \xi_ {n - 1}, \tag {2}
$$

这里

$$
T _ {n - 1} = \left\{\left(\xi_ {1}, \xi_ {2}, \dots , \xi_ {n - 1}\right) \mid \xi_ {1} + \xi_ {2} + \dots + \xi_ {n - 1} \leqslant 1 - \xi_ {n}, \xi_ {1} \geqslant 0, \xi_ {2} \geqslant 0, \dots , \xi_ {n - 1} \geqslant 0 \right\}.
$$

对积分(2)作变换

$$
\xi_ {1} = (1 - \xi_ {n}) \zeta_ {1}, \dots , \xi_ {n - 1} = (1 - \xi_ {n}) \zeta_ {n - 1}.
$$

这时 $J = (1 - \xi_{n})^{n - 1}$ ，因此有

$$
\begin{array}{l} \alpha_ {n} = \int_ {0} ^ {1} \left(1 - \xi_ {n}\right) ^ {n - 1} \mathrm{d} \xi_ {n} \overbrace {\int_ {D _ {2}} \cdots \int} ^ {n - 1 \text {个}} \mathrm{d} \zeta_ {1} \mathrm{d} \zeta_ {2} \dots \mathrm{d} \zeta_ {n - 1} \\ = \alpha_ {n - 1} \int_ {0} ^ {1} (1 - \xi_ {n}) ^ {n - 1} \mathrm{d} \xi_ {n} = \frac {\alpha_ {n - 1}}{n}, \\ \end{array}
$$

其中  $D_{2}=\left\{\left(\zeta_{1},\zeta_{2},\cdots,\zeta_{n-1}\right)\mid\zeta_{1}+\cdots+\zeta_{n-1}\leqslant1,\zeta_{1}\geqslant0,\cdots,\zeta_{n-1}\geqslant0\right\}$ . 这是一个递推公式. 由于当 n=1 时,  $\alpha_{1}=1$ , 因此

$$
\alpha_ {n} = \frac {1}{n !}.
$$

于是  $\Delta T_{n}=\frac{h^{n}}{n!}$ .

例 2 求 n 维球体  $V_{n}: x_{1}^{2} + x_{2}^{2} + \cdots + x_{n}^{2} \leqslant R^{2}$  的体积  $\Delta V_{n}$ .

解  $\Delta V_{n}=\overbrace{\int\cdots\int}_{x_{1}^{2}+\cdots+x_{n}^{2}\leqslant R^{2}}^{\text{n个}}\mathrm{d}x_{1}\cdots\mathrm{d}x_{n}.$

作变换  $x_{1}=R\xi_{1},\cdots,x_{n}=R\xi_{n}$ . 这时  $J=R^{n}$ ，因此有

$$
\Delta V _ {n} = R ^ {n} \overbrace {\int \cdots \int} ^ {n \text {个}} \mathrm{d} \xi_ {1} \dots \mathrm{d} \xi_ {n} = R ^ {n} \beta_ {n},
$$

其中

$$
\beta_ {n} = \int_ {- 1} ^ {1} \mathrm{d} \xi_ {n} \overbrace {\int \cdots \int} ^ {n - 1 \text {个}} \mathrm{d} \xi_ {1} \dots \mathrm{d} \xi_ {n - 1}.
$$

它是 $n$ 维单位球体的体积. 注意 $\beta_{n}$ 中右边的 $n - 1$ 重积分表示以 $\sqrt{1 - \xi_n^2}$ 为半径的 $n - 1$ 维球体的体积. 因而它应等于 $\beta_{n - 1}(1 - \xi_n^2)^{\frac{n - 1}{2}}$, 其中 $\beta_{n - 1}$ 为 $n - 1$ 维单位球体的体积. 于是有

$$
\beta_ {n} = \int_ {- 1} ^ {1} (1 - \xi_ {n} ^ {2}) ^ {\frac {n - 1}{2}} \mathrm{d} \xi_ {n} \cdot \beta_ {n - 1}.
$$

令 $\xi_{n} = \cos \theta$ ，又得一递推公式

$$
\beta_ {n} = 2 \beta_ {n - 1} \int_ {0} ^ {\frac {\pi}{2}} \sin^ {n} \theta \mathrm{d} \theta .
$$

由于

$$
\int_ {0} ^ {\frac {\pi}{2}} \sin^ {n} \theta \mathrm{d} \theta = \left\{ \begin{array}{l l} \frac {(2 m - 1) ! !}{(2 m) ! !} \frac {\pi}{2}, & n = 2 m, \\ \frac {(2 m) ! !}{(2 m + 1) ! !}, & n = 2 m + 1 \end{array} \right.
$$

和 $\beta_{1} = 2$ ，所以

$$
\Delta V _ {n} = R ^ {n} \beta_ {n} = \left\{ \begin{array}{l l} \frac {R ^ {2 m}}{m !} \pi^ {m}, & n = 2 m, \\ \frac {2 R ^ {2 m + 1} (2 \pi) ^ {m}}{(2 m + 1) ! !}, & n = 2 m + 1. \end{array} \right.
$$

特别当 n=1,2,3 时,有

$$
\Delta V _ {1} = 2 R, \Delta V _ {2} = \pi R ^ {2}, \Delta V _ {3} = \frac {4}{3} \pi R ^ {3}.
$$

本题也可用 n 维球坐标变换求得. n 维球坐标变换为

$$
\begin{array}{l} x _ {1} = r \cos \varphi_ {1}, \\ x _ {2} = r \sin \varphi_ {1} \cos \varphi_ {2}, \\ x _ {3} = r \sin \varphi_ {1} \sin \varphi_ {2} \cos \varphi_ {3}, \\ \dots \\ x _ {n - 1} = r \sin \varphi_ {1} \sin \varphi_ {2} \dots \sin \varphi_ {n - 2} \cos \varphi_ {n - 1}, \\ x _ {n} = r \sin \varphi_ {1} \sin \varphi_ {2} \dots \sin \varphi_ {n - 2} \sin \varphi_ {n - 1}. \\ \end{array}
$$

因此有

$$
J = r ^ {n - 1} \sin^ {n - 2} \varphi_ {1} \sin^ {n - 3} \varphi_ {2} \dots \sin^ {2} \varphi_ {n - 3} \sin \varphi_ {n - 2}.
$$

因为积分区域为

$$
0 \leqslant r \leqslant R, 0 \leqslant \varphi_ {1}, \varphi_ {2}, \dots , \varphi_ {n - 2} \leqslant \pi , 0 \leqslant \varphi_ {n - 1} \leqslant 2 \pi,
$$

所以

$$
\begin{array}{l} \Delta V _ {n} = \int_ {0} ^ {R} \mathrm{d} r \int_ {0} ^ {\pi} \mathrm{d} \varphi_ {1} \dots \int_ {0} ^ {\pi} \mathrm{d} \varphi_ {n - 2} \int_ {0} ^ {2 \pi} r ^ {n - 1} \sin^ {n - 2} \varphi_ {1} \dots \sin \varphi_ {n - 2} \mathrm{d} \varphi_ {n - 1} \\ = \frac {1}{n} R ^ {n} \left(\int_ {0} ^ {\pi} \sin^ {n - 2} \varphi_ {1} \mathrm{d} \varphi_ {1}\right) \left(\int_ {0} ^ {\pi} \sin^ {n - 3} \varphi_ {2} \mathrm{d} \varphi_ {2}\right) \dots \left(\int_ {0} ^ {\pi} \sin \varphi_ {n - 2} \mathrm{d} \varphi_ {n - 2}\right) \left(\int_ {0} ^ {2 \pi} \mathrm{d} \varphi_ {n - 1}\right). \\ \end{array}
$$

这与上面的结果完全一致.

![](images/page_253_image_9.jpg)

例 3 求 n 维单位球面  $x_{1}^{2} + x_{2}^{2} + \cdots + x_{n}^{2} = 1$  的面积.

解 设  $x_{n}=f(x_{1},\cdots,x_{n-1}),(x_{1},x_{2},\cdots,x_{n-1})\in\Delta\subset\mathbf{R}^{n-1}$  为 n 维空间中的曲面, 则其面积为

$$
\overbrace {\int \cdots \int} _ {\Delta} \sqrt {1 + \left(\frac {\partial x _ {n}}{\partial x _ {1}}\right) ^ {2} + \cdots + \left(\frac {\partial x _ {n}}{\partial x _ {n - 1}}\right) ^ {2}} \mathrm{d} x _ {1} \dots \mathrm{d} x _ {n - 1}.
$$

因 $n$ 维单位球面的上半部可由方程

$$
x _ {n} = \sqrt {1 - (x _ {1} ^ {2} + \cdots + x _ {n - 1} ^ {2})} \quad (x _ {1} ^ {2} + \dots + x _ {n - 1} ^ {2} \leqslant 1)
$$

确定,又由于

$$
\sqrt {1 + \left(\frac {\partial x _ {n}}{\partial x _ {1}}\right) ^ {2} + \cdots + \left(\frac {\partial x _ {n}}{\partial x _ {n - 1}}\right) ^ {2}} = \frac {1}{x _ {n}},
$$

所以上半球面面积

$$
\begin{array}{l} \frac {1}{2} \Delta S = \overbrace {\int \cdots \int} ^ {n - 1 \text {个}} \frac {\mathrm{d} x _ {1} \cdots \mathrm{d} x _ {n - 1}}{x _ {n}} \\ = \overbrace {\int \cdots \int} _ {x _ {1} ^ {2} + \dots + x _ {n - 1} ^ {2} \leqslant 1} ^ {n - 1 \text {个}} \frac {\mathrm{d} x _ {1} \cdots \mathrm{d} x _ {n - 1}}{\sqrt {1 - \left(x _ {1} ^ {2} + \cdots + x _ {n - 1} ^ {2}\right)}} \\ = \overbrace {\int \cdots \int} ^ {n - 2 \text {个}} \mathrm{d} x _ {1} \dots \mathrm{d} x _ {n - 2} \int_ {- \sqrt {1 - \left(x _ {1} ^ {2} + \cdots + x _ {n - 2} ^ {2}\right)}} ^ {\sqrt {1 - \left(x _ {1} ^ {2} + \cdots + x _ {n - 2} ^ {2}\right)}} \frac {\mathrm{d} x _ {n - 1}}{\sqrt {1 - \left(x _ {1} ^ {2} + \cdots + x _ {n - 1} ^ {2}\right)}}. \\ \end{array}
$$

由于对变量 $x_{n - 1}$ 的积分等于 $\pi$ ，从而有

$$
\frac {1}{2} \Delta S = \pi \overbrace {\int \cdots \int} ^ {n - 2 \text {个}} \mathrm{d} x _ {1} \dots \mathrm{d} x _ {n - 2} = \pi \beta_ {n - 2},
$$

其中  $\beta_{n-2}=\overbrace{\int\cdots\int}_{x_{1}^{2}+\cdots+x_{n-2}^{2}\leqslant1}\mathrm{d}x_{1}\cdots\mathrm{d}x_{n-2}$  为 n-2 维空间中单位球体体积. 因此由例 2 得 n 维球面面积为

$$
\Delta S _ {n} = 2 \pi \beta_ {n - 2} = \left\{ \begin{array}{l l} \frac {2 \pi^ {m}}{(m - 1) !}, & n = 2 m, \\ \frac {2 (2 \pi) ^ {m}}{(2 m - 1) ! !}, & n = 2 m + 1. \end{array} \right.
$$

特别当 $n = 2,3$ 时，它们分别为 $\Delta S_2 = 2\pi ,\Delta S_3 = 4\pi .$

## 习题 21.7

1. 计算五重积分

$$
\iiint_ {V} \mathrm{d} x \mathrm{d} y \mathrm{d} z \mathrm{d} u \mathrm{d} v,
$$

其中 $V: x^{2} + y^{2} + z^{2} + u^{2} + v^{2} \leqslant r^{2}$.

2. 计算四重积分

$$
\iiint_ {V} \sqrt {\frac {1 - x ^ {2} - y ^ {2} - z ^ {2} - u ^ {2}}{1 + x ^ {2} + y ^ {2} + z ^ {2} + u ^ {2}}} \mathrm{d} x \mathrm{d} y \mathrm{d} z \mathrm{d} u,
$$

其中 $V: x^{2} + y^{2} + z^{2} + u^{2} \leqslant 1$.

3. 求 n 维角锥  $x_{i} \geqslant 0, \frac{x_{1}}{a_{1}} + \frac{x_{2}}{a_{2}} + \cdots + \frac{x_{n}}{a_{n}} \leqslant 1, a_{i} > 0 (i = 1, 2, \cdots, n)$  的体积.
4. 把  $\Omega: x_{1}^{2} + x_{2}^{2} + \cdots + x_{n}^{2} \leqslant R^{2}$  上的  $n (n \geqslant 2)$  重积分

$$
\overbrace {\int \cdots \int} _ {\Omega} f \left(\sqrt {x _ {1} ^ {2} + x _ {2} ^ {2} + \cdots + x _ {n} ^ {2}}\right) \mathrm{d} x _ {1} \mathrm{d} x _ {2} \dots \mathrm{d} x _ {n}
$$

化为单重积分,其中 $f(u)$ 为连续函数.

## \* §8 反常二重积分

前面我们是在有界区域上讨论有界函数的二重积分. 本节将研究无界区域上或无界函数的二重积分.

## 一、无界区域上的二重积分

定义1 设 $f(x, y)$ 为定义在无界区域 $D$ 上的二元函数. 若对于平面上任一包围原点的光滑封闭曲线 $\gamma, f(x, y)$ 在曲线 $\gamma$ 所围的有界区域 $E_{\gamma}$ 与 $D$ 的交集 $E_{\gamma} \cap D = D_{\gamma}$ （图

21-43) 上恒可积. 令

$$
d _ {\gamma} = \inf \{\sqrt {x ^ {2} + y ^ {2}} | (x, y) \in \gamma \}.
$$

若极限

$$
\lim _ {d _ {\gamma} \to + \infty} \iint_ {D _ {\gamma}} f (x, y)   \mathrm{d} \sigma
$$

存在且有限,且与  $\gamma$  的取法无关,则称  $f(x,y)$  在 D 上的反常二重积分收敛,并记

$$
\iint_ {D} f (x, y) \mathrm{d} \sigma = \lim _ {d _ {\gamma} \to + \infty} \iint_ {D _ {\gamma}} f (x, y) \mathrm{d} \sigma , \tag {1}
$$

否则称 $f(x,y)$ 在 $D$ 上的反常二重积分发散，或简称 $\iint_{D} f(x,y) \, \mathrm{d}\sigma$ 发散.

定理 21.17 设在无界区域 D 上  $f(x,y) \geqslant 0, \gamma_{1}, \gamma_{2}, \cdots, \gamma_{n}, \cdots$  为一列包围原点的光滑封闭曲线序列，满足

(i)  $d_{n}=\inf\left\{\sqrt{x^{2}+y^{2}}\mid(x,y)\in\gamma_{n}\right\}\rightarrow+\infty\quad(n\rightarrow\infty)$ ,
(ii) $I = \sup_{n}\iint_{D_n}f(x,y)\mathrm{d}\sigma < + \infty$

其中  $D_{n}$  为  $\gamma_{n}$  所围的有界区域  $E_{n}$  与 D 的交集, 则反常二重积分(1)收敛, 并且

![](images/page_255_image_13.jpg)

<details>
<summary>text_image</summary>

y
γ
D
Dγ
Eγ
O
x
</details>

图21-43

$$
\iint_ {D} f (x, y) \mathrm{d} \sigma = I.
$$

证 设 $\gamma'$ 为任何包围原点的光滑封闭曲线, 这曲线所围的区域记为 $E'$, 并记 $D' = E' \cap D$. 因为 $\lim_{n \to \infty} d_n = +\infty$, 因此存在 $n$, 使得 $D' \subset D_n \subset D$. 由于 $f(x, y) \geqslant 0$, 所以有

$$
\iint_ {D ^ {\prime}} f (x, y) \mathrm{d} \sigma \leqslant \iint_ {D _ {n}} f (x, y) \mathrm{d} \sigma \leqslant I.
$$

另一方面,因为

$$
I = \sup _ {n} \iint_ {D _ {n}} f (x, y) \mathrm{d} \sigma ,
$$

对于任给的 $\varepsilon > 0$ ，总有 $n_0$ ，使得

$$
\iint_ {D _ {n _ {0}}} f (x, y) \mathrm{d} \sigma > I - \varepsilon .
$$

对于充分大的  $d'$ ，区域  $D'$  又可包含  $D_{n_{0}}$ ，因而

$$
\iint_ {D ^ {\prime}} f (x, y) \mathrm{d} \sigma > I - \varepsilon .
$$

由

$$
I - \varepsilon <   \iint_ {D ^ {\prime}} f (x, y) \mathrm{d} \sigma \leqslant I
$$

知 $f(x,y)$ 在 $D$ 上的反常二重积分存在，且等于 $I$.

由定理21.17容易看到:若在D上 $f(x,y)\geqslant0$ ,且它在D的任何有界子区域上可积且积分值有界,则 $f(x,y)$ 在D上的反常二重积分存在.反过来,若 $f(x,y)$ 在D上的反