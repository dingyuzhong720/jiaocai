# 第8章 相量法

原始 PDF 第 217–233 页。

![](../../raw/pages_0193-0224/images/page_216_image_0.jpg)

<details>
<summary>text_image</summary>

第八章
相量法
</details>

## 第八章 相量法

![](../../raw/pages_0193-0224/images/page_216_image_2.jpg)

![](../../raw/pages_0193-0224/images/page_216_image_3.jpg)

## 导读

对线性电路施加激励(独立电源)均为同频率的正弦时间函数,在电路达到稳态时,线性电路的所有响应(电压和电流)均为与激励具有相同频率的正弦时间函数,称电路为正弦稳态电路。

由第七章获知,含有储能元件的线性电路用线性常微分方程描述。施加正弦激励的线性电路的稳态响应,是线性常微分方程的特解,它是与激励具有相同频率的正弦时间函数。显然,对正弦稳态电路,采用微分方程求特解将非常困难。

1893年,工程师 C.P. 施泰因梅茨率先用约定的“符号”将正弦稳态电路的微(积)分方程的特解问题变换为复代数方程的求解问题,这种方法就是本章介绍的相量法。相量法将正弦稳态电路中的电压和电流(正弦时间函数)变换为用复数表示的电压相量和电流相量,将电路元件用复阻抗或复导纳表示,从而将时域的微分方程变换为复代数方程。显然,用相量法分析正弦稳态电路比用微分方程要容易得多。

本章简单介绍复数及其运算、正弦量、基尔霍夫定律的相量形式以及元件电压电流关系的相量形式，为后续各章正弦稳态电路的分析奠定基础。

相量法也是分析研究非正弦周期信号、任意信号和许多相关学科的理论基础之一。

本书第八章至第十三章都是分析研究正弦稳态电路的相关内容。

## §8-1 复数

复数及其运算是应用相量法的数学基础。本节仅作简要的介绍。

一个复数有多种表示形式。复数 F 的代数形式为

$$
F = a + j b
$$

式中  $j=\sqrt{-1}$  为虚单位。a 称为复数 F 的实部，b 称为复数 F 的虚部。复数 F 在复平面上是一个坐标点，常用原点至该点的向量表示，如图 8-1 所示。

根据图 8-1, 可得复数 F 的三角形式

---

194

第八章 相量法

$$
F = \mid F \mid (\cos \theta + \mathrm{j} \sin \theta)
$$

而复数 $F$ 的指数形式或极坐标形式为

$$
F = | F | \mathrm{e} ^ {\mathrm{j} \theta}, \quad F = | F | / \theta
$$

式中  $\left|F\right|$  为复数的模(值)， $\theta$  为复数的辐角，即  $\theta=\arg F$ 。 $\theta$  可以用弧度或度表示。 $\left|F\right|$  和  $\theta$  与 a 和 b 之间的关系为

$$
\mid F \mid = \sqrt {a ^ {2} + b ^ {2}}
$$

$$
\theta = \arctan \left(\frac {b}{a}\right)
$$

$$
a = | F | \cos \theta , \quad b = | F | \sin \theta
$$

![](../../raw/pages_0193-0224/images/page_217_image_10.jpg)

<details>
<summary>text_image</summary>

+j
b
F
θ
O
a
+1
</details>

图8-1 复数的表示

本书还常用到如下一些复数的概念, $\mathrm{Re}[F]$ 表示取复数F的实部,即

$$
\mathrm{Re} [ F ] = a
$$

Im[F]表示取复数F的虚部,即

$$
\operatorname{Im} [ F ] = b
$$

$F^{*}$  表示复数 F 的共轭复数, 即

$$
F ^ {*} = a - \mathrm{j} b \quad \text {或} \quad F ^ {*} = | F | / - \theta
$$

下面介绍复数的运算。复数的相加和相减必须用代数形式进行。例如，设

$$
F _ {1} = a _ {1} + \mathrm{j} b _ {1}, \quad F _ {2} = a _ {2} + \mathrm{j} b _ {2}
$$

则

$$
F _ {1} \pm F _ {2} = (a _ {1} + \mathrm{j} b _ {1}) \pm (a _ {2} + \mathrm{j} b _ {2})
$$

$$
= (a _ {1} \pm a _ {2}) + \mathrm{j} (b _ {1} \pm b _ {2})
$$

复数的相加和相减的运算也可以按平行四边形法在复平面上用向量的相加和相减求得,如图 8-2 所示。

![](../../raw/pages_0193-0224/images/page_217_image_24.jpg)

<details>
<summary>text_image</summary>

+j
F₁+F₂
F₂
O
+1
F₁
</details>

(a) $F_{1} + F_{2}$

![](../../raw/pages_0193-0224/images/page_217_image_26.jpg)

<details>
<summary>text_image</summary>

+j
F₁
F₂
F₁-F₂
O
+1
</details>

(b) $F_{1} - F_{2}$

图8-2 复数代数和的图解法

复数相乘用指数形式比较方便,即

$$
\begin{array}{l} F _ {1} F _ {2} = \left| F _ {1} \right| \mathrm{e} ^ {\mathrm{j} \theta_ {1}} \left| F _ {2} \right| \mathrm{e} ^ {\mathrm{j} \theta_ {2}} \\ = \mid F _ {1} \mid \mid F _ {2} \mid \mathrm{e} ^ {\mathrm{j} (\theta_ {1} + \theta_ {2})} \\ \end{array}
$$

所以

---

§ 8-1 复数

195

$$
\mid F _ {1} F _ {2} \mid = \mid F _ {1} \mid \mid F _ {2} \mid
$$

$$
\arg (F _ {1} F _ {2}) = \arg (F _ {1}) + \arg (F _ {2})
$$

两个复数的相乘,用代数形式有

$$
F _ {1} F _ {2} = (a _ {1} + \mathrm{j} b _ {1}) (a _ {2} + \mathrm{j} b _ {2})
$$

$$
= (a _ {1} a _ {2} - b _ {1} b _ {2}) + \mathrm{j} (a _ {1} b _ {2} + a _ {2} b _ {1})
$$

复数相除的运算为

$$
\frac {F _ {1}}{F _ {2}} = \frac {\left| F _ {1} \right| / \theta_ {1}}{\left| F _ {2} \right| / \theta_ {2}} = \frac {\left| F _ {1} \right|}{\left| F _ {2} \right|} / \left(\theta_ {1} - \theta_ {2}\right)
$$

所以

$$
\left| \frac {F _ {1}}{F _ {2}} \right| = \frac {\mid F _ {1} \mid}{\mid F _ {2} \mid}
$$

$$
\arg \left(\frac {F _ {1}}{F _ {2}}\right) = \arg (F _ {1}) - \arg (F _ {2})
$$

如用代数形式有

$$
\frac {F _ {1}}{F _ {2}} = \frac {a _ {1} + \mathrm{j} b _ {1}}{a _ {2} + \mathrm{j} b _ {2}} = \frac {(a _ {1} + \mathrm{j} b _ {1}) (a _ {2} - \mathrm{j} b _ {2})}{(a _ {2} + \mathrm{j} b _ {2}) (a _ {2} - \mathrm{j} b _ {2})}
$$

$$
= \frac {a _ {1} a _ {2} + b _ {1} b _ {2}}{\left(a _ {2}\right) ^ {2} + \left(b _ {2}\right) ^ {2}} + \mathrm{j} \frac {a _ {2} b _ {1} - a _ {1} b _ {2}}{\left(a _ {2}\right) ^ {2} + \left(b _ {2}\right) ^ {2}}
$$

式中 $a_2 - \mathrm{j}b_2$ 为 $F_{2}$ 的共轭复数 $F_{2}^{*}$ 。 $F_{2}F_{2}^{*}$ 的结果为实数，称为有理化运算。

图 8-3(a)(b)为复数乘、除的图解表示,从图上可以看出:复数乘、除表示为模的放大或缩小,辐角表示为逆时针旋转或顺时针旋转。

![](../../raw/pages_0193-0224/images/page_218_image_17.jpg)

<details>
<summary>text_image</summary>

+j
F₁F₂
θ₂
|F₂|F₁
F₁
θ₁
θ₂
O
+1
</details>

(a) $F_{1}F_{2}$

![](../../raw/pages_0193-0224/images/page_218_image_19.jpg)

<details>
<summary>text_image</summary>

+j
F₁
F₁/|F₂|
θ₂
F₁/F₂
θ₁
F₂
θ₂
O
+1
</details>

(b) $F_{1} / F_{2}$

图8-3 复数乘、除的图解示意

复数  $e^{j\theta}=1/\theta$  是一个模等于 1，辐角为  $\theta$  的复数。任意复数  $A=|A|e^{j\theta_{n}}$  乘以  $e^{j\theta}$  等于把复数 A 逆时针旋转一个角度  $\theta$ ，而 A 的模值不变，所以  $e^{j\theta}$  称为旋转因子。

根据欧拉公式,不难得出  $e^{j\frac{\pi}{2}}=j,e^{-j\frac{\pi}{2}}=-j,e^{j\pi}=-1$ 。因此“±j”和“-1”都可以看成旋

![](../../raw/pages_0193-0224/images/page_218_image_24.jpg)

<details>
<summary>natural_image</summary>

Pure technical line drawing of mechanical components without any text or symbols
</details>

---

196

第八章 相量法

转因子。例如一个复数乘以 j，等于把该复数在复平面上逆时针旋转  $\frac{\pi}{2}$ ；一个复数除以 j，等于该复数乘以 -j，因此等于把它顺时针旋转  $\frac{\pi}{2}$ 。

在复数运算中常有两个复数相等的运算。两个复数相等必须满足两个条件，如 $F_{1}=F_{2}$ 必须有

$$
\mathrm{Re} \left[ F _ {1} \right] = \mathrm{Re} \left[ F _ {2} \right], \quad \mathrm{Im} \left[ F _ {1} \right] = \mathrm{Im} \left[ F _ {2} \right]
$$

或者有

$$
\left| F _ {1} \right| = \left| F _ {2} \right|, \quad \arg (F _ {1}) = \arg (F _ {2})
$$

一个复数方程可以分解为两个实数方程。

例8-1 设 $F_{1} = 3 - \mathrm{j}4, F_{2} = 10 / 135^{\circ}$。求 $F_{1} + F_{2}$ 和 $\frac{F_1}{F_2}$。

解 用代数形式求复数的代数和,有

$$
F _ {2} = 1 0 \angle 1 3 5 ^ {\circ} = 1 0 (\cos 1 3 5 ^ {\circ} + j \sin 1 3 5 ^ {\circ})
$$

$$
= - 7. 0 7 + \mathrm{j} 7. 0 7
$$

$$
F _ {1} + F _ {2} = (3 - \mathrm{j} 4) + (- 7. 0 7 + \mathrm{j} 7. 0 7) = - 4. 0 7 + \mathrm{j} 3. 0 7
$$

转换为指数形式有

$$
\arg (F _ {1} + F _ {2}) = \arctan \left(\frac {3 . 0 7}{- 4 . 0 7}\right) = 1 4 3 ^ {\circ}
$$

$$
\mid F _ {1} + F _ {2} \mid = \frac {- 4 . 0 7}{\cos 1 4 3 ^ {\circ}} = \frac {3 . 0 7}{\sin 1 4 3 ^ {\circ}} = 5. 1
$$

即有

$$
F _ {1} + F _ {2} = 5. 1 / 1 4 3 ^ {\circ}
$$

$$
\frac {F _ {1}}{F _ {2}} = \frac {3 - \mathrm{j} 4}{- 7 . 0 7 + \mathrm{j} 7 . 0 7} = \frac {(3 - \mathrm{j} 4) (- 7 . 0 7 - \mathrm{j} 7 . 0 7)}{(- 7 . 0 7 + \mathrm{j} 7 . 0 7) (- 7 . 0 7 - \mathrm{j} 7 . 0 7)} = - 0. 4 9 5 + \mathrm{j} 0. 0 7 1
$$

或者

$$
\frac {F _ {1}}{F _ {2}} = \frac {3 - \mathrm{j} 4}{1 0 / 1 3 5 ^ {\circ}} = \frac {5 / - 5 3 . 1 ^ {\circ}}{1 0 / 1 3 5 ^ {\circ}} = 0. 5 / - 1 8 8. 1 ^ {\circ} = 0. 5 / 1 7 1. 9 ^ {\circ}
$$

## §8-2 正弦量

电路中按正弦规律变化的电压或电流,统称为正弦量。对正弦量的数学描述,可以采用 sine 函数,也可以用 cosine 函数。本书采用 cosine 函数。

图 8-4 表示一段电路中有正弦电流 i，在图示参考方向下，其数学表达式定义如下:

$$
i = I _ {\mathrm{m}} \cos (\omega t + \phi_ {i}) \tag {8-1}
$$

![](../../raw/pages_0193-0224/images/page_219_image_26.jpg)

图8-4 一段正弦电流电路

![](../../raw/pages_0193-0224/images/page_219_image_28.jpg)

正弦量

---

§ 8-2 正弦量

197

式中的 3 个常数  $I_{m}$ 、 $\omega$  和  $\phi_{i}$  称为正弦量的三要素。

$I_{m}$  称为正弦量的振幅, 它是正弦量在整个振荡过程中达到的最大值, 即  $\cos(\omega t + \phi_{i}) = 1$  时, 有

$$
i _ {\mathrm{max}} = I _ {\mathrm{m}}
$$

这也是正弦量的极大值。当  $\cos\left(\omega t+\phi_{i}\right)=-1$  时，将有最小值（也是极小值） $i_{\min}=-I_{m}$ 。 $i_{\max}-i_{\min}=2I_{m}$  称为正弦量的峰-峰值。

随时间变化的角度 $(\omega t+\phi_{i})$ 称为正弦量的相位,或称相角。 $\omega$ 称为正弦量的角频率,它是正弦量的相位随时间变化的角速度,即

$$
\omega = \frac {\mathrm{d}}{\mathrm{d} t} (\omega t + \phi_ {i})
$$

单位为 rad/s(弧度/秒)。它与正弦量的周期 T 和频率 f 之间的关系为

$$
\omega T = 2 \pi , \quad \omega = 2 \pi f, \quad f = \frac {1}{T}
$$

频率f的单位为1/s(1/秒)，称为Hz(赫兹，简称赫)。我国工业化生产的电能为正弦电压源，其频率为50 Hz，该频率称为工频。工程中还常以频率区分电路，如音频电路、高频电路、甚高频电路等。

$\phi_{i}$  是正弦量在 t=0 时刻的相位, 称为正弦量的初相位(角), 简称初相, 即

$$
\left(\dot {\omega} t + \phi_ {i}\right) \mid_ {t = 0} = \phi_ {i}
$$

初相的单位用弧度或度表示,通常在主值范围内取值,即  $\left|\phi_{i}\right| \leqslant 180^{\circ}$ 。初相与计时零点的选择有关。对任一正弦量,初相是允许任意指定的,但对于同一电路系统中的许多相关的正弦量,只能相对于一个共同的计时零点确定各自的相位。

正弦量的三要素是正弦量之间进行比较和区分的依据。

正弦量随时间变化的图形称为正弦波。图8-5是正弦电流 $i$ 的波形图 $(\phi_{i} > 0)$ 。横轴可以用时间 $t$ ，也可以用 $\omega t(\mathrm{rad})$ 表示。

![](../../raw/pages_0193-0224/images/page_220_chart_16.jpg)

<details>
<summary>line</summary>

| Parameter | Value |
| --- | --- |
| Peak Current (Im) | Im |
| Half-Value Interval (T/2) | \(2\pi\) |
| Phase Shift \((\phi i)\) | \(\phi i\) |
| Period (T) | T/2 |
| Half-Value Interval (T/2) | \(2\pi\) |
</details>

图 8-5 正弦量 i 的波形 ( $\phi_{i}>0$ )

正弦量乘以常数,正弦量的微分、积分,同频正弦量的代数和等运算,其结果仍为一个同频率的正弦量。正弦量的这个性质十分重要。

工程中常将周期电流或电压在一个周期内产生的平均效应换算为等效的直流量，

---

198

第八章 相量法

以衡量和比较周期电流或电压的效应,这一等效的直流量就称为周期量的有效值,用相对应的大写字母表示。如周期量i的有效值I定义如下:

$$
I \stackrel {\mathrm{def}} {=} \sqrt {\frac {1}{T} \int_ {0} ^ {T} i ^ {2} \mathrm{d} t} \tag {8-2}
$$

上式表示:周期量的有效值等于其瞬时值的平方在一个周期内积分的平均值的平方根,因此有效值又称为均方根值 $^{①}$ 。上式的定义是周期量有效值普遍适用的公式。当电流i是正弦量时,可以推出正弦量的有效值与正弦量的振幅之间的特殊关系。此时有

$$
\bar {I} = \sqrt {\frac {1}{T} \int_ {0} ^ {T} I _ {\mathrm{m}} ^ {2} \cos^ {2} (\omega t + \phi_ {i}) \mathrm{d} t}
$$

由于  $\cos^{2}(\omega t+\phi_{i})=\frac{1+\cos\left[2(\omega t+\phi_{i})\right]}{2}$ ，代入上式后得

$$
I = \frac {I _ {\mathrm{m}}}{\sqrt {2}} = 0. 7 0 7 I _ {\mathrm{m}}
$$

所以正弦量的有效值与其最大值之间有 $\sqrt{2}$ 关系，根据这一关系常将正弦量 $i$ 改写成如下的形式:

$$
i = \sqrt {2} I \cos \left(\omega t + \phi_ {i}\right)
$$

上式中  $I, \omega, \phi_{i}$  也可用来表示正弦量的三要素。正弦量的有效值与正弦量的频率和初相无关。工程中使用的交流电气设备铭牌上标出的额定电流、电压的数值，交流电压表、电流表显示的数字都是有效值。

电路中常引用“相位差”的概念描述两个同频正弦量之间的相位关系。例如，设两个同频正弦量电流 $i_{1}$ 、电压 $u_{2}$ 分别为

$$
i _ {1} = \sqrt {2} I _ {1} \cos (\omega t + \phi_ {i 1})
$$

$$
u _ {2} = \sqrt {2} U _ {2} \cos (\omega t + \phi_ {u 2})
$$

两个同频正弦量的相位差等于它们相位相减的结果。如设  $\varphi_{12}$  表示电流  $i_{1}$  与电压  $u_{2}$  之间的相位差，则有

$$
\varphi_ {1 2} = (\omega t + \phi_ {i 1}) - (\omega t + \phi_ {u 2}) = \phi_ {i 1} - \phi_ {u 2}
$$

相位差也是在主值范围内取值。上述结果表明:同频正弦量的相位差等于它们的初相之差，为一个与时间无关的常数。电路常采用“超（越）前”和“滞（落）后”等概念来说明两个同频正弦量相位比较的结果。

当 $\varphi_{12} > 0$ 时，称为 $i_1$ 超前 $u_{2}$；当 $\varphi_{12} < 0$ 时，称为 $i_1$ 滞后 $u_{2}$；当 $\varphi_{12} = 0$ 时，称为 $i_1$ 和 $u_{2}$ 同相；当 $|\varphi_{12}| = \frac{\pi}{2}$ 时，称为 $i_1$ 与 $u_{2}$ 正交；当 $|\varphi_{12}| = \pi$ 时，称为 $i_1, u_2$ 彼此反相。

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① root-mean-square value(r. m. s. v)。</span></small>

---

§ 8-3 相量法的基础

199

相位差可以通过观察波形来确定,如图8-6所示。在同一个周期内两个波形与横坐标轴的两个交点(正斜率过零点或负斜率过零点)之间的坐标值即为两者的相位差,先到达零点的为超前波。图中所示为 $i_{1}$ 滞后 $u_{2}$ 。相位差与计时零点的选取、改变无关。

由于正弦量的初相与设定的参考方向有关,当改设某一正弦量的参考方向时,则该正弦量的初相将改变  $\pi$ ,它与其他正弦量的相位差也将相应地改变  $\pi$ 。

![](../../raw/pages_0193-0224/images/page_222_chart_4.jpg)

<details>
<summary>line</summary>

| \(\omega t\) | u1 | u2 |
| --- | --- | --- |
| 0 | 0 | 0 |
| ~\(\pi/4\) | ~0.5 | ~0.8 |
| \(\pi/4\) | ~0.3 | ~0.6 |
| \(\pi/2\) | 0 | 0 |
| \(3\pi/4\) | ~-0.5 | ~-0.3 |
| \(\pi\) | ~-0.8 | ~-0.9 |
| \(5\pi/4\) | ~-0.3 | ~-0.5 |
| \(\pi\) | 0 | 0 |
</details>

图 8-6 同频正弦量的相位差

## §8-3 相量法的基础

相量法是分析研究正弦电流电路稳定状态的一种简单易行的方法。它是在数学理论和电路理论的基础上建立起来的一种系统方法。

根据电路的基本定律 VCR、KCL 和 KVL, 编写含有储能元件的线性非时变电路的电路方程时, 将获得一组常微(积)分方程。现以图 8-7 所示的 RLC 串联电路为例, 电路的 KVL 方程为

$$
u _ {R} + u _ {L} + u _ {C} = u _ {S}
$$

其中

$$
u _ {R} = R i, \quad u _ {L} = L \frac {\mathrm{d} i}{\mathrm{d} t}, \quad u _ {C} = \frac {1}{C} \int i \mathrm{d} t
$$

将上述元件的 VCR 代入 KVL 方程有

![](../../raw/pages_0193-0224/images/page_222_image_13.jpg)

<details>
<summary>text_image</summary>

i
R
L
+
uR
-
+
uL
-
C
+
uC
-
us
-
</details>

图8-7 RLC串联电路

$$
R i + L \frac {\mathrm{d} i}{\mathrm{d} t} + \frac {1}{C} \int i \mathrm{d} t = u _ {\mathrm{s}} \tag {8-3}
$$

由数学理论可知，当 $u_{\mathrm{s}}$ （激励）为正弦量时，上述微分方程中的电流变量 $i$ 的特解（响应的强制分量）也一定是与 $u_{\mathrm{s}}$ 同一频率的正弦量，反之亦然。这一重要结论具有普遍意义，即线性非时变电路在正弦电源激励下，各支路电压、电流的特解都是与激励同频率的正弦量，当电路中存在多个同频率的正弦激励时，该结论也成立。工程上将电路的这一特解状态称为正弦电流电路的稳定状态，简称正弦稳态。电路处于正弦稳态时，同频率的各正弦量之间，仅在有效值（或振幅）、初相上存在“差异和联系”，这种“差异和联系”正是正弦稳态分析求解中的关键问题。现以式(8-3)的求解为例，从理论上说明相量法的基础。

若已知式(8-3)中的正弦电源  $u_{s}$  为

$$
u _ {\mathrm{s}} = \sqrt {2} U _ {\mathrm{s}} \cos (\omega t + \phi_ {u})
$$

则电流 i 的特解将是与  $u_{s}$  同一频率的正弦量, 因此, 可设为

![](../../raw/pages_0193-0224/images/page_222_image_20.jpg)

<details>
<summary>natural_image</summary>

Technical line drawing of a mechanical assembly or joint (no visible text or symbols)
</details>

![](../../raw/pages_0193-0224/images/page_222_image_21.jpg)

相量法的基础

---

200

第八章 相量法

$$
i = \sqrt {2} I \cos (\omega t + \phi_ {i})
$$

式中  $I_{i}\phi_{i}$  为待求量。将上述正弦量代入式(8-3)后，则可将微分方程式(8-3)变换为

$$
R \sqrt {2} I \cos (\omega t + \phi_ {i}) - \omega L \sqrt {2} I \sin (\omega t + \phi_ {i}) + \frac {1}{\omega C} \sqrt {2} I \sin (\omega t + \phi_ {i}) = \sqrt {2} U _ {\mathrm{s}} \cos (\omega t + \phi_ {u}) (8 - 4)
$$

上述方程说明，正弦稳态电路方程是一组同频正弦函数描述的代数方程，电路基本定律所涉及的正弦电流、电压的运算，不会改变电压、电流同频正弦量的性质，即正弦量乘常数 $(Ri)$ 、正弦量的微分 $(u_{L})$ 、正弦量的积分 $(u_{C})$ 和同频正弦量的代数和（KCL、KVL）等运算，其结果仍是同频的正弦量，这就验证了前述的结论。可以看出，各同频正弦电压、电流之间，在有效值(振幅)、初相上的“差异和联系”寓于正弦函数描述的电压、电流表达式及电路方程中。无疑，求解和分析同频正弦函数所描述的电路方程，将能获得正确的结果或结论，但这一方法对于复杂电路将显得非常繁琐，使分析求解相当困难。根据欧拉公式，可将正弦函数用复指数函数表示，如前所述的正弦量 $u_{\mathrm{s}}$ 和 $i$ 可表示为

$$
u _ {\mathrm{s}} = \frac {1}{2} \left[ U _ {\mathrm{sm}} \mathrm{e} ^ {\mathrm{j} (\omega t + \phi_ {u})} + U _ {\mathrm{sm}} \mathrm{e} ^ {- \mathrm{j} (\omega t + \phi_ {u})} \right]
$$

$$
i = \frac {1}{2} \left[ I _ {\mathrm{m}} \mathrm{e} ^ {\mathrm{j} (\omega t + \phi_ {i})} + I _ {\mathrm{m}} \mathrm{e} ^ {- \mathrm{j} (\omega t + \phi_ {i})} \right]
$$

上述变换表明，一个正弦量可以分解为一对共轭的复指数函数。根据叠加定理和数学理论，只要对其中一个分量进行分析求解，就能写出全部结果。如取分量 $U_{\mathrm{sm}} \mathrm{e}^{\mathrm{j}(\omega t + \phi_u)}$ （激励），则对应的响应分量为 $I_{\mathrm{m}} \mathrm{e}^{\mathrm{j}(\omega t + \phi_i)}$，代入式(8-3)，注意到 $I_{\mathrm{m}} = \sqrt{2} I$ 和 $U_{\mathrm{sm}} = \sqrt{2} U_{\mathrm{s}}$，经整理后有

$$
R I \mathrm{e} ^ {\mathrm{j} \phi_ {i}} + \mathrm{j} \omega L I \mathrm{e} ^ {\mathrm{j} \phi_ {i}} - \mathrm{j} \frac {1}{\omega C} I \mathrm{e} ^ {\mathrm{j} \phi_ {i}} = U _ {\mathrm{s}} \mathrm{e} ^ {\mathrm{j} \phi_ {u}} \tag {8-5}
$$

由上述代数方程求得

$$
I \mathrm{e} ^ {\mathrm{j} \phi_ {i}} = \frac {U _ {\mathrm{s}} \mathrm{e} ^ {\mathrm{j} \phi_ {u}}}{R + \mathrm{j} \omega L - \mathrm{j} \frac {1}{\omega C}}
$$

该结果用复数形式表述了正弦量 $i$ 除频率 $\omega$ 外的另两个要素 $I$ (有效值) 和 $\phi_i$ (初相), 因此, 根据正弦量的 3 个要素就可以直接写出正弦量 $i$ 的表达式。这表明方程式(8-5)在理论上和实际上已足以满足正弦稳态分析的需要, 不需要再求解另一分量的结果按欧拉公式写出正弦量 $i$。

上述变换只是数学形式的变换,与式(8-4)相比,并无实质性的区别,但在形式上实现了非常有益的转换,它将与时间有关的同频的正弦函数的电路方程转换为与时间无关的复代数形式的电路方程。更重要的是,它将正弦稳态中全部同频的正弦电压、电流转换为由各正弦量的有效值和初相组合成的复数表示,如 $Ie^{j\phi_{i}}$ 、 $U_{s}e^{j\phi_{u}}$ ,使同频的各正弦量在有效值、初相上的“差异和联系”,在电路方程中表述得更清晰、更直观和更简

---

§ 8-3 相量法的基础

201

单,这将大大简化对正弦稳态的表述和分析求解的过程。

电路理论中将式(8-5)中与正弦量 $u_{\mathrm{s}}$ 、 $i$ 关联的复数 $U_{\mathrm{s}}\mathrm{e}^{\mathrm{j}\phi_{\mathrm{u}}}$ 和 $I\mathrm{e}^{\mathrm{j}\phi_{i}}$ 定义为正弦量$u_{\mathrm{s}},i$ 对应的相量，并用对应的带“·”（点）符号的大写字母表示，如上述的正弦电压 $u_{\mathrm{s}}$ 和正弦电流 $i$ 对应的相量表示分别为

$$
\dot {U} _ {\mathrm{s}} \stackrel {\mathrm{def}} {=} U _ {\mathrm{s}} \mathrm{e} ^ {\mathrm{j} \phi_ {u}} = U _ {\mathrm{s}} / \phi_ {u}
$$

$$
\dot {I} \stackrel {\mathrm{def}} {=} I \mathrm{e} ^ {\mathrm{j} \phi_ {i}} = I / \phi_ {i}
$$

即正弦量的对应相量是一个复数,它的模为正弦量的有效值,它的辐角为正弦量的初相。式中  $\dot{U}_{s}$ 、 $\dot{I}$  中的“·”(点)号,既表示这一复数与正弦量关联的特殊身份,以区别于一般的复数,同时也表示区别于正弦量的有效值。正弦量对应的相量可直接根据上述定义写出。相量在复平面上表示的图形称为相量图,如图8-8所示为正弦电压  $u_{s}$  对应的相量  $\dot{U}_{s}$  的相量图。

![](../../raw/pages_0225-0256/images/page_224_image_7.jpg)

<details>
<summary>text_image</summary>

+j
Ûs
φu
O
+1
</details>

图8-8 相量 $\dot{U}_{\mathrm{s}}$ 的相量图

电路中有时也用正弦量的振幅表示相量的模,称为振幅相量,如有

$$
\dot {U} _ {\mathrm{sm}} \stackrel {\mathrm{def}} {=} U _ {\mathrm{sm}} \mathrm{e} ^ {\mathrm{j} \phi_ {u}} = U _ {\mathrm{sm}} \Big / \phi_ {u}
$$

$$
\dot {I} _ {\mathrm{m}} \stackrel {\mathrm{def}} {=} I _ {\mathrm{m}} \mathrm{e} ^ {\mathrm{j} \phi_ {i}} = I _ {\mathrm{m}} \Big / \phi_ {i}
$$

学习时要注意两者的区别。

本节的论述,仅从理论上向读者展示相量法的“来龙去脉”,以利于学习掌握。下一节将在此基础上加以归纳总结,系统构建电路基本定律的相量形式,可不经变换直接获得所需要的相量(复数)形式的电路方程。

例 8-2 写出下列正弦电流对应的相量

$$
i _ {1} = 1 4. 1 4 \cos (3 1 4 t + 3 0 ^ {\circ}) \mathrm{A}
$$

$$
i _ {2} = - 1 4. 1 4 \sin (1 0 ^ {3} t - 6 0 ^ {\circ}) \mathrm{A}
$$

解 本书根据国家标准,统一用 cosine 函数表示正弦量。因此,电流  $i_{2}$  的表达式应改写为

$$
i _ {2} = - 1 4. 1 4 \cos (1 0 ^ {3} t - 6 0 ^ {\circ} - 9 0 ^ {\circ}) \mathrm{A}
$$

$$
= - 1 4. 1 4 \cos (1 0 ^ {3} t - 1 5 0 ^ {\circ}) \mathrm{A}
$$

电流相量可按定义直接写出

$$
\dot {I} _ {1} = \frac {1 4 . 1 4}{\sqrt {2}} / 3 0 ^ {\circ} \mathrm{A} = 1 0 / 3 0 ^ {\circ} \mathrm{A}
$$

$$
\dot {I} _ {2} = \frac {- 1 4 . 1 4}{\sqrt {2}} / - 1 5 0 ^ {\circ} \mathrm{A} = 1 0 / 3 0 ^ {\circ} \mathrm{A}
$$

相量与正弦量之间不是相等的关系,因此,下面的写法是错误的

---

![](../../raw/pages_0225-0256/images/page_225_image_0.jpg)

<details>
<summary>natural_image</summary>

Pure technical line drawing of intersecting lines and shapes without any text, numbers, or symbols
</details>

202

第八章 相量法

$$
i _ {1} = 1 4. 1 4 \cos (3 1 4 t + 3 0 ^ {\circ}) \mathrm{A} = 1 0 / 3 0 ^ {\circ} \mathrm{A}
$$

相量与频率无关。由相量反求正弦量的表达式时必须知道  $\omega$  才能写出。本例中  $\dot{I}_{1} = \dot{I}_{2}$  没有实际意义，因为相量之间所表示的运算关系只能在同频的正弦量中使用。

例 8-3 求例 8-2 中正弦电流  $i_{1}$ 、 $i_{2}$  的微分及其相量。

解 正弦电流  $i_{1}$ 、 $i_{2}$  微分的时域形式的结果为

$$
y _ {1} = \frac {\mathrm{d} i _ {1}}{\mathrm{d} t} = - 1 0 \sqrt {2} \times 3 1 4 \sin (3 1 4 t + 3 0 ^ {\circ}) = 1 0 \sqrt {2} \times 3 1 4 \cos (3 1 4 t + 3 0 ^ {\circ} + 9 0 ^ {\circ})
$$

$$
y _ {1} = \frac {\mathrm{d} i _ {2}}{\mathrm{d} t} = - 1 0 \sqrt {2} \times 1 0 ^ {3} \cos \left(- 1 0 ^ {3} t - 6 0 ^ {\circ}\right) = - 1 0 \sqrt {2} \times 1 0 ^ {3} \cos \left(- 1 0 ^ {3} t - 6 0 ^ {\circ} + 1 8 0 ^ {\circ}\right)
$$

微分结果是与原函数同频的正弦量,直接根据正弦量表达式写出其相量,但正弦量必须转换为 cosine 函数表示。 $y_{1}$ 、 $y_{2}$  对应的有效值相量分别为

$$
\dot {Y} _ {1} = 3 1 4 0 / 1 2 0 ^ {\circ} = \mathrm{j} \omega_ {1} \dot {I} _ {1}
$$

$$
\dot {Y} _ {2} = 1 0 ^ {4} / 1 2 0 ^ {\circ} = \mathrm{j} \omega_ {2} \dot {I} _ {2}
$$

本例表明,正弦量的微分是与原正弦量同频率的正弦量,其对应的相量等于原正弦量 $i_{1}$ (或 $i_{2}$ )对应的相量 $\dot{I}_{1}$ (或 $\dot{I}_{2}$ )乘以 $j\omega_{1}$ (或 $j\omega_{2}$ )。

## §8-4 电路定律的相量形式

在上一节的理论叙述中,已经得到一个重要的结论,即在线性非时变的正弦稳态电路中,全部电压、电流都是同一频率的正弦量。本节将在此基础上,直接用相量通过复数形式的电路方程描述电路的基本定律 VCR、KCL 和 KVL,称为电路定律的相量形式。

KCL 的相量形式:

对电路中任一节点有

$$
i _ {1} + i _ {2} + i _ {3} + \dots + i _ {k} + \dots = 0 \quad \text {或} \quad \sum i = 0
$$

当式中的电流全部都是同频率的正弦量时,则可变换为相量形式为

$$
\dot {I} _ {1} + \dot {I} _ {2} + \dot {I} _ {3} + \dots + \dot {I} _ {k} + \dots = 0 \quad \text {或} \quad \sum \dot {I} = 0
$$

即任一节点上同频的正弦电流的对应相量的代数和为零。

KVL 的相量形式:

对电路中任一回路有

$$
u _ {1} + u _ {2} + u _ {3} + \dots + u _ {k} + \dots = 0 \quad \text {或} \quad \sum u = 0
$$

当式中的电压全都是同频的正弦量时,可变换成相量形式为

$$
\dot {U} _ {1} + \dot {U} _ {2} + \dot {U} _ {3} + \dots + \dot {U} _ {k} + \dots = 0 \quad \text {或} \quad \sum \dot {U} = 0
$$

即任一回路中同频的正弦电压的对应相量的代数和为零。

电阻、电感和电容元件的 VCR 的相量形式:

![](../../raw/pages_0225-0256/images/page_225_image_28.jpg)

电路定律的相量形式

---

§ 8-4 电路定律的相量形式

203

对于图 8-9(a) 所示电阻 R，当有正弦电流  $i_{R}=\sqrt{2}I_{R}\cos(\omega t+\phi_{i})$  通过时，根据欧姆定律，电压-电流的时域关系为

$$
u _ {R} = R i _ {R} = \sqrt {2} R I _ {R} \cos (\omega t + \phi_ {i})
$$

说明电阻上的电压、电流都是同频的正弦量。令电压相量为  $\dot{U}_{R}=U_{R}\angle\phi_{u}$ ，则相量形式有

$$
\dot {U} _ {R} = R I _ {R} \underline {{{{\phi_ {i}}}}} = R \dot {I} _ {R} \quad (\text {或} \dot {I} _ {R} = G \dot {U} _ {R})
$$

$$
U _ {R} = R I _ {R} \quad (\text {或} I _ {R} = G U _ {R})
$$

$$
\phi_ {u} = \phi_ {i}
$$

它们的有效值仍符合欧姆定律，而辐角相等，即电压、电流同相。图8-9(b)为电阻的相量模型，图8-9(c)是其电压、电流的相量图，它们在同一个方向的直线上（相位差为零）。

![](../../raw/pages_0225-0256/images/page_226_image_10.jpg)

(a)

![](../../raw/pages_0225-0256/images/page_226_image_12.jpg)

(b)

![](../../raw/pages_0225-0256/images/page_226_image_14.jpg)

<details>
<summary>text_image</summary>

+j
ÛR
İR
φu
φi
O
+1
</details>

(c)

图8-9 电阻中的电压、电流

对于图 8-10(a) 所示的电感 L 中, 当有正弦电流  $i_{L}=\sqrt{2}I_{L}\cos(\omega t+\phi_{i})$  通过时, 根据电感的电压-电流的时域关系有

$$
\begin{array}{l} u _ {L} = L \frac {\mathrm{d} i _ {L}}{\mathrm{d} t} = - \sqrt {2} \omega L I _ {L} \sin (\omega t + \phi_ {i}) \\ = \sqrt {2} \omega L I _ {L} \cos \left(\omega t + \phi_ {i} + 9 0 ^ {\circ}\right) \\ \end{array}
$$

说明电感 L 上的电压、电流为同频正弦量。令电压相量为  $\dot{U}_{L}=U_{L}/\phi_{u}, u_{L}$  的表达式变换后的相量形式为

$$
\dot {U} _ {L} = \mathrm{j} \omega L \dot {I} _ {L}
$$

$$
U _ {L} = \omega L I _ {L}
$$

$$
\phi_ {u} = \phi_ {i} + 9 0 ^ {\circ}
$$

电压、电流有效值之间的关系类似于欧姆定律，但与角频率 $\omega$ 有关，其中与频率成正比的 $\omega L$ 具有与电阻相同的量纲 $[\Omega]$，称为感抗，这样命名表示它与电阻有本质上的差别，$-\frac{1}{\omega L}$ 称为感纳，电感 $L$ 上的电压将跟随频率变化，当 $\omega = 0$ 时（直流），$\omega L = 0, u_L = 0$，电感相当于短路。当 $\omega = \infty$ 时，$\omega L \to \infty, i = 0$，电感相当于开路，在相位上电压超前电流 $90^\circ$。图8-10(b)是电感的相量模型，图8-10(c)是电感电压、电流的相量图。

---

204

第八章 相量法

![](../../raw/pages_0225-0256/images/page_227_image_3.jpg)

(a)

![](../../raw/pages_0225-0256/images/page_227_image_5.jpg)

(b)

![](../../raw/pages_0225-0256/images/page_227_image_7.jpg)

<details>
<summary>text_image</summary>

+j
ÛL
φu
O
φi
+1
ÎL
</details>

(c)

图 8-10 电感中的电压、电流

对于图 8-11(a) 所示的电容 C，它的电压、电流关系的相量形式与电感 L 类似。当有正弦电流  $i_{c}=\sqrt{2}I_{c}\cos(\omega t+\phi_{i})$  通过时，其时域形式的关系为

$$
u _ {c} = \frac {1}{C} \int i _ {c} \mathrm{d} t = \sqrt {2} \frac {1}{\omega C} I _ {c} \sin \left(\omega t + \phi_ {i}\right)
$$

说明电容上的电压、电流为同频的正弦量，电压、电流关系的相量形式为

$$
\dot {U} _ {c} = - \mathrm{j} \frac {1}{\omega C} \dot {I} _ {c}
$$

$$
U _ {c} = \frac {1}{\omega C} I _ {c}
$$

$$
\phi_ {u} = \phi_ {i} - 9 0 ^ {\circ}
$$

电压、电流有效值之间的关系类似于欧姆定律，但与频率 $\omega$ 有关，式中与频率成反比的 $-\frac{1}{\omega C}$ 具有与电阻相同的量纲 $[\Omega]$，称为容抗，$\omega C$ 称为容纳。电容电压将随频率变化而变化，当 $\omega = 0$（直流）时，$\frac{1}{\omega C} = \infty, i_{C} = 0$，电容相当于开路。当 $\omega = \infty$ 时，$\frac{1}{\omega C} \rightarrow 0, u_{C} = 0$，电容相当于短路。在相位上，电流超前电压 $90^{\circ}$。图8-11(b)(c)分别是电容的相量模型和电压、电流的相量图。

![](../../raw/pages_0225-0256/images/page_227_image_17.jpg)

(a)

![](../../raw/pages_0225-0256/images/page_227_image_19.jpg)

(b)

![](../../raw/pages_0225-0256/images/page_227_image_21.jpg)

<details>
<summary>text_image</summary>

+j
îc
φi
O
+1
Ûc
φu
</details>

(c)

图 8-11 电容上的电压、电流

如果(线性)受控源的控制电压或电流是正弦量,则受控源的电压或电流将是同一频率的正弦量。现以图8-12(a)所示的VCCS为例说明,此时有

$$
i _ {j} = g u _ {k}
$$

---

§ 8-4 电路定律的相量形式

205

1. 用 $\mathrm{H}_{2}$ 气相分离的气体，用于化学分析（如: $\mathrm{H}_{2}$ 和 $\mathrm{H}_{2}$ 气相分离的气体）。

相量形式为

$$
\dot {I} _ {j} = g \dot {U} _ {k}
$$

图 8-12(b)为其相量形式的电路图(其他形式的受控源与其类似)。

![](../../raw/pages_0225-0256/images/page_228_image_6.jpg)

图8-12 VCCS的相量表示

用复数代数方程描述电路定律的相量形式(略去变换过程)是相量法体系的基础,其中 VCR 的相量形式对正确应用相量法十分重要,不仅要用到电阻、感抗和容抗,或者电导、感纳和容纳等概念,而且要特别注意电压、电流之间的相位差。

例 8-4 图 8-13(a) 所示电路中， $i_{S}=5\sqrt{2}\cos(10^{3}t+30^{\circ})A$ ， $R=30\Omega, L=0.12H$ ， $C=12.5\mu F$ ，求电压  $u_{ad}$  和  $u_{bd}$ 。

解 为了帮助理解和避免错误,可根据原电路图画出对应的相量模型,它是将时域中的正弦电压、电流用相量标记,电路中的电阻、电感和电容元件根据 VCR 的相量形式分别用复数形式的  $R_{1}$ 、 $j\omega L$  和  $\frac{1}{j\omega C}$  标记,而其他与原电路图相同。根据相量形式的电路图就可以直接写出相量形式的电路方程。

图 8-13(a) 所示电路相对应的相量形式的电路图如图 8-13(b) 所示。图中  $\dot{I}_{s}=5\angle30^{\circ}A, j\omega L=j120\Omega, -j\frac{1}{\omega C}=-j80\Omega$ 。

![](../../raw/pages_0225-0256/images/page_228_image_12.jpg)

图8-13 例8-4图

根据元件的 VCR 的相量形式有

$\dot{U}_{R}=R\dot{I}=150/30^{\circ}V$  （与  $\dot{I}_{s}$  相同）

$\dot{U}_L = \mathrm{j}\omega L\dot{I} = 600 / 120^{\circ}\mathrm{V}$ （超前 $\dot{I}_{\mathrm{a}}90^{\circ}$ ）

$\dot{U}_{c} = -\mathrm{j}\frac{1}{\omega C}\dot{I} = 400 / - 60^{\circ}\mathrm{V}$ （滞后 $\dot{I}_{s}90^{\circ}$ ）

---

206

第八章 相量法

根据 KVL, 有

$$
\dot {U} _ {\mathrm{bd}} = \dot {U} _ {L} + \dot {U} _ {c} = (6 0 0 / 1 2 0 ^ {\circ} + 4 0 0 / - 6 0 ^ {\circ}) \mathrm{V} = 2 0 0 / 1 2 0 ^ {\circ} \mathrm{V}
$$

$$
\dot {U} _ {\mathrm{ad}} = \dot {U} _ {R} + \dot {U} _ {\mathrm{bd}} = (1 5 0 / 3 0 ^ {\circ} + 2 0 0 / 1 2 0 ^ {\circ}) \mathrm{V} = 2 5 0 / 8 3. 1 3 ^ {\circ} \mathrm{V}
$$

所以 $u_{\mathrm{bd}} = 200\sqrt{2}\cos (10^3 t + 120^\circ)\mathrm{V}$

$$
u _ {\mathrm{ad}} = 2 5 0 \sqrt {2} \cos (1 0 ^ {3} t + 8 3. 1 3 ^ {\circ}) \mathrm{V}
$$

应用相量法分析正弦稳态电路时,其电路方程的相量形式与电阻电路相似,因此,线性电阻电路的各种分析方法和电路定理可推广用于线性电路的正弦稳态分析,差别仅在于所得电路方程为以相量形式表示的代数方程以及用相量形式描述的电路定理,而计算则为复数运算。

通过例 8-4 可以看出, 当串联电路中同时有电感、电容时, 其结果与电阻电路相比, 存在明显的差异, 这是因为感抗和容抗不仅与频率的关系彼此相反, 而且在串联时有互相抵消的作用。在一定的条件下, 电感、电容的电压可能会出现高于总电压的现象, 如本例中  $U_{C}$ 、 $U_{L}$  都比总电压  $U_{ad}$  高很多, 这些现象在电阻串联电路中是不可能出现的。这些特点在学习中要特别注意分析。

图 8-13(b) 所示的电路相量模型已集数学理论和电路定律于一体, 直接用它对电路的正弦稳态响应进行分析研究, 自然要方便快捷, 而且在方法上完全可以仿照电阻电路。

例 8-5 图 8-14 所示为正弦稳态电路，电路中的仪表为交流电流表，其仪表所指示的读数为电流的有效值，其中电流表  $A_{1}$  的读数为 5A，电流表  $A_{2}$  的读数为 20A，电流表  $A_{3}$  的读数为 25A。求电流表 A 和  $A_{4}$  的读数。

解 图中各交流电流表的读数就是仪表所在支路的电流相量的模(有效值),但初相未知。

![](../../raw/pages_0225-0256/images/page_229_image_13.jpg)

<details>
<summary>text_image</summary>

I
A
I4
A4
A3
+
Us
-
R
A1
I1
A2
jωL
I2
1
jωC
I3
</details>

图8-14 例8-5图

显然,如果设并联支路的电压相量为参考相量,即令  $\dot{U}_{s}=U_{s}/0^{\circ}V$  作为参考相量,则根据元件的 VCR 相对  $\dot{U}_{s}$  就能很方便地确定这些并联支路中电流的初相。它们分别为

$$
\dot {I} _ {1} = 5 / 0 ^ {\circ} \mathrm{A} (\text {与} \dot {U} _ {\mathrm{s}} \text {同相})
$$

$$
\dot {I} _ {2} = - \mathrm{j} 2 0 \mathrm{A} (\text {滞后} \dot {U} _ {\mathrm{s}} 9 0 ^ {\circ})
$$

$$
\dot {I} _ {3} = \mathrm{j} 2 5 \mathrm{A} (\text {超前} \dot {U} _ {\mathrm{s}} 9 0 ^ {\circ})
$$

根据 KCL, 有

$$
\dot {I} = \dot {I} _ {1} + \dot {I} _ {2} + \dot {I} _ {3} = (5 + \mathrm{j} 5) \mathrm{A} = 7. 0 7 / 4 5 ^ {\circ} \mathrm{A}
$$

$$
\dot {I} _ {4} = \dot {I} _ {2} + \dot {I} _ {3} = \mathrm{j} 5 \mathrm{A} = 5 / 9 0 ^ {\circ} \mathrm{A}
$$

所求电流表的读数为

表 A:7.07 A， 表  $A_{4}:5$  A

在本章最后,有必要简单讨论电力技术发展历程上著名的交直流之争和当代高压

---

习题

207

直流输电。19世纪末，由于正弦交流电在交流发电机、交流电动机等方面的优势和容易经过变压器变压实现高压输电，交流电战胜了直流电。所以100多年来，交流电在电力系统中占据统治地位。然而随着电力电子技术的发展，可以采用高压直流输电。由于高压直流输电效率更高，直流输电在20世纪80年代重新登上历史舞台。虽然当代的发电、配电均采用交流电，但在输电方面，已经形成了交流输电和直流输电并存的局面。所以，电力技术发展也是螺旋式的和波浪式的，并不是一成不变的。

![](../../raw/pages_0225-0256/images/page_230_image_3.jpg)

## 思考题

8-1 何谓正弦稳态电路？对激励有何要求？响应是何种形式的时间函数？为什么？
8-2 正弦量的初相位为何在主值范围内取值,而两个正弦量的相位差也是在主值范围内取值?
8-3 对于正弦稳态电路,为什么可以采用相量法分析?是否可以在时域进行分析?
8-4 对于电感元件,为什么电压相量超前电流相量 $\frac{\pi}{2}$ ? 对于电容元件,为什么电流相量超前电压相量 $\frac{\pi}{2}$ ?

8-5 随着正弦激励频率的增加,感抗和容抗如何变化?

![](../../raw/pages_0225-0256/images/page_230_image_11.jpg)

## 习题

8-1 将下列复数化为极坐标形式:

(1) $F_{1} = -5 - \mathrm{j}5$; (2) $F_{2} = -4 + \mathrm{j}3$; (3) $F_{3} = 20 + \mathrm{j}40$; (4) $F_{4} = \mathrm{j}10$; (5) $F_{5} = -3$; (6) $F_{6} = 2.78 - \mathrm{j}9.20$。

8-2 将下列复数化为代数形式:

(1) $F_{1}=10\angle-73^{\circ}$; (2) $F_{2}=15\angle112.6^{\circ}$; (3) $F_{3}=1.2\angle52^{\circ}$; (4) $F_{4}=10\angle-90^{\circ}$; (5) $F_{5}=5\angle-180^{\circ}$; (6) $F_{6}=10\angle-135^{\circ}$。

8-3 若  $100/0^{\circ}+A/60^{\circ}=175/\varphi$ ，求 A 和  $\varphi$ 。

8-4 求题 8-1 中的  $F_{2} \cdot F_{6}$  和  $\frac{F_{2}}{F_{6}}$ 。

8-5 求题 8-2 中的  $F_{1}+F_{5}$  和  $-F_{1}+F_{5}$ 。

8-6 已知 $F_{1} = \left|F_{1}\right|\angle 60^{\circ},F_{2} = -7.07 - \mathrm{j}7.07$ 。求 $\left|F_1 + F_2\right|$ 最小时的 $F_{1}$ 。

8-7 若已知两个同频正弦电压的相量分别为  $\dot{U}_{1}=50/30^{\circ}V,\dot{U}_{2}=-100/-150^{\circ}V$ ，其频率  $f=100\ Hz$ 。求:

(1)  $u_{1}$ 、 $u_{2}$  的时域形式。
(2) $u_{1}$ 与 $u_{2}$ 的相位差。

---

208

第八章 相量法

8-8 已知一段电路的电压、电流为

$$
u = 1 0 \sin (1 0 ^ {3} t - 2 0 ^ {\circ}) \mathrm{V}
$$

$$
i = 2 \cos (1 0 ^ {3} t - 5 0 ^ {\circ}) \mathrm{A}
$$

(1) 画出它们的波形图, 求出它们的有效值、频率 f 和周期 T。
(2) 写出它们的相量和画出其相量图, 求出它们的相位差。
(3) 如把电压 u 的参考方向反向, 重新回答问题(1)和(2)。

8-9 已知题 8-9 图所示 3 个电压源的电压分别为

$$
u _ {\mathrm{a}} = 2 2 0 \sqrt {2} \cos (\omega t + 1 0 ^ {\circ}) \mathrm{V}
$$

$$
u _ {\mathrm{b}} = 2 2 0 \sqrt {2} \cos (\omega t - 1 1 0 ^ {\circ}) \mathrm{V}
$$

$$
u _ {\mathrm{c}} = 2 2 0 \sqrt {2} \cos (\omega t + 1 3 0 ^ {\circ}) \mathrm{V}
$$

![](../../raw/pages_0225-0256/images/page_231_image_14.jpg)

<details>
<summary>text_image</summary>

- uₐ +
a
+ uₐₑ
- uₑ +
b
+ uₑₑ
- u꜀ +
c
</details>

题8-9图

(1) 求 3 个电压的和。(2) 求 $u_{\mathrm{ab}}$、$u_{\mathrm{bo}}$。(3) 画出它们的相量图。

8-10 已知题 8-10 图(a)中电压表读数为  $V_{1}:30V, V_{2}:60V$ ; 题 8-10 图(b)中的  $V_{1}:15V, V_{2}:80V, V_{3}:100V$  (电压表的读数为正弦电压的有效值)。求图中电压  $u_{s}$  的有效值  $U_{s}$ 。

![](../../raw/pages_0225-0256/images/page_231_image_18.jpg)

<details>
<summary>text_image</summary>

V₁
+
us
-
R
L
V₂
</details>

(a)

![](../../raw/pages_0225-0256/images/page_231_image_20.jpg)

<details>
<summary>text_image</summary>

V₁
V₂
R
L
C
uₛ
+
-
V₃
</details>

(b)

题8-10图

8-11 如果维持例 8-5 图 8-14 所示电路中  $A_{1}$  的读数不变, 而把电源的频率提高一倍, 求电流表 A 的读数。
8-12 对 RC 并联电路做如下 2 次测量: (1) 端口加 120 V 直流电压 ( $\omega=0$ ) 时, 输入电流为 4 A; (2) 端口加频率为 50 Hz, 有效值为 120 V 的正弦电压时, 输入电流有效值为 5 A。求 R 和 C 的值。

8-13 某一元件的电压、电流(关联方向)分别为下述4种情况时,它可能是什么元件?

(1) $\left\{ \begin{array}{l} u = 10 \cos (10t + 45^{\circ}) \mathrm{~V} \\ i = 2 \sin (10t + 135^{\circ}) \mathrm{~A} \end{array} \right.$;

(2) $\left\{ \begin{array}{l} u = 10 \sin (100t) \mathrm{~V} \\ i = 2 \cos (100t) \mathrm{~A} \end{array} \right.$;

(3)  $\left\{\begin{aligned}u&=-10\cos t\ V\\ i&=-\sin t\ A\end{aligned}\right.$ ;

(4).  $\left\{\begin{aligned}u=10\cos(314t+45^{\circ})&V\\ i=2\cos(314t)&A\end{aligned}\right.$

8-14 电路由电压源  $u_{\mathrm{s}}=100\cos(10^{3}t)$  V 及 R 和 L=0.025H 串联组成，电感端电压的有效值为 25 V。求 R 值和电流的表达式。

8-15 已知题 8-15 图所示电路中  $I_{1}=I_{2}=10\ A$ 。求  $\dot{I}$  和  $\dot{U}_{s}$ 。

---

习题

209

1. 工程图

8-16 题 8-16 图所示电路中  $\dot{I}_{s}=2\angle0^{\circ}A$ 。求电压  $\dot{U}$ 。

![](../../raw/pages_0225-0256/images/page_232_image_4.jpg)

<details>
<summary>text_image</summary>

i
j10 Ω
+
Ûs
-
i1
10 Ω
i2
</details>

题8-15图

![](../../raw/pages_0225-0256/images/page_232_image_6.jpg)

<details>
<summary>text_image</summary>

İs
+
Ü
-
1 Ω
-j0.5 Ω
j1 Ω
</details>

题 8-16 图

8-17 电路如题8-17图所示。已知 $C = 1\mu \mathrm{F}, L = 1\mu \mathrm{H}, u_{\mathrm{s}} = 1.414\cos (10^{6}t + \phi_{u})\mathrm{V}$ 。当电路稳态时，在 $t = t_{1}$ 时刻打开开关，有 $i_{L}(t_{1}) = 0.6786\mathrm{A}$，求 $t\geqslant t_{1}$ 时的电流 $i_{L}$。

8-18 已知题 8-18 图中 $U_{\mathrm{s}} = 10 \, \mathrm{V}$ (直流), $L = 1 \, \mu \mathrm{H}$, $R_{1} = 1 \, \Omega$, $i_{\mathrm{s}} = 2 \cos(10^{6} t + 45^{\circ}) \, \mathrm{A}$。用叠加定理求电压 $u_{C}$ 和电流 $i_{L}$。

![](../../raw/pages_0225-0256/images/page_232_image_10.jpg)

<details>
<summary>text_image</summary>

R
1 Ω
i
iL
+
us
-
C
iC
S(t=t1)
L
</details>

题 8-17 图

![](../../raw/pages_0225-0256/images/page_232_image_12.jpg)

<details>
<summary>text_image</summary>

C
+
uC
-
L
iL
R2
+
Us
-
R1
iS
</details>

题8-18图

8-19 求题 8-19 图中所示的电流  $\dot{I}$  (分三种情况:  $\beta > 1, \beta < 1$  和  $\beta = 1$ )。

8-20 已知题 8-20 图中 $u_{\mathrm{s}} = 25\sqrt{2}\cos (10^{6}t - 126.87^{\circ}) \mathrm{~V}, R = 3 \Omega, C = 0.2 \mu \mathrm{F}, u_{c} = 20\sqrt{2}\cos (10^{6}t - 90^{\circ}) \mathrm{~V}$。

(1) 求各支路电流。
(2) 支路 1 可能是什么元件?

![](../../raw/pages_0225-0256/images/page_232_image_19.jpg)

<details>
<summary>text_image</summary>

+
Ûs
-
i
C
βi
</details>

题 8-19 图

![](../../raw/pages_0225-0256/images/page_232_image_21.jpg)

<details>
<summary>text_image</summary>

i
R
i₂
+
us
-
1
i₁
+
uC
-
C
</details>

题 8-20 图

![](../../raw/pages_0225-0256/images/page_232_image_23.jpg)

第八章部分习题答案
