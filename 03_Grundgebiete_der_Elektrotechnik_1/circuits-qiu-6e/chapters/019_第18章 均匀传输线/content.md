# 第18章 均匀传输线

原始 PDF 第 474–502 页。

The image contains no text or mathematical content to process. It is a graphical representation of a triangular shape composed of small, irregular black dots. Therefore, the correct OCR output is an empty string.

# 第十八章 均匀传输线

![](../../raw/pages_0449-0480/images/page_473_image_2.jpg)

## 导读

电磁现象都是在空间发生的。集总参数电路不能考虑电磁现象的空间分布性，因为实际电磁现象的发生是电磁作用（以场的形式）在空间传播的结果。其传播速度是有限的，远离电源处比起较近处电磁作用的出现有推迟现象。对正弦变化来说，远处的正弦变化在相位上要比较落后，这就意味着难以用一个物理量（例如电流）来概括不同空间所出现的电磁现象（例如在空间的能量损耗等）。以传递能量、信号为目的的传输线，在传输方向上线路可以甚长，沿线路电磁作用的推迟作用必须考虑；但是在垂直于传输方向的空间上，尺寸不会很大，可以不计该方向上的推迟作用。这就使得我们仍可使用电路的物理量和电路元件来描述线路的物理过程，但此时的电路物理量应沿线路长度而变化，并且元件也必须是沿线路作分布的分布参数元件。只有如此才能正确地描绘这种特殊情况的电路。

均匀传输线的电路变量既是时间又是空间的函数,故电路方程将是偏微分方程。讨论其正弦稳态解时,解答是沿线变化的复数相量,方程也成为常微分方程。在这些解中出现的波动特性应在学习过程中倍加注意和领会。

## §18-1 分布参数电路

在以前各章中，讨论了由集总参数元件组成的电路模型。每一种集总参数元件被假设集中由一种电磁现象所表征。例如，电阻元件集中表征了某一个实际部件或某一段实际电路中的能量消耗，电感元件集中地反映了磁场的物理现象，电容元件则集中反映了电场的物理现象（如充、放电，位移电流等）。但是，在某些实际电路中，发生的电磁现象往往是带有分布性的，必须在一定条件下才能建立其集总参数模型。图18-1(a)示出一个实际电路，这是一个电源通过导线向负载传递信号或能量的传输电路。导线中的电流是由导线中电场产生的，电流在导线外产生磁场（用磁感应强度 $B$ 表示）；并且由于两导线之间的电压，导线间也有电场（用电场强度 $E$ 表示），此电场在导

---

§ 18-1 分布参数电路

451

线间产生电容电流和漏电流。这些电场-磁场都是沿线分布，即分散在空间的。就导线上的能量损耗与磁场效应来说，因导线间的电流导致导线中的电流处处不同，故不能以一项 $i^2 R$ 或 $L\frac{\mathrm{d}i}{\mathrm{d}t}$ （即以一个集总参数 $R, L$）来概括导线上的物理过程；而导线上的电阻、电感压降也导致线间的电压处处不相同，故不能以一项 $u^2 G$ 或 $C\frac{\mathrm{d}u}{\mathrm{d}t}$（即以一个集总参数 $G, C$）来概括导线间的物理过程。接近这种物理现象的电路模型，应是由无限多个导线上的电阻、电感以及无限多个导线间的电导、电容所组成的分布参数模型，如图18-1(b)所示。

![](../../raw/pages_0449-0480/images/page_474_image_4.jpg)

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

![](../../raw/pages_0449-0480/images/page_474_image_6.jpg)

<details>
<summary>natural_image</summary>

Pure electrical circuit diagram with three parallel branches and resistors, no text or symbols present
</details>

(b)

图 18-1 实际电路参数的分布

应当说,任何实际电路都有是否必须采用分布参数模型的问题。以传输线为例,只要沿线流动的电流随空间距离变化很小,即导线间的空间电容电流及电导电流不大时,就可以用单个电阻来描述损耗、单个电感来描述磁场作用。引申至一个实际电阻器的情况,在直流工作条件下其模型仅为一个电阻元件,在低频交流工作条件下其模型则是电阻元件和电感元件的串联组合;另一方面,当可不计导线上电阻、电感电压降时,认为导线间所有漏电流、所有电容电流处于同一个电压时,就可以用单个电导来描述导线间的漏电作用、单个电容来描述导线间的电容作用。实际电容器部件则是另一例,在直流及低频交流下可不计在极板上电流的电阻性压降和电感性压降,其模型就是一个电容元件和电导元件的并联组合。这些模型都是集总参数模型,构成的电路模型就是集总参数电路。

---

452

第十八章 均匀传输线

直流稳态下,有时也要用分布参数模型。例如在直流输电线中,如果要研究沿线的电压、电流变化,这时虽然电感、电容不产生影响,还应从导线上电阻及导线间电导所构成的分布参数模型来研究。

在交流稳态下,由于电感电压以及电容电流都与工作频率成正比,因此在高频下分布参数问题就更为突出。这可以从电磁波的传播来解释。真空中电磁波是以有限速度(光速)的波动方式运动的,在运动过程中在传播方向会出现波峰(极值)、波节(零值)的移动。相邻波峰(或波节)的距离称为工作波长 $\lambda$ 。众所周知, $\lambda=\frac{v}{f}=vT$ ,其中v为波速,f为工作频率,T为周期。在电压(或电流)波峰所到之处,电压(电流)达到极值,在电压(电流)波节所到之处,电压(电流)为零。因此沿传播方向,即使在同一时刻,沿线电压(或电流)是以波长 $\lambda$ 为重复周期 $^{①}$ 的电压(或电流)波动形式。图18-2(a)示出,当线长 $l<<\lambda$ 时,全线的电压(电流)处于同一个变化状态,就可使用集总参数模型 $^{②}$ ;图18-2(b)中示出 $l\ll\lambda$ 时,即线长可与 $\lambda$ 做比较时,此时沿线电压(或电流)有明显的波动,各处数值不一,就不可使用集总参数模型,而必须采用分布参数模型。

![](../../raw/pages_0449-0480/images/page_475_image_5.jpg)

<details>
<summary>text_image</summary>

+
-
λ
l
</details>

(a) $l <   <   \lambda$

![](../../raw/pages_0449-0480/images/page_475_image_7.jpg)

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

令  $\Delta t=\frac{l}{v}$ ， $\Delta t$  为电磁作用传遍线长所需的时间。条件  $l\ll\lambda$  两侧均除以 v 后，就可写为  $\Delta t\ll T$ 。周期 T 是度量正弦时间函数随时间变化快慢的值。因此，使用集总模型的条件也可理解为:在电磁作用传遍全线的时间内，电源值几乎未发生变化。此时自然

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 由于沿线传播有衰减,故非严格意义的周期变化。</span></small>

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">② 如舍弃线间电流，则视为集总电阻、电感串联；如舍弃线上压降，则视为集总电导、电容并联。</span></small>

---

§ 18-2 均匀传输线及其方程

453

不会沿线出现具有波峰、波节形式的波动。也相当于波是以无限大速度传播的，沿线不存在电磁作用的推迟作用。①

应当指出,如果仅关心长线电源端以及负载端的电压、电流,还是可以将传输线部分看为一个二端口网络,或相应地用等值T形、 $\pi$ 形电路来替代,但是这些二端口的参数、等值电路应由分布参数模型来求出。此外,虽然等值T形、 $\pi$ 形电路是集总参数电路,但其中的Z、Y都是在一定的频率下求得的,并非传输线线路参数的直接归结 $^{②}$ 。不能误解为此时分布参数模型可以由集总参数模型来代替。

## §18-2 均匀传输线及其方程

最典型的传输线是由在均匀媒质中放置的两根平行直线导体构成的,其通常的形式如图18-3所示。其中图(a)为两线架空线,图(b)为同轴电缆,图(c)为二芯电缆,图(d)是一线一地构成的传输线,图(e)(f)是在高频下工作的天线。[图(e)是最普通的半波电视天线,左右两段导线的总长为 $\lambda/2$ 。图(f)是中波使用的垂直天线,亦由一线一地构成。]

![](../../raw/pages_0449-0480/images/page_476_image_6.jpg)

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

在上述传输线中,电流在导线的电阻中引起沿线的电压降,并在导线的周围产生磁场,即沿线有电感的存在,变动的电流沿线产生电感电压降。所以,导线间的电压是连续变化的。另一方面,由于两导体构成电容,因此在导线间存在电容电流;导体间还有漏电导,故还有电导电流。这样,沿线不同的地方,导线中的电流也是不同的。为了计

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 读者将在电磁场的学习中加深理解此点。</span></small>

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">② T形、π形等效电路中的各个Z、Y如果以集总元件R、L、G、C来实现时，这些参数将是频率f的函数。此情况类似于:交流电路中，R、L串联组合用 $R'$ 、 $L'$ 并联组合来等效替代时， $R'$ 、 $L'$ 还将与频率有关。并不说明串联结构在一切频率下等同于一个确定值的 $R'$ 、 $L'$ 并联结构。</span></small>

---

454

第十八章 均匀传输线

及沿线电压与电流的变化,必须认为导线的每一元段(无限小长度的一段)上,在导线上具有无限小的电阻和电感;在导线间则有电容和电导。这就是传输线的分布参数模型,它是集总参数元件构成的极限情况。由于电阻、电感、电容和电导这些参数是分布在线上的,因此必须用单位长度上传输线具有的参数表示,即:

$R_{0}$ ——两根导线每单位长度具有的电阻,其单位为  $\Omega/m$  (在电力传输线中,常用  $\Omega/km$ )。

$L_{0}$ ——两根导线每单位长度具有的电感,其单位为 H/m(或 H/km)。

$C_{0}$ ——每单位长度导线之间的电容,其单位为 F/m(或 F/km)。

$G_{0}$ ——每单位长度导线之间的电导,其单位为 S/m(或 S/km)。

$R_{0}$ 、 $L_{0}$ 、 $C_{0}$ 、 $G_{0}$ 称为传输线的原参数，如果沿线原参数到处相等，则称为均匀传输线。图18-3中图(a)(b)(c)(d)均可看为均匀传输线，图(e)(f)则是不均匀传输线。当然实际的传输线不可能是均匀的。例如图18-3(a)所示的两线架空线在有支架处和没有支架处是不一样的，因为漏电的情况不尽相同。在架空线的每一跨度之间，由于导线的自重引起的下垂情况也改变了传输线对大地的电容的分布均匀性。但是，为了便于分析起见，通常忽略所有造成不均匀性的因素而把实际的传输线当作均匀的传输线。以后的讨论都局限于均匀传输线。

![](../../raw/pages_0449-0480/images/page_477_image_9.jpg)

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

---

§ 18-3 均匀传输线方程的正弦稳态解

455

对回路 abcda 应用 KVL, 则有

$$
u - \left(u + \frac {\partial u}{\partial x} \mathrm{d} x\right) = R _ {0} i \mathrm{d} x + L _ {0} \frac {\partial i}{\partial t} \mathrm{d} x
$$

![](../../raw/pages_0449-0480/images/page_478_image_4.jpg)

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

其中 $Z_0 = R_0 + \mathrm{j}\omega L_0$ 为单位长度的阻抗，$Y_0 = G_0 + \mathrm{j}\omega C_0$ 为单位长度的导纳。由于相量 $\dot{U}$ 和 $\dot{I}$ 仅为距离 $x$ 的函数，所以在式(18-1)中对 $u$ 和 $i$ 的偏导数可以写成全导数，这样，

---

456

第十八章 均匀传输线

式(18-1)的偏微分方程组就成为式(18-2)的常微分方程组。将式(18-2)对 $x$ 取一次导数，得

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

---

§ 18-3 均匀传输线方程的正弦稳态解

457

一种是设传输线的始端电压  $\dot{U}_{1}$  和电流  $\dot{I}_{1}$  为已知。当以始端作为计算距离 x 的起点时，在始端处 x=0。根据给定的边界条件，由式(18-3)可以得到

$$
\dot {U} _ {\mathrm{1}} = A _ {1} + A _ {2}
$$

$$
\dot {I} _ {1} = \frac {A _ {1}}{Z _ {\mathrm{c}}} - \frac {A _ {2}}{Z _ {\mathrm{c}}}
$$

解得

$$
A _ {1} = \frac {1}{2} (\dot {U} _ {1} + Z _ {\mathrm{c}} \dot {I} _ {1})
$$

$$
A _ {2} = \frac {1}{2} (\dot {U} _ {\mathrm{t}} - Z _ {\mathrm{c}} \dot {I} _ {1})
$$

由此得到传输线上与始端的距离为 x 处的电压和电流为

$$
\begin{array}{r l} \dot {U} & = \frac {1}{2} (\dot {U} _ {1} + Z _ {\mathrm{c}} \dot {I} _ {1}) \mathrm{e} ^ {- \gamma x} + \frac {1}{2} (\dot {U} _ {1} - Z _ {\mathrm{c}} \dot {I} _ {1}) \mathrm{e} ^ {\gamma x} \\ \dot {I} & = \frac {1}{2} \left(\frac {\dot {U} _ {1}}{Z _ {\mathrm{c}}} + \dot {I} _ {1}\right) \mathrm{e} ^ {- \gamma x} - \frac {1}{2} \left(\frac {\dot {U} _ {1}}{Z _ {\mathrm{c}}} - \dot {I} _ {1}\right) \mathrm{e} ^ {\gamma x} \end{array} \tag {18-4}
$$

利用双曲线函数

$$
\cosh (\gamma x) = \frac {1}{2} (\mathrm{e} ^ {\gamma x} + \mathrm{e} ^ {- \gamma x})
$$

$$
\sinh (\gamma x) = \frac {1}{2} (\mathrm{e} ^ {\gamma x} - \mathrm{e} ^ {- \gamma x})
$$

式(18-4)又可以改写为

$$
\left. \begin{array}{l} \dot {U} = \dot {U} _ {1} \cosh (\gamma x) - Z _ {\mathrm{e}} \dot {I} _ {1} \sinh (\gamma x) \\ \dot {I} = \dot {I} _ {1} \cosh (\gamma x) - \frac {\dot {U} _ {1}}{Z _ {\mathrm{e}}} \sinh (\gamma x) \end{array} \right\} \tag {18-5}
$$

另一种情况是设传输线终端(即 x=l 处, l 为线长)的电压  $\dot{U}_{2}$  和电流  $\dot{I}_{2}$  为已知。根据这种边界条件,从式(18-3)得

$$
\dot {U} _ {2} = A _ {1} \mathrm{e} ^ {- \gamma l} + A _ {2} \mathrm{e} ^ {\gamma l}
$$

$$
\dot {I} _ {2} = \frac {A _ {1}}{Z _ {\mathrm{c}}} \mathrm{e} ^ {- \gamma l} - \frac {A _ {2}}{Z _ {\mathrm{c}}} \mathrm{e} ^ {\gamma l}
$$

从而有

$$
A _ {1} = \frac {1}{2} (\dot {U} _ {2} + Z _ {\mathrm{c}} \dot {I} _ {2}) \mathrm{e} ^ {\gamma l}
$$

$$
A _ {2} = \frac {1}{2} (\dot {U} _ {2} - Z _ {\mathrm{c}} \dot {I} _ {2}) \mathrm{e} ^ {- \gamma l}
$$

这样,当终端的电压  $\dot{U}_{2}$  和电流  $\dot{I}_{2}$  已知时,传输线上与始端距离为 x 处的任一点电压和电流为

1. 用 $\mathrm{H}_2\mathrm{O}$ 气相分离的气体，用于气体交换反应。

---

[No text]

458

第十八章 均匀传输线

$$
\dot {U} = \frac {1}{2} \left(\dot {U} _ {2} + Z _ {\mathrm{c}} \dot {I} _ {2}\right) \mathrm{e} ^ {\gamma (l - x)} + \frac {1}{2} \left(\dot {U} _ {2} - Z _ {\mathrm{c}} \dot {I} _ {2}\right) \mathrm{e} ^ {- \gamma (l - x)}
$$

$$
\dot {I} = \frac {1}{2} \left(\frac {\dot {U} _ {2}}{Z _ {\mathrm{c}}} + \dot {I} _ {2}\right) \mathrm{e} ^ {\gamma (l - x)} - \frac {1}{2} \left(\frac {\dot {U} _ {2}}{Z _ {\mathrm{c}}} - \dot {I} _ {2}\right) \mathrm{e} ^ {- \gamma (l - x)}.
$$

如果把计算距离的起点改为传输线的终端,则线上任一点到终端的距离为  $x' = l - x$ , 上式可以改写为

$$
\left. \begin{array}{l} \dot {U} = \frac {1}{2} (\dot {U} _ {2} + Z _ {\mathrm{c}} \dot {I} _ {2}) \mathrm{e} ^ {\gamma x ^ {\prime}} + \frac {1}{2} (\dot {U} _ {2} - Z _ {\mathrm{c}} \dot {I} _ {2}) \mathrm{e} ^ {- \gamma x ^ {\prime}} \\ \dot {I} = \frac {1}{2} \left(\frac {\dot {U} _ {2}}{Z _ {\mathrm{c}}} + \dot {I} _ {2}\right) \mathrm{e} ^ {\gamma x ^ {\prime}} - \frac {1}{2} \left(\frac {\dot {U} _ {2}}{Z _ {\mathrm{c}}} - \dot {I} _ {2}\right) \mathrm{e} ^ {- \gamma x ^ {\prime}} \end{array} \right\} \tag {18-6}
$$

通常把上式的 $x'$ 仍记为 $x$, 这样做并不会引起混淆, 因为式中右方的 $\dot{U}_2$ 和 $\dot{I}_2$ 就意味着以传输线的终端作为计算距离的起点。

同样,将式(18-6)用双曲线函数表示时,得

$$
\left. \begin{array}{l} \dot {U} = \dot {U} _ {2} \cosh (\gamma x) + Z _ {\mathrm{c}} \dot {I} _ {2} \sinh (\gamma x) \\ \dot {I} = \dot {I} _ {2} \cosh (\gamma x) + \frac {\dot {U} _ {2}}{Z _ {\mathrm{c}}} \sinh (\gamma x) \end{array} \right\} \tag {18-7}
$$

式中 x 为距终端的距离。

例 18-1 一高压线长 l=300 km, 终端接负载, 功率为 30 MW, 功率因数  $\lambda=0.9$  (感性), 已知输电线的  $Z_{0}=1\angle80^{\circ}\Omega/km, Y_{0}=6.5\times10^{-6}\angle90^{\circ}S/km$ 。设负载端电压  $\dot{U}_{2}=115.5\angle0^{\circ}kV$ , 求距离始端 200 km 处的电压、电流相量。

解  $I_{2}=\frac{30\times10^{6}}{115.5\times10^{3}\times0.9}$  A=288.6 A

$$
\dot {I} _ {2} = 2 8 8. 6 / - 2 5. 8 4 ^ {\circ} \mathrm{A}
$$

$$
\gamma = \sqrt {Z _ {0} Y _ {0}} = 2. 5 5 \times 1 0 ^ {- 3} / 8 5 ^ {\circ} \mathrm{km} ^ {- 1}
$$

$$
Z _ {\mathrm{c}} = \sqrt {\frac {Z _ {0}}{Y _ {0}}} = 3 9 2. 2 / - 5 ^ {\circ} \Omega
$$

距离始端 200 km 即距离终端 100 km, 该处电压和电流分别为

$$
\begin{array}{l} \dot {U} = \dot {U} _ {2} \cosh (1 0 0 \gamma) + Z _ {\circ} \dot {I} _ {2} \sinh (1 0 0 \gamma) \\ = (1 2 8. 3 + j 2 3. 9 5) \mathrm{kV} \\ = 1 3 0. 5 / 1 0. 5 ^ {\circ} \mathrm{kV} \\ \end{array}
$$

$$
\begin{array}{l} \dot {I} = \dot {I} _ {2} \cosh (1 0 0 \gamma) + \frac {\dot {U} _ {2}}{Z _ {\mathrm{c}}} \sinh (1 0 0 \gamma) \\ = (2 5 2. 9 - \mathrm{j} 4 4. 1 1) \mathrm{A} \\ = 2 5 6. 7 / - 9. 8 9 3 ^ {\circ} \mathrm{A} \\ \end{array}
$$

---

§ 18-3 均匀传输线方程的正弦稳态解

459

其中 $100\gamma = 0.255 / 85^{\circ} = 0.0222 + \mathrm{j}0.254$

而

$$
\begin{array}{l} \sinh (1 0 0 \gamma) = 0. 2 5 2 / 8 5. 1 1 ^ {\circ} \\ \cosh (1 0 0 \gamma) = 0. 9 6 8 / 0. 3 3 ^ {\circ} \\ \end{array}
$$

为了说明传输线上的电压、电流是波动形式,可以从式(18-4)出发,先将该式中的 $\dot{U}$ 、 $\dot{I}$ 表达式改写如下:

$$
\left. \begin{array}{l} \dot {U} = \dot {U} ^ {+} + \dot {U} ^ {-} \\ \dot {I} = \dot {I} ^ {+} - \dot {I} ^ {-} \end{array} \right\} \tag {18-8}
$$

其中

$$
\begin{array}{l} \dot {U} ^ {+} = A _ {1} \mathrm{e} ^ {- \gamma x} = \frac {1}{2} (\dot {U} _ {1} + Z _ {\mathrm{c}} \dot {I} _ {1}) \mathrm{e} ^ {- \gamma x} \\ = \left| A _ {1} \right| \mathrm{e} ^ {\mathrm{j} \phi_ {+}} \cdot \mathrm{e} ^ {- \gamma x} = U _ {0} ^ {+} \mathrm{e} ^ {\mathrm{j} \phi_ {+}} \cdot \mathrm{e} ^ {- \gamma x} \\ \dot {U} ^ {-} = A _ {2} \mathrm{e} ^ {\gamma x} = \frac {1}{2} (\dot {U} _ {1} - Z _ {\mathrm{c}} \dot {I} _ {1}) \mathrm{e} ^ {\gamma x} \\ = \left| A _ {2} \right| \mathrm{e} ^ {\mathrm{j} \phi_ {-}} \cdot \mathrm{e} ^ {\gamma x} = U _ {0} ^ {-} \mathrm{e} ^ {\mathrm{j} \phi_ {-}} \cdot \mathrm{e} ^ {\gamma x} \\ \end{array}
$$

$$
\begin{array}{l} \dot {U} ^ {-} = A _ {2} \mathrm{e} ^ {\gamma x} = \frac {1}{2} (\dot {U} _ {1} - Z _ {\mathrm{c}} \dot {I} _ {1}) \mathrm{e} ^ {\gamma x} \\ = \left| A _ {2} \right| \mathrm{e} ^ {\mathrm{j} \phi_ {-}} \cdot \mathrm{e} ^ {\gamma x} = U _ {0} ^ {-} \mathrm{e} ^ {\mathrm{j} \phi_ {-}} \cdot \mathrm{e} ^ {\gamma x} \\ \end{array}
$$

式中 $U_{0}^{+} = \left|A_{1}\right|, U_{0}^{-} = \left|A_{2}\right|$; 对于电流有 $\dot{I}^{+} = \frac{\dot{U}^{+}}{Z_{\mathrm{c}}}, \dot{I}^{-} = \frac{\dot{U}^{-}}{Z_{\mathrm{c}}}$。

由于  $\gamma=\alpha+j\beta$ ，式(18-8)中电压  $\dot{U}$  可写为

$$
\dot {U} = U _ {0} ^ {+} \mathrm{e} ^ {- \alpha x} \mathrm{e} ^ {\mathrm{j} (\phi_ {+} - \beta x)} + U _ {0} ^ {-} \mathrm{e} ^ {\alpha x} \mathrm{e} ^ {\mathrm{j} (\phi_ {-} + \beta x)}
$$

现在把电压相量  $\dot{U}$  化为时间函数形式, 得

$$
\begin{array}{l} u = \sqrt {2} U _ {0} ^ {+} \mathrm{e} ^ {- \alpha x} \cos (\omega t - \beta x + \phi_ {+}) + \sqrt {2} U _ {0} ^ {-} \mathrm{e} ^ {\alpha x} \cos (\omega t + \beta x + \phi_ {-}) \\ = u ^ {+} + u ^ {-} \tag {18-9} \\ \end{array}
$$

这样一来，u 可以看作是两个电压分量  $u^{+}$  和  $u^{-}$  的叠加。现在分别研究  $u^{+}$  和  $u^{-}$  这两个分量具有的含义。第一个分量  $u^{+}$  为

$$
u ^ {+} = \sqrt {2} U _ {0} ^ {+} \mathrm{e} ^ {- \alpha x} \cos (\omega t - \beta x + \phi_ {+})
$$

它既是时间 $t$ 的函数，又是空间位置 $x$ 的函数。如果在传输线的某一固定点，即 $x = x_{1}$ 的地方观察 $u^{+}$，它将是时间 $t$ 的正弦函数。假想在某一固定瞬间 $t = t_{1}$ 观察，则 $u^{+}$沿线按照振幅为指数衰减的正弦规律随 $x$ 变化。为了便于理解 $u^{+}$的性质，在图18-6中画出3个不同瞬间 $u^{+}$沿线的分布情况。可见，可以把 $u^{+}$看为一个随时间增加向 $x$ 增加方向（即从线的始端向终端的方向）运动的衰减波。通常将这种波称为电压入射波、直波或正向行波。

为了确定这个电压波 $u^{+}$ 运动或传播的速度，假设 $\alpha = 0$ ，这时 $u^{+} = \sqrt{2} U_{0}^{+}\cos (\omega t - \beta x + \phi_{+})$ ，也就是说把 $u^{+}$ 看作是一个不衰减的正弦波。现在分析 $x = x_{1}$ 与 $x = x_{2}$ 两点上电压波动的情况。在 $x = x_{1}$ 处，$u^{+}(x_{1},t) = \sqrt{2} U_{0}^{+}\cos (\omega t - \beta x_{1} + \phi_{+})$ ，而在 $x = x_{2}$ 处，$u^{+}(x_{2},t) =$

---

图 1-2

460

第十八章 均匀传输线

$\sqrt{2} U_0^+ \cos (\omega t - \beta x_2 + \phi_+)$ 。若 $x_2 > x_1$ ，则该两点电压正弦变化的相位关系是 $u^+(x_2, t)$ 比 $u^+(x_1, t)$ 落后，落后的相位为 $(- \beta x_1 + \phi_)-(- \beta x_2 + \phi_)=\beta (x_2 - x_1)=\beta \Delta x$ 。因此，在 $x_1$ 处出现的正弦时间变化过程，要在一定的时间差后才会在距 $x_1$ 为 $\Delta x$ 的 $x_2$ 处重复出现。这一时间差为

$$
\Delta t = \frac {\beta (x _ {2} - x _ {1})}{\omega} = \frac {\beta \Delta x}{\omega}
$$

故相应的沿线从始端向终端传播速度为.

$$
v _ {\varphi} = \lim _ {\Delta t \to 0} \frac {\Delta x}{\Delta t} = \frac {\omega}{\beta} \tag {18-10}
$$

这就是整个电压波  $u^{+}$  的传播速度。由于这是同相点的运动速度，称为相位速度，简称相速，以  $v_{\varphi}$  表示。

![](../../raw/pages_0481-0512/images/page_483_chart_8.jpg)

<details>
<summary>line</summary>

| Category | Description |
| --- | --- |
| Curve 1 | \(\sqrt{2}U_0^+e^{-ax}\) |
| Curve 2 | \(-\sqrt{2}U_0^+e^{-ax}\) |
| Curve 3 | \(t_1<t_2<t_3\) |
</details>

图 18-6 入射波沿线的传播

用同样的方法研究式(18-9)右端的第二项

$$
u ^ {-} = \sqrt {2} U _ {0} ^ {-} \mathrm{e} ^ {\alpha x} \cos (\omega t + \beta x + \phi_ {-})
$$

它与 $u^{+}$ 不同之处在于式中 $\alpha x$ 与 $\beta x$ 前面的符号恰好相反，所以可以说 $u^{-}$ 也是一种行波，但其传播方向和 $u^{+}$ 相反，也即 $u^{-}$ 是沿 $x$ 减少的方向以相速 $v_{\varphi}$ 传播的衰减波，即由终端沿线向始端传播的衰减正弦波。通常把 $u^{-}$ 称为电压反射波、回波或反向行波。注意在式(18-9)中 $u = u^{+} + u^{-}$，所以 $u^{+}$ 和 $u^{-}$ 所取参考方向与 $u$ 的参考方向一致，也就是把传输线的来线取为正极。

在波的传播方向上,相位差  $2\pi$  的两点间的距离称为波长,以  $\lambda$  表示。这样,从式 (18-9) 右端的第一项,得

$$
\omega t - \beta (x + \lambda) + \phi_ {+} = \omega t - \beta x + \phi_ {+} - 2 \pi
$$

从而得

$$
\lambda = \frac {2 \pi}{\beta} \tag {18-11}
$$

---

§ 18-3 均匀传输线方程的正弦稳态解

461

而

$$
v _ {\varphi} = \frac {\omega}{\beta} = \frac {2 \pi f}{\beta} = \lambda f = \frac {\lambda}{T} \tag {18-12}
$$

也就是在一个周期的时间内,波传播的距离等于一个波长。

在式(18-8)中的电流相量 $\dot{I}$ 也可以写成相应的时间函数形式

$$
\begin{array}{l} i = \sqrt {2} \frac {U _ {0} ^ {+}}{\left| Z _ {\mathrm{c}} \right|} \mathrm{e} ^ {- \alpha x} \cos (\omega t - \beta x + \phi_ {+} - \theta) - \sqrt {2} \frac {U _ {0} ^ {-}}{\left| Z _ {\mathrm{c}} \right|} \mathrm{e} ^ {\alpha x} \cos (\omega t + \beta x + \phi_ {-} - \theta) \\ = i ^ {+} - i ^ {-} \tag {18-13} \\ \end{array}
$$

其中 $|Z_{\mathrm{c}}|$ 和 $\theta$ 为特性阻抗 $Z_{\mathrm{c}}$ 的模和辐角，即 $Z_{\mathrm{c}} = |Z_{\mathrm{c}}| / \theta$ 。可见电流 $i$ 也可以看作是两个以相同的相位速度、但以相反方向传播的衰减正弦波，即入射波电流 $i^{+}$ 和反射波电流 $i^{-}$ 叠加的结果。但须注意，对于反射波电流 $i^{-}$，由于在导线中其方向与入射波电流的方向相反，故两者为相减。可以看出，虽然合成的电压波与电流波的形式很复杂，但对同一方向行进的入射电压波与入射电流波，或是反射电压波与反射电流波，都是随行进方向衰减的行波；且电压波与电流波之间的关系由传输线特性阻抗 $Z_{\mathrm{c}}$ 来决定。

例 18-2 有一均匀传输线长 300 km，在频率 f=50 Hz 时，传播常数  $\gamma=1.06\times10^{-3}/84.7^{\circ}km^{-1}$ ， $Z_{e}=400/-5.3^{\circ}\Omega$ ，若已知  $\dot{U}_{1}=120/0^{\circ}kV,\dot{I}_{1}=30/-10^{\circ}A$ 。求:(1) 行波的相速；(2) 距始端 50 km 处电压、电流入射波和反射波的瞬时值表达式。

解（1）由于 $\gamma = 1.06\times 10^{-3} / 84.7^{\circ}\mathrm{km}^{-1} = (0.979\times 10^{-4} + \mathrm{j}1.055\times 10^{-3})\mathrm{km}^{-1}$ ，故相速

$$
v _ {\varphi} = \frac {\omega}{\beta} = \frac {2 \pi \times 5 0}{1 . 0 5 5 \times 1 0 ^ {- 3}} \mathrm{km/s} = 2. 9 8 \times 1 0 ^ {5} \mathrm{km/s}
$$

(2) 按式(18-4)和式(18-8)求出  $\dot{U}_{1}^{+}$  和  $\dot{U}_{1}^{-}$  为

$$
\dot {U} _ {1} ^ {+} = \frac {1}{2} \left(\dot {U} _ {1} + Z _ {\mathrm{c}} \dot {I} _ {1}\right) = 6 5 8 0 6 / - 1. 3 8 1 ^ {\circ} \mathrm{V}
$$

$$
\dot {U} _ {1} ^ {-} = \frac {1}{2} (\dot {U} _ {1} - Z _ {\mathrm{c}} \dot {I} _ {1}) = 5 4 2 3 6 / 1. 6 7 3 ^ {\circ} \mathrm{V}
$$

由式(18-9)可得

$$
u ^ {+} = \sqrt {2} \times 6 5 8 0 6 \mathrm{e} ^ {- 0. 9 7 9 \times 1 0 ^ {- 4} x} \cos (3 1 4 t - 1. 0 5 5 \times 1 0 ^ {- 3} x - 1. 3 8 1 ^ {\circ}) \mathrm{V}
$$

$$
u ^ {-} = \sqrt {2} \times 5 4 2 3 6 \mathrm{e} ^ {0. 9 7 9 \times 1 0 ^ {- 4} x} \cos (3 1 4 t + 1. 0 5 5 \times 1 0 ^ {- 3} x + 1. 6 7 3 ^ {\circ}) \mathrm{V}
$$

所以在  $x=50\ km$  处, 有

$$
u ^ {+} = \sqrt {2} \times 6 5 4 8 6 \cos (3 1 4 t - 4. 4 0 5 ^ {\circ}) \mathrm{V}
$$

$$
u ^ {-} = \sqrt {2} \times 5 4 5 0 2 \cos (3 1 4 t + 4. 6 9 7 ^ {\circ}) \mathrm{V}
$$

根据电压与电流入射波与反射波之间的关系,可得

$$
i ^ {+} = \sqrt {2} \times 1 6 3. 7 1 \cos (3 1 4 t + 0. 9 ^ {\circ}) \mathrm{A}
$$

$$
i ^ {-} = \sqrt {2} \times 1 3 6. 2 5 \cos (3 1 4 t + 1 0 ^ {\circ}) \mathrm{A}
$$

---

1. 用 $\mathrm{H}_{2}$ 气相分离的气体，用于气体的蒸馏过程。

462

第十八章 均匀传输线

当传输线终端所接的负载阻抗  $Z_{2}=Z_{c}$  时，电压、电流波中均没有反射波。因此可以认为反射波是由于  $Z_{2}$  与  $Z_{c}$  不等而引起的。定义终端的反射系数为该处反射波与入射波电压相量或电流相量之比，即

$$
n = \frac {\dot {U} _ {2} ^ {-}}{\dot {U} _ {2} ^ {+}} = \frac {\dot {I} _ {2} ^ {-}}{\dot {I} _ {2} ^ {+}} = \frac {\dot {U} _ {2} - Z _ {\mathrm{c}} \dot {I} _ {2}}{\dot {U} _ {2} + Z _ {\mathrm{c}} \dot {I} _ {2}} = \frac {Z _ {2} - Z _ {\mathrm{c}}}{Z _ {2} + Z _ {\mathrm{c}}} \tag {18-14}
$$

反射系数是一个复数,反映了反射波与入射波在幅值和相位上的差异。n=0时,不存在反射,称为终端阻抗与传输线阻抗相匹配 $^{①}$ 。在通信线路和设备连接(例如电视接收机与信号馈线的连接)时,均要求匹配,避免反射。

终端开路时, $Z_{2}\rightarrow\infty,n=1$ ; 终端短路时, $Z_{2}=0,n=-1$ 。 $|n|=1$ 称为全反射。终端开路及短路都产生全反射,但相位不同,前者使 $\dot{I}_{2}=0$ ,后者使 $\dot{U}_{2}=0$ ,满足了边界条件。

## §18-4 均匀传输线的原参数和副参数

传输线单位长度的电阻  $R_{0}$ 、电感  $L_{0}$ 、电容  $C_{0}$  和电导  $G_{0}$  称为它的原参数， $L_{0}$  和  $C_{0}$  的计算公式在电磁场课程中介绍。上一节引入的传播常数  $\gamma$  和特性阻抗  $Z_{0}$  称为传输线的副参数。

传播常数 $\gamma$ 是一个复数, 其实部 $\alpha$ 称为衰减常数, 虚部 $\beta$ 称为相位常数。从式 (18-9) 及以后有关的讨论中可以看出, $\alpha$ 表示入射波和反射波沿线的衰减特性, 其单位通常用 $\mathrm{Np/m}$ 或 $\mathrm{dB/m}^{②}$; 而 $\beta$ 表示入射波和反射波沿线的相位变化的特性, 其单位通常用 $\mathrm{rad/m}$ 。

为了计算均匀传输线的  $\alpha$  和  $\beta$ ，设  $R_{0}$ 、 $L_{0}$ 、 $C_{0}$  和  $G_{0}$  为已知，则根据  $\gamma = \alpha + j\beta$  有

$$
\gamma = \alpha + \mathrm{j} \beta = \sqrt {Z _ {0} Y _ {0}} = \sqrt {\left(R _ {0} + \mathrm{j} \omega L _ {0}\right) \left(G _ {0} + \mathrm{j} \omega C _ {0}\right)}
$$

所以

$$
\mid \gamma \mid^ {2} = \alpha^ {2} + \beta^ {2} = \sqrt {\left(R _ {0} ^ {2} + \omega^ {2} L _ {0} ^ {2}\right) \left(G _ {0} ^ {2} + \omega^ {2} C _ {0} ^ {2}\right)}
$$

$$
\gamma^ {2} = \alpha^ {2} - \beta^ {2} + \mathrm{j} 2 \alpha \beta = (R _ {0} G _ {0} - \omega^ {2} L _ {0} C _ {0}) + \mathrm{j} (G _ {0} \omega L _ {0} + R _ {0} \omega C _ {0})
$$

① 这里的“匹配”（即  $Z_{2}=Z_{c}$ ），与最大功率传输时的匹配是不同的。

② 在有线通信中通常用奈培(Neper, Np)表示电平。Np是根据研究的量的比值的自然对数定义的。以两个电压 $U_{1}$ 、 $U_{2}$ 为例，有

$$
H _ {\mathrm{NP}} = \ln \left(\left| \frac {U _ {2}}{U _ {1}} \right|\right)
$$

前面已指出分贝(dB)是根据常用对数定义的,即

$$
H _ {\mathrm{dB}} = 2 0 \lg \left(\left| \frac {U _ {2}}{U _ {1}} \right|\right)
$$

由上述定义,可推出

1 Np = 8.686 dB

1 dB = 0.115 Np

---

§ 18-4 均匀传输线的原参数和副参数

463

图 2

从以上两式不难分别求得

$$
\left. \begin{array}{l} \alpha = \sqrt {\frac {1}{2} \left[ R _ {0} G _ {0} - \omega^ {2} L _ {0} C _ {0} + \sqrt {\left(R _ {0} ^ {2} + \omega^ {2} L _ {0} ^ {2}\right) \left(G _ {0} ^ {2} + \omega^ {2} C _ {0} ^ {2}\right)} \right]} \\ \beta = \sqrt {\frac {1}{2} \left[ \omega^ {2} L _ {0} C _ {0} - R _ {0} G _ {0} + \sqrt {\left(R _ {0} ^ {2} + \omega^ {2} L _ {0} ^ {2}\right) \left(G _ {0} ^ {2} + \omega^ {2} C _ {0} ^ {2}\right)} \right]} \end{array} \right\} \tag {18-15}
$$

值得注意的是,相位常数 $\beta$ 是单调地随频率增高而增加的,图18-7给出了 $\alpha$ 和 $\beta$ 与角频率的变化关系。

按式(18-10)和式(18-11)，相位速度和波长是由相位常数 $\beta$ 决定的，即有

$$
v _ {\varphi} = \frac {\omega}{\beta}, \quad \lambda = \frac {2 \pi}{\beta}
$$

当传输线的原参数满足条件 $\frac{R_{0}}{G_{0}}=\frac{L_{0}}{C_{0}}$ 时，按式(18-15)可推得

$$
\alpha = \sqrt {\frac {1}{2} (R _ {0} G _ {0} - \omega^ {2} L _ {0} C _ {0} + R _ {0} G _ {0} + \omega^ {2} L _ {0} C _ {0})} = \sqrt {R _ {0} G _ {0}}
$$

$$
\beta = \sqrt {\frac {1}{2} (\omega^ {2} L _ {0} C _ {0} - R _ {0} G _ {0} + R _ {0} G _ {0} + \omega^ {2} L _ {0} C _ {0})} = \omega \sqrt {L _ {0} C _ {0}}
$$

此时，衰减系数 $\alpha$ 与频率无关；相位系数 $\beta$ 与频率成正比，故相速 $v_{\varphi}$ 也与频率无关，且 $\alpha, \beta$ 均达其最小值，这种传输线称为无畸变线。当非正弦信号在线上传输时，各次谐波分量将发生同样程度的衰减且以同样的速度传输，因而不会发生畸变。这一条件也称为传输线的无畸变条件①。满足 $R_0 = G_0 = 0$ 的传输线称为无损耗线（将在 §18-5 中讨论），此时 $\alpha = 0, \beta = \omega \sqrt{L_0 C_0}$，因此，无损耗线也是无畸变线。图18-7示出了 $\alpha$ 与 $\beta$ 的频率特性，可以看出，当 $\omega$ 很高时，传输线也接近于无畸变线。对于上述两种情况，有

$$
v _ {\varphi} = \frac {1}{\sqrt {L _ {0} C _ {0}}}
$$

或②

$$
v _ {\varphi} \approx \frac {c}{\sqrt {\varepsilon_ {\mathrm{r}} \mu_ {\mathrm{r}}}}
$$

后一式中， $c$ 为真空中的光速， $\varepsilon_{\mathrm{r}}$ 和 $\mu_{\mathrm{r}}$ 分别为导线周围媒质的相对介电常数和相对磁导率。对于架空线， $\varepsilon_{\mathrm{r}}\approx 1$ 和 $\mu_{\mathrm{r}}\approx 1$ ，即波的传播速度 $v_{\varphi}$ 实际上等于真空中的光速。对于电

![](../../raw/pages_0481-0512/images/page_486_chart_16.jpg)

<details>
<summary>line</summary>

| \(\omega\) | \(\alpha (\)Value) | \(\beta (\)Value) |
| --- | --- | --- |
| 0 | ~0.25 | 0 |
| — | \(R_{0}/2 \sqrt{C_{0}/L_{0}} + G_{0}/2 \sqrt{L_{0}/C_{0}}\) | \(\sqrt{R_{0}G_{0}}\) |
</details>

图 18-7  $\alpha$  和  $\beta$  的频率特性

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 通常情况下的架空传输线和电缆都不满足无畸变条件，前者的 $C_0$ 小；后者的 $C_0$ 大。因此常常使用增加$L_{0}$ 的方法来满足无畸变传输。例如使用集中加感、分布加感等方法。</span></small>

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">② 此公式的证明需用计算  $L_{0}$  和  $C_{0}$  的公式，请参阅电磁场教材。</span></small>

---

464

第十八章 均匀传输线

缆, 这一速度要小一些, 因为电缆中用的绝缘介质的相对介电常数 $\varepsilon_{\mathrm{r}} \approx 4 \sim 5$, 所以波的相速比真空中的光速低。在有损耗的线中 $(R_{0} \neq 0, G_{0} \neq 0)$, 相速总是比光速小。

从式(18-8)可见。特性阻抗 $Z_{\mathrm{c}}$ 为入射波(或反射波)电压、电流相量的比值。它与原参数的关系是

$$
Z _ {\mathrm{c}} = \sqrt {\frac {Z _ {0}}{Y _ {0}}} = \sqrt {\frac {R _ {0} + \mathrm{j} \omega L _ {0}}{G _ {0} + \mathrm{j} \omega C _ {0}}} = | Z _ {\mathrm{c}} | \mathrm{e} ^ {\mathrm{j} \theta} \tag {18-16}
$$

式中

$$
\left| Z _ {0} \right| = \sqrt [ 4 ]{\frac {R _ {0} ^ {2} + \omega^ {2} L _ {0} ^ {2}}{G _ {0} ^ {2} + \omega^ {2} C _ {0} ^ {2}}} \tag {18-17}
$$

$$
\begin{array}{l} \theta = \frac {1}{2} \Bigg [ \arctan \bigg (\frac {\omega L _ {0}}{R _ {0}} \bigg) - \arctan \bigg (\frac {\omega C _ {0}}{G _ {0}} \bigg) \Bigg ] \\ = \frac {1}{2} \arctan \left(\frac {\omega L _ {0} G _ {0} - \omega C _ {0} R _ {0}}{R _ {0} G _ {0} + \omega^ {2} L _ {0} C _ {0}}\right) \tag {18-18} \\ \end{array}
$$

当  $\omega=0$  时, 即在直流情况下

$$
\mid Z _ {\mathrm{c}} \mid = \sqrt {\frac {R _ {0}}{G _ {0}}}, \quad \theta = 0
$$

此时特性阻抗是纯电阻。对工作频率较高的传输线，由于 $R_{0}\ll\omega L_{0}$ 和 $G_{0}\ll\omega C_{0}$ ，所以

$$
Z _ {\mathrm{c}} = \sqrt {\frac {R _ {0} + \mathrm{j} \omega L _ {0}}{G _ {0} + \mathrm{j} \omega C _ {0}}} = \sqrt {\frac {\mathrm{j} \omega L _ {0} \left(1 + \frac {R _ {0}}{\mathrm{j} \omega L _ {0}}\right)}{\mathrm{j} \omega C _ {0} \left(1 + \frac {G _ {0}}{\mathrm{j} \omega C _ {0}}\right)}} \approx \sqrt {\frac {L _ {0}}{C _ {0}}}
$$

可见,此时  $Z_{c}$  也是纯电阻性质的。

显然，$R_{0}=0$ 和 $G_{0}=0$ 的无损耗传输线的特性阻抗也是一个纯电阻，且其 $Z_{\mathrm{c}}=\sqrt{\frac{L_{0}}{C_{0}}}$。一般架空线的特性阻抗 $\left|Z_{\mathrm{c}}\right|$ 约为 $400\sim600\Omega$，而电力电缆约为 $50\Omega$，这是因为与架空线相比，电缆中的导线彼此相距较近，而且导线间的绝缘材料的相对介电常数 $\varepsilon_{\mathrm{r}}\approx4\sim5$，所以 $L_{0}$ 和 $C_{0}$ 的比值要比架空线的小。因此电缆的 $\left|Z_{\mathrm{c}}\right|$ 只有架空线的 $\frac{1}{8}\sim\frac{1}{6}$。在

通信中使用的同轴电缆的  $\left|Z_{c}\right|$  一般为 40\~100 Ω，常用的有 75 Ω 和 50 Ω 两种。

由于  $\omega C_{0} \gg G_{0}$ ，式(18-16)中分母复数的辐角接近  $45^{\circ}$ ，要比分子复数的辐角大，所以特性阻抗的辐角  $\theta$  常为负值。

根据式（18-17）和式（18-18）作出 $|Z_{c}|$ 和 $\theta$ 的频率特性如图18-8所示。从

![](../../raw/pages_0481-0512/images/page_487_chart_18.jpg)

图 18-8  $\left|Z_{c}\right|$  和  $\theta$  的频率特性

---

§ 18-5 无损耗传输线

465

1. 工程图

式(18-16)可以看出,当  $\omega=0$  时

$$
\mid Z _ {c} \mid = \sqrt {\frac {R _ {0}}{G _ {0}}}
$$

而当 $\omega \to \infty$ 时

$$
\mid Z _ {\mathrm{c}} \mid = \sqrt {\frac {L _ {0}}{C _ {0}}}
$$

不论是架空线还是电缆，都有 $\frac{R_0}{G_0} >\frac{L_0}{C_0}$ ，所以 $\omega = 0$ 时的 $|Z_{\mathrm{c}}|$ 比 $\omega \rightarrow \infty$ 时的大。

## §18-5 无损耗传输线

如果传输线的电阻  $R_{0}$  和导线间的漏电导  $G_{0}$  等于零, 这种传输线就称为无损耗传输线, 简称为无损耗线。

在无线电工程中由于工作频率较高,因此  $\omega L_{0} \gg R_{0}, \omega C_{0} \gg G_{0}$  。如将损耗略去不计,即令  $R_{0} = 0$  和  $G_{0} = 0$ , 不致引起较大的误差, 就可看为无损耗线。在这种情况下有

$$
\gamma = \sqrt {Z _ {0} Y _ {0}} = \sqrt {\left(\mathrm{j} \omega L _ {0}\right) \left(\mathrm{j} \omega C _ {0}\right)} = \mathrm{j} \omega \sqrt {L _ {0} C _ {0}}
$$

故 $\alpha = 0$ ，而 $\beta = \omega \sqrt{L_0C_0}$ 。特性阻抗

$$
Z _ {\mathrm{c}} = \sqrt {\frac {Z _ {0}}{Y _ {0}}} = \sqrt {\frac {L _ {0}}{C _ {0}}}
$$

可见无损耗的特性阻抗是一个纯电阻且与频率无关。

距终端 x 处的电压、电流为

$$
\left. \begin{array}{l} \dot {U} _ {x} = \dot {U} _ {2} \cos (\beta x) + \mathrm{j} Z _ {\mathrm{c}} \dot {I} _ {2} \sin (\beta x) \\ \dot {I} _ {x} = \dot {I} _ {2} \cos (\beta x) + \mathrm{j} \frac {\dot {U} _ {2}}{Z _ {\mathrm{c}}} \sin (\beta x) \end{array} \right\} \tag {18-19}
$$

距终端 x 处的入端阻抗为

$$
\begin{array}{l} Z _ {\mathrm{ix}} = \frac {\dot {U} _ {x}}{\dot {I} _ {x}} = \frac {\dot {U} _ {2} \cos (\beta x) + \mathrm{j} \dot {Z} _ {\mathrm{c}} \dot {I} _ {2} \sin (\beta x)}{\dot {I} _ {2} \cos (\beta x) + \mathrm{j} \frac {\dot {U} _ {2}}{Z _ {\mathrm{c}}} \sin (\beta x)} \\ = \frac {Z _ {2} \cos (\beta x) + \mathrm{j} Z _ {\mathrm{c}} \sin (\beta x)}{Z _ {\mathrm{c}} \cos (\beta x) + \mathrm{j} Z _ {2} \sin (\beta x)} Z _ {\circ} \tag {18-20} \\ \end{array}
$$

式中  $Z_{2}=\frac{\dot{U}_{2}}{\dot{I}_{2}}$  为终端的负载阻抗。

以下讨论几种特殊的终端情况。

第一种情况是终端阻抗与传输线匹配, 即  $Z_{2}=Z_{0}$  的情况。此时有

---

466

第十八章 均匀传输线

$$
\dot {U} _ {x} = \dot {U} _ {2} \cos (\beta x) + \mathrm{j} Z _ {\circ} I _ {2} \sin (\beta x) = \dot {U} _ {2} [ \cos (\beta x) + \mathrm{j} \sin (\beta x) ] = \dot {U} _ {2} \mathrm{e} ^ {\mathrm{j} \beta x}
$$

$$
\dot {I} _ {x} = \dot {I} _ {2} \mathrm{e} ^ {\mathrm{j} \beta x}
$$

$$
Z _ {\mathrm{ix}} = Z _ {\mathrm{c}}
$$

传输线上出现的电压、电流是从始端向终端传输的入射行波，且无振幅的衰减；在相位上，离始端越远处，相位越落后，但在同一点上，电压、电流则为同相，其振幅比等于 $Z_{c}$ （为实数）。电压、电流行波将电能从始端无损耗地传递到终端阻抗中去，不产生反射。

第二种情况为终端开路(即空载), $Z_{2}\rightarrow\infty$ 。此时 $\dot{I}_{2}=0$ 。从式(18-19)中可以得到\_\_\_\_

$$
\left. \begin{array}{l} \dot {U} _ {x} = \dot {U} _ {2} \cos (\beta x) \\ \dot {I} _ {x} = \mathrm{j} \frac {\dot {U} _ {2}}{Z _ {\mathrm{c}}} \sin (\beta x) \end{array} \right\} \tag {18-21}
$$

假设终端电压  $u_{2}=\sqrt{2}U_{2}\sin(\omega t)$ ，式(18-21)的时间函数形式为

$$
\left. \begin{array}{l} u _ {x} = \sqrt {2} U _ {2} \cos (\beta x) \sin (\omega t) \\ i _ {x} = \frac {\sqrt {2} U _ {2}}{Z _ {\mathrm{c}}} \sin (\beta x) \cos (\omega t) \end{array} \right\} \tag {18-22}
$$

表明传输线上出现的电压、电流并非行波。由于  $\beta=\frac{2\pi}{\lambda}$ ，因此在  $x=0,\frac{\lambda}{2},\lambda,\frac{3\lambda}{2},\cdots$  处  $\beta x=0,\pi,2\pi,\cdots$ ，此时  $\cos(\beta x)=\pm1,\sin(\beta x)=0$ ，故这些地方的电压值始终是沿线电压分布中的极值（最大或最小），称之为电压的波腹；而这些地方的电流值始终是沿线电流分布中的零值，称之为电流的波节。在  $x=\frac{\lambda}{4},\frac{3\lambda}{4},\frac{5\lambda}{4},\cdots$  处， $\beta x=\frac{\pi}{2},\frac{3\pi}{2},\frac{5\pi}{2},\cdots$ ， $\cos(\beta x)=0,\sin(\beta x)=\pm1$ ，故这些地方是电流的波腹也是电压的波节。图 18-9 画出几个不同瞬间  $u_{x}$  和  $i_{x}$  沿线的分布曲线，它们对应于时间  $t=0,\frac{T}{4},\frac{T}{2},\frac{3T}{4}$  等时刻。从图中

![](../../raw/pages_0481-0512/images/page_489_chart_12.jpg)

<details>
<summary>line</summary>

| Point | Description |
| --- | --- |
| x | Horizontal axis label |
| i(3T/4) | Lower amplitude curve |
| i(0) | Intersection point on the first wave |
| i(T/2) | Upper amplitude curve |
| i(T/4) | Intersection point on the second wave |
| u(0) | Intersection point on the third wave |
| \(\lambda\) | Total duration of the wave |
</details>

图 18-9 空载无损耗线的电压和电流分布曲线

---

§ 18-5 无损耗传输线

467

可看出电流、电压的波腹、波节的位置是固定不变的。这种波腹、波节位置固定不变的波称为驻波。

空载时,在距终端 x 处向终端看去的输入阻抗为

$$
Z _ {\mathrm{ix}} = \frac {\dot {U} _ {x}}{\dot {I} _ {x}} = - \mathrm{j} Z _ {\mathrm{c}} \cot (\beta x) = - \mathrm{j} Z _ {\mathrm{c}} \cot \left(\frac {2 \pi}{\lambda} x\right) = \mathrm{j} X _ {\mathrm{oc}} \tag {18-23}
$$

表明输入阻抗是一个纯电抗，以 $\frac{\lambda}{4}$ 为间隔变号；在电压波节（电流波腹）处，$Z_{ix} = 0$ ，相当于短路，也可理解为是一个串联谐振电路①；在电流波节（电压波腹）处，$Z_{ix} = \infty$ ，相当于开路，理解为是一个并联谐振电路。如图18-10所示。

![](../../raw/pages_0481-0512/images/page_490_image_6.jpg)

<details>
<summary>text_image</summary>

Xoc
3λ/4
λ/2
λ/4
O
I
</details>

图 18-10 空载无损耗线的输入阻抗

第三种是终端短路的情况,此时, $Z_{2}=0,\dot{U}_{2}=0$ 。从式(18-19)可得

$$
\left. \begin{array}{l} \dot {U} _ {x} = \mathrm{j} Z _ {\mathrm{c}} \dot {I} _ {2} \sin (\beta x) \\ \dot {I} _ {x} = \dot {I} _ {2} \cos (\beta x) \end{array} \right\} \tag {18-24}
$$

设终端电流  $i_{2}=\sqrt{2}I_{2}\sin(\omega t)$ ，则  $\dot{U}_{x}$ 、 $\dot{I}_{x}$  对应的时间函数为

$$
\left. \begin{array}{l} u _ {x} = \sqrt {2} Z _ {\mathrm{c}} I _ {2} \sin (\beta x) \cos (\omega t) \\ i _ {x} = \sqrt {2} I _ {2} \cos (\beta x) \sin (\omega t) \end{array} \right\} \tag {18-25}
$$

传输线上也出现电压、电流驻波，但电压、电流驻波的波腹、波节位置与终端开路情况的位置不同，都移动了 $\frac{\lambda}{4}$ ②。图18-11示出了几个特定时刻线上出现的电压、电流驻波分布。

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 正弦稳态时，在终端开路或短路的无损耗线上电压或电流的波节处，功率为零 $(p_{x}=u_{x}i_{x})$ ，与谐振情况相似。</span></small>

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">② 根据  $Z_{ix}$  的意义, 在终端开路的无损耗线的电压波节处加以短路(例如在离开路终端  $\frac{\lambda}{4}$  处), 在此处与始端之间的电压、电流波形不会受到影响, 也就是短了  $\frac{\lambda}{4}$  长度的终端短路无损耗线。</span></small>

1

---

[No text]

468

第十八章 均匀传输线

![](../../raw/pages_0481-0512/images/page_491_chart_3.jpg)

<details>
<summary>line</summary>

| Component | Description |
| --- | --- |
| i(T/4) | Current component at the origin of the wave |
| u(T/2) | Current component at the center of the wave |
| u(0) | Current component at the peak of the wave |
</details>

图 18-11 短路无损耗线的电压和电流分布曲线

短路时,在距终端 x 处向终端看去的输入阻抗为

$$
Z _ {\mathrm{iz}} = \frac {\dot {U} _ {x}}{\dot {I} _ {x}} = \mathrm{j} Z _ {\mathrm{c}} \tan (\beta x) = \mathrm{j} Z _ {\mathrm{c}} \tan \left(\frac {2 \pi}{\lambda} x\right) = \mathrm{j} X _ {\mathrm{sc}} \tag {18-26}
$$

可见 $Z_{\mathrm{ix}}$ 也是一个纯电抗。输入阻抗随 $x$ 的变化如图18-12所示，与空载无损耗线阻抗图18-10比较，可见两者图形仅在长度上有 $\frac{\lambda}{4}$ 的移动。

![](../../raw/pages_0481-0512/images/page_491_image_8.jpg)

<details>
<summary>text_image</summary>

Xoc
3λ/4      λ/2      Xoc
λ/4      O
l λ       O
</details>

图 18-12 短路无损耗线的输入阻抗

上述无损耗线在终端开路或短路时,其输入阻抗具有的一些特点在高频技术中获得了一定的应用。

例如长度小于 $\frac{\lambda}{4}$ 的开路无损耗线可以用来代替电容,而长度小于 $\frac{\lambda}{4}$ 的短路无损耗线可以用来代替电感。考虑到频率较高时,常用的电感线圈或电容器已经不可能作为电感元件或电容元件工作,这种方法的意义就更明显了。假定要替代的容抗 $X_{c}$ 或感抗

---

§ 18-5 无损耗传输线

469

$X_{L}$  为已知,则利用下列公式就可以分别决定所需开路无损耗线或短路无损耗线的长度 l:

$$
\begin{array}{l} X _ {c} = - \frac {1}{\omega C} = - Z _ {\mathrm{e}} \cot \left(\frac {2 \pi}{\lambda} l\right), \\ X _ {L} = \omega L = Z _ {\mathrm{c}} \tan \left(\frac {2 \pi}{\lambda} l\right) \\ \end{array}
$$

长度为 $\frac{\lambda}{4}$ 的无损耗线,还可以用来作为接在传输线和负载之间的匹配元件,它的作用如同一个阻抗变换器。下面介绍其工作原理。

设无损耗线的特性阻抗为 $Z_{\mathrm{el}}$ ，负载阻抗为 $Z_{2}$ ，且设 $Z_{2}$ 为纯电阻（即 $Z_{2} = R_{2}$ ），现在

要求设法使 $Z_{2}$ 和 $Z_{\mathrm{cl}}$ 匹配。为此目的，在传输线的终端与负载 $Z_{2}$ 之间插入一段 $l = \frac{\lambda}{4}$ 的无损耗线（见图18-13）。根据式(18-11)，可以求得这段长度为 $\frac{\lambda}{4}$ 的无损耗线的输入阻抗 $Z_{\mathrm{i}}$ 为（注意其终端负载为 $Z_{2}$）

![](../../raw/pages_0481-0512/images/page_492_image_7.jpg)

<details>
<summary>text_image</summary>

Z_{c1} → Z_i → Z_2
λ/4
</details>

图 18-13 无损耗线作为阻抗变换器

$$
Z _ {\mathrm{i}} = Z _ {\mathrm{c}} \frac {Z _ {2} + \mathrm{j} Z _ {\mathrm{c}} \tan \left(\frac {2 \pi}{\lambda} \frac {\lambda}{4}\right)}{\mathrm{j} Z _ {2} \tan \left(\frac {2 \pi}{\lambda} \frac {\lambda}{4}\right) + Z _ {\mathrm{c}}} \tag {18-27}
$$

式中 $Z_{\mathrm{c}}$ 为无损耗线的特性阻抗。因为 $\tan \left(\frac{\pi}{2}\right) = \infty$ ，所以上式成为 $Z_{\mathrm{i}} = \frac{Z_{\mathrm{c}}^{2}}{Z_{2}}$ 。可见，为了达到匹配的目的，应使 $Z_{\mathrm{i}} = Z_{\mathrm{c1}}$ 。于是求得此 $\frac{\lambda}{4}$ 无损耗线的特性阻抗应为

$$
Z _ {\mathrm{c}} = \sqrt {Z _ {\mathrm{c1}} Z _ {2}}
$$

此外，在超高频技术中，用固体介质做成支持传输线的绝缘子，其介质损耗往往会太大，以致失去绝缘的作用。因而有时采用所谓“金属绝缘子”，也就是一段长度为 $\frac{\lambda}{4}$ 的短路传输线作为支架。由于这种短路传输线的输入阻抗非常大（在理想情况等于无限大），因此其损耗小于介质绝缘子中的损耗。

当无损耗线的终端所接负载  $Z_{2}=\pm jX_{2}$  为纯电抗时，沿线也将出现电压和电流驻波。这不难解释如下:由于电抗可以用一段适当长的开路或短路无损耗线代替，因此，沿终端接有电抗负载的无损耗线的电压和电流的分布情况，与开路或短路的无损耗线上的分布将没有什么本质上的差别。显然，终端接有电抗负载时，在终端处将既不是电流或电压的波腹，也不是电流或电压的波节（见图 18-14）。

1

---

470

第十八章 均匀传输线

![](../../raw/pages_0481-0512/images/page_493_image_3.jpg)

<details>
<summary>text_image</summary>

u
i
x
O
u,i
</details>

图 18-14 负载为纯电抗的无损耗线的电压和电流分布

不论在哪种情况下,当出现驻波时,在任何瞬间波节处的电压或电流始终为零。所以在这些波节所在处功率也恒等于零。这样,在相邻电压和电流波节之间能量(线上电感的磁场能量和线间电容的电场能量)被封闭在 $\frac{\lambda}{4}$ 的区域内,不能越出波节而彼此交换。因此,在传输线上出现驻波,将意味着没有有功功率被传输到终端负载。一般说来,只有电压和电流的行波才能传输有功功率。

例 18-3 现用特性阻抗为  $75 \Omega$  终端短路的无损耗线来实现工作频率 f=600 MHz 下  $0.7589 \mu H$  的电感，试求其长度 l。如果改用终端开路的同一线实现，则长度应为多少？

解 根据终端短路时输入阻抗公式,有

$$
Z _ {\mathrm{i}} = \mathrm{j} Z _ {\mathrm{c}} \tan \left(\frac {2 \pi}{\lambda} l\right)
$$

现有 $Z_{\mathrm{e}} = 75\Omega ,\lambda = \frac{3\times 10^{8}}{600\times 10^{6}}\mathrm{m} = 0.5\mathrm{m}$ ，则

$$
Z _ {\mathrm{i}} = \mathrm{j} X _ {L} = \mathrm{j} 2 \pi \times 6 0 0 \times 1 0 ^ {6} \times 0. 7 5 8 9 \times 1 0 ^ {- 6} \Omega = \mathrm{j} 2 8 6 1 \Omega
$$

故有  $\tan\left(\frac{2\pi}{\lambda}l\right)=\frac{2861}{75}=38.146$  , 解得  $\frac{2\pi}{0.5}l=1.5446, l=0.123\ m$ 。

如果使用终端开路的同一无损耗线, 参阅图 8-10 和图 18-12 可知, 应为  $l' = 0.123 + \frac{\lambda}{4} = 0.248 \, m$ 。

例 18-4 现有一长度为 0.0625 m、终端开路且  $Z_{c}=50\Omega$  的无损耗线，已知其工作频率为 600 MHz，试求其输入阻抗，它相当于什么元件？

解 输入阻抗

$$
Z _ {\mathrm{i}} = - \mathrm{j} Z _ {\mathrm{c}} \cot \left(\frac {2 \pi}{\lambda} l\right)
$$

现 $Z_{\mathrm{e}} = 50\Omega, \lambda = 0.5\mathrm{m}, l = 0.0625\mathrm{m}$，代入后可得 $Z_{\mathrm{i}} = -\mathrm{j}50\Omega$，故为容抗。相当的电容值为

---

§ 18-6 无损耗线方程的通解

471

$$
C = \frac {1}{\omega \times 5 0} = 5. 3 0 5 \mathrm{pF}
$$

例 18-5 架空无损耗线的特性阻抗  $Z_{c}=100\ \Omega$ ，线长  $l=60\ m$ ，工作频率  $f=10^{6}\ Hz$ 。今欲使始端的输入阻抗为零，试问终端应接怎样的负载？

解 根据输入阻抗的公式和题意,有

$$
Z _ {\mathrm{i}} = Z _ {\mathrm{c}} \frac {Z _ {2} + \mathrm{j} Z _ {\mathrm{c}} \tan (\beta l)}{Z _ {\mathrm{c}} + \mathrm{j} Z _ {2} \tan (\beta l)} = 0
$$

从而得

$$
Z _ {2} + \mathrm{j} Z _ {\mathrm{c}} \tan (\beta l) = 0
$$

其中  $\beta=\frac{\omega}{c}$ ，而 c 为真空中的光速，故

$$
\begin{array}{l} Z _ {2} = - \mathrm{j} Z _ {\mathrm{c}} \tan (\beta l) = - \mathrm{j} 1 0 0 \tan \left(\frac {2 \pi \times 1 0 ^ {6}}{3 \times 1 0 ^ {8}} \times 6 0\right) \Omega \\ = - \mathrm{j} 3 0 7. 7 \Omega \\ \end{array}
$$

在终端应接容抗值为  $308 \Omega$  的负载。

例 18-6 把两段无损耗传输线连接起来,如图 18-15 所示。已知它们的特性阻抗分别为  $Z_{c1}=60\ \Omega, Z_{c2}=100\ \Omega$ 。为了使这两段线上都不产生反射,试求应接的负载  $Z_{1}$  和  $Z_{2}$ 。

解 由图18-15可以看出,要求在第二段线上不产生反射,必须满足 $Z_{2} = Z_{\mathrm{c2}} = 100 \Omega$。这样在 $2 - 2'$ 处第二段线的输入阻抗 $Z_{\mathrm{i2}} = Z_{\mathrm{c2}} = 100 \Omega$。

为了使得在第一段线上没有反射,必须使该线的特性阻抗为

$$
Z _ {\mathrm{c1}} = \frac {Z _ {1} Z _ {\mathrm{c2}}}{Z _ {1} + Z _ {\mathrm{c2}}} = \frac {1 0 0 Z _ {1}}{Z _ {1} + 1 0 0}
$$

或

$$
60 = \frac{100Z_1}{Z_1 + 100}
$$

所以

$$
Z _ {1} = 1 5 0 \Omega
$$

![](../../raw/pages_0481-0512/images/page_494_image_19.jpg)

<details>
<summary>text_image</summary>

1
Zc1
2
Z1
Zc2
Z2
1'
2'
</details>

图18-15 例18-6图

## §18-6 无损耗线方程的通解

在前面各节中讨论了在正弦稳态下均匀传输线的一些特点,本节和下一节介绍均匀传输线的时域分析,并简要地讨论其中发生的过渡过程。这种过渡过程是一系列的波过程,所以与集总电路的过渡过程有所不同。

在 §18-2 中导出了均匀传输线的偏微分方程式(18-1)

1

---

472

第十八章 均匀传输线

$$
\left. \begin{array}{l} - \frac {\partial u}{\partial x} = R _ {0} i + L _ {0} \frac {\partial i}{\partial t} \\ - \frac {\partial i}{\partial x} = G _ {0} u + C _ {0} \frac {\partial u}{\partial t} \end{array} \right\},
$$

式中  $R_{0}$ 、 $L_{0}$ 、 $C_{0}$  和  $G_{0}$  是传输线的原参数，x 是从始端到讨论点的距离。

为简化起见,忽略传输线的损耗,即认为  $R_{0}=0$  和  $G_{0}=0$ ,则上述方程成为

$$
\begin{array}{l} \left. - \frac {\partial u}{\partial x} = L _ {0} \frac {\partial i}{\partial t} \right\} \tag {18-28} \\ \left. - \frac {\partial i}{\partial x} = C _ {0} \frac {\partial u}{\partial t} \right] \\ \end{array}
$$

由于讨论的是均匀传输线,因此  $L_{0}$  和  $C_{0}$  为常数且与 x 无关。上述偏微分方程的通解具有下列形式:

$$
\left. \begin{array}{l} u (x, t) = f _ {1} (x - v t) + f _ {2} (x + v t) = u ^ {+} + u ^ {-} \\ i (x, t) = \sqrt {\frac {C _ {0}}{L _ {0}}} [ f _ {1} (x - v t) - f _ {2} (x + v t) ] = i ^ {+} - i ^ {-} \end{array} \right\} \tag {18-29}
$$

式中  $v=\frac{1}{\sqrt{L_{0}C_{0}}}$  称为波的速度, 简称波速 (在数值上恰好等于正弦稳态下的相速  $v_{\varphi}$ ); 而函数  $f_{1}$  和  $f_{2}$  均为待定, 要根据具体的边界条件和初始条件确定。此通解的正确性, 可以把它们代入方程 (18-28) 加以验证。

为了理解通解的每一项表示的意义,首先对式(18-29)中的电压分量 $u^{+}$ 进行讨论。设在 $t=t_{0}$ 时,电压分量

$$
u ^ {+} (x, t _ {0}) = f _ {1} (x - v t _ {0})
$$

设此时电压沿线的分布如图18-16中实线所示。在经过时间 $\Delta t$ 后，此电压分量 $u^{+}$ 将为 $u^{+}(x,t_{0}+\Delta t)=f_{1}(x-v\Delta t-vt_{0})=f_{1}(x-\Delta x-vt_{0})$ ，式中 $\Delta x=v\Delta t$ 。

![](../../raw/pages_0481-0512/images/page_495_image_13.jpg)

<details>
<summary>text_image</summary>

u
u⁺(x,t₀) u⁺(x,t₀+Δt)
O
v
x
Δx
</details>

图 18-16 电压入射波沿线的分布

比较上两式可以看出， $u^{+}(x,t_{0}+\Delta t)$  和  $u^{+}(x,t_{0})$  沿线的分布规律是相同的，只不过前者比后者向 x 增加的方向移动了一个距离  $\Delta x=v\Delta t$ 。所以  $u^{+}(x,t)$  是向前（即从始端向终端）运动的行波分量，也即入射波，其波速显然就是  $v=\frac{dx}{dt}=\frac{1}{\sqrt{L_{0}C_{0}}}$ 。为了便于描述波的传播过程，引进“波前”的概念。对应于离始端为  $x_{f}$  的点，如果当  $x>x_{f}$  时， $u^{\ddagger}=0$ ，而  $x=x_{f}$  时， $u^{+}\neq0$ ，则称该点为入射波的波前。

同理,用相同的方法分析电压分量  $u^{-}$ , 不难看出它是一个以相同波速 v 向 x 减少的方向运动的行波, 也即反射波。

从式(18-29)可以得出沿线任一点电压分量 $u^{+}(u^{-})$ 和电流分量 $i^{+}(i^{-})$ 的比值为

---

§ 18-6 无损耗线方程的通解

473

$$
\frac {u ^ {+}}{i ^ {+}} = \frac {u ^ {-}}{i ^ {-}} = \sqrt {\frac {L _ {0}}{C _ {0}}} = Z _ {\mathrm{c}}
$$

$Z_{c}$  就是无损耗线的特性阻抗或波阻抗。因此， $u^{+}$ 和  $i^{+}$ 都是从始端向终端传播的入射波；而  $u^{-}$ 和  $i^{-}$ 都是向相反方向传播的反射波。这样，在任何瞬间，沿线的电压和电流都可以看作是入射波和反射波的叠加。

为了形象地阐明电压波或电流波沿线传播的过程，假定研究的无损耗线原来没有充电，且其终端在无限远处（半无限长线）。设在 $t = 0$ 时，将电压为 $U_{0}$ 的直流电压源接到该线的始端。由于反射波是在终端产生的，而现在终端在无限远处，因此在有限的时间内，传输线上不会出现反射波，所以只要研究入射波就可以了。这时，电压波将沿线由始端向终端行进，使传输线充电到 $U_{0}$ 。设在某一瞬间波前传播到 $\mathrm{m - n}$ 处（见图18-17），于是在 $\mathrm{m - n}$ 处的左边沿线各处线间电压为 $U_{0}$，同时来线（上方导线）带正电荷，回线（下方导线）带负电荷（显然，每单位长度所带电荷为 $q_{0} = C_{0}U_{0}$），而在 $\mathrm{m - n}$ 处的右边，由于电压波尚未到达，各处线间电压均为零，来、回线上也就没有电荷。

![](../../raw/pages_0481-0512/images/page_496_image_6.jpg)

图18-17 波沿线的传播

在时间 dt 内, 电压波向前移动了距离 dx = v dt。与此同时在线段 dx 中获得的电荷  $dq = q_{0} dx = C_{0} U_{0} dx$ 。此充电电荷将通过 m-n 左边的所有截面, 于是从电源到 m-n 的全线上就产生了充电电流

$$
I _ {0} = \frac {\mathrm{d} q}{\mathrm{d} t} = q _ {0} \frac {\mathrm{d} x}{\mathrm{d} t} = C _ {0} U _ {0} \frac {\mathrm{d} x}{\mathrm{d} t} = C _ {0} U _ {0} v = \frac {U _ {0}}{Z _ {\mathrm{c}}}
$$

入射电流波伴随着入射电压波以同样速度向终端传播。

电源供给的功率为  $U_{0}I_{0}$ ，而入射波在 dt 时间内经过线段 dx 建立的电场和磁场储存的能量分别为

$$
\mathrm{d} W _ {c} = \frac {1}{2} C _ {0} U _ {0} ^ {2} \mathrm{d} x, \quad \mathrm{d} W _ {L} = \frac {1}{2} L _ {0} I _ {0} ^ {2} \mathrm{d} x
$$

由于 $\frac{U_{0}}{I_{0}}=Z_{c}=\sqrt{\frac{L_{0}}{C_{0}}}$ ，所以 $dW_{c}=dW_{L}$ ，在线段dx内储存的总能量为

$$
\mathrm{d} W = \mathrm{d} W _ {c} + \mathrm{d} W _ {L} = C _ {0} U _ {0} ^ {2} \mathrm{d} x \tag {18-30}
$$

---

474

第十八章 均匀传输线

此能量是在 dt 时间内建立起来的,所以传输线吸收的功率为

$$
p = \frac {\mathrm{d} W}{\mathrm{d} t} = C _ {0} U _ {0} ^ {2} \frac {\mathrm{d} x}{\mathrm{d} t} = C _ {0} U _ {0} ^ {2} v = \frac {U _ {0} ^ {2}}{Z _ {\mathrm{o}}} = U _ {0} I _ {0}
$$

此功率恰好就是始端电源供给的功率。

在无反射情况下传输线上的电压、电流行波可以解析形式表示。设始端电压为 $u(0,t)=U_{0}\varepsilon(t)$ ，式中 $\varepsilon(t)$ 为单位阶跃函数，线上任一点的电压、电流波为

$$
u (x, t) = U _ {0} \varepsilon \left(t - \frac {x}{v}\right)
$$

$$
\frac {U _ {0}}{i (x , t)} = \frac {\varepsilon}{\sqrt {\frac {L _ {0}}{C _ {0}}}} \left(t - \frac {x}{v}\right)
$$

图 18-18 示出这些波形。

![](../../raw/pages_0481-0512/images/page_497_chart_10.jpg)

<details>
<summary>line</summary>

| Time (t) | Value (u(0,t)) |
| --- | --- |
| \(0\) | \(U_{0}\) |
| \(t_{1}\) | \(U_{0}\) |
</details>

(a)

![](../../raw/pages_0481-0512/images/page_497_image_12.jpg)

<details>
<summary>text_image</summary>

u(x,t₁)
U₀
u
i
U₀
|Zc|
O
x₁(=vt₁)
x
v
</details>

(b)

图 18-18 半无限长线的电压和电流行波

如果始端的激励电压为任意波形  $u_{s}(t)\varepsilon(t)$ ，如图 18-19(a) 所示，可得到线上任一点 x 处在 t 时刻的电压为

$$
u (x, t) = u _ {\mathrm{S}} \left(t - \frac {x}{v}\right) \varepsilon \left(t - \frac {x}{v}\right)
$$

如图 18-19(b) 所示。注意电压波以  $u_{\mathrm{s}}(0)$  为波前向 x 方向行进，图 18-19(b) 示出了  $t_{1}$  时刻 ( $t_{1}>t_{2}$ ) 沿线的电压分布，可注意到图 18-19(a)(b) 中两波形的相似关系。

![](../../raw/pages_0481-0512/images/page_497_chart_18.jpg)

<details>
<summary>line</summary>

| Time (t) | Response \((u_S(t)\epsilon(t))\) |
| --- | --- |
| 0 | u_S(0) |
| t_2 | 0 |
</details>

(a)

![](../../raw/pages_0481-0512/images/page_497_chart_20.jpg)

<details>
<summary>contour</summary>

| Variable | Value |
| --- | --- |
| Peak (u) | v |
| Lower bound (u_s) | 0 |
| X-axis range | 0 ~ x1 |
| X-axis value | x_1 = vt_1 |
| X-axis range | 0 ~ x |
</details>

(b)

图 18-19 始端激励为任意波时波过程

---

§ 18-7 无损耗线的波过程

475

## §18-7 无损耗线的波过程

上节中讨论了不存在反射时无损耗线上的波过程。当传输线存在终端且不匹配的情况下，在终端将引起波的反射，因此，传输线上除了入射波以外还将存在反射波。本节讨论无损耗线在终端开路和短路两种情况下波的反射过程。

首先研究终端开路的无损耗线接通直流电压 $U_{0}$ 的波过程。在入射波未到达终端 $0 < t < \frac{l}{v}$ 的时间间隔内，反射尚未产生，因此线上的波过程和上节所述相同。在 $t = \frac{l}{v}$ 时波到达终端，由于终端开路，这一边界条件要求电流反射波大小为 $I_{0}$，因为只有电流的这种全反射才能使终端电流为零（$i = i^{+} - i^{-}$）。反射波所到之处电流变为零。由于 $u^{-} = Z_{\mathrm{e}}i^{-} = U_{0}$，而 $u^{+} = U_{0}$，因此，电压的反射波所到之处使线间电压成为 $2U_{0}$，如图18-20(a)(b)所示。这一过程发生在 $\frac{l}{v} \leqslant t < \frac{2l}{v}$ 之间。当反射波到达始端的前一瞬间时，全线电

![](../../raw/pages_0481-0512/images/page_498_image_6.jpg)

(d)

图 18-20 电压波和电流波在开路线上的多次入射和反射

---

476

第十八章 均匀传输线

流为零，电压为 $2U_{0}$ 。当反射波到达始端时，由于始端的边界条件要求电压为 $U_{0}$，因此在始端也将产生反射，反射波（也即是第二次入射波）将为 $-U_{0}$ 以满足始端的边界条件，这也决定了第二次入射电流波为 $-I_{0}$。故 $\frac{2l}{v} \leqslant t < \frac{3l}{v}$ 的时间间隔内，波所到之处将使电压为 $U_{0}$ 而电流为 $-I_{0}$，如图18-20(c)所示。在 $t = \frac{3l}{v}$ 第二次入射波到达终端时，终端的边界条件要求第二次反射波为 $-I_{0}$，使 $i^{+} - i^{-} = 0$，第二次反射电压为 $-U_{0}$。故在 $\frac{3l}{v} \leqslant t < \frac{4l}{v}$ 时间间隔内，波所到之处将使线上电压和电流均为零，如图18-20(d)所示。当 $t = \frac{4l}{v}$ 时，第二次反射波到达始端，全线电压和电流均为零，完成接通过程的一次循环，即恢复到开始接通的状态。以后的过程将周期性地重复出现。此周期等于波行进4倍线长所需的时间，即 $T = \frac{4l}{v} = 4l\sqrt{L_{0}C_{0}}$。

终端短路的无损耗线与直流电压的接通过程与上述开路线相仿。当第一次入射波到达终端时将产生电压的全反射，第一次电压反射波为 $-U_{0}$ 而电流反射波为 $-I_{0}$，将使线上电流增加为 $2I_{0}$，从图18-21(a)(b)可以看出，经 $\frac{2l}{v}$ 时间，电压就完成一次周期重复而电流将增至 $2I_{0}$ 。之后每次由始端产生的入射波使沿线电压变为 $U_{0}$，从终端产生的反射波使电压为零，所以，电压在零和 $U_{0}$ 之间变动。对电流来说，在始端产生的入射波和终端产生的反射波，总是使得沿线电流增加一个 $I_{0}$ 。因此，线上电流最后将增加到无限大。

![](../../raw/pages_0481-0512/images/page_499_image_5.jpg)

图 18-21 电压波和电流波在短路线上的多次入射和反射

---

习题

477

如果终端接以非匹配的电阻负载 $R_{\mathrm{L}}$，则视此电阻 $R_{\mathrm{L}}$ 与 $Z_{\mathrm{c}}$ 的大小关系将有不同的反射。如果 $R_{\mathrm{L}}>Z_{\mathrm{c}}$，则反射使电流减小、电压增加；如果 $R_{\mathrm{L}}<Z_{\mathrm{c}}$，则反射将使电流增加、电压减少。两种情况下，经过多次反射以后沿线电压与电流趋近恒定。如果终端的负载不是纯电阻而是电阻与电感或电容的组合，则由于终端将出现集总元件的过渡过程，反射的方式也将随时间而变。对这类问题不再深入讨论。

前面介绍的是无损耗线的时域分析。如果需要计及传输线的 $R_{0}$ 和 $G_{0}$，对有损耗线进行时域分析则要困难得多。

近年来由于超大规模集成电路的发展，并为提高数字电子计算机的运算速度，使用了更高的工作频率和变化更快的短脉冲，信号经过集成电路芯片之间的相互连接导线（简称互连）时，会产生延迟、畸变和交叉干扰等现象。对这种互连的时域分析需要用分布参数电路或传输线的观点处理。同时，这类传输线的损耗不能忽略，加上互连的数目很多，它们之间还有互感耦合，这些使得这类问题的分析变得更为复杂。

![](../../raw/pages_0481-0512/images/page_500_image_5.jpg)

## 思考题

18-1 均匀传输线各处电流不同的原因什么？均匀传输线各处电压不同的原因是什么？
18-2 均匀传输线上的电压和电流为什么遵循波动规律？
18-3 在均匀传输线上产生驻波的条件是什么？
18-4 对长度不等的导线,在什么条件下,采用均匀传输线模型?如采用集总参数模型,对信号有什么要求?
18-5 对于直流输电工程中的传输线,分析稳定运行应采用什么模型?而发生暂态过程时,应采用什么模型?
18-6 在集成电路中各器件之间连接的导线,应采用什么电路模型?

![](../../raw/pages_0481-0512/images/page_500_image_14.jpg)

## 习题

18-1 一对架空传输线的原参数是 $L_{0} = 2.89 \times 10^{-3} \mathrm{H / km}, C_{0} = 3.85 \times 10^{-9} \mathrm{F / km}, R_{0} = 0.3 \Omega / \mathrm{km}, G_{0} = 0$ 。试求当工作频率为 $50 \mathrm{~Hz}$ 时的特性阻抗 $Z_{\mathrm{c}}$ 、传播常数 $\gamma$ 、相位速度 $v_{\varphi}$ 和波长 $\lambda$ 。如果频率为 $10^{4} \mathrm{~Hz}$，重求上述各参数。
18-2 一同轴电缆的原参数为: $R_{0}=7\ \Omega/\mathrm{km}, L_{0}=0.3\ \mathrm{mH/km}, C_{0}=0.2\ \mu\mathrm{F/km}, G_{0}=0.5\times10^{-6}\ \mathrm{S/km}$。试计算当工作频率为 $800\ \mathrm{Hz}$ 时此电缆的特性阻抗 $Z_{c}$、传播常数 $\gamma$、相位速度 $v_{\varphi}$ 和波长 $\lambda$。
18-3 传输线的长度 $l = 70.8 \mathrm{~km}$, 其中 $R_{0} = 1 \Omega / \mathrm{km}, \omega C_{0} = 4 \times 10^{-4} \mathrm{~S} / \mathrm{km}$, 而 $G_{0} = 0$, $L_{0} = 0$。在线的终端所接阻抗 $Z_{2} = Z_{\mathrm{c}}$。终端的电压 $U_{2} = 3 \mathrm{~V}$。试求始端的电压 $U_{1}$ 和电

1. 用 $\mathrm{H}_{2}$ 气体中加入一个液体，使气体浓度从 $\mathrm{H}_{2}$ 气体中的 $\mathrm{H}_{2}$ 气体的体积逐渐减小。

---

478

第十八章 均匀传输线

流 $I_{1}$ 。

18-4 一高压输电线长 $300 \mathrm{~km}$, 线路原参数 $R_{0} = 0.06 \Omega / \mathrm{km}, L_{0} = 1.40 \times 10^{-3} \mathrm{H} / \mathrm{km}, G_{0} = 3.75 \times 10^{-8} \mathrm{~S} / \mathrm{km}, C_{0} = 9.0 \times 10^{-9} \mathrm{~F} / \mathrm{km}$ 。电源的频率为 $50 \mathrm{~Hz}$ 。终端为一电阻负载, 终端的电压为 $220 \mathrm{kV}$, 电流为 $455 \mathrm{~A}$ 。试求始端的电压 $\dot{U}_{1}$ 和电流 $\dot{I}_{1}$ 。

18-5 两段特性阻抗分别为 $Z_{\mathrm{c1}}$ 和 $Z_{\mathrm{c2}}$ 的无损耗线连接的传输线如题18-5图所示。已知终端所接负载为 $Z_{2} = (50 + \mathrm{j}50)\Omega$ 。设 $Z_{\mathrm{c1}} = 75\Omega, Z_{\mathrm{c2}} = 50\Omega$ 。两段线的长度都为 $0.2\lambda (\lambda$ 为线的工作波长)，试求 $1 - 1'$ 端的输入阻抗。

![](../../raw/pages_0481-0512/images/page_501_image_6.jpg)

<details>
<summary>text_image</summary>

1
Zc1
2
Zc2
2'
1'
0.2λ
0.2λ
Z2
</details>

题18-5图

18-6 特性阻抗为  $50 \Omega$  的同轴线，其中介质为空气，终端连接的负载  $Z_{2} = (50 + j100) \Omega$ 。试求终端处的反射系数，距负载  $2.5 \, cm$  处的输入阻抗和反射系数。已知线的工作波长为  $10 \, cm$ 。
18-7 试证明无损耗线沿线电压和电流的分布及输入导纳可以表示为下面的形式:

$$
\dot {U} = \dot {U} _ {2} \left[ \cos (\beta x) + \mathrm{j} \frac {Y _ {2}}{Y _ {\mathrm{c}}} \sin (\beta x) \right]
$$

$$
\dot {I} = \dot {I} _ {2} \left[ \cos (\beta x) + \mathrm{j} \frac {Y _ {\mathrm{c}}}{Y _ {2}} \sin (\beta x) \right]
$$

$$
Y _ {\mathrm{i}} = Y _ {\mathrm{c}} \frac {Y _ {2} + \mathrm{j} Y _ {\mathrm{c}} \tan (\beta x)}{Y _ {\mathrm{c}} + \mathrm{j} Y _ {2} \tan (\beta x)}
$$

![](../../raw/pages_0481-0512/images/page_501_image_14.jpg)

第十八章部分习题答案

其中  $Y_{c}=\frac{1}{Z_{c}}, Y_{2}=\frac{1}{Z_{2}}, Z_{2}$  为负载阻抗。
