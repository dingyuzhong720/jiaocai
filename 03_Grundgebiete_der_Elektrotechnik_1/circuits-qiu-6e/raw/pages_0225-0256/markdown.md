单,这将大大简化对正弦稳态的表述和分析求解的过程。

电路理论中将式(8-5)中与正弦量 $u_{\mathrm{s}}$ 、 $i$ 关联的复数 $U_{\mathrm{s}}\mathrm{e}^{\mathrm{j}\phi_{\mathrm{u}}}$ 和 $I\mathrm{e}^{\mathrm{j}\phi_{i}}$ 定义为正弦量$u_{\mathrm{s}},i$ 对应的相量，并用对应的带“·”（点）符号的大写字母表示，如上述的正弦电压 $u_{\mathrm{s}}$ 和正弦电流 $i$ 对应的相量表示分别为

$$
\dot {U} _ {\mathrm{s}} \stackrel {\mathrm{def}} {=} U _ {\mathrm{s}} \mathrm{e} ^ {\mathrm{j} \phi_ {u}} = U _ {\mathrm{s}} / \phi_ {u}
$$

$$
\dot {I} \stackrel {\mathrm{def}} {=} I \mathrm{e} ^ {\mathrm{j} \phi_ {i}} = I / \phi_ {i}
$$

即正弦量的对应相量是一个复数,它的模为正弦量的有效值,它的辐角为正弦量的初相。式中  $\dot{U}_{s}$ 、 $\dot{I}$  中的“·”(点)号,既表示这一复数与正弦量关联的特殊身份,以区别于一般的复数,同时也表示区别于正弦量的有效值。正弦量对应的相量可直接根据上述定义写出。相量在复平面上表示的图形称为相量图,如图8-8所示为正弦电压  $u_{s}$  对应的相量  $\dot{U}_{s}$  的相量图。

![](images/page_224_image_7.jpg)

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

![](images/page_225_image_0.jpg)

<details>
<summary>natural_image</summary>

Pure technical line drawing of intersecting lines and shapes without any text, numbers, or symbols
</details>

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

![](images/page_225_image_28.jpg)

电路定律的相量形式

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

![](images/page_226_image_10.jpg)

(a)

![](images/page_226_image_12.jpg)

(b)

![](images/page_226_image_14.jpg)

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

![](images/page_227_image_3.jpg)

(a)

![](images/page_227_image_5.jpg)

(b)

![](images/page_227_image_7.jpg)

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

![](images/page_227_image_17.jpg)

(a)

![](images/page_227_image_19.jpg)

(b)

![](images/page_227_image_21.jpg)

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

相量形式为

$$
\dot {I} _ {j} = g \dot {U} _ {k}
$$

图 8-12(b)为其相量形式的电路图(其他形式的受控源与其类似)。

![](images/page_228_image_6.jpg)

图8-12 VCCS的相量表示

用复数代数方程描述电路定律的相量形式(略去变换过程)是相量法体系的基础,其中 VCR 的相量形式对正确应用相量法十分重要,不仅要用到电阻、感抗和容抗,或者电导、感纳和容纳等概念,而且要特别注意电压、电流之间的相位差。

例 8-4 图 8-13(a) 所示电路中， $i_{S}=5\sqrt{2}\cos(10^{3}t+30^{\circ})A$ ， $R=30\Omega, L=0.12H$ ， $C=12.5\mu F$ ，求电压  $u_{ad}$  和  $u_{bd}$ 。

解 为了帮助理解和避免错误,可根据原电路图画出对应的相量模型,它是将时域中的正弦电压、电流用相量标记,电路中的电阻、电感和电容元件根据 VCR 的相量形式分别用复数形式的  $R_{1}$ 、 $j\omega L$  和  $\frac{1}{j\omega C}$  标记,而其他与原电路图相同。根据相量形式的电路图就可以直接写出相量形式的电路方程。

图 8-13(a) 所示电路相对应的相量形式的电路图如图 8-13(b) 所示。图中  $\dot{I}_{s}=5\angle30^{\circ}A, j\omega L=j120\Omega, -j\frac{1}{\omega C}=-j80\Omega$ 。

![](images/page_228_image_12.jpg)

图8-13 例8-4图

根据元件的 VCR 的相量形式有

$\dot{U}_{R}=R\dot{I}=150/30^{\circ}V$  （与  $\dot{I}_{s}$  相同）

$\dot{U}_L = \mathrm{j}\omega L\dot{I} = 600 / 120^{\circ}\mathrm{V}$ （超前 $\dot{I}_{\mathrm{a}}90^{\circ}$ ）

$\dot{U}_{c} = -\mathrm{j}\frac{1}{\omega C}\dot{I} = 400 / - 60^{\circ}\mathrm{V}$ （滞后 $\dot{I}_{s}90^{\circ}$ ）

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

![](images/page_229_image_13.jpg)

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

在本章最后,有必要简单讨论电力技术发展历程上著名的交直流之争和当代高压直流输电。19世纪末，由于正弦交流电在交流发电机、交流电动机等方面的优势和容易经过变压器变压实现高压输电，交流电战胜了直流电。所以100多年来，交流电在电力系统中占据统治地位。然而随着电力电子技术的发展，可以采用高压直流输电。由于高压直流输电效率更高，直流输电在20世纪80年代重新登上历史舞台。虽然当代的发电、配电均采用交流电，但在输电方面，已经形成了交流输电和直流输电并存的局面。所以，电力技术发展也是螺旋式的和波浪式的，并不是一成不变的。

![](images/page_230_image_3.jpg)

## 思考题

8-1 何谓正弦稳态电路？对激励有何要求？响应是何种形式的时间函数？为什么？
8-2 正弦量的初相位为何在主值范围内取值,而两个正弦量的相位差也是在主值范围内取值?
8-3 对于正弦稳态电路,为什么可以采用相量法分析?是否可以在时域进行分析?
8-4 对于电感元件,为什么电压相量超前电流相量 $\frac{\pi}{2}$ ? 对于电容元件,为什么电流相量超前电压相量 $\frac{\pi}{2}$ ?

8-5 随着正弦激励频率的增加,感抗和容抗如何变化?

![](images/page_230_image_11.jpg)

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

![](images/page_231_image_14.jpg)

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

![](images/page_231_image_18.jpg)

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

![](images/page_231_image_20.jpg)

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

8-16 题 8-16 图所示电路中  $\dot{I}_{s}=2\angle0^{\circ}A$ 。求电压  $\dot{U}$ 。

![](images/page_232_image_4.jpg)

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

![](images/page_232_image_6.jpg)

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

![](images/page_232_image_10.jpg)

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

![](images/page_232_image_12.jpg)

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

![](images/page_232_image_19.jpg)

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

![](images/page_232_image_21.jpg)

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

![](images/page_232_image_23.jpg)

第八章部分习题答案

# 第九章

# 正弦稳态电路的分析

## 导读

对正弦稳态电路的分析,无论在实际应用上,还是在理论上都极为重要。电力工程中遇到的大多数问题都可以按正弦稳态电路分析来解决。许多电气、电子设备的设计和性能指标也往往是按正弦稳态考虑的。

在第八章中已为相量法奠定了理论基础,获得了电路基本定律的相量形式以及电阻、电容和电感元件的电压电流关系的相量形式。

本章首先介绍不含独立源的一端口的阻抗和导纳。其次，通过大量实例，较为全面、深入地展示相量法在正弦稳态电路分析中的应用。用相量法分析时，线性电阻电路的各种分析方法和电路定理可推广用于线性电路的正弦稳态分析。

本章还引入了有功功率、无功功率、视在功率、复功率等新概念，这些新概念在正弦稳态电路分析中占有十分重要的地位，须深入理解和牢固掌握。

![](images/page_233_image_8.jpg)

阻抗和导纳

## §9-1 阻抗和导纳

阻抗和导纳的概念以及对它们的运算和等效变换是线性电路正弦稳态分析中的重要内容。图9-1(a)所示为一个不含独立源的一端口 $N_{0}$ ，当它在角频率为 $\omega$ 的正弦电源激励下处于稳定状态时，端口的电流、电压都是同频率的正弦量，其相量分别设为 $\dot{U}=U/\phi_{u}$ 和 $\dot{I}=I/\phi_{i}$ 。在相量法中，可以通过一端口的电压相量、电流相量，用两种不同类型的等效参数来表述一端口 $N_{0}$ 的对外特性。这与电阻一端口电路类似（既可以用等效电阻，也可以用等效电导来表述其特性），现分述如下。

一端口  $N_{0}$  的端电压相量  $\dot{U}$  与电流相量  $\dot{I}$  的比值定义为一端口  $N_{0}$  的(复)阻抗 Z, 即有

$$
Z \stackrel {\text {def}} {=} \frac {\dot {U}}{\dot {I}} = \frac {U}{I} / \left(\phi_ {u} - \phi_ {i}\right) = | Z | / \varphi_ {z}
$$

或

$$
\dot {U} = Z \dot {I}
$$

上式是用阻抗 $Z$ 表示的欧姆定律的相量形式。$Z$ 不是正弦量，而是一个复数，称为复阻抗，其模 $|Z| = \frac{U}{I}$ 称为阻抗模（经常将 $Z$、$|Z|$ 简称为阻抗），辐角 $\varphi_Z = \phi_u - \phi_i$ 称为阻抗角。$Z$ 的单位为 $\Omega$，其电路符号与电阻相同，如图9-1(b)所示。$Z$ 的代数形式为

$$
Z = R + \mathrm{j} X
$$

式中 R 为等效电阻分量, X 为等效电抗分量, X > 0 时, Z 称为感性阻抗; X < 0 时, Z 称为容性阻抗。Z 在复平面上用直角三角形表示, 如图 9-2(a) 所示 (图中设 X > 0), 称为阻抗三角形。

![](images/page_234_image_7.jpg)

<details>
<summary>text_image</summary>

1
+
I
U̇
-
1'
N₀
</details>

(a)

![](images/page_234_image_9.jpg)

<details>
<summary>text_image</summary>

i
+
Ü
-
Z (Y)
</details>

(b)

图 9-1 一端口  $N_{0}$  的阻抗、导纳

根据阻抗表示的欧姆定律有

$$
\dot {U} = (R + \mathrm{j} X) \dot {I}
$$

上式表明通过电阻和电抗的是同一电流，等效电路要用两个电路元件串联表示，一为电阻元件 $R$ （表示实部），另一元件为储能元件（电感或电容），但要根据电抗的性质来定，当 $X > 0(\varphi_{z} > 0)$ 时，$X$ 称为感性电抗，可用等效电感 $L_{\mathrm{eq}}$ 的感抗替代，即

$$
\omega L _ {\mathrm{eq}} = X, \quad L _ {\mathrm{eq}} = \frac {X}{\omega}
$$

当  $X<0(\varphi_{z}<0)$  时，X 称为容性电抗，可用等效电容  $C_{eq}$  的容抗替代，即

$$
\frac {1}{\omega C _ {\mathrm{eq}}} = \mid X \mid , \quad C _ {\mathrm{eq}} = \frac {1}{\omega \mid X \mid}
$$

串联等效电路如图9-2(b)所示，等效电路将端电压 $\dot{U}$ 分解为两个分量，$\dot{U}_R = R\dot{I}$ 和 $\dot{U}_X = \mathrm{j}X\dot{I}$，根据KVL,3个电压相量在复平面上组成一个与阻抗三角形相似的直角三角形（将阻抗三角形乘以 $\dot{I}$ 获得），称为电压三角形，如图9-2(c)所示。

![](images/page_234_image_19.jpg)

<details>
<summary>text_image</summary>

+j
Z jX
φz
O R +1
</details>

(a)

![](images/page_234_image_21.jpg)

<details>
<summary>text_image</summary>

I
R
+  +
ÜR
-
+
UX
jX
-
U
-
</details>

(b)

![](images/page_234_image_23.jpg)

<details>
<summary>text_image</summary>

Û
Ûₓ
φₓ
î
φᵢ
Ûᵣ
</details>

(c)

图 9-2 一端口  $N_{0}$  用阻抗 Z 表示 ( $\varphi_{z}>0$ )

一端口  $N_{0}$  的电流相量  $\dot{I}$  与端电压相量  $\dot{U}$  的比值定义为一端口  $N_{0}$  的(复)导纳 Y, 它是表述一端口  $N_{0}$  对外特性的另一种参数, 即有

$$
Y \stackrel {\text {def}} {=} \frac {\dot {I}}{\dot {U}} = \frac {I}{U} / (\phi_ {i} - \phi_ {u}) = | Y | / \varphi_ {Y}
$$

或

$$
\dot {I} = Y \dot {U}
$$

上式是用导纳 $Y$ 表示的欧姆定律的相量形式。$Y$ 是一个复数，称为复导纳，模值 $\left|Y\right| = \frac{I}{U}$ 称为导纳模（经常将 $Y, |Y|$ 简称为导纳），辐角 $\varphi_{Y} = \phi_{i} - \phi_{u}$ 称为导纳角，$Y$ 的单位为 $S$ （西门子），其电路符号与电导相同。$Y$ 的代数形式为

$$
Y = G + \mathrm{j} B
$$

G 为等效电导(分量), B 为等效电纳(分量)。B>0 时, Y 称为容性导纳; B<0 时, Y 称为感性导纳。Y 在复平面上是一个直角三角形, 如图 9-3(a) 所示(图中设 B<0), 称为导纳三角形。

用导纳表示的欧姆定律有

$$
\dot {I} = (\dot {G} + \mathrm{j} B) \dot {U}
$$

等效电路要用等效电导与等效电感 $L_{eq}$ 或等效电容 $C_{eq}$ 的并联形式表示，并有

$C_{\mathrm{eq}} = \frac{B}{\omega}\quad (B > 0,$ 容性电纳）， $L_{\mathrm{eq}} = \frac{1}{|B|\omega}\quad (B <   0,$ 感性电纳）

并联等效电路如图 9-3(b) 所示, 电流  $\dot{I}$  被分解为两个分量,  $\dot{I}_{G} = \dot{U}G$  和  $\dot{I}_{B} = jB\dot{U}$ , 根据 KCL, 三个电流相量在复平面上组成一个与导纳三角形相似的电流三角形, 如图 9-3(c) 所示。

![](images/page_235_image_15.jpg)

<details>
<summary>text_image</summary>

+j
O
φY
G
jB
+1
Y
</details>

(a)

![](images/page_235_image_17.jpg)

<details>
<summary>text_image</summary>

i̇
+   G   i̇B
U̇   jB
-   i̇G
</details>

(b)

![](images/page_235_image_19.jpg)

<details>
<summary>text_image</summary>

Û
ÎG
ÎB
φY
Î
φi
</details>

(c)

图 9-3 一端口  $N_{0}$  用导纳 Y 表示 ( $\varphi_{Y}<0$ )

当 X=0 或  $B=0(G=0 \text{ 或 } R=0)$ ，等效电路就变成为一个参数和一种形式。

用 $Z$ 或 $Y$ 表示的欧姆定律是一种普遍形式, 第八章 §8-4 中表述的 VCR 的相量形式实质上是欧姆定律的特例, 是单一元件的欧姆定律, 所以也可以用阻抗或导纳的形式表示, 即有

$$
Z _ {R} = R
$$

$$
Y _ {G} = G = \frac {1}{R}
$$

$$
(\varphi_ {z} = 0) \quad (\varphi_ {Y} = 0)
$$

$$
Z _ {L} = \mathrm{j} \omega L \quad Y _ {L} = - \mathrm{j} \frac {1}{\omega L}
$$

$$
\left(\varphi_ {Z} = 9 0 ^ {\circ}\right) \quad \left(\varphi_ {Y} = - 9 0 ^ {\circ}\right)
$$

$$
Z _ {c} = - \mathrm{j} \frac {1}{\omega C} \quad Y _ {c} = \mathrm{j} \omega C
$$

$$
\left(\varphi_ {z} = - 9 0 ^ {\circ}\right) \quad \left(\varphi_ {Y} = 9 0 ^ {\circ}\right)
$$

感抗和容抗也常用电抗的符号表示，即 $X_{L} = \omega L, X_{C} = -\frac{1}{\omega C}$ 。单一元件的阻抗和导纳是阻抗、导纳的基础。

最后需要指出如下几点:

（1）一端口  $N_{0}$  的阻抗或导纳是由其内部的参数、结构和正弦电源的频率决定的，在一般情况下，其每一部分都是频率、参数的函数，随频率、参数而变。
(2) 一端口  $N_{0}$  中如不含受控源，则有  $\left|\varphi_{Z}\right| \leqslant 90^{\circ}$  或  $\left|\varphi_{Y}\right| \leqslant 90^{\circ}$ ，但有受控源时，可能会出现  $\left|\varphi_{Z}\right| > 90^{\circ}$  或  $\left|\varphi_{Y}\right| > 90^{\circ}$ ，其实部将为负值，其等效电路要设定受控源来表示实部。
(3) 一端口  $N_{0}$  的两种参数 Z 和 Y 具有同等效用, 彼此可以等效互换, 即有

$$
ZY = 1
$$

Z 和 Y 互为倒数, 其极坐标形式表示的互换条件为

$$
\mid Z \mid \mid Y \mid = 1 \quad \varphi_ {Z} + \varphi_ {Y} = 0
$$

等效互换常用代数形式。阻抗 Z 变换为等效导纳 Y 为

$$
Y = G + \mathrm{j} B = \frac {1}{R + \mathrm{j} X}
$$

Y 的实部、虚部分别为

$$
G = \frac {R}{| Z | ^ {2}}, \quad B = - \frac {X}{| Z | ^ {2}}
$$

串联等效电路就变换为相应的并联等效电路。同理,导纳 Y 变换为等效阻抗 Z 为

$$
Z = R + \mathrm{j} X = \frac {1}{G + \mathrm{j} B}
$$

$$
R = \frac {G}{\mid Y \mid^ {2}}, \quad X = - \frac {B}{\mid Y \mid^ {2}}
$$

并联等效电路就变换为相应的串联等效电路。显然，等效变换不会改变阻抗（或导纳）原来的感性或容性性质。

（4）对阻抗或导纳的串、并联电路的分析计算，三角形和星形之间的互换，完全可以采纳电阻电路中的方法及相关的公式。

例 9-1 RLC 串联电路如图 9-4(a) 所示, 其中  $R = 15 \Omega, L = 12 \, mH, C = 5 \, \mu F$ , 端电压  $u_{s}=100\sqrt{2}\cos(5\ 000t)$  V。试求:(1) 电路中的电流 i（瞬时表达式）和各元件的电压相量；(2) 电路的等效导纳和并联等效电路。

![](images/page_237_image_4.jpg)

<details>
<summary>text_image</summary>

I
R
jωL
+  +  +
ÛR -  +  ÛL -
Ûs
1
jωC
+  ÛC
-
</details>

(a)

![](images/page_237_image_6.jpg)

<details>
<summary>text_image</summary>

+
i
u_S
G
L_eq
-
</details>

(b)

图9-4 例9-1图

解（1）用相量法求解时，可先写出已知相量和设定待求相量，本例已知 $\dot{U}_{\mathrm{a}} = 100 / 0^{\circ}\mathrm{V}$，而 $\dot{I}, \dot{U}_{R}, \dot{U}_{L}$ 和 $\dot{U}_{C}$ 为待求相量，如图9-4(a)所示。然后计算各部分阻抗为:

$$
Z _ {R} = 1 5 \Omega
$$

$$
Z _ {L} = \mathrm{j} \omega L = \mathrm{j} 6 0 \Omega
$$

$$
Z _ {c} = - \mathrm{j} \frac {1}{\omega C} = - \mathrm{j} 4 0 \Omega
$$

$$
Z _ {\mathrm{eq}} = Z _ {R} + Z _ {L} + Z _ {C} = (1 5 + \mathrm{j} 2 0) \Omega
$$

$$
= 2 5 / 5 3. 1 3 ^ {\circ} \Omega (\text {感性阻抗})
$$

电流相量为

$$
\dot {I} = \frac {\dot {U} _ {\mathrm{s}}}{Z _ {\mathrm{eq}}} = \frac {1 0 0 / 0 ^ {\circ}}{2 5 / 5 3 . 1 3 ^ {\circ}} \mathrm{A} = 4 / - 5 3. 1 3 ^ {\circ} \mathrm{A}
$$

正弦电流 i 为

$$
i = 4 \sqrt {2} \cos (5 0 0 0 t - 5 3. 1 3 ^ {\circ}) \mathrm{A}
$$

各元件电压相量为

$$
\dot {U} _ {R} = R \dot {I} = 6 0 / - 5 3. 1 3 ^ {\circ} \mathrm{V}
$$

$$
\dot {U} _ {L} = \mathrm{j} \omega L \dot {I} = 2 4 0 / 3 6. 8 7 ^ {\circ} \mathrm{V}
$$

$$
\dot {U} _ {c} = - \mathrm{j} \frac {1}{\omega C} \dot {I} = 1 6 0 / - 1 4 3. 1 3 ^ {\circ} \mathrm{V}
$$

(2) 电路的等效导纳  $Y_{eq}$  为

$$
Y _ {\mathrm{eq}} = \frac {1}{Z _ {\mathrm{eq}}} = \frac {1}{2 5} / - 5 3. 1 3 ^ {\circ} \mathrm{S} = (0. 0 2 4 - \mathrm{j} 0. 0 3 2) \mathrm{S} (\text {感性})
$$

等效电导  $G=0.024S$ （或  $R=41.67\Omega$ ），等效电感  $L_{eq}=\frac{1}{|B|\omega}=6.25\ mH$ 。

等效电路如图9-4(b)所示。由读者思考并回答下列问题:(1) 将本例的电路改为RLC并联电路，求各支路电流和串联等效电路；(2) 如果电源的角频率改为  $\omega =$

2 500 rad/s, 其等效电路将发生怎样的变化?

例 9-2 图 9-5(a) 所示电路中  $Z=(10+j157)\ \Omega, Z_{1}=1\ 000\ \Omega, Z_{2}=-j318.47\ \Omega, U_{s}=100\ V, \omega=314\ rad/s$ 。求:(1) 各支路电流和电压  $\dot{U}_{10}$ ; (2) 并联等效电路。

![](images/page_238_image_4.jpg)

<details>
<summary>text_image</summary>

i
+
Üs
-
Z
1
i1
Z1
0
i2
Z2
</details>

(a)

![](images/page_238_image_6.jpg)

<details>
<summary>text_image</summary>

i
+
us
G
Ceq
-
</details>

(b)

图9-5 例9-2图

解 （1）令  $\dot{U}_{s}=100/0^{\circ}V$  (参考相量)，设各支路电流相量为  $\dot{I}$ 、 $\dot{I}_{1}$  和  $\dot{I}_{2}$ ，如图 9-5(a) 所示。计算方法和步骤完全与电阻串并联电路相同。 $Z_{1}$  与  $Z_{2}$  的并联等效阻抗为  $Z_{12}$ ，有

$$
\begin{array}{l} Z _ {1 2} = \frac {Z _ {1} Z _ {2}}{Z _ {1} + Z _ {2}} = \frac {1 0 0 0 (- \mathrm{j} 3 1 8 . 4 7)}{1 0 0 0 - \mathrm{j} 3 1 8 . 4 7} \Omega = 3 0 3. 4 5 / - 7 2. 3 3 ^ {\circ} \Omega \\ = (9 2. 1 1 - \mathrm{j} 2 8 9. 1 3) \Omega (\text {容性}) \\ \end{array}
$$

总的输入阻抗 $Z_{\mathrm{eq}}$ 为

$$
Z _ {\mathrm{eq}} = Z _ {1 2} + Z = (1 0 2. 1 1 - \mathrm{j} 1 3 2. 1 3) \Omega = 1 6 6. 9 9 / - 5 2. 3 0 ^ {\circ} \Omega (\text {容性})
$$

各支路电流和电压  $\dot{U}_{10}$  计算如下:

$$
\dot {I} = \frac {\dot {U} _ {\mathrm{s}}}{Z _ {\mathrm{eq}}} = 0. 6 0 / 5 2. 3 0 ^ {\circ} \mathrm{A}
$$

$$
\dot {U} _ {1 0} = Z _ {1 2} \dot {I} = 1 8 2. 0 7 / - 2 0. 0 3 ^ {\circ} \mathrm{V}
$$

$$
\dot {I} _ {1} = \frac {\dot {U} _ {1 0}}{Z _ {1}} = 0. 1 8 / - 2 0. 0 3 ^ {\circ} \mathrm{A}
$$

$$
\dot {I} _ {2} = \frac {\dot {U} _ {1 0}}{\bar {Z} _ {2}} = 0. 5 7 / 6 9. 9 6 ^ {\circ} \mathrm{A}
$$

也可以用分流公式计算  $\dot{I}_{1}$ 、 $\dot{I}_{2}$ ，即有

$$
\dot {I} _ {1} = \dot {I}   \frac {Z _ {2}}{Z _ {1} + Z _ {2}}, \quad \dot {I} _ {2} = \dot {I}   \frac {Z _ {1}}{Z _ {1} + Z _ {2}} (\text {或} \dot {I} _ {2} = \dot {I} - \dot {I} _ {1})
$$

(2) 电路的等效导纳  $Y_{eq}$  为

$$
\begin{array}{l} Y _ {\mathrm{eq}} = \frac {1}{Z _ {\mathrm{eq}}} = 5. 9 9 \times 1 0 ^ {- 3} / 5 2. 3 0 ^ {\circ} \mathrm{S} \\ = (3. 6 6 \times 1 0 ^ {- 3} + j 4. 7 4 \times 1 0 ^ {- 3}) \mathrm{S} (\text {容性}) \\ \end{array}
$$

并联等效电路的等效电导和等效电容为

![](images/page_238_image_23.jpg)

<details>
<summary>natural_image</summary>

Pure technical line drawing of mechanical components without any text or symbols
</details>

$$
G = 3. 6 6 \times 1 0 ^ {- 3} \mathrm{S} (\text {或} R = 2 7 3. 2 2 \Omega)
$$

$$
C _ {\mathrm{eq}} = \frac {4 . 7 4 \times 1 0 ^ {- 3}}{3 1 4} \mathrm{F} = 1 5. 0 9 \mu \mathrm{F}
$$

等效电路如图 9-5(b) 所示。

## §9-2 电路的相量图

在分析阻抗(导纳)串、并联电路时,可以利用相关的电压和电流相量在复平面上组成的电路的相量图。相量图可以直观地显示各相量之间的关系,并可用来辅助电路的分析计算。在相量图上,除了按比例反映各相量的模(有效值)以外,最重要的是相对地确定各相量在图上的位置(方位)。一般的做法是:相对于电路并联部分的电压相量,根据支路的VCR确定各并联支路的电流相量与电压相量之间的夹角;然后,再根据节点上的KCL方程,用相量平移求和法则,画出节点上各支路电流相量组成的多边形;相对于电路串联部分的电流相量,根据VCR确定串联部分有关电压相量与电流相量之间的夹角,再根据回路上的KVL方程,用相量平移求和的法则,画出回路上各电压相量所组成的多边形。

例 9-3 画出例 9-1 电路 [图 9-4(a) 所示] 的相量图。

解 该电路为串联电路, 可以相对于电流相量  $\dot{I}$  确定各串联元件的电压相量在相量图中的位置, 根据  $\dot{U}_{s} = \dot{U}_{R} + \dot{U}_{L} + \dot{U}_{C}$  画出电压相量组成的多边形。画法如下。

在复平面上先画出电流相量 $\dot{I}$, 然后, 从原点 $O$ 起, 相对于电流相量 $\dot{I}$, 按平移求和法则, 逐一画出 KVL 方程右边各电压相量。例如, 画出 $\dot{U}_{R} = R\dot{I}$ (与 $\dot{I}$ 同相), 然后, 再从 $\dot{U}_{R}$ 的末端画出下一个电压相量, 例如, $\dot{U}_{L} = \mathrm{j}\omega L\dot{I}$ (超前 $\dot{I}90^{\circ}$), 依此类推。最后, 从原点 $O$ 至最后一个电压相量的末端的相量就是上述 KVL 方程左边的电压相量 $\dot{U}_{s}$, 如图 9-6(a) 所示。KVL 方程在相量图上表示为一个封闭的多边形, 本例为四边形。根据 KVL 方程求和时, 与电压相量的次序无关, 所以, 图 9-6(b) 也是该电路的相量图。(本例也可以先设电流相量的相位为零画出, 最后将整个图形顺时针旋转 $53.13^{\circ}$)

![](images/page_239_image_11.jpg)

<details>
<summary>text_image</summary>

O
I
53.13°
Ûs
ÛR
ÛL
ÛC
</details>

(a)

![](images/page_239_image_13.jpg)

<details>
<summary>text_image</summary>

O
Ûs
î
ÛL
ÛC
ÛR
</details>

(b)

图 9-6 例 9-1 电路的相量图

例9-4 画出例9-2电路[图9-5(a)所示]的相量图。

解 先画出并联部分的电压的相量  $\dot{U}_{10}=U_{10}/-20.03^{\circ}$ ，然后相对于电压  $\dot{U}_{10}$  画出

描述 $\dot{I} = \dot{I}_1 + \dot{I}_2$ 的电流相量组成的三角形，注意，$\dot{I}_1$ 与 $\dot{U}_{10}$ 同相，$\dot{I}_2$ 超前 $\dot{U}_{10}$ 的角度为 $90^\circ$；然后，相对于已画出的电流相量 $\dot{I}$，画出描述 $\dot{U}_s = \dot{U}_{10} + \dot{U}_z = \dot{U}_{10} + Z\dot{I}$ 的电压相量组成的多边形。图9-7所示即为该电路的相量图。

上述两个例子的相量图都是根据电路的求解结果画出的,有时候也可以根据电路的参数和结构定性地画出相量图,以辅助电路的求解。

![](images/page_240_image_6.jpg)

<details>
<summary>text_image</summary>

i₁
i₂
i
O
i₁
Ûₛ
Zî
Û₁₀
</details>

图9-7 例9-2电路的相量图

## §9-3 正弦稳态电路的分析

对线性电路的正弦稳态分析,无论在实际应用上,还是在理论上都极为重要。电力工程中遇到的大多数问题都可以按正弦稳态电路分析来解决。许多电气、电子设备的设计和性能指标也往往是按正弦稳态考虑的。电工技术和电子技术中的非正弦周期信号可以分解为频率成整数倍的正弦函数的无穷级数,这类问题也可以应用正弦稳态分析方法处理。

在前面的章节中已为相量法奠定了理论基础,获得了电路基本定律的相量形式,即

$$
\begin{array}{l l} \text {KCL} & \sum \dot {I} = 0 \\ \text {KVL} & \sum \dot {U} = 0 \\ \text {VCR} & \dot {U} = Z \dot {I} \quad \text {或} \quad \dot {I} = Y \dot {U} \end{array}
$$

并通过一些实例,初步展示了相量法的应用。这些都说明,相量法与线性电阻电路中的分析方法相比,不仅在表述的形式上十分相似,而且在分析方法上也完全一样。因此,用相量法分析时,线性电阻电路的各种分析方法和电路定理可推广用于线性电路的正弦稳态分析,差别仅在于所得电路方程为以相量形式表示的代数方程以及用相量形式描述的电路定理,而计算则为复数运算。本节将通过举例,较为全面、深入地展示相量法在正弦稳态分析中的应用。

例 9-5 图 9-8(a) 中已知  $u_{\mathrm{s}} = 200\sqrt{2}\cos(314t + \frac{\pi}{3}) \, \mathrm{V}$ ，电流表 A 的读数为 2 A，电压表  $V_{1}, V_{2}$  的读数均为 200 V。求参数 R、L、C，并作出该电路的相量图。

解 电路的基本定律和电路方程乃是解题的根本途径。根据题意可设:$\dot{U}_{\mathrm{s}} = 200 / 60^{\circ}\mathrm{V}$（已知），$\dot{U}_{1} = 200 / \phi_{1}\mathrm{V}, \dot{U}_{2} = 200 / \phi_{2}\mathrm{V}, \dot{I} = 2 / \phi_{i}\mathrm{A}$。根据图9-8(a)电路可列写如下电压、电流关系和电路方程:

$$
2 0 0 \angle 6 0 ^ {\circ} = 2 0 0 \angle \phi_ {1} + 2 0 0 \angle \phi_ {2} \quad (\mathrm{KVL})
$$

![](images/page_240_image_16.jpg)

<details>
<summary>natural_image</summary>

Pure technical line drawing of a mechanical assembly without any text, numbers, or symbols
</details>

![](images/page_240_image_17.jpg)

正弦稳态电路的分析

$$
- \mathrm{j} \frac {1}{\omega C} = \frac {\dot {U} _ {2}}{\dot {I}} = 1 0 0 / (\phi_ {2} - \phi_ {i})
$$

$$
Z _ {1} = \frac {\dot {U} _ {1}}{\dot {I}} = R + \mathrm{j} \omega L = 1 0 0 / (\phi_ {1} - \phi_ {i})
$$

依次求解上列方程,取一组合理解答为

$$
\phi_ {1} = 1 2 0 ^ {\circ}
$$

$$
\phi_ {2} = 0 ^ {\circ}
$$

$$
\phi_ {i} = 9 0 ^ {\circ}
$$

$$
C = 3 1. 8 5 \mu \mathrm{F}
$$

$$
R = 8 6. 6 0 \Omega
$$

$$
L = 0. 1 5 9 \mathrm{H}
$$

读者可查验上述结果。对串、并联电路常常采用相量图来启发解题思路和方法。本例可先根据KVL作电路的电压相量图，如图9-8(b)所示（两种可能的封闭的正三角形），很容易根据该图求得 $\phi_{1}$ 和 $\phi_{2}$ （有两种可能的解答）。也可作本题的阻抗三角形: $Z = 100 / \varphi_{Z}\Omega ,Z_{1} = 100 / \varphi_{Z1}\Omega ,Z_{C} = -\mathrm{j}100\Omega$ ，有

$$
1 0 0 \underline {{\varphi_ {z}}} = 1 0 0 \underline {{\phi_ {z 1}}} - j 1 0 0
$$

如图 9-8(c) 所示, 根据该图可得

$$
Z = 1 0 0 \angle - 3 0 ^ {\circ} \Omega
$$

$$
Z _ {1} = 1 0 0 / 3 0 ^ {\circ} \Omega
$$

![](images/page_241_image_17.jpg)

<details>
<summary>text_image</summary>

+
us
-
A
R
L
V1
C
V2
</details>

(a)

![](images/page_241_image_19.jpg)

<details>
<summary>text_image</summary>

Û₁
Û₂
Û₃
(Û₂)
60°
(Û₁)
</details>

(b)

![](images/page_241_image_21.jpg)

(c)

图9-8 例9-5图

当出现多解的情况时,必须判断其合理性。本例中有另一组解  $\phi_{1}=0^{\circ},\phi_{2}=120^{\circ}$  是不合理的。(请读者思考为什么。)

例 9-6 图 9-9 所示电路中 R 可变。在什么条件下 I 可保持不变？

解 根据题意,电阻 R 是从其左侧的一端口 1-1' 获得电流的,所以,一端口 1-1' 的诺顿等效电路应为理想电流源,其等效导纳应为零,则有

$$
Y _ {\mathrm{eq}} = \mathrm{j} \omega C - \mathrm{j} \frac {1}{\omega L} = 0
$$

$$
\dot {I} = \mathrm{j} \omega C \dot {U} _ {\mathrm{s}} (\text {短路电流})
$$

应当满足的条件为

$$
\omega = \frac {1}{\sqrt {L C}}
$$

![](images/page_241_image_31.jpg)

<details>
<summary>text_image</summary>

+
1
jωC
Ûs
-
1
jωL
i
R
1'
-
</details>

图9-9 例9-6图

解题时要用多种方法试探,启发思维,达到举一反三的目的。以下提供其他的求解方法,由读者分析完成。

根据电路的节点方程有

$$
(\mathrm{j} \omega C - \mathrm{j} \frac {1}{\omega L}) \dot {U} _ {1 1 ^ {\prime}} + \dot {I} = \mathrm{j} \omega C \dot {U} _ {\mathrm{s}}
$$

根据网孔法(顺时针)解得电流 $\dot{I}$ 为

$$
\dot {I} = \frac {\mathrm{j} \omega L \dot {U} _ {\mathrm{s}}}{(\mathrm{j} \omega L - \mathrm{j} \frac {1}{\omega C}) (\bar {R} + \mathrm{j} \omega L) - (\mathrm{j} \omega L) ^ {2}}
$$

当  $R=\infty$  (开路) 时, 开路电压的模  $U_{11'oe}=\infty$ , 而  $\dot{U}_{11'oe}$  为

$$
\dot {U} _ {1 1 ^ {\prime} \mathrm{oc}} = \frac {\mathrm{j} \omega L \dot {U} _ {\mathrm{s}}}{\mathrm{j} \omega L - \mathrm{j} \frac {1}{\omega C}}
$$

例 9-7 求图 9-10(a) 所示一端口的戴维南等效电路。

解 戴维南等效电路的开路电压  $\dot{U}_{oc}$  和戴维南等效阻抗  $Z_{eq}$  的求解方法与电阻电路相同。

![](images/page_242_image_11.jpg)

<details>
<summary>text_image</summary>

Z₁
a
+ rI₂ -
1
+
U̇₅₁
-
Z₂
I₂
İ₃
0
U̇ₒₒ
-
1'
</details>

(a)

![](images/page_242_image_13.jpg)

<details>
<summary>text_image</summary>

Z₁
+
rI'₂
-
i₀
1
+
Z₂
i'₂
U₀
-1'
1'
</details>

(b)

![](images/page_242_image_15.jpg)

<details>
<summary>text_image</summary>

Z₁
a
+ rI₂ -
1
+
U̇₅₁
-
Z₂
i₂
iₛ₃
0
1'
i
</details>

(c)

图9-10 例9-7图

先求  $\dot{U}_{oc}$ ，将  $1-1'$  开路，由图 9-10(a) 可知

$$
\dot {U} _ {\mathrm{oc}} = - r \dot {I} _ {2} + \dot {U} _ {\mathrm{a0}}
$$

又有

$$
(Y _ {1} + Y _ {2}) \dot {U} _ {\mathrm{a0}} = Y _ {1} \dot {U} _ {\mathrm{s1}} - \dot {I} _ {\mathrm{s3}}
$$

![](images/page_242_image_22.jpg)

<details>
<summary>natural_image</summary>

Pure architectural line drawing of a building with scaffolding and structural elements (no text or symbols)
</details>

解得

$$
\dot {I} _ {2} = Y _ {2} \dot {U} _ {\mathrm{a0}}
$$

$$
\dot {U} _ {\mathrm{oc}} = \frac {(1 - r Y _ {2}) (Y _ {1} \dot {U} _ {\mathrm{s1}} - \dot {I} _ {\mathrm{s3}})}{Y _ {1} + Y _ {2}}
$$

可按图9-10(b)求解等效阻抗 $Z_{\mathrm{eq}}$ 。在端口 $1 - 1^{\prime}$ 置一电压源 $\dot{U}_0$ （与独立电源同频率），求得 $\dot{I}_0$ 后有

$$
Z _ {\mathrm{eq}} = \frac {\dot {U} _ {0}}{\dot {I} _ {0}}
$$

可以设  $\dot{I}_{2}^{\prime}$  为已知, 然后求出  $\dot{U}_{0}$ 、 $\dot{I}_{0}$ 。由图 9-10(b) 得

$$
\dot {I} _ {0} = \dot {I} _ {2} ^ {\prime} + Z _ {2} Y _ {1} \dot {I} _ {2} ^ {\prime}
$$

$$
\dot {U} _ {0} = Z _ {2} \dot {I} _ {2} ^ {\prime} - r \dot {I} _ {2} ^ {\prime}
$$

解得

$$
Z _ {\mathrm{eq}} = \frac {(Z _ {2} - r) \dot {I} _ {2} ^ {\prime}}{(1 + Z _ {2} Y _ {1}) \dot {I} _ {2} ^ {\prime}} = \frac {Z _ {2} - r}{1 + Z _ {2} Y _ {1}} = \frac {1 - r Y _ {2}}{Y _ {1} + Y _ {2}}
$$

从求得的  $\dot{U}_{oc}$  和  $Z_{eq}$  的表达式可知，应有  $Y_{1} + Y_{2} \neq 0$  成立。

也可求解端口  $1-1'$  的短路电流  $\dot{I}_{sc}$ ，用  $Z_{eq}=\frac{\dot{U}_{oc}}{\dot{I}_{sc}}$  求得等效电抗。本例有

$$
\dot {I} _ {\mathrm{sc}} = Y _ {1} \dot {U} _ {\mathrm{s1}} - \dot {I} _ {\mathrm{s3}}
$$

当电路中有受控源时,上述方法要对电路进行两次求解,如用一步法可能要方便些。具体做法为:在端口 1-1'置一电流源 $\dot{I}$ 替代一端口的输出电流 $\dot{I}$,如图 9-10(c)中虚线所示,求端电压 $\dot{U}_{11'}$ 与 $\dot{I}$ 的电压电流关系,即 $\dot{U}_{11'} = f(\dot{I})$(外特性),如本例有电路方程

$$
(Y _ {1} + Y _ {2}) \dot {U} _ {\mathrm{a0}} = Y _ {1} \dot {U} _ {\mathrm{s1}} - \dot {I} _ {\mathrm{s3}} - \dot {I}
$$

$$
\dot {U} _ {1 1 ^ {\prime}} = - r \dot {I} _ {2} + Z _ {2} \dot {I} _ {2}
$$

$$
\dot {I} _ {2} = \dot {U} _ {\mathrm{a0}} Y _ {2}
$$

最后解得

$$
\dot {U} _ {1 1 ^ {\prime}} = \frac {1 - r Y _ {2}}{Y _ {1} + Y _ {2}} (Y _ {1} \dot {U} _ {\mathrm{s} 1} - \dot {I} _ {\mathrm{s} 3}) - \frac {1 - r Y _ {2}}{Y _ {1} + Y _ {2}} \dot {I}
$$

根据上述方程就能获得戴维南等效电路的两个参数。

例 9-8 求图 9-11 所示电路中的电流  $i_{L}$ 。图中电压源  $u_{s}=10.39\sqrt{2}\sin(2t+60^{\circ})$  V，电流源  $i_{s}=3\sqrt{2}\cos(2t-30^{\circ})$  A。

解 电路中的电源为同一频率,则有

$$
\dot {U} _ {\mathrm{s}} = 1 0. 3 9 \angle - 3 0 ^ {\circ} \mathrm{V}, \quad \dot {I} _ {\mathrm{s}} = 3 \angle - 3 0 ^ {\circ} \mathrm{A}, \quad \frac {1}{\omega C} = 1 \Omega , \quad \omega L = 1 \Omega
$$

![](images/page_244_image_2.jpg)

<details>
<summary>text_image</summary>

0.5 F
① 0.5 H iL ② R
10 Ω
us +
-
0.5 F
0.5 F
iS
</details>

图9-11 例9-8图

本例将仿照电阻电路用不同方法编写电路方程求解。

(1) 用节点法求解, 列方程为

$$
(2 \mathrm{j} - \mathrm{j}) \dot {U} _ {1 0} - (- \mathrm{j}) \dot {U} _ {2 0} = \mathrm{j} \dot {U} _ {\mathrm{s}}
$$

$$
- (- \mathrm{j}) \dot {U} _ {1 0} + (\mathrm{j} - \mathrm{j}) \dot {U} _ {2 0} = - \dot {I} _ {\mathrm{s}}
$$

$$
\dot {I} _ {L} = \frac {\dot {U} _ {1 0} - \dot {U} _ {2 0}}{\mathrm{j}}
$$

可解得 $\dot{U}_{10} = \mathrm{j}\dot{I}_{\mathrm{s}},\quad \dot{U}_{20} = \dot{U}_{\mathrm{s}} - \mathrm{j}\dot{I}_{\mathrm{s}},\quad \dot{I}_L = -\mathrm{j}(\dot{U}_{10} - \dot{U}_{20}) = \mathrm{j}\dot{U}_{\mathrm{s}} + 2\dot{I}_{\mathrm{s}}$

(2) 用网孔法(顺时针方向)求解, 设网孔电流为  $\dot{I}_{1}$ 、 $\dot{I}_{2}$  和  $\dot{I}_{s}$  (自左至右), 有

$$
\begin{array}{l} - \mathrm{j} 2 \dot {I} _ {1} - (- \mathrm{j}) \dot {I} _ {2} = \dot {U} _ {\mathrm{a}} \\ - (- \mathrm{j}) \dot {I} _ {1} + (\mathrm{j-j2}) \dot {I} _ {2} - (- \mathrm{j}) \dot {I} _ {\mathrm{a}} = 0 \\ \end{array}
$$

(右网孔方程省列)

$$
\dot {I} _ {L} = \dot {I} _ {2}
$$

(3) 用叠加定理求解。

$$
\dot {I} _ {L} ^ {\prime} = \mathrm{j}   \dot {U} _ {\mathrm{s}} \quad (\dot {U} _ {\mathrm{s}} \text {单独作用})
$$

$I_{L}^{\prime\prime}= \dot{I}_{s}\frac{-j}{-j0.5}=2 \dot{I}_{s}$  ( $\dot{I}_{s}$  单独作用)

$$
\dot {I} _ {L} = \dot {I} _ {L} ^ {\prime} + \dot {I} _ {L} ^ {\prime \prime}
$$

(4) 用戴维南等效电路求解。

端口 1-2 的开路电压  $\dot{U}_{oc}$  为

$$
\dot {U} _ {\mathrm{oc}} = \frac {1}{2} \dot {U} _ {\mathrm{s}} - \mathrm{j} \dot {I} _ {\mathrm{s}}
$$

端口1-2的等效阻抗 $Z_{\mathrm{eq}}$ 为

$$
Z _ {\mathrm{eq}} = \left(\frac {1}{\mathrm{j} 2} - \mathrm{j}\right) \Omega = - \mathrm{j} 1. 5 \Omega
$$

解得

$$
\dot {I} _ {L} = \dot {I} _ {2} = \frac {\dot {U} _ {\mathrm{oc}}}{\mathrm{j} - \mathrm{j} 1 . 5} = \mathrm{j} \dot {U} _ {\mathrm{s}} + 2 \dot {I} _ {\mathrm{s}} = 1 0 / 3 0 ^ {\circ} \mathrm{A}
$$

$$
i _ {L} = 1 0 \sqrt {2} \cos (2 t + 3 0 ^ {\circ}) \mathrm{A}
$$

![](images/page_244_image_26.jpg)

<details>
<summary>natural_image</summary>

Pure technical line drawing of a mechanical assembly without any text, numbers, or symbols
</details>

读者可思考,当电路中的电阻 R 变化时,将对电路产生哪些影响?

## §9-4 正弦稳态电路的功率

设图 9-12(a) 所示一端口 N 吸收的瞬时功率 p 等于电压 u 和电流 i 的乘积

$$
p = u i
$$

当一端口 N 处于正弦稳态时, 端口的电压、电流是同频正弦量, 瞬时功率是两个同频正弦量的乘积, 是一个随时间作周期变化的非正弦周期量。工程上计量的功率, 家用电器标记的功率都是周期量的平均功率, 如电热水器的功率为 1500 W, 日光灯的功率为 40 W 等, 都是指平均功率。周期量的平均功率 P 定义为

$$
P \stackrel {\mathrm{def}} {=} \frac {1}{T} \int_ {0} ^ {T} p \mathrm{d} t = \frac {1}{T} \int_ {0} ^ {T} u i \mathrm{d} t
$$

![](images/page_245_image_9.jpg)

正弦稳态电路的功率

![](images/page_245_image_11.jpg)

功率因数的提高

![](images/page_245_image_13.jpg)

<details>
<summary>text_image</summary>

i
+
u
-
N
(a)
u,i,p
p
i
UIcosφz
O
t
(b)
</details>

图9-12 一端口电路N的功率

下面将以 RLC 串联电路作为不含独立源的一端口的例子, 来研究在正弦稳态下, 这些元件在能量转换过程中的作用。电路可参阅图 9-4(a) 所示, 设正弦电流为  $i = I_{m} \cos(\omega t)$ , 各元件吸收的瞬时功率分述如下:

电阻 R 吸收的瞬时功率  $p_{R}$  为

$$
\begin{array}{l} p _ {R} = R i ^ {2} = R I _ {\mathrm{m}} ^ {2} \cos^ {2} (\omega t) \\ = R I ^ {2} \left[ 1 + \cos (2 \omega t) \right] \\ \end{array}
$$

它是一个频率为正弦电流(或电压)频率2倍的非正弦周期量,始终有 $p_{R}\geqslant0$ ,表明电阻的耗能特性,其吸收的平均功率 $P_{R}$ 为

$$
P _ {R} = \frac {1}{T} \int_ {0} ^ {T} R I ^ {2} \left[ 1 + \cos (2 \omega t) \right] \mathrm{d} t = R I ^ {2}
$$

电感 L 吸收的瞬时功率  $p_{L}$  为

$$
\begin{array}{l} p _ {L} = i L \frac {\mathrm{d} i}{\mathrm{d} t} = - \omega L I _ {\mathrm{m}} ^ {2} \cos (\omega t) \sin (\omega t) \\ = - \omega L I ^ {2} \sin (2 \omega t) \\ \end{array}
$$

它是一个频率为正弦电流(或电压)频率2倍的正弦量,在正弦电流的一个周期内正负交替变化2次,即吸收(储存)—释放能量2次。其吸收的平均功率 $P_{L}$ 为

$$
P _ {L} = \frac {1}{T} \int_ {0} ^ {T} - \omega L I ^ {2} \sin (2 \omega t)   \mathrm{d} t = 0
$$

这反映了电感的非耗能的储能特性。

电容 C 吸收的瞬时功率  $p_{c}$  为

$$
\begin{array}{l} p _ {c} = i \frac {1}{C} \int i \mathrm{d} t = \frac {1}{\omega C} I _ {\mathrm{m}} ^ {2} \cos (\omega t) \sin (\omega t) \\ = \frac {1}{\omega C} I ^ {2} \sin (2 \omega t) \\ \end{array}
$$

它也是一个频率为正弦电流(或电压)频率2倍的正弦量,在正弦电流的一个周期内,吸收(储存)—释放能量2次,其吸收的平均功率 $P_{c}$ 为

$$
P _ {c} = \frac {1}{T} \int_ {0} ^ {T} \frac {1}{\omega C} I ^ {2} \sin (2 \omega t)   \mathrm{d} t = 0
$$

这反映了电容的非耗能的储能特性。

整个 RLC 串联电路吸收的瞬时功率为上述三项之和, 即

$$
\begin{array}{l} p = p _ {R} + p _ {L} + p _ {C} \\ = R I ^ {2} \left[ 1 + \cos (2 \omega t) \right] - \left(\omega L - \frac {1}{\omega C}\right) I ^ {2} \sin (2 \omega t) \\ \end{array}
$$

它是一个频率为正弦电流(或电压)频率2倍的非正弦周期量。第一项始终大于或等于零，是瞬时功率的不可逆部分，为电路所吸收的功率（此处为电阻所吸收的功率），不再返回外部电路。第二项表明，电感和电容的瞬时功率反相，在能量交换过程中，彼此互补，即电感吸收(或释放)能量时，恰好是电容释放(或吸收)能量，彼此互补后的不足部分由外部电路补充(供给)，这第二项就是 $L, C$ 之间功率互补后不足部分与外电路往复交换的瞬时功率，这是瞬时功率的可逆部分。当 $\omega L - \frac{1}{\omega C} = 0$ 时，$L, C$ 之间完全互补，第二项可逆部分将不存在，但 $L, C$ 之间吸收一释放能量的交换过程仍按原周期进行，并未消失。如果只含有一种储能元件，将不存在功率的互补情况，如果电路中不存在储能元件，则电路与外部往复交换的瞬时功率(第二项)将不会发生。

根据一端口的阻抗三角形可做如下变换:

$$
R = \left| Z \right| \cos \varphi_ {z}, \quad (\omega L - \frac {1}{\omega C}) = \left| Z \right| \sin \varphi_ {z}, \quad U = \left| Z \right| I
$$

代入后有

$$
p = U I \cos \varphi_ {z} \left[ 1 + \cos (2 \omega t) \right] - U I \sin \varphi_ {z} \sin (2 \omega t)
$$

图9-12(b)为正弦稳态电路瞬时功率的波形图 $(\varphi_{z} > 0$ 呈感性)。从该图形可以看出，在正弦电流的一个周期内有两个时区 $p \leqslant 0$ （图中斜线所示部分），当一端口为感性阻抗时，在此时区内有 $i \geqslant 0$ （或 $i \leqslant 0$），但 $|i|$ 在下降，表明电感在释放能量，而此时电容电压 $u_{c}$ 在增加（滞后电流 $90^{\circ}$），表明电容在吸收能量，因此，电感将释放的能量除了供给电阻和电容外，将多余的能量返回外电路。

上述关于正弦稳态电路瞬时功率的描述,反映了一端口电路(或元件)在能量转换过程中的状态,并为工程测量和全面反映正弦稳态电路的功率提供了理论依据。可以通过一端口的 U、I 和  $\varphi_{z}$  从如下几个方面反映正弦稳态电路的功率状态。

1. 有功功率 P(即平均功率) 定义为

$$
P \stackrel {\mathrm{def}} {=} \frac {1}{T} \int_ {0} ^ {T} p \mathrm{d} t = U I \cos \varphi_ {z}
$$

它是瞬时功率不可逆部分的恒定分量,也是其变动部分的振幅,它是衡量一端口实际所吸收的功率,其单位用 W(瓦)表示。

2. 无功功率 Q 定义为

$$
Q \stackrel {\text {def}} {=} U I \sin \varphi_ {z}
$$

它是瞬时功率可逆部分的振幅,是衡量由储能元件引起的与外部电路交换的功率,这里“无功”的意思是指这部分能量在往复交换的过程中,没有“消耗”掉。其单位用var(乏)表示。

3. 视在功率 S 定义为

$$
S \stackrel {\text { def }} {=} U I
$$

它是满足一端口电路有功功率和无功功率两者的需要时,要求外部提供的功率容量,显然有  $S \geqslant P$  和  $S \geqslant Q, P, Q$  及 S 三者的关系为

$$
P = S \cos \varphi_ {z}, \quad Q = S \sin \varphi_ {z}, \quad S = \sqrt {P ^ {2} + Q ^ {2}}
$$

这是一个直角三角形关系(S 是斜边)。工程上常用视在功率衡量电气设备在额定的电压、电流条件下最大的负荷能力,或承载能力(指对外输出有功功率的最大能力)。视在功率的单位常用 V·A (伏安)表示。

上面所用单位 W、var 和 V·A，其量纲相同，目的是区分三种不同的功率。

工程中通常用到功率因数  $\lambda$  的概念, 其定义为

$$
\lambda = \cos \varphi_ {z} \leqslant 1
$$

$\varphi_{z}$  称为功率因数角(不含独立源的一端口的阻抗角)。它是衡量传输电能效果的一个非常重要的指标,表示传输系统有功功率所占的比例,即

$$
\lambda = \frac {P}{S}
$$

实际电网非常庞大,延伸数千公里,人们当然不希望电能的往复传输,这样会增加

系统电能的消耗和增大系统设备的容量,所以,理想状态为  $\lambda=1,Q=0$ 。

上述关于正弦稳态功率的论述,虽然是通过 RLC 串联电路获得的,但它适用于任何一端口电路,具有普遍意义。

对于不含独立源的一端口,可以用等效阻抗  $Z=R+jX=|Z|/\varphi_{z}$  (串联形式的等效电路)替代,端电压  $\dot{U}$  被分解为两个分量  $\dot{U}_{R}$  和  $\dot{U}_{X}$  (参阅图9-2),其中  $\dot{U}_{R}$  产生有功功率 P,  $\dot{U}_{X}$  产生无功功率 Q,即为

$$
P = U I \cos \varphi_ {z} = I U _ {R} = I ^ {2} R
$$

$$
Q = U I \sin \varphi_ {z} = I U _ {x} = I ^ {2} X
$$

式中 $U_{R} = U\cos \varphi_{Z}$ 称为电压 $U$ 的有功分量，$U_{X} = U\sin \varphi_{Z}$ 称为电压 $U$ 的无功分量。

如用等效导纳  $Y=G+jB$  (并联等效电路) 替代, 则输入电流  $\dot{I}$  被分解为两个分量  $\dot{I}_{G}$  和  $\dot{I}_{B}$  (参阅图 9-3), 其中  $\dot{I}_{G}$  产生有功功率,  $\dot{I}_{B}$  产生无功功率, 由于  $\varphi_{Z}=-\varphi_{Y}$ , 则

$$
P = U I \cos \varphi_ {Y} = U I _ {G} = U ^ {2} G
$$

$$
Q = - U I \sin \varphi_ {Y} = - U I _ {B} = - U ^ {2} B
$$

式中  $I_{G}=I\cos\varphi_{Y}$  称为 I 的有功分量， $I_{B}=I\sin\varphi_{Y}$  称为 I 的无功分量。

对于单一的 R、L、C 元件, 可以认为是不含独立源的一端口的特例, 也适用上述有关功率的定义。

对于电阻 R，由于  $\varphi_{z}=0,\lambda=1$ ，它的有功功率和无功功率分别为

$$
P _ {R} = S \cos \varphi_ {Z} = S = U I = R I ^ {2} = G U ^ {2}
$$

$$
Q _ {R} = S \sin \varphi_ {Z} = 0
$$

对于电感 L，由于  $\varphi_{z}=90^{\circ},\lambda=0$ ，故

$$
P _ {L} = S \cos \varphi_ {z} = 0
$$

$$
Q _ {L} = S \sin \varphi_ {z} = S = U I = \dot {\omega} L I ^ {2} = \frac {U ^ {2}}{\omega L}
$$

对于电容 $C$ ，由于 $\varphi_{z} = -90^{\circ},\lambda = 0$ ，故

$$
P _ {c} = S \cos \varphi_ {z} = 0
$$

$$
Q _ {c} = S \sin \varphi_ {z} = - S = - U I = - \frac {1}{\omega C} I ^ {2} = - \omega C U ^ {2}
$$

在电路系统中,电感和电容的无功功率有互补作用,工程上认为电感吸收无功功率,而认为电容发出无功功率,将两者加以区别。

对于含有独立源的一端口电路,由于电源参与有功功率、无功功率的交换,使问题变得较为复杂,但上述有关三个功率的定义,仍然适用于含源一端口,可通过端口的电压、电流的计算获得,但功率因数将失去实际意义。设含源一端口的电压、电流分别为(关联参考方向)

$$
\begin{array}{l} i = I _ {\mathrm{m}} \cos (\omega t + \phi_ {i}) \\ u = U _ {\mathrm{m}} \cos (\omega t + \phi_ {i} + \varphi) \\ \end{array}
$$

式中  $\varphi=\phi_{u}-\phi_{i}$ ，由于有

$$
U _ {\mathrm{m}} \cos (\omega t + \phi_ {i} + \varphi) = U _ {\mathrm{m}} \cos \varphi \cos (\omega t + \phi_ {i}) - U _ {\mathrm{m}} \sin \varphi \sin (\omega t + \phi_ {i})
$$

则

$$
p = u i = U I \cos \varphi [ 1 + \cos (2 \omega t + 2 \phi_ {i}) ] - U I \sin \varphi \sin (2 \omega t + 2 \phi_ {i})
$$

瞬时功率仍然由两部分组成:不可逆部分(式中第一项)和可逆部分(式中第二项)。通过 U、I 和  $\varphi$  表示的三个功率为

$$
P = U I \cos \varphi , \quad Q = U I \sin \varphi , \quad S = U I
$$

此外 $\varphi = \phi_{u} - \phi_{i}$, 对不含独立源的一端口它就是阻抗角 $\varphi_{z}$。当一端口含有受控源时, 有可能出现 $|\varphi_{z}| > 90^{\circ}$ 的情况, 此时, 一端口发出有功功率; 当 $|\varphi_{z}| \leqslant 90^{\circ}$ 时, 含有受控源的一端口与不含受控源的一端口的情况相同。

整个电路遵守功率守恒原理,有

$$
\sum P = 0, \quad \sum Q = 0
$$

一般情况下不存在  $\Sigma S=0$ 。

例 9-9 求图 9-5(a) 所示电路中电源发出的有功功率 P、无功功率 Q、视在功率 S 和电路的功率因数  $\lambda$ 。

解 求功率必先解电路,求得各部分的电压、电流就能求得各种功率。图中电源发出的功率可根据  $\dot{U}_{s}$  和  $\dot{I}$  求得,其结果如下:

视在功率 $S_{\mathrm{s}}$ 为

$$
S _ {\mathrm{s}} = U _ {\mathrm{s}} I = 1 0 0 \times 0. 6 \mathrm{V} \cdot \mathrm{A} = 6 0 \mathrm{V} \cdot \mathrm{A}
$$

$\dot{U}_{s}$  与  $\dot{I}$  的相位差  $\varphi$  和功率因数  $\lambda$  分别为

$$
\varphi = 0 ^ {\circ} - 5 2. 3 0 ^ {\circ} = - 5 2. 3 0 ^ {\circ} \quad (\text {容性})
$$

$$
\lambda = \cos \varphi = 0. 6 1 2
$$

有功功率 P 为

$$
P = S _ {s} \lambda = 6 0 \times 0. 6 1 2 \mathrm{W} = 3 6. 7 2 \mathrm{W}
$$

无功功率 $Q$ 为

$$
Q = S _ {\mathrm{s}} \sin \cdot \varphi = - 4 7. 4 7 \text {   var }
$$

## §9-5 复功率

由上一节可知,正弦电流电路的瞬时功率等于两个同频率正弦量的乘积,其结果是一个非正弦周期量,同时它的频率也不同于电压或电流的频率,所以不能用相量法讨论。但是正弦电流电路的有功功率、无功功率和视在功率三者之间是一个直角三角形的关系,可以通过“复功率”表述。

设一端口的电压相量为  $\dot{U}$ ，电流相量为  $\dot{I}$ ，复功率  $\overline{S}$  定义为

![](images/page_249_image_27.jpg)

复功率

$$
\begin{array}{l} \overline {{S}} \stackrel {\text {def}} {=} \dot {U} \dot {I} ^ {*} = U I / \left(\phi_ {u} - \phi_ {i}\right) \\ = U I \cos \varphi + \mathrm{j} U I \sin \varphi \\ = P + \mathrm{j} Q \\ \end{array}
$$

式中  $\dot{I}^{*}$  是  $\dot{I}$  的共轭复数 $^{①}$ 。复功率的吸收或发出同样根据端口电压和电流的参考方向来判断。复功率是一个辅助计算功率的复数，它将正弦稳态电路的3种功率和功率因数统一为一个公式表示，是一个“四归一”公式。只要计算出电路中的电压和电流相量，各种功率就可以很方便地计算出来。例如求图9-5(a)所示电源发出的复功率  $\overline{S}_{a}$  为

$$
\overline {{S}} _ {\mathrm{s}} = \dot {U} _ {\mathrm{s}} \dot {I} ^ {*} = 1 0 0 \times 0. 6 / - 5 2. 3 0 \mathrm{V} \cdot \mathrm{A} = (3 6. 6 9 - \mathrm{j} 4 7. 4 7) \mathrm{V} \cdot \mathrm{A}
$$

显然,复功率将一端口的功率表述得非常简单。复功率的单位为 V·A。

最后,应当注意,复功率  $\bar{S}$  不代表正弦量,乘积  $\dot{U}\dot{I}$  是没有意义的。复功率的概念显然适用于单个电路元件或任何一端口电路。

对于不含独立源的一端口可以用等效阻抗 Z 或等效导纳 Y 替代, 则复功率  $\bar{S}$  又可表示为

$$
\overline {{S}} = \dot {U} \dot {I} ^ {*} = (\dot {I} Z) \dot {I} ^ {*} = I ^ {2} Z
$$

$$
\overline {{S}} = \dot {U} \dot {I} ^ {*} = U (Y \dot {U}) ^ {*} = U ^ {2} Y ^ {*}
$$

由  $\overline{S}$ 、P、Q 形成的三角形是一个与阻抗三角形相似的直角三角形。上式中  $Y = G + jB$ ， $Y^{*} = G - jB$ 。

可以证明,对整个电路复功率守恒,即有

$$
\sum \overline {{S}} = 0, \quad \sum P = 0, \quad \sum Q = 0
$$

例 9-10 图 9-13(a) 所示电路外加 50 Hz、380 V 的正弦电压, 感性负载吸收的功率  $P_{1}=20\ kW$ , 功率因数  $\lambda_{1}=0.6$ 。若要使电路的功率因数提高到  $\lambda=0.9$ , 求在负载的两端并接的电容值(图中虚线所示)。

![](images/page_250_image_14.jpg)

<details>
<summary>text_image</summary>

i
+
Ù
R
jωL
I₁
I₂
1
jωC
-
</details>

(a)

![](images/page_250_image_16.jpg)

<details>
<summary>text_image</summary>

S̅₁
S̅C
φz
φz₁
O
+1
</details>

(b)

![](images/page_250_image_18.jpg)

<details>
<summary>text_image</summary>

İ₂
O
φ₁
φᵢ
φᵢ₁
İ
İ₂
İ₁
(İ′)
(İ₂′)
Ü
</details>

(c)

![](images/page_250_image_20.jpg)

<details>
<summary>text_image</summary>

O
φY
+1
φY1
Y
YC
Y1
</details>

(d)

图9-13 例9-10图

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① $\overline{S}$ 的另一种定义:$\overline{S} \stackrel{\text{def}}{=} \dot{U}^{*} \dot{I}$。</span></small>

解 工程上常利用电感、电容无功功率的互补特性,通过在感性的负载端并联电容来提高电路的功率因数。接入电容后,不会改变原负载的工作状态,而利用电容发出的无功功率,部分(或全部)补偿感性负载所吸收的无功功率,从而减轻了电源和传输系统的无功功率的负担。

解法一:根据复功率守恒原理求解。

接入电容 C 后,根据复功率守恒原理有

$$
\overline {{S}} = \overline {{S}} _ {1} + \overline {{S}} _ {c}
$$

$\overline{S}$ 为并联电容C后电源发出的复功率,设阻抗角为 $\varphi_{z},\overline{S}_{1}$ 为支路1吸收的复功率,设其阻抗角为 $\varphi_{z1}$ ,而 $\overline{S}_{c}=-j\omega CU^{2}$ 为电容吸收的复功率,这些复功率组成了功率三角形,如图9-13(b)所示,上式复功率方程分列为

$$
S \cos \varphi_ {z} = S _ {1} \cos \varphi_ {z 1} = P _ {1} \quad (\text {有功功率})
$$

$$
S \sin \varphi_ {z} = S _ {1} \sin \varphi_ {z 1} - \omega C U ^ {2}
$$

从以上两式解得

$$
C = \frac {P _ {1}}{\dot {\omega} U ^ {2}} (\tan \varphi_ {z 1} - \tan \varphi_ {z})
$$

式中

$$
\varphi_ {z} = \arccos \lambda = 2 5. 8 4 ^ {\circ} \quad (\text {感性})
$$

$$
\varphi_ {z 1} = \arccos \lambda_ {1} = 5 3. 1 3 ^ {\circ} \quad (\text {感性})
$$

最后有

$$
C = 3 7 4. 5 1 \mu \mathrm{F}
$$

解法二:根据 KCL 电流方程求解。

并入电容 C 后, 根据 KCL 有

$$
\dot {I} = \dot {I} _ {1} + \dot {I} _ {2}
$$

令 $\dot{U} = 380 / 0^{\circ}\mathrm{V}$ （参考相量）， $\dot{I} = I / \phi_{i}$ （并联电容后）， $\dot{I}_1 = I_1 / \phi_{i1}$ 和 $\dot{I}_2 = \mathrm{j}\omega C\dot{U}$ ，电流三角形如图9-13(c)中实线所示，则电流方程可分列为

$$
I \cos \phi_ {i} = I _ {1} \cos \phi_ {i 1} \quad (\text {有功分量})
$$

$$
I \sin \phi_ {i} = I _ {1} \sin \phi_ {i 1} + \omega C U \quad (\text {无功分量})
$$

并有

$$
U I _ {1} \cos \phi_ {i 1} = P _ {1}
$$

则解得

$$
C = \frac {P _ {1}}{\omega U ^ {2}} (\tan \phi_ {i} - \tan \phi_ {i 1})
$$

式中， $\phi_{i}=-\varphi_{z},\phi_{i1}=-\varphi_{z1}$ ，这里  $\varphi_{z}$  和  $\varphi_{z1}$  分别为并联电容后的阻抗角和支路 1 的阻抗角，所以

$$
\phi_ {i} = - \arccos \lambda = - 2 5. 8 4 ^ {\circ} \quad (\text {感性})
$$

$$
\phi_ {i 1} = - \arccos \lambda_ {1} = - 5 3. 1 3 ^ {\circ} \quad (\text {感性})
$$

可求得同样结果。表明，并联电容后，容性和感性的无功电流分量有互补作用。

解法三:根据等效导纳求解。

并接入电容 C 后有

$$
Y = Y _ {1} + Y _ {c}
$$

设 $Y = |Y| / \varphi_Y$ （并联电容后），$Y_{1} = |Y_{1}| / \varphi_{Y1}$ （支路1），而 $Y_{C} = \mathrm{j}\omega C$ ，导纳三角形如图9-13(d)所示，则导纳方程可分列为

$$
\mid Y \mid \cos \phi_ {Y} = \mid Y _ {1} \mid \cos \varphi_ {Y 1} \quad (\text {实部})
$$

$$
\mid Y \mid \sin \phi_ {Y} = \mid Y _ {1} \mid \sin \varphi_ {Y 1} + \omega C \quad (\text {虚部})
$$

又由于  $\left|Y_{1}\right|\cos\varphi_{Y1}U^{2}=P_{1}$ ，则解得

$$
C = \frac {P _ {1}}{\omega U ^ {2}} (\tan \varphi_ {Y} - \tan \varphi_ {Y 1})
$$

式中  $\varphi_{Y}=\arccos\lambda=-25.84^{\circ}$  （感性）

$$
\varphi_ {Y 1} = \arccos \lambda_ {1} = - 5 3. 1 3 ^ {\circ} \quad (\text {感性})
$$

图 9-13(c) 中虚线所示是符合要求的另一解答, 功率因数角  $\varphi_{z} = -25.84^{\circ}$  (容性), 需要更大的电容量, 经济上不可取。

通过这个例子可以看出功率因数提高的经济意义。并联电容后  $S < S_{1}, I < I_{1}$ ，这样既提高了电源设备的利用率，也减少了传输线上的损耗。

读者请思考:能否采用串联电容或串联电阻的方法提高功率因数?

## §9-6 最大功率传输

图 9-14(a) 所示电路为含源一端口  $N_{s}$  向终端负载 Z 传输功率, 当传输的功率较小 (如通信系统、电子电路中), 而不必计较传输效率时, 常常要研究使负载获得最大功率 (有功) 的条件。根据戴维南定理, 该问题可以简化为图 9-14(b) 所示等效电路进行研究。

![](images/page_252_image_19.jpg)

<details>
<summary>text_image</summary>

Ns
1
+
Ü
-
1'
i
Z
</details>

(a)

![](images/page_252_image_21.jpg)

<details>
<summary>text_image</summary>

Zeq
1
+
Üoc
Ü
I'
Z
-
1'
</details>

(b)

图 9-14 最大功率传输

设 $Z_{\mathrm{eq}} = R_{\mathrm{eq}} + \mathrm{j}X_{\mathrm{eq}}, Z = R + \mathrm{j}X$ ，则负载吸收的有功功率为

![](images/page_252_image_25.jpg)

<details>
<summary>natural_image</summary>

Pure technical line drawing of a mechanical assembly without any text, numbers, or symbols
</details>

![](images/page_252_image_26.jpg)

最大功率传输

$$
P = I ^ {2} R = \frac {U _ {\mathrm{oo}} ^ {2} R}{\left(R + R _ {\mathrm{eq}}\right) ^ {2} + \left(X _ {\mathrm{eq}} + X\right) ^ {2}}
$$

从上式可以看出,负载端获得的功率与一端口的等效参数(内部)和负载的参数(外部)有关,在内部不便变动的情况下(且 $U_{oc}\neq0$ ),则负载Z必须根据 $Z_{eq}$ 进行配置(匹配),才可能获得最大功率。配置条件不同,获得的最大功率也不同。如果R和X可以任意变动,而其他参数不变时,则获得最大功率的条件为

$$
\left. \begin{array}{l} X + X _ {\mathrm{eq}} = 0 \\ \frac {\mathrm{d}}{\mathrm{d} R} \left[ \frac {R}{\left(R + R _ {\mathrm{eq}}\right) ^ {2}} \right] = 0 \end{array} \right\}
$$

解得  $\left.\begin{aligned} X &= -X_{\mathrm{eq}} \\ R &= R_{\mathrm{eq}} \end{aligned}\right\}$

即有 $Z = R_{\mathrm{eq}} - \mathrm{j}X_{\mathrm{eq}} = Z_{\mathrm{eq}}^{*}$

此时获得的最大功率为

$$
P _ {\max} = \frac {U _ {\mathrm{oc}} ^ {2}}{4 R _ {\mathrm{eq}}}
$$

当用诺顿等效电路时,获最大功率的条件可表示为

$$
Y = Y _ {\mathrm{eq}} ^ {*}
$$

上述获最大功率的条件称为最佳匹配(共轭匹配)。工程上还可以根据其他的匹配条件求解最大功率。在此不一一列举。

例 9-11 图 9-15 所示电路中的正弦电源  $\dot{U}_{s}=10/-45^{\circ}V$ ，负载  $Z_{L}$  可任意变动。求  $Z_{L}$  可能获得的最大功率（分 3 种情况:g=0.5 S, -0.5 S 和 1 S）。

![](images/page_253_image_14.jpg)

<details>
<summary>text_image</summary>

1 Ω
-j1 Ω
+ U_s -
j1 Ω
1
2 Ω
2
gU̇₁₀
1
i
Z_L
0
1'
</details>

图 9-15 例 9-11 图

解 求一端口  $1-1'$  的戴维南等效电路。用电流源  $\dot{I}$  替代  $Z_{L}$  后，节点方程为

$$
\begin{array}{l} \left(\frac {1}{1 - \mathrm{j}} + \frac {1}{\mathrm{j}} + \frac {1}{2}\right) \dot {U} _ {1 0} - \frac {1}{2} \dot {U} _ {2 0} = \frac {\dot {U} _ {\mathrm{s}}}{1 - \mathrm{j}} \\ - \frac {1}{2} \dot {U} _ {1 0} + \frac {1}{2} \dot {U} _ {2 0} - g \dot {U} _ {1 0} = - \dot {I} \\ \end{array}
$$

解得

$$
\dot {U} _ {2 0} = \dot {U} _ {1 1 ^ {\prime}} = \frac {1 + 2 g}{- g + \mathrm{j} (g - 1)} \dot {U} _ {\mathrm{s}} - \frac {1 - \mathrm{j} 3}{- g + \mathrm{j} (g - 1)} \dot {I}
$$

戴维南等效电路的参数为

$$
\dot {U} _ {\mathrm{oc}} = \frac {1 + 2 g}{- \mathrm{g} + \mathrm{j} (g - 1)} \dot {U} _ {\mathrm{s}}, \quad Z _ {\mathrm{eq}} = \frac {1 - \mathrm{j} 3}{- \mathrm{g} + \mathrm{j} (g - 1)}
$$

(1) 当 g=0.5 S 时, 有

$$
\dot {U} _ {\mathrm{oc}} = 2 0 \sqrt {2} / 9 0 ^ {\circ} \mathrm{V}, \quad Z _ {\mathrm{eq}} = (2 + \mathrm{j} 4) \Omega
$$

当 $Z_{\mathrm{L}} = Z_{\mathrm{eq}}^{*} = (2 - \mathrm{j}4)\Omega$ 时，$Z_{\mathrm{L}}$ 可获最大功率为

$$
P _ {\max} = \frac {U _ {\mathrm{oc}} ^ {2}}{2 \times 4} = 1 0 0 \mathrm{W}
$$

(2) 当  $g = -0.5 \, S$  时, 有

$$
\dot {U} _ {\mathrm{oc}} = 0, \quad Z _ {\mathrm{eq}} = 2 \Omega
$$

得最佳匹配,但一端口无功率输出。

(3) 当 g=1 S 时，

$$
\dot {U} _ {\mathrm{oc}} = 3 0 / 1 3 5 ^ {\circ} \mathrm{V}, \quad Z _ {\mathrm{eq}} = (- 1 + \mathrm{j} 3) \Omega
$$

该情况留给读者分析、讨论。

![](images/page_254_image_16.jpg)

## 思考题

9-1 在正弦稳态电路中,一端口的阻抗和导纳的定义与电阻电路的电阻和电导定义的区别和联系?
9-2 对于正弦一端口, 端口的电压有效值一定大于其中一个元件电压的有效值吗? 说明理由。
9-3 对于正弦稳态一端口,当阻抗的实部小于零时,该一端口具有何种特性?
9-4 当采用相量图辅助分析正弦稳态电路时,如何选择参考相量?
9-5 在正弦稳态电路中,什么条件下可以不用相量分析法,而直接使用有效值或瞬时值进行计算?
9-6 无功功率的含义是什么？它的本质是什么？
9-7 如果正弦稳态电路的视在功率等于有功功率,它是否还含有电抗元件?
9-8 试说明提高功率因数的意义和方法。
9-9 为什么正弦电路中,视在功率不守恒,而复功率守恒?

![](images/page_254_image_28.jpg)

## 习题

9-1 试求题 9-1 图所示各电路的输入阻抗 Z 和导纳 Y。

![](images/page_255_image_3.jpg)

<details>
<summary>text_image</summary>

1 Ω
j2 Ω
-j1 Ω
</details>

(a)

![](images/page_255_image_5.jpg)

<details>
<summary>text_image</summary>

1 Ω
- j1 Ω
1 Ω
j1 Ω
</details>

(b)

![](images/page_255_image_7.jpg)

<details>
<summary>text_image</summary>

40 Ω
40 Ω
-j40 Ω
j40 Ω
</details>

(c)

![](images/page_255_image_9.jpg)

<details>
<summary>text_image</summary>

i
jωL
R
+
-
rI
-
</details>

(d)

题 9-1 图

9-2 将题 9-2 图所示三角形 [图(a)] 和星形 [图(b)] 联结的电路转换为等效星形和三角形联结的电路。

![](images/page_255_image_13.jpg)

<details>
<summary>text_image</summary>

1. j8 Ω
4 Ω -j4 Ω
3
</details>

(a)

![](images/page_255_image_15.jpg)

<details>
<summary>text_image</summary>

1
1 Ω
j1 Ω
2
-j0.5 Ω
3
</details>

(b)

题9-2图

9-3 题 9-3 图中 N 为不含独立源的一端口, 端口电压 u、电流 i 分别如下列各式所示。试求每一种情况下的输入阻抗 Z 和导纳 Y, 并给出等效电路图(包括元件的参数值)。

(1) $\left\{ \begin{array}{l} u = 200 \cos(314t) \mathrm{~V} \\ i = 10 \cos(314t) \mathrm{~A} \end{array} \right.$;

(2) $\left\{\begin{aligned}u=10\cos(10t+45^{\circ})&V\\ i=2\cos(10t-90^{\circ})&A\end{aligned}\right.$ ;

(3) $\left\{ \begin{array}{l} u = 100 \cos (2t + 60^{\circ}) \mathrm{~V} \\ i = 5 \cos (2t - 30^{\circ}) \mathrm{~A} \end{array} \right.$;

(4) $\left\{\begin{aligned}u=40\cos\left(100t+17^{\circ}\right)&V\\ i=8\sin\left(100t+\frac{\pi}{2}\right)&A\end{aligned}\right.$

![](images/page_255_image_23.jpg)

<details>
<summary>text_image</summary>

i
+
u
N
-
</details>

题9-3图