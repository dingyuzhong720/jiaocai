# 第16章 二端口网络

原始 PDF 第 417–438 页。

![](../../raw/pages_0417-0448/images/page_416_image_0.jpg)

<details>
<summary>text_image</summary>

第十六章
二端口网络
</details>

![](../../raw/pages_0417-0448/images/page_416_image_1.jpg)

## 导读

在工程实际中经常会遇到二端口和多端口问题，在有些情况下，用二端口或多端口分析电路会给人们带来方便。例如利用二端口方程和参数描述电路，使电路模型更简洁。本章介绍二端口（网络）及其方程，二端口的 $Y, Z, T(A), H$ 等参数矩阵以及它们之间的相互关系，还介绍转移函数，T形和 $\pi$ 形等效电路及二端口的连接。最后介绍两种可用二端口描述的电路元件——回转器和负阻抗变换器。

## §16-1 二端口网络

前面讨论的电路分析主要属于这样一类问题:在一个电路及其输入已经给定的情况下,如何去计算一条或多条支路的电压和电流。如果一个复杂的电路只有两个端子向外连接,且仅对外接电路中的情况感兴趣,则该电路可视为一个一端口,并用戴维南或诺顿等效电路替代,然后再计算感兴趣的电压和电流。在工程实际中遇到的问题还常常涉及两对端子之间的关系,如变压器、滤波器、放大器、反馈网络等,如图16-1(a)(b)(c)所示。对于这些电路,都可以把两对端子之间的电路概括在一个方框中,如图16-1(d)所示。一对端子1-1'通常是输入端子,另一对端子2-2'为输出端子。

如果这两对端子满足端口条件,即对于所有时间t,从端子1流入方框的电流等于从端子1'流出的电流;同时,从端子2流入方框的电流等于从端子2'流出的电流,这种电路称为二端口网络,简称二端口。若向外伸出的4个端子上的电流无上述限制,称为四端网络。本章仅讨论二端口。

用二端口概念分析电路时,仅对二端口处的电流、电压之间的关系感兴趣,这种相互关系可以通过一些参数表示,而这些参数只决定于构成二端口本身的元件及它们的连接方式。一旦确定表征这个二端口的参数后,当一个端口的电压、电流发生变化,要找出另外一个端口上的电压、电流就比较容易了。同时,还可以利用这些参数比较不同的二端口在传递电能和信号方面的性能,从而评价它们的质量。一个任意复杂的二端

---

394

第十六章 二端口网络

口,还可以看作由若干简单的二端口组成。如果已知这些简单的二端口的参数,那么,根据它们与复杂二端口的关系就可以直接求出后者的参数,从而找出后者在两个端口处的电压与电流关系,而不再涉及原来复杂电路内部的任何计算。总之,这种分析方法有它的特点,与前面介绍的一端口有类似的地方。

![](../../raw/pages_0417-0448/images/page_417_image_4.jpg)

图16-1 二端口

本章介绍的二端口是由线性的电阻、电感（包括耦合电感）、电容和线性受控源组成，并规定不包含任何独立电源（如用运算法分析时，还规定独立的初始条件均为零，即不存在附加电源）。

## §16-2 二端口的方程和参数

图 16-2 所示为一线性二端口。在分析中将按正弦稳态情况考虑，并应用相量法。

当然，也可以用运算法讨论。在端口1-1'和2-2'处的电流相量和电压相量的参考方向如图所示。假设两个端口电压 $\dot{U}_{1}$ 和 $\dot{U}_{2}$ 已知，可以利用替代定理把两个端口电压 $\dot{U}_{1}$ 和 $\dot{U}_{2}$ 都看作是外施的独立电压源。这样，根据叠加定理， $\dot{I}_{1}$ 和 $\dot{I}_{2}$ 应分别等于各个独立电压源单独作用时产生的电流之和，即

![](../../raw/pages_0417-0448/images/page_417_image_10.jpg)

<details>
<summary>text_image</summary>

1○+ 
Ü₁
1'○-
İ₁
.
İ₂
2○+
Ü₂
-2'
-
</details>

图 16-2 线性二端口的电流电压关系

$$
\left. \begin{array}{l} \dot {I} _ {1} = Y _ {1 1} \dot {U} _ {1} + Y _ {1 2} \dot {U} _ {2} \\ \dot {I} _ {2} = Y _ {2 1} \dot {U} _ {1} + Y _ {2 2} \dot {U} _ {2} \end{array} \right\} \tag {16-1}
$$

式(16-1)还可以写成如下的矩阵形式

$$
\left[ \begin{array}{c} \dot {I} _ {1} \\ \dot {I} _ {2} \end{array} \right] = \left[ \begin{array}{c c} Y _ {1 1} & Y _ {1 2} \\ Y _ {2 1} & Y _ {2 2} \end{array} \right] \left[ \begin{array}{c} \dot {U} _ {1} \\ \dot {U} _ {2} \end{array} \right] = \boldsymbol {Y} \left[ \begin{array}{c} \dot {U} _ {1} \\ \dot {U} _ {2} \end{array} \right]
$$

---

§ 16-2 二端口的方程和参数

395

其中

$$
Y \stackrel {\mathrm{def}} {=} \left[ \begin{array}{l l} Y _ {1 1} & Y _ {1 2} \\ Y _ {2 1} & Y _ {2 2} \end{array} \right]
$$

称为二端口的 Y 参数矩阵，而  $Y_{11}$ 、 $Y_{12}$ 、 $Y_{21}$ 、 $Y_{22}$  称为二端口的 Y 参数。不难看出 Y 参数属于导纳性质，可以按下述方法计算或试验测量求得:如果在端口 1-1' 上外施电压  $\dot{U}_{1}$ ，而把端口 2-2' 短路，即  $\dot{U}_{2}=0$ ，工作情况如图 16-3(a) 所示。由式(16-1) 可得

$$
Y _ {1 1} = \frac {\dot {I} _ {1}}{\dot {U} _ {1}} \Bigg | _ {\dot {U} _ {2} = 0}
$$

$$
Y _ {2 1} = \frac {\dot {I} _ {2}}{\dot {U} _ {1}} \Bigg | _ {\dot {U} _ {2} = 0}
$$

$Y_{11}$  表示端口  $2-2'$  短路时，端口  $1-1'$  处的输入导纳或驱动点导纳； $Y_{21}$  表示端口  $2-2'$  短路时，端口  $2-2'$  与端口  $1-1'$  之间的转移导纳，这是因为  $Y_{21}$  是  $\dot{I}_{2}$  与  $\dot{U}_{1}$  的比值，它表示一个端口的电流与另一个端口的电压之间的关系。

同理,在端口 2-2'外施电压  $\dot{U}_{2}$ , 而把端口 1-1'短路, 即  $\dot{U}_{1}=0$ , 工作情况如图 16-3(b) 所示, 由式(16-1)得到

$$
Y _ {1 2} = \frac {\dot {I} _ {1}}{\dot {U} _ {2}} \Bigg | _ {\dot {U} _ {1} = 0}
$$

$$
Y _ {2 2} = \frac {\dot {I} _ {2}}{\dot {U} _ {2}} \Bigg | _ {\dot {U} _ {1} = 0}
$$

$Y_{12}$ 是端口 $1-1'$ 与端口 $2-2'$ 之间的转移导纳， $Y_{22}$ 是端口 $2-2'$ 的输入导纳。由于Y参数都是在一个端口短路情况下通过计算或测试求得的，所以又称为短路导纳参数，例如 $Y_{11}$ 就称为端口 $1-1'$ 的短路输入导纳。以上说明了Y参数表示的具体含义。

![](../../raw/pages_0417-0448/images/page_418_image_13.jpg)

<details>
<summary>text_image</summary>

1
+   Ê₁
-       1'
+       Ê₁
+       2
+       Ê₂=0
-       2'
</details>

(a)

![](../../raw/pages_0417-0448/images/page_418_image_15.jpg)

<details>
<summary>text_image</summary>

1
+
U₁=0
-
1'
I₁
I₂
2
+
U₂
-
2'
+U₂
-
</details>

(b)

图 16-3 短路导纳参数的测定

例 16-1 求图 16-4(a) 所示二端口的 Y 参数。

解 这个端口的结构比较简单, 它是一个  $\pi$  形电路。求它的  $Y_{11}$  和  $Y_{12}$  时, 把端口  $2-2'$  短路, 在端口  $1-1'$  上外施电压  $\dot{U}_{1}$  [如图 16-4(b) 所示], 这时可求得

$$
\begin{array}{l} \dot {I} _ {1} = \dot {U} _ {1} (Y _ {\mathrm{a}} + Y _ {\mathrm{b}}) \\ - \dot {I} _ {2} = \dot {U} _ {1} Y _ {\mathrm{b}} \\ \end{array}
$$

---

396

第十六章 二端口网络

式中  $\dot{I}_{2}$  前有负号是由指定的电流和电压参考方向造成的。根据定义可求得

$$
Y _ {1 1} = \frac {\dot {I} _ {1}}{\dot {U} _ {1}} \Bigg | _ {\dot {U} _ {2} = 0} = Y _ {\mathrm{a}} + Y _ {\mathrm{b}},
$$

$$
Y _ {2 1} = \frac {\dot {I} _ {2}}{\dot {U} _ {1}} \Bigg | _ {\dot {U} _ {2} = 0} = - Y _ {\mathrm{b}}
$$

同样,如果把端口 1-1'短路,并在端口 2-2'上外施电压  $\dot{U}_{2}$ ,则可求得

$$
Y _ {1 2} = - Y _ {\mathrm{b}}
$$

$$
Y _ {2 2} = Y _ {\mathrm{b}} + Y _ {\mathrm{c}}
$$

![](../../raw/pages_0417-0448/images/page_419_image_9.jpg)

<details>
<summary>text_image</summary>

1
Yb
2
Ya
Yc
1'
2'
</details>

(a)

![](../../raw/pages_0417-0448/images/page_419_image_11.jpg)

<details>
<summary>text_image</summary>

1
+
I₁
Yb
I₂
2
U̇₁
Ya
Yc
1'
2'
</details>

(b)

![](../../raw/pages_0417-0448/images/page_419_image_13.jpg)

<details>
<summary>text_image</summary>

1
I₁
Yb
I₂
2
+
Ya
\ Yc
U₂
-
1'
2'
</details>

(c)

图16-4 例16-1图

由此可见， $Y_{12}=Y_{21}$ 。此结果虽然是根据这个特例得到的，但是根据互易定理不难证明，对于由线性R、L(M)、C元件构成的任何无源二端口， $Y_{12}=Y_{21}$ 总是成立的。所以对任何一个无源线性二端口，只要3个独立的参数就足以表征它的性能。

如果一个二端口的 $Y$ 参数, 除了 $Y_{12} = Y_{21}$ 外, 还有 $Y_{11} = Y_{22}$, 则此二端口的两个端口 $1 - 1'$ 和 $2 - 2'$ 互换位置后与外电路连接, 其外部特性将不会有任何变化。也就是说, 这种二端口从任一端口看进去, 它的电气特性是一样的, 因而称为电气上对称的, 或简称为对称二端口。结构上对称①的二端口显然一定是对称二端口。例如在例 16-1 中的 $\pi$ 形电路, 如果 $Y_{\mathrm{a}} = Y_{\mathrm{c}}$, 它在结构上就是对称的, 这时就有 $Y_{11} = Y_{22}$ 。但是电气上对称并不一定意味着结构上对称。显然, 对于对称二端口的 $Y$ 参数, 只有 2 个是独立的。

假设图 16-2 所示二端口的  $\dot{I}_{1}$  和  $\dot{I}_{2}$  是已知的，可以利用替代定理把  $\dot{I}_{1}$  和  $\dot{I}_{2}$  看作是外施电流源的电流。根据叠加定理， $\dot{U}_{1}$ 、 $\dot{U}_{2}$  应等于各个电流源单独作用时产生的电压之和，即

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① “结构上对称”是指连接方式和元件性质及其参数的大小均具对称性。</span></small>

---

§ 16-2 二端口的方程和参数

397

$$
\left. \begin{array}{l} \dot {U} _ {1} = Z _ {1 1} \dot {I} _ {1} + Z _ {1 2} \dot {I} _ {2} \\ \dot {U} _ {2} = Z _ {2 1} \dot {I} _ {1} + Z _ {2 2} \dot {I} _ {2} \end{array} \right\} \tag {16-2}
$$

式中 $Z_{11}, Z_{12}, Z_{21}, Z_{22}$ 称为 $Z$ 参数，它们具有阻抗性质。$Z$ 参数可按下述方法计算或试验测量求得:设端口 $2 - 2'$ 开路，即 $\dot{I}_2 = 0$ ，只在端口 $1 - 1'$ 施加一个电流源 $\dot{I}_1$ ，如图16-5(a)所示。由式(16-2)可得

$$
\begin{array}{l} Z _ {1 1} = \frac {\dot {U} _ {1}}{\dot {I} _ {1}} \Bigg | _ {-} \dot {I} _ {2} = 0 \\ Z _ {2 1} = \frac {\dot {U} _ {2}}{\dot {I} _ {1}} \Bigg | _ {\dot {I} _ {2} = 0} \\ \end{array}
$$

所以 $Z_{11}$ 称为端口 $2 - 2^{\prime}$ 开路时端口 $1 - 1^{\prime}$ 的开路输入阻抗，$Z_{21}$ 称为端口 $2 - 2^{\prime}$ 开路时端口 $2 - 2^{\prime}$ 与端口 $1 - 1^{\prime}$ 之间的开路转移阻抗。同理，将端口 $1 - 1^{\prime}$ 开路，即 $\dot{I}_1 = 0$ ，并在端口 $2 - 2^{\prime}$ 施加电流源 $\dot{I}_2$ ，如图16-5(b)所示，由式(16-2)得

$$
\begin{array}{l} Z _ {1 2} = \frac {\dot {U} _ {1}}{\dot {I} _ {2}} \Bigg | _ {\dot {I} _ {1} = 0} \\ Z _ {2 2} = \frac {\dot {U} _ {2}}{\dot {I} _ {2}} \Bigg | _ {\dot {I} _ {1} = 0} \\ \end{array}
$$

即 $Z_{12}$ 是端口 $1 - 1'$ 开路时端口 $1 - 1'$ 与端口 $2 - 2'$ 之间的开路转移阻抗，$Z_{22}$ 是端口 $1 - 1'$ 开路时端口 $2 - 2'$ 的开路输入阻抗。

![](../../raw/pages_0417-0448/images/page_420_image_8.jpg)

图16-5 开路阻抗参数的测定

把式(16-2)改写成矩阵形式,有

$$
\left[ \begin{array}{c} \dot {U} _ {1} \\ \dot {U} _ {2} \end{array} \right] = \left[ \begin{array}{c c} Z _ {1 1} & Z _ {1 2} \\ Z _ {2 1} & Z _ {2 2} \end{array} \right] \left[ \begin{array}{c} \dot {I} _ {1} \\ \dot {I} _ {2} \end{array} \right] = \mathbb {Z} \left[ \begin{array}{c} \dot {I} _ {1} \\ \dot {I} _ {2} \end{array} \right]
$$

其中

$$
\mathbb {Z} \stackrel {\mathrm{def}} {=} \left[ \begin{array}{l l} Z _ {1 1} & Z _ {1 2} \\ Z _ {2 1} & Z _ {2 2} \end{array} \right]
$$

称为二端口的 Z 参数矩阵,也称开路阻抗矩阵。

同理,根据互易定理不难证明,对于线性 R、L(M)、C 元件构成的任何无源二端口,

![](../../raw/pages_0417-0448/images/page_420_image_16.jpg)

<details>
<summary>text_image</summary>

Technical diagram with labeled mechanical components and annotations, likely from a technical drawing or engineering manual.
</details>

---

398

第十六章 二端口网络

$Z_{12}=Z_{21}$  总是成立的。所以在这种情况下，Z 参数只有 3 个是独立的。对于对称的二端口，则还有  $Z_{11}=Z_{22}$  的关系，故只有 2 个参数是独立的。

比较式(16-1)与式(16-2)可以看出开路阻抗矩阵 $Z$ 与短路导纳矩阵 $Y$ 之间存在着互为逆阵的关系, 即

$$
\mathbf {Z} = \mathbf {Y} ^ {- 1} \text {或} \mathbf {Y} = \mathbf {Z} ^ {- 1}
$$

即

$$
\left[ \begin{array}{l l} Z _ {1 1} & Z _ {1 2} \\ Z _ {2 1} & Z _ {2 2} \end{array} \right] = \frac {1}{\Delta_ {Y}} \left[ \begin{array}{c c} Y _ {2 2} & - Y _ {1 2} \\ - Y _ {2 1} & Y _ {1 1} \end{array} \right] \tag {16-3}
$$

式中  $\Delta_{Y}=Y_{11}Y_{22}-Y_{12}Y_{21}$ 。

对于含有受控源的线性 $R, L(M), C$ 二端口，利用特勒根定理可以证明互易定理一般不再成立，因此 $Y_{12} \neq Y_{21}, Z_{12} \neq Z_{21}$ 。下面的例子将说明这一点。

例 16-2 求图 16-6 所示二端口的 Y 参数。

解 把端口 2-2' 短路, 在端口 1-1' 外施电压  $\dot{U}_{1}$ , 得

$$
\dot {I} _ {1} = \dot {U} _ {1} (Y _ {\mathrm{a}} + Y _ {\mathrm{b}})
$$

$$
\dot {I} _ {2} = - \dot {U} _ {1} Y _ {\mathrm{b}} - g \dot {U} _ {1}
$$

于是,可求得

$$
Y _ {1 1} = \frac {\dot {I} _ {1}}{\dot {U} _ {1}} = Y _ {\mathrm{a}} + Y _ {\mathrm{b}}
$$

$$
Y _ {2 1} = \frac {\dot {I} _ {2}}{\dot {U} _ {1}} = - Y _ {\mathrm{b}} - g
$$

![](../../raw/pages_0417-0448/images/page_421_image_17.jpg)

<details>
<summary>text_image</summary>

1
+
I₁
Yb
I₂
2
+
U̇₁
Ya
Yc
gÛ₁
U̇₂
-
1'
-
</details>

图16-6 例16-2图

同理,为了求  $Y_{12}$ 、 $Y_{22}$ , 把端口  $1-1'$  短路, 即令  $\dot{U}_{1}=0$ , 这时受控源的电流也等于零, 故得

$$
Y _ {1 2} = \frac {\dot {I} _ {1}}{\dot {U} _ {2}} = - Y _ {\mathrm{b}}
$$

$$
Y _ {2 2} = \frac {\dot {I} _ {2}}{\dot {U} _ {2}} = Y _ {\mathrm{b}} + Y _ {\mathrm{c}}
$$

可见,在这种情况下, $Y_{12}\neq Y_{21}$ 。

Y 参数和 Z 参数都可用来描述一个二端口的端口外特性。如果一个二端口的 Y 参数已经确定,一般就可以用式(16-3)求出它的 Z 参数。反之亦然(参阅后面的表 16-1)。

在许多工程实际问题中,往往希望找到一个端口的电流、电压与另一端口的电流、电压之间的直接关系。例如,放大器、滤波器的输入和输出之间的关系;传输线的始端和终端之间的关系。另外,有些二端口并不同时存在阻抗矩阵和导纳矩阵表达式;或者既无阻抗矩阵表达式,又无导纳矩阵表达式。例如理想变压器就属这类二端口。这意味着某些二端口宜用除 Z 参数和 Y 参数以外的其他形式的参数描述其端口外特性。

---

§ 16-2 二端口的方程和参数

399

1. 用 $\mathrm{H}_{2}$ 气相分离的气体，用于化学分析。

为此,可把式(16-1)的第二式化为

$$
\dot {U} _ {1} = - \frac {Y _ {2 2}}{Y _ {2 1}} \dot {U} _ {2} + \frac {1}{Y _ {2 1}} \dot {I} _ {2}
$$

然后把它代入该式中的第一式,经整理后有

$$
\dot {I} _ {1} = \left(Y _ {1 2} - \frac {Y _ {1 1} Y _ {2 2}}{Y _ {2 1}}\right) \dot {U} _ {2} + \frac {Y _ {1 1}}{Y _ {2 1}} \dot {I} _ {2}
$$

把以上两式写成如下形式:

$$
\left. \begin{array}{l} \dot {U} _ {1} = A \dot {U} _ {2} - B \dot {I} _ {2} \\ \dot {I} _ {1} = C \dot {U} _ {2} - D \dot {I} _ {2} \end{array} \right\} ^ {(1)} \tag {16-4}
$$

式中(注意,右方第二项前面用的是负号)

$$
\begin{array}{l l} A = - \frac {Y _ {2 2}}{Y _ {2 1}}, & B = - \frac {1}{Y _ {2 1}} \\ C = Y _ {1 2} - \frac {Y _ {1 1} Y _ {2 2}}{Y _ {2 1}}, & D = - \frac {Y _ {1 1}}{Y _ {2 1}} \end{array} \tag {16-5}
$$

这样，就把端口 $1 - 1^{\prime}$ 的电流 $\dot{I}_1$ 、电压 $\dot{U}_1$ 用端口 $2 - 2^{\prime}$ 的电流 $\dot{I}_2$ 、电压 $\dot{U}_2$ 通过 $A, B, C, D$ 4个参数表示出来了。$A, B, C, D$ 称为二端口的一般参数、传输参数、$T$ 参数或 $A$ 参数。它们表示的具体含义可分别用以下各式说明:

$$
\begin{array}{l} A = \frac {\dot {U} _ {1}}{\dot {U} _ {2}} \Bigg | _ {\dot {I} _ {2} = 0} \\ \mathcal {B} = \frac {\stackrel {\circ} {U} _ {1}}{- \stackrel {\circ} {I} _ {2}} \Bigg | _ {\stackrel {\circ} {U} _ {2} = 0} \\ C = \frac {\dot {I} _ {1}}{\dot {U} _ {2}} \Bigg | _ {\dot {I} _ {2} = 0} \\ D = \frac {\dot {I} _ {1}}{- \dot {I} _ {2}} \Bigg | _ {\dot {U} _ {2} = 0} \\ \end{array}
$$

可见，A 是两个电压的比值，是一个量纲一的量；B 是短路转移阻抗；C 是开路转移导纳；D 是两个电流的比值，也是量纲一的量。A、B、C、D 都具有转移参数性质。

对于不含受控源的无源线性二端口，A、B、C、D 4 个参数中将只有 3 个是独立的，这是因为按式(16-5)并注意到  $Y_{12}=Y_{21}$ ，得

$$
A D - B C = \frac {Y _ {1 1} Y _ {2 2}}{Y _ {2 1} ^ {2}} + \frac {1}{Y _ {2 1}} \frac {Y _ {1 2} Y _ {2 1} - Y _ {1 1} Y _ {2 2}}{Y _ {2 1}} = \frac {Y _ {1 2}}{Y _ {2 1}} = 1
$$

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 有时用 $A_{11}, A_{12}, A_{21}, A_{22}$ 分别表示 $A, B, C, D$。</span></small>

---

400

第十六章 二端口网络

对于对称的二端口，由于  $Y_{11}=Y_{22}$ ，故由式(16-5)，还将有 A=D。

式(16-4)写成矩阵形式时,有

$$
\left[ \begin{array}{c} \dot {U} _ {1} \\ \dot {I} _ {1} \end{array} \right] = \left[ \begin{array}{c c} A & B \\ C & D \end{array} \right] \left[ \begin{array}{c} \dot {U} _ {2} \\ - \dot {I} _ {2} \end{array} \right] = T \left[ \begin{array}{c} \dot {U} _ {2} \\ - \dot {I} _ {2} \end{array} \right]
$$

其中

$$
T \stackrel {\mathrm{def}} {=} \left[ \begin{array}{c c} A & B \\ C & D \end{array} \right]
$$

T 称为 T 参数矩阵, 引用上式时, 要注意式中电流  $\dot{I}_{2}$  前面的负号。

还有一套常用的参数,称为混合参数或 H 参数,用下面一组方程表示:

$$
\left. \begin{array}{l} \dot {U} _ {1} = H _ {1 1} \dot {I} _ {1} + H _ {1 2} \dot {U} _ {2} \\ \dot {I} _ {2} = H _ {2 1} \dot {I} _ {1} + H _ {2 2} \dot {U} _ {2} \end{array} \right\} \tag {16-6}
$$

在晶体管电路中，H 参数获得了广泛的应用。H 参数的具体意义可以分别用下列各式说明:

$$
H _ {1 1} = \frac {\dot {U} _ {1}}{\dot {I} _ {1}} \Bigg | _ {\dot {U} _ {2} = 0}
$$

$$
H _ {1 2} = \frac {\dot {U} _ {1}}{\dot {U} _ {2}} \Bigg | _ {\dot {I} _ {1} = 0}
$$

$$
H _ {2 1} = \frac {\dot {I} _ {2}}{\dot {I} _ {1}} \Bigg | _ {\dot {U} _ {2} = 0}
$$

$$
H _ {2 2} = \frac {\dot {I} _ {2}}{\dot {U} _ {2}} \Bigg | _ {\dot {I} _ {1} = 0}
$$

可见 $H_{11}$ 和 $H_{21}$ 有短路参数的性质，$H_{12}$ 和 $H_{22}$ 有开路参数的性质。不难看出，$H_{11} = \frac{1}{Y_{11}}$，$H_{22} = \frac{1}{Z_{22}}$，$H_{21}$ 为两个电流之间的比值，$H_{12}$ 为两个电压之间的比值。

用矩阵形式表示时,有

$$
\left[ \begin{array}{c} \dot {U} _ {1} \\ \dot {I} _ {2} \end{array} \right] = \left[ \begin{array}{l l} H _ {1 1} & H _ {1 2} \\ H _ {2 1} & H _ {2 2} \end{array} \right] \left[ \begin{array}{c} \dot {I} _ {1} \\ \dot {U} _ {2} \end{array} \right] = \boldsymbol {H} \left[ \begin{array}{c} \dot {I} _ {1} \\ \dot {U} _ {2} \end{array} \right]
$$

其中 H 称为 H 参数矩阵

$$
H \stackrel {\mathrm{def}} {=} \left[ \begin{array}{l l} H _ {1 1} & H _ {1 2} \\ H _ {2 1} & H _ {2 2} \end{array} \right]
$$

对于不含受控源的无源线性二端口，H 参数中只有 3 个是独立的。例如，将前面求得的 Y 参数代入，就可得出图 16-4(a) 所示二端口的 H 参数

---

§ 16-2 二端口的方程和参数

401

$$
H _ {1 1} = \frac {1}{Y _ {\mathrm{a}} + Y _ {\mathrm{b}}}, \quad H _ {1 2} = \frac {Y _ {\mathrm{b}}}{Y _ {\mathrm{a}} + Y _ {\mathrm{b}}}
$$

$$
H _ {2 1} = \frac {- Y _ {\mathrm{b}}}{Y _ {\mathrm{a}} + Y _ {\mathrm{b}}}, \quad H _ {2 2} = Y _ {\mathrm{c}} + \frac {Y _ {\mathrm{a}} Y _ {\mathrm{b}}}{Y _ {\mathrm{a}} + Y _ {\mathrm{b}}}
$$

可见 $H_{21} = -H_{12}$ 。对于对称的二端口，由于 $Y_{11} = Y_{22}$ 或 $Z_{11} = Z_{22}$，则有

$$
H _ {1 1} H _ {2 2} - H _ {1 2} H _ {2 1} = 1
$$

图 16-7 所示为一只晶体管的小信号工作条件下的简化等效电路, 不难根据 H 参数的定义, 求得

$$
H _ {1 1} = \frac {\dot {U} _ {1}}{\dot {I} _ {1}} \Bigg | _ {\dot {U} _ {2} = 0} = R _ {1}, \quad H _ {1 2} = \frac {\dot {U} _ {1}}{\dot {U} _ {2}} \Bigg | _ {\dot {I} _ {1} = 0} = 0
$$

$$
H _ {2 1} = \frac {\dot {I} _ {2}}{\dot {I} _ {1}} \Bigg | _ {\dot {U} _ {2} = 0} = \beta , \quad H _ {2 2} = \frac {\dot {I} _ {2}}{\dot {U} _ {2}} \Bigg | _ {i _ {1} = 0} = \frac {1}{R _ {2}}
$$

![](../../raw/pages_0417-0448/images/page_424_image_9.jpg)

<details>
<summary>text_image</summary>

1
+
î₁
Û₁
R₁
βî₁
R₂
2
+
î₂
Û₂
1'
2'
</details>

图 16-7 晶体管的等效电路

Y 参数、Z 参数、T 参数、H 参数之间的相互转换关系不难根据以上的基本方程推导出来, 表 16-1 总结了这些关系。

表 16-1

<table><tr><td></td><td colspan="2"> $Z$ 参数</td><td colspan="2"> $Y$ 参数</td><td colspan="2"> $H$ 参数</td><td colspan="2"> $T(A)$ 参数</td></tr><tr><td rowspan="3"> $Z$ 参数</td><td colspan="2"></td><td rowspan="2"> $\frac{Y_{22}}{\Delta_Y}$ </td><td rowspan="2"> $-\frac{Y_{12}}{\Delta_Y}$ </td><td rowspan="2"> $\frac{\Delta_H}{H_{22}}$ </td><td rowspan="2"> $\frac{H_{12}}{H_{22}}$ </td><td rowspan="2"> $\frac{A}{C}$ </td><td rowspan="2"> $\frac{\Delta_T}{C}$ </td></tr><tr><td> $Z_{11}$ </td><td> $Z_{12}$ </td></tr><tr><td> $Z_{21}$ </td><td> $Z_{22}$ </td><td> $-\frac{Y_{21}}{\Delta_Y}$ </td><td> $\frac{Y_{11}}{\Delta_Y}$ </td><td> $-\frac{H_{21}}{H_{22}}$ </td><td> $\frac{1}{H_{22}}$ </td><td> $\frac{1}{C}$ </td><td> $\frac{D}{C}$ </td></tr><tr><td rowspan="2"> $Y$ 参数</td><td> $\frac{Z_{22}}{\Delta_Z}$ </td><td> $-\frac{Z_{12}}{\Delta_Z}$ </td><td> $Y_{11}$ </td><td> $Y_{12}$ </td><td> $\frac{1}{H_{11}}$ </td><td> $-\frac{H_{12}}{H_{11}}$ </td><td> $\frac{D}{B}$ </td><td> $-\frac{\Delta_T}{B}$ </td></tr><tr><td> $-\frac{Z_{21}}{\Delta_Z}$ </td><td> $\frac{Z_{11}}{\Delta_Z}$ </td><td> $Y_{21}$ </td><td> $Y_{22}$ </td><td> $\frac{H_{21}}{H_{11}}$ </td><td> $\frac{\Delta_H}{H_{11}}$ </td><td> $-\frac{1}{B}$ </td><td> $\frac{A}{B}$ </td></tr><tr><td rowspan="2"> $H$ 参数</td><td> $\frac{\Delta_Z}{Z_{22}}$ </td><td> $\frac{Z_{12}}{Z_{22}}$ </td><td> $\frac{1}{Y_{11}}$ </td><td> $-\frac{Y_{12}}{Y_{11}}$ </td><td> $H_{11}$ </td><td> $H_{12}$ </td><td> $\frac{B}{D}$ </td><td> $\frac{\Delta_T}{D}$ </td></tr><tr><td> $-\frac{Z_{21}}{Z_{22}}$ </td><td> $\frac{1}{Z_{22}}$ </td><td> $\frac{Y_{21}}{Y_{11}}$ </td><td> $\frac{\Delta_Y}{Y_{11}}$ </td><td> $H_{21}$ </td><td> $H_{22}$ </td><td> $-\frac{1}{D}$ </td><td> $\frac{C}{D}$ </td></tr><tr><td rowspan="2"> $T(A)$ 参数</td><td> $\frac{Z_{11}}{Z_{21}}$ </td><td> $\frac{\Delta_Z}{Z_{21}}$ </td><td> $-\frac{Y_{22}}{Y_{21}}$ </td><td> $-\frac{1}{Y_{21}}$ </td><td> $-\frac{\Delta_H}{H_{21}}$ </td><td> $-\frac{H_{11}}{H_{21}}$ </td><td> $A$ </td><td> $B$ </td></tr><tr><td> $\frac{1}{Z_{21}}$ </td><td> $\frac{Z_{22}}{Z_{21}}$ </td><td> $-\frac{\Delta_Y}{Y_{21}}$ </td><td> $-\frac{Y_{11}}{Y_{21}}$ </td><td> $-\frac{H_{22}}{H_{21}}$ </td><td> $-\frac{1}{H_{21}}$ </td><td> $C$ </td><td> $D$ </td></tr></table>

---

402

第十六章 二端口网络

表中

$$
\begin{array}{l} \Delta_ {Z} = \left| \begin{array}{c c} Z _ {1 1} & Z _ {1 2} \\ Z _ {2 1} & Z _ {2 2} \end{array} \right|, \quad \Delta_ {Y} = \left| \begin{array}{c c} Y _ {1 1} & Y _ {1 2} \\ Y _ {2 1} & Y _ {2 2} \end{array} \right| \\ \Delta_ {H} = \left| \begin{array}{c c} H _ {1 1} & H _ {1 2} \\ H _ {2 1} & H _ {2 2} \end{array} \right|, \quad \Delta_ {T} = \left| \begin{array}{c c} A & B \\ C & D \end{array} \right| \\ \end{array}
$$

二端口一共有6组不同的参数,其余2组分别与H参数和T参数相似,只是把电路方程等号两边的端口变量互换而已,此处不再列举。

## §16-3 二端口的等效电路

任何复杂的由线性 $R, L(M), C$ 元件构成的无源一端口可以用一个等效阻抗表征它的外部特性。同理，任何给定的由线性 $R, L(M), C$ 元件构成的无源二端口的外部性能既然可以用3个参数确定，那么只要找到一个由具有3个阻抗（或导纳）组成的简单二端口，如果这个二端口与给定的二端口的参数分别相等，则这两个二端口的外部特性也就完全相同，即它们是等效的。由3个阻抗（或导纳）组成的二端口只有两种形式，即T形电路和 $\pi$ 形电路，分别如图16-8(a)(b)所示。

![](../../raw/pages_0417-0448/images/page_425_image_8.jpg)

<details>
<summary>text_image</summary>

1
+
i₁
Z₁
i₁
Z₂
i₂
Z₃
i₂
2
+
U₁
-
1'
2'
</details>

(a)

![](../../raw/pages_0417-0448/images/page_425_image_10.jpg)

<details>
<summary>text_image</summary>

1
+
I₁
Y₂
2
+
U̇₁
Y₁
Y₃
U̇₂
1'
-
2'
</details>

(b)

图 16-8 二端口的等效电路

如果给定二端口的 Z 参数,要确定此二端口的等效 T 形电路 [图 16-8(a)] 中的  $Z_{1}$ 、 $Z_{2}$ 、 $Z_{3}$  的值,可先按图中所示回路电流的方向,写出 T 形电路的回路电流方程

$$
\left. \begin{array}{l} \dot {U} _ {1} = Z _ {1} \dot {I} _ {1} + Z _ {2} (\dot {I} _ {1} + \dot {I} _ {2}) \\ \dot {U} _ {2} = Z _ {2} (\dot {I} _ {1} + \dot {I} _ {2}) + Z _ {3} \dot {I} _ {2} \end{array} \right\} \tag {16-7}
$$

而由 Z 参数表示的二端口方程(16-2)中,由于  $Z_{12}=Z_{21}$ ,可以将式(16-2)改写为

$$
\left. \begin{array}{l} \dot {U} _ {1} = (Z _ {1 1} - Z _ {1 2}) \dot {I} _ {1} + Z _ {1 2} (\dot {I} _ {1} + \dot {I} _ {2}) \\ \dot {U} _ {2} = Z _ {1 2} (\dot {I} _ {1} + \dot {I} _ {2}) + (Z _ {2 2} - Z _ {1 2}) \dot {I} _ {2} \end{array} \right\} \tag {16-8}
$$

比较式(16-7)与式(16-8)可知

$$
Z _ {1} = Z _ {1 1} - Z _ {1 2}, Z _ {2} = Z _ {1 2}, Z _ {3} = Z _ {2 2} - Z _ {1 2} \tag {16-9}
$$

如果二端口给定的是 Y 参数, 宜先求出其等效  $\pi$  形电路 [图 16-8(b)] 中的  $Y_{1}$ 、 $Y_{2}$

---

§ 16-4 二端口的转移函数

403

$Y_{3}$  的值。为此针对图 16-8(b) 所示电路, 按求 T 形电路相似的方法可得

$$
Y _ {1} = Y _ {1 1} + Y _ {1 2}, Y _ {2} = - Y _ {1 2} = - Y _ {2 1}, Y _ {3} = Y _ {2 2} + Y _ {2 1} \tag {16-10}
$$

如果给定二端口的其他参数,则可查表16-1,把其他参数变换成Z参数或Y参数,然后再由式(16-9)或式(16-10)求得T形等效电路或 $\pi$ 形等效电路的参数值。例如T形等效电路的 $Z_{1}$ 、 $Z_{2}$ 、 $Z_{3}$ 与T参数之间的关系为

$$
Z _ {1} = \frac {A - 1}{C}, Z _ {2} = \frac {1}{C}, Z _ {3} = \frac {D - 1}{C}
$$

$\pi$  形等效电路的  $Y_{1}$ 、 $Y_{2}$ 、 $Y_{3}$  与 T 参数之间的关系为

$$
Y _ {1} = \frac {D - 1}{B}, Y _ {2} = \frac {1}{B}, Y _ {3} = \frac {A - 1}{B}
$$

对于对称二端口，由于  $Z_{11}=Z_{22}, Y_{11}=Y_{22}, A=D$ ，故它的等效 T 形或  $\pi$  形电路也一定是对称的，这时应有  $Y_{1}=Y_{3}, Z_{1}=Z_{3}$ 。

如果二端口内部含有受控源,那么,二端口的4个参数将是相互独立的。若给定二端口的Z参数,则式(16-2)可写成

$$
\dot {U} _ {1} = Z _ {1 1} \dot {I} _ {1} + Z _ {1 2} \dot {I} _ {2}
$$

$$
\dot {U} _ {2} = Z _ {1 2} \dot {I} _ {1} + Z _ {2 2} \dot {I} _ {2} + (Z _ {2 1} - Z _ {1 2}) \dot {I} _ {1}
$$

这样第 2 个方程右端的最后一项是一个 CCVS, 其等效电路如图 16-9(a) 所示。同理，用 Y 参数表示的含受控电源的二端口可用图 16-9(b) 所示等效电路代替。

![](../../raw/pages_0417-0448/images/page_426_image_13.jpg)

<details>
<summary>text_image</summary>

1
+ 
Ü₁
-
Z₁₁-Z₁₂
Z₁₂-Z₁₂
(Z₂₁-Z₁₂)İ₁
- +
2
+
Ü₂
-
2'
-
</details>

(a)

![](../../raw/pages_0417-0448/images/page_426_image_15.jpg)

<details>
<summary>text_image</summary>

1
+ 
Ü₁
Y₁₁+Y₁₂
- Y₁₂
Y₂₂+Y₁₂
Ü₂
2
+
-
(Y₂₁-Y₁₂)Ü₁
2'
- 
1'
</details>

(b)

图 16-9 含受控电源的二端口的等效电路

## §16-4 二端口的转移函数

以上对二端口的讨论都是按正弦稳态情况考虑的，故用相量法。如果用运算法分析二端口，则上述这些参数都是复变量 $s$ 的函数。二端口的转移函数（传递函数），就是用拉氏变换形式表示的输出电压或电流与输入电压或电流之比（注意，二端口内部必须没有独立电源，也没有由动态元件的非零初值引起的附加电源）。当二端口没有外接负载及输入激励无内阻抗时，二端口称为无端接的。下面分别推导无端接的二端口的电压转移函数 $\frac{U_2(s)}{U_1(s)}$ ，电流转移函数 $\frac{I_2(s)}{I_1(s)}$ ，转移导纳（函数） $\frac{I_2(s)}{U_1(s)}$ 和转移阻抗（函数） $\frac{U_2(s)}{I_1(s)}$ 。

A.  $\frac{1}{2}$

---

404

第十六章 二端口网络

令式(16-2)中的电流 $I_{2}(s)=0$ ,有

$$
U _ {1} (s) = Z _ {1 1} (s) I _ {1} (s)
$$

$$
U _ {2} (s) = Z _ {2 1} (s) I _ {1} (s)
$$

因此电压转移函数为

$$
\frac {U _ {2} (s)}{U _ {1} (s)} = \frac {Z _ {2 1} (s)}{Z _ {1 1} (s)}
$$

或者令式(16-1)中的 $I_{2}=0$ ，有

$$
0 = Y _ {2 1} (s) U _ {1} (s) + Y _ {2 2} (s) U _ {2} (s)
$$

所以电压转移函数为

$$
\frac {U _ {2} (s)}{U _ {1} (s)} = - \frac {Y _ {2 1} (s)}{Y _ {2 2} (s)}
$$

同理,可求得二端口的其余转移函数为

电流转移函数 $\frac{I_2(s)}{I_1(s)} = \frac{Y_{21}(s)}{Y_{11}(s)} = -\frac{Z_{21}(s)}{Z_{22}(s)}\quad [U_2(s) = 0]$

转移导纳 $\frac{I_2(s)}{U_1(s)} = Y_{21}(s)\quad [U_2(s) = 0]$

转移阻抗. $\frac{U_2(s)}{I_1(s)} = Z_{21}(s)\quad [I_2(s) = 0]$

这些转移函数可纯粹用 Y 参数或 Z 参数表示。当然,也可纯粹用  $T(A)$  参数或 H 参数表示。

在实际应用中，二端口的输出端口往往接有负载阻抗 $Z_{\mathrm{L}}$ ，输入端口接有电压源和阻抗 $Z_{\mathrm{s}}$ 的串联组合或电流源和阻抗 $Z_{\mathrm{s}}$ 的并联组合。这种情况下该二端口称为具有“双端接”的二端口。如果只计及 $Z_{\mathrm{L}}$ 或只计及 $Z_{\mathrm{s}}$ ，则称为具有“单端接”的二端口。具有单端接或双端接的二端口的转移函数与端接阻抗有关。

图 16-10 所示为一个输出端接有电阻 R 的二端口。对此二端口，有

$$
I _ {2} (s) = Y _ {2 1} (s) U _ {1} (s) + Y _ {2 2} (s) U _ {2} (s)
$$

$$
U _ {2} (s) = - R I _ {2} (s)
$$

消去  $U_{2}(s)$  后, 得转移导纳

$$
\frac {I _ {2} (s)}{U _ {1} (s)} = \frac {\frac {Y _ {2 1} (s)}{R}}{Y _ {2 2} (s) + \frac {1}{R}}
$$

对此二端口还有

![](../../raw/pages_0417-0448/images/page_427_image_24.jpg)

<details>
<summary>text_image</summary>

1
+
I₁(s)
U₁(s)
-
1'
I₂(s)
2
+
U₂(s)
R
2'
</details>

图16-10 具有端接电阻的二端口

$$
U _ {2} (s) = Z _ {2 1} (s) I _ {1} (s) + Z _ {2 2} (s) I _ {2} (s)
$$

$$
U _ {2} (s) = - R I _ {2} (s)
$$

---

§ 16-4 二端口的转移函数

405

消去  $I_{2}(s)$  后, 得转移阻抗

$$
\frac {U _ {2} (s)}{I _ {1} (s)} = \frac {R Z _ {2 1} (s)}{R + Z _ {2 2} (s)}
$$

如果对此二端口写出如下方程:

$$
\begin{array}{l} I _ {2} (s) = Y _ {2 1} (s) U _ {1} (s) + Y _ {2 2} (s) U _ {2} (s) \\ U _ {1} (s) = Z _ {i 1} (s) I _ {1} (s) + Z _ {1 2} (s) I _ {2} (s) \\ U _ {2} (s) = - R I _ {2} (s) \\ \end{array}
$$

消去  $U_{2}(s)$  和  $U_{1}(s)$  后, 得电流转移函数

$$
\begin{array}{l} \frac {I _ {2} (s)}{I _ {1} (s)} = \frac {Y _ {2 1} (s) Z _ {1 1} (s)}{1 + Y _ {2 2} (s) R - Z _ {1 2} (s) Y _ {2 1} (s)} \\ = \frac {\frac {Y _ {2 1} (s)}{R}}{Y _ {1 1} (s) \left[ \frac {1}{R} + Y _ {2 2} (s) \right] - Y _ {1 2} (s) Y _ {2 1} (s)} \\ \end{array}
$$

如果对此二端口写出如下方程:

$$
U _ {2} (s) = Z _ {2 1} (s) I _ {1} (s) + Z _ {2 2} (s) I _ {2} (s)
$$

$$
I _ {1} (s) = Y _ {1 1} (s) U _ {1} (s) + Y _ {1 2} (s) U _ {2} (s)
$$

$$
U _ {2} (s) = - R I _ {2} (s)
$$

消去  $I_{1}(s)$  和  $I_{2}(s)$  后，得电压转移函数

$$
\begin{array}{l} \frac {U _ {2} (s)}{U _ {1} (s)} = \frac {Z _ {2 1} (s) Y _ {1 1} (s)}{1 + Z _ {2 2} (s) \frac {1}{R} - Z _ {2 1} (s) Y _ {1 2} (s)} \\ = \frac {Z _ {2 1} (s) R}{Z _ {1 1} (s) [ R + Z _ {2 2} (s) ] - Z _ {1 2} (s) Z _ {2 1} (s)} \\ \end{array}
$$

对于双端接二端口,转移函数将与两个端接阻抗有关。图 16-11 所示为这种情况,

其中  $R_{1}$  为输入端的电阻,  $R_{2}$  为输出端的电阻。假定要求的是  $\frac{U_{2}(s)}{U_{\mathrm{a}}(s)}$  [这里应当把  $U_{\mathrm{a}}(s)$  作为输入], 这时有

$$
U _ {1} (s) = U _ {\mathrm{s}} (s) - R _ {1} I _ {1} (s)
$$

$$
U _ {2} (s) = - R _ {2} I _ {2} (s)
$$

把它们代入式(16-2)，得

![](../../raw/pages_0417-0448/images/page_428_image_19.jpg)

<details>
<summary>text_image</summary>

1 I₁(s)
+
R₁
U₁(s)
+
Us(s)
-
1'
I₂(s) 2
+
U₂(s)
R₂
-
2'
</details>

图 16-11 两个端口都有端接电阻影响的情况

$$
\begin{array}{l} U _ {s} (s) - R _ {1} I _ {1} (s) = Z _ {1 1} (s) I _ {1} (s) + Z _ {1 2} (s) I _ {2} (s) \\ - R _ {2} I _ {2} (s) = Z _ {2 1} (s) I _ {1} (s) + Z _ {2 2} (s) I _ {2} (s) \\ \end{array}
$$

解得

---

406

第十六章 二端口网络

$$
I _ {2} (s) = - \frac {U _ {\mathrm{s}} (s) Z _ {2 1} (s)}{\left[ R _ {1} + Z _ {1 1} (s) \right] \left[ R _ {2} + Z _ {2 2} (s) \right] - Z _ {1 2} (s) Z _ {2 1} (s)}
$$

这样有

$$
\frac {U _ {2} (s)}{U _ {\mathrm{s}} (s)} = \frac {- R _ {2} I _ {2} (s)}{U _ {\mathrm{s}} (s)} = \frac {Z _ {2 1} (s) R _ {2}}{\left[ R _ {1} + Z _ {1 1} (s) \right] \left[ R _ {2} + Z _ {2 2} (s) \right] - Z _ {1 2} (s) Z _ {2 1} (s)}
$$

以上介绍了一些转移函数的计算方法。如前所述，二端口常为完成某种功能起着耦合两部分电路的作用。例如，滤波器能让具有某些频率的信号通过，而对另一些频率的信号则加以抑制。这种功能往往是通过转移函数描述或指定的。另一方面，转移函数的极、零点的分布与二端口内部的元件及连接方式等密切相关，而极、零点的分布又决定了电路的特性。所以可以根据转移函数确定二端口内部元件的连接方式及元件值，即所谓电路设计或网络综合。可见二端口的转移函数是一个很重要的概念。

## §16-5 二端口的连接

如果把一个复杂的二端口看成是由若干个简单的二端口按某种方式连接而成，这将使电路分析得到简化。另一方面，在设计和实现一个复杂的二端口时，也可以用简单的二端口作为“积木块”，把它们按一定方式连接成具有所需特性的二端口。一般说来，设计简单的部分电路并加以连接要比直接设计一个复杂的整体电路容易些。因此讨论二端口的连接问题具有重要意义。

二端口可按多种不同方式相互连接,这里主要介绍3种方式:级联(链联)、串联和并联,分别如图16-12(a)(b)(c)所示。在二端口的连接问题上,感兴趣的是复合二端口的参数与部分二端口的参数之间的关系。

![](../../raw/pages_0417-0448/images/page_429_image_10.jpg)

<details>
<summary>text_image</summary>

P₁
P₂
</details>

(a)

![](../../raw/pages_0417-0448/images/page_429_image_12.jpg)

<details>
<summary>text_image</summary>

P₁
P₂
</details>

(b)

![](../../raw/pages_0417-0448/images/page_429_image_14.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph LR
  A["Input 1"] --> B["P1"]
  A --> C["P2"]
  B --> D["Output 1"]
  C --> E["Output 2"]
```
</details>

(c)

图16-12 二端口的连接

当两个无源二端口  $P_{1}$  和  $P_{2}$  按级联方式连接后, 它们构成了一个复合二端口, 如图

---

§ 16-5 二端口的连接

407

16-13 所示。设二端口  $P_{1}$  和  $P_{2}$  的 T 参数分别为

$$
\mathbb {T} ^ {\prime} = \left[ \begin{array}{c c} A ^ {\prime} & B ^ {\prime} \\ C ^ {\prime} & D ^ {\prime} \end{array} \right], \quad \mathbb {T} ^ {\prime \prime} = \left[ \begin{array}{c c} A ^ {\prime \prime} & B ^ {\prime \prime} \\ C ^ {\prime \prime} & D ^ {\prime \prime} \end{array} \right]
$$

则应有

$$
\left[ \begin{array}{c} \dot {U} _ {1} ^ {\prime} \\ \dot {I} _ {1} ^ {\prime} \end{array} \right] = \mathbb {T} ^ {\prime} \left[ \begin{array}{c} \dot {U} _ {2} ^ {\prime} \\ - \dot {I} _ {2} ^ {\prime} \end{array} \right], \quad \left[ \begin{array}{c} \dot {U} _ {1} ^ {\prime \prime} \\ \dot {I} _ {1} ^ {\prime \prime} \end{array} \right] = \mathbb {T} ^ {\prime \prime} \left[ \begin{array}{c} \dot {U} _ {2} ^ {\prime \prime} \\ - \dot {I} _ {2} ^ {\prime \prime} \end{array} \right]
$$

但由于 $\dot{U}_1 = \dot{U}_1'$, $\dot{U}_2' = \dot{U}_1''$, $\dot{U}_2'' = \dot{U}_2$, $\dot{I}_1 = \dot{I}_1'$, $\dot{I}_2' = -\dot{I}_1''$ 及 $\dot{I}_2'' = \dot{I}_2$, 所以有

$$
\left[ \begin{array}{c} \dot {U} _ {1} \\ \dot {I} _ {1} \end{array} \right] = \left[ \begin{array}{c} \dot {U} _ {1} ^ {\prime} \\ \dot {I} _ {1} ^ {\prime} \end{array} \right] = \mathbb {T} ^ {\prime} \left[ \begin{array}{c} \dot {U} _ {2} ^ {\prime} \\ - \dot {I} _ {2} ^ {\prime} \end{array} \right] = \mathbb {T} ^ {\prime} \left[ \begin{array}{c} \dot {U} _ {1} ^ {\prime \prime} \\ \dot {I} _ {1} ^ {\prime \prime} \end{array} \right] = \mathbb {T} ^ {\prime} \mathbb {T} ^ {\prime \prime} \left[ \begin{array}{c} \dot {U} _ {2} ^ {\prime \prime} \\ - \dot {I} _ {2} ^ {\prime \prime} \end{array} \right] = \mathbb {T} ^ {\prime} \mathbb {T} ^ {\prime \prime} \left[ \begin{array}{c} \dot {U} _ {2} \\ - \dot {I} _ {2} \end{array} \right] = \mathbb {T} \left[ \begin{array}{c} \dot {U} _ {2} \\ - \dot {I} _ {2} \end{array} \right]
$$

其中 T 为复合二端口的 T 参数矩阵, 它与二端口  $P_{1}$  和  $P_{2}$  的 T 参数矩阵的关系为

$$
T = T ^ {\prime} T ^ {\prime \prime}
$$

即

$$
\boldsymbol {T} = \left[ \begin{array}{c c} A ^ {\prime} A ^ {\prime \prime} + B ^ {\prime} C ^ {\prime \prime} & A ^ {\prime} B ^ {\prime \prime} + B ^ {\prime} D ^ {\prime \prime} \\ C ^ {\prime} A ^ {\prime \prime} + D ^ {\prime} C ^ {\prime \prime} & C ^ {\prime} B ^ {\prime \prime} + D ^ {\prime} D ^ {\prime \prime} \end{array} \right]
$$

![](../../raw/pages_0417-0448/images/page_430_image_12.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph LR
  Input["Input Voltage: U1 = U1'"] --> P1["P1"]
  P1 --> Output1["Output Voltage: U2'"]
  P1 --> Output2["Output Voltage: U1''"]
  Output1 --> P2["P2"]
  Output2 --> P2
  P2 --> Output3["Output Voltage: U2'' = U2"]
  Output3 --> Output4["Output Current: I2'' = I2"]
```
</details>

图16-13 二端口的级联

当两个二端口  $P_{1}$  和  $P_{2}$  按并联方式连接时，如图 16-14 所示，两个二端口的输入电压和输出电压被分别强制为相同，即  $\dot{U}_{1}^{\prime} = \dot{U}_{1}^{\prime\prime} = \dot{U}_{1}, \dot{U}_{2}^{\prime} = \dot{U}_{2}^{\prime\prime} = \dot{U}_{2}$ 。如果每个二端口的端口条件（即端口上流入一个端子的电流等于流出另一端子的电流）不因并联连接而被破坏，则复合二端口的总端口的电流应为

$$
\dot {I} _ {1} = \dot {I} _ {1} ^ {\prime} + \dot {I} _ {1} ^ {\prime \prime}, \quad \dot {I} _ {2} = \dot {I} _ {2} ^ {\prime} + \dot {I} _ {2} ^ {\prime \prime}
$$

![](../../raw/pages_0417-0448/images/page_430_image_16.jpg)

<details>
<summary>text_image</summary>

I₁
+ 
U̇₁
- 
I₁'
+ 
U̇₁"
- 
I₁'
+ 
I₁''
+ 
I₁''
+ 
P₁
P₂
I₂'
+ 
U̇₂'
- 
I₂'
+ 
U̇₂"
- 
I₂''
+ 
I₂''
- 
U̇₂''
- 
İ₂'
</details>

图16-14 二端口的并联

---

408

第十六章 二端口网络

若设 $\mathbf{P}_1$ 和 $\mathrm{P}_2$ 的 $Y$ 参数分别为

$$
\boldsymbol {Y} ^ {\prime} = \left[ \begin{array}{c c} Y _ {1 1} ^ {\prime} & Y _ {1 2} ^ {\prime} \\ Y _ {2 1} ^ {\prime} & Y _ {2 2} ^ {\prime} \end{array} \right], \quad \boldsymbol {Y} ^ {\prime \prime} = \left[ \begin{array}{c c} Y _ {1 1} ^ {\prime \prime} & Y _ {1 2} ^ {\prime \prime} \\ Y _ {2 1} ^ {\prime \prime} & Y _ {2 2} ^ {\prime \prime} \end{array} \right]
$$

则应有

$$
\left[ \begin{array}{l} \dot {I} _ {1} \\ \dot {I} _ {2} \end{array} \right] = \left[ \begin{array}{l} \dot {I} _ {1} ^ {\prime} \\ \dot {I} _ {2} ^ {\prime} \end{array} \right] + \left[ \begin{array}{l} \dot {I} _ {1} ^ {\prime \prime} \\ \dot {I} _ {2} ^ {\prime \prime} \end{array} \right] = Y ^ {\prime} \left[ \begin{array}{l} \dot {U} _ {1} ^ {\prime} \\ \dot {U} _ {2} ^ {\prime} \end{array} \right] + Y ^ {\prime \prime} \left[ \begin{array}{l} \dot {U} _ {1} ^ {\prime \prime} \\ \dot {U} _ {2} ^ {\prime \prime} \end{array} \right] = (Y ^ {\prime} + Y ^ {\prime \prime}) \left[ \begin{array}{l} \dot {U} _ {1} \\ \dot {U} _ {2} \end{array} \right] = Y \left[ \begin{array}{l} \dot {U} _ {1} \\ \dot {U} _ {2} \end{array} \right]
$$

其中 Y 为复合二端口的 Y 参数矩阵, 它与二端口  $P_{1}$  和  $P_{2}$  的 Y-参数矩阵的关系为

$$
Y = Y ^ {\prime} + Y ^ {\prime \prime}
$$

当两个二端口按串联方式连接时, 只要端口条件仍然成立, 用类似方法, 不难导得复合二端口的 Z 参数矩阵与串联连接的两个二端口的 Z 参数矩阵有如下关系:

$$
\mathbb {Z} = \mathbb {Z} ^ {\prime} + \mathbb {Z} ^ {\prime \prime}
$$

## §16-6 回转器和负阻抗变换器

回转器是一种线性非互易的多端元件, 图 16-15 为它的电路图形符号。理想回转器可视为一个二端口, 它的端口电压、电流关系可用下列方程表示:

$$
\left. \begin{array}{l} u _ {1} = - r i _ {. 2} \\ u _ {2} = r i _ {1} \end{array} \right\}
$$

或写为

$$
\left. \begin{array}{l} i _ {1} = g u _ {2} \\ i _ {2} = - g u _ {1} \end{array} \right\} ^ {(1)}
$$

(16-11)

(16-12)

![](../../raw/pages_0417-0448/images/page_431_image_18.jpg)

图 16-15 回转器

式中的 r 和 g 分别具有电阻和电导的量纲。它们分别称为回转电阻和回转电导，简称回转常数。把上式与理想变压器的关系式对比，就可以明确两者的差别所在。

用矩阵形式表示时,式(16-11)和式(16-12)可分别写为

$$
\left[ \begin{array}{c} u _ {1} \\ u _ {2} \end{array} \right] = \left[ \begin{array}{c c} 0 & - r \\ r & 0 \end{array} \right] \left[ \begin{array}{c} i _ {1} \\ i _ {2} \end{array} \right]
$$

① 式(16-11)和式(16-12)的另一种形式为

$$
\left. \begin{array}{l} u _ {1} = r i _ {2} \\ u _ {2} = - r i _ {1} \end{array} \right\} \tag {$16-11^{\prime$}}
$$

$$
\left. \begin{array}{l} i _ {1} = - g u _ {2} \\ i _ {2} = g u _ {1} \end{array} \right\} \tag {$16-12^{\prime$}}
$$

为了区别这两种情况，习惯上在图16-15所示电路符号图上方加一个箭头。当箭头自左指向右时，它对应式(16-11)或式(16-12)，而自右指向左时则对应式(16-11')或式(16-12')。本书的有关图中略去了这个箭头。

---

§ 16-6 回转器和负阻抗变换器

409

$$
\left[ \begin{array}{c} i _ {1} \\ i _ {2} \end{array} \right] = \left[ \begin{array}{c c} 0 & g \\ - g & 0 \end{array} \right] \left[ \begin{array}{c} u _ {1} \\ u _ {2} \end{array} \right]
$$

可见,回转器的 Z 参数矩阵和 Y 参数矩阵分别为

$$
\mathbb {Z} = \left[ \begin{array}{c c} 0 & - r \\ r & 0 \end{array} \right], \quad \mathbb {Y} = \left[ \begin{array}{c c} 0 & g \\ - g & 0 \end{array} \right]
$$

根据理想回转器的端口方程,即式(16-11),有

$$
u _ {1} i _ {1} + u _ {2} i _ {2} = - r i _ {1} i _ {2} + r i _ {1} i _ {2} = 0
$$

由于图 16-15 中回转器的两个端口的电压电流均取关联参考方向,因此上式表示理想回转器既不消耗功率又不发出功率,它是一个无源线性元件。另外,按式(16-11)或式(16-12),不难证明互易定理不适用于回转器。

从式(16-11)或式(16-12)可以看出,回转器有把一个端口上的电流“回转”为另一端口上的电压或相反过程的性质。正是这一性质,使回转器具有把一个电容回转为一个电感的本领,这在微电子器件中为用易于集成的电容实现难以集成的电感提供了可能性。下面说明回转器的这一功能。

对图 16-16 所示电路, 有  $I_{2}(s) = -s CU_{2}(s)$  (这里采用运算形式), 故按式 (16-11) 或式 (16-12) 可得

$$
U _ {1} (s) = - r I _ {2} (s) = r s C U _ {2} (s) = r ^ {2} s C I _ {1} (s)
$$

或

$$
I _ {1} (s) = g U _ {2} (s) = - g \frac {1}{s C} I _ {2} (s) = g ^ {2} \frac {1}{s C} U _ {1} (s)
$$

于是,输入阻抗为

$$
Z _ {\mathrm{in}} = \frac {U _ {1} (s)}{I _ {1} (s)} = s r ^ {2} C = s \frac {C}{g ^ {2}}
$$

![](../../raw/pages_0417-0448/images/page_432_image_15.jpg)

<details>
<summary>text_image</summary>

I₁(s)
+
U₁(s)
-
I₂(s)
1/sC
+
U₂(s)
-
</details>

图16-16 电感的实现

可见,对于图16-16所示电路,从输入端看,相当于一个电感元件,它的电感值 $L=r^{2}C=\frac{C}{g^{2}}$ 。如果设 $C=1\mu F,r=50k\Omega$ ,则 $L=2500H$ 。换言之,回转器可把 $1\mu F$ 的电容回转成2500H的电感。

负阻抗变换器(简称NIC①)也是一个二端口,它的符号如图16-17(a)所示。它的端口特性可以用下列 $T$ 参数描述[采用运算形式,但为简化起见,略去 $U,I$ 后的“(s)”]

$$
\left[ \begin{array}{l} U _ {1} \\ I _ {1} \end{array} \right] = \left[ \begin{array}{c c} 1 & 0 \\ 0 & - k \end{array} \right] \left[ \begin{array}{l} U _ {2} \\ - I _ {2} \end{array} \right] \tag {16-13a}
$$

或

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① negative impedance converter 的缩写。</span></small>

1. 工程图

---

410

第十六章 二端口网络

$$
\left[ \begin{array}{l} U _ {1} \\ I _ {1} \end{array} \right] = \left[ \begin{array}{l l} - k & 0 \\ 0 & 1 \end{array} \right] \left[ \begin{array}{l} U _ {2} \\ - I _ {2} \end{array} \right] \tag {16-13b}
$$

式中 k 为正实常数。

![](../../raw/pages_0417-0448/images/page_433_image_5.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph LR
  A["1"] -->|I1| B["NIC"]
  C["U1"] -->|I2| D["2"]
  E["-"] -->|I1'| B
  F["1'"] -->|I2'| D
  G["U2"] -->|I2'| D
  H["-"] -->|I2'| D
```
</details>

(a)

![](../../raw/pages_0417-0448/images/page_433_image_7.jpg)

<details>
<summary>text_image</summary>

1
+
I₁
U₁
-
1'
NIC
I₂ 2
+
U₂
Z₂
-
2'
</details>

(b)

图 16-17 负阻抗变换器

从式(16-13a)可以看出,输入电压 $U_{1}$ 经过传输后成为 $U_{2}$,但 $U_{1}$ 等于 $U_{2}$,因此电压的大小和方向均没有改变;但是电流 $I_{1}$ 经传输后变为 $kI_{2}$,换句话说,电流经传输后改变了方向,所以该式定义的NIC称为电流反向型的NIC。

从式(16-13b)可以看出,经传输后电压变为 $-kU_{2}$ ,改变了方向,电流却不改变方向。这种NIC称为电压反向型的NIC。下面说明NIC把正阻抗变为负阻抗的性质。

在端口 2-2' 接上阻抗  $Z_{2}$ ，如图 16-17(b) 所示。从端口 1-1' 看进去的输入阻抗  $Z_{1}$  可计算如下:

设 NIC 为电流反向型, 利用式(16-13a), 得 $^{①}$

$$
Z _ {1} = \frac {U _ {1}}{I _ {1}} = \frac {U _ {2}}{k I _ {2}}
$$

但是  $U_{2}=-Z_{2}I_{2}$  (根据指定的参考方向)，因此

$$
Z _ {1} = - \frac {Z _ {2}}{k}
$$

换句话说, 输入阻抗 $Z_{1}$ 是负载阻抗 $Z_{2}\left(\text{乘以}\frac{1}{k}\right)$ 的负值。所以这个二端口有把一个正阻抗变为负阻抗的本领, 也即当端口 $2-2'$ 接上电阻 $R$、电感 $L$ 或电容 $C$ 时, 则在端口 $1-1'$ 将变为 $-\frac{1}{k} R$、$-\frac{1}{k} L$ 或 $-kC$。

负阻抗变换器为电路设计中实现负 R、L、C 提供了可能性。

![](../../raw/pages_0417-0448/images/page_433_image_19.jpg)

## 思考题

16-1 采用二端口的方程和参数的分析方法可以推广到多端口网络吗？如果可以，哪些方程可以直接推广到多端口网络，哪些方程需要改进后可以推广到多端口网络？
16-2 研究二端口网络,为什么要求二端口内不含独立源,但却可以包含受控源?

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 如 NIC 为电压反向型, 利用式(16-13b) 可得  $Z_{1}=kU_{2}/I_{2}$ 。</span></small>

---

习题

411

16-3 如果二端口网络完全由 $LC$ 元件组成, 它的开路阻抗参数矩阵有何特点?
16-4 为什么用 $Z$ 参数表示的二端口,采用 $\mathrm{T}$ 形等效电路?而用 $Y$ 参数表示的二端口,采用 $\pi$ 形等效电路?
16-5 二端口的连接需符合什么条件？

![](../../raw/pages_0417-0448/images/page_434_image_6.jpg)

## 习题

16-1 求题 16-1 图所示二端口的 Y 参数、Z 参数和 T 参数矩阵。

![](../../raw/pages_0417-0448/images/page_434_image_9.jpg)

<details>
<summary>chemical</summary>

Electrical circuit diagram with inductor L and capacitor C
</details>

(a)

![](../../raw/pages_0417-0448/images/page_434_image_11.jpg)

<details>
<summary>chemical</summary>

Electrical circuit diagram with inductor L and capacitor C
</details>

(b)

题 16-1 图

16-2 求题 16-2 图所示二端口的 Y 参数和 Z 参数矩阵。

![](../../raw/pages_0417-0448/images/page_434_image_15.jpg)

<details>
<summary>text_image</summary>

1 Ω
1 Ω 1 Ω 2
1 Ω
1 Ω
1' 2'
</details>

(a)

![](../../raw/pages_0417-0448/images/page_434_image_17.jpg)

<details>
<summary>text_image</summary>

1
1 Ω
2
2 Ω
2
1'
1 Ω
2'
</details>

(b)

题 16-2 图

16-3 求题 16-3 图所示二端口的 T 参数矩阵。

![](../../raw/pages_0417-0448/images/page_434_image_21.jpg)

(a)

![](../../raw/pages_0417-0448/images/page_434_image_23.jpg)

(b)

![](../../raw/pages_0417-0448/images/page_434_image_25.jpg)

<details>
<summary>text_image</summary>

M
L₁ L₂
</details>

(c)

![](../../raw/pages_0417-0448/images/page_434_image_27.jpg)

(d)

![](../../raw/pages_0417-0448/images/page_434_image_29.jpg)

(e)

题 16-3 图

---

412

第十六章 二端口网络

16-4 求题 16-4 图所示二端口的 Y 参数矩阵。

![](../../raw/pages_0417-0448/images/page_435_image_4.jpg)

题16-4图

16-5—求题 16-5 图所示二端口的混合(H)参数矩阵。

![](../../raw/pages_0417-0448/images/page_435_image_7.jpg)

题16-5图

16-6 已知题 16-6 图所示二端口的 Z 参数矩阵为

$$
\mathbf {Z} = \left[ \begin{array}{c c} 1 0 & 8 \\ 5 & 1 0 \end{array} \right] \Omega
$$

求  $R_{1}$ 、 $R_{2}$ 、 $R_{3}$  和 r 的值。

16-7 已知二端口的 $Y$ 参数矩阵为

$$
\mathbf {Y} = \left[ \begin{array}{c c} 1. 5 & - 1. 2 \\ - 1. 2 & 1. 8 \end{array} \right] \mathrm{S}
$$

求 H 参数矩阵, 并说明该二端口中是否有受控源。

16-8 求题 16-8 图所示二端口的 Z 参数、T 参数矩阵。

![](../../raw/pages_0417-0448/images/page_435_image_16.jpg)

<details>
<summary>text_image</summary>

I₁ + rI₂ - R₁ R₂ I₂
R₃
</details>

题16-6图

![](../../raw/pages_0417-0448/images/page_435_image_18.jpg)

题 16-8 图

16-9 电路如题 16-9 图所示, 已知二端口的 H 参数矩阵为

$$
H = \left[ \begin{array}{l l} 4 0 & 0. 4 \\ 1 0 & 0. 1 \end{array} \right]
$$

---

习题

413

求电压转移函数 $\frac{U_{2}(s)}{U_{1}(s)}$ 。

![](../../raw/pages_0417-0448/images/page_436_image_4.jpg)

<details>
<summary>text_image</summary>

5 Ω
+
Us(s)
-
1
I₁(s)
+
U₁(s)
-
1'
I₂(s)
2
+
U₂(s)
-
2'
10 Ω
</details>

题16-9图

16-10 已知二端口参数矩阵为

(a)  $Z = \begin{bmatrix} \frac{60}{9} & \frac{40}{9} \\ \frac{40}{9} & \frac{100}{9} \end{bmatrix} \Omega;$

(b)  $Y=\begin{bmatrix}5 & -2 \\ 0 & 3\end{bmatrix}$   $S_{o}$

试问二端口是否有受控源,并求它们的等效  $\pi$  形电路。

16-11 求题 16-11 图所示双 T 电路的 Y 参数矩阵。

![](../../raw/pages_0417-0448/images/page_436_image_11.jpg)

<details>
<summary>text_image</summary>

C
R
R
C
R
C
</details>

题 16-11 图

16-12 求题 16-12 图所示二端口的 T 参数矩阵, 设内部二端口  $P_{1}$  的 T 参数矩阵为

$$
\mathcal {T} _ {1} = \left[ \begin{array}{c c} A & B \\ C & D \end{array} \right]
$$

![](../../raw/pages_0417-0448/images/page_436_image_15.jpg)

<details>
<summary>text_image</summary>

1
Y
P₁
1'
2
2'
</details>

(a)

![](../../raw/pages_0417-0448/images/page_436_image_17.jpg)

<details>
<summary>text_image</summary>

1
P₁
Z
2
1'
2'
</details>

(b)

题 16-12 图

---

414

第十六章 二端口网络

16-13 利用题 16-1、题 16-3 的结果, 求出题 16-13 图所示二端口的 T 参数矩阵。设已知  $\omega L_{1}=10\Omega,\frac{1}{\omega C}=20\Omega,\omega L_{2}=\omega L_{3}=8\Omega,\omega M_{23}=4\Omega$ 。

![](../../raw/pages_0417-0448/images/page_437_image_4.jpg)

<details>
<summary>text_image</summary>

1
L₁ L₁
C C L₂ M₂₃ L₃
1'
2
2'
</details>

题-16-13图

16-14 试证明两个回转器级联后[如题16-14图(a)所示], 可等效为一个理想变压器[如题16-14图(b)所示], 并求出变比 $n$ 与两个回转器的回转电导 $g_{1}$ 和 $g_{2}$ 的关系。

![](../../raw/pages_0417-0448/images/page_437_image_7.jpg)

<details>
<summary>text_image</summary>

1
g₁
g₂
2
1'
(a)
2'
→
1
n:1
2
1'
(b)
2'
1'
</details>

题 16-14 图

16-15 试求题 16-15 图所示电路的输入阻抗 $Z_{\mathrm{i}}$ 。已知 $C_{1} = C_{2} = 1 \mathrm{~F}, G_{1} = G_{2} = 1 \mathrm{~S}, g = 2 \mathrm{~S}$ 。

![](../../raw/pages_0417-0448/images/page_437_image_10.jpg)

第十六章部

分习题答案

![](../../raw/pages_0417-0448/images/page_437_image_13.jpg)

<details>
<summary>text_image</summary>

1
G₁
Z₁
C₁'
g
C₂
G₂
2
1'
2'
</details>

题 16-15 图
