# 第13章 函数列与函数项级数

原始 PDF 第 33–48 页。

## 第十三章

## 函数列与函数项级数

## § 1 一致收敛性

我们已经知道可以用收敛数列(或数项级数)来表示或定义一个数.本章将讨论怎样用函数列(或函数项级数)来表示(或定义)一个函数,并研究这个函数所具有的性质.

## 一、函数列及其一致收敛性

设

$$
f _ {1}, f _ {2}, \dots , f _ {n}, \dots \tag {1}
$$

是一列定义在同一数集 $E$ 上的函数，称为定义在 $E$ 上的函数列.(1)也可简单地写作

$$
\{f _ {n} \} \quad \text {或} \quad f _ {n}, \quad n = 1, 2, \dots .
$$

设 $x_0 \in E$，以 $x_0$ 代入(1)可得数列

$$
f _ {1} (x _ {0}), f _ {2} (x _ {0}), \dots , f _ {n} (x _ {0}), \dots . \tag {2}
$$

若数列(2)收敛,则称函数列(1)在点 $x_{0}$ 收敛, $x_{0}$ 称为函数列(1)的收敛点.若数列(2)发散,则称函数列(1)在点 $x_{0}$ 发散.若函数列(1)在数集 $D\subset E$ 上每一点都收敛,则称(1)在数集D上收敛.这时对D上每一点x,都有数列 $\{f_{n}(x)\}$ 的一个极限值与之相对应,由这个对应法则所确定的D上的函数,称为函数列(1)的极限函数.若把此极限函数记作f,则有

$$
\lim _ {n \to \infty} f _ {n} (x) = f (x), \quad x \in D
$$

或

$$
f _ {n} (x) \rightarrow f (x) \quad (n \rightarrow \infty), \quad x \in D.
$$

函数列极限的 $\varepsilon - N$ 定义是: 对每一固定的 $x \in D$, 任给正数 $\varepsilon$, 恒存在正数 $N$ (注意: 一般说来 $N$ 值的确定与 $\varepsilon$ 和 $x$ 的值都有关, 所以也用 $N(\varepsilon, x)$ 表示它们之间的依赖关系), 使得当 $n > N$ 时, 总有

$$
\mid f _ {n} (x) - f (x) \mid <   \varepsilon .
$$

使函数列 $\{f_{n}\}$ 收敛的全体收敛点集合,称为函数列 $\{f_{n}\}$ 的收敛域.

例 1 设  $f_{n}(x)=x^{n}, n=1,2,\cdots$  为定义在  $(-∞,+∞)$  上的函数列，证明它的收敛域是  $(-1,1]$ ，且有极限函数

25

---

第十三章 函数列与函数项级数

$$
f (x) = \left\{ \begin{array}{l l} 0, & | x | <   1, \\ 1, & x = 1. \end{array} \right. \tag {3}
$$

证 任给 $\varepsilon > 0$ （不妨设 $\varepsilon < 1$），当 $0 < |x| < 1$ 时，由于

$$
\mid f _ {n} (x) - f (x) \mid = \mid x \mid^ {n},
$$

只要取 $N(\varepsilon, x) = \frac{\ln \varepsilon}{\ln |x|}$, 当 $n > N(\varepsilon, x)$ 时, 就有

$$
\left| f _ {n} (x) - f (x) \right| <   \varepsilon .
$$

当 x=0 和 x=1 时, 则对任何正整数 n, 都有

$$
\left| f _ {n} (0) - f (0) \right| = 0 <   \varepsilon , \quad \left| f _ {n} (1) - f (1) \right| = 0 <   \varepsilon.
$$

这就证得 $\{f_{n}\}$ 在 $(-1,1]$ 上收敛，且有(3)式所表示的极限函数.

当 $|x|>1$ 时,则有 $|x|^{n}\rightarrow+\infty\quad(n\rightarrow\infty)$ ,当x=-1时,对应的数列为

$$
- 1, 1, - 1, 1, \dots .
$$

它显然是发散的. 所以函数列  $\{x^{n}\}$  在区间  $(-1,1]$  外都是发散的.

例 2 定义在 $(-∞,+∞)$ 上的函数列 $f_{n}(x)=\frac{\sin nx}{n}, n=1,2,\cdots$ . 由于对任何实数 x, 都有

$$
\left| \frac {\sin n x}{n} \right| \leqslant \frac {1}{n},
$$

故对任给的  $\varepsilon>0$  , 只要  $n>N=\frac{1}{\varepsilon}$  , 就有

$$
\left| \frac {\sin n x}{n} - 0 \right| <   \varepsilon .
$$

所以函数列 $\left\{\frac{\sin nx}{n}\right\}$ 的收敛域为无限区间 $(-∞,+∞)$ ，极限函数 $f(x)=0$ .

对于函数列,我们不仅要讨论它在哪些点上收敛,而更重要的是要研究极限函数所具有的解析性质.比如能否由函数列每项的连续性判断出极限函数的连续性.又如极限函数的导数或积分,是否分别是函数列每项导数或积分的极限.对这些问题的讨论,只要求函数列在数集D上收敛是不够的,必须对它在D上的收敛性提出更高的要求才行,这就是以下所要讨论的一致收敛性问题.

定义1 设函数列 $\{f_n\}$ 与函数 $f$ 定义在同一数集 $D$ 上, 若对任给的正数 $\varepsilon$, 总存在某一正整数 $N$, 使得当 $n > N$ 时, 对一切 $x \in D$, 都有

$$
\mid f _ {n} (x) - f (x) \mid <   \varepsilon ,
$$

则称函数列 $\{f_{n}\}$ 在D上一致收敛于f,记作

$$
f _ {n} (x) \stackrel {\longrightarrow} {\longrightarrow} f (x) (n \to \infty), \quad x \in D.
$$

由定义看到,如果函数列 $\{f_{n}\}$ 在D上一致收敛,那么对于所给的 $\varepsilon$ ,不管D上哪一点x,总存在公共的 $N(\varepsilon)$ （即N的选取仅与 $\varepsilon$ 有关,与x的取值无关）,只要n>N,都有

$$
\left| f _ {n} (x) - f (x) \right| <   \varepsilon .
$$

由此看到函数列 $\{f_n\}$ 在 $D$ 上一致收敛，必在 $D$ 上每一点都收敛.反之，在 $D$ 上每一点都收敛的函数列 $\{f_n\}$，在 $D$ 上不一定一致收敛.

26

---

§ 1 一致收敛性

如上述例2中函数列 $\left\{\frac{\sin nx}{n}\right\}$, 对任给正数 $\varepsilon$, 不管 $x$ 取 $(- \infty, +\infty)$ 上什么值, 都可取 $N = \frac{1}{\varepsilon}$ (它仅依赖于 $\varepsilon$ 的值), 当 $n > N$ 时, 恒有 $\left|\frac{\sin nx}{n}\right| < \varepsilon$, 所以函数列 $\left\{\frac{\sin nx}{n}\right\}$ 在 $(- \infty, +\infty)$ 上一致收敛于函数 $f(x) = 0$.

函数列 $\{f_n\}$ 在 $D$ 上不一致收敛于函数 $f$, 是指它们不满足定义1的条件. 但也可以根据定义1对不一致收敛给予正面的陈述. 即函数列(1)在 $D$ 上不一致收敛于 $f$ 的充要条件是: 存在某正数 $\varepsilon_0$, 对任何正数 $N$, 都有 $D$ 上某一点 $x'$ 与正整数 $n' > N$ (注意: $x'$ 与 $n'$ 的取值与 $N$ 有关), 使得

$$
\mid f _ {n ^ {\prime}} (x ^ {\prime}) - f (x ^ {\prime}) \mid \geqslant \varepsilon_ {0}.
$$

从前面例1中知道，函数列 $\{x^n\}$ 在(0,1)上收敛于 $f(x) = 0$。我们证明它在(0,1)上不一致收敛。事实上，令 $\varepsilon_0 = \frac{1}{2}$，对任何正数 $N$，取正整数 $n > N + 1$ 及 $x' = \left(1 - \frac{1}{n}\right)^{\frac{1}{n}} \in (0,1)$，则有

$$
\mid x ^ {\prime n} - 0 \mid = 1 - \frac {1}{n} \geqslant \frac {1}{2}.
$$

函数列(1)一致收敛于f,从几何意义上讲:对任何正数 $\varepsilon$ ,存在正整数N,对于一切序号大于N的曲线 $y=f_{n}(x)$ ,都落在以曲线 $y=f(x)+\varepsilon$ 与 $y=f(x)-\varepsilon$ 为边(即以曲线 $y=f(x)$ 为“中心线”,宽度为 $2\varepsilon$ )的带形区域内(如图13-1所示).

函数列 $\{x^n\}$ 在区间(0,1)内不一致收敛，从几何意义上讲:对于某个事先给定的 $\varepsilon$ （$0 < \varepsilon < 1$），无论 $N$ 多么大，总有曲线 $y = x^n$（$n > N$）不能全部落在以 $y = \varepsilon$ 与 $y = -\varepsilon$ 为边的带形区域内，如图13-2所示。若函数列 $\{x^n\}$ 只限于在区间(0,b)(b<1)内讨论，容易看到，只要 $n > \frac{\ln \varepsilon}{\ln b}$（其中 $0 < \varepsilon < 1$），曲线 $y = x^n$ 就全部落在以 $y = \varepsilon$ 和 $y = -\varepsilon$ 为上下边的带形区域内。所以 $\{x^n\}$ 在(0,b)内是一致收敛的。

![](../../raw/pages_0033-0064/images/page_34_image_8.jpg)

<details>
<summary>text_image</summary>

y
f(x)
fn(x)
O
a
b
x
f(x)+ε
f(x)-ε
</details>

图13-1

![](../../raw/pages_0033-0064/images/page_34_image_10.jpg)

<details>
<summary>text_image</summary>

y
x¹
x²
ε
O
-ε
1 x
</details>

图13-2

定理13.1（函数列一致收敛的柯西准则）函数列 $\{f_n\}$ 在数集 $D$ 上一致收敛的充要条件是:对任给正数 $\varepsilon$ ，总存在正数 $N$ ，使得当 $n, m > N$ 时，对一切 $x \in D$ ，都有

$$
\left| f _ {n} (x) - f _ {m} (x) \right| <   \varepsilon . \tag {4}
$$

证 [必要性] 设 $f_{n}(x) \longrightarrow f(x) (n \to \infty), x \in D$，即对任给 $\varepsilon > 0$，存在正数 $N$，使得当 $n > N$ 时，对一切 $x \in D$，都有

27

---

第十三章 函数列与函数项级数

$$
\left| f _ {n} (x) - f (x) \right| <   \frac {\varepsilon}{2}. \tag {5}
$$

于是当 $n, m > N$，由(5)就有

$$
\begin{array}{l} \left| f _ {n} (x) - f _ {m} (x) \right| \leqslant \left| f _ {n} (x) - f (x) \right| + \left| f (x) - f _ {m} (x) \right| \\ <   \frac {\varepsilon}{2} + \frac {\varepsilon}{2} = \varepsilon . \\ \end{array}
$$

[充分性] 若条件(4)成立,由数列收敛的柯西准则, $\{f_{n}\}$ 在D上任一点都收敛,记其极限函数为 $f(x),x\in D.$ 现固定(4)式中的n,让 $m\to\infty$ ,于是当n>N时,对一切 $x\in D$ ,都有

$$
\left| f _ {n} (x) - f (x) \right| \leqslant \varepsilon .
$$

由定义 1, $f_{n}(x)\longrightarrow f(x)$ ( $n\to\infty$ ), $x\in D$.

根据一致收敛定义可推出下述定理.

定理13.2 函数列 $\{f_n\}$ 在区间 $D$ 上一致收敛于 $f$ 的充要条件是:

$$
\lim _ {n \to \infty} \sup _ {x \in D} | f _ {n} (x) - f (x) | = 0. \tag {6}
$$

证 [必要性] 若 $f_{n}(x) \longrightarrow f(x) (n \to \infty), x \in D$. 则对任给的正数 $\varepsilon$, 存在不依赖于 $x$ 的正整数 $N$, 当 $n > N$ 时, 有

$$
\left| f _ {n} (x) - f (x) \right| <   \varepsilon , \quad x \in D.
$$

由上确界的定义,亦有

$$
\sup _ {x \in D} \left| f _ {n} (x) - f (x) \right| \leqslant \varepsilon .
$$

这就证得(6)式成立.

[充分性] 由假设,对任给  $\varepsilon>0$ , 存在正整数 N, 使得当 n>N 时, 有

$$
\sup _ {x \in D} | f _ {n} (x) - f (x) | <   \varepsilon . \tag {7}
$$

因为对一切 $x \in D$，总有

$$
\left| f _ {n} (x) - f (x) \right| \leqslant \sup _ {x \in D} \left| f _ {n} (x) - f (x) \right|,
$$

故由(7)式得

$$
\left| f _ {n} (x) - f (x) \right| <   \varepsilon .
$$

于是 $\{f_{n}\}$ 在D上一致收敛于f.

在判断函数列是否一致收敛上定理13.2更为方便一些（其缺点是必须事先知道它的极限函数），如例2，由于

$$
\lim _ {n \to \infty} \sup _ {x \in (- \infty , + \infty)} \left| \frac {\sin n x}{n} - 0 \right| = \lim _ {n \to \infty} \frac {1}{n} = 0,
$$

所以在 $(-∞,+∞)$ 上， $\frac{\sin nx}{n}\xrightarrow[n]{\longrightarrow}0(n\to\infty)$ .

推论 函数列 $\{f_n\}$ 在 $D$ 上不一致收敛于 $f$ 的充分且必要条件是: 存在 $\{x_{n}\} \subset D$, 使得 $\{f_n(x_n) - f(x_n)\}$ 不收敛于 0.

例 3 设  $f_{n}(x)=nx\mathrm{e}^{-nx^{2}}, x \in D=(0,+\infty), n=1,2,\cdots.$  判别  $\{f_{n}(x)\}$  在 D 上的一致收敛性.

解 对任意 $x \in (0, +\infty)$, $\lim_{n \to \infty} n x \mathrm{e}^{-nx^2} = 0 = f(x)$. 在 $(0, +\infty)$ 上, 每个 $n x \mathrm{e}^{-nx^2}$ 只有一个

28

---

§ 1 一致收敛性

极大值点 $x_{n} = \frac{1}{\sqrt{2n}}$，而 $\sup_{x\in (0, + \infty)}|f_n(x)| = f_n(x_n) = \sqrt{\frac{n}{2}}\mathrm{e}^{-\frac{1}{2}}\rightarrow$ $\infty$。因此由定理13.2可知 $\{f_n\}$ 在 $D$ 上不一致收敛于 $f$。（见图13-3）

为避免求上确界, 亦可取 $x_{n} = \frac{1}{n} \in (0, +\infty)$, 则 $f_{n}(x_{n}) = \mathrm{e}^{-\frac{1}{n}} \to 1 \neq 0 (n \to \infty)$, 因此由推论同样可知 $\{f_{n}\}$ 在 $(0, +\infty)$ 上不一致收敛于 $f(x)$.

定义 2 设函数列  $\{f_{n}\}$  与 f 定义在区间 I 上, 若对任意闭区间  $[a, b] \subset I, \{f_{n}\}$  在  $[a, b]$  上一致收敛于 f, 则称  $\{f_{n}\}$  在 I 上内闭一致收敛于 f.

![](../../raw/pages_0033-0064/images/page_36_chart_4.jpg)

<details>
<summary>contour</summary>

| Category | Peak X-coordinate | Peak Y-value |
| --- | --- | --- |
| n=15 | ~0.2 | ~0.9 |
| n=10 | ~0.3 | ~0.6 |
| y=nxe^-nx^2 | 1/√(2n) | ~0.4 |
</details>

图13-3

注 若 $I = [\alpha, \beta]$ 是有界闭区间，显然 $\{f_n\}$ 在 $I$ 上内闭一致收敛于 $f$ 与 $\{f_n\}$ 在 $I$ 上一致收敛于 $f$ 是一致的.

例1中函数列 $\{f_n\}$ 在[0,1)上不一致收敛于 $f$ ，但对任意 $\delta >0$ ， $\sup_{x\in [0,\delta]}|x^n |\leqslant \delta^n\to 0(n\to \infty)$ ，因此 $\{f_n\}$ 在[0,1)上内闭一致收敛.

例3中函数列 $\{f_n\}$ 在 $(0, +\infty)$ 上不一致收敛于0，但对任意 $[a, b] \subset (0, +\infty)$，$\sup_{x \in [a, b]} |nxe^{-nx^2}| \leqslant nbe^{-na^2} \to 0 (n \to \infty)$，因此 $\{f_n\}$ 在 $(0, +\infty)$ 上内闭一致收敛于0.

## 二、函数项级数及其一致收敛性

设 $\{u_{n}(x)\}$ 是定义在数集E上的一个函数列,表达式

$$
u _ {1} (x) + u _ {2} (x) + \dots + u _ {n} (x) + \dots , \quad x \in E \tag {8}
$$

称为定义在 $E$ 上的函数项级数，简记为 $\sum_{n=1}^{\infty} u_n(x)$ 或 $\sum u_n(x)$. 称

$$
S _ {n} (x) = \sum_ {k = 1} ^ {n} u _ {k} (x), \quad x \in E, \quad n = 1, 2, \dots \tag {9}
$$

为函数项级数(8)的部分和函数列.

若 $x_0 \in E$，数项级数

$$
u _ {1} (x _ {0}) + u _ {2} (x _ {0}) + \dots + u _ {n} (x _ {0}) + \dots \tag {10}
$$

收敛, 即部分和 $S_{n}(x_{0}) = \sum_{k=1}^{n} u_{k}(x_{0})$ 当 $n \to \infty$ 时极限存在, 则称级数 (8) 在点 $x_{0}$ 收敛, $x_{0}$ 称为级数 (8) 的收敛点. 若级数 (10) 发散, 则称级数 (8) 在点 $x_{0}$ 发散. 若级数 (8) 在 $E$ 的某个子集 $D$ 上每点都收敛, 则称级数 (8) 在 $D$ 上收敛. 若 $D$ 为级数 (8) 全体收敛点的集合, 这时则称 $D$ 为级数 (8) 的收敛域. 级数 (8) 在 $D$ 上每一点 $x$ 与其所对应的数项级数 (10) 的和 $S(x)$ 构成一个定义在 $D$ 上的函数, 称为级数 (8) 的和函数, 并写作

$$
u _ {1} (x) + u _ {2} (x) + \dots + u _ {n} (x) + \dots = S (x), \quad x \in D,
$$

即

$$
\lim _ {n \to \infty} S _ {n} (x) = S (x), \quad x \in D.
$$

也就是说,函数项级数(8)的收敛性就是指它的部分和函数列(9)的收敛性.

例 4 定义在 $(-∞,+∞)$ 上的函数项级数(几何级数)

29

---

第十三章 函数列与函数项级数

$$
1 + x + x ^ {2} + \dots + x ^ {n} + \dots \tag {11}
$$

的部分和函数为 $S_{n}(x) = \frac{1 - x^{n}}{1 - x}$. 当 $|x| < 1$ 时，

$$
S (x) = \lim _ {n \to \infty} S _ {n} (x) = \frac {1}{1 - x}.
$$

所以几何级数(11)在 $(-1,1)$ 内收敛于和函数 $S(x)=\frac{1}{1-x}$ ; 当 $|x|\geqslant1$ 时, 几何级数是发散的.

定义3 设 $\{S_n(x)\}$ 是函数项级数 $\sum u_n(x)$ 的部分和函数列.若 $\{S_n(x)\}$ 在数集 $D$ 上一致收敛于 $S(x)$，则称 $\sum u_n(x)$ 在 $D$ 上一致收敛于 $S(x)$. 若 $\sum u_n(x)$ 在任意闭区间 $[a, b] \subset I$ 上一致收敛，则称 $\sum u_n(x)$ 在 $I$ 上内闭一致收敛.

由于函数项级数的一致收敛性由它的部分和函数列来确定,所以由前段中有关函数列一致收敛的定理,都可推出相应的有关函数项级数的定理.

定理 13.3(一致收敛的柯西准则) 函数项级数  $\sum u_{n}(x)$  在数集 D 上一致收敛的充要条件为: 对任给的正数  $\varepsilon$ , 总存在某正整数 N, 使得当 n > N 时, 对一切  $x \in D$  和一切正整数 p, 都有

$$
\mid S _ {n + p} (x) - S _ {n} (x) \mid <   \varepsilon
$$

或

$$
\mid u _ {n + 1} (x) + u _ {n + 2} (x) + \dots + u _ {n + p} (x) \mid <   \varepsilon .
$$

此定理中当 p=1 时, 得到函数项级数一致收敛的一个必要条件.

推论 函数项级数 $\sum u_{n}(x)$ 在数集 $D$ 上一致收敛的必要条件是函数列 $\{u_n(x)\}$ 在 $D$ 上一致收敛于零.

设函数项级数 $\sum u_{n}(x)$ 在 $D$ 上的和函数为 $S(x)$，称

$$
R _ {n} (x) = S (x) - S _ {n} (x)
$$

为函数项级数  $\sum u_{n}(x)$  的余项.

定理13.4 函数项级数 $\sum u_{n}(x)$ 在数集 $D$ 上一致收敛于 $S(x)$ 的充要条件是

$$
\lim _ {n \to \infty} \sup _ {x \in D} | R _ {n} (x) | = \lim _ {n \to \infty} \sup _ {x \in D} | S (x) - S _ {n} (x) | = 0.
$$

我们再来看例4中的级数 $\sum_{n = 0}^{\infty}x^n$ ，由于

$$
\begin{array}{l} \sup _ {x \in (- 1, 1)} | S _ {n} (x) - S (x) | = \sup _ {x \in (- 1, 1)} \left| \frac {x ^ {n}}{x - 1} \right| \geqslant \left| \frac {\left(\frac {n}{n + 1}\right) ^ {n}}{1 - \frac {n}{n + 1}} \right| \\ = n \left(\frac {n}{n + 1}\right) ^ {n - 1} \rightarrow \infty (n \rightarrow \infty), \\ \end{array}
$$

知道级数  $\sum_{n=0}^{\infty}x^{n}$  在  $(-1,1)$  上不一致收敛.

对任意  $a \quad (0 < a < 1)$ ,

$$
\sup _ {x \in [ - a, a ]} | S _ {n} (x) - S (x) | = \sup _ {x \in [ - a, a ]} \left| \frac {- x ^ {n}}{1 - x} \right| = \frac {a ^ {n}}{1 - a} \rightarrow 0 \quad (n \rightarrow \infty)
$$

30

---

§ 1 一致收敛性 |||

可得级数 $\sum x^n$ 在 $(-1,1)$ 上内闭一致收敛.

## 三、函数项级数的一致收敛性判别法

判别函数项级数的一致收敛性除了根据定义或定理 13.4 外,有些级数还可根据级数各项的特性来判别.

定理 13.5(魏尔斯特拉斯判别法) 设函数项级数  $\sum u_{n}(x)$  定义在数集 D 上,  $\sum M_{n}$  为收敛的正项级数, 若对一切  $x \in D$ , 有

$$
\mid u _ {n} (x) \mid \leqslant M _ {n}, \quad n = 1, 2, \dots , \tag {12}
$$

则函数项级数 $\sum u_{n}(x)$ 在 $D$ 上一致收敛.

证 由假设正项级数 $\sum M_{n}$ 收敛, 根据数项级数的柯西准则, 任给正数 $\varepsilon$, 存在某正整数 $N$, 使得当 $n > N$ 及任何正整数 $p$, 有

$$
\left| M _ {n + 1} + \dots + M _ {n + p} \right| = M _ {n + 1} + \dots + M _ {n + p} <   \varepsilon .
$$

又由(12)式,对一切  $x \in D$  有

$$
\begin{array}{l} \mid u _ {n + 1} (x) + \dots + u _ {n + p} (x) \mid \leqslant \mid u _ {n + 1} (x) \mid + \dots + \mid u _ {n + p} (x) \mid \\ \leqslant M _ {n + 1} + \dots + M _ {n + p} <   \varepsilon . \\ \end{array}
$$

根据函数项级数一致收敛的柯西准则,级数 $\sum u_{n}(x)$ 在D上一致收敛.

![](../../raw/pages_0033-0064/images/page_38_image_12.jpg)

例5 函数项级数

$$
\sum \frac {\sin n x}{n ^ {2}}, \qquad \sum \frac {\cos n x}{n ^ {2}}
$$

在 $(-\infty, +\infty)$ 上一致收敛，因为对一切 $x \in (-\infty, +\infty)$ 有

$$
\left| \frac {\sin n x}{n ^ {2}} \right| \leqslant \frac {1}{n ^ {2}}, \quad \left| \frac {\cos n x}{n ^ {2}} \right| \leqslant \frac {1}{n ^ {2}},
$$

而正项级数  $\sum\frac{1}{n^{2}}$  是收敛的.

![](../../raw/pages_0033-0064/images/page_38_image_18.jpg)

定理13.5也称为 $M$ 判别法或优级数判别法.当级数 $\sum u_{n}(x)$ 与级数 $\sum M_{n}$ 在区间$[a,b]$ 上成立关系式(12)时，则称级数 $\sum M_n$ 在 $[a,b]$ 上优于级数 $\sum u_{n}(x)$ ，或称 $\sum M_{n}$ 为 $\sum u_{n}(x)$ 的优级数.

下面讨论定义在区间 $I$ 上形如

$$
\sum u _ {n} (x) v _ {n} (x) = u _ {1} (x) v _ {1} (x) + u _ {2} (x) v _ {2} (x) + \dots + u _ {n} (x) v _ {n} (x) + \dots \tag {13}
$$

的函数项级数的一致收敛性判别法,它与数项级数一样,也是基于阿贝尔分部求和公式(第十二章§3的引理).

定理 13.6(阿贝尔判别法) 设

(i)  $\sum u_{n}(x)$  在区间 I 上一致收敛；
(ii) 对于每一个 $x \in I, \{v_n(x)\}$ 是单调的；
(iii)  $\{v_{n}(x)\}$  在 I 上一致有界, 即存在正数 M, 使得对一切  $x \in I$  和正整数 n, 有

$$
\mid v _ {n} (x) \mid \leqslant M,
$$

则级数(13)在 I 上一致收敛.

证 由(i)，任给 $\varepsilon > 0$ ，存在某正数 $N$ ，使得当 $n > N$ 及任何正整数 $p$ ，对一切 $x \in I$ ，有

$$
\mid u _ {n + 1} (x) + \dots + u _ {n + p} (x) \mid <   \varepsilon .
$$

又由(ii)，(iii)及阿贝尔引理(第十二章§3引理的推论)得到

31

---

第十三章 函数列与函数项级数

$$
\begin{array}{l} \left| u _ {n + 1} (x) v _ {n + 1} (x) + \dots + u _ {n + p} (x) v _ {n + p} (x) \right| \\ \leqslant \left(\left| v _ {n + 1} (x) \right| + 2 \left| v _ {n + p} (x) \right|\right) \varepsilon \leqslant 3 M \varepsilon. \\ \end{array}
$$

于是根据函数项级数一致收敛性的柯西准则就得到本定理的结论.

定理 13.7(狄利克雷判别法) 设

(i) $\sum u_{n}(x)$ 的部分和函数列

$$
S _ {n} (x) = \sum_ {k = 1} ^ {n} u _ {k} (x) \quad (n = 1, 2, \dots)
$$

在 I 上一致有界；

(ii) 对于每一个 $x \in I, \{v_n(x)\}$ 是单调的；

(iii) 在 I 上  $v_{n}(x) \longrightarrow 0 (n \to \infty)$ ,

则级数(13)在 I 上一致收敛.

证 证法与定理13.6相仿.由(i)，存在正数 $M$ ，对一切 $x\in I$ ，有 $\mid S_n(x)\mid \leqslant M.$ 因此当 $n,p$ 为任何正整数时，

$$
\mid u _ {n + 1} (x) + \dots + u _ {n + p} (x) \mid = \mid S _ {n + p} (x) - S _ {n} (x) \mid \leqslant 2 M.
$$

对任何一个 $x \in I$，再由(ii)及阿贝尔引理，得到

$$
\begin{array}{l} \left| u _ {n + 1} (x) v _ {n + 1} (x) + \dots + u _ {n + p} (x) v _ {n + p} (x) \right| \\ \leqslant 2 M (\mid v _ {n + 1} (x) \mid + 2 \mid v _ {n + p} (x) \mid). \\ \end{array}
$$

再由(iii)，对任给的 $\varepsilon > 0$ ，存在正数 $N$ ，当 $n > N$ 时，对一切 $x \in I$ ，有

$$
\mid v _ {n} (x) \mid <   \varepsilon ,
$$

所以

$$
\mid u _ {n + 1} (x) v _ {n + 1} (x) + \dots + u _ {n + p} (x) v _ {n + p} (x) \mid <   2 M (\varepsilon + 2 \varepsilon) = 6 M \varepsilon .
$$

于是由一致收敛性的柯西准则,级数(13)在I上一致收敛.

例6 函数项级数

$$
\sum \frac {(- 1) ^ {n} (x + n) ^ {n}}{n ^ {n + 1}}
$$

在[0,1]上一致收敛. 这是因为记 $u_{n}(x) = \frac{(-1)^{n}}{n}, v_{n}(x) = \left(1 + \frac{x}{n}\right)^{n}$ 时，由阿贝尔判别法（定理13.6）就能得到结果. □

例 7 若数列  $\{a_{n}\}$  单调且收敛于零, 则级数

$$
\sum a _ {n} \cos n x \tag {14}
$$

在 $\left[\alpha,2\pi-\alpha\right]\left(0<\alpha<\pi\right)$ 上一致收敛.

证 由第十二章 §3(21)式, 在  $[\alpha, 2\pi-\alpha]$  上有

$$
\begin{array}{l} \left| \sum_ {k = 1} ^ {n} \cos k x \right| = \left| \frac {\sin \left(n + \frac {1}{2}\right) x}{2 \sin \frac {x}{2}} - \frac {1}{2} \right| \\ \leqslant \frac {1}{2 \left| \sin \frac {x}{2} \right|} + \frac {1}{2} \leqslant \frac {1}{2 \sin \frac {\alpha}{2}} + \frac {1}{2}, \\ \end{array}
$$

所以级数  $\sum \cos nx$  的部分和函数列在  $[\alpha, 2\pi - \alpha]$  上一致有界，于是令

32

---

§ 1 一致收敛性

$$
u _ {n} (x) = \cos n x, v _ {n} (x) = a _ {n},
$$

则由狄利克雷判别法可得级数(14)在 $[\alpha,2\pi-\alpha]$ 上一致收敛.

对于例7中的级数(14)，只要 $\{a_{n}\}$ 单调且收敛于零，那么级数(14)在不包含 $2k\pi(k=0,\pm1,\pm2,\cdots)$ 的任何闭区间上都一致收敛.

## 习题 13.1

1. 讨论下列函数列在所示区间 $D$ 上是否一致收敛或内闭一致收敛，并说明理由:

(1)  $f_{n}(x)=\sqrt{x^{2}+\frac{1}{n^{2}}}$ ,  $n=1,2,\cdots$ ,  $D=(-1,1)$ ;
(2) $f_{n}(x)=\frac{x}{1+n^{2}x^{2}},\quad n=1,2,\cdots,\quad D=(-\infty,+\infty);$

(3) $f_{n}(x)=\left\{\begin{aligned}-(n+1)x+1,&0\leqslant x\leqslant\frac{1}{n+1},\\ 0,&\frac{1}{n+1}<x<1,\quad n=1,2,\cdots;\end{aligned}\right.$

(4)  $f_{n}(x)=\frac{x}{n},\quad n=1,2,\cdots,\quad D=\left[0,+\infty\right)$ ;

(5) $f_{n}(x)=\sin\frac{x}{n},\quad n=1,2,\cdots,\quad D=(-\infty,+ \infty).$

2. 证明:设 $f_{n}(x) \to f(x), x \in D, a_{n} \to 0 (n \to \infty) (a_{n} > 0)$. 若对每一个正整数 $n$ 有 $|f_{n}(x) - f(x)| \leqslant a_{n}, x \in D$，则 $\{f_{n}\}$ 在 $D$ 上一致收敛于 $f$.

3. 判别下列函数项级数在所示区间上的一致收敛性:

(1)  $\sum\frac{x^{n}}{(n-1)!}, x\in[-r,r]$ ;
(2) $\sum \frac{(-1)^{n-1}x^2}{(1+x^2)^n}, x \in (-\infty, +\infty)$;
(3)  $\sum\frac{n}{x^{n}}, |x| > r \geqslant 1;$
(4)  $\sum\frac{x^{n}}{n^{2}}, x \in [0,1]$ ;
(5)  $\sum\frac{(-1)^{n-1}}{x^{2}+n}, x\in(-\infty,+\infty)$ ;
(6)  $\sum\frac{x^{2}}{\left(1+x^{2}\right)^{n-1}}, x\in(-\infty,+\infty).$

4. 设函数项级数 $\sum u_{n}(x)$ 在 $D$ 上一致收敛于 $S(x)$，函数 $g(x)$ 在 $D$ 上有界。证明级数 $\sum g(x)u_{n}(x)$ 在 $D$ 上一致收敛于 $g(x)S(x)$。

5. 若在区间 I 上, 对任何正整数 n,

$$
\mid u _ {n} (x) \mid \leqslant v _ {n} (x),
$$

证明当 $\sum v_{n}(x)$ 在 $I$ 上一致收敛时，级数 $\sum u_{n}(x)$ 在 $I$ 上也一致收敛.

6. 设  $u_{n}(x)$  ( $n=1,2,\cdots$ ) 是  $[a,b]$  上的单调函数. 证明: 若  $\sum u_{n}(a)$  与  $\sum u_{n}(b)$  都绝对收敛, 则  $\sum u_{n}(x)$  在  $[a,b]$  上绝对且一致收敛.

7. 证明: $\{f_{n}\}$  在区间 I 上内闭一致收敛于 f 的充分且必要条件是:对任意  $x_{0} \in I$ ，存在  $x_{0}$  的一个邻域  $U(x_{0})$ ，使得  $\{f_{n}\}$  在  $U(x_{0}) \cap I$  上一致收敛于 f.

8. 在 $[0,1]$ 上定义函数列

$$
u _ {n} (x) = \left\{ \begin{array}{l l} \frac {1}{n}, & x = \frac {1}{n}, \\ 0, & x \neq \frac {1}{n}, \end{array} \right. n = 1, 2, \dots ,
$$

证明级数 $\sum u_{n}(x)$ 在[0,1]上一致收敛，但它不存在优级数.

33

---

第十三章 函数列与函数项级数

9. 讨论下列函数列或函数项级数在所示区间 $D$ 上的一致收敛性:

(1) $\sum_{n=2}^{\infty} \frac{1 - 2n}{\left(x^{2} + n^{2}\right)\left[x^{2} + (n-1)^{2}\right]}, D = [-1,1]$;
(2)  $\sum 2^{n}\sin\frac{x}{3^{n}}, D=(0,+\infty)$ ;
(3)  $\sum\frac{x^{2}}{\left[1+(n-1)x^{2}\right](1+nx^{2})},D=(0,+\infty);$
(4)  $\sum\frac{x^{n}}{\sqrt{n}}, D=[-1,0]$ ;
(5)  $\sum(-1)^{n}\frac{x^{2n+1}}{2n+1}, D=(-1,1)$ ;
(6) $\sum_{n=1}^{\infty} \frac{\sin nx}{n}, D = (0, 2\pi)$.

10. 证明: 级数 $\sum (-1)^n x^n (1 - x)$ 在 $[0,1]$ 上绝对收敛并一致收敛, 但由其各项绝对值组成的级数在 $[0,1]$ 上却不一致收敛.

11. 设 $f$ 为定义在区间 $(a, b)$ 内的任一函数，记

$$
f _ {n} (x) = \frac {\left[ n f (x) \right]}{n}, \quad n = 1, 2, \dots ,
$$

证明函数列 $\{f_{n}\}$ 在 $(a,b)$ 内一致收敛于f.

12. 设 $\{u_n(x)\}$ 为 $[a, b]$ 上正的递减且收敛于零的函数列，每一个 $u_n(x)$ 都是 $[a, b]$ 上的单调函数，则级数

$$
u _ {1} (x) - u _ {2} (x) + u _ {3} (x) - u _ {4} (x) + \dots
$$

在 $[a,b]$ 上不仅收敛,而且一致收敛.

13. 证明: 若 $\{f_n(x)\}$ 在区间 $I$ 上一致收敛于 0, 则存在子列 $\{f_{n_i}\}$, 使得 $\sum_{i=1}^{\infty} f_{n_i}(x)$ 在 $I$ 上一致收敛.

## § 2 一致收敛函数列与函数项级数的性质

本节讨论由函数列与函数项级数所确定的函数的连续性、可积性与可微性.

定理13.8 设函数列 $\{f_n\}$ 在 $(a, x_0) \cup (x_0, b)$ 上一致收敛于 $f(x)$，且对每个 $n$，$\lim_{x \to x_0} f_n(x) = a_n$，则 $\lim_{n \to \infty} a_n$ 和 $\lim_{x \to x_0} f(x)$ 均存在且相等。

证 先证 $\{a_{n}\}$ 是收敛数列. 对任意 $\varepsilon > 0$, 由于 $\{f_{n}\}$ 一致收敛, 故有 $N$, 当 $n > N$ 时, 对任意正整数 $p$ 和对一切 $x \in (a, x_{0}) \cup (x_{0}, b)$, 有

$$
\left| f _ {n} (x) - f _ {n + p} (x) \right| <   \varepsilon . \tag {1}
$$

从而

$$
\mid a _ {n} - a _ {n + p} \mid = \lim _ {x \to x _ {0}} \mid f _ {n} (x) - f _ {n + p} (x) \mid \leqslant \varepsilon .
$$

这样由柯西准则可知 $\{a_{n}\}$ 是收敛数列.

设 $\lim_{n\to \infty}a_n = A$ .再证 $\lim_{x\to x_0}f(x) = A$

34

---

§ 2 一致收敛函数列与函数项级数的性质

由于 $f_{n}(x)$ 一致收敛于 $f(x)$ 及 $a_{n}$ 收敛于 $A$ ，因此对任意 $\varepsilon >0$ ，存在正数 $N$ ，当 $n > N$ 时，对任意 $x\in (a,x_0)\cup (x_0,b)$

$$
\mid f _ {n} (  x  ) - f (  x  ) \mid   <     \frac {\varepsilon}{3} \quad \text {和} \quad \mid a _ {n} - A \mid   <     \frac {\varepsilon}{3}
$$

同时成立. 特别取  $n=N+1$ , 有

$$
\left| f _ {N + 1} (x) - f (x) \right| <   \frac {\varepsilon}{3}, \quad \left| a _ {N + 1} - A \right| <   \frac {\varepsilon}{3}.
$$

又 $\lim_{x\to x_0}f_{N + 1}(x) = a_{N + 1}$ ，故存在 $\delta >0$ ，当 $0 < |x - x_0| < \delta$ 时，

$$
\left| f _ {N + 1} (x) - a _ {N + 1} \right| <   \frac {\varepsilon}{3}.
$$

这样, 当 x 满足  $0 < |x - x_{0}| < \delta$  时,

$$
\begin{array}{l} \left| f (x) - A \right| \leqslant \left| f (x) - f _ {N + 1} (x) \right| + \left| f _ {N + 1} (x) - a _ {N + 1} \right| + \left| a _ {N + 1} - A \right| \\ <   \frac {\varepsilon}{3} + \frac {\varepsilon}{3} + \frac {\varepsilon}{3} = \varepsilon , \\ \end{array}
$$

即  $\lim_{x\to x_{0}}f(x)=A.$

![](../../raw/pages_0033-0064/images/page_42_image_10.jpg)

这个定理指出:在一致收敛的条件下, $\{f_{n}(x)\}$ 中两个独立变量x与n,在分别求极限时其求极限的顺序可以交换,即

$$
\lim _ {x \to x _ {0}} \lim _ {n \to \infty} f _ {n} (x) = \lim _ {n \to \infty} \lim _ {x \to x _ {0}} f _ {n} (x). \tag {2}
$$

类似地，若 $f_{n}(x)$ 在 $(a,b)$ 上一致收敛且 $\lim_{x\to a^{+}}f_{n}(x)$ 存在，可推得 $\lim_{x\to a^{+}}\lim_{n\to \infty}f_n(x) =$ $\lim_{n\to \infty}\lim_{x\to a^{+}}f_{n}(x)$ ；若 $f_{n}(x)$ 在 $(a,b)$ 上一致收敛且 $\lim_{x\to b^{-}}f_n(x)$ 存在，则可推得 $\lim_{x\to b^{-}}\lim_{n\to \infty}f_n(x) =$ $\lim_{n\to \infty}\lim_{x\to b^{-}}f_n(x)$

由定理 13.8 可得到以下定理.

定理 13.9(连续性) 若函数列  $\{f_{n}\}$  在区间 I 上一致收敛, 且每一项都连续, 则其极限函数 f 在 I 上也连续.

证 设 $x_0$ 为 $I$ 上任一点. 由于 $\lim_{x\to x_0}f_n(x) = f_n(x_0)$, 于是由定理13.8知 $\lim_{x\to x_0}f(x)$ 亦存在, 且 $\lim_{x\to x_0}f(x) = \lim_{n\to \infty}f_n(x_0) = f(x_0)$, 因此 $f(x)$ 在 $x_0$ 上连续.

由定理 13.9 可知: 若各项为连续函数的函数列在区间 I 上其极限函数不连续, 则此函数列在区间 I 上不一致收敛.

例如:函数列 $\{x^{n}\}$ 的各项在 $(-1,1]$ 上都是连续的,但其极限函数

$$
f (x) = \left\{ \begin{array}{l l} 0, & - 1 <   x <   1, \\ 1, & x = 1 \end{array} \right.
$$

在 x=1 时不连续,从而推得  $\{x^{n}\}$  在  $(-1,1]$  上不一致收敛.

注意到函数 $f(x)$ 在 $x$ 上连续仅与它在 $x$ 的近旁的性质有关，因此由定理13.9可得以下推论.

推论 若连续函数列  $\{f_{n}\}$  在区间 I 上内闭一致收敛于 f，则 f 在 I 上连续.

上节例1中 $\{f_n(x)\} = \{x^n\}$ 在 $(-1,1)$ 上不一致收敛，但内闭一致收敛，其极限函数在 $(-1,1)$ 上连续.

35

---

第十三章 函数列与函数项级数

定理13.10（可积性） 若函数列 $\{f_n\}$ 在 $[a,b]$ 上一致收敛，且每一项都连续，则

$$
\int_ {a} ^ {b} \lim _ {n \to \infty} f _ {n} (x) \mathrm{d} x = \lim _ {n \to \infty} \int_ {a} ^ {b} f _ {n} (x) \mathrm{d} x. \tag {3}
$$

证 设 f 为函数列  $\{f_{n}\}$  在  $[a, b]$  上的极限函数. 由定理 13.9, f 在  $[a, b]$  上连续, 从而  $f_{n}$  ( $n=1,2,\cdots$ ) 与 f 在  $[a, b]$  上都可积.

因为在 $[a, b]$ 上 $f_n \longrightarrow f (n \to \infty)$, 故对任给正数 $\varepsilon$, 存在 $N$, 当 $n > N$ 时, 对一切 $x \in [a, b]$, 都有

$$
\left| f _ {n} (x) - f (x) \right| <   \varepsilon .
$$

再根据定积分的性质, 当 n > N 时有

$$
\begin{array}{l} \left| \int_ {a} ^ {b} f _ {n} (x) \mathrm{d} x - \int_ {a} ^ {b} f (x) \mathrm{d} x \right| = \left| \int_ {a} ^ {b} (f _ {n} (x) - f (x)) \mathrm{d} x \right| \\ \leqslant \int_ {a} ^ {b} \left| f _ {n} (x) - f (x) \right| \mathrm{d} x \\ \leqslant \varepsilon (b - a). \\ \end{array}
$$

这就证明了等式(3).

这个定理指出:在一致收敛的条件下,极限运算与积分运算的顺序可以交换.

例1 设函数

$$
f _ {n} (x) = \left\{ \begin{array}{l l} 2 n \alpha_ {n} x, & 0 \leqslant x <   \frac {1}{2 n}, \\ 2 \alpha_ {n} - 2 n \alpha_ {n} x, & \frac {1}{2 n} \leqslant x <   \frac {1}{n}, \\ 0, & \frac {1}{n} \leqslant x \leqslant 1, \end{array} \right. \quad n = 1, 2, \dots .
$$

其图像如图 13-4 所示.

显然 $\{f_n(x)\}$ 是[0,1]上的连续函数列，且对任意 $x\in [0,1]$ ， $\lim_{n\to \infty}f_n(x) = 0.$ 又 $\sup_{x\in [0,1]}\left|f_n(x) - 0\right| = \alpha_{n}$ ，因此 $\{f_n(x)\}$ 在[0,1]上一致收敛于0的充要条件是 $\alpha_{n}\rightarrow 0$ （ $n\to \infty$ ）.

由于 $\int_0^1 f_n(x)\mathrm{d}x = \frac{\alpha_n}{2n}$ ，因此 $\int_0^1 f_n(x)\mathrm{d}x\to \int_0^1 f(x)\mathrm{d}x = 0$ 的充要条件是 $\lim_{n\to \infty}\frac{\alpha_n}{2n} = 0.$ 这样当 $\alpha_{n}\equiv 1$ 时，虽然 $\{f_n(x)\}$ 不一致收敛于 $f(x)$ ，但定理13.10的结论仍成立.但当 $\alpha_{n} = n$ 时，$\{f_n(x)\}$ 不一致收敛于 $f(x)$ ，且 $\int_0^1 f_n(x)\mathrm{d}x\equiv \frac{1}{2}$ 也不收敛于

![](../../raw/pages_0033-0064/images/page_43_chart_15.jpg)

<details>
<summary>line</summary>

| X | Y |
| --- | --- |
| 0 | 0 |
| 1/2n | \(\alpha_n\) |
| 1/n | 0 |
| >1/n | 0 |
</details>

图13-4

例 1 说明当  $\{f_{n}(x)\}$  收敛于  $f(x)$  时, 一致收敛性是极限运算与积分运算交换的充分条件, 但不是必要条件.

定理13.11（可微性）设 $\{f_n\}$ 为定义在 $[a,b]$ 上的函数列，若 $x_0\in [a,b]$ 为 $\{f_n\}$ 的收敛点， $\{f_n\}$ 的每一项在 $[a,b]$ 上有连续的导数，且 $\{f'_n\}$ 在 $[a,b]$ 上一致收敛，则

$$
\frac {\mathrm{d}}{\mathrm{d} x} \left(\lim _ {n \to \infty} f _ {n} (x)\right) = \lim _ {n \to \infty} \frac {\mathrm{d}}{\mathrm{d} x} f _ {n} (x). \tag {4}
$$

36

---

§ 2 一致收敛函数列与函数项级数的性质

证 设 $f_{n}(x_{0}) \to A (n \to \infty), f_{n}^{\prime} \longrightarrow g (n \to \infty), x \in [a, b]$. 我们要证明函数列 $\{f_{n}\}$ 在区间 $[a, b]$ 上收敛，且其极限函数的导数存在且等于 $g$.

由定理条件,对任一 $x\in[a,b]$ ,总有

$$
f _ {n} (x) = f _ {n} (x _ {0}) + \int_ {x _ {0}} ^ {x} f _ {n} ^ {\prime} (t) \mathrm{d} t.
$$

当 $n\to \infty$ 时，右边第一项极限为 $A$ ，第二项极限为 $\int_{x_0}^x g(t)\mathrm{d}t$ （定理13.10），所以左边极限存在，记为 $f$ ，则有

$$
f (x) = \lim _ {n \to \infty} f _ {n} (x) = f (x _ {0}) + \int_ {x _ {0}} ^ {x} g (t) \mathrm{d} t,
$$

其中 $f(x_0) = A$ .由 $g$ 的连续性及微积分学基本定理(第九章 §5)推得

$$
f ^ {\prime} = g.
$$

这就证明了等式(4).

在定理 13.11 的条件下, 还可推出在  $[a, b]$  上  $f_{n} \longrightarrow f (n \to \infty)$ , 请读者自己证明.

由于函数的可微性是函数的局部性质,故以下推论成立.

推论 设函数列 $\{f_n\}$ 定义在区间 $I$ 上，若 $x_0 \in I$ 为 $\{f_n\}$ 的收敛点，且 $\{f_n'\}$ 在 $I$ 上内闭一致收敛，则 $f$ 在 $I$ 上可导，且 $f'(x) = \lim_{n \to \infty} f_n'(x)$.

例2 函数列

$$
f _ {n} (x) = \frac {1}{2 n} \ln (1 + n ^ {2} x ^ {2}), \quad n = 1, 2, \dots
$$

与

$$
f _ {n} ^ {\prime} (x) = \frac {n x}{1 + n ^ {2} x ^ {2}}, \quad n = 1, 2, \dots
$$

在 $[0,1]$ 上都收敛于0,由于

$$
\lim _ {n \to \infty} \max _ {x \in [ 0, 1 ]} \left| f _ {n} ^ {\prime} (x) - f ^ {\prime} (x) \right| = \frac {1}{2},
$$

所以导函数列 $\{f_{n}^{\prime}(x)\}$ 在 $[0,1]$ 上不一致收敛，但对任意 $\delta>0$ ，

$$
\sup _ {x \in [ \delta , 1 ]} \left| f _ {n} ^ {\prime} (x) - f ^ {\prime} (x) \right| \leqslant \frac {n}{1 + n ^ {2} \delta} \rightarrow 0 (n \rightarrow \infty),
$$

所以 $\{f_n'\}$ 在(0,1]上内闭一致收敛.由推论，在(0,1]上， $\lim_{n\to \infty}f_n'(x) = (\lim_{n\to \infty}f_n(x))'$ 仍成立.

事实上， $\lim_{n\to\infty}f_n'(x)=0,\quad\lim_{n\to\infty}f_n(x)=0,\quad\lim_{n\to\infty}f_n'(x)=(\lim_{n\to\infty}f_n(x))'$  在 $[0,1]$ 上都成立.

□

此例说明,一致收敛性是极限运算与求导运算交换的充分条件,而不是必要条件.

现在再来讨论定义在区间 $[a, b]$ 上函数项级数

$$
u _ {1} (x) + u _ {2} (x) + \dots + u _ {n} (x) + \dots \tag {5}
$$

的连续性、逐项求积与逐项求导的性质,这些性质可由函数列的相应性质推出.

定理13.12（连续性）若函数项级数 $\sum u_{n}(x)$ 在区间 $[a,b]$ 上一致收敛，且每一项都连续，则其和函数在 $[a,b]$ 上也连续.

37

---

第十三章 函数列与函数项级数

这个定理指出:在一致收敛条件下,(无限项)求和运算与求极限运算可以交换顺序,即

$$
\sum (\lim _ {x \to x _ {0}} u _ {n} (x)) = \lim _ {x \to x _ {0}} (\sum u _ {n} (x)). \tag {6}
$$

定理13.13(逐项求积) 若函数项级数  $\sum u_{n}(x)$  在  $[a, b]$  上一致收敛, 且每一项  $u_{n}(x)$  都连续, 则

$$
\sum \int_ {a} ^ {b} u _ {n} (x) \mathrm{d} x = \int_ {a} ^ {b} \sum u _ {n} (x) \mathrm{d} x. \tag {7}
$$

定理13.14（逐项求导） 若函数项级数 $\sum u_{n}(x)$ 在 $[a,b]$ 上每一项都有连续的导函数，$x_0 \in [a,b]$ 为 $\sum u_n(x)$ 的收敛点，且 $\sum u_n'(x)$ 在 $[a,b]$ 上一致收敛，则

$$
\sum \left(\frac {\mathrm{d}}{\mathrm{d} x} u _ {n} (x)\right) = \frac {\mathrm{d}}{\mathrm{d} x} (\sum u _ {n} (x)). \tag {8}
$$

定理 13.13 和定理 13.14 指出, 在一致收敛条件下, 逐项求积或求导后求和等于求和后再求积或求导.

最后,我们指出,本节中六个定理的意义不只是检验函数列或函数项级数是否满足关系式(2)—(4),(6)—(8),更重要的是根据定理的条件,即使没有求出极限函数或和函数,也能由函数列或函数项级数本身获得极限函数或和函数的解析性质.

例3 设

$$
u _ {n} (x) = \frac {1}{n ^ {3}} \ln \left(1 + n ^ {2} x ^ {2}\right), \quad n = 1, 2, \dots .
$$

证明函数项级数 $\sum u_{n}(x)$ 在[0,1]上一致收敛，并讨论其和函数在[0,1]上的连续性、可积性与可微性.

证 对每一个 $n$ ，易见 $u_{n}(x)$ 为[0,1]上增函数，故有

$$
u _ {n} (x) \leqslant u _ {n} (1) = \frac {1}{n ^ {3}} \mathrm{ln} (1 + n ^ {2}), \quad n = 1, 2, \dots .
$$

又当 $t \geqslant 1$ 时，有不等式 $\ln (1 + t^2) < t$ ，所以

$$
u _ {n} (x) \leqslant \frac {1}{n ^ {3}} \mathrm{ln} (1 + n ^ {2}) <   \frac {1}{n ^ {3}} \cdot n = \frac {1}{n ^ {2}}, \quad n = 1, 2, \dots .
$$

以收敛级数 $\sum \frac{1}{n^2}$ 为 $\sum u_n(x)$ 的优级数，推得 $\sum u_n(x)$ 在[0,1]上一致收敛.

由于每一个 $u_{n}(x)$ 在 $[0,1]$ 上连续，根据定理13.12与定理13.13，$\sum u_{n}(x)$ 的和函数 $S(x)$ 在 $[0,1]$ 上连续且可积。又由

$$
u _ {n} ^ {\prime} (x) = \frac {2 x}{n (1 + n ^ {2} x ^ {2})} = \frac {2 n x}{n ^ {2} (1 + n ^ {2} x ^ {2})} \leqslant \frac {1}{n ^ {2}}, \quad n = 1, 2, \dots ,
$$

即 $\sum \frac{1}{n^2}$ 也是 $\sum u_n'(x)$ 的优级数，故 $\sum u_n'(x)$ 也在[0,1]上一致收敛.由定理13.14，得$S(x)$ 在[0,1]上可微.

与函数列的情况相同,定理 13.12 和定理 13.14 中的一致收敛的条件可以减弱为内闭一致收敛.

38

---

§ 2 一致收敛函数列与函数项级数的性质

例 4 证明: 函数  $\zeta(x)=\sum_{n=1}^{\infty}\frac{1}{n^{x}}$  在  $(1,+\infty)$  上有连续的各阶导函数.

证 设 $u_{n}(x) = \frac{1}{n^{x}}$，则 $u_{n}^{(k)}(x) = (-1)^{k}\frac{\ln^{k}n}{n^{x}}, k = 1,2,\dots.$ 设 $[a,b] \subset (1, +\infty)$，对任意 $x \in [a,b]$，有

$$
\mid u _ {n} ^ {(k)} (x) \mid = \frac {\ln^ {k} n}{n ^ {x}} \leqslant \frac {\ln^ {k} n}{n ^ {a}}, \quad k = 1, 2, \dots .
$$

由于 $\lim_{n\to \infty}\frac{\ln^n n}{n^{(a - 1) / 2}} = 0$ ，因此对于充分大的 $n,\frac{\ln^n n}{n^{(a - 1) / 2}} < 1$ ，从而

$$
\frac {\ln^ {k} n}{n ^ {a}} = \frac {1}{n ^ {(a + 1) / 2}} \cdot \frac {\ln^ {k} n}{n ^ {(a - 1) / 2}} <   \frac {1}{n ^ {(a + 1) / 2}}.
$$

因为  $\sum_{n=1}^{\infty}\frac{1}{n^{(a+1)/2}}$  收敛，所以  $\sum_{n=1}^{\infty}u_{n}^{(k)}(x)$  在  $[a,b]$  上一致收敛，于是  $\sum_{n=1}^{\infty}u_{n}^{(k)}(x)$  在  $(1,+\infty)$  上内闭一致收敛。对  $\sum_{n=1}^{\infty}(-1)^{k}\frac{\ln^{k}n}{n^{x}}$  用定理 13.12 和定理 13.14， $\zeta(x)$  在  $(1,+\infty)$  上有连续的各阶导函数，且  $\zeta^{(k)}(x)=\sum_{n=1}^{\infty}(-1)^{k}\frac{\ln^{k}n}{n^{x}}, k=1,2,\cdots.$

## 习题 13.2

1. 讨论下列各函数列 $\{f_n\}$ 在所定义的区间上:

(a)  $\{f_{n}\}$  与  $\{f_{n}^{\prime}\}$  的一致收敛性；
(b) $\{f_n\}$ 是否有定理13.9, 13.10, 13.11的条件与结论.
(1) $f_{n}(x)=\frac{2x+n}{x+n},x\in[0,b]$; (2) $f_{n}(x)=x-\frac{x^{n}}{n},x\in[0,1]$;
(3) $f_{n}(x)=nx\mathrm{e}^{-nx^{2}},x\in[0,1].$

2. 证明: 若函数列  $\{f_{n}\}$  在  $[a, b]$  上满足定理 13.11 的条件, 则  $\{f_{n}\}$  在  $[a, b]$  上一致收敛.

3. 证明定理13.12和定理13.14.

4. 设 $S(x) = \sum_{n=1}^{\infty} \frac{x^{n-1}}{n^2}, x \in [-1, 1]$, 计算积分 $\int_0^x S(t) \, \mathrm{d}t$.

5. 设 $S(x) = \sum_{n=1}^{\infty} \frac{\cos nx}{n\sqrt{n}}, x \in (-\infty, +\infty)$, 计算积分 $\int_{0}^{x} S(t) \, \mathrm{d}t$.

6. 设 $S(x) = \sum_{n=1}^{\infty} n \mathrm{e}^{-nx}, x > 0$，计算 $\int_{\ln 2}^{\ln 3} S(t) \, \mathrm{d}t$.

7. 证明: 函数 $f(x) = \sum \frac{\sin nx}{n^3}$ 在 $(- \infty, +\infty)$ 上连续, 且有连续的导函数.

8. 证明:定义在 $[0, 2\pi]$ 上的函数项级数 $\sum_{n=0}^{\infty} r^n \cos nx$ ($0 < r < 1$) 满足定理 13.13 条件，且 $\int_0^{2\pi} \left( \sum_{n=0}^{\infty} r^n \cos nx \right) \mathrm{d}x = 2\pi$.

9. 讨论下列函数列在所定义区间上的一致收敛性及极限函数的连续性、可微性和可积性:

39

---

第十三章 函数列与函数项级数

(1)  $f_{n}(x) = x e^{-nx^{2}}, n = 1, 2, \cdots, x \in [-l, l]$ ;
(2)  $f_{n}(x)=\frac{nx}{nx+1}$ ,  $n=1,2,\cdots$ , (i)  $x\in[0,+\infty)$ , (ii)  $x\in[a,+\infty)$  (a>0).

10. 设 $f$ 在 $(- \infty, +\infty)$ 上有任意阶导数，记 $F_{n} = f^{(n)}$ ，且在任何有限区间内

$$
F _ {n} \longrightarrow \varphi (n \to \infty),
$$

试证 $\varphi (x) = ce^{x}$ （ $c$ 为常数）.

## 第十三章总练习题

1. 试问 $k$ 为何值时，下列函数列 $\{f_n\}$ 一致收敛:

(1) $f_{n}(x)=xn^{k}e^{-nx},0\leqslant x<+\infty;$

(2) $f_{n}(x)=\left\{\begin{aligned}&xn^{k},&0\leqslant x\leqslant\frac{1}{n},\\ &\left(\frac{2}{n}-x\right)n^{k},&\frac{1}{n}<x\leqslant\frac{2}{n},\\ &0,&\frac{2}{n}<x\leqslant1.\end{aligned}\right.$

2. 证明:(1) 若 $f_{n}(x) \longrightarrow f(x) (n \to \infty), x \in I$，且 $f$ 在 $I$ 上有界，则 $\{f_{n}\}$ 至多除有限项外在 $I$ 上是一致有界的；
(2) 若  $f_{n}(x) \longrightarrow f(x) (n \to \infty)$ ,  $x \in I$ , 且对每个正整数 n,  $f_{n}$  在 I 上有界, 则  $\{f_{n}\}$  在 I 上一致有界.
3. 设 $f$ 为 $\left[\frac{1}{2}, 1\right]$ 上的连续函数. 证明:

(1) $\{x^n f(x)\}$ 在 $\left[\frac{1}{2}, 1\right]$ 上收敛；
(2) $\{x^n f(x)\}$ 在 $\left[\frac{1}{2}, 1\right]$ 上一致收敛的充要条件是 $f(1) = 0$.

4. 若把定理13.10中一致收敛函数列 $\{f_n\}$ 的每一项在 $[a, b]$ 上连续改为在 $[a, b]$ 上可积，试证 $\{f_n\}$ 在 $[a, b]$ 上的极限函数在 $[a, b]$ 上也可积.

5. 设级数 $\sum a_{n}$ 收敛. 证明

$$
\lim _ {x \to 0 ^ {+}} \sum \frac {a _ {n}}{n ^ {x}} = \sum a _ {n}.
$$

6. 设可微函数列 $\{f_n\}$ 在 $[a, b]$ 上收敛，$\{f_n'\}$ 在 $[a, b]$ 上一致有界。证明:$\{f_n\}$ 在 $[a, b]$ 上一致收敛。
7. 设连续函数列 $\{f_n(x)\}$ 在 $[a, b]$ 上一致收敛于 $f(x)$，而 $g(x)$ 在 $(- \infty, +\infty)$ 上连续。证明:$\{g(f_n(x))\}$ 在 $[a, b]$ 上一致收敛于 $g(f(x))$。

![](../../raw/pages_0033-0064/images/page_47_image_24.jpg)

## 第十三章综合自测题

40
