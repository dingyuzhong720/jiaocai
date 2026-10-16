输入差模信号时的电压放大倍数称为差模放大倍数，记作 $A_{d}^{①}$ ，定义为

$$
A _ {\mathrm{d}} = \frac {\Delta u _ {\mathrm{0d}}}{\Delta u _ {\mathrm{1d}}} \tag {3.3.6}
$$

式中的 $\Delta u_{\mathrm{Od}}$ 是 $\Delta u_{\mathrm{Id}}$ 作用下的输出电压。从图（b）中可知，$\Delta u_{\mathrm{Id}} = 2\Delta i_{\mathrm{B1}}(R_{\mathrm{b}} + r_{\mathrm{be}})$，$\Delta u_{\mathrm{Od}} = -2\Delta i_{\mathrm{Cl}}\left(R_{\mathrm{c}} / / \frac{R_{\mathrm{L}}}{2}\right)$，所以

$$
A _ {\mathrm{d}} = - \frac {\beta \left(R _ {\mathrm{c}} / / \frac {R _ {\mathrm{L}}}{2}\right)}{R _ {\mathrm{b}} + r _ {\mathrm{be}}} \tag {3.3.7}
$$

由此可见,虽然差分放大电路用了两只晶体管,但它的电压放大能力只相当于单管共射放大电路。因而,差分放大电路是以牺牲一只管子的放大倍数为代价来换取低温漂的效果的。

根据输入电阻的定义,从图(b)可以看出

$$
R _ {\mathrm{i}} = 2 (R _ {\mathrm{b}} + r _ {\mathrm{be}}) \tag {3.3.8}
$$

它是单管共射放大电路输入电阻的两倍。

电路的输出电阻

$$
R _ {\mathrm{o}} = 2 R _ {\mathrm{c}} \tag {3.3.9}
$$

也是单管共射放大电路输出电阻的两倍。

为了综合考察差分放大电路对差模信号的放大能力和对共模信号的抑制能力,特引入了一个指标参数——共模抑制比,记作 $K_{CMR}$ ,定义为

$$
K _ {\mathrm{CMR}} = \left| \frac {A _ {\mathrm{d}}}{A _ {\mathrm{c}}} \right| \tag {3.3.10}
$$

其值愈大，说明电路性能愈好。在图3.3.3所示电路中，若电路参数理想对称，由于 $A_{\mathrm{c}} = 0$ $K_{\mathrm{CMR}} = \infty$ 。

## 4. 电压传输特性

放大电路输出电压与输入电压之间的关系曲线称为电压传输特性,即

$$
u _ {0} = f (u _ {1}) \tag {3.3.11}
$$

将差模输入电压  $\Delta u_{1d}$  按图 3.3.5(a) 接到输入端，并令其幅值由零逐渐增加时，输出端的  $\Delta u_{0d}$  也将出现相应的变化，画出二者的关系，如图 3.3.6 中的实线 $^{②}$ 所示。可以看出，只有在中间一段二者是线性关系，斜率就是式 (3.3.6) 所表示的差模放大倍数。当输入电压幅值过大时，输出电压就会产生失真，若再加大  $\Delta u_{1d}$ ，则  $\Delta u_{0d}$  将趋于不变，其数值取决于电源电压  $V_{CC}$ 。

若改变  $\Delta u_{Id}$  的极性, 则可得到另一条如图 3.3.6 中虚线所示的曲线, 它与实线完全对称。

![](images/page_160_image_21.jpg)

<details>
<summary>text_image</summary>

uOd
u1d
O
线性关系
</details>

图 3.3.6 差分放大电路的电压传输特性

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 脚注中的 d 是 differential 的字头。</span></small>

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">② 图中曲线可用  $u_{0d}=i_{C}R_{c}$ th $\left(-\frac{u_{1d}}{2U_{T}}\right)$ 来表示。</span></small>

## 三、差分放大电路的四种接法

在图 3.3.3 所示电路中, 输入端与输出端均没有接“地”点, 称为双端输入、双端输出电路。在实际应用中, 为了防止干扰和负载的安全, 常将信号源的一端接地, 或者将负载电阻的一端接地。根据输入端和输出端接地情况不同, 除上述双端输入、双端输出电路外, 还有双端输入、单端输出, 单端输入、双端输出和单端输入、单端输出, 共四种接法。下面分别介绍其电路的特点。

## 1. 双端输入、单端输出电路

图 3.3.7 所示为双端输入、单端输出差分放大电路。与图 3.3.3 所示电路相比，只在输出端不同，其负载电阻  $R_{L}$  的一端接  $T_{1}$  管的集电极，另一端接地。它的输出回路已不对称，因此影响了它的静态工作点和动态参数。

画出图 3.3.7 所示电路的直流通路如图 3.3.8 所示, 图中  $V_{CC}^{\prime}$  和  $R_{c}^{\prime}$  是利用戴维宁定理进行变换得出的等效电源和电阻, 其表达式分别为

$$
V _ {\mathrm{cc}} ^ {\prime} = \frac {R _ {\mathrm{L}}}{R _ {\mathrm{c}} + R _ {\mathrm{L}}} \cdot V _ {\mathrm{cc}} \tag {3.3.12}
$$

$$
R _ {\mathrm{c}} ^ {\prime} = R _ {\mathrm{c}} / / R _ {\mathrm{L}} \tag {3.3.13}
$$

![](images/page_161_image_9.jpg)

<details>
<summary>text_image</summary>

Rc
+VCC
Rc
+
RL
uO
T1
-
T2
Rb
uI
-
Re
-VEE
</details>

图 3.3.7 双端输入、单端输出差分放大电路

![](images/page_161_image_11.jpg)

<details>
<summary>text_image</summary>

+V'CC
R'c
UCCQ1
Rc
+VCC
T1
T2
Rb
Re
-VEE
</details>

图 3.3.8 图 3.3.7 所示电路的直流通路

虽然由于输入回路参数对称，使静态电流 $I_{\mathrm{BQ1}} = I_{\mathrm{BQ2}}$，从而 $I_{\mathrm{CQ1}} = I_{\mathrm{CQ2}}$；但是，由于输出回路的不对称性，使 $\mathrm{T}_{1}$ 管和 $\mathrm{T}_{2}$ 管的集电极电位 $U_{\mathrm{CQ1}} \neq U_{\mathrm{CQ2}}$，从而使管压降 $U_{\mathrm{CEQ1}} \neq U_{\mathrm{CEQ2}}$。由图3.3.8可得

$$
U _ {\mathrm{CQ1}} = V _ {\mathrm{CC}} ^ {\prime} - I _ {\mathrm{CQ}} R _ {\mathrm{c}} ^ {\prime} \tag {3.3.14}
$$

$$
U _ {\mathrm{CQ2}} = V _ {\mathrm{CC}} - I _ {\mathrm{CQ}} R _ {\mathrm{e}} \tag {3.3.15}
$$

静态工作点  $I_{CQ}$ 、 $I_{BQ}$  和  $U_{CEQ1}$ 、 $U_{CEQ2}$  可通过式(3.3.2)、(3.3.3)、(3.3.4)计算。

因为在差模信号作用时，负载电阻仅取得 $\mathrm{T}_{1}$ 管集电极电位的变化量，所以与双端输出电路相比，差模放大倍数的数值减小。画出图3.3.7所示电路对差模信号的等效电路，如图3.3.9所示。在差模信号作用时，由于 $\mathrm{T}_{1}$ 管与 $\mathrm{T}_{2}$ 管中电流大小相等且方向相反，所以发射极相当于接地。输出电压 $\Delta u_{\mathrm{0d}} = -\Delta i_{\mathrm{C}}(R_{\mathrm{c}} / / R_{\mathrm{L}})$，输入电压 $\Delta u_{\mathrm{Id}} = 2\Delta i_{\mathrm{B}}(R_{\mathrm{b}} + r_{\mathrm{be}})$，因此差模放大倍数

$$
A _ {\mathrm{d}} = \frac {\Delta u _ {\mathrm{0d}}}{\Delta u _ {\mathrm{1d}}} = - \frac {1}{2} \cdot \frac {\beta (R _ {\mathrm{c}} / / R _ {\mathrm{L}})}{R _ {\mathrm{b}} + r _ {\mathrm{be}}} \tag {3.3.16}
$$

电路的输入回路没有变,所以输入电阻  $R_{i}$  仍为  $2(R_{\mathrm{b}} + r_{\mathrm{be}})$ 。

电路的输出电阻  $R_{o}$  为  $R_{c}$ ，是双端输出电路输出电阻的一半。

如果输入差模信号极性不变,而输出信号取自 $T_{2}$ 管的集电极,则输出与输入同相。

![](images/page_162_image_2.jpg)

<details>
<summary>text_image</summary>

Rb
ΔiB
βΔiB
Rc
RL
ΔuOd
+
-
ΔuId
rbe
rbe
Rc
Rb
-
</details>

图 3.3.9 图 3.3.7 所示电路对差模信号的等效电路

当输入共模信号时，由于两边电路的输入信号大小相等且极性相同。所以发射极电阻 $R_{\mathrm{e}}$ 上的电流变化量 $\Delta i_{\mathrm{E}} = 2\Delta i_{\mathrm{E}}$，发射极电位的变化量 $\Delta u_{\mathrm{E}} = 2\Delta i_{\mathrm{E}}R_{\mathrm{e}}$；对于每只管子而言，可以认为是 $\Delta i_{\mathrm{E}}$ 流过阻值为 $2R_{\mathrm{e}}$ 所造成的，如图3.3.10(a)所示。因此，与输出电压相关的 $T_{1}$ 管一边电路对共模信号的等效电路如图3.3.10(b)所示。从图上可以求出

![](images/page_162_image_5.jpg)

<details>
<summary>text_image</summary>

Rc
+VCC
RL
uO
+
Rb
T1
-
T2
Rb
2Re
2Re
+ uic
-
VEE
</details>

(a)

![](images/page_162_image_7.jpg)

<details>
<summary>text_image</summary>

Rb
βΔiB
rbe
2Re
Rc
RL
ΔuIc
ΔuOc
+
</details>

(b)

图 3.3.10 图 3.3.7 所示电路对共模信号的等效电路

(a) 等效变换 (b) 等效电路

$$
A _ {\mathrm{c}} = \frac {\Delta u _ {\mathrm{Oc}}}{\Delta u _ {\mathrm{Ic}}} = - \frac {\beta (R _ {\mathrm{c}} / / R _ {\mathrm{L}})}{R _ {\mathrm{b}} + r _ {\mathrm{be}} + 2 (1 + \beta) R _ {\mathrm{e}}} \tag {3.3.17}
$$

共模抑制比

$$
K _ {\mathrm{CMR}} = \left| \frac {A _ {\mathrm{d}}}{A _ {\mathrm{c}}} \right| = \frac {R _ {\mathrm{b}} + r _ {\mathrm{be}} + 2 (1 + \beta) R _ {\mathrm{e}}}{2 (R _ {\mathrm{b}} + r _ {\mathrm{be}})} \tag {3.3.18}
$$

从式(3.3.17)和式(3.3.18)可以看出， $R_{e}$  愈大， $A_{c}$  的值愈小， $K_{CMR}$  愈大，电路的性能也就愈好。因此，增大  $R_{e}$  是改善共模抑制比的基本措施。

## 2. 单端输入、双端输出电路

图 3.3.11(a) 所示为单端输入、双端输出电路，两个输入端中有一个接地，输入信号加在另一端与地之间。因为电路对于差模信号是通过发射极相连的方式将  $T_{1}$  管的发射极电流传递到  $T_{2}$  管的发射极的，故称这种电路为射极耦合电路。

![](images/page_163_image_2.jpg)

<details>
<summary>text_image</summary>

Rc
+ uO -
RL
+VCC
Rb
T1
T2
Rc
-VEE
uI
-
</details>

(a)

![](images/page_163_image_4.jpg)

<details>
<summary>text_image</summary>

Rc
+ uO -
RL
+ VCC
Rb
T1
T2
Rb
u1/2
+
-
u1/2
-
-
Re
-VEE
u1/2
+
-
u1/2
+
</details>

(b)

图 3.3.11 单端输入、双端输出电路

(a) 电路 (b) 输入信号的等效变换

为了说明这种输入方式的特点,不妨将输入信号进行如下的等效变换。在加信号一端,可将输入信号分为两个串联的信号源,它们的数值均为  $\Delta u_{1}/2$ , 极性相同; 在接地一端,也可等效为两个串联的信号源,它们的数值均为  $\Delta u_{1}/2$ , 但极性相反, 如图(b)所示。不难看出, 同双端输入时一样, 左右两边获得的差模信号仍为  $\pm\Delta u_{1}/2$ ; 但是与此同时, 两边输入了  $\Delta u_{1}/2$  的共模信号。可见, 单端输入电路与双端输入电路的区别在于: 在输入差模信号的同时, 伴随着共模信号的输入。因此, 在共模放大倍数  $A_{c}$  不为零时, 输出端不仅有差模信号作用而得到的差模输出电压, 而且还有共模信号作用而得到的共模输出电压, 即输出电压

$$
\Delta u _ {0} = A _ {\mathrm{d}} \Delta u _ {1} + A _ {\mathrm{c}} \cdot \frac {\Delta u _ {1}}{2} \tag {3.3.19}
$$

当然，若电路参数理想对称，则 $A_{c}=0$ ，即式中的第二项为0，此时 $K_{CMR}$ 将为无穷大。

单端输入、双端输出电路与双端输入、双端输出电路的静态工作点以及动态参数的分析完全相同，这里不再一一推导。

## 3. 单端输入、单端输出电路

图 3.3.12 所示为单端端入、单端输出电路，对于单端输出电路，常将不输出信号一边的  $R_{c}$  省掉。该电路对 Q 点、 $A_{d}$ 、 $A_{c}$ 、 $R_{i}$  和  $R_{o}$  的分析与图 3.3.7 所示电路相同，对输入信号作用的分析与图 3.3.11 所示电路相同。

![](images/page_163_image_14.jpg)

<details>
<summary>text_image</summary>

Rc
+VCC
RL
uo
+
T1
-
T2
Rb
u1
-
Rc
-VEE
</details>

图 3.3.12 单端输入、单端输出电路

由以上分析可知,将四种接法的动态参数特点归纳如下:

(1) 输入电阻均为  $2(R_{\mathrm{b}} + r_{\mathrm{be}})$ 。
（2） $A_{d}$ 、 $A_{c}$ 、 $R_{o}$ 与输出方式有关，双端输出时， $A_{d}$ 见式（3.3.7）， $A_{c}=0, R_{o}=2R_{c}$ ；单端输出时， $A_{d}$ 与 $A_{c}$ 分别见式（3.3.16）、（3.3.17），而 $R_{o}=R_{c}$ 。
（3）单端输入时，在差模信号输入的同时总伴随着共模输入。若输入信号为  $\Delta u_{1}$ ，则  $\Delta u_{Id} = \Delta u_{1}, \Delta u_{Ic} = +\Delta u_{1}/2$ ，输出电压表达式为式(3.3.19)。

## 四、改进型差分放大电路

在差分放大电路中，增大发射极电阻 $R_{\mathrm{e}}$ 的阻值，能够有效地抑制每一边电路的温漂，提高共模抑制比，这一点对于单端输出电路尤为重要。可以设想，若 $R_{\mathrm{e}}$ 为无穷大，则即使是单端输出电路，根据式(3.3.17)和式(3.3.10)，$A_{\mathrm{c}}$ 也为零，$K_{\mathrm{CMR}}$ 也为无穷大。设晶体管发射极静态电流为 $0.5\mathrm{mA}$，则 $R_{\mathrm{e}}$ 中电流就为 $1\mathrm{mA}$；若 $R_{\mathrm{e}}$ 为 $10\mathrm{k}\Omega$，则电源 $V_{\mathrm{EE}}$ 的值约为 $10.7\mathrm{V}$；若 $R_{\mathrm{e}} = 100\mathrm{k}\Omega$，则 $V_{\mathrm{EE}} \approx 100.7\mathrm{V}$，这显然是不现实的。考虑到故障情况下这样高的电源电压会全部加在差分管上，差分管必须选择高耐压管，对于小信号放大电路这是不合理的。差分电路需要既能采用较低的电源电压、又能有很大的等效电阻 $R_{\mathrm{e}}$ 的发射极电路，电流源具备上述特点。

利用工作点稳定电路来取代 $R_{\mathrm{e}}$ ，就得到如图3.3.13所示的具有恒流源的差分放大电路。图中 $R_{1}, R_{2}, R_{3}$ 和 $\mathrm{T}_{3}$ 组成工作点稳定电路，电源 $V_{\mathrm{EE}}$ 可取几伏，电路参数应满足 $I_{2} >> I_{\mathrm{B3}}$ 。这样，$I_{1} \approx I_{2}$，所以 $R_{2}$ 上的电压为

$$
U _ {R 2} \approx \frac {R _ {2}}{R _ {1} + R _ {2}} \cdot V _ {\mathrm{EE}} \tag {3.3.20}
$$

![](images/page_164_image_11.jpg)

<details>
<summary>text_image</summary>

Rc
+ uO -
Rc
+VCC
Rb
T1
T2
Rb
u11
iE1
iE2
I1
IB3
T3
I2
R1
R2
I3
R3
-VEE
u12
</details>

图 3.3.13 具有恒流源的差分放大电路

$T_{3}$ 管的集电极电流

$$
I _ {\mathrm{C3}} \approx I _ {\mathrm{E3}} = \frac {U _ {R 2} - U _ {\mathrm{BE3}}}{R _ {3}} \tag {3.3.21}
$$

若 $U_{\mathrm{BE3}}$ 的变化可忽略不计，则 $I_{\mathrm{C3}}$ 基本不受温度影响。而且，由图3.3.13可知，没有动态信号能够作用到 $\mathrm{T}_{3}$ 管的基极或发射极，因此 $I_{\mathrm{C3}}$ 为恒流，发射极所接电路可以等效成一个恒流源。 $\mathrm{T}_{1}$ 管和 $\mathrm{T}_{2}$ 管的发射极静态电流

$$
I _ {\mathrm{EQ1}} = I _ {\mathrm{EQ2}} = \frac {I _ {\mathrm{C3}}}{2} \tag {3.3.22}
$$

当  $T_{3}$  管输出特性为理想特性时， $T_{3}$  在放大区的输出特性曲线是横轴的平行线时，恒流源的内阻为无大，即相当于  $T_{1}$  管和  $T_{2}$  管的发射极接了一个阻值为无穷大的电阻，对共模信号的负反馈作用无穷大，因此使电路的  $A_{c}=0, K_{CMR}=\infty$ 。

恒流源的具体电路是多种多样的，在集成运放中一般采用3.3.3节所述的电流源电路。若用恒流源符号取代具体电路，则可得到图3.3.14所示差分放大电路。在实际电路中，由于难于做到参数理想对称，常用一个阻值很小的电位器加在两只管子发射极之间，见图中的 $R_{w}$ 。调节电位器滑动端的位置便可使电路在 $u_{11}=u_{12}=0$ 时 $u_{0}=0$ ，所以常称 $R_{w}$ 为调零电位器。

为了获得高输入电阻的差分放大电路,可以将前面所讲电路中的差放管用场效应管取代,如图3.3.15所示。这种电路特别适于做直接耦合多级放大电路的输入级。通常情况下,可以认为其输入电阻为无穷大。和晶体管差分放大电路相同,场效应管差分放大电路也有四种接法,可以采用前面叙述的方法对四种接法进行分析,这里不赘述。

![](images/page_165_image_6.jpg)

<details>
<summary>text_image</summary>

Rc
+ VCC
uO
-
Rc
Rb
T1
Rw
T2
iE1
iE2
I
-Vee
u11
u12
</details>

图 3.3.14 恒流源电路的简化画法及电路调零措施

![](images/page_165_image_8.jpg)

<details>
<summary>text_image</summary>

Rd
+ VDD
RD
uO
-
T1
T2
Rg
u11
RG
iS1
iS2
I
-VSS
Rg
u12
</details>

图 3.3.15 场效应管差分放大电路

【例3.3.1】电路如图3.3.5(a)所示，已知 $R_{\mathrm{b}} = 1\mathrm{k}\Omega ,R_{\mathrm{c}} = 10\mathrm{k}\Omega ,R_{\mathrm{L}} = 5.1\mathrm{k}\Omega ,V_{\mathrm{CC}} = 12\mathrm{V},$ $V_{\mathrm{EE}} = 6\mathrm{V}$ ；晶体管的 $\beta = 100,r_{\mathrm{be}} = 2\mathrm{k}\Omega ,U_{\mathrm{BEQ}} = 0.7\mathrm{V};\mathrm{T}_{1}$ 管和 $\mathrm{T}_{2}$ 管的发射极静态电流均为$0.5\mathrm{mA}_{\circ}$

(1) $R_{e}$ 的取值应为多少？ $T_{1}$ 管和 $T_{2}$ 管的管压降 $U_{CEQ}$ 等于多少？

(2) 计算  $A_{u}^{①}$ 、 $R_{i}$  和  $R_{o}$  的数值；

（3）若将电路改成单端输出，如图3.3.7所示，用直流表测得输出电压 $u_{0}=3\ V$ ，试问输入电压 $u_{1}$ 约为多少？设共模输出电压可忽略不计。

解:(1)根据式(3.3.2)有

$$
R _ {\mathrm{e}} \approx \frac {V _ {\mathrm{EE}} - U _ {\mathrm{BEQ}}}{2 I _ {\mathrm{EQ}}} = \frac {6 - 0 . 7}{2 \times 0 . 5} \mathrm{k} \Omega = 5. 3 \mathrm{k} \Omega
$$

$$
U _ {\mathrm{cQ}} = V _ {\mathrm{cc}} - I _ {\mathrm{cQ}} R _ {\mathrm{e}} \approx (1 2 - 0. 5 \times 1 0) \mathrm{V} = 7 \mathrm{V}
$$

根据式(3.3.4)有

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 因为所加信号为有用信号，也就是差模信号，故 $A_{u}$ 就是 $A_{\mathrm{d}}$。</span></small>

$$
U _ {\mathrm{CEQ}} = U _ {\mathrm{CQ}} - U _ {\mathrm{EQ}} \approx (7 + 0. 7) \mathrm{V} = 7. 7 \mathrm{V}
$$

(2) 根据式 $(3.3.7)$ 、 $(3.3.8)$ 、 $(3.3.9)$ ，可计算出动态参数。

$$
A _ {u} = - \frac {\beta \left(R _ {\mathrm{c}} / / \frac {R _ {\mathrm{L}}}{2}\right)}{R _ {\mathrm{b}} + r _ {\mathrm{be}}} = - \frac {1 0 0 \times \frac {1 0 \times 2 . 5 5}{1 0 + 2 . 5 5}}{1 + 2} \approx - 6 8
$$

$$
R _ {\mathrm{i}} = 2 (R _ {\mathrm{b}} + r _ {\mathrm{be}}) = 2 \times (1 + 2) \mathrm{k} \Omega = 6 \mathrm{k} \Omega
$$

$$
R _ {\mathrm{o}} = 2 R _ {\mathrm{c}} = 2 \times 1 0 \mathrm{k} \Omega = 2 0 \mathrm{k} \Omega
$$

（3）由于用直流表测得的输出电压中既含有直流（静态）量又含有变化量（信号作用的结果），所以首先应计算出静态时 $T_{1}$ 管的集电极电位，然后用所测电压减去计算出静态电位就可得到动态电压。根据式(3.3.12)、(3.3.13)、(3.3.14)可得

$$
U _ {\mathrm{CQ1}} = \frac {R _ {\mathrm{L}}}{R _ {\mathrm{c}} + R _ {\mathrm{L}}} \cdot V _ {\mathrm{CC}} - I _ {\mathrm{CQ}} (R _ {\mathrm{c}} / / R _ {\mathrm{L}}) = \left(\frac {5 . 1}{1 0 + 5 . 1} \times 1 2 - 0. 5 \times \frac {1 0 \times 5 . 1}{1 0 + 5 . 1}\right) \mathrm{V} \approx 2. 3 6 \mathrm{V}
$$

$$
\Delta u _ {0} = u _ {0} - U _ {\mathrm{CQ1}} \approx (3 - 2. 3 6) \mathrm{V} = 0. 6 4 \mathrm{V}
$$

已知  $\Delta u_{o}$ ，且共模输出电压可忽略不计，因而若能计算出差模电压放大倍数，就可以得出输入电压的数值。根据式(3.3.16)有

$$
A _ {\mathrm{d}} = - \frac {1}{2} \cdot \frac {\beta (R _ {\mathrm{c}} / / R _ {\mathrm{L}})}{R _ {\mathrm{b}} + r _ {\mathrm{be}}} = - \frac {1}{2} \times \frac {1 0 0 \times \frac {1 0 \times 5 . 1}{1 0 + 5 . 1}}{1 + 2} \approx - 5 6
$$

所以输入电压

$$
\Delta u _ {1} \approx \frac {\Delta u _ {0}}{A _ {\mathrm{d}}} = \left(\frac {0 . 6 4}{- 5 6}\right) \mathrm{V} \approx - 0. 0 1 1 4 \mathrm{V} = - 1 1. 4 \mathrm{mV}
$$

## 3.3.3 电流源电路

集成运放电路中的晶体管和场效应管,除了作为放大管外,还构成电流源电路,为各级提供合适的静态电流;或作为有源负载取代高阻值的电阻,从而提高放大电路的放大能力。本节将介绍常见的电流源电路及有源负载的应用。

## 一、基本电流源电路

## 1. 镜像电流源

图 3.3.16 所示为镜像电流源电路, 它由两只特性完全相同的管子  $T_{0}$  和  $T_{1}$  构成, 由于  $T_{0}$  的管

压降 $U_{\mathrm{CE0}}$ 与其b-e间电压 $U_{\mathrm{BE0}}$ 相等，从而保证 $T_0$ 工作在放大状态，而不进入饱和状态，故集电极电流 $I_{\mathrm{CO}} = \beta_0 I_{\mathrm{BO}}$ 。由于图中 $T_0$ 和 $T_1$ 的b-e间电压相等，故基极电流 $I_{\mathrm{B0}} = I_{\mathrm{B1}} = I_{\mathrm{B}}$ ；而由于电流放大系数 $\beta_0 = \beta_1 = \beta$，故集电极电流 $I_{\mathrm{C0}} = I_{\mathrm{C1}} = I_{\mathrm{C}} = \beta I_{\mathrm{B}}$ 。可见，电路的这种特殊接法，造成 $I_{\mathrm{C1}}$ 和 $I_{\mathrm{C0}}$ 呈镜像关系，因而称此电路为镜像电流源。 $I_{\mathrm{C1}}$ 为输出电流。

电阻 R 中的电流为基准电流, 其表达式为

$$
I _ {\mathrm{R}} = \frac {V _ {\mathrm{CC}} - U _ {\mathrm{BE}}}{R} = I _ {\mathrm{C}} + 2 I _ {\mathrm{B}} = I _ {\mathrm{C}} + 2 \cdot \frac {I _ {\mathrm{C}}}{\beta}
$$

所以集电极电流

![](images/page_166_image_23.jpg)

<details>
<summary>text_image</summary>

+VCC
IR
R
2IB
IC0
T0
IB0
IB1
T1
IC1
</details>

图 3.3.16 镜像电流源

$$
I _ {\mathrm{C}} = \frac {\beta}{\beta + 2} \cdot I _ {\mathrm{R}} \tag {3.3.23}
$$

当 $\beta\gg2$ 时,输出电流

$$
I _ {\mathrm{C}} \approx I _ {\mathrm{R}} = \frac {V _ {\mathrm{CC}} - U _ {\mathrm{BE}}}{R} \tag {3.3.24}
$$

集成运放中纵向晶体管的  $\beta$  均在百倍以上，因而式(3.3.24)成立。当  $V_{CC}$  和 R 的数值一定时， $I_{C1}$  也就随之确定。

镜像电流源具有一定的温度补偿作用,简述如下:

$$
\text {当温度升高时} \xrightarrow [ I _ {\mathrm{C0}} ]{I _ {\mathrm{C1}} \uparrow} \begin{array}{l} I _ {\mathrm{C1}} \downarrow \\ I _ {\mathrm{C0}} \uparrow \end{array} \xrightarrow [ I _ {\mathrm{R}} ]{I _ {\mathrm{R}} \uparrow} \begin{array}{l} U _ {\mathrm{R}} (I _ {\mathrm{R}} R) \uparrow \\ U _ {\mathrm{B}} \downarrow \end{array} \xrightarrow [ I _ {\mathrm{B}} ]{I _ {\mathrm{B}} \downarrow}
$$

当温度降低时,电流、电压的变化与上述过程相反,因此提高了输出电流 $I_{C1}$ 的稳定性。

镜像电流源电路简单，应用广泛。但是，在电源电压 $V_{CC}$ 一定的情况下，若要求 $I_{CI}$ 较大，则根据式(3.3.24)， $I_{R}$ 势必增大，R的功耗也就增大，这是集成电路中应当避免的；若要求 $I_{CI}$ 很小，则 $I_{R}$ 势必也小，R的数值必然很大，这在集成电路中是很难做到的。因此，派生了其它类型的电流源电路。

## 2. 比例电流源

比例电流源电路改变了镜像电流源中 $I_{\mathrm{Cl}} \approx I_{\mathrm{R}}$ 的关系，而使 $I_{\mathrm{Cl}}$ 可以大于 $I_{\mathrm{R}}$，可以小于 $I_{\mathrm{R}}$，与 $I_{\mathrm{R}}$ 成比例关系，从而克服镜像电流源的上述缺点，其电路如图3.3.17所示。

从电路可知

$$
U _ {\mathrm{BE0}} + I _ {\mathrm{E0}} R _ {\mathrm{e0}} = U _ {\mathrm{BE1}} + I _ {\mathrm{E1}} R _ {\mathrm{e1}} \tag {3.3.25}
$$

根据晶体管发射结电压与发射极电流的近似关系 $^{①}$ 可得

$$
U _ {\mathrm{BE}} \approx U _ {\mathrm{T}} \ln \frac {I _ {\mathrm{E}}}{I _ {\mathrm{S}}}
$$

由于  $T_{0}$  与  $T_{1}$  的特性完全相同, 所以

$$
U _ {\mathrm{BE0}} - U _ {\mathrm{BE1}} \approx U _ {\mathrm{T}} \ln \frac {I _ {\mathrm{E0}}}{I _ {\mathrm{E1}}}
$$

代入式(3.3.25)，整理可得

$$
I _ {\mathrm{E1}} R _ {\mathrm{e1}} \approx I _ {\mathrm{E0}} R _ {\mathrm{e0}} + U _ {\mathrm{T}} \ln \frac {I _ {\mathrm{E0}}}{I _ {\mathrm{E1}}}
$$

当  $\beta \gg 2$  时， $I_{C0} \approx I_{E0} \approx I_{R}$ ， $I_{C1} \approx I_{E1}$ ，所以

$$
I _ {\mathrm{Cl}} \approx \frac {R _ {\mathrm{e0}}}{R _ {\mathrm{e1}}} \cdot I _ {\mathrm{R}} + \frac {U _ {\mathrm{T}}}{R _ {\mathrm{e1}}} \ln \frac {I _ {\mathrm{R}}}{I _ {\mathrm{Cl}}} \tag {3.3.26}
$$

在一定的取值范围内,若式(3.3.26)中的对数项可忽略,则

$$
I _ {\mathrm{Cl}} \approx \frac {R _ {\mathrm{e0}}}{R _ {\mathrm{e1}}} \cdot I _ {\mathrm{R}} \tag {3.3.27}
$$

可见，只要改变 $R_{e0}$ 和 $R_{e1}$ 的阻值，就可以改变 $I_{C1}$ 和 $I_{R}$ 的比例关系。式中基准电流

![](images/page_167_image_25.jpg)

<details>
<summary>text_image</summary>

+VCC
IR
R
IC0
T0
IB0+IB1
IB0
IB1
T1
IC1
Re0
IE0
IE1
Re1
</details>

图 3.3.17 比例电流源

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 在忽略基区电阻  $r_{bb'}$  上的电压时，晶体管发射极电流与 b-e 间电压的关系约为  $I_{E} \approx I_{S} e^{\frac{U_{BE}}{U_{T}}}$ 。</span></small>

$$
I _ {\mathrm{R}} \approx \frac {V _ {\mathrm{CC}} - U _ {\mathrm{BE0}}}{R + R _ {\mathrm{e0}}} \tag {3.3.28}
$$

与典型的静态工作点稳定电路一样， $R_{e0}$  和  $R_{e1}$  是电流负反馈电阻，因此与镜像电流源比较，比例电流源的输出电流  $I_{CI}$  具有更高的温度稳定性。

## 3. 微电流源

集成运放输入级放大管的集电极(发射极)静态电流很小,往往只有几十微安,甚至更小。

为了只采用阻值较小的电阻，而又获得较小的输出电流 $I_{\mathrm{C1}}$，可以将比例电流源中 $R_{\mathrm{e0}}$ 的阻值减小到零，便得到如图3.3.18所示的微电流源电路。当 $\beta \gg 1$ 时，$T_1$ 管集电极电流

$$
I _ {\mathrm{Cl}} \approx I _ {\mathrm{E1}} = \frac {U _ {\mathrm{BE0}} - U _ {\mathrm{BE1}}}{R _ {\mathrm{e}}} \tag {3.3.29}
$$

式中 $(U_{\mathrm{BE0}}-U_{\mathrm{BE1}})$ 只有几十毫伏，甚至更小，因此，只要几千欧的 $R_{e}$ ，就可得到几十微安的 $I_{C1}$ 。

图中 $\mathrm{T}_{1}$ 与 $\mathrm{T}_0$ 特性完全相同，根据式(3.3.26)可得

$$
I _ {\mathrm{Cl}} \approx \frac {U _ {\mathrm{T}}}{R _ {\mathrm{e}}} \ln \frac {I _ {\mathrm{R}}}{I _ {\mathrm{Cl}}} \tag {3.3.30}
$$

![](images/page_168_image_11.jpg)

<details>
<summary>text_image</summary>

+VCC
IR
R
IB0+IB1
IC0
T0
IB0
IB1
T1
IC1
Re
IE1
</details>

图 3.3.18 微电流源

在已知  $R_{e}$  的情况下, 上式对  $I_{CI}$  而言是超越方程, 可以通过图解法或累试法解出  $I_{CI}$ 。式中基准电流

$$
I _ {\mathrm{R}} \approx \frac {V _ {\mathrm{CC}} - U _ {\mathrm{BE0}}}{R} \tag {3.3.31}
$$

实际上，在设计电路时，首先应确定 $I_{\mathrm{R}}$ 和 $I_{\mathrm{CI}}$ 的数值，然后求出 $R$ 和 $R_{\mathrm{e}}$ 的数值。例如，在图3.3.18所示电路中，若 $V_{\mathrm{CC}} = 15\mathrm{V}, I_{\mathrm{R}} = 1\mathrm{mA}, U_{\mathrm{BE0}} = 0.7\mathrm{V}, U_{\mathrm{T}} = 26\mathrm{mV}, I_{\mathrm{CI}} = 20\mu \mathrm{A}$；则根据式(3.3.31)可得 $R = 14.3\mathrm{k}\Omega$，根据式(3.3.30)可得 $R_{\mathrm{e}} \approx 5.09\mathrm{k}\Omega$。可见求解过程并不复杂。

## 二、改进型电流源电路

在基本电流源电路中，$\beta$ 足够大时式（3.3.24）、(3.3.26)、(3.3.30)才成立。换言之，在上述电路的分析中均忽略了基极电流对 $I_{\mathrm{C1}}$ 的影响。如果在基本电流源中采用横向PNP型管，则 $\beta$ 只有几倍至十几倍。例如，若镜像电流源中 $\beta = 10$ ，则根据式（3.3.23），$I_{\mathrm{C1}} \approx 0.833 I_{\mathrm{R}}$ ，$I_{\mathrm{C1}}$ 与 $I_{\mathrm{R}}$ 相差很大。为了减小基极电流 $I_{\mathrm{B0}}$ 和 $I_{\mathrm{B1}}$ 的影响，提高输出电流与基准电流的传输精度，稳定输出电流，可对基本镜像电流源电路加以改进。

## 1. 加射极输出器的电流源

在镜像电流源  $T_{0}$  管的集电极与基极之间加一只从射极输出的晶体管  $T_{2}$ ，便构成图 3.3.19 所示电路。利用  $T_{2}$  管的电流放大作用，减小了基极电流  $I_{B0}$  和  $I_{B1}$  对基准电流  $I_{R}$  的分流。

$\mathrm{T_0,T_1}$ 和 $\mathrm{T}_{2}$ 特性完全相同，因而 $\beta_0 = \beta_1 = \beta_2 = \beta$ ，而由于 $U_{\mathrm{BE1}} = U_{\mathrm{BE0}},I_{\mathrm{B1}} = I_{\mathrm{B0}} = I_{\mathrm{B}}$ ，因此输出电流

$$
I _ {\mathrm{C1}} = I _ {\mathrm{C0}} = I _ {\mathrm{R}} - I _ {\mathrm{B2}} = I _ {\mathrm{R}} - \frac {I _ {\mathrm{E2}}}{1 + \beta} = I _ {\mathrm{R}} - \frac {2 I _ {\mathrm{B}}}{1 + \beta} = I _ {\mathrm{R}} - \frac {2 I _ {\mathrm{C1}}}{(1 + \beta) \beta}
$$

整理后可得

$$
I _ {\mathrm{CI}} = \frac {I _ {\mathrm{R}}}{1 + \frac {2}{(1 + \beta) \beta}} \approx I _ {\mathrm{R}} \tag {3.3.32}
$$

若  $\beta=10$ ，则代入上式可得  $I_{C1}\approx0.982I_{R}$ 。说明即使  $\beta$  很小，也可以认为  $I_{C1}\approx I_{R}, I_{C1}$  与  $I_{R}$  保持很好的镜像关系。

在实际电路中,有时在  $T_{0}$  管和  $T_{1}$  管的基极与地之间加电阻  $R_{e2}$  (如图中虚线所画),用来增大  $T_{2}$  管的工作电流,从而提高  $T_{2}$  的  $\beta$ 。此时,  $T_{2}$  管发射极电流  $I_{E2}=I_{B0}+I_{B1}+I_{R_{e2}}$ 。

## 2. 威尔逊电流源

图3.3.20所示电路为威尔逊电流源， $I_{\mathrm{C2}}$ 为输出电流。 $T_{1}$ 管c-e串联在 $T_{2}$ 管的发射极，其作用与典型工作点稳定电路中的 $R_{e}$ 相同。因为c-e间等效电阻非常大，所以可使 $I_{\mathrm{C2}}$ 高度稳定。图中 $T_{0}$ 、 $T_{1}$ 和 $T_{2}$ 管特性完全相同，因而 $\beta_{0}=\beta_{1}=\beta_{2}=\beta,I_{\mathrm{C1}}=I_{\mathrm{C0}}=I_{\mathrm{C}}$ 。

![](images/page_169_image_7.jpg)

<details>
<summary>text_image</summary>

+VCC
IR
R
IC0
T0
IB2
T2
IE2
IB0
RE2
IB1
T1
IC1
</details>

图 3.3.19 加射极输出器的电流源

![](images/page_169_image_9.jpg)

<details>
<summary>text_image</summary>

+VCC
T0
IC0
2IB
A
IC1
IE2
B
IR
R
IB2
T2
IC2
</details>

图 3.3.20 威尔逊电流源

根据各管的电流可知，A 点的电流方程为

$$
I _ {\mathrm{E2}} = I _ {\mathrm{C}} + 2 I _ {\mathrm{B}} = I _ {\mathrm{C}} + \frac {2 I _ {\mathrm{C}}}{\beta}
$$

所以

$$
I _ {\mathrm{C}} = \frac {\beta}{\beta + 2} \cdot I _ {\mathrm{E2}} = \frac {\beta}{\beta + 2} \cdot \frac {1 + \beta}{\beta} I _ {\mathrm{C2}} = \frac {\beta + 1}{\beta + 2} \cdot I _ {\mathrm{C2}}
$$

在 B 点

$$
I _ {\mathrm{R}} = I _ {\mathrm{B2}} + I _ {\mathrm{C}} = \frac {I _ {\mathrm{C2}}}{\beta} + \frac {\beta + 1}{\beta + 2} \cdot I _ {\mathrm{C2}} = \frac {\beta^ {2} + 2 \beta + 2}{\beta^ {2} + 2 \beta} \cdot I _ {\mathrm{C2}}
$$

整理可得

$$
I _ {\mathrm{C2}} = \left(1 - \frac {2}{\beta^ {2} + 2 \beta + 2}\right) I _ {\mathrm{R}} \approx I _ {\mathrm{R}} \tag {3.3.33}
$$

当  $\beta=10$  时， $I_{C2}\approx0.984I_{R}$ ，可见，在  $\beta$  很小时也可认为  $I_{C2}\approx I_{R}$ ， $I_{C2}$  受基极电流影响很小。

## 三、多路电流源电路

集成运放是一个多级放大电路,因而需要多路电流源分别给各级提供合适的静态电流。可以利用一个基准电流去获得多个不同的输出电流,以适应各级的需要。

图 3.3.21 所示电路是在比例电流源基础上得到的多路电流源， $I_{R}$  为基准电流， $I_{C1}$ 、 $I_{C2}$  和  $I_{C3}$  为三路输出电流。根据  $T_{0} \sim T_{3}$  的接法，可得

![](images/page_170_image_3.jpg)

<details>
<summary>text_image</summary>

I_R
R
I_C0
T_0
R_e0
I_E0
T_1
R_e1
I_E1
T_2
R_e2
I_E2
T_3
R_e3
I_E3
I_C1
I_C2
I_C3
</details>

图 3.3.21 基于比例电流源的多路电流源

$$
U _ {\mathrm{BE0}} + I _ {\mathrm{E0}} R _ {\mathrm{e0}} = U _ {\mathrm{BE1}} + I _ {\mathrm{E1}} R _ {\mathrm{e1}} = U _ {\mathrm{BE2}} + I _ {\mathrm{E2}} R _ {\mathrm{e2}} = U _ {\mathrm{BE3}} + I _ {\mathrm{E3}} R _ {\mathrm{e3}}
$$

由于各管的 b-e 间电压  $U_{BE}$  数值大致相等, 因此可得近似关系

$$
I _ {\mathrm{E0}} R _ {\mathrm{e0}} \approx I _ {\mathrm{E1}} R _ {\mathrm{e1}} \approx I _ {\mathrm{E2}} R _ {\mathrm{e2}} \approx I _ {\mathrm{E3}} R _ {\mathrm{e3}} \tag {3.3.34}
$$

当  $I_{E0}$  确定后, 各级只要选择合适的电阻, 就可以得到所需的电流。

图 3.3.22 所示电路为多集电极管构成的多路电流源，T 多为横向 PNP 型管。当基极电流一定时，集电极电流之比等于它们的集电区面积之比。设各集电区面积分别为  $S_{0}$ 、 $S_{1}$ 、 $S_{2}$ ，则

$$
\frac {I _ {\mathrm{C1}}}{I _ {\mathrm{C0}}} = \frac {S _ {1}}{S _ {0}}, \quad \frac {I _ {\mathrm{C2}}}{I _ {\mathrm{C0}}} = \frac {S _ {2}}{S _ {0}} \tag {3.3.35}
$$

![](images/page_170_image_11.jpg)

<details>
<summary>text_image</summary>

+VCC
IB
T
IR
R
IC0
IC1
IC2
</details>

图 3.3.22 多集电极管构成的多路电流源

![](images/page_170_image_13.jpg)

<details>
<summary>text_image</summary>

+VDD
IR
R
ID1
ID2
ID3
T0
T1
T2
T3
</details>

图 3.3.23 MOS 管多路电流源

用场效应管同样可以组成镜像电流源、比例电流源等。在实际电路中，常见图3.3.23所示的MOS管多路电流源。 $T_{0}\sim T_{3}$ 均为N沟道增强型MOS管，它们的开启电压 $U_{\mathrm{GS(th)}}$ 等参数相等，在 $U_{\mathrm{GS0}} = U_{\mathrm{GS1}} = U_{\mathrm{GS2}} = U_{\mathrm{GS3}}$ 时，它们的漏极电流 $I_{D}$ 正比于沟道的宽长比。设宽长比W/L=S，且 $T_{0}\sim T_{3}$ 的宽长比分别为 $S_{0},S_{1},S_{2},S_{3}$ ，则

$$
\frac {I _ {\mathrm{D1}}}{I _ {\mathrm{D0}}} = \frac {S _ {1}}{S _ {0}}, \quad \frac {I _ {\mathrm{D2}}}{I _ {\mathrm{D0}}} = \frac {S _ {2}}{S _ {0}}, \quad \frac {I _ {\mathrm{D3}}}{I _ {\mathrm{D0}}} = \frac {S _ {3}}{S _ {0}} \tag {3.3.36}
$$

可以通过改变场效应管的几何尺寸来获得各种数值的电流。

为了获得更加稳定的输出电流,多路电流源中可以采用带有射极输出器的电流源和威尔逊电流源等形式,这里不赘述。

【例 3.3.2】图 3.3.24 所示电路是型号为 F007 的通用型集成运放的电流源部分。其中$\mathrm{T}_{10}$ 与 $\mathrm{T}_{11}$ 为纵向管； $\mathrm{T}_{12}$ 与 $\mathrm{T}_{13}$ 是横向PNP型管，它们的 $\beta$ 均为5，它们b-e间电压值均约为$0.7\mathrm{V}$ 。试求出各管的集电极电流。

![](images/page_171_image_3.jpg)

<details>
<summary>text_image</summary>

T12
IC12
T13
IC13
+VCC
(+15V)
IR
R5
39 kΩ
IB10+IB11
IC10
T10
R4
3 kΩ
T11
- VCC
(-15V)
</details>

图 3.3.24 F007 中的电流源电路

解: 图中  $R_{5}$  上的电流是基准电流, 根据  $R_{5}$  所在回路可以求出

$$
I _ {\mathrm{R}} = \frac {2 V _ {\mathrm{CC}} - U _ {\mathrm{EB12}} - U _ {\mathrm{BE11}}}{R _ {5}} \approx \left(\frac {3 0 - 0 . 7 - 0 . 7}{3 9}\right) \mathrm{mA} \approx 0. 7 3 \mathrm{mA}
$$

$T_{10}$ 与 $T_{11}$ 构成微电流源,根据式(3.3.30)

$$
I _ {\mathrm{C10}} \approx \frac {U _ {\mathrm{T}}}{R _ {4}} \mathrm{ln} \frac {I _ {\mathrm{R}}}{I _ {\mathrm{C10}}} \approx \left(\frac {2 6}{3} \mathrm{ln} \frac {0 . 7 3}{I _ {\mathrm{C10}}}\right) \mu \mathrm{A}
$$

利用累试法或图解法求出  $I_{C10} \approx 28 \mu A$ 。

$T_{12}$ 与 $T_{13}$ 构成镜像电流源,根据式(3.3.23)有

$$
I _ {\mathrm{C13}} = I _ {\mathrm{C12}} = \frac {\beta}{\beta + 2} \cdot I _ {\mathrm{R}} \approx \frac {5}{5 + 2} \times 0. 7 3 \mathrm{mA} \approx 0. 5 2 \mathrm{mA}
$$

在电流源电路的分析中,首先应求出基准电流 $I_{R},I_{R}$ 常常是集成运放电路中唯一一个通过列回路方程直接估算出的电流;然后利用与 $I_{R}$ 的关系,分别求出各路输出电流。

## 四、以电流源为有源负载的放大电路

在共射(共源)放大电路中,为了提高电压放大倍数的数值,行之有效的方法是增大集电极电阻 $R_{c}$ (或漏极电阻 $R_{d}$ )。然而,为了维持晶体管(场效应管)的静态电流不变,在增大 $R_{c}(R_{d})$ 的同时必须提高电源电压。当电源电压增大到一定程度时,电路的设计就变得不合理了。在集成运放中,常用电流源电路取代 $R_{c}$ (或 $R_{d}$ ),这样在电源电压不变的情况下,既可获得合适的静态电流,对于交流信号,又可得到很大的等效的 $R_{c}$ (或 $R_{d}$ )。由于晶体管和场效应管是有源元件,而上述电路中又以它们作为负载,故称之为有源负载。

## 1. 有源负载共射放大电路

图3.3.25(a)所示为有源负载共射放大电路。 $\mathrm{T}_{1}$ 为放大管， $\mathrm{T}_{2}$ 与 $\mathrm{T}_{3}$ 构成镜像电流源， $\mathrm{T}_{2}$ 是 $\mathrm{T}_{1}$ 的有源负载。设 $\mathrm{T}_{2}$ 与 $\mathrm{T}_{3}$ 管特性完全相同，因而 $\beta_{2} = \beta_{3} = \beta, I_{\mathrm{C2}} = I_{\mathrm{C3}}$ 。基准电流

$$
I _ {\mathrm{R}} = \frac {V _ {\mathrm{CC}} - U _ {\mathrm{EB3}}}{R}
$$

根据式(3.3.23)，空载时 $T_{1}$ 管的静态集电极电流

$$
I _ {\mathrm{CQ1}} = I _ {\mathrm{C2}} = \frac {\beta}{\beta + 2} \cdot I _ {\mathrm{R}}
$$

可见，电路中并不需要很高的电源电压，只要 $V_{CC}$ 与R相配合，就可设置合适的集电极电流 $I_{CQ1}$ 。

![](images/page_172_image_5.jpg)

<details>
<summary>text_image</summary>

T2
+VCC
T3
IC2
+
IR
Rb
u1
-
IC1
T1
RL
uo
-
R
</details>

(a)

![](images/page_172_image_7.jpg)

<details>
<summary>text_image</summary>

Rb
+   iB
Üi   rbe1   β1iB
-   -   -   -   -   -   -   -
rce1   rce2   RL   Ûo
-   -   -   -   -   -
</details>

(b)

图 3.3.25 有源负载共射放大电路

(a) 电路 (b) 交流等效电路

应当指出，输入端的 $u_{1}$ 中应含有直流分量，为 $\mathrm{T}_{1}$ 提供静态基极电流 $I_{\mathrm{BQ1}}, I_{\mathrm{BQ1}}$ 应等于 $I_{\mathrm{CQ1}} / \beta_{1}$，而不应与镜像电流源提供的 $I_{\mathrm{C2}}$ 产生冲突。应当注意，当电路带上负载电阻 $R_{\mathrm{L}}$ 后，由于 $R_{\mathrm{L}}$ 对 $I_{\mathrm{C2}}$ 的分流作用，$I_{\mathrm{CQ1}}$ 将有所变化。

若负载电阻  $R_{L}$  很大，则  $T_{1}$  管和  $T_{2}$  管在 h 参数等效电路中的  $1/h_{22}$  就不能忽略不计，即应考虑 c-e 之间动态电阻中的电流，因此图(a)所示电路的交流等效电路如图(b)所示。这样，电路的电压放大倍数

$$
\dot {A} _ {u} = - \frac {\beta_ {1} (r _ {\mathrm{ce1}} / / r _ {\mathrm{ce2}} / / R _ {\mathrm{L}})}{R _ {\mathrm{b}} + r _ {\mathrm{bel}}} \tag {3.3.37}
$$

若 $R_{\mathrm{L}} \ll (r_{\mathrm{cel}} / / r_{\mathrm{ce2}})$，则

$$
\dot {A} _ {u} \approx - \frac {\beta_ {1} R _ {\mathrm{L}}}{R _ {\mathrm{b}} + r _ {\mathrm{bel}}} \tag {3.3.38}
$$

说明  $T_{1}$  管集电极的动态电流  $\beta_{1}\dot{I}_{b}$  全部流向负载  $R_{L}$ ，有源负载使  $\left|\dot{A}_{u}\right|$  大大提高。

## 2. 有源负载差分放大电路

利用镜像电流源可以使单端输出差分放大电路的差模放大倍数提高到双端输出时的情况，常见的电路形式如图 3.3.26 所示。

图中 N 沟道增强型 MOS 管  $T_{1}$  与  $T_{2}$  为放大管；P 沟道增强型 MOS 管  $T_{3}$  与  $T_{4}$  的特性理想对称，组成镜像电流源作为有源负载， $i_{D3}=i_{D4}$ 。

静态时， $T_{1}$ 管和 $T_{2}$ 管的源极电流 $I_{S1}=I_{S2}=I/2$ ；同样，漏极电流 $I_{D1}=I_{D2}=I/2$ ；因可认为栅极电流为零，故 $I_{D3}=I_{D1}$ ；又因 $I_{D4}=I_{D3}=I_{D1}$ ，所以 $i_{0}=I_{D4}-I_{D2}=0$ 。

当差模信号  $\Delta u_{I}$  输入时，根据差分放大电路的特点，动态漏极电流  $\Delta i_{D1} = -\Delta i_{D2}$ ，而  $\Delta i_{D3} = \Delta i_{D1}$ ；由于  $i_{D4}$  和  $i_{D3}$  的镜像关系， $\Delta i_{D4} = \Delta i_{D3} = \Delta i_{D1}$ ；所以， $\Delta i_{0} = \Delta i_{D4} - \Delta i_{D2} = \Delta i_{D1} - (-\Delta i_{D1}) = 2\Delta i_{D1}$ 。由此可见，输出电流为单端输出时的两倍，这时输出电流与输入电压之比

![](images/page_173_image_2.jpg)

<details>
<summary>text_image</summary>

+VDD
T3
iD3
iD1
T1
T4
iD4
iD2
iQ
+
uI
-
T2
RL uO
-
I
-VSS
</details>

图 3.3.26 利用 MOS 管作差分管的有源负载差分放大电路

$$
A _ {i u} = \frac {\Delta i _ {\mathrm{O}}}{\Delta u _ {\mathrm{I}}} = \frac {2 \Delta i _ {\mathrm{DI}}}{2 \cdot \frac {\Delta u _ {\mathrm{I}}}{2}} = g _ {\mathrm{m}}
$$

式中 $g_{\mathrm{m}}$ 为MOS管的跨导。设 $\mathrm{T}_{1}$ 管和 $\mathrm{T}_{4}$ 管漏-源之间动态电阻分别为 $r_{\mathrm{ds1}}$ 和 $r_{\mathrm{ds4}}$；当电路带负载电阻 $R_{\mathrm{L}}$ 时，其电压放大倍数的分析与图3.3.25所示电路相同，若 $R_{\mathrm{L}}$ 与 $(r_{\mathrm{ds1}} / / r_{\mathrm{ds4}})$ 可以相比，则

$$
A _ {u} = \frac {\Delta u _ {0}}{\Delta u _ {1}} = \frac {\Delta i _ {0}}{\Delta u _ {1}} \cdot (r _ {\mathrm{ds1}} / / r _ {\mathrm{ds4}} / / R _ {\mathrm{L}}) = g _ {\mathrm{m}} (r _ {\mathrm{ds1}} / / r _ {\mathrm{ds4}} / / R _ {\mathrm{L}}) \tag {3.3.39}
$$

因而电压放大倍数与双端输出时的情况相等。

若 $R_{\mathrm{L}} \ll (r_{\mathrm{ds1}} / / r_{\mathrm{ds4}})$，则

$$
A _ {u} = g _ {\mathrm{m}} R _ {\mathrm{L}} \tag {3.3.40}
$$

说明利用镜像电流源作有源负载,不但可将  $T_{1}$  管的漏极电流变化转换为输出电流,而且还将所有变化电流流向负载  $R_{L}$ 。

若将图 3.3.25(a) 所示电路中的晶体管用合适的场效应管取代, 则构成有源负载共源放大电路; 若将图 3.3.26 所示电路中的场效应管用合适的晶体管取代, 则构成双极型管差分放大电路; 它们也具有上述电路的特点, 分析过程相类似, 这里不赘述。

## 3.3.4 直接耦合互补输出级

对于电压放大电路的输出级,一般有两个基本要求:一是输出电阻低,二是最大不失真输出电压尽可能大。分析所学过的各种基本放大电路,共集放大电路满足前一要求,但它带上负载后静态工作点会产生变化,且输出不失真电压也将减小。为了满足上述要求,并且做到输入电压为零时输出电压为零,便产生了双向跟随的互补输出级。

## 一、基本电路

图 3.3.27(a) 所示为互补输出级的基本电路。虽然  $T_{1}$  管为 NPN 型管， $T_{2}$  管为 PNP 型管，但是要求它的参数相同，特性对称。

![](images/page_174_image_2.jpg)

<details>
<summary>text_image</summary>

+VCC
T1
ui
T2
RL
+ uo
-VCC
-
</details>

(a)

![](images/page_174_chart_4.jpg)

<details>
<summary>line</summary>

| uBE | iB |
| --- | --- |
| 0 | 0 |
| ~Low | ~0 |
| ~High | ~High |
</details>

(b)

![](images/page_174_chart_6.jpg)

<details>
<summary>line</summary>

| Time \((\omega t)\) | u_i | u_o |
| --- | --- | --- |
| 0 | O | O |
| ~1.5 | Peak | Peak |
| ~3.5 | Trough | Trough |
| ~6.5 | Peak | Peak |
| ~8.5 | O | O |
</details>

(c)

图 3.3.27 互补输出级的基本电路及其交越失真

(a) 电路 (b)  $T_{1}$  管的理想输入特性 (c) 交越失真

设晶体管有理想输入特性，见图(b)中实线所示。静态时，输入电压为零（即将输入端接地），输出电压为零（即输出端电位为零）。设输入电压 $\dot{U}_{\mathrm{i}}$ 为正弦波，当 $u_{\mathrm{i}} > 0$ 时，$\mathrm{T}_{1}$ 管导通，$\mathrm{T}_{2}$ 管截止，$\mathrm{T}_{1}$ 管以射极输出形式将正半周信号传递到负载，$u_{\mathrm{o}} = u_{\mathrm{i}}$ 。此时正电源 $+V_{\mathrm{CC}}$ 供电，电流通路如图3.3.27(a)中实线所标注。与此相反，当 $u_{\mathrm{i}} < 0$ 时，$\mathrm{T}_{1}$ 管截止，$\mathrm{T}_{2}$ 管导通，$\mathrm{T}_{2}$ 管以射极输出形式将负半周信号传递到负载，$u_{\mathrm{o}} = u_{\mathrm{i}}$ 。此时负电源 $-V_{\mathrm{CC}}$ 供电，电流通路如图3.3.27(a)中虚线所标注。这样，$\mathrm{T}_{1}$ 管与 $\mathrm{T}_{2}$ 管以互补的方式交替工作，正、负电源交替供电，电路实现了双向跟随。在输入电压幅值足够大时，输出电压的最大幅值可达 $\pm (V_{\mathrm{CC}} - |U_{\mathrm{CES}}|)$，$U_{\mathrm{CES}}$ 为饱和管压降。

如果考虑晶体管的实际输入特性如图(b)中虚线所示,则不难发现,当输入电压小于b-e间开启电压 $U_{on}$ 时, $T_{1}$ 管与 $T_{2}$ 管均处于截止状态。也就是说,只有当 $|u_{i}|>U_{on}$ 时,输出电压才跟随 $u_{i}$ 变化。因此,当输入电压为正弦波时,在 $u_{i}$ 过零附近输出电压将产生失真,波形如图(c)所示,这种失真称为交越失真。

与一般放大电路相同,消除失真的方法是设置合适的静态工作点。可以设想,若在静态时 $T_{1}$ 管与 $T_{2}$ 管均处于临界导通或微导通(即有一个微小的静态电流)状态,则当输入信号作用时,就能保证至少有一只管子导通,实现双向跟随。

## 二、消除交越失真的互补输出级

在图 3.3.28(a) 所示电路中, 静态时, 从正电源  $+V_{CC}$  经  $R_{1}$ 、 $D_{1}$ 、 $D_{2}$ 、 $R_{2}$  到负电源  $-V_{CC}$  形成一个直流电流, 必然使  $T_{1}$  和  $T_{2}$  的两个基极之间产生电压

$$
U _ {\mathrm{B1B2}} = U _ {\mathrm{D1}} + U _ {\mathrm{D2}}
$$

如果晶体管与二极管采用同一种材料，如都为硅管，就可以通过调整 $R_{1}$ 、 $R_{2}$ 的阻值来改变二极管管压降，使 $T_{1}$ 和 $T_{2}$ 均处于微导通状态。由于二极管的动态电阻很小，可以认为 $T_{1}$ 管基极动态电位与 $T_{2}$ 管基极动态电位近似相等，且均约为 $u_{i}$，即 $u_{b1}\approx u_{b2}\approx u_{i}$ 。

为消除交越失真，在集成电路中常采用图3.3.28(b)所示电路。若 $I_{2}\gg I_{B}$ ，则

$$
U _ {\mathrm{B1B2}} = U _ {\mathrm{CE}} \approx \frac {R _ {3} + R _ {4}}{R _ {4}} \cdot U _ {\mathrm{BE}} = \left(1 + \frac {R _ {3}}{R _ {4}}\right) U _ {\mathrm{BE}} \tag {3.3.41}
$$

合理选择  $R_{3}$  和  $R_{4}$ ，可以得到  $U_{BE}$  任意倍数的直流电压，故称为  $U_{BE}$  倍增电路。同时也可得到 PN 结任意倍数的温度系数，从而得到温度补偿。

![](images/page_175_image_2.jpg)

<details>
<summary>text_image</summary>

R1
D1
u_i
D2
R2
b1
T1
b2
T2
+Vcc
+
RL
uo
-
-Vcc
</details>

(a)

![](images/page_175_image_4.jpg)

<details>
<summary>text_image</summary>

I
R₃ I₁
R₄ I₂ I_B T
b₁
b₂
</details>

(b)

图 3.3.28 消交越失真的互补输出级

(a) 用二极管电路 (b) 用  $U_{BE}$  倍增电路

为了增大  $T_{1}$  管和  $T_{2}$  管的电流放大系数，以减小前级驱动电流，常采用复合管结构。而要寻找特性完全对称的 NPN 型和 PNP 型管是比较困难的，所以，在实用电路中常采用图 3.3.29 所示电路。图中  $T_{1}$  管和  $T_{2}$  管复合成 NPN 型管， $T_{3}$  管和  $T_{4}$  管复合成 PNP 型管。从输出端看进去， $T_{2}$  管和  $T_{4}$  管均采用了同类型管，较容易做到特性相同。这种输出管为同一类型管的电路称为准互补电路。

![](images/page_175_image_9.jpg)

<details>
<summary>text_image</summary>

R1
R3
ui
R4
R2
T5
T1
T2
T3
T4
RL
uo
-
+VCC
-VCC
</details>

图 3.3.29 采用复合的互补输出级

本节所介绍的互补输出级(简称互补电路)常作为功率放大电路,也称为 OCL $^{①}$  电路。有关输出功率及效率等问题见第 8 章。

## 三、CMOS互补输出级

与晶体管构成的互补输出级相类似，利用MOS管也可构成互补电路，称为CMOS电路。CMOS互补输出级由具有对称特性的增强型NMOS管和PMOS管组成，它们的两个栅极相连作为输入端，两个源极相连作为输出端，两个漏极分别接正、负电源，如图3.3.30(a)所示。与晶体管构成的互补输出级工作原理相同，设输入信号 $u_{1}$ 为正弦波电压；则正半周时 $T_{1}$ 导通、 $T_{2}$ 截止，$+V_{DD}$ 供电,构成源极输出电路,输出跟随输入变化;负半周时 $T_{1}$ 截止、 $T_{2}$ 导通, $-V_{DD}$ 供电,仍构成源极输出电路,输出仍跟随输入变化。

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① OCL 为英文 Output Capacitorless 的缩写。</span></small>

![](images/page_176_image_3.jpg)

<details>
<summary>text_image</summary>

+VDD
T1
ui
T2
RL u0
-VDD
</details>

(a)

![](images/page_176_image_5.jpg)

<details>
<summary>text_image</summary>

I
R1
ui
R2
R3
+VDD
T1
T2
-VDD
+
RL uo
-
</details>

(b)

图 3.3.30 CMOS 互补输出级

(a) 基本电路 (b) 消除交越失真的电路

由于 MOS 管的开启电压要大于晶体管的开启电压, 可达几伏, 因而消除交越失真显得尤为重要, 图(b) 所示为一种消除交越失真的 CMOS 输出级。图中电流源 I 既为前级提供静态电流, 又作为前级电路的有源负载, I 在  $R_{1}$  和  $R_{2}$  上的压降等于  $T_{1}$  管和  $T_{2}$  管栅极间的静态电压, 应使两只管子处于临界导通或微导通状态, 从而能够消除交越失真。

## 思考题

3.3.1 已知图 3.3.3 所示电路中  $R_{c1} = 1.01 R_{c2}$ ，其余参数理想对称。试问:与全部参数理想对称情况相比，电路的静态和动态参数有哪些不同？
3.3.2 在图 3.3.7 所示电路中, 若从  $T_{2}$  集电极单端输出, 则对电路的静态和动态有什么影响?
3.3.3 在图 3.3.18 所示微电流源电路中，电阻  $R_{e}$  是否具有稳定输出电流  $I_{C1}$  的作用？简述理由。
3.3.4 共射放大电路采用有源负载后输出电阻是增大了还是减小了？输出电流是增大了还是减小了？为什么？
3.3.5 在图 3.3.30(b) 电路中, 可以认为  $T_{1}$  和  $T_{2}$  动态电位相等吗? 为什么?

## 3.4 集成运放电路简介

从本质上看,集成运放是一种高性能的直接耦合放大电路。尽管品种繁多,内部电路结构也不尽相同,但是它们的基本组成部分、结构形式和组成原则基本一致。本章首先从集成运放电路的原理电路谈起,然后对典型电路进行分析。分析集成运放电路的目的,一是从中更加深入地理解集成运放的性能特点,二是了解复杂电路的分析方法。

## 3.4.1 双极型集成运放电路

在分析集成运放电路时,首先应将电路“化整为零”,分为偏置电路、输入级、中间级和输出级四个部分；进而“分析功能”，弄清每部分电路的结构形式和性能特点；最后“统观整体”，研究各部分相互间的联系，从而理解电路如何实现所具有的功能；必要时再进行“定量估算”。

## 一、原理电路

双极型集成运放的原理电路如图 3.4.1(a) 所示, 首先将偏置电路分离出来, 然后再对放大电路进行分析。

## 1. 对偏置电路的分析

在集成运放电路中,若有一个支路的电流可以直接估算出来,通常该电流就是偏置电路的基准电流。观察图3.4.1(a)所示电路,电阻 $R_{4}$ 中的电流

$$
I _ {R _ {4}} = \frac {2 V _ {\mathrm{CC}} - U _ {\mathrm{EB10}}}{R _ {4}}
$$

为电流源的基准电流。 $T_{12}$ 与 $T_{10}$ 构成镜像电流源， $T_{11}$ 、 $R_{5}$ 与 $T_{10}$ 构成微电流源，故 $T_{10}$ 、 $T_{11}$ 、 $T_{12}$ 和 $R_{4}$ 、 $R_{5}$ 构成多路电流源； $T_{11}$ 的集电极电流为输入级提供静态电流， $T_{12}$ 的集电极电流为中间级和输出级提供静态电流。用电流源符号取代两路电流源电路，则得图(b)所示简化后的放大电路部分，两个输入端的差值 $(u_{11}-u_{12})$ 为输入电压。

![](images/page_177_image_9.jpg)

<details>
<summary>text_image</summary>

R5
T11
T10
T12
+VCC
u11○
T1
T2
u12
IR
R4
R2
T5
T6
T7
+
RL
uO
-
R3
T3
T4
T8
T9
-VCC
</details>

(a)

![](images/page_177_image_11.jpg)

<details>
<summary>text_image</summary>

I1
+ VCC
T1 T2
u11 - u12
R1 -
T3 T4
I2
R2
T5
R3
T6 T7
+
T8
T9
RL uO
- VCC
</details>

(b)

图 3.4.1 双极型集成运放的原理电路

(a) 原理电路 (b) 放大电路部分

## 2. 对原理电路的定性分析

观察图(b)电路，按输入信号 $(u_{11} - u_{12})$ 传递的顺序可以看出，所示为三级大电路。与图3.2.1所示集成运放电路方框图对照，第一级是以 $\mathrm{T}_{1}$ 管和 $\mathrm{T}_{2}$ 管为放大管、双端输入、单端输出的差分放大电路，以减小整个电路的温漂，增大共模抑制比。第二级是以 $\mathrm{T}_{3}$ 和 $\mathrm{T}_{4}$ 管组成的复合管为放大管、以恒流源作有源负载的共射放大电路，可获得很高的电压放大倍数。第三级是准互补电路，带负载能力强，且最大不失真输出电压幅值接近电源电压； $R_{2}, R_{3}$ 和 $\mathrm{T}_{5}$ 组成 $U_{\mathrm{BE}}$ 倍增电路，用来消除交越失真。电路还采用NPN和PNP型混合使用的方法，以保证各级均有合适的静态工作点，且输入电压为零时输出电压为零。

当输入的差模信号极性 $u_{11}$ 为正、 $u_{12}$ 为负时， $T_{1}$ 管集电极动态电位的极性为负，即 $T_{3}$ 管的基极动态电位为负，因而 $T_{3}$ 和 $T_{4}$ 管集电极动态电位为正（共射电路输出电压与输入电压反相），所以输出电压为正（OCL电路是电压跟随电路）。因此， $u_{11}$ 与 $u_{0}$ 极性相同， $u_{12}$ 与 $u_{0}$ 极性相反。可见， $u_{11}$ 为同相输入端， $u_{12}$ 为反相输入端。

## 3. 对原理电路的定量估算

为了分析动态参数,首先应画出图3.4.1(b)所示电路的交流等效电路,如图3.4.2所示。因为 $T_{3}$ 和 $T_{4}$ 管的集电极所接恒流源的动态电阻无穷大,所以 $T_{3}$ 和 $T_{4}$ 管的动态电流全部流向输出级;且 $T_{5}$ 管的集电极和发射极之间无动态压降,即可视为短路。因为在输入信号极性不同时,输出级的 $T_{6}$ 和 $T_{7}$ 、 $T_{8}$ 和 $T_{9}$ 中只有一对管子工作,所以交流等效电路中可只画一半电路。

![](images/page_178_image_7.jpg)

<details>
<summary>text_image</summary>

+
İb1
rbe1
β1İb1
R1
İb3
rbe3
β3İb3
rbe4
β4İb4
rbe6
İb6
β6İb6
β7İb7
RL
Üo
-
Input级
中间级
输出级
İe7
İb7
İb2
β2İb2
rbe2
-
</details>

图3.4.2 图3.4.1所示电路的交流等效电路

交流等效电路中各支路的电流方向是以输入信号方向为依据逐级确定的。设电路中所有晶体管的电流放大系数均为  $\beta$ ，以下逐级分析电流关系。

若电阻 $R_{1}$ 远远大于第二级放大电路的输入电阻，则 $\mathrm{T}_{3}$ 管的基极电流 $\dot{I}_{\mathrm{b3}} \approx \dot{I}_{\mathrm{c1}} = \beta \dot{I}_{\mathrm{b1}}$，而且根据图中电流关系可得

$$
\dot {I} _ {\mathrm{b4}} \approx \dot {I} _ {\mathrm{c3}} = \beta \dot {I} _ {\mathrm{b3}} = \beta^ {2} \dot {I} _ {\mathrm{b1}}
$$

$$
\dot {I} _ {\mathrm{b6}} \approx \dot {I} _ {\mathrm{c4}} = \beta \dot {I} _ {\mathrm{b4}} = \beta^ {3} \dot {I} _ {\mathrm{b1}}
$$

$$
\dot {I} _ {\mathrm{b} 7} \approx \dot {I} _ {\mathrm{c} 6} = \beta \dot {I} _ {\mathrm{b} 6} = \beta^ {4} \dot {I} _ {\mathrm{b} 1}
$$

$T_{7}$ 管的发射极电流全部流入负载,负载电阻上的电流

$$
\dot {I} _ {\mathrm{L}} = \dot {I} _ {\mathrm{e7}} \approx \dot {I} _ {\mathrm{e7}} = \beta \dot {I} _ {\mathrm{b7}} \approx \beta^ {5} \dot {I} _ {\mathrm{b1}}
$$

因此，图 3.4.1 所示电路的电压放大倍数

$$
\dot {A} _ {u} = \frac {\Delta u _ {0}}{\Delta (u _ {1 1} - u _ {1 2})} = \frac {\dot {I} _ {\mathrm{L}} R _ {\mathrm{L}}}{\dot {I} _ {\mathrm{bl}} \cdot 2 r _ {\mathrm{bel}}} \approx \frac {\beta^ {5} R _ {\mathrm{L}}}{2 r _ {\mathrm{bel}}}
$$

上式表明要使电压放大倍数达到几十万甚至上百万倍不是太困难的事。同时说明，双极型管放大电路高电压放大倍数是依靠晶体管的电流放大作用的积累来实现的。

输入电阻

$$
R _ {\mathrm{i}} = r _ {\mathrm{bel}} + r _ {\mathrm{be2}} = 2 r _ {\mathrm{bel}}
$$

因为差分放大电路的集电极静态电流很小,为几十微安甚至更小,所以输入电阻很大。

## 二、F007 电路分析

在集成运放电路中,若有一个支路的电流可以直接估算出来,通常该电流就是偏置电路的基准电流,电路中与之相关联的电流源(如镜像电流源、比例电流源等)部分,就是偏置电路。将偏置电路分离出来,剩下部分一般为三级放大电路,按信号的流通方向,以“输入”和“输出”为线索,既可将三级分开,又可得出每一级属于哪种基本放大电路。

F007 是通用型集成运放，其电路如图 3.4.3 所示，它由 ±15 V 两路电源供电。从图中可以看出，从 +V$_{CC}$ 经 T$_{12}$、R$_{5}$ 和 T$_{11}$ 到 -V$_{CC}$ 所构成的回路的电流能够直接估算出来，因而 R$_{5}$ 中的电流为偏置电路的基准电流。T$_{10}$ 与 T$_{11}$ 构成微电流源，而且 T$_{10}$ 的集电极电流 I$_{C10}$ 等于 T$_{9}$ 管集电极电流 I$_{C9}$ 与 T$_{3}$、T$_{4}$ 的基极电流 I$_{B3}$、I$_{B4}$ 之和，即 I$_{C10}$ = I$_{C9}$ + I$_{B3}$ + I$_{B4}$；T$_{8}$ 与 T$_{9}$ 为镜像关系，为第一级提供静态电流；T$_{13}$ 与 T$_{12}$ 为镜像关系，为第二、三级提供静态电流。F007 的偏置电路如图中所标注，其分析估算见例 3.3.2。将偏置电路分离出来后，可得到 F007 的放大电路部分，如图 3.4.4 所示。根据信号的流通方向可将其分为三级，下面就各级作具体分析。

![](images/page_179_image_12.jpg)

<details>
<summary>text_image</summary>

T8
T9
T12
T13
+VCC
T14
R9
25 Ω
uO
T1
T2
T3
T4
T7
R5
39 kΩ
C
30pF
R7
4.5 kΩ
T15
R8
7.5 kΩ
D1
R10
50 Ω
D2
T16
T17
T18
T19
-Rw
R1
1 kΩ
R2
50 kΩ
R3
1 kΩ
外接调零电位器
输入级
偏置电路
中间级
输出级
-R4
3 kΩ
-VCC
</details>

图 3.4.3 F007 电路原理图

![](images/page_180_image_2.jpg)

<details>
<summary>text_image</summary>

T8
T9
+VCC
T1
T2
T4
iC13
iC9
R7
T14
R9
uO
T3
iC3
iB3+iB4
T7
iC4
iB16
R8
D1
T15
R10
T5
iC5
iC6
T6
IC10
T16
T17
D2
T18
T19
恒流源负载
共射电路
R1
R2
R3
- VCC
共集-共基差分
放大电路
准互补
输出级
</details>

图 3.4.4 F007 电路中的放大电路部分

## 1. 输入级

输入信号 $u_{1}$ 加在 $T_{1}$ 和 $T_{2}$ 管的基极，而从 $T_{4}$ 管（即 $T_{6}$ 管）的集电极输出信号，故输入级是双端输入、单端输出的差分放大电路，完成了整个电路对地输出的转换。 $T_{1}$ 与 $T_{2}$ 、 $T_{3}$ 与 $T_{4}$ 管两、两特性对称，构成共集-共基电路，从而提高电路的输入电阻，改善频率响应。 $T_{1}$ 与 $T_{2}$ 管为纵向管， $\beta$ 大； $T_{3}$ 与 $T_{4}$ 管为横向管， $\beta$ 小但耐压高； $T_{5}$ 、 $T_{6}$ 与 $T_{7}$ 管构成的电流源电路作为差分放大电路的有源负载；因此输入级可承受较高的差模输入电压并具有较强的放大能力。

$\mathrm{T}_{5}, \mathrm{T}_{6}$ 与 $\mathrm{T}_{7}$ 构成的电流源电路不但作为有源负载，而且将 $\mathrm{T}_{3}$ 管集电极动态电流转换为输出电流 $\Delta i_{\mathrm{B16}}$ 的一部分。由于电路的对称性，当有差模信号输入时，$\Delta i_{\mathrm{C3}} = -\Delta i_{\mathrm{C4}}, \Delta i_{\mathrm{C5}} \approx \Delta i_{\mathrm{C3}}$（忽略 $\mathrm{T}_{7}$ 管的基极电流），$\Delta i_{\mathrm{C5}} = \Delta i_{\mathrm{C6}}$（因为 $R_{1} = R_{3}$），因而 $\Delta i_{\mathrm{C6}} \approx -\Delta i_{\mathrm{C4}}$，所以 $\Delta i_{\mathrm{B16}} = \Delta i_{\mathrm{C4}} - \Delta i_{\mathrm{C6}} \approx 2\Delta i_{\mathrm{C4}}$ 输出电流加倍，当然会使电压放大倍数增大。电流源电路还对共模信号起抑制作用，当共模信号输入时，$\Delta i_{\mathrm{C3}} = \Delta i_{\mathrm{C4}}$，而 $\Delta i_{\mathrm{C6}} = \Delta i_{\mathrm{C5}} \approx \Delta i_{\mathrm{C3}}$（忽略 $\mathrm{T}_{7}$ 管的基极电流），$\Delta i_{\mathrm{B16}} = \Delta i_{\mathrm{C4}} - \Delta i_{\mathrm{C6}} \approx 0$，可见，共模信号基本不传递到下一级，提高了整个电路的共模抑制比。

此外，当某种原因使输入级静态电流增大时，$\mathrm{T_8}$ 与 $\mathrm{T_9}$ 管集电极电流会相应增大，但因为 $I_{\mathrm{C10}} = I_{\mathrm{C9}} + I_{\mathrm{B3}} + I_{\mathrm{B4}}$ ，且 $I_{\mathrm{C10}}$ 基本恒定，所以 $I_{\mathrm{C9}}$ 的增大势必使 $I_{\mathrm{B3}}$ 、 $I_{\mathrm{B4}}$ 减小，从而使输入级静态电流$I_{\mathrm{C1}}$ 、 $I_{\mathrm{C2}}$ 、 $I_{\mathrm{C3}}$ 、 $I_{\mathrm{C4}}$ 减小，保持它们基本不变。当某种原因使输入级静态电流减小时，各电流的变化与上述过程相反。

综上所述,输入级是一个输入电阻大、输入端耐压高、对共模信号抑制能力强、有较大差模放大倍数的双端输入、单端输出差分放大电路。

## 2. 中间级

中间级是以  $T_{16}$  和  $T_{17}$  组成的复合管为放大管，以电流源为集电极负载的共射放大电路，具有很强的放大能力。

## 3. 输出级

输出级是准互补电路， $T_{18}$  和  $T_{19}$  复合而成的 PNP 型管与 NPN 型管  $T_{14}$  构成互补形式，为了弥补它们的非对称性，在发射极加了两个阻值不同的电阻 $R_{9}$ 和 $R_{10}$ 。$R_{7}, R_{8}$ 和 $\mathrm{T}_{15}$ 构成 $U_{\mathrm{BE}}$ 倍增电路，为输出级设置合适的静态工作点，以消除交越失真。$R_{9}$ 和 $R_{10}$ 还作为输出电流 $i_{0}$ （发射极电流）的采样电阻与 $\mathrm{D}_1, \mathrm{D}_2$ 共同构成过流保护电路，这是因为 $\mathrm{T}_{14}$ 导通时 $R_{7}$ 上电压与二极管 $\mathrm{D}_1$ 上电压之和等于 $\mathrm{T}_{14}$ 管b-e间电压与 $R_{9}$ 上电压之和，即

$$
u _ {R _ {7}} + u _ {\mathrm{D1}} = u _ {\mathrm{BE14}} + i _ {\mathrm{O}} R _ {9}
$$

当 $i_0$ 未超过额定值时，$u_{\mathrm{D1}} < U_{\mathrm{ON}}$，$\mathrm{D}_1$ 截止；而当 $i_0$ 过大时，$R_9$ 上电压变大使 $\mathrm{D}_1$ 导通，为 $\mathrm{T}_{14}$ 的基极分流，从而限制了 $\mathrm{T}_{14}$ 的发射极电流，保护了 $\mathrm{T}_{14}$ 管。$\mathrm{D}_2$ 在 $\mathrm{T}_{18}$ 和 $\mathrm{T}_{19}$ 导通时起保护作用。

在图 3.4.3 中, 电容 C 的作用是相位补偿, 具体分析见第 5 章 5.6 节; 外接电位器  $R_{w}$  起调零作用, 改变其滑动端, 可改变  $T_{5}$  和  $T_{6}$  管的发射极电阻, 以调整输入级的对称程度。

读者可参阅本节对图 3.4.1 所示电路的定量分析自行分析 F007 电路的输入电阻、输出电阻和电压放大倍数。其电压放大倍数可达几十万倍，输入电阻可达 2 MΩ 以上。

## 3.4.2 单极型集成运放

在测量设备中，常需要高输入电阻的集成运放，其输入电流小到 $10\mathrm{pA}$ 以下，这对于任何双极型集成运放都无法实现，必须采用场效应管构成的集成运放。由于同时制作N沟道和P沟道互补对称管工艺较易实现，所以CMOS技术广泛用于集成运放。CMOS集成运放的输入电阻高达 $10^{10}\Omega$ 以上，并可在很宽的电源电压范围内工作。它们所需的芯片面积只是可比的双极型设计的 $1 / 5\sim 1 / 3$ ，因此CMOS电路的集成度更高。

C14573 是四个独立的运放制作在一个芯片上的器件，其电路原理图如图 3.4.5 所示，它全部由增强型 MOS 管构成，与晶体管集成运放电路结构相类比可知。 $T_{1}$ 、 $T_{2}$  和  $T_{7}$  管构成多路电流源，在已知  $T_{1}$  管的开启电压的前提下，利用外接电阻可以求出基准电压  $I_{R}$ ，一般选择  $I_{R}$  为  $20 \sim 200 \mu A$ 。根据  $T_{1}$ 、 $T_{2}$  和  $T_{7}$  管的结构尺寸可以得到  $T_{2}$  与  $T_{7}$  管的漏极电流，它们为放大电路提供静态电流。把偏置电路简化后，便可得到如图 3.4.6 所示的放大电路部分；由图可知，C14573 是两级放大电路。

![](images/page_181_image_10.jpg)

<details>
<summary>text_image</summary>

T₁
T₂
+VDD
u₁
-
T₃
T₄
C
T₈
uO
R
T₅
T₆
-VSS
</details>

图 3.4.5 C14573 电路图

第一级是以 P 沟道管  $T_{3}$  和  $T_{4}$  为放大管、以  $T_{5}$  和  $T_{6}$  管构成的电流源为有源负载、采用共源形式的双端输入、单端输出差分放大电路，有源负载使单端输出电路的动态输出电流近似等于双端输出电流的情况。由于第二级电路从  $T_{8}$  的栅极输入，其输入电阻非常大，所以使第一级具有很强的电压放大能力。

![](images/page_182_image_2.jpg)

<details>
<summary>text_image</summary>

+VDD
I1
+
u1
-
T3
T4
T5
T6
I2
uO
T8
-VSS
</details>

图 3.4.6 C14573 的放大电路部分

第二级是共源放大电路，以 N 沟道管  $T_{8}$  为放大管，漏极带有源负载，因此也具有很强的电压放大能力。但它的输出电阻很大，因而带负载能力较差，是为高阻抗负载而设计的，适用于以场效应管为负载的电路。

电容 C 起相位补偿作用。

在使用时，工作电源电压 $V_{\mathrm{DD}}$ 与 $V_{\mathrm{SS}}$ 之间的差值应满足 $5\mathrm{V}\leqslant (V_{\mathrm{DD}} - V_{\mathrm{SS}})\leqslant 15\mathrm{V}$ ；可以单电源供电（正、负均可）；也可以双电源供电，并允许正负电源不对称。使用者可根据对输出电压动态范围的要求选择电源电压的数值。

## 3.4.3 双极型与单极型混合结构集成运放

为了提高集成运放的性能,常采用晶体管和场效应管混合方式构成内部电路,包括Bi-MOS(晶体管-MOS管混合)、Bi-CMOS(晶体管-CMOS电路混合)、Bi-FET(晶体管-结型场效应管混合)等。本节介绍一种Bi-FET电路,第8章将介绍一种Bi-CMOS电路。

LF153 是双运放, 每个运放由输入级、中间级、输出级和偏置电路等四部分组成, 如图 3.4.7 (a) 所示。其中  $T_{12} \sim T_{16}$  与  $D_{Z}$ 、 $R_{11}$  组成偏置电路, 简化后如图 (b) 所示。图 (b) 中电流源  $I_{1}$ 、 $I_{2}$  分别为各级提供静态电流。

LF153 的输入级可与图 3.4.1 所示 F007 电路原理图相类比,除了用结型场效应管  $T_{1}$ 、 $T_{2}$  取代 F007 的晶体管  $T_{1} \sim T_{4}$  之外,其余部分几乎完全相同,工作原理不赘述。

LF153 的中间级由  $T_{6}$ 、 $T_{7}$  构成共集-共射形式，以增大电流放大能力；由电流源  $I_{2}$  作有源负载，以增大电压放大能力；是主放大器。

LF153 的输出级是由  $T_{10}$ 、 $T_{11}$  构成的互补输出级， $T_{8}$ 、 $T_{9}$ 、 $R_{5}$  所构成的电路用以消除交越失真。

电阻  $R_{10}$  在输出短路时可起到过流保护作用。

LF153 的部分性能指标与 F007 相当,但它的输入阻抗更高、输入偏置电流更小、功耗更低,且能够实现输出短路过流保护。此外,还有与之电路结构完全相同但用于不同环境温度的 LF253、LF353。

![](images/page_183_image_2.jpg)

<details>
<summary>text_image</summary>

+VCC
(+15 V)
T14
T15
T16
+
u1
-
T1
T2
C
D
T8
T9
R7
R10
+
uO
-
T6
T6
R5
R9
T11
T13
T12
R11
DZ
(-15 V)
-R1
R2
R3
R4
R6
T4
T7
R6
T3
</details>

(a)

![](images/page_183_image_4.jpg)

<details>
<summary>text_image</summary>

+VCC
(+15 V)
T1
T2
C
D
T5
T8
T9
R7
R10
+
uO
-
T10
T6
T11
R5
R9
T7
R4
R6
T3
T4
R1
R2
R3
R6
(-15 V)
-VCC
</details>

(b)

图 3.4.7 LF153 内部电路图

(a) 电路 (b) 简化电路

## 思考题

3.4.1 如何将偏置电路从集成运放电路中分离出来？
3.4.2 根据什么原则来判断集成运算放大电路中各级放大电路的基本接法和性能特点？
3.4.3 对于单电源供电的集成运放,为了使其输出电压在两个变化方向上的最大值相等,应如何设置静态工作点?画出信号源与集成运放直接耦合和阻容耦合两种方式的电路。
3.4.4 为什么采用双极型管和单极型管混合应用来构成集成运放？

## 3.5 集成运放的性能指标及低频等效电路

## 3.5.1 集成运放的主要性能指标

在考察集成运放的性能时,常用下列参数来描述:

## 一、开环差模增益 $A_{\mathrm{od}}$

在集成运放无外加反馈时的差模放大倍数称为开环差模增益，记作 $A_{\mathrm{od}} \circ A_{\mathrm{od}} = \Delta u_{\mathrm{O}} / \Delta (u_{\mathrm{P}} - u_{\mathrm{N}})$，常用分贝（dB）表示，其分贝数为 $20 \lg |A_{\mathrm{od}}|$。通用型集成运放的 $A_{\mathrm{od}}$ 通常在 $10^{5}$ 左右，即 $100 \mathrm{~dB}$ 左右。F007C 的 $A_{\mathrm{od}}$ 大于 $94 \mathrm{~dB}$。

## 二、共模抑制比 $K_{\mathrm{CMR}}$

共模抑制比等于差模放大倍数与共模放大倍数之比的绝对值，即 $K_{\mathrm{CMR}} = \left|A_{\mathrm{od}} / A_{\mathrm{oc}}\right|$，也常用分贝表示，其数值为 $20\lg K_{\mathrm{CMR}}$。

F007 的  $K_{CMR}$  大于 80 dB。由于  $A_{od}$  大于 94 dB，所以  $A_{oc}$  小于 14 dB。

## 三、差模输入电阻 $r_{\mathrm{id}}$

$r_{id}$ 是集成运放对输入差模信号的输入电阻。 $r_{id}$ 愈大，从信号源索取的电流愈小。F007C 的 $r_{id}$ 大于 2 MΩ。

## 四、输入失调电压 $U_{10}$ 及其温漂 $\mathrm{d}U_{10} / \mathrm{d}T$

由于集成运放的输入级电路参数不可能绝对对称，所以当输入电压为零时， $u_{0}$  并不为零。 $U_{10}$  是使输出电压为零时在输入端所加的补偿电压，若运放工作在线性区，则  $U_{10}$  的数值是  $u_{1}$  为零时输出电压折合到输入端的电压，即

$$
U _ {1 0} = - \frac {U _ {0} \Big | _ {u _ {1} = 0}}{A _ {\mathrm{od}}} \tag {3.5.1}
$$

$U_{10}$  愈小,表明电路参数对称性愈好。对于有外接调零电位器的运放,可以通过改变电位器滑动端的位置使得输入为零时输出为零。

$dU_{10}/dT$ 是 $U_{10}$ 的温度系数,是衡量运放温漂的重要参数,其值愈小,表明运放的温漂愈小。

F007C 的 $U_{10}$ 小于 2 mV, d$U_{10}$/dT 小于 20 μV/℃。因为 F007C 的开环差模增益为 94 dB，约 $5 \times 10^{4}$ 倍；根据式 (3.2.2) 可知，在输入失调电压 (2 mV) 作用下，集成运放已工作在非线性区；所以若不加调零措施，则输出电压不是 + $U_{OM}$，就是 - $U_{OM}$，而无法放大。

## 五、输入失调电流 $I_{10}$ 及其温漂 $\mathrm{d}I_{10} / \mathrm{d}T$

$$
I _ {\mathrm{IO}} = \left| I _ {\mathrm{B1}} - I _ {\mathrm{B2}} \right| \tag {3.5.2}
$$

$I_{10}$  反映输入级差放管输入电流的不对称程度。 $dI_{10}/dT$  与  $dU_{10}/dT$  的含义相类似，只不过研究的对象为  $I_{10}$ 。 $I_{10}$  和  $dI_{10}/dT$  愈小，运放的质量愈好。

## 六、输入偏置电流 $I_{\mathrm{IB}}$

$I_{1B}$ 是输入级差放管的基极(栅极)偏置电流的平均值,即

$$
I _ {\mathrm{IB}} = \frac {1}{2} (I _ {\mathrm{B1}} + I _ {\mathrm{B2}}) \tag {3.5.3}
$$

$I_{IB}$  愈小,信号源内阻对集成运放静态工作点的影响也就愈小。而通常  $I_{IB}$  愈小,往往  $I_{10}$  也愈小。

## 七、最大共模输入电压  $U_{Icmax}$

$U_{1cmax}$ 是输入级能正常放大差模信号情况下允许输入的最大共模信号,若共模输入电压高于此值,则运放不能对差模信号进行放大。因此,在实际应用时,要特别注意输入信号中共模信号的大小。

F007 的  $U_{lemax}$  高达 ±13 V。

## 八、最大差模输入电压  $U_{Idmax}$

当集成运放所加差模信号大到一定程度时，输入级至少有一个PN结承受反向电压， $U_{1dmax}$ 是不至于使PN结反向击穿所允许的最大差模输入电压。当输入电压大于此值时，输入级将损坏。运放中NPN型管的b-e间耐压值只有几伏，而横向PNP型管的b-e间耐压值可达几十伏。

F007C 中输入级采用了横向 PNP 型管, 因而  $U_{Idmax}$  可达 ±30 V。

## 九、-3 dB 带宽  $f_{H}$

$f_{H}$ 是使 $A_{od}$ 下降3 dB(即下降到约0.707倍)时的信号频率。由于集成运放中晶体管(或场效应管)数目多,因而极间电容就较多;又因为那么多元件制作在一小块硅片上,分布电容和寄生电容也较多;因此,当信号频率升高时,这些电容的容抗变小,使信号受到损失,导致 $A_{od}$ 数值下降且产生相移。

F007C 的  $f_{H}$  仅为 7 Hz。

应当指出,在实用电路中,因为引入负反馈,展宽了频带 $^{①}$ ,所以上限频率可达数百千赫以上。

## 十、单位增益带宽 $f_{c}$

$f_{c}$ 是使 $A_{od}$ 下降到零分贝（即 $A_{od}=1$，失去电压放大能力）时的信号频率，与晶体管的特征频率 $f_{T}$ 相类似。

## 十一、转换速率 $SR$

$SR^{②}$ 是在大信号作用下输出电压在单位时间变化量的最大值,即

$$
S R = \left| \frac {\mathrm{d} u _ {0}}{\mathrm{d} t} \right| _ {\max} \tag {3.5.4}
$$

SR 表示集成运放对信号变化速度的适应能力, 是衡量运放在大幅值信号作用时工作速度的参数, 常用每微秒输出电压变化多少伏来表示。当输入信号变化斜率的绝对值小于 SR 时, 输出电压才能按线性规律变化。信号幅值愈大、频率愈高, 要求集成运放的 SR 也就愈大。

在近似分析时，常把集成运放的参数理想化，即认为 $A_{\mathrm{od}}, K_{\mathrm{CMR}}, r_{\mathrm{id}}, f_{\mathrm{H}}$ 等参数值均为无穷大，而 $U_{10}$ 和 $\mathrm{d}U_{10} / \mathrm{d}T, I_{10}$ 和 $\mathrm{d}I_{10} / \mathrm{d}T, I_{1B}$ 等参数值均为零。

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 具体分析参阅第 5 章 5.4 节，上限频率与负反馈的深度有关。</span></small>

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">② SR 是英文 Slew Rate 的缩写,也称为“压摆率”。</span></small>

## 3.5.2 集成运放的低频等效电路

在分立元件放大电路的交流通路中，若用晶体管、场效应管的交流等效模型取代管子，则电路的分析与一般线性电路完全相同。同理，如果在集成运放应用电路中用运放的等效模型取代运放，那么电路的分析也将与线性电路完全相同。但是，如果在运放电路中将所有管子都用其等效模型取代去构造运放的模型，那么势必使等效电路非常复杂。例如F007电路中有19只晶体管，在计算机辅助分析中，若采用EM2模型，每只管子均由11个元件构成，则19只管子共有$11\times 19 = 209$ 个元件，可以想象电路的复杂程度。因此，人们常构造集成运放的宏模型，即在一定的精度范围内构造一个等效电路，使之与运放（或其它复杂电路）的输入端口和输出端口的特性相同或相似。分析的问题不同，所构造的宏模型也有所不同。

![](images/page_186_image_4.jpg)

图 3.5.1 集成运放低频等效电路

图3.5.1所示为集成运放的低频等效电路，对于输入回路，考虑了差模输入电阻 $r_{\mathrm{id}}$ 、偏置电流 $I_{\mathrm{IB}}$ 、失调电压 $U_{\mathrm{IO}}$ 和失调电流 $I_{\mathrm{IO}}$ 等四个参数；对于输出回路，考虑了差模输出电压 $u_{\mathrm{OD}}$，共模输出电压 $u_{\mathrm{OC}}$ 和输出电阻 $r_{\mathrm{o}}$ 等三个参数。显然，图示电路中没有考虑管子的结电容及分布电容、寄生电容等的影响，因此，只适用于输入信号频率不高情况下的电路分析。

如果仅研究对输入信号（即差模信号）的放大问题，而不考虑失调因素对电路的影响，那么可用简化的集成运放低频等效电路，如图3.5.2所示。这时，从运放输入端看进去，等效为一个电阻 $r_{id}$ ；从输出端看进去，等效为一个电压 $u_{1}$ （即 $u_{p}-u_{N}$ ）控制的电压源 $A_{od}u_{1}$ ，内阻为 $r_{o}$ 。若将集成运放理想化，则 $r_{id}=\infty, r_{o}=0$ 。

![](images/page_186_image_8.jpg)

<details>
<summary>text_image</summary>

+
u₁
-
rᵢₐ
- Aₒd u₁ +
rₒ
uₒ
</details>

图 3.5.2 简化的集成运放低频等效电路

## 思考题

3.5.1 对于实际的集成运放,当差模输入信号为零时其输出电压为零吗?为什么?
3.5.2 集成运放的主要参数中有哪些描述输入级的非对称性？它们与温度有关吗？为什么？

## 3.6 集成运放的种类及选择

## 3.6.1 集成运放的发展概况

集成运放自20世纪60年代问世以来，飞速发展，目前已经历了四代产品。

第一代产品虽然基本沿用了分立元件放大电路的设计思想，采用了集成数字电路的制造工艺，利用了少量横向PNP型管，构成以电流源作偏置电路的三级直接耦合放大电路；但是，它各方面性能都远远优于分立元件电路，满足了一般应用的要求。典型产品有 $\mu \mathrm{A}709$ ，国产的F003、5G23等。

第二代产品普遍采用了有源负载，简化了电路设计，并使开环增益有了明显的提高，各方面性能指标比较均衡，因此属于通用型运放，应用非常广泛。典型产品有 $\mu \mathrm{A}741$ 、LM324，国产的F007、F324、5G24等。

第三代产品的输入级采用了超 $\beta$ 管，$\beta$ 值高达1 000～5 000，而且版图设计上考虑了热效应的影响，从而减小了失调电压、失调电流及它们的温漂，增大了共模抑制比和输入电阻。典型产品有AD508、MC1556、国产的F1556、F030等。

第四代产品采用了斩波稳零和动态稳零技术，使各性能指标参数更加理想化，一般情况下不需调零就能正常工作，大大提高了精度。典型产品有 HA2900、SN62088，国产的 5G7650 等。

目前,除有不同增益的各种通用型运放外,还有品种繁多的专用型运放,以满足各种特殊要求。

## 3.6.2 集成运放的种类

从前面集成运放典型电路的分析可知，按供电方式可将运放分为双电源供电和单电源供电，在双电源供电中又分正、负电源对称型和不对称型供电。按集成度（即一个芯片上运放个数）可分为单运放、双运放和四运放，目前四运放日益增多。按内部结构和制造工艺可将运放分为双极型、CMOS型、Bi-JFET和Bi-MOS型。双极型运放一般输入偏置电流及器件功耗较大，但由于采用多种改进技术，所以种类多、功能强。CMOS型运放输入阻抗高、功耗小，可在低电源电压下工作，目前已有低失调电压、低噪声、高速度、强驱动能力的产品。Bi-JFET、Bi-MOS型运放采用双极型管与单极型管混合搭配的生产工艺，以场效应管作输入级，使输入电阻高达 $10^{12}\Omega$ 以上；Bi-MOS常以CMOS电路作输出级，可输出较大功率。目前具有各不相同电参数的产品种类繁多。

除以上几种分类方法外,还可从内部电路的工作原理、电路的可控性和电参数的特点等三个方面分类,下面简单加以介绍。

## 一、按工作原理分类

## 1. 电压放大型

实现电压放大，输出回路等效成由电压 $u_{\mathrm{I}}$ 控制的电压源 $u_{0} = A_{\mathrm{od}}u_{\mathrm{I}}$ 。F007、F324、C14573均属这类产品。

## 2. 电流放大型

实现电流放大，输出回路等效成由电流 $i_{1}$ 控制的电流源 $i_{0}=A_{i}i_{1}$ 。LM3900、F1900属于这类

产品。

## 3. 跨导放大型

将输入电压转换成输出电流，输出回路等效成由电压 $u_{1}$ 控制的电流源 $i_{0}$，即 $i_{0}=A_{in}u_{1}, A_{iu}$ 的量纲为电导，它是输出电流与输入电压之比，故称跨导，常记作 $g_{m}$ 。LM3080、F3080属于这类产品。

## 4. 互阻放大型

将输入电流转换成输出电压，输出回路等效成由电流 $i_{1}$ 控制的电压源 $u_{0}$，即 $u_{0}=A_{ui}i_{1}, A_{ui}$ 的量纲为电阻，故称这种电路为互阻放大电路。AD8009、AD8011属于这类产品。

输出等效为电压源的运放,输出电阻很小,通常为几十至上百欧;而输出等效为电流源的运放,输出电阻较大,通常为几千欧以上。

## 二、按可控性分类

## 1. 可变增益运放

可变增益运放有两类电路，一类由外接的控制电压 $u_{\mathrm{C}}$ 来调整开环差模增益 $A_{\mathrm{od}}$，称为电压控制增益的放大电路，如VCA610，当 $u_{\mathrm{C}}$ 从 $0\mathrm{V}$ 变为 $-2\mathrm{V}$ 时，$A_{\mathrm{od}}$ 从 $-40\mathrm{dB}$ 变为 $+40\mathrm{dB}$，中间连续可调；另一类是利用数字编码信号来控制开环差模增益 $A_{\mathrm{od}}$ 的，这类运放是模拟电路与数字电路的混合集成电路，具有较强的编程功能，例如AD526，其控制变量为 $A_{2}, A_{1}, A_{0}$，当给定不同的二进制码时，$A_{\mathrm{od}}$ 将随之改变。

## 2. 选通控制运放

此类运放的输入为多通道，输出为一个通道，即对“地”输出电压信号。利用输入逻辑信号的选通作用来确定电路对哪个通道的输入信号进行放大。图3.6.1所示为两通道选通控制运放OPA676的原理示意图。当 $\overline{CHA}$ 为 $0\mathrm{V}$ 时，开关S倒向电路 $\mathrm{A}_{1}$ 的输出端，电路对 $u_{\mathrm{IA}}$ 放大，输出电压 $u_{\mathrm{O}} = A_{\mathrm{od}}u_{\mathrm{IA}}$；当 $\overline{CHA}$ 为 $2.7\mathrm{V}$ 时，开关S倒向电路 $\mathrm{A}_2$ 的输出端，电路对 $u_{\mathrm{IB}}$ 放大，输出电压 $u_{\mathrm{O}} = A_{\mathrm{od}}u_{\mathrm{IB}}$；$A_{\mathrm{od}}$ 为开环差模增益。由于开关起切换输入通道的作用，故也称这类电路为输入切换运放。

![](images/page_188_image_13.jpg)

<details>
<summary>text_image</summary>

+ uIA
-
+
A1
-
S
A2
+
uIB
-
+
A3
uO
CHA
</details>

图 3.6.1 两通道选通控制运放 OPA676 的原理示意图

## 三、按性能指标分类

按性能指标可分为通用型和专用型两类。通用型运放用于无特殊要求的电路之中，其性能指标的数值范围见表3.6.1，少数运放可能超出表中数值范围；专用型运放为了适应各种特殊要求，某一方面性能特别突出，下面作一简单介绍。

表 3.6.1 通用型运放的性能指标

<table><tr><td>参数</td><td>单位</td><td>数值范围</td><td>参数</td><td>单位</td><td>数值范围</td></tr><tr><td> $A_{\text{od}}$ </td><td>dB</td><td>65~100</td><td> $K_{\text{CMR}}$ </td><td>dB</td><td>70~90</td></tr><tr><td> $r_{\text{id}}$ </td><td>MΩ</td><td>0.5~2</td><td rowspan="2">单位增益带宽</td><td rowspan="2">MHz</td><td rowspan="2">0.5~2</td></tr><tr><td> $U_{\text{IO}}$ </td><td>mV</td><td>2~5</td></tr><tr><td> $I_{\text{IO}}$ </td><td>μA</td><td>0.2~2</td><td>SR</td><td>V/μs</td><td>0.5~0.7</td></tr><tr><td> $I_{\text{IB}}$ </td><td>μA</td><td>0.3~7</td><td>功耗</td><td>mW</td><td>80~120</td></tr></table>

## 1. 高阻型

具有高输入电阻 $(r_{\mathrm{id}})$ 的运放称为高阻型运放。它们的输入级多采用超 $\beta$ 管或场效应管， $r_{id}$ 大于 $10^{9}\Omega$ ，适用于测量放大电路、信号发生电路或采样-保持电路。

国产的 F3130, 输入级采用 MOS 管。输入电阻大于  $10^{12} \Omega$ ,  $I_{IB}$  仅为 5 pA。

## 2. 高速型

单位增益带宽和转换速率高的运放为高速型运放。它的种类很多，增益带宽多在10 MHz左右，有的高达千兆赫；转换速率大多在几十伏/微秒至几百伏/微秒，有的高达几千伏/微秒。适用于模数转换器、数模转换器、锁相环电路和视频放大电路。

国产超高速运放 3554 的 SR 为 1 000 V/ $\mu$ s，单位增益带宽为 1.7 GHz。

## 3. 高精度型

高精度型运放具有低失调、低温漂、低噪声、高增益等特点，它的失调电压和失调电流比通用型运放小两个数量级，而开环差模增益和共模抑制比均大于100 dB。适用于对微弱信号的精密测量和运算，常用于高精度的仪器设备中。

国产的超低噪声高精度运放 F5037 的  $U_{10}$  为  $10 \mu V$ ，其温漂为  $0.2 \mu V/^{ \circ C}$ ;  $I_{10}$  为 7 nA；等效输入噪声电压密度约为  $3.5 nV/\sqrt{Hz}$ ，电流密度约为  $1.7 pA/\sqrt{Hz}$ ;  $A_{od}$  约为 105 dB。

## 4. 低功耗型

低功耗型运放具有静态功耗低、工作电源电压低等特点，它们的功耗只有几毫瓦，甚至更小，电源电压为几伏，而其它方面的性能不比通用型运放差。适用于能源有严格限制的情况，例如空间技术、军事科学及工业中的遥感遥测等领域。

微功耗高性能运放 TLC2252 的功耗约为  $180 \mu W$ ，工作电源为 5 V，开环差模增益为 100 dB，差模输入电阻为  $10^{12} \Omega$ 。可见，它集高阻与低功耗于一身。

此外,还有能够输出高电压(如100 V)的高压型运放,能够输出大功率(如几十瓦)的大功率型运放等。

除了通用型和专用型运放外，还有一类运放是为完成某种特定功能而生产的，例如仪表用放大器、隔离放大器、缓冲放大器、对数/反对数放大器等。随着EDA技术的发展，人们会越来越多地自己设计专用芯片。目前可编程模拟器件也在发展之中，人们可以在一块芯片上通过编程的方法实现对多路信号的各种处理，如放大、有源滤波、电压比较等。

## 3.6.3 集成运放的选择

通常情况下,在设计集成运放应用电路时,没有必要研究运放的内部电路,而是根据设计需求寻找具有相应性能指标的芯片。因此,了解运放的类型,理解运放主要性能指标的物理意义,是正确选择运放的前提。应根据以下几方面的要求选择运放。

## 一、信号源的性质

根据信号源是电压源还是电流源，内阻大小、输入信号的幅值及频率的变化范围等，选择运放的差模输入电阻 $r_{id}$ 、-3 dB带宽（或单位增益带宽）、转换速率SR等指标参数。

## 二、负载的性质

根据负载电阻的大小,确定所需运放的输出电压和输出电流的幅值。对于容性负载或感性负载,还要考虑它们对频率参数的影响。

## 三、精度要求

对模拟信号的处理,如放大、运算等,往往提出精度要求;如电压比较,往往提出响应时间、灵敏度要求。根据这些要求选择运放的开环差模增益 $A_{od}$ 、失调电压 $U_{10}$ 、失调电流 $I_{10}$ 及转换速率SR等指标参数。

## 四、环境条件

根据环境温度的变化范围,可正确选择运放的失调电压及失调电流的温漂  $dU_{10}/dT$ 、 $dI_{10}/dT$  等参数;根据所能提供的电源(如有些情况只能用干电池)选择运放的电源电压;根据对能耗有无限制,选择运放的功耗等。

根据上述分析就可以通过查阅手册等手段选择某一型号的运放了,必要时还可以通过各种EDA软件进行仿真,最终确定最满意的芯片。目前,各种专用运放和多方面性能俱佳的运放种类繁多,采用它们会大大提高电路的质量。

不过,从性能价格比方面考虑,应尽量采用通用型运放,只有在通用型运放不能满足应用要求时才采用专用型运放。

## 3.7 集成运放的使用

本节将对使用集成运放时必做的工作和运放的保护措施作简单的介绍。

## 3.7.1 使用时必做的工作

## 一、集成运放的外引线（管脚）

目前集成运放的常见封装方式有金属壳封装和双列直插式封装，外形如图3.7.1所示，以后者居多。双列直插式有8、10、12、14、16管脚等种类，虽然它们的外引线排列日趋标准化，但各制造厂仍略有区别。因此，使用运放前必须查阅有关手册，辨认管脚，以便正确连线。

## 二、参数测量

使用运放之前往往要用简易测试法判断其好坏,例如用万用表电阻的中间挡(“×100Ω”或“×1kΩ”挡,避免电流或电压过大)对照管脚测试有无短路和断路现象。必要时还可采用测试设备量测运放的主要参数。

![](images/page_191_image_2.jpg)

<details>
<summary>natural_image</summary>

Line drawing of a cylindrical electronic component with multiple pins (no text or symbols)
</details>

(a)

![](images/page_191_image_4.jpg)

<details>
<summary>natural_image</summary>

Technical line drawing of an integrated circuit chip with multiple pins (no text or symbols)
</details>

(b)

图 3.7.1 集成电路的外形

(a) 圆壳式外形 (b) 双列直插式外形

## 三、调零和设置偏置电压

由于失调电压及失调电流的存在,输入为零时输出往往不为零。对于内部无自动稳零措施的运放需外加调零电路,使之在零输入时输出为零。

对于单电源供电的运放，常需在输入端加直流偏置电压，设置合适的静态点，以便能放大正、负两个方向的变化信号。例如，为使正、负两个方向信号变化的幅值相同，应将 $Q$ 点设置在集成运放电压传输特性的中点，即 $V_{\mathrm{cc}} / 2$ 处，如图3.7.2(a)所示。图(b)和(c)分别为阻容耦

![](images/page_191_chart_11.jpg)

<details>
<summary>line</summary>

| uP - un | uO |
| --- | --- |
| 0 | 0 |
| 1/2Vcc | 0 |
| >1/2Vcc | 1/2Vcc |
| >1/2Vcc | 1 |
</details>

(a)

![](images/page_191_image_13.jpg)

<details>
<summary>text_image</summary>

u11○─C─R─R─uP＋A─o uO
u12○─C─R─R─uN─o uO
          │           │           │
          │           │           │
          │           │           │
          │           │           │
          │           │           │
          │           │           │
          │           │           │
          │           │           │
          │           │           │
          │           │           │
          │           │           │
          │           │           │
          │           │           │
          │           │           │
          │           │           │
         │           │           │
         │           │           │
         │           │           │
         │           │           │
         │           │           │
         │           │           │
         │           │           │
         │           │           │
         │           │           │
         │           │           │
         └───+VCC
</details>

(b)

![](images/page_191_image_15.jpg)

<details>
<summary>text_image</summary>

u11
R
R
uP
+
A
uO
uN
u12
R
</details>

(c)

图 3.7.2 单电源集成运放静态工作点的设置

(a) Q 点在电压传输特性上的位置 (b) 阻容耦合偏置电路 (c) 直接耦合偏置电路