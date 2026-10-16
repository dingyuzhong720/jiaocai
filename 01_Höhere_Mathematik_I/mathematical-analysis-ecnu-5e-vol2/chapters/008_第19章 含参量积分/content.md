# 第19章 含参量积分

原始 PDF 第 171–192 页。

## 第十九章含参量积分

## §1 含参量正常积分

从本章开始我们讨论多元函数的各种积分问题,首先研究含参量积分.设 $f(x,y)$ 是定义在矩形区域 $R=[a,b]\times[c,d]$ 上的二元函数 $^{①}$ .当x取[a,b]上某定值时,函数 $f(x,y)$ 则是定义在 $[c,d]$ 上以y为自变量的一元函数.倘若这时 $f(x,y)$ 在 $[c,d]$ 上可积,则其积分值是x在 $[a,b]$ 上取值的函数,记它为 $\varphi(x)$ ,就有

$$
\varphi (x) = \int_ {c} ^ {d} f (x, y) \mathrm{d} y, x \in [ a, b ]. \tag {1}
$$

一般地，设 $f(x,y)$ 为定义在区域 $G = \{(x,y)\mid c(x)\leqslant y\leqslant d(x),a\leqslant x\leqslant b\}$ 上的二元函数，其中$c(x),d(x)$ 为定义在 $[a,b]$ 上的连续函数（图19-1），若对于 $[a,b]$ 上每一固定的 $x$ 值，$f(x,y)$ 作为 $y$ 的函数在闭区间 $[c(x),d(x)]$ 上可积，则其积分值是 $x$ 在 $[a,b]$ 上取值的函数，记作 $F(x)$ 时，就有

![](../../raw/pages_0161-0192/images/page_170_image_5.jpg)

<details>
<summary>text_image</summary>

y
y=d(x)
G
y=c(x)
O
a
b
x
</details>

图19-1

$$
F (x) = \int_ {c (x)} ^ {d (x)} f (x, y) \mathrm{d} y, x \in [ a, b ]. \tag {2}
$$

用积分形式所定义的这两个函数(1)与(2)，通称为定义在 $[a,b]$ 上含参量x的(正常)积分，或简称含参量积分.

下面讨论含参量积分的连续性、可微性与可积性.

定理 19.1（连续性） 若二元函数  $f(x,y)$  在矩形区域  $R=[a,b]\times[c,d]$  上连续，则函数

$$
\varphi (x) = \int_ {c} ^ {d} f (x, y)   \mathrm{d} y
$$

在 $[a,b]$ 上连续.

证 设 $x \in [a, b]$, 对充分小的 $\Delta x$, 有 $x + \Delta x \in [a, b]$ (若 $x$ 为区间的端点, 则仅考

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 在建立含参量积分的概念和讨论其连续性与可微性时, 矩形区域  $[a, b] \times [c, d]$  可改为更一般的区域  $I \times [c, d]$ , 其中 I 为区间.</span></small>

163

---

第十九章 含参量积分

虑  $\Delta x > 0$  或  $\Delta x < 0$  ), 于是

$$
\varphi (x + \Delta x) - \varphi (x) = \int_ {c} ^ {d} [ f (x + \Delta x, y) - f (x, y) ] \mathrm{d} y. \tag {3}
$$

由于 $f(x,y)$ 在有界闭域 $R$ 上连续，从而一致连续，即对任给的正数 $\varepsilon$ ，总存在某个正数$\delta$ ，对 $R$ 内任意两点 $(x_{1},y_{1})$ 与 $(x_{2},y_{2})$ ，只要

$$
\mid x _ {1} - x _ {2} \mid <   \delta , \quad \mid y _ {1} - y _ {2} \mid <   \delta ,
$$

就有

$$
\left| f (x _ {1}, y _ {1}) - f (x _ {2}, y _ {2}) \right| <   \varepsilon . \tag {4}
$$

所以由(3)，(4)可推得:当 $\left|\Delta x\right|<\delta$ 时，

$$
\begin{array}{l} \mid \varphi (x + \Delta x) - \varphi (x) \mid \leqslant \int_ {c} ^ {d} \mid f (x + \Delta x, y) - f (x, y) \mid \mathrm{d} y \\ <   \int_ {c} ^ {d} \varepsilon \mathrm{d} x = \varepsilon (d - c). \\ \end{array}
$$

这就证明了  $\varphi(x)$  在  $[a,b]$  上连续.

![](../../raw/pages_0161-0192/images/page_171_image_10.jpg)

同理可证: 若  $f(x,y)$  在矩形区域 R 上连续, 则含参量 y 的积分

$$
\psi (y) = \int_ {a} ^ {b} f (x, y) \mathrm{d} x \tag {5}
$$

在 $[c,d]$ 上连续.

对于定理19.1的结论也可以写成如下的形式:若 $f(x,y)$ 在矩形区域 $R$ 上连续，则对任何 $x_0\in [a,b]$ ，都有

$$
\lim _ {x \to x _ {0}} \int_ {c} ^ {d} f (x, y)   \mathrm{d} y = \int_ {c} ^ {d} \lim _ {x \to x _ {0}} f (x, y)   \mathrm{d} y.
$$

这个结论表明,定义在矩形区域上的连续函数,其极限运算与积分运算的顺序是可以交换的.

定理 19.2(连续性) 设二元函数  $f(x,y)$  在区域

$$
G = \{(x, y) \mid c (x) \leqslant y \leqslant d (x), a \leqslant x \leqslant b \}
$$

上连续,其中  $c(x)$ ,  $d(x)$  为  $[a,b]$  上的连续函数,则函数

$$
F (x) = \int_ {c (x)} ^ {d (x)} f (x, y) \mathrm{d} y \tag {6}
$$

在 $[a,b]$ 上连续.

证 对积分(6)用换元积分法,令

$$
y = c (x) + t (d (x) - c (x)).
$$

当 $y$ 在 $c(x)$ 与 $d(x)$ 之间取值时，$t$ 在 $[0,1]$ 上取值，且

$$
\mathrm{d} y = (d (x) - c (x)) \mathrm{d} t.
$$

所以从(6)式可得

$$
\begin{array}{l} F (x) = \int_ {c (x)} ^ {d (x)} f (x, y) \mathrm{d} y \\ = \int_ {0} ^ {1} f (x, c (x) + t (d (x) - c (x))) (d (x) - c (x)) \mathrm{d} t. \\ \end{array}
$$

由于被积函数

164

---

§ 1 含参量正常积分

$$
f (x, c (x) + t (d (x) - c (x))) (d (x) - c (x))
$$

在矩形区域 $[a, b] \times [0, 1]$ 上连续，由定理19.1得积分(6)所确定的函数 $F(x)$ 在 $[a, b]$ 上连续.

下面讨论含参量积分的求导运算与积分运算的可交换性.

定理 19.3(可微性) 若函数  $f(x,y)$  与其偏导数  $\frac{\partial}{\partial x}f(x,y)$  都在矩形区域  $R=[a,b]\times[c,d]$  上连续，则

$$
\varphi (x) = \int_ {c} ^ {d} f (x, y)   \mathrm{d} y
$$

在 $[a,b]$ 上可微，且

$$
\frac {\mathrm{d}}{\mathrm{d} x} \int_ {c} ^ {d} f (x, y) \mathrm{d} y = \int_ {c} ^ {d} \frac {\partial}{\partial x} f (x, y) \mathrm{d} y.
$$

证 对于 $[a, b]$ 内任一点 $x$, 设 $x + \Delta x \in [a, b]$ (若 $x$ 为区间端点, 则讨论单侧导数), 则

$$
\frac {\varphi (x + \Delta x) - \varphi (x)}{\Delta x} = \int_ {c} ^ {d} \frac {f (x + \Delta x , y) - f (x , y)}{\Delta x} \mathrm{d} y.
$$

由微分学的拉格朗日中值定理及 $f_{x}(x,y)$ 在有界闭域R上连续（从而一致连续），对任给正数 $\varepsilon$ ，存在正数 $\delta$ ，只要当 $|\Delta x|<\delta$ 时，就有

$$
\begin{array}{l} \left| \frac {f (x + \Delta x , y) - f (x , y)}{\Delta x} - f _ {x} (x, y) \right| \\ = \left| f _ {x} (x + \theta \Delta x, y) - f _ {x} (x, y) \right| <   \varepsilon , \\ \end{array}
$$

其中  $\theta\in(0,1)$ . 因此

$$
\begin{array}{l} \left| \frac {\Delta \varphi}{\Delta x} - \int_ {c} ^ {d} f _ {x} (x, y) \mathrm{d} y \right| \\ \leqslant \int_ {c} ^ {d} \left| \frac {f (x + \Delta x , y) - f (x , y)}{\Delta x} - f _ {x} (x, y) \right| \mathrm{d} y \\ <   \varepsilon (d - c). \\ \end{array}
$$

这就证得对一切 $x \in [a, b]$, 有

$$
\frac {\mathrm{d}}{\mathrm{d} x} \varphi (x) = \int_ {c} ^ {d} \frac {\partial}{\partial x} f (x, y) \mathrm{d} y.
$$

定理 19.4(可微性) 设  $f(x,y)$ ,  $f_{x}(x,y)$  在  $R=[a,b]\times[p,q]$  上连续,  $c(x)$ ,  $d(x)$  为定义在  $[a,b]$  上其值含于  $[p,q]$  内的可微函数, 则函数

$$
F (x) = \int_ {c (x)} ^ {d (x)} f (x, y) \mathrm{d} y
$$

在 $[a,b]$ 上可微，且

$$
F ^ {\prime} (x) = \int_ {c (x)} ^ {d (x)} f _ {x} (x, y) \mathrm{d} y + f (x, d (x)) d ^ {\prime} (x) - f (x, c (x)) c ^ {\prime} (x). \tag {7}
$$

证 把 $F(x)$ 看作复合函数

$$
\begin{array}{l} F (x) = H (x, c, d) = \int_ {c} ^ {d} f (x, y)   \mathrm{d} y, \\ c = c (x), d = d (x). \\ \end{array}
$$

165

---

第十九章 含参量积分

由复合函数求导法则及变限积分的求导法则,有

$$
\begin{array}{l} \frac {\mathrm{d}}{\mathrm{d} x} F (x) = \frac {\partial H}{\partial x} + \frac {\partial H}{\partial c} \frac {\mathrm{d} c}{\mathrm{d} x} + \frac {\partial H}{\partial d} \frac {\mathrm{d} d}{\mathrm{d} x} \\ = \int_ {c (x)} ^ {d (x)} f _ {x} (x, y) \mathrm{d} y + f (x, d (x)) d ^ {\prime} (x) - f (x, c (x)) c ^ {\prime} (x). \\ \end{array}
$$

关于函数  $\varphi(x)$  和  $F(x)$  的可积性, 可由定理 19.1 与定理 19.2 推得.

定理 19.5(可积性) 若  $f(x,y)$  在矩形区域  $R=[a,b]\times[c,d]$  上连续，则  $\varphi(x)$  和  $\psi(y)$  分别在  $[a,b]$  和  $[c,d]$  上可积.

这就是说:在 $f(x,y)$ 连续性假设下,同时存在两个求积顺序不同的积分:

$$
\int_ {a} ^ {b} \Big [ \int_ {c} ^ {d} f (  x  , y  )   \mathrm{d} y   \Big ]   \mathrm{d} x \quad \text {与} \quad \int_ {c} ^ {d} \Big [ \int_ {a} ^ {b} f (  x  , y  )   \mathrm{d} x   \Big ]   \mathrm{d} y.
$$

为书写简便起见,今后将上述两个积分写作

$$
\int_ {a} ^ {b} \mathrm{d} x \int_ {c} ^ {d} f (  x  , y  )   \mathrm{d} y \quad \text {与} \quad \int_ {c} ^ {d} \mathrm{d} y \int_ {a} ^ {b} f (  x  , y  )   \mathrm{d} x,
$$

前者表示 $f(x,y)$ 先对 $y$ 求积然后对 $x$ 求积, 后者则求积顺序相反. 它们统称为累次积分, 或更确切地称为二次积分.

下面的定理指出,在 $f(x,y)$ 连续性假设下,累次积分与求积顺序无关.

定理 19.6 若  $f(x,y)$  在矩形区域  $R=[a,b]\times[c,d]$  上连续，则

$$
\int_ {a} ^ {b} \mathrm{d} x \int_ {c} ^ {d} f (x, y) \mathrm{d} y = \int_ {c} ^ {d} \mathrm{d} y \int_ {a} ^ {b} f (x, y) \mathrm{d} x. \tag {8}
$$

证记

$$
\begin{array}{l} \varphi_ {1} (u) = \int_ {a} ^ {u} \mathrm{d} x \int_ {c} ^ {d} f (x, y) \mathrm{d} y, \\ \varphi_ {2} (u) = \int_ {c} ^ {d} \mathrm{d} y \int_ {a} ^ {u} f (x, y) \mathrm{d} x, \\ \end{array}
$$

其中 $u \in [a, b]$, 现在分别求 $\varphi_1(u)$ 与 $\varphi_2(u)$ 的导数.

$$
\varphi_ {1} ^ {\prime} (u) = \frac {\mathrm{d}}{\mathrm{d} u} \int_ {a} ^ {u} \varphi (x) \mathrm{d} x = \varphi (u).
$$

对于 $\varphi_{2}(u)$ ，令 $H(u,y) = \int_{a}^{u}f(x,y)\mathrm{d}x$ ，则有

$$
\varphi_ {2} (u) = \int_ {c} ^ {d} H (u, y) \mathrm{d} y.
$$

因为  $H(u,y)$  与  $H_{u}(u,y)=f(u,y)$  都在 R 上连续，由定理 19.3，

$$
\begin{array}{l} \varphi_ {2} ^ {\prime} (u) = \frac {\mathrm{d}}{\mathrm{d} u} \int_ {c} ^ {d} H (u, y) \mathrm{d} y = \int_ {c} ^ {d} H _ {u} (u, y) \mathrm{d} y \\ = \int_ {c} ^ {d} f (u, y) \mathrm{d} y = \varphi (u). \\ \end{array}
$$

故得 $\varphi_1'(u) = \varphi_2'(u)$，因此对一切 $u \in [a, b]$，有

$$
\varphi_ {1} (  u  ) = \varphi_ {2} (  u  )   +   k \quad (  k   \text {为常数})  .
$$

当 u=a 时， $\varphi_{1}(a)=\varphi_{2}(a)=0$ ，于是 k=0，即得

$$
\varphi_ {1} (u) = \varphi_ {2} (u), u \in [ a, b ].
$$

取 u=b，就得到所要证明的(8)式.

□

166

---

§ 1 含参量正常积分

例1 求 $\lim_{\alpha \to 0}\int_{\alpha}^{1 + \alpha}\frac{\mathrm{d}x}{1 + x^2 + \alpha^2}.$

解 记 $I(\alpha) = \int_{\alpha}^{1 + \alpha}\frac{\mathrm{d}x}{1 + x^2 + \alpha^2}$. 由于 $\alpha, 1 + \alpha, \frac{1}{1 + x^2 + \alpha^2}$ 都是 $\alpha$ 和 $x$ 的连续函数，由定理19.2知 $I(\alpha)$ 在 $\alpha = 0$ 处连续，所以

$$
\lim _ {\alpha \to 0} I (\alpha) = I (0) = \int_ {0} ^ {1} \frac {\mathrm{d} x}{1 + x ^ {2}} = \frac {\pi}{4}.
$$

例 2 设  $f(x)$  在 x=0 的某个邻域 U 上连续, 验证当  $x \in U$  时, 函数

$$
\varphi (x) = \frac {1}{(n - 1) !} \int_ {0} ^ {x} (x - t) ^ {n - 1} f (t) \mathrm{d} t \tag {9}
$$

的 n 阶导数存在, 且  $\varphi^{(n)}(x)=f(x)$ .

解 由于(9)中被积函数 $F(x,t) = (x - t)^{n - 1}f(t)$ 及其偏导数 $F_{x}(x,t)$ 在 $U\times U$ 上连续,于是由定理19.4可得

$$
\begin{array}{l} \varphi^ {\prime} (x) = \frac {1}{(n - 1) !} \int_ {0} ^ {x} (n - 1) (x - t) ^ {n - 2} f (t) \mathrm{d} t + \frac {1}{(n - 1) !} (x - x) ^ {n - 1} f (x) \\ = \frac {1}{(n - 2) !} \int_ {0} ^ {x} (x - t) ^ {n - 2} f (t) \mathrm{d} t. \\ \end{array}
$$

同理

$$
\varphi^ {\prime \prime} (x) = \frac {1}{(n - 3) !} \int_ {0} ^ {x} (x - t) ^ {n - 3} f (t) \mathrm{d} t.
$$

如此继续下去,求得 k 阶导数为

$$
\varphi^ {(k)} (x) = \frac {1}{(n - k - 1) !} \int_ {0} ^ {x} (x - t) ^ {n - k - 1} f (t) \mathrm{d} t, \quad k = 1, 2, \dots , n - 1.
$$

特别当 $k = n - 1$ 时有

$$
\varphi^ {(n - 1)} (x) = \int_ {0} ^ {x} f (t) \mathrm{d} t,
$$

于是 $\varphi^{(n)}(x) = f(x)$. 附带说明, 当 $x = 0$ 时, $\varphi(x)$ 及其各阶导数为

$$
\varphi (0) = \varphi^ {\prime} (0) = \dots = \varphi^ {(n - 1)} (0) = 0.
$$

例3 求 $I = \int_{0}^{1}\frac{x^{b} - x^{a}}{\ln x}\mathrm{d}x\quad (b > a > 0)$

解 因为  $\int_{a}^{b}x^{y}dy=\frac{x^{b}-x^{a}}{\ln x}$ ，所以

$$
I = \int_ {0} ^ {1} \mathrm{d} x \int_ {a} ^ {b} x ^ {y} \mathrm{d} y.
$$

由于函数 $x^{y}$ 在 $R = [0,1]\times [a,b]$ 上满足定理19.6的条件，所以交换积分顺序得到

$$
I = \int_ {a} ^ {b} \mathrm{d} y \int_ {0} ^ {1} x ^ {y} \mathrm{d} x = \int_ {a} ^ {b} \frac {1}{1 + y} \mathrm{d} y = \ln \frac {1 + b}{1 + a}.
$$

例4 计算积分

$$
I = \int_ {0} ^ {1} \frac {\ln (1 + x)}{1 + x ^ {2}} \mathrm{d} x.
$$

解 考虑含参量积分

167

---

第十九章 含参量积分

$$
\varphi (\alpha) = \int_ {0} ^ {1} \frac {\ln (1 + \alpha x)}{1 + x ^ {2}} \mathrm{d} x, \quad \alpha \in [ 0, 1 ].
$$

显然 $\varphi(0) = 0, \varphi(1) = I$，且函数 $\frac{\ln(1 + \alpha x)}{1 + x^2}$ 在 $R = [0,1] \times [0,1]$ 上满足定理19.3的条件，于是

$$
\varphi^ {\prime} (\alpha) = \int_ {0} ^ {1} \frac {x}{(1 + x ^ {2}) (1 + \alpha x)} \mathrm{d} x.
$$

因为

$$
\frac {x}{(1 + x ^ {2}) (1 + \alpha x)} = \frac {1}{1 + \alpha^ {2}} \left(\frac {\alpha + x}{1 + x ^ {2}} - \frac {\alpha}{1 + \alpha x}\right),
$$

所以

$$
\begin{array}{l} \varphi^ {\prime} (\alpha) = \frac {1}{1 + \alpha^ {2}} \left(\int_ {0} ^ {1} \frac {\alpha}{1 + x ^ {2}} \mathrm{d} x + \int_ {0} ^ {1} \frac {x}{1 + x ^ {2}} \mathrm{d} x - \int_ {0} ^ {1} \frac {\alpha}{1 + \alpha x} \mathrm{d} x\right) \\ = \frac {1}{1 + \alpha^ {2}} \left[ \alpha \arctan x \left| _ {0} ^ {1} + \frac {1}{2} \ln (1 + x ^ {2}) \right| _ {0} ^ {1} - \ln (1 + \alpha x) \right| _ {0} ^ {1} \\ = \frac {1}{1 + \alpha^ {2}} \left[ \alpha \cdot \frac {\pi}{4} + \frac {1}{2} \ln 2 - \ln (1 + \alpha) \right]. \\ \end{array}
$$

因此

$$
\begin{array}{l} \int_ {0} ^ {1} \varphi^ {\prime} (\alpha) \mathrm{d} \alpha = \int_ {0} ^ {1} \frac {1}{1 + \alpha^ {2}} \left[ \frac {\pi}{4} \alpha + \frac {1}{2} \ln 2 - \ln (1 + \alpha) \right] \mathrm{d} \alpha \\ = \frac {\pi}{8} \ln (1 + \alpha^ {2}) \left| _ {0} ^ {1} + \frac {1}{2} \ln 2 \arctan \alpha \right| _ {0} ^ {1} - \varphi (1) \\ = \frac {\pi}{8} \ln 2 + \frac {\pi}{8} \ln 2 - \varphi (1) \\ = \frac {\pi}{4} \ln 2 - \varphi (1). \\ \end{array}
$$

另一方面，

$$
\int_ {0} ^ {1} \varphi^ {\prime} (\alpha) \mathrm{d} \alpha = \varphi (1) - \varphi (0) = \varphi (1),
$$

所以  $I=\varphi(1)=\frac{\pi}{8}\ln2.$

## 习题 19.1

1. 设 $f(x, y) = \operatorname{sgn}(x - y)$ （这个函数在 $x = y$ 时不连续），试证由含参量积分

$$
F (y) = \int_ {0} ^ {1} f (x, y)   \mathrm{d} x
$$

所确定的函数在 $(-∞,+∞)$ 上连续，并作函数 $F(y)$ 的图像.

2. 求下列极限:

(1) $\lim_{\alpha \to 0}\int_{-1}^{1}\sqrt{x^2 + \alpha^2}\mathrm{d}x;$

(2) $\lim_{\alpha \to 0}\int_{0}^{2}x^2\cos \alpha x\mathrm{d}x.$

168

---

§ 2 含参量反常积分

3. 设 $F(x) = \int_{x}^{x^2}\mathrm{e}^{-xy^2}\mathrm{d}y$ ，求 $F^{\prime}(x)$

4. 应用对参量的微分法, 求下列积分:

(1) $\int_{0}^{\frac{\pi}{2}}\ln (a^{2}\sin^{2}x + b^{2}\cos^{2}x)\mathrm{d}x$ ($a^2 +b^2\neq 0$);
(2) $\int_{0}^{\pi}\ln (1 - 2a\cos x + a^{2})\mathrm{d}x.$

5. 应用积分号下的积分法, 求下列积分:

(1) $\int_{0}^{1}\sin \left(\ln \frac{1}{x}\right)\frac{x^b - x^a}{\ln x}\mathrm{d}x$ （ $b > a > 0$ ）；
(2) $\int_{0}^{1}\cos \left(\ln \frac{1}{x}\right)\frac{x^b - x^a}{\ln x}\mathrm{d}x$ （ $b > a > 0$ ）.

6. 试求累次积分:

$$
\int_ {0} ^ {1} \mathrm{d} x \int_ {0} ^ {1} {\frac {x ^ {2} - y ^ {2}}{(  x ^ {2} + y ^ {2}  ) ^ {2}}} \mathrm{d} y \quad \text {与} \quad \int_ {0} ^ {1} \mathrm{d} y \int_ {0} ^ {1} {\frac {x ^ {2} - y ^ {2}}{(  x ^ {2} + y ^ {2}  ) ^ {2}}} \mathrm{d} x,
$$

并指出它们为什么与定理 19.6 的结果不符.

7. 研究函数 $F(y) = \int_{0}^{1} \frac{yf(x)}{x^2 + y^2} \, \mathrm{d}x$ 的连续性，其中 $f(x)$ 在闭区间 $[0, 1]$ 上是正的连续函数.

8. 设函数 $f(x)$ 在区间 $[a, A)$ 上连续. 证明

$$
\lim _ {h \to 0 ^ {+}} \frac {1}{h} \int_ {a} ^ {x} \left[ f (t + h) - f (t) \right] \mathrm{d} t = f (x) - f (a) \quad (a <   x <   A).
$$

9. 设

$$
F (x, y) = \int_ {\frac {x}{y}} ^ {x y} (x - y z) f (z)   \mathrm{d} z,
$$

其中 $f(z)$ 为可微函数，求 $F_{xy}(x,y)$

10. 设

$$
E (k) = \int_ {0} ^ {\frac {\pi}{2}} \sqrt {1 - k ^ {2} \sin^ {2} \varphi} \mathrm{d} \varphi , F (k) = \int_ {0} ^ {\frac {\pi}{2}} \frac {\mathrm{d} \varphi}{\sqrt {1 - k ^ {2} \sin^ {2} \varphi}},
$$

其中 0<k<1（这两个积分称为完全椭圆积分）.

(1) 试求  $E(k)$  与  $F(k)$  的导数，并以  $E(k)$  与  $F(k)$  来表示它们；
(2) 证明  $E(k)$  满足方程

$$
E ^ {\prime \prime} (k) + \frac {1}{k} E ^ {\prime} (k) + \frac {E (k)}{1 - k ^ {2}} = 0.
$$

## § 2 含参量反常积分

## 一、一致收敛性及其判别法

设函数 $f(x,y)$ 定义在无界区域 $R = \{(x,y) | x \in I, c \leqslant y < +\infty\}$ 上，其中 $I$ 为一区间，若对每一个固定的 $x \in I$ ，反常积分

169

---

第十九章 含参量积分

$$
\int_ {c} ^ {+ \infty} f (x, y) \mathrm{d} y \tag {1}
$$

都收敛,则它的值是 x 在 I 上取值的函数,当记这个函数为  $\Phi(x)$  时,则有

$$
\Phi (x) = \int_ {c} ^ {+ \infty} f (x, y) \mathrm{d} y, x \in I, \tag {2}
$$

称(1)式为定义在 I 上的含参量 x 的无穷限反常积分,或简称含参量反常积分.

如同反常积分与数项级数的关系那样,含参量反常积分与函数项级数在所研究的问题与论证方法上也极为相似.

首先引入含参量反常积分的一致收敛概念及柯西准则.

定义1 若含参量反常积分(1)与函数 $\Phi(x)$ 对任给的正数 $\varepsilon$，总存在某一实数 $N > c$，使得当 $M > N$ 时，对一切 $x \in I$，都有

$$
\left| \int_ {c} ^ {M} f (x, y) \mathrm{d} y - \Phi (x) \right| <   \varepsilon ,
$$

即

$$
\left| \int_ {M} ^ {+ \infty} f (x, y) \mathrm{d} y \right| <   \varepsilon ,
$$

则称含参量反常积分(1)在 I 上一致收敛于  $\Phi(x)$ ，或简单地说含参量反常积分(1)在 I 上一致收敛.

定理 19.7(一致收敛的柯西准则) 含参量反常积分(1)在 I 上一致收敛的充要条件是: 对任给正数  $\varepsilon$ , 总存在某一实数 M > c, 使得当  $A_{1}, A_{2} > M$  时, 对一切  $x \in I$ , 都有

$$
\left| \int_ {A _ {1}} ^ {A _ {2}} f (x, y) \mathrm{d} y \right| <   \varepsilon . \tag {3}
$$

由定义 1, 我们还有以下含参量反常积分一致收敛的判别准则.

定理19.8 含参量反常积分 $\int_{c}^{+\infty}f(x,y)\mathrm{d}y$ 在 $I$ 上一致收敛的充分必要条件是

$$
\lim _ {A \to + \infty} F (A) = 0,
$$

其中 $F(A) = \sup_{x\in I}\left|\int_{A}^{+\infty}f(x,y)\mathrm{d}y\right|.$

例 1 证明含参量反常积分

$$
\int_ {0} ^ {+ \infty} \frac {\sin x y}{y} \mathrm{d} y \tag {4}
$$

在 $\left[\delta,+\infty\right)$ 上一致收敛(其中 $\delta>0$ ),但在 $(0,+\infty)$ 上不一致收敛.

证 先证(4)式在 $[\delta,+\infty)$ 上一致收敛.作变量代换u=xy,得

$$
\int_ {A} ^ {+ \infty} \frac {\sin x y}{y} \mathrm{d} y = \int_ {A x} ^ {+ \infty} \frac {\sin u}{u} \mathrm{d} u, \tag {5}
$$

其中 $A > 0$ .由于 $\int_0^{+\infty}\frac{\sin u}{u}\mathrm{d}u$ 收敛，故对任给正数 $\varepsilon$ ，总存在正数 $M^{\prime}$ ，使当 $A^{\prime} > M^{\prime}$ 时，就有

$$
\left| \int_ {A ^ {\prime}} ^ {+ \infty} \frac {\sin u}{u} \mathrm{d} u \right| <   \varepsilon .
$$

取 $M = \frac{M'}{\delta}$, 则当 $A > M$ 时, 对一切 $x \geqslant \delta > 0$, 有 $Ax > M'$, 由 (5) 式有

170

---

§ 2 含参量反常积分

$$
\left| \int_ {A} ^ {+ \infty} \frac {\sin x y}{y} \mathrm{d} y \right| = \left| \int_ {A x} ^ {+ \infty} \frac {\sin u}{u} \mathrm{d} u \right| <   \varepsilon ,
$$

因此 $\lim_{A\to +\infty}F(A) = 0$ ，从而由定理19.8，(4)式在 $[\delta , + \infty)$ 上一致收敛

下证(4)式在 $(0,+\infty)$ 上不一致收敛.

由柯西准则, 含参量反常积分(1)不一致收敛的充要条件应为: 存在  $\varepsilon_{0}>0$ , 对任意实数  $M(M>c)$ , 总能找到  $A_{1}, A_{2}>M$  和某个  $\bar{x}\in[a,b]$ , 满足

$$
\left| \int_ {A _ {1}} ^ {A _ {2}} f (\bar {x}, y) \mathrm{d} y \right| \geqslant \varepsilon_ {0}.
$$

令 $\varepsilon_0 = \frac{\ln 2}{2}$，对任意 $M > 0$，令 $A_{1} = \frac{\pi}{3} M, A_{2} = 2A_{1}$，$\bar{x} = \frac{1}{M} \in (0, +\infty)$，对 $y \in [A_{1}, A_{2}]$ 此时有 $\bar{x}y \in \left[\frac{\pi}{3}, \frac{2\pi}{3}\right]$. 因此

$$
\left| \int_ {A _ {1}} ^ {A _ {2}} \frac {\sin \bar {x} y}{y} \mathrm{d} y \right| \geqslant \frac {1}{2} \int_ {A _ {1}} ^ {A _ {2}} \frac {1}{y} \mathrm{d} y = \frac {\ln 2}{2} = \varepsilon_ {0},
$$

所以(4)式在 $(0,+\infty)$ 上不一致收敛.

若对任意 $[a, b] \subset I$，含参量反常积分(1)在 $[a, b]$ 上一致收敛，则称(1)在 $I$ 上内闭一致收敛（若 $I = [a, b]$，则内闭一致收敛即一致收敛），以上论述证明了含参量反常积分(4)在 $(0, +\infty)$ 上内闭一致收敛.

关于含参量反常积分一致收敛性与函数项级数一致收敛性之间的联系有下述定理.

定理19.9 含参量反常积分(1)在 $I$ 上一致收敛的充要条件是: 对任一趋于 $+\infty$ 的递增数列 $\{A_{n}\}$ (其中 $A_{1} = c$), 函数项级数

$$
\sum_ {n = 1} ^ {\infty} \int_ {A _ {n}} ^ {A _ {n + 1}} f (x, y) \mathrm{d} y = \sum_ {n = 1} ^ {\infty} u _ {n} (x) \tag {6}
$$

在 I 上一致收敛.

证 [必要性] 由(1)在 I 上一致收敛, 故对任给  $\varepsilon > 0$ , 必存在 M > c, 使当  $A'' > A' > M$  时, 对一切  $x \in I$ , 总有

$$
\left| \int_ {A ^ {\prime}} ^ {A ^ {\prime \prime}} f (x, y) \mathrm{d} y \right| <   \varepsilon . \tag {7}
$$

又由 $A_{n}\rightarrow +\infty (n\to \infty)$ ，所以对正数 $M$ ，存在正整数 $N$ ，只要当 $m > n > N$ 时，就有 $A_{m}\geqslant A_{n}>$ $M.$ 由(7)对一切 $x\in I$ ，就有

$$
\begin{array}{l} \mid u _ {n} (x) + \dots + u _ {m} (x) \mid = \left| \int_ {A _ {m}} ^ {A _ {m + 1}} f (x, y) \mathrm{d} y + \dots + \int_ {A _ {n}} ^ {A _ {n + 1}} f (x, y) \mathrm{d} y \right| \\ = \left| \int_ {A _ {n}} ^ {A _ {m + 1}} f (x, y)   \mathrm{d} y \right| <   \varepsilon . \\ \end{array}
$$

这就证明了级数(6)在 I 上一致收敛.

[充分性] 用反证法. 假若(1)在 I 上不一致收敛, 则存在某个正数  $\varepsilon_{0}$ , 使得对于任何实数 M > c, 存在相应的  $A'' > A' > M$  和  $x' \in I$ , 使得

$$
\left| \int_ {A ^ {\prime}} ^ {A ^ {\prime \prime}} f (x ^ {\prime}, y) \mathrm{d} y \right| \geqslant \varepsilon_ {0}.
$$

现取 $M_{1} = \max \{1, c\}$，则存在 $A_{2} > A_{1} > M_{1}$ 及 $x_{1} \in I$，使得

171

---

第十九章 含参量积分

$$
\left| \int_ {A _ {1}} ^ {A _ {2}} f (x _ {1}, y) \mathrm{d} y \right| \geqslant \varepsilon_ {0}.
$$

一般地，取 $M_{n} = \max \{n,A_{2(n - 1)}\}$ （$n\geqslant 2$），则有 $A_{2n} > A_{2n - 1} > M_n$ 及 $x_{n}\in I$ ，使得

$$
\left| \int_ {A _ {2 n - 1}} ^ {A _ {2 n}} f (x _ {n}, y) \mathrm{d} y \right| \geqslant \varepsilon_ {0}. \tag {8}
$$

由上述所得到的数列 $\{A_{n}\}$ 是递增数列，且 $\lim_{n\to \infty}A_n = +\infty$ .现在考察级数

$$
\sum_ {n = 1} ^ {\infty} u _ {n} (x) = \sum_ {n = 1} ^ {\infty} \int_ {A _ {n}} ^ {A _ {n + 1}} f (x, y) \mathrm{d} y.
$$

由(8)式知存在正数 $\varepsilon_0$ ，对任何正整数 $N$ ，只要 $n > N$ ，就有某个 $x_{n}\in I$ ，使得

$$
\left| u _ {2 n - 1} (x _ {n}) \right| = \left| \int_ {A _ {2 n - 1}} ^ {A _ {2 n}} f (x _ {n}, y) \mathrm{d} y \right| \geqslant \varepsilon_ {0}.
$$

这与级数(6)在 $I$ 上一致收敛的假设矛盾. 故含参量反常积分(1)在 $I$ 上一致收敛.

下面列出含参量反常积分的一致收敛性判别法. 由于它们的证明与函数项级数相应的判别法相仿, 故从略.

魏尔斯特拉斯 $M$ 判别法 设有函数 $g(y)$, 使得

$$
\mid f (x, y) \mid \leqslant g (y), (x, y) \in I \times [ c, + \infty).
$$

若 $\int_{c}^{+\infty}g(y)\mathrm{d}y$ 收敛，则 $\int_{c}^{+\infty}f(x,y)\mathrm{d}y$ 在 $I$ 上一致收敛.

狄利克雷判别法 设

(i) 对一切实数 $N > c$，含参量正常积分

$$
\int_ {c} ^ {N} f (x, y) \mathrm{d} y
$$

对参量 $x$ 在 $I$ 上一致有界，即存在正数 $M$ ，对一切 $N > c$ 及一切 $x\in I$ ，都有

$$
\left| \int_ {c} ^ {N} f (x, y) \mathrm{d} y \right| \leqslant M.
$$

（ii）对每一个 $x \in I$，函数 $g(x, y)$ 为 $y$ 的单调函数，且当 $y \to +\infty$ 时，对参量 $x, g(x, y)$ 一致地收敛于0.

则含参量反常积分

$$
\int_ {c} ^ {+ \infty} f (x, y) g (x, y) \mathrm{d} y
$$

在 I 上一致收敛.

阿贝尔判别法 设

(i) $\int_{c}^{+\infty}f(x,y)\mathrm{d}y$ 在 $I$ 上一致收敛.

(ii) 对每一个 $x \in I$, 函数 $g(x, y)$ 为 $y$ 的单调函数, 且对参量 $x, g(x, y)$ 在 $I$ 上一致有界.

则含参量反常积分

$$
\int_ {c} ^ {+ \infty} f (x, y) g (x, y) \mathrm{d} y
$$

在 I 上一致收敛.

例 2 证明含参量反常积分

$$
\int_ {0} ^ {+ \infty} \frac {\cos x y}{1 + x ^ {2}} \mathrm{d} x \tag {9}
$$

172

---

§ 2 含参量反常积分

在 $(-∞,+∞)$ 上一致收敛.

证 由于对任何实数 $y$ ，有

$$
\left| \frac {\cos x y}{1 + x ^ {2}} \right| \leqslant \frac {1}{1 + x ^ {2}}
$$

及反常积分

$$
\int_ {0} ^ {+ \infty} \frac {\mathrm{d} x}{1 + x ^ {2}}
$$

收敛,故由魏尔斯特拉斯 M 判别法,含参量反常积分(9)在 $(-∞,+∞)$ 上一致收敛. □

例 3 证明含参量反常积分

$$
\int_ {0} ^ {+ \infty} \mathrm{e} ^ {- x y} \frac {\sin x}{x} \mathrm{d} x \tag {10}
$$

在 $[0,+\infty)$ 上一致收敛.

证 由于反常积分 $\int_{0}^{+\infty}\frac{\sin x}{x}\mathrm{d}x$ 收敛（当然，对于参量 $y$ ，它在 $[0, + \infty)$ 上一致收敛），函数 $g(x,y) = \mathrm{e}^{-xy}$ 对每个 $y\in [0, + \infty)$ 单调，且对任何 $0\leqslant y <   + \infty ,x\geqslant 0$ ，都有

$$
\mid g (x, y) \mid = \mid \mathrm{e} ^ {- x y} \mid \leqslant 1.
$$

故由阿贝尔判别法即得含参量反常积分(10)在 $[0,+\infty)$ 上一致收敛.

例 4 证明含参量反常积分

$$
\int_ {1} ^ {+ \infty} \frac {y \sin x y}{1 + y ^ {2}} \mathrm{d} y \tag {11}
$$

在 $(0,+\infty)$ 上内闭一致收敛.

证 若 $[a, b] \subset (0, +\infty)$，则对任意 $x \in [a, b]$，

$$
\left| \int_ {a} ^ {N} \sin x y \mathrm{d} y \right| = \left| - \frac {\cos x y}{x} \right| _ {a} ^ {N} \Big | \leqslant \frac {2}{a},
$$

因此一致有界. 又

$$
\left(\frac {y}{1 + y ^ {2}}\right) ^ {\prime} = \frac {1 - y ^ {2}}{\left(1 + y ^ {2}\right) ^ {2}} \leqslant 0,
$$

因此 $\frac{y}{1+y^{2}}$ 关于y单调递减，且当 $y\to+\infty$ 时， $\frac{y}{1+y^{2}}\to0$ （对x一致），故由狄利克雷判别法，含参量反常积分(11)在 $[a,b]$ 上一致收敛。又由 $[a,b]$ 的任意性，含参量反常积分(11)在 $(0,+\infty)$ 上内闭一致收敛。

## 二、含参量反常积分的性质

定理 19.10(连续性) 设  $f(x,y)$  在  $I \times [c, +\infty)$  上连续, 若含参量反常积分

$$
\Phi (x) = \int_ {c} ^ {+ \infty} f (x, y) \mathrm{d} y \tag {12}
$$

在 I 上一致收敛, 则  $\Phi(x)$  在 I 上连续.

证 由定理19.9,对任一递增且趋于 $+\infty$ 的数列 $\{A_{n}\} (A_{1} = c)$,函数项级数

$$
\varPhi (x) = \sum_ {n = 1} ^ {\infty} \int_ {A _ {n}} ^ {A _ {n + 1}} f (x, y) \mathrm{d} y = \sum_ {n = 1} ^ {\infty} u _ {n} (x) \tag {13}
$$

在 I 上一致收敛. 又由于  $f(x,y)$  在  $I \times [c, +\infty)$  上连续, 故每个  $u_{n}(x)$  都在 I 上连续. 根据

173

---

第十九章 含参量积分

函数项级数的连续性定理, 函数  $\Phi(x)$  在 I 上连续.

推论 设 $f(x, y)$ 在 $I \times [c, +\infty)$ 上连续，若 $\Phi(x) = \int_{c}^{+\infty} f(x, y) \mathrm{d}y$ 在 $I$ 上内闭一致收敛，则 $\Phi(x)$ 在 $I$ 上连续.

这个定理也表明,在一致收敛的条件下,极限运算与无穷积分运算可以交换:

$$
\lim _ {x \to x _ {0}} \int_ {c} ^ {+ \infty} f (x, y) \mathrm{d} y = \int_ {c} ^ {+ \infty} f (x _ {0}, y) \mathrm{d} y = \int_ {c} ^ {+ \infty} \lim _ {x \to x _ {0}} f (x, y) \mathrm{d} y. \tag {14}
$$

定理 19.11（可微性）设  $f(x,y)$  与  $f_{x}(x,y)$  在区域  $I \times [c, +\infty)$  上连续。若  $\Phi(x)=\int_{c}^{+\infty}f(x,y)\mathrm{d}y$  在 I 上收敛， $\int_{c}^{+\infty}f_{x}(x,y)\mathrm{d}y$  在 I 上一致收敛，则  $\Phi(x)$  在 I 上可微，且

$$
\Phi^ {\prime} (x) = \int_ {c} ^ {+ \infty} f _ {x} (x, y) \mathrm{d} y. \tag {15}
$$

证 对任一递增且趋于 $+\infty$ 的数列 $\{A_{n}\} (A_{1} = c)$，令

$$
u _ {n} (x) = \int_ {A _ {n}} ^ {A _ {n + 1}} f (x, y) \mathrm{d} y.
$$

由定理19.3推得

$$
u _ {n} ^ {\prime} (x) = \int_ {A _ {n}} ^ {A _ {n + 1}} f _ {x} (x, y) \mathrm{d} y.
$$

由 $\int_{c}^{+\infty}f_{x}(x,y)\mathrm{d}y$ 在 $I$ 上一致收敛及定理19.9，可得函数项级数

$$
\sum_ {n = 1} ^ {\infty} u _ {n} ^ {\prime} (x) = \sum_ {n = 1} ^ {\infty} \int_ {A _ {n}} ^ {A _ {n + 1}} f _ {x} (x, y) \mathrm{d} y
$$

在 I 上一致收敛,因此根据函数项级数的逐项求导定理,即得

$$
\Phi^ {\prime} (x) = \sum_ {n = 1} ^ {\infty} u _ {n} ^ {\prime} (x) = \sum_ {n = 1} ^ {\infty} \int_ {A _ {n}} ^ {A _ {n + 1}} f _ {x} (x, y) \mathrm{d} y = \int_ {c} ^ {+ \infty} f _ {x} (x, y) \mathrm{d} y,
$$

或写作

$$
\frac {\mathrm{d}}{\mathrm{d} x} \int_ {c} ^ {+ \infty} f (x, y) \mathrm{d} y = \int_ {c} ^ {+ \infty} \frac {\partial}{\partial x} f (x, y) \mathrm{d} y.
$$

推论 设 $f(x, y)$ 和 $f_{x}(x, y)$ 在 $I \times [c, +\infty)$ 上连续，若 $\Phi(x) = \int_{c}^{+\infty} f(x, y) \mathrm{d}y$ 在 $I$ 上收敛，而 $\int_{c}^{+\infty} f_{x}(x, y) \mathrm{d}y$ 在 $I$ 上内闭一致收敛，则 $\Phi(x)$ 在 $I$ 上可微，且 $\Phi'(x) = \int_{c}^{+\infty} f_{x}(x, y) \mathrm{d}y$.

最后结果表明在定理条件下,求导运算和无穷积分运算可以交换.

定理 19.12(可积性) 设  $f(x,y)$  在  $[a,b]\times[c,+\infty)$  上连续, 若  $\Phi(x)=\int_{c}^{+\infty}f(x,y)\mathrm{d}y$  在  $[a,b]$  上一致收敛, 则  $\Phi(x)$  在  $[a,b]$  上可积, 且

$$
\int_ {a} ^ {b} \mathrm{d} x \int_ {c} ^ {+ \infty} f (x, y) \mathrm{d} y = \int_ {c} ^ {+ \infty} \mathrm{d} y \int_ {a} ^ {b} f (x, y) \mathrm{d} x. \tag {16}
$$

证 由定理 19.10 知道  $\Phi(x)$  在  $[a,b]$  上连续, 从而  $\Phi(x)$  在  $[a,b]$  上可积.

又由定理19.10的证明中可以看到，函数项级数(13)在 $[a,b]$ 上一致收敛，且各项$u_{n}(x)$ 在 $[a,b]$ 上连续，因此根据函数项级数逐项求积定理，有

174

---

§ 2 含参量反常积分

$$
\begin{array}{l} \int_ {a} ^ {b} \Phi (x) \mathrm{d} x = \sum_ {n = 1} ^ {\infty} \int_ {a} ^ {b} u _ {n} (x) \mathrm{d} x = \sum_ {n = 1} ^ {\infty} \int_ {a} ^ {b} \mathrm{d} x \int_ {A _ {n}} ^ {A _ {n + 1}} f (x, y) \mathrm{d} y \\ = \sum_ {n = 1} ^ {\infty} \int_ {A _ {n}} ^ {A _ {n + 1}} \mathrm{d} y \int_ {a} ^ {b} f (x, y) \mathrm{d} x, \tag {17} \\ \end{array}
$$

这里最后一步是根据定理19.6关于积分顺序的可交换性.(17)式又可写作

$$
\int_ {a} ^ {b} \Phi (x) \mathrm{d} x = \int_ {c} ^ {+ \infty} \mathrm{d} y \int_ {a} ^ {b} f (x, y) \mathrm{d} x.
$$

这就是(16)式.

![](../../raw/pages_0161-0192/images/page_182_image_5.jpg)

当定理 19.12 中 x 的取值范围为无限区间  $[a, +\infty)$  时，则有如下的定理.

定理19.13 设 $f(x,y)$ 在 $[a, +\infty)\times [c, +\infty)$ 上连续.若

(i) $\int_{a}^{+\infty} f(x, y) \mathrm{d}x$ 关于 $y$ 在 $[c, +\infty)$ 上内闭一致收敛，$\int_{c}^{+\infty} f(x, y) \mathrm{d}y$ 关于 $x$ 在 $[a, +\infty)$ 上内闭一致收敛.

(ii) 积分

$$
\int_ {a} ^ {+ \infty} \mathrm{d} x \int_ {c} ^ {+ \infty} | f (x, y) | \mathrm{d} y \text {与} \int_ {c} ^ {+ \infty} \mathrm{d} y \int_ {a} ^ {+ \infty} | f (x, y) | \mathrm{d} x \tag {18}
$$

中有一个收敛.

则

$$
\int_ {a} ^ {+ \infty} \mathrm{d} x \int_ {c} ^ {+ \infty} f (x, y) \mathrm{d} y = \int_ {c} ^ {+ \infty} \mathrm{d} y \int_ {a} ^ {+ \infty} f (x, y) \mathrm{d} x. \tag {19}
$$

证 不妨设(18)式中第一个积分收敛,由此推得

$$
\int_ {a} ^ {+ \infty} \mathrm{d} x \int_ {c} ^ {+ \infty} f (x, y) \mathrm{d} y
$$

也收敛. 当 d > c 时,

$$
\begin{array}{l} J _ {d} = \left| \int_ {c} ^ {d} \mathrm{d} y \int_ {a} ^ {+ \infty} f (x, y) \mathrm{d} x - \int_ {a} ^ {+ \infty} \mathrm{d} x \int_ {c} ^ {+ \infty} f (x, y) \mathrm{d} y \right| \\ = \left| \int_ {c} ^ {d} \mathrm{d} y \int_ {a} ^ {+ \infty} f (x, y) \mathrm{d} x - \int_ {a} ^ {+ \infty} \mathrm{d} x \int_ {c} ^ {d} f (x, y) \mathrm{d} y - \int_ {a} ^ {+ \infty} \mathrm{d} x \int_ {d} ^ {+ \infty} f (x, y) \mathrm{d} y \right|. \\ \end{array}
$$

根据条件(i)及定理19.12,可推得

$$
\begin{array}{l} J _ {d} = \left| \int_ {a} ^ {+ \infty} \mathrm{d} x \int_ {d} ^ {+ \infty} f (x, y) \mathrm{d} y \right| \\ \leqslant \left| \int_ {a} ^ {A} \mathrm{d} x \int_ {d} ^ {+ \infty} f (x, y) \mathrm{d} y \right| + \int_ {A} ^ {+ \infty} \mathrm{d} x \int_ {d} ^ {+ \infty} | f (x, y) | \mathrm{d} y. \tag {20} \\ \end{array}
$$

由条件(ii)，对于任给的 $\varepsilon > 0$ ，有 $G > a$ ，使当 $A > G$ 时，有

$$
\int_ {A} ^ {+ \infty} \mathrm{d} x \int_ {d} ^ {+ \infty} \mid f (x, y) \mid \mathrm{d} y <   \frac {\varepsilon}{2}.
$$

选定 A 后，由  $\int_{c}^{+\infty} f(x, y) \, dy$  的内闭一致收敛性，存在 M > c，使得当 d > M 时有

$$
\left| \int_ {d} ^ {+ \infty} f (x, y) \mathrm{d} y \right| <   \frac {\varepsilon}{2 (A - a)}, \quad \forall x \in [ a, A ].
$$

把这两个结果应用到(20)式,得到

$$
J _ {d} <   \frac {\varepsilon}{2} + \frac {\varepsilon}{2} = \varepsilon ,
$$

175

---

第十九章 含参量积分

即  $\lim_{d\to+\infty}J_{d}=0$  , 这就证明了(19)式.

例5 计算

$$
J = \int_ {0} ^ {+ \infty} \mathrm{e} ^ {- p x} \frac {\sin b x - \sin a x}{x} \mathrm{d} x \quad (p > 0, b > a).
$$

解 因为  $\frac{\sin bx - \sin ax}{x} = \int_{a}^{b} \cos xy dy$ ，所以

$$
\begin{array}{l} J = \int_ {0} ^ {+ \infty} \mathrm{e} ^ {- p x} \frac {\sin b x - \sin a x}{x} \mathrm{d} x \\ = \int_ {0} ^ {+ \infty} \mathrm{e} ^ {- p x} \left(\int_ {a} ^ {b} \cos x y \mathrm{d} y\right) \mathrm{d} x \\ = \int_ {0} ^ {+ \infty} \mathrm{d} x \int_ {a} ^ {b} \mathrm{e} ^ {- p x} \cos x y \mathrm{d} y. \tag {21} \\ \end{array}
$$

由于 $|\mathrm{e}^{-px}\cos xy| \leqslant \mathrm{e}^{-px}$ 及反常积分 $\int_0^{+\infty}\mathrm{e}^{-px}\mathrm{d}x$ 收敛，根据魏尔斯特拉斯 $M$ 判别法，含参量反常积分

$$
\int_ {0} ^ {+ \infty} \mathrm{e} ^ {- p x} \cos x y \mathrm{d} x
$$

在 $[a, b]$ 上一致收敛. 由于 $\mathrm{e}^{-px} \cos xy$ 在 $[0, +\infty) \times [a, b]$ 上连续, 根据定理19.12交换积分(21)的顺序, 积分 $J$ 的值不变. 于是

$$
\begin{array}{l} J = \int_ {a} ^ {b} \mathrm{d} y \int_ {0} ^ {+ \infty} \mathrm{e} ^ {- p x} \cos x y \mathrm{d} x = \int_ {a} ^ {b} \frac {p}{p ^ {2} + y ^ {2}} \mathrm{d} y \\ = \arctan \frac {b}{p} - \arctan \frac {a}{p}. \\ \end{array}
$$

例6 计算 $\int_0^{+\infty}\frac{\sin ax}{x}\mathrm{d}x.$

解 在上例中, 令 b=0, 则有

$$
F (p) = \int_ {0} ^ {+ \infty} \mathrm{e} ^ {- p x} \frac {\sin a x}{x} \mathrm{d} x = \arctan \frac {a}{p} \quad (p > 0). \tag {22}
$$

由阿贝尔判别法可得上述含参量反常积分在 $p \geqslant 0$ 上一致收敛. 于是由定理19.10, $F(p)$ 在 $p \geqslant 0$ 上连续, 且

$$
F (0) = \int_ {0} ^ {+ \infty} \frac {\sin a x}{x} \mathrm{d} x.
$$

又由(22)式

$$
F (0) = \lim _ {p \to 0 ^ {+}} F (p) = \lim _ {p \to 0 ^ {+}} \arctan \frac {a}{p} = \frac {\pi}{2} \mathrm{sgn} a.
$$

例7 计算

$$
\varphi (r) = \int_ {0} ^ {+ \infty} \mathrm{e} ^ {- x ^ {2}} \cos r x \mathrm{d} x. \tag {23}
$$

解 由于 $|\mathrm{e}^{-x^2}\cos rx| \leqslant \mathrm{e}^{-x^2}$ 对任一实数 $r$ 成立及反常积分 $\int_0^{+\infty}\mathrm{e}^{-x^2}\mathrm{d}x$ 收敛，所以积分(23)在 $r\in (-\infty , + \infty)$ 上收敛.

176

---

§ 2 含参量反常积分

考察含参量反常积分

$$
\int_ {0} ^ {+ \infty} \frac {\partial}{\partial r} (\mathrm{e} ^ {- x ^ {2}} \cos r x) \mathrm{d} x = \int_ {0} ^ {+ \infty} - x \mathrm{e} ^ {- x ^ {2}} \sin r x \mathrm{d} x. \tag {24}
$$

由于 $\left| -x\mathrm{e}^{-x^2}\sin rx \right| \leqslant x\mathrm{e}^{-x^2}$ 对一切 $x \geqslant 0, -\infty < r < +\infty$ 成立及反常积分 $\int_{0}^{+\infty} x\mathrm{e}^{-x^2}\mathrm{d}x$ 收敛，根据魏尔斯特拉斯 $M$ 判别法，含参量反常积分(24)在 $(-∞,+∞)$ 上一致收敛.

综合上述结果由定理19.11即得

$$
\begin{array}{l} \varphi^ {\prime} (r) = \int_ {0} ^ {+ \infty} - x \mathrm{e} ^ {- x ^ {2}} \sin r x \mathrm{d} x = \lim _ {A \rightarrow + \infty} \int_ {0} ^ {A} - x \mathrm{e} ^ {- x ^ {2}} \sin r x \mathrm{d} x \\ = \lim _ {A \to + \infty} \left(\frac {1}{2} \mathrm{e} ^ {- x ^ {2}} \sin r x \bigg | _ {0} ^ {A} - \frac {1}{2} \int_ {0} ^ {A} r \mathrm{e} ^ {- x ^ {2}} \cos r x \mathrm{d} x\right) \\ = - \frac {r}{2} \int_ {0} ^ {+ \infty} \mathrm{e} ^ {- x ^ {2}} \cos r x \mathrm{d} x = - \frac {r}{2} \varphi (r). \\ \end{array}
$$

于是有

$$
\ln \varphi (r) = - \frac {r ^ {2}}{4} + \ln c,
$$

$$
\varphi (r) = c \mathrm{e} ^ {- \frac {r ^ {2}}{4}}.
$$

从而 $\varphi(0) = c$，又由(23)式，$\varphi(0) = \int_{0}^{+\infty} \mathrm{e}^{-x^2} \, \mathrm{d}x = \frac{\sqrt{\pi}}{2}$①，所以 $c = \frac{\sqrt{\pi}}{2}$，因此得到

$$
\varphi (r) = \frac {\sqrt {\pi}}{2} \mathrm{e} ^ {- \frac {r ^ {2}}{4}}.
$$

最后简略地提一下关于含参量无界函数非正常积分. 设 $f(x, y)$ 在区域 $R = [a, b] \times [c, d)$ 上有定义. 若对 $x$ 的某些值, $y = d$ 为函数 $f(x, y)$ 的瑕点, 则称

$$
\int_ {c} ^ {d} f (x, y) \mathrm{d} y \tag {25}
$$

为含参量 $x$ 的无界函数反常积分, 或简称为含参量反常积分. 若对每一个 $x \in [a, b]$, 积分 (25) 都收敛, 则其积分值是 $x$ 在 $[a, b]$ 上取值的函数. 含参量反常积分 (25) 在 $[a, b]$ 上一致收敛的定义如下.

定义 2 对任给正数  $\varepsilon$ ，总存在某正数  $\delta < d - c$ ，使得当  $0 < \eta < \delta$  时，对一切  $x \in [a, b]$ ，都有

$$
\left| \int_ {d - \eta} ^ {d} f (x, y) \mathrm{d} y \right| <   \varepsilon ,
$$

则称含参量反常积分(25)在 $[a,b]$ 上一致收敛.

读者可参照含参量无穷限反常积分的办法建立相应的含参量无界函数反常积分的一致收敛性判别法,并讨论它们的性质,这里不再赘述了.

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 关于反常积分 $\int_{0}^{+\infty}\mathrm{e}^{-x^2}\mathrm{d}x$ 的值等于 $\frac{\sqrt{\pi}}{2}$ 的证明将在第二十一章“反常二重积分”一节中给出.</span></small>

177

---

第十九章 含参量积分

## 习题 19.2

1. 证明下列各题:

(1) $\int_{1}^{+\infty}\frac{y^2 - x^2}{(x^2 + y^2)^2}\mathrm{d}x$ 在 $(-\infty , + \infty)$ 上一致收敛；
(2) $\int_{0}^{+\infty}\mathrm{e}^{-x^2 y}\mathrm{d}y$ 在 $[a,b]$ （ $a > 0$ ）上一致收敛；
(3) $\int_{0}^{+\infty} x\mathrm{e}^{-xy}\mathrm{d}y$

(i) 在  $[a, b]$  (a>0) 上一致收敛，
(ii) 在 $[0, b]$ 上不一致收敛；

(4) $\int_{0}^{1}\ln (xy)\mathrm{d}y$ 在 $\left[\frac{1}{b},b\right]\quad (b > 1)$ 上一致收敛；
(5) $\int_{0}^{1}\frac{\mathrm{d}x}{x^p}$ 在 $(-\infty ,b]$ （ $b < 1$ )上一致收敛.

2. 从等式 $\int_{a}^{b}\mathrm{e}^{-xy}\mathrm{d}y = \frac{\mathrm{e}^{-ax} - \mathrm{e}^{-bx}}{x}$ 出发，计算积分

$$
\int_ {0} ^ {+ \infty} \frac {\mathrm{e} ^ {- a x} - \mathrm{e} ^ {- b x}}{x} \mathrm{d} x \quad (b > a > 0).
$$

3. 证明函数

$$
F (y) = \int_ {0} ^ {+ \infty} \mathrm{e} ^ {- (x - y) ^ {2}} \mathrm{d} x
$$

在 $(-∞,+∞)$ 上连续（提示:证明中可利用公式 $\int_{0}^{+\infty}e^{-x^{2}}dx=\frac{\sqrt{\pi}}{2}$ ）.

4. 求下列积分:

(1) $\int_{0}^{+\infty}\frac{\mathrm{e}^{-a^2x^2}-\mathrm{e}^{-b^2x^2}}{x^2}\mathrm{d}x$ （提示:可利用公式 $\int_0^{+\infty}\mathrm{e}^{-x^2}\mathrm{d}x = \frac{\sqrt{\pi}}{2}$）；
(2) $\int_{0}^{+\infty}\mathrm{e}^{-t}\frac{\sin xt}{t}\mathrm{d}t;$
(3) $\int_{0}^{+\infty}\mathrm{e}^{-x}\frac{1 - \cos xy}{x^2}\mathrm{d}x.$

5. 回答下列问题:

（1）对极限 $\lim_{x\to 0^{+}}\int_{0}^{+\infty}2xy\mathrm{e}^{-xy^2}\mathrm{d}y$ 能否施行极限与积分运算顺序的交换来求解？
(2) 对  $\int_{0}^{1}\mathrm{d}y\int_{0}^{+\infty}(2y-2xy^{3})\mathrm{e}^{-xy^{2}}\mathrm{d}x$  能否运用积分顺序交换来求解？
(3) 对  $F(x)=\int_{0}^{+\infty}x^{3}\mathrm{e}^{-x^{2}y}\mathrm{d}y$  能否运用积分与求导运算顺序交换来求解？

6. 应用  $\int_{0}^{+\infty} e^{-at^{2}} dt = \frac{\sqrt{\pi}}{2} a^{-\frac{1}{2}} \quad (a > 0)$ ，证明:

(1) $\int_{0}^{+\infty} t^2 \mathrm{e}^{-at^2} \, \mathrm{d}t = \frac{\sqrt{\pi}}{4} a^{-\frac{3}{2}};$
(2) $\int_{0}^{+\infty} t^{2n} \mathrm{e}^{-at^2} \, \mathrm{d}t = \frac{\sqrt{\pi}}{2} \frac{1 \cdot 3 \cdot \cdots \cdot (2n - 1)}{2^n} a^{-\left(n + \frac{1}{2}\right)}.$

178

---

§ 3 欧拉积分

7. 应用  $\int_{0}^{+\infty}\frac{dx}{x^{2}+a^{2}}=\frac{\pi}{2a}$ ，求  $\int_{0}^{+\infty}\frac{dx}{\left(x^{2}+a^{2}\right)^{n+1}}$ .

8. 设  $f(x,y)$  为  $[a,b]\times[c,+\infty)$  上连续非负函数，

$$
I (x) = \int_ {c} ^ {+ \infty} f (x, y) \mathrm{d} y
$$

在 $[a,b]$ 上连续,证明 $I(x)$ 在 $[a,b]$ 上一致收敛.

9. 设在 $[a, +\infty) \times [c, d]$ 上成立不等式 $|f(x, y)| \leqslant F(x, y)$. 若 $\int_{a}^{+\infty} F(x, y) \mathrm{d}x$ 在 $y \in [c, d]$ 上一致收敛，证明 $\int_{a}^{+\infty} f(x, y) \mathrm{d}x$ 在 $y \in [c, d]$ 上一致收敛且绝对收敛.

## §3 欧拉积分

含参量积分

$$
\Gamma (s) = \int_ {0} ^ {+ \infty} x ^ {s - 1} \mathrm{e} ^ {- x} \mathrm{d} x, s > 0, \tag {1}
$$

$$
\mathrm{B} (p, q) = \int_ {0} ^ {1} x ^ {p - 1} (1 - x) ^ {q - 1} \mathrm{d} x, p > 0, q > 0 \tag {2}
$$

在应用中经常出现,它们统称为欧拉积分,其中前者又称为伽马(Gamma)函数(或写作 $\Gamma$ 函数),后者称为贝塔(Beta)函数(或写作B函数).下面我们分别讨论这两个函数的性质.

## 一、$\Gamma$ 函数

$\Gamma$ 函数(1)可写成如下两个积分之和:

$$
\Gamma (s) = \int_ {0} ^ {1} x ^ {s - 1} \mathrm{e} ^ {- x} \mathrm{d} x + \int_ {1} ^ {+ \infty} x ^ {s - 1} \mathrm{e} ^ {- x} \mathrm{d} x = \varPhi (s) + \varPsi (s),
$$

其中  $\Phi(s)$  当  $s \geqslant 1$  时是正常积分, 当 0 < s < 1 时是收敛的无界函数反常积分 (可用柯西判别法推得);  $\Psi(s)$  当 s > 0 时是收敛的无穷限反常积分 (也可用柯西判别法推得). 所以含参量积分 (1) 在 s > 0 时收敛, 即  $\Gamma$  函数的定义域为 s > 0.

1. $\Gamma(s)$ 在定义域 $s > 0$ 上连续且可导

在任何闭区间 $[a, b]$ ($a > 0$) 上，对于函数 $\Phi(s)$，当 $0 < x \leqslant 1$ 时有 $x^{s-1} \mathrm{e}^{-x} \leqslant x^{a-1} \mathrm{e}^{-x}$，由于 $\int_{0}^{1} x^{a-1} \mathrm{e}^{-x} \mathrm{d}x$ 收敛，从而 $\Phi(s)$ 在 $[a, b]$ 上一致收敛；对于 $\Psi(s)$，当 $1 \leqslant x < +\infty$ 时，有 $x^{s-1} \mathrm{e}^{-x} \leqslant x^{b-1} \mathrm{e}^{-x}$，由于 $\int_{1}^{+\infty} x^{b-1} \mathrm{e}^{-x} \mathrm{d}x$ 收敛，从而 $\Psi(s)$ 在 $[a, b]$ 上也一致收敛。于是 $\Gamma(s)$ 在 $s > 0$ 上连续。

用上述相同的方法考察积分

$$
\int_ {0} ^ {+ \infty} \frac {\partial}{\partial s} (x ^ {s - 1} \mathrm{e} ^ {- x}) \mathrm{d} x = \int_ {0} ^ {+ \infty} x ^ {s - 1} \mathrm{e} ^ {- x} \ln x \mathrm{d} x.
$$

它在任何闭区间 $[a, b]$ ($a > 0$) 上一致收敛. 于是由定理 19.11 得到 $\Gamma(s)$ 在 $[a, b]$ 上可导, 由 $a, b$ 的任意性, $\Gamma(s)$ 在 $s > 0$ 上可导, 且

179

---

第十九章 含参量积分

$$
\Gamma^ {\prime} (s) = \int_ {0} ^ {+ \infty} x ^ {s - 1} \mathrm{e} ^ {- x} \ln x \mathrm{d} x, s > 0.
$$

仿照上面的办法,还可推得  $\Gamma(s)$  在 s>0 上存在任意阶导数:

$$
\Gamma^ {(n)} (s) = \int_ {0} ^ {+ \infty} x ^ {s - 1} \mathrm{e} ^ {- x} (\ln x) ^ {n} \mathrm{d} x, s > 0.
$$

2. 递推公式 $\Gamma(s + 1) = s\Gamma(s)$

对下述积分应用分部积分法,有

$$
\begin{array}{l} \int_ {0} ^ {A} x ^ {s} \mathrm{e} ^ {- x} \mathrm{d} x = - \left. x ^ {s} \mathrm{e} ^ {- x} \right| _ {0} ^ {A} + s \int_ {0} ^ {A} x ^ {s - 1} \mathrm{e} ^ {- x} \mathrm{d} x \\ = - A ^ {s} \mathrm{e} ^ {- A} + s \int_ {0} ^ {A} x ^ {s - 1} \mathrm{e} ^ {- x} \mathrm{d} x. \\ \end{array}
$$

让 $A \to +\infty$ 就得到 $\Gamma$ 函数的递推公式:

$$
\Gamma (s + 1) = s \Gamma (s). \tag {3}
$$

设 $n < s \leqslant n + 1$，即 $0 < s - n \leqslant 1$，应用递推公式(3) $n$ 次可得到

$$
\begin{array}{l} \Gamma (s + 1) = s \Gamma (s) = s (s - 1) \Gamma (s - 1) = \dots \\ = s (s - 1) \dots (s - n) \Gamma (s - n). \tag {4} \\ \end{array}
$$

公式(3)还指出,如果已知  $\Gamma(s)$  在  $0<s\leqslant1$  上的值,那么在其他范围内的函数值可由它计算出来.

若 $s$ 为正整数 $n + 1$ ，则(4)式可写成

$$
\Gamma (n + 1) = n (n - 1) \cdot \dots \cdot 2 \cdot 1 \cdot \Gamma (1) = n! \int_ {0} ^ {+ \infty} \mathrm{e} ^ {- x} \mathrm{d} x = n!. \tag {5}
$$

## 3. $\Gamma$ 函数图像的讨论

对一切 $s > 0, \Gamma(s)$ 和 $\Gamma''(s)$ 恒大于0，因此 $\Gamma(s)$ 的图形位于 $s$ 轴上方，且是严格凸的。因为 $\Gamma(1) = \Gamma(2) = 1$ ，所以 $\Gamma(s)$ 在 $s > 0$ 上存在惟一的极小点 $x_0$ 且 $x_0 \in (1,2)$ 。又 $\Gamma(s)$ 在 $(0, x_0)$ 上严格减，在 $(x_0, +\infty)$ 上严格增。

由于 $\Gamma(s) = \frac{s\Gamma(s)}{s} = \frac{\Gamma(s + 1)}{s}$ ($s > 0$) 及 $\lim_{s \to 0^+} \Gamma(s + 1) = \Gamma(1) = 1$，故有

$$
\lim _ {s \to 0 ^ {+}} \Gamma (s) = \lim _ {s \to 0 ^ {+}} \frac {\Gamma (s + 1)}{s} = + \infty .
$$

由(5)式及 $\Gamma (s)$ 在 $(x_0, +\infty)$ 上严格增可推得

$$
\lim _ {s \to + \infty} \Gamma (s) = + \infty .
$$

综上所述, $\Gamma$ 函数的图像如图19-2中s>0部分所示.

## 4. 延拓 $\Gamma(s)$

改写递推公式(3)为

$$
\Gamma (s) = \frac {\Gamma (s + 1)}{s}. \tag {6}
$$

当-1<s<0时,(6)式右端有意义,于是可应用(6)式来定义左端函数 $\Gamma(s)$ 在(-1,0)上的值,并且可推得这时 $\Gamma(s)<0$ .

用同样的方法,利用  $\Gamma(s)$  已在  $(-1,0)$  上有定义这一事实,由(6)式又可定义  $\Gamma(s)$  在  $(-2,$

![](../../raw/pages_0161-0192/images/page_187_chart_26.jpg)

<details>
<summary>contour</summary>

| s | \(\Gamma(s)\) |
| --- | --- |
| 0 | 4 |
| ~1.5 | ~0.9 |
| ~3.8 | 4 |
</details>

图19-2

180

---

§ 3 欧拉积分

-1)上的值,而且这时  $\Gamma(s)>0$ . 依此下去可把  $\Gamma(s)$  延拓到整个数轴(除了 s=0,-1,-2,…以外),其图像如图 19-2 所示.

## 5. $\Gamma(s)$ 的其他形式

在应用中，$\Gamma(s)$ 也常以如下形式出现。如令 $x = y^2$，则有

$$
\Gamma (s) = \int_ {0} ^ {+ \infty} x ^ {s - 1} \mathrm{e} ^ {- x} \mathrm{d} x = 2 \int_ {0} ^ {+ \infty} y ^ {2 s - 1} \mathrm{e} ^ {- y ^ {2}} \mathrm{d} y \quad (s > 0). \tag {7}
$$

令 $x = py$ ，就有

$$
\Gamma (s) = \int_ {0} ^ {+ \infty} x ^ {s - 1} \mathrm{e} ^ {- x} \mathrm{d} x = p ^ {s} \int_ {0} ^ {+ \infty} y ^ {s - 1} \mathrm{e} ^ {- p y} \mathrm{d} y \quad (s > 0, p > 0). \tag {8}
$$

## 二、B函数

B函数(2)当 $p < 1$ 时，是以 $x = 0$ 为瑕点的无界函数反常积分；当 $q < 1$ 时，是以 $x = 1$ 为瑕点的无界函数反常积分.应用柯西判别法可证得当 $p > 0, q > 0$ 时这两个无界函数反常积分都收敛，所以函数 $\mathrm{B}(p, q)$ 的定义域为 $p > 0, q > 0$.

虽然 $\mathrm{B}(p,q)$ 是含两个参量的含参量积分，但与含单参数的含参量积分一样，相应的一致收敛性的定义、判别和性质是完全相同的.应用这些结论，我们可得以下 $\mathrm{B}(p,q)$ 的性质.

1. $\mathrm{B}(p,q)$ 在定义域 $p > 0, q > 0$ 内连续

由于对任何 $p_0 > 0, q_0 > 0$ 成立不等式

$$
x ^ {p - 1} (1 - x) ^ {q - 1} \leqslant x ^ {p _ {0} - 1} (1 - x) ^ {q _ {0} - 1}, p \geqslant p _ {0}, q \geqslant q _ {0},
$$

而积分 $\int_0^1 x^{p_0 - 1}(1 - x)^{q_0 - 1}\mathrm{d}x$ 收敛，故由魏尔斯特拉斯 $M$ 判别法知 $\mathrm{B}(p,q)$ 在 $p_0\leqslant p < + \infty$ ，$q_{0}\leqslant q < + \infty$ 上一致收敛.因而推得 $\mathrm{B}(p,q)$ 在 $p > 0,q > 0$ 上连续.

2. 对称性: $\mathrm{B}(p,q) = \mathrm{B}(q,p)$

作变换 $x = 1 - y$ ，得

$$
\begin{array}{l} \mathrm{B} (p, q) = \int_ {0} ^ {1} x ^ {p - 1} (1 - x) ^ {q - 1} \mathrm{d} x \\ = \int_ {0} ^ {1} (1 - y) ^ {p - 1} y ^ {q - 1} \mathrm{d} y = \mathrm{B} (q, p). \\ \end{array}
$$

3. 递推公式

$$
\mathrm{B} (p, q) = \frac {q - 1}{p + q - 1} \mathrm{B} (p, q - 1) \quad (p > 0, q > 1), \tag {9}
$$

$$
\mathrm{B} (p, q) = \frac {p - 1}{p + q - 1} \mathrm{B} (p - 1, q) \quad (p > 1, q > 0), \tag {10}
$$

$$
\mathrm{B} (p, q) = \frac {(p - 1) (q - 1)}{(p + q - 1) (p + q - 2)} \mathrm{B} (p - 1, q - 1) \quad (p > 1, q > 1).
$$

证 下面只证公式(9)，公式(10)可由对称性及公式(9)推得，而最后一个公式则可由公式(9)，(10)推得.

当 $p > 0, q > 1$ 时，有

$$
\mathrm{B} (p, q) = \int_ {0} ^ {1} x ^ {p - 1} (1 - x) ^ {q - 1} \mathrm{d} x
$$

181

---

第十九章 含参量积分

$$
\begin{array}{l} = \frac {x ^ {p} (1 - x) ^ {q - 1}}{p} \Bigg | _ {0} ^ {1} + \frac {q - 1}{p} \int_ {0} ^ {1} x ^ {p} (1 - x) ^ {q - 2} \mathrm{d} x \\ = \frac {q - 1}{p} \int_ {0} ^ {1} \left[ x ^ {p - 1} - x ^ {p - 1} (1 - x) \right] (1 - x) ^ {q - 2} \mathrm{d} x \\ = \frac {q - 1}{p} \int_ {0} ^ {1} x ^ {p - 1} (1 - x) ^ {q - 2} \mathrm{d} x - \frac {q - 1}{p} \int_ {0} ^ {1} x ^ {p - 1} (1 - x) ^ {q - 1} \mathrm{d} x \\ = \frac {q - 1}{p} \mathrm{B} (p, q - 1) - \frac {q - 1}{p} \mathrm{B} (p, q), \\ \end{array}
$$

移项并整理就得(9).

## 4. $\mathrm{B}(p,q)$ 的其他形式

在应用中 B 函数也常以如下形式出现. 如令  $x = \cos^{2}\varphi$ , 则有

$$
\mathrm{B} (p, q) = 2 \int_ {0} ^ {\frac {\pi}{2}} \sin^ {2 q - 1} \varphi \cos^ {2 p - 1} \varphi \mathrm{d} \varphi . \tag {11}
$$

令  $x=\frac{y}{1+y},1-x=\frac{1}{1+y},dx=\frac{dy}{(1+y)^{2}}$ ，则有

$$
\mathrm{B} (p, q) = \int_ {0} ^ {+ \infty} \frac {y ^ {p - 1}}{(1 + y) ^ {p + q}} \mathrm{d} y.
$$

考察 $\int_{1}^{+\infty}\frac{y^{p - 1}}{(1 + y)^{p + q}}\mathrm{d}y.$ 令 $y = \frac{1}{t}$，则有

$$
\int_ {1} ^ {+ \infty} \frac {y ^ {p - 1}}{(1 + y) ^ {p + q}} \mathrm{d} y = - \int_ {1} ^ {0} \frac {t ^ {q - 1}}{(1 + t) ^ {p + q}} \mathrm{d} t.
$$

所以

$$
\mathrm{B} (p, q) = \int_ {0} ^ {1} \frac {y ^ {p - 1} + y ^ {q - 1}}{(1 + y) ^ {p + q}} \mathrm{d} y.
$$

## 三、$\Gamma$ 函数与 B 函数之间的关系

当 m, n 为正整数时, 反复应用 B 函数的递推公式可得

$$
\begin{array}{l} \mathrm{B} (m, n) = \frac {n - 1}{m + n - 1} \mathrm{B} (m, n - 1) \\ = \frac {n - 1}{m + n - 1} \frac {n - 2}{m + n - 2} \dots \frac {1}{m + 1} \mathrm{B} (m, 1). \\ \end{array}
$$

又由于 $\mathrm{B}(m,1) = \int_0^1 x^{m - 1}\mathrm{d}x = \frac{1}{m}$，所以

$$
\begin{array}{l} \mathrm{B} (m, n) = \frac {n - 1}{m + n - 1} \frac {n - 2}{m + n - 2} \dots \frac {1}{m + 1} \frac {1}{m} \cdot \frac {(m - 1) !}{(m - 1) !} \\ = \frac {(n - 1) ! (m - 1) !}{(m + n - 1) !}, \\ \end{array}
$$

即

$$
\mathrm{B} (m, n) = \frac {\Gamma (n) \Gamma (m)}{\Gamma (n + m)}. \tag {12}
$$

对于任何正实数 p, q 也有相同的关系:

182

---

第十九章总练习题

$$
\mathrm{B} (p, q) = \frac {\Gamma (p) \Gamma (q)}{\Gamma (p + q)} \quad (p > 0, q > 0). \tag {13}
$$

这个关系式我们将在第二十一章 §8 中加以证明.

## 习题 19.3

1. 计算 $\Gamma\left(\frac{5}{2}\right), \Gamma\left(-\frac{5}{2}\right), \Gamma\left(\frac{1}{2} + n\right), \Gamma\left(\frac{1}{2} - n\right)$.

2. 计算  $\int_{0}^{\frac{\pi}{2}}\sin^{2n}u\,du,\int_{0}^{\frac{\pi}{2}}\sin^{2n+1}u\,du.$

3. 证明下列各式:

(1) $\Gamma(a) = \int_{0}^{1}\left(\ln \frac{1}{x}\right)^{a - 1}\mathrm{d}x, a > 0;$
(2) $\int_{0}^{+\infty}\frac{x^{a - 1}}{1 + x}\mathrm{d}x = \Gamma (a)\Gamma (1 - a),0 <   a <   1;$
(3) $\int_{0}^{1} x^{p-1} (1 - x^r)^{q-1} \, \mathrm{d}x = \frac{1}{r} \mathrm{B}\left(\frac{p}{r}, q\right), p > 0, q > 0, r > 0;$
(4) $\int_{0}^{+\infty}\frac{\mathrm{d}x}{1 + x^4} = \frac{\pi}{2\sqrt{2}}.$

4. 证明公式

$$
\mathrm{B} (p, q) = \mathrm{B} (p + 1, q) + \mathrm{B} (p, q + 1).
$$

5. 已知 $\Gamma\left(\frac{1}{2}\right) = \sqrt{\pi}$, 试证

$$
\int_ {- \infty} ^ {+ \infty} x ^ {2} \mathrm{e} ^ {- x ^ {2}} \mathrm{d} x = \frac {\sqrt {\pi}}{2}.
$$

6. 试将下列积分用欧拉积分表示,并指出参量的取值范围:

(1) $\int_{0}^{\frac{\pi}{2}}\sin^{m}x\cos^{n}x\mathrm{d}x;$

(2) $\int_{0}^{1}\left(\ln \frac{1}{x}\right)^{p}\mathrm{d}x.$

## 第十九章总练习题

1. 在区间 $1 \leqslant x \leqslant 3$ 上用线性函数 $a + bx$ 近似代替 $f(x) = x^2$，试求 $a, b$，使得积分 $\int_{1}^{3} (a + bx - x^2)^2 \mathrm{d}x$ 取最小值.

2. 设 $u(x) = \int_{0}^{1} k(x, y) v(y) \, \mathrm{d}y$，其中

$$
k (x, y) = \left\{ \begin{array}{l l} x (1 - y), & x \leqslant y, \\ y (1 - x), & x > y, \end{array} \right.
$$

$v(y)$ 为 $[0,1]$ 上的连续函数,证明

$$
u ^ {\prime \prime} (x) = - v (x).
$$

183

---

第十九章 含参量积分

3. 求函数

$$
F (a) = \int_ {0} ^ {+ \infty} \frac {\sin (1 - a ^ {2}) x}{x} \mathrm{d} x
$$

的不连续点,并作函数  $F(a)$  的图像.

4. 证明: 若 $\int_{0}^{+\infty} f(x, t) \mathrm{d}t$ 在 $x \in (0, +\infty)$ 上一致收敛于 $F(x)$, 且 $\lim_{x \to +\infty} f(x, t) = \varphi(t)$ 对任意 $t \in [a, b] \subset (0, +\infty)$ 一致地成立（即对任意 $\varepsilon > 0$, 存在 $M > 0$, 当 $x > M$ 时, $|f(x, t) - \varphi(t)| < \varepsilon$ 对一切 $t \in [a, b]$ 成立），则有

$$
\lim _ {x \to + \infty} F (x) = \int_ {0} ^ {+ \infty} \varphi (t)   \mathrm{d} t.
$$

5. 设 $f(x)$ 为二阶可微函数, $F(x)$ 为可微函数. 证明函数

$$
u (x, t) = \frac {1}{2} [ f (x - a t) + f (x + a t) ] + \frac {1}{2 a} \int_ {x - a t} ^ {x + a t} F (z) \mathrm{d} z
$$

满足弦振动方程

$$
\frac {\partial^ {2} u}{\partial t ^ {2}} = a ^ {2} \frac {\partial^ {2} u}{\partial x ^ {2}}
$$

及初值条件 $u(x,0) = f(x), u_t(x,0) = F(x)$.

6. 证明:

(1) $\int_{0}^{1}\frac{\ln x}{1 - x}\mathrm{d}x = -\frac{\pi^2}{6};$

(2) $\int_{0}^{u}\frac{\ln(1 - t)}{t}\mathrm{d}t = -\sum_{n = 1}^{\infty}\frac{u^n}{n^2}, 0\leqslant u\leqslant 1.$

![](../../raw/pages_0161-0192/images/page_191_image_14.jpg)

## 第十九章综合自测题

184
