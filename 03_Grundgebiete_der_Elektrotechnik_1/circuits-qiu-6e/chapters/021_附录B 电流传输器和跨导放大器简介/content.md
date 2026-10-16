# 附录B 电流传输器和跨导放大器简介

原始 PDF 第 518–522 页。

The image contains no text or mathematical content to process. It is a graphical representation of a triangular shape composed of small, irregular black dots. Therefore, the correct OCR output is an empty string.

# 附录 B

# 电流传输器和跨导放大器简介

本附录简要介绍电流传输器(current conveyor, CC)和跨导放大器(operational transconductance amplifier, OTC)的基本特性、基本功能及其简单应用。

## §B-1 电流传输器

电流传输器(CC)是 Smith 和 Sedra 于 1968 年提出的一种具有多功能且与运算放大器相似的基本电路器件。随着集成电路的发展,电流传输器作为一种集成电路器件在振荡器、滤波器及放大器等电路构造中获得了广泛的应用。电流传输器在控制、测量、通信等领域具有重要用途。

电流传输器从第一代已经发展到第三代。第一代电流传输器简称 CC I，用晶体管实现，其图形符号如图 B-1 所示。

它对外有三个端子(接地端除外), X、Y、Z 端, 其中 X 端对地电压与 Y 端对地电压相等。若各端子的电流参考方向如图 B-1 中所示, 则流入 X 端的电流等于流入 Y 端的电流, 流入 X 端的电流等于流

![](../../raw/pages_0513-0544/images/page_517_image_8.jpg)

<details>
<summary>text_image</summary>

uY ○ → iY
CC I
Y
K Z
iZ
uZ
uX ○ → iX
X
</details>

图 B-1 CCI

入 Z 端电流的 K 倍, K 为一常数, 其典型值取 K=1 。电流传输器通常分为两种, 即正向电流传输器和反向电流传输器, 对于正向电流传输器  $K=+1$ , 而反向电流传输器则取 K=-1, 故电流传输器的外特性关系式定义为

$$
\left[ \begin{array}{c} i _ {\mathrm{Y}} \\ u _ {\mathrm{X}} \\ i _ {\mathrm{Z}} \end{array} \right] = \left[ \begin{array}{c c c} 0 & 1 & 0 \\ 1 & 0 & 0 \\ 0 & \pm K & 0 \end{array} \right] = \left[ \begin{array}{c} u _ {\mathrm{Y}} \\ i _ {\mathrm{X}} \\ u _ {\mathrm{Z}} \end{array} \right]
$$

第二代电流传输器(CCⅡ)的外特性与第一代电流传输器不同,在其Y端不取电流,因此第二代电流传输器在实际使用中具有更大的灵活性。其外特性关系式定义为

---

§ B-1 电流传输器

495

$$
\left[ \begin{array}{c} i _ {\mathrm{Y}} \\ u _ {\mathrm{X}} \\ i _ {\mathrm{Z}} \end{array} \right] = \left[ \begin{array}{c c c} 0 & 0 & . 0 \\ 1 & 0 & 0 \\ 0 & \pm K & 0 \end{array} \right] = \left[ \begin{array}{c} u _ {\mathrm{Y}} \\ i _ {\mathrm{X}} \\ u _ {\mathrm{Z}} \end{array} \right]
$$

第二代电流传输器其 Y 端的输入阻抗为无限大, 为电压输入端, 而 X 端的电压总是跟随 Y 端的输入电压, 因此 X 端的输入阻抗等于零, 故 X 端的输入电流被传输到高阻抗 Z 输出端并得到了放大, 即  $i_{Z} = \pm K i_{X}$ 。

第二代电流传输器比第一代电流传输器具有更广泛的用途。CCⅡ不但能直接处理电压信号，而且能直接处理电流信号。通常采用电流型有源器件设计的电路称为电流模式电路，这种电路的特点是其输入、输出均为电流，由于电流传输器具有能够将X端的输入电流放大传输到高阻抗Z输出端的功能，因此，由电流传输器构成的电路就被称为电流模式电路。电流模式电路频带较宽，因而在电路设计中受到重视。

由电流传输器既可以构成电压模式基本单元电路,也可以构成电流模式基本单元电路,构成的电压模式基本单元电路有电压放大器、电压积分器、电压微分器。

以电流传输器构成的电压放大器如图 B-2 所示,由于

$$
U _ {\mathrm{o}} (s) = R _ {2} I _ {\mathrm{o}} (s)
$$

则有

$$
I _ {\mathrm{o}} (s) = \pm K I _ {\mathrm{X}} (s) = \pm K \frac {U _ {\mathrm{X}} (s)}{R _ {1}}
$$

故其传输函数为

$$
H (s) = \frac {U _ {\mathrm{o}} (s)}{U _ {\mathrm{i}} (s)} = \pm \frac {R _ {2} K}{R _ {1}}
$$

以电流传输器构成的电压积分器如图 B-3 所示, 其传输函数为

$$
H (s) = \frac {U _ {\mathrm{o}} (s)}{U _ {\mathrm{i}} (s)} = \pm \frac {K}{s C R _ {1}}
$$

![](../../raw/pages_0513-0544/images/page_518_image_14.jpg)

<details>
<summary>text_image</summary>

ui
Y
CC II
K
Z
X
R1
uo
R2
</details>

图 B-2 电压放大器

![](../../raw/pages_0513-0544/images/page_518_image_16.jpg)

<details>
<summary>text_image</summary>

u_i
Y
CC II
K Z
X
R
u_o
C
</details>

图 B-3 电压积分器

以电流传输器构成的电压微分器如图 B-4 所示, 其传输函数为

$$
H (s) = \frac {U _ {\mathrm{o}} (s)}{U _ {\mathrm{i}} (s)} = \pm s C R K
$$

---

496

附录 B 电流传输器和跨导放大器简介

由电流传输器构成的电流模式基本单元电路有电流放大器、电流积分器、电流微分器。

以电流传输器构成的电流放大器如图 B-5 所示, 其传输函数为

$$
H (s) = \frac {I _ {\mathrm{o}} (s)}{I _ {\mathrm{i}} (s)} = \pm \frac {R _ {2} K}{R _ {1}}
$$

![](../../raw/pages_0513-0544/images/page_519_image_6.jpg)

<details>
<summary>text_image</summary>

ui
Y
CC II
K Z
X
C
uo
R
</details>

图 B-4 电压微分器

![](../../raw/pages_0513-0544/images/page_519_image_8.jpg)

<details>
<summary>text_image</summary>

i₁
Y
CC II
K
Z
iₒ
X
R₂
R₁
</details>

图 B-5 电流放大器

以电流传输器构成的电流积分器如图 B-6 所示, 其传输函数为

$$
H (s) = \frac {I _ {\mathrm{o}} (s)}{I _ {\mathrm{i}} (s)} = \pm \frac {K}{s C R}
$$

以电流传输器构成的电流微分器如图 B-7 所示, 其传输函数为

$$
H (s) = \frac {I _ {\mathrm{o}} (s)}{I _ {\mathrm{i}} (s)} = \pm s C R K
$$

![](../../raw/pages_0513-0544/images/page_519_image_14.jpg)

<details>
<summary>text_image</summary>

i_i
Y
CC II
K
Z
i_o
X
C
R
</details>

图 B-6 电流积分器

![](../../raw/pages_0513-0544/images/page_519_image_16.jpg)

<details>
<summary>text_image</summary>

i_i
Y
CCII
K Z
X
R
C
i_o
</details>

图 B-7 电流微分器

电流模式基本单元电路在通信、测量、控制等电流模式电路设计中获得了广泛的应用，特别是在电流模式滤波器设计中具有重要应用。

## §B-2 跨导放大器

这里主要介绍(运算)跨导放大器(operationnal transconductance amplifier, OTA)，其图形符号和它的理想电路模型如图 B-8 所示，它有两个输入端，一个输出端，一个控制端。跨导运算放大器的输入信号为电压信号，图中“+”表示同相输入端，“-”表示反相

---

§ B-2 跨导放大器

497

输入端, 输出信号为电流信号, 其开环增益称为跨导, 用  $g_{m}$  表示, 它具有电导的性质, 受控制端的偏置电流  $I_{B}$  或偏置电压  $U_{B}$  控制。跨导运算放大器的输出电流近似为

$$
i _ {\mathrm{m}} = g _ {\mathrm{m}} (  u _ {\mathrm{P}} - u _ {\mathrm{N}}  )
$$

对于理想电路模型,由于两个电压输入端开路,故其差模输入阻抗无穷大,而输出电流类似于一个受差模输入电压控制的电流源,因此其输出阻抗为无穷大。

![](../../raw/pages_0513-0544/images/page_520_image_5.jpg)

<details>
<summary>text_image</summary>

(a) 图形符号
(b) 理想电路模型
</details>

图 B-8 跨导放大器

与常规的运算放大器(电压输入/电压输出)相比较,跨导运算放大器特点为:(1)输入差模电压控制输出电流;(2)增加了一个控制端,调节控制电流 $I_{B}$ 可以改变跨导 $g_{m}$ 值;(3)具有电流模式电路的特点。

跨导运算放大器的作用是将电压信号变换为电流信号,可对电流模式电路输入信号进行预处理,通常在电压模式与电流模式电路之间作为接口电路使用,其次它可以构成各种基本单元电路用于滤波器设计及各种电子测量、控制、通信电路。

以跨导运算放大器构成的差模电压积分器如图 B-9 所示, 其输出电流为

$$
I _ {\mathrm{o}} (s) = g _ {\mathrm{m}} \left[ U _ {\mathrm{P}} (s) - U _ {\mathrm{N}} (s) \right]
$$

输出电压为

$$
U _ {\mathrm{o}} (s) = \frac {1}{s C} I _ {\mathrm{o}} (s) = \frac {1}{s C} g _ {\mathrm{m}} U _ {\mathrm{i}} (s)
$$

故传输函数为

$$
H (s) = \frac {U _ {\mathrm{o}} (s)}{U _ {\mathrm{i}} (s)} = \frac {g _ {\mathrm{m}}}{s C}
$$

![](../../raw/pages_0513-0544/images/page_520_image_15.jpg)

<details>
<summary>text_image</summary>

uP
+
ui
-
uN
+
gm
-
C
+
uo
-
</details>

图 B-9 差模电压积分器

---

498

附录 B 电流传输器和跨导放大器简介

以跨导运算放大器构成的有损电压积分器如图 B-10 所示, 其跨导运算放大器 1 输出电流  $I_{o1}(s)$  为

$$
I _ {\mathrm{o1}} (s) = g _ {\mathrm{m1}} \left[ U _ {\mathrm{P}} (s) - U _ {\mathrm{N}} (s) \right] = g _ {\mathrm{m1}} U _ {\mathrm{i}} (s)
$$

跨导运算放大器 2 的同相输入端接地, 其输出电流  $I_{o2}(s)$  为

$$
I _ {\mathrm{o2}} (s) = g _ {\mathrm{m2}} [ 0 - U _ {c} (s) ] = - g _ {\mathrm{m2}} U _ {c} (s)
$$

由于跨导运算放大器 2 输出电流  $I_{o2}(s)$  反馈到它的反相输入端, 因此电容 C 的电流  $I_{C}(s)$  为

$$
I _ {C} (s) = I _ {\mathrm{o1}} (s) + I _ {\mathrm{o2}} (s) = g _ {\mathrm{m1}} U _ {\mathrm{i}} (s) - g _ {\mathrm{m2}} U _ {C} (s)
$$

而电容 $C$ 的电压 $U_{c}(s)$ 为

$$
U _ {c} (s) = \frac {1}{s C} I _ {c} (s) = \frac {1}{s C} g _ {\mathrm{m1}} U _ {\mathrm{i}} (s) - \frac {1}{s C} g _ {\mathrm{m2}} U _ {c} (s)
$$

由于电压  $U_{0}(s)=U_{C}(s)$ ，故有损电压积分器传输函数为

$$
H (s) = \frac {U _ {\mathrm{o}} (s)}{U _ {\mathrm{i}} (s)} = \frac {g _ {\mathrm{m1}}}{s C + g _ {\mathrm{m2}}}
$$

![](../../raw/pages_0513-0544/images/page_521_image_13.jpg)

<details>
<summary>text_image</summary>

u_p
+
-
u_i
-
u_N
+
-
gm1
-
C
gm2
+
-
u_o
-
</details>

图 B-10 有损电压积分器
