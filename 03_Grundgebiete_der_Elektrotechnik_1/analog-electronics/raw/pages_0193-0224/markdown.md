合和直接耦合两种情况下的偏置电路；静态时， $u_{11}=u_{12}=0$ ，由于4个电阻均为R，阻值相等，故 $u_{P}=u_{N}=V_{CC}/2$ 。如果正、负两个方向信号变化的幅值不同，可通过调整偏置电路中电阻阻值来调高或调低Q点。

## 四、消除自激振荡

为防止电路产生自激振荡 $^{①}$ ，且消除各电路因共用一个电源相互之间所产生的影响，应在集成运放的电源端加去耦电容；“去耦”是指去掉联系，一般去耦电容多用一个容量大的和一个容量小的电容并联在电源正、负极。

有的集成运放还需外接频率补偿电容,应特别注意接入电容的容量需合适,否则会影响集成运放的带宽,详细分析可查阅第5章5.5节。

## 3.7.2 保护措施

集成运放在使用中常因以下三种原因被损坏:输入信号过大,使 PN 结击穿;电源电压极性接反或过高;输出端直接接“地”或接电源,运放将因输出级功耗过大而损坏。因此,为使运放安全工作,也从三个方面进行保护。

## 一、输入保护

一般情况下,运放工作在开环(即未引反馈)状态时,易因差模电压过大而损坏;在闭环状态时,易因共模电压超出极限值而损坏。图3.7.3(a)所示是防止差模电压过大的保护电路,(b)所示是防止共模电压过大的保护电路。

![](images/page_192_image_10.jpg)

图 3.7.3 输入保护措施

(a) 防止输入差模信号过大 (b) 防止共模信号过大

## 二、输出保护

图 3.7.4 所示为输出端保护电路,限流电阻 R 与稳压管  $D_{z}$  构成限幅电路。一方面将负载与集成运放输出端隔离开来,限制了运放的输出电流;另一方面也限制了输出电压的幅值。当然,任何保护措施都是有限度的,若将输出端直接接电源,则稳压管会损坏,使电路的输出电阻大大提高,影响了电路的性能。

## 三、电源端保护

为了防止电源极性接反,可利用二极管的单向导电性,在电源端串联二极管来实现保护,如图3.7.5所示。

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 关于自激振荡，请参阅第5章5.5节。</span></small>

![](images/page_193_image_2.jpg)

<details>
<summary>text_image</summary>

A
R
Dz
uO
</details>

图 3.7.4 输出保护电路

![](images/page_193_image_4.jpg)

<details>
<summary>text_image</summary>

+VCC
D1
A
-
D2
-VCC
</details>

图 3.7.5 电源端保护

## 3.8 Multisim 应用举例

## 3.8.1 直接耦合多级放大电路调试方法的研究

## 一、仿真电路

在图3.8.1中所示两级直接耦合放大电路中，第一级为双端输入、单端输出差分放大电路，放大管Q1、Q2和恒流源电路中的晶体管Q3均为2N2222A, $\beta = 220, r_{\mathrm{bb'}} = 130\Omega$；稳压管的型号为IN4730A，稳定电压为 $3.891\mathrm{V}$；第二级为PNP型管组成的共射放大电路，管子型号为2N3720，$\beta = 133, r_{\mathrm{bb'}} = 10\Omega$。

## 二、仿真目的

调整两级放大电路的集电极电阻  $R_{1}$ 、 $R_{5}$ （其余电阻阻值如图 3.8.1 所标注保持不变），使电路静态时放大管 Q4 的集电极电位为 2～3 V，以保证电路的最大不失真输出电压尽可能大些；而且使电路电压放大倍数的数值大于 500。

在满足上述条件下,研究电路共模抑制比的测试方法和温度对电路静态工作点的影响。

![](images/page_193_image_13.jpg)

<details>
<summary>text_image</summary>

Multim - 直接耦合两级放大电路
File Edit View Place Simulate Transfer Tools Reports Options Window Help
直接耦合两级放大电路
Oscilloscope-XSC1
XPG1
2N2222A
Q1
R1
18kOhm
R3
2kOhm
R4
360 Ohm
XMC3
XSC1
R6
1kOhm
JDM1
R7
1kOhm
Q3
2N2222A
Q2
R2
30kOhm
D3
1N4730A
VCC
12 V
Q4
2N3702
R5
16kOhm
VSE
6 V
Multimeter-XMM1
Multimeter-XMM2
Multimeter-XMM3
11.10V
A V dB
Set
Multimeter-XMM2
A V dB
Set
Multimeter-XMM3
A V dB
Set
A V dB
Channel_A  Channel_B  Reverse Save
Time  Channel_A  Channel_B  Thigger Edge  C
97.508 ms  1.100 V  -27.904 mV  Save
Scale: 5 MHz/Div  Scale: 500 mV/Div  Scale: 20 mV/Div  Level: 0  V
X position  B Y position  B Y position  B Level: 0  V
Y/T Add B/A A/B AC 0 DC AC 0 DC - Steg Nor Auto
</details>

图 3.8.1 两级直接耦合放大电路的测试

## 三、仿真内容

## 1. 根据仿真目的确定部分电路参数

利用参数扫描分析或者累试的方法,结合虚拟仪器的测试调整  $R_{1}$  和  $R_{5}$  阻值,使之满足 Q4 集电极静态电位在 2\~3 V 之间,且  $\left|\dot{A}_{u}\right|>500$ 。

在图 3.8.1 中,用自左至右三个万用表的直流电压挡,分别测量 Q2 集电极、Q4 集电极和 Q4 发射极静态电位;用函数发生器给放大电路输入频率为 100 Hz、峰-峰值为 2 mV 的正弦波电压,用示波器测量 Q2 集电极、Q4 集电极的交流信号的峰值电压。参数调试结果如图中标注,测试数据见万用表和示波器的读数。

静态数据整理如表 3.8.1 所示。

表 3.8.1 静态工作点的调试

| Q2集电极电阻$R_1/k\Omega$ | Q4集电极电阻$R_5/k\Omega$ | Q2集电极静态电位$U_{C2Q}/V$ | Q4集电极静态电位$U_{C4Q}/V$ | Q4集电极静态电流$I_{C4Q}/mA$ | Q4静态管压降$U_{CE4Q}/V$ |
| --- | --- | --- | --- | --- | --- |
| 18 | 16 | 11.102 | 2.411 | 0.53 | 8.441 |

表中 Q4 的静态电流和管压降算式如下:

$$
I _ {\mathrm{C4Q}} = \frac {U _ {\mathrm{C4Q}} + V _ {\mathrm{EE}}}{R _ {5}} = \frac {(2 . 4 1 1 + 6) \mathrm{V}}{1 6 \mathrm{k} \Omega} \approx 0. 5 3 \mathrm{mA}
$$

$$
U _ {\mathrm{CE4Q}} = U _ {\mathrm{C4Q}} + V _ {\mathrm{EE}} = (2. 4 1 1 + 6) \mathrm{V} = 8. 4 4 1 \mathrm{V}
$$

管压降数据表明 Q4 远离饱和区；且由于总电源电压为  $V_{CC} + V_{EE} = 18 \, V$ ，表明 Q4 也远离截止区；所以最大不失真输出电压较大。

动态测试数据及整理如表 3.8.2 所示。

表 3.8.2 电压放大倍数的调试

| 输入差模信号电压峰值/mV | 第一级输出电压峰值/mV | 第二级输出电压峰值/V | 第一级差模放大倍数 | 第二级电压放大倍数 | 整个电路的电压放大倍数 |
| --- | --- | --- | --- | --- | --- |
| 2 | -27.904 | 1.100 | -13.95 | 39.42 | -550 |

表 3.8.1 和表 3.8.2 表明,从静态到动态均达到仿真的目的。

应当指出,选取电路参数是电路设计的一部分,而且通常满足要求的参数不是唯一的,可以有多组。根据确定的参数,读者可自行进行分析估算,并与仿真结果比较,这里不赘述。

## 2. 测试电路的共模抑制比

加共模信号,从示波器可读出输出电压的峰值,得到共模电压放大倍数,从而得共模抑制比。测试电路如图3.8.2所示。测试结果及分析见表3.8.3。

利用分立元件搭建实际硬件电路很难保证差分电路的对称性,同时其恒流源电路也不是理想恒流源,因此共模放大倍数比较大,共模抑制比比较小。这里采用了器件的真实模型,虽然解决了对称性问题,但没有解决恒流源的理想化问题,故而共模放大倍数不是零,共模抑制比不是无穷大。尽管如此,与实际的分立元件电路比较,这两项指标已相当优秀了。

## 3. 温度对静态工作点的影响

在 Multisim 环境下, 默认温度是  $27^{\circ}C$  。利用“温度扫描分析”(Temperature Sweep Analysis)能够了解温度对静态工作点的影响。首先设置温度的起始值( $0^{\circ}C$ )、终了值( $50^{\circ}C$ )和点数(步长为  $10^{\circ}C$ ), 然后确定扫描对象 Q2 集电极(S6)和 Q4 集电极(S5)的电位, 最后按扫描键, 结果如图 3.8.3 所示。

![](images/page_195_image_4.jpg)

<details>
<summary>text_image</summary>

File Edit View Place Simulate Transfer Tools Reports Options Window Help
XPU1
2N2222A
Q1
2N2222A
Q2
2N2222A
Function Generator XF
Waveform
Signal Options
Frequency 101 Hz
Duty Cycles 50 %
Amplitude 50 mV
Offset 0 V
Common
@ # -
On-Bioscope-XSC.T
XNC1
XNC2
XNC3
XNC4
XNC5
XNC6
XNC7
XNC8
XNC9
XNC10
XNC11
XNC12
XNC13
XNC14
XNC15
XNC16
XNC17
XNC18
XNC19
XNC20
XNC21
XNC22
XNC23
XNC24
XNC25
XNC26
XNC27
XNC28
XNC29
XNC30
XNC31
XNC32
XNC33
XNC34
XNC35
XNC36
XNC37
XNC38
XNC39
XNC40
XNC41
XNC42
XNC43
XNC44
XNC45
XNC46
XNC47
XNC48
XNC49
XNC50
XNC51
XNC52
XNC53
XNC54
XNC55
XNC56
XNC57
XNC58
XNC59
XNC60
XNC61
XNC62
XNC63
XNC64
XNC65
XNC66
XNC67
XNC68
XNC69
XNC70
XNC71
XNC72
XNC73
XNC74
XNC75
XNC76
XNC77
XNC78
XNC79
XNC80
XNC81
XNC82
XNC83
XNC84
XNC85
XNC86
XNC87
XNC88
XNC89
XNC90
XNC91
XNC92
XNC93
XNC94
XNC95
XNC96
XNC97
XNC98
XNC99
XNSC1
</details>

图 3.8.2 两级直接耦合放大电路共模放大倍数的测试

表 3.8.3 共模放大倍数的测试

| 输入共模信号电压峰值/mV | 第一级输出电压峰值/μV | 第二级输出电压/μV | 第一级共模放大倍数 | 整个电路的共模放大倍数 | 共模抑制比 |
| --- | --- | --- | --- | --- | --- |
| 50 | 1.988 | 66.006 | $4 \times 10^{-5}$ | $-1.32 \times 10^{-3}$ | $4.08 \times 10^{5}$ |

![](images/page_195_image_8.jpg)

<details>
<summary>text_image</summary>

直接耦合两级放大电路
Temperature Sweep:
$5, Temperature=0 493.65123m
$6, Temperature=0 11.10889
$5, Temperature=10 1.19122
$6, Temperature=10 11.10654
$5, Temperature=20 1.90301
$6, Temperature=20 11.10398
$5, Temperature=30 2.62777
$6, Temperature=30 11.10121
$5, Temperature=40 3.36440
$6, Temperature=40 11.09825
$5, Temperature=50 4.11192
$6, Temperature=50 11.09512
</details>

图 3.8.3 两级直接耦合放大电路温度扫描分析结果

从扫描结果可以看出，Q2集电极电位变化较小，这是因为差分放大电路中恒流源电路的共模负反馈作用很强，使之温度漂移不明显。而第二级电路直流负反馈较弱，因而随着温度的升高，Q4集电极电位不断升高，即Q4集电极电阻上电压不断增大，说明其集电极电流增大，管压降减小，Q点明显漂移。Q点变化，将引起一系列动态参数的变化；因此，如果直接耦合放大电路不解决温度漂移的问题就不能成为实用电路。

## 四、总结

1. 由于直接耦合放大电路各级之间的静态工作点相互影响，在变化某一电路参数时会引起多个静态参数变化，直接在硬件电路中进行调试比较困难；因此，应通过EDA软件调整电路参数使之基本达到预期结果，再搭建电路，进行实际测试。利用参数扫描分析或累试的方法均可较快地确定电路参数，而且电路仿真时应采用实际所用元器件的模型参数，仿真对硬件实现才有指导意义。
2. 图 3.8.1 所示电路可等效为一个双端输入单端输出的差分放大电路, 可用对差分放大电路的评价方法来测评其性能好坏, 其电压放大倍数就是差模放大倍数。
3. 实际的差分放大电路的共模放大倍数不可能为零，即共模抑制比不可能无穷大；而且仿真表明，图 3.8.1 所示电路在温度变化时第二级 Q 点的变化很大，因此直接耦合多级放大电路需引入足够强的直流负反馈才能稳定静态工作点，克服漂移，也才能成为实用电路。

## 3.8.2 消除互补输出级交越失真方法的研究

## 一、仿真电路

基本互补电路和消除交越失真互补输出级如图 3.8.4(a) 所示。晶体管采用 NPN 型晶体管 2N3904 和 PNP 型晶体管 2N3906。二极管采用 1N4009。

在实际的实验中,几乎不可能得到具有较为理想对称特性的 NPN 型和 PNP 型管,但是在 Multisim 中却可以做到。因此,可以看到只受晶体管输入特性影响(不受其它因素影响)所产生的失真和消除这种失真的方法。

## 二、仿真内容

1. 利用直流电压表测量两个电路中晶体管基极和发射极电位, 得到静态工作点, 如图 3.8.4(a) 所示。各电压表所测量的电压如图中所标注。
2. 用示波器分别观察两个电路输入信号波形和输出信号波形，并测试输出电压的幅值。如图3.8.4(b)所示。Channel A为输入电压波形，Channel B为输出电压波形。

## 三、仿真结果

仿真结果如表 3.8.4 和表 3.8.5 所示。

表 3.8.4 基本互补电路的测试数据

| 直流电压表1读数$U_{B1}$/mV | 直流电压表2读数$U_{E1}$/nV | 输入信号V1峰值/V | 输出信号峰值/V |
| --- | --- | --- | --- |
| 0 | -8.987 | 2 | 1.331 |

表 3.8.5 消除交越失真的互补输出级的测试数据

| 直流电压表3读数$U_{B3}$/mV | 直流电压表4读数$U_{B4}$/mV | 直流电压表5读数$U_{E3}$/mV | 输入信号V2峰值/V | $Q_3$基极动态电位/V | $Q_4$基极动态电位/V | 输出信号峰值/V |
| --- | --- | --- | --- | --- | --- | --- |
| 721.256 | -721.324 | 14.705 | 2 | 1.406 | 1.406 | 1.997 |

![](images/page_197_image_2.jpg)

<details>
<summary>text_image</summary>

Multisim - [互补输出集成电路-0点]
File Edit View Place Simulate Transfer Tools Reports Options Window Help
A
B
C
D
E
F
G
H
I
J
K
L
M
N
O
P
Q
R
S
T
U
V
W
X
Y
Z
VCC 15V
Q1
180404
Q2
20042
RL1 1kOhm
-15V
VCC 15V
R1 1kOhm
Q1
R1 1k4009
203904
V3 0 V 100 Hz 0deg
R2 1k4009
Q4
20044
RL2 1kOhm
-15V
Multimeter-XMM1
U/V
A V dB
Set...
Multimeter-XMM2
-0.90 mV
A V dB
Set...
Multimeter-XMM3
721.25 mV
A V dB
Set...
Multimeter-XMM4
721.25 mV²
A V dB
Set...
Multimeter-XMM5
-1.75 mV
A V dB
Set...
</details>

(a)

![](images/page_197_image_4.jpg)

<details>
<summary>text_image</summary>

Multisim - [互补输出级电路.ms7]
File Edit View Place Simulate Transfer Tools Reports Options Window Help
VCL 1kV
Q1
JSC2
JSC3
Multimeter...
1.406 V
A V
Set...
Multimeter...
1.406 V
A V
Set...
Oscilloscope-XSC2
Oscilloscope-XSC3
T1 Time Channel_A Channel_B Reverse T2 Time Channel_A Channel_B Reverse T2-T1
72.472 ms 2.000 V 1.331 V
Timebase Channel_A Channel_B Trigger Edge SND C
Scale 2 ms/Div Scale 1 V/Div Scale 1 V/Div
X position 0 Y position 0 Y position 0 Y position 0 Y position 0 Y position 0 Y position 0 Y position 0 Y position 0 Y position 0 Y position 0 Y position 0 Y position 0 Y position 0 Y position 0 Y position 0 Y position 0 Y position 0 Y position 0 Y position 0 Y position 0 Y position 0 Y position 0 Y position 0 Y position 0 Y position 0
Add B/A A/S AC 0 DC C Sing, Nor, Auto
</details>

(b)

图 3.8.4 互补输出级电路的测试

(a) 静态测试 (b) 动态测试

## 四、总结

1. 对基本互补电路的测试可得到如下结论:

(1) 静态时晶体管基极和发射极的直流电压均为0, 静态功耗小。

（2）由于输入电压小于 b-e 间的开启电压时两只晶体管均截止，输出信号波形明显产生了交越失真，且输出电压峰值小于输入电压峰值。

2. 对消除交越失真的互补输出级的测试可得到如下结论:

（1）晶体管基极直流电位 $U_{\mathrm{B3}} \approx -U_{\mathrm{B4}} = 721 \mathrm{~mV}$，表明两只管子在静态均处于导通状态，发射极的直流电位 $U_{\mathrm{E3}} \approx 14.7 \mathrm{~mV}$，很接近0，说明管子具有很好的对称性。 $U_{\mathrm{B3}} \neq -U_{\mathrm{B4}}, U_{\mathrm{E3}} \neq 0$ 的原因仍在于NPN型晶体管2N3904和PNP型晶体管2N3906的不对称性。
（2）输入电压的峰值为 2 V，有效值约为 1.414 V。在动态测试中， $U_{b3} = U_{b4} = 1.406 V \approx U_i$ ，说明在动态的近似分析中可将  $T_3$  和  $T_4$  的基极与输入端看成为一个点。
（3）输出电压峰值与输入电压峰值相差无几，且输出信号波形没有产生失真，说明合理设置静态工作点是消除交越失真的基本方法，且使电路的跟随特性更好。

## 本章小结

本章首先讲述多级放大电路的耦合方式及分析方法，然后阐明集成运放的结构特点、电路组成、电压传输特性，进而分析组成运放的差分放大电路、电流源电路、互补输出级电路，最后简述集成运放内部电路的工作原理、主要性能指标、种类及使用方法等。

一、多级放大电路的耦合方式和分析方法。

直接耦合放大电路存在温度漂移问题，低频特性好，能够放大变化缓慢的信号，便于集成化，应用广泛；阻容耦合放大电路利用耦合电容“隔离直流，通过交流”，低频特性差，不便于集成化，仅用于非用分立元件电路不可的情况；变压器耦合放大电路能够实现阻抗变换，常用作调谐放大电路或输出功率很大的功率放大电路；光电耦合方式具有电气隔离作用，使电路抗干扰能力强，适用于信号的隔离和远距离传送。

多级放大电路的电压放大倍数等于组成它的各级电路电压放大倍数之积，在求解某一级的电压放大倍数时应将后级输入电阻作为负载。其输入电阻是第一级的输入电阻，输出电阻是末级的输出电阻。输出波形失真时，应首先判断从哪一级开始产生失真，然后再判断失真性质并予以消除。

二、集成运放是一种高性能的直接耦合放大电路，从外部看，可等效成双端输入、单端输出的差分放大电路。通常由输入级、中间级、输出级和偏置电路四部分组成。输入级多用差分放大电路，中间级为共射（共源）电路，输出级多用互补输出级，偏置电路是多路电流源电路。
三、基本差分放大电路利用参数的对称性进行补偿来抑制温漂，长尾式放大电路和具有恒流源的差分放大电路还利用共模负反馈抑制每只放大管的温漂。用共模放大倍数 $A_{e}$ 、差模放大倍数 $A_{d}$ 、共模抑制比 $K_{CMR}$ 、输入电阻和输出电阻来描述差分电路的性能。根据输入端与输出端接地情况不同，差分放大电路有四种接法。

在集成运放中,不但充分利用元件参数一致性好的特点构成高质量的差分放大电路,而且还可构成各种电流源电路,它们既为各级放大电路提供合适的静态电流,又作为有源负载,从而大大提高了运放的增益。

互补输出电路在零输入时零输出，输出正、负方向对称，双向跟随，具有很强的带负载能力。

四、集成运放的主要性能指标有 $A_{\mathrm{od}}, r_{\mathrm{id}}, U_{10}$ 和 $\mathrm{d}U_{10} / \mathrm{d}T, I_{10}$ 和 $\mathrm{d}I_{10} / \mathrm{d}T, -3$ dB带宽 $f_{\mathrm{H}}$ 、单位增益带宽 $f_{\mathrm{c}}$ 和 $SR$ 等。通用型运放各方面参数均衡，适合一般应用；专用型运放在某方面的性能指标特别优秀，适合有特殊要求的场合。
五、使用运放时应注意调零、设置偏置电压、频率补偿和必要的保护措施。目前多数产品内部有补偿电容，部分产品内部有稳零措施。

学完本章后希望能够达到以下要求:

一、掌握以下概念及定义:零点漂移与温度漂移，共模信号与共模放大倍数，差模信号与差模放大倍数，共模抑制比，差模输入电阻，失调电压和失调电流，-3 dB带宽 $f_{H}$ 等。

二、掌握各种耦合方式的优缺点，能够正确估算多级放大电路的 $\dot{A}_{u}$ 、 $R_{i}$ 和 $R_{o}$ 。

三、熟悉集成运放的组成及各部分的作用，正确理解主要指标参数的物理意义及其使用注意事项。

四、理解差分放大电路的组成和工作原理,掌握静态和动态参数的分析方法;了解电流源电路的工作原理;掌握互补输出级(OCL电路)的正确接法和输入-输出关系。

五、了解一种运放电路的工作原理。

## 自测题

## 一、现有基本放大电路:

A. 共射电路

B. 共集电路

C. 共基电路

D. 共源电路

E. 共漏电路

根据要求选择合适电路组成两级放大电路。

（1）要求输入电阻为 $1\sim 2\mathrm{k}\Omega$ ，电压放大倍数大于3000，第一级应采用\_\_\_\_，第二级应采用\_\_\_\_。
(2) 要求输入电阻大于  $10 \, M\Omega$ ，电压放大倍数大于 300，第一级应采用 \_\_\_\_，第二级应采用 \_\_\_\_。
（3）要求输入电阻为  $100 \sim 200 \, k\Omega$ ，电压放大倍数数值大于 100。第一级应采用 \_\_\_\_，第二级应采用 \_\_\_\_。
(4) 要求电压放大倍数的数值大于 10, 输入电阻大于  $10 \, M\Omega$ , 输出电阻小于  $100 \, \Omega$ , 第一级应采用 \_\_\_\_ , 第二级应采用 \_\_\_\_ 。
（5）设信号源为内阻很大的电压源，要求将输入电流转换成输出电压，且 $|\dot{A}_{si}|=|\dot{U}_{o}/\dot{I}_{i}|>1000$ ，输出电阻 $R_{o}<100$ ，第一级应采用\_\_\_\_，第二级应采用\_\_\_\_。

## 二、选择合适的答案填入空内。

(1) 直接耦合放大电路存在零点漂移的原因是\_\_\_\_。

A. 元件老化

B. 晶体管参数受温度影响

C. 放大倍数不够稳定

D. 电源电压不稳定

(2) 集成放大电路采用直接耦合方式的原因是 \_\_\_\_。

A. 便于设计

B. 放大交流信号

C. 不易制作大容量电容

(3)差分放大电路的差模信号是两个输入端信号的\_\_\_\_，共模信号是两个输入端信号的\_\_\_\_。

A. 差

B. 和

C. 平均值

（4）用恒流源取代长尾式差分放大电路中的发射极电阻  $R_{e}$ ，将使电路的 \_\_\_\_。

A. 差模放大倍数数值增大

B. 抑制共模信号能力增强

C. 差模输入电阻增大

(5) 通用型集成运放适用于放大\_\_\_\_。

A. 高频信号

B. 低频信号

C. 任何频率信号

(6) 集成运放的输入级采用差分放大电路是因为可以 \_\_\_\_。

A. 减小温漂

B. 增大放大倍数

C. 提高输入电阻

(7) 为增大电压放大倍数, 集成运放的中间级多采用 \_\_\_\_。

A. 共射放大电路

B. 共集放大电路

C. 共基放大电路

(8)集成运放的末级采用互补输出级是为了\_\_\_\_。

A. 电压放大倍数大

B. 不失真输出电压大

C. 带负载能力强

三、电路如图 T3.3 所示，所有晶体管均为硅管， $\beta$ 均为 200， $r_{bb'} = 200 \Omega$，静态时 $|U_{BEQ}| \approx 0.7 V$。试求:

(1) 静态时  $T_{1}$  管和  $T_{2}$  管的发射极电流；
（2）若静态时  $u_{0}>0$ ，则应如何调节  $R_{c2}$  的值才能使  $u_{0}=0\ V$ ？若静态  $u_{0}=0\ V$ ，则  $R_{c2}=$ ？电压放大倍数为多少？

![](images/page_200_image_2.jpg)

<details>
<summary>text_image</summary>

+VCC
(+12V)
Rc2 2 kΩ R Re4 500Ω T4
+ uI T1 T2
- T3 + uO
Re3 10 kΩ DZ 3.7 V - Rc4 10 kΩ -VEE (-6V)
</details>

图 T3.3

四、电路如图 T3.4 所示，已知  $\beta_{1}=\beta_{2}=\beta_{3}=100$ 。各管的  $U_{BE}$  均为 0.7 V，试求  $I_{C2}$  的值。

![](images/page_200_image_5.jpg)

<details>
<summary>text_image</summary>

+Vcc
(+15V)
R
134kΩ
T2
IC2
T0
T1
</details>

图 T3.4

![](images/page_200_image_7.jpg)

<details>
<summary>text_image</summary>

u11
T1
T2
u12
I2
T3
T4
D1
D2
T7
T8
R
T5
T6
+VCC
T9
uO
T10
-VCC
</details>

图 T3.5

五、某型号集成运放的简化电路如图 T3.5 所示。

（1）说明电路是几级放大电路，各级分别是哪种形式的放大电路（共射、共集、差分……）:
(2) 分别说明各级采用了哪些措施来改善其性能指标(如增大放大倍数、增大输入电阻……)。

## 习题

3.1 判断图 P3.1 所示各两级放大电路中， $T_{1}$  和  $T_{2}$  管分别组成哪种组态（共射、共射……接法）。设图中所有电容对于交流信号均可视为短路。
3.2 设图 P3.2 所示各电路的静态工作点均合适, 分别画出它们的交流等效电路, 并写出  $\dot{A}_{u}$ 、 $R_{i}$  和  $R_{o}$  的表达式。
3.3 基本放大电路如图 P3.3(a)、(b) 所示，图 (a) 点画线框内为电路 I，图 (b) 点画线框内为电路 II。由电路 I、II 组成的多级放大电路如图 (c)、(d)、(e) 所示，它们均正常工作。试说明图 (c)、(d)、(e) 所示电路中

(1) 哪些电路的输入电阻比较大；
(2) 哪些电路的输出电阻比较小；
(3) 哪个电路的  $\dot{A}_{us} = | \dot{U}_{o} / \dot{U}_{s} |$  最大。

![](images/page_201_image_2.jpg)

<details>
<summary>text_image</summary>

R1
25 kΩ
C1
+
u1
-
R2
5 kΩ
T1
R3
3 kΩ
R5
20 kΩ
+VCC
C3
+
T2
R6
20 kΩ
C4
uO
R4
1 kΩ
C2
-
</details>

(a)

![](images/page_201_image_4.jpg)

<details>
<summary>text_image</summary>

R1
20 kΩ
R4
1 kΩ
C2
+VCC
T2
uO
+
-
C1
T1
R5 500 Ω
180 kΩ
R2
R3
500 Ω
C3
-VEE
</details>

(b)

![](images/page_201_image_6.jpg)

<details>
<summary>text_image</summary>

C1
+
ui
R1
300 kΩ
R2
1 kΩ
T1
R3
5 kΩ
C2
R4
2 kΩ
T2
R5
1 kΩ
C4
+VCC
+
uo
-
C3
</details>

(c)

![](images/page_201_image_8.jpg)

<details>
<summary>text_image</summary>

R1
C1
+
ui
-
T1
R3
R5
C3
+
VCC
T2
uO
R2
R4
C2
-
</details>

(d)

![](images/page_201_image_10.jpg)

<details>
<summary>text_image</summary>

R2
2 kΩ
+VCC
C1
T1
T2
C3
+
ui
R1
10 MΩ
R3
1 kΩ
C2
5 kΩ
uO
-
</details>

(e)

![](images/page_201_image_12.jpg)

<details>
<summary>text_image</summary>

C1
+
ui
-
R1
C2
R2
R3
T1
R4
C3
R5
T2
C4
R6
+VCC
uo
-
</details>

(f)

图 P3.1

3.4 电路如图 P3.1(e) 所示, 晶体管的  $\beta$  为 200,  $r_{be}$  为 3 kΩ, 场效应管的  $g_{m}$  为 15 mS; Q 点合适。求解  $\dot{A}_{u}$ 、 $R_{i}$  和  $R_{o}$ 。
3.5 图 P3.5 所示电路参数理想对称，晶体管的  $\beta$  均为 100,  $r_{bb'} = 100 \Omega$ ,  $U_{BEQ} \approx 0.7$ 。试计算  $R_{w}$  滑动端在中点时  $T_{1}$  管和  $T_{2}$  管的发射极静态电流  $I_{EQ}$ ，以及动态参数  $A_{d}$  和  $R_{i}$ 。
3.6 电路如图 P3.6 所示，已知  $T_{1}$  管和  $T_{2}$  管的  $\beta$  均为 140,  $r_{be}$  均为 4 kΩ。试问:若输入直流信号  $u_{11} = 20 \, mV, u_{t2} = 10 \, mV$ ，则电路的共模输入电压  $u_{1c} = ?$  差模输入电压  $u_{1d} = ?$  输出动态电压  $\Delta u_{0} = ?$
3.7 电路如图 P3.7 所示， $T_{1}$  和  $T_{2}$  的低频跨导  $g_{m}$  均为 10 mS。试求解差模放大倍数和输入电阻。
3.8 电路如图 P3.8 所示， $T_{1} \sim T_{5}$  的电流放大系数分别为  $\beta_{1} \sim \beta_{5}$ ，b - e 间动态电阻分别为  $r_{bel} \sim r_{be5}$ ，写出  $\dot{A}_{u}, R_{i}$  和  $R_{0}$  的表达式。

![](images/page_202_image_2.jpg)

图 P3.2

![](images/page_202_image_4.jpg)

图 P3.3

![](images/page_203_image_2.jpg)

<details>
<summary>text_image</summary>

+VCC
(+12V)
Rc
10 kΩ
+
uo
-
Rc
10 kΩ
T1
Rw
T2
100 Ω
ui
-
Re
5.1 kΩ
-VEE
(-6V)
</details>

图 P3.5

![](images/page_203_image_4.jpg)

<details>
<summary>text_image</summary>

Rc
10 kΩ
+VCC
+
uo
-
T1
T2
u11
u12
-
I
-VEE
</details>

图P3.6

![](images/page_203_image_6.jpg)

<details>
<summary>text_image</summary>

Rd
20 kΩ
+
uo
-
Rd
20 kΩ
+VDD
T1
T2
u1
-
I
-Vss
</details>

图 P3.7

![](images/page_203_image_8.jpg)

<details>
<summary>text_image</summary>

+VCC
R2 R3 R5
T1 T2 T4
+ u1 -
T3 R1 R4 R6 R7
T5 + uO -
- VEE
</details>

图P3.8

3.9 电路如图 P3.9 所示。已知电压放大倍数为 -100，输入电压  $u_{1}$  为正弦波， $T_{2}$  和  $T_{3}$  管的饱和压降  $\left|U_{CES}\right|=1\ V$ 。试问:

(1) 在不失真的情况下, 输入电压最大有效值  $U_{imax}$  为多少?
(2) 若  $U_{i}=10\ mV$  (有效值)，则  $U_{o}=?$  若此时  $R_{3}$  开路，则  $U_{o}=?$  若  $R_{3}$  短路，则  $U_{o}=?$

![](images/page_203_image_14.jpg)

<details>
<summary>text_image</summary>

R3
+VCC
(+12 V)
R2
D1
T2
D2
T3
RL
uO
+
-
R1
T1
u1
-
- VCC
(-12 V)
</details>

图 P3.9

3.10 根据下列要求,将应优先考虑使用的集成运放填入空内。已知现有集成运放的类型是:

① 通用型 ② 高阻型 ③ 高速型 ④ 低功耗型 ⑤ 高压型 ⑥ 大功率型 ⑦ 高精度型

(1) 作低频放大器, 应选用 \_\_\_\_ ;

(2) 作宽频带放大器, 应选用 \_\_\_\_ ;
(3) 作幅值为  $1 \mu V$  以下微弱信号的测量放大器, 应选用 \_\_\_\_ ;
(4) 作内阻为  $100 \, k\Omega$  信号源的放大器, 应选用 \_\_\_\_ ;
(5) 负载需 5 A 电流驱动的放大器, 应选用 \_\_\_\_ ;
(6) 要求输出电压幅值为  $\pm80\ V$  的放大器, 应选用 \_\_\_\_ ;
(7) 宇航仪器中所用的放大器, 应选用 \_\_\_\_。

3.11 已知几个集成运放的参数如表 P3.11 所示, 试分别说明它们各属于哪种类型的运放。

表 P3.11

| 特性指标 | $A_{cd}$ | $r_{id}$ | $U_{IO}$ | $I_{IO}$ | $I_{IB}$ | -3 dB$f_{H}$ | $K_{CMR}$ | SR | 单位增益带宽 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 单位 | dB | MΩ | mV | nA | nA | Hz | dB | V/μs | MHz |
| $A_1$ | 100 | 2 | 5 | 200 | 600 | 7 | 86 | 0.5 |  |
| $A_2$ | 130 | 2 | 0.01 | 2 | 40 | 7 | 120 | 0.5 |  |
| $A_3$ | 100 | 1 000 | 5 | 0.02 | 0.03 |  | 86 | 0.5 | 5 |
| $A_4$ | 100 | 2 | 2 | 20 | 150 |  | 96 | 65 | 12.5 |

3.12 多路电流源电路如图 P3.12 所示, 已知所有晶体管的特性均相同,  $U_{BE}$  均为 0.7 V。试求  $I_{C1}$ 、 $I_{C2}$  各为多少。

3.13 电路如图 P3.13 所示，各晶体管的低频跨导均为  $g_{m}$ ， $T_{1}$  和  $T_{2}$  管 D-S 间的动态电阻分别为  $r_{ds1}$  和  $r_{ds2}$ 。试求解电压放大倍数  $A_{u} = \Delta u_{0} / \Delta u_{1}$  的表达式。

![](images/page_204_image_14.jpg)

<details>
<summary>text_image</summary>

+VCC
(+15V)
R 136 kΩ
T3
IC1
IC2
T0
T1
T2
</details>

图 P3.12

![](images/page_204_image_16.jpg)

<details>
<summary>text_image</summary>

+VDD
T3
T2
uO
I
T1
u1
-VSS
</details>

图 P3.13

3.14 电路如图 P3.14 所示， $T_{1}$  与  $T_{2}$  管特性相同，它们的低频跨导为  $g_{m}$ ； $T_{3}$  与  $T_{4}$  管特性对称； $T_{2}$  与  $T_{4}$  管 d-s 间动态电阻分别为  $r_{d+2}$  和  $r_{d+4}$ 。试求出电压放大倍数  $A_{u} = \Delta u_{0} / \Delta (u_{11} - u_{12})$  的表达式。

3.15 电路如图 P3.15 所示, $T_{1}$ 与 $T_{2}$ 管为超 $\beta$ 管,电路具有理想的对称性。选择合适的答案填入空内。

(1) 该电路采用了 \_\_\_\_;

A. 共集 - 共基接法

B. 共集 - 共射接法

C. 共射 - 共基接法

(2) 电路所采用的上述接法是为了 \_\_\_\_；

A. 增大输入电阻

B. 增大电流放大系数

C. 展宽频带

![](images/page_205_image_2.jpg)

<details>
<summary>text_image</summary>

+VDD
I
u11
T1
T2
u12
uO
T3
T4
-VSS
</details>

图 P3.14

![](images/page_205_image_4.jpg)

<details>
<summary>text_image</summary>

+VCC
Rc R Rc
+ uO -
T3 T4
D1
uI1 T1 D2 T2 uI2
I - VEE
</details>

图 P3.15

(3) 电路采用超  $\beta$  管能够 \_\_\_\_ ;

A. 增大输入级的耐压值

B. 增大放大能力

C. 增大带负载能力

(4)  $T_{1}$  与  $T_{2}$  管的静态管压降约为 \_\_\_\_。

A. 0.7 V

B. 1.4 V

C. 不可知

3.16 在图 P3.16 所示电路中，已知  $T_{1} \sim T_{3}$  管的特性完全相同， $\beta \gg 2$ ；反相输入端的输入电流为  $i_{11}$ ，同相输入端的输入电流为  $i_{12}$ 。试问:

(1)  $i_{C2} \approx ?$
(2)  $i_{B3} \approx ?$
(3) $A_{\mathrm{m}} = \Delta u_0 / (i_{11} - i_{12})\approx ?$

![](images/page_205_image_19.jpg)

<details>
<summary>text_image</summary>

i11
iB3
T3
+VCC
Rc
uO
iC2
iC1
T2
T1
i12
</details>

图 P3.16

3.17 比较图 P3.17 所示两个电路, 分别说明它们是如何消除交越失真和如何实现过流保护的。

3.18 图 P3.18 所示为简化的高精度运放电路原理图, 试分析:

(1) 两个输入端中哪个是同相输入端, 哪个是反相输入端;
(2)  $T_{3}$  与  $T_{4}$  的作用；
(3) 电流源  $I_{3}$  的作用；
(4)  $D_{2}$  与  $D_{3}$  的作用。

3.19 通用型运放 F747 的内部电路如图 P3.19 所示, 试分析:

（1）偏置电路由哪些元件组成？基准电流约为多少？
(2) 哪些是放大管？组成几级放大电路？每级各是什么基本电路？

![](images/page_206_image_2.jpg)

图 P3.17

![](images/page_206_image_4.jpg)

<details>
<summary>text_image</summary>

T3
T4
I2
T6
T5
T7
T8
D2
D3
T10
uO
T11
u11
T1
T2
u12
I1
I3
I4
T9
+VCC
-VCC
</details>

图 P3.18

![](images/page_206_image_6.jpg)

<details>
<summary>text_image</summary>

T8
T9
T13
T21
+VCC (+15V)
T23
T1
T2
u12
T12
R9
uO
T4
T7
R5 39 kΩ
T19
T20
T22
R8
R10
T24
T16
T14
T15
T17
T18
R1 R2 R3
R4
T5 T6 T10 T11
R6 R7
-Rw
-VCC (-15V)
</details>

图 P3.19

(3)  $T_{19}$ 、 $T_{20}$  和  $R_{8}$  组成的电路的作用是什么?

3.20 型号为 5G28 的集成运放内部电路如图 P3.20 所示。试分析:

![](images/page_207_image_4.jpg)

<details>
<summary>text_image</summary>

R1
1.4 kΩ
T1
3
T2
T3
4
C
9
T4
T5
T6
T7
T8
R5
600 Ω
R4
30 kΩ
R6
600 Ω
Rw
2 kΩ
R3
30 kΩ
R8
60 Ω
D1
D2
D3
D4
R7
50 Ω
R9
50 Ω
T10
+VCC
8
7
T11
5
-VEE
</details>

图 P3.20

(1) 该运放属于哪种类型的运放(双极型、单极型……);
(2) 哪些是放大管？组成几级放大电路？每级各是什么基本电路；
(3) $R_{7}$ 、 $R_{9}$ 的作用是什么？
(4) 电容 C 的作用是什么?

3.21 利用 Multisim 研究图 P3.5 所示电路在下列情况下对电路静态和动态的影响:

(1) 两个  $R_{c}$  阻值相差 5%;
(2) $R_{w}$ 不在中点；
(3) 两个差分管的电流放大倍数不相等。

提示:为便于调节晶体管参数,采用虚拟晶体管。

3.22 利用 Multisim 为图 P3.8 所示电路选择电路参数, 使之正常工作, 并测试 Q 点、电压放大倍数和输入电阻。

出题目的:

(1) 学习搭建复杂电路的方法和利用 Multisim 辅助设计电子电路的方法。
(2) 了解直接耦合多级放大电路 Q 点的调试方法。

提示:

(1) 晶体管采用实际晶体管, 其余可采用虚拟元件。
(2) 需思考为提高输入电阻, $R_{1} \sim R_{7}$ 应如何选取; 为提高差模放大能力, $R_{1} \sim R_{7}$ 应如何选取。
（3）若测试过程中电路产生了自激振荡，即在输入电压为零时输出为一定频率、一定幅值的正弦波，则在 $T_{4}$ 管基极与集电极之间加一个小容量的电容（如10 pF）消振。

## 第4章

## 放大电路的频率响应

## 本章讨论的问题

- 为什么要研究放大电路的频率响应？
- 如何测定一个RC网络的频率响应？怎样画出频率特性曲线？
- 晶体管与场效应管的h参数等效模型在高频信号下还适用吗？为什么？如何构造高频等效模型？
- 什么是放大电路的通频带？哪些因素影响通频带？如何确定放大电路的通频带？
- 如果放大电路的频率响应不满足要求，应该怎么办？
- 对于放大电路，是通频带愈宽愈好吗？为什么？
- 为什么集成运放的通频带很窄？

## 4.1 频率响应概述

本节将讲述研究频率响应的必要性、有关频率响应的基本概念、放大电路频率响应的分析方法以及频率特性曲线的画法等问题。

## 4.1.1 研究放大电路频率响应的必要性

在放大电路中，由于电抗元件（如电容、电感线圈等）及半导体管极间电容的存在，当输入信号的频率过低或过高时，不但放大倍数的数值会变小，而且还将产生超前或滞后的相移，说明放大倍数是信号频率的函数，这种函数关系称为频率响应或频率特性。第2章中所介绍的“通频带”就是用来描述电路对不同频率信号适应能力的动态参数，对于任何一个具体的放大电路都有一个确定的通频带。因此，在设计电路时，必须首先了解信号的频率范围，以便使所设计的电路具有适应于该信号频率范围的通频带；在使用电路前，应查阅手册、资料，或实测其通频带，以便确定电路的适用范围。

在前面的电路分析中,所用的双极型管和单极型管的等效模型均未考虑极间电容的作用,即认为它们对信号频率呈现出的电抗值为无穷大,因而它们只适用于对低频信号的分析。本章将引入半导体管的高频等效模型,并阐明放大电路上限频率、下限频率和通频带的求解方法,以及频率响应的描述方法。

## 4.1.2 频率响应的基本概念

在放大电路中,由于耦合电容的存在,对信号构成了高通电路,即对于频率足够高的信号电容相当于短路,信号几乎毫无损失地通过;而当信号频率低到一定程度时,电容的容抗不可忽略,信号将在其上产生压降,从而导致放大倍数的数值减小且产生相移。与耦合电容相反,由于半导体管极间电容的存在,对信号构成了低通电路,即对于频率足够低的信号相当于开路,对电路不产生影响;而当信号频率高到一定程度时,极间电容将分流,从而导致放大倍数的数值减小且产生相移。为了便于理解有关频率响应的基本要领,这里将对无源单级RC电路的频率响应加以分析。

## 一、高通电路

在图4.1.1(a)所示高通电路中，设输出电压 $\dot{U}_{\mathrm{o}}$ 与输入电压 $\dot{U}_{\mathrm{i}}$ 之比为 $\dot{A}_u$ ，则

![](images/page_209_image_5.jpg)

图 4.1.1 高通电路及其频率响应

(a) 电路 (b) 频率响应

$$
\dot {A} _ {u} = \frac {\dot {U} _ {o}}{\dot {U} _ {i}} = \frac {R}{\frac {1}{j \omega C} + R} = \frac {1}{1 + \frac {1}{j \omega R C}} \tag {4.1.1}
$$

式中  $\omega$  为输入信号的角频率, RC 为回路的时间常数  $\tau$ , 令  $\omega_{L}=\frac{1}{RC}=\frac{1}{\tau}$ , 则

$$
f _ {\mathrm{L}} = \frac {\omega_ {\mathrm{L}}}{2 \pi} = \frac {1}{2 \pi \tau} = \frac {1}{2 \pi R C} \tag {4.1.2}
$$

因此

$$
\dot {A} _ {u} = \frac {1}{1 + \frac {\omega_ {\mathrm{L}}}{\mathrm{j} \omega}} = \frac {1}{1 + \frac {f _ {\mathrm{L}}}{\mathrm{j} f}} = \frac {\mathrm{j} \frac {f}{f _ {\mathrm{L}}}}{1 + \mathrm{j} \frac {f}{f _ {\mathrm{L}}}} \tag {4.1.3}
$$

将  $\dot{A}_{u}$  用其幅值与相角表示, 得出

$$
\left\{ \begin{array}{l} \mid \dot {A} _ {u} \mid = \frac {\frac {f}{f _ {\mathrm{L}}}}{\sqrt {1 + \left(\frac {f}{f _ {\mathrm{L}}}\right) ^ {2}}} \\ \varphi = 9 0 ^ {\circ} - \arctan \frac {f}{f _ {\mathrm{L}}} \end{array} \right. \tag {4.1.4a}
$$

因式(4.1.4a)表明  $\dot{A}_{u}$  的幅值与频率的函数关系,故称之为  $\dot{A}_{u}$  的幅频特性;因式(4.1.4b)表明  $\dot{A}_{u}$  的相位与频率的函数关系,故称之为  $\dot{A}_{u}$  的相频特性。

由式(4.1.4)可知，当 $f \gg f_{L}$ 时， $\left|\dot{A}_{u}\right| \approx 1, \varphi \approx 0^{\circ}$ ; 当 $f = f_{L}$ 时， $\left|\dot{A}_{u}\right| = 1 / \sqrt{2} \approx 0.707, \varphi =$

$45^{\circ}$; 当 $f \ll f_{\mathrm{L}}$ 时, $f / f_{\mathrm{L}} \ll 1$, $|\dot{A}_u| \approx f / f_{\mathrm{L}}$, 表明 $f$ 每下降 10 倍, $|\dot{A}_u|$ 也下降 10 倍; 当 $f$ 趋于零时, $|\dot{A}_u|$ 也趋于零, $\varphi$ 趋于 $+90^{\circ}$。由此可见, 对于高通电路, 频率愈低, 衰减愈大, 相移愈大; 只有当信号频率远高于 $f_{\mathrm{L}}$ 时, $\dot{U}_{\mathrm{o}}$ 才约为 $\dot{U}_{\mathrm{i}}$。称 $f_{\mathrm{L}}$ 为下限截止频率, 简称下限频率, 在该频率下, $\dot{A}_u$ 的幅值下降到 $70.7\%$, 相移恰为 $+45^{\circ}$。画出图 4.1.1(a) 所示电路的频率特性曲线如图(b)所示, 上边为幅频特性曲线, 下边为相频特性曲线。

## 二、低通电路

图 4.1.2(a) 所示为低通电路, 输出电压  $\dot{U}_{o}$  与输入电压  $\dot{U}_{i}$  之比

![](images/page_210_image_5.jpg)

<details>
<summary>text_image</summary>

R
+   +
Üi   C   Üo
-   -
</details>

(a)

![](images/page_210_chart_7.jpg)

<details>
<summary>line</summary>

| Magnitude | 0.707 |
| --- | --- |
| Phase \(\phi\) | \(0{}^{\circ}\) |
| Phase | \(-45{}^{\circ}\) |
| Phase | \(-90{}^{\circ}\) |
</details>

(b)

图 4.1.2 低通电路及其频率响应

(a) 电路 (b) 频率响应

$$
\dot {A} _ {u} = \frac {\dot {U} _ {\mathrm{o}}}{\dot {U} _ {\mathrm{i}}} = \frac {\frac {1}{\mathrm{j} \omega C}}{R + \frac {1}{\mathrm{j} \omega C}} = \frac {1}{1 + \mathrm{j} \omega R C} \tag {4.1.5}
$$

回路的时间常数  $\tau = RC$ ，令  $\omega_{H} = \frac{1}{\tau}$ ，则

$$
f _ {\mathrm{H}} = \frac {\omega_ {\mathrm{H}}}{2 \pi} = \frac {1}{2 \pi \tau} = \frac {1}{2 \pi R C} \tag {4.1.6}
$$

代入式(4.1.5)可得

$$
\dot {A} _ {u} = \frac {1}{1 + \mathrm{j} \frac {\omega}{\omega_ {\mathrm{H}}}} = \frac {1}{1 + \mathrm{j} \frac {f}{f _ {\mathrm{H}}}} \tag {4.1.7}
$$

将  $\dot{A}_{u}$  用其幅值及相角表示, 得出

$$
\left\{ \begin{array}{l} \mid \dot {A} _ {u} \mid = \frac {1}{\sqrt {1 + \left(\frac {f}{f _ {\mathrm{H}}}\right) ^ {2}}} \\ \varphi = - \arctan \frac {f}{f _ {\mathrm{H}}} \end{array} \right. \tag {4.1.8a}
$$

式(4.1.8a)是 $\dot{A}_{u}$ 的幅频特性,式(4.1.8b)是 $\dot{A}_{u}$ 的相频特性。从对式(4.1.8)的分析可得,当 $f\ll f_{H}$ 时, $|\dot{A}_{u}|\approx1,\varphi\approx0^{\circ}$ ;当 $f=f_{H}$ 时, $|\dot{A}_{u}|=1/\sqrt{2}\approx0.707,\varphi=-45^{\circ}$ ;当 $f\gg f_{H}$ 时, $f/f_{H}\gg1$ , $|\dot{A}_{u}|\approx f_{H}/f$ ,表明f每升高10倍, $|\dot{A}_{u}|$ 降低10倍;当f趋于无穷时, $|\dot{A}_{u}|$ 趋于零, $\varphi$ 趋于$-90^{\circ}$ 。由此可见，对于低通电路，频率愈高，衰减愈大，相移愈大；只有当频率远低于 $f_{\mathrm{H}}$ 时， $\dot{U}_{\circ}$ 才约为 $\dot{U}_{\mathrm{i}}$ 。称 $f_{\mathrm{H}}$ 为上限截止频率，简称上限频率，在该频率下， $\left|\dot{A}_{u}\right|$ 降到 $70.7\%$ ，相移为 $-45^{\circ}$ 。画出幅频特性曲线与相频特性曲线如图4.1.2(b)所示。

放大电路上限频率 $f_{H}$ 与下限频率 $f_{L}$ 之差就是其通频带 $f_{hw}$ ，即

$$
f _ {\mathrm{bw}} = f _ {\mathrm{H}} - f _ {\mathrm{L}} \tag {4.1.9}
$$

## 4.1.3 波特图

在研究放大电路的频率响应时,输入信号(即加在放大电路输入端的测试信号)的频率范围常常设置在几赫到上百兆赫,甚至更宽;而放大电路的放大倍数可从几倍到上百万倍;为了在同一坐标系中表示如此宽的变化范围,在画频率特性曲线时常采用对数坐标,称为波特图 $^{①}$ 。

波特图由对数幅频特性和对数相频特性两部分组成，它们的横轴采用对数刻度 $\lg f$ ，幅频特性的纵轴采用 $20\mathrm{lg}|\dot{A}_u|$ 表示，单位是分贝（dB）；相频特性的纵轴仍用 $\varphi$ 表示。这样不但开阔了视野，而且将放大倍数的乘除运算转换成加减运算。

根据式(4.1.4a)，高通电路的对数幅频特性为

$$
2 0 \lg | \dot {A} _ {u} | = 2 0 \lg \frac {f}{f _ {\mathrm{L}}} - 2 0 \lg \sqrt {1 + \left(\frac {f}{f _ {\mathrm{L}}}\right) ^ {2}} \tag {4.1.10}
$$

与式(4.1.4b)联立可知，当 $f >> f_{\mathrm{L}}$ 时，$20\lg |\dot{A}_{u}| \approx 0\mathrm{dB}, \varphi \approx 0^{\circ}$；当 $f = f_{\mathrm{L}}$ 时，$20\lg |\dot{A}_{u}| = -20\lg \sqrt{2} \approx -3\mathrm{dB}, \varphi = +45^{\circ}$；当 $f << f_{\mathrm{L}}$ 时，$20\lg |\dot{A}_{u}| \approx 20\lg \frac{f}{f_{\mathrm{L}}}$，表明 $f$ 每下降10倍，增益下降$20\mathrm{dB}$，即对数幅频特性在此区间可等效成斜率为 $20\mathrm{dB}/$ 十倍频的直线。

根据式(4.1.8a)，低通电路的对数幅频特性为

$$
2 0 \lg | \dot {A} _ {u} | = - 2 0 \lg \sqrt {1 + \left(\frac {f}{f _ {\mathrm{H}}}\right) ^ {2}} \tag {4.1.11}
$$

与式(4.1.8b)联立可知，当 $f<<f_{H}$ 时， $20\lg|\dot{A}_{u}|\approx0\mathrm{~dB},\varphi\approx0^{\circ}$ ; 当 $f=f_{H}$ 时， $20\lg|\dot{A}_{u}|=-20\lg\sqrt{2}\approx-3\mathrm{~dB},\varphi=-45^{\circ}$ ; 当 $f>>f_{H}$ 时， $20\lg|\dot{A}_{u}|\approx-20\lg\frac{f}{f_{H}}$ ，表明f每上升10倍，增益下降20 dB，即对数幅频特性在此区间可等效成斜率为-20 dB/十倍频的直线。

在电路的近似分析中，为简单起见，常将波特图的曲线折线化，称为近似的波特图。对于高通电路，在对数幅频特性中，以截止频率 $f_{\mathrm{L}}$ 为拐点，由两段直线近似曲线。当 $f > f_{\mathrm{L}}$ 时，以 $20\lg |\dot{A}_u| = 0$ dB 的直线近似；当 $f < f_{\mathrm{L}}$ 时，以斜率为 $20\mathrm{dB} /$ 十倍频的直线近似。在对数相频特性中，用三段直线取代曲线；以 $10f_{\mathrm{L}}$ 和 $0.1f_{\mathrm{L}}$ 为两个拐点，当 $f > 10f_{\mathrm{L}}$ 时，用 $\varphi = 0^{\circ}$ 的直线近似，即认为 $f = 10f_{\mathrm{L}}$ 时 $\dot{A}_u$ 开始产生相移（误差为 $-5.71^\circ$ ）；当 $f < 0.1f_{\mathrm{L}}$ 时，用 $\varphi = +90^\circ$ 的直线近似，即认为 $f = 0.1f_{\mathrm{L}}$ 时已产生 $-90^\circ$ 相移（误差为 $5.71^\circ$ ）；当 $0.1f_{\mathrm{L}} < f < 10f_{\mathrm{L}}$ 时，$\varphi$ 随 $f$ 线性下降，因此当 $f = f_{\mathrm{L}}$ 时 $\varphi = +45^\circ$ 。图4.1.1(a)所示高通电路的波特图如图4.1.3(a)所示。

用同样的方法，将低通电路的对数幅频特性以 $f_{\mathrm{H}}$ 为拐点用两段直线近似，对数相频特性以

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 由 H. W. Bode 提出。</span></small>

![](images/page_212_image_2.jpg)

图 4.1.3 高通电路与低通电路的波特图

(a) 高通电路波特图 (b) 低通电路波特图

0.1 $f_{H}$ 和 $10f_{H}$ 为拐点用三段直线近似，图4.1.2(a)所示低通电路的波特图如图4.1.3(b)所示。

在本节的分析中,具有普遍意义的结论是:

（1）电路的截止频率决定于电容所在回路的时间常数  $\tau$ ，如图 4.1.1(a) 和图 4.1.2(a) 所示电路的  $f_{L}$  和  $f_{H}$  分别如式(4.1.2)、(4.1.6) 所示。
（2）当信号频率等于下限频率 $f_{L}$ 或上限频率 $f_{H}$ 时，放大电路的增益下降3 dB，且产生 $+45^{\circ}$ 或 $-45^{\circ}$ 相移。
(3) 在近似分析中, 可用折线化的近似波特图描述放大电路的频率特性。

## 思考题

4.1.1 试分别用相量图说明图 4.1.1 和图 4.1.2 所示两电路的频率响应。
4.1.2 若一放大电路的电压增益为 100 dB, 则其电压放大倍数为多少?

## 4.2 晶体管的高频等效模型

从晶体管的物理结构出发,考虑发射结和集电结电容的影响,就可以得到在高频信号作用下的物理模型,称为混合  $\pi$  模型。由于晶体管的混合  $\pi$  模型与第 2 章所介绍的 h 参数等效模型在低频信号作用下具有一致性,因此,可用 h 参数来计算混合  $\pi$  模型中的某些参数,并用于高频信号作用下的电路分析。

## 4.2.1 晶体管的混合 $\pi$ 模型

## 一、完整的混合 $\pi$ 模型

图 4.2.1(a) 所示为晶体管结构示意图。 $r_{e}$  和  $r_{e}$  分别为集电区体电阻和发射区体电阻，它们的数值较小，常常忽略不计。 $C_{\mu}$  为集电结电容， $r_{b'e'}$  为集电结电阻， $r_{bb'}$  为基区体电阻， $C_{\pi}$  为发射结电容， $r_{b'e'}$  为发射结电阻。图(b) 是与图(a) 对应的混合  $\pi$  模型。

图中，由于  $C_{\pi}$  与  $C_{\mu}$  的存在，使  $\dot{I}_{c}$  和  $\dot{I}_{b}$  的大小、相角均与频率有关，即电流放大系数是频率的函数，应记作  $\dot{\beta}$ 。根据半导体物理的分析，晶体管的受控电流  $\dot{I}_{c}$  与发射结电压  $\dot{U}_{b'e}$  成线性关系，且与信号频率无关。因此，混合 $\pi$ 模型中引入了一个新参数 $g_{\mathrm{m}}, g_{\mathrm{m}}$ 为跨导，描述 $\dot{U}_{\mathrm{b'e}}$ 对 $\dot{I}_{\mathrm{c}}$ 的控制关系，即 $\dot{I}_{\mathrm{e}} = g_{\mathrm{m}} \dot{U}_{\mathrm{b'e}}$。

![](images/page_213_image_2.jpg)

<details>
<summary>text_image</summary>

c
r_c
c'
R_{b'e'}
R_{bb'}
b'
C_{b'e'} (C_μ)
C_{b'e'} (C_π)
e'
R_{b'e'}
e
e
</details>

(a)

![](images/page_213_image_4.jpg)

<details>
<summary>text_image</summary>

b
+
rbb'
i_b
b'
+
U_be
-
U_b'e
r_b'e
C_π
C_μ
r_b'c
g_m U_b'e
i_c
c
e
r_ce
</details>

(b)

图 4.2.1 晶体管结构示意图及混合  $\pi$  模型

(a) 晶体管的结构示意图 (b) 混合  $\pi$  模型

## 二、简化的混合 $\pi$ 模型

在图4.2.1(b)所示电路中，通常情况下， $r_{ce}$ 远大于c-e间所接的负载电阻，而 $r_{b'e}$ 也远大于 $C_{\mu}$ 的容抗，因而可认为 $r_{ee}$ 和 $r_{b'e}$ 开路，如图4.2.2(a)所示。

由于  $C_{\mu}$  跨接在输入与输出回路之间，使电路的分析变得十分复杂。因此，为简单起见，将  $C_{\mu}$  等效到输入回路和输出回路中去，称为单向化。单向化是通过等效变换来实现的。设  $C_{\mu}$  折合到  $b^{\prime}-e$  间的电容为  $C_{\mu}^{\prime}$ ，折合到 c-e 间的电容为  $C_{\mu}^{\prime\prime}$ ，则单向化之后的电路如图(b)所示。

![](images/page_213_image_12.jpg)

<details>
<summary>text_image</summary>

b
+
rbb'
+
b'
iCμ
Cμ
gmUb'e
c
+
Ube
Ub'e
rbe
Cπ
e
Uce
RL'
</details>

(a)

![](images/page_213_image_14.jpg)

<details>
<summary>text_image</summary>

b
+
rbb'
+
b'
Ube
Ub'e
rbe'
Cπ
Cμ'
gm Ub'e
e
c
Cμ''
-
</details>

(b)

![](images/page_213_image_16.jpg)

<details>
<summary>text_image</summary>

b
+
rbb'
+
b'
gmÛb'e
Ûbe
Ûb'e
r b'e
C'π
e
c
-
</details>

(c)

图 4.2.2 混合  $\pi$  模型的简化

（a）简化的混合 $\pi$ 模型 (b）单向化后的混合 $\pi$ 模型 (c）忽略 $C_{\mu}^{\prime \prime}$ 的混合 $\pi$ 模型

等效变换过程如下: 在图(a)所示电路中, 从 b' 看进去  $C_{\mu}$  中流过的电流为

$$
\dot {I} _ {C \mu} = \frac {\dot {U} _ {\mathrm {b^{\prime} e}} - \dot {U} _ {\mathrm{ce}}}{X _ {C \mu}} = \frac {(1 - \dot {K}) \dot {U} _ {\mathrm {b^{\prime} e}}}{X _ {C \mu}} \quad \left(\dot {K} = \frac {\dot {U} _ {\mathrm{ce}}}{\dot {U} _ {\mathrm {b^{\prime} e}}}\right)
$$

为保证变换的等效性，要求流过 $C_{\mu}^{\prime}$ 的电流仍为 $\dot{I}_{C\mu}$，而它的端电压为 $\dot{U}_{\mathrm{b'e}}$，因此 $C_{\mu}^{\prime}$ 的电抗为

率,因此共基放大电路可作为宽频带放大电路。

在器件手册中查出 $f_{\beta}$ （或 $f_{\mathrm{T}}$ ）和 $C_\mathrm{ob}$ （近似为 $C_\mu$），并估算出发射极静态电流 $I_{\mathrm{EQ}}$，从而得到 $r_{\mathrm{b'e}}$ [见式(4.2.4)]，再根据式(4.2.7)、(4.2.10)就可求出 $C_\pi$ 的值。

## 思考题

4.2.1 为什么在研究晶体管的高频等效电路时引入参数 $g_{\mathrm{m}}$，而且只考虑 $\mathrm{b}' - \mathrm{e}$ 间等效电容的影响，而不考虑 $\mathrm{c} - \mathrm{e}$ 间等效电容的影响？
4.2.2 在共射放大电路中,若静态工作点沿直流负载线上移,则放大管发射结等效电容  $C_{\pi}^{\prime}$  如何变化?为什么?

## 4.3 场效应管的高频等效模型

由于场效应管各极之间存在极间电容，因而其高频响应与晶体管相似。根据场效应管的结构，可得出图4.3.1(a)所示的高频等效模型，大多数场效应管的参数如表4.3.1所示。由于一般情况下 $r_{gs}$ 和 $r_{ds}$ 比外接电阻大得多，因而，在近似分析时，可认为它们是开路的。而对于跨接在g-d之间的电容 $C_{gd}$ ，可将其进行等效变换，即将其折合到输入回路和输出回路，使电路单向化。这样，g-s间的等效电容为

$$
C _ {\mathrm{gs}} ^ {\prime} = C _ {\mathrm{gs}} + (1 - \dot {K}) C _ {\mathrm{gd}} \quad (\dot {K} \approx - g _ {\mathrm{m}} R _ {\mathrm{L}} ^ {\prime}) \tag {4.3.1}
$$

d-s间的等效电容为

$$
C _ {\mathrm{ds}} ^ {\prime} = C _ {\mathrm{ds}} + \frac {\dot {K} - 1}{\dot {K}} C _ {\mathrm{gd}} \quad (\dot {K} \approx - g _ {\mathrm{m}} R _ {\mathrm{L}} ^ {\prime}) \tag {4.3.2}
$$

![](images/page_214_image_13.jpg)

<details>
<summary>text_image</summary>

g
+
U̇gs rgs Cgs gm U̇gs d
-
s
rds Cds U̇ds R'L
</details>

(a)

![](images/page_214_image_15.jpg)

<details>
<summary>chemical</summary>

Electrical circuit diagram of a MOSFET with gate, source, and drain terminals labeled
</details>

(b)

图 4.3.1 场效应管的高频等效模型

(a) 高频等效模型 (b) 简化模型

由于输出回路的时间常数通常比输入回路的小得多,故分析频率特性时可忽略  $C_{ds}^{\prime}$  的影响。这样就得到场效应管的简化的单向化的高频等效模型,如图 4.3.1(b) 所示。

表 4.3.1 场效应管的主要参数

| 管子类型\\参数(单位) | $g_m/mS$ | $r_{ds}/\Omega$ | $r_{gs}/\Omega$ | $C_{gs}/pF$ | $C_{gd}/pF$ | $C_{ds}/pF$ |
| --- | --- | --- | --- | --- | --- | --- |
| 结型 | 0.1~10 | $10^5$ | $>10^7$ | 1~10 | 1~10 | 0.1~1 |
| 绝缘栅型 | 0.1~20 | $10^4$ | $>10^9$ | 1~10 | 1~10 | 0.1~1 |

与  $\dot{I}_{b}$  之比, 因此  $\dot{K}=0$  。根据式(4.2.2)

$$
C _ {\pi} ^ {\prime} \approx C _ {\pi} + (1 + | \dot {K} |) C _ {\mu} = C _ {\pi} + C _ {\mu}
$$

由于  $\dot{I}_{c}=g_{m}\dot{U}_{b'e}, g_{m}=\beta_{0}/r_{b'e}$ ，所以

$$
\dot {\beta} = \frac {I _ {\mathrm{e}}}{I _ {r _ {\mathrm{b} ^ {\prime} \mathrm{e}}} + I _ {C _ {\pi} ^ {\prime}}} = \frac {g _ {\mathrm{m}} U _ {\mathrm{b} ^ {\prime} \mathrm{e}}}{U _ {\mathrm{b} ^ {\prime} \mathrm{e}} \left(\frac {1}{r _ {\mathrm{b} ^ {\prime} \mathrm{e}}} + \mathrm{j} \omega C _ {\pi} ^ {\prime}\right)} = \frac {\beta_ {0}}{1 + \mathrm{j} \omega r _ {\mathrm{b} ^ {\prime} \mathrm{e}} C _ {\pi} ^ {\prime}} \tag {4.2.6}
$$

与式(4.1.5)的形式完全一样，说明  $\dot{\beta}$  的频率响应与低通电路相似。 $f_{\beta}$  为  $\dot{\beta}$  的截止频率，称为共射截止频率。

$$
f _ {\beta} = \frac {1}{2 \pi \tau} = \frac {1}{2 \pi r _ {\mathrm{b'e}} C _ {\pi} ^ {\prime}} \quad (C _ {\pi} ^ {\prime} = C _ {\pi} + C _ {\mu}) \tag {4.2.7}
$$

将其代入式(4.2.6)，得出

$$
\dot {\beta} = \frac {\beta_ {0}}{1 + \mathrm{j} \frac {f}{f _ {\beta}}} \tag {4.2.8}
$$

写出  $\dot{\beta}$  的对数幅频特性与对数相频特性为

$$
\left\{ \begin{array}{l} 2 0 \lg | \dot {\beta} | = 2 0 \lg \beta_ {0} - 2 0 \lg \sqrt {1 + \left(\frac {f}{f _ {\beta}}\right) ^ {2}} \\ \varphi = - \arctan \frac {f}{f _ {\beta}} \end{array} \right. \tag {4.2.9a}
$$

画出  $\dot{\beta}$  的折线化波特图如图 4.2.3 所示，图中  $f_{T}$  是使  $\left|\dot{\beta}\right|$  下降到 1（即 0 dB）时的频率。

令式(4.2.9a)等于0，则 $f=f_{T}$ ，由此可求出 $f_{T}$ 。

$$
2 0 \mathrm{lg} \beta_ {0} - 2 0 \mathrm{lg}   \sqrt {1 + \left(\frac {f _ {\mathrm{T}}}{f _ {\beta}}\right) ^ {2}} = 0 \quad \text {或} \quad \sqrt {1 + \left(\frac {f _ {\mathrm{T}}}{f _ {\beta}}\right) ^ {2}} = \beta_ {0}
$$

因 $f_{T} \gg f_{\beta}$ ，所以

$$
f _ {\mathrm{T}} \approx \beta_ {0} f _ {\beta} \tag {4.2.10}
$$

利用  $\beta$  的表达式, 可以求出  $\dot{\alpha}$  的截止频率

$$
\dot {\alpha} = \frac {\dot {\beta}}{1 + \dot {\beta}} = \frac {\frac {\beta_ {0}}{1 + \mathrm{j} f / f _ {\beta}}}{1 + \frac {\beta_ {0}}{1 + \mathrm{j} f / f _ {\beta}}} = \frac {\beta_ {0}}{1 + \beta_ {0} + \mathrm{j} f / f _ {\beta}} = \frac {\frac {\beta_ {0}}{1 + \beta_ {0}}}{1 + \mathrm{j} \frac {f}{(1 + \beta_ {0}) f _ {\beta}}}
$$

$$
\dot {\alpha} = \frac {\alpha_ {0}}{1 + \mathrm{j} \frac {f}{f _ {\alpha}}} \qquad \left[ f _ {\alpha} = (1 + \beta_ {0}) f _ {\beta} \right] \tag {4.2.11}
$$

$f_{\alpha}$  是使  $\left|\dot{\alpha}\right|$  下降到 70.7%  $\alpha_{0}$  的频率, 称为共基截止频率。式(4.2.11)表明

$$
f _ {\alpha} = (1 + \beta_ {0}) f _ {\beta} \approx f _ {\mathrm{T}} \tag {4.2.12}
$$

可见,共基电路的截止频率远高于共射电路的截止频

![](images/page_215_chart_23.jpg)

<details>
<summary>line</summary>

| \(0\) | \(20lg\beta_{0}\) | 0 |
| --- | --- | --- |
| \(0.1f\beta\) | \(20lg\beta_{0}\) | 0 |
| \(f\beta\) | \(20lg\beta_{0}\) | \(-45{}^{\circ}\) |
| \(10f\beta\) | \(0\) | \(-90{}^{\circ}\) |
</details>

图 4.2.3  $\dot{\beta}$  的波特图

$$
X _ {C _ {\mu} ^ {\prime}} = \frac {\dot {U} _ {\mathrm {b^ {\prime} e}}}{\dot {I} _ {C _ {\mu}}} = \frac {\dot {U} _ {\mathrm {b^ {\prime} e}}}{(1 - \dot {K}) \frac {\dot {U} _ {\mathrm {b^ {\prime} e}}}{X _ {C _ {\mu}}}} = \frac {X _ {C _ {\mu}}}{1 - \dot {K}}
$$

考虑在近似计算时，$\dot{K}$ 取中频时的值，所以 $|\dot{K}| = -\dot{K}$。$X_{C\mu}$ 约为 $X_{C\mu}$ 的 $(1 + |\dot{K} |)$ 分之一，因此

$$
C _ {\mu} ^ {\prime} = (1 - \dot {K}) C _ {\mu} \approx (1 + | \dot {K} |) C _ {\mu} \tag {4.2.1}
$$

$b' - e$  间总电容为

$$
C _ {\pi} ^ {\prime} = C _ {\pi} + C _ {\mu} ^ {\prime} \approx C _ {\pi} + (1 + | \dot {K} |) C _ {\mu} \tag {4.2.2}
$$

用同样的分析方法,可以得出

$$
C _ {\mu} ^ {\prime \prime} = \frac {\dot {K} - 1}{\dot {K}} \cdot C _ {\mu} \tag {4.2.3}
$$

因为 $C_{\pi}^{\prime} \gg C_{\mu}^{\prime \prime}$, 且一般情况下 $C_{\mu}^{\prime \prime}$ 的容抗远大于 $R_{\mathrm{L}}^{\prime}, C_{\mu}^{\prime \prime}$ 中的电流可忽略不计, 所以简化的混合 $\pi$ 模型如图 (c) 所示。

## 三、混合 $\pi$ 模型的主要参数

将简化的混合  $\pi$  模型与简化的 h 参数等效模型相比较, 它们的电阻参数是完全相同的, 从手册中可查得  $r_{bb'}$ , 而

$$
r _ {\mathrm {b^ {\prime} e}} = (1 + \beta_ {0}) \frac {U _ {\mathrm{T}}}{I _ {\mathrm{EQ}}} \tag {4.2.4}
$$

式中  $\beta_{0}$  为低频段晶体管的电流放大系数。虽然利用  $\beta$  和  $g_{m}$  表述的受控关系不同，但是它们所要表述的却是同一个物理量，即

$$
\dot {I} _ {\mathrm{c}} = g _ {\mathrm{m}} \dot {U} _ {\mathrm {b^ {\prime} e}} = \beta_ {0} \dot {I} _ {\mathrm{b}}
$$

由于  $\dot{U}_{b'e} = \dot{I}_{b} r_{b'e}$ ，且  $r_{b'e}$  如式(4.2.4)所示，又由于通常  $\beta_{0} \gg 1$ ，所以

$$
g _ {\mathrm{m}} = \frac {\beta_ {0}}{r _ {\mathrm {b^{\prime} e}}} \approx \frac {I _ {\mathrm{EQ}}}{U _ {\mathrm{T}}} \tag {4.2.5}
$$

在半导体器件手册中可以查得参数 $C_{\mathrm{ob}}, C_{\mathrm{ob}}$ 是晶体管为共基接法且发射极开路时 $\mathrm{c - b}$ 间的结电容，$C_{\mu}$ 近似为 $C_{\mathrm{ob}}$。$C_{\pi}$ 的数值可通过手册给出的特征频率 $f_{\mathrm{T}}$ 和放大电路的静态工作点求解，具体分析见4.2.2节。$\dot{K}$ 是电路的电压放大倍数，可通过计算得到。

## 4.2.2 晶体管电流放大倍数的频率响应

从混合 $\pi$ 等效模型可以看出，管子工作在高频段时，若基极注入的交流电流 $\dot{I}_{\mathrm{b}}$ 的幅值不变，则随着信号频率的升高，$\mathrm{b}' - \mathrm{e}$ 间的电压 $\dot{U}_{\mathrm{b'e}}$ 的幅值将减小，相移将增大；从而使 $\dot{I}_{\mathrm{c}}$ 的幅值随 $|\dot{U}_{\mathrm{b'e}}|$ 线性下降，并产生与 $\dot{U}_{\mathrm{b'e}}$ 相同的相移。可见，在高频段，当信号频率变化时 $\dot{I}_{\mathrm{c}}$ 与 $\dot{I}_{\mathrm{b}}$ 的关系也随之变化，电流放大系数不是常量，$\dot{\beta}$ 是频率的函数。

根据电流放大系数的定义

$$
\dot {\beta} = \frac {\dot {I} _ {\mathrm{c}}}{\dot {I} _ {\mathrm{b}}} \Bigg | _ {U _ {\mathrm{CE}}}
$$

表明  $\dot{\beta}$  是在 c-e 间无动态电压, 即令图 4.2.2(c) 所示电路中 c-e 间电压为零时动态电流  $\dot{I}_{c}$

## 思考题

4.3.1 场效应管栅 - 源等效电容是常量吗？它决定于哪些参数？

## 4.4 单管放大电路的频率响应

利用晶体管和场效应管的高频等效模型,可以分析放大电路的频率响应。本节通过单管放大电路来讲述频率响应的一般分析方法。

## 4.4.1 单管共射放大电路的频率响应

考虑到耦合电容和结电容的影响,图4.4.1(a)所示电路的等效电路如图(b)所示。

![](images/page_217_image_8.jpg)

<details>
<summary>text_image</summary>

Rb
+VCC
Rc
C
+
Rs
+
us
u1
-
RL
uo
-
</details>

(a)

![](images/page_217_image_10.jpg)

<details>
<summary>text_image</summary>

Rs
+
Us
-
b
+
-
Rb
U̇i
Rb
U̇b'e
rbb'
b'
+
-
r b'e
C'π
gm U̇b'e
c
C
+
-
RL
Uo
-
</details>

(b)

图 4.4.1 单管共射放大电路及其等效电路

(a) 共射放大电路 (b) 适应于频率从零到无穷大的交流等效电路

在分析放大电路的频率响应时,为了方便起见,一般将输入信号的频率范围分为中频、低频和高频三个频段。在中频段,极间电容因容抗很大而视为开路,耦合电容(或旁路电容)因容抗很小而视为短路,故不考虑它们的影响;在低频段,应当考虑耦合电容(或旁路电容)的影响,此时极间电容仍视为开路;在高频段,应当考虑极间电容的影响,此时耦合电容(或旁路电容)仍视为短路;根据上述原则,便可得到放大电路在各频段的等效电路,从而得到各频段的放大倍数。

## 一、中频电压放大倍数

在中频电压信号  $\dot{U}_{s}$  作用于电路时，由于  $\frac{1}{\omega C_{\pi}^{\prime}} \gg r_{b'e}, C_{\pi}^{\prime}$  可视为开路；又由于  $\frac{1}{\omega C} \ll R_{L}, C$  可视为短路；因此，图 4.4.1(a) 所示电路的中频等效电路如图 4.4.2 所示。输入电阻  $R_{i} = R_{b} // (r_{bb'} + r_{b'e}) = R_{b} // r_{be}$ ，中频电压放大倍数

$$
\dot {A} _ {\mathrm{usm}} = \frac {\dot {U} _ {\mathrm{o}}}{\dot {U} _ {\mathrm{s}}} = \frac {\dot {U} _ {\mathrm{i}}}{\dot {U} _ {\mathrm{s}}} \cdot \frac {\dot {U} _ {\mathrm {b^{\prime}e}}}{\dot {U} _ {\mathrm{i}}} \cdot \frac {\dot {U} _ {\mathrm{o}}}{\dot {U} _ {\mathrm {b^{\prime}e}}} = \frac {R _ {\mathrm{i}}}{R _ {\mathrm{s}} + R _ {\mathrm{i}}} \cdot \frac {r _ {\mathrm {b^{\prime}e}}}{r _ {\mathrm{be}}} \cdot (- g _ {\mathrm{m}} R _ {\mathrm{L}} ^ {\prime}) \tag {4.4.1}
$$

$$
(R _ {\mathrm{L}} ^ {\prime} = R _ {\mathrm{c}} / / R _ {\mathrm{L}})
$$

电路空载时的中频电压放大倍数为

$$
\dot {A} _ {\mathrm{usm}} = \frac {\dot {U} _ {\mathrm{o}}}{\dot {U} _ {\mathrm{s}}} = \frac {R _ {\mathrm{i}}}{R _ {\mathrm{s}} + R _ {\mathrm{i}}} \cdot \frac {r _ {\mathrm {b^{\prime} e}}}{r _ {\mathrm{be}}} \cdot (- g _ {\mathrm{m}} R _ {\mathrm{c}}) \tag {4.4.2}
$$

![](images/page_218_image_2.jpg)

<details>
<summary>text_image</summary>

Rs
+
Us
-
+
b
rbb'
+
b'
gmÛb'e
Rb
Ui
Ub'e
rb'e
Rc
RL
Uo
+
-
</details>

图 4.4.2 单管共射放大电路的中频等效电路

## 二、低频电压放大倍数

考虑到低频电压信号作用时耦合电容 C 的影响, 图 4.4.1(a) 所示电路的低频等效电路如图 4.4.3(a) 所示。将受控电流源  $g_{m}\dot{U}_{b'e}$  与  $R_{c}$  进行等效变换如图 (b) 所示,  $\dot{U}'_{o}$  是空载时的输出电压, 电容 C 与负载电阻  $R_{L}$  组成了如图 4.1.1(a) 所示的高通电路。

![](images/page_218_image_6.jpg)

图 4.4.3 单管共射放大电路的低频等效电路

(a) 低频等效电路 (b) 输出回路的等效电路

低频电压放大倍数为

$$
\dot {A} _ {\mathrm{usl}} = \frac {\dot {U} _ {\mathrm{o}}}{\dot {U} _ {\mathrm{s}}} = \frac {\dot {U} _ {\mathrm{o}} ^ {\prime}}{\dot {U} _ {\mathrm{s}}} \cdot \frac {\dot {U} _ {\mathrm{o}}}{\dot {U} _ {\mathrm{o}} ^ {\prime}}
$$

将式(4.4.2)代入上式

$$
\dot {A} _ {\mathrm{usl}} = \frac {R _ {\mathrm{i}}}{R _ {\mathrm{s}} + R _ {\mathrm{i}}} \cdot \frac {r _ {\mathrm {b^ {\prime} e}}}{r _ {\mathrm{be}}} \cdot (- g _ {\mathrm{m}} R _ {\mathrm{c}}) \cdot \frac {R _ {\mathrm{L}}}{R _ {\mathrm{c}} + \frac {1}{\mathrm{j} \omega C} + R _ {\mathrm{L}}}
$$

将上式的分子与分母同除以 $(R_{\mathrm{c}}+R_{\mathrm{L}})$ 便可得到

$$
\dot {A} _ {\mathrm{usl}} = \frac {R _ {\mathrm{i}}}{R _ {\mathrm{s}} + R _ {\mathrm{i}}} \cdot \frac {r _ {\mathrm {b^{\prime} e}}}{r _ {\mathrm{be}}} \cdot (- g _ {\mathrm{m}} R _ {\mathrm{L}} ^ {\prime}) \cdot \frac {\mathrm{j} \omega (R _ {\mathrm{c}} + R _ {\mathrm{L}}) C}{1 + \mathrm{j} \omega (R _ {\mathrm{c}} + R _ {\mathrm{L}}) C}
$$

与式(4.4.1)比较,得出

$$
\dot {A} _ {\mathrm{usl}} = \dot {A} _ {\mathrm{usm}} \cdot \frac {\mathrm{j} \frac {f}{f _ {\mathrm{L}}}}{1 + \mathrm{j} \frac {f}{f _ {\mathrm{L}}}} = \dot {A} _ {\mathrm{usm}} \cdot \frac {1}{1 + \frac {f _ {\mathrm{L}}}{\mathrm{j} f}} \tag {4.4.3}
$$

其中 $f_{L}$ 为下限频率,其表达式为

$$
f _ {\mathrm{L}} = \frac {1}{2 \pi (R _ {\mathrm{c}} + R _ {\mathrm{L}}) C} \tag {4.4.4}
$$

式(4.4.4)中的 $(R_{\mathrm{c}}+R_{\mathrm{L}})C$ 正是C所在回路的时间常数,它等于从电容C两端向外看的等效总

电阻乘以 C。

根据式(4.4.3)，单管共射放大电路的对数幅频特性及相频特性的表达式为

$$
\left\{ \begin{array}{l} 2 0 \lg | \dot {A} _ {\mathrm{usl}} | = 2 0 \lg | \dot {A} _ {\mathrm{usm}} | + 2 0 \lg \frac {\frac {f}{f _ {\mathrm{L}}}}{\sqrt {1 + \left(\frac {f}{f _ {\mathrm{L}}}\right) ^ {2}}} \\ \varphi = - 1 8 0 ^ {\circ} + \left(9 0 ^ {\circ} - \arctan \frac {f}{f _ {\mathrm{L}}}\right) = - 9 0 ^ {\circ} - \arctan \frac {f}{f _ {\mathrm{L}}} \end{array} \right. \tag {4.4.5a}
$$

式(4.4.5b)中的  $-180^{\circ}$  表示中频段时  $\dot{U}_{o}$  与  $\dot{U}_{s}$  反相。因电抗元件引起的相移称为附加相移，因而式(4.4.5b)表明低频段最大附加相移为  $+90^{\circ}$ 。

## 三、高频电压放大倍数

考虑到高频信号作用时  $C_{\pi}^{\prime}$  的影响, 图 4.4.1(a) 所示电路的高频等效电路如图 4.4.4(a) 所示。

利用戴维宁定理，从  $C_{\pi}^{\prime}$  两端向左看，电路可等效成图(b)所示电路，R 和  $C_{\pi}^{\prime}$  构成如图4.1.2(a)所示的低通电路。通过图(c)所示电路可以求出  $b^{\prime}-e$  间的开路电压及等效内阻 R 的表达式。

$$
\dot {U} _ {\mathrm{s}} ^ {\prime} = \frac {r _ {\mathrm {b^ {\prime} e}}}{r _ {\mathrm{be}}} \cdot \dot {U} _ {\mathrm{i}} = \frac {r _ {\mathrm {b^ {\prime} e}}}{r _ {\mathrm{be}}} \cdot \frac {R _ {\mathrm{i}}}{R _ {\mathrm{s}} + R _ {\mathrm{i}}} \cdot \dot {U} _ {\mathrm{s}} \tag {4.4.6}
$$

$$
R = r _ {\mathrm {b^ {\prime} e}} / / (r _ {\mathrm {bb^ {\prime}}} + R _ {\mathrm{s}} / / R _ {\mathrm{b}}) \tag {4.4.7}
$$

![](images/page_219_image_11.jpg)

<details>
<summary>text_image</summary>

Rs
+
Us
-
b
rbb'
b'
Rb
rb'e
C'π
gmÛb'e
Rc
RL
Uo
+
</details>

(a)

![](images/page_219_image_13.jpg)

<details>
<summary>chemical</summary>

Electrical circuit diagram with resistor and capacitor components labeled R, b', C'π, and Ũ'
</details>

(b)

![](images/page_219_image_15.jpg)

<details>
<summary>text_image</summary>

Rs
+
Us
-
b
rbb'
b'
+
Ui
Rb
rb'e
Us'
C'π
</details>

(c)

图 4.4.4 单管共射放大电路的高频等效电路

(a) 高频等效电路 (b) 输入回路的等效变换 (c) 输入回路

因为  $b^{\prime}-e$  间电压  $\dot{U}_{b^{\prime}e}$  与输出电压  $\dot{U}_{o}$  的关系没变, 所以高频电压放大倍数

$$
\dot {A} _ {\mathrm{ush}} = \frac {\dot {U} _ {\mathrm{o}}}{\dot {U} _ {\mathrm{s}}} = \frac {\dot {U} _ {\mathrm{s}} ^ {\prime}}{\dot {U} _ {\mathrm{s}}} \cdot \frac {\dot {U} _ {\mathrm {b^ {\prime} e}}}{\dot {U} _ {\mathrm{s}} ^ {\prime}} \cdot \frac {\dot {U} _ {\mathrm{o}}}{\dot {U} _ {\mathrm {b^ {\prime} e}}} = \frac {R _ {\mathrm{i}}}{R _ {\mathrm{s}} + R _ {\mathrm{i}}} \cdot \frac {r _ {\mathrm {b^ {\prime} e}}}{r _ {\mathrm{be}}} \cdot \frac {\frac {1}{\mathrm{j} \omega R C _ {\pi} ^ {\prime}}}{1 + \frac {1}{\mathrm{j} \omega R C _ {\pi} ^ {\prime}}} \cdot (- g _ {\mathrm{m}} R _ {\mathrm{L}} ^ {\prime})
$$

将上式与式(4.4.1)比较,可得

$$
\dot {A} _ {u s h} = \dot {A} _ {u s m} \cdot \frac {1}{1 + j \omega R C}
$$

令 $f_{\mathrm{H}} = \frac{1}{2\pi RC_{\pi}^{\prime}}, RC_{\pi}^{\prime}$ 是 $C_{\pi}^{\prime}$ 所在回路的时间常数，因而

$$
\dot {A} _ {u s h} = \dot {A} _ {u s m} \cdot \frac {1}{1 + \mathrm{j} \frac {f}{f _ {\mathrm{H}}}} \tag {4.4.8}
$$

$\dot{A}_{ush}$ 的对数幅频特性与相频特性的表达式为

$$
\left\{ \begin{array}{l} 2 0 \lg | \dot {A} _ {\mathrm{ush}} | = 2 0 \lg | \dot {A} _ {\mathrm{usm}} | - 2 0 \lg \sqrt {1 + \left(\frac {f}{f _ {\mathrm{H}}}\right) ^ {2}} \\ \varphi = - 1 8 0 ^ {\circ} - \arctan \frac {f}{f _ {\mathrm{H}}} \end{array} \right. \tag {4.4.9a}
$$

式(4.4.9b)表明,在高频段,由 $C_{\pi}^{\prime}$ 引起的最大附加相移为 $-90^{\circ}$ 。

## 四、波特图

综上所述,若考虑耦合电容及结电容的影响,对于频率从零到无穷大的输入电压,电压放大倍数的表达式应为

$$
\dot {A} _ {u s} = \dot {A} _ {u s m} \cdot \frac {\mathrm{j} \frac {f}{f _ {\mathrm{L}}}}{\left(1 + \mathrm{j} \frac {f}{f _ {\mathrm{L}}}\right) \left(1 + \mathrm{j} \frac {f}{f _ {\mathrm{H}}}\right)} = \dot {A} _ {u s m} \cdot \frac {1}{\left(1 + \frac {f _ {\mathrm{L}}}{\mathrm{j} f}\right) \left(1 + \mathrm{j} \frac {f}{f _ {\mathrm{H}}}\right)} \tag {4.4.10}
$$

当 $f_{\mathrm{L}} \ll f \ll f_{\mathrm{H}}$ 时，$f_{\mathrm{L}} / f$ 趋于零，$f / f_{\mathrm{H}}$ 也趋于零，因而式(4.4.10)近似为 $\dot{A}_{us} \approx \dot{A}_{usm}$，即 $\dot{A}_{us}$ 为中频电压放大倍数，其表达式为式(4.4.1)。当 $f$ 接近 $f_{\mathrm{L}}$ 时，必有 $f \ll f_{\mathrm{H}}, f / f_{\mathrm{H}}$ 趋于零，因而式(4.4.10)近似为 $\dot{A}_{us} \approx \dot{A}_{usl}$，即 $\dot{A}_{us}$ 为低频电压放大倍数，其表达式为式(4.4.3)。当 $f$ 接近 $f_{\mathrm{H}}$ 时，必有 $f \gg f_{\mathrm{L}}, f_{\mathrm{L}} / f$ 趋于零，因而式(4.4.10)近似为 $\dot{A}_{us} \approx \dot{A}_{ush}$，即 $\dot{A}_{us}$ 为高频电压放大倍数，其表达式为式(4.4.8)。根据式(4.4.10)，或者式(4.4.2)、(4.4.5)、(4.4.9)，可画出图4.4.1(a)所示单管放大电路的折线化波特图，如图4.4.5所示。

![](images/page_220_image_12.jpg)

图 4.4.5 单管共射放大电路的波特图

从以上分析可知,式(4.4.10)可以全面表示任何频段的电压放大倍数,而且上限频率和下限频率均可表示为 $\frac{1}{2\pi\tau},\tau$ 分别是极间电容 $C_{\pi}^{\prime}$ 和耦合电容C所在回路的时间常数, $\tau$ 是从电容两端向外看的总等效电阻与相应的电容之积。可见,求解上、下限截止频率的关键是正确求出回路的等效电阻。

【例 4.4.1】 在图 4.4.1(a) 所示电路中, 已知  $V_{CC} = 15 \, V, R_{s} = 1 \, k\Omega, R_{b} = 20 \, k\Omega, R_{c} = R_{L} = 5 \, k\Omega, C = 5 \, \muF$ ; 晶体管的  $U_{BEQ} = 0.7 \, V, r_{bb'} = 100 \, \Omega, \beta = 100, f_{\beta} = 0.5 \, MHz, C_{ob} = 5 \, pF$ 。

试估算电路的截止频率 $f_{H}$ 和 $f_{L}$，并画出 $\dot{A}_{us}$ 的波特图。

解:(1) 求解 Q 点

$$
I _ {\mathrm{BQ}} = \frac {V _ {\mathrm{CC}} - U _ {\mathrm{BEQ}}}{R _ {\mathrm{b}}} - \frac {U _ {\mathrm{BEQ}}}{R _ {\mathrm{s}}} = \left(\frac {1 5 - 0 . 7}{2 0} - \frac {0 . 7}{1}\right) \mathrm{mA} = 0. 0 1 5 \mathrm{mA}
$$

$$
I _ {\mathrm{CQ}} = \beta I _ {\mathrm{BQ}} = (1 0 0 \times 0. 0 1 5) \mathrm{mA} = 1. 5 \mathrm{mA}
$$

$$
U _ {\mathrm{CEQ}} = V _ {\mathrm{CC}} - I _ {\mathrm{CQ}} R _ {\mathrm{e}} = (1 5 - 1. 5 \times 5) \mathrm{V} = 7. 5 \mathrm{V}
$$

可见,放大电路的 Q 点合适。

(2) 求解混合  $\pi$  模型中的参数

$$
r _ {\mathrm {b^{\prime} e}} = (1 + \beta) \frac {U _ {\mathrm{T}}}{I _ {\mathrm{EQ}}} = \frac {U _ {\mathrm{T}}}{I _ {\mathrm{BQ}}} = \frac {2 6}{0 . 0 1 5} \Omega \approx 1 7 3 3 \Omega
$$

根据式(4.2.7)

$$
C _ {\pi} = \frac {1}{2 \pi r _ {\mathrm {b^{\prime} o}} f _ {\beta}} - C _ {\mu} \approx \frac {1}{2 \pi r _ {\mathrm {b^{\prime} o}} f _ {\beta}} - C _ {\mathrm{ob}} = \left(\frac {1 0 ^ {1 2}}{2 \pi \times 1 7 3 3 \times 5 \times 1 0 ^ {5}} - 5\right) \mathrm{pF} \approx 1 7 8 \mathrm{pF}
$$

$$
g _ {\mathrm{m}} = \frac {I _ {\mathrm{EQ}}}{U _ {\mathrm{T}}} \approx \frac {1 . 5}{2 6} \mathrm{S} \approx 0. 0 5 7 7 \mathrm{S}
$$

$$
\dot {K} = \frac {\dot {U} _ {\mathrm{ce}}}{\dot {U} _ {\mathrm{be}}} = - g _ {\mathrm{m}} (R _ {\mathrm{c}} / / R _ {\mathrm{L}}) \approx - 0. 0 5 7 7 \times 2 5 0 0 \approx - 1 4 4
$$

$$
C _ {\pi} ^ {\prime} = C _ {\pi} + (1 - \dot {K}) C _ {\mu} \approx (1 7 8 + 1 4 4 \times 5) \mathrm{pF} = 8 9 8 \mathrm{pF}
$$

(3) 求解中频电压放大倍数

$$
r _ {\mathrm{be}} = r _ {\mathrm {b b ^ {\prime}}} + r _ {\mathrm {b^ {\prime} e}} \approx (1 0 0 + 1 7 3 3) \Omega \approx 1. 8 3 \mathrm{k} \Omega
$$

$$
R _ {\mathrm{i}} = R _ {\mathrm{b}} / / r _ {\mathrm{be}} \approx \frac {2 0 \times 1 . 8 3}{2 0 + 1 . 8 3} \mathrm{k} \Omega \approx 1. 6 8 \mathrm{k} \Omega
$$

$$
\dot {A} _ {u s m} = \frac {\dot {U} _ {\mathrm{o}}}{\dot {U} _ {\mathrm{s}}} = \frac {R _ {\mathrm{i}}}{R _ {\mathrm{s}} + R _ {\mathrm{i}}} \cdot \frac {r _ {\mathrm {b^ {\prime} e}}}{r _ {\mathrm{be}}} \cdot (- g _ {\mathrm{m}} R _ {\mathrm{L}}) \approx \frac {1 . 6 8}{1 + 1 . 6 8} \times \frac {1 . 7 3}{1 . 8 3} \times (- 1 4 4) \approx - 8 5
$$

(4) 求解  $f_{H}$  和  $f_{L}$

$$
f _ {\mathrm{H}} = \frac {1}{2 \pi [ r _ {\mathrm {b^ {'} e}} / / (r _ {\mathrm {bb^ {'}}} + R _ {\mathrm{s}} / / R _ {\mathrm{b}}) ] C _ {\pi} ^ {\prime}}
$$

因为 $R_{\mathrm{s}} \ll R_{\mathrm{b}}$ ，所以

$$
\begin{array}{l} f _ {\mathrm{H}} = \frac {1}{2 \pi [ r _ {\mathrm {b^{\prime} e}} / / (r _ {\mathrm {bb^{\prime}}} + R _ {\mathrm{s}}) ] C _ {\pi} ^ {\prime}} \\ \approx \frac {1}{2 \pi \times \frac {1 7 3 3 \times (1 0 0 + 1 0 0 0)}{1 7 3 3 + (1 0 0 + 1 0 0 0)} \times 8 9 8 \times 1 0 ^ {- 1 2}} \mathrm{Hz} \\ \end{array}
$$

$$
\begin{array}{l} \approx 2 6 3 0 0 0 \mathrm{Hz} \\ = 2 6 3 \mathrm{kHz} \\ f _ {\mathrm{L}} = \frac {1}{2 \pi (R _ {\mathrm{c}} + R _ {\mathrm{L}}) C} = \frac {1}{2 \pi (5 \times 1 0 ^ {3} + 5 \times 1 0 ^ {3}) \times 5 \times 1 0 ^ {- 6}} \mathrm{Hz} \approx 3. 2 \mathrm{Hz} \\ \end{array}
$$

(5) 画  $\dot{A}_{us}$  的波特图

根据式(4.4.10)及以上的计算结果可得

$$
\dot {A} _ {u s} = \dot {A} _ {u s m} \cdot \frac {\mathrm{j} \frac {f}{f _ {\mathrm{L}}}}{\left(1 + \mathrm{j} \frac {f}{f _ {\mathrm{L}}}\right) \left(1 + \mathrm{j} \frac {f}{f _ {\mathrm{H}}}\right)} \approx \frac {- 8 5 \times \left(\mathrm{j} \frac {f}{3 . 2}\right)}{\left(1 + \mathrm{j} \frac {f}{3 . 2}\right) \left(1 + \mathrm{j} \frac {f}{2 6 3 \times 1 0 ^ {3}}\right)}
$$

$20\lg\left|\dot{A}_{usm}\right| \approx 38.6\mathrm{~dB}$ ，画出 $\dot{A}_{us}$ 的波特图如图4.4.6所示。

![](images/page_222_chart_7.jpg)

<details>
<summary>line</summary>

| Frequency (f/Hz) | Magnitude (dB) | Phase \((\phi)\) |
| --- | --- | --- |
| 3.2 | 40 | -180 |
| 263x10^3 | 40 | -180 |
| f_H | 40 | -225 |
| ~10^6 | -20 | -270 |
</details>

图 4.4.6 例 4.4.1 图

## 4.4.2 单管共源放大电路的频率响应

对于图 4.4.7(a) 所示共源放大电路, 考虑到极间电容和耦合电容的影响, 其动态等效电路如图(b) 所示。

![](images/page_222_image_11.jpg)

图 4.4.7 单管共源放大电路及其等效电路

（a）共源放大电路 （b）适应于频率从零到无穷大的交流等效电路

在中频段, $C'_{gs}$ 开路,C短路,因而中频电压放大倍数

$$
\dot {A} _ {\mathrm{um}} = \frac {\dot {U} _ {\mathrm{o}}}{\dot {U} _ {\mathrm{i}}} = \frac {- g _ {\mathrm{m}} \dot {U} _ {\mathrm{gs}} (R _ {\mathrm{d}} / / R _ {\mathrm{L}})}{\dot {U} _ {\mathrm{gs}}} = - g _ {\mathrm{m}} R _ {\mathrm{L}} ^ {\prime} \tag {4.4.11}
$$

在高频段， $C$ 短路，考虑 $C_{\mathrm{gs}}^{\prime}$ 的影响，它所在回路的时间常数 $\tau = R_{\mathrm{g}}C_{\mathrm{gs}}^{\prime}$，因而上限频率为

$$
f _ {\mathrm{H}} = \frac {1}{2 \pi R _ {\mathrm{g}} C _ {\mathrm{gs}} ^ {\prime}} \tag {4.4.12}
$$

在低频段， $C_{\mathrm{gs}}^{\prime}$ 开路，考虑 $C$ 的影响，它所在回路的时间常数 $\tau = (R_{\mathrm{d}} + R_{\mathrm{L}})C$ ，因而下限频率为

$$
f _ {\mathrm{L}} = \frac {1}{2 \pi (R _ {\mathrm{d}} + R _ {\mathrm{L}}) C} \tag {4.4.13}
$$

写出 $\dot{A}_{u}$ 的表达式

$$
\dot {A} _ {u} = \dot {A} _ {u m} \cdot \frac {\mathrm{j} \frac {f}{f _ {\mathrm{L}}}}{\left(1 + \mathrm{j} \frac {f}{f _ {\mathrm{L}}}\right) \left(1 + \mathrm{j} \frac {f}{f _ {\mathrm{H}}}\right)} \tag {4.4.14}
$$

式(4.4.14)与式(4.4.10)形式上相同,若画出 $\dot{A}_{u}$ 的波特图,则与图4.4.5相似,此处从略。

## 4.4.3 放大电路频率响应的改善和增益带宽积

为了改善单管放大电路的低频特性,需加大耦合电容及其回路电阻,以增大回路时间常数,从而降低下限频率。然而这种改善是很有限的,因此在信号频率很低的使用场合,应考虑采用直接耦合方式。

为了改善单管放大电路的高频特性,需减小  $b^{\prime}-e$  间等效电容  $C_{\pi}^{\prime}$  或 g-s 间等效电容  $C_{gs}^{\prime}$  及其回路电阻,以减小回路时间常数,从而增大上限频率。

根据式(4.2.2)， $C_{\pi}^{\prime} = C_{\pi} + (1 + |\dot{K}|)C_{\mu}\approx C_{\pi} + (1 + g_{\mathrm{m}}R_{\mathrm{L}}^{\prime})C_{\mu}$ ；而根据式（4.4.1），中频电压放大倍数 $\dot{A}_{usm} = \frac{R_i}{R_s + R_i}\cdot \frac{r_{b'e}}{r_{be}}\cdot (-g_mR_L')$ ；因此，为减小 $C_\pi^\prime$ 需减小 $g_{\mathrm{m}}R_{\mathrm{L}}^{\prime}$ ，而减小 $g_{\mathrm{m}}R_{\mathrm{L}}^{\prime}$ 必然使$|\dot{A}_{usm}|$ 减小。可见， $f_{\mathrm{H}}$ 的提高与 $\mid \dot{A}_{usm}\mid$ 的增大是相互矛盾的。

对于大多数放大电路， $f_{H} \gg f_{L}$ ，因而通频带 $f_{bw} = f_{H} - f_{L} \approx f_{H}$ 。也就是说， $f_{H}$ 与 $| \dot{A}_{usm} |$ 的矛盾就是带宽与增益的矛盾，即增益提高时，必使带宽变窄，增益减小时，必使带宽变宽。为了综合考察这两方面的性能，引入一个新的参数“带宽增益积”。

根据式(4.4.1)和式(4.4.7)，图4.4.1(a)所示单管共射放大电路的带宽增益积

$$
\left| \dot {A} _ {\mathrm{usm}} f _ {\mathrm{bw}} \right| \approx \left| \dot {A} _ {\mathrm{usm}} f _ {\mathrm{H}} \right| = \frac {R _ {\mathrm{i}}}{R _ {\mathrm{s}} + R _ {\mathrm{i}}} \cdot \frac {r _ {\mathrm {b^{\prime} e}}}{r _ {\mathrm{be}}} \cdot g _ {\mathrm{m}} R _ {\mathrm{L}} ^ {\prime} \cdot \frac {1}{2 \pi \left[ r _ {\mathrm {b^{\prime} e}} / / (r _ {\mathrm {bb^{\prime}}} + R _ {\mathrm{s}} / / R _ {\mathrm{b}}) \right] C _ {\pi} ^ {\prime}}
$$

为使问题简单化，设电路中 $R_{\mathrm{b}} \gg r_{\mathrm{be}}$ ，则 $R_{\mathrm{i}} \approx r_{\mathrm{be}}$ ；设 $R_{\mathrm{b}} \gg R_{\mathrm{s}}$ ，则 $R_{\mathrm{b}} / / R_{\mathrm{s}} \approx R_{\mathrm{s}}$ ；设 $(1 + g_{\mathrm{m}}R_{\mathrm{L}}^{\prime})C_{\mu} \gg C_{\pi}$ ，且 $g_{\mathrm{m}}R_{\mathrm{L}}^{\prime} \gg 1$ ，则 $C_{\pi}^{\prime} \approx g_{\mathrm{m}}R_{\mathrm{L}}^{\prime}C_{\mu}$ 。在假设条件均成立的条件下，上式将变换成

$$
\begin{array}{l} \mid \dot {A} _ {\mathrm{usm}} f _ {\mathrm{bw}} \mid \approx \frac {r _ {\mathrm{be}}}{R _ {\mathrm{s}} + r _ {\mathrm{be}}} \cdot \frac {r _ {\mathrm {b^{\prime} e}}}{r _ {\mathrm{be}}} \cdot g _ {\mathrm{m}} R _ {\mathrm{L}} ^ {\prime} \cdot \frac {1}{2 \pi [ r _ {\mathrm {b^{\prime} e}} / / (r _ {\mathrm {bb^ {\prime}}} + R _ {\mathrm{s}}) ] g _ {\mathrm{m}} R _ {\mathrm{L}} ^ {\prime} C _ {\mu}} \\ = \frac {r _ {\mathrm{b} ^ {\prime} \mathrm{e}}}{R _ {\mathrm{s}} + r _ {\mathrm{be}}} \cdot \frac {1}{2 \pi \cdot \frac {r _ {\mathrm{b} ^ {\prime} \mathrm{e}} \cdot (r _ {\mathrm{bb} ^ {\prime}} + R _ {\mathrm{s}})}{r _ {\mathrm{b} ^ {\prime} \mathrm{e}} + (r _ {\mathrm{bb} ^ {\prime}} + R _ {\mathrm{s}})} \cdot C _ {\mu}} \\ \end{array}
$$