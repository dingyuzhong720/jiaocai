8. 设 $u = x^3 + y^3 + z^3 - 3xyz$，试问在怎样的点集上 $\operatorname{grad} u$ 分别满足:

(1) 垂直于 z 轴；

(2) 平行于 z 轴；

(3) 恒为零向量.

9. 设 $f(x, y)$ 可微, $l$ 是 $\mathbf{R}^2$ 上的一个确定向量. 倘若处处有 $f_l(x, y) \equiv 0$, 试问此函数 $f$ 有何特征?

10. 设 $f(x, y)$ 可微，$l_1$ 与 $l_2$ 是 $\mathbf{R}^2$ 上的一组线性无关向量。试证明:若 $f_{l_i}(x, y) \equiv 0 \quad (i = 1, 2)$，则 $f(x, y) \equiv \text{常数}$。

## § 4 泰勒公式与极值问题

## 一、高阶偏导数

由于 $z = f(x,y)$ 的偏导函数 $f_{x}(x,y),f_{y}(x,y)$ 仍然是自变量 $x$ 与 $y$ 的函数，如果它们关于 $x$ 与 $y$ 的偏导数也存在，则说函数 $f$ 具有二阶偏导数，二元函数的二阶偏导数有如下四种情形:

$$
\begin{array}{l} \frac {\partial}{\partial x} \Big (\frac {\partial z}{\partial x} \Big) = \frac {\partial^ {2} z}{\partial x ^ {2}} = f _ {x x} (x, y), \\ \frac {\partial}{\partial y} \Big (\frac {\partial z}{\partial x} \Big) = \frac {\partial^ {2} z}{\partial x \partial y} = f _ {x y} (x, y), \\ \frac {\partial}{\partial x} \Big (\frac {\partial z}{\partial y} \Big) = \frac {\partial^ {2} z}{\partial y \partial x} = f _ {y x} (x, y), \\ \frac {\partial}{\partial y} \Big (\frac {\partial z}{\partial y} \Big) = \frac {\partial^ {2} z}{\partial y ^ {2}} = f _ {y y} (x, y). \\ \end{array}
$$

类似地可定义更高阶的偏导数, $z=f(x,y)$ 的三阶偏导数共有八种情形,如

$$
\begin{array}{l} \frac {\partial}{\partial x} \Big (\frac {\partial^ {2} z}{\partial x ^ {2}} \Big) = \frac {\partial^ {3} z}{\partial x ^ {3}} = f _ {x ^ {3}} (x, y), \\ \frac {\partial}{\partial y} \Big (\frac {\partial^ {2} z}{\partial x ^ {2}} \Big) = \frac {\partial^ {3} z}{\partial x ^ {2} \partial y} = f _ {x ^ {2} y} (x, y), \\ \end{array}
$$

... ... ... ... ... ... ...

例1 求函数 $z = \mathrm{e}^{x + 2y}$ 的所有二阶偏导数和 $\frac{\partial^3z}{\partial y\partial x^2}$.

解 由于函数的一阶偏导数是

$$
\frac {\partial z}{\partial x} = \mathrm{e} ^ {x + 2 y}, \quad \frac {\partial z}{\partial y} = 2 \mathrm{e} ^ {x + 2 y}.
$$

因此有

$$
\begin{array}{l} \frac {\partial^ {2} z}{\partial x ^ {2}} = \frac {\partial}{\partial x} \Big (\frac {\partial z}{\partial x} \Big) = \frac {\partial}{\partial x} (\mathrm{e} ^ {x + 2 y}) = \mathrm{e} ^ {x + 2 y}, \\ \frac {\partial^ {2} z}{\partial x \partial y} = \frac {\partial}{\partial y} \Big (\frac {\partial z}{\partial x} \Big) = \frac {\partial}{\partial y} (\mathrm{e} ^ {x + 2 y}) = 2 \mathrm{e} ^ {x + 2 y}, \\ \end{array}
$$

$$
\frac {\partial^ {2} z}{\partial y \partial x} = \frac {\partial}{\partial x} \left(\frac {\partial z}{\partial y}\right) = \frac {\partial}{\partial x} (2 \mathrm{e} ^ {x + 2 y}) = 2 \mathrm{e} ^ {x + 2 y},
$$

$$
\frac {\partial^ {2} z}{\partial y ^ {2}} = \frac {\partial}{\partial y} \left(\frac {\partial z}{\partial y}\right) = \frac {\partial}{\partial y} (2 \mathrm{e} ^ {x + 2 y}) = 4 \mathrm{e} ^ {x + 2 y}
$$

和 $\frac{\partial^3z}{\partial y\partial x^2} = \frac{\partial}{\partial x}\left(\frac{\partial^2z}{\partial y\partial x}\right) = \frac{\partial}{\partial x}(2\mathrm{e}^{x + 2y}) = 2\mathrm{e}^{x + 2y}.$

例2 求函数 $z = \arctan \frac{y}{x}$ 的所有二阶偏导数.

解 因为 $\frac{\partial z}{\partial x} = \frac{-y}{x^2 + y^2}, \frac{\partial z}{\partial y} = \frac{x}{x^2 + y^2}$, 所以二阶偏导数为

$$
\frac {\partial^ {2} z}{\partial x ^ {2}} = \frac {\partial}{\partial x} \left(\frac {- y}{x ^ {2} + y ^ {2}}\right) = \frac {2 x y}{\left(x ^ {2} + y ^ {2}\right) ^ {2}},
$$

$$
\frac {\partial^ {2} z}{\partial x \partial y} = \frac {\partial}{\partial y} \left(\frac {- y}{x ^ {2} + y ^ {2}}\right) = - \frac {x ^ {2} - y ^ {2}}{\left(x ^ {2} + y ^ {2}\right) ^ {2}},
$$

$$
\frac {\partial^ {2} z}{\partial y \partial x} = \frac {\partial}{\partial x} \left(\frac {x}{x ^ {2} + y ^ {2}}\right) = - \frac {x ^ {2} - y ^ {2}}{\left(x ^ {2} + y ^ {2}\right) ^ {2}},
$$

$$
\frac {\partial^ {2} z}{\partial y ^ {2}} = \frac {\partial}{\partial y} \left(\frac {x}{x ^ {2} + y ^ {2}}\right) = \frac {- 2 x y}{\left(x ^ {2} + y ^ {2}\right) ^ {2}}.
$$

注 从上面两个例子看到,这些函数关于 x 和 y 的不同顺序的两个二阶偏导数都相等(这种既有关于 x 又有关于 y 的高阶偏导数称为混合偏导数),即

$$
\frac {\partial^ {2} z}{\partial x \partial y} = \frac {\partial^ {2} z}{\partial y \partial x}.
$$

但这个结论并不对任何函数都成立,例如函数

$$
f (x, y) = \left\{ \begin{array}{l l} x y \frac {x ^ {2} - y ^ {2}}{x ^ {2} + y ^ {2}}, & x ^ {2} + y ^ {2} \neq 0, \\ 0, & x ^ {2} + y ^ {2} = 0. \end{array} \right.
$$

它的一阶偏导数为

$$
f _ {x} (x, y) = \left\{ \begin{array}{l l} \frac {y (x ^ {4} + 4 x ^ {2} y ^ {2} - y ^ {4})}{(x ^ {2} + y ^ {2}) ^ {2}}, & x ^ {2} + y ^ {2} \neq 0, \\ 0, & x ^ {2} + y ^ {2} = 0, \end{array} \right.
$$

$$
f _ {y} (x, y) = \left\{ \begin{array}{l l} \frac {x (x ^ {4} - 4 x ^ {2} y ^ {2} - y ^ {4})}{(x ^ {2} + y ^ {2}) ^ {2}}, & x ^ {2} + y ^ {2} \neq 0, \\ 0, & x ^ {2} + y ^ {2} = 0. \end{array} \right.
$$

进而求 f 在  $(0,0)$  处关于 x 和 y 的两个不同顺序的混合偏导数, 得

$$
f _ {x y} (0, 0) = \lim _ {\Delta y \to 0} \frac {f _ {x} (0 , \Delta y) - f _ {x} (0 , 0)}{\Delta y} = \lim _ {\Delta y \to 0} \frac {- \Delta y}{\Delta y} = - 1,
$$

$$
f _ {y x} (0, 0) = \lim _ {\Delta x \to 0} \frac {f _ {y} (\Delta x , 0) - f _ {y} (0 , 0)}{\Delta x} = \lim _ {\Delta x \to 0} \frac {\Delta x}{\Delta x} = 1.
$$

由此看到, 这里的  $f(x,y)$  在原点处的两个二阶混合偏导数与求导顺序有关. 那么, 在什么条件下混合偏导数与求导顺序无关呢? 为此, 我们按定义先把  $f_{xy}(x_{0},y_{0})$  与  $f_{yx}(x_{0},y_{0})$  表示成极限形式. 由于

$$
f _ {x} (x, y) = \lim _ {\Delta x \to 0} \frac {f (x + \Delta x , y) - f (x , y)}{\Delta x},
$$

因此有

$$
\begin{array}{l} f _ {x y} (x _ {0}, y _ {0}) = \lim _ {\Delta y \to 0} \frac {f _ {x} (x _ {0} , y _ {0} + \Delta y) - f _ {x} (x _ {0} , y _ {0})}{\Delta y} \\ = \lim _ {\Delta y \to 0} \frac {1}{\Delta y} \left[ \lim _ {\Delta x \to 0} \frac {f (x _ {0} + \Delta x , y _ {0} + \Delta y) - f (x _ {0} , y _ {0} + \Delta y)}{\Delta x} - \right. \\ \lim _ {\Delta x \to 0} \frac {f (x _ {0} + \Delta x , y _ {0}) - f (x _ {0} , y _ {0})}{\Delta x} \\ = \lim _ {\Delta y \to 0} \lim _ {\Delta x \to 0} \frac {f (x _ {0} + \Delta x , y _ {0} + \Delta y) - f (x _ {0} , y _ {0} + \Delta y) - f (x _ {0} + \Delta x , y _ {0}) + f (x _ {0} , y _ {0})}{\Delta x \Delta y}. \tag {1} \\ \end{array}
$$

类似地有

$$
\begin{array}{l} f _ {y x} (x _ {0}, y _ {0}) \\ = \lim _ {\Delta x \to 0} \lim _ {\Delta y \to 0} \frac {f (x _ {0} + \Delta x , y _ {0} + \Delta y) - f (x _ {0} + \Delta x , y _ {0}) - f (x _ {0} , y _ {0} + \Delta y) + f (x _ {0} , y _ {0})}{\Delta x \Delta y}. \tag {2} \\ \end{array}
$$

为使 $f_{xy}(x_0, y_0) = f_{yx}(x_0, y_0)$ 成立，必须使(1)，(2)这两个累次极限相等，即可以交换累次极限的极限次序。下述定理给出了使极限(1)，(2)相等的一个充分条件。

定理17.7 若 $f_{xy}(x,y)$ 和 $f_{yx}(x,y)$ 都在点 $(x_0,y_0)$ 连续，则

$$
f _ {x y} (x _ {0}, y _ {0}) = f _ {y x} (x _ {0}, y _ {0}). \tag {3}
$$

证令

$$
F (\Delta x, \Delta y) = f (x _ {0} + \Delta x, y _ {0} + \Delta y) - f (x _ {0} + \Delta x, y _ {0}) - f (x _ {0}, y _ {0} + \Delta y) + f (x _ {0}, y _ {0}),
$$

$$
\varphi (x) = f (x, y _ {0} + \Delta y) - f (x, y _ {0}).
$$

于是有

$$
F (\Delta x, \Delta y) = \varphi (x _ {0} + \Delta x) - \varphi (x _ {0}). \tag {4}
$$

由于函数 $f$ 存在关于 $x$ 的偏导数，所以函数 $\varphi$ 可导.应用一元函数的中值定理，有

$$
\begin{array}{l} \varphi (x _ {0} + \Delta x) - \varphi (x _ {0}) \\ = \varphi^ {\prime} (x _ {0} + \theta_ {1} \Delta x) \Delta x \\ = \left[ f _ {x} (x _ {0} + \theta_ {1} \Delta x, y _ {0} + \Delta y) - f _ {x} (x _ {0} + \theta_ {1} \Delta x, y _ {0}) \right] \Delta x \quad (0 <   \theta_ {1} <   1). \\ \end{array}
$$

又由 $f_{x}$ 存在关于 $y$ 的偏导数，故对以 $y$ 为自变量的函数 $f_{x}(x_{0} + \theta_{1}\Delta x,y)$ 应用一元函数中值定理，又使上式化为

$$
\varphi (x _ {0} + \Delta x) - \varphi (x _ {0}) = f _ {x y} (x _ {0} + \theta_ {1} \Delta x, y _ {0} + \theta_ {2} \Delta y) \Delta x \Delta y \quad (0 <   \theta_ {1}, \theta_ {2} <   1).
$$

由(4)则有

$$
F (\Delta x, \Delta y) = f _ {x y} (x _ {0} + \theta_ {1} \Delta x, y _ {0} + \theta_ {2} \Delta y) \Delta x \Delta y \quad (0 <   \theta_ {1}, \theta_ {2} <   1). \tag {5}
$$

如果令

$$
\psi (y) = f (x _ {0} + \Delta x, y) - f (x _ {0}, y),
$$

则有

$$
F (\Delta x, \Delta y) = \psi (y _ {0} + \Delta y) - \psi (y _ {0}).
$$

用前面相同的方法,又可得到

$$
F (\Delta x, \Delta y) = f _ {y x} (x _ {0} + \theta_ {3} \Delta x, y _ {0} + \theta_ {4} \Delta y) \Delta x \Delta y \quad (0 <   \theta_ {3}, \theta_ {4} <   1). \tag {6}
$$

当  $\Delta x, \Delta y$  不为零时，由(5)，(6)两式得到

$$
f _ {x y} (x _ {0} + \theta_ {1} \Delta x, y _ {0} + \theta_ {2} \Delta y) = f _ {y x} (x _ {0} + \theta_ {3} \Delta x, y _ {0} + \theta_ {4} \Delta y) \quad (0 <   \theta_ {1}, \theta_ {2}, \theta_ {3}, \theta_ {4} <   1). \tag {7}
$$

由定理假设 $f_{xy}(x,y)$ 与 $f_{yx}(x,y)$ 在点 $(x_0,y_0)$ 连续，故当 $\Delta x\to 0,\Delta y\to 0$ 时，(7)式两边极限都存在而且相等，这就得到所要证明的(3)式. □

这个定理的结论对 $n$ 元函数的混合偏导数也成立. 如三元函数 $u = f(x, y, z)$, 若下述六个三阶混合偏导数

$$
f _ {x y z} (x, y, z), \quad f _ {y z x} (x, y, z), \quad f _ {z x y} (x, y, z),
$$

$$
f _ {x z y} (x, y, z), \quad f _ {y x z} (x, y, z), \quad f _ {z y x} (x, y, z)
$$

在某一点都连续,则在这一点六个混合偏导数都相等.同样,若二元函数 $z=f(x,y)$ 在点 $(x,y)$ 存在直到n阶的连续混合偏导数,则在这一点 $m\left(\leqslant n\right)$ 阶混合偏导数都与顺序无关.

今后除特别指出外,都假设相应阶数的混合偏导数连续,从而混合偏导数与求导顺序无关.

下面讨论复合函数的高阶偏导数. 设 z 是通过中间变量 x, y 而成为 s, t 的函数, 即

$$
z = f (x, y),
$$

其中 $x = \varphi (s,t),y = \psi (s,t)$ .若函数 $f,\varphi ,\psi$ 都具有连续的二阶偏导数，则作为复合函数的 $z$ 对 $s,t$ 同样存在二阶连续偏导数.具体计算如下:

$$
\frac {\partial z}{\partial s} = \frac {\partial z}{\partial x} \frac {\partial x}{\partial s} + \frac {\partial z}{\partial y} \frac {\partial y}{\partial s},
$$

$$
\frac {\partial z}{\partial t} = \frac {\partial z}{\partial x} \frac {\partial x}{\partial t} + \frac {\partial z}{\partial y} \frac {\partial y}{\partial t}.
$$

显然 $\frac{\partial z}{\partial s}$ 与 $\frac{\partial z}{\partial t}$ 仍是s,t的复合函数,其中 $\frac{\partial z}{\partial x},\frac{\partial z}{\partial y}$ 是x,y的函数, $\frac{\partial x}{\partial s},\frac{\partial x}{\partial t},\frac{\partial y}{\partial s},\frac{\partial y}{\partial t}$ 是s,t的函数.继续求z关于s,t的二阶偏导数

$$
\begin{array}{l} \frac {\partial^ {2} z}{\partial s ^ {2}} = \frac {\partial}{\partial s} \left(\frac {\partial z}{\partial x}\right) \frac {\partial x}{\partial s} + \frac {\partial z}{\partial x} \cdot \frac {\partial}{\partial s} \left(\frac {\partial x}{\partial s}\right) + \frac {\partial}{\partial s} \left(\frac {\partial z}{\partial y}\right) \frac {\partial y}{\partial s} + \frac {\partial z}{\partial y} \cdot \frac {\partial}{\partial s} \left(\frac {\partial y}{\partial s}\right) \\ = \left(\frac {\partial^ {2} z}{\partial x ^ {2}} \frac {\partial x}{\partial s} + \frac {\partial^ {2} z}{\partial x \partial y} \frac {\partial y}{\partial s}\right) \frac {\partial x}{\partial s} + \frac {\partial z}{\partial x} \frac {\partial^ {2} x}{\partial s ^ {2}} + \left(\frac {\partial^ {2} z}{\partial y \partial x} \frac {\partial x}{\partial s} + \frac {\partial^ {2} z}{\partial y ^ {2}} \frac {\partial y}{\partial s}\right) \frac {\partial y}{\partial s} + \frac {\partial z}{\partial y} \frac {\partial^ {2} y}{\partial s ^ {2}} \\ = \frac {\partial^ {2} z}{\partial x ^ {2}} \left(\frac {\partial x}{\partial s}\right) ^ {2} + 2 \frac {\partial^ {2} z}{\partial x \partial y} \frac {\partial x}{\partial s} \frac {\partial y}{\partial s} + \frac {\partial^ {2} z}{\partial y ^ {2}} \left(\frac {\partial y}{\partial s}\right) ^ {2} + \frac {\partial z}{\partial x} \frac {\partial^ {2} x}{\partial s ^ {2}} + \frac {\partial z}{\partial y} \frac {\partial^ {2} y}{\partial s ^ {2}}. \\ \end{array}
$$

同理可得

$$
\frac {\partial^ {2} z}{\partial t ^ {2}} = \frac {\partial^ {2} z}{\partial x ^ {2}} \left(\frac {\partial x}{\partial t}\right) ^ {2} + 2 \frac {\partial^ {2} z}{\partial x \partial y} \frac {\partial x}{\partial t} \frac {\partial y}{\partial t} + \frac {\partial^ {2} z}{\partial y ^ {2}} \left(\frac {\partial y}{\partial t}\right) ^ {2} + \frac {\partial z}{\partial x} \frac {\partial^ {2} x}{\partial t ^ {2}} + \frac {\partial z}{\partial y} \frac {\partial^ {2} y}{\partial t ^ {2}},
$$

$$
\begin{array}{l} \frac {\partial^ {2} z}{\partial s \partial t} = \frac {\partial^ {2} z}{\partial x ^ {2}} \frac {\partial x}{\partial s} \frac {\partial x}{\partial t} + \frac {\partial^ {2} z}{\partial x \partial y} \left(\frac {\partial x}{\partial s} \frac {\partial y}{\partial t} + \frac {\partial x}{\partial t} \frac {\partial y}{\partial s}\right) + \frac {\partial^ {2} z}{\partial y ^ {2}} \frac {\partial y}{\partial s} \frac {\partial y}{\partial t} + \frac {\partial z}{\partial x} \frac {\partial^ {2} x}{\partial s \partial t} + \frac {\partial z}{\partial y} \frac {\partial^ {2} y}{\partial s \partial t} \\ = \frac {\partial^ {2} z}{\partial t \partial s}. \\ \end{array}
$$

例3 设 $z = f\left(x, \frac{x}{y}\right)$, 求 $\frac{\partial^2 z}{\partial x^2}, \frac{\partial^2 z}{\partial x \partial y}$.

解 这里 z 是以 x 和 y 为自变量的复合函数, 它也可改写成如下形式:

$$
z = f (u, v), \quad u = x, \quad v = \frac {x}{y}.
$$

由复合函数求导公式有

$$
\frac {\partial z}{\partial x} = \frac {\partial f}{\partial u} \frac {\partial u}{\partial x} + \frac {\partial f}{\partial v} \frac {\partial v}{\partial x} = \frac {\partial f}{\partial u} + \frac {1}{y} \frac {\partial f}{\partial v}.
$$

注意,这里 $\frac{\partial f}{\partial u},\frac{\partial f}{\partial v}$ 仍是以u,v为中间变量,以x,y为自变量的复合函数.所以

$$
\begin{array}{l} \frac {\partial^ {2} z}{\partial x ^ {2}} = \frac {\partial}{\partial x} \left(\frac {\partial f}{\partial u} + \frac {1}{y} \frac {\partial f}{\partial v}\right) \\ = \frac {\partial^ {2} f}{\partial u ^ {2}} \frac {\partial u}{\partial x} + \frac {\partial^ {2} f}{\partial u \partial v} \frac {\partial v}{\partial x} + \frac {1}{y} \left(\frac {\partial^ {2} f}{\partial v \partial u} \frac {\partial u}{\partial x} + \frac {\partial^ {2} f}{\partial v ^ {2}} \frac {\partial v}{\partial x}\right) \\ = \frac {\partial^ {2} f}{\partial u ^ {2}} + \frac {2}{y} \frac {\partial^ {2} f}{\partial u \partial v} + \frac {1}{y ^ {2}} \frac {\partial^ {2} f}{\partial v ^ {2}}, \\ \frac {\partial^ {2} z}{\partial x \partial y} = \frac {\partial}{\partial y} \left(\frac {\partial f}{\partial u} + \frac {1}{y} \frac {\partial f}{\partial v}\right) \\ = \frac {\partial^ {2} f}{\partial u ^ {2}} \frac {\partial u}{\partial y} + \frac {\partial^ {2} f}{\partial u \partial v} \frac {\partial v}{\partial y} - \frac {1}{y ^ {2}} \frac {\partial f}{\partial v} + \frac {1}{y} \left(\frac {\partial^ {2} f}{\partial v \partial u} \frac {\partial u}{\partial y} + \frac {\partial^ {2} f}{\partial v ^ {2}} \frac {\partial v}{\partial y}\right) \\ = - \frac {x}{y ^ {2}} \frac {\partial^ {2} f}{\partial u \partial v} - \frac {x}{y ^ {3}} \frac {\partial^ {2} f}{\partial v ^ {2}} - \frac {1}{y ^ {2}} \frac {\partial f}{\partial v}. \\ \end{array}
$$

## 二、中值定理和泰勒公式

二元函数的中值公式和泰勒公式,与一元函数的拉格朗日公式和泰勒公式相仿,对于 n 元函数 $(n>2)$ 也有同样的公式,只是形式上更复杂一些.

在叙述有关定理之前,先介绍凸区域的概念.

若区域 $D$ 上任意两点的连线都含于 $D$, 则称 $D$ 为凸区域 (图17-9). 这就是说, 若 $D$ 为凸区域, 则对任意两点 $P_{1}(x_{1}, y_{1}), P_{2}(x_{2}, y_{2}) \in D$ 和一切 $\lambda$ ($0 \leqslant \lambda \leqslant 1$), 恒有

$$
P (x _ {1} + \lambda (x _ {2} - x _ {1}), y _ {1} + \lambda (y _ {2} - y _ {1})) \in D.
$$

定理17.8(中值定理) 设二元函数 f 在凸开域  $D \subset R^{2}$  上可微, 则对任意两点  $P(a, b)$ ,  $Q(a + h, b + k) \in D$ , 存在实数  $\theta (0 < \theta < 1)$ , 使得

$$
\begin{array}{l} f (a + h, b + k) - f (a, b) \\ = f _ {x} (a + \theta h, b + \theta k) h + f _ {y} (a + \theta h, b + \theta k) k. \tag {8} \\ \end{array}
$$

证令

![](images/page_133_image_1.jpg)

<details>
<summary>text_image</summary>

P₁
P
P₂
凸区域
P₁
P₂
非凸区域
</details>

图17-9

$$
\Phi (t) = f (a + t h, b + t k).
$$

因为 $D$ 是凸开域, 所以 $\Phi(t)$ 是定义在 $[0,1]$ 上的一元函数. 由定理中的条件知 $\Phi(t)$ 在 $[0,1]$ 上连续, 在 $(0,1)$ 上可微. 于是根据一元函数中值定理, 存在 $\theta (0 < \theta < 1)$, 使得

$$
\Phi (1) - \Phi (0) = \Phi^ {\prime} (\theta). \tag {9}
$$

由复合函数的求导法则

$$
\Phi^ {\prime} (\theta) = f _ {x} (a + \theta h, b + \theta k) h + f _ {y} (a + \theta h, b + \theta k) k. \tag {10}
$$

由于 D 为凸区域, 所以  $(a+\theta h, b+\theta k) \in D$ , 故由 (9), (10) 即得所要证明的 (8) 式.

注 若 $D$ 是闭凸域, 且对 $D$ 上任意两点 $P_{1}(x_{1}, y_{1}), P_{2}(x_{2}, y_{2})$ 及任意 $\lambda (0 < \lambda < 1)$, 都有

$$
P (x _ {1} + \lambda (x _ {2} - x _ {1}), y _ {1} + \lambda (y _ {2} - y _ {1})) \in \mathrm{int} D,
$$

则对 $D$ 上连续，$\operatorname{int} D$ 内可微的函数 $f$，只要 $P, Q \in D$，也存在 $\theta \in (0,1)$，使(8)式成立.

例如 $D$ 是圆域 $\{(x,y) \mid (x - \xi)^2 + (y - \eta)^2 \leqslant r^2\}$, $f$ 在 $D$ 上连续, 在 $\operatorname{int} D$ 内可微, 则必有 (8) 式成立. 倘若 $D$ 是矩形区域 $[a, b] \times [c, d]$, 那就不能保证对 $D$ 上任意两点 $P, Q$ 都有 (8) 式成立 (为什么?).

公式(8)也称为二元函数(在凸域上)的中值公式. 它与定理17.3的中值公式(12)相比较, 差别在于这里的中值点 $(a+\theta h, b+\theta k)$ 是在P, Q的连线上, 而在定理17.3中 $\theta_{1}$ 与 $\theta_{2}$ 可以不相等.

推论 若函数 $f$ 在区域 $D$ 上存在偏导数，且

$$
f _ {x} = f _ {y} \equiv 0,
$$

则 f 在区域 D 上为常量函数.

请读者作为练习自行证明(注意本推论与§1习题16(2)两者证明的差别).

例 4 对  $f(x,y)=\frac{1}{\sqrt{x^{2}-2xy+1}}$  应用微分中值定理, 证明存在  $\theta(0<\theta<1)$ , 使得

$$
1 - \sqrt {2} = \sqrt {2} (1 - 3 \theta) (1 - 2 \theta + 3 \theta^ {2}) ^ {- 3 / 2}.
$$

证 将 $1 - \sqrt{2} = \sqrt{2}(1 - 3\theta)(1 - 2\theta + 3\theta^2)^{-3/2}$ 改写成

$$
\frac {1 - \sqrt {2}}{\sqrt {2}} = (1 - 3 \theta) (1 - 2 \theta + 3 \theta^ {2}) ^ {- 3 / 2},
$$

左边恰好是 $f(1,0) - f(0,1) = \frac{1}{\sqrt{2}} -1$ ，所以尝试在凸区域 $D = \{(x,y)\mid x^2 +y^2\leqslant 1\}$ 上，对两点 $P_{1}(1,0)$ 与 $P_{2}(0,1)$ 应用微分中值定理.

因为当 $x^{2} + y^{2}\leqslant 1$ 时， $x^{2} - 2xy + 1 > 0$ ，所以函数 $f$ 在 $D$ 上连续，并且

$$
f _ {x} = - \frac {x - y}{\left(x ^ {2} - 2 x y + 1\right) ^ {3 / 2}}, \quad f _ {y} = \frac {x}{\left(x ^ {2} - 2 x y + 1\right) ^ {3 / 2}}
$$

也在 $D$ 上连续. $P_{1}, P_{2} \in D$, 根据微分中值定理, 存在 $\theta (0 < \theta < 1)$, 使得

$$
\begin{array}{l} \frac {1}{\sqrt {2}} - 1 = f (1, 0) - f (0, 1) = f _ {x} (0 + \theta , 1 - \theta) \cdot 1 + f _ {y} (0 + \theta , 1 - \theta) \cdot (- 1) \\ = - \frac {\theta - (1 - \theta)}{\left[ \theta^ {2} - 2 \theta (1 - \theta) + 1 \right] ^ {3 / 2}} - \frac {\theta}{\left[ \theta^ {2} - 2 \theta (1 - \theta) + 1 \right] ^ {3 / 2}} \\ = (1 - 3 \theta) (1 - 2 \theta + 3 \theta^ {2}) ^ {- 3 / 2}. \\ \end{array}
$$

定理17.9（泰勒定理）若函数 $f$ 在点 $P_0(x_0,y_0)$ 的某邻域 $U(P_0)$ 上有直到 $n + 1$ 阶的连续偏导数，则对 $U(P_0)$ 上任一点 $(x_0 + h,y_0 + k)$，存在相应的 $\theta \in (0,1)$，使得

$$
\begin{array}{l} f (x _ {0} + h, y _ {0} + k) = f (x _ {0}, y _ {0}) + \left(h \frac {\partial}{\partial x} + k \frac {\partial}{\partial y}\right) f (x _ {0}, y _ {0}) + \frac {1}{2 !} \left(h \frac {\partial}{\partial x} + k \frac {\partial}{\partial y}\right) ^ {2} f (x _ {0}, y _ {0}) + \dots + \\ \frac {1}{n !} \left(h \frac {\partial}{\partial x} + k \frac {\partial}{\partial y}\right) ^ {n} f (x _ {0}, y _ {0}) + \frac {1}{(n + 1) !} \left(h \frac {\partial}{\partial x} + k \frac {\partial}{\partial y}\right) ^ {n + 1} f (x _ {0} + \theta h, y _ {0} + \theta k). \tag {11} \\ \end{array}
$$

(11)式称为二元函数f在点 $P_{0}$ 的n阶泰勒公式,其中

$$
\left(h \frac {\partial}{\partial x} + k \frac {\partial}{\partial y}\right) ^ {m} f (x _ {0}, y _ {0}) = \sum_ {i = 0} ^ {m} \mathrm{G} _ {m} ^ {i} \frac {\partial^ {m}}{\partial x ^ {i} \partial y ^ {m - i}} f (x _ {0}, y _ {0}) h ^ {i} k ^ {m - i}.
$$

证 与定理17.8的证明一样.作函数

$$
\Phi (t) = f (x _ {0} + t h, y _ {0} + t k).
$$

由定理的假设,一元函数  $\Phi(t)$  在  $[0,1]$  上满足一元函数泰勒定理条件,于是有

$$
\Phi (1) = \Phi (0) + \frac {\Phi^ {\prime} (0)}{1 !} + \frac {\Phi^ {\prime \prime} (0)}{2 !} + \dots + \frac {\Phi^ {(n)} (0)}{n !} + \frac {\Phi^ {(n + 1)} (\theta)}{(n + 1) !} \quad (0 <   \theta <   1). \tag {12}
$$

应用复合函数求导法则,可求得  $\Phi(t)$  的各阶导数:

$$
\Phi^ {(m)} (t) = \left(h \frac {\partial}{\partial x} + k \frac {\partial}{\partial y}\right) ^ {m} f (x _ {0} + t h, y _ {0} + t k) \quad (m = 1, 2, \dots , n + 1).
$$

当 $t = 0$ 时, 则有

$$
\Phi^ {(m)} (0) = \left(h \frac {\partial}{\partial x} + k \frac {\partial}{\partial y}\right) ^ {m} f (x _ {0}, y _ {0}) \quad (m = 1, 2, \dots , n), \tag {13}
$$

$$
\Phi^ {(n + 1)} (\theta) = \left(h \frac {\partial}{\partial x} + k \frac {\partial}{\partial y}\right) ^ {n + 1} f (x _ {0} + \theta h, y _ {0} + \theta k). \tag {14}
$$

将(13)，(14)式代入(12)式就得到所求之泰勒公式(11).

易见,中值公式(8)正是泰勒公式(11)在 n=0 时的特殊情形.

若在公式(11)中只要求余项 $R_{n} = o(\rho^{n})(\rho = \sqrt{h^{2} + k^{2}})$，则仅需 $f$ 在 $U(P_0)$ 内存在直到 $n$ 阶连续偏导数，便有

$$
\begin{array}{l} f (x _ {0} + h, y _ {0} + k) \\ = f (x _ {0}, y _ {0}) + \sum_ {P = 1} ^ {n} \frac {1}{P !} \left(h \frac {\partial}{\partial x} + k \frac {\partial}{\partial y}\right) ^ {P} f (x _ {0}, y _ {0}) + o (\rho^ {n}). \tag {15} \\ \end{array}
$$

例 5 求  $f(x, y) = x^{y}$  在点 (1,4) 的泰勒公式（到二阶为止），并用它计算  $(1.08)^{3.96}$ .

解 由于 $x_0 = 1, y_0 = 4, n = 2$，因此有

$$
\begin{array}{l} f (x, y) = x ^ {y}, \quad f (1, 4) = 1, \\ f _ {x} (x, y) = y x ^ {y - 1}, \quad f _ {x} (1, 4) = 4, \\ f _ {y} (x, y) = x ^ {y} \ln x, \quad f _ {y} (1, 4) = 0, \\ f _ {x ^ {2}} (x, y) = y (y - 1) x ^ {y - 2}, \quad f _ {x ^ {2}} (1, 4) = 1 2, \\ f _ {x y} (x, y) = x ^ {y - 1} + y x ^ {y - 1} \ln x, \quad f _ {x y} (1, 4) = 1. \\ f _ {y ^ {2}} (x, y) = x ^ {y} (\ln x) ^ {2}, \quad f _ {y ^ {2}} (1, 4) = 0. \\ \end{array}
$$

将它们代入泰勒公式(15)，即得

$$
x ^ {y} = 1 + 4 (x - 1) + 6 (x - 1) ^ {2} + (x - 1) (y - 4) + o (\rho^ {2}).
$$

若略去余项,并让 x=1.08, y=3.96, 则有

$$
(1. 0 8) ^ {3. 9 6} \approx 1 + 4 \times 0. 0 8 + 6 \times 0. 0 8 ^ {2} - 0. 0 8 \times 0. 0 4 = 1. 3 5 5 2.
$$

与 §1 例 7 的结果相比较, 这是更接近于精确值 (1.356 307…) 的近似值. 因为微分近似式相当于现在的一阶泰勒公式.

## 三、极值问题

多元函数的极值问题是多元函数微分学的重要应用,这里仍以二元函数为例进行讨论.

定义1 设函数 $f$ 在点 $P_0(x_0, y_0)$ 的某邻域 $U(P_0)$ 上有定义. 若对于任何点 $P(x, y) \in U(P_0)$, 成立不等式

$$
f (P) \leqslant f (P _ {0}) \quad (\text {或} f (P) \geqslant f (P _ {0}))  ,
$$

则称函数 f 在点  $P_{0}$  取得极大（或极小）值，点  $P_{0}$  称为 f 的极大（或极小）值点。极大值、极小值统称极值。极大值点、极小值点统称极值点。

注 这里所讨论的极值点只限于定义域的内点.

例6 设 $f(x, y) = 2x^{2} + y^{2}, g(x, y) = \sqrt{1 - x^{2} - y^{2}}, h(x, y) = xy$. 由定义直接知道，坐标原点(0,0)是 $f$ 的极小值点，是 $g$ 的极大值点，但不是 $h$ 的极值点. 这是因为对任何点 $(x, y)$，恒有 $f(x, y) \geqslant f(0, 0) = 0$; 对任何 $(x, y) \in \{(x, y) | x^{2} + y^{2} \leqslant 1\}$，恒有 $g(x, y) \leqslant g(0, 0) = 1$; 而对于函数 $h$，在原点的任意小邻域上，既含有使 $h(x, y) > 0$ 的 I，Ⅲ象限中的点，又含有使 $h(x, y) < 0$ 的 II，IV象限中的点，所以 $h(0, 0) = 0$ 既不是极大值又不是极小值.

由定义可见, 若 f 在点  $(x_{0}, y_{0})$  取得极值, 则当固定  $y = y_{0}$  时, 一元函数  $f(x, y_{0})$  必定在  $x = x_{0}$  取相同的极值. 同理, 一元函数  $f(x_{0}, y)$  在  $y = y_{0}$  也取相同的极值. 于是得到二元函数取极值的必要条件如下:

定理17.10(极值必要条件) 若函数 $f$ 在点 $P_0(x_0, y_0)$ 存在偏导数，且在 $P_0$ 取得极值，则有

$$
f _ {x} (x _ {0}, y _ {0}) = 0, \quad f _ {y} (x _ {0}, y _ {0}) = 0. \tag {16}
$$

反之, 若函数 f 在点  $P_{0}$  满足 (16), 则称点  $P_{0}$  为 f 的稳定点. 定理 17.10 指出: 若 f 存在偏导数, 则其极值点必是稳定点. 但稳定点并不都是极值点, 如例 6 中的函数 h, 原点为其稳定点, 但它在原点并不取得极值.

与一元函数的情形相同,函数在偏导数不存在的点上也有可能取得极值.例如 $f(x,y)=\sqrt{x^{2}+y^{2}}$ 在原点没有偏导数,但 $f(0,0)=0$ 是f的极小值.

为了讨论二元函数 f 在点  $P_{0}(x_{0}, y_{0})$  取得极值的充分条件, 我们假定 f 具有二阶连续偏导数, 并记

$$
\boldsymbol {H} _ {f} (P _ {0}) = \left( \begin{array}{l l} f _ {x x} (P _ {0}) & f _ {x y} (P _ {0}) \\ f _ {y x} (P _ {0}) & f _ {y y} (P _ {0}) \end{array} \right) = \left( \begin{array}{l l} f _ {x x} & f _ {x y} \\ f _ {y x} & f _ {y y} \end{array} \right) _ {P _ {0}} \tag {17}
$$

它称为f在 $P_{0}$ 的黑塞(Hesse)矩阵①.

定理17.11（极值充分条件）设二元函数 $f$ 在点 $P_0(x_0,y_0)$ 的某邻域 $U(P_0)$ 上具有二阶连续偏导数，且 $P_0$ 是 $f$ 的稳定点.则当 $\pmb{H}_f(P_0)$ 是正定矩阵时， $f$ 在点 $P_0$ 取得极小值；当 $\pmb{H}_f(P_0)$ 是负定矩阵时， $f$ 在点 $P_0$ 取得极大值；当 $\pmb{H}_f(P_0)$ 是不定矩阵时， $f$ 在点$P_0$ 不取极值.

证 由 $f$ 在点 $P_0$ 的二阶泰勒公式，并注意到条件 $f_{x}(P_{0}) = f_{y}(P_{0}) = 0$ ，有

$$
\begin{array}{l} f (x, y) - f (x _ {0}, y _ {0}) \\ = \frac {1}{2} (\Delta x, \Delta y) \boldsymbol {H} _ {f} (P _ {0}) (\Delta x, \Delta y) ^ {\mathrm{T}} + o (\Delta x ^ {2} + \Delta y ^ {2}). \\ \end{array}
$$

由于 $H_{f}(P_{0})$ 正定，所以对任何 $(\Delta x, \Delta y) \neq (0, 0)$，恒使二次型

$$
Q (\Delta x, \Delta y) = (\Delta x, \Delta y) H _ {f} (P _ {0}) (\Delta x, \Delta y) ^ {\mathrm{T}} > 0.
$$

因此存在一个与  $\Delta x, \Delta y$  无关的正数  $q^{②}$ ，使得

$$
Q (\Delta x, \Delta y) \geqslant 2 q (\Delta x ^ {2} + \Delta y ^ {2}).
$$

从而对于充分小的 $U(P_0)$，只要 $(x,y) \in U(P_0)$，就有

$$
\begin{array}{l} f (x, y) - f \left(x _ {0}, y _ {0}\right) \geqslant q \left(\Delta x ^ {2} + \Delta y ^ {2}\right) + o \left(\Delta x ^ {2} + \Delta y ^ {2}\right) \\ = (\Delta x ^ {2} + \Delta y ^ {2}) (q + o (1)) \geqslant 0, \\ \end{array}
$$

即 f 在点  $(x_{0}, y_{0})$  取得极小值.

同理可证  $H_{f}(P_{0})$  为负定矩阵时，f 在点  $P_{0}$  取得极大值.

最后，当 $H_{f}(P_{0})$ 不定时，$f$ 在点 $P_{0}$ 不取极值。这是因为倘若 $f$ 取极值（例如取极大值），则沿任何过点 $P_{0}$ 的直线 $x = x_{0} + t\Delta x, y = y_{0} + t\Delta y, f(x,y) = f(x_{0} + t\Delta x,y_{0} + t\Delta y) = \varphi(t)$ 在 $t = 0$ 亦取极大值。由一元函数取极值的充分条件，$\varphi''(0) > 0$ 是不可能的（否则 $\varphi$ 在 $t = 0$ 将取极小值），故 $\varphi''(0) \leqslant 0$。而

$$
\begin{array}{l} \varphi^ {\prime} (t) = f _ {x} \Delta x + f _ {y} \Delta y, \\ \varphi^ {\prime \prime} (t) = f _ {x x} \Delta x ^ {2} + 2 f _ {x y} \Delta x \Delta y + f _ {y y} \Delta y ^ {2}, \\ \varphi^ {\prime \prime} (0) = (\Delta x, \Delta y) \boldsymbol {H} _ {f} \left(P _ {0}\right) (\Delta x, \Delta y) ^ {\mathrm{T}}. \\ \end{array}
$$

这表明 $H_{f}(P_{0})$ 必须是半负定的.同理，倘若 $f$ 取极小值，则将导致 $H_{f}(P_{0})$ 必须是半正定的.也就是说,当f在点 $P_{0}$ 取得极值时, $H_{f}(P_{0})$ 必须是半正定或半负定矩阵,但这与假设相矛盾.

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 关于黑塞矩阵的一般形式,将在第二十三章里介绍.</span></small>

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">② 因为 $Q(\Delta x, \Delta y) / (\Delta x^2 + \Delta y^2) = (u, v)\boldsymbol{H}_f(P_0)(u, v)^{\mathrm{T}} = \Phi(u, v)$，其中</span></small>

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">$u = \Delta x / \sqrt{\Delta x^2 + \Delta y^2}, v = \Delta y / \sqrt{\Delta x^2 + \Delta y^2}.$</span></small>

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">显然，$\Phi(u, v)$ 是 $(u, v)$ 的连续函数。由于 $u^2 + v^2 = 1$，因此 $\Phi$ 在单位圆 $u^2 + v^2 = 1$ 上必有最小值 $2q \geqslant 0$。又因 $(u, v) \neq (0, 0)$，故 $q > 0$。</span></small>

根据半正定或半负定对称阵所属主子行列式的符号规则, 定理 17.11 又可写成如下比较实用的形式.

若函数 f 如定理 17.11 所设.  $P_{0}$  是 f 的稳定点, 则有:

(i) 当 $f_{xx}(P_0) > 0, (f_{xx}f_{yy} - f_{xy}^2)(P_0) > 0$ 时，$f$ 在点 $P_0$ 取得极小值；
(ii) 当  $f_{xx}(P_{0})<0$ ,  $(f_{xx}f_{yy}-f_{xy}^{2})(P_{0})>0$  时, f 在点  $P_{0}$  取得极大值;
(iii) 当 $(f_{xx}f_{yy}-f_{xy}^{2})(P_{0})<0$ 时，f在点 $P_{0}$ 不能取得极值；
(iv) 当 $(f_{xx}f_{yy}-f_{xy}^{2})(P_{0})=0$ 时,不能肯定f在点 $P_{0}$ 是否取得极值.

例 7 求  $f(x,y)=x^{2}+5y^{2}-6x+10y+6$  的极值.

解 由方程组

$$
\left\{ \begin{array}{l} f _ {x} = 2 x - 6 = 0, \\ f _ {y} = 1 0 y + 1 0 = 0 \end{array} \right.
$$

得 f 的稳定点  $P_{0}(3,-1)$ ，由于

$$
f _ {x x} (P _ {0}) = 2, \quad f _ {x y} (P _ {0}) = 0,
$$

$$
f _ {y y} (P _ {0}) = 1 0, \quad (f _ {x x} f _ {y y} - f _ {x y} ^ {2}) (P _ {0}) = 2 0.
$$

因此 $f$ 在点 $P_0$ 取得极小值 $f(3, -1) = -8$. 又因 $f$ 处处存在偏导数，故 $(3, -1)$ 为 $f$ 的惟一极值点. □

例 8 讨论  $f(x,y)=x^{2}+xy$  是否存在极值.

解 由方程组 $f_{x} = 2x + y = 0, f_{y} = x = 0$ 得稳定点为原点.

因 $f_{xx}f_{yy} - f_{xy}^{2} = -1 < 0$ ，故原点不是 $f$ 的极值点.又因 $f$ 处处可微，所以 $f$ 没有极值点

例 9 讨论  $f(x,y)=(y-x^{2})(y-2x^{2})$  在原点是否取得极值.

解 容易验证原点是 $f$ 的稳定点，且在原点 $f_{xx} f_{yy} - f_{xy}^2 = 0$ ，故由定理17.11无法判定 $f$ 在原点是否取到极值.但由于当 $x^{2} < y < 2x^{2}$ 时 $f(x,y) < 0$ ，而当 $y > 2x^{2}$ 或 $y < x^{2}$ 时，$f(x,y) > 0$ （图17-10），所以函数 $f$ 不可能在原点取得极值.

由极值的定义还知道,极值只是函数f在某一点的局部性概念.要想获得函数f在区域D上的最大值和最小值(由上一章知道在有界闭区域上的连续函数一定

![](images/page_137_image_22.jpg)

<details>
<summary>text_image</summary>

y
y=2x²
-
+
-
y=x²
+
+
O
x
</details>

图17-10

能取得最大与最小值),与一元函数的问题一样,必须考察函数f在所有稳定点、无偏导点以及属于区域的界点上的函数值 $^{①}$ .

比较这些值,其中最大者(或最小者)即为函数f在D上的最大(小)值.

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 如果属于区域的界点成一曲线  $F(x,y)=0$ ，求函数 f 在此曲线上的最大（小）值一般要用下一章的条件极值方法去解决。倘若该曲线有一显式方程  $y=\varphi(x)$ ，则上述问题归结为求一元函数  $g(x)=f(x,\varphi(x))$  的极值。</span></small>

例 10 证明: 圆的所有外切三角形中, 以正三角形的面积为最小.

证 设圆的半径为 $a$. 任一外切三角形为 $\triangle ABC$, 三切点处的半径两两相夹的中心角分别为 $\alpha, \beta, \gamma$. 其中 $\gamma = 2\pi - (\alpha + \beta)$ (图17-11). 容易得出 $\triangle ABC$ 的面积表达式为

$$
\begin{array}{l} S = a ^ {2} \left(\tan \frac {\alpha}{2} + \tan \frac {\beta}{2} + \tan \frac {\gamma}{2}\right) \\ = a ^ {2} \left(\tan \frac {\alpha}{2} + \tan \frac {\beta}{2} - \tan \frac {\alpha + \beta}{2}\right). \\ \end{array}
$$

![](images/page_138_image_4.jpg)

<details>
<summary>text_image</summary>

A
α
β
γ
B
C
</details>

图17-11

其中 $0 < \alpha, \beta < \pi$. 为求得稳定点，令

$$
\left\{ \begin{array}{l} S _ {\alpha} = \frac {1}{2} a ^ {2} \Big (\sec^ {2} \frac {\alpha}{2} - \sec^ {2} \frac {\alpha + \beta}{2} \Big) = 0, \\ S _ {\beta} = \frac {1}{2} a ^ {2} \Big (\sec^ {2} \frac {\beta}{2} - \sec^ {2} \frac {\alpha + \beta}{2} \Big) = 0. \end{array} \right.
$$

在定义域内上述关于 $\alpha, \beta$ 的方程组仅有惟一解 $\alpha = \beta = \frac{2}{3}\pi, \gamma = 2\pi - (\alpha + \beta) = \frac{2}{3}\pi$.

为了应用定理 17.11, 求得在稳定点  $(\alpha, \beta) = \left(\frac{2}{3}\pi, \frac{2}{3}\pi\right)$  处的二阶偏导数为

$$
S _ {\alpha \alpha} = 4 \sqrt {3} a ^ {2}, S _ {\alpha \beta} = 2 \sqrt {3} a ^ {2}, S _ {\beta \beta} = 4 \sqrt {3} a ^ {2}.
$$

由于 $S_{\alpha \alpha} > 0, S_{\alpha \alpha} S_{\beta \beta} - S_{\alpha \beta}^{2} = 36a^{4} > 0$ ，因此 $S$ 在此稳定点上取得极小值.

因为面积函数 S 在定义域内处处存在偏导数, 又因此时  $\alpha = \beta = \gamma$ , 而具体问题存在最小值, 故外切三角形中以正三角形的面积为最小. ☐

例 11(最小二乘法问题) 设通过观测或实验得到一列点 $(x_{i}, y_{i}), i=1,2,\cdots,n$ . 它们大体上在一条直线上, 即大体上可用直线方程来反映变量 x 与 y 之间的对应关系(参见图 17-12). 现要确定一直线使得与这 n 个点的偏差平方和最小(最小二乘方).

解 设所求直线方程为

$$
y = a x + b,
$$

所测得的 n 个点为  $(x_{i}, y_{i})$  ( $i = 1, 2, \cdots, n$ ). 现要确定 a, b, 使得

![](images/page_138_image_17.jpg)

<details>
<summary>text_image</summary>

y
y=ax+b
ax_i+b-y_i
(x_i, y_i)
O
x
</details>

图17-12

$$
f (a, b) = \sum_ {i = 1} ^ {n} \left(a x _ {i} + b - y _ {i}\right) ^ {2}
$$

为最小.为此,令

$$
\left\{ \begin{array}{l} f _ {a} = 2 \sum_ {i = 1} ^ {n} x _ {i} (a x _ {i} + b - y _ {i}) = 0, \\ f _ {b} = 2 \sum_ {i = 1} ^ {n} (a x _ {i} + b - y _ {i}) = 0, \end{array} \right.
$$

把这组关于 a, b 的线性方程加以整理, 得

$$
\left\{ \begin{array}{l} a \sum_ {i = 1} ^ {n} x _ {i} ^ {2} + b \sum_ {i = 1} ^ {n} x _ {i} = \sum_ {i = 1} ^ {n} x _ {i} y _ {i}, \\ a \sum_ {i = 1} ^ {n} x _ {i} + b n = \sum_ {i = 1} ^ {n} y _ {i}. \end{array} \right.
$$

求此方程组的解,即得 $f(a,b)$ 的稳定点①

$$
\overline {{a}} = \frac {n \sum_ {i = 1} ^ {n} x _ {i} y _ {i} - \left(\sum_ {i = 1} ^ {n} x _ {i}\right) \left(\sum_ {i = 1} ^ {n} y _ {i}\right)}{n \sum_ {i = 1} ^ {n} x _ {i} ^ {2} - \left(\sum_ {i = 1} ^ {n} x _ {i}\right) ^ {2}},
$$

$$
\bar {b} = \frac {\left(\sum_ {i = 1} ^ {n} x _ {i} ^ {2}\right) \left(\sum_ {i = 1} ^ {n} y _ {i}\right) - \left(\sum_ {i = 1} ^ {n} x _ {i} y _ {i}\right) \left(\sum_ {i = 1} ^ {n} x _ {i}\right)}{n \sum_ {i = 1} ^ {n} x _ {i} ^ {2} - \left(\sum_ {i = 1} ^ {n} x _ {i}\right) ^ {2}}.
$$

为进一步确定该点是极小值点,我们计算得

$$
A = f _ {a a} = 2 \sum_ {i = 1} ^ {n} x _ {i} ^ {2} > 0,
$$

$$
B = f _ {a b} = 2 \sum_ {i = 1} ^ {n} x _ {i},
$$

$$
C = f _ {b b} = 2 n,
$$

$$
D = A C - B ^ {2} = 4 n \sum_ {i = 1} ^ {n} x _ {i} ^ {2} - 4 \Big (\sum_ {i = 1} ^ {n} x _ {i} \Big) ^ {2} > 0,
$$

从而根据定理 17.11,  $f(a,b)$  在点  $(\bar{a},\bar{b})$  取得极小值. 由实际问题可知此极小值为最小值. □

## 习题 17.4

1. 求下列函数的高阶偏导数:

(1) $z = x^{4} + y^{4} - 4x^{2}y^{2}$, 所有二阶偏导数；
(2) $z = \mathrm{e}^{x}(\cos y + x\sin y)$, 所有二阶偏导数；

(3)  $z = x \ln(xy)$ ,  $\frac{\partial^{3}z}{\partial x^{2}\partial y}$ ,  $\frac{\partial^{3}z}{\partial x\partial y^{2}}$ ;

(4)  $u = xyz e^{x + y + z}, \frac{\partial^{p + q + r} u}{\partial x^{p} \partial y^{q} \partial z^{r}};$

(5)  $z=f(xy^{2},x^{2}y)$ ，所有二阶偏导数；

(6)  $u = f(x^{2} + y^{2} + z^{2})$ , 所有二阶偏导数;

(7)  $z = f \left( x + y, xy, \frac{x}{y} \right)$ ,  $z_{x}, z_{xx}, z_{xy}$ .

2. 设 $u = f(x, y), x = r\cos \theta, y = r\sin \theta$. 证明:

① 当  $x_{1}, x_{2}, \cdots, x_{n}$  不全相等时，可由数学归纳法证得  $n \sum_{i=1}^{n} x_{i}^{2} - \left( \sum_{i=1}^{n} x_{i} \right)^{2} > 0.$

$$
\frac {\partial^ {2} u}{\partial r ^ {2}} + \frac {1}{r} \frac {\partial u}{\partial r} + \frac {1}{r ^ {2}} \frac {\partial^ {2} u}{\partial \theta^ {2}} = \frac {\partial^ {2} u}{\partial x ^ {2}} + \frac {\partial^ {2} u}{\partial y ^ {2}}.
$$

3. 设  $u = f(r)$ ,  $r^{2} = x_{1}^{2} + x_{2}^{2} + \cdots + x_{n}^{2}$ . 证明:

$$
\frac {\partial^ {2} u}{\partial x _ {1} ^ {2}} + \frac {\partial^ {2} u}{\partial x _ {2} ^ {2}} + \dots + \frac {\partial^ {2} u}{\partial x _ {n} ^ {2}} = \frac {\mathrm{d} ^ {2} u}{\mathrm{d} r ^ {2}} + \frac {n - 1}{r} \frac {\mathrm{d} u}{\mathrm{d} r}.
$$

4. 设  $v=\frac{1}{r}g\left(t-\frac{r}{c}\right)$ ，c 为常数， $r=\sqrt{x^{2}+y^{2}+z^{2}}$ . 证明:

$$
v _ {x x} + v _ {y y} + v _ {z z} = \frac {1}{c ^ {2}} v _ {t t}.
$$

5. 证明定理 17.8 的推论.

6. 通过对 $F(x, y) = \sin x \cos y$ 施用中值定理，证明对某 $\theta \in (0,1)$，有

$$
\frac {3}{4} = \frac {\pi}{3} \cos \frac {\pi \theta}{3} \cos \frac {\pi \theta}{6} - \frac {\pi}{6} \sin \frac {\pi \theta}{3} \sin \frac {\pi \theta}{6}.
$$

7. 求下列函数在指定点处的泰勒公式:

(1) $f(x,y)=\sin(x^{2}+y^{2})$ 在点(0,0)(到二阶为止);
(2) $f(x,y)=\frac{x}{y}$ 在点(1,1)(到三阶为止);
(3)  $f(x,y)=\ln(1+x+y)$  在点  $(0,0)$ ;
(4) $f(x,y)=2x^{2}-xy-y^{2}-6x-3y+5$ 在点 $(1,-2)$.

8. 求下列函数的极值点:

(1)  $z = 3axy - x^{3} - y^{3}$  (a > 0);
(2)  $z = x^{2} - xy + y^{2} - 2x + y$ ;
(3)  $z = e^{2x}(x + y^{2} + 2y)$ .

9. 求下列函数在指定范围内的最大值与最小值:

(1) $z = x^{2} - y^{2},\{(x,y)\mid x^{2} + y^{2}\leqslant 4\}$;
(2) $z = x^{2} - xy + y^{2},\{(x,y)||x| + |y|\leqslant 1\}$;
(3) $z = \sin x + \sin y - \sin (x + y),\{(x,y)\mid x\geqslant 0,y\geqslant 0,x + y\leqslant 2\pi \}$.

10. 在已知周长为 2p 的一切三角形中, 求出面积为最大的三角形.

11. 在 $xy$ 平面上求一点，使它到三直线 $x = 0, y = 0$ 及 $x + 2y - 16 = 0$ 的距离平方和最小.

12. 已知平面上 $n$ 个点的坐标分别是

$$
A _ {1} (x _ {1}, y _ {1}), A _ {2} (x _ {2}, y _ {2}), \dots , A _ {n} (x _ {n}, y _ {n}),
$$

试求一点,使它与这 n 个点距离的平方和最小.

13. 证明: 函数 $u = \frac{1}{2a\sqrt{\pi t}}\mathrm{e}^{-\frac{(x - b)^2}{4a^2t}}$ ($a, b$ 为常数) 满足热传导方程

$$
\frac {\partial u}{\partial t} = a ^ {2} \frac {\partial^ {2} u}{\partial x ^ {2}}.
$$

14. 证明: 函数 $u = \ln \sqrt{(x - a)^2 + (y - b)^2}$ ($a, b$ 为常数) 满足拉普拉斯方程

$$
\frac {\partial^ {2} u}{\partial x ^ {2}} + \frac {\partial^ {2} u}{\partial y ^ {2}} = 0.
$$

15. 证明: 若函数  $u = f(x, y)$  满足拉普拉斯方程

$$
\frac {\partial^ {2} u}{\partial x ^ {2}} + \frac {\partial^ {2} u}{\partial y ^ {2}} = 0,
$$

则函数  $v=f\left(\frac{x}{x^{2}+y^{2}},\frac{y}{x^{2}+y^{2}}\right)$  也满足此方程.

16. 设函数  $u = \varphi(x + \psi(y))$ ，证明

$$
\frac {\partial u}{\partial x} \frac {\partial^ {2} u}{\partial x \partial y} = \frac {\partial u}{\partial y} \frac {\partial^ {2} u}{\partial x ^ {2}}.
$$

17. 设 $f_{x}, f_{y}$ 和 $f_{yx}$ 在点 $(x_0, y_0)$ 的某邻域上存在，$f_{yx}$ 在点 $(x_0, y_0)$ 连续，证明 $f_{xy}(x_0, y_0)$ 也存在，且 $f_{xy}(x_0, y_0) = f_{yx}(x_0, y_0)$.

18. 设 $f_{x}, f_{y}$ 在点 $(x_{0}, y_{0})$ 的某邻域上存在且在点 $(x_{0}, y_{0})$ 可微，则有

$$
f _ {x y} (  x _ {0}  , y _ {0}  ) = f _ {y x} (  x _ {0}  , y _ {0}  ).
$$

19. 设

$$
u = \left| \begin{array}{c c c} 1 & 1 & 1 \\ x & y & z \\ x ^ {2} & y ^ {2} & z ^ {2} \end{array} \right|.
$$

求:(1) $u_{x}+u_{y}+u_{z}$; (2) $xu_{x}+yu_{y}+zu_{z}$; (3) $u_{xx}+u_{yy}+u_{zz}$.

20. 设 $f(x, y, z) = Ax^2 + By^2 + Cz^2 + Dxy + Eyz + Fzx$，试按 $h, k, l$ 的正数幂展开 $f(x + h, y + k, z + l)$.

## 第十七章总练习题

1. 设 $f(x, y, z) = x^2y + y^2z + z^2x$，证明

$$
f _ {x} + f _ {y} + f _ {z} = (x + y + z) ^ {2}.
$$

2. 求函数

$$
f (x, y) = \left\{ \begin{array}{l l} \frac {x ^ {3} - y ^ {3}}{x ^ {2} + y ^ {2}}, & x ^ {2} + y ^ {2} \neq 0, \\ 0, & x ^ {2} + y ^ {2} = 0 \end{array} \right.
$$

在原点的偏导数 $f_{x}(0,0)$ 与 $f_{y}(0,0)$，并考察 $f(x,y)$ 在 $(0,0)$ 的可微性.

3. 设

$$
u = \left| \begin{array}{c c c c} 1 & 1 & \dots & 1 \\ x _ {1} & x _ {2} & \dots & x _ {n} \\ x _ {1} ^ {2} & x _ {2} ^ {2} & \dots & x _ {n} ^ {2} \\ \vdots & \vdots & & \vdots \\ x _ {1} ^ {n - 1} & x _ {2} ^ {n - 1} & \dots & x _ {n} ^ {n - 1} \end{array} \right|,
$$

证明:（1） $\sum_{k = 1}^{n}\frac{\partial u}{\partial x_k} = 0$ （2） $\sum_{k = 1}^{n}x_{k}\frac{\partial u}{\partial x_{k}} = \frac{n(n - 1)}{2} u.$

4. 设函数  $f(x,y)$  具有连续的 n 阶偏导数, 试证函数  $g(t)=f(a+ht,b+kt)$  的 n 阶导数

$$
\frac {\mathrm{d} ^ {n} g (t)}{\mathrm{d} t ^ {n}} = \left(h \frac {\partial}{\partial x} + k \frac {\partial}{\partial y}\right) ^ {n} f (a + h t, b + k t).
$$

5. 设

$$
\varphi (x, y, z) = \left| \begin{array}{l l l} a + x & b + y & c + z \\ d + z & e + x & f + y \\ g + y & h + z & k + x \end{array} \right|,
$$

求 $\frac{\partial^{2}\varphi}{\partial x^{2}}$ .

6. 设

$$
\Phi (x, y, z) = \left| \begin{array}{c c c} f _ {1} (x) & f _ {2} (x) & f _ {3} (x) \\ g _ {1} (y) & g _ {2} (y) & g _ {3} (y) \\ h _ {1} (z) & h _ {2} (z) & h _ {3} (z) \end{array} \right|,
$$

求 $\frac{\partial^{3}\Phi}{\partial x\partial y\partial z}.$

7. 设函数 $u = f(x, y)$ 在 $\mathbf{R}^2$ 上有 $u_{xy} = 0$，试求 $u$ 关于 $x, y$ 的函数式.

8. 设 f 在点  $P_{0}(x_{0}, y_{0})$  可微，且在  $P_{0}$  给定了 n 个向量  $l_{i}, i=1,2,\cdots,n$ ，相邻两个向量之间的夹角为  $\frac{2\pi}{n}$ . 证明

$$
\sum_ {i = 1} ^ {n} f _ {l _ {i}} (P _ {0}) = 0.
$$

![](images/page_142_image_7.jpg)

## 第十七章综合自测题

## §1 隐函数

## 一、隐函数的概念

在这之前我们所接触的函数,其表达式大多是自变量的某个算式,如

$$
y = x ^ {2} + 1, u = \mathrm{e} ^ {x y z} (\sin x y + \sin y z + \sin z x).
$$

这种形式的函数称为显函数.但在不少场合常会遇到另一种形式的函数,其自变量与因变量之间的对应法则由一个方程式所确定,通常称为隐函数.例如: $x^{3}+y^{3}+z^{3}-3xy=0$ .

设 $E \subset \mathbf{R}^2$，函数 $F: E \to \mathbf{R}$. 对于方程

$$
F (x, y) = 0, \tag {1}
$$

如果存在集合 $I, J \subset \mathbf{R}$, 对任何 $x \in I$, 有惟一确定的 $y \in J$, 使得 $(x, y) \in E$, 且满足方程 (1), 则称方程 (1) 确定了一个定义在 $I$ 上, 值域含于 $J$ 的隐函数. 若把它记为

$$
y = f (x) ①, x \in I, y \in J,
$$

则成立恒等式

$$
F (x, f (x)) \equiv 0, x \in I.
$$

例如方程

$$
x y + y - 1 = 0
$$

能确定一个定义在 $(-∞,-1)∪(-1,+∞)$ 上的隐函数 $y=f(x)$ . 如果从方程中把y解出, 这个函数也可表示为显函数形式

$$
y = \frac {1}{1 + x}.
$$

又如圆方程 $x^{2} + y^{2} = 1$ 能确定一个定义在 $[-1,1]$ 上，函数值不小于0的隐函数 $y = \sqrt{1 - x^2}$；又能确定另一个定义在 $[-1,1]$ 上，函数值不大于0的隐函数 $y = -\sqrt{1 - x^2}$。

所以隐函数必须在指出确定它的方程以及 x, y 的取值范围后才有意义. 当然在不产生误解的情况下, 其取值范围也可不必一一指明. 此外, 还需指出:

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 这里只表示存在着定义在 I 上、值域在 J 内的函数 f，它并不意味着 y 能否用 x 的某一显式来表示.</span></small>

(i) 并不是任一方程都能确定出隐函数, 如方程

$$
x ^ {2} + y ^ {2} + c = 0.
$$

当 c>0 时, 就不能确定任何函数  $f(x)$ , 使得

$$
x ^ {2} + \left[ f (x) \right] ^ {2} + c \equiv 0.
$$

而只有当 $c \leqslant 0$ 时, 才能确定隐函数. 因此我们必须研究方程(1)在什么条件下才能确定隐函数.

（ii）倘若方程(1)能确定隐函数,一般并不都像前面的一些例子那样,能从方程中解出y,并用自变量x的算式来表示(即使 $F(x,y)$ 是初等函数).例如,对于方程

$$
y - x - \frac {1}{2} \sin y = 0.
$$

确实存在一个定义在 $(-\infty, +\infty)$ 上的函数 $f(x)$，使得

$$
f (x) - x + \frac {1}{2} \sin f (x) \equiv 0,
$$

但函数 $f(x)$ 却无法用 $x$ 的算式来表达. 因此, 在一般情况下, 我们主要考虑方程(1)能否确定隐函数以及这个隐函数的连续性、可微性, 而不管它是否能用显式表示.

## 二、隐函数存在性条件的分析

上一段给出了隐函数的定义, 现在的问题是: 当函数  $F(x,y)$  满足哪些条件时, 由方程(1)能确定隐函数  $y=f(x)$ , 并且该隐函数具有连续、可微等性质? 为此我们先作一些分析.

首先, $y=f(x)$ 可以看作曲面 $z=F(x,y)$ 与坐标平面z=0的交线,因此隐函数要存在,至少该交集不能为空,即存在 $P_{0}(x_{0},y_{0})$ ,使 $F(x_{0},y_{0})=0,y_{0}=f(x_{0})$ .

![](images/page_144_image_14.jpg)

<details>
<summary>text_image</summary>

z
z=F(x,y)
O
y=f(x)
P₀
l
x
y
</details>

图18-1

其次，方程(1)能在点 $P_0$ 附近确定一个连续函数，表现为上述交集是一条通过点$P_{0}$ 的连续曲线段（图18-1).如果曲面 $z = F(x,y)$ 在点 $P_0$ 存在切平面，且切平面与坐标平面 $z = 0$ 相交于直线 $l$ ，那么曲面 $z = F(x,y)$ 在点 $P_0$ 附近亦必与坐标平面 $z = 0$ 相交（其交线在点 $P_0$ 处的切线正是 $l$ ).为此，设 $F$ 在点 $P_0$ 可微，且

$$
(F _ {x} (P _ {0}), F _ {y} (P _ {0})) \neq (0, 0), \tag {2}
$$

则可使上述切平面存在,并满足与 z=0 相交成直线的要求.

如果进一步要求上述隐函数 $y = f(x)$ （或 $x = g(y)$ ）在点 $P_0$ 可微，则在 $F$ 可微的假设下，通过方程(1)在 $P_0$ 处对 $x$ 求导，依链式法则得到

$$
F _ {x} (P _ {0}) + F _ {y} (P _ {0}) \cdot \frac {\mathrm{d} y}{\mathrm{d} x} \Big | _ {x = x _ {0}} = 0. \tag {3}
$$

当 $F_{y}(P_{0})\neq 0$ 时，可由(3)解出

$$
\frac {\mathrm{d} y}{\mathrm{d} x} \Bigg | _ {x = x _ {0}} = - \frac {F _ {x} (P _ {0})}{F _ {y} (P _ {0})}. \tag {4}
$$

类似地，当 $F_{x}(P_{0})\neq 0$ 时，通过方程(1)对 $y$ 求导后也可解出

$$
\frac {\mathrm{d} x}{\mathrm{d} y} \Big | _ {y = y _ {0}} = - \frac {F _ {y} (P _ {0})}{F _ {x} (P _ {0})}.
$$

由此可见,条件(2)不仅对于隐函数的存在性,而且对于隐函数的求导同样是重要的.

## 三、隐函数定理

定理 18.1(隐函数存在惟一性定理) 若函数  $F(x,y)$  满足下列条件:

(i) F 在以  $P_{0}(x_{0}, y_{0})$  为内点的某一区域  $D \subset R^{2}$  上连续；
(ii)  $F(x_{0}, y_{0}) = 0$  (通常称为初始条件);
(iii) F 在 D 上存在连续的偏导数  $F_{y}(x,y)$ ;
(iv)  $F_{y}(x_{0}, y_{0}) \neq 0.$

则

$1^{\circ}$ 存在点 $P_{0}$ 的某邻域 $U(P_{0})\subset D$ ，在 $U(P_0)$ 上方程 $F(x,y) = 0$ 惟一地决定了一个定义在某区间 $(x_0 - \alpha ,x_0 + \alpha)$ 上的（隐）函数 $y = f(x)$ ，使得当 $x\in (x_0 - \alpha ,x_0 + \alpha)$ 时，$(x,f(x))\in U(P_0)$ ，且 $F(x,f(x))\equiv 0,f(x_0) = y_0$

$2^{\circ}f(x)$ 在 $(x_0 - \alpha ,x_0 + \alpha)$ 上连续.

证 先证隐函数 f 的存在性与惟一性.

由条件(iv)，不妨设 $F_{y}(x_{0},y_{0}) > 0$ （若 $F_{y}(x_{0},y_{0}) < 0$ ，则可讨论 $-F(x,y) = 0$ ).由条件(iii) $F_{y}$ 在 $D$ 上连续，由连续函数的局部保号性，存在点 $P_0$ 的某一闭的方邻域$[x_0 - \beta ,x_0 + \beta ]\times [y_0 - \beta ,y_0 + \beta ]\subset D$ ，使得在其上每一点都有 $F_{y}(x,y) > 0.$ 因而，对每个固定的 $x\in [x_0 - \beta ,x_0 + \beta ],F(x,y)$ 作为 $y$ 的一元函数，必定在 $[y_0 - \beta ,y_0 + \beta ]$ 上严格增且连续.由初始条件(ii)可知

$$
F (x _ {0}, y _ {0} - \beta) <   0, F (x _ {0}, y _ {0} + \beta) > 0.
$$

再由 $F$ 的连续性条件(i)，又可知道 $F(x,y_0 - \beta)$ 与 $F(x,y_0 + \beta)$ 在 $[x_0 - \beta ,x_0 + \beta ]$ 上也是连续的.因此由保号性存在 $\alpha >0$ （ $\alpha \leqslant \beta$ )，当 $x\in (x_0 - \alpha ,x_0 + \alpha)$ 时恒有

$$
F (x, y _ {0} - \beta) <   0, F (x, y _ {0} + \beta) > 0.
$$

如图 18-2 所示, 在矩形  $ABB'A'$  的 AB 边上 F 取负值, 在  $A'B'$  边上 F 取正值. 因此对

$(x_0 - \alpha, x_0 + \alpha)$ 上每个固定值 $\bar{x}$, 同样有 $F(\bar{x}, y_0 - \beta) < 0, F(\bar{x}, y_0 + \beta) > 0$. 根据前已指出的 $F(\bar{x}, y)$ 在 $[y_0 - \beta, y_0 + \beta]$ 上严格增且连续, 由介值性定理知存在惟一的 $\bar{y} \in (y_0 - \beta, y_0 + \beta)$, 满足 $F(\bar{x}, \bar{y}) = 0$. 由 $\bar{x}$ 在 $(x_0 - \alpha, x_0 + \alpha)$ 中的任意性, 这就证明了存在惟一的一个隐函数 $y = f(x)$, 它的定义域为 $(x_0 - \alpha, x_0 + \alpha)$, 值域含于 $(y_0 - \beta, y_0 + \beta)$. 若记

$$
\begin{array}{l} U (P _ {0}) = (x _ {0} - \alpha , x _ {0} + \alpha) \\ \times (y _ {0} - \beta , y _ {0} + \beta), \\ \end{array}
$$

则  $y=f(x)$  在  $U(P_{0})$  上满足结论  $1^{\circ}$  的各项要求.

再证明 f 的连续性.

![](images/page_145_chart_23.jpg)

<details>
<summary>contour</summary>

| Point | X-coordinate | Y-coordinate |
| --- | --- | --- |
| P0 | x0 | y0 |
| A | \(x0-\alpha\) | — |
| B | \(x0+\alpha\) | — |
</details>

图18-2

对于 $(x_{0}-\alpha,x_{0}+\alpha)$ 上的任意点 $\bar{x},\bar{y}=f(\bar{x})$ .由上述结论可知 $y_{0}-\beta<\bar{y}<y_{0}+\beta$ .任给 $\varepsilon>$

0, 且  $\varepsilon$  足够小, 使得

$$
y _ {0} - \beta \leqslant \bar {y} - \varepsilon <   \bar {y} <   \bar {y} + \varepsilon \leqslant y _ {0} + \beta .
$$

由 $F(\bar{x},\bar{y}) = 0$ 及 $F(x,y)$ 关于 $y$ 严格递增，可得 $F(\bar{x},\bar{y} -\varepsilon) <   0,F(\bar{x},\bar{y} +\varepsilon) > 0.$ 根据保号性，知存在 $\bar{x}$ 的某邻域 $(\bar{x} -\delta ,\bar{x} +\delta)\subset (x_0 - \alpha ,x_0 + \alpha)$ ，使得当 $x\in (\bar{x} -\delta ,\bar{x} +\delta)$ 时同样有

$$
F (x, \bar {y} - \varepsilon) <   0, F (x, \bar {y} + \varepsilon) > 0.
$$

因此存在惟一的 $y$，使得 $F(x, y) = 0$，即 $y = f(x)$，$|y - \bar{y}| < \varepsilon$。这就证明了当 $|x - \bar{x}| < \delta$ 时，$|f(x) - f(\bar{x})| < \varepsilon$，即 $f(x)$ 在 $\bar{x}$ 连续。由 $\bar{x}$ 的任意性，可得 $f(x)$ 在 $(x_0 - \alpha, x_0 + \alpha)$ 上连续。

注1 定理18.1的条件仅仅是充分的.例如方程 $y^{3} - x^{3} = 0$ ，在点 $(0,0)$ 不满足条件

(iv) $(F_{y}(0,0)=0)$ ，但它仍能确定惟一的连续函数 y=x。当然，由于条件(iv)不满足，往往导致定理结论的失效，例如图18-3所示的双纽线，其方程为

$$
F (x, y) = \left(x ^ {2} + y ^ {2}\right) ^ {2} - x ^ {2} + y ^ {2} = 0.
$$

由于 $F(0,0) = 0,F$ 与 $F_{y} = 4y(x^{2} + y^{2}) + 2y$ 均连续，故满足定理条件(i)，(ii)，(iii).但因 $F_{y}(0,0) = 0$ ，致使在原点的无论怎样小的邻域内都不可能存在惟一的隐函数.

![](images/page_146_image_10.jpg)

<details>
<summary>text_image</summary>

y
O
x
</details>

图18-3

注2 在定理证明过程中, 条件(iii)和(iv)只是用来保证存在 $P_{0}$ 的某一邻域, 在此邻域上 $F$ 关于变量 $y$ 是严格单调的. 因此对于本定理所要证明的结论来说, 可以把这两个条件减弱为“$F$ 在 $P_{0}$ 的某一邻域上关于 $y$ 严格单调”. 现在采用较强的条件 (iii) 和 (iv), 只是为了在实际应用中便于检验.

注3 如果把定理的条件(iii)和(iv)改为 $F_{x}(x,y)$ 连续，且 $F_{x}(x_{0},y_{0})\neq 0.$ 这时结论是存在惟一的连续函数 $x = g(y)$

定理18.2（隐函数可微性定理）设 $F(x,y)$ 满足隐函数存在惟一性定理中的条件(i)—(iv)，又设在 $D$ 上还存在连续的偏导数 $F_{x}(x,y)$，则由方程(1)所确定的隐函数$y = f(x)$ 在其定义域 $(x_0 - \alpha ,x_0 + \alpha)$ 上有连续导函数，且

$$
f ^ {\prime} (x) = - \frac {F _ {x} (x , y)}{F _ {y} (x , y)}. \tag {5}
$$

证 设 $x$ 与 $x + \Delta x$ 都属于 $(x_0 - \alpha, x_0 + \alpha)$，它们所对应的函数值 $y = f(x)$ 与 $y + \Delta y = f(x + \Delta x)$ 都含于 $(y_0 - \beta, y_0 + \beta)$ 内。由于

$$
F (x, y) = 0, F (x + \Delta x, y + \Delta y) = 0,
$$

因此由 $F_{x}, F_{y}$ 的连续性以及二元函数中值定理，有

$$
\begin{array}{l} 0 = F (x + \Delta x, y + \Delta y) - F (x, y) \\ = F _ {x} (x + \theta \Delta x, y + \theta \Delta y) \Delta x + F _ {y} (x + \theta \Delta x, y + \theta \Delta y) \Delta y, \\ \end{array}
$$

其中 $0 < \theta < 1$ .因而

$$
\frac {\Delta y}{\Delta x} = - \frac {F _ {x} (x + \theta \Delta x , y + \theta \Delta y)}{F _ {y} (x + \theta \Delta x , y + \theta \Delta y)}.
$$

注意到上式右端是连续函数 $F_{x}(x,y), F_{y}(x,y)$ 与 $f(x)$ 的复合函数，而且 $F_{y}(x,y)$ 在 $U(P_0)$ 上不等于零，故有

$$
f ^ {\prime} (x) = \lim _ {\Delta x \to 0} \frac {\Delta y}{\Delta x} = - \frac {F _ {x} (x , y)}{F _ {y} (x , y)}
$$

且 $f^{\prime}(x)$ 在 $(x_0 - \alpha, x_0 + \alpha)$ 上连续.

像在第二段里我们所分析的那样,若已知方程(1)确实存在连续可微的隐函数,则可对方程(1)应用复合函数求导法得到隐函数的导数,因为把 $F(x,f(x))$ 看作 $F(x,y)$ 与 $y=f(x)$ 的复合函数时,有

$$
F _ {x} (x, y) + F _ {y} (x, y) y ^ {\prime} = 0. \tag {6}
$$

当 $F_{y}(x,y)\neq 0$ 时，由它可立刻推得与(5)相同的结果.

对于隐函数的高阶导数,可用和上面同样的方法来求得,这时只要假定函数 F 存在相应阶数的连续高阶偏导数.例如,要计算  $y''$ , 只需对恒等式(6)继续应用复合函数求导法则,便得

$$
F _ {x x} (x, y) + F _ {x y} (x, y) y ^ {\prime} + \left[ F _ {y x} (x, y) + F _ {y y} (x, y) y ^ {\prime} \right] y ^ {\prime} + F _ {y} (x, y) y ^ {\prime \prime} = 0.
$$

再把(5)的结果代入上式,整理后得到

$$
\begin{array}{l} y ^ {\prime \prime} = - \frac {1}{F _ {y}} (F _ {x x} + 2 F _ {x y} y ^ {\prime} + F _ {y y} y ^ {\prime 2}) \\ = \frac {2 F _ {x} F _ {y} F _ {x y} - F _ {y} ^ {2} F _ {x x} - F _ {x} ^ {2} F _ {y y}}{F _ {y} ^ {3}}, \tag {7} \\ \end{array}
$$

当然它也可由公式(5)直接对 x 求导数而得到.

隐函数极值问题 利用隐函数求导公式(5)，(7)，得到求由 $F(x,y)=0$ 确定的隐函数 $y=f(x)$ 极值的方法如下:

首先，求 $y'$ 为零的点（驻点）$A(\widetilde{x},\widetilde{y})$ ，即方程组 $F(x,y) = 0,F_{x}(x,y) = 0$ 的解；其次，因在 $A$ 处 $F_{x} = 0$ ，从而使(7)式简化为 $y''|_A = -\frac{F_{xx}}{F_y}\Bigg|_A$ ；最后根据极值判别的第二充分条件，当 $y''|_A <   0$ （或 $>0$ )时，隐函数 $y = f(x)$ 在 $\widetilde{x}$ 处取极大值（极小值） $\widetilde{y}$

最后,我们可以类似地理解由方程  $F(x_{1},x_{2},\cdots,x_{n},y)=0$  所确定的 n 元隐函数的概念,并叙述下列 n 元隐函数的惟一存在与连续可微性定理.

## 定理18.3 若

(i) 函数  $F(x_{1}, x_{2}, \cdots, x_{n}, y)$  在以点  $P_{0}(x_{1}^{0}, x_{2}^{0}, \cdots, x_{n}^{0}, y^{0})$  为内点的区域  $D \subset R^{n+1}$  上连续；

(ii)  $F(x_{1}^{0}, x_{2}^{0}, \cdots, x_{n}^{0}, y^{0}) = 0$ ;

(iii) 偏导数  $F_{x_{1}}, F_{x_{2}}, \cdots, F_{x_{n}}, F_{y}$  在 D 上存在且连续；

(iv)  $F_{y}(x_{1}^{0}, x_{2}^{0}, \cdots, x_{n}^{0}, y^{0}) \neq 0.$

则

$1^{\circ}$ 存在点 $P_{0}$ 的某邻域 $U(P_{0})\subset D$ ，在 $U(P_{0})$ 上方程 $F(x_{1},\dots ,x_{n},y) = 0$ 惟一地确定了一个定义在 $Q_{0}(x_{1}^{0},x_{2}^{0},\dots ,x_{n}^{0})$ 的某邻域 $U(Q_0)\subset \mathbf{R}^n$ 上的 $n$ 元连续函数（隐函数） $y = f(x_{1},\dots ,x_{n})$ ，使得当 $(x_{1},x_{2},\dots ,x_{n})\in U(Q_{0})$ 时，

$$
(x _ {1}, x _ {2}, \dots , x _ {n}, f (x _ {1}, x _ {2}, \dots , x _ {n})) \in U (P _ {0}),
$$

且  $F(x_{1},\cdots,x_{n},f(x_{1},\cdots,x_{n}))\equiv0,$

$$
y ^ {0} = f (x _ {1} ^ {0}, \dots , x _ {n} ^ {0});
$$

$2^{\circ}\quad y=f(x_{1},\cdots,x_{n})$ 在 $U(Q_{0})$ 上有连续偏导数 $f_{x_1},f_{x_2},\cdots,f_{x_n}$ ，而且

$$
f _ {x _ {1}} = - \frac {F _ {x _ {1}}}{F _ {y}}, f _ {x _ {2}} = - \frac {F _ {x _ {2}}}{F _ {y}}, \dots , f _ {x _ {n}} = - \frac {F _ {x _ {n}}}{F _ {y}}.
$$

## 四、隐函数求导举例

例1 设方程

$$
F (x, y) = y - x - \frac {1}{2} \sin y = 0. \tag {8}
$$

由于 $F$ 及其偏导数 $F_{x}, F_{y}$ 在平面上任一点都连续，且

$$
F (0, 0) = 0,
$$

$$
F _ {y} (x, y) = 1 - \frac {1}{2} \cos y > 0.
$$

故依定理 18.1 和 18.2, 方程(8)确定了一个连续可导隐函数  $y=f(x)$ , 按公式(5), 其导数为

$$
f ^ {\prime} (x) = - \frac {F _ {x} (x , y)}{F _ {y} (x , y)} = \frac {1}{1 - \frac {1}{2} \cos y} = \frac {2}{2 - \cos y}. \tag {$\square$}
$$

例 2 讨论笛卡儿(Descartes)叶形线(图 18-4)

$$
x ^ {3} + y ^ {3} - 3 a x y = 0 \tag {9}
$$

所确定的隐函数  $y=f(x)$  的一阶与二阶导数, 并求隐函数的极值.

解 令 $F(x, y) = x^3 + y^3 - 3axy$ ($a > 0$). 在曲线 (9) 上使 $F_y = 3(y^2 - ax) = 0$ 的点是 $O(0, 0)$ 和 $B(\sqrt[3]{4}a, \sqrt[3]{2}a)$. 除这两点外，方程 (9) 在其他各点附近都能确定隐函数 $y = f(x)$.

由公式(5)，得到

$$
y ^ {\prime} = - \frac {F _ {x}}{F _ {y}} = - \frac {3 (x ^ {2} - a y)}{3 (y ^ {2} - a x)} = \frac {a y - x ^ {2}}{y ^ {2} - a x}.
$$

由于

$$
2 F _ {x} F _ {y} F _ {x y} = - 5 4 a (y ^ {2} - a x) (x ^ {2} - a y),
$$

$$
F _ {y} ^ {2} F _ {x x} = 5 4 x (y ^ {2} - a x) ^ {2}, \quad F _ {x} ^ {2} F _ {y y} = 5 4 y (x ^ {2} - a y) ^ {2},
$$

于是根据公式(7)，有

$$
\begin{array}{l} y ^ {\prime \prime} = \frac {2 F _ {x} F _ {y} F _ {x y} - F _ {y} ^ {2} F _ {x x} - F _ {x} ^ {2} F _ {y y}}{F _ {y} ^ {3}} \\ = \frac {- 5 4 \left[ a \left(y ^ {2} - a x\right) \left(x ^ {2} - a y\right) + x \left(y ^ {2} - a x\right) ^ {2} + y \left(x ^ {2} - a y\right) ^ {2} \right]}{2 7 \left(y ^ {2} - a x\right) ^ {3}} \\ = \frac {- 2 \left[ - 3 a x ^ {2} y ^ {2} + x y (x ^ {3} + y ^ {3} + a ^ {3}) \right]}{(y ^ {2} - a x) ^ {3}} = \frac {- 2 \left[ - 3 a x ^ {2} y ^ {2} + x y (3 a x y + a ^ {3}) \right]}{(y ^ {2} - a x) ^ {3}} \\ = - \frac {2 a ^ {3} x y}{\left(y ^ {2} - a x\right) ^ {3}}. \\ \end{array}
$$

下面讨论极值问题. 从 $x^{3} + y^{3} - 3axy = 0$ 和 $x^{2} - ay = 0$ 解出隐函数 $y = f(x)$ 的驻点 $A(\sqrt[3]{2} a, \sqrt[3]{4} a)$. 因为 $y''|_{A} = -\frac{2a^{3}xy}{(y^{2} - ax)^{3}}\bigg|_{(\sqrt[3]{2} a, \sqrt[3]{4} a)} = -\frac{4}{\sqrt[3]{2} a} < 0$, 所以隐函数 $y = f(x)$ 在点

![](images/page_148_image_22.jpg)

<details>
<summary>text_image</summary>

y
A
B
-a
O
x
√2a
x+y+a=0
</details>

图18-4

$A(\sqrt[3]{2}a,\sqrt[3]{4}a)$  取得极大值 $\sqrt[3]{4}a$ .

注 由于在 $B$ 点和原点处的任何邻域上, 每一个 $x$ 所对应的 $y$ 值不惟一, 所以方程(9)不能在那两点的邻域上确定惟一的隐函数.

例3 求由方程

$$
F (x, y, z) = x y z ^ {3} + x ^ {2} + y ^ {3} - z = 0 \tag {10}
$$

在原点附近所确定的二元隐函数  $z=f(x,y)$  的偏导数及在  $(0,1,1)$  处的全微分.

解 由于 $F(0,0,0) = 0, F_z(0,0,0) = -1 \neq 0, F, F_x, F_y, F_z$ 处处连续，根据隐函数定理18.3，在原点 $(0,0,0)$ 附近能惟一确定连续可微的隐函数 $z = f(x,y)$，且可求得它的偏导数如下:

$$
\begin{array}{l} \frac {\partial z}{\partial x} = - \frac {F _ {x}}{F _ {z}} = \frac {y z ^ {3} + 2 x}{1 - 3 x y z ^ {2}}, \\ \frac {\partial z}{\partial y} = - \frac {F _ {y}}{F _ {z}} = \frac {x z ^ {3} + 3 y ^ {2}}{1 - 3 x y z ^ {2}}. \\ \end{array}
$$

以 $(x,y,z)=(0,1,1)$ 代入，得 $\left.\frac{\partial z}{\partial x}\right|_{(0,1,1)}=1,\left.\frac{\partial z}{\partial y}\right|_{(0,1,1)}=3,\mathrm{d}z\mid_{(0,1,1)}=\mathrm{d}x+3\mathrm{d}y.$

例 4(反函数的存在性与其导数) 设  $y=f(x)$  在  $x_{0}$  的某邻域上有连续的导函数  $f'(x)$ ，且  $f(x_{0})=y_{0}$ ，考虑方程

$$
F (x, y) = y - f (x) = 0. \tag {11}
$$

由于

$$
F (x _ {0}, y _ {0}) = 0, F _ {y} = 1, F _ {x} (x _ {0}, y _ {0}) = - f ^ {\prime} (x _ {0}),
$$

所以只要 $f'(x_0) \neq 0$，就能满足隐函数定理的所有条件，这时方程(11)能确定出在 $y_0$ 的某邻域 $U(y_0)$ 上的连续可微隐函数 $x = g(y)$，并称它为函数 $y = f(x)$ 的反函数。反函数的导数是

$$
g ^ {\prime} (y) = - \frac {F _ {y}}{F _ {x}} = - \frac {1}{- f ^ {\prime} (x)} = \frac {1}{f ^ {\prime} (x)}. \tag {12}
$$

事实上,这就是在第五章里曾经得到过的反函数求导公式.

例 5 设  $z=z(x,y)$  由方程  $F(x-z,y-z)=0$  确定, 其中 F 具有二阶偏导数. 试证:  $z_{xx}+2z_{xy}+z_{yy}=0$ .

证 以 $F_{1}, F_{2}$ 分别表示 $F$ 关于第一个变量和第二个变量的偏导数，则 $F_{x} = F_{1}$，$F_{y} = F_{2}$，$F_{z} = -(F_{1} + F_{2})$，于是有

$$
z _ {x} = \frac {F _ {1}}{F _ {1} + F _ {2}}, \quad z _ {y} = \frac {F _ {2}}{F _ {1} + F _ {2}},
$$

所以 $z_{x} + z_{y} = 1$。再两边分别对 $x$ 和 $y$ 求偏导，得 $z_{xx} + z_{yx} = 0, z_{xy} + z_{yy} = 0$。由于二阶偏导数连续，故 $z_{xy} = z_{yx}$，将上述两项相加即得所需结果。

## 习题 18.1

1. 方程 $\cos x + \sin y = \mathrm{e}^{xy}$ 能否在原点的某邻域上确定隐函数 $y = f(x)$ 或 $x = g(y)$?
2. 方程  $xy + z \ln y + e^{xz} = 1$  在点  $(0, 1, 1)$  的某邻域上能否确定出某一个变量为另外两个变量的

函数？

3. 求由下列方程所确定的隐函数的导数:

(1) $x^{2}y + 3x^{4}y^{3} - 4 = 0$ ，求 $\frac{\mathrm{dy}}{\mathrm{dx}};$
(2)  $\ln \sqrt{x^{2}+y^{2}} = \arctan \frac{y}{x}$ ，求  $\frac{dy}{dx}$ ;
(3)  $e^{-xy} + 2z - e^{z} = 0$ , 求  $\frac{\partial z}{\partial x}, \frac{\partial z}{\partial y}$ ;
(4) $a + \sqrt{a^2 - y^2} = y\mathrm{e}^u, u = \frac{x + \sqrt{a^2 - y^2}}{a}$ ($a > 0$), 求 $\frac{\mathrm{d}y}{\mathrm{d}x}, \frac{\mathrm{d}^2y}{\mathrm{d}x^2}$;
(5) $x^{2} + y^{2} + z^{2} - 2x + 2y - 4z - 5 = 0$ ，求 $\frac{\partial z}{\partial x},\frac{\partial z}{\partial y};$
(6) $z = f(x + y + z, xyz)$, 求 $\frac{\partial z}{\partial x}, \frac{\partial x}{\partial y}, \frac{\partial y}{\partial z}$.

4. 设 $z = x^{2} + y^{2}$, 其中 $y = f(x)$ 为由方程 $x^{2} - xy + y^{2} = 1$ 所确定的隐函数, 求 $\frac{\mathrm{dz}}{\mathrm{dx}}$ 及 $\frac{\mathrm{d}^2z}{\mathrm{dx}^2}$.

5. 设 $u = x^{2} + y^{2} + z^{2}$, 其中 $z = f(x, y)$ 是由方程 $x^{3} + y^{3} + z^{3} = 3xyz$ 所确定的隐函数, 求 $u_{x}$ 及 $u_{xx}$.

6. 设 $F(x, y, z) = 0$ 可以确定连续可微隐函数: $x = x(y, z), y = y(z, x), z = z(x, y)$, 试证: $\frac{\partial x}{\partial y} \cdot \frac{\partial y}{\partial z} \cdot \frac{\partial z}{\partial x} = -1$ (偏导数不再是偏微分的商!).

7. 求由下列方程所确定的隐函数的偏导数:

(1)  $x + y + z = \mathrm{e}^{-(x + y + z)}$ ，求 z 对于 x, y 的一阶与二阶偏导数；
(2) $F(x,x+y,x+y+z)=0$, 求 $\frac{\partial z}{\partial x},\frac{\partial z}{\partial y}$ 和 $\frac{\partial^{2}z}{\partial x^{2}}$.

8. 证明: 设方程 $F(x, y) = 0$ 所确定的隐函数 $y = f(x)$ 具有二阶导数, 则当 $F_y \neq 0$ 时, 有

$$
F _ {y} ^ {3} y ^ {\prime \prime} = \left| \begin{array}{c c c} F _ {x x} & F _ {x y} & F _ {x} \\ F _ {x y} & F _ {y y} & F _ {y} \\ F _ {x} & F _ {y} & 0 \end{array} \right|.
$$

9. 设 $f$ 是一元函数, 试问应对 $f$ 提出什么条件, 方程

$$
2 f (x y) = f (x) + f (y)
$$

在点(1,1)的邻域上就能确定出惟一的 $y$ 为 $x$ 的函数？

## § 2 隐函数组

## 一、隐函数组的概念

前一节讨论的是由一个方程所确定的隐函数,本节将讨论由方程组所确定的隐函数组.

设有方程组

$$
\left\{ \begin{array}{l} F (x, y, u, v) = 0, \\ G (x, y, u, v) = 0, \end{array} \right. \tag {1}
$$

其中 $F(x,y,u,v), G(x,y,u,v)$ 为定义在 $V \subset \mathbb{R}^4$ 上的4元函数. 若存在平面区域 $D, E \subset \mathbb{R}^2$, 对于 $D$ 中每一点 $(x,y)$, 有惟一的 $(u,v) \in E$, 使得 $(x,y,u,v) \in V$, 且满足方程组(1), 则称由方程组(1)确定了隐函数组

$$
\left\{ \begin{array}{l l} u = f (x, y), \\ v = g (x, y), \end{array} \right. (x, y) \in D, \quad (u, v) \in E,
$$

并在 $D$ 上成立恒等式

$$
\left\{ \begin{array}{l} F (x, y, f (x, y), g (x, y)) \equiv 0, \\ G (x, y, f (x, y), g (x, y)) \equiv 0, \end{array} \right. \quad (x, y) \in D.
$$

关于隐函数组的一般情况(含有  $m+n$  个变量的 m 个方程所确定的 m 个隐函数)将在第二十三章里用向量形式作进一步讨论.

## 二、隐函数组定理

为了探索由方程组(1)确定隐函数组所需要的条件,不妨假设(1)中的函数F与G是可微的,而且由(1)所确定的两个隐函数u与v也是可微的.那么通过对方程组(1)关于x,y分别求偏导数,得到

$$
\left\{ \begin{array}{l} F _ {x} + F _ {u} u _ {x} + F _ {v} v _ {x} = 0, \\ G _ {x} + G _ {u} u _ {x} + G _ {v} v _ {x} = 0, \end{array} \right. \tag {2}
$$

$$
\left\{ \begin{array}{l} F _ {y} + F _ {u} u _ {y} + F _ {v} v _ {y} = 0, \\ G _ {y} + G _ {u} u _ {y} + G _ {v} v _ {y} = 0. \end{array} \right. \tag {3}
$$

要想从(2)解出 $u_{x}$ 与 $v_{x}$, 从(3)解出 $u_{y}$ 与 $v_{y}$, 其充分条件是它们的系数行列式不为零, 即

$$
\left| \begin{array}{l l} F _ {u} & F _ {v} \\ G _ {u} & G _ {v} \end{array} \right| \neq 0. \tag {4}
$$

(4)式左边的行列式称为函数 $F, G$ 关于变量 $u, v$ 的函数行列式（或雅可比（Jacobi）行列式），亦可记作 $\frac{\partial(F, G)}{\partial(u, v)}$. 条件(4)在隐函数组定理中所起的作用，与定理18.1中的条件(iv)相当.

定理18.4（隐函数组定理）若

(i) $F(x,y,u,v)$ 与 $G(x,y,u,v)$ 在以点 $P_0(x_0,y_0,u_0,v_0)$ 为内点的区域 $V\subset \mathbf{R}^4$ 上连续；

(ii)  $F(x_{0}, y_{0}, u_{0}, v_{0}) = 0$ ,  $G(x_{0}, y_{0}, u_{0}, v_{0}) = 0$  (初始条件);

(iii) 在 V 上 F, G 具有一阶连续偏导数；

(iv) $J = \frac{\partial(F, G)}{\partial(u, v)}$ 在点 $P_0$ 不等于零.

则

$1^{\circ}$ 存在点 $P_{0}$ 的某一(四维空间)邻域 $U(P_0)\subset V$ ，在 $U(P_0)$ 上方程组(1)惟一地

确定了定义在点 $Q_{0}(x_{0},y_{0})$ 的某一(二维空间)邻域 $U(Q_0)$ 上的两个二元隐函数

$$
u = f (x, y), v = g (x, y),
$$

使得 $u_0 = f(x_0, y_0), v_0 = g(x_0, y_0)$，且当 $(x, y) \in U(Q_0)$ 时，

$$
\begin{array}{l} (x, y, f (x, y), g (x, y)) \in U (P _ {0}), \\ F (x, y, f (x, y), g (x, y)) \equiv 0, \\ G (x, y, f (x, y), g (x, y)) \equiv 0; \\ \end{array}
$$

$2^{\circ}f(x,y),g(x,y)$ 在 $U(Q_0)$ 上连续；

$3^{\circ}f(x,y),g(x,y)$ 在 $U(Q_0)$ 上有一阶连续偏导数，且

$$
\begin{array}{l} \frac {\partial u}{\partial x} = - \frac {1}{J} \frac {\partial (F , G)}{\partial (x , v)}, \quad \frac {\partial v}{\partial x} = - \frac {1}{J} \frac {\partial (F , G)}{\partial (u , x)}, \tag {5} \\ \frac {\partial u}{\partial y} = - \frac {1}{J} \frac {\partial (F , G)}{\partial (y , v)}, \quad \frac {\partial v}{\partial y} = - \frac {1}{J} \frac {\partial (F , G)}{\partial (u , y)}. \\ \end{array}
$$

本定理的证明这里从略,有兴趣的读者可参阅第二十三章里的一般隐函数组定理及其证明.

注 在定理18.4中, 若将条件(iv)改为 $\frac{\partial(F,G)}{\partial(y,v)}\Big|_{P_0} \neq 0$, 则方程(1)所确定的隐函数组相应是 $y = y(u,x), v = v(u,x)$, 其他情形均可类似推得. 总之, 由方程组定义隐函数组及隐函数组求导时, 应先明确哪些变量是自变量, 哪些变量是因变量, 然后再进行有关的运算和讨论.

例1 讨论方程组

$$
\left\{ \begin{array}{l} F (x, y, u, v) = u ^ {2} + v ^ {2} - x ^ {2} - y = 0, \\ G (x, y, u, v) = - u + v - x y + 1 = 0 \end{array} \right. \tag {6}
$$

在点 $P_0(2,1,1,2)$ 近旁能确定怎样的隐函数组，并求其偏导数.

解 首先, $F(P_{0})=G(P_{0})=0$ , 即  $P_{0}$  满足初始条件. 再求出 F, G 的所有一阶偏导数

$$
\begin{array}{l} F _ {x} = - 2 x, F _ {y} = - 1, F _ {u} = 2 u, F _ {v} = 2 v, \\ G _ {x} = - y, G _ {y} = - x, G _ {u} = - 1, G _ {v} = 1. \\ \end{array}
$$

容易验算,在  $P_{0}$  处的所有六个雅可比行列式中只有

$$
\frac {\partial (F , G)}{\partial (x , v)} = 0.
$$

因此, 只有 x, v 难以肯定能否作为以 y, u 为自变量的隐函数. 除此之外, 在  $P_{0}$  的近旁任何两个变量都可作为以其余两个变量为自变量的隐函数.

如果我们想求得 $x = x(u, v), y = y(u, v)$ 的偏导数，只需对方程组(6)分别关于 $u, v$ 求偏导数，得到

$$
\left\{ \begin{array}{l} 2 u - 2 x x _ {u} - y _ {u} = 0, \\ - 1 - y x _ {u} - x y _ {u} = 0, \end{array} \right. \tag {7}
$$

$$
\left\{ \begin{array}{l} 2 v - 2 x x _ {v} - y _ {v} = 0, \\ 1 - x y _ {v} - y x _ {v} = 0. \end{array} \right. \tag {8}
$$

由(7)解出

$$
x _ {u} = \frac {2 x u + 1}{2 x ^ {2} - y}, y _ {u} = - \frac {2 x + 2 y u}{2 x ^ {2} - y}.
$$

由(8)解出

$$
x _ {v} = \frac {2 x v - 1}{2 x ^ {2} - y}, y _ {v} = \frac {2 x - 2 y v}{2 x ^ {2} - y}.
$$

例 2 设函数  $f(x,y)$ ,  $g(x,y)$  具有连续偏导数，而  $u=u(x,y)$ ,  $v=v(x,y)$  是由方程组  $u=f(ux,v+y)$ ,  $g(u-x,v^{2}y)=0$  确定的隐函数组，试求  $\frac{\partial u}{\partial x}, \frac{\partial v}{\partial y}$ .

解 设 $F = u - f(ux, v + y), G = g(u - x, v^2y)$，则有

$$
\left( \begin{array}{c c c c} F _ {x} & F _ {y} & F _ {u} & F _ {v} \\ G _ {x} & G _ {y} & G _ {u} & G _ {v} \end{array} \right) = \left( \begin{array}{c c c c} - u f _ {1} & - f _ {2} & 1 - x f _ {1} & - f _ {2} \\ - g _ {1} & v ^ {2} g _ {2} & g _ {1} & 2 v y g _ {2} \end{array} \right).
$$

于是

$$
\begin{array}{l} J _ {u v} = \left| \begin{array}{c c} 1 - x f _ {1} & - f _ {2} \\ g _ {1} & 2 v y g _ {2} \end{array} \right| = 2 y v g _ {2} - 2 x y v f _ {1} g _ {2} + f _ {2} g _ {1}, \\ J _ {x v} = \left| \begin{array}{c c} - u f _ {1} & - f _ {2} \\ - g _ {1} & 2 v y g _ {2} \end{array} \right| = - 2 y u v f _ {1} g _ {2} - f _ {2} g _ {1}, \\ J _ {u y} = \left| \begin{array}{c c} 1 - x f _ {1} & - f _ {2} \\ g _ {1} & v ^ {2} g _ {2} \end{array} \right| = v ^ {2} g _ {2} - x v ^ {2} f _ {1} g _ {2} + f _ {2} g _ {1}. \\ \end{array}
$$

因此

$$
\begin{array}{l} \frac {\partial u}{\partial x} = - \frac {J _ {x v}}{J _ {u v}} = \frac {2 y u v f _ {1} g _ {2} + f _ {2} g _ {1}}{2 y v g _ {2} - 2 x y v f _ {1} g _ {2} + f _ {2} g _ {1}}, \\ \frac {\partial v}{\partial y} = - \frac {J _ {u y}}{J _ {u v}} = \frac {x v ^ {2} f _ {1} g _ {2} - f _ {2} g _ {1} - v ^ {2} g _ {2}}{2 y v g _ {2} - 2 x y v f _ {1} g _ {2} + f _ {2} g _ {1}}. \\ \end{array}
$$

## 三、反函数组与坐标变换

在 §1 例 4 中, 我们通过隐函数定理讨论了一元函数反函数存在的(充分)条件. 现在讨论由二元函数组所确定的反函数组存在的(充分)条件.

设函数组

$$
u = u (x, y), v = v (x, y) \tag {9}
$$

是定义在 $xy$ 平面点集 $B \subset \mathbf{R}^2$ 上的两个函数，对每一点 $P(x, y) \in B$ ，由方程组(9)有 $uv$ 平面上惟一的一点 $Q(u, v) \in \mathbf{R}^2$ 与之对应. 我们称方程组(9)确定了 $B$ 到 $\mathbf{R}^2$ 的一个映射（变换），记作 $T$. 这时映射(9)可写成如下函数形式:

$$
\begin{array}{l} T: B \to \mathbf {R} ^ {2}, \\ P (x, y) \mapsto Q (u, v) \\ \end{array}
$$

或写成点函数形式 $Q = T(P), P \in B$，并称 $Q(u, v)$ 为映射 $T$ 下 $P(x, y)$ 的象，而 $P$ 则是 $Q$ 的原象。记 $B$ 在映射 $T$ 下的象集为 $B' = T(B)$。

反过来, 若 T 为一一映射(即不仅每一原象只对应一个象, 而且不同的原象对应不同的象). 这时每一点  $Q \in B'$ , 由方程组(9)都有惟一的一点  $P \in B$  与之相对应. 由此所产生的新映射称为映射 $T$ 的逆映射（逆变换），记作 $T^{-1}$，即

$$
T ^ {- 1}: B ^ {\prime} \rightarrow B,
$$

$$
Q \mapsto P
$$

或 $P = T^{-1}(Q), Q \in B'$.

亦即存在定义在 $B'$ 上的一个函数组

$$
x = x (u, v), y = y (u, v), \tag {10}
$$

把它代入(9)而成为恒等式:

$$
u \equiv u (x (u, v), y (u, v)), v \equiv v (x (u, v), y (u, v)), \tag {11}
$$

这时我们又称函数组(10)是函数组(9)的反函数组.

关于反函数组的存在性问题,其实是隐函数组存在性问题的一种特殊情形.这只需把方程组(9)改写成

$$
\left\{ \begin{array}{l} F (x, y, u, v) = u - u (x, y) = 0, \\ G (x, y, u, v) = v - v (x, y) = 0, \end{array} \right. \tag {12}
$$

并将定理 18.4 应用于(12)，便可得到函数组(9)在某个局部范围内存在反函数组(10)的下述定理.

定理18.5（反函数组定理）设函数组(9)及其一阶偏导数在某区域 $D\subset \mathbf{R}^2$ 上连续，点 $P_0(x_0,y_0)$ 是 $D$ 的内点，且

$$
u _ {0} = u (x _ {0}, y _ {0}), \quad v _ {0} = v (x _ {0}, y _ {0}), \quad \frac {\partial (u , v)}{\partial (x , y)} \Big | _ {P _ {0}} \neq 0,
$$

则在点 $P_0'(u_0, v_0)$ 的某一邻域 $U(P_0')$ 上存在惟一的一组反函数 (10)，使得 $x_0 = x(u_0, v_0), y_0 = y(u_0, v_0)$，且当 $(u, v) \in U(P_0')$ 时，有

$$
(x (u, v), y (u, v)) \in U (P _ {0})
$$

以及恒等式(11). 此外, 反函数组(10)在  $U(P_{0}^{\prime})$  上存在连续的一阶偏导数, 且

$$
\frac {\partial x}{\partial u} = \frac {\partial v}{\partial y} / \frac {\partial (u , v)}{\partial (x , y)}, \quad \frac {\partial x}{\partial v} = - \frac {\partial u}{\partial y} / \frac {\partial (u , v)}{\partial (x , y)},
$$

$$
\frac {\partial y}{\partial u} = - \left. \frac {\partial v}{\partial x} \right/ \frac {\partial (u , v)}{\partial (x , y)}, \quad \frac {\partial y}{\partial v} = \frac {\partial u}{\partial x} \Bigg / \frac {\partial (u , v)}{\partial (x , y)}. \tag {13}
$$

由(13)式看到:互为反函数组的(9)与(10),它们的雅可比行列式互为倒数,即

$$
\frac {\partial (u , v)}{\partial (x , y)} \cdot \frac {\partial (x , y)}{\partial (u , v)} = 1.
$$

这与(一元)反函数求导公式(§1中(12)式)相类似.

例 3 平面上的点 P 的直角坐标  $(x, y)$  与极坐标  $(r, \theta)$  之间的坐标变换公式为

$$
x = r \cos \theta , \quad y = r \sin \theta . \tag {14}
$$

由于

$$
\frac {\partial (x , y)}{\partial (r , \theta)} = \left| \begin{array}{c c} \cos \theta & - r \sin \theta \\ \sin \theta & r \cos \theta \end{array} \right| = r,
$$

所以除原点外,在一切点上由函数组(14)所确定的反函数组是

$$
r = \sqrt {x ^ {2} + y ^ {2}},
$$

$$
\theta = \left\{ \begin{array}{l l} \arctan \frac {y}{x}, & x > 0, \\ \pi + \arctan \frac {y}{x}, & x <   0 \end{array} \right. \quad \text {或} \quad \theta = \left\{ \begin{array}{l l} \operatorname{arccot} \frac {x}{y}, & y > 0, \\ \pi + \operatorname{arccot} \frac {x}{y}, & y <   0. \end{array} \right.
$$

对于函数组

$$
x = x (u, v, w), y = y (u, v, w), z = z (u, v, w),
$$

在相应于定理18.5的条件下所确定出的反函数组为

$$
u = u (x, y, z), v = v (x, y, z), w = w (x, y, z),
$$

它们是三维空间中直角坐标与曲面坐标之间的坐标变换.

例4 直角坐标 $(x,y,z)$ 与球坐标 $(r,\varphi ,\theta)$ 之间的变换公式为

$$
\left\{ \begin{array}{l} x = r \sin \varphi \cos \theta , \\ y = r \sin \varphi \sin \theta , \\ z = r \cos \varphi . \end{array} \right. \tag {15}
$$

由于

$$
\begin{array}{l} \frac {\partial (x , y , z)}{\partial (r , \varphi , \theta)} = \left| \begin{array}{c c c} \sin \varphi \cos \theta & r \cos \varphi \cos \theta & - r \sin \varphi \sin \theta \\ \sin \varphi \sin \theta & r \cos \varphi \sin \theta & r \sin \varphi \cos \theta \\ \cos \varphi & - r \sin \varphi & 0 \end{array} \right| \\ = r ^ {2} \sin \varphi , \\ \end{array}
$$

所以在 $r^2\sin \varphi \neq 0$ 即除去 $z$ 轴上的一切点，由方程组(15)可确定出 $r, \varphi, \theta$ 为 $x, y, z (x > 0)$ 的函数，即

$$
\begin{array}{l} r = \sqrt {x ^ {2} + y ^ {2} + z ^ {2}}, \varphi = \arccos \frac {z}{r}, \\ \theta = \left\{ \begin{array}{l l} {\arctan \frac {y}{x},} & {x > 0,} \\ {\pi + \arctan \frac {y}{x},} & {x <   0} \end{array} \right. \quad \text {或} \quad \theta = \left\{ \begin{array}{l l} {\operatorname{arccot} \frac {x}{y},} & {y > 0,} \\ {\pi + \operatorname{arccot} \frac {x}{y},} & {y <   0.} \end{array} \right. \\ \end{array}
$$

例5 设 $\varphi$ 为二元连续可微函数. 对于函数组 $u = x + at, v = x - at$, 试把弦振动方程

$$
a ^ {2} \frac {\partial^ {2} \varphi}{\partial x ^ {2}} = \frac {\partial^ {2} \varphi}{\partial t ^ {2}} (a > 0)
$$

变换成以 u, v 为自变量的形式.

解 首先有 $u_{x} = v_{x} = 1, u_{t} = -v_{t} = a$，从而 $\frac{\partial(u, v)}{\partial(x, t)} = -2a \neq 0$，因此所设变换存在逆变换，而且又有

$$
\mathrm{d} u = u _ {x} \mathrm{d} x + u _ {t} \mathrm{d} t = \mathrm{d} x + a \mathrm{d} t, \mathrm{d} v = \mathrm{d} x - a \mathrm{d} t.
$$

于是按微分形式不变性,得到

$$
\mathrm{d} \varphi = \varphi_ {u} \mathrm{d} u + \varphi_ {v} \mathrm{d} v = (\varphi_ {u} + \varphi_ {v}) \mathrm{d} x + a (\varphi_ {u} - \varphi_ {v}) \mathrm{d} t,
$$

并由此推知

$$
\varphi_ {x} = \varphi_ {u} + \varphi_ {v}, \quad \varphi_ {t} = a (\varphi_ {u} - \varphi_ {v}).
$$

按此继续求以 $u, v$ 为自变量的 $\varphi_{xx}$ 与 $\varphi_{u}$ 如下:

$$
\varphi_ {x x} = \frac {\partial}{\partial u} (\varphi_ {u} + \varphi_ {v}) u _ {x} + \frac {\partial}{\partial v} (\varphi_ {u} + \varphi_ {v}) v _ {x}
$$

$$
\begin{array}{l} = \varphi_ {u u} + \varphi_ {v u} + \varphi_ {u v} + \varphi_ {v v} = \varphi_ {u u} + 2 \varphi_ {u v} + \varphi_ {v v}, \\ \varphi_ {u} = a \frac {\partial}{\partial u} \left(\varphi_ {u} - \varphi_ {v}\right) u _ {t} + a \frac {\partial}{\partial v} \left(\varphi_ {u} - \varphi_ {v}\right) v _ {t} \\ = a ^ {2} (\varphi_ {u u} - 2 \varphi_ {u v} + \varphi_ {v v}). \\ \end{array}
$$

借助这些结果就得到

$$
a ^ {2} \varphi_ {x x} - \varphi_ {u} = 4 a ^ {2} \varphi_ {u v} = 0,
$$

即把原来以 $x, t$ 作为自变量的弦振动方程变换成以 $u, v$ 作为新自变量的方程为

$$
\frac {\partial^ {2} \varphi}{\partial u \partial v} = 0.
$$

而且进一步容易求得此方程的解的形式为

$$
\varphi = f (u) + g (v) = f (x + a t) + g (x - a t)
$$

(参见第十七章总练习题7).

## 习题 18.2

1. 试讨论方程组

$$
\left\{ \begin{array}{l} x ^ {2} + y ^ {2} = \frac {z ^ {2}}{2}, \\ x + y + z = 2 \end{array} \right.
$$

在点 $(1, -1, 2)$ 的附近能否确定形如 $x = f(z), y = g(z)$ 的隐函数组？

2. 求下列方程组所确定的隐函数组的导数:

(1) $\left\{ \begin{array}{l} x^{2} + y^{2} + z^{2} = a^{2}, \\ x^{2} + y^{2} = ax, \end{array} \right.$ 求 $\frac{\mathrm{d}y}{\mathrm{d}x}, \frac{\mathrm{d}z}{\mathrm{d}x}$;
(2) $\left\{ \begin{array}{l} x - u^2 - yv = 0, \\ y - v^2 - xu = 0, \end{array} \right.$ 求 $\frac{\partial u}{\partial x}, \frac{\partial v}{\partial x}, \frac{\partial u}{\partial y}, \frac{\partial v}{\partial y};$
(3) $\left\{ \begin{array}{l} u = f(ux, v + y), \\ v = g(u - x, v^2y), \end{array} \right.$ 求 $\frac{\partial u}{\partial x}, \frac{\partial v}{\partial x}$.

3. 求下列函数组所确定的反函数组的偏导数:

(1) $\left\{ \begin{array}{l} x = \mathrm{e}^{u} + u \sin v, \\ y = \mathrm{e}^{u} - u \cos v, \end{array} \right.$ 求 $u_{x}, v_{x}, u_{y}, v_{y}$;
(2) $\left\{\begin{aligned}x&=u+v,\\ y&=u^{2}+v^{2},\\ z&=u^{3}+v^{3},\end{aligned}\right.$  求  $z_{x}$

4. 设函数 $z = z(x, y)$ 是由方程组

$$
x = \mathrm{e} ^ {u + v}, y = \mathrm{e} ^ {u - v}, z = u v
$$

$(u, v$ 为参量)所定义的函数, 求当 $u = 0, v = 0$ 时的 $\mathrm{dz}$.

5. 设以 $u, v$ 为新的自变量变换下列方程:

(1) $(x+y)\frac{\partial z}{\partial x}-(x-y)\frac{\partial z}{\partial y}=0$ , 设  $u=\ln\sqrt{x^{2}+y^{2}}$ ,  $v=\arctan\frac{y}{x}$ ;
(2) $x^{2}\frac{\partial^{2}z}{\partial x^{2}} - y^{2}\frac{\partial^{2}z}{\partial y^{2}} = 0$ ，设 $u = xy, v = \frac{x}{y}$.

6. 设函数 $u = u(x, y)$ 由方程组

$$
u = f (x, y, z, t), \quad g (y, z, t) = 0, \quad h (z, t) = 0
$$

所确定, 求  $\frac{\partial u}{\partial x}$  和  $\frac{\partial u}{\partial y}$ .

7. 设 $u = u(x, y, z), v = v(x, y, z)$ 和 $x = x(s, t), y = y(s, t), z = z(s, t)$ 都有连续的一阶偏导数. 证明

$$
\frac {\partial (u , v)}{\partial (s , t)} = \frac {\partial (u , v)}{\partial (x , y)} \frac {\partial (x , y)}{\partial (s , t)} + \frac {\partial (u , v)}{\partial (y , z)} \frac {\partial (y , z)}{\partial (s , t)} + \frac {\partial (u , v)}{\partial (z , x)} \frac {\partial (z , x)}{\partial (s , t)}.
$$

8. 设 $u = \frac{y}{\tan x}, v = \frac{y}{\sin x}$. 证明: 当 $0 < x < \frac{\pi}{2}, y > 0$ 时, $u, v$ 可以用来作为曲线坐标, 解出 $x, y$ 作为 $u, v$ 的函数, 画出 $xy$ 平面上 $u = 1, v = 2$ 所对应的坐标曲线, 计算 $\frac{\partial(u, v)}{\partial(x, y)}$ 和 $\frac{\partial(x, y)}{\partial(u, v)}$ 并验证它们互为倒数.

9. 将以下式中的 $(x,y,z)$ 变换成球面坐标 $(r,\theta,\varphi)$ 的形式:

$$
\Delta_ {1} u = \left(\frac {\partial u}{\partial x}\right) ^ {2} + \left(\frac {\partial u}{\partial y}\right) ^ {2} + \left(\frac {\partial u}{\partial z}\right) ^ {2},
$$

$$
\Delta_ {2} u = \frac {\partial^ {2} u}{\partial x ^ {2}} + \frac {\partial^ {2} u}{\partial y ^ {2}} + \frac {\partial^ {2} u}{\partial z ^ {2}}.
$$

10. 设 $u = \frac{x}{r^2}, v = \frac{y}{r^2}, w = \frac{z}{r^2}$, 其中 $r = \sqrt{x^2 + y^2 + z^2}$.

(1) 试求以 u, v, w 为自变量的反函数组；

(2) 计算 $\frac{\partial(u,v,w)}{\partial(x,y,z)}$ .

## §3 几何应用

在本节中所讨论的曲线和曲面,由于它们的方程是以隐函数(组)的形式出现的,因此在求它们的切线(或切平面)时都要用到隐函数(组)的微分法.

## 一、平面曲线的切线与法线

设平面曲线由方程

$$
F (x, y) = 0 \tag {1}
$$

给出,它在点  $P_{0}(x_{0},y_{0})$  的某邻域上满足隐函数定理条件,于是在点  $P_{0}$  附近所确定的连续可微隐函数  $y=f(x)$  (或  $x=g(y)$ ) 和方程(1)在点  $P_{0}$  附近表示同一曲线,从而该曲线在点  $P_{0}$  存在切线和法线,其方程分别为

$$
y - y _ {0} = f ^ {\prime} (  x _ {0}  )   (  x - x _ {0}  ) \quad (\text {或}   x - x _ {0} = g ^ {\prime} (  y _ {0}  )   (  y - y _ {0}  )  )
$$

与

$$
y - y _ {0} = - \frac {1}{f ^ {\prime} (  x _ {0}  )} (  x - x _ {0}  ) \quad (\text {或}   x - x _ {0} = - \frac {1}{g ^ {\prime} (  y _ {0}  )} (  y - y _ {0}  )  ).
$$

由于

$$
f ^ {\prime} (  x  ) = -   \frac {F _ {x}}{F _ {y}} \quad \left(  \text {或}    g ^ {\prime} (  y  ) = -   \frac {F _ {y}}{F _ {x}}\right)  ,
$$

所以曲线(1)在点 $P_{0}$ 的切线与法线方程为

切线: $F_{x}(x_{0},y_{0})(x - x_{0}) + F_{y}(x_{0},y_{0})(y - y_{0}) = 0,$ (2)

法线: $F_{y}(x_{0},y_{0})(x - x_{0}) - F_{x}(x_{0},y_{0})(y - y_{0}) = 0.$ (3)

例 1 求笛卡儿叶形线(参见 §1 例 2)

$$
2 (x ^ {3} + y ^ {3}) - 9 x y = 0
$$

在点 $(2,1)$ 的切线与法线.

解 设 $F(x, y) = 2(x^3 + y^3) - 9xy$，于是 $F_x = 6x^2 - 9y, F_y = 6y^2 - 9x$ 在全平面连续，且 $F_x(2,1) = 15 \neq 0, F_y(2,1) = -12 \neq 0$. 因此，由公式（2）与（3）分别求得曲线在点（2，1）的切线方程与法线方程分别为

$$
\begin{array}{l} 1 5 (x - 2) - 1 2 (y - 1) = 0 \quad \text {即} \quad 5 x - 4 y - 6 = 0, \\ - 1 2 (x - 2) - 1 5 (y - 1) = 0 \quad \text {即} \quad 4 x + 5 y - 1 3 = 0. \\ \end{array}
$$

![](images/page_158_image_8.jpg)

## 二、空间曲线的切线与法平面

下面我们讨论由参数方程

$$
L \colon x = x (t), y = y (t), z = z (t), \alpha \leqslant t \leqslant \beta \tag {4}
$$

表示的空间曲线 L 上某一点  $P_{0}(x_{0}, y_{0}, z_{0})$  的切线和法平面方程，这里  $x_{0} = x(t_{0})$ ,  $y_{0} = y(t_{0})$ ,  $z_{0} = z(t_{0})$ ,  $\alpha \leqslant t_{0} \leqslant \beta$ ，并假定(4)式中的三个函数在  $t_{0}$  处可导，且

$$
\left[ x ^ {\prime} (t _ {0}) \right] ^ {2} + \left[ y ^ {\prime} (t _ {0}) \right] ^ {2} + \left[ z ^ {\prime} (t _ {0}) \right] ^ {2} \neq 0.
$$

在曲线 L 上点  $P_{0}$  附近选取一点  $P(x,y,z)=P(x_{0}+\Delta x,y_{0}+\Delta y,z_{0}+\Delta z)$ ，于是连接 L 上的点  $P_{0}$  与 P 的割线方程为

$$
\frac {x - x _ {0}}{\Delta x} = \frac {y - y _ {0}}{\Delta y} = \frac {z - z _ {0}}{\Delta z},
$$

其中  $\Delta x = x(t_{0} + \Delta t) - x(t_{0})$ ,  $\Delta y = y(t_{0} + \Delta t) - y(t_{0})$ ,  $\Delta z = z(t_{0} + \Delta t) - z(t_{0})$ . 以  $\Delta t$  除上式各分母, 得

$$
\frac {x - x _ {0}}{\frac {\Delta x}{\Delta t}} = \frac {y - y _ {0}}{\frac {\Delta y}{\Delta t}} = \frac {z - z _ {0}}{\frac {\Delta z}{\Delta t}}.
$$

当  $\Delta t \rightarrow 0$  时,  $P \rightarrow P_{0}$ , 且

$$
\frac {\Delta x}{\Delta t} \rightarrow x ^ {\prime} (  t _ {0})  , \quad \frac {\Delta y}{\Delta t} \rightarrow y ^ {\prime} (  t _ {0})  , \quad \frac {\Delta z}{\Delta t} \rightarrow z ^ {\prime} (  t _ {0})  ,
$$

即得曲线 L 在  $P_{0}$  处的切线方程为

$$
\frac {x - x _ {0}}{x ^ {\prime} (t _ {0})} = \frac {y - y _ {0}}{y ^ {\prime} (t _ {0})} = \frac {z - z _ {0}}{z ^ {\prime} (t _ {0})}. \tag {5}
$$

由此可见，当 $x'(t_0), y'(t_0), z'(t_0)$ 不全为零时，它们是该切线的方向数.

过点 $P_{0}$ 可以作无穷多条直线与切线 $l$ 垂直，所有这些直线都在同一平面上，称此平面为曲线 $L$ 在点$P_{0}$ 的法平面（图18-5中的平面 $\Pi$ ).它通过点 $P_{0}$ ，且以 $L$ 在 $P_{0}$ 的切线 $l$ 为它的法线，所以法平面 $\Pi$ 的方程为

![](images/page_158_image_24.jpg)

<details>
<summary>text_image</summary>

Π
P₀
l
L
</details>

图18-5

$$
x ^ {\prime} (t _ {0}) (x - x _ {0}) + y ^ {\prime} (t _ {0}) (y - y _ {0}) + z ^ {\prime} (t _ {0}) (z - z _ {0}) = 0. \tag {6}
$$

当空间曲线 $L$ 由方程组

$$
L: \left\{ \begin{array}{l} F (x, y, z) = 0, \\ G (x, y, z) = 0 \end{array} \right. \tag {7}
$$

给出时, 若它在点 $P_{0}(x_{0}, y_{0}, z_{0})$ 的某邻域上满足隐函数组定理的条件 (这里不妨设条件 (iv) 是 $\frac{\partial(F, G)}{\partial(x, y)} \bigg|_{P_{0}} \neq 0$), 则方程组 (7) 在点 $P_{0}$ 附近能确定惟一连续可微的隐函数组

$$
x = \varphi (z), y = \psi (z), \tag {8}
$$

使得 $x_0 = \varphi (z_0), y_0 = \psi (z_0)$，且

$$
\frac {\mathrm{d} x}{\mathrm{d} z} = - \frac {\frac {\partial (F , G)}{\partial (z , y)}}{\frac {\partial (F , G)}{\partial (x , y)}}, \frac {\mathrm{d} y}{\mathrm{d} z} = - \frac {\frac {\partial (F , G)}{\partial (x , z)}}{\frac {\partial (F , G)}{\partial (x , y)}}.
$$

由于在点 $P_0$ 附近方程组(7)与函数组(8)表示同一空间曲线,因此以 $z$ 为参量时,就得到点 $P_0$ 附近曲线 $L$ 的参量方程

$$
x = \varphi (z), y = \psi (z), z = z.
$$

于是由(5)式,曲线在 $P_{0}$ 处的切线方程为

$$
\frac {x - x _ {0}}{\left. \frac {\mathrm{d} x}{\mathrm{d} z} \right| _ {P _ {0}}} = \frac {y - y _ {0}}{\left. \frac {\mathrm{d} y}{\mathrm{d} z} \right| _ {P _ {0}}} = \frac {z - z _ {0}}{1},
$$

即

$$
\frac {x - x _ {0}}{\left. \frac {\partial (F , G)}{\partial (y , z)} \right| _ {P _ {0}}} = \frac {y - y _ {0}}{\left. \frac {\partial (F , G)}{\partial (z , x)} \right| _ {P _ {0}}} = \frac {z - z _ {0}}{\left. \frac {\partial (F , G)}{\partial (x , y)} \right| _ {P _ {0}}}. \tag {9}
$$

按(6)式,曲线在 $P_{0}$ 处的法平面方程为

$$
\frac {\partial (F , G)}{\partial (y , z)} \Big | _ {P _ {0}} (x - x _ {0}) + \frac {\partial (F , G)}{\partial (z , x)} \Big | _ {P _ {0}} (y - y _ {0}) + \frac {\partial (F , G)}{\partial (x , y)} \Big | _ {P _ {0}} (z - z _ {0}) = 0. \tag {10}
$$

同样可推出: 当  $\frac{\partial(F,G)}{\partial(y,z)}$  或  $\frac{\partial(F,G)}{\partial(z,x)}$  在  $P_{0}$  处不等于零时, 曲线在  $P_{0}$  处的切线与法平面方程仍分别取(9)与(10)的形式. 由此可见, 当

$$
\frac {\partial (F , G)}{\partial (y , z)} \Big | _ {P _ {0}}, \quad \frac {\partial (F , G)}{\partial (z , x)} \Big | _ {P _ {0}}, \quad \frac {\partial (F , G)}{\partial (x , y)} \Big | _ {P _ {0}}
$$

不全为零时,它们是空间曲线(7)在 $P_{0}$ 处的切线的方向数.

例 2 求球面  $x^{2}+y^{2}+z^{2}=50$  与锥面  $x^{2}+y^{2}=z^{2}$  所截出的曲线在  $(3,4,5)$  处的切线与法平面方程.

解设

$$
F (x, y, z) = x ^ {2} + y ^ {2} + z ^ {2} - 5 0,
$$

$$
G (x, y, z) = x ^ {2} + y ^ {2} - z ^ {2}.
$$

它们在(3,4,5)处的偏导数和雅可比行列式之值分别为

$$
\frac {\partial F}{\partial x} = 6, \quad \frac {\partial F}{\partial y} = 8, \quad \frac {\partial F}{\partial z} = 1 0,
$$