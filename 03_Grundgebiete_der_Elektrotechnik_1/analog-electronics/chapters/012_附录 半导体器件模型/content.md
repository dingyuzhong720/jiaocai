# 附录 半导体器件模型

原始 PDF 第 525–535 页。

## 附录

## 半导体器件模型

在电子电路的分析计算中,通常将半导体器件用其等效模型取代。在本教材中,第1章介绍的二极管等效模型,第2章介绍的晶体管和场效应管h参数等效模型,第3章介绍的集成运放等效模型,第4章介绍的晶体管和场效应管高频等效模型,共同的特点是用于特定条件下的近似分析,因而尽量简化。而在利用计算机辅助分析和设计(Computer Aided Design,简称CAD)电子电路时,构造电子器件等效模型的出发点是如何更正确和准确地反映其各方面的特性,从而使分析结果更精确,因此所采用的模型要比前面所介绍的复杂得多,它们是在器件物理原理基础上构造而成的。为描述半导体器件的复杂特性,需用较多的模型参数;例如,晶体管和场效应管的模型参数就有40个之多,即使比较简化的EM2模型也有十几个参数。

本节对 SPICE 中半导体器件模型加以简单介绍 $^{①}$ ，并在此基础上介绍 Multisim 中模型参数与之相同和不同之处。

## 一、二极管的模型及其参数

二极管的模型如图1所示。图中 $R_{\mathrm{s}}$ 为二极管的材料电阻，称为欧姆电阻； $C_\mathrm{D}$ 为二极管等效电容； $I_{\mathrm{D}}$ 为二极管的电流。设二极管端电压为 $U_{\mathrm{D}}$ ，则 $I_{\mathrm{D}}$ 和 $U_{\mathrm{D}}$ 的关系为

$$
I _ {\mathrm{D}} = f (U _ {\mathrm{D}}) = \left\{ \begin{array}{l l} (\mathrm{e} ^ {q U _ {\mathrm{D}} / n k T} - 1) + U _ {\mathrm{D}} G _ {\min} & - 5 \frac {n k T}{q} \leqslant U _ {\mathrm{D}} \\ - I _ {\mathrm{S}} + U _ {\mathrm{D}} G _ {\min} & - B U <   U _ {\mathrm{D}} <   - 5 \frac {n k T}{q} \\ - I _ {\mathrm{BU}} & U _ {\mathrm{D}} = - B U \\ - I _ {\mathrm{S}} \Big [ \mathrm{e} ^ {- q (B U + U _ {\mathrm{D}}) / k T} - 1 + \frac {q B U}{k T} \Big ] & U _ {\mathrm{D}} <   - B U \end{array} \right.
$$

其中  $I_{s}$  ——反向饱和电流(A);

q——电子电荷 $(1.602 \times 10^{-19}C)$ ;

k——玻尔兹曼常数 $(1.38 \times 10^{-23} \text{J/K})$ ;

T——绝对温度(K);

N——发射系数(硅管1.2\~2.0);

BU——反向击穿电压(V);

$I_{BU}$ ——反向击穿时的电流(A);

$G_{min}$ ——是 SPICE 程序中非线性支路的一个给定小电导，隐含值为  $10^{-12}S$ ，一般情况下不影响二极管的特性。

![](../../raw/pages_0513-0544/images/page_524_image_15.jpg)

<details>
<summary>text_image</summary>

I_D
R_s
C_D
U_D
+
-
I_D
</details>

图 1 二极管的模型

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 附录中所涉及内容的详细分析可参阅《电子电路的计算机辅助分析与设计方法》(汪蕙、王志华编著, 清华大学出版社 1996 年出版) 第 3 章。为便于参阅, 本节中所用符号与上述参考书中基本相同。</span></small>

---

附录 半导体器件模型

503

二极管的等效电容  $C_{D}$  为结电容  $C_{j}$ ，它是势垒电容  $C_{b}$  和扩散电容  $C_{d}$  之和，即

$$
C _ {\mathrm{j}} = C _ {\mathrm{b}} + C _ {\mathrm{d}}
$$

其中 $C_{\mathrm{d}} = \tau_{\mathrm{D}}\frac{\mathrm{d}I_{\mathrm{D}}}{\mathrm{d}U_{\mathrm{D}}}$ （ $\tau_{\mathrm{D}}$ 为少数载流子的渡越时间）

$$
C _ {\mathrm{b}} = \left\{ \begin{array}{l l} C _ {\mathrm{j0}} \left(1 - \frac {U _ {\mathrm{D}}}{\varphi_ {\mathrm{D}}}\right) ^ {- m} & U _ {\mathrm{D}} <   F C \times \varphi_ {\mathrm{D}} \\ \frac {C _ {\mathrm{j0}}}{(1 - F C) ^ {1 + m}} \Big [ 1 - F C (1 + m) + \frac {m U _ {\mathrm{D}}}{\varphi_ {\mathrm{D}}} \Big ] & U _ {\mathrm{D}} \geqslant F C \times \varphi_ {\mathrm{D}} \end{array} \right.
$$

其中  $C_{j0}$  ——零偏置时 PN 结的电容；

$\varphi_{D}$ ——PN 结自建电势,二极管的典型值为  $0.7 \sim 0.8$  V;

m——电容梯度因子,典型值为0.3\~0.5;

FC——正偏耗尽电容公式的系数,典型值为0.5。

综上所述,二极管的模型参数共14个,如表1所示。

表 1 二极管的模型参数

| 序号 | 符号 | SPICE关键字 | 名称 | 隐含值 | 单位 | 举例 |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | IS | IS | 反向饱和电流 | 10-14 | A | 2x10-15A |
| 2 | Rs | RS | 欧姆电阻 | 0 | Ω | 10Ω |
| 3 | n | N | 发射系数 | 1 |  | 1.2 |
| 4 | τD | TT | 渡越时间 | 0 | s | 1 ns |
| 5 | Cjo | CJO | 零偏置电容 | 0 | F | 2 pF |
| 6 | φD | VJ | 结电压 | 1 | V | 0.6 V |
| 7 | m | M | 电容梯度因子 | 0.5 |  | 0.33 |
| 8 | Eg | EG | 禁带宽度 | 1.11 | eV | 1.11 eV(硅)0.69 eV(锑)0.67 eV(锗) |
| 9 | pt | XTI | 饱和电流温度系数 | 3.0 |  | 3.0 |
| 10 | FC | FC | 正偏耗尽层电容公式系数 | 0.5 |  | 0.5 |
| 11 | BV | BV | 反向击穿电压 | ∞ | V | 40 V |
| 12 | IBV | IBV | 反向击穿时电流 | 10-3 | A | 10-3A |
| 13 | Kf | KF | 闪烁噪声系数 | 0 |  |  |
| 14 | af | AF | 闪烁噪声指数 | 1 |  |  |

在 Multisim V7 中, 虚拟二极管和实际二极管模型参数均与 SPICE 中的完全相同。

---

504

附录 半导体器件模型

## 二、晶体三极管的模型及其参数

晶体三极管(简称BJT)的模型种类很多,应用最为广泛的是Ebers-Moll模型(简称EM模型)和Gummel-Poon模型(GP模型)。其中EM模型从1954年诞生时的简单非线性直流模型EM1,逐渐改进,已成为包括各种效应的较为完善的通用模型EM3。GP模型与EM3等价,是一种数学推导上更加严格和完整的模型。

晶体管的 EM2 模型如图 2 所示, 它不但反映了晶体管的直流特性, 而且在一定程度上描述了其频域和时域特性。其中  $r_{CC'}$ 、 $r_{EE'}$  和  $r_{BB'}$  分别为集电极、发射极和基极的欧姆电阻,  $C_{DC}$ 、 $C_{DE}$  为两个 PN 结的扩散电容,  $C_{JC}$ 、 $C_{JE}$  为两个 PN 结的势垒电容。 $C_{SUB}$  为衬底电容, 其典型值为 1\~2 pF。

![](../../raw/pages_0513-0544/images/page_526_image_5.jpg)

<details>
<summary>text_image</summary>

B
I_B
R'_BB
C_DC
C_C
B'
C_JC
C_DE
C_JE
C'_C
C
I_C
R_CC'
C'
I_RC / β_R
I_FC / β_F
I_CT
C_SUB
E'
E
I_E
R_EE'
E
</details>

图 2 晶体管的 EM2 模型

电流源的电流为

$$
I _ {\mathrm{CT}} = I _ {\mathrm{FC}} - I _ {\mathrm{RC}} = I _ {\mathrm{S}} \Big [ \exp \bigg (\frac {q U _ {\mathrm {B^{\prime} E^{\prime}}}}{k T} \bigg) - \exp \bigg (\frac {q U _ {\mathrm {B^{\prime} C^{\prime}}}}{k T} \bigg) \Big ]
$$

晶体管三个极的电流为

$$
I _ {\mathrm{E}} = - \frac {I _ {\mathrm{FC}}}{\beta_ {\mathrm{F}}} - I _ {\mathrm{CT}}, \quad I _ {\mathrm{B}} = \frac {I _ {\mathrm{FC}}}{\beta_ {\mathrm{F}}} + \frac {I _ {\mathrm{RC}}}{\beta_ {\mathrm{R}}}, \quad I _ {\mathrm{C}} = I _ {\mathrm{CT}} - \frac {I _ {\mathrm{RC}}}{\beta_ {\mathrm{R}}}
$$

参数  $I_{s}$  ——晶体管的饱和电流；

$\beta_{F}$ ——正向共射电流放大系数；

$\beta_{R}$ ——反向共射电流放大系数。

发射结电容随发射结电压变化的表达式为

$$
C _ {\mathrm{JE}} = \left\{ \begin{array}{l l} C _ {\mathrm{JE0}} \bigg (1 - \frac {U _ {\mathrm {B^{\prime} E^{\prime}}}}{\varphi_ {\mathrm{E}}} \bigg) ^ {- m _ {\mathrm{E}}} & U _ {\mathrm {B^{\prime} E^{\prime}}} <   F C \times \varphi_ {\mathrm{E}} \\ \frac {C _ {\mathrm{JE0}}}{F _ {2}} \bigg (F _ {3} + \frac {m _ {\mathrm{E}} U _ {\mathrm {B^{\prime} E^{\prime}}}}{\varphi_ {\mathrm{E}}} \bigg) & U _ {\mathrm {B^{\prime} E^{\prime}}} \geqslant F C \times \varphi_ {\mathrm{E}} \end{array} \right.
$$

其中  $F_{2}=(1-FC)^{1+m_{E}}, F_{3}=1-FC(1+m_{E})$ 。参数

$C_{JEO}$ —— $U_{B'E'} = 0$ 时发射结电容值；

$\varphi_{E}$ ——发射区-基区内建势垒电位,典型值为0.7\~0.8 V;

$m_{E}$ ——发射区-基区电容梯度因子,典型值为0.333\~0.5;

---

附录 半导体器件模型

505

FC——正偏耗尽电容公式系数。

集电结电容随结电压变化的表达式为

$$
C _ {\mathrm{JC}} = \left\{ \begin{array}{l l} C _ {\mathrm{JC0}} \bigg (1 - \frac {U _ {\mathrm {B^{\prime} C^{\prime}}}}{\varphi_ {\mathrm{C}}} \bigg) ^ {- m _ {\mathrm{C}}} & U _ {\mathrm {B^{\prime} C^{\prime}}} <   F C \times \varphi_ {\mathrm{C}} \\ \frac {C _ {\mathrm{JC0}}}{F _ {2}} \bigg (F _ {3} + \frac {m _ {\mathrm{C}} U _ {\mathrm {B^{\prime} C^{\prime}}}}{\varphi_ {\mathrm{C}}} \bigg) & U _ {\mathrm {B^{\prime} C^{\prime}}} \geqslant F C \times \varphi_ {\mathrm{C}} \end{array} \right.
$$

其中  $F_{2}=(1-FC)^{1+m_{C}}, F_{3}=1-FC(1+m_{C})$ ，参数:

$C_{JCO}$ —— $U_{B'C'} = 0$ 时集电结电容值；

$\varphi_{c}$ ——集电区-基区内建势垒电位，典型值为0.7\~0.8 V；

$m_{c}$ ——集电区-基区电容梯度因子，典型值为0.333～0.5；

FC——正偏耗尽电容公式系数。

扩散电容的表达式为

$$
C _ {\mathrm{DE}} \approx \tau_ {\mathrm{F}} \frac {q I _ {\mathrm{FC}}}{k T}
$$

$$
C _ {\mathrm{DC}} \approx \tau_ {\mathrm{R}} \frac {q I _ {\mathrm{FC}}}{k T}
$$

其中  $\tau_{F}$  为正向渡越时间， $\tau_{R}$  为反向渡越时间。 $\tau_{F}$  可由下面公式求出。

$$
\tau_ {\mathrm{F}} = \frac {1}{2 \pi f _ {\mathrm{T}}} - C _ {\mathrm{JC}} R _ {\mathrm{CC}},
$$

式中 $f_{T}$ 为晶体管的特征频率。

综上所述，EM2共有16个模型参数。在EM2模型基础上，为了进一步反映晶体管基区宽度调制效应、电流和电压对电流放大系数的影响、电流对正向渡越时间的影响、温度对器件参数的影响等，便产生了EM3模型。EM3模型中利用数学公式来描述上述效应，模型参数有40个之多，如表2所示。在SPICE程序中，若模型语句中没有定义EM3模型参数，则程序自动认为模型为EM2模型。

表 2 SPICE 中 BJT 管的模型参数

| 序号 | 符号 | SPICE关键字 | 名称 | 隐含值 | 单位 | 举例 |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | $I_S$ | IS | 饱和电流 | $10^{-16}$ | A | $10^{-15}$ |
| 2 | $\beta_F$ | BF | 正向电流增益 | 100 |  | 80 |
| 3 | $\beta_R$ | BR | 反向电流增益 | 1 |  | 1.5 |
| 4 | $n_F$ | NF | 正向电流发射系数 | 1 |  | 1 |
| 5 | $n_R$ | NR | 反向电流发射系数 | 1 |  | 1 |
| 6 | $c_2$ | ISE($c_2I_S$) | B-E结泄漏饱和电流 | 0 | A |  |
| 7 | $c_4$ | ISC($c_4I_S$) | B-C结泄漏饱和电流 | 0 | A |  |
| 8 | $I_{KF}$ | IKF | 正向β大电流下降点 | ∞ | A | $10^{-2}$ |

---

506

附录 半导体器件模型

续表

| 序号 | 符号 | SPICE关键字 | 名 称 | 隐含值 | 单位 | 举例 |
| --- | --- | --- | --- | --- | --- | --- |
| 9 | IRF | IRF | 反向β大电流下降点 | ∞ | A | 10-13 |
| 10 | nEL | NE | B-E结泄漏发射系数 | 1.5 |  | 2 |
| 11 | ncL | NC | B-C结泄漏发射系数 | 2 |  | 2 |
| 12 | UA | VAF | 正向欧拉电压 | ∞ | V | 200 |
| 13 | UB | VAR | 反向欧拉电压 | ∞ | V | 200 |
| 14 | Rcc' | RC | 集电极电阻 | 0 | Ω | 10 |
| 15 | REE' | RE | 发射极电阻 | 0 | Ω | 1 |
| 16 | RBB' | RB | 基极电阻 | 0 | Ω | 10 |
| 17 | RBM | RBM | 大电流时最小基极欧姆电阻 | RB | Ω | 10 |
| 18 | IRB | IRB | 基极电阻下降到1/2最小值时的电流 | ∞ | A | 0.1 |
| 19 | τF | TF | 理想正向渡越时间 | 0 | ns | 1 |
| 20 | τR | TR | 理想反向渡越时间 | 0 | ns | 10 |
| 21 | XTF | XTF | TF随偏置变化系数 | 0 |  |  |
| 22 | UTF | VTF | TF随UBC变化的电压 | ∞ |  |  |
| 23 | ITF | ITF | TF的大电流参数 | 0 | A |  |
| 24 | PTF | PTF | f=(1/2πτF)时超前相位 | 0 |  |  |
| 25 | CJE0 | CJE | B-E结零偏置耗尽电容 | 0 | pF | 2 |
| 26 | φE | VJE | B-E结内建电势 | 0.75 | V | 0.70 |
| 27 | mE | MJE | B-E结梯度因子 | 0.33 |  | 0.35 |
| 28 | CJCO | CJE | B-C结零偏置耗尽电容 | 0 | pF | 2 |
| 29 | φC | VJC | B-C结内建电势 | 0.75 | V | 0.70 |
| 30 | mC | MJC | B-C结梯度因子 | 0.33 |  | 0.35 |
| 31 | CSUB | CJS | C-衬底结零偏置电容 | 0 | pF | 5 |
| 32 | φS | VJS | 衬底结内建电势 | 0.75 | V | 0.70 |
| 33 | mS | MJS | 衬底结梯度因子 | 0.33 |  | 0.33 |
| 34 | FC | FC | 正偏压耗尽电容公式中的系数 | 0.5 |  |  |
| 35 | XCJC | XCJC | B-C结耗尽电容连接到基极内节点的百分数 | 1 |  |  |
| 36 | XTB | XTB | BETA的温度指数 | 0 |  |  |
| 37 | XTI | XTI | 饱和电流温度指数 | 3 |  |  |

---

附录 半导体器件模型

507

续表

| 序号 | 符号 | SPICE关键字 | 名称 | 隐含值 | 单位 | 举例 |
| --- | --- | --- | --- | --- | --- | --- |
| 38 | $E_{g}$ | EG | IS温度效应中的禁带宽度 | 1.11 | (硅)eV |  |
| 39 | $K_{f}$ | KF | 闪烁噪声系数 | 0 |  |  |
| 40 | $a_{f}$ | AF | 闪烁噪声指数 | 1 |  |  |

此外,若采用改进的 GP 模型,则在 SPICE 程序中应定义。

Multisim 中虚拟晶体管模型采用了改进的 GP 模型, 共有 40 个参数; 实际晶体管模型采用了改进的 GP 模型中的一部分参数, 共 27 个。

## 三、场效应管的模型及其参数

## 1. 结型场效应管的模型及其参数

图3所示为N沟道结型场效应管(简称JFET)的模型。图中$I_{\mathrm{DS}}$ 为非线性电流源， $R_{\mathrm{D}}$ 和 $R_{\mathrm{S}}$ 分别是漏极和源极的欧姆电阻，电容 $C_\mathrm{GD}$ 和 $C_\mathrm{GS}$ 反映两个栅结的电容存储效应，两只二极管 $\mathrm{D}_{\mathrm{D}}$ 和 $\mathrm{D}_{\mathrm{S}}$ 分别表示栅-漏和栅-源两个PN结。

二极管的电流方程为

$$
\begin{array}{l} I _ {\mathrm{GD}} = \left\{ \begin{array}{l l} - I _ {\mathrm{S}} + U _ {\mathrm{GD}} G _ {\min} & U _ {\mathrm{GD}} \leqslant - 5 \frac {k T}{q} \\ I _ {\mathrm{S}} \left[ \exp \left(\frac {q U _ {\mathrm{GD}}}{k T}\right) - 1 \right] + U _ {\mathrm{GD}} G _ {\min} & U _ {\mathrm{GD}} > - 5 \frac {k T}{q} \end{array} \right. \\ I _ {\mathrm{GS}} = \left\{ \begin{array}{l l} I _ {\mathrm{S}} \Big [ \exp \Big (\frac {q U _ {\mathrm{GS}}}{k T} \Big) - 1 \Big ] + U _ {\mathrm{GD}} G _ {\mathrm{min}} & U _ {\mathrm{GS}} > - 5 \frac {k T}{q} \\ - I _ {\mathrm{S}} + U _ {\mathrm{GD}} G _ {\mathrm{min}} & U _ {\mathrm{GS}} \leqslant - 5 \frac {k T}{q} \end{array} \right. \\ \end{array}
$$

![](../../raw/pages_0513-0544/images/page_529_image_11.jpg)

<details>
<summary>chemical</summary>

Electronic circuit diagram of a MOSFET amplifier with diodes, capacitors, and resistors labeled
</details>

图 3 N 沟道结型场效应管的模型

$I_{DS}$ 在正向工作区的计算公式为

$$
I _ {\mathrm{DS}} = \left\{ \begin{array}{l l} 0 & U _ {\mathrm{GS}} - U _ {\mathrm{T0}} \leqslant 0 \\ \beta (U _ {\mathrm{GS}} - U _ {\mathrm{T0}}) ^ {2} (1 + \lambda U _ {\mathrm{DS}}) & 0 <   U _ {\mathrm{GS}} - U _ {\mathrm{T0}} \leqslant U _ {\mathrm{DS}} \\ \beta U _ {\mathrm{DS}} [ 2 (U _ {\mathrm{GS}} - U _ {\mathrm{T0}}) - U _ {\mathrm{DS}} ] (1 + \lambda U _ {\mathrm{DS}}) & 0 <   U _ {\mathrm{DS}} <   U _ {\mathrm{GS}} - U _ {\mathrm{T0}} \end{array} \right.
$$

$I_{DS}$ 在反向工作区的计算公式为

$$
I _ {\mathrm{DS}} = \left\{ \begin{array}{l l} 0 & U _ {\mathrm{GS}} - U _ {\mathrm{T0}} \leqslant 0 \\ \beta (U _ {\mathrm{GS}} - U _ {\mathrm{T0}}) ^ {2} (1 + \lambda U _ {\mathrm{DS}}) & 0 <   U _ {\mathrm{GS}} - U _ {\mathrm{T0}} \leqslant U _ {\mathrm{DS}} \\ \beta U _ {\mathrm{DS}} [ 2 (U _ {\mathrm{GS}} - U _ {\mathrm{T0}}) - U _ {\mathrm{DS}} ] (1 + \lambda U _ {\mathrm{DS}}) & 0 <   U _ {\mathrm{DS}} <   U _ {\mathrm{GS}} - U _ {\mathrm{T0}} \end{array} \right.
$$

其中  $\beta$ ——跨导参数；

$U_{T0}$ ——夹断电压；

$\lambda$ ——沟道长度调制系数。

---

508

附录 半导体器件模型

由于正常工作时  $D_{D}$  和  $D_{S}$  均截止，故可只考虑势垒电容的电荷存储效应。势垒电容的计算公式为

$$
\begin{array}{l} C _ {\mathrm{GS}} = \left\{ \begin{array}{l l} C _ {\mathrm{GS0}} \left(1 - \frac {U _ {\mathrm{GS}}}{\varphi_ {0}}\right) ^ {- \frac {1}{2}} & U _ {\mathrm{GS}} <   F C \times \varphi_ {0} \\ \frac {C _ {\mathrm{GS0}}}{F _ {2}} \left(F _ {3} + \frac {U _ {\mathrm{GS}}}{2 \varphi_ {0}}\right) & U _ {\mathrm{GS}} \geqslant F C \times \varphi_ {0} \end{array} \right. \\ C _ {\mathrm{GD}} = \left\{ \begin{array}{l l} C _ {\mathrm{GD0}} \left(1 - \frac {U _ {\mathrm{GD}}}{\varphi_ {0}}\right) ^ {- \frac {1}{2}} & U _ {\mathrm{GD}} <   F C \times \varphi_ {0} \\ \frac {C _ {\mathrm{GD0}}}{F _ {2}} \left(F _ {3} + \frac {U _ {\mathrm{GD}}}{2 \varphi_ {0}}\right) & U _ {\mathrm{GD}} \geqslant F C \times \varphi_ {0} \end{array} \right. \\ \end{array}
$$

其中  $F_{2}=(1-FC)^{1+m}, F_{3}=1-FC(1+m)$ 。参数:

$C_{GS0}$ ——零偏置 G-S 结电容值；

$C_{GDO}$ ——零偏置 G-D 结电容值；

$\varphi_{0}$  ——栅结内建电势；

m ——电容梯度因子；

FC ——正偏耗尽电容公式系数。

在 SPICE 中, JFET 有 13 个模型参数, 如表 3 所示。

表 3 SPICE 中 JFET 的模型参数

| 序号 | 符号 | SPICE关键字 | 名称 | 隐含值 | 单位 | 举例 |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | $U_{\text{TO}}$ | VTO | 阈值电压(夹断电压) | -2 | V |  |
| 2 | $\beta$ | BETA | 跨导参数 | $10^{-4}$ | A/$V^2$ |  |
| 3 | $\lambda$ | LAMBDA | 沟道长度调制系数 | 0 | $V^{-1}$ |  |
| 4 | $R_{\text{D}}$ | RD | 漏极欧姆电阻 | 0 | Ω | 10Ω |
| 5 | $R_{\text{s}}$ | RS | 源极欧姆电阻 | 0 | Ω | 10Ω |
| 6 | $C_{\text{GS0}}$ | CGS | 零偏G-S结电容 | 0 | F |  |
| 7 | $C_{\text{GD0}}$ | CGD | 零偏G-D结电容 | 0 | F |  |
| 8 | $\varphi_0$ | PB | 栅结内建电势 | 1 | V |  |
| 9 | m | M | 电容梯度因子 | 0.33 |  | 0.35 |
| 10 | $I_{\text{s}}$ | IS | 栅PN结饱和电流 | $10^{-14}$ | A |  |
| 11 | FC | FC | 正偏耗尽电容系数 | 0.5 |  |  |
| 12 | $K_{\text{f}}$ | KF | 闪烁噪声系数 | 0 |  |  |
| 13 | $a_{\text{f}}$ | AF | 闪烁噪声指数 | 0 |  |  |

在 Multisim 中, 虚拟 JFET 模型参数采用了 SPICE3 中的 13 个参数, 其中 12 个参数与 SPICE 中的完全相同, 只有一个参数 B(Doping Tail Parameter, 掺杂尾部参数) 与 SPICE 中的 M

---

附录 半导体器件模型

509

(电容梯度因子)不同;实际JFET模型采用了PSpice中的JFET模型,共有21个参数,除了包含SPICE中JFET模型的13个参数外,其余参数参见表4,参数的关键字第一个字母大写,其余字母均小写。

表 4 Multisim 中增加的模型参数

| 序号 | 符号 | 关键字 | 名称 | 单位 | 隐含值 |
| --- | --- | --- | --- | --- | --- |
| 14 | n | N | 栅PN结发射系数 |  | 1.0 |
| 15 | - | $X_{TI}$ | 饱和电流温度指数 |  | 3.0 |
| 16 | $I_{sscr}$或$I_{ssr}$ | $I_{SR}$ | 栅PN结复合电流参数 | A | 0 |
| 17 | n | $N_R$ | $I_{SR}$的发射系数 |  | 2.0 |
| 18 | - | Alpha | 电离系数 | $V^{-1}$ | 0 |
| 19 | - | Vk | 电离“膝点”电压 | V | 0 |
| 20 | - | Vtotc | 阈值电压温度系数 | V/°C | 0 |
| 21 | - | Betatce | Beta指数温度系数 | %/°C | 0 |

## 2. MOS 管的模型及其参数 $^{①}$

MOS管是个四端器件，除栅极G、漏极D和源极S外，还有衬底B。N沟道MOS管的模型如图4所示。由于绝缘层的隔离作用，从栅极看进去为栅-漏电容 $C_\mathrm{GD}$ 和栅-源电容 $C_\mathrm{GS}$ ；漏-衬、源-衬PN结分别用两只二极管表示，它们的电容效应用$C_\mathrm{BD}$ 和 $C_\mathrm{BS}$ 表示； $I_{\mathrm{DS}}$ 为非线性电流源； $R_{\mathrm{D}}$ 和 $R_{\mathrm{S}}$ 分别是漏极和源极的欧姆电阻。

MOS 管的模型在 SPICE 中分为 4 级 (SPICE3 分为 6 级)，模型级别用变量 LEVEL 指定:

$$
\text {LEVEL} = 1 \quad \text {Shichma - Hodges 模型(缺省模型)}
$$

$$
\mathrm{LEVEL} = 2 \quad \text {基于几何图形的一种二维分析模型}
$$

$$
\mathrm{LEVEL} = 3 \quad \text {半经验短沟道模型}
$$

$$
\mathrm{LEVEL} = 4 \quad \text {适用于亚微米的 BSIM 模型}
$$

![](../../raw/pages_0513-0544/images/page_531_image_12.jpg)

<details>
<summary>chemical</summary>

Electronic circuit diagram of a MOSFET amplifier with labeled components and current directions
</details>

图 4 N 沟道 MOS 管的模型

若不指定 LEVEL, 则 SPICE 采用缺省模型, 即一阶模型。SPICE 中 MOS 管的 1、2、3、6 阶有 41 个模型参数。Multisim 中虚拟 MOS 管模型采用了一阶模型, 共有 28 个参数; 实际晶体管模型采用了三阶模型, 即半经验短沟道模型, 共有 25 个参数, 如表 5 所示, 在序号栏中打“\*”的为一阶模型参数, 打“#”的为三阶模型参数。

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 场效应管模型参数的有关资料来源于姚立真主编的《通用电路模拟技术及软件应用》(北京:电子工业出版社.1994年5月)、http://www.ee.duke.edu/\~hcc/DEVICE/node13.html、Spice3f User Manual 和 Orcad Pspice Reference Manual。</span></small>

---

510

附录 半导体器件模型

表 5 SPICE 中 MOS 管的模型参数

| 序号 | 符号 | SPICE关键字 | 名称 | 隐含值 | 单位 | 举例 |
| --- | --- | --- | --- | --- | --- | --- |
| 1*# | $V_{TO}$ | VTO | 零偏阈值电压 | 1.0 | V | 1.0 |
| 2* | $K_p$ | KP | 跨导参数 | $2\times 10^{-5}$ | A/$V^2$ | $3\times 10^{-5}$ |
| 3* | γ | GAMMA | 体效应阈值参数 | 0.0 | $V^{1/2}$ | 0.35 |
| 4* | $2\Phi_p$ | PHI | 表面电势 | 0.0 | V | 0.65 |
| 5* | λ | LAMBDA | 沟道长度调制系数 | 0 | $V^{-1}$ | 0.02 |
| 6*# | $t_{ox}$ | TOX | 氧化层厚度 | $1\times 10^{-7}$ | m | $1\times 10^{-7}$ |
| 7# | $N_b$ | NSUB | 衬底掺杂浓度 | 0.0 | $/cm^3$ | $1\times 10^{15}$ |
| 8*# | $N_{SS}$ | NSS | 表面态密度 | 0.0 | $/cm^2$ | $1\times 10^{10}$ |
| 9# | $N_{FS}$ | NFS | 快表面态密度 | 0.0 | $/cm^2$ | $1\times 10^{10}$ |
| 10 | $N_{eff}$ | NEFF | 总沟道电荷系数 | 1 |  | 5.0 |
| 11# | $X_J$ | XJ | 结深 | 0.0 | m | $1\times 10^{-6}$ |
| 12*# | $L_d$ | LD | 横向扩散长度 | 0.0 | m | $8\times 10^{-7}$ |
| 13* | $T_{PG}$ | TPG | 栅材料类型 | 1(硅栅) |  | 0(铝栅) |
| 14*# | $μ_o$ | UO | 载流子表面迁移率 | 600 | $cm^2/(V·s)$ | 700 |
| 15 | $U_e$ | UCRIT | 迁移率下降时临界电场 | $1\times 10^4$ | V/cm | $1\times 10^4$ |
| 16 | $U_e$ | UEXP | 迁移率下降时临界电场指数 | 0.0 |  | 0.1 |
| 17 | $U_t$ | UTRA | 迁移率下降时横向电场系数 | 0.0 |  | 0.5 |
| 18# | $v_{max}$ | VMAX | 载流子最大漂移速度 | 0.0 | m/s | $5\times 10^4$ |
| 19# | δ | DELTA | 阈值电压的沟道宽度效应系数 | 0.1 |  | 1.0 |
| 20 | $X_{QC}$ | XQC | 漏端沟道电荷分配系数 | 0.0 |  | 0.4 |
| 21# | η | ETA | 静态反馈系数 | 0.0 |  | 1.0 |
| 22# | θ | THETA | 迁移率调制系数 | 0.0 | $V^{-1}$ | 0.05 |
| 23* | $A_F$ | AF | 闪烁噪声指数 | 1.0 |  | 1.2 |
| 24* | $K_F$ | KF | 闪烁噪声系数 | 0.0 |  | $1\times 10^{-26}$ |
| 25*# | $I_S$ | IS | 衬底结饱和电流 | $1\times 10^{-14}$ | A | $1\times 10^{-15}$ |
| 26* | $J_S$ | JS | 衬底结饱和电流密度 | 0.0 | $A/m^2$ | $1\times 10^{-8}$ |
| 27*# | $Φ_J$ | PB | 衬底结电势 | 0.8 | V | 0.75 |
| 28*# | $C_J$ | CJ | 零偏衬底电容/平方米 | 0.0 | $F/m^2$ | $2\times 10^{-4}$ |
| 29*# | $M_J$ | MJ | 衬底结电容梯度因子 | 0.5 |  | 0.5 |
| 30*# | $C_{JSW}$ | CJSW | 零偏衬底电容/单位周边长度 | 0.0 | F/m | $1\times 10^{-9}$ |
| 31*# | $M_{JSW}$ | MJSW | 衬底周边电容梯度因子 | 0.33 |  | 0.33 |
| 32*# | FC | FC | 正偏耗尽电容系数 | 0.5 |  | 0.5 |

---

附录 半导体器件模型

511

续表

| 序号 | 符号 | SPICE关键字 | 名称 | 隐含值 | 单位 | 举例 |
| --- | --- | --- | --- | --- | --- | --- |
| 33* | $C_{GBO}$ | CGBO | G-B间覆盖电容/单位沟道宽度 | 0.0 | F/m | $2\times10^{-10}$ |
| 34* | $C_{GDO}$ | CGDO | G-D间覆盖电容/单位沟道宽度 | 0.0 | F/m | $2\times10^{-11}$ |
| 35* | $C_{GSO}$ | CGSO | G-S间覆盖电容/单位沟道宽度 | 0.0 | F/m | $2\times10^{-11}$ |
| 36*# | $R_D$ | RD | 漏极欧姆电阻 | 0.0 | Ω | 10 |
| 37*# | $R_S$ | RS | 源极欧姆电阻 | 0.0 | Ω | 10 |
| 38*# | $R_{SH}$ | RSH | 漏-源扩散区薄层电阻 | 0.0 | Ω | 30 |
| 39*# | $C_{BD}$ | CBD | 零偏B-D电容 | 0.0 | F |  |
| 40*# | $C_{BS}$ | CBS | 零偏B-S电容 | 0.0 | F |  |
| 41# | — | KAPPA | 饱和场因子 | 0.2 |  |  |

## 四、集成运放的模型及其参数

为了使问题简单化,突出主要特性,对于复杂的电子电路或电子系统往往采用宏模型。宏模型应在一定精度内,准确地模拟原电路的电特性,且电路的结构要尽可能简单。图5所示为集成运放的直流特性宏模型,表6所示为F007的手册参数和直流宏模型参数的关系。

![](../../raw/pages_0513-0544/images/page_533_image_6.jpg)

<details>
<summary>text_image</summary>

gm2 UIC
RC - EID + RID UID +
U1 +
- +
UIC RIC I+ RIC - I- gm1 UID UO
RO
</details>

图 5 集成运放的直流特性宏模型

表 6 集成运放 F007 的手册参数和直流宏模型参数

| 序号 | 参数名称 | 手册参数 | 宏模型参数与手册参数的关系 |
| --- | --- | --- | --- |
| 1 | 输入偏置电流 | $I_{\text{B}} = 80 \times 10^{-9} \text{A}$ | $I^{+} = I_{\text{B}} = 80 \times 10^{-9} \text{A}$ |
| 2 | 输入失调电流 | $I_{\text{IO}} = 10 \times 10^{-9} \text{A}$ | $I^{-} = I_{\text{B}} + I_{\text{IO}} = 90 \times 10^{-9} \text{A}$ |
| 3 | 差模输入电阻 | $r_{\text{id}} = 2 \text{ M}\Omega$ | $R_{\text{ID}} = r_{\text{id}} = 2 \text{ M}\Omega$ |
| 4 | 共模输入电阻 | $r_{\text{ic}} = 2 \times 10^{9} \Omega$ | $R_{\text{IC}}^{+} = R_{\text{IC}}^{-} = r_{\text{ic}} = 2 \times 10^{9} \Omega$ |
| 5 | 输出电阻 | $r_{\text{o}} = 75 \Omega$ | $R_{\text{O}} = r_{\text{o}} = 75 \Omega$ |
| 6 | 输入失调电压 | $U_{\text{IO}} = 2 \text{ mV}$ | $E_{\text{IO}} = U_{\text{IO}} = 2 \text{ mV}$ |
| 7 | 差模开环增益 | $A_{\text{od}} = 2 \times 10^{5}$ | $g_{\text{m1}} = A_{\text{od}} / R_{\text{O}} = 2.76 \times 10^{3} \text{S}$ |
| 8 | 共模抑制比 | $K_{\text{CMR}} = 3.16 \times 10^{4}$ | $g_{\text{m2}} = 1 / (K_{\text{CMR}} R_{\text{C}}) = 0.316 \times 10^{-6} \text{S} \quad (R_{\text{C}} = 100 \Omega)$ |

---

512

附录 半导体器件模型

图 6 所示为集成运放的交流小信号宏模型, 其电路由输入级、第一中间级、第二中间级和输出级组成。输入级模拟运放差模和共模输入阻抗、共模抑制比, 第一中间级模拟差模开环电压增益、上限频率, 第二中间级模拟单位增益带宽, 输出级模拟输出阻抗。表 7 所示为 F007 的手册参数和交流宏模型参数的关系。

![](../../raw/pages_0513-0544/images/page_534_image_3.jpg)

<details>
<summary>text_image</summary>

g_m1 U_IC
R_C
U_I
R_ID C_ID
U_I
+
U_I^+ U_IC C_IC
-
输入级
R_IC
U_I
+
第一中间级
R_1 C_1 U_1
+
R_2 R_3 C_2 U_2
g_m2 U_I
g_m3 U_1
g_m4 U_2
输出级
R_O U_O
</details>

图 6 集成运放的交流小信号宏模型

表 7 集成运放 F007 的手册参数和交流小信号宏模型参数

| 序号 | 参数名称 | 手册参数 | 宏模型参数与手册参数的关系 |
| --- | --- | --- | --- |
| 1 | 差模输入电阻 | $r_{\text{id}} = 2 \, \text{M}\Omega$ | $R_{\text{ID}} = r_{\text{id}} = 2 \, \text{M}\Omega$ |
| 2 | 差模输入电容 | $C_{\text{id}} = 1.4 \times 10^{-12} \, \text{F}$ | $C_{\text{ID}} = C_{\text{id}} = 1.4 \times 10^{-12} \, \text{F}$ |
| 3 | 共模输入电阻 | $r_{\text{ic}} = 2 \times 10^{9} \, \Omega$ | $R_{\text{IC}} = r_{\text{ic}} = 2 \times 10^{9} \, \Omega, C_{\text{IC}} = 0.256 \times 10^{-12} \, \text{F}$ |
| 4 | 共模抑制比 | $K_{\text{CMR}} = 3.16 \times 10^{4}$ | $R_{\text{C}} = 10 \, \Omega, g_{\text{m2}}(f) = (300 + \text{j}f) \times 0.105 \times 10^{-7} \, \text{S}$ |
| 5 | 差模开环增益 | $A_{\text{od}} = 2 \times 10^{5}$ | $R_{1} = 85.2 \times 10^{3} \, \Omega, g_{\text{m2}} = 2.35 \, \text{S}$ |
| 6 | 上限频率 | $f_{\text{H}} = 7 \, \text{Hz}$ | $R_{1} = 85.2 \times 10^{3} \, \Omega, C_{1} = 0.267 \times 10^{-6} \, \text{F}$ |
| 7 | 单位增益带宽 | $f_{\text{C}} = 2 \times 10^{6} \, \text{Hz}$ | $R_{2} = 1 \times 10^{3} \, \Omega, C_{2} = 79.6 \times 10^{-12} \, \text{F}, R_{3} = 10 \, \Omega, g_{\text{m3}} = 0.1 \, \text{S}$ |
| 8 | 输出电阻 | $r_{\text{o}} = 75 \, \Omega$ | $r_{\text{o}} = 75 \, \Omega, g_{\text{m3}} = 0.013 \, \text{S}$ |
