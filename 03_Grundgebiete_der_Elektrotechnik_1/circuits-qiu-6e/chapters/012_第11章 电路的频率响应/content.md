# 第11章 电路的频率响应

原始 PDF 第 285–304 页。

# 第十一章

# 电路的频率响应

![](../../raw/pages_0257-0288/images/page_284_image_2.jpg)

![](../../raw/pages_0257-0288/images/page_284_image_3.jpg)

## 导读

由于电路中存在着电感和电容,当电路中正弦激励源的频率变化时,电路中的感抗、容抗将跟随频率变化,从而导致电路的电压电流亦跟随频率变化。此外,电路和系统还可能遭到外部的各种频率电磁信号的干扰,如雷电或太阳风暴对电路和系统的袭击而造成的破坏。

电路和系统的工作状态跟随频率而变化的现象,称为电路和系统的频率特性,又称频率响应。通常采用网络函数来描述电路和系统的频率特性。谐振是线性电路在某些特定频率时的一种物理现象,电路发生谐振时,使得电路某一部分呈现出纯电阻,并往往在储能元件中产生过电压或过电流。

所以,对电路系统的频率特性和谐振的分析研究是正弦稳态电路分析的重要组成部分。

## §11-1 网络函数

由于电路和系统中存在着电感和电容,当电路中激励源的频率变化时,电路中的感抗、容抗将跟随频率变化,从而导致电路的工作状态亦跟随频率变化。当频率的变化超出一定的范围时,电路将偏离正常的工作范围,并可能导致电路失效,甚至使电路遭到损坏。此外,电路和系统还可能遭到外部的各种频率的电磁干扰,如雷电或太阳风暴对电路和系统的袭击而造成的破坏,所以,对电路和系统的频率特性的分析研究就显得格外重要。

电路和系统的工作状态跟随频率而变化的现象,称为电路和系统的频率特性,又称频率响应。通常是采用单输入(一个激励变量)-单输出(一个输出变量)的方式,在输入变量和输出变量之间建立函数关系,来描述电路的频率特性,这一函数关系就称为电路和系统的网络函数。本章仅对正弦稳态电路的频率特性作初步分析和研究。

电路在一个正弦电源激励下稳定时,各部分的响应都是同频率的正弦量,通过正弦

---

262

第十一章 电路的频率响应

量的相量,网络函数  $H(j\omega)$  定义为

$$
H (\mathrm{j} \omega) {\stackrel {\mathrm{def}} {=}} \frac {\dot {R} _ {k} (\mathrm{j} \omega)}{\dot {E} _ {\mathrm{sj}} (\mathrm{j} \omega)}
$$

此式定义的网络函数是描述正弦稳态下响应与激励之间的一种关系。式中 $\dot{R}_k(\mathrm{j}\omega)$ 为输出端口 $k$ 的响应，为电压相量 $\dot{U}_k(\mathrm{j}\omega)$ 或电流相量 $\dot{I}_k(\mathrm{j}\omega);\dot{E}_{sj}(\mathrm{j}\omega)$ 为输入端口 $j$ 的输入变量（正弦激励），为电压源相量 $\dot{U}_{sj}(\mathrm{j}\omega)$ 或电流源相量 $\dot{I}_{sj}(\mathrm{j}\omega)$ 。显然，网络函数有多种类型，当 $k = j$ 时（同一端口），网络函数就是第九章 §9-1 中定义的阻抗 $Z\left(\frac{\dot{U}_k}{\dot{I}_{sk}}\right)$ 或导纳 $Y\left(\frac{\dot{I}_k}{\dot{U}_{sk}}\right)$，称为驱动点阻抗或导纳。当 $k \neq j$ 时，即不同端口，统称为转移函数，分别为转移阻抗 $\left(\frac{\dot{U}_k}{\dot{I}_{sj}}\right)$、转移电流比 $\left(\frac{\dot{I}_k}{\dot{I}_{sj}}\right)$、转移导纳 $\left(\frac{\dot{I}_k}{\dot{U}_{sj}}\right)$ 和转移电压比 $\left(\frac{\dot{U}_k}{\dot{U}_{sj}}\right)$。

网络函数不仅与电路的结构、参数值有关，还与输入、输出变量的类型以及端口对的相互位置有关。这犹如从不同“窗口”来分析研究网络的频率特性，可以从不同角度寻找电路比较优越的频率特性和电路工作的最佳频域范围。网络函数是网络性质的一种体现，与输入、输出幅值无关。

网络函数是一个复数,它的频率特性分为两个部分。它的模(值) $|H(j\omega)|$ 是两个正弦量的有效值(或振幅)的比值,它与频率的关系 $|H(j\omega)|-\omega$ 称为幅频特性。它的幅角 $\varphi(j\omega)=\arg[H(j\omega)]$ 是两个同频正弦量的相位差(又称相移),它与频率的关系 $\varphi(j\omega)-\omega$ 称为相频特性。这两种特性与频率的关系,都可以在图上用曲线表示,称为网络的频率响应曲线。即幅频响应和相频响应曲线。

网络函数可以用相量法中任一分析求解方法获得。

例11-1 求图11-1所示电路的网络函数 $\frac{\dot{I}_2}{\dot{U}_s}$ 和 $\frac{\dot{U}_L}{\dot{U}_s}$。

![](../../raw/pages_0257-0288/images/page_285_image_10.jpg)

<details>
<summary>text_image</summary>

jω
+   jω
-   +
ÛL
-   Ê2
Üs 2 Ω 2 Ω
-   Ê1 2 Ω
-   Ê2
</details>

图11-1 例11-1图

解 列网孔方程解电流  $\dot{I}_{2}$

$$
(2 + \mathrm{j} \omega) \dot {I} _ {1} - 2 \dot {I} _ {2} = \dot {U} _ {\mathrm{a}}
$$

---

§ 11-2 RLC 串联电路的谐振

263

$$
- 2 \dot {I} _ {1} + (4 + \mathrm{j} \omega) \dot {I} _ {2} = 0
$$

解得电流  $\dot{I}_{2}$  为

$$
\dot {I} _ {2} = \frac {2 \dot {U} _ {\mathrm{s}}}{4 + (\mathrm{j} \omega) ^ {2} + \mathrm{j} 6 \omega}
$$

网络函数分别为

$$
\frac {\dot {I} _ {2}}{\dot {U} _ {\mathrm{s}}} = \frac {2}{4 - \omega^ {2} + \mathrm{j} 6 \omega} (\text {转移导纳})
$$

$$
\frac {\dot {U} _ {L}}{\dot {U} _ {\mathrm{s}}} = \frac {\mathrm{j} 2 \omega}{4 - \omega^ {2} + \mathrm{j} 6 \omega} (\text {电压比})
$$

本例也可以求得 $\frac{\dot{I}_1}{\dot{U}_s}$ (驱动点导纳)。如果将 $\dot{U}_s$ 改为 $\dot{I}_s$，即可求得其他形式的网络函数。

以网络函数中 $(\mathrm{j}\omega)$ 的最高次方的次数来定义网络函数的阶数,如本例为二阶(与网络的阶数相同)。一旦获得端口对的网络函数,也就能求得网络在任意正弦输入时的端口正弦响应,即有

$$
\dot {U} _ {k} (\text {或} \dot {I} _ {k}) = H (\mathrm{j} \omega) \dot {U} _ {\mathrm{sj}} (\text {或} \dot {I} _ {\mathrm{sj}})
$$

网络函数等于单位激励( $\dot{U}_{sj}$  或  $\dot{I}_{sj}$  为 1 单位量)的响应。

## §11-2 RLC 串联电路的谐振

图 11-2 所示为 RLC 串联电路, 在可变频的正弦电压源  $u_{s}$  激励下, 由于感抗、容抗随频率变动, 所以, 电路中的电压、电流响应亦随频率变动。本节将首先分析研究工程上特别关注的谐振状态。根据相量法, 电路的输入阻抗  $Z(j\omega)$  可表示为

$$
Z (\mathrm{j} \omega) = R + \mathrm{j} \left(\omega L - \frac {1}{\omega C}\right)
$$

频率特性表示为

$$
\varphi (\mathrm{j} \omega) = \arctan \left(\frac {\omega L - \frac {1}{\omega C}}{R}\right)
$$

$$
\mid Z (\mathrm{j} \omega) \mid = \frac {R}{\cos [ \varphi (\mathrm{j} \omega) ]}
$$

![](../../raw/pages_0257-0288/images/page_286_image_18.jpg)

<details>
<summary>text_image</summary>

i
R
L
us
C
</details>

图 11-2 RLC 串联电路

可以看出,由于串联电路中同时存在着电感 L 和电容 C,两者的频率特性不仅相反(感抗与  $\omega$  成正比,而容抗与  $\omega$  成反比),而且直接相减(电抗角差  $180^{\circ}$ )。可以肯定,一定存在一个角频率  $\omega_{0}$ ,使感抗和容抗相互完全抵消,即  $X(j\omega_{0})=0$ 。因此,阻抗  $Z(j\omega)$  以  $\omega_{0}$  为中心,在全频域内随频率变动的情况分为 3 个频区,描述如下:

![](../../raw/pages_0257-0288/images/page_286_image_21.jpg)

RLC 串联电路的谐振

---

264

第十一章 电路的频率响应

$$
\omega <   \omega_ {0}
$$

$$
X (\mathrm{j} \omega) <   0, \quad \varphi (\mathrm{j} \omega) <   0
$$

容性区

$$
R <   \mid Z (\mathrm{j} \omega) \mid
$$

$$
\text {且} \lim _ {\omega \to 0} \mid Z (\mathrm{j} \omega) \mid = \infty
$$

$$
\omega = \omega_ {0}
$$

$$
X (\mathrm{j} \omega) = 0, \quad \varphi (\mathrm{j} \omega) = 0
$$

电阻性

$$
Z (\mathrm{j} \omega_ {0}) = R
$$

$$
\omega > \omega_ {0}
$$

$$
X (\mathrm{j} \omega) > 0, \quad \varphi (\mathrm{j} \omega) > 0
$$

感性区

$$
R <   | Z (\mathrm{j} \omega) |
$$

$$
\text {且} \lim _ {\omega \to \infty} | Z (\mathrm{j} \omega) | = \infty
$$

阻抗随频率变化的频响曲线如图 11-3 所示。

当  $\omega=\omega_{0}$  时,  $X(j\omega_{0})=0$ , 电路的工作状况将出现一些重要的特征, 现分述如下:

(1) $\varphi(\mathrm{j}\omega_0) = 0$，所以 $\dot{I}(\mathrm{j}\omega_0)$ 与 $\dot{U}_{\mathrm{s}}(\mathrm{j}\omega_0)$ 同相，工程上将电路的这一特殊状态定义为谐振，由于是在 $RLC$ 串联电路中发生的谐振，又常称为串联谐振。由上述分析可知，谐振发生的条件为

$$
\mathrm{Im} \left[ Z (\mathrm{j} \omega_ {0}) \right] = X (\mathrm{j} \omega_ {0}) = \omega_ {0} L - \frac {1}{\omega_ {0} C} = 0
$$

这只有在电感、电容同时存在时，上述条件才能满足。由上式可知电路发生谐振的角频率  $\omega_{0}$  和频率  $f_{0}$  为

![](../../raw/pages_0257-0288/images/page_287_chart_22.jpg)

<details>
<summary>line</summary>

| 0 | Max |
| --- | --- |
| \(\omega_{0}\) | Min |
</details>

图11-3 $Z(\mathrm{j}\omega)$ 频响曲线

$$
\omega_ {0} = \frac {1}{\sqrt {L C}} \quad f _ {0} = \frac {1}{2 \pi \sqrt {L C}}
$$

可以看出，RLC串联电路的谐振频率只有1个，而且，仅与电路中L、C有关，与电阻R无关。 $\omega_{0}$ （或 $f_{0}$ ）称为电路的固有频率（或自由频率）。因此，只有当输入信号 $u_{s}$ 的频率与电路的固有频率 $f_{0}$ 相同时（合拍），才能在电路中激起谐振。如果电路中L、C可调，改变电路的固有频率，则RLC串联电路就具有选择任一频率谐振（调谐），或避开某一频率谐振（失谐）的性能，也可以利用串联谐振现象，判别输入信号的频率。

(2) $Z(\mathrm{j}\omega_0) = R$ 为最小值（极小值），电路在谐振时的电流 $I(\mathrm{j}\omega_0)$ 为极大值（也是最大值），有

$$
I (\mathrm{j} \omega_ {0}) = \frac {U _ {\mathrm{s}} (\mathrm{j} \omega_ {0})}{R}
$$

此极大值又称为谐振峰, 这是 RLC 串联电路发生谐振时的突出标志, 据此, 可以判断电路是否发生了谐振。当  $u_{s}$  的幅值不变时, 谐振峰仅与电阻 R 有关, 所以, 电阻 R 是唯一能控制和调节谐振峰的电路元件, 从而控制谐振时的电感和电容的电压及其储能状态(下面有说明)。图 11-4 所示为两个参数不同的 RLC 串

![](../../raw/pages_0257-0288/images/page_287_chart_29.jpg)

<details>
<summary>line</summary>

| Series | Description |
| --- | --- |
| (1) R1 | Solid curve representing the primary signal peak |
| (2) R2 | Dashed curve representing a secondary, lower-amplitude response |
| \(\omega01\) | Peak frequency point on the x-axis |
| \(\omega02\) | Peak frequency point on the x-axis |
</details>

图 11-4 电流  $I(\mathrm{j}\omega)$  的特性

---

§ 11-2 RLC 串联电路的谐振

265

联电路 $(u_{s}$ 相同 $)$ 电流的幅频特性, 即  $\left|\dot{I}(j\omega)\right|-\omega$ , 从特性可以看出, 两者在全频域内的变化走向是相同的, 但曲线的整体形状差异很大, 这将在下一节作重点分析比较。

(3) 电抗电压  $U_{X}(j\omega_{0})=0$  , 即有

$$
\begin{array}{l} \dot {U} _ {x} (\mathrm{j} \omega_ {0}) = \mathrm{j} \left(\omega_ {0} L - \frac {1}{\omega_ {0} C}\right) \dot {I} (\mathrm{j} \omega_ {0}) = \mathrm{j} \frac {\omega_ {0} L}{R} \dot {U} _ {s} (\mathrm{j} \omega_ {0}) - \mathrm{j} \frac {1}{\omega_ {0} C R} \dot {U} _ {s} (\mathrm{j} \omega_ {0}) \\ = \dot {U} _ {L} (\mathrm{j} \omega_ {0}) + \dot {U} _ {C} (\mathrm{j} \omega_ {0}) = 0 \\ \end{array}
$$

因此，$L$、$C$ 串联端口相当于短路，但 $\dot{U}_L(\mathrm{j}\omega_0)$、$\dot{U}_C(\mathrm{j}\omega_0)$ 分别都不等于零，两者模值相等且反相，相互完全抵消。根据这一特点，串联谐振又称为电压谐振。此外，工程上将式中的比值 $\frac{\omega_0L}{R} = \frac{1}{\omega_0CR}$ 定义为谐振电路的品质因数 $Q$（称 $Q$ 值），即

$$
Q \stackrel {\mathrm{def}} {=} \frac {\omega_ {0} L}{R} = \frac {1}{\omega_ {0} C R} = \frac {1}{R} \sqrt {\frac {L}{C}}
$$

(注意: Q 在这里不表示无功功率)。进一步分析可知, Q 值不仅综合反映了电路中三个参数对谐振状态的影响, 而且, 也是分析和比较谐振电路频率特性的一个重要的辅助参数。用 Q 值表示  $U_{L}(j\omega_{0})$  和  $U_{C}(j\omega_{0})$  为

$$
U _ {L} (\mathrm{j} \omega_ {0}) = U _ {C} (\mathrm{j} \omega_ {0}) = Q U _ {\mathrm{s}} (\mathrm{j} \omega_ {0})
$$

显然，当 $Q > 1$ 时，电感和电容两端将分别出现比 $U_{\mathrm{s}}(\mathrm{j}\omega_0)$ 高 $Q$ 倍的过电压。在高电压的电路系统中（如电力系统），这种过电压非常高，可能会危及系统的安全，必须采取必要的防范措施。但在低电压的电路系统中，如无线电接收系统中，则要利用谐振时出现的过电压来获得较大的输入信号。

Q 值可通过测定谐振时的电感或电容电压求得, 即

$$
Q = \frac {U _ {c} (\mathrm{j} \omega_ {0})}{U _ {s} (\mathrm{j} \omega_ {0})} = \frac {U _ {L} (\mathrm{j} \omega_ {0})}{U _ {s} (\mathrm{j} \omega_ {0})}
$$

而谐振时电阻 R 的端电压  $U_{R}(j\omega_{0})$  为

$$
\dot {U} _ {R} (\mathrm{j} \omega_ {0}) = \dot {U} _ {\mathrm{s}} (\mathrm{j} \omega_ {0})
$$

这也是谐振峰,表明谐振时,电阻 R 上将获得全额的输入电压。图 11-5 为谐振时的电压相量图。

根据上述分析可知,RLC 串联电路中的三个元件都可以作为信号的输出端口,只要参数选配确当,输出信号的幅值就能大于或等于输入信号的幅值。

![](../../raw/pages_0289-0320/images/page_288_image_16.jpg)

<details>
<summary>text_image</summary>

ÛL
ÛR
Q>1
O
ÛC
Ûs
</details>

图11-5 谐振时的电压相量图

(4) $Q(\mathrm{j}\omega_{0})=0$ , 即电路吸收的无功功率等于零, 有

$$
Q (\mathrm{j} \omega_ {0}) = Q _ {L} (\mathrm{j} \omega_ {0}) + Q _ {C} (\mathrm{j} \omega_ {0}) = \omega_ {0} L I ^ {2} (\mathrm{j} \omega_ {0}) - \frac {1}{\omega_ {0} C} I ^ {2} (\mathrm{j} \omega_ {0}) = 0
$$

上式表明,电感吸收的无功功率等于电容发出的无功功率,但各自不等于零。电路中储存的电磁能在L和C之间以两倍于谐振频率的频率做周期性的交换,相互完全补偿,自成独立系统,与外源无能量交换。储存的电磁能的总和为一常数,可根据i或 $u_{s}$ 的最

---

266

第十一章 电路的频率响应

大值求得,即

$$
\begin{array}{l} W (\mathrm{j} \omega_ {0}) = W _ {L} (\mathrm{j} \omega_ {0}) + W _ {C} (\mathrm{j} \omega_ {0}) = \frac {1}{2} L I _ {\mathrm{m}} ^ {2} (\mathrm{j} \omega_ {0}) = \frac {1}{2} C U _ {c m} ^ {2} (\mathrm{j} \omega_ {0}) \\ = C Q ^ {2} U _ {\mathrm{s}} ^ {2} (\mathrm{j} \omega_ {0}) \\ \end{array}
$$

(式中 Q 为电路的品质因数)。此时,电压源  $u_{s}$  只发出有功功率  $P(j\omega_{0})$ ,供电阻 R 消耗,即

$$
\overline {{S}} _ {\mathrm{s}} (\mathrm{j} \omega_ {0}) = R I ^ {2} (\mathrm{j} \omega_ {0}) = \frac {U _ {\mathrm{s}} ^ {2} (\mathrm{j} \omega_ {0})}{R} = P (\mathrm{j} \omega_ {0})
$$

电路的 Q 值亦可根据谐振时,电感或电容的无功功率和电阻消耗的有功功率  $P(j\omega_{0})$  的比值来表示

$$
Q = \frac {\omega_ {0} L I ^ {2} (\mathrm{j} \omega_ {0})}{R I ^ {2} (\mathrm{j} \omega_ {0})} = \frac {| Q _ {L} (\mathrm{j} \omega_ {0}) |}{P (\mathrm{j} \omega_ {0})} = \frac {| Q _ {C} (\mathrm{j} \omega_ {0}) |}{P (\mathrm{j} \omega_ {0})}
$$

例 11-2 图 11-2 所示电路中, $U_{s}=0.1\ V$, $R=1\Omega$, $L=2\ \mu H$, $C=200\ pF$ 时, 电流 $I=0.1\ A$。求正弦电压源 $u_{s}$ 的频率 $\omega$ 和电压 $U_{C}$、$U_{L}$ 以及电路的 $Q$ 值。

解 令 $\dot{U}_{s}=0.1/0^{\circ}\mathrm{V}$, 设电流为 $\dot{I}=0.1/\phi_{i}\mathrm{A}$, 则有

$$
0. 1 / \phi_ {i} = \frac {0 . 1 / 0 ^ {\circ}}{1 + \mathrm{j} X (\mathrm{j} \omega)}
$$

显然有  $X(j\omega)=0,\phi_{i}=0^{\circ}$ ，所以电流  $\dot{I}$  与电压  $\dot{U}_{s}$  同相，电路处于谐振状态。谐振频率  $\omega_{0}$  为

$$
\omega_ {0} = \frac {1}{\sqrt {L C}} = \frac {1}{\sqrt {2 \times 1 0 ^ {- 6} \times 2 0 0 \times 1 0 ^ {- 1 2}}} \mathrm{rad/s} = 5 0 \times 1 0 ^ {6} \mathrm{rad/s}
$$

$\omega_{0}$  即为电压源  $u_{s}$  的频率。电路的 Q 值为

$$
Q = \frac {1}{R} \sqrt {\frac {L}{C}} = 1 0 0
$$

谐振时电压  $U_{L}$  和  $U_{C}$  为

$$
U _ {L} = U _ {c} = Q U _ {\mathrm{s}} = 1 0 \mathrm{V}
$$

## §11-3 RLC 串联电路的频率响应

上一节着重分析了 RLC 串联电路在谐振点  $\omega_{0}$  的状态。本节将分析下述网络函数（电压比）:

$$
\frac {\dot {U} _ {R} (\mathrm{j} \omega)}{\dot {U} _ {\mathrm{s}} (\mathrm{j} \omega)}, \frac {\dot {U} _ {L} (\mathrm{j} \omega)}{\dot {U} _ {\mathrm{s}} (\mathrm{j} \omega)} \text {和} \frac {\dot {U} _ {G} (\mathrm{j} \omega)}{\dot {U} _ {\mathrm{s}} (\mathrm{j} \omega)}
$$

的频率特性。当输入信号  $u_{s}$  的幅值不变而  $\omega$  变动时，这犹如从输入端口输入变量  $\omega$ ，而在不同“窗口”（输出端口）观察频率  $\omega$  的响应，所以，这些网络函数的频率特性又统称为电路的频率响应，为了便于比较不同参数的 RLC 串联电路的频率响应之间在性能

![](../../raw/pages_0289-0320/images/page_289_image_22.jpg)

RLC 串联电路的频率响应

---

§ 11-3 RLC 串联电路的频率响应

267

上的差异，纵、横坐标都采用相对于谐振点的比值(倍率)作为绘制频率特性的坐标系。由于已设定 $U_{\mathrm{s}}(\mathrm{j}\omega)=U_{\mathrm{s}}(\mathrm{j}\omega_{0})$ ，所以上述电压比的模就表示任一频率时的输出电压与其谐振点的输入电压之比值；而横坐标也用与谐振频率 $\omega_{0}$ 的比值表示，即 $\eta=\frac{\omega}{\omega_{0}},\omega=\eta\omega_{0}$ 。这样，所有的RLC电路都在 $\eta=1$ 处谐振，都在同一个相对尺度下来比较相互频率特性的差异，这一共同的尺度也表示各谐振电路的偏谐程度（偏离谐振点程度），下面用新坐标系来分析上述网络函数的频率特性，这样绘制的频率响应曲线，称为通用曲线。

(1) 当以电阻电压  $\dot{U}_{R}(j\eta)$  作为输出变量, 其网络函数  $H_{R}(j\eta)$  表示为

$$
H _ {R} (\mathrm{j} \eta) = \frac {\dot {U} _ {R} (\mathrm{j} \omega)}{\dot {U} _ {\mathrm{s}} (\mathrm{j} \omega)} = \frac {R}{R + \mathrm{j} \left(\omega L - \frac {1}{\omega C}\right)} = \frac {1}{1 + \mathrm{j} Q \left(\eta - \frac {1}{\eta}\right)}
$$

频率响应分别为

$$
\phi (\mathrm{j} \eta) = - \arctan \left[ Q \left(\eta - \frac {1}{\eta}\right) \right] (\text {相频特性})
$$

$$
\mid H _ {R} (\mathrm{j} \eta) \mid = \cos [ \phi (\mathrm{j} \eta) ] (\text {幅频特性})
$$

从上式可以看出,不同参数的 RLC 串联电路在频响上的差异,可以通过各自的 Q 值体现出来。电路的谐振曲线如图 11-6(a)(b) 所示,图中  $Q_{1} \gg Q_{2}$ 。从幅频特性可以很清楚地看出,它们有如下的共同点及差异:

![](../../raw/pages_0289-0320/images/page_290_chart_9.jpg)

<details>
<summary>line</summary>

| \(\eta\) | Curve (1) | Curve (2) |
| --- | --- | --- |
| ~0.5 | — | \(1/\sqrt{2}\) |
| 1 | 1 | 1 |
| ~1.5 | — | \(1/\sqrt{2}\) |
</details>

(a)

![](../../raw/pages_0289-0320/images/page_290_chart_11.jpg)

<details>
<summary>contour</summary>

| \(\eta\) | Curve (1) \(({}^{\circ})\) | Curve (2) \(({}^{\circ})\) |
| --- | --- | --- |
| 0 | ~88 | ~85 |
| 1 | 0 | 0 |
| ~1.3 | ~-88 | ~-85 |
</details>

(b)

图 11-6  $\dot{U}_{R}(j\eta)/\dot{U}_{s}(j1)$  频率响应

① 它们都在谐振点  $\eta=1$  处出现峰值，在其邻域  $\eta=1+\Delta\eta$  内都有较大幅度的输出信号，这表明 RLC 串联电路都具有在全频域内选择各自谐振信号的性能，工程上称这一性能为“选择性”。
② 当信号的频率偏离谐振频率 $(\eta\neq1)$ 后, 输出信号的幅度都从峰值开始下降, 表明电路对非谐振频率的信号有抑制能力(简称抑非能力), 电路的这种抑非能力取决于

---

268

第十一章 电路的频率响应

述比值:

$$
\left| Q \left(\eta - \frac {1}{\eta}\right) \right| _ {\eta \neq 1} = \left| \frac {X (1 + \Delta \eta)}{R} \right| \quad [ R = Z (\mathrm{j} \omega_ {0}) ]
$$

该比值为信号偏离谐振频率后，电路电抗的增量[因为 $X(\mathrm{j}1) = 0$ ]与谐振时阻抗的比值，它与电路的 $Q$ 值成正比，$Q$ 值越大，该比值越大，电抗的相对增量就越大，电路的抑非能力越强，这也说明，电路的抑非能力主要是由非零电抗引起的。从曲线可以看出，由于 $Q_{1} \gg Q_{2}$，曲线(1)代表的电路的抑非能力强于曲线(2)代表的电路，所以曲线(1)急速下降，显得十分陡峭，而曲线(2)下降很慢，顶部的变化显得比较平缓。曲线的整体形状显示了电路在抑非能力上的差异，而这一差异在谐振点附近显得尤为突出；当信号的频率远离谐振频率后，左侧趋同于 $RC$ 电路，右侧趋同于 $RL$ 电路，彼此的差异逐渐缩小，而趋于消失。

③ 电路在全频域内都有信号的输出,但只有在谐振点附近的邻域 $(\eta=1+\Delta\eta)$ 内输出幅度较大,具有工程实际应用价值。为此,工程上设定一个输出幅度指标来界定频率范围,划分出谐振电路的通频带(简称通带)和阻带。通带限定的频域范围称为带宽,记为BW。工程上按下式决定通带的BW,即

$$
\mid H _ {R} (\mathrm{j} \eta) \mid \geqslant \frac {1}{\sqrt {2}} = 0. 7 0 7 (\text {设定的指标})
$$

上式取等号时,根据  $H_{R}(j\eta)$  的表达式有

$$
Q \bigg (\eta - \frac {1}{\eta} \bigg) = \pm 1
$$

根据该方程可求得两个频率点,作为通带BW的上下界,可分别设 $\eta_{j1}<1$ (谐振点左侧)称为下界(下截止频率), $\eta_{j2}>1$ (谐振点右侧)称为上界(上截止频率),分别为

$$
\eta_ {\mathrm{j1}} = - \frac {1}{2 Q} + \sqrt {\left(\frac {1}{2 Q}\right) ^ {2} + 1} <   1 \quad \text {和} \quad \omega_ {\mathrm{j1}} = \eta_ {\mathrm{j1}} \omega_ {0} (\text {下界})
$$

$$
\eta_ {\mathrm{j2}} = \frac {1}{2 Q} + \sqrt {\left(\frac {1}{2 Q}\right) ^ {2} + 1} > 1 \quad \text {和} \quad \omega_ {\mathrm{j2}} = \eta_ {\mathrm{j2}} \omega_ {0} (\text {上界})
$$

通带的 $BW$ 为

$$
B W = \omega_ {\mathrm{j2}} - \omega_ {\mathrm{j1}} = \frac {\omega_ {0}}{Q} \quad \text {或} \quad B W = \frac {f _ {0}}{Q}
$$

上述界定的通带位于频域中段,呈带状形,所以网络函数  $H_{R}(j\eta)$  称为带通函数。通带的频率范围为

$$
\omega_ {\mathrm{j} 1} \leqslant \omega \leqslant \omega_ {\mathrm{j} 2}
$$

$\omega_{j1}$ 、 $\omega_{j2}$ 分别位于 $\omega_{0}$ 两侧，因此 $\omega_{0}$ 又常称为中心频率。

工程上对  $\omega_{j1}, \omega_{j2}$  常另有称谓，如 3dB 点 $^{①}$ ，半功率点（因为此时电阻上的功耗等于谐振时电阻功耗的一半），并有  $\varphi(j\eta_{j1}) = 45^{\circ}, \varphi(j\eta_{j2}) = -45^{\circ}$ 。

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 按分贝的定义,此电压比值相当于  $20 \lg(0.707) = -3 \text{ dB}$ , 即电压下降了 3 dB。</span></small>

---

§ 11-3 RLC 串联电路的频率响应

269

工程上亦常用通带的 $BW$ 来比较和评价电路的选择性，由上面的论述可以看出，$BW$ 与 $Q$ 值成反比，$Q$ 值越大，$BW$ 越窄，电路选择性越好，抑非能力越强，反之，$Q$ 值越小，$BW$ 就越宽，抑非能力越弱，选择性能越差，但宽带包含的信号多，信号流失少，有利于减少信号的失真。上述两种情况都有工程实用价值。$BW$ 如图11-6(a)所示，读者可将曲线(1)和曲线(2)的 $BW_{(1)}$ 和 $BW_{(2)}$ 作一比较。

通过本节的分析可知，RLC串联谐振电路是一种简单、易调和频响性能优良的谐振电路。

(2) 分别以电感电压  $\dot{U}_{L}(\mathrm{j}\eta)$  和电容电压  $\dot{U}_{c}(\mathrm{j}\eta)$  为输出变量的网络函数  $H_{L}(\mathrm{j}\eta)$ 、 $H_{c}(\mathrm{j}\eta)$  分别为

$$
H _ {c} (\mathrm{j} \eta) = \frac {\dot {U} _ {c} (\mathrm{j} \eta)}{\dot {U} _ {s} (\mathrm{j} 1)} = \frac {- \mathrm{j} Q}{\eta + \mathrm{j} Q (\eta^ {2} - 1)}
$$

$$
H _ {L} (\mathrm{j} \eta) = \frac {\dot {U} _ {L} (\mathrm{j} \eta)}{\dot {U} _ {\mathrm{s}} (\mathrm{j} 1)} = \frac {\mathrm{j} Q}{\frac {1}{\eta} + \mathrm{j} Q \left(1 - \frac {1}{\eta^ {2}}\right)}
$$

由于  $\dot{U}_{c}(\mathrm{j}\eta)$  滞后  $\dot{U}_{R}(\mathrm{j}\eta)90^{\circ}$ ，而  $\dot{U}_{L}(\mathrm{j}\eta)$  超前  $90^{\circ}$ ，所以，上述网络函数的相频特性可不予分析。而描绘幅频特性曲线时，必须首先确定函数的极值点。函数  $H_{c}(\mathrm{j}\eta)$  的极值条件为

$$
\frac {\mathrm{d}}{\mathrm{d} \eta} \left[ \frac {U _ {c} (\mathrm{j} \eta)}{U _ {\mathrm{s}} (\mathrm{j} 1)} \right] = 0
$$

可求得如下三个极值点  $\eta_{c1}, \eta_{c2}$  和  $\eta_{c3}$  及对应的极值:

$$
\eta_ {c 1} = 0, \quad \frac {U _ {c} (\mathrm{j} \eta_ {c 1})}{U _ {\mathrm{s}} (\mathrm{j} 1)} = 1
$$

$$
\eta_ {c 2} = \sqrt {1 - \frac {1}{2 Q ^ {2}}}, \quad \frac {U _ {c} (\mathrm{j} \eta_ {c 2})}{U _ {\mathrm{s}} (\mathrm{j} 1)} = \frac {Q}{\sqrt {1 - \frac {1}{4 Q ^ {2}}}} > Q \quad (\text {当} Q > 0. 7 0 7 \text {时})
$$

$$
\eta_ {c 3} = \infty , \quad \frac {U _ {c} (\mathrm{j} \eta_ {c 3})}{U _ {\mathrm{e}} (\mathrm{j} 1)} = 0
$$

对于 $\frac{U_L(\mathrm{j}\eta)}{U_2(\mathrm{j}1)}$ 可作类似的分析，从表达式可知，$\eta_{L} = \frac{1}{\eta_{C}}$ 所以三个极值点 $\eta_{L1}, \eta_{L2}$ 和 $\eta_{L3}$ 及对应的极值为

$$
\eta_ {L 1} = \frac {1}{\eta_ {c 3}} = 0, \quad \frac {U _ {L} (\mathrm{j} \eta_ {L 1})}{U _ {\mathrm{s}} (\mathrm{j} 1)} = 0
$$

$$
\eta_ {L 2} = \frac {1}{\eta_ {c 2}} = \sqrt {\frac {2 Q ^ {2}}{2 Q ^ {2} - 1}}, \quad \frac {U _ {L} (\mathrm{j} \eta_ {L 2})}{U _ {\mathrm{a}} (\mathrm{j} 1)} = \frac {Q}{\sqrt {1 - \frac {1}{4 Q ^ {2}}}} > Q \quad (\text {当} Q > 0. 7 0 7 \text {时})
$$

$$
\eta_ {L 3} = \frac {1}{\eta_ {c 1}} = \infty , \quad \frac {U _ {L} (\mathrm{j} \eta_ {L 3})}{U _ {\mathrm{s}} (\mathrm{j} 1)} = 1
$$

---

1. 用 $\mathrm{H}_{2}$ 气相反应, 用 $\mathrm{H}_{2}$ 气相反应, 用 $\mathrm{H}_{2}$ 气相反应, 用 $\mathrm{H}_{2}$ 气相反应, 用 $\mathrm{H}_{2}$ 气相反应

270

第十一章 电路的频率响应

两条幅频特性如图11-7所示，图中粗虚线表示 $Q \leqslant 0.707$ 时的幅频特性。从图中可以看出，$H_{C}(\mathrm{j}\eta)$ 为低通函数，当 $Q \gg 1$ 时，可求得上截止频率 $\omega_{\mathrm{j}} = 1.55\omega_{0}$，其通频带域 $0 \leqslant \omega \leqslant \omega_{\mathrm{j}}$；函数 $H_{L}(\mathrm{j}\eta)$ 为高通函数，当 $Q \gg 1$ 时，求得下截止频率 $\omega_{\mathrm{j}} = \frac{\omega_{0}}{1.55} = 0.645\omega_{0}$，通频带域为 $\omega_{\mathrm{j}} \leqslant \omega < \infty$，当 $Q > 0.707$ 时，两者都有大于 $Q$ 且相等的峰值，当 $Q$ 增大时，$\eta_{C2}, \eta_{L2}$ 都向 $\eta = 1$ 靠拢，峰值增高，图中 $a, b, c$ 三点在抬高的同时，逐渐向 $c$ 点合拢，当 $Q \to \infty$，三点合于无穷远。

![](../../raw/pages_0289-0320/images/page_293_chart_4.jpg)

<details>
<summary>line</summary>

| \(\eta\) | UL/Us | UC/Us | Dashed Curve |
| --- | --- | --- | --- |
| 0 | 1 | 0 | 1 |
| \(\eta C2\) | Peak | — | — |
| 1 | — | Peak | — |
| \(\eta L2\) | Peak | — | — |
</details>

图 11-7  $H_{L}(j\eta)$ 、 $H_{C}(j\eta)$  的幅频特性

例 11-3 RLC 串联电路中  $U_{s}=200\ V, C=6.34\ \mu F$ ，电路的固有频率  $\omega_{0}=314\ rad/s$ ，带通函数的带宽  $BW=6.28\ rad/s$ 。求 L、R 和  $U_{L}$ 、 $U_{C}$ 。

解 电路的 Q 值为

$$
Q = \frac {\omega_ {0}}{B W} = \frac {3 1 4}{6 . 2 8} = 5 0
$$

谐振时容抗等于感抗,则 L 为

$$
L = \frac {1}{\omega_ {0} ^ {2} C} = \frac {1}{(3 1 4) ^ {2} \times 6 . 3 4 \times 1 0 ^ {- 6}} \mathrm{H} = 1. 6 0 \mathrm{H}
$$

$R$ 的值为

$$
R = \frac {\omega_ {0} L}{Q} = \frac {3 1 4 \times 1 . 6}{5 0} \Omega = 1 0 \Omega
$$

$U_{L}(j\omega_{0})$ 、 $U_{C}(j\omega_{0})$ 为

$$
U _ {L} (\mathrm{j} \omega_ {0}) = U _ {c} (\mathrm{j} \omega_ {0}) = Q U _ {\mathrm{s}} (\mathrm{j} \omega_ {0}) = 5 0 \times 2 0 0 \mathrm{V} = 1 0 0 0 0 \mathrm{V}
$$

## §11-4 RLC 并联谐振电路

图 11-8(a) 所示 RLC 并联电路是与 RLC 串联电路相对应的另一种形式的谐振电路。

并联谐振的定义与串联谐振的定义相同,即端口上的电压  $\dot{U}$  与输入电流  $\dot{I}$  同相时的工作状况称为谐振。由于发生在并联电路中,所以称为并联谐振。分析方法与 RLC 串联电路相同,并联谐振的条件为

$$
\mathrm{Im} \left[ Y (\mathrm{j} \omega_ {0}) \right] = 0
$$

因为 $Y(\mathrm{j}\omega_0) = G + \mathrm{j}\left(\omega_0C - \frac{1}{\omega_0L}\right)$，可解得谐振时的角频率 $\omega_0$ 和频率 $f_0$ 为

$$
\omega_ {0} = \frac {1}{\sqrt {L C}}
$$

![](../../raw/pages_0289-0320/images/page_293_image_21.jpg)

RLC并联谐振电路

---

§ 11-4 RLC 并联谐振电路

271

$$
f _ {0} = \frac {1}{2 \pi \sqrt {L C}}
$$

该频率称为电路的固有频率。

并联谐振时,输入导纳  $Y(\mathrm{j}\omega_{0})$  为最小

$$
Y (\mathrm{j} \omega_ {0}) = G + \mathrm{j} \left(\omega_ {0} C - \frac {1}{\omega_ {0} L}\right) = G
$$

或者说输入阻抗最大, $Z(j\omega_{0})=R$ ,所以谐振时端电压达最大值

![](../../raw/pages_0289-0320/images/page_294_image_7.jpg)

<details>
<summary>text_image</summary>

i̇
+   i̇G   i̇L   i̇C
      G       1
      /jωL     jωC
      U
      -
</details>

(a)

![](../../raw/pages_0289-0320/images/page_294_image_9.jpg)

<details>
<summary>text_image</summary>

I_C
I_G
O
I_L
I_S
U
</details>

(b)

图 11-8 并联谐振电路

$$
U (\omega_ {0}) = \mid Z (\mathrm{j} \omega_ {0}) \mid I _ {\mathrm{s}} = R I _ {\mathrm{s}}
$$

可以根据这一现象判别并联电路是否发生了谐振。

并联谐振时有  $\dot{I}_{L} + \dot{I}_{C} = 0$  (所以并联谐振又称电流谐振):

$$
\dot {I} _ {L} (\omega_ {0}) = - \mathrm{j} \frac {1}{\omega_ {0} L} \dot {U} = - \mathrm{j} \frac {1}{\omega_ {0} L G} \dot {I} _ {\mathrm{s}} = - \mathrm{j} Q \dot {I} _ {\mathrm{s}}
$$

$$
\dot {I} _ {c} (\omega_ {0}) = \mathrm{j} \omega_ {0} C \dot {U} = \mathrm{j} \frac {\omega_ {0} C}{G} \dot {I} _ {\mathrm{s}} = \mathrm{j} Q \dot {I} _ {\mathrm{s}}
$$

式中 Q 称为并联谐振电路的品质因数

$$
Q = \frac {I _ {L} (\omega_ {0})}{I _ {\mathrm{s}}} = \frac {I _ {C} (\omega_ {0})}{I _ {\mathrm{s}}} = \frac {1}{\omega_ {0} L G} = \frac {\omega_ {0} C}{G} = \frac {1}{G} \sqrt {\frac {C}{L}}
$$

如果 $Q \gg 1$，则谐振时在电感和电容中会出现过电流，但从 $L, C$ 两端看进去的等效电纳等于零，即阻抗为无限大，相当于开路。图11-8(b)为并联谐振时的电流相量图。

谐振时无功功率 $Q_{L} = \frac{1}{\omega_{0}L} U^{2}, Q_{C} = -\omega_{0}CU^{2}$，所以 $Q_{L} + Q_{C} = 0$，表明在谐振时，电感的磁场能量与电容的电场能量彼此相互交换，完全补偿，两种能量的总和为

$$
W (\omega_ {0}) = W _ {L} (\omega_ {0}) + W _ {C} (\omega_ {0}) = L Q ^ {2} I _ {\mathrm{s}} ^ {2} = \text {常数}
$$

工程中采用的电感线圈和电容并联的谐振电路,如图 11-9(a) 所示,其中电感线圈用 R 和 L 串联组合表示。谐振时,有

$$
\mathrm{Im} \left[ Y (\mathrm{j} \omega_ {0}) \right] = 0
$$

而

$$
Y (\mathrm{j} \omega_ {0}) = \mathrm{j} \omega_ {0} C + \frac {1}{R + \mathrm{j} \omega_ {0} L} = \mathrm{j} \omega_ {0} C + \frac {R}{| Z (\mathrm{j} \omega_ {0}) | ^ {2}} - \mathrm{j} \frac {\omega_ {0} L}{| Z (\mathrm{j} \omega_ {0}) | ^ {2}}
$$

故有

$$
\omega_ {0} C - \frac {\omega_ {0} L}{\mid Z (\mathrm{j} \omega_ {0}) \mid^ {2}} = 0
$$

由上式可解得

$$
\omega_ {0} = \frac {1}{\sqrt {L C}} \sqrt {1 - \frac {C R ^ {2}}{L}}
$$

---

272

第十一章 电路的频率响应

显然，只有当 $1 - \frac{CR^2}{L} > 0$ ，即 $R < \sqrt{\frac{L}{C}}$ 时，$\omega_0$ 才是实数，所以 $R > \sqrt{\frac{L}{C}}$ 时，电路不会发生谐振。该电路调节电阻可改变电路的固有频率。

谐振时的输入导纳为

$$
Y (\mathrm{j} \omega_ {0}) = \frac {R}{| Z (\mathrm{j} \omega_ {0}) | ^ {2}} = \frac {C R}{L}
$$

可以证明,该电路发生谐振时的输入导纳不是最小值(即输入阻抗不是最大值),所以谐振时的端电压不是最大值。这种电路只有当  $R \ll \sqrt{\frac{L}{C}}$  时,它发生谐振时的特点才与图 11-8(a) 所示 GLC 并联谐振的特点接近。

![](../../raw/pages_0289-0320/images/page_295_image_7.jpg)

<details>
<summary>text_image</summary>

i_s
+
I_1
R
jωL
i_2
1
jωC
O
i_s
φ_1
U
i_2
i_1
(a)
(b)
</details>

图 11-9 一种并联谐振电路

此并联电路发生电流谐振时的电流相量图如图 11-9(b) 所示, 这时有

$$
I _ {2} = I _ {1} \sin \varphi_ {1} = I _ {\mathrm{s}} \tan \varphi_ {1}
$$

若电感线圈的阻抗角  $\varphi_{1}$  很大, 谐振时有过电流出现在电感支路和电容中。

下面对电路中的各种过电压和过电流现象做简单讨论。

当 RLC 串联电路发生谐振时, 若品质因数 Q 大于 1, 电容电压和电感电压大于激励电压, 呈现过电压现象。当 RLC 并联电路发生谐振时, 若品质因数 Q 大于 1, 电容中电流和电感中电流大于激励电流, 呈现过电流现象。需要指出的是, 正弦稳态电路出现的过电压和过电流是谐振过电压和谐振过电流, 只要电路结构参数和正弦激励频率不改变, 这种过电压和过电流将持续存在。

正弦稳态电路的谐振过电压和过电流与动态电路换路后产生的过电压和过电流的机理完全不同,有本质的区别,请学习者从两者产生的原因、电路方程、电路响应表达式等方面分析两者的差异。

在实际电路中还有一种情形,当电路中出现短路时,会出现过电流现象。请学习者独立思考电路短路发生初期和电路达到稳态后,短路电流表达式有何变化。

虽然电路中有各种过电压和过电流现象,但物理本质不同。学习者要善于透过现象看本质,从电路各种过电压和过电流现象入手,通过电路理论分析,从物理理论上理解电路不同过电压和过电流的本质。

## §11-5 波特图 $^{①}$

对电路和系统的频率特性进行分析时,为了直观地观察频率特性随频率变化的趋

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① H. W. Bode 最先使用这种图形, 故称波特图。</span></small>

---

§ 11-5 波特图

273

势和特征,需要准确地描绘频率响应曲线,这往往不是一件容易的事。工程上常采用对数坐标绘制频响曲线,这样做可以在不同频域内用直线近似代替曲线,使曲线局部直线化,整个曲线则折线化,从而使频响曲线变得易于描绘。这种用对数坐标描绘的频率响应图就称为频响波特图。

网络函数  $H(j\omega)$  是一个复数, 其指数形式为

$$
H (\mathrm{j} \omega) = \mid H (\mathrm{j} \omega) \mid \mathrm{e} ^ {\mathrm{j} \varphi (\mathrm{j} \omega)}
$$

对其取对数有

$$
\ln [ H (\mathrm{j} \omega) ] = \ln [ | H (\mathrm{j} \omega) | ] + \mathrm{j} \varphi (\mathrm{j} \omega)
$$

其实部为  $H(j\omega)$  的对数模，而虚部为  $H(j\omega)$  的相移函数，两者都是  $\omega$  的实函数。用对数坐标作图时，仍然要作两个图，一为对数模（用分贝表示）与对数频率的关系图形，称为幅频波特图，一为相移与对数频率的关系图形，称为相频波特图。作图时两者的横轴坐标都采用对数频率  $\lg \omega$ 。幅频波特图用分贝（dB）表示对数模，记为  $H_{dB}$ ，有

$$
H _ {\mathrm{dB}} = 2 0 \lg [ | H (\mathrm{j} \omega) | ]
$$

对相频波特图,其纵坐标仍然用度表示。

下面,通过具体例子来说明绘制波特图的方法。

例 11-4 画出如下网络函数的波特图。

$$
H (\mathrm{j} \omega) = \frac {2 0 0 \mathrm{j} \omega}{(\mathrm{j} \omega + 2) (\mathrm{j} \omega + 1 0)}
$$

解 首先将  $H(j\omega)$  改写成如下形式:

$$
\begin{array}{l} H (\mathrm{j} \omega) = \frac {1 0 \mathrm{j} \omega}{\left(1 + \frac {\mathrm{j} \omega}{2}\right) \left(1 + \frac {\mathrm{j} \omega}{1 0}\right)} \\ = \frac {1 0 \mid \mathrm{j} \omega \mid}{\left| 1 + \frac {\mathrm{j} \omega}{2} \right| \cdot \left| 1 + \frac {\mathrm{j} \omega}{1 0} \right|} \sqrt {9 0 ^ {\circ} - \arctan \left(\frac {\omega}{2}\right) - \arctan \left(\frac {\omega}{1 0}\right)} \\ \end{array}
$$

因此对数模(单位分贝)和相位(单位度)分别为

$$
\begin{array}{l} H _ {\mathrm{dB}} = 2 0 \lg 1 0 + 2 0 \lg (\mid \mathrm{j} \omega \mid) - 2 0 \lg \left(\left| 1 + \mathrm{j} \frac {\omega}{2} \right|\right) - 2 0 \lg \left(\left| 1 + \mathrm{j} \frac {\omega}{1 0} \right|\right) \\ \phi = 9 0 ^ {\circ} - \arctan \left(\frac {\omega}{2}\right) - \arctan \left(\frac {\omega}{1 0}\right) \\ \end{array}
$$

注意到幅频波特图和相频波特图的横坐标均取对数频率 $\lg \omega$ ，对 $H_{\mathrm{dB}}$ 各项的分析如下:

(1)  $20 \lg 10 = 20 \, dB$  为常量, 为 20dB 的水平直线。
(2) $20\lg(|j\omega|)$ 为20 dB/10倍频的直线。当 $\omega=0.1$ 时, $20\lg(|j0.1|)=-20$ ; 当 $\omega=1$ 时, $20\lg(|j1|)=0$ ; 当 $\omega=10$ 时, $20\lg(|j10|)=20$ 。
(3) $-20\lg \left(\left|1 + \mathrm{j}\frac{\omega}{2}\right|\right)$ 可由两段直线逼近。当 $\omega \rightarrow 0$ 时，$-20\lg 1 = 0$；当 $\omega \rightarrow \infty$ 时，

![](../../raw/pages_0289-0320/images/page_296_image_22.jpg)

<details>
<summary>text_image</summary>

Technical diagram of a mechanical assembly with labeled components and cross-sectional views
</details>

---

[No text]

274

第十一章 电路的频率响应

$-20 \lg \left( \left| 1 + j \frac{\omega}{2} \right| \right) \approx -20 \lg \left( \frac{\omega}{2} \right)$ 。这样，以 $\omega = 2$ 为分界点，在 $\omega < 2$ 区间，该项可用斜率为零的直线逼近；在 $\omega > 2$ 区间，该项用斜率为 $-20 \mathrm{~dB} / 10$ 倍频的直线逼近。

(4) $-20\lg \left(\left|1 + \mathrm{j}\frac{\omega}{10}\right|\right)$ 的分析与(3)类似，以 $\omega = 10$ 为分界点，在 $\omega < 10$ 区间，该项用斜率为零的直线逼近；在 $\omega > 10$ 区间，该项用斜率等于-20dB/10倍频的直线逼近。

将以上四项叠加,就得到如图 11-10(a) 中实线所示的幅频波特图。

![](../../raw/pages_0289-0320/images/page_297_chart_6.jpg)

<details>
<summary>line</summary>

| \(lg\omega\) | HdB/dB |
| --- | --- |
| 0.1 | 0 |
| 1 | 20 |
| 10 | 20 |
| 200 | 0 |
</details>

(a) 幅频波特图

![](../../raw/pages_0289-0320/images/page_297_chart_8.jpg)

<details>
<summary>line</summary>

| \(1g\omega/\omega\) | \(\phi (\)Solid Line) | \(\phi (-\)arctan(ω/2)) | \(\phi (-\)arctan(ω/10)) |
| --- | --- | --- | --- |
| 0.1 | \(90{}^{\circ}\) | — | — |
| 0.2 | \(90{}^{\circ}\) | 0 | — |
| 1 | ~\(75{}^{\circ}\) | 0 | 0 |
| 10 | 0 | — | — |
| 20 | ~\(-65{}^{\circ}\) | — | — |
| 100 | \(-90{}^{\circ}\) | — | — |
| 200 | \(-90{}^{\circ}\) | — | — |
</details>

(b) 相频波特图

图 11-10  $H(j\omega)$  的波特图

对  $\phi$  各项的分析如下:

(1)  $90^{\circ}$  为常量, 在相频波特图上是值为  $90^{\circ}$  的水平直线。

---

§ 11-6 滤波器简介

275

(2)  $-\arctan\left(\frac{\omega}{2}\right)=\left\{\begin{aligned}&0&\omega=0\\ &-45^{\circ}&\omega=2\\ &-90^{\circ}&\omega\rightarrow\infty\end{aligned}\right.$

在 $0 \leqslant \omega \leqslant 0.2$ 区间，$-\arctan \left(\frac{\omega}{2}\right) \approx 0$，该项用值为 $0^{\circ}$ 的水平直线逼近；当 $\omega = 2$ 时，$-\arctan 1 = -45^{\circ}$；当 $\omega = 20$ 时，$-\arctan 10 \approx -90^{\circ}$。即在 $0.2 \leqslant \omega \leqslant 20$ 区间，$-\arctan \left(\frac{\omega}{2}\right)$ 可用斜率为 $-45^{\circ} / 10$ 倍频的直线逼近。在 $\omega \geqslant 20$ 区间，该项用值为 $-90^{\circ}$ 的水平直线逼近。三段逼近直线的交点在 $\omega = 0.2$ 处和 $\omega = 20$ 处。

(3) $-\arctan \left(\frac{\omega}{10}\right)$ 的分析与(2)类似, 即在 $1 \leqslant \omega \leqslant 100$ 区间, $-\arctan \left(\frac{\omega}{10}\right)$ 用斜率为 $-45^{\circ} / 10$ 倍频的直线逼近; 在 $0 \leqslant \omega \leqslant 1$ 区间, 该项用值为 $0^{\circ}$ 的水平直线逼近; 在 $\omega \geqslant 100$ 区间, 该项用值为 $-90^{\circ}$ 的水平直线逼近。

将以上三条折线叠加,就得到如图 11-10(b) 实线所示的相频波特图。

## §11-6 滤波器简介

工程上根据输出端口对信号频率范围的要求,设计专门的网络,置于输入-输出端口之间,使输出端口所需要的频率分量能够顺利通过,而抑制不需要的频率分量,这种具有选频功能的中间网络,工程上称为滤波器。通常将希望保留的频率范围称为通带,将希望抑制的频率范围称为阻带。根据通带和阻带在频率范围中的相对位置,滤波器分为低通、高通、带通和带阻四种类型。

工程上利用电感 $L$ 和电容 $C$ 彼此相反而又互补的频率特性, 先设计具有一定滤波功能的“单元电路”, 然后再用搭“积木”方式(如并联、级联等), 连接成各种各样的滤波器网络。如图 11-11(a) 所示为 L 形低通滤波器, 图 11-11(b)(c) 所示 T 形和 $\pi$ 形电路又是 L 形电路的一种镜像连接电路。图 11-12(a) 所示为高通滤波器的单元电路(与图 11-11 类似)。图 11-13 所示为 LC 串并联谐振电路构成的带通滤波器, 它利用谐振电路的频率特性, 只允许谐振频率邻域内的信号通过。图 11-14 所示电路为带阻滤波器, 它阻止谐振频率邻域内的信号通过。

![](../../raw/pages_0289-0320/images/page_298_image_9.jpg)

<details>
<summary>chemical</summary>

Simple LC circuit diagram with inductor L and capacitor C
</details>

(a) L形

![](../../raw/pages_0289-0320/images/page_298_image_11.jpg)

<details>
<summary>chemical</summary>

Electrical circuit diagram with inductors and capacitors labeled L and C
</details>

(b) T形

![](../../raw/pages_0289-0320/images/page_298_image_13.jpg)

<details>
<summary>chemical</summary>

Electrical circuit diagram with inductors and capacitors labeled L and C
</details>

(c) $\pi$ 形

图11-11 低通滤波器的单元电路

1. 用 $\mathrm{H}_{2}$ 气相分离的气体，用于化学分析（如: $\mathrm{H}_{2}$ 和 $\mathrm{H}_{2}$ 气相分离的气体）。

---

276

第十一章 电路的频率响应

![](../../raw/pages_0289-0320/images/page_299_image_2.jpg)

(a) L形

![](../../raw/pages_0289-0320/images/page_299_image_4.jpg)

<details>
<summary>chemical</summary>

Electrical circuit diagram with capacitors and inductors labeled C, L, and dashed line
</details>

(b) T形

![](../../raw/pages_0289-0320/images/page_299_image_6.jpg)

<details>
<summary>chemical</summary>

Electrical circuit diagram with capacitors and inductors labeled C and L
</details>

(c) $\pi$ 形

图 11-12 高通滤波器的单元电路

![](../../raw/pages_0289-0320/images/page_299_image_9.jpg)

<details>
<summary>chemical</summary>

Electrical circuit diagram with inductors L1 and L2, capacitors C1 and C2, and ground connections
</details>

图 11-13 带通滤波器

![](../../raw/pages_0289-0320/images/page_299_image_11.jpg)

<details>
<summary>chemical</summary>

Electrical circuit diagram with inductors and capacitors labeled L1, C1, L2, C2
</details>

图 11-14 带阻滤波器

上述无损耗 LC 滤波器中的电感元件体积较大,难以使滤波器小型化和集成化。

目前，在滤波器的设计中，已大量使用小型的片式电路元件，可以使滤波器小型化。随着电路和系统集成化的发展，滤波器的设计中，已广泛采用运算放大器，或其他VCVS有源器件，不再使用电感元件，称为RC有源滤波器，实现了滤波器的集成化，有关这方面的初步知识，读者可参阅本章后面的有关习题。滤波器的设计需要专门的理论知识，本书不做论述。

![](../../raw/pages_0289-0320/images/page_299_image_15.jpg)

## 思考题

11-1 为什么电路响应的幅值和相位会随着频率的变化而变化？电路的这个性质有哪些应用？

11-2 驱动点阻抗和导纳与正弦一端口的阻抗和导纳的概念是相同的吗？

11-3 使 RLC 串联电路发生谐振的方法有哪些？如何避免发生串联谐振？

11-4 RLC 串联电路发生谐振时,电路具有哪些特征?

11-5 RLC 串联电路中各元件上的电压响应的频率特性如何？

11-6 RLC 并联电路发生谐振时,电路具有哪些特征?

11-7 试简单阐述滤波器的用途？

![](../../raw/pages_0289-0320/images/page_299_image_24.jpg)

## 习题

11-1 求题 11-1 图所示电路端口 1-1' 的驱动点阻抗  $\frac{\dot{U}}{\dot{I}_{1}}$ 、转移电流比  $\frac{\dot{I}_{c}}{\dot{I}_{1}}$  和转移阻

---

习题

277

抗 $\frac{\dot{U}_{2}}{\dot{I}_{1}}$ 。

11-2 求题 11-2 图所示电路的转移电压比  $\frac{\dot{U}_{2}}{\dot{U}_{1}}$  和驱动点导纳  $\frac{\dot{I}_{1}}{\dot{U}_{1}}$ 。

![](../../raw/pages_0289-0320/images/page_300_image_5.jpg)

<details>
<summary>text_image</summary>

i₁ 2 Ω 1 Ω
+     ↓
U̇      1 F     2 H
-       +
      -
</details>

题11-1图

![](../../raw/pages_0289-0320/images/page_300_image_7.jpg)

<details>
<summary>text_image</summary>

i₁ 2 Ω 1 Ω
+       +
Ù₁ 1 F 1 Ω  Ù₂
-       -
</details>

题 11-2 图

11-3 RLC 串联电路中  $R=1\Omega, L=0.01\mathrm{H}, C=1\mu\mathrm{F}$ 。求:

(1) 输入阻抗与频率  $\omega$  的关系。
(2) 画出阻抗的频率响应。
(3) 谐振频率  $\omega_{0}$ 。
(4) 谐振电路的品质因数 Q。
(5) 通频带的宽度 BW。

11-4 RLC 并联电路中  $R = 10 \, k\Omega, L = 1 \, mH, C = 0.1 \, \muF$ 。求习题 11-3 中所列各项。
11-5 已知 RLC 串联电路中, $R = 50 \Omega, L = 400 \mathrm{mH}$, 谐振角频率 $\omega_0 = 5000 \mathrm{rad/s}$, $U_{\mathrm{s}} = 1 \mathrm{~V}$。求电容 $C$ 及各元件电压的瞬时表达式。
11-6 求题 11-6 图所示电路在哪些频率时短路或开路。

![](../../raw/pages_0289-0320/images/page_300_image_20.jpg)

(a)

![](../../raw/pages_0289-0320/images/page_300_image_22.jpg)

<details>
<summary>chemical</summary>

Simple LC circuit diagram with inductor L and capacitor C
</details>

(b)

![](../../raw/pages_0289-0320/images/page_300_image_24.jpg)

<details>
<summary>chemical</summary>

Electrical circuit diagram with inductors L1 and L2, and capacitor C1
</details>

(c)

![](../../raw/pages_0289-0320/images/page_300_image_26.jpg)

<details>
<summary>chemical</summary>

Simple LC circuit diagram with inductor L1 and capacitors C1 and C2
</details>

(d)

题11-6图

11-7 RLC 串联电路中, $L = 50 \mu \mathrm{H}, C = 100 \mathrm{pF}, Q = 50 \sqrt{2} = 70.71$, 电源 $U_{\mathrm{s}} = 1 \mathrm{mV}$。求电路的谐振频率 $f_{0}$、谐振时的电容电压 $U_{C}$ 和通带 $BW$。
11-8 RLC 串联电路谐振时，已知 $BW = 6.4\mathrm{kHz}$，电阻的功耗 $2\mu \mathrm{W}, u_{\mathrm{s}}(t) =$

---

278

第十一章 电路的频率响应

$\sqrt{2}\cos(\omega_{0}t)$  mV 和 C=400 pF。求 L、谐振频率  $f_{0}$  和谐振时电感电压  $U_{L}$ 。

11-9 RLC 串联电路中, $U_{s}=1\ V$ , 电源频率 $f_{s}=1\ MHz$ , 发生谐振时 $I(j\omega_{0})=100\ mA$ , $U_{c}(j\omega_{0})=100\ V$ , 试求 R、L 和 C 的值, Q 值和通带 BW。

11-10 RLC 并联谐振时， $f_{0}=1\ \mathrm{kHz}, Z(\mathrm{j}\omega_{0})=100\ \mathrm{k}\Omega, BW=100\ \mathrm{Hz}$ ，求 R、L 和 C。
11-11 求题 11-11 图所示电路的谐振频率及各频段的电抗性质。

![](../../raw/pages_0289-0320/images/page_301_image_8.jpg)

<details>
<summary>chemical</summary>

Electrical circuit diagram with inductors L1 and L2, capacitors C1 and C2, and ground connection
</details>

(a)

![](../../raw/pages_0289-0320/images/page_301_image_10.jpg)

<details>
<summary>text_image</summary>

jωL
2iC
iC
1
jωC
</details>

(b)

题11-11图

11-12 题 11-12 图所示电路中 $I_{s} = 20 \mathrm{~mA}, L = 100 \mu \mathrm{H}, C = 400 \mathrm{pF}, R = 10 \Omega$ 。电路谐振时的通带 $BW$ 和 $R_{L}$ 等于何值时能获得最大功率？求最大功率。
11-13 题 11-13 图所示电路中 $R = 10 \Omega, C = 0.1 \mu \mathrm{F}$, 正弦电压 $u_{\mathrm{s}}$ 的有效值 $U_{\mathrm{s}} = 1 \mathrm{~V}$, 电路的 $Q$ 值为 100, 求参数 $L$ 和谐振时的 $U_{L}$。

![](../../raw/pages_0289-0320/images/page_301_image_16.jpg)

<details>
<summary>text_image</summary>

i_s
R
L
C
R_L
</details>

题 11-12 图

![](../../raw/pages_0289-0320/images/page_301_image_18.jpg)

<details>
<summary>text_image</summary>

R
C
1:5
uS
+
-
uL
L'
</details>

题11-13图

11-14 题 11-14 图中  $C_{2}=400\ pF, L_{1}=100\ \mu H$ 。求下列两种条件下，电路的谐振频率  $\omega_{0}$ 。

(1) $R_{1} = R_{2}\neq \sqrt{\frac{L_{1}}{C_{2}}}$
(2) $R_{1} = R_{2} = \sqrt{\frac{L_{1}}{C_{2}}}$

![](../../raw/pages_0289-0320/images/page_301_image_24.jpg)

<details>
<summary>chemical</summary>

Electrical circuit diagram with resistors R1 and R2, inductor L1, and capacitor C2
</details>

题11-14图

---

习题

279

11-15 求题 11-15 图所示电路的转移电压比  $\frac{\dot{U}_{2}}{\dot{U}_{1}}$ 。

![](../../raw/pages_0289-0320/images/page_302_image_4.jpg)

<details>
<summary>text_image</summary>

1 Ω
1 F
+
u₁
-
1 F u
+
-
ku
+
-
u₂
+
</details>

(a)

![](../../raw/pages_0289-0320/images/page_302_image_6.jpg)

<details>
<summary>text_image</summary>

1 F
1 Ω
+
u₁
-
1 F
+
1 Ω
u
-
+
ku
-
u₂
+
</details>

(b)

题 11-15 图

11-16 求题 11-16 图所示电路的转移电压比  $\frac{\dot{U}_{2}}{\dot{U}_{1}}$ 。

![](../../raw/pages_0289-0320/images/page_302_image_10.jpg)

(a)

(b)

题 11-16 图

11-17 题 11-17 图所示电路中, $RC = 1 \mathrm{~s}$ 。求 $\frac{\dot{U}_2}{\dot{U}_1}$ 和 $\frac{U_2}{U_1} - \omega$ 。

![](../../raw/pages_0289-0320/images/page_302_image_15.jpg)

<details>
<summary>chemical</summary>

Electrical circuit diagram with two resistors and capacitors in parallel configuration
</details>

题 11-17 图

---

![](../../raw/pages_0289-0320/images/page_303_image_0.jpg)

<details>
<summary>natural_image</summary>

Pure mechanical assembly diagram without any text, numbers, or symbols
</details>

280

第十一章 电路的频率响应

11-18 题 11-18 图(a)所示系统的网络函数 $H(\mathrm{j}\omega)=\frac{\dot{U}_{2}}{\dot{U}_{s}}$, 其幅频特性 $|H(\mathrm{j}\omega)|-\omega$ 和相频特性 $\varphi(\mathrm{j}\omega)-\omega$ 如题 11-18 图(b)所示。求当 $u_{\mathrm{s}}=10-6.4\sin t-3.2\sin(2t)\sim2.1\sin(3t)+\cdots$ 时, 输出 $u_{2}$。

![](../../raw/pages_0289-0320/images/page_303_chart_4.jpg)

<details>
<summary>line</summary>

| (a) | -2 | 0 |
| --- | --- | --- |
| (a) | -1 | 0 |
| (a) | 0 | 0 |
| (a) | 1 | 0 |
| (a) | 2 | 0 |
| (b) | -2 | 0 |
| (b) | -1 | 0 |
| (b) | 0 | 2 |
| (b) | 1 | 0 |
| (b) | 2 | 0 |
</details>

题 11-18 图

![](../../raw/pages_0289-0320/images/page_303_image_6.jpg)

第十一章部分习题答案

11-19 作下列网络函数  $H(j\omega)$  的波特图。

(1) $H(\mathrm{j}\omega) = \frac{1}{10 + \mathrm{j}\omega}$。
(2) $H(\mathrm{j}\omega) = \frac{5(\mathrm{j}\omega + 2)}{\mathrm{j}\omega(\mathrm{j}\omega + 10)}$。
