$$
- 4 - y _ {0} = \frac {3}{2} \sqrt {x _ {0}} (0 - x _ {0}). \tag {1-9}
$$

求得方程(1-8)及(1-9)组成的方程组的解为 $x_{0}=4,y_{0}=8$ ，代入(1-7)式并化简，即得所求切线方程为

$$
3 x - y - 4 = 0.
$$

## 四、函数可导性与连续性的关系

设函数  $y=f(x)$  在点 x 处可导, 即

$$
\lim _ {\Delta x \to 0} \frac {\Delta y}{\Delta x} = f ^ {\prime} (x)
$$

存在.由具有极限的函数与无穷小的关系知道,

$$
\frac {\Delta y}{\Delta x} = f ^ {\prime} (x) + \alpha ,
$$

其中 $\alpha$ 为当 $\Delta x\to 0$ 时的无穷小.上式两边同乘 $\Delta x$ ，得

$$
\Delta y = f ^ {\prime} (x) \Delta x + \alpha \Delta x.
$$

由此可见, 当  $\Delta x \rightarrow 0$  时,  $\Delta y \rightarrow 0$ . 这就是说, 函数  $y = f(x)$  在点 x 处是连续的. 所以, 如果函数  $y = f(x)$  在点 x 处可导, 那么函数在该点必连续.

另一方面,一个函数在某点连续却不一定在该点可导.举例说明如下:

例 10 函数  $y=f(x)=\sqrt[3]{x}$  在区间  $(-∞,+∞)$  内连续,但在点 x=0 处不可导.这是因为在点 x=0 处有

$$
\frac {f (0 + h) - f (0)}{h} = \frac {\sqrt [ 3 ]{h} - 0}{h} = \frac {1}{h ^ {2 / 3}},
$$

因而， $\lim_{h\to0}\frac{f(0+h)-f(0)}{h}=\lim_{h\to0}\frac{1}{h^{2/3}}=+\infty$ ，即导数为无穷大（注意，导数不存在）。这一事实在图形中表现为曲线 $y=\sqrt[3]{x}$ 在原点O具有垂直于x轴的切线x=0（图2-4）。

例 11 函数  $y=\sqrt{x^{2}}$  （即  $y=|x|$ ）在  $(-∞,+∞)$  内连续，但在例 7 中已经看到，这个函数在 x=0 处不可导。曲线  $y=\sqrt{x^{2}}$  在原点 O 没有切线（图 2-5）。

![](images/page_96_image_17.jpg)

<details>
<summary>text_image</summary>

y
y=3√(x)
O
x
</details>

图2-4

![](images/page_96_image_19.jpg)

<details>
<summary>text_image</summary>

y
y=√x²
O
x
</details>

图2-5

由以上讨论可知,函数在某点连续是函数在该点可导的必要条件,但不是充分条件.

## 习题2- 1

1. 设物体绕定轴旋转, 在时间间隔 $[0, t]$ 上转过角度 $\theta$, 从而转角 $\theta$ 是 $t$ 的函数: $\theta = \theta(t)$. 如果旋转是匀速的, 那么称 $\omega = \frac{\theta}{t}$ 为该物体旋转的角速度. 如果旋转是非匀速的, 应怎样确定该物体在时刻 $t_0$ 的角速度?

2. 当物体的温度高于周围介质的温度时, 物体就不断冷却. 若物体的温度 T 与时间 t 的函数关系为  $T = T(t)$ , 应怎样确定该物体在时刻 t 的冷却速度?

3. 设某工厂生产 x 件产品的成本为

$$
C (x) = 2 0 0 0 + 1 0 0 x - 0. 1 x ^ {2} (\text {元}),
$$

这函数 $C(x)$ 称为成本函数,成本函数 $C(x)$ 的导数 ${C}^{\prime }\left( x\right)$ 在经济学中称为边际成本.试求

(1) 当生产 100 件产品时的边际成本；
(2) 生产第 101 件产品的成本,并与(1)中求得的边际成本作比较,说明边际成本的实际意义.

4. 设函数  $f(x)=\frac{(x-1)(x-2)\cdots(x-n)}{(x+1)(x+2)\cdots(x+n)}$ ，求  $f'(1)$ .

5. 证明 $(\cos x)'=-\sin x.$

6. 下列各题中均假定 $f'(x_0)$ 存在, 按照导数定义观察下列极限, 指出 $A$ 表示什么:

(1)  $\lim_{\Delta x\to0}\frac{f(x_{0}-\Delta x)-f(x_{0})}{\Delta x}=A;$

(2) $\lim_{x\to 0}\frac{f(x)}{x} = A$ ，其中 $f(0) = 0$ ，且 $f^{\prime}(0)$ 存在；

(3)  $\lim_{h\to0}\frac{f(x_{0}+h)-f(x_{0}-h)}{h}=A.$

以下两题中给出了四个结论,从中选出一个正确的结论:

7. 设

$$
f (x) = \left\{ \begin{array}{l l} \frac {2}{3} x ^ {3}, & x \leqslant 1, \\ x ^ {2}, & x > 1, \end{array} \right.
$$

则 $f(x)$ 在x=1处的().

(A) 左、右导数都存在

(B) 左导数存在, 右导数不存在

(C) 左导数不存在, 右导数存在

(D) 左、右导数都不存在

8. 设 $f(x)$ 可导, $F(x) = f(x)(1 + |\sin x|)$, 则 $f(0) = 0$ 是 $F(x)$ 在 $x = 0$ 处可导的 ( ).

(A) 充分必要条件

(B) 充分条件但非必要条件

(C) 必要条件但非充分条件

(D) 既非充分条件又非必要条件

9. 求下列函数的导数:

(1) $y = x^4$;

(2) $y = \sqrt[3]{x^2}$;

(3) $y = x^{1.6}$;

(4) $y = \frac{1}{\sqrt{x}}$;

(5)  $y=\frac{1}{x^{2}}$ ;

(6) $y = x^3\sqrt[5]{x}$;

(7) $y = \frac{x^2\sqrt[3]{x^2}}{\sqrt{x^5}}.$

10. 已知物体的运动规律为  $s = t^{3} \, m$ ，求这物体在  $t = 2 \, s$  时的速度.

11. 试证明:

(1) 若  $f(x)$  为可导的奇函数, 则  $f'(x)$  为偶函数;
(2) 若  $f(x)$  为可导的偶函数, 则  $f'(x)$  为奇函数;
(3) 若  $f(x)$  为偶函数, 且  $f'(0)$  存在, 则  $f'(0)=0$ .

12. 求曲线  $y = \sin x$  在具有下列横坐标的各点处切线的斜率:

$$
x = \frac {2}{3} \pi , \quad x = \pi .
$$

13. 求曲线  $y = \cos x$  上点  $\left(\frac{\pi}{3}, \frac{1}{2}\right)$  处的切线方程和法线方程.

14. 求曲线  $y=e^{x}$  在点  $(0,1)$  处的切线方程.

15. 在抛物线 $y = x^2$ 上取横坐标为 $x_1 = 1$ 及 $x_2 = 3$ 的两点，作过这两点的割线。问该抛物线上哪一点的切线平行于这条割线？

16. 讨论下列函数在 x=0 处的连续性与可导性:

(1) $y = |\sin x|$;

(2)  $y=\left\{\begin{aligned}x^{2}\sin\frac{1}{x},&x\neq0,\\ 0,&x=0.\end{aligned}\right.$

17. 设函数

$$
f (x) = \left\{ \begin{array}{l l} x ^ {2}, & x \leqslant 1, \\ a x + b, & x > 1. \end{array} \right.
$$

为了使函数 $f(x)$ 在x=1处连续且可导,a,b应取什么值?

18. 已知 $f(x) = \begin{cases} -x, & x < 0, \\ x^2, & x \geqslant 0, \end{cases}$ 求 $f_{+}^{\prime}(0)$ 及 $f_{-}^{\prime}(0)$，又 $f^{\prime}(0)$ 是否存在？

19. 已知 $f(x) = \begin{cases} \sin x, & x < 0, \\ x, & x \geqslant 0, \end{cases}$ 求 $f'(x)$.

20. 证明: 双曲线 $xy = a^2$ 上任一点处的切线与两坐标轴构成的三角形的面积都等于 $2a^2$.

## 第二节 函数的求导法则

在本节中,将介绍求导数的几个基本法则以及前一节中未讨论过的几个基本初等函数的导数公式.借助于这些法则和基本初等函数的导数公式,就能比较方便地求出

常见的初等函数的导数.

## 一、函数的和、差、积、商的求导法则

定理1 如果函数 $u = u(x)$ 及 $v = v(x)$ 都在点 $x$ 具有导数，那么它们的和、差、积、商（除分母为零的点外）都在点 $x$ 具有导数，且

(1) \([u(x)\pm v(x)]' = u'(x)\pm v'(x);\]
(2) $[u(x)v(x)]' = u'(x)v(x) + u(x)v'(x)$;
(3) $\left[\frac{u(x)}{v(x)}\right]' = \frac{u'(x)v(x) - u(x)v'(x)}{v^2(x)} (v(x) \neq 0)$.

证 (1) $[u(x)\pm v(x)]'$

$$
\begin{array}{l} = \lim _ {\Delta x \to 0} \frac {\left[ u (x + \Delta x) \pm v (x + \Delta x) \right] - \left[ u (x) \pm v (x) \right]}{\Delta x} \\ = \lim _ {\Delta x \to 0} \frac {u (x + \Delta x) - u (x)}{\Delta x} \pm \lim _ {\Delta x \to 0} \frac {v (x + \Delta x) - v (x)}{\Delta x} = u ^ {\prime} (x) \pm v ^ {\prime} (x). \\ \end{array}
$$

于是法则(1)获得证明.法则(1)可简单地表示为

$$
(u \pm v) ^ {\prime} = u ^ {\prime} \pm v ^ {\prime}.
$$

(2) $[u(x)v(x)]'$

$$
\begin{array}{l} = \lim _ {\Delta x \to 0} \frac {u (x + \Delta x) v (x + \Delta x) - u (x) v (x)}{\Delta x} \\ = \lim _ {\Delta x \to 0} \left[ \frac {u (x + \Delta x) - u (x)}{\Delta x} \cdot v (x + \Delta x) + u (x) \cdot \frac {v (x + \Delta x) - v (x)}{\Delta x} \right] \\ = \lim _ {\Delta x \to 0} \frac {u (x + \Delta x) - u (x)}{\Delta x} \cdot \lim _ {\Delta x \to 0} v (x + \Delta x) + u (x) \cdot \lim _ {\Delta x \to 0} \frac {v (x + \Delta x) - v (x)}{\Delta x} \\ = u ^ {\prime} (x) v (x) + u (x) v ^ {\prime} (x). \\ \end{array}
$$

其中 $\lim_{\Delta x\to 0}v(x + \Delta x) = v(x)$ 是由于 $v^{\prime}(x)$ 存在，故 $v(x)$ 在点 $x$ 连续.于是法则(2)获得证明.法则(2)可简单地表示为

$$
(u v) ^ {\prime} = u ^ {\prime} v + u v ^ {\prime}.
$$

(3) $\left[\frac{u(x)}{v(x)}\right]' = \lim_{\Delta x \to 0} \frac{\frac{u(x + \Delta x)}{v(x + \Delta x)} - \frac{u(x)}{v(x)}}{\Delta x}$

$$
\begin{array}{l} = \lim _ {\Delta x \to 0} \frac {u (x + \Delta x) v (x) - u (x) v (x + \Delta x)}{v (x + \Delta x) v (x) \Delta x} \\ = \lim _ {\Delta x \to 0} \frac {\left[ u (x + \Delta x) - u (x) \right] v (x) - u (x) \left[ v (x + \Delta x) - v (x) \right]}{v (x + \Delta x) v (x) \Delta x} \\ \end{array}
$$

$$
\begin{array}{l} = \lim _ {\Delta x \to 0} \frac {\frac {u (x + \Delta x) - u (x)}{\Delta x} v (x) - u (x) \frac {v (x + \Delta x) - v (x)}{\Delta x}}{v (x + \Delta x) v (x)} \\ = \frac {u ^ {\prime} (x) v (x) - u (x) v ^ {\prime} (x)}{v ^ {2} (x)}. \\ \end{array}
$$

于是法则(3)获得证明.法则(3)可简单地表示为

$$
\left(\frac {u}{v}\right) ^ {\prime} = \frac {u ^ {\prime} v - u v ^ {\prime}}{v ^ {2}}.
$$

定理1中的法则（1）、（2）可推广到任意有限个可导函数的情形.例如，设$u = u(x),v = v(x),w = w(x)$均可导，则有

![](images/page_100_image_5.jpg)

释疑解难
2-2

$$
\begin{array}{l} (u + v - w) ^ {\prime} = u ^ {\prime} + v ^ {\prime} - w ^ {\prime}, \\ (u v w) ^ {\prime} = [ (u v) w ] ^ {\prime} = (u v) ^ {\prime} w + (u v) w ^ {\prime} = (u ^ {\prime} v + u v ^ {\prime}) w + u v w ^ {\prime}, \\ \end{array}
$$

即

$$
(u v w) ^ {\prime} = u ^ {\prime} v w + u v ^ {\prime} w + u v w ^ {\prime}.
$$

在法则(2)中, 当  $v(x)=C$  (C 为常数) 时, 有

$$
(C u) ^ {\prime} = C u ^ {\prime}.
$$

例 1 设  $y=2x^{3}-5x^{2}+3x-7$ ，求  $y'$ .

解 $y' = (2x^3 - 5x^2 + 3x - 7)' = (2x^3)' - (5x^2)' + (3x)' - (7)'$

$$
= 2 \cdot 3 x ^ {2} - 5 \cdot 2 x + 3 - 0 = 6 x ^ {2} - 1 0 x + 3.
$$

例2 设 $f(x) = x^3 + 4\cos x - \sin \frac{\pi}{2}$, 求 $f'(x)$ 及 $f'\left(\frac{\pi}{2}\right)$.

解  $f'(x)=3x^{2}-4\sin x,$

$$
f ^ {\prime} \left(\frac {\pi}{2}\right) = \frac {3}{4} \pi^ {2} - 4.
$$

例3 设 $y = \mathrm{e}^{x}(\sin x + \cos x)$，求 $y'$.

解 $y' = (e^x)'(\sin x + \cos x) + e^x(\sin x + \cos x)'$

$$
= \mathrm{e} ^ {x} (\sin x + \cos x) + \mathrm{e} ^ {x} (\cos x - \sin x) = 2 \mathrm{e} ^ {x} \cos x.
$$

例 4 设  $y=\tan x$ , 求  $y'$ .

解 $y' = (\tan x)' = \left( \frac{\sin x}{\cos x} \right)' = \frac{(\sin x)' \cos x - \sin x(\cos x)'}{\cos^2 x}$

$$
= \frac {\cos^ {2} x + \sin^ {2} x}{\cos^ {2} x} = \frac {1}{\cos^ {2} x} = \sec^ {2} x,
$$

即

$$
(\tan x) ^ {\prime} = \sec^ {2} x.
$$

这就是正切函数的导数公式.

例 5 设  $y = \sec x = \frac{1}{\cos x}$ ，求  $y'$ .

解 $y' = (\sec x)' = \left( \frac{1}{\cos x} \right)' = \frac{(1)' \cos x - 1 \cdot (\cos x)'}{\cos^2 x} = \frac{\sin x}{\cos^2 x} = \sec x \tan x,$

即

$$
(\sec x) ^ {\prime} = \sec x \tan x.
$$

这就是正割函数的导数公式.

用类似方法,还可求得余切函数及余割函数的导数公式

$$
(\cot x) ^ {\prime} = \left(\frac {\cos x}{\sin x}\right) ^ {\prime} = - \csc^ {2} x,
$$

$$
(\csc x) ^ {\prime} = \left(\frac {1}{\sin x}\right) ^ {\prime} = - \csc x \cot x.
$$

## 二、反函数的求导法则

定理2 如果函数 $x = f(y)$ 在区间 $I_{y}$ 内单调、可导且 $f'(y) \neq 0$，那么它的反函数 $y = f^{-1}(x)$ 在区间 $I_{x} = \{x \mid x = f(y), y \in I_{y}\}$ 内也可导，且

$$
\left[ f ^ {- 1} (x) \right] ^ {\prime} = \frac {1}{f ^ {\prime} (y)} \quad \text {或} \quad \frac {\mathrm{d} y}{\mathrm{d} x} = \frac {1}{\frac {\mathrm{d} x}{\mathrm{d} y}}. \tag {2-1}
$$

证 由于 $x = f(y)$ 在 $I_y$ 内单调、可导（从而连续），由第一章第九节定理2知道，$x = f(y)$ 的反函数 $y = f^{-1}(x)$ 存在，且 $f^{-1}(x)$ 在 $I_x$ 内也单调、连续.

任取 $x \in I_x$，给 $x$ 以增量 $\Delta x$（$\Delta x \neq 0, x + \Delta x \in I_x$），由 $y = f^{-1}(x)$ 的单调性可知

$$
\Delta y = f ^ {- 1} (x + \Delta x) - f ^ {- 1} (x) \neq 0,
$$

于是有

$$
\frac {\Delta y}{\Delta x} = \frac {1}{\frac {\Delta x}{\Delta y}}.
$$

因 $y = f^{-1}(x)$ 连续，故

$$
\lim _ {\Delta x \to 0} \Delta y = 0,
$$

从而

$$
\left[ f ^ {- 1} (x) \right] ^ {\prime} = \lim _ {\Delta x \to 0} \frac {\Delta y}{\Delta x} = \lim _ {\Delta y \to 0} \frac {1}{\frac {\Delta x}{\Delta y}} = \frac {1}{f ^ {\prime} (y)}.
$$

上述结论可简单地说成:反函数的导数等于直接函数导数的倒数.

下面用上述结论来求反三角函数及对数函数的导数.

例6 设 $x = \sin y, y \in \left[-\frac{\pi}{2}, \frac{\pi}{2}\right]$ 为直接函数，则 $y = \arcsin x$ 是它的反函数. 函数 $x = \sin y$ 在开区间 $I_{\gamma} = \left(-\frac{\pi}{2}, \frac{\pi}{2}\right)$ 内单调、可导，且

$$
(\sin y) ^ {\prime} = \cos y > 0.
$$

因此，由公式(2-1)，在对应区间 $I_{x} = (-1,1)$ 内有

$$
(\arcsin x) ^ {\prime} = \frac {1}{(\sin y) ^ {\prime}} = \frac {1}{\cos y}.
$$

但  $\cos y=\sqrt{1-\sin^{2}y}=\sqrt{1-x^{2}}$  （因为当  $-\frac{\pi}{2}<y<\frac{\pi}{2}$  时， $\cos y>0$ ，所以根号前只取正号），从而得反正弦函数的导数公式

$$
(\arcsin x) ^ {\prime} = \frac {1}{\sqrt {1 - x ^ {2}}}. \tag {2-2}
$$

用类似的方法可得反余弦函数的导数公式

$$
(\arccos x) ^ {\prime} = - \frac {1}{\sqrt {1 - x ^ {2}}}. \tag {2-3}
$$

例7 设 $x = \tan y$ 是直接函数, $y \in I_y = \left(-\frac{\pi}{2}, \frac{\pi}{2}\right)$, 则 $y = \arctan x$ 是它的反函数. 函数 $x = \tan y$ 在 $I_y = \left(-\frac{\pi}{2}, \frac{\pi}{2}\right)$ 内单调、可导, 且

$$
(\tan y) ^ {\prime} = \sec^ {2} y \neq 0.
$$

因此，由公式(2-1)，在对应区间 $I_{x} = (-\infty, +\infty)$ 内有

$$
(\arctan x) ^ {\prime} = \frac {1}{(\tan y) ^ {\prime}} = \frac {1}{\sec^ {2} y}.
$$

但 $\sec^2 y = 1 + \tan^2 y = 1 + x^2$ ，从而得反正切函数的导数公式

$$
(\arctan x) ^ {\prime} = \frac {1}{1 + x ^ {2}}. \tag {2-4}
$$

用类似的方法可得反余切函数的导数公式

$$
(\operatorname{arccot} x) ^ {\prime} = - \frac {1}{1 + x ^ {2}}. \tag {2-5}
$$

如果利用三角学中的公式

$$
\arccos x = \frac {\pi}{2} - \arcsin x \quad \text {和} \quad \operatorname{arccot} x = \frac {\pi}{2} - \arctan x,
$$

那么从公式(2-2)和(2-4)，也立刻可得公式(2-3)和(2-5).

例8 设 $x = a^{y} (a > 0, a \neq 1)$ 为直接函数, 则 $y = \log_a x$ 是它的反函数. 函数 $x = a^{y}$ 在

区间  $I_{y}=(-\infty,+\infty)$  内单调、可导，且

$$
(a ^ {\gamma}) ^ {\prime} = a ^ {\gamma} \ln a \neq 0.
$$

因此，由公式(2-1)，在对应区间 $I_{x} = (0, +\infty)$ 内有

$$
(\log_ {a} x) ^ {\prime} = \frac {1}{(a ^ {y}) ^ {\prime}} = \frac {1}{a ^ {y} \ln a}.
$$

但 $a^y = x$ ，从而得到第一节例6中已求得的对数函数的导数公式

$$
(\log_ {a} x) ^ {\prime} = \frac {1}{x \ln a}.
$$

## 三、复合函数的求导法则

到目前为止,对于

$$
y = \ln \tan x, \quad y = \mathrm{e} ^ {x ^ {3}}, \quad y = \sin \frac {2 x}{1 + x ^ {2}}
$$

那样的函数,我们还不知道它们是否可导,可导的话如何求它们的导数.这些问题借助于下面的重要法则可以得到解决,从而使可以求得导数的函数的范围得到很大扩充.

定理3 如果 $u = g(x)$ 在点 $x$ 处可导, 而 $y = f(u)$ 在点 $u = g(x)$ 处可导, 那么复合函数 $y = f[g(x)]$ 在点 $x$ 处可导, 且其导数为

$$
\frac {\mathrm{d} y}{\mathrm{d} x} = f ^ {\prime} (u) \cdot g ^ {\prime} (x) \quad \text {或} \quad \frac {\mathrm{d} y}{\mathrm{d} x} = \frac {\mathrm{d} y}{\mathrm{d} u} \cdot \frac {\mathrm{d} u}{\mathrm{d} x}. \tag {2-6}
$$

证 由于 $y = f(u)$ 在点 $u$ 处可导, 因此

$$
\lim _ {\Delta u \to 0} \frac {\Delta y}{\Delta u} = f ^ {\prime} (u)
$$

存在,于是根据极限与无穷小的关系有

$$
\frac {\Delta y}{\Delta u} = f ^ {\prime} (u) + \alpha (\Delta u),
$$

其中 $\alpha (\Delta u)$ 是 $\Delta u\to 0$ 时的无穷小.上式中 $\Delta u\neq 0$ ，用 $\Delta u$ 乘上式两边，得

$$
\Delta y = f ^ {\prime} (u) \cdot \Delta u + \alpha (\Delta u) \cdot \Delta u. \tag {2-7}
$$

当 $\Delta u = 0$ 时，规定 $\alpha (\Delta u) = 0^{①}$，这时因 $\Delta y = f(u + \Delta u) - f(u) = 0$，而(2-7)式右端亦为零，故(2-7)式对 $\Delta u = 0$ 也成立.用 $\Delta x\neq 0$ 除(2-7)式两边，得

$$
\frac {\Delta y}{\Delta x} = f ^ {\prime} (u) \cdot \frac {\Delta u}{\Delta x} + \alpha (\Delta u) \cdot \frac {\Delta u}{\Delta x},
$$

于是

① 这时， $\alpha(\Delta u)=\left\{\begin{aligned}\frac{\Delta y}{\Delta u}-f'(u),&\quad\Delta u\neq0,\\ 0,&\quad\Delta u=0,\end{aligned}\right.$  函数  $\alpha(\Delta u)$  在  $\Delta u=0$  处连续，即  $\lim_{\Delta u\to0}\alpha(\Delta u)=0=\alpha(0)$ .

$$
\lim _ {\Delta x \to 0} \frac {\Delta y}{\Delta x} = \lim _ {\Delta x \to 0} \left[ f ^ {\prime} (u) \cdot \frac {\Delta u}{\Delta x} + \alpha (\Delta u) \cdot \frac {\Delta u}{\Delta x} \right].
$$

根据函数在某点处可导必在该点连续的性质知道, 当  $\Delta x \rightarrow 0$  时,  $\Delta u \rightarrow 0$ , 从而可以推知

$$
\lim _ {\Delta x \to 0} \alpha (\Delta u) = \lim _ {\Delta u \to 0} \alpha (\Delta u) = 0.
$$

又因 $u = g(x)$ 在点 $x$ 处可导，有

$$
\lim _ {\Delta x \to 0} \frac {\Delta u}{\Delta x} = g ^ {\prime} (x),
$$

故

$$
\lim _ {\Delta x \to 0} \frac {\Delta y}{\Delta x} = f ^ {\prime} (u) \cdot \lim _ {\Delta x \to 0} \frac {\Delta u}{\Delta x},
$$

即

$$
\frac {\mathrm{d} y}{\mathrm{d} x} = f ^ {\prime} (u) \cdot g ^ {\prime} (x).
$$

这就是公式(2-6).

例 9 设  $y=e^{x^{3}}$ ，求  $\frac{dy}{dx}$ .

解 $y = \mathrm{e}^{x^3}$ 可看作由 $y = \mathrm{e}^u, u = x^3$ 复合而成，因此

$$
\frac {\mathrm{d} y}{\mathrm{d} x} = \frac {\mathrm{d} y}{\mathrm{d} u} \cdot \frac {\mathrm{d} u}{\mathrm{d} x} = \mathrm{e} ^ {u} \cdot 3 x ^ {2} = 3 x ^ {2} \mathrm{e} ^ {x ^ {3}}.
$$

例10 设 $y = \sin \frac{2x}{1 + x^2}$，求 $\frac{\mathrm{dy}}{\mathrm{dx}}$.

解 $y = \sin \frac{2x}{1 + x^2}$ 可看作由 $y = \sin u, u = \frac{2x}{1 + x^2}$ 复合而成. 因

$$
\begin{array}{l} \frac {\mathrm{d} y}{\mathrm{d} u} = \cos u, \\ \frac {\mathrm{d} u}{\mathrm{d} x} = \frac {2 (1 + x ^ {2}) - (2 x) ^ {2}}{(1 + x ^ {2}) ^ {2}} = \frac {2 (1 - x ^ {2})}{(1 + x ^ {2}) ^ {2}}, \\ \end{array}
$$

所以

$$
\frac {\mathrm{d} y}{\mathrm{d} x} = \cos u \cdot \frac {2 (1 - x ^ {2})}{(1 + x ^ {2}) ^ {2}} = \frac {2 (1 - x ^ {2})}{(1 + x ^ {2}) ^ {2}} \cos \frac {2 x}{1 + x ^ {2}}.
$$

从以上例子看出,应用复合函数求导法则时,首先要分析所给函数可看作由哪些函数复合而成,或者说,所给函数能分解成哪些函数的复合.如果所给函数能分解成比较简单的函数的复合,而这些简单函数的导数我们已经会求,那么应用复合函数求导法则就可以求所给函数的导数了.

对复合函数的分解比较熟练后,就不必再写出中间变量,而可以采用下列例题的

方式来计算.

例 11 设  $y=\ln \sin x$ , 求  $\frac{dy}{dx}$ .

解 $\frac{\mathrm{dy}}{\mathrm{dx}} = (\ln \sin x)' = \frac{1}{\sin x} (\sin x)' = \frac{\cos x}{\sin x} = \cot x.$

例 12 设  $y=\sqrt[3]{1-2x^{2}}$ ，求  $\frac{dy}{dx}$ .

解 $\frac{\mathrm{dy}}{\mathrm{dx}} = [(1 - 2x^2)^{\frac{1}{3}}]' = \frac{1}{3} (1 - 2x^2)^{-\frac{2}{3}}\cdot (1 - 2x^2)' = \frac{-4x}{3\sqrt[3]{(1 - 2x^2)^2}}.$

复合函数的求导法则可以推广到多个中间变量的情形.我们以两个中间变量为例,设  $y=f(u)$ ,  $u=\varphi(v)$ ,  $v=\psi(x)$ , 则

$$
\frac {\mathrm{d} y}{\mathrm{d} x} = \frac {\mathrm{d} y}{\mathrm{d} u} \cdot \frac {\mathrm{d} u}{\mathrm{d} x},
$$

而 $\frac{\mathrm{d}u}{\mathrm{d}x} = \frac{\mathrm{d}u}{\mathrm{d}v}\cdot \frac{\mathrm{d}v}{\mathrm{d}x}$ 故复合函数 $y = f\{\varphi [\psi (x)]\}$ 的导数为

$$
\frac {\mathrm{d} y}{\mathrm{d} x} = \frac {\mathrm{d} y}{\mathrm{d} u} \cdot \frac {\mathrm{d} u}{\mathrm{d} v} \cdot \frac {\mathrm{d} v}{\mathrm{d} x}.
$$

当然,这里假定上式右端所出现的导数在相应处都存在.

例 13 设  $y=\ln\cos(e^{x})$ ，求  $\frac{dy}{dx}$ .

解 所给函数可分解为 $y = \ln u, u = \cos v, v = \mathrm{e}^x$. 因 $\frac{\mathrm{d}y}{\mathrm{d}u} = \frac{1}{u}, \frac{\mathrm{d}u}{\mathrm{d}v} = -\sin v, \frac{\mathrm{d}v}{\mathrm{d}x} = \mathrm{e}^x$，故

$$
\frac {\mathrm{d} y}{\mathrm{d} x} = \frac {1}{u} \cdot (- \sin v) \cdot \mathrm{e} ^ {x} = - \frac {\sin (\mathrm{e} ^ {x})}{\cos (\mathrm{e} ^ {x})} \cdot \mathrm{e} ^ {x} = - \mathrm{e} ^ {x} \tan (\mathrm{e} ^ {x}).
$$

不写出中间变量,此例可这样写:

$$
\frac {\mathrm{d} y}{\mathrm{d} x} = \left[ \ln \cos \left(\mathrm{e} ^ {x}\right) \right] ^ {\prime} = \frac {1}{\cos \left(\mathrm{e} ^ {x}\right)} \left[ \cos \left(\mathrm{e} ^ {x}\right) \right] ^ {\prime} = \frac {- \sin \left(\mathrm{e} ^ {x}\right)}{\cos \left(\mathrm{e} ^ {x}\right)} \left(\mathrm{e} ^ {x}\right) ^ {\prime} = - \mathrm{e} ^ {x} \tan \left(\mathrm{e} ^ {x}\right).
$$

例14 设 $y = \mathrm{e}^{\sin \frac{1}{x}}$，求 $y'$.

解 $y' = \left( e^{\sin \frac{1}{x}} \right)' = e^{\sin \frac{1}{x}} \left( \sin \frac{1}{x} \right)' = e^{\sin \frac{1}{x}} \cdot \cos \frac{1}{x} \cdot \left( \frac{1}{x} \right)' = -\frac{1}{x^2} e^{\sin \frac{1}{x}} \cos \frac{1}{x}$.

## 四、基本求导法则与导数公式

基本初等函数的导数公式与本节中所讨论的求导法则,在初等函数的求导运算中起着重要的作用,我们必须熟练地掌握它们.为了便于查阅,现在把这些导数公式和求导法则归纳如下:

## 1. 常数和基本初等函数的导数公式

(1) $(C)' = 0,$
(2) $(x^{\mu})' = \mu x^{\mu -1}$,
(3) $(\sin x)' = \cos x,$
(4) $(\cos x)' = -\sin x,$
(5) $(\tan x)' = \sec^2 x,$
(6) $(\cot x)' = -\csc^2 x,$
(7)  $(\sec x)' = \sec x \tan x,$
(8) $(\csc x)' = -\csc x \cot x,$
(9) $(a^{x})' = a^{x}\ln a$ ($a > 0, a \neq 1$),
(10) $(\mathrm{e}^x)' = \mathrm{e}^x,$
(11) $(\log_a x)' = \frac{1}{x \ln a} (a > 0, a \neq 1)$,
(12) $(\ln x)' = \frac{1}{x}$,
(13) $(\arcsin x)'=\frac{1}{\sqrt{1-x^{2}}}$ ,
(14) $(\arccos x)' = -\frac{1}{\sqrt{1 - x^2}}$,
(15) $(\arctan x)'=\frac{1}{1+x^{2}}$
(16) $(\operatorname{arccot} x)' = -\frac{1}{1 + x^2}$.

## 2. 函数的和、差、积、商的求导法则

设  $u=u(x)$ ,  $v=v(x)$  都可导, 则

(1) $(u\pm v)'=u'\pm v'$ ,

(2) $(Cu)'=Cu'$  (C 是常数),

(3) $(uv)'=u'v+uv'$ ,

(4) $\left(\frac{u}{v}\right)^{\prime}=\frac{u^{\prime}v-uv^{\prime}}{v^{2}}\quad(v\neq0).$

## 3. 反函数的求导法则

设 $x = f(y)$ 在区间 $I_{y}$ 内单调、可导且 $f'(y) \neq 0$，则它的反函数 $y = f^{-1}(x)$ 在 $I_{x} = f(I_{y})$ 内也可导，且

$$
\left[ f ^ {- 1} (x) \right] ^ {\prime} = \frac {1}{f ^ {\prime} (y)} \quad \text {或} \quad \frac {\mathrm{d} y}{\mathrm{d} x} = \frac {1}{\frac {\mathrm{d} x}{\mathrm{d} y}}.
$$

## 4. 复合函数的求导法则

设 $y = f(u)$，而 $u = g(x)$ 且 $f(u)$ 及 $g(x)$ 都可导，则复合函数 $y = f[g(x)]$ 的导数为

$$
\frac {\mathrm{d} y}{\mathrm{d} x} = \frac {\mathrm{d} y}{\mathrm{d} u} \cdot \frac {\mathrm{d} u}{\mathrm{d} x} \quad \text {或} \quad y ^ {\prime} (  x) = f ^ {\prime} (  u) \cdot g ^ {\prime} (  x).
$$

下面再举两个综合运用这些法则和导数公式的例子.

例 15 设  $y=\sin nx \cdot \sin^{n}x$  (n 为常数), 求  $y'$ .

解 首先应用积的求导法则得

$$
y ^ {\prime} = (\sin n x) ^ {\prime} \cdot \sin^ {n} x + \sin n x \cdot (\sin^ {n} x) ^ {\prime}.
$$

在计算 $(\sin nx)'$ 与 $(\sin^{n}x)'$ 时,都要应用复合函数求导法则,由此得

$$
\begin{array}{l} y ^ {\prime} = n \cos n x \cdot \sin^ {n} x + \sin n x \cdot n \sin^ {n - 1} x \cdot \cos x = n \sin^ {n - 1} x (\cos n x \cdot \sin x + \sin n x \cdot \cos x) \\ = n \sin^ {n - 1} x \cdot \sin (n + 1) x. \\ \end{array}
$$

\* 例16 证明下列双曲函数及反双曲函数的导数公式:

$$
\begin{array}{l} (\mathrm{sh} x) ^ {\prime} = \mathrm{ch} x, (\mathrm{ch} x) ^ {\prime} = \mathrm{sh} x, (\mathrm{th} x) ^ {\prime} = \frac {1}{\mathrm{ch} ^ {2} x}, \\ (\operatorname{arsh} x) ^ {\prime} = \frac {1}{\sqrt {1 + x ^ {2}}}, (\operatorname{arch} x) ^ {\prime} = \frac {1}{\sqrt {x ^ {2} - 1}}, (\operatorname{arth} x) ^ {\prime} = \frac {1}{1 - x ^ {2}}. \\ \end{array}
$$

证 由定理 1(1)、(2)，有

$$
(\mathrm{sh} x) ^ {\prime} = \left(\frac {\mathrm{e} ^ {x} - \mathrm{e} ^ {- x}}{2}\right) ^ {\prime} = \frac {(\mathrm{e} ^ {x}) ^ {\prime} - (\mathrm{e} ^ {- x}) ^ {\prime}}{2},
$$

再利用 $\left(\mathrm{e}^{x}\right)^{\prime}=\mathrm{e}^{x}$ 及定理3,得 $\left(\mathrm{e}^{-x}\right)^{\prime}=-\mathrm{e}^{-x}$ .于是

$$
(\mathrm{sh} x) ^ {\prime} = \frac {(\mathrm{e} ^ {x}) ^ {\prime} - (\mathrm{e} ^ {- x}) ^ {\prime}}{2} = \frac {\mathrm{e} ^ {x} + \mathrm{e} ^ {- x}}{2} = \mathrm{ch} x.
$$

同理可得

$$
(\mathrm{ch} x) ^ {\prime} = \left(\frac {\mathrm{e} ^ {x} + \mathrm{e} ^ {- x}}{2}\right) ^ {\prime} = \frac {\mathrm{e} ^ {x} - \mathrm{e} ^ {- x}}{2} = \mathrm{sh} x.
$$

由定理 1(3) 及上述结果, 有

$$
(\operatorname{th} x) ^ {\prime} = \left(\frac {\operatorname{sh} x}{\operatorname{ch} x}\right) ^ {\prime} = \frac {(\operatorname{sh} x) ^ {\prime} \operatorname{ch} x - \operatorname{sh} x (\operatorname{ch} x) ^ {\prime}}{\operatorname{ch} ^ {2} x} = \frac {\operatorname{ch} ^ {2} x - \operatorname{sh} ^ {2} x}{\operatorname{ch} ^ {2} x} = \frac {1}{\operatorname{ch} ^ {2} x}.
$$

由 arsh  $x=\ln(x+\sqrt{1+x^{2}})$ ，应用复合函数求导法则及定理 1(1)，有

$$
\begin{array}{l} (\operatorname{arsh} x) ^ {\prime} = \frac {1}{x + \sqrt {1 + x ^ {2}}} (x + \sqrt {1 + x ^ {2}}) ^ {\prime} \\ = \frac {1}{x + \sqrt {1 + x ^ {2}}} \left(1 + \frac {x}{\sqrt {1 + x ^ {2}}}\right) = \frac {1}{\sqrt {1 + x ^ {2}}}. \\ \end{array}
$$

由 arch  $x=\ln(x+\sqrt{x^{2}-1})$ ，同理可得

$$
(\operatorname{arch} x) ^ {\prime} = \frac {1}{\sqrt {x ^ {2} - 1}}, \quad x \in (1, + \infty).
$$

由 arth  $x=\frac{1}{2}\ln\frac{1+x}{1-x}$ ，可得

$$
(\operatorname{arth} x) ^ {\prime} = \frac {1}{1 - x ^ {2}}, \quad x \in (- 1, 1).
$$

#

例题精讲

2-1

## 习题2-2

1. 推导余切函数及余割函数的导数公式:

$$
(\cot x) ^ {\prime} = - \csc^ {2} x, \quad (\csc x) ^ {\prime} = - \csc x \cot x.
$$

2. 求下列函数的导数:

(1) $y = x^3 + \frac{7}{x^4} - \frac{2}{x} + 12$;

(2) $y = 5x^{3} - 2^{x} + 3\mathrm{e}^{x}$;

(3)  $y=2\tan x+\sec x-1;$

(4)  $y = \sin x \cdot \cos x;$

(5) $y = x^{2} \ln x;$

(6) $y = 3\mathrm{e}^{x}\cos x;$

(7)  $y=\frac{\ln x}{x};$

(8)  $y=\frac{e^{x}}{x^{2}}+\ln3;$

(9) $y = x^{2} \ln x \cos x;$

(10)  $s=\frac{1+\sin t}{1+\cos t}.$

3. 求下列函数在给定点处的导数:

(1) $y = \sin x - \cos x$, 求 $y' \bigg|_{x = \frac{\pi}{6}}$ 和 $y' \bigg|_{x = \frac{\pi}{4}}$;
(2) $\rho = \theta \sin \theta + \frac{1}{2} \cos \theta$, 求 $\left. \frac{\mathrm{d}\rho}{\mathrm{d}\theta} \right|_{\theta = \frac{\pi}{4}}$;
(3) $f(x)=\frac{3}{5-x}+\frac{x^{2}}{5}$ , 求  $f'(0)$  和  $f'(2)$ .

4. 以初速度 $v_{0}$ 竖直上抛的物体, 其上升高度 $s$ 与时间 $t$ 的关系是 $s = v_{0} t - \frac{1}{2} g t^{2}$. 求:

(1) 该物体的速度  $v(t)$ ;

(2) 该物体达到最高点的时刻.

5. 求曲线  $y=2\sin x+x^{2}$  上横坐标为 x=0 的点处的切线方程和法线方程.

6. 求下列函数的导数:

(1) $y=(2x+5)^{4}$;

(2) $y = \cos (4 - 3x)$;

(3)  $y=e^{-3x^{2}}$ ;

(4) $y = \ln (1 + x^2)$;

(5) $y = \sin^2 x$;

(6) $y = \sqrt{a^2 - x^2}$;

(7) $y = \tan x^2$;

(8) $y = \arctan(e^x)$;

(9) $y = (\arcsin x)^2$;

(10)  $y=\ln \cos x.$

7. 求下列函数的导数:

(1) $y = \arcsin (1 - 2x)$;

(2) $y = \frac{1}{\sqrt{1 - x^2}}$;

(3) $y = e^{-\frac{x}{2}} \cos 3x;$

(4)  $y = \arccos \frac{1}{x}$ ;

(5) $y = \frac{1 - \ln x}{1 + \ln x};$

(6) $y = \frac{\sin 2x}{x}$;

(7) $y = \arcsin \sqrt{x}$;

(8) $y = \ln (x + \sqrt{a^2 + x^2})$;

(9) $y = \ln (\sec x + \tan x)$;

(10) $y = \ln (\csc x - \cot x)$.

8. 求下列函数的导数:

(1) $y = \left(\arcsin \frac{x}{2}\right)^2$;

(2) $y = \ln \tan \frac{x}{2}$;

(3) $y = \sqrt{1 + \ln^2 x}$;

(4) $y = \mathrm{e}^{\arctan \sqrt{x}}$;

(5) $y = \sin^n x \cos nx$;

(6) $y = \arctan \frac{x + 1}{x - 1};$

(7)  $y=\frac{\arcsin x}{\arccos x}$ ;

(8) $y = \ln \ln \ln x;$

(9) $y = \frac{\sqrt{1 + x} - \sqrt{1 - x}}{\sqrt{1 + x} + \sqrt{1 - x}}$;

(10)  $y = \arcsin \sqrt{\frac{1 - x}{1 + x}}.$

9. 设函数 $f(x)$ 和 $g(x)$ 可导，且 $f^2(x) + g^2(x) \neq 0$，试求函数 $y = \sqrt{f^2(x) + g^2(x)}$ 的导数.

10. 设 $f(x)$ 可导, 求下列函数的导数 $\frac{\mathrm{d}y}{\mathrm{d}x}$:

(1) $y = f(x^2)$;

(2) $y = f(\sin^2 x) + f(\cos^2 x)$;

(3) $y = \frac{f(\mathrm{e}^x)}{\mathrm{e}^{f(x)}}$.

11. 求下列函数的导数:

(1) $y = \mathrm{e}^{-x}(x^2 - 2x + 3)$;

(2)  $y = \sin^{2}x \cdot \sin(x^{2})$ ;

(3) $y = \left(\arctan \frac{x}{2}\right)^2$;

(4)  $y=\frac{\ln x}{x^{n}}$ ;

(5)  $y=\frac{e^{t}-e^{-t}}{e^{t}+e^{-t}};$

(6) $y = \ln \cos \frac{1}{x}$;

(7)  $y=e^{-\sin^{2}\frac{1}{x}}$ ;

(8) $y = \sqrt{x + \sqrt{x}}$;

(9) $y = x \arcsin \frac{x}{2} + \sqrt{4 - x^2}$;

(10)  $y=\arcsin\frac{2t}{1+t^{2}}$

\* 12. 求下列函数的导数:

(1)  $y=\mathrm{ch}(\mathrm{sh}x)$ ;

(2) $y = \mathrm{sh} x \cdot \mathrm{e}^{\mathrm{ch} x}$;

(3)  $y=\mathrm{th}(\ln x)$ ;

(4) $y = \mathrm{sh}^3 x + \mathrm{ch}^2 x;$

(5) $y = \text{th}(1 - x^2)$;

(6) $y = \operatorname{arsh}(x^2 + 1)$;

(7) $y = \text{arch}(\mathrm{e}^{2x})$;

(8) $y = \arctan (\text{th } x)$;

(9)  $y=\ln ch x+\frac{1}{2ch^{2}x};$

(10) $y = \mathrm{ch}^2\left(\frac{x - 1}{x + 1}\right)$.

13. 设函数 $f(x)$ 和 $g(x)$ 均在点 $x_0$ 的某一邻域内有定义，$f(x)$ 在 $x_0$ 处可导，$f(x_0) = 0, g(x)$ 在 $x_0$ 处连续，试讨论 $f(x)g(x)$ 在 $x_0$ 处的可导性.

14. 设函数 $f(x)$ 满足下列条件:

(1) $f(x+y)=f(x)\cdot f(y)$ ，对一切 $x,y\in R;$

(2)  $f(x)$  在 x=0 处可导.

试证明 $f(x)$ 在 $\mathbb{R}$ 上处处可导，且 $f'(x) = f(x) \cdot f'(0)$.

## 第三节 高阶导数

我们知道,变速直线运动的速度  $v(t)$  是位置函数  $s(t)$  对时间 t 的导数,即

$$
v = \frac {\mathrm{d} s}{\mathrm{d} t} \quad \text {或} \quad v = s ^ {\prime},
$$

而加速度 $a(t)$ 又是速度 $v(t)$ 对时间 $t$ 的变化率，即速度 $v(t)$ 对时间 $t$ 的导数:

$$
a = \frac {\mathrm{d} v}{\mathrm{d} t} = \frac {\mathrm{d}}{\mathrm{d} t} \left(\frac {\mathrm{d} s}{\mathrm{d} t}\right)    \text {或}    a = (  s ^ {\prime}  ) ^ {\prime}.
$$

这种导数的导数 $\frac{\mathrm{d}}{\mathrm{d}t}\left(\frac{\mathrm{d}s}{\mathrm{d}t}\right)$ 或 $(s')'$ 叫做s对t的二阶导数，记作

$$
\frac {\mathrm{d} ^ {2} s}{\mathrm{d} t ^ {2}} \quad \text {或} \quad s ^ {\prime \prime} (t).
$$

所以,直线运动的加速度就是位置函数  $s(t)$  对时间 t 的二阶导数.

一般地, 函数 $y = f(x)$ 的导数 $y' = f'(x)$ 仍然是 $x$ 的函数. 我们把 $y' = f'(x)$ 的导数叫做函数 $y = f(x)$ 的二阶导数, 记作 $y''$ 或 $\frac{\mathrm{d}^2y}{\mathrm{d}x^2}$, 即

$$
y ^ {\prime \prime} = (  y ^ {\prime}  ) ^ {\prime} \quad \text {或} \quad \frac {\mathrm{d} ^ {2} y}{\mathrm{d} x ^ {2}}   =   \frac {\mathrm{d}}{\mathrm{d} x} \left(\frac {\mathrm{d} y}{\mathrm{d} x}\right).
$$

相应地, 把  $y=f(x)$  的导数  $f'(x)$  叫做函数  $y=f(x)$  的一阶导数.

类似地,二阶导数的导数叫做三阶导数,三阶导数的导数叫做四阶导数……一般地,(n-1)阶导数的导数叫做n阶导数,分别记作

$$
y ^ {\prime \prime \prime}, y ^ {(4)}, \dots , y ^ {(n)}
$$

或

$$
\frac {\mathrm{d} ^ {3} y}{\mathrm{d} x ^ {3}}, \frac {\mathrm{d} ^ {4} y}{\mathrm{d} x ^ {4}}, \dots , \frac {\mathrm{d} ^ {n} y}{\mathrm{d} x ^ {n}}.
$$

函数 $y = f(x)$ 具有 $n$ 阶导数,也常说成函数 $y = f(x)$ 为 $n$ 阶可导.如果函数 $y = f(x)$ 在点 $x$ 处具有 $n$ 阶导数,那么 $y = f(x)$ 在点 $x$ 的某一邻域内必定具有一切低于 $n$ 阶的导数.二阶及二阶以上的导数统称高阶导数.

由此可见,求高阶导数就是按前面学过的求导法则多次接连地求导数,若需要求函数的高阶导数公式,则需要在逐次求导过程中,善于寻求它的某种规律.

例 1 设  $y=ax+b$ ，求  $y''$ .

解  $y' = a, y'' = 0.$

例 2 设  $s = \sin \omega t$ , 求  $s''$ .

解 $s^{\prime} = \omega \cos \omega t,s^{\prime \prime} = -\omega^{2}\sin \omega t.$

例3 证明: 函数 $y = \sqrt{2x - x^2}$ 满足关系式 $y^3 y'' + 1 = 0$.

证 将 $y = \sqrt{2x - x^2}$ 求导, 得

$$
y ^ {\prime} = \frac {2 - 2 x}{2 \sqrt {2 x - x ^ {2}}} = \frac {1 - x}{\sqrt {2 x - x ^ {2}}},
$$

$$
y ^ {\prime \prime} = \frac {- \sqrt {2 x - x ^ {2}} - (1 - x) \frac {2 - 2 x}{2 \sqrt {2 x - x ^ {2}}}}{2 x - x ^ {2}} = \frac {- 2 x + x ^ {2} - (1 - x) ^ {2}}{(2 x - x ^ {2}) \sqrt {2 x - x ^ {2}}} = - \frac {1}{(2 x - x ^ {2}) ^ {\frac {3}{2}}} = - \frac {1}{y ^ {3}}.
$$

于是

$$
y ^ {3} y ^ {\prime \prime} + 1 = 0.
$$

下面介绍几个初等函数的 n 阶导数.

例 4 求指数函数  $y=e^{x}$  的 n 阶导数.

解 $y' = e^x, \quad y'' = e^x, \quad y''' = e^x, \quad y^{(4)} = e^x.$

一般地,可得

$$
y ^ {(n)} = \mathrm{e} ^ {x},
$$

即

$$
(\mathrm{e} ^ {x}) ^ {(n)} = \mathrm{e} ^ {x}.
$$

例 5 求正弦函数与余弦函数的 n 阶导数.

解  $y=\sin x,$

$$
\begin{array}{l} y ^ {\prime} = \cos x = \sin \left(x + \frac {\pi}{2}\right), \\ y ^ {\prime \prime} = \cos \left(x + \frac {\pi}{2}\right) = \sin \left(x + \frac {\pi}{2} + \frac {\pi}{2}\right) = \sin \left(x + 2 \cdot \frac {\pi}{2}\right), \\ y ^ {\prime \prime \prime} = \cos \left(x + 2 \cdot \frac {\pi}{2}\right) = \sin \left(x + 3 \cdot \frac {\pi}{2}\right), \\ y ^ {(4)} = \cos \left(x + 3 \cdot \frac {\pi}{2}\right) = \sin \left(x + 4 \cdot \frac {\pi}{2}\right), \\ \end{array}
$$

一般地,可得

$$
y ^ {(n)} = \sin \left(x + n \cdot \frac {\pi}{2}\right),
$$

即

$$
(\sin x) ^ {(n)} = \sin \left(x + n \cdot \frac {\pi}{2}\right).
$$

用类似方法,可得

$$
(\cos x) ^ {(n)} = \cos \left(x + n \cdot \frac {\pi}{2}\right).
$$

例 6 求函数  $y=\ln(1+x)$  的 n 阶导数.

解

$$
y ^ {\prime} = \frac {1}{1 + x}, \quad y ^ {\prime \prime} = - \frac {1}{(1 + x) ^ {2}}, \quad y ^ {\prime \prime \prime} = \frac {1 \cdot 2}{(1 + x) ^ {3}}, \quad y ^ {(4)} = - \frac {1 \cdot 2 \cdot 3}{(1 + x) ^ {4}},
$$

一般地,可得

$$
y ^ {(n)} = (- 1) ^ {n - 1} \frac {(n - 1) !}{(1 + x) ^ {n}},
$$

即

$$
\left[ \ln (1 + x) \right] ^ {(n)} = (- 1) ^ {n - 1} \frac {(n - 1) !}{(1 + x) ^ {n}}.
$$

通常规定 0! = 1, 所以这个公式当 n = 1 时也成立.

例 7 求幂函数的 n 阶导数公式.

解 设  $y=x^{\mu}$  ( $\mu$  是任意常数), 那么

$$
\begin{array}{l} y ^ {\prime} = \mu x ^ {\mu - 1}, \\ y ^ {\prime \prime} = \mu (\mu - 1) x ^ {\mu - 2}, \\ y ^ {\prime \prime \prime} = \mu (\mu - 1) (\mu - 2) x ^ {\mu - 3}, \\ y ^ {(4)} = \mu (\mu - 1) (\mu - 2) (\mu - 3) x ^ {\mu - 4}, \\ \end{array}
$$

一般地,可得

$$
y ^ {(n)} = \mu (\mu - 1) (\mu - 2) \dots (\mu - n + 1) x ^ {\mu - n},
$$

即

$$
(x ^ {\mu}) ^ {(n)} = \mu (\mu - 1) (\mu - 2) \dots (\mu - n + 1) x ^ {\mu - n}.
$$

当 $\mu = n$ 时, 得到

$$
(x ^ {n}) ^ {(n)} = n (n - 1) (n - 2) \cdot \dots \cdot 3 \cdot 2 \cdot 1 = n!,
$$

而

$$
(x ^ {n}) ^ {(n + k)} = 0 \quad (k = 1, 2, \dots).
$$

如果函数 $u = u(x)$ 及 $v = v(x)$ 都在点 $x$ 处具有 $n$ 阶导数，那么显然 $u(x) + v(x)$ 及 $u(x) - v(x)$ 也在点 $x$ 处具有 $n$ 阶导数，且

$$
(u \pm v) ^ {(n)} = u ^ {(n)} \pm v ^ {(n)}.
$$

但乘积 $u(x)v(x)$ 的 $n$ 阶导数并不简单.由

$$
(u v) ^ {\prime} = u ^ {\prime} v + u v ^ {\prime}
$$

首先得出

$$
(u v) ^ {\prime \prime} = u ^ {\prime \prime} v + 2 u ^ {\prime} v ^ {\prime} + u v ^ {\prime \prime},
$$

$$
(u v) ^ {\prime \prime \prime} = u ^ {\prime \prime \prime} v + 3 u ^ {\prime \prime} v ^ {\prime} + 3 u ^ {\prime} v ^ {\prime \prime} + u v ^ {\prime \prime \prime}.
$$

用数学归纳法可以证明

$$
(uv)^{(n)} = u^{(n)}v + nu^{(n - 1)}v' + \frac{n(n - 1)}{2!} u^{(n - 2)}v'' + \dots +\frac{n(n - 1)\cdots(n - k + 1)}{k!} u^{(n - k)}v^{(k)} + \dots +uv^{(n)}.
$$

上式称为莱布尼茨(Leibniz)公式.这个公式可以这样记忆:把 $(u+v)^{n}$ 按二项式定理展开写成

$$
(u + v) ^ {n} = u ^ {n} v ^ {0} + n u ^ {n - 1} v ^ {1} + \frac {n (n - 1)}{2 !} u ^ {n - 2} v ^ {2} + \dots + u ^ {0} v ^ {n},
$$

即

$$
(u + v) ^ {n} = \sum_ {k = 0} ^ {n} \mathrm{C} _ {n} ^ {k} u ^ {n - k} v ^ {k} ①,
$$

然后把 $k$ 次幂换成 $k$ 阶导数（零阶导数理解为函数本身），再把左端的 $u + v$ 换成 $uv$ ，这样就得到莱布尼茨公式

$$
(uv)^{(n)} = \sum_{k = 0}^{n}\mathrm{C}_{n}^{k}u^{(n - k)}v^{(k)}.
$$

例 8 设  $y=x^{2}e^{2x}$ ，求  $y^{(20)}$ .

解 设 $u = \mathrm{e}^{2x}, v = x^2$，则

$$
u ^ {(k)} = 2 ^ {k} \mathrm{e} ^ {2 x} \quad (k = 1, 2, \dots , 2 0),
$$

$$
v ^ {\prime} = 2 x, \quad v ^ {\prime \prime} = 2, \quad v ^ {(k)} = 0 \quad (k = 3, 4, \dots , 2 0),
$$

代入莱布尼茨公式,得

$$
\begin{array}{l} y ^ {(2 0)} = (x ^ {2} \mathrm{e} ^ {2 x}) ^ {(2 0)} = 2 ^ {2 0} \mathrm{e} ^ {2 x} \cdot x ^ {2} + 2 0 \cdot 2 ^ {1 9} \mathrm{e} ^ {2 x} \cdot 2 x + \frac {2 0 \cdot 1 9}{2 !} 2 ^ {1 8} \mathrm{e} ^ {2 x} \cdot 2 \\ = 2 ^ {2 0} \mathrm{e} ^ {2 x} (x ^ {2} + 2 0 x + 9 5). \\ \end{array}
$$

## 习题2-3

1. 求下列函数的二阶导数:

(1) $y = 2x^{2} + \ln x$;

(2) $y=e^{2x-1}$;

(3) $y = x \cos x$;

(4)  $y=e^{-t}\sin t;$

(5) $y = \sqrt{a^2 - x^2}$;

(6) $y = \ln (1 - x^2)$;

(7)  $y = \tan x;$

(8)  $y=\frac{1}{x^{3}+1};$

(9) $y = (1 + x^2)\arctan x$;

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 记号  $\sum$  表示对同一类型诸项求和.例如， $\sum_{k=0}^{n} C_{n}^{k} u^{n-k} v^{k}$  表示在  $C_{n}^{k} u^{n-k} v^{k}$  中依次令  $k = 0, 1, \cdots, n$ ，然后对这样得到的  $n + 1$  项求和.</span></small>

(10)  $y=\frac{e^{x}}{x};$

(11) $y = x\mathrm{e}^{x^2}$;

(12) $y = \ln (x + \sqrt{1 + x^2})$.

2. 设 $f(x) = (x + 10)^6$，求 $f'''(2)$.

3. 设 $f''(x)$ 存在, 求下列函数的二阶导数 $\frac{\mathrm{d}^2y}{\mathrm{d}x^2}$:

(1)  $y=f(x^{2})$ ;

(2) $y = \ln [f(x)]$.

4. 试从 $\frac{dx}{dy}=\frac{1}{y'}$ 导出:

(1) $\frac{\mathrm{d}^2x}{\mathrm{d}y^2} = -\frac{y''}{(y')^3}$;

(2) $\frac{\mathrm{d}^3x}{\mathrm{d}y^3} = \frac{3(y'')^2 - y'y'''}{(y')^5}.$

5. 已知物体的运动规律为  $s = A \sin \omega t$  (A,  $\omega$  是常数)，求该物体运动的加速度，并验证:

$$
\frac {\mathrm{d} ^ {2} s}{\mathrm{d} t ^ {2}} + \omega^ {2} s = 0.
$$

6. 密度大的陨星进入大气层时, 它离地心为 $s \mathrm{~km}$ 时的速度与 $\sqrt{s}$ 成反比. 试证陨星的加速度与 $s^2$ 成反比.

7. 假设质点沿 $x$ 轴运动的速度为 $\frac{\mathrm{d}x}{\mathrm{d}t} = f(x)$，试求该质点运动的加速度。

8. 设函数 $f(x) = \begin{cases} e^x \cos x, & x \leqslant 0, \\ ax^2 + bx + c, & x > 0, \end{cases}$ 试选择常数 $a, b, c$，使 $f(x)$ 具有二阶导数.

9. 求下列函数所指定的阶的导数:

(1) $y=e^{x}\cos x$, 求 $y^{(4)}$;

(2) $y = x^{2} \sin 2x$, 求 $y^{(50)}$.

\* 10. 求下列函数的 $n$ 阶导数的一般表达式:

(1)  $y = x^{n} + a_{1}x^{n-1} + a_{2}x^{n-2} + \cdots + a_{n-1}x + a_{n} \quad (a_{1}, a_{2}, \cdots, a_{n} \text{都是常数})$ ;

(2)  $y=\sin^{2}x;$

(3) $y = x \ln x$;

(4) $y = x\mathrm{e}^{x}$.

\* 11. 求函数 $f(x) = x^{2} \ln (1 + x)$ 在 $x = 0$ 处的 $n$ 阶导数 $f^{(n)}(0)$ ($n \geqslant 3$).

## 第四节 隐函数及由参数方程所确定的函数的导数 相关变化率

## 一、隐函数的导数

函数 $y = f(x)$ 表示两个变量 $y$ 与 $x$ 之间的对应关系, 这种对应关系可以用各种不同方式表达. 前面我们遇到的函数, 例如 $y = \sin x, y = \ln x + \sqrt{1 - x^2}$ 等, 这种函数表达方式的特点是: 等号左端是因变量的符号, 而右端是含有自变量的式子, 当自变量取定义域内任一值时, 由这式子能确定对应的函数值. 用这种方式表达的函数叫做显函数. 有些

函数的表达方式却不是这样,例如,方程

$$
x + y ^ {3} - 1 = 0
$$

表示一个函数,因为当变量 x 在  $(-∞,+∞)$  内取值时,变量 y 有确定的值与之对应.例如,当 x=0 时,y=1;当  $x=-1$  时, $y=\sqrt[3]{2}$ ,等等.这样的函数称为隐函数.

一般地,如果变量 x 和 y 满足一个方程  $F(x,y)=0$ , 在一定条件下, 当 x 取某区间内的任一值时, 相应地总有满足这方程的唯一的 y 值存在, 那么就说方程  $F(x,y)=0$  在该区间内确定了一个隐函数.

把一个隐函数化成显函数, 叫做隐函数的显化. 例如从方程 $x + y^3 - 1 = 0$ 解出 $y = \sqrt[3]{1 - x}$, 就把隐函数化成了显函数. 隐函数的显化有时是有困难的, 甚至是不可能的. 但在实际问题中, 有时需要计算隐函数的导数, 因此, 我们希望有一种方法, 不管隐函数能否显化, 都能直接由方程算出它所确定的隐函数的导数. 下面通过具体例子来说明这种方法.

例1 求由方程 $\mathrm{e}^{\gamma} + xy - \mathrm{e} = 0$ 所确定的隐函数的导数 $\frac{\mathrm{d}y}{\mathrm{d}x}$.

解 我们把方程两端分别对 $x$ 求导数①, 注意 $y = y(x)$. 方程左端对 $x$ 求导得

$$
\frac {\mathrm{d}}{\mathrm{d} x} (\mathrm{e} ^ {y} + x y - \mathrm{e}) = \mathrm{e} ^ {y} \frac {\mathrm{d} y}{\mathrm{d} x} + y + x \frac {\mathrm{d} y}{\mathrm{d} x},
$$

方程右端对 $x$ 求导得

$$
(0) ^ {\prime} = 0.
$$

由于等式两端对 x 的导数相等, 所以

$$
\mathrm{e} ^ {y} \frac {\mathrm{d} y}{\mathrm{d} x} + y + x \frac {\mathrm{d} y}{\mathrm{d} x} = 0,
$$

从而

$$
\frac {\mathrm{d} y}{\mathrm{d} x} = - \frac {y}{x + \mathrm{e} ^ {y}} \quad (x + \mathrm{e} ^ {y} \neq 0).
$$

在这个结果中,分式中的  $y=y(x)$  是由方程  $e^{y}+xy-e=0$  所确定的隐函数.

例2 求由方程 $y^{5} + 2y - x - 3x^{7} = 0$ 所确定的隐函数在 $x = 0$ 处的导数 $\frac{\mathrm{dy}}{\mathrm{dx}}\Big|_{x = 0}$.

解 把方程两端分别对 x 求导,由于方程两端的导数相等,所以

$$
5 y ^ {4} \frac {\mathrm{d} y}{\mathrm{d} x} + 2 \frac {\mathrm{d} y}{\mathrm{d} x} - 1 - 2 1 x ^ {6} = 0.
$$

由此得

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 假设方程 $F(x, y) = 0$ 确定一个函数 $y = y(x)$，把 $y = y(x)$ 代入方程便得恒等式 $F[x, y(x)] \equiv 0$. 因此，这里说的方程两端对 $x$ 求导，是指恒等式两端对 $x$ 求导.</span></small>

$$
\frac {\mathrm{d} y}{\mathrm{d} x} = \frac {1 + 2 1 x ^ {6}}{5 y ^ {4} + 2}.
$$

因为当 x=0 时,从原方程得 y=0,所以

$$
\frac {\mathrm{d} y}{\mathrm{d} x} \Big | _ {x = 0} = \frac {1}{2}.
$$

例3 求椭圆 $\frac{x^2}{16} +\frac{y^2}{9} = 1$ 在点 $\left(2,\frac{3}{2}\sqrt{3}\right)$ 处的切线方程（图2-6）.

解 由导数的几何意义知道,所求切线的斜率为

$$
k = y ^ {\prime} \Bigg | _ {x = 2}.
$$

椭圆方程的两端分别对 x 求导, 有

$$
\frac {x}{8} + \frac {2}{9} y \cdot \frac {\mathrm{d} y}{\mathrm{d} x} = 0.
$$

从而

$$
\frac {\mathrm{d} y}{\mathrm{d} x} = - \frac {9 x}{1 6 y}.
$$

![](images/page_116_image_11.jpg)

<details>
<summary>text_image</summary>

y
3
(2, \frac{3}{2}\sqrt{3})
O
4 x
</details>

图2-6

当 $x = 2$ 时，$y = \frac{3}{2}\sqrt{3}$，代入上式得

$$
\frac {\mathrm{d} y}{\mathrm{d} x} \Big | _ {x = 2} = - \frac {\sqrt {3}}{4}.
$$

于是所求的切线方程为

$$
y - \frac {3}{2} \sqrt {3} = - \frac {\sqrt {3}}{4} (x - 2),
$$

即

$$
\sqrt {3} x + 4 y - 8 \sqrt {3} = 0.
$$

例4 求由方程 $x - y + \frac{1}{2}\sin y = 0$ 所确定的隐函数的二阶导数 $\frac{\mathrm{d}^2y}{\mathrm{d}x^2}$.

解 应用隐函数的求导方法, 得

$$
1 - \frac {\mathrm{d} y}{\mathrm{d} x} + \frac {1}{2} \cos y \cdot \frac {\mathrm{d} y}{\mathrm{d} x} = 0,
$$

于是

$$
\frac {\mathrm{d} y}{\mathrm{d} x} = \frac {2}{2 - \cos y}.
$$

上式两端再对 x 求导, 得

$$
\frac {\mathrm{d} ^ {2} y}{\mathrm{d} x ^ {2}} = \frac {- 2 \sin y \frac {\mathrm{d} y}{\mathrm{d} x}}{(2 - \cos y) ^ {2}} = \frac {- 4 \sin y}{(2 - \cos y) ^ {3}}.
$$

上式右端分式中的  $y=y(x)$  是由方程  $x-y+\frac{1}{2}\sin y=0$  所确定的隐函数.

在某些场合,利用所谓对数求导法求导数比用通常的方法简便些.这种方法是先在  $y=f(x)$  的两端取对数,然后再求出 y 的导数.我们通过下面的例子来说明这种方法.

例 5 求  $y = x^{\sin x}$  (x > 0) 的导数.

解 这函数是幂指函数.为了求这函数的导数,可以先在等式两端取对数,得

$$
\ln y = \sin x \cdot \ln x.
$$

上式两端对 x 求导, 注意到  $y = y(x)$ , 得

$$
\frac {1}{y} y ^ {\prime} = \cos x \cdot \ln x + \sin x \cdot \frac {1}{x},
$$

于是

$$
y ^ {\prime} = y \left(\cos x \cdot \ln x + \frac {\sin x}{x}\right) = x ^ {\sin^ {\prime} x} \left(\cos x \cdot \ln x + \frac {\sin x}{x}\right).
$$

对于一般形式的幂指函数

$$
y = u ^ {v} \quad (u > 0), \tag {4-1}
$$

如果  $u=u(x)$ ,  $v=v(x)$  都可导, 那么可像例 5 那样利用对数求导法求出幂指函数 (4-1) 的导数, 也可把幂指函数 (4-1) 表示为

$$
y = \mathrm{e} ^ {v \ln u}.
$$

这样,便可直接求得

$$
y ^ {\prime} = \mathrm{e} ^ {v \ln u} \left(v ^ {\prime} \cdot \ln u + v \cdot \frac {u ^ {\prime}}{u}\right) = u ^ {v} \left(v ^ {\prime} \cdot \ln u + \frac {v u ^ {\prime}}{u}\right).
$$

例 6 求  $y=\sqrt{\frac{(x-1)(x-2)}{(x-3)(x-4)}}$  的导数.

解 先在等式两端取对数(假定 x>4)，得

$$
\ln y = \frac {1}{2} [ \ln (x - 1) + \ln (x - 2) - \ln (x - 3) - \ln (x - 4) ],
$$

上式两端对 x 求导, 注意到  $y = y(x)$ , 得

$$
\frac {1}{y} y ^ {\prime} = \frac {1}{2} \left(\frac {1}{x - 1} + \frac {1}{x - 2} - \frac {1}{x - 3} - \frac {1}{x - 4}\right),
$$

于是

$$
y ^ {\prime} = \frac {y}{2} \left(\frac {1}{x - 1} + \frac {1}{x - 2} - \frac {1}{x - 3} - \frac {1}{x - 4}\right).
$$

当 $x < 1$ 时，$y = \sqrt{\frac{(1 - x)(2 - x)}{(3 - x)(4 - x)}}$;

当 $2 < x < 3$ 时，$y = \sqrt{\frac{(x - 1)(x - 2)}{(3 - x)(4 - x)}}$

![](images/page_117_image_25.jpg)

例题精讲

2-2

用同样的方法可得与上面相同的结果.

## 二、由参数方程所确定的函数的导数

研究物体运动的轨迹时,常遇到参数方程.例如,研究抛射体的运动问题时,如果空气阻力忽略不计,那么抛射体的运动轨迹可表示为

$$
\left\{ \begin{array}{l} x = v _ {1} t, \\ y = v _ {2} t - \frac {1}{2} g t ^ {2}, \end{array} \right. \tag {4-2}
$$

其中  $v_{1}, v_{2}$  分别是抛射体初速度的水平、铅直分量，g 是重力加速度，t 是飞行时间，x 和 y 分别是飞行中抛射体在铅直平面上的位置的横坐标和纵坐标（图 2-7）.

![](images/page_118_image_6.jpg)

<details>
<summary>text_image</summary>

y
v₂
v
α
O
v₁
x
</details>

图2-7

在(4-2)式中， $x, y$ 都与 $t$ 存在函数关系. 如

果把对应于同一个 $t$ 值的 $y$ 与 $x$ 的值看做是对应的, 那么这样就得到 $y$ 与 $x$ 之间的函数关系. 消去(4-2)中的参数 $t$, 有

$$
y = \frac {v _ {2}}{v _ {1}} x - \frac {g}{2 v _ {1} ^ {2}} x ^ {2}.
$$

这是因变量 $y$ 与自变量 $x$ 直接联系的式子,也是参数方程(4-2)所确定的函数的显式表示.

一般地,若参数方程

$$
\left\{ \begin{array}{l} x = \varphi (t), \\ y = \psi (t) \end{array} \right. \tag {4-3}
$$

确定 $y$ 与 $x$ 间的函数关系, 则称此函数关系所表达的函数为由参数方程(4-3)所确定的函数.

在实际问题中,需要计算由参数方程(4-3)所确定的函数的导数.但从(4-3)中消去参数t有时会有困难.因此,我们希望有一种方法能直接由参数方程(4-3)算出它所确定的函数的导数.下面就来讨论由参数方程(4-3)所确定的函数的求导方法.

在(4-3)式中,如果函数 $x = \varphi (t)$ 具有单调连续反函数 $t = \varphi^{-1}(x)$, 且此反函数能与函数 $y = \psi (t)$ 构成复合函数, 那么由参数方程(4-3)所确定的函数可以看成是由函数 $y = \psi (t), t = \varphi^{-1}(x)$ 复合而成的函数 $y = \psi [\varphi^{-1}(x)]$. 现在, 要计算这个复合函数的导数. 为此再假定函数 $x = \varphi (t), y = \psi (t)$ 都可导, 而且 $\varphi'(t) \neq 0$. 于是根据复合函数的求导法则与反函数的求导法则, 就有

$$
\frac {\mathrm{d} y}{\mathrm{d} x} = \frac {\mathrm{d} y}{\mathrm{d} t} \cdot \frac {\mathrm{d} t}{\mathrm{d} x} = \frac {\mathrm{d} y}{\mathrm{d} t} \cdot \frac {1}{\frac {\mathrm{d} x}{\mathrm{d} t}} = \frac {\psi^ {\prime} (t)}{\varphi^ {\prime} (t)},
$$

即

$$
\frac {\mathrm{d} y}{\mathrm{d} x} = \frac {\psi^ {\prime} (t)}{\varphi^ {\prime} (t)}. \tag {4-4}
$$

上式也可写成

$$
\frac {\mathrm{d} y}{\mathrm{d} x} = \frac {\frac {\mathrm{d} y}{\mathrm{d} t}}{\frac {\mathrm{d} x}{\mathrm{d} t}}.
$$

(4-4)式就是由参数方程(4-3)所确定的x的函数的导数公式 $^{①}$ .

如果 $x = \varphi (t), y = \psi (t)$ 还是二阶可导的，那么从(4-4)式又可得到函数的二阶导数公式

$$
\frac {\mathrm{d} ^ {2} y}{\mathrm{d} x ^ {2}} = \frac {\mathrm{d}}{\mathrm{d} x} \left(\frac {\mathrm{d} y}{\mathrm{d} x}\right) = \frac {\mathrm{d}}{\mathrm{d} t} \left(\frac {\psi^ {\prime} (t)}{\varphi^ {\prime} (t)}\right) \cdot \frac {\mathrm{d} t}{\mathrm{d} x} = \frac {\psi^ {\prime \prime} (t) \varphi^ {\prime} (t) - \psi^ {\prime} (t) \varphi^ {\prime \prime} (t)}{\varphi^ {\prime 2} (t)} \cdot \frac {1}{\varphi^ {\prime} (t)},
$$

即

$$
\frac {\mathrm{d} ^ {2} \gamma}{\mathrm{d} x ^ {2}} = \frac {\psi^ {\prime \prime} (t) \varphi^ {\prime} (t) - \psi^ {\prime} (t) \varphi^ {\prime \prime} (t)}{\varphi^ {\prime 3} (t)}. \tag {4-5}
$$

例 7 已知椭圆的参数方程为

$$
\left\{ \begin{array}{l} x = a \cos t, \\ y = b \sin t, \end{array} \right.
$$

求椭圆在  $t=\frac{\pi}{4}$  相应的点处的切线方程(图 2-8).

解 当  $t=\frac{\pi}{4}$  时, 椭圆上的相应点  $M_{0}$  的坐标是

$$
x _ {0} = a \cos \frac {\pi}{4} = \frac {\sqrt {2} a}{2},
$$

$$
y _ {0} = b \sin \frac {\pi}{4} = \frac {\sqrt {2} b}{2}.
$$

曲线在点 $M_0$ 的切线斜率为

![](images/page_119_image_17.jpg)

<details>
<summary>text_image</summary>

y
b
M₀(√2a/2, √2b/2)
t=π/4
O
a
x
</details>

图2-8

① 作为 $x$ 的函数, $\frac{\mathrm{d}y}{\mathrm{d}x}$ 应表示为

$$
\left\{ \begin{array}{l} x = \varphi (t), \\ \frac {\mathrm{d} y}{\mathrm{d} x} = \frac {\psi^ {\prime} (t)}{\varphi^ {\prime} (t)}, \end{array} \right.
$$

但为了方便起见,通常把  $x=\varphi(t)$  省去.后面的公式(4-5)也作类似的理解.

$$
\frac {\mathrm{dy}}{\mathrm{dx}} \Big | _ {t = \frac {\pi}{4}} = \frac {(b \sin t) ^ {\prime}}{(a \cos t) ^ {\prime}} \Big | _ {t = \frac {\pi}{4}} = \frac {b \cos t}{- a \sin t} \Big | _ {t = \frac {\pi}{4}} = - \frac {b}{a}.
$$

代入点斜式方程,即得椭圆在点  $M_{0}$  处的切线方程

$$
y - \frac {\sqrt {2} b}{2} = - \frac {b}{a} \left(x - \frac {\sqrt {2} a}{2}\right).
$$

化简后得

$$
b x + a y - \sqrt {2}   a b = 0.
$$

例8 已知抛射体的运动轨迹的参数方程为

$$
\left\{ \begin{array}{l} x = v _ {1} t, \\ y = v _ {2} t - \frac {1}{2} g t ^ {2}, \end{array} \right.
$$

求抛射体在时刻 t 的运动速度的大小和方向.

解 先求速度的大小.

由于速度的水平分量为

$$
\frac {\mathrm{d} x}{\mathrm{d} t} = v _ {1},
$$

铅直分量为

$$
\frac {\mathrm{d} y}{\mathrm{d} t} = v _ {2} - g t,
$$

所以抛射体运动速度的大小为

$$
v = \sqrt {\left(\frac {\mathrm{d} x}{\mathrm{d} t}\right) ^ {2} + \left(\frac {\mathrm{d} y}{\mathrm{d} t}\right) ^ {2}} = \sqrt {v _ {1} ^ {2} + (v _ {2} - g t) ^ {2}}.
$$

再求速度的方向,也就是轨迹的切线方向.

设 $\alpha$ 是切线的倾角, 则根据导数的几何意义, 得

$$
\tan \alpha = \frac {\mathrm{d} y}{\mathrm{d} x} = \frac {\frac {\mathrm{d} y}{\mathrm{d} t}}{\frac {\mathrm{d} x}{\mathrm{d} t}} = \frac {v _ {2} - g t}{v _ {1}}.
$$

在抛射体刚射出(即 t=0)时，

$$
\tan \alpha \Big | _ {t = 0} = \frac {\mathrm{d} y}{\mathrm{d} x} \Big | _ {t = 0} = \frac {v _ {2}}{v _ {1}};
$$

当 $t = \frac{v_2}{g}$ 时，

$$
\tan \alpha \Big | _ {t = \frac {v _ {2}}{g}} = \frac {\mathrm{d} y}{\mathrm{d} x} \Big | _ {t = \frac {v _ {2}}{g}} = 0,
$$

这时,运动方向是水平的,即抛射体达到最高点(图 2-7).

例 9 计算由摆线(图 2-9)的参数方程

$$
\left\{ \begin{array}{l} x = a (t - \sin t), \\ y = a (1 - \cos t) \end{array} \right.
$$

![](images/page_121_image_4.jpg)

<details>
<summary>text_image</summary>

y
a
M(x, y)
O
πa
2πa
x
</details>

图2-9

所确定的函数  $y=y(x)$  的二阶导数.

解 $\frac{\mathrm{dy}}{\mathrm{dx}} = \frac{\frac{\mathrm{dy}}{\mathrm{dt}}}{\frac{\mathrm{dx}}{\mathrm{dt}}} = \frac{a\sin t}{a(1 - \cos t)} = \frac{\sin t}{1 - \cos t} = \cot \frac{t}{2}$ （$t \neq 2n\pi, n \in \mathbb{Z}$）.

$$
\begin{array}{l} \frac {\mathrm{d} ^ {2} y}{\mathrm{d} x ^ {2}} = \frac {\mathrm{d}}{\mathrm{d} t} \left(\cot \frac {t}{2}\right) \cdot \frac {1}{\frac {\mathrm{d} x}{\mathrm{d} t}} = - \frac {1}{2 \sin^ {2} \frac {t}{2}} \cdot \frac {1}{a (1 - \cos t)} \\ = - \frac {1}{a (1 - \cos t) ^ {2}} \quad (t \neq 2 n \pi , n \in \mathbf {Z}). \\ \end{array}
$$

## 三、相关变化率

设 $x = x(t)$ 及 $y = y(t)$ 都是可导函数, 而变量 $x$ 与 $y$ 间存在某种关系, 从而变化率 $\frac{\mathrm{d}x}{\mathrm{d}t}$ 与 $\frac{\mathrm{d}y}{\mathrm{d}t}$ 间也存在一定关系. 这两个相互依赖的变化率称为相关变化率. 相关变化率问题就是研究这两个变化率之间的关系, 以便从其中一个变化率求出另一个变化率.

例 10 一气球从离开观察员 500 m 处离地面铅直上升, 当气球高度为 500 m 时, 其速率为 140 m/min(米/分). 求此时观察员视线的仰角增加的速率是多少?

解 设气球上升 $t$ s(秒)后, 其高度为 $h$, 观察员视线的仰角为 $\alpha$, 则

$$
\tan \alpha = \frac {h}{5 0 0},
$$

其中  $\alpha$  及 h 都与 t 存在可导的函数关系. 上式两边对 t 求导, 得

$$
\sec^ {2} \alpha \cdot \frac {\mathrm{d} \alpha}{\mathrm{d} t} = \frac {1}{5 0 0} \cdot \frac {\mathrm{d} h}{\mathrm{d} t}.
$$

由已知条件, 存在  $t_{0}$ , 使  $h\left|_{t=t_{0}}=500\ m,\frac{dh}{dt}\right|_{t=t_{0}}=140\ m/min.$  又  $\tan\alpha\left|_{t=t_{0}}=1,\sec^{2}\alpha\right|_{t=t_{0}}=2.$  代入上式得

$$
2 \frac {\mathrm{d} \alpha}{\mathrm{d} t} \Bigg | _ {t = t _ {0}} = \frac {1}{5 0 0} \cdot 1 4 0,
$$

所以

$$
\frac {\mathrm{d} \alpha}{\mathrm{d} t} \Bigg | _ {t = t _ {0}} = \frac {7 0}{5 0 0} = 0. 1 4.
$$

即此时观察员视线的仰角增加的速率是 0.14 rad/min(弧度/分).

## 习题2-4

1. 求由下列方程所确定的隐函数的导数 $\frac{\mathrm{dy}}{\mathrm{dx}}$:

(1)  $y^{2}-2xy+9=0;$

(2) $x^{3}+y^{3}-3axy=0;$

(3)  $xy=e^{x+y}$ ;

(4) $y = 1 - x\mathrm{e}^{y}$.

2. 求曲线  $x^{\frac{2}{3}} + y^{\frac{2}{3}} = a^{\frac{2}{3}}$  在点  $\left(\frac{\sqrt{2}}{4}a, \frac{\sqrt{2}}{4}a\right)$  处的切线方程和法线方程.
3. 设曲线 $C$ 的方程为 $x^{2}y - xy^{2} = 2$, 试找出 $C$ 上有水平切线和铅直切线的点.
4. 求由下列方程所确定的隐函数的二阶导数 $\frac{\mathrm{d}^2y}{\mathrm{d}x^2}$:

(1) $b^{2}x^{2}+a^{2}y^{2}=a^{2}b^{2};$

(2) $y = \tan (x + y)$;

(3)  $y = 1 + x e^{y}$ ;

(4)  $y-2x=(x-y)\ln(x-y).$

5. 用对数求导法求下列函数的导数:

(1)  $y=\left(\frac{x}{1+x}\right)^{x}$ ;

(2) $y = \sqrt[5]{\frac{x - 5}{\sqrt[5]{x^2 + 2}}}$;

(3)  $y=\frac{\sqrt{x+2}(3-x)^{4}}{(x+1)^{5}};$

(4) $y = \sqrt{x\sin x\sqrt{1 - e^x}}$.

6. 求下列参数方程所确定的函数的导数 $\frac{\mathrm{dy}}{\mathrm{dx}}$:

(1) $\left\{\begin{aligned}x=at^{2},\\ y=bt^{3};\end{aligned}\right.$

(2) $\left\{ \begin{array}{l}x = \theta (1 - \sin \theta),\\ y = \theta \cos \theta . \end{array} \right.$

7. 已知  $\left\{\begin{aligned} x &= e^{t} \sin t, \\ y &= e^{t} \cos t, \end{aligned}\right.$  求当  $t = \frac{\pi}{3}$  时  $\frac{dy}{dx}$  的值.

8. 写出下列曲线在所给参数值相应的点处的切线方程和法线方程:

(1) $\left\{ \begin{array}{l} x = \sin t, \\ y = \cos 2t, \end{array} \right.$ 在 $t = \frac{\pi}{4}$ 处；

(2) $\left\{\begin{aligned}x&=\frac{3at}{1+t^{2}},\\ y&=\frac{3at^{2}}{1+t^{2}},\end{aligned}\right.$ 在t=2处.

9. 求下列参数方程所确定的函数的二阶导数 $\frac{\mathrm{d}^2y}{\mathrm{d}x^2}$:

(1) $\left\{ \begin{array}{l} x = \frac{t^2}{2}, \\ y = 1 - t; \end{array} \right.$

(2) $\left\{\begin{aligned}x=a\cos t,\\ y=b\sin t;\end{aligned}\right.$

(3) $\left\{ \begin{array}{l}x = 3\mathrm{e}^{-t},\\ y = 2\mathrm{e}^{t}; \end{array} \right.$

(4) $\left\{\begin{aligned}x=f'(t),\\ y=tf'(t)-f(t)\end{aligned}\right.$ 设 $f''(t)$ 存在且不为零.

\* 10. 求下列参数方程所确定的函数的三阶导数 $\frac{\mathrm{d}^3y}{\mathrm{d}x^3}$:

(1) $\left\{\begin{aligned}x=1-t^{2},\\ y=t-t^{3};\end{aligned}\right.$

(2) $\left\{ \begin{array}{l} x = \ln (1 + t^2), \\ y = t - \arctan t. \end{array} \right.$

11. 落在平静水面上的石头, 产生同心波纹. 若最外一圈波纹半径的增大速率总是  $6 \, m/s$ , 问在 2 s 末扰动水面面积增大的速率为多少?
12. 注水入深 8 m、上顶直径 8 m 的正圆锥形容器中, 其速率为  $4 \, m^{3}/min$ . 当水深为 5 m 时, 其表面上升的速率为多少?
13. 溶液自深  $18 \, cm$ 、顶直径  $12 \, cm$  的正圆锥形漏斗中漏入一直径为  $10 \, cm$  的圆柱形筒中。开始时漏斗中盛满了溶液。已知当溶液在漏斗中深为  $12 \, cm$  时，其表面下降的速率为  $1 \, cm/min$ 。问此时圆柱形筒中溶液表面上升的速率为多少？

## 第五节 函数的微分

## 一、微分的定义

先分析一个具体问题.一块正方形金属薄片受温度变化的影响,其边长由 $x_{0}$ 变到 $x_{0}+\Delta x$ （图2-10）,问此薄片的面积改变了多少?

设此薄片的边长为 x，面积为 A，则 A 与 x 存在函数关系: $A = x^{2}$ 。薄片受温度变化的影响时面积的改变量可以看成是当自变量 x 自  $x_{0}$  取得增量  $\Delta x$  时，函数  $A = x^{2}$  相应的增量  $\Delta A$ ，即

$$
\Delta A = (x _ {0} + \Delta x) ^ {2} - x _ {0} ^ {2} = 2 x _ {0} \Delta x + (\Delta x) ^ {2}.
$$

从上式可以看出, $\Delta A$ 分成两部分,第一部

![](images/page_123_image_18.jpg)

<details>
<summary>text_image</summary>

x₀
Δx
(Δx)²
x₀Δx
Δx
A=x₀²
x₀Δx
x₀
</details>

图2-10

分 $2x_{0}\Delta x$ 是 $\Delta x$ 的线性函数，即图中带有斜线的两个矩形面积之和，而第二部分 $(\Delta x)^{2}$ 在图中是带有交叉斜线的小正方形的面积，当 $\Delta x\to 0$ 时，第二部分 $(\Delta x)^{2}$ 是比 $\Delta x$ 高阶的无穷小，即 $(\Delta x)^{2} = o(\Delta x)$.由此可见，如果边长改变很微小，即 $|\Delta x|$ 很小时，面积的改变量 $\Delta A$ 可近似地用第一部分来代替.

一般地,如果函数  $y=f(x)$  满足一定条件,那么增量  $\Delta y$  可表示为

$$
\Delta y = A \Delta x + o (\Delta x),
$$

其中 $A$ 是不依赖于 $\Delta x$ 的常数，因此 $A\Delta x$ 是 $\Delta x$ 的线性函数，且 $\Delta y$ 与它的差

$$
\Delta y - A \Delta x = o (\Delta x)
$$

是比 $\Delta x$ 高阶的无穷小. 所以, 当 $A \neq 0$, 且 $|\Delta x|$ 很小时, 我们就可以用 $\Delta x$ 的线性函数 $A \Delta x$ 来近似代替 $\Delta y$.

定义 设函数 $y = f(x)$ 在某区间内有定义, $x_0$ 及 $x_0 + \Delta x$ 在这区间内, 如果函数的增量

$$
\Delta y = f (x _ {0} + \Delta x) - f (x _ {0})
$$

可表示为

$$
\Delta y = A \Delta x + o (\Delta x), \tag {5-1}
$$

其中 A 是不依赖于  $\Delta x$  的常数, 那么称函数  $y = f(x)$  在点  $x_{0}$  是可微的, 而  $A\Delta x$  叫做函数  $y = f(x)$  在点  $x_{0}$  相应于自变量增量  $\Delta x$  的微分, 记作 dy, 即

$$
\mathrm{d} y = A \Delta x.
$$

下面讨论函数可微的条件. 设函数  $y=f(x)$  在点  $x_{0}$  可微, 则按定义有 (5-1) 式成立. (5-1) 式两边除以  $\Delta x$ , 得

$$
\frac {\Delta y}{\Delta x} = A + \frac {o (\Delta x)}{\Delta x}.
$$

于是, 当  $\Delta x \rightarrow 0$  时, 由上式就得到

$$
A = \lim _ {\Delta x \to 0} \frac {\Delta y}{\Delta x} = f ^ {\prime} (x _ {0}).
$$

因此,如果函数 $f(x)$ 在点 $x_{0}$ 可微,那么 $f(x)$ 在点 $x_{0}$ 也一定可导(即 $f'(x_{0})$ 存在),且 $A=f'(x_{0})$ .

反之,如果  $y=f(x)$  在点  $x_{0}$  可导,即

$$
\lim _ {\Delta x \to 0} \frac {\Delta y}{\Delta x} = f ^ {\prime} (x _ {0})
$$

存在,根据极限与无穷小的关系(第一章第四节定理1),上式可写成

$$
\frac {\Delta y}{\Delta x} = f ^ {\prime} (x _ {0}) + \alpha ,
$$

其中 $\alpha \rightarrow 0$ （当 $\Delta x\to 0$ ).由此又有

$$
\Delta y = f ^ {\prime} (x _ {0}) \Delta x + \alpha \Delta x.
$$

因 $\alpha \Delta x = o(\Delta x)$，且 $f'(x_0)$ 不依赖于 $\Delta x$，故上式相当于(5-1)式，所以 $f(x)$ 在点 $x_0$ 也是可微的。

由此可见，函数 $f(x)$ 在点 $x_0$ 可微的充分必要条件是函数 $f(x)$ 在点 $x_0$ 可导，且当

$f(x)$  在点  $x_{0}$  可微时, 其微分一定是

$$
\mathrm{d} y = f ^ {\prime} \left(x _ {0}\right) \Delta x. \tag {5-2}
$$

当 $f'(x_{0})\neq0$ 时,有

$$
\lim _ {\Delta x \to 0} \frac {\Delta y}{\mathrm{d} y} = \lim _ {\Delta x \to 0} \frac {\Delta y}{f ^ {\prime} (x _ {0}) \Delta x} = \frac {1}{f ^ {\prime} (x _ {0})} \lim _ {\Delta x \to 0} \frac {\Delta y}{\Delta x} = 1.
$$

从而, 当  $\Delta x \rightarrow 0$  时,  $\Delta y$  与 dy 是等价无穷小, 于是由第一章第七节定理 1 可知, 这时有

$$
\Delta y = \mathrm{d} y + o (\mathrm{d} y), \tag {5-3}
$$

即 dy 是  $\Delta y$  的主部①. 又由于  $\mathrm{dy}=f'(x_{0})\Delta x$  是  $\Delta x$  的线性函数, 所以在  $f'(x_{0})\neq0$  的条件下, 我们说 dy 是  $\Delta y$  的线性主部(当  $\Delta x\to0$ ). 于是我们得到结论: 在  $f'(x_{0})\neq0$  的条件下, 以微分  $\mathrm{dy}=f'(x_{0})\Delta x$  近似代替增量  $\Delta y=f(x_{0}+\Delta x)-f(x_{0})$  时, 其误差为  $o(\mathrm{dy})$ . 因此, 在  $|\Delta x|$  很小时, 有近似等式

$$
\Delta y \approx \mathrm{d} y.
$$

例 1 求函数  $y=x^{2}$  在 x=1 和 x=3 处的微分.

解 函数 $y = x^2$ 在 $x = 1$ 处的微分为

$$
\mathrm{d} y = (x ^ {2}) ^ {\prime} \mid_ {x = 1} \Delta x = 2 \Delta x,
$$

在 $x = 3$ 处的微分为

$$
\mathrm{d} y = (x ^ {2}) ^ {\prime} \mid_ {x = 3} \Delta x = 6 \Delta x.
$$

函数  $y=f(x)$  在任意点 x 的微分, 称为函数的微分, 记作 dy 或  $\mathrm{d}f(x)$ , 即

$$
\mathrm{d} y = f ^ {\prime} (x) \Delta x.
$$

例如,函数  $y=\cos x$  的微分为

$$
\mathrm{d} y = (\cos x) ^ {\prime} \Delta x = - \sin x \Delta x,
$$

函数 $y = \mathrm{e}^{x}$ 的微分为

$$
\mathrm{d} y = \left(\mathrm{e} ^ {x}\right) ^ {\prime} \Delta x = \mathrm{e} ^ {x} \Delta x.
$$

显然,函数的微分  $\mathrm{d}y=f'(x)\Delta x$  与 x 和  $\Delta x$  有关.

例 2 求函数  $y=x^{3}$  当 x=2,  $\Delta x=0.02$  时的微分.

解 先求函数在任意点 $x$ 的微分

$$
\mathrm{d} y = (x ^ {3}) ^ {\prime} \Delta x = 3 x ^ {2} \Delta x.
$$

再求函数当  $x=2,\Delta x=0.02$  时的微分

$$
\mathrm{dy} \Bigg | _ {\substack {x = 2 \\ \Delta x = 0.02}} = (3x^2\Delta x) \Bigg | _ {\substack {x = 2 \\ \Delta x = 0.02}} = 3\times 2^2\times 0.02 = 0.24.
$$

通常把自变量 x 的增量  $\Delta x$  称为自变量的微分, 记作 dx, 即 dx =  $\Delta x$ . 于是函数  $y = f(x)$  的微分又可记作

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 设  $\alpha$  及  $\beta$  都是在同一个自变量的变化过程中的无穷小, 如果  $\beta = \alpha + o(\alpha)$ , 那么称  $\alpha$  是  $\beta$  的主部.</span></small>

$$
\mathrm{d} y = f ^ {\prime} (x) \mathrm{d} x.
$$

从而有

$$
\frac {\mathrm{d} y}{\mathrm{d} x} = f ^ {\prime} (x).
$$

这就是说,函数的微分 dy 与自变量的微分 dx 之商等于该函数的导数.因此,导数也叫做“微商”.

## 二、微分的几何意义

为了对微分有比较直观的了解,我们来说明微分的几何意义.

在直角坐标系中, 函数  $y=f(x)$  的图形是一条曲线. 对于某一固定的  $x_{0}$  值, 曲线上有一个确定点  $M(x_{0}, y_{0})$ , 当自变量 x 有微小增量  $\Delta x$  时, 就得到曲线上另一点  $N(x_{0}+\Delta x, y_{0}+\Delta y)$ . 从图 2-11 可知:

$$
M Q = \Delta x, \quad Q N = \Delta y.
$$

![](images/page_126_image_9.jpg)

<details>
<summary>text_image</summary>

y
T
N
P
dy
Δy
M
y=f(x)
Q
Δx
O
x₀
x₀+Δx
α
x
</details>

图2-11

过点 $M$ 作曲线的切线 $MT$, 它的倾角为 $\alpha$, 则

$$
Q P = M Q \cdot \tan \alpha = \Delta x \cdot f ^ {\prime} (x _ {0}),
$$

即

$$
\mathrm{d} y = Q P.
$$

由此可见,对于可微函数 $y = f(x)$ 而言,当 $\Delta y$ 是曲线 $y = f(x)$ 上的点的纵坐标的增量时,dy 就是曲线的切线上点的纵坐标的相应增量.当 $|\Delta x|$ 很小时, $|\Delta y - dy|$ 比 $|\Delta x|$ 小得多.因此在点 M 的邻近,我们可以用切线段来近似代替曲线段.在局部范围内用线性函数近似代替非线性函数,在几何上就是局部用切线段近似代替曲线段,这在数学上称为非线性函数的局部线性化,这是微分学的基本思想方法之一.这种思想方法在自然科学和工程问题的研究中是经常采用的.

## 三、基本初等函数的微分公式与微分运算法则

从函数的微分的表达式

$$
\mathrm{d} y = f ^ {\prime} (x) \mathrm{d} x
$$

可以看出,要计算函数的微分,只要计算函数的导数,再乘自变量的微分.因此,可得如下的微分公式和微分运算法则.

## 1. 基本初等函数的微分公式

由基本初等函数的导数公式,可以直接写出基本初等函数的微分公式.为了便于

对照,列表于下:

| 导数公式 | 微分公式 |
| --- | --- |
| $(x^{\mu})' = \mu x^{\mu-1}$ ($\mu$ 是任意常数) | $d(x^{\mu}) = \mu x^{\mu-1} dx$ ($\mu$ 是任意常数) |
| $(\sin x)' = \cos x$ | $d(\sin x) = \cos x dx$ |
| $(\cos x)' = -\sin x$ | $d(\cos x) = -\sin x dx$ |
| $(\tan x)' = \sec^{2} x$ | $d(\tan x) = \sec^{2} x dx$ |
| $(\cot x)' = -\csc^{2} x$ | $d(\cot x) = -\csc^{2} x dx$ |
| $(\sec x)' = \sec x\tan x$ | $d(\sec x) = \sec x\tan x dx$ |
| $(\csc x)' = -\csc x\cot x$ | $d(\csc x) = -\csc x\cot x dx$ |
| $(a^{x})' = a^{x}\ln a$ ($a>0$ 且 $a \neq 1$) | $d(a^{x}) = a^{x}\ln adx$ ($a>0$ 且 $a \neq 1$) |
| $(e^{x})' = e^{x}$ | $d(e^{x}) = e^{x} dx$ |
| $(\log_{a}x)' = \frac{1}{x\ln a}$ ($a>0$ 且 $a \neq 1$) | $d(\log_{a}x) = \frac{1}{x\ln a} dx$ ($a>0$ 且 $a \neq 1$) |
| $(\ln x)' = \frac{1}{x}$ | $d(\ln x) = \frac{1}{x} dx$ |
| $(\arcsin x)' = \frac{1}{\sqrt{1-x^{2}}}$ | $d(\arcsin x) = \frac{1}{\sqrt{1-x^{2}}} dx$ |
| $(\arccos x)' = -\frac{1}{\sqrt{1-x^{2}}}$ | $d(\arccos x) = -\frac{1}{\sqrt{1-x^{2}}} dx$ |
| $(\arctan x)' = \frac{1}{1+x^{2}}$ | $d(\arctan x) = \frac{1}{1+x^{2}} dx$ |
| $(\operatorname{arccot} x)' = -\frac{1}{1+x^{2}}$ | $d(\operatorname{arccot} x) = -\frac{1}{1+x^{2}} dx$ |

## 2. 函数和、差、积、商的微分法则

由函数和、差、积、商的求导法则,可推得相应的微分法则.为了便于对照,列成下表(表中  $u=u(x)$ ,  $v=v(x)$  都可导).

| 函数和、差、积、商的求导法则 | 函数和、差、积、商的微分法则 |
| --- | --- |
| $(u \pm v)' = u' \pm v'$ | $d(u \pm v) = du \pm dv$ |
| $(Cu)' = Cu' (C \text{是常数})$ | $d(Cu) = Cdu (C \text{是常数})$ |
| $(uv)' = u'v + uv'$ | $d(uv) = vdu + udv$ |
| $\left( \frac{u}{v} \right)' = \frac{u'v - uv'}{v^2} \quad (v \neq 0)$ | $d\left( \frac{u}{v} \right) = \frac{vdu - udv}{v^2} \quad (v \neq 0)$ |