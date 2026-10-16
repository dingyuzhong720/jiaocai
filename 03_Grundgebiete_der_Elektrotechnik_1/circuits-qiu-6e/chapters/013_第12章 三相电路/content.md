# 第12章 三相电路

原始 PDF 第 305–318 页。

第十二章

三相电路

The image contains no text or mathematical content to process. It is a graphical representation of a triangular shape with dense, pixelated patterns. Therefore, the correct OCR output is an empty string.

## 导读

目前，世界各国的电力系统中电能的生产、传输和供电方式绝大多数都采用三相制。它是世界上规模最大的生产系统，系统的结构为适应工业化生产的需要，已经标准化或规范化，它主要是由三相电源、三相负载和三相输电线路三部分组成。三相交流发电机、变压器和三相制的发明是人类社会跨入电气化时代的里程碑，至今已有100多年的发展史，是当今社会发展的物质基础之一。

本章将系统介绍三相制电路。理论上它是正弦稳态电路的一部分,通过学习可以了解三相制电路的特殊性和解决问题的特殊方法,学习一些用电知识和启发创新思维。

## §12-1 三相电路

三相电路是由三相电源、三相负载和三相输电线路三部分组成。

对称三相电源是由3个同频率、等幅值、初相依次滞后 $120^{\circ}$ 的正弦电压源连接成星形(Y)或三角形( $\Delta$ )组成的电源,如图12-1(a)(b)所示。这3个电源依次称为A相、B相和C相,它们的电压瞬时表达式及其相量分别为

$$
\begin{array}{l} u _ {\mathrm{A}} = \sqrt {2} U \cos (\omega t) \quad \dot {U} _ {\mathrm{A}} = U / 0 ^ {\circ} \\ u _ {\mathrm{B}} = \sqrt {2} U \cos (\omega t - 1 2 0 ^ {\circ}) \quad \dot {U} _ {\mathrm{B}} = U / - 1 2 0 ^ {\circ} = a ^ {2} \dot {U} _ {\mathrm{A}} \\ u _ {\mathrm{C}} = \sqrt {2} U \cos (\omega t + 1 2 0 ^ {\circ}) \quad \dot {U} _ {\mathrm{C}} = U / 1 2 0 ^ {\circ} = a \dot {U} _ {\mathrm{A}} \\ \end{array}
$$

式中以 A 相电压  $u_{A}$  作为参考正弦量。 $a=1/120^{\circ}$ ，它是工程中为了方便而引入的单位相量算子。

上述三相电压的相序(次序)A、B、C称为正序或顺序。与此相反,如B相超前A相120°,C相超前B相120°,这种相序称为负序或逆序。相位差为零的相序称为零序。电力系统一般采用正序。

对称三相电压各相的波形和相量图如图 12-1(c)(d) 所示。对称三相电压满足:

![](../../raw/pages_0289-0320/images/page_304_image_13.jpg)

三相电路

---

282

第十二章 三相电路

$$
u _ {\mathrm{A}} + u _ {\mathrm{B}} + u _ {\mathrm{C}} = 0 \quad \text {或} \quad \dot {U} _ {\mathrm{A}} + \dot {U} _ {\mathrm{B}} + \dot {U} _ {\mathrm{C}} = 0
$$

对称三相电压源是由三相发电机提供的(我国三相系统电源频率 $f=50\ Hz$ , 入户电压为220 V, 而日、美、欧洲等国为60 Hz, 110 V)。

图 12-1(a) 所示为三相电压源的星形连接方式, 简称星形或 Y 形电源。从 3 个电压源正极性端子 A、B、C 向外引出的导线称为端线, 从中性点 N 引出的导线称为中性线 (旧称零线)。把三相电压源依次连接成一个回路, 再从端子 A、B、C 引出端线, 如图 12-1(b) 所示, 就成为三相电源的三角形联结, 简称三角形或  $\Delta$  形电源。三角形电源不能引出中性线。

![](../../raw/pages_0289-0320/images/page_305_image_6.jpg)

<details>
<summary>text_image</summary>

ÛA + A
- ÛB + B
N - ÛC + C
N
</details>

(a)

![](../../raw/pages_0289-0320/images/page_305_image_8.jpg)

<details>
<summary>text_image</summary>

uA
+
-
uC
+
-
xB
A
B
C
-
</details>

(b)

![](../../raw/pages_0289-0320/images/page_305_chart_10.jpg)

<details>
<summary>line</summary>

| \(\omega t\) | uA | uB | uC |
| --- | --- | --- | --- |
| 0 | 0 | 0 | 0 |
| \(\pi/2\) | ~0.87 | 0 | 0 |
| \(3\pi/4\) | 0 | ~-0.87 | 0 |
| \(5\pi/6\) | 0 | 0 | ~0.87 |
| \(7\pi/8\) | 0 | ~0.87 | 0 |
| \(9\pi/10\) | 0 | 0 | ~-0.87 |
| \(11\pi/12\) | 0 | 0 | 0 |
| \(13\pi/14\) | 0 | ~-0.87 | ~0.87 |
| \(15\pi/16\) | 0 | 0 | 0 |
| \(17\pi/18\) | 0 | ~0.87 | ~-0.87 |
| \(19\pi/20\) | 0 | 0 | 0 |
| \(21\pi/22\) | 0 | 0 | ~0.87 |
| \(23\pi/24\) | 0 | 0 | 0 |
| \(25\pi/26\) | 0 | ~-0.87 | ~-0.87 |
| \(27\pi/28\) | 0 | 0 | 0 |
| \(29\pi/29\) | 0 | ~0.87 | ~-0.87 |
| \(31\pi/30\) | 0 | 0 | 0 |
| \(33\pi/31\) | 0 | 0 | ~0.87 |
| \(35\pi/32\) | 0 | 0 | 0 |
| \(37\pi/33\) | 0 | ~-0.87 | ~-0.87 |
| \(39\pi/34\) | 0 | 0 | 0 |
| \(41\pi/35\) | 0 | ~0.87 | ~-0.87 |
| \(43\pi/36\) | 0 | 0 | 0 |
| \(45\pi/37\) | 0 | 0 | ~0.87 |
| \(47\pi/38\) | 0 | 0 | 0 |
| \(49\pi/39\) | 0 | ~-0.87 | ~-0.87 |
| \(51\pi/40\) | 0 | 0 | 0 |
| \(53\pi/41\) | 0 | ~0.87 | ~-0.87 |
| \(55\pi/42\) | 0 | 0 | 0 |
| \(57\pi/43\) | 0 | 0 | ~0.87 |
| \(59\pi/44\) | 0 | 0 | 0 |
| \(61\pi/45\) | 0 | ~-0.87 | ~-0.87 |
| \(63\pi/46\) | 0 | 0 | 0 |
| \(65\pi/47\) | 0 | ~0.87 | ~-0.87 |
| \(67\pi/48\) | 0 | 0 | 0 |
| \(69\pi/49\) | 0 | 0 | ~0.87 |
| \(71\pi/50\) | 0 | 0 | 0 |
| \(73\pi/51\) | 0 | ~-0.87 | ~-0.87 |
| \(75\pi/52\) | 0 | 0 | 0 |
| \(77\pi/53\) | 0 | ~0.87 | ~-0.87 |
| \(79\pi/54\) | 0 | 0 | 0 |
| \(81\pi/55\) | 0 | 0 | ~0.87 |
| \(83\pi/56\) | 0 | 0 | 0 |
| \(85\pi/57\) | 0 | ~-0.87 | ~-0.87 |
| \(87\pi/58\) | 0 | 0 | 0 |
| \(89\pi/59\) | 0 | ~0.87 | ~-0.87 |
| \(91\pi/60\) | 0 | 0 | 0 |
| \(93\pi/61\) | 0 | 0 | ~0.87 |
| \(95\pi/62\) | 0 | 0 | 0 |
| \(97\pi/63\) | 0 | ~-0.87 | ~-0.87 |
| \(99\pi/64\) | 0 | 0 | 0 |
</details>

(c)

![](../../raw/pages_0289-0320/images/page_305_image_12.jpg)

<details>
<summary>text_image</summary>

ÛC
120°
O
ÛA
120°
ÛB
</details>

(d)

图12-1 对称三相电压源连接及其电压波形和相量图

3 个阻抗连接成星形(或三角形)就构成星形(或三角形)负载,如图 12-2 所示。当这 3 个阻抗相等时,就称为对称三相负载。

从对称三相电源的3个端子引出具有相同阻抗的3条端线(或输电线)，把一些对称三相负载连接在端线上就形成了对称三相电路。图12-2(a)(b)为两个对称三相电路的示例。图(a)中的三相电源为星形电源，负载为星形负载，称为Y-Y连接方式(实线所示部分)；图(b)中，三相电源为星形电源，负载为三角形负载，称为Y-Δ连接方

---

§ 12-2 线电压(电流)与相电压(电流)的关系

283

式。还有  $\Delta-Y$  和  $\Delta-\Delta$  连接方式。

在 Y-Y 联结中,如把三相电源的中性点 N 和负载的中性点 N' 用一条具有阻抗为  $Z_{N}$  的中性线连接起来,如图 12-2(a) 中虚线所示,这种连接方式称为三相四线制方式。上述其余连接方式均属三相三线制。

![](../../raw/pages_0289-0320/images/page_306_image_4.jpg)

图 12-2 对称三相电路

实际三相电路中,三相电源是对称的,3条端线阻抗是相等的,但负载则不一定是对称的。

## §12-2 线电压(电流)与相电压(电流)的关系

三相系统中，流经输电线中的电流称为线电流，如图12-2(a)(b)所示的 $\dot{I}_{\mathrm{A}}$ 、 $\dot{I}_{\mathrm{B}}$ 、$\dot{I}_{\mathrm{C}}$ ， $\dot{I}_{\mathrm{N}}$ 称为中性线的电流。各输电线线端之间的电压，如图12-2(a)(b)中所示电源端的 $\dot{U}_{\mathrm{AB}}$ 、 $\dot{U}_{\mathrm{BC}}$ 、 $\dot{U}_{\mathrm{CA}}$ 和负载端的 $\dot{U}_{\mathrm{A'B'}}$ 、 $\dot{U}_{\mathrm{B'C'}}$ 、 $\dot{U}_{\mathrm{C'A'}}$ ，都称为线电压。三相电源和三相负载中每一相的电压、电流称为相电压和相电流。三相系统中的线电压和相电压、线电流和相电流之间的关系都与连接方式有关。

对于对称星形电源，依次设其线电压为  $\dot{U}_{AB}$ 、 $\dot{U}_{BC}$ 、 $\dot{U}_{CA}$ ，相电压为  $\dot{U}_{A}$ 、 $\dot{U}_{B}$ 、 $\dot{U}_{C}$ （或  $\dot{U}_{AN}$ 、 $\dot{U}_{BN}$ 、 $\dot{U}_{CN}$ ），如图 12-1(a) 所示，根据 KVL，有

$$
\begin{array}{l} \dot {U} _ {\mathrm{AB}} = \dot {U} _ {\mathrm{A}} - \dot {U} _ {\mathrm{B}} = (1 - a ^ {2}) \dot {U} _ {\mathrm{A}} = \sqrt {3} \dot {U} _ {\mathrm{A}} / 3 0 ^ {\circ} \\ \dot {U} _ {\mathrm{BC}} = \dot {U} _ {\mathrm{B}} - \dot {U} _ {\mathrm{C}} = (1 - a ^ {2}) \dot {U} _ {\mathrm{B}} = \sqrt {3} \dot {U} _ {\mathrm{B}} / 3 0 ^ {\circ} \\ \dot {U} _ {\mathrm{CA}} = \dot {U} _ {\mathrm{C}} - \dot {U} _ {\mathrm{A}} = (1 - a ^ {2}) \dot {U} _ {\mathrm{C}} = \sqrt {3} \dot {U} _ {\mathrm{C}} / 3 0 ^ {\circ} \end{array} \tag {12-1}
$$

另有  $\dot{U}_{AB} + \dot{U}_{BC} + \dot{U}_{CA} = 0$  。对称的星形三相电源端的线电压与相电压之间的关系，可用一种特殊的电压相量图表示，如图 12-3(a) 所示①。它是由式(12-1)三个公式的相量图拼接而成，图中实线所示部分表示  $\dot{U}_{AB}$  的图解方法，它是以 B 为原点画出  $\dot{U}_{AB} =$

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 注意,图中的电压相量是按该电压下标的相反次序画的。例如画  $\dot{U}_{AN}$  时,应从 N 点指向 A 点,画  $\dot{U}_{AB}$  时,应从 B 点指向 A 点。A、B、C、N 点则表示电压源的对应端子。</span></small>

The image provided is a QR code. It does not contain any text, mathematical formulas, tables, or figures that can be processed according to the given instructions. Therefore, no OCR output can be generated from this image.

线电压（电流）与相电压（电流）的关系

---

284

第十二章 三相电路

$(-\dot{U}_{\mathrm{BN}})+\dot{U}_{\mathrm{AN}}$ ，其他线电压的图解求法类同。从图中可以看出，线电压与对称相电压之间的关系可以用图示电压正三角形说明，相电压对称时，线电压也一定依序对称，它是相电压的 $\sqrt{3}$ 倍，依次超前 $\dot{U}_{A}$ 、 $\dot{U}_{B}$ 、 $\dot{U}_{C}$ 相位 $30^{\circ}$ ，实际计算时，只要算出 $\dot{U}_{AB}$ ，就可以依序写出 $\dot{U}_{BC}=a^{2}\dot{U}_{AB},\dot{U}_{CA}=a\dot{U}_{AB}$ 。

对于三角形电源[如图12-1(b)所示],有

$$
\dot {U} _ {\mathrm{AB}} = \dot {U} _ {\mathrm{A}}, \dot {U} _ {\mathrm{BC}} = \dot {U} _ {\mathrm{B}}, \dot {U} _ {\mathrm{CA}} = \dot {U} _ {\mathrm{C}}
$$

所以线电压等于相电压,相电压对称时,线电压也一定对称。

以上有关线电压和相电压的关系也适用于对称星形负载端和三角形负载端。

对称三相电源和三相负载中的线电流和相电流之间的关系叙述如下。

对于星形联结,线电流显然等于相电流,对三角形联结则不是如此。以图12-2(b)所示三角形负载为例,设每相负载中的对称相电流分别为 $\dot{I}_{A'B'}$ 、 $\dot{I}_{B'C'}(=a^{2}\dot{I}_{A'B'})$ 、 $\dot{I}_{C'A'}(=a\dot{I}_{A'B'})$ ，3个线电流依次分别为 $\dot{I}_{A}$ 、 $\dot{I}_{B}$ 、 $\dot{I}_{C}$ ，电流的参考方向如图所示。根据KCL,有

$$
\left. \begin{array}{l} \dot {I} _ {\mathrm{A}} = \dot {I} _ {\mathrm {A^{\prime} B^{\prime}}} - \dot {I} _ {\mathrm {C^{\prime} A^{\prime}}} = (1 - a) \dot {I} _ {\mathrm {A^{\prime} B^{\prime}}} = \sqrt {3} \dot {I} _ {\mathrm {A^{\prime} B^{\prime}}} / - 3 0 ^ {\circ} \\ \dot {I} _ {\mathrm{B}} = \dot {I} _ {\mathrm {B^{\prime} C^{\prime}}} - \dot {I} _ {\mathrm {A^{\prime} B^{\prime}}} = (1 - a) \dot {I} _ {\mathrm {B^{\prime} C^{\prime}}} = \sqrt {3} \dot {I} _ {\mathrm {B^{\prime} C^{\prime}}} / - 3 0 ^ {\circ} \\ \dot {I} _ {\mathrm{C}} = \dot {I} _ {\mathrm {C^{\prime} A^{\prime}}} - \dot {I} _ {\mathrm {B^{\prime} C^{\prime}}} = (1 - a) \dot {I} _ {\mathrm {C^{\prime} A^{\prime}}} = \sqrt {3} \dot {I} _ {\mathrm {C^{\prime} A^{\prime}}} / - 3 0 ^ {\circ} \end{array} \right\} \tag {12-2}
$$

另有 $\dot{I}_{\mathrm{A}} + \dot{I}_{\mathrm{B}} + \dot{I}_{\mathrm{C}} = 0$ 。所以，上述3个方程中，只有2个方程是独立的。线电流与对称相电流之间的关系，也可以用一种特殊的电流相量图表示，如图12-3(b)所示，图中实线部分表示 $\dot{I}_{\mathrm{A}}$ 的图解求法，其他线电流的图解求法类同。从图中可以看出，线电流与对称的三角形负载相电流之间的关系，可以用一个电流正三角形说明，相电流对称时，线电流也一定对称，它是相电流的 $\sqrt{3}$ 倍，依次滞后 $\dot{I}_{\mathrm{A'B'}}$、$\dot{I}_{\mathrm{B'C'}}$、$\dot{I}_{\mathrm{C'A'}}$ 的相位为 $30^{\circ}$ 。实际计算时，只要计算出 $\dot{I}_{\mathrm{A}}$，就可依次写出 $\dot{I}_{\mathrm{B}} = a^{2} \dot{I}_{\mathrm{A}}$，$\dot{I}_{\mathrm{C}} = a \dot{I}_{\mathrm{A}}$。

![](../../raw/pages_0289-0320/images/page_307_image_12.jpg)

<details>
<summary>text_image</summary>

C
ÛCA
ÛCN
ÛAN
N
A
-ÛBN
ÛAB
B
</details>

(a)

![](../../raw/pages_0289-0320/images/page_307_image_14.jpg)

<details>
<summary>text_image</summary>

İA
-İC'A'
İA'B'
İB'C'
İB
</details>

(b)

图12-3 线值和相值之间的关系

上述分析方法也适用于三角形电源。

最后还必须指出,所有关于电压、电流的对称性以及上述对称相值和对称线值之间

---

§ 12-3 对称三相电路的计算

285

关系的论述,只能在指定的顺序和参考方向的条件下,才能以简单有序的形式表达出来,而不能任意设定(理论上可以),否则将会使问题的表述变得杂乱无序。

## §12-3 对称三相电路的计算

对称三相电路是一类特殊类型的正弦电流电路。因此，分析正弦电流电路的相量法对对称三相电路完全适用。但本节根据对称三相电路的一些特点，来简化对称三相电路分析计算。

现在，以对称三相四线制电路为例来进行分析，如图12-2(a)所示，其中 $Z_{1}$ 为线路阻抗，$Z_{\mathrm{N}}$ 为中性线阻抗。N和 $\mathbf{N}'$ 为中性点。对于这种电路，一般可用节点法先求出中性点 $\mathbf{N}'$ 与N之间的电压。以N为参考节点，可得

$$
\left(\frac {1}{Z _ {\mathrm{N}}} + \frac {3}{Z + Z _ {1}}\right) \dot {U} _ {\mathrm {N ^ {\prime} N}} = \frac {1}{Z _ {1} + Z} (\dot {U} _ {\mathrm{A}} + \dot {U} _ {\mathrm{B}} + \dot {U} _ {\mathrm{C}})
$$

由于 $\dot{U}_{\mathrm{A}} + \dot{U}_{\mathrm{B}} + \dot{U}_{\mathrm{C}} = 0$ ，所以 $\dot{U}_{\mathrm{N^{\prime}N}} = 0$ ，各相电源和负载中的相电流等于线电流，它们是

$$
\dot {I} _ {\mathrm{A}} = \frac {\dot {U} _ {\mathrm{A}} - \dot {U} _ {\mathrm {N^{\prime} N}}}{Z + Z _ {1}} = \frac {\dot {U} _ {\mathrm{A}}}{Z + Z _ {1}}
$$

$$
\dot {I} _ {\mathrm{B}} = \frac {\dot {U} _ {\mathrm{B}}}{Z + Z _ {1}} = a ^ {2} \dot {I} _ {\mathrm{A}}
$$

$$
\dot {I} _ {\mathrm{c}} = \frac {\dot {U} _ {\mathrm{c}}}{Z + Z _ {1}} = a \dot {I} _ {\mathrm{A}}
$$

可以看出,各线(相)电流独立, $\dot{U}_{N'N}=0$ 是各线(相)电流独立,彼此无关的必要和充分条件,所以,对称的Y-Y电路可分列为三个独立的单相电路。又由于三相电源、三相负载的对称性,所以线(相)电流构成对称组。因此,只要分析计算三相中的任一相,

而其他两线（相）的电流就能按对称顺序写出。这就是对称的Y-Y三相电路归结为一相的计算方法。图12-4为一相计算电路（A相）。注意，在一相计算电路中，连接N、N'的短路线是 $\dot{U}_{N'N}=0$ 的等效线，与中性线阻抗 $Z_{N}$ 无关。另外，中性线的电流为

$$
\dot {I} _ {\mathrm{N}} = \dot {I} _ {\mathrm{A}} + \dot {I} _ {\mathrm{B}} + \dot {I} _ {\mathrm{C}} = 0
$$

![](../../raw/pages_0289-0320/images/page_308_image_14.jpg)

<details>
<summary>text_image</summary>

- \u221a_A + \nZ_1 \u221a_I_A \u221a_Z
\u221a_{N'N} = 0
N N'
</details>

图 12-4 一相计算电路

这表明,对称的 Y-Y 三相电路,在理论上不需要中性线,可以移去。而在任一时刻, $i_{A}$ 、 $i_{B}$ 、 $i_{C}$ 中至少有一个为负值,对应此负值电流的输电线则作为对称电流系统在该时刻的电流回线。

对于其他连接方式的对称三相电路,可以根据星形和三角形的等效互换,化成对称的 Y-Y 三相电路,然后用一相计算法求解。

![](../../raw/pages_0289-0320/images/page_308_image_18.jpg)

对称三相电路的计算

---

图2

286

第十二章 三相电路

例 12-1 对称三相电路如图 12-2(a) 所示, 已知  $Z_{1}=(1+j2)\Omega, Z=(5+j6)\Omega, u_{AB}=380\sqrt{2}\cos(\omega t+30^{\circ})V$ 。试求负载中各电流相量。

解 可设一组对称三相电压源与该组对称线电压对应。根据式(12-1)的关系,有

$$
\dot {U} _ {\mathrm{A}} = \frac {\dot {U} _ {\mathrm{AB}}}{\sqrt {3}} \angle - 3 0 ^ {\circ} = 2 2 0 \angle 0 ^ {\circ} \mathrm{V}
$$

据此可画出一相(A 相)计算电路,如图 12-4 所示。可以求得

$$
\dot {I} _ {\mathrm{A}} = \frac {\dot {U} _ {\mathrm{A}}}{Z + Z _ {1}} = \frac {2 2 0 / 0 ^ {\circ}}{6 + \mathrm{j} 8} \mathrm{A} = 2 2 / - 5 3. 1 ^ {\circ} \mathrm{A}
$$

根据对称性可以写出

$$
\dot {I} _ {\mathrm{B}} = a ^ {2} \dot {I} _ {\mathrm{A}} = 2 2 / - 1 7 3. 1 ^ {\circ} \mathrm{A}, \quad \dot {I} _ {\mathrm{C}} = a \dot {I} _ {\mathrm{A}} = 2 2 / 6 6. 9 ^ {\circ} \mathrm{A}
$$

对称三相电路的相量图,可将 A 线(相)的相量图依序顺时针旋转  $120^{\circ}$  合成。

例 12-2 对称三相电路如图 12-2(b) 所示。已知  $Z=(19.2+j14.4)\Omega, Z_{1}=(3+j4)\Omega$ ，对称线电压  $U_{AB}=380V$ 。求负载端的线电压和线电流。

解 该电路可以变换为对称的 Y-Y 电路, 如图 12-5 所示。图中  $Z'$  为(三角形变换为星形)

$$
Z ^ {\prime} = \frac {Z}{3} = \frac {1 9 . 2 + \mathrm{j} 1 4 . 4}{3} \Omega = (6. 4 + \mathrm{j} 4. 8) \Omega
$$

令  $\dot{U}_{A}=220\angle0^{\circ}V$ 。根据一相计算电路有

$$
\dot {I} _ {\mathrm{A}} = \frac {\dot {U} _ {\mathrm{A}}}{Z _ {1} + Z ^ {\prime}} = 1 7. 1 / - 4 3. 2 ^ {\circ} \mathrm{A}
$$

而

$$
\dot {I} _ {\mathrm{B}} = a ^ {2} \dot {I} _ {\mathrm{A}} = 1 7. 1 / - 1 6 3. 2 ^ {\circ} \mathrm{A}
$$

$$
\dot {I} _ {\mathrm{C}} = a \dot {I} _ {\mathrm{A}} = 1 7. 1 / 7 6. 8 ^ {\circ} \mathrm{A}
$$

![](../../raw/pages_0289-0320/images/page_309_image_19.jpg)

<details>
<summary>text_image</summary>

ÜA +
- A Z1 A' Z' İA
ÜB +
- B Z1 B' Z' İB
ÜC +
- C Z1 C' Z' İC
N N'
</details>

图12-5 例12-2图

此电流即为负载端的线电流。再求出负载端的相电压,利用线电压与相电压的关系就可得负载端的线电压。 $\dot{U}_{A'N'}$ 为

$$
\dot {U} _ {\mathrm{A} ^ {\prime} \mathrm{N} ^ {\prime}} = \dot {I} _ {\mathrm{A}} Z ^ {\prime} = 1 3 6. 8 / - 6. 3 ^ {\circ} \mathrm{V}
$$

根据式(12-1)，有

$$
\dot {U} _ {\mathrm{A'B'}} = \sqrt {3} \dot {U} _ {\mathrm{A'N'}} / 3 0 ^ {\circ} = 2 3 6. 9 / 2 3. 7 ^ {\circ} \mathrm{V}
$$

根据对称性可写出

$$
\dot {U} _ {\mathrm{B} ^ {\prime} \mathrm{C} ^ {\prime}} = a ^ {2} \dot {U} _ {\mathrm{A} ^ {\prime} \mathrm{B} ^ {\prime}} = 2 3 6. 9 / - 9 6. 3 ^ {\circ} \mathrm{V}
$$

$$
\dot {U} _ {\mathrm{C'A'}} = a \dot {U} _ {\mathrm {A ^ {\prime} B ^ {\prime}}} = 2 3 6. 9 / 1 4 3. 7 ^ {\circ} \mathrm{V}
$$

根据负载端的线电压[如图 12-2(b) 所示]可以求得负载中的相电流,有

$$
\dot {I} _ {\mathrm{A'B'}} = \frac {\dot {U} _ {\mathrm{A'B'}}}{Z} = 9. 9 / - 1 3. 2 ^ {\circ} \mathrm{A}
$$

---

§ 12-4 不对称三相电路的概念

287

$$
\dot {I} _ {\mathrm{B} ^ {\prime} \mathrm{C} ^ {\prime}} = \alpha^ {2} \dot {I} _ {\mathrm{A} ^ {\prime} \mathrm{B} ^ {\prime}} = 9. 9 / - 1 3 3. 2 ^ {\circ} \mathrm{A}
$$

$$
\dot {I} _ {\mathrm{C'A'}} = a \dot {I} _ {\mathrm {A^{\prime} B^{\prime}}} = 9. 9 / 1 0 6. 8 ^ {\circ} \mathrm{A}
$$

也可以利用式(12-2)计算负载的相电流。

## §12-4 不对称三相电路的概念

在三相电路中, 只要有一部分不对称就称为不对称三相电路, 例如, 对称三相电路的某一条端线断开, 或某一相负载发生短路或开路, 它就失去了对称性, 成为不对称的三相电路。对于不对称三相电路的分析, 一般情况下, 不能引用上一节介绍的一相计算方法, 而要用其他方法求解。本节只简要地介绍由于负载不对称而引起的一些特点。

图 12-6(a) 的 Y-Y 联结电路中三相电源是对称的,但负载不对称。先讨论开关 S 打开(即不接中性线)时的情况。用节点电压法,可以求得节点电压  $\dot{U}_{N'N}$  为

$$
\dot {U} _ {\mathrm{N'N}} = \frac {\dot {U} _ {\mathrm{A}} Y _ {\mathrm{A}} + \dot {U} _ {\mathrm{B}} Y _ {\mathrm{B}} + \dot {U} _ {\mathrm{C}} Y _ {\mathrm{C}}}{Y _ {\mathrm{A}} + Y _ {\mathrm{B}} + Y _ {\mathrm{C}}}
$$

由于负载不对称，一般情况下 $\dot{U}_{\mathrm{N}^{\prime}\mathrm{N}}\neq 0$ ，即 $\mathbf{N}^{\prime}$ 点和N点电位不同了。从图12-6(b)的相量关系可以清楚看出， $\mathbf{N}^{\prime}$ 点和N点不重合，这一现象称为中性点位移。在电源对称的情况下，可以根据中性点位移的情况判断负载端不对称的程度。当中性点位移较大时，会造成负载端的电压严重的不对称，从而可能使负载的工作不正常。另一方面，如果负载变动时，由于各相的工作相互关联，因此彼此都互有影响。

![](../../raw/pages_0289-0320/images/page_310_image_10.jpg)

<details>
<summary>text_image</summary>

ÜA +
-       A
ÜB +
-       B
ÜC +
-       C
iA     ZA
iB     ZB
iC     ZC
N'      N'
      S
      iN
</details>

(a)

![](../../raw/pages_0289-0320/images/page_310_image_12.jpg)

<details>
<summary>text_image</summary>

ÛCN'
ÛC
ÛNN
N'
N
ÛAN'
ÛA
ÛB
ÛBN'
</details>

(b)

图 12-6 不对称三相电路

合上开关 S(接上中性线)，如果  $Z_{N} \approx 0$ ，则可强使  $\dot{U}_{N'N} = 0$ 。尽管电路是不对称，但在这个条件下，可强使各相保持独立性，各相的工作互不影响，因而各相可以分别独立计算。能确保各相负载在相电压下安全工作，这就克服了无中性线时引起的缺点。因此，在负载不对称的情况下中性线的存在是非常重要的，它能起到保证安全供电的作用。

由于线(相)电流的不对称,中性线的电流一般不为零,即

![](../../raw/pages_0289-0320/images/page_310_image_18.jpg)

不对称三相电路的概念

---

![](../../raw/pages_0289-0320/images/page_311_image_0.jpg)

<details>
<summary>natural_image</summary>

Abstract line drawing of a windmill with blades and a flag (no text or symbols)
</details>

288

第十二章 三相电路

$$
\dot {I} _ {\mathrm{N}} = \dot {I} _ {\mathrm{A}} + \dot {I} _ {\mathrm{B}} + \dot {I} _ {\mathrm{C}} \neq 0
$$

例 12-3 图 12-6(a) 所示电路中, 若  $Z_{A} = -j \frac{1}{\omega C}$  (电容), 而  $Z_{B} = Z_{C} = R$ , 并且  $R = \frac{1}{\omega C}$ , 则电路是一种测定相序的仪器, 称为相序指示器 (图中电阻 R 用两个相同的白炽灯代替)。试说明在相电压对称的情况下, 当 S 打开时, 如何根据两个白炽灯的亮度确定电源的相序。

解 图 12-6(a) 所示电路中性点电压  $\dot{U}_{N'N}$  为

$$
\dot {U} _ {\mathrm{N} ^ {\prime} \mathrm{N}} = \frac {\mathrm{j} \omega C \dot {U} _ {\mathrm{A}} + G \left(\dot {U} _ {\mathrm{B}} + \dot {U} _ {\mathrm{C}}\right)}{\mathrm{j} \omega C + 2 G}
$$

令  $\dot{U}_{A}=U/0^{\circ}V$ ，代入给定的参数关系后，有

$$
\dot {U} _ {\mathrm{N} ^ {\prime} \mathrm{N}} = (- 0. 2 + \mathrm{j} 0. 6) U = 0. 6 3 U / 1 0 8. 4 ^ {\circ}
$$

B 相白炽灯承受的电压  $\dot{U}_{BN}$ ，为

$$
\dot {U} _ {\mathrm{BN} ^ {\prime}} = \dot {U} _ {\mathrm{BN}} - \dot {U} _ {\mathrm{N} ^ {\prime} \mathrm{N}} = 1. 5 U / - 1 0 1. 5 ^ {\circ}
$$

所以

$$
U _ {\mathrm{BN} ^ {\prime}} = 1. 5 U
$$

而

$$
\dot {U} _ {\mathrm{CN} ^ {\prime}} = \dot {U} _ {\mathrm{CN}} - \dot {U} _ {\mathrm {N^{\prime} N}} = 0. 4 U / 1 3 3. 4 ^ {\circ}
$$

即

$$
U _ {\mathrm{CN} ^ {\prime}} = 0. 4 U
$$

根据上述结果可以判断: $U_{CN}$ 最小,则白炽灯较暗的一相为 C 相。

## §12-5 三相电路的功率

在三相电路中,三相负载吸收的复功率等于各相复功率之和,即

$$
\overline {{S}} = \overline {{S}} _ {\mathrm{A}} + \overline {{S}} _ {\mathrm{B}} + \overline {{S}} _ {\mathrm{C}}
$$

在对称的三相电路中有  $\overline{S}_{A}=\overline{S}_{B}=\overline{S}_{C}$ ，因而  $\overline{S}=3\overline{S}_{A}$ 。

三相电路的瞬时功率为各相负载瞬时功率之和。如对图 12-2(a) 所示的对称三相电路, 有

$$
\begin{array}{l} p _ {\mathrm{A}} = u _ {\mathrm{AN}} i _ {\mathrm{A}} = \sqrt {2} U _ {\mathrm{AN}} \cos (\omega t) \times \sqrt {2} I _ {\mathrm{A}} \cos (\omega t - \varphi) \\ = U _ {\mathrm{AN}} I _ {\mathrm{A}} \left[ \cos \varphi + \cos (2 \omega t - \varphi) \right] \\ p _ {\mathrm{B}} = u _ {\mathrm{BN}} i _ {\mathrm{B}} = \sqrt {2} U _ {\mathrm{AN}} \cos (\omega t - 1 2 0 ^ {\circ}) \times \sqrt {2} I _ {\mathrm{A}} \cos (\omega t - \varphi - 1 2 0 ^ {\circ}) \\ = U _ {\mathrm{AN}} I _ {\mathrm{A}} \left[ \cos \varphi + \cos (2 \omega t - \varphi - 2 4 0 ^ {\circ}) \right] \\ p _ {\mathrm{C}} = u _ {\mathrm{CN}} i _ {\mathrm{C}} = \sqrt {2} U _ {\mathrm{AN}} \cos (\omega t + 1 2 0 ^ {\circ}) \times \sqrt {2} I _ {\mathrm{A}} \cos (\omega t - \varphi + 1 2 0 ^ {\circ}) \\ = U _ {\mathrm{AN}} I _ {\mathrm{A}} \left[ \cos \varphi + \cos (2 \omega t - \varphi + 2 4 0 ^ {\circ}) \right] \\ \end{array}
$$

$$
\begin{array}{l} p _ {\mathrm{B}} = u _ {\mathrm{BN}} i _ {\mathrm{B}} = \sqrt {2} U _ {\mathrm{AN}} \cos (\omega t - 1 2 0 ^ {\circ}) \times \sqrt {2} I _ {\mathrm{A}} \cos (\omega t - \varphi - 1 2 0 ^ {\circ}) \\ = U _ {\mathrm{AN}} I _ {\mathrm{A}} \left[ \cos \varphi + \cos (2 \omega t - \varphi - 2 4 0 ^ {\circ}) \right] \\ \end{array}
$$

$$
\begin{array}{l} p _ {\mathrm{C}} = u _ {\mathrm{CN}} i _ {\mathrm{C}} = \sqrt {2} U _ {\mathrm{AN}} \cos (\omega t + 1 2 0 ^ {\circ}) \times \sqrt {2} I _ {\mathrm{A}} \cos (\omega t - \varphi + 1 2 0 ^ {\circ}) \\ = U _ {\mathrm{AN}} I _ {\mathrm{A}} \left[ \cos \varphi + \cos (2 \omega t - \varphi + 2 4 0 ^ {\circ}) \right] \\ \end{array}
$$

![](../../raw/pages_0289-0320/images/page_311_image_26.jpg)

三相电路的
功率

---

§ 12-5 三相电路的功率

289

它们的和为

$$
p = p _ {\mathrm{A}} + p _ {\mathrm{B}} + p _ {\mathrm{C}} = 3 U _ {\mathrm{AN}} I _ {\mathrm{A}} \cos \varphi = 3 P _ {\mathrm{A}}
$$

此式表明,对称三相电路的瞬时功率是一个常量,其值等于平均功率。这是对称三相电路的一个优越的性能。习惯上把这一性能称为瞬时功率平衡。

在三相三线制电路中,不论对称与否,都可以使用两个功率表的方法测量三相功率(称为二瓦计法)。两个功率表的一种连接方式如图12-7所示。使线电流从\*端分别

流入两个功率表的电流线圈(图示为  $\dot{I}_{A}, \dot{I}_{B}$ )，它们的电压线圈的非 \* 端共同接到非电流线圈所在的第 3 条端线上(图示为 C 端线)。可以看出, 这种测量方法中功率表的接线只触及端线, 而与负载和电源的连接方式无关。

可以证明图中两个功率表读数的代数和为三相三线制中右侧电路吸收的平均功率。

![](../../raw/pages_0289-0320/images/page_312_image_8.jpg)

<details>
<summary>text_image</summary>

A○—*—W₁
B○—*—W₂
C○—*
iₐ
iᵦ
i꜀
三相负载
</details>

图 12-7 二瓦计法

设两个功率表的读数分别用  $P_{1}$  和  $P_{2}$  表示, 根据功率表的工作原理, 有

$$
P _ {1} = \mathrm{Re} \left[ \dot {U} _ {\mathrm{AC}} \dot {I} _ {\mathrm{A}} ^ {*} \right], \quad P _ {2} = \mathrm{Re} \left[ \dot {U} _ {\mathrm{BC}} \dot {I} _ {\mathrm{B}} ^ {*} \right]
$$

所以

$$
P _ {1} + P _ {2} = \mathrm{Re} \left[ \dot {U} _ {\mathrm{AC}} \dot {I} _ {\mathrm{A}} ^ {*} + \dot {U} _ {\mathrm{BC}} \dot {I} _ {\mathrm{B}} ^ {*} \right]
$$

因为 $\dot{U}_{\mathrm{AC}} = \dot{U}_{\mathrm{A}} - \dot{U}_{\mathrm{C}},\dot{U}_{\mathrm{BC}} = \dot{U}_{\mathrm{B}} - \dot{U}_{\mathrm{C}},\dot{I}_{\mathrm{A}}^{*} + \dot{I}_{\mathrm{B}}^{*} = -\dot{I}_{\mathrm{C}}^{*}$ ，代入上式有

$$
\begin{array}{l} P _ {1} + P _ {2} = \mathrm{Re} \left[ \dot {U} _ {\mathrm{A}} \dot {I} _ {\mathrm{A}} ^ {*} + \dot {U} _ {\mathrm{B}} \dot {I} _ {\mathrm{B}} ^ {*} + \dot {U} _ {\mathrm{C}} \dot {I} _ {\mathrm{C}} ^ {*} \right] = \mathrm{Re} \left[ \overline {{S}} _ {\mathrm{A}} + \overline {{S}} _ {\mathrm{B}} + \overline {{S}} _ {\mathrm{C}} \right] \\ = \operatorname{Re} [ \bar {S} ] \\ \end{array}
$$

而 $\operatorname{Re}[\bar{S}]$ 则表示右侧三相负载的有功功率。在对称三相制中令 $\dot{U}_{\mathrm{A}} = U_{\mathrm{A}} / 0^{\circ}$, $\dot{I}_{\mathrm{A}} = I_{\mathrm{A}} / -\varphi$, 则有

$$
\left. \begin{array}{l} P _ {1} = \operatorname{Re} \left[ \dot {U} _ {\mathrm{AC}} \dot {I} _ {\mathrm{A}} ^ {*} \right] = U _ {\mathrm{AC}} I _ {\mathrm{A}} \cos (\varphi - 3 0 ^ {\circ}) \\ P _ {2} = \operatorname{Re} \left[ \dot {U} _ {\mathrm{BC}} \dot {I} _ {\mathrm{B}} ^ {*} \right] = U _ {\mathrm{BC}} I _ {\mathrm{B}} \cos (\varphi + 3 0 ^ {\circ}) \end{array} \right\} \tag {12-3}
$$

式中  $\varphi$  为负载的阻抗角。应当注意，在一定的条件下（例如  $\left|\varphi\right|>60^{\circ}$ ），两个功率表之一的读数可能为负，求代数和时该读数应取负值。一般来讲，单独一个功率表的读数是没有意义的。

不对称的三相四线制不能用二瓦计法测量三相功率, 这是因为在一般情况下,  $\dot{I}_{A} + \dot{I}_{B} + \dot{I}_{C} \neq 0$ 。

例 12-4 若图 12-7 所示电路为对称三相电路, 已知对称三相负载吸收的功率为 2.5 kW, 功率因数  $\lambda = \cos \varphi = 0.866$  (感性), 线电压为 380 V。求图中两个功率表的读数。

解 对称三相负载吸收的功率是一相负载所吸收功率的3倍，令 $\dot{U}_{\mathrm{A}} = U_{\mathrm{A}} / 0^{\circ}$ ， $\dot{I}_{\mathrm{A}} = I_{\mathrm{A}} / -\varphi$ ，则

$$
P = 3 \mathrm{Re} \left[ \dot {U} _ {\mathrm{A}} \dot {I} _ {\mathrm{A}} ^ {*} \right] = \sqrt {3} U _ {\mathrm{AB}} I _ {\mathrm{A}} \cos \varphi
$$

求得电流 $I_{A}$ 为

---

290

第十二章 三相电路

$$
I _ {\mathrm{A}} = \frac {P}{\sqrt {3} U _ {\mathrm{AB}} \cos \varphi} = 4. 3 8 6 \mathrm{A}
$$

又

$$
\varphi = \arccos \lambda = 3 0 ^ {\circ} (\text {感性})
$$

则图中功率表相关的电压、电流相量为

$$
\dot {I} _ {\mathrm{A}} = 4. 3 8 6 / - 3 0 ^ {\circ} \mathrm{A}, \dot {U} _ {\mathrm{AC}} = 3 8 0 / - 3 0 ^ {\circ} \mathrm{V}
$$

$$
\dot {I} _ {\mathrm{B}} = 4. 3 8 6 / - 1 5 0 ^ {\circ} \mathrm{A}, \dot {U} _ {\mathrm{BC}} = 3 8 0 / - 9 0 ^ {\circ} \mathrm{V}
$$

则功率表的读数如下:

$$
P _ {1} = \mathrm{Re} \left[ \dot {U} _ {\mathrm{AC}} \dot {I} _ {\mathrm{A}} ^ {*} \right] = \mathrm{Re} \left[ 3 8 0 \times 4. 3 8 6 / 0 ^ {\circ} \right] \mathrm{W} = 1 6 6 6. 6 8 \mathrm{W}
$$

$$
P _ {2} = \mathrm{Re} \left[ \dot {U} _ {\mathrm{BC}} \dot {I} _ {\mathrm{B}} ^ {*} \right] = \mathrm{Re} \left[ 3 8 0 \times 4. 3 8 6 / 6 0 ^ {\circ} \right] \mathrm{W} = 8 3 3. 3 4 \mathrm{W}
$$

其实,只要求得两个功率表之一的读数,另一功率表的读数等于负载的功率减去该表的读数,例如,求得 $P_{1}$ 后, $P_{2}=P-P_{1}$ 。

我们已经学习了三相电路、变压器等内容,学习电路理论要与工程实际相结合,才能更牢固地掌握电路理论。学习者现在能够在学习电路理论的基础上,设计一个家庭的供电系统、一个居民小区的供电系统,或是设计一个工厂的供电系统。在设计过程中,对变压器容量选择、电表量程、导线和开关选择、电压损失、线路损耗、无功补偿进行深入讨论和思考,一方面加深对电路理论的理解和掌握,一方面增强实践动手能力。

在设计中,可能会碰到书本中没有提及的知识,需要自主学习,敢于创新,在解决问题的过程中锻炼自己发现问题、解决问题和综合应用知识的能力。如果是一个团队完成设计任务,则要做好顶层设计、合理分工,处理好个人与集体、局部与全局的关系,发挥集体优势,集思广益,相互协调,设计出考虑全面、符合实际的供电系统。

![](../../raw/pages_0289-0320/images/page_313_image_15.jpg)

## 思考题

12-1 为什么现有电力系统采用三相制？

12-2 星形联结的三相电源和负载,如果中性线电流为零,能否表明三相电压源的相电压是对称的?

12-3 在实际的三相供电系统中,除了电动机外,很多负载是单相的,如何布置负载,可使三相负载尽可能对称?

12-4 当三相系统的负载不对称时,为什么还要保证三相电压尽可能对称?

12-5 对称三相电路的瞬时功率是常量,为什么还存在无功功率?

12-6 对于不对称的三相四线制系统,如何测量功率?

12-7 一般家庭或办公室都是使用单相交流电,但配电网却是三相交流电。试问,当一个住宅小区或一栋建筑的电源是三相交流电,如何使得进入各用户的是单相交

---

习题

291

流电,而电源端看起来是一个对称的三相负载?

![](../../raw/pages_0289-0320/images/page_314_image_4.jpg)

## 习题

12-1 已知对称三相电路的星形负载阻抗  $Z=(165+j84)\Omega$ ，端线阻抗  $Z_{1}=(2+j1)\Omega$ ，中性线阻抗  $Z_{N}=(1+j1)\Omega$ ，线电压  $U_{1}=380V$ 。求负载端的电流和线电压，并作电路的相量图。
12-2 已知对称三相电路的线电压 $U_{1} = 380 \mathrm{~V}$ （电源端），三角形负载阻抗 $Z = (4.5 + \mathrm{j}14)\Omega$，端线阻抗 $Z_{1} = (1.5 + \mathrm{j}2)\Omega$。求线电流和负载的相电流，并作相量图。
12-3 将题 12-1 中负载 Z 改为三角形联结(无中性线)。比较两种连接方式中负载所吸收的复功率。
12-4 题 12-4 图所示对称三相耦合电路接于对称三相电源, 电源频率为 50 Hz, 线电压  $U_{1}=380\ V, R=30\ \Omega, L=0.29\ H, M=0.12\ H$ 。求相电流和负载吸收的总功率。
12-5 题 12-5 图所示对称 Y-Y 三相电路中, 电压表的读数为 1143.16 V,  $Z = (15 + j15\sqrt{3})\Omega$ ,  $Z_{1} = (1 + j2)\Omega$ 。

(1) 求图中电流表的读数及线电压  $U_{AB}$ 。
(2) 求三相负载吸收的功率。
(3) 如果 A 相的负载阻抗等于零(其他不变), 再求(1)和(2)。
(4) 如果 A 相负载开路, 再求 (1) 和 (2)。
(5) 如果加接零阻抗中性线  $Z_{N}=0$ ，则 (3) 和 (4) 将发生怎样的变化？

![](../../raw/pages_0289-0320/images/page_314_image_18.jpg)

<details>
<summary>chemical</summary>

Electrical circuit diagram with resistors, inductors, and mutual inductance symbols
</details>

题12-4图

![](../../raw/pages_0289-0320/images/page_314_image_20.jpg)

<details>
<summary>text_image</summary>

A
Z₁
A'
Z
B
Z₁
V
B'
Z
N'
C
Z₁
C'
Z
</details>

题 12-5 图

12-6 题 12-6 图所示对称三相电路中, $U_{A'B'} = 380 \mathrm{~V}$, 三相电动机吸收的功率为 $1.4 \mathrm{kW}$, 其功率因数 $\lambda = 0.866$ (滞后), $Z_1 = -\mathrm{j}55\Omega$。求 $U_{AB}$ 和电源端的功率因数 $\lambda'$。
12-7 题 12-7 图所示对称 Y- $\Delta$  三相电路中, $U_{AB}=380\ V$ , 图中功率表的读数为 $W_{1}:782,W_{2}:1976.44$ 。求:

---

292

第十二章 三相电路

(1) 负载吸收的复功率  $\bar{S}$  和阻抗 Z。
(2) 开关 S 打开后, 功率表的读数。

![](../../raw/pages_0289-0320/images/page_315_image_6.jpg)

<details>
<summary>text_image</summary>

A○─Z₁─A′─
B○─Z₁─B′─
C○─Z₁─C′─
三相
电动机
</details>

题12-6图

![](../../raw/pages_0289-0320/images/page_315_image_8.jpg)

<details>
<summary>text_image</summary>

A○
B○
C○
W₁
W₂
*
*
*
Z
Z
S
Z
</details>

题12-7图

12-8 题 12-8 图所示电路中, 对称三相电源端的线电压 $U_{1} = 380 \mathrm{~V}, Z = (50 + \mathrm{j}50) \Omega$, $Z_{1} = (100 + \mathrm{j}100) \Omega, Z_{\mathrm{A}}$ 由 $R, L, C$ 串联组成, $R = 50 \Omega, X_{L} = 314 \Omega, X_{C} = -264 \Omega$。

(1) 求开关 S 打开时的线电流。
(2) 若用二瓦计法测量电源端三相功率, 试画出接线图, 并求两个功率表的读数 (S 闭合时)。

12-9 题 12-9 图所示电路中,电源为对称三相电源。

(1) L、C 满足什么条件时, 线电流对称?
(2) 若  $R = \infty$  (开路), 再求线电流。

![](../../raw/pages_0289-0320/images/page_315_image_18.jpg)

<details>
<summary>text_image</summary>

A○─ Zambia
      S
      Z₁
B○─ Z     N′
C○─ Z
</details>

题12-8图

![](../../raw/pages_0289-0320/images/page_315_image_20.jpg)

<details>
<summary>text_image</summary>

A
B
C
R
L
C
</details>

题12-9图

12-10 已知对称三相电路中的线电压为 $380\mathrm{V}, f = 50\mathrm{Hz}$，负载吸收的功率为 $2.4\mathrm{kW}$（参阅图12-7），功率因数为0.4（感性）。

(1) 求两个功率表的读数(用二瓦计法测量功率时)。
(2) 怎样才能使负载端的功率因数提高到 0.8？并再求出两个功率表的读数。

12-11 题 12-11 图所示三相(四线)制电路中, $Z_{1}=-j10\ \Omega,Z_{2}=(5+j12)\ \Omega$ ,对称三相电源的线电压为380 V,图中电阻R吸收的功率为24 200 W(S闭合时)。

（1）求开关 S 闭合时图中各表的读数。根据功率表的读数能否求得整个负载吸收的总功率？
(2) 开关 S 打开时图中各表的读数有无变化, 功率表的读数有无意义?

---

习题

293

![](../../raw/pages_0289-0320/images/page_316_image_2.jpg)

<details>
<summary>text_image</summary>

A○—W
*
B○—A₁
C○—Z₂ Z₂ Z₂
N○—S
A₂
Z₁
Z₁
Z₁
R
</details>

题12-11图

12-12 题 12-12 图所示为对称三相电路, 线电压为 380 V, R=200 Ω, 负载吸收的无功功率为  $1520\sqrt{3}$  var。试求:

(1) 各线电流。
(2) 电源发出的复功率。

12-13 题 12-13 图所示为对称三相电路, 线电压为 $380 \mathrm{~V}$, 相电流 $I_{\mathrm{A'B'}} = 2 \mathrm{~A}$ 。求图中功率表的读数。

![](../../raw/pages_0289-0320/images/page_316_image_9.jpg)

<details>
<summary>text_image</summary>

iA
A○
iB
B○
iC
C○
1
jωC
1
jωC
R
R
R
1
jωC
</details>

题12-12图

![](../../raw/pages_0289-0320/images/page_316_image_11.jpg)

<details>
<summary>text_image</summary>

A○—W₁—○—A′
B○—W₂—○—B′—jωL
C○—○—C′—jωL
iA′B′
jωL
</details>

题12-13图

12-14 题 12-14 图所示电路中的 $\dot{U}_{\mathrm{s}}$ 是频率 $f = 50 \mathrm{~Hz}$ 的正弦电压源。若要使 $\dot{U}_{\mathrm{so}}$、$\dot{U}_{\mathrm{bo}}$、$\dot{U}_{\mathrm{co}}$ 构成对称三相电压，$R, L, C$ 之间应当满足什么关系？设 $R = 20 \Omega$，求 $L$ 和 $C$ 的值。

![](../../raw/pages_0289-0320/images/page_316_image_14.jpg)

<details>
<summary>text_image</summary>

+
a
jωL
b
1
jωC
c
R
R
o
R
-
</details>

题12-14图

---

294

第十二章 三相电路

\*12-15 试设计一个居民小区的配电站。假设小区住宅楼楼层分别为18层、24层、32层等，各有若干栋。每栋楼有2\~3个单元，住宅户型有 $105\mathrm{m}^2$ 、 $120\mathrm{m}^2$ 、 $140\mathrm{m}^2$ 三种。请读者自己给出小区共有多少栋楼，每栋楼各类户型有多少套。参考第一章习题1-19的家用电器用电量表，综合如下因素，设计出该小区共需多大容量的变压器、各住户导线及变压器出线导线、开关容量、电容器组容量等。

(1) 各栋楼的位置, 配电站的位置。
(2) 除了居民家中用电负荷外, 还要考虑公用负荷。例如每个单元需 1\~2 部电梯, 楼道和小区照明设施等。
(3) 不能简单将家中用电设备容量直接相加作为用户的总负荷, 要考虑同时率的问题。
（4）小区配电室是三相电源，但用户家中负荷基本上是单相负荷。应考虑三相电源如何分配至各楼层的用户，以尽可能满足三相负载对称的要求。

(5) 功率因数提高, 确定电容器组的容量。

(6) 可能的用电设施的故障。

(7) 根据自定的设计目标, 确定变压器容量的计算值, 再通过查阅设计手册, 确定实际变压器的型号和台数。

\*12-16 选定一个大的工业用户, 工业用户的特点是大多数负荷为三相对称负载, 但车间和办公区的照明等少量负荷是单相的, 根据所选企业的生产情况, 包括生产车间用电设备、公用电梯、照明、中央空调等用电设备, 设计所选企业配电所的变压器和电容器组的容量和台数。

![](../../raw/pages_0289-0320/images/page_317_image_13.jpg)

第十二章部分习题答案
