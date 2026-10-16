# 第3章 微分中值定理与导数的应用

原始 PDF 第 139–196 页。

# 第三章

# 微分中值定理与导数的应用

上一章里,从分析实际问题中因变量相对于自变量的变化快慢出发,引进了导数概念,并讨论了导数的计算方法.本章中,我们将应用导数来研究函数以及曲线的某些性态,并利用这些知识解决一些实际问题.为此,先要介绍微分学的几个中值定理,它们是导数应用的理论基础.

## 第一节 微分中值定理

我们先讲罗尔(Rolle)定理,然后根据它推出拉格朗日(Lagrange)中值定理和柯西(Cauchy)中值定理.

## 一、罗尔定理

首先,我们观察图3-1.设曲线弧AB是函数 $y=f(x)$ ( $x\in[a,b]$ )的图形.这是一条连续的曲线弧,除端点外处处有不垂直于x轴的切线,且两个端点的纵坐标相等,即 $f(a)=f(b)$ .可以发现在曲线弧的最高点C处或最低点D处,曲线有水平的切线.如果记点C的横坐标为 $\xi$ ,那么就有 $f'(\xi)=0$ .现在用分析语言把这个几何现象描述出来,就可得下面的罗尔定理.为了应用方便,先介绍费马(Fermat)引理.

![](../../raw/pages_0129-0160/images/page_138_chart_7.jpg)

<details>
<summary>line</summary>

| Point | x-coordinate | y-coordinate |
| --- | --- | --- |
| A | a | ~0.5 |
| C | \(\xi\) | ~0.7 |
| D | b | ~0.2 |
| B | b | ~0.5 |
</details>

图3-1

费马引理 设函数 $f(x)$ 在点 $x_0$ 的某邻域 $U(x_0)$ 内有定义，并且在 $x_0$ 处可导，如果对任意的 $x \in U(x_0)$，有

$$
f (x) \leqslant f (x _ {0}) \quad (\text {或} f (x) \geqslant f (x _ {0}))  ,
$$

122

---

第一节 微分中值定理

那么 $f^{\prime}(x_0) = 0.$

证 不妨设 $x \in U(x_0)$ 时, $f(x) \leqslant f(x_0)$ (如果 $f(x) \geqslant f(x_0)$, 可以类似地证明). 于是, 对于 $x_0 + \Delta x \in U(x_0)$, 有

$$
f (x _ {0} + \Delta x) \leqslant f (x _ {0}),
$$

从而当 $\Delta x > 0$ 时，

$$
\frac {f (x _ {0} + \Delta x) - f (x _ {0})}{\Delta x} \leqslant 0;
$$

当 $\Delta x < 0$ 时，

$$
\frac {f (x _ {0} + \Delta x) - f (x _ {0})}{\Delta x} \geqslant 0.
$$

根据函数 $f(x)$ 在 $x_0$ 可导的条件及极限的保号性，便得到

$$
f ^ {\prime} (x _ {0}) = f _ {+} ^ {\prime} (x _ {0}) = \lim _ {\Delta x \to 0 ^ {+}} \frac {f (x _ {0} + \Delta x) - f (x _ {0})}{\Delta x} \leqslant 0,
$$

$$
f ^ {\prime} (x _ {0}) = f _ {-} ^ {\prime} (x _ {0}) = \lim _ {\Delta x \to 0 ^ {-}} \frac {f (x _ {0} + \Delta x) - f (x _ {0})}{\Delta x} \geqslant 0.
$$

所以， $f'(x_{0})=0$ . 证毕.

通常称导数等于零的点为函数的驻点(或稳定点,临界点).

罗尔定理 如果函数 $f(x)$ 满足

(1) 在闭区间  $[a, b]$  上连续；
(2) 在开区间 $(a,b)$ 内可导；
(3) 在区间端点处的函数值相等, 即  $f(a)=f(b)$ ,

那么在 $(a,b)$ 内至少有一点 $\xi (a <   \xi <  b)$ ，使得 $f^{\prime}(\xi) = 0$

证 由于 $f(x)$ 在闭区间 $[a, b]$ 上连续，根据闭区间上连续函数的最大值最小值定理，$f(x)$ 在闭区间 $[a, b]$ 上必定取得它的最大值 $M$ 和最小值 $m$. 这样，只有两种可能情形:

(1) M=m. 这时  $f(x)$  在区间  $[a,b]$  上必然取相同的数值  $M:f(x)=M.$  由此， $\forall x\in(a,b)$ ，有  $f'(x)=0.$  因此，任取  $\xi\in(a,b)$ ，有  $f'(\xi)=0.$
(2) $M > m$. 因为 $f(a) = f(b)$, 所以 $M$ 和 $m$ 这两个数中至少有一个不等于 $f(x)$ 在区间 $[a, b]$ 的端点处的函数值. 为确定起见, 不妨设 $M \neq f(a)$ (如果设 $m \neq f(a)$, 证法完全类似), 那么必定在开区间 $(a, b)$ 内有一点 $\xi$ 使 $f(\xi) = M$. 因此, $\forall x \in [a, b]$, 有 $f(x) \leqslant f(\xi)$, 从而由费马引理可知 $f'(\xi) = 0$.

定理证毕.

## 二、拉格朗日中值定理

罗尔定理中 $f(a) = f(b)$ 这个条件是相当特殊的，它使罗尔定理的应用受到限

123

---

第三章 微分中值定理与导数的应用

制.如果把 $f(a)=f(b)$ 这个条件取消,但仍保留其余两个条件,并相应地改变结论,那么就得到微分学中十分重要的拉格朗日中值定理.

拉格朗日中值定理 如果函数 $f(x)$ 满足

(1) 在闭区间  $[a, b]$  上连续；
(2) 在开区间 $(a,b)$ 内可导，

那么在 $(a,b)$ 内至少有一点 $\xi (a <   \xi <  b)$ ，使等式

$$
f (b) - f (a) = f ^ {\prime} (\xi) (b - a) \tag {1-1}
$$

成立.

在证明之前,先看一下定理的几何意义.如果把(1-1)式改写成

$$
\frac {f (b) - f (a)}{b - a} = f ^ {\prime} (\xi),
$$

由图3-2可看出， $\frac{f(b) - f(a)}{b - a}$ 为弦 $AB$ 的斜率，而 $f^{\prime}(\xi)$ 为曲线在点 $C$ 处的切线的斜

率.因此拉格朗日中值定理的几何意义是:如果连续曲线  $y=f(x)$  的弧  $\widehat{AB}$  上除端点外处处具有不垂直于 x 轴的切线,那么这弧上至少有一点 C,使曲线在点 C 处的切线平行于弦 AB.

从图3-1看出，在罗尔定理中，由于 $f(a) = f(b)$，弦 $AB$ 是平行于 $x$ 轴的，因此点 $C$ 处的切线实际上也平行于弦 $AB$. 由此可见，罗尔定理是拉格朗日中值定理的特殊情形.

![](../../raw/pages_0129-0160/images/page_140_chart_14.jpg)

<details>
<summary>line</summary>

| Point | x-coordinate | y-coordinate |
| --- | --- | --- |
| A | a | 0 |
| C | \(\xi\) | ~0.8 |
| M | x | ~0.8 |
| B | b | ~0.8 |
</details>

图3-2

从上述拉格朗日中值定理与罗尔定理的关系,自然想到利用罗尔定理来证明拉格朗日中值定理.但在拉格朗日中值定理中,函数 $f(x)$ 不一定具备 $f(a)=f(b)$ 这个条件,为此我们设想构造一个与 $f(x)$ 有密切联系的函数 $\varphi(x)$ （称为辅助函数）,使 $\varphi(x)$ 满足条件 $\varphi(a)=\varphi(b)$ .然后对 $\varphi(x)$ 应用罗尔定理,再把对 $\varphi(x)$ 所得的结论转化到 $f(x)$ 上,证得所要的结果.我们从拉格朗日中值定理的几何解释中来寻找辅助函数,从图3-2中看到,有向线段NM的值是x的函数,把它表示为 $\varphi(x)$ ,它与 $f(x)$ 有密切的联系,且当x=a及x=b时,点M与点N重合,即有 $\varphi(a)=\varphi(b)=0$ .为求得函数 $\varphi(x)$ 的表达式,设直线AB的方程为 $y=L(x)$ ,则

$$
L (x) = f (a) + \frac {f (b) - f (a)}{b - a} (x - a),
$$

由于点 $M, N$ 的纵坐标依次为 $f(x)$ 及 $L(x)$，故表示有向线段 $NM$ 的值的函数

$$
\varphi (x) = f (x) - L (x) = f (x) - f (a) - \frac {f (b) - f (a)}{b - a} (x - a).
$$

124

---

第一节 微分中值定理

下面就利用这个辅助函数来证明拉格朗日中值定理.

拉格朗日中值定理的证明 引进辅助函数

$$
\varphi (x) = f (x) - f (a) - \frac {f (b) - f (a)}{b - a} (x - a).
$$

容易验证函数 $\varphi (x)$ 适合罗尔定理的条件: $\varphi (a) = \varphi (b) = 0,\varphi (x)$ 在闭区间 $[a,b]$ 上连续，在开区间 $(a,b)$ 内可导，且

$$
\varphi^ {\prime} (x) = f ^ {\prime} (x) - \frac {f (b) - f (a)}{b - a}.
$$

根据罗尔定理, 可知在  $(a, b)$  内至少有一点  $\xi$ , 使  $\varphi'(\xi)=0$ , 即

$$
f ^ {\prime} (\xi) - \frac {f (b) - f (a)}{b - a} = 0.
$$

由此得

$$
\frac {f (b) - f (a)}{b - a} = f ^ {\prime} (\xi),
$$

即

$$
f (b) - f (a) = f ^ {\prime} (\xi) (b - a).
$$

定理证毕.

显然,公式(1-1)对于 b<a 也成立.(1-1)式叫做拉格朗日中值公式.

设 $x$ 为区间 $[a, b]$ 内一点，$x + \Delta x$ 为这区间内的另一点（$\Delta x > 0$ 或 $\Delta x < 0$），则公式 (1-1) 在区间 $[x, x + \Delta x]$（当 $\Delta x > 0$ 时）或在区间 $[x + \Delta x, x]$（当 $\Delta x < 0$ 时）上就成为

$$
f (x + \Delta x) - f (x) = f ^ {\prime} (x + \theta \Delta x) \cdot \Delta x \quad (0 <   \theta <   1). \tag {1-2}
$$

这里数值  $\theta$  在 0 与 1 之间, 所以  $x + \theta \Delta x$  是在 x 与  $x + \Delta x$  之间.

如果记 $f(x)$ 为 $y$ ，那么(1-2)式又可写成

$$
\Delta y = f ^ {\prime} (x + \theta \Delta x) \cdot \Delta x \quad (0 <   \theta <   1). \tag {1-3}
$$

我们知道,函数的微分  $\mathrm{dy}=f'(x)\cdot\Delta x$  是函数的增量  $\Delta y$  的近似表达式,一般说来,以 dy 近似代替  $\Delta y$  时所产生的误差只有当  $\Delta x\to0$  时才趋于零;而(1-3)式却给出了自变量取得有限增量  $\Delta x(|\Delta x|$  不一定很小)时,函数增量  $\Delta y$  的准确表达式.因此,这个定理也叫做有限增量定理,(1-3)式称为有限增量公式.拉格朗日中值定理在微分学中占有重要地位,有时也称这定理为微分中值定理.在某些问题中当自变量 x 取得有限增量  $\Delta x$  而需要函数增量的准确表达式时,拉格朗日中值定理就显出它的价值.

作为拉格朗日中值定理的一个应用,我们来导出以后讲积分学时很有用的一个定理.我们知道,如果函数 $f(x)$ 在某一区间上是一个常数,那么 $f(x)$ 在该区间上的导数恒为零.它的逆命题也是成立的,这就是:

图

例题精讲

3-1

125

---

第三章 微分中值定理与导数的应用

定理 如果函数 $f(x)$ 在区间 $I$ 上连续, $I$ 内①可导且导数恒为零, 那么 $f(x)$ 在区间 $I$ 上是一个常数.

证 在区间 $I$ 上任取两点 $x_{1}, x_{2} (x_{1} < x_{2})$，应用(1-1)式就得

$$
f (x _ {2}) - f (x _ {1}) = f ^ {\prime} (\xi) (x _ {2} - x _ {1}) \quad (x _ {1} <   \xi <   x _ {2}).
$$

由假定， $f^{\prime}(\xi) = 0$ ，所以 $f(x_{2}) - f(x_{1}) = 0$ ，即

$$
f (x _ {2}) = f (x _ {1}).
$$

因为 $x_{1}, x_{2}$ 是 $I$ 上任意两点，所以上面的等式表明:$f(x)$ 在 $I$ 上的函数值总是相等的，这就是说，$f(x)$ 在区间 $I$ 上是一个常数.

从上述论证中可以看出,虽然拉格朗日中值定理中的  $\xi$  的准确数值不知道,但在这里并不妨碍它的应用.

例 证明当 x>0 时，

$$
\frac {x}{1 + x} <   \ln (1 + x) <   x.
$$

证 设 $f(t) = \ln (1 + t)$，显然 $f(t)$ 在区间 $[0, x]$ 上满足拉格朗日中值定理的条件，根据定理，应有

$$
f (x) - f (0) = f ^ {\prime} (\xi) (x - 0), \quad 0 <   \xi <   x.
$$

由于 $f(0) = 0, f'(t) = \frac{1}{1 + t}$, 因此上式即为

$$
\ln (1 + x) = \frac {x}{1 + \xi}.
$$

又由 $0 < \xi < x$ ，有

$$
\frac {x}{1 + x} <   \frac {x}{1 + \xi} <   x,
$$

即

$$
\frac {x}{1 + x} <   \ln (1 + x) <   x (x > 0).
$$

## 三、柯西中值定理

上面已经指出,如果连续曲线弧 $\widehat{AB}$ 上除端点外处处具有不垂直于横轴的切线,那么这段弧上至少有一点C,使曲线在点C处的切线平行于弦AB.设 $\widehat{AB}$ 由参数方程

$$
\left\{ \begin{array}{l l} x = \varphi (t), \\ y = \psi (t) \end{array} \right. \quad (a \leqslant t \leqslant b)
$$

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① $x$ 在区间 $I$ 内指 $x \in I$, 且 $x$ 不是 $I$ 的端点.</span></small>

126

---

第一节 微分中值定理

表示,其中 t 为参数,则曲线上点 $(x,y)$ 处的切线斜率为

$$
\frac {\mathrm{d} y}{\mathrm{d} x} = \frac {\psi^ {\prime} (t)}{\varphi^ {\prime} (t)},
$$

弦 ${AB}$ 的斜率为

$$
\frac {\psi (b) - \psi (a)}{\varphi (b) - \varphi (a)}.
$$

假定点 C 对应于参数  $t=\xi$ ，那么曲线上点 C 处的切线平行于弦 AB，可表示为

$$
\frac {\psi (b) - \psi (a)}{\varphi (b) - \varphi (a)} = \frac {\psi^ {\prime} (\xi)}{\varphi^ {\prime} (\xi)}.
$$

这是函数在参数方程形式下的拉格朗日中值定理的表达形式.通过对这个特殊问题的思考,可以得到以下一般性的结论.

柯西中值定理 如果函数 $f(x)$ 及 $F(x)$ 满足

(1) 在闭区间  $[a, b]$  上连续；
(2) 在开区间 $(a,b)$ 内可导；
(3) 对任一  $x \in (a, b)$ ,  $F'(x) \neq 0$ ,

那么在 $(a,b)$ 内至少有一点 $\xi$ ，使等式

$$
\frac {f (b) - f (a)}{F (b) - F (a)} = \frac {f ^ {\prime} (\xi)}{F ^ {\prime} (\xi)} \tag {1-4}
$$

成立.

在定理证明之前,先对要证的结论作一些分析,以便寻找证明的思路.

要证在 $(a,b)$ 内至少有一点 $\xi$ ，使等式(1-4)成立，即成立

$$
\frac {f (b) - f (a)}{F (b) - F (a)} F ^ {\prime} (\xi) = f ^ {\prime} (\xi)
$$

或

$$
f ^ {\prime} (\xi) - \frac {f (b) - f (a)}{F (b) - F (a)} F ^ {\prime} (\xi) = 0
$$

若设函数

$$
\varphi (x) = f (x) - \frac {f (b) - f (a)}{F (b) - F (a)} F (x),
$$

则要证成立

$$
\varphi^ {\prime} (\xi) = f ^ {\prime} (\xi) - \frac {f (b) - f (a)}{F (b) - F (a)} F ^ {\prime} (\xi) = 0.
$$

由此联想到:是否可以利用罗尔定理来证明.而要做到这一点,关键是需要检查函数 $\varphi(x)$ 在闭区间 $[a,b]$ 两端点处的函数值是否相等.

127

---

第三章 微分中值定理与导数的应用

因为

$$
\begin{array}{l} \varphi (x) = f (x) - \frac {f (b) - f (a)}{F (b) - F (a)} F (x) = \frac {[ F (b) - F (a) ] f (x) - [ f (b) - f (a) ] F (x)}{F (b) - F (a)}, \\ \varphi (a) = \frac {\left[ F (b) - F (a) \right] f (a) - \left[ f (b) - f (a) \right] F (a)}{F (b) - F (a)} = \frac {F (b) f (a) - F (a) f (b)}{F (b) - F (a)}, \\ \varphi (b) = \frac {\left[ F (b) - F (a) \right] f (b) - \left[ f (b) - f (a) \right] F (b)}{F (b) - F (a)} = \frac {F (b) f (a) - F (a) f (b)}{F (b) - F (a)}, \\ \end{array}
$$

所以

$$
\varphi (a) = \varphi (b) = \frac {F (b) f (a) - F (a) f (b)}{F (b) - F (a)}.
$$

由以上分析可知,可以通过引入辅助函数  $\varphi(x)$ , 对  $\varphi(x)$  应用罗尔定理来证明本定理.

证 首先注意到 $F(b) - F(a) \neq 0$. 这是由于

$$
F (b) - F (a) = F ^ {\prime} (\eta) (b - a),
$$

其中 $a < \eta < b$，根据假定 $F'(\eta) \neq 0$，又 $b - a \neq 0$，所以

$$
F (b) - F (a) \neq 0.
$$

设辅助函数

$$
\varphi (x) = f (x) - \frac {f (b) - f (a)}{F (b) - F (a)} F (x),
$$

显然，$\varphi(x)$ 在闭区间 $[a, b]$ 上连续，在开区间 $(a, b)$ 内可导，且

$$
\varphi (a) = \varphi (b) = \frac {F (b) f (a) - F (a) f (b)}{F (b) - F (a)},
$$

故 $\varphi (x)$ 适合罗尔定理的条件，因此在 $(a,b)$ 内至少有一点 $\xi$ ，使

$$
\varphi^ {\prime} (\xi) = f ^ {\prime} (\xi) - \frac {f (b) - f (a)}{F (b) - F (a)} F ^ {\prime} (\xi) = 0,
$$

由此得

$$
\frac {f (b) - f (a)}{F (b) - F (a)} = \frac {f ^ {\prime} (\xi)}{F ^ {\prime} (\xi)}.
$$

定理证毕.

很明显,如果取  $F(x)=x$ ,那么  $F(b)-F(a)=b-a,F'(x)=1$ ,因而公式(1-4)就可以写成

$$
f (b) - f (a) = f ^ {\prime} (\xi) (b - a) \quad (a <   \xi <   b),
$$

这样就变成拉格朗日中值公式了.

128

---

第二节 洛必达法则

## 习题3-1

1. 验证罗尔定理对函数  $y=\ln \sin x$  在区间  $\left[\frac{\pi}{6},\frac{5\pi}{6}\right]$  上的正确性.

2. 验证拉格朗日中值定理对函数 $y = 4x^{3} - 5x^{2} + x - 2$ 在区间[0,1]上的正确性.

3. 对函数 $f(x) = \sin x$ 及 $F(x) = x + \cos x$ 在区间 $\left[0, \frac{\pi}{2}\right]$ 上验证柯西中值定理的正确性.

4. 试证明对函数 $y = px^2 + qx + r$ 应用拉格朗日中值定理时所求得的点 $\xi$ 总是位于区间的正中间.

5. 不用求出函数 $f(x) = (x - 1)(x - 2)(x - 3)(x - 4)$ 的导数，说明方程 $f'(x) = 0$ 有几个实根，并指出它们所在的区间.

6. 证明恒等式: $\arcsin x + \arccos x = \frac{\pi}{2} (-1 \leqslant x \leqslant 1)$.

7. 若方程 $a_0x^n + a_1x^{n-1} + \cdots + a_{n-1}x = 0$ 有一个正根 $x = x_0$, 证明方程 $a_0nx^{n-1} + a_1(n-1)x^{n-2} + \cdots + a_{n-1} = 0$ 必有一个小于 $x_0$ 的正根.

8. 若函数 $f(x)$ 在[1,2]上具有二阶导数，且 $f(2) = 0$，又 $F(x) = (x - 1)^2 f(x)$，证明在(1,2)内至少存在一点 $\xi$，使 $F''(\xi) = 0$.

9. 设 $a > b > 0, n > 1$，证明:$nb^{n-1}(a-b) < a^n - b^n < na^{n-1}(a-b)$.

10. 设 a > b > 0，证明: $\frac{a - b}{a} < \ln \frac{a}{b} < \frac{a - b}{b}.$

11. 证明下列不等式:

(1)  $\left|\arctan a-\arctan b\right|\leqslant\left|a-b\right|;$

(2) 当 x>1 时,  $e^{x}>ex$ .

12. 证明方程  $x^{5}+x-1=0$  只有一个正根.

\*13. 设 $f(x), g(x)$ 在 $[a, b]$ 上连续，在 $(a, b)$ 内可导，证明在 $(a, b)$ 内有一点 $\xi$，使

$$
\left| \begin{array}{l l} f (a) & f (b) \\ g (a) & g (b) \end{array} \right| = (b - a) \left| \begin{array}{l l} f (a) & f ^ {\prime} (\xi) \\ g (a) & g ^ {\prime} (\xi) \end{array} \right|.
$$

14. 证明: 若函数 $y = f(x)$ 在 $(- \infty, +\infty)$ 内满足关系式 $f'(x) = f(x)$，且 $f(0) = 1$，则 $f(x) = \mathrm{e}^x$.

\* 15. 设函数 $y = f(x)$ 在 $x = 0$ 的某邻域内具有 $n$ 阶导数，且 $f(0) = f'(0) = \cdots = f^{(n-1)}(0) = 0$，试用柯西中值定理证明:

$$
\frac {f (x)}{x ^ {n}} = \frac {f ^ {(n)} (\theta x)}{n !} \quad (0 <   \theta <   1).
$$

## 第二节 洛必达法则

如果当 $x \to a$ （或 $x \to \infty$）时，两个函数 $f(x)$ 与 $F(x)$ 都趋于零或都趋于无穷大，那

129

---

第三章 微分中值定理与导数的应用

么极限 $\lim_{\substack{x\to a\\ (x\to \infty)}}\frac{f(x)}{F(x)}$ 可能存在、也可能不存在.通常把这种极限叫做未定式，并分别简记为 $\frac{0}{0}$ 或 $\frac{\infty}{\infty}$.在第一章第六节中讨论过的极限 $\lim_{x\to 0}\frac{\sin x}{x}$ 就是未定式 $\frac{0}{0}$ 的一个例子.对于这类极限，即使它存在也不能用“商的极限等于极限的商”这一法则.下面我们将根据柯西中值定理来推出求这类极限的一种简便且重要的方法.

我们着重讨论 $x \to a$ 时的未定式 $\frac{0}{0}$ 的情形, 关于这情形有以下定理:

## 定理1 设

(1) 当  $x \to a$  时, 函数  $f(x)$  及  $F(x)$  都趋于零;
(2) 在点 a 的某去心邻域内,  $f'(x)$  及  $F'(x)$  都存在且  $F'(x) \neq 0$ ;
(3) $\lim_{x\to a}\frac{f'(x)}{F'(x)}$ 存在（或为无穷大），

则

$$
\lim _ {x \to a} \frac {f (x)}{F (x)} = \lim _ {x \to a} \frac {f ^ {\prime} (x)}{F ^ {\prime} (x)}.
$$

这就是说,当 $\lim_{x\to a}\frac{f'(x)}{F'(x)}$ 存在时, $\lim_{x\to a}\frac{f(x)}{F(x)}$ 也存在且等于 $\lim_{x\to a}\frac{f'(x)}{F'(x)}$ ;当 $\lim_{x\to a}\frac{f'(x)}{F'(x)}$ 为无穷大时, $\lim_{x\to a}\frac{f(x)}{F(x)}$ 也是无穷大.这种在一定条件下通过分子、分母分别求导再求极限来确定未定式的值的方法称为洛必达(L'Hospital)法则.

证 因为求 $\frac{f(x)}{F(x)}$ 当 $x \to a$ 时的极限与 $f(a)$ 及 $F(a)$ 无关, 所以可以假定 $f(a) = F(a) = 0$, 于是由条件 (1)、(2) 知道, $f(x)$ 及 $F(x)$ 在点 $a$ 的某一邻域内是连续的. 设 $x$ 是这邻域内的一点, 那么在以 $x$ 及 $a$ 为端点的区间上, 柯西中值定理的条件均满足, 因此有

$$
\frac {f (x)}{F (x)} = \frac {f (x) - f (a)}{F (x) - F (a)} = \frac {f ^ {\prime} (\xi)}{F ^ {\prime} (\xi)} \quad (\xi \text {在} x \text {与} a \text {之间}).
$$

令 $x \to a$，并对上式两端求极限，注意到 $x \to a$ 时 $\xi \to a$，再根据条件(3)便得要证明的结论.

如果 $\frac{f'(x)}{F'(x)}$ 当 $x \to a$ 时仍属 $\frac{0}{0}$ 型，且这时 $f'(x), F'(x)$ 能满足定理中 $f(x), F(x)$ 所要满足的条件，那么可以继续使用洛必达法则先确定 $\lim_{x \to a} \frac{f'(x)}{F'(x)}$，从而确定 $\lim_{x \to a} \frac{f(x)}{F(x)}$，即

$$
\lim _ {x \to a} \frac {f (x)}{F (x)} = \lim _ {x \to a} \frac {f ^ {\prime} (x)}{F ^ {\prime} (x)} = \lim _ {x \to a} \frac {f ^ {\prime \prime} (x)}{F ^ {\prime \prime} (x)}.
$$

130

---

第二节 洛必达法则

且可以以此类推.

例 1 求  $\lim_{x\to0}\frac{\sin ax}{\sin bx}$  ( $b\neq0$ ).

解 $\lim_{x\to 0}\frac{\sin ax}{\sin bx} = \lim_{x\to 0}\frac{a\cos ax}{b\cos bx} = \frac{a}{b}.$

例2 求 $\lim_{x\to 1}\frac{x^3 - 3x + 2}{x^3 - x^2 - x + 1}.$

解 $\lim_{x\to 1}\frac{x^3 - 3x + 2}{x^3 - x^2 - x + 1} = \lim_{x\to 1}\frac{3x^2 - 3}{3x^2 - 2x - 1} = \lim_{x\to 1}\frac{6x}{6x - 2} = \frac{3}{2}.$

注意,上式中的 $\lim_{x\to1}\frac{6x}{6x-2}$ 已不是未定式,不能对它应用洛必达法则,否则要导致错误结果.以后使用洛必达法则时应当经常注意这一点,如果不是未定式,那么就不能应用洛必达法则.

例3 求 $\lim_{x\to 0}\frac{x - \sin x}{x^3}.$

解  $\lim_{x\to0}\frac{x-\sin x}{x^{3}}=\lim_{x\to0}\frac{1-\cos x}{3x^{2}}=\lim_{x\to0}\frac{\sin x}{6x}=\frac{1}{6}.$

我们指出,对于 $x\to\infty$ 时的未定式 $\frac{0}{0}$ 以及对于 $x\to a$ 或 $x\to\infty$ 时的未定式 $\frac{\infty}{\infty}$ ，也有相应的洛必达法则.例如，对于 $x\to\infty$ 时的未定式 $\frac{0}{0}$ 有以下定理:

## 定理2 设

(1) 当  $x \to \infty$  时, 函数  $f(x)$  及  $F(x)$  都趋于零;
(2) 当  $\left|x\right|>N$  时  $f'(x)$  与  $F'(x)$  都存在, 且  $F'(x)\neq0$ ;
(3) $\lim_{x\to \infty}\frac{f'(x)}{F'(x)}$ 存在（或为无穷大），

则

$$
\lim _ {x \to \infty} \frac {f (x)}{F (x)} = \lim _ {x \to \infty} \frac {f ^ {\prime} (x)}{F ^ {\prime} (x)}.
$$

例4 求 $\lim_{x\to +\infty}\frac{\frac{\pi}{2} - \arctan x}{\frac{1}{x}}.$

解 $\lim_{x\to +\infty}\frac{\frac{\pi}{2} - \arctan x}{\frac{1}{x}} = \lim_{x\to +\infty}\frac{-\frac{1}{1 + x^2}}{-\frac{1}{x^2}} = \lim_{x\to +\infty}\frac{x^2}{1 + x^2} = 1.$

131

---

第三章 微分中值定理与导数的应用

例 5 求  $\lim_{x\to+\infty}\frac{\ln x}{x^{n}}(n>0)$ .

解 $\lim_{x\to +\infty}\frac{\ln x}{x^n} = \lim_{x\to +\infty}\frac{\frac{1}{x}}{nx^{n - 1}} = \lim_{x\to +\infty}\frac{1}{nx^n} = 0.$

例6 求 $\lim_{x\to +\infty}\frac{x^n}{\mathrm{e}^{\lambda x}} (n$ 为正整数， $\lambda >0)$

解 相继应用洛必达法则 n 次, 得

$$
\lim _ {x \to + \infty} \frac {x ^ {n}}{\mathrm{e} ^ {\lambda x}} = \lim _ {x \to + \infty} \frac {n x ^ {n - 1}}{\lambda \mathrm{e} ^ {\lambda x}} = \lim _ {x \to + \infty} \frac {n (n - 1) x ^ {n - 2}}{\lambda^ {2} \mathrm{e} ^ {\lambda x}} = \dots = \lim _ {x \to + \infty} \frac {n !}{\lambda^ {n} \mathrm{e} ^ {\lambda x}} = 0.
$$

事实上,如果例6中的n不是正整数而是任何正数,那么极限仍为零.

对数函数  $y=\ln x$  、幂函数  $y=x^{n}\quad(n>0)$  、指数函数  $y=e^{\lambda x}\quad(\lambda>0)$  均为当  $x\to+\infty$  时的无穷大，但从例 5、例 6 可以看出，这三个函数增大的“速度”是很不一样的，幂函数增大的“速度”比对数函数快得多，而指数函数增大的“速度”又比幂函数快得多。

下表列出了 $x$ 分别取10,100,1000时， $\ln x,\sqrt{x},x^2$ 及 $\mathrm{e}^x$ 相应的值.从中可以看出当$x$ 增大时这几个函数增大“速度”快慢的情况

| x | 10 | 100 | 1 000 |
| --- | --- | --- | --- |
| ln x | 2.3 | 4.6 | 6.9 |
| $\sqrt{x}$ | 3.2 | 10 | 31.6 |
| $x^2$ | 100 | $10^4$ | $10^6$ |
| $e^x$ | $2.20×10^4$ | $2.69×10^{43}$ | $1.97×10^{434}$ |

其他还有一些 $0 \cdot \infty, \infty - \infty, 0^0, 1^\infty, \infty^0$ 型的未定式，也可通过 $\frac{0}{0}$ 或 $\frac{\infty}{\infty}$ 型的未定式来计算，下面用例子说明.

例 7 求  $\lim_{x\to0^{+}}x^{n}\ln x$  (n>0).

解 这是未定式 $0 \cdot \infty$. 因为

$$
x ^ {n} \ln x = \frac {\ln x}{\frac {1}{x ^ {n}}},
$$

当 $x \to 0^{+}$时，上式右端是未定式 $\frac{\infty}{\infty}$，应用洛必达法则，得

$$
\lim _ {x \to 0 ^ {+}} x ^ {n} \ln x = \lim _ {x \to 0 ^ {+}} \frac {\ln x}{x ^ {- n}} = \lim _ {x \to 0 ^ {+}} \frac {\frac {1}{x}}{- n x ^ {- n - 1}} = \lim _ {x \to 0 ^ {+}} \left(\frac {- x ^ {n}}{n}\right) = 0.
$$

释疑解难
3-1

132

---

第二节 洛必达法则

例8 求 $\lim_{x\to \frac{\pi}{2}}(\sec x - \tan x)$

解 这是未定式 $\infty -\infty$ .因为

$$
\sec x - \tan x = \frac {1 - \sin x}{\cos x},
$$

当 $x \to \frac{\pi}{2}$ 时，上式右端是未定式 $\frac{0}{0}$，应用洛必达法则，得

$$
\lim _ {x \to \frac {\pi}{2}} (\sec x - \tan x) = \lim _ {x \to \frac {\pi}{2}} \frac {1 - \sin x}{\cos x} = \lim _ {x \to \frac {\pi}{2}} \frac {- \cos x}{- \sin x} = 0.
$$

例9 求 $\lim_{x\to 0^{+}}x^{x}$

解 这是未定式 $0^0$ 设 $y = x^x$ ，两端取对数得

$$
\ln y = x \ln x,
$$

当 $x \to 0^{+}$时，上式右端是未定式 $0 \cdot \infty$。应用例7的结果，得

$$
\lim _ {x \to 0 ^ {+}} \ln y = \lim _ {x \to 0 ^ {+}} (x \ln x) = 0.
$$

因为 $y = \mathrm{e}^{\ln y}$ ，而 $\lim y = \lim \mathrm{e}^{\ln y} = \mathrm{e}^{\lim \ln y}$ （当 $x\to 0^{+}$ ），所以

$$
\lim _ {x \to 0 ^ {+}} x ^ {x} = \lim _ {x \to 0 ^ {+}} y = \mathrm{e} ^ {0} = 1.
$$

洛必达法则是求未定式的一种有效方法,但最好能与其他求极限的方法结合使用.例如能化简时应尽可能先化简,可以应用等价无穷小替换或重要极限时,应尽可能应用,这样可以使运算简捷.

例10 求 $\lim_{x\to 0}\frac{\tan x - x}{x^2\sin x}.$

解 如果直接用洛必达法则,那么分母的导数(尤其是高阶导数)较繁.如果作一个等价无穷小替换,那么运算就方便得多.其运算如下:

$$
\lim _ {x \to 0} \frac {\tan x - x}{x ^ {2} \sin x} = \lim _ {x \to 0} \frac {\tan x - x}{x ^ {3}} = \lim _ {x \to 0} \frac {\sec^ {2} x - 1}{3 x ^ {2}} = \lim _ {x \to 0} \frac {2 \sec^ {2} x \tan x}{6 x} = \frac {1}{3} \lim _ {x \to 0} \frac {\tan x}{x} = \frac {1}{3}.
$$

最后,我们指出,本节定理给出的是求未定式的一种方法.当定理条件满足时,所求的极限当然存在(或为 $\infty$ ),但当定理条件不满足时,所求极限却不一定不存在,这就是说,当 $\lim\frac{f'(x)}{F'(x)}$ 不存在时(等于无穷大的情况除外), $\lim\frac{f(x)}{F(x)}$ 仍可能存在(见本节习题第2、第3题).

## 习题3-2

1. 用洛必达法则求下列极限:

133

例题精讲
3-2

---

第三章 微分中值定理与导数的应用

(1) $\lim_{x\to 0}\frac{\ln(1 + x)}{x};$

(2) $\lim_{x\to 0}\frac{\mathrm{e}^x - \mathrm{e}^{-x}}{\sin x};$

(3) $\lim_{x\to 0}\frac{\tan{x} - x}{x - \sin{x}};$

(4) $\lim_{x\to \pi}\frac{\sin{3}x}{\tan{5}x};$

(5) $\lim_{x\to \frac{\pi}{2}}\frac{\ln\sin x}{(\pi - 2x)^{2}};$

(6) $\lim_{x\to a}\frac{x^m - a^m}{x^n - a^n} (a\neq 0);$

(7)  $\lim_{x\to0^{+}}\frac{\ln\tan7x}{\ln\tan2x};$

(8)  $\lim_{x\to\frac{\pi}{2}}\frac{\tan x}{\tan3x};$

(9)  $\lim_{x\to+\infty}\frac{\ln\left(1+\frac{1}{x}\right)}{\operatorname{arccot}x};$

(10)  $\lim_{x\to0}\frac{\ln(1+x^{2})}{\sec x-\cos x};$

(11)  $\lim_{x\to0}x\cot2x;$

(12) $\lim_{x\to 0}x^2\mathrm{e}^{\frac{1}{x^2}};$

(13)  $\lim_{x\to1}\left(\frac{2}{x^{2}-1}-\frac{1}{x-1}\right)$ ;

(14)  $\lim_{x\to0}(e^{x}+x)^{\frac{1}{x}}$ ;

(15)  $\lim_{x\to0^{+}}x^{\sin x}$ ;

(16) $\lim_{x\to 0^{+}}\left(\frac{1}{x}\right)^{\tan x}.$

2. 验证极限  $\lim_{x\to\infty}\frac{x+\sin x}{x}$  存在, 但不能用洛必达法则得出.

3. 验证极限 $\lim_{x\to 0}\frac{x^2\sin\frac{1}{x}}{\sin x}$ 存在, 但不能用洛必达法则得出.

\* 4. 讨论函数

$$
f (x) = \left\{ \begin{array}{l l} {\left[ \frac {(1 + x) ^ {\frac {1}{x}}}{\mathrm{e}} \right] ^ {\frac {1}{x}},} & {x > 0,} \\ {\mathrm{e} ^ {- \frac {1}{2}},} & {x \leqslant 0} \end{array} \right.
$$

在点 x=0 处的连续性.

## 第三节 泰勒公式

对于一些较复杂的函数,为了便于研究,往往希望用一些简单的函数来近似表达.由于用多项式表示的函数,只要对自变量进行有限次加、减、乘三种算术运算,便能求出它的函数值来,因此我们经常用多项式来近似表达函数.

在微分的应用中已经知道, 当  $\left|x\right|$  很小时, 有如下的近似等式:

$$
\mathrm{e} ^ {x} \approx 1 + x, \quad \ln (1 + x) \approx x.
$$

这些都是用一次多项式来近似表达函数的例子. 显然, 在 $x = 0$ 处这些一次多项式及其一阶导数的值, 分别等于被近似表达的函数及其导数的相应值.

但是这种近似表达式的精确度不高,它所产生的误差仅是关于 x 的高阶无穷小.为了提高精确度,自然想到用更高次的多项式来逼近函数.于是,提出如下问题:

设 $f(x)$ 在 $x_0$ 处具有 $n$ 阶导数，试找出一个关于 $x - x_0$ 的 $n$ 次多项式

134

---

第三节 泰勒公式

$$
p _ {n} (x) = a _ {0} + a _ {1} \left(x - x _ {0}\right) + a _ {2} \left(x - x _ {0}\right) ^ {2} + \dots + a _ {n} \left(x - x _ {0}\right) ^ {n} \tag {3-1}
$$

来近似表达 $f(x)$ ，要求使得 $p_n(x)$ 与 $f(x)$ 之差是当 $x \to x_0$ 时比 $(x - x_0)^n$ 高阶的无穷小.

下面我们来讨论这个问题. 假设  $p_{n}(x)$  在  $x_{0}$  处的函数值及它的直到 n 阶导数在  $x_{0}$  处的值依次与  $f(x_{0})$ ,  $f'(x_{0})$ ,  $\cdots$ ,  $f^{(n)}(x_{0})$  相等, 即满足

$$
p _ {n} (x _ {0}) = f (x _ {0}), \quad p _ {n} ^ {\prime} (x _ {0}) = f ^ {\prime} (x _ {0}), \quad p _ {n} ^ {\prime \prime} (x _ {0}) = f ^ {\prime \prime} (x _ {0}), \quad \dots , \quad p _ {n} ^ {(n)} (x _ {0}) = f ^ {(n)} (x _ {0}),
$$

按这些等式来确定多项式(3-1)的系数 $a_{0},a_{1},a_{2},\cdots,a_{n}$ .为此,对(3-1)式求各阶导数,然后分别代入以上等式,得

$$
a _ {0} = f (x _ {0}), \quad 1 \cdot a _ {1} = f ^ {\prime} (x _ {0}), \quad 2! a _ {2} = f ^ {\prime \prime} (x _ {0}), \quad \dots , \quad n! a _ {n} = f ^ {(n)} (x _ {0}),
$$

即得

$$
a _ {0} = f (x _ {0}), \quad a _ {1} = f ^ {\prime} (x _ {0}), \quad a _ {2} = \frac {1}{2 !} f ^ {\prime \prime} (x _ {0}), \quad \dots , \quad a _ {n} = \frac {1}{n !} f ^ {(n)} (x _ {0}).
$$

将求得的系数 $a_0, a_1, a_2, \dots, a_n$ 代入(3-1)式，有

$$
p _ {n} (x) = f \left(x _ {0}\right) + f ^ {\prime} \left(x _ {0}\right) \left(x - x _ {0}\right) + \frac {f ^ {\prime \prime} \left(x _ {0}\right)}{2 !} \left(x - x _ {0}\right) ^ {2} + \dots + \frac {f ^ {(n)} \left(x _ {0}\right)}{n !} \left(x - x _ {0}\right) ^ {n}. \tag {3-2}
$$

下面的定理表明,多项式(3-2)的确是所要找的 n 次多项式.

泰勒(Taylor)中值定理1 如果函数 $f(x)$ 在 $x_0$ 处具有 $n$ 阶导数, 那么存在 $x_0$ 的一个邻域, 对于该邻域内的任一 $x$, 有

$$
f (x) = f (x _ {0}) + f ^ {\prime} (x _ {0}) (x - x _ {0}) + \frac {f ^ {\prime \prime} (x _ {0})}{2 !} (x - x _ {0}) ^ {2} + \dots + \frac {f ^ {(n)} (x _ {0})}{n !} (x - x _ {0}) ^ {n} + R _ {n} (x), \tag {3-3}
$$

其中

$$
R _ {n} (x) = o \left(\left(x - x _ {0}\right) ^ {n}\right). \tag {3-4}
$$

证 记 $R_{n}(x) = f(x) - p_{n}(x)$，则

$$
R _ {n} (x _ {0}) = R _ {n} ^ {\prime} (x _ {0}) = R _ {n} ^ {\prime \prime} (x _ {0}) = \dots = R _ {n} ^ {(n)} (x _ {0}) = 0.
$$

由于 $f(x)$ 在 $x_0$ 处有 $n$ 阶导数，因此 $f(x)$ 必在 $x_0$ 的某邻域内存在 $n - 1$ 阶导数，从而$R_{n}(x)$ 也在该邻域内 $n - 1$ 阶可导，反复应用洛必达法则，得

$$
\begin{array}{l} \lim _ {x \to x _ {0}} \frac {R _ {n} (x)}{(x - x _ {0}) ^ {n}} = \lim _ {x \to x _ {0}} \frac {R _ {n} ^ {\prime} (x)}{n (x - x _ {0}) ^ {n - 1}} = \lim _ {x \to x _ {0}} \frac {R _ {n} ^ {\prime \prime} (x)}{n (n - 1) (x - x _ {0}) ^ {n - 2}} = \dots \\ = \lim _ {x \to x _ {0}} \frac {R _ {n} ^ {(n - 1)} (x)}{n ! (x - x _ {0})} = \frac {1}{n !} \lim _ {x \to x _ {0}} \frac {R _ {n} ^ {(n - 1)} (x) - R _ {n} ^ {(n - 1)} (x _ {0})}{x - x _ {0}} = \frac {1}{n !} R _ {n} ^ {(n)} (x _ {0}) = 0, \\ \end{array}
$$

因此 $R_{n}(x) = o((x - x_{0})^{n})$ ，定理证毕.

多项式(3-2)称为函数 $f(x)$ 在 $x_0$ 处（或按 $x - x_0$ 的幂展开）的 $n$ 次泰勒多项式，公式(3-3)称为 $f(x)$ 在 $x_0$ 处（或按 $x - x_0$ 的幂展开）的带有佩亚诺(Peano)余项的 $n$ 阶泰勒公式，而 $R_{n}(x)$ 的表达式(3-4)称为佩亚诺余项，它就是用 $n$ 次泰勒多项式来近似

135

---

第三章 微分中值定理与导数的应用

表达 $f(x)$ 所产生的误差，这一误差是当 $x \to x_0$ 时比 $(x - x_0)^n$ 高阶的无穷小，但不能由它具体估算出误差的大小。下面给出的具有另一种余项形式的泰勒定理则解决了这一问题。

泰勒中值定理2 如果函数 $f(x)$ 在 $x_0$ 的某个邻域 $U(x_0)$ 内具有 $n + 1$ 阶导数，那么对任一 $x \in U(x_0)$，有

$$
\begin{array}{l} f (x) = f \left(x _ {0}\right) + f ^ {\prime} \left(x _ {0}\right) \left(x - x _ {0}\right) + \frac {f ^ {\prime \prime} \left(x _ {0}\right)}{2 !} \left(x - x _ {0}\right) ^ {2} + \dots + \\ \frac {f ^ {(n)} (x _ {0})}{n !} (x - x _ {0}) ^ {n} + R _ {n} (x), \tag {3-5} \\ \end{array}
$$

其中

$$
R _ {n} (x) = \frac {f ^ {(n + 1)} (\xi)}{(n + 1) !} (x - x _ {0}) ^ {n + 1}, \tag {3-6}
$$

这里  $\xi$  是  $x_{0}$  与 x 之间的某个值.

证 记 $R_{n}(x) = f(x) - p_{n}(x)$. 只需证明

$$
R _ {n} (x) = \frac {f ^ {(n + 1)} (\xi)}{(n + 1) !} (x - x _ {0}) ^ {n + 1} \quad (\xi \text {在} x _ {0} \text {与} x \text {之间}).
$$

由假设可知, $R_{n}(x)$ 在 $U(x_{0})$ 内具有 $n+1$ 阶导数,且

$$
R _ {n} (x _ {0}) = R _ {n} ^ {\prime} (x _ {0}) = R _ {n} ^ {\prime \prime} (x _ {0}) = \dots = R _ {n} ^ {(n)} (x _ {0}) = 0.
$$

对两个函数  $R_{n}(x)$  及  $(x-x_{0})^{n+1}$  在以  $x_{0}$  及 x 为端点的区间上应用柯西中值定理（显然，这两个函数满足柯西中值定理的条件），得

$$
\frac {R _ {n} (x)}{(x - x _ {0}) ^ {n + 1}} = \frac {R _ {n} (x) - R _ {n} (x _ {0})}{(x - x _ {0}) ^ {n + 1} - 0} = \frac {R _ {n} ^ {\prime} (\xi_ {1})}{(n + 1) (\xi_ {1} - x _ {0}) ^ {n}} \quad (\xi_ {1} \text {在} x _ {0} \text {与} x \text {之间}),
$$

再对两个函数 $R_{n}^{\prime}(x)$ 与 $(n + 1)(x - x_0)^n$ 在以 $x_0$ 及 $\xi_{1}$ 为端点的区间上应用柯西中值定理，得

$$
\frac {R _ {n} ^ {\prime} (\xi_ {1})}{(n + 1) (\xi_ {1} - x _ {0}) ^ {n}} = \frac {R _ {n} ^ {\prime} (\xi_ {1}) - R _ {n} ^ {\prime} (x _ {0})}{(n + 1) (\xi_ {1} - x _ {0}) ^ {n} - 0} = \frac {R _ {n} ^ {\prime \prime} (\xi_ {2})}{(n + 1) n (\xi_ {2} - x _ {0}) ^ {n - 1}} \quad (\xi_ {2} \text {在} x _ {0} \text {与} \xi_ {1} \text {之间}).
$$

照此方法继续做下去, 经过  $n+1$  次后, 得

$$
\frac {R _ {n} (x)}{(x - x _ {0}) ^ {n + 1}} = \frac {R _ {n} ^ {(n + 1)} (\xi)}{(n + 1) !} \quad (\xi \text {在} x _ {0} \text {与} \xi_ {n} \text {之间}, \text {因而也在} x _ {0} \text {与} x \text {之间}).
$$

注意到 $R_{n}^{(n + 1)}(x) = f^{(n + 1)}(x)$ （因 $p_n^{(n + 1)}(x) = 0$），则由上式得

$$
R _ {n} (x) = \frac {f ^ {(n + 1)} (\xi)}{(n + 1) !} (x - x _ {0}) ^ {n + 1} \quad (\xi \text {在} x _ {0} \text {与} x \text {之间}),
$$

定理证毕.

公式(3-5)称为 $f(x)$ 在 $x_{0}$ 处(或按 $x-x_{0}$ 的幂展开)的带有拉格朗日余项的n阶泰

136

---

第三节 泰勒公式

勒公式,而  $R_{n}(x)$  的表达式(3-6)称为拉格朗日余项.

当 $n = 0$ 时, 泰勒公式(3-5)变成拉格朗日中值公式

$$
f (x) = f (x _ {0}) + f ^ {\prime} (\xi) (x - x _ {0}) \quad (\xi \text {在} x _ {0} \text {与} x \text {之间}).
$$

因此,泰勒中值定理2是拉格朗日中值定理的推广.

由泰勒中值定理2可知，以多项式 $p_n(x)$ 近似表达函数 $f(x)$ 时，其误差为$\left|R_n(x)\right|$.如果对于某个固定的 $n$ ，当 $x\in U(x_0)$ 时， $\left|f^{(n + 1)}(x)\right|\leqslant M$ ，那么有估计式

$$
\mid R _ {n} (x) \mid = \left| \frac {f ^ {(n + 1)} (\xi)}{(n + 1) !} (x - x _ {0}) ^ {n + 1} \right| \leqslant \frac {M}{(n + 1) !} \mid x - x _ {0} \mid^ {n + 1}. \tag {3-7}
$$

在泰勒公式(3-3)中,如果取 $x_{0}=0$ ,那么有带有佩亚诺余项的麦克劳林(Maclaurin)公式

$$
f (x) = f (0) + f ^ {\prime} (0) x + \dots + \frac {f ^ {(n)} (0)}{n !} x ^ {n} + o (x ^ {n}). \tag {3-8}
$$

在泰勒公式(3-5)中, 如果取 $x_0 = 0$, 那么 $\xi$ 在 0 与 $x$ 之间. 因此可以令 $\xi = \theta x (0 < \theta < 1)$, 从而泰勒公式(3-5)变成较简单的形式, 即所谓带有拉格朗日余项的麦克劳林公式

$$
f (x) = f (0) + f ^ {\prime} (0) x + \frac {f ^ {\prime \prime} (0)}{2 !} x ^ {2} + \dots + \frac {f ^ {(n)} (0)}{n !} x ^ {n} + \frac {f ^ {(n + 1)} (\theta x)}{(n + 1) !} x ^ {n + 1} \quad (0 <   \theta <   1). \tag {3-9}
$$

由(3-8)或(3-9)可得近似公式

$$
f (x) \approx f (0) + f ^ {\prime} (0) x + \frac {f ^ {\prime \prime} (0)}{2 !} x ^ {2} + \dots + \frac {f ^ {(n)} (0)}{n !} x ^ {n},
$$

误差估计式(3-7)相应地变成

$$
\mid R _ {n} (x) \mid \leqslant \frac {M}{(n + 1) !} \mid x \mid^ {n + 1}. \tag {3-10}
$$

例 1 写出函数  $f(x)=\mathrm{e}^{x}$  的带有拉格朗日余项的 n 阶麦克劳林公式.

解 因为

$$
f ^ {\prime} (x) = f ^ {\prime \prime} (x) = \dots = f ^ {(n)} (x) = \mathrm{e} ^ {x},
$$

所以

$$
f (0) = f ^ {\prime} (0) = f ^ {\prime \prime} (0) = \dots = f ^ {(n)} (0) = 1.
$$

把这些值代入公式(3-9)，并注意到 $f^{(n + 1)}(\theta x) = \mathrm{e}^{\theta x}$ 便得

$$
\mathrm{e} ^ {x} = 1 + x + \frac {x ^ {2}}{2 !} + \dots + \frac {x ^ {n}}{n !} + \frac {\mathrm{e} ^ {\theta x}}{(n + 1) !} x ^ {n + 1} \quad (0 <   \theta <   1).
$$

由这个公式可知,若把  $e^{x}$  用它的 n 次泰勒多项式表达为

$$
\mathrm{e} ^ {x} \approx 1 + x + \frac {x ^ {2}}{2 !} + \dots + \frac {x ^ {n}}{n !},
$$

释疑解难

3-2

137

---

第三章 微分中值定理与导数的应用

这时所产生的误差为

$$
\mid R _ {n} (x) \mid = \left| \frac {\mathrm{e} ^ {\theta x}}{(n + 1) !} x ^ {n + 1} \right| <   \frac {\mathrm{e} ^ {| x |}}{(n + 1) !} \mid x \mid^ {n + 1} \quad (0 <   \theta <   1).
$$

如果取 $x = 1$ ，则得无理数 $\mathbf{e}$ 的近似式为

$$
e \approx 1 + 1 + \frac {1}{2 !} + \dots + \frac {1}{n !},
$$

其误差

$$
\mid R _ {n} \mid <   \frac {\mathrm{e}}{(n + 1) !} <   \frac {3}{(n + 1) !}.
$$

当 n=10 时, 可算出  $e \approx 2.718\ 282$ , 其误差不超过  $10^{-6}$ .

例 2 求  $f(x)=\sin x$  的带有拉格朗日余项的 n 阶麦克劳林公式.

解 因为

$$
f ^ {\prime} (x) = \cos x, \quad f ^ {\prime \prime} (x) = - \sin x, \quad f ^ {\prime \prime \prime} (x) = - \cos x,
$$

$$
f ^ {(4)} (x) = \sin x, \quad \dots , \quad f ^ {(n)} (x) = \sin \left(x + \frac {n \pi}{2}\right),
$$

所以

$$
f (0) = 0, f ^ {\prime} (0) = 1, f ^ {\prime \prime} (0) = 0, f ^ {\prime \prime \prime} (0) = - 1, f ^ {(4)} (0) = 0
$$

等. 它们顺序循环地取四个数 0,1,0,-1, 于是按公式(3-9)得(令 n=2m)

$$
\sin x = x - \frac {x ^ {3}}{3 !} + \frac {x ^ {5}}{5 !} - \dots + (- 1) ^ {m - 1} \frac {x ^ {2 m - 1}}{(2 m - 1) !} + R _ {2 m} (x),
$$

其中

$$
R _ {2 m} (x) = \frac {\sin \left[ \theta x + (2 m + 1) \frac {\pi}{2} \right]}{(2 m + 1) !} x ^ {2 m + 1} = (- 1) ^ {m} \frac {\cos \theta x}{(2 m + 1) !} x ^ {2 m + 1} \quad (0 <   \theta <   1).
$$

如果取 m=1，那么得近似公式

$$
\sin x \approx x,
$$

这时误差为

$$
| R _ {2} | = \left| - \frac {\cos \theta x}{3 !} x ^ {3} \right| \leqslant \frac {| x | ^ {3}}{6} \quad (0 <   \theta <   1).
$$

如果 $m$ 分别取2和3,那么可得 $\sin x$ 的3次和5次泰勒多项式

$$
\sin x \approx x - \frac {1}{3 !} x ^ {3} \quad \text {和} \quad \sin x \approx x - \frac {1}{3 !} x ^ {3} + \frac {1}{5 !} x ^ {5},
$$

其误差的绝对值依次不超过 $\frac{1}{5!} |x|^5$ 和 $\frac{1}{7!} |x|^7$. 以上三个泰勒多项式及正弦函数的图形都画在图3-3中, 以便于比较.

138

---

第三节 泰勒公式

![](../../raw/pages_0129-0160/images/page_155_chart_1.jpg)

<details>
<summary>line</summary>

| Function | Equation |
| --- | --- |
| Linear function | y=x |
| Parabola function | y=sin x |
| Quadrilateral function | \(y=x - \frac{1}{6}x^{3} + \frac{1}{120}x^{5}\) |
</details>

图3-3

类似地,还可以得到

$$
\cos x = 1 - \frac {1}{2 !} x ^ {2} + \frac {1}{4 !} x ^ {4} - \dots + (- 1) ^ {m} \frac {1}{(2 m) !} x ^ {2 m} + R _ {2 m + 1} (x),
$$

其中 $R_{2m + 1}(x) = \frac{\cos[\theta x + (m + 1)\pi]}{(2m + 2)!} x^{2m + 2} = (-1)^{m + 1}\frac{\cos\theta x}{(2m + 2)!} x^{2m + 2}$ （ $0 <   \theta <  1$ ）；

$$
\ln (1 + x) = x - \frac {1}{2} x ^ {2} + \frac {1}{3} x ^ {3} - \dots + (- 1) ^ {n - 1} \frac {1}{n} x ^ {n} + R _ {n} (x),
$$

其中 $R_{n}(x) = \frac{(-1)^{n}}{(n + 1)(1 + \theta x)^{n + 1}} x^{n + 1}$ （$0 < \theta < 1$）；

$$
(1 + x) ^ {\alpha} = 1 + \alpha x + \frac {\alpha (\alpha - 1)}{2 !} x ^ {2} + \dots + \frac {\alpha (\alpha - 1) \cdot \cdots \cdot (\alpha - n + 1)}{n !} x ^ {n} + R _ {n} (x),
$$

其中 $R_{n}(x) = \frac{\alpha(\alpha - 1)\cdot\cdots\cdot(\alpha - n + 1)(\alpha - n)}{(n + 1)!} (1 + \theta x)^{\alpha - n - 1}x^{n + 1}$ （$0 < \theta < 1$）.

由以上带有拉格朗日余项的麦克劳林公式,易得相应的带有佩亚诺余项的麦克劳林公式,读者可自行写出.

例3 利用带有佩亚诺余项的麦克劳林公式, 求极限 $\lim_{x\to 0}\frac{\sin x - x\cos x}{\sin^3 x}$.

解 由于分式的分母 $\sin^3 x \sim x^3 (x \to 0)$, 我们只需将分子中的 $\sin x$ 和 $x \cos x$ 分别用带有佩亚诺余项的 3 阶麦克劳林公式表示, 即

$$
\sin x = x - \frac {x ^ {3}}{3 !} + o (x ^ {3}), \quad x \cos x = x - \frac {x ^ {3}}{2 !} + o (x ^ {3}).
$$

于是

$$
\sin x - x \cos x = x - \frac {x ^ {3}}{3 !} + o (x ^ {3}) - x + \frac {x ^ {3}}{2 !} - o (x ^ {3}) = \frac {1}{3} x ^ {3} + o (x ^ {3}),
$$

139

---

第三章 微分中值定理与导数的应用

对上式作运算时,把两个比  $x^{3}$  高阶的无穷小的代数和仍记作  $o(x^{3})$ , 故

![](../../raw/pages_0129-0160/images/page_156_image_2.jpg)

例题精讲

3-3

$$
\lim _ {x \to 0} \frac {\sin x - x \cos x}{\sin^ {3} x} = \lim _ {x \to 0} \frac {\frac {1}{3} x ^ {3} + o (x ^ {3})}{x ^ {3}} = \frac {1}{3}.
$$

## 习题 3-3

1. 按 $x - 4$ 的幂展开多项式 $f(x) = x^4 - 5x^3 + x^2 - 3x + 4$.
2. 应用麦克劳林公式, 按 x 的幂展开函数  $f(x)=(x^{2}-3x+1)^{3}$ .
3. 求函数  $f(x)=\sqrt{x}$  按 x-4 的幂展开的带有拉格朗日余项的 3 阶泰勒公式.
4. 求函数  $f(x)=\ln x$  按 x-2 的幂展开的带有佩亚诺余项的 n 阶泰勒公式.
5. 求函数 $f(x) = \frac{1}{x}$ 按 $x + 1$ 的幂展开的带有拉格朗日余项的 $n$ 阶泰勒公式.
6. 求函数  $f(x)=\tan x$  的带有佩亚诺余项的 3 阶麦克劳林公式.
7. 求函数  $f(x)=xe^{x}$  的带有佩亚诺余项的 n 阶麦克劳林公式.
9. 应用 3 阶泰勒公式求下列各数的近似值, 并估计误差:

8. 验证当 $0 < x \leqslant \frac{1}{2}$ 时，按公式 $\mathrm{e}^x \approx 1 + x + \frac{x^2}{2} + \frac{x^3}{6}$ 计算 $\mathrm{e}^x$ 的近似值时，所产生的误差小于0.01，并求 $\sqrt{\mathrm{e}}$ 的近似值，使误差小于0.01.

(1)  $\sqrt[3]{30}$ ;

(2) $\sin 18^{\circ}$.

\* 10. 利用泰勒公式求下列极限:

(1) $\lim_{x\to +\infty}(\sqrt[3]{x^3 + 3x^2} -\sqrt[4]{x^4 - 2x^3})$

(2) $\lim_{x\to 0}\frac{\cos x - e^{-\frac{x^2}{2}}}{x^2[x + \ln(1 - x)]};$

(3) $\lim_{x\to 0}\frac{1 + \frac{1}{2}x^2 - \sqrt{1 + x^2}}{(\cos x - e^{x^2})\sin x^2};$

(4) $\lim_{x\to \infty}\left[x - x^2\ln \left(1 + \frac{1}{x}\right)\right].$

11. 若函数 $f(x)$ 在 $(- \infty, +\infty)$ 内具有二阶导数，且 $f''(x) > 0$，又 $\lim_{x \to 0} \frac{f(x)}{x} = 1$，证明:$f(x) \geqslant x, x \in (-\infty, +\infty)$.

## 第四节 函数的单调性与曲线的凹凸性

## 一、函数单调性的判定法

第一章第一节中已经介绍了函数在区间上单调的概念.下面利用导数来对函数的

140

---

第四节 函数的单调性与曲线的凹凸性

单调性进行研究.

如果函数 $y = f(x)$ 在 $[a, b]$ 上单调增加（单调减少），那么它的图形是一条沿 $x$ 轴正向上升（下降）的曲线。这时，如图3-4，曲线上各点处的切线斜率是非负的（是非正的），即 $y' = f'(x) \geqslant 0$ ($y' = f'(x) \leqslant 0$)。由此可见，函数的单调性与导数的符号有着密切的联系。

![](../../raw/pages_0129-0160/images/page_157_chart_3.jpg)

<details>
<summary>line</summary>

| Point | X | Y |
| --- | --- | --- |
| A | a | ~0.2 |
| Intersection (y=f(x), x) | b | ~0.5 |
| B | b | >0.8 |
</details>

(a) 函数图形上升时切线斜率非负

![](../../raw/pages_0129-0160/images/page_157_chart_5.jpg)

<details>
<summary>line</summary>

| Point | x | y |
| --- | --- | --- |
| A | a | ~0.8 |
| B | b | ~0.3 |
</details>

(b) 函数图形下降时切线斜率非正

图3-4

反过来,能否用导数的符号来判定函数的单调性呢?

下面我们利用拉格朗日中值定理来进行讨论.

设函数 $y = f(x)$ 在 $[a, b]$ 上连续，在 $(a, b)$ 内可导，在 $[a, b]$ 上任取两点 $x_1, x_2 (x_1 < x_2)$，应用拉格朗日中值定理，得到

$$
f (x _ {2}) - f (x _ {1}) = f ^ {\prime} (\xi) (x _ {2} - x _ {1}) \quad (x _ {1} <   \xi <   x _ {2}).
$$

由于在上式中， $x_{2} - x_{1} > 0$ ，因此，如果在 $(a,b)$ 内导数 $f^{\prime}(x)$ 保持正号，即 $f^{\prime}(x) > 0$ 那么也有 $f^{\prime}(\xi) > 0.$ 于是

$$
f (x _ {2}) - f (x _ {1}) = f ^ {\prime} (\xi) (x _ {2} - x _ {1}) > 0,
$$

即

$$
f (x _ {1}) <   f (x _ {2}),
$$

表明函数 $y = f(x)$ 在 $[a, b]$ 上单调增加. 同理, 如果在 $(a, b)$ 内导数 $f'(x)$ 保持负号, 即 $f'(x) < 0$, 那么 $f'(\xi) < 0$, 于是 $f(x_2) - f(x_1) < 0$, 即 $f(x_1) > f(x_2)$, 表明函数 $y = f(x)$ 在 $[a, b]$ 上单调减少.

此外,如果 $f'(x)$ 在 $(a,b)$ 内的某点x=c处等于零,而在其余各点处均为正(负),那么 $f(x)$ 在区间 $[a,c]$ 和区间 $[c,b]$ 上都是单调增加(减少)的,因此在区间 $[a,b]$ 上仍是单调增加(减少)的.显然,如果 $f'(x)$ 在 $(a,b)$ 内等于零的点为有限多个,只要它在其余各点处保持定号,那么 $f(x)$ 在 $[a,b]$ 上仍是单调的.

归纳以上讨论,即得

定理1 设函数 $y = f(x)$ 在 $[a, b]$ 上连续，在 $(a, b)$ 内可导.

（1）如果在 $(a,b)$ 内 $f^{\prime}(x)\geqslant 0$ ，且等号仅在有限多个点处成立，那么函数 $y = f(x)$ 在 $[a,b]$ 上单调增加；

141

---

第三章 微分中值定理与导数的应用

（2）如果在 $(a,b)$ 内 $f^{\prime}(x)\leqslant 0$ ，且等号仅在有限多个点处成立，那么函数 $y = f(x)$ 在 $[a,b]$ 上单调减少.

如果把这个判定法中的闭区间换成其他各种区间(对于无穷区间,要求在其任一有限的子区间上满足定理的条件),那么结论也成立,参阅本节习题8.

例1 判定函数 $y = x - \sin x$ 在 $[- \pi, \pi]$ 上的单调性.

解 因为所给函数在 $[- \pi, \pi]$ 上连续，在 $(- \pi, \pi)$ 内

$$
y ^ {\prime} = 1 - \cos x \geqslant 0,
$$

且等号仅在 $x = 0$ 处成立，所以由定理1可知，函数 $y = x - \sin x$ 在 $[- \pi, \pi]$ 上单调增加.

例 2 讨论函数  $y=e^{x}-x-1$  的单调性.

解  $y' = e^{x} - 1.$

函数 $y = \mathrm{e}^{x} - x - 1$ 的定义域为 $(- \infty, +\infty)$. 因为在 $(- \infty, 0)$ 内 $y' < 0$, 所以函数 $y = \mathrm{e}^{x} - x - 1$ 在 $(- \infty, 0]$ 上单调减少; 因为在 $(0, +\infty)$ 内 $y' > 0$, 所以函数 $y = \mathrm{e}^{x} - x - 1$ 在 $[0, +\infty)$ 上单调增加.

例3 讨论函数 $y = \sqrt[3]{x^2}$ 的单调性.

解 这函数的定义域为 $(-∞,+∞)$ .

当 $x \neq 0$ 时, 这函数的导数为

$$
y ^ {\prime} = \frac {2}{3 \sqrt [ 3 ]{x}},
$$

当 $x = 0$ 时，函数的导数不存在.在 $(-\infty ,0)$ 内， $y^{\prime} <   0$ ，因此函数 $y = \sqrt[3]{x^2}$ 在 $(-\infty ,0]$ 上单

调减少；在 $(0, +\infty)$ 内，$y' > 0$，因此函数 $y = \sqrt[3]{x^2}$ 在 $[0, +\infty)$ 上单调增加。函数的图形如图3-5所示。

我们注意到,在例2中,x=0是函数 $y=e^{x}-x-1$ 的单调减少区间 $(-∞,0]$ 与单调增加区间 $[0,+∞)$ 的分界点,而在该点处 $y'=0$.在例3中,x=0是函数 $y=\sqrt[3]{x^{2}}$ 的单调减少区间 $(-∞,0]$ 与单调增加区间 $[0,+∞)$ 的分界点,而在该点处导数不存在.

![](../../raw/pages_0129-0160/images/page_158_chart_17.jpg)

<details>
<summary>contour</summary>

| X | Y |
| --- | --- |
| -1 | ~0.67 |
| 0 | 0 |
| 1 | ~0.67 |
</details>

图3-5

从例 2 中看出,有些函数在它的定义区间上不是单调的,但是当我们用函数的驻点来划分函数的定义区间以后,就可以使函数在各个部分区间上单调.从例 3 中可看出,如果函数在某些点处不可导,则划分函数的定义区间的分点,还应包括这些导数不存在的点.一般地,我们有如下结论:

如果函数 $y = f(x)$ 在定义区间上连续，除去有限个导数不存在的点外导数存在且在区间内只有有限个驻点，那么只要用函数的驻点及导数不存在的点来划分函数 $y = f(x)$ 的定义区间，就能保证 $f'(x)$ 在各个部分区间内保持固定符号，因而函数 $y = f(x)$

142

---

第四节 函数的单调性与曲线的凹凸性

在每个部分区间上单调.

例 4 确定函数  $f(x)=2x^{3}-9x^{2}+12x-3$  的单调区间.

解 这函数的定义域为 $(-\infty, +\infty)$. 求这函数的导数

$$
f ^ {\prime} (x) = 6 x ^ {2} - 1 8 x + 1 2 = 6 (x - 1) (x - 2).
$$

解方程 $f'(x)=0$ , 即解

$$
6 (x - 1) (x - 2) = 0,
$$

得出它在函数定义域 $(- \infty, +\infty)$ 内的两个根 $x_{1} = 1, x_{2} = 2$. 这两个根把 $(- \infty, +\infty)$ 分成三个部分区间 $(- \infty, 1], [1, 2]$ 及 $[2, +\infty)$.

在区间 $(-∞,1)$ 内,x-1<0且x-2<0,所以 $f'(x)>0$ .因此,函数 $f(x)$ 在 $(-∞,1]$ 上单调增加.在区间(1,2)内,x-1>0但x-2<0,所以 $f'(x)<0$ .因此,函数 $f(x)$ 在[1,2]上单调减少.在区间 $(2,+∞)$ 内,x-1>0且x-2>0,所以 $f'(x)>0$ .因此,函数 $f(x)$ 在 $[2,+∞)$ 上单调增加.

函数  $y=f(x)$  的图形如图 3-6 所示.

下面我们举一个利用函数的单调性证明不等式的例子.

![](../../raw/pages_0129-0160/images/page_159_chart_11.jpg)

<details>
<summary>line</summary>

| X | Y |
| --- | --- |
| 1 | 2 |
| 2 | 1 |
</details>

图3-6

例 5 证明: 当 x > 1 时,  $2\sqrt{x} > 3 - \frac{1}{x}$ .

证 令 $f(x) = 2\sqrt{x} - \left(3 - \frac{1}{x}\right)$, 则

$$
f ^ {\prime} (x) = \frac {1}{\sqrt {x}} - \frac {1}{x ^ {2}} = \frac {1}{x ^ {2}} (x \sqrt {x} - 1).
$$

$f(x)$ 在 $[1, +\infty)$ 上连续，在 $(1, +\infty)$ 内 $f'(x) > 0$ ，因此在 $[1, +\infty)$ 上 $f(x)$ 单调增加，从而当 $x > 1$ 时，$f(x) > f(1)$.

由于 $f(1) = 0$ ，故 $f(x) > f(1) = 0$ ，即

$$
2 \sqrt {x} - \left(3 - \frac {1}{x}\right) > 0,
$$

亦即

$$
2 \sqrt {x} > 3 - \frac {1}{x} (x > 1).
$$

## 二、曲线的凹凸性与拐点

在第一目中,我们研究了函数单调性的判定法.函数的单调性反映在图形上,就是曲线的上升或下降.但是,曲线在上升或下降的过程中,还有一个弯曲方向的问题.例如,图3-7中有两条曲线弧,虽然它们都是上升的,但图形却有显著的不同, $\widehat{ACB}$ 是向上

![](../../raw/pages_0129-0160/images/page_159_image_23.jpg)

例题精讲

3-4

![](../../raw/pages_0129-0160/images/page_159_image_26.jpg)

释疑解难

3-3

143

---

第三章 微分中值定理与导数的应用

凸的曲线弧,而 $\widehat{ADB}$ 是向上凹的曲线弧,它们的凹凸性不同,下面我们就来研究曲线的凹凸性及其判定法.

我们从几何上看到,在有的曲线弧上,如果任取两点,则连接这两点间的弦总位于这两点间的弧段的上方(图3-8(a)),而有的曲线弧,则正好相反(图3-8(b)).曲线的这种性质就是曲线的凹凸性.因此曲线的凹凸性可以用连接曲线弧上任意两点的弦的中点与曲线弧上相应点(即具有相同横坐标的点)的位置关系来描述,下面给出曲线凹凸性的定义.

![](../../raw/pages_0161-0192/images/page_160_image_3.jpg)

<details>
<summary>text_image</summary>

y
C
B
A
D
O
x
</details>

图3-7

![](../../raw/pages_0161-0192/images/page_160_chart_5.jpg)

<details>
<summary>contour</summary>

| Point | X-coordinate | Y-coordinate |
| --- | --- | --- |
| f(x1) | x1 | 2 |
| f(x2) | x2 | 2 |
| Intersection (f(x1)+f(x2)) | x1 | 2 |
| Intersection (f(x1)+f(x2)) | x1+x2/2 | f(2/x1+x2)/2 |
</details>

(a)

![](../../raw/pages_0161-0192/images/page_160_chart_7.jpg)

<details>
<summary>area</summary>

| Point | X-coordinate | Y-coordinate |
| --- | --- | --- |
| Point 1 | x1 | (x1+x2)/2 |
| Point 2 | x2 | f(x2) |
</details>

(b)

图3-8

定义 设 $f(x)$ 在区间 $I$ 上连续, 如果对 $I$ 上任意两点 $x_{1}, x_{2}$ 恒有

$$
f \left(\frac {x _ {1} + x _ {2}}{2}\right) <   \frac {f (x _ {1}) + f (x _ {2})}{2},
$$

那么称 $f(x)$ 在 I 上的图形是(向上)凹的(或凹弧); 如果恒有

$$
f \left(\frac {x _ {1} + x _ {2}}{2}\right) > \frac {f (x _ {1}) + f (x _ {2})}{2},
$$

那么称 $f(x)$ 在 $I$ 上的图形是(向上)凸的(或凸弧).

如果函数 $f(x)$ 在I内具有二阶导数,那么可以利用二阶导数的符号来判定曲线的凹凸性,这就是下面的曲线凹凸性的判定定理.

定理2 设 $f(x)$ 在 $[a, b]$ 上连续，在 $(a, b)$ 内具有一阶和二阶导数，那么

(1) 若在 $(a,b)$ 内 $f''(x)>0$ ，则 $f(x)$ 在 $[a,b]$ 上的图形是凹的:
(2) 若在 $(a,b)$ 内 $f''(x)<0$ , 则 $f(x)$ 在 $[a,b]$ 上的图形是凸的.

证 在情形(1)，设 $x_{1}$ 和 $x_{2}$ 为 $[a,b]$ 内任意两点，且 $x_{1} < x_{2}$，记 $\frac{x_1 + x_2}{2} = x_0$，并记 $x_{2} - x_{0} = x_{0} - x_{1} = h$，则 $x_{1} = x_{0} - h, x_{2} = x_{0} + h$，由拉格朗日中值公式，得

144

---

第四节 函数的单调性与曲线的凹凸性

$$
\begin{array}{l} f (x _ {0} + h) - f (x _ {0}) = f ^ {\prime} (x _ {0} + \theta_ {1} h) h, \\ f (x _ {0}) - f (x _ {0} - h) = f ^ {\prime} (x _ {0} - \theta_ {2} h) h, \\ \end{array}
$$

其中 $0 < \theta_{1} < 1, 0 < \theta_{2} < 1$. 两式相减，即得

$$
f (x _ {0} + h) + f (x _ {0} - h) - 2 f (x _ {0}) = \left[ f ^ {\prime} (x _ {0} + \theta_ {1} h) - f ^ {\prime} (x _ {0} - \theta_ {2} h) \right] h.
$$

对 $f^{\prime}(x)$ 在区间 $[x_0 - \theta_2h, x_0 + \theta_1h]$ 上再利用拉格朗日中值公式，得

$$
\left[ f ^ {\prime} (x _ {0} + \theta_ {1} h) - f ^ {\prime} (x _ {0} - \theta_ {2} h) \right] h = f ^ {\prime \prime} (\xi) (\theta_ {1} + \theta_ {2}) h ^ {2},
$$

其中 $x_0 - \theta_2h < \xi < x_0 + \theta_1h.$ 按情形(1)的假设，$f''(\xi) > 0$，故有

$$
f (x _ {0} + h) + f (x _ {0} - h) - 2 f (x _ {0}) > 0,
$$

即

$$
\frac {f (x _ {0} + h) + f (x _ {0} - h)}{2} > f (x _ {0}),
$$

亦即

$$
\frac {f (x _ {1}) + f (x _ {2})}{2} > f \left(\frac {x _ {1} + x _ {2}}{2}\right),
$$

所以 $f(x)$ 在 $[a, b]$ 上的图形是凹的.

类似地可证明情形(2).

如果把这个判定法中的闭区间换成其他各种区间(包括无穷区间),那么结论也成立.

例 6 判定曲线  $y=\ln x$  的凹凸性.

解 因为 $y' = \frac{1}{x}, y'' = -\frac{1}{x^2}$，所以在函数 $y = \ln x$ 的定义域 $(0, +\infty)$ 内，$y'' < 0$，由定理2可知，曲线 $y = \ln x$ 是凸的.

例 7 判定曲线  $y=x^{3}$  的凹凸性.

解 因为 $y' = 3x^2, y'' = 6x$. 当 $x < 0$ 时, $y'' < 0$, 所以曲线在 $(-\infty, 0]$ 内为凸弧; 当 $x > 0$ 时, $y'' > 0$, 所以曲线在 $[0, +\infty)$ 内为凹弧.

一般地, 设  $y=f(x)$  在区间 I 上连续,  $x_{0}$  是 I 内的点. 如果曲线  $y=f(x)$  在经过点  $(x_{0}, f(x_{0}))$  时, 曲线的凹凸性改变了, 那么就称点  $(x_{0}, f(x_{0}))$  为这曲线的拐点.

如何来寻找曲线  $y=f(x)$  的拐点呢？

从上面的定理知道,由 $f''(x)$ 的符号可以判定曲线的凹凸性,因此,如果 $f''(x)$ 在 $x_0$ 的左、右两侧邻近异号,那么点 $(x_0, f(x_0))$ 就是曲线的一个拐点,所以,要寻找拐点,只要找出 $f''(x)$ 符号发生变化的分界点即可,也就是找出 $f'(x)$ 单调增减区间发生变化的分界点即可.因此,如果 $f(x)$ 在区间 $(a, b)$ 内具有二阶导数,那么在这样的分界点处必然有 $f''(x) = 0$;除此以外,$f(x)$ 的二阶导数不存在的点,也有可能是 $f''(x)$ 的符号发生变化的分界点.综合以上分析,我们可以按下列步骤来判定区间I上的连

145

---

第三章 微分中值定理与导数的应用

续曲线  $y=f(x)$  的拐点:

(1) 求  $f''(x)$ ;
（2）令 $f''(x)=0$ ，解出这方程在区间I内的实根，并求出在区间I内 $f''(x)$ 不存在的点①；
（3）对于(2)中求出的每一个实根或二阶导数不存在的点 $x_0$ ，检查 $f''(x)$ 在 $x_0$ 左、右两侧邻近的符号，那么当两侧的符号相反时，点 $(x_0, f(x_0))$ 是拐点，当两侧的符号相同时，点 $(x_0, f(x_0))$ 不是拐点.

例 8 求曲线  $y=2x^{3}+3x^{2}-12x+14$  的拐点.

解 $y' = 6x^2 + 6x - 12$，$y'' = 12x + 6 = 12\left(x + \frac{1}{2}\right)$.

解方程 $y'' = 0$，得 $x = -\frac{1}{2}$。当 $x < -\frac{1}{2}$ 时，$y'' < 0$；当 $x > -\frac{1}{2}$ 时，$y'' > 0$。因此，点 $\left(-\frac{1}{2}, 20\frac{1}{2}\right)$ 是这曲线的拐点。

例 9 求曲线  $y=3x^{4}-4x^{3}+1$  的拐点及凹、凸的区间.

解 函数 $y = 3x^4 - 4x^3 + 1$ 的定义域为 $(- \infty, +\infty)$.

$$
y ^ {\prime} = 1 2 x ^ {3} - 1 2 x ^ {2}, \quad y ^ {\prime \prime} = 3 6 x ^ {2} - 2 4 x = 3 6 x \left(x - \frac {2}{3}\right).
$$

解方程  $y''=0$ , 得  $x_{1}=0, x_{2}=\frac{2}{3}$ .

$x_{1} = 0$ 及 $x_{2} = \frac{2}{3}$ 把函数的定义域 $(-\infty, +\infty)$ 分成三个部分区间: $(- \infty, 0]$，$\left[0, \frac{2}{3}\right], \left[\frac{2}{3}, +\infty\right)$.

在 $(-∞,0)$ 内, $y''>0$ ,因此在区间 $(-∞,0]$ 上这曲线是凹的.在 $\left(0,\frac{2}{3}\right)$ 内, $y''<0$ ,因此在区间 $\left[0,\frac{2}{3}\right]$ 上这曲线是凸的.在 $\left(\frac{2}{3},+\infty\right)$ 内, $y''>0$ ,因此在区间 $\left[\frac{2}{3},+\infty\right)$ 上这曲线是凹的.

当 $x = 0$ 时，$y = 1$，点 $(0,1)$ 是这曲线的一个拐点。当 $x = \frac{2}{3}$ 时 $y = \frac{11}{27}$，点 $\left(\frac{2}{3}, \frac{11}{27}\right)$ 也是这曲线的拐点。

例 10 问曲线  $y=x^{4}$  是否有拐点？

解 $y' = 4x^3, y'' = 12x^2.$

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 这里假设这两种点在区间 I 内的个数均为有限个.</span></small>

146

---

第四节 函数的单调性与曲线的凹凸性

显然, 只有 $x = 0$ 是方程 $y'' = 0$ 的根. 但当 $x \neq 0$ 时, 无论 $x < 0$ 或 $x > 0$ 都有 $y'' > 0$, 因此点 $(0,0)$ 不是这曲线的拐点. 曲线 $y = x^4$ 没有拐点, 它在 $(- \infty, +\infty)$ 内是凹的.

例11 求曲线 $y = \sqrt[3]{x}$ 的拐点.

解 这函数在 $(-\infty, +\infty)$ 内连续，当 $x \neq 0$ 时，

$$
y ^ {\prime} = \frac {1}{3 \sqrt [ 3 ]{x ^ {2}}}, \quad y ^ {\prime \prime} = - \frac {2}{9 x \sqrt [ 3 ]{x ^ {2}}},
$$

当 $x = 0$ 时，$y', y''$ 都不存在。故二阶导数在 $(- \infty, +\infty)$ 内不连续且不具有零点。但 $x = 0$ 是 $y''$ 不存在的点，它把 $(- \infty, +\infty)$ 分成两个部分区间:$(- \infty, 0], [0, +\infty)$。

在 $(-∞,0)$ 内， $y''>0$ ，这曲线在 $(-∞,0]$ 上是凹的。在 $(0,+∞)$ 内， $y"<0$ ，这曲线在 $[0,+∞)$ 上是凸的。

当 $x = 0$ 时，$y = 0$，点 $(0,0)$ 是这曲线的一个拐点.

## 习题3-4

1. 判定函数 $f(x) = \arctan x - x$ 的单调性.
2. 判定函数 $f(x) = x + \cos x$ 的单调性.
3. 确定下列函数的单调区间:

(1) $y = 2x^{3} - 6x^{2} - 18x - 7$;
(2) $y = 2x + \frac{8}{x}$ ($x > 0$);
(3)  $y=\frac{10}{4x^{3}-9x^{2}+6x}$ ;
(4) $y = \ln (x + \sqrt{1 + x^2})$;
(5)  $y=(x-1)(x+1)^{3}$ ;
(6)  $y = \sqrt[3]{(2x - a)(a - x)^{2}} \quad (a > 0)$ ;
(7) $y = x^n \mathrm{e}^{-x} (n > 0, x \geqslant 0)$; (8) $y = x + |\sin 2x|$.

4. 设函数 $y = f(x)$ 在定义域内可导, $y = f(x)$ 的图形如图3-9所示, 则导函数 $f'(x)$ 的图形为图3-10中所示的四个图形中的哪一个?

![](../../raw/pages_0161-0192/images/page_163_image_22.jpg)

<details>
<summary>text_image</summary>

y
O
x
</details>

图3-9

![](../../raw/pages_0161-0192/images/page_163_image_24.jpg)

<details>
<summary>text_image</summary>

y
O
x
</details>

(A)

![](../../raw/pages_0161-0192/images/page_163_image_26.jpg)

<details>
<summary>text_image</summary>

y
O
x
</details>

(B)

![](../../raw/pages_0161-0192/images/page_163_chart_28.jpg)

<details>
<summary>contour</summary>

| X | Y |
| --- | --- |
| 0 | ~0.2 |
| ~0.15 | ~0.8 |
| ~0.3 | ~0.4 |
| ~0.5 | ~0.1 |
| ~0.7 | ~0.3 |
</details>

(C)

![](../../raw/pages_0161-0192/images/page_163_image_30.jpg)

<details>
<summary>text_image</summary>

y
O
x
</details>

(D)

图3-10

147

---

第三章 微分中值定理与导数的应用

5. 证明下列不等式:

(1) 当 x > 0 时,  $1 + \frac{1}{2}x > \sqrt{1 + x}$ ;

(2) 当 x>0 时,  $1+x\ln(x+\sqrt{1+x^{2}})>\sqrt{1+x^{2}}$ ;

(3) 当  $0 < x < \frac{\pi}{2}$  时,  $\sin x + \tan x > 2x$ ;

(4) 当  $0 < x < \frac{\pi}{2}$  时， $\tan x > x + \frac{1}{3}x^{3}$ ;

(5) 当 x>4 时,  $2^{x}>x^{2}$ .

6. 讨论方程  $\ln x = ax$  （其中 a > 0）有几个实根.

7. 单调函数的导函数是否必为单调函数？研究下面的例子:

$$
f (x) = x + \sin x.
$$

8. 设 $I$ 为任一无穷区间, 函数 $f(x)$ 在区间 $I$ 上连续, $I$ 内可导. 试证明: 如果 $f(x)$ 在 $I$ 的任一有限的子区间上 $f'(x) \geqslant 0$ (或 $f'(x) \leqslant 0$), 且等号仅在有限多个点处成立, 那么 $f(x)$ 在区间 $I$ 上单调增加 (或单调减少).

9. 判定下列曲线的凹凸性:

(1)  $y=4x-x^{2}$ ;

(2) y = sh x;

(3)  $y = x + \frac{1}{x} \quad (x > 0)$ ;

(4) $y = x \arctan x.$

10. 求下列函数图形的拐点及凹或凸的区间:

(1)  $y=x^{3}-5x^{2}+3x+5;$

(2) $y = x\mathrm{e}^{-x}$;

(3)  $y=(x+1)^{4}+e^{x}$ ;

(4) $y = \ln (x^2 + 1)$;

(5)  $y=e^{\arctan x}$ ;

(6) $y = x^4 (12\ln x - 7)$.

11. 利用函数图形的凹凸性, 证明下列不等式:

(1) $\frac{1}{2} (x^n + y^n) > \left(\frac{x + y}{2}\right)^n (x > 0, y > 0, x \neq y, n > 1)$;

(2) $\frac{\mathrm{e}^x + \mathrm{e}^y}{2} >\mathrm{e}^{\frac{x + y}{2}} (x\neq y);$

(3)  $x \ln x + y \ln y > (x + y) \ln \frac{x + y}{2} \quad (x > 0, y > 0, x \neq y)$ ;

(4) $\sin x > \frac{2x}{\pi}\left(0 < x < \frac{\pi}{2}\right)$.

\* 12. 试证明曲线 $y = \frac{x - 1}{x^2 + 1}$ 有三个拐点位于同一直线上.

13. 问 a, b 为何值时, 点  $(1,3)$  为曲线  $y=ax^{3}+bx^{2}$  的拐点?

14. 试决定曲线 $y = ax^3 + bx^2 + cx + d$ 中的 $a, b, c, d$，使得 $x = -2$ 处曲线有水平切线，(1, -10)为拐点，且点(-2,44)在曲线上.

15. 试决定 $y = k(x^{2} - 3)^{2}$ 中 $k$ 的值，使曲线的拐点处的法线通过原点

\* 16. 设 $y = f(x)$ 在 $x = x_0$ 的某邻域内具有三阶连续导数, 如果 $f''(x_0) = 0$, 而 $f'''(x_0) \neq 0$, 试问 $(x_0, f(x_0))$ 是不是拐点? 为什么?

148

---

第五节 函数的极值与最大值最小值

# 第五节 函数的极值与最大值最小值

## 一、函数的极值及其求法

在上节例4中我们看到,点x=1及x=2是函数

$$
f (x) = 2 x ^ {3} - 9 x ^ {2} + 1 2 x - 3
$$

的单调区间的分界点.例如,在点x=1的左侧邻近,函数 $f(x)$ 是单调增加的,在点x=1的右侧邻近,函数 $f(x)$ 是单调减少的.因此,存在点x=1的一个去心邻域,对于这去心邻域内的任何点x,f(x)&lt;f(1)均成立.类似地,关于点x=2,也存在着一个去心邻域,对于这去心邻域内的任何点x,f(x)&gt;f(2)均成立(参看图3-6).具有这种性质的点如x=1及x=2,在应用上有着重要的意义,值得我们对此作一般性的讨论.

定义 设函数 $f(x)$ 在点 $x_0$ 的某邻域 $U(x_0)$ 内有定义, 如果对于去心邻域 $\dot{U}(x_0)$ 内的任一 $x$, 有

$$
f (x) <   f (x _ {0}) \quad (\text {或} f (x) > f (x _ {0})) ,
$$

那么就称 $f(x_{0})$ 是函数 $f(x)$ 的一个极大值(或极小值).

函数的极大值与极小值统称为函数的极值,使函数取得极值的点称为极值点.例如,上节例4中的函数

$$
f (x) = 2 x ^ {3} - 9 x ^ {2} + 1 2 x - 3
$$

有极大值 $f(1)=2$ 和极小值 $f(2)=1$，点 x=1 和 x=2 是函数 $f(x)$ 的极值点.

函数的极大值和极小值概念是局部性的. 如果 $f(x_0)$ 是函数 $f(x)$ 的一个极大值, 那只是就 $x_0$ 附近的一个局部范围来说, $f(x_0)$ 是 $f(x)$ 的一个最大值; 如果就 $f(x)$ 的整个定义域来说, $f(x_0)$ 不见得是最大值. 关于极小值也类似.

在图3-11中，函数 $y = f(x)$ 有两个极大值:$f(x_{2}), f(x_{5})$，三个极小值:$f(x_{1})$

$f(x_{4}), f(x_{6})$，其中极大值 $f(x_{2})$ 比极小值 $f(x_{6})$ 还小。就整个区间 $[a, b]$ 来说，只有一个极小值 $f(x_{1})$ 同时也是最小值，而没有一个极大值是最大值。

从图中还可看到,在函数取得极值处,曲线的切线是水平的.但曲线上有水平切线的地方,函数不一定取得极值.例如图中 $x=x_{3}$ 处,曲线上有水平切线,但

![](../../raw/pages_0161-0192/images/page_165_chart_16.jpg)

<details>
<summary>line</summary>

| Point | Value |
| --- | --- |
| a | ~0.2 |
| x1 | ~0.1 |
| x2 | ~0.7 |
| x3 | ~0.4 |
| x4 | ~0.2 |
| x5 | ~0.8 |
| x6 | ~0.6 |
| b | ~1.0 |
</details>

图3-11

149

---

第三章 微分中值定理与导数的应用

$f(x_{3})$ 不是极值.

由本章第一节费马引理可知,如果函数  $f(x)$  在  $x_{0}$  处可导,且  $f(x)$  在  $x_{0}$  处取得极值,那么  $f'(x_{0})=0$ . 这就是可导函数取得极值的必要条件. 现将此结论叙述成如下定理:

定理1（必要条件）设函数 $f(x)$ 在 $x_0$ 处可导，且在 $x_0$ 处取得极值，则 $f'(x_0) = 0$.

定理1就是说:可导函数 $f(x)$ 的极值点必定是它的驻点.但反过来，函数的驻点却不一定是极值点.例如， $f(x) = x^3$ 的导数 $f'(x) = 3x^{2}, f'(0) = 0$ ，因此 $x = 0$ 是这可导函数的驻点，但 $x = 0$ 却不是这函数的极值点.所以，函数的驻点只是可能的极值点.此外，函数在它的导数不存在的点处也可能取得极值.例如，函数 $f(x) = |x|$ 在点 $x = 0$ 处不可导，但函数在该点取得极小值

怎样判定函数在驻点或不可导的点处究竟是否取得极值？如果是的话，究竟取得极大值还是极小值？下面给出两个判定极值的充分条件:

定理2（第一充分条件）设函数 $f(x)$ 在 $x_0$ 处连续，且在 $x_0$ 的某去心邻域 $\dot{U}(x_0, \delta)$ 内可导.

（1）若 $x \in (x_0 - \delta, x_0)$ 时，$f'(x) > 0$，而 $x \in (x_0, x_0 + \delta)$ 时，$f'(x) < 0$，则 $f(x)$ 在 $x_0$ 处取得极大值；
(2) 若  $x \in (x_{0}-\delta, x_{0})$  时， $f'(x) < 0$ ，而  $x \in (x_{0}, x_{0}+\delta)$  时， $f'(x) > 0$ ，则  $f(x)$  在  $x_{0}$  处取得极小值；
(3) 若 $x \in \mathring{U}(x_0, \delta)$ 时, $f'(x)$ 的符号保持不变, 则 $f(x)$ 在 $x_0$ 处没有极值.

证 事实上, 就情形 (1) 来说, 根据函数单调性的判定法, 函数 $f(x)$ 在 $(x_0 - \delta, x_0)$ 内单调增加, 而在 $(x_0, x_0 + \delta)$ 内单调减少, 又由于函数 $f(x)$ 在 $x_0$ 处是连续的, 故当 $x \in \mathring{U}(x_0, \delta)$ 时, 总有 $f(x) < f(x_0)$. 所以, $f(x_0)$ 是 $f(x)$ 的一个极大值 (图 3-12 (a)).

类似地可论证情形(2)(图3-12(b))及情形(3)(图3-12(c)、(d)).

定理2也可简单地这样说:当 $x$ 在 $x_0$ 的邻近渐增地经过 $x_0$ 时，如果 $f'(x)$ 的符号由正变负，那么 $f(x)$ 在 $x_0$ 处取得极大值；如果 $f'(x)$ 的符号由负变正，那么 $f(x)$ 在 $x_0$ 处取得极小值；如果 $f'(x)$ 的符号并不改变，那么 $f(x)$ 在 $x_0$ 处没有极值.

根据上面的两个定理,如果函数 $f(x)$ 在所讨论的区间内连续,除个别点外处处可导,那么就可以按下列步骤来求 $f(x)$ 在该区间内的极值点和相应的极值:

(1) 求出导数 $f'(x)$;
(2) 求出  $f(x)$  的全部驻点与不可导点；
（3）考察 $f'(x)$ 的符号在每个驻点或不可导点的左、右邻近的情形，以确定该点是否为极值点；如果是极值点，进一步确定是极大值点还是极小值点；

150

---

第五节 函数的极值与最大值最小值

![](../../raw/pages_0161-0192/images/page_167_chart_1.jpg)

<details>
<summary>contour</summary>

| Point | x-coordinate | y-coordinate |
| --- | --- | --- |
| f'(x)>0 | \(x_{0}\) | ~Intersection of curves |
| f'(x)<0 | \(x_{0}\) | ~Intersection of curves |
</details>

(a)

![](../../raw/pages_0161-0192/images/page_167_chart_3.jpg)

<details>
<summary>contour</summary>

| Point | x-coordinate | y-coordinate |
| --- | --- | --- |
| f'(x)<0 | \(x_{0}\) | ~Intersection of curves |
| f'(x)>0 | \(x_{0}\) | ~Intersection of curves |
</details>

(b)

![](../../raw/pages_0161-0192/images/page_167_chart_5.jpg)

<details>
<summary>contour</summary>

| Point | Description |
| --- | --- |
| Intersection (x0, y) | f'(x) > 0 |
| Horizontal Line | y = f(x) |
</details>

(c)

![](../../raw/pages_0161-0192/images/page_167_chart_7.jpg)

<details>
<summary>contour</summary>

| Point | Description |
| --- | --- |
| Intersection (x0, y) | f'(x)<0 |
| Horizontal Line | y=f(x) = f'(x)<0 |
</details>

(d)

图3-12

(4) 求出各极值点的函数值, 就得函数  $f(x)$  的全部极值.

例1 求函数 $f(x) = (x - 4)\sqrt[3]{(x + 1)^2}$ 的极值.

解 （1） $f(x)$  在  $(-∞,+∞)$  内连续，除 x=-1 外处处可导，且

$$
f ^ {\prime} (x) = \frac {5 (x - 1)}{3 \sqrt [ 3 ]{x + 1}};
$$

(2) 令  $f'(x)=0$  , 得驻点 x=1, x=-1 为  $f(x)$  的不可导点；
(3) 在 $(-∞,-1)$ 内, $f'(x)>0$; 在 $(-1,1)$ 内, $f'(x)<0$. 故不可导点 x=-1 是一个极大值点; 又在 $(1,+∞)$ 内, $f'(x)>0$, 故驻点 x=1 是一个极小值点;
(4) 极大值为  $f(-1)=0$ ，极小值为  $f(1)=-3\sqrt[3]{4}$ .

当函数 $f(x)$ 在驻点处的二阶导数存在且不为零时,也可以利用下述定理来判定 $f(x)$ 在驻点处取得极大值还是极小值.

定理3（第二充分条件）设函数 $f(x)$ 在 $x_0$ 处具有二阶导数且 $f'(x_0) = 0, f''(x_0) \neq 0$，则

(1) 当  $f''(x_{0})<0$  时, 函数  $f(x)$  在  $x_{0}$  处取得极大值;
(2) 当  $f''(x_{0}) > 0$  时, 函数  $f(x)$  在  $x_{0}$  处取得极小值.

证 在情形(1)，由于 $f''(x_{0})<0$ ，按二阶导数的定义有

$$
f ^ {\prime \prime} (x _ {0}) = \lim _ {x \to x _ {0}} \frac {f ^ {\prime} (x) - f ^ {\prime} (x _ {0})}{x - x _ {0}} <   0.
$$

根据函数极限的局部保号性, 当 x 在  $x_{0}$  的足够小的去心邻域内时,

151

---

第三章 微分中值定理与导数的应用

$$
\frac {f ^ {\prime} (x) - f ^ {\prime} (x _ {0})}{x - x _ {0}} <   0.
$$

但 $f'(x_{0})=0$ ,所以上式即

$$
\frac {f ^ {\prime} (x)}{x - x _ {0}} <   0.
$$

从而知道,对于这去心邻域内的 x 来说, $f'(x)$ 与 $x-x_{0}$ 符号相反.因此,当 $x-x_{0}<0$ 即 $x<x_{0}$ 时, $f'(x)>0$;当 $x-x_{0}>0$ 即 $x>x_{0}$ 时, $f'(x)<0$.于是根据定理2 知道, $f(x)$ 在点 $x_{0}$ 处取得极大值.

类似地可以证明情形(2).

定理3表明,如果函数 $f(x)$ 在驻点 $x_{0}$ 处的二阶导数 $f''(x_{0})\neq0$ ,那么该驻点 $x_{0}$ 一定是极值点,并且可以按二阶导数 $f''(x_{0})$ 的符号来判定 $f(x_{0})$ 是极大值还是极小值.但如果 $f''(x_{0})=0$ ,那么定理3就不能应用.事实上,当 $f'(x_{0})=0,f''(x_{0})=0$ 时, $f(x)$ 在 $x_{0}$ 处可能有极大值,也可能有极小值,也可能没有极值.例如, $f_{1}(x)=-x^{4},f_{2}(x)=x^{4},f_{3}(x)=x^{3}$ 这三个函数在x=0处就分别属于这三种情况.因此,如果函数在驻点处的二阶导数为零,那么可以用一阶导数在驻点左、右邻近的符号来判定;如果函数在驻点处有 $f''(x_{0})=\cdots=f^{(n-1)}(x_{0})=0,f^{(n)}(x_{0})\neq0$ ,那么也可利用具有佩亚诺余项的泰勒公式来讨论判定(参阅本节习题4).

例 2 求函数  $f(x)=(x^{2}-1)^{3}+1$  的极值.

解 $f^{\prime}(x) = 6x(x^{2} - 1)^{2}$

令 $f'(x)=0$ , 求得驻点  $x_{1}=-1, x_{2}=0, x_{3}=1$ .

$$
f ^ {\prime \prime} (x) = 6 (x ^ {2} - 1) (5 x ^ {2} - 1).
$$

因 $f''(0)=6>0$ ，故 $f(x)$ 在x=0处取得极小值，极小值为 $f(0)=0$ .

因 $f''(-1)=f''(1)=0$ ，故用定理3无法判别。考察一阶导数 $f'(x)$ 在驻点 $x_{1}=-1$ 及 $x_{3}=1$ 左、右邻近的符号:

当 $x$ 取-1左侧邻近的值时，$f'(x) < 0$；当 $x$ 取-1右侧邻近的值时，$f'(x) < 0$；因为 $f'(x)$ 的符号没有改变，所以 $f(x)$ 在 $x = -1$ 处没有极值。同理，$f(x)$ 在 $x = 1$ 处也没有极值（图3-13）。

![](../../raw/pages_0161-0192/images/page_168_chart_14.jpg)

<details>
<summary>contour</summary>

| X | Y |
| --- | --- |
| -1 | ~0.5 |
| 0 | 0 |
| 1 | ~0.5 |
</details>

图3-13

## 二、最大值最小值问题

在工农业生产、工程技术及科学实验中,常常会遇到这样一类问题:在一定条件下,怎样使“产品最多”“用料最省”“成本最低”“效率最高”等问题,这类问题在数学上有时可归结为求某一函数(通常称为目标函数)的最大值或最小值问题.

152

---

第五节 函数的极值与最大值最小值

假定函数 $f(x)$ 在闭区间 $[a,b]$ 上连续，在开区间 $(a,b)$ 内除有限个点外可导，且至多有有限个驻点。在上述条件下，我们来讨论 $f(x)$ 在 $[a,b]$ 上的最大值和最小值的求法。

首先,由闭区间上连续函数的性质可知, $f(x)$ 在 $[a,b]$ 上的最大值和最小值一定存在.

其次,如果最大值(或最小值) $f(x_{0})$ 在开区间 $(a,b)$ 内的点 $x_{0}$ 处取得,那么,按 $f(x)$ 在开区间内除有限个点外可导且至多有有限个驻点的假定,可知 $f(x_{0})$ 一定也是 $f(x)$ 的极大值(或极小值),从而 $x_{0}$ 一定是 $f(x)$ 的驻点或不可导点.又 $f(x)$ 的最大值和最小值也可能在区间的端点处取得.因此,可用如下方法求 $f(x)$ 在 $[a,b]$ 上的最大值和最小值.

(1) 求出  $f(x)$  在  $(a, b)$  内的驻点①及不可导点；

(2) 计算  $f(x)$  在上述驻点、不可导点处的函数值及  $f(a)$ ,  $f(b)$ ;

(3) 比较(2)中诸值的大小,其中最大的便是 $f(x)$ 在 $[a,b]$ 上的最大值,最小的便是 $f(x)$ 在 $[a,b]$ 上的最小值.

例 3 求函数  $f(x)=\left|x^{2}-3x+2\right|$  在  $[-3,4]$  上的最大值与最小值.

解 $f(x) = \begin{cases} x^2 - 3x + 2, & x \in [-3,1] \cup [2,4], \\ -x^2 + 3x - 2, & x \in (1,2). \end{cases}$

$$
f ^ {\prime} (x) = \left\{ \begin{array}{l l} 2 x - 3, & x \in (- 3, 1) \cup (2, 4), \\ - 2 x + 3, & x \in (1, 2). \end{array} \right.
$$

在 $(-3,4)$ 内， $f(x)$ 的驻点为 $x=\frac{3}{2}$ ; 不可导点为x=1,x=2.

由于 $f(-3) = 20, f(1) = 0, f\left(\frac{3}{2}\right) = \frac{1}{4}, f(2) = 0, f(4) = 6$，比较可得 $f(x)$ 在 $x = -3$ 处取得它在 $[-3, 4]$ 上的最大值20，在 $x = 1$ 和 $x = 2$ 处取得它在 $[-3, 4]$ 上的最小值0.

例 4 铁路线上 AB 段的距离为 100 km. 工厂 C 距 A 处为 20 km, AC 垂直于 AB

(图 3-14).为了运输需要,要在AB线上选定一点D向工厂修筑一条公路.已知铁路每千米货运的运费与公路上每千米货运的运费之比为3:5.为了使货物从供应站B运到工厂C的运费最省,问D点应选在何处?

解 设  $AD = x \, km$ ，则  $DB = (100 - x) \, \text{km}$ ，

![](../../raw/pages_0161-0192/images/page_169_image_15.jpg)

<details>
<summary>text_image</summary>

100 km
A
20 km
D
C
B
</details>

图3-14

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 当 $f(x)$ 在 $(a,b)$ 内没有驻点时,这个求驻点的步骤自动取消.</span></small>

153

---

第三章 微分中值定理与导数的应用

$$
C D = \sqrt {2 0 ^ {2} + x ^ {2}} = \sqrt {4 0 0 + x ^ {2}}.
$$

由于铁路上每千米货运的运费与公路上每千米货运的运费之比为 $3:5$ ，因此我们不妨设铁路上每千米的运费为 $3k$ ，公路上每千米的运费为 $5k$ （$k$ 为某个正数，因它与本题的解无关，所以不必定出).设从供应站 $B$ 到工厂 $C$ 需要的总运费为 $y$ ，则

$$
y = 5 k \cdot C D + 3 k \cdot D B,
$$

即

$$
y = 5 k \sqrt {4 0 0 + x ^ {2}} + 3 k (1 0 0 - x) \quad (0 \leqslant x \leqslant 1 0 0).
$$

现在,问题就归结为:x 在[0,100]内取何值时目标函数 y 的值最小.

先求 $y$ 对 $x$ 的导数

$$
y ^ {\prime} = k \left(\frac {5 x}{\sqrt {4 0 0 + x ^ {2}}} - 3\right).
$$

解方程  $y' = 0$ , 得  $x = 15 \, km$ .

由于 $y \mid_{x=0} = 400k, y \mid_{x=15} = 380k, y \bigg|_{x=100} = 500k \sqrt{1 + \frac{1}{5^2}}$，其中以 $y \bigg|_{x=15} = 380k$ 为最小，因此，当 $AD = x = 15 \mathrm{~km}$ 时，总运费为最省.

在求函数的最大值(或最小值)时,特别值得指出的是下述情形:f(x)在一个区间(有限或无限,开或闭)内可导且只有一个驻点 $x_{0}$ ,并且这个驻点 $x_{0}$ 是函数 $f(x)$ 的极值点,那么,当 $f(x_{0})$ 是极大值时, $f(x_{0})$ 就是 $f(x)$ 在该区间上的最大值(图3-15(a));当 $f(x_{0})$ 是极小值时, $f(x_{0})$ 就是 $f(x)$ 在该区间上的最小值(图3-15(b)).在应用问题中往往遇到这样的情形.

![](../../raw/pages_0161-0192/images/page_170_chart_12.jpg)

<details>
<summary>area</summary>

| Point | x-coordinate | y-coordinate |
| --- | --- | --- |
| f(x0) | x0 | ~f(x0) |
</details>

(a)

![](../../raw/pages_0161-0192/images/page_170_chart_14.jpg)

<details>
<summary>contour</summary>

| Point | x-coordinate | y-coordinate |
| --- | --- | --- |
| f(x0) | x0 | f(x0) |
</details>

(b)

图3-15

例 5 一束光线由空气中点 A 经过水面折射后到达水中点 B （图 3-16）. 已知光在空气中和水中传播的速度分别是  $v_{1}$  和  $v_{2}$ ，光线在介质中总是沿着耗时最少的路径传播. 试确定光线传播的路径.

解 设点 A 到水面的垂直距离为  $AO = h_{1}$ ，点 B 到水面的垂直距离为  $BQ = h_{2}$ ，x 轴沿水面过点 O 和 Q，OQ 的长度为 l.

154

---

第五节 函数的极值与最大值最小值

由于光线总是沿着耗时最少的路径传播,因此光线在同一均匀介质中必沿直线传播.设光线的传播路径与x轴的交点为P,OP=x,则光线从点A到点B的传播路径必为折线APB,其所需要的传播时间为

$$
T (x) = \frac {\sqrt {h _ {1} ^ {2} + x ^ {2}}}{v _ {1}} + \frac {\sqrt {h _ {2} ^ {2} + (l - x) ^ {2}}}{v _ {2}}, \quad x \in [ 0, l ].
$$

下面来确定 x 满足什么条件时,  $T(x)$  在  $[0, l]$  上取得最小值.

![](../../raw/pages_0161-0192/images/page_171_image_4.jpg)

<details>
<summary>text_image</summary>

A
h₁
O
P
θ₁
θ₂
Q
x
h₂
B
</details>

图3-16

由于

$$
\begin{array}{l} T ^ {\prime} (x) = \frac {1}{v _ {1}} \cdot \frac {x}{\sqrt {h _ {1} ^ {2} + x ^ {2}}} - \frac {1}{v _ {2}} \cdot \frac {l - x}{\sqrt {h _ {2} ^ {2} + (l - x) ^ {2}}}, \quad x \in [ 0, l ], \\ T ^ {\prime \prime} (x) = \frac {1}{v _ {1}} \cdot \frac {h _ {1} ^ {2}}{(h _ {1} ^ {2} + x ^ {2}) ^ {\frac {3}{2}}} + \frac {1}{v _ {2}} \cdot \frac {h _ {2} ^ {2}}{[ h _ {2} ^ {2} + (l - x) ^ {2} ] ^ {\frac {3}{2}}} > 0, \quad x \in [ 0, l ], \\ T ^ {\prime} (0) <   0, \quad T ^ {\prime} (l) > 0, \\ \end{array}
$$

又 $T'(x)$ 在 $[0, l]$ 上连续，故 $T'(x)$ 在 $(0, l)$ 内存在唯一零点 $x_0$，且 $x_0$ 是 $T(x)$ 在 $(0, l)$ 内的唯一极小值点，从而也是 $T(x)$ 在 $[0, l]$ 上的最小值点。

设 $x_0$ 满足 $T'(x) = 0$ ，即

$$
\frac {x _ {0}}{v _ {1} \sqrt {h _ {1} ^ {2} + x _ {0} ^ {2}}} = \frac {l - x _ {0}}{v _ {2} \sqrt {h _ {2} ^ {2} + (l - x _ {0}) ^ {2}}}.
$$

记

$$
\frac {x _ {0}}{\sqrt {h _ {1} ^ {2} + x _ {0} ^ {2}}} = \sin \theta_ {1}, \quad \frac {l - x _ {0}}{\sqrt {h _ {2} ^ {2} + (l - x _ {0}) ^ {2}}} = \sin \theta_ {2},
$$

就得到

$$
\frac {\sin \theta_ {1}}{v _ {1}} = \frac {\sin \theta_ {2}}{v _ {2}}.
$$

这就是说,当点 P 满足以上条件时,折线 APB 就是光线的传播路径.上式就是光学中著名的折射定律,其中  $\theta_{1},\theta_{2}$  分别是光线的入射角和折射角(见图 3-16).

还要指出,实际问题中,往往根据问题的性质就可以断定可导函数 $f(x)$ 确有最大值或最小值,而且一定在定义区间内部取得.这时如果 $f(x)$ 在定义区间内部只有一个驻点 $x_{0}$ ,那么不必讨论 $f(x_{0})$ 是不是极值,就可以断定 $f(x_{0})$ 是最大值或最小值.

例6 把一根直径为 $d$ 的圆木锯成截面为矩形的梁(图3-17). 问矩形截面的高 $h$ 和宽 $b$ 应如何选择才能使梁的抗弯截面模量最大？

解 由力学分析知道:矩形梁的抗弯截面模量为

155

---

第三章 微分中值定理与导数的应用

$$
W = \frac {1}{6} b h ^ {2}.
$$

由图 3-17 看出, b 与 h 有下面的关系:

$$
h ^ {2} = d ^ {2} - b ^ {2},
$$

因而

$$
W = \frac {1}{6} (d ^ {2} b - b ^ {3}).
$$

![](../../raw/pages_0161-0192/images/page_172_image_6.jpg)

<details>
<summary>text_image</summary>

d
h
b
</details>

图3-17

这样， $W$ 就与 $b$ 存在函数关系， $b$ 的变化范围是 $(0,d)$ .现在，

问题化为: b 等于多少时目标函数  $W = W(b)$  取最大值? 为此, 求 W 对 b 的导数

$$
W ^ {\prime} = \frac {1}{6} (d ^ {2} - 3 b ^ {2}).
$$

令  $W' = 0$ , 解得

$$
b = \sqrt {\frac {1}{3}} d.
$$

由于梁的最大抗弯截面模量一定存在,而且在 $(0,d)$ 内部取得;现在, $W'=0$ 在 $(0,d)$ 内只有一个根 $b=\sqrt{\frac{1}{3}}d$ ,所以,当 $b=\sqrt{\frac{1}{3}}d$ 时,W的值最大.这时,

$$
h ^ {2} = d ^ {2} - b ^ {2} = d ^ {2} - \frac {1}{3} d ^ {2} = \frac {2}{3} d ^ {2},
$$

即

$$
h = \sqrt {\frac {2}{3}} d.
$$

亦即

$$
d: h: b = \sqrt {3}: \sqrt {2}: 1.
$$

例 7 假设某工厂生产某产品 x 万件的成本是  $C(x)=x^{3}-6x^{2}+15x$ ，售出该产品 x 万件的收入是  $r(x)=9x$ 。问是否存在一个能取得最大利润的生产水平？如果存在的话，找出这个生产水平。

解 由题意知,售出 x 万件产品的利润是

$$
p (x) = r (x) - C (x).
$$

如果 $p(x)$ 取得最大值, 那么它一定在使得 $p'(x) = 0$ 的生产水平处获得. 因此, 令

$$
p ^ {\prime} (x) = r ^ {\prime} (x) - C ^ {\prime} (x) = 0,
$$

即

$$
r ^ {\prime} (x) = C ^ {\prime} (x).
$$

得

156

---

第五节 函数的极值与最大值最小值

$$
x ^ {2} - 4 x + 2 = 0.
$$

解得  $x=\frac{4\pm\sqrt{8}}{2}=2\pm\sqrt{2}$ ，即

$$
x _ {1} = 2 - \sqrt {2} \approx 0. 5 8 6, \quad x _ {2} = 2 + \sqrt {2} \approx 3. 4 1 4.
$$

又

$$
p ^ {\prime \prime} (x) = - 6 x + 1 2, p ^ {\prime \prime} (x _ {1}) > 0, \quad p ^ {\prime \prime} (x _ {2}) <   0.
$$

故在  $x_{2}=3.414$  处达到最大利润, 而在  $x_{1}=0.586$  处发生局部最大亏损.

在经济学中,称  $C'(x)$  为边际成本, $r'(x)$  为边际收入, $p'(x)$  为边际利润.上述结果表明:在给出最大利润的生产水平上, $r'(x)=C'(x)$ ,即边际收入等于边际成本.上面的结果也可以从图3-18的成本曲线和收入曲线中看出.

![](../../raw/pages_0161-0192/images/page_173_chart_8.jpg)

<details>
<summary>line</summary>

| X | C(x) | r(x) |
| --- | --- | --- |
| \(2-\sqrt{2}\) | ~8 | ~8 |
| \(2+\sqrt{2}\) | ~20 | ~20 |
</details>

图3-18

## 习题3-5

1. 求下列函数的极值:

(1) $y = 2x^{3} - 6x^{2} - 18x + 7$;

(2) $y = x - \ln (1 + x)$;

(3) $y = -x^4 + 2x^2$;

(4) $y = x + \sqrt{1 - x}$;

(5)  $y=\frac{1+3x}{\sqrt{4+5x^{2}}}$ ;

(6) $y = \frac{3x^2 + 4x + 4}{x^2 + x + 1}$;

(7) $y = e^{x} \cos x;$

(8) $y = x^{\frac{1}{x}}$;

(9) $y = 3 - 2(x + 1)^{\frac{1}{3}}$;

(10)  $y = x + \tan x.$

2. 试证明: 如果函数  $y=ax^{3}+bx^{2}+cx+d$  满足条件  $b^{2}-3ac<0$ , 那么这个函数没有极值.
3. 试问 $a$ 为何值时, 函数 $f(x) = a \sin x + \frac{1}{3} \sin 3x$ 在 $x = \frac{\pi}{3}$ 处取得极值? 它是极大值还是极小值? 并求此极值.
4. 设函数 $f(x)$ 在 $x_0$ 处有 $n$ 阶导数，且 $f'(x_0) = f''(x_0) = \cdots = f^{(n-1)}(x_0) = 0, f^{(n)}(x_0) \neq 0$，证明:

(1) 当 n 为奇数时,  $f(x)$  在  $x_{0}$  处不取得极值;
(2) 当 n 为偶数时,  $f(x)$  在  $x_{0}$  处取得极值, 且当  $f^{(n)}(x_{0}) < 0$  时,  $f(x_{0})$  为极大值, 当  $f^{(n)}(x_{0}) > 0$  时,  $f(x_{0})$  为极小值.

5. 试利用习题4的结论, 讨论函数 $f(x) = \mathrm{e}^{x} + \mathrm{e}^{-x} + 2\cos x$ 的极值.

6. 求下列函数的最大值、最小值；

(1) $y = 2x^{3} - 3x^{2}, -1 \leqslant x \leqslant 4;$

(2) $y = x^4 - 8x^2 + 2, -1 \leqslant x \leqslant 3$;

(3) $y = x + \sqrt{1 - x}, -5 \leqslant x \leqslant 1.$

7. 问函数 $y = 2x^{3} - 6x^{2} - 18x - 7$ ($1 \leqslant x \leqslant 4$) 在何处取得最大值？并求出它的最大值.
8. 求下列函数在何处取得最小值或最大值:

157

---

第三章 微分中值定理与导数的应用

(1) $y = x^{2} - \frac{54}{x} (x < 0)$, 最小值; (2) $y = \frac{x}{x^{2} + 1} (x \geqslant 0)$, 最大值.

9. 设函数 $f_{n}(x) = nx(1 - x)^{n}$ ($n = 1,2,3,\dots$), $M(n) = \max_{x\in [0,1]}f_n(x)$, 试求 $\lim_{n\to \infty}M(n)$.

10. 某车间靠墙壁要盖一间长方形小屋,现有存砖只够砌 20 m 长的墙壁.问应围成怎样的长方形才能使这间小屋的面积最大?

11. 要造一圆柱形油罐,体积为 V,问底半径 r 和高 h 各等于多少时,才能使表面积最小?这时底直径与高的比是多少?

12. 某地区防空洞的截面拟建成矩形加半圆(图 3-19). 截面的面积为 $5 \mathrm{~m}^{2}$. 问底宽 $x$ 为多少时才能使截面的周长最小, 从而使建造时所用的材料最省?

13. 设有质量为 5 kg 的物体, 置于水平面上, 受力 F 的作用而开始移动 (图 3-20). 设摩擦系数  $\mu = 0.25$ , 问力 F 与水平线的交角  $\alpha$  为多少时, 才可使力 F 的大小为最小?

![](../../raw/pages_0161-0192/images/page_174_image_7.jpg)

<details>
<summary>text_image</summary>

x
y
</details>

图3-19

![](../../raw/pages_0161-0192/images/page_174_image_9.jpg)

<details>
<summary>text_image</summary>

F
α
P
</details>

图3-20

14. 有一杠杆, 支点在它的一端. 在距支点 $0.1 \mathrm{~m}$ 处挂一质量为 $49 \mathrm{~kg}$ 的物体. 加力 $\pmb{F}$ 于杠杆的另一端使杠杆保持水平 (图3-21). 如果杠杆的线密度为 $5 \mathrm{~kg} / \mathrm{m}$, 求最省力的杆长.

15. 从一块半径为 R 的圆铁片上剪去一个扇形做成一个漏斗(图 3-22). 问留下的扇形的圆心角  $\varphi$  取多大时, 做成的漏斗的容积最大?

![](../../raw/pages_0161-0192/images/page_174_image_13.jpg)

<details>
<summary>text_image</summary>

0.1 m
支点
49 kg
F
</details>

图3-21

![](../../raw/pages_0161-0192/images/page_174_image_15.jpg)

<details>
<summary>text_image</summary>

φ
O
R
</details>

图3-22

16. 某吊车的车身高为  $1.5 \, m$ ，吊臂长  $15 \, m$ 。现在要把一个  $6 \, m$  宽、 $2 \, m$  高的屋架（图 3-23(a)），水平地吊到  $6 \, m$  高的柱子上去（图 3-23(b)），问能否吊得上去？

158

---

第六节 函数图形的描绘

![](../../raw/pages_0161-0192/images/page_175_image_1.jpg)

图3-23

17. 一房地产公司有 50 套公寓要出租. 当月租金定为 4 000 元时, 公寓会全部租出去. 当月租金每增加 200 元时, 就会多一套公寓租不出去, 而租出去的公寓平均每月需花费 400 元的维修费. 试问房租定为多少可获得最大收入?
18. 已知制作一个背包的成本为 40 元. 如果每一个背包的售出价格为 $x$ 元, 售出的背包数由

$$
n = \frac {a}{x - 4 0} + b (8 0 - x)
$$

给出,其中 a,b 为正常数.问什么样的售出价格能带来最大利润?

## 第六节 函数图形的描绘

借助于一阶导数的符号,可以确定函数图形在哪个区间上上升,在哪个区间下降;借助于二阶导数的符号,可以确定函数图形在哪个区间上为凹,在哪个区间上为凸,在什么地方有拐点.知道了函数图形的升降、凹凸以及拐点后,也就可以掌握函数的性态,并把函数的图形画得比较准确.

现在,随着现代计算机技术的发展,借助于计算机和许多数学软件,可以方便地画出各种函数的图形.但是,如何识别机器作图中的误差、如何掌握图形上的关键点、如何选择作图的范围等,从而进行人工干预,仍然需要我们有运用微分学的方法描绘函数图形的基本知识.

利用导数描绘函数图形的一般步骤如下:

第一步 确定函数  $y=f(x)$  的定义域及函数所具有的某些特性（如奇偶性、周期性等），并求出函数的一阶导数  $f'(x)$  和二阶导数  $f''(x)$ ;

第二步 求出一阶导数 $f'(x)$ 和二阶导数 $f''(x)$ 在函数定义域内的全部零点，并求出函数 $f(x)$ 的间断点及 $f'(x)$ 和 $f''(x)$ 不存在的点，用这些点把函数的定义域划分成几个部分区间；

159

---

第三章 微分中值定理与导数的应用

第三步 确定在这些部分区间内 $f'(x)$ 和 $f''(x)$ 的符号，并由此确定函数图形的升降、凹凸和拐点；

第四步 确定函数图形的水平、铅直渐近线以及其他变化趋势；

第五步 算出 $f'(x)$ 和 $f''(x)$ 的零点以及不存在的点所对应的函数值, 定出图形上相应的点; 为了把图形描绘得准确些, 有时还需要补充一些点, 然后结合第三、四步中得到的结果, 连接这些点画出函数 $y = f(x)$ 的图形.

例 1 画出函数  $y=x^{3}-x^{2}-x+1$  的图形.

解（1）所给函数 $y = f(x)$ 的定义域为 $(-\infty, +\infty)$，而

$$
f ^ {\prime} (x) = 3 x ^ {2} - 2 x - 1 = (3 x + 1) (x - 1),
$$

$$
f ^ {\prime \prime} (x) = 6 x - 2 = 2 (3 x - 1).
$$

(2) $f'(x)$ 的零点为 $x=-\frac{1}{3}$ 和 x=1; $f''(x)$ 的零点为 $x=\frac{1}{3}$. 将点 $x=-\frac{1}{3}, x=\frac{1}{3}, x=1$ 由小到大排列, 依次把定义域 $(-∞,+∞)$ 划分成四个部分区间

$$
\left(- \infty , - \frac {1}{3} \right], \quad \left[ - \frac {1}{3}, \frac {1}{3} \right], \quad \left[ \frac {1}{3}, 1 \right], \quad [ 1, + \infty).
$$

（3）在 $\left(-\infty,-\frac{1}{3}\right)$ 内， $f'(x)>0,f''(x)<0$ ，所以在 $\left(-\infty,-\frac{1}{3}\right]$ 上的曲线弧上升而且是凸的.

在 $\left(-\frac{1}{3},\frac{1}{3}\right)$ 内， $f'(x)<0$ ， $f''(x)<0$ ，所以在 $\left[-\frac{1}{3},\frac{1}{3}\right]$ 上的曲线弧下降而且是凸的.

同样,可以讨论在区间 $\left[\frac{1}{3},1\right]$ 及区间 $[1,+\infty)$ 上相应的曲线弧的升降和凹凸.为了明确起见,我们把所得的结论列成下表:

| x | $\left(-\infty,-\frac{1}{3}\right)$ | $-\frac{1}{3}$ | $\left(-\frac{1}{3},\frac{1}{3}\right)$ | $\frac{1}{3}$ | $\left(\frac{1}{3},1\right)$ | 1 | $(1,+\infty)$ |
| --- | --- | --- | --- | --- | --- | --- | --- |
| f'(x) | + | 0 | - | - | - | 0 | + |
| f''(x) | - | - | - | 0 | + | + | + |
| y=f(x)的图形 |  |  |  | 拐点 |  |  |  |

这里记号（表示曲线弧上升而且是凸的，表示曲线弧下降而且是凸的，表示曲线弧下降而且是凹的，表示曲线弧上升而且是凹的.

160

---

第六节 函数图形的描绘

(4) 当  $x \to +\infty$  时,  $y \to +\infty$ ; 当  $x \to -\infty$  时,  $y \to -\infty$ .
(5) 算出  $x = -\frac{1}{3}, x = \frac{1}{3}, x = 1$  处的函数值

$$
f \left(- \frac {1}{3}\right) = \frac {3 2}{2 7}, \quad f \left(\frac {1}{3}\right) = \frac {1 6}{2 7}, \quad f (1) = 0.
$$

从而得到函数  $y=x^{3}-x^{2}-x+1$  图形上的三个点

$$
\left(- \frac {1}{3}, \frac {3 2}{2 7}\right), \quad \left(\frac {1}{3}, \frac {1 6}{2 7}\right), \quad (1, 0).
$$

适当补充一些点.例如,计算出

$$
f (- 1) = 0, \quad f (0) = 1, \quad f \left(\frac {3}{2}\right) = \frac {5}{8},
$$

就可补充描出点 $(-1,0)$ ，点 $(0,1)$ 和点 $\left(\frac{3}{2},\frac{5}{8}\right)$ .结合(3)、(4)中得到的结果,就可以画出

$$
y = x ^ {3} - x ^ {2} - x + 1
$$

的图形(图 3-24).

![](../../raw/pages_0161-0192/images/page_177_chart_12.jpg)

<details>
<summary>line</summary>

| X | Y |
| --- | --- |
| \(-\frac{1}{3}, \frac{32}{27}\) | 1 |
| \(\frac{1}{3}, \frac{16}{27}\) | ~0.5 |
| \(\frac{3}{2}, \frac{5}{8}\) | 1 |
</details>

图3-24

例 2 描绘函数  $y=\frac{1}{\sqrt{2\pi}}e^{-\frac{x^{2}}{2}}$  的图形.

解（1）所给函数 $f(x) = \frac{1}{\sqrt{2\pi}}\mathrm{e}^{-\frac{x^2}{2}}$ 的定义域为 $(- \infty, + \infty)$. 由于

$$
f (- x) = \frac {1}{\sqrt {2 \pi}} \mathrm{e} ^ {- \frac {(- x) ^ {2}}{2}} = \frac {1}{\sqrt {2 \pi}} \mathrm{e} ^ {- \frac {x ^ {2}}{2}} = f (x),
$$

所以 $f(x)$ 是偶函数, 它的图形关于 $y$ 轴对称. 因此可以只讨论 $[0, +\infty)$ 上该函数的图形. 求出

$$
f ^ {\prime} (x) = \frac {1}{\sqrt {2 \pi}} \mathrm{e} ^ {- \frac {x ^ {2}}{2}} \cdot (- x) = - \frac {1}{\sqrt {2 \pi}} x \mathrm{e} ^ {- \frac {x ^ {2}}{2}},
$$

$$
f ^ {\prime \prime} (x) = - \frac {1}{\sqrt {2 \pi}} \left[ \mathrm{e} ^ {- \frac {x ^ {2}}{2}} + x \mathrm{e} ^ {- \frac {x ^ {2}}{2}} \cdot (- x) \right] = \frac {1}{\sqrt {2 \pi}} \mathrm{e} ^ {- \frac {x ^ {2}}{2}} (x ^ {2} - 1).
$$

(2) 在  $[0, +\infty)$  上， $f'(x)$  的零点为 x = 0;  $f''(x)$  的零点为 x = 1. 用点 x = 1 把  $[0, +\infty)$  划分成两个区间  $[0, 1]$  和  $[1, +\infty)$ .

(3) 在 $(0,1)$ 内, $f'(x) < 0$, $f''(x) < 0$, 所以在 $[0,1]$ 上的曲线弧下降而且是凸的. 在 $(1, +\infty)$ 内, $f'(x) < 0$, $f''(x) > 0$, 所以在 $[1, +\infty)$ 上的曲线弧下降而且是凹的. 上述的这些结果, 可以列成下表:

161

---

第三章 微分中值定理与导数的应用

| x | 0 | (0,1) | 1 | (1,+∞) |
| --- | --- | --- | --- | --- |
| f'(x) | 0 | - | - | - |
| f''(x) | - | - | 0 | + |
| y=f(x)的图形 |  | ↘ | 拐点 | ↘ |

(4) 由于  $\lim_{x\to+\infty}f(x)=0$  , 所以图形有一条水平渐近线 y=0.

(5) 算出 $f(0) = \frac{1}{\sqrt{2\pi}}$, $f(1) = \frac{1}{\sqrt{2\pi e}}$. 从而得到函数 $y = \frac{1}{\sqrt{2\pi}} e^{-\frac{x^2}{2}}$ 图形上的两点 $M_1 \left(0, \frac{1}{\sqrt{2\pi}}\right)$ 和 $M_2 \left(1, \frac{1}{\sqrt{2\pi e}}\right)$. 又由 $f(2) = \frac{1}{\sqrt{2\pi} e^2}$ 得 $M_3 \left(2, \frac{1}{\sqrt{2\pi} e^2}\right)$. 结合 (3)、(4) 的讨论, 画出函数 $y = \frac{1}{\sqrt{2\pi}} e^{-\frac{x^2}{2}}$ 在 $[0, +\infty)$ 上的图形. 最后, 利用图形的对称性, 便可得到函数在 $(-∞, 0]$ 上的图形 (图 3-25).

![](../../raw/pages_0161-0192/images/page_178_chart_4.jpg)

<details>
<summary>contour</summary>

| Point | x | y |
| --- | --- | --- |
| M1 | 0 | ~0.8 |
| M2 | 1 | ~0.5 |
| M3 | 2 | ~0.1 |
</details>

图3-25

例 3 描绘函数  $y=1+\frac{36x}{(x+3)^{2}}$  的图形.

解（1）所给函数 $y = f(x)$ 的定义域为 $(-\infty, -3), (-3, +\infty)$.

$$
f ^ {\prime} (x) = \frac {3 6 (3 - x)}{(x + 3) ^ {3}}, \quad f ^ {\prime \prime} (x) = \frac {7 2 (x - 6)}{(x + 3) ^ {4}}.
$$

(2) $f'(x)$ 的零点为 x=3; $f''(x)$ 的零点为 x=6; x=-3 是函数的间断点. 点 x=-3, x=3 和 x=6 把定义域划分成四个部分区间:

$$
(- \infty , - 3), \quad (- 3, 3 ], \quad [ 3, 6 ], \quad [ 6, + \infty).
$$

（3）在各部分区间内 $f'(x)$ 及 $f''(x)$ 的符号，相应曲线弧的升降、凹凸和拐点等如下表:

| x | (-∞,-3) | (-3,3) | 3 | (3,6) | 6 | (6,+∞) |
| --- | --- | --- | --- | --- | --- | --- |
| f'(x) | - | + | 0 | - | - | - |
| f''(x) | - | - | - | - | 0 | + |
| y=f(x)的图形 |  |  |  |  | 拐点 |  |

162

---

第六节 函数图形的描绘

（4）由于 $\lim_{x\to +\infty}f(x) = 1,\lim_{x\to -3}f(x) = -\infty$ ，所以图形有一条水平渐近线 $y = 1$ 和一条铅直渐近线 $x = -3$

(5) 算出 x=3, x=6 处的函数值:

$$
f (3) = 4, \quad f (6) = \frac {1 1}{3},
$$

从而得到图形上的两个点

$$
M _ {1} (3, 4), \quad M _ {2} \bigg (6, \frac {1 1}{3} \bigg).
$$

又由于

$$
f (0) = 1, \quad f (- 1) = - 8, \quad f (- 9) = - 8, \quad f (- 1 5) = - \frac {1 1}{4},
$$

得图形上的四个点

$$
M _ {3} (0, 1), \quad M _ {4} (- 1, - 8), \quad M _ {5} (- 9, - 8), \quad M _ {6} \left(- 1 5, - \frac {1 1}{4}\right).
$$

结合(3)、(4)中得到的结果,画出函数  $y=1+\frac{36x}{(x+3)^{2}}$  的图形如图 3-26 所示.

![](../../raw/pages_0161-0192/images/page_179_chart_11.jpg)

<details>
<summary>contour</summary>

| Point | x | y |
| --- | --- | --- |
| M1 | 3 | ~0.8 |
| M2 | 6 | ~0.7 |
| M3 | 0 | 0 |
| M4 | 0 | 0 |
| M5 | -9 | ~-0.5 |
| M6 | -15 | ~-0.8 |
</details>

图3-26

## 习题3-6

描绘下列函数的图形:

1.  $y=\frac{1}{5}(x^{4}-6x^{2}+8x+7)$ ;
2. $y = \frac{x}{1 + {x}^{2}}$;
3.  $y=e^{-(x-1)^{2}}$ ;

163

---

第三章 微分中值定理与导数的应用

4.  $y=x^{2}+\frac{1}{x};$
5.  $y=\frac{\cos x}{\cos 2x}.$

## 第七节 曲率

## 一、弧微分

作为曲率的预备知识,先介绍弧微分的概念.

设函数 $f(x)$ 在区间 $(a,b)$ 内具有连续导数.在曲线 $y = f(x)$ 上取固定点 $M_0(x_0,y_0)$

作为度量弧长的基点(图3-27)，并规定依x增大的方向作为曲线的正向.对曲线上任一点 $M(x,y)$ ，规定有向弧段 $\widehat{M_{0}M}$ 的值s（简称为弧s）①如下:s的绝对值等于这弧段的长度，当有向弧段 $\widehat{M_{0}M}$ 的方向与曲线的正向一致时s>0，相反时s<0.显然，弧s与x存在函数关系: $s=s(x)$ ，而且 $s(x)$ 是x的单调增加函数.下面来求 $s(x)$ 的导数及微分.

![](../../raw/pages_0161-0192/images/page_180_chart_9.jpg)

<details>
<summary>contour</summary>

| Point | x-coordinate | y-coordinate |
| --- | --- | --- |
| M0 | x0 | — |
| M | x | — |
| M' | \(x+\Delta x\) | — |
</details>

图3-27

设 $x, x + \Delta x$ 为 $(a, b)$ 内两个邻近的点，它们在曲

线 $y = f(x)$ 上的对应点为 $M, M'$ （图3-27），并设对应于 $x$ 的增量为 $\Delta x$ ，弧 $s$ 的增量为 $\Delta s$ ，那么

$$
\Delta s = \widehat {M _ {0} M ^ {\prime}} - \widehat {M _ {0} M} = \widehat {M M ^ {\prime}}.
$$

于是

$$
\begin{array}{l} \left(\frac {\Delta s}{\Delta x}\right) ^ {2} = \left(\widehat {\frac {M M ^ {\prime}}{\Delta x}}\right) ^ {2} = \left(\frac {\widehat {M M ^ {\prime}}}{| M M ^ {\prime} |}\right) ^ {2} \cdot \frac {| M M ^ {\prime} | ^ {2}}{(\Delta x) ^ {2}} \\ = \left(\frac {\widehat {M M ^ {\prime}}}{| M M ^ {\prime} |}\right) ^ {2} \cdot \frac {(\Delta x) ^ {2} + (\Delta y) ^ {2}}{(\Delta x) ^ {2}} = \left(\frac {\widehat {M M ^ {\prime}}}{| M M ^ {\prime} |}\right) ^ {2} \left[ 1 + \left(\frac {\Delta y}{\Delta x}\right) ^ {2} \right], \\ \frac {\Delta s}{\Delta x} = \pm \sqrt {\left(\frac {\widehat {M M ^ {\prime}}}{| M M ^ {\prime} |}\right) ^ {2} \cdot \left[ 1 + \left(\frac {\Delta y}{\Delta x}\right) ^ {2} \right]}. \\ \end{array}
$$

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 有向弧段 $\widehat{M_{0}M}$ 的值也常记作 $\widehat{M_{0}M}$ ，即记号 $\widehat{M_{0}M}$ 既表示有向弧段，又表示有向弧段的值.</span></small>

164

---

第七节 曲率

令 $\Delta x\to 0$ ，取极限，由于 $\Delta x\rightarrow 0$ 时， $M^{\prime}\rightarrow M$ ，这时弧的长度与弦的长度之比的极限等于1，即

$$
\lim _ {M ^ {\prime} \to M} \frac {| \widehat {M M ^ {\prime}} |}{| M M ^ {\prime} |} = 1,
$$

又

$$
\lim _ {\Delta x \to 0} \frac {\Delta y}{\Delta x} = y ^ {\prime},
$$

因此得

$$
\frac {\mathrm{d} s}{\mathrm{d} x} = \pm \sqrt {1 + y ^ {\prime 2}}.
$$

由于 $s = s(x)$ 是单调增加函数，从而根号前应取正号，于是有

$$
\mathrm{d} s = \sqrt {1 + y ^ {\prime 2}} \mathrm{d} x. \tag {7-1}
$$

这就是弧微分公式.

## 二、曲率及其计算公式

我们直觉地认识到:直线不弯曲,半径较小的圆弯曲得比半径较大的圆厉害些,而其他曲线的不同部分有不同的弯曲程度,例如抛物线  $y=x^{2}$  在顶点附近弯曲得比远离顶点的部分厉害些.

在工程技术中,有时需要研究曲线的弯曲程度.例如,船体结构中的钢梁、机床的转轴等,它们在荷载作用下要产生弯曲变形,在设计时对它们的弯曲必须有一定的限制,这就要定量地研究它们的弯曲程度.为此首先要讨论如何用数量来描述曲线的弯曲程度.

在图3-28中可以看出，弧段 $\widehat{M_1M_2}$ 比较平直，当动点沿这段弧从 $M_{1}$ 移动到 $M_{2}$ 时，切线转过的角度 $\varphi_{1}$ 不大，而弧段 $\widehat{M_2M_3}$ 弯曲得比较厉害，角 $\varphi_{2}$ 就比较大.

但是,切线转过的角度的大小还不能完全反映曲线弯曲的程度.例如,从图3-29中可以看出,两段曲线弧 $\widehat{M_{1}M_{2}}$ 及 $\widehat{N_{1}N_{2}}$ 尽管切线转过的角度都是 $\varphi$ ,然而弯曲程度并不相同,短弧段比长弧段弯曲得厉害些.由此可见,曲线弧的弯曲程度还与弧段的长度有关.

按上面的分析,我们引入描述曲线弯曲程度的曲率概念如下:

设曲线 $C$ 是光滑的①, 在曲线 $C$ 上选定一点 $M_0$ 作为度量弧 $s$ 的基点. 设曲线上点

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 当曲线上每一点处都具有切线,且切线随切点的移动而连续转动,这样的曲线称为光滑曲线.</span></small>

165

---

第三章 微分中值定理与导数的应用

![](../../raw/pages_0161-0192/images/page_182_image_1.jpg)

<details>
<summary>text_image</summary>

φ₁
M₂
φ₂
M₃
M₁
</details>

图3-28

![](../../raw/pages_0161-0192/images/page_182_image_3.jpg)

<details>
<summary>text_image</summary>

M₁
N₁
φ
N₂
M₂
</details>

图3-29

M 对应于弧 s, 在点 M 处切线的倾角为  $\alpha$  （这里假定曲线 C 所在的平面上已设立

了xOy坐标系)，曲线上另外一点 $M'$ 对应于弧 $s+\Delta s$ ，在点 $M'$ 处切线的倾角为 $\alpha+\Delta\alpha$ （图3-30），则弧段 $\widehat{MM'}$ 的长度为 $|\Delta s|$ ，当动点从点M移动到点 $M'$ 时切线转过的角度为 $|\Delta\alpha|$ .

我们用比值 $\frac{|\Delta\alpha|}{|\Delta s|}$ ，即单位弧段上切线转过的角度的大小来表达弧段 $\widehat{MM'}$ 的平均弯曲程度，把这比值叫做弧段 $\widehat{MM'}$ 的平均曲率，并记作 $\overline{K}$ ，即

![](../../raw/pages_0161-0192/images/page_182_image_8.jpg)

<details>
<summary>text_image</summary>

y
C
M'
Δs
M
M₀ s
α + Δα
O x
</details>

图3-30

$$
\overline {{K}} = \left| \frac {\Delta \alpha}{\Delta s} \right|.
$$

类似于从平均速度引进瞬时速度的方法, 当  $\Delta s \rightarrow 0$  时(即  $M' \rightarrow M$  时), 上述平均曲率的极限叫做曲线 C 在点 M 处的曲率, 记作 K, 即

$$
K = \lim _ {\Delta s \to 0} \left| \frac {\Delta \alpha}{\Delta s} \right|.
$$

在 $\lim_{\Delta s\to0}\frac{\Delta\alpha}{\Delta s}=\frac{d\alpha}{ds}$ 存在的条件下,K也可以表示为

$$
K = \left| \frac {\mathrm{d} \alpha}{\mathrm{d} s} \right|. \tag {7-2}
$$

对于直线来说,切线与直线本身重合,当点沿直线移动时,切线的倾角  $\alpha$  不变(图3-31),  $\Delta\alpha=0,\frac{\Delta\alpha}{\Delta s}=0$ , 从而  $K=\left|\frac{d\alpha}{ds}\right|=0$ . 这就是说,直线上任意点 M 处的曲率都等于零,这与我们直觉认识到的“直线不弯曲”一致.

设圆的半径为 $a$，由图3-32可见圆在点 $M, M'$ 处的切线所夹的角 $\Delta \alpha$ 等于圆心角 $MDM'$. 但 $\angle MDM' = \frac{\Delta s}{a}$，于是

166

---

第七节 曲率

$$
\frac {\Delta \alpha}{\Delta s} = \frac {\frac {\Delta s}{a}}{\Delta s} = \frac {1}{a},
$$

从而

$$
K = \left| \frac {\mathrm{d} \alpha}{\mathrm{d} s} \right| = \frac {1}{a}.
$$

![](../../raw/pages_0161-0192/images/page_183_image_4.jpg)

<details>
<summary>text_image</summary>

y
M Δs M'
α
O x
</details>

图3-31

![](../../raw/pages_0161-0192/images/page_183_image_6.jpg)

<details>
<summary>text_image</summary>

y
D
a
Δα
M'
T'
M
α+Δα
O
x
</details>

图3-32

因为点 $M$ 是圆上任意取定的一点，上述结论表示圆上各点处的曲率都等于半径 $a$ 的倒数 $\frac{1}{a}$，这就是说，圆的弯曲程度到处一样，且半径越小曲率越大，即圆弯曲得越厉害.

在一般情况下,我们根据(7-2)式来导出便于实际计算曲率的公式.

设曲线的直角坐标方程是  $y=f(x)$ ，且  $f(x)$  具有二阶导数（这时  $f'(x)$  连续，从而曲线是光滑的）。因为  $\tan\alpha=y'$ ，所以

$$
\sec^ {2} \alpha \frac {\mathrm{d} \alpha}{\mathrm{d} x} = y ^ {\prime \prime},
$$

$$
\frac {\mathrm{d} \alpha}{\mathrm{d} x} = \frac {y ^ {\prime \prime}}{1 + \tan^ {2} \alpha} = \frac {y ^ {\prime \prime}}{1 + y ^ {2}},
$$

于是

$$
\mathrm{d} \alpha = \frac {y ^ {\prime \prime}}{1 + y ^ {\prime 2}} \mathrm{d} x.
$$

又由(7-1)知道

$$
\mathrm{d} s = \sqrt {1 + y ^ {\prime 2}} \mathrm{d} x.
$$

从而,根据曲率 K 的表达式(7-2),有

$$
K = \frac {| y ^ {\prime \prime} |}{(1 + y ^ {2}) ^ {3 / 2}}. \tag {7-3}
$$

167

---

第三章 微分中值定理与导数的应用

设曲线由参数方程

$$
\left\{ \begin{array}{l} x = \varphi (t), \\ y = \psi (t) \end{array} \right.
$$

给出,则可利用由参数方程所确定的函数的求导法,求出  $y_{x}^{\prime}$  及  $y_{x}^{\prime\prime}$ ,代入(7-3)便得

$$
K = \frac {\left| \varphi^ {\prime} (t) \psi^ {\prime \prime} (t) - \varphi^ {\prime \prime} (t) \psi^ {\prime} (t) \right|}{\left[ \varphi^ {\prime 2} (t) + \psi^ {\prime 2} (t) \right] ^ {3 / 2}}. \tag {7-4}
$$

例1 计算等边双曲线 $xy = 1$ 在点(1,1)处的曲率.

解 由 $y = \frac{1}{x}$，得

$$
y ^ {\prime} = - \frac {1}{x ^ {2}}, \quad y ^ {\prime \prime} = \frac {2}{x ^ {3}}.
$$

因此，

$$
y ^ {\prime} \mid_ {x = 1} = - 1, \quad y ^ {\prime \prime} \mid_ {x = 1} = 2.
$$

把它们代入公式(7-3)，便得曲线 $xy = 1$ 在点(1,1)处的曲率为

$$
K = \frac {2}{[ 1 + (- 1) ^ {2} ] ^ {3 / 2}} = \frac {\sqrt {2}}{2}.
$$

例2 抛物线 $y = ax^{2} + bx + c (a \neq 0)$ 上哪一点处的曲率最大？

解 由 $y = ax^2 + bx + c$，得

$$
y ^ {\prime} = 2 a x + b, \quad y ^ {\prime \prime} = 2 a,
$$

代入公式(7-3)，得

$$
K = \frac {\mid 2 a \mid}{\left[ 1 + (2 a x + b) ^ {2} \right] ^ {3 / 2}}.
$$

因为 K 的分子是常数  $\left|2a\right|$ ，所以只要分母最小，K 就最大。容易看出，当  $2ax + b = 0$ ，即  $x = -\frac{b}{2a}$  时，K 的分母最小，因而 K 有最大值  $\left|2a\right|$ 。而  $x = -\frac{b}{2a}$  所对应的点为抛物线的顶点。因此，抛物线在顶点处的曲率最大。

在有些实际问题中， $|y'|$ 同1比较起来是很小的（有的工程技术书上把这种关系记成 $|y'|\ll1$ ），可以忽略不计。这时，由

$$
1 + y ^ {\prime 2} \approx 1,
$$

而有曲率的近似计算公式

$$
K = \frac {| y ^ {\prime \prime} |}{(1 + y ^ {2}) ^ {3 / 2}} \approx | y ^ {\prime \prime} |.
$$

这就是说, 当  $\left|y'\right|\ll1$  时, 曲率 K 近似于  $\left|y''\right|$ . 经过这样简化之后, 对一些复杂问题的计算和讨论就方便多了.

168

---

第七节 曲率

## 三、曲率圆与曲率半径

设曲线 $y = f(x)$ 在点 $M(x, y)$ 处的曲率为 $K (K \neq 0)$. 在点 $M$ 处的曲线的法线上，

在凹的一侧取一点 D，使  $\left|DM\right|=\frac{1}{K}=\rho$ 。以 D 为圆心， $\rho$  为半径作圆（图 3-33），这个圆叫做曲线在点 M 处的曲率圆，曲率圆的圆心 D 叫做曲线在点 M 处的曲率中心，曲率圆的半径  $\rho$  叫做曲线在点 M 处的曲率半径。

按上述规定可知,曲率圆与曲线在点 M 有相同的切线和曲率,且在点 M 邻近有相同的凹向.因此,在

![](../../raw/pages_0161-0192/images/page_185_image_5.jpg)

<details>
<summary>text_image</summary>

y
D ρ=1/K
M
y=f(x)
O x
</details>

图3-33

实际问题中,常常用曲率圆在点M邻近的一段圆弧来近似代替曲线弧,以使问题简化.

按上述规定.曲线在点 $M$ 处的曲率 $K(K \neq 0)$ 与曲线在点 $M$ 处的曲率半径 $\rho$ 有如下关系:

$$
\rho = \frac {1}{K}, \quad K = \frac {1}{\rho}.
$$

这就是说:曲线上一点处的曲率半径与曲线在该点处的曲率互为倒数.

例 3 设工件内表面的截线为抛物线  $y = 0.4x^{2}$  (图 3-34). 现在要用砂轮磨削其内表面. 问用直径多大的砂轮才比较合适?

解 为了在磨削时不使砂轮与工件接触处附近的那部分工件磨去太多,砂轮的半径应不大于抛物线上各点处曲率半径中的最小值.由本节例2知道,抛物线在其顶点处的曲率最大,也就是说,抛物

![](../../raw/pages_0161-0192/images/page_185_chart_13.jpg)

<details>
<summary>contour</summary>

| Feature | Value |
| --- | --- |
| Parabola Equation | \(y=0.4x^{2}\) |
| Intersection Point | (1.25, 0) |
</details>

图3-34

线在其顶点处的曲率半径最小.因此,只要求出抛物线 $y=0.4x^{2}$ 在顶点 $O(0,0)$ 处的曲率半径.由

$$
y ^ {\prime} = 0. 8 x, \quad y ^ {\prime \prime} = 0. 8,
$$

而有

$$
y ^ {\prime} \mid_ {x = 0} = 0, \quad y ^ {\prime \prime} \mid_ {x = 0} = 0. 8.
$$

把它们代入公式(7-3)，得

$$
K = 0. 8.
$$

因而求得抛物线顶点处的曲率半径

169

---

第三章 微分中值定理与导数的应用

$$
\rho = \frac {1}{K} = 1. 2 5.
$$

所以选用砂轮的半径不得超过 1.25 单位长, 即直径不得超过 2.50 单位长.

对于用砂轮磨削一般工件的内表面时,也有类似的结论,即选用的砂轮的半径不应超过这工件内表面的截线上各点处曲率半径中的最小值.

## \* 四、曲率中心的计算公式 渐屈线与渐伸线

设已知曲线的方程是  $y=f(x)$ ，且其二阶导数  $y''$  在点 x 不为零，则曲线在对应点  $M(x,y)$  的曲率中心  $D(\alpha,\beta)$  的坐标为

$$
\left\{ \begin{array}{l} \alpha = x - \frac {y ^ {\prime} (1 + y ^ {\prime 2})}{y ^ {\prime \prime}}, \\ \beta = y + \frac {1 + y ^ {\prime 2}}{y ^ {\prime \prime}}. \end{array} \right. \tag {7-5}
$$

这是因为,曲线  $y=f(x)$  在点  $M(x,y)$  的曲率圆的方程为

$$
(\xi - \alpha) ^ {2} + (\eta - \beta) ^ {2} = \rho^ {2},
$$

其中  $\xi,\eta$  是曲率圆上的动点坐标,且

$$
\rho^ {2} = \frac {1}{K ^ {2}} = \frac {(1 + y ^ {\prime 2}) ^ {3}}{y ^ {\prime \prime 2}}.
$$

因为点 M 在曲率圆上, 所以

$$
(x - \alpha) ^ {2} + (y - \beta) ^ {2} = \rho^ {2}; \tag {7-6}
$$

又因为曲线在点 $M$ 的切线与曲率圆的半径 $DM$ 相垂直(图3-33)，所以

$$
y ^ {\prime} = - \frac {x - \alpha}{y - \beta}. \tag {7-7}
$$

由式(7-6)和(7-7)消去 $x - \alpha$ ，解出

$$
(y - \beta) ^ {2} = \frac {\rho^ {2}}{1 + y ^ {\prime 2}} = \frac {(1 + y ^ {\prime 2}) ^ {2}}{y ^ {\prime \prime 2}}.
$$

由于当 $y'' > 0$ 时曲线为凹弧，$y - \beta < 0$；当 $y'' < 0$ 时曲线为凸弧，$y - \beta > 0$。总之，$y''$ 与 $y - \beta$ 异号。因此取上式两边的平方根，得

$$
y - \beta = - \frac {1 + y ^ {\prime 2}}{y ^ {\prime \prime}},
$$

又

$$
x - \alpha = - y ^ {\prime} (y - \beta) = \frac {y ^ {\prime} (1 + y ^ {\prime 2})}{y ^ {\prime \prime}}.
$$

从而有公式(7-5).

当点 $(x, f(x))$ 沿曲线 $C$ 移动时，相应的曲率中心 $D$ 的轨迹曲线 $G$ 称为曲线 $C$ 的

170

---

第七节 曲率

渐屈线,而曲线 C 称为曲线 G 的渐伸线(图3-35).所以曲线  $y=f(x)$  的渐屈线的参数方程为

$$
\left\{ \begin{array}{l} \alpha = x - \frac {y ^ {\prime} (1 + y ^ {\prime 2})}{y ^ {\prime \prime}}, \\ \beta = y + \frac {1 + y ^ {\prime 2}}{y ^ {\prime \prime}}, \end{array} \right. \tag {7-8}
$$

其中 $y = f(x), y' = f'(x), y'' = f''(x), x$ 为参数，直角坐标系 $\alpha O\beta$ 与 $xOy$ 坐标系重合.

![](../../raw/pages_0161-0192/images/page_187_image_4.jpg)

<details>
<summary>text_image</summary>

y
β
G
C
O
α
x
</details>

图3-35

例4 求摆线

$$
\left\{ \begin{array}{l} x = a (t - \sin t), \\ y = a (1 - \cos t) \end{array} \right.
$$

的渐屈线方程.

解 $\frac{\mathrm{d}x}{\mathrm{d}t} = a(1 - \cos t),\frac{\mathrm{d}y}{\mathrm{d}t} = a\sin t$ ，所以

$$
\frac {\mathrm{d} y}{\mathrm{d} x} = \frac {\sin t}{1 - \cos t},
$$

$$
\frac {\mathrm{d} ^ {2} y}{\mathrm{d} x ^ {2}} = \frac {\frac {\mathrm{d}}{\mathrm{d} t} \left(\frac {\mathrm{d} y}{\mathrm{d} x}\right)}{\frac {\mathrm{d} x}{\mathrm{d} t}} = \frac {\frac {\cos t - 1}{(1 - \cos t) ^ {2}}}{a (1 - \cos t)} = - \frac {1}{a (1 - \cos t) ^ {2}}.
$$

将这些结果代入(7-8)式并化简,便得摆线的渐屈线的参数方程

$$
\left\{ \begin{array}{l} \alpha = a (t + \sin t), \\ \beta = a (\cos t - 1), \end{array} \right. \tag {7-9}
$$

其中 t 为参数, 直角坐标系  $\alpha O\beta$  与 xOy 坐标系重合. 为了作出渐屈线 (7-9), 令  $t = \pi + \tau$ , 代入 (7-9) 式得

$$
\left\{ \begin{array}{l} \alpha - \pi a = a (\tau - \sin \tau), \\ \beta + 2 a = a (1 - \cos \tau), \end{array} \right.
$$

再令 $\alpha -\pi a = \xi ,\beta +2a = \eta$ ，则得

$$
\left\{ \begin{array}{l} \xi = a (\tau - \sin \tau), \\ \eta = a (1 - \cos \tau). \end{array} \right. \tag {7-10}
$$

在新坐标系  $\xi O_{1}\eta$  中, 曲线 (7-10) 为一摆线, 其中新坐标系  $\xi O_{1}\eta$  由旧坐标系 xOy 平移到新原点  $O_{1}(\pi a,-2a)$  得到. 由此可知摆线的渐屈线仍为一摆线, 如图3-36所示.

171

---

第三章 微分中值定理与导数的应用

![](../../raw/pages_0161-0192/images/page_188_image_1.jpg)

<details>
<summary>text_image</summary>

y β η
G
O
α x
O₁ (πa, -2a)
ξ
</details>

图3-36

## 习题3-7

1. 求椭圆  $4x^{2}+y^{2}=4$  在点  $(0,2)$  处的曲率.

2. 求曲线  $\gamma=\ln \sec x$  在点  $(x,y)$  处的曲率及曲率半径.

3. 求抛物线  $y=x^{2}-4x+3$  在其顶点处的曲率及曲率半径.

4. 求曲线  $x = a \cos^{3} t, y = a \sin^{3} t$  在  $t = t_{0}$  相应的点处的曲率.

5. 对数曲线  $\gamma=\ln x$  上哪一点处的曲率半径最小？求出该点处的曲率半径.

\* 6. 证明曲线 $y = a \operatorname{ch} \frac{x}{a}$ 在点 $(x, y)$ 处的曲率半径为 $\frac{y^2}{a}$.

7. 一飞机沿抛物线路径 $y = \frac{x^2}{10000}$ (y 轴铅直向上, 单位为 m) 做俯冲飞行. 在坐标原点 O 处飞机的速度为 $v = 200 \mathrm{~m/s}$. 飞行员体重 $G = 70 \mathrm{~kg}$. 求飞机俯冲至最低点即原点 O 处时座椅对飞行员的反力.

8. 汽车连同载质量共 5 t, 在抛物线拱桥上行驶, 速度为 21.6 km/h, 桥的跨度为 10 m, 拱的矢高为 0.25 m (图 3-37). 求汽车越过桥顶时对桥的压力.

![](../../raw/pages_0161-0192/images/page_188_image_12.jpg)

<details>
<summary>text_image</summary>

0.25 m
10 m
</details>

图3-37

9. 设 $R$ 为抛物线 $y = x^2$ 上任一点 $M(x, y)$ 处的曲率半径，$s$ 为该曲线上某一点 $M_0$ 到点 $M$ 的弧长，证明:$3R \frac{\mathrm{d}^2 R}{\mathrm{d}s^2} - \left(\frac{\mathrm{d}R}{\mathrm{d}s}\right)^2 - 9 = 0.$

\* 10. 求曲线 $y = \tan x$ 在点 $\left( \frac{\pi}{4}, 1 \right)$ 处的曲率圆方程.

\*11. 求抛物线 $\gamma^2 = 2px$ 的渐屈线方程.

172

---

第八节 方程的近似解

## 第八节 方程的近似解

在科学技术问题中,经常会遇到求解高次代数方程或其他类型的方程的问题.要求得这类方程的实根的精确值,往往比较困难,因此就需要寻求方程的近似解.

求方程的近似解,可分两步来做.

第一步是确定根的大致范围.具体地说,就是确定一个区间 $[a,b]$ ,使所求的根是位于这个区间内的唯一实根.这一步工作称为根的隔离,区间 $[a,b]$ 称为所求实根的隔离区间.由于方程 $f(x)=0$ 的实根在几何上表示曲线 $y=f(x)$ 与x轴交点的横坐标,因此为了确定根的隔离区间,可以先较精确地画出 $y=f(x)$ 的图形,然后从图上定出它与x轴交点的大概位置.由于作图和读数的误差,这种做法得不出根的高精确度的近似值,但一般已可以确定出根的隔离区间.

第二步是以根的隔离区间的端点作为根的初始近似值,逐步改善根的近似值的精确度,直至求得满足精确度要求的近似解.完成这一步工作有多种方法,这里我们介绍三种常用的方法——二分法、切线法和割线法,按照这些方法,编出简单的程序,就可以在计算机上求出方程足够精确的近似解.

## 一、二分法

设 $f(x)$ 在区间 $[a, b]$ 上连续，$f(a) \cdot f(b) < 0$，且方程 $f(x) = 0$ 在 $(a, b)$ 内仅有一个实根 $\xi$，于是 $[a, b]$ 即是这个根的一个隔离区间。

取 $[a, b]$ 的中点 $\xi_1 = \frac{a + b}{2}$, 计算 $f(\xi_1)$.

如果 $f(\xi_{1})=0$ ,那么 $\xi=\xi_{1}$ ;

如果 $f(\xi_1)$ 与 $f(a)$ 同号，那么取 $a_1 = \xi_1, b_1 = b$ ，由 $f(a_1) \cdot f(b_1) < 0$ ，即知 $a_1 < \xi < b_1$ 且 $b_1 - a_1 = \frac{1}{2}(b - a)$

如果 $f(\xi_1)$ 与 $f(b)$ 同号，那么取 $a_1 = a, b_1 = \xi_1$ ，也有 $a_1 < \xi < b_1$ 及 $b_1 - a_1 = \frac{1}{2}(b - a)$

总之，当 $\xi \neq \xi_{1}$ 时，可求得 $a_1 < \xi < b_1$ ，且 $b_{1} - a_{1} = \frac{1}{2}(b - a)$.

以 $[a_{1}, b_{1}]$ 作为新的隔离区间, 重复上述做法, 当 $\xi \neq \xi_{2} = \frac{1}{2}(a_{1} + b_{1})$ 时, 可求得 $a_{2} < \xi < b_{2}$, 且 $b_{2} - a_{2} = \frac{1}{2^{2}}(b - a)$.

173

---

第三章 微分中值定理与导数的应用

如此重复 $n$ 次, 可求得 $a_{n} < \xi < b_{n}$, 且 $b_{n} - a_{n} = \frac{1}{2^{n}} (b - a)$. 由此可知, 如果以 $a_{n}$ 或 $b_{n}$ 作为 $\xi$ 的近似值, 那么其误差小于 $\frac{1}{2^{n}} (b - a)$.

例 1 用二分法求方程  $x^{3}+1.1x^{2}+0.9x-1.4=0$  的实根的近似值, 使误差不超过  $10^{-3}$ ①.

解 令 $f(x) = x^3 + 1.1x^2 + 0.9x - 1.4$，显然 $f(x)$ 在 $(- \infty, +\infty)$ 内连续.

由 $f^{\prime}(x) = 3x^{2} + 2.2x + 0.9$ ，根据判别式 $B^{2} - 4AC = 2.2^{2} - 4\times 3\times 0.9 = -5.96 <   0$ ，知 $f^{\prime}(x) > 0.$ 故 $f(x)$ 在 $(-\infty , + \infty)$ 内单调增加， $f(x) = 0$ 至多有一个实根.

由 $f(0) = -1.4 < 0, f(1) = 1.6 > 0$ ，知 $f(x) = 0$ 在 $[0,1]$ 内有唯一的实根.取 $a = 0, b = 1, [0,1]$ 即是一个隔离区间.

计算得

$$
\xi_ {1} = 0. 5, f \left(\xi_ {1}\right) = - 0. 5 5 <   0 \text {, 故} a _ {1} = 0. 5, b _ {1} = 1;
$$

$$
\xi_ {2} = 0. 7 5, f \left(\xi_ {2}\right) = 0. 3 2 > 0 \text {, 故} a _ {2} = 0. 5, b _ {2} = 0. 7 5;
$$

$$
\xi_ {3} = 0. 6 2 5, f \left(\xi_ {3}\right) = - 0. 1 6 <   0 \text {, 故} a _ {3} = 0. 6 2 5, b _ {3} = 0. 7 5;
$$

$$
\xi_ {4} = 0. 6 8 7, f \left(\xi_ {4}\right) = 0. 0 6 2 > 0 \text {, 故} a _ {4} = 0. 6 2 5, b _ {4} = 0. 6 8 7;
$$

$$
\xi_ {5} = 0. 6 5 6, f \left(\xi_ {5}\right) = - 0. 0 5 4 <   0 \text {, 故} a _ {5} = 0. 6 5 6, b _ {5} = 0. 6 8 7;
$$

$$
\xi_ {6} = 0. 6 7 2, f \left(\xi_ {6}\right) = 0. 0 0 5 > 0 \text {, 故} a _ {6} = 0. 6 5 6, b _ {6} = 0. 6 7 2;
$$

$$
\xi_ {7} = 0. 6 6 4, f \left(\xi_ {7}\right) = - 0. 0 2 5 <   0 \text {, 故} a _ {7} = 0. 6 6 4, b _ {7} = 0. 6 7 2;
$$

$$
\xi_ {8} = 0. 6 6 8, f \left(\xi_ {8}\right) = - 0. 0 1 0 <   0 \text {, 故} a _ {8} = 0. 6 6 8, b _ {8} = 0. 6 7 2;
$$

$$
\xi_ {9} = 0. 6 7 0, f \left(\xi_ {9}\right) = - 0. 0 0 2 <   0 \text {, 故} a _ {9} = 0. 6 7 0, b _ {9} = 0. 6 7 2;
$$

$$
\xi_ {1 0} = 0. 6 7 1, f \left(\xi_ {1 0}\right) = 0. 0 0 1 > 0 \text {, 故} a _ {1 0} = 0. 6 7 0, b _ {1 0} = 0. 6 7 1.
$$

于是

$$
0. 6 7 0 <   \xi <   0. 6 7 1.
$$

即 0.670 作为根的不足近似值,0.671 作为根的过剩近似值,其误差都小于  $10^{-3}$ .

## 二、切线法

设 $f(x)$ 在 $[a, b]$ 上具有二阶导数，$f(a) \cdot f(b) < 0$ 且 $f'(x)$ 及 $f''(x)$ 在 $[a, b]$ 上保持定号。在上述条件下，方程 $f(x) = 0$ 在 $(a, b)$ 内有唯一的实根 $\xi, [a, b]$ 为根的一个隔离区间。此时，$y = f(x)$ 在 $[a, b]$ 上的图形 $\widehat{AB}$ 只有如图3-38所示的四种不同情形。

考虑用曲线弧一端的切线来代替曲线弧,从而求出方程实根的近似值.这种方法

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 按本例误差不超过 $10^{-3}$ 的要求, 计算时只取 3 位小数.</span></small>

174

---

第八节 方程的近似解

![](../../raw/pages_0161-0192/images/page_191_image_1.jpg)

<details>
<summary>text_image</summary>

y
y=f(x)
a
ξ
O
x₁
b
B
A
x
</details>

(a) $f(a) < 0, f(b) > 0$ $f'(x) > 0, f''(x) > 0$

![](../../raw/pages_0161-0192/images/page_191_chart_3.jpg)

<details>
<summary>line</summary>

| Point | x-coordinate | y-coordinate |
| --- | --- | --- |
| A | a | f(x) |
| B | b | 0 |
</details>

(b) $f(a) > 0, f(b) < 0$ $f'(x) < 0, f''(x) > 0$

![](../../raw/pages_0161-0192/images/page_191_chart_5.jpg)

<details>
<summary>line</summary>

| Point | x | y |
| --- | --- | --- |
| A | a | 0 |
| B | b | y |
</details>

(c)  $f(a)<0,\ f(b)>0$ 
 $f'(x)>0, f''(x)<0$

![](../../raw/pages_0161-0192/images/page_191_chart_7.jpg)

<details>
<summary>line</summary>

| Point | x | y |
| --- | --- | --- |
| A | a | f(x) |
| B | b | 0 |
</details>

(d) $f(a) > 0, f(b) < 0$ $f'(x) < 0, f''(x) < 0$

图3-38

叫做切线法.从图3-38中看出,如果在纵坐标与 $f''(x)$ 同号的那个端点(此端点记作 $(x_{0},f(x_{0})))$ 处作切线,这切线与x轴的交点的横坐标 $x_{1}$ 就比 $x_{0}$ 更接近方程的根 $\xi$ .

下面以图3-38(a): $f(a)<0,f(b)>0,f'(x)>0$ ,  $f''(x)>0$  的情形为例进行讨论. 此时, 因为 $f(b)$ 与 $f''(x)$ 同号, 所以令 $x_{0}=b$ , 在端点 $(x_{0},f(x_{0}))$ 处作切线(图3-39), 这切线的方程为

$$
y - f (x _ {0}) = f ^ {\prime} (x _ {0}) (x - x _ {0}).
$$

令 y=0，从上式中解出 x，就得到切线与 x 轴交点的横坐标为

![](../../raw/pages_0161-0192/images/page_191_chart_14.jpg)

<details>
<summary>line</summary>

| Point | X-coordinate | Y-coordinate |
| --- | --- | --- |
| Origin | 0 | 0 |
| \(\xi\) | \(x_{2}\) | 0 |
| \(x_{1}\) | \(x_{1}\) | 0 |
| b | b | y=f(x) |
</details>

图3-39

$$
x _ {1} = x _ {0} - \frac {f (x _ {0})}{f ^ {\prime} (x _ {0})},
$$

它比 $x_0$ 更接近方程的根 $\xi$.

再在点 $(x_{1},f(x_{1}))$ 处作切线,可得根的近似值 $x_{2}$ .如此继续,一般地,在点 $(x_{n},f(x_{n}))$ 处作切线,得根的近似值

$$
x _ {n + 1} = x _ {n} - \frac {f (x _ {n})}{f ^ {\prime} (x _ {n})}. \tag {8-1}
$$

如果 $f(a)$ 与 $f''(x)$ 同号，那么切线作在端点 $(a, f(a))$ 处（如图3-38情形(b)及(c))，可记 $x_0 = a$ ，仍按公式(8-1)计算切线与 $x$ 轴交点的横坐标.

175

---

第三章 微分中值定理与导数的应用

例 2 用切线法求方程  $x^{3}+1.1x^{2}+0.9x-1.4=0$  的实根的近似值, 使误差不超过  $10^{-3}$ .

解 令 $f(x) = x^3 + 1.1x^2 + 0.9x - 1.4$. 由例 1 知 $[0,1]$ 是根的一个隔离区间. $f(0) < 0$, $f(1) > 0$.

在 $[0,1]$ 上，

$$
f ^ {\prime} (x) = 3 x ^ {2} + 2. 2 x + 0. 9 > 0, \quad f ^ {\prime \prime} (x) = 6 x + 2. 2 > 0,
$$

故 $f(x)$ 在 $[0,1]$ 上的图形属于图3-38中情形(a).按 $f''(x)$ 与 $f(1)$ 同号，所以令 $x_0 = 1$

连续应用公式(8-1)，得

$$
\begin{array}{l} x _ {1} = 1 - \frac {f (1)}{f ^ {\prime} (1)} \approx 0. 7 3 8, \\ x _ {2} = 0. 7 3 8 - \frac {f (0 . 7 3 8)}{f ^ {\prime} (0 . 7 3 8)} \approx 0. 6 7 4, \\ x _ {3} = 0. 6 7 4 - \frac {f (0 . 6 7 4)}{f ^ {\prime} (0 . 6 7 4)} \approx 0. 6 7 1, \\ x _ {4} = 0. 6 7 1 - \frac {f (0 . 6 7 1)}{f ^ {\prime} (0 . 6 7 1)} \approx 0. 6 7 1. \\ \end{array}
$$

至此,计算不能再继续.注意到 $f(x_{i})$  ( $i=0,1,\cdots$ )与 $f''(x)$ 同号,知 $f(0.671)>0$ ,经计算可知 $f(0.670)<0$ ,于是有

$$
0. 6 7 0 <   \xi <   0. 6 7 1.
$$

以 0.670 或 0.671 作为根的近似值, 其误差都小于  $10^{-3}$ .

## 三、割线法

利用切线法需要计算函数的导数, 当  $f(x)$  比较复杂时, 计算  $f'(x)$  可能有困难. 这时, 可考虑用

$$
\frac {f (x _ {n}) - f (x _ {n - 1})}{x _ {n} - x _ {n - 1}}
$$

来近似代替(8-1)式中的 $f'(x_{n})$ ，这时的迭代公式成为

$$
x _ {n + 1} = x _ {n} - \frac {x _ {n} - x _ {n - 1}}{f (x _ {n}) - f (x _ {n - 1})} \cdot f (x _ {n}), \tag {8-2}
$$

其中， $x_0, x_1$ 为初始值。迭代公式(8-2)的几何意义是用过点 $(x_{n-1}, f(x_{n-1}))$ 和点 $(x_n, f(x_n))$ 的割线来近似代替点 $(x_n, f(x_n))$ 处的切线，将这条割线与 $x$ 轴交点的横坐标作为新的近似值（见图3-40）。因此，这个方法叫做割线法或弦截法。

![](../../raw/pages_0193-0224/images/page_192_chart_17.jpg)

<details>
<summary>line</summary>

| Point | X-coordinate | Y-coordinate |
| --- | --- | --- |
| \(\xi\) | \(x_{n+1}\) | — |
| \(x_n\) | \(x_n\) | — |
| \(b\) | \(x_{n-1}\) | — |
</details>

图3-40

176

---

总习题三

以下用割线法对例 2 中的方程求近似解.

取 $x_0 = 1, x_1 = 0.8$. 连续用迭代公式(8-2)，得

$$
x _ {2} = x _ {1} - \frac {x _ {1} - x _ {0}}{f (x _ {1}) - f (x _ {0})} \cdot f (x _ {1}) \approx 0. 6 9 9,
$$

$$
x _ {3} = x _ {2} - \frac {x _ {2} - x _ {1}}{f (x _ {2}) - f (x _ {1})} \cdot f (x _ {2}) \approx 0. 6 7 2,
$$

$$
x _ {4} = x _ {3} - \frac {x _ {3} - x _ {2}}{f (x _ {3}) - f (x _ {2})} \cdot f (x _ {3}) \approx 0. 6 7 1,
$$

$$
x _ {5} = x _ {4} - \frac {x _ {4} - x _ {3}}{f (x _ {4}) - f (x _ {3})} \cdot f (x _ {4}) \approx 0. 6 7 1.
$$

至此,计算不能再继续.因 $x_{4}$ 与 $x_{5}$ 小数前三位数字相同,故以0.671作为根的近似值其误差小于 $10^{-3}$ .

## 习题3-8

1. 试证明方程 $x^{3} - 3x^{2} + 6x - 1 = 0$ 在区间 $(0,1)$ 内有唯一的实根，并用二分法求这个根的近似值，使误差不超过0.01.
2. 试证明方程 $x^{5} + 5x + 1 = 0$ 在区间 $(-1,0)$ 内有唯一的实根，并用切线法求这个根的近似值，使误差不超过0.01.
3. 用割线法求方程  $x^{3}+3x-1=0$  的近似根, 使误差不超过 0.01.
4. 求方程  $x \lg x = 1$  的近似根, 使误差不超过 0.01.

## 总习题三

1. 填空:

设常数 k>0，函数  $f(x)=\ln x-\frac{x}{e}+k$  在  $(0,+\infty)$  内零点的个数为 \_\_\_\_.

2. 以下两题中给出了四个结论,从中选出一个正确的结论:

（1）设在 $[0,1]$ 上 $f''(x) > 0$ ，则 $f'(0), f'(1), f(1) - f(0)$ 或 $f(0) - f(1)$ 这几个数的大小顺序为（）；

(A) $f^{\prime}(1) > f^{\prime}(0) > f(1) - f(0)$

(B) $f^{\prime}(1) > f(1) - f(0) > f^{\prime}(0)$

(C)  $f(1)-f(0)>f'(1)>f'(0)$

(D) $f^{\prime}(1) > f(0) - f(1) > f^{\prime}(0)$

(2) 设  $f'(x_{0}) = f''(x_{0}) = 0$ ,  $f'''(x_{0}) > 0$ , 则().

(A) $f'(x_0)$ 是 $f'(x)$ 的极大值

(B) $f(x_0)$ 是 $f(x)$ 的极大值

177

---

第三章 微分中值定理与导数的应用

(C) $f(x_0)$ 是 $f(x)$ 的极小值

(D) $(x_0, f(x_0))$ 是曲线 $y = f(x)$ 的拐点

3. 列举一个函数 $f(x)$ 满足: $f(x)$ 在 $[a, b]$ 上连续, 在 $(a, b)$ 内除某一点外处处可导, 但在 $(a, b)$ 内不存在点 $\xi$, 使 $f(b) - f(a) = f'(\xi)(b - a)$.

4. 设 $\lim_{x\to \infty}f'(x) = k$，求 $\lim_{x\to \infty}[f(x + a) - f(x)]$。

5. 证明多项式 $f(x) = x^3 - 3x + a$ 在[0,1]上不可能有两个零点.

6. 设  $a_{0}+\frac{a_{1}}{2}+\cdots+\frac{a_{n}}{n+1}=0$ ，证明多项式  $f(x)=a_{0}+a_{1}x+\cdots+a_{n}x^{n}$  在  $(0,1)$  内至少有一个零点.

\*7. 设 $f(x)$ 在 $[0, a]$ 上连续，在 $(0, a)$ 内可导，且 $f(a) = 0$ ，证明存在一点 $\xi \in (0, a)$，使 $f(\xi) + \xi f'(\xi) = 0$.

\*8. 设 $0 < a < b$, 函数 $f(x)$ 在 $[a, b]$ 上连续, 在 $(a, b)$ 内可导, 试利用柯西中值定理, 证明存在一点 $\xi \in (a, b)$, 使

$$
f (b) - f (a) = \xi f ^ {\prime} (\xi) \ln \frac {b}{a}.
$$

9. 设 $f(x), g(x)$ 都是可导函数，且 $|f'(x)| < g'(x)$，证明:当 $x > a$ 时，$|f(x) - f(a)| < g(x) - g(a)$.

10. 求下列极限:

(1)  $\lim_{x\to1}\frac{x-x^{x}}{1-x+\ln x};$

(2)  $\lim_{x\to0}\left[\frac{1}{\ln(1+x)}-\frac{1}{x}\right]$ ;

(3)  $\lim_{x\to+\infty}\left(\frac{2}{\pi}\arctan x\right)^x;$

(4) $\lim_{x\to\infty}\left(\frac{a_{1}^{\frac{1}{x}}+a_{2}^{\frac{1}{x}}+\cdots+a_{n}^{\frac{1}{x}}}{n}\right)^{nx}$ （其中 $a_{1},a_{2},\cdots,a_{n}>0$ ）.

11. 求下列函数在指定点 $x_0$ 处具有指定阶数及余项的泰勒公式:

(1) $f(x)=x^{3}\ln x,x_{0}=1,n=4$ ,拉格朗日余项；
(2) $f(x)=\arctan x,x_{0}=0,n=3$ ,佩亚诺余项；
(3) $f(x)=\mathrm{e}^{\sin x},x_{0}=0,n=3$ ,佩亚诺余项;
(4) $f(x)=\ln \cos x,x_{0}=0,n=6$ ,佩亚诺余项.

12. 证明下列不等式:

(1) 当  $0 < x_{1} < x_{2} < \frac{\pi}{2}$  时， $\frac{\tan x_{2}}{\tan x_{1}} > \frac{x_{2}}{x_{1}}$ ;
(2) 当 x > 0 时,  $\ln(1 + x) > \frac{\arctan x}{1 + x}$ ;
(3) 当  $e < a < b < e^{2}$  时,  $\ln^{2} b - \ln^{2} a > \frac{4}{e^{2}} (b - a)$ .

13. 设 $a > 1, f(x) = a^x - ax$ 在 $(-\infty, +\infty)$ 内的驻点为 $x(a)$. 问 $a$ 为何值时, $x(a)$ 最小? 并求出最小值.

14. 求椭圆  $x^{2}-xy+y^{2}=3$  上纵坐标最大和最小的点.

15. 椭圆 $\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1$ 内嵌入一内接矩形, 使矩形的边平行于椭圆的轴而面积最大, 求最大矩形的面积.

178

---

总习题三

16. 求数列  $\{\sqrt[n]{n}\}$  的最大项.

17. 曲线弧  $y=\sin x$  ( $0<x<\pi$ ) 上哪一点处的曲率半径最小？求出该点处的曲率半径.

18. 证明方程 $x^{3} - 5x - 2 = 0$ 只有一个正根，并求此正根的近似值，精确到 $10^{-3}$.

\* 19. 设 $f''(x_0)$ 存在, 证明: $\lim_{h\to 0}\frac{f(x_0 + h) + f(x_0 - h) - 2f(x_0)}{h^2} = f''(x_0)$.

20. 设 $f(x)$ 在 $(a, b)$ 内二阶可导，且 $f''(x) \geqslant 0$. 证明对于 $(a, b)$ 内任意两点 $x_1, x_2$ 及 $0 \leqslant t \leqslant 1$，有

$$
f \left[ (1 - t) x _ {1} + t x _ {2} \right] \leqslant (1 - t) f (x _ {1}) + t f (x _ {2}).
$$

21. 试确定常数 $a$ 和 $b$, 使 $f(x) = x - (a + b \cos x) \sin x$ 为当 $x \to 0$ 时关于 $x$ 的 5 阶无穷小.

第三章释疑解难

![](../../raw/pages_0193-0224/images/page_195_image_9.jpg)

第三章例题精讲

![](../../raw/pages_0193-0224/images/page_195_image_11.jpg)

179
