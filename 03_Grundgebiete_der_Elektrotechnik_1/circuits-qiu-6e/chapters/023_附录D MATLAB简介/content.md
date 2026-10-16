# 附录D MATLAB简介

原始 PDF 第 534–540 页。

The image contains no text or mathematical content to process. It is a graphical representation of a triangular shape composed of small, irregular black dots. Therefore, the correct OCR output is an empty string.

## 附录 D

## MATLAB 简介

附录 D 首先简要地介绍 MATLAB 的初步知识,然后,结合本书涉及的内容,简要介绍如何应用 MATLAB 求解电路问题。

## §D-1 MATLAB 概述

MATLAB 是美国 MathWorks 公司开发的大型数学计算软件, 它具有强大的矩阵处理功能和绘图功能, 已经广泛地应用于科学研究和工程技术的各个领域, MATLAB 以矩阵和向量为基本数据单元, 提供了丰富的矩阵操作和矩阵运算功能, 并在这些基本运算的基础上提供了可供各种科学研究和工程技术门类使用的工具箱, 极大地方便了科学计算和工程问题的求解, 使得科技人员从复杂的编程工作中解放出来, 专注于数学模型的建立。

例 D-1，求解以下线性代数方程组。

$$
\left[ \begin{array}{c c c} 1 & - 1 & - 1 \\ 1 0 & 1 0 & 0 \\ 1 0 & - 1 0 & 1 0 \end{array} \right] \left[ \begin{array}{c} i _ {1} \\ i _ {2} \\ i _ {3} \end{array} \right] = \left[ \begin{array}{c} 0 \\ 1 0 \\ 0 \end{array} \right]
$$

解 下列语句实现矩阵相乘和线性代数方程组的求解运算功能。

```matlab
A = [ 1 -1 -1; 10 10 0; 10 -10 10 ];
B = [ 0 10 0 ]';
i = inv(A) * B;
i
```

其中 A 是三阶方阵, B 是一阶转置矩阵, inv(A) 表示 A 的逆阵。运算结果如下:

```txt
i=
    0.6000
    0.4000
    0.2000
```

在 MATLAB 函数库中,除了基本初等函数外,还有初等矩阵和矩阵变换、线性代数

---

§ D-2 MATLAB 在电路分析中的应用举例

511

方程组和矩阵特征值的求解、多项式运算和求根、函数的插值和数据的多项式拟合、数值积分和常微分方程数值解、函数求极值、单变量非线性方程求根、数据分析和傅里叶变换，以及某些特殊的矩阵函数和数学函数，这些函数都可以直接调用。用户还可以根据自己的需要任意扩充函数库。

MATLAB 中常用的数学函数有:

三角函数和双曲函数类:正弦函数 sin、余弦函数 cos、正切函数 tan、余切函数 cot、反正弦函数 asin、反余弦函数 acos、反正切函数 atan、反余切函数 acot、双曲正弦函数 sinh、双曲余弦函数 cosh、双曲正切函数 tanh，双曲余切函数 coth、反双曲正弦函数 asinh、反双曲余弦函数 acosh、反双曲正切函数 atanh，反双曲余切函数 acoth 等。

指数对数函数类: 指数函数 exp、自然对数函数 log、常用对数 log 10、以 2 为底的对数 log 2、平方根函数 sqrt 等。

圆整函数和求余函数类:向正无穷圆整函数ceil、向负无穷圆整函数floor、向0圆整函数fix、模除求余函数mod、四舍五入函数round、符号函数sign等。

MATLAB 规定了一些内置变量, 其中常用的有: eps 表示误差容限, i 和 j 表示虚数单位; inf 表示正无穷大量, 而 -inf 表示负无穷大量; 用 NaN 表示不定值, 如 inf/inf 或 0/0; pi 表示圆周率  $\pi$ 。

MATLAB 的基本算数运算符主要有: 加法运算符+, 减法运算符-, 数组乘法运算符. \*, 数组除法运算符./, 数组乘幂运算符.^, 非共轭转置运算符.', 共轭转置运算符', 矩阵乘法运算符 \*, 矩阵右除运算符/, 矩阵左除运算符\ (注意: MATLAB 中的除法中有右除和左除之分, 如矩阵 A、B, 则 $AB^{-1}$ 可表示成 A/B, 而 $A^{-1}B$ 表示为 A\B), 矩阵乘幂运算符^等。

MATLAB 绘图功能使用方法也非常简便。可以绘制二维或三维图形,用户可以根据需要在坐标图上加标题、坐标轴标记、文本注释及栅格等,还可以指定图线形式(如实线、虚线等)和颜色,也可以在同一张图上画出不同函数的曲线,对于曲面图还能画出等高线。

MATLAB 常用绘图命令有: plot 表示线性 x-y 坐标图; plot3 表示线性 x-y-z 三维坐标图; mesh 表示三维消隐图。

MATLAB 常用图形注释命令有: title 表示题头标注, xlabel 表示 x 轴标注, ylabel 表示 y 轴标注。

## §D-2 MATLAB 在电路分析中的应用举例

现以下述电路为例,简要介绍如何使用 MATLAB 进行电路分析问题的求解。

## 1. 直流电路分析

例 D-2 电路如图 D-1 所示, 已知 $R_{1} = 10 \Omega, R_{2} = 20 \Omega, R_{3} = R_{4} = 10 \Omega, u_{\mathrm{S}} = 40 \mathrm{~V}, i_{\mathrm{S}} = 1 \mathrm{~A}$, 求节点电压 $u_{\mathrm{n1}}, u_{\mathrm{n2}}$。

---

512

附录 D MATLAB 简介

解 以节点①为参考节点,电路的节点电压方程为

$$
\left(G _ {1} + G _ {2} + G _ {3}\right) u _ {\mathrm{n1}} - G _ {3} u _ {\mathrm{n2}} = G _ {1} u _ {\mathrm{S}} + i _ {\mathrm{S}}
$$

$$
- \left(G _ {3} + 2 G _ {4}\right) u _ {\mathrm{n1}} + \left(G _ {3} + G _ {4}\right) u _ {\mathrm{n2}} = - i _ {\mathrm{S}}
$$

将节点电压方程写成矩阵形式,在 MATLAB 命令菜单中输入 edit 命令进入程序编辑器,编辑文件。运行下述程序:

$$
\mathrm{G} 1 = 1 / 1 0; \mathrm{G} 2 = 1 / 2 0; \mathrm{G} 3 = 1 / 1 0; \mathrm{G} 4 = 1 / 1 0;
$$

$$
\mathrm{us} = 4 0; \mathrm{is} = 1;
$$

$$
\mathrm{Gn} = \left[ \mathrm{G1} + \mathrm{G2} + \mathrm{G3} - \mathrm{G3}; - (\mathrm{G3} + 2 * \mathrm{G4}) \mathrm{G3} + \mathrm{G4} \right]
$$

$$
\mathrm{In} = \left[ \mathrm{G1} * \mathrm{us} + \mathrm{is}; - \mathrm{is} \right];
$$

$$
\mathrm{Un} = \mathrm{inv} (\mathrm{Gn}) * \mathrm{In}.
$$

得出以下运算结果。

$$
\begin{array}{l} \mathrm{Gn} = \quad \cap \\ 0. 2 5 0 0 \quad - 0. 1 0 0 0 \\ - 0. 3 0 0 0 \quad 0. 2 0 0 0 \\ \mathrm{Un} = \\ 4 5. 0 0 0 0 \\ 6 2. 5 0 0 0 \\ \end{array}
$$

## 2. 交流电路分析

![](../../raw/pages_0513-0544/images/page_535_image_15.jpg)

<details>
<summary>text_image</summary>

iS
①
+
us
-
R1
+
u1
R2
-
①
R3
②
R4
+
2u1
-
</details>

图D-1 例D-2电路

应用 MATLAB 进行复数和相量运算也是很方便的,下面用例题予以说明。

例 D-3 正弦稳态电路如图 D-2 所示, 已知  $R_{1}=R_{2}=5\Omega$ ,  $j\omega L_{1}=j\omega L_{2}=j5\Omega$ ,  $-j\frac{1}{\omega C}=-j5\Omega$ ,  $\dot{U}_{s}=10/0^{\circ}V$ , 试求电流  $\dot{I}_{11}$  和  $\dot{I}_{12}$ 。

![](../../raw/pages_0513-0544/images/page_535_image_19.jpg)

<details>
<summary>text_image</summary>

a \dot{I}_a R_1 L_1 c R_2 L_2 b
\dot{U}_s +
- \dot{I}_{11} C \dot{I}_{12} \dot{I}_b
</details>

图 D-2 例 D-3 电路

解 其回路电流方程为

$$
(5 + \mathrm{j} 5 - \mathrm{j} 5) \dot {I} _ {1 1} + \mathrm{j} 5 \dot {I} _ {1 2} = 1 0 / 0 ^ {\circ}
$$

$$
\mathrm{j} 5 \dot {I} _ {1 1} + (5 + \mathrm{j} 5 - \mathrm{j} 5) \dot {I} _ {1 2} = 0
$$

将回路电流方程写成矩阵形式,在 MATLAB 命令菜单中输入 edit 命令进入程序编辑器,编辑文件。注意: MATLAB 一般用“i”表示虚数,这里为了不重复,我们用“x”表示回路电流,运行下述程序:

---

§ D-2 MATLAB 在电路分析中的应用举例

513

```matlab
A = [ 5 + 5 * i - 5 * i 5 * i ; 5 * i 5 + 5 * i - 5 * i ] ;
B = [ 10 0 ]';
x = inv( A ) * B ;
x
```

计算结果为

<div class="docvortex-algorithm" style="white-space: pre-wrap; font-family:monospace;">
$\mathrm{x} =$
</div>

1.0000

```txt
0 - 1.0000i
```

即  $\dot{I}_{a} = \dot{I}_{11} = 1 A, \dot{I}_{b} = \dot{I}_{12} = -j1 A。$

这里若采用 MATLAB 中一般代数方程组的求解方式, 求解指令是 solve, 该指令的使用格式如下:

$$
\mathrm{S} = \text {solve} \left(^ {\prime} \mathrm{eq} 1 ^ {\prime}, ^ {\prime} \mathrm{eq} 2 ^ {\prime}, \dots , ^ {\prime} \mathrm{eqn} ^ {\prime}, ^ {\prime} \mathrm{v} 1 ^ {\prime}, ^ {\prime} \mathrm{v} 2 ^ {\prime}, \dots , ^ {\prime} \mathrm{vn} ^ {\prime}\right)
$$

其中'eq1', 'eq2', ..., 'eqn', 是字符串表达的方程; 而 'v1', 'v2', ..., 'vn' 是字符串表达的求解变量名。S 是一个构架数组。如要显示求解结果, 必须采用 S.v1, S.v2, ..., S.vn 的援引方式。

将电路方程编写为如下程序文件:

```javascript
S = solve('(5+5*i-5*i)*x+5*i*y=10','5*i*x+(5+5*i-5*i)*y=0','x','y');
disp('S,x'),disp(S.x),disp('S,y'),disp(S.y)
```

这里 x 表示回路电流  $\dot{I}_{11}$ , y 表示回路电流  $\dot{I}_{12}$ , 运行程序后得

```txt
S,x
1
```

```txt
S, y
-i
```

可见采用 MATLAB 中的两种算法所得电路方程结果完全一致。

例 D-4 含理想运算放大器的低通滤波电路如图 D-3 所示, 已知  $G_{1}=G_{2}=G_{3}=10^{-3}$  S,  $C_{1}=1.414\times10^{-3}$  F,  $C_{2}=0.707\times10^{-4}$  F。试绘制传递函数  $H(s)=\frac{U_{2}(s)}{U_{i}(s)}$  的幅频特性。

解 应用节点法得到传递函数  $H(s)$  如下:

$$
\begin{array}{l} H (s) = \frac {U _ {2} (s)}{U _ {i} (s)} = - \frac {G _ {1} G _ {2} / C _ {1} C _ {2}}{s ^ {2} + \frac {(G _ {1} + G _ {2} + G _ {3})}{C _ {1}} s + \frac {G _ {2} G _ {3}}{C _ {1} C _ {2}}} \\ = - \frac {1 0}{s ^ {2} + 2 . 1 2 s + 1 0} \\ \end{array}
$$

---

514

附录 D MATLAB 简介

![](../../raw/pages_0513-0544/images/page_537_image_3.jpg)

<details>
<summary>text_image</summary>

G1
①
G2
a
G3
sC2
U1(s)
-
G1
②
+
-
U2(s)
+
-
sC1
b
+
①
</details>

图D-3 例D-4电路

应用 MATLAB, 在命令菜单中输入 edit 命令进入程序编辑器, 编辑并输入文件。有

```matlab
num = 10;
den = [ 1 2.12 10 ];
w = 0 : 0.01 : 10;
g = freqs( num, den, w );
mag = abs( g );
plot( w, mag )
xlabel( 'Frequency-rad/s' );
ylabel( 'Magnitude' );
```

在程序中:

第 1 行，“num”表示传递函数的分子多项式，“10”是分子。

第 2 行，“den”指传递函数的分母多项式，“1”是分母多项式中二次函数的系数，“2.12”是分母多项式中一次函数的系数，“10”是常数项。

第 3 行，“w”表示角频率，“0”表示起始频率，“0.01”表示间隔，“10”表示终止频率。

第 4 行，“g”表示传递函数，“freqs()”表示频率特性。

第 5 行，“mag=abs(g)”表示传递函数幅频特性的幅值。

第 6 行，“plot(w, mag)”表示绘出传递函数幅频特性图。

第 7 行，“xlabel”表示幅频特性图的横坐标。

第 8 行，“ylabel”表示幅频特性图的纵坐标。

运行上述程序得到的幅频特性如图 D-4 所示。

## 3. 动态电路计算

MATLAB 为求解常微分方程提供了一组配套齐全,结构完整的指令。包括: 常微分方程解算指令 (Solver), 调用的 ODE 文件格式指令 (MATLAB 中计算导数的 M 函数文件称为 ODE 文件)。“ode23” 是采用二、三阶龙格-库塔法求解常微分方程调用的 ODE 文件, “ode45” 是采用四、五阶龙格-库塔法求解常微分方程调用的 ODE 文件。

---

§ D-2 MATLAB 在电路分析中的应用举例

515

![](../../raw/pages_0513-0544/images/page_538_chart_3.jpg)

<details>
<summary>line</summary>

| Frequency-rad/s | Magnitude |
| --- | --- |
| 0 | 1.0 |
| 1 | ~1.1 |
| 2 | ~1.35 |
| 2.8 | ~1.6 |
| 4 | ~0.9 |
| 5 | ~0.55 |
| 6 | ~0.35 |
| 7 | ~0.25 |
| 8 | ~0.18 |
| 9 | ~0.14 |
| 10 | ~0.12 |
</details>

图 D-4 例 D-4 电路的幅频特性

利用 MATLAB 指令具体求解动态电路的步骤是:

（1）应用支路法或回路法等写出电路的一阶微分方程组和相应的初始条件，这里变量指定用 y 表示。
(2) 编写能计算导数的 M 函数文件, 最简易的编写方法是把 y, t 作为输入宗量。
（3）将编写好能计算导数的 M 函数文件(ODE 函数文件)和初始值供微分方程解算指令(solver)调用,运行程序后就可得到变量 y 及其导数在指定时间上的数值解。

solver 解算指令的使用格式为

$$
[ t, \mathrm{YY} ] = \text {solver} (^ {\prime} \mathrm{F} ^ {\prime}, \text {tspan}, \mathrm{Y0})
$$

这是用 MATLAB 求解微分方程的最简单的格式。实际计算时, solver 应是具体指令名（如 ode45），这里输入宗量“F”是 ODE 函数文件名；当 tspan 被赋予二元向量 [t0, tf] 时，“tspan”用来定义求数值解的时间区间。输入宗量“Y0”表示初始值的列向量。

例 D-5 二阶动态电路如图 D-5 所示, 已知电压源  $u_{s}=10\ V, R_{1}=4\ \Omega, R_{2}=0.2\ \Omega, C_{1}=1\ F, L=1\ H, u_{c}(0_{-})=0, i_{L}(0_{-})=0, t=0$  时开关 S 闭合, 试绘出电容电压  $u_{c}$  的波形。

解 电路的状态方程表示如下:

$$
\frac {\mathrm{d} u _ {c}}{\mathrm{d} t} = - \frac {1}{R _ {1} C} u _ {c} - \frac {1}{C} i _ {L} + \frac {u _ {\mathrm{s}}}{R _ {1} C}
$$

$$
\frac {\mathrm{d} i _ {L}}{\mathrm{d} t} = \frac {1}{L} u _ {c} - \frac {R _ {2}}{L} i _ {L}
$$

应用 MATLAB, 在命令菜单中输入 edit 命令进入程序编辑器, 编辑文件。电路的一阶微分方程组编写的 MATLAB 文件为

$$
\text {function} \mathrm{yd} = \mathrm{DYDt50(t,y)}
$$

![](../../raw/pages_0513-0544/images/page_538_image_19.jpg)

<details>
<summary>text_image</summary>

S(t=0)
+
us
-
R1
+
uc
C
-
R2
iL
+
uL
L
-
</details>

图 D-5 例 D-5 电路

---

516

附录 D MATLAB 简介

```matlab
U = 10;
R1 = 4;
R2 = 0.2;
C = 1;
L = 1;
yd = [-(1/(R1 * C))*y(1)-(1/C)*y(2)+(1/(R1 * C))*U;
(1/L)*y(1)-(R2/L)*y(2)];
```

solver 解算指令的使用格式程序为

```matlab
tspan≡[0,40];
y0=[0;0];
[t,YY]=ode45('DYDt50',tspan,y0);
plot(t,YY(:,1));
xlabel('t'),ylabel('uc');
```

在程序中:

第 1 行，“tspan”用来定义求数值解的时间区间，“0”表示起始时间，“40”表示终止时间。

第 2 行，“y0”表示电路变量的初始时值。

第 3 行, solver 解算指令的使用格式。

第 4 行，“plot(t,YY(:,1))”表示绘制变量  $y(1)$  [即  $u_{c}(t)$ ] 的时域波形图。

第 5 行, 表示横坐标是 t, 纵坐标是  $u_{C}$ 。

调用 solver 解算指令的使用格式程序, 运行程序得  $u_{c}(t)$  的时域波形如图 D-6 所示。

![](../../raw/pages_0513-0544/images/page_539_chart_13.jpg)

<details>
<summary>line</summary>

| t | uC |
| --- | --- |
| 0 | 0 |
| ~2 | ~2.15 |
| 5 | ~-0.35 |
| ~8 | ~0.9 |
| ~11 | ~0.3 |
| ~14 | ~0.6 |
| ~17 | ~0.45 |
| ~20 | ~0.5 |
| 25~40 | ~0.45 |
</details>

图 D-6  $u_{c}(t)$  的时域波形
