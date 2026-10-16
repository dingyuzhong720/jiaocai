$$
= 1 + \frac {1 - \frac {1}{2 ^ {n}}}{1 - \frac {1}{2}} = 3 - \frac {1}{2 ^ {n - 1}} <   3,
$$

这就说明数列 $\{x_{n}\}$ 是有界的.根据极限存在准则Ⅱ，这个数列 $\{x_{n}\}$ 的极限存在，通常用字母e来表示它，即

$$
\lim _ {n \to \infty} \left(1 + \frac {1}{n}\right) ^ {n} = \mathrm{e}.
$$

可以证明, 当 x 取实数而趋于  $+\infty$  或  $-\infty$  时, 函数  $\left(1+\frac{1}{x}\right)^{x}$  的极限都存在且都等于  $e^{①}$ . 因此②,

$$
\lim _ {x \to \infty} \left(1 + \frac {1}{x}\right) ^ {x} = \mathrm{e}. \tag {6-3}
$$

这个数 e 是无理数, 它的值是

$$
\mathrm{e} = 2. 7 1 8 2 8 1 8 2 8 4 5 9 0 4 5 \dots
$$

在第一节中提到的指数函数 $y = \mathrm{e}^x$ 以及自然对数 $y = \ln x$ 中的底 $\mathbf{e}$ 就是这个常数.

利用复合函数的极限运算法则, 可把(6-3)式写成另一形式. 在 $(1+z)^{\frac{1}{z}}$ 中作代换

① 设 $n \leqslant x < n + 1$，则

$$
\left(1 + \frac {1}{n + 1}\right) ^ {n} <   \left(1 + \frac {1}{x}\right) ^ {x} <   \left(1 + \frac {1}{n}\right) ^ {n + 1},
$$

且 $n$ 与 $x$ 同时趋于 $+\infty$ ，因为

$$
\lim _ {n \to \infty} \left(1 + \frac {1}{n + 1}\right) ^ {n} = \lim _ {n \to \infty} \frac {\left(1 + \frac {1}{n + 1}\right) ^ {n + 1}}{1 + \frac {1}{n + 1}} = e,
$$

$$
\lim _ {n \to \infty} \left(1 + \frac {1}{n}\right) ^ {n + 1} = \lim _ {n \to \infty} \left[ \left(1 + \frac {1}{n}\right) ^ {n} \cdot \left(1 + \frac {1}{n}\right) \right] = e,
$$

应用夹逼准则,即得

$$
\lim _ {x \to + \infty} \left(1 + \frac {1}{x}\right) ^ {x} = e.
$$

令 $x = -(t + 1)$ ，则 $x\to -\infty$ 时， $t\to +\infty$ .从而

$$
\begin{array}{l} \lim _ {x \to - \infty} \left(1 + \frac {1}{x}\right) ^ {x} = \lim _ {t \to + \infty} \left(1 - \frac {1}{t + 1}\right) ^ {- (t + 1)} = \lim _ {t \to + \infty} \left(\frac {t}{t + 1}\right) ^ {- (t + 1)} \\ = \lim _ {t \to + \infty} \left(1 + \frac {1}{t}\right) ^ {t + 1} = \lim _ {t \to + \infty} \left[ \left(1 + \frac {1}{t}\right) ^ {t} \cdot \left(1 + \frac {1}{t}\right) \right] = e. \\ \end{array}
$$

② 参阅习题 1-3 第 10 题.

$x = \frac{1}{z}$, 得 $\left(1 + \frac{1}{x}\right)^x$. 又当 $z \to 0$ 时 $x \to \infty$. 因此由复合函数的极限运算法则得

$$
\lim _ {z \to 0} (1 + z) ^ {\frac {1}{z}} = \lim _ {x \to \infty} \left(1 + \frac {1}{x}\right) ^ {x} = \mathrm{e}.
$$

下面的例 4 也是用代换方法来做的,实质上还是用到了复合函数的极限运算法则.

例4 求 $\lim_{x\to \infty}\left(1 - \frac{1}{x}\right)^x.$

解 令 $t = -x$ ，则当 $x \to \infty$ 时，$t \to \infty$ .于是

$$
\lim _ {x \to \infty} \left(1 - \frac {1}{x}\right) ^ {x} = \lim _ {t \to \infty} \left(1 + \frac {1}{t}\right) ^ {- t} = \lim _ {t \to \infty} \frac {1}{\left(1 + \frac {1}{t}\right) ^ {t}} = \frac {1}{\mathrm{e}}.
$$

相应于单调有界数列必有极限的准则Ⅱ，函数极限也有类似的准则。对于自变量的不同变化过程 $(x\to x_{0}^{-},x\to x_{0}^{+},x\to-\infty,x\to+\infty)$ ，准则有不同的形式。现以 $x\to x_{0}^{-}$ 为例，将相应的准则叙述如下:

准则Ⅱ' 设函数 $f(x)$ 在点 $x_0$ 的某个左邻域内单调并且有界, 则 $f(x)$ 在 $x_0$ 的左极限 $f(x_0^-)$ 必定存在.

\* 柯西(Cauchy)①极限存在准则

在第二节例 1 及例 2 中, 我们看到收敛数列不一定是单调的. 因此, 准则Ⅱ所给出的单调有界这条件, 是数列收敛的充分条件, 而不是必要的. 当然, 其中有界这一条件对数列的收敛性来说是必要的. 下面叙述的柯西极限存在准则, 它给出了数列收敛的充分必要条件.

柯西极限存在准则 数列  $\{x_{n}\}$  收敛的充分必要条件是: 对于任意给定的正数  $\varepsilon$ ，存在正整数 N，使得当 m > N, n > N 时，有

$$
\left| x _ {n} - x _ {m} \right| <   \varepsilon .
$$

证 必要性 设 $\lim_{n\to \infty}x_n = a.\forall \varepsilon >0$ ，由数列极限的定义， $\exists$ 正整数 $N$ ，当 $n > N$ 时，有

$$
\mid x _ {n} - a \mid <   \frac {\varepsilon}{2};
$$

同样, 当 m > N 时, 也有

$$
\mid x _ {m} - a \mid <   \frac {\varepsilon}{2}.
$$

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 柯西(Augustin-Louis Cauchy,1789—1857),法国数学家,他出版了《分析教程》(1821)、《无穷小分析教程概论》(1823)、《微积分在几何中的应用》(1826—1828)这几部划时代的著作,给出了分析学一系列基本概念的严格定义,将微积分理论完整而严密地奠基于极限的基础之上,从而使他成为严格微积分学的奠基者.</span></small>

因此, 当 m > N, n > N 时, 有

$$
\left| x _ {n} - x _ {m} \right| = \left| (x _ {n} - a) - (x _ {m} - a) \right| \leqslant \left| x _ {n} - a \right| + \left| x _ {m} - a \right| <   \frac {\varepsilon}{2} + \frac {\varepsilon}{2} = \varepsilon,
$$

所以条件是必要的.

充分性这里不予证明.

这准则的几何意义表示,数列 $\{x_{n}\}$ 收敛的充分必要条件是:对于任意给定的正数 $\varepsilon$ ,在数轴上一切具有足够大序号的点 $x_{n}$ 中,任意两点间的距离小于 $\varepsilon$ .

柯西极限存在准则有时也叫做柯西审敛原理.

## 习题1-6

1. 计算下列极限:

(1)  $\lim_{x\to0}\frac{\sin\omega x}{x};$

(2)  $\lim_{x\to0}\frac{\tan3x}{x};$

(3)  $\lim_{x\to0}\frac{\sin2x}{\sin5x};$

(4)  $\lim_{x\to0}x\cot x;$

(5)  $\lim_{x\to0}\frac{1-\cos2x}{x\sin x};$

(6) $\lim_{n\to \infty}2^n\sin \frac{x}{2^n}$ ($x$ 为不等于零的常数, $n\in \mathbf{N}_+$).

2. 计算下列极限:

(1)  $\lim_{x\to0}(1-x)^{\frac{1}{x}}$ ;

(2) $\lim_{x\to 0}(1 + 2x)^{\frac{1}{x}}$

(3)  $\lim_{x\to\infty}\left(\frac{1+x}{x}\right)^{2x}$ ;

(4) $\lim_{x\to \infty}\left(1 - \frac{1}{x}\right)^{kx}(k$ 为正整数).

\*3. 根据函数极限的定义,证明极限存在的准则 I'.

4. 利用极限存在准则证明:

(1)  $\lim_{n\to\infty}\sqrt{1+\frac{1}{n}}=1;$

(2)  $\lim_{n\to\infty}n\left(\frac{1}{n^{2}+\pi}+\frac{1}{n^{2}+2\pi}+\cdots+\frac{1}{n^{2}+n\pi}\right)=1;$

(3)  $\lim_{x\to0}\sqrt[n]{1+x}=1;$

(4)  $\lim_{x\to0^{+}}x\left[\frac{1}{x}\right]=1.$

5. 设数列 $\{x_{n}\}$ 满足: $x_{1} = \sqrt{2}, x_{n+1} = \sqrt{2 + x_{n}} (n \in \mathbf{N}_{+})$. 证明 $\lim_{n \to \infty} x_{n}$ 存在, 并求此极限.

6. 设数列 $\{x_{n}\}$ 满足: $x_{1} \in (0, \pi), x_{n+1} = \sin x_{n} \quad (n \in \mathbb{N}_{+})$. 证明 $\lim_{n \to \infty} x_{n}$ 存在, 并求此极限.

## 第七节 无穷小的比较

在第五节中我们已经知道,两个无穷小的和、差及乘积仍旧是无穷小.但是,关于两个无穷小的商,却会出现不同的情况,例如,当 $x\to0$ 时, $3x,x^{2},\sin x$ 都是无穷小,而

$$
\lim _ {x \to 0} \frac {x ^ {2}}{3 x} = 0, \quad \lim _ {x \to 0} \frac {3 x}{x ^ {2}} = \infty , \quad \lim _ {x \to 0} \frac {\sin x}{3 x} = \frac {1}{3}.
$$

两个无穷小之比的极限的各种不同情况,反映了不同的无穷小趋于零的“快慢”程度.就上面几个例子来说,在 $x \to 0$ 的过程中, $x^{2} \to 0$ 比 $3x \to 0$ “快些”,反过来 $3x \to 0$ 比 $x^{2} \to 0$ “慢些”,而 $\sin x \to 0$ 与 $3x \to 0$ “快慢相仿”.

下面,我们就无穷小之比的极限存在或为无穷大时,来说明两个无穷小之间的比较.应当注意,下面的  $\alpha$  及  $\beta$  都是在同一个自变量的变化过程中的无穷小,且  $\alpha \neq 0$ ,  $\lim \frac{\beta}{\alpha}$  也是在这个变化过程中的极限.

定义

如果  $\lim_{\alpha}\frac{\beta}{\alpha}=0$  ,那么就说  $\beta$  是比  $\alpha$  高阶的无穷小,记作  $\beta=o(\alpha)$ ;

如果  $\lim \frac{\beta}{\alpha} = \infty$ ，那么就说  $\beta$  是比  $\alpha$  低阶的无穷小；

如果  $\lim \frac{\beta}{\alpha} = c \neq 0$ ，那么就说  $\beta$  与  $\alpha$  是同阶无穷小；

如果  $\lim_{\alpha^{k}}\frac{\beta}{\alpha^{k}}=c\neq0, k>0$  ,那么就说  $\beta$  是关于  $\alpha$  的 k 阶无穷小；

如果  $\lim_{\alpha}\frac{\beta}{\alpha}=1$  ,那么就说  $\beta$  与  $\alpha$  是等价无穷小,记作  $\alpha\sim\beta$ .

显然,等价无穷小是同阶无穷小的特殊情形,即 c=1 的情形.

下面举一些例子:

因为 $\lim_{x\to0}\frac{3x^{2}}{x}=0$ ，所以当 $x\to0$ 时， $3x^{2}$ 是比x高阶的无穷小，即

$$
3 x ^ {2} = o (x) (x \to 0).
$$

因为 $\lim_{n\to \infty}\frac{\frac{1}{n}}{\frac{1}{n^2}} = \infty$ ，所以当 $n\to \infty$ 时， $\frac{1}{n}$ 是比 $\frac{1}{n^2}$ 低阶的无穷小.

因为 $\lim_{x\to3}\frac{x^{2}-9}{x-3}=6$ ，所以当 $x\to3$ 时， $x^{2}-9$ 与x-3是同阶无穷小.

因为 $\lim_{x\to 0}\frac{1 - \cos x}{x^2} = \frac{1}{2}$ ，所以当 $x\to 0$ 时， $1 - \cos x$ 是关于 $x$ 的二阶无穷小

因为 $\lim_{x\to0}\frac{\sin x}{x}=1$ ，所以当 $x\to0$ 时， $\sin x$ 与x是等价无穷小，即

$$
\sin x \sim x (x \to 0).
$$

下面再举一个常用的等价无穷小的例子.

例1 证明: 当 $x \to 0$ 时, $\sqrt[n]{1 + x} - 1 \sim \frac{1}{n} x$.

证 因为

$$
\begin{array}{l} \lim _ {x \to 0} \frac {\sqrt [ n ]{1 + x} - 1}{\frac {1}{n} x} = \lim _ {x \to 0} \frac {(\sqrt [ n ]{1 + x}) ^ {n} - 1}{\frac {1}{n} x [ \sqrt [ n ]{(1 + x) ^ {n - 1}} + \sqrt [ n ]{(1 + x) ^ {n - 2}} + \cdots + 1 ]} \\ = \lim _ {x \to 0} \frac {n}{\sqrt [ n ]{(1 + x) ^ {n - 1}} + \sqrt [ n ]{(1 + x) ^ {n - 2}} + \cdots + 1} = 1 ①, \\ \end{array}
$$

所以 $\sqrt[n]{1 + x} - 1 \sim \frac{1}{n} x (x \to 0)$.

关于等价无穷小,有下面两个定理:

定理1 $\beta$ 与 $\alpha$ 是等价无穷小的充分必要条件为

$$
\beta = \alpha + o (\alpha).
$$

证 必要性 设 $\alpha \sim \beta$ ，则

$$
\lim \frac {\beta - \alpha}{\alpha} = \lim \left(\frac {\beta}{\alpha} - 1\right) = \lim \frac {\beta}{\alpha} - 1 = 0,
$$

因此 $\beta -\alpha = o(\alpha)$ ，即 $\beta = \alpha +o(\alpha)$

充分性 设  $\beta=\alpha+o(\alpha)$ ，则

$$
\lim \frac {\beta}{\alpha} = \lim \frac {\alpha + o (\alpha)}{\alpha} = \lim \left(1 + \frac {o (\alpha)}{\alpha}\right) = 1,
$$

因此 $\alpha \sim \beta$.

例2 因为当 $x \to 0$ 时, $\sin x \sim x, \tan x \sim x, \arcsin x \sim x, 1 - \cos x \sim \frac{1}{2} x^2$, 所以当 $x \to 0$ 时有

$$
\begin{array}{l} \sin x = x + o (x), \quad \tan x = x + o (x), \\ \arcsin x = x + o (x), \quad 1 - \cos x = \frac {1}{2} x ^ {2} + o (x ^ {2}). \\ \end{array}
$$

定理2 设 $\alpha \sim \widetilde{\alpha}, \beta \sim \widetilde{\beta}$, 且 $\lim_{\widetilde{\alpha}} \frac{\widetilde{\beta}}{\widetilde{\alpha}}$ 存在, 则

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 极限 $\lim_{x\to0}\sqrt[n]{(1+x)^{m}}=1(m=n-1,n-2,\cdots,1)$ 用到了习题1-6中题4(3)的结果及第五节中定理3的推论2.</span></small>

$$
\lim \frac {\beta}{\alpha} = \lim \frac {\widetilde {\beta}}{\widetilde {\alpha}}.
$$

证 $\lim \frac{\beta}{\alpha} = \lim \left(\frac{\beta}{\widetilde{\beta}}\cdot \frac{\widetilde{\beta}}{\widetilde{\alpha}}\cdot \frac{\widetilde{\alpha}}{\alpha}\right) = \lim \frac{\beta}{\widetilde{\beta}}\cdot \lim \frac{\widetilde{\beta}}{\widetilde{\alpha}}\cdot \lim \frac{\widetilde{\alpha}}{\alpha} = \lim \frac{\widetilde{\beta}}{\widetilde{\alpha}}.$

定理 2 表明, 求两个无穷小之比的极限时, 分子及分母都可用等价无穷小来代替. 因此, 如果用来代替的无穷小选得适当的话, 就可以使计算简化.

例 3 求  $\lim_{x\to0}\frac{\tan2x}{\sin5x}$ .

解 当 $x \to 0$ 时, $\tan 2x \sim 2x$, $\sin 5x \sim 5x$, 所以

$$
\lim _ {x \to 0} \frac {\tan 2 x}{\sin 5 x} = \lim _ {x \to 0} \frac {2 x}{5 x} = \frac {2}{5}.
$$

例 4 求  $\lim_{x\to0}\frac{\sin x}{x^{3}+3x}$ .

解 当 $x \to 0$ 时, $\sin x \sim x$, 无穷小 $x^3 + 3x$ 与它本身显然是等价的, 所以

$$
\lim _ {x \to 0} \frac {\sin x}{x ^ {3} + 3 x} = \lim _ {x \to 0} \frac {x}{x (x ^ {2} + 3)} = \lim _ {x \to 0} \frac {1}{x ^ {2} + 3} = \frac {1}{3}.
$$

例 5 求  $\lim_{x\to0}\frac{(1+x^{2})^{\frac{1}{3}}-1}{\cos x-1}$ .

解 当 $x \to 0$ 时, $(1 + x^2)^{\frac{1}{3}} - 1 \sim \frac{1}{3} x^2$, $\cos x - 1 \sim -\frac{1}{2} x^2$, 所以

$$
\lim _ {x \to 0} \frac {(1 + x ^ {2}) ^ {\frac {1}{3}} - 1}{\cos x - 1} = \lim _ {x \to 0} \frac {\frac {1}{3} x ^ {2}}{- \frac {1}{2} x ^ {2}} = - \frac {2}{3}.
$$

## 习题1-7

1. 当 $x \to 0$ 时, $2x - x^2$ 与 $x^2 - x^3$ 相比, 哪一个是高阶无穷小?
2. 当 $x \to 0$ 时, $(1 - \cos x)^2$ 与 $\sin^2 x$ 相比, 哪一个是高阶无穷小?
3. 当 $x \to 1$ 时, 无穷小 $1 - x$ 和 (1) $1 - x^3$, (2) $\frac{1}{2} (1 - x^2)$ 是否同阶, 是否等价?
4. 证明: 当  $x \to 0$  时, 有

(1) arctan $x \sim x$;

(2) $\sec x - 1 \sim \frac{x^2}{2}$.

5. 利用等价无穷小的性质, 求下列极限:

(1) $\lim_{x\to 0}\frac{\tan{3}x}{2x}$;

(2) $\lim_{x\to 0}\frac{\sin(x^n)}{(\sin x)^m} (n,m$ 为正整数）；

(3)  $\lim_{x\to0}\frac{\tan x-\sin x}{\sin^{3}x};$

(4) $\lim_{x\to 0}\frac{\sin x - \tan x}{\left(\sqrt[3]{1 + x^2} - 1\right)\left(\sqrt{1 + \sin x} - 1\right)}.$

6. 证明无穷小的等价关系具有下列性质:

(1)  $\alpha \sim \alpha$  (自反性);

(2) 若  $\alpha \sim \beta$ ，则  $\beta \sim \alpha$ （对称性）；

(3) 若  $\alpha\sim\beta,\beta\sim\gamma$ ，则  $\alpha\sim\gamma$ （传递性）.

## 第八节 函数的连续性与间断点

## 一、函数的连续性

自然界中有许多现象,如气温的变化、河水的流动、植物的生长等都是连续地变化着的.这种现象在函数关系上的反映,就是函数的连续性.例如就气温的变化来看,当时间变动很微小时,气温的变化也很微小,这种特点就是所谓连续性.下面我们先引入增量的概念,然后来描述连续性,并引出函数的连续性的定义.

设变量 u 从它的一个初值  $u_{1}$  变到终值  $u_{2}$ ，终值与初值的差  $u_{2}-u_{1}$  就叫做变量 u 的增量，记作  $\Delta u$ ，即

$$
\Delta u = u _ {2} - u _ {1}.
$$

增量  $\Delta u$  可以是正的,也可以是负的.在  $\Delta u$  为正的情形,变量 u 从  $u_{1}$  变到  $u_{2}=u_{1}+\Delta u$  时是增大的;当  $\Delta u$  为负时,变量 u 是减小的.

应该注意到:记号  $\Delta u$  并不表示某个量  $\Delta$  与变量 u 的乘积, 而是一个整体不可分割的记号.

现在假定函数 $y = f(x)$ 在点 $x_0$ 的某一个邻域内是有定义的. 当自变量 $x$ 在这邻域内从 $x_0$ 变到 $x_0 + \Delta x$ 时, 函数值或因变量 $f(x)$ 相应地从 $f(x_0)$ 变到 $f(x_0 + \Delta x)$, 因此函数

值或因变量 $f(x)$ 的对应增量为

$$
\Delta y = f (x _ {0} + \Delta x) - f (x _ {0}).
$$

习惯上也称  $\Delta y$  为函数的增量, 函数增量的几何解释如图 1-33 所示.

假如保持  $x_{0}$  不变而让自变量的增量  $\Delta x$  变动, 一般说来, 函数的增量  $\Delta y$  也要随着变动. 现在我们对连续性的概念可以这样描述: 如果当  $\Delta x$  趋于零时, 函数的对应增量  $\Delta y$  也趋于零, 即

![](images/page_70_chart_22.jpg)

<details>
<summary>line</summary>

| Point | X-coordinate | Y-coordinate |
| --- | --- | --- |
| Tangent point (f(x0)) | x0 | f(x0) |
| Tangent point (f(x0+Δx)) | \(x0+\Delta x\) | \(f(x0+\Delta x)\) |
</details>

图1-33

$$
\lim _ {\Delta x \to 0} \Delta y = 0 \tag {8-1}
$$

或

$$
\lim _ {\Delta x \to 0} \left[ f (x _ {0} + \Delta x) - f (x _ {0}) \right] = 0,
$$

那么就称函数  $y=f(x)$  在点  $x_{0}$  处是连续的, 即有下述定义:

定义 设函数 $y = f(x)$ 在点 $x_0$ 的某一邻域内有定义, 如果

$$
\lim _ {\Delta x \to 0} \Delta y = \lim _ {\Delta x \to 0} \left[ f (x _ {0} + \Delta x) - f (x _ {0}) \right] = 0,
$$

那么就称函数  $y=f(x)$  在点  $x_{0}$  连续.

为了应用方便起见,下面把函数  $y=f(x)$  在点  $x_{0}$  连续的定义用不同的方式来叙述.

设 $x = x_0 + \Delta x$ ，则 $\Delta x\to 0$ 就是 $x\to x_0$ .又由于

$$
\Delta y = f (x _ {0} + \Delta x) - f (x _ {0}) = f (x) - f (x _ {0}),
$$

即

$$
f (x) = f (x _ {0}) + \Delta y,
$$

可见 $\Delta y\to 0$ 就是 $f(x)\rightarrow f(x_0)$ ，因此(8-1)式与

$$
\lim _ {x \to x _ {0}} f (x) = f (x _ {0})
$$

相当.所以,函数  $y=f(x)$  在点  $x_{0}$  连续的定义又可叙述如下:

设函数  $y=f(x)$  在点  $x_{0}$  的某一邻域内有定义, 如果

$$
\lim _ {x \to x _ {0}} f (x) = f (x _ {0}), \tag {8-2}
$$

那么就称函数 $f(x)$ 在点 $x_{0}$ 连续.

由函数 $f(x)$ 当 $x \to x_0$ 时的极限的定义可知，上述定义也可用“$\varepsilon - \delta$”语言表达如下:$f(x)$ 在点 $x_0$ 连续 $\Leftrightarrow \forall \varepsilon > 0, \exists \delta > 0$，当 $|x - x_0| < \delta$ 时，有 $|f(x) - f(x_0)| < \varepsilon$.

下面说明左连续及右连续的概念.

如果 $\lim_{x\to x_0^-}f(x) = f(x_0^-)$ 存在且等于 $f(x_0)$，即

$$
f (x _ {0} ^ {-}) = f (x _ {0}),
$$

那么就说函数 $f(x)$ 在点 $x_0$ 左连续. 如果 $\lim_{x\to x_0^+}f(x) = f(x_0^+)$ 存在且等于 $f(x_0)$，即

$$
f (x _ {0} ^ {+}) = f (x _ {0}),
$$

那么就说函数 $f(x)$ 在点 $x_{0}$ 右连续.

在区间上每一点都连续的函数,叫做在该区间上的连续函数,或者说函数在该区间上连续.如果区间包括端点,那么函数在右端点连续是指左连续,在左端点连续是指右连续.

连续函数的图形是一条连续而不间断的曲线.

在第五节中,我们曾经证明:如果 $f(x)$ 是有理整函数(多项式),那么对于任意的实数 $x_0$ ，都有 $\lim_{x\to x_0}f(x) = f(x_0)$ ，因此有理整函数在区间 $(-\infty , + \infty)$ 内是连续的.对于有理分式函数 $F(x) = \frac{P(x)}{Q(x)}$ ，只要 $Q(x_0)\neq 0$ ，就有 $\lim_{x\to x_0}F(x) = F(x_0)$ ，因此有理分式函数在其定义域内的每一点都是连续的

由第三节例5可知，函数 $f(x) = \sqrt{x}$ 在 $(0, +\infty)$ 内是连续的.

作为例子,我们来证明,函数  $y=\sin x$  在区间  $(-∞,+∞)$  内是连续的.

设 $x$ 是区间 $(-\infty, +\infty)$ 内任意取定的一点. 当 $x$ 有增量 $\Delta x$ 时, 对应的函数的增量为

$$
\Delta y = \sin (x + \Delta x) - \sin x,
$$

由三角公式有

$$
\sin (x + \Delta x) - \sin x = 2 \sin \frac {\Delta x}{2} \cos \left(x + \frac {\Delta x}{2}\right),
$$

注意到

$$
\left| \cos \left(x + \frac {\Delta x}{2}\right) \right| \leqslant 1,
$$

就推得

$$
\mid \Delta y \mid = \mid \sin (x + \Delta x) - \sin x \mid \leqslant 2 \left| \sin \frac {\Delta x}{2} \right|.
$$

因为对于任意的角 $\alpha$ ，当 $\alpha \neq 0$ 时有 $|\sin \alpha| < |\alpha|$，所以

$$
0 \leqslant | \Delta y | = | \sin (x + \Delta x) - \sin x | <   | \Delta x |.
$$

因此, 当 $\Delta x \to 0$ 时, 由夹逼准则得 $|\Delta y| \to 0$, 这就证明了 $y = \sin x$ 对于任一 $x \in (-\infty, +\infty)$ 是连续的.

类似地可以证明,函数  $y=\cos x$  在区间  $(-∞,+∞)$  内是连续的.

## 二、函数的间断点

设函数 $f(x)$ 在点 $x_0$ 的某去心邻域内有定义.在此前提下，如果函数 $f(x)$ 有下列三种情形之一:

(1) 在  $x = x_{0}$  没有定义；
(2) 虽在  $x = x_{0}$  有定义, 但  $\lim_{x \to x_{0}} f(x)$  不存在;
(3) 虽在  $x = x_{0}$  有定义，且  $\lim_{x \to x_{0}} f(x)$  存在，但  $\lim_{x \to x_{0}} f(x) \neq f(x_{0})$ ,

那么函数 $f(x)$ 在点 $x_0$ 为不连续，而点 $x_0$ 称为函数 $f(x)$ 的不连续点或间断点.

下面举例来说明函数间断点的几种常见类型.

例1 正切函数 $y = \tan x$ 在 $x = \frac{\pi}{2}$ 处没有定义，所以点 $x = \frac{\pi}{2}$ 是函数 $\tan x$ 的间断

点.因

$$
\lim_{x\to \frac{\pi}{2}}\tan x = \infty ,
$$

我们称  $x=\frac{\pi}{2}$  为函数  $\tan x$  的无穷间断点（图 1-34）.

例 2 函数  $y=\sin\frac{1}{x}$  在点 x=0 没有定义; 当  $x\to0$  时, 函数值在 -1 与 1 之间变动无限多次(图 1-35), 所以点 x=0 称为函数  $\sin\frac{1}{x}$  的振荡间断点.

![](images/page_73_chart_5.jpg)

<details>
<summary>contour</summary>

| X | Y |
| --- | --- |
| \(-\pi/2\) | ~-1.5 |
| 0 | 0 |
| \(\pi/2\) | ~1.5 |
| \(\pi/3\) | ~-1.5 |
| \(3\pi/2\) | ~1.5 |
</details>

图1-34

![](images/page_73_chart_7.jpg)

<details>
<summary>contour</summary>

| X-axis | Y-axis |
| --- | --- |
| O | 1 |
| \(1/\pi\) | 0 |
| \(2/\pi\) | 1 |
| \(3/\pi\) | ~0.8 |
| \(4/\pi\) | ~0.6 |
| \(5/\pi\) | ~0.4 |
| \(6/\pi\) | ~0.2 |
</details>

图1-35

例3 函数 $y = \frac{x^2 - 1}{x - 1}$ 在点 $x = 1$ 没有定义, 所以函数在点 $x = 1$ 不连续 (图1-36). 但这里

$$
\lim _ {x \to 1} \frac {x ^ {2} - 1}{x - 1} = \lim _ {x \to 1} (x + 1) = 2.
$$

如果补充定义: 令 x=1 时 y=2, 那么所给函数在 x=1 成为连续. 所以 x=1 称为该函数的可去间断点.

![](images/page_73_chart_12.jpg)

<details>
<summary>line</summary>

| X | Y |
| --- | --- |
| 1 | 2 |
</details>

图1-36

例4 函数

$$
y = f (x) = \left\{ \begin{array}{l l} x, & x \neq 1, \\ \frac {1}{2}, & x = 1. \end{array} \right.
$$

这里 $\lim_{x\to 1}f(x) = \lim_{x\to 1}x = 1$ ，但 $f(1) = \frac{1}{2}$ ，所以

$$
\lim _ {x \to 1} f (x) \neq f (1).
$$

因此, 点 x=1 是函数  $f(x)$  的间断点(图 1-37). 但如果改变函数  $f(x)$  在 x=1 处的定义: 令  $f(1)=1$ , 那么  $f(x)$  在 x=1 成为连续. 所以 x=1 也称为该函数的可去间断点.

例5 函数

$$
f (x) = \left\{ \begin{array}{l l} x - 1, & x <   0, \\ 0, & x = 0, \\ x + 1 & x > 0. \end{array} \right.
$$

这里, 当  $x \to 0$  时,

$$
\lim _ {x \to 0 ^ {-}} f (x) = \lim _ {x \to 0 ^ {-}} (x - 1) = - 1, \quad \lim _ {x \to 0 ^ {+}} f (x) = \lim _ {x \to 0 ^ {+}} (x + 1) = 1.
$$

左极限与右极限虽都存在,但不相等,故极限 $\lim_{x\to0}f(x)$ 不存在,所以点x=0是函数 $f(x)$ 的间断点(图1-38).因 $y=f(x)$ 的图形在x=0处产生跳跃现象,我们称x=0为函数 $f(x)$ 的跳跃间断点.

![](images/page_74_chart_5.jpg)

<details>
<summary>scatter</summary>

| Point | X | Y |
| --- | --- | --- |
| Open Circle | 1 | 1 |
| Solid Dot | 1 | 0.5 |
</details>

图1-37

![](images/page_74_image_7.jpg)

<details>
<summary>text_image</summary>

y
y=x+1
1
O
x
-1
y=x-1
</details>

图1-38

上面举了一些间断点的例子.通常把间断点分成两类:如果 $x_0$ 是函数 $f(x)$ 的间断点,但左极限 $f(x_0^-)$ 及右极限 $f(x_0^+)$ 都存在,那么 $x_0$ 称为函数 $f(x)$ 的第一类间断点.不是第一类间断点的任何间断点,称为第二类间断点.在第一类间断点中,左、右极限相等者称为可去间断点,不相等者称为跳跃间断点.无穷间断点和振荡间断点显然是第二类间断点.

## 习题1-8

1. 设  $y=f(x)$  的图形如图 1-39 所示, 试指出  $f(x)$  的全部间断点, 并对可去间断点补充或修改函数值的定义, 使它成为连续点.

2. 研究下列函数的连续性,并画出函数的图形:

(1) $f(x)=\begin{cases}x^{2},&0\leqslant x\leqslant1,\\2-x,&1<x\leqslant2;\end{cases}$

(2) $f(x)=\begin{cases}x,&-1\leqslant x\leqslant1,\\1,&x<-1\text{或}x>1.\end{cases}$

![](images/page_74_chart_15.jpg)

<details>
<summary>line</summary>

| X | Y |
| --- | --- |
| -1 | 0 |
| 0 | 0 |
| 1 | 2 |
| 2 | 0 |
</details>

图1-39

3. 下列函数在指出的点处间断,说明这些间断点属于哪一类.如果是可去间断点,那么补充或改变函数的定义使它连续:

(1) $y = \frac{x^2 - 1}{x^2 - 3x + 2}, x = 1, x = 2;$

(2) $y = \frac{x}{\tan x}, x = k\pi, x = k\pi + \frac{\pi}{2} \quad (k = 0, \pm 1, \pm 2, \cdots)$;

(3)  $y = \cos^{2}\frac{1}{x}, x = 0;$

(4) $y = \begin{cases} x - 1, & x \leqslant 1, \\ 3 - x, & x > 1, \end{cases} \quad x = 1.$

4. 讨论函数 $f(x) = \lim_{n\to \infty}\frac{1 - x^{2n}}{1 + x^{2n}}x$ ($n \in \mathbb{N}_+$) 的连续性, 若有间断点, 则判别其类型.

5. 下列陈述中,哪些是对的,哪些是错的? 如果是对的,说明理由;如果是错的,试给出一个反例.

(1) 如果函数  $f(x)$  在 a 连续, 那么  $\left|f(x)\right|$  也在 a 连续;

(2) 如果函数  $\left|f(x)\right|$  在 a 连续, 那么  $f(x)$  也在 a 连续.

\*6. 证明: 若函数 $f(x)$ 在点 $x_0$ 连续且 $f(x_0) \neq 0$, 则存在 $x_0$ 的某一邻域 $U(x_0)$, 当 $x \in U(x_0)$ 时, $f(x) \neq 0$.

\*7. 设

$$
f (x) = \left\{ \begin{array}{l l} x, & x \in \mathbb {Q}, \\ 0, & x \in \mathbb {R} \backslash \mathbb {Q}, \end{array} \right.
$$

证明:

(1) $f(x)$ 在 x=0 连续；

(2) $f(x)$ 在非零的x处都不连续.

8. 设 $f(x)$ 对任意实数 $x, y$，有 $f(x + y) = f(x) + f(y)$，且 $f(x)$ 在 $x = 0$ 连续，证明:$f(x)$ 在 $\mathbb{R}$ 上连续.

## 第九节 连续函数的运算与初等函数的连续性

## 一、连续函数的和、差、积、商的连续性

由函数在某点连续的定义和极限的四则运算法则,立即可得出下面的定理:

定理1 设函数 $f(x)$ 和 $g(x)$ 在点 $x_0$ 连续，则它们的和（差）$f \pm g$、积 $f \cdot g$ 及商 $\frac{f}{g}$ （当 $g(x_0) \neq 0$ 时）都在点 $x_0$ 连续.

例1 因 $\tan x = \frac{\sin x}{\cos x}, \cot x = \frac{\cos x}{\sin x}$, 而 $y = \sin x$ 和 $y = \cos x$ 都在区间 $(- \infty, +\infty)$ 内连续(第八节), 故由定理1知 $y = \tan x$ 和 $y = \cot x$ 在它们的定义域内是连续的.

## 二、反函数与复合函数的连续性

反函数和复合函数的概念已经在第一节中讲过,这里来讨论它们的连续性.

定理2 如果函数 $y = f(x)$ 在区间 $I_{x}$ 上单调增加（或单调减少）且连续，那么它的反函数 $x = f^{-1}(y)$ 也在对应的区间 $I_{y} = \{y \mid y = f(x), x \in I_{x}\}$ 上单调增加（或单调减少）且连续.

证明从略.

例2 由于 $y = \sin x$ 在闭区间 $\left[-\frac{\pi}{2}, \frac{\pi}{2}\right]$ 上单调增加且连续，所以它的反函数 $y = \arcsin x$ 在闭区间 $[-1, 1]$ 上也是单调增加且连续的.

同样,应用定理2可证: $y = \arccos x$ 在闭区间 $[-1, 1]$ 上单调减少且连续, $y = \arctan x$ 在区间 $(- \infty, +\infty)$ 内单调增加且连续, $y = \operatorname{arccot} x$ 在区间 $(- \infty, +\infty)$ 内单调减少且连续.

总之,反三角函数  $y=\arcsin x, y=\arccos x, y=\arctan x, y=\operatorname{arccot} x$  在它们的定义域内都是连续的.

定理3 设函数 $y = f[g(x)]$ 由函数 $u = g(x)$ 与函数 $y = f(u)$ 复合而成，$\stackrel{\circ}{U}(x_0) \subset D_{f \circ g}$. 若 $\lim_{x \to x_0} g(x) = u_0$，而函数 $y = f(u)$ 在 $u = u_0$ 连续，则

$$
\lim _ {x \to x _ {0}} f [ g (x) ] = \lim _ {u \to u _ {0}} f (u) = f (u _ {0}). \tag {9-1}
$$

证 在第五节定理6中, 令 $A = f(u_0)$ (这时 $f(u)$ 在点 $u_0$ 连续), 并取消“存在 $\delta_0 > 0$, 当 $x \in \mathring{U}(x_0, \delta_0)$ 时, 有 $g(x) \neq u_0$”这个条件, 便得上面的定理. 这里可以取消条件 $g(x) \neq u_0$ 的理由是: $\forall \varepsilon > 0$, 使 $g(x) = u_0$ 成立的那些点 $x$, 显然也使 $|f[g(x)] - f(u_0)| < \varepsilon$ 成立. 因此就没有必要附加条件 $g(x) \neq u_0$ 了.

因为在定理3中有

$$
\lim _ {x \to x _ {0}} g (x) = u _ {0}, \quad \lim _ {u \to u _ {0}} f (u) = f (u _ {0}),
$$

故(9-1)式又可写成

$$
\lim _ {x \to x _ {0}} f [ g (x) ] = f [ \lim _ {x \to x _ {0}} g (x) ]. \tag {9-2}
$$

(9-1)式表示,在定理3的条件下,如果作代换 $u=g(x)$ ,那么求 $\lim_{x\to x_{0}}f[g(x)]$ 就化为求 $\lim_{u\to u_{0}}f(u)$ ,这里 $u_{0}=\lim_{x\to x_{0}}g(x)$ .

(9-2)式表示,在定理3的条件下,求复合函数 $f[g(x)]$ 的极限时,函数符号f与极限号 $\lim_{x\to x_{0}}$ 可以交换次序.

把定理3中的 $x \to x_0$ 换成 $x \to \infty$ ，可得类似的定理.

例3 求 $\lim_{x\to 3}\sqrt{\frac{x - 3}{x^2 - 9}}.$

解 $y = \sqrt{\frac{x - 3}{x^2 - 9}}$ 可看作由 $y = \sqrt{u}$ 与 $u = \frac{x - 3}{x^2 - 9}$ 复合而成. 因为 $\lim_{x \to 3} \frac{x - 3}{x^2 - 9} = \frac{1}{6}$, 而函数 $y = \sqrt{u}$ 在点 $u = \frac{1}{6}$ 连续, 所以

$$
\lim _ {x \to 3} \sqrt {\frac {x - 3}{x ^ {2} - 9}} = \sqrt {\lim _ {x \to 3} \frac {x - 3}{x ^ {2} - 9}} = \sqrt {\frac {1}{6}} = \frac {\sqrt {6}}{6}.
$$

定理4 设函数 $y = f[g(x)]$ 是由函数 $u = g(x)$ 与函数 $y = f(u)$ 复合而成，$U(x_0) \subset D_{f \cdot g}$. 若函数 $u = g(x)$ 在 $x = x_0$ 连续，且 $g(x_0) = u_0$，而函数 $y = f(u)$ 在 $u = u_0$ 连续，则复合函数 $y = f[g(x)]$ 在 $x = x_0$ 也连续.

证 只要在定理3中令 $u_0 = g(x_0)$，这就表示 $g(x)$ 在点 $x_0$ 连续，于是由(9-1)式得

$$
\lim _ {x \to x _ {0}} f [ g (x) ] = f (u _ {0}) = f [ g (x _ {0}) ],
$$

这就证明了复合函数 $f[g(x)]$ 在点 $x_{0}$ 连续.

例 4 讨论函数  $y=\sin\frac{1}{x}$  的连续性.

解 函数 $y = \sin \frac{1}{x}$ 可看作是由 $u = \frac{1}{x}$ 及 $y = \sin u$ 复合而成的. $u = \frac{1}{x}$ 当 $-\infty < x < 0$ 和 $0 < x < +\infty$ 时是连续的, $y = \sin u$ 当 $-\infty < u < +\infty$ 时是连续的. 根据定理4, 函数 $y = \sin \frac{1}{x}$ 在无限区间 $(-\infty, 0)$ 和 $(0, +\infty)$ 内是连续的.

## 三、初等函数的连续性

前面证明了三角函数及反三角函数在它们的定义域内是连续的.

我们指出(但不详细讨论), 指数函数  $y = a^{x} (a > 0, a \neq 1)$  对于一切实数 x 都有定义, 且在区间  $(-\infty, +\infty)$  内是单调的和连续的, 它的值域为  $(0, +\infty)$ .

由指数函数的单调性和连续性, 引用定理 2 可得: 对数函数  $y = \log_{a} x \quad (a > 0, a \neq 1)$  在区间  $(0, +\infty)$  内单调且连续.

幂函数 $y = x^{\mu}$ 的定义域随 $\mu$ 的值而异,但无论 $\mu$ 为何值,在区间 $(0, +\infty)$ 内幂函数总是有定义的.下面我们来证明,在 $(0, +\infty)$ 内幂函数是连续的.事实上,设 $x > 0$,则

$$
y = x ^ {\mu} = a ^ {\mu \log_ {a} x},
$$

因此，幂函数 $x^{\mu}$ 可看作是由 $y = a^{u}, u = \mu \log_{a} x$ 复合而成的，由此，根据定理4，它在 $(0, +\infty)$ 内连续.如果对于 $\mu$ 取各种不同值加以分别讨论，可以证明（证明从略）幂函

数在它的定义域内是连续的.

综合起来得到:基本初等函数在它们的定义域内都是连续的.

最后,根据第一节中关于初等函数的定义,由基本初等函数的连续性以及本节定理1、定理4可得下列重要结论:一切初等函数在其定义区间内都是连续的.所谓定义区间,就是包含在定义域内的区间.

根据函数 $f(x)$ 在点 $x_0$ 连续的定义, 如果已知 $f(x)$ 在点 $x_0$ 连续, 那么求 $f(x)$ 当 $x \to x_0$ 的极限时, 只要求 $f(x)$ 在点 $x_0$ 的函数值就行了. 因此, 上述关于初等函数连续性的结论提供了求极限的一个方法, 这就是: 如果 $f(x)$ 是初等函数, 且 $x_0$ 是 $f(x)$ 的定义区间内的点, 那么

$$
\lim _ {x \to x _ {0}} f (x) = f (x _ {0}).
$$

例如，点 $x_0 = 0$ 是初等函数 $f(x) = \sqrt{1 - x^2}$ 的定义区间 $[-1, 1]$ 上的点，所以 $\lim_{x \to 0} \sqrt{1 - x^2} = \sqrt{1} = 1$；又如点 $x_0 = \frac{\pi}{2}$ 是初等函数 $f(x) = \ln \sin x$ 的一个定义区间 $(0, \pi)$ 内的点，所以

$$
\lim _ {x \to \frac {\pi}{2}} \ln \sin x = \ln \sin \frac {\pi}{2} = 0.
$$

例5 求 $\lim_{x\to 0}\frac{\log_a(1 + x)}{x} (a > 0,a\neq 1)$

解 $\lim_{x\to 0}\frac{\log_a(1 + x)}{x} = \lim_{x\to 0}\log_a(1 + x)^{\frac{1}{x}} = \log_a\mathrm{e} = \frac{1}{\ln a}.$

例6 求 $\lim_{x\to 0}\frac{a^x - 1}{x} (a > 0,a\neq 1)$

解 令 $a^x - 1 = t$，则 $x = \log_a(1 + t)$，当 $x \to 0$ 时 $t \to 0$，于是

$$
\lim _ {x \to 0} \frac {a ^ {x} - 1}{x} = \lim _ {t \to 0} \frac {t}{\log_ {a} (1 + t)} = \ln a.
$$

例7 求 $\lim_{x\to 0}\frac{(1 + x)^{\alpha} - 1}{x} (\alpha \in \mathbb{R})$

解 令 $(1 + x)^{\alpha} - 1 = t$ ，则当 $x\to 0$ 时， $t\to 0$ ，于是

$$
\lim _ {x \to 0} \frac {(1 + x) ^ {\alpha} - 1}{x} = \lim _ {x \to 0} \left[ \frac {(1 + x) ^ {\alpha} - 1}{\ln (1 + x) ^ {\alpha}} \cdot \frac {\alpha \ln (1 + x)}{x} \right] = \lim _ {t \to 0} \frac {t}{\ln (1 + t)} \cdot \lim _ {x \to 0} \frac {\alpha \ln (1 + x)}{x} = \alpha .
$$

由例 5、例 6、例 7 可得下列三个常用的等价无穷小关系式:

$$
\ln (1 + x) \sim x \quad (x \to 0),
$$

$$
\mathrm{e} ^ {x} - 1 \sim x (x \to 0),
$$

$$
(1 + x) ^ {\alpha} - 1 \sim \alpha x (x \rightarrow 0).
$$

例8 求 $\lim_{x\to 0}(1 + 2x)^{\frac{3}{\sin x}}.$

解 因为

$$
(1 + 2 x) ^ {\frac {3}{\sin x}} = (1 + 2 x) ^ {\frac {1}{2 x} \cdot \frac {x}{\sin x} \cdot 6} = \mathrm{e} ^ {6 \cdot \frac {x}{\sin x} \ln (1 + 2 x)} ^ {\frac {1}{2 x}},
$$

利用定理 3 及极限的运算法则,便有

$$
\lim _ {x \to 0} (1 + 2 x) ^ {\frac {3}{\sin x}} = \mathrm{e} ^ {\lim _ {x \to 0} \left[ 6 \cdot \frac {x}{\sin x} \cdot \ln (1 + 2 x) ^ {\frac {1}{2 x}} \right]} = \mathrm{e} ^ {6}.
$$

一般地,对于形如  $u(x)^{v(x)}$  ( $u(x)>0, u(x)\neq1$ ) 的函数(通常称为幂指函数),如果

$$
\lim u (x) = a > 0, \quad \lim v (x) = b,
$$

那么

$$
\lim u (x) ^ {v (x)} = a ^ {b}.
$$

注意 这里三个 lim 都表示在同一自变量变化过程中的极限.

## 习题1-9

1. 求函数 $f(x) = \frac{x^3 + 3x^2 - x - 3}{x^2 + x - 6}$ 的连续区间，并求极限 $\lim_{x \to 0} f(x), \lim_{x \to -3} f(x)$ 及 $\lim_{x \to 2} f(x)$.
2. 设函数 $f(x)$ 与 $g(x)$ 在点 $x_0$ 连续，证明函数

$$
\varphi (x) = \max \{f (x), g (x) \}, \quad \psi (x) = \min \{f (x), g (x) \}
$$

在点 $x_0$ 也连续.

3. 求下列极限:

(1) $\lim_{x\to 0}\sqrt{x^2 - 2x + 5}$;
(2)  $\lim_{\alpha\to\frac{\pi}{4}}(\sin2\alpha)^{3}$ ;
(3)  $\lim_{x\to\frac{\pi}{6}}\ln(2\cos2x)$ ;
(4)  $\lim_{x\to0}\frac{\sqrt{x+1}-1}{x};$
(5)  $\lim_{x\to1}\frac{\sqrt{5x-4}-\sqrt{x}}{x-1};$
(6)  $\lim_{x\to\alpha}\frac{\sin x-\sin\alpha}{x-\alpha};$
(7)  $\lim_{x\to+\infty}\left(\sqrt{x^{2}+x}-\sqrt{x^{2}-x}\right)$ ;
(8)  $\lim_{x\to0}\frac{\left(1-\frac{1}{2}x^{2}\right)^{\frac{2}{3}}-1}{x\ln(1+x)}$ .

4. 求下列极限:

(1) $\lim_{x\to \infty}\mathrm{e}^{\frac{1}{x}};$

(2)  $\lim_{x\to0}\ln\frac{\sin x}{x};$

(3) $\lim_{x\to \infty}\left(1 + \frac{1}{x}\right)^{\frac{x}{2}};$

(4)  $\lim_{x\to0}(1+3\tan^{2}x)^{\cot^{2}x};$

(5)  $\lim_{x\to\infty}\left(\frac{3+x}{6+x}\right)^{\frac{x-1}{2}}$ ;

(6) $\lim_{x\to 0}\frac{\sqrt{1 + \tan x} - \sqrt{1 + \sin x}}{x\sqrt{1 + \sin^2x} - x};$

(7)  $\lim_{x\to e}\frac{\ln x-1}{x-e};$

(8)  $\lim_{x\to0}\frac{e^{3x}-e^{2x}-e^{x}+1}{\sqrt[3]{(1-x)(1+x)}-1};$

(9) $\lim_{x\to \infty}x(\mathrm{e}^{\frac{1}{2x}} - 1)$;

(10) $\lim_{x\to 1}\frac{x^2 - 1}{x - 1}\mathrm{e}^{\frac{1}{x - 1}}.$

5. 设 $f(x)$ 在 $\mathbb{R}$ 上连续, 且 $f(x) \neq 0, \varphi(x)$ 在 $\mathbb{R}$ 上有定义, 且有间断点, 则下列陈述中哪些是对的, 哪些是错的? 如果是对的, 试说明理由; 如果是错的, 试给出一个反例.

(1)  $\varphi[f(x)]$  必有间断点； (2)  $[\varphi(x)]^{2}$  必有间断点；
(3) $f[\varphi(x)]$ 未必有间断点；(4) $\frac{\varphi(x)}{f(x)}$ 必有间断点.

6. 设函数

$$
f (x) = \left\{ \begin{array}{l l} \mathrm{e} ^ {x}, & x <   0, \\ a + x, & x \geqslant 0. \end{array} \right.
$$

应当怎样选择数 $a$ ，才能使得 $f(x)$ 成为在 $(-\infty, +\infty)$ 内的连续函数？

## 第十节 闭区间上连续函数的性质

第八节中已说明了函数在区间上连续的概念,如果函数 $f(x)$ 在开区间 $(a,b)$ 内连续,在右端点b左连续,在左端点a右连续,那么函数 $f(x)$ 就是在闭区间 $[a,b]$ 上连续的.在闭区间上连续的函数有几个重要的性质,下面以定理的形式叙述它们.

## 一、有界性与最大值最小值定理

先说明最大值和最小值的概念.对于在区间 $I$ 上有定义的函数 $f(x)$, 如果有 $x_0 \in I$, 使得对于任一 $x \in I$ 都有

$$
f (x) \leqslant f (x _ {0}) \quad (f (x) \geqslant f (x _ {0})),
$$

那么称 $f(x_0)$ 是函数 $f(x)$ 在区间 $I$ 上的最大值(最小值).

例如, 函数 $f(x) = 1 + \sin x$ 在区间 $[0, 2\pi]$ 上有最大值 2 和最小值 0. 又例如, 函数 $f(x) = \operatorname{sgn} x$ 在区间 $(- \infty, +\infty)$ 内有最大值 1 和最小值 -1. 在开区间 $(0, +\infty)$ 内, $\operatorname{sgn} x$ 的最大值和最小值都等于 1 (注意: 最大值和最小值可以相等!). 但函数 $f(x) = x$ 在开区间 $(a, b)$ 内既无最大值又无最小值. 下面的定理给出函数有界且最大值和最小值存在的充分条件.

定理1（有界性与最大值最小值定理）在闭区间上连续的函数在该区间上有界且一定能取得它的最大值和最小值.

这就是说,如果函数 $f(x)$ 在闭区间 $[a,b]$ 上连续,那么存在常数M>0,使得对任一 $x\in[a,b]$ ,满足 $|f(x)|\leqslant M$ ;且至少有一点 $\xi_{1}$ ,使 $f(\xi_{1})$ 是 $f(x)$ 在 $[a,b]$ 上的最小值;又至少有一点 $\xi_{2}$ ,使 $f(\xi_{2})$ 是 $f(x)$ 在 $[a,b]$ 上的最大值(图1-40).

这里不予证明.

注意 如果函数在开区间内连续,或函数在闭区间上有间断点,那么函数在该区间上不一定有界,也不一定有最大值或最小值.例如,函数  $y = \tan x$  在开区间  $\left(-\frac{\pi}{2}, \frac{\pi}{2}\right)$  内是连续的,但它在开区间  $\left(-\frac{\pi}{2}, \frac{\pi}{2}\right)$  内是无界的,且既无最大值又无最小值;又如,函数

$$
y = f (x) = \left\{ \begin{array}{l l} - x + 1, & 0 \leqslant x <   1, \\ 1, & x = 1, \\ - x + 3, & 1 <   x \leqslant 2 \end{array} \right.
$$

在闭区间 $[0,2]$ 上有间断点 $x = 1$ ，这函数 $f(x)$ 在闭区间 $[0,2]$ 上虽然有界，但是既无最大值又无最小值（图1-41）.

![](images/page_81_chart_4.jpg)

<details>
<summary>contour</summary>

| X | Y |
| --- | --- |
| a | ~0.4 |
| \(\xi1\) | ~0.3 |
| \(\xi2\) | ~0.9 |
| b | ~0.8 |
</details>

图1-40

![](images/page_81_chart_6.jpg)

<details>
<summary>line</summary>

| X | Y (Line 1) | Y (Line 2) |
| --- | --- | --- |
| 0 | 1 | — |
| 1 | 0 | 2 |
| 2 | 1 | 1 |
</details>

图1-41

## 二、零点定理与介值定理

如果 $x_0$ 使 $f(x_0) = 0$，那么 $x_0$ 称为函数 $f(x)$ 的零点.

定理2（零点定理）设函数 $f(x)$ 在闭区间 $[a,b]$ 上连续，且 $f(a)$ 与 $f(b)$ 异号（即 $f(a)\cdot f(b) < 0$），则在开区间 $(a,b)$ 内至少有一点 $\xi$，使

$$
f (\xi) = 0.
$$

这里不予证明.

从几何上看,定理2表示:如果连续曲线弧 $y=f(x)$ 的两个端点位于x轴的不同侧,那么这段曲线弧与x轴至少有一个交点(图1-42).

由定理 2 立即可推得下列较一般性的定理.

定理3（介值定理）设函数 $f(x)$ 在闭区间$[a,b]$ 上连续，且在这区间的端点取不同的函数值

$$
f (  a  ) = A \quad \text {及} \quad f (  b  ) = B  ,
$$

![](images/page_81_chart_17.jpg)

<details>
<summary>line</summary>

| X | Y |
| --- | --- |
| a | ~-1.5 |
| \(\xi\) | 0 |
| b | ~1.5 |
</details>

图1-42

则对于 $A$ 与 $B$ 之间的任意一个数 $C$ ，在开区间 $(a,b)$ 内至少有一点 $\xi$ ，使得

$$
f (\xi) = C \quad (a <   \xi <   b).
$$

证 设 $\varphi(x) = f(x) - C$，则 $\varphi(x)$ 在闭区间 $[a, b]$ 上连续，且 $\varphi(a) = A - C$ 与 $\varphi(b) = B - C$ 异号。根据零点定理，开区间 $(a, b)$ 内至少有一点 $\xi$ 使得

$$
\varphi (\xi) = 0 \quad (a <   \xi <   b).
$$

又 $\varphi (\xi) = f(\xi) - C$ ，因此由上式即得

$$
f (\xi) = C \quad (a <   \xi <   b).
$$

这个定理的几何意义是: 连续曲线弧  $y=f(x)$  与水平直线 y=C 至少相交于一点(图 1-43).

推论 在闭区间 $[a, b]$ 上连续的函数 $f(x)$ 的值域为闭区间 $[m, M]$, 其中 $m$ 与 $M$ 依次为 $f(x)$ 在 $[a, b]$ 上的最小值与最大值.

设 $m = f(x_{1}), M = f(x_{2})$，而 $m \neq M$，在闭区间 $[x_{1}, x_{2}]$（或 $[x_{2}, x_{1}]$）上应用介值定理，知 $f(x)$ 可取区间 $(m, M)$ 内的一切值，结合 $f(x_{1}) = m$，$f(x_{2}) = M$，便得上述推论.

![](images/page_82_chart_9.jpg)

<details>
<summary>line</summary>

| Point | x-coordinate | y-coordinate |
| --- | --- | --- |
| P1 | \(\xi1\) | C |
| P2 | \(\xi2\) | C |
| P3 | \(\xi3\) | C |
</details>

图1-43

例 1 证明方程  $x^{3}-4x^{2}+1=0$  在区间  $(0,1)$  内至少有一个根.

证 函数 $f(x) = x^{3} - 4x^{2} + 1$ 在闭区间[0,1]上连续，又

$$
f (0) = 1 > 0, \quad f (1) = - 2 <   0.
$$

根据零点定理,在 $(0,1)$ 内至少有一点 $\xi$ ,使得

$$
f (\xi) = 0,
$$

即

$$
\xi^ {3} - 4 \xi^ {2} + 1 = 0 \quad (0 <   \xi <   1).
$$

这等式说明方程 $x^{3} - 4x^{2} + 1 = 0$ 在区间(0,1)内至少有一个根是 $\xi$.

## \* 三、一致连续性

我们先介绍函数的一致连续性概念.

设函数在区间 $I$ 上连续，$x_0$ 是在 $I$ 上任意取定的一个点。由于 $f(x)$ 在点 $x_0$ 连续，因此 $\forall \varepsilon > 0, \exists \delta > 0$，使得当 $|x - x_0| < \delta$ 时，就有 $|f(x) - f(x_0)| < \varepsilon$。通常这个 $\delta$ 不仅与 $\varepsilon$ 有关，而且与所取定的 $x_0$ 有关，即使 $\varepsilon$ 不变，但选取区间 $I$ 上的其他点作为 $x_0$ 时，这个 $\delta$ 就不一定适用了。可是对于某些函数，却有这样一种重要情形:存在着只与 $\varepsilon$ 有关，而对区间 $I$ 上任何点 $x_0$ 都能适用的正数 $\delta$，即对任何 $x_0 \in I$，只要 $|x - x_0| < \delta$ 时，就有 $|f(x) - f(x_0)| < \varepsilon$。如果函数 $f(x)$ 在区间 $I$ 上能使这种情形发生，就说函数 $f(x)$ 在区间 $I$ 上是一致连续的。

定义 设函数 $f(x)$ 在区间 $I$ 上有定义. 如果对于任意给定的正数 $\varepsilon$, 总存在正数 $\delta$, 使得对于区间 $I$ 上的任意两点 $x_{1}, x_{2}$, 当 $|x_{1} - x_{2}| < \delta$ 时, 有

$$
\left| f (x _ {1}) - f (x _ {2}) \right| <   \varepsilon ,
$$

那么称函数 $f(x)$ 在区间I上一致连续.

一致连续性表示,不论在区间 I 的任何部分,只要自变量的两个数值接近到一定程度,就可使对应的函数值达到所指定的接近程度.

由上述定义可知,如果函数 $f(x)$ 在区间I上一致连续,那么 $f(x)$ 在区间I上也是连续的.但反过来不一定成立,举例说明如下:

例 2 函数  $f(x)=\frac{1}{x}$  在区间  $(0,1]$  上是连续的,但不是一致连续的.

因为函数 $f(x)=\frac{1}{x}$ 是初等函数,它在区间(0,1]上有定义,所以在(0,1]上是连续的.

$\forall \varepsilon > 0 (0 < \varepsilon < 1)$, 假定 $f(x) = \frac{1}{x}$ 在 $(0,1]$ 上一致连续, 应该 $\exists \delta > 0$, 使得对于 $(0,1]$ 上的任意两个值 $x_1, x_2$, 当 $|x_1 - x_2| < \delta$ 时, 就有 $|f(x_1) - f(x_2)| < \varepsilon$.

现在取原点附近的两点

$$
x _ {1} = \frac {1}{n}, \quad x _ {2} = \frac {1}{n + 1},
$$

其中 $n$ 为正整数，这样的 $x_{1}, x_{2}$ 显然在 $(0,1]$ 上. 因

$$
\left| x _ {1} - x _ {2} \right| = \left| \frac {1}{n} - \frac {1}{n + 1} \right| = \frac {1}{n (n + 1)},
$$

故只要 $n$ 取得足够大，总能使 $\left|x_1 - x_2\right| < \delta.$ 但这时有

$$
\left| f (x _ {1}) - f (x _ {2}) \right| = \left| \frac {1}{\frac {1}{n}} - \frac {1}{\frac {1}{n + 1}} \right| = | n - (n + 1) | = 1 > \varepsilon ,
$$

不符合一致连续的定义,所以  $f(x)=\frac{1}{x}$  在  $(0,1]$  上不是一致连续的.

上例说明,在半开区间上连续的函数不一定在该区间上一致连续.但是,有下面的定理:

定理 4(一致连续性定理) 如果函数  $f(x)$  在闭区间  $[a, b]$  上连续, 那么它在该区间上一致连续.

这里不予证明.

## 习题1-10

1. 假设函数 $f(x)$ 在闭区间 $[0,1]$ 上连续，并且对 $[0,1]$ 上任一点 $x$ 有 $0 \leqslant f(x) \leqslant 1$. 试证明 $[0,1]$

中必存在一点 $c$ ，使得 $f(c) = c$ （$c$ 称为函数 $f(x)$ 的不动点）.

2. 证明方程 $x^{5} - 3x = 1$ 至少有一个根介于1和2之间.

3. 证明方程 $x = a\sin x + b$，其中 $a > 0, b > 0$，至少有一个正根，并且它不超过 $a + b$.

4. 证明任一最高次幂的指数为奇数的代数方程

$$
a _ {0} x ^ {2 n + 1} + a _ {1} x ^ {2 n} + \dots + a _ {2 n} x + a _ {2 n + 1} = 0
$$

至少有一个实根,其中  $a_{0}, a_{1}, \cdots, a_{2n+1}$  均为常数,  $n \in N$ .

5. 证明: 方程 $x^{3} + 2x^{2} - 4x - 1 = 0$ 有三个实根.

6. 若  $f(x)$  在  $[a, b]$  上连续， $a < x_{1} < x_{2} < \cdots < x_{n} < b \quad (n \geqslant 3)$ ，证明:在  $(x_{1}, x_{n})$  内至少有一点  $\xi$ ，使  $f(\xi) = \frac{f(x_{1}) + f(x_{2}) + \cdots + f(x_{n})}{n}$ .

\*7. 设函数 $f(x)$ 对于闭区间 $[a, b]$ 上的任意两点 $x, y$，恒有 $|f(x) - f(y)| \leqslant L|x - y|$，其中 $L$ 为正常数，且 $f(a) \cdot f(b) < 0$. 证明:至少有一点 $\xi \in (a, b)$，使得 $f(\xi) = 0$.

\*8. 证明: 若 $f(x)$ 在 $(- \infty, +\infty)$ 内连续, 且 $\lim_{x \to -\infty} f(x)$ 存在, 则 $f(x)$ 必在 $(- \infty, +\infty)$ 内有界.

\*9. 在什么条件下，$(a, b)$ 内的连续函数 $f(x)$ 为一致连续？

## 总习题一

1. 在“充分”“必要”和“充分必要”三者中选择一个正确的填入下列空格内:

(1) 数列  $\{x_{n}\}$  有界是数列  $\{x_{n}\}$  收敛的 \_\_\_\_ 条件, 数列  $\{x_{n}\}$  收敛是数列  $\{x_{n}\}$  有界的 \_\_\_\_ 条件;

(2) $f(x)$ 在 $x_0$ 的某一去心邻域内有界是 $\lim_{x \to x_0} f(x)$ 存在的 \_\_\_\_ 条件, $\lim_{x \to x_0} f(x)$ 存在是 $f(x)$ 在 $x_0$ 的某一去心邻域内有界的 \_\_\_\_ 条件;

(3) $f(x)$ 在 $x_0$ 的某一去心邻域内无界是 $\lim_{x \to x_0} f(x) = \infty$ 的 \_\_\_\_ 条件, $\lim_{x \to x_0} f(x) = \infty$ 是 $f(x)$ 在 $x_0$ 的某一去心邻域内无界的 \_\_\_\_ 条件;

(4) $f(x)$ 当 $x \to x_0$ 时的右极限 $f(x_0^+)$ 及左极限 $f(x_0^-)$ 都存在且相等是 $\lim_{x \to x_0} f(x)$ 存在的 \_\_\_\_ 条件.

2. 已知函数

$$
f (x) = \left\{ \begin{array}{l l} (\cos x) ^ {- x ^ {2}}, & 0 <   | x | <   \frac {\pi}{2}, \\ a, & x = 0 \end{array} \right.
$$

在 x=0 连续, 则 a= \_\_\_\_.

3. 以下两题中给出了四个结论,从中选出一个正确的结论:

(1) 设  $f(x)=2^{x}+3^{x}-2$ ，则当  $x\to0$  时，有().

(A) $f(x)$ 与 $x$ 是等价无穷小

(B) $f(x)$ 与 $x$ 同阶但非等价无穷小

(C) $f(x)$ 是比 $x$ 高阶的无穷小

(D) $f(x)$ 是比 $x$ 低阶的无穷小

(2) 设  $f(x)=\frac{\mathrm{e}^{\frac{1}{x}}-1}{\mathrm{e}^{\frac{1}{x}}+1}$ ，则 x=0 是  $f(x)$  的().

(A) 可去间断点

(B) 跳跃间断点

(C) 第二类间断点

(D) 连续点

4. 设 $f(x)$ 的定义域是 $[0,1]$，求下列函数的定义域:

(1)  $f(e^{x})$ ;

(2) $f(\ln x)$;

(3) $f(\arctan x)$;

(4) $f(\cos x)$.

5. 设

$$
f (x) = \left\{ \begin{array}{l l} 0, & x \leqslant 0, \\ x, & x > 0, \end{array} \right. \quad g (x) = \left\{ \begin{array}{l l} 0, & x \leqslant 0, \\ - x ^ {2}, & x > 0, \end{array} \right.
$$

求 $f[f(x)]$ ,  $g[g(x)]$ ,  $f[g(x)]$ ,  $g[f(x)]$ .

6. 利用  $y = \sin x$  的图形作出下列函数的图形:

(1)  $y = |\sin x|$ ;

(2)  $y=\sin |x|$ ;

(3) $y = 2\sin \frac{x}{2}$.

7. 把半径为 R 的一圆形铁皮, 自圆心处剪去圆心角为  $\alpha$  的一扇形后围成一无底圆锥. 试建立该圆锥的体积 V 与角  $\alpha$  间的函数关系.

\* 8. 根据函数极限的定义证明 $\lim_{x\to3}\frac{x^{2}-x-6}{x-3}=5$.

9. 求下列极限:

(1)  $\lim_{x\to1}\frac{x^{2}-x+1}{(x-1)^{2}};$

(2) $\lim_{x\to +\infty}x(\sqrt{x^2 + 1} -x)$;

(3)  $\lim_{x\to\infty}\left(\frac{2x+3}{2x+1}\right)^{x+1}$ ;

(4)  $\lim_{x\to0}\frac{\tan x-\sin x}{x^{3}};$

(5) $\lim_{x\to 0}\left(\frac{a^x + b^x + c^x}{3}\right)^{\frac{1}{x}}$ ($a > 0, a \neq 1; b > 0, b \neq 1; c > 0, c \neq 1$);

(6)  $\lim_{x\to\frac{\pi}{2}}(\sin x)^{\tan x}$ ;

(7)  $\lim_{x\to a}\frac{\ln x-\ln a}{x-a}$  (a>0);

(8)  $\lim_{x\to0}\frac{x\tan x}{\sqrt{1-x^{2}}-1}.$

10. 设

$$
f (x) = \left\{ \begin{array}{l l} x \sin \frac {1}{x}, & x > 0, \\ a + x ^ {2} & x \leqslant 0, \end{array} \right.
$$

要使 $f(x)$ 在 $(-∞,+∞)$ 内连续,应当怎样选择数a?

11. 设

$$
f (x) = \lim _ {n \to \infty} \frac {1 + x}{1 + x ^ {2 n}},
$$

求 $f(x)$ 的间断点,并说明间断点所属类型.

12. 证明

$$
\lim _ {n \to \infty} \left(\frac {1}{\sqrt {n ^ {2} + 1}} + \frac {1}{\sqrt {n ^ {2} + 2}} + \dots + \frac {1}{\sqrt {n ^ {2} + n}}\right) = 1.
$$

13. 证明方程 $\sin x + x + 1 = 0$ 在开区间 $\left(-\frac{\pi}{2}, \frac{\pi}{2}\right)$ 内至少有一个根.

14. 如果存在直线 $L: y = kx + b$，使得当 $x \to \infty$（或 $x \to +\infty, x \to -\infty$）时，曲线 $y = f(x)$ 上的动点 $M(x, y)$ 到直线 $L$ 的距离 $d(M, L) \to 0$，那么称 $L$ 为曲线 $y = f(x)$ 的渐近线。当直线 $L$ 的斜率 $k \neq 0$ 时，称 $L$ 为斜渐近线。

（1）证明:直线 $L: y = kx + b$ 为曲线 $y = f(x)$ 的渐近线的充分必要条件是

$$
k = \lim_{\substack{x\to \infty \\ \left( \begin{array}{c}x\to +\infty \\ x\to -\infty \end{array} \right)}}\frac{f(x)}{x}, \quad b = \lim_{\substack{x\to \infty \\ \left( \begin{array}{c}x\to +\infty \\ x\to -\infty \end{array} \right)}}[f(x) - kx];
$$

(2) 求曲线  $y=(2x-1)\mathrm{e}^{\frac{1}{x}}$  的斜渐近线；
(3) 求曲线  $y = x \ln \left( e + \frac{1}{x} \right)$  的渐近线.

![](images/page_86_image_7.jpg)

第一章释疑解难

![](images/page_86_image_9.jpg)

第一章例题精讲

## 第二章

## 导数与微分

微分学是微积分的重要组成部分,它的基本概念是导数与微分.

本章中,我们主要讨论导数和微分的概念以及它们的计算方法.至于导数的应用,将在第三章讨论.

## 第一节 导数概念

## 一、引例

为了说明微分学的基本概念——导数,我们先讨论两个问题:速度问题和切线问题.这两个问题在历史上都与导数概念的形成有密切的关系.

## 1. 直线运动的速度

设某质点沿直线运动.在直线上规定了原点、正方向和单位长度,使直线成为数轴.此外,再取定一个时刻作为测量时间的零点.设质点于时刻 t 在直线上的位置的坐标为 s (简称位置 s).这样,该质点的运动完全由某个函数

$$
s = f (t)
$$

所确定. 此函数对运动过程中所出现的 t 值有定义, 称为位置函数. 在最简单的情形, 该质点所经过的路程与所花的时间成正比. 就是说, 无论取哪一段时间间隔, 比值

$$
\frac {\text {经过的路程}}{\text {所花的时间}} \tag {1-1}
$$

总是相同的.这个比值就称为该质点的速度,并说该质点做匀速运动.如果运动不是匀速的,那么在运动的不同时间间隔内,比值(1-1)会有不同的值.这样,把比值(1-1)笼统地称为该质点的速度就不合适了,而需要按不同时刻来考虑.那么,这种非匀速运动的质点在某一时刻(设为 $t_0$ )的速度应如何理解而又如何求得呢？

首先取从时刻 $t_0$ 到 $t$ 这样一个时间间隔，在这段时间内，质点从位置 $s_0 = f(t_0)$ 移动到 $s = f(t)$. 这时由(1-1)式算得的比值

$$
\frac {s - s _ {0}}{t - t _ {0}} = \frac {f (t) - f \left(t _ {0}\right)}{t - t _ {0}} \tag {1-2}
$$

可认为是质点在上述时间间隔内的平均速度.如果时间间隔选得较短,这个比值(1-2)在实践中也可用来说明质点在时刻 $t_{0}$ 的速度.但对于质点在时刻 $t_{0}$ 的速度的精确概念来说,这样做是不够的,而更确切地应当这样:令 $t\rightarrow t_{0}$ ,取(1-2)式的极限,如果这个极限存在,设为v,即

$$
v = \lim _ {t \to t _ {0}} \frac {f (t) - f (t _ {0})}{t - t _ {0}},
$$

这时就把这个极限值 v 称为质点在时刻  $t_{0}$  的(瞬时)速度.

## 2. 切线问题

圆的切线可定义为“与曲线只有一个交点的直线”.但是对于其他曲线,用“与曲线只有一个交点的直线”作为切线的定义就不一定合适.例如,对于抛物线 $y=x^{2}$ ,在原点O处两个坐标轴都符合上述定义,但实际上只有x轴是该抛物线在点O处的切线.下面给出切线的定义.

设有曲线 C 及 C 上的一点 M(图 2-1)，在点 M 外另取 C 上一点 N，作割线 MN。当点 N 沿曲线 C 趋于点 M 时，如果割线 MN 绕点 M 旋转而趋于极限位置 MT，直线 MT 就称为曲线 C 在点 M 处的切线。这里极限位置的含义是:只要弦长  $\left|MN\right|$  趋于零， $\angle NMT$  也趋于零。

现在就曲线 $C$ 为函数 $y = f(x)$ 的图形的情形来讨论切线问题. 设 $M(x_0, y_0)$ 是曲线 $C$ 上的一个点（图2-2），则 $y_0 = f(x_0)$. 根据上述定义要定出曲线 $C$ 在点 $M$ 处的切线，只要定出切线的斜率就行了. 为此，在点 $M$ 外另取 $C$ 上的一点 $N(x, y)$，于是割线 $MN$ 的斜率为

![](images/page_88_image_11.jpg)

<details>
<summary>text_image</summary>

C
N
M
T
</details>

图2-1

![](images/page_88_image_13.jpg)

<details>
<summary>text_image</summary>

y
y=f(x)
N
C
M
T
α
φ
O
x₀
x
x
</details>

图2-2

$$
\tan \varphi = \frac {y - y _ {0}}{x - x _ {0}} = \frac {f (x) - f (x _ {0})}{x - x _ {0}},
$$

其中 $\varphi$ 为割线 $MN$ 的倾角. 当点 $N$ 沿曲线 $C$ 趋于点 $M$ 时, $x \to x_0$. 如果当 $x \to x_0$ 时, 上式的极限存在, 设为 $k$, 即

$$
k = \lim _ {x \to x _ {0}} \frac {f (x) - f (x _ {0})}{x - x _ {0}}
$$

存在,那么此极限 k 是割线斜率的极限,也就是切线的斜率.这里  $k=\tan\alpha$ ,其中  $\alpha$  是切线 MT 的倾角.于是,通过点  $M(x_{0},f(x_{0}))$  且以 k 为斜率的直线 MT 便是曲线 C 在点 M 处的切线.事实上,由  $\angle NMT=\varphi-\alpha$  以及  $x\to x_{0}$  时  $\varphi\to\alpha$ ,可见  $x\to x_{0}$  时(这时  $|MN|\to0$ ),  $\angle NMT\to0$ .因此直线 MT 确为曲线 C 在点 M 处的切线.

## 二、导数的定义

## 1. 函数在一点处的导数与导函数

从上面所讨论的两个问题看出,非匀速直线运动的速度和切线的斜率都归结为如下的极限:

$$
\lim _ {x \to x _ {0}} \frac {f (x) - f (x _ {0})}{x - x _ {0}}, \tag {1-3}
$$

这里 $x - x_0$ 和 $f(x) - f(x_0)$ 分别是函数 $y = f(x)$ 的自变量的增量 $\Delta x$ 和函数的增量 $\Delta y$:

$$
\Delta x = x - x _ {0}, \quad \Delta y = f (x) - f (x _ {0}) = f (x _ {0} + \Delta x) - f (x _ {0}).
$$

因 $x \to x_0$ 相当于 $\Delta x \to 0$, 故(1-3)式也可写成

$$
\lim _ {\Delta x \to 0} \frac {\Delta y}{\Delta x} \quad \text {或} \quad \lim _ {\Delta x \to 0} \frac {f (x _ {0} + \Delta x) - f (x _ {0})}{\Delta x}.
$$

在自然科学和工程技术领域内,还有许多概念,例如电流强度、角速度、线密度等,都可归结为形如(1-3)式的数学形式.我们撇开这些量的具体意义,抓住它们在数量关系上的共性,就得出函数的导数概念.

定义 设函数 $y = f(x)$ 在点 $x_0$ 的某个邻域内有定义, 当自变量 $x$ 在 $x_0$ 处取得增量 $\Delta x$ (点 $x_0 + \Delta x$ 仍在该邻域内) 时, 相应地, 因变量取得增量 $\Delta y = f(x_0 + \Delta x) - f(x_0)$; 如果 $\Delta y$ 与 $\Delta x$ 之比当 $\Delta x \to 0$ 时的极限存在, 那么称函数 $y = f(x)$ 在点 $x_0$ 处可导, 并称这个极限为函数 $y = f(x)$ 在点 $x_0$ 处的导数, 记为 $f'(x_0)$, 即

$$
f ^ {\prime} (x _ {0}) = \lim _ {\Delta x \to 0} \frac {\Delta y}{\Delta x} = \lim _ {\Delta x \to 0} \frac {f (x _ {0} + \Delta x) - f (x _ {0})}{\Delta x}, \tag {1-4}
$$

也可记作 $y^{\prime}\mid_{x = x_0},\frac{\mathrm{d}y}{\mathrm{d}x}\bigg|_{x = x_0}$ 或 $\frac{\mathrm{d}f(x)}{\mathrm{d}x}\bigg|_{x = x_0}$

函数 $f(x)$ 在点 $x_0$ 处可导有时也说成 $f(x)$ 在点 $x_0$ 处具有导数或导数存在.

导数的定义式(1-4)也可取不同的形式, 常见的有

$$
f ^ {\prime} (x _ {0}) = \lim _ {h \to 0} \frac {f (x _ {0} + h) - f (x _ {0})}{h} \tag {1-5}
$$

和

$$
f ^ {\prime} (x _ {0}) = \lim _ {x \to x _ {0}} \frac {f (x) - f (x _ {0})}{x - x _ {0}}. \tag {1-6}
$$

(1-5)式中的 h 即自变量的增量  $\Delta x$ .

在实际中,需要讨论各种具有不同意义的变量的变化“快慢”问题,在数学上就是所谓函数的变化率问题.导数概念就是函数变化率这一概念的精确描述.它撇开了自变量和因变量所代表的几何或物理等方面的特殊意义,纯粹从数量方面来刻画变化率的本质:因变量增量与自变量增量之比 $\frac{\Delta y}{\Delta x}$ 是因变量y在以 $x_{0}$ 和 $x_{0}+\Delta x$ 为端点的区间上的平均变化率,而导数 $f'(x_{0})$ 则是因变量y在点 $x_{0}$ 处的变化率,它反映了因变量随自变量的变化而变化的快慢程度.

如果极限(1-4)不存在,就说函数  $y=f(x)$  在点  $x_{0}$  处不可导.如果不可导的原因是由于  $\Delta x\to0$  时,比式  $\frac{\Delta y}{\Delta x}\to\infty$ ,为了方便起见,也往往说函数  $y=f(x)$  在点  $x_{0}$  处的导数为无穷大.

上面讲的是函数在一点处可导.如果函数 $y = f(x)$ 在开区间 $I$ 内的每点处都可导,那么就称函数 $f(x)$ 在开区间 $I$ 内可导.这时,对于任一 $x \in I$,都对应着 $f(x)$ 的一个确定的导数值.这样就构成了一个新的函数,这个函数叫做原来函数 $y = f(x)$ 的导函数,记作 $y', f'(x), \frac{\mathrm{d}y}{\mathrm{d}x}$ 或 $\frac{\mathrm{d}f(x)}{\mathrm{d}x}$.

在(1-4)式或(1-5)式中把 $x_0$ 换成 $x$ ，即得导函数的定义式

$$
y ^ {\prime} = \lim _ {\Delta x \to 0} \frac {f (x + \Delta x) - f (x)}{\Delta x}
$$

或

$$
f ^ {\prime} (x) = \lim _ {h \to 0} \frac {f (x + h) - f (x)}{h}.
$$

注意 在以上两式中, 虽然 $x$ 可以取区间 $I$ 内的任何数值, 但在极限过程中, $x$ 是常量, $\Delta x$ 或 $h$ 是变量.

显然,函数 $f(x)$ 在点 $x_{0}$ 处的导数 $f'(x_{0})$ 就是导函数 $f'(x)$ 在点 $x=x_{0}$ 处的函数值,即

$$
f ^ {\prime} (x _ {0}) = f ^ {\prime} (x) \mid_ {x = x _ {0}}.
$$

导函数 $f'(x)$ 简称导数,而 $f'(x_0)$ 是 $f(x)$ 在 $x_0$ 处的导数或导数 $f'(x)$ 在点 $x_0$ 处的值.

## 2. 求导数举例

下面根据导数定义求一些简单函数的导数.

例 1 求函数  $f(x)=C$  (C 为常数) 的导数.

解 $f^{\prime}(x) = \lim_{h\to 0}\frac{f(x + h) - f(x)}{h} = \lim_{h\to 0}\frac{C - C}{h} = 0$ ，即

$$
(C) ^ {\prime} = 0.
$$

这就是说,常数的导数等于零.

例 2 求函数  $f(x)=x^{n}\quad(n\in\mathbb{N}_{+})$  的导数.

解 当 $n = 1$ 时, $f'(x) = \lim_{h\to 0}\frac{f(x + h) - f(x)}{h} = \lim_{h\to 0}\frac{(x + h) - x}{h} = 1;$

当 $n > 1$ 时，

$$
\begin{array}{l} f ^ {\prime} (x) = \lim _ {h \to 0} \frac {f (x + h) - f (x)}{h} = \lim _ {h \to 0} \frac {(x + h) ^ {n} - x ^ {n}}{h} \\ = \lim _ {h \to 0} \left[ n x ^ {n - 1} + \frac {n (n - 1)}{2} x ^ {n - 2} h + \dots + h ^ {n - 1} \right] = n x ^ {n - 1}. \\ \end{array}
$$

即

$$
(x ^ {n}) ^ {\prime} = \left\{ \begin{array}{l l} 1, & n = 1, \\ n x ^ {n - 1}, & n > 1. \end{array} \right.
$$

例 3 求幂函数  $f(x)=x^{\mu}\left(\mu\in\mathbb{R}\right)$  的导数.

解 幂函数的定义域与常数 $\mu$ 有关, 以下设 $x$ 在幂函数 $x^{\mu}$ 的定义域内且 $x \neq 0$, 则

$$
\frac {f (x + h) - f (x)}{h} = \frac {(x + h) ^ {\mu} - x ^ {\mu}}{h} = x ^ {\mu - 1} \cdot \frac {\left(1 + \frac {h}{x}\right) ^ {\mu} - 1}{\frac {h}{x}}.
$$

利用第一章第九节例 7 的结果,便得

$$
f ^ {\prime} (x) = \lim _ {h \to 0} \frac {f (x + h) - f (x)}{h} = \mu x ^ {\mu - 1},
$$

即

$$
(x ^ {\mu}) ^ {\prime} = \mu x ^ {\mu - 1}.
$$

这就是幂函数的导数公式①.

利用这公式,可以很方便地求出幂函数的导数,例如:

当 $\mu = \frac{1}{2}$ 时，$y = x^{\frac{1}{2}} = \sqrt{x} (x > 0)$ 的导数为

$$
(x ^ {\frac {1}{2}}) ^ {\prime} = \frac {1}{2} x ^ {\frac {1}{2} - 1} = \frac {1}{2} x ^ {- \frac {1}{2}},
$$

即

$$
(\sqrt {x}) ^ {\prime} = \frac {1}{2 \sqrt {x}};
$$

当 $\mu = -1$ 时，$y = x^{-1} = \frac{1}{x} (x\neq 0)$ 的导数为

$$
(x ^ {- 1}) ^ {\prime} = (- 1) x ^ {- 1 - 1} = - x ^ {- 2},
$$

即

$$
\left(\frac {1}{x}\right) ^ {\prime} = - \frac {1}{x ^ {2}}.
$$

例 4 求函数  $f(x)=\sin x$  的导数.

解 $f^{\prime}(x) = \lim_{h\to 0}\frac{f(x + h) - f(x)}{h} = \lim_{h\to 0}\frac{\sin(x + h) - \sin x}{h}$

$$
= \lim _ {h \to 0} \frac {1}{h} \cdot 2 \cos \left(x + \frac {h}{2}\right) \sin \frac {h}{2} = \lim _ {h \to 0} \cos \left(x + \frac {h}{2}\right) \cdot \frac {\sin \frac {h}{2}}{\frac {h}{2}} = \cos x,
$$

即

$$
(\sin x) ^ {\prime} = \cos x.
$$

这就是说,正弦函数的导数是余弦函数.

用类似的方法,可求得

$$
(\cos x) ^ {\prime} = - \sin x,
$$

就是说,余弦函数的导数是负的正弦函数.

例 5 求函数  $f(x)=a^{x}\quad(a>0,a\neq1)$  的导数.

解 $f^{\prime}(x) = \lim_{h\to 0}\frac{f(x + h) - f(x)}{h} = \lim_{h\to 0}\frac{a^{x + h} - a^x}{h} = a^x\lim_{h\to 0}\frac{a^h - 1}{h}.$

利用第一章第九节例6的结果得

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 对 $x = 0$ 时，若 $\mu > 1$ ，则用导数定义直接计算得 $f'(0) = 0$ ，而此时公式右端当 $x = 0$ 时也为零，故公式对一切 $x$ 适用；若 $\mu = 1$ ，则对一切 $x$ 有 $f'(x) = 1$ ，而此时公式右端当 $x \neq 0$ 时也为1，当 $x = 0$ 时，其值特别约定为1，这样，公式对一切 $x$ 也适用.</span></small>

$$
f ^ {\prime} (x) = a ^ {x} \ln a,
$$

即

$$
(a ^ {x}) ^ {\prime} = a ^ {x} \ln a.
$$

这就是指数函数的导数公式.特别地,当 a=e 时,因  $\ln e=1$ ,故有

$$
(e ^ {x}) ^ {\prime} = e ^ {x}.
$$

上式表明,以 e 为底的指数函数的导数就是它自己,这是以 e 为底的指数函数的一个重要特性.

例 6 求函数  $f(x)=\log_{a}x$  ( $a>0, a\neq1$ ) 的导数.

解 $f^{\prime}(x) = \lim_{h\to 0}\frac{f(x + h) - f(x)}{h} = \lim_{h\to 0}\frac{\log_a(x + h) - \log Mel}{h}$

$$
= \lim _ {h \to 0} \frac {1}{h} \log_ {a} \frac {x + h}{x} = \lim _ {h \to 0} \frac {1}{x} \cdot \frac {x}{h} \log_ {a} \left(1 + \frac {h}{x}\right) = \frac {1}{x} \lim _ {h \to 0} \frac {\log_ {a} \left(1 + \frac {h}{x}\right)}{\frac {h}{x}}.
$$

作代换  $u=\frac{h}{x}$  并利用第一章第九节例 5 的结果得

$$
f ^ {\prime} (x) = \frac {1}{x \ln a},
$$

即

$$
(\log_ {a} x) ^ {\prime} = \frac {1}{x \ln a}.
$$

这就是对数函数的导数公式.特别地,当 a=e 时,由上式得自然对数函数的导数公式

$$
(\ln x) ^ {\prime} = \frac {1}{x}.
$$

例 7 求函数  $f(x)=|x|$  在 x=0 处的导数.

解 $\lim_{h\to 0}\frac{f(0 + h) - f(0)}{h} = \lim_{h\to 0}\frac{|h| - 0}{h} = \lim_{h\to 0}\frac{|h|}{h}.$

当 $h < 0$ 时，$\frac{|h|}{h} = -1$，故 $\lim_{h \to 0^-} \frac{|h|}{h} = -1$；

当 $h > 0$ 时， $\frac{|h|}{h} = 1$ ，故 $\lim_{h\to 0^{+}}\frac{|h|}{h} = 1.$

所以， $\lim_{h\to0}\frac{f(0+h)-f(0)}{h}$  不存在，即函数  $f(x)=|x|$  在 x=0 处不可导.

## 3. 单侧导数

根据函数 $f(x)$ 在点 $x_0$ 处的导数 $f'(x_0)$ 的定义，导数

$$
f ^ {\prime} (x _ {0}) = \lim _ {h \to 0} \frac {f (x _ {0} + h) - f (x _ {0})}{h}
$$

是一个极限,而极限存在的充分必要条件是左、右极限都存在且相等,因此  $f'(x_{0})$  存在即  $f(x)$  在点  $x_{0}$  处可导的充分必要条件是左、右极限

$$
\lim _ {h \to 0 ^ {-}} {\frac {f (x _ {0} + h) - f (x _ {0})}{h}} \quad {\text {及}} \quad \lim _ {h \to 0 ^ {+}} {\frac {f (x _ {0} + h) - f (x _ {0})}{h}}
$$

都存在且相等. 这两个极限分别称为函数 $f(x)$ 在点 $x_0$ 处的左导数和右导数, 记作 $f_{-}^{\prime}(x_0)$ 及 $f_{+}^{\prime}(x_0)$, 即

$$
f _ {-} ^ {\prime} (x _ {0}) = \lim _ {h \to 0 ^ {-}} \frac {f (x _ {0} + h) - f (x _ {0})}{h},
$$

$$
f _ {+} ^ {\prime} (x _ {0}) = \lim _ {h \to 0 ^ {+}} \frac {f (x _ {0} + h) - f (x _ {0})}{h}.
$$

现在可以说,函数 $f(x)$ 在点 $x_0$ 处可导的充分必要条件是左导数 $f_{-}^{\prime}(x_{0})$ 和右导数 $f_{+}^{\prime}(x_{0})$ 都存在且相等.

函数 $f(x)=|x|$ 在x=0处的左导数 $f_{-}^{\prime}(0)=-1$ 及右导数 $f_{+}^{\prime}(0)=1$ 虽然都存在，但不相等，故 $f(x)=|x|$ 在x=0处不可导.

左导数和右导数统称为单侧导数.

如果函数 $f(x)$ 在开区间 $(a,b)$ 内可导，且 $f_{+}^{\prime}(a)$ 及 $f_{-}^{\prime}(b)$ 都存在，那么就说 $f(x)$ 在闭区间 $[a,b]$ 上可导.

## 三、导数的几何意义

由第一目中切线问题的讨论以及第二目中导数的定义可知: 函数  $y=f(x)$  在点  $x_{0}$  处的导数  $f'(x_{0})$  在几何上表示曲线  $y=f(x)$  在点  $M(x_{0},f(x_{0}))$  处的切线的斜率, 即

$$
f ^ {\prime} (x _ {0}) = \tan \alpha ,
$$

其中  $\alpha$  是切线的倾角(图 2-3).

如果  $y=f(x)$  在点  $x_{0}$  处的导数为无穷大, 那么这时曲线  $y=f(x)$  的割线以垂直于 x 轴的直线  $x=x_{0}$  为极限位置, 即曲线  $y=f(x)$  在点  $M(x_{0},f(x_{0}))$  处具有垂直于 x 轴的切线  $x=x_{0}$  (参看后面例 10).

根据导数的几何意义并应用直线的点斜式方程，可知曲线 $y = f(x)$ 在点 $M(x_0, y_0)$ 处的切线方程为

$$
y - y _ {0} = f ^ {\prime} (x _ {0}) (x - x _ {0}),
$$

![](images/page_94_image_18.jpg)

<details>
<summary>text_image</summary>

y
y=f(x)
T
M
α
O
x₀
x
</details>

图2-3

过切点 $M(x_0, y_0)$ 且与切线垂直的直线叫做曲线 $y = f(x)$ 在点 $M$ 处的法线. 如果 $f'(x_0) \neq 0$, 法线的斜率为 $-\frac{1}{f'(x_0)}$, 从而法线方程为

$$
y - y _ {0} = - \frac {1}{f ^ {\prime} (x _ {0})} (x - x _ {0}).
$$

例8 求等边双曲线 $y = \frac{1}{x}$ 在点 $\left(\frac{1}{2}, 2\right)$ 处的切线的斜率，并写出在该点处的切线方程和法线方程.

解 根据导数的几何意义知道,所求切线的斜率为

$$
k _ {1} = y ^ {\prime} \mid_ {x = \frac {1}{2}}.
$$

由于 $y' = \left(\frac{1}{x}\right)' = -\frac{1}{x^2}$, 于是

$$
k _ {1} = - \frac {1}{x ^ {2}} \Bigg | _ {x = \frac {1}{2}} = - 4.
$$

从而所求切线方程为

$$
y - 2 = - 4 \left(x - \frac {1}{2}\right),
$$

即

$$
4 x + y - 4 = 0.
$$

所求法线的斜率为

$$
k _ {2} = - \frac {1}{k _ {1}} = \frac {1}{4},
$$

于是所求法线方程为

$$
y - 2 = \frac {1}{4} \left(x - \frac {1}{2}\right),
$$

即

$$
2 x - 8 y + 1 5 = 0.
$$

例 9 求曲线  $y=x^{\frac{3}{2}}$  的通过点  $(0,-4)$  的切线方程.

解 设切点为 $(x_0, y_0)$，则切线的斜率为

$$
f ^ {\prime} (x _ {0}) = \frac {3}{2} \sqrt {x} \Bigg | _ {x = x _ {0}} = \frac {3}{2} \sqrt {x _ {0}}.
$$

于是所求切线方程可设为

$$
y - y _ {0} = \frac {3}{2} \sqrt {x _ {0}} (x - x _ {0}). \tag {1-7}
$$

因切点 $(x_0, y_0)$ 在曲线 $y = x^{\frac{3}{2}}$ 上，故有

$$
y _ {0} = x _ {0} ^ {\frac {3}{2}}, \tag {1-8}
$$

由已知切线(1-7)通过点(0,-4)，故有