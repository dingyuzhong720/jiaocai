$$
\frac {1}{k ^ {p}} = \int_ {k - 1} ^ {k} \frac {1}{k ^ {p}} \mathrm{d} x \leqslant \int_ {k - 1} ^ {k} \frac {1}{x ^ {p}} \mathrm{d} x \quad (k = 2, 3, \dots),
$$

从而级数(2-2)的部分和

$$
\begin{array}{l} s _ {n} = 1 + \sum_ {k = 2} ^ {n} \frac {1}{k ^ {p}} \leqslant 1 + \sum_ {k = 2} ^ {n} \int_ {k - 1} ^ {k} \frac {1}{x ^ {p}} \mathrm{d} x = 1 + \int_ {1} ^ {n} \frac {1}{x ^ {p}} \mathrm{d} x \\ = 1 + \frac {1}{p - 1} \left(1 - \frac {1}{n ^ {p - 1}}\right) <   1 + \frac {1}{p - 1} \quad (n = 2, 3, \dots), \\ \end{array}
$$

这表明数列 $\{s_{n}\}$ 有界,因此级数(2-2)收敛.

综合上述结果,我们得到:p 级数(2-2)当 p>1 时收敛,当  $p \leqslant 1$  时发散.

例2 证明级数 $\sum_{n=1}^{\infty} \frac{1}{\sqrt{n(n+1)}}$ 是发散的.

证 因为 $n(n + 1) < (n + 1)^2$，所以 $\frac{1}{\sqrt{n(n + 1)}} > \frac{1}{n + 1}$. 而级数

$$
\sum_ {n = 1} ^ {\infty} \frac {1}{n + 1} = \frac {1}{2} + \frac {1}{3} + \dots + \frac {1}{n + 1} + \dots
$$

是发散的.根据比较审敛法可知所给级数也是发散的.

为应用上的方便,下面我们给出比较审敛法的极限形式.

定理3（比较审敛法的极限形式）设 $\sum_{n = 1}^{\infty}u_n$ 和 $\sum_{n = 1}^{\infty}v_n$ 都是正项级数，

（1）如果 $\lim_{n\to \infty}\frac{u_n}{v_n} = l$ （$0\leqslant l < +\infty$），且级数 $\sum_{n = 1}^{\infty}v_n$ 收敛，那么级数 $\sum_{n = 1}^{\infty}u_n$ 收敛；
(2) 如果  $\lim_{n\to\infty}\frac{u_n}{v_n}=l>0$  或  $\lim_{n\to\infty}\frac{u_n}{v_n}=+\infty$  ，且级数  $\sum_{n=1}^{\infty}v_n$  发散，那么级数  $\sum_{n=1}^{\infty}u_n$  发散.

证（1）由极限定义可知，对 $\varepsilon = 1$ ，存在正整数 $N$ ，当 $n > N$ 时，有

$$
\frac {u _ {n}}{v _ {n}} <   l + 1,
$$

即 $u_{n} < (l + 1)v_{n}$. 而级数 $\sum_{n=1}^{\infty} v_{n}$ 收敛, 根据比较审敛法的推论, 知级数 $\sum_{n=1}^{\infty} u_{n}$ 收敛.

（2）按已知条件知极限 $\lim_{n\to \infty}\frac{v_n}{u_n}$ 存在，如果级数 $\sum_{n = 1}^{\infty}u_n$ 收敛，那么由结论(1)必有级数 $\sum_{n = 1}^{\infty}v_n$ 收敛，但已知级数 $\sum_{n = 1}^{\infty}v_n$ 发散，因此级数 $\sum_{n = 1}^{\infty}u_n$ 不可能收敛，即级数 $\sum_{n = 1}^{\infty}u_n$ 发散.对于 $\lim_{n\to \infty}\frac{u_n}{v_n} = +\infty$ 的情形，留给读者证明.

极限形式的比较审敛法,在两个正项级数的一般项均趋于零的情况下,其实是比较它们的一般项作为无穷小量的阶.定理表明,当  $n \to \infty$  时,如果  $u_{n}$  是与  $v_{n}$  同阶或是比  $v_{n}$  高阶的无穷小,而级数  $\sum_{n=1}^{\infty} v_{n}$  收敛,那么级数  $\sum_{n=1}^{\infty} u_{n}$  收敛;如果  $u_{n}$  是与  $v_{n}$  同阶或是比  $v_{n}$  低阶的无穷小,而级数  $\sum_{n=1}^{\infty} v_{n}$  发散,那么级数  $\sum_{n=1}^{\infty} u_{n}$  发散.

例3 判定级数 $\sum_{n=1}^{\infty} \sin \frac{1}{n}$ 的收敛性.

解 因为

$$
\lim _ {n \to \infty} \frac {\sin \frac {1}{n}}{\frac {1}{n}} = 1 > 0,
$$

而级数  $\sum_{n=1}^{\infty}\frac{1}{n}$  发散, 根据定理 3 知此级数发散.

用比较审敛法审敛时,需要适当地选取一个已知其收敛性的级数  $\sum_{n=1}^{\infty}v_{n}$  作为比较的基准.最常选作基准级数的是等比级数和 p 级数.

将所给正项级数与等比级数比较,我们能得到在实用上很方便的比值审敛法和根值审敛法.

定理4(比值审敛法, 达朗贝尔(d'Alembert)判别法) 设 $\sum_{n=1}^{\infty} u_n$ 为正项级数, 如果

$$
\lim _ {n \to \infty} \frac {u _ {n + 1}}{u _ {n}} = \rho ,
$$

那么当 $\rho < 1$ 时级数收敛, $\rho > 1$ （或 $\lim_{n\to \infty}\frac{u_{n + 1}}{u_n} = \infty$）时级数发散, $\rho = 1$ 时级数可能收敛也可能发散.

证（1）当 $\rho < 1$ 时.取一个适当小的正数 $\varepsilon$ ，使得 $\rho +\varepsilon = r < 1$ ，根据极限定义，存在正整数 $m$ ，当 $n\geqslant m$ 时有不等式

$$
\frac {u _ {n + 1}}{u _ {n}} <   \rho + \varepsilon = r.
$$

因此

$$
u _ {m + 1} <   r u _ {m}, u _ {m + 2} <   r u _ {m + 1} <   r ^ {2} u _ {m}, \dots , u _ {m + k} <   r ^ {k} u _ {m}, \dots .
$$

而级数 $\sum_{k=1}^{\infty} r^{k} u_{m}$ 收敛(公比 $r < 1$), 根据定理2的推论, 知级数 $\sum_{n=1}^{\infty} u_{n}$ 收敛.

(2) 当  $\rho > 1$  时. 取一个适当小的正数  $\varepsilon$ , 使得  $\rho - \varepsilon > 1$ . 根据极限定义, 当  $n \geqslant m$  时有

![](images/page_257_image_17.jpg)

例题精讲

12-2

不等式

$$
\frac {u _ {n + 1}}{u _ {n}} > \rho - \varepsilon > 1,
$$

也就是

$$
u _ {n + 1} > u _ {n}.
$$

所以当 $n \geqslant m$ 时, 级数的一般项 $u_{n}$ 是逐渐增大的, 从而 $\lim_{n \to \infty} u_{n} \neq 0$. 根据级数收敛的必要条件可知级数 $\sum_{n=1}^{\infty} u_{n}$ 发散.

类似地, 可以证明当  $\lim_{n\to\infty}\frac{u_{n+1}}{u_n}=\infty$  时, 级数  $\sum_{n=1}^{\infty}u_n$  发散.

(3) 当  $\rho=1$  时. 级数可能收敛也可能发散. 例如 p 级数 (2-2), 不论 p 为何值都有

$$
\lim _ {n \to \infty} \frac {u _ {n + 1}}{u _ {n}} = \lim _ {n \to \infty} \frac {\frac {1}{(n + 1) ^ {p}}}{\frac {1}{n ^ {p}}} = 1.
$$

但我们知道, 当 p>1 时级数收敛, 当  $p \leqslant 1$  时级数发散, 因此只根据  $\rho=1$  不能判定级数的收敛性.

例4 证明级数

$$
1 + \frac {1}{1} + \frac {1}{1 \times 2} + \frac {1}{1 \times 2 \times 3} + \dots + \frac {1}{(n - 1) !} + \dots
$$

是收敛的,并估计以级数的部分和  $s_{n}$  近似代替和 s 所产生的误差.

解 因为

$$
\lim _ {n \to \infty} \frac {u _ {n + 1}}{u _ {n}} = \lim _ {n \to \infty} \frac {(n - 1) !}{n !} = \lim _ {n \to \infty} \frac {1}{n} = 0 <   1,
$$

根据比值审敛法可知所给级数收敛.

以这级数的部分和 $s_n$ 近似代替和 $s$ 所产生的误差为

$$
\begin{array}{l} \mid r _ {n} \mid = \frac {1}{n !} + \frac {1}{(n + 1) !} + \frac {1}{(n + 2) !} + \dots \\ = \frac {1}{n !} \left[ 1 + \frac {1}{n + 1} + \frac {1}{(n + 1) (n + 2)} + \dots \right] \\ <   \frac {1}{n !} \left(1 + \frac {1}{n} + \frac {1}{n ^ {2}} + \dots\right) \\ = \frac {1}{n !} \frac {1}{1 - \frac {1}{n}} = \frac {1}{(n - 1) (n - 1) !}. \\ \end{array}
$$

例5 判定级数

$$
\frac {1}{1 0} + \frac {1 \times 2}{1 0 ^ {2}} + \frac {1 \times 2 \times 3}{1 0 ^ {3}} + \dots + \frac {n !}{1 0 ^ {n}} + \dots
$$

的收敛性.

解 因为

$$
\frac {u _ {n + 1}}{u _ {n}} = \frac {(n + 1) !}{1 0 ^ {n + 1}} \times \frac {1 0 ^ {n}}{n !} = \frac {n + 1}{1 0},
$$

$$
\lim _ {n \to \infty} \frac {u _ {n + 1}}{u _ {n}} = \lim _ {n \to \infty} \frac {n + 1}{1 0} = \infty .
$$

根据比值审敛法可知所给级数发散.

\*定理5（根值审敛法，柯西判别法）设 $\sum_{n=1}^{\infty} u_n$ 为正项级数，如果

$$
\lim _ {n \to \infty} \sqrt [ n ]{u _ {n}} = \rho ,
$$

那么当 $\rho < 1$ 时级数收敛, $\rho > 1$ (或 $\lim_{n\to \infty}\sqrt[n]{u_n} = +\infty$) 时级数发散, $\rho = 1$ 时级数可能收敛也可能发散.

定理 5 的证明与定理 4 相仿, 这里从略.

例6 判定级数 $\sum_{n=1}^{\infty} \frac{2 + (-1)^n}{2^n}$ 的收敛性.

证 $\lim_{n\to \infty}\sqrt[n]{u_n} = \lim_{n\to \infty}\frac{1}{2}\sqrt[n]{2 + (-1)^n} = \lim_{n\to \infty}\frac{1}{2}\mathrm{e}^{\frac{1}{n}\ln [2 + (-1)^n]},$

因 $\ln [2 + (-1)^n]$ 有界，故 $\lim_{n\to \infty}\frac{1}{n}\ln [2 + (-1)^n] = 0$ ，从而

$$
\lim _ {n \to \infty} \sqrt [ n ]{u _ {n}} = \frac {1}{2}.
$$

因此,根据根值审敛法知所给级数收敛.

将所给正项级数与 p 级数作比较, 可得在实用上较方便的极限审敛法.

定理6（极限审敛法）设 $\sum_{n = 1}^{\infty}u_n$ 为正项级数，

（1）如果 $\lim_{n\to \infty}nu_n = l > 0$ （或 $\lim_{n\to \infty}nu_n = +\infty$ ），那么级数 $\sum_{n = 1}^{\infty}u_n$ 发散；
(2) 如果 p > 1，而  $\lim_{n \to \infty} n^{p} u_{n} = l$  ( $0 \leqslant l < +\infty$ )，那么级数  $\sum_{n=1}^{\infty} u_{n}$  收敛.

证（1）在极限形式的比较审敛法中，取 $v_{n} = \frac{1}{n}$，由调和级数 $\sum_{n=1}^{\infty} \frac{1}{n}$ 发散，知结论成立.

例题精讲 12-3

(2) 在极限形式的比较审敛法中, 取  $v_{n}=\frac{1}{n^{p}}$ , 当 p>1 时, p 级数  $\sum_{n=1}^{\infty}\frac{1}{n^{p}}$  收敛, 故结论成立.

例7 判定级数 $\sum_{n=1}^{\infty} \ln \left(1 + \frac{1}{n^{2}}\right)$ 的收敛性.

解 因 $\ln \left(1 + \frac{1}{n^2}\right) \sim \frac{1}{n^2} (n \to \infty)$, 故

$$
\lim _ {n \to \infty} n ^ {2} u _ {n} = \lim _ {n \to \infty} n ^ {2} \ln \left(1 + \frac {1}{n ^ {2}}\right) = \lim _ {n \to \infty} n ^ {2} \times \frac {1}{n ^ {2}} = 1,
$$

根据极限审敛法,知所给级数收敛.

例8 判定级数 $\sum_{n=1}^{\infty} \sqrt{n+1}\left(1 - \cos \frac{\pi}{n}\right)$ 的收敛性.

解 因为

$$
\lim _ {n \to \infty} n ^ {\frac {3}{2}} u _ {n} = \lim _ {n \to \infty} n ^ {\frac {3}{2}} \sqrt {n + 1} \left(1 - \cos \frac {\pi}{n}\right) = \lim _ {n \to \infty} n ^ {2} \sqrt {\frac {n + 1}{n}} \times \frac {1}{2} \left(\frac {\pi}{n}\right) ^ {2} = \frac {1}{2} \pi^ {2},
$$

根据极限审敛法,知所给级数收敛.

## 二、交错级数及其审敛法

所谓交错级数是这样的级数,它的各项是正负交错的,从而可以写成下面的形式:

$$
u _ {1} - u _ {2} + u _ {3} - u _ {4} + \dots , \tag {2-3}
$$

或

$$
- u _ {1} + u _ {2} - u _ {3} + u _ {4} - \dots , \tag {2-4}
$$

其中  $u_{1}, u_{2}, \cdots$  都是正数. 我们按级数 (2-3) 的形式来证明关于交错级数的一个审敛法.

定理7（莱布尼茨定理）如果交错级数 $\sum_{n = 1}^{\infty}(-1)^{n - 1}u_n$ 满足条件:

(1)  $u_{n} \geqslant u_{n+1}$  ( $n = 1, 2, 3, \cdots$ );
(2) $\lim_{n\to \infty}u_n = 0,$

那么级数收敛,且其和  $s \leqslant u_{1}$ , 其余项  $r_{n}$  的绝对值  $\left|r_{n}\right| \leqslant u_{n+1}$ .

证 先证明前 $2n$ 项的和 $s_{2n}$ 的极限存在.为此把 $s_{2n}$ 写成两种形式:

$$
s _ {2 n} = (u _ {1} - u _ {2}) + (u _ {3} - u _ {4}) + \dots + (u _ {2 n - 1} - u _ {2 n})
$$

及

$$
s _ {2 n} = u _ {1} - (u _ {2} - u _ {3}) - (u _ {4} - u _ {5}) - \dots - (u _ {2 n - 2} - u _ {2 n - 1}) - u _ {2 n}.
$$

根据条件(1)知道所有括号中的差都是非负的.由第一种形式可见数列 $\{s_{2n}\}$ 是单调增加的,由第二种形式可见 $s_{2n}<u_{1}$ .于是,根据单调有界数列必有极限的准则知道,当n无

释疑解难

12-2

限增大时, $s_{2n}$ 趋于一个极限s,并且s不大于 $u_{1}$ :

$$
\lim _ {n \to \infty} s _ {2 n} = s \leqslant u _ {1}.
$$

再证明前 $2n + 1$ 项的和 $s_{2n + 1}$ 的极限也是 $s$. 事实上, 我们有

$$
s _ {2 n + 1} = s _ {2 n} + u _ {2 n + 1}.
$$

由条件(2)知 $\lim_{n\to\infty}u_{2n+1}=0$ ,因此

$$
\lim _ {n \to \infty} s _ {2 n + 1} = \lim _ {n \to \infty} (s _ {2 n} + u _ {2 n + 1}) = s.
$$

由于级数的前偶数项的和与奇数项的和趋于同一极限 $s$，故级数 $\sum_{n=1}^{\infty} (-1)^{n-1} u_n$ 的部分和 $s_n$ 当 $n \to \infty$ 时具有极限 $s$。这就证明了级数 $\sum_{n=1}^{\infty} (-1)^{n-1} u_n$ 收敛于和 $s$，且 $s \leqslant u_1$.

最后,不难看出余项  $r_{n}$  可以写成

$$
r _ {n} = \pm (u _ {n + 1} - u _ {n + 2} + \dots),
$$

其绝对值

$$
\mid r _ {n} \mid = u _ {n + 1} - u _ {n + 2} + \dots ,
$$

上式右端也是一个交错级数,它也满足收敛的两个条件,所以其和小于级数的第一项,也就是说

$$
\mid r _ {n} \mid \leqslant u _ {n + 1}.
$$

证明完毕.

例如,交错级数

$$
1 - \frac {1}{2} + \frac {1}{3} - \frac {1}{4} + \dots + (- 1) ^ {n - 1} \frac {1}{n} + \dots
$$

满足条件

(1) $u_{n} = \frac{1}{n} >\frac{1}{n + 1} = u_{n + 1}$ ($n = 1,2,\dots$)

及

(2) $\lim_{n\to \infty}u_n = \lim_{n\to \infty}\frac{1}{n} = 0,$

所以它是收敛的,且其和 s<1. 如果取前 n 项的和

$$
s _ {n} = 1 - \frac {1}{2} + \frac {1}{3} - \dots + (- 1) ^ {n - 1} \frac {1}{n}
$$

作为 $s$ 的近似值, 所产生的误差 $\left|r_{n}\right| \leqslant \frac{1}{n+1} (= u_{n+1})$.

## 三、绝对收敛与条件收敛

现在我们讨论一般的级数

![](images/page_261_image_26.jpg)

例题精讲

$$
u _ {1} + u _ {2} + \dots + u _ {n} + \dots ,
$$

它的各项为任意实数.如果级数 $\sum_{n=1}^{\infty} u_n$ 各项的绝对值所构成的正项级数 $\sum_{n=1}^{\infty} |u_n|$ 收敛,那么称级数 $\sum_{n=1}^{\infty} u_n$ 绝对收敛;如果级数 $\sum_{n=1}^{\infty} u_n$ 收敛,而级数 $\sum_{n=1}^{\infty} |u_n|$ 发散,那么称级数 $\sum_{n=1}^{\infty} u_n$ 条件收敛.容易知道,级数 $\sum_{n=1}^{\infty} (-1)^{n-1} \frac{1}{n^2}$ 是绝对收敛级数,而级数 $\sum_{n=1}^{\infty} (-1)^{n-1} \frac{1}{n}$ 是条件收敛级数.

级数绝对收敛与级数收敛有以下重要关系:

定理8 如果级数 $\sum_{n=1}^{\infty} u_n$ 绝对收敛, 那么级数 $\sum_{n=1}^{\infty} u_n$ 必定收敛.

证令

$$
v _ {n} = \frac {1}{2} (u _ {n} + | u _ {n} |) \quad (n = 1, 2, \dots).
$$

显然 $v_{n} \geqslant 0$ 且 $v_{n} \leqslant |u_{n}| (n = 1,2,\dots)$. 因级数 $\sum_{n=1}^{\infty} |u_{n}|$ 收敛, 故由比较审敛法知道, 级数 $\sum_{n=1}^{\infty} v_{n}$ 收敛, 从而级数 $\sum_{n=1}^{\infty} 2v_{n}$ 也收敛. 而 $u_{n} = 2v_{n} - |u_{n}|$, 由收敛级数的基本性质可知

$$
\sum_ {n = 1} ^ {\infty} u _ {n} = \sum_ {n = 1} ^ {\infty} 2 v _ {n} - \sum_ {n = 1} ^ {\infty} | u _ {n} |,
$$

所以级数  $\sum_{n=1}^{\infty}u_{n}$  收敛. 定理证毕.

上述证明中引入的级数 $\sum_{n=1}^{\infty} v_n$，其一般项

$$
v _ {n} = \frac {1}{2} (u _ {n} + | u _ {n} |) = \left\{ \begin{array}{l l} u _ {n}, & u _ {n} > 0, \\ 0, & u _ {n} \leqslant 0, \end{array} \right.
$$

可见级数 $\sum_{n=1}^{\infty} v_n$ 是把级数 $\sum_{n=1}^{\infty} u_n$ 中的负项换成 0 而得的, 它也就是级数 $\sum_{n=1}^{\infty} u_n$ 中的全体正项所构成的级数. 类似可知, 令

$$
w _ {n} = \frac {1}{2} (| u _ {n} | - u _ {n}),
$$

则 $\sum_{n=1}^{\infty} w_n$ 为级数 $\sum_{n=1}^{\infty} u_n$ 中全体负项的绝对值所构成的级数. 如果级数 $\sum_{n=1}^{\infty} u_n$ 绝对收敛, 那么级数 $\sum_{n=1}^{\infty} v_n$ 与 $\sum_{n=1}^{\infty} w_n$ 都收敛; 如果级数条件收敛（即 $\sum_{n=1}^{\infty} u_n$ 收敛, 而 $\sum_{n=1}^{\infty} |u_n|$ 发

散），那么级数  $\sum_{n=1}^{\infty}v_{n}$  与  $\sum_{n=1}^{\infty}w_{n}$  都发散.

定理8说明,对于一般的级数 $\sum_{n=1}^{\infty} u_n$, 如果我们用正项级数的审敛法判定级数 $\sum_{n=1}^{\infty} |u_n|$ 收敛, 那么此级数收敛. 这就使得一大类级数的收敛性判定问题, 转化成正项级数的收敛性判定问题.

一般说来,如果级数  $\sum_{n=1}^{\infty}|u_{n}|$  发散,我们不能断定级数  $\sum_{n=1}^{\infty}u_{n}$  也发散.但是,如果我们用比值审敛法或根值审敛法根据  $\lim_{n\to\infty}\left|\frac{u_{n+1}}{u_n}\right|=\rho>1$  或  $\lim_{n\to\infty}\sqrt[n]{|u_n|}=\rho>1$  判定级数  $\sum_{n=1}^{\infty}|u_{n}|$  发散,那么我们可以断定级数  $\sum_{n=1}^{\infty}u_{n}$  必定发散.这是因为从  $\rho>1$  可推知  $|u_{n}|\nrightarrow0(n\to\infty)$ ,从而  $u_{n}\nrightarrow0(n\to\infty)$ ,因此级数  $\sum_{n=1}^{\infty}u_{n}$  是发散的.

例9 判定级数 $\sum_{n=1}^{\infty} \frac{\sin n\alpha}{n^2}$ 的收敛性.

解 因为 $\left|\frac{\sin n\alpha}{n^2}\right| \leqslant \frac{1}{n^2}$, 而级数 $\sum_{n=1}^{\infty} \frac{1}{n^2}$ 收敛, 所以级数 $\sum_{n=1}^{\infty} \left|\frac{\sin n\alpha}{n^2}\right|$ 也收敛. 由定理8知, 级数 $\sum_{n=1}^{\infty} \frac{\sin n\alpha}{n^2}$ 收敛.

例10 判定级数 $\sum_{n=1}^{\infty}(-1)^{n}\frac{1}{2^{n}}\left(1+\frac{1}{n}\right)^{n^{2}}$ 的收敛性.

解 这是交错级数. 记 $u_{n} = \frac{1}{2^{n}}\left(1 + \frac{1}{n}\right)^{n^{2}}$，有

$$
\sqrt [ n ]{u _ {n}} = \frac {1}{2} \left(1 + \frac {1}{n}\right) ^ {n} \rightarrow \frac {1}{2} \mathrm{e} \quad (n \rightarrow \infty),
$$

而 $\frac{1}{2}e>1$ , 可知  $u_{n}\rightarrow0(n\rightarrow\infty)$ , 因此所给级数发散.

## \* 四、绝对收敛级数的性质

绝对收敛级数有很多性质是条件收敛级数所没有的,下面给出关于绝对收敛级数的两个性质.

定理 9 绝对收敛级数经改变项的位置后构成的级数也收敛,且与原级数有相同的和(即绝对收敛级数具有可交换性).

证（1）先证定理对于收敛的正项级数是正确的.

设级数

$$
u _ {1} + u _ {2} + \dots + u _ {n} + \dots
$$

为收敛的正项级数,其部分和为  $s_{n}$ , 和为 s. 并设级数

$$
u _ {1} ^ {*} + u _ {2} ^ {*} + \dots + u _ {n} ^ {*} + \dots
$$

为改变项的位置后构成的级数,其部分和为  $s_{n}^{*}$ .

对于任何 n, 当它固定后, 取 m 足够大, 使  $u_{1}^{*}, u_{2}^{*}, \cdots, u_{n}^{*}$  各项都出现在  $s_{m} = u_{1} + u_{2} + \cdots + u_{m}$  中, 于是得

$$
s _ {n} ^ {*} \leqslant s _ {m} \leqslant s,
$$

所以,单调增加的数列 $\{s_{n}^{*}\}$ 不超过定数s,根据单调有界数列必有极限的准则(第一章第六节),可知 $\lim_{n\to\infty}s_{n}^{*}$ 存在,即级数 $\sum_{n=1}^{\infty}u_{n}^{*}$ 收敛,且

$$
\lim _ {n \to \infty} s _ {n} ^ {*} = s ^ {*} \leqslant s.
$$

另一方面,如果把原来级数  $\sum_{n=1}^{\infty}u_{n}$  看成是级数  $\sum_{n=1}^{\infty}u_{n}^{*}$  改变项的位置以后所成的级数,那么应用刚才证得的结论,又有

$$
s \leqslant s ^ {*}.
$$

要使得上面两个不等式同时成立,必定有

$$
s ^ {*} = s.
$$

(2) 再证定理对一般的绝对收敛级数是正确的.

设级数 $\sum_{n=1}^{\infty}|u_n|$ 收敛.在定理8的证明中已得

$$
u _ {n} = 2 v _ {n} - \mid u _ {n} \mid ,
$$

而 $\sum_{n=1}^{\infty} v_n$ 是收敛的正项级数. 故有

$$
\sum_ {n = 1} ^ {\infty} u _ {n} = \sum_ {n = 1} ^ {\infty} (2 v _ {n} - | u _ {n} |) = \sum_ {n = 1} ^ {\infty} 2 v _ {n} - \sum_ {n = 1} ^ {\infty} | u _ {n} |.
$$

若级数 $\sum_{n=1}^{\infty} u_n$ 改变项的位置后的级数为 $\sum_{n=1}^{\infty} u_n^*$, 则相应的 $\sum_{n=1}^{\infty} v_n$ 改变为 $\sum_{n=1}^{\infty} v_n^*$, $\sum_{n=1}^{\infty} |u_n|$ 改变为 $\sum_{n=1}^{\infty} |u_n^*|$, 由(1)证得的结论可知

$$
\sum_ {n = 1} ^ {\infty} v _ {n} = \sum_ {n = 1} ^ {\infty} v _ {n} ^ {*}, \quad \sum_ {n = 1} ^ {\infty} | u _ {n} | = \sum_ {n = 1} ^ {\infty} | u _ {n} ^ {*} |.
$$

所以

$$
\sum_ {n = 1} ^ {\infty} u _ {n} ^ {*} = \sum_ {n = 1} ^ {\infty} 2 v _ {n} ^ {*} - \sum_ {n = 1} ^ {\infty} | u _ {n} ^ {*} | = \sum_ {n = 1} ^ {\infty} 2 v _ {n} - \sum_ {n = 1} ^ {\infty} | u _ {n} | = \sum_ {n = 1} ^ {\infty} u _ {n}.
$$

证毕.

在给出绝对收敛级数的另一个性质以前,我们先来讨论级数的乘法运算.

设级数  $\sum_{n=1}^{\infty}u_{n}$  和  $\sum_{n=1}^{\infty}v_{n}$  都收敛,仿照有限项之和相乘的规则,作出这两个级数的项所有可能的乘积  $u_{i}v_{k}\quad(i,k=1,2,3,\cdots)$ ,这些乘积是

$$
\begin{array}{l} u _ {1} v _ {1}, u _ {1} v _ {2}, u _ {1} v _ {3}, \dots , u _ {1} v _ {i}, \dots , \\ u _ {2} v _ {1}, u _ {2} v _ {2}, u _ {2} v _ {3}, \dots , u _ {2} v _ {i}, \dots , \\ u _ {3} v _ {1}, u _ {3} v _ {2}, u _ {3} v _ {3}, \dots , u _ {3} v _ {i}, \dots , \\ u _ {k} v _ {1}, u _ {k} v _ {2}, u _ {k} v _ {3}, \dots , u _ {k} v _ {i}, \dots , \\ \end{array}
$$

...

...

这些乘积可以用很多方式将它们排列成一个数列.例如可以按“对角线法”或按“正方形法”将它们排列成下面形状的数列(图12-2):

![](images/page_265_image_7.jpg)

图12-2

（对角线法） $u_{1}v_{1};u_{1}v_{2},u_{2}v_{1};\cdots;u_{1}v_{n},u_{2}v_{n-1},\cdots,u_{n}v_{1};\cdots.$

（正方形法） $u_{1}v_{1};u_{1}v_{2},u_{2}v_{2},u_{2}v_{1};\cdots;u_{1}v_{n},u_{2}v_{n},\cdots,u_{n}v_{n},u_{n}v_{n-1},\cdots,u_{n}v_{1};\cdots.$

把上面排列好的数列用加号相连,就组成无穷级数.我们称按“对角线法”排列所组成的级数

$$
u _ {1} v _ {1} + (u _ {1} v _ {2} + u _ {2} v _ {1}) + \dots + (u _ {1} v _ {n} + u _ {2} v _ {n - 1} + \dots + u _ {n} v _ {1}) + \dots .
$$

为两级数  $\sum_{n=1}^{\infty}u_{n}$  和  $\sum_{n=1}^{\infty}v_{n}$  的柯西乘积.

定理10(绝对收敛级数的乘法) 设级数 $\sum_{n=1}^{\infty} u_n$ 和 $\sum_{n=1}^{\infty} v_n$ 都绝对收敛, 其和分别为 $s$ 和 $\sigma$, 则它们的柯西乘积

$$
u _ {1} v _ {1} + (u _ {1} v _ {2} + u _ {2} v _ {1}) + \dots + (u _ {1} v _ {n} + u _ {2} v _ {n - 1} + \dots + u _ {n} v _ {1}) + \dots \tag {2-5}
$$

也是绝对收敛的,且其和为  $s\sigma$ .

证 考虑把级数(2-5)的括号去掉后所成的级数

$$
u _ {1} v _ {1} + u _ {1} v _ {2} + u _ {2} v _ {1} + \dots + u _ {1} v _ {n} + \dots . \tag {2-6}
$$

如果级数(2-6)绝对收敛且其和为 $w$ ，那么由收敛级数的基本性质4及比较审敛法可知，级数(2-5)也绝对收敛且其和为 $w$ .因此只要证明级数(2-6)绝对收敛且其和$w = s\sigma$ 就行了.

(1) 先证级数(2-6)绝对收敛.

设 $w_{m}$ 为级数(2-6)的前 $m$ 项分别取绝对值后所作成的和，又设

$$
\sum_ {n = 1} ^ {\infty} \mid u _ {n} \mid = A, \quad \sum_ {n = 1} ^ {\infty} \mid v _ {n} \mid = B,
$$

则显然有

$$
w _ {m} \leqslant \sum_ {n = 1} ^ {\infty} | u _ {n} | \cdot \sum_ {n = 1} ^ {\infty} | v _ {n} | \leqslant A B.
$$

由此可见单调增加数列 $\{w_{m}\}$ 不超过定数AB,所以级数(2-6)绝对收敛.

(2) 再证级数(2-6)的和  $w = s\sigma$ .

把级数(2-6)的各项位置重新排列并加上括号使它成为按“正方形法”排列所组成的级数

$$
u _ {1} v _ {1} + (u _ {1} v _ {2} + u _ {2} v _ {2} + u _ {2} v _ {1}) + \dots + (u _ {1} v _ {n} + u _ {2} v _ {n} + \dots + u _ {n} v _ {n} + u _ {n} v _ {n - 1} + \dots + u _ {n} v _ {1}) + \dots . \tag {2-7}
$$

根据定理 9 及收敛级数的基本性质 4 可知, 对于绝对收敛级数 (2-6) 这样做法是不会改变其和的. 容易看出, 级数 (2-7) 的前 n 项的和恰好为

$$
(u _ {1} + u _ {2} + \dots + u _ {n}) \cdot (v _ {1} + v _ {2} + \dots + v _ {n}) = s _ {n} \sigma_ {n},
$$

因此

$$
w = \lim _ {n \to \infty} (s _ {n} \sigma_ {n}) = s \sigma .
$$

## 习题12-2

1. 以下各题中给出了四个结论,从中选出一个正确的结论:

（1）设 $\sum_{n=1}^{\infty} a_n$ 是收敛的正项级数，$b_n = \frac{1 - \cos a_n}{a_n}, c_n = \frac{1 - \cos \sqrt{a_n}}{\sqrt{a_n}}$. 则有（ ）；

(A) $\sum_{n=1}^{\infty} b_n$ 和 $\sum_{n=1}^{\infty} c_n$ 均收敛

(B) $\sum_{n=1}^{\infty} b_n$ 收敛, $\sum_{n=1}^{\infty} c_n$ 敛散性不确定

(C) $\sum_{n=1}^{\infty} b_n$ 和 $\sum_{n=1}^{\infty} c_n$ 均发散

(D)  $\sum_{n=1}^{\infty}b_{n}$  发散， $\sum_{n=1}^{\infty}c_{n}$  敛散性不确定

(2) 设有两个数列  $\{a_{n}\}$  和  $\{b_{n}\}$ ，若  $\lim_{n\to\infty}a_{n}=0$ ，则有（）.

(A) 当 $\sum_{n=1}^{\infty} b_n$ 收敛时, $\sum_{n=1}^{\infty} a_n b_n$ 收敛

(B) 当 $\sum_{n=1}^{\infty} b_n$ 发散时, $\sum_{n=1}^{\infty} a_n b_n$ 发散

(C) 当  $\sum_{n=1}^{\infty}|b_{n}|$  收敛时， $\sum_{n=1}^{\infty}|a_{n}b_{n}|$  收敛

(D) 当 $\sum_{n=1}^{\infty}\left|b_n\right|$ 发散时，$\sum_{n=1}^{\infty}\left|a_nb_n\right|$ 发散

2. 用比较审敛法或极限形式的比较审敛法判定下列级数的收敛性:

(1) $1+\frac{1}{3}+\frac{1}{5}+\cdots+\frac{1}{2n-1}+\cdots;$

(2) $1+\frac{1+2}{1+2^{2}}+\frac{1+3}{1+3^{2}}+\cdots+\frac{1+n}{1+n^{2}}+\cdots;$

(3) $\frac{1}{2 \times 5} + \frac{1}{3 \times 6} + \cdots + \frac{1}{(n+1)(n+4)} + \cdots$;

(4)  $\sin\frac{\pi}{2}+\sin\frac{\pi}{2^{2}}+\sin\frac{\pi}{2^{3}}+\cdots+\sin\frac{\pi}{2^{n}}+\cdots;$

(5) $\sum_{n=1}^{\infty} \frac{1}{1 + a^n} (a > 0)$.

3. 用比值审敛法判定下列级数的收敛性:

(1) $\frac{3}{1\times2}+\frac{3^{2}}{2\times2^{2}}+\frac{3^{3}}{3\times2^{3}}+\cdots+\frac{3^{n}}{n\times2^{n}}+\cdots;$

(2) $\sum_{n=1}^{\infty} \frac{n^{2}}{3^{n}}$;

(3) $\sum_{n=1}^{\infty} \frac{2^n \times n!}{n^n}$;

(4) $\sum_{n=1}^{\infty} n \tan \frac{\pi}{2^{n+1}}$.

\* 4. 用根值审敛法判定下列级数的收敛性:

(1) $\sum_{n=1}^{\infty}\left(\frac{n}{2n+1}\right)^{n}$;

(2) $\sum_{n=1}^{\infty} \frac{1}{\left[\ln(n+1)\right]^{n}};$

(3) $\sum_{n=1}^{\infty}\left(\frac{n}{3n-1}\right)^{2n-1}$;

(4) $\sum_{n=1}^{\infty}\left(\frac{b}{a_n}\right)^n$, 其中 $a_n \to a (n \to \infty)$, $a_n, b, a$ 均为正数.

5. 判定下列级数的收敛性:

(1) $\frac{3}{4}+2\left(\frac{3}{4}\right)^{2}+3\left(\frac{3}{4}\right)^{3}+\cdots+n\left(\frac{3}{4}\right)^{n}+\cdots;$

(2) $\frac{1^{4}}{1!}+\frac{2^{4}}{2!}+\frac{3^{4}}{3!}+\cdots+\frac{n^{4}}{n!}+\cdots;$

(3) $\sum_{n=1}^{\infty} \frac{n+1}{n(n+2)}$;

(4) $\sum_{n=1}^{\infty} 2^{n} \sin \frac{\pi}{3^{n}}$;

(5)  $\sqrt{2}+\sqrt{\frac{3}{2}}+\cdots+\sqrt{\frac{n+1}{n}}+\cdots;$

(6) $\frac{1}{a+b}+\frac{1}{2a+b}+\cdots+\frac{1}{na+b}+\cdots\quad(a>0,b>0).$

6. 判定下列级数是否收敛,如果是收敛的,是绝对收敛还是条件收敛?

(1) $1-\frac{1}{\sqrt{2}}+\frac{1}{\sqrt{3}}-\frac{1}{\sqrt{4}}+\cdots+\frac{(-1)^{n-1}}{\sqrt{n}}+\cdots;$

(2) $\sum_{n=1}^{\infty}(-1)^{n-1}\frac{n}{3^{n-1}};$

(3) $\frac{1}{3} \times \frac{1}{2} - \frac{1}{3} \times \frac{1}{2^2} + \frac{1}{3} \times \frac{1}{2^3} - \frac{1}{3} \times \frac{1}{2^4} + \cdots + (-1)^{n-1} \frac{1}{3} \times \frac{1}{2^n} + \cdots$;

(4) $\frac{1}{\ln 2} - \frac{1}{\ln 3} + \frac{1}{\ln 4} - \frac{1}{\ln 5} + \cdots + (-1)^{n-1} \frac{1}{\ln (n+1)} + \cdots;$

(5) $\sum_{n=1}^{\infty}(-1)^{n+1}\frac{2^{n^2}}{n!}$.

## 第三节 幂级数

## 一、函数项级数的概念

如果给定一个定义在区间 $I$ 上的函数列

$$
u _ {1} (x), u _ {2} (x), u _ {3} (x), \dots , u _ {n} (x), \dots ,
$$

那么由这函数列构成的表达式

$$
u _ {1} (x) + u _ {2} (x) + u _ {3} (x) + \dots + u _ {n} (x) + \dots \tag {3-1}
$$

称为定义在区间 I 上的(函数项)无穷级数,简称(函数项)级数.

对于每一个确定的值 $x_0 \in I$，函数项级数(3-1)成为常数项级数

$$
u _ {1} (x _ {0}) + u _ {2} (x _ {0}) + u _ {3} (x _ {0}) + \dots + u _ {n} (x _ {0}) + \dots . \tag {3-2}
$$

这个级数(3-2)可能收敛也可能发散.如果级数(3-2)收敛,就称点 ${x}_{0}$ 是函数项级数 (3-1)的收敛点；如果级数(3-2)发散,就称点 ${x}_{0}$ 是函数项级数(3-1)的发散点.函数 项级数(3-1)的收敛点的全体称为它的收敛域,发散点的全体称为它的发散域.

对应于收敛域内的任意一个数 $x$，函数项级数成为一收敛的常数项级数，因而有一确定的和 $s$。这样，在收敛域上，函数项级数的和是 $x$ 的函数 $s(x)$，通常称 $s(x)$ 为函数项级数的和函数，这个函数的定义域就是级数的收敛域，并写成

$$
s (x) = u _ {1} (x) + u _ {2} (x) + u _ {3} (x) + \dots + u _ {n} (x) + \dots = \sum_ {i = 1} ^ {\infty} u _ {i} (x).
$$

把函数项级数(3-1)的前 $n$ 项的部分和记作 $s_n(x)$，则在收敛域上有

$$
\lim _ {n \to \infty} s _ {n} (x) = s (x).
$$

记 $r_n(x) = s(x) - s_n(x), r_n(x)$ 叫做函数项级数的余项（当然，只有 $x$ 在收敛域上 $r_n(x)$ 才有意义），并有

$$
\lim _ {n \to \infty} r _ {n} (x) = 0.
$$

## 二、幂级数及其收敛性

函数项级数中简单而常见的一类级数就是各项都是常数乘幂函数的函数项级数，即所谓幂级数，它的形式是①

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 幂级数的一般形式是 $a_0 + a_1(x - x_0) + a_2(x - x_0)^2 + \dots + a_n(x - x_0)^n + \dots$. 只要作代换 $t = x - x_0$，就可以把它化成(3-3)的形式. 所以取(3-3)式来讨论，并不影响一般性.</span></small>

$$
\sum_ {n = 0} ^ {\infty} a _ {n} x ^ {n} = a _ {0} + a _ {1} x + a _ {2} x ^ {2} + \dots + a _ {n} x ^ {n} + \dots , \tag {3-3}
$$

其中常数  $a_{0}, a_{1}, a_{2}, \cdots, a_{n}, \cdots$  叫做幂级数的系数.例如

$$
\begin{array}{l} 1 + x + x ^ {2} + \dots + x ^ {n} + \dots , \\ 1 + x + \frac {1}{2 !} x ^ {2} + \dots + \frac {1}{n !} x ^ {n} + \dots \\ \end{array}
$$

都是幂级数.

现在我们来讨论:对于一个给定的幂级数,它的收敛域与发散域是怎样的?即 x 取数轴上哪些点时幂级数收敛,取哪些点时幂级数发散?这就是幂级数的收敛性问题.

先看一个例子.考察幂级数

$$
1 + x + x ^ {2} + \dots + x ^ {n} + \dots
$$

的收敛性.由第一节例1知道,当 $|x|<1$ 时,这级数收敛于和 $\frac{1}{1-x}$ ;当 $|x|\geqslant1$ 时,这级数发散.因此,这幂级数的收敛域是开区间 $(-1,1)$ ,发散域是 $(-∞,-1]$ 及 $[1,+∞)$ ,并有

$$
\frac {1}{1 - x} = 1 + x + x ^ {2} + \dots + x ^ {n} + \dots \quad (- 1 <   x <   1).
$$

在这个例子中我们看到,这个幂级数的收敛域是一个区间.事实上,这个结论对于一般的幂级数也是成立的.我们有如下定理:

定理1(阿贝尔(Abel)定理) 如果级数 $\sum_{n=0}^{\infty} a_n x^n$ 当 $x = x_0 (x_0 \neq 0)$ 时收敛, 那么适合不等式 $|x| < |x_0|$ 的一切 $x$ 使这幂级数绝对收敛. 反之, 如果级数 $\sum_{n=0}^{\infty} a_n x^n$ 当 $x = x_0$ 时发散, 那么适合不等式 $|x| > |x_0|$ 的一切 $x$ 使这幂级数发散.

证 先设 $x_0$ 是幂级数(3-3)的收敛点, 即级数

$$
a _ {0} + a _ {1} x _ {0} + a _ {2} x _ {0} ^ {2} + \dots + a _ {n} x _ {0} ^ {n} + \dots
$$

收敛.根据级数收敛的必要条件,这时有

$$
\lim _ {n \to \infty} a _ {n} x _ {0} ^ {n} = 0,
$$

于是存在一个常数 M, 使得

$$
\mid a _ {n} x _ {0} ^ {n} \mid \leqslant M \quad (n = 0, 1, 2, \dots).
$$

这样级数(3-3)的一般项的绝对值

$$
\mid a _ {n} x ^ {n} \mid = \left| a _ {n} x _ {0} ^ {n} \cdot \frac {x ^ {n}}{x _ {0} ^ {n}} \right| = \left| a _ {n} x _ {0} ^ {n} \right| \cdot \left| \frac {x}{x _ {0}} \right| ^ {n} \leqslant M \left| \frac {x}{x _ {0}} \right| ^ {n}.
$$

因为当 $|x| < |x_0|$ 时，等比级数 $\sum_{n=0}^{\infty} M \left| \frac{x}{x_0} \right|^n$ 收敛（公比 $\left| \frac{x}{x_0} \right| < 1$），所以级数 $\sum_{n=0}^{\infty} |a_n x^n|$ 收敛，也就是级数 $\sum_{n=0}^{\infty} a_n x^n$ 绝对收敛.

定理的第二部分可用反证法证明. 假设幂级数当 $x = x_0$ 时发散而有一点 $x_1$ 适合 $|x_1| > |x_0|$ 使级数收敛, 则根据本定理的第一部分, 级数当 $x = x_0$ 时应收敛, 这与假设矛盾. 定理得证.

定理1表明,如果幂级数在 $x = x_0$ 处收敛,那么对于开区间 $(-\left|x_0\right|, \left|x_0\right|)$ 内的任何 $x$,幂级数都收敛;如果幂级数在 $x = x_0$ 处发散,那么对于闭区间 $\left[-\left|x_0\right|, \left|x_0\right|\right]$ 外的任何 $x$,幂级数都发散.

设已给幂级数在数轴上既有收敛点(不仅是原点)也有发散点.现在从原点沿数轴向右方走,最初只遇到收敛点,然后就只遇到发散点.这两部分的界点可能是收敛点也可能是发散点.从原点沿数轴向左方走情形也是如此.两个界点P与 $P'$ 在原点的两侧,

且由定理1可以证明它们到原点的距离是一样的(图12-3).

![](images/page_270_image_6.jpg)

<details>
<summary>text_image</summary>

P'
-R
O
P
R
x
</details>

图12-3

从上面的几何说明,得到下述重要推论:

推论 如果幂级数 $\sum_{n=0}^{\infty} a_n x^n$ 不是仅在 $x=0$ 一点收敛, 也不是在整个数轴上都收敛, 那么必有一个确定的正数 $R$ 存在, 使得

当 $|x| < R$ 时，幂级数绝对收敛；

当  $\left|x\right|>R$  时, 幂级数发散;

当 x=R 与 x=-R 时, 幂级数可能收敛也可能发散.

正数 $R$ 通常叫做幂级数(3-3)的收敛半径.开区间 $(-R,R)$ 叫做幂级数(3-3)的收敛区间.再由幂级数在 $x = \pm R$ 处的收敛性就可以决定它的收敛域是 $(-R,R)$, $[-R,R)$, $(-R,R]$ 或 $[-R,R]$ 这四个区间之一.

如果幂级数(3-3)只在 $x = 0$ 处收敛, 这时收敛域只有一点 $x = 0$, 但为了方便起见, 规定这时收敛半径 $R = 0$; 如果幂级数(3-3)对一切 $x$ 都收敛, 则规定收敛半径 $R = +\infty$, 这时收敛域是 $(- \infty, +\infty)$. 这两种情形确实都是存在的, 见下面的例2及例3.

关于幂级数的收敛半径的求法,有下面的定理.

定理2 如果

$$
\lim _ {n \to \infty} \left| \frac {a _ {n + 1}}{a _ {n}} \right| = \rho ,
$$

其中 $a_{n}, a_{n+1}$ 是幂级数 $\sum_{n=0}^{\infty} a_{n} x^{n}$ 的相邻两项的系数, 那么这幂级数的收敛半径

$$
R = \left\{ \begin{array}{l l} \frac {1}{\rho}, & \rho \neq 0, \\ + \infty , & \rho = 0, \\ 0, & \rho = + \infty . \end{array} \right.
$$

证 考察幂级数(3-3)的各项取绝对值所成的级数

$$
\left| a _ {0} \right| + \left| a _ {1} x \right| + \left| a _ {2} x ^ {2} \right| + \dots + \left| a _ {n} x ^ {n} \right| + \dots , \tag {3-4}
$$

这级数相邻两项之比为

$$
\frac {\mid a _ {n + 1} x ^ {n + 1} \mid}{\mid a _ {n} x ^ {n} \mid} = \left| \frac {a _ {n + 1}}{a _ {n}} \right| \mid x \mid .
$$

(1) 如果  $\lim_{n\to\infty}\left|\frac{a_{n+1}}{a_n}\right|=\rho\quad(\rho\neq0)$  存在, 根据比值审敛法, 那么当  $\rho|x|<1$  即  $|x|<\frac{1}{\rho}$  时, 级数 (3-4) 收敛, 从而级数 (3-3) 绝对收敛; 当  $\rho|x|>1$  即  $|x|>\frac{1}{\rho}$  时, 级数 (3-4) 发散并且从某一个 n 开始

$$
\mid a _ {n + 1} x ^ {n + 1} \mid > \mid a _ {n} x ^ {n} \mid ,
$$

因此一般项 $|a_{n}x^{n}|$ 不能趋于零,所以 $a_{n}x^{n}$ 也不能趋于零,从而级数(3-3)发散.于是收敛半径 $R=\frac{1}{\rho}$ .

(2) 如果  $\rho=0$ ，那么对任何  $x\neq0$ ，有  $\frac{\left|a_{n+1}x^{n+1}\right|}{\left|a_{n}x^{n}\right|}\rightarrow0\quad(n\rightarrow\infty)$ ，所以级数(3-4)收敛，从而级数(3-3)绝对收敛。于是  $R=+\infty$ 。
（3）如果  $\rho=+\infty$ ，那么对于除 x=0 外的其他一切 x 值，级数(3-3)必发散，否则由定理1知道将有点  $x\neq0$  使级数(3-4)收敛。于是 R=0。

例1 求幂级数 $x - \frac{x^2}{2} +\frac{x^3}{3} -\dots +(-1)^{n - 1}\frac{x^n}{n} +\dots$ 的收敛半径与收敛域.

解 因为

$$
\rho = \lim _ {n \to \infty} \left| \frac {a _ {n + 1}}{a _ {n}} \right| = \lim _ {n \to \infty} \frac {\frac {1}{n + 1}}{\frac {1}{n}} = 1,
$$

所以收敛半径

$$
R = \frac {1}{\rho} = 1.
$$

对于端点 $x = -1$ ，级数成为

图

例题精讲

12-5

$$
- 1 - \frac {1}{2} - \frac {1}{3} - \dots - \frac {1}{n} - \dots ,
$$

此级数发散；

对于端点 x=1, 级数成为交错级数

$$
1 - \frac {1}{2} + \frac {1}{3} - \dots + (- 1) ^ {n - 1} \frac {1}{n} + \dots ,
$$

此级数收敛.因此,收敛域是 $(-1,1]$ .

例 2 求幂级数  $1 + x + \frac{1}{2!}x^{2} + \cdots + \frac{1}{n!}x^{n} + \cdots$  的收敛域.

解 因为

$$
\rho = \lim _ {n \to \infty} \left| \frac {a _ {n + 1}}{a _ {n}} \right| = \lim _ {n \to \infty} \frac {\frac {1}{(n + 1) !}}{\frac {1}{n !}} = \lim _ {n \to \infty} \frac {1}{n + 1} = 0,
$$

所以收敛半径  $R = +\infty$ ，从而收敛域是  $(- \infty, +\infty)$ .

例3 求幂级数 $\sum_{n=0}^{\infty} n! x^n$ 的收敛半径（规定 $0! = 1$）.

解 因为

$$
\rho = \lim _ {n \to \infty} \left| \frac {a _ {n + 1}}{a _ {n}} \right| = \lim _ {n \to \infty} \frac {(n + 1) !}{n !} = + \infty ,
$$

所以收敛半径 R=0，即级数仅在点 x=0 处收敛.

例4 求幂级数 $\sum_{n=0}^{\infty} \frac{(2n)!}{(n!)^2} x^{2n}$ 的收敛半径.

解 级数缺少奇次幂的项,定理 2 不能直接应用.我们根据比值审敛法来求收敛半径:

$$
\lim _ {n \to \infty} \left| \frac {\frac {[ 2 (n + 1) ] !}{[ (n + 1) ! ] ^ {2}} x ^ {2 (n + 1)}}{\frac {(2 n) !}{(n !) ^ {2}} x ^ {2 n}} \right| = 4 | x | ^ {2}.
$$

当 $4|x|^2 < 1$ 即 $|x| < \frac{1}{2}$ 时，级数收敛；当 $4|x|^2 > 1$ 即 $|x| > \frac{1}{2}$ 时，级数发散.所以收敛半径 $R = \frac{1}{2}$.

例 5 求幂级数  $\sum_{n=1}^{\infty}\frac{(x-1)^{n}}{2^{n}\cdot n}$  的收敛域.

解 令 $t = x - 1$ ，上述级数变为

$$
\sum_ {n = 1} ^ {\infty} \frac {t ^ {n}}{2 ^ {n} \cdot n}.
$$

因为

$$
\rho = \lim _ {n \to \infty} \left| \frac {a _ {n + 1}}{a _ {n}} \right| = \lim _ {n \to \infty} \frac {2 ^ {n} \cdot n}{2 ^ {n + 1} (n + 1)} = \frac {1}{2},
$$

所以收敛半径 $R = 2$ 收敛区间为 $|t| < 2$ ，即 $-1 < x < 3$

当 $x = -1$ 时，级数成为 $\sum_{n=1}^{\infty} \frac{(-1)^n}{n}$，这级数收敛；当 $x = 3$ 时，级数成为 $\sum_{n=1}^{\infty} \frac{1}{n}$，这级数发散。因此原级数的收敛域为 $[-1, 3)$。

## 三、幂级数的运算

设幂级数

$$
a _ {0} + a _ {1} x + a _ {2} x ^ {2} + \dots + a _ {n} x ^ {n} + \dots
$$

及

$$
b _ {0} + b _ {1} x + b _ {2} x ^ {2} + \dots + b _ {n} x ^ {n} + \dots
$$

分别在区间 $(-R,R)$ 及 $(-R',R')$ 内收敛,对于这两个幂级数,可以进行下列四则运算:

加法

$$
\begin{array}{l} (a _ {0} + a _ {1} x + a _ {2} x ^ {2} + \dots + a _ {n} x ^ {n} + \dots) + (b _ {0} + b _ {1} x + b _ {2} x ^ {2} + \dots + b _ {n} x ^ {n} + \dots) \\ = (a _ {0} + b _ {0}) + (a _ {1} + b _ {1}) x + (a _ {2} + b _ {2}) x ^ {2} + \dots + (a _ {n} + b _ {n}) x ^ {n} + \dots . \\ \end{array}
$$

减法

$$
\begin{array}{l} (a _ {0} + a _ {1} x + a _ {2} x ^ {2} + \dots + a _ {n} x ^ {n} + \dots) - (b _ {0} + b _ {1} x + b _ {2} x ^ {2} + \dots + b _ {n} x ^ {n} + \dots) \\ = (a _ {0} - b _ {0}) + (a _ {1} - b _ {1}) x + (a _ {2} - b _ {2}) x ^ {2} + \dots + (a _ {n} - b _ {n}) x ^ {n} + \dots . \\ \end{array}
$$

根据收敛级数的基本性质2,上面两式在 $(-R,R)$ 与 $(-R',R')$ 中较小的区间内成立.

乘法

$$
\begin{array}{l} (a _ {0} + a _ {1} x + a _ {2} x ^ {2} + \dots + a _ {n} x ^ {n} + \dots) (b _ {0} + b _ {1} x + b _ {2} x ^ {2} + \dots + b _ {n} x ^ {n} + \dots) \\ = a _ {0} b _ {0} + (a _ {0} b _ {1} + a _ {1} b _ {0}) x + (a _ {0} b _ {2} + a _ {1} b _ {1} + a _ {2} b _ {0}) x ^ {2} + \dots + (a _ {0} b _ {n} + a _ {1} b _ {n - 1} + \dots + a _ {n} b _ {0}) x ^ {n} + \dots . \\ \end{array}
$$

这是两个幂级数的柯西乘积. 可以证明上式在 $(-R, R)$ 与 $(-R', R')$ 中较小的区间内成立.

除法

$$
\frac {a _ {0} + a _ {1} x + a _ {2} x ^ {2} + \cdots + a _ {n} x ^ {n} + \cdots}{b _ {0} + b _ {1} x + b _ {2} x ^ {2} + \cdots + b _ {n} x ^ {n} + \cdots} = c _ {0} + c _ {1} x + c _ {2} x ^ {2} + \dots + c _ {n} x ^ {n} + \dots ,
$$

这里假设 $b_{0} \neq 0$. 为了决定系数 $c_{0}, c_{1}, c_{2}, \cdots, c_{n}, \cdots$, 可以将级数 $\sum_{n=0}^{\infty} b_{n} x^{n}$ 与 $\sum_{n=0}^{\infty} c_{n} x^{n}$ 相

![](images/page_273_image_23.jpg)

释疑解难

12-3

乘,并令乘积中各项的系数分别等于级数  $\sum_{n=0}^{\infty}a_{n}x^{n}$  中同次幂的系数,即得

$$
\begin{array}{l} a _ {0} = b _ {0} c _ {0}, \\ a _ {1} = b _ {1} c _ {0} + b _ {0} c _ {1}, \\ a _ {2} = b _ {2} c _ {0} + b _ {1} c _ {1} + b _ {0} c _ {2}, \\ \end{array}
$$

...

由这些方程就可以顺序地求出 $c_{0}, c_{1}, c_{2}, \cdots, c_{n}, \cdots$.

相除后所得的幂级数 $\sum_{n=0}^{\infty} c_n x^n$ 的收敛区间可能比原来两级数的收敛区间小得多①.

关于幂级数的和函数有下列重要性质②:

性质1 幂级数 $\sum_{n=0}^{\infty} a_n x^n$ 的和函数 $s(x)$ 在其收敛域 $I$ 上连续.

性质2 幂级数 $\sum_{n=0}^{\infty} a_n x^n$ 的和函数 $s(x)$ 在其收敛域 $I$ 上可积，并有逐项积分公式

$$
\int_ {0} ^ {x} s (t) \mathrm{d} t = \int_ {0} ^ {x} \left[ \sum_ {n = 0} ^ {\infty} a _ {n} t ^ {n} \right] \mathrm{d} t = \sum_ {n = 0} ^ {\infty} \int_ {0} ^ {x} a _ {n} t ^ {n} \mathrm{d} t = \sum_ {n = 0} ^ {\infty} \frac {a _ {n}}{n + 1} x ^ {n + 1} \quad (x \in I), \tag {3-5}
$$

逐项积分后所得到的幂级数和原级数有相同的收敛半径.

性质3 幂级数 $\sum_{n=0}^{\infty} a_n x^n$ 的和函数 $s(x)$ 在其收敛区间 $(-R, R)$ 内可导，且有逐项求导公式

$$
s ^ {\prime} (x) = \left(\sum_ {n = 0} ^ {\infty} a _ {n} x ^ {n}\right) ^ {\prime} = \sum_ {n = 0} ^ {\infty} \left(a _ {n} x ^ {n}\right) ^ {\prime} = \sum_ {n = 1} ^ {\infty} n a _ {n} x ^ {n - 1} \quad (\mid x \mid <   R), \tag {3-6}
$$

逐项求导后所得到的幂级数和原级数有相同的收敛半径.

反复应用上述结论可得: 幂级数  $\sum_{n=0}^{\infty}a_{n}x^{n}$  的和函数  $s(x)$  在其收敛区间  $(-R,R)$  内具有任意阶导数.

例6 求幂级数 $\sum_{n=0}^{\infty} \frac{x^n}{n+1}$ 的和函数.

解 先求收敛域.由

① 例如

$$
\frac {1}{1 - x} = 1 + x + x ^ {2} + \dots + x ^ {n} + \dots .
$$

级数  $\sum_{n=0}^{\infty}a_{n}x^{n}=1+0x+\cdots+0x^{n}+\cdots$  与  $\sum_{n=0}^{\infty}b_{n}x^{n}=1-x+0x^{2}+\cdots+0x^{n}+\cdots$  在整个数轴上收敛，但级数  $\sum_{n=0}^{\infty}c_{n}x^{n}=\sum_{n=0}^{\infty}x^{n}$  仅在区间  $(-1,1)$  内收敛.

② 证明见本章第六节第二目.

$$
\lim _ {n \to \infty} \left| \frac {a _ {n + 1}}{a _ {n}} \right| = \lim _ {n \to \infty} \frac {n + 1}{n + 2} = 1,
$$

得收敛半径 R=1.

在端点 $x = -1$ 处，幂级数成为 $\sum_{n=0}^{\infty} \frac{(-1)^n}{n+1}$，是收敛的交错级数；在端点 $x = 1$ 处，幂级数成为 $\sum_{n=0}^{\infty} \frac{1}{n+1}$，是发散的。因此收敛域为 $I = [-1, 1)$。

设和函数为 $s(x)$ ，即

$$
s (x) = \sum_ {n = 0} ^ {\infty} \frac {x ^ {n}}{n + 1}, \quad x \in [ - 1, 1).
$$

于是

$$
xs(x) = \sum_{n = 0}^{\infty}\frac{x^{n + 1}}{n + 1}.
$$

利用性质 3, 逐项求导, 并由

$$
\frac {1}{1 - x} = 1 + x + x ^ {2} + \dots + x ^ {n} + \dots \quad (- 1 <   x <   1),
$$

得

$$
\left[ x s (x) \right] ^ {\prime} = \sum_ {n = 0} ^ {\infty} \left(\frac {x ^ {n + 1}}{n + 1}\right) ^ {\prime} = \sum_ {n = 0} ^ {\infty} x ^ {n} = \frac {1}{1 - x} \quad (\mid x \mid <   1).
$$

对上式从0到 $x$ 积分，得

$$
x s (x) = \int_ {0} ^ {x} \frac {1}{1 - t} \mathrm{d} t = - \ln (1 - x) \quad (- 1 \leqslant x <   1).
$$

于是, 当  $x \neq 0$  时, 有  $s(x) = -\frac{1}{x} \ln(1 - x)$ . 而  $s(0)$  可由  $s(0) = a_{0} = 1$  得出, 也可由和函数的连续性得到

$$
s (0) = \lim _ {x \to 0} s (x) = \lim _ {x \to 0} \left[ - \frac {1}{x} \ln (1 - x) \right] = 1.
$$

故

$$
s (x) = \left\{ \begin{array}{l l} - \frac {1}{x} \ln (1 - x), & x \in [ - 1, 0) \cup (0, 1), \\ 1, & x = 0. \end{array} \right.
$$

## 习题12-3

1. 下题中给出了四个结论,从中选出一个正确的结论:

![](images/page_275_image_21.jpg)

例题精讲

12-6

已知 $\alpha > 0$，若幂级数 $\sum_{n=1}^{\infty} a_n (x + \alpha)^n$ 在 $x = 0$ 处发散，在 $x = -2\alpha$ 处收敛，则幂级数 $\sum_{n=1}^{\infty} a_n (x - \alpha)^n$ 的收敛域为（ ）.

(A) $[-2\alpha, 0)$

(B) $[0, 2\alpha)$

(C) $(-2\alpha, 0]$

(D) $(0,2\alpha ]$

2. 求下列幂级数的收敛区间:

(1)  $x+2x^{2}+3x^{3}+\cdots+nx^{n}+\cdots;$
(3) $\frac{x}{2}+\frac{x^{2}}{2\times4}+\frac{x^{3}}{2\times4\times6}+\cdots+\frac{x^{n}}{2\times4\times\cdots\times(2n)}+\cdots;$
(5) $\frac{2}{2}x+\frac{2^{2}}{5}x^{2}+\frac{2^{3}}{10}x^{3}+\cdots+\frac{2^{n}}{n^{2}+1}x^{n}+\cdots;$
(7) $\sum_{n=1}^{\infty} \frac{2n-1}{2^n} x^{2n-2}$;

(2) $1-x+\frac{x^{2}}{2^{2}}+\cdots+(-1)^{n}\frac{x^{n}}{n^{2}}+\cdots;$

(4) $\frac{x}{1\times3}+\frac{x^{2}}{2\times3^{2}}+\frac{x^{3}}{3\times3^{3}}+\cdots+\frac{x^{n}}{n\times3^{n}}+\cdots;$

(6) $\sum_{n=1}^{\infty}(-1)^{n}\frac{x^{2n+1}}{2n+1}$;

(8) $\sum_{n=1}^{\infty} \frac{(x-5)^n}{\sqrt{n}}.$

3. 利用逐项求导或逐项积分, 求下列级数的和函数:

(1)  $\sum_{n=1}^{\infty}nx^{n-1}$ ;
(3) $x+\frac{x^{3}}{3}+\frac{x^{5}}{5}+\cdots+\frac{x^{2n-1}}{2n-1}+\cdots;$

(2) $\sum_{n=1}^{\infty} \frac{x^{4n+1}}{4n+1}$;

(4) $\sum_{n=1}^{\infty}(n+2)x^{n+3}$.

## 第四节 函数展开成幂级数

前面讨论了幂级数的收敛域及其和函数的性质.但在许多应用中,我们遇到的却是相反的问题:给定函数 $f(x)$ ,要考虑它是否能在某个区间内“展开成幂级数”,就是说,是否能找到这样一个幂级数,它在某区间内收敛,且其和恰好就是给定的函数 $f(x)$ .如果能找到这样的幂级数,我们就说,函数 $f(x)$ 在该区间内能展开成幂级数,而这个幂级数在该区间内就表达了函数 $f(x)$ .

假设函数 $f(x)$ 在点 $x_0$ 的某邻域 $U(x_0)$ 内能展开成幂级数，即有

$$
f (x) = a _ {0} + a _ {1} (x - x _ {0}) + a _ {2} (x - x _ {0}) ^ {2} + \dots + a _ {n} (x - x _ {0}) ^ {n} + \dots , \quad x \in U (x _ {0}), \tag {4-1}
$$

则根据和函数的性质, 可知  $f(x)$  在  $U(x_{0})$  内应具有任意阶导数, 且

$$
f ^ {(n)} (x) = n! a _ {n} + (n + 1)! a _ {n + 1} (x - x _ {0}) + \frac {(n + 2) !}{2 !} a _ {n + 2} (x - x _ {0}) ^ {2} + \dots ,
$$

由此可得

$$
f ^ {(n)} (x _ {0}) = n! a _ {n},
$$

于是

$$
a _ {n} = \frac {1}{n !} f ^ {(n)} (x _ {0}) \quad (n = 0, 1, 2, \dots). \tag {4-2}
$$

这就表明,如果函数 $f(x)$ 有幂级数展开式(4-1),那么该幂级数的系数 $a_{n}$ 由公式(4-2)确定,即该幂级数必为

$$
f (x _ {0}) + f ^ {\prime} (x _ {0}) (x - x _ {0}) + \dots + \frac {1}{n !} f ^ {(n)} (x _ {0}) (x - x _ {0}) ^ {n} + \dots = \sum_ {n = 0} ^ {\infty} \frac {1}{n !} f ^ {(n)} (x _ {0}) (x - x _ {0}) ^ {n}, \tag {4-3}
$$

而展开式必为

$$
f (x) = \sum_ {n = 0} ^ {\infty} \frac {1}{n !} f ^ {(n)} \left(x _ {0}\right) \left(x - x _ {0}\right) ^ {n}, \quad x \in U \left(x _ {0}\right). \tag {4-4}
$$

幂级数(4-3)叫做函数 $f(x)$ 在点 $x_{0}$ 处的泰勒级数.展开式(4-4)叫做函数 $f(x)$ 在点 $x_{0}$ 处的泰勒展开式.

由以上讨论可知,函数 $f(x)$ 在 $U(x_{0})$ 内能展开成幂级数的充分必要条件是泰勒展开式(4-4)成立,也就是泰勒级数(4-3)在 $U(x_{0})$ 内收敛,且收敛到 $f(x)$.

下面讨论泰勒展开式(4-4)成立的条件.

定理 设函数 $f(x)$ 在点 $x_0$ 的某一邻域 $U(x_0)$ 内具有各阶导数，则 $f(x)$ 在该邻域内能展开成泰勒级数的充分必要条件是在该邻域内 $f(x)$ 的泰勒公式中的余项 $R_n(x)$ 当 $n \to \infty$ 时的极限为零，即

$$
\lim _ {n \to \infty} R _ {n} (x) = 0, \quad x \in U (x _ {0}).
$$

证 $f(x)$ 的 $n$ 阶泰勒公式为（见第三章第三节）

$$
f (x) = p _ {n} (x) + R _ {n} (x),
$$

其中

$$
p _ {n} (x) = f (x _ {0}) + f ^ {\prime} (x _ {0}) (x - x _ {0}) + \dots + \frac {1}{n !} f ^ {(n)} (x _ {0}) (x - x _ {0}) ^ {n}
$$

叫做函数 $f(x)$ 的n次泰勒多项式,而

$$
R _ {n} (x) = f (x) - p _ {n} (x)
$$

就是定理中所指的余项.

由于 n 次泰勒多项式  $p_{n}(x)$  就是级数 (4-3) 的前  $n+1$  项部分和, 根据级数收敛的定义, 即有

$$
\begin{array}{l} \sum_ {n = 0} ^ {\infty} \frac {1}{n !} f ^ {(n)} (x _ {0}) (x - x _ {0}) ^ {n} = f (x), \quad x \in U (x _ {0}) \\ \Leftrightarrow \lim _ {n \to \infty} p _ {n} (x) = f (x), \quad x \in U (x _ {0}) \\ \Leftrightarrow \lim _ {n \to \infty} [ f (x) - p _ {n} (x) ] = 0, \quad x \in U (x _ {0}) \\ \Leftrightarrow \lim _ {n \to \infty} R _ {n} (x) = 0, \quad x \in U (x _ {0}). \\ \end{array}
$$

下面着重讨论 $x_0 = 0$ 的情形.在(4-3)式中，取 $x_0 = 0$ ，得

$$
f (0) + f ^ {\prime} (0) x + \dots + \frac {1}{n !} f ^ {(n)} (0) x ^ {n} + \dots = \sum_ {n = 0} ^ {\infty} \frac {1}{n !} f ^ {(n)} (0) x ^ {n}, \tag {4-5}
$$

级数(4-5)称为函数 $f(x)$ 的麦克劳林级数.若 $f(x)$ 能在 $(-r,r)$ 内展开成x的幂级数，则有

$$
f (x) = \sum_ {n = 0} ^ {\infty} \frac {1}{n !} f ^ {(n)} (0) x ^ {n} \quad (\mid x \mid <   r), \tag {4-6}
$$

(4-6)式称为函数 $f(x)$ 的麦克劳林展开式.

要把函数 $f(x)$ 展开成x的幂级数,可以按照下列步骤进行:

第一步 求出 $f(x)$ 的各阶导数 $f'(x), f''(x), \cdots, f^{(n)}(x), \cdots$，如果在 $x = 0$ 处某阶导数不存在，就停止进行，例如在 $x = 0$ 处，$f(x) = x^{7/3}$ 的三阶导数不存在，它就不能展开为 $x$ 的幂级数.

第二步 求出函数及其各阶导数在 x=0 处的值

$$
f (0), f ^ {\prime} (0), f ^ {\prime \prime} (0), \dots , f ^ {(n)} (0), \dots .
$$

第三步 写出幂级数

$$
f (0) + f ^ {\prime} (0) x + \frac {f ^ {\prime \prime} (0)}{2 !} x ^ {2} + \dots + \frac {f ^ {(n)} (0)}{n !} x ^ {n} + \dots ,
$$

并求出收敛半径 R.

第四步 利用余项 $R_{n}(x)$ 的表达式 $R_{n}(x) = \frac{1}{(n + 1)!} f^{(n + 1)}(\theta x)x^{n + 1}(0 < \theta < 1)$，考察当 $x$ 在区间 $(-R, R)$ 内时余项 $R_{n}(x)$ 的极限是不是零。如果为零，那么函数 $f(x)$ 在区间 $(-R, R)$ 内的幂级数展开式为

$$
f (x) = f (0) + f ^ {\prime} (0) x + \frac {f ^ {\prime \prime} (0)}{2 !} x ^ {2} + \dots + \frac {f ^ {(n)} (0)}{n !} x ^ {n} + \dots \quad (- R <   x <   R).
$$

例 1 将函数  $f(x)=\mathrm{e}^{x}$  展开成 x 的幂级数.

解 所给函数的各阶导数为  $f^{(n)}(x)=\mathrm{e}^{x}\quad(n=1,2,\cdots)$ ，因此  $f^{(n)}(0)=1\quad(n=0,1,2,\cdots)$ ，这里  $f^{(0)}(0)=f(0)$ 。于是得级数

$$
1 + x + \frac {x ^ {2}}{2 !} + \dots + \frac {x ^ {n}}{n !} + \dots ,
$$

它的收敛半径  $R = +\infty$ .

对于任何有限的数 $x$ 与 $\xi$ （$\xi$ 在0与 $x$ 之间），余项的绝对值为

$$
\left| R _ {n} (x) \right| = \left| \frac {\mathrm{e} ^ {\xi}}{(n + 1) !} x ^ {n + 1} \right| <   \mathrm{e} ^ {| x |} \cdot \frac {| x | ^ {n + 1}}{(n + 1) !}.
$$

因 $\mathrm{e}^{|x|}$ 为有限值，而 $\frac{|x|^{n + 1}}{(n + 1)!}$ 是收敛级数 $\sum_{n = 0}^{\infty}\frac{|x|^{n + 1}}{(n + 1)!}$ 的一般项，所以当 $n\to \infty$ 时，

$$
\mathrm{e} ^ {| x |} \cdot \frac {| x | ^ {n + 1}}{(n + 1) !} \rightarrow 0,
$$

即当 $n\to \infty$ 时，有 $\mid R_n(x)\mid \rightarrow 0.$ 于是得展开式

$$
\mathrm{e} ^ {x} = 1 + x + \frac {x ^ {2}}{2 !} + \dots + \frac {x ^ {n}}{n !} + \dots
$$

$$
(- \infty <   x <   + \infty). \tag {4-7}
$$

如果在 x=0 处附近, 用级数的部分和 (即多项式) 来近似代替  $e^{x}$ , 那么随着项数的增加, 它们就越来越接近于  $e^{x}$ , 如图 12-4 所示.

例 2 将函数  $f(x)=\sin x$  展开成 x 的幂级数.

![](images/page_279_chart_6.jpg)

<details>
<summary>line</summary>

| Function | Equation |
| --- | --- |
| Solid line | y=e^x |
| Dashed line | y=1+x + x^2/2 + x^3/6 |
| Dash-dotted line | y=1+x |
</details>

图12-4

解 所给函数的各阶导数为

$$
f ^ {(n)} (x) = \sin \left(x + n \cdot \frac {\pi}{2}\right) \quad (n = 1, 2, \dots),
$$

$f^{(n)}(0)$ 顺序循环地取 $0,1,0,-1,\cdots(n=0,1,2,3,\cdots)$ ，于是得级数

$$
x - \frac {x ^ {3}}{3 !} + \frac {x ^ {5}}{5 !} - \dots + (- 1) ^ {n} \frac {x ^ {2 n + 1}}{(2 n + 1) !} + \dots ,
$$

它的收敛半径  $R = +\infty$ .

对于任何有限的数 $x$ 与 $\xi$ （$\xi$ 在0与 $x$ 之间），余项的绝对值当 $n \to \infty$ 时的极限为零:

$$
\mid R _ {n} (x) \mid = \left| \frac {\sin \left[ \xi + \frac {(n + 1) \pi}{2} \right]}{(n + 1) !} x ^ {n + 1} \right| \leqslant \frac {\mid x \mid^ {n + 1}}{(n + 1) !} \rightarrow 0 \quad (n \rightarrow \infty).
$$

因此得展开式

$$
\sin x = x - \frac {x ^ {3}}{3 !} + \frac {x ^ {5}}{5 !} - \dots + (- 1) ^ {n} \frac {x ^ {2 n + 1}}{(2 n + 1) !} + \dots \quad (- \infty <   x <   + \infty). \tag {4-8}
$$

以上将函数展开成幂级数的例子, 是直接按公式 $a_{n} = \frac{f^{(n)}(0)}{n!}$ 计算幂级数的系数, 最后考察余项 $R_{n}(x)$ 是否趋于零. 这种直接展开的方法计算量较大, 而且研究余项即使在初等函数中也不是一件容易的事. 下面介绍间接展开的方法, 这就是利用一些已知的函数展开式, 通过幂级数的运算 (如四则运算、逐项求导、逐项积分) 以及变量代换等, 将所给函数展开成幂级数. 这样做不但计算简单, 而且可以避免研究余项.

前面我们已经求得的幂级数展开式有

$$
\mathrm{e} ^ {x} = \sum_ {n = 0} ^ {\infty} \frac {1}{n !} x ^ {n} \quad (- \infty <   x <   + \infty), \tag {4-7}
$$

$$
\sin x = \sum_ {n = 0} ^ {\infty} \frac {(- 1) ^ {n}}{(2 n + 1) !} x ^ {2 n + 1} \quad (- \infty <   x <   + \infty), \tag {4-8}
$$

$$
\frac {1}{1 + x} = \sum_ {n = 0} ^ {\infty} (- 1) ^ {n} x ^ {n} \quad (- 1 <   x <   1). \tag {4-9}
$$

利用这三个展开式,可以求得许多函数的幂级数展开式.例如

对(4-9)式两端从0到x积分,可得

$$
\ln (1 + x) = \sum_ {n = 0} ^ {\infty} \frac {(- 1) ^ {n}}{n + 1} x ^ {n + 1} = \sum_ {n = 1} ^ {\infty} \frac {(- 1) ^ {n - 1}}{n} x ^ {n} \quad (- 1 <   x \leqslant 1), \tag {4-10}
$$

对(4-8)式两端求导,即得

$$
\cos x = \sum_ {n = 0} ^ {\infty} \frac {(- 1) ^ {n}}{(2 n) !} x ^ {2 n} \quad (- \infty <   x <   + \infty), \tag {4-11}
$$

把(4-7)式中的 $x$ 换成 $x \ln a$, 可得

$$
a ^ {x} = \mathrm{e} ^ {x \ln a} = \sum_ {n = 0} ^ {\infty} \frac {(\ln a) ^ {n}}{n !} x ^ {n} \quad (- \infty <   x <   + \infty),
$$

把(4-9)式中的 x 换成  $x^{2}$ ，可得

$$
\frac {1}{1 + x ^ {2}} = \sum_ {n = 0} ^ {\infty} (- 1) ^ {n} x ^ {2 n} \quad (- 1 <   x <   1),
$$

对上式从 0 到 x 积分, 可得

$$
\arctan x = \sum_ {n = 0} ^ {\infty} \frac {(- 1) ^ {n}}{2 n + 1} x ^ {2 n + 1} \quad (- 1 \leqslant x \leqslant 1).
$$

(4-7)、(4-8)、(4-9)、(4-10)、(4-11)等五个幂级数展开式是最常用的,记住前三个,后两个也就掌握了.

下面再举几个用间接法把函数展开成幂级数的例子.

例 3 把函数  $f(x)=(1-x)\ln(1+x)$  展开成 x 的幂级数.

解 由 $\ln (1 + x) = \sum_{n=1}^{\infty} \frac{(-1)^{n-1}}{n} x^n (-1 < x \leqslant 1)$ 得

$$
\begin{array}{l} f (x) = (1 - x) \sum_ {n = 1} ^ {\infty} \frac {(- 1) ^ {n - 1}}{n} x ^ {n} = \sum_ {n = 1} ^ {\infty} \frac {(- 1) ^ {n - 1}}{n} x ^ {n} - \sum_ {n = 1} ^ {\infty} \frac {(- 1) ^ {n - 1}}{n} x ^ {n + 1} \\ = \sum_ {n = 1} ^ {\infty} \frac {(- 1) ^ {n - 1}}{n} x ^ {n} - \sum_ {n = 2} ^ {\infty} \frac {(- 1) ^ {n}}{n - 1} x ^ {n} = x + \sum_ {n = 2} ^ {\infty} \frac {(- 1) ^ {n - 1} (2 n - 1)}{n (n - 1)} x ^ {n} \quad (- 1 <   x \leqslant 1). \\ \end{array}
$$

例 4 将函数  $\sin x$  展开成  $\left(x - \frac{\pi}{4}\right)$  的幂级数.

解 因为

$$
\begin{array}{l} \sin x = \sin \left[ \frac {\pi}{4} + \left(x - \frac {\pi}{4}\right) \right] = \sin \frac {\pi}{4} \cos \left(x - \frac {\pi}{4}\right) + \cos \frac {\pi}{4} \sin \left(x - \frac {\pi}{4}\right) \\ = \frac {1}{\sqrt {2}} \left[ \cos \left(x - \frac {\pi}{4}\right) + \sin \left(x - \frac {\pi}{4}\right) \right], \\ \end{array}
$$

并且有

$$
\cos \left(x - \frac {\pi}{4}\right) = 1 - \frac {\left(x - \frac {\pi}{4}\right) ^ {2}}{2 !} + \frac {\left(x - \frac {\pi}{4}\right) ^ {4}}{4 !} - \dots + \frac {(- 1) ^ {n}}{(2 n) !} \left(x - \frac {\pi}{4}\right) ^ {2 n} + \dots \quad (- \infty <   x <   + \infty),
$$

$$
\sin \left(x - \frac {\pi}{4}\right) = \left(x - \frac {\pi}{4}\right) - \frac {\left(x - \frac {\pi}{4}\right) ^ {3}}{3 !} + \frac {\left(x - \frac {\pi}{4}\right) ^ {5}}{5 !} - \dots + \frac {(- 1) ^ {n}}{(2 n + 1) !} \left(x - \frac {\pi}{4}\right) ^ {2 n + 1} + \dots . \quad (- \infty <   x <   + \infty),
$$

所以

$$
\begin{array}{l} \sin x = \frac {1}{\sqrt {2}} \left[ 1 + \left(x - \frac {\pi}{4}\right) - \frac {\left(x - \frac {\pi}{4}\right) ^ {2}}{2 !} - \frac {\left(x - \frac {\pi}{4}\right) ^ {3}}{3 !} + \dots + \right. \\ \frac {(- 1) ^ {n}}{(2 n) !} \left(x - \frac {\pi}{4}\right) ^ {2 n} + \frac {(- 1) ^ {n}}{(2 n + 1) !} \left(x - \frac {\pi}{4}\right) ^ {2 n + 1} + \dots ] \quad (- \infty <   x <   + \infty). \\ \end{array}
$$

例 5 将函数  $f(x)=\frac{1}{x^{2}+4x+3}$  展开成  $(x-1)$  的幂级数.

解 因为

$$
\begin{array}{l} f (x) = \frac {1}{x ^ {2} + 4 x + 3} = \frac {1}{(x + 1) (x + 3)} = \frac {1}{2 (1 + x)} - \frac {1}{2 (3 + x)} \\ = \frac {1}{4 \left(1 + \frac {x - 1}{2}\right)} - \frac {1}{8 \left(1 + \frac {x - 1}{4}\right)}, \\ \end{array}
$$

而

$$
\begin{array}{l} \frac {1}{4 \left(1 + \frac {x - 1}{2}\right)} = \frac {1}{4} \sum_ {n = 0} ^ {\infty} \frac {(- 1) ^ {n}}{2 ^ {n}} (x - 1) ^ {n} \quad (- 1 <   x <   3), \\ \frac {1}{8 \left(1 + \frac {x - 1}{4}\right)} = \frac {1}{8} \sum_ {n = 0} ^ {\infty} \frac {(- 1) ^ {n}}{4 ^ {n}} (x - 1) ^ {n} \quad (- 3 <   x <   5), \\ \end{array}
$$

所以

$$
f (x) = \frac {1}{x ^ {2} + 4 x + 3} = \sum_ {n = 0} ^ {\infty} (- 1) ^ {n} \left(\frac {1}{2 ^ {n + 2}} - \frac {1}{2 ^ {2 n + 3}}\right) (x - 1) ^ {n} \quad (- 1 <   x <   3).
$$

例题精讲

12-7

最后,再举一个用直接法展开的例子.

例 6 将函数  $f(x)=(1+x)^{m}$  展开成 x 的幂级数, 其中 m 为任意实数.

解 $f(x)$ 的各阶导数为

$$
\begin{array}{l} f ^ {\prime} (x) = m (1 + x) ^ {m - 1}, \\ f ^ {\prime \prime} (x) = m (m - 1) (1 + x) ^ {m - 2}, \\ \dots \\ f ^ {(n)} (x) = m (m - 1) (m - 2) \dots (m - n + 1) (1 + x) ^ {m - n}, \\ \dots \\ \end{array}
$$

所以

$$
f (0) = 1, \quad f ^ {\prime} (0) = m, \quad f ^ {\prime \prime} (0) = m (m - 1), \quad \dots ,
$$

$$
f ^ {(n)} (0) = m (m - 1) \dots (m - n + 1), \quad \dots
$$

于是得级数

$$
1 + m x + \frac {m (m - 1)}{2 !} x ^ {2} + \dots + \frac {m (m - 1) \cdots (m - n + 1)}{n !} x ^ {n} + \dots .
$$

这级数相邻两项的系数之比的绝对值

$$
\left| \frac {a _ {n + 1}}{a _ {n}} \right| = \left| \frac {m - n}{n + 1} \right|\rightarrow 1 \quad (n \rightarrow \infty),
$$

因此,对于任何实数 m 这级数在开区间  $(-1,1)$  内收敛.

为了避免直接研究余项,设这级数在开区间 $(-1,1)$ 内收敛到函数 $F(x)$ :

$$
F (x) = 1 + m x + \frac {m (m - 1)}{2 !} x ^ {2} + \dots + \frac {m (m - 1) \cdots (m - n + 1)}{n !} x ^ {n} + \dots \quad (- 1 <   x <   1),
$$

下面证明  $F(x)=(1+x)^{m}$  (-1<x<1).

逐项求导,得

$$
F ^ {\prime} (x) = m \left[ 1 + \frac {m - 1}{1} x + \dots + \frac {(m - 1) \cdots (m - n + 1)}{(n - 1) !} x ^ {n - 1} + \dots \right],
$$

两端各乘 $(1+x)$ ，并把含有 $x^{n}\quad(n=1,2,\cdots)$ 的两项合并起来.根据恒等式

$$
\frac {(m - 1) \cdots (m - n + 1)}{(n - 1) !} + \frac {(m - 1) \cdots (m - n)}{n !} = \frac {m (m - 1) \cdots (m - n + 1)}{n !} \quad (n = 1, 2, \dots),
$$

可得

$$
\begin{array}{l} (1 + x) F ^ {\prime} (x) = m \left[ 1 + m x + \frac {m (m - 1)}{2 !} x ^ {2} + \dots + \frac {m (m - 1) \cdots (m - n + 1)}{n !} x ^ {n} + \dots \right] \\ = m F (x) \quad (- 1 <   x <   1). \\ \end{array}
$$

现在令 $\varphi (x) = \frac{F(x)}{(1 + x)^m}$，于是 $\varphi (0) = F(0) = 1$，且

$$
\begin{array}{l} \varphi^ {\prime} (x) = \frac {(1 + x) ^ {m} F ^ {\prime} (x) - m (1 + x) ^ {m - 1} F (x)}{(1 + x) ^ {2 m}} \\ = \frac {(1 + x) ^ {m - 1} [ (1 + x) F ^ {\prime} (x) - m F (x) ]}{(1 + x) ^ {2 m}} = 0, \\ \end{array}
$$

所以 $\varphi (x) = c$ （常数).但是 $\varphi (0) = 1$ ，从而 $\varphi (x) = 1$ ，即

$$
F (x) = (1 + x) ^ {m}.
$$

因此在区间 $(-1,1)$ 内有展开式

$$
(1 + x) ^ {m} = 1 + m x + \frac {m (m - 1)}{2 !} x ^ {2} + \dots + \frac {m (m - 1) \cdots (m - n + 1)}{n !} x ^ {n} + \dots (- 1 <   x <   1). \tag {4-12}
$$

在区间的端点,展开式是否成立要看 m 的数值而定.

公式(4-12)叫做二项展开式.特殊地,当m为正整数时,级数为x的m次多项式,这就是代数学中的二项式定理.

对应于 $m$ 为 $\frac{1}{2}$ 与 $-\frac{1}{2}$ 的二项展开式分别为

$$
\begin{array}{l} \sqrt {1 + x} = 1 + \frac {1}{2} x - \frac {1}{2 \times 4} x ^ {2} + \frac {1 \times 3}{2 \times 4 \times 6} x ^ {3} - \frac {1 \times 3 \times 5}{2 \times 4 \times 6 \times 8} x ^ {4} + \dots + \\ (- 1) ^ {n - 1} \frac {1 \times 3 \times 5 \times \cdots \times (2 n - 3)}{2 \times 4 \times 6 \times \cdots \times (2 n)} x ^ {n} + \dots \quad (- 1 \leqslant x \leqslant 1), \\ \frac {1}{\sqrt {1 + x}} = 1 - \frac {1}{2} x + \frac {1 \times 3}{2 \times 4} x ^ {2} - \frac {1 \times 3 \times 5}{2 \times 4 \times 6} x ^ {3} + \frac {1 \times 3 \times 5 \times 7}{2 \times 4 \times 6 \times 8} x ^ {4} - \dots + \\ (- 1) ^ {n} \frac {1 \times 3 \times 5 \times \cdots \times (2 n - 1)}{2 \times 4 \times 6 \times \cdots \times (2 n)} x ^ {n} + \dots \quad (- 1 <   x \leqslant 1). \\ \end{array}
$$

## 习题12-4

1. 求函数 $f(x) = \cos x$ 的泰勒级数，并验证它在整个数轴上收敛于这函数

2. 将下列函数展开成 $x$ 的幂级数，并求展开式成立的区间:

(1) sh  $x=\frac{e^{x}-e^{-x}}{2}$ ;

(2) $\ln (a + x)$ （ $a > 0$ ）；

(3) $a^x$ （$a > 0$ 且 $a \neq 1$）；

(4) $\sin^2 x$;

(5) $(1 + x)\ln (1 + x)$;

(6) $\frac{x}{\sqrt{1 + x^2}}.$

3. 将下列函数展开成 $(x-1)$ 的幂级数, 并求展开式成立的区间:

(1) $\sqrt{x^3}$;

(2) $\lg x$;

(3) $x\mathrm{e}^{x}$.

4. 将函数 $f(x) = \cos x$ 展开成 $\left(x + \frac{\pi}{3}\right)$ 的幂级数.

5. 将函数 $f(x) = \frac{1}{x}$ 展开成 $(x - 3)$ 的幂级数.
6. 将函数 $f(x) = \frac{1}{x^2 + 3x + 2}$ 展开成 $(x + 4)$ 的幂级数.

## 第五节 函数的幂级数展开式的应用

## 一、近似计算

有了函数的幂级数展开式,就可用它来进行近似计算,即在展开式有效的区间上,函数值可以近似地利用这个级数按精确度要求计算出来.

例 1 计算 $\sqrt[5]{240}$ 的近似值,要求误差不超过0.0001.

解 因为

$$
\sqrt [ 5 ]{2 4 0} = \sqrt [ 5 ]{2 4 3 - 3} = 3 \left(1 - \frac {1}{3 ^ {4}}\right) ^ {1 / 5},
$$

所以在二项展开式(4-12)中取 $m = \frac{1}{5}, x = -\frac{1}{3^4}$, 即得

$$
\sqrt [ 5 ]{2 4 0} = 3 \left(1 - \frac {1}{5} \times \frac {1}{3 ^ {4}} - \frac {1 \times 4}{5 ^ {2} \times 2 !} \times \frac {1}{3 ^ {8}} - \frac {1 \times 4 \times 9}{5 ^ {3} \times 3 !} \times \frac {1}{3 ^ {1 2}} - \dots - \frac {1 \times 4 \times 9 \times \cdots \times (5 n - 6)}{5 ^ {n} \times n !} \times \frac {1}{3 ^ {4 n}} - \dots\right).
$$

这个级数收敛很快.取前两项的和作为 $\sqrt[5]{240}$ 的近似值,其误差(也叫做截断误差)为

$$
\begin{array}{l} \mid r _ {2} \mid = 3 \left(\frac {1 \times 4}{5 ^ {2} \times 2 !} \times \frac {1}{3 ^ {8}} + \frac {1 \times 4 \times 9}{5 ^ {3} \times 3 !} \times \frac {1}{3 ^ {1 2}} + \frac {1 \times 4 \times 9 \times 1 4}{5 ^ {4} \times 4 !} \times \frac {1}{3 ^ {1 6}} + \dots\right) \\ <   3 \times \frac {1 \times 4}{5 ^ {2} \times 2 !} \times \frac {1}{3 ^ {8}} \left[ 1 + \frac {1}{8 1} + \left(\frac {1}{8 1}\right) ^ {2} + \dots \right] \\ = \frac {6}{2 5} \times \frac {1}{3 ^ {8}} \times \frac {1}{1 - \frac {1}{8 1}} = \frac {1}{2 5 \times 2 7 \times 4 0} <   \frac {1}{2 0 0 0 0}, \\ \end{array}
$$

于是取近似式为

$$
\sqrt [ 5 ]{2 4 0} \approx 3 \left(1 - \frac {1}{5} \times \frac {1}{3 ^ {4}}\right).
$$

为了使“四舍五入”引起的误差(叫做舍入误差)与截断误差之和不超过 $10^{-4}$ ，计算时应取五位小数，然后再四舍五入.因此最后得

$$
\sqrt [ 5 ]{2 4 0} \approx 2. 9 9 2 6.
$$

例 2 计算 ln 2 的近似值,要求误差不超过 0.0001.

解 在公式(4-10)中, 令 x=1 可得

$$
\ln 2 = 1 - \frac {1}{2} + \frac {1}{3} - \dots + (- 1) ^ {n - 1} \frac {1}{n} + \dots .
$$

取这级数前 $n$ 项的和作为 $\ln 2$ 的近似值, 其误差为

$$
\mid r _ {n} \mid \leqslant \frac {1}{n + 1}
$$

(见第二节第二目).为了保证误差不超过 $10^{-4}$ ,就需要取级数的前10 000项进行计算.这样做计算量太大了,我们必须用收敛较快的级数来代替它.

把公式(4-10)

$$
\ln (1 + x) = x - \frac {x ^ {2}}{2} + \frac {x ^ {3}}{3} - \frac {x ^ {4}}{4} + \dots + (- 1) ^ {n - 1} \frac {x ^ {n}}{n} + \dots \quad (- 1 <   x \leqslant 1)
$$

中将 $x$ 换成 $-x$, 得

$$
\ln (1 - x) = - x - \frac {x ^ {2}}{2} - \frac {x ^ {3}}{3} - \frac {x ^ {4}}{4} - \dots + (- 1) ^ {n - 1} \frac {(- x) ^ {n}}{n} + \dots \quad (- 1 \leqslant x <   1),
$$

两式相减,得到不含有偶次幂的展开式

$$
\ln \frac {1 + x}{1 - x} = \ln (1 + x) - \ln (1 - x) = 2 \left(x + \frac {1}{3} x ^ {3} + \frac {1}{5} x ^ {5} + \dots + \frac {1}{2 n + 1} x ^ {2 n + 1} + \dots\right) \quad (- 1 <   x <   1).
$$

令 $\frac{1+x}{1-x}=2$ , 解出  $x=\frac{1}{3}$ . 以  $x=\frac{1}{3}$  代入最后一个展开式, 得

$$
\ln 2 = 2 \left(\frac {1}{3} + \frac {1}{3} \times \frac {1}{3 ^ {3}} + \frac {1}{5} \times \frac {1}{3 ^ {5}} + \frac {1}{7} \times \frac {1}{3 ^ {7}} + \dots + \frac {1}{2 n + 1} \times \frac {1}{3 ^ {2 n + 1}} + \dots\right).
$$

取前四项作为  $\ln 2$  的近似值, 其误差为

$$
\begin{array}{l} \left| r _ {4} \right| = 2 \left(\frac {1}{9} \times \frac {1}{3 ^ {9}} + \frac {1}{1 1} \times \frac {1}{3 ^ {1 1}} + \frac {1}{1 3} \times \frac {1}{3 ^ {1 3}} + \dots + \frac {1}{2 n + 1} \times \frac {1}{3 ^ {2 n + 1}} + \dots\right) \\ <   \frac {2}{3 ^ {1 1}} \left[ 1 + \frac {1}{9} + \left(\frac {1}{9}\right) ^ {2} + \dots + \left(\frac {1}{9}\right) ^ {n} + \dots \right] \\ = \frac {2}{3 ^ {1 1}} \times \frac {1}{1 - \frac {1}{9}} = \frac {1}{4 \times 3 ^ {9}} <   \frac {1}{7 0 0 0 0}. \\ \end{array}
$$

于是取

$$
\ln 2 \approx 2 \left(\frac {1}{3} + \frac {1}{3} \times \frac {1}{3 ^ {3}} + \frac {1}{5} \times \frac {1}{3 ^ {5}} + \frac {1}{7} \times \frac {1}{3 ^ {7}}\right).
$$

同样地,考虑到舍入误差,计算时应取五位小数:

$$
\frac {1}{3} \approx 0. 3 3 3 3 3, \quad \frac {1}{3} \times \frac {1}{3 ^ {3}} \approx 0. 0 1 2 3 5, \quad \frac {1}{5} \times \frac {1}{3 ^ {5}} \approx 0. 0 0 0 8 2, \quad \frac {1}{7} \times \frac {1}{3 ^ {7}} \approx 0. 0 0 0 0 7.
$$

因此得

$$
\ln 2 \approx 0. 6 9 3 1.
$$

例 3 利用  $\sin x \approx x - \frac{x^{3}}{3!}$  求  $\sin 9^{\circ}$  的近似值, 并估计误差.

解 首先把角度化成弧度，

$$
9^{\circ} = \frac{\pi}{180}\times 9\text{弧度} = \frac{\pi}{20}\text{弧度},
$$

从而

$$
\sin \frac {\pi}{2 0} \approx \frac {\pi}{. 2 0} - \frac {1}{3 !} \left(\frac {\pi}{2 0}\right) ^ {3}.
$$

其次估计这个近似值的精确度.在  $\sin x$  的幂级数展开式(4-8)中令  $x=\frac{\pi}{20}$ ，得

$$
\sin \frac {\pi}{2 0} = \frac {\pi}{2 0} - \frac {1}{3 !} \left(\frac {\pi}{2 0}\right) ^ {3} + \frac {1}{5 !} \left(\frac {\pi}{2 0}\right) ^ {5} - \frac {1}{7 !} \left(\frac {\pi}{2 0}\right) ^ {7} + \dots + \frac {(- 1) ^ {n}}{(2 n + 1) !} \left(\frac {\pi}{2 0}\right) ^ {2 n + 1} + \dots ,
$$

等式右端是一个收敛的交错级数,且各项的绝对值单调减少.取它的前两项之和作为 $\sin\frac{\pi}{20}$ 的近似值,其误差为

$$
\mid r _ {2} \mid \leqslant \frac {1}{5 !} \left(\frac {\pi}{2 0}\right) ^ {5} <   \frac {1}{1 2 0} \times 0. 2 ^ {5} <   \frac {1}{3 0 0 0 0 0}.
$$

因此取

$$
\frac {\pi}{2 0} \approx 0. 1 5 7 0 8 0, \quad \frac {1}{3 !} \left(\frac {\pi}{2 0}\right) ^ {3} \approx 0. 0 0 0 6 4 6,
$$

于是得

$$
\sin 9 ^ {\circ} \approx 0. 1 5 6 4 3,
$$

这时误差不超过 $10^{-5}$

利用幂级数不仅可计算一些函数值的近似值,而且可计算一些定积分的近似值.具体地说,如果被积函数在积分区间上能展开成幂级数,那么把这个幂级数逐项积分,用积分后的级数就可算出定积分的近似值.

例4 计算定积分

$$
\frac {2}{\sqrt {\pi}} \int_ {0} ^ {\frac {1}{2}} \mathrm{e} ^ {- x ^ {2}} \mathrm{d} x
$$

的近似值,要求误差不超过0.0001  $\left(\text{取}\frac{1}{\sqrt{\pi}}\approx0.564\ 19\right)$ .

解 将 $\mathrm{e}^x$ 的幂级数展开式(4-7)中的 $x$ 换成 $-x^2$ ，就得到被积函数的幂级数展开式

$$
\begin{array}{l} \mathrm{e} ^ {- x ^ {2}} = 1 + \frac {(- x ^ {2})}{1 !} + \frac {(- x ^ {2}) ^ {2}}{2 !} + \frac {(- x ^ {2}) ^ {3}}{3 !} + \dots + \frac {(- x ^ {2}) ^ {n}}{n !} + \dots \\ = \sum_ {n = 0} ^ {\infty} (- 1) ^ {n} \frac {x ^ {2 n}}{n !} \quad (- \infty <   x <   + \infty). \\ \end{array}
$$

于是,根据幂级数在收敛区间内逐项可积,得

$$
\begin{array}{l} \frac {2}{\sqrt {\pi}} \int_ {0} ^ {\frac {1}{2}} \mathrm{e} ^ {- x ^ {2}} \mathrm{d} x = \frac {2}{\sqrt {\pi}} \int_ {0} ^ {\frac {1}{2}} \left[ \sum_ {n = 0} ^ {\infty} \frac {(- 1) ^ {n}}{n !} x ^ {2 n} \right] \mathrm{d} x = \frac {2}{\sqrt {\pi}} \sum_ {n = 0} ^ {\infty} \frac {(- 1) ^ {n}}{n !} \int_ {0} ^ {\frac {1}{2}} x ^ {2 n} \mathrm{d} x \\ = \frac {1}{\sqrt {\pi}} \left[ 1 - \frac {1}{2 ^ {2} \times 3} + \frac {1}{2 ^ {4} \times 5 \times 2 !} - \frac {1}{2 ^ {6} \times 7 \times 3 !} + \dots + (- 1) ^ {n} \frac {1}{2 ^ {2 n} (2 n + 1) n !} + \dots \right]. \\ \end{array}
$$

取前四项的和作为近似值,其误差为

$$
\mid r _ {4} \mid \leqslant \frac {1}{\sqrt {\pi}} \frac {1}{2 ^ {8} \times 9 \times 4 !} <   \frac {1}{9 0 0 0 0},
$$

所以

$$
\frac {2}{\sqrt {\pi}} \int_ {0} ^ {\frac {1}{2}} \mathrm{e} ^ {- x ^ {2}} \mathrm{d} x \approx \frac {1}{\sqrt {\pi}} \left(1 - \frac {1}{2 ^ {2} \times 3} + \frac {1}{2 ^ {4} \times 5 \times 2 !} - \frac {1}{2 ^ {6} \times 7 \times 3 !}\right),
$$

算得

$$
\frac {2}{\sqrt {\pi}} \int_ {0} ^ {\frac {1}{2}} \mathrm{e} ^ {- x ^ {2}} \mathrm{d} x \approx 0. 5 2 0 5.
$$

例5 计算积分

$$
\int_ {0} ^ {1} \frac {\sin x}{x} \mathrm{d} x
$$

的近似值,要求误差不超过 0.0001.

解 由于 $\lim_{x\to 0}\frac{\sin x}{x} = 1$ ，因此所给积分不是反常积分.若定义被积函数在 $x = 0$ 处的值为1，则它在积分区间[0,1]上连续.

展开被积函数,有

$$
\frac {\sin x}{x} = 1 - \frac {x ^ {2}}{3 !} + \frac {x ^ {4}}{5 !} - \frac {x ^ {6}}{7 !} + \dots + (- 1) ^ {n} \frac {x ^ {2 n}}{(2 n + 1) !} + \dots \quad (- \infty <   x <   + \infty).
$$

在区间 $[0,1]$ 上逐项积分,得

$$
\int_ {0} ^ {1} \frac {\sin x}{x} \mathrm{d} x = 1 - \frac {1}{3 \times 3 !} + \frac {1}{5 \times 5 !} - \frac {1}{7 \times 7 !} + \dots + (- 1) ^ {n} \frac {1}{(2 n + 1) (2 n + 1) !} + \dots .
$$

因为第四项的绝对值

$$
\frac {1}{7 \times 7 !} <   \frac {1}{3 0 0 0 0},
$$

所以取前三项的和作为积分的近似值: