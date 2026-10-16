$$
\lim _ {n \to \infty} a _ {n} = a ^ {①}, \text {或} a _ {n} \to a (n \to \infty),
$$

读作“当 $n$ 趋于无穷大时，$\{a_{n}\}$ 的极限等于 $a$ 或 $a_{n}$ 趋于 $a$”.

若数列 $\{a_{n}\}$ 没有极限, 则称 $\{a_{n}\}$ 不收敛, 或称 $\{a_{n}\}$ 为发散数列.

定义1常称为数列极限的 $\varepsilon -N$ 定义.下面举例说明如何根据 $\varepsilon -N$ 定义来验证数列极限.

例 2 证明  $\lim_{n\to\infty}\frac{1}{n^{\alpha}}=0$  , 这里  $\alpha$  为正数.

证 由于

$$
\left| \frac {1}{n ^ {\alpha}} - 0 \right| = \frac {1}{n ^ {\alpha}},
$$

故对任给的 $\varepsilon > 0$，只要取 $N = \left[\frac{1}{\mathcal{E}^{\frac{1}{\alpha}}}\right] + 1$，则当 $n > N$ 时，便有

$$
\frac {1}{n ^ {\alpha}} <   \frac {1}{N ^ {\alpha}} <   \varepsilon , \quad \text {即} \left| \frac {1}{n ^ {\alpha}} - 0 \right| <   \varepsilon .
$$

这就证明了  $\lim_{n\to\infty}\frac{1}{n^{\alpha}}=0.$

□

例3 证明

$$
\lim _ {n \to \infty} \frac {3 n ^ {2}}{n ^ {2} - 3} = 3.
$$

分析 由于

$$
\left| \frac {3 n ^ {2}}{n ^ {2} - 3} - 3 \right| = \frac {9}{n ^ {2} - 3} \leqslant \frac {9}{n} \quad (n \geqslant 3). \tag {1}
$$

因此,对任给的  $\varepsilon>0$ , 只要  $\frac{9}{n}<\varepsilon$ , 便有

$$
\left| \frac {3 n ^ {2}}{n ^ {2} - 3} - 3 \right| <   \varepsilon , \tag {2}
$$

即当 $n > \frac{9}{\varepsilon}$ 时，(2)式成立.又由于(1)式是在 $n\geqslant 3$ 的条件下成立的，故应取

$$
N = \max \left\{3, \frac {9}{\varepsilon} \right\}. \tag {3}
$$

证 任给 $\varepsilon > 0$，取 $N = \max \left\{3, \frac{9}{\varepsilon}\right\}$. 据分析，当 $n > N$ 时（2）式成立. 于是本题得证. □

注 本例在求 N 的过程中, (1) 式中运用了适当放大的方法, 这样求 N 就比较方便. 但应注意这种放大必须“适当”, 以根据给定的  $\varepsilon$  能确定出 N. 又 (3) 式给出的 N 不一定是正整数. 一般地, 在定义 1 中 N 不一定限于正整数, 而只要它是正数即可.

例 4 证明  $\lim_{n\to\infty}q^{n}=0$  , 这里  $|q|<1$ .

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 记号 $\lim$ 是拉丁文 limes(极限) 一词的前三个字母. 由于 $n$ 限于取正整数, 所以在表示数列极限的记号中把 $n \to +\infty$ 简单地写作 $n \to \infty$.</span></small>

证 若 $q = 0$ ，则结果是显然的.现设 $0 < |q| < 1.$ 记 $h = \frac{1}{|q|} - 1$ ，则 $h > 0.$ 我们有

$$
\mid q ^ {n} - 0 \mid = \mid q \mid^ {n} = \frac {1}{(1 + h) ^ {n}},
$$

并由 $(1 + h)^n\geqslant 1 + nh$ 得到

$$
\mid q \mid^ {n} \leqslant \frac {1}{1 + n h} <   \frac {1}{n h}. \tag {4}
$$

对任给的 $\varepsilon > 0$，只要取 $N = \frac{1}{\varepsilon h}$，则当 $n > N$ 时，由（4）式得 $|q^n - 0| < \varepsilon$。这就证明了 $\lim_{n \to \infty} q^n = 0$。

当  $q=\frac{1}{2}$  时, 就是前面例 1 的结果.

注 本例还可利用对数函数 $y = \lg x$ 的严格增性来证明（见第一章 §4 例6的注及(2)式），简述如下:

对任给的 $\varepsilon > 0$ （不妨设 $\varepsilon < 1$），为使 $|q^n - 0| = |q|^n < \varepsilon$，只要

$n\lg|q|<\lg\varepsilon$ ，即 $n>\frac{\lg\varepsilon}{\lg|q|}$ （这里也假定 $0<|q|<1$ ）.

于是, 只要取  $N=\frac{\lg \varepsilon}{\lg |q|}$  即可.

例 5 证明  $\lim_{n\to\infty}\sqrt[n]{a}=1$  , 其中 a>0.

证 当 $a = 1$ 时, 结论显然成立. 现设 $a > 1$. 记 $\alpha_{n} = a^{\frac{1}{n}} - 1$, 则 $\alpha_{n} > 0$. 由

$$
a = (1 + \alpha_ {n}) ^ {n} \geqslant 1 + n \alpha_ {n} = 1 + n (a ^ {\frac {1}{n}} - 1),
$$

得

$$
a ^ {\frac {1}{n}} - 1 \leqslant \frac {a - 1}{n}. \tag {5}
$$

任给 $\varepsilon > 0$，由（5）式可见，当 $n > \frac{a - 1}{\varepsilon} = N$ 时，就有 $a^{\frac{1}{n}} - 1 < \varepsilon$，即 $|a^{\frac{1}{n}} - 1| < \varepsilon$. 所以 $\lim_{n \to \infty} \sqrt[n]{a} = 1$. 对于 $0 < a < 1$ 的情形，其证明留给读者. □

例 6 证明  $\lim_{n\to\infty}\frac{a^{n}}{n!}=0.$

证 若 $a = 0$ ，结论是显然的，现设 $a \neq 0, k = [|a|] + 1$ ，有

$$
\left| \frac {a ^ {n}}{n !} - 0 \right| = \frac {| a | ^ {n}}{n !} = \frac {| a | \cdot | a | \cdot \cdots \cdot | a | \cdot \cdots \cdot | a |}{1 \cdot 2 \cdot \cdots \cdot k \cdot \cdots \cdot n} \leqslant K \frac {| a |}{n},
$$

其中 $K = \frac{|a| \cdot |a| \cdot \dots \cdot |a|}{1 \cdot 2 \cdot \dots \cdot k}$. 所以对于任给的 $\varepsilon > 0$, 取 $N = \max \left\{k, \frac{K|a|}{\varepsilon}\right\}$, 只要 $n > N$, 就有

$$
\left| \frac {a ^ {n}}{n !} - 0 \right| \leqslant K \frac {| a |}{n} <   \varepsilon ,
$$

这就证明了 $\lim_{n\to \infty}\frac{a^n}{n!} = 0.$

关于数列极限的  $\varepsilon-N$  定义,通过以上几个例子,读者已有了初步的认识.对此还应着重注意下面几点:

1. $\varepsilon$ 的任意性 定义1中正数 $\varepsilon$ 的作用在于衡量数列通项 $a_{n}$ 与定数 $a$ 的接近程度, $\varepsilon$ 愈小, 表示接近得愈好; 而正数 $\varepsilon$ 可以任意地小, 说明 $a_{n}$ 与 $a$ 可以接近到任何程度. 然而, 尽管 $\varepsilon$ 有其任意性, 但一经给出, 就暂时被确定下来, 以便依靠它来求出 $N$. 又 $\varepsilon$ 既是任意小的正数, 那么 $\frac{\varepsilon}{2}, 3\varepsilon$ 或 $\varepsilon^{2}$ 等同样也是任意小的正数, 因此定义1中不等式 $|a_{n} - a| < \varepsilon$ 中的 $\varepsilon$ 可用 $\frac{\varepsilon}{2}, 3\varepsilon$ 或 $\varepsilon^{2}$ 等来代替. 同时, 正由于 $\varepsilon$ 是任意小正数, 我们可限定 $\varepsilon$ 小于一个确定的正数 (如在例4的注给出的证明方法中限定 $\varepsilon < 1$). 另外, 定义1中的 $|a_{n} - a| < \varepsilon$ 也可改写成 $|a_{n} - a| \leqslant \varepsilon$.

2. $N$ 的相应性 一般说, $N$ 随 $\varepsilon$ 的变小而变大, 由此常把 $N$ 写作 $N(\varepsilon)$, 来强调 $N$ 是依赖于 $\varepsilon$ 的, 但这并不意味着 $N$ 是由 $\varepsilon$ 所唯一确定的. 因为对给定的 $\varepsilon$, 比如当 $N = 100$ 时, 能使得当 $n > N$ 时有 $\left|a_{n} - a\right| < \varepsilon$, 则 $N = 101$ 或更大时此不等式自然也成立. 这里重要的是 $N$ 的存在性, 而不在于它的值的大小. 另外, 定义 1 中的 $n > N$ 也可改写成 $n \geqslant N$.

3. 从几何意义上看，“当 $n > N$ 时有 $\left|a_{n} - a\right| < \varepsilon$”意味着:所有下标大于 $N$ 的项 $a_{n}$ 都落在邻域 $U(a;\varepsilon)$ 内；而在 $U(a;\varepsilon)$ 之外，数列 $\{a_n\}$ 中的项至多只有 $N$ 个（有限个）。反之，任给 $\varepsilon > 0$ ，若在 $U(a;\varepsilon)$ 之外数列 $\{a_{n}\}$ 中的项只有有限个，设这有限个项的最大下标为 $N$ ，则当 $n > N$ 时有 $a_{n} \in U(a;\varepsilon)$，即当 $n > N$ 时有 $\left|a_{n} - a\right| < \varepsilon$。由此，我们可写出数列极限的一种等价定义如下。

定义 1' 任给  $\varepsilon>0$ ，若在  $U(a;\varepsilon)$  之外数列  $\{a_{n}\}$  中的项至多只有有限个，则称数列  $\{a_{n}\}$  收敛于极限 a.

由定义 $1'$ 可知, 若存在某 $\varepsilon_0 > 0$, 使得数列 $\{a_n\}$ 中有无穷多个项落在 $U(a; \varepsilon_0)$ 之外, 则 $\{a_n\}$ 一定不以 $a$ 为极限.

例 7 证明  $\{n^{2}\}$  和  $\{(-1)^{n}\}$  都是发散数列.

证 对任何 $a \in \mathbb{R}$, 取 $\varepsilon_0 = 1$, 则数列 $\{n^2\}$ 中所有满足 $n > a + 1$ 的项 (有无穷多个) 显然都落在 $U(a; \varepsilon_0)$ 之外, 故 $\{n^2\}$ 不以任何数 $a$ 为极限, 即 $\{n^2\}$ 为发散数列.

至于数列 $\{(-1)^n\}$, 当 $a = 1$ 时取 $\varepsilon_0 = 1$, 则在 $U(a; \varepsilon_0)$ 之外有 $\{(-1)^n\}$ 中的所有奇数项; 当 $a \neq 1$ 时取 $\varepsilon_0 = \frac{1}{2} |a - 1|$, 则在 $U(a; \varepsilon_0)$ 之外有 $\{(-1)^n\}$ 中的所有偶数项. 所以 $\{(-1)^n\}$ 不以任何数 $a$ 为极限, 即 $\{(-1)^n\}$ 为发散数列.

例8 设 $\lim_{n\to \infty}x_n = a, \lim_{n\to \infty}y_n = b.$ 作数列 $\{z_n\}$ 为

$$
x _ {1}, y _ {1}, x _ {2}, y _ {2}, \dots , x _ {n}, y _ {n}, \dots .
$$

求证: 数列  $\{z_{n}\}$  收敛的充分必要条件是 a=b.

证 充分性 因为 $a = b$，即 $\lim_{n\to \infty}x_n = \lim_{n\to \infty}y_n = a$，所以对于任给的 $\varepsilon > 0$，数列 $\{x_n\}$ 和 $\{y_n\}$ 落在 $U(a; \varepsilon)$ 之外的项至多只有有限个，从而数列 $\{z_n\}$ 落在 $U(a; \varepsilon)$ 之外的项至多

只有有限个。由定义 $1'$，证得 $\lim_{n\to \infty}z_n = a$.

必要性 设 $\lim_{n\to \infty}z_n = A$。那么对于任给的 $\varepsilon > 0$，数列 $\{z_n\}$ 落在 $U(A; \varepsilon)$ 之外的项至多只有有限个，从而数列 $\{x_n\}$ 和 $\{y_n\}$ 落在 $U(A; \varepsilon)$ 之外的项也至多只有有限个。由定义 $1'$，证得

$$
a = \lim _ {n \to \infty} x _ {n} = A = \lim _ {n \to \infty} y _ {n} = b.
$$

例9 设 $\{a_{n}\}$ 为给定的数列，$\{b_{n}\}$ 为对 $\{a_{n}\}$ 增加、减少或改变有限项之后得到的数列. 证明:数列 $\{b_{n}\}$ 与 $\{a_{n}\}$ 同时收敛或发散，且在收敛时两者的极限相等.

证 设 $\{a_{n}\}$ 为收敛数列，且 $\lim_{n\to \infty}a_n = a.$ 按定义 $1'$，对任给的 $\varepsilon >0$，数列 $\{a_{n}\}$ 中落在 $U(a;\varepsilon)$ 之外的项至多只有有限个.而数列 $\{b_n\}$ 是对 $\{a_{n}\}$ 增加、减少或改变有限项之后得到的，故从某一项开始，$\{b_n\}$ 中的每一项都是 $\{a_{n}\}$ 中确定的一项，所以 $\{b_{n}\}$ 中落在 $U(a;\varepsilon)$ 之外的项也至多只有有限个.这就证得 $\lim_{n\to \infty}b_n = a.$

现设 $\{a_{n}\}$ 发散.倘若 $\{b_{n}\}$ 收敛,则因 $\{a_{n}\}$ 可看成是对 $\{b_{n}\}$ 增加、减少或改变有限项之后得到的数列,故由刚才所证,$\{a_{n}\}$ 收敛,矛盾.所以当 $\{a_{n}\}$ 发散时 $\{b_{n}\}$ 也发散.

在所有收敛数列中,有一类重要的数列,称为无穷小数列,其定义如下.

定义 2 若  $\lim_{n\to\infty}a_{n}=0$ ，则称  $\{a_{n}\}$  为无穷小数列.

前面例 1,2,4,6 中的数列都是无穷小数列.由无穷小数列的定义,读者不难证明如下定理.

定理2.1 数列 $\{a_{n}\}$ 收敛于 $a$ 的充要条件是: $\{a_n - a\}$ 为无穷小数列.

最后我们介绍一下无穷大数列的概念.

定义 3 若数列  $\{a_{n}\}$  满足: 对任意正数 M>0, 总存在正整数 N, 使得当 n>N 时, 有

$$
\mid a _ {n} \mid > M,
$$

则称数列 $\{a_{n}\}$ 发散于无穷大，并记作

$$
\lim _ {n \to \infty} a _ {n} = \infty , \text {或} a _ {n} \to \infty .
$$

注 若 $\lim_{n\to \infty}a_n = \infty$ ，则称 $\{a_n\}$ 是一个无穷大数列或无穷大量.

定义 4 若数列  $\{a_{n}\}$  满足: 对任意正数 M>0, 存在正整数 N, 使得当 n>N 时, 有

$$
a _ {n} > M \quad (  a _ {n} <   - M  ) ,
$$

则称数列 $\{a_{n}\}$ 发散于正(负)无穷大,并记作

$$
\lim _ {n \to \infty} a _ {n} = + \infty , \text {或} a _ {n} \to + \infty \quad (\lim _ {n \to \infty} a _ {n} = - \infty , \text {或} a _ {n} \to - \infty).
$$

例如数列 $\{n\}, \left\{(-1)^n \frac{n^2 + 1}{n}\right\}$ 均是无穷大量；而数列 $\{[1 + (-1)^n]n\}$ 虽然是无界数列，但却不是无穷大量.

## 习题 2.1

1. 设  $a_{n}=\frac{1+(-1)^{n}}{n},\quad n=1,2,\cdots,a=0.$

(1) 对下列  $\varepsilon$  分别求出极限定义中相应的 N:

$$
\varepsilon_ {1} = 0. 1, \quad \varepsilon_ {2} = 0. 0 1, \quad \varepsilon_ {3} = 0. 0 0 1;
$$

(2) 对  $\varepsilon_{1}, \varepsilon_{2}, \varepsilon_{3}$  可找到相应的 N，这是否证明了  $a_{n}$  趋于 0？应该怎样做才对；
(3) 对给定的  $\varepsilon$  是否只能找到一个 N?

2. 按 $\varepsilon - N$ 定义证明:

(1)  $\lim_{n\to\infty}\frac{n}{n+1}=1;$

(2)  $\lim_{n\to\infty}\frac{3n^{2}+n}{2n^{2}-1}=\frac{3}{2}$ ;

(3)  $\lim_{n\to\infty}\frac{n!}{n^{n}}=0;$

(4)  $\lim_{n\to\infty}\sin\frac{\pi}{n}=0;$

(5) $\lim_{n\to \infty}\frac{n}{a^n} = 0$ ( $a > 1$ ).

3. 根据例 2, 例 4 和例 5 的结果求出下列极限, 并指出哪些是无穷小数列:

(1)  $\lim_{n\to\infty}\frac{1}{\sqrt{n}}$ ;

(2) $\lim_{n\to \infty}\sqrt[n]{3}$;

(3) $\lim_{n\to \infty}\frac{1}{n^3};$

(4)  $\lim_{n\to\infty}\frac{1}{3^{n}}$ ;

(5) $\lim_{n\to \infty}\frac{1}{\sqrt{2^n}};$

(6)  $\lim_{n\to\infty}\sqrt[n]{10}$ ;

(7)  $\lim_{n\to\infty}\frac{1}{\sqrt[n]{2}}.$

4. 证明: 若 $\lim_{n\to \infty}a_n = a$，则对任一正整数 $k$，有 $\lim_{n\to \infty}a_{n+k} = a$.

5. 试用定义 1' 证明:

(1) 数列  $\left\{\frac{1}{n}\right\}$  不以 1 为极限；(2) 数列  $\left\{n^{(-1)^{n}}\right\}$  发散.

6. 证明定理2.1，并应用它证明数列 $\left\{1 + \frac{(-1)^n}{n}\right\}$ 的极限是1.

7. 在下列数列中哪些数列是有界数列、无界数列以及无穷大数列:

(1) $\{[1 + (-1)^n]\sqrt{n}\}; (2)\{\sin n\}; (3)\left\{\frac{n^2}{n - \sqrt{5}}\right\}; (4)\{2^{(-1)^n n}\}$.

8. 证明: 若 $\lim_{n\to \infty}a_n = a$, 则 $\lim_{n\to \infty}|a_n| = |a|$. 当且仅当 $a$ 为何值时反之也成立?

9. 按 $\varepsilon - N$ 定义证明:

(1)  $\lim_{n\to\infty}(\sqrt{n+1}-\sqrt{n})=0;$

(2)  $\lim_{n\to\infty}\frac{1+2+3+\cdots+n}{n^{3}}=0;$

(3)  $\lim_{n\to\infty}a_{n}=1$ , 其中

$$
a _ {n} = \left\{ \begin{array}{l l} \frac {n - 1}{n}, & n \text {为偶数,} \\ \frac {\sqrt {n ^ {2} + n}}{n}, & n \text {为奇数.} \end{array} \right.
$$

10. 设 $a_{n} \neq 0$. 证明: $\lim_{n \to \infty} a_{n} = 0$ 的充要条件是 $\lim_{n \to \infty} \frac{1}{a_{n}} = \infty$.

## § 2 收敛数列的性质

收敛数列有如下一些重要性质.

定理 2.2(唯一性) 若数列  $\{a_{n}\}$  收敛, 则它只有一个极限.

证 设 $a$ 是 $\{a_{n}\}$ 的一个极限. 我们证明: 对任何数 $b \neq a, b$ 不是 $\{a_{n}\}$ 的极限. 事实上, 若取  $\varepsilon_{0}=\frac{1}{2}|b-a|$ , 则按定义  $1'$ , 在  $U(a;\varepsilon_{0})$  之外至多只有  $\{a_{n}\}$  中有限个项, 从而在  $U(b;\varepsilon_{0})$  内至多只有  $\{a_{n}\}$  中有限个项, 所以 b 不是  $\{a_{n}\}$  的极限. 这就证明了收敛数列只能有一个极限. □

一个收敛数列一般含有无穷多个数,而它的极限只是一个数.我们单凭这一个数就能精确地估计出几乎全体项的大小.以下收敛数列的一些性质,大都基于这一事实.

定理 2.3(有界性) 若数列  $\{a_{n}\}$  收敛, 则  $\{a_{n}\}$  为有界数列, 即存在正数 M, 使得对一切正整数 n, 都有

$$
\mid a _ {n} \mid \leqslant M.
$$

证 设 $\lim_{n\to \infty}a_n = a.$ 取 $\varepsilon = 1$ ，存在正数 $N$ ，对一切 $n > N$ ，有

$$
\mid a _ {n} - a \mid <   1, \text {即} \quad a - 1 <   a _ {n} <   a + 1.
$$

记

$$
M = \max \left\{\mid a _ {1} \mid , \mid a _ {2} \mid , \dots , \mid a _ {N} \mid , \mid a - 1 \mid , \mid a + 1 \mid \right\},
$$

则对一切正整数 $n$ ，都有 $\mid a_n\mid \leqslant M.$

注 有界性只是数列收敛的必要条件,而非充分条件.例如数列 $\{(-1)^{n}\}$ 有界,但它并不收敛(见§1例7).

定理2.4（保号性）若 $\lim_{n\to \infty}a_n = a > 0$ （或 $<  0$ ，则对任何 $a^\prime \in (0,a)$ （或 $a^{\prime}\in (a,0)$ ），存在正数 $N$ ，使得当 $n > N$ 时，有 $a_{n} > a^{\prime}$ （或 $a_{n} <   a^{\prime}$ ）.

证 设 a>0. 取  $\varepsilon=a-a'(>0)$ ，则存在正数 N，使得当 n>N 时，有  $a_{n}>a-\varepsilon=a'$ ，这就证得结果。对于 a<0 的情形，也可类似地证明。

注 在应用保号性时,经常取  $a'=\frac{a}{2}$ .

推论 设 $\lim_{n\to \infty}a_n = a,\lim_{n\to \infty}b_n = b,a <   b$ ，则存在 $N$ ，使得当 $n > N$ 时，有

$$
a _ {n} <   b _ {n}.
$$

证 因为 $\lim_{n\to \infty}a_n = a,\lim_{n\to \infty}b_n = b,a <   \frac{a + b}{2} <  b$ ，所以由保号性，存在 $N_{1}$ ，当 $n > N_{1}$ 时，有

$$
a _ {n} <   \frac {a + b}{2};
$$

存在 $N_{2}$ ，当 $n > N_{2}$ 时，有

$$
b _ {n} > \frac {a + b}{2}.
$$

取 $N = \max \{N_{1}, N_{2}\}$, 那么当 $n > N$ 时, 有

$$
a _ {n} <   b _ {n}.
$$

定理2.5（保不等式性）设 $\{a_{n}\}$ 与 $\{b_n\}$ 均为收敛数列.若存在正数 $N_0$ ，使得当$n > N_0$ 时，有 $a_{n}\leqslant b_{n}$ ，则 $\lim_{n\to \infty}a_n\leqslant \lim_{n\to \infty}b_n$

证 设 $\lim_{n\to \infty}a_n = a, \lim_{n\to \infty}b_n = b.$ 任给 $\varepsilon >0$ ，分别存在正数 $N_{1}$ 与 $N_{2}$ ，使得当 $n > N_{1}$ 时，有

$$
a - \varepsilon <   a _ {n}, \tag {1}
$$

当 $n > N_{2}$ 时，有

$$
b _ {n} <   b + \varepsilon . \tag {2}
$$

取 $N = \max \{N_0,N_1,N_2\}$ ，则当 $n > N$ 时，按假设及不等式(1)和(2)，有

$$
a - \varepsilon <   a _ {n} \leqslant b _ {n} <   b + \varepsilon ,
$$

由此得到 $a < b + 2\varepsilon$. 由 $\varepsilon$ 的任意性推得 $a \leqslant b$ (参见第一章 §1 例 2), 即 $\lim_{n \to \infty} a_n \leqslant \lim_{n \to \infty} b_n$. □

请读者自行思考:如果把定理2.5中的条件 $a_{n}\leqslant b_{n}$ 换成严格不等式 $a_{n}<b_{n}$ ，那么能否把结论换成 $\lim_{n\to\infty}a_{n}<\lim_{n\to\infty}b_{n}$ ?

例 1 设  $a_{n} \geqslant 0 (n = 1, 2, \cdots)$ . 证明: 若  $\lim_{n \to \infty} a_{n} = a$ , 则

$$
\lim _ {n \to \infty} \sqrt {a _ {n}} = \sqrt {a}. \tag {3}
$$

证 由定理2.5可得 $a \geqslant 0$.

若 $a = 0$ ，则由 $\lim_{n\to \infty}a_n = 0$ ，任给 $\varepsilon >0$ ，存在正数 $N$ ，使得当 $n > N$ 时，有 $a_{n} <   \varepsilon^{2}$ ，从而$\sqrt{a_n} <  \varepsilon$ ，即 $|\sqrt{a_n} -0| <   \varepsilon$ ，故有 $\lim_{n\to \infty}\sqrt{a_n} = 0.$

若 a>0 , 则有

$$
\mid \sqrt {a _ {n}} - \sqrt {a} \mid = \frac {\mid a _ {n} - a \mid}{\sqrt {a _ {n}} + \sqrt {a}} \leqslant \frac {\mid a _ {n} - a \mid}{\sqrt {a}}.
$$

任给 $\varepsilon > 0$，由 $\lim_{n \to \infty} a_n = a$，存在正数 $N$，使得当 $n > N$ 时，有

$$
\mid a _ {n} - a \mid <   \sqrt {a} \varepsilon ,
$$

从而 $|\sqrt{a_n} -\sqrt{a}| <   \varepsilon .(3)$ 式得证.

定理 2.6(迫敛性) 设收敛数列  $\{a_{n}\}, \{b_{n}\}$  都以 a 为极限, 数列  $\{c_{n}\}$  满足: 存在正数  $N_{0}$ , 当  $n > N_{0}$  时, 有

$$
a _ {n} \leqslant c _ {n} \leqslant b _ {n}, \tag {4}
$$

则数列  $\{c_{n}\}$  收敛, 且  $\lim_{n\to\infty}c_{n}=a$ .

证 任给 $\varepsilon > 0$，由 $\lim_{n \to \infty} a_n = \lim_{n \to \infty} b_n = a$，分别存在正数 $N_1$ 与 $N_2$，使得当 $n > N_1$ 时，有

$$
a - \varepsilon <   a _ {n}; \tag {5}
$$

当 $n > N_{2}$ 时，有

$$
b _ {n} <   a + \varepsilon . \tag {6}
$$

取  $N=\max\left\{N_{0},N_{1},N_{2}\right\}$ ，则当 n>N 时，不等式(4)、(5)、(6)同时成立，即有

$$
a - \varepsilon <   a _ {n} \leqslant c _ {n} \leqslant b _ {n} <   a + \varepsilon.
$$

从而有 $|c_n - a| < \varepsilon$，这就证得所要的结果.

定理 2.6 不仅给出了判定数列收敛的一种方法,而且提供了一个求极限的工具.

例 2 求数列  $\{\sqrt[n]{n}\}$  的极限.

解 记 $a_{n} = \sqrt[n]{n} = 1 + h_{n}$ ，这里 $h_n > 0 (n > 1)$ ，则有

$$
n = (1 + h _ {n}) ^ {n} > \frac {n (n - 1)}{2} h _ {n} ^ {2}.
$$

由上式得 $0 < h_{n} < \sqrt{\frac{2}{n - 1}} (n > 1)$，从而有

$$
1 \leqslant a _ {n} = 1 + h _ {n} <   1 + \sqrt {\frac {2}{n - 1}}. \tag {7}
$$

数列 $\left\{1 + \sqrt{\frac{2}{n - 1}}\right\}$ 是收敛于1的，因对任给的 $\varepsilon >0$ ，取 $N = 1 + \frac{2}{\varepsilon^2}$ ，则当 $n > N$ 时，有$\left|1 + \sqrt{\frac{2}{n - 1}} -1\right| <   \varepsilon .$ 于是，不等式(7)的左右两边的极限皆为1，故由迫敛性证得 $\lim_{n\to \infty}\sqrt[n]{n} = 1.$

例3 求证: $\lim_{n\to \infty}\frac{1}{\sqrt[n]{n!}} = 0.$

证 对于任给的正数 $\varepsilon$ ，因为 $\lim_{n\to \infty}\frac{\left(\frac{1}{\varepsilon}\right)^n}{n!} = 0$ （本章 §1 例6），所以由极限的保号性定理及推论，存在 $N, n > N$ 时，

$$
\frac {\frac {1}{\varepsilon^ {n}}}{n !} <   1,
$$

从而 $\frac{1}{\sqrt[n]{n!}} < \varepsilon$，即 $\lim_{n\to \infty}\frac{1}{\sqrt[n]{n!}} = 0.$

□

在求数列极限时,常需要使用极限的四则运算法则.

定理2.7（四则运算法则） 若 $\{a_{n}\}$ 与 $\{b_{n}\}$ 为收敛数列，则 $\{a_{n} + b_{n}\},\{a_{n} - b_{n}\}$，$\{a_{n} \cdot b_{n}\}$ 也都是收敛数列，且有

$$
\lim _ {n \to \infty} (a _ {n} \pm b _ {n}) = \lim _ {n \to \infty} a _ {n} \pm \lim _ {n \to \infty} b _ {n},
$$

$$
\lim _ {n \to \infty} (a _ {n} \cdot b _ {n}) = \lim _ {n \to \infty} a _ {n} \cdot \lim _ {n \to \infty} b _ {n}.
$$

特别当 $b_{n}$ 为常数 $c$ 时，有

$$
\lim _ {n \to \infty} (a _ {n} + c) = \lim _ {n \to \infty} a _ {n} + c, \lim _ {n \to \infty} c a _ {n} = c \lim _ {n \to \infty} a _ {n}.
$$

若再假设 $b_{n} \neq 0$ 及 $\lim_{n\to \infty}b_n\neq 0$ ，则 $\left\{\frac{a_n}{b_n}\right\}$ 也是收敛数列，且有

$$
\lim _ {n \to \infty} \frac {a _ {n}}{b _ {n}} = \lim _ {n \to \infty} a _ {n} / \lim _ {n \to \infty} b _ {n}.
$$

证 由于 $a_{n} - b_{n} = a_{n} + (-1)b_{n}$ 及 $\frac{a_n}{b_n} = a_n\cdot \frac{1}{b_n}$，因此我们只需证明关于和、积与倒数运算的结论即可.

设 $\lim_{n\to \infty}a_n = a,\lim_{n\to \infty}b_n = b$ ，则对任给的 $\varepsilon >0$ ，分别存在正数 $N_{1}$ 与 $N_{2}$ ，使得

$$
\mid a _ {n} - a \mid <   \varepsilon , \text {当} n > N _ {1},
$$

$$
\mid b _ {n} - b \mid <   \varepsilon , \text {当} n > N _ {2}.
$$

取 $N = \max \{N_{1}, N_{2}\}$，则当 $n > N$ 时上述两不等式同时成立，从而有

1. $\left|\left(a_{n}+b_{n}\right)-\left(a+b\right)\right|\leqslant\left|a_{n}-a\right|+\left|b_{n}-b\right|<2\varepsilon\Rightarrow\lim_{n\to\infty}\left(a_{n}+b_{n}\right)=a+b.$

2. $|a_{n}b_{n}-ab|=|(a_{n}-a)b_{n}+a(b_{n}-b)|\leqslant|a_{n}-a||b_{n}|+|a||b_{n}-b|$. (8)

由收敛数列的有界性定理,存在正数 M, 对一切 n 有  $\left|b_{n}\right| < M$ . 于是, 当 n > N 时, 由(8)式可得

$$
\mid a _ {n} b _ {n} - a b \mid <   (M + \mid a \mid) \varepsilon .
$$

由 $\varepsilon$ 的任意性，这就证得 $\lim_{n\to \infty}a_nb_n = ab.$

3. 由于 $\lim_{n\to \infty}b_n = b\neq 0$ ，根据收敛数列的保号性，存在正数 $N_{3}$ ，使得当 $n > N_{3}$ 时，有$|b_n| > \frac{1}{2} |b|$ .取 $N^{\prime} = \max \{N_2,N_3\}$ ，则当 $n > N^{\prime}$ 时，有

$$
\left| \frac {1}{b _ {n}} - \frac {1}{b} \right| = \frac {\mid b _ {n} - b \mid}{\mid b _ {n} b \mid} <   \frac {2 \mid b _ {n} - b \mid}{b ^ {2}} <   \frac {2 \varepsilon}{b ^ {2}}.
$$

由  $\varepsilon$  的任意性, 这就证得  $\lim_{n\to\infty}\frac{1}{b_n}=\frac{1}{b}$ .

例4 求

$$
\lim _ {n \to \infty} \frac {a _ {m} n ^ {m} + a _ {m - 1} n ^ {m - 1} + \cdots + a _ {1} n + a _ {0}}{b _ {k} n ^ {k} + b _ {k - 1} n ^ {k - 1} + \cdots + b _ {1} n + b _ {0}},
$$

其中 $m \leqslant k, a_{m} \neq 0, b_{k} \neq 0$.

解 以  $n^{-k}$  同乘分子分母后, 所求极限式化为

$$
\lim _ {n \to \infty} \frac {a _ {m} n ^ {m - k} + a _ {m - 1} n ^ {m - 1 - k} + \cdots + a _ {1} n ^ {1 - k} + a _ {0} n ^ {- k}}{b _ {k} + b _ {k - 1} n ^ {- 1} + \cdots + b _ {1} n ^ {1 - k} + b _ {0} n ^ {- k}}.
$$

由 §1 例 2 知, 当 $\alpha > 0$ 时, 有 $\lim_{n \to \infty} n^{-\alpha} = 0$. 于是, 当 $m = k$ 时, 上式除了分子分母的第一项分别为 $a_m$ 与 $b_k$ 外, 其余各项的极限皆为 0 , 故此时所求的极限等于 $\frac{a_m}{b_k}$; 当 $m < k$ 时, 由于 $n^{m-k} \to 0 (n \to \infty)$, 故此时所求的极限等于 0 . 综上所述, 得到

$$
\lim _ {n \to \infty} \frac {a _ {m} n ^ {m} + a _ {m - 1} n ^ {m - 1} + \cdots + a _ {1} n + a _ {0}}{b _ {k} n ^ {k} + b _ {k - 1} n ^ {k - 1} + \cdots + b _ {1} n + b _ {0}} = \left\{ \begin{array}{l l} \frac {a _ {m}}{b _ {m}}, & k = m, \\ 0, & k > m. \end{array} \right.
$$

例 5 求  $\lim_{n\to\infty}\frac{a^{n}}{a^{n}+1}$ ，其中  $a\neq-1$ .

解 若 $a = 1$ ，则显然有 $\lim_{n\to \infty}\frac{a^n}{a^n + 1} = \frac{1}{2}$

若 $|a| < 1$，则由 $\lim_{n\to \infty}a^n = 0$ 得

$$
\lim _ {n \to \infty} \frac {a ^ {n}}{a ^ {n} + 1} = \lim _ {n \to \infty} a ^ {n} / (\lim _ {n \to \infty} a ^ {n} + 1) = 0;
$$

若 $|a| > 1$ ，则

$$
\lim _ {n \to \infty} \frac {a ^ {n}}{a ^ {n} + 1} = \lim _ {n \to \infty} \frac {1}{1 + \frac {1}{a ^ {n}}} = \frac {1}{1 + 0} = 1.
$$

例6 求 $\lim_{n\to \infty}\sqrt{n} (\sqrt{n + 1} -\sqrt{n})$

解 $\sqrt{n} (\sqrt{n + 1} -\sqrt{n}) = \frac{\sqrt{n}}{\sqrt{n + 1} + \sqrt{n}} = \frac{1}{\sqrt{1 + \frac{1}{n}} + 1},$

由 $1 + \frac{1}{n}\rightarrow 1(n\to \infty)$ 及例1得

$$
\lim _ {n \to \infty} \sqrt {n} (\sqrt {n + 1} - \sqrt {n}) = \lim _ {n \to \infty} \frac {1}{\sqrt {1 + \frac {1}{n}} + 1} = \frac {1}{2}.
$$

最后,我们给出数列的子列概念和关于子列的一个重要定理.

定义 1 设  $\{a_{n}\}$  为数列,  $\{n_{k}\}$  为正整数集  $N_{+}$  的无限子集, 且  $n_{1}<n_{2}<\cdots<n_{k}<\cdots$ , 则数列

$$
a _ {n _ {1}}, a _ {n _ {2}}, \dots , a _ {n _ {k}}, \dots
$$

称为数列 $\{a_{n}\}$ 的一个子列，记为 $\{a_{n_k}\}$.

注1 由定义1可见，$\{a_{n}\}$ 的子列 $\{a_{n_k}\}$ 的各项都选自 $\{a_{n}\}$，且保持这些项在 $\{a_{n}\}$ 中的先后次序。$\{a_{n_k}\}$ 中的第 $k$ 项是 $\{a_{n}\}$ 中的第 $n_k$ 项，故总有 $n_k \geqslant k$. 实际上 $\{n_k\}$ 本身也是正整数列 $\{n\}$ 的子列.

例如, 子列  $\{a_{2k}\}$  由数列  $\{a_{n}\}$  的所有偶数项所组成, 而子列  $\{a_{2k-1}\}$  则由  $\{a_{n}\}$  的所有奇数项所组成. 又  $\{a_{n}\}$  本身也是  $\{a_{n}\}$  的一个子列, 此时  $n_{k}=k, k=1,2,\cdots$ .

定理2.8 数列 $\{a_{n}\}$ 收敛的充要条件是: $\{a_{n}\}$ 的任何子列都收敛.

证 充分性 因为 $\{a_{n}\}$ 也是自身的一个子列, 所以结论是显然的.

必要性 设 $\lim_{n\to \infty}a_n = a, \{a_{n_k}\}$ 是 $\{a_n\}$ 的任一个子列. 对任给的正数 $\varepsilon$，存在正数 $N$，当 $k > N$ 时，有 $|a_k - a| < \varepsilon$. 又因为 $n_k \geqslant k$，所以当 $k > N$ 时，有 $|a_{n_k} - a| < \varepsilon$. 这就证明了 $\{a_{n_k}\}$ 收敛（且与 $\{a_n\}$ 有相同的极限）. □

由定理2.8的证明可见，若数列 $\{a_{n}\}$ 的任何子列都收敛，则所有这些子列与 $\{a_{n}\}$ 必收敛于同一个极限。于是，若数列 $\{a_{n}\}$ 有一个子列发散，或有两个子列收敛而极限不相等，则数列 $\{a_{n}\}$ 一定发散。例如数列 $\{(-1)^{n}\}$，其偶数项组成的子列 $\{(-1)^{2k}\}$ 收敛于1，而奇数项组成的子列 $\{(-1)^{2k-1}\}$ 收敛于-1，从而 $\{(-1)^{n}\}$ 发散。再如数列 $\left\{\sin \frac{n\pi}{2}\right\}$，它的奇数项组成的子列 $\left\{\sin \frac{2k-1}{2}\pi\right\}$ 即为 $\{(-1)^{k-1}\}$，由于这个子列发散，故数列 $\left\{\sin \frac{n\pi}{2}\right\}$ 发散。由此可见，定理2.8是判断数列发散的有力工具。

这里应该注意: 若数列  $\{a_{n}\}$  满足  $\lim_{n\to\infty}a_{2n-1}=\lim_{n\to\infty}a_{2n}=A$ ，由本章 §1 例 8 可知  $\lim_{n\to\infty}a_{n}=A$ .

## 习题 2.2

1. 求下列极限:

(1)  $\lim_{n\to\infty}\frac{n^{3}+3n^{2}+1}{4n^{3}+2n+3};$

(2)  $\lim_{n\to\infty}\frac{1+2n}{n^{2}}$ ;

(3)  $\lim_{n\to\infty}\frac{(-2)^{n}+3^{n}}{(-2)^{n+1}+3^{n+1}};$

(4)  $\lim_{n\to\infty}\left(\sqrt{n^{2}+n}-n\right)$ ;

(5)  $\lim_{n\to\infty}\left(\sqrt[n]{1}+\sqrt[n]{2}+\cdots+\sqrt[n]{10}\right)$ ;

(6)  $\lim_{n\to\infty}\frac{\frac{1}{2}+\frac{1}{2^2}+\cdots+\frac{1}{2^n}}{\frac{1}{3}+\frac{1}{3^2}+\cdots+\frac{1}{3^n}}.$

2. 设 $\lim_{n\to \infty}a_n = a, \lim_{n\to \infty}b_n = b$，且 $a < b$. 证明:存在正数 $N$，使得当 $n > N$ 时，有 $a_n < b_n$.

3. 设 $\{a_{n}\}$ 为无穷小数列，$\{b_{n}\}$ 为有界数列，证明:$\{a_{n}b_{n}\}$ 为无穷小数列.

4. 求下列极限:

(1)  $\lim_{n\to\infty}\left(\frac{1}{1\cdot2}+\frac{1}{2\cdot3}+\cdots+\frac{1}{n(n+1)}\right)$ ;

(2)  $\lim_{n\to\infty}\left(\sqrt{2}\sqrt[4]{2}\sqrt[8]{2}\cdots^{2\sqrt[n]{2}}\right)$ ;

(3)  $\lim_{n\to\infty}\left(\frac{1}{2}+\frac{3}{2^{2}}+\cdots+\frac{2n-1}{2^{n}}\right)$ ;

(4)  $\lim_{n\to\infty}\sqrt[n]{1-\frac{1}{n}}$ ;

(5)  $\lim_{n\to\infty}\left(\frac{1}{n^{2}}+\frac{1}{(n+1)^{2}}+\cdots+\frac{1}{(2n)^{2}}\right)$ ;

(6)  $\lim_{n\to\infty}\left(\frac{1}{\sqrt{n^{2}+1}}+\frac{1}{\sqrt{n^{2}+2}}+\cdots+\frac{1}{\sqrt{n^{2}+n}}\right).$

5. 设 $\{a_{n}\}$ 与 $\{b_{n}\}$ 中一个是收敛数列, 另一个是发散数列. 证明 $\{a_{n} \pm b_{n}\}$ 是发散数列. 又问 $\{a_{n}b_{n}\}$ 和 $\left\{\frac{a_{n}}{b_{n}}\right\} (b_{n} \neq 0)$ 是否必为发散数列?

6. 证明以下数列发散:

(1)  $\left\{(-1)^{n}\frac{n}{n+1}\right\}$ ;

(2) $\{n^{(-1)^n}\}$;

(3) $\left\{\cos \frac{n\pi}{4}\right\}$.

7. 判断以下结论是否成立(若成立,说明理由;若不成立,举出反例):

(1) 若  $\{a_{2k-1}\}$  和  $\{a_{2k}\}$  都收敛，则  $\{a_{n}\}$  收敛；
(2) 若  $\{a_{3k-2}\}$ ,  $\{a_{3k-1}\}$  和  $\{a_{3k}\}$  都收敛, 且有相同极限, 则  $\{a_{n}\}$  收敛.

8. 求下列极限:

(1)  $\lim_{n\to\infty}\frac{1}{2}\cdot\frac{3}{4}\cdot\cdots\cdot\frac{2n-1}{2n};$
(2) $\lim_{n\to \infty}\frac{\sum_{p = 1}^{n}p!}{n!};$
(3)  $\lim_{n\to\infty}\left[(n+1)^{\alpha}-n^{\alpha}\right],0<\alpha<1;$
(4)  $\lim_{n\to\infty}(1+\alpha)(1+\alpha^{2})\cdots(1+\alpha^{2^{n}}),\quad|\alpha|<1.$

9. 设  $a_{1}, a_{2}, \cdots, a_{m}$  为 m 个正数, 证明:

$$
\lim _ {n \to \infty} \sqrt [ n ]{a _ {1} ^ {n} + a _ {2} ^ {n} + \cdots + a _ {m} ^ {n}} = \max \left\{a _ {1}, a _ {2}, \dots , a _ {m} \right\}.
$$

10. 设  $\lim_{n\to\infty}a_{n}=a$ . 证明:

(1)  $\lim_{n\to\infty}\frac{\left[na_{n}\right]}{n}=a;$

(2) 若  $a > 0, a_{n} > 0$ ，则  $\lim_{n \to \infty} \sqrt[n]{a_{n}} = 1$ .

## § 3 数列极限存在的条件

在研究比较复杂的数列极限问题时,通常先考察该数列是否有极限(极限的存在性问题);若有极限,再考虑如何计算此极限(极限值的计算问题).这是极限理论的两个基本问题.在实际应用中,解决了数列 $\{a_{n}\}$ 极限的存在性问题之后,即使极限值的计算较为困难,但由于当n充分大时, $a_{n}$ 能充分接近其极限a,故可用 $a_{n}$ 作为a的近似

值.本节将重点讨论极限的存在性问题.

为了确定某个数列是否存在极限,当然不可能将每个实数依定义一一验证,根本的办法是直接从数列本身的特征来作出判断.

首先讨论单调数列,其定义与单调函数相仿.若数列 $\{a_{n}\}$ 的各项满足关系式

$$
a _ {n} \leqslant a _ {n + 1} \quad (a _ {n} \geqslant a _ {n + 1}),
$$

则称 $\{a_{n}\}$ 为递增（递减）数列.递增数列和递减数列统称为单调数列.如 $\left\{\frac{1}{n}\right\}$ 为递减数列； $\left\{\frac{n}{n + 1}\right\}$ 与 $\{n^2\}$ 为递增数列；而 $\left\{\frac{(-1)^n}{n}\right\}$ 则不是单调数列，但 $\left\{\frac{(-1)^n}{n}\right\}$ 的奇数项子列与偶数项子列分别是单调的.

定理 2.9(单调有界定理) 在实数系中,有界的单调数列必有极限.

证 不妨设 $\{a_{n}\}$ 为有上界的递增数列. 由确界原理, 数列 $\{a_{n}\}$ 有上确界, 记 $a = \sup \{a_{n}\}$. 下面证明 $a$ 就是 $\{a_{n}\}$ 的极限. 事实上, 任给 $\varepsilon > 0$, 按上确界的定义, 存在数列 $\{a_{n}\}$ 中某一项 $a_{N}$, 使得 $a - \varepsilon < a_{N}$. 又由 $\{a_{n}\}$ 的递增性, 当 $n \geqslant N$ 时, 有

$$
a - \varepsilon <   a _ {N} \leqslant a _ {n}.
$$

另一方面，由于 $a$ 是 $\{a_{n}\}$ 的一个上界，故对一切 $a_{n}$，都有 $a_{n} \leqslant a < a + \varepsilon$. 所以当 $n \geqslant N$ 时，有

$$
a - \varepsilon <   a _ {n} <   a + \varepsilon ,
$$

这就证得 $\lim_{n\to \infty}a_n = a$ .同理可证有下界的递减数列必有极限，且其极限即为它的下确界.□

例 1 设  $a_{n}=1+\frac{1}{2^{\alpha}}+\cdots+\frac{1}{n^{\alpha}},\alpha>1$ . 证明: $\{a_{n}\}$  收敛.

证 显然 $\{a_{n}\}$ 是递增数列.因为当 $n\geqslant 2$ 时，

$$
\begin{array}{l} a _ {2 n} = 1 + \frac {1}{2 ^ {\alpha}} + \dots + \frac {1}{(2 n) ^ {\alpha}} = \left(1 + \frac {1}{3 ^ {\alpha}} + \dots + \frac {1}{(2 n - 1) ^ {\alpha}}\right) + \left(\frac {1}{2 ^ {\alpha}} + \dots + \frac {1}{(2 n) ^ {\alpha}}\right) \\ <   \left(1 + \frac {1}{3 ^ {\alpha}} + \dots + \frac {1}{(2 n + 1) ^ {\alpha}}\right) + \left(\frac {1}{2 ^ {\alpha}} + \dots + \frac {1}{(2 n) ^ {\alpha}}\right) \\ <   1 + 2 \frac {a _ {n}}{2 ^ {\alpha}} = 1 + \frac {a _ {n}}{2 ^ {\alpha - 1}}, \\ \end{array}
$$

以及 $a_{n} < a_{2n}$ ，所以

$$
a _ {n} <   \frac {1}{1 - \frac {1}{2 ^ {\alpha - 1}}},
$$

故 $\{a_{n}\}$ 是有界的.根据单调有界定理可知数列 $\{a_{n}\}$ 是收敛的.

例2 证明数列

$$
\sqrt {2}, \sqrt {2 + \sqrt {2}}, \dots , \underbrace {\sqrt {2 + \sqrt {2 + \cdots + \sqrt {2}}}} _ {n \text {个根号}}, \dots
$$

收敛,并求其极限.

证 记 $a_{n} = \sqrt{2 + \sqrt{2 + \cdots + \sqrt{2}}}$, 易见数列 $\{a_{n}\}$ 是递增的. 现用数学归纳法来证明

$\{a_{n}\}$ 有上界.

显然 $a_1 = \sqrt{2} < 2$. 假设 $a_n < 2$, 则有 $a_{n+1} = \sqrt{2 + a_n} < \sqrt{2 + 2} = 2$, 从而对一切 $n$, 有 $a_n < 2$, 即 $\{a_n\}$ 有上界.

由单调有界定理,数列 $\{a_{n}\}$ 有极限,记为a.由于

$$
a _ {n + 1} ^ {2} = 2 + a _ {n},
$$

对上式两边取极限得  $a^{2}=2+a$ ，即有

$$
(a + 1) (a - 2) = 0 \text {, 解得} a = - 1 \text {或} a = 2.
$$

由数列极限的保不等式性,a=-1 是不可能的,故有

$$
\lim _ {n \to \infty} \sqrt {2 + \sqrt {2 + \cdots + \sqrt {2}}} = 2.
$$

例3 设 $S$ 为有界数集. 证明: 若 $\sup S = a \notin S$, 则存在严格递增数列 $\{x_{n}\} \subset S$, 使得 $\lim_{n\to \infty}x_{n} = a$.

证 因 $a$ 是 $S$ 的上确界, 故对任给的 $\varepsilon > 0$, 存在 $x \in S$, 使得 $x > a - \varepsilon$. 又因 $a \notin S$, 故 $x < a$, 从而有

$$
a - \varepsilon <   x <   a.
$$

现取 $\varepsilon_{1} = 1$ ，则存在 $x_{1}\in S$ ，使得

$$
a - \varepsilon_ {1} <   x _ {1} <   a.
$$

再取 $\varepsilon_{2} = \min \left\{\frac{1}{2}, a - x_{1}\right\} > 0$，则存在 $x_{2} \in S$，使得

$$
a - \varepsilon_ {2} <   x _ {2} <   a,
$$

且有 $x_{2} > a - \varepsilon_{2}\geqslant a - (a - x_{1}) = x_{1}.$

一般地，按上述步骤得到 $x_{n - 1}\in S$ 之后，取 $\varepsilon_{n} = \min \left\{\frac{1}{n},a - x_{n - 1}\right\}$ ，则存在 $x_{n}\in S$ ，使得

$$
a - \varepsilon_ {n} <   x _ {n} <   a,
$$

且有 $x_{n} > a - \varepsilon_{n}\geqslant a - (a - x_{n - 1}) = x_{n - 1}.$

上述过程无限地进行下去,得到数列 $\{x_{n}\}\subset S$ ,它是严格递增数列,且满足

$$
a - \varepsilon_ {n} <   x _ {n} <   a <   a + \varepsilon_ {n} \Rightarrow | x _ {n} - a | <   \varepsilon_ {n} \leqslant \frac {1}{n}, n = 1, 2, \dots .
$$

这就证明了 $\lim_{n\to \infty}x_n = a$

例 4 证明极限  $\lim_{n\to\infty}\left(1+\frac{1}{n}\right)^{n}$  存在.

证 设  $a_{n}=\left(1+\frac{1}{n}\right)^{n}, n=1,2,\cdots$ . 由二项式定理

$$
\begin{array}{l} a _ {n} = \left(1 + \frac {1}{n}\right) ^ {n} = 1 + C _ {n} ^ {1} \frac {1}{n} + \dots + C _ {n} ^ {k} \frac {1}{n ^ {k}} + \dots + C _ {n} ^ {n} \frac {1}{n ^ {n}} \\ = 1 + 1 + \frac {n (n - 1)}{2 !} \frac {1}{n ^ {2}} + \dots + \frac {n (n - 1) \cdots (n - k + 1)}{k !} \frac {1}{n ^ {k}} + \dots + \frac {1}{n ^ {n}} \\ = 2 + \frac {1}{2 !} \left(1 - \frac {1}{n}\right) + \dots + \frac {1}{k !} \left(1 - \frac {1}{n}\right) \left(1 - \frac {2}{n}\right) \dots \left(1 - \frac {k - 1}{n}\right) + \dots + \\ \end{array}
$$

$$
\begin{array}{l} \frac {1}{n !} \left(1 - \frac {1}{n}\right) \left(1 - \frac {2}{n}\right) \dots \left(1 - \frac {n - 1}{n}\right) \\ <   2 + \frac {1}{2 !} \left(1 - \frac {1}{n + 1}\right) + \dots + \frac {1}{k !} \left(1 - \frac {1}{n + 1}\right) \left(1 - \frac {2}{n + 1}\right) \dots \left(1 - \frac {k - 1}{n + 1}\right) + \dots + \\ \frac {1}{(n + 1) !} \left(1 - \frac {1}{n + 1}\right) \left(1 - \frac {2}{n + 1}\right) \dots \left(1 - \frac {n}{n + 1}\right) \\ = a _ {n + 1}, \\ \end{array}
$$

故 $\{a_{n}\}$ 是严格递增的.由上式可推得

$$
\begin{array}{l} a _ {n} <   2 + \frac {1}{2 !} + \dots + \frac {1}{k !} + \dots + \frac {1}{n !} <   2 + \frac {1}{1 \cdot 2} + \dots + \frac {1}{(k - 1) k} + \dots + \frac {1}{(n - 1) n} \\ <   2 + \left(1 - \frac {1}{2}\right) + \dots + \left(\frac {1}{k - 1} - \frac {1}{k}\right) + \dots + \left(\frac {1}{n - 1} - \frac {1}{n}\right) = 3 - \frac {1}{n} <   3, \\ \end{array}
$$

这表明 $\{a_{n}\}$ 又是有界的.由单调有界定理推知 $\lim_{n\to \infty}\left(1 + \frac{1}{n}\right)^n$ 存在.

通常用拉丁字母 e 代表该数列的极限, 即

$$
\lim _ {n \to \infty} \left(1 + \frac {1}{n}\right) ^ {n} = \mathrm{e},
$$

它是一个无理数(待证),其前十三位数字是

$$
\mathrm{e} \approx 2. 7 1 8 2 8 1 8 2 8 4 5 9.
$$

以 e 为底的对数称为自然对数,通常记

$$
\ln x = \log_ {\mathrm{e}} x.
$$

例 5 任何数列都存在单调子列.

证 设数列为 $\{a_{n}\}$. 下面分两种情形来讨论:

1. 若对任何正整数 $k$，数列 $\{a_{k+n}\}$ 有最大项。设 $\{a_{1+n}\}$ 的最大项为 $a_{n_1}$，因 $\{a_{n_1+n}\}$ 亦有最大项，设其最大项为 $a_{n_2}$，显然有 $n_2 > n_1$，且因 $\{a_{n_1+n}\}$ 是 $\{a_{1+n}\}$ 的一个子列，故

$$
a _ {n _ {2}} \leqslant a _ {n _ {1}};
$$

同理存在 $n_3 > n_2$ ，使得

$$
a _ {n _ {3}} \leqslant a _ {n _ {2}};
$$

... ... ... ... ... ... ... ...

这样就得到一个单调递减的子列 $\{a_{n_k}\}$.

2. 至少存在某正整数 $k$，数列 $\{a_{k+n}\}$ 没有最大项。先取 $n_1 = k + 1$，因 $\{a_{k+n}\}$ 没有最大项，故 $a_{n_1}$ 后面总存在项 $a_{n_2}(n_2 > n_1)$，使得

$$
a _ {n _ {2}} > a _ {n _ {1}};
$$

同理存在 $a_{n_2}$ 后面的项 $a_{n_3}(n_3 > n_2)$，使得

$$
a _ {n _ {3}} > a _ {n _ {2}};
$$

... ... ... ... ... ... ...

这样就得到一个严格递增的子列 $\{a_{n_k}\}$.

定理 2.10(致密性定理) 任何有界数列必定有收敛的子列.

证 设数列 $\{a_{n}\}$ 有界, 由例5可知: $\{a_{n}\}$ 存在单调且有界的子列 $\{a_{n_k}\}$. 再由单调有界定理, 证得此子列是收敛的.

例6 设数列 $\{a_{n}\}$ 无上界，则存在 $\{a_{n}\}$ 的子列 $\{a_{n_k}\}$，$\lim_{k\to \infty}a_{n_k} = +\infty$。

证 因为 $\{a_{n}\}$ 无上界，所以对于任意正数 $M$ ，存在 $a_{n_0}$ ，使得 $a_{n_0} > M.$ 据此分别取

$M_{1} = 1$ ，存在 $a_{n_1}, a_{n_1} > 1$

$M_{2}=\max\left\{2,\mid a_{1}\mid,\mid a_{2}\mid,\cdots,\mid a_{n_{1}}\mid\right\}$ ，存在 $a_{n_{2}}(n_{2}>n_{1})$ ，使得 $a_{n_{2}}>M_{2}$ ;

... ... ... ... ... ... ...

$M_{k}=\max\left\{k,\mid a_{1}\mid,\mid a_{2}\mid,\cdots,\mid a_{n_{k-1}}\mid\right\}$ ，存在 $a_{n_{k}}(n_{k}>n_{k-1})$ ，使得 $a_{n_{k}}>M_{k}$ ;

... ... ... ... ... ... ...

由此得到 $\{a_{n}\}$ 的一个子列 $\{a_{n_k}\}$，满足 $a_{n_k} > M_k \geqslant k$，推得

$$
\lim _ {k \to \infty} a _ {n _ {k}} = + \infty .
$$

单调有界定理只是数列收敛的充分条件.下面给出在实数系中数列收敛的充分必要条件.

定理 2.11(柯西(Cauchy)收敛准则) 数列  $\{a_{n}\}$  收敛的充要条件是: 对任给的  $\varepsilon>0$ , 存在正整数 N, 使得当 n, m>N 时, 有

$$
\left| a _ {n} - a _ {m} \right| <   \varepsilon .
$$

这个定理从理论上完全解决了数列极限的存在性问题.

证 必要性 设 $\lim_{n\to \infty}a_n = A.$ 由数列极限定义，对任给的 $\varepsilon >0$ ，存在 $N > 0$ ，当 $m,n > N$ 时，有

$$
\mid a _ {m} - A \mid <   \frac {\varepsilon}{2}, \mid a _ {n} - A \mid <   \frac {\varepsilon}{2},
$$

因而 $|a_{m} - a_{n}| \leqslant |a_{m} - A| + |a_{n} - A| < \frac{\varepsilon}{2} + \frac{\varepsilon}{2} = \varepsilon.$

充分性 先证明该数列必定有界. 取 $\varepsilon_0 = 1$，因为 $\{a_n\}$ 满足柯西条件，所以 $\exists N_0, \forall n > N_0$，有

$$
\mid a _ {n} - a _ {N _ {0} + 1} \mid <   1.
$$

令  $M=\max\left\{\left|a_{1}\right|,\left|a_{2}\right|,\cdots,\left|a_{N_{0}}\right|,\left|a_{N_{0}+1}\right|+1\right\}$ ，则对一切 n，成立

$$
\mid a _ {n} \mid \leqslant M.
$$

由致密性定理,在 $\{a_{n}\}$ 中必有收敛子列

$$
\lim _ {k \to \infty} a _ {n _ {k}} = \xi .
$$

由条件, $\forall\varepsilon>0,\exists N$ ,当n,m>N时,有

$$
\mid a _ {n} - a _ {m} \mid <   \frac {\varepsilon}{2}.
$$

在上式中取 $a_{m} = a_{n_{k}}$ ，其中 $k$ 充分大，满足 $n_k > N$ ，并且令 $k\to \infty$ ，于是得到

$$
\mid a _ {n} - \xi \mid \leqslant \frac {\varepsilon}{2} <   \varepsilon ,
$$

即数列 $\{a_{n}\}$ 收敛.

柯西收敛准则的条件称为柯西条件,它反映这样的事实:收敛数列各项的值愈到后面,彼此愈是接近,以至充分后面的任何两项之差的绝对值可小于预先给定的任意小正数.或者形象地说,收敛数列的各项越到后面越是“挤”在一起.另外,柯西收敛准则把  $\varepsilon-N$  定义中  $a_{n}$  与 a 的关系换成了  $a_{n}$  与  $a_{m}$  的关系,其好处在于无需借助数列以外的数 a,只要根据数列本身的特征就可以鉴别其(收)敛(发)散性.

例 7 证明:任一无限十进小数  $\alpha=0.b_{1}b_{2}\cdots b_{n}\cdots$  的 n 位不足近似值  $(n=1,2,\cdots)$  所组成的数列

$$
\frac {b _ {1}}{1 0}, \frac {b _ {1}}{1 0} + \frac {b _ {2}}{1 0 ^ {2}}, \dots , \frac {b _ {1}}{1 0} + \frac {b _ {2}}{1 0 ^ {2}} + \dots + \frac {b _ {n}}{1 0 ^ {n}}, \dots \tag {1}
$$

满足柯西条件(从而必收敛),其中 $b_{k}$ 为0,1,2,…,9中的一个数, $k=1,2,\cdots$ .

证 记  $a_{n}=\frac{b_{1}}{10}+\frac{b_{2}}{10^{2}}+\cdots+\frac{b_{n}}{10^{n}}$ . 不妨设 n>m, 则有

$$
\begin{array}{l} \mid a _ {n} - a _ {m} \mid = \frac {b _ {m + 1}}{1 0 ^ {m + 1}} + \frac {b _ {m + 2}}{1 0 ^ {m + 2}} + \dots + \frac {b _ {n}}{1 0 ^ {n}} \\ \leqslant \frac {9}{1 0 ^ {m + 1}} \bigg (1 + \frac {1}{1 0} + \dots + \frac {1}{1 0 ^ {n - m - 1}} \bigg) \\ = \frac {1}{1 0 ^ {m}} \bigg (1 - \frac {1}{1 0 ^ {n - m}} \bigg) <   \frac {1}{1 0 ^ {m}} <   \frac {1}{m}. \\ \end{array}
$$

对任给的 $\varepsilon > 0$ ，取 $N = \frac{1}{\varepsilon}$ ，则对一切 $n > m > N$ ，有

$$
\left| a _ {n} - a _ {m} \right| <   \varepsilon .
$$

这就证明了数列(1)满足柯西条件.

循环小数 0.9 的不足近似值组成的数列为

$$
a _ {n} = \frac {9}{1 0} + \frac {9}{1 0 ^ {2}} + \dots + \frac {9}{1 0 ^ {n}}, \quad n = 1, 2, \dots .
$$

由 §1 例 4 可知  $\lim_{n\to\infty}a_{n}=\lim_{n\to\infty}\frac{9}{10}\cdot\frac{1-\left(\frac{1}{10}\right)^{n}}{1-\frac{1}{10}}=1$ . 这就是为什么可以将无限小数 0.9 表示为 1 的一个原因.

## 习题2.3

1. 利用 $\lim_{n\to \infty}\left(1 + \frac{1}{n}\right)^n = \mathrm{e}$ 求下列极限:

(1) $\lim_{n\to \infty}\left(1 - \frac{1}{n}\right)^n;$

(2) $\lim_{n\to \infty}\left(1 + \frac{1}{n}\right)^{n + 1}$;

(3) $\lim_{n\to \infty}\left(1 + \frac{1}{n + 1}\right)^n;$

(4)  $\lim_{n\to\infty}\left(1+\frac{1}{2n}\right)^{n}$ ;

(5) $\lim_{n\to \infty}\left(1 + \frac{1}{n^2}\right)^n.$

2. 试问下面的解题方法是否正确:

求  $\lim_{n\to\infty}2^{n}$ .

解 设 $a_{n} = 2^{n}$ 及 $\lim_{n\to \infty}a_n = a.$ 由于 $a_{n} = 2a_{n - 1}$，两边取极限（$n\to \infty$）得 $a = 2a$，所以 $a = 0$

3. 证明下列数列极限存在并求其值:

(1) 设  $a_{1}=\sqrt{2}, a_{n+1}=\sqrt{2a_{n}}, n=1,2,\cdots;$
(2) 设  $a_{1}=\sqrt{c}\quad(c>0)$ ,  $a_{n+1}=\sqrt{c+a_{n}}$ ,  $n=1,2,\cdots;$
(3)  $a_{n}=\frac{c^{n}}{n!}\quad(c>0),\quad n=1,2,\cdots.$

4. 利用 $\left\{\left(1 + \frac{1}{n}\right)^n\right\}$ 为递增数列的结论，证明 $\left\{\left(1 + \frac{1}{n + 1}\right)^n\right\}$ 为递增数列.

5. 应用柯西收敛准则, 证明以下数列  $\{a_{n}\}$  收敛:

(1) $a_{n}=\frac{\sin 1}{2}+\frac{\sin 2}{2^{2}}+\cdots+\frac{\sin n}{2^{n}};$

(2) $a_{n} = 1 + \frac{1}{2^{2}} +\frac{1}{3^{2}} +\dots +\frac{1}{n^{2}}.$

6. 证明: 若单调数列  $\{a_{n}\}$  含有一个收敛子列, 则  $\{a_{n}\}$  收敛.

7. 证明: 若 $a_{n} > 0$, 且 $\lim_{n \to \infty} \frac{a_{n}}{a_{n+1}} = l > 1$, 则 $\lim_{n \to \infty} a_{n} = 0$.

8. 证明:若 $\{a_{n}\}$ 为递增（递减）有界数列，则

$$
\lim _ {n \to \infty} a _ {n} = \sup \left\{a _ {n} \right\} (\inf \left\{a _ {n} \right\}).
$$

又问逆命题成立否？

9. 利用不等式

$$
b ^ {n + 1} - a ^ {n + 1} > (n + 1) a ^ {n} (b - a), b > a > 0,
$$

证明: $\left\{\left(1+\frac{1}{n}\right)^{n+1}\right\}$  为递减数列，并由此推出 $\left\{\left(1+\frac{1}{n}\right)^{n}\right\}$  为有界数列.

10. 证明: $\left|\mathrm{e}-\left(1+\frac{1}{n}\right)^{n}\right|<\frac{3}{n}.$

提示: 利用上题可知  $e<\left(1+\frac{1}{n}\right)^{n+1}$ ，又易证  $\left(1+\frac{1}{n}\right)^{n+1}<\frac{3}{n}+\left(1+\frac{1}{n}\right)^{n}$ .

11. 给定两正数 $a_1$ 与 $b_1(a_1 > b_1)$，作出其等差中项 $a_2 = \frac{a_1 + b_1}{2}$ 与等比中项 $b_2 = \sqrt{a_1b_1}$，一般地令

$$
a _ {n + 1} = \frac {a _ {n} + b _ {n}}{2}, b _ {n + 1} = \sqrt {a _ {n} b _ {n}}, n = 1, 2, \dots .
$$

证明: $\lim_{n\to \infty}a_n$ 与 $\lim_{n\to \infty}b_n$ 皆存在且相等.

12. 设 $\{a_{n}\}$ 为有界数列，记

$$
\overline {{a}} _ {n} = \sup \left\{a _ {n}, a _ {n + 1}, \dots \right\}, \underline {{a}} _ {n} = \inf \left\{a _ {n}, a _ {n + 1}, \dots \right\}.
$$

证明:（1）对任何正整数 $n, \bar{a}_n \geqslant \underline{a}_n$；

(2) $\{\bar{a}_{n}\}$ 为递减有界数列, $\{\underline{a}_{n}\}$ 为递增有界数列,且对任何正整数n,m,有 $\bar{a}_{n}\geqslant\underline{a}_{m}$ ;

(3) 设  $\bar{a}$  和  $\underline{a}$  分别是  $\{\bar{a}_{n}\}$  和  $\{\underline{a}_{n}\}$  的极限, 则  $\bar{a} \geqslant \underline{a}$ ;

(4)  $\{a_{n}\}$  收敛的充要条件是  $\bar{a}=a.$

# 第二章总练习题

1. 求下列数列的极限:

(1)  $\lim_{n\to\infty}\sqrt[n]{n^{3}+3^{n}}$ ;
(2)  $\lim_{n\to\infty}\frac{n^{5}}{e^{n}}$ ;
(3)  $\lim_{n\to\infty}\left(\sqrt{n+2}-2\sqrt{n+1}+\sqrt{n}\right).$

2. 证明:

(1)  $\lim_{n\to\infty}n^{2}q^{n}=0\left(\left|q\right|<1\right)$ ;

(2) $\lim_{n\to \infty}\frac{\lg n}{n^{\alpha}} = 0 (\alpha \geqslant 1)$.

3. 设 $\lim_{n\to \infty}a_n = a$ ，证明:

(1)  $\lim_{n\to\infty}\frac{a_{1}+a_{2}+\cdots+a_{n}}{n}=a$  (又问由此等式能否反过来推出  $\lim_{n\to\infty}a_{n}=a$ );
(2) 若  $a_{n}>0\ (n=1,2,\cdots)$ ，则  $\lim_{n\to\infty}\sqrt[n]{a_{1}a_{2}\cdots a_{n}}=a.$

4. 应用上题的结论证明下列各题:

(1)  $\lim_{n\to\infty}\frac{1+\frac{1}{2}+\frac{1}{3}+\cdots+\frac{1}{n}}{n}=0;$

(2)  $\lim_{n\to\infty}\sqrt[n]{a}=1\quad(a>0)$ ;

(3)  $\lim_{n\to\infty}\sqrt[n]{n}=1;$

(4)  $\lim_{n\to\infty}\frac{1}{\sqrt[n]{n!}}=0;$

(5)  $\lim_{n\to\infty}\frac{n}{\sqrt[n]{n!}}=e;$

(6)  $\lim_{n\to\infty}\frac{1+\sqrt{2}+\sqrt[3]{3}+\cdots+\sqrt[n]{n}}{n}=1;$

(7) 若  $\lim_{n\to\infty}\frac{b_{n+1}}{b_n}=a(b_n>0)$ ，则  $\lim_{n\to\infty}\sqrt[n]{b_n}=a$ ;

(8) 若  $\lim_{n\to\infty}(a_{n}-a_{n-1})=d$  , 则  $\lim_{n\to\infty}\frac{a_{n}}{n}=d$ .

5. 证明:若 $\{a_{n}\}$ 为递增数列，$\{b_{n}\}$ 为递减数列，且

$$
\lim _ {n \to \infty} (a _ {n} - b _ {n}) = 0,
$$

则 $\lim_{n\to \infty}a_n$ 与 $\lim_{n\to \infty}b_n$ 都存在且相等.

6. 设数列 $\{a_{n}\}$ 满足: 存在正数 $M$, 对一切 $n$ 有

$$
A _ {n} = \left| a _ {2} - a _ {1} \right| + \left| a _ {3} - a _ {2} \right| + \dots + \left| a _ {n} - a _ {n - 1} \right| \leqslant M.
$$

证明: 数列  $\{a_{n}\}$  与  $\{A_{n}\}$  都收敛.

7. 设 $a > 0, \sigma > 0, a_{1} = \frac{1}{2}\left(a + \frac{\sigma}{a}\right), a_{n+1} = \frac{1}{2}\left(a_{n} + \frac{\sigma}{a_{n}}\right), n = 1, 2, \cdots$. 证明: 数列 $\{a_{n}\}$ 收敛, 且其极限为 $\sqrt{\sigma}$.

8. 设 $a_{1} > b_{1} > 0$ ，记

$$
a _ {n} = \frac {a _ {n - 1} + b _ {n - 1}}{2}, \quad b _ {n} = \frac {2 a _ {n - 1} b _ {n - 1}}{a _ {n - 1} + b _ {n - 1}}, n = 2, 3, \dots .
$$

证明:数列 $\{a_{n}\}$ 与 $\{b_n\}$ 的极限都存在且等于 $\sqrt{a_1b_1}$.

9. 按柯西收敛准则叙述数列 $\{a_{n}\}$ 发散的充要条件，并用它证明下列数列 $\{a_{n}\}$ 是发散的:

(1) $a_{n} = (-1)^{n}n$;

(2) $a_{n} = \sin \frac{n\pi}{2}$;

(3) $a_{n} = 1 + \frac{1}{2} +\dots +\frac{1}{n}.$

10. 设 $\lim_{n\to \infty}a_n = a, \lim_{n\to \infty}b_n = b.$ 记

$$
S _ {n} = \max \left\{a _ {n}, b _ {n} \right\}, T _ {n} = \min \left\{a _ {n}, b _ {n} \right\}, n = 1, 2, \dots .
$$

证明:（1） $\lim_{n\to \infty}S_n = \max \{a,b\}$ ；（2） $\lim_{n\to \infty}T_n = \min \{a,b\}$

提示:参考第一章总练习题1.

11. 设 $\{a_{n}\}$ 是无界数列，$\{b_{n}\}$ 是无穷大数列. 证明:$\{a_{n}b_{n}\}$ 必为无界数列.
12. 倘若  $\{a_{n}\},\{b_{n}\}$  都是无界数列, 试问  $\{a_{n}b_{n}\}$  是否必为无界数列?

(若是,需作证明;若否,需给出反例.)

![](images/page_50_image_13.jpg)

## 第二章综合自测题

## § 1 函数极限概念

## 一、 $x$ 趋于 $\infty$ 时函数的极限

设函数 $f$ 定义在 $[a, +\infty)$ 上，类似于数列情形，我们研究当自变量 $x$ 趋于 $+\infty$ 时，对应的函数值能否无限地接近于某个定数 $A$。例如，对于函数 $f(x) = \frac{1}{x}$，从图像上可见，当 $x$ 无限增大时，函数值无限地接近于0；而对于函数 $g(x) = \arctan x$，则当 $x$ 趋于 $+\infty$ 时函数值无限地接近于 $\frac{\pi}{2}$。我们称这两个函数当 $x$ 趋于 $+\infty$ 时有极限。一般地，当 $x$ 趋于 $+\infty$ 时函数极限的精确定义如下:

定义1 设 $f$ 为定义在 $[a, +\infty)$ 上的函数, $A$ 为定数. 若对任给的 $\varepsilon > 0$, 存在正数 $M (\geqslant a)$, 使得当 $x > M$ 时, 有

$$
\mid f (x) - A \mid <   \varepsilon ,
$$

则称函数 $f$ 当 $x$ 趋于 $+\infty$ 时以 $A$ 为极限，记作

$$
\lim _ {x \to + \infty} f (  x  ) = A \quad \text {或} \quad f (  x  ) \to A    (  x \to +   \infty  )  .
$$

在定义 1 中正数 M 的作用与数列极限定义中的 N 相类似, 表明 x 充分大的程度;

但这里所考虑的是比 $M$ 大的所有实数 $x$ ，而不仅仅是正整数 $n$ .因此，当 $x\to +\infty$ 时函数 $f$ 以 $A$ 为极限意味着: $A$ 的任意小邻域内必含有 $f$ 在 $+\infty$ 的某邻域上的全部函数值.

定义1的几何意义如图3-1所示,对任给的 $\varepsilon>0$ ,在坐标平面上平行于x轴的两条直线 $y=A+\varepsilon$ 与 $y=A-\varepsilon$ ,围成以直线y=A为中心线、宽为 $2\varepsilon$ 的带形区域;定义中的“当x>M时,有 $|f(x)-A|<\varepsilon$ ”表示:在直线x=M的右

![](images/page_51_chart_12.jpg)

<details>
<summary>contour</summary>

| Line Type | Description |
| --- | --- |
| Solid Curve | y=f(x) |
| Dashed Line | \(A\) |
| Shaded Area | \(y=f(x) \le A + \epsilon, A - \epsilon\) |
</details>

图3-1

方, 曲线  $y = f(x)$  全部落在这个带形区域之内. 如果正数  $\varepsilon$  给得小一点, 即当带形区域更窄一点时, 直线 x = M 一般要往右平移; 但无论带形区域如何窄, 总存在这样的正数 M, 使得曲线  $y = f(x)$  在直线 x = M 的右边部分全部落在这更窄的带形区域内.

现设 $f$ 为定义在 $U(-\infty)$ 或 $U(\infty)$ 上的函数，当 $x \to -\infty$ 或 $x \to \infty$ 时，若函数值 $f(x)$

能无限地接近某定数 $A$ ，则称 $f$ 当 $x\to -\infty$ 或 $x\to \infty$ 时以 $A$ 为极限，分别记作

$$
\lim _ {x \to - \infty} f (  x  ) = A \quad \text {或} \quad f (  x  ) \to A    (  x \to - \infty    )  ;
$$

$$
\lim _ {x \to \infty} f (  x  ) = A \quad {\text {或}} \quad f (  x  ) \to A    (  x \to \infty    ).
$$

这两种函数极限的精确定义与定义1相仿, 只需把定义1中的“x>M”分别改为“x<-M”或“|x|>M”即可.

读者不难证明: 若 f 为定义在  $U(\infty)$  上的函数, 则

$$
\lim _ {x \to \infty} f (x) = A \Longleftrightarrow \lim _ {x \to + \infty} f (x) = \lim _ {x \to - \infty} f (x) = A. \tag {1}
$$

例1 证明 $\lim_{x\to \infty}\frac{1}{x} = 0.$

证 任给 $\varepsilon > 0$，取 $M = \frac{1}{\varepsilon}$，则当 $|x| > M$ 时，有

$$
\left| \frac {1}{x} - 0 \right| = \frac {1}{| x |} <   \frac {1}{M} = \varepsilon ,
$$

所以  $\lim_{x\to\infty}\frac{1}{x}=0.$

□

例2 证明:1） $\lim_{x\to -\infty}\arctan x = -\frac{\pi}{2};$ 2） $\lim_{x\to +\infty}\arctan x = \frac{\pi}{2}.$

证 任给 $\varepsilon > 0$ ，由于

$$
\left| \arctan x - \left(- \frac {\pi}{2}\right) \right| <   \varepsilon \tag {2}
$$

等价于 $-\varepsilon - \frac{\pi}{2} < \arctan x < \varepsilon - \frac{\pi}{2}$, 而此不等式的左半部分对任何 $x$ 都成立, 所以只需考察其右半部分 $x$ 的变化范围. 为此, 先限制 $\varepsilon < \frac{\pi}{2}$, 则有

$$
x <   \tan \left(\varepsilon - \frac {\pi}{2}\right) = - \tan \left(\frac {\pi}{2} - \varepsilon\right).
$$

故对任给的正数 $\varepsilon \left(<\frac{\pi}{2}\right)$，只需取 $M = \tan \left(\frac{\pi}{2} - \varepsilon\right)$，则当 $x < -M$ 时，便有(2)式成立。这就证明了1).类似地可证2).

注 由例 2 可知, 当  $x \to \infty$  时  $\arctan x$  不存在极限.

## 二、 $x$ 趋于 $x_0$ 时函数的极限

设 $f$ 为定义在点 $x_0$ 的某个空心邻域 $U^{\circ}(x_0)$ 上的函数. 现在讨论当 $x$ 趋于 $x_0 (x \neq x_0)$ 时, 对应的函数值能否趋于某个定数 $A$. 这类函数极限的精确定义如下.

定义2（函数极限的 $\varepsilon -\delta$ 定义）设函数 $f$ 在点 $x_0$ 的某个空心邻域 $U^{\circ}(x_0;\delta ')$ 内有定义，$A$ 为定数.若对任给的 $\varepsilon >0$ ，存在正数 $\delta (<\delta ')$ ，使得当 $0 < |x - x_0| < \delta$ 时，有

$$
\mid f (x) - A \mid <   \varepsilon ,
$$

则称函数 $f$ 当 $x$ 趋于 $x_0$ 时以 $A$ 为极限，记作

$$
\lim _ {x \to x _ {0}} f (  x  ) = A \quad \text {或} \quad f (  x  ) \to A    (  x \to x _ {0}  ).
$$

下面我们举例说明如何应用 $\varepsilon -\delta$ 定义来验证这种类型的函数极限.请读者特别注意以下各例中 $\delta$ 的值是怎样确定的.

例3 设 $f(x) = \frac{x^2 - 4}{x - 2}$，证明 $\lim_{x \to 2} f(x) = 4$.

证 由于当 $x \neq 2$ 时，

$$
\mid f (x) - 4 \mid = \left| \frac {x ^ {2} - 4}{x - 2} - 4 \right| = \mid x + 2 - 4 \mid = \mid x - 2 \mid ,
$$

故对给定的 $\varepsilon > 0$，只要取 $\delta = \varepsilon$，则当 $0 < |x - 2| < \delta$ 时，有 $|f(x) - 4| < \varepsilon$. 这就证明了 $\lim_{x \to 2} f(x) = 4$.

例 4 证明:1)  $\lim_{x\to x_{0}}\sin x=\sin x_{0}$ ; 2)  $\lim_{x\to x_{0}}\cos x=\cos x_{0}$ .

证 先建立一个不等式: 当  $0 < x < \frac{\pi}{2}$  时, 有

$$
\sin x <   x <   \tan x. \tag {3}
$$

事实上,在如图 3-2 的单位圆内,当  $0 < x < \frac{\pi}{2}$  时,若用 S 表示面积,显然有

$$
S _ {_ {\triangle O A D}} <   S _ {_ {\text {扇形} O A D}} <   S _ {_ {\triangle O A B}},
$$

即 $\frac{1}{2}\sin x<\frac{1}{2}x<\frac{1}{2}\tan x$ ，由此立得(3)式.

又当 $x \geqslant \frac{\pi}{2}$ 时, 有 $\sin x \leqslant 1 < x$, 故对一切 $x > 0$, 都有 $\sin x < x$; 当 $x < 0$ 时, 由 $\sin(-x) < -x$ 得 $-\sin x < -x$. 综上, 我们又得到不等式

$$
\mid \sin x \mid \leqslant \mid x \mid , x \in \mathbf {R}, \tag {4}
$$

其中等号仅当 $x = 0$ 时成立.

现证1). 由(4)式得

$$
\left| \sin x - \sin x _ {0} \right| = 2 \left| \cos \frac {x + x _ {0}}{2} \right| \left| \sin \frac {x - x _ {0}}{2} \right| \leqslant \left| x - x _ {0} \right|.
$$

对任给的 $\varepsilon > 0$，只要取 $\delta = \varepsilon$，则当 $0 < |x - x_0| < \delta$ 时，就有

$$
\left| \sin x - \sin x _ {0} \right| <   \varepsilon .
$$

所以 $\lim_{x\to x_0}\sin x = \sin x_0$ 2）的证明留给读者作为练习.

例 5 证明  $\lim_{x\to1}\frac{x^{2}-1}{2x^{2}-x-1}=\frac{2}{3}$ .

证 当 $x \neq 1$ 时, 有

$$
\left| \frac {x ^ {2} - 1}{2 x ^ {2} - x - 1} - \frac {2}{3} \right| = \left| \frac {x + 1}{2 x + 1} - \frac {2}{3} \right| = \frac {\mid x - 1 \mid}{3 \mid 2 x + 1 \mid}.
$$

若限制 $x$ 于 $0 < |x - 1| < 1$ （此时 $x > 0$），则 $|2x + 1| > 1$. 于是，对任给的 $\varepsilon > 0$，只要取 $\delta = \min \{3\varepsilon, 1\}$，则当 $0 < |x - 1| < \delta$ 时，便有

$$
\left| \frac {x ^ {2} - 1}{2 x ^ {2} - x - 1} - \frac {2}{3} \right| <   \frac {\mid x - 1 \mid}{3} <   \varepsilon .
$$

![](images/page_53_image_25.jpg)

<details>
<summary>text_image</summary>

D
B
x
O
C
A
</details>

图3-2

例6 证明 $\lim_{x\to x_0}\sqrt{1 - x^2} = \sqrt{1 - x_0^2}$ （ $|x_0| <   1$ ）.

证 由于 $|x| \leqslant 1, |x_0| < 1$，因此

$$
\begin{array}{l} \mid \sqrt {1 - x ^ {2}} - \sqrt {1 - x _ {0} ^ {2}} \mid = \frac {\mid x _ {0} ^ {2} - x ^ {2} \mid}{\sqrt {1 - x ^ {2}} + \sqrt {1 - x _ {0} ^ {2}}} \\ \leqslant \frac {\left| x + x _ {0} \right| \left| x - x _ {0} \right|}{\sqrt {1 - x _ {0} ^ {2}}} \leqslant \frac {2 \left| x - x _ {0} \right|}{\sqrt {1 - x _ {0} ^ {2}}}. \\ \end{array}
$$

于是，对任给的 $\varepsilon > 0$ （不妨设 $0 < \varepsilon < 1$），取

$$
\delta = \min \left\{\mid x _ {0} - 1 \mid , \mid x _ {0} + 1 \mid , \frac {\sqrt {1 - x _ {0} ^ {2}}}{2} \varepsilon \right\},
$$

则当 $0 < |x - x_0| < \delta$ 时，就有 $|\sqrt{1 - x^2} -\sqrt{1 - x_0^2}| < \varepsilon.$

应用 $\varepsilon -\delta$ 定义还立刻可得

$$
\lim _ {x \to x _ {0}} c = c, \lim _ {x \to x _ {0}} x = x _ {0},
$$

这里 c 为常数, $x_{0}$  为给定实数.

通过以上各个例子,读者对函数极限的  $\varepsilon-\delta$  定义应能体会到下面几点:

1. 定义2中的正数 $\delta$, 相当于数列极限 $\varepsilon - N$ 定义中的 $N$, 它依赖于 $\varepsilon$, 但也不是由 $\varepsilon$ 所唯一确定的. 一般来说, $\varepsilon$ 愈小, $\delta$ 也相应地要小一些, 而且把 $\delta$ 取得更小些也无妨. 如在例3中可取 $\delta = \frac{\varepsilon}{2}$ 或 $\delta = \frac{\varepsilon}{3}$, 等等.
2. 定义中只要求函数 $f$ 在 $x_0$ 的某一空心邻域上有定义，而一般不考虑 $f$ 在点 $x_0$ 处的函数值是否有定义，或者取什么值。这是因为，对于函数极限我们所研究的是当 $x$ 趋于 $x_0$ 过程中函数值的变化趋势。如在例3中，函数 $f$ 在点 $x = 2$ 是没有定义的，但当 $x \to 2$ 时 $f$ 的函数值趋于一个定数。
3. 定义2中的不等式 $0 < |x - x_0| < \delta$ 等价于 $x \in U^{\circ}(x_0; \delta)$，而不等式 $|f(x) - A| < \varepsilon$ 等价于 $f(x) \in U(A; \varepsilon)$. 于是，$\varepsilon - \delta$ 定义又可写成

任给 $\varepsilon > 0$，存在 $\delta > 0$，使得对一切 $x \in U^{\circ}(x_0; \delta)$，有 $f(x) \in U(A; \varepsilon)$.

或更简单地表述为

任给 $\varepsilon > 0$，存在 $\delta > 0$，使得 $f(U^{\circ}(x_0; \delta)) \subset U(A; \varepsilon)$.

4. $\varepsilon -\delta$ 定义的几何意义如图3-3所示.对任给的 $\varepsilon >0$ ，在坐标平面上画一条以直线 $y = A$ 为中心线、宽为 $2\varepsilon$ 的横带，则必存在以直线 $x = x_0$ 为中心线、宽为 $2\delta$ 的竖带，使函数 $y = f(x)$ 的图像在该竖带中的部分全部落在横带内，但点 $(x_0,f(x_0))$ 可能例外（或无意义）.

下面我们讨论单侧极限.

![](images/page_54_chart_20.jpg)

<details>
<summary>area</summary>

| Feature | Value |
| --- | --- |
| Lower bound (x₀ - \(\delta)\) | \(A - \epsilon\) |
| Upper bound (x₀ + \(\delta)\) | \(A + \epsilon\) |
| Point on curve at x₀ | \(x_{0}\) |
| Point on curve above x₀ | \(x_{0} + \delta\) |
</details>

图3-3

有些函数在其定义域上某些点左侧与右侧的解析

式不同(如分段函数定义域上的某些点),或函数在某些点仅在其一侧有定义(如在定义区间端点处),这时函数在那些点上的极限只能单侧地给出定义.

例如,函数

$$
f (x) = \left\{ \begin{array}{l l} x ^ {2}, & x \geqslant 0, \\ x, & x <   0 \end{array} \right. \tag {5}
$$

当 $x > 0$ 而趋于0时，应按 $f(x) = x^{2}$ 来考察函数值的变化趋势；当 $x < 0$ 而趋于0时，则应按 $f(x) = x$ 来考察.又如函数 $\sqrt{1 - x^2}$ 在其定义区间[-1,1]端点 $x = \pm 1$ 处的极限，也只能在点 $x = -1$ 的右侧和点 $x = 1$ 的左侧来分别讨论.

定义3 设函数 $f$ 在 $U_{+}^{\circ}(x_0; \delta')$ （或 $U_{-}^{\circ}(x_0; \delta')$）上有定义，$A$ 为定数。若对任给的 $\varepsilon > 0$，存在正数 $\delta (< \delta')$，使得当 $x_0 < x < x_0 + \delta$（或 $x_0 - \delta < x < x_0$）时，有

$$
\mid f (x) - A \mid <   \varepsilon ,
$$

则称数 A 为函数 f 当 x 趋于  $x_{0}^{+}$  (或  $x_{0}^{-}$ ) 时的右(左)极限, 记作

$$
\lim _ {x \to x _ {0} ^ {+}} f (x) = A \left(\lim _ {x \to x _ {0} ^ {-}} f (x) = A\right)
$$

或

$$
f (x) \rightarrow A (x \rightarrow x _ {0} ^ {+}) (f (x) \rightarrow A (x \rightarrow x _ {0} ^ {-})).
$$

右极限与左极限统称为单侧极限. $f$ 在点 $x_0$ 的右极限与左极限又分别记为

$$
f (  x _ {0} + 0  ) = \lim _ {x \to x _ {0} ^ {+}} f (  x  ) \quad \text {与} \quad f (  x _ {0} - 0  ) = \lim _ {x \to x _ {0} ^ {-}} f (  x  ).
$$

按定义3容易验证函数(5)在 $x = 0$ 处的左、右极限分别为

$$
f (0 - 0) = \lim _ {x \to 0 ^ {-}} f (x) = \lim _ {x \to 0 ^ {-}} x = 0,
$$

$$
f (0 + 0) = \lim _ {x \to 0 ^ {+}} f (x) = \lim _ {x \to 0 ^ {+}} x ^ {2} = 0.
$$

同样还可验证符号函数 $\operatorname{sgn} x$ 在 $x = 0$ 处的左、右极限分别为

$$
\operatorname * {l i m s g n} _ {x \to 0 ^ {-}} x = \lim _ {x \to 0 ^ {-}} (- 1) = - 1, \lim _ {x \to 0 ^ {+}} \operatorname * {s g n} _ {x} = \lim _ {x \to 0 ^ {+}} 1 = 1.
$$

例7 讨论函数 $\sqrt{1 - x^2}$ 在定义区间端点 $\pm 1$ 处的单侧极限.

解 由于 $|x| \leqslant 1$ ，故有

$$
1 - x ^ {2} = (1 + x) (1 - x) \leqslant 2 (1 - x).
$$

任给 $0 < \varepsilon < 1$ ，当 $2(1 - x) < \varepsilon^2$ 时，就有

$$
\sqrt {1 - x ^ {2}} <   \varepsilon . \tag {6}
$$

于是取 $\delta = \frac{\varepsilon^2}{2}$，则当 $0 < 1 - x < \delta$ 即 $1 - \delta < x < 1$ 时，(6)式成立.这就推出 $\lim_{x\to 1^{-}}\sqrt{1 - x^2} = 0.$ 类似地可得 $\lim_{x\to (-1)^+}\sqrt{1 - x^2} = 0.$

关于函数极限 $\lim_{x\to x_0}f(x)$ 与相应的左、右极限之间的关系，有下述定理:

定理3.1 $\lim_{x\to x_0}f(x) = A\Leftrightarrow \lim_{x\to x_0^+}f(x) = \lim_{x\to x_0^-}f(x) = A.$

这个定理的证明留给读者.

应用定理 3.1, 除了可验证函数极限的存在 (如对函数 (3) 有  $\lim_{x\to0}f(x)=0$ ), 还常可说明某些函数极限的不存在, 如前面提到的符号函数 sgn x, 由于它在 x=0 处的左、右极限不相等, 所以  $\lim_{x\to0}\operatorname{sgn}x$  不存在.

## 习题 3.1

1. 按定义证明下列极限:

(1)  $\lim_{x\to+\infty}\frac{6x+5}{x}=6;$

(2)  $\lim_{x\to2}(x^{2}-6x+10)=2;$

(3)  $\lim_{x\to\infty}\frac{x^{2}-5}{x^{2}-1}=1;$

(4)  $\lim_{x\to2^{-}}\sqrt{4-x^{2}}=0;$

(5)  $\lim_{x\to x_{0}}\cos x=\cos x_{0}.$

2. 根据定义 2 叙述  $\lim_{x\to x_{0}}f(x)\neq A$ .

3. 设 $\lim_{x\to x_0}f(x) = A$ ，证明 $\lim_{h\to 0}f(x_0 + h) = A.$

4. 证明:若 $\lim_{x\to x_0}f(x) = A$ ，则 $\lim_{x\to x_0}|f(x)| = |A|$ .当且仅当 $A$ 为何值时反之也成立？

5. 证明定理 3.1.

6. 讨论下列函数在  $x \rightarrow 0$  时的极限或左、右极限:

(1)  $f(x) = \frac{|x|}{x}$ ;

(2) $f(x) = [x]$;

(3) $f(x) = \left\{ \begin{array}{ll}2^{x}, & x > 0,\\ 0, & x = 0,\\ 1 + x^{2}, & x <   0. \end{array} \right.$

7. 设 $\lim_{x\to +\infty}f(x) = A$ ，证明 $\lim_{x\to 0^{+}}f\left(\frac{1}{x}\right) = A.$

8. 证明:对黎曼函数 $R(x)$ 有 $\lim_{x\to x_0}R(x) = 0, x_0 \in [0,1]$ （当 $x_0 = 0$ 或1时，考虑单侧极限）.

## § 2 函数极限的性质

在 §1 中我们引入了下述六种类型的函数极限:

1)  $\lim_{x\to+\infty}f(x)$ ;

2)  $\lim_{x\to-\infty}f(x)$ ;

3)  $\lim_{x\to\infty}f(x)$ ;

4)  $\lim_{x\to x_{0}}f(x)$ ;

5) $\lim_{x\to x_0^+}f(x)$;

6) $\lim_{x\to x_0^-}f(x)$

它们具有与数列极限相类似的一些性质,下面以第4)种类型的极限为代表来叙述并证明这些性质.至于其他类型极限的性质及其证明,只要相应地做些修改即可.

定理 3.2(唯一性) 若极限  $\lim_{x\to x_{0}}f(x)$  存在, 则此极限是唯一的.

证 设 A, B 都是 f 当  $x \to x_{0}$  时的极限, 则对任给的  $\varepsilon > 0$ , 分别存在正数  $\delta_{1}$  与  $\delta_{2}$ , 使得当  $0 < |x - x_{0}| < \delta_{1}$  时, 有

$$
\left| f (x) - A \right| <   \varepsilon , \tag {1}
$$

当 $0 < |x - x_0| < \delta_2$ 时，有

$$
\mid f (x) - B \mid <   \varepsilon . \tag {2}
$$

取  $\delta=\min(\delta_{1},\delta_{2})$ ，则当  $0<|x-x_{0}|<\delta$  时，(1)式与(2)式同时成立，故有

$$
\begin{array}{l} \mid A - B \mid = \mid (f (x) - A) - (f (x) - B) \mid \\ \leqslant \left| f (x) - A \right| + \left| f (x) - B \right| <   2 \varepsilon . \\ \end{array}
$$

由  $\varepsilon$  的任意性得 A = B. 这就证明了极限是唯一的.

定理3.3（局部有界性）若 $\lim_{x\to x_0}f(x)$ 存在，则 $f$ 在 $x_0$ 的某空心邻域 $U^{\circ}(x_0)$ 上有界.

证 设 $\lim_{x\to x_0}f(x) = A.$ 取 $\varepsilon = 1$ ，则存在 $\delta >0$ ，使得对一切 $x\in U^{\circ}(x_0;\delta)$ ，有

$$
\mid f (x) - A \mid <   1 \Rightarrow \mid f (x) \mid <   \mid A \mid + 1.
$$

这就证明了 $f$ 在 $U^{\circ}(x_0;\delta)$ 上有界.

定理3.4（局部保号性）若 $\lim_{x\to x_0}f(x) = A > 0$ （或 $<  0$ ，则对任何正数 $r <   A$ （或 $r <   - A$ ），存在 $U^{\circ}(x_0)$ ，使得对一切 $x\in U^{\circ}(x_0)$ ，有

$$
f (x) > r > 0 (\text {或} f (x) <   - r <   0).
$$

证 设 $A > 0$ ，对任何 $r \in (0, A)$，取 $\varepsilon = A - r$，则存在 $\delta > 0$，使得对一切 $x \in U^{\circ}(x_0; \delta)$，有

$$
f (x) > A - \varepsilon = r,
$$

这就证得结论.对于 A<0 的情形可类似地证明.

注 在以后应用局部保号性时, 常取  $r=\frac{A}{2}$ .

定理3.5（保不等式性）设 $\lim_{x\to x_0}f(x)$ 与 $\lim_{x\to x_0}g(x)$ 都存在，且在某邻域 $U^{\circ}(x_0;\delta ')$ 上有 $f(x)\leqslant g(x)$，则

$$
\lim _ {x \to x _ {0}} f (x) \leqslant \lim _ {x \to x _ {0}} g (x). \tag {3}
$$

证 设 $\lim_{x\to x_0}f(x) = A,\lim_{x\to x_0}g(x) = B$ ，则对任给的 $\varepsilon >0$ ，分别存在正数 $\delta_1$ 与 $\delta_{2}$ ，使得当$0 <   |x - x_0| <   \delta_1$ 时，有

$$
A - \varepsilon <   f (x), \tag {4}
$$

当 $0 < |x - x_0| < \delta_2$ 时，有

$$
g (x) <   B + \varepsilon . \tag {5}
$$

令  $\delta=\min\left\{\delta',\delta_{1},\delta_{2}\right\}$ ，则当  $0<\left|x-x_{0}\right|<\delta$  时，不等式  $f(x)\leqslant g(x)$  与（4）、（5）两式同时成立，于是有

$$
A - \varepsilon <   f (x) \leqslant g (x) <   B + \varepsilon ,
$$

从而 $A < B + 2\varepsilon$. 由 $\varepsilon$ 的任意性推出 $A \leqslant B$, 即 (3) 式成立.

定理3.6（迫敛性）设 $\lim_{x\to x_0}f(x) = \lim_{x\to x_0}g(x) = A$ ，且在某 $U^{\circ}(x_0;\delta ')$ 上有

$$
f (x) \leqslant h (x) \leqslant g (x), \tag {6}
$$

则 $\lim_{x\to x_0}h(x) = A.$

证 按假设,对任给的  $\varepsilon>0$ , 分别存在正数  $\delta_{1}$  与  $\delta_{2}$ , 使得当  $0<\left|x-x_{0}\right|<\delta_{1}$  时, 有

$$
A - \varepsilon <   f (x), \tag {7}
$$

当 $0 < |x - x_0| < \delta_2$ 时，有

$$
g (x) <   A + \varepsilon . \tag {8}
$$

令  $\delta=\min\left\{\delta',\delta_{1},\delta_{2}\right\}$ ，则当  $0<\left|x-x_{0}\right|<\delta$  时，不等式(6)、(7)、(8)同时成立，故有

$$
A - \varepsilon <   f (x) \leqslant h (x) \leqslant g (x) <   A + \varepsilon ,
$$

由此得 $|h(x) - A| < \varepsilon$，所以 $\lim_{x \to x_0} h(x) = A$.

定理3.7（四则运算法则）若极限 $\lim_{x\to x_0}f(x)$ 与 $\lim_{x\to x_0}g(x)$ 都存在，则函数 $f\pm g,f\cdot g$ 当$x\to x_0$ 时极限也存在，且

1)  $\lim_{x\to x_{0}}\left[f(x)\pm g(x)\right]=\lim_{x\to x_{0}}f(x)\pm\lim_{x\to x_{0}}g(x)$ ;
2)  $\lim_{x\to x_{0}}\left[f(x)g(x)\right]=\lim_{x\to x_{0}}f(x)\cdot\lim_{x\to x_{0}}g(x)$ ;

又若 $\lim_{x\to x_0}g(x)\neq 0$ ，则 $f / g$ 当 $x\to x_0$ 时极限存在，且有

3) $\lim_{x\to x_0}\frac{f(x)}{g(x)} = \lim_{x\to x_0}f(x)\Big / \lim_{x\to x_0}g(x).$

这个定理的证明类似于数列极限中的相应定理,留给读者作为练习.

利用函数极限的迫敛性与四则运算法则,我们可从一些简单的函数极限出发,计算较复杂的函数极限.

例 1 求  $\lim_{x\to0}x\left[\frac{1}{x}\right]$ .

解 由第一章 §3 习题 12, 当 x > 0 时, 有

$$
1 - x <   x \left[ \frac {1}{x} \right] \leqslant 1,
$$

而 $\lim_{x\to 0^{+}}(1 - x) = 1$ ，故由迫敛性得

$$
\lim _ {x \to 0 ^ {+}} x \left[ \frac {1}{x} \right] = 1.
$$

另一方面，当 $x < 0$ 时，有 $1 \leqslant x\left[\frac{1}{x}\right] < 1 - x$ ，故由迫敛性又可得

$$
\lim _ {x \to 0 ^ {-}} x \left[ \frac {1}{x} \right] = 1.
$$

综上,我们求得  $\lim_{x\to0}x\left[\frac{1}{x}\right]=1.$

例 2 求  $\lim_{x\to\frac{\pi}{4}}(x\tan x-1)$ .

解 由 $x \tan x = x \frac{\sin x}{\cos x}$ 及 §1 例4 所得的

$$
\lim _ {x \to \frac {\pi}{4}} x = \sin \frac {\pi}{4} = \frac {\sqrt {2}}{2} = \lim _ {x \to \frac {\pi}{4}} \cos x,
$$

并按四则运算法则有

$$
\lim _ {x \to \frac {\pi}{4}} (x \tan x - 1) = \lim _ {x \to \frac {\pi}{4}} x \cdot \frac {\lim _ {x \to \frac {\pi}{4}} \sin x}{\lim _ {x \to \frac {\pi}{4}} \cos x} - \lim _ {x \to \frac {\pi}{4}} 1 = \frac {\pi}{4} - 1.
$$

例3 求极限 $\lim_{x\to 1}\frac{1 + x + \cdots + x^n - n - 1}{x - 1}$

解 对任意正整数 $k$ ，当 $x \neq 1$ 时，有

$$
\frac {x ^ {k} - 1}{x - 1} = \frac {(x - 1) (1 + x + \cdots + x ^ {k - 1})}{x - 1} = 1 + x + \dots + x ^ {k - 1},
$$

故 $\lim_{x\to 1}\frac{1 + x + \cdots + x^n - n - 1}{x - 1} = \lim_{x\to 1}\sum_{k = 1}^{n}\frac{x^k - 1}{x - 1}$

$$
= \sum_ {k = 1} ^ {n} \lim _ {x \to 1} (1 + x + \dots + x ^ {k - 1}) = \sum_ {k = 1} ^ {n} k = \frac {n (n + 1)}{2}.
$$

例 4 证明  $\lim_{x\to0}a^{x}=1\quad(a>1)$ .

证 任给 $\varepsilon > 0$，因为 $\lim_{n \to \infty} a^{\frac{1}{n}} = 1, \lim_{n \to \infty} a^{-\frac{1}{n}} = 1$，所以存在 $N$，使得

$$
a ^ {\frac {1}{N}} - 1 <   \varepsilon , \quad 1 - a ^ {- \frac {1}{N}} <   \varepsilon .
$$

取  $\delta=\frac{1}{N}$ ，当  $0<|x|<\delta$  时，

$$
- \varepsilon <   a ^ {- \frac {1}{N}} - 1 <   a ^ {x} - 1 <   a ^ {\frac {1}{N}} - 1 <   \varepsilon ,
$$

即 $|a^x - 1| < \varepsilon$，从而 $\lim_{x \to 0} a^x = 1$.

## 习题 3.2

1. 求下列极限:

(1)  $\lim_{x\to\frac{\pi}{2}}2(\sin x-\cos x-x^{2})$ ;
(3)  $\lim_{x\to1}\frac{x^{2}-1}{2x^{2}-x-1}$ ;
(5) $\lim_{x\to 1}\frac{x^n - 1}{x^m - 1}$ ($n,m$ 为正整数);
(7)  $\lim_{x\to0}\frac{\sqrt{a^{2}+x}-a}{x}$  (a>0);

(2)  $\lim_{x\to0}\frac{x^{2}-1}{2x^{2}-x-1}$ ;
(4)  $\lim_{x\to0}\frac{(x-1)^{3}+(1-3x)}{x^{2}+2x^{3}}$ ;
(6)  $\lim_{x\to4}\frac{\sqrt{1+2x}-3}{\sqrt{x}-2}$ ;
(8) $\lim_{x\to +\infty}\frac{(3x + 6)^{70}(8x - 5)^{20}}{(5x - 1)^{90}}.$

2. 利用迫敛性求极限:

(1)  $\lim_{x\to-\infty}\frac{x-\cos x}{x};$  (2)  $\lim_{x\to+\infty}\frac{x\sin x}{x^{2}-4}.$

3. 设  $\lim_{x\to x_{0}}f(x)=A,\lim_{x\to x_{0}}g(x)=B.$  证明:

(1)  $\lim_{x\to x_{0}}\left[f(x)\pm g(x)\right]=A\pm B;$
(2)  $\lim_{x\to x_{0}}\left[f(x)g(x)\right]=AB;$
(3) $\lim_{x\to x_0}\frac{f(x)}{g(x)} = \frac{A}{B}$ (当 $B\neq 0$ 时).

4. 设

$$
f (x) = \frac {a _ {0} x ^ {m} + a _ {1} x ^ {m - 1} + \cdots + a _ {m - 1} x + a _ {m}}{b _ {0} x ^ {n} + b _ {1} x ^ {n - 1} + \cdots + b _ {n - 1} x + b _ {n}}, a _ {0} \neq 0, b _ {0} \neq 0, m \leqslant n,
$$

试求  $\lim_{x\to+\infty}f(x)$ .

5. 设 $f(x) > 0, \lim_{x \to x_0} f(x) = A$. 证明

$$
\lim _ {x \to x _ {0}} \sqrt [ n ]{f (x)} = \sqrt [ n ]{A},
$$

其中  $n \geqslant 2$  为正整数.

6. 证明 $\lim_{x\to 0}a^x = 1(0 <   a <   1)$

7. 设  $\lim_{x\to x_{0}}f(x)=A,\lim_{x\to x_{0}}g(x)=B.$

(1) 若在某  $U^{\circ}(x_{0})$  上有  $f(x) < g(x)$ ，问是否必有 A < B？为什么？
(2) 证明: 若 A > B, 则在某  $U^{\circ}(x_{0})$  上有  $f(x) > g(x)$ .

8. 求下列极限(其中 n 皆为正整数):

(1)  $\lim_{x\to0^{-}}\frac{|x|}{x}\frac{1}{1+x^{n}};$
(2) $\lim_{x\to 0^{+}}\frac{|x|}{x}\frac{1}{1 + x^n};$
(3)  $\lim_{x\to-1}\left(\frac{1}{x+1}-\frac{3}{x^{3}+1}\right)$ ;
(4)  $\lim_{x\to0}\frac{\sqrt[n]{1+x}-1}{x}$ ;
(5)  $\lim_{x\to\infty}\frac{[x]}{x}$  (提示: 参照例 1).

9.（1）证明:若 $\lim_{x\to 0}f(x^3)$ 存在，则 $\lim_{x\to 0}f(x) = \lim_{x\to 0}f(x^3)$

(2) 若  $\lim_{x\to0}f(x^{2})$  存在, 试问是否成立  $\lim_{x\to0}f(x)=\lim_{x\to0}f(x^{2})$ ?

## § 3 函数极限存在的条件

与讨论数列极限存在的条件一样,我们将从函数值的变化趋势来判断其极限的存在性.下面的定理只对  $x \rightarrow x_{0}$  这种类型的函数极限进行论述,但其结论对其他类型的函数极限也是成立的.下述归结原则有时称为海涅(Heine)定理.

定理3.8（归结原则）设 $f$ 在 $U^{\circ}(x_0;\delta ')$ 上有定义. $\lim_{x\to x_0}f(x)$ 存在的充要条件是:对任何含于 $U^{\circ}(x_0;\delta ')$ 且以 $x_0$ 为极限的数列 $\{x_n\}$，极限 $\lim_{n\to \infty}f(x_n)$ 都存在且相等.

证 必要性 设 $\lim_{x\to x_0}f(x) = A$ ，则对任给的 $\varepsilon >0$ ，存在正数 $\delta (\leqslant \delta ')$ ，使得当$0 <   |x - x_0| <   \delta$ 时，有 $|f(x) - A| <   \varepsilon .$

另一方面，设数列 $\{x_{n}\} \subset U^{\circ}(x_{0};\delta^{\prime})$ 且 $\lim_{n\to \infty}x_n = x_0$ ，则对上述的 $\delta >0$ ，存在 $N > 0$ ，使得当 $n > N$ 时，有 $0 <   |x_{n} - x_{0}| <   \delta$ ，从而有 $|f(x_n) - A| <   \varepsilon .$ 这就证明了 $\lim_{n\to \infty}f(x_n) = A.$

充分性 设对任何数列  $\{x_{n}\}\subset U^{\circ}(x_{0};\delta^{\prime})$  且  $\lim_{n\to\infty}x_{n}=x_{0}$ ，有  $\lim_{n\to\infty}f(x_{n})=A$ ，则可用反证法推出  $\lim_{x\to x_{0}}f(x)=A$ 。事实上，倘若当  $x\to x_{0}$  时 f 不以 A 为极限，则存在某  $\varepsilon_{0}>0$ ，对任何  $\delta>0$ （不论多么小），总存在一点 x，尽管  $0<|x-x_{0}|<\delta$ ，但有  $|f(x)-A|\geqslant\varepsilon_{0}$ （§1习题2）。现依次取  $\delta=\delta^{\prime},\frac{\delta^{\prime}}{2},\frac{\delta^{\prime}}{3},\cdots,\frac{\delta^{\prime}}{n},\cdots$ ，则存在相应的点  $x_{1},x_{2},x_{3},\cdots,x_{n},\cdots$ ，使得

$$
0 <   \mid x _ {n} - x _ {0} \mid <   \frac {\delta^ {\prime}}{n}, \text {而} \mid f (x _ {n}) - A \mid \geqslant \varepsilon_ {0}, n = 1, 2, \dots .
$$

显然数列 $\{x_{n}\} \subset U^{\circ}(x_{0};\delta^{\prime})$ 且 $\lim_{n\to \infty}x_n = x_0$ ，但当 $n\to \infty$ 时 $f(x_{n})$ 不趋于 $A.$ 这与假设相矛盾，

所以必有 $\lim_{x\to x_{0}}f(x)=A.$

![](images/page_61_image_2.jpg)

注1 归结原则也可简述为:

$$
\lim _ {x \to x _ {0}} f (  x  ) = A \Leftrightarrow \text {对任何}   x _ {_ n} \to x _ {0} (  n \to \infty  )   \text {有} \lim _ {n \to \infty} f (  x _ {_ n}  ) = A.
$$

注2 若可找到一个以 $x_0$ 为极限的数列 $\{x_n\}$, 使 $\lim_{n\to \infty}f(x_n)$ 不存在, 或找到两个都以 $x_0$ 为极限的数列 $\{x_n'\}$ 与 $\{x_n''\}$, 使 $\lim_{n\to \infty}f(x_n')$ 与 $\lim_{n\to \infty}f(x_n'')$ 都存在而不相等, 则 $\lim_{x\to x_0}f(x)$ 不存在.

例 1 证明极限 $\lim_{x\to0}\sin\frac{1}{x}$ 不存在.

证 设  $x_{n}^{\prime}=\frac{1}{n\pi},x_{n}^{\prime\prime}=\frac{1}{2n\pi+\frac{\pi}{2}}\quad(n=1,2,\cdots)$ ，则显

然有

$$
\begin{array}{l} x _ {n} ^ {\prime} \rightarrow 0, x _ {n} ^ {\prime \prime} \rightarrow 0 (n \rightarrow \infty), \\ \sin \frac {1}{x _ {n} ^ {\prime}} = 0 \rightarrow 0, \sin \frac {1}{x _ {n} ^ {\prime \prime}} = 1 \rightarrow 1 (n \rightarrow \infty). \\ \end{array}
$$

故由归结原则即得结论.

![](images/page_61_chart_11.jpg)

<details>
<summary>contour</summary>

| X | Y |
| --- | --- |
| \(-2\pi\) | ~-0.5 |
| 0 | 1 |
| \(2\pi\) | ~0.8 |
</details>

图3-4

函数  $y=\sin\frac{1}{x}$  的图像如图 3-4 所示. 由图像可见,

当  $x \to 0$  时, 其函数值无限次地在 -1 与 1 的范围内振荡, 而不趋于任何确定的数.

归结原则的意义在于把函数极限归结为数列极限问题来处理.从而,我们能应用归结原则和数列极限的有关性质来证明上一节中所述的函数极限的所有性质.

对于 $x \to x_0^+$, $x \to x_0^-$, $x \to +\infty$ 和 $x \to -\infty$ 这四种类型的单侧极限, 相应的归结原则可表示为更强的形式. 现以 $x \to x_0^+$ 这种类型为例阐述如下:

定理3.9 设函数 $f$ 在点 $x_0$ 的某空心右邻域 $U_{+}^{\circ}(x_0)$ 有定义. $\lim_{x\to x_0^\circ}f(x) = A$ 的充要条件是:对任何以 $x_0$ 为极限的递减数列 $\{x_n\} \subset U_{+}^{\circ}(x_0)$，有 $\lim_{n\to \infty}f(x_n) = A$.

这个定理的证明可仿照定理3.8进行,但在运用反证法证明充分性时,对 $\delta$ 的取法要作适当的修改,以保证所找到的数列 $\{x_{n}\}$ 能递减地趋于 $x_{0}$ .证明的细节留给读者作为练习.

相应于数列极限的单调有界定理,关于上述四类单侧极限也有相应的定理.现以 $x\to x_{0}^{+}$ 这种类型为例叙述如下.

定理3.10 设 $f$ 为定义在 $U_{+}^{\circ}(x_0)$ 上的单调有界函数，则右极限 $\lim_{x\to x_0^+}f(x)$ 存在.

证 不妨设 $f$ 在 $U_{+}^{\circ}(x_0)$ 上递增. 因 $f$ 在 $U_{+}^{\circ}(x_0)$ 上有界, 由确界原理, $\inf_{x \in U_{+}^{\circ}(x_0)} f(x)$ 存在, 记为 $A$. 下证 $\lim_{x \to x_0^+} f(x) = A$.

事实上，任给 $\varepsilon > 0$ ，按下确界定义，存在 $x' \in U_{+}^{\circ}(x_0)$，使得 $f(x') < A + \varepsilon$。取 $\delta = x' - x_0 > 0$，则由 $f$ 的递增性，对一切 $x \in (x_0, x') = U_{+}^{\circ}(x_0; \delta)$，有

$$
f (x) \leqslant f (x ^ {\prime}) <   A + \varepsilon .
$$

另一方面，由 $A \leqslant f(x)$，更有 $A - \varepsilon < f(x)$. 从而对一切 $x \in U_{+}^{\circ}(x_{0}; \delta)$，有

$$
A - \varepsilon <   f (x) <   A + \varepsilon ,
$$

这就证得 $\lim_{x\to x_{0}^{+}}f(x)=A.$

最后,我们叙述并证明关于函数极限的柯西准则.

定理3.11（柯西准则）设函数 $f$ 在 $U^{\circ}(x_0;\delta ')$ 上有定义. $\lim_{x\to x_0}f(x)$ 存在的充要条件是:任给 $\varepsilon >0$ ，存在正数 $\delta (< \delta ')$ ，使得对任何 $x^{\prime},x^{\prime \prime}\in U^{\circ}(x_0;\delta)$ ，有 $|f(x^{\prime}) - f(x^{\prime \prime})| < \varepsilon .$

证 必要性 设 $\lim_{x\to x_0}f(x) = A$，则对任给的 $\varepsilon > 0$，存在正数 $\delta (< \delta')$，使得对任何 $x \in U^\circ(x_0; \delta)$，有 $|f(x) - A| < \frac{\varepsilon}{2}$. 于是对任何 $x', x'' \in U^\circ(x_0; \delta)$，有

$$
\mid f (x ^ {\prime}) - f (x ^ {\prime \prime}) \mid \leqslant \mid f (x ^ {\prime}) - A \mid + \mid f (x ^ {\prime \prime}) - A \mid <   \frac {\varepsilon}{2} + \frac {\varepsilon}{2} = \varepsilon .
$$

充分性 设数列 $\{x_{n}\} \subset U^{\circ}(x_{0};\delta)$ 且 $\lim_{n\to \infty}x_n = x_0$ .按假设，对任给的 $\varepsilon >0$ ，存在正数$\delta (< \delta ')$ ，使得对任何 $x^{\prime},x^{\prime \prime}\in U^{\circ}(x_0;\delta)$ ，有 $\mid f(x^{\prime}) - f(x^{\prime \prime})\mid < \varepsilon .$ 由于 $x_{n}\rightarrow x_{0}(n\to \infty)$ ，对上述的 $\delta >0$ ，存在 $N > 0$ ，使得当 $n,m > N$ 时，有 $x_{n},x_{m}\in U^{\circ}(x_{0};\delta)$ ，从而有

$$
\mid f (x _ {n}) - f (x _ {m}) \mid <   \varepsilon .
$$

于是，按数列的柯西收敛准则，数列 $\{f(x_n)\}$ 的极限存在，记为 $A$ ，即 $\lim_{n\to \infty}f(x_n) = A.$

对任意  $x \in U^{\circ}(x_{0};\delta)$ ，当 n > N 时，有

$$
\mid f (x) - f (x _ {n}) \mid <   \varepsilon .
$$

令 $n\to \infty$ ，则

$$
\mid f (x) - A \mid \leqslant \varepsilon .
$$

这就证明了 $\lim_{x\to x_0}f(x) = A.$

按照函数极限的柯西准则,我们能写出极限 $\lim_{x\to x_{0}}f(x)$ 不存在的充要条件:存在 $\varepsilon_{0}>0$ ,对任何 $\delta>0$ (无论 $\delta$ 多么小),总可找到 $x^{\prime},x^{\prime\prime}\in U^{\circ}(x_{0};\delta)$ ,使得 $\left|f(x^{\prime})-f(x^{\prime\prime})\right|\geqslant\varepsilon_{0}$ .

如在例1中我们可取 $\varepsilon_0 = 1$ ，对任何 $\delta >0$ ，设正整数 $n > \frac{1}{\delta}$ ，令

$$
x ^ {\prime} = \frac {1}{n \pi}, x ^ {\prime \prime} = \frac {1}{n \pi + \frac {\pi}{2}},
$$

则有 $x^{\prime}, x^{\prime \prime} \in U^{\circ}(0; \delta)$，而 $\left|\sin \frac{1}{x'} - \sin \frac{1}{x''}\right| = 1 = \varepsilon_0$。于是按柯西准则，极限 $\lim_{x \to 0} \sin \frac{1}{x}$ 不存在。

## 习题3.3

1. 叙述函数极限 $\lim_{x\to +\infty}f(x)$ 的归结原则，并应用它证明 $\lim_{x\to +\infty}\cos x$ 不存在.

2. 设 $f$ 为定义在 $[a, +\infty)$ 上的增（减）函数. 证明:$\lim_{x \to +\infty} f(x)$ 存在的充要条件是 $f$ 在 $[a, +\infty)$ 上有上（下）界.

3.（1）叙述极限 $\lim_{x\to -\infty}f(x)$ 的柯西准则；

(2) 根据柯西准则叙述  $\lim_{x\to-\infty}f(x)$  不存在的充要条件，并应用它证明  $\lim_{x\to-\infty}\sin x$  不存在.

4. 设 $f$ 在 $U^{\circ}(x_0)$ 有定义. 证明: 若对任何数列 $\{x_n\} \subset U^{\circ}(x_0)$ 且 $\lim_{n\to \infty}x_n = x_0$，极限 $\lim_{n\to \infty}f(x_n)$ 都存在，则所有这些极限都相等.

5. 设 $f$ 为 $U^{\circ}(x_0)$ 上的递增函数. 证明: $f(x_0 - 0)$ 和 $f(x_0 + 0)$ 都存在, 且

$$
f (x _ {0} - 0) = \sup _ {x \in U _ {-} ^ {\circ} (x _ {0})} f (x), f (x _ {0} + 0) = \inf _ {x \in U _ {+} ^ {\circ} (x _ {0})} f (x).
$$

6. 设 $D(x)$ 为狄利克雷函数, $x_0 \in \mathbf{R}$. 证明: $\lim_{x \to x_0} D(x)$ 不存在.

7. 证明: 若 f 为周期函数, 且  $\lim_{x\to+\infty}f(x)=0$ , 则  $f(x)\equiv0$ .

8. 证明定理 3.9.

## § 4 两个重要的极限

## 一、证明 $\lim_{x\to 0}\frac{\sin x}{x} = 1$

证 在 §1 例4中我们已导出如下不等式:

$$
\sin x <   x <   \tan x \quad \left(0 <   x <   \frac {\pi}{2}\right),
$$

除以 $\sin x$ ，得到 $1 < \frac{x}{\sin x} < \frac{1}{\cos x}$ ，由此得

$$
\cos x <   \frac {\sin x}{x} <   1. \tag {1}
$$

在(1)式中用-x代替x时,(1)式不变,故(1)式当 $-\frac{\pi}{2}<x<0$ 时也成立,从而它对一切满足不等式

![](images/page_63_image_15.jpg)

<details>
<summary>text_image</summary>

y=\frac{\sin x}{x}
O
x
</details>

图3-5

$0 < |x| < \frac{\pi}{2}$ 的 x 都成立. 由 $\lim_{x \to 0} \cos x = 1$ 及函数极限的迫敛性, 即得 $\lim_{x \to 0} \frac{\sin x}{x} = 1$.

函数  $y=\frac{\sin x}{x}$  的图像如图 3-5 所示.

例1 求 $\lim_{x\to \pi}\frac{\sin x}{\pi - x}.$

解 令 $t = \pi - x$，则 $\sin x = \sin (\pi - t) = \sin t$，且当 $x \to \pi$ 时 $t \to 0$. 所以有

$$
\lim _ {x \to \pi} \frac {\sin x}{\pi - x} = \lim _ {t \to 0} \frac {\sin t}{t} = 1.
$$

例 2 求  $\lim_{x\to0}\frac{1-\cos x}{x^{2}}$ .

解