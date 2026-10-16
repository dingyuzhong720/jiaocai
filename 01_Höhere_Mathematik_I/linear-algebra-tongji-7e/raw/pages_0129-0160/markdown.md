在第2章中我们曾得出结论: 若  $A = PBP^{-1}$ ，则  $A^{k} = PB^{k}P^{-1}.A$  的多项式

$$
\varphi (A) = P \varphi (B) P ^ {- 1}.
$$

特别地,若有可逆矩阵 P 使  $P^{-1}AP=\Lambda$  为对角矩阵,即若 A 相似于对角矩阵  $\Lambda$ ,则

$$
A ^ {k} = P \Lambda^ {k} P ^ {- 1}, \quad \varphi (A) = P \varphi (\Lambda) P ^ {- 1}.
$$

而对于对角矩阵 $\Lambda$ ，有

$$
\boldsymbol {\Lambda} ^ {k} = \left( \begin{array}{c c c c} \lambda_ {1} ^ {k} & & & \\ & \lambda_ {2} ^ {k} & & \\ & & \ddots & \\ & & & \lambda_ {n} ^ {k} \end{array} \right), \quad \varphi (\boldsymbol {\Lambda}) = \left( \begin{array}{c c c c} \varphi (\lambda_ {1}) & & & \\ & \varphi (\lambda_ {2}) & & \\ & & \ddots & \\ & & & \varphi (\lambda_ {n}) \end{array} \right),
$$

由此可方便地计算 A 的多项式  $\varphi(A)$ .

下面我们要讨论的主要问题是: 对 n 阶矩阵 A, 是否存在相似变换矩阵 P, 使  $P^{-1}AP = \Lambda$  为对角矩阵, 如果这样的 P 存在, 则称矩阵 A 可对角化.

假设已经找到可逆矩阵 $P$，使 $P^{-1}AP = \Lambda$ 为对角矩阵。把 $P$ 用其列向量表示为

$$
\boldsymbol {P} = (\boldsymbol {p} _ {1}, \boldsymbol {p} _ {2}, \dots , \boldsymbol {p} _ {n}),
$$

由 $P^{-1}AP = \Lambda$ ，得 $AP = P\Lambda$ ，即

$$
A (\boldsymbol {p} _ {1}, \boldsymbol {p} _ {2}, \dots , \boldsymbol {p} _ {n}) = (\boldsymbol {p} _ {1}, \boldsymbol {p} _ {2}, \dots , \boldsymbol {p} _ {n}) \left( \begin{array}{c c c c} \lambda_ {1} & & & \\ & \lambda_ {2} & & \\ & & \ddots & \\ & & & \lambda_ {n} \end{array} \right) = (\lambda_ {1} \boldsymbol {p} _ {1}, \lambda_ {2} \boldsymbol {p} _ {2}, \dots , \lambda_ {n} \boldsymbol {p} _ {n}),
$$

于是有

$$
A p _ {i} = \lambda_ {i} p _ {i} \quad (i = 1, 2, \dots , n).
$$

可见  $\lambda_{i}$  是 A 的特征值, 而 P 的列向量  $p_{i}$  就是 A 的对应于特征值  $\lambda_{i}$  的特征向量. 由于 P 可逆, 所以 A 有 n 个线性无关的特征向量  $p_{1}, p_{2}, \cdots, p_{n}$ .

反之, 若 A 有 n 个线性无关的特征向量  $p_{1}, p_{2}, \cdots, p_{n}$ ，其中  $p_{i}$  对应于特征值  $\lambda_{i}$ ，则矩阵  $P = (p_{1}, p_{2}, \cdots, p_{n})$  可逆，且 AP = PA，这里  $\Lambda = \text{diag}(\lambda_{1}, \lambda_{2}, \cdots, \lambda_{n})$ 。于是  $P^{-1}AP = \Lambda$ ，即 A 与对角矩阵相似。

由上面的讨论即有

定理 4 n 阶矩阵 A 与对角矩阵相似（即 A 可对角化）的充分必要条件是 A 有 n 个线性无关的特征向量.

联系定理 2, 可得

推论 如果 $n$ 阶矩阵 $\pmb{A}$ 的 $n$ 个特征值互不相等, 则 $\pmb{A}$ 与对角矩阵相似.

当 A 的特征方程有重根时, 就不一定有 n 个线性无关的特征向量, 从而不一定能对角化.例如在例6中 $\pmb{A}$ 的特征方程有重根，确实找不到3个线性无关的特征向量，因此例6中的 $\pmb{A}$ 不可对角化.

例10 设矩阵

$$
\boldsymbol {A} = \left( \begin{array}{c c c} - 2 & 1 & 1 \\ 0 & 2 & 0 \\ - 4 & 1 & 3 \end{array} \right),
$$

问 A 能否对角化？若能，则求可逆矩阵 P 和对角矩阵  $\Lambda$ ，使  $P^{-1}AP = \Lambda$ .

解 先求 A 的特征值.

$$
\begin{array}{l} \left| \boldsymbol {A} - \lambda \boldsymbol {E} \right| = \left| \begin{array}{c c c} - 2 - \lambda & 1 & 1 \\ 0 & 2 - \lambda & 0 \\ - 4 & 1. & 3 - \lambda \end{array} \right| = (2 - \lambda) \left| \begin{array}{c c} - 2 - \lambda & 1 \\ - 4 & 3 - \lambda \end{array} \right| \\ = (2 - \lambda) (\lambda^ {2} - \lambda - 2) = - (\lambda + 1) (\lambda - 2) ^ {2}, \\ \end{array}
$$

所以 A 的特征值为  $\lambda_{1} = -1, \lambda_{2} = \lambda_{3} = 2.$

再求 A 的特征向量.

当  $\lambda_{1}=-1$  时, 解方程  $(A+E)x=0$ . 由

$$
\boldsymbol {A} + \boldsymbol {E} = \left( \begin{array}{c c c} - 1 & 1 & 1 \\ 0 & 3 & 0 \\ - 4 & 1 & 4 \end{array} \right) \stackrel {{r}} {{\sim}} \left( \begin{array}{c c c} 1 & 0 & - 1 \\ 0 & 1 & 0 \\ 0 & 0 & 0 \end{array} \right),
$$

得对应的特征向量

$$
\boldsymbol {p} _ {1} = \left( \begin{array}{c} 1 \\ 0 \\ 1 \end{array} \right);
$$

当 $\lambda_{2} = \lambda_{3} = 2$ 时，解方程 $(A - 2E)x = 0.$ 由

$$
\boldsymbol {A} - 2 \boldsymbol {E} = \left( \begin{array}{c c c} {- 4} & {1} & {1} \\ {0} & {0} & {0} \\ {- 4} & {1} & {1} \end{array} \right) \stackrel {{r}} {{\sim}} \left( \begin{array}{c c c} {- 4} & {1} & {1} \\ {0} & {0} & {0} \\ {0} & {0} & {0} \end{array} \right),
$$

得对应的线性无关特征向量

$$
\boldsymbol {p} _ {2} = \left( \begin{array}{c} 0 \\ 1 \\ - 1 \end{array} \right), \quad \boldsymbol {p} _ {3} = \left( \begin{array}{c} 1 \\ 0 \\ 4 \end{array} \right).
$$

由定理2的推论,知 $p_{1},p_{2},p_{3}$ 线性无关,再由定理4知A可对角化;并且若记

$$
\boldsymbol {P} = (\boldsymbol {p} _ {1}, \boldsymbol {p} _ {2}, \boldsymbol {p} _ {3}) = \left( \begin{array}{c c c} 1 & 0 & 1 \\ 0 & 1 & 0 \\ 1 & - 1 & 4 \end{array} \right),
$$

则有

$$
P ^ {- 1} A P = \mathrm{diag} (- 1, 2, 2).
$$

要注意上式中对角矩阵的对角元的排列次序应与 P 中列向量的排列次序一致.

例11 设

$$
\boldsymbol {A} = \left( \begin{array}{c c c} 0 & 0 & 1 \\ 1 & 1 & t \\ 1 & 0 & 0 \end{array} \right),
$$

问 $t$ 为何值时, 矩阵 $\pmb{A}$ 可对角化?

解 由

$$
\left| \boldsymbol {A} - \lambda \boldsymbol {E} \right| = \left| \begin{array}{c c c} - \lambda & 0 & 1 \\ 1 & 1 - \lambda & t \\ 1 & 0 & - \lambda \end{array} \right| = (1 - \lambda) \left| \begin{array}{c c} - \lambda & 1 \\ 1 & - \lambda \end{array} \right| = - (\lambda - 1) ^ {2} (\lambda + 1),
$$

得 $\lambda_{1} = -1, \lambda_{2} = \lambda_{3} = 1$.

当单根 $\lambda_{1} = -1$ 时, 可求得线性无关的特征向量恰有 1 个, 故矩阵 $A$ 可对角化的充分必要条件是对应重根 $\lambda_{2} = \lambda_{3} = 1$, 有 2 个线性无关的特征向量, 即方程 $(A - E)x = 0$ 有 2 个线性无关的解, 亦即系数矩阵 $A - E$ 的秩 $R(A - E) = 1$. 由

$$
\boldsymbol {A} - \boldsymbol {E} = \left( \begin{array}{c c c} {- 1} & {0} & {1} \\ {1} & {0} & {t} \\ {1} & {0} & {- 1} \end{array} \right) \stackrel {{r}} {{\sim}} \left( \begin{array}{c c c} {1} & {0} & {- 1} \\ {0} & {0} & {t + 1} \\ {0} & {0} & {0} \end{array} \right),
$$

要 $R(A - E) = 1$ ，得 $t + 1 = 0$ ，即 $t = -1$

因此, 当 t = -1 时, 矩阵 A 可对角化.

## § 4 对称矩阵的对角化

一个 $n$ 阶矩阵具备什么条件才能有 $n$ 个线性无关的特征向量, 从而可对角化? 这是一个较复杂的问题. 我们对此不进行一般性的讨论, 而仅讨论当 $\pmb{A}$ 为对称矩阵的情形.

先介绍两个关于对称矩阵的特征值和特征向量的性质.

## 性质 1 对称矩阵的特征值为实数.

证 先介绍一个记号. 设复数矩阵 $X = (x_{ij}), \overline{x}_{ij}$ 为 $x_{ij}$ 的共轭复数, 记 $\overline{X} = (\overline{x}_{ij})$, 即 $\overline{X}$ 是由 $X$ 的对应元素的共轭复数构成的矩阵.

设复数  $\lambda$  为对称矩阵 A 的特征值, 复向量 x 为对应的特征向量, 即  $Ax = \lambda x, x \neq 0$ .

用 $\overline{\lambda}$ 表示 $\lambda$ 的共轭复数, 而 $A$ 为实矩阵, 有 $A = \overline{A}$, 故 $A\overline{x} = \overline{A}\overline{x} = \overline{Ax} = \overline{\lambda x} = \overline{\lambda}\overline{x}$. 于是有

$$
\overline {{x}} ^ {\mathrm{T}} A x = \overline {{x}} ^ {\mathrm{T}} (A x) = \overline {{x}} ^ {\mathrm{T}} \lambda x = \lambda \overline {{x}} ^ {\mathrm{T}} x
$$

及

$$
\overline {{x}} ^ {\mathrm{T}} A x = (\overline {{x}} ^ {\mathrm{T}} A ^ {\mathrm{T}}) x = (A \overline {{x}}) ^ {\mathrm{T}} x = (\overline {{\lambda}} \overline {{x}}) ^ {\mathrm{T}} x = \overline {{\lambda}} \overline {{x}} ^ {\mathrm{T}} x,
$$

两式相减, 得

$$
(\lambda - \overline {{\lambda}}) \overline {{x}} ^ {\mathrm{T}} x = 0,
$$

但因 $x \neq 0$，所以

$$
\overline {{x}} ^ {\mathrm{T}} x = \sum_ {i = 1} ^ {n} \overline {{x}} _ {i} x _ {i} = \sum_ {i = 1} ^ {n} \left| x _ {i} \right| ^ {2} \neq 0,
$$

故 $\lambda -\overline{\lambda} = 0$ ，即 $\lambda = \overline{\lambda}$ ，这就说明 $\lambda$ 是实数.

证毕

显然,当特征值  $\lambda_{i}$  为实数时,齐次线性方程组

$$
(A - \lambda_ {i} E) x = 0
$$

是实系数方程组, 由  $\left|A-\lambda_{i}E\right|=0$  知必有实的基础解系, 所以对应的特征向量可以取实向量.

性质2 设 $\lambda_{1}, \lambda_{2}$ 是对称矩阵 $A$ 的两个特征值, $p_{1}, p_{2}$ 是对应的特征向量. 若 $\lambda_{1} \neq \lambda_{2}$, 则 $p_{1}$ 与 $p_{2}$ 正交.

证 $\lambda_{1}p_{1} = Ap_{1},\lambda_{2}p_{2} = Ap_{2},\lambda_{1}\neq \lambda_{2}.$

因 $\mathbf{A}$ 为对称矩阵，故 $\lambda_1\pmb{p}_1^{\mathrm{T}} = (\lambda_1\pmb{p}_1)^{\mathrm{T}} = (\pmb {A}\pmb{p}_1)^{\mathrm{T}} = \pmb{p}_1^{\mathrm{T}}\pmb{A}^{\mathrm{T}} = \pmb{p}_1^{\mathrm{T}}\pmb{A}$，于是

$$
\lambda_ {1} \boldsymbol {p} _ {1} ^ {\mathrm{T}} \boldsymbol {p} _ {2} = \boldsymbol {p} _ {1} ^ {\mathrm{T}} \boldsymbol {A} \boldsymbol {p} _ {2} = \boldsymbol {p} _ {1} ^ {\mathrm{T}} (\lambda_ {2} \boldsymbol {p} _ {2}) = \lambda_ {2} \boldsymbol {p} _ {1} ^ {\mathrm{T}} \boldsymbol {p} _ {2},
$$

即

$$
(\lambda_ {1} - \lambda_ {2}) \boldsymbol {p} _ {1} ^ {\mathrm{T}} \boldsymbol {p} _ {2} = 0.
$$

但 $\lambda_1 \neq \lambda_2$，故 $p_1^T p_2 = 0$，即 $p_1$ 与 $p_2$ 正交。

证毕

定理5 设 $A$ 为 $n$ 阶对称矩阵, 则必有正交矩阵 $P$, 使 $P^{-1}AP = P^{\mathrm{T}}AP = A$, 其中 $\Lambda$ 是以 $A$ 的 $n$ 个特征值为对角元的对角矩阵.

此定理不予证明.

性质3 设 $A$ 为 $n$ 阶对称矩阵, $\lambda$ 是 $A$ 的特征方程的 $k$ 重根, 则矩阵 $A - \lambda E$ 的秩 $R(A - \lambda E) = n - k$, 从而对应特征值 $\lambda$ 恰有 $k$ 个线性无关的特征向量.

证 按定理 5 知对称矩阵 A 与对角矩阵  $\boldsymbol{\Lambda}=\mathrm{diag}(\lambda_{1},\lambda_{2},\cdots,\lambda_{n})$  相似，从而  $A-\lambda E$  与  $\boldsymbol{\Lambda}-\lambda E=\mathrm{diag}(\lambda_{1}-\lambda,\lambda_{2}-\lambda,\cdots,\lambda_{n}-\lambda)$  相似。当  $\lambda$  是 A 的 k 重特征根时， $\lambda_{1},\lambda_{2},\cdots,\lambda_{n}$  这 n 个特征值中有 k 个等于  $\lambda'$ ，有 n-k 个不等于  $\lambda$ ，从而对角矩阵  $A-\lambda E$  的对角元恰有 k 个等于 0，于是  $R(\boldsymbol{\Lambda}-\lambda\boldsymbol{E})=n-k$ 。而  $R(\boldsymbol{A}-\lambda\boldsymbol{E})=R(\boldsymbol{\Lambda}-\lambda\boldsymbol{E})$ ，所以  $R(\boldsymbol{A}-\lambda\boldsymbol{E})=n-k$ 。

证毕

依据定理5及性质3,我们有下述把 $n$ 阶对称矩阵 $\pmb{A}$ 对角化的步骤:

(i) 求出 A 的全部互不相等的特征值  $\lambda_{1}, \lambda_{2}, \cdots, \lambda_{s}$ ，它们的重数依次为  $k_{1}, k_{2}, \cdots, k_{s}$  ( $k_{1} + k_{2} + \cdots + k_{s} = n$ ).

（ii）对每个 $k_{i}$ 重特征值 $\lambda_{i}$，求方程 $(A - \lambda_{i}E)x = 0$ 的基础解系，得 $k_{i}$ 个线性无关的特征向量。再把它们正交化、单位化，得 $k_{i}$ 个两两正交的单位特征向量。因 $k_{1} + k_{2} + \dots + k_{s} = n$，故总共可得 $n$ 个两两正交的单位特征向量。

（iii）把这 $n$ 个两两正交的单位特征向量构成正交矩阵 $\pmb{P}$，便有 $\pmb{P}^{-1}\pmb{A}\pmb{P} = \pmb{P}^{\mathrm{T}}\pmb{A}\pmb{P} = \pmb{\Lambda}$. 注意 $\pmb{\Lambda}$ 中对角元的排列次序应与 $\pmb{P}$ 中列向量的排列次序相对应.

例12 设

$$
\boldsymbol {A} = \left( \begin{array}{c c c} 0 & - 1 & 1 \\ - 1 & 0 & 1 \\ 1 & 1 & 0 \end{array} \right),
$$

求一个正交矩阵 P, 使  $P^{-1}AP = \Lambda$  为对角矩阵.

解 由

$$
\begin{array}{l} \left| \boldsymbol {A} - \lambda \boldsymbol {E} \right| = \left| \begin{array}{r r r} - \lambda & - 1 & 1 \\ - 1 & - \lambda & 1 \\ 1 & 1 & - \lambda \end{array} \right| \stackrel {{r _ {1} - r _ {2}}} {{=}} \left| \begin{array}{c c c} 1 - \lambda & \lambda - 1 & 0 \\ - 1 & - \lambda & 1 \\ 1 & 1 & - \lambda \end{array} \right| \stackrel {{c _ {2} + c _ {1}}} {{=}} \left| \begin{array}{c c c} 1 - \lambda & 0 & 0 \\ - 1 & - 1 - \lambda & 1 \\ 1 & 2 & - \lambda \end{array} \right| \\ = (1 - \lambda) (\lambda^ {2} + \lambda - 2) = - (\lambda - 1) ^ {2} (\lambda + 2), \\ \end{array}
$$

求得 A 的特征值为  $\lambda_{1} = -2, \lambda_{2} = \lambda_{3} = 1$ .

对应 $\lambda_{1} = -2$ ，解方程 $(A + 2E)x = 0$ ，由

$$
\boldsymbol {A} + 2 \boldsymbol {E} = \left( \begin{array}{r r r} 2 & - 1 & 1 \\ - 1 & 2 & 1 \\ 1 & 1 & 2 \end{array} \right) \stackrel {{r}} {{\sim}} \left( \begin{array}{c c c} 1 & 0 & 1 \\ 0 & 1 & 1 \\ 0 & 0 & 0 \end{array} \right),
$$

得基础解系  $\xi_{1}=\begin{pmatrix}-1\\-1\\1\end{pmatrix}$ . 将  $\xi_{1}$  单位化, 得  $p_{1}=\frac{1}{\sqrt{3}}\begin{pmatrix}-1\\-1\\1\end{pmatrix}$ .

对应 $\lambda_{2} = \lambda_{3} = 1$ ，解方程 $(A - E)x = 0$ ，由

$$
\boldsymbol {A} - \boldsymbol {E} = \left( \begin{array}{c c c} - 1 & - 1 & 1 \\ - 1 & - 1 & 1 \\ 1 & 1 & - 1 \end{array} \right) \stackrel {{r}} {{\sim}} \left( \begin{array}{c c c} 1 & 1 & - 1 \\ 0 & 0 & 0 \\ 0 & 0 & 0 \end{array} \right),
$$

得基础解系  $\boldsymbol{\xi}_{2}=\begin{pmatrix}-1\\1\\0\end{pmatrix},\boldsymbol{\xi}_{3}=\begin{pmatrix}1\\0\\1\end{pmatrix}.$

将 $\pmb{\xi}_2, \pmb{\xi}_3$ 正交化: 取 $\pmb{\eta}_2 = \pmb{\xi}_2$,

$$
\boldsymbol {\eta} _ {3} = \boldsymbol {\xi} _ {3} - \frac {(\boldsymbol {\xi} _ {3} , \boldsymbol {\eta} _ {2})}{\| \boldsymbol {\eta} _ {2} \| ^ {2}} \boldsymbol {\eta} _ {2} = \left( \begin{array}{c} 1 \\ 0 \\ 1 \end{array} \right) + \frac {1}{2} \left( \begin{array}{c} - 1 \\ 1 \\ 0 \end{array} \right) = \frac {1}{2} \left( \begin{array}{c} 1 \\ 1 \\ 2 \end{array} \right).
$$

再将  $\eta_{2},\eta_{3}$  单位化, 得  $p_{2}=\frac{1}{\sqrt{2}}\begin{pmatrix}-1\\1\\0\end{pmatrix},p_{3}=\frac{1}{\sqrt{6}}\begin{pmatrix}1\\1\\2\end{pmatrix}.$

将 $p_{1},p_{2},p_{3}$ 构成正交矩阵

$$
\boldsymbol {P} = (\boldsymbol {p} _ {1}, \boldsymbol {p} _ {2}, \boldsymbol {p} _ {3}) = \left( \begin{array}{c c c} - \frac {1}{\sqrt {3}} & - \frac {1}{\sqrt {2}} & \frac {1}{\sqrt {6}} \\ - \frac {1}{\sqrt {3}} & \frac {1}{\sqrt {2}} & \frac {1}{\sqrt {6}} \\ \frac {1}{\sqrt {3}} & 0 & \frac {2}{\sqrt {6}} \end{array} \right),
$$

有

$$
\boldsymbol {P} ^ {- 1} \boldsymbol {A} \boldsymbol {P} = \boldsymbol {P} ^ {\mathrm{T}} \boldsymbol {A} \boldsymbol {P} = \boldsymbol {\Lambda} = \left( \begin{array}{c c c} - 2 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{array} \right).
$$

例 13 设  $A=\begin{pmatrix}2&-1\\-1&2\end{pmatrix}$ ，求  $A^{n}$ .

解 因 A 对称, 故 A 可对角化, 即有可逆矩阵 P 及对角矩阵 A, 使  $P^{-1}AP = A$ . 于是  $A = P\Lambda P^{-1}$ , 从而  $A^{n} = P\Lambda^{n}P^{-1}$ . 由

$$
\left| \boldsymbol {A} - \lambda \boldsymbol {E} \right| = \left| \begin{array}{c c} 2 - \lambda & - 1 \\ - 1 & 2 - \lambda \end{array} \right| = \lambda^ {2} - 4 \lambda + 3 = (\lambda - 1) (\lambda - 3),
$$

得 A 的特征值  $\lambda_{1}=1,\lambda_{2}=3$ . 于是

$$
\boldsymbol {\Lambda} = \left( \begin{array}{c c} 1 & 0 \\ 0 & 3 \end{array} \right), \quad \boldsymbol {\Lambda} ^ {n} = \left( \begin{array}{c c} 1 & 0 \\ 0 & 3 ^ {n} \end{array} \right).
$$

对应  $\lambda_{1}=1$ ，由  $A-E=\begin{pmatrix}1&-1\\ -1&1\end{pmatrix}\stackrel{r}{\sim}\begin{pmatrix}1&-1\\ 0&0\end{pmatrix}$ ，得  $\xi_{1}=\begin{pmatrix}1\\ 1\end{pmatrix}$ ;

对应  $\lambda_{2}=3$ ，由  $A-3E=\begin{pmatrix}-1&-1\\-1&-1\end{pmatrix}\stackrel{r}{\sim}\begin{pmatrix}1&1\\0&0\end{pmatrix}$ ，得  $\xi_{2}=\begin{pmatrix}1\\-1\end{pmatrix}$ .

并有  $\boldsymbol{P}=(\boldsymbol{\xi}_{1},\boldsymbol{\xi}_{2})=\begin{pmatrix}1&1\\ 1&-1\end{pmatrix}$ ，再求出  $P^{-1}=\frac{1}{2}\begin{pmatrix}1&1\\ 1&-1\end{pmatrix}$ .于是

$$
\boldsymbol {A} ^ {n} = \boldsymbol {P} \boldsymbol {\Lambda} ^ {n} \boldsymbol {P} ^ {- 1} = \frac {1}{2} \left( \begin{array}{c c} 1 & 1 \\ 1 & - 1 \end{array} \right) \left( \begin{array}{c c} 1 & 0 \\ 0 & 3 ^ {n} \end{array} \right) \left( \begin{array}{c c} 1 & 1 \\ 1 & - 1 \end{array} \right) = \frac {1}{2} \left( \begin{array}{c c} 1 + 3 ^ {n} & 1 - 3 ^ {n} \\ 1 - 3 ^ {n} & 1 + 3 ^ {n} \end{array} \right).
$$

![](images/page_133_image_17.jpg)

## § 5 二次型及其标准形

在解析几何中,为了便于研究二次曲线

$$
a x ^ {2} + b x y + c y ^ {2} = 1 \tag {4}
$$

的几何性质,可以选择适当的坐标旋转变换

$$
\left\{ \begin{array}{l} x = x ^ {\prime} \cos \theta - y ^ {\prime} \sin \theta , \\ y = x ^ {\prime} \sin \theta + y ^ {\prime} \cos \theta , \end{array} \right.
$$

把方程(4)化为标准形

$$
m x ^ {\prime 2} + n y ^ {r 2} = 1.
$$

(4)式的左边是一个二次齐次多项式,从代数学的观点看,化标准形的过程就是通过变量的线性变换化简一个二次齐次多项式,使它只含有平方项.这样一个问题,在许多理论问题或实际问题中常会遇到.现在我们把这类问题一般化,讨论n个变量的二次齐次多项式的化简问题.

定义 8 含有 n 个变量  $x_{1}, x_{2}, \cdots, x_{n}$  的二次齐次函数

$$
f \left(x _ {1}, x _ {2}, \dots , x _ {n}\right) = a _ {1 1} x _ {1} ^ {2} + a _ {2 2} x _ {2} ^ {2} + \dots + a _ {n n} x _ {n} ^ {2} + 2 a _ {1 2} x _ {1} x _ {2} + 2 a _ {1 3} x _ {1} x _ {3} + \dots + 2 a _ {n - 1, n} x _ {n - 1} x _ {n} \tag {5}
$$

称为二次型.

当 $j > i$ 时，取 $a_{ji} = a_{ij}$，则 $2a_{ij}x_{i}x_{j} = a_{ij}x_{i}x_{j} + a_{ji}x_{j}x_{i}$，于是(5)式可写成

$$
\begin{array}{l} f = a _ {1 1} x _ {1} ^ {2} + a _ {1 2} x _ {1} x _ {2} + \dots + a _ {1 n} x _ {1} x _ {n} + a _ {2 1} x _ {2} x _ {1} + a _ {2 2} x _ {2} ^ {2} + \dots + a _ {2 n} x _ {2} x _ {n} + \dots + a _ {n 1} x _ {n} x _ {1} + a _ {n 2} x _ {n} x _ {2} + \dots + a _ {n n} x _ {n} ^ {2} \\ = \sum_ {i, j = 1} ^ {n} a _ {i j} x _ {i} x _ {j}. \tag {6} \\ \end{array}
$$

当 $a_{ij}$ 为复数时, $f$ 称为复二次型; 当 $a_{ij}$ 为实数时, $f$ 称为实二次型. 这里, 我们仅讨论实二次型.

若二次型只含有平方项,则称为标准二次型(简称标准形);若二次型形如 $f=y_{1}^{2}+y_{2}^{2}+\cdots+y_{p}^{2}-y_{p+1}^{2}-y_{p+2}^{2}-\cdots-y_{r}^{2}$ ，则称为规范二次型(简称规范形).

利用矩阵,二次型(6)可表示为

$$
f = x _ {1} \left(a _ {1 1} x _ {1} + a _ {1 2} x _ {2} + \dots + a _ {1 n} x _ {n}\right) + x _ {2} \left(a _ {2 1} x _ {1} + a _ {2 2} x _ {2} + \dots + a _ {2 n} x _ {n}\right) + \dots + x _ {n} \left(a _ {n 1} x _ {1} + a _ {n 2} x _ {2} + \dots + a _ {n n} x _ {n}\right)
$$

$$
= (x _ {1}, x _ {2}, \dots , x _ {n}) \left( \begin{array}{c} a _ {1 1} x _ {1} + a _ {1 2} x _ {2} + \dots + a _ {1 n} x _ {n} \\ a _ {2 1} x _ {1} + a _ {2 2} x _ {2} + \dots + a _ {2 n} x _ {n} \\ \vdots \\ a _ {n 1} x _ {1} + a _ {n 2} x _ {2} + \dots + a _ {n n} x _ {n} \end{array} \right)
$$

$$
= (x _ {1}, x _ {2}, \dots , x _ {n}) \left( \begin{array}{c c c c} a _ {1 1} & a _ {1 2} & \dots & a _ {1 n} \\ a _ {2 1} & a _ {2 2} & \dots & a _ {2 n} \\ \vdots & \vdots & & \vdots \\ a _ {n 1} & a _ {n 2} & \dots & a _ {n n} \end{array} \right) \left( \begin{array}{c} x _ {1} \\ x _ {2} \\ \vdots \\ x _ {n} \end{array} \right),
$$

记

$$
\boldsymbol {A} = \left( \begin{array}{c c c c} a _ {1 1} & a _ {1 2} & \dots & a _ {1 n} \\ a _ {2 1} & a _ {2 2} & \dots & a _ {2 n} \\ \vdots & \vdots & & \vdots \\ a _ {n 1} & a _ {n 2} & \dots & a _ {n n} \end{array} \right), \quad \boldsymbol {x} = \left( \begin{array}{c} x _ {1} \\ x _ {2} \\ \vdots \\ x _ {n} \end{array} \right),
$$

则二次型可用矩阵记作

$$
f = \boldsymbol {x} ^ {\mathrm{T}} \boldsymbol {A} \boldsymbol {x}, \tag {7}
$$

其中 A 为对称矩阵.

例如,二次型 $f=x^{2}-3z^{2}-4xy+yz$ 用矩阵记号写出来,就是

$$
f = (x, y, z) \left( \begin{array}{c c c} 1 & - 2 & 0 \\ - 2 & 0 & \frac {1}{2} \\ 0 & \frac {1}{2} & - 3 \end{array} \right) \left( \begin{array}{c} x \\ y \\ z \end{array} \right).
$$

任给一个二次型,就惟一地确定一个对称矩阵;反之,任给一个对称矩阵,也可惟一地确定一个二次型.这样,二次型与对称矩阵之间存在一一对应的关系.因此,我们把对称矩阵A叫做二次型f的矩阵,也把f叫做对称矩阵A的二次型.对称矩阵A的秩就叫做二次型f的秩.

对二次型,我们讨论的主要问题是:是否存在可逆的线性变换(若存在,如何寻找):

$$
\left\{ \begin{array}{l} x _ {1} = c _ {1 1} y _ {1} + c _ {1 2} y _ {2} + \dots + c _ {1 n} y _ {n}, \\ x _ {2} = c _ {2 1} y _ {1} + c _ {2 2} y _ {2} + \dots + c _ {2 n} y _ {n}, \\ \dots \dots \\ x _ {n} = c _ {n 1} y _ {1} + c _ {n 2} y _ {2} + \dots + c _ {n n} y _ {n}, \end{array} \right. \tag {8}
$$

使原二次型变成标准形.

记 $C = (c_{ij})$ ，把可逆变换(8)记作

$$
x = C y,
$$

代入(7)式,有 $f=x^{T}Ax=(Cy)^{T}ACy=y^{T}(C^{T}AC)y$ .

定义9 设 $A$ 和 $B$ 是 $n$ 阶矩阵, 若有可逆矩阵 $C$, 使 $B = C^{\mathrm{T}}AC$, 则称矩阵 $A$ 与 $B$ 合同.

显然, 若 A 为对称矩阵, 则  $B = C^{T} AC$  也为对称矩阵, 且  $R(B) = R(A)$ . 事实上,

$$
\boldsymbol {B} ^ {\mathrm{T}} = (\boldsymbol {C} ^ {\mathrm{T}} \boldsymbol {A} \boldsymbol {C}) ^ {\mathrm{T}} = \boldsymbol {C} ^ {\mathrm{T}} \boldsymbol {A} ^ {\mathrm{T}} \boldsymbol {C} = \boldsymbol {C} ^ {\mathrm{T}} \boldsymbol {A} \boldsymbol {C} = \boldsymbol {B},
$$

即 $\pmb{B}$ 为对称矩阵. 又因 $B = C^{\mathrm{T}}AC$ ，而 $C$ 可逆，从而 $C^{\mathrm{T}}$ 也可逆，由矩阵秩的性质即知 $R(B) = R(A)$.

由此可知,经可逆变换 x = Cy 后,二次型 f 的矩阵由 A 变为与 A 合同的矩阵  $C^{T}AC$ ,且二次型的秩不变.

要使二次型 $f$ 经可逆变换 $\pmb {x} = \pmb{C}\pmb{y}$ 变成标准形，这就是要使

$$
\mathbf {y} ^ {\mathrm{T}} \boldsymbol {C} ^ {\mathrm{T}} \boldsymbol {A} \boldsymbol {C} \mathbf {y} = k _ {1} y _ {1} ^ {2} + k _ {2} y _ {2} ^ {2} + \dots + k _ {n} y _ {n} ^ {2} = (y _ {1}, y _ {2}, \dots , y _ {n}) \left( \begin{array}{c c c c} k _ {1} & & & \\ & k _ {2} & & \\ & & \ddots & \\ & & & k _ {n} \end{array} \right) \left( \begin{array}{c} y _ {1} \\ y _ {2} \\ \vdots \\ y _ {n} \end{array} \right),
$$

也就是要使 $C^{\mathrm{T}}AC$ 成为对角矩阵. 因此, 我们的主要问题就是: 对于对称矩阵 $A$, 是否存在可逆矩阵 $C$, 使 $C^{\mathrm{T}}AC$ 为对角矩阵. 这个问题称为把对称矩阵 $A$ 合同对角化.

由上节定理5知,任给对称矩阵A,总有正交矩阵P,使 $P^{-1}AP=\Lambda$ ,即 $P^{T}AP=\Lambda$ .把此结论应用于二次型,即有

定理6 任给二次型 $f = \sum_{i,j=1}^{n} a_{ij} x_i x_j$ ($a_{ij} = a_{ji}$)，总有正交变换 $x = Py$，使 $f$ 化为标准形

$$
f = \lambda_ {1} y _ {1} ^ {2} + \lambda_ {2} y _ {2} ^ {2} + \dots + \lambda_ {n} y _ {n} ^ {2},
$$

其中  $\lambda_{1},\lambda_{2},\cdots,\lambda_{n}$  是 f 的矩阵  $A=(a_{ij})$  的特征值.

推论 任给 $n$ 元二次型 $f(x) = x^{\mathrm{T}}Ax$ ($A^{\mathrm{T}} = A$), 总有可逆变换 $x = Cz$, 使 $f(Cz)$ 为规范形.

证 按定理6,有

$$
f (\boldsymbol {P} \boldsymbol {y}) = \boldsymbol {y} ^ {\mathrm{T}} \boldsymbol {\Lambda} \boldsymbol {y} = \lambda_ {1} y _ {1} ^ {2} + \lambda_ {2} y _ {2} ^ {2} + \dots + \lambda_ {n} y _ {n} ^ {2}.
$$

设二次型 $f$ 的秩为 $r$, 则特征值 $\lambda_{i}$ 中恰有 $r$ 个不为 0, 无妨设 $\lambda_{1}, \lambda_{2}, \cdots, \lambda_{r}$ 不等于 0, $\lambda_{r+1} = \lambda_{r+2} = \cdots = \lambda_{n} = 0$. 令

$$
\boldsymbol {K} = \left( \begin{array}{c c c c} k _ {1} & & & \\ & k _ {2} & & \\ & & \ddots & \\ & & & k _ {n} \end{array} \right),
$$

其中

$$
k _ {i} = \left\{ \begin{array}{c c} \frac {1}{\sqrt {| \lambda_ {i} |}}, i \leqslant r, \\ 1, & i > r, \end{array} \right.
$$

则 K 可逆, 变换 y = Kz 把  $f(Py)$  化为

$$
f (\boldsymbol {P} \boldsymbol {K} z) = z ^ {\mathrm{T}} \boldsymbol {K} ^ {\mathrm{T}} \boldsymbol {P} ^ {\mathrm{T}} \boldsymbol {A} \boldsymbol {P} \boldsymbol {K} z = z ^ {\mathrm{T}} \boldsymbol {K} ^ {\mathrm{T}} \boldsymbol {\Lambda} \boldsymbol {K} z,
$$

而

$$
\boldsymbol {K} ^ {\mathrm{T}} \boldsymbol {\Lambda} \boldsymbol {K} = \operatorname{diag} \left(\frac {\lambda_ {1}}{| \lambda_ {1} |}, \frac {\lambda_ {2}}{| \lambda_ {2} |}, \dots , \frac {\lambda_ {r}}{| \lambda_ {r} |}, 0, \dots , 0\right).
$$

记 $C = PK$ ，即知可逆变换 $\pmb {x} = \pmb{Cz}$ 把 $f$ 化成规范形

$$
f (\boldsymbol {C} z) = \frac {\lambda_ {1}}{| \lambda_ {1} |} z _ {1} ^ {2} + \frac {\lambda_ {2}}{| \lambda_ {2} |} z _ {2} ^ {2} + \dots + \frac {\lambda_ {r}}{| \lambda_ {r} |} z _ {r} ^ {2}.
$$

证毕

例14 求一个正交变换 $x = Py$ ，把二次型

$$
f = - 2 x _ {1} x _ {2} + 2 x _ {1} x _ {3} + 2 x _ {2} x _ {3}
$$

化为标准形.

解 二次型 $f$ 的矩阵为

$$
\boldsymbol {A} = \left( \begin{array}{c c c} 0 & - 1 & 1 \\ - 1 & 0 & 1 \\ 1 & 1 & 0 \end{array} \right),
$$

这与例 12 所给矩阵相同. 按例 12 的结果, 有正交矩阵

$$
\boldsymbol {P} = \left( \begin{array}{c c c} - \frac {1}{\sqrt {3}} & - \frac {1}{\sqrt {2}} & \frac {1}{\sqrt {6}} \\ - \frac {1}{\sqrt {3}} & \frac {1}{\sqrt {2}} & \frac {1}{\sqrt {6}} \\ \frac {1}{\sqrt {3}} & 0 & \frac {2}{\sqrt {6}} \end{array} \right),
$$

使

$$
\boldsymbol {P} ^ {\mathrm{T}} \boldsymbol {A} \boldsymbol {P} = \boldsymbol {\Lambda} = \left( \begin{array}{c c c} - 2 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{array} \right),
$$

于是有正交变换

$$
\left( \begin{array}{c} x _ {1} \\ x _ {2} \\ x _ {3} ^ {\prime} \end{array} \right) = \left( \begin{array}{c c c} - \frac {1}{\sqrt {3}} & - \frac {1}{\sqrt {2}} & \frac {1}{\sqrt {6}} \\ - \frac {1}{\sqrt {3}} & \frac {1}{\sqrt {2}} & \frac {1}{\sqrt {6}} \\ \frac {1}{\sqrt {3}} & 0 & \frac {2}{\sqrt {6}} \end{array} \right) \left( \begin{array}{c} y _ {1} \\ y _ {2} \\ y _ {3} \end{array} \right),
$$

把二次型 $f$ 化成标准形

$$
f = - 2 y _ {1} ^ {2} + y _ {2} ^ {2} + y _ {3} ^ {2}.
$$

如果要把二次型 $f$ 化成规范形，只需令

$$
\left\{ \begin{array}{l} y _ {1} = \frac {1}{\sqrt {2}} z _ {1}, \\ y _ {2} = \quad z _ {2}, \\ y _ {3} = \quad z _ {3}, \end{array} \right.
$$

即得 $f$ 的规范形

$$
f = - z _ {1} ^ {2} + z _ {2} ^ {2} + z _ {3} ^ {2}.
$$

## § 6 用配方法化二次型成标准形

用正交变换化二次型成标准形,具有保持几何形状不变的优点.如果不限于用正交变换,那么还可以有多种方法(对应有多个可逆的线性变换)把二次型化成标准形.这里只介绍拉格朗日配方法,下面举例来说明这种方法.

例15 化二次型

$$
f = x _ {1} ^ {2} + 2 x _ {2} ^ {2} + 5 x _ {3} ^ {2} + 2 x _ {1} x _ {2} + 2 x _ {1} x _ {3} + 6 x _ {2} x _ {3}
$$

成标准形,并求所用的变换矩阵.

解 由于 $f$ 中含变量 $x_{1}$ 的平方项, 故把含 $x_{1}$ 的项归并起来, 配方可得

$$
\begin{array}{l} f = x _ {1} ^ {2} + 2 x _ {1} x _ {2} + 2 x _ {1} x _ {3} + 2 x _ {2} ^ {2} + 5 x _ {3} ^ {2} + 6 x _ {2} x _ {3} \\ = \left(x _ {1} + x _ {2} + x _ {3}\right) ^ {2} - x _ {2} ^ {2} - x _ {3} ^ {2} - 2 x _ {2} x _ {3} + 2 x _ {2} ^ {2} + 5 x _ {3} ^ {2} + 6 x _ {2} x _ {3} \\ = \left(x _ {1} + x _ {2} + x _ {3}\right) ^ {2} + x _ {2} ^ {2} + 4 x _ {2} x _ {3} + 4 x _ {3} ^ {2}, \\ \end{array}
$$

上式右端除第一项外已不再含 $x_{1}$. 继续配方, 可得

$$
f = \left(x _ {1} + x _ {2} + x _ {3}\right) ^ {2} + \left(x _ {2} + 2 x _ {3}\right) ^ {2}.
$$

令 $\left\{\begin{aligned}y_{1}&=x_{1}+x_{2}+x_{3},\\ y_{2}&=x_{2}+2x_{3},\\ y_{3}&=x_{3},\end{aligned}\right.\quad\left\{\begin{aligned}x_{1}&=y_{1}-y_{2}+y_{3},\\ x_{2}&=y_{2}-2y_{3},\\ x_{3}&=y_{3},\end{aligned}\right.$ 就把f化成标准形(规范形) $f=y_{1}^{2}+y_{2}^{2}$ ，所用

变换矩阵为

$$
\boldsymbol {C} = \left( \begin{array}{c c c} 1 & - 1 & 1 \\ 0 & 1 & - 2 \\ 0 & 0 & 1 \end{array} \right) \quad (| \boldsymbol {C} | = 1 \neq 0).
$$

例16 化二次型

$$
f = 2 x _ {1} x _ {2} + 2 x _ {1} x _ {3} - 6 x _ {2} x _ {3}
$$

成规范形,并求所用的变换矩阵.

解 在 $f$ 中不含平方项. 由于含有 $x_{1}x_{2}$ 乘积项, 故令

$$
\left\{ \begin{array}{l} x _ {1} = y _ {1} + y _ {2}, \\ x _ {2} = y _ {1} - y _ {2}, \\ x _ {3} = y _ {3}, \end{array} \right.
$$

代入可得

$$
f = 2 y _ {1} ^ {2} - 2 y _ {2} ^ {2} - 4 y _ {1} y _ {3} + 8 y _ {2} y _ {3}.
$$

再配方,得

$$
f = 2 (y _ {1} - y _ {3}) ^ {2} - 2 (y _ {2} - 2 y _ {3}) ^ {2} + 6 y _ {3} ^ {2}.
$$

令 $\left\{\begin{aligned}z_{1}&=\sqrt{2}\left(y_{1}-y_{3}\right),\\ z_{2}&=\sqrt{2}\left(y_{2}-2y_{3}\right),\\ z_{3}&=\sqrt{6}y_{3},\end{aligned}\right.$  即 $\left\{\begin{aligned}y_{1}&=\frac{1}{\sqrt{2}}z_{1}+\frac{1}{\sqrt{6}}z_{3},\\ y_{2}&=\frac{1}{\sqrt{2}}z_{2}+\frac{2}{\sqrt{6}}z_{3},\\ y_{3}&=\frac{1}{\sqrt{6}}z_{3},\end{aligned}\right.$  就把f化成规范形

$$
f = z _ {1} ^ {2} - z _ {2} ^ {2} + z _ {3} ^ {2},
$$

所用变换矩阵为

$$
\boldsymbol {C} = \left( \begin{array}{c c c} 1 & 1 & 0 \\ 1 & - 1 & 0 \\ 0 & 0 & 1 \end{array} \right) \left( \begin{array}{c c c} \frac {1}{\sqrt {2}} & 0 & \frac {1}{\sqrt {6}} \\ 0 & \frac {1}{\sqrt {2}} & \frac {2}{\sqrt {6}} \\ 0 & 0 & \frac {1}{\sqrt {6}} \end{array} \right) = \left( \begin{array}{c c c} \frac {1}{\sqrt {2}} & \frac {1}{\sqrt {2}} & \frac {3}{\sqrt {6}} \\ \frac {1}{\sqrt {2}} & - \frac {1}{\sqrt {2}} & - \frac {1}{\sqrt {6}} \\ 0 & 0 & \frac {1}{\sqrt {6}} \end{array} \right) (| \boldsymbol {C} | = - \frac {1}{\sqrt {6}} \neq 0).
$$

一般地,任何二次型都可用上面两例的方法找到可逆变换,把二次型化成标准形(或规范形).

## § 7 正定二次型

二次型的标准形显然不是惟一的,只是标准形中所含项数是确定的(即是二次型的秩).不仅如此,在限定变换为实变换时,标准形中正系数的个数是不变的(从而负系数的个数也不变),也就是有

定理7 设二次型 $f = x^{\mathrm{T}}Ax$ 的秩为 $r$, 且有两个可逆变换

$$
x = C y \quad {\text {及}} \quad x = P z
$$

使

$$
f = k _ {1} y _ {1} ^ {2} + k _ {2} y _ {2} ^ {2} + \dots + k _ {r} y _ {r} ^ {2} \quad (k _ {i} \neq 0)
$$

及

$$
f = \lambda_ {1} z _ {1} ^ {2} + \lambda_ {2} z _ {2} ^ {2} + \dots + \lambda_ {r} z _ {r} ^ {2} \quad (\lambda_ {i} \neq 0),
$$

则  $k_{1}, k_{2}, \cdots, k_{r}$  中正数的个数与  $\lambda_{1}, \lambda_{2}, \cdots, \lambda_{r}$  中正数的个数相等.

这个定理称为惯性定理,这里不予证明.

二次型的标准形中正系数的个数称为二次型的正惯性指数,负系数的个数称为负惯性指数.若二次型f的正惯性指数为p,秩为r,则f的规范形便可确定为

$$
f = y _ {1} ^ {2} + y _ {2} ^ {2} + \dots + y _ {p} ^ {2} - y _ {p + 1} ^ {2} - \dots - y _ {r} ^ {2}.
$$

科学技术上用得较多的二次型是正惯性指数为 $n$ 或负惯性指数为 $n$ 的 $n$ 元二次型, 我们有下述定义.

定义 10 设二次型 $f(x) = x^{\mathrm{T}}Ax$，若对任何 $x \neq 0$，都有 $f(x) > 0$（显然 $f(0) = 0$），则称 $f$ 为正定二次型，并称对称矩阵 $A$ 是正定的；如果对任何 $x \neq 0$ 都有 $f(x) < 0$，则称 $f$ 为负定二次型，并称对称矩阵 $A$ 是负定的。

定理8 $n$ 元二次型 $f = x^{\mathrm{T}}Ax$ 为正定的充分必要条件是:它的标准形的 $n$ 个系数全为正，即它的规范形的 $n$ 个系数全为1，亦即它的正惯性指数等于 $n$. 公众号:旗胜考研

证 设可逆变换 $x = Cy$ 使

$$
f (\boldsymbol {x}) = f (\boldsymbol {C y}) = \sum_ {i = 1} ^ {n} k _ {i} y _ {i} ^ {2}.
$$

先证充分性. 设  $k_{i}>0\ (i=1,2,\cdots,n)$ . 任给  $x\neq0$ , 则  $y=C^{-1}x\neq0$ , 故

$$
f (\boldsymbol {x}) = \sum_ {i = 1} ^ {n} k _ {i} y _ {i} ^ {2} > 0.
$$

再证必要性.用反证法.假设有 $k_{s} \leqslant 0$, 则当 $y = e_{s}$ (单位坐标向量)时, $f(Ce_{s}) = k_{s} \leqslant 0$. 显然 $Ce_{s} \neq 0$, 这与 $f$ 为正定相矛盾.这就证明了 $k_{i} > 0 (i = 1,2,\dots,n)$. 证毕

推论 对称矩阵 A 为正定的充分必要条件是: A 的特征值全为正.

定理9 对称矩阵 $A$ 为正定的充分必要条件是: $A$ 的各阶顺序主子式都为正, 即

$$
a _ {1 1} > 0, \quad \left| \begin{array}{c c} a _ {1 1} & a _ {1 2} \\ a _ {2 1} & a _ {2 2} \end{array} \right| > 0, \dots , \quad \left| \begin{array}{c c c c} a _ {1 1} & a _ {1 2} & \dots & a _ {1 n} \\ a _ {2 1} & a _ {2 2} & \dots & a _ {2 n} \\ \vdots & \vdots & & \vdots \\ a _ {n 1} & a _ {n 2} & \dots & a _ {n n} \end{array} \right| > 0,
$$

对称矩阵 A 为负定的充分必要条件是: 奇数阶顺序主子式为负, 而偶数阶顺序主子式为正, 即

$$
\left(- 1\right) ^ {r} \left| \begin{array}{c c c c} a _ {1 1} & a _ {1 2} & \dots & a _ {1 r} \\ a _ {2 1} & a _ {2 2} & \dots & a _ {2 n} \\ \vdots & \vdots & & \vdots \\ a _ {r 1} & a _ {r 2} & \dots & a _ {r r} \end{array} \right| > 0 \quad (r = 1, 2, \dots , n).
$$

这个定理称为赫尔维茨定理,这里不予证明.

例 17 判定二次型  $f = -5x^{2} - 6y^{2} - 4z^{2} + 4xy + 4xz$  的正定性.

解 $f$ 的矩阵为

$$
A = \left( \begin{array}{c c c} {- 5} & {2} & {2} \\ {2} & {- 6} & {0} \\ {2} & {0} & {- 4} \end{array} \right),
$$

其中

$$
a _ {1 1} = - 5 <   0, \quad \left| \begin{array}{c c} a _ {1 1} & a _ {1 2} \\ a _ {2 1} & a _ {2 2} \end{array} \right| = \left| \begin{array}{c c} - 5 & 2 \\ 2 & - 6 \end{array} \right| = 2 6 > 0, \quad | A | = - 8 0 <   0,
$$

根据定理9知 $f$ 为负定.

设 $f(x,y)$ 是二元正定二次型，则 $f(x,y) = c$ （$c > 0$ 为常数）的图形是以原点为中心的椭圆.当把 $c$ 看作任意常数时则是一族椭圆，这族椭圆随着 $c\to 0$ 而收缩到原点.当 $f$ 为三元正定二次型时， $f(x,y,z) = c$ （$c > 0$）的图形是一族椭球.

## 习题五

1. 设  $a=\begin{pmatrix}1\\0\\-2\end{pmatrix},b=\begin{pmatrix}-4\\2\\3\end{pmatrix}$ ，c 与 a 正交，且  $b=\lambda a+c$ ，求  $\lambda$  和 c.

2. 试把下列向量组施密特正交化,然后再单位化:

$$
(a _ {1}, a _ {2}, a _ {3}) = \left( \begin{array}{c c c} 1 & 1 & 1 \\ 1 & 2 & 4 \\ 1 & 3 & 9 \end{array} \right);
$$

$$
(a _ {1}, a _ {2}, a _ {3}) = \left( \begin{array}{r r r} 1 & 1 & - 1 \\ 0 & - 1 & 1 \\ - 1 & 0 & 1 \\ 1 & 1 & 0 \end{array} \right). \tag {2}
$$

3. 下列矩阵是不是正交矩阵？并说明理由:

$$
\left( \begin{array}{c c c} 1 & - \frac {1}{2} & \frac {1}{3} \\ - \frac {1}{2} & 1 & \frac {1}{2} \\ \frac {1}{3} & \frac {1}{2} & - 1 \end{array} \right); \tag {1}
$$

$$
\left( \begin{array}{c c c} \frac {1}{9} & - \frac {8}{9} & - \frac {4}{9} \\ - \frac {8}{9} & \frac {1}{9} & - \frac {4}{9} \\ - \frac {4}{9} & - \frac {4}{9} & \frac {7}{9} \end{array} \right). \tag {2}
$$

4.（1）设 $x$ 为 $n$ 维列向量，$x^{\mathrm{T}}x = 1$，令 $H = E - 2xx^{\mathrm{T}}$，证明 $H$ 是对称的正交矩阵；

(2) 设 A, B 都是正交矩阵, 证明 AB 也是正交矩阵.

5. 设 $a_1, a_2, a_3$ 为两两正交的单位向量组，$b_1 = -\frac{1}{3} a_1 + \frac{2}{3} a_2 + \frac{2}{3} a_3, b_2 = \frac{2}{3} a_1 + \frac{2}{3} a_2 - \frac{1}{3} a_3, b_3 = -\frac{2}{3} a_1 + \frac{1}{3} a_2 - \frac{2}{3} a_3$，证明 $b_1, b_2, b_3$ 也是两两正交的单位向量组。

6. 求下列矩阵的特征值和特征向量:

(1) $\begin{pmatrix}2&-1&2\\5&-3&3\\-1&0&-2\end{pmatrix};$

(2) $\begin{pmatrix}1&2&3\\2&1&3\\3&3&6\end{pmatrix};$

(3) $\begin{pmatrix}0&0&0&1\\0&0&1&0\\0&1&0&0\\1&0&0&0\end{pmatrix}.$

7. 设 A 为 n 阶矩阵, 证明  $A^{T}$  与 A 的特征值相同.

8. 设 $n$ 阶矩阵 $A, B$ 满足 $R(A) + R(B) < n$, 证明 $A$ 与 $B$ 有公共的特征值和公共的特征向量.

9. 设 $A^2 - 3A + 2E = O$，证明 $A$ 的特征值只能取 1 或 2.

10. 设 A 为正交矩阵, 且  $\left|A\right| = -1$ , 证明  $\lambda = -1$  是 A 的特征值.

11. 设 $\lambda \neq 0$ 是 $m$ 阶矩阵 $A_{m \times n} B_{n \times m}$ 的特征值, 证明 $\lambda$ 也是 $n$ 阶矩阵 $BA$ 的特征值.

12. 已知 3 阶矩阵 A 的特征值为 1, 2, 3, 求  $\left|A^{3}-5A^{2}+7A\right|$ .

13. 已知 3 阶矩阵 A 的特征值为 1,2,-3, 求  $\left|A^{*}+3A+2E\right|$ .

14. 设 A, B 都是 n 阶矩阵, 且 A 可逆, 证明 AB 与 BA 相似.

15. 设矩阵  $A=\begin{pmatrix}2&0&1\\3&1&x\\4&0&5\end{pmatrix}$  可相似对角化, 求 x.

16. 已知  $p=\begin{pmatrix}1\\1\\-1\end{pmatrix}$  是矩阵  $A=\begin{pmatrix}2&-1&2\\5&a&3\\-1&b&-2\end{pmatrix}$  的一个特征向量，

(1) 求参数 a, b 及特征向量 p 所对应的特征值；

(2) 问 A 能不能相似对角化？并说明理由.

17. 设  $A=\begin{pmatrix}1&4&2\\0&-3&4\\0&4&3\end{pmatrix}$ ，求  $A^{100}$ .

18. 在某国, 每年有比例为 $p$ 的农村居民移居城镇, 有比例为 $q$ 的城镇居民移居农村. 假设该国总人口数不变, 且上述人口迁移的规律也不变. 把 $n$ 年后农村人口和城镇人口占总人口的比例依次记为 $x_{n}$ 和 $y_{n} (x_{n} + y_{n} = 1)$.

(1) 求关系式  $\begin{pmatrix} x_{n+1} \\ y_{n+1} \end{pmatrix} = A \begin{pmatrix} x_n \\ y_n \end{pmatrix}$  中的矩阵 A;

(2) 设目前农村人口与城镇人口相等, 即  $\begin{pmatrix} x_{0} \\ y_{0} \end{pmatrix} = \begin{pmatrix} 0.5 \\ 0.5 \end{pmatrix}$ , 求  $\begin{pmatrix} x_{n} \\ y_{n} \end{pmatrix}$ .

19. 试求一个正交的相似变换矩阵, 将下列对称矩阵化为对角矩阵:

(1) $\begin{pmatrix}2&-2&0\\-2&1&-2\\0&-2&0\end{pmatrix};$  (2) $\begin{pmatrix}2&2&-2\\2&5&-4\\-2&-4&5\end{pmatrix}.$

20. 设矩阵  $A = \begin{pmatrix} 1 & -2 & -4 \\ -2 & x & -2 \\ -4 & -2 & 1 \end{pmatrix}$  与  $\Lambda = \begin{pmatrix} 5 & & \\ & -4 & \\ & & y \end{pmatrix}$  相似，求 x, y；并求一个正交矩阵 P，使  $P^{-1}AP = \Lambda$ .

21. 设 3 阶矩阵 A 的特征值为  $\lambda_{1}=2, \lambda_{2}=-2, \lambda_{3}=1$ ，对应的特征向量依次为

$$
\boldsymbol {p} _ {1} = \left( \begin{array}{c} 0 \\ 1 \\ 1 \end{array} \right), \quad \boldsymbol {p} _ {2} = \left( \begin{array}{c} 1 \\ 1 \\ 1 \end{array} \right), \quad \boldsymbol {p} _ {3} = \left( \begin{array}{c} 1 \\ 1 \\ 0 \end{array} \right),
$$

求 A.

22. 设 3 阶对称矩阵 A 的特征值为  $\lambda_{1}=1,\lambda_{2}=-1,\lambda_{3}=0$ ，对应  $\lambda_{1},\lambda_{2}$  的特征向量依次为

$$
\boldsymbol {p} _ {1} = \left( \begin{array}{c} 1 \\ 2 \\ 2 \end{array} \right), \quad \boldsymbol {p} _ {2} = \left( \begin{array}{c} 2 \\ 1 \\ - 2 \end{array} \right),
$$

求A.

23. 设 3 阶对称矩阵 A 的特征值为  $\lambda_{1}=6, \lambda_{2}=\lambda_{3}=3$ ，与特征值  $\lambda_{1}=6$  对应的特征向量为  $p_{1}=(1,1,1)^{\mathrm{T}}$ ，求 A.

24. 设  $\boldsymbol{a}=(a_{1},a_{2},\cdots,a_{n})^{\mathrm{T}}, a_{1}\neq0, A=\boldsymbol{a}\boldsymbol{a}^{\mathrm{T}}$

(1) 证明  $\lambda=0$  是 A 的 n-1 重特征值；
(2) 求 A 的非零特征值及 n 个线性无关的特征向量.

25. 设 A, B 均为 n 阶方阵, 证明  $\mathrm{tr}(AB)=\mathrm{tr}(BA)$ .

26. (1) 设  $A = \begin{pmatrix} 3 & -2 \\ -2 & 3 \end{pmatrix}$ ，求  $\varphi(A) = A^{10} - 5A^{9}$ ;

(2) 设  $A = \begin{pmatrix} 2 & 1 & 2 \\ 1 & 2 & 2 \\ 2 & 2 & 1 \end{pmatrix}$ ，求  $\varphi(A) = A^{10} - 6A^{9} + 5A^{8}$ .

27. 用矩阵记号表示下列二次型:

(1)  $f = x^{2} + 4xy + 4y^{2} + 2xz + z^{2} + 4yz;$

(2) $f = x^{2} + y^{2} - 7z^{2} - 2xy - 4xz - 4yz$;

(3) $f = x_{1}^{2} + x_{2}^{2} + x_{3}^{2} - 2x_{1}x_{2} + 6x_{2}x_{3}.$

28. 写出下列二次型的矩阵:

(1) $f(\boldsymbol{x}) = \boldsymbol{x}^{\mathrm{T}}\begin{pmatrix} 2 & 1 \\ 3 & 1 \end{pmatrix} \boldsymbol{x}$;

(2) $f(\boldsymbol{x}) = \boldsymbol{x}^{\mathrm{T}}\begin{pmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \\ 7 & 8 & 9 \end{pmatrix}\boldsymbol{x}.$

29. 求一个正交变换化下列二次型成标准形:

(1) $f=2x_{1}^{2}+3x_{2}^{2}+3x_{3}^{2}+4x_{2}x_{3};$

(2) $f = x_{1}^{2} + x_{3}^{2} + 2x_{1}x_{2} - 2x_{2}x_{3}.$

30. 求一个正交变换把二次曲面的方程

$$
3 x ^ {2} + 5 y ^ {2} + 5 z ^ {2} + 4 x y - 4 x z - 1 0 y z = 1
$$

化成标准方程.

31. 证明:二次型 $f = x^{\mathrm{T}}Ax$ 在 $\| x \| = 1$ 时的最大值为矩阵 $A$ 的最大特征值.

32. 用配方法化下列二次型成规范形,并写出所用变换的矩阵:

(1) $f(x_{1},x_{2},x_{3}) = x_{1}^{2} + 3x_{2}^{2} + 5x_{3}^{2} + 2x_{1}x_{2} - 4x_{1}x_{3};$
(2) $f(x_{1},x_{2},x_{3})=x_{1}^{2}+2x_{3}^{2}+2x_{1}x_{3}+2x_{2}x_{3};$
(3) $f(x_{1},x_{2},x_{3})=2x_{1}^{2}+x_{2}^{2}+4x_{3}^{2}+2x_{1}x_{2}-2x_{2}x_{3}.$

33. 设 $f = x_{1}^{2} + x_{2}^{2} + 5x_{3}^{2} + 2ax_{1}x_{2} - 2x_{1}x_{3} + 4x_{2}x_{3}$ 为正定二次型, 求 $a$.

34. 判定下列二次型的正定性:

(1) $f = -2x_{1}^{2} - 6x_{2}^{2} - 4x_{3}^{2} + 2x_{1}x_{2} + 2x_{1}x_{3}$;

(2) $f = x_{1}^{2} + 3x_{2}^{2} + 9x_{3}^{2} - 2x_{1}x_{2} + 4x_{1}x_{3}.$

35. 证明对称矩阵 A 为正定的充分必要条件是: 存在可逆矩阵 U, 使  $A = U^{T}U$ , 即 A 与单位矩阵 E 合同.

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

定义 5 设有两个非空集合 A, B, 如果对于 A 中任一元素  $\alpha$ , 按照一定的规则, 总有 B 中一个确定的元素  $\beta$  和它对应, 那么, 这个对应规则称为从集合 A 到集合 B 的映射. 我们常用字母表示一个映射, 譬如把上述映射记作 T, 并记

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

简单明了地表示出 $\mathbb{R}^n$ 中的一个线性变换. 我们自然希望 $\mathbb{R}^n$ 中任何一个线性变换都能用这样的关系式来表示.为此,考虑到  $\alpha_{1}=Ae_{1},\alpha_{2}=Ae_{2},\cdots,\alpha_{n}=Ae_{n}$  （ $e_{1},e_{2},\cdots,e_{n}$  为单位坐标向量）,即

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