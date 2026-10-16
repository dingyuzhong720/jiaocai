# 第3章 函数极限

原始 PDF 第 52–75 页。

第三章

函数极限

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

![](../../raw/pages_0033-0064/images/page_51_chart_12.jpg)

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

41

---

第三章 函数极限

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

42

---

§ 1 函数极限概念

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

![](../../raw/pages_0033-0064/images/page_53_image_25.jpg)

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

43

---

第三章 函数极限

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

![](../../raw/pages_0033-0064/images/page_54_chart_20.jpg)

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

44

---

§ 1 函数极限概念

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

45

---

第三章 函数极限

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

46

---

§ 2 函数极限的性质

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

47

---

第三章 函数极限

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

48

---

§ 2 函数极限的性质

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

49

---

第三章 函数极限

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

50

---

§ 3 函数极限存在的条件

所以必有 $\lim_{x\to x_{0}}f(x)=A.$

![](../../raw/pages_0033-0064/images/page_61_image_2.jpg)

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

![](../../raw/pages_0033-0064/images/page_61_chart_11.jpg)

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

51

---

第三章 函数极限

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

52

---

§ 4 两个重要的极限

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

![](../../raw/pages_0033-0064/images/page_63_image_15.jpg)

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

53

---

第三章 函数极限

$$
\lim _ {x \to 0} \frac {1 - \cos x}{x ^ {2}} = \lim _ {x \to 0} \frac {1}{2} \left(\frac {\sin \frac {x}{2}}{\frac {x}{2}}\right) ^ {2} = \frac {1}{2}.
$$

## 二、证明 $\lim_{x\to \infty}\left(1 + \frac{1}{x}\right)^x = \mathrm{e}$

证 所求证的极限等价于同时成立以下两个极限:

$$
\lim _ {x \to + \infty} \left(1 + \frac {1}{x}\right) ^ {x} = \mathrm{e}, \tag {2}
$$

$$
\lim _ {x \to - \infty} \left(1 + \frac {1}{x}\right) ^ {x} = \mathrm{e}. \tag {3}
$$

先利用数列极限 $\lim_{n\to \infty}\left(1 + \frac{1}{n}\right)^n = \mathrm{e}$ 证明（2）式成立.

因为 $\lim_{n\to \infty}\left(1 + \frac{1}{n + 1}\right)^n = \lim_{n\to \infty}\left(1 + \frac{1}{n}\right)^{n + 1} = \mathrm{e}$ ，所以对任意正数 $\varepsilon$ ，存在正整数 $N$ ，当 $n\geqslant N$ 时，有

$$
\mathrm{e} - \varepsilon <   \left(1 + \frac {1}{n + 1}\right) ^ {n} <   \left(1 + \frac {1}{n}\right) ^ {n + 1} <   \mathrm{e} + \varepsilon . \tag {4}
$$

取 $X = N$ ，当 $x > X$ 时，令 $n = [x]$ ，那么

$$
\left(1 + \frac {1}{n + 1}\right) ^ {n} <   \left(1 + \frac {1}{x}\right) ^ {x} <   \left(1 + \frac {1}{n}\right) ^ {n + 1}.
$$

由(4)式有

$$
\mathrm{e} - \varepsilon <   \left(1 + \frac {1}{x}\right) ^ {x} <   \mathrm{e} + \varepsilon ,
$$

这就证明了 $\lim_{x\to +\infty}\left(1 + \frac{1}{x}\right)^x = \mathrm{e}.$

现证(3)式.为此作代换 $x = -y$ ，则

$$
\left(1 + \frac {1}{x}\right) ^ {\bar {x}} = \left(1 - \frac {1}{y}\right) ^ {- y} = \left(1 + \frac {1}{y - 1}\right) ^ {y},
$$

且当 $x \to -\infty$ 时 $y \to +\infty$，从而有

$$
\lim _ {x \to - \infty} \left(1 + \frac {1}{x}\right) ^ {x} = \lim _ {y \to + \infty} \left(1 + \frac {1}{y - 1}\right) ^ {y - 1} \cdot \left(1 + \frac {1}{y - 1}\right) = \mathrm{e}.
$$

以后还常用到 $\mathbf{e}$ 的另一种极限形式:

$$
\lim _ {\alpha \to 0} (1 + \alpha) ^ {\frac {1}{\alpha}} = \mathrm{e}. \tag {5}
$$

事实上，令 $\alpha = \frac{1}{x}$，则 $x \to \infty \Leftrightarrow \alpha \to 0$，所以

$$
\mathrm{e} = \lim _ {x \to \infty} \left(1 + \frac {1}{x}\right) ^ {x} = \lim _ {\alpha \to 0} (1 + \alpha) ^ {\frac {1}{\alpha}}.
$$

54

---

§ 4 两个重要的极限

例3 求 $\lim_{x\to 0}(1 + 2x)^{\frac{1}{x}}$

解 $\lim_{x\to 0}(1 + 2x)^{\frac{1}{x}} = \lim_{x\to 0}\left[(1 + 2x)^{\frac{1}{2x}}\cdot (1 + 2x)^{\frac{1}{2x}}\right] = \mathrm{e}^2.$

例 4 求  $\lim_{x\to0}(1-x)^{\frac{1}{x}}$ .

解 令 $u = -x$ ，则当 $x \to 0$ 时 $u \to 0$. 因此

$$
\lim _ {x \to 0} (1 - x) ^ {\frac {1}{x}} = \lim _ {u \to 0} (1 + u) ^ {- \frac {1}{u}} = \frac {1}{\mathrm{e}}.
$$

例5 求 $\lim_{n\to \infty}\left(1 + \frac{1}{n} -\frac{1}{n^2}\right)^n.$

解 $\left(1 + \frac{1}{n} -\frac{1}{n^2}\right)^n <   \left(1 + \frac{1}{n}\right)^n\to \mathrm{e}(n\to \infty)$ .另一方面，当 $n > 1$ 时有

$$
\left(1 + \frac {1}{n} - \frac {1}{n ^ {2}}\right) ^ {n} = \left(1 + \frac {n - 1}{n ^ {2}}\right) ^ {\frac {n ^ {2}}{n - 1} - \frac {n}{n - 1}} \geqslant \left(1 + \frac {n - 1}{n ^ {2}}\right) ^ {\frac {n ^ {2}}{n - 1} - 2},
$$

而由归结原则 $\left(\text{取 } x_{n}=\frac{n^{2}}{n-1},n=2,3,\cdots\right)$ ,

$$
\begin{array}{l} \lim _ {n \to \infty} \left(1 + \frac {n - 1}{n ^ {2}}\right) ^ {\frac {n ^ {2}}{n - 1} - 2} = \lim _ {n \to \infty} \left(1 + \frac {n - 1}{n ^ {2}}\right) ^ {\frac {n ^ {2}}{n - 1}} \\ = \lim _ {x \to + \infty} \left(1 + \frac {1}{x}\right) ^ {x} = \mathrm{e}. \\ \end{array}
$$

于是，由数列极限的迫敛性得

$$
\lim _ {n \to \infty} \left(1 + \frac {1}{n} - \frac {1}{n ^ {2}}\right) ^ {n} = \mathrm{e}.
$$

## 习题 3.4

1. 求下列极限:

(1)  $\lim_{x\to0}\frac{\sin2x}{x};$

(2)  $\lim_{x\to0}\frac{\sin x^{3}}{(\sin x)^{2}};$

(3)  $\lim_{x\to\frac{\pi}{2}}\frac{\cos x}{x-\frac{\pi}{2}};$

(4)  $\lim_{x\to0}\frac{\tan x}{x}$ ;

(5)  $\lim_{x\to0}\frac{\tan x-\sin x}{x^{3}}$ ;

(6)  $\lim_{x\to0}\frac{\arctan x}{x}$ ;

(7)  $\lim_{x\to+\infty}x\sin\frac{1}{x};$

(8)  $\lim_{x\to a}\frac{\sin^{2}x-\sin^{2}a}{x-a};$

(9)  $\lim_{x\to0}\frac{\sin4x}{\sqrt{x+1}-1};$

(10)  $\lim_{x\to0}\frac{\sqrt{1-\cos x^{2}}}{1-\cos x}.$

55

---

第三章 函数极限

2. 求下列极限:

(1)  $\lim_{x\to\infty}\left(1-\frac{2}{x}\right)^{-x}$ ;

(2)  $\lim_{x\to0}(1+\alpha x)^{\frac{1}{x}}$  ( $\alpha$  为给定实数);

(3)  $\lim_{x\to0}(1+\tan x)^{\cot x}$ ;

(4)  $\lim_{x\to0}\left(\frac{1+x}{1-x}\right)^{\frac{1}{x}}$ ;

(5)  $\lim_{x\to+\infty}\left(\frac{3x+2}{3x-1}\right)^{2x-1}$ ;

(6) $\lim_{x\to +\infty}\left(1 + \frac{\alpha}{x}\right)^{\beta x}(\alpha ,\beta$ 为给定实数).

3. 证明: $\lim_{x\to0}\left\{\lim_{n\to\infty}\left[\cos x\cos\frac{x}{2}\cos\frac{x}{2^2}\cdots\cos\frac{x}{2^n}\right]\right\}=1.$

4. 利用归结原则计算下列极限:

(1)  $\lim_{n\to\infty}\sqrt{n}\sin\frac{\pi}{n}$ ;

(2) $\lim_{n\to \infty}\left(1 + \frac{1}{n} +\frac{1}{n^2}\right)^n.$

## § 5 无穷小量与无穷大量

## 一、无穷小量

与无穷小数列的概念相类似,我们给出关于函数为无穷小量的定义.

定义1 设 $f$ 在某 $U^{\circ}(x_0)$ 上有定义. 若

$$
\lim _ {x \to x _ {0}} f (x) = 0,
$$

则称 f 为当  $x \rightarrow x_{0}$  时的无穷小量.

若函数 $g$ 在某 $U^{\circ}(x_0)$ 上有界，则称 $g$ 为当 $x \to x_0$ 时的有界量.

类似地，定义当 $x \to x_0^+, x \to x_0^-, x \to +\infty, x \to -\infty$ 以及 $x \to \infty$ 时的无穷小量与有界量.

例如, $x^{2}$ ,  $\sin x$  与  $1-\cos x$  都是当  $x\to0$  时的无穷小量,  $\sqrt{1-x}$  是当  $x\to1^{-}$  时的无穷小量, 而  $\frac{1}{x^{2}}$ ,  $\frac{\sin x}{x}$  为  $x\to\infty$  时的无穷小量. 又如  $\sin x$  是当  $x\to\infty$  时的有界量,  $\sin\frac{1}{x}$  是当  $x\to0$  时的有界量. 特别地, 任何无穷小量也必都是有界量.

由无穷小量的定义可立刻推得如下性质:

1. 两个(相同类型的)无穷小量之和、差、积仍为无穷小量.

2. 无穷小量与有界量的乘积为无穷小量.

例如, 当  $x \to 0$  时,  $x^{2}$  是无穷小量,  $\sin \frac{1}{x}$  为有界量, 故由性质 2 即得

$$
\lim _ {x \to 0} x ^ {2} \sin \frac {1}{x} = 0.
$$

函数  $y=x^{2}\sin\frac{1}{x}$  的图像如图 3-6 所示.

由函数极限与无穷小量的定义可立即推出如下结论:

![](../../raw/pages_0065-0096/images/page_66_image_28.jpg)

<details>
<summary>text_image</summary>

y
y=x²
-1/π
O
1/π
x
y=x²sin 1/x
y=-x²
</details>

图3-6

56

---

§ 5 无穷小量与无穷大量

$\lim_{x\to x_0}f(x) = A\Leftrightarrow f(x) - A$ 是当 $x\to x_0$ 时的无穷小量.

## 二、无穷小量阶的比较

无穷小量是以0为极限的函数,而不同的无穷小量收敛于0的速度有快有慢.为此,我们考察两个无穷小量的比,以便对它们的收敛速度作出判断.

设当 $x \to x_0$ 时, $f$ 与 $g$ 均为无穷小量.

1. 若 $\lim_{x\to x_0} \frac{f(x)}{g(x)} = 0$，则称当 $x \to x_0$ 时 $f$ 为 $g$ 的高阶无穷小量，或称 $g$ 为 $f$ 的低阶无穷小量，记作

$$
f (x) = o \left(g (x)\right) (x \to x _ {0}).
$$

特别地， $f$ 为当 $x\to x_0$ 时的无穷小量记作

$$
f (x) = o (1) (x \to x _ {0}).
$$

例如, 当  $x \to 0$  时,  $x, x^{2}, \cdots, x^{n}$  (n 为正整数) 等都是无穷小量, 因而有

$$
x ^ {k} = o (1) (x \rightarrow 0), k = 1, 2, \dots ,
$$

而且它们中后一个为前一个的高阶无穷小量,即有

$$
x ^ {k + 1} = o (x ^ {k}) (x \to 0).
$$

又如，由于 $\lim_{x\to 0}\frac{1 - \cos x}{\sin x} = \lim_{x\to 0}\tan \frac{x}{2} = 0.$ 故有

$$
1 - \cos x = o (\sin x) (x \rightarrow 0).
$$

2. 若存在正数 $K$ 和 $L$, 使得在某 $U^{\circ}(x_0)$ 上有

$$
K \leqslant \left| \frac {f (x)}{g (x)} \right| \leqslant L,
$$

则称 $f$ 与 $g$ 为当 $x \to x_0$ 时的同阶无穷小量. 特别当

$$
\lim _ {x \to x _ {0}} \frac {f (x)}{g (x)} = c \neq 0
$$

时,f与g必为同阶无穷小量.

例如, 当  $x \to 0$  时,  $1 - \cos x$  与  $x^{2}$  皆为无穷小量. 由于

$$
\lim _ {x \to 0} \frac {1 - \cos x}{x ^ {2}} = \frac {1}{2},
$$

所以 $1 - \cos x$ 与 $x^{2}$ 为当 $x\to 0$ 时的同阶无穷小量.又如，当 $x\to 0$ 时， $x$ 与 $x\left(2 + \sin \frac{1}{x}\right)$ 都是无穷小量，由于它们之比的绝对值满足

$$
1 \leqslant \left| 2 + \sin \frac {1}{x} \right| \leqslant 3,
$$

所以 $x$ 与 $x\left(2 + \sin \frac{1}{x}\right)$ 为当 $x\to 0$ 时的同阶无穷小量.

若无穷小量 $f$ 与 $g$ 满足关系式

$$
\left| \frac {f (x)}{g (x)} \right| \leqslant L, \quad x \in U ^ {\circ} (x _ {0}),
$$

57

---

第三章 函数极限

则记作

$$
f (x) = O (g (x)) (x \to x _ {0}).
$$

特别地, 若 f 在某  $U^{\circ}(x_{0})$  上有界, 则记为

$$
f (x) = O (1) (x \to x _ {0}).
$$

例如，

$$
\begin{array}{l} 1 - \cos x = O (x ^ {2}) (x \rightarrow 0), \\ x \bigg (2 + \sin \frac {1}{x} \bigg) = O (x) (x \to 0), \\ \sin x = O (1) (x \to \infty). \\ \end{array}
$$

甚至当 $f(x) = o(g(x))(x \to x_0)$ 时，也有 $f(x) = O(g(x))(x \to x_0)$.

注 本段中的等式 $f(x)=o(g(x))(x\to x_{0})$ 与 $f(x)=O(g(x))(x\to x_{0})$ 等，与通常等式的含义是不同的。这里等式左边是一个函数，右边是一个函数类，而中间的等号的含义是“属于”。例如，前面已经得到

$$
1 - \cos x = o (\sin x) (x \to 0), \tag {1}
$$

其中

$$
o (\sin x) = \left\{f \Big | \lim _ {x \to 0} \frac {f (x)}{\sin x} = 0 \right\},
$$

等式(1)表示函数  $1-\cos x$  属于此函数类.

3. 若 $\lim_{x\to x_0} \frac{f(x)}{g(x)} = 1$，则称 $f$ 与 $g$ 是当 $x \to x_0$ 时的等价无穷小量。记作

$$
f (x) \sim g (x) (x \to x _ {0}).
$$

例如，由于 $\lim_{x\to 0}\frac{\sin x}{x} = 1$ ，故有 $\sin x\sim x(x\to 0)$ .又由于 $\lim_{x\to 0}\frac{\arctan x}{x} = 1$ （上节习题1(6))，故有 $\arctan x\sim x(x\to 0)$

以上讨论了两个无穷小量阶的比较.但应指出,并不是任何两个无穷小量都可以进行这种阶的比较.例如,当 $x\to0$ 时, $x\sin\frac{1}{x}$ 和 $x^{2}$ 都是无穷小量,但它们的比

$$
\frac {x \sin \frac {1}{x}}{x ^ {2}} = \frac {1}{x} \sin \frac {1}{x} \quad \text {或} \quad \frac {x ^ {2}}{x \sin \frac {1}{x}} = \frac {x}{\sin \frac {1}{x}}
$$

当  $x \to 0$  时都不是有界量, 所以这两个无穷小量不能进行阶的比较.

下述定理显示了等价无穷小量在求极限问题中的作用.

定理 3.12 设函数 f, g, h 在  $U^{\circ}(x_{0})$  上有定义, 且有

$$
f (x) \sim g (x) (x \to x _ {0}).
$$

(i) 若  $\lim_{x\to x_{0}}f(x)h(x)=A$ ，则  $\lim_{x\to x_{0}}g(x)h(x)=A$ ;

(ii) 若  $\lim_{x\to x_{0}}\frac{h(x)}{f(x)}=B$  , 则  $\lim_{x\to x_{0}}\frac{h(x)}{g(x)}=B$ .

58

---

§ 5 无穷小量与无穷大量 |||

证 (i) $\lim_{x\to x_0}g(x)h(x) = \lim_{x\to x_0}\frac{g(x)}{f(x)}\cdot \lim_{x\to x_0}f(x)h(x) = 1\cdot A = A.$

(ii) 可类似地证明.

例 1 求  $\lim_{x\to0}\frac{\arctan x}{\sin 4x}$ .

解 由于 $\arctan x \sim x (x \to 0), \sin 4x \sim 4x (x \to 0)$. 故由定理3.12得

$$
\lim _ {x \to 0} \frac {\arctan x}{\sin 4 x} = \lim _ {x \to 0} \frac {x}{4 x} = \frac {1}{4}.
$$

例 2 利用等价无穷小量代换求极限

$$
\lim _ {x \to 0} \frac {\tan x - \sin x}{\sin x ^ {3}}.
$$

解 由于 $\tan x - \sin x = \frac{\sin x}{\cos x} (1 - \cos x)$，而

$$
\sin x \sim x (x \to 0), 1 - \cos x \sim \frac {x ^ {2}}{2} (x \to 0), \sin x ^ {3} \sim x ^ {3} (x \to 0),
$$

故有

$$
\lim _ {x \to 0} \frac {\tan x - \sin x}{\sin x ^ {3}} = \lim _ {x \to 0} \frac {1}{\cos x} \cdot \frac {x \cdot \frac {x ^ {2}}{2}}{x ^ {3}} = \frac {1}{2}.
$$

注 在利用等价无穷小量代换求极限时,应注意:只有对所求极限式中相乘或相除的因式才能用等价无穷小量来替代,而对极限式中的相加或相减部分则不能随意替代.如在例2中,若因有

$$
\tan x \sim x (x \to 0), \sin x \sim x (x \to 0),
$$

而推出

$$
\lim _ {x \to 0} \frac {\tan x - \sin x}{\sin x ^ {3}} = \lim _ {x \to 0} \frac {x - x}{\sin x ^ {3}} = 0,
$$

则得到的是错误的结果.

## 三、无穷大量

定义2 设函数 $f$ 在某 $U^{\circ}(x_0)$ 上有定义. 若对任给的 $G > 0$, 存在 $\delta > 0$, 使得当 $x \in U^{\circ}(x_0; \delta) (\subset U^{\circ}(x_0))$ 时, 有

$$
\mid f (x) \mid > G, \tag {2}
$$

则称函数 f 当  $x \rightarrow x_{0}$  时有非正常极限  $\infty$ ，记作

$$
\lim _ {x \to x _ {0}} f (x) = \infty .
$$

若(2)式换成“ $f(x)>G$ ”或“ $f(x)<-G$ ”，则分别称f当 $x\to x_{0}$ 时有非正常极限 $+\infty$ 或 $-\infty$ ，记作

$$
\lim _ {x \to x _ {0}} f (  x  ) = +   \infty \qquad {\text {或}} \qquad \lim _ {x \to x _ {0}} f (  x  ) = -   \infty  .
$$

关于函数 $f$ 在自变量 $x$ 的其他不同趋向的非正常极限的定义, 以及数列 $\{a_{n}\}$ 当 $n \to \infty$ 时的非正常极限的定义, 都可类似地给出. 例如:

59

---

第三章 函数极限

$\lim_{x\to +\infty}f(x) = -\infty$ 的定义:任给 $G > 0$ ，存在 $M > 0$ ，使得当 $x > M$ 时，有 $f(x) < -G$

$\lim_{n\to \infty}a_n = +\infty$ 的定义:任给 $G > 0$ ，存在 $N > 0$ ，使得当 $n > N$ 时，有 $a_{n} > G.$

定义3 对于自变量 $x$ 的某种趋向（或 $n\to \infty$ 时），所有以 $\infty, + \infty$ 或 $-\infty$ 为非正常极限的函数（包括数列），都称为无穷大量.

例3 证明 $\lim_{x\to 0}\frac{1}{x^2} = +\infty$

证 任给 $G > 0$ ，要使 $\frac{1}{x^2} > G$ ，只要 $|x| < \frac{1}{\sqrt{G}}$ ，因此令 $\delta = \frac{1}{\sqrt{G}}$ ，则对一切 $x \in U^\circ(0; \delta)$ ，有 $\frac{1}{x^2} > G.$ 这就证明了 $\lim_{x \to 0} \frac{1}{x^2} = +\infty.$ □

例 4 证明: 当 a > 1 时,  $\lim_{x \to +\infty} a^{x} = +\infty$ .

证 任给 G>0（不妨设 G>1），要使  $a^{x}>G$ ，由对数函数的严格增性，只要  $x>\log_{a}G$ ，因此令  $M=\log_{a}G$ ，则对一切 x>M，有  $a^{x}>G$ 。这就证得  $\lim_{x\to+\infty}a^{x}=+\infty$ 。

顺便指出,容易证明:当 a>1 时, $\lim_{x\to-\infty}a^{x}=0$ ; 当 0<a<1 时,有

$$
\lim _ {x \to + \infty} a ^ {x} = 0, \quad \lim _ {x \to - \infty} a ^ {x} = + \infty .
$$

注1 无穷大量不是很大的数,而是具有非正常极限的函数.如由例3知 $\frac{1}{x^{2}}$ 是当 $x\to0$ 时的无穷大量,由例4知 $a^{x}(a>1)$ 是当 $x\to+\infty$ 时的无穷大量.

注2 若 $f$ 为 $x \to x_0$ 时的无穷大量, 则易见 $f$ 为 $U^{\circ}(x_0)$ 上的无界函数. 但无界函数却不一定是无穷大量. 如 $f(x) = x \sin x$ 在 $U(+\infty)$ 上无界, 因对任给的 $G > 0$, 取 $x_n = 2n\pi + \frac{\pi}{2}$, 这里正整数 $n > \frac{G}{2\pi}$, 则有

$$
f (x _ {n}) = \left(2 n \pi + \frac {\pi}{2}\right) \sin \left(2 n \pi + \frac {\pi}{2}\right) = 2 n \pi + \frac {\pi}{2} > G.
$$

但  $\lim_{x\to+\infty}f(x)\neq\infty$  ，因若取数列  $x_{n}^{*}=2n\pi(n=1,2,\cdots)$  ，则  $x_{n}^{*}\to+\infty\quad(n\to\infty)$  ，而

$$
\lim _ {n \to + \infty} f (x _ {n} ^ {*}) = 0.
$$

例 5 设  $f(x)$  为  $x \to x_{0}$  时的无穷大量,  $g(x)$  在  $U(x_{0})$  上满足  $|g(x)| \geqslant K > 0$ . 证明:  $f(x)g(x)$  为  $x \to x_{0}$  时的无穷大量。

证 因为 $\lim_{x\to x_0}f(x) = \infty$ ，则对任给 $G > 0$ ，存在 $\delta >0$ ，当 $0 < |x - x_0| < \delta$ 时，有

$$
\mid f (x) \mid > \frac {G}{K}.
$$

那么

$$
\mid f (x) g (x) \mid > \frac {G}{K} \cdot K = G,
$$

这就说明 $\lim_{x\to x_0}f(x)g(x) = \infty$

□

如同对无穷小量进行阶的比较的讨论一样,对两个无穷大量也可定义高阶无穷大量、同阶无穷大量等概念.这里就不再详述了.

60

---

§ 5 无穷小量与无穷大量

由无穷大量与无穷小量的定义,可推得它们之间有如下关系:

定理3.13 (i) 设 $f$ 在 $U^{\circ}(x_0)$ 上有定义且不等于0. 若 $f$ 为 $x \to x_0$ 时的无穷小量，则 $\frac{1}{f}$ 为 $x \to x_0$ 时的无穷大量.

(ii) 若 $g$ 为 $x \to x_0$ 时的无穷大量, 则 $\frac{1}{g}$ 为 $x \to x_0$ 时的无穷小量.

定理的证明留给读者.根据这个定理,对无穷大量的研究可归结为对无穷小量的讨论.

## 四、曲线的渐近线

作为函数极限的一个应用,我们讨论曲线的渐近线问题.由平面解析几何知道,双曲线 $\frac{x^{2}}{a^{2}}-\frac{y^{2}}{b^{2}}=1$ 有两条渐近线 $\frac{x}{a}\pm\frac{y}{b}=0$ (图3-7).一般地,曲线的渐近线定义如下.

定义 4 若曲线 C 上的动点 P 沿着曲线无限地远离原点时, 点 P 与某定直线 L 的距离趋于 0, 则称直线 L 为曲线 C 的渐近线(图 3-8).

![](../../raw/pages_0065-0096/images/page_71_image_8.jpg)

<details>
<summary>text_image</summary>

y
x²/a² - y²/b²=1
O
x
</details>

图3-7

![](../../raw/pages_0065-0096/images/page_71_image_10.jpg)

<details>
<summary>text_image</summary>

y
C
P
y=f(x)
M
N
y=kx+b
α
O
L
x
</details>

图3-8

下面我们讨论曲线 $y = f(x)$ 在什么条件下存在斜渐近线 $y = kx + b$ 与垂直渐近线 $x = x_0$，以及怎样求出渐近线方程.

现假设曲线  $y=f(x)$  有斜渐近线  $y=kx+b$ . 如图 3-8 所示, 曲线上动点 P 到渐近线的距离为

$$
\mid P N \mid = \mid P M \cos \alpha \mid = \mid f (x) - (k x + b) \mid \frac {1}{\sqrt {1 + k ^ {2}}}.
$$

按渐近线的定义, 当  $x \to +\infty$  时 $^{①}$ ,  $|PN| \to 0$ , 即有

$$
\lim _ {x \to + \infty} \left[ f (x) - (k x + b) \right] = 0,
$$

或

$$
\lim _ {x \to + \infty} \left[ f (x) - k x \right] = b. \tag {3}
$$

又由

$$
\lim _ {x \to + \infty} \left[ \frac {f (x)}{x} - k \right] = \lim _ {x \to + \infty} \frac {1}{x} [ f (x) - k x ] = 0 \cdot b = 0,
$$

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 对于  $x \to -\infty$  或  $x \to \infty$  的情形,也有相应的结果.</span></small>

61

---

第三章 函数极限

得到

$$
\lim _ {x \to + \infty} \frac {f (x)}{x} = k. \tag {4}
$$

由上面的讨论可知,若曲线  $y=f(x)$  有斜渐近线  $y=kx+b$ , 则常数 k 与 b 可相继由 (4) 式和 (3) 式来确定; 反之, 若由 (4)、(3) 两式求得 k 与 b, 则可知  $|PN|\to0$  ( $x\to+\infty$ ), 从而  $y=kx+b$  为曲线  $y=f(x)$  的渐近线.

若函数 $f$ 满足

$$
\lim _ {x \to x _ {0}} f (  x  ) =   \infty \quad (\text {或} \lim _ {x \to x _ {0} ^ {+}} f (  x  ) =   \infty  , \lim _ {x \to x _ {0} ^ {-}} f (  x  ) =   \infty  ),
$$

则按渐近线的定义可知,曲线  $y=f(x)$  有垂直于 x 轴的渐近线  $x=x_{0}$ , 称为垂直渐近线.

例 6 求曲线  $f(x)=\frac{x^{3}}{x^{2}+2x-3}$  的渐近线.

解 由(4)式

$$
\frac {f (x)}{x} = \frac {x ^ {3}}{x ^ {3} + 2 x ^ {2} - 3 x} \rightarrow 1 \quad (x \rightarrow \infty),
$$

得 $k = 1$ .再由(3)式

$$
f (x) - k x = \frac {x ^ {3}}{x ^ {2} + 2 x - 3} - x \rightarrow - 2 \quad (x \rightarrow \infty),
$$

得 $b = -2$. 从而求得此曲线的斜渐近线方程为 $y = x - 2$.

又由 $f(x) = \frac{x^3}{(x + 3)(x - 1)}$ 易见

$$
\lim _ {x \to - 3} f (x) = \infty , \lim _ {x \to 1} f (x) = \infty ,
$$

所以此曲线有垂直渐近线 $x = -3$ 和 $x = 1$ （图3-9）.

![](../../raw/pages_0065-0096/images/page_72_chart_16.jpg)

<details>
<summary>contour</summary>

| Feature | Description |
| --- | --- |
| Function | f(x) = (x+3)(x-1) |
| Intersection Point | O, x=1 |
| Horizontal Line | y=x-2 |
| Vertical Line | x=-3 |
| Curve 1 | Curve starting above y=-3 and curving downward |
| Curve 2 | Curve passing through origin to x=-3 and x=1 |
</details>

图3-9

## 习题 3.5

1. 证明下列各式:

(1) $2x - x^{2} = O(x)(x\to 0)$; (2) $x\sin \sqrt{x} = O(x^{\frac{3}{2}})(x\to 0^{+})$
(3)  $\sqrt{1+x}-1=o(1)\quad(x\rightarrow0)$ ;
(4) $(1+x)^{n}=1+nx+o(x)\quad(x\rightarrow0)$  (n为正整数);

62

---

第三章总练习题

(5) $2x^{3} + x^{2} = O(x^{3})(x\longrightarrow \infty)$
(6)  $o(g(x)) \pm o(g(x)) = o(g(x)) \quad (x \to x_{0})$ ①;
(7)  $o(g_{1}(x)) \cdot o(g_{2}(x)) = o(g_{1}(x)g_{2}(x)) \quad (x \to x_{0})$ .

2. 应用定理 3.12 求下列极限:

(1)  $\lim_{x\to\infty}\frac{x\arctan\frac{1}{x}}{x-\cos x}$ ;

(2) $\lim_{x\to 0}\frac{\sqrt{1 + x^2} - 1}{1 - \cos{x}}.$

3. 证明定理 3.13.

4. 求下列函数所表示曲线的渐近线:

(1)  $y=\frac{1}{x}$ ;

(2) $y = \arctan x$;

(3)  $y=\frac{3x^{3}+4}{x^{2}-2x}.$

5. 试确定 $\alpha$ 的值, 使下列函数与 $x^{\alpha}$ 当 $x \to 0$ 时为同阶无穷小量:

(1)  $\sin 2x - 2\sin x;$

(2) $\frac{1}{1+x}-(1-x)$ ;

(3)  $\sqrt{1+\tan x}-\sqrt{1-\sin x}$ ;

(4) $\sqrt[5]{3x^2 - 4x^3}$.

6. 试确定 $\alpha$ 的值, 使下列函数与 $x^{\alpha}$ 当 $x \to \infty$ 时为同阶无穷大量:

(1)  $\sqrt{x^{2}+x^{5}}$ ;

(2)  $x + x^{2}(2 + \sin x)$ ;

(3) $(1+x)(1+x^{2})\cdots(1+x^{n})$ .

7. 证明: 若 $S$ 为无上界数集, 则存在一递增数列 $\{x_{n}\} \subset S$, 使得 $x_{n} \to +\infty (n \to \infty)$.

8. 设 $\lim_{x\to x_0}f(x) = \infty, \lim_{x\to x_0}g(x) = b\neq 0.$ 证明: $\lim_{x\to x_0}f(x)g(x) = \infty$

9. 设 $f(x) \sim g(x) (x \to x_0)$, 证明:

$f(x) - g(x) = o(f(x))$  或  $f(x) - g(x) = o(g(x))$ .

10. 写出并证明 $\lim_{x\to +\infty}f(x) = +\infty$ 的归结原则.

## 第三章总练习题

1. 求下列极限:

(1)  $\lim_{x\to3^{-}}(x-[x])$ ;

(2) $\lim_{x\to 1^{+}}([x] + 1)^{-1}$;

(3)  $\lim_{x\to+\infty}\left(\sqrt{(a+x)(b+x)}-\sqrt{(a-x)(b-x)}\right)$ ;

(4)  $\lim_{x\to+\infty}\frac{x}{\sqrt{x^{2}-a^{2}}}$ ;

(5)  $\lim_{x\to-\infty}\frac{x}{\sqrt{x^{2}-a^{2}}}$ ;

(6)  $\lim_{x\to0}\frac{\sqrt{1+x}-\sqrt{1-x}}{\sqrt[3]{1+x}-\sqrt[3]{1-x}}$ ;

(7) $\lim_{x\to 1}\left(\frac{m}{1 - x^m} -\frac{n}{1 - x^n}\right),m,n$ 为正整数.

2. 分别求出满足下述条件的常数 $a$ 与 $b$:

(1)  $\lim_{x\to+\infty}\left(\frac{x^{2}+1}{x+1}-ax-b\right)=0;$

(2) $\lim_{x\to -\infty}(\sqrt{x^2 - x + 1} -ax - b) = 0;$

① 这里等式的含义是:两个比 g 高阶的无穷小量的和或差仍是一个比 g 高阶的无穷小量.后一小题类似.

63

---

第三章 函数极限

(3)  $\lim_{x\to+\infty}\left(\sqrt{x^{2}-x+1}-ax-b\right)=0.$

3. 试分别举出符合下列要求的函数 $f$:

(1)  $\lim_{x\to2}f(x)\neq f(2)$ ; (2)  $\lim_{x\to2}f(x)$  不存在.

4. 试给出函数 $f$ 的例子，使 $f(x) > 0$ 恒成立，而在某一点 $x_0$ 处有 $\lim_{x\to x_0}f(x) = 0.$ 这同极限的局部保号性有矛盾吗？

5. 设 $\lim_{x\to a}f(x) = A, \lim_{u\to A}g(u) = B$，在何种条件下能由此推出

$$
\lim _ {x \to a} g (f (x)) = B?
$$

6. 设 $f(x) = x \cos x$. 试作数列

(1)  $\{x_{n}\}$  使得  $x_{n}\to\infty\quad(n\to\infty)$ ， $f(x_{n})\to0\quad(n\to\infty)$ ;
(2)  $\{y_{n}\}$  使得  $y_{n} \rightarrow \infty \quad (n \rightarrow \infty)$ ， $f(y_{n}) \rightarrow +\infty \quad (n \rightarrow \infty)$ ;
(3) $\{z_{n}\}$ 使得 $z_{n} \to \infty (n \to \infty)$, $f(z_{n}) \to -\infty (n \to \infty)$.

7. 证明: 若数列  $\{a_{n}\}$  满足下列条件之一, 则  $\{a_{n}\}$  是无穷大数列:

(1)  $\lim_{n\to\infty}\sqrt[n]{|a_{n}|}=r>1;$
(2)  $\lim_{n\to\infty}\left|\frac{a_{n+1}}{a_n}\right|=s>1\quad(a_n\neq0,n=1,2,\cdots).$

8. 利用上题(1)的结论求极限:

(1) $\lim_{n\to \infty}\left(1 + \frac{1}{n}\right)^{n^2}$; (2) $\lim_{n\to \infty}\left(1 - \frac{1}{n}\right)^{n^2}$.

9. 设 $\lim_{n\to \infty}a_n = +\infty$ ，证明

(1)  $\lim_{n\to\infty}\frac{1}{n}(a_{1}+a_{2}+\cdots+a_{n})=+\infty$ ;
(2) 若  $a_{n}>0(n=1,2,\cdots)$ ，则  $\lim_{n\to\infty}\sqrt[n]{a_{1}a_{2}\cdots a_{n}}=+\infty$ .

10. 利用上题结果求极限:

(1)  $\lim_{n\to\infty}\sqrt[n]{n!}$ ; (2)  $\lim_{n\to\infty}\frac{\ln(n!)}{n}$ .

11. 设 $f$ 为 $U_{-}^{\circ}(x_0)$ 上的递增函数. 证明: 若存在数列 $\{x_n\} \subset U_{-}^{\circ}(x_0)$ 且 $x_{n} \to x_{0}(n \to \infty)$, 使得 $\lim_{n \to \infty} f(x_{n}) = A$, 则有

$$
f (x _ {0} - 0) = \sup _ {x \in U _ {-} ^ {\circ} (x _ {0})} f (x) = A.
$$

12. 设函数 $f$ 在 $(0, +\infty)$ 上满足方程 $f(2x) = f(x)$，且 $\lim_{x \to +\infty} f(x) = A$。证明:$f(x) \equiv A, x \in (0, +\infty)$.

13. 设函数 $f$ 在 $(0, +\infty)$ 上满足方程 $f(x^{2}) = f(x)$，且

$$
\lim _ {x \to 0 ^ {+}} f (x) = \lim _ {x \to + \infty} f (x) = f (1).
$$

证明: $f(x)\equiv f(1),x\in (0, + \infty)$

14. 设函数 $f$ 定义在 $(a, +\infty)$ 上，$f$ 在每一个有限区间 $(a, b)$ 上有界，并满足 $\lim_{x \to +\infty} (f(x + 1) - f(x)) = A.$ 证明

$$
\lim _ {x \to + \infty} \frac {f (x)}{x} = A.
$$

![](../../raw/pages_0065-0096/images/page_74_image_32.jpg)

## 第三章综合自测题

64
