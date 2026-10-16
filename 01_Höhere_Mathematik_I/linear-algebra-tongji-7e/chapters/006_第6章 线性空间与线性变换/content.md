# 第6章 线性空间与线性变换

原始 PDF 第 146–163 页。

The quick brown fox jumps over the lazy dog.

## \* 第6章

## 线性空间与线性变换

向量空间又称线性空间,是线性代数中一个最基本的概念.在第4章中,我们把有序数组叫做向量,并介绍过向量空间的概念.在这一章中,我们要把这些概念推广,使向量及向量空间的概念更具一般性.当然,推广后的向量概念也就更加抽象化了.

## § 1 线性空间的定义与性质

定义1 设 $V$ 是一个非空集合, $\mathbb{R}$ 为实数域. 如果在 $V$ 中定义了一个加法, 即对于任意两个元素 $\alpha, \beta \in V$, 总有惟一的一个元素 $\gamma \in V$ 与之对应, 称为 $\alpha$ 与 $\beta$ 的和, 记作 $\gamma = \alpha + \beta$; 在 $V$ 中又定义了一个数与元素的乘法 (简称数乘), 即对于任一数 $\lambda \in \mathbb{R}$ 与任一元素 $\alpha \in V$, 总有惟一的一个元素 $\delta \in V$ 与之对应, 称为 $\lambda$ 与 $\alpha$ 的数量乘积, 记作 $\delta = \lambda \alpha$, 并且这两种运算满足以下八条运算规律 (设 $\alpha, \beta, \gamma \in V, \lambda, \mu \in \mathbb{R}$):

(i)  $\alpha+\beta=\beta+\alpha;$
(ii)  $(\alpha+\beta)+\gamma=\alpha+(\beta+\gamma)$ ;
(iii) 在 V 中存在零元素0, 对任何  $\alpha \in V$ , 都有  $\alpha + 0 = \alpha$ ;
(iv) 对任何  $\alpha \in V$ ，都有  $\alpha$  的负元素  $\beta \in V$ ，使  $\alpha + \beta = 0$ ;
(v)  $1\alpha=\alpha;$
(vi)  $\lambda(\mu\alpha)=(\lambda\mu)\alpha;$
(vii)  $(\lambda + \mu)\alpha = \lambda\alpha + \mu\alpha;$
(viii)  $\lambda(\boldsymbol{\alpha}+\boldsymbol{\beta})=\lambda\boldsymbol{\alpha}+\lambda\boldsymbol{\beta}$ ,

那么, $V$ 就称为(实数域 $\mathbb{R}$ 上的)线性空间(或向量空间), 借助几何语言, $V$ 中的元素不论其本来的性质如何, 可统称为向量.

简言之,凡满足上述八条规律的加法及数乘运算,就称为线性运算;凡定义了线性运算的集合,就称向量空间,其中的元素就称为向量.

142

---

§1 线性空间的定义与性质

这八条规律中,规律(i)与(ii)是我们熟知的加法的交换律和结合律,而规律(iii)和(iv)则保证了加法有逆运算,即

$$
\text {若} \alpha + \beta = \gamma , \beta \text {的负元素为} \delta , \text {则} \gamma + \delta = \alpha ;
$$

规律(vi)、(vii)、(viii)是数乘的结合律和分配律,而规律(v)则保证了非零数乘有逆运算,即

$$
\text {当} \lambda \neq 0 \text {时,若} \lambda \alpha = \beta , \text {则} \frac {1}{\lambda} \beta = \alpha .
$$

在第 4 章中, 我们把有序数组称为向量, 并对它定义了加法和数乘运算, 容易验证这些运算满足上述八条规律. 最后, 把对于运算为封闭的有序数组的集合称为向量空间. 显然, 那些只是现在定义的特殊情形. 比较起来, 现在的定义有了很大的推广:

1. 向量不一定是有序数组；

2. 向量空间中的运算只要求满足上述八条运算规律,当然也就不一定是有序数组的加法及数乘运算.

下面举一些例子.

例1 次数不超过 $n$ 的多项式的全体，记作 $P[x]_n$ ，即

$$
P [ x ] _ {n} = \left\{a _ {n} x ^ {n} + a _ {n - 1} x ^ {n - 1} + \dots + a _ {1} x + a _ {0} \mid a _ {n}, a _ {n - 1}, \dots , a _ {1}, a _ {0} \in \mathbb {R} \right\},
$$

对于通常的多项式加法、数乘多项式的乘法构成向量空间.这是因为:通常的多项式加法、数乘多项式的乘法两种运算显然满足线性运算规律,故只要验证 $P[x]_{n}$ 对运算封闭:

$$
(a _ {n} x ^ {n} + \dots + a _ {1} x + a _ {0}) + (b _ {n} x ^ {n} + \dots + b _ {1} x + b _ {0}) = (a _ {n} + b _ {n}) x ^ {n} + \dots + (a _ {1} + b _ {1}) x + (a _ {0} + b _ {0}) \in P [ x ] _ {n},
$$

$$
\lambda \left(a _ {n} x ^ {n} + \dots + a _ {1} x + a _ {0}\right) = (\lambda a _ {n}) x ^ {n} + \dots + (\lambda a _ {1}) x + (\lambda a _ {0}) \in P [ x ] _ {n},
$$

所以 $P[x]_n$ 是一个向量空间.

例2 $n$ 次多项式的全体

$$
Q [ x ] _ {n} = \left\{a _ {n} x ^ {n} + a _ {n - 1} x ^ {n - 1} + \dots + a _ {1} x + a _ {0} \mid a _ {n}, a _ {n - 1}, \dots , a _ {1}, a _ {0} \in \mathbb {R}, \text {且} a _ {n} \neq 0 \right\}
$$

对于通常的多项式加法和数乘运算不构成向量空间.这是因为

$$
0 p = 0 x ^ {n} + 0 x ^ {n - 1} + \dots + 0 x + 0 \notin Q [ x ] _ {n},
$$

即 $Q[x]_n$ 对运算不封闭.

例3 正弦函数的集合

$$
S [ x ] = \{A \sin (x + B) \mid A, B \in \mathbb {R} \}
$$

对于通常的函数加法及数乘函数的乘法构成向量空间.这是因为:通常的函数加法及数乘运算显然满足线性运算规律,故只要验证 $S[x]$ 对运算封闭:

$$
\begin{array}{l} s _ {1} + s _ {2} = A _ {1} \sin (x + B _ {1}) + A _ {2} \sin (x + B _ {2}) \\ = (a _ {1} \cos x + b _ {1} \sin x) + (a _ {2} \cos x + b _ {2} \sin x) \\ = (a _ {1} + a _ {2}) \cos x + (b _ {1} + b _ {2}) \sin x = A \sin (x + B) \in S [ x ], \\ \end{array}
$$

考研电子书网站:www.pdf2book.com

143

---

\*第6章 线性空间与线性变换

$$
\lambda s _ {1} = \lambda A _ {1} \sin (x + B _ {1}) = (\lambda A _ {1}) \sin (x + B _ {1}) \in S [ x ],
$$

所以 $S[x]$ 是一个向量空间.

检验一个集合是否构成向量空间,当然不能只检验对运算的封闭性(如上面两例).若所定义的加法和数乘运算不是通常的实数的加、乘运算,则就应仔细检验是否满足八条线性运算规律.

例4 $n$ 个有序实数组成的数组的全体

$$
S ^ {n} = \left\{\left(x _ {1}, x _ {2}, \dots , x _ {n}\right) ^ {\mathrm{T}} \mid x _ {1}, x _ {2}, \dots , x _ {n} \in \mathbb {R} \right\}
$$

对于通常的有序数组的加法及如下定义的数乘

$$
\lambda \circ (x _ {1}, x _ {2}, \dots , x _ {n}) ^ {\mathrm{T}} = (0, 0, \dots , 0) ^ {\mathrm{T}}
$$

不构成向量空间.

可以验证 $S^n$ 对运算封闭. 但因 $1 \circ x = 0$, 不满足线性运算的规律 (v), 即所定义的运算不是线性运算, 所以 $S^n$ 不是向量空间.

比较 $S^n$ 与 $\mathbb{R}^n$, 作为集合它们是一样的, 但由于在其中所定义的运算不同, 以至 $\mathbb{R}^n$ 构成向量空间而 $S^n$ 不是向量空间. 由此可见, 向量空间的概念是集合与运算二者的结合. 一般来说, 同一个集合, 若定义两种不同的线性运算, 就构成不同的向量空间; 若定义的运算不是线性运算, 就不能构成向量空间. 所以, 所定义的线性运算是向量空间的本质, 而其中的元素是什么并不重要.

为了对线性运算的理解更具有一般性,请看下例.

例 5 正实数的全体, 记作  $R^{+}$ , 在其中定义加法及数乘运算为

$$
a \oplus b = a b \quad (a, b \in \mathbb {R} ^ {+}),
$$

$$
\lambda \circ a = a ^ {\lambda} \quad (\lambda \in \mathbb {R}, a \in \mathbb {R} ^ {+}),
$$

验证  $R^{+}$ 对上述加法与数乘运算构成线性空间.

证 实际上要验证十条:

对加法封闭: 对任意的  $a, b \in R^{+}$ ，有  $a \oplus b = ab \in R^{+}$ ;

对数乘封闭: 对任意的  $\lambda \in R, a \in R^{+}$ ，有  $\lambda \circ a = a^{\lambda} \in R^{+}$ .

(i)  $a \oplus b = ab = ba = b \oplus a;$
(ii)  $(a \oplus b) \oplus c = (ab) \oplus c = (ab)c = a(bc) = a \oplus (b \oplus c)$ ;
(iii)  $R^{+}$  中存在零元素 1, 对任何  $a \in R^{+}$ , 有  $a \oplus 1 = a \cdot 1 = a$ ;
(iv) 对任何 $a \in \mathbb{R}^+$, 有负元素 $a^{-1} \in \mathbb{R}^+$, 使 $a \oplus a^{-1} = aa^{-1} = 1$;
(v)  $1 \circ a = a^{1} = a;$
(vi)  $\lambda\circ(\mu\circ a)=\lambda\circ a^{\mu}=\left(^{\prime}\dot{a}^{\mu}\right)^{\lambda}=a^{\lambda\mu}=\left(\lambda\mu\right)\circ a;$
(vii) $(\lambda + \mu) \circ a = a^{\lambda + \mu} = a^{\lambda}a^{\mu} = a^{\lambda} \oplus a^{\mu} = \lambda \circ a \oplus \mu \circ a;$
(viii) $\lambda \circ (a \oplus b) = \lambda \circ (ab) = (ab)^{\lambda} = a^{\lambda}b^{\lambda} = a^{\lambda} \oplus b^{\lambda} = \lambda \circ a \oplus \lambda \circ b,$

144

---

§1 线性空间的定义与性质

因此，$\mathbb{R}^{+}$对于所定义的运算构成线性空间.

下面讨论线性空间的性质.

## 1. 零向量是惟一的.

证 设 $\mathbf{0}_1, \mathbf{0}_2$ 是线性空间 $V$ 中的两个零向量，即对任何 $\alpha \in V$，有 $\alpha + \mathbf{0}_1 = \alpha$，$\alpha + \mathbf{0}_2 = \alpha$。于是特别有

$$
\mathbf {0} _ {2} + \mathbf {0} _ {1} = \mathbf {0} _ {2}, \quad \mathbf {0} _ {1} + \mathbf {0} _ {2} = \mathbf {0} _ {1},
$$

所以

$$
\mathbf {0} _ {1} = \mathbf {0} _ {1} + \mathbf {0} _ {2} = \mathbf {0} _ {2} + \mathbf {0} _ {1} = \mathbf {0} _ {2}.
$$

证毕

2. 任一向量的负向量是惟一的, $\alpha$ 的负向量记作- $\alpha$.

证 设 $\beta, \gamma$ 是 $\alpha$ 的负向量，即 $\alpha + \beta = 0, \alpha + \gamma = 0$. 于是

$$
\boldsymbol {\beta} = \boldsymbol {\beta} + \mathbf {0} = \boldsymbol {\beta} + (\alpha + \gamma) = (\alpha + \boldsymbol {\beta}) + \gamma = \mathbf {0} + \gamma = \gamma .
$$

证毕

3. $0\alpha = 0, (-1)\alpha = -\alpha, \lambda 0 = 0.$

证 $\alpha + 0\alpha = 1\alpha + 0\alpha = (1 + 0)\alpha = 1\alpha = \alpha,$

两端同时加上 $\alpha$ 的负向量，即得 $0\alpha = 0$

$$
\alpha + (- 1) \alpha = 1 \alpha + (- 1) \alpha = [ 1 + (- 1) ] \alpha = 0 \alpha = 0,
$$

所以

$$
(- 1) \alpha = - \alpha ;
$$

$$
\lambda \mathbf {0} = \lambda [ \alpha + (- 1) \alpha ] = \lambda \alpha + (- \lambda) \alpha = [ \lambda + (- \lambda) ] \alpha = 0 \alpha = \mathbf {0}.
$$

证毕

4. 如果  $\lambda\alpha=0$ ，则  $\lambda=0$  或  $\alpha=0$ .

证 若 $\lambda \neq 0$ ，在 $\lambda \alpha = 0$ 两端乘 $\frac{1}{\lambda}$ 得

$$
\frac {1}{\lambda} (\lambda \alpha) = \frac {1}{\lambda} \mathbf {0} = \mathbf {0},
$$

而

$$
\frac {1}{\lambda} (\lambda \alpha) = \left(\frac {1}{\lambda} \lambda\right) \alpha = 1 \alpha = \alpha ,
$$

所以

$$
\alpha = 0.
$$

证毕

在第 4 章中, 我们提出过子空间的定义, 今稍作修正.

定义 2 设 V 是一个线性空间, L 是 V 的一个非空子集, 如果 L 对于 V 中所定义的加法和数乘两种运算也构成一个线性空间, 则称 L 为 V 的子空间.

考研电子书网站:www.pdf2book.com

145

---

\*第6章 线性空间与线性变换

一个非空子集要满足什么条件才构成子空间？因 $L$ 是 $V$ 的一部分，$V$ 中的运算对于 $L$ 而言，规律(i)、(ii)、(v)、(vi)、(vii)、(viii)显然是满足的，因此只要 $L$ 对运算封闭且满足规律(iii)、(iv)即可.但由线性空间的性质知，若 $L$ 对运算封闭，则即能满足规律(iii)、(iv).因此我们有

定理1 线性空间 $V$ 的非空子集 $L$ 构成子空间的充分必要条件是: $L$ 对于 $V$ 中的线性运算封闭.

## § 2 维数、基与坐标

在第4章中,我们用线性运算来讨论n维数组向量之间的关系,介绍了一些重要概念,如线性组合、线性相关与线性无关等.这些概念以及有关的性质只涉及线性运算,因此,对于一般的线性空间中的向量仍然适用.以后我们将直接引用这些概念和性质.

在第 4 章中我们已经提出了基与维数的概念, 这当然也适用于一般的线性空间. 这是线性空间的主要特性, 特再叙述如下:

定义 3 在线性空间 V 中, 如果存在 n 个向量  $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{n}$ , 满足

(i)  $\alpha_{1},\alpha_{2},\cdots,\alpha_{n}$  线性无关；
(ii) V 中任一向量  $\alpha$  总可由  $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{n}$  线性表示，

那么  $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{n}$  就称为线性空间 V 的一个基，n 称为线性空间 V 的维数。只含一个零向量的线性空间没有基，规定它的维数为 0。

维数为 n 的线性空间称为 n 维线性空间, 记作  $V_{n}$ .

这里要指出:线性空间的维数可以是无穷.对于无穷维的线性空间,本书不作讨论.

对于 n 维线性空间  $V_{n}$ ，若知  $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{n}$  为  $V_{n}$  的一个基，则  $V_{n}$  可表示为

$$
V _ {n} = \left\{x _ {1} \boldsymbol {\alpha} _ {1} + x _ {2} \boldsymbol {\alpha} _ {2} + \dots + x _ {n} \boldsymbol {\alpha} _ {n} \mid x _ {1}, x _ {2}, \dots , x _ {n} \in \mathbb {R} \right\} = \operatorname{Span} \left\{\boldsymbol {\alpha} _ {1}, \boldsymbol {\alpha} _ {2}, \dots , \boldsymbol {\alpha} _ {n} \right\},
$$

即  $V_{n}$  是基所生成的线性空间, 这就较清楚地显示出线性空间  $V_{n}$  的构造.

若  $\alpha_{1},\alpha_{2},\cdots,\alpha_{n}$  为  $V_{n}$  的一个基，则对任何  $\alpha\in V_{n}$ ，都有惟一的一组有序数  $x_{1},x_{2},\cdots,x_{n}$ ，使

$$
\boldsymbol {\alpha} = x _ {1} \boldsymbol {\alpha} _ {1} + x _ {2} \boldsymbol {\alpha} _ {2} + \dots + x _ {n} \boldsymbol {\alpha} _ {n};
$$

反之，任给一组有序数 $x_{1}, x_{2}, \cdots, x_{n}$，总有惟一的向量

$$
\dot {\boldsymbol {\alpha}} = x _ {1} \boldsymbol {\alpha} _ {1} + x _ {2} \boldsymbol {\alpha} _ {2} + \dots + x _ {n} \boldsymbol {\alpha} _ {n} \in V _ {n}.
$$

这样  $V_{n}$  的向量  $\alpha$  与有序数组  $(x_{1}, x_{2}, \cdots, x_{n})^{\mathrm{T}}$  之间存在着一一对应的关系, 因此可以用这组有序数来表示向量  $\alpha$ . 于是我们有

146

---

§2 维数、基与坐标

定义 4 设  $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{n}$  是线性空间  $V_{n}$  的一个基. 对于任一向量  $\alpha \in V_{n}$ ，总有且仅有一组有序数  $x_{1}, x_{2}, \cdots, x_{n}$  使

$$
\boldsymbol {\alpha} = x _ {1} \boldsymbol {\alpha} _ {1} + x _ {2} \boldsymbol {\alpha} _ {2} + \dots + x _ {n} \boldsymbol {\alpha} _ {n},
$$

$x_{1},x_{2},\cdots,x_{n}$  这组有序数就称为向量  $\alpha$  在  $\alpha_{1},\alpha_{2},\cdots,\alpha_{n}$  这个基中的坐标，并记作

$$
\boldsymbol {x} = (x _ {1}, x _ {2}, \dots , x _ {n}) ^ {\mathrm{T}}.
$$

例6 在线性空间 $P[x]_4$ 中, $p_1 = 1, p_2 = x, p_3 = x^2, p_4 = x^3, p_5 = x^4$ 就是它的一个基.任一不超过4次的多项式

$$
p = a _ {4} x ^ {4} + a _ {3} x ^ {3} + a _ {2} x ^ {2} + a _ {1} x + a _ {0}
$$

都可表示为

$$
\boldsymbol {p} = a _ {0} \boldsymbol {p} _ {1} + a _ {1} \boldsymbol {p} _ {2} + a _ {2} \boldsymbol {p} _ {3} + a _ {3} \boldsymbol {p} _ {4} + a _ {4} \boldsymbol {p} _ {5},
$$

因此 $\pmb{p}$ 在这个基中的坐标为 $(a_0, a_1, a_2, a_3, a_4)^{\mathrm{T}}$.

若另取一个基 $q_{1} = 1, q_{2} = 1 + x, q_{3} = 2x^{2}, q_{4} = x^{3}, q_{5} = x^{4}$, 则

$$
\begin{array}{l} p = a _ {0} + a _ {1} x + a _ {2} x ^ {2} + a _ {3} x ^ {3} + a _ {4} x ^ {4} \\ = (a _ {0} - a _ {1}) + a _ {1} (1 + x) + \frac {a _ {2}}{2} 2 x ^ {2} + a _ {3} x ^ {3} + a _ {4} x ^ {4} \\ = (a _ {0} - a _ {1}) q _ {1} + a _ {1} q _ {2} + \frac {1}{2} a _ {2} q _ {3} + a _ {3} q _ {4} + a _ {4} q _ {5}, \\ \end{array}
$$

因此 p 在这个基中的坐标为  $\left(a_{0}-a_{1},a_{1},\frac{1}{2}a_{2},a_{3},a_{4}\right)^{\mathrm{T}}$ .

建立了坐标以后,就把抽象的向量  $\alpha$  与具体的数组向量  $(x_{1}, x_{2}, \cdots, x_{n})^{\mathrm{T}}$  联系起来了,并且还可把  $V_{n}$  中抽象的线性运算与  $R^{n}$  中数组向量的线性运算联系起来.

设  $\alpha,\beta\in V_{n}$ ，有  $\alpha=x_{1}\alpha_{1}+x_{2}\alpha_{2}+\cdots+x_{n}\alpha_{n},\beta=y_{1}\alpha_{1}+y_{2}\alpha_{2}+\cdots+y_{n}\alpha_{n}$ ，于是

$$
\alpha + \beta = (x _ {1} + y _ {1}) \alpha_ {1} + (x _ {2} + y _ {2}) \alpha_ {2} + \dots + (x _ {n} + y _ {n}) \alpha_ {n},
$$

$$
\lambda \alpha = (\lambda x _ {1}) \alpha_ {1} + (\lambda x _ {2}) \alpha_ {2} + \dots + (\lambda x _ {n}) \alpha_ {n},
$$

即 $\alpha +\beta$ 的坐标是

$$
(x _ {1} + y _ {1}, x _ {2} + y _ {2}, \dots , x _ {n} + y _ {n}) ^ {\mathrm{T}} = (x _ {1}, x _ {2}, \dots , x _ {n}) ^ {\mathrm{T}} + (y _ {1}, y _ {2}, \dots , y _ {n}) ^ {\mathrm{T}},
$$

$\lambda \alpha$ 的坐标是

$$
\left(\lambda x _ {1}, \lambda x _ {2}, \dots , \lambda x _ {n}\right) ^ {\mathrm{T}} = \lambda \left(x _ {1}, x _ {2}, \dots , x _ {n}\right) ^ {\mathrm{T}}.
$$

总之, 设在 $n$ 维线性空间 $V_{n}$ 中取定一个基 $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{n}$, 则 $V_{n}$ 中的向量 $\alpha$ 与 $\mathbb{R}^{n}$ 中 $n$ 维数组向量空间的向量 $(x_{1}, x_{2}, \cdots, x_{n})^{\mathrm{T}}$ 之间就有一个一一对应的关系, 且这个对应关系具有下述性质:

设  $\boldsymbol{\alpha}\leftrightarrow(x_{1},x_{2},\cdots,x_{n})^{\mathrm{T}},\boldsymbol{\beta}\leftrightarrow(y_{1},y_{2},\cdots,y_{n})^{\mathrm{T}}$ ，则

(i)  $\boldsymbol{\alpha}+\boldsymbol{\beta}\leftrightarrow(x_{1},x_{2},\cdots,x_{n})^{\mathrm{T}}+(y_{1},y_{2},\cdots,y_{n})^{\mathrm{T}},$

考研电子书网站:www.pdf2book.com

147

---

\*第6章 线性空间与线性变换

(ii)  $\lambda\alpha\leftrightarrow\lambda(x_{1},x_{2},\cdots,x_{n})^{\mathrm{T}}.$

也就是说, 这个对应关系保持线性组合的对应. 因此, 我们可以说 $V_{n}$ 与 $\mathbb{R}^{n}$ 有相同的结构, 我们称 $V_{n}$ 与 $\mathbb{R}^{n}$ 同构.

一般地, 设 V 与 U 是两个线性空间, 如果在它们的向量之间有一一对应关系, 且这个对应关系保持线性组合的对应, 那么就说线性空间 V 与 U 同构.

显然,任何 n 维线性空间都与  $R^{n}$  同构,即维数相等的线性空间都同构.从而可知线性空间的结构完全被它的维数所决定.

同构的概念除向量一一对应外,主要是保持线性运算的对应关系.因此, $V_{n}$ 中的抽象的线性运算就可转化为 $R^{n}$ 中的线性运算,并且 $R^{n}$ 中凡是只涉及线性运算的性质就都适用于 $V_{n}$.但 $R^{n}$ 中超出线性运算的性质,在 $V_{n}$ 中就不一定具备,例如 $R^{n}$ 中的内积概念在 $V_{n}$ 中就不一定有意义.

## § 3 基变换与坐标变换

由例 6 可见, 同一向量在不同的基中有不同的坐标, 那么, 不同的基与不同的坐标之间有怎样的关系呢?

设  $\alpha_{1},\alpha_{2},\cdots,\alpha_{n}$  及  $\beta_{1},\beta_{2},\cdots,\beta_{n}$  是线性空间  $V_{n}$  中的两个基，

$$
\left\{ \begin{array}{l} \boldsymbol {\beta} _ {1} = p _ {1 1} \boldsymbol {\alpha} _ {1} + p _ {2 1} \boldsymbol {\alpha} _ {2} + \dots + p _ {n 1} \boldsymbol {\alpha} _ {n}, \\ \boldsymbol {\beta} _ {2} = p _ {1 2} \boldsymbol {\alpha} _ {1} + p _ {2 2} \boldsymbol {\alpha} _ {2} + \dots + p _ {n 2} \boldsymbol {\alpha} _ {n}, \\ \dots \dots \\ \boldsymbol {\beta} _ {n} = p _ {1 n} \boldsymbol {\alpha} _ {1} + p _ {2 n} \boldsymbol {\alpha} _ {2} + \dots + p _ {n n} \boldsymbol {\alpha} _ {n}, \end{array} \right. \tag {1}
$$

把  $\alpha_{1},\alpha_{2},\cdots,\alpha_{n}$  这 n 个有序向量记作  $(\boldsymbol{\alpha}_{1},\boldsymbol{\alpha}_{2},\cdots,\boldsymbol{\alpha}_{n})$ ，记 n 阶矩阵  $\boldsymbol{P}=(p_{ij})$ ，利用向量和矩阵的形式，(1) 式可表示为

$$
(\boldsymbol {\beta} _ {1}, \boldsymbol {\beta} _ {2}, \dots , \boldsymbol {\beta} _ {n}) = (\boldsymbol {\alpha} _ {1}, \boldsymbol {\alpha} _ {2}, \dots , \boldsymbol {\alpha} _ {n}) \boldsymbol {P}. \tag {2}
$$

(1)式或(2)式称为基变换公式,矩阵P称为由基 $\alpha_{1},\alpha_{2},\cdots,\alpha_{n}$ 到基 $\beta_{1},\beta_{2},\cdots,\beta_{n}$ 的过渡矩阵.由于 $\beta_{1},\beta_{2},\cdots,\beta_{n}$ 线性无关,故过渡矩阵P可逆.

定理 2 设  $V_{n}$  中的向量  $\alpha$  在基  $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{n}$  中的坐标为  $(x_{1}, x_{2}, \cdots, x_{n})^{\mathrm{T}}$ ，在基  $\beta_{1}, \beta_{2}, \cdots, \beta_{n}$  中的坐标为  $(x_{1}', x_{2}', \cdots, x_{n}')^{\mathrm{T}}$ 。若两个基满足关系式(2)，则有坐标变换公式

$$
\left( \begin{array}{c} x _ {1} \\ x _ {2} \\ \vdots \\ x _ {n} \end{array} \right) = \boldsymbol {P} \left( \begin{array}{c} x _ {1} ^ {\prime} \\ x _ {2} ^ {\prime} \\ \vdots \\ x _ {n} ^ {\prime} \end{array} \right) \quad \text {或} \quad \left( \begin{array}{c} x _ {1} ^ {\prime} \\ x _ {2} ^ {\prime} \\ \vdots \\ x _ {n} ^ {\prime} \end{array} \right) = \boldsymbol {P} ^ {- 1} \left( \begin{array}{c} x _ {1} \\ x _ {2} \\ \vdots \\ x _ {n} \end{array} \right). \tag {3}
$$

148

---

§3 基变换与坐标变换

证因

$$
(\boldsymbol {\alpha} _ {1}, \boldsymbol {\alpha} _ {2}, \dots , \boldsymbol {\alpha} _ {n}) \left( \begin{array}{c} x _ {1} \\ x _ {2} \\ \vdots \\ x _ {n} \end{array} \right) = \boldsymbol {\alpha} = (\boldsymbol {\beta} _ {1}, \boldsymbol {\beta} _ {2}, \dots , \boldsymbol {\beta} _ {n}) \left( \begin{array}{c} x _ {1} ^ {\prime} \\ x _ {2} ^ {\prime} \\ \vdots \\ x _ {n} ^ {\prime} \end{array} \right) = (\boldsymbol {\alpha} _ {1}, \boldsymbol {\alpha} _ {2}, \dots , \boldsymbol {\alpha} _ {n}) P \left( \begin{array}{c} x _ {1} ^ {\prime} \\ x _ {2} ^ {\prime} \\ \vdots \\ x _ {n} ^ {\prime} \end{array} \right),
$$

由于  $\alpha_{1},\alpha_{2},\cdots,\alpha_{n}$  线性无关,故即有关系式(3).

证毕

这个定理的逆命题也成立. 即若任一向量的两种坐标满足坐标变换公式(3), 则两个基满足基变换公式(2).

例7 在 $P[x]_3$ 中取两个基

$$
\boldsymbol {\alpha} _ {1} = x ^ {3} + 2 x ^ {2} - x, \quad \boldsymbol {\alpha} _ {2} = x ^ {3} - x ^ {2} + x + 1, \quad \boldsymbol {\alpha} _ {3} = - x ^ {3} + 2 x ^ {2} + x + 1, \quad \boldsymbol {\alpha} _ {4} = - x ^ {3} - x ^ {2} + 1
$$

及

$$
\boldsymbol {\beta} _ {1} = 2 x ^ {3} + x ^ {2} + 1, \quad \boldsymbol {\beta} _ {2} = x ^ {2} + 2 x + 2, \quad \boldsymbol {\beta} _ {3} = - 2 x ^ {3} + x ^ {2} + x + 2, \quad \boldsymbol {\beta} _ {4} = x ^ {3} + 3 x ^ {2} + x + 2.
$$

求坐标变换公式.

解 将 $\beta_{1},\beta_{2},\beta_{3},\beta_{4}$ 用 $\alpha_{1},\alpha_{2},\alpha_{3},\alpha_{4}$ 表示.由

$$
(\boldsymbol {\alpha} _ {1}, \boldsymbol {\alpha} _ {2}, \boldsymbol {\alpha} _ {3}, \boldsymbol {\alpha} _ {4}) = (x ^ {3}, x ^ {2}, x, 1) \boldsymbol {A}, \quad (\boldsymbol {\beta} _ {1}, \boldsymbol {\beta} _ {2}, \boldsymbol {\beta} _ {3}, \boldsymbol {\beta} _ {4}) = (x ^ {3}, x ^ {2}, x, 1) \boldsymbol {B},
$$

其中

$$
\boldsymbol {A} = \left( \begin{array}{r r r r} 1 & 1 & - 1 & - 1 \\ 2 & - 1 & 2 & - 1 \\ - 1 & 1 & 1 & 0 \\ 0 & 1 & 1 & 1 \end{array} \right), \quad \boldsymbol {B} = \left( \begin{array}{r r r r} 2 & 0 & - 2 & 1 \\ 1 & 1 & 1 & 3 \\ 0 & 2 & 1 & 1 \\ 1 & 2 & 2 & 2 \end{array} \right),
$$

得

$$
(\boldsymbol {\beta} _ {1}, \boldsymbol {\beta} _ {2}, \boldsymbol {\beta} _ {3}, \boldsymbol {\beta} _ {4}) = (\boldsymbol {\alpha} _ {1}, \boldsymbol {\alpha} _ {2}, \boldsymbol {\alpha} _ {3}, \boldsymbol {\alpha} _ {4}) \boldsymbol {A} ^ {- 1} \boldsymbol {B},
$$

故坐标变换公式为

$$
\left( \begin{array}{c} x _ {1} ^ {\prime} \\ x _ {2} ^ {\prime} \\ x _ {3} ^ {\prime} \\ x _ {4} ^ {\prime} \end{array} \right) = \boldsymbol {B} ^ {- 1} \boldsymbol {A} \left( \begin{array}{c} x _ {1} \\ x _ {2} \\ x _ {3} \\ x _ {4} \end{array} \right).
$$

用矩阵的初等行变换求  $B^{-1}A$ : 把矩阵  $(B,A)$  中的 B 变成 E, 则 A 即变成  $B^{-1}A$ . 计算如下:

$$
(\boldsymbol {B}, \boldsymbol {A}) = \left( \begin{array}{c c c c c c c c} 2 & 0 & - 2 & 1 & 1 & 1 & - 1 & - 1 \\ 1 & 1, & 1 & 3 & 2 & - 1 & 2 & - 1 \\ 0 & 2 & 1 & 1 & - 1 & 1 & 1 & 0 \\ 1 & 2 & 2 & 2 & 0 & 1 & 1 & 1 \end{array} \right)
$$

考研电子书网站:www.pdf2book.com

149

---

\*第6章 线性空间与线性变换

$$
\underbrace {r _ {1} - 2 r _ {2}} _ {r _ {4} - r _ {2}} \left( \begin{array}{c c c c c c c c} 0 & - 2 & - 4 & - 5 & - 3 & 3 & - 5 & 1 \\ 1 & 1 & 1 & 3 & 2 & - 1 & 2 & - 1 \\ 0 & 2 & 1 & 1 & - 1 & 1 & 1 & 0 \\ 0 & 1 & 1 & - 1 & - 2 & 2 & - 1 & 2 \end{array} \right)
$$

$$
\left( \begin{array}{c c c c c c c c} 0 & 0 & - 2 & - 7 & - 7 & 7 & - 7 & 5 \\ 1 & 0 & 0 & 4 & 4 & - 3 & 3 & - 3 \\ 0 & 0 & - 1 & 3 & 3 & - 3 & 3 & - 4 \\ 0 & 1 & 1 & - 1 & - 2 & 2 & - 1 & 2 \end{array} \right)
$$

$$
\underbrace {r _ {1} - 2 r _ {3}} _ {r _ {4} + r _ {3}} \left( \begin{array}{c c c c c c c c} 0 & 0 & 0 & - 1 3 & - 1 3 & 1 3 & - 1 3 & 1 3 \\ 1 & 0 & 0 & 4 & 4 & - 3 & 3 & - 3 \\ 0 & 0 & - 1 & 3 & 3 & - 3 & 3 & - 4 \\ 0 & 1 & 0 & 2 & 1 & - 1 & 2 & - 2 \end{array} \right)
$$

$$
\underbrace {r _ {1} \times \left(- \frac {1}{1 3}\right)} _ {r _ {2} - 4 r _ {1}} \left( \begin{array}{c c c c c c c c} 0 & 0 & 0 & 1 & 1 & - 1 & 1 & - 1 \\ 1 & 0 & 0 & 0 & 0 & 1 & - 1 & 1 \\ 0 & 0 & - 1 & 0 & 0 & 0 & 0 & - 1 \\ 0 & 1 & 0 & 0 & - 1 & 1 & 0 & 0 \end{array} \right)
$$

$$
\underbrace { \begin{array}{c} r _ {1} \leftrightarrow r _ {2} \\ r _ {3} \times (- 1) \\ r _ {2} \leftrightarrow r _ {4} \end{array} } _ {r _ {2} \leftrightarrow r _ {4}} \left( \begin{array}{c c c c c c c c} 1 & 0 & 0 & 0 & 0 & 1 & - 1 & 1 \\ 0 & 1 & 0 & 0 & - 1 & 1 & 0 & 0 \\ 0 & 0 & 1 & 0 & 0 & 0 & 0 & 1 \\ 0 & 0 & 0 & 1 & 1 & - 1 & 1 & - 1 \end{array} \right),
$$

于是坐标变换公式为

$$
\left( \begin{array}{c} x _ {1} ^ {\prime} \\ x _ {2} ^ {\prime} \\ x _ {3} ^ {\prime} \\ x _ {4} ^ {\prime} \end{array} \right) = \left( \begin{array}{c c c c} 0 & 1 & - 1 & 1 \\ - 1 & 1 & 0 & 0 \\ 0 & 0 & 0 & 1 \\ 1 & - 1 & 1 & - 1 \end{array} \right) \left( \begin{array}{c} x _ {1} \\ x _ {2} \\ x _ {3} \\ x _ {4} \end{array} \right).
$$

## § 4 线性变换

定义 5 设有两个非空集合 A, B, 如果对于 A 中任一元素  $\alpha$ , 按照一定的规则, 总

150

---

§4 线性变换

有 B 中一个确定的元素  $\beta$  和它对应, 那么, 这个对应规则称为从集合 A 到集合 B 的映射. 我们常用字母表示一个映射, 譬如把上述映射记作 T, 并记

$$
\beta = T (\alpha) \quad \text {或} \quad \beta = T \alpha (\alpha \in A). \tag {4}
$$

设 $\alpha_{1} \in A, T(\alpha_{1}) = \beta_{1}$, 就说映射 $T$ 把元素 $\alpha_{1}$ 变为 $\beta_{1}, \beta_{1}$ 称为 $\alpha_{1}$ 在映射 $T$ 下的像, $\alpha_{1}$ 称为 $\beta_{1}$ 在映射 $T$ 下的原像. $A$ 称为映射 $T$ 的定义域, 像的全体所构成的集合称为像集, 记作 $T(A)$, 即

$$
T (A) = \{\beta = T (\alpha) \mid \alpha \in A \},
$$

显然 $T(A)\subseteq B$

映射的概念是函数概念的推广.例如,设二元函数 $z=f(x,y)$ 的定义域为平面区域G,函数值域为Z,那么,函数关系f就是一个从定义域G到实数域R的映射;函数值 $f(x_{0},y_{0})=z_{0}$ 就是元素 $(x_{0},y_{0})$ 的像, $(x_{0},y_{0})$ 就是 $z_{0}$ 的原像,Z就是像集.

定义6 设 $V_{n}, U_{m}$ 分别是 $n$ 维和 $m$ 维线性空间, $T$ 是一个从 $V_{n}$ 到 $U_{m}$ 的映射, 如果映射 $T$ 满足

(i) 任给 $\alpha_{1}, \alpha_{2} \in V_{n}$ （从而 $\alpha_{1} + \alpha_{2} \in V_{n}$），有

$$
T (\boldsymbol {\alpha} _ {1} + \boldsymbol {\alpha} _ {2}) = T (\boldsymbol {\alpha} _ {1}) + T (\boldsymbol {\alpha} _ {2}),
$$

(ii) 任给 $\alpha \in V_{n}, \lambda \in \mathbb{R}$ （从而 $\lambda \alpha \in V_{n}$），有

$$
T (\lambda \alpha) = \lambda T (\alpha),
$$

那么 T 就称为从  $V_{n}$  到  $U_{m}$  的线性映射.

简言之,线性映射就是保持线性组合的对应的映射.

例如,关系式

$$
\left( \begin{array}{c} y _ {1} \\ y _ {2} \\ \vdots \\ y _ {m} \end{array} \right) = \left( \begin{array}{c c c c} a _ {1 1} & a _ {1 2} & \dots & a _ {1 n} \\ a _ {2 1} & a _ {2 2} & \dots & a _ {2 n} \\ \vdots & \vdots & & \vdots \\ a _ {m 1} & a _ {m 2} & \dots & a _ {m n} \end{array} \right) \left( \begin{array}{c} x _ {1} \\ x _ {2} \\ \vdots \\ x _ {n} \end{array} \right)
$$

就确定了一个从 $\mathbb{R}^n$ 到 $\mathbb{R}^m$ 的映射，并且是个线性映射(参见后面的例10).

特别地,在定义6中,如果 $U_{m}=V_{n}$ ,那么T是一个从线性空间 $V_{n}$ 到其自身的线性映射,称为线性空间 $V_{n}$ 中的线性变换.

下面我们只讨论线性空间  $V_{n}$  中的线性变换.

例8 在线性空间 $P[x]_3$ 中，

(1) 如果微分运算 D 表示对 x 求导的运算  $\frac{d}{dx}$ ，那么 D 是一个线性变换。这是因为任取  $p = a_{3}x^{3} + a_{2}x^{2} + a_{1}x + a_{0} \in P[x]_{3}$ ，则  $Dp = 3a_{3}x^{2} + 2a_{2}x + a_{1}$ ;

$q=b_{3}x^{3}+b_{2}x^{2}+b_{1}x+b_{0}\in P[x]_{3}$ ，则 $Dq=3b_{3}x^{2}+2b_{2}x+b_{1}$

从而有

考研电子书网站:www.pdf2book.com

151

---

\*第6章 线性空间与线性变换

$$
\begin{array}{l} \mathrm{D} (\boldsymbol {p} + \boldsymbol {q}) = \mathrm{D} \left[ \left(a _ {3} + b _ {3}\right) x ^ {3} + \left(a _ {2} + b _ {2}\right) x ^ {2} + \left(a _ {1} + b _ {1}\right) x + \left(a _ {0} + b _ {0}\right) \right] \\ = 3 \left(a _ {3} + b _ {3}\right) x ^ {2} + 2 \left(a _ {2} + b _ {2}\right) x + \left(a _ {1} + b _ {1}\right) \\ = (3 a _ {3} x ^ {2} + 2 a _ {2} x + a _ {1}) + (3 b _ {3} x ^ {2} + 2 b _ {2} x + b _ {1}) = \mathrm{D} p + \mathrm{D} q; \\ \mathrm{D} (\lambda p) = \mathrm{D} \left(\lambda a _ {3} x ^ {3} + \lambda a _ {2} x ^ {2} + \lambda a _ {1} x + \lambda a _ {0}\right) = \lambda \left(3 a _ {3} x ^ {2} + 2 a _ {2} x + a _ {1}\right) = \lambda \mathrm{D} p. \\ \end{array}
$$

(2) 如果  $T(\boldsymbol{p}) = a_{0}$ ，那么 T 也是一个线性变换。这是因为

$$
T (\boldsymbol {p} + \boldsymbol {q}) = a _ {0} + b _ {0} = T (\boldsymbol {p}) + T (\boldsymbol {q});
$$

$$
T (\lambda \boldsymbol {p}) = \lambda a _ {0} = \lambda T (\boldsymbol {p}).
$$

（3）如果 $T_{1}(\pmb {p}) = 1$ ，那么 $T_{1}$ 是个变换，但不是线性变换.这是因为 $T_{1}(\pmb {p} + \pmb {q}) = 1$ ，而$T_{1}(\pmb {p}) + T_{1}(\pmb {q}) = 1 + 1 = 2,$ 故

$$
T _ {1} (\boldsymbol {p} + \boldsymbol {q}) \neq T _ {1} (\boldsymbol {p}) + T _ {1} (\boldsymbol {q}).
$$

例9 关系式

$$
T \binom{x}{y} = \left( \begin{array}{c c} \cos \varphi & - \sin \varphi \\ \sin \varphi & \cos \varphi \end{array} \right) \binom{x}{y}
$$

确定了 $xOy$ 平面上的一个变换 $T$, 说明变换 $T$ 的几何意义(参见第2章图2.3).

解 记 $\left\{\begin{aligned}x&=r\cos\theta,\\ y&=r\sin\theta,\end{aligned}\right.$ 于是

$$
T \binom{x}{y} = \binom {x \cos \varphi - y \sin \varphi}{x \sin \varphi + y \cos \varphi} = \binom {r \cos \theta \cos \varphi - r \sin \theta \sin \varphi}{r \cos \theta \sin \varphi + r \sin \theta \cos \varphi} = \binom {r \cos (\theta + \varphi)} {r \sin (\theta + \varphi)},
$$

这表示变换 $T$ 把任一向量按逆时针方向旋转 $\varphi$ 角（由例10可知这个变换是一个线性变换）.

线性变换具有下述基本性质:

(i)  $T0=0, T(-\alpha)=-T\alpha.$
(ii) 若  $\beta=k_{1}\alpha_{1}+k_{2}\alpha_{2}+\cdots+k_{m}\alpha_{m}$ ，则

$$
T \boldsymbol {\beta} = k _ {1} T \boldsymbol {\alpha} _ {1} + k _ {2} T \boldsymbol {\alpha} _ {2} + \dots + k _ {m} T \boldsymbol {\alpha} _ {m}.
$$

(iii) 若  $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{m}$  线性相关，则  $T\alpha_{1}, T\alpha_{2}, \cdots, T\alpha_{m}$  亦线性相关.

这些性质请读者证明之. 注意性质(iii)的逆命题是不成立的, 即当  $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{m}$  线性无关时,  $T\alpha_{1}, T\alpha_{2}, \cdots, T\alpha_{m}$  不一定线性无关.

(iv) 线性变换 T 的像集  $T(V_{n})$  是一个线性空间, 称为线性变换 T 的像空间.

证 设 $\beta_{1},\beta_{2}\in T(V_{n})$ ，则有 $\alpha_{1},\alpha_{2}\in V_{n}$ ，使 $T\pmb{\alpha}_{1} = \pmb{\beta}_{1},T\pmb{\alpha}_{2} = \pmb{\beta}_{2}$ ，从而

$$
\boldsymbol {\beta} _ {1} + \boldsymbol {\beta} _ {2} = T \boldsymbol {\alpha} _ {1} + T \boldsymbol {\alpha} _ {2} = T (\boldsymbol {\alpha} _ {1} + \boldsymbol {\alpha} _ {2}) \in T (V _ {n}) \quad (\text {因} \boldsymbol {\alpha} _ {1} + \boldsymbol {\alpha} _ {2} \in V _ {n}),
$$

$$
\lambda \boldsymbol {\beta} _ {1} = \lambda T \boldsymbol {\alpha} _ {1} = T (\lambda \boldsymbol {\alpha} _ {1}) \in T (V _ {n}) \quad (\text {因} \lambda \boldsymbol {\alpha} _ {1} \in V _ {n}),
$$

由上述证明知它对  $V_{n}$  中的线性运算封闭, 故它是一个线性空间.

证毕

(v) 使 $T\alpha = 0$ 的 $\alpha$ 的全体

152

---

§5 线性变换的矩阵表示式

$$
N _ {T} = \{\alpha \mid \alpha \in V _ {n}, T \alpha = 0 \}
$$

也是一个线性空间. $N_{T}$ 称为线性变换 T 的核.

证 $N_{T} \subseteq V_{n}$, 且易见 $T(\mathbf{0}) = \mathbf{0}$, 故 $\mathbf{0} \in N_{T}, N_{T} \neq \emptyset$.

若  $\alpha_{1},\alpha_{2}\in N_{T}$ ，即  $T\alpha_{1}=0,T\alpha_{2}=0$ ，则  $T(\alpha_{1}+\alpha_{2})=T\alpha_{1}+T\alpha_{2}=0$ ，所以  $\alpha_{1}+\alpha_{2}\in N_{T}$ ;

若  $\alpha_{1}\in N_{T},\lambda\in R$  , 则  $T(\lambda\alpha_{1})=\lambda T\alpha_{1}=\lambda0=0$  , 所以  $\lambda\alpha_{1}\in N_{T}$

以上表明 $N_{T}$ 对 $V_{n}$ 中的线性运算封闭，所以 $N_{T}$ 是一个线性空间. 证毕

例10 设有 $n$ 阶矩阵

$$
\boldsymbol {A} = \left( \begin{array}{c c c c} a _ {1 1} & a _ {1 2} & \dots & a _ {1 n} \\ a _ {2 1} & a _ {2 2} & \dots & a _ {2 n} \\ \vdots & \vdots & & \vdots \\ a _ {n 1} & a _ {n 2} & \dots & a _ {n n} \end{array} \right) = (\boldsymbol {\alpha} _ {1}, \boldsymbol {\alpha} _ {2}, \dots , \boldsymbol {\alpha} _ {n}),
$$

其中

$$
\boldsymbol {\alpha} _ {i} = \left( \begin{array}{c} a _ {1 i} \\ a _ {2 i} \\ \vdots \\ a _ {n i} \end{array} \right),
$$

定义  $R^{n}$  中的变换  $y = T(x)$  为

$$
T (\boldsymbol {x}) = \boldsymbol {A} \boldsymbol {x} \quad (\boldsymbol {x} \in \mathbb {R} ^ {n}),
$$

则 T 为线性变换.

证 设 $a, b \in \mathbb{R}^n$，则

$$
T (\boldsymbol {a} + \boldsymbol {b}) = \boldsymbol {A} (\boldsymbol {a} + \boldsymbol {b}) = \boldsymbol {A} \boldsymbol {a} + \boldsymbol {A} \boldsymbol {b} = T (\boldsymbol {a}) + T (\boldsymbol {b}),
$$

$$
T (\lambda \boldsymbol {a}) = \boldsymbol {A} (\lambda \boldsymbol {a}) = \lambda \boldsymbol {A} \boldsymbol {a} = \lambda T (\boldsymbol {a}).
$$

故 T 是线性变换.

又，T 的像空间就是由  $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{n}$  所生成的向量空间

$$
T (\mathbb {R} ^ {n}) = \{x _ {1} a _ {1} + x _ {2} a _ {2} + \dots + x _ {n} a _ {n} \mid x _ {1}, x _ {2}, \dots , x _ {n} \in \mathbb {R} \},
$$

T 的核  $N_{T}$  就是齐次线性方程组 Ax=0 的解空间.

## § 5 线性变换的矩阵表示式

上节例 10 中, 关系式

$$
T (\boldsymbol {x}) = \boldsymbol {A} \boldsymbol {x} \quad (\boldsymbol {x} \in \mathbb {R} ^ {n})
$$

简单明了地表示出 $\mathbb{R}^n$ 中的一个线性变换. 我们自然希望 $\mathbb{R}^n$ 中任何一个线性变换都能

考研电子书网站:www.pdf2book.com

153

---

\*第6章 线性空间与线性变换

用这样的关系式来表示.为此,考虑到  $\alpha_{1}=Ae_{1},\alpha_{2}=Ae_{2},\cdots,\alpha_{n}=Ae_{n}$  （ $e_{1},e_{2},\cdots,e_{n}$  为单位坐标向量）,即

$$
\boldsymbol {\alpha} _ {i} = T (\boldsymbol {e} _ {i}) \quad (i = 1, 2, \dots , n),
$$

可见如果线性变换 T 有关系式  $T(x)=Ax$ ，那么矩阵 A 应以  $T(e_{i})$  为列向量。反之，如果一个线性变换 T 使  $T(e_{i})=\alpha_{i}\quad(i=1,2,\cdots,n)$ ，那么 T 必有关系式

$$
\begin{array}{l} T (\boldsymbol {x}) = T [ (\boldsymbol {e} _ {1}, \boldsymbol {e} _ {2}, \dots , \boldsymbol {e} _ {n}) \boldsymbol {x} ] = T (x _ {1} \boldsymbol {e} _ {1} + x _ {2} \boldsymbol {e} _ {2} + \dots + x _ {n} \boldsymbol {e} _ {n}). \\ = x _ {1} T (e _ {1}) + x _ {2} T (e _ {2}) + \dots + x _ {n} T (e _ {n}) \\ = (T (\boldsymbol {e} _ {1}), T (\boldsymbol {e} _ {2}), \dots , T (\boldsymbol {e} _ {n})) \boldsymbol {x} = (\boldsymbol {\alpha} _ {1}, \boldsymbol {\alpha} _ {2}, \dots , \boldsymbol {\alpha} _ {n}) \boldsymbol {x} = A \boldsymbol {x}. \\ \end{array}
$$

总之，$\mathbb{R}^n$ 中任何线性变换 $T$ ，都能用关系式

$$
T (\boldsymbol {x}) = \boldsymbol {A} \boldsymbol {x} \quad (\boldsymbol {x} \in \mathbb {R} ^ {n})
$$

表示,其中  $A=(T(\boldsymbol{e}_{1}),T(\boldsymbol{e}_{2}),\cdots,T(\boldsymbol{e}_{n}))$ .

把上面的讨论推广到一般的线性空间,我们有

定义 7 设 T 是线性空间  $V_{n}$  中的线性变换, 在  $V_{n}$  中取定一个基  $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{n}$ , 如果这个基在变换 T 下的像(用这个基线性表示)为

$$
\left\{ \begin{array}{l} T (\boldsymbol {\alpha} _ {1}) = a _ {1 1} \boldsymbol {\alpha} _ {1} + a _ {2 1} \boldsymbol {\alpha} _ {2} + \dots + a _ {n 1} \boldsymbol {\alpha} _ {n}, \\ T (\boldsymbol {\alpha} _ {2}) = a _ {1 2} \boldsymbol {\alpha} _ {1} + a _ {2 2} \boldsymbol {\alpha} _ {2} + \dots + a _ {n 2} \boldsymbol {\alpha} _ {n}, \\ \dots \dots \\ T (\boldsymbol {\alpha} _ {n}) = a _ {1 n} \boldsymbol {\alpha} _ {1} + a _ {2 n} \boldsymbol {\alpha} _ {2} + \dots + a _ {n n} \boldsymbol {\alpha} _ {n}, \end{array} \right.
$$

记  $T(\boldsymbol{\alpha}_{1},\boldsymbol{\alpha}_{2},\cdots,\boldsymbol{\alpha}_{n})=(T(\boldsymbol{\alpha}_{1}),T(\boldsymbol{\alpha}_{2}),\cdots,T(\boldsymbol{\alpha}_{n}))$ ，上式可表示为

$$
T (\alpha_ {1}, \alpha_ {2}, \dots , \alpha_ {n}) = (\alpha_ {1}, \alpha_ {2}, \dots , \alpha_ {n}) A, \tag {5}
$$

其中

$$
\boldsymbol {A} = \left( \begin{array}{c c c c} a _ {1 1} & a _ {1 2} & \dots & a _ {1 n} \\ a _ {2 1} & a _ {2 2} & \dots & a _ {2 n} \\ \vdots & \vdots & & \vdots \\ a _ {n 1} & a _ {n 2} & \dots & a _ {n n} \end{array} \right),
$$

那么 A 就称为线性变换 T 在基  $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{n}$  下的矩阵.

显然,矩阵 A 由基的像  $T(\boldsymbol{\alpha}_{1})$ ,  $T(\boldsymbol{\alpha}_{2})$ ,  $\cdots$ ,  $T(\boldsymbol{\alpha}_{n})$  惟一确定.

如果给出一个矩阵 A 作为线性变换 T 在基  $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{n}$  下的矩阵, 也就是给出了这个基在变换 T 下的像, 那么根据变换 T 保持线性关系的特性, 我们来推导变换 T 必须满足的关系式.

将 $V_{n}$ 中的任意元素记为 $\alpha' = \sum_{i=1}^{n} x_{i} \alpha_{i}$, 有

$$
T \left(\sum_ {i = 1} ^ {n} x _ {i} \pmb {\alpha} _ {i}\right) = \sum_ {i = 1} ^ {n} x _ {i} T (\pmb {\alpha} _ {i})
$$

154

---

§ 5 线性变换的矩阵表示式

$$
= (T (\boldsymbol {\alpha} _ {1}), T (\boldsymbol {\alpha} _ {2}), \dots , T (\boldsymbol {\alpha} _ {n})) \left( \begin{array}{c} x _ {1} \\ x _ {2} \\ \vdots \\ x _ {n} \end{array} \right) = (\boldsymbol {\alpha} _ {1}, \boldsymbol {\alpha} _ {2}, \dots , \boldsymbol {\alpha} _ {n}) A \left( \begin{array}{c} x _ {1} \\ x _ {2} \\ \vdots \\ x _ {n} \end{array} \right),
$$

即

$$
T \left[ (\boldsymbol {\alpha} _ {1}, \boldsymbol {\alpha} _ {2}, \dots , \boldsymbol {\alpha} _ {n}) \left( \begin{array}{c} x _ {1} \\ x _ {2} \\ \vdots \\ x _ {n} \end{array} \right) \right] = (\boldsymbol {\alpha} _ {1}, \boldsymbol {\alpha} _ {2}, \dots , \boldsymbol {\alpha} _ {n}) A \left( \begin{array}{c} x _ {1} \\ x _ {2} \\ \vdots \\ x _ {n} \end{array} \right). \tag {6}
$$

这个关系式惟一地确定一个变换 $T$，可以验证所确定的变换 $T$ 是以 $\pmb{A}$ 为矩阵的线性变换。总之，以 $\pmb{A}$ 为矩阵的线性变换 $T$ 由关系式(6)惟一确定。

定义7和上面一段讨论表明,在 $V_{n}$ 中取定一个基以后,由线性变换 $T$ 可惟一地确定一个矩阵 $\pmb{A}$, 由一个矩阵 $\pmb{A}$ 也可惟一地确定一个线性变换 $T$, 这样, 在线性变换与矩阵之间就有一一对应的关系.

由关系式(6)，可见若  $\alpha$  在基  $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{n}$  下的坐标为

$$
\boldsymbol {x} = \left( \begin{array}{c} x _ {1} \\ x _ {2} \\ \vdots \\ x _ {n} \end{array} \right),
$$

则  $T(\boldsymbol{\alpha})$  在基  $\alpha_{1},\alpha_{2},\cdots,\alpha_{n}$  下的坐标就为  $Ax=A\begin{pmatrix}x_{1}\\x_{2}\\\vdots\\x_{n}\end{pmatrix}$ .

例11 在 $P[x]_3$ 中, 取基

$$
\boldsymbol {p} _ {1} = x ^ {3}, \quad \boldsymbol {p} _ {2} = x ^ {2}, \quad \boldsymbol {p} _ {3} = x, \quad \boldsymbol {p} _ {4} = 1,
$$

求微分运算 D 的矩阵.

解

$$
\left\{ \begin{array}{l} \mathrm{D} \boldsymbol {p} _ {1} = 3 x ^ {2} = 0 \boldsymbol {p} _ {1} + 3 \boldsymbol {p} _ {2} + 0 \boldsymbol {p} _ {3} + 0 \boldsymbol {p} _ {4}, \\ \mathrm{D} \boldsymbol {p} _ {2} = 2 x = 0 \boldsymbol {p} _ {1} + 0 \boldsymbol {p} _ {2} + 2 \boldsymbol {p} _ {3} + 0 \boldsymbol {p} _ {4}, \\ \mathrm{D} \boldsymbol {p} _ {3} = 1 = 0 \boldsymbol {p} _ {1} + 0 \boldsymbol {p} _ {2} + 0 \boldsymbol {p} _ {3} + 1 \boldsymbol {p} _ {4}, \\ \mathrm{D} \boldsymbol {p} _ {4} = 0 = 0 \boldsymbol {p} _ {1} + 0 \boldsymbol {p} _ {2} + 0 \boldsymbol {p} _ {3} + 0 \boldsymbol {p} _ {4}, \end{array} \right.
$$

所以D在这组基下的矩阵为

考研电子书网站:www.pdf2book.com

155

---

\*第6章 线性空间与线性变换

$$
\boldsymbol {A} = \left( \begin{array}{c c c c} 0 & 0 & 0 & 0 \\ 3 & 0 & 0 & 0 \\ 0 & 2 & 0 & 0 \\ \dot {0} & 0 & 1 & 0 \end{array} \right).
$$

例12 在 $\mathbb{R}^3$ 中, $T$ 表示将向量投影到 $xOy$ 平面的线性变换, 即

$$
T (x i + y j + z k) = x i + y j.
$$

(1) 取基为 i, j, k, 求 T 的矩阵;
(2) 取基为  $\alpha=i,\beta=j,\gamma=i+j+k$ ，求 T 的矩阵.

解 (1) $\left\{ \begin{array}{l}Ti = i,\\ Tj = j,\\ Tk = 0, \end{array} \right.$

即

$$
T (\boldsymbol {i}, \boldsymbol {j}, \boldsymbol {k}) = (\boldsymbol {i}, \boldsymbol {j}, \boldsymbol {k}) \left( \begin{array}{c c c} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 0 \end{array} \right).
$$

(2) $\left\{ \begin{array}{l} T\alpha = i = \alpha, \\ T\beta = j = \beta, \\ T\gamma = i + j = \alpha + \beta, \end{array} \right.$

即

$$
T (\boldsymbol {\alpha}, \boldsymbol {\beta}, \boldsymbol {\gamma}) = (\boldsymbol {\alpha}, \boldsymbol {\beta}, \boldsymbol {\gamma}) \left( \begin{array}{c c c} 1 & 0 & 1 \\ 0 & 1 & 1 \\ 0 & 0 & 0 \end{array} \right).
$$

由上例可见,同一个线性变换在不同的基下有不同的矩阵.一般地,我们有

定理 3 设线性空间  $V_{n}$  中取定两个基

$$
\alpha_ {1}, \alpha_ {2}, \dots , \alpha_ {n}; \quad \beta_ {1}, \beta_ {2}, \dots , \beta_ {n},
$$

由基  $\alpha_{1},\alpha_{2},\cdots,\alpha_{n}$  到基  $\beta_{1},\beta_{2},\cdots,\beta_{n}$  的过渡矩阵为 P, $V_{n}$  中的线性变换 T 在这两个基下的矩阵依次为 A 和 B，那么  $B=P^{-1}AP$ .

证 按定理的假设,有

$$
(\boldsymbol {\beta} _ {1}, \boldsymbol {\beta} _ {2}, \dots , \boldsymbol {\beta} _ {n}) = (\boldsymbol {\alpha} _ {1}, \boldsymbol {\alpha} _ {2}, \dots , \boldsymbol {\alpha} _ {n}) \boldsymbol {P},
$$

$\pmb{P}$ 可逆;及

$$
\begin{array}{l} T (\boldsymbol {\alpha} _ {1}, \boldsymbol {\alpha} _ {2}, \dots , \boldsymbol {\alpha} _ {n}) = (\boldsymbol {\alpha} _ {1}, \boldsymbol {\alpha} _ {2}, \dots , \boldsymbol {\alpha} _ {n}) \boldsymbol {A}, \\ T (\boldsymbol {\beta} _ {1}, \boldsymbol {\beta} _ {2}, \dots , \boldsymbol {\beta} _ {n}) = (\boldsymbol {\beta} _ {1}, \boldsymbol {\beta} _ {2}, \dots , \boldsymbol {\beta} _ {n}) \boldsymbol {B}, \\ \end{array}
$$

于是

$$
(\boldsymbol {\beta} _ {1}, \boldsymbol {\beta} _ {2}, \dots , \boldsymbol {\beta} _ {n}) \boldsymbol {B} = T (\boldsymbol {\beta} _ {1}, \boldsymbol {\beta} _ {2}, \dots , \boldsymbol {\beta} _ {n}) = T [ (\boldsymbol {\alpha} _ {1}, \boldsymbol {\alpha} _ {2}, \dots , \boldsymbol {\alpha} _ {n}) \boldsymbol {P} ]
$$

156

---

习题六

$$
\begin{array}{l} = \left[ T \left(\alpha_ {1}, \alpha_ {2}, \dots , \alpha_ {n}\right) \right] P = \left(\alpha_ {1}, \alpha_ {2}, \dots , \alpha_ {n}\right) A P \\ = (\boldsymbol {\beta} _ {1}, \boldsymbol {\beta} _ {2}, \dots , \boldsymbol {\beta} _ {n}) \boldsymbol {P} ^ {- 1} \boldsymbol {A} \boldsymbol {P}, \\ \end{array}
$$

因为 $\beta_{1},\beta_{2},\cdots,\beta_{n}$ 线性无关,所以

$$
\boldsymbol {B} = \boldsymbol {P} ^ {- 1} \boldsymbol {A} \boldsymbol {P}.
$$

证毕

这定理表明 A 与 B 相似,且两个基之间的过渡矩阵 P 就是相似变换矩阵.

例 13 设  $V_{2}$  中的线性变换 T 在基  $\alpha_{1}, \alpha_{2}$  下的矩阵为

$$
\boldsymbol {A} = \left( \begin{array}{c c} a _ {1 1} & a _ {1 2} \\ a _ {2 1} & a _ {2 2} \end{array} \right),
$$

求 T 在基  $\alpha_{2}, \alpha_{1}$  下的矩阵.

解  $(\boldsymbol{\alpha}_{2},\boldsymbol{\alpha}_{1})=(\boldsymbol{\alpha}_{1},\boldsymbol{\alpha}_{2})\begin{pmatrix}0&1\\1&0\end{pmatrix},$

即  $P=\begin{pmatrix}0&1\\ 1&0\end{pmatrix}$ ，求得  $P^{-1}=\begin{pmatrix}0&1\\ 1&0\end{pmatrix}$ ，于是 T 在基  $(\boldsymbol{\alpha}_{2},\boldsymbol{\alpha}_{1})$  下的矩阵为

$$
\boldsymbol {B} = \left( \begin{array}{c c} 0 & 1 \\ 1 & 0 \end{array} \right) \left( \begin{array}{c c} a _ {1 1} & a _ {1 2} \\ a _ {2 1} & a _ {2 2} \end{array} \right) \left( \begin{array}{c c} 0 & 1 \\ 1 & 0 \end{array} \right) = \left( \begin{array}{c c} a _ {2 1} & a _ {2 2} \\ a _ {1 1} & a _ {1 2} \end{array} \right) \left( \begin{array}{c c} 0 & 1 \\ 1 & 0 \end{array} \right) = \left( \begin{array}{c c} a _ {2 2} & a _ {2 1} \\ a _ {1 2} & a _ {1 1} \end{array} \right).
$$

定义 8 线性变换 T 的像空间  $T(V_{n})$  的维数, 称为线性变换 T 的秩.

显然,若 A 是 T 的矩阵,则 T 的秩就是  $R(A)$ .

若 T 的秩为 r，则 T 的核  $N_{T}$  的维数为 n-r.

## 习题六

1. 验证:

(1) 2 阶矩阵的全体  $S_{1}$ ;
(2) 主对角线上的元素之和等于 0 的 2 阶矩阵的全体  $S_{2}$ ;
(3) 2 阶对称矩阵的全体  $S_{3}$ ,

对于矩阵的加法和数乘运算构成线性空间,并写出各个空间的一个基.

2. 验证: 与向量 $(0,0,1)^{T}$ 不平行的全体3维数组向量, 对于数组向量的加法和数乘运算不构成线性空间.

3. 在线性空间 $P[x]_3$ 中, 下列向量组是否为一个基?

(1) I:  $1 + x, x + x^{2}, 1 + x^{3}, 2 + 2x + x^{2} + x^{3}$ ;
(2) Ⅱ:  $-1+x,1-x^{2},-2+2x+x^{2},x^{3}.$

4. 在  $R^{3}$  中求向量  $\boldsymbol{\alpha}=(7,3,1)^{\mathrm{T}}$  在基

$$
\boldsymbol {\alpha} _ {1} = (1, 3, 5) ^ {\mathrm{T}}, \quad \boldsymbol {\alpha} _ {2} = (6, 3, 2) ^ {\mathrm{T}}, \quad \boldsymbol {\alpha} _ {3} = (3, 1, 0) ^ {\mathrm{T}}
$$

深入探究

157

---

\*第6章 线性空间与线性变换

中的坐标.

5. 在 $\mathbb{R}^3$ 中, 取两个基

$$
\boldsymbol {\alpha} _ {1} = (1, 2, 1) ^ {\mathrm{T}}, \quad \boldsymbol {\alpha} _ {2} = (2, 3, 3) ^ {\mathrm{T}}, \quad \boldsymbol {\alpha} _ {3} = (3, 7, - 2) ^ {\mathrm{T}};
$$

$$
\boldsymbol {\beta} _ {1} = (3, 1, 4) ^ {\mathrm{T}}, \quad \boldsymbol {\beta} _ {2} = (5, 2, 1) ^ {\mathrm{T}}, \quad \boldsymbol {\beta} _ {3} = (1, 1, - 6) ^ {\mathrm{T}},
$$

试求坐标变换公式.

6. 在 $\mathbb{R}^4$ 中取两个基

$$
\left\{ \begin{array}{l} \boldsymbol {e} _ {1} = (1, 0, 0, 0) ^ {\mathrm{T}}, \\ \boldsymbol {e} _ {2} = (0, 1, 0, 0) ^ {\mathrm{T}}, \\ \boldsymbol {e} _ {3} = (0, 0, 1, 0) ^ {\mathrm{T}}, \\ \boldsymbol {e} _ {4} = (0, 0, 0, 1) ^ {\mathrm{T}}, \end{array} \right. \quad \left\{ \begin{array}{l} \boldsymbol {\alpha} _ {1} = (2, 1, - 1, 1) ^ {\mathrm{T}}, \\ \boldsymbol {\alpha} _ {2} = (0, 3, 1, 0) ^ {\mathrm{T}}, \\ \boldsymbol {\alpha} _ {3} = (5, 3, 2, 1) ^ {\mathrm{T}}, \\ \boldsymbol {\alpha} _ {4} = (6, 6, 1, 3) ^ {\mathrm{T}}. \end{array} \right.
$$

(1) 求由前一个基到后一个基的过渡矩阵；
(2) 求向量 $(x_{1}, x_{2}, x_{3}, x_{4})^{T}$ 在后一个基中的坐标；
(3) 求在两个基中有相同坐标的向量.

7. 设线性空间 $S_{1}$ （习题六第1题(1))中向量

$$
\boldsymbol {a} _ {1} = \left( \begin{array}{c c} 1 & 2 \\ 1 & 0 \end{array} \right), \quad \boldsymbol {a} _ {2} = \left( \begin{array}{c c} - 1 & - 1 \\ 1 & 1 \end{array} \right), \quad \boldsymbol {b} _ {1} = \left( \begin{array}{c c} 1 & 3 \\ 3 & 1 \end{array} \right), \quad \boldsymbol {b} _ {2} = \left( \begin{array}{c c} 2 & - 1 \\ 4 & 1 \end{array} \right),
$$

(1) 问  $b_{1}$  能否由  $a_{1}, a_{2}$  线性表示？ $b_{2}$  能否由  $a_{1}, a_{2}$  线性表示？
(2) 求由向量组  $a_{1}, a_{2}, b_{1}, b_{2}$  所生成的向量空间 L 的维数和一个基.

8. 说明 $xOy$ 平面上变换 $T\begin{pmatrix} x \\ y \end{pmatrix} = A\begin{pmatrix} x \\ y \end{pmatrix}$ 的几何意义, 其中

(1)  $A = \begin{pmatrix} -1 & 0 \\ 0 & 1 \end{pmatrix};$

(2)  $A = \begin{pmatrix} 0 & 0 \\ 0 & 1 \end{pmatrix}$ ;

(3)  $A = \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix}$ ;

(4)  $A=\begin{pmatrix}0&1\\-1&0\end{pmatrix}.$

9. $n$ 阶对称矩阵的全体 $V$ 对于矩阵的线性运算构成一个 $\frac{n(n + 1)}{2}$ 维线性空间. 给出 $n$ 阶可逆矩阵 $P$, 以 $A$ 表示 $V$ 中的任一元素, 试证合同变换

$$
T (\boldsymbol {A}) = \boldsymbol {P} ^ {\mathrm{T}} \boldsymbol {A} \boldsymbol {P}
$$

是 V 中的线性变换.

10. 函数集合

$$
V _ {3} = \left\{\left(a _ {2} x ^ {2} + a _ {1} x + a _ {0}\right) \mathrm{e} ^ {x} \mid a _ {2}, a _ {1}, a _ {0} \in \mathbb {R} \right\}
$$

对于函数的线性运算构成3维线性空间.在 $V_{3}$ 中取一个基

$$
\alpha_ {1} = x ^ {2} \mathrm{e} ^ {x}, \quad \alpha_ {2} = x \mathrm{e} ^ {x}, \quad \alpha_ {3} = \mathrm{e} ^ {x},
$$

求微分运算 D 在这个基下的矩阵.

11.2 阶对称矩阵的全体

$$
V _ {3} = \left\{\left( \begin{array}{c c} x _ {1} & x _ {2} \\ x _ {2} & x _ {3} \end{array} \right) \Bigg | x _ {1}, x _ {2}, x _ {3} \in \mathbb {R} \right\}
$$

对于矩阵的线性运算构成3维线性空间.在 $V_{3}$ 中取一个基

158

---

习题六

$$
\boldsymbol {A} _ {1} = \left( \begin{array}{c c} 1 & 0 \\ 0 & 0 \end{array} \right), \quad \boldsymbol {A} _ {2} = \left( \begin{array}{c c} 0 & 1 \\ 1 & 0 \end{array} \right), \quad \boldsymbol {A} _ {3} = \left( \begin{array}{c c} 0 & 0 \\ 0 & 1 \end{array} \right),
$$

在 $V_{3}$ 中定义合同变换

$$
T (\boldsymbol {A}) = \left( \begin{array}{c c} 1 & 0 \\ 1 & 1 \end{array} \right) \boldsymbol {A} \left( \begin{array}{c c} 1 & 1 \\ 0 & 1 \end{array} \right),
$$

求 T 在基  $A_{1}, A_{2}, A_{3}$  下的矩阵.

12. 次数不超过 2 的全体实系数多项式对于多项式的线性运算构成一个线性空间 $V$. 在 $V$ 上定义变换 $T(a_0 + a_1x + a_2x^2) = \left(a_0 + \frac{1}{2}a_2\right) + \left(a_1 - \frac{1}{2}a_2\right)x + \frac{1}{2}a_2x^2$.

(1) 试证 T 是 V 中的线性变换；
(2) 求 T 在基  $1, x, x^{2}$  下的矩阵；
(3) 设 W 为 V 的子空间, 且满足对任意  $p(x) \in W$ , 总有  $T(p(x)) = p(x)$ , 求子空间 W 的维数的最大值.
13. 已知 n 维线性空间 V 中的线性变换 T 在 V 的某个基  $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{n}$  下的矩阵为 A，若  $A^{2} = A$ ，证明:存在线性空间 V 的一个基  $\beta_{1}, \beta_{2}, \cdots, \beta_{n}$ ，使得 T 在这个基下的矩阵为对角矩阵.

考研电子书网站:www.pdf2book.com

159
