# 第4章 不定积分

原始 PDF 第 197–235 页。

# 第四章 不定积分

在第二章中,我们讨论了如何求一个函数的导函数问题,本章将讨论它的反问题,即要寻求一个可导函数,使它的导函数等于已知函数.这是积分学的基本问题之一.

## 第一节 不定积分的概念与性质

## 一、原函数与不定积分的概念

定义1 如果在区间 $I$ 上, 可导函数 $F(x)$ 的导函数为 $f(x)$, 即对任一 $x \in I$, 都有

$$
F ^ {\prime} (x) = f (x) \text {或} \mathrm{d} F (x) = f (x) \mathrm{d} x,
$$

那么函数  $F(x)$  就称为  $f(x)$  （或  $f(x)\mathrm{d}x$ ）在区间 I 上的一个原函数.

例如, 因  $(\sin x)' = \cos x$ , 故  $\sin x$  是  $\cos x$  的一个原函数.

又如当 $x \in (1, +\infty)$ 时，

$$
\left[ \ln (x + \sqrt {x ^ {2} - 1}) \right] ^ {\prime} = \frac {1}{x + \sqrt {x ^ {2} - 1}} \left(1 + \frac {x}{\sqrt {x ^ {2} - 1}}\right) = \frac {1}{\sqrt {x ^ {2} - 1}},
$$

故 $\ln (x + \sqrt{x^2 - 1})$ 是 $\frac{1}{\sqrt{x^2 - 1}}$ 在区间 $(1, +\infty)$ 内的一个原函数.

关于原函数,我们首先要问:一个函数具备什么条件,能保证它的原函数一定存在?这个问题将在下一章中讨论,这里先介绍一个结论.

原函数存在定理 如果函数 $f(x)$ 在区间 $I$ 上连续, 那么在区间 $I$ 上存在可导函数 $F(x)$, 使对任一 $x \in I$ 都有

$$
F ^ {\prime} (x) = f (x).
$$

简单地说就是:连续函数一定有原函数.

180

---

第一节 不定积分的概念与性质

下面还要说明两点:

第一,如果 $f(x)$ 在区间I上有原函数,即有一个函数 $F(x)$ ,使对任一 $x\in I$ ,都有 $F'(x)=f(x)$ ,那么,对任何常数C,显然也有

$$
\left[ F (x) + C \right] ^ {\prime} = f (x),
$$

即对任何常数 $C$，函数 $F(x) + C$ 也是 $f(x)$ 的原函数。这说明，如果 $f(x)$ 有一个原函数，那么 $f(x)$ 就有无限多个原函数。

第二,如果在区间 I 上  $F(x)$  是  $f(x)$  的一个原函数,那么  $f(x)$  的其他原函数与  $F(x)$  有什么关系?

设  $\Phi(x)$  是  $f(x)$  的另一个原函数, 即对任一  $x \in I$  有

$$
\Phi^ {\prime} (x) = f (x),
$$

于是

$$
\left[ \Phi (x) - F (x) \right] ^ {\prime} = \Phi^ {\prime} (x) - F ^ {\prime} (x) = f (x) - f (x) = 0.
$$

在第三章第一节中已经知道,在一个区间上导数恒为零的函数必为常数,所以

$$
\Phi (x) - F (x) = C _ {0} \quad (C _ {0} \text {为某个常数}).
$$

这表明 $\Phi (x)$ 与 $F(x)$ 只差一个常数.因此，当 $C$ 为任意的常数时，表达式

$$
F (x) + C
$$

就可表示 $f(x)$ 的任意一个原函数.

由以上两点说明,我们引进下述定义:

定义 2 在区间 I 上, 函数  $f(x)$  的带有任意常数项的原函数称为  $f(x)$  （或  $f(x)\mathrm{d}x$ ）在区间 I 上的不定积分, 记作

$$
\int f (x) \mathrm{d} x.
$$

其中记号 $\int$ 称为积分号，$f(x)$ 称为被积函数，$f(x)\mathrm{d}x$ 称为被积表达式，$x$ 称为积分变量.

由此定义及前面的说明可知,如果  $F(x)$  是  $f(x)$  在区间 I 上的一个原函数,那么  $F(x)+C$  就是  $f(x)$  的不定积分,即

$$
\int f (x) \mathrm{d} x = F (x) + C.
$$

因而不定积分 $\int f(x)\mathrm{d}x$ 可以表示 $f(x)$ 的任意一个原函数.

例1 求 $\int x^{2}\mathrm{d}x.$

解 由于 $\left(\frac{x^3}{3}\right)' = x^2$，所以 $\frac{x^3}{3}$ 是 $x^2$ 的一个原函数。因此

图

释疑解难
4-1

图

释疑解难

4-2

181

---

第四章 不定积分

$$
\int x ^ {2} \mathrm{d} x = \frac {x ^ {3}}{3} + C.
$$

例2 求 $\int \frac{1}{x}\mathrm{d}x.$

解 当 $x > 0$ 时, 由于 $(\ln x)' = \frac{1}{x}$, 所以 $\ln x$ 是 $\frac{1}{x}$ 在 $(0, +\infty)$ 内的一个原函数. 因此, 在 $(0, +\infty)$ 内,

$$
\int \frac {1}{x} \mathrm{d} x = \ln x + C.
$$

当 $x < 0$ 时，由于 $[\ln (-x)]' = \frac{1}{-x} (-1) = \frac{1}{x}$，所以 $\ln (-x)$ 是 $\frac{1}{x}$ 在 $(-∞, 0)$ 内的一个原函数。因此，在 $(-∞, 0)$ 内，

$$
\int \frac {1}{x} \mathrm{d} x = \ln (- x) + C.
$$

把在 $x > 0$ 及 $x < 0$ 内的结果合起来，可写作

$$
\int \frac {1}{x} \mathrm{d} x = \ln | x | + C.
$$

例 3 设曲线通过点 $(1,2)$ ，且其上任一点处的切线斜率等于这点横坐标的两倍，求此曲线的方程.

解 设所求的曲线方程为  $y=f(x)$ ，按题设，曲线上任一点  $(x,y)$  处的切线斜率为

$$
\frac {\mathrm{d} y}{\mathrm{d} x} = 2 x,
$$

即 $f(x)$ 是 $2x$ 的一个原函数.

因为 $\int 2x\mathrm{d}x = x^2 +C$ ，故必有某个常数 $C$ 使 $f(x) = x^{2} + C$ ，即曲线方程为 $y = x^{2} + C.$ 因所求曲线通过点(1,2)，故

$$
2 = 1 + C, \quad C = 1.
$$

于是所求曲线方程为

$$
y = x ^ {2} + 1.
$$

函数 $f(x)$ 的原函数的图形称为 $f(x)$ 的积分曲线. 本例即是求函数 y=2x 的通过点(1,2)的那条积分曲线. 显然，这条积分曲线可以由另一条积分曲线（例如 $y=x^{2}$）沿 y 轴方向平移而得（图 4-1）.

例 4 质点以初速度  $v_{0}$  铅直上抛, 不计阻力, 求它的运动规律.

![](../../raw/pages_0193-0224/images/page_198_chart_19.jpg)

<details>
<summary>contour</summary>

| Point | x | y |
| --- | --- | --- |
| Intersection (y=x²+1) | 1 | 2 |
</details>

图4-1

182

---

第一节 不定积分的概念与性质

解 所谓运动规律,是指质点的位置关于时间 t 的函数关系.为表示质点的位置,取坐标系如下:把质点所在的铅直线取作坐标轴,指向朝上,轴与地面的交点取作坐标原点.设质点抛出时刻为 t=0,当 t=0 时质点所在位置的坐标为  $x_{0}$ ,在时刻 t 时坐标为 x (图 4-2),  $x=x(t)$  就是要求的函数.

按导数的物理意义知道，

$$
\frac {\mathrm{d} x}{\mathrm{d} t} = v (t),
$$

![](../../raw/pages_0193-0224/images/page_199_image_4.jpg)

<details>
<summary>text_image</summary>

x
x=x(t)
x₀=x(0)
O
</details>

图4-2

即为质点在时刻 $t$ 时向上运动的速度（如果 $v(t) < 0$ ，那么运动方向实际朝下）.

又知

$$
\frac {\mathrm{d} ^ {2} x}{\mathrm{d} t ^ {2}} = \frac {\mathrm{d} v}{\mathrm{d} t} = a (t),
$$

即为质点在时刻 $t$ 时向上运动的加速度，按题意，有 $a(t) = -g$ ，即

$$
\frac {\mathrm{d} v}{\mathrm{d} t} = - g \quad \text {或} \quad \frac {\mathrm{d} ^ {2} x}{\mathrm{d} t ^ {2}} = - g.
$$

先求 $v(t)$. 由 $\frac{\mathrm{d}v}{\mathrm{d}t} = -g$，即 $v(t)$ 是 $-g$ 的原函数，故

$$
v (t) = \int (- g) \mathrm{d} t = - g t + C _ {1},
$$

由 $v(0) = v_0$ ，得 $v_{0} = C_{1}$ ，于是

$$
v (t) = - g t + v _ {0}.
$$

再求 $x(t)$. 由 $\frac{\mathrm{d}x}{\mathrm{d}t} = v(t)$, 即 $x(t)$ 是 $v(t)$ 的原函数, 故

$$
x (t) = \int v (t) \mathrm{d} t = \int (- g t + v _ {0}) \mathrm{d} t = - \frac {1}{2} g t ^ {2} + v _ {0} t + C _ {2},
$$

由 $x(0) = x_0$ ，得 $x_0 = C_2$ ，于是所求运动规律为

$$
x = - \frac {1}{2} g t ^ {2} + v _ {0} t + x _ {0}, \quad t \in [ 0, T ],
$$

其中 T 表示质点落地的时刻.

从不定积分的定义,即可知下述关系:

由于 $\int f(x)\mathrm{d}x$ 是 $f(x)$ 的原函数，所以

$$
\frac {\mathrm{d}}{\mathrm{d} x} \Big [ \int f (x)   \mathrm{d} x \Big ] = f (x),
$$

或

$$
\mathrm{d} \left[ \int f (x)   \mathrm{d} x \right] = f (x)   \mathrm{d} x; \tag {1-1}
$$

183

---

第四章 不定积分

又由于 $F(x)$ 是 $F'(x)$ 的原函数，所以

$$
\int F ^ {\prime} (x) \mathrm{d} x = F (x) + C,
$$

或记作

$$
\int \mathrm{d} F (x) = F (x) + C. \tag {1-2}
$$

由此可见,微分运算(以记号 d 表示)与求不定积分的运算(简称积分运算,以记号  $\int$  表示)是互逆的.当记号  $\int$  与 d 连在一起时,或者抵消,或者抵消后差一个常数.

## 二、基本积分表

既然积分运算是微分运算的逆运算,那么很自然地可以从导数公式得到相应的积分公式.

例如,因为 $\left(\frac{x^{\mu+1}}{\mu+1}\right)^{\prime}=x^{\mu}$ ，所以 $\frac{x^{\mu+1}}{\mu+1}$ 是 $x^{\mu}$ 的一个原函数,于是

$$
\int x ^ {\mu} \mathrm{d} x = \frac {x ^ {\mu + 1}}{\mu + 1} + C \quad (\mu \neq - 1).
$$

类似地可以得到其他积分公式.下面我们把一些基本的积分公式列成一个表,这个表通常叫做基本积分表.

①  $\int k dx = kx + C$  （k 是常数），
② $\int x^{\mu}\mathrm{d}x = \frac{x^{\mu + 1}}{\mu + 1} +C (\mu \neq -1),$
③ $\int \frac{\mathrm{d}x}{x} = \ln |x| + C,$
④  $\int\frac{dx}{1+x^{2}}=\arctan x+C,$
⑤ $\int \frac{\mathrm{d}x}{\sqrt{1 - x^2}} = \arcsin x + C,$
⑥  $\int\cos x dx=\sin x+C,$
⑦ $\int \sin x\mathrm{d}x = -\cos x + C,$
⑧ $\int \frac{\mathrm{d}x}{\cos^2 x} = \int \sec^2 x\mathrm{d}x = \tan x + C,$
⑨ $\int \frac{\mathrm{d}x}{\sin^2 x} = \int \csc^2 x\mathrm{d}x = -\cot x + C,$
⑩  $\int \sec x \tan x dx = \sec x + C,$

184

---

第一节 不定积分的概念与性质

⑪  $\int \csc x \cot x dx = -\csc x + C,$
⑫  $\int e^{x}dx=e^{x}+C,$
⑬  $\int a^{x}dx=\frac{a^{x}}{\ln a}+C\quad(a>0\text{且}a\neq1).$

以上十三个基本积分公式是求不定积分的基础,必须熟记,下面举几个应用幂函数的积分公式②的例子.

例 5 求  $\int\frac{dx}{x^{3}}$ .

解 $\int \frac{\mathrm{d}x}{x^3} = \int x^{-3}\mathrm{d}x = \frac{x^{-3 + 1}}{-3 + 1} +C = -\frac{1}{2x^2} +C.$

例6 求 $\int x^2\sqrt{x}\mathrm{d}x.$

解 $\int x^{2}\sqrt{x}\mathrm{d}x = \int x^{\frac{5}{2}}\mathrm{d}x = \frac{x^{\frac{5}{2} + 1}}{\frac{5}{2} + 1} +C = \frac{2}{7} x^{\frac{7}{2}} + C = \frac{2}{7} x^{3}\sqrt{x} +C.$

例 7 求  $\int\frac{dx}{x\sqrt[3]{x}}$ .

解 $\int \frac{\mathrm{d}x}{x\sqrt[3]{x}} = \int x^{-\frac{4}{3}}\mathrm{d}x = \frac{x^{-\frac{4}{3} + 1}}{-\frac{4}{3} + 1} +C = -3x^{-\frac{1}{3}} + C = -\frac{3}{\sqrt[3]{x}} +C.$

上面三个例子表明,有时被积函数实际是幂函数,但用分式或根式表示.遇此情形,应先把它化为 $x^{\mu}$ 的形式,然后应用幂函数的积分公式②来求不定积分.

## 三、不定积分的性质

根据不定积分的定义,可以推得它有如下两个性质:

性质1 设函数 $f(x)$ 及 $g(x)$ 的原函数存在, 则

$$
\int [ f (x) + g (x) ] \mathrm{d} x = \int f (x) \mathrm{d} x + \int g (x) \mathrm{d} x. \tag {1-3}
$$

证 将(1-3)式右端求导,得

$$
\left[ \int f (x) \mathrm{d} x + \int g (x) \mathrm{d} x \right] ^ {\prime} = \left[ \int f (x) \mathrm{d} x \right] ^ {\prime} + \left[ \int g (x) \mathrm{d} x \right] ^ {\prime} = f (x) + g (x).
$$

这表示，(1-3)式右端是 $f(x) + g(x)$ 的原函数，又(1-3)式右端有两个积分记号，形式上含两个任意常数，由于任意常数之和仍为任意常数，故实际上含一个任意常数，因此(1-3)式右端是 $f(x) + g(x)$ 的不定积分.

性质 1 对于有限个函数都是成立的.

185

---

第四章 不定积分

类似地可以证明不定积分的第二个性质.

性质2 设函数 $f(x)$ 的原函数存在, $k$ 为非零常数, 则

$$
\int k f (x) \mathrm{d} x = k \int f (x) \mathrm{d} x.
$$

利用基本积分表以及不定积分的这两个性质,可以求出一些简单函数的不定积分.

例8 求 $\int \sqrt{x} (x^2 - 5) \, \mathrm{d}x$.

解 $\int \sqrt{x}(x^2 - 5)\mathrm{d}x = \int (x^{\frac{5}{2}} - 5x^{\frac{1}{2}})\mathrm{d}x = \int x^{\frac{5}{2}}\mathrm{d}x - \int 5x^{\frac{1}{2}}\mathrm{d}x$

$$
= \int x ^ {\frac {5}{2}} \mathrm{d} x - 5 \int x ^ {\frac {1}{2}} \mathrm{d} x = \frac {2}{7} x ^ {\frac {7}{2}} - 5 \cdot \frac {2}{3} x ^ {\frac {3}{2}} + C
$$

$$
= \frac {2}{7} x ^ {3} \sqrt {x} - \frac {1 0}{3} x \sqrt {x} + C.
$$

注意 检验积分结果是否正确,只要对结果求导,看它的导数是否等于被积函数,相等时结果是正确的,否则结果是错误的.如就例8的结果来看,由于

$$
\left(\frac {2}{7} x ^ {3} \sqrt {x} - \frac {1 0}{3} x \sqrt {x} + C\right) ^ {\prime} = \left(\frac {2}{7} x ^ {\frac {7}{2}} - \frac {1 0}{3} x ^ {\frac {3}{2}} + C\right) ^ {\prime} = x ^ {\frac {5}{2}} - 5 x ^ {\frac {1}{2}} = \sqrt {x} (x ^ {2} - 5),
$$

所以结果是正确的.

例9 求 $\int \frac{(x - 1)^3}{x^2}\mathrm{d}x.$

解 $\int \frac{(x - 1)^3}{x^2}\mathrm{d}x = \int \frac{x^3 - 3x^2 + 3x - 1}{x^2}\mathrm{d}x = \int \left(x - 3 + \frac{3}{x} -\frac{1}{x^2}\right)\mathrm{d}x$

$$
= \int x \mathrm{d} x - 3 \int \mathrm{d} x + 3 \int \frac {\mathrm{d} x}{x} - \int \frac {\mathrm{d} x}{x ^ {2}} = \frac {x ^ {2}}{2} - 3 x + 3 \ln | x | + \frac {1}{x} + C.
$$

例10 求 $\int (\mathrm{e}^x - 3\cos x)\mathrm{d}x.$

解 $\int (\mathrm{e}^x - 3\cos x)\mathrm{d}x = \int \mathrm{e}^x\mathrm{d}x - 3\int \cos x\mathrm{d}x = \mathrm{e}^x - 3\sin x + C.$

例11 求 $\int 2^{x}\mathrm{e}^{x}\mathrm{d}x.$

解 因为

$$
2 ^ {x} \mathrm{e} ^ {x} = (2 \mathrm{e}) ^ {x},
$$

所以可把 2e 看作 a, 并利用积分公式⑬, 便得

$$
\int 2 ^ {x} \mathrm{e} ^ {x} \mathrm{d} x = \int (2 \mathrm{e}) ^ {x} \mathrm{d} x = \frac {(2 \mathrm{e}) ^ {x}}{\ln (2 \mathrm{e})} + C = \frac {2 ^ {x} \mathrm{e} ^ {x}}{1 + \ln 2} + C.
$$

186

---

第一节 不定积分的概念与性质

例12 求 $\int \tan^2 x\mathrm{d}x.$

解 基本积分表中没有这种类型的积分,先利用三角恒等式化成表中所列类型的积分,然后再逐项求积分.

$$
\int \tan^ {2} x \mathrm{d} x = \int (\sec^ {2} x - 1) \mathrm{d} x = \int \sec^ {2} x \mathrm{d} x - \int \mathrm{d} x = \tan x - x + C.
$$

例 13 求  $\int\sin^{2}\frac{x}{2}dx.$

解 基本积分表中也没有这种类型的积分, 同上例一样, 可以先利用三角恒等式变形, 然后再逐项求积分.

$$
\begin{array}{l} \int \sin^ {2} \frac {x}{2} \mathrm{d} x = \int \frac {1}{2} (1 - \cos x) \mathrm{d} x = \frac {1}{2} \int (1 - \cos x) \mathrm{d} x \\ = \frac {1}{2} \left(\int \mathrm{d} x - \int \cos x \mathrm{d} x\right) = \frac {1}{2} (x - \sin x) + C. \\ \end{array}
$$

例14 求 $\int \frac{1}{\sin^2\frac{x}{2}\cos^2\frac{x}{2}}\mathrm{d}x.$

解 同上例一样,先利用三角恒等式变形,然后再求积分.

$$
\int \frac {1}{\sin^ {2} \frac {x}{2} \cos^ {2} \frac {x}{2}} \mathrm{d} x = \int \frac {1}{\left(\frac {\sin x}{2}\right) ^ {2}} \mathrm{d} x = 4 \int \csc^ {2} x \mathrm{d} x = - 4 \cot x + C.
$$

例15 求 $\int \frac{2x^4 + x^2 + 3}{x^2 + 1}\mathrm{d}x.$

解 被积函数的分子和分母都是多项式,通过多项式的除法,可以把它化成基本积分表中所列类型的积分,然后再逐项求积分.

$$
\begin{array}{l} \int \frac {2 x ^ {4} + x ^ {2} + 3}{x ^ {2} + 1} \mathrm{d} x = \int \left(2 x ^ {2} - 1 + \frac {4}{x ^ {2} + 1}\right) \mathrm{d} x \\ = 2 \int x ^ {2} \mathrm{d} x - \int 1 \mathrm{d} x + 4 \int \frac {1}{x ^ {2} + 1} \mathrm{d} x = \frac {2}{3} x ^ {3} - x + 4 \arctan x + C. \\ \end{array}
$$

## 习题4-1

1. 利用求导运算验证下列等式:

(1) $\int \frac{1}{\sqrt{x^2 + 1}}\mathrm{d}x = \ln (x + \sqrt{x^2 + 1}) + C;$

(2) $\int \frac{1}{x^2\sqrt{x^2 - 1}}\mathrm{d}x = \frac{\sqrt{x^2 - 1}}{x} +C;$

187

---

第四章 不定积分

(3) $\int \frac{2x}{(x^2 + 1)(x + 1)^2} \, \mathrm{d}x = \arctan x + \frac{1}{x + 1} + C;$
(4) $\int \sec x\mathrm{d}x = \ln |\tan x + \sec x| + C;$
(5) $\int x\cos x\mathrm{d}x = x\sin x + \cos x + C;$
(6) $\int \mathrm{e}^{x}\sin x\mathrm{d}x = \frac{1}{2}\mathrm{e}^{x}(\sin x - \cos x) + C.$

2. 求下列不定积分:

(1) $\int \frac{\mathrm{d}x}{x^2}$;

(2) $\int x\sqrt{x}\mathrm{d}x;$

(3) $\int \frac{\mathrm{d}x}{\sqrt{x}};$

(4) $\int x^{2\sqrt[3]{x}}dx;$

(5) $\int \frac{\mathrm{d}x}{x^2\sqrt{x}};$

(6) $\int \sqrt[m]{x^n} \, \mathrm{d}x$;

(7) $\int5x^{3}dx;$

(8) $\int (x^2 - 3x + 2)\mathrm{d}x$;

(9) $\int\frac{dh}{\sqrt{2gh}}$  (g 是常数);

(10) $\int (x^2 + 1)^2 \mathrm{d}x$;

(11) $\int (\sqrt{x} + 1)(\sqrt{x^3} - 1)\mathrm{d}x;$

(12) $\int \frac{(1 - x)^2}{\sqrt{x}}\mathrm{d}x;$

(13) $\int \left(2\mathrm{e}^{x} + \frac{3}{x}\right)\mathrm{d}x;$

(14) $\int \left(\frac{3}{1 + x^2} -\frac{2}{\sqrt{1 - x^2}}\right)\mathrm{d}x;$

(15) $\int \mathrm{e}^{x}\left(1 - \frac{\mathrm{e}^{-x}}{\sqrt{x}}\right)\mathrm{d}x;$

(16) $\int 3^{x} \mathrm{e}^{x} \mathrm{d}x$;

(17) $\int \frac{2 \cdot 3^x - 5 \cdot 2^x}{3^x} \, \mathrm{d}x$;

(18) $\int \sec x (\sec x - \tan x) \, \mathrm{d}x$;

(19) $\int \cos^2\frac{x}{2}\mathrm{d}x;$

(20) $\int\frac{dx}{1+\cos2x};$

(21) $\int \frac{\cos 2x}{\cos x - \sin x} \, \mathrm{d}x;$

(22) $\int \frac{\cos 2x}{\cos^2 x \sin^2 x} \, \mathrm{d}x;$

(23) $\int\cot^{2}xdx;$

(24) $\int \cos \theta (\tan \theta +\sec \theta)\mathrm{d}\theta ;$

(25) $\int\frac{x^{2}}{x^{2}+1}dx;$

(26) $\int \frac{3x^4 + 2x^2}{x^2 + 1}\mathrm{d}x.$

3. 含有未知函数的导数的方程称为微分方程, 例如方程 $\frac{\mathrm{dy}}{\mathrm{dx}} = f(x)$, 其中 $\frac{\mathrm{dy}}{\mathrm{dx}}$ 为未知函数的导数, $f(x)$ 为已知函数. 如果将函数 $y = \varphi(x)$ 代入微分方程, 使微分方程成为恒等式, 那么函数 $y = \varphi(x)$ 就称为该微分方程的解. 求下列微分方程满足所给条件的解:

(1) $\frac{\mathrm{d}y}{\mathrm{d}x} = (x - 2)^2, y|_{x = 2} = 0;$
(2) $\frac{\mathrm{d}^2x}{\mathrm{d}t^2} = \frac{2}{t^3}, \quad \frac{\mathrm{d}x}{\mathrm{d}t}\bigg|_{t=1} = 1, x\bigg|_{t=1} = 1.$

4. 汽车以  $20 \, m/s$  的速度沿直线行驶, 刹车后匀减速行驶了  $50 \, m$  停住, 求刹车加速度. 可执行下列步骤:

（1）求微分方程 $\frac{\mathrm{d}^2s}{\mathrm{d}t^2} = -k$ 满足条件 $\frac{\mathrm{ds}}{\mathrm{dt}}\Big|_{t = 0} = 20$ 及 $s\big|_{t = 0} = 0$ 的解；
(2) 求使 $\frac{ds}{dt}=0$ 的 t 值及相应的 s 值；
(3) 求使 s=50 的 k 值.

5. 一曲线通过点 $(e^2,3)$, 且在任一点处的切线的斜率等于该点横坐标的倒数, 求该曲线的方程.

188

---

第二节 换元积分法

6. 一物体沿直线由静止开始运动, 经 $t \mathrm{~s}$ 后的速度是 $3 t^{2} \mathrm{~m} / \mathrm{s}$, 问

(1) 3 s 后物体离开出发点的距离是多少?

(2) 物体走完 360 m 需要多少时间?

7. 证明 $\arcsin(2x-1)$, $\arccos(1-2x)$ 和 $2\arctan\sqrt{\frac{x}{1-x}}$ 都是 $\frac{1}{\sqrt{x-x^2}}$ 的原函数.

## 第二节 换元积分法

利用基本积分表与积分的性质,所能计算的不定积分是非常有限的.因此,有必要进一步来研究不定积分的求法.本节把复合函数的微分法反过来用于求不定积分,利用中间变量的代换,得到复合函数的积分法,称为换元积分法,简称换元法.换元法通常分成两类,下面先讲第一类换元法.

## 一、第一类换元法

设 $f(u)$ 具有原函数 $F(u)$，即

$$
F ^ {\prime} (u) = f (u), \quad \int f (u) \mathrm{d} u = F (u) + C.
$$

如果 u 是中间变量:  $u = \varphi(x)$ ，且设  $\varphi(x)$  可微，那么，根据复合函数微分法，有

$$
\mathrm{d} F [ \varphi (x) ] = f [ \varphi (x) ] \varphi^ {\prime} (x) \mathrm{d} x,
$$

从而根据不定积分的定义就得

$$
\int f [ \varphi (x) ] \varphi^ {\prime} (x) \mathrm{d} x = F [ \varphi (x) ] + C = \left[ \int f (u) \mathrm{d} u \right] _ {u = \varphi (x)}.
$$

于是有下述定理:

定理1 设 $f(u)$ 具有原函数, $u = \varphi (x)$ 可导, 则有换元公式

$$
\int f [ \varphi (x) ] \varphi^ {\prime} (x) \mathrm{d} x = \left[ \int f (u) \mathrm{d} u \right] _ {u = \varphi (x)}. \tag {2-1}
$$

由此定理可见,虽然  $\int f[\varphi(x)]\varphi'(x)\mathrm{d}x$  是一个整体的记号,但从形式上看,被积表达式中的 dx 也可当作变量 x 的微分来对待,从而微分等式  $\varphi'(x)\mathrm{d}x=\mathrm{d}u$  可以方便地应用到被积表达式中来,我们在上节第一目中已经这样用了,那里把积分  $\int F'(x)\mathrm{d}x$  记作  $\int\mathrm{d}F(x)$ , 就是按微分  $F'(x)\mathrm{d}x=\mathrm{d}F(x)$ , 把被积表达式  $F'(x)\mathrm{d}x$  记作  $\mathrm{d}F(x)$ .

如何应用公式(2-1)来求不定积分？设要求 $\int g(x)\mathrm{d}x$ ，如果函数 $g(x)$ 可以化为$g(x) = f[\varphi (x)]\varphi '(x)$ 的形式，那么

189

---

第四章 不定积分

$$
\int g (x) \mathrm{d} x = \int f [ \varphi (x) ] \varphi^ {\prime} (x) \mathrm{d} x = \left[ \int f (u) \mathrm{d} u \right] _ {u = \varphi (x)},
$$

这样, 函数 $g(x)$ 的积分即转化为函数 $f(u)$ 的积分. 如果能求得 $f(u)$ 的原函数, 那么也就得到了 $g(x)$ 的原函数.

例1 求 $\int 2\cos 2x\mathrm{d}x.$

解 被积函数中, $\cos 2x$ 是一个由 $\cos 2x = \cos u, u = 2x$ 复合而成的复合函数, 常数因子恰好是中间变量 u 的导数. 因此, 作变换 u = 2x, 便有

$$
\int 2 \cos 2 x \mathrm{d} x = \int \cos 2 x \cdot 2 \mathrm{d} x = \int \cos 2 x \cdot (2 x) ^ {\prime} \mathrm{d} x = \int \cos u \mathrm{d} u = \sin u + C,
$$

再以 u=2x 代入, 即得

$$
\int 2 \cos 2 x \mathrm{d} x = \sin 2 x + C.
$$

例 2 求  $\int\frac{1}{3+2x}dx.$

解 被积函数 $\frac{1}{3+2x}=\frac{1}{u},u=3+2x.$ 这里缺少 $\frac{du}{dx}=2$ 这样一个因子,但由于 $\frac{du}{dx}$ 是个常数,故可改变系数凑出这个因子:

$$
\frac {1}{3 + 2 x} = \frac {1}{2} \cdot \frac {1}{3 + 2 x} \cdot 2 = \frac {1}{2} \cdot \frac {1}{3 + 2 x} (3 + 2 x) ^ {\prime},
$$

从而令 $u = 3 + 2x$ ，便有

$$
\begin{array}{l} \int \frac {1}{3 + 2 x} \mathrm{d} x = \int \frac {1}{2} \cdot \frac {1}{3 + 2 x} (3 + 2 x) ^ {\prime} \mathrm{d} x = \int \frac {1}{2} \cdot \frac {1}{u} \mathrm{d} u \\ = \frac {1}{2} \ln | u | + C = \frac {1}{2} \ln | 3 + 2 x | + C. \\ \end{array}
$$

一般地，对于积分 $\int f(ax + b)\mathrm{d}x$ （ $a\neq 0$ ），总可作变换 $u = ax + b$ ，把它化为

$$
\int f (a x + b) \mathrm{d} x = \int \frac {1}{a} f (a x + b) \mathrm{d} (a x + b) = \frac {1}{a} \left[ \int f (u) \mathrm{d} u \right] _ {u = a x + b},
$$

例3 求 $\int \frac{x^2}{(x + 2)^3}\mathrm{d}x.$

解 令 $u = x + 2$ ，则 $x = u - 2, \mathrm{d}x = \mathrm{d}u,$ 于是

$$
\begin{array}{l} \int \frac {x ^ {2}}{(x + 2) ^ {3}} \mathrm{d} x = \int \frac {(u - 2) ^ {2}}{u ^ {3}} \mathrm{d} u = \int (u ^ {2} - 4 u + 4) u ^ {- 3} \mathrm{d} u \\ = \int (u ^ {- 1} - 4 u ^ {- 2} + 4 u ^ {- 3}) \mathrm{d} u = \ln | u | + 4 u ^ {- 1} - 2 u ^ {- 2} + C \\ = \ln | x + 2 | + \frac {4}{x + 2} - \frac {2}{(x + 2) ^ {2}} + C. \\ \end{array}
$$

190

---

第二节 换元积分法

例4 求 $\int 2x\mathrm{e}^{x^2}\mathrm{d}x.$

解 被积函数中的一个因子为 $\mathrm{e}^{x^2} = \mathrm{e}^u, u = x^2$，剩下的因子 $2x$ 恰好是中间变量 $u = x^2$ 的导数，于是有

$$
\int 2 x \mathrm{e} ^ {x ^ {2}} \mathrm{d} x = \int \mathrm{e} ^ {x ^ {2}} \mathrm{d} (x ^ {2}) = \int \cdot \mathrm{e} ^ {u} \mathrm{d} u = \mathrm{e} ^ {u} + C = \mathrm{e} ^ {x ^ {2}} + C.
$$

例5 求 $\int x\sqrt{1 - x^2}\mathrm{d}x.$

解 设 $u = 1 - x^2$，则 $\mathrm{du} = -2x\mathrm{dx}$，即 $-\frac{1}{2}\mathrm{du} = x\mathrm{dx}$，因此，

$$
\int x \sqrt {1 - x ^ {2}} \mathrm{d} x = \int u ^ {\frac {1}{2}} \cdot \left(- \frac {1}{2}\right) \mathrm{d} u = - \frac {1}{2} \frac {u ^ {\frac {3}{2}}}{\frac {3}{2}} + C = - \frac {1}{3} u ^ {\frac {3}{2}} + C = - \frac {1}{3} (1 - x ^ {2}) ^ {\frac {3}{2}} + C.
$$

在对变量代换比较熟练以后,就不一定写出中间变量 u.

例6 求 $\int \frac{1}{a^2 + x^2} \, \mathrm{d}x (a \neq 0)$.

解 $\int \frac{1}{a^2 + x^2}\mathrm{d}x = \int \frac{1}{a^2}\cdot \frac{1}{1 + \left(\frac{x}{a}\right)^2}\mathrm{d}x = \frac{1}{a}\int \frac{1}{1 + \left(\frac{x}{a}\right)^2}\mathrm{d}\frac{x}{a} = \frac{1}{a}\arctan \frac{x}{a} +C.$

在上例中,我们实际上已经用了变量代换  $u=\frac{x}{a}$ ，并在求出积分  $\frac{1}{a}\int\frac{1}{1+u^{2}}du$  之后，代回了原积分变量 x，只是没有把这些步骤写出来而已.

例7 求 $\int \frac{\mathrm{d}x}{\sqrt{a^2 - x^2}} (a > 0)$.

解 $\int \frac{\mathrm{d}x}{\sqrt{a^2 - x^2}} = \int \frac{1}{a}\cdot \frac{\mathrm{d}x}{\sqrt{1 - \left(\frac{x}{a}\right)^2}} = \int \frac{\mathrm{d}\frac{x}{a}}{\sqrt{1 - \left(\frac{x}{a}\right)^2}} = \arcsin \frac{x}{a} +C.$

例8 求 $\int \frac{1}{x^2 - a^2}\mathrm{d}x$ （ $a\neq 0$ ）.

解 由于

$$
\frac {1}{x ^ {2} - a ^ {2}} = \frac {1}{2 a} \left(\frac {1}{x - a} - \frac {1}{x + a}\right),
$$

所以

191

---

第四章 不定积分

$$
\begin{array}{l} \int \frac {1}{x ^ {2} - a ^ {2}} \mathrm{d} x = \frac {1}{2 a} \int \left(\frac {1}{x - a} - \frac {1}{x + a}\right) \mathrm{d} x = \frac {1}{2 a} \left(\int \frac {1}{x - a} \mathrm{d} x - \int \frac {1}{x + a} \mathrm{d} x\right) \\ = \frac {1}{2 a} \left[ \int \frac {1}{x - a} \mathrm{d} (x - a) - \int \frac {1}{x + a} \mathrm{d} (x + a) \right] \\ = \frac {1}{2 a} (\ln | x - a | - \ln | x + a |) + C = \frac {1}{2 a} \ln \left| \frac {x - a}{x + a} \right| + C. \\ \end{array}
$$

例9 求 $\int \frac{\mathrm{d}x}{x(1 + 2\ln x)}.$

解 $\int \frac{\mathrm{d}x}{x(1 + 2\ln x)} = \int \frac{\mathrm{d}(\ln x)}{1 + 2\ln x} = \frac{1}{2}\int \frac{\mathrm{d}(1 + 2\ln x)}{1 + 2\ln x} = \frac{1}{2}\ln |1 + 2\ln x| + C.$

例 10 求  $\int\frac{e^{3/\sqrt{x}}}{\sqrt{x}}dx.$

解 由于 $\mathrm{d}\sqrt{x} = \frac{1}{2}\frac{\mathrm{d}x}{\sqrt{x}}$ ，因此，

$$
\int \frac {\mathrm{e} ^ {3 \sqrt {x}}}{\sqrt {x}} \mathrm{d} x = 2 \int \mathrm{e} ^ {3 \sqrt {x}} \mathrm{d} \sqrt {x} = \frac {2}{3} \int \mathrm{e} ^ {3 \sqrt {x}} \mathrm{d} (3 \sqrt {x}) = \frac {2}{3} \mathrm{e} ^ {3 \sqrt {x}} + C.
$$

下面再举一些积分的例子,它们的被积函数中含有三角函数,在计算这种积分的过程中,往往要用到一些三角恒等式.

例 11 求  $\int\sin^{3}x dx$ .

解 $\int \sin^3 x\mathrm{d}x = \int \sin^2 x\sin x\mathrm{d}x = -\int (1 - \cos^2 x)\mathrm{d}(\cos x) = -\cos x + \frac{1}{3}\cos^3 x + C.$

例12 求 $\int \sin^2 x\cos^5 x\mathrm{d}x.$

$$
\begin{array}{l} = \int \left(\sin^ {2} x - 2 \sin^ {4} x + \sin^ {6} x\right) \mathrm{d} (\sin x) \\ = \frac {1}{3} \sin^ {3} x - \frac {2}{5} \sin^ {5} x + \frac {1}{7} \sin^ {7} x + C. \\ \end{array}
$$

解 $\int \sin^2 x\cos^5 x\mathrm{d}x = \int \sin^2 x\cos^4 x\cos x\mathrm{d}x = \int \sin^2 x(1 - \sin^2 x)^2\mathrm{d}(\sin x)$

一般地,对于  $\sin^{2k+1}x\cos^{n}x$  或  $\sin^{n}x\cos^{2k+1}x$  （其中  $k\in N$ ）型函数的积分,总可依次作变换  $u=\cos x$  或  $u=\sin x$ ,求得结果.

例13 求 $\int \tan x\mathrm{d}x.$

192

---

第二节 换元积分法

解 $\int \tan x\mathrm{d}x = \int \frac{\sin x}{\cos x}\mathrm{d}x = -\int \frac{1}{\cos x}\mathrm{d}(\cos x) = -\ln |\cos x| + C.$

类似地可得

$$
\int \cot x \mathrm{d} x = \ln | \sin x | + C.
$$

例14 求 $\int \cos^2 x\mathrm{d}x.$

解 $\int \cos^2 x\mathrm{d}x = \int \frac{1 + \cos 2x}{2}\mathrm{d}x = \frac{1}{2}\left(\int \mathrm{d}x + \int \cos 2x\mathrm{d}x\right)$

$$
= \frac {1}{2} \int \mathrm{d} x + \frac {1}{4} \int \cos 2 x \mathrm{d} (2 x) = \frac {x}{2} + \frac {\sin 2 x}{4} + C.
$$

例15 求 $\int \sin^2 x\cos^4 x\mathrm{d}x$

$$
\begin{array}{l} = \frac {1}{8} \int (1 + \cos 2 x - \cos^ {2} 2 x - \cos^ {3} 2 x) \mathrm{d} x \\ = \frac {1}{8} \int (\cos 2 x - \cos^ {3} 2 x) \mathrm{d} x + \frac {1}{8} \int (1 - \cos^ {2} 2 x) \mathrm{d} x \\ = \frac {1}{8} \int \sin^ {2} 2 x \cdot \frac {1}{2} \mathrm{d} (\sin 2 x) + \frac {1}{8} \int \frac {1}{2} (1 - \cos 4 x) \mathrm{d} x \\ = \frac {1}{4 8} \sin^ {3} 2 x + \frac {x}{1 6} - \frac {1}{6 4} \sin 4 x + C. \\ \end{array}
$$

解 $\int \sin^2 x\cos^4 x\mathrm{d}x = \frac{1}{8}\int (1 - \cos 2x)(1 + \cos 2x)^2\mathrm{d}x$

一般地, 对于  $\sin^{2k}x\cos^{2l}x\quad(k,l\in\mathbb{N})$  型函数, 总可利用三角恒等式:  $\sin^{2}x=\frac{1}{2}(1-\cos2x),\cos^{2}x=\frac{1}{2}(1+\cos2x)$  化成  $\cos2x$  的多项式, 然后采用例 15 中所用的方法求得积分的结果.

例 16 求  $\int \sec^{6}x dx$ .

解 $\int \sec^6 x\mathrm{d}x = \int (\sec^2 x)^2\sec^2 x\mathrm{d}x = \int (1 + \tan^2 x)^2\mathrm{d}(\tan x)$

$$
= \int (1 + 2 \tan^ {2} x + \tan^ {4} x) \mathrm{d} (\tan x) = \tan x + \frac {2}{3} \tan^ {3} x + \frac {1}{5} \tan^ {5} x + C.
$$

例 17 求  $\int\tan^{5}x\sec^{3}x dx.$

解 $\int \tan^5 x\sec^3 x\mathrm{d}x$

193

---

第四章 不定积分

$$
\begin{array}{l} = \int \tan^ {4} x \sec^ {2} x \sec x \tan x \mathrm{d} x = \int (\sec^ {2} x - 1) ^ {2} \sec^ {2} x \mathrm{d} (\sec x) \\ = \int (\sec^ {6} x - 2 \sec^ {4} x + \sec^ {2} x) \mathrm{d} (\sec x) = \frac {1}{7} \sec^ {7} x - \frac {2}{5} \sec^ {5} x + \frac {1}{3} \sec^ {3} x + C. \\ \end{array}
$$

一般地, 对于  $\tan^{n}x\sec^{2k}x$  或  $\tan^{2k-1}x\sec^{n}x$  ( $n, k \in N_{+}$ ) 型函数的积分, 可依次作变换  $u = \tan x$  或  $u = \sec x$ , 求得结果.

例 18 求  $\int \csc x dx.$

解 $\int \csc x\mathrm{d}x = \int \frac{\mathrm{d}x}{\sin x} = \int \frac{\mathrm{d}x}{2\sin\frac{x}{2}\cos\frac{x}{2}}$

$$
= \int \frac {\mathrm{d} \left(\frac {x}{2}\right)}{\tan \frac {x}{2} \cos^ {2} \frac {x}{2}} = \int \frac {\mathrm{d} \left(\tan \frac {x}{2}\right)}{\tan \frac {x}{2}} = \ln \left| \tan \frac {x}{2} \right| + C.
$$

因为

$$
\tan \frac {x}{2} = \frac {\sin \frac {x}{2}}{\cos \frac {x}{2}} = \frac {2 \sin^ {2} \frac {x}{2}}{\sin x} = \frac {1 - \cos x}{\sin x} = \csc x - \cot x,
$$

所以上述不定积分又可表示为

$$
\int \csc x \mathrm{d} x = \ln | \csc x - \cot x | + C.
$$

例 19 求  $\int \sec x dx$ .

解 利用上例的结果,有

$$
\begin{array}{l} \int \sec x \mathrm{d} x = \int \csc \left(x + \frac {\pi}{2}\right) \mathrm{d} \left(x + \frac {\pi}{2}\right) \\ = \ln \left| \csc \left(x + \frac {\pi}{2}\right) - \cot \left(x + \frac {\pi}{2}\right) \right| + C = \ln | \sec x + \tan x | + C. \\ \end{array}
$$

例 20 求  $\int \cos 3x \cos 2x dx$ .

解 利用三角函数的积化和差公式

$$
\cos A \cos B = \frac {1}{2} [ \cos (A - B) + \cos (A + B) ]
$$

194

---

第二节 换元积分法

得

$$
\cos 3 x \cos 2 x = \frac {1}{2} (\cos x + \cos 5 x),
$$

于是

$$
\begin{array}{l} \int \cos 3 x \cos 2 x \mathrm{d} x = \frac {1}{2} \int (\cos x + \cos 5 x) \mathrm{d} x \\ = \frac {1}{2} \left[ \int \cos x \mathrm{d} x + \frac {1}{5} \int \cos 5 x \mathrm{d} (5 x) \right] \\ = \frac {1}{2} \sin x + \frac {1}{1 0} \sin 5 x + C. \\ \end{array}
$$

上面所举的例子,可以使我们认识到公式(2-1)在求不定积分中所起的作用.像复合函数的求导法则在微分学中一样,公式(2-1)在积分学中也是经常使用的.但利用公式(2-1)来求不定积分,一般却比利用复合函数的求导法则求函数的导数要来得困难,因为其中需要一定的技巧,而且如何适当地选择变量代换 $u=\varphi(x)$ 没有一般规律可循,因此要掌握换元法,除了熟悉一些典型的例子外,还要做较多的练习才行.

上述各例用的都是第一类换元法, 即形如  $u = \varphi(x)$  的变量代换. 下面介绍另一种形式的变量代换  $x = \psi(t)$ , 即所谓第二类换元法.

## 二、第二类换元法

上面介绍的第一类换元法是通过变量代换 $u = \varphi(x)$，将积分 $\int f[\varphi(x)] \cdot \varphi'(x) \, \mathrm{d}x$ 化为积分 $\int f(u) \, \mathrm{d}u$.

下面将介绍的第二类换元法是:适当地选择变量代换  $x=\psi(t)$ ，将积分  $\int f(x)\mathrm{d}x$  化为积分  $\int f[\psi(t)]\psi'(t)\mathrm{d}t$ 。这是另一种形式的变量代换，换元公式可表达为

$$
\int f (x) \mathrm{d} x = \int f [ \psi (t) ] \psi^ {\prime} (t) \mathrm{d} t.
$$

这公式的成立是需要一定条件的. 首先, 等式右边的不定积分要存在, 即 $f[\psi(t)]\psi'(t)$ 有原函数; 其次, $\int f[\psi(t)]\psi'(t)\mathrm{d}t$ 求出后必须用 $x = \psi(t)$ 的反函数 $t = \psi^{-1}(x)$ 代回去, 为了保证这反函数存在而且是可导的, 我们假定直接函数 $x = \psi(t)$ 在 $t$ 的某一个区间 (这区间和所考虑的 $x$ 的积分区间相对应) 上是单调的、可导的, 并且 $\psi'(t) \neq 0$.

195

---

第四章 不定积分

归纳上述,我们给出下面的定理:

定理2 设 $x = \psi(t)$ 是单调的可导函数，并且 $\psi'(t) \neq 0$. 又设 $f[\psi(t)]\psi'(t)$ 具有原函数，则有换元公式

$$
\int f (x) \mathrm{d} x = \left[ \int f [ \psi (t) ] \psi^ {\prime} (t) \mathrm{d} t \right] _ {t = \psi^ {- 1} (x)}, \tag {2-2}
$$

其中 $\psi^{-1}(x)$ 是 $x = \psi (t)$ 的反函数.

证 设 $f[\psi(t)]\psi'(t)$ 的原函数为 $\Phi(t)$, 记 $\Phi[\psi^{-1}(x)] = F(x)$, 利用复合函数及反函数的求导法则, 得到

$$
F ^ {\prime} (x) = \frac {\mathrm{d} \Phi}{\mathrm{d} t} \cdot \frac {\mathrm{d} t}{\mathrm{d} x} = f [ \psi (t) ] \psi^ {\prime} (t) \cdot \frac {1}{\psi^ {\prime} (t)} = f [ \psi (t) ] = f (x),
$$

即 $F(x)$ 是 $f(x)$ 的原函数.所以有

$$
\int f (x) \mathrm{d} x = F (x) + C = \Phi [ \psi^ {- 1} (x) ] + C = \left[ \int f [ \psi (t) ] \psi^ {\prime} (t) \mathrm{d} t \right] _ {t = \psi^ {- 1} (x)},
$$

这就证明了公式(2-2).

下面举例说明换元公式(2-2)的应用.

例 21 求  $\int\sqrt{a^{2}-x^{2}}dx$  (a>0).

解 求这个积分的困难在于有根式 $\sqrt{a^2 - x^2}$, 但我们可以利用三角函数公式

$$
\sin^ {2} t + \cos^ {2} t = 1
$$

来化去根式.

设 $x = a\sin t, -\frac{\pi}{2} < t < \frac{\pi}{2}$，则 $\sqrt{a^2 - x^2} = \sqrt{a^2 - a^2\sin^2t} = a\cos t, \mathrm{d}x = a\cos t\mathrm{d}t$，于是根式化成了三角式，所求积分化为

$$
\int \sqrt {a ^ {2} - x ^ {2}} \mathrm{d} x = \int a \cos t \cdot a \cos t \mathrm{d} t = a ^ {2} \int \cos^ {2} t \mathrm{d} t.
$$

利用例14的结果得

$$
\int \sqrt {a ^ {2} - x ^ {2}} \mathrm{d} x = a ^ {2} \left(\frac {t}{2} + \frac {\sin 2 t}{4}\right) + C = \frac {a ^ {2}}{2} t + \frac {a ^ {2}}{2} \sin t \cos t + C.
$$

由于 $x = a\sin t, -\frac{\pi}{2} < t < \frac{\pi}{2}$，所以

$$
t = \arcsin \frac {x}{a},
$$

196

---

第二节 换元积分法

$$
\cos t = \sqrt {1 - \sin^ {2} t} = \sqrt {1 - \left(\frac {x}{a}\right) ^ {2}} = \frac {\sqrt {a ^ {2} - x ^ {2}}}{a},
$$

于是所求积分为

$$
\int \sqrt {a ^ {2} - x ^ {2}} \mathrm{d} x = \frac {a ^ {2}}{2} \arcsin \frac {x}{a} + \frac {1}{2} x \sqrt {a ^ {2} - x ^ {2}} + C.
$$

例22 求 $\int \frac{\mathrm{d}x}{\sqrt{x^2 + a^2}} (a > 0)$

解 和上例类似,可以利用三角函数公式

$$
1 + \tan^ {2} t = \sec^ {2} t
$$

来化去根式.

设 $x = a\tan t\left(-\frac{\pi}{2} <  t <   \frac{\pi}{2}\right)$ ，则

$$
\sqrt {x ^ {2} + a ^ {2}} = \sqrt {a ^ {2} \tan^ {2} t + a ^ {2}} = a \sqrt {\tan^ {2} t + 1} = a \sec t, \quad \mathrm{d} x = a \sec^ {2} t \mathrm{d} t,
$$

于是

$$
\int \frac {\mathrm{d} x}{\sqrt {x ^ {2} + a ^ {2}}} = \int \frac {a \sec^ {2} t}{a \sec t} \mathrm{d} t = \int \sec t \mathrm{d} t.
$$

利用例 19 的结果得

$$
\int \frac {\mathrm{d} x}{\sqrt {x ^ {2} + a ^ {2}}} = \ln | \sec t + \tan t | + C.
$$

为了要把 $\sec t$ 及 $\tan t$ 换成 $x$ 的函数, 可以根据 $\tan t = \frac{x}{a}$ 作辅助三角形(图4-3), 便有

$$
\sec t = \frac {\sqrt {x ^ {2} + a ^ {2}}}{a},
$$

且  $\sec t + \tan t > 0$ ，因此，

$$
\begin{array}{l} \int \frac {\mathrm{d} x}{\sqrt {x ^ {2} + a ^ {2}}} = \ln \left(\frac {x}{a} + \frac {\sqrt {x ^ {2} + a ^ {2}}}{a}\right) + C \\ = \ln (x + \sqrt {x ^ {2} + a ^ {2}}) + C _ {1}, \\ \end{array}
$$

![](../../raw/pages_0193-0224/images/page_213_image_18.jpg)

<details>
<summary>text_image</summary>

√x²+a²
x
t
a
</details>

图4-3

其中 $C_1 = C - \ln a$.

例23 求 $\int \frac{\mathrm{d}x}{\sqrt{x^2 - a^2}} (a > 0)$.

197

---

第四章 不定积分

解 和以上两例类似,可以利用公式

$$
\sec^ {2} t - 1 = \tan^ {2} t
$$

来化去根式. 注意到被积函数的定义域是 x > a 和 x < -a 两个区间, 我们在两个区间内分别求不定积分.

当 $x > a$ 时，设 $x = a\sec t\left(0 < t < \frac{\pi}{2}\right)$，则

$$
\sqrt {x ^ {2} - a ^ {2}} = \sqrt {a ^ {2} \sec^ {2} t - a ^ {2}} = a \sqrt {\sec^ {2} t - 1} = a \tan t,
$$

$$
\mathrm{d} x = a \sec t \tan t \mathrm{d} t,
$$

于是

$$
\int \frac {\mathrm{d} x}{\sqrt {x ^ {2} - a ^ {2}}} = \int \frac {a \sec t \tan t}{a \tan t} \mathrm{d} t = \int \sec t \mathrm{d} t = \ln (\sec t + \tan t) + C.
$$

为了把 $\sec t$ 及 $\tan t$ 换成 $x$ 的函数, 我们根据 $\sec t = \frac{x}{a}$ 作辅助三角形(图4-4), 得到

$$
\tan t = \frac {\sqrt {x ^ {2} - a ^ {2}}}{a},
$$

![](../../raw/pages_0193-0224/images/page_214_image_11.jpg)

<details>
<summary>text_image</summary>

x
√x²−a²
t
a
</details>

图4-4

因此

$$
\int \frac {\mathrm{d} x}{\sqrt {x ^ {2} - a ^ {2}}} = \ln \left(\frac {x}{a} + \frac {\sqrt {x ^ {2} - a ^ {2}}}{a}\right) + C = \ln (x + \sqrt {x ^ {2} - a ^ {2}}) + C _ {1},
$$

其中  $C_{1}=C-\ln a.$

当 $x < -a$ 时，令 $x = -u$ ，那么 $u > a$ .由上段结果，有

$$
\begin{array}{l} \int \frac {\mathrm{d} x}{\sqrt {x ^ {2} - a ^ {2}}} = - \int \frac {\mathrm{d} u}{\sqrt {u ^ {2} - a ^ {2}}} = - \ln (u + \sqrt {u ^ {2} - a ^ {2}}) + C \\ = - \ln \left(- x + \sqrt {x ^ {2} - a ^ {2}}\right) + C = \ln \frac {- x - \sqrt {x ^ {2} - a ^ {2}}}{a ^ {2}} + C \\ = \ln (- x - \sqrt {x ^ {2} - a ^ {2}}) + C _ {1}, \\ \end{array}
$$

其中  $C_{1}=C-2\ln a.$

把在 $x > a$ 及 $x < -a$ 内的结果合起来, 可写作

$$
\int \frac {\mathrm{d} x}{\sqrt {x ^ {2} - a ^ {2}}} = \ln \left| x + \sqrt {x ^ {2} - a ^ {2}} \right| + C.
$$

198

---

第二节 换元积分法

从上面的三个例子可以看出:如果被积函数含有 $\sqrt{a^{2}-x^{2}}$ ，可以作代换 $x=a\sin t$ 化去根式；如果被积函数含有 $\sqrt{x^{2}+a^{2}}$ ，可以作代换 $x=atan t$ 化去根式；如果被积函数含有 $\sqrt{x^{2}-a^{2}}$ ，可以作代换 $x=\pm a\sec t$ 化去根式。但具体解题时要分析被积函数的具体情况，选取尽可能简捷的代换，不要拘泥于上述的变量代换（如例5、例7）。

当被积函数含有 $\sqrt{x^2\pm a^2}$ 时，为了化去根式，除采用三角代换 $x = a\tan t$ 或 $x = \pm a\sec t$ 外，还可利用公式

$$
\mathrm{ch} ^ {2} t - \mathrm{sh} ^ {2} t = 1,
$$

采用双曲代换  $x = a \operatorname{sh} t, x = \pm a \operatorname{ch} t$  来化去根式.

例如,在例 22 中,可设 x=ash t,则

$$
\sqrt {x ^ {2} + a ^ {2}} = \sqrt {a ^ {2} \mathrm{sh} ^ {2} t + a ^ {2}} = a \mathrm{ch} t, \quad \mathrm{d} x = a \mathrm{ch} t \mathrm{d} t,
$$

于是

$$
\begin{array}{l} \int \frac {\mathrm{d} x}{\sqrt {x ^ {2} + a ^ {2}}} = \int \frac {a \operatorname{ch} t}{a \operatorname{ch} t} \mathrm{d} t = \int \mathrm{d} t = t + C = \operatorname{arsh} \frac {x}{a} + C \\ = \ln \left[ \frac {x}{a} + \sqrt {\left(\frac {x}{a}\right) ^ {2} + 1} \right] + C = \ln (x + \sqrt {x ^ {2} + a ^ {2}}) + C _ {1}, \\ \end{array}
$$

其中  $C_{1}=C-\ln a.$

在例 23 中, 当 x > a 时, 可设  $x = a \operatorname{ch} t \quad (t > 0)$ , 则

$$
\sqrt {x ^ {2} - a ^ {2}} = \sqrt {a ^ {2} \mathrm{ch} ^ {2} t - a ^ {2}} = a \mathrm{sh} t, \quad \mathrm{d} x = a \mathrm{sh} t \mathrm{d} t,
$$

于是当 $x > a$ 时，

$$
\begin{array}{l} \int \frac {\mathrm{d} x}{\sqrt {x ^ {2} - a ^ {2}}} = \int \frac {a \mathrm{sh} t}{a \mathrm{sh} t} \mathrm{d} t = \int \mathrm{d} t = t + C = \mathrm{arch} \frac {x}{a} + C \\ = \ln \left[ \frac {x}{a} + \sqrt {\left(\frac {x}{a}\right) ^ {2} - 1} \right] + C = \ln (x + \sqrt {x ^ {2} - a ^ {2}}) + C _ {1}, \\ \end{array}
$$

其中  $C_{1}=C-\ln a.$

当 $x < -a$ 时，令 $x = -acht (t > 0)$，类似可得

$$
\int \frac {\mathrm{d} x}{\sqrt {x ^ {2} - a ^ {2}}} = \ln (- x - \sqrt {x ^ {2} - a ^ {2}}) + C _ {1}.
$$

上节所列基本积分表中没有双曲函数的积分公式,现添加两个常用的双曲函数积分公式:

⑭  $\int sh x dx = ch x + C,$

199

---

第四章 不定积分

⑮  $\int ch x dx = sh x + C.$

下面我们通过例子来介绍一种也很有用的代换——倒代换,利用它常可消去被积函数的分母中的变量因子 x.

例24 求 $\int \frac{\sqrt{a^2 - x^2}}{x^4}\mathrm{d}x$ （ $a\neq 0$ ）.

解 设 $x = \frac{1}{t}$, 则 $\mathrm{dx} = -\frac{\mathrm{dt}}{t^2}$, 于是

$$
\int \frac {\sqrt {a ^ {2} - x ^ {2}}}{x ^ {4}} \mathrm{d} x = \int \frac {\sqrt {a ^ {2} - \frac {1}{t ^ {2}}} \cdot \left(- \frac {\mathrm{d} t}{t ^ {2}}\right)}{\frac {1}{t ^ {4}}} = - \int (a ^ {2} t ^ {2} - 1) ^ {\frac {1}{2}} | t | \mathrm{d} t,
$$

当 $x > 0$ 时，有

$$
\begin{array}{l} \int \frac {\sqrt {a ^ {2} - x ^ {2}}}{x ^ {4}} \mathrm{d} x = - \frac {1}{2 a ^ {2}} \int (a ^ {2} t ^ {2} - 1) ^ {\frac {1}{2}} \mathrm{d} (a ^ {2} t ^ {2} - 1) \\ = - \frac {(a ^ {2} t ^ {2} - 1) ^ {\frac {3}{2}}}{3 a ^ {2}} + C = - \frac {(a ^ {2} - x ^ {2}) ^ {\frac {3}{2}}}{3 a ^ {2} x ^ {3}} + C, \\ \end{array}
$$

当 $x < 0$ 时, 有相同的结果.

在本节的例题中,有几个积分是以后经常会遇到的,所以它们通常也被当作公式使用.这样,常用的积分公式,除了基本积分表中的几个外,再添加下面几个(其中常数a>0):

⑯  $\int \tan x dx = -\ln |\cos x| + C,$

⑰  $\int\cot x dx=\ln|\sin x|+C,$

⑱  $\int \sec x dx = \ln |\sec x + \tan x| + C,$

⑲  $\int \csc x dx = \ln |\csc x - \cot x| + C,$

②0 $\int \frac{\mathrm{d}x}{a^2 + x^2} = \frac{1}{a}\arctan \frac{x}{a} + C,$

②1 $\int \frac{\mathrm{d}x}{x^2 - a^2} = \frac{1}{2a}\ln \left|\frac{x - a}{x + a}\right| + C,$

② $\int \frac{\mathrm{d}x}{\sqrt{a^2 - x^2}} = \arcsin \frac{x}{a} + C,$

②3 $\int \frac{\mathrm{d}x}{\sqrt{x^2 + a^2}} = \ln (x + \sqrt{x^2 + a^2}) + C,$

200

---

第二节 换元积分法

②4 $\int \frac{\mathrm{d}x}{\sqrt{x^2 - a^2}} = \ln \left|x + \sqrt{x^2 - a^2}\right| + C.$

例25 求 $\int \frac{\mathrm{d}x}{\sqrt{4x^2 + 9}}.$

解 $\int \frac{\mathrm{d}x}{\sqrt{4x^2 + 9}} = \int \frac{\mathrm{d}x}{\sqrt{(2x)^2 + 3^2}} = \frac{1}{2}\int \frac{\mathrm{d}(2x)}{\sqrt{(2x)^2 + 3^2}},$

利用公式②3,便得

$$
\int \frac {\mathrm{d} x}{\sqrt {4 x ^ {2} + 9}} = \frac {1}{2} \ln (2 x + \sqrt {4 x ^ {2} + 9}) + C.
$$

例26 求 $\int \frac{\mathrm{d}x}{\sqrt{1 + x - x^2}}.$

解 $\int \frac{\mathrm{d}x}{\sqrt{1 + x - x^2}} = \int \frac{\mathrm{d}\left(x - \frac{1}{2}\right)}{\sqrt{\left(\frac{\sqrt{5}}{2}\right)^2 - \left(x - \frac{1}{2}\right)^2}},$

利用公式②2,便得

$$
\int \frac {\mathrm{d} x}{\sqrt {1 + x - x ^ {2}}} = \arcsin \frac {2 x - 1}{\sqrt {5}} + C.
$$

在例 22 中, 我们用变换  $x = a \tan t$  消去被积函数中的根式  $\sqrt{x^{2} + a^{2}}$ , 这个变换还能消去被积函数分母中的  $(x^{2} + a^{2})$  的高次幂. 请看下例.

例27 求 $\int \frac{x^3}{(x^2 - 2x + 2)^2} \, \mathrm{d}x.$

解 分母是二次质因式的平方, 把二次质因式配方成  $(x-1)^{2}+1$ , 令  $x-1=\tan t\left(-\frac{\pi}{2}<t<\frac{\pi}{2}\right)$ , 则

$$
x ^ {2} - 2 x + 2 = \sec^ {2} t, \quad \mathrm{d} x = \sec^ {2} t \mathrm{d} t.
$$

于是

$$
\begin{array}{l} \int \frac {x ^ {3}}{(x ^ {2} - 2 x + 2) ^ {2}} \mathrm{d} x \\ = \int \frac {(\tan t + 1) ^ {3}}{\sec^ {4} t} \cdot \sec^ {2} t \mathrm{d} t \\ = \int \left(\sin^ {3} t \cos^ {- 1} t + 3 \sin^ {2} t + 3 \sin t \cos t + \cos^ {2} t\right) \mathrm{d} t \\ = \int (\sin^ {2} t \cos^ {- 1} t + 3 \cos t) \sin t \mathrm{d} t + \int (3 \sin^ {2} t + \cos^ {2} t) \mathrm{d} t \\ \end{array}
$$

201

---

第四章 不定积分

$$
\begin{array}{l} = \int \left[ (1 - \cos^ {2} t) \cos^ {- 1} t + 3 \cos t \right] \left[ - \mathrm{d} (\cos t) \right] + \int (2 - \cos 2 t) \mathrm{d} t \\ = - \int (\cos^ {- 1} t + 2 \cos t) \mathrm{d} (\cos t) + 2 t - \frac {1}{2} \sin 2 t \\ = - \ln \cos t - \cos^ {2} t + 2 t - \sin t \cos t + C, \\ \end{array}
$$

按  $\tan t = x - 1$  作辅助三角形(图 4-5)，便有

$$
\cos t = \frac {1}{\sqrt {x ^ {2} - 2 x + 2}}, \quad \sin t = \frac {x - 1}{\sqrt {x ^ {2} - 2 x + 2}},
$$

![](../../raw/pages_0193-0224/images/page_218_image_4.jpg)

<details>
<summary>text_image</summary>

√x²-2x+2
x-1
t
1
</details>

图4-5

于是

$$
\begin{array}{l} \int \frac {x ^ {3}}{(x ^ {2} - 2 x + 2) ^ {2}} \mathrm{d} x \\ = \frac {1}{2} \ln (x ^ {2} - 2 x + 2) + 2 \arctan (x - 1) - \frac {x}{x ^ {2} - 2 x + 2} + C. \\ \end{array}
$$

## 习题4-2

1. 在下列各式等号右端的横线处填入适当的系数, 使等式成立 (例如: $\mathrm{d}x = \frac{1}{4}\mathrm{d}(4x + 7)$):

(1)  $\mathrm{d}x=\_\mathrm{d}(ax)(a\neq0)$ ;
(2) $\mathrm{dx} = \_\mathrm{d}(7x - 3)$;
(3)  $x \, dx = \_\mathrm{d}(x^{2})$ ;
(4)  $x \, dx = \_\_ \, d(5x^{2})$ ;
(5)  $x \, dx = \_\mathrm{d}(1 - x^{2})$ ;
(6)  $x^{3}dx=$  \_\_\_\_ d( $3x^{4}-2$ );
(7)  $e^{2x}dx=$  \_ d(e^{2x});
(8)  $e^{-\frac{x}{2}}dx=$  \_\_\_\_  $d(1+e^{-\frac{x}{2}})$ ;
(9)  $\sin\frac{3}{2}xdx=$  \_ d  $\left(\cos\frac{3}{2}x\right)$ ;
(10) $\frac{\mathrm{d}x}{x} = \_ \mathrm{d}(5\ln |x|)$;
(11)  $\frac{dx}{x} = \_ d(3 - 5\ln |x|)$ ;
(12) $\frac{\mathrm{d}x}{1 + 9x^2} = -\mathrm{d}(\arctan 3x)$;
(13) $\frac{\mathrm{d}x}{\sqrt{1 - x^2}} = \_ \mathrm{d}(1 - \arcsin x)$;
(14) $\frac{x\mathrm{d}x}{\sqrt{1 - x^2}} = -\mathrm{d}(\sqrt{1 - x^2}).$

2. 求下列不定积分(其中  $a, b, \omega, \varphi$  均为常数):

(1) $\int \mathrm{e}^{5t}\mathrm{d}t$;
(2) $\int (3 - 2x)^{3}\mathrm{d}x;$
(3) $\int \frac{\mathrm{d}x}{1 - 2x}$;
(4) $\int \frac{\mathrm{d}x}{\sqrt[3]{2 - 3x}};$
(5) $\int (\sin ax - e^{\frac{x}{b}})dx;$
(6) $\int \frac{\sin\sqrt{t}}{\sqrt{t}}\mathrm{d}t;$
(7) $\int x\mathrm{e}^{-x^2}\mathrm{d}x;$
(8) $\int x\cos (x^2)\mathrm{d}x;$

202

---

第二节 换元积分法

(9) $\int \frac{x}{\sqrt{2 - 3x^2}}\mathrm{d}x;$

(10) $\int \frac{3x^3}{1 - x^4}\mathrm{d}x;$

(11) $\int\frac{x+1}{x^{2}+2x+5}dx;$

(12) $\int \cos^2 (\omega t + \varphi)\sin (\omega t + \varphi)\mathrm{d}t;$

(13) $\int \frac{\sin x}{\cos^3 x} \, \mathrm{d}x$;

(14) $\int \frac{\sin x + \cos x}{\sqrt[3]{\sin x - \cos x}}\mathrm{d}x;$

(15) $\int \tan^{10}x\cdot \sec^2 x\mathrm{d}x;$

(16) $\int \frac{\mathrm{d}x}{x\ln x\ln\ln x};$

(17) $\int \frac{\mathrm{d}x}{(\arcsin x)^2\sqrt{1 - x^2}};$

(18) $\int \frac{10^{2\arccos x}}{\sqrt{1 - x^2}}\mathrm{d}x;$

(19) $\int \tan \sqrt{1 + x^2} \cdot \frac{x \, \mathrm{d}x}{\sqrt{1 + x^2}};$

(20) $\int \frac{\arctan\sqrt{x}}{\sqrt{x}(1 + x)}\mathrm{d}x;$

(21) $\int \frac{1 + \ln x}{(x\ln x)^2}\mathrm{d}x;$

(22) $\int \frac{\mathrm{d}x}{\sin x\cos x}$;

(23) $\int\frac{\ln\tan x}{\cos x\sin x}dx;$

(24) $\int \cos^3 x\mathrm{d}x$

(25) $\int \cos^2 (\omega t + \varphi)\mathrm{d}t;$

(26) $\int \sin 2x\cos 3xdx$;

(27) $\int \cos x\cos \frac{x}{2}\mathrm{d}x;$

(28)  $\int \sin 5x \sin 7x dx;$

(29) $\int \tan^3 x\sec x\mathrm{d}x;$

(30) $\int \frac{\mathrm{d}x}{\mathrm{e}^x + \mathrm{e}^{-x}};$

(31) $\int \frac{1 - x}{\sqrt{9 - 4x^2}}\mathrm{d}x;$

(32) $\int \frac{x^3}{9 + x^2}\mathrm{d}x;$

(33) $\int\frac{dx}{2x^{2}-1};$

(34) $\int \frac{\mathrm{d}x}{(x + 1)(x - 2)};$

(35) $\int \frac{x}{x^2 - x - 2}\mathrm{d}x;$

(36) $\int \frac{x^2\mathrm{d}x}{\sqrt{a^2 - x^2}} (a > 0);$

(37) $\int \frac{\mathrm{d}x}{x\sqrt{x^2 - 1}};$

(38) $\int \frac{\mathrm{d}x}{\sqrt{(x^2 + 1)^3}};$

(39) $\int \frac{\sqrt{x^2 - 9}}{x}\mathrm{d}x;$

(40) $\int \frac{\mathrm{d}x}{1 + \sqrt{2x}};$

(41) $\int \frac{\mathrm{d}x}{1 + \sqrt{1 - x^2}};$

(42) $\int \frac{\mathrm{d}x}{x + \sqrt{1 - x^2}};$

(43) $\int \frac{x - 1}{x^2 + 2x + 3}\mathrm{d}x;$

(44) $\int \frac{x^3 + 1}{(x^2 + 1)^2} \, \mathrm{d}x.$

203

---

第四章 不定积分

## 第三节 分部积分法

前面我们在复合函数求导法则的基础上,得到了换元积分法.现在我们利用两个函数乘积的求导法则,来推得另一个求积分的基本方法——分部积分法.

设函数 $u = u(x)$ 及 $v = v(x)$ 具有连续导数，则两个函数乘积的导数公式为

$$
(u v) ^ {\prime} = u ^ {\prime} v + u v ^ {\prime},
$$

移项,得

$$
u v ^ {\prime} = (u v) ^ {\prime} - u ^ {\prime} v.
$$

对这个等式两边求不定积分,得

$$
\int u v ^ {\prime} \mathrm{d} x = u v - \int u ^ {\prime} v \mathrm{d} x. \tag {3-1}
$$

公式(3-1)称为分部积分公式.如果求 $\int uv^{\prime}\mathrm{d}x$ 有困难，而求 $\int u^{\prime}v\mathrm{d}x$ 比较容易时，分部积分公式就可以发挥作用了.

为简便起见,也可把公式(3-1)写成下面的形式:

$$
\int u \mathrm{d} v = u v - \int v \mathrm{d} u. \tag {3-2}
$$

现在通过例子说明如何运用这个重要公式.

例1 求 $\int x\cos x\mathrm{d}x.$

解 这个积分用换元积分法不易求得结果, 现在试用分部积分法来求它. 但是怎样选取 u 和 dv 呢? 如果设  $u = x, dv = \cos x \, dx$ , 则  $du = dx, v = \sin x$ , 代入分部积分公式 (3-2), 得

$$
\int x \cos x \mathrm{d} x = x \sin x - \int \sin x \mathrm{d} x,
$$

而 $\int v\mathrm{d}u = \int \sin x\mathrm{d}x$ 容易积出，所以

$$
\int x \cos x \mathrm{d} x = x \sin x + \cos x + C.
$$

求这个积分时,如果设  $u=\cos x$ , dv=xdx, 则

$$
\mathrm{d} u = - \sin x \mathrm{d} x, \quad v = \frac {x ^ {2}}{2}.
$$

于是

$$
\int x \cos x \mathrm{d} x = \frac {x ^ {2}}{2} \cos x + \int \frac {x ^ {2}}{2} \sin x \mathrm{d} x.
$$

204

---

第三节 分部积分法

上式右端的积分比原积分更不容易求出.

由此可见,如果 u 和 dv 选取不当,就求不出结果,所以应用分部积分法时,恰当选取 u 和 dv 是一个关键.选取 u 和 dv 一般要考虑下面两点:

(1) v 要容易求得;
(2) $\int vdu$  要比  $\int udv$  容易积出.

例2 求 $\int x\mathrm{e}^{x}\mathrm{d}x.$

解 设 $u = x, \mathrm{d}v = \mathrm{e}^x\mathrm{d}x$，则 $\mathrm{d}u = \mathrm{d}x, v = \mathrm{e}^x$. 于是

$$
\int x \mathrm{e} ^ {x} \mathrm{d} x = x \mathrm{e} ^ {x} - \int \mathrm{e} ^ {x} \mathrm{d} x = x \mathrm{e} ^ {x} - \mathrm{e} ^ {x} + C = \mathrm{e} ^ {x} (x - 1) + C.
$$

运用分部积分公式(3-2)的形式,例1、例2的求解过程也可表述为

$$
\begin{array}{l} \int x \cos x \mathrm{d} x = \int x \mathrm{d} (\sin x) = x \sin x - \int \sin x \mathrm{d} x = x \sin x + \cos x + C. \\ \int x \mathrm{e} ^ {x} \mathrm{d} x = \int x \mathrm{d} (\mathrm{e} ^ {x}) = x \mathrm{e} ^ {x} - \int \mathrm{e} ^ {x} \mathrm{d} x = x \mathrm{e} ^ {x} - \mathrm{e} ^ {x} + C = (x - 1) \mathrm{e} ^ {x} + C. \\ \end{array}
$$

例3 求 $\int x^{2}\mathrm{e}^{x}\mathrm{d}x.$

解 设 $u = x^{2}, \mathrm{d}v = \mathrm{e}^{x}\mathrm{d}x = \mathrm{d}(\mathrm{e}^{x})$，则

$$
\int x ^ {2} \mathrm{e} ^ {x} \mathrm{d} x = \int x ^ {2} \mathrm{d} (\mathrm{e} ^ {x}) = x ^ {2} \mathrm{e} ^ {x} - \int \mathrm{e} ^ {x} \mathrm{d} (x ^ {2}) = x ^ {2} \mathrm{e} ^ {x} - 2 \int x \mathrm{e} ^ {x} \mathrm{d} x.
$$

这里 $\int x\mathrm{e}^{x}\mathrm{d}x$ 比 $\int x^{2}\mathrm{e}^{x}\mathrm{d}x$ 容易积出，因为被积函数中 $x$ 的幂次前者比后者降低了一次.由例2可知，对 $\int x\mathrm{e}^{x}\mathrm{d}x$ 再使用一次分部积分法就可以了.于是

$$
\begin{array}{l} \int x ^ {2} \mathrm{e} ^ {x} \mathrm{d} x = x ^ {2} \mathrm{e} ^ {x} - 2 \int x \mathrm{e} ^ {x} \mathrm{d} x = x ^ {2} \mathrm{e} ^ {x} - 2 \int x \mathrm{d} (\mathrm{e} ^ {x}) \\ = x ^ {2} \mathrm{e} ^ {x} - 2 (x \mathrm{e} ^ {x} - \mathrm{e} ^ {x}) + C = \mathrm{e} ^ {x} (x ^ {2} - 2 x + 2) + C. \\ \end{array}
$$

总结上面三个例子可以知道,如果被积函数是幂函数和正(余)弦函数或幂函数和指数函数的乘积,就可以考虑用分部积分法,并设幂函数为 u. 这样用一次分部积分法就可以使幂函数的幂次降低一次.这里假定幂指数是正整数.

例4 求 $\int x\ln x\mathrm{d}x.$

解 设 $u = \ln x, \mathrm{d}v = x\mathrm{d}x$ ，则

$$
\begin{array}{l} \int x \ln x \mathrm{d} x = \int \ln x \mathrm{d} \left(\frac {x ^ {2}}{2}\right) = \frac {x ^ {2}}{2} \ln x - \int \frac {x ^ {2}}{2} \mathrm{d} (\ln x) \\ = \frac {x ^ {2}}{2} \ln x - \frac {1}{2} \int x \mathrm{d} x = \frac {x ^ {2}}{2} \ln x - \frac {x ^ {2}}{4} + C. \\ \end{array}
$$

205

---

第四章 不定积分

例 5 求  $\int \arccos x dx$ .

解 设 $u = \arccos x, \mathrm{d}v = \mathrm{d}x$，则

$$
\begin{array}{l} \int \arccos x \mathrm{d} x = x \arccos x - \int x \mathrm{d} (\arccos x) = x \arccos x + \int \frac {x}{\sqrt {1 - x ^ {2}}} \mathrm{d} x \\ = x \arccos x - \frac {1}{2} \int \frac {1}{(1 - x ^ {2}) ^ {\frac {1}{2}}} \mathrm{d} (1 - x ^ {2}) = x \arccos x - \sqrt {1 - x ^ {2}} + C. \\ \end{array}
$$

在分部积分法运用比较熟练以后,就不必再写出哪一部分选作 u,哪一部分选作 dv. 只要把被积表达式凑成  $\varphi(x)\mathrm{d}\psi(x)$  的形式,便可使用分部积分公式.

例6 求 $\int x\arctan x\mathrm{d}x.$

$$
\begin{array}{l} = \frac {x ^ {2}}{2} \arctan x - \frac {1}{2} \int \frac {1 + x ^ {2} - 1}{1 + x ^ {2}} \mathrm{d} x = \frac {x ^ {2}}{2} \arctan x - \frac {1}{2} \int \left(1 - \frac {1}{1 + x ^ {2}}\right) \mathrm{d} x \\ = \frac {x ^ {2}}{2} \arctan x - \frac {1}{2} (x - \arctan x) + C = \frac {1}{2} (x ^ {2} + 1) \arctan x - \frac {1}{2} x + C. \\ \end{array}
$$

解 $\int x\arctan x\mathrm{d}x = \frac{1}{2}\int \arctan x\mathrm{d}(x^2) = \frac{x^2}{2}\arctan x - \frac{1}{2}\int \frac{x^2}{1 + x^2}\mathrm{d}x$

总结上面三个例子可以知道,如果被积函数是幂函数和对数函数或幂函数和反三角函数的乘积,就可以考虑用分部积分法,并设对数函数或反三角函数为 u.

下面几个例子中所用的方法也是比较典型的，

例7 求 $\int \mathrm{e}^{x}\sin x\mathrm{d}x.$

解 $\int \mathrm{e}^{x}\sin x\mathrm{d}x = \int \sin x\mathrm{d}(e^{x}) = e^{x}\sin x - \int e^{x}\cos x\mathrm{d}x,$

等式右端的积分与等式左端的积分是同一类型的,对右端的积分再用一次分部积分法,得

$$
\int \mathrm{e} ^ {x} \sin x \mathrm{d} x = \mathrm{e} ^ {x} \sin x - \int \cos x \mathrm{d} (\mathrm{e} ^ {x}) = \mathrm{e} ^ {x} \sin x - \mathrm{e} ^ {x} \cos x - \int \mathrm{e} ^ {x} \sin x \mathrm{d} x,
$$

由于上式右端的第三项就是所求的积分 $\int \mathrm{e}^{x}\sin x\mathrm{d}x$ ，把它移到等号左端去，等式两端再同除以2,便得

$$
\int \mathrm{e} ^ {x} \sin x \mathrm{d} x = \frac {1}{2} \mathrm{e} ^ {x} (\sin x - \cos x) + C.
$$

因上式右端已不包含积分项,所以必须加上任意常数 C.

206

---

第三节 分部积分法

例 8 求  $\int \sec^{3}x dx,$

解 $\int \sec^3 x\mathrm{d}x = \int \sec x\mathrm{d}(\tan x)$

$$
\begin{array}{l} = \sec x \tan x - \int \sec x \tan^ {2} x \mathrm{d} x \\ = \sec x \tan x - \int \sec x (\sec^ {2} x - 1) \mathrm{d} x \\ = \sec x \tan x - \int \sec^ {3} x \mathrm{d} x + \int \sec x \mathrm{d} x \\ = \sec x \tan x + \ln | \sec x + \tan x | - \int \sec^ {3} x \mathrm{d} x. \\ \end{array}
$$

由于上式右端的第三项就是所求的积分 $\int \sec^3 x\mathrm{d}x$ ，把它移到等号左端去，等式两端再同时除以2，便得

$$
\int \sec^ {3} x \mathrm{d} x = \frac {1}{2} (\sec x \tan x + \ln | \sec x + \tan x |) + C.
$$

在积分的过程中往往要兼用换元法与分部积分法,如例5,下面再来举一个例子.

例 9 求  $\int e^{\sqrt{x}} dx$ .

解 令 $\sqrt{x} = t$ ，则 $x = t^2, \mathrm{d}x = 2t\mathrm{d}t.$ 于是

$$
\int \mathrm{e} ^ {\sqrt {x}} \mathrm{d} x = 2 \int t \mathrm{e} ^ {t} \mathrm{d} t.
$$

利用例 2 的结果, 并用  $t=\sqrt{x}$  代回, 便得所求积分:

$$
\int \mathrm{e} ^ {\sqrt {x}} \mathrm{d} x = 2 \int t \mathrm{e} ^ {t} \mathrm{d} t = 2 \mathrm{e} ^ {t} (t - 1) + C = 2 \mathrm{e} ^ {\sqrt {x}} (\sqrt {x} - 1) + C.
$$

## 习题 4-3

求下列不定积分:

1. $\int x\sin x\mathrm{d}x.$

2. $\int \ln x\mathrm{d}x.$

3. $\int \arcsin x \, \mathrm{d}x$.

4. $\int x\mathrm{e}^{-x}\mathrm{d}x.$

5. $\int x^{2}\ln x\mathrm{d}x.$

6. $\int \mathrm{e}^{-x}\cos x\mathrm{d}x.$

7. $\int \mathrm{e}^{-2x}\sin \frac{x}{2}\mathrm{d}x.$

8. $\int x\cos \frac{x}{2}\mathrm{d}x.$

9. $\int x^{2}\arctan x\mathrm{d}x$.

10. $\int x\tan^2 x\mathrm{d}x$

11. $\int x^{2}\cos x\mathrm{d}x.$

12. $\int t\mathrm{e}^{-2t}\mathrm{d}t.$

13. $\int \ln^2 x\mathrm{d}x$

14. $\int x\sin x\cos x\mathrm{d}x.$

15. $\int x^{2}\cos^{2}\frac{x}{2}\mathrm{d}x.$

图

释疑解难

4-3

207

---

第四章 不定积分

16. $\int x\ln (x - 1)\mathrm{d}x.$

17. $\int (x^{2} - 1)\sin 2x\mathrm{d}x.$

18. $\int \frac{\ln^3 x}{x^2} \, \mathrm{d}x$.

19. $\int \mathrm{e}^{\sqrt[3]{x}}\mathrm{d}x.$

20. $\int \cos \ln x\mathrm{d}x.$

21. $\int (\arcsin x)^{2}\mathrm{d}x.$

22. $\int \mathrm{e}^{x}\sin^{2}x\mathrm{d}x.$

23. $\int x\ln^2 x\mathrm{d}x.$

24. $\int \mathrm{e}^{\sqrt{3x + 9}}\mathrm{d}x.$

## 第四节 有理函数的积分

前面已经介绍了求不定积分的两个基本方法——换元积分法和分部积分法,下面简要地介绍有理函数的积分及可化为有理函数的积分.

## 一、有理函数的积分

两个多项式的商 $\frac{P(x)}{Q(x)}$ 称为有理函数,又称有理分式.我们总假定分子多项式 $P(x)$ 与分母多项式 $Q(x)$ 之间没有公因式.当分子多项式 $P(x)$ 的次数小于分母多项式 $Q(x)$ 的次数时,称这有理函数为真分式,否则称为假分式.

利用多项式的除法,总可以将一个假分式化成一个多项式与一个真分式之和的形式,例如第一节例15中的被积函数

$$
\frac {2 x ^ {4} + x ^ {2} + 3}{x ^ {2} + 1} = 2 x ^ {2} - 1 + \frac {4}{x ^ {2} + 1}.
$$

对于真分式 $\frac{P(x)}{Q(x)}$ ，如果分母可分解为两个多项式的乘积

$$
Q (x) = Q _ {1} (x) Q _ {2} (x),
$$

且 $Q_{1}(x)$ 与 $Q_{2}(x)$ 没有公因式，那么它可分拆成两个真分式之和

$$
\frac {P (x)}{Q (x)} = \frac {P _ {1} (x)}{Q _ {1} (x)} + \frac {P _ {2} (x)}{Q _ {2} (x)},
$$

上述步骤称为把真分式化成部分分式之和.如果 $Q_{1}(x)$ 或 $Q_{2}(x)$ 还能再分解成两个没有公因式的多项式的乘积，那么就可再分拆成更简单的部分分式.最后，有理函数的分解式中只出现多项式、 $\frac{P_1(x)}{(x - a)^k}$ 、 $\frac{P_2(x)}{(x^2 + px + q)^l}$ 等三类函数（这里 $p^2 -4q <   0,P_1(x)$ 为小于 $k$ 次的多项式， $P_{2}(x)$ 为小于 $2l$ 次的多项式).多项式的积分容易求得，后两类真分式的积分可参看第二节例3和例27.

208

---

第四节 有理函数的积分

下面举几个真分式的积分的例子.

例1 求 $\int \frac{x + 1}{x^2 - 5x + 6}\mathrm{d}x.$

解 被积函数的分母分解成 $(x-3)(x-2)$ ，故可设

$$
\frac {x + 1}{x ^ {2} - 5 x + 6} = \frac {A}{x - 3} + \frac {B}{x - 2},
$$

其中 A, B 为待定系数. 上式两端去分母后, 得

$$
x + 1 = A (x - 2) + B (x - 3),
$$

即

$$
x + 1 = (A + B) x - 2 A - 3 B.
$$

比较上式两端同次幂的系数,即有

$$
\left\{ \begin{array}{l} A + B = 1, \\ 2 A + 3 B = - 1, \end{array} \right.
$$

从而解得 A=4, B=-3. 于是

$$
\int \frac {x + 1}{x ^ {2} - 5 x + 6} \mathrm{d} x = \int \left(\frac {4}{x - 3} - \frac {3}{x - 2}\right) \mathrm{d} x = 4 \ln | x - 3 | - 3 \ln | x - 2 | + C.
$$

例2 求 $\int \frac{x + 2}{(2x + 1)(x^2 + x + 1)}\mathrm{d}x.$

解 设 $\frac{x + 2}{(2x + 1)(x^2 + x + 1)} = \frac{A}{2x + 1} +\frac{Bx + D}{x^2 + x + 1}$ ，则

$$
x + 2 = A (x ^ {2} + x + 1) + (B x + D) (2 x + 1),
$$

即

$$
x + 2 = (A + 2 B) x ^ {2} + (A + B + 2 D) x + A + D,
$$

比较上式两端同次幂的系数,即有

$$
\left\{ \begin{array}{l} A + 2 B = 0, \\ A + B + 2 D = 1, \\ A + D = 2, \end{array} \right.
$$

从而解得 $\left\{\begin{aligned}A=2,\\ B=-1,\\ D=0.\end{aligned}\right.$ 于是

209

---

第四章 不定积分

$$
\begin{array}{l} \int \frac {x + 2}{(2 x + 1) (x ^ {2} + x + 1)} \mathrm{d} x \\ = \int \left(\frac {2}{2 x + 1} - \frac {x}{x ^ {2} + x + 1}\right) \mathrm{d} x = \ln | 2 x + 1 | - \frac {1}{2} \int \frac {(2 x + 1) - 1}{x ^ {2} + x + 1} \mathrm{d} x \\ = \ln | 2 x + 1 | - \frac {1}{2} \int \frac {\mathrm{d} (x ^ {2} + x + 1)}{x ^ {2} + x + 1} + \frac {1}{2} \int \frac {\mathrm{d} x}{\left(x + \frac {1}{2}\right) ^ {2} + \frac {3}{4}} \\ = \ln | 2 x + 1 | - \frac {1}{2} \ln (x ^ {2} + x + 1) + \frac {1}{\sqrt {3}} \arctan \frac {2 x + 1}{\sqrt {3}} + C. \\ \end{array}
$$

例3 求 $\int \frac{x - 3}{(x - 1)(x^2 - 1)}\mathrm{d}x.$

解 被积函数分母的两个因式 $x - 1$ 与 $x^{2} - 1$ 有公因式, 故需再分解成 $(x - 1)^{2}(x + 1)$. 设

$$
\frac {x - 3}{(x - 1) ^ {2} (x + 1)} = \frac {A x + B}{(x - 1) ^ {2}} + \frac {D}{x + 1},
$$

则

$$
x - 3 = (A x + B) (x + 1) + D (x - 1) ^ {2},
$$

即

$$
x - 3 = (A + D) x ^ {2} + (A + B - 2 D) x + B + D,
$$

比较上式两端同次幂的系数,即有

$$
\left\{ \begin{array}{l} A + D = 0, \\ A + B - 2 D = 1, \\ B + D = - 3, \end{array} \right.
$$

从而解得 $\left\{\begin{aligned}A=1,\\ B=-2,\\ D=-1.\end{aligned}\right.$ 于是

$$
\begin{array}{l} \int \frac {x - 3}{(x - 1) (x ^ {2} - 1)} \mathrm{d} x \\ = \int \frac {x - 3}{(x - 1) ^ {2} (x + 1)} \mathrm{d} x = \int \left[ \frac {x - 2}{(x - 1) ^ {2}} - \frac {1}{x + 1} \right] \mathrm{d} x \\ = \int \frac {x - 1 - 1}{(x - 1) ^ {2}} \mathrm{d} x - \ln | x + 1 | \\ = \ln | x - 1 | + \frac {1}{x - 1} - \ln | x + 1 | + C. \\ \end{array}
$$

210

---

第四节 有理函数的积分

## 二、可化为有理函数的积分举例

例 4 求  $\int\frac{1+\sin x}{\sin x(1+\cos x)}dx.$

解 由三角函数公式知道, $\sin x$ 与 $\cos x$ 都可以用 $\tan\frac{x}{2}$ 的有理式表示,即

$$
\sin x = 2 \sin \frac {x}{2} \cos \frac {x}{2} = \frac {2 \tan \frac {x}{2}}{\sec^ {2} \frac {x}{2}} = \frac {2 \tan \frac {x}{2}}{1 + \tan^ {2} \frac {x}{2}},
$$

$$
\cos x = \cos^ {2} \frac {x}{2} - \sin^ {2} \frac {x}{2} = \frac {1 - \tan^ {2} \frac {x}{2}}{\sec^ {2} \frac {x}{2}} = \frac {1 - \tan^ {2} \frac {x}{2}}{1 + \tan^ {2} \frac {x}{2}}.
$$

如果作代换 $u = \tan \frac{x}{2} (-\pi < x < \pi)$ ①, 那么

$$
\sin x = \frac {2 u}{1 + u ^ {2}}, \quad \cos x = \frac {1 - u ^ {2}}{1 + u ^ {2}},
$$

而 $x = 2\arctan u$ ，从而

$$
\mathrm{d} x = \frac {2}{1 + u ^ {2}} \mathrm{d} u.
$$

于是

$$
\begin{array}{l} \int \frac {1 + \sin x}{\sin x (1 + \cos x)} \mathrm{d} x \\ = \int \frac {\left(1 + \frac {2 u}{1 + u ^ {2}}\right) \frac {2 \mathrm{d} u}{1 + u ^ {2}}}{\frac {2 u}{1 + u ^ {2}} \left(1 + \frac {1 - u ^ {2}}{1 + u ^ {2}}\right)} = \frac {1}{2} \int \left(u + 2 + \frac {1}{u}\right) \mathrm{d} u \\ = \frac {1}{2} \left(\frac {u ^ {2}}{2} + 2 u + \ln | u |\right) + C = \frac {1}{4} \tan^ {2} \frac {x}{2} + \tan \frac {x}{2} + \frac {1}{2} \ln \left| \tan \frac {x}{2} \right| + C. \\ \end{array}
$$

本例所用的变量代换  $u=\tan\frac{x}{2}$  对三角函数有理式的积分都可以应用.

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 当 $x \in ((2k - 1)\pi, (2k + 1)\pi), k \in \mathbb{Z}$ 时，作代换 $u = \tan \frac{x - 2k\pi}{2} = \tan \frac{x}{2}, x = 2k\pi + 2\arctan u$ ，以下所得结果相同.</span></small>

![](../../raw/pages_0225-0256/images/page_227_image_14.jpg)

释疑解难

4-4

211

---

第四章 不定积分

例5 求 $\int \frac{\sqrt{x - 1}}{x}\mathrm{d}x.$

解 为了去掉根号, 可以设  $\sqrt{x-1}=u$ , 于是  $x=u^{2}+1$ , dx=2udu, 从而所求积分为

$$
\begin{array}{l} \int \frac {\sqrt {x - 1}}{x} \mathrm{d} x = \int \frac {u}{u ^ {2} + 1} \cdot 2 u \mathrm{d} u = 2 \int \frac {u ^ {2}}{u ^ {2} + 1} \mathrm{d} u \\ = 2 \int \left(1 - \frac {1}{1 + u ^ {2}}\right) \mathrm{d} u = 2 (u - \arctan u) + C \\ = 2 (\sqrt {x - 1} - \arctan \sqrt {x - 1}) + C. \\ \end{array}
$$

例6 求 $\int \frac{\mathrm{d}x}{1 + \sqrt[3]{x + 2}}.$

解 为了去掉根号, 可以设  $\sqrt[3]{x+2}=u$ . 于是  $x=u^{3}-2$ ,  $dx=3u^{2}du$ , 从而所求积分为

$$
\begin{array}{l} \int \frac {\mathrm{d} x}{1 + \sqrt [ 3 ]{x + 2}} = \int \frac {3 u ^ {2}}{1 + u} \mathrm{d} u \\ = 3 \int \left(u - 1 + \frac {1}{1 + u}\right) \mathrm{d} u = 3 \left(\frac {u ^ {2}}{2} - u + \ln | 1 + u |\right) + C \\ = \frac {3}{2} \sqrt [ 3 ]{(x + 2) ^ {2}} - 3 \sqrt [ 3 ]{x + 2} + 3 \ln | 1 + \sqrt [ 3 ]{x + 2} | + C. \\ \end{array}
$$

例7 求 $\int \frac{\mathrm{d}x}{(1 + \sqrt[3]{x})\sqrt{x}}.$

解 被积函数中出现了两个根式 $\sqrt{x}$ 及 $\sqrt[3]{x}$, 为了能同时消去这两个根式, 可令 $x = u^6$, 于是 $\mathrm{dx} = 6u^5\mathrm{du}$, 从而所求积分为

$$
\begin{array}{l} \int \frac {\mathrm{d} x}{(1 + \sqrt [ 3 ]{x}) \sqrt {x}} = \int \frac {6 u ^ {5}}{(1 + u ^ {2}) u ^ {3}} \mathrm{d} u = 6 \int \frac {u ^ {2}}{1 + u ^ {2}} \mathrm{d} u \\ = 6 \int \left(1 - \frac {1}{1 + u ^ {2}}\right) \mathrm{d} u = 6 (u - \arctan u) + C \\ = 6 \left(\sqrt [ 6 ]{x} - \arctan \sqrt [ 6 ]{x}\right) + C. \\ \end{array}
$$

例8 求 $\int \frac{1}{x}\sqrt{\frac{1 + x}{x}}\mathrm{d}x.$

解 为了去掉根号, 可以设  $\sqrt{\frac{1+x}{x}} = u$ , 于是  $\frac{1+x}{x} = u^{2}$ ,  $x = \frac{1}{u^{2}-1}$ ,  $dx = -\frac{2udu}{(u^{2}-1)^{2}}$ , 从而所求积分为

$$
\int \frac {1}{x} \sqrt {\frac {1 + x}{x}} \mathrm{d} x = \int (u ^ {2} - 1) u \cdot \frac {- 2 u}{(u ^ {2} - 1) ^ {2}} \mathrm{d} u = - 2 \int \frac {u ^ {2}}{u ^ {2} - 1} \mathrm{d} u
$$

212

---

第五节 积分表的使用

$$
\begin{array}{l} = - 2 \int \left(1 + \frac {1}{u ^ {2} - 1}\right) \mathrm{d} u = - 2 u - \ln \left| \frac {u - 1}{u + 1} \right| + C \\ = - 2 u + 2 \ln (u + 1) - \ln | u ^ {2} - 1 | + C \\ = - 2 \sqrt {\frac {1 + x}{x}} + 2 \ln \left(\sqrt {\frac {1 + x}{x}} + 1\right) + \ln | x | + C. \\ \end{array}
$$

以上四个例子表明,如果被积函数中含有简单根式 $\sqrt[n]{ax+b}$ 或 $\sqrt[n]{\frac{ax+b}{cx+d}}$ ，可以令这个简单根式为u.由于这样的变换具有反函数,且反函数是u的有理函数,因此原积分即可化为有理函数的积分.

## 习题4- 4

求下列不定积分:

1.  $\int\frac{x^{3}}{x+3}dx.$

2. $\int \frac{2x + 3}{x^2 + 3x - 10}\mathrm{d}x.$

3. $\int \frac{x + 1}{x^2 - 2x + 5}\mathrm{d}x.$

4. $\int \frac{\mathrm{d}x}{x(x^2 + 1)}.$

5. $\int \frac{3}{x^3 + 1}\mathrm{d}x.$

6. $\int \frac{x^2 + 1}{(x + 1)^2(x - 1)}\mathrm{d}x.$

7. $\int \frac{x\mathrm{d}x}{(x + 1)(x + 2)(x + 3)}.$

8. $\int \frac{x^5 + x^4 - 8}{x^3 - x}\mathrm{d}x.$

9. $\int \frac{\mathrm{d}x}{(x^2 + 1)(x^2 + x)}.$

10. $\int \frac{1}{x^4 - 1}\mathrm{d}x.$

11. $\int \frac{\mathrm{d}x}{(x^2 + 1)(x^2 + x + 1)}.$

12. $\int \frac{(x + 1)^2}{(x^2 + 1)^2}\mathrm{d}x.$

13.  $\int\frac{-x^{2}-2}{(x^{2}+x+1)^{2}}dx.$

14.  $\int\frac{dx}{3+\sin^{2}x}.$

15. $\int \frac{\mathrm{d}x}{3 + \cos x}$.

16.  $\int\frac{dx}{2+\sin x}.$

17. $\int \frac{\mathrm{d}x}{1 + \sin x + \cos x}$.

18.  $\int\frac{dx}{2\sin x-\cos x+5}.$

19. $\int \frac{\mathrm{d}x}{1 + \sqrt[3]{x + 1}}.$

20. $\int \frac{(\sqrt{x})^3 - 1}{\sqrt{x} + 1}\mathrm{d}x.$

21. $\int \frac{\sqrt{x + 1} - 1}{\sqrt{x + 1} + 1}\mathrm{d}x.$

22. $\int \frac{\mathrm{d}x}{\sqrt{x} + \sqrt[4]{x}}.$

23. $\int \sqrt{\frac{1 - x}{1 + x}}\frac{\mathrm{d}x}{x}.$

24. $\int \frac{\mathrm{d}x}{\sqrt[3]{(x + 1)^2(x - 1)^4}}.$

## 第五节 积分表的使用

通过前面的讨论可以看出,积分的计算要比导数的计算来得灵活、复杂.为了实用的方便,往往把常用的积分公式汇集成表,这种表叫做积分表.积分表是按照被积函数的类型来排列的.求积分时,可根据被积函数的类型直接地或经过简单的变形后,在表

213

---

第四章 不定积分

内查得所需的结果.

本书末附录Ⅳ有一个简单的积分表,以供查阅.

我们先举几个可以直接从积分表中查得结果的积分例子.

例1 求 $\int \frac{x}{(3x + 4)^2}\mathrm{d}x.$

解 被积函数含有 $ax + b$ ，在积分表(一)中查得公式7

$$
\int \frac {x}{(a x + b) ^ {2}} \mathrm{d} x = \frac {1}{a ^ {2}} \left(\ln | a x + b | + \frac {b}{a x + b}\right) + C.
$$

现在 $a = 3, b = 4$ ，于是

$$
\int \frac {x}{(3 x + 4) ^ {2}} \mathrm{d} x = \frac {1}{9} \left(\ln | 3 x + 4 | + \frac {4}{3 x + 4}\right) + C.
$$

例2 求 $\int \frac{\mathrm{d}x}{5 - 4\cos x}$.

解 被积函数含有三角函数, 在积分表(十一)中查得关于积分  $\int\frac{dx}{a+b\cos x}$  的公式, 但是公式有两个, 要看  $a^{2}>b^{2}$  或  $a^{2}<b^{2}$  而决定采用哪一个.

现在 $a = 5, b = -4, a^2 > b^2$，所以用公式105

$$
\int \frac {\mathrm{d} x}{a + b \cos x} = \frac {2}{a + b} \sqrt {\frac {a + b}{a - b}} \arctan \left(\sqrt {\frac {a - b}{a + b}} \tan \frac {x}{2}\right) + C \quad (a ^ {2} > b ^ {2}).
$$

于是

$$
\begin{array}{l} \int \frac {\mathrm{d} x}{5 - 4 \cos x} = \frac {2}{5 + (- 4)} \sqrt {\frac {5 + (- 4)}{5 - (- 4)}} \arctan \left(\sqrt {\frac {5 - (- 4)}{5 + (- 4)}} \tan \frac {x}{2}\right) + C \\ = \frac {2}{3} \arctan \left(3 \tan \frac {x}{2}\right) + C. \\ \end{array}
$$

下面再举一个需要先进行变量代换,然后再查表求积分的例子.

例3 求 $\int \frac{\mathrm{d}x}{x\sqrt{4x^2 + 9}}.$

解 这个积分不能在表中直接查到,需要先进行变量代换.

令 $2x = u$ ，那么 $\sqrt{4x^2 + 9} = \sqrt{u^2 + 3^2}, x = \frac{u}{2}, \mathrm{d}x = \frac{1}{2} \mathrm{d}u.$ 于是

$$
\int \frac {\mathrm{d} x}{x \sqrt {4 x ^ {2} + 9}} = \int \frac {\frac {1}{2} \mathrm{d} u}{\frac {u}{2} \sqrt {u ^ {2} + 3 ^ {2}}} = \int \frac {\mathrm{d} u}{u \sqrt {u ^ {2} + 3 ^ {2}}}.
$$

被积函数中含有 $\sqrt{u^2 + 3^2}$，在积分表（六）中查到公式37

214

---

第五节 积分表的使用

$$
\int \frac {\mathrm{d} x}{x \sqrt {x ^ {2} + a ^ {2}}} = \frac {1}{a} \ln \frac {\sqrt {x ^ {2} + a ^ {2}} - a}{| x |} + C.
$$

现在 $a = 3, x$ 相当于 $u$, 于是

$$
\int \frac {\mathrm{d} u}{u \sqrt {u ^ {2} + 3 ^ {2}}} = \frac {1}{3} \ln \frac {\sqrt {u ^ {2} + 3 ^ {2}} - 3}{| u |} + C.
$$

再把 u=2x 代入, 最后得到

$$
\int \frac {\mathrm{d} x}{x \sqrt {4 x ^ {2} + 9}} = \int \frac {\mathrm{d} u}{u \sqrt {u ^ {2} + 3 ^ {2}}} = \frac {1}{3} \ln \frac {\sqrt {u ^ {2} + 3 ^ {2}} - 3}{| u |} + C = \frac {1}{3} \ln \frac {\sqrt {4 x ^ {2} + 9} - 3}{2 | x |} + C.
$$

最后,举一个用递推公式求积分的例子.

例 4 求  $\int \sin^{4}x dx$ .

解 在积分表(十一)中查到公式 95

$$
\int \sin^ {n} x \mathrm{d} x = - \frac {\sin^ {n - 1} x \cos x}{n} + \frac {n - 1}{n} \int \sin^ {n - 2} x \mathrm{d} x.
$$

利用这个公式可以使被积函数中正弦的幂次减少2次, 只要重复使用这个公式, 可以使正弦的幂次继续减少, 直到求出最后结果为止, 这种公式叫做递推公式.

现在 $n = 4$ ，于是

$$
\int \sin^ {4} x \mathrm{d} x = - \frac {\sin^ {3} x \cos x}{4} + \frac {3}{4} \int \sin^ {2} x \mathrm{d} x.
$$

对积分  $\int\sin^{2}x dx$  用公式 93

$$
\int \sin^ {2} x \mathrm{d} x = \frac {x}{2} - \frac {1}{4} \sin 2 x + C,
$$

从而所求积分为

$$
\int \sin^ {4} x \mathrm{d} x = - \frac {\sin^ {3} x \cos x}{4} + \frac {3}{4} \left(\frac {x}{2} - \frac {1}{4} \sin 2 x\right) + C.
$$

一般说来,查积分表可以节省计算积分的时间,但是,只有掌握了前面学过的基本积分方法才能灵活地使用积分表,而且对一些比较简单的积分,应用基本积分方法来计算比查表更快些,例如,对 $\int\sin^{2}x\cos^{3}xdx$ ,用代换u=sin x很快就可得到结果.所以,求积分时究竟是直接计算,还是查表,或是两者结合使用,应该作具体分析,不能一概而论.

在本章结束之前,我们还要指出:对初等函数来说,在其定义区间上,它的原函数一定存在,但原函数不一定都是初等函数,如

215

---

第四章 不定积分

$$
\int \mathrm{e} ^ {- x ^ {2}} \mathrm{d} x, \quad \int \frac {\sin x}{x} \mathrm{d} x, \quad \int \frac {\mathrm{d} x}{\ln x}, \quad \int \frac {\mathrm{d} x}{\sqrt {1 + x ^ {4}}},
$$

等等,它们的原函数就都不是初等函数.

## 习题 4-5

利用积分表计算下列不定积分:

1. $\int \frac{\mathrm{d}x}{\sqrt{4x^2 - 9}}.$

2. $\int \frac{1}{x^2 + 2x + 5} \, \mathrm{d}x.$

3. $\int \frac{\mathrm{d}x}{\sqrt{5 - 4x + x^2}}.$

4. $\int \sqrt{2x^2 + 9}\mathrm{d}x.$

5. $\int \sqrt{3x^2 - 2}\mathrm{d}x.$

6. $\int \mathrm{e}^{2x}\cos x\mathrm{d}x.$

7. $\int x\arcsin \frac{x}{2}\mathrm{d}x.$

8. $\int \frac{\mathrm{d}x}{(x^2 + 9)^2}$.

9. $\int \frac{\mathrm{d}x}{\sin^3 x}$.

10. $\int \mathrm{e}^{-2x}\sin 3x\mathrm{d}x.$

11.  $\int \sin 3x \sin 5x dx.$

12. $\int \ln^3 x\mathrm{d}x$

13. $\int \frac{1}{x^2(1 - x)}\mathrm{d}x.$

14. $\int \frac{\sqrt{x - 1}}{x}\mathrm{d}x.$

15. $\int \frac{1}{(1 + x^2)^2}\mathrm{d}x.$

16. $\int \frac{1}{x\sqrt{x^2 - 1}}\mathrm{d}x.$

17. $\int \frac{x}{(2 + 3x)^2}\mathrm{d}x.$

18. $\int \cos^6 x\mathrm{d}x$

19. $\int x^{2}\sqrt{x^{2} - 2}\mathrm{d}x.$

20. $\int \frac{1}{2 + 5\cos x}\mathrm{d}x.$

21. $\int \frac{\mathrm{d}x}{x^2\sqrt{2x - 1}}.$

22. $\int \sqrt{\frac{1 - x}{1 + x}}\mathrm{d}x.$

23. $\int \frac{x + 5}{x^2 - 2x - 1}\mathrm{d}x.$

24. $\int \frac{x\mathrm{d}x}{\sqrt{1 + x - x^2}}.$

25. $\int \frac{x^4}{25 + 4x^2}\mathrm{d}x.$

## 总习题四

1. 填空:

(1) $\int x^{3}e^{x}dx =$ \_\_\_\_;
(2) $\int \frac{x + 5}{x^2 - 6x + 13} \, \mathrm{d}x =$ \_\_\_\_.

2. 以下两题中给出了四个结论,从中选出一个正确的结论:

(1) 已知  $f'(x)=\frac{1}{x(1+2\ln x)}$ ，且  $f(1)=1$ ，则  $f(x)$  等于（）；

(A) $\ln (1 + 2\ln x) + 1$

(B) $\frac{1}{2} \ln (1 + 2 \ln x) + 1$

216

---

总习题四

(C) $\frac{1}{2} \ln (1 + 2 \ln x) + \frac{1}{2}$

(D) $2\ln (1 + 2\ln x) + 1$

(2) 在下列等式中, 正确的结果是().

(A) $\int f'(x)\mathrm{d}x = f(x)$

(B) $\int \mathrm{d}f(x) = f(x)$

(C) $\frac{\mathrm{d}}{\mathrm{d}x}\int f(x)\mathrm{d}x = f(x)$

(D) $\mathrm{d}\int f(x)\mathrm{d}x = f(x)$

3. 已知 $\frac{\sin x}{x}$ 是 $f(x)$ 的一个原函数, 求 $\int x^3 f'(x) \mathrm{d}x$.

4. 求下列不定积分(其中 a, b 为常数):

(1) $\int \frac{\mathrm{d}x}{\mathrm{e}^x - \mathrm{e}^{-x}};$

(2) $\int \frac{x}{(1 - x)^3} \, \mathrm{d}x$;

(3) $\int \frac{x^2}{a^6 - x^6} \, \mathrm{d}x (a > 0)$;

(4) $\int \frac{1 + \cos x}{x + \sin x} \, \mathrm{d}x$;

(5) $\int \frac{\ln\ln x}{x}\mathrm{d}x;$

(6) $\int \frac{\sin x\cos x}{1 + \sin^4x}\mathrm{d}x;$

(7) $\int \tan^4 x\mathrm{d}x;$

(8) $\int \sin x\sin 2x\sin 3xdx;$

(9) $\int \frac{\mathrm{d}x}{x(x^6 + 4)}$;

(10) $\int \sqrt{\frac{a + x}{a - x}}\mathrm{d}x (a > 0);$

(11) $\int \frac{\mathrm{d}x}{\sqrt{x(1 + x)}};$

(12) $\int x\cos^2 x\mathrm{d}x$;

(13) $\int \mathrm{e}^{ax}\cos bx\mathrm{d}x;$

(14) $\int \frac{\mathrm{d}x}{\sqrt{1 + \mathrm{e}^x}};$

(15) $\int \frac{\mathrm{d}x}{x^2\sqrt{x^2 - 1}};$

(16) $\int \frac{\mathrm{d}x}{\left(a^2 - x^2\right)^{5 / 2}};$

(17) $\int \frac{\mathrm{d}x}{x^4\sqrt{1 + x^2}};$

(18) $\int \sqrt{x} \sin \sqrt{x} \, \mathrm{d}x$;

(19) $\int \ln (1 + x^2)\mathrm{d}x;$

(20) $\int \frac{\sin^2 x}{\cos^3 x} \, \mathrm{d}x$;

(21) $\int \arctan \sqrt{x} \, \mathrm{d}x$;

(22) $\int \frac{\sqrt{1 + \cos x}}{\sin x} \, \mathrm{d}x$;

(23) $\int \frac{x^3}{(1 + x^8)^2}\mathrm{d}x;$

(24) $\int \frac{x^{11}}{x^8 + 3x^4 + 2}\mathrm{d}x;$

(25) $\int\frac{dx}{16-x^{4}};$

(26) $\int \frac{\sin x}{1 + \sin x} \, \mathrm{d}x$;

(27) $\int \frac{x + \sin x}{1 + \cos x} \, \mathrm{d}x$;

(28) $\int \mathrm{e}^{\sin x}\frac{x\cos^3x - \sin x}{\cos^2x}\mathrm{d}x;$

(29) $\int \frac{\sqrt[3]{x}}{x(\sqrt{x} + \sqrt[3]{x})}\mathrm{d}x;$

(30) $\int \frac{\mathrm{d}x}{\left(1 + \mathrm{e}^x\right)^2}$;

(31) $\int \frac{\mathrm{e}^{3x} + \mathrm{e}^x}{\mathrm{e}^{4x} - \mathrm{e}^{2x} + 1}\mathrm{d}x;$

(32) $\int \frac{x\mathrm{e}^x}{(\mathrm{e}^x + 1)^2}\mathrm{d}x;$

(33) $\int \ln^2 (x + \sqrt{1 + x^2})\mathrm{d}x;$

(34) $\int \frac{\ln x}{(1 + x^2)^{\frac{3}{2}}}\mathrm{d}x;$

(35) $\int \sqrt{1 - x^2}\arcsin x\mathrm{d}x;$

(36) $\int \frac{x^3\arccos x}{\sqrt{1 - x^2}}\mathrm{d}x;$

(37) $\int \frac{\cot x}{1 + \sin x} \, \mathrm{d}x$;

(38) $\int \frac{\mathrm{d}x}{\sin^3 x \cos x}$;

(39) $\int \frac{\mathrm{d}x}{(2 + \cos x)\sin x};$

(40) $\int \frac{\sin x\cos x}{\sin x + \cos x}\mathrm{d}x.$

217

---

第四章 不定积分

![](../../raw/pages_0225-0256/images/page_234_image_1.jpg)

第四章释疑解难

218
