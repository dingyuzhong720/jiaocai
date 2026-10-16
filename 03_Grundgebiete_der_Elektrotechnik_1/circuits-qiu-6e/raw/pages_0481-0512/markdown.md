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

为了确定这个电压波 $u^{+}$ 运动或传播的速度，假设 $\alpha = 0$ ，这时 $u^{+} = \sqrt{2} U_{0}^{+}\cos (\omega t - \beta x + \phi_{+})$ ，也就是说把 $u^{+}$ 看作是一个不衰减的正弦波。现在分析 $x = x_{1}$ 与 $x = x_{2}$ 两点上电压波动的情况。在 $x = x_{1}$ 处，$u^{+}(x_{1},t) = \sqrt{2} U_{0}^{+}\cos (\omega t - \beta x_{1} + \phi_{+})$ ，而在 $x = x_{2}$ 处，$u^{+}(x_{2},t) =$ $\sqrt{2} U_0^+ \cos (\omega t - \beta x_2 + \phi_+)$ 。若 $x_2 > x_1$ ，则该两点电压正弦变化的相位关系是 $u^+(x_2, t)$ 比 $u^+(x_1, t)$ 落后，落后的相位为 $(- \beta x_1 + \phi_)-(- \beta x_2 + \phi_)=\beta (x_2 - x_1)=\beta \Delta x$ 。因此，在 $x_1$ 处出现的正弦时间变化过程，要在一定的时间差后才会在距 $x_1$ 为 $\Delta x$ 的 $x_2$ 处重复出现。这一时间差为

$$
\Delta t = \frac {\beta (x _ {2} - x _ {1})}{\omega} = \frac {\beta \Delta x}{\omega}
$$

故相应的沿线从始端向终端传播速度为.

$$
v _ {\varphi} = \lim _ {\Delta t \to 0} \frac {\Delta x}{\Delta t} = \frac {\omega}{\beta} \tag {18-10}
$$

这就是整个电压波  $u^{+}$  的传播速度。由于这是同相点的运动速度，称为相位速度，简称相速，以  $v_{\varphi}$  表示。

![](images/page_483_chart_8.jpg)

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

后一式中， $c$ 为真空中的光速， $\varepsilon_{\mathrm{r}}$ 和 $\mu_{\mathrm{r}}$ 分别为导线周围媒质的相对介电常数和相对磁导率。对于架空线， $\varepsilon_{\mathrm{r}}\approx 1$ 和 $\mu_{\mathrm{r}}\approx 1$ ，即波的传播速度 $v_{\varphi}$ 实际上等于真空中的光速。对于电缆, 这一速度要小一些, 因为电缆中用的绝缘介质的相对介电常数 $\varepsilon_{\mathrm{r}} \approx 4 \sim 5$, 所以波的相速比真空中的光速低。在有损耗的线中 $(R_{0} \neq 0, G_{0} \neq 0)$, 相速总是比光速小。

![](images/page_486_chart_16.jpg)

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

根据式（18-17）和式（18-18）作出 $|Z_{c}|$ 和 $\theta$ 的频率特性如图18-8所示。从式(18-16)可以看出,当  $\omega=0$  时

![](images/page_487_chart_18.jpg)

图 18-8  $\left|Z_{c}\right|$  和  $\theta$  的频率特性

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

表明传输线上出现的电压、电流并非行波。由于  $\beta=\frac{2\pi}{\lambda}$ ，因此在  $x=0,\frac{\lambda}{2},\lambda,\frac{3\lambda}{2},\cdots$  处  $\beta x=0,\pi,2\pi,\cdots$ ，此时  $\cos(\beta x)=\pm1,\sin(\beta x)=0$ ，故这些地方的电压值始终是沿线电压分布中的极值（最大或最小），称之为电压的波腹；而这些地方的电流值始终是沿线电流分布中的零值，称之为电流的波节。在  $x=\frac{\lambda}{4},\frac{3\lambda}{4},\frac{5\lambda}{4},\cdots$  处， $\beta x=\frac{\pi}{2},\frac{3\pi}{2},\frac{5\pi}{2},\cdots$ ， $\cos(\beta x)=0,\sin(\beta x)=\pm1$ ，故这些地方是电流的波腹也是电压的波节。图 18-9 画出几个不同瞬间  $u_{x}$  和  $i_{x}$  沿线的分布曲线，它们对应于时间  $t=0,\frac{T}{4},\frac{T}{2},\frac{3T}{4}$  等时刻。从图中可看出电流、电压的波腹、波节的位置是固定不变的。这种波腹、波节位置固定不变的波称为驻波。

![](images/page_489_chart_12.jpg)

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

空载时,在距终端 x 处向终端看去的输入阻抗为

$$
Z _ {\mathrm{ix}} = \frac {\dot {U} _ {x}}{\dot {I} _ {x}} = - \mathrm{j} Z _ {\mathrm{c}} \cot (\beta x) = - \mathrm{j} Z _ {\mathrm{c}} \cot \left(\frac {2 \pi}{\lambda} x\right) = \mathrm{j} X _ {\mathrm{oc}} \tag {18-23}
$$

表明输入阻抗是一个纯电抗，以 $\frac{\lambda}{4}$ 为间隔变号；在电压波节（电流波腹）处，$Z_{ix} = 0$ ，相当于短路，也可理解为是一个串联谐振电路①；在电流波节（电压波腹）处，$Z_{ix} = \infty$ ，相当于开路，理解为是一个并联谐振电路。如图18-10所示。

![](images/page_490_image_6.jpg)

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

![](images/page_491_chart_3.jpg)

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

![](images/page_491_image_8.jpg)

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

$X_{L}$  为已知,则利用下列公式就可以分别决定所需开路无损耗线或短路无损耗线的长度 l:

$$
\begin{array}{l} X _ {c} = - \frac {1}{\omega C} = - Z _ {\mathrm{e}} \cot \left(\frac {2 \pi}{\lambda} l\right), \\ X _ {L} = \omega L = Z _ {\mathrm{c}} \tan \left(\frac {2 \pi}{\lambda} l\right) \\ \end{array}
$$

长度为 $\frac{\lambda}{4}$ 的无损耗线,还可以用来作为接在传输线和负载之间的匹配元件,它的作用如同一个阻抗变换器。下面介绍其工作原理。

设无损耗线的特性阻抗为 $Z_{\mathrm{el}}$ ，负载阻抗为 $Z_{2}$ ，且设 $Z_{2}$ 为纯电阻（即 $Z_{2} = R_{2}$ ），现在

要求设法使 $Z_{2}$ 和 $Z_{\mathrm{cl}}$ 匹配。为此目的，在传输线的终端与负载 $Z_{2}$ 之间插入一段 $l = \frac{\lambda}{4}$ 的无损耗线（见图18-13）。根据式(18-11)，可以求得这段长度为 $\frac{\lambda}{4}$ 的无损耗线的输入阻抗 $Z_{\mathrm{i}}$ 为（注意其终端负载为 $Z_{2}$）

![](images/page_492_image_7.jpg)

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

![](images/page_493_image_3.jpg)

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

![](images/page_494_image_19.jpg)

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

![](images/page_495_image_13.jpg)

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

$$
\frac {u ^ {+}}{i ^ {+}} = \frac {u ^ {-}}{i ^ {-}} = \sqrt {\frac {L _ {0}}{C _ {0}}} = Z _ {\mathrm{c}}
$$

$Z_{c}$  就是无损耗线的特性阻抗或波阻抗。因此， $u^{+}$ 和  $i^{+}$ 都是从始端向终端传播的入射波；而  $u^{-}$ 和  $i^{-}$ 都是向相反方向传播的反射波。这样，在任何瞬间，沿线的电压和电流都可以看作是入射波和反射波的叠加。

为了形象地阐明电压波或电流波沿线传播的过程，假定研究的无损耗线原来没有充电，且其终端在无限远处（半无限长线）。设在 $t = 0$ 时，将电压为 $U_{0}$ 的直流电压源接到该线的始端。由于反射波是在终端产生的，而现在终端在无限远处，因此在有限的时间内，传输线上不会出现反射波，所以只要研究入射波就可以了。这时，电压波将沿线由始端向终端行进，使传输线充电到 $U_{0}$ 。设在某一瞬间波前传播到 $\mathrm{m - n}$ 处（见图18-17），于是在 $\mathrm{m - n}$ 处的左边沿线各处线间电压为 $U_{0}$，同时来线（上方导线）带正电荷，回线（下方导线）带负电荷（显然，每单位长度所带电荷为 $q_{0} = C_{0}U_{0}$），而在 $\mathrm{m - n}$ 处的右边，由于电压波尚未到达，各处线间电压均为零，来、回线上也就没有电荷。

![](images/page_496_image_6.jpg)

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

![](images/page_497_chart_10.jpg)

<details>
<summary>line</summary>

| Time (t) | Value (u(0,t)) |
| --- | --- |
| \(0\) | \(U_{0}\) |
| \(t_{1}\) | \(U_{0}\) |
</details>

(a)

![](images/page_497_image_12.jpg)

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

![](images/page_497_chart_18.jpg)

<details>
<summary>line</summary>

| Time (t) | Response \((u_S(t)\epsilon(t))\) |
| --- | --- |
| 0 | u_S(0) |
| t_2 | 0 |
</details>

(a)

![](images/page_497_chart_20.jpg)

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

## §18-7 无损耗线的波过程

上节中讨论了不存在反射时无损耗线上的波过程。当传输线存在终端且不匹配的情况下，在终端将引起波的反射，因此，传输线上除了入射波以外还将存在反射波。本节讨论无损耗线在终端开路和短路两种情况下波的反射过程。

首先研究终端开路的无损耗线接通直流电压 $U_{0}$ 的波过程。在入射波未到达终端 $0 < t < \frac{l}{v}$ 的时间间隔内，反射尚未产生，因此线上的波过程和上节所述相同。在 $t = \frac{l}{v}$ 时波到达终端，由于终端开路，这一边界条件要求电流反射波大小为 $I_{0}$，因为只有电流的这种全反射才能使终端电流为零（$i = i^{+} - i^{-}$）。反射波所到之处电流变为零。由于 $u^{-} = Z_{\mathrm{e}}i^{-} = U_{0}$，而 $u^{+} = U_{0}$，因此，电压的反射波所到之处使线间电压成为 $2U_{0}$，如图18-20(a)(b)所示。这一过程发生在 $\frac{l}{v} \leqslant t < \frac{2l}{v}$ 之间。当反射波到达始端的前一瞬间时，全线电流为零，电压为 $2U_{0}$ 。当反射波到达始端时，由于始端的边界条件要求电压为 $U_{0}$，因此在始端也将产生反射，反射波（也即是第二次入射波）将为 $-U_{0}$ 以满足始端的边界条件，这也决定了第二次入射电流波为 $-I_{0}$。故 $\frac{2l}{v} \leqslant t < \frac{3l}{v}$ 的时间间隔内，波所到之处将使电压为 $U_{0}$ 而电流为 $-I_{0}$，如图18-20(c)所示。在 $t = \frac{3l}{v}$ 第二次入射波到达终端时，终端的边界条件要求第二次反射波为 $-I_{0}$，使 $i^{+} - i^{-} = 0$，第二次反射电压为 $-U_{0}$。故在 $\frac{3l}{v} \leqslant t < \frac{4l}{v}$ 时间间隔内，波所到之处将使线上电压和电流均为零，如图18-20(d)所示。当 $t = \frac{4l}{v}$ 时，第二次反射波到达始端，全线电压和电流均为零，完成接通过程的一次循环，即恢复到开始接通的状态。以后的过程将周期性地重复出现。此周期等于波行进4倍线长所需的时间，即 $T = \frac{4l}{v} = 4l\sqrt{L_{0}C_{0}}$。

![](images/page_498_image_6.jpg)

(d)

图 18-20 电压波和电流波在开路线上的多次入射和反射

终端短路的无损耗线与直流电压的接通过程与上述开路线相仿。当第一次入射波到达终端时将产生电压的全反射，第一次电压反射波为 $-U_{0}$ 而电流反射波为 $-I_{0}$，将使线上电流增加为 $2I_{0}$，从图18-21(a)(b)可以看出，经 $\frac{2l}{v}$ 时间，电压就完成一次周期重复而电流将增至 $2I_{0}$ 。之后每次由始端产生的入射波使沿线电压变为 $U_{0}$，从终端产生的反射波使电压为零，所以，电压在零和 $U_{0}$ 之间变动。对电流来说，在始端产生的入射波和终端产生的反射波，总是使得沿线电流增加一个 $I_{0}$ 。因此，线上电流最后将增加到无限大。

![](images/page_499_image_5.jpg)

图 18-21 电压波和电流波在短路线上的多次入射和反射

如果终端接以非匹配的电阻负载 $R_{\mathrm{L}}$，则视此电阻 $R_{\mathrm{L}}$ 与 $Z_{\mathrm{c}}$ 的大小关系将有不同的反射。如果 $R_{\mathrm{L}}>Z_{\mathrm{c}}$，则反射使电流减小、电压增加；如果 $R_{\mathrm{L}}<Z_{\mathrm{c}}$，则反射将使电流增加、电压减少。两种情况下，经过多次反射以后沿线电压与电流趋近恒定。如果终端的负载不是纯电阻而是电阻与电感或电容的组合，则由于终端将出现集总元件的过渡过程，反射的方式也将随时间而变。对这类问题不再深入讨论。

前面介绍的是无损耗线的时域分析。如果需要计及传输线的 $R_{0}$ 和 $G_{0}$，对有损耗线进行时域分析则要困难得多。

近年来由于超大规模集成电路的发展，并为提高数字电子计算机的运算速度，使用了更高的工作频率和变化更快的短脉冲，信号经过集成电路芯片之间的相互连接导线（简称互连）时，会产生延迟、畸变和交叉干扰等现象。对这种互连的时域分析需要用分布参数电路或传输线的观点处理。同时，这类传输线的损耗不能忽略，加上互连的数目很多，它们之间还有互感耦合，这些使得这类问题的分析变得更为复杂。

![](images/page_500_image_5.jpg)

## 思考题

18-1 均匀传输线各处电流不同的原因什么？均匀传输线各处电压不同的原因是什么？
18-2 均匀传输线上的电压和电流为什么遵循波动规律？
18-3 在均匀传输线上产生驻波的条件是什么？
18-4 对长度不等的导线,在什么条件下,采用均匀传输线模型?如采用集总参数模型,对信号有什么要求?
18-5 对于直流输电工程中的传输线,分析稳定运行应采用什么模型?而发生暂态过程时,应采用什么模型?
18-6 在集成电路中各器件之间连接的导线,应采用什么电路模型?

![](images/page_500_image_14.jpg)

## 习题

18-1 一对架空传输线的原参数是 $L_{0} = 2.89 \times 10^{-3} \mathrm{H / km}, C_{0} = 3.85 \times 10^{-9} \mathrm{F / km}, R_{0} = 0.3 \Omega / \mathrm{km}, G_{0} = 0$ 。试求当工作频率为 $50 \mathrm{~Hz}$ 时的特性阻抗 $Z_{\mathrm{c}}$ 、传播常数 $\gamma$ 、相位速度 $v_{\varphi}$ 和波长 $\lambda$ 。如果频率为 $10^{4} \mathrm{~Hz}$，重求上述各参数。
18-2 一同轴电缆的原参数为: $R_{0}=7\ \Omega/\mathrm{km}, L_{0}=0.3\ \mathrm{mH/km}, C_{0}=0.2\ \mu\mathrm{F/km}, G_{0}=0.5\times10^{-6}\ \mathrm{S/km}$。试计算当工作频率为 $800\ \mathrm{Hz}$ 时此电缆的特性阻抗 $Z_{c}$、传播常数 $\gamma$、相位速度 $v_{\varphi}$ 和波长 $\lambda$。
18-3 传输线的长度 $l = 70.8 \mathrm{~km}$, 其中 $R_{0} = 1 \Omega / \mathrm{km}, \omega C_{0} = 4 \times 10^{-4} \mathrm{~S} / \mathrm{km}$, 而 $G_{0} = 0$, $L_{0} = 0$。在线的终端所接阻抗 $Z_{2} = Z_{\mathrm{c}}$。终端的电压 $U_{2} = 3 \mathrm{~V}$。试求始端的电压 $U_{1}$ 和电流 $I_{1}$ 。

18-4 一高压输电线长 $300 \mathrm{~km}$, 线路原参数 $R_{0} = 0.06 \Omega / \mathrm{km}, L_{0} = 1.40 \times 10^{-3} \mathrm{H} / \mathrm{km}, G_{0} = 3.75 \times 10^{-8} \mathrm{~S} / \mathrm{km}, C_{0} = 9.0 \times 10^{-9} \mathrm{~F} / \mathrm{km}$ 。电源的频率为 $50 \mathrm{~Hz}$ 。终端为一电阻负载, 终端的电压为 $220 \mathrm{kV}$, 电流为 $455 \mathrm{~A}$ 。试求始端的电压 $\dot{U}_{1}$ 和电流 $\dot{I}_{1}$ 。

18-5 两段特性阻抗分别为 $Z_{\mathrm{c1}}$ 和 $Z_{\mathrm{c2}}$ 的无损耗线连接的传输线如题18-5图所示。已知终端所接负载为 $Z_{2} = (50 + \mathrm{j}50)\Omega$ 。设 $Z_{\mathrm{c1}} = 75\Omega, Z_{\mathrm{c2}} = 50\Omega$ 。两段线的长度都为 $0.2\lambda (\lambda$ 为线的工作波长)，试求 $1 - 1'$ 端的输入阻抗。

![](images/page_501_image_6.jpg)

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

![](images/page_501_image_14.jpg)

第十八章部分习题答案

其中  $Y_{c}=\frac{1}{Z_{c}}, Y_{2}=\frac{1}{Z_{2}}, Z_{2}$  为负载阻抗。

## 附录 A

## 磁路和铁心线圈

本附录介绍磁场、磁路和磁路定律，并对无分支磁路和有分支磁路的计算做简要介绍。另外还简要地介绍铁磁物质的磁化过程和铁心损耗以及磁饱和对电流和磁通波形的影响。最后介绍铁心线圈的电路模型和分析。

## §A-1 磁场和磁路

根据电磁场理论,磁场是由电流产生的,它与电流在空间的分布和周围空间磁介质的性质密切相关。在工程中,常把载流导体制成的线圈绕在由磁性材料制成的(闭合)铁心上。由于磁性材料的磁导率比周围空气的磁导率大很多,因此,铁心中的磁场比周围空气中的磁场强得多,磁场的磁感线大部分汇聚于铁心中,工程上把这种由磁性材料

组成的、能使磁感线集中通过的整体，称为磁路。磁路这种形式，可以用相对较小的电流，在其限定的区域内获得较强的磁场。在工程上，凡需要强磁场的场合，都广泛采用磁路实现，如各种型号的电机、变压器、继电器、电磁铁和电磁仪表等电气设备中，都有由磁性材料制成的磁路，图 A-1 是一种变压器的示意图。

![](images/page_502_image_6.jpg)

<details>
<summary>text_image</summary>

i₁
Φ
B H
Φσ
i₂
铁心
</details>

图 A-1 变压器的磁路

磁路在载流线圈的作用下(如图 A-1 中的电流  $i_{1}$  和  $i_{2}$ ), 在其内、外分布着电磁场, 因此, 磁路的分析计算实际上是电磁场的求解问题。描述磁场的两个基本物理量: 磁感应强度 B (向量), 磁场强度 H (向量) 以及它们的积分性质是分析计算磁路的基础。

磁感应强度用向量 B 表示, 是根据洛伦兹力定义的。在 SI 中, B 的单位是 T(特斯拉)。B 与电流的关系满足毕奥-沙伐定律。穿过某一截面 S 的磁感应强度 B 的通量称为磁通量, 简称磁通, 它定义为

$$
\varPhi = \int_ {S} \boldsymbol {B} \cdot \mathrm{d} S
$$

所以 B 在某截面 S 上的面积分就是通过该截面的磁通。磁通是一个标量，在 SI 中，它的单位是 Wb(韦伯)。磁通的参考方向与电流的方向满足右手螺旋定则。在磁场中，对 B 的任意闭合面积分为零，即有

$$
\oint_ {S} \boldsymbol {B} \cdot \mathrm{d} \boldsymbol {S} = 0 \tag {A-1}
$$

式中 dS 的方向规定为闭合面的外法线方向，同时又规定穿出闭合面的磁通为它的参考方向。所以在上式中穿进闭合面的磁通取“-”号，穿出闭合面的磁通取“+”号，两者的绝对值是相等的，这就是磁通连续性原理。

磁场强度用向量 H 表示, 在 SI 中它的单位是 A/m, 它是计及磁介质的作用后, 描述磁场的另一个物理量, 它与磁感应强度 B、磁介质的磁导率  $\mu$  之间有如下关系:

$$
B = \mu H
$$

由于磁性材料的  $\mu$  不是常量, 所以, 在磁路中上述关系为非线性关系。在磁场中, 对 H 的任意闭合路径(环路)的线积分, 等于穿过该闭合路径所界定面的电流的代数和, 即

$$
\oint_ {l} \boldsymbol {H} \cdot \mathrm{d} \boldsymbol {l} = \sum N i \tag {A-2}
$$

该积分称为安培环路定律。当电流的参考方向与环路的绕向符合右手螺旋定则时，该电流前取“+”号，反之，取“-”号。Ni又称为磁通势，可用 $F_{m}$ 表示，即 $F_{m}=Ni$ ，其单位为A，有时也用At(安匝)。

以上有关 B 和 H 的内容可参阅电磁场理论或物理学的有关部分。

现对图A-1所示磁路做进一步的说明。图中载流线圈的电流 $i_1$ 和 $i_2$ 共同产生的磁通分为两部分，其中只经铁心闭合的磁通 $\Phi$ 称为主磁通，另一部分是部分经铁心、部分经空气闭合的磁通 $\Phi_{\sigma}$，称为漏磁通①。要精确分析计算电流与这两部分磁通在空间分布的关系，是一个非线性磁场的求解问题。为简化磁路的分析，工程上根据实际情况假设如下的近似条件存在:

（1）由于铁心的磁性材料的磁导率  $\mu$  与空气的磁导率  $\mu_{0}$ （真空）之比约为  $10^{3} \sim 10^{4}$ ，在计算精度要求不高的情况下，可假设  $\Phi_{\sigma}=0$ （漏磁通）认为磁通全部集中在磁路内，即只考虑主磁通  $\Phi$  的计算。
(2) 磁路通常由同种类磁性材料或规则分段的不同种类的磁性材料组成, 可以根据磁通的走向, 按磁介质和截面都相同的原则分段计算。当每段磁路的截面较小时, 可以近似地认为磁场是均匀分布的, 即 B 和 H 在各磁路段内分别处处相等, 并假设它们的方向和磁通的方向相同, 均平行于磁路段的中心线, 如图 A-1 中所示。

在上述条件下,可按下述关系分段计算磁路:

① 第 $k$ 段磁路内的磁通

$$
\Phi_ {k} = \int_ {S _ {k}} \boldsymbol {B} _ {k} \cdot \mathrm{d} S _ {k} = B _ {k} S _ {k}, B _ {k} = \frac {\Phi_ {k}}{S _ {k}} \tag {A-3}
$$

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 主磁通与两个线圈交链，漏磁通只穿过一个线圈的一部分。</span></small>

② 沿第 k 磁路段的中心线, 有

$$
\int_ {l _ {k}} \mathbb {H} \cdot \mathrm{d} l = H _ {k} l _ {k} = u _ {\mathrm{m} k} \tag {A-4}
$$

上述积分是安培环路定律在一段路径上的积分结果,称为 k 磁路段的端磁位差(与电路中的端电压类似)。

③ $B_{k}$ 与 $H_{k}$ 之间的关系仍为

$$
B _ {k} = \mu_ {k} H _ {k}
$$

这一非线性关系,在工程上将用  $B=f(H)$  函数关系画出的曲线表示,称为 B-H 曲线或磁化曲线,计算时可查阅。

真空的磁导率  $\mu_{0}=4\pi\times10^{-7}\ H/m,\mu_{0}$  是一个常数。非铁磁物质的磁导率  $\mu$  与  $\mu_{0}$  相差无几，所以一般可以当作  $\mu_{0}$  计算。

## §A-2 铁磁物质的磁化曲线

工程上常用的铁磁材料主要是指铁、钴、镍及其合金,它们的磁化特性常用 B-H 曲线的形式表示,称为磁化曲线,通常是通过实验的方法获得的。

图A-2(a)(b)所示就是实验测得的磁化曲线，它表现为回线的形式，分别称为磁滞回线[图(a)所示]和磁滞回线簇[图(b)所示]。回线表明: $B$ 和 $H$ 之间是多值的函数关系，而且回线的形状与磁场强度的最大值 $H_{\mathrm{m}}$ 和磁化状态的历史有关。回线的走向与 $\Delta H$ 的符号有关，在回线任一点上 $\Delta H > 0$ （上升）和 $\Delta H < 0$ （下降）时的曲线不在同一条曲线上，当 $\Delta H > 0$ 时，曲线是沿着右侧的曲线上升[图A-2(a)所示]， $\Delta H < 0$ 时，曲线是沿着左侧所示曲线下降，图(a)所示的回线是在相同的 $H_{\mathrm{m}}$ 和 $-H_{\mathrm{m}}$ 下，连续地来回反复十多次获得的结果。如果在回线上的任一点上[如图A-2(a)中的a点]，小范围内来回反复变化一次或数次，可以生成一条小回线(称为局部回线)。图A-2(b)所示回线簇是在不同的最大值 $H_{\mathrm{m}}$ 下形成的磁滞回线。如果回线横向宽度较窄（回线所围成的面积较小），则铁磁材料称为软磁材料，电机、变压器等铁心是用软磁材料制成的。如果回线横向宽度较宽，则称为硬磁材料，工程上多用此材料制成永久磁铁。

![](images/page_504_image_13.jpg)

图 A-2 磁滞回线(簇)

计算软磁材料制成的磁路时,常采用一条基本磁化曲线近似替代磁滞回线,它是从B-H平面坐标的原点开始,到磁滞回线簇的顶点 $(H_{\mathrm{m}},B_{\mathrm{m}})$ 描成的一条曲线,如图A-2

(b)所示。工程上给出的磁化曲线都是基本磁化曲线，如图A-3所示。从曲线上可以看出，开始B随H增长较慢(Oa段)，然后迅速增长(ab段)，之后，增长速率减慢(bc段)，逐渐趋向于饱和(cd段)。c点称为曲线饱和点。图中还画出了磁导率 $\mu$ 随H的变化曲线。

磁化曲线还与温度有关,磁导率  $\mu$  一般随温度的升高而下降,高于某一温度时(居里点)可能完全失去磁性材料的磁性,使  $\mu=\mu_{0}$  (真空),如铁的居里点为  $760^{\circ}C$ 。

![](images/page_505_chart_7.jpg)

<details>
<summary>line</summary>

| Point | H | \(\mu\) |
| --- | --- | --- |
| a | ~0.1 | ~0.05 |
| b | ~0.3 | ~0.4 |
| c | ~0.6 | ~0.7 |
| d | ~0.9 | ~0.8 |
</details>

图A-3 基本磁化曲线

## §A-3 磁路的基本定律

由式(A-1)表示的磁感应强度 B 的闭合面积分在磁路中也处处适用, 当用于磁路中不同磁段的截面结合处时, 有

$$
\oint_ {S} \boldsymbol {B} \cdot \mathrm{d} S = \varPhi_ {1} + \varPhi_ {2} + \dots + \varPhi_ {k} + \dots = 0
$$

即有

$$
\sum \Phi = 0 \tag {A-5}
$$

积分式中的闭合面包括结合处所有磁段的截面。这是磁通连续性原理在磁路中的表示,式(A-5)称为磁路的基尔霍夫第一定律,可叙述为:穿过磁路中不同截面结合处的磁通的代数和等于零。式(A-5)也可表示为

$$
B _ {1} S _ {1} + B _ {2} S _ {2} + \dots + B _ {k} S _ {k} + \dots = 0
$$

$$
\sum B S = 0
$$

该定律形式上类似于电路中的 KCL。

在近似计算磁路时,取每一磁路段的中心线为计算长度的路径,当积分环路由磁路段的中心线组成时,应用式(A-2)表示的磁场强度闭合线积分有

$$
\oint_ {l} \boldsymbol {H} \cdot \mathrm{d} l = H _ {1} l _ {1} + H _ {2} l _ {2} + \dots + H _ {k} l _ {k} + \dots = \sum N i
$$

根据式(A-2), Ni 为磁通势  $F_{m}$ , 是磁路中的激励, 故

$$
\sum H l = \sum F _ {\mathrm{m}} \tag {A-6}
$$

式(A-6)称为磁路的基尔霍夫第二定律,可叙述为:磁路中由磁路段的中心线组成的环路上各磁路段的 Hl 的代数和等于中心线(环路)交链的磁通势的代数和。此定律形式上类似于电路中的 KVL。

计算磁路时有时用到磁阻的概念。每一磁路段的磁阻 $R_{mk}^{\prime}$ 是该磁路段的磁位差 $U_{mk}=H_{k}l_{k}$ 与该磁路段中的磁通 $\Phi_{k}$ 之比，即有

$$
R _ {m k} = \frac {H _ {k} l _ {k}}{\Phi_ {k}} = \frac {H _ {k} l _ {k}}{\mu_ {k} H _ {k} S _ {k}} = \frac {l _ {k}}{\mu_ {k} S _ {k}}
$$

磁阻类似于电路中的非线性电阻。上式表示的磁阻是静态磁阻，由于  $\mu_{k}$  与 B-H 曲线有关，不是常数，直接计算磁阻不很方便。

现以图A-4的有分支磁路为例说明磁路定律的应用。绕组1和2的匝数分别为$N_{1}$ 和 $N_{2}$，其中电流为 $i_1$ 和 $i_2$。先把磁路分段，并画出各段的中心线，即图A-4中的虚线。为简化起见，设ab、fa、ef三段的材料和截面积相同，截面积设为 $S_{1}$；bc、cd、de三段也作为一磁路段，截面积设为 $S_{2}$。根据磁通连续性原理，在ab、fa、ef三磁路段内的磁通是相等的，设为 $\Phi_{1}$。由于这三段的截面又相等，故三段的 $B$ 和 $H$ 值分别是相等的，设为 $B_{1}$ 和 $H_{1}$，而 $\Phi_{1}$（或 $B_{1}$ 和 $H_{1}$）的方向取为与电流 $i_1$ 呈右手螺旋关系。同理，在bc、cd、de三磁路段内的磁通相等，设为 $\Phi_{2}, B$ 和 $H$ 设为 $B_{2}$ 和 $H_{2}$，其方向与电流 $i_2$ 呈右手螺旋关系。对be段内的磁通设为 $\Phi_{3}, B$ 和 $H$ 设为 $B_{3}$ 和 $H_{3}$，截面积设为 $S_{3}, \Phi_{3}$ 的方向可任意指定，如图A-4所示。

![](images/page_506_image_7.jpg)

<details>
<summary>text_image</summary>

a
Φ₁
b
Φ₂
c
i₁
N₁
Φ₃
f
Φ₁
e
Φ₂
d
i₂
N₂
</details>

图A-4 分支磁路的例子

按式(A-5)，在b处有

$$
- \bar {\Phi} _ {1} - \bar {\Phi} _ {2} - \bar {\Phi} _ {3} = 0
$$

按式(A-6)，有

$$
H _ {1} (l _ {\mathrm{fa}} + l _ {\mathrm{ab}} + l _ {\mathrm{ef}}) - H _ {3} l _ {\mathrm{be}} = N _ {1} i _ {1}
$$

$$
H _ {2} (  l _ {\mathrm{bc}} + l _ {\mathrm{cd}} + l _ {\mathrm{de}}  ) - H _ {3} l _ {\mathrm{be}} = N _ {2} i _ {2}
$$

其他关系有

$$
B _ {1} = \frac {\Phi_ {1}}{S _ {1}}, \quad B _ {2} = \frac {\Phi_ {2}}{S _ {2}}, \quad B _ {3} = \frac {\Phi_ {3}}{S _ {3}}
$$

$$
B _ {1} = \mu_ {1} H _ {1}, \quad B _ {2} = \mu_ {2} H _ {2}, \quad B _ {3} = \mu_ {3} H _ {3}
$$

式中  $\mu_{1}, \mu_{2}, \mu_{3}$  分别为三磁路段的磁导率。

若磁路为同一铁磁材料构成,则有  $\mu_{1}=\mu_{2}=\mu_{3}$ 。

## §A-4 恒定磁通磁路的计算

通常在计算电机、电器的磁路时有两类问题,一类是预先给定磁通(或磁感应强度),然后按照给定的磁通和磁路的结构及材料去求所需磁通势 $F_{m}$ 。另一类问题是预先给定磁通势,要求求出磁路中的磁通。

恒定磁通磁路是指磁路中各励磁线圈的电流是直流,就是说磁路中的磁通和磁通势都是恒定的。

首先介绍无分支恒定磁通磁路的计算。无分支磁路的主要特点是在不计及漏磁通时,磁路中处处都有相等的(主)磁通 $\Phi$ ,其计算可按下述步骤进行:

（1）根据磁路中各部分的材料和截面积进行分段,要求每一段磁路具有相同的材料和截面积。
（2）根据各分段磁路的尺寸计算出各段的截面积和平均长度(一般沿中心线计算)。在计算截面积时,必须注意,计算出的截面积称为视在面积,要扣除硅钢片之间的绝缘层占去的截面积,才是磁感线通过的有效面积,一般可以用下式近似表示:

$$
\text {有效面积} = k \times \text {视在面积}
$$

式中 k 称为填充因数, 它随硅钢片厚度和绝缘层厚度而定, 一般约为 0.9 左右。

如磁路中存在空气隙,则磁通会向外扩张,造成边缘效应,如图 A-5 所示,增大了有效面积。当铁心为矩形截面时,其有效面积可按下式估算

(空气隙很短时):

$$
S _ {\mathrm{a}} \approx (a + \delta) (b + \delta) \approx a b + (a + b) \delta
$$

式中 a、b 分别为矩形截面的长和宽， $\delta$  为空气隙长度。对于半径为 r 的圆形截面，可按下式估算:

$$
S _ {\mathrm{a}} \approx \pi \left(r + \frac {\delta}{2}\right) ^ {2} \approx \pi r ^ {2} + \pi r \delta
$$

![](images/page_507_image_19.jpg)

<details>
<summary>text_image</summary>

N
S
δ
</details>

图 A-5 空气隙中磁通的边缘效应

(3) 根据已知的磁通计算各磁路段的磁感应强度  $B=\frac{\Phi}{S}$ 。

(4) 根据每一磁路段的 B, 查阅对应的磁性材料的基本磁化曲线, 求得每一磁路段的磁场强度 H; 对于空气隙有  $H_{a} = \frac{B_{a}}{\mu_{0}}$ , 或采用下列近似公式:

$$
H _ {\mathrm{a}} = \frac {B _ {\mathrm{a}}}{4 \pi \times 1 0 ^ {- 7}} \approx 0. 8 \times 1 0 ^ {6} B _ {\mathrm{a}}
$$

(5) 求出每一磁段的 Hl 值。
(6) 按式(A-6)求出所需磁通势。

例 A-1 某磁路的结构与尺寸(单位为 mm)如图 A-6(a)所示。已知  $\Phi = 15 \times 10^{-4} Wb, k = 0.90$  (填充因数)，励磁绕组的匝数为 120，所用硅钢片的基本磁化曲线如图 A-6(b) 所示。求励磁电流 I。

![](images/page_508_image_3.jpg)

图A-6 例A-1图

解 （1）根据该磁路的结构和尺寸,硅钢片有两种截面积,所以,该磁路连同空气隙共分为三段计算。

(2) 每段的截面积和平均长度为

$$
\begin{array}{l} \left\{ \begin{array}{l} S _ {1} = 5 0 \times 5 0 \times 0. 9 \mathrm{mm} ^ {2} = 2 2. 5 \times 1 0 ^ {- 4} \mathrm{m} ^ {2} \\ l _ {1} = 2 l _ {1} ^ {\prime} = (1 0 0 - 2 0) \times 2 \mathrm{mm} = 0. 1 6 \mathrm{m} \end{array} \right. \\ \left\{ \begin{array}{l} S _ {2} = 5 0 \times 2 0 \times 0. 9 \mathrm{mm} ^ {2} = 9 \times 1 0 ^ {- 4} \mathrm{m} ^ {2} \\ l _ {2} = l _ {2} ^ {\prime} + 2 l _ {3} ^ {\prime} = [ (2 5 0 - 5 0) \times 2 - 2 ] \mathrm{mm} = 0. 3 9 8 \mathrm{m} \end{array} \right. \\ \left\{ \begin{array}{l} S _ {\mathrm{a}} = [ 2 0 \times 5 0 + (2 0 + 5 0) \times 2 ] \mathrm{mm} ^ {2} = 1 1. 4 \times 1 0 ^ {- 4} \mathrm{m} ^ {2} \\ l _ {\mathrm{a}} = 2 \mathrm{mm} = 0. 0 0 2 \mathrm{m} \end{array} \right. \\ \end{array}
$$

(3) 每磁路段的磁感应强度为

$$
\begin{array}{l} B _ {1} = \frac {\Phi}{S _ {1}} = \frac {1 5 \times 1 0 ^ {- 4}}{2 2 . 5 \times 1 0 ^ {- 4}} \mathrm{T} = 0. 6 6 7 \mathrm{T} \\ B _ {2} = \frac {\varPhi}{S _ {2}} = \frac {1 5 \times 1 0 ^ {- 4}}{9 \times 1 0 ^ {- 4}} \mathrm{T} = 1. 6 6 7 \mathrm{T} \\ B _ {\mathrm{a}} = \frac {\varPhi}{S _ {\mathrm{a}}} = \frac {1 5 \times 1 0 ^ {- 4}}{1 1 . 4 \times 1 0 ^ {- 4}} \mathrm{T} = 1. 3 1 6 \mathrm{T} \\ \end{array}
$$

## (4) 每磁路段的磁场强度。

由图 A-6(b) 所示曲线查得

$$
H _ {1} = 1 7 0 \mathrm{A/m}, H _ {2} = 4 5 0 0 \mathrm{A/m}
$$

根据公式可得

$$
H _ {\mathrm{a}} = 0. 8 \times 1 0 ^ {6} B _ {\mathrm{a}} = 1 0. 5 3 \times 1 0 ^ {5} \mathrm{A/m}
$$

(5) 每磁路段的 Hl 为

$$
\begin{array}{l} H _ {1} l _ {1} = 1 7 0 \times 0. 1 6 \mathrm{A} = 2 7. 2 \mathrm{A} \\ H _ {2} l _ {2} = 4 5 0 0 \times 0. 3 9 8 \mathrm{A} = 1 7 9 1 \mathrm{A} \\ H _ {\mathrm{a}} l _ {\mathrm{a}} = 1 0. 5 3 \times 1 0 ^ {5} \times 0. 0 0 2 \mathrm{A} = 2. 1 0 6 \mathrm{A} \\ \end{array}
$$

(6) 总磁通势为

$$
F _ {\mathrm{m}} = N I = H _ {1} l _ {1} + H _ {2} l _ {2} + H _ {\mathrm{a}} l _ {\mathrm{a}} = 3 9 2 4 \mathrm{At}
$$

$$
I = \frac {F _ {\mathrm{m}}}{N} = \frac {3 9 2 4}{1 2 0} \mathrm{A} = 3 2. 7 \mathrm{A}
$$

从以上计算可以看出,空气隙虽然很短,它只占磁路平均长度的0.35%,但空气隙的 $H_{a}l_{a}$ 却占总磁通势的53.4%。这是由于空气的磁导率比硅钢片的磁导率小很多的缘故。在本例中, $l_{2}$ 部分的截面积较小,在磁通 $\Phi=15\times10^{-4}Wb$ 的作用下已处于饱和状态,使这部分硅钢片的磁导率显著下降,所以这一段的磁阻较大,磁位差增大,否则空气隙的磁位差所占比例还要高。

如果给定无分支磁路的磁通势而要求出该磁通势在磁路中激发的磁通,则由于磁路各段的磁导率不是常数,因此需要采用试探法或图解法,其求解步骤见下例。

例 A-2 图 A-7(a) 所示磁路中, 空气隙的长度  $l_{a}=1\ mm$ , 磁路横截面面积  $S=16\ cm^{2}$ , 中心线长度  $l=50\ cm$ , 线圈的匝数 N=1250, 励磁电流  $I=800\ mA$ 。磁路的材料为铸钢, 其基本磁化曲线如图 A-7(b) 所示。求磁路中的磁通。

![](images/page_509_image_16.jpg)

<details>
<summary>text_image</summary>

Φ
I
N
l
la
</details>

(a)

![](images/page_509_chart_18.jpg)

<details>
<summary>line</summary>

| H (A/m) | B (T) |
| --- | --- |
| 0 | 0 |
| ~250 | ~0.35 |
| ~500 | ~0.65 |
| ~750 | ~0.85 |
| ~1000 | ~1.05 |
| ~1250 | ~1.2 |
| ~1500 | ~1.3 |
</details>

(b)

图A-7 例A-2图

解 此磁路由两段构成,其平均长度和面积分别为(铸钢段)

$$
l _ {1} \approx 5 0 \mathrm{cm} = 0. 5 \mathrm{m}
$$

$$
S _ {1} = 1 6 \mathrm{cm} ^ {2} = 1 6 \times 1 0 ^ {- 4} \mathrm{m} ^ {2}
$$

(空气隙段)为简化起见,忽略空气隙的边缘效应,设

$$
l _ {\mathrm{a}} = 0. 1 \mathrm{cm} = 1 0 ^ {- 3} \mathrm{m}, S _ {\mathrm{a}} \approx 1 6 \times 1 0 ^ {- 4} \mathrm{m} ^ {2}
$$

磁路中的磁通势为

$$
F _ {\mathrm{m}} = N I = 1 2 5 0 \times 8 0 0 \times 1 0 ^ {- 3} \mathrm{At} = 1 0 0 0 \mathrm{At}
$$

由于空气隙的磁阻较大,故可暂设整个磁路磁通势全部用于空气隙中,这样算出的磁通作为第1次试探值 $\Phi^{1}$ ,即

$$
\begin{array}{l} \Phi^ {1} = B _ {\mathrm{a}} ^ {1} S _ {\mathrm{a}} = \frac {N I \mu_ {0} S _ {\mathrm{a}}}{l _ {\mathrm{a}}} = \frac {1 0 0 0 \times 1 6 \times 1 0 ^ {- 4} \times 4 \pi \times 1 0 ^ {- 7}}{1 0 ^ {- 3}} \mathrm{Wb} \\ = 2 0. 1 1 \times 1 0 ^ {- 4} \mathrm{Wb} \\ \end{array}
$$

由于设  $S_{1}=S_{a}$ ，故算得磁感应强度为

$$
B _ {1} ^ {1} = B _ {\mathrm{a}} ^ {1} = \frac {\Phi^ {1}}{S _ {1}} = \frac {2 0 . 1 1 \times 1 0 ^ {- 4}}{1 6 \times 1 0 ^ {- 4}} \mathrm{T} = 1. 2 6 \mathrm{T}
$$

按图 A-7(b) 查得

$$
H ^ {1} = 1 4 1 0 \mathrm{A/m}
$$

空气隙中的磁场强度为

$$
H _ {a} ^ {1} = 0. 8 \times 1 0 ^ {6} B _ {a} ^ {1} = 1 0. 0 8 \times 1 0 ^ {5} \mathrm{A/m}
$$

磁通势为

$$
F _ {\mathrm{m}} ^ {1} = H _ {1} ^ {1} l _ {1} + H _ {\mathrm{a}} ^ {1} l _ {\mathrm{a}} = 1 7 1 3 \mathrm{At}
$$

由于  $F_{m}^{1} \neq F_{m}(= NI)$ ，所以要进行第2、3、…次试探，直至误差小于某一给定值为止。从第2次试探起，各次试探值与前1次试探值之间可按下式联系起来:

$$
\Phi^ {n + 1} = \Phi^ {n} \frac {F _ {\mathrm{m}}}{F _ {\mathrm{m}} ^ {n}}
$$

各次试探结果见表 A-1。

表 A-1

| $n$ | $\sigma^{\mathrm{a}} \times {10}^{-4}/\mathrm{{Wb}}$ | ${B}_{1} = {B}_{\mathrm{n}}/\mathrm{T}$ | ${H}_{1}/\left( {\mathrm{A}/\mathrm{m}}\right)$ | ${H}_{2}/\left( {\mathrm{A}/\mathrm{m}}\right)$ | ${F}_{\mathrm{a}}/\mathrm{{Ai}}$ | 误差/% |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | 20.11 | 1.26 | 1 410 | ${10.10} \times {10}^{5}$ | 1 713 | +71.3 |
| 2 | 11.74 | 0.733 | 640 | ${5.87} \times {10}^{5}$ | 906 | -9.4 |
| 3 | 12.94 | 0.809 | 680 | ${6.47} \times {10}^{5}$ | 987 | -1.3 |
| 4 | 13.11 | 0.819 | 694 | ${6.55} \times {10}^{5}$ | 1 002 | +0.2 |

可见,第4次试探值可以作为最后的结果,即  $\Phi=\Phi^{4}=13.11\times10^{-4}$  Wb。求解这类问题的图解法与非线性电阻电路的图解法相似。以例 A-2 的无分支磁路为例说明,它可以看作是由两段磁路的磁阻串联组成,一是空气隙的磁阻  $R_{ma}$ ,它是线性的,另一是铁心(铸钢)的磁阻 $R_{\mathrm{ml}}$ ，它是非线性的，可以用韦安特性即磁通 $\Phi$ 与磁位差 $U_{\mathrm{m1}}(= H_1l_1)$ 的关系曲线 $\Phi - U_{\mathrm{m1}}$ 表示，它可以根据该磁段的截面积和平均长度，按基本磁化曲线上的磁感应强度值和对应的磁场强度值逐点求出。而 $R_{\mathrm{ma}}$ 则可表示为 $R_{\mathrm{ma}} = \frac{l_{\mathrm{a}}}{\mu_0S_{\mathrm{a}}}$ 。这样就可以获得图A-8(a)所示计算磁路图，其中 $F_{\mathrm{m}} = NI$ 相当于电路中的电压源电压。于是可以用类似于非线性电阻电路中的“曲线相交法”得出图A-8(b)，从两条曲线的交点即可求得所需磁通。

![](images/page_511_image_4.jpg)

图 A-8 计算磁路图及图解法

如果给定的无分支磁路是由几段不同的磁段组成的,则其计算磁路图可以看作是由几个磁阻串联组成的,同样可以用图解法求解。

有分支的恒定磁通磁路的计算比较复杂。下面通过一个具体的示例介绍计算方法的思路。

图 A-9 是具有一个磁通势的分支磁路。按假设的各磁通参考方向和磁路定律式(A-5)、式(A-6)，有下列关系式:

$$
\begin{array}{l} \Phi_ {1} = \Phi_ {2} + \Phi_ {3} \\ H _ {2} l _ {2} + H _ {\mathrm{a}} l _ {\mathrm{a}} = H _ {3} l _ {3} \\ H _ {1} l _ {1} + H _ {3} l _ {3} = N I \\ \end{array}
$$

如果给定的为通过空气隙的磁通  $\Phi_{2}$ ，则可直接求出所需磁通势。主要步骤如下:

![](images/page_511_image_11.jpg)

<details>
<summary>text_image</summary>

(l₁,S₁)
Φ₁
Φ₃
(l₃,S₃)
I
(lₐ,Sₐ)
Φ₂
(l₂,S₂)
</details>

图A-9 有分支磁路

(1) 从给定 $\Phi_{2}$ 可以求得 $B_{2} \left( = \frac{\Phi_{2}}{S_{2}}\right)$, 并从相应的基本磁化曲线查出 $H_{2}$, 这样就可以按下式求出 $H_{3}$.

$$
H _ {3} = \frac {H _ {2} l _ {2} + H _ {\mathrm{a}} l _ {\mathrm{a}}}{l _ {3}}
$$

(2) 由  $H_{3}$  和基本磁化曲线  $B_{3}-H_{3}$  查得  $B_{3}$ ，并可求得  $\Phi_{3}=B_{3}S_{3}$ 。
(3) 按  $\Phi_{1}=\Phi_{2}+\Phi_{3}$ ，求得  $\Phi_{1}$ 。