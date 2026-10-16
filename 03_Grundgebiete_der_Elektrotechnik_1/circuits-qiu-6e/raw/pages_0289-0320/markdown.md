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

![](images/page_288_image_16.jpg)

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

的频率特性。当输入信号  $u_{s}$  的幅值不变而  $\omega$  变动时，这犹如从输入端口输入变量  $\omega$ ，而在不同“窗口”（输出端口）观察频率  $\omega$  的响应，所以，这些网络函数的频率特性又统称为电路的频率响应，为了便于比较不同参数的 RLC 串联电路的频率响应之间在性能上的差异，纵、横坐标都采用相对于谐振点的比值(倍率)作为绘制频率特性的坐标系。由于已设定 $U_{\mathrm{s}}(\mathrm{j}\omega)=U_{\mathrm{s}}(\mathrm{j}\omega_{0})$ ，所以上述电压比的模就表示任一频率时的输出电压与其谐振点的输入电压之比值；而横坐标也用与谐振频率 $\omega_{0}$ 的比值表示，即 $\eta=\frac{\omega}{\omega_{0}},\omega=\eta\omega_{0}$ 。这样，所有的RLC电路都在 $\eta=1$ 处谐振，都在同一个相对尺度下来比较相互频率特性的差异，这一共同的尺度也表示各谐振电路的偏谐程度（偏离谐振点程度），下面用新坐标系来分析上述网络函数的频率特性，这样绘制的频率响应曲线，称为通用曲线。

![](images/page_289_image_22.jpg)

RLC 串联电路的频率响应

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

![](images/page_290_chart_9.jpg)

<details>
<summary>line</summary>

| \(\eta\) | Curve (1) | Curve (2) |
| --- | --- | --- |
| ~0.5 | — | \(1/\sqrt{2}\) |
| 1 | 1 | 1 |
| ~1.5 | — | \(1/\sqrt{2}\) |
</details>

(a)

![](images/page_290_chart_11.jpg)

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

两条幅频特性如图11-7所示，图中粗虚线表示 $Q \leqslant 0.707$ 时的幅频特性。从图中可以看出，$H_{C}(\mathrm{j}\eta)$ 为低通函数，当 $Q \gg 1$ 时，可求得上截止频率 $\omega_{\mathrm{j}} = 1.55\omega_{0}$，其通频带域 $0 \leqslant \omega \leqslant \omega_{\mathrm{j}}$；函数 $H_{L}(\mathrm{j}\eta)$ 为高通函数，当 $Q \gg 1$ 时，求得下截止频率 $\omega_{\mathrm{j}} = \frac{\omega_{0}}{1.55} = 0.645\omega_{0}$，通频带域为 $\omega_{\mathrm{j}} \leqslant \omega < \infty$，当 $Q > 0.707$ 时，两者都有大于 $Q$ 且相等的峰值，当 $Q$ 增大时，$\eta_{C2}, \eta_{L2}$ 都向 $\eta = 1$ 靠拢，峰值增高，图中 $a, b, c$ 三点在抬高的同时，逐渐向 $c$ 点合拢，当 $Q \to \infty$，三点合于无穷远。

![](images/page_293_chart_4.jpg)

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

![](images/page_293_image_21.jpg)

RLC并联谐振电路

$$
f _ {0} = \frac {1}{2 \pi \sqrt {L C}}
$$

该频率称为电路的固有频率。

并联谐振时,输入导纳  $Y(\mathrm{j}\omega_{0})$  为最小

$$
Y (\mathrm{j} \omega_ {0}) = G + \mathrm{j} \left(\omega_ {0} C - \frac {1}{\omega_ {0} L}\right) = G
$$

或者说输入阻抗最大, $Z(j\omega_{0})=R$ ,所以谐振时端电压达最大值

![](images/page_294_image_7.jpg)

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

![](images/page_294_image_9.jpg)

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

显然，只有当 $1 - \frac{CR^2}{L} > 0$ ，即 $R < \sqrt{\frac{L}{C}}$ 时，$\omega_0$ 才是实数，所以 $R > \sqrt{\frac{L}{C}}$ 时，电路不会发生谐振。该电路调节电阻可改变电路的固有频率。

谐振时的输入导纳为

$$
Y (\mathrm{j} \omega_ {0}) = \frac {R}{| Z (\mathrm{j} \omega_ {0}) | ^ {2}} = \frac {C R}{L}
$$

可以证明,该电路发生谐振时的输入导纳不是最小值(即输入阻抗不是最大值),所以谐振时的端电压不是最大值。这种电路只有当  $R \ll \sqrt{\frac{L}{C}}$  时,它发生谐振时的特点才与图 11-8(a) 所示 GLC 并联谐振的特点接近。

![](images/page_295_image_7.jpg)

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

对电路和系统的频率特性进行分析时,为了直观地观察频率特性随频率变化的趋势和特征,需要准确地描绘频率响应曲线,这往往不是一件容易的事。工程上常采用对数坐标绘制频响曲线,这样做可以在不同频域内用直线近似代替曲线,使曲线局部直线化,整个曲线则折线化,从而使频响曲线变得易于描绘。这种用对数坐标描绘的频率响应图就称为频响波特图。

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① H. W. Bode 最先使用这种图形, 故称波特图。</span></small>

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
(3) $-20\lg \left(\left|1 + \mathrm{j}\frac{\omega}{2}\right|\right)$ 可由两段直线逼近。当 $\omega \rightarrow 0$ 时，$-20\lg 1 = 0$；当 $\omega \rightarrow \infty$ 时，$-20 \lg \left( \left| 1 + j \frac{\omega}{2} \right| \right) \approx -20 \lg \left( \frac{\omega}{2} \right)$ 。这样，以 $\omega = 2$ 为分界点，在 $\omega < 2$ 区间，该项可用斜率为零的直线逼近；在 $\omega > 2$ 区间，该项用斜率为 $-20 \mathrm{~dB} / 10$ 倍频的直线逼近。

![](images/page_296_image_22.jpg)

<details>
<summary>text_image</summary>

Technical diagram of a mechanical assembly with labeled components and cross-sectional views
</details>

(4) $-20\lg \left(\left|1 + \mathrm{j}\frac{\omega}{10}\right|\right)$ 的分析与(3)类似，以 $\omega = 10$ 为分界点，在 $\omega < 10$ 区间，该项用斜率为零的直线逼近；在 $\omega > 10$ 区间，该项用斜率等于-20dB/10倍频的直线逼近。

将以上四项叠加,就得到如图 11-10(a) 中实线所示的幅频波特图。

![](images/page_297_chart_6.jpg)

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

![](images/page_297_chart_8.jpg)

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

(2)  $-\arctan\left(\frac{\omega}{2}\right)=\left\{\begin{aligned}&0&\omega=0\\ &-45^{\circ}&\omega=2\\ &-90^{\circ}&\omega\rightarrow\infty\end{aligned}\right.$

在 $0 \leqslant \omega \leqslant 0.2$ 区间，$-\arctan \left(\frac{\omega}{2}\right) \approx 0$，该项用值为 $0^{\circ}$ 的水平直线逼近；当 $\omega = 2$ 时，$-\arctan 1 = -45^{\circ}$；当 $\omega = 20$ 时，$-\arctan 10 \approx -90^{\circ}$。即在 $0.2 \leqslant \omega \leqslant 20$ 区间，$-\arctan \left(\frac{\omega}{2}\right)$ 可用斜率为 $-45^{\circ} / 10$ 倍频的直线逼近。在 $\omega \geqslant 20$ 区间，该项用值为 $-90^{\circ}$ 的水平直线逼近。三段逼近直线的交点在 $\omega = 0.2$ 处和 $\omega = 20$ 处。

(3) $-\arctan \left(\frac{\omega}{10}\right)$ 的分析与(2)类似, 即在 $1 \leqslant \omega \leqslant 100$ 区间, $-\arctan \left(\frac{\omega}{10}\right)$ 用斜率为 $-45^{\circ} / 10$ 倍频的直线逼近; 在 $0 \leqslant \omega \leqslant 1$ 区间, 该项用值为 $0^{\circ}$ 的水平直线逼近; 在 $\omega \geqslant 100$ 区间, 该项用值为 $-90^{\circ}$ 的水平直线逼近。

将以上三条折线叠加,就得到如图 11-10(b) 实线所示的相频波特图。

## §11-6 滤波器简介

工程上根据输出端口对信号频率范围的要求,设计专门的网络,置于输入-输出端口之间,使输出端口所需要的频率分量能够顺利通过,而抑制不需要的频率分量,这种具有选频功能的中间网络,工程上称为滤波器。通常将希望保留的频率范围称为通带,将希望抑制的频率范围称为阻带。根据通带和阻带在频率范围中的相对位置,滤波器分为低通、高通、带通和带阻四种类型。

工程上利用电感 $L$ 和电容 $C$ 彼此相反而又互补的频率特性, 先设计具有一定滤波功能的“单元电路”, 然后再用搭“积木”方式(如并联、级联等), 连接成各种各样的滤波器网络。如图 11-11(a) 所示为 L 形低通滤波器, 图 11-11(b)(c) 所示 T 形和 $\pi$ 形电路又是 L 形电路的一种镜像连接电路。图 11-12(a) 所示为高通滤波器的单元电路(与图 11-11 类似)。图 11-13 所示为 LC 串并联谐振电路构成的带通滤波器, 它利用谐振电路的频率特性, 只允许谐振频率邻域内的信号通过。图 11-14 所示电路为带阻滤波器, 它阻止谐振频率邻域内的信号通过。

![](images/page_298_image_9.jpg)

<details>
<summary>chemical</summary>

Simple LC circuit diagram with inductor L and capacitor C
</details>

(a) L形

![](images/page_298_image_11.jpg)

<details>
<summary>chemical</summary>

Electrical circuit diagram with inductors and capacitors labeled L and C
</details>

(b) T形

![](images/page_298_image_13.jpg)

<details>
<summary>chemical</summary>

Electrical circuit diagram with inductors and capacitors labeled L and C
</details>

(c) $\pi$ 形

图11-11 低通滤波器的单元电路

![](images/page_299_image_2.jpg)

(a) L形

![](images/page_299_image_4.jpg)

<details>
<summary>chemical</summary>

Electrical circuit diagram with capacitors and inductors labeled C, L, and dashed line
</details>

(b) T形

![](images/page_299_image_6.jpg)

<details>
<summary>chemical</summary>

Electrical circuit diagram with capacitors and inductors labeled C and L
</details>

(c) $\pi$ 形

图 11-12 高通滤波器的单元电路

![](images/page_299_image_9.jpg)

<details>
<summary>chemical</summary>

Electrical circuit diagram with inductors L1 and L2, capacitors C1 and C2, and ground connections
</details>

图 11-13 带通滤波器

![](images/page_299_image_11.jpg)

<details>
<summary>chemical</summary>

Electrical circuit diagram with inductors and capacitors labeled L1, C1, L2, C2
</details>

图 11-14 带阻滤波器

上述无损耗 LC 滤波器中的电感元件体积较大,难以使滤波器小型化和集成化。

目前，在滤波器的设计中，已大量使用小型的片式电路元件，可以使滤波器小型化。随着电路和系统集成化的发展，滤波器的设计中，已广泛采用运算放大器，或其他VCVS有源器件，不再使用电感元件，称为RC有源滤波器，实现了滤波器的集成化，有关这方面的初步知识，读者可参阅本章后面的有关习题。滤波器的设计需要专门的理论知识，本书不做论述。

![](images/page_299_image_15.jpg)

## 思考题

11-1 为什么电路响应的幅值和相位会随着频率的变化而变化？电路的这个性质有哪些应用？

11-2 驱动点阻抗和导纳与正弦一端口的阻抗和导纳的概念是相同的吗？

11-3 使 RLC 串联电路发生谐振的方法有哪些？如何避免发生串联谐振？

11-4 RLC 串联电路发生谐振时,电路具有哪些特征?

11-5 RLC 串联电路中各元件上的电压响应的频率特性如何？

11-6 RLC 并联电路发生谐振时,电路具有哪些特征?

11-7 试简单阐述滤波器的用途？

![](images/page_299_image_24.jpg)

## 习题

11-1 求题 11-1 图所示电路端口 1-1' 的驱动点阻抗  $\frac{\dot{U}}{\dot{I}_{1}}$ 、转移电流比  $\frac{\dot{I}_{c}}{\dot{I}_{1}}$  和转移阻

抗 $\frac{\dot{U}_{2}}{\dot{I}_{1}}$ 。

11-2 求题 11-2 图所示电路的转移电压比  $\frac{\dot{U}_{2}}{\dot{U}_{1}}$  和驱动点导纳  $\frac{\dot{I}_{1}}{\dot{U}_{1}}$ 。

![](images/page_300_image_5.jpg)

<details>
<summary>text_image</summary>

i₁ 2 Ω 1 Ω
+     ↓
U̇      1 F     2 H
-       +
      -
</details>

题11-1图

![](images/page_300_image_7.jpg)

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

![](images/page_300_image_20.jpg)

(a)

![](images/page_300_image_22.jpg)

<details>
<summary>chemical</summary>

Simple LC circuit diagram with inductor L and capacitor C
</details>

(b)

![](images/page_300_image_24.jpg)

<details>
<summary>chemical</summary>

Electrical circuit diagram with inductors L1 and L2, and capacitor C1
</details>

(c)

![](images/page_300_image_26.jpg)

<details>
<summary>chemical</summary>

Simple LC circuit diagram with inductor L1 and capacitors C1 and C2
</details>

(d)

题11-6图

11-7 RLC 串联电路中, $L = 50 \mu \mathrm{H}, C = 100 \mathrm{pF}, Q = 50 \sqrt{2} = 70.71$, 电源 $U_{\mathrm{s}} = 1 \mathrm{mV}$。求电路的谐振频率 $f_{0}$、谐振时的电容电压 $U_{C}$ 和通带 $BW$。
11-8 RLC 串联电路谐振时，已知 $BW = 6.4\mathrm{kHz}$，电阻的功耗 $2\mu \mathrm{W}, u_{\mathrm{s}}(t) =$

$\sqrt{2}\cos(\omega_{0}t)$  mV 和 C=400 pF。求 L、谐振频率  $f_{0}$  和谐振时电感电压  $U_{L}$ 。

11-9 RLC 串联电路中, $U_{s}=1\ V$ , 电源频率 $f_{s}=1\ MHz$ , 发生谐振时 $I(j\omega_{0})=100\ mA$ , $U_{c}(j\omega_{0})=100\ V$ , 试求 R、L 和 C 的值, Q 值和通带 BW。

11-10 RLC 并联谐振时， $f_{0}=1\ \mathrm{kHz}, Z(\mathrm{j}\omega_{0})=100\ \mathrm{k}\Omega, BW=100\ \mathrm{Hz}$ ，求 R、L 和 C。
11-11 求题 11-11 图所示电路的谐振频率及各频段的电抗性质。

![](images/page_301_image_8.jpg)

<details>
<summary>chemical</summary>

Electrical circuit diagram with inductors L1 and L2, capacitors C1 and C2, and ground connection
</details>

(a)

![](images/page_301_image_10.jpg)

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

![](images/page_301_image_16.jpg)

<details>
<summary>text_image</summary>

i_s
R
L
C
R_L
</details>

题 11-12 图

![](images/page_301_image_18.jpg)

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

![](images/page_301_image_24.jpg)

<details>
<summary>chemical</summary>

Electrical circuit diagram with resistors R1 and R2, inductor L1, and capacitor C2
</details>

题11-14图

11-15 求题 11-15 图所示电路的转移电压比  $\frac{\dot{U}_{2}}{\dot{U}_{1}}$ 。

![](images/page_302_image_4.jpg)

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

![](images/page_302_image_6.jpg)

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

![](images/page_302_image_10.jpg)

(a)

(b)

题 11-16 图

11-17 题 11-17 图所示电路中, $RC = 1 \mathrm{~s}$ 。求 $\frac{\dot{U}_2}{\dot{U}_1}$ 和 $\frac{U_2}{U_1} - \omega$ 。

![](images/page_302_image_15.jpg)

<details>
<summary>chemical</summary>

Electrical circuit diagram with two resistors and capacitors in parallel configuration
</details>

题 11-17 图

![](images/page_303_image_0.jpg)

<details>
<summary>natural_image</summary>

Pure mechanical assembly diagram without any text, numbers, or symbols
</details>

11-18 题 11-18 图(a)所示系统的网络函数 $H(\mathrm{j}\omega)=\frac{\dot{U}_{2}}{\dot{U}_{s}}$, 其幅频特性 $|H(\mathrm{j}\omega)|-\omega$ 和相频特性 $\varphi(\mathrm{j}\omega)-\omega$ 如题 11-18 图(b)所示。求当 $u_{\mathrm{s}}=10-6.4\sin t-3.2\sin(2t)\sim2.1\sin(3t)+\cdots$ 时, 输出 $u_{2}$。

![](images/page_303_chart_4.jpg)

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

![](images/page_303_image_6.jpg)

第十一章部分习题答案

11-19 作下列网络函数  $H(j\omega)$  的波特图。

(1) $H(\mathrm{j}\omega) = \frac{1}{10 + \mathrm{j}\omega}$。
(2) $H(\mathrm{j}\omega) = \frac{5(\mathrm{j}\omega + 2)}{\mathrm{j}\omega(\mathrm{j}\omega + 10)}$。

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

![](images/page_304_image_13.jpg)

三相电路

$$
u _ {\mathrm{A}} + u _ {\mathrm{B}} + u _ {\mathrm{C}} = 0 \quad \text {或} \quad \dot {U} _ {\mathrm{A}} + \dot {U} _ {\mathrm{B}} + \dot {U} _ {\mathrm{C}} = 0
$$

对称三相电压源是由三相发电机提供的(我国三相系统电源频率 $f=50\ Hz$ , 入户电压为220 V, 而日、美、欧洲等国为60 Hz, 110 V)。

图 12-1(a) 所示为三相电压源的星形连接方式, 简称星形或 Y 形电源。从 3 个电压源正极性端子 A、B、C 向外引出的导线称为端线, 从中性点 N 引出的导线称为中性线 (旧称零线)。把三相电压源依次连接成一个回路, 再从端子 A、B、C 引出端线, 如图 12-1(b) 所示, 就成为三相电源的三角形联结, 简称三角形或  $\Delta$  形电源。三角形电源不能引出中性线。

![](images/page_305_image_6.jpg)

<details>
<summary>text_image</summary>

ÛA + A
- ÛB + B
N - ÛC + C
N
</details>

(a)

![](images/page_305_image_8.jpg)

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

![](images/page_305_chart_10.jpg)

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

![](images/page_305_image_12.jpg)

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

从对称三相电源的3个端子引出具有相同阻抗的3条端线(或输电线)，把一些对称三相负载连接在端线上就形成了对称三相电路。图12-2(a)(b)为两个对称三相电路的示例。图(a)中的三相电源为星形电源，负载为星形负载，称为Y-Y连接方式(实线所示部分)；图(b)中，三相电源为星形电源，负载为三角形负载，称为Y-Δ连接方式。还有  $\Delta-Y$  和  $\Delta-\Delta$  连接方式。

在 Y-Y 联结中,如把三相电源的中性点 N 和负载的中性点 N' 用一条具有阻抗为  $Z_{N}$  的中性线连接起来,如图 12-2(a) 中虚线所示,这种连接方式称为三相四线制方式。上述其余连接方式均属三相三线制。

![](images/page_306_image_4.jpg)

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

![](images/page_307_image_12.jpg)

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

![](images/page_307_image_14.jpg)

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

最后还必须指出,所有关于电压、电流的对称性以及上述对称相值和对称线值之间关系的论述,只能在指定的顺序和参考方向的条件下,才能以简单有序的形式表达出来,而不能任意设定(理论上可以),否则将会使问题的表述变得杂乱无序。

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

![](images/page_308_image_14.jpg)

<details>
<summary>text_image</summary>

- \u221a_A + \nZ_1 \u221a_I_A \u221a_Z
\u221a_{N'N} = 0
N N'
</details>

图 12-4 一相计算电路

这表明,对称的 Y-Y 三相电路,在理论上不需要中性线,可以移去。而在任一时刻, $i_{A}$ 、 $i_{B}$ 、 $i_{C}$ 中至少有一个为负值,对应此负值电流的输电线则作为对称电流系统在该时刻的电流回线。

对于其他连接方式的对称三相电路,可以根据星形和三角形的等效互换,化成对称的 Y-Y 三相电路,然后用一相计算法求解。

![](images/page_308_image_18.jpg)

对称三相电路的计算

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

![](images/page_309_image_19.jpg)

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

![](images/page_310_image_10.jpg)

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

![](images/page_310_image_12.jpg)

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

![](images/page_310_image_18.jpg)

不对称三相电路的概念

![](images/page_311_image_0.jpg)

<details>
<summary>natural_image</summary>

Abstract line drawing of a windmill with blades and a flag (no text or symbols)
</details>

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

![](images/page_311_image_26.jpg)

三相电路的
功率

它们的和为

$$
p = p _ {\mathrm{A}} + p _ {\mathrm{B}} + p _ {\mathrm{C}} = 3 U _ {\mathrm{AN}} I _ {\mathrm{A}} \cos \varphi = 3 P _ {\mathrm{A}}
$$

此式表明,对称三相电路的瞬时功率是一个常量,其值等于平均功率。这是对称三相电路的一个优越的性能。习惯上把这一性能称为瞬时功率平衡。

在三相三线制电路中,不论对称与否,都可以使用两个功率表的方法测量三相功率(称为二瓦计法)。两个功率表的一种连接方式如图12-7所示。使线电流从\*端分别

流入两个功率表的电流线圈(图示为  $\dot{I}_{A}, \dot{I}_{B}$ )，它们的电压线圈的非 \* 端共同接到非电流线圈所在的第 3 条端线上(图示为 C 端线)。可以看出, 这种测量方法中功率表的接线只触及端线, 而与负载和电源的连接方式无关。

可以证明图中两个功率表读数的代数和为三相三线制中右侧电路吸收的平均功率。

![](images/page_312_image_8.jpg)

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

![](images/page_313_image_15.jpg)

## 思考题

12-1 为什么现有电力系统采用三相制？

12-2 星形联结的三相电源和负载,如果中性线电流为零,能否表明三相电压源的相电压是对称的?

12-3 在实际的三相供电系统中,除了电动机外,很多负载是单相的,如何布置负载,可使三相负载尽可能对称?

12-4 当三相系统的负载不对称时,为什么还要保证三相电压尽可能对称?

12-5 对称三相电路的瞬时功率是常量,为什么还存在无功功率?

12-6 对于不对称的三相四线制系统,如何测量功率?

12-7 一般家庭或办公室都是使用单相交流电,但配电网却是三相交流电。试问,当一个住宅小区或一栋建筑的电源是三相交流电,如何使得进入各用户的是单相交流电,而电源端看起来是一个对称的三相负载?

![](images/page_314_image_4.jpg)

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

![](images/page_314_image_18.jpg)

<details>
<summary>chemical</summary>

Electrical circuit diagram with resistors, inductors, and mutual inductance symbols
</details>

题12-4图

![](images/page_314_image_20.jpg)

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

(1) 负载吸收的复功率  $\bar{S}$  和阻抗 Z。
(2) 开关 S 打开后, 功率表的读数。

![](images/page_315_image_6.jpg)

<details>
<summary>text_image</summary>

A○─Z₁─A′─
B○─Z₁─B′─
C○─Z₁─C′─
三相
电动机
</details>

题12-6图

![](images/page_315_image_8.jpg)

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

![](images/page_315_image_18.jpg)

<details>
<summary>text_image</summary>

A○─ Zambia
      S
      Z₁
B○─ Z     N′
C○─ Z
</details>

题12-8图

![](images/page_315_image_20.jpg)

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

![](images/page_316_image_2.jpg)

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

![](images/page_316_image_9.jpg)

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

![](images/page_316_image_11.jpg)

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

![](images/page_316_image_14.jpg)

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

\*12-15 试设计一个居民小区的配电站。假设小区住宅楼楼层分别为18层、24层、32层等，各有若干栋。每栋楼有2\~3个单元，住宅户型有 $105\mathrm{m}^2$ 、 $120\mathrm{m}^2$ 、 $140\mathrm{m}^2$ 三种。请读者自己给出小区共有多少栋楼，每栋楼各类户型有多少套。参考第一章习题1-19的家用电器用电量表，综合如下因素，设计出该小区共需多大容量的变压器、各住户导线及变压器出线导线、开关容量、电容器组容量等。

(1) 各栋楼的位置, 配电站的位置。
(2) 除了居民家中用电负荷外, 还要考虑公用负荷。例如每个单元需 1\~2 部电梯, 楼道和小区照明设施等。
(3) 不能简单将家中用电设备容量直接相加作为用户的总负荷, 要考虑同时率的问题。
（4）小区配电室是三相电源，但用户家中负荷基本上是单相负荷。应考虑三相电源如何分配至各楼层的用户，以尽可能满足三相负载对称的要求。

(5) 功率因数提高, 确定电容器组的容量。

(6) 可能的用电设施的故障。

(7) 根据自定的设计目标, 确定变压器容量的计算值, 再通过查阅设计手册, 确定实际变压器的型号和台数。

\*12-16 选定一个大的工业用户, 工业用户的特点是大多数负荷为三相对称负载, 但车间和办公区的照明等少量负荷是单相的, 根据所选企业的生产情况, 包括生产车间用电设备、公用电梯、照明、中央空调等用电设备, 设计所选企业配电所的变压器和电容器组的容量和台数。

![](images/page_317_image_13.jpg)

第十二章部分习题答案

# 第十三章

# 非正弦周期电流电路和信号的频谱

![](images/page_318_image_2.jpg)

## 导读

在生产实践和科学实验中,通常会遇到按非正弦规律变化的电源和电信号。另外,如果电路存在非线性元件,即使在正弦电源的作用下,电路中也将产生非正弦周期的电压和电流。

非正弦电流、电压又可分为周期的和非周期的两种。本章主要讨论在非正弦周期电源或电信号的作用下，线性电路的稳态分析和计算方法，并简要地介绍信号频谱的初步概念。首先应用数学中的傅里叶级数（傅氏级数）展开方法，将非正弦周期电压、电流或电信号分解为一系列频率为周期函数频率的正整数倍的正弦量之和表示的无穷级数，再根据线性电路的叠加定理，分别计算每一频率的正弦量单独作用下在电路中产生的同频正弦电流分量和电压分量；把所得分量按时域形式叠加，就可以得到电路在非正弦周期激励下的稳态电流和电压。这种方法称为谐波分析法。最后，将谐波分析法推广用于非正弦非周期信号的分析，简单介绍傅里叶变换。

## §13-1 非正弦周期信号

在生产实践和科学实验中,通常会遇到按非正弦规律变化的电源和信号。例如,通信工程方面传输的各种信号,如收音机、电视机收到的信号电压或电流,它们的波形都是非正弦波。在自动控制、电子计算机等技术领域中用到的脉冲信号也都是非正弦波。本章表13-1所示非正弦周期波形都是工程中常见的例子。

另外,如果电路存在非线性元件,即使在正弦电源的作用下,电路中也将产生非正弦周期的电压和电流。

非正弦电流、电压又可分为周期的和非周期的两种。本章主要讨论在非正弦周期电源或信号的作用下，线性电路的稳态分析和计算方法，并简要地介绍信号频谱的初步概念。

![](images/page_318_image_10.jpg)

非正弦周期
信号

## §13-2 非正弦周期函数分解为傅里叶级数

非正弦周期电流、电压、信号等都可以用周期函数表示，即

$$
f (t) = f (t + n T)
$$

式中 T 为周期函数  $f(t)$  的周期, n 为自然数 0, 1, 2, …。

如果给定的周期函数 $f(t)$ 满足狄里赫利条件，即（1）周期函数的极值点的数目为有限个；(2）间断点的数目为有限个；(3）在一个周期内绝对可积，即有

$$
\int_ {0} ^ {T} \left| f (t) \right| \mathrm{d} t <   \infty (\text {有界})
$$

它就能展开成一个收敛的傅里叶级数,即

$$
\begin{array}{l} f (t) = \frac {a _ {0}}{2} + \left[ a _ {1} \cos (\omega_ {1} t) + b _ {1} \sin (\omega_ {1} t) \right] + \left[ a _ {2} \cos (2 \omega_ {1} t) + b _ {2} \sin (2 \omega_ {1} t) \right] + \dots + \\ \left[ a _ {k} \cos (k \omega_ {1} t) + b _ {k} \sin (k \omega_ {1} t) \right] + \dots \\ = \frac {a _ {0}}{2} + \sum_ {k = 1} ^ {\infty} \left[ a _ {k} \cos (k \omega_ {1} t) + b _ {k} \sin (k \omega_ {1} t) \right] \tag {13-1} \\ \end{array}
$$

式(13-1)中， $a_{k}$ 项为偶函数， $b_{k}$ 项为奇函数。还可合并成另一种形式（式中 $\omega_{1} = \frac{2\pi}{T}$

$$
\begin{array}{l} f (t) = \frac {A _ {0}}{2} + A _ {1 \mathrm{m}} \cos (\omega_ {1} t + \phi_ {1}) + A _ {2 \mathrm{m}} \cos (2 \omega_ {1} t + \phi_ {2}) + \dots + \\ A _ {k m} \cos (k \omega_ {1} t + \phi_ {k}) + \dots \\ = \frac {A _ {0}}{2} + \sum_ {k = 1} ^ {\infty} A _ {k m} \cos (k \omega_ {1} t + \phi_ {k}) \tag {13-2} \\ \end{array}
$$

不难得出上述两种形式系数之间有如下关系:

$$
a _ {0} = A _ {0}
$$

$$
a _ {k} = A _ {k m} \cos \phi_ {k}
$$

$$
b _ {k} = - A _ {k m} \sin \phi_ {k}
$$

$$
A _ {k m} = \sqrt {a _ {k} ^ {2} + b _ {k} ^ {2}}
$$

$$
\phi_ {k} = \arctan \left(\frac {- b _ {k}}{a _ {k}}\right)
$$

$$
A _ {k \mathrm{m}} \mathrm{e} ^ {\mathrm{j} \phi_ {k}} = a _ {k} - \mathrm{j} b _ {k}
$$

傅里叶级数是一个无穷三角级数。式(13-2)的第1项 $\frac{A_0}{2}$ 称为周期函数 $f(t)$ 的恒