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

## 部分习题参考答案

## 习题一

1. (1) -4; (2) $3abc - a^3 - b^3 - c^3$; (3) $(a - b)(b - c)(c - a)$; (4) $-2(x^3 + y^3)$.
2. (1) 0; (2) 4; (3) 5; (4) 3; (5) $\frac{n(n - 1)}{2}$; (6) $n(n - 1)$.

3.  $-a_{11}a_{23}a_{32}a_{44}, a_{11}a_{23}a_{34}a_{42}.$

4. (1) 0; (2) 0; (3) 4abcdef; (4) 0; (5) abcd+ab+cd+ad+1; (6) 16.

5. (1) $x = -3$ 或 $x = \pm \sqrt{3}$; (2) $x = a, x = b$ 或 $x = c$.

8. (1) $a^{n-2}(a^2 - 1)$; (2) $[x + (n - 1)a](x - a)^{n-1}$; (3) $\prod_{n+1 \geqslant i > j \geqslant 1} (i - j)$;
(4)  $\prod_{i=1}^{n}(a_{i}d_{i}-b_{i}c_{i})$ ; (5)  $1+a_{1}+\cdots+a_{n}$ ; (6)  $(-1)^{n-1}(n-1)2^{n-2}$ ;
(7) $a_{1}a_{2}\cdots a_{n}\left(1+\sum_{i=1}^{n}\frac{1}{a_{i}}\right).$

9. 24.

## 习题二

1. (1)  $\begin{pmatrix}35 \\6 \\49\end{pmatrix}$ ; (2) 10; (3)  $\begin{pmatrix}-2 & 4 \\-1 & 2 \\-3 & 6\end{pmatrix}$ ; (4)  $\begin{pmatrix}6 & -7 & 8 \\20 & -5 & -6\end{pmatrix}$ ;
(5) $a_{11}x_1^2 + a_{22}x_2^2 + a_{33}x_3^2 + 2a_{12}x_1x_2 + 2a_{13}x_1x_3 + 2a_{23}x_2x_3.$

2. $3\boldsymbol{A}\boldsymbol{B} - 2\boldsymbol{A} = \begin{pmatrix} -2 & 13 & 22\\ -2 & -17 & 20\\ 4 & 29 & -2 \end{pmatrix},\boldsymbol{A}^{\mathrm{T}}\boldsymbol {B} = \begin{pmatrix} 0 & 5 & 8\\ 0 & -5 & 6\\ 2 & 9 & 0 \end{pmatrix}.$

3. $\left\{ \begin{array}{l}x_{1} = -6z_{1} + z_{2} + 3z_{3},\\ x_{2} = 12z_{1} - 4z_{2} + 9z_{3},\\ x_{3} = -10z_{1} - z_{2} + 16z_{3}. \end{array} \right.$

5. (1) 取  $A = \begin{pmatrix} 1 & 1 \\ -1 & -1 \end{pmatrix} \neq O$  而  $A^{2} = O$ ;

(2) 取  $A = \begin{pmatrix} 1 & 0 \\ 0 & 0 \end{pmatrix}$ ，有  $A \neq O, A \neq E$  而  $A^{2} = A$ ;

(3) 取  $A=\begin{pmatrix}1&0\\0&0\end{pmatrix},X=\begin{pmatrix}1&0\\0&0\end{pmatrix},Y=\begin{pmatrix}1&0\\0&1\end{pmatrix}$ ，有  $X \neq Y$  而 AX = AY.

6. (1) $A^2 = \begin{pmatrix} 1 & 0 \\ 2\lambda & 1 \end{pmatrix}, A^3 = \begin{pmatrix} 1 & 0 \\ 3\lambda & 1 \end{pmatrix}, \dots, A^k = \begin{pmatrix} 1 & 0 \\ k\lambda & 1 \end{pmatrix}$;

(2) $\begin{pmatrix}\lambda^{4}&4\lambda^{3}&6\lambda^{2}\\0&\lambda^{4}&4\lambda^{3}\\0&0&\lambda^{4}\end{pmatrix}.$

7. (1) $10^{25}E, 10^{25}\left( \begin{array}{cc}3 & 1\\ 1 & -3 \end{array} \right);\quad (2) - 8^{99}\left( \begin{array}{ccc}2 & 4 & 8\\ 1 & 2 & 4\\ -3 & -6 & -12 \end{array} \right).$

9. (1) $\begin{pmatrix}5 & -2 \\ -2 & 1\end{pmatrix}; \quad (2)\begin{pmatrix}\cos\theta & \sin\theta \\ -\sin\theta & \cos\theta\end{pmatrix};$

(3) $\begin{pmatrix}-2&1&0\\-\frac{13}{2}&3&-\frac{1}{2}\\-16&7&-1\end{pmatrix};$  (4) $\begin{pmatrix}\frac{1}{a_{1}}&&0\\&&\frac{1}{a_{2}}&&\\&&\ddots&&\\0&&\frac{1}{a_{n}}\end{pmatrix}.$

10.  $\left\{\begin{aligned}y_{1}&=-7x_{1}-4x_{2}+9x_{3},\\ y_{2}&=6x_{1}+3x_{2}-7x_{3},\\ y_{3}&=3x_{1}+2x_{2}-4x_{3}.\end{aligned}\right.$

13. $A^{-1} = \frac{1}{2} (A - E), (A + 2E)^{-1} = \frac{1}{4} (3E - A)$.

14. (1) $X = \begin{pmatrix} 2 & -23 \\ 0 & 8 \end{pmatrix}$; (2) $X = \begin{pmatrix} -2 & 2 & 1 \\ -\frac{8}{3} & 5 & -\frac{2}{3} \end{pmatrix}$; (3) $X = \begin{pmatrix} 1 & 1 \\ \frac{1}{4} & 0 \end{pmatrix}$;

(4) $X=\frac{1}{3}\left(\begin{array}{ccc}23&-7&-13\\-22&5&14\end{array}\right).$

15. (1)  $\left\{\begin{aligned}x_{1}&=1,\\ x_{2}&=0,\\ x_{3}&=0;\end{aligned}\right.$  (2)  $\left\{\begin{aligned}x_{1}&=2,\\ x_{2}&=-\frac{1}{2},\\ x_{3}&=\frac{1}{2}.\end{aligned}\right.$
16. -16.
17. $\begin{pmatrix}0&3&3\\-1&2&3\\1&1&0\end{pmatrix}.$
18.  $B = A + E = \begin{pmatrix} 2 & 0 & 1 \\ 0 & 3 & 0 \\ 1 & 0 & 2 \end{pmatrix}.$
19.  $B=2A=2\mathrm{diag}(1,-2,1)$ .
20. $B = \mathrm{diag}(6,6,6, - 1)$
21. $\frac{1}{3}\left( \begin{array}{cc}1 + 2^{13} & 4 + 2^{13}\\ -1 - 2^{11} & -4 - 2^{11} \end{array} \right) = \left( \begin{array}{cc}2731 & 2732\\ -683 & -684 \end{array} \right).$
22.  $4\begin{pmatrix}1&1&1\\1&1&1\\1&1&1\end{pmatrix}.$
25. $\begin{pmatrix}1&2&5&2\\0&1&2&-4\\0&0&-4&3\\0&0&0&-9\end{pmatrix}.$
26. $|A^8| = 10^{16}, A^4 = \begin{pmatrix} 5^4 & 0 & 0 & 0 \\ 0 & 5^4 & 0 & 0 \\ 0 & 0 & 2^4 & 0 \\ 0 & 0 & 2^6 & 2^4 \end{pmatrix}$.
27. $\left( \begin{array}{cc}O & B^{-1}\\ A^{-1} & O \end{array} \right).$
28. (1) $\begin{pmatrix} 1 & -2 & 0 & 0 \\ -2 & 5 & 0 & 0 \\ 0 & 0 & 2 & -3 \\ 0 & 0 & -5 & 8 \end{pmatrix},$. (2) $\frac{1}{2}\begin{pmatrix} 0 & 3 & -1 \\ 0 & -4 & 2 \\ 10 & 0 & 0 \end{pmatrix}.$

## 习题三

1. (1) $\begin{pmatrix} 1 & 0 & 0 & 5 \\ 0 & 0 & 1 & -3 \\ 0 & 0 & 0 & 0 \end{pmatrix}$; (2) $\begin{pmatrix} 0 & 1 & 0 & 5 \\ 0 & 0 & 1 & 3 \\ 0 & 0 & 0 & 0 \end{pmatrix}$;

(3) $\begin{pmatrix}1&-1&0&2&-3\\0&0&1&-2&2\\0&0&0&0&0\\0&0&0&0&.0\end{pmatrix};$  (4) $\begin{pmatrix}1&0&2&0&-2\\0&1&-1&0&3\\0&0&0&1&4\\0&0&0&0&0\end{pmatrix}.$

2.  $P = \begin{pmatrix} -3 & 2 & 0 \\ 2 & -1 & 0 \\ 7 & -6 & 1 \end{pmatrix}$ ,  $PA = \begin{pmatrix} 1 & 0 & -1 & -2 \\ 0 & 1 & 2 & 3 \\ 0 & 0 & 0 & 0 \end{pmatrix}$ .

3. (1) $P = \begin{pmatrix} 1 & 3 \\ 2 & 5 \end{pmatrix}$, $PA = \begin{pmatrix} 1 & 0 & 4 \\ 0 & 1 & 7 \end{pmatrix}$; (2) $Q = \begin{pmatrix} 1 & 2 & 0 \\ 3 & 5 & 0 \\ -4 & -7 & 1 \end{pmatrix}$, $QA^{\mathrm{T}} = \begin{pmatrix} 1 & 0 \\ 0 & 1 \\ 0 & 0 \end{pmatrix}$.

4. (1) $\begin{pmatrix} \frac{7}{6} & \frac{2}{3} & -\frac{3}{2} \\ -1 & -1 & 2 \\ -\frac{1}{2} & 0 & \frac{1}{2} \end{pmatrix}$; (2) $\begin{pmatrix} 1 & 1 & -2 & -4 \\ 0 & 1 & 0 & -1 \\ -1 & -1 & 3 & 6 \\ 2 & 1 & -6 & -10 \end{pmatrix}$.

5. $\begin{pmatrix}x_{1}\\x_{2}\\x_{3}\end{pmatrix}=\begin{pmatrix}2\\-\frac{1}{2}\\\frac{1}{2}\end{pmatrix}.$

6. (1) $\begin{pmatrix} 10 & 2 \\ -15 & -3 \\ 12 & 4 \end{pmatrix}$; (2) $\begin{pmatrix} 2 & -1 & -1 \\ -4 & 7 & 4 \end{pmatrix}$; (3) $\begin{pmatrix} 0 & 1 & -1 \\ -1 & 0 & 1 \\ 1 & -1 & 0 \end{pmatrix}$.

7. 都可能有.

8. $R(\mathbf{A})\geqslant R(\mathbf{B})\geqslant R(\mathbf{A}) - 1.$

9. $\begin{pmatrix}1&0&1&0&0\\1&-1&0&0&0\\0&0&1&0&0\\0&0&0&1&0\\0&0&0&0&0\end{pmatrix}.$

10. (1) R=2; (2) R=3; (3) R=3.
12. (1) $k = 1$; (2) $k = -2$; (3) $k \neq 1$ 且 $k \neq -2$.

14. (1) $\begin{pmatrix} x_1 \\ x_2 \\ x_3 \\ x_4 \end{pmatrix} = c \begin{pmatrix} \frac{4}{3} \\ -3 \\ \frac{4}{3} \\ 1 \end{pmatrix} (c \in \mathbb{R})$; (2) $\begin{pmatrix} x_1 \\ x_2 \\ x_3 \\ x_4 \end{pmatrix} = c_1 \begin{pmatrix} -2 \\ 1 \\ 0 \\ 0 \end{pmatrix} + c_2 \begin{pmatrix} 1 \\ 0 \\ 0 \\ 1 \end{pmatrix} (c_1, c_2 \in \mathbb{R})$;

(3) $\begin{pmatrix} x_1 \\ x_2 \\ x_3 \\ x_4 \end{pmatrix} = c \begin{pmatrix} -\frac{1}{2} \\ \frac{7}{2} \\ \frac{5}{2} \\ 1 \end{pmatrix} (c \in \mathbb{R})$; (4) $\begin{pmatrix} x_1 \\ x_2 \\ x_3 \\ x_4 \end{pmatrix} = c_1 \begin{pmatrix} \frac{3}{17} \\ \frac{19}{17} \\ 1 \\ 0 \end{pmatrix} + c_2 \begin{pmatrix} -\frac{13}{17} \\ -\frac{20}{17} \\ 0 \\ 1 \end{pmatrix} (c_1, c_2 \in \mathbb{R})$.

15.（1）无解；（2） $\begin{pmatrix}x\\y\\z\end{pmatrix}=c\begin{pmatrix}-2\\1\\1\end{pmatrix}+\begin{pmatrix}-1\\2\\0\end{pmatrix}\quad(c\in\mathbb{R})$ ;

(3) $\begin{pmatrix} x \\ y \\ z \\ w \end{pmatrix} = c_1 \begin{pmatrix} -\frac{1}{2} \\ 1 \\ 0 \\ 0 \end{pmatrix} + c_2 \begin{pmatrix} \frac{1}{2} \\ 0 \\ 1 \\ 0 \end{pmatrix} + \begin{pmatrix} \frac{1}{2} \\ 0 \\ 0 \\ 0 \end{pmatrix}$ ($c_1, c_2 \in \mathbb{R}$);
(4) $\begin{pmatrix} x \\ y \\ z \\ w \end{pmatrix} = c_1 \begin{pmatrix} \frac{1}{7} \\ \frac{5}{7} \\ 1 \\ 0 \end{pmatrix} + c_2 \begin{pmatrix} \frac{1}{7} \\ -\frac{9}{7} \\ 0 \\ 1 \end{pmatrix} + \begin{pmatrix} \frac{6}{7} \\ -\frac{5}{7} \\ 0 \\ 0 \end{pmatrix}$ ($c_1, c_2 \in \mathbb{R}$).

16. $\left\{ \begin{array}{l}x_{1} - 2x_{3} + 2x_{4} = 0,\\ x_{2} + 3x_{3} - 4x_{4} = 0. \end{array} \right.$

17. (1) $\lambda \neq -\frac{1}{2}$ 且 $\lambda \neq 2$; (2) $\lambda = -\frac{1}{2}$;

(3) $\lambda = 2, \begin{pmatrix} x_1 \\ x_2 \\ x_3 \end{pmatrix} = c \begin{pmatrix} -1 \\ 1 \\ 0 \end{pmatrix} + \begin{pmatrix} 3 \\ 0 \\ 1 \end{pmatrix} (c \in \mathbb{R}).$

18. (1) $\lambda \neq 1$, 且 $\lambda \neq -2$; (2) $\lambda = -2$;

(3) $\lambda = 1$, $\begin{pmatrix} x_1 \\ x_2 \\ x_3 \end{pmatrix} = c_1 \begin{pmatrix} -1 \\ 1 \\ 0 \end{pmatrix} + c_2 \begin{pmatrix} -1 \\ 0 \\ 1 \end{pmatrix} + \begin{pmatrix} 1 \\ 0 \\ 0 \end{pmatrix}$ ($c_1, c_2 \in \mathbb{R}$).

19. $\lambda = 1$ 时有解 $\begin{pmatrix} x_1 \\ x_2 \\ x_3 \end{pmatrix} = c \begin{pmatrix} 1 \\ 1 \\ 1 \end{pmatrix} + \begin{pmatrix} 1 \\ 0 \\ 0 \end{pmatrix}, \lambda = -2$ 时有解 $\begin{pmatrix} x_1 \\ x_2 \\ x_3 \end{pmatrix} = c \begin{pmatrix} 1 \\ 1 \\ 1 \end{pmatrix} + \begin{pmatrix} 2 \\ 2 \\ 0 \end{pmatrix} (c \in \mathbb{R})$.

20. $\lambda \neq 1$ ，且 $\lambda \neq 10$ 时有惟一解； $\lambda = 10$ 时无解； $\lambda = 1$ 时有无限多解，解为

$$
\left( \begin{array}{c} x _ {1} \\ x _ {2} \\ x _ {3} \end{array} \right) = c _ {1} \left( \begin{array}{c} - 2 \\ 1 \\ 0 \end{array} \right) + c _ {2} \left( \begin{array}{c} 2 \\ 0 \\ 1 \end{array} \right) + \left( \begin{array}{c} 1 \\ 0 \\ 0 \end{array} \right) (c _ {1}, c _ {2} \in \mathbb {R}).
$$

## 习题四

3.（1）线性相关；（2）线性无关.

4. $a = 2$ 或 $a = -1$.

6.  $b = c a_{1} - (1 + c) a_{2}, c \in R$ .

7. 若  $a_{1}=\begin{pmatrix}1\\0\end{pmatrix},a_{2}=\begin{pmatrix}0\\0\end{pmatrix};b_{1}=\begin{pmatrix}0\\0\end{pmatrix},b_{2}=\begin{pmatrix}0\\1\end{pmatrix}$ ，则  $a_{1}+b_{1},a_{2}+b_{2}$  线性无关.

11.（1）线性无关；（2）线性无关；（3）线性相关.

13. (1) $2, \pmb{a}_{1}, \pmb{a}_{2}$; (2) $2, \pmb{a}_{1}, \pmb{a}_{2}$.

14. (1) $a_{1}, a_{2}, a_{3}$ 为最大无关组, $a_{4} = \frac{8}{5} a_{1} - a_{2} + 2a_{3}$;

(2) $a_{1},a_{2},a_{3}$ 为最大无关组, $a_{4}=a_{1}+3a_{2}-a_{3},a_{5}=-a_{2}+a_{3}.$

15. a=2, b=5.

16. $R_{D} = 3$

20. (1)  $B=\begin{pmatrix}0&0&0\\1&0&3\\0&1&-1\end{pmatrix};$  (2)  $|A|=0.$

21. $V_{1}$ 是, $V_{2}$ 不是.

23.  $v_{1}=2a_{1}+3a_{2}-a_{3},v_{2}=3a_{1}-3a_{2}-2a_{3}.$

24. (1) $\begin{pmatrix}2&3&4\\0&-1&0\\-1&0&-1\end{pmatrix};$  (2) $\begin{pmatrix}-8\\-1\\5\end{pmatrix}.$

25. (1) $\xi_{1} = \begin{pmatrix} 0 \\ 1 \\ 0 \\ 4 \end{pmatrix}$, $\xi_{2} = \begin{pmatrix} -4 \\ 0 \\ 1 \\ -3 \end{pmatrix}$; (2) $\xi_{1} = \begin{pmatrix} 1 \\ 7 \\ 0 \\ 19 \end{pmatrix}$, $\xi_{2} = \begin{pmatrix} 0 \\ 0 \\ 1 \\ 2 \end{pmatrix}$;

(3) $(\boldsymbol{\xi}_{1},\boldsymbol{\xi}_{2},\cdots,\boldsymbol{\xi}_{n-1})=\begin{pmatrix}1&&&\\&1&&\\&&\ddots&&\\&&&1\\-n&-n+1&\cdots&-2\end{pmatrix}.$

26. $\begin{pmatrix}1&0\\5&2\\8&1\\0&1\end{pmatrix}.$

27.  $\left\{\begin{aligned}x_{1}-2x_{2}+x_{3}&=0,\\ 2x_{1}-3x_{2}+x_{4}&=0.\end{aligned}\right.$

28. (1) $\mathrm{I}:\pmb{\xi}_1 = \begin{pmatrix} -1 \\ 1 \\ 0 \\ 1 \end{pmatrix},\pmb{\xi}_2 = \begin{pmatrix} 0 \\ 0 \\ 1 \\ 0 \end{pmatrix};\mathrm{II}:\pmb{\xi}_1 = \begin{pmatrix} 1 \\ 1 \\ 0 \\ -1 \end{pmatrix},\pmb{\xi}_2 = \begin{pmatrix} -1 \\ 0 \\ 1 \\ 1 \end{pmatrix};$ (2) $x = c\left( \begin{array}{c} -1\\ 1\\ 2\\ 1 \end{array} \right)(c\in \mathbb{R}).$

31. (1) $\boldsymbol{\eta} = \begin{pmatrix} -8 \\ 13 \\ 0 \\ 2 \end{pmatrix}, \boldsymbol{\xi} = \begin{pmatrix} -1 \\ 1 \\ 1 \\ 0 \end{pmatrix}$; (2) $\boldsymbol{\eta} = \begin{pmatrix} -17 \\ 0 \\ 14 \\ 0 \end{pmatrix}, \boldsymbol{\xi}_1 = \begin{pmatrix} -9 \\ 1 \\ 7 \\ 0 \end{pmatrix}, \boldsymbol{\xi}_2 = \begin{pmatrix} -4 \\ 0 \\ \frac{7}{2} \\ 1 \end{pmatrix}$.

32.  $x=c\begin{pmatrix}3\\4\\5\\6\end{pmatrix}+\begin{pmatrix}2\\3\\4\\5\end{pmatrix}\quad(c\in\mathbb{R}).$

33. (1) $\alpha = -4$ 且 $\beta \neq 0$; (2) $\alpha \neq -4$;

(3)  $\alpha = -4$ , 且  $\beta = 0, b = ca_{1} - (2c + 1)a_{2} + a_{3} \quad (c \in \mathbb{R})$ .

35.  $x=c\begin{pmatrix}1\\-2\\1\\0\end{pmatrix}+\begin{pmatrix}1\\1\\1\\1\end{pmatrix}\quad(c\in\mathbb{R}).$

## 习题五

1. $\lambda = -2, c = (-2, 2, -1)^{\mathrm{T}}$.

2. (1)  $p_{1}=\frac{1}{\sqrt{3}}\begin{pmatrix}1\\1\\1\end{pmatrix},p_{2}=\frac{1}{\sqrt{2}}\begin{pmatrix}-1\\0\\1\end{pmatrix},p_{3}=\frac{1}{\sqrt{6}}\begin{pmatrix}1\\-2\\1\end{pmatrix};$

(2) $p_{1}=\frac{1}{\sqrt{3}}\left(\begin{array}{c}1\\0\\-1\\1\end{array}\right),p_{2}=\frac{1}{\sqrt{15}}\left(\begin{array}{c}1\\-3\\2\\1\end{array}\right),p_{3}=\frac{1}{\sqrt{35}}\left(\begin{array}{c}-1\\3\\3\\4\end{array}\right).$

3.（1）不是； （2）是

6. (1)  $\lambda = -1$  为三重根,  $p = \begin{pmatrix} 1 \\ 1 \\ -1 \end{pmatrix}$ ;

(2) $\lambda_{1} = -1, \lambda_{2} = 9, \lambda_{3} = 0, \boldsymbol{p}_{1} = \begin{pmatrix} -1 \\ 1 \\ 0 \end{pmatrix}, \boldsymbol{p}_{2} = \begin{pmatrix} 1 \\ 1 \\ 2 \end{pmatrix}, \boldsymbol{p}_{3} = \begin{pmatrix} -1 \\ -1 \\ 1 \end{pmatrix};$

(3) $\lambda_{1} = \lambda_{2} = 1, \lambda_{3} = \lambda_{4} = -1, (\boldsymbol{p}_{1}, \boldsymbol{p}_{2}, \boldsymbol{p}_{3}, \boldsymbol{p}_{4}) = \begin{pmatrix} 1 & 0 & 0 & -1 \\ 0 & 1 & -1 & 0 \\ 0 & 1 & 1 & 0 \\ 1 & 0 & 0 & 1 \end{pmatrix}$.

12. 18.

13. 25.

15. x = 3.

16. (1) $a = -3, b = 0, \lambda = -1$; (2) 不能.

17. $A^{100} = \left( \begin{array}{ccc}1 & 0 &  & 5^{100} - 1\\ 0 & 5^{100} &  & 0\\ 0 & 0 &  & 5^{100} \end{array} \right).$

18. (1)  $A = \begin{pmatrix} 1 - p & q \\ p & 1 - q \end{pmatrix}$ ;

(2) $\begin{pmatrix}x_{n}\\y_{n}\end{pmatrix}=A^{n}\begin{pmatrix}x_{0}\\y_{0}\end{pmatrix}=\frac{1}{2(p+q)}\begin{pmatrix}2q+(p-q)r^{n}\\2p+(q-p)r^{n}\end{pmatrix}$ ，其中r=1-p-q.

19. (1) $P = \frac{1}{3} \begin{pmatrix} 1 & 2 & 2 \\ 2 & 1 & -2 \\ 2 & -2 & 1 \end{pmatrix}, P^{-1} A P = \begin{pmatrix} -2 &  &  \\  & 1 &  \\  &  & 4 \end{pmatrix}$;

(2) $P = \begin{pmatrix} \frac{1}{3} & 0 & \frac{4}{3\sqrt{2}} \\ \frac{2}{3} & \frac{1}{\sqrt{2}} & -\frac{1}{3\sqrt{2}} \\ -\frac{2}{3} & \frac{1}{\sqrt{2}} & \frac{1}{3\sqrt{2}} \end{pmatrix}, P^{-1}AP = \begin{pmatrix} 10 &  &  \\  & 1 &  \\  &  & 1 \end{pmatrix}.$

20. $x = 4, y = 5, \boldsymbol{P} = \begin{pmatrix} \frac{1}{\sqrt{2}} & \frac{2}{3} & \frac{1}{3\sqrt{2}} \\ 0 & \frac{1}{3} & -\frac{4}{3\sqrt{2}} \\ -\frac{1}{\sqrt{2}} & \frac{2}{3} & \frac{1}{3\sqrt{2}} \end{pmatrix}$.

21.  $A=\begin{pmatrix}-2&3&-3\\-4&5&-3\\-4&4&-2\end{pmatrix}.$

22.  $A=\frac{1}{3}\begin{pmatrix}-1&0&2\\0&1&2\\2&2&0\end{pmatrix}.$

23.  $A = \begin{pmatrix} 4 & 1 & 1 \\ 1 & 4 & 1 \\ 1 & 1 & 4 \end{pmatrix}.$

24. (2)  $\lambda_{1}=\sum_{i=1}^{n}a_{i}^{2},\lambda_{2}=\lambda_{3}=\cdots=\lambda_{n}=0,(p_{1},p_{2},\cdots,p_{n})=\begin{pmatrix}a_{1}&-a_{2}&\cdots&-a_{n}\\a_{2}&a_{1}&\cdots&a_{n-1}\\ \vdots&\vdots&&\vdots\\a_{n}&a_{n-1}&\cdots&a_{1}\end{pmatrix}.$

26. (1) $-2\left( \begin{array}{cc}1 & 1\\ 1 & 1 \end{array} \right);$ (2) $2\left( \begin{array}{ccc}1 & 1 & -2\\ 1 & 1 & -2\\ -2 & -2 & 4 \end{array} \right).$

27. (1) $f = (x, y, z) \begin{pmatrix} 1 & 2 & 1 \\ 2 & 4 & 2 \\ 1 & 2 & 1 \end{pmatrix} \begin{pmatrix} x \\ y \\ z \end{pmatrix}$;

(2) $f=(x,y,z)\begin{pmatrix}1&-1&-2\\-1&1&-2\\-2&-2&-7\end{pmatrix}\begin{pmatrix}x\\y\\z\end{pmatrix};$

(3) $f = (x_{1}, x_{2}, x_{3}) \begin{pmatrix} 1 & -1 & 0 \\ -1 & 1 & 3 \\ 0 & 3 & 1 \end{pmatrix} \begin{pmatrix} x_{1} \\ x_{2} \\ x_{3} \end{pmatrix}$.

28. (1) $\begin{pmatrix}2&2\\ 2&1\end{pmatrix};$  (2) $\begin{pmatrix}1&3&5\\ 3&5&7\\ 5&7&9\end{pmatrix}.$

29. (1) $\begin{pmatrix} x_1 \\ x_2 \\ x_3 \end{pmatrix} = \begin{pmatrix} 1 & 0 & 0 \\ 0 & \frac{1}{\sqrt{2}} & \frac{1}{\sqrt{2}} \\ 0 & \frac{1}{\sqrt{2}} & -\frac{1}{\sqrt{2}} \end{pmatrix} \begin{pmatrix} y_1 \\ y_2 \\ y_3 \end{pmatrix}, f = 2y_1^2 + 5y_2^2 + y_3^2;$

(2) $\begin{pmatrix}x_{1}\\x_{2}\\x_{3}\end{pmatrix}=\begin{pmatrix}\frac{1}{\sqrt{3}}&\frac{1}{\sqrt{2}}&-\frac{1}{\sqrt{6}}\\ \frac{1}{\sqrt{3}}&0&\frac{2}{\sqrt{6}}\\ -\frac{1}{\sqrt{3}}&\frac{1}{\sqrt{2}}&\frac{1}{\sqrt{6}}\end{pmatrix}\begin{pmatrix}y_{1}\\y_{2}\\y_{3}\end{pmatrix},f=2y_{1}^{2}+y_{2}^{2}-y_{3}^{2}.$

30. $\begin{pmatrix} x \\ y \\ z \end{pmatrix} = \begin{pmatrix} 0 & \frac{4}{3\sqrt{2}} & \frac{1}{3} \\ \frac{1}{\sqrt{2}} & -\frac{1}{3\sqrt{2}} & \frac{2}{3} \\ \frac{1}{\sqrt{2}} & \frac{1}{3\sqrt{2}} & -\frac{2}{3} \end{pmatrix} \begin{pmatrix} u \\ v \\ w \end{pmatrix}, 2v^2 + 11w^2 = 1.$

32. (1) $f(Cy) = y_1^2 + y_2^2 - y_3^2, C = \begin{pmatrix} 1 & -\frac{1}{\sqrt{2}} & 3 \\ 0 & \frac{1}{\sqrt{2}} & -1 \\ 0 & 0 & 1 \end{pmatrix} \left( |C| = \frac{1}{\sqrt{2}} \right)$;

(2) $f(Cy) = y_1^2 - y_2^2 + y_3^2, C = \begin{pmatrix} 1 & 1 & -1 \\ 0 & 1 & 0 \\ 0 & -1 & 1 \end{pmatrix} (|C| = 1)$;

(3) $f(\boldsymbol{C}\boldsymbol{y}) = y_1^2 + y_2^2 + y_3^2, \boldsymbol{C} = \frac{1}{\sqrt{2}} \begin{pmatrix} 1 & -1 & -1 \\ 0 & 2 & 2 \\ 0 & 0 & 1 \end{pmatrix} (|\boldsymbol{C}| = \sqrt{2}).$

33.  $-\frac{4}{5}<a<0.$

34.（1）负定；（2）正定.

## 习题六

1. 各个线性空间的基可取为

(1)  $\alpha_{1}=\begin{pmatrix}1&0\\0&0\end{pmatrix},\alpha_{2}=\begin{pmatrix}0&1\\0&0\end{pmatrix},\alpha_{3}=\begin{pmatrix}0&0\\1&0\end{pmatrix},\alpha_{4}=\begin{pmatrix}0&0\\0&1\end{pmatrix};$
(2)  $\alpha_{1}=\begin{pmatrix}1&0\\0&-1\end{pmatrix},\alpha_{2}=\begin{pmatrix}0&1\\0&0\end{pmatrix},\alpha_{3}=\begin{pmatrix}0&0\\1&0\end{pmatrix};$
(3)  $\alpha_{1}=\begin{pmatrix}1&0\\0&0\end{pmatrix},\alpha_{2}=\begin{pmatrix}0&0\\0&1\end{pmatrix},\alpha_{3}=\begin{pmatrix}0&1\\1&0\end{pmatrix}.$

3.（1）不是；（2）是

4. $(1,-2,6)^{\mathrm{T}}$

5. 设 $\alpha$ 在 $\alpha_{1}, \alpha_{2}, \alpha_{3}$ 下的坐标是 $(x_{1}, x_{2}, x_{3})^{\mathrm{T}}$, 在 $\beta_{1}, \beta_{2}, \beta_{3}$ 下的坐标是 $(x_{1}', x_{2}', x_{3}')^{\mathrm{T}}$, 有

$$
\left( \begin{array}{c} x _ {1} ^ {\prime} \\ x _ {2} ^ {\prime} \\ x _ {3} ^ {\prime} \end{array} \right) = \left( \begin{array}{c c c} 1 3 & 1 9 & 4 3 \\ - 9 & - 1 3 & - 3 0 \\ 7 & 1 0 & 2 4 \end{array} \right) \left( \begin{array}{c} x _ {1} \\ x _ {2} \\ x _ {3} \end{array} \right), \quad \text {或} \quad \left( \begin{array}{c} x _ {1} \\ x _ {2} \\ x _ {3} \end{array} \right) = \left( \begin{array}{c c c} - 1 2 & - 2 6 & - 1 1 \\ 6 & 1 1 & 3 \\ 1 & 3 & 2 \end{array} \right) \left( \begin{array}{c} x _ {1} ^ {\prime} \\ x _ {2} ^ {\prime} \\ x _ {3} ^ {\prime} \end{array} \right).
$$

$$
6. (1) \boldsymbol {P} = \left( \begin{array}{r r r r} 2 & 0 & 5 & 6 \\ 1 & 3 & 3 & 6 \\ - 1 & 1 & 2 & 1 \\ 1 & 0 & 1 & 3 \end{array} \right); \quad (2) \left( \begin{array}{c} x _ {1} ^ {\prime} \\ x _ {2} ^ {\prime} \\ x _ {3} ^ {\prime} \\ x _ {4} ^ {\prime} \end{array} \right) = \frac {1}{2 7} \left( \begin{array}{c c c c} 1 2 & 9 & - 2 7 & - 3 3 \\ 1 & 1 2 & - 9 & - 2 3 \\ 9 & 0 & 0 & - 1 8 \\ - 7 & - 3 & 9 & 2 6 \end{array} \right) \left( \begin{array}{c} x _ {1} \\ x _ {2} \\ x _ {3} \\ x _ {4} \end{array} \right);
$$

(3)  $k(1,1,1,-1)^{\mathrm{T}}$  ( $k \in R$ ).

7.（1）能，不能；（2）维数为3，基可选为 $a_{1},a_{2},b_{2}$

8.（1）关于 y 轴对称；（2）投影到 y 轴；（3）关于直线 y=x 对称；公众号:旗胜考研
（4）顺时针方向旋转  $90^{\circ}$ .

10. $\begin{pmatrix}1&0&0\\2&1&0\\0&1&1\end{pmatrix}.$

11. $\begin{pmatrix}1&0&0\\1&1&0\\1&2&1\end{pmatrix}.$

12. (2) $\begin{pmatrix}1&0&\frac{1}{2}\\0&1&-\frac{1}{2}\\0&0&\frac{1}{2}\end{pmatrix};$  (3) 2.

## 2000 年中国高校科学技术奖二等奖

## 第八届全国高校出版社优秀畅销书一等奖

高等数学 第七版 上册
高等数学 第七版 下册
高等数学附册 学习辅导与习题选解 同济·第七版
高等数学习题全解指南 上册 同济·第七版
高等数学习题全解指南 下册 同济·第七版
工程数学——线性代数 第七版
线性代数附册 学习辅导与习题全解 同济·第七版
工程数学——概率统计简明教程 第三版
▷ 概率统计简明教程附册 学习辅导与习题全解 同济·第三版
工程数学——新编统计学教程