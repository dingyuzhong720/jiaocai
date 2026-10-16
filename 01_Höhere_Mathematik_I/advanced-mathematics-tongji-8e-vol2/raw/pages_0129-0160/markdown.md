当 $h, k$ 不同时为零且 $(x_0 + h, y_0 + k) \in U_2(P_0)$ 时，上式右端方括号内的值为正，所以 $\Delta f$ 异于零且与 $f_{xx}$ 同号。又由 $f(x, y)$ 的二阶偏导数的连续性知 $f_{xx}$ 与 $A$ 同号，因此 $\Delta f$ 与 $A$ 同号。所以，当 $A > 0$ 时 $f(x_0, y_0)$ 为极小值，当 $A < 0$ 时 $f(x_0, y_0)$ 为极大值。

(2) 设  $AC-B^{2}<0$  , 即

$$
f _ {x x} (x _ {0}, y _ {0}) f _ {y y} (x _ {0}, y _ {0}) - [ f _ {x y} (x _ {0}, y _ {0}) ] ^ {2} <   0. \tag {9-8}
$$

先假定 $f_{xx}(x_0,y_0) = f_{yy}(x_0,y_0) = 0$ ，于是由(9-8)式可知这时 $f_{xy}(x_0,y_0)\neq 0.$ 现在分别令 $k = h$ 及 $k = -h$ ，则由(9-5)式分别得

$$
\Delta f = \frac {h ^ {2}}{2} [ f _ {x x} (x _ {0} + \theta_ {1} h, y _ {0} + \theta_ {1} h) + 2 f _ {x y} (x _ {0} + \theta_ {1} h, y _ {0} + \theta_ {1} h) + f _ {y y} (x _ {0} + \theta_ {1} h, y _ {0} + \theta_ {1} h) ]
$$

及

$$
\Delta f = \frac {h ^ {2}}{2} \left[ f _ {x x} (x _ {0} + \theta_ {2} h, y _ {0} - \theta_ {2} h) - 2 f _ {x y} (x _ {0} + \theta_ {2} h, y _ {0} - \theta_ {2} h) + f _ {y y} (x _ {0} + \theta_ {2} h, y _ {0} - \theta_ {2} h) \right],
$$

其中 $0 < \theta_{1}, \theta_{2} < 1$. 当 $h \to 0$ 时，以上两式中右端方括号内的式子分别趋于极限

$$
2 f _ {x y} (x _ {0}, y _ {0}) \quad \text {及} \quad - 2 f _ {x y} (x _ {0}, y _ {0}),
$$

从而当 h 充分接近零时,两式中方括号内的值有相反的符号,因此  $\Delta f$  可取不同符号的值,所以  $f(x_{0},y_{0})$  不是极值.

再证 $f_{xx}(x_0,y_0)$ 和 $f_{yy}(x_0,y_0)$ 不同时为零的情形.不妨假定 $f_{xx}(x_0,y_0)\neq 0.$ 先取 $k = 0$ ，于是由(9-5)式得

$$
\Delta f = \frac {1}{2} h ^ {2} f _ {x x} (x _ {0} + \theta h, y _ {0}).
$$

由此看出, 当 h 充分接近零时,  $\Delta f$  与  $f_{xx}(x_{0}, y_{0})$  同号.

但如果取

$$
h = - f _ {x y} (x _ {0}, y _ {0}) s, \quad k = f _ {x x} (x _ {0}, y _ {0}) s, \tag {9-9}
$$

其中 $s$ 是异于零但充分接近零的数, 则可发现, 当 $|s|$ 充分小时, $\Delta f$ 与 $f_{xx}(x_0, y_0)$ 异号. 事实上, 在(9-5)式中将 $h$ 及 $k$ 用(9-9)式给定的值代入, 得

$$
\Delta f = \frac {1}{2} s ^ {2} \left\{\left[ f _ {x y} (x _ {0}, y _ {0}) \right] ^ {2} f _ {x x} (x _ {0} + \theta h, y _ {0} + \theta k) - 2 f _ {x y} (x _ {0}, y _ {0}) f _ {x x} (x _ {0}, y _ {0}) f _ {x y} (x _ {0} + \theta h, y _ {0} + \theta k) + \right.
$$

$$
\left[ f _ {x x} (x _ {0}, y _ {0}) \right] ^ {2} f _ {y y} (x _ {0} + \theta h, y _ {0} + \theta k) \}. \tag {9-10}
$$

上式右端花括号内的式子当 $s \to 0$ 时趋于极限

$$
f _ {x x} (x _ {0}, y _ {0}) \left\{f _ {x x} (x _ {0}, y _ {0}) f _ {y y} (x _ {0}, y _ {0}) - [ f _ {x y} (x _ {0}, y _ {0}) ] ^ {2} \right\}.
$$

由不等式(9-8)，上式花括号内的值为负，因此当 $s$ 充分接近零时，(9-10)式右端（从而 $\Delta f$ ）与 $f_{xx}(x_0,y_0)$ 异号.

以上已经证得:在点 $(x_{0},y_{0})$ 的任意邻近, $\Delta f$ 可取不同符号的值,因此 $f(x_{0},y_{0})$ 不是极值.

## (3) 考察函数

$$
f (x, y) = x ^ {2} + y ^ {4} \quad {\text {及}} \quad g (x, y) = x ^ {2} + y ^ {3}.
$$

容易验证, 这两个函数都以  $(0,0)$  为驻点, 且在点  $(0,0)$  处都满足  $AC-B^{2}=0$ . 但  $f(x,y)$  在点  $(0,0)$  处有极小值, 而  $g(x,y)$  在点  $(0,0)$  处却没有极值.

## \*习题9-9

1. 求函数 $f(x, y) = 2x^{2} - xy - y^{2} - 6x - 3y + 5$ 在点(1, -2)的泰勒公式.
2. 求函数  $f(x,y)=\mathrm{e}^{x}\ln(1+y)$  在点  $(0,0)$  的三阶泰勒公式.
3. 求函数 $f(x, y) = \sin x \sin y$ 在点 $\left(\frac{\pi}{4}, \frac{\pi}{4}\right)$ 的二阶泰勒公式.
4. 利用函数 $f(x, y) = x^y$ 的三阶泰勒公式，计算 1.1^{1.02} 的近似值.
5. 求函数 $f(x, y) = \mathrm{e}^{x + y}$ 在点(0,0)的 $n$ 阶泰勒公式.

## \* 第十节 最小二乘法

许多工程问题,常常需要根据两个变量的几组实验数值——实验数据,来找出这两个变量间的函数关系的近似表达式.通常把这样得到的函数的近似表达式叫做经验公式.经验公式建立以后,就可以把生产或实验中所积累的某些经验,提高到理论上加以分析.下面通过举例介绍常用的一种建立经验公式的方法.

例 1 为了测定刀具的磨损速度,我们做这样的实验:经过一定时间(如每隔1 h),测量一次刀具的厚度,得到一组实验数据如下:

| 顺序编号i | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 时间ti/h | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 |
| 刀具厚度yi/mm | 27.0 | 26.8 | 26.5 | 26.3 | 26.1 | 25.7 | 25.3 | 24.8 |

试根据上面的实验数据建立 y 和 t 之间的经验公式  $y=f(t)$ . 也就是, 要找出一个能使上述数据大体适合的函数关系  $y=f(t)$ .

解 首先,要确定 $f(t)$ 的类型.为此,可按下面的方法处理.在直角坐标系中取t为横坐标,y为纵坐标,描出上述各对数据的对应点,如图9-12所示.从图上可以看出,这些点的连线大致接近于一条直线.于是,就可以认为 $y=f(t)$ 是线性函数,并设

$$
f (t) = a t + b,
$$

其中 a 和 b 是待定常数.

常数 a 和 b 如何确定呢？最理想的情形是选取这样的 a 和 b，能使直线  $y = at + b$  经过图 9-12 中所标出的各点。但在实际上这是不可能的。因为这些点本来就不在同一条直线上。因此，只能要求选取这样的 a, b，使得  $f(t) = at + b$  在  $t_{0}, t_{1}, t_{2}, \cdots, t_{7}$  处的函数值与实验数据  $y_{0}, y_{1}, y_{2}, \cdots, y_{7}$  相差都很小，就是要使偏差

$$
y _ {i} - f (t _ {i}) \quad (i = 0, 1, 2, \dots , 7)
$$

都很小.那么如何达到这一要求呢？能否设法使偏差的和

![](images/page_130_chart_4.jpg)

<details>
<summary>scatter</summary>

| t | y |
| --- | --- |
| 0 | 27 |
| 1 | ~26.8 |
| 2 | ~26.5 |
| 3 | ~26.3 |
| 4 | ~26.1 |
| 5 | ~25.7 |
| 6 | ~25.3 |
| 7 | ~24.8 |
</details>

图9-12

$$
\sum_ {i = 0} ^ {7} [ y _ {i} - f (t _ {i}) ]
$$

很小来保证每个偏差都很小呢？不能，因为偏差有正有负，在求和时，可能互相抵消.为了避免这种情形，可对偏差取绝对值再求和，只要

$$
\sum_ {i = 0} ^ {7} \mid y _ {i} - f (t _ {i}) \mid = \sum_ {i = 0} ^ {7} \mid y _ {i} - (a t _ {i} + b) \mid
$$

很小, 就可以保证每个偏差的绝对值都很小. 但是这个式子中有绝对值符号, 不便于进一步分析讨论. 由于任何实数的平方都是正数或零, 因此可以考虑选取常数 a 与 b, 使

$$
M = \sum_ {i = 0} ^ {7} \left[ y _ {i} - (a t _ {i} + b) \right] ^ {2}
$$

最小来保证每个偏差的绝对值都很小.这种根据偏差的平方和为最小的条件来选择常数 $a$ 与 $b$ 的方法叫做最小二乘法.这种确定常数 $a$ 与 $b$ 的方法是通常所采用的.

现在我们来研究,经验公式  $y=at+b$  中,a 和 b 符合什么条件时,可以使上述的 M 为最小.如果把 M 看成与自变量 a 和 b 相对应的因变量,那么问题就可归结为求函数  $M=M(a,b)$  在哪些点处取得最小值.由第八节中的讨论可知,上述问题可以通过求方程组

$$
\left\{ \begin{array}{l} M _ {a} (a, b) = 0, \\ M _ {b} (a, b) = 0 \end{array} \right.
$$

的解来解决,即令

$$
\left\{ \begin{array}{l} \frac {\partial M}{\partial a} = - 2 \sum_ {i = 0} ^ {7} [ y _ {i} - (a t _ {i} + b) ] t _ {i} = 0, \\ \frac {\partial M}{\partial b} = - 2 \sum_ {i = 0} ^ {7} [ y _ {i} - (a t _ {i} + b) ] = 0, \end{array} \right.
$$

亦即

$$
\left\{ \begin{array}{l} \sum_ {i = 0} ^ {7} t _ {i} \left[ y _ {i} - (a t _ {i} + b) \right] = 0, \\ \sum_ {i = 0} ^ {7} \left[ y _ {i} - (a t _ {i} + b) \right] = 0. \end{array} \right.
$$

将括号内各项进行整理合并,并把未知数 a 和 b 分离出来,便得

$$
\left\{ \begin{array}{l} a \sum_ {i = 0} ^ {7} t _ {i} ^ {2} + b \sum_ {i = 0} ^ {7} t _ {i} = \sum_ {i = 0} ^ {7} y _ {i} t _ {i}, \\ a \sum_ {i = 0} ^ {7} t _ {i} + 8 b = \sum_ {i = 0} ^ {7} y _ {i}. \end{array} \right. \tag {10-1}
$$

下面通过列表来计算 $\sum_{i=0}^{7} t_i$, $\sum_{i=0}^{7} t_i^2$, $\sum_{i=0}^{7} y_i$ 及 $\sum_{i=0}^{7} y_i t_i$.

<table><tr><td></td><td> $t_i$ </td><td> $t_i^2$ </td><td> $y_i$ </td><td> $y_it_i$ </td></tr><tr><td rowspan="8"></td><td>0</td><td>0</td><td>27.0</td><td>0</td></tr><tr><td>1</td><td>1</td><td>26.8</td><td>26.8</td></tr><tr><td>2</td><td>4</td><td>26.5</td><td>53.0</td></tr><tr><td>3</td><td>9</td><td>26.3</td><td>78.9</td></tr><tr><td>4</td><td>16</td><td>26.1</td><td>104.4</td></tr><tr><td>5</td><td>25</td><td>25.7</td><td>128.5</td></tr><tr><td>6</td><td>36</td><td>25.3</td><td>151.8</td></tr><tr><td>7</td><td>49</td><td>24.8</td><td>173.6</td></tr><tr><td>合计</td><td>28</td><td>140</td><td>208.5</td><td>717.0</td></tr></table>

代入方程组(10-1)，得到

$$
\left\{ \begin{array}{l} 1 4 0 a + 2 8 b = 7 1 7, \\ 2 8 a + 8 b = 2 0 8. 5. \end{array} \right.
$$

解此方程组,得到 a=-0.3036, b=27.125. 这样便得到所求经验公式为

$$
y = f (t) = - 0. 3 0 3 6 t + 2 7. 1 2 5. \tag {10-2}
$$

由(10-2)式算出的函数值 $f(t_{i})$ 与实测的 $y_{i}$ 有一定的偏差.现列表比较如下:

| ti/h | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 实测的yi/mm | 27.0 | 26.8 | 26.5 | 26.3 | 26.1 | 25.7 | 25.3 | 24.8 |
| 算得的f(ti)/mm | 27.125 | 26.821 | 26.518 | 26.214 | 25.911 | 25.607 | 25.303 | 25.000 |
| 偏差/mm | -0.125 | -0.021 | -0.018 | 0.086 | 0.189 | 0.093 | -0.003 | -0.200 |

偏差的平方和 M=0.108165，它的算术平方根  $\sqrt{M}=0.329\sqrt{M}$  称为均方误差，它的大小在一定程度上反映了用经验公式来近似表达原来函数关系的近似程度的好坏。

在例 1 中, 按实验数据描出的图形接近于一条直线. 在这种情形下, 就可认为函数关系是线性函数类型的, 从而问题可化为求解一个二元一次方程组, 计算比较方便. 还有一些实际问题, 经验公式的类型不是线性函数, 但可以设法把它化成线性函数的类型来讨论. 举例说明于下:

例 2 在研究某单分子化学反应速度时,得到下列数据:

| i | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| $\tau_{i}$ | 3 | 6 | 9 | 12 | 15 | 18 | 21 | 24 |
| $y_{i}$ | 57.6 | 41.9 | 31.0 | 22.7 | 16.6 | 12.2 | 8.9 | 6.5 |

其中  $\tau$  表示从实验开始算起的时间, y 表示时刻  $\tau$  反应物的量. 试根据上述数据定出经验公式  $y = f(\tau)$ .

解 由化学反应速度的理论知道, $y=f(\tau)$ 应是指数函数 $y=ke^{m\tau}$, 其中 k 和 m 是待定常数. 对这批数据, 先来验证这个结论. 为此, 在 $y=ke^{m\tau}$ 的两端取常用对数, 得

$$
\lg y = (m \lg e) \tau + \lg k.
$$

记 $m\lg e$ 即0.434 $3m = a,\lg k = b$ ，则上式可写为

$$
\lg y = a \tau + b,
$$

于是  $\lg y$  就是  $\tau$  的线性函数. 所以, 把表中各对数据  $(\tau_{i}, y_{i}) (i = 1, 2, \cdots, 8)$  所对应的点描在半对数坐标系上 (半对数坐标系的横轴上各点处所标明的数字与普通的直角坐标系相同, 而纵轴上各点处所标明的数字是这样的, 它的常用对数就是该点到原点的距离), 如图 9-13 所示. 从图上看出, 这些点的连线非常接近于一条直线, 这说明  $y = f(\tau)$  确实可以认为是指数函数.

下面来具体定出 $k$ 与 $m$ 的值.由于

$$
\lg y = a \tau + b,
$$

![](images/page_132_chart_12.jpg)

<details>
<summary>line</summary>

| t | y |
| --- | --- |
| ~3 | 60 |
| ~6 | 42 |
| ~9 | 32 |
| ~12 | 21 |
| ~15 | 13 |
| ~18 | 11 |
| ~21 | 8.5 |
| ~24 | 6 |
</details>

图9-13

所以可仿照例 1 中的讨论,通过求方程组

$$
\left\{ \begin{array}{l} a \sum_ {i = 1} ^ {8} \tau_ {i} ^ {2} + b \sum_ {i = 1} ^ {8} \tau_ {i} = \sum_ {i = 1} ^ {8} \tau_ {i} \lg y _ {i}, \\ a \sum_ {i = 1} ^ {8} \tau_ {i} + 8 b = \sum_ {i = 1} ^ {8} \lg y _ {i} \end{array} \right. \tag {10-3}
$$

的解, 把 a 与 b 确定出来.

下面通过列表来计算  $\sum_{i=1}^{8}\tau_{i},\quad\sum_{i=1}^{8}\tau_{i}^{2},\quad\sum_{i=1}^{8}\lg y_{i}$  及  $\sum_{i=1}^{8}\tau_{i}\lg y_{i}.$

<table><tr><td></td><td> $\tau_{i}$ </td><td> $\tau_{i}^{2}$ </td><td> $y_{i}$ </td><td> $\lg y_{i}$ </td><td> $\tau_{i}\lg y_{i}$ </td></tr><tr><td rowspan="8"></td><td>3</td><td>9</td><td>57.6</td><td>1.7604</td><td>5.2812</td></tr><tr><td>6</td><td>36</td><td>41.9</td><td>1.6222</td><td>9.7332</td></tr><tr><td>9</td><td>81</td><td>31.0</td><td>1.4914</td><td>13.4226</td></tr><tr><td>12</td><td>144</td><td>22.7</td><td>1.3560</td><td>16.2720</td></tr><tr><td>15</td><td>225</td><td>16.6</td><td>1.2201</td><td>18.3015</td></tr><tr><td>18</td><td>324</td><td>12.2</td><td>1.0864</td><td>19.5552</td></tr><tr><td>21</td><td>441</td><td>8.9</td><td>0.9494</td><td>19.9374</td></tr><tr><td>24</td><td>576</td><td>6.5</td><td>0.8129</td><td>19.5096</td></tr><tr><td>合计</td><td>108</td><td>1836</td><td></td><td>10.2988</td><td>122.0127</td></tr></table>

将它们代入方程组(10-3) $\left(\text{其中取}\sum_{i=1}^{8}\lg y_{i}=10.3,\sum_{i=1}^{8}\tau_{i}\lg y_{i}=122\right)$ ，得

$$
\left\{ \begin{array}{l} 1 8 3 6 a + 1 0 8 b = 1 2 2, \\ 1 0 8 a + 8 b = 1 0. 3. \end{array} \right.
$$

解这个方程组,得

$$
\left\{ \begin{array}{l} a = 0. 4 3 4 3 m = - 0. 0 4 5, \\ b = \lg k = 1. 8 9 6 4, \end{array} \right.
$$

所以

$$
m = - 0. 1 0 3 6, \quad k = 7 8. 7 8.
$$

因此所求的经验公式为

$$
y = 7 8. 7 8 \mathrm{e} ^ {- 0. 1 0 3 6 \tau}.
$$

## \*习题9-10

1. 某种合金的含铅量百分比(%)为p,其熔解温度(℃)为 $\theta$ ,由实验测得p与 $\theta$ 的数据如下表:

| p/% | 36.9 | 46.7 | 63.7 | 77.8 | 84.0 | 87.5 |
| --- | --- | --- | --- | --- | --- | --- |
| θ/°C | 181 | 197 | 235 | 270 | 283 | 292 |

试用最小二乘法建立  $\theta$  与 p 之间的经验公式  $\theta = ap + b$ .

2. 已知一组实验数据为 $(x_{1},y_{1}),(x_{2},y_{2}),\cdots,(x_{n},y_{n})$ . 现若假定经验公式是

$$
y = a x ^ {2} + b x + c.
$$

试按最小二乘法建立 a, b, c 应满足的三元一次方程组.

## 总习题九

1. 在“充分”“必要”和“充分必要”三者中选择一个正确的填入下列空格内:

(1) $f(x,y)$ 在点 $(x,y)$ 可微分是 $f(x,y)$ 在该点连续的\_\_\_\_条件, $f(x,y)$ 在点 $(x,y)$ 连续是 $f(x,y)$ 在该点可微分的\_\_\_\_条件;

(2) $z = f(x, y)$ 在点 $(x, y)$ 的偏导数 $\frac{\partial z}{\partial x}$ 及 $\frac{\partial z}{\partial y}$ 存在是 $f(x, y)$ 在该点可微分的 \_\_\_\_ 条件, $z = f(x, y)$ 在点 $(x, y)$ 可微分是函数在该点的偏导数 $\frac{\partial z}{\partial x}$ 及 $\frac{\partial z}{\partial y}$ 存在的 \_\_\_\_ 条件;

(3) $z = f(x, y)$ 的偏导数 $\frac{\partial z}{\partial x}$ 及 $\frac{\partial z}{\partial y}$ 在点 $(x, y)$ 存在且连续是 $f(x, y)$ 在该点可微分的 \_\_\_\_ 条件；

（4）函数 $z = f(x,y)$ 的两个二阶混合偏导数 $\frac{\partial^2z}{\partial x\partial y}$ 及 $\frac{\partial^2z}{\partial y\partial x}$ 在区域 $D$ 内连续是这两个二阶混合偏导数在 $D$ 内相等的 \_\_\_\_ 条件.

2. 下题中给出了四个结论,从中选出一个正确的结论:

设函数 $f(x,y)$ 在点 $(0,0)$ 的某邻域内有定义，且 $f_{x}(0,0) = 3,f_{y}(0,0) = -1$ ，则有（ ）.

(A)  $dz \mid_{(0,0)} = 3dx - dy$
(B) 曲面  $z=f(x,y)$  在点  $(0,0,f(0,0))$  的一个法向量为  $(3,-1,1)$
(C) 曲线  $\left\{\begin{aligned}z=f(x,y),\\ y=0\end{aligned}\right.$  在点  $(0,0,f(0,0))$  的一个切向量为  $(1,0,3)$
(D) 曲线  $\left\{\begin{aligned}z=f(x,y),\\ y=0\end{aligned}\right.$  在点  $(0,0,f(0,0))$  的一个切向量为  $(3,0,1)$

3. 求函数 $f(x, y) = \frac{\sqrt{4x - y^2}}{\ln(1 - x^2 - y^2)}$ 的定义域，并求 $\lim_{(x, y) \to \left(\frac{1}{2}, 0\right)} f(x, y)$.

\* 4. 证明极限 $\lim_{(x,y)\to (0,0)}\frac{xy^2}{x^2 + y^4}$ 不存在.

5. 设 $f(x,y)=\left\{\begin{aligned}\frac{x^{2}y}{x^{2}+y^{2}},&x^{2}+y^{2}\neq0,\\ 0,&x^{2}+y^{2}=0.\end{aligned}\right.$ 求 $f_{x}(x,y)$ 及 $f_{y}(x,y)$.
6. 求下列函数的一阶和二阶偏导数:

(1) $z = \ln (x + y^2)$;

(2) $z = x^{y}$.

7. 求函数 $z = \frac{xy}{x^2 - y^2}$ 当 $x = 2, y = 1, \Delta x = 0.01, \Delta y = 0.03$ 时的全增量和全微分.

\*8. 设 $f(x, y) = \begin{cases} \frac{x^2y^2}{(x^2 + y^2)^{3/2}}, & x^2 + y^2 \neq 0, \\ 0, & x^2 + y^2 = 0. \end{cases}$ 证明:$f(x, y)$ 在点(0,0)处连续且偏导数存在，但不可微分.
9. 设 $u = x^{\gamma}$, 而 $x = \varphi(t)$, $y = \psi(t)$ 都是可微函数, 求 $\frac{\mathrm{d}u}{\mathrm{d}t}$.
10. 设  $z=f(u,v,w)$  具有连续偏导数, 而

$$
u = \eta - \zeta , \quad v = \zeta - \xi , \quad w = \xi - \eta ,
$$

求 $\frac{\partial z}{\partial\xi},\frac{\partial z}{\partial\eta},\frac{\partial z}{\partial\zeta}.$

11. 设 $z = f(u, x, y), u = x\mathrm{e}^y$，其中 $f$ 具有连续的二阶偏导数，求 $\frac{\partial^2 z}{\partial x \partial y}$.

12. 设 $x = \mathrm{e}^{u}\cos v, y = \mathrm{e}^{u}\sin v, z = uv$. 试求 $\frac{\partial z}{\partial x}$ 和 $\frac{\partial z}{\partial y}$.

13. 求螺旋线  $x = a \cos \theta, y = a \sin \theta, z = b \theta$  在点  $(a, 0, 0)$  处的切线及法平面方程.

14. 在曲面 z=xy 上求一点, 使这点处的法线垂直于平面  $x+3y+z+9=0$ , 并写出该法线的方程.

15. 设 $e_l = (\cos \theta, \sin \theta)$, 求函数

$$
f (x, y) = x ^ {2} - x y + y ^ {2}
$$

在点(1,1)沿方向 $l$ 的方向导数，并分别确定角 $\theta$ ，使这个方向导数

(1)有最大值;(2)有最小值;(3)等于0.

16. 求函数 $u = x^{2} + y^{2} + z^{2}$ 在椭球面 $\frac{x^2}{a^2} + \frac{y^2}{b^2} + \frac{z^2}{c^2} = 1$ 上点 $M_0(x_0, y_0, z_0)$ 处沿外法线方向的方向导数.

17. 求平面 $\frac{x}{3} + \frac{y}{4} + \frac{z}{5} = 1$ 和柱面 $x^{2} + y^{2} = 1$ 的交线上与 $xOy$ 面距离最短的点.

18. 在第 I 卦限内作椭球面  $\frac{x^{2}}{a^{2}} + \frac{y^{2}}{b^{2}} + \frac{z^{2}}{c^{2}} = 1$  的切平面, 使该切平面与三坐标面所围成的四面体的体积最小. 求这切平面的切点, 并求此最小体积.

19. 某厂家生产的一种产品同时在两个市场销售, 售价分别为  $p_{1}$  和  $p_{2}$ , 销售量分别为  $q_{1}$  和  $q_{2}$ , 需求函数分别为

$$
q _ {1} = 2 4 - 0. 2 p _ {1}, \quad q _ {2} = 1 0 - 0. 0 5 p _ {2},
$$

总成本函数为

$$
C = 3 5 + 4 0 (q _ {1} + q _ {2}).
$$

试问:厂家如何确定两个市场的售价,能使其获得的总利润最大,最大总利润为多少?

20. 设有一小山, 取它的底面所在的平面为 $xOy$ 坐标面, 其底部所占的闭区域为 $D = \{(x, y) \mid x^2 + y^2 - xy \leqslant 75\}$, 小山的高度函数为 $h = f(x, y) = 75 - x^2 - y^2 + xy$.

（1）设 $M(x_0,y_0)\in D$ ，问 $f(x,y)$ 在该点沿平面上什么方向的方向导数最大，若记此方向导数的最大值为 $g(x_0,y_0)$ ，试写出 $g(x_0,y_0)$ 的表达式；
（2）现欲利用此小山开展攀岩活动，为此需要在山脚找一上山坡度最大的点作为攀岩的起点。也就是说，要在 $D$ 的边界线 $x^{2} + y^{2} - xy = 75$ 上找出(1)中的 $g(x,y)$ 达到最大值的点。试确定攀岩起点的位置。

# 第十章

# 重积分

本章和下一章是多元函数积分学的内容.在一元函数积分学中我们知道,定积分是某种确定形式的和的极限.这种和的极限的概念推广到定义在区域、曲线及曲面上的多元函数的情形,便得到重积分、曲线积分及曲面积分的概念.本章将介绍重积分(包括二重积分和三重积分)的概念、计算方法以及它们的一些应用.

## 第一节 二重积分的概念与性质

## 一、二重积分的概念

## 1. 曲顶柱体的体积

设有一立体,它的底是xOy面上的闭区域 $D^{①}$ ,它的侧面是以D的边界曲线为准

线而母线平行于 $z$ 轴的柱面, 它的顶是曲面 $z = f(x, y)$, 这里 $f(x, y) \geqslant 0$ 且在 $D$ 上连续 (图10-1). 这种立体叫做曲顶柱体. 现在我们来讨论如何定义并计算上述曲顶柱体的体积 $V$.

我们知道,平顶柱体的高是不变的,它的体积可以用公式

$$
\text {体积} = \text {高} \times \text {底面积}
$$

来定义和计算.关于曲顶柱体,当点 $(x,y)$ 在区域D上变动时,高度 $f(x,y)$ 是个变量,因此它的体积不能直接用上式来定义和计算.但如果回忆起第五章中求曲边梯形面积的问题,就不难想到,那里所采用的解决办法,原则上可以用来解决目前的问题.

![](images/page_136_image_11.jpg)

<details>
<summary>text_image</summary>

z
z=f(x,y)
O
y
D
x
</details>

图10-1

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 为简便起见,本章以后除特别说明者外,都假定平面闭区域和空间闭区域是有界的,且平面闭区域有有限面积,空间闭区域有有限体积.</span></small>

首先,用一组曲线网把 D 分成 n 个小闭区域

$$
\Delta \sigma_ {1}, \Delta \sigma_ {2}, \dots , \Delta \sigma_ {n}.
$$

分别以这些小闭区域的边界曲线为准线,作母线平行于z轴的柱面,这些柱面把原来的曲顶柱体分为n个细曲顶柱体.当这些小闭区域的直径①很小时,由于 $f(x,y)$ 连续,对同一个小闭区域来说, $f(x,y)$ 变化很小,这时细曲顶柱体可近似看做平顶柱体.我们

在每个  $\Delta\sigma_{i}$  （这个小闭区域的面积也记作  $\Delta\sigma_{i}$ ）中任取一点  $(\xi_{i},\eta_{i})$ ，以  $f(\xi_{i},\eta_{i})$  为高而底为  $\Delta\sigma_{i}$  的平顶柱体（图10-2）的体积为

$$
f (\xi_ {i}, \eta_ {i}) \Delta \sigma_ {i} \quad (i = 1, 2, \dots , n).
$$

这 $n$ 个平顶柱体体积之和

$$
\sum_ {i = 1} ^ {n} f (\xi_ {i}, \eta_ {i}) \Delta \sigma_ {i}
$$

可以认为是整个曲顶柱体体积的近似值.令 n 个小闭区域的直径中的最大值(记作  $\lambda$ ) 趋于零,取上述和的极限,所得的极限便自然地定义为所论曲顶柱体的体积 V,即

$$
V = \lim _ {\lambda \to 0} \sum_ {i = 1} ^ {n} f (\xi_ {i}, \eta_ {i}) \Delta \sigma_ {i}.
$$

![](images/page_137_image_11.jpg)

<details>
<summary>text_image</summary>

z
z=f(x,y)
O
y
D
Δσᵢ
x
(ξᵢ, ηᵢ)
</details>

图10-2

## 2. 平面薄片的质量

设有一平面薄片占有 $xOy$ 面上的闭区域 $D$, 它在点 $(x, y)$ 处的面密度为 $\mu(x, y)$, 这里 $\mu(x, y) > 0$ 且在 $D$ 上连续. 现在要计算该薄片的质量 $m$.

我们知道,如果薄片是均匀的,即面密度是常数,那么薄片的质量可以用公式

$$
\mathrm{质量} = \mathrm{面密度} \times \mathrm{面积}
$$

来计算. 现在面密度  $\mu(x,y)$  是变量, 薄片的质量就不能直接用上式来计算. 但是上面用来处理曲顶柱体体积问题的方法完全适用于本问题.

由于  $\mu(x,y)$  连续, 把薄片分成许多小块后, 只要小块所占的小闭区域  $\Delta\sigma_{i}$  的直径很小, 这些小块就可以近似地看做均匀薄片. 在  $\Delta\sigma_{i}$  上任取一点  $(\xi_{i},\eta_{i})$ , 则

$$
\mu (\xi_ {i}, \eta_ {i}) \Delta \sigma_ {i} \quad (i = 1, 2, \dots , n)
$$

可看做第 $i$ 个小块的质量的近似值(图10-3).通过求和、取极限，便得出

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 一个闭区域的直径是指区域上任意两点间距离的最大者.</span></small>

$$
m = \lim _ {\lambda \to 0} \sum_ {i = 1} ^ {n} \mu (\xi_ {i}, \eta_ {i}) \Delta \sigma_ {i}.
$$

上面两个问题的实际意义虽然不同,但所求量都归结为同一形式的和的极限.在物理、力学、几何和工程技术中,有许多物理量或几何量都可归结为这一形式的和的极限.因此我们要一般地研究这种和的极限,并抽象出下述二重积分的定义:

![](images/page_138_image_3.jpg)

<details>
<summary>text_image</summary>

(ξᵢ, ηᵢ)
Δσᵢ
O
x
y
</details>

图10-3

定义 设 $f(x, y)$ 是有界闭区域 $D$ 上的有界函数. 将闭区域 $D$ 任意分成 $n$ 个小闭区域

$$
\Delta \sigma_ {1}, \Delta \sigma_ {2}, \dots , \Delta \sigma_ {n},
$$

其中  $\Delta\sigma_{i}$  表示第 i 个小闭区域,也表示它的面积.在每个  $\Delta\sigma_{i}$  上任取一点  $(\xi_{i},\eta_{i})$ ,作乘积  $f(\xi_{i},\eta_{i})\Delta\sigma_{i}\quad(i=1,2,\cdots,n)$ ,并作和  $\sum_{i=1}^{n}f(\xi_{i},\eta_{i})\Delta\sigma_{i}$ .如果当各小闭区域的直径中的最大值  $\lambda\to0$  时,这和的极限总存在,且与闭区域 D 的分法及点  $(\xi_{i},\eta_{i})$  的取法无关,那么称此极限为函数  $f(x,y)$  在闭区域 D 上的二重积分,记作  $\iint_{D}f(x,y)\mathrm{d}\sigma$ ,即

$$
\iint_ {D} f (x, y) \mathrm{d} \sigma = \lim _ {\lambda \to 0} \sum_ {i = 1} ^ {n} f (\xi_ {i}, \eta_ {i}) \Delta \sigma_ {i}. \tag {1-1}
$$

其中 $f(x,y)$ 叫做被积函数, $f(x,y)\mathrm{d}\sigma$ 叫做被积表达式, $\mathrm{d}\sigma$ 叫做面积元素, $x$ 与 $y$ 叫做积分变量, $D$ 叫做积分区域, $\sum_{i=1}^{n} f(\xi_i, \eta_i) \Delta \sigma_i$ 叫做积分和.

在二重积分的定义中对闭区域 $D$ 的划分是任意的, 如果在直角坐标系中用平行于坐标轴的直线网来划分 $D$, 那么除了包含边界点的一些小闭区域外①, 其余的小闭区域都是矩形闭区域. 设矩形闭区域 $\Delta \sigma_{i}$ 的边长为 $\Delta x_{j}$ 和 $\Delta y_{k}$, 则 $\Delta \sigma_{i} = \Delta x_{j} \cdot \Delta y_{k}$. 因此在直角坐标系中, 有时也把面积元素 $\mathrm{d}\sigma$ 记作 $\mathrm{d}x\mathrm{d}y$, 而把二重积分记作

$$
\iint_ {D} f (x, y) \mathrm{d} x \mathrm{d} y,
$$

其中 $\mathrm{d}x\mathrm{d}y$ 叫做直角坐标系中的面积元素.

这里我们要指出, 当 $f(x, y)$ 在闭区域 $D$ 上连续时, (1-1) 式右端的和的极限必定存在, 也就是说, 函数 $f(x, y)$ 在 $D$ 上的二重积分必定存在, 即函数 $f(x, y)$ 在 $D$ 上必定可积. 以后我们总假定函数 $f(x, y)$ 在闭区域 $D$ 上可积.

由二重积分的定义可知,曲顶柱体的体积是函数 $f(x,y)$ 在底D上的二重积分

$$
V = \iint_ {D} f (x, y)   \mathrm{d} \sigma  ,
$$

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 求和的极限时,这些小闭区域所对应的项的和的极限为零,因此这些小闭区域可以略去不计.</span></small>

平面薄片的质量是它的面密度 $\mu (x,y)$ 在薄片所占闭区域 $D$ 上的二重积分

$$
m = \iint_ {D} \mu (x, y) \mathrm{d} \sigma .
$$

一般地, 如果 $f(x, y) \geqslant 0$, 被积函数 $f(x, y)$ 可以解释为曲顶柱体的顶在点 $(x, y)$ 处的竖坐标, 所以二重积分的几何意义就是柱体的体积. 如果 $f(x, y)$ 是负的, 柱体就在 $xOy$ 面的下方, 二重积分的绝对值仍等于柱体的体积, 但二重积分的值是负的. 如果 $f(x, y)$ 在 $D$ 的若干部分区域上是正的, 而在其他的部分区域上是负的, 那么, $f(x, y)$ 在 $D$ 上的二重积分就等于 $xOy$ 面上方的柱体体积减去 $xOy$ 面下方的柱体体积所得之差.

## 二、二重积分的性质

比较定积分与二重积分的定义可以想到,二重积分与定积分有类似的性质,现叙述于下:

性质1 设 $\alpha$ 与 $\beta$ 为常数, 则

$$
\iint_ {D} [ \alpha f (x, y) + \beta g (x, y) ] \mathrm{d} \sigma = \alpha \iint_ {D} f (x, y) \mathrm{d} \sigma + \beta \iint_ {D} g (x, y) \mathrm{d} \sigma .
$$

性质 2 如果闭区域 D 被有限条曲线分为有限个部分闭区域,那么在 D 上的二重积分等于在各部分闭区域上的二重积分的和.

例如 $D$ 分为两个闭区域 $D_{1}$ 与 $D_{2}$, 则

$$
\iint_ {D} f (x, y) \mathrm{d} \sigma = \iint_ {D _ {1}} f (x, y) \mathrm{d} \sigma + \iint_ {D _ {2}} f (x, y) \mathrm{d} \sigma .
$$

这个性质表示二重积分对于积分区域具有可加性.

性质3 如果在 $D$ 上, $f(x,y) = 1, \sigma$ 为 $D$ 的面积, 那么

$$
\sigma = \iint_ {D} 1 \cdot \mathrm{d} \sigma = \iint_ {D} \mathrm{d} \sigma.
$$

这性质的几何意义是很明显的,因为高为1的平顶柱体的体积在数值上就等于柱体的底面积.

性质4 如果在 $D$ 上，$f(x,y) \leqslant g(x,y)$，那么有

$$
\iint_ {D} f (x, y) \mathrm{d} \sigma \leqslant \iint_ {D} g (x, y) \mathrm{d} \sigma .
$$

特殊地,由于

$$
- \left| f (x, y) \right| \leqslant f (x, y) \leqslant \left| f (x, y) \right|,
$$

又有

$$
\left| \iint_ {D} f (x, y)   \mathrm{d} \sigma \right| \leqslant \iint_ {D} | f (x, y) |   \mathrm{d} \sigma.
$$

性质5 设 $M$ 和 $m$ 分别是 $f(x, y)$ 在闭区域 $D$ 上的最大值和最小值, $\sigma$ 是 $D$ 的面积, 则有

$$
m \sigma \leqslant \iint_ {D} f (x, y)   \mathrm{d} \sigma \leqslant M \sigma.
$$

上述不等式是对于二重积分估值的不等式. 因为 $m \leqslant f(x, y) \leqslant M$, 所以由性质 4 有

$$
\iint_ {D} m \mathrm{d} \sigma \leqslant \iint_ {D} f (x, y) \mathrm{d} \sigma \leqslant \iint_ {D} M \mathrm{d} \sigma ,
$$

再应用性质 1 和性质 3, 便得此估值不等式.

性质6(二重积分的中值定理) 设函数 $f(x, y)$ 在闭区域 $D$ 上连续, $\sigma$ 是 $D$ 的面积, 则在 $D$ 上至少存在一点 $(\xi, \eta)$, 使得

$$
\iint_ {D} f (x, y) \mathrm{d} \sigma = f (\xi , \eta) \sigma .
$$

证 显然 $\sigma \neq 0$ .把性质5中不等式各除以 $\sigma$ ，有

$$
m \leqslant \frac {1}{\sigma} \iint_ {D} f (x, y)   \mathrm{d} \sigma \leqslant M.
$$

这就是说,确定的数值 $\frac{1}{\sigma}\iint_{D}f(x,y)\mathrm{d}\sigma$ 是介于函数 $f(x,y)$ 的最大值M与最小值m之间的.根据在闭区域上连续函数的介值定理,在D上至少存在一点 $(\xi,\eta)$ ,使得函数在该点的值与这个确定的数值相等,即

$$
\frac {1}{\sigma} \iint_ {D} f (x, y) \mathrm{d} \sigma = f (\xi , \eta).
$$

上式两端各乘  $\sigma$ ，就得所需要证明的公式.

例1 估计二重积分 $I = \iint_{D} (x + y + 10) \, \mathrm{d}\sigma$ 的值，其中 $D = \{(x, y) | (x - 2)^2 + (y - 1)^2 \leqslant 2\}$.

解 按照二重积分的性质 5, 估计二重积分的值, 关键是要确定被积函数 $f(x, y)$ 在积分区域 $D$ 上的最大值和最小值. 本例中, 被积函数 $f(x, y) = x + y + 10$ 的图形是一张平面. 容易知道, 它在 $D$ 上的最大值、最小值均在 $D$ 的边界上取得, 所以, 只需考虑它在 $D$ 的边界上的取值情形.

$D$ 的边界曲线 $L$ 的参数方程为

$$
\left\{ \begin{array}{l l} x = 2 + \sqrt {2} \cos t, \\ y = 1 + \sqrt {2} \sin t, \end{array} \right. \quad t \in [ 0, 2 \pi ].
$$

因此在 $L$ 上, 有

$$
f (x, y) = \sqrt {2} (\cos t + \sin t) + 1 3 = 2 \sin \left(t + \frac {\pi}{4}\right) + 1 3,
$$

![](images/page_140_image_19.jpg)

例题精讲

10-1

便得

$$
1 1 \leqslant f (x, y) \leqslant 1 5.
$$

区域 D 的面积  $\sigma=2\pi$ ，于是

$$
2 2 \pi \leqslant I \leqslant 3 0 \pi .
$$

例2 设 $f(x, y)$ 在闭区域 $D$ 上连续，$D$ 关于 $x$ 轴和 $y$ 轴均对称，记 $D_{1} = \{(x, y) | (x, y) \in D, x \geqslant 0, y \geqslant 0\}$，二重积分 $I = \iint_{D} f(x, y) \, \mathrm{d}\sigma = 4 \iint_{D_{1}} f(x, y) \, \mathrm{d}\sigma$ 成立的条件是下列条件中的哪一个？

(1) $f(x,y)$ 关于 $x$ 是奇函数, 关于 $y$ 是偶函数, 即

$$
f (- x, y) = - f (x, y), \quad f (x, - y) = f (x, y), \quad (x, y) \in D;
$$

(2) $f(-x,y)=f(x,y),f(x,-y)=f(x,y),(x,y)\in D;$
(3)  $f(-x,y)=f(x,y)$ ,  $f(x,-y)=-f(x,y)$ ,  $(x,y)\in D;$
(4) $f(-x, y) = -f(x, y)$, $f(x, -y) = -f(x, y)$, $(x, y) \in D$.

解（2）中的函数 $f(x,y)$ 关于 $x$ 、关于 $y$ 均是偶函数，而积分区域 $D$ 关于 $y$ 轴、$x$ 轴均对称，由二重积分对于积分区域的可加性和几何意义，可知题中给出的积分等式成立，其余三种条件下，积分等式均不成立。例如条件(1)和(4)，$f(x,y)$ 关于 $x$ 是奇函数，而积分区域 $D$ 关于 $y$ 轴对称，即知 $I = 0$；同理，条件(3)，$f(x,y)$ 关于 $y$ 是奇函数，而积分区域 $D$ 关于 $x$ 轴对称，即知 $I = 0$。

## 习题10-1

1. 设有一平面薄板(不计其厚度)占有 xOy 面上的闭区域 D, 薄板上分布有面密度为  $\mu = \mu(x, y)$  的电荷, 且  $\mu(x, y)$  在 D 上连续, 试用二重积分表达该薄板上的全部电荷 Q.
2. 设 $I_{1} = \iint_{D_{1}} (x^{2} + y^{2})^{3} \mathrm{d}\sigma$，其中 $D_{1} = \{(x, y) | -1 \leqslant x \leqslant 1, -2 \leqslant y \leqslant 2\}$; 又 $I_{2} = \iint_{D_{2}} (x^{2} + y^{2})^{3} \mathrm{d}\sigma$，其中 $D_{2} = \{(x, y) | 0 \leqslant x \leqslant 1, 0 \leqslant y \leqslant 2\}$. 试利用二重积分的几何意义说明 $I_{1}$ 与 $I_{2}$ 之间的关系.

3. 利用二重积分定义证明:

(1) $\iint_{D} \mathrm{d}\sigma = \sigma$ （其中 $\sigma$ 为 $D$ 的面积）；
(2) $\iint_{D}kf(x,y)\mathrm{d}\sigma=k\iint_{D}f(x,y)\mathrm{d}\sigma$ （其中k为常数）；
(3) $\iint_{D} f(x, y) \mathrm{d}\sigma = \iint_{D_1} f(x, y) \mathrm{d}\sigma + \iint_{D_2} f(x, y) \mathrm{d}\sigma$，其中 $D = D_1 \cup D_2, D_1, D_2$ 为两个无公共内点的闭区域.

4. 试确定积分区域 D, 使二重积分  $\iint_{D}(1-2x^{2}-y^{2})\mathrm{d}x\mathrm{d}y$  达到最大值.

5. 根据二重积分的性质, 比较下列积分的大小:

(1) $\iint_{D}(x + y)^{2}\mathrm{d}\sigma$ 与 $\iint_{D}(x + y)^{3}\mathrm{d}\sigma$ ，其中积分区域 $D$ 是由 $x$ 轴、$y$ 轴与直线 $x + y = 1$ 所围成；
(2) $\iint_{D}(x + y)^{2}\mathrm{d}\sigma$ 与 $\iint_{D}(x + y)^3\mathrm{d}\sigma$ ，其中积分区域 $D$ 是由圆周 $(x - 2)^{2} + (y - 1)^{2} = 2$ 所围成；
(3) $\iint_{D} \ln (x + y) \, \mathrm{d}\sigma$ 与 $\iint_{D} [\ln (x + y)]^2 \, \mathrm{d}\sigma$, 其中 $D$ 是三角形闭区域, 三顶点分别为 $(1,0),(1,1),(2,0)$;
(4) $\iint_{D} \ln(x + y) \, \mathrm{d}\sigma$ 与 $\iint_{D} [\ln(x + y)]^2 \, \mathrm{d}\sigma$, 其中 $D = \{(x, y) \mid 3 \leqslant x \leqslant 5, 0 \leqslant y \leqslant 1\}$.

6. 计算 $\iint_{D}(2 + y\cos x + xy\sin y)\mathrm{d}\sigma$ ，其中 $D = \{(x,y)\left|x^{2} + y^{2}\leqslant 1\}$

7. 利用二重积分的性质估计下列积分的值:

(1) $I = \iint_{D} xy(x + y) \, \mathrm{d}\sigma$，其中 $D = \{(x, y) \mid 0 \leqslant x \leqslant 1, 0 \leqslant y \leqslant 1\}$;
(2) $I = \iint_{D} \sin^{2} x \sin^{2} y \, \mathrm{d}\sigma$，其中 $D = \{(x, y) \mid 0 \leqslant x \leqslant \pi, 0 \leqslant y \leqslant \pi\}$;
(3) $I = \iint_{D}(x + y + 1)\mathrm{d}\sigma$，其中 $D = \{(x,y) \mid 0 \leqslant x \leqslant 1, 0 \leqslant y \leqslant 2\}$;
(4) $I = \iint_{D} (x^{2} + 4y^{2} + 9)\mathrm{d}\sigma$, 其中 $D = \{(x, y) \mid x^{2} + y^{2} \leqslant 4\}$.

## 第二节 二重积分的计算法

按照二重积分的定义来计算二重积分,对少数特别简单的被积函数和积分区域来说是可行的,但对一般的函数和区域来说,这不是一种切实可行的方法.本节介绍一种计算二重积分的方法,这种方法是把二重积分化为两次定积分来计算.

## 一、利用直角坐标计算二重积分

下面用几何观点来讨论二重积分 $\iint_{D} f(x, y) \, \mathrm{d}\sigma$ 的计算问题. 在讨论中我们假定 $f(x, y) \geqslant 0$.

设积分区域 $D$ 可以用不等式

$$
\varphi_ {1} (x) \leqslant y \leqslant \varphi_ {2} (x), \quad a \leqslant x \leqslant b
$$

来表示(图10-4)，其中函数 $\varphi_1(x),\varphi_2(x)$ 在区间 $[a,b]$ 上连续.

按照二重积分的几何意义,二重积分  $\iint_{D} f(x, y) \, d\sigma$  的值等于以 D 为底,曲面  $z = f(x, y)$  为顶的曲顶柱体(图 10-5)的体积.下面我们应用第六章中计算“平行截面面积为已知的立体的体积”的方法来计算这个曲顶柱体的体积.

![](images/page_143_image_2.jpg)

图10-4

![](images/page_143_image_4.jpg)

<details>
<summary>text_image</summary>

z
z=f(x,y)
A(x₀)
y=φ₂(x)
y=φ₁(x)
O
a
x₀
b
x
</details>

图10-5

先计算截面面积.为此,在区间 $[a,b]$ 上任意取定一点 $x_{0}$ ,作平行于yOz面的平面 $x=x_{0}$ .这平面截曲顶柱体所得的截面是一个以区间 $\left[\varphi_{1}(x_{0}),\varphi_{2}(x_{0})\right]$ 为底、曲线 $z=f(x_{0},y)$ 为曲边的曲边梯形(图10-5中阴影部分),所以这截面的面积为

$$
A (x _ {0}) = \int_ {\varphi_ {1} (x _ {0})} ^ {\varphi_ {2} (x _ {0})} f (x _ {0}, y) \mathrm{d} y.
$$

一般地, 过区间  $[a, b]$  上任一点 x 且平行于 yOz 面的平面截曲顶柱体所得截面的面积为

$$
A (x) = \int_ {\varphi_ {1} (x)} ^ {\varphi_ {2} (x)} f (x, y)   \mathrm{d} y.
$$

于是,应用计算平行截面面积为已知的立体体积的方法,得曲顶柱体体积为

$$
V = \int_ {a} ^ {b} A (x)   \mathrm{d} x = \int_ {a} ^ {b} \left[ \int_ {\varphi_ {1} (x)} ^ {\varphi_ {2} (x)} f (x, y)   \mathrm{d} y \right]   \mathrm{d} x.
$$

这个体积也就是所求二重积分的值,从而有等式

$$
\iint_ {D} f (x, y) \mathrm{d} \sigma = \int_ {a} ^ {b} \left[ \int_ {\varphi_ {1} (x)} ^ {\varphi_ {2} (x)} f (x, y) \mathrm{d} y \right] \mathrm{d} x. \tag {2-1}
$$

上式右端的积分叫做先对 $y$ 、后对 $x$ 的二次积分. 就是说, 先把 $x$ 看做常数, 把 $f(x, y)$ 只看做 $y$ 的函数, 并对 $y$ 计算从 $\varphi_1(x)$ 到 $\varphi_2(x)$ 的定积分; 然后把算得的结果 (是 $x$ 的函数) 再对 $x$ 计算在区间 $[a, b]$ 上的定积分. 这个先对 $y$ 、后对 $x$ 的二次积分也常记作

$$
\int_ {a} ^ {b} \mathrm{d} x \int_ {\varphi_ {1} (x)} ^ {\varphi_ {2} (x)} f (x, y) \mathrm{d} y.
$$

因此,等式(2-1)也写成

$$
\iint_ {D} f (x, y) \mathrm{d} \sigma = \int_ {a} ^ {b} \mathrm{d} x \int_ {\varphi_ {1} (x)} ^ {\varphi_ {2} (x)} f (x, y) \mathrm{d} y, \tag {$2-1^{\prime$}}
$$

这就是把二重积分化为先对 y、后对 x 的二次积分的公式.

在上述讨论中,我们假定 $f(x,y)\geqslant0$ ,但实际上公式(2-1)的成立并不受此条件限制.

类似地,如果积分区域 D 可以用不等式

$$
\psi_ {1} (y) \leqslant x \leqslant \psi_ {2} (y), \quad c \leqslant y \leqslant d
$$

来表示(图 10-6)，其中函数  $\psi_{1}(y)$ ,  $\psi_{2}(y)$  在区间  $[c,d]$  上连续，那么就有

$$
\iint_ {D} f (x, y) \mathrm{d} \sigma = \int_ {c} ^ {d} \left[ \int_ {\psi_ {1} (y)} ^ {\psi_ {2} (y)} f (x, y) \mathrm{d} x \right] \mathrm{d} y. \tag {2-2}
$$

上式右端的积分叫做先对 $x$ 、后对 $y$ 的二次积分，这个积分也常记作

$$
\int_ {c} ^ {d} \mathrm{d} y \int_ {\psi_ {1} (y)} ^ {\psi_ {2} (y)} f (x, y) \mathrm{d} x.
$$

因此,等式(2-2)也写成

$$
\iint_ {D} f (x, y) \mathrm{d} \sigma = \int_ {c} ^ {d} \mathrm{d} y \int_ {\psi_ {1} (y)} ^ {\psi_ {2} (y)} f (x, y) \mathrm{d} x, \tag {$2-2^{\prime$}}
$$

这就是把二重积分化为先对 x、后对 y 的二次积分的公式.

![](images/page_144_image_10.jpg)

图10-6

以后我们称图10-4所示的积分区域为 $X$ 型区域，图10-6所示的积分区域为 $Y$ 型区域.应用公式(2-1)时，积分区域必须是 $X$ 型区域，$X$ 型区域 $D$ 的特点是:穿过 $D$ 内部且平行于 $y$ 轴的直线与 $D$ 的边界相交不多于两点；而用公式(2-2)时，积分区域必须是 $Y$ 型区域，$Y$ 型区域 $D$ 的特点是:穿过 $D$ 内部且平行于 $x$ 轴的直线与 $D$ 的边界相交不多于两点.如果积分区域 $D$ 如图10-7那样，既有一部分使穿过 $D$ 内部且平行于 $y$ 轴的直线与 $D$ 的边界相交多于两点，又有一部分使穿过 $D$ 内部且平行于 $x$ 轴的直线与 $D$ 的边界相交多于两点，那么 $D$ 既不是 $X$ 型区域，又不是 $Y$ 型区域.对于这种情形，可以把 $D$ 分成几部分，使每个部分是 $X$ 型区域或是 $Y$ 型区域.例如，在图10-7中，把 $D$ 分成三部分，它们都是 $X$ 型区域，从而在这三部分上的二重积分都可应用公式(2-1).各部分上的二重积分求得后，根据二重积分的性质2,它们的和就是在 $D$ 上的二重积分.

如果积分区域 $D$ 既是 $X$ 型的，可用不等式 $\varphi_{1}(x) \leqslant y \leqslant \varphi_{2}(x), a \leqslant x \leqslant b$ 表示，又是 $Y$ 型的，可用不等式 $\psi_{1}(y) \leqslant x \leqslant \psi_{2}(y), c \leqslant y \leqslant d$ 表示（图10-8），那么由公式(2-1')及(2-2')就得

$$
\int_ {a} ^ {b} \mathrm{d} x \int_ {\varphi_ {1} (x)} ^ {\varphi_ {2} (x)} f (x, y) \mathrm{d} y = \int_ {c} ^ {d} \mathrm{d} y \int_ {\psi_ {1} (y)} ^ {\psi_ {2} (y)} f (x, y) \mathrm{d} x. \tag {2-3}
$$

上式表明, 这两个不同次序的二次积分相等, 因为它们都等于同一个二重积分

$$
\iint_ {D} f (x, y) \mathrm{d} \sigma .
$$

将二重积分化为二次积分时,确定积分限是一个关键.积分限是根据积分区域D来确定的,先画出积分区域D的图形.假如积分区域D是X型的,如图10-9所示,在区间 $[a,b]$ 上任意取定一个x值,积分区域上以这个x值为横坐标的点在一段直线上,这段直线平行于y轴,该线段上点的纵坐标从 $\varphi_{1}(x)$ 变到 $\varphi_{2}(x)$ ,这就是公式(2-1)中先把x看做常量而对y积分时的下限和上限.因为上面的x值是在 $[a,b]$ 上任意取定的,所以再把x看做变量而对x积分时,积分区间就是 $[a,b]$ .

![](images/page_145_image_5.jpg)

<details>
<summary>text_image</summary>

y
I
II
III
O
x
</details>

图10-7

![](images/page_145_image_7.jpg)

<details>
<summary>text_image</summary>

y
d
D
c
O
a
b
x
</details>

图10-8

![](images/page_145_image_9.jpg)

<details>
<summary>text_image</summary>

y
φ₂(x)
D
φ₁(x)
O a x b x
</details>

图10-9

例 1 计算  $\iint_{D} xy \, d\sigma$ ，其中 D 是由直线 y = 1, x = 2 及 y = x 所围成的闭区域.

解法一 首先画出积分区域 $D$ （图10-10）. $D$ 是 $X$ 型的，$D$ 上的点的横坐标的变动范围是区间[1,2].在区间[1,2]上任意取定一个 $x$ 值，则 $D$ 上以这个 $x$ 值为横坐标的点在一段直线上，这段直线平行于 $y$ 轴，该线段上点的纵坐标从 $y = 1$ 变到 $y = x$.利用公式(2-1)得

$$
\iint_ {D} x y \mathrm{d} \sigma = \int_ {1} ^ {2} \left[ \int_ {1} ^ {x} x y \mathrm{d} y \right] \mathrm{d} x = \int_ {1} ^ {2} \left[ x \cdot \frac {y ^ {2}}{2} \right] _ {1} ^ {x} \mathrm{d} x = \int_ {1} ^ {2} \left(\frac {x ^ {3}}{2} - \frac {x}{2}\right) \mathrm{d} x = \left[ \frac {x ^ {4}}{8} - \frac {x ^ {2}}{4} \right] _ {1} ^ {2} = \frac {9}{8}.
$$

解法二 如图10-11, 积分区域 $D$ 是 $Y$ 型的, $D$ 上的点的纵坐标的变动范围是区间[1,2]. 在区间[1,2]上任意取定一个 $y$ 值, 则 $D$ 上以这个 $y$ 值为纵坐标的点在一段直线上, 这段直线平行于 $x$ 轴, 该线段上点的横坐标从 $x = y$ 变到 $x = 2$. 于是, 利用公式(2-2)得

$$
\iint_ {D} x y \mathrm{d} \sigma = \int_ {1} ^ {2} \left[ \int_ {y} ^ {2} x y \mathrm{d} x \right] \mathrm{d} y = \int_ {1} ^ {2} \left[ y \cdot \frac {x ^ {2}}{2} \right] _ {y} ^ {2} \mathrm{d} y = \int_ {1} ^ {2} \left(2 y - \frac {y ^ {3}}{2}\right) \mathrm{d} y = \left[ y ^ {2} - \frac {y ^ {4}}{8} \right] _ {1} ^ {2} = \frac {9}{8}.
$$

![](images/page_146_image_1.jpg)

<details>
<summary>text_image</summary>

y
y=x
D
y=1
O 1 x 2 x
</details>

图 10-10

![](images/page_146_image_3.jpg)

<details>
<summary>text_image</summary>

y
2
x=y
y
D
x=2
1
O
x
</details>

图10-11

例2 计算 $\iint_{D} y \sqrt{1 + x^2 - y^2} \, \mathrm{d}\sigma$，其中 $D$ 是由直线 $y = x, x = -1$ 和 $y = 1$ 所围成的闭区域.

解 画出积分区域 $D$ 如图10-12所示. $D$ 既是 $X$ 型的, 又是 $Y$ 型的. 若利用公式(2-1), 得

$$
\begin{array}{l} \iint_ {D} y \sqrt {1 + x ^ {2} - y ^ {2}} \mathrm{d} \sigma = \int_ {- 1} ^ {1} \left[ \int_ {x} ^ {1} y \sqrt {1 + x ^ {2} - y ^ {2}} \mathrm{d} y \right] \mathrm{d} x = - \frac {1}{3} \int_ {- 1} ^ {1} \left[ (1 + x ^ {2} - y ^ {2}) ^ {\frac {3}{2}} \right] _ {x} ^ {1} \mathrm{d} x \\ = - \frac {1}{3} \int_ {- 1} ^ {1} (| x | ^ {3} - 1) \mathrm{d} x = - \frac {2}{3} \int_ {0} ^ {1} (x ^ {3} - 1) \mathrm{d} x = \frac {1}{2}. \\ \end{array}
$$

若利用公式(2-2)(图 10-13)，就有

$$
\iint_ {D} y \sqrt {1 + x ^ {2} - y ^ {2}} \mathrm{d} \sigma = \int_ {- 1} ^ {1} y \left[ \int_ {- 1} ^ {y} \sqrt {1 + x ^ {2} - y ^ {2}} \mathrm{d} x \right] \mathrm{d} y,
$$

其中关于 $x$ 的积分计算比较麻烦. 所以这里用公式(2-1)计算较为方便.

![](images/page_146_image_11.jpg)

<details>
<summary>text_image</summary>

y
1
D
y=x
-1 x O 1 x
</details>

图10-12

![](images/page_146_image_13.jpg)

<details>
<summary>text_image</summary>

y
1
y
D
y=x
-1 O 1 x
-1
</details>

图10-13

例3 计算 $\iint_{D} xy \, \mathrm{d}\sigma$，其中 $D$ 是由抛物线 $y^2 = x$ 及直线 $y = x - 2$ 所围成的闭区域.

解 画出积分区域 $D$ 如图10-14所示. $D$ 既是 $X$ 型的, 又是 $Y$ 型的. 若利用公式(2-2), 则得

$$
\iint_ {D} x y \mathrm{d} \sigma = \int_ {- 1} ^ {2} \left[ \int_ {y ^ {2}} ^ {y + 2} x y \mathrm{d} x \right] \mathrm{d} y = \int_ {- 1} ^ {2} \left[ \frac {x ^ {2}}{2} y \right] _ {y ^ {2}} ^ {y + 2} \mathrm{d} y = \frac {1}{2} \int_ {- 1} ^ {2} \left[ y (y + 2) ^ {2} - y ^ {5} \right] \mathrm{d} y
$$

$$
= \frac {1}{2} \left[ \frac {y ^ {4}}{4} + \frac {4}{3} y ^ {3} + 2 y ^ {2} - \frac {y ^ {6}}{6} \right] _ {- 1} ^ {2} = \frac {4 5}{8}.
$$

若利用公式(2-1)来计算,则由于在区间[0,1]及[1,4]上表示 $\varphi_{1}(x)$ 的式子不同,所以要用经过交点(1,-1)且平行于y轴的直线x=1把区域D分成 $D_{1}$ 和 $D_{2}$ 两部分(图10-15),其中

$$
D _ {1} = \{(x, y) | - \sqrt {x} \leqslant y \leqslant \sqrt {x}, 0 \leqslant x \leqslant 1 \}, \quad D _ {2} = \{(x, y) | x - 2 \leqslant y \leqslant \sqrt {x}, 1 \leqslant x \leqslant 4 \}.
$$

![](images/page_147_image_4.jpg)

<details>
<summary>text_image</summary>

y
2
x=y²
y
D
O
x=y+2
-1
(1, -1)
(4, 2)
</details>

图10-14

![](images/page_147_image_6.jpg)

<details>
<summary>text_image</summary>

y
y=√x
D₁
D₂
O
x 1
y=x-2
x 4 x
(4, 2)
y=-√x
(1, -1)
</details>

图10-15

![](images/page_147_image_8.jpg)

因此,根据二重积分的性质2,就有

$$
\iint_ {D} x y \mathrm{d} \sigma = \iint_ {D _ {1}} x y \mathrm{d} \sigma + \iint_ {D _ {2}} x y \mathrm{d} \sigma = \int_ {0} ^ {1} \left[ \int_ {- \sqrt {x}} ^ {\sqrt {x}} x y \mathrm{d} y \right] \mathrm{d} x + \int_ {1} ^ {4} \left[ \int_ {x - 2} ^ {\sqrt {x}} x y \mathrm{d} y \right] \mathrm{d} x.
$$

由此可见,这里用公式(2-1)来计算需要化为两个二次积分.

上述几个例子说明,在化二重积分为二次积分时,为了计算简便,需要选择恰当的

二次积分的次序.这时,既要考虑积分区域D的形状,又要考虑被积函数 $f(x,y)$ 的特性.

例 4 求两个底圆半径都等于 R 的直交圆柱面所围成的立体的体积.

解 设这两个圆柱面的方程分别为

$$
x ^ {2} + y ^ {2} = R ^ {2} \quad {\text {及}} \quad x ^ {2} + z ^ {2} = R ^ {2}.
$$

利用立体关于坐标平面的对称性, 只要算出它在第 I 卦限部分(图 10-16(a)) 的体积  $V_{1}$ , 然后再乘 8 就行了.

所求立体在第Ⅰ卦限部分可以看成是一个曲顶柱体,它的底为

$$
D = \{(x, y) \mid 0 \leqslant y \leqslant \sqrt {R ^ {2} - x ^ {2}}, 0 \leqslant x \leqslant R \},
$$

如图 10-16(b) 所示. 它的顶是柱面  $z=\sqrt{R^{2}-x^{2}}$ . 于是,

$$
V _ {1} = \iint_ {D} \sqrt {R ^ {2} - x ^ {2}}   \mathrm{d} \sigma .
$$

![](images/page_147_image_22.jpg)

<details>
<summary>text_image</summary>

z
O
D
R
y
x
R
</details>

(a)

![](images/page_147_image_24.jpg)

<details>
<summary>text_image</summary>

y
y=\u221a(R²-x²)
D
O	x	R	x
</details>

(b)

图10-16

利用公式(2-1)，得

$$
\begin{array}{l} V _ {1} = \iint_ {D} \sqrt {R ^ {2} - x ^ {2}} \mathrm{d} \sigma = \int_ {0} ^ {R} \left[ \int_ {0} ^ {\sqrt {R ^ {2} - x ^ {2}}} \sqrt {R ^ {2} - x ^ {2}} \mathrm{d} y \right] \mathrm{d} x \\ = \int_ {0} ^ {R} \left[ \sqrt {R ^ {2} - x ^ {2}} y \right] _ {0} ^ {\sqrt {R ^ {2} - x ^ {2}}} \mathrm{d} x = \int_ {0} ^ {R} \left(R ^ {2} - x ^ {2}\right) \mathrm{d} x = \frac {2}{3} R ^ {3}. \\ \end{array}
$$

从而所求立体的体积为

$$
V = 8 V _ {1} = \frac {1 6}{3} R ^ {3}.
$$

## 二、利用极坐标计算二重积分

有些二重积分,积分区域 D 的边界曲线用极坐标方程来表示比较方便,且被积函数用极坐标变量  $\rho,\theta$  表达比较简单.这时,就可以考虑利用极坐标来计算二重积分  $\iint_{D}f(x,y)\mathrm{d}\sigma$ .

按二重积分的定义

$$
\iint_ {D} f (x, y) \mathrm{d} \sigma = \lim _ {\lambda \to 0} \sum_ {i = 1} ^ {n} f (\xi_ {i}, \eta_ {i}) \Delta \sigma_ {i},
$$

下面我们来研究这个和的极限在极坐标系中的形式.

假定从极点 $O$ 出发且穿过闭区域 $D$ 内部的射线与 $D$ 的边界曲线相交不多于两点.我们用以极点为中心的一族同心圆: $\rho =$ 常数以及从极点出发的一族射线: $\theta =$ 常数，

把 D 分成 n 个小闭区域(图10-17).除了包含边界点的一些小闭区域外,小闭区域的面积  $\Delta\sigma_{i}$  可计算如下:

$$
\begin{array}{l} \Delta \sigma_ {i} = \frac {1}{2} \left(\rho_ {i} + \Delta \rho_ {i}\right) ^ {2} \cdot \Delta \theta_ {i} - \frac {1}{2} \rho_ {i} ^ {2} \cdot \Delta \theta_ {i} \\ = \frac {1}{2} \left(2 \rho_ {i} + \Delta \rho_ {i}\right) \Delta \rho_ {i} \cdot \Delta \theta_ {i} \\ = \frac {\rho_ {i} + (\rho_ {i} + \Delta \rho_ {i})}{2} \cdot \Delta \rho_ {i} \cdot \Delta \theta_ {i} = \bar {\rho_ {i}} \cdot \Delta \rho_ {i} \cdot \Delta \theta_ {i}, \\ \end{array}
$$

![](images/page_148_image_13.jpg)

<details>
<summary>text_image</summary>

ρ=ρᵢ+Δρᵢ
ρ=ρᵢ
θ=θᵢ+Δθᵢ
θ=θᵢ
Δσᵢ
Δρᵢ
Δθᵢ
D
O
A
</details>

图10-17

其中 $\bar{\rho}_i$ 表示相邻两圆弧的半径的平均值. 在这小闭区域内取圆周 $\rho = \bar{\rho}_i$ 上的一点 $(\bar{\rho}_i, \bar{\theta}_i)$, 设该点的直角坐标为 $(\xi_i, \eta_i)$, 则由直角坐标与极坐标之间的关系有 $\xi_i = \bar{\rho}_i \cos \bar{\theta}_i$, $\eta_i = \bar{\rho}_i \sin \bar{\theta}_i$. 于是

$$
\lim _ {\lambda \rightarrow 0} \sum_ {i = 1} ^ {n} f (\xi_ {i}, \eta_ {i}) \Delta \sigma_ {i} = \lim _ {\lambda \rightarrow 0} \sum_ {i = 1} ^ {n} f (\bar {\rho} _ {i} \cos \bar {\theta} _ {i}, \bar {\rho} _ {i} \sin \bar {\theta} _ {i}) \bar {\rho} _ {i} \cdot \Delta \rho_ {i} \cdot \Delta \theta_ {i},
$$

即

$$
\iint_ {D} f (x, y) \mathrm{d} \sigma = \iint_ {D} f (\rho \cos \theta , \rho \sin \theta) \rho \mathrm{d} \rho \mathrm{d} \theta .
$$

这里我们把点 $(\rho, \theta)$ 看做是在同一平面上的点 $(x, y)$ 的极坐标表示，所以上式右端的积分区域仍然记作 $D$。因为在直角坐标系中 $\iint_{D} f(x, y) \mathrm{d}\sigma$ 也常记作 $\iint_{D} f(x, y) \mathrm{d}x \mathrm{d}y$，所以上式又可写成

$$
\iint_ {D} f (x, y) \mathrm{d} x \mathrm{d} y = \iint_ {D} f (\rho \cos \theta , \rho \sin \theta) \rho \mathrm{d} \rho \mathrm{d} \theta . \tag {2-4}
$$

这就是二重积分的变量从直角坐标变换为极坐标的变换公式,其中  $\rho d\rho d\theta$  就是极坐标系中的面积元素.

公式(2-4)表明,要把二重积分中的变量从直角坐标变换为极坐标,只要把被积函数中的x与y分别换成 $\rho\cos\theta$ 与 $\rho\sin\theta$ ,并把直角坐标系中的面积元素dxdy换成极坐标系中的面积元素 $\rho d\rho d\theta$ .

极坐标系中的二重积分,同样可以化为二次积分来计算.

设积分区域 $D$ 可以用不等式

$$
\varphi_ {1} (\theta) \leqslant \rho \leqslant \varphi_ {2} (\theta), \quad \alpha \leqslant \theta \leqslant \beta
$$

来表示(图 10-18)，其中函数  $\varphi_{1}(\theta)$ ,  $\varphi_{2}(\theta)$  在区间  $[\alpha, \beta]$  上连续.

![](images/page_149_image_10.jpg)

<details>
<summary>text_image</summary>

ρ=φ₂(θ)
D
ρ=φ₁(θ)
β
α
O
A
</details>

(a)

![](images/page_149_image_12.jpg)

<details>
<summary>text_image</summary>

ρ=φ₂(θ)
D
ρ=φ₁(θ)
β
α
O
A
</details>

(b)

图10-18

先在区间 $[\alpha, \beta]$ 上任意取定一个 $\theta$ 值. 对应于这个 $\theta$ 值, $D$ 上的点 (图10-19中这些点在线段 $EF$ 上) 的极径 $\rho$ 从 $\varphi_1(\theta)$ 变到 $\varphi_2(\theta)$. 又 $\theta$ 是在 $[\alpha, \beta]$ 上任意取定的, 所以 $\theta$ 的变化范围是区间 $[\alpha, \beta]$. 这样就可看出, 极坐标系中的二重积分化为二次积分的公式为

$$
\iint_ {D} f (\rho \cos \theta , \rho \sin \theta) \rho \mathrm{d} \rho \mathrm{d} \theta = \int_ {\alpha} ^ {\beta} \left[ \int_ {\varphi_ {1} (\theta)} ^ {\varphi_ {2} (\theta)} f (\rho \cos \theta , \rho \sin \theta) \rho \mathrm{d} \rho \right] \mathrm{d} \theta . \tag {2-5}
$$

上式也写成

$$
\iint_ {D} f (\rho \cos \theta , \rho \sin \theta) \rho \mathrm{d} \rho \mathrm{d} \theta = \int_ {\alpha} ^ {\beta} \mathrm{d} \theta \int_ {\varphi_ {1} (\theta)} ^ {\varphi_ {2} (\theta)} f (\rho \cos \theta , \rho \sin \theta) \rho \mathrm{d} \rho . \tag {$2-5^{\prime$}}
$$

如果积分区域 $D$ 是图10-20所示的曲边扇形，那么可以把它看做图10-18(a)中当 $\varphi_1(\theta) \equiv 0, \varphi_2(\theta) = \varphi(\theta)$ 时的特例.这时闭区域 $D$ 可以用不等式

$$
0 \leqslant \rho \leqslant \varphi (\theta), \quad \alpha \leqslant \theta \leqslant \beta
$$

来表示,而公式 $(2-5')$ 成为

$$
\iint_ {D} f (\rho \cos \theta , \rho \sin \theta) \rho \mathrm{d} \rho \mathrm{d} \theta = \int_ {\alpha} ^ {\beta} \mathrm{d} \theta \int_ {0} ^ {\varphi (\theta)} f (\rho \cos \theta , \rho \sin \theta) \rho \mathrm{d} \rho .
$$

如果积分区域 $D$ 如图10-21所示, 极点在 $D$ 的内部, 那么可以把它看做图10-20中当 $\alpha = 0$ 且 $\beta = 2\pi$ 时的特例. 这时闭区域 $D$ 可以用不等式

$$
0 \leqslant \rho \leqslant \varphi (\theta), \quad 0 \leqslant \theta \leqslant 2 \pi
$$

来表示,而公式 $(2-5')$ 成为

$$
\iint_ {D} f (\rho \cos \theta , \rho \sin \theta) \rho \mathrm{d} \rho \mathrm{d} \theta = \int_ {0} ^ {2 \pi} \mathrm{d} \theta \int_ {0} ^ {\varphi (\theta)} f (\rho \cos \theta , \rho \sin \theta) \rho \mathrm{d} \rho .
$$

![](images/page_150_image_8.jpg)

<details>
<summary>text_image</summary>

D
F
E
β
θ
α
O
φ₁(θ)
φ₂(θ)
A
</details>

图10-19

![](images/page_150_image_10.jpg)

<details>
<summary>text_image</summary>

ρ=φ(θ)
D
β
α
O
A
</details>

图10-20

![](images/page_150_image_12.jpg)

<details>
<summary>text_image</summary>

ρ=φ(θ)
D
O
A
</details>

图10-21

由二重积分的性质3,闭区域D的面积 $\sigma$ 可以表示为

$$
\sigma = \iint_ {D} \mathrm{d} \sigma.
$$

在极坐标系中,面积元素  $d\sigma=\rho d\rho d\theta$ , 上式成为

$$
\sigma = \iint_ {D} \rho \mathrm{d} \rho \mathrm{d} \theta .
$$

如果闭区域 D 如图 10-18(a) 所示, 那么由公式  $(2-5')$  有

$$
\sigma = \iint_ {D} \rho \mathrm{d} \rho \mathrm{d} \theta = \int_ {\alpha} ^ {\beta} \mathrm{d} \theta \int_ {\varphi_ {1} (\theta)} ^ {\varphi_ {2} (\theta)} \rho \mathrm{d} \rho = \frac {1}{2} \int_ {\alpha} ^ {\beta} [ \varphi_ {2} ^ {2} (\theta) - \varphi_ {1} ^ {2} (\theta) ] \mathrm{d} \theta.
$$

特别地,如果闭区域 D 如图 10-20 所示,那么  $\varphi_{1}(\theta)=0,\varphi_{2}(\theta)=\varphi(\theta)$ .于是

$$
\sigma = \frac {1}{2} \int_ {\alpha} ^ {\beta} \varphi^ {2} (\theta) \mathrm{d} \theta .
$$

例 5 计算  $\iint_{D} e^{-x^{2}-y^{2}} dx dy$ ，其中 D 是由圆心在原点、半径为 a 的圆周所围成的闭区域.

解 在极坐标系中,闭区域 D 可表示为

$$
0 \leqslant \rho \leqslant a, \quad 0 \leqslant \theta \leqslant 2 \pi .
$$

由公式(2-4)及(2-5)有

$$
\begin{array}{l} \iint_ {D} \mathrm{e} ^ {- x ^ {2} - y ^ {2}} \mathrm{d} x \mathrm{d} y = \iint_ {D} \mathrm{e} ^ {- p ^ {2}} \rho \mathrm{d} \rho \mathrm{d} \theta = \int_ {0} ^ {2 \pi} \left[ \int_ {0} ^ {a} \mathrm{e} ^ {- p ^ {2}} \rho \mathrm{d} \rho \right] \mathrm{d} \theta \\ = \int_ {0} ^ {2 \pi} \left[ - \frac {1}{2} \mathrm{e} ^ {- p ^ {2}} \right] _ {0} ^ {a} \mathrm{d} \theta = \frac {1}{2} (1 - \mathrm{e} ^ {- a ^ {2}}) \int_ {0} ^ {2 \pi} \mathrm{d} \theta = \pi (1 - \mathrm{e} ^ {- a ^ {2}}). \\ \end{array}
$$

本题如果用直角坐标计算,因为积分  $\int e^{-x^{2}} dx$  不能用初等函数表示,所以算不出来.现在我们利用上面的结果来计算工程上常用的反常积分  $\int_{0}^{+\infty} e^{-x^{2}} dx$ .

设

$$
D _ {1} = \{(x, y) | x ^ {2} + y ^ {2} \leqslant R ^ {2}, x \geqslant 0, y \geqslant 0 \},
$$

$$
D _ {2} = \{(x, y) | x ^ {2} + y ^ {2} \leqslant 2 R ^ {2}, x \geqslant 0, y \geqslant 0 \},
$$

$$
S = \{(x, y) \mid 0 \leqslant x \leqslant R, 0 \leqslant y \leqslant R \}.
$$

显然 $D_{1} \subset S \subset D_{2}$ (图10-22). 由于 $\mathrm{e}^{-x^2 - y^2} > 0$，从而在这些闭区域上的二重积分之间有不等式

$$
\iint_ {D _ {1}} \mathrm{e} ^ {- x ^ {2} - y ^ {2}} \mathrm{d} x \mathrm{d} y <   \iint_ {S} \mathrm{e} ^ {- x ^ {2} - y ^ {2}} \mathrm{d} x \mathrm{d} y <   \iint_ {D _ {2}} \mathrm{e} ^ {- x ^ {2} - y ^ {2}} \mathrm{d} x \mathrm{d} y.
$$

![](images/page_151_image_9.jpg)

<details>
<summary>text_image</summary>

y
S
D₁
D₂
O
R √2R x
</details>

图10-22

因为

$$
\iint_ {S} \mathrm{e} ^ {- x ^ {2} - y ^ {2}} \mathrm{d} x \mathrm{d} y = \int_ {0} ^ {R} \mathrm{e} ^ {- x ^ {2}} \mathrm{d} x \cdot \int_ {0} ^ {R} \mathrm{e} ^ {- y ^ {2}} \mathrm{d} y = \left(\int_ {0} ^ {R} \mathrm{e} ^ {- x ^ {2}} \mathrm{d} x\right) ^ {2},
$$

又应用上面已得的结果有

$$
\iint_ {D _ {1}} \mathrm{e} ^ {- x ^ {2} - y ^ {2}} \mathrm{d} x \mathrm{d} y = \frac {\pi}{4} (1 - \mathrm{e} ^ {- R ^ {2}}), \quad \iint_ {D _ {2}} \mathrm{e} ^ {- x ^ {2} - y ^ {2}} \mathrm{d} x \mathrm{d} y = \frac {\pi}{4} (1 - \mathrm{e} ^ {- 2 R ^ {2}}),
$$

于是上面的不等式可写成

$$
\frac {\pi}{4} (1 - \mathrm{e} ^ {- R ^ {2}}) <   \left(\int_ {0} ^ {R} \mathrm{e} ^ {- x ^ {2}} \mathrm{d} x\right) ^ {2} <   \frac {\pi}{4} (1 - \mathrm{e} ^ {- 2 R ^ {2}}).
$$

令 $R\to +\infty$ ，上式两端趋于同一极限 $\frac{\pi}{4}$ ，从而

$$
\int_ {0} ^ {+ \infty} \mathrm{e} ^ {- x ^ {2}} \mathrm{d} x = \frac {\sqrt {\pi}}{2}.
$$

例 6 求球体  $x^{2}+y^{2}+z^{2}\leqslant4a^{2}$  被圆柱面  $x^{2}+y^{2}=2ax\quad(a>0)$  所截得的（含在圆柱面内的部分）立体的体积（图 10-23）.

解 由对称性，

$$
V = 4 \iint_ {D} \sqrt {4 a ^ {2} - x ^ {2} - y ^ {2}}   \mathrm{d} x \mathrm{d} y,
$$

其中 D 为半圆周  $y=\sqrt{2ax-x^{2}}$  及 x 轴所围成的闭区域. 在极坐标系中, 闭区域 D 可用不

等式

$$
0 \leqslant \rho \leqslant 2 a \cos \theta , \quad 0 \leqslant \theta \leqslant \frac {\pi}{2}
$$

来表示.于是

$$
\begin{array}{l} V = 4 \iint_ {D} \sqrt {4 a ^ {2} - \rho^ {2}} \rho \mathrm{d} \rho \mathrm{d} \theta = 4 \int_ {0} ^ {\frac {\pi}{2}} \mathrm{d} \theta \int_ {0} ^ {2 a \cos \theta} \sqrt {4 a ^ {2} - \rho^ {2}} \rho \mathrm{d} \rho \\ = \frac {3 2}{3} a ^ {3} \int_ {0} ^ {\frac {\pi}{2}} (1 - \sin^ {3} \theta) \mathrm{d} \theta = \frac {3 2}{3} a ^ {3} \left(\frac {\pi}{2} - \frac {2}{3}\right). \\ \end{array}
$$

![](images/page_152_image_5.jpg)

<details>
<summary>text_image</summary>

z
O
y
D
2a
x
</details>

(a)

![](images/page_152_image_7.jpg)

<details>
<summary>text_image</summary>

ρ=2acos θ
D
θ
O
a
2a
A
</details>

(b)

图10-23

## \* 三、二重积分的换元法

上一目得到的二重积分的变量从直角坐标变换为极坐标的变换公式, 是二重积分换元法的一种特殊情形. 在那里, 我们把平面上同一个点 M, 既用直角坐标  $(x, y)$  表示, 又用极坐标  $(\rho, \theta)$  表示, 它们间的关系为

$$
\left\{ \begin{array}{l} x = \rho \cos \theta , \\ y = \rho \sin \theta . \end{array} \right. \tag {2-6}
$$

也就是说,由(2-6)式联系的点 $(x,y)$ 和点 $(\rho ,\theta)$ 看成是同一个平面上的同一个点,只是采用不同的坐标罢了.现在,我们采用另一种观点来加以解释.把(2-6)式看成是从直角坐标平面 $\rho O\theta$ 到直角坐标平面 $xOy$ 的一种变换,即对于 $\rho O\theta$ 平面上的一点$M^{\prime}(\rho ,\theta)$,通过变换(2-6),变成 $xOy$ 平面上的一点 $M(x,y)$.在两个平面各自限定的某个范围内,这种变换还是一对一的(即是一一映射).下面就采用这种观点来讨论二重积分换元法的一般情形.

定理 设 $f(x, y)$ 在 $xOy$ 平面上的闭区域 $D$ 上连续, 若变换

$$
T: x = x (u, v), y = y (u, v) \tag {2-7}
$$

将 $uOv$ 平面上的闭区域 $D'$ 变为 $xOy$ 平面上的 $D$, 且满足

(1) $x(u, v), y(u, v)$ 在 $D'$ 上具有一阶连续偏导数；

(2) 在  $D'$  上雅可比式  $J(u,v)=\frac{\partial(x,y)}{\partial(u,v)}\neq0;$
(3) 变换  $T:D'\rightarrow D$  是一对一的，

则有

$$
\iint_ {D} f (x, y) \mathrm{d} x \mathrm{d} y = \iint_ {D ^ {\prime}} f [ x (u, v), y (u, v) ] | J (u, v) | \mathrm{d} u \mathrm{d} v. \tag {2-8}
$$

公式(2-8)称为二重积分的换元公式.

证 显然, 在定理的假设下, (2-8) 式两端的二重积分都存在. 由于二重积分与积分区域的分法无关, 我们用平行于坐标轴的直线网来分割 $D'$, 使得除去包含边界点的小闭区域外, 其余的小闭区域都为边长是 $h$ 的正方形闭区域. 任取一个这样得到的正方形闭区域, 设其顶点为 $M_1'(u, v), M_2'(u + h, v), M_3'(u + h, v + h), M_4'(u, v + h)$, 其面积为 $\Delta \sigma' = h^2$ (图 10-24(a)). 正方形闭区域 $M_1'M_2'M_3'M_4'$ 经变换 (2-7) 变成 $xOy$ 平面上的一个曲边四边形 $M_1M_2M_3M_4$, 它的四个顶点的坐标是

$$
\begin{array}{l} M _ {1}: x _ {1} = x (u, v), y _ {1} = y (u, v); \\ M _ {2}: x _ {2} = x (u + h, v) = x (u, v) + x _ {u} (u, v) h + o (h), \\ y _ {2} = y (u + h, v) = y (u, v) + y _ {u} (u, v) h + o (h); \\ M _ {3}: x _ {3} = x (u + h, v + h) = x (u, v) + x _ {u} (u, v) h + x _ {v} (u, v) h + o (h), \\ y _ {3} = y (u + h, v + h) = y (u, v) + y _ {u} (u, v) h + y _ {v} (u, v) h + o (h); \\ M _ {4}: x _ {4} = x (u, v + h) = x (u, v) + x _ {v} (u, v) h + o (h), \\ y _ {4} = y (u, v + h) = y (u, v) + y _ {v} (u, v) h + o (h), \\ \end{array}
$$

其面积为 $\Delta \sigma$ （图10-24(b)). 可以证明，曲边四边形 $M_{1}M_{2}M_{3}M_{4}$ 的面积与直边四边形 $M_{1}M_{2}M_{3}M_{4}$ （四个顶点用直线相连）的面积当 $h \to 0$ 时只相差高阶无穷小. 又由上面这些坐标表示式可知，若不计高阶无穷小，则有

$$
x _ {2} - x _ {1} = x _ {3} - x _ {4}, \quad y _ {2} - y _ {1} = y _ {3} - y _ {4}, \quad x _ {4} - x _ {1} = x _ {3} - x _ {2}, \quad y _ {4} - y _ {1} = y _ {3} - y _ {2},
$$

![](images/page_153_image_11.jpg)

<details>
<summary>text_image</summary>

v
Δσ'
M₄ M₃' M₁' M₂'
v+h
v
O u u+h u
</details>

(a)

![](images/page_153_image_13.jpg)

<details>
<summary>text_image</summary>

y
Δσ
M₄
M₃
M₁
M₂
O
x
</details>

(b)

图10-24

这表示, 直边四边形 $M_{1}M_{2}M_{3}M_{4}$ 的对边的长度可看做两两相等. 因此, 若不计高阶无穷小, 曲边四边形 $M_{1}M_{2}M_{3}M_{4}$ 可看做平行四边形, 于是它的面积 $\Delta\sigma$ 近似等于 $\triangle M_{1}M_{2}M_{3}$ 的面积的 2 倍. 根据解析几何, $\triangle M_{1}M_{2}M_{3}$ 的面积的 2 倍等于行列式

$$
\left| \begin{array}{c c} x _ {2} - x _ {1} & x _ {3} - x _ {2} \\ y _ {2} - y _ {1} & y _ {3} - y _ {2} \end{array} \right|
$$

的绝对值,由于

$$
x _ {2} - x _ {1} = x _ {u} (u, v) h + o (h), \quad x _ {3} - x _ {2} = x _ {v} (u, v) h + o (h),
$$

$$
y _ {2} - y _ {1} = y _ {u} (u, v) h + o (h), \quad y _ {3} - y _ {2} = y _ {v} (u, v) h + o (h),
$$

因此上面的行列式与行列式

$$
\left| \begin{array}{l l} x _ {u} (u, v) h & x _ {v} (u, v) h \\ y _ {u} (u, v) h & y _ {v} (u, v) h \end{array} \right| = \left| \begin{array}{l l} x _ {u} (u, v) & x _ {v} (u, v) \\ y _ {u} (u, v) & y _ {v} (u, v) \end{array} \right| h ^ {2}
$$

只相差一个比 $h^2$ 高阶的无穷小.于是

$$
\Delta \sigma = \left| \frac {\partial (x , y)}{\partial (u , v)} \right| \Delta \sigma^ {\prime} + o (\Delta \sigma^ {\prime}) \quad (h \rightarrow 0).
$$

把 $f(x,y) = f[x(u,v),y(u,v)]$ 的两端分别与上式两端相乘，得

$$
f (x, y) \Delta \sigma = f [ x (u, v), y (u, v) ] \left| \frac {\partial (x , y)}{\partial (u , v)} \right| \Delta \sigma^ {\prime} + f [ x (u, v), y (u, v) ] \cdot o (\Delta \sigma^ {\prime}).
$$

上式对一切小正方形闭区域取和并令 $h \to 0$ 求极限, 由于上式右端第二项的和的极限为零, 于是得公式(2-8). 定理证毕.

这里我们指出,如果雅可比式  $J(u,v)$  只在  $D'$  内个别点上,或一条曲线上为零,而在其他点上不为零,那么换元公式(2-8)仍成立.

在变换为极坐标  $x=\rho\cos\theta, y=\rho\sin\theta$  的特殊情形下, 雅可比式

$$
J = \left| \begin{array}{c c} \frac {\partial x}{\partial \rho} & \frac {\partial x}{\partial \theta} \\ \frac {\partial y}{\partial \rho} & \frac {\partial y}{\partial \theta} \end{array} \right| = \left| \begin{array}{c c} \cos \theta & - \rho \sin \theta \\ \sin \theta & \rho \cos \theta \end{array} \right| = \rho ,
$$

它仅在 $\rho = 0$ 处为零，故不论闭区域 $D'$ 是否含有极点，换元公式仍成立.即有

$$
\iint_ {D} f (x, y) \mathrm{d} x \mathrm{d} y = \iint_ {D ^ {\prime}} f (\rho \cos \theta , \rho \sin \theta) \rho \mathrm{d} \rho \mathrm{d} \theta ,
$$

这里 $D'$ 是 $D$ 在直角坐标平面 $\rho O\theta$ 上的对应区域.在上一目内所证得的相同的公式中用的是 $D$ 而不是 $D'$, 当积分区域 $D$ 用极坐标表示时, 其形式就与上式右端的形式完全等同了.

例7 计算 $\iint_{D} \mathrm{e}^{\frac{y - x}{y + x}} \, \mathrm{d}x \, \mathrm{d}y$，其中 $D$ 是由 $x$ 轴、$y$ 轴和直线 $x + y = 2$ 所围成的闭区域.

解 令 $u = y - x, v = y + x$，则 $x = \frac{v - u}{2}, y = \frac{v + u}{2}$.

作变换 $x = \frac{v - u}{2}, y = \frac{v + u}{2}$，则 $xOy$ 平面上的闭区域 $D$ 和它在 $uOv$ 平面上的对应区域 $D'$ 如图10-25所示.

![](images/page_155_image_3.jpg)

<details>
<summary>text_image</summary>

y
x+y=2
D
O
x
</details>

(a)

![](images/page_155_image_5.jpg)

<details>
<summary>text_image</summary>

v
v=2
D'
u=-v
u=v
O
u
</details>

(b)

图10-25

雅可比式为

$$
J = \frac {\partial (x , y)}{\partial (u , v)} = \left| \begin{array}{c c} - \frac {1}{2} & \frac {1}{2} \\ \frac {1}{2} & \frac {1}{2} \end{array} \right| = - \frac {1}{2}.
$$

利用公式(2-8)，得

$$
\iint_ {D} \mathrm{e} ^ {\frac {y - x}{y + x}} \mathrm{d} x \mathrm{d} y = \iint_ {D ^ {\prime}} \mathrm{e} ^ {\frac {u}{v}} \left| - \frac {1}{2} \right| \mathrm{d} u \mathrm{d} v = \frac {1}{2} \int_ {0} ^ {2} \mathrm{d} v \int_ {- v} ^ {v} \mathrm{e} ^ {\frac {u}{v}} \mathrm{d} u = \frac {1}{2} \int_ {0} ^ {2} (\bar {\mathrm{e}} - \mathrm{e} ^ {- 1}) v \mathrm{d} v = \mathrm{e} - \mathrm{e} ^ {- 1}.
$$

例8 求由直线 $x + y = c, x + y = d, y = ax, y = bx$ ($0 < c < d, 0 < a < b$) 所围成的闭区域 $D$ (图10-26(a)) 的面积.

![](images/page_155_image_13.jpg)

<details>
<summary>text_image</summary>

y
d
y=bx
C
D
O
c
x
y=ax
d
</details>

(a)

![](images/page_155_image_15.jpg)

<details>
<summary>text_image</summary>

v
b
D'
a
O
c
d
u
</details>

(b)

图10-26

解 所求面积为

$$
\iint_ {D} \mathrm{d} x \mathrm{d} y.
$$

上述二重积分直接化为二次积分计算比较麻烦.现采用换元法.令 $u = x + y, v = \frac{y}{x}$, 则 $x = \frac{u}{1 + v}, y = \frac{uv}{1 + v}$. 在这变换下, $D$ 的边界 $x + y = c, x + y = d, y = ax, y = bx$ 依次与 $u = c, u = d, v = a, v = b$ 对应.后者构成与 $D$ 对应的闭区域 $D'$ 的边界.于是

$$
D ^ {\prime} = \{(u, v) \mid c \leqslant u \leqslant d, a \leqslant v \leqslant b \},
$$

如图 10-26(b) 所示. 又雅可比式

$$
J = \frac {\partial (x , y)}{\partial (u , v)} = \frac {u}{(1 + v) ^ {2}} \neq 0, \quad (u, v) \in D ^ {\prime}.
$$

从而所求面积为

$$
\iint_ {D} \mathrm{d} x \mathrm{d} y = \iint_ {D ^ {\prime}} \frac {u}{(1 + v) ^ {2}} \mathrm{d} u \mathrm{d} v = \int_ {a} ^ {b} \frac {\mathrm{d} v}{(1 + v) ^ {2}} \int_ {c} ^ {d} u \mathrm{d} u = \frac {(b - a) (d ^ {2} - c ^ {2})}{2 (1 + a) (1 + b)}.
$$

例9 计算 $\iint_{D} \sqrt{1 - \frac{x^2}{a^2} - \frac{y^2}{b^2}} \, \mathrm{d}x \, \mathrm{d}y$，其中 $D$ 为椭圆 $\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1$ 所围成的闭区域.

解 作广义极坐标变换

$$
\left\{ \begin{array}{l} x = a \rho \cos \theta , \\ y = b \rho \sin \theta , \end{array} \right.
$$

其中 $a > 0, b > 0, \rho \geqslant 0, 0 \leqslant \theta \leqslant 2\pi$. 在这个变换下，与 $D$ 对应的闭区域为 $D' = \{(\rho, \theta) | 0 \leqslant \rho \leqslant 1, 0 \leqslant \theta \leqslant 2\pi\}$，雅可比式

$$
J = \frac {\partial (x , y)}{\partial (\rho , \theta)} = a b \rho .
$$

J 在  $D'$  内仅在  $\rho=0$  处为零, 故换元公式仍成立, 从而有

$$
\iint_ {D} \sqrt {1 - \frac {x ^ {2}}{a ^ {2}} - \frac {y ^ {2}}{b ^ {2}}} \mathrm{d} x \mathrm{d} y = \iint_ {D ^ {\prime}} \sqrt {1 - \rho^ {2}} a b \rho \mathrm{d} \rho \mathrm{d} \theta = \frac {2}{3} \pi a b.
$$

## 习题10-2

1. 计算下列二重积分:

(1) $\iint_{D}(x^{2} + y^{2})\mathrm{d}\sigma$ ，其中 $D = \{(x,y)\mid |x|\leqslant 1,|y|\leqslant 1\}$
(2) $\iint_{D}(3x + 2y)\mathrm{d}\sigma$ ，其中 $D$ 是由两坐标轴及直线 $x + y = 2$ 所围成的闭区域；
(3) $\iint_{D} (x^3 + 3x^2y + y^3) \, \mathrm{d}\sigma$, 其中 $D = \{(x, y) \mid 0 \leqslant x \leqslant 1, 0 \leqslant y \leqslant 1\}$;

(4) $\iint_{D} x\cos (x + y)\mathrm{d}\sigma$，其中 $D$ 是顶点分别为 $(0,0), (\pi, 0)$ 和 $(\pi, \pi)$ 的三角形闭区域；
(5) $\iint_{D} \sqrt{|y - x^2|} \, \mathrm{d}x \, \mathrm{d}y$, 其中 $D = \{(x, y) | 0 \leqslant x \leqslant 1, 0 \leqslant y \leqslant 1\}$.

2. 画出积分区域,并计算下列二重积分:

(1) $\iint_{D} x\sqrt{y} \, \mathrm{d}\sigma$，其中 $D$ 是由两条抛物线 $y = \sqrt{x}, y = x^2$ 所围成的闭区域；
(2) $\iint_{D} xy^{2} \, \mathrm{d}\sigma$, 其中 $D$ 是由圆周 $x^{2} + y^{2} = 4$ 及 $y$ 轴所围成的右半闭区域;
(3) $\iint_{D} \mathrm{e}^{x + y} \, \mathrm{d}\sigma$, 其中 $D = \{(x, y) \mid |x| + |y| \leqslant 1\}$;
(4) $\iint_{D} (x^{2} + y^{2} - x) \, \mathrm{d}\sigma$, 其中 $D$ 是由直线 $y = 2, y = x$ 及 $y = 2x$ 所围成的闭区域.

3. 如果二重积分 $\iint_{D} f(x, y) \, \mathrm{d}x \, \mathrm{d}y$ 的被积函数 $f(x, y)$ 是两个函数 $f_1(x)$ 及 $f_2(y)$ 的乘积，即 $f(x, y) = f_1(x) \cdot f_2(y)$，积分区域 $D = \{(x, y) \mid a \leqslant x \leqslant b, c \leqslant y \leqslant d\}$，证明这个二重积分等于两个定积分的乘积，即

$$
\iint_ {D} f _ {1} (x) \cdot f _ {2} (y) \mathrm{d} x \mathrm{d} y = \left[ \int_ {a} ^ {b} f _ {1} (x) \mathrm{d} x \right] \cdot \left[ \int_ {c} ^ {d} f _ {2} (y) \mathrm{d} y \right].
$$

4. 化二重积分

$$
I = \iint_ {D} f (x, y) \mathrm{d} \sigma
$$

为二次积分(分别列出对两个变量先后次序不同的两个二次积分),其中积分区域 D 是

(1) 由直线 y = x 及抛物线  $y^{2} = 4x$  所围成的闭区域；
(2) 由 x 轴及半圆周  $x^{2}+y^{2}=r^{2}\quad(y\geqslant0)$  所围成的闭区域；
(3) 由直线 y=x, x=2 及双曲线  $y=\frac{1}{x}$  (x>0) 所围成的闭区域；
(4) 环形闭区域  $\{(x,y)\mid1\leqslant x^{2}+y^{2}\leqslant4\}$ .

5. 设 $f(x, y)$ 在 $D$ 上连续，其中 $D$ 是由直线 $y = x, y = a$ 及 $x = b$ ($b > a$) 所围成的闭区域，证明

$$
\int_ {a} ^ {b} \mathrm{d} x \int_ {a} ^ {x} f (x, y) \mathrm{d} y = \int_ {a} ^ {b} \mathrm{d} y \int_ {y} ^ {b} f (x, y) \mathrm{d} x.
$$

6. 交换下列二次积分的积分次序:

(1) $\int_0^1\mathrm{d}y\int_0^y f(x,y)\mathrm{d}x;$

(2) $\int_0^2\mathrm{d}y\int_{y^2}^{2y}f(x,y)\mathrm{d}x;$

(3) $\int_0^1\mathrm{d}y\int_{-\sqrt{1 - y^2}}^{\sqrt{1 - y^2}}f(x,y)\mathrm{d}x;$

(4) $\int_{1}^{2}\mathrm{d}x\int_{2 - x}^{\sqrt{2x - x^2}}f(x,y)\mathrm{d}y;$

(5) $\int_{1}^{\mathrm{e}}\mathrm{d}x\int_{0}^{\ln x}f(x,y)\mathrm{d}y;$

(6) $\int_0^\pi \mathrm{d}x\int_{-\sin \frac{x}{2}}^{\sin x}f(x,y)\mathrm{d}y.$

7. 设平面薄片所占的闭区域 $D$ 由直线 $x + y = 2, y = x$ 和 $x$ 轴所围成，它的面密度 $\mu(x, y) = x^2 + y^2$ 求该薄片的质量.

8. 计算由四个平面 $x = 0, y = 0, x = 1, y = 1$ 所围成的柱体被平面 $z = 0$ 及 $2x + 3y + z = 6$ 截得的立体

的体积.

9. 求由平面 $x = 0, y = 0, x + y = 1$ 所围成的柱体被平面 $z = 0$ 及抛物面 $x^{2} + y^{2} = 6 - z$ 截得的立体的体积.

10. 求由曲面 $z = x^{2} + 2y^{2}$ 及 $z = 6 - 2x^{2} - y^{2}$ 所围成的立体的体积.

11. 画出积分区域, 把积分  $\iint_{D} f(x, y) \, dx \, dy$  表示为极坐标形式的二次积分, 其中积分区域 D 是

(1)  $\{(x,y)\mid x^{2}+y^{2}\leqslant a^{2}\}(a>0)$ ;

(2) $\{(x, y) \mid x^2 + y^2 \leqslant 2x\}$;

(3) $\{(x, y) \mid a^2 \leqslant x^2 + y^2 \leqslant b^2\}$, 其中 $0 < a < b$;

(4) $\{(x, y) \mid 0 \leqslant y \leqslant 1 - x, 0 \leqslant x \leqslant 1\}$.

12. 化下列二次积分为极坐标形式的二次积分:

(1) $\int_0^1\mathrm{d}x\int_0^1 f(x,y)\mathrm{d}y;$

(2) $\int_0^2\mathrm{d}x\int_{x}^{\sqrt{3} x}f(\sqrt{x^2 + y^2})\mathrm{d}y;$

(3) $\int_0^1\mathrm{d}x\int_{1 - x}^{\sqrt{1 - x^2}}f(x,y)\mathrm{d}y;$

(4) $\int_0^1\mathrm{d}x\int_0^{x^2}f(x,y)\mathrm{d}y.$

13. 把下列积分化为极坐标形式,并计算积分值:

(1) $\int_{0}^{2a}\mathrm{d}x\int_{0}^{\sqrt{2ax - x^2}}(x^2 +y^2)\mathrm{d}y;$

(2) $\int_{0}^{a}\mathrm{d}x\int_{0}^{x}\sqrt{x^{2} + y^{2}}\mathrm{d}y;$

(3) $\int_0^1\mathrm{d}x\int_{x^2}^x (x^2 +y^2)^{-\frac{1}{2}}\mathrm{d}y;$

(4) $\int_{0}^{a}\mathrm{d}y\int_{0}^{\sqrt{a^{2} - y^{2}}}(x^{2} + y^{2})\mathrm{d}x.$

14. 利用极坐标计算下列各题:

(1) $\iint_{D} \mathrm{e}^{x^2 + y^2} \, \mathrm{d}\sigma$, 其中 $D$ 是由圆周 $x^2 + y^2 = 4$ 所围成的闭区域;

(2) $\iint_{D} \ln (1 + x^2 + y^2) \, \mathrm{d}\sigma$，其中 $D$ 是由圆周 $x^2 + y^2 = 1$ 及坐标轴所围成的在第一象限内的闭区域；

(3) $\iint_{D} \arctan \frac{y}{x} \mathrm{d}\sigma$，其中 $D$ 是由圆周 $x^{2} + y^{2} = 4, x^{2} + y^{2} = 1$ 及直线 $y = 0, y = x$ 所围成的在第一象限内的闭区域.

15. 选用适当的坐标计算下列各题:

(1) $\iint_{D} \frac{x^2}{y^2} \mathrm{d}\sigma$，其中 $D$ 是由直线 $x = 2, y = x$ 及曲线 $xy = 1$ 所围成的闭区域；

(2) $\iint_{D} \sqrt{\frac{1 - x^2 - y^2}{1 + x^2 + y^2}} \, \mathrm{d}\sigma$, 其中 $D$ 是由圆周 $x^2 + y^2 = 1$ 及坐标轴所围成的在第一象限内的闭区域;

(3) $\iint_{D}(x^{2} + y^{2})\mathrm{d}\sigma$ ，其中 $D$ 是由直线 $y = x,y = x + a,y = a,y = 3a$ （$a > 0$）所围成的闭区域；

(4) $\iint_{D} \sqrt{x^2 + y^2} \, \mathrm{d}\sigma$, 其中 $D$ 是圆环形闭区域 $\{(x, y) \mid a^2 \leqslant x^2 + y^2 \leqslant b^2\}$;

(5) $\iint_{D} \sqrt{a^2 - x^2 - y^2} \, \mathrm{d}\sigma$, 其中 $D$ 是圆形闭区域 $\{(x, y) | x^2 + y^2 \leqslant ax \mid (a > 0)$.

16. 设平面薄片所占的闭区域 $D$ 由螺线 $\rho = 2\theta$ 上一段弧 $\left(0 \leqslant \theta \leqslant \frac{\pi}{2}\right)$ 与直线 $\theta = \frac{\pi}{2}$ 所围成, 它的

面密度为  $\mu(x,y)=x^{2}+y^{2}$ . 求这薄片的质量(图 10-27).

17. 求由平面 $y = 0, y = kx (k > 0), z = 0$ 以及球心在原点、半径为 $R$ 的上半球面所围成的在第 I 卦限内的立体的体积(图 10-28).

![](images/page_159_image_3.jpg)

<details>
<summary>text_image</summary>

θ=π/2
ρ=2θ
D
θ
O
A
</details>

图10-27

![](images/page_159_image_5.jpg)

<details>
<summary>text_image</summary>

z
O
α=arctan k
D
y
x
</details>

图10-28

18. 计算以 $xOy$ 面上的圆周 $x^{2} + y^{2} = ax (a > 0)$ 围成的闭区域为底，而以曲面 $z = x^{2} + y^{2}$ 为顶的曲顶柱体的体积.

\* 19. 作适当的变换,计算下列二重积分:

(1) $\iint_{D}(x - y)^{2}\sin^{2}(x + y)\mathrm{d}x\mathrm{d}y$ ，其中 $D$ 是平行四边形闭区域，它的四个顶点是 $(\pi ,0),(2\pi ,\pi)$ ，$(\pi ,2\pi)$ 和 $(0,\pi)$ ；
(2) $\iint_{D} x^{2} y^{2} \, \mathrm{d}x \, \mathrm{d}y$，其中 $D$ 是由两条双曲线 $xy = 1$ 和 $xy = 2$，直线 $y = x$ 和 $y = 4x$ 所围成的在第一象限内的闭区域；
(3) $\iint_{D} \mathrm{e}^{\frac{y}{x + y}} \mathrm{d}x \, \mathrm{d}y$，其中 $D$ 是由 $x$ 轴、$y$ 轴和直线 $x + y = 1$ 所围成的闭区域；
(4) $\iint_{D} \left( \frac{x^2}{a^2} + \frac{y^2}{b^2} \right) \, \mathrm{d}x \, \mathrm{d}y$，其中 $D = \left\{ (x, y) \mid \frac{x^2}{a^2} + \frac{y^2}{b^2} \leqslant 1 \right\}$.

\*20. 求由下列曲线所围成的闭区域 $D$ 的面积:

(1) D 是由曲线  $xy=4, xy=8, xy^{3}=5, xy^{3}=15$  所围成的第一象限部分的闭区域；

(2) D 是由曲线  $y=x^{3}, y=4x^{3}, x=y^{3}, x=4y^{3}$  所围成的第一象限部分的闭区域.

\* 21. 设闭区域 $D$ 是由直线 $x + y = 1, x = 0, y = 0$ 所围成，求证 $\iint_{D} \cos \left( \frac{x - y}{x + y} \right) \mathrm{d}x \mathrm{~d}y = \frac{1}{2} \sin 1.$

\* 22. 选取适当的变换,证明下列等式:

(1) $\iint_{D} f(x + y) \, \mathrm{d}x \, \mathrm{d}y = \int_{-1}^{1} f(u) \, \mathrm{d}u$，其中闭区域 $D = \{(x, y) \mid |x| + |y| \leqslant 1\}$;
(2) $\iint_{D} f(ax + by + c) \, \mathrm{d}x \, \mathrm{d}y = 2\int_{-1}^{1} \sqrt{1 - u^2} f(u \sqrt{a^2 + b^2} + c) \, \mathrm{d}u$，其中 $D = \{(x, y) | x^2 + y^2 \leqslant 1\}$，且 $a^2 + b^2 \neq 0$.