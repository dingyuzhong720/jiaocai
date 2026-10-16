# 第12章 无穷级数

原始 PDF 第 248–321 页。

# 第十二章

# 无穷级数

无穷级数是高等数学的一个重要组成部分,它是表示函数、研究函数的性质以及进行数值计算的一种工具.本章先讨论常数项级数,介绍无穷级数的一些基本内容,然后讨论函数项级数,着重讨论如何将函数展开成幂级数和三角级数的问题.

## 第一节 常数项级数的概念和性质

## 一、常数项级数的概念

人们认识事物在数量方面的特性,往往有一个由近似到精确的过程.在这种认识过程中,会遇到由有限个数量相加到无穷多个数量相加的问题.

例如计算半径为 R 的圆面积 A, 具体做法如下: 作圆的内接正六边形, 算出这六边

形的面积 $a_1$，它是圆面积 $A$ 的一个粗糙的近似值。为了比较准确地计算出 $A$ 的值，我们以这个正六边形的每一边为底分别作一个顶点在圆周上的等腰三角形（图12-1），算出这六个等腰三角形的面积之和 $a_2$。那么 $a_1 + a_2$（即内接正十二边形的面积）就是 $A$ 的一个较好的近似值。同样地，在这正十二边形的每一边上分别作一个顶点在圆周上的等腰三角形，算出这十二个等腰三角形的面积之和 $a_3$。那么 $a_1 + a_2 + a_3$（即内接正二

![](../../raw/pages_0225-0256/images/page_247_image_8.jpg)

<details>
<summary>text_image</summary>

R
</details>

图12-1

十四边形的面积)是 $A$ 的一个更好的近似值.如此继续下去，内接正 $3\times 2^{n}$ 边形的面积就逐步逼近圆面积:

$$
A \approx a _ {1}, A \approx a _ {1} + a _ {2}, A \approx a _ {1} + a _ {2} + a _ {3}, \dots , A \approx a _ {1} + a _ {2} + \dots + a _ {n}.
$$

如果内接正多边形的边数无限增多, 即 n 无限增大, 那么和  $a_{1} + a_{2} + \cdots + a_{n}$  的极限就是所要求的圆面积 A. 这时和式中的项数无限增多, 于是出现了无穷多个数量依次相加

241

---

第十二章 无穷级数

的数学式子.

一般地,如果给定一个数列

$$
u _ {1}, u _ {2}, u _ {3}, \dots , u _ {n}, \dots ,
$$

那么由这数列构成的表达式

$$
u _ {1} + u _ {2} + u _ {3} + \dots + u _ {n} + \dots \tag {1-1}
$$

叫做(常数项)无穷级数,简称(常数项)级数,记为 $\sum_{i=1}^{\infty}u_{i}$ ,即

$$
\sum_ {i = 1} ^ {\infty} u _ {i} = u _ {1} + u _ {2} + u _ {3} + \dots + u _ {i} + \dots ,
$$

其中第 n 项  $u_{n}$  叫做级数的一般项.

上述级数的定义只是一个形式上的定义,怎样理解无穷级数中无穷多个数量相加呢?联系上面关于计算圆面积的例子,我们可以从有限项的和出发,观察它们的变化趋势,由此来理解无穷多个数量相加的含义.

作(常数项)级数(1-1)的前 $n$ 项的和

$$
s _ {n} = u _ {1} + u _ {2} + \dots + u _ {n} = \sum_ {i = 1} ^ {n} u _ {i}, \tag {1-2}
$$

$s_{n}$  称为级数(1-1)的部分和. 当 n 依次取 1,2,3,…时, 它们构成一个新的数列

$$
s _ {1} = u _ {1}, s _ {2} = u _ {1} + u _ {2}, s _ {3} = u _ {1} + u _ {2} + u _ {3}, \dots , s _ {n} = u _ {1} + u _ {2} + \dots + u _ {n}, \dots .
$$

根据这个数列有没有极限,我们引进无穷级数(1-1)的收敛与发散的概念.

定义 如果级数 $\sum_{i=1}^{\infty} u_i$ 的部分和数列 $\{s_n\}$ 有极限 $s$, 即

$$
\lim _ {n \to \infty} s _ {n} = s,
$$

那么称无穷级数 $\sum_{i=1}^{\infty} u_i$ 收敛, 这时极限 $s$ 叫做这级数的和, 并写成

$$
s = u _ {1} + u _ {2} + \dots + u _ {i} + \dots ;
$$

如果 $\{s_n\}$ 没有极限,那么称无穷级数 $\sum_{i=1}^{\infty} u_i$ 发散.

显然,当级数收敛时,其部分和 $s_{n}$ 是级数的和s的近似值,它们之间的差值

$$
r _ {n} = s - s _ {n} = u _ {n + 1} + u _ {n + 2} + \dots
$$

叫做级数的余项. 用近似值 $s_n$ 代替和 $s$ 所产生的误差是这个余项的绝对值, 即误差是 $|r_n|$.

从上述定义可知,级数与数列极限有着紧密的联系.给定级数  $\sum_{i=1}^{\infty}u_{i}$ , 就有部分和数列  $\{s_{n}\}$ ; 反之, 给定数列  $\{s_{n}\}$ , 就有以  $\{s_{n}\}$  为部分和数列的级数

$$
s _ {1} + (s _ {2} - s _ {1}) + \dots + (s _ {i} - s _ {i - 1}) + \dots = s _ {1} + \sum_ {i = 2} ^ {\infty} (s _ {i} - s _ {i - 1}) = \sum_ {i = 1} ^ {\infty} u _ {i},
$$

242

---

第一节 常数项级数的概念和性质

其中 $u_{1} = s_{1}, u_{n} = s_{n} - s_{n-1} (n \geqslant 2)$. 按定义, 级数 $\sum_{i=1}^{\infty} u_{i}$ 与数列 $\{s_n\}$ 同时收敛或同时发散, 且在收敛时, 有

$$
\sum_ {i = 1} ^ {\infty} u _ {i} = \lim _ {n \to \infty} s _ {n},
$$

即

$$
\sum_ {i = 1} ^ {\infty} u _ {i} = \lim _ {n \to \infty} \sum_ {i = 1} ^ {n} u _ {i}.
$$

例1 无穷级数

$$
\sum_ {i = 0} ^ {\infty} a q ^ {i} = a + a q + a q ^ {2} + \dots + a q ^ {i} + \dots \tag {1-3}
$$

叫做等比级数(又称为几何级数),其中  $a \neq 0, q$  叫做级数的公比.试讨论级数(1-3)的收敛性.

解 如果 $q \neq 1$ ，那么部分和

$$
s _ {n} = a + a q + \dots + a q ^ {n - 1} = \frac {a - a q ^ {n}}{1 - q} = \frac {a}{1 - q} - \frac {a q ^ {n}}{1 - q}.
$$

当 $|q| < 1$ 时，由于 $\lim_{n\to \infty}q^n = 0$ ，从而 $\lim_{n\to \infty}s_n = \frac{a}{1 - q}$ ，因此这时级数(1-3)收敛，其和为$\frac{a}{1 - q}$ .当 $|q| > 1$ 时，由于 $\lim_{n\to \infty}q^n = \infty$ ，从而 $\lim_{n\to \infty}s_n = \infty$ ，这时级数(1-3)发散.

如果 $|q| = 1$ ，那么当 $q = 1$ 时，$s_n = na \to \infty$ ，因此级数(1-3)发散；当 $q = -1$ 时，级数(1-3)成为

$$
a - a + a - a + \dots ,
$$

显然 $s_n$ 随着 $n$ 为奇数或为偶数而等于 $a$ 或等于0, 从而 $s_n$ 的极限不存在, 这时级数(1-3)也发散.

综合上述结果,我们得到:如果等比级数(1-3)的公比的绝对值 $|q|<1$ ,那么级数收敛;如果 $|q|\geqslant1$ ,那么级数发散.

例 2 证明级数  $1+2+3+\cdots+n+\cdots$  是发散的.

证 这级数的部分和为

$$
s _ {n} = 1 + 2 + 3 + \dots + n = \frac {n (n + 1)}{2}.
$$

显然， $\lim_{n\to \infty}s_n = \infty$ ，因此所给级数是发散的

例3 判定无穷级数 $\frac{1}{1\times 2} +\frac{1}{2\times 3} +\dots +\frac{1}{n(n + 1)} +\dots$

的收敛性.

243

---

第十二章 无穷级数

例题精讲

12-1

解 由于

$$
u _ {n} = \frac {1}{n (n + 1)} = \frac {1}{n} - \frac {1}{n + 1},
$$

因此

$$
s _ {n} = \frac {1}{1 \times 2} + \frac {1}{2 \times 3} + \dots + \frac {1}{n (n + 1)} = \left(1 - \frac {1}{2}\right) + \left(\frac {1}{2} - \frac {1}{3}\right) + \dots + \left(\frac {1}{n} - \frac {1}{n + 1}\right) = 1 - \frac {1}{n + 1}.
$$

从而

$$
\lim _ {n \to \infty} s _ {n} = \lim _ {n \to \infty} \left(1 - \frac {1}{n + 1}\right) = 1,
$$

所以这级数收敛,它的和是1.

## 二、收敛级数的基本性质

根据无穷级数收敛、发散以及和的概念,可以得出收敛级数的几个基本性质.

性质1 如果级数 $\sum_{n=1}^{\infty} u_n$ 收敛于和 $s$, 那么级数 $\sum_{n=1}^{\infty} k u_n$ 也收敛, 且其和为 $ks$.

证 设级数 $\sum_{n=1}^{\infty} u_n$ 与级数 $\sum_{n=1}^{\infty} k u_n$ 的部分和分别为 $s_n$ 与 $\sigma_n$, 则

$$
\sigma_ {n} = k u _ {1} + k u _ {2} + \dots + k u _ {n} = k s _ {n},
$$

于是

$$
\lim _ {n \to \infty} \sigma_ {n} = \lim _ {n \to \infty} k s _ {n} = k \lim _ {n \to \infty} s _ {n} = k s.
$$

这就表明级数  $\sum_{n=1}^{\infty}ku_{n}$  收敛,且和为 ks.

由关系式 $\sigma_{n} = k s_{n}$ 知道, 如果 $\{s_n\}$ 没有极限且 $k \neq 0$, 那么 $\{\sigma_{n}\}$ 也不可能有极限. 因此我们得到如下结论: 级数的每一项同乘一个不为零的常数后, 它的收敛性不会改变.

性质2 如果级数 $\sum_{n=1}^{\infty} u_n$ 与 $\sum_{n=1}^{\infty} v_n$ 分别收敛于和 $s$ 与 $\sigma$, 那么级数 $\sum_{n=1}^{\infty} (u_n \pm v_n)$ 也收敛, 且其和为 $s \pm \sigma$.

证 设级数 $\sum_{n=1}^{\infty} u_n$ 与 $\sum_{n=1}^{\infty} v_n$ 的部分和分别为 $s_n$ 与 $\sigma_n$, 则级数 $\sum_{n=1}^{\infty} (u_n \pm v_n)$ 的部分和

$$
\tau_ {n} = (u _ {1} \pm v _ {1}) + (u _ {2} \pm v _ {2}) + \dots + (u _ {n} \pm v _ {n}) = (u _ {1} + u _ {2} + \dots + u _ {n}) \pm (v _ {1} + v _ {2} + \dots + v _ {n}) = s _ {n} \pm \sigma_ {n},
$$

于是

$$
\lim _ {n \to \infty} \tau_ {n} = \lim _ {n \to \infty} (s _ {n} \pm \sigma_ {n}) = s \pm \sigma .
$$

244

---

第一节 常数项级数的概念和性质

这就表明级数 $\sum_{n=1}^{\infty}\left(u_n\pm v_n\right)$ 收敛, 且其和为 $s\pm \sigma$.

性质 2 也说成: 两个收敛级数可以逐项相加与逐项相减.

性质 3 在级数中去掉、加上或改变有限项,不会改变级数的收敛性.

证 我们只需证明“在级数的前面部分去掉或加上有限项,不会改变级数的收敛性”,因为其他情形(即在级数中任意去掉、加上或改变有限项的情形)都可以看成在级数的前面部分先去掉有限项,然后再加上有限项的结果.

设将级数

$$
u _ {1} + u _ {2} + \dots + u _ {k} + u _ {k + 1} + \dots + u _ {k + n} + \dots
$$

的前 $k$ 项去掉, 则得级数

$$
u _ {k + 1} + u _ {k + 2} + \dots + u _ {k + n} + \dots ,
$$

于是新得的级数的部分和为

$$
\sigma_ {n} = u _ {k + 1} + u _ {k + 2} + \dots + u _ {k + n} = s _ {k + n} - s _ {k},
$$

其中 $s_{k + n}$ 是原来级数的前 $k + n$ 项的和.因为 $s_k$ 是常数，所以当 $n\to \infty$ 时， $\sigma_{n}$ 与 $s_{k + n}$ 或者同时具有极限，或者同时没有极限.

类似地,可以证明在级数的前面加上有限项,不会改变级数的收敛性.

性质4 如果级数 $\sum_{n=1}^{\infty} u_n$ 收敛, 那么对这级数的项任意加括号后所成的级数

$$
(u _ {1} + u _ {2} + \dots + u _ {n _ {1}}) + (u _ {n _ {1} + 1} + u _ {n _ {1} + 2} + \dots + u _ {n _ {2}}) + \dots + (u _ {n _ {k - 1} + 1} + u _ {n _ {k - 1} + 2} + \dots + u _ {n _ {k}}) + \dots \tag {1-4}
$$

仍收敛,且其和不变.

证 设级数 $\sum_{n=1}^{\infty} u_n$ 的部分和数列为 $\{s_n\}$, 加括号后所成的级数 (1-4) 的部分和数列为 $\{A_k\}$, 则

$$
A _ {1} = u _ {1} + u _ {2} + \dots + u _ {n _ {1}} = s _ {n _ {1}},
$$

$$
A _ {2} = (u _ {1} + u _ {2} + \dots + u _ {n _ {1}}) + (u _ {n _ {1} + 1} + u _ {n _ {1} + 2} + \dots + u _ {n _ {2}}) = s _ {n _ {2}},
$$

...

$$
A _ {k} = (u _ {1} + u _ {2} \dots + u _ {n _ {1}}) + (u _ {n _ {1} + 1} + u _ {n _ {1} + 2} + \dots + u _ {n _ {2}}) + \dots + (u _ {n _ {k - 1} + 1} + u _ {n _ {k - 1} + 2} + \dots + u _ {n _ {k}}) = s _ {n _ {k}},
$$

...

可见, 数列  $\{A_{k}\}$  是数列  $\{s_{n}\}$  的一个子数列. 由数列  $\{s_{n}\}$  的收敛性以及收敛数列与其子数列的关系可知, 数列  $\{A_{k}\}$  必定收敛, 且有

$$
\lim _ {k \to \infty} A _ {k} = \lim _ {n \to \infty} s _ {n},
$$

即加括号后所成的级数收敛,且其和不变.

注意 如果加括号后所成的级数收敛,那么不能断定去括号后原来的级数也收敛.例如,级数

释疑解难 12-1

245

---

第十二章 无穷级数

$$
(1 - 1) + (1 - 1) + \dots
$$

收敛于零,但级数

$$
1 - 1 + 1 - 1 + \dots
$$

却是发散的.

根据性质 4 可得如下推论: 如果加括号后所成的级数发散, 那么原来级数也发散. 事实上, 倘若原来级数收敛, 则根据性质 4 知道, 加括号后的级数就应该收敛了.

性质5(级数收敛的必要条件) 如果级数 $\sum_{n=1}^{\infty} u_n$ 收敛, 那么它的一般项 $u_n$ 趋于零, 即

$$
\lim _ {n \to \infty} u _ {n} = 0.
$$

证 设级数 $\sum_{n=1}^{\infty} u_n$ 的部分和为 $s_n$, 且 $s_n \to s (n \to \infty)$, 则

$$
\lim _ {n \to \infty} u _ {n} = \lim _ {n \to \infty} (s _ {n} - s _ {n - 1}) = \lim _ {n \to \infty} s _ {n} - \lim _ {n \to \infty} s _ {n - 1} = s - s = 0.
$$

由性质 5 可知, 如果级数的一般项不趋于零, 那么该级数必定发散. 例如, 级数

$$
\frac {1}{2} - \frac {2}{3} + \frac {3}{4} - \dots + (- 1) ^ {n - 1} \frac {n}{n + 1} + \dots ,
$$

它的一般项 $u_{n} = (-1)^{n - 1}\frac{n}{n + 1}$ 当 $n\to \infty$ 时不趋于零，因此该级数是发散的.

注意 级数的一般项趋于零并不是级数收敛的充分条件.有些级数虽然一般项趋于零,但仍然是发散的.例如,调和级数

$$
1 + \frac {1}{2} + \frac {1}{3} + \dots + \frac {1}{n} + \dots , \tag {1-5}
$$

虽然它的一般项 $u_{n} = \frac{1}{n}\rightarrow 0(n\to \infty)$ ，但是它是发散的.现在我们用反证法证明如下:

假若级数(1-5)收敛,设它的部分和为 $s_{n}$ ,且 $s_{n}\rightarrow s(n\rightarrow\infty)$ .显然,对级数(1-5)的部分和 $s_{2n}$ ,也有 $s_{2n}\rightarrow s(n\rightarrow\infty)$ .于是

$$
s _ {2 n} - s _ {n} \longrightarrow s - s = 0 \quad (n \longrightarrow \infty).
$$

但另一方面

$$
s _ {2 n} - s _ {n} = \frac {1}{n + 1} + \frac {1}{n + 2} + \dots + \frac {1}{2 n} > \underbrace {\frac {1}{2 n} + \frac {1}{2 n} + \cdots + \frac {1}{2 n}} _ {n \text {项}} = \frac {1}{2},
$$

故

$$
s _ {2 n} - s _ {n} \not \to 0 \quad (n \to \infty) ,
$$

与假设级数(1-5)收敛矛盾.这矛盾说明级数(1-5)必定发散.

246

---

第一节 常数项级数的概念和性质

## \*三、柯西审敛原理

怎样判定一个级数的收敛性呢？我们有下述的柯西审敛原理.

定理(柯西审敛原理) 级数  $\sum_{n=1}^{\infty}u_{n}$  收敛的充分必要条件为: 对于任意给定的正数  $\varepsilon$ , 总存在正整数 N, 使得当 n > N 时, 对于任意的正整数 p, 都有

$$
\mid u _ {n + 1} + u _ {n + 2} + \dots + u _ {n + p} \mid <   \varepsilon
$$

成立.

证 设级数 $\sum_{n=1}^{\infty} u_n$ 的部分和为 $s_n$, 因为

$$
\mid u _ {n + 1} + u _ {n + 2} + \dots + u _ {n + p} \mid = \mid s _ {n + p} - s _ {n} \mid ,
$$

所以由数列的柯西极限存在准则(第一章第六节),即得本定理结论.

例 4 利用柯西审敛原理判定级数  $\sum_{n=1}^{\infty}\frac{1}{n^{2}}$  的收敛性.

解 因为对任何正整数 p,

$$
\begin{array}{l} \mid u _ {n + 1} + u _ {n + 2} + \dots + u _ {n + p} \mid = \frac {1}{(n + 1) ^ {2}} + \frac {1}{(n + 2) ^ {2}} + \dots + \frac {1}{(n + p) ^ {2}} \\ <   \frac {1}{n (n + 1)} + \frac {1}{(n + 1) (n + 2)} + \dots + \frac {1}{(n + p - 1) (n + p)} \\ = \left(\frac {1}{n} - \frac {1}{n + 1}\right) + \left(\frac {1}{n + 1} - \frac {1}{n + 2}\right) + \dots + \left(\frac {1}{n + p - 1} - \frac {1}{n + p}\right) \\ = \frac {1}{n} - \frac {1}{n + p} <   \frac {1}{n}, \\ \end{array}
$$

所以对于任意给定的正数 $\varepsilon$ ，取正整数 $N\geqslant \frac{1}{\varepsilon}$ ，则当 $n > N$ 时，对任何正整数 $p$ ，都有

$$
\mid u _ {n + 1} + u _ {n + 2} + \dots + u _ {n + p} \mid <   \varepsilon
$$

成立.按柯西审敛原理,级数  $\sum_{n=1}^{\infty}\frac{1}{n^{2}}$  收敛.

## 习题12-1

1. 写出下列级数的前五项:

(1) $\sum_{n=1}^{\infty} \frac{1 + n}{1 + n^2}$;

(2) $\sum_{n=1}^{\infty}\frac{1\times3\times\cdots\times(2n-1)}{2\times4\times\cdots\times(2n)};$

(3) $\sum_{n=1}^{\infty} \frac{(-1)^{n-1}}{5^n}$;

(4) $\sum_{n=1}^{\infty} \frac{n!}{n^n}$.

247

---

第十二章 无穷级数

2. 根据级数收敛与发散的定义判定下列级数的收敛性:

(1) $\sum_{n=1}^{\infty} (\sqrt{n+1}-\sqrt{n})$;

(2) $\frac{1}{1\times3}+\frac{1}{3\times5}+\frac{1}{5\times7}+\cdots+\frac{1}{(2n-1)(2n+1)}+\cdots;$

(3)  $\sin\frac{\pi}{6}+\sin\frac{2\pi}{6}+\cdots+\sin\frac{n\pi}{6}+\cdots;$

(4) $\sum_{n=1}^{\infty} \ln \left(1 + \frac{1}{n}\right)$.

3. 设级数 $\sum_{n=1}^{\infty} u_n$ 满足条件: (1) $\lim_{n \to \infty} u_n = 0$; (2) $\sum_{k=1}^{\infty} (u_{2k-1} + u_{2k})$ 收敛. 证明: 级数 $\sum_{n=1}^{\infty} u_n$ 收敛.

4. 判定下列级数的收敛性:

(1) $-\frac{8}{9}+\frac{8^{2}}{9^{2}}-\frac{8^{3}}{9^{3}}+\cdots+(-1)^{n}\frac{8^{n}}{9^{n}}+\cdots;$

(2) $\frac{1}{3}+\frac{1}{6}+\frac{1}{9}+\cdots+\frac{1}{3n}+\cdots;$

(3) $\frac{1}{3}+\frac{1}{\sqrt{3}}+\frac{1}{\sqrt[3]{3}}+\cdots+\frac{1}{\sqrt[n]{3}}+\cdots;$

(4) $\frac{3}{2}+\frac{3^{2}}{2^{2}}+\frac{3^{3}}{2^{3}}+\cdots+\frac{3^{n}}{2^{n}}+\cdots;$

(5) $\left(\frac{1}{2}+\frac{1}{3}\right)+\left(\frac{1}{2^{2}}+\frac{1}{3^{2}}\right)+\left(\frac{1}{2^{3}}+\frac{1}{3^{3}}\right)+\cdots+\left(\frac{1}{2^{n}}+\frac{1}{3^{n}}\right)+\cdots.$

\*5. 利用柯西审敛原理判定下列级数的收敛性:

(1)  $\sum_{n=1}^{\infty}\frac{(-1)^{n+1}}{n};$

(2) $1+\frac{1}{2}-\frac{1}{3}+\frac{1}{4}+\frac{1}{5}-\frac{1}{6}+\cdots+\frac{1}{3n-2}+\frac{1}{3n-1}-\frac{1}{3n}+\cdots;$

(3) $\sum_{n=1}^{\infty} \frac{\sin nx}{2^n}$;

(4) $\sum_{n=0}^{\infty}\left(\frac{1}{3n+1}+\frac{1}{3n+2}-\frac{1}{3n+3}\right)$.

## 第二节 常数项级数的审敛法

## 一、正项级数及其审敛法

一般的常数项级数,它的各项可以是正数、负数或零.现在我们先讨论各项都是正数或零的级数,这种级数称为正项级数.这种级数特别重要,以后将看到许多级数的收敛性问题可归结为正项级数的收敛性问题.

设级数

$$
u _ {1} + u _ {2} + \dots + u _ {n} + \dots \tag {2-1}
$$

是一个正项级数 $(u_{n}\geqslant 0)$ ，它的部分和为 $s_n$ .显然，数列 $\{s_n\}$ 是一个单调增加数列

$$
s _ {1} \leqslant s _ {2} \leqslant \dots \leqslant s _ {n} \leqslant \dots .
$$

如果数列 $\{s_n\}$ 有界，即 $s_n$ 总不大于某一常数 $M$ ，根据单调有界的数列必有极限的准则，级数(2-1)必收敛于和 $s$ ，且 $s_n \leqslant s \leqslant M.$ 反之，如果正项级数(2-1)收敛于和 $s$ ，即 $\lim_{n \to \infty} s_n = s$ ，根据有极限的数列是有界数列的性质可知，数列 $\{s_n\}$ 有界.因此，我们得到如下重要的结论:

248

---

第二节 常数项级数的审敛法

定理1 正项级数 $\sum_{n=1}^{\infty} u_n$ 收敛的充分必要条件是: 它的部分和数列 $\{s_n\}$ 有界.

由定理1可知,如果正项级数  $\sum_{n=1}^{\infty}u_{n}$  发散,那么它的部分和数列  $s_{n}\rightarrow+\infty(n\rightarrow\infty)$ ,
即  $\sum_{n=1}^{\infty}u_{n}=+\infty$ .

根据定理1,可得关于正项级数的一个基本的审敛法.

定理 2(比较审敛法) 设  $\sum_{n=1}^{\infty}u_{n}$  和  $\sum_{n=1}^{\infty}v_{n}$  都是正项级数, 且  $u_{n} \leqslant v_{n} (n=1,2,\cdots)$ . 若级数  $\sum_{n=1}^{\infty}v_{n}$  收敛, 则级数  $\sum_{n=1}^{\infty}u_{n}$  收敛; 反之, 若级数  $\sum_{n=1}^{\infty}u_{n}$  发散, 则级数  $\sum_{n=1}^{\infty}v_{n}$  发散.

证 设级数 $\sum_{n=1}^{\infty} v_n$ 收敛于和 $\sigma$, 则级数 $\sum_{n=1}^{\infty} u_n$ 的部分和

$$
s _ {n} = u _ {1} + u _ {2} + \dots + u _ {n} \leqslant v _ {1} + v _ {2} + \dots + v _ {n} \leqslant \sigma \quad (n = 1, 2, \dots),
$$

即部分和数列 $\{s_{n}\}$ 有界,由定理1知级数 $\sum_{n=1}^{\infty}u_{n}$ 收敛.

反之, 设级数 $\sum_{n=1}^{\infty} u_n$ 发散, 则级数 $\sum_{n=1}^{\infty} v_n$ 必发散. 因为若级数 $\sum_{n=1}^{\infty} v_n$ 收敛, 由上面已证明的结论, 将有级数 $\sum_{n=1}^{\infty} u_n$ 也收敛, 与假设矛盾.

注意到级数的每一项同乘不为零的常数 $k$ 以及去掉级数前面部分的有限项不会影响级数的收敛性, 我们可得如下推论:

推论 设 $\sum_{n=1}^{\infty} u_n$ 和 $\sum_{n=1}^{\infty} v_n$ 都是正项级数, 如果级数 $\sum_{n=1}^{\infty} v_n$ 收敛, 且存在正整数 $N$, 使当 $n \geqslant N$ 时有 $u_n \leqslant k v_n (k > 0)$ 成立, 那么级数 $\sum_{n=1}^{\infty} u_n$ 收敛; 如果级数 $\sum_{n=1}^{\infty} v_n$ 发散, 且当 $n \geqslant N$ 时有 $u_n \geqslant k v_n (k > 0)$ 成立, 那么级数 $\sum_{n=1}^{\infty} u_n$ 发散.

例1 讨论 $p$ 级数

$$
1 + \frac {1}{2 ^ {p}} + \frac {1}{3 ^ {p}} + \frac {1}{4 ^ {p}} + \dots + \frac {1}{n ^ {p}} + \dots \tag {2-2}
$$

的收敛性,其中常数p>0.

解 设 $p \leqslant 1$. 这时级数的各项不小于调和级数的对应项, 即 $\frac{1}{n^p} \geqslant \frac{1}{n}$, 但调和级数发散, 因此根据比较审敛法可知, 当 $p \leqslant 1$ 时级数 (2-2) 发散.

设 $p > 1$ .因为当 $k - 1\leqslant x\leqslant k$ 时，有 $\frac{1}{k^p}\leqslant \frac{1}{x^p}$ ，所以

249

---

第十二章 无穷级数

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

极限形式的比较审敛法,在两个正项级数的一般项均趋于零的情况下,其实是比

250

---

第二节 常数项级数的审敛法

较它们的一般项作为无穷小量的阶.定理表明,当  $n \to \infty$  时,如果  $u_{n}$  是与  $v_{n}$  同阶或是比  $v_{n}$  高阶的无穷小,而级数  $\sum_{n=1}^{\infty} v_{n}$  收敛,那么级数  $\sum_{n=1}^{\infty} u_{n}$  收敛;如果  $u_{n}$  是与  $v_{n}$  同阶或是比  $v_{n}$  低阶的无穷小,而级数  $\sum_{n=1}^{\infty} v_{n}$  发散,那么级数  $\sum_{n=1}^{\infty} u_{n}$  发散.

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

![](../../raw/pages_0257-0288/images/page_257_image_17.jpg)

例题精讲

12-2

251

---

第十二章 无穷级数

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

252

---

第二节 常数项级数的审敛法

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

253

---

第十二章 无穷级数

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

254

---

第二节 常数项级数的审敛法

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

![](../../raw/pages_0257-0288/images/page_261_image_26.jpg)

例题精讲

12-4

255

---

第十二章 无穷级数

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

256

---

第二节 常数项级数的审敛法

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

257

---

第十二章 无穷级数

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

258

---

第二节 常数项级数的审敛法

在给出绝对收敛级数的另一个性质以前,我们先来讨论级数的乘法运算.

设级数  $\sum_{n=1}^{\infty}u_{n}$  和  $\sum_{n=1}^{\infty}v_{n}$  都收敛,仿照有限项之和相乘的规则,作出这两个级数的项所有可能的乘积  $u_{i}v_{k}\quad(i,k=1,2,3,\cdots)$ ,这些乘积是

$$
\begin{array}{l} u _ {1} v _ {1}, u _ {1} v _ {2}, u _ {1} v _ {3}, \dots , u _ {1} v _ {i}, \dots , \\ u _ {2} v _ {1}, u _ {2} v _ {2}, u _ {2} v _ {3}, \dots , u _ {2} v _ {i}, \dots , \\ u _ {3} v _ {1}, u _ {3} v _ {2}, u _ {3} v _ {3}, \dots , u _ {3} v _ {i}, \dots , \\ u _ {k} v _ {1}, u _ {k} v _ {2}, u _ {k} v _ {3}, \dots , u _ {k} v _ {i}, \dots , \\ \end{array}
$$

...

...

这些乘积可以用很多方式将它们排列成一个数列.例如可以按“对角线法”或按“正方形法”将它们排列成下面形状的数列(图12-2):

![](../../raw/pages_0257-0288/images/page_265_image_7.jpg)

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

259

---

第十二章 无穷级数

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

260

---

第二节 常数项级数的审敛法

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

261

---

第十二章 无穷级数

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

262

---

第三节 幂级数

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

263

---

第十二章 无穷级数

因为当 $|x| < |x_0|$ 时，等比级数 $\sum_{n=0}^{\infty} M \left| \frac{x}{x_0} \right|^n$ 收敛（公比 $\left| \frac{x}{x_0} \right| < 1$），所以级数 $\sum_{n=0}^{\infty} |a_n x^n|$ 收敛，也就是级数 $\sum_{n=0}^{\infty} a_n x^n$ 绝对收敛.

定理的第二部分可用反证法证明. 假设幂级数当 $x = x_0$ 时发散而有一点 $x_1$ 适合 $|x_1| > |x_0|$ 使级数收敛, 则根据本定理的第一部分, 级数当 $x = x_0$ 时应收敛, 这与假设矛盾. 定理得证.

定理1表明,如果幂级数在 $x = x_0$ 处收敛,那么对于开区间 $(-\left|x_0\right|, \left|x_0\right|)$ 内的任何 $x$,幂级数都收敛;如果幂级数在 $x = x_0$ 处发散,那么对于闭区间 $\left[-\left|x_0\right|, \left|x_0\right|\right]$ 外的任何 $x$,幂级数都发散.

设已给幂级数在数轴上既有收敛点(不仅是原点)也有发散点.现在从原点沿数轴向右方走,最初只遇到收敛点,然后就只遇到发散点.这两部分的界点可能是收敛点也可能是发散点.从原点沿数轴向左方走情形也是如此.两个界点P与 $P'$ 在原点的两侧,

且由定理1可以证明它们到原点的距离是一样的(图12-3).

![](../../raw/pages_0257-0288/images/page_270_image_6.jpg)

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

264

---

第三节 幂级数

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

265

---

第十二章 无穷级数

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

266

---

第三节 幂级数

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

![](../../raw/pages_0257-0288/images/page_273_image_23.jpg)

释疑解难

12-3

267

---

第十二章 无穷级数

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

268

---

第三节 幂级数

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

269

![](../../raw/pages_0257-0288/images/page_275_image_21.jpg)

例题精讲

12-6

---

第十二章 无穷级数

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

270

---

第四节 函数展开成幂级数

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

271

---

第十二章 无穷级数

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

图

释疑解难

12-4

272

---

第四节 函数展开成幂级数

即当 $n\to \infty$ 时，有 $\mid R_n(x)\mid \rightarrow 0.$ 于是得展开式

$$
\mathrm{e} ^ {x} = 1 + x + \frac {x ^ {2}}{2 !} + \dots + \frac {x ^ {n}}{n !} + \dots
$$

$$
(- \infty <   x <   + \infty). \tag {4-7}
$$

如果在 x=0 处附近, 用级数的部分和 (即多项式) 来近似代替  $e^{x}$ , 那么随着项数的增加, 它们就越来越接近于  $e^{x}$ , 如图 12-4 所示.

例 2 将函数  $f(x)=\sin x$  展开成 x 的幂级数.

![](../../raw/pages_0257-0288/images/page_279_chart_6.jpg)

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

273

---

第十二章 无穷级数

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

274

---

第四节 函数展开成幂级数

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

275

---

第十二章 无穷级数

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

276

---

第四节 函数展开成幂级数

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

277

---

第十二章 无穷级数

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

278

---

第五节 函数的幂级数展开式的应用

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

279

---

第十二章 无穷级数

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

280

---

第五节 函数的幂级数展开式的应用

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

281

---

第十二章 无穷级数

$$
\int_ {0} ^ {1} \frac {\sin x}{x} \mathrm{d} x \approx 1 - \frac {1}{3 \times 3 !} + \frac {1}{5 \times 5 !},
$$

算得

$$
\int_ {0} ^ {1} \frac {\sin x}{x} \mathrm{d} x \approx 0. 9 4 6 1.
$$

## 二、微分方程的幂级数解法

这里,我们简单介绍一阶微分方程和二阶齐次线性微分方程的幂级数解法.

为求一阶微分方程

$$
\frac {\mathrm{d} y}{\mathrm{d} x} = f (x, y) \tag {5-1}
$$

满足初值条件 $y\mid_{x = x_0} = y_0$ 的特解，如果其中函数 $f(x,y)$ 是 $(x - x_0),(y - y_0)$ 的多项式

$$
f (x, y) = a _ {0 0} + a _ {1 0} (x - x _ {0}) + a _ {0 1} (y - y _ {0}) + \dots + a _ {l m} (x - x _ {0}) ^ {l} (y - y _ {0}) ^ {m}.
$$

那么可以设所求特解可展开为 $x - x_0$ 的幂级数:

$$
y = y _ {0} + a _ {1} (x - x _ {0}) + a _ {2} (x - x _ {0}) ^ {2} + \dots + a _ {n} (x - x _ {0}) ^ {n} + \dots , \tag {5-2}
$$

其中 $a_1, a_2, \dots, a_n, \dots$ 是待定的系数. 把(5-2)代入(5-1)中, 便得一恒等式, 比较所得恒等式两端 $x - x_0$ 的同次幂的系数, 就可定出常数 $a_1, a_2, \dots$, 以这些常数为系数的级数(5-2)在其收敛区间内就是方程(5-1)满足初值条件 $y|_{x = x_0} = y_0$ 的特解.

例6 求方程 $\frac{\mathrm{dy}}{\mathrm{dx}} = -y - x$ 满足 $y|_{x=0} = 2$ 的特解.

解 这时, $x_{0}=0,y_{0}=2$ . 故设方程的特解为

$$
y = 2 + a _ {1} x + a _ {2} x ^ {2} + \dots + a _ {n} x ^ {n} + \dots .
$$

由此，得  $y' = a_{1} + 2a_{2}x + \cdots + na_{n}x^{n-1} + \cdots$

将 y 及  $y'$  的幂级数展开式代入方程, 得

$$
a _ {1} + 2 a _ {2} x + \dots + n a _ {n} x ^ {n - 1} + \dots = - 2 - (a _ {1} + 1) x - a _ {2} x ^ {2} - \dots - a _ {n} x ^ {n} - \dots .
$$

上式为恒等式, 比较上式两端 x 的同次幂的系数, 得

$$
a _ {1} = - 2, \quad 2 a _ {2} = - (a _ {1} + 1), \quad 3 a _ {3} = - a _ {2}, \quad \dots , \quad n a _ {n} = - a _ {n - 1}, \quad \dots .
$$

故 $a_1 = -2, a_2 = \frac{1}{2}, a_3 = -\frac{1}{3!}, \cdots$ 由数学归纳法可得

$$
a _ {n} = (- 1) ^ {n} \frac {1}{n !} \quad (n \geqslant 2).
$$

于是,得

$$
y = 2 - 2 x + \frac {1}{2 !} x ^ {2} - \frac {1}{3 !} x ^ {3} + \dots + (- 1) ^ {n} \frac {1}{n !} x ^ {n} + \dots
$$

282

---

第五节 函数的幂级数展开式的应用

$$
\begin{array}{l} = 1 - x + \left[ 1 - x + \frac {1}{2 !} x ^ {2} - \frac {1}{3 !} x ^ {3} + \dots + (- 1) ^ {n} \frac {1}{n !} x ^ {n} + \dots \right] \\ = 1 - x + \mathrm{e} ^ {- x}. \\ \end{array}
$$

这就是所求的特解.

事实上,所给方程是一阶线性的,容易求得它的通解为  $y = C e^{-x} + 1 - x$ , 由条件  $y \mid_{x=0} = 2$  确定常数 C = 1, 即得方程的特解  $y = e^{-x} + 1 - x$ .

关于二阶齐次线性方程

$$
y ^ {\prime \prime} + P (x) y ^ {\prime} + Q (x) y = 0 \tag {5-3}
$$

用幂级数求解的问题,我们先叙述一个定理:

定理 如果方程(5-3)中的系数 $P(x)$ 与 $Q(x)$ 可在 $-R < x < R$ 内展开为 $x$ 的幂级数, 那么在 $-R < x < R$ 内方程(5-3)必有形如

$$
y = \sum_ {n = 0} ^ {\infty} a _ {n} x ^ {n}
$$

的解.

这定理的证明从略.

例7 求微分方程

$$
y ^ {\prime \prime} - x y = 0
$$

满足初值条件

$$
y \mid_ {x = 0} = 0, \quad y ^ {\prime} \mid_ {x = 0} = 1
$$

的特解.

解 这里 $P(x) = 0, Q(x) = -x$ 在整个数轴上满足定理的条件. 因此所求的解可在整个数轴上展开成 $x$ 的幂级数

$$
y = a _ {0} + a _ {1} x + a _ {2} x ^ {2} + \dots + a _ {n} x ^ {n} + \dots = \sum_ {n = 0} ^ {\infty} a _ {n} x ^ {n}. \tag {5-4}
$$

由条件  $y|_{x=0}=0$  , 得  $a_{0}=0$ . 对级数 (5-4) 逐项求导, 有

$$
y ^ {\prime} = a _ {1} + 2 a _ {2} x + 3 a _ {3} x ^ {2} + \dots + n a _ {n} x ^ {n - 1} + \dots = \sum_ {n = 1} ^ {\infty} n a _ {n} x ^ {n - 1},
$$

由条件 $y^{\prime}|_{x = 0} = 1$ ，得 $a_1 = 1.$ 于是所求特解 $y$ 及 $y^{\prime}$ 的展开式成为

$$
y = x + a _ {2} x ^ {2} + a _ {3} x ^ {3} + \dots + a _ {n} x ^ {n} + \dots = x + \sum_ {n = 2} ^ {\infty} a _ {n} x ^ {n}, \tag {5-5}
$$

$$
y ^ {\prime} = 1 + 2 a _ {2} x + 3 a _ {3} x ^ {2} + \dots + n a _ {n} x ^ {n - 1} + \dots = 1 + \sum_ {n = 2} ^ {\infty} n a _ {n} x ^ {n - 1}. \tag {5-6}
$$

对级数(5-6)逐项求导,得

$$
y ^ {\prime \prime} = 2 a _ {2} + 3 \times 2 a _ {3} x + \dots + n (n - 1) a _ {n} x ^ {n - 2} + \dots = \sum_ {n = 2} ^ {\infty} n (n - 1) a _ {n} x ^ {n - 2}. \tag {5-7}
$$

把(5-5)和(5-7)代入所给方程,并按 $x$ 的升幂集项,得

283

---

第十二章 无穷级数

$$
2 a _ {2} + 3 \times 2 a _ {3} x + (4 \times 3 a _ {4} - 1) x ^ {2} + (5 \times 4 a _ {5} - a _ {2}) x ^ {3} +
$$

$$
(6 \times 5 a _ {6} - a _ {3}) x ^ {4} + \dots + [ (n + 2) (n + 1) a _ {n + 2} - a _ {n - 1} ] x ^ {n} + \dots = 0.
$$

因为上式是恒等式,所以上式左端各项的系数必全为零,于是有

$$
a _ {2} = 0, \quad a _ {3} = 0, \quad a _ {4} = \frac {1}{4 \times 3}, \quad a _ {5} = 0, \quad a _ {6} = 0, \quad \dots ,
$$

一般地

$$
a _ {n + 2} = \frac {a _ {n - 1}}{(n + 2) (n + 1)} \quad (n = 3, 4, \dots).
$$

从这递推公式可以推得

$$
a _ {7} = \frac {a _ {4}}{7 \times 6} = \frac {1}{7 \times 6 \times 4 \times 3}, \quad a _ {8} = \frac {a _ {5}}{8 \times 7} = 0, \quad a _ {9} = \frac {a _ {6}}{9 \times 8} = 0,
$$

$$
a _ {1 0} = \frac {a _ {7}}{1 0 \times 9} = \frac {1}{1 0 \times 9 \times 7 \times 6 \times 4 \times 3}, \dots ,
$$

一般地

$$
a _ {3 m - 1} = a _ {3 m} = 0,
$$

$$
a _ {3 m + 1} = \frac {1}{(3 m + 1) \times (3 m) \times \cdots \times 7 \times 6 \times 4 \times 3} \quad (m = 1, 2, \dots).
$$

于是所求的特解为

$$
\begin{array}{l} y = x + \frac {x ^ {4}}{4 \times 3} + \frac {x ^ {7}}{7 \times 6 \times 4 \times 3} + \frac {x ^ {1 0}}{1 0 \times 9 \times 7 \times 6 \times 4 \times 3} + \dots + \\ \frac {x ^ {3 m + 1}}{(3 m + 1) \times (3 m) \times \cdots \times 1 0 \times 9 \times 7 \times 6 \times 4 \times 3} + \dots \\ \end{array}
$$

## 三、欧拉公式

设有复数项级数为

$$
(u _ {1} + v _ {1} \mathrm{i}) + (u _ {2} + v _ {2} \mathrm{i}) + \dots + (u _ {n} + v _ {n} \mathrm{i}) + \dots , \tag {5-8}
$$

其中  $u_{n}$  与  $v_{n}$  ( $n=1,2,3,\cdots$ ) 为实常数或实函数. 如果实部所成的级数

$$
u _ {1} + u _ {2} + \dots + u _ {n} + \dots \tag {5-9}
$$

收敛于和 u，并且虚部所成的级数

$$
v _ {1} + v _ {2} + \dots + v _ {n} + \dots \tag {5-10}
$$

收敛于和 v, 那么就说级数 (5-8) 收敛且其和为  $u + vi$ .

如果级数(5-8)各项的模所构成的级数

$$
\sqrt {u _ {1} ^ {2} + v _ {1} ^ {2}} + \sqrt {u _ {2} ^ {2} + v _ {2} ^ {2}} + \dots + \sqrt {u _ {n} ^ {2} + v _ {n} ^ {2}} + \dots
$$

收敛,那么称级数(5-8)绝对收敛.如果级数(5-8)绝对收敛,由于

284

---

第五节 函数的幂级数展开式的应用

$$
\mid u _ {n} \mid \leqslant \sqrt {u _ {n} ^ {2} + v _ {n} ^ {2}}, \mid v _ {n} \mid \leqslant \sqrt {u _ {n} ^ {2} + v _ {n} ^ {2}} \quad (n = 1, 2, 3, \dots),
$$

那么级数(5-9)与(5-10)绝对收敛,从而级数(5-8)收敛.

考察复数项级数

$$
1 + z + \frac {1}{2 !} z ^ {2} + \dots + \frac {1}{n !} z ^ {n} + \dots \quad (z = x + y i). \tag {5-11}
$$

可以证明级数(5-11)在整个复平面上是绝对收敛的.在 $x$ 轴上 $(z = x)$ 它表示指数函数$\mathrm{e}^x$ ，在整个复平面上我们用它来定义复变量指数函数，记作 $\mathbf{e}^z$ .于是 $\mathbf{e}^z$ 定义为

$$
\mathrm{e} ^ {z} = 1 + z + \frac {1}{2 !} z ^ {2} + \dots + \frac {1}{n !} z ^ {n} + \dots \quad (| z | <   \infty). \tag {5-12}
$$

当 x=0 时, z 为纯虚数 yi, (5-12) 式成为

$$
\begin{array}{l} \mathrm{e} ^ {y \mathrm{i}} = 1 + y \mathrm{i} + \frac {1}{2 !} (y \mathrm{i}) ^ {2} + \frac {1}{3 !} (y \mathrm{i}) ^ {3} + \dots + \frac {1}{n !} (y \mathrm{i}) ^ {n} + \dots \\ = 1 + y \mathrm{i} - \frac {1}{2 !} y ^ {2} - \frac {1}{3 !} y ^ {3} \mathrm{i} + \frac {1}{4 !} y ^ {4} + \frac {1}{5 !} y ^ {5} \mathrm{i} - \dots \\ = \left(1 - \frac {1}{2 !} y ^ {2} + \frac {1}{4 !} y ^ {4} - \dots\right) + \left(y - \frac {1}{3 !} y ^ {3} + \frac {1}{5 !} y ^ {5} - \dots\right) i \\ = \cos y + \mathrm{i} \sin y. \\ \end{array}
$$

把 y 换写为 x, 上式变为

$$
\mathrm{e} ^ {x \mathrm{i}} = \cos x + \mathrm{i} \sin x, \tag {5-13}
$$

这就是欧拉(Euler)公式.

应用公式(5-13)，复数z可以表示为指数形式:

$$
z = \rho (\cos \theta + \mathrm{i} \sin \theta) = \rho \mathrm{e} ^ {\mathrm{i} \theta}, \tag {5-14}
$$

其中  $\rho = |z|$  是 z 的模,  $\theta = \arg z$  是 z 的辐角(图 12-5).

在(5-13)式中把 $x$ 换成 $-x$, 又有

$$
\mathrm{e} ^ {- x \mathrm{i}} = \cos x - \mathrm{i} \sin x.
$$

把上式与(5-13)相加或相减,得

$$
\left\{ \begin{array}{l} \cos x = \frac {\mathrm{e} ^ {x \mathrm{i}} + \mathrm{e} ^ {- x \mathrm{i}}}{2}, \\ \sin x = \frac {\mathrm{e} ^ {x \mathrm{i}} - \mathrm{e} ^ {- x \mathrm{i}}}{2 \mathrm{i}}. \end{array} \right. \tag {5-15}
$$

这两个式子也叫做欧拉公式.(5-13)式或(5-15)式揭示了三角函数与复变量指数函数之间的一种联系.

最后,根据定义式(5-12),并利用幂级数的乘法,我们不难验证

$$
\mathrm{e} ^ {z _ {1} + z _ {2}} = \mathrm{e} ^ {z _ {1}} \cdot \mathrm{e} ^ {z _ {2}}.
$$

![](../../raw/pages_0289-0320/images/page_291_image_22.jpg)

<details>
<summary>text_image</summary>

y
z=x+yi
ρ
θ
O
x
x
</details>

图12-5

285

---

第十二章 无穷级数

特殊地,取 $z_{1}$ 为实数 $x,z_{2}$ 为纯虚数yi,则有

$$
\mathrm{e} ^ {x + y \mathrm{i}} = \mathrm{e} ^ {x} \cdot \mathrm{e} ^ {y \mathrm{i}} = \mathrm{e} ^ {x} (\cos y + \mathrm{i} \sin y).
$$

这就是说,复变量指数函数  $e^{z}$  在  $z=x+yi$  处的值是模为  $e^{x}$ 、辐角为 y 的复数.

## 习题12-5

1. 利用函数的幂级数展开式求下列各数的近似值:

(1)  $\ln 3$  (误差不超过 0.0001); (2)  $\sqrt{e}$  (误差不超过 0.001);
(3)  $\sqrt[9]{522}$  (误差不超过0.00001); (4)  $\cos 2^{\circ}$  (误差不超过0.0001).

2. 利用被积函数的幂级数展开式求下列定积分的近似值:

(1) $\int_{0}^{0.5}\frac{1}{1 + x^4}\mathrm{d}x$ （误差不超过0.0001）； (2) $\int_0^{0.5}\frac{\arctan x}{x}\mathrm{d}x$ （误差不超过0.001）.

3. 试用幂级数求下列各微分方程的解:

(1)  $y' - xy - x = 1$ ;

(2) $y''+xy'+y=0;$

(3) $(1-x)y'=x^{2}-y.$

4. 试用幂级数求下列方程满足所给初值条件的特解:

(1) $y' = y^2 + x^3, y \mid_{x=0} = \frac{1}{2};$

(2) $(1-x)y'+y=1+x,y\mid_{x=0}=0.$

5. 验证函数  $y(x)=1+\frac{x^{3}}{3!}+\frac{x^{6}}{6!}+\cdots+\frac{x^{3n}}{(3n)!}+\cdots$  ( $-\infty<x<+\infty$ ) 满足微分方程  $y''+y'+y=e^{x}$ ，并利用此结果求幂级数  $\sum_{n=0}^{\infty}\frac{x^{3n}}{(3n)!}$  的和函数.

6. 利用欧拉公式将函数  $e^{x}\cos x$  展开成 x 的幂级数.

## \* 第六节 函数项级数的一致收敛性及一致收敛级数的基本性质

## 一、函数项级数的一致收敛性

我们知道,有限个连续函数的和仍然是连续函数,有限个函数的和的导数及积分也分别等于它们的导数及积分的和.但是对于无穷多个函数的和是否也具有这些性质呢?换句话说,无穷多个连续函数的和 $s(x)$ 是否仍然是连续函数?无穷多个函数的导数及积分的和是否仍然分别等于它们的和函数的导数及积分呢?我们曾经指出,对于幂级数来说,回答是肯定的.但是,对于一般的函数项级数是否都是如此呢?下面来看一个例子.

286

---

\*第六节 函数项级数的一致收敛性及一致收敛级数的基本性质

例1 函数项级数

$$
x + (x ^ {2} - x) + (x ^ {3} - x ^ {2}) + \dots + (x ^ {n} - x ^ {n - 1}) + \dots
$$

的每一项都在[0,1]上连续,其前n项之和为 $s_{n}(x)=x^{n}$ ，因此和函数为

$$
s (x) = \lim _ {n \to \infty} s _ {n} (x) = \left\{ \begin{array}{l l} 0, & 0 \leqslant x <   1, \\ 1, & x = 1. \end{array} \right.
$$

这和函数 $s(x)$ 在 $x = 1$ 处间断.由此可见，函数项级数的每一项在 $[a,b]$ 上连续，并且级数在 $[a,b]$ 上收敛，其和函数不一定在 $[a,b]$ 上连续.也可以举出这样的例子，函数项级数的每一项的导数及积分所成的级数的和并不等于它们的和函数的导数及积分.这就提出了这样一个问题:对什么级数，能够从级数每一项的连续性得出它的和函数的连续性，从级数的每一项的导数及积分所成的级数之和得出原来级数的和函数的导数及积分呢？要回答这个问题，就需要引入下面的函数项级数的一致收敛性概念.

设函数项级数

$$
u _ {1} (x) + u _ {2} (x) + \dots + u _ {n} (x) + \dots
$$

在区间 $I$ 上收敛于和 $s(x)$. 也就是对于区间 $I$ 上的每一个值 $x_0$, 数项级数 $\sum_{n=1}^{\infty} u_n(x_0)$ 收敛于 $s(x_0)$, 即级数的部分和所成的数列

$$
s _ {n} (x _ {0}) = \sum_ {i = 1} ^ {n} u _ {i} (x _ {0}) \longrightarrow s (x _ {0}) \quad (n \longrightarrow \infty).
$$

按数列极限的定义,对于任意给定的正数  $\varepsilon$  以及区间 I 上的每一个值  $x_{0}$ , 都存在着一个正整数 N, 使得当 n > N 时, 有不等式

$$
\mid s (x _ {0}) - s _ {n} (x _ {0}) \mid <   \varepsilon ,
$$

即

$$
\mid r _ {n} (x _ {0}) \mid = \Big | \sum_ {i = n + 1} ^ {\infty} u _ {i} (x _ {0}) \Big | <   \varepsilon .
$$

这个数 $N$ 一般说来不仅依赖于 $\varepsilon$, 而且也依赖于 $x_0$, 我们记它为 $N(x_0, \varepsilon)$. 如果对于某一函数项级数能够找到这样一个正整数 $N$, 它只依赖于 $\varepsilon$ 而不依赖于 $x_0$, 也就是对区间 $I$ 上的每一个值 $x_0$ 都能适用的 $N(\varepsilon)$, 对这类级数我们给一个特殊的名称以区别于一般的收敛级数, 这就是下面的一致收敛的定义.

定义 设有函数项级数 $\sum_{n=1}^{\infty} u_n(x)$. 如果对于任意给定的正数 $\varepsilon$, 都存在着一个只依赖于 $\varepsilon$ 的正整数 $N$, 使得当 $n > N$ 时, 对区间 $I$ 上的一切 $x$, 都有不等式

$$
\mid r _ {n} (x) \mid = \mid s (x) - s _ {n} (x) \mid <   \varepsilon
$$

成立,那么称函数项级数  $\sum_{n=1}^{\infty}u_{n}(x)$  在区间 I 上一致收敛于和  $s(x)$ ，也称函数序列

287

---

第十二章 无穷级数

$\{s_{n}(x)\}$  在区间 I 上一致收敛于  $s(x)$ .

以上函数项级数一致收敛的定义在几何上可解释为: 只要 n 充分大  $(n > N)$ ，在区间 I 上的所有曲线  $y = s_{n}(x)$  将位于曲线

$$
y = s (x) + \varepsilon \quad \text {与} \quad y = s (x) - \varepsilon
$$

之间(图 12-6).

![](../../raw/pages_0289-0320/images/page_294_image_5.jpg)

<details>
<summary>text_image</summary>

y
y=s(x)+ε
ε
ε
y=s_n(x)
y=s(x)
y=s(x)-ε
O
I
x
</details>

图12-6

例2 研究级数

$$
\frac {1}{x + 1} + \left(\frac {1}{x + 2} - \frac {1}{x + 1}\right) + \dots + \left(\frac {1}{x + n} - \frac {1}{x + n - 1}\right) + \dots
$$

在区间 $[0,+\infty)$ 上的一致收敛性.

解 级数的前 $n$ 项和 $s_n(x) = \frac{1}{x + n}$, 因此级数的和

$$
s (x) = \lim _ {n \to \infty} s _ {n} (x) = \lim _ {n \to \infty} \frac {1}{x + n} = 0 \quad (0 \leqslant x <   + \infty).
$$

于是,余项的绝对值

$$
\mid r _ {n} (x) \mid = \mid s (x) - s _ {n} (x) \mid = \frac {1}{x + n} \leqslant \frac {1}{n} \quad (0 \leqslant x <   + \infty).
$$

对于任给 $\varepsilon > 0$，取正整数 $N \geqslant \frac{1}{\varepsilon}$，则当 $n > N$ 时，对于区间 $[0, +\infty)$ 上的一切 $x$，有

$$
\mid r _ {n} (x) \mid <   \varepsilon .
$$

根据定义,所给级数在区间 $[0,+\infty)$ 上一致收敛于 $s(x)\equiv0$ .

例3 研究例1中的级数

$$
x + (x ^ {2} - x) + \dots + (x ^ {n} - x ^ {n - 1}) + \dots
$$

在区间 $(0,1)$ 内的一致收敛性.

解 这级数在区间(0,1)内处处收敛于和 $s(x) \equiv 0$, 但并不一致收敛. 事实上, 这个级数的部分和 $s_n(x) = x^n$, 对于任意一个正整数 $n$, 取 $x_n = \frac{1}{\sqrt[n]{2}}$, 于是

$$
s _ {n} (x _ {n}) = x _ {n} ^ {n} = \frac {1}{2},
$$

但 $s(x_{n}) = 0$ ，从而

$$
\mid r _ {n} (x _ {n}) \mid = \mid s (x _ {n}) - s _ {n} (x _ {n}) \mid = \frac {1}{2}.
$$

所以, 只要取 $\varepsilon < \frac{1}{2}$, 不论 $n$ 多么大, 在 $(0,1)$ 内总存在这样的点 $x_{n}$, 使得 $|r_{n}(x_{n})| > \varepsilon$, 因此所给级数在 $(0,1)$ 内不一致收敛. 这表明虽然函数序列 $s_{n}(x) = x^{n}$ 在 $(0,1)$ 内处处

288

---

\*第六节 函数项级数的一致收敛性及一致收敛级数的基本性质

收敛于 $s(x) \equiv 0$，但 $s_n(x)$ 在 $(0,1)$ 内各点处收敛于零的“快慢”程度是不一致的，从图12-7中我们也可以看出这一情形。

可是对于任意正数 $r < 1$ ，这级数在 $[0, r]$ 上一致收敛. 这是因为当 $x = 0$ 时，显然

$$
\mid r _ {n} (x) \mid = x ^ {n} <   \varepsilon ;
$$

当 $0 < x \leqslant r$ 时，要使 $x^n < \varepsilon$ （不妨设 $\varepsilon < 1$），只要 $n \ln x < \ln \varepsilon$ 或 $n > \frac{\ln \varepsilon}{\ln x}$，而 $\frac{\ln \varepsilon}{\ln x}$ 在 $(0, r]$ 上的最大值为

![](../../raw/pages_0289-0320/images/page_295_chart_5.jpg)

<details>
<summary>contour</summary>

| n | Description |
| --- | --- |
| 1 | Curve starting at (0,0) and ending at (1,1) |
| 2 | Curve starting from (0,0) and ending at (1,1) |
| 4 | Curve starting from (0,0) and ending at (1,1) |
| 10 | Curve starting from (0,0) and ending at (1,1) |
| 30 | Curve starting from (0,0) and ending at (1,1) |
</details>

图12-7

$\frac{\ln\varepsilon}{\ln r}$ ，故取正整数 $N\geqslant \frac{\ln\varepsilon}{\ln r}$ ，则当 $n > N$ 时，对 $[0,r]$ 上的一切 $x$ 都有 $x^n <   \varepsilon$

上述例子也说明了一致收敛性与所讨论的区间有关.以上两例都是直接根据定义来判定级数的一致收敛性的,现在介绍一个在实用上较方便的判别法.

定理(魏尔斯特拉斯(Weierstrass)判别法) 如果函数项级数  $\sum_{n=1}^{\infty} u_{n}(x)$  在区间 I 上满足条件:

(1)  $\left|u_{n}(x)\right|\leqslant a_{n}\quad(n=1,2,3,\cdots);$
(2) 正项级数  $\sum_{n=1}^{\infty}a_{n}$  收敛，

那么函数项级数 $\sum_{n=1}^{\infty} u_n(x)$ 在区间 $I$ 上一致收敛.

证 由条件(2)，对任意给定的 $\varepsilon > 0$，根据柯西审敛原理（第一节第三目）存在正整数 $N$，使得当 $n > N$ 时，对任意的正整数 $p$，都有

$$
a _ {n + 1} + a _ {n + 2} + \dots + a _ {n + p} <   \frac {\varepsilon}{2}.
$$

由条件(1)，对任何 $x \in I$ ，都有

$$
\begin{array}{l} \mid u _ {n + 1} (x) + u _ {n + 2} (x) + \dots + u _ {n + p} (x) \mid \leqslant \mid u _ {n + 1} (x) \mid + \mid u _ {n + 2} (x) \mid + \dots + \mid u _ {n + p} (x) \mid \\ \leqslant a _ {n + 1} + a _ {n + 2} + \dots + a _ {n + p} <   \frac {\varepsilon}{2}, \\ \end{array}
$$

令 $p\to \infty$ ，则由上式得

$$
\mid r _ {n} (x) \mid \leqslant \frac {\varepsilon}{2} <   \varepsilon .
$$

因此函数项级数 $\sum_{n=1}^{\infty} u_n(x)$ 在区间 $I$ 上一致收敛.

例 4 证明级数

289

---

第十二章 无穷级数

$$
\frac {\sin x}{1 ^ {2}} + \frac {\sin 2 ^ {2} x}{2 ^ {2}} + \dots + \frac {\sin n ^ {2} x}{n ^ {2}} + \dots
$$

在 $(-∞,+∞)$ 内一致收敛.

证 因为在 $(-∞,+∞)$ 内

$$
\left| \frac {\sin n ^ {2} x}{n ^ {2}} \right| \leqslant \frac {1}{n ^ {2}} \quad (n = 1, 2, 3, \dots),
$$

而 $\sum_{n=1}^{\infty} \frac{1}{n^{2}}$ 收敛, 故由魏尔斯特拉斯判别法, 所给级数在 $(- \infty, +\infty)$ 内一致收敛.

## 二、一致收敛级数的基本性质

一致收敛级数有如下基本性质:

定理1 如果级数 $\sum_{n=1}^{\infty} u_n(x)$ 的各项 $u_n(x)$ 在区间 $[a, b]$ 上都连续，且 $\sum_{n=1}^{\infty} u_n(x)$ 在区间 $[a, b]$ 上一致收敛于 $s(x)$，那么 $s(x)$ 在 $[a, b]$ 上也连续。

证 设 $x_0, x$ 为 $[a, b]$ 上任意两点. 由等式

$$
s (x) = s _ {n} (x) + r _ {n} (x), \quad s (x _ {0}) = s _ {n} (x _ {0}) + r _ {n} (x _ {0})
$$

得

$$
\begin{array}{l} \mid s (x) - s (x _ {0}) \mid = \mid s _ {n} (x) - s _ {n} (x _ {0}) + r _ {n} (x) - r _ {n} (x _ {0}) \mid \\ \leqslant \left| s _ {n} (x) - s _ {n} (x _ {0}) \right| + \left| r _ {n} (x) \right| + \left| r _ {n} (x _ {0}) \right|. \tag {6-1} \\ \end{array}
$$

因为级数 $\sum_{n=1}^{\infty} u_n(x)$ 一致收敛于 $s(x)$, 所以对任意给定的正数 $\varepsilon$, 必有正整数 $N = N(\varepsilon)$, 使得当 $n > N$ 时, 对 $[a, b]$ 上的一切 $x$, 都有

$$
\mid r _ {n} (x) \mid <   \frac {\varepsilon}{3}. \tag {6-2}
$$

当然,也有 $\left|r_{n}(x_{0})\right|<\frac{\varepsilon}{3}$ .选定满足大于N的n之后, $s_{n}(x)$ 是有限项连续函数之和,故 $s_{n}(x)$ 在点 $x_{0}$ 连续,从而必有一个 $\delta>0$ 存在,当 $\left|x-x_{0}\right|<\delta$ 时,总有

$$
\mid s _ {n} (x) - s _ {n} (x _ {0}) \mid <   \frac {\varepsilon}{3}. \tag {6-3}
$$

由(6-1)、(6-2)、(6-3)式可见，对任给 $\varepsilon >0$ ，必有 $\delta >0$ ，当 $|x - x_0| < \delta$ 时，有

$$
\mid s (x) - s (x _ {0}) \mid <   \varepsilon .
$$

所以 $s(x)$ 在点 $x_0$ 处连续，而 $x_0$ 在 $[a, b]$ 上是任意的，因此 $s(x)$ 在 $[a, b]$ 上连续.

定理2 如果级数 $\sum_{n=1}^{\infty} u_n(x)$ 的各项 $u_n(x)$ 在区间 $[a, b]$ 上连续，且 $\sum_{n=1}^{\infty} u_n(x)$ 在 $[a, b]$ 上一致收敛于 $s(x)$，那么级数 $\sum_{n=1}^{\infty} u_n(x)$ 在 $[a, b]$ 上可以逐项积分，即

290

---

\*第六节 函数项级数的一致收敛性及一致收敛级数的基本性质

$$
\int_ {x _ {0}} ^ {x} s (x) \mathrm{d} x = \int_ {x _ {0}} ^ {x} u _ {1} (x) \mathrm{d} x + \int_ {x _ {0}} ^ {x} u _ {2} (x) \mathrm{d} x + \dots + \int_ {x _ {0}} ^ {x} u _ {n} (x) \mathrm{d} x + \dots , \tag {6-4}
$$

其中 $a \leqslant x_0 < x \leqslant b$，并且上式右端的级数在 $[a, b]$ 上也一致收敛。

证 因为级数 $\sum_{n=1}^{\infty} u_n(x)$ 在 $[a, b]$ 上一致收敛，由定理 $1, s(x), r_n(x)$ 都在 $[a, b]$ 上连续，所以积分 $\int_{x_0}^{x} s(x) \mathrm{d}x, \int_{x_0}^{x} r_n(x) \mathrm{d}x$ 存在，从而有

$$
\left| \int_ {x _ {0}} ^ {x} s (x) \mathrm{d} x - \int_ {x _ {0}} ^ {x} s _ {n} (x) \mathrm{d} x \right| = \left| \int_ {x _ {0}} ^ {x} r _ {n} (x) \mathrm{d} x \right| \leqslant \int_ {x _ {0}} ^ {x} | r _ {n} (x) | \mathrm{d} x.
$$

又由级数的一致收敛性,对任给正数  $\varepsilon$ , 必有  $N=N(\varepsilon)$ , 使得当 n>N 时, 对  $[a,b]$  上的一切 x, 都有

$$
\mid r _ {n} (x) \mid <   \frac {\varepsilon}{b - a}.
$$

于是, 当 n > N 时有

$$
\left| \int_ {x _ {0}} ^ {x} s (x) \mathrm{d} x - \int_ {x _ {0}} ^ {x} s _ {n} (x) \mathrm{d} x \right| \leqslant \int_ {x _ {0}} ^ {x} | r _ {n} (x) | \mathrm{d} x <   \frac {\varepsilon}{b - a} (x - x _ {0}) \leqslant \varepsilon .
$$

根据极限的定义,有

$$
\int_ {x _ {0}} ^ {x} s (x) \mathrm{d} x = \lim _ {n \to \infty} \int_ {x _ {0}} ^ {x} s _ {n} (x) \mathrm{d} x = \lim _ {n \to \infty} \sum_ {i = 1} ^ {n} \int_ {x _ {0}} ^ {x} u _ {i} (x) \mathrm{d} x,
$$

即

$$
\int_ {x _ {0}} ^ {x} s (x) \mathrm{d} x = \sum_ {i = 1} ^ {\infty} \int_ {x _ {0}} ^ {x} u _ {i} (x) \mathrm{d} x.
$$

由于 $N$ 只依赖于 $\varepsilon$ 而与 $x_0, x$ 无关，所以级数 $\sum_{i=1}^{\infty} \int_{x_0}^{x} u_i(x) \mathrm{d}x$ 在 $[a, b]$ 上一致收敛.

定理3 如果级数 $\sum_{n=1}^{\infty} u_n(x)$ 在区间 $[a, b]$ 上收敛于和 $s(x)$，它的各项 $u_n(x)$ 都具有连续导数 $u_n'(x)$，并且级数 $\sum_{n=1}^{\infty} u_n'(x)$ 在 $[a, b]$ 上一致收敛，那么级数 $\sum_{n=1}^{\infty} u_n(x)$ 在 $[a, b]$ 上也一致收敛，且可逐项求导，即

$$
s ^ {\prime} (x) = u _ {1} ^ {\prime} (x) + u _ {2} ^ {\prime} (x) + \dots + u _ {n} ^ {\prime} (x) + \dots . \tag {6-5}
$$

证 先证等式(6-5). 由于 $\sum_{n=1}^{\infty} u_n'(x)$ 在 $[a, b]$ 上一致收敛, 设其和为 $\varphi(x)$, 即 $\sum_{n=1}^{\infty} u_n'(x) = \varphi(x)$, 欲证(6-5), 只需证 $\varphi(x) = s'(x)$ 就可以了.

根据定理1知, $\varphi(x)$ 在 $[a,b]$ 上连续,根据定理2,级数 $\sum_{n=1}^{\infty}u_{n}^{\prime}(x)$ 可逐项积分,故有

$$
\int_ {x _ {0}} ^ {x} \varphi (x) \mathrm{d} x = \sum_ {n = 1} ^ {\infty} \int_ {x _ {0}} ^ {x} u _ {n} ^ {\prime} (x) \mathrm{d} x = \sum_ {n = 1} ^ {\infty} \left[ u _ {n} (x) - u _ {n} (x _ {0}) \right],
$$

291

---

第十二章 无穷级数

而

$$
\sum_ {n = 1} ^ {\infty} u _ {n} (x) = s (x), \quad \sum_ {n = 1} ^ {\infty} u _ {n} (x _ {0}) = s (x _ {0}),
$$

故

$$
\sum_ {n = 1} ^ {\infty} \left[ u _ {n} (x) - u _ {n} (x _ {0}) \right] = s (x) - s (x _ {0}),
$$

从而有

$$
\int_ {x _ {0}} ^ {x} \varphi (x) \mathrm{d} x = s (x) - s (x _ {0}),
$$

其中 $a \leqslant x_0 < x \leqslant b$. 上式两端求导, 即得关系式

$$
\varphi (x) = s ^ {\prime} (x).
$$

再证级数 $\sum_{n=1}^{\infty} u_n(x)$ 在 $[a, b]$ 上也一致收敛.

根据定理2,级数  $\sum_{n=1}^{\infty}\int_{x_{0}}^{x}u_{n}^{\prime}(x)\mathrm{d}x$  在  $[a,b]$  上一致收敛,而

$$
\sum_ {n = 1} ^ {\infty} \int_ {x _ {0}} ^ {x} u _ {n} ^ {\prime} (x) \mathrm{d} x = \sum_ {n = 1} ^ {\infty} u _ {n} (x) - \sum_ {n = 1} ^ {\infty} u _ {n} (x _ {0}),
$$

所以

$$
\sum_ {n = 1} ^ {\infty} u _ {n} (x) = \sum_ {n = 1} ^ {\infty} \int_ {x _ {0}} ^ {x} u _ {n} ^ {\prime} (x) \mathrm{d} x + \sum_ {n = 1} ^ {\infty} u _ {n} (x _ {0}),
$$

由此即得所要证的结论.

必须注意,级数一致收敛并不能保证可以逐项求导.例如,在例4中我们已证明了级数

$$
\frac {\sin x}{1 ^ {2}} + \frac {\sin 2 ^ {2} x}{2 ^ {2}} + \dots + \frac {\sin n ^ {2} x}{n ^ {2}} + \dots
$$

在任何区间 $[a, b]$ 上都是一致收敛的，但逐项求导后的级数

$$
\cos x + \cos 2 ^ {2} x + \dots + \cos n ^ {2} x + \dots ,
$$

其一般项不趋于零,所以对任意值 x 都是发散的,因此原级数不可以逐项求导.

下面我们来讨论幂级数的一致收敛性.

定理4 如果幂级数 $\sum_{n=0}^{\infty} a_n x^n$ 的收敛半径为 $R > 0$, 那么此级数在 $(-R, R)$ 内的任一闭区间 $[a, b]$ 上一致收敛.

证 记 $r = \max \{|a|, |b|\}$，则对 $[a, b]$ 上的一切 $x$，都有

$$
\mid a _ {n} x ^ {n} \mid \leqslant \mid a _ {n} r ^ {n} \mid \quad (n = 0, 1, 2, \dots),
$$

而 $0 < r < R$ ，根据第三节定理1级数 $\sum_{n=0}^{\infty} a_n r^n$ 绝对收敛，由魏尔斯特拉斯判别法即得所要证的结论.

292

---

\*第六节 函数项级数的一致收敛性及一致收敛级数的基本性质

进一步还可证明,如果幂级数  $\sum_{n=0}^{\infty}a_{n}x^{n}$  在收敛区间的端点收敛,那么一致收敛的区间可扩大到包含端点.

下面我们来证明在第三节中指出的关于幂级数在其收敛区间内的和函数的连续性、逐项可导、逐项可积的结论.

关于和函数的连续性及逐项可积的结论,由定理4和定理1、定理2立即可得.关于逐项可导的结论,我们重新叙述成如下定理并给出证明.

定理5 如果幂级数 $\sum_{n=0}^{\infty} a_n x^n$ 的收敛半径为 $R > 0$, 那么其和函数 $s(x)$ 在 $(-R, R)$ 内可导, 且有逐项求导公式

$$
s ^ {\prime} (x) = \left(\sum_ {n = 0} ^ {\infty} a _ {n} x ^ {n}\right) ^ {\prime} = \sum_ {n = 1} ^ {\infty} n a _ {n} x ^ {n - 1},
$$

逐项求导后所得到的幂级数与原级数有相同的收敛半径.

证 先证级数 $\sum_{n=1}^{\infty} na_n x^{n-1}$ 在 $(-R, R)$ 内收敛.

在 $(-R,R)$ 内任意取定x,再选定 $x_{1}$ ,使得 $|x|<x_{1}<R.$ 记 $q=\frac{|x|}{x_{1}}<1$ ,则

$$
\left| n a _ {n} x ^ {n - 1} \right| = n \left| \frac {x}{x _ {1}} \right| ^ {n - 1} \cdot \frac {1}{x _ {1}} \left| a _ {n} x _ {1} ^ {n} \right| = n q ^ {n - 1} \cdot \frac {1}{x _ {1}} \left| a _ {n} x _ {1} ^ {n} \right|,
$$

由比值审敛法可知级数 $\sum_{n=1}^{\infty} n q^{n-1}$ 收敛, 于是

$$
n q ^ {n - 1} \longrightarrow 0 \quad (n \longrightarrow \infty),
$$

故数列 $\{nq^{n - 1}\}$ 有界，必有 $M > 0$ ，使得

$$
n q ^ {n - 1} \cdot \frac {1}{x _ {1}} \leqslant M \quad (n = 1, 2, \dots).
$$

又 $0 < x_{1} < R$ ，级数 $\sum_{n=1}^{\infty}\left|a_{n}x_{1}^{n}\right|$ 收敛，由比较审敛法的推论即得级数 $\sum_{n=1}^{\infty}na_{n}x^{n-1}$ 收敛.

由定理4,级数 $\sum_{n=1}^{\infty} na_n x^{n-1}$ 在 $(-R, R)$ 内的任一闭区间 $[a, b]$ 上一致收敛, 故幂级数 $\sum_{n=1}^{\infty} a_n x^n$ 在 $[a, b]$ 上符合定理3的条件, 从而可逐项求导. 再由 $[a, b]$ 在 $(-R, R)$ 内的任意性, 即得幂级数 $\sum_{n=1}^{\infty} a_n x^n$ 在 $(-R, R)$ 内可逐项求导.

设幂级数 $\sum_{n=1}^{\infty} na_n x^{n-1}$ 的收敛半径为 $R'$, 上面已证得 $R \leqslant R'$. 将此幂级数在 $[0, x]$ ($|x| < R'$) 上逐项积分即得 $\sum_{n=1}^{\infty} a_n x^n$, 因逐项积分所得级数的收敛半径不会缩小, 所以

293

---

第十二章 无穷级数

$R'\leqslant R$ , 于是  $R'=R$ . 定理 5 证毕.

## \*习题12-6

1. 已知函数序列  $s_{n}(x)=\sin\frac{x}{n}\quad(n=1,2,3,\cdots)$  在  $(-∞,+∞)$  上收敛于 0,

(1) 问  $N(\varepsilon, x)$  取多大, 能使当 n > N 时,  $s_{n}(x)$  与其极限之差的绝对值小于正数  $\varepsilon$ ;
(2) 证明 $s_n(x)$ 在任一有限区间 $[a, b]$ 上一致收敛.

2. 已知级数  $x^{2}+\frac{x^{2}}{1+x^{2}}+\frac{x^{2}}{(1+x^{2})^{2}}+\cdots$  在  $(-∞,+∞)$  上收敛.

(1) 求出该级数的和;
(2) 问 $N(\varepsilon, x)$ 取多大, 能使当 $n > N$ 时, 级数的余项 $r_n$ 的绝对值小于正数 $\varepsilon$;
(3) 分别讨论级数在区间  $[0,1]$ ,  $\left\lceil\frac{1}{2},1\right\rceil$  上的一致收敛性.

3. 按定义讨论下列级数在所给区间上的一致收敛性:

(1) $\sum_{n=1}^{\infty}(-1)^{n-1}\frac{x^2}{(1+x^2)^n}, (-\infty, +\infty)$;

(2) $\sum_{n=0}^{\infty}(1-x)x^{n}, (0,1)$.

4. 利用魏尔斯特拉斯判别法证明下列级数在所给区间上的一致收敛性:

(1) $\sum_{n=1}^{\infty} \frac{\cos nx}{2^n}, (-\infty, +\infty)$;

(2) $\sum_{n=1}^{\infty} \frac{\sin nx}{\sqrt[3]{n^4 + x^4}}, (-\infty, +\infty)$;

(3) $\sum_{n=1}^{\infty} x^{2} \mathrm{e}^{-nx}, [0, +\infty)$;

(4) $\sum_{n=1}^{\infty} \frac{e^{-nx}}{n!}, (-10, 10)$;

(5) $\sum_{n=1}^{\infty} \frac{(-1)^{n}(1 - e^{-nx})}{n^{2} + x^{2}}, [0, +\infty)$.

## 第七节 傅里叶级数

从本节开始,我们讨论由三角函数组成的函数项级数,即所谓三角级数,着重研究如何把函数展开成三角级数.

## 一、三角级数 三角函数系的正交性

在第一章中,我们介绍过周期函数的概念,周期函数反映了客观世界中的周期运动.

正弦函数是一种常见而简单的周期函数.例如描述简谐振动的函数

$$
y = A \sin (\omega t + \varphi)
$$

294

---

第七节 傅里叶级数

就是一个以 $\frac{2\pi}{\omega}$ 为周期的正弦函数,其中y表示动点的位置,t表示时间,A为振幅, $\omega$ 为角频率, $\varphi$ 为初相.

在实际问题中,除了正弦函数外,还会遇到非正弦函数的周期函数,它们反映了较

复杂的周期运动. 如电子技术中常用的周期为 T 的矩形波(图 12-8), 就是一个非正弦周期函数的例子.

如何深入研究非正弦周期函数呢？联系到前面介绍过的用函数的幂级数展开式表示与讨论函数，我们也

![](../../raw/pages_0289-0320/images/page_301_chart_5.jpg)

<details>
<summary>line</summary>

| Point | x | u |
| --- | --- | --- |
| 1 | ~-0.5 | E |
| 2 | ~-0.5 | E |
| 3 | ~-0.5 | E |
| 4 | ~-0.5 | E |
| 5 | ~-0.5 | E |
| 6 | ~-0.5 | E |
| 7 | ~-0.5 | E |
| 8 | ~-0.5 | E |
| 9 | ~-0.5 | E |
| 10 | ~-0.5 | E |
| 11 | ~-0.5 | E |
| 12 | ~-0.5 | E |
| 13 | ~-0.5 | E |
| 14 | ~-0.5 | E |
| 15 | ~-0.5 | E |
| 16 | ~-0.5 | E |
| 17 | ~-0.5 | E |
| 18 | ~-0.5 | E |
| 19 | ~-0.5 | E |
| 20 | ~-0.5 | E |
| 21 | ~-0.5 | E |
| 22 | ~-0.5 | E |
| 23 | ~-0.5 | E |
| 24 | ~-0.5 | E |
| 25 | ~-0.5 | E |
| 26 | ~-0.5 | E |
| 27 | ~-0.5 | E |
| 28 | ~-0.5 | E |
| 29 | ~-0.5 | E |
| 30 | ~-0.5 | E |
| 31 | ~-0.5 | E |
| 32 | ~-0.5 | E |
| 33 | ~-0.5 | E |
| 34 | ~-0.5 | E |
| 35 | ~-0.5 | E |
| 36 | ~-0.5 | E |
| 37 | ~-0.5 | E |
| 38 | ~-0.5 | E |
| 39 | ~-0.5 | E |
| 40 | ~-0.5 | E |
| 41 | ~-0.5 | E |
| 42 | ~-0.5 | E |
| 43 | ~-0.5 | E |
| 44 | ~-0.5 | E |
| 45 | ~-0.5 | E |
| 46 | ~-0.5 | E |
| 47 | ~-0.5 | E |
| 48 | ~-0.5 | E |
| 49 | ~-0.5 | E |
| 50 | ~-0.5 | E |
| 51 | ~-0.5 | E |
| 52 | ~-0.5 | E |
| 53 | ~-0.5 | E |
| 54 | ~-0.5 | E |
| 55 | ~-0.5 | E |
| 56 | ~-0.5 | E |
| 57 | ~-0.5 | E |
| 58 | ~-0.5 | E |
| 59 | ~-0.5 | E |
| 60 | ~-0.5 | E |
| 61 | ~-0.5 | E |
| 62 | ~-0.5 | E |
| 63 | ~-0.5 | E |
| 64 | ~-0.5 | E |
| 65 | ~-0.5 | E |
| 66 | ~-0.5 | E |
| 67 | ~-0.5 | E |
| 68 | ~-0.5 | E |
| 69 | ~-0.5 | E |
| 70 | ~-0.5 | E |
| 71 | ~-0.5 | E |
| 72 | ~-0.5 | E |
| 73 | ~-0.5 | E |
| 74 | ~-0.5 | E |
| 75 | ~-0.5 | E |
| 76 | ~-0.5 | E |
| 77 | ~-0.5 | E |
| 78 | ~-0.5 | E |
| 79 | ~-0.5 | E |
| 80 | ~-0.5 | E |
| 81 | ~-0.5 | E |
| 82 | ~-0.5 | E |
| 83 | ~-0.5 | E |
| 84 | ~-0.5 | E |
| 85 | ~-0.5 | E |
| 86 | ~-0.5 | E |
| 87 | ~-0.5 | E |
| 88 | ~-0.5 | E |
| 89 | ~-0.5 | E |
| 90 | ~-0.5 | E |
| 91 | ~-0.5 | E |
| 92 | ~-0.5 | E |
| 93 | ~-0.5 | E |
| 94 | ~-0.5 | E |
| 95 | ~-0.5 | E |
| 96 | ~-0.5 | E |
| 97 | ~-0.5 | E |
| 98 | ~-0.5 | E |
| 99 | ~-0.5 | E |
| 100 | ~-0.5 | E |
</details>

图12-8

想将周期函数展开成由简单的周期函数例如三角函数组成的级数.具体地说,将周期为  $T\left(T=\frac{2\pi}{\omega}\right)$  的周期函数用一系列以 T 为周期的正弦函数  $A_{n}\sin(n\omega t+\varphi_{n})$  组成的级数来表示,记为

$$
f (t) = A _ {0} + \sum_ {n = 1} ^ {\infty} A _ {n} \sin (n \omega t + \varphi_ {n}), \tag {7-1}
$$

其中  $A_{0}, A_{n}, \varphi_{n} (n=1,2,3,\cdots)$  都是常数.

将周期函数按上述方式展开,它的物理意义是很明确的,这就是把一个比较复杂的周期运动看成是许多不同频率的简谐振动的叠加.在电工学上,这种展开称为谐波分析,其中常数项 $A_{0}$ 称为 $f(t)$ 的直流分量, $A_{1}\sin(\omega t+\varphi_{1})$ 称为一次谐波(又叫做基波), $A_{2}\sin(2\omega t+\varphi_{2})$ , $A_{3}\sin(3\omega t+\varphi_{3})$ ,…依次称为二次谐波,三次谐波,等等.

为了以后讨论方便起见,我们将正弦函数 $A_{n}\sin(n\omega t+\varphi_{n})$ 按三角公式变形,得

$$
A _ {n} \sin (n \omega t + \varphi_ {n}) = A _ {n} \sin \varphi_ {n} \cos n \omega t + A _ {n} \cos \varphi_ {n} \sin n \omega t,
$$

并且令 $\frac{a_{0}}{2}=A_{0},a_{n}=A_{n}\sin\varphi_{n},b_{n}=A_{n}\cos\varphi_{n},\omega=\frac{\pi}{l}$ （即T=2l），则(7-1)式右端的级数就可以改写为

$$
\frac {a _ {0}}{2} + \sum_ {n = 1} ^ {\infty} \left(a _ {n} \cos \frac {n \pi t}{l} + b _ {n} \sin \frac {n \pi t}{l}\right). \tag {7-2}
$$

形如(7-2)式的级数叫做三角级数,其中 $a_{0},a_{n},b_{n}(n=1,2,3,\cdots)$ 都是常数.

令 $\frac{\pi t}{l} = x, (7 - 2)$ 式成为

$$
\frac {a _ {0}}{2} + \sum_ {n = 1} ^ {\infty} (a _ {n} \cos n x + b _ {n} \sin n x), \tag {7-3}
$$

这就把以 $2l$ 为周期的三角级数转换成以 $2\pi$ 为周期的三角级数.

295

---

第十二章 无穷级数

下面我们讨论以  $2\pi$  为周期的三角级数(7-3).

如同讨论幂级数时一样,我们必须讨论三角级数(7-3)的收敛问题,以及给定周期为 $2\pi$ 的周期函数如何把它展开成三角级数(7-3).为此,我们首先介绍三角函数系的正交性.

所谓三角函数系

$$
1, \cos x, \sin x, \cos 2 x, \sin 2 x, \dots , \cos n x, \sin n x, \dots \tag {7-4}
$$

在区间 $[-π,π]$ 上正交,就是指在三角函数系(7-4)中任何不同的两个函数的乘积在区间 $[-π,π]$ 上的积分等于零,即

$$
\begin{array}{l} \int_ {- \pi} ^ {\pi} \cos n x \mathrm{d} x = 0 \quad (n = 1, 2, 3, \dots), \\ \int_ {- \pi} ^ {\pi} \sin n x \mathrm{d} x = 0 \quad (n = 1, 2, 3, \dots), \\ \int_ {- \pi} ^ {\pi} \sin k x \cos n x \mathrm{d} x = 0 \quad (k, n = 1, 2, 3, \dots), \\ \int_ {- \pi} ^ {\pi} \cos k x \cos n x \mathrm{d} x = 0 \quad (k, n = 1, 2, 3, \dots , k \neq n), \\ \int_ {- \pi} ^ {\pi} \sin k x \sin n x \mathrm{d} x = 0 \quad (k, n = 1, 2, 3, \dots , k \neq n). \\ \end{array}
$$

以上等式,都可以通过计算定积分来验证,现将第四式验证如下:

利用三角函数中积化和差的公式

$$
\cos k x \cos n x = \frac {1}{2} \big [ \cos (k + n) x + \cos (k - n) x \big ],
$$

当 $k \neq n$ 时, 有

$$
\begin{array}{l} \int_ {- \pi} ^ {\pi} \cos k x \cos n x \mathrm{d} x = \frac {1}{2} \int_ {- \pi} ^ {\pi} [ \cos (k + n) x + \cos (k - n) x ] \mathrm{d} x \\ = \frac {1}{2} \left[ \frac {\sin (k + n) x}{k + n} + \frac {\sin (k - n) x}{k - n} \right] _ {- \pi} ^ {\pi} \\ = 0 \quad (k, n = 1, 2, 3, \dots , k \neq n). \\ \end{array}
$$

其余等式请读者自行验证.

在三角函数系(7-4)中,两个相同函数的乘积在区间 $[-π,π]$ 上的积分不等于零,即

$$
\int_ {- \pi} ^ {\pi} 1 ^ {2} \mathrm{d} x = 2 \pi , \quad \int_ {- \pi} ^ {\pi} \sin^ {2} n x \mathrm{d} x = \pi , \quad \int_ {- \pi} ^ {\pi} \cos^ {2} n x \mathrm{d} x = \pi \quad (n = 1, 2, 3, \dots).
$$

## 二、函数展开成傅里叶级数

设 $f(x)$ 是周期为 $2\pi$ 的周期函数，且能展开成三角级数

296

---

第七节 傅里叶级数

$$
f (x) = \frac {a _ {0}}{2} + \sum_ {k = 1} ^ {\infty} (a _ {k} \cos k x + b _ {k} \sin k x). \tag {7-5}
$$

我们自然要问:系数 $a_{0},a_{1},b_{1},\cdots$ 与函数 $f(x)$ 之间存在着怎样的关系?换句话说,如何利用 $f(x)$ 把 $a_{0},a_{1},b_{1},\cdots$ 表达出来?为此,我们进一步假设(7-5)式右端的级数可以逐项积分.

先求 $a_0$ 对(7-5)式从 $-\pi$ 到 $\pi$ 积分，由于假设(7-5)式右端级数可逐项积分，因此有

$$
\int_ {- \pi} ^ {\pi} f (x) \mathrm{d} x = \int_ {- \pi} ^ {\pi} \frac {a _ {0}}{2} \mathrm{d} x + \sum_ {k = 1} ^ {\infty} \left[ a _ {k} \int_ {- \pi} ^ {\pi} \cos k x \mathrm{d} x + b _ {k} \int_ {- \pi} ^ {\pi} \sin k x \mathrm{d} x \right].
$$

根据三角函数系(7-4)的正交性,等式右端除第一项外,其余各项均为零,所以

$$
\int_ {- \pi} ^ {\pi} f (x) \mathrm{d} x = \frac {a _ {0}}{2} \cdot 2 \pi ,
$$

于是得

$$
a _ {0} = \frac {1}{\pi} \int_ {- \pi} ^ {\pi} f (x) \mathrm{d} x.
$$

其次求 $a_{n}$. 用 $\cos nx$ 乘(7-5)式两端, 再从 $-\pi$ 到 $\pi$ 积分, 我们得到

$$
\int_ {- \pi} ^ {\pi} f (x) \cos n x \mathrm{d} x = \frac {a _ {0}}{2} \int_ {- \pi} ^ {\pi} \cos n x \mathrm{d} x + \sum_ {k = 1} ^ {\infty} \left[ a _ {k} \int_ {- \pi} ^ {\pi} \cos k x \cos n x \mathrm{d} x + b _ {k} \int_ {- \pi} ^ {\pi} \sin k x \cos n x \mathrm{d} x \right].
$$

根据三角函数系(7-4)的正交性,等式右端除k=n的一项外,其余各项均为零,所以

$$
\int_ {- \pi} ^ {\pi} f (x) \cos n x \mathrm{d} x = a _ {n} \int_ {- \pi} ^ {\pi} \cos^ {2} n x \mathrm{d} x = a _ {n} \pi ,
$$

于是得

$$
a _ {n} = \frac {1}{\pi} \int_ {- \pi} ^ {\pi} f (x) \cos n x \mathrm{d} x \quad (n = 1, 2, 3, \dots).
$$

类似地,用  $\sin nx$  乘(7-5)式的两端,再从  $-\pi$  到  $\pi$  积分,可得

$$
b _ {n} = \frac {1}{\pi} \int_ {- \pi} ^ {\pi} f (x) \sin n x \mathrm{d} x \quad (n = 1, 2, 3, \dots).
$$

由于当 $n = 0$ 时，$a_{n}$ 的表达式正好给出 $a_0$ ，因此，已得结果可以合并写成

$$
\left. \begin{array}{l} a _ {n} = \frac {1}{\pi} \int_ {- \pi} ^ {\pi} f (x) \cos n x \mathrm{d} x \quad (n = 0, 1, 2, 3, \dots), \\ b _ {n} = \frac {1}{\pi} \int_ {- \pi} ^ {\pi} f (x) \sin n x \mathrm{d} x \quad (n = 1, 2, 3, \dots). \end{array} \right\} \tag {7-6}
$$

如果公式(7-6)中的积分都存在,这时它们定出的系数 $a_{0},a_{1},b_{1},\cdots$ 叫做函数 $f(x)$ 的傅里叶(Fourier)系数,将这些系数代入(7-5)式右端,所得的三角级数

$$
\frac {a _ {0}}{2} + \sum_ {n = 1} ^ {\infty} (a _ {n} \cos n x + b _ {n} \sin n x)
$$

297

---

第十二章 无穷级数

叫做函数 $f(x)$ 的傅里叶级数.

一个定义在 $(-\infty, +\infty)$ 上周期为 $2\pi$ 的函数 $f(x)$，如果它在一个周期上可积，那么一定可以作出 $f(x)$ 的傅里叶级数。然而，函数 $f(x)$ 的傅里叶级数是否一定收敛？如果它收敛，它是否一定收敛于函数 $f(x)$？一般说来，这两个问题的答案都不是肯定的。那么，$f(x)$ 在怎样的条件下，它的傅里叶级数不仅收敛，而且收敛于 $f(x)$？也就是说，$f(x)$ 满足什么条件可以展开成傅里叶级数？这是我们面临的一个基本问题。

下面我们叙述一个收敛定理(不加证明),它给出关于上述问题的一个重要结论.

定理(收敛定理,狄利克雷(Dirichlet)充分条件) 设 $f(x)$ 是周期为 $2\pi$ 的周期函数,如果它满足

（1）在一个周期内连续或只有有限个第一类间断点，
(2) 在一个周期内至多只有有限个极值点，

那么 $f(x)$ 的傅里叶级数收敛，并且

当 $x$ 是 $f(x)$ 的连续点时，级数收敛于 $f(x)$；

当 $x$ 是 $f(x)$ 的间断点时，级数收敛于 $\frac{1}{2} [f(x^{-}) + f(x^{+})]$.

收敛定理告诉我们: 只要函数在  $[-π, π]$  上至多有有限个第一类间断点, 并且不做无限次振动, 函数的傅里叶级数在连续点处就收敛于该点的函数值, 在间断点处收敛于该点左极限与右极限的算术平均值. 可见, 函数展开成傅里叶级数的条件比展开成幂级数的条件低得多. 记

$$
C = \left\{x \Bigg | f (x) = \frac {1}{2} [ f (x ^ {-}) + f (x ^ {+}) ] \right\},
$$

在 $C$ 上就成立 $f(x)$ 的傅里叶级数展开式

$$
f (x) = \frac {a _ {0}}{2} + \sum_ {n = 1} ^ {\infty} (a _ {n} \cos n x + b _ {n} \sin n x), \quad x \in C. \tag {7-7}
$$

例1 设 $f(x)$ 是周期为 $2\pi$ 的周期函数, 它在 $[- \pi, \pi)$ 上的表达式为

$$
f (x) = \left\{ \begin{array}{l l} - 1, & - \pi \leqslant x <   0, \\ 1, & 0 \leqslant x <   \pi . \end{array} \right.
$$

将 $f(x)$ 展开成傅里叶级数，并作出级数的和函数的图形

解 所给函数满足收敛定理的条件, 它在点  $x=k\pi$  ( $k=0,\pm1,\pm2,\cdots$ ) 处不连续, 在其他点处连续, 从而由收敛定理知道  $f(x)$  的傅里叶级数收敛, 并且当  $x=k\pi$  时级数收敛于

$$
\frac {- 1 + 1}{2} = \frac {1 + (- 1)}{2} = 0,
$$

298

---

第七节 傅里叶级数

当  $x \neq k\pi$  时级数收敛于  $f(x)$ .

计算傅里叶系数如下:

$$
\begin{array}{l} a _ {n} = \frac {1}{\pi} \int_ {- \pi} ^ {\pi} f (x) \cos n x \mathrm{d} x = \frac {1}{\pi} \int_ {- \pi} ^ {0} (- 1) \cos n x \mathrm{d} x + \frac {1}{\pi} \int_ {0} ^ {\pi} 1 \cdot \cos n x \mathrm{d} x \\ = 0 \quad (n = 0, 1, 2, \dots); \\ b _ {n} = \frac {1}{\pi} \int_ {- \pi} ^ {\pi} f (x) \sin n x \mathrm{d} x = \frac {1}{\pi} \int_ {- \pi} ^ {0} (- 1) \sin n x \mathrm{d} x + \frac {1}{\pi} \int_ {0} ^ {\pi} 1 \cdot \sin n x \mathrm{d} x \\ = \frac {1}{\pi} \left[ \frac {\cos n x}{n} \right] _ {- \pi} ^ {0} + \frac {1}{\pi} \left[ - \frac {\cos n x}{n} \right] _ {0} ^ {\pi} \\ = \frac {1}{n \pi} [ 1 - \cos n \pi - \cos n \pi + 1 ] = \frac {2}{n \pi} [ 1 - (- 1) ^ {n} ] \\ = \left\{ \begin{array}{l l} \frac {4}{n \pi}, & n = 1, 3, 5, \dots , \\ 0, & n = 2, 4, 6, \dots . \end{array} \right. \\ \end{array}
$$

将求得的系数代入(7-7)式,就得到 $f(x)$ 的傅里叶级数展开式为

$$
\begin{array}{l} f (x) = \frac {4}{\pi} \left[ \sin x + \frac {1}{3} \sin 3 x + \dots + \frac {1}{2 k - 1} \sin (2 k - 1) x + \dots \right] \\ = \frac {4}{\pi} \sum_ {k = 1} ^ {\infty} \frac {1}{2 k - 1} \sin (2 k - 1) x \quad (- \infty <   x <   + \infty ; x \neq 0, \pm \pi , \pm 2 \pi , \dots). \\ \end{array}
$$

级数的和函数的图形如图 12-9 所示:

如果把例 1 中的函数理解为矩形波的波形函数(周期  $T=2\pi$ , 振幅 E=1, 自变量 x 表示时间), 那么上面所得到的展开式表明: 矩形波是由一系列不同频率的正弦波叠加而成的, 这些正弦波的频率依次为基波频率的奇数倍.

![](../../raw/pages_0289-0320/images/page_305_chart_8.jpg)

<details>
<summary>line</summary>

| X | Y |
| --- | --- |
| \(-2\pi\) | 1 |
| \(-\pi\) | 1 |
| 0 | 1 |
| \(\pi\) | 1 |
| \(2\pi\) | 1 |
</details>

图12-9

例 2 设  $f(x)$  是周期为  $2\pi$  的周期函数, 它在  $[-\pi, \pi)$  上的表达式为

$$
f (x) = \left\{ \begin{array}{l l} x, & - \pi \leqslant x <   0, \\ 0, & 0 \leqslant x <   \pi . \end{array} \right.
$$

将 $f(x)$ 展开成傅里叶级数,并作出级数的和函数的图形.

解 所给函数满足收敛定理的条件, 它在点  $x=(2k+1)\pi$  ( $k=0,\pm1,\pm2,\cdots$ ) 处不连续. 因此,  $f(x)$  的傅里叶级数在  $x=(2k+1)\pi$  处收敛于

$$
\frac {f (\pi^ {-}) + f (- \pi^ {+})}{2} = \frac {0 - \pi}{2} = - \frac {\pi}{2}.
$$

在连续点 $x (x \neq (2k + 1)\pi)$ 处收敛于 $f(x)$.

图

释疑解难

12-5

299

---

第十二章 无穷级数

计算傅里叶系数如下:

例题精讲

12-8

$$
\begin{array}{l} a _ {n} = \frac {1}{\pi} \int_ {- \pi} ^ {\pi} f (x) \cos n x \mathrm{d} x = \frac {1}{\pi} \int_ {- \pi} ^ {0} x \cos n x \mathrm{d} x \\ = \frac {1}{\pi} \left[ \frac {x \sin n x}{n} + \frac {\cos n x}{n ^ {2}} \right] _ {- \pi} ^ {0} = \frac {1}{n ^ {2} \pi} (1 - \cos n \pi) \\ = \left\{ \begin{array}{l l} \frac {2}{n ^ {2} \pi}, & n = 1, 3, 5, \dots , \\ 0, & n = 2, 4, 6, \dots ; \end{array} \right. \\ a _ {0} = \frac {1}{\pi} \int_ {- \pi} ^ {\pi} f (x) \mathrm{d} x = \frac {1}{\pi} \int_ {- \pi} ^ {0} x \mathrm{d} x = \frac {1}{\pi} \left[ \frac {x ^ {2}}{2} \right] _ {- \pi} ^ {0} = - \frac {\pi}{2}; \\ b _ {n} = \frac {1}{\pi} \int_ {- \pi} ^ {\pi} f (x) \sin n x \mathrm{d} x = \frac {1}{\pi} \int_ {- \pi} ^ {0} x \sin n x \mathrm{d} x \\ = \frac {1}{\pi} \left[ - \frac {x \cos n x}{n} + \frac {\sin n x}{n ^ {2}} \right] _ {- \pi} ^ {0} \\ = - \frac {\cos n \pi}{n} = \frac {(- 1) ^ {n + 1}}{n} \quad (n = 1, 2, 3, \dots). \\ \end{array}
$$

将求得的系数代入(7-7)式,得到 $f(x)$ 的傅里叶级数展开式为

$$
\begin{array}{l} f (x) = - \frac {\pi}{4} + \left(\frac {2}{\pi} \cos x + \sin x\right) - \frac {1}{2} \sin 2 x + \left(\frac {2}{3 ^ {2} \pi} \cos 3 x + \frac {1}{3} \sin 3 x\right) - \\ \frac {1}{4} \sin 4 x + \left(\frac {2}{5 ^ {2} \pi} \cos 5 x + \frac {1}{5} \sin 5 x\right) - \dots \\ = - \frac {\pi}{4} + \frac {2}{\pi} \sum_ {k = 1} ^ {\infty} \frac {1}{(2 k - 1) ^ {2}} \cos (2 k - 1) x + \sum_ {n = 1} ^ {\infty} \frac {(- 1) ^ {n - 1}}{n} \sin n x \\ (- \infty <   x <   + \infty ; x \neq \pm \pi , \pm 3 \pi , \dots). \\ \end{array}
$$

级数的和函数的图形如图 12-10 所示:

![](../../raw/pages_0289-0320/images/page_306_chart_8.jpg)

<details>
<summary>line</summary>

| X-axis (x) | Y-axis (y) |
| --- | --- |
| \(-3\pi\) | 0 |
| \(-2\pi\) | 0 |
| \(-\pi\) | 0 |
| 0 | 0 |
| \(\pi/2\) | 0 |
| \(2\pi\) | 0 |
| \(3\pi\) | 0 |
</details>

图12-10

应该注意,如果函数 $f(x)$ 只在 $[-\pi,\pi]$ 上有定义,并且满足收敛定理的条件,那么 $f(x)$ 也可以展开成傅里叶级数.事实上,我们可在 $[-\pi,\pi)$ 或 $(-π,π]$ 外补充函数 $f(x)$ 的定义,使它拓广成周期为 $2π$ 的周期函数 $F(x)$.按这种方式拓广函数的定义域的过

300

---

第七节 傅里叶级数

程称为周期延拓.再将 $F(x)$ 展开成傅里叶级数.最后限制x在 $(-π,π)$ 内,此时 $F(x)≡f(x)$ ,这样便得到 $f(x)$ 的傅里叶级数展开式.根据收敛定理,这级数在区间端点 $x=±π$ 处收敛于 $\frac{f(\pi^{-})+f(-\pi^{+})}{2}$ .

例3 将函数

$$
u (t) = E \left| \sin \frac {t}{2} \right|, \quad - \pi \leqslant t \leqslant \pi
$$

展开成傅里叶级数,其中 E 是正的常数.

解 所给函数在区间 $[-π, π]$ 上满足收敛定理的条件,并且拓广为周期函数时,

它在每一点 $x$ 处都连续（图12-11），因此拓广的周期函数的傅里叶级数在 $[- \pi, \pi]$ 上收敛于 $u(t)$.

计算傅里叶系数如下:

$$
\begin{array}{l} a _ {n} = \frac {1}{\pi} \int_ {- \pi} ^ {\pi} u (t) \cos n t \mathrm{d} t \\ = \frac {E}{\pi} \int_ {- \pi} ^ {\pi} \left| \sin \frac {t}{2} \right| \cos n t \mathrm{d} t, \\ \end{array}
$$

![](../../raw/pages_0289-0320/images/page_307_chart_9.jpg)

<details>
<summary>contour</summary>

| t | u |
| --- | --- |
| \(-2\pi\) | 0 |
| \(-\pi\) | ~E |
| 0 | 0 |
| \(\pi\) | ~E |
| \(2\pi\) | 0 |
</details>

图12-11

因为上列积分中被积函数为偶函数,所以

$$
\begin{array}{l} a _ {n} = \frac {2 E}{\pi} \int_ {0} ^ {\pi} \sin \frac {t}{2} \cos n t \mathrm{d} t = \frac {E}{\pi} \int_ {0} ^ {\pi} \left[ \sin \left(n + \frac {1}{2}\right) t - \sin \left(n - \frac {1}{2}\right) t \right] \mathrm{d} t \\ = \frac {E}{\pi} \left[ - \frac {\cos \left(n + \frac {1}{2}\right) t}{n + \frac {1}{2}} + \frac {\cos \left(n - \frac {1}{2}\right) t}{n - \frac {1}{2}} \right] _ {0} ^ {\pi} \\ = \frac {E}{\pi} \left(\frac {1}{n + \frac {1}{2}} - \frac {1}{n - \frac {1}{2}}\right) = - \frac {4 E}{(4 n ^ {2} - 1) \pi} \quad (n = 0, 1, 2, \dots). \\ b _ {n} = \frac {E}{\pi} \int_ {- \pi} ^ {\pi} \left| \sin \frac {t}{2} \right| \sin n t \mathrm{d} t = 0 \quad (n = 1, 2, 3, \dots). \\ \end{array}
$$

上式等于零是因为被积函数是奇函数.

将求得的系数代入(7-7)式, 得  $u(t)$  的傅里叶级数展开式为

$$
u (t) = \frac {4 E}{\pi} \left(\frac {1}{2} - \sum_ {n = 1} ^ {\infty} \frac {1}{4 n ^ {2} - 1} \cos n t\right) \quad (- \pi \leqslant t \leqslant \pi).
$$

## 三、正弦级数和余弦级数

一般说来,一个函数的傅里叶级数既含有正弦项,又含有余弦项(见例2).但是,

301

---

第十二章 无穷级数

也有一些函数的傅里叶级数只含有正弦项(见例1)或者只含有常数项和余弦项(见例3).这是什么原因呢？实际上，这些情况是与所给函数 $f(x)$ 的奇偶性有密切关系的.对于周期为 $2\pi$ 的函数 $f(x)$，它的傅里叶系数计算公式为

$$
a _ {n} = \frac {1}{\pi} \int_ {- \pi} ^ {\pi} f (x) \cos n x \mathrm{d} x \quad (n = 0, 1, 2, \dots),
$$

$$
b _ {n} = \frac {1}{\pi} \int_ {- \pi} ^ {\pi} f (x) \sin n x \mathrm{d} x \quad (n = 1, 2, 3, \dots).
$$

由于奇函数在对称区间上的积分为零,偶函数在对称区间上的积分等于半区间上积分的2倍,因此,

当 $f(x)$ 为奇函数时, $f(x)\cos nx$ 是奇函数, $f(x)\sin nx$ 是偶函数,故

$$
\left. \begin{array}{l} a _ {n} = 0 \quad (n = 0, 1, 2, \dots), \\ b _ {n} = \frac {2}{\pi} \int_ {0} ^ {\pi} f (x) \sin n x \mathrm{d} x \quad (n = 1, 2, 3, \dots). \end{array} \right\} \tag {7-8}
$$

即知奇函数的傅里叶级数是只含有正弦项的正弦级数

$$
\sum_ {n = 1} ^ {\infty} b _ {n} \sin n x. \tag {7-9}
$$

当 $f(x)$ 为偶函数时，$f(x)\cos nx$ 是偶函数，$f(x)\sin nx$ 是奇函数，故

$$
\left. \begin{array}{l} a _ {n} = \frac {2}{\pi} \int_ {0} ^ {\pi} f (x) \cos n x \mathrm{d} x \quad (n = 0, 1, 2, \dots), \\ b _ {n} = 0 \quad (n = 1, 2, 3, \dots). \end{array} \right\} \tag {7-10}
$$

即知偶函数的傅里叶级数是只含常数项和余弦项的余弦级数

$$
\frac {a _ {0}}{2} + \sum_ {n = 1} ^ {\infty} a _ {n} \cos n x. \tag {7-11}
$$

例 4 设  $f(x)$  是周期为  $2\pi$  的周期函数, 它在  $[-\pi, \pi)$  上的表达式为  $f(x) = x$ . 将  $f(x)$  展开成傅里叶级数, 并作出级数的和函数的图形.

解 首先,所给函数满足收敛定理的条件,它在点

$$
x = (2 k + 1) \pi \quad (k = 0, \pm 1, \pm 2, \dots)
$$

处不连续,因此 $f(x)$ 的傅里叶级数在点 $x=(2k+1)\pi$ 处收敛于

$$
\frac {f (\pi^ {-}) + f (- \pi^ {+})}{2} = \frac {\pi + (- \pi)}{2} = 0,
$$

在连续点 $x (x \neq (2k + 1)\pi)$ 处收敛于 $f(x)$.

其次,若不计 $x=(2k+1)\pi(k=0,\pm1,\pm2,\cdots)$ ，则 $f(x)$ 是周期为 $2\pi$ 的奇函数.显然,此时(7-8)式仍成立.按公式(7-8)有 $a_{n}=0(n=0,1,2,\cdots)$ ，而

$$
b _ {n} = \frac {2}{\pi} \int_ {0} ^ {\pi} f (x) \sin n x \mathrm{d} x = \frac {2}{\pi} \int_ {0} ^ {\pi} x \sin n x \mathrm{d} x = \frac {2}{\pi} \left[ - \frac {x \cos n x}{n} + \frac {\sin n x}{n ^ {2}} \right] _ {0} ^ {\pi}
$$

302

---

第七节 傅里叶级数

$$
= - \frac {2}{n} \cos n \pi = \frac {2}{n} (- 1) ^ {n + 1} \quad (n = 1, 2, 3, \dots).
$$

将求得的 $b_{n}$ 代入正弦级数(7-9)，得 $f(x)$ 的傅里叶级数展开式为

$$
\begin{array}{l} f (x) = 2 \left(\sin x - \frac {1}{2} \sin 2 x + \frac {1}{3} \sin 3 x - \dots + \frac {(- 1) ^ {n + 1}}{n} \sin n x + \dots\right) \\ = 2 \sum_ {n = 1} ^ {\infty} \frac {(- 1) ^ {n + 1}}{n} \sin n x \quad (- \infty <   x <   + \infty ; x \neq \pm \pi , \pm 3 \pi , \dots). \\ \end{array}
$$

级数的和函数的图形如图 12-12 所示:

![](../../raw/pages_0289-0320/images/page_309_chart_5.jpg)

<details>
<summary>line</summary>

| Point | x-coordinate | y-coordinate |
| --- | --- | --- |
| 1 | \(-3\pi\) | \(\pi\) |
| 2 | \(-2\pi\) | \(\pi\) |
| 3 | \(-\pi\) | \(\pi\) |
| 4 | \(\pi\) | \(\pi\) |
| 5 | \(2\pi\) | \(\pi\) |
| 6 | \(3\pi\) | \(\pi\) |
</details>

图12-12

例 5 设  $f(x)$  是周期为  $2\pi$  的周期函数, 它在  $[-\pi, \pi)$  上的表达式为  $f(x) = |x|$ , 将  $f(x)$  展开成傅里叶级数.

解 所给函数满足收敛定理的条件, 它在整个数轴上连续, 因此  $f(x)$  的傅里叶级数处处收敛于  $f(x)$ .

因为 $f(x)$ 是偶函数,所以按公式(7-10),有 $b_{n}=0\quad(n=1,2,3,\cdots)$ ,而

$$
\begin{array}{l} a _ {n} = \frac {2}{\pi} \int_ {0} ^ {\pi} f (x) \cos n x \mathrm{d} x = \frac {2}{\pi} \int_ {0} ^ {\pi} x \cos n x \mathrm{d} x \\ = \frac {2}{\pi} \left[ \frac {x \sin n x}{n} + \frac {\cos n x}{n ^ {2}} \right] _ {0} ^ {\pi} = \frac {2}{\pi n ^ {2}} (\cos n \pi - 1) \\ = \left\{ \begin{array}{l l} - \frac {4}{\pi n ^ {2}}, & n = 1, 3, 5, \dots , \\ 0, & n = 2, 4, 6, \dots ; \end{array} \right. \\ a _ {0} = \frac {2}{\pi} \int_ {0} ^ {\pi} f (x) \mathrm{d} x = \frac {2}{\pi} \int_ {0} ^ {\pi} x \mathrm{d} x = \pi . \\ \end{array}
$$

将求得的系数 $a_{n}$ 代入余弦级数(7-11)，得 $f(x)$ 的傅里叶级数展开式为

$$
\begin{array}{l} f (x) = \frac {\pi}{2} - \frac {4}{\pi} \left(\cos x + \frac {1}{3 ^ {2}} \cos 3 x + \frac {1}{5 ^ {2}} \cos 5 x + \dots + \frac {1}{(2 k - 1) ^ {2}} \cos (2 k - 1) x + \dots\right) \\ = \frac {\pi}{2} - \frac {4}{\pi} \sum_ {k = 1} ^ {\infty} \frac {1}{(2 k - 1) ^ {2}} \cos (2 k - 1) x \quad (- \infty <   x <   + \infty). \\ \end{array}
$$

在实际应用(如研究某种波动问题,热的传导、扩散问题)中,有时还需要把定义

303

---

第十二章 无穷级数

在区间 $[0,\pi]$ 上的函数 $f(x)$ 展开成正弦级数或余弦级数.

根据前面讨论的结果,这类展开问题可以按如下的方法解决:设函数 $f(x)$ 定义在区间 $[0,\pi]$ 上并且满足收敛定理的条件,我们在开区间 $(-π,0)$ 内补充函数 $f(x)$ 的定义,得到定义在 $(-π,\pi]$ 上的函数 $F(x)$,使它在 $(-π,\pi)$ 上成为奇函数①(偶函数).按这种方式拓广函数定义域的过程称为奇延拓(偶延拓).然后将奇延拓(偶延拓)后的函数展开成傅里叶级数,这个级数必定是正弦级数(余弦级数).再限制x在 $(0,\pi]$ 上,此时 $F(x)\equiv f(x)$,这样便得到 $f(x)$ 的正弦级数(余弦级数)展开式.

例如将函数

$$
\varphi (x) = x \quad (0 \leqslant x \leqslant \pi)
$$

作奇延拓,再作周期延拓,便成例4中的函数,按例4的结果,有

$$
x = 2 \sum_ {n = 1} ^ {\infty} \frac {(- 1) ^ {n + 1}}{n} \sin n x \quad (0 \leqslant x <   \pi);
$$

将 $\varphi (x)$ 作偶延拓，再作周期延拓，便成例5中的函数，按例5的结果，有

$$
x = \frac {\pi}{2} - \frac {4}{\pi} \sum_ {k = 1} ^ {\infty} \frac {1}{(2 k - 1) ^ {2}} \cos (2 k - 1) x \quad (0 \leqslant x \leqslant \pi).
$$

例6 将函数

$$
f (x) = \left\{ \begin{array}{l l} \cos x, & 0 \leqslant x <   \frac {\pi}{2}, \\ 0, & \frac {\pi}{2} \leqslant x \leqslant \pi \end{array} \right.
$$

分别展开成正弦级数和余弦级数.

解 先展开成正弦级数.为此对函数 $f(x)$ 作奇延拓(图12-13).按公式(7-8)有

$$
\begin{array}{l} b _ {n} = \frac {2}{\pi} \int_ {0} ^ {\pi} f (x) \sin n x \mathrm{d} x = \frac {2}{\pi} \int_ {0} ^ {\frac {\pi}{2}} \cos x \sin n x \mathrm{d} x \\ = \frac {1}{\pi} \int_ {0} ^ {\frac {\pi}{2}} \left[ \sin (n - 1) x + \sin (n + 1) x \right] \mathrm{d} x \\ = \frac {1}{\pi} \left[ - \frac {1}{n - 1} \cos (n - 1) x - \frac {1}{n + 1} \cos (n + 1) x \right] _ {0} ^ {\frac {\pi}{2}} \\ = \frac {1}{\pi} \left(\frac {1}{n - 1} + \frac {1}{n + 1} - \frac {1}{n - 1} \cos \frac {n - 1}{2} \pi - \frac {1}{n + 1} \cos \frac {n + 1}{2} \pi\right) \\ = \frac {1}{\pi} \left(\frac {2 n}{n ^ {2} - 1} - \frac {1}{n - 1} \sin \frac {n \pi}{2} + \frac {1}{n + 1} \sin \frac {n \pi}{2}\right) \\ \end{array}
$$

![](../../raw/pages_0289-0320/images/page_310_chart_14.jpg)

<details>
<summary>contour</summary>

| Point | X | Y |
| --- | --- | --- |
| Top-left | 0 | 1 |
| Bottom-left | \(-\pi/2\) | -1 |
| Center | 0 | 0 |
| Right-pointing edge | \(\pi/2\) | 0 |
</details>

图12-13

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 补充 $f(x)$ 的定义使它在 $(-π, π)$ 上成为奇函数时，若 $f(0) ≠ 0$，则规定 $F(0) = 0$.</span></small>

304

---

第七节 傅里叶级数

$$
= \frac {2}{\pi (n ^ {2} - 1)} (n - \sin \frac {n \pi}{2}).
$$

以上计算对 n=1 不适合, $b_{1}$  需另行计算:

$$
b _ {1} = \frac {2}{\pi} \int_ {0} ^ {\pi} f (x) \sin x \mathrm{d} x = \frac {2}{\pi} \int_ {0} ^ {\frac {\pi}{2}} \cos x \sin x \mathrm{d} x = \frac {1}{\pi}.
$$

将求得的 $b_{n}$ 代入(7-9)式，得 $f(x)$ 的正弦级数展开式为

$$
f (x) = \frac {1}{\pi} [ \sin x + 2 \sum_ {n = 2} ^ {\infty} \frac {1}{n ^ {2} - 1} (n - \sin \frac {n \pi}{2}) \sin n x ] \quad (0 <   x \leqslant \pi).
$$

在端点 x=0 处级数收敛到零, 它不等于  $f(0)$ .

再展开成余弦级数.为此对函数 $f(x)$ 作偶延拓(图12-14).

按公式(7-10)有

$$
\begin{array}{l} a _ {n} = \frac {2}{\pi} \int_ {0} ^ {\pi} f (x) \cos n x \mathrm{d} x = \frac {2}{\pi} \int_ {0} ^ {\frac {\pi}{2}} \cos x \cos n x \mathrm{d} x \\ = \frac {1}{\pi} \int_ {0} ^ {\frac {\pi}{2}} \left[ \cos (n - 1) x + \cos (n + 1) x \right] \mathrm{d} x \\ = \frac {1}{\pi} \left[ \frac {1}{n - 1} \sin \frac {n - 1}{2} \pi + \frac {1}{n + 1} \sin \frac {n + 1}{2} \pi \right] \\ = \frac {2}{\pi (n ^ {2} - 1)} \sin \frac {n - 1}{2} \pi = \left\{ \begin{array}{l l} 0, & n = 2 k - 1, \\ \frac {2 (- 1) ^ {k - 1}}{\pi (4 k ^ {2} - 1)}, & n = 2 k. \end{array} \right. \\ \end{array}
$$

![](../../raw/pages_0289-0320/images/page_311_image_10.jpg)

<details>
<summary>text_image</summary>

-π
-π/2
O
1
π/2
π x
y
</details>

图12-14

以上计算对 n=1 不适合, $a_{1}$  需另行计算:

$$
a _ {1} = \frac {2}{\pi} \int_ {0} ^ {\frac {\pi}{2}} \cos^ {2} x \mathrm{d} x = \frac {1}{\pi} \int_ {0} ^ {\frac {\pi}{2}} (1 + \cos 2 x) \mathrm{d} x = \frac {1}{2}.
$$

将求得的 $a_{n}$ 代入(7-11)式, 得 $f(x)$ 的余弦级数展开式为

$$
f (x) = \frac {1}{\pi} + \frac {1}{2} \cos x + \frac {2}{\pi} \sum_ {k = 1} ^ {\infty} \frac {(- 1) ^ {k - 1}}{4 k ^ {2} - 1} \cos 2 k x \quad (0 \leqslant x \leqslant \pi).
$$

利用函数的傅里叶级数展开式,有时可得一些特殊级数的和,例如按例5的结果,有

$$
\mid x \mid = \frac {\pi}{2} - \frac {4}{\pi} \sum_ {k = 1} ^ {\infty} \frac {1}{(2 k - 1) ^ {2}} \cos (2 k - 1) x \quad (- \pi \leqslant x \leqslant \pi),
$$

在上式中令 x=0, 便得

$$
\sum_ {k = 1} ^ {\infty} \frac {1}{(2 k - 1) ^ {2}} = \frac {\pi^ {2}}{8}.
$$

设

305

---

第十二章 无穷级数

$$
\begin{array}{l} \sigma = 1 + \frac {1}{2 ^ {2}} + \frac {1}{3 ^ {2}} + \frac {1}{4 ^ {2}} + \dots + \frac {1}{n ^ {2}} + \dots , \\ \sigma_ {1} = 1 + \frac {1}{3 ^ {2}} + \frac {1}{5 ^ {2}} + \dots + \frac {1}{(2 n - 1) ^ {2}} + \dots \left(= \frac {\pi^ {2}}{8}\right), \\ \sigma_ {2} = \frac {1}{2 ^ {2}} + \frac {1}{4 ^ {2}} + \frac {1}{6 ^ {2}} + \dots + \frac {1}{(2 n) ^ {2}} + \dots , \\ \sigma_ {3} = 1 - \frac {1}{2 ^ {2}} + \frac {1}{3 ^ {2}} - \frac {1}{4 ^ {2}} + \dots + (- 1) ^ {n - 1} \frac {1}{n ^ {2}} + \dots . \\ \end{array}
$$

因为

$$
\sigma_ {2} = \frac {\sigma}{4} = \frac {\sigma_ {1} + \sigma_ {2}}{4},
$$

所以

$$
\sigma_ {2} = \frac {\sigma_ {1}}{3} = \frac {\pi^ {2}}{2 4}, \quad \sigma = \sigma_ {1} + \sigma_ {2} = \frac {\pi^ {2}}{8} + \frac {\pi^ {2}}{2 4} = \frac {\pi^ {2}}{6},
$$

又

$$
\sigma_ {3} = 2 \sigma_ {1} - \sigma = \frac {\pi^ {2}}{4} - \frac {\pi^ {2}}{6} = \frac {\pi^ {2}}{1 2}.
$$

## 习题12-7

1. 下列周期函数 $f(x)$ 的周期为 $2\pi$，试将 $f(x)$ 展开成傅里叶级数，如果 $f(x)$ 在 $[-\pi, \pi)$ 上的表达式为

(1)  $f(x)=3x^{2}+1$  ( $-\pi\leqslant x<\pi$ );
(2) $f(x) = \mathrm{e}^{2x} (-\pi \leqslant x < \pi)$;
(3) $f(x)=\left\{\begin{aligned}&bx, & -\pi \leqslant x<0,\\ &ax, & 0 \leqslant x<\pi\quad(a,b\text{为常数，且}a>b>0).\end{aligned}\right.$

2. 将下列函数 $f(x)$ 展开成傅里叶级数:

(1) $f(x)=2\sin\frac{x}{3}\quad(-\pi\leqslant x\leqslant\pi)$;
(2) $f(x)=\left\{\begin{aligned}e^{x},&-\pi\leqslant x<0,\\ 1,&0\leqslant x\leqslant\pi;\end{aligned}\right.$
(3) $f(x) = x \sin x \quad (-\pi \leqslant x \leqslant \pi)$.

3. 将函数 $f(x) = \cos \frac{x}{2} (-\pi \leqslant x \leqslant \pi)$ 展开成傅里叶级数.

4. 设 $f(x)$ 是周期为 $2\pi$ 的周期函数, 它在 $[-\pi, \pi)$ 上的表达式为

$$
f (x) = \left\{ \begin{array}{l l} - \frac {\pi}{2}, & - \pi \leqslant x <   - \frac {\pi}{2}, \\ x, & - \frac {\pi}{2} \leqslant x <   \frac {\pi}{2}, \\ \frac {\pi}{2}, & \frac {\pi}{2} \leqslant x <   \pi , \end{array} \right.
$$

306

---

第八节 一般周期函数的傅里叶级数

将 $f(x)$ 展开成傅里叶级数.

5. 将函数 $f(x) = \frac{\pi - x}{2} (0 \leqslant x \leqslant \pi)$ 展开成正弦级数.
6. 将函数 $f(x) = 2x^{2} (0 \leqslant x \leqslant \pi)$ 分别展开成正弦级数和余弦级数.
7. 设周期函数  $f(x)$  的周期为  $2\pi$ . 证明:

(1) 若  $f(x-\pi)=-f(x)$ ，则  $f(x)$  的傅里叶系数  $a_{0}=0, a_{2k}=0, b_{2k}=0 \quad (k=1,2,\cdots)$ ;

(2) 若  $f(x-\pi)=f(x)$ ，则  $f(x)$  的傅里叶系数  $a_{2k+1}=0, b_{2k+1}=0$  ( $k=0,1,2,\cdots$ ).

## 第八节 一般周期函数的傅里叶级数

## 一、周期为 $2l$ 的周期函数的傅里叶级数

上节所讨论的周期函数都是以 $2\pi$ 为周期的,但是实际问题中所遇到的周期函数,它的周期不一定是 $2\pi$.例如上节中提到的矩形波,它的周期是 $T = \frac{2\pi}{\omega}$.因此,本节我们讨论周期为 $2l$ 的周期函数的傅里叶级数.根据上节讨论的结果,经过自变量的变量代换,可得下面的定理:

定理 设周期为 $2l$ 的周期函数 $f(x)$ 满足收敛定理的条件, 则它的傅里叶级数展开式为

$$
f (x) = \frac {a _ {0}}{2} + \sum_ {n = 1} ^ {\infty} \left(a _ {n} \cos \frac {n \pi x}{l} + b _ {n} \sin \frac {n \pi x}{l}\right) \quad (x \in C), \tag {8-1}
$$

其中

$$
\begin{array}{l} \left. \begin{array}{l} a _ {n} = \frac {1}{l} \int_ {- l} ^ {l} f (x) \cos \frac {n \pi x}{l} \mathrm{d} x \quad (n = 0, 1, 2, \dots), \\ b _ {n} = \frac {1}{l} \int_ {- l} ^ {l} f (x) \sin \frac {n \pi x}{l} \mathrm{d} x \quad (n = 1, 2, 3, \dots), \end{array} \right\} \tag {8-2} \\ C = \left\{x   \Big |   f (  x  ) = \frac {1}{2} [ f (  x ^ {-}  ) + f (  x ^ {+}  )   ] \right\}. \\ \end{array}
$$

当 $f(x)$ 为奇函数时，

$$
f (x) = \sum_ {n = 1} ^ {\infty} b _ {n} \sin \frac {n \pi x}{l} \quad (x \in C), \tag {8-3}
$$

其中

$$
b _ {n} = \frac {2}{l} \int_ {0} ^ {l} f (x) \sin \frac {n \pi x}{l} \mathrm{d} x \quad (n = 1, 2, 3, \dots). \tag {8-4}
$$

当 $f(x)$ 为偶函数时，

307

---

第十二章 无穷级数

$$
f (x) = \frac {a _ {0}}{2} + \sum_ {n = 1} ^ {\infty} a _ {n} \cos \frac {n \pi x}{l} \quad (x \in C), \tag {8-5}
$$

其中

$$
a _ {n} = \frac {2}{l} \int_ {0} ^ {l} f (x) \cos \frac {n \pi x}{l} \mathrm{d} x \quad (n = 0, 1, 2, \dots). \tag {8-6}
$$

证 作变量代换 $z = \frac{\pi x}{l}$, 于是区间 $-l \leqslant x \leqslant l$ 就变换成 $-\pi \leqslant z \leqslant \pi$. 设函数 $f(x) = f\left(\frac{lz}{\pi}\right) = F(z)$, 从而 $F(z)$ 是周期为 $2\pi$ 的周期函数, 并且它满足收敛定理的条件, 将 $F(z)$ 展开成傅里叶级数

$$
F (z) = \frac {a _ {0}}{2} + \sum_ {n = 1} ^ {\infty} \left(a _ {n} \cos n z + b _ {n} \sin n z\right),
$$

其中

$$
a _ {n} = \frac {1}{\pi} \int_ {- \pi} ^ {\pi} F (z) \cos n z \mathrm{d} z, \quad b _ {n} = \frac {1}{\pi} \int_ {- \pi} ^ {\pi} F (z) \sin n z \mathrm{d} z.
$$

在以上式子中令 $z = \frac{\pi x}{l}$，并注意到 $F(z) = f(x)$，于是有

$$
f (x) = \frac {a _ {0}}{2} + \sum_ {n = 1} ^ {\infty} \left(a _ {n} \cos \frac {n \pi x}{l} + b _ {n} \sin \frac {n \pi x}{l}\right),
$$

而且

$$
a _ {n} = \frac {1}{l} \int_ {- l} ^ {l} f (x) \cos \frac {n \pi x}{l} \mathrm{d} x, \quad b _ {n} = \frac {1}{l} \int_ {- l} ^ {l} f (x) \sin \frac {n \pi x}{l} \mathrm{d} x.
$$

类似地,可以证明定理的其余部分.

例1 设 $f(x)$ 是周期为4的周期函数, 它在[-2,2)上的表达式为

$$
f (x) = \left\{ \begin{array}{l l} 0, & - 2 \leqslant x <   0, \\ h, & 0 \leqslant x <   2 \end{array} \right. \quad (\text {常数} h \neq 0).
$$

将 $f(x)$ 展开成傅里叶级数,并作出级数的和函数的图形.

解 这时 $l = 2$ ，按公式(8-2)有

$$
\begin{array}{l} a _ {n} = \frac {1}{2} \int_ {0} ^ {2} h \cos \frac {n \pi x}{2} \mathrm{d} x = \left[ \frac {h}{n \pi} \sin \frac {n \pi x}{2} \right] _ {0} ^ {2} = 0 \quad (n \neq 0); \\ a _ {0} = \frac {1}{2} \int_ {- 2} ^ {0} 0 \mathrm{d} x + \frac {1}{2} \int_ {0} ^ {2} h \mathrm{d} x = h; \\ b _ {n} = \frac {1}{2} \int_ {0} ^ {2} h \sin \frac {n \pi x}{2} \mathrm{d} x = \left[ - \frac {h}{n \pi} \cos \frac {n \pi x}{2} \right] _ {0} ^ {2} \\ \end{array}
$$

308

---

第八节 一般周期函数的傅里叶级数

$$
= \frac {h}{n \pi} (1 - \cos n \pi) = \left\{ \begin{array}{l l} \frac {2 h}{n \pi}, & n = 1, 3, 5, \dots , \\ 0, & n = 2, 4, 6, \dots . \end{array} \right.
$$

将求得的系数 $a_{n}, b_{n}$ 代入(8-1)式, 得

$$
\begin{array}{l} f (x) = \frac {h}{2} + \frac {2 h}{\pi} \left(\sin \frac {\pi x}{2} + \frac {1}{3} \sin \frac {3 \pi x}{2} + \frac {1}{5} \sin \frac {5 \pi x}{2} + \dots + \frac {1}{2 n - 1} \sin \frac {(2 n - 1) \pi x}{2} + \dots\right) \\ (- \infty <   x <   + \infty ; x \neq 0, \pm 2, \pm 4, \dots) \\ \end{array}
$$

级数的和函数的图形如图 12-15 所示.

例2 将如图12-16所示的函数

$$
M (x) = \left\{ \begin{array}{l l} \frac {p x}{2}, & 0 \leqslant x <   \frac {l}{2}, \\ \frac {p (l - x)}{2}, & \frac {l}{2} \leqslant x \leqslant l \end{array} \right.
$$

分别展开成正弦级数和余弦级数.

![](../../raw/pages_0289-0320/images/page_315_chart_8.jpg)

<details>
<summary>line</summary>

| X | Y |
| --- | --- |
| -2 | 1 |
| -2 | 0 |
| 0 | 0 |
| 0 | 1 |
| 2 | 1 |
| 2 | 0 |
| 2 | 0 |
</details>

图12-15

![](../../raw/pages_0289-0320/images/page_315_chart_10.jpg)

<details>
<summary>line</summary>

| X | Y |
| --- | --- |
| 0 | 0 |
| l/2 | pl/4 |
| l | 0 |
</details>

图12-16

解 $M(x)$ 是定义在 $[0, l]$ 上的函数, 要将它展开成正弦级数, 必须对 $M(x)$ 进行奇延拓. 按公式(8-4)计算延拓后的函数的傅里叶系数

$$
\begin{array}{l} b _ {n} = \frac {2}{l} \int_ {0} ^ {l} M (x) \sin \frac {n \pi x}{l} \mathrm{d} x \\ = \frac {2}{l} \left[ \int_ {0} ^ {\frac {l}{2}} \frac {p x}{2} \sin \frac {n \pi x}{l} \mathrm{d} x + \int_ {\frac {l}{2}} ^ {l} \frac {p (l - x)}{2} \sin \frac {n \pi x}{l} \mathrm{d} x \right]. \\ \end{array}
$$

对上式右端的第二项,令 t=l-x,则

$$
\begin{array}{l} b _ {n} = \frac {p}{l} \left[ \int_ {0} ^ {\frac {l}{2}} x \sin \frac {n \pi x}{l} \mathrm{d} x + \int_ {\frac {l}{2}} ^ {0} t \sin \frac {n \pi (l - t)}{l} (- \mathrm{d} t) \right] \\ = \frac {p}{l} \left[ \int_ {0} ^ {\frac {l}{2}} x \sin \frac {n \pi x}{l} \mathrm{d} x + (- 1) ^ {n + 1} \int_ {0} ^ {\frac {l}{2}} t \sin \frac {n \pi t}{l} \mathrm{d} t \right]. \\ \end{array}
$$

当 $n = 2k$ 为偶数时，$b_{2k} = 0$；当 $n = 2k - 1$ 为奇数时，

$$
b _ {2 k - 1} = \frac {2 p}{l} \int_ {0} ^ {\frac {l}{2}} x \sin \frac {(2 k - 1) \pi x}{l} \mathrm{d} x = \frac {2 p l}{(2 k - 1) ^ {2} \pi^ {2}} \sin \frac {2 k - 1}{2} \pi .
$$

309

---

第十二章 无穷级数

$$
= \frac {2 p l (- 1) ^ {k - 1}}{(2 k - 1) ^ {2} \pi^ {2}}.
$$

将求得的 $b_{n}$ 代入(8-3)式, 得 $M(x)$ 的正弦级数展开式为

$$
M (x) = \frac {2 p l}{\pi^ {2}} \sum_ {k = 1} ^ {\infty} \frac {(- 1) ^ {k - 1}}{(2 k - 1) ^ {2}} \sin \frac {(2 k - 1) \pi x}{l} \quad (0 \leqslant x \leqslant l).
$$

再求 $M(x)$ 的余弦级数展开式. 为此对 $M(x)$ 作偶延拓, 再作周期延拓. 注意到延拓所得周期函数的周期为 $l$, 知 $M(x)$ 可展开成周期为 $l$ 的余弦级数. 按公式 (8-6) 将 (8-6) 中的 $l$ 换成 $\frac{l}{2}$ 计算傅里叶系数:

$$
\begin{array}{l} a _ {n} = \frac {4}{l} \int_ {0} ^ {\frac {l}{2}} M (x) \cos \frac {2 n \pi x}{l} \mathrm{d} x = \frac {4}{l} \int_ {0} ^ {\frac {l}{2}} \frac {p x}{2} \cos \frac {2 n \pi x}{l} \mathrm{d} x \\ = \frac {2 p}{l} \left[ \frac {l}{2 n \pi} x \sin \frac {2 n \pi x}{l} + \left(\frac {l}{2 n \pi}\right) ^ {2} \cos \frac {2 n \pi x}{l} \right] _ {0} ^ {\frac {l}{2}} \\ = \frac {p l}{2 n ^ {2} \pi^ {2}} (\cos n \pi - 1) = \left\{ \begin{array}{l l} - \frac {p l}{n ^ {2} \pi^ {2}}, & n = 1, 3, 5, \dots , \\ 0, & n = 2, 4, 6, \dots . \end{array} \right. \\ a _ {0} = \frac {4}{l} \int_ {0} ^ {\frac {l}{2}} \frac {p x}{2} \mathrm{d} x = \frac {p l}{4}. \\ \end{array}
$$

将求得的 $a_{n}$ 代入(8-5)式，得

$$
M (x) = \frac {p l}{8} - \frac {p l}{\pi^ {2}} \sum_ {k = 1} ^ {\infty} \frac {1}{(2 k - 1) ^ {2}} \cos \frac {2 (2 k - 1) \pi x}{l} \quad (0 \leqslant x \leqslant l).
$$

## \*二、傅里叶级数的复数形式

傅里叶级数还可以用复数形式表示.在电子技术中,经常应用这种形式.

设周期为 $2l$ 的周期函数 $f(x)$ 的傅里叶级数为

$$
\frac {a _ {0}}{2} + \sum_ {n = 1} ^ {\infty} \left(a _ {n} \cos \frac {n \pi x}{l} + b _ {n} \sin \frac {n \pi x}{l}\right), \tag {8-7}
$$

其中系数 $a_{n}$ 与 $b_{n}$ 为

$$
\left. \begin{array}{l} a _ {n} = \frac {1}{l} \int_ {- l} ^ {l} f (x) \cos \frac {n \pi x}{l} \mathrm{d} x \quad (n = 0, 1, 2, \dots), \\ b _ {n} = \frac {1}{l} \int_ {- l} ^ {l} f (x) \sin \frac {n \pi x}{l} \mathrm{d} x \quad (n = 1, 2, 3, \dots). \end{array} \right\} \tag {8-8}
$$

利用欧拉公式

$$
\cos t = \frac {\mathrm{e} ^ {t i} + \mathrm{e} ^ {- t i}}{2}, \quad \sin t = \frac {\mathrm{e} ^ {t i} - \mathrm{e} ^ {- t i}}{2 \mathrm{i}},
$$

310

---

第八节 一般周期函数的傅里叶级数

把(8-7)式化为

$$
\begin{array}{l} \frac {a _ {0}}{2} + \sum_ {n = 1} ^ {\infty} \left[ \frac {a _ {n}}{2} \left(\mathrm{e} ^ {\frac {n \pi x}{l} \mathrm{i}} + \mathrm{e} ^ {- \frac {n \pi x}{l} \mathrm{i}}\right) - \frac {b _ {n} \mathrm{i}}{2} \left(\mathrm{e} ^ {\frac {n \pi x}{l} \mathrm{i}} - \mathrm{e} ^ {- \frac {n \pi x}{l} \mathrm{i}}\right) \right] \\ = \frac {a _ {0}}{2} + \sum_ {n = 1} ^ {\infty} \left[ \frac {a _ {n} - b _ {n} \mathrm{i}}{2} \mathrm{e} ^ {\frac {n \pi x}{l} \mathrm{i}} + \frac {a _ {n} + b _ {n} \mathrm{i}}{2} \mathrm{e} ^ {- \frac {n \pi x}{l} \mathrm{i}} \right]. \tag {8-9} \\ \end{array}
$$

记

$$
\frac {a _ {0}}{2} = c _ {0}, \quad \frac {a _ {n} - b _ {n} \mathrm{i}}{2} = c _ {n}, \quad \frac {a _ {n} + b _ {n} \mathrm{i}}{2} = c _ {- n} \quad (n = 1, 2, 3, \dots), \tag {8-10}
$$

则(8-9)式就表示为

$$
c _ {0} + \sum_ {n = 1} ^ {\infty} (c _ {n} \mathrm{e} ^ {\frac {n \pi x}{l} \mathrm{i}} + c _ {- n} \mathrm{e} ^ {- \frac {n \pi x}{l} \mathrm{i}}) = (c _ {n} \mathrm{e} ^ {\frac {n \pi x}{l} \mathrm{i}}) _ {n = 0} + \sum_ {n = 1} ^ {\infty} (c _ {n} \mathrm{e} ^ {\frac {n \pi x}{l} \mathrm{i}} + c _ {- n} \mathrm{e} ^ {- \frac {n \pi x}{l} \mathrm{i}}).
$$

即得傅里叶级数的复数形式为

$$
\sum_ {n = - \infty} ^ {\infty} c _ {n} \mathrm{e} ^ {\frac {n \pi x}{l} \mathrm{i}}. \tag {8-11}
$$

为得出系数 $c_{n}$ 的表达式，把(8-8)式代入(8-10)式，得

$$
\begin{array}{l} c _ {0} = \frac {a _ {0}}{2} = \frac {1}{2 l} \int_ {- l} ^ {l} f (x) \mathrm{d} x; \\ c _ {n} = \frac {a _ {n} - b _ {n} \mathrm{i}}{2} = \frac {1}{2} \left[ \frac {1}{l} \int_ {- l} ^ {l} f (x) \cos \frac {n \pi x}{l} \mathrm{d} x - \frac {\mathrm{i}}{l} \int_ {- l} ^ {l} f (x) \sin \frac {n \pi x}{l} \mathrm{d} x \right] \\ = \frac {1}{2 l} \int_ {- l} ^ {l} f (x) \left(\cos \frac {n \pi x}{l} - \mathrm{i} \sin \frac {n \pi x}{l}\right) \mathrm{d} x \\ = \frac {1}{2 l} \int_ {- l} ^ {l} f (x) \mathrm{e} ^ {- \frac {n \pi x}{l} \mathrm{i}} \mathrm{d} x \quad (n = 1, 2, 3, \dots); \\ \end{array}
$$

$$
c _ {- n} = \frac {a _ {n} + b _ {n} \mathrm{i}}{2} = \frac {1}{2 l} \int_ {- l} ^ {l} f (x) \mathrm{e} ^ {\frac {n \pi x}{l} \mathrm{i}} \mathrm{d} x \quad (n = 1, 2, 3, \dots).
$$

将已得的结果合并写为

$$
c _ {n} = \frac {1}{2 l} \int_ {- l} ^ {l} f (x) \mathrm{e} ^ {- \frac {n \pi x}{l} \mathrm{i}} \mathrm{d} x \quad (n = 0, \pm 1, \pm 2, \dots). \tag {8-12}
$$

这就是傅里叶系数的复数形式.

傅里叶级数的两种形式本质上是一样的,但复数形式比较简洁,且只用一个算式计算系数.

例 3 把宽为  $\tau$ 、高为 h、周期为 T 的矩形波(图 12-17)展开成复数形式的傅里叶级数.

![](../../raw/pages_0289-0320/images/page_317_chart_17.jpg)

<details>
<summary>line</summary>

| Time (t) | Value (u) |
| --- | --- |
| 0 | 0 |
| ~0.15 | h |
| ~0.35 | h |
| ~0.45 | 0 |
| \(-T/2\) | 0 |
| \(-\tau/2\) | 0 |
| \(+\tau/2\) | h |
| \(\tau/2\) | h |
| \(T/2\) | 0 |
| ~\(T/3\) | h |
| ~\(T/4\) | h |
</details>

图12-17

311

---

第十二章 无穷级数

解 在一个周期 $\left[-\frac{T}{2}, \frac{T}{2}\right)$ 内矩形波的函数表达式为

$$
u (t) = \left\{ \begin{array}{l l} 0, & - \frac {T}{2} \leqslant t <   - \frac {\tau}{2}, \\ h, & - \frac {\tau}{2} \leqslant t <   \frac {\tau}{2}, \\ 0, & \frac {\tau}{2} \leqslant t <   \frac {T}{2}. \end{array} \right.
$$

按公式(8-12)有

$$
\begin{array}{l} c _ {n} = \frac {1}{T} \int_ {- T / 2} ^ {T / 2} u (t) \mathrm{e} ^ {- \frac {2 n \pi t}{T} \mathrm{i}} \mathrm{d} t = \frac {1}{T} \int_ {- \tau / 2} ^ {\tau / 2} h \mathrm{e} ^ {- \frac {2 n \pi t}{T} \mathrm{i}} \mathrm{d} t \\ = \frac {h}{T} \left[ \frac {- T}{2 n \pi \mathrm{i}} \mathrm{e} ^ {- \frac {2 n \pi t}{T} \mathrm{i}} \right] _ {- \tau / 2} ^ {\tau / 2} = \frac {h}{n \pi} \sin \frac {n \pi \tau}{T} \quad (n = \pm 1, \pm 2, \dots), \\ c _ {0} = \frac {1}{T} \int_ {- T / 2} ^ {T / 2} u (t) \mathrm{d} t = \frac {1}{T} \int_ {- \tau / 2} ^ {\tau / 2} h \mathrm{d} t = \frac {h \tau}{T}, \\ \end{array}
$$

将求得的 $c_{n}$ 代入级数(8-11)，得

$$
u(t) = \frac{h\tau}{T} +\frac{h}{\pi}\sum_{\substack{n = -\infty \\ n\neq 0}}^{\infty}\frac{1}{n}\sin \frac{n\pi\tau}{T}\mathrm{e}^{\frac{2n\pi t}{T} \mathrm{i}}\quad \left(-\infty <  t <   + \infty ;t\neq nT\pm \frac{\tau}{2},n = 0,\pm 1, \pm 2,\dots\right).
$$

## 习题12-8

1. 将下列各周期函数展开成傅里叶级数(下面给出函数在一个周期内的表达式):

(1) $f(x) = 1 - x^2 \left( -\frac{1}{2} \leqslant x < \frac{1}{2} \right)$;

(2) $f(x)=\begin{cases}x,&-1\leqslant x<0,\\1,&0\leqslant x<\frac{1}{2},\\-1&\frac{1}{2}\leqslant x<1;\end{cases}$

(3) $f(x)=\begin{cases}2x+1,&-3\leqslant x<0,\\1,&0\leqslant x<3.\end{cases}$

2. 将下列函数分别展开成正弦级数和余弦级数:

(1) $f(x)=\left\{\begin{aligned}x,&0\leqslant x<\frac{l}{2},\\ l-x,&\frac{l}{2}\leqslant x\leqslant l;\end{aligned}\right.$

(2) $f(x) = x^{2}$ $(0\leqslant x\leqslant 2)$

\*3. 设 $f(x)$ 是周期为 2 的周期函数, 它在 $[-1, 1)$ 上的表达式为 $f(x) = \mathrm{e}^{-x}$. 试将 $f(x)$ 展开成复数形式的傅里叶级数.

\* 4. 设 $u\left( t\right)$ 是周期为 $T$ 的周期函数. 已知它的傅里叶级数的复数形式为 (参阅本节例题)

312

---

总习题十二

$$
u(t) = \frac{h\tau}{T} +\frac{h}{\pi}\sum_{\substack{n = -\infty \\ n\neq 0}}^{\infty}\frac{1}{n}\sin \frac{n\pi\tau}{T}\mathrm{e}^{\frac{2n\pi t}{T}\mathrm{i}}\quad (-\infty <  t <   + \infty),
$$

试写出 $u(t)$ 的傅里叶级数的实数形式（即三角形式）.

## 总习题十二

1. 填空:

（1）对级数 $\sum_{n=1}^{\infty} u_n, \lim_{n \to \infty} u_n = 0$ 是它收敛的 \_\_\_\_ 条件，不是它收敛的 \_\_\_\_ 条件；
(2) 部分和数列  $\{s_{n}\}$  有界是正项级数  $\sum_{n=1}^{\infty} u_{n}$  收敛的 \_\_\_\_ 条件；
(3) 若级数  $\sum_{n=1}^{\infty}u_{n}$  绝对收敛, 则级数  $\sum_{n=1}^{\infty}u_{n}$  必定 \_\_\_\_; 若级数  $\sum_{n=1}^{\infty}u_{n}$  条件收敛, 则级数  $\sum_{n=1}^{\infty}|u_{n}|$  必定 \_\_\_\_.

2. 下题中给出了四个结论,从中选出一个正确的结论:

设 $f(x)$ 是以 $2\pi$ 为周期的周期函数，它在 $[- \pi, \pi)$ 上的表达式为 $|x|$，则 $f(x)$ 的傅里叶级数为（）.

(A) $\frac{\pi}{2} - \frac{4}{\pi} \left[ \cos x + \frac{1}{3^2} \cos 3x + \frac{1}{5^2} \cos 5x + \cdots + \frac{1}{(2n-1)^2} \cos (2n-1)x + \cdots \right]$
(B)  $\frac{2}{\pi}\left[\frac{1}{2^{2}}\sin 2x+\frac{1}{4^{2}}\sin 4x+\frac{1}{6^{2}}\sin 6x+\cdots+\frac{1}{(2n)^{2}}\sin 2nx+\cdots\right]$
(C)  $\frac{4}{\pi}\left[\cos x+\frac{1}{3^{2}}\cos 3x+\frac{1}{5^{2}}\cos 5x+\cdots+\frac{1}{(2n-1)^{2}}\cos(2n-1)x+\cdots\right]$
(D)  $\frac{1}{\pi}\left[\frac{1}{2^{2}}\cos2x+\frac{1}{4^{2}}\cos4x+\frac{1}{6^{2}}\cos6x+\cdots+\frac{1}{(2n)^{2}}\cos2nx+\cdots\right]$

3. 判定下列级数的收敛性:

(1)  $\sum_{n=1}^{\infty}\frac{1}{n\sqrt[n]{n}};$
(2) $\sum_{n=1}^{\infty}\frac{(n!)^{2}}{2n^{2}};$
(3) $\sum_{n=1}^{\infty} \frac{n \cos^{2} \frac{n\pi}{3}}{2^{n}};$
(4)  $\sum_{n=2}^{\infty}\frac{1}{\ln^{10}n};$
(5) $\sum_{n=1}^{\infty} \frac{a^n}{n^s} \quad (a > 0, s > 0)$.

4. 设正项级数 $\sum_{n=1}^{\infty} u_n$ 和 $\sum_{n=1}^{\infty} v_n$ 都收敛, 证明级数 $\sum_{n=1}^{\infty} (u_n + v_n)^2$ 也收敛.

5. 设级数 $\sum_{n=1}^{\infty} u_n$ 收敛, 且 $\lim_{n \to \infty} \frac{v_n}{u_n} = 1$. 问级数 $\sum_{n=1}^{\infty} v_n$ 是否也收敛? 试说明理由.

6. 讨论下列级数的绝对收敛性与条件收敛性:

(1) $\sum_{n=1}^{\infty}(-1)^{n}\frac{1}{n^{p}}$;

(2) $\sum_{n=1}^{\infty}(-1)^{n+1}\frac{\sin\frac{\pi}{n+1}}{\pi^{n+1}};$

313

---

第十二章 无穷级数

(3) $\sum_{n=1}^{\infty}(-1)^{n}\ln \frac{n+1}{n}$;

(4) $\sum_{n=1}^{\infty}(-1)^{n} \frac{(n+1)!}{n^{n+1}}$.

7. 求下列极限:

(1) $\lim_{n\to \infty}\frac{1}{n}\sum_{k = 1}^{n}\frac{1}{3^k}\left(1 + \frac{1}{k}\right)^{k^2};$

(2) $\lim_{n\to \infty}\left[2^{\frac{1}{3}}\times 4^{\frac{1}{9}}\times 8^{\frac{1}{27}}\times \dots \times (2^n)^{\frac{1}{3^n}}\right].$

8. 求下列幂级数的收敛区间:

(1) $\sum_{n=1}^{\infty} \frac{3^n + 5^n}{n} x^n$;

(2) $\sum_{n=1}^{\infty}\left(1 + \frac{1}{n}\right)^{n^2}x^n;$

(3) $\sum_{n=1}^{\infty} n(x+1)^{n}$;

(4) $\sum_{n=1}^{\infty} \frac{n}{2^n} x^{2n}$.

9. 求下列幂级数的和函数:

(1) $\sum_{n=1}^{\infty} \frac{2n-1}{2^n} x^{2(n-1)}$;

\* (2) $\sum_{n=1}^{\infty} \frac{(-1)^{n-1}}{2n-1} x^{2n-1}$;

(3)  $\sum_{n=1}^{\infty}n(x-1)^{n};$

\* (4) $\sum_{n=1}^{\infty} \frac{x^n}{n(n+1)}$.

10. 设幂级数 $\sum_{n=1}^{\infty} a_n x^n$ 的系数 $a_1 = 1, a_2 = 0$, 且满足 $a_n = \frac{-1}{(n-1)(n-2)} a_{n-2} (n \geqslant 3, n \in \mathbb{N})$. 试求该幂级数的收敛域与和函数 $f(x)$.

11. 求下列数项级数的和:

(1) $\sum_{n=1}^{\infty} \frac{n^{2}}{n!}$;

(2) $\sum_{n=0}^{\infty}(-1)^{n} \frac{n+1}{(2n+1)!}$.

12. 将下列函数展开成 $x$ 的幂级数:

(1)  $\ln(x+\sqrt{x^{2}+1})$ ;

(2) $\frac{1}{(2 - x)^2}$.

13. 设 $f(x)$ 是周期为 $2\pi$ 的函数, 它在 $[-\pi, \pi)$ 上的表达式为

$$
f (x) = \left\{ \begin{array}{l l} 0, & x \in [ - \pi , 0), \\ \mathrm{e} ^ {x}, & x \in [ 0, \pi). \end{array} \right.
$$

将 $f(x)$ 展开成傅里叶级数.

14. 将函数

$$
f (x) = \left\{ \begin{array}{l l} 1, & 0 \leqslant x \leqslant h, \\ 0, & h <   x \leqslant \pi \end{array} \right.
$$

分别展开成正弦级数和余弦级数.

![](../../raw/pages_0321-0352/images/page_320_image_29.jpg)

第十二章释疑解难

![](../../raw/pages_0321-0352/images/page_320_image_31.jpg)

第十二章例题精讲

314
