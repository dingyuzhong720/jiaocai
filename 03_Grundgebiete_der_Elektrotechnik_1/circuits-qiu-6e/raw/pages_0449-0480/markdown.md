![](images/page_448_image_2.jpg)

<details>
<summary>text_image</summary>

i₀
R
iₛ(t)
+
Us
-
i'
u
-
</details>

(a)

![](images/page_448_image_4.jpg)

<details>
<summary>text_image</summary>

i₁
G
iₛ(t)
Gₐ
+
u₁
-
</details>

(b)

图17-13 例17-4图

解 对于图 17-13(a)，应用 KCL 和 KVL 有

$$
i = i _ {0} + i _ {\mathrm{s}}
$$

$$
u = U _ {\mathrm{s}} - R i _ {0}
$$

整理后即得

$$
\frac {u}{R} + g (u) = 6 + 0. 5 \cos \omega t
$$

(1) 先求电路的静态工作点, 令  $i_{\mathrm{S}}(t)=0$ , 则

$$
u ^ {2} + u - 6 = 0
$$

解得 u=2 和 u=-3，而 u=-3 不符合题意，故可得静态工作点  $U_{Q}=2\ V, I_{Q}=U_{Q}^{2}=4\ A$ 。

(2) 求解非线性电路的动态电导, 静态工作点处的动态电导为

$$
G _ {\mathrm{d}} = \frac {\mathrm{d} g (u)}{\mathrm{d} u} \Bigg | _ {U _ {\mathrm{Q}}} = 2 u \Bigg | _ {U _ {\mathrm{Q}}} = 4 \mathrm{S}
$$

（3）作出给定非线性电导在静态工作点处的小信号等效电路如图 17-13(b) 所示，则有

$$
u _ {1} (t) = \frac {i _ {\mathrm{S}}}{G + G _ {\mathrm{d}}} = \frac {0 . 5 \cos \omega t}{1 + 4} \mathrm{V} = 0. 1 \cos \omega t \mathrm{V}
$$

$$
i _ {1} (t) = u _ {1} (t) \times G _ {\mathrm{d}} = 4 \times 0. 1 \cos \omega t \mathrm{A} = 0. 4 \cos \omega t \mathrm{A}
$$

故得图 17-13(a) 中

$$
u (t) = U _ {\mathrm{Q}} + u _ {1} (t) = (2 + 0. 1 \cos \omega t) \mathrm{V}
$$

$$
i (t) = I _ {\mathrm{Q}} + i _ {1} (t) = (4 + 0. 4 \cos \omega t) \mathrm{A}
$$

## §17-5 分段线性化方法

分段线性化方法(又称折线法)是研究非线性电路的一种有效方法,它的特点在于能把非线性的求解过程分成几个线性区段,就每个线性区段来说,又可以应用线性电路的计算方法。

应用分段线性化方法时,为了画出一端口网络的驱动点特性曲线,常引用理想二极管模型。它的特点是,在电压为正向时,二极管完全导通,它相当于短路;在电压反向时，二极管不导通，电流为零，它相当于开路，其伏安特性如图17-14所示。一个实际二极管的模型可由理想二极管和线性电阻串联组成，其伏安特性可用图17-15的折线$\overline{BOA}$近似地逼近，当这个二极管加上正向电压时，它相当于一个线性电阻，其伏安特性用直线 $\overline{OA}$ 表示；当电压反向时，二极管完全不导通，其伏安特性用直线 $\overline{BO}$ 表示。

![](images/page_449_image_4.jpg)

<details>
<summary>text_image</summary>

i
A
B
O
u
</details>

图17-14 理想二极管伏安特性

![](images/page_449_chart_6.jpg)

<details>
<summary>line</summary>

| u | i |
| --- | --- |
| 0 | 0 |
| ~0.2 | ~0.1 |
| ~0.4 | ~0.3 |
| ~0.6 | ~0.5 |
| ~0.8 | ~0.7 |
| ~1.0 | ~0.9 |
</details>

图 17-15 PN 结二极管伏安特性

例 17-5 （1）图 17-16(a) 所示电路由线性电阻 R、理想二极管和直流电压源串联组成。电阻 R 的伏安特性如图 17-16(b) 所示，画出此串联电路的伏安特性。（2）把图 17-16(a) 中的电阻 R 和二极管与直流电流源并联，如图 17-16(d) 所示，画出此并联电路的伏安特性。

![](images/page_449_image_9.jpg)

<details>
<summary>text_image</summary>

i
+
R
u
+
uD
-
+
U0
-
-
</details>

(a)

![](images/page_449_chart_11.jpg)

<details>
<summary>line</summary>

| u | i |
| --- | --- |
| 0 | 0 |
| U0 | 1 |
</details>

(b)

![](images/page_449_image_13.jpg)

<details>
<summary>text_image</summary>

i
A
G=1/R
1
C
O
B
U₀
u
</details>

(c)

![](images/page_449_image_15.jpg)

<details>
<summary>text_image</summary>

i
+
u
R
I₀
-
</details>

(d)

![](images/page_449_image_17.jpg)

<details>
<summary>text_image</summary>

i
A
1/R
1
G=1/R
I₀
B
O
u
二极管
C
</details>

(e)

图17-16 例17-5图

解 （1）各元件的伏安特性如图 17-16(b) 所示, 电路方程为

$$
u = R i + u _ {\mathrm{D}} + U _ {0} \quad (i > 0)
$$

串联电路的伏安特性可用图解法求得,如图 17-16(c) 的折线  $\overline{ABC}$  (当  $u<U_{0}$  时, i=0) 所示。

(2) 电路方程为

$$
i = \frac {u}{R} + I _ {0} \quad (u > 0)
$$

当 u<0 时，二极管完全导通，电路被短路。当 u>0 时，用图解法求得的伏安特性如图 17-16(e) 中的折线  $\overline{ABO}$  所示。

图 17-17(a) 中的虚线为隧道二极管的伏安特性, 此特性可用图示的三段直线来粗略地表示。假设这三段直线的斜率分别为

当 $u \leqslant U_{1}$ （区域1），$G = G_{\mathrm{a}}$

当 $U_{1} < u \leqslant U_{2}$ （区域2）， $G = G_{\mathrm{b}}$

当 $u > U_{2}$ （区域3）， $G = G_{\mathrm{c}}$

其中 $U_{1}, U_{2}$ 确定了这三个区域，而 $U_{1}$ 和 $U_{2}$ 为转折点的电压值。图17-17(a)所示的伏安特性可以分解为三个伏安特性，即图17-17(b)中的直线 $\overline{AOB}$、折线 $\overline{EU_1C}$ 和 $\overline{EU_2D}$，并设图17-17(b)中有关直线段的斜率分别为 $G_{1}, G_{2}$ 和 $G_{3}$，根据非线性电阻（或电导）并联的图解法原则，就可以确定 $G_{1}, G_{2}$ 和 $G_{3}$。

![](images/page_450_image_14.jpg)

图 17-17 分段线性化特性的合成

在区域1应当有

$$
G _ {1} u = G _ {\mathrm{a}} u \quad \text {或} \quad G _ {1} = G _ {\mathrm{a}}
$$

在区域2有

$$
G _ {1} u + G _ {2} u = G _ {\mathrm{b}} u \quad \text {或} \quad G _ {1} + G _ {2} = G _ {\mathrm{b}}
$$

同理,在区域3有

$$
G _ {1} u + G _ {2} u + G _ {3} u = G _ {\mathrm{c}} u \quad \text {或} \quad G _ {1} + G _ {2} + G _ {3} = G _ {\mathrm{c}}
$$

因此,可得

$$
G _ {1} = G _ {\mathrm{a}}, \quad G _ {2} = G _ {\mathrm{b}} - G _ {\mathrm{a}}, \quad G _ {3} = G _ {\mathrm{c}} - G _ {\mathrm{b}}
$$

而图17-17(a)所示的伏安特性则是 $G_{1}, G_{2}$ 和 $G_{3}$ 这三个电导并联后的等效电导的伏安特性。其静态工作点也可以用图解法来确定。不过应当注意，如果静态工作点位于图17-18(a)所示的位置，表示该点确实是工作点，如果负载线与分段线性的伏安特性曲线交点位于图17-18(b)所示位置，则只有 $Q_{3}$ 为实际的工作点，而 $Q_{1}, Q_{2}$ 并不代表实际的工作点，因为其交点并不位于对应的区段。

![](images/page_451_chart_7.jpg)

<details>
<summary>line</summary>

| Point | u | i |
| --- | --- | --- |
| A | 0 | \(U_{0}/R_{0}\) |
| C | \(U_{1}\) | \(Q_{1}\) |
| D | \(U_{2}\) | \(Q_{3}\) |
</details>

(a)

![](images/page_451_chart_9.jpg)

<details>
<summary>line</summary>

| Point | u | i |
| --- | --- | --- |
| E | 0 | 0 |
| E | U0 | 0 |
| E | U0 | A |
| Q3 | U1 | A |
| Q3 | U2 | D |
| C | U1 | A |
| C | U1 | B |
</details>

(b)

图 17-18 隧道二极管的静态工作点

图 17-19(a) 所示电路是一个分段线性 RC 电路, 其中虚线框部分为一端口 N, 它的驱动点特性如图 17-19(b) 所示, 在端口处电压电流关系为

$$
\frac {\mathrm{d} u}{\mathrm{d} t} = \frac {\mathrm{d} u _ {c}}{\mathrm{d} t} = - \frac {i}{C} \tag {17-7}
$$

设方程的解用 u-i 平面上的点  $(u,i)$  表示，并称之为动态点，动态点  $(u,i)$  随时间将沿着 N 的驱动点特性（端口伏安特性）移动，移动的方向由上式确定。动态点移动的路径（包括方向）称为动态路径。所以由式(17-7)可以看出，在任何时刻 t，当 i<0 时有  $\frac{du}{dt}>0$ ，因此，在 u-i 平面的下半平面，动态点应当从初始位置沿着动态路径向右移动。当 i>0 时有  $\frac{du}{dt}<0$ ，因此，在 u-i 平面的上半平面，动态点应当沿着动态路径向左移动，如图 17-19(b) 中箭头所示。

假设动态点 $(u, i)$ 的初始位置位于 $Q_{2}$, 随着时间的增长, 动态点应当向 $A$ 点移动, 但到达 $A$ 点后它不能再沿着 $\overline{AB}$ 线段继续移动, 因为方向不对。同样, 如果初始位置位于 $Q_{1}$, 则动态点到达 $A$ 点后也不能再继续前进, 对于转折点 $C$ 也有同样的情况, 因为表示动态路径方向的两个箭头都是指向 $C$ 点的。由于对应 $A$ 点和 $C$ 点的电流值均为非零值, 因此 $A$ 点和 $C$ 点均不对应最终的平衡点或稳态, 这是因为 $\frac{\mathrm{d}u}{\mathrm{d}t}$ 在此时不等于零。

![](images/page_452_image_3.jpg)

<details>
<summary>text_image</summary>

i
1
+
uc
+
-
C
u
-
1'
Rf
-
∞
+
Ra
Rb
N
</details>

(a)

![](images/page_452_image_5.jpg)

<details>
<summary>text_image</summary>

i
Q_C
C
Q_3
O
Q_2
u
Q_1
B
A
Q_A
D
Q_4
</details>

(b)

图 17-19 分段线性 RC 电路

为了解决这个问题,必须计及电路中存在的微小的串联电感,并按二阶电路分析。在这种情况下,动态路径将如图17-20(a)所示,图中假设 $P_{0}$ 表示动态点的初始点。当动态点到达 $P_{1}$ (对应转折点A)后,由于电感电流不能跃变,它将从 $P_{1}$ 前进到 $P_{2}$,当动态点到达 $P_{3}$ (对应转折点C)后,它将从 $P_{3}$ 前进到 $P_{4}$,如图17-20(a)中箭头所示。从 $P_{1}$ 前进到 $P_{2}$(或从 $P_{3}$ 前进到 $P_{4}$)所需时间随电感L值的减小而减小,当电感L的值趋近于零时,可以认为动态点从 $P_{1}$ 前进到 $P_{2}$(或从 $P_{3}$ 前进到 $P_{4}$)所需时间也趋近于零,或者说,动态点将瞬时从 $P_{1}(P_{3})$ “跳跃”到 $P_{2}(P_{4})$,此时,电路中发生跃变的是电流值。这个电路的动态路径将如图17-20(b)中箭头所示。这里除了从初始点 $P_{0}$ 到 $P_{1}$ 这个过渡过程阶段,动态路径是闭合的,这说明电路中的电压或电流从初始状态开始经短暂时间后,就将周期性变化。这个电路能产生周期性变化的电压和电流,所以它具有振荡器的作用。这种振荡称为张弛振荡,因为产生的电压或电流波形与正弦波相差甚大。振荡周期等于从 $P_{2}$ 到 $P_{3}$ 的时间和从 $P_{4}$ 到 $P_{1}$ 的时间之和。

![](images/page_452_image_9.jpg)

<details>
<summary>text_image</summary>

i
P₂
P₃ C
O P₀ u
A P₁
P₄
</details>

(a)

![](images/page_452_image_11.jpg)

<details>
<summary>text_image</summary>

i
I_{P2}
P_2
P_3
I_{P3}
C
-U_S
-U_1
U_0
U_1
U_S
u
O
I_0
A
I_{P1}
P_1
P_4
I_{P4}
</details>

(b)

图 17-20 动态路径和跳跃现象

## \*§17-6 工作在非线性范围的运算放大器

本书在前面章节中把运放的工作范围局限在线性区域,即认为输出电压  $u_{0}$  与  $u_{d}$  成正比,而且

$$
- U _ {\mathrm{sat}} <   u _ {\mathrm{o}} <   U _ {\mathrm{sat}}
$$

$\pm U_{sat}$  为运放输出电压的饱和值。

设运放的放大倍数 A 为无限大, 并考虑到输出电压达到饱和值, 则运放的输出电压  $\bar{u}_{0}$  与差分电压  $u_{d}$  之间的关系可用图 17-21 所示特性曲线来表示。这时可用以下表达式描述运放的工作:

$$
i ^ {-} = 0, \quad i ^ {+} = 0
$$

$$
u _ {\mathrm{o}} = U _ {\mathrm{sat}} \frac {| u _ {\mathrm{d}} |}{u _ {\mathrm{d}}}, \quad u _ {\mathrm{d}} \neq 0
$$

$$
u _ {\mathrm{d}} = 0, \quad - U _ {\mathrm{sat}} <   u _ {\mathrm{o}} <   U _ {\mathrm{sat}}
$$

这里把电压的关系分为 3 个区域来考虑:

线性区  $u_{d}=0,\quad-U_{sat}<u_{o}<U_{sat}$

正饱和区  $u_{o}=U_{sat},\quad u_{d}=(u^{+}-u^{-})>0$

负饱和区  $u_{o} = -U_{sat}, \quad u_{d} = (u^{+} - u^{-}) < 0$

![](images/page_453_image_15.jpg)

<details>
<summary>text_image</summary>

u⁻○ → i⁻ → - ∞
          u_d
          +
          +
          i⁺
          u⁺○ → i⁻ → + → u_o
          U_sat
          O
          u_d
          -U_sat
</details>

图 17-21 理想运放的饱和  $u_{d}-u_{0}$  特性

注意，在正、负饱和区， $u_{d}$  不再等于零，但  $u_{0}$  是定值。而在线性区  $u_{d}$  被强制为零，但  $u_{0}$  不是定值，它的大小取决于外电路。当运放在正饱和区和负饱和区工作时，它是在非线性区工作。

图 17-22 所示电路是一个实现分段线性电阻的电路, 其中运放通过  $R_{f}$  实现负反馈, 通过  $R_{a}$  和  $R_{b}$  实现正反馈。如果计及运放工作在饱和区的情况, 这个电路的输入电阻在一定范围内具有负电阻的性质。现分析这个电路的驱动点特性。

![](images/page_454_image_3.jpg)

<details>
<summary>text_image</summary>

i
Rf
+
-
u_d
+
-
u
u_2
Ra
Rb
uo
-
</details>

(a)

![](images/page_454_image_5.jpg)

<details>
<summary>text_image</summary>

i
D
负饱和
C
-αUsat
O
αUsat
u
A
正饱和
B
</details>

(b)

图 17-22 负电阻的实现

在线性区,对于图 17-22(a),根据“虚短”,有  $u=u_{2}$ ,根据“虚断”,流过  $R_{a}$  中的电流等于流过  $R_{b}$  中的电流,因此可以得出

$$
u _ {2} = \frac {R _ {\mathrm{b}}}{R _ {\mathrm{a}} + R _ {\mathrm{b}}} u _ {\mathrm{o}} = \alpha u _ {\mathrm{o}}
$$

其中  $\alpha=\frac{R_{b}}{R_{a}+R_{b}}$ ，而  $u_{o}=\frac{1}{\alpha}u_{o}$

应用 KVL, 有

$$
u = R _ {\mathrm{f}} i + u _ {\mathrm{o}}
$$

把 $u_{\mathrm{o}} = \frac{u}{\alpha}$ 代入，则得

$$
i = - \left(\frac {R _ {\mathrm{a}}}{R _ {\mathrm{b}}}\right) \left(\frac {1}{R _ {\mathrm{f}}}\right) u
$$

上式可以用图 17-22(b) 的直线段 AOC 表示。对应此线段的两个端点 A 和 C 的电压值可以求得如下。

在线性区,由于  $u_{0}=\frac{1}{\alpha}u$ , 故

$$
- \alpha U _ {\mathrm{sat}} <   u <   \alpha U _ {\mathrm{sat}}
$$

直线段  $\overline{AOC}$  的斜率是负的,且正比于  $-\frac{R_{a}}{R_{b}}\cdot\frac{1}{R_{f}}$ 。

在正饱和区, $u_{o}=U_{sat}$ ,应用KVL,有

$$
u = R _ {\mathrm{f}} i + U _ {\mathrm{sat}}
$$

$$
i = \frac {1}{R _ {\mathrm{f}}} (u - U _ {\mathrm{sat}}) \tag {17-8}
$$

为了确定电压 u 的范围,应用 KVL,得

$$
u _ {\mathrm{d}} = u _ {2} - u = \frac {R _ {\mathrm{b}}}{R _ {\mathrm{a}} + R _ {\mathrm{b}}} U _ {\mathrm{sut}} - u
$$

$$
u _ {\mathrm{d}} = \alpha U _ {\mathrm{sat}} - u
$$

由于 $u_{\mathrm{d}} > 0$ ，故 $u < \alpha U_{\mathrm{sat}}$ 。这与式(17-8)确定了图17-22(b)中的直线段 $\overline{AB}$ ，它表示在正饱和区的伏安特性，其斜率正比于 $\frac{1}{R_{\mathrm{f}}}$ 。

在负饱和区, $u_{0}=-U_{sat}$ ,有

$$
u = R _ {\mathrm{f}} i - U _ {\mathrm{sat}}
$$

由于  $u_{d}<0$ ，故  $u>-\alpha U_{sat}$ 。图 17-22(b) 中的直线段 CD 表示在负饱和区的伏安特性，其斜率正比于  $\frac{1}{R_{f}}$ 。

所以这个电路可以实现一个折线或分段线性电阻,此电阻在运放线性工作范围内具有负电阻性质,其值等于 $-\frac{R_{b}R_{f}}{R_{a}}$ 。

## \* §17-7 小扰动下的动态电路分析

非线性动态电路在直流源激励工作时，由于各种原因会受到外界的突然干扰，从而导致非线性动态电路的工作状态突然发生变化。例如含非线性动态元件的精密测量及精确控制电路受到雷电的突然影响，外界电磁脉冲的突然干扰，工作电源的突然波动等。外界的扰动可能是暂时的，其幅值可能是很小的，但这种由小扰动引起的暂态响应对测量及控制效果的影响是值得注意的，其暂态响应的分析对评价精密测量及精确控制的电路性能也是有用的。基于非线性电路的局部线性化思想，对于小扰动引起的非线性动态电路的暂态响应应用小信号分析法进行求解也是行之有效的。

例17-6 含有非线性电感的一阶动态电路如图17-23(a)所示，已知直流电压源$U_{\mathrm{s}} = 30~\mathrm{V}$，小扰动电压源 $u_{\mathrm{s}}(t) = 1.5\mathrm{e}^{-10t}\varepsilon (t)\mathrm{V}$，线性电阻 $R_{1} = 6\Omega ,R_{2} = 40\Omega ,R_{3} = 60\Omega$ 非线性电感 $\psi = 0.5i^3 (\psi$ 单位为Wb，i单位为A）。求 $t > 0$ 时的响应 $i_L(t),i_3(t),u_3(t)$。

解 （1）由题意可知,当直流电压源单独作用于电路时,根据等效电路图 17-23(b)求得

$$
R = R _ {1} + \frac {R _ {2} R _ {3}}{R _ {2} + R _ {3}} = (6 + 2 4) \Omega = 3 0 \Omega , \quad I _ {L 0} = \frac {U _ {\mathrm{s}}}{R} = \frac {3 0}{3 0} \mathrm{A} = 1 \mathrm{A}
$$

$$
I _ {3 0} = I _ {L 0} \times \frac {R _ {2}}{R _ {2} + R _ {3}} = \left(1 \times \frac {4 0}{1 0 0}\right) \mathrm{A} = 0. 4 \mathrm{A}, \quad U _ {3 0} = R _ {3} \times I _ {3 0} = (6 0 \times 0. 4) \mathrm{V} = 2 4 \mathrm{V}
$$

![](images/page_456_image_3.jpg)

<details>
<summary>text_image</summary>

uS(t)
+
-
R1
ψ
iL
i3
+
Us
-
R2
R3
+
u3
-
</details>

(a)

![](images/page_456_image_5.jpg)

<details>
<summary>text_image</summary>

+
Us
-
R1
IL0
I30
R2
R3
+
U30
-
</details>

(b)

![](images/page_456_image_7.jpg)

<details>
<summary>text_image</summary>

R₁
Lₐ
iₗΔ
i₃Δ
uₛ(t)
+
-
R₂
R₃
u₃Δ
-
</details>

(c)

图17-23 例17-6图

(2) 电路的动态电感为

$$
L _ {\mathrm{d}} = \frac {\mathrm{d} \psi}{\mathrm{d} i} \Bigg | _ {i _ {L} = I _ {L 0}} = 3 \times 0. 5 \times I _ {L 0} ^ {2} = 1. 5 \mathrm{H}
$$

（3）根据动态电感值建立的小参数一阶线性动态电路如图17-23(c)所示，且电路处于零状态，求小扰动电压源激励时的零状态响应 $i_{L\Delta}(t)$ 。其一阶电路的微分方程为

$$
L _ {\mathrm{d}} \frac {\mathrm{d} i _ {L \Delta}}{\mathrm{d} t} + R i _ {L \Delta} = u _ {\mathrm{S}} (t)
$$

代入参数得

$$
\frac {\mathrm{d} i _ {L \Delta}}{\mathrm{d} t} + 2 0 i _ {L \Delta} = \mathrm{e} ^ {- 1 0 t}
$$

(对于规范的一阶线性微分方程 $\frac{dy}{dt}+py=x(t)$ ，其解用积分表示，则有 $y(t)=\mathrm{e}^{-\int p\mathrm{d}t}\left[\int x(t)\mathrm{e}^{\int p\mathrm{d}t}\mathrm{d}t+A\right]$ ，式中A是取决于初始条件的积分常数。)

因此,对于电感电流进行积分可得

$$
\begin{array}{l} i _ {L \Delta} (  t  ) = \mathrm{e} ^ {- \int 2 0 \mathrm{d} t}   \left[   \int \mathrm{e} ^ {- 1 0 t} \mathrm{e} ^ {\int 2 0 \mathrm{d} t}   \mathrm{d} t + A   \right] \\ = \mathrm{e} ^ {- \int 2 0 \mathrm{d} t} \left[ \int \mathrm{e} ^ {- 1 0 t} \mathrm{e} ^ {2 0 t} \mathrm{d} t + A \right] \\ = 0. 1 \mathrm{e} ^ {- 1 0 t} + A \mathrm{e} ^ {- 2 0 t} \\ \end{array}
$$

当 $t = 0_{+}$ 时，$i_{L\Delta}(0_{+}) = i_{L\Delta}(0_{-}) = 0$ ，故 $A = -0.1$ ，因此小扰动电压源激励时的零状态响应为

$$
\begin{array}{l} i _ {L \Delta} (  t) = \left(0. 1 \mathrm{e} ^ {- 1 0 t} - 0. 1 \mathrm{e} ^ {- 2 0 t}\right) \varepsilon (  t)   \mathrm{A} \\ i _ {3 \Delta} (t) = \frac {i _ {L \Delta} \times R _ {2}}{R _ {2} + R _ {3}} \\ = (0. 0 4 \mathrm{e} ^ {- 1 0 t} - 0. 0 4 \mathrm{e} ^ {- 2 0 t}) \varepsilon (t) \mathrm{A} \\ \end{array}
$$

$$
\begin{array}{l} u _ {3 \Delta} (t) = R _ {3} i _ {3 \Delta} \\ = (2. 4 \mathrm{e} ^ {- 1 0 t} - 2. 4 \mathrm{e} ^ {- 2 0 t}) \varepsilon (t) \mathrm{V} \\ \end{array}
$$

因此图 17-23(a) 所示电路的总响应为

$$
\begin{array}{l} i _ {L} (t) = I _ {L 0} + i _ {L \Delta} \\ = \left[ 1 + (0. 1 \mathrm{e} ^ {- 1 0 t} - 0. 1 \mathrm{e} ^ {- 2 0 t}) \varepsilon (t) \right] \mathrm{A} \\ i _ {3} (t) = I _ {3 0} + i _ {3 \Delta} \\ = \left[ 0. 4 + (0. 0 4 \mathrm{e} ^ {- 1 0 t} - 0. 0 4 \mathrm{e} ^ {- 2 0 t}) \varepsilon (t) \right] \mathrm{A} \\ u _ {3} (t) = U _ {3 0} + u _ {3 \Delta} \\ = \left[ 2 4 + (2. 4 \mathrm{e} ^ {- 1 0 t} - 2. 4 \mathrm{e} ^ {- 2 0 t}) \varepsilon (t) \right] \mathrm{V} \\ \end{array}
$$

$$
\begin{array}{l} i _ {3} (t) = I _ {3 0} + i _ {3 \Delta} \\ = \left[ 0. 4 + (0. 0 4 \mathrm{e} ^ {- 1 0 t} - 0. 0 4 \mathrm{e} ^ {- 2 0 t}) \varepsilon (t) \right] \mathrm{A} \\ \end{array}
$$

$$
\begin{array}{l} u _ {3} (t) = U _ {3 0} + u _ {3 \Delta} \\ = \left[ 2 4 + (2. 4 \mathrm{e} ^ {- 1 0 t} - 2. 4 \mathrm{e} ^ {- 2 0 t}) \varepsilon (t) \right] \mathrm{V} \\ \end{array}
$$

例 17-7 含有非线性电感和电容的二阶动态电路如图 17-24(a) 所示, 已知直流电压源 $U_{\mathrm{S}} = 2.25 \mathrm{~V}$, 小扰动电压源 $u_{\mathrm{S}}(t) = [0.45 \times 10^{-2} \varepsilon(t) - 0.45 \times 10^{-2} \varepsilon(t-1)] \mathrm{~V}$, 线性电阻 $R_{1} = 1 \Omega, R_{2} = 1.25 \Omega$, 非线性电感 $\psi = 0.1 i_{L} + 0.05 i_{L}^{3} (\psi$ 单位为 $\mathrm{Wb}, i_{L}$ 单位为 A), 非线性电容 $q = 0.8 u_{C}^{2} (q$ 单位为 C, $u_{C}$ 单位为 V)。求 $t > 0$ 时的响应 $i_{L}(t)$。

![](images/page_457_image_9.jpg)

<details>
<summary>text_image</summary>

uS(t)
+
-
Us
+
-
R1
ψ
iL
q
uC
+
-
R2
+
uR2
(a)
</details>

![](images/page_457_image_10.jpg)

<details>
<summary>text_image</summary>

+
Us
-
R1
+
UC0
-
IL0
R2
(b)
</details>

![](images/page_457_image_11.jpg)

<details>
<summary>text_image</summary>

+
us
-
i
R1
Ld
ILΔ
+
Cd
uCΔ
-
R2
(c)
</details>

图17-24 例17-7图

解 （1）当直流电压源单独作用于电路时，在稳定状态下，电感处于短路，电容处于开路，其等效电路如图 17-24(b) 所示，故得

$$
I _ {L 0} = \frac {U _ {\mathrm{s}}}{R _ {1} + R _ {2}} = \frac {2 . 2 5}{2 . 2 5} \mathrm{A} = 1 \mathrm{A}, \quad U _ {c 0} = R _ {2} \times I _ {L 0} = (1. 2 5 \times 1) \mathrm{V} = 1. 2 5 \mathrm{V}
$$

(2) 电路的动态电感为

$$
L _ {\mathrm{d}} = \frac {\mathrm{d} \psi}{\mathrm{d} i _ {L}} \Bigg | _ {i _ {L} = I _ {L 0}} = 0. 1 + 3 \times 0. 0 5 \times I _ {L 0} ^ {2} = 0. 2 5 \mathrm{H}
$$

电路的动态电容为

$$
C _ {\mathrm{d}} = \frac {\mathrm{d} q}{\mathrm{d} u _ {c}} \Bigg | _ {u _ {c} = U _ {c 0}} = 2 \times 0. 8 \times U _ {c 0} = 2 \mathrm{F}
$$

(3) 根据动态电感值和动态电容值建立的小参数二阶线性动态电路如图 17-24 (c) 所示, 且电路处于零状态, 求小扰动电压源激励时的零状态响应  $i_{L\Delta}(t)$ 。根据支路电流法, 得

$$
\begin{array}{l} i = i _ {L \Delta} + C _ {\mathrm{d}} \frac {\mathrm{d} u _ {c \Delta}}{\mathrm{d} t} \\ L _ {\mathrm{d}} \frac {\mathrm{d} i _ {L \Delta}}{\mathrm{d} t} + R _ {2} i _ {L \Delta} - u _ {c} = 0 \\ R _ {1} \Bigg (i _ {_ {L \Delta}} + C _ {\mathrm{d}} \frac {\mathrm{d} u _ {_ {C \Delta}}}{\mathrm{d} t} \Bigg) + L _ {\mathrm{d}} \frac {\mathrm{d} i _ {_ {L \Delta}}}{\mathrm{d} t} + R _ {2} i _ {_ {L \Delta}} = u _ {\mathrm{S}} (t) \\ \end{array}
$$

以  $i_{L\Delta}(t)$  为电路变量, 整理得其二阶电路的微分方程为

$$
R _ {1} C _ {\mathrm{d}} L _ {\mathrm{d}} \frac {\mathrm{d} ^ {2} i _ {L \Delta}}{\mathrm{d} t ^ {2}} + (R _ {1} R _ {2} C _ {\mathrm{d}} + L _ {\mathrm{d}}) \frac {\mathrm{d} i _ {L \Delta}}{\mathrm{d} t} + (R _ {1} + R _ {2}) i _ {L \Delta} = u _ {\mathrm{S}} (t)
$$

代入电路参数, 当干扰信号  $u_{S1}=0.45\times10^{-2}\varepsilon(t)$  V 单独作用于电路时, 得

$$
0. 5 \frac {\mathrm{d} ^ {2} i _ {L \Delta}}{\mathrm{d} t ^ {2}} + 2. 7 5 \frac {\mathrm{d} i _ {L \Delta}}{\mathrm{d} t} + 2. 2 5 i _ {L \Delta} = 0. 4 5 \times 1 0 ^ {- 2} \varepsilon (t)
$$

其相应的齐次微分方程为

$$
0. 5 \frac {\mathrm{d} ^ {2} i _ {L \Delta}}{\mathrm{d} t ^ {2}} + 2. 7 5 \frac {\mathrm{d} i _ {L \Delta}}{\mathrm{d} t} + 2. 2 5 i _ {L \Delta} = 0
$$

齐次微分方程的特征方程为

$$
0. 5 p ^ {2} + 2. 7 5 p + 2. 2 5 = 0
$$

其特征根为

$$
p _ {1} = - 1, \quad p _ {2} = - 4. 5
$$

相应的齐次解为

$$
i _ {L \Delta} (t) = (k _ {1} \mathrm{e} ^ {- t} + k _ {2} \mathrm{e} ^ {- 4. 5 t}) \mathrm{A}
$$

相应的特解为

$$
I _ {0 \Delta} = \left(\frac {0 . 4 5}{2 . 2 5} \times 1 0 ^ {- 2}\right) \mathrm{A} = 0. 2 \times 1 0 ^ {- 2} \mathrm{A}
$$

全解为

$$
i _ {L \Delta} (t) = (k _ {1} \mathrm{e} ^ {- t} + k _ {2} \mathrm{e} ^ {- 4. 5 t}) + 0. 2 \times 1 0 ^ {- 2}
$$

根据初始条件确定积分常数  $k_{1}$  和  $k_{2}$ 。

当 $t = 0_{+}$ 时，已知 $i_{L\Delta}(0_{+}) = i_{L\Delta}(0_{-}) = 0$ ，则有

$$
i _ {L \Delta} (t) \mid_ {t = 0} = (k _ {1} \mathrm{e} ^ {- t} + k _ {2} \mathrm{e} ^ {- 4. 5 t}) + 0. 2 \times 1 0 ^ {- 2} \mid_ {t = 0} = 0
$$

当 $t = 0_{+}$ 时，已知 $u_{c\Delta}(0_{+}) = u_{c\Delta}(0_{-}) = 0$ ，则有

$$
\begin{array}{l} u _ {C \Delta} (t) \mid_ {t = 0} = \left(L _ {\mathrm{d}} \frac {\mathrm{d} i _ {L \Delta}}{\mathrm{d} t} + R _ {2} i _ {L \Delta}\right) \mid_ {t = 0} \\ = 0. 2 5 \left(- k _ {1} \mathrm{e} ^ {- t} - 4. 5 k _ {2} \mathrm{e} ^ {- 4. 5 t}\right) + 1. 2 5 \left(k _ {1} \mathrm{e} ^ {- t} + k _ {2} \mathrm{e} ^ {- 4. 5 t} + 0. 2 \times 1 0 ^ {- 2}\right) \mid_ {t = 0} = 0 \\ \end{array}
$$

故得

$$
k _ {1} + k _ {2} + 0. 2 \times 1 0 ^ {- 2} = 0
$$

$$
0. 2 5 \times (- k _ {1} - 4. 5 k _ {2}) + 1. 2 5 \times (k _ {1} + k _ {2} + 0. 2 \times 1 0 ^ {- 2}) = 0
$$

联立求解以上两式,得

$$
k _ {1} = \frac {9}{3 5} \times 1 0 ^ {- 2}, \quad k _ {2} = - \frac {2}{3 5} \times 1 0 ^ {- 2}
$$

因此，得

$$
i _ {L \Delta 1} (t) = \left(- \frac {9}{3 5} \times 1 0 ^ {- 2} \mathrm{e} ^ {- t} + \frac {2}{3 5} \times 1 0 ^ {- 2} \mathrm{e} ^ {- 4. 5 t} + 0. 2 \times 1 0 ^ {- 2}\right) \varepsilon (t) \mathrm{A}
$$

当干扰信号  $u_{s2} = -0.45 \times 10^{-2} \varepsilon (t-1) \, V$  单独作用于电路时得

$$
i _ {L \Delta 2} (t) = - \left[ - \frac {9}{3 5} \times 1 0 ^ {- 2} \mathrm{e} ^ {- (t - 1)} + \frac {2}{3 5} \times 1 0 ^ {- 2} \mathrm{e} ^ {- 4. 5 (t - 1)} + 0. 2 \times 1 0 ^ {- 2} \right] \varepsilon (t - 1) \mathrm{A}
$$

直流电压源与干扰信号产生的响应之和为

$$
i _ {L} (t) = \left\{1 + \left(- \frac {9}{3 5} \times 1 0 ^ {- 2} \mathrm{e} ^ {- t} + \frac {2}{3 5} \times 1 0 ^ {- 2} \mathrm{e} ^ {- 4. 5 t} + 0. 2 \times 1 0 ^ {- 2}\right) \varepsilon (t) - \right.
$$

$$
\left[ - \frac {9}{3 5} \times 1 0 ^ {- 2} \mathrm{e} ^ {- (t - 1)} + \frac {2}{3 5} \times 1 0 ^ {- 2} \mathrm{e} ^ {- 4. 5 (t - 1)} + 0. 2 \times 1 0 ^ {- 2} \right] \varepsilon (t - 1) \Bigg \} \mathrm{A}
$$

## \*§17-8 二阶非线性电路的状态平面

二阶非线性电路方程的一般形式可写为

$$
\left. \begin{array}{l} \frac {\mathrm{d} x _ {1}}{\mathrm{d} t} = f _ {1} (x _ {1}, x _ {2}, t) \\ \frac {\mathrm{d} x _ {2}}{\mathrm{d} t} = f _ {2} (x _ {1}, x _ {2}, t) \end{array} \right\} \tag {17-9}
$$

其中  $x_{1}(t)$ ,  $x_{2}(t)$  为状态变量, 式(17-9)为状态方程。

如果式(17-9)右方的函数不随时间 $t$ 而变, 即自变量 $t$ 除了在 $\frac{\mathrm{d}x}{\mathrm{d}t}$ 中以隐含形式出现外, 不以任何显含形式出现, 既有

$$
\left. \begin{array}{l} \frac {\mathrm{d} x _ {1}}{\mathrm{d} t} = f _ {1} (x _ {1}, x _ {2}) \\ \frac {\mathrm{d} x _ {2}}{\mathrm{d} t} = f _ {2} (x _ {1}, x _ {2}) \end{array} \right\} \tag {17-10}
$$

这种自变量 $t$ 不以任何显含形式出现的方程(17-10)称为自治方程。若电路是时变的，或电路中包含随时间变化的外施激励，使得方程中自变量 $t$ 以显含形式出现，如式(17-9)所示，则称为非自治方程。在零输入或在直流激励下的非线性二阶电路的方程是自治方程,对应的电路就称为自治电路。

一般来说,求解非线性微分方程(17-9)或(17-10)是比较困难的。通常无闭式解。

把自治方程(17-10)中的状态变量 $x_{1}, x_{2}$ 看作是平面上的坐标点，这种平面就称为状态平面。状态平面上每一点的坐标 $(x_{1}, x_{2})$ 随着时间 $t$ 的变化将在平面上描绘出式(17-10)的某些曲线。设给定的初始状态（条件）为 $x_{1}(0), x_{2}(0)$，对所有 $t \geqslant 0$，方程(17-10)的解 $[x_{1}(t), x_{2}(t)]$ 在平面上描绘出的以 $[x_{1}(0), x_{2}(0)]$ 为起点的轨迹称为该状态方程的一条轨道或相轨道（又称轨迹）。对于不同的初始条件，可以在状态平面上描绘出一簇相轨道，这簇相轨道又称为该自治方程的相图。坐标点 $(x_{1}, x_{2})$ 称为相点。通常从相图可以定性地了解状态方程所描述的电路工作状态的整个变化情况，而不必直接求解非线性微分方程。可以利用数值法通过电子计算机把相轨道描绘出来。相轨道还可以通过实验的方法来观察，例如只要把 $x_{1}(t)$ 和 $x_{2}(t)$ 作为信号电压，把它们加到示波器的水平输入和垂直输入，就可以显示出相应的相轨道。

下面用状态平面讨论二阶 RLC 串联电路放电的动态过程, 其电路如图 17-25 所示。为了简化分析, 设电阻 R、电感 L 和电容 C 都是线性元件。

设电容电压的初始值为 $u_{c}(0_{-}) = U_{0}$，电感电流的初始值为 $i(0_{-}) = 0$，电路的方程为

$$
L \frac {\mathrm{d} ^ {2} i}{\mathrm{d} t ^ {2}} + R \frac {\mathrm{d} i}{\mathrm{d} t} + \frac {i}{C} = 0
$$

令 $x_{1} = i, x_{2} = \frac{\mathrm{d}i}{\mathrm{d}t} = \frac{\mathrm{d}x_{1}}{\mathrm{d}t}$, 上式可改写为

![](images/page_460_image_9.jpg)

<details>
<summary>text_image</summary>

S
R
i
C + U₀ -
L
</details>

图17-25 研究相图用的电路

$$
\left. \begin{array}{l} \frac {\mathrm{d} x _ {1}}{\mathrm{d} t} = x _ {2} \\ \frac {\mathrm{d} x _ {2}}{\mathrm{d} t} = - \omega_ {0} ^ {2} x _ {1} - 2 \delta x _ {2} \end{array} \right\} \tag {17-11}
$$

式中  $\delta=\frac{R}{2L},\omega_{0}^{2}=\frac{1}{LC}$ 。

对式(17-11)直接积分,可以求得相轨道的方程,但需要一定的数学运算。这里主要用状态平面来讨论。

当 $\delta^2 < \omega_0^2$ 或 $R < 2\sqrt{\frac{L}{C}}$ 时，电路中的放电过程为衰减振荡性质，相应的相轨道将如图17-26(a)所示。对应不同的初始条件，相轨道将是一簇螺旋线，并以原点为其渐近点。该图中螺旋线的圈间距离表征了振荡的衰减率，而每一圈对应于振荡的一个周期，原点表示 $x_{1} = 0, x_{2} = 0$ ，是方程(17-11)的所谓“平衡点”。

方程(17-11)的解为

$$
x _ {1} = K \mathrm{e} ^ {- \delta t} \cos (\omega t + \varphi)
$$

$$
x _ {2} = - K \omega_ {0} \mathrm{e} ^ {- \delta t} \sin (\omega t + \varphi + \beta^ {\prime})
$$

式中  $\omega^{2}=\omega_{0}^{2}-\delta^{2},\beta^{\prime}=\arctan\frac{\delta}{\omega}$ ，常数 K 和  $\varphi$  则由初始条件决定。

当 $\delta^2 >\omega_0^2$ 或 $R > 2\sqrt{\frac{L}{C}}$ 时，电路中的放电过程为非周期衰减性质，相应的相轨道将如图17-26(b)所示。对应不同的初始条件，相轨道将是一簇变形的抛物线，原点是它们的渐近点，相点的运动方向是趋近于原点的。

方程式(17-11)的解为

$$
x _ {1} = K _ {1} \mathrm{e} ^ {- m _ {1} t} + K _ {2} \mathrm{e} ^ {- m _ {2} t}
$$

$$
x _ {2} = - K _ {1} m _ {1} \mathrm{e} ^ {- m _ {1} t} - K _ {2} m _ {2} \mathrm{e} ^ {- m _ {2} t}
$$

其中 $-m_{1}=-\delta+\sqrt{\delta^{2}-\omega_{0}^{2}},-m_{2}=-\delta-\sqrt{\delta^{2}-\omega_{0}^{2}}$ ，常数 $K_{1}$ 和 $K_{2}$ 由初始条件确定。

![](images/page_461_image_9.jpg)

<details>
<summary>text_image</summary>

x₂
x₁
</details>

(a)

![](images/page_461_image_11.jpg)

<details>
<summary>text_image</summary>

x₂
O
x₁
</details>

(b)

![](images/page_461_image_13.jpg)

<details>
<summary>text_image</summary>

x₂
O
x₁
</details>

(c)

图 17-26 式(17-11)的相图

当  $\delta=0$  或 R=0 时, 式  $(17-11)$  变为

$$
\frac {\mathrm{d} x _ {2}}{\mathrm{d} x _ {1}} = - \omega_ {0} ^ {2} \frac {x _ {1}}{x _ {2}}
$$

经过积分后得

$$
\frac {x _ {1} ^ {2}}{K ^ {2}} + \frac {x _ {2} ^ {2}}{K ^ {2} \omega_ {0} ^ {2}} = 1
$$

式中 K 是与初始条件有关的积分常数。对应不同的初始条件，相轨道是具有水平轴为 K，垂直半轴为  $\omega_{0}K$  的一簇椭圆，如图 17-26(c) 所示，它对应于不衰减的正弦振荡。振荡的振幅与初始条件有关。

方程式(17-11)的解为

$$
x _ {1} = K \cos (\omega_ {0} t + \varphi)
$$

$$
x _ {2} = - K \omega_ {0} \sin (\omega_ {0} t + \varphi)
$$

这个例子说明相轨道形状的研究可以对定性了解电路全部解提供有用的信息。

另外，在某些非线性自治电路中，在一定的初始条件下会建立起不衰减的周期振荡过程，此时所对应的相轨道将是一条称为极限环的孤立闭合曲线。

## \* §17-9 非线性振荡电路

电子振荡电路一般至少含有两个储能元件和至少一个非线性元件。本节通过实例介绍一种典型的非线性振荡电路，即范德坡电路。它是由一个线性电感，一个线性电容和一个非线性电阻组成，如图17-27(a)所示，非线性电阻的伏安特性曲线有一段为负电阻性质，它的伏安特性可用下式表示(属电流控制型):

$$
u _ {R} = \frac {1}{3} i _ {R} ^ {3} - i _ {R}
$$

伏安特性曲线的大致形状如图 17-27(b) 所示。

![](images/page_462_image_12.jpg)

<details>
<summary>text_image</summary>

iL L
+ uC C + iR
- uR
</details>

(a)

![](images/page_462_image_14.jpg)

<details>
<summary>text_image</summary>

i_R
O
u_R
</details>

(b)

图 17-27 范德坡电路

电路的状态方程可写为(注意  $i_{L}=i_{R}$ )

$$
\left. \begin{array}{l} \frac {\mathrm{d} u _ {C}}{\mathrm{d} t} = - \frac {i _ {L}}{C} \\ \frac {\mathrm{d} i _ {L}}{\mathrm{d} t} = \frac {u _ {C} - \left(\frac {1}{3} i _ {L} ^ {3} - i _ {L}\right)}{L} \end{array} \right\} \tag {17-12}
$$

其中  $u_{C}$  和  $i_{L}$  为状态变量。为了使用量纲为一的量，令  $\tau=\frac{1}{\sqrt{LC}}t,\tau$  是量纲为一的量。这样有

$$
\frac {\mathrm{d} u _ {c}}{\mathrm{d} t} = \frac {\mathrm{d} u _ {c}}{\mathrm{d} \tau} \frac {\mathrm{d} \tau}{\mathrm{d} t} = \frac {1}{\sqrt {L C}} \frac {\mathrm{d} u _ {c}}{\mathrm{d} \tau}
$$

$$
\frac {\mathrm{d} i _ {L}}{\mathrm{d} t} = \frac {\mathrm{d} i _ {L}}{\mathrm{d} \tau} \frac {\mathrm{d} \tau}{\mathrm{d} t} = \frac {1}{\sqrt {L C}} \frac {\mathrm{d} i _ {L}}{\mathrm{d} \tau}
$$

令 $\varepsilon = \sqrt{\frac{C}{L}}$ ，则式(17-12)可改写为

$$
\left. \begin{array}{l} \frac {\mathrm{d} u _ {c}}{\mathrm{d} \tau} = - \frac {1}{\varepsilon} i _ {L} \\ \frac {\mathrm{d} i _ {L}}{\mathrm{d} \tau} = \varepsilon \left[ u _ {c} - \left(\frac {1}{3} i _ {L} ^ {3} - i _ {L}\right) \right] \end{array} \right\}
$$

若令 $x_{1} = i_{L}, x_{2} = \frac{\mathrm{d}i_{L}}{\mathrm{d}\tau}$, 则上式又可改写为

$$
\left. \begin{array}{l} \frac {\mathrm{d} x _ {1}}{\mathrm{d} \tau} = x _ {2} \\ \frac {\mathrm{d} x _ {2}}{\mathrm{d} \tau} = \varepsilon (1 - x _ {1} ^ {2}) x _ {2} - x _ {1} \end{array} \right\} \tag {17-13}
$$

方程(17-13)中仅有一个参数  $\varepsilon$ 。对不同的  $\varepsilon$  值, 可以画出该方程不同的相图, 就可以了解图 17-27(a) 所示电路的定性性质。图 17-28 画出了  $\varepsilon=0.1$  时的相图。从图中可

以看出有单一的闭合曲线存在。这种单一的或孤立的闭合曲线称为极限环，与其相邻的相轨道都是卷向它的。所以不管相点最初在极限环外或是在极限环内，最终都将沿着极限环运动。如果取 $u_{c}$ 的标度为 $i_{L}$ 标度的 $\frac{1}{\varepsilon}$ 倍，则极限环接近为一个圆。此时 $u_{c}$ 和 $i_{L}$ 的波形与正弦波形接近， $u_{c}$ 的振幅为 $i_{L}$ 的振幅的 $\frac{1}{\varepsilon}$ 倍。这说明不管初始条件如何，在所研究电路中最终将建立起周期性振荡。这种在非线性自治电路中产生的持续振荡是一种自激振荡，它与图17-26(c)在线性电路中产生的振荡过程有所不同,后者的振荡振幅是与初始条件有关的。

![](images/page_463_image_12.jpg)

<details>
<summary>text_image</summary>

i_L
2
-20
O
20 u_C
-2
</details>

图 17-28 · 范德坡振荡电路的相图

如果令式(17-13)中的 $x_{1} = x$ ，该方程还可写为含有一个变量的二阶非线性微分方程

$$
\frac {\mathrm{d} ^ {2} x}{\mathrm{d} t ^ {2}} - \varepsilon (1 - x ^ {2}) \frac {\mathrm{d} x}{\mathrm{d} t} + x = 0
$$

上式就是范德坡方程。

## \* §17-10 混沌电路简介

混沌理论自20世纪70年代以来已成为许多不同学科领域的研究热点。粗略地说，混沌是发生在确定性系统中的一种不确定行为，或类似随机的行为，混沌运动是另一种非周期运动。混沌的一个最显著的特点是，状态变量的波形对状态变量的初始值极为敏感，或者说初始值对波形有重大影响。在有些二阶非线性非自治电路或三阶非线性自治电路中就存在着混沌现象。这类动态电路方程是二阶或三阶非线性常微分方程。根据经典理论，在初始态条件确定之后，它的解是确定的。但是发现在一定参数值的条件下，电路会出现很复杂的解，这种解不是周期解，又不是拟周期解 $^{①}$ ，在状态平面上它的相轨道始终不会重复，但是有界的，即在一定的有界范围内具有遍历性，它对初始态条件极为敏感。

图 17-29 所示是线性电阻 R、线性电感 L 和半导体变容二极管 D 组成的串联电路，外施电压为正弦电压。变容二极管可以用一个非线性电阻和一个非线性电容的并联组合作为其电路模型。

此电路的方程是一个二阶非自治非线性微分方程。在一定的参数条件下，该电路中当正弦激励的频率固定，振幅  $U_{m}$  自零逐步增长时，用实验观察或

![](images/page_464_image_11.jpg)

<details>
<summary>text_image</summary>

i
R
L
+
u=Um cos(ωt)
-
D
</details>

图 17-29 变容二极管混沌电路

用计算机求解电路中的电流 $i$，将会发现当 $U_{\mathrm{m}}$ 自零增长到 $U_{\mathrm{m1}}$ 之前，电流 $i$ 的稳态解是非正弦周期解，这时它的周期与外施正弦激励的周期相同。当达到 $U_{\mathrm{m1}}$ 时，电流 $i$ 仍为非正弦周期性的，但它的周期已变为外施正弦激励周期的2倍。所以电流的基波频率为正弦激励频率的 $\frac{1}{2}$②，即 $\frac{1}{2}\omega$。当 $U_{\mathrm{m}}$ 继续增大时，例如达到 $U_{\mathrm{m2}}$ 时，会出现稳定的周期为外施激励周期4倍的解。之后又会出现8倍周期解，16倍周期解。这种现象称为分叉。自16周期分叉后会出现一个混沌区，此时电流即非周期解又非拟周期解。在混沌区后，随激励幅值的增加还发现有3周期、6周期等分叉。图17-30就是电流分叉的示意图，图中的数字2、4等表示2周期、4周期等分叉。

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 拟周期解可以看作是一些具有不同频率的周期解之和，这些频率的相互比值是非有理数。总体看来，它似乎是具有“很长”的周期又接近周期解的一种解。</span></small>

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">② 一个非正弦周期解,如果它的基波频率是外施频率的分数倍,这种“谐波”称为“子谐波”。线性电路的非正弦周期解,它的“谐波”是外施频率的整数倍,基波频率则与外施频率相同。</span></small>

![](images/page_465_chart_4.jpg)

<details>
<summary>funnel</summary>

| Um | Current (State 1) | Current (State 2) | Current (State 3) | Current (State 4) |
| --- | --- | --- | --- | --- |
| Um1 | Stable | — | — | — |
| Um2 | Decreasing | Increasing | Increasing | Increasing |
| Um4 | Decreasing | Decreasing | Increasing | Increasing |
| Um8 | Decreasing | Decreasing | Decreasing | Increasing |
| Unlabeled Region | — | — | — | — |
| Unlabeled Region (subset) | — | — | — | — |
| Unlabeled Region (outer) | — | — | — | Increasing |
| Unlabeled Region (end) | — | — | — | Increasing |
</details>

图 17-30 电流的分叉

混沌现象广泛地存在于非线性电路中,其中比较典型并已得到深入研究的电路是二阶非自治铁磁谐振电路和称为蔡氏电路的三阶自治电路。

蔡氏电路 $^{①}$ 如图17-31(a)所示,它是由两个线性电容、一个线性电感、一个线性电阻和一个非线性电阻构成的三阶自治动态电路,非线性电阻的伏安特性为 $i_{R}=g(u_{R})$ ,是一个分段线性电阻,如图17-31(b)所示,其中 $m_{0},m_{1},m_{2}$ 分别表示相应折线的斜率。

![](images/page_465_image_8.jpg)

图 17-31 · 蔡氏电路

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 此电路由 L. O. Chua(蔡少棠) 提出, 故称为蔡氏电路, 又称为“双涡卷(double scroll) 电路”。</span></small>

设电容电压 $u_{C_1}, u_{C_2}$ 和电感电流 $i_L$ 为状态变量，得电路的状态方程如下:

$$
\left. \begin{array}{l} C _ {1} \frac {\mathrm{d} u _ {c _ {1}}}{\mathrm{d} t} = \frac {1}{R _ {0}} (u _ {c _ {2}} - u _ {c _ {1}}) - g (u _ {R}) \\ C _ {2} \frac {\mathrm{d} u _ {c _ {2}}}{\mathrm{d} t} = \frac {1}{R _ {0}} (u _ {c _ {1}} - u _ {c _ {2}}) + i _ {L} \\ L \frac {\mathrm{d} i _ {L}}{\mathrm{d} t} = - u _ {c _ {2}} \end{array} \right\} \tag {17-14}
$$

这是一个三阶非线性自治方程组。这个电路在不同的参数值条件下会发生丰富多样的自激振荡动态过程，并有混沌出现，同时方程的解对初始条件非常敏感。根据不同的 $C_1, C_2, L, R_0$ 及非线性电阻的 $U_1, U_2, m_0, m_1, m_2$ 等和不同的 $u_{c_1}(0), u_{c_2}(0), i_L(0)$ 初始条件，按式(17-14)，应用计算机可以计算出以 $u_{c_1}, u_{c_2}$ 和 $i_L$ 为坐标的状态空间的相轨道和它们的时域波形。

图 17-32 示出了在某一组参数值及初始条件下,电路出现混沌时投影在  $i_{L}-u_{C_{1}}$  状态平面上的相轨道,它具有“双涡卷”形状,故称此电路为“双涡卷”电路,其相轨道永不重复。图 17-33 示出了电容电压的时域波形,说明了混沌振荡的非周期性。

![](images/page_466_chart_7.jpg)

<details>
<summary>contour</summary>

| Series | iL (range) | uCi (range) |
| --- | --- | --- |
| Phase space | -2.5~2.7 | -3.1~3.2 |
</details>

图 17-32 双涡卷相轨道

由于非线性电路中混沌解的特殊性,分析研究混沌的方法主要有:(1) 使用计算机对非线性电路进行数值计算,从得到的相图和时域波形等来判别混沌特征的信息;(2) 对电路直接进行实验,在实验中对混沌现象进行观察和分析。

![](images/page_467_chart_3.jpg)

<details>
<summary>line</summary>

| t | uC_i |
| --- | --- |
| 0 | ~0.1 |
| 0.2 | ~2.1 |
| 0.5 | ~-0.4 |
| 1.0 | ~-2.1 |
| 1.5 | ~-2.1 |
| 2.0 | ~-1.9 |
| 2.5 | ~-2.2 |
| 3.0 | ~1.4 |
| 4.0 | ~1.6 |
| 4.5 | ~2.1 |
| 5.0 | ~-1.7 |
| 6.0 | ~-2.2 |
| 6.5 | ~1.9 |
| 7.0 | ~-0.2 |
| 7.5 | ~2.1 |
| 8.0 | ~-1.5 |
</details>

图 17-33 电容电压的时域波形

## \*§17-11 人工神经元电路

人工神经网络(简称神经网络)试图部分模仿人脑神经系统的结构和功能,它与数字计算机迥然不同,它具有分布式存储和并行处理的特色。人工神经网络只是人脑功能的一种简化和抽象的模型。人的大脑含有数以亿万计的生物神经元,以特定的方式相互连接,从而使人具有理解、记忆、联想、识别和计算的能力。生物神经元可以当作是具有输入和输出的处理信息的单元,其输入和输出之间的关系可用具有饱和特性的一种S型非线性转移函数来描述。人工神经元模型就是根据这一设想构成的。

神经网络具有广泛的应用前景,可用来处理识别、分类、联想、优化等问题。目前有许多种神经网络模型。本书介绍人工神经网络的 Hopfield 电路模型,这是一种用电路实现的神经网络模型。

图 17-34 示出了这个电路模型的第 k 个人工神经元的构成, 图中的运放具有有限放大倍数并计及其饱和特性, 运放的输出电压与输入电压之间的转移函数关系  $u_{ok}=f_{k}(u_{ik})$  可用来描述神经元的相应转移函数关系。运放输入

![](images/page_467_image_9.jpg)

<details>
<summary>text_image</summary>

u_{o1} u_{oj} u_{on}
R_{k1} ... R_{kj} ... R_{kn}
I_k +
R_k C_k
u_{jk}
- ▶
+ +
+ u_{ok}
-
</details>

图17-34 第 $k$ 个神经元电路

端的电容 $C_k$ 和电阻 $R_{k}$ 对于输出与输入信号之间产生延迟作用，以此模仿神经元的动态特性。另外在输入端连接的电阻 $R_{kj}$ 用来表示第 $j$ 个神经元的输出电压 $u_{oj}$ 与第 $k$ 个神经元产生的输入电流之间的相互联系。电流 $I_{k}$ 表示注入第 $k$ 个神经元的电流。

根据 KCL, 在第 k 个神经元的输入节点处有

$$
C _ {k} \frac {\mathrm{d} u _ {\mathrm{ik}}}{\mathrm{d} t} + \frac {u _ {\mathrm{ik}}}{R _ {k}} = \sum_ {j \neq k} ^ {n} \frac {1}{R _ {k j}} (u _ {\mathrm{o} j} - u _ {\mathrm{ik}}) + I _ {k}
$$

整理后,有

$$
C \frac {\mathrm{d} u _ {\mathrm{ik}}}{\mathrm{d} t} = \sum_ {j \neq k} ^ {n} \frac {1}{R _ {k j}} u _ {\mathrm{o} j} - \frac {1}{R _ {k} ^ {\prime}} u _ {\mathrm{ik}} + I _ {k}
$$

其中

$$
\frac {1}{R _ {k} ^ {\prime}} = \frac {1}{R _ {k}} + \sum_ {j \neq k} ^ {n} \frac {1}{R _ {k j}}
$$

另外有

$$
u _ {o k} = f _ {k} (  u _ {i k})
$$

上式中假设共有 n 个神经元相互连接，而  $k=1,2,\cdots,n$ 。

对于每个神经元都可以列出上述类似的方程,这样就构成了一个 n 阶非线性微分方程组。当给定一组初始值后,就可以求出此方程组的解。如果方程组的解为一组确定值,则表明电路最终将达到一个稳定状态。

以这种神经元模型为基础,可以设计出用来处理和求解多种不同类型问题的神经网络电路。这些问题包括“旅行商最优路径问题”、模-数转换问题、线性规划问题以及其他各种优化问题等。

![](images/page_468_image_14.jpg)

## 思考题

17-1 动态电阻和静态电阻各用于什么场合？
17-2 非线性电阻电路的方程是什么方程？
17-3 包含非线性电阻元件和线性储能元件的电路方程是什么方程？包含线性电阻和非线性储能元件的电路方程是什么方程？
17-4 如果电路中含有电压控制电阻,请问电路适合列写节点电压方程还是回路电流方程?如果电路含有电流控制的非线性电阻,适合列写节点电压方程还是回路电流方程?如果电路既含有电压控制非线性电阻也含有电流控制非线性电阻,适合采用哪种电路方程?
17-5 如果采用分段线性法分析非线性电路,你认为主要的困难是什么?

17-6 本章介绍的小扰动下的动态电路分析,有哪些限制条件?

![](images/page_469_image_4.jpg)

## 习题

17-1 如果通过非线性电阻的电流为  $\cos(\omega t)A$ ，要使该电阻两端的电压中含有  $4\omega$  角频率的电压分量，试求该电阻的伏安特性，写出其解析表达式。
17-2 写出题 17-2 图所示电路的节点电压方程, 假设电路中各非线性电阻的伏安特性为  $i_{1}=u_{1}^{3}, i_{2}=u_{2}^{2}, i_{3}=u_{3}^{3/2}$ 。
17-3 一个非线性电容的库伏特性为 $u = 1 + 2q + 3q^2$，如果电容从 $q(t_0) = 0$ 充电至 $q(t) = 1\mathrm{C}$。试求此电容储存的能量。
17-4 非线性电感的韦安特性为  $\Psi=i^{3}$ ，当有 2 A 电流通过该电感时，试求此时的静态电感值。
17-5 已知题 17-5 图所示电路中， $U_{s}=84\ V, R_{1}=2\ k\Omega, R_{2}=10\ k\Omega$ ，非线性电阻  $R_{3}$  的伏安特性可表示为  $i_{3}=0.3u_{3}+0.04u_{3}^{2}$ 。试求电流  $i_{1}$  和  $i_{3}$ 。

![](images/page_469_image_12.jpg)

<details>
<summary>text_image</summary>

12 A
i₁
+
u₁
-
①
i₂
+
u₂
-
②
i₃
+
u₃
-
4 A
</details>

题 17-2 图

![](images/page_469_image_14.jpg)

<details>
<summary>text_image</summary>

R₁ i₁
+ Uₛ R₂ i₃
- +
u₃ R₃
</details>

题 17-5 图

17-6 题 17-6 图所示电路由一个线性电阻 R，一个理想二极管和一个直流电压源串联组成。已知  $R=2\Omega, U_{s}=1V$ ，在 u-i 平面上画出对应的伏安特性。
17-7. 题 17-7 图所示电路由一个线性电阻 R、一个理想二极管和一个直流电流源并联组成。已知  $R = 1 \Omega, I_{s} = 1 \, A$ ，在 u-i 平面上画出对应的伏安特性。

![](images/page_469_image_19.jpg)

<details>
<summary>text_image</summary>

i
+
R
u
+
Us
-
-
-
</details>

题17-6图

![](images/page_469_image_21.jpg)

<details>
<summary>text_image</summary>

i
+
u
R
I_S
-
</details>

题 17-7 图

17-8 试设计一个由线性电阻、独立电源和理想二极管组成的一端口网络，要求它的伏安特性具有题17-8图所示特性。

17-9 设题 17-9 图所示电路中二极管的伏安特性可用下式表示:

$$
i _ {\mathrm{D}} = 1 0 ^ {- 6} (\mathrm{e} ^ {4 0 u _ {\mathrm{D}}} - 1) \mathrm{A}
$$

式中  $u_{D}$  为二极管的电压，其单位为 V，已知  $R_{1}=0.5\Omega, R_{2}=0.5\Omega, R_{3}=0.75\Omega, U_{S}=2V$ 。试用图解法求出静态工作点。

![](images/page_470_chart_6.jpg)

<details>
<summary>line</summary>

| u/V | i/A |
| --- | --- |
| -1 | 0 |
| 0 | 2 |
</details>

题 17-8 图

![](images/page_470_image_8.jpg)

<details>
<summary>text_image</summary>

R₁
+
Uₛ
-
R₂
R₃
iₐ
+
uₐ
-
</details>

题 17-9 图

17-10 题 17-10 图所示非线性电阻电路中,非线性电阻的伏安特性为

$$
u = 2 i + i ^ {3}
$$

现已知当 $u_{\mathrm{s}}(t) = 0$ 时，回路中的电流为 $1\mathrm{A}$ 。如果 $u_{\mathrm{s}}(t) = \cos (\omega t)\mathrm{V}$ 时，试用小信号分析法求回路中的电流 $i$ 。

17-11 题 17-11 图所示电路中, $R=2\Omega$ 。直流电压源 $U_{s}=9V$ ,非线性电阻的伏安特性 $u=-2i+\frac{1}{3}i^{3}$ ,若 $u_{s}(t)=\cos tV$ ,试求电流i。

![](images/page_470_image_14.jpg)

<details>
<summary>text_image</summary>

i
+
us
-
5 V
2 Ω
u=f(i)
</details>

题 17-10 图

![](images/page_470_image_16.jpg)

<details>
<summary>text_image</summary>

+
Us
-
R
i
+
Us
-
+ u
-
</details>

题 17-11 图

17-12 题 17-12 图(a)所示电路中, 直流电压源  $U_{s}=3.5\ V, R=1\ \Omega$ , 非线性电阻的伏安特性曲线如题 17-12 图(b)所示。

(1) 试用图解法求静态工作点。
(2) 如将曲线分成 OC、CD 和 DE 三段, 试用分段线性化方法求静态工作点, 并与 (1) 的结果相比较。

![](images/page_471_image_3.jpg)

<details>
<summary>text_image</summary>

R
+
Us
-
+
u
-
i
</details>

(a)

![](images/page_471_chart_5.jpg)

<details>
<summary>line</summary>

| Point | i/A | u/V |
| --- | --- | --- |
| C | 1 | 1 |
| D | 2 | 3 |
| E | 3 | 6 |
</details>

(b)

题17-12图

17-13 题 17-13 图所示电路中, 非线性电阻的伏安特性为  $i=u^{2}$ , 试求电路的静态工作点及该点的动态电阻  $R_{d}$ 。
17-14 题 17-14 图所示电路中, 非线性电阻的伏安特性为  $u = i^{3}$ , 如将此电阻突然与一个充电的电容接通, 试求电容两端的电压  $u_{C}$ , 设  $u_{C}(0_{+}) = U_{0}$ 。

![](images/page_471_image_11.jpg)

<details>
<summary>text_image</summary>

3 A
I₀
R 0.5 Ω
+
u
-
i=g(u)
</details>

题 17-13 图

![](images/page_471_image_13.jpg)

<details>
<summary>text_image</summary>

+
U₀
-
C
+
uC
-
S
i
+
u=i³
-
</details>

题17-14图

\* 17-15 在题 17-15 图所示电路中, 线性电容通过非线性电阻放电, 非线性电阻伏安特性如题 17-15 图 (b) 所示。已知 $C = 1 \mathrm{~F}, u_{c}(0_{-}) = 3 \mathrm{~V}$, 试求 $u_{c}$。

![](images/page_471_image_16.jpg)

<details>
<summary>text_image</summary>

+
U₀
-
+
uC
-
S
i
+
uᵣ
-
</details>

(a)

![](images/page_471_chart_18.jpg)

<details>
<summary>line</summary>

| uR (V) | i (A) |
| --- | --- |
| 0 | 0 |
| 1 | 2 |
| 2 | 1 |
| 3 | 2 |
</details>

(b)

题 17-15 图

\* 17-16 含有非线性电感的一阶动态电路如题 17-16 图所示, 已知直流电压源 $U_{\mathrm{S}} = 40 \mathrm{~V}$, 小扰动电压源 $u_{\mathrm{S}}(t) = 1.2 \mathrm{e}^{-10 t} \varepsilon(t) \mathrm{~V}$, 线性电阻 $R_{1} = 10 \Omega, R_{2} = 40 \Omega$, 非线性电感 $\psi = 0.5 i^{3} (\psi$ 单位为 $\mathrm{Wb}, i$ 单位为 A)。求 $t > 0$ 时的响应 $i_{L}(t), u_{2}(t)$。

![](images/page_472_image_3.jpg)

<details>
<summary>text_image</summary>

u_s(t)
+
-
R_1
ψ
i_L
+
U_S
-
R_2
u_2
-
</details>

题 17-16 图

\* 17-17 （综合设计题）已知 Lorenz 混沌系统为

$$
\frac {\mathrm{d} x}{\mathrm{d} t} = a (y - x)
$$

$$
\frac {\mathrm{d} y}{\mathrm{d} t} = b x - x z - y
$$

$$
\frac {\mathrm{d} z}{\mathrm{d} t} = x y - c x
$$

系统参数 a=10, b=28, c=8/3，试应用电路元件电阻、电容、运算放大器、乘法器来设计实现 Lorenz 混沌系统。

![](images/page_472_image_10.jpg)

第十七章部

分习题答案

# 第十八章 均匀传输线

![](images/page_473_image_2.jpg)

## 导读

电磁现象都是在空间发生的。集总参数电路不能考虑电磁现象的空间分布性，因为实际电磁现象的发生是电磁作用（以场的形式）在空间传播的结果。其传播速度是有限的，远离电源处比起较近处电磁作用的出现有推迟现象。对正弦变化来说，远处的正弦变化在相位上要比较落后，这就意味着难以用一个物理量（例如电流）来概括不同空间所出现的电磁现象（例如在空间的能量损耗等）。以传递能量、信号为目的的传输线，在传输方向上线路可以甚长，沿线路电磁作用的推迟作用必须考虑；但是在垂直于传输方向的空间上，尺寸不会很大，可以不计该方向上的推迟作用。这就使得我们仍可使用电路的物理量和电路元件来描述线路的物理过程，但此时的电路物理量应沿线路长度而变化，并且元件也必须是沿线路作分布的分布参数元件。只有如此才能正确地描绘这种特殊情况的电路。

均匀传输线的电路变量既是时间又是空间的函数,故电路方程将是偏微分方程。讨论其正弦稳态解时,解答是沿线变化的复数相量,方程也成为常微分方程。在这些解中出现的波动特性应在学习过程中倍加注意和领会。

## §18-1 分布参数电路

在以前各章中，讨论了由集总参数元件组成的电路模型。每一种集总参数元件被假设集中由一种电磁现象所表征。例如，电阻元件集中表征了某一个实际部件或某一段实际电路中的能量消耗，电感元件集中地反映了磁场的物理现象，电容元件则集中反映了电场的物理现象（如充、放电，位移电流等）。但是，在某些实际电路中，发生的电磁现象往往是带有分布性的，必须在一定条件下才能建立其集总参数模型。图18-1(a)示出一个实际电路，这是一个电源通过导线向负载传递信号或能量的传输电路。导线中的电流是由导线中电场产生的，电流在导线外产生磁场（用磁感应强度 $B$ 表示）；并且由于两导线之间的电压，导线间也有电场（用电场强度 $E$ 表示），此电场在导线间产生电容电流和漏电流。这些电场-磁场都是沿线分布，即分散在空间的。就导线上的能量损耗与磁场效应来说，因导线间的电流导致导线中的电流处处不同，故不能以一项 $i^2 R$ 或 $L\frac{\mathrm{d}i}{\mathrm{d}t}$ （即以一个集总参数 $R, L$）来概括导线上的物理过程；而导线上的电阻、电感压降也导致线间的电压处处不相同，故不能以一项 $u^2 G$ 或 $C\frac{\mathrm{d}u}{\mathrm{d}t}$（即以一个集总参数 $G, C$）来概括导线间的物理过程。接近这种物理现象的电路模型，应是由无限多个导线上的电阻、电感以及无限多个导线间的电导、电容所组成的分布参数模型，如图18-1(b)所示。

![](images/page_474_image_4.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph LR
  A["电源"] -->|"E"| B["负载"]
  B -->|"B"| C["..."]
  C -->|"B"| D["..."]
  D -->|"B"| E["..."]
  E -->|"E"| F["..."]
  F -->|"E"| G["..."]
  G -->|"E"| H["..."]
  H -->|"E"| I["..."]
  I -->|"E"| J["..."]
  J -->|"E"| K["..."]
  K -->|"E"| L["..."]
  L -->|"E"| M["..."]
  M -->|"E"| N["..."]
  N -->|"E"| O["..."]
  O -->|"E"| P["..."]
  P -->|"E"| Q["..."]
  Q -->|"E"| R["..."]
  R -->|"E"| S["..."]
  S -->|"E"| T["..."]
  T -->|"E"| U["..."]
  U -->|"E"| V["..."]
  V -->|"E"| W["..."]
  W -->|"E"| X["..."]
  X -->|"E"| Y["..."]
  Y -->|"E"| Z["..."]
  Z -->|"E"| AA["..."]
  AA -->|"E"| AB["..."]
  AB -->|"E"| AC["..."]
  AC -->|"E"| AD["..."]
  AD -->|"E"| AE["..."]
  AE -->|"E"| AF["..."]
  AF -->|"E"| AG["..."]
  AG -->|"E"| AH["..."]
  AH -->|"E"| AI["..."]
  AI -->|"E"| AJ["..."]
  AJ -->|"E"| AK["..."]
  AK -->|"E"| AL["..."]
  AL -->|"E"| AM["..."]
  AM -->|"E"| AN["..."]
  AN -->|"E"| AO["..."]
  AO -->|"E"| AP["..."]
  AP -->|"E"| AQ["..."]
  AQ -->|"E"| AR["..."]
  AR -->|"E"| AS["..."]
  AS -->|"E"| AT["..."]
  AT -->|"E"| AU["..."]
  AU -->|"E"| AV["..."]
  AV -->|"E"| AW["..."]
  AW -->|"E"| AX["..."]
  AX -->|"E"| AY["..."]
  AY -->|"E"| AZ["..."]
  AZ -->|"E"| BA["..."]
  BA -->|"E"| BB["..."]
  BB -->|"E"| BC["..."]
  BC -->|"E"| BD["..."]
  BD -->|"E"| BE["..."]
  BE -->|"E"| BF["..."]
  BF -->|"E"| BG["..."]
  BG -->|"E"| BH["..."]
  BH -->|"E"| BI["..."]
  BI -->|"E"| BJ["..."]
  BJ -->|"E"| BK["..."]
  BK -->|"E"| BL["..."]
  BL -->|"E"| BM["..."]
  BM -->|"E"| BN["..."]
  BN -->|"E"| BO["..."]
  BO -->|"E"| BP["..."]
  BP -->|"E"| BR["..."]
  BR -->|"E"| BS["..."]
  BS -->|"E"| BT["..."]
  BT -->|"E"| BU["..."]
  BU -->|"E"| BV["..."]
  BV -->|"E"| BW["..."]
  BW -->|"E"| BX["..."]
  BX -->|"E"| BY["..."]
  BY --> "EB" --> AY
  AY --> "EB" --> BZ["..."]
```
</details>

(a)

![](images/page_474_image_6.jpg)

<details>
<summary>natural_image</summary>

Pure electrical circuit diagram with three parallel branches and resistors, no text or symbols present
</details>

(b)

图 18-1 实际电路参数的分布

应当说,任何实际电路都有是否必须采用分布参数模型的问题。以传输线为例,只要沿线流动的电流随空间距离变化很小,即导线间的空间电容电流及电导电流不大时,就可以用单个电阻来描述损耗、单个电感来描述磁场作用。引申至一个实际电阻器的情况,在直流工作条件下其模型仅为一个电阻元件,在低频交流工作条件下其模型则是电阻元件和电感元件的串联组合;另一方面,当可不计导线上电阻、电感电压降时,认为导线间所有漏电流、所有电容电流处于同一个电压时,就可以用单个电导来描述导线间的漏电作用、单个电容来描述导线间的电容作用。实际电容器部件则是另一例,在直流及低频交流下可不计在极板上电流的电阻性压降和电感性压降,其模型就是一个电容元件和电导元件的并联组合。这些模型都是集总参数模型,构成的电路模型就是集总参数电路。

直流稳态下,有时也要用分布参数模型。例如在直流输电线中,如果要研究沿线的电压、电流变化,这时虽然电感、电容不产生影响,还应从导线上电阻及导线间电导所构成的分布参数模型来研究。

在交流稳态下,由于电感电压以及电容电流都与工作频率成正比,因此在高频下分布参数问题就更为突出。这可以从电磁波的传播来解释。真空中电磁波是以有限速度(光速)的波动方式运动的,在运动过程中在传播方向会出现波峰(极值)、波节(零值)的移动。相邻波峰(或波节)的距离称为工作波长 $\lambda$ 。众所周知, $\lambda=\frac{v}{f}=vT$ ,其中v为波速,f为工作频率,T为周期。在电压(或电流)波峰所到之处,电压(电流)达到极值,在电压(电流)波节所到之处,电压(电流)为零。因此沿传播方向,即使在同一时刻,沿线电压(或电流)是以波长 $\lambda$ 为重复周期 $^{①}$ 的电压(或电流)波动形式。图18-2(a)示出,当线长 $l<<\lambda$ 时,全线的电压(电流)处于同一个变化状态,就可使用集总参数模型 $^{②}$ ;图18-2(b)中示出 $l\ll\lambda$ 时,即线长可与 $\lambda$ 做比较时,此时沿线电压(或电流)有明显的波动,各处数值不一,就不可使用集总参数模型,而必须采用分布参数模型。

![](images/page_475_image_5.jpg)

<details>
<summary>text_image</summary>

+
-
λ
l
</details>

(a) $l <   <   \lambda$

![](images/page_475_image_7.jpg)

<details>
<summary>text_image</summary>

+
-
λ
l
</details>

(b) $l \preccurlyeq \lambda$

图 18-2 电磁作用在线上的传播

线长 $l$ 与工作波长 $\lambda$ 可相比较的传输线称为长线。“长”是以线长相对工作波长 $\lambda$ 而衡量的，因此与工作频率 $f$ 有关。如果波动的速率以真空中的光速计，即 $v = c = 3 \times 10^{8} \mathrm{~m/s}$ 。在工频 $f = 50 \mathrm{~Hz}$ 时，$\lambda = \frac{v}{f} = 6000 \mathrm{~km}$ 。一般的电气部件、传输线都满足 $l < \lambda$ ，可以使用集总参数模型。但在高频情况下就不同了，当 $f = 300 \mathrm{MHz}$ （超高频）时 $\lambda = 1 \mathrm{~m}; f = 30 \mathrm{GHz}$ 时 $\lambda = 1 \mathrm{~cm}$；此时不长的一段线就是长线，如再使用集总模型将会得出错误的结果。在研究天线、雷达及微波设备中的电路时，广泛地使用了分布参数模型。

令  $\Delta t=\frac{l}{v}$ ， $\Delta t$  为电磁作用传遍线长所需的时间。条件  $l\ll\lambda$  两侧均除以 v 后，就可写为  $\Delta t\ll T$ 。周期 T 是度量正弦时间函数随时间变化快慢的值。因此，使用集总模型的条件也可理解为:在电磁作用传遍全线的时间内，电源值几乎未发生变化。此时自然不会沿线出现具有波峰、波节形式的波动。也相当于波是以无限大速度传播的，沿线不存在电磁作用的推迟作用。①

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 由于沿线传播有衰减,故非严格意义的周期变化。</span></small>

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">② 如舍弃线间电流，则视为集总电阻、电感串联；如舍弃线上压降，则视为集总电导、电容并联。</span></small>

应当指出,如果仅关心长线电源端以及负载端的电压、电流,还是可以将传输线部分看为一个二端口网络,或相应地用等值T形、 $\pi$ 形电路来替代,但是这些二端口的参数、等值电路应由分布参数模型来求出。此外,虽然等值T形、 $\pi$ 形电路是集总参数电路,但其中的Z、Y都是在一定的频率下求得的,并非传输线线路参数的直接归结 $^{②}$ 。不能误解为此时分布参数模型可以由集总参数模型来代替。

## §18-2 均匀传输线及其方程

最典型的传输线是由在均匀媒质中放置的两根平行直线导体构成的,其通常的形式如图18-3所示。其中图(a)为两线架空线,图(b)为同轴电缆,图(c)为二芯电缆,图(d)是一线一地构成的传输线,图(e)(f)是在高频下工作的天线。[图(e)是最普通的半波电视天线,左右两段导线的总长为 $\lambda/2$ 。图(f)是中波使用的垂直天线,亦由一线一地构成。]

![](images/page_476_image_6.jpg)

<details>
<summary>text_image</summary>

(a)
(b)
(c)
(d)
(e)
(f)
</details>

图18-3 不同形式的传输线

在上述传输线中,电流在导线的电阻中引起沿线的电压降,并在导线的周围产生磁场,即沿线有电感的存在,变动的电流沿线产生电感电压降。所以,导线间的电压是连续变化的。另一方面,由于两导体构成电容,因此在导线间存在电容电流;导体间还有漏电导,故还有电导电流。这样,沿线不同的地方,导线中的电流也是不同的。为了计及沿线电压与电流的变化,必须认为导线的每一元段(无限小长度的一段)上,在导线上具有无限小的电阻和电感;在导线间则有电容和电导。这就是传输线的分布参数模型,它是集总参数元件构成的极限情况。由于电阻、电感、电容和电导这些参数是分布在线上的,因此必须用单位长度上传输线具有的参数表示,即:

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 读者将在电磁场的学习中加深理解此点。</span></small>

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">② T形、π形等效电路中的各个Z、Y如果以集总元件R、L、G、C来实现时，这些参数将是频率f的函数。此情况类似于:交流电路中，R、L串联组合用 $R'$ 、 $L'$ 并联组合来等效替代时， $R'$ 、 $L'$ 还将与频率有关。并不说明串联结构在一切频率下等同于一个确定值的 $R'$ 、 $L'$ 并联结构。</span></small>

$R_{0}$ ——两根导线每单位长度具有的电阻,其单位为  $\Omega/m$  (在电力传输线中,常用  $\Omega/km$ )。

$L_{0}$ ——两根导线每单位长度具有的电感,其单位为 H/m(或 H/km)。

$C_{0}$ ——每单位长度导线之间的电容,其单位为 F/m(或 F/km)。

$G_{0}$ ——每单位长度导线之间的电导,其单位为 S/m(或 S/km)。

$R_{0}$ 、 $L_{0}$ 、 $C_{0}$ 、 $G_{0}$ 称为传输线的原参数，如果沿线原参数到处相等，则称为均匀传输线。图18-3中图(a)(b)(c)(d)均可看为均匀传输线，图(e)(f)则是不均匀传输线。当然实际的传输线不可能是均匀的。例如图18-3(a)所示的两线架空线在有支架处和没有支架处是不一样的，因为漏电的情况不尽相同。在架空线的每一跨度之间，由于导线的自重引起的下垂情况也改变了传输线对大地的电容的分布均匀性。但是，为了便于分析起见，通常忽略所有造成不均匀性的因素而把实际的传输线当作均匀的传输线。以后的讨论都局限于均匀传输线。

![](images/page_477_image_9.jpg)

<details>
<summary>text_image</summary>

i来线
始端
电源
+
us
-
i回线
x
dx
l
终端
负载
</details>

图 18-4 均匀传输线

图 18-4 表示一均匀传输线, 传输线的一方与电源连接, 称为始端; 传输线的另一方与负载连接, 称为终端。两根导线中, 一根称为来线, 另一根称为回线, 来线是指电流参考方向从始端指向终端的传输线, 回线则指电流参考方向从终端指向始端的传输线。设来线和回线的长度都为 l, 从线的始端到所讨论长度元的距离为 x。

上面已经提到,设想均匀传输线是由一系列集总元件构成的,也就是设想它是由许多无穷小的长度元 dx 组成,每一长度元 dx 具有电阻  $R_{0}dx$  和电感  $L_{0}dx$ ,而两导线间具有电容  $C_{0}dx$  和电导  $G_{0}dx$ 。这样构成了图 18-5 所示的电路模型。设在 dx 左端的电压和电流为 u 和 i,在 dx 右端的电压和电流为  $u+\frac{\partial u}{\partial x}dx$  和  $i+\frac{\partial i}{\partial x}dx$ ,根据 KCL,对于节点 b,有

$$
i - \left(i + \frac {\partial i}{\partial x} \mathrm{d} x\right) = G _ {0} \left(u + \frac {\partial u}{\partial x} \mathrm{d} x\right) \mathrm{d} x + C _ {0} \frac {\partial}{\partial t} \left(u + \frac {\partial u}{\partial x} \mathrm{d} x\right) \mathrm{d} x
$$

对回路 abcda 应用 KVL, 则有

$$
u - \left(u + \frac {\partial u}{\partial x} \mathrm{d} x\right) = R _ {0} i \mathrm{d} x + L _ {0} \frac {\partial i}{\partial t} \mathrm{d} x
$$

![](images/page_478_image_4.jpg)

<details>
<summary>text_image</summary>

i
R₀dx
L₀dx
i+∂i/∂x dx
a
+
u
-
G₀dx
b
+
C₀dx
-
u+∂u/∂x dx
c
x
dx
</details>

图 18-5 均匀传输线的电路模型

略去二阶无穷小量并约去 dx 后, 得下列方程:

$$
\begin{array}{l} \left. - \frac {\partial u}{\partial x} = R _ {0} i + L _ {0} \frac {\partial i}{\partial t} \right\} \tag {18-1} \\ \left. - \frac {\partial i}{\partial x} = G _ {0} u + C _ {0} \left. \frac {\partial u}{\partial t} \right]\right. \\ \end{array}
$$

这就是均匀传输线方程,它是一组偏微分方程。根据边界条件(即始端和终端的情况)和初始条件(即时间起始时的条件),求出方程(18-1)的解,就可以得到电压u和电流i,它们将是x和t的函数。可见电压和电流不仅随时间变化,同时也随距离变化。这是分布电路与集总电路的一个显著区别。

## §18-3 均匀传输线方程的正弦稳态解

本节研究均匀传输线在始端电源角频率为  $\omega$  的正弦时间函数时电路的稳态分析。在这种情况下，沿线的电压、电流是同一频率的正弦时间函数，因此，可以用相量法分析沿线的电压和电流。于是有

$$
u (x, t) = \mathrm{Re} \left[ \sqrt {2} \stackrel {\circ} {U} (x) \mathrm{e} ^ {\mathrm{j} \omega t} \right]
$$

$$
i (x, t) = \mathrm{Re} [ \sqrt {2} \dot {I} (x) \mathrm{e} ^ {\mathrm{j} \omega t} ]
$$

其中  $\dot{U}(x)$  和  $\dot{I}(x)$  均为 x 的函数, 简写为  $\dot{U}$  和  $\dot{I}$ , 因而方程 (18-1) 可以写成以下形式:

$$
\left. \begin{array}{l} - \frac {\mathrm{d} \dot {U}}{\mathrm{d} x} = (R _ {0} + \mathrm{j} \omega L _ {0}) \dot {I} = Z _ {0} \dot {I} \\ - \frac {\mathrm{d} \dot {I}}{\mathrm{d} x} = (G _ {0} + \mathrm{j} \omega C _ {0}) \dot {U} = Y _ {0} \dot {U} \end{array} \right\} \tag {18-2}
$$

其中 $Z_0 = R_0 + \mathrm{j}\omega L_0$ 为单位长度的阻抗，$Y_0 = G_0 + \mathrm{j}\omega C_0$ 为单位长度的导纳。由于相量 $\dot{U}$ 和 $\dot{I}$ 仅为距离 $x$ 的函数，所以在式(18-1)中对 $u$ 和 $i$ 的偏导数可以写成全导数，这样，式(18-1)的偏微分方程组就成为式(18-2)的常微分方程组。将式(18-2)对 $x$ 取一次导数，得

$$
\begin{array}{l} - \frac {\mathrm{d} ^ {2} \dot {U}}{\mathrm{d} x ^ {2}} = Z _ {0} \frac {\mathrm{d} \dot {I}}{\mathrm{d} x} \\ - \frac {\mathrm{d} ^ {2} \dot {I}}{\mathrm{d} x ^ {2}} = Y _ {0} \frac {\mathrm{d} \dot {U}}{\mathrm{d} x} \\ \end{array}
$$

把式(18-2)中的 $\frac{d\dot{I}}{dx}$ 和 $\frac{d\dot{U}}{dx}$ 代入上式,便得到

$$
\frac {\mathrm{d} ^ {2} \dot {U}}{\mathrm{d} x ^ {2}} = Z _ {0} Y _ {0} \dot {U}
$$

$$
\frac {\mathrm{d} ^ {2} \dot {I}}{\mathrm{d} x ^ {2}} = Z _ {0} Y _ {0} \dot {I}
$$

令 $\gamma = \alpha +\mathrm{j}\beta = \sqrt{Z_0Y_0} = \sqrt{(R_0 + \mathrm{j}\omega L_0)(G_0 + \mathrm{j}\omega C_0)}$ ，代入上式后得

$$
\begin{array}{l} \frac {\mathrm{d} ^ {2} \dot {U}}{\mathrm{d} x ^ {2}} = \gamma^ {2} \dot {U} \\ \frac {\mathrm{d} ^ {2} \dot {I}}{\mathrm{d} x ^ {2}} = \gamma^ {2} \dot {I} \\ \end{array}
$$

$\gamma$ 称为传播常数。上列方程是常系数二阶线性微分方程。它们的通解具有下列形式:

$$
\left. \begin{array}{l} \dot {U} = A _ {1} \mathrm{e} ^ {- \gamma x} + A _ {2} \mathrm{e} ^ {\gamma x} \\ \dot {I} = B _ {1} \mathrm{e} ^ {- \gamma x} + B _ {2} \mathrm{e} ^ {\gamma x} \end{array} \right\} \tag {18-3}
$$

利用式(18-2)可以求得积分常数 $A_{1}$ 和 $B_{1}$ 及 $A_{2}$ 和 $B_{2}$ 之间的关系。由式(18-2)中的第一个方程得

$$
\begin{array}{l} \dot {I} = - \frac {1}{Z _ {0}} \frac {\mathrm{d} \dot {U}}{\mathrm{d} x} = - \frac {1}{Z _ {0}} (- A _ {1} \gamma \mathrm{e} ^ {- \gamma x} + A _ {2} \gamma \mathrm{e} ^ {\gamma x}) \\ = \frac {A _ {1}}{\sqrt {\frac {Z _ {0}}{Y _ {0}}}} \mathrm{e} ^ {- \gamma x} - \frac {A _ {2}}{\sqrt {\frac {Z _ {0}}{Y _ {0}}}} \mathrm{e} ^ {\gamma x} = B _ {1} \mathrm{e} ^ {- \gamma x} + B _ {2} \mathrm{e} ^ {\gamma x} \\ \end{array}
$$

令 $Z_{\mathrm{c}} = \sqrt{\frac{Z_0}{Y_0}}$ ，从上式中有 $B_{1} = \frac{A_{1}}{Z_{\mathrm{c}}}, B_{2} = -\frac{A_{2}}{Z_{\mathrm{c}}}$ 而电流

$$
\dot {I} = \frac {A _ {1}}{Z _ {\mathrm{c}}} \mathrm{e} ^ {- \gamma x} - \frac {A _ {2}}{Z _ {\mathrm{c}}} \mathrm{e} ^ {\gamma x}
$$

$Z_{c}$  称为特性阻抗或波阻抗。它和称为传播常数的  $\gamma$  都是复数。后面将会看到  $Z_{c}$  和  $\gamma$  可以用来表征均匀传输线的主要特性。

根据边界条件可以确定积分常数  $A_{1}$  和  $A_{2}$ ，可以分两种不同情况讨论。