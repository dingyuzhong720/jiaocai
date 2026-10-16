称为菲涅耳(Fresnel)积分,在光学中有重要应用.

(1) 证明: $S(x)$ 为奇函数;
(2) 求出  $S(x)$  的极小值点.

17. 设 $f(x)$ 在 $[0, +\infty)$ 内连续，且 $\lim_{x \to +\infty} f(x) = 1$。证明函数

$$
y = \mathrm{e} ^ {- x} \int_ {0} ^ {x} \mathrm{e} ^ {t} f (t) \mathrm{d} t
$$

满足方程 $\frac{dy}{dx}+y=f(x)$ ，并求 $\lim_{x\to+\infty}y(x)$ .

## 第三节 定积分的换元法和分部积分法

由上节结果知道,计算定积分 $\int_{a}^{b}f(x)\mathrm{d}x$ 的简便方法是把它转化为求 $f(x)$ 的原函数的增量.在第四章中,我们知道用换元积分法和分部积分法可以求出一些函数的原函数.因此,在一定条件下,可以用换元积分法和分部积分法来计算定积分.下面就来讨论定积分的这两种计算方法.

## 一、定积分的换元法

为了说明如何用换元法来计算定积分,先证明下面的定理:

定理 设函数 $f(x)$ 在区间 $[a, b]$ 上连续，函数 $x = \varphi(t)$ 满足条件:

(1)  $\varphi(\alpha)=a,\varphi(\beta)=b;$
(2) $\varphi(t)$ 在 $[\alpha, \beta]$ （或 $[\beta, \alpha]$）上具有连续导数，且其值域 $R_{\varphi} = [a, b]$ ①，则有

$$
\int_ {a} ^ {b} f (x) \mathrm{d} x = \int_ {\alpha} ^ {\beta} f [ \varphi (t) ] \varphi^ {\prime} (t) \mathrm{d} t. \tag {3-1}
$$

公式(3-1)叫做定积分的换元公式.

证 由假设可以知道,上式两端的被积函数都是连续的,因此不仅上式两端的定积分都存在,而且由上节的定理2知道,被积函数的原函数也都存在.所以,(3-1)式两端的定积分都可应用牛顿-莱布尼茨公式.假设 $F(x)$ 是 $f(x)$ 的一个原函数,则

$$
\int_ {a} ^ {b} f (x) \mathrm{d} x = F (b) - F (a).
$$

另一方面，记 $\Phi(t) = F[\varphi(t)]$ ，它是由 $F(x)$ 与 $x = \varphi(t)$ 复合而成的函数.由复合函数求导法则，得

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 当 $\varphi(t)$ 的值域 $R_{\varphi}$ 超出 $[a, b]$，但 $\varphi(t)$ 满足其余条件时，只要 $f(x)$ 在 $R_{\varphi}$ 上连续，定理的结论仍成立.</span></small>

$$
\Phi^ {\prime} (t) = \frac {\mathrm{d} F}{\mathrm{d} x} \cdot \frac {\mathrm{d} x}{\mathrm{d} t} = f (x) \varphi^ {\prime} (t) = f [ \varphi (t) ] \varphi^ {\prime} (t).
$$

这表明 $\Phi(t)$ 是 $f[\varphi(t)]\varphi'(t)$ 的一个原函数.因此有

$$
\int_ {\alpha} ^ {\beta} f [ \varphi (t) ] \varphi^ {\prime} (t) \mathrm{d} t = \Phi (\beta) - \Phi (\alpha).
$$

又由 $\Phi(t) = F[\varphi(t)]$ 及 $\varphi(\alpha) = a, \varphi(\beta) = b$ 可知

$$
\Phi (\beta) - \Phi (\alpha) = F [ \varphi (\beta) ] - F [ \varphi (\alpha) ] = F (b) - F (a).
$$

所以

$$
\int_ {a} ^ {b} f (x) \mathrm{d} x = F (b) - F (a) = \Phi (\beta) - \Phi (\alpha) = \int_ {\alpha} ^ {\beta} f [ \varphi (t) ] \varphi^ {\prime} (t) \mathrm{d} t.
$$

这就证明了换元公式.

在定积分 $\int_{a}^{b}f(x)\mathrm{d}x$ 中的 $\mathrm{dx}$ ，本来是整个定积分记号中不可分割的一部分，但由上述定理可知，在一定条件下，它确实可以作为微分记号来对待.这就是说，应用换元公式时，如果把 $\int_{a}^{b}f(x)\mathrm{d}x$ 中的 $x$ 换成 $\varphi (t)$ ，那么 $\mathrm{dx}$ 就换成 $\varphi '(t)\mathrm{d}t$ ，这正好是 $x = \varphi (t)$ 的微分 $\mathrm{dx}$

应用换元公式时有两点值得注意:（1）用 $x = \varphi(t)$ 把原来变量 $x$ 代换成新变量 $t$ 时，积分限也要换成相应于新变量 $t$ 的积分限；（2）求出 $f[\varphi(t)]\varphi'(t)$ 的一个原函数 $\Phi(t)$ 后，不必像计算不定积分那样再要把 $\Phi(t)$ 变换成原来变量 $x$ 的函数，而只要把新变量 $t$ 的上、下限分别代入 $\Phi(t)$ 中然后相减就行了.

例1 计算 $\int_0^a\sqrt{a^2 - x^2}\mathrm{d}x$ （ $a > 0$ ）.

解 设  $x = a \sin t$ ，则  $dx = a \cos t dt$ ，

当 $x = 0$ 时，取 $t = 0$；当 $x = a$ 时，取 $t = \frac{\pi}{2}$.

于是

$$
\begin{array}{l} \int_ {0} ^ {a} \sqrt {a ^ {2} - x ^ {2}} \mathrm{d} x = a ^ {2} \int_ {0} ^ {\frac {\pi}{2}} \cos^ {2} t \mathrm{d} t = \frac {a ^ {2}}{2} \int_ {0} ^ {\frac {\pi}{2}} (1 + \cos 2 t) \mathrm{d} t \\ = \frac {a ^ {2}}{2} \left[ t + \frac {1}{2} \sin 2 t \right] _ {0} ^ {\frac {\pi}{2}} = \frac {\pi a ^ {2}}{4}. \\ \end{array}
$$

换元公式也可反过来使用.为使用方便起见,把换元公式中左、右两端对调位置,同时把 t 改记为 x,而 x 改记为 t,得

$$
\int_ {a} ^ {b} f \left[ \varphi (x) \right] \varphi^ {\prime} (x) \mathrm{d} x = \int_ {\alpha} ^ {\beta} f (t) \mathrm{d} t.
$$

这样,我们可用  $t=\varphi(x)$  来引入新变量 t, 而  $\alpha=\varphi(a)$ ,  $\beta=\varphi(b)$ .

例2 计算 $\int_0^{\frac{\pi}{2}}\cos^5 x\sin x\mathrm{d}x.$

解 设 $t = \cos x$ ，则 $\mathrm{dt} = -\sin x\mathrm{dx}$ ，且

$$
\text {当} x = 0 \text {时,} t = 1; \quad \text {当} x = \frac {\pi}{2} \text {时,} t = 0.
$$

于是

$$
\int_ {0} ^ {\frac {\pi}{2}} \cos^ {5} x \sin x \mathrm{d} x = - \int_ {1} ^ {0} t ^ {5} \mathrm{d} t = \int_ {0} ^ {1} t ^ {5} \mathrm{d} t = \left[ \frac {t ^ {6}}{6} \right] _ {0} ^ {1} = \frac {1}{6}.
$$

在例 2 中, 如果我们不明显地写出新变量 t, 那么定积分的上、下限就不要变更. 现在用这种记法写出计算过程如下:

$$
\int_ {0} ^ {\frac {\pi}{2}} \cos^ {5} x \sin x \mathrm{d} x = - \int_ {0} ^ {\frac {\pi}{2}} \cos^ {5} x \mathrm{d} (\cos x) = - \left[ \frac {\cos^ {6} x}{6} \right] _ {0} ^ {\frac {\pi}{2}} = - \left(0 - \frac {1}{6}\right) = \frac {1}{6}.
$$

例3 计算 $\int_0^\pi \sqrt{\sin^3 x - \sin^5 x} \, \mathrm{d}x.$

解 由于 $\sqrt{\sin^3 x - \sin^5 x} = \sqrt{\sin^3 x(1 - \sin^2 x)} = \sin^{\frac{3}{2}}x\cdot |\cos x|$，在 $\left[0,\frac{\pi}{2}\right]$ 上，$|\cos x| = \cos x$；在 $\left[\frac{\pi}{2},\pi\right]$ 上，$|\cos x| = -\cos x$，所以

$$
\begin{array}{l} \int_ {0} ^ {\pi} \sqrt {\sin^ {3} x - \sin^ {5} x} \mathrm{d} x = \int_ {0} ^ {\frac {\pi}{2}} \sin^ {\frac {3}{2}} x \cos x \mathrm{d} x + \int_ {\frac {\pi}{2}} ^ {\pi} \sin^ {\frac {3}{2}} x (- \cos x) \mathrm{d} x \\ = \int_ {0} ^ {\frac {\pi}{2}} \sin^ {\frac {3}{2}} x \mathrm{d} (\sin x) - \int_ {\frac {\pi}{2}} ^ {\pi} \sin^ {\frac {3}{2}} x \mathrm{d} (\sin x) \\ = \left[ \frac {2}{5} \sin^ {\frac {5}{2}} x \right] _ {0} ^ {\frac {\pi}{2}} - \left[ \frac {2}{5} \sin^ {\frac {5}{2}} x \right] _ {\frac {\pi}{2}} ^ {\pi} \\ = \frac {2}{5} - \left(- \frac {2}{5}\right) = \frac {4}{5}. \\ \end{array}
$$

注意 如果忽略 $\cos x$ 在 $\left[\frac{\pi}{2},\pi\right]$ 上非正, 而按 $\sqrt{\sin^3x - \sin^5x} = \sin^{\frac{3}{2}}x\cos x$ 计算, 将导致错误.

例4 计算 $\int_0^4\frac{x + 2}{\sqrt{2x + 1}}\mathrm{d}x.$

解 设 $\sqrt{2x + 1} = t$，则 $x = \frac{t^2 - 1}{2}, \mathrm{d}x = t\mathrm{d}t$，且

$$
\text {当} x = 0 \text {时,} t = 1; \quad \text {当} x = 4 \text {时,} t = 3.
$$

于是

$$
\begin{array}{l} \int_ {0} ^ {4} \frac {x + 2}{\sqrt {2 x + 1}} \mathrm{d} x = \int_ {1} ^ {3} \frac {\frac {t ^ {2} - 1}{2} + 2}{t} t \mathrm{d} t = \frac {1}{2} \int_ {1} ^ {3} (t ^ {2} + 3) \mathrm{d} t \\ = \frac {1}{2} \left[ \frac {t ^ {3}}{3} + 3 t \right] _ {1} ^ {3} = \frac {1}{2} \left[ \left(\frac {2 7}{3} + 9\right) - \left(\frac {1}{3} + 3\right) \right] = \frac {2 2}{3}. \\ \end{array}
$$

例 5 证明:

(1) 若  $f(x)$  在  $[-a, a]$  上连续且为偶函数, 则

$$
\int_ {- a} ^ {a} f (x) \mathrm{d} x = 2 \int_ {0} ^ {a} f (x) \mathrm{d} x;
$$

(2) 若  $f(x)$  在  $[-a, a]$  上连续且为奇函数，则

$$
\int_ {- a} ^ {a} f (x) \mathrm{d} x = 0.
$$

证 因为

$$
\int_ {- a} ^ {a} f (x) \mathrm{d} x = \int_ {- a} ^ {0} f (x) \mathrm{d} x + \int_ {0} ^ {a} f (x) \mathrm{d} x,
$$

对积分 $\int_{-a}^{0}f(x)\mathrm{d}x$ 作代换 $x = -t$ ，则得

$$
\int_ {- a} ^ {0} f (x) \mathrm{d} x = - \int_ {a} ^ {0} f (- t) \mathrm{d} t = \int_ {0} ^ {a} f (- t) \mathrm{d} t = \int_ {0} ^ {a} f (- x) \mathrm{d} x,
$$

于是

$$
\int_ {- a} ^ {a} f (x) \mathrm{d} x = \int_ {0} ^ {a} f (- x) \mathrm{d} x + \int_ {0} ^ {a} f (x) \mathrm{d} x = \int_ {0} ^ {a} [ f (x) + f (- x) ] \mathrm{d} x.
$$

(1) 若  $f(x)$  为偶函数, 则

$$
f (x) + f (- x) = 2 f (x),
$$

从而

$$
\int_ {- a} ^ {a} f (x) \mathrm{d} x = 2 \int_ {0} ^ {a} f (x) \mathrm{d} x.
$$

(2) 若  $f(x)$  为奇函数, 则

$$
f (x) + f (- x) = 0,
$$

从而

$$
\int_ {- a} ^ {a} f (x) \mathrm{d} x = 0.
$$

利用例 5 的结论, 常可简化计算偶函数、奇函数在对称于原点的区间上的定积分.

例6 设 $f(x)$ 在 $[0,1]$ 上连续，证明:

(1) $\int_{0}^{\frac{\pi}{2}} f(\sin x) \, \mathrm{d}x = \int_{0}^{\frac{\pi}{2}} f(\cos x) \, \mathrm{d}x$;

(2) $\int_{0}^{\pi} x f(\sin x) \, \mathrm{d}x = \frac{\pi}{2} \int_{0}^{\pi} f(\sin x) \, \mathrm{d}x$，由此计算

$$
\int_ {0} ^ {\pi} \frac {x \sin x}{1 + \cos^ {2} x} \mathrm{d} x.
$$

证（1）设 $x = \frac{\pi}{2} - t$，则 $\mathrm{dx} = -\mathrm{dt}$，且

当 $x = 0$ 时，$t = \frac{\pi}{2}$；当 $x = \frac{\pi}{2}$ 时，$t = 0$.

于是

$$
\int_ {0} ^ {\frac {\pi}{2}} f (\sin x) \mathrm{d} x = - \int_ {\frac {\pi}{2}} ^ {0} f \left[ \sin \left(\frac {\pi}{2} - t\right) \right] \mathrm{d} t = \int_ {0} ^ {\frac {\pi}{2}} f (\cos t) \mathrm{d} t = \int_ {0} ^ {\frac {\pi}{2}} f (\cos x) \mathrm{d} x.
$$

(2) 设  $x=\pi-t$ ，则 dx=-dt，且

当 x=0 时, $t=\pi$ ; 当  $x=\pi$  时, t=0.

于是

$$
\begin{array}{l} \int_ {0} ^ {\pi} x f (\sin x) \mathrm{d} x = - \int_ {\pi} ^ {0} (\pi - t) f [ \sin (\pi - t) ] \mathrm{d} t = \int_ {0} ^ {\pi} (\pi - t) f (\sin t) \mathrm{d} t \\ = \pi \int_ {0} ^ {\pi} f (\sin t) \mathrm{d} t - \int_ {0} ^ {\pi} t f (\sin t) \mathrm{d} t = \pi \int_ {0} ^ {\pi} f (\sin x) \mathrm{d} x - \int_ {0} ^ {\pi} x f (\sin x) \mathrm{d} x, \\ \end{array}
$$

所以

$$
\int_ {0} ^ {\pi} x f (\sin x) \mathrm{d} x = \frac {\pi}{2} \int_ {0} ^ {\pi} f (\sin x) \mathrm{d} x.
$$

利用上述结论,即得

$$
\begin{array}{l} \int_ {0} ^ {\pi} \frac {x \sin x}{1 + \cos^ {2} x} \mathrm{d} x = \frac {\pi}{2} \int_ {0} ^ {\pi} \frac {\sin x}{1 + \cos^ {2} x} \mathrm{d} x = - \frac {\pi}{2} \int_ {0} ^ {\pi} \frac {\mathrm{d} (\cos x)}{1 + \cos^ {2} x} \\ = - \frac {\pi}{2} [ \arctan (\cos x) ] _ {0} ^ {\pi} = - \frac {\pi}{2} \left(- \frac {\pi}{4} - \frac {\pi}{4}\right) = \frac {\pi^ {2}}{4}. \\ \end{array}
$$

例 7 设  $f(x)$  是连续的周期函数, 周期为 T, 证明:

(1) $\int_{a}^{a + T}f(x)\mathrm{d}x = \int_{0}^{T}f(x)\mathrm{d}x;$

(2) $\int_{a}^{a + nT}f(x)\mathrm{d}x = n\int_{0}^{T}f(x)\mathrm{d}x (n\in \mathbf{N})$ ，由此计算

$$
\int_ {0} ^ {n \pi} \sqrt {1 + \sin 2 x}   \mathrm{d} x.
$$

证 (1) 记 $\Phi(a) = \int_{a}^{a + T} f(x) \, \mathrm{d}x$，则

$$
\Phi^ {\prime} (a) = \left[ \int_ {0} ^ {a + T} f (x) \mathrm{d} x - \int_ {0} ^ {a} f (x) \mathrm{d} x \right] ^ {\prime} = f (a + T) - f (a) = 0,
$$

知 $\Phi(a)$ 与 $a$ 无关, 因此 $\Phi(a)=\Phi(0)$, 即

$$
\int_ {a} ^ {a + T} f (x) \mathrm{d} x = \int_ {0} ^ {T} f (x) \mathrm{d} x.
$$

(2) $\int_{a}^{a + nT}f(x)\mathrm{d}x = \sum_{k = 0}^{n - 1}\int_{a + kT}^{a + kT + T}f(x)\mathrm{d}x$ ，由（1）知

$$
\int_ {a + k T} ^ {a + k T + T} f (x) \mathrm{d} x = \int_ {0} ^ {T} f (x) \mathrm{d} x,
$$

因此

$$
\int_ {a} ^ {a + n T} f (x) \mathrm{d} x = n \int_ {0} ^ {T} f (x) \mathrm{d} x.
$$

由于 $\sqrt{1 + \sin 2x}$ 是以 $\pi$ 为周期的周期函数, 利用上述结论, 有

$$
\begin{array}{l} \int_ {0} ^ {n \pi} \sqrt {1 + \sin 2 x} \mathrm{d} x = n \int_ {0} ^ {\pi} \sqrt {1 + \sin 2 x} \mathrm{d} x = n \int_ {0} ^ {\pi} | \sin x + \cos x | \mathrm{d} x \\ = \sqrt {2} n \int_ {0} ^ {\pi} \left| \sin \left(x + \frac {\pi}{4}\right) \right| \mathrm{d} x = \sqrt {2} n \int_ {\frac {\pi}{4}} ^ {\frac {5 \pi}{4}} | \sin t | \mathrm{d} t \\ = \sqrt {2} n \int_ {0} ^ {\pi} | \sin t | \mathrm{d} t = \sqrt {2} n \int_ {0} ^ {\pi} \sin t \mathrm{d} t = 2 \sqrt {2} n. \\ \end{array}
$$

例8 计算 $\int_0^3\frac{x^2}{(x^2 - 3x + 3)^2}\mathrm{d}x.$

解 因 $x^{2} - 3x + 3 = \left(x - \frac{3}{2}\right)^{2} + \frac{3}{4}$, 令 $x - \frac{3}{2} = \frac{\sqrt{3}}{2} \tan u\left(|u| < \frac{\pi}{2}\right)$, 则

$$
(x ^ {2} - 3 x + 3) ^ {2} = \left(\frac {3}{4} \sec^ {2} u\right) ^ {2} = \frac {9}{1 6} \sec^ {4} u, \mathrm{d} x = \frac {\sqrt {3}}{2} \sec^ {2} u \mathrm{d} u.
$$

当 $x = 0$ 时, $u = -\frac{\pi}{3}$; $x = 3$ 时, $u = \frac{\pi}{3}$.

于是

$$
\begin{array}{l} \int_ {0} ^ {3} \frac {x ^ {2}}{(x ^ {2} - 3 x + 3) ^ {2}} \mathrm{d} x = \int_ {- \frac {\pi}{3}} ^ {\frac {\pi}{3}} \left(\frac {3}{4} \tan^ {2} u + \frac {3 \sqrt {3}}{2} \tan u + \frac {9}{4}\right) \cdot \frac {1 6}{9} \cdot \frac {\sqrt {3}}{2} \cos^ {2} u \mathrm{d} u \\ = \frac {8}{3 \sqrt {3}} \cdot 2 \int_ {0} ^ {\frac {\pi}{3}} \left(\frac {3}{4} \tan^ {2} u + \frac {9}{4}\right) \cos^ {2} u \mathrm{d} u \\ = \frac {4}{\sqrt {3}} \int_ {0} ^ {\frac {\pi}{3}} (\sin^ {2} u + 3 \cos^ {2} u) \mathrm{d} u = \frac {4}{\sqrt {3}} \int_ {0} ^ {\frac {\pi}{3}} (2 + \cos 2 u) \mathrm{d} u \\ = \frac {4}{\sqrt {3}} \left[ 2 u + \frac {1}{2} \sin 2 u \right] _ {0} ^ {\frac {\pi}{3}} = \frac {8 \pi}{3 \sqrt {3}} + 1. \\ \end{array}
$$

例9 设函数

$$
f (x) = \left\{ \begin{array}{l l} \frac {1}{1 + \cos x}, & - \pi <   x <   0, \\ x \mathrm{e} ^ {- x ^ {2}}, & x \geqslant 0, \end{array} \right.
$$

计算 $\int_{1}^{4}f(x - 2)\mathrm{d}x.$

解 设 x-2=t，则 dx=dt，且

$$
\text {当} x = 1 \text {时,} t = - 1; \quad \text {当} x = 4 \text {时,} t = 2.
$$

于是

$$
\begin{array}{l} \int_ {1} ^ {4} f (x - 2) \mathrm{d} x = \int_ {- 1} ^ {2} f (t) \mathrm{d} t = \int_ {- 1} ^ {0} \frac {\mathrm{d} t}{1 + \cos t} + \int_ {0} ^ {2} t \mathrm{e} ^ {- t ^ {2}} \mathrm{d} t \\ = \left[ \tan \frac {t}{2} \right] _ {- 1} ^ {0} - \left[ \frac {1}{2} \mathrm{e} ^ {- t ^ {2}} \right] _ {0} ^ {2} = \tan \frac {1}{2} - \frac {1}{2} \mathrm{e} ^ {- 4} + \frac {1}{2}. \\ \end{array}
$$

## 二、定积分的分部积分法

依据不定积分的分部积分法, 若  $u(x)$ ,  $v(x)$  在  $[a, b]$  上具有连续导数, 则

$$
\begin{array}{l} \int_ {a} ^ {b} u (x) v ^ {\prime} (x) \mathrm{d} x = \left[ \int u (x) v ^ {\prime} (x) \mathrm{d} x \right] _ {a} ^ {b} = \left[ u (x) v (x) - \int v (x) u ^ {\prime} (x) \mathrm{d} x \right] _ {a} ^ {b} \\ = [ u (x) v (x) ] _ {a} ^ {b} - \int_ {a} ^ {b} v (x) u ^ {\prime} (x) \mathrm{d} x, \tag {3-2} \\ \end{array}
$$

简记作

$$
\int_ {a} ^ {b} u v ^ {\prime} \mathrm{d} x = [ u v ] _ {a} ^ {b} - \int_ {a} ^ {b} v u ^ {\prime} \mathrm{d} x,
$$

或

$$
\int_ {a} ^ {b} u \mathrm{d} v = [ u v ] _ {a} ^ {b} - \int_ {a} ^ {b} v \mathrm{d} u.
$$

公式(3-2)叫做定积分的分部积分公式.公式表明原函数已经积出的部分可以先用上、下限代入.

例10 计算 $\int_0^{\frac{1}{2}}\arcsin x\mathrm{d}x.$

解 $\int_0^{\frac{1}{2}}\arcsin x\mathrm{d}x = [x\arcsin x]^{\frac{1}{2}}_0 - \int_0^{\frac{1}{2}}\frac{x}{\sqrt{1 - x^2}}\mathrm{d}x$

$$
= \frac {1}{2} \cdot \frac {\pi}{6} + \left[ \sqrt {1 - x ^ {2}} \right] _ {0} ^ {\frac {1}{2}} = \frac {\pi}{1 2} + \frac {\sqrt {3}}{2} - 1.
$$

例11 计算 $\int_0^1\mathrm{e}^{\sqrt{x}}\mathrm{d}x.$

解 先用换元法. 令 $\sqrt{x} = t$，则 $x = t^2, \mathrm{d}x = 2t\mathrm{d}t$，且

当 $x = 0$ 时，$t = 0$；当 $x = 1$ 时，$t = 1$.

于是

$$
\begin{array}{l} \int_ {0} ^ {1} \mathrm{e} ^ {\sqrt {x}} \mathrm{d} x = 2 \int_ {0} ^ {1} t \mathrm{e} ^ {t} \mathrm{d} t = 2 \int_ {0} ^ {1} t \mathrm{d} (\mathrm{e} ^ {t}) = 2 \left(\left[ t \mathrm{e} ^ {t} \right] _ {0} ^ {1} - \int_ {0} ^ {1} \mathrm{e} ^ {t} \mathrm{d} t\right) \\ = 2 (\mathrm{e} - [ \mathrm{e} ^ {t} ] _ {0} ^ {1}) = 2 [ \mathrm{e} - (\mathrm{e} - 1) ] = 2. \\ \end{array}
$$

例 12 证明定积分公式(见附录Ⅳ积分表公式 147):

$$
\begin{array}{l} I _ {n} = \int_ {0} ^ {\frac {\pi}{2}} \sin^ {n} x \mathrm{d} x \left(= \int_ {0} ^ {\frac {\pi}{2}} \cos^ {n} x \mathrm{d} x\right) \\ = \left\{ \begin{array}{l l} \frac {n - 1}{n} \cdot \frac {n - 3}{n - 2} \cdot \dots \cdot \frac {3}{4} \cdot \frac {1}{2} \cdot \frac {\pi}{2}, & n \text {为正偶数,} \\ \frac {n - 1}{n} \cdot \frac {n - 3}{n - 2} \cdot \dots \cdot \frac {4}{5} \cdot \frac {2}{3}, & n \text {为大于1的正奇数.} \end{array} \right. \\ \end{array}
$$

证 $I_{n} = -\int_{0}^{\frac{\pi}{2}}\sin^{n - 1}x\mathrm{d}(\cos x)$

$$
= \left[ - \cos x \sin^ {n - 1} x \right] _ {0} ^ {\frac {\pi}{2}} + (n - 1) \int_ {0} ^ {\frac {\pi}{2}} \sin^ {n - 2} x \cos^ {2} x \mathrm{d} x.
$$

右端第一项等于零；将第二项里的  $\cos^{2}x$  写成  $1-\sin^{2}x$ ，并把积分分成两个，得

$$
I _ {n} = (n - 1) \int_ {0} ^ {\frac {\pi}{2}} \sin^ {n - 2} x \mathrm{d} x - (n - 1) \int_ {0} ^ {\frac {\pi}{2}} \sin^ {n} x \mathrm{d} x = (n - 1) I _ {n - 2} - (n - 1) I _ {n},
$$

由此得

$$
I _ {n} = \frac {n - 1}{n} I _ {n - 2}.
$$

这个等式叫做积分  $I_{n}$  关于下标的递推公式.

如果把 n 换成 n-2, 那么得

$$
I _ {n - 2} = \frac {n - 3}{n - 2} I _ {n - 4}.
$$

同样地依次进行下去,直到 $I_{n}$ 的下标递减到0或1为止.于是,

$$
\begin{array}{l} I _ {2 m} = \frac {2 m - 1}{2 m} \cdot \frac {2 m - 3}{2 m - 2} \cdot \dots \cdot \frac {5}{6} \cdot \frac {3}{4} \cdot \frac {1}{2} I _ {0}, \\ I _ {2 m + 1} = \frac {2 m}{2 m + 1} \cdot \frac {2 m - 2}{2 m - 1} \cdot \dots \cdot \frac {6}{7} \cdot \frac {4}{5} \cdot \frac {2}{3} I _ {1} \quad (m = 1, 2, \dots), \\ \end{array}
$$

而

$$
I _ {0} = \int_ {0} ^ {\frac {\pi}{2}} \mathrm{d} x = \frac {\pi}{2}, \quad I _ {1} = \int_ {0} ^ {\frac {\pi}{2}} \sin x \mathrm{d} x = 1,
$$

因此

$$
I _ {2 m} = \frac {2 m - 1}{2 m} \cdot \frac {2 m - 3}{2 m - 2} \cdot \dots \cdot \frac {5}{6} \cdot \frac {3}{4} \cdot \frac {1}{2} \cdot \frac {\pi}{2},
$$

$$
I _ {2 m + 1} = \frac {2 m}{2 m + 1} \cdot \frac {2 m - 2}{2 m - 1} \cdot \dots \cdot \frac {6}{7} \cdot \frac {4}{5} \cdot \frac {2}{3} \quad (m = 1, 2, \dots).
$$

至于定积分 $\int_0^{\frac{\pi}{2}}\cos^n x\mathrm{d}x$ 与 $\int_0^{\frac{\pi}{2}}\sin^n x\mathrm{d}x$ 相等，由本节例6(1）即可知道，证毕.

## 习题 5-3

1. 计算下列定积分:

(1) $\int_{\frac{\pi}{3}}^{\pi}\sin \left(x + \frac{\pi}{3}\right)\mathrm{d}x;$

(2) $\int_{-2}^{1}\frac{\mathrm{d}x}{(11 + 5x)^3};$

(3) $\int_{0}^{\frac{\pi}{2}}\sin \varphi \cos^{3}\varphi \mathrm{d}\varphi$

(4) $\int_0^\pi (1 - \sin^3\theta)\mathrm{d}\theta$

(5) $\int_{\frac{\pi}{6}}^{\frac{\pi}{2}}\cos^2 u\mathrm{d}u;$

(6) $\int_0^{\sqrt{2}}\sqrt{2 - x^2}\mathrm{d}x;$

(7) $\int_{-\sqrt{2}}^{\sqrt{2}}\sqrt{8 - 2y^2}\mathrm{d}y;$

(8) $\int_{\frac{1}{\sqrt{2}}}\frac{\sqrt{1 - x^2}}{x^2}\mathrm{d}x;$

(9) $\int_{0}^{a} x^{2} \sqrt{a^{2} - x^{2}} \, \mathrm{d}x (a > 0)$;

(10) $\int_{1}^{\sqrt{3}}\frac{\mathrm{d}x}{x^2\sqrt{1 + x^2}};$

(11) $\int_{-1}^{1}\frac{x\mathrm{d}x}{\sqrt{5 - 4x}};$

(12) $\int_{1}^{4}\frac{\mathrm{d}x}{1 + \sqrt{x}};$

(13) $\int_{\frac{3}{4}}^{1}\frac{\mathrm{d}x}{\sqrt{1 - x} - 1};$

(14) $\int_0^{\sqrt{2a}}\frac{x\mathrm{d}x}{\sqrt{3a^2 - x^2}} (a > 0);$

(15) $\int_0^1 t\mathrm{e}^{-\frac{t^2}{2}}\mathrm{d}t;$

(16) $\int_{1}^{\mathrm{e}^2}\frac{\mathrm{d}x}{x\sqrt{1 + \ln x}};$

(17) $\int_{-2}^{0}\frac{(x+2)\mathrm{d}x}{x^{2}+2x+2};$

(18) $\int_0^2\frac{x\mathrm{d}x}{(x^2 - 2x + 2)^2};$

(19) $\int_{-\pi}^{\pi} x^4 \sin x \, \mathrm{d}x$;

(20) $\int_{-\frac{\pi}{2}}^{\frac{\pi}{2}} 4\cos^{4}\theta \mathrm{d}\theta$;

(21) $\int_{-\frac{1}{2}}^{\frac{1}{2}}\frac{(\arcsin x)^{2}}{\sqrt{1 - x^{2}}}\mathrm{d}x;$

(22) $\int_{-5}^{5}\frac{x^3\sin^2x}{x^4 + 2x^2 + 1}\mathrm{d}x;$

(23) $\int_{-\frac{\pi}{2}}^{\frac{\pi}{2}}\cos x\cos 2x\mathrm{d}x;$

(24) $\int_{-\frac{\pi}{2}}^{\frac{\pi}{2}}\sqrt{\cos x - \cos^3x}\mathrm{d}x;$

(25) $\int_0^\pi \sqrt{1 + \cos 2x} \, \mathrm{d}x$;

(26) $\int_{0}^{2\pi}|\sin (x + 1)|\mathrm{d}x.$

2. 设 $f(x)$ 在 $[a, b]$ 上连续，证明:

$$
\int_ {a} ^ {b} f (x) \mathrm{d} x = \int_ {a} ^ {b} f (a + b - x) \mathrm{d} x.
$$

3. 证明:$\int_{x}^{1}\frac{\mathrm{d}t}{1+t^2}=\int_{1}^{\frac{1}{x}}\frac{\mathrm{d}t}{1+t^2}\quad(x>0)$.

4. 证明: $\int_{0}^{1}x^{m}(1-x)^{n}\mathrm{d}x=\int_{0}^{1}x^{n}(1-x)^{m}\mathrm{d}x\quad(m,n\in\mathbf{N})$

5. 设 $f(x)$ 在 $[0,1]$ 上连续, $n \in \mathbb{Z}$, 证明:

$$
\int_ {\frac {n}{2} \pi} ^ {\frac {n + 1}{2} \pi} f (\mid \sin x \mid) \mathrm{d} x = \int_ {\frac {n}{2} \pi} ^ {\frac {n + 1}{2} \pi} f (\mid \cos x \mid) \mathrm{d} x = \int_ {0} ^ {\frac {\pi}{2}} f (\sin x) \mathrm{d} x.
$$

6. 若 $f(t)$ 是连续的奇函数, 证明 $\int_{0}^{x} f(t) \, \mathrm{d}t$ 是偶函数; 若 $f(t)$ 是连续的偶函数, 证明 $\int_{0}^{x} f(t) \, \mathrm{d}t$ 是奇函数.

7. 设 $x = \varphi(y)$ 是单调函数 $y = x\mathrm{e}^{x^2}$ 的反函数, 求 $\int_0^{\mathrm{e}}\varphi(y)\mathrm{d}y$.
8. 计算下列定积分:

(1) $\int_0^1 x\mathrm{e}^{-x}\mathrm{d}x;$

(2) $\int_{1}^{\mathrm{e}} x \ln x \, \mathrm{d}x$;

(3) $\int_{0}^{\frac{2\pi}{\omega}}t\sin\omega tdt(\omega$ 为常数);

(4) $\int_{\frac{\pi}{4}}^{\frac{\pi}{3}}\frac{x}{\sin^2x}\mathrm{d}x;$

(5) $\int_{1}^{4}\frac{\ln x}{\sqrt{x}}\mathrm{d}x;$

(6) $\int_0^1 x\arctan x\mathrm{d}x;$

(7) $\int_{0}^{\frac{\pi}{2}}\mathrm{e}^{2x}\cos x\mathrm{d}x;$

(8) $\int_{1}^{2} x \log_2 x \, \mathrm{d}x$;

(9) $\int_{0}^{\pi}(x\sin x)^{2}\mathrm{d}x;$

(10) $\int_{1}^{e}\sin (\ln x)\mathrm{d}x;$

(11) $\int_{\frac{1}{e}}^{e}|\ln x|dx;$

(12) $\int_0^1 (1 - x^2)^{\frac{m}{2}}\mathrm{d}x$ ($m\in \mathbf{N}_+$);

(13) $J_{m} = \int_{0}^{\pi}x\sin^{m}x\mathrm{d}x (m\in \mathbf{N}_{+}).$

## 第四节 反常积分

在一些实际问题中,常会遇到积分区间为无穷区间,或者被积函数为无界函数的积分,它们已经不属于前面所说的定积分了.因此,我们对定积分作如下两种推广,从而形成反常积分的概念.

## 一、无穷限的反常积分

设函数 $f(x)$ 在区间 $[a, +\infty)$ 上连续，任取 $t > a$ ，作定积分 $\int_{a}^{t}f(x)\mathrm{d}x$ ，再求极限:

$$
\lim _ {t \to + \infty} \int_ {a} ^ {t} f (x)   \mathrm{d} x, \tag {4-1}
$$

这个对变上限定积分的算式(4-1)称为函数 $f(x)$ 在无穷区间 $[a,+\infty)$ 上的反常积分，记为 $\int_{a}^{+\infty}f(x)\mathrm{d}x$ ，即

$$
\int_ {a} ^ {+ \infty} f (x) \mathrm{d} x = \lim _ {t \to + \infty} \int_ {a} ^ {t} f (x) \mathrm{d} x, \tag {$4-1^{\prime$}}
$$

根据算式(4-1)的结果是否存在,可引入反常积分 $\int_{a}^{+\infty}f(x)\mathrm{d}x$ 收敛与发散的定义如下:

定义1（1）设函数 $f(x)$ 在区间 $[a, +\infty)$ 上连续，如果极限(4-1)存在，那么称反常积分 $\int_{a}^{+\infty} f(x) \mathrm{d}x$ 收敛，并称此极限为该反常积分的值；如果极限(4-1)不存在，那么称反常积分 $\int_{a}^{+\infty} f(x) \mathrm{d}x$ 发散.

类似地，设函数 $f(x)$ 在区间 $(-\infty, b]$ 上连续，任取 $t < b$ ，算式

$$
\lim _ {t \to - \infty} \int_ {t} ^ {b} f (x) \mathrm{d} x \tag {4-2}
$$

称为函数 $f(x)$ 在无穷区间 $(- \infty, b]$ 上的反常积分，记为 $\int_{-\infty}^{b} f(x) \mathrm{d}x$ ，即

$$
\int_ {- \infty} ^ {b} f (x) \mathrm{d} x = \lim _ {t \to - \infty} \int_ {t} ^ {b} f (x) \mathrm{d} x. \tag {$4-2^{\prime$}}
$$

于是有

（2）设函数 $f(x)$ 在区间 $(- \infty, b]$ 上连续，如果极限(4-2)存在，那么称反常积分 $\int_{-\infty}^{b} f(x) \mathrm{d}x$ 收敛，并称此极限为该反常积分的值；如果极限(4-2)不存在，那么称反常积分 $\int_{-\infty}^{b} f(x) \mathrm{d}x$ 发散.

设函数 $f(x)$ 在区间 $(-\infty, +\infty)$ 上连续，反常积分 $\int_{-\infty}^{0} f(x) \mathrm{d}x$ 与反常积分 $\int_{0}^{+\infty} f(x) \mathrm{d}x$ 之和称为函数 $f(x)$ 在无穷区间 $(- \infty, +\infty)$ 上的反常积分，记为 $\int_{-\infty}^{+\infty} f(x) \mathrm{d}x$ 即

$$
\int_ {- \infty} ^ {+ \infty} f (x) \mathrm{d} x = \int_ {- \infty} ^ {0} f (x) \mathrm{d} x + \int_ {0} ^ {+ \infty} f (x) \mathrm{d} x. \tag {4-3}
$$

（3）设函数 $f(x)$ 在区间 $(-\infty, +\infty)$ 上连续，如果反常积分 $\int_{-\infty}^{0} f(x) \mathrm{d}x$ 与反常积分 $\int_{0}^{+\infty} f(x) \mathrm{d}x$ 均收敛，那么称反常积分 $\int_{-\infty}^{+\infty} f(x) \mathrm{d}x$ 收敛，并称反常积分 $\int_{-\infty}^{0} f(x) \mathrm{d}x$ 的值与反常积分 $\int_{0}^{+\infty} f(x) \mathrm{d}x$ 的值之和为反常积分 $\int_{-\infty}^{+\infty} f(x) \mathrm{d}x$ 的值，否则就称反常积分 $\int_{-\infty}^{+\infty} f(x) \mathrm{d}x$ 发散.

上述反常积分统称为无穷限的反常积分.

由上述定义及牛顿-莱布尼茨公式,可得如下结果:

设 $F(x)$ 为 $f(x)$ 在 $[a, +\infty)$ 上的一个原函数，若 $\lim_{x\to +\infty}F(x)$ 存在，则反常积分

$$
\int_ {a} ^ {+ \infty} f (x)   \mathrm{d} x = \lim _ {x \to + \infty} F (x) - F (a);
$$

若 $\lim_{x\to +\infty}F(x)$ 不存在，则反常积分 $\int_{a}^{+\infty}f(x)\mathrm{d}x$ 发散.

若记 $F(+\infty) = \lim_{x\to +\infty}F(x),[F(x)]_a^{+\infty} = F(+\infty) - F(a)$ ，则当 $F(+\infty)$ 存在时，

$$
\int_ {a} ^ {+ \infty} f (x) \mathrm{d} x = [ F (x) ] _ {a} ^ {+ \infty};
$$

当  $F(+\infty)$  不存在时, 反常积分  $\int_{a}^{+\infty} f(x) \, dx$  发散.

类似地, 若在 $(-∞,b]$ 上 $F'(x)=f(x)$ ，则当 $F(-∞)$ 存在时，

$$
\int_ {- \infty} ^ {b} f (x)   \mathrm{d} x = [ F (x) ] _ {- \infty} ^ {b};
$$

当 $F(-\infty)$ 不存在时，反常积分 $\int_{-\infty}^{b}f(x)\mathrm{d}x$ 发散.

若在 $(- \infty, +\infty)$ 内 $F'(x) = f(x)$，则当 $F(-\infty)$ 与 $F(+\infty)$ 都存在时，

$$
\int_ {- \infty} ^ {+ \infty} f (x) \mathrm{d} x = [ F (x) ] _ {- \infty} ^ {+ \infty};
$$

当 $F(-\infty)$ 与 $F(+\infty)$ 有一个不存在时，反常积分 $\int_{-\infty}^{+\infty}f(x)\mathrm{d}x$ 发散.

例1 计算反常积分 $\int_{-\infty}^{+\infty}\frac{\mathrm{d}x}{1 + x^2}.$

解 $\int_{-\infty}^{+\infty}\frac{\mathrm{d}x}{1 + x^2} = [\arctan x]_{-\infty}^{+\infty} = \lim_{x\to +\infty}\arctan x - \lim_{x\to -\infty}\arctan x = \frac{\pi}{2} -\left(-\frac{\pi}{2}\right) = \pi .$

这个反常积分值的几何意义是: 当  $a \rightarrow -\infty$ ,  $b \rightarrow +\infty$  时, 虽然图 5-9 中阴影部分向左、右无限延伸, 但其面积却有极限值  $\pi$ . 简单地说, 它是位于曲线  $y = \frac{1}{1 + x^{2}}$  的下方, x 轴上方的图形面积.

![](images/page_267_image_16.jpg)

<details>
<summary>text_image</summary>

y
y=\frac{1}{1+x^2}
a O b x
</details>

图5-9

例 2 计算反常积分  $\int_{0}^{+\infty} te^{-pt} dt$ ，其中 p 是常数，且 p > 0.

$$
\begin{array}{l} = \left[ - \frac {t}{p} \mathrm{e} ^ {- p t} + \frac {1}{p} \int \mathrm{e} ^ {- p t} \mathrm{d} t \right] _ {0} ^ {+ \infty} = \left[ - \frac {t}{p} \mathrm{e} ^ {- p t} \right] _ {0} ^ {+ \infty} - \left[ \frac {1}{p ^ {2}} \mathrm{e} ^ {- p t} \right] _ {0} ^ {+ \infty} \\ = - \frac {1}{p} \lim _ {t \to + \infty} t \mathrm{e} ^ {- p t} - 0 - \frac {1}{p ^ {2}} (0 - 1) = \frac {1}{p ^ {2}}. \\ \end{array}
$$

解 $\int_0^{+\infty}t\mathrm{e}^{-pt}\mathrm{d}t = \left[\int t\mathrm{e}^{-pt}\mathrm{d}t\right]_{0}^{+\infty} = \left[-\frac{1}{p}\int t\mathrm{d}(\mathrm{e}^{-pt})\right]_{0}^{+\infty}$

图

释疑解难

5-2

注意,上式中的极限  $\lim_{t\to+\infty}te^{-pt}$  是未定式,可用洛必达法则确定.

例3 证明反常积分 $\int_{a}^{+\infty}\frac{\mathrm{d}x}{x^p} (a > 0)$ 当 $p > 1$ 时收敛，当 $p\leqslant 1$ 时发散.

证 当 $p = 1$ 时，

$$
\int_ {a} ^ {+ \infty} \frac {\mathrm{d} x}{x ^ {p}} = \int_ {a} ^ {+ \infty} \frac {\mathrm{d} x}{x} = [ \ln x ] _ {a} ^ {+ \infty} = + \infty ,
$$

当 $p \neq 1$ 时，

$$
\int_ {a} ^ {+ \infty} \frac {\mathrm{d} x}{x ^ {p}} = \left[ \frac {x ^ {1 - p}}{1 - p} \right] _ {a} ^ {+ \infty} = \left\{ \begin{array}{l l} + \infty , & p <   1, \\ \frac {a ^ {1 - p}}{p - 1}, & p > 1. \end{array} \right.
$$

因此, 当 p>1 时, 这反常积分收敛, 其值为  $\frac{a^{1-p}}{p-1}$ ; 当  $p \leqslant 1$  时, 这反常积分发散.

## 二、无界函数的反常积分

现在我们把定积分推广到被积函数为无界函数的情形.

如果函数 $f(x)$ 在点 $a$ 的任一邻域内都无界,那么点 $a$ 称为函数 $f(x)$ 的瑕点(也称为无界间断点).无界函数的反常积分又称为瑕积分.

设函数 $f(x)$ 在区间 $(a, b]$ 上连续，点 $a$ 为 $f(x)$ 的瑕点。任取 $t > a$，作定积分 $\int_{t}^{b} f(x) \mathrm{d}x$，再求极限

$$
\lim _ {t \to a ^ {+}} \int_ {t} ^ {b} f (x) \mathrm{d} x, \tag {4-4}
$$

这个对变下限的定积分求极限的算式(4-4)称为函数 $f(x)$ 在区间 $(a,b]$ 上的反常积分,仍然记为 $\int_{a}^{b}f(x)\mathrm{d}x$ ,即

$$
\int_ {a} ^ {b} f (x) \mathrm{d} x = \lim _ {t \to a ^ {+}} \int_ {t} ^ {b} f (x) \mathrm{d} x. \tag {$4-4^{\prime$}}
$$

根据算式(4-4)的结果是否存在,可引入反常积分 $\int_{a}^{b}f(x)\mathrm{d}x$ 收敛与发散的定义如下:

定义2（1）设函数 $f(x)$ 在区间 $(a, b]$ 上连续，点 $a$ 为 $f(x)$ 的瑕点，如果极限(4-4)存在，那么称反常积分 $\int_{a}^{b} f(x) \mathrm{d}x$ 收敛，并称此极限为该反常积分的值；如果极限(4-4)不存在，那么称反常积分 $\int_{a}^{b} f(x) \mathrm{d}x$ 发散.

类似地, 设函数  $f(x)$  在区间  $[a, b)$  上连续, 点 b 为  $f(x)$  的瑕点. 任取 t < b, 算式

$$
\lim _ {t \to b ^ {-}} \int_ {a} ^ {t} f (x) \mathrm{d} x \tag {4-5}
$$

称为函数 $f(x)$ 在区间 $[a, b)$ 上的反常积分，仍然记为 $\int_{a}^{b} f(x) \mathrm{d}x$，即

$$
\int_ {a} ^ {b} f (x) \mathrm{d} x = \lim _ {t \to b ^ {-}} \int_ {a} ^ {t} f (x) \mathrm{d} x. \tag {$4-5^{\prime$}}
$$

于是有

（2）设函数 $f(x)$ 在区间 $[a, b)$ 上连续，点 $b$ 为 $f(x)$ 的瑕点，如果极限(4-5)存在，那么称反常积分 $\int_{a}^{b} f(x) \mathrm{d}x$ 收敛，并称此极限为该反常积分的值；如果极限(4-5)不存在，那么称反常积分 $\int_{a}^{b} f(x) \mathrm{d}x$ 发散.

设函数 $f(x)$ 在区间 $[a, c)$ 及区间 $(c, b]$ 上连续，点 $c$ 为 $f(x)$ 的瑕点。反常积分 $\int_{a}^{c} f(x) \mathrm{d}x$ 与反常积分 $\int_{c}^{b} f(x) \mathrm{d}x$ 之和称为函数 $f(x)$ 在区间 $[a, b]$ 上的反常积分，仍然记为 $\int_{a}^{b} f(x) \mathrm{d}x$，即

$$
\int_ {a} ^ {b} f (x) \mathrm{d} x = \int_ {a} ^ {c} f (x) \mathrm{d} x + \int_ {c} ^ {b} f (x) \mathrm{d} x. \tag {4-6}
$$

（3）设函数 $f(x)$ 在区间 $[a, c)$ 及区间 $(c, b]$ 上连续，点 $c$ 为 $f(x)$ 的瑕点。如果反常积分 $\int_{a}^{c} f(x) \mathrm{d}x$ 与反常积分 $\int_{c}^{b} f(x) \mathrm{d}x$ 均收敛，那么称反常积分 $\int_{a}^{b} f(x) \mathrm{d}x$ 收敛，并称反常积分 $\int_{a}^{c} f(x) \mathrm{d}x$ 的值与反常积分 $\int_{c}^{b} f(x) \mathrm{d}x$ 的值之和为反常积分 $\int_{a}^{b} f(x) \mathrm{d}x$ 的值；否则，就称反常积分 $\int_{a}^{b} f(x) \mathrm{d}x$ 发散。

计算无界函数的反常积分,也可借助于牛顿-莱布尼茨公式.

设 $x = a$ 为 $f(x)$ 的瑕点，在 $(a,b]$ 上 $F^{\prime}(x) = f(x)$，如果极限 $\lim_{x\to a^{+}}F(x)$ 存在，那么反常积分

$$
\int_ {a} ^ {b} f (x) \mathrm{d} x = F (b) - \lim _ {x \to a ^ {+}} F (x) = F (b) - F (a ^ {+});
$$

如果 $\lim_{x\to a^{+}}F(x)$ 不存在，那么反常积分 $\int_{a}^{b}f(x)\mathrm{d}x$ 发散.

我们仍用记号 $[F(x)]_a^b$ 来表示 $F(b) - F(a^{+})$ ，从而形式上仍有

$$
\int_ {a} ^ {b} f (x) \mathrm{d} x = \left[ F (x) \right] _ {a} ^ {b}.
$$

对于 $f(x)$ 在 $[a, b)$ 上连续，$b$ 为瑕点的反常积分，也有类似的计算公式，这里不再详述.

例 4 计算反常积分

$$
\int_ {0} ^ {a} \frac {\mathrm{d} x}{\sqrt {a ^ {2} - x ^ {2}}} \quad (a > 0),
$$

解 因为

$$
\lim _ {x \to a ^ {-}} \frac {1}{\sqrt {a ^ {2} - x ^ {2}}} = + \infty ,
$$

所以点 a 是瑕点, 于是

$$
\int_ {0} ^ {a} \frac {\mathrm{d} x}{\sqrt {a ^ {2} - x ^ {2}}} = \left[ \arcsin \frac {x}{a} \right] _ {0} ^ {a} = \lim _ {x \to a ^ {-}} \arcsin \frac {x}{a} - 0 = \frac {\pi}{2}.
$$

这个反常积分值的几何意义是:位于曲线  $y=\frac{1}{\sqrt{a^{2}-x^{2}}}$  之下,x 轴之上,直线 x=0 与 x=a 之间的图形面积(图 5-10).

例 5 讨论反常积分  $\int_{-1}^{1}\frac{dx}{x^{2}}$  的收敛性.

解 被积函数 $f(x) = \frac{1}{x^2}$ 在积分区间 $[-1, 1]$ 上除 $x = 0$ 外连续，且 $\lim_{x \to 0} \frac{1}{x^2} = \infty$. 由于

$$
\int_ {- 1} ^ {0} \frac {\mathrm{d} x}{x ^ {2}} = \left[ - \frac {1}{x} \right] _ {- 1} ^ {0} = \lim _ {x \to 0 ^ {-}} \left(- \frac {1}{x}\right) - 1 = + \infty ,
$$

![](images/page_270_chart_10.jpg)

<details>
<summary>area</summary>

| X | Y |
| --- | --- |
| 0 | 1/a |
| xa | >1/a |
</details>

图5-10

即反常积分 $\int_{-1}^{0}\frac{\mathrm{d}x}{x^2}$ 发散，所以反常积分 $\int_{-1}^{1}\frac{\mathrm{d}x}{x^2}$ 发散.

注意 如果疏忽了 $x = 0$ 是被积函数的瑕点，就会得到以下的错误结果:

$$
\int_ {- 1} ^ {1} \frac {\mathrm{d} x}{x ^ {2}} = \left[ - \frac {1}{x} \right] _ {- 1} ^ {1} = - 1 - 1 = - 2.
$$

例6 证明反常积分 $\int_{a}^{b}\frac{\mathrm{d}x}{(x - a)^q}$ 当 $0 < q < 1$ 时收敛, 当 $q \geqslant 1$ 时发散.

证 当 $q = 1$ 时，

$$
\int_ {a} ^ {b} \frac {\mathrm{d} x}{(x - a) ^ {q}} = \int_ {a} ^ {b} \frac {\mathrm{d} x}{x - a} = [ \ln (x - a) ] _ {a} ^ {b} = \ln (b - a) - \lim _ {x \to a ^ {+}} \ln (x - a) = + \infty .
$$

当 $q \neq 1$ 时，

$$
\int_ {a} ^ {b} \frac {\mathrm{d} x}{(x - a) ^ {q}} = \left[ \frac {(x - a) ^ {1 - q}}{1 - q} \right] _ {a} ^ {b} = \left\{ \begin{array}{l l} \frac {(b - a) ^ {1 - q}}{1 - q}, & 0 <   q <   1, \\ + \infty , & q > 1. \end{array} \right.
$$

因此, 当 0 < q < 1 时, 该反常积分收敛, 其值为  $\frac{(b-a)^{1-q}}{1-q}$ ; 当  $q \geqslant 1$  时, 该反常积分

发散.

设有反常积分 $\int_{a}^{b}f(x)\mathrm{d}x$ ，其中 $f(x)$ 在开区间 $(a,b)$ 内连续， $a$ 可以是 $-\infty ,b$ 可以是 $+\infty ,a,b$ 也可以是 $f(x)$ 的瑕点.对于这样的反常积分，在另加换元函数单调的假定下，可以像定积分一样作换元

例7 求反常积分 $\int_0^{+\infty}\frac{\mathrm{d}x}{\sqrt{x(x + 1)^3}}.$

解 这里,积分上限为 $+\infty$ ,且下限x=0为被积函数的瑕点.

令 $\sqrt{x} = t$ ，则 $x = t^2$ ，当 $x\to 0^{+}$ 时 $t\to 0$ ；当 $x\to +\infty$ 时 $t\to +\infty$ .于是

$$
\int_ {0} ^ {+ \infty} \frac {\mathrm{d} x}{\sqrt {x (x + 1) ^ {3}}} = \int_ {0} ^ {+ \infty} \frac {2 t \mathrm{d} t}{t (t ^ {2} + 1) ^ {3 / 2}} = 2 \int_ {0} ^ {+ \infty} \frac {\mathrm{d} t}{(t ^ {2} + 1) ^ {3 / 2}}.
$$

再令 $t = \tan u$ ，则 $u = \arctan t$ ，当 $t = 0$ 时 $u = 0$ ；当 $t\to +\infty$ 时 $u\to \frac{\pi}{2}$ .于是

$$
\int_ {0} ^ {+ \infty} \frac {\mathrm{d} x}{\sqrt {x (x + 1) ^ {3}}} = 2 \int_ {0} ^ {\frac {\pi}{2}} \frac {\sec^ {2} u \mathrm{d} u}{\sec^ {3} u} = 2 \int_ {0} ^ {\frac {\pi}{2}} \cos u \mathrm{d} u = 2.
$$

本例如用代换 $\frac{1}{x}=t$ 或 $\frac{1}{x+1}=t$ ，计算会更简单些，读者可自行解之.

## 习题5-4

1. 判定下列各反常积分的收敛性, 如果收敛, 计算反常积分的值:

(1) $\int_{1}^{+\infty}\frac{\mathrm{d}x}{x^4};$

(2) $\int_{1}^{+\infty}\frac{\mathrm{d}x}{\sqrt{x}};$

(3) $\int_{0}^{+\infty}\mathrm{e}^{-ax}\mathrm{d}x$ ($a > 0$);

(4) $\int_0^{+\infty}\frac{\mathrm{d}x}{(1 + x)(1 + x^2)};$

(5) $\int_{0}^{+\infty}\mathrm{e}^{-pt}\sin \omega t\mathrm{d}t$ ($p > 0, \omega > 0$);

(6) $\int_{-\infty}^{+\infty}\frac{\mathrm{d}x}{x^2 + 2x + 2};$

(7) $\int_0^1\frac{x\mathrm{d}x}{\sqrt{1 - x^2}};$

(8) $\int_0^2\frac{\mathrm{d}x}{(1 - x)^2};$

(9) $\int_{1}^{2}\frac{x\mathrm{d}x}{\sqrt{x - 1}};$

(10) $\int_{1}^{\mathrm{e}}\frac{\mathrm{d}x}{x\sqrt{1 - (\ln x)^2}}.$

2. 求由曲线  $y=\frac{1}{4x^{2}-1}$ 、x 轴和直线 x=1 所围成的向右无限延伸的图形的面积.

3. 当 $k$ 为何值时, 反常积分 $\int_{2}^{+\infty} \frac{\mathrm{d}x}{x(\ln x)^k}$ 收敛? 当 $k$ 为何值时, 该反常积分发散? 又当 $k$ 为何值时, 该反常积分取得最小值?

4. 利用递推公式计算反常积分 $I_{n} = \int_{0}^{+\infty} x^{n} \mathrm{e}^{-x} \, \mathrm{d}x$ ($n \in \mathbb{N}$).
5. 计算反常积分  $\int_{0}^{1}\ln x dx$ .

## \* 第五节 反常积分的审敛法 Γ函数

反常积分的收敛性,可以通过求被积函数的原函数,然后按定义取极限,根据极限的存在与否来判定.本节中我们来建立不通过被积函数的原函数判定反常积分收敛性的判定法.

## 一、无穷限反常积分的审敛法

定理1 设函数 $f(x)$ 在区间 $[a, +\infty)$ 上连续，且 $f(x) \geqslant 0$。若函数

$$
F (x) = \int_ {a} ^ {x} f (t) \mathrm{d} t
$$

在 $[a, +\infty)$ 上有上界，则反常积分 $\int_{a}^{+\infty} f(x) \, \mathrm{d}x$ 收敛.

事实上, 因为 $f(x) \geqslant 0, F(x)$ 在 $[a, +\infty)$ 上单调增加, 又 $F(x)$ 在 $[a, +\infty)$ 上有上界, 故 $F(x)$ 在 $[a, +\infty)$ 上是单调有界的函数. 按照“$[a, +\infty)$ 上的单调有界函数 $F(x)$ 必有极限 $\lim_{x \to +\infty} F(x)$”的准则, 就可知道极限

$$
\lim _ {x \to + \infty} \int_ {a} ^ {x} f (t)   \mathrm{d} t
$$

存在,即反常积分 $\int_{a}^{+\infty}f(x)\mathrm{d}x$ 收敛.

根据定理 1, 对于非负函数的无穷限的反常积分, 有以下的比较审敛原理:

定理2（比较审敛原理）设函数 $f(x), g(x)$ 在区间 $[a, +\infty)$ 上连续. 如果 $0 \leqslant f(x) \leqslant g(x) (a \leqslant x < +\infty)$，并且 $\int_{a}^{+\infty} g(x) \mathrm{d}x$ 收敛，那么 $\int_{a}^{+\infty} f(x) \mathrm{d}x$ 也收敛；如果 $0 \leqslant g(x) \leqslant f(x) (a \leqslant x < +\infty)$，并且 $\int_{a}^{+\infty} g(x) \mathrm{d}x$ 发散，那么 $\int_{a}^{+\infty} f(x) \mathrm{d}x$ 也发散.

证 设 $a < t < +\infty$ ，由 $0 \leqslant f(x) \leqslant g(x)$ 及 $\int_{a}^{+\infty} g(x) \, \mathrm{d}x$ 收敛，得

$$
\int_ {a} ^ {t} f (x) \mathrm{d} x \leqslant \int_ {a} ^ {t} g (x) \mathrm{d} x \leqslant \int_ {a} ^ {+ \infty} g (x) \mathrm{d} x.
$$

这表明作为积分上限 $t$ 的函数

$$
F (t) = \int_ {a} ^ {t} f (x) \mathrm{d} x
$$

在 $[a, +\infty)$ 上有上界. 由定理1即知反常积分 $\int_{a}^{+\infty} f(x) \mathrm{d}x$ 收敛.

如果 $0 \leqslant g(x) \leqslant f(x)$, 且 $\int_{a}^{+\infty} g(x) \mathrm{d}x$ 发散, 那么 $\int_{a}^{+\infty} f(x) \mathrm{d}x$ 必定发散. 因为如果 $\int_{a}^{+\infty} f(x) \mathrm{d}x$ 收敛, 由定理的第一部分即知 $\int_{a}^{+\infty} g(x) \mathrm{d}x$ 也收敛, 这与假设相矛盾. 证毕.

由上节例3知道,反常积分 $\int_{a}^{+\infty}\frac{\mathrm{d}x}{x^{p}}(a>0)$ 当p>1时收敛,当 $p\leqslant1$ 时发散.因此,取 $g(x)=\frac{A}{x^{p}}(A>0)$ ,立即可得下面的反常积分的比较审敛法.

定理3（比较审敛法1）设函数 $f(x)$ 在区间 $[a, +\infty)$ （$a > 0$）上连续，且 $f(x) \geqslant 0$。如果存在常数 $M > 0$ 及 $p > 1$，使得 $f(x) \leqslant \frac{M}{x^p}$（$a \leqslant x < +\infty$），那么反常积分 $\int_{a}^{+\infty} f(x) \mathrm{d}x$ 收敛；如果存在常数 $N > 0$，使得 $f(x) \geqslant \frac{N}{x}$（$a \leqslant x < +\infty$），那么反常积分 $\int_{a}^{+\infty} f(x) \mathrm{d}x$ 发散。

例1 判定反常积分 $\int_{1}^{+\infty}\frac{\mathrm{d}x}{\sqrt[3]{x^4 + 1}}$ 的收敛性.

解 由于

$$
0 <   \frac {1}{\sqrt [ 3 ]{x ^ {4} + 1}} <   \frac {1}{\sqrt [ 3 ]{x ^ {4}}} = \frac {1}{x ^ {\frac {4}{3}}},
$$

根据比较审敛法1,这个反常积分收敛.

以比较审敛法 1 为基础, 可以得到在应用上较为方便的极限审敛法.

定理4（极限审敛法1）设函数 $f(x)$ 在区间 $[a, +\infty)$ 上连续，且 $f(x) \geqslant 0$。如果存在常数 $p > 1$，使得 $\lim_{x \to +\infty} x^p f(x) = c < +\infty$，那么反常积分 $\int_{a}^{+\infty} f(x) \mathrm{d}x$ 收敛；如果 $\lim_{x \to +\infty} xf(x) = d > 0$（或 $\lim_{x \to +\infty} xf(x) = +\infty$），那么反常积分 $\int_{a}^{+\infty} f(x) \mathrm{d}x$ 发散。

证 由假设 $\lim_{x\to +\infty}x^{p}f(x) = c(p > 1)$. 根据极限的定义, 存在充分大的 $x_{1}(x_{1}\geqslant a,x_{1} > 0)$, 当 $x > x_{1}$ 时, 必有

$$
\mid x ^ {p} f (x) - c \mid <   1,
$$

由此得

$$
0 \leqslant x ^ {p} f (x) <   1 + c.
$$

令 $1 + c = M > 0$ ，于是在区间 $(x_{1}, + \infty)$ 内不等式 $0\leqslant f(x) <   \frac{M}{x^p}$ 成立.由比较审敛法1知

$\int_{x_1}^{+\infty}f(x)\mathrm{d}x$ 收敛，而

$$
\begin{array}{l} \int_ {a} ^ {+ \infty} f (x) \mathrm{d} x = \lim _ {t \rightarrow + \infty} \int_ {a} ^ {t} f (x) \mathrm{d} x = \lim _ {t \rightarrow + \infty} \left[ \int_ {a} ^ {x _ {1}} f (x) \mathrm{d} x + \int_ {x _ {1}} ^ {t} f (x) \mathrm{d} x \right] \\ = \int_ {a} ^ {x _ {1}} f (x) \mathrm{d} x + \lim _ {t \rightarrow + \infty} \int_ {x _ {1}} ^ {t} f (x) \mathrm{d} x = \int_ {a} ^ {x _ {1}} f (x) \mathrm{d} x + \int_ {x _ {1}} ^ {+ \infty} f (x) \mathrm{d} x, \\ \end{array}
$$

故反常积分

$$
\int_ {a} ^ {+ \infty} f (x) \mathrm{d} x
$$

收敛.

如果 $\lim_{x\to +\infty}xf(x) = d > 0$ （或 $+\infty$ ），那么存在充分大的 $x_{1}$ ，当 $x > x_{1}$ 时，必有

$$
\mid x f (x) - d \mid <   \frac {d}{2},
$$

由此得

$$
xf(x) > \frac{d}{2}.
$$

(当 $\lim_{x\to +\infty}xf(x) = +\infty$ 时, 可取任意正数作为 $d$.) 令 $\frac{d}{2} = N > 0$, 于是在区间 $(x_1, +\infty)$ 内不等式 $f(x) \geqslant \frac{N}{x}$ 成立. 根据比较审敛法 1 知 $\int_{x_1}^{+\infty} f(x) \mathrm{d}x$ 发散, 从而反常积分 $\int_{a}^{+\infty} f(x) \mathrm{d}x$ 发散.

例2 判定反常积分 $\int_{1}^{+\infty}\frac{\mathrm{d}x}{x\sqrt{1 + x^2}}$ 的收敛性.

解 由于

$$
\lim _ {x \to + \infty} x ^ {2} \cdot \frac {1}{x \sqrt {1 + x ^ {2}}} = \lim _ {x \to + \infty} \frac {1}{\sqrt {\frac {1}{x ^ {2}} + 1}} = 1,
$$

根据极限审敛法1,知所给反常积分收敛.

例3 判定反常积分 $\int_{1}^{+\infty}\frac{x^{\frac{3}{2}}}{1 + x^2}\mathrm{d}x$ 的收敛性.

解 由于

$$
\lim _ {x \to + \infty} x \frac {x ^ {\frac {3}{2}}}{1 + x ^ {2}} = \lim _ {x \to + \infty} \frac {x ^ {2} \sqrt {x}}{1 + x ^ {2}} = + \infty ,
$$

根据极限审敛法1,知所给反常积分发散.

例4 判定反常积分 $\int_{1}^{+\infty}\frac{\arctan x}{x}\mathrm{d}x$ 的收敛性.

解 由于

$$
\lim _ {x \to + \infty} x \frac {\arctan x}{x} = \lim _ {x \to + \infty} \arctan x = \frac {\pi}{2},
$$

根据极限审敛法1,知所给反常积分发散.

假定反常积分的被积函数在所讨论的区间上可取正值也可取负值,对于这类反常积分的收敛性,有如下的结论:

定理5 设函数 $f(x)$ 在区间 $[a, +\infty)$ 上连续. 如果反常积分

$$
\int_ {a} ^ {+ \infty} | f (x) | \mathrm{d} x
$$

收敛,那么反常积分

$$
\int_ {a} ^ {+ \infty} f (x) \mathrm{d} x
$$

也收敛.

证 令 $\varphi(x) = \frac{1}{2}[f(x) + |f(x)|]$, 于是 $\varphi(x) \geqslant 0$, 且 $\varphi(x) \leqslant |f(x)|$, 而

$\int_{a}^{+\infty}|f(x)|\mathrm{d}x$ 收敛，由比较审敛法1即知 $\int_{a}^{+\infty}\varphi (x)\mathrm{d}x$ 也收敛.但 $f(x) = 2\varphi (x) - |f(x)|$ ，因此

$$
\int_ {a} ^ {+ \infty} f (x) \mathrm{d} x = 2 \int_ {a} ^ {+ \infty} \varphi (x) \mathrm{d} x - \int_ {a} ^ {+ \infty} | f (x) | \mathrm{d} x.
$$

可见反常积分 $\int_{a}^{+\infty}f(x)\mathrm{d}x$ 是两个收敛的反常积分的差，因此它是收敛的.证毕

通常称满足定理5条件的反常积分 $\int_{a}^{+\infty} f(x) \mathrm{d}x$ 绝对收敛. 于是, 定理5可简单地表达为: 绝对收敛的反常积分 $\int_{a}^{+\infty} f(x) \mathrm{d}x$ 必定收敛.

例5 判定反常积分 $\int_0^{+\infty}\mathrm{e}^{-ax}\sin bx\mathrm{d}x$ （ $a,b$ 都是常数，且 $a > 0)$ 的收敛性.

解 因为 $|\mathrm{e}^{-ax}\sin bx| \leqslant \mathrm{e}^{-ax}$, 而 $\int_{0}^{+\infty}\mathrm{e}^{-ax}\mathrm{d}x$ 收敛, 根据比较审敛法 1, 反常积分 $\int_{0}^{+\infty}|\mathrm{e}^{-ax}\sin bx|\mathrm{d}x$ 收敛. 由定理 5 可知所给反常积分收敛.

## 二、无界函数的反常积分的审敛法

对于无界函数的反常积分,也有类似的审敛法.

由上节例6知道,反常积分

$$
\int_ {a} ^ {b} \frac {\mathrm{d} x}{(x - a) ^ {q}}
$$

当 $q < 1$ 时收敛, 当 $q \geqslant 1$ 时发散. 于是, 与定理3、定理4类似可得如下两个审敛法:

定理6(比较审敛法2) 设函数 $f(x)$ 在区间 $(a, b]$ 上连续，且 $f(x) \geqslant 0, x = a$ 为 $f(x)$ 的瑕点. 如果存在常数 $M > 0$ 及 $q < 1$ ，使得

$$
f (x) \leqslant \frac {M}{(x - a) ^ {q}} \quad (a <   x \leqslant b),
$$

那么反常积分 $\int_{a}^{b}f(x)\mathrm{d}x$ 收敛；如果存在常数 $N > 0$ ，使得

$$
f (x) \geqslant \frac {N}{x - a} \quad (a <   x \leqslant b),
$$

那么反常积分  $\int_{a}^{b}f(x)\mathrm{d}x$  发散.

定理7(极限审敛法2) 设函数 $f(x)$ 在区间 $(a, b]$ 上连续，且 $f(x) \geqslant 0, x = a$ 为 $f(x)$ 的瑕点. 如果存在常数 $0 < q < 1$ ，使得

$$
\lim _ {x \to a ^ {+}} (x - a) ^ {q} f (x)
$$

存在,那么反常积分  $\int_{a}^{b}f(x)\mathrm{d}x$  收敛;如果

$$
\lim _ {x \to a ^ {+}} (  x   -   a  ) f (  x  ) = d   >   0 \quad (\text {或} \lim _ {x \to a ^ {+}} (  x   -   a  ) f (  x  ) = + \infty) ,
$$

那么反常积分  $\int_{a}^{b}f(x)\mathrm{d}x$  发散.

例6 判定反常积分 $\int_{1}^{3}\frac{\mathrm{d}x}{\ln x}$ 的收敛性.

解 这里 $x = 1$ 是被积函数的瑕点.由洛必达法则知

$$
\lim _ {x \to 1 ^ {+}} (x - 1) \frac {1}{\ln x} = \lim _ {x \to 1 ^ {+}} \frac {1}{\frac {1}{x}} = 1 > 0,
$$

根据极限审敛法 2, 所给反常积分发散.

例 7 判定椭圆积分

$$
\int_ {0} ^ {1} \frac {\mathrm{d} x}{\sqrt {(1 - x ^ {2}) (1 - k ^ {2} x ^ {2})}} \quad (k ^ {2} <   1)
$$

的收敛性.

解 这里 $x = 1$ 是被积函数的瑕点.由于

$$
\lim _ {x \to 1 ^ {-}} (1 - x) ^ {\frac {1}{2}} \frac {1}{\sqrt {(1 - x ^ {2}) (1 - k ^ {2} x ^ {2})}} = \lim _ {x \to 1 ^ {-}} \frac {1}{\sqrt {(1 + x) (1 - k ^ {2} x ^ {2})}} = \frac {1}{\sqrt {2 (1 - k ^ {2})}},
$$

根据极限审敛法2,所给反常积分收敛.

对于无界函数的反常积分,当被积函数在所讨论的区间上可取正值也可取负值时,有与定理5相类似的结论,在此不再详述.

例8 判定反常积分 $\int_0^1\frac{1}{\sqrt{x}}\sin \frac{1}{x}\mathrm{d}x$ 的收敛性.

解 因为 $\left|\frac{1}{\sqrt{x}}\sin \frac{1}{x}\right| \leqslant \frac{1}{\sqrt{x}}$，而 $\int_0^1\frac{\mathrm{d}x}{\sqrt{x}}$ 收敛，根据比较审敛法2，反常积分 $\int_0^1\left|\frac{1}{\sqrt{x}}\sin \frac{1}{x}\right|\mathrm{d}x$ 收敛，从而反常积分 $\int_0^1\frac{1}{\sqrt{x}}\sin \frac{1}{x}\mathrm{d}x$ 也收敛.

## 三、$\Gamma$ 函数

下面介绍在理论上和应用上都有重要意义的 $\Gamma$ 函数.这函数的定义是

$$
\Gamma (s) = \int_ {0} ^ {+ \infty} \mathrm{e} ^ {- x} x ^ {s - 1} \mathrm{d} x \quad (s > 0). \tag {5-1}
$$

首先,讨论(5-1)式右端积分的收敛性问题.这个积分的积分区间为无穷,又当s-1<0时x=0是被积函数的瑕点.为此,分别讨论下列两个积分

$$
I _ {1} = \int_ {0} ^ {1} \mathrm{e} ^ {- x} x ^ {s - 1} \mathrm{d} x, \quad I _ {2} = \int_ {1} ^ {+ \infty} \mathrm{e} ^ {- x} x ^ {s - 1} \mathrm{d} x
$$

的收敛性.

先讨论 $I_{1}$. 当 $s \geqslant 1$ 时, $I_{1}$ 是定积分; 当 $0 < s < 1$ 时, 因为

$$
\mathrm{e} ^ {- x} \cdot x ^ {s - 1} = \frac {1}{\mathrm{e} ^ {x}} \frac {1}{x ^ {1 - s}} <   \frac {1}{x ^ {1 - s}},
$$

而 1-s<1, 根据比较审敛法 2, 反常积分  $I_{1}$  收敛.

再讨论 $I_{2}$ .因为

$$
\lim _ {x \to + \infty} x ^ {2} \cdot (\mathrm{e} ^ {- x} x ^ {s - 1}) = \lim _ {x \to + \infty} \frac {x ^ {s + 1}}{\mathrm{e} ^ {x}} = 0,
$$

根据极限审敛法  $1, I_{2}$  也收敛.

由以上讨论即得反常积分 $\int_0^{+\infty}\mathrm{e}^{-x}x^{s - 1}\mathrm{d}x$ 对 $s > 0$ 均收敛. $\Gamma$ 函数的图形如图5-11所示.

其次,讨论  $\Gamma$  函数的几个重要性质.

1. 递推公式 $\Gamma(s + 1) = s\Gamma(s) (s > 0)$.

证 应用分部积分法,有

$$
\Gamma (s + 1) = \int_ {0} ^ {+ \infty} \mathrm{e} ^ {- x} x ^ {s} \mathrm{d} x = - \int_ {0} ^ {+ \infty} x ^ {s} \mathrm{d} (\mathrm{e} ^ {- x}) = [ - x ^ {s} \mathrm{e} ^ {- x} ] _ {0} ^ {+ \infty} + s \int_ {0} ^ {+ \infty} \mathrm{e} ^ {- x} x ^ {s - 1} \mathrm{d} x = s \Gamma (s),
$$

其中  $\lim_{x\to+\infty}x^{s}e^{-x}=0$  可由洛必达法则求得.

显然，$\Gamma(1) = \int_{0}^{+\infty}\mathrm{e}^{-x}\mathrm{d}x = 1.$

反复运用递推公式,便有

![](images/page_277_chart_23.jpg)

<details>
<summary>line</summary>

| s | \(\Gamma(s)\) |
| --- | --- |
| 0 | ~6.5 |
| 1 | ~1.2 |
| 1.5 | 1 |
| 3 | ~2.2 |
| 4 | ~6.5 |
</details>

图5-11

$$
\Gamma (2) = 1 \cdot \Gamma (1) = 1,
$$

$$
\Gamma (3) = 2 \cdot \Gamma (2) = 2!,
$$

$$
\Gamma (4) = 3 \cdot \Gamma (3) = 3!, \dots
$$

一般地,对任何正整数 n,有

$$
\Gamma (n + 1) = n!,
$$

所以,我们可以把  $\Gamma$  函数看成是阶乘的推广.

2. 当 $s \to 0^{+}$ 时, $\Gamma(s) \to +\infty$.

证 因为

$$
\Gamma (s) = \frac {\Gamma (s + 1)}{s}, \quad \Gamma (1) = 1,
$$

所以当 $s \to 0^{+}$时, $\Gamma(s) \to +\infty$ ①.

3.  $\Gamma(s)\Gamma(1-s)=\frac{\pi}{\sin\pi s}(0<s<1)$ .

这个公式称为余元公式,在此我们不作证明.

当 $s = \frac{1}{2}$ 时，由余元公式可得

$$
\Gamma \left(\frac {1}{2}\right) = \sqrt {\pi}.
$$

4. 在 $\Gamma(s) = \int_{0}^{+\infty} \mathrm{e}^{-x} x^{s-1} \, \mathrm{d}x$ 中，作代换 $x = u^2$，有

$$
\Gamma (s) = 2 \int_ {0} ^ {+ \infty} \mathrm{e} ^ {- u ^ {2}} u ^ {2 s - 1} \mathrm{d} u. \tag {5-2}
$$

再令 $2s - 1 = t$ 或 $s = \frac{1 + t}{2}$, 便有

$$
\int_ {0} ^ {+ \infty} \mathrm{e} ^ {- u ^ {2}} u ^ {t} \mathrm{d} u = \frac {1}{2} \Gamma \left(\frac {1 + t}{2}\right) \quad (t > - 1).
$$

上式左端是实际应用中常见的积分,它的值可以通过上式用  $\Gamma$  函数计算出来.

在(5-2)中,令 $s=\frac{1}{2}$ ,得

$$
2 \int_ {0} ^ {+ \infty} \mathrm{e} ^ {- u ^ {2}} \mathrm{d} u = \Gamma \left(\frac {1}{2}\right) = \sqrt {\pi}.
$$

从而

$$
\int_ {0} ^ {+ \infty} \mathrm{e} ^ {- u ^ {2}} \mathrm{d} u = \frac {\sqrt {\pi}}{2}.
$$

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">①  $\Gamma$  函数在 s>0 时连续.</span></small>

上式左端的积分是在概率论中常用的积分.

## \*习题5-5

1. 判定下列反常积分的收敛性:

(1) $\int_{0}^{+\infty}\frac{x^2}{x^4 + x^2 + 1}\mathrm{d}x;$

(2) $\int_{1}^{+\infty}\frac{\mathrm{d}x}{x\sqrt[3]{x^2 + 1}};$

(3) $\int_{1}^{+\infty}\sin \frac{1}{x^2}\mathrm{d}x;$

(4) $\int_0^{+\infty}\frac{\mathrm{d}x}{1 + x|\sin x|};$

(5) $\int_{1}^{+\infty}\frac{x\arctan x}{1 + x^3}\mathrm{d}x;$

(6) $\int_{1}^{2}\frac{\mathrm{d}x}{(\ln x)^3};$

(7) $\int_0^1\frac{x^4}{\sqrt{1 - x^4}}\mathrm{d}x;$

(8) $\int_{1}^{2}\frac{\mathrm{d}x}{\sqrt[3]{x^2 - 3x + 2}}.$

2. 设反常积分  $\int_{1}^{+\infty} f^{2}(x) \, dx$  收敛, 证明反常积分  $\int_{1}^{+\infty} \frac{f(x)}{x} \, dx$  绝对收敛.

3. 用 $\Gamma$ 函数表示下列积分, 并指出这些积分的收敛范围:

(1) $\int_{0}^{+\infty}\mathrm{e}^{-x^n}\mathrm{d}x (n > 0);$

(2) $\int_{0}^{1}\left(\ln\frac{1}{x}\right)^{p}dx;$

(3) $\int_{0}^{+\infty} x^{m} \mathrm{e}^{-x^{n}} \, \mathrm{d}x (n \neq 0)$.

4. 证明 $\Gamma\left(\frac{2k+1}{2}\right)=\frac{1\cdot3\cdot5\cdot\cdots\cdot(2k-1)\sqrt{\pi}}{2^{k}}$, 其中 $k\in\mathbb{N}_{+}$.

5. 证明以下各式(其中  $n \in N_{+}$ ):

(1)  $2 \cdot 4 \cdot 6 \cdot \cdots \cdot 2n = 2^{n}\Gamma(n+1)$ ;

(2) $1 \cdot 3 \cdot 5 \cdot \cdots \cdot (2n-1) = \frac{\Gamma(2n)}{2^{n-1}\Gamma(n)}$;

(3)  $\sqrt{\pi}\Gamma(2n)=2^{2n-1}\Gamma(n)\Gamma\left(n+\frac{1}{2}\right)$  (勒让德(Legendre)倍量公式).

## 总习题五

1. 填空:

（1）函数 $f(x)$ 在 $[a,b]$ 上有界是 $f(x)$ 在 $[a,b]$ 上可积的\_\_\_\_条件，而 $f(x)$ 在 $[a,b]$ 上连续是 $f(x)$ 在 $[a,b]$ 上可积的\_\_\_\_条件；

(2) 对  $[a, +\infty)$  上非负、连续的函数  $f(x)$ ，积分上限的函数  $\int_{a}^{x} f(t) dt$  在  $[a, +\infty)$  上有界是反常积分  $\int_{a}^{+\infty} f(x) dx$  收敛的 \_\_\_\_ 条件；

\* (3) 绝对收敛的反常积分 $\int_{a}^{+\infty} f(x) \mathrm{d}x$ 一定\_\_\_\_；

(4) 函数 $f(x)$ 在 $[a, b]$ 上有定义且 $|f(x)|$ 在 $[a, b]$ 上可积，此时积分 $\int_{a}^{b} f(x) \, \mathrm{d}x$ \_\_\_\_ 存在.

(5) 设函数  $f(x)$  连续，则  $\frac{\mathrm{d}}{\mathrm{d}x}\int_{0}^{x}tf(t^{2}-x^{2})\mathrm{d}t=$ \_\_\_\_ .

2. 以下两题中给出了四个结论,从中选出一个正确的结论:

（1）设 $I = \int_0^1\frac{x^4}{\sqrt{1 + x}}\mathrm{d}x$ ，则估计 $I$ 值的大致范围为（ ）；

(A) $0 \leqslant I \leqslant \frac{\sqrt{2}}{10}$

(B) $\frac{\sqrt{2}}{10} \leqslant I \leqslant \frac{1}{5}$

(C) $\frac{1}{5} < I < 1$

(D) $I \geqslant 1$

(2) 设  $F(x)$  是连续函数  $f(x)$  的一个原函数, 则必有().

(A)  $F(x)$  是偶函数  $\Leftrightarrow f(x)$  是奇函数

(B) $F(x)$ 是奇函数 $\Leftrightarrow f(x)$ 是偶函数

(C)  $F(x)$  是周期函数  $\Leftrightarrow f(x)$  是周期函数

(D)  $F(x)$  是单调函数  $\Leftrightarrow f(x)$  是单调函数

3. 回答下列问题:

（1）设函数 $f(x)$ 及 $g(x)$ 在区间 $[a, b]$ 上连续，且 $f(x) \geqslant g(x)$，则 $\int_{a}^{b}[f(x) - g(x)] \mathrm{d}x$ 在几何上表示什么？

(2) 设函数  $f(x)$  在区间  $[a, b]$  上连续，且  $f(x) \geqslant 0$ ，则  $\int_{a}^{b} \pi f^{2}(x) \, dx$  在几何上表示什么？

（3）如果在时刻 t 以  $\varphi(t)$  的流量(单位时间内流过的流体的体积或质量)向一水池注水,那么  $\int_{t_{1}}^{t_{2}}\varphi(t)\mathrm{d}t$  表示什么?

（4）如果某国人口增长的速率为 $u(t)$，那么 $\int_{T_1}^{T_2} u(t) \, \mathrm{d}t$ 表示什么？

(5) 如果一公司经营某种产品的边际利润函数为  $P'(x)$ ，那么  $\int_{1000}^{2000} P'(x) \, dx$  表示什么？

\* 4. 利用定积分的定义计算下列极限:

(1)  $\lim_{n\to\infty}\frac{1}{n}\sum_{i=1}^{n}\sqrt{1+\frac{i}{n}}$ ;

(2)  $\lim_{n\to\infty}\frac{1^{p}+2^{p}+\cdots+n^{p}}{n^{p+1}}\quad(p>0).$

5. 求下列极限:

(1) $\lim_{x\to a}\frac{x}{x - a}\int_{a}^{x}f(t)\mathrm{d}t$ ，其中 $f(x)$ 连续；

(2) $\lim_{x\to +\infty}\frac{\int_0^x(\arctan t)^2\mathrm{d}t}{\sqrt{x^2 + 1}}.$

6. 下列计算是否正确,试说明理由:

(1) $\int_{-1}^{1} \frac{\mathrm{d}x}{1 + x^2} = -\int_{-1}^{1} \frac{\mathrm{d}\left(\frac{1}{x}\right)}{1 + \left(\frac{1}{x}\right)^2} = \left[-\arctan \frac{1}{x}\right]_{-1}^{1} = -\frac{\pi}{2};$

(2) 因为  $\int_{-1}^{1}\frac{\mathrm{d}x}{x^{2}+x+1}=\frac{x=\frac{1}{t}}{-\int_{-1}^{1}\frac{\mathrm{d}t}{t^{2}+t+1}}$ ，所以  $\int_{-1}^{1}\frac{\mathrm{d}x}{x^{2}+x+1}=0.$

7. 设 $x > 0$ ，证明:$\int_{0}^{x} \frac{1}{1 + t^2} \mathrm{d}t + \int_{0}^{\frac{1}{x}} \frac{1}{1 + t^2} \mathrm{d}t = \frac{\pi}{2}$.

8. 设 $p > 0$，证明:$\frac{p}{p + 1} < \int_{0}^{1} \frac{\mathrm{d}x}{1 + x^p} < 1$.

9. 设 $f(x), g(x)$ 在区间 $[a, b]$ 上均连续，证明:

(1) $\left[\int_{a}^{b}f(x)g(x)\mathrm{d}x\right]^{2}\leqslant \int_{a}^{b}f^{2}(x)\mathrm{d}x\cdot \int_{a}^{b}g^{2}(x)\mathrm{d}x$ （柯西-施瓦茨不等式）；

(2) $\left\{\int_{a}^{b}[f(x) + g(x)]^{2}\mathrm{d}x\right\}^{\frac{1}{2}}\leqslant \left[\int_{a}^{b}f^{2}(x)\mathrm{d}x\right]^{\frac{1}{2}} + \left[\int_{a}^{b}g^{2}(x)\mathrm{d}x\right]^{\frac{1}{2}}$ （闵可夫斯基不等式）.

10. 设 $f(x)$ 在区间 $[a, b]$ 上连续，且 $f(x) > 0$. 证明:$\int_{a}^{b} f(x) \, \mathrm{d}x \cdot \int_{a}^{b} \frac{\mathrm{d}x}{f(x)} \geqslant (b - a)^2$.

11. 计算下列积分:

(1) $\int_{0}^{\frac{\pi}{2}}\frac{x + \sin x}{1 + \cos x}\mathrm{d}x;$

(2) $\int_{0}^{\frac{\pi}{4}}\ln (1 + \tan x)\mathrm{d}x;$

(3) $\int_{0}^{a}\frac{\mathrm{d}x}{x + \sqrt{a^2 - x^2}} (a > 0);$

(4) $\int_0^{\frac{\pi}{2}}\sqrt{1 - \sin 2x}\mathrm{d}x;$

(5) $\int_{0}^{\frac{\pi}{2}}\frac{\mathrm{d}x}{1 + \cos^2x};$

(6) $\int_0^\pi x\sqrt{\cos^2x - \cos^4x}\mathrm{d}x;$

(7) $\int_{0}^{\pi} x^{2} \mid \cos x \mid \mathrm{d}x$;

(8) $\int_{0}^{+\infty}\frac{\mathrm{d}x}{\mathrm{e}^{x + 1} + \mathrm{e}^{3 - x}};$

(9) $\int_{\frac{1}{2}}^{\frac{3}{2}}\frac{\mathrm{d}x}{\sqrt{|x^2 - x|}};$

(10) $\int_0^x\max \{t^3,t^2,1\} \mathrm{d}t.$

12. 设 $f(x)$ 为连续函数, 证明: $\int_{0}^{x} f(t)(x - t) \, \mathrm{d}t = \int_{0}^{x} \left[ \int_{0}^{t} f(u) \, \mathrm{d}u \right] \, \mathrm{d}t$.

13. 设  $f(x)$  在区间  $[a, b]$  上连续，且  $f(x) > 0$ ，

$$
F (x) = \int_ {a} ^ {x} f (t)   \mathrm{d} t + \int_ {b} ^ {x} \frac {\mathrm{d} t}{f (t)}, \quad x \in [ a, b ].
$$

证明:

(1)  $F'(x) \geqslant 2;$

(2) 方程  $F(x)=0$  在区间  $(a,b)$  内有且仅有一个根.

14. 求  $\int_{0}^{2}f(x-1)\mathrm{d}x$ , 其中

$$
f (x) = \left\{ \begin{array}{l l} \frac {1}{1 + \mathrm{e} ^ {x}}, & x <   0, \\ \frac {1}{1 + x}, & x \geqslant 0. \end{array} \right.
$$

15. 设 $f'(x)$ 在 $[- \pi, \pi]$ 上连续，$a_n = \frac{1}{\pi} \int_{-\pi}^{\pi} f(x) \cos nx \, \mathrm{d}x$ ($n \in \mathbb{N}$)，证明:$\lim_{n \to \infty} a_n = 0$

16. 设 $f(x)$ 在区间 $[a, b]$ 上连续，$g(x)$ 在区间 $[a, b]$ 上连续且不变号。证明:至少存在一点 $\xi \in [a, b]$，使下式成立:

$$
\int_ {a} ^ {b} f (x) g (x) \mathrm{d} x = f (\xi) \int_ {a} ^ {b} g (x) \mathrm{d} x \quad (\text {积分第一中值定理}).
$$

\* 17. 证明: $\int_{0}^{+\infty} x^{n} \mathrm{e}^{-x^{2}} \mathrm{d}x = \frac{n-1}{2} \int_{0}^{+\infty} x^{n-2} \mathrm{e}^{-x^{2}} \mathrm{d}x (n>1)$, 并用它证明

$$
\int_ {0} ^ {+ \infty} x ^ {2 n + 1} \mathrm{e} ^ {- x ^ {2}} \mathrm{d} x = \frac {1}{2} \Gamma (n + 1) \quad (n \in \mathbf {N}).
$$

\* 18. 判定下列反常积分的收敛性:

(1) $\int_{0}^{+\infty}\frac{\sin x}{\sqrt{x^3}}\mathrm{d}x;$

(2) $\int_{2}^{+\infty}\frac{\mathrm{d}x}{x\cdot\sqrt[3]{x^2 - 3x + 2}};$

(3) $\int_{2}^{+\infty}\frac{\cos x}{\ln x}dx;$

(4) $\int_{0}^{+\infty}\frac{\mathrm{d}x}{\sqrt[3]{x^2(x - 1)(x - 2)}}.$

\* 19. 计算下列反常积分:

(1) $\int_{0}^{\frac{\pi}{2}}\ln\sin xdx;$

(2) $\int_{0}^{+\infty}\frac{\mathrm{d}x}{(1 + x^2)(1 + x^\alpha)} (\alpha \geqslant 0)$.

![](images/page_282_image_11.jpg)

第五章释疑解难

![](images/page_282_image_13.jpg)

第五章例题精讲

## 第六章

## 定积分的应用

本章中我们将应用前面学过的定积分理论来分析和解决一些几何、物理中的问题,其目的不仅在于建立计算这些几何、物理量的公式,更重要的还在于介绍运用元素法将一个量表达成为定积分的分析方法.

## 第一节 定积分的元素法

在定积分的应用中,经常采用所谓元素法.为了说明这种方法,我们先回顾一下第五章中讨论过的曲边梯形的面积问题.

设 $f(x)$ 在区间 $[a, b]$ 上连续且 $f(x) \geqslant 0$，求以曲线 $y = f(x)$ 为曲边、底为 $[a, b]$ 的曲边梯形的面积 $A$. 把这个面积 $A$ 表示为定积分

$$
A = \int_ {a} ^ {b} f (x) \mathrm{d} x
$$

的步骤是

（1）用任意一组分点把区间 $[a, b]$ 分成长度为 $\Delta x_{i} (i = 1,2,\dots,n)$ 的 $n$ 个小区间，相应地把曲边梯形分成 $n$ 个窄曲边梯形，第 $i$ 个窄曲边梯形的面积设为 $\Delta A_{i}$，于是有

$$
A = \sum_ {i = 1} ^ {n} \Delta A _ {i};
$$

(2) 计算  $\Delta A_{i}$  的近似值

$$
\Delta A _ {i} \approx f (\xi_ {i}) \Delta x _ {i} \quad (x _ {i - 1} \leqslant \xi_ {i} \leqslant x _ {i});
$$

(3) 求和, 得 A 的近似值

$$
A \approx \sum_ {i = 1} ^ {n} f (\xi_ {i}) \Delta x _ {i};
$$

(4) 求极限, 记  $\lambda = \max\{\Delta x_{1}, \Delta x_{2}, \cdots, \Delta x_{n}\}$ , 得

$$
A = \lim _ {\lambda \to 0} \sum_ {i = 1} ^ {n} f (\xi_ {i}) \Delta x _ {i} = \int_ {a} ^ {b} f (x) \mathrm{d} x.
$$

在上述问题中我们注意到,所求量(即面积 A)与区间  $[a, b]$  有关.如果把区间  $[a, b]$  分成许多部分区间,那么所求量相应地分成许多部分量(即  $\Delta A_{i}$ ),而所求量等于所有部分量之和(即  $A = \sum_{i=1}^{n} \Delta A_{i}$ ),这一性质称为所求量对于区间  $[a, b]$  具有可加性.此外,以  $f(\xi_{i}) \Delta x_{i}$  近似代替部分量  $\Delta A_{i}$  时,要求它们只相差一个比  $\Delta x_{i}$  高阶的无穷小,以使和式  $\sum_{i=1}^{n} f(\xi_{i}) \Delta x_{i}$  的极限是 A 的精确值,从而 A 可以表示为定积分

$$
A = \int_ {a} ^ {b} f (x)   \mathrm{d} x.
$$

在引出 A 的积分表达式的四个步骤中, 主要的是第二步, 这一步是要确定  $\Delta A_{i}$  的近似值  $f(\xi_{i})\Delta x_{i}$ , 使得

$$
A = \lim _ {\lambda \to 0} \sum_ {i = 1} ^ {n} f (\xi_ {i}) \Delta x _ {i} = \int_ {a} ^ {b} f (x) \mathrm{d} x.
$$

在实用上,为了简便起见,省略下标 i,用  $\Delta A$  表示任一小区间  $[x, x + dx]$  上的窄曲边梯形的面积,这样,

$$
A = \sum \Delta A.
$$

取 $[x,x+dx]$ 的左端点x为 $\xi$ ，以点x处的函数值 $f(x)$ 为高、dx为底的矩形的面积 $f(x)\mathrm{d}x$ 为 $\Delta A$ 的近似值（如图6-1阴影部分所示），即

$$
\Delta A \approx f (x)   \mathrm{d} x.
$$

上式右端 $f(x)\mathrm{d}x$ 叫做面积元素，记为 $\mathrm{dA} = f(x)\mathrm{dx}$ 于是

$$
A \approx \sum f (x) \mathrm{d} x,
$$

![](images/page_284_image_12.jpg)

<details>
<summary>text_image</summary>

y
y=f(x)
f(x)
dA
x x+dx
O a b x
</details>

图6-1

因此

$$
A = \lim \sum f (x)   \mathrm{d} x = \int_ {a} ^ {b} f (x)   \mathrm{d} x.
$$

一般地,如果某一实际问题中的所求量 U 符合下列条件:

(1) U 是与一个变量 x 的变化区间  $[a, b]$  有关的量；
(2) U 对于区间  $[a, b]$  具有可加性, 就是说, 如果把区间  $[a, b]$  分成许多部分区间, 那么 U 相应地分成许多部分量, 而 U 等于所有部分量之和;
(3) 部分量  $\Delta U_{i}$  的近似值可表示为  $f(\xi_{i})\Delta x_{i}$ ,

那么就可考虑用定积分来表达这个量 $U$. 通常写出这个量 $U$ 的积分表达式的步骤是

1）根据问题的具体情况，选取一个变量例如 x 为积分变量，并确定它的变化区间

$[a,b]$ ;

2）设想把区间 $[a, b]$ 分成 $n$ 个小区间，取其中任一小区间并记作 $[x, x + \mathrm{d}x]$，求出相应于这个小区间的部分量 $\Delta U$ 的近似值。如果 $\Delta U$ 能近似地表示为 $[a, b]$ 上的一个连续函数在 $x$ 处的值 $f(x)$ 与 $\mathrm{d}x$ 的乘积①，就把 $f(x) \mathrm{d}x$ 称为量 $U$ 的元素且记作 $\mathrm{d}U$，即

$$
\mathrm{d} U = f (x) \mathrm{d} x;
$$

3）以所求量 $U$ 的元素 $f(x)\mathrm{d}x$ 为被积表达式，在区间 $[a,b]$ 上作定积分，得

$$
U = \int_ {a} ^ {b} f (x)   \mathrm{d} x.
$$

这就是所求量 U 的积分表达式.

这个方法通常叫做元素法.下面两节中我们将应用这个方法来讨论几何、物理中的一些问题.

## 第二节 定积分在几何学上的应用

## 一、平面图形的面积

## 1. 直角坐标情形

在第五章中我们已经知道,由曲线  $y=f(x)\quad(f(x)\geqslant0)$  及直线 x=a,x=b (a<b) 与 x 轴所围成的曲边梯形的面积 A 是定积分

$$
A = \int_ {a} ^ {b} f (x)   \mathrm{d} x,
$$

其中被积表达式 $f(x)\mathrm{d}x$ 就是直角坐标下的面积元素,它表示高为 $f(x)$ 、底为 dx 的一个矩形面积.

应用定积分,不但可以计算曲边梯形面积,还可以计算一些比较复杂的平面图形的面积.

例 1 计算由两条抛物线:  $y^{2}=x, y=x^{2}$  所围成的图形的面积.

解 这两条抛物线所围成的图形如图 6-2 所示.为了具体定出图形的所在范围,先求出这两条抛物线的交点.为此,解方程组

![](images/page_285_chart_17.jpg)

<details>
<summary>area</summary>

| Point | X | Y |
| --- | --- | --- |
| Intersection (x+dx) | 1 | 1 |
</details>

图6-2

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 这里  $\Delta U$  与  $f(x)\mathrm{d}x$  相差一个比 dx 高阶的无穷小.</span></small>

$$
\left\{ \begin{array}{l} y ^ {2} = x, \\ y = x ^ {2}, \end{array} \right.
$$

得到两个解

$$
x = 0, y = 0 \quad {\text {及}} \quad x = 1, y = 1.
$$

即这两抛物线的交点为(0,0)及(1,1)，从而知道这图形在直线 $x = 0$ 与 $x = 1$ 之间.

取横坐标 $x$ 为积分变量, 它的变化区间为 $[0,1]$. 相应于 $[0,1]$ 上的任一小区间 $[x, x + \mathrm{d}x]$ 的窄条的面积近似于高为 $\sqrt{x} - x^2$、底为 $\mathrm{d}x$ 的窄矩形的面积, 从而得到面积元素

$$
\mathrm{d} A = (\sqrt {x} - x ^ {2}) \mathrm{d} x.
$$

以 $(\sqrt{x}-x^{2})\mathrm{d}x$ 为被积表达式,在闭区间[0,1]上作定积分,便得所求面积为

$$
A = \int_ {0} ^ {1} (\sqrt {x} - x ^ {2}) \mathrm{d} x = \left[ \frac {2}{3} x ^ {\frac {3}{2}} - \frac {x ^ {3}}{3} \right] _ {0} ^ {1} = \frac {1}{3}.
$$

例 2 计算抛物线  $y^{2}=2x$  与直线 y=x-4 所围成的图形的面积.

解 这个图形如图 6-3 所示.为了定出这图形所在的范围,先求出所给抛物线和直线的交点.解方程组

$$
\left\{ \begin{array}{l} y ^ {2} = 2 x, \\ y = x - 4, \end{array} \right.
$$

得交点(2,-2)和(8,4)，从而知道这图形在直线 $y = -2$ 及 $y = 4$ 之间.

现在,选取纵坐标 y 为积分变量,它的变化区间为  $[-2,4]$  (读者可以思考一下,取横坐标 x 为积分

![](images/page_286_chart_14.jpg)

<details>
<summary>contour</summary>

| Point | x-coordinate | y-coordinate |
| --- | --- | --- |
| Intersection of y=x-4 and y=dy | 8 | 4 |
| Intersection of y=dy and y=x-4 | 2 | -2 |
</details>

图6-3

变量,有什么不方便的地方).相应于 $[-2,4]$ 上任一小区间 $[y,y+dy]$ 的窄条面积近似于高为dy、底为 $(y+4)-\frac{1}{2}y^{2}$ 的窄矩形的面积,从而得到面积元素

$$
\mathrm{d} A = \left(y + 4 - \frac {1}{2} y ^ {2}\right) \mathrm{d} y.
$$

以 $\left(y+4-\frac{1}{2}y^{2}\right)dy$ 为被积表达式,在闭区间 $[-2,4]$ 上作定积分,便得所求的面积为

$$
A = \int_ {- 2} ^ {4} \left(y + 4 - \frac {1}{2} y ^ {2}\right) \mathrm{d} y = \left[ \frac {y ^ {2}}{2} + 4 y - \frac {y ^ {3}}{6} \right] _ {- 2} ^ {4} = 1 8.
$$

由例 2 可以看到, 积分变量选得适当, 可使计算方便.

例3 求椭圆 $\frac{x^2}{a^2} +\frac{y^2}{b^2} = 1$ 所围成的图形的面积.

解 该椭圆关于两坐标轴都对称(图6-4)，所以椭圆所围成的图形的面积为

$$
A = 4 A _ {1},
$$

其中  $A_{1}$  为该椭圆在第一象限部分与两坐标轴所围图形的面积, 因此

$$
A = 4 A _ {1} = 4 \int_ {0} ^ {a} y \mathrm{d} x.
$$

利用椭圆的参数方程

$$
\left\{ \begin{array}{l l} x = a \cos t, \\ y = b \sin t \end{array} \right. \quad \left(0 \leqslant t \leqslant \frac {\pi}{2}\right),
$$

应用定积分换元法,令  $x = a \cos t$ , 则

$$
y = b \sin t, \quad \mathrm{d} x = - a \sin t \mathrm{d} t.
$$

![](images/page_287_image_9.jpg)

<details>
<summary>text_image</summary>

y
b
O x x+dx a x
</details>

图6-4

当 $x$ 由0变到 $a$ 时，$t$ 由 $\frac{\pi}{2}$ 变到0，所以

$$
\begin{array}{l} A = 4 \int_ {\frac {\pi}{2}} ^ {0} b \sin t (- a \sin t) \mathrm{d} t = - 4 a b \int_ {\frac {\pi}{2}} ^ {0} \sin^ {2} t \mathrm{d} t \\ = 4 a b \int_ {0} ^ {\frac {\pi}{2}} \sin^ {2} t \mathrm{d} t = 4 a b \cdot \frac {1}{2} \cdot \frac {\pi}{2} = \pi a b. \\ \end{array}
$$

当 a=b 时, 就得到大家所熟悉的圆面积的公式  $A=\pi a^{2}$ .

## 2. 极坐标情形

某些平面图形,用极坐标来计算它们的面积比较方便.

设由曲线 $\rho = \rho (\theta)$ 及射线 $\theta = \alpha ,\theta = \beta$ 围成一图形（简称为曲边扇形），现在要计算它的面积(图6-5).这里， $\rho (\theta)$ 在 $[\alpha ,\beta ]$ 上连续，且 $\rho (\theta)\geqslant 0,0 <   \beta -\alpha \leqslant 2\pi .$

由于当  $\theta$  在  $[\alpha, \beta]$  上变动时, 极径  $\rho = \rho(\theta)$  也随之变动, 因此所求图形的面积不能直接利用扇形面积的公式  $A = \frac{1}{2} R^{2} \theta$  来计算.

![](images/page_287_image_18.jpg)

<details>
<summary>text_image</summary>

ρ=ρ(θ)
dθ
α β θ θ+dθ
O A
</details>

图6-5

取极角 $\theta$ 为积分变量，它的变化区间为 $[\alpha, \beta]$. 相应于任一小区间 $[\theta, \theta + \mathrm{d}\theta]$ 的窄曲边扇形的面积可以用半径为 $\rho = \rho(\theta)$、中心角为 $\mathrm{d}\theta$ 的扇形的面积来近似代替，从而得到这窄曲边扇形面积的近似值，即曲边扇形的面积元素

$$
\mathrm{d} A = \frac {1}{2} [ \rho (\theta) ] ^ {2} \mathrm{d} \theta .
$$

以 $\frac{1}{2} [\rho (\theta)]^2\mathrm{d}\theta$ 为被积表达式，在闭区间 $[\alpha ,\beta ]$ 上作定积分，便得所求曲边扇形的面