# 第14章 线性动态电路的复频域分析

原始 PDF 第 344–384 页。

# 第十四章

# 线性动态电路的 复频域分析

![](../../raw/pages_0321-0352/images/page_343_image_2.jpg)

## 导读

第七章介绍了用经典法求解动态电路,其优点是物理概念清楚,但当分析具有多个动态元件及多个激励电源的复杂电路时,则直接求解微分方程会有一定的困难。拉普拉斯①变换法是在复频域求解高阶动态电路方程行之有效的方法之一。本章介绍的主要内容有:

1. 常用函数的拉普拉斯变换, 拉普拉斯变换的基本性质, 拉普拉斯反变换的部分分式展开法。
2. 应用拉普拉斯变换分析动态电路, 其步骤是: (1) 画出正确的运算电路图; (2) 应用电路分析的一般方法或电路定理求出响应的象函数; (3) 应用部分分式展开法进行拉普拉斯反变换, 求得响应的时域表达式。
3. 复频域的网络函数及其零极点在电路分析中的应用。

网络函数是指线性时不变电路在单一电源激励下,其零状态响应的象函数与激励的象函数之比,即  $H(s)=\frac{R(s)}{E(s)}$ 。 $H(s)$  是与输入  $E(s)$  无关的量,它取决于网络结构和电路参数。它与网络的冲激响应构成拉普拉斯变换对,即  $H(s)=\mathcal{L}[h(t)]$ ,根据网络函数的极点分布情况和激励的变化规律可预见时域响应的全部特点。如果令网络函数  $H(s)$  中的复频率  $s=j\omega$ ,那么分析  $H(j\omega)$  随频率变化的情况可以预见相应的网络函数的频率特性。

## §14-1 拉普拉斯变换的定义

第七章研究了一阶电路和二阶电路,所应用的方法是根据电路定律和元件的电压、电流关系建立描述电路的方程,建立的方程是以时间为自变量的线性常微分方程,求解

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 法国数学家拉普拉斯(P.S.Laplace)。</span></small>

---

§ 14-1 拉普拉斯变换的定义

321

常微分方程即可得到电路变量在时域的解答,这种方法又称为经典法。

对于具有多个动态元件的复杂电路，用直接求解微分方程的方法比较困难。例如对于一个 $n$ 阶方程，直接求解时需要知道变量及其各阶导数[直到 $(n - 1)$ 阶导数]在 $t = 0_{+}$时刻的值，而电路中给定的初始状态是各电感电流和电容电压在 $t = 0_{+}$时刻的值，从这些值求得所需初始条件的工作量很大。积分变换法是通过积分变换，把已知的时域函数变换为频域函数，从而把时域的微分方程化为频域的代数方程。求出频域函数后，再作反变换，返回时域，可以求得满足电路初始条件的原微分方程的解答，而不需要确定积分常数。拉普拉斯变换是一种重要的积分变换，是求解高阶复杂动态电路的有效而重要的方法之一。

一个定义在 $[0,\infty)$ 区间的函数 $f(t)$ ，它的拉普拉斯变换式 $F(s)$ 定义为

$$
F (s) = \int_ {0 _ {-}} ^ {\infty} f (t) \mathrm{e} ^ {- s t} \mathrm{d} t \tag {14-1}
$$

式中  $s=\sigma+j\omega$  为复数， $F(s)$  称为  $f(t)$  的象函数， $f(t)$  称为  $F(s)$  的原函数。拉普拉斯变换简称为拉氏变换。

式(14-1)表明拉氏变换是一种积分变换。还可以看出 $f(t)$ 的拉氏变换 $F(s)$ 存在的条件是该式右边的积分为有限值，故 $\mathrm{e}^{-t}$ 称为收敛因子。对于一个函数 $f(t)$，如果存在正的有限值常数 $M$ 和 $c$，使得对于所有 $t$ 满足条件

$$
\mid f (t) \mid \leqslant M \mathrm{e} ^ {c t}
$$

则 $f(t)$ 的拉氏变换式 $F(s)$ 总存在，因为总可以找到一个合适的 $s$ 值，使式(14-1)中的积分为有限值①。假设本书涉及的 $f(t)$ 都满足此条件。

从式(14-1)还可看出，把原函数 $f(t)$ 与 $e^{-st}$ 的乘积从 $t=0$ 到 $\infty$ 对t进行积分，则此积分的结果不再是t的函数。所以拉氏变换是把一个时间域的函数 $f(t)$ 变换到s域内的复变函数 $F(s)$ 。变量s称为复频率。应用拉氏变换法进行电路分析称为电路的复频域分析方法，又称为运算法。定义中拉氏变换的积分从 $t=0$ 开始，可以计及t=0时 $f(t)$ 包含的冲激，从而给计算存在冲激函数电压和电流的电路带来方便。

如果  $F(s)$  已知, 要求出与它对应的原函数  $f(t)$ , 由  $F(s)$  到  $f(t)$  的变换称为拉普拉斯反变换, 它定义为

$$
f (t) = \frac {1}{2 \pi \mathrm{j}} \int_ {c - \mathrm{j} \infty} ^ {c + \mathrm{j} \infty} F (s) \mathrm{e} ^ {s t} \mathrm{d} s \tag {14-2}
$$

式中 c 为正的有限常数。

通常可用符号 $\mathcal{L}[\quad]$ 表示对方括号里的时域函数作拉氏变换，用符号 $\mathcal{B}^{-1}[\quad]$ 表示对方括号内的复变函数作拉氏反变换。

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 式(14-1)严格应称为单边拉普拉斯变换。由于本书着重拉氏变换在电路分析中的应用,关于式(14-1)存在的条件以及s的取值问题等有关拉氏变换的数学理论问题,可参阅有关教材。</span></small>

1. 用 $\mathrm{H}_{2}$ 气体中加入一个液体，使气体浓度从 $0.5\mathrm{mg/L}$ 上升至 $1.0\mathrm{mg/L}$ 。

---

图 3-1

322

第十四章 线性动态电路的复频域分析

例14-1 求以下函数的象函数:

(1) 单位阶跃函数；
(2) 单位冲激函数；
(3) 指数函数。

解（1）求单位阶跃函数的象函数

$$
\begin{array}{l} f (t) = \varepsilon (t) \\ F (s) = \mathscr {L} [ f (t) ] = \int_ {0 _ {-}} ^ {\infty} \varepsilon (t) \mathrm{e} ^ {- s t} \mathrm{d} t = \int_ {0 _ {-}} ^ {\infty} \mathrm{e} ^ {- s t} \mathrm{d} t \\ = - \frac {1}{s} \mathrm{e} ^ {- s t} \Bigg | _ {0 _ {-}} ^ {\infty} = \frac {1}{s} \\ \end{array}
$$

(2) 求单位冲激函数的象函数

$$
\begin{array}{l} f (t) = \delta (t) \\ F (s) = \mathscr {L} [ f (t) ] = \int_ {0 _ {-}} ^ {\infty} \delta (t) \mathrm{e} ^ {- s t} \mathrm{d} t \\ = \int_ {0 _ {-}} ^ {0 _ {+}} \delta (t) \mathrm{e} ^ {- s t} \mathrm{d} t = \mathrm{e} ^ {- s (0)} = 1 \\ \end{array}
$$

可以看出按式(14-1)的定义,能计及 t=0 时  $f(t)$  所包含的冲激函数。

(3) 指数函数的象函数

$$
f (t) = \mathrm{e} ^ {\alpha t} \quad (\alpha \text {为实数})
$$

$$
\begin{array}{l} F (s) = \mathscr {L} [ f (t) ] = \int_ {0 _ {-}} ^ {\infty} \mathrm{e} ^ {\alpha t} \mathrm{e} ^ {- s t} \mathrm{d} t \\ = \frac {1}{- (s - \alpha)} \mathrm{e} ^ {- (s - \alpha) t} \Bigg | _ {0 _ {-}} ^ {\infty} \\ = \frac {1}{s - \alpha} \\ \end{array}
$$

## §14-2 拉普拉斯变换的基本性质

拉普拉斯变换有许多重要性质,本节仅介绍与分析线性电路有关的一些基本性质。

## 1. 线性性质

设 $f_{1}(t)$ 和 $f_{2}(t)$ 是两个任意的时间函数，它们的象函数分别为 $F_{1}(s)$ 和 $F_{2}(s), A_{1}$ 和 $A_{2}$ 是两个任意实常数，则

$$
\begin{array}{l} \mathscr {L} [ A _ {1} f _ {1} (t) + A _ {2} f _ {2} (t) ] = A _ {1} \mathscr {L} [ f _ {1} (t) ] + A _ {2} \mathscr {L} [ f _ {2} (t) ] \\ = A _ {1} F _ {1} (s) + A _ {2} F _ {2} (s) \\ \end{array}
$$

证 $\mathcal{L}[A_1f_1(t) + A_2f_2(t)] = \int_{0_{-}}^{\infty}\left[A_1f_1(t) + A_2f_2(t)\right]\mathrm{e}^{-st}\mathrm{d}t$

$$
= A _ {1} \int_ {0 _ {-}} ^ {\infty} f _ {1} (t) \mathrm{e} ^ {- s t} \mathrm{d} t + A _ {2} \int_ {0 _ {-}} ^ {\infty} f _ {2} (t) \mathrm{e} ^ {- s t} \mathrm{d} t
$$

---

§ 14-2 拉普拉斯变换的基本性质

323

$$
= A _ {1} F _ {1} (s) + A _ {2} F _ {2} (s)
$$

例 14-2 若: (1)  $f(t)=\sin(\omega t)$ ;

$$
f (t) = K \left(1 - \mathrm{e} ^ {- \alpha t}\right) 。 \tag {2}
$$

上述函数的定义域为 $[0,\infty)$ ，求其象函数。

$$
\begin{array}{l} = \frac {1}{2 \mathrm{j}} \bigg (\frac {1}{s - \mathrm{j} \omega} - \frac {1}{s + \mathrm{j} \omega} \bigg) \\ = \frac {\omega}{s ^ {2} + \omega^ {2}} \\ \end{array}
$$

解 (1) $\mathcal{L}[\sin (\omega t)] = \mathcal{L}\left[\frac{1}{2\mathrm{j}} (\mathrm{e}^{\mathrm{j}\omega t} - \mathrm{e}^{-\mathrm{j}\omega t})\right]$

$$
\begin{array}{l} = \frac {K}{s} - \frac {K}{s + \alpha} \\ = \frac {K \alpha}{s (s + \alpha)} \\ \end{array}
$$

(2) $\mathcal{L}[K(1 - \mathrm{e}^{-\alpha t})] = \mathcal{L}[K] - \mathcal{L}[Ke^{-\alpha t}]$

由此可见,根据拉氏变换的线性性质,求函数乘以常数的象函数以及求几个函数相加减的结果的象函数时,可以先求各函数的象函数再进行计算。

## 2. 微分性质

函数 $f(t)$ 的象函数与其导数 $f^{\prime}(t) = \frac{\mathrm{d}f(t)}{\mathrm{d}t}$ 的象函数之间有如下关系:

若 $\mathcal{L}[f(t)] = F(s)$ 则 $\mathcal{B}[f'(t)] = sF(s) - f(0_{-})$

证 $\mathcal{L}\left[\frac{\mathrm{d}f(t)}{\mathrm{d}t}\right] = \int_{0_{-}}^{\infty}\frac{\mathrm{d}f(t)}{\mathrm{d}t}\mathrm{e}^{-st}\mathrm{d}t$

设 $\mathrm{e}^{-st} = u, f'(t) \, \mathrm{d}t = \mathrm{d}v$，则 $\mathrm{d}u = -s\mathrm{e}^{-st}\mathrm{d}t, v = f(t)$。由于 $\int u \, \mathrm{d}v = uv - \int v \, \mathrm{d}u$，所以

$$
\begin{array}{l} \int_ {0 _ {-}} ^ {\infty} f ^ {\prime} (t) \mathrm{e} ^ {- s t} \mathrm{d} t = f (t) \mathrm{e} ^ {- s t} \Bigg | _ {0 _ {-}} ^ {\infty} - \int_ {0 _ {-}} ^ {\infty} f (t) (- s \mathrm{e} ^ {- s t}) \mathrm{d} t \\ = - f (0 _ {-}) + s \int_ {0 _ {-}} ^ {\infty} f (t) \mathrm{e} ^ {- s t} \mathrm{d} t \\ \end{array}
$$

只要 $s$ 的实部 $\sigma$ 取得足够大，当 $t \to \infty$ 时，$\mathrm{e}^{-st} f(t) \to 0$，则 $F(s)$ 存在，于是得

$$
\mathcal {L} [ f ^ {\prime} (t) ] = s F (s) - f (0 _ {-})
$$

例14-3 应用导数性质求下列函数的象函数:

(1) $f(t) = \cos(\omega t)$;
(2) $f(t) = \delta (t)$ 。

解（1）由于 $\frac{\mathrm{d}\sin(\omega t)}{\mathrm{d}t} = \omega \cos (\omega t)$

---

324

第十四章 线性动态电路的复频域分析

$$
\cos (\omega t) = \frac {1}{\omega} \frac {\mathrm{d} \sin (\omega t)}{\mathrm{d} t}
$$

而  $\mathcal{L}[\sin(\omega t)]=\frac{\omega}{s^{2}+\omega^{2}}$  (例 14-2 中已求得)，所以

$$
\begin{array}{l} \mathcal {L} [ \cos (\omega t) ] = \mathcal {L} \left[ \frac {1}{\omega} \frac {\mathrm{d}}{\mathrm{d} t} \sin (\omega t) \right] = \frac {1}{\omega} \left(s \frac {\omega}{s ^ {2} + \omega^ {2}} - 0\right) \\ = \frac {s}{s ^ {2} + \omega^ {2}}. \\ \end{array}
$$

(2) 由于 $\delta(t) = \frac{\mathrm{d}}{\mathrm{d}t}\varepsilon(t)$, 而 $\mathcal{L}[\varepsilon(t)] = \frac{1}{s}$, 所以

$$
\mathscr {L} [ \delta (t) ] = \mathscr {L} \left[ \frac {\mathrm{d}}{\mathrm{d} t} \varepsilon (t) \right] = s \cdot \frac {1}{s} - 0 = 1
$$

此结果与例 14-1 所得结果完全相同。

## 3. 积分性质

函数 $f(t)$ 的象函数与其积分 $\int_0^t f(\xi)\mathrm{d}\xi$ 的象函数之间满足如下关系:

若 $\mathcal{L}[f(t)] = F(s)$

则 $\mathcal{L}\left[\int_{0_{-}}^{t}f(\xi)\mathrm{d}\xi\right] = \frac{F(s)}{s}$

证 令 $u = \int f(t) \, \mathrm{d}t, \, \mathrm{d}v = \mathrm{e}^{-st} \, \mathrm{d}t$，则 $\mathrm{d}u = f(t) \, \mathrm{d}t, v = -\frac{\mathrm{e}^{-st}}{s}$，利用分部积分公式 $\int u \, \mathrm{d}v = uv - \int v \, \mathrm{d}u$，所以

$$
\begin{array}{l} \int_ {0 _ {-}} ^ {\infty} \left\{\left[ \int_ {0 _ {-}} ^ {t} f (\xi) \mathrm{d} \xi \right] \mathrm{e} ^ {- s t} \mathrm{d} t \right\} \\ = \left(\int_ {0 _ {-}} ^ {t} f (\xi) \mathrm{d} \xi\right) \frac {\mathrm{e} ^ {- s t}}{- s} \Bigg | _ {0 _ {-}} ^ {\infty} - \int_ {0 _ {-}} ^ {\infty} f (t) \left(- \frac {\mathrm{e} ^ {- s t}}{s}\right) \mathrm{d} t \\ = \left[ \int_ {0 _ {-}} ^ {t} f (\xi) \mathrm{d} \xi \right] \frac {\mathrm{e} ^ {- s t}}{- s} \Bigg | _ {0 _ {-}} ^ {\infty} + \frac {1}{s} \int_ {0 _ {-}} ^ {\infty} f (t) \mathrm{e} ^ {- s t} \mathrm{d} t \\ \end{array}
$$

只要 s 的实部  $\sigma$  足够大, 当  $t \to \infty$  时和  $t = 0_{-}$  时, 等式右边第一项都为零, 所以有

$$
\mathcal {L} \Big [ \int_ {0 _ {-}} ^ {t} f (\xi)   \mathrm{d} \xi \Big ] = \frac {F (s)}{s}
$$

例 14-4 利用积分性质求函数  $f(t)=t$  的象函数。

解 由于 $f(t) = t = \int_{0}^{t}\varepsilon (\xi)\mathrm{d}\xi$ ，所以

$$
\mathcal {L} [ f (t) ] = \frac {1}{s} \cdot \frac {1 ^ {\prime}}{s} = \frac {1}{s ^ {2}}
$$

---

§ 14-2 拉普拉斯变换的基本性质

325

## 4. 延迟性质

函数 $f(t)$ 的象函数与其延迟函数 $f(t-t_{0})\varepsilon(t-t_{0})$ 的象函数之间有如下关系:

若 $\mathcal{L}[f(t)] = F(s)$

则 $\mathcal{L}[f(t - t_0)\varepsilon (t - t_0)] = \mathrm{e}^{-st_0}F(s)$

证 $\mathcal{L}[f(t - t_0)\varepsilon (t - t_0)] = \int_{0\pm}^{\infty}f(t - t_0)\varepsilon (t - t_0)\mathrm{e}^{-st}\mathrm{d}t$

$$
= \int_ {t _ {0}} ^ {\infty} f (t - t _ {0}) \mathrm{e} ^ {- s t} \mathrm{d} t
$$

令  $\tau=t-t_{0}$ ，则上式为

$$
\begin{array}{l} \mathcal {L} [ f (  t - t _ {0}  )   \varepsilon (  t - t _ {0}  )   ] = \int_ {0 _ {-}} ^ {\infty} f (  \tau  )   \mathrm{e} ^ {- s (  \tau + t _ {0}  )}   \mathrm{d} \tau \\ = \mathrm{e} ^ {- s t _ {0}} \int_ {0 _ {-}} ^ {\infty} f (\tau) \mathrm{e} ^ {- s \tau} \mathrm{d} \tau \\ = \mathrm{e} ^ {- s t _ {0}} F (s) \\ \end{array}
$$

例 14-5 求图 14-1 所示矩形脉冲的象函数。

解 图 14-1 中的矩形脉冲可用解析式表示为

$$
f (t) = \varepsilon (t) - \varepsilon (t - \tau)
$$

因为  $\mathcal{L}[\varepsilon(t)]=\frac{1}{s}$ ，根据延迟性质

$$
\mathcal {L} [ \varepsilon (t - \tau) ] = \frac {1}{s} \mathrm{e} ^ {- s \tau}
$$

又根据拉氏变换的线性性质,得

$$
\begin{array}{l} \mathcal {L} [ f (t) ] = \mathcal {L} [ \varepsilon (t) - \varepsilon (t - \tau) ] \\ = \frac {1}{s} - \frac {1}{s} \mathrm{e} ^ {- s \tau} \\ = \frac {1}{s} (1 - \mathrm{e} ^ {- s \tau}) \\ \end{array}
$$

![](../../raw/pages_0321-0352/images/page_348_chart_18.jpg)

<details>
<summary>area</summary>

| Time (t) | Value (f(t)) |
| --- | --- |
| 0 | 0 |
| \(\tau\) | A |
| \(\tau\) | 0 |
</details>

图14-1 例14-5图

## 5. 拉氏变换的卷积定理

§ 7-9 已介绍过两个时间函数 $f_{1}(t)$ 和 $f_{2}(t)$, 它们在 $t < 0$ 时为零, $f_{1}(t)$ 和 $f_{2}(t)$ 的卷积用下列积分式定义:

$$
f _ {1} (t) * f _ {2} (t) = \int_ {0} ^ {t} f _ {1} (t - \xi) f _ {2} (\xi)   \mathrm{d} \xi
$$

设 $f_{1}(t)$ 和 $f_{2}(t)$ 的象函数分别为 $F_{1}(s)$ 和 $F_{2}(s)$，有

$$
\begin{array}{l} \mathcal {L} [ f _ {1} (t) * f _ {2} (t) ] = \mathcal {L} \left[ \int_ {0} ^ {t} f _ {1} (t - \xi) f _ {2} (\xi)   \mathrm{d} \xi \right] \\ = F _ {1} (s) F _ {2} (s) \\ \end{array}
$$

证 根据拉氏变换定义,有

---

326

第十四章 线性动态电路的复频域分析

$$
\mathcal {L} [ f _ {1} (t) * f _ {2} (t) ] = \int_ {0} ^ {\infty} \mathrm{e} ^ {- s t} \left[ \int_ {0} ^ {t} f _ {1} (t - \xi) f _ {2} (\xi) \mathrm{d} \xi \right] \mathrm{d} t
$$

根据延迟的单位阶跃函数的定义

$$
\varepsilon (t - \xi) = \left\{ \begin{array}{l l} 1 & \xi <   t \\ 0 & \xi > t \end{array} \right.
$$

故 $\int_0^t f_1(t - \xi)f_2(\xi)\mathrm{d}\xi = \int_0^\infty f_1(t - \xi)\varepsilon (t - \xi)f_2(\xi)\mathrm{d}\xi$

$$
\mathcal {L} [ f _ {1} (t) * f _ {2} (t) ] = \int_ {0} ^ {\infty} \mathrm{e} ^ {- s t} \int_ {0} ^ {\infty} f _ {1} (t - \xi)   \varepsilon (t - \xi) f _ {2} (\xi)   \mathrm{d} \xi \mathrm{d} t
$$

令 $x = t - \xi$ ，则 $\mathrm{e}^{-st} = \mathrm{e}^{-s(x + \xi)}$ ，上式变为

$$
\begin{array}{l} \mathcal {L} [ f _ {1} (t) * f _ {2} (t) ] = \int_ {0} ^ {\infty} \int_ {0} ^ {\infty} f _ {1} (x) \varepsilon (x) f _ {2} (\xi) \mathrm{e} ^ {- s \xi} \mathrm{e} ^ {- s x} \mathrm{d} \xi \mathrm{d} x \\ = \int_ {0} ^ {\infty} f _ {1} (x) \varepsilon (x) \mathrm{e} ^ {- s x} \mathrm{d} x \int_ {0} ^ {\infty} f _ {2} (\xi) \mathrm{e} ^ {- s \xi} \mathrm{d} \xi \\ = F _ {1} (s) F _ {2} (s) \\ \end{array}
$$

同理,可以证明

$$
\mathscr {L} [ f _ {2} (t) * f _ {1} (t) ] = F _ {2} (s) F _ {1} (s)
$$

所以

$$
f _ {1} (t) * f _ {2} (t) = f _ {2} (t) * f _ {1} (t)
$$

根据以上介绍的拉氏变换的定义及与电路分析有关的拉氏变换的一些基本性质，可以方便地求得一些常用的时间函数的象函数，表14-1为常用函数的拉氏变换表。

表 14-1

| 原函数$f(t)$ | 原函数$f(t)$ | 原函数$f(t)$ | 原函数$f(t)$ |
| --- | --- | --- | --- |
| $A\delta(t)$ | $A$ | $\cos(\omega t+\phi)$ | $\frac{s\cos\phi-\omega\sin\phi}{s^{2}+\omega^{2}}$ |
| $A\varepsilon(t)$ | $A/s$ | $e^{-\alpha t}\sin(\omega t)$ | $\frac{\omega}{(s+\alpha)^{2}+\omega^{2}}$ |
| $Ae^{-\alpha t}$ | $\frac{A}{s+\alpha}$ | $e^{-\alpha t}\cos(\omega t)$ | $\frac{s+\alpha}{(s+\alpha)^{2}+\omega^{2}}$ |
| $1-e^{-\alpha t}$ | $\frac{\alpha}{s(s+\alpha)}$ | $te^{-\alpha t}$ | $\frac{1}{(s+\alpha)^{2}}$ |
| $\sin(\omega t)$ | $\frac{\omega}{s^{2}+\omega^{2}}$ | $t$ | $\frac{1}{s^{2}}$ |
| $\cos(\omega t)$ | $\frac{s}{s^{2}+\omega^{2}}$ | $\sinh(\alpha t)$ | $\frac{\alpha}{s^{2}-\alpha^{2}}$ |
| $\sin(\omega t+\phi)$ | $\frac{s\sin\phi+\omega\cos\phi}{s^{2}+\omega^{2}}$ | $\cosh(\alpha t)$ | $\frac{s}{s^{2}-\alpha^{2}}$ |

---

§ 14-3 拉普拉斯反变换的部分分式展开

327

续表

| 原函数$f(t)$ | 象函数$F(s)$ | 原函数$f(t)$ | 象函数$F(s)$ |
| --- | --- | --- | --- |
| $(1-\alpha t)\mathrm{e}^{-\alpha t}$ | $\frac{s}{(s+\alpha)^2}$ | $\frac{1}{n!}t^n$ | $\frac{1}{s^{n+1}}$ |
| $\frac{1}{2}t^2$ | $\frac{1}{s^3}$ | $\frac{1}{n!}t^n\mathrm{e}^{-\alpha t}$ | $\frac{1}{(s+\alpha)^{n+1}}$ |

## §14-3 拉普拉斯反变换的部分分式展开

用拉氏变换求解线性电路的时域响应时，需要把求得的响应的拉氏变换式反变换为时间函数。拉氏反变换可以用式(14-2)求得，但涉及计算一个复变函数的积分，一般比较复杂。如果象函数比较简单，往往能从拉氏变换表中查出其原函数。对于不能从表中查出原函数的情况，如果能设法把象函数分解为若干较简单的、能够从表中查到的项，就可查出各项对应的原函数，而它们之和即为所求原函数。电路响应的象函数通常可表示为两个实系数的 $s$ 的多项式之比，即 $s$ 的一个有理分式

$$
F (s) = \frac {N (s)}{D (s)} = \frac {a _ {0} s ^ {m} + a _ {1} s ^ {m - 1} + \cdots + a _ {m}}{b _ {0} s ^ {n} + b _ {1} s ^ {n - 1} + \cdots + b _ {n}} \tag {14-3}
$$

式中 m 和 n 为正整数，且  $n \geqslant m^{①}$ 。

把  $F(s)$  分解成若干简单项之和, 而这些简单项可以在拉氏变换表中找到, 这种方法称为部分分式展开法, 或称为分解定理。

用部分分式展开有理分式  $F(s)$  时, 需要把有理分式化为真分式。若 n > m, 则  $F(s)$  为真分式。若 n = m, 则

$$
F (s) = A + \frac {N _ {0} (s)}{D (s)}
$$

式中 A 是一个常数, 其对应的时间函数为  $A\delta(t)$ , 余数项  $\frac{N_{0}(s)}{D(s)}$  是真分式。

用部分分式展开真分式时,需要对分母多项式作因式分解,求出  $D(s)=0$  的根。 $D(s)=0$  的根可以是单根、共轭复根和重根几种情况。

## 1. 单根

如果  $D(s)=0$  有 n 个单根, 设 n 个单根分别是  $p_{1}, p_{2}, \cdots, p_{n}$ 。于是  $F(s)$  可以展开为

$$
F (s) = \frac {K _ {1}}{s - p _ {1}} + \frac {K _ {2}}{s - p _ {2}} + \dots + \frac {K _ {n}}{s - p _ {n}} \tag {14-4}
$$

式中  $K_{1}, K_{2}, \cdots, K_{n}$  是待定系数。

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 在电路分析中,通常不出现 n<m 的情况。</span></small>

---

328

第十四章 线性动态电路的复频域分析

将上式两边都乘以 $(s-p_{1})$ ，得

$$
(s - p _ {1}) F (s) = K _ {1} + (s - p _ {1}) \left(\frac {K _ {2}}{s - p _ {2}} + \dots + \frac {K _ {n}}{s - p _ {n}}\right)
$$

令 $s = p_{1}$ ，则等式除第一项外都变为零，这样求得

$$
K _ {1} = \left[ (s - p _ {1}) F (s) \right] _ {s = p _ {1}}
$$

同理可求得 $K_{2}, K_{3}, \cdots, K_{n}$ 。所以确定式(14-4)中各待定系数的公式为

$$
K _ {i} = \left[ (s - p _ {i}) F (s) \right] _ {s = p _ {i}} \quad (i = 1, 2, 3, \dots , n)
$$

因为 $p_i$ 是 $D(s) = 0$ 的一个根，故上面关于 $K_{i}$ 的表达式为 $\frac{0}{0}$ 的不定式，可以用求极限的方法确定 $K_{i}$ 的值，即

$$
K _ {i} = \lim _ {s \to p _ {i}} \frac {(s - p _ {i}) N (s)}{D (s)} = \lim _ {s \to p _ {i}} \frac {(s - p _ {i}) N ^ {\prime} (s) + N (s)}{D ^ {\prime} (s)} = \frac {N (p _ {i})}{D ^ {\prime} (p _ {i})}
$$

所以确定式(14-4)中各待定系数的另一公式为

$$
K _ {i} = \frac {N (s)}{D ^ {\prime} (s)} \Bigg | _ {s = p _ {i}} \quad (i = 1, 2, 3, \dots , n) \tag {14-5}
$$

确定了式(14-4)中各待定系数后,相应的原函数为

$$
f (t) = \mathscr {L} ^ {- 1} [ F (s) ] = \sum_ {i = 1} ^ {n} K _ {i} \mathrm{e} ^ {p _ {i} t} = \sum_ {i = 1} ^ {n} \frac {N (p _ {i})}{D ^ {\prime} (p _ {i})} \mathrm{e} ^ {p _ {i} t}
$$

例14-6 求 $F(s) = \frac{2s + 1}{s^3 + 7s^2 + 10s}$ 的原函数 $f(t)$。

解 因为 $F(s) = \frac{2s + 1}{s^3 + 7s^2 + 10s} = \frac{2s + 1}{s(s + 2)(s + 5)}$

所以, $D(s)=0$ 的根为

$$
p _ {1} = 0, p _ {2} = - 2, p _ {3} = - 5
$$

$$
D ^ {\prime} (s) = 3 s ^ {2} + 1 4 s + 1 0
$$

根据式(14-5)确定各系数

$$
K _ {1} = \frac {\dot {N} (s)}{D ^ {\prime} (s)} \Bigg | _ {s = p _ {1}} = \frac {2 s + 1}{3 s ^ {2} + 1 4 s + 1 0} \Bigg | _ {s = 0} = 0. 1
$$

同理求得 $K_{2} = 0.5$

$$
K _ {3} = - 0. 6
$$

所以 $f(t) = 0.1 + 0.5\mathrm{e}^{-2t} - 0.6\mathrm{e}^{-5t}$

## 2. 共轭复根

如果 $D(s) = 0$ 具有共轭复根 $p_1 = \alpha +\mathrm{j}\omega ,p_2 = \alpha -\mathrm{j}\omega$ ，则

$$
K _ {1} = [ (s - \alpha - \mathrm{j} \omega) F (s) ] _ {s = \alpha + \mathrm{j} \omega} = \frac {N (s)}{D ^ {\prime} (s)} \Bigg | _ {s = \alpha + \mathrm{j} \omega}
$$

---

§ 14-3 拉普拉斯反变换的部分分式展开

329

$$
K _ {2} = \left[ (s - \alpha + \mathrm{j} \omega) F (s) \right] _ {s = \alpha - \mathrm{j} \omega} = \frac {N (s)}{D ^ {\prime} (s)} \Bigg | _ {s = \alpha - \mathrm{j} \omega}
$$

由于  $F(s)$  是实系数多项式之比，故  $K_{1}, K_{2}$  为共轭复数。

设  $\dot{K}_{1}=\left|K_{1}\right|e^{j\theta_{1}}$ ，则  $K_{2}=\left|K_{1}\right|e^{-j\theta_{1}}$ ，有

$$
\begin{array}{l} f (t) = K _ {1} \mathrm{e} ^ {(\alpha + \mathrm{j} \omega) t} + K _ {2} \mathrm{e} ^ {(\alpha - \mathrm{j} \omega) t} \\ = \left| K _ {1} \right| \mathrm{e} ^ {\mathrm{j} \theta_ {1}} \mathrm{e} ^ {(\alpha + \mathrm{j} \omega) t} + \left| K _ {1} \right| \mathrm{e} ^ {- \mathrm{j} \theta_ {1}} \mathrm{e} ^ {(\alpha - \mathrm{j} \omega) t} \\ = \left| K _ {1} \right| \mathrm{e} ^ {\alpha t} \left[ \mathrm{e} ^ {\mathrm{j} (\omega t + \theta_ {1})} + \mathrm{e} ^ {- \mathrm{j} (\omega t + \theta_ {1})} \right] \\ = 2 \mid K _ {1} \mid \mathrm{e} ^ {\alpha t} \cos (\omega t + \theta_ {1}) \tag {14-6} \\ \end{array}
$$

例14-7 求 $F(s) = \frac{s + 3}{s^2 + 2s + 5}$ 的原函数 $f(t)$。

解 $D(s) = 0$ 的根为共轭复根，$p_{1} = -1 + \mathrm{j}2, p_{2} = -1 - \mathrm{j}2$。

$$
K _ {1} = \frac {N (s)}{D ^ {\prime} (s)} \Bigg | _ {s = p _ {1}} = \frac {s + 3}{2 s + 2} \Bigg | _ {s = - 1 + j 2}
$$

$$
= 0. 5 - \mathrm{j} 0. 5 = 0. 5 \sqrt {2} \mathrm{e} ^ {- \mathrm{j} \frac {\pi}{4}}
$$

$$
K _ {2} = \mid K _ {1} \mid \mathrm{e} ^ {- \mathrm{j} \theta_ {1}} = 0. 5 \sqrt {2} \mathrm{e} ^ {\mathrm{j} \frac {\pi}{4}}
$$

根据式(14-6)可得

$$
\begin{array}{l} f (t) = 2 \mid K _ {1} \mid \mathrm{e} ^ {- t} \cos \left(2 t - \frac {\pi}{4}\right) \\ = \sqrt {2}   \mathrm{e} ^ {- t} \cos \left(2 t - \frac {\pi}{4}\right) \\ \end{array}
$$

## 3. 重根

如果 $D(s) = 0$ 具有重根，则应含 $(s - p_1)^n$ 的因式。现设 $D(s)$ 中含有 $(s - p_1)^3$ 的因式，$p_i$ 为 $D(s) = 0$ 的三重根，其余为单根，$F(s)$ 可分解为

$$
F (s) = \frac {K _ {1 3}}{s - p _ {1}} + \frac {K _ {1 2}}{(s - p _ {1}) ^ {2}} + \frac {K _ {1 1}}{(s - p _ {1}) ^ {3}} + \left(\frac {K _ {2}}{s - p _ {2}} + \dots\right) ① \tag {14-7}
$$

对于单根，仍采用 $K_{i} = \frac{N(s)}{D'(s)}\Bigg|_{s = p_i}$ 公式计算。为了确定 $K_{11}, K_{12}$ 和 $K_{13}$ 可以将式(14-7)两边都乘以 $(s - p_1)^3$ ，则 $K_{11}$ 被单独分离出来，即

$$
(s - p _ {1}) ^ {3} F (s) = (s - p _ {1}) ^ {2} K _ {1 3} + (s - p _ {1}) K _ {1 2} + \dot {K} _ {1 1} + (s - p _ {1}) ^ {3} \left(\frac {K _ {2}}{s - p _ {2}} + \dots\right) \tag {14-8}
$$

则 $K_{11} = (s - p_1)^3 F(s)\big|_{s = p_1}$

式(14-8)两边再对 s 求导一次, $K_{12}$  被分离出来,即

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">① 括号中为其余单根项。</span></small>

1. 工程图

---

330

第十四章 线性动态电路的复频域分析

$$
\frac {\mathrm{d}}{\mathrm{d} s} \left[ (s - p _ {1}) ^ {3} F (s) \right] = 2 (s - p _ {1}) K _ {1 3} + K _ {1 2} + \frac {\mathrm{d}}{\mathrm{d} s} \left[ (s - p _ {1}) ^ {3} \left(\frac {K _ {2}}{s - p _ {2}} + \dots\right) \right]
$$

所以

$$
K _ {1 2} = \frac {\mathrm{d}}{\mathrm{d} s} \left[ (s - p _ {1}) ^ {3} F (s) \right] _ {s = p _ {1}}
$$

用同样的方法可得

$$
K _ {1 3} = \frac {1}{2} \frac {\mathrm{d} ^ {2}}{\mathrm{d} s ^ {2}} \left[ (s - p _ {1}) ^ {3} F (s) \right] _ {s = p _ {1}}
$$

从以上分析过程可以推论得出当 $D(s) = 0$ 具有 $q$ 阶重根，其余为单根时的分解式为

$$
F (s) = \frac {K _ {1 q}}{s - p _ {1}} + \frac {K _ {1 (q - 1)}}{(s - p _ {1}) ^ {2}} + \dots + \frac {K _ {1 1}}{(s - p _ {1}) ^ {q}} + \left(\frac {K _ {2}}{s - p _ {2}} + \dots\right) \tag {14-9}
$$

式中

$$
K _ {1 1} = (s - p _ {1}) ^ {q} F (s) \mid_ {s = p _ {1}}
$$

$$
K _ {1 2} = \frac {\mathrm{d}}{\mathrm{d} s} \left[ (s - p _ {1}) ^ {q} F (s) \right] \Bigg | _ {s = p _ {1}}
$$

$$
K _ {1 3} = \frac {1}{2} \frac {\mathrm{d} ^ {2}}{\mathrm{d} s ^ {2}} \left[ (s - p _ {1}) ^ {q} F (s) \right] \Bigg | _ {s = p _ {1}}
$$

• • • • • • • • • • • •

$$
K _ {1 q} = \frac {1}{(q - 1) !} \frac {\mathrm{d} ^ {q - 1}}{\mathrm{d} s ^ {q - 1}} \left[ (s - p _ {1}) ^ {q} F (s) \right] \Bigg | _ {s = p _ {1}}
$$

如果  $D(s)=0$  具有多个重根时, 对每个重根分别利用上述方法即可得到各系数。

例14-8 求 $F(s) = \frac{1}{(s + 1)^3 s^2}$ 的原函数 $f(t)$。

解 令 $D(s) = (s + 1)^3 s^2 = 0$，有 $p_1 = -1$ 为三重根，$p_2 = 0$ 为二重根，所以

$$
F (s) = \frac {K _ {1 3}}{s + 1} + \frac {K _ {1 2}}{(s + 1) ^ {2}} + \frac {K _ {1 1}}{(s + 1) ^ {3}} + \frac {K _ {2 2}}{s} + \frac {K _ {2 1}}{s ^ {2}}
$$

首先以 $(s + 1)^{3}$ 乘以 $F(s)$ 得

$$
(s + 1) ^ {3} F (s) = \frac {1}{s ^ {2}}
$$

应用式(14-9)得

$$
K _ {1 1} = \frac {1}{s ^ {2}} \Bigg | _ {s = - 1} = 1
$$

$$
K _ {1 2} = \frac {\mathrm{d}}{\mathrm{d} s} \frac {1}{s ^ {2}} \Bigg | _ {s = - 1} = \frac {- 2}{s ^ {3}} \Bigg | _ {s = - 1} = 2
$$

---

§ 14-4 运算电路

331

$$
K _ {1 3} = \frac {1}{2} \frac {\mathrm{d} ^ {2}}{\mathrm{d} s ^ {2}} \frac {1}{s ^ {2}} \Bigg | _ {s = - 1} = \frac {1}{2} \frac {6}{s ^ {4}} \Bigg | _ {s = - 1} = 3
$$

同样为计算 $K_{21}$ 和 $K_{22}$, 首先以 $s^2$ 乘 $F(s)$ 得

$$
s ^ {2} F (s) = \frac {1}{(s + 1) ^ {3}}
$$

应用式(14-9)可求得

$$
K _ {2 1} = 1
$$

$$
K _ {2 2} = - 3
$$

所以

$$
F (s) = \frac {1}{(s + 1) ^ {3} s ^ {2}} = \frac {3}{s + 1} + \frac {2}{(s + 1) ^ {2}} + \frac {1}{(s + 1) ^ {3}} - \frac {3}{s} + \frac {1}{s ^ {2}}
$$

相应的原函数为

$$
f (t) = 3 \mathrm{e} ^ {- t} + 2 t \mathrm{e} ^ {- t} + \frac {1}{2} t ^ {2} \mathrm{e} ^ {- t} - 3 + t
$$

## §14-4 运算电路

基尔霍夫定律的时域表示式为:

对任一节点  $\sum i(t)=0$

对任一回路 $\sum u(t) = 0$

根据拉氏变换的线性性质得出基尔霍夫定律的运算形式如下:

对任一节点  $\sum I(s)=0$

对任一回路  $\sum U(s)=0$

根据元件电压、电流的时域关系,可以推导出各元件电压电流关系的运算形式。

图 14-2(a) 所示电阻元件的电压电流关系为  $u(t)=Ri(t)$ ，两边取拉氏变换，得

$$
U (s) = R I (s) \tag {14-10}
$$

式(14-10)就是电阻 VCR 的运算形式, 图 14-2(b) 称为电阻 R 的运算电路。

![](../../raw/pages_0353-0384/images/page_354_image_23.jpg)

(a)

![](../../raw/pages_0353-0384/images/page_354_image_25.jpg)

(b)

图14-2 电阻的运算电路

对于图 14-3(a) 所示电感有  $u(t)=L\frac{\mathrm{d}i(t)}{\mathrm{d}t}$ ，取拉氏变换并根据拉氏变换的微分性质，得

![](../../raw/pages_0353-0384/images/page_354_image_29.jpg)

<details>
<summary>natural_image</summary>

Pure technical line drawing of a mechanical or architectural component without any text, numbers, or symbols
</details>

[Illegible]

---

332

第十四章 线性动态电路的复频域分析

$$
\mathcal {L} [ u (t) ] = \mathcal {L} \bigg [ L \frac {\mathrm{d} i (t)}{\mathrm{d} t} \bigg ]
$$

$$
U (s) = s L I (s) - L i (0 _ {-}) \tag {14-11a}
$$

式中 $sL$ 为电感的运算阻抗，$i(0_{-})$ 表示电感中的初始电流。这样就可以得到图14-3(b)所示运算电路，$Li(0_{-})$ 表示附加电压源的电压，它反映了电感中初始电流的作用。还可以把式(14-11a)改写为

$$
I (s) = \frac {1}{s L} U (s) + \frac {i (0 _ {-})}{s} \tag {14-11b}
$$

就可以获得图 14-3(c) 所示运算电路, 其中  $\frac{1}{sL}$  为电感的运算导纳,  $\frac{i(0_{-})}{s}$  表示附加电流源的电流。

![](../../raw/pages_0353-0384/images/page_355_image_8.jpg)

(a)

![](../../raw/pages_0353-0384/images/page_355_image_10.jpg)

<details>
<summary>text_image</summary>

I(s) sL - Li(0_) +
U(s) + -
</details>

(b)

![](../../raw/pages_0353-0384/images/page_355_image_12.jpg)

<details>
<summary>text_image</summary>

1/sL
i(0_)/s
I(s)
+
U(s)
-
</details>

(c)

图 14-3 电感的运算电路

同理,对于图 14-4(a) 所示,电容有  $u(t)=\frac{1}{C}\int_{0_{-}}^{t}i(\xi)\mathrm{d}\xi+u(0_{-})$ , 取拉氏变换并根据拉氏变换的积分性质, 得

$$
\left. \begin{array}{l} U (s) = \frac {1}{s C} I (s) + \frac {u (0 _ {-})}{s} \\ I (s) = s C U (s) - C u (0 _ {-}) \end{array} \right\} \tag {14-12}
$$

这样可以分别获得图 14-4(b)(c) 所示运算电路, 其中  $\frac{1}{sC}$  和 sC 分别为电容 C 的运算阻抗和运算导纳,  $\frac{u(0_{-})}{s}$  和  $Cu(0_{-})$  分别为反映电容初始电压的附加电压源的电压和附加电流源的电流。

![](../../raw/pages_0353-0384/images/page_355_image_18.jpg)

(a)

![](../../raw/pages_0353-0384/images/page_355_image_20.jpg)

<details>
<summary>text_image</summary>

I(s)
+   +   -   +
      1/sC       u(0_)
        /s
          U(s)
           -
           -
</details>

(b)

![](../../raw/pages_0353-0384/images/page_355_image_22.jpg)

<details>
<summary>text_image</summary>

+
sC
-
Cu(0_)
I(s)
+
U(s)
-
</details>

(c)

图 14-4 电容的运算电路

---

§ 14-4 运算电路

333

对两个耦合电感,运算电路中应包括由于互感引起的附加电源。根据图 14-5(a),有

$$
u _ {1} = L _ {1} \frac {\mathrm{d} i _ {1}}{\mathrm{d} t} + M \frac {\mathrm{d} i _ {2}}{\mathrm{d} t}
$$

$$
u _ {2} = L _ {2} \frac {\mathrm{d} i _ {2}}{\mathrm{d} t} + M \frac {\mathrm{d} i _ {1}}{\mathrm{d} t}
$$

对上式两边取拉氏变换有

$$
U _ {1} (s) = s L _ {1} I _ {1} (s) - L _ {1} i _ {1} (0 _ {-}) + s M I _ {2} (s) - M i _ {2} (0 _ {-})
$$

$$
U _ {2} (s) = s L _ {2} I _ {2} (s) - L _ {2} i _ {2} (0 _ {-}) + s M I _ {1} (s) - M i _ {1} (0 _ {-}) \tag {14-13}
$$

式中 $sM$ 称为互感运算阻抗，$Mi_{1}(0_{-})$ 和 $Mi_{2}(0_{-})$ 都是附加的电压源，附加电压源的方向与电流 $i_{1}, i_{2}$ 的参考方向有关。图 14-5(b) 为具有耦合电感的运算电路。

![](../../raw/pages_0353-0384/images/page_356_image_10.jpg)

<details>
<summary>text_image</summary>

i₁
+
M
i₂
+
u₁
L₁
L₂
u₂
-
</details>

(a)

![](../../raw/pages_0353-0384/images/page_356_image_12.jpg)

<details>
<summary>text_image</summary>

I₁(s)
+
sL₁
sM
I₂(s)
+
sL₂
U₁(s)
-
L₁i₁(0_)
+
-
L₂i₂(0_)
+
U₂(s)
Mi₂(0_)
+
-
Mi₁(0_)
+
</details>

(b)

图14-5 耦合电感的运算电路

图 14-6(a) 所示为 RLC 串联电路。设电源电压为  $u(t)$ ，电感中初始电流为  $i(0_{-})$ ，电容中初始电压为  $u_{c}(0_{-})$ 。如用运算电路表示，将得到图 14-6(b)。

![](../../raw/pages_0353-0384/images/page_356_image_16.jpg)

<details>
<summary>text_image</summary>

i(t)
+
u(t)
-
S
R
L
C
+
</details>

(a)

![](../../raw/pages_0353-0384/images/page_356_image_18.jpg)

<details>
<summary>text_image</summary>

I(s)
S
R
sL
+
U(s)
-
Li(0_)
-
1/sC
-
+
-
uC(0_)/s
</details>

(b)

图 14-6 RLC 串联电路

根据  $\sum U(s)=0$  , 有

$$
R I (s) + s L I (s) - L i (0 _ {-}) + \frac {1}{s C} I (s) + \frac {u _ {c} (0 _ {-})}{s} = U (s)
$$

---

334

第十四章 线性动态电路的复频域分析

或

$$
\left(R + s L + \frac {1}{s C}\right) I (s) = U (s) + L i (0 _ {-}) - \frac {u _ {c} (0 _ {-})}{s}
$$

$$
Z (s) I (s) = U (s) + L i (0 _ {-}) - \frac {u _ {c} (0 _ {-})}{s}
$$

式中 $Z(s) = R + sL + \frac{1}{sC}$ 为RLC串联电路的运算阻抗。在零值初始条件下，$i(0_{-}) = 0$，$u_{c}(0_{-}) = 0$，则有

$$
Z (s) I (s) = U (s)
$$

上式即为运算形式的欧姆定律。

## §14-5 应用拉普拉斯变换法分析线性电路

运算法与相量法的基本思想类似。相量法把正弦量变换为相量(复数)，从而把求解线性电路的正弦稳态问题归结为以相量为变量的线性代数方程。运算法把时间函数变换为对应的象函数，从而把问题归结为求解以象函数为变量的线性代数方程。当电路的所有独立初始条件为零时，电路元件VCR的运算形式与相量形式是类似的，加之KCL和KVL的运算形式与相量形式也是类似的，所以对于同一电路列出的零状态下的运算形式的方程和相量方程在形式上相似，但这两种方程具有不同的意义。在非零状态条件下，电路方程的运算形式中还应考虑附加电源的作用。当电路中的非零独立初始条件考虑成附加电源之后，电路方程的运算形式仍与相量方程类似。可见相量法中各种计算方法和定理在形式上完全可以移用于运算法。

在运算法中求得象函数之后,利用拉氏反变换就可以求得对应的时间函数。

根据上述思想,以下将通过一些实例说明拉氏变换法在线性电路分析中的应用。

例 14-9 图 14-7(a) 所示电路原处于稳态。t=0 时开关 S 闭合，试用运算法求解换路后的电流  $i_{L}(t)$ 。

![](../../raw/pages_0353-0384/images/page_357_image_14.jpg)

(a)

(b)

图14-7 例14-9图

解 首先求  $U_{s}$  的拉氏变换

---

§ 14-5 应用拉普拉斯变换法分析线性电路

335

$$
\mathcal {L} \left[ U _ {\mathrm{s}} \right] = \mathcal {L} \left[ 1 \right] = \frac {1}{s}
$$

1. 工程图

由于开关闭合前电路已处于稳态,所以电感电流  $i_{L}(0_{-})=0$ , 电容电压  $u_{C}(0_{-})=1\ V$ 。该电路的运算电路如图 14-7(b) 所示。

应用回路电流法,设回路电流为  $I_{\mathrm{a}}(s)$ 、 $I_{\mathrm{b}}(s)$ ,方向如图 14-7(b) 所示,可列出方程

$$
\begin{array}{l} \left(R _ {1} + s L + \frac {1}{s C}\right) I _ {\mathrm{a}} (s) - \frac {1}{s C} I _ {\mathrm{b}} (s) = \frac {1}{s} - \frac {u _ {c} (0 _ {-})}{s} \\ - \frac {1}{s C} I _ {\mathrm{a}} (s) + \left(R _ {2} + \frac {1}{s C}\right) I _ {\mathrm{b}} (s) = \frac {u _ {C} (0 _ {-})}{s} \\ \end{array}
$$

代入已知数据,得

$$
\begin{array}{l} \left(1 + s + \frac {1}{s}\right) I _ {\mathrm{a}} (s) - \frac {1}{s} I _ {\mathrm{b}} (s) = 0 \\ - \frac {1}{s} I _ {\mathrm{a}} (s) + \left(1 + \frac {1}{s}\right) I _ {\mathrm{b}} (s) = \frac {1}{s} \\ \end{array}
$$

解得

$$
I _ {L} (s) = I _ {\mathrm{a}} (s) = \frac {1}{s (s ^ {2} + 2 s + 2)}
$$

求其反变换

$$
\mathcal {L} ^ {- 1} \left[ I _ {L} (s) \right] = \frac {1}{2} (1 - \mathrm{e} ^ {- t} \cos t - \mathrm{e} ^ {- t} \sin t)
$$

所以 $i_{L}(t) = \frac{1}{2} (1 - \mathrm{e}^{-t}\cos t - \mathrm{e}^{-t}\sin t)\mathrm{A}\quad (t\geqslant 0)$

例 14-10 图 14-8(a) 所示为 RC 并联电路, 激励为电流源  $i_{\mathrm{s}}(t)$ , 若

(1)  $i_{\mathrm{S}}(t)=\varepsilon(t)\mathrm{A};$
(2)  $i_{\mathrm{S}}(t)=\delta(t)\mathrm{A}$ 。

试求电路响应  $u(t)$ 。

![](../../raw/pages_0353-0384/images/page_358_image_19.jpg)

<details>
<summary>text_image</summary>

i_S(t)
C
R
u(t)
+
</details>

(a)

![](../../raw/pages_0353-0384/images/page_358_image_21.jpg)

<details>
<summary>text_image</summary>

I_s(s)
1/sC
R
+
U(s)
-
</details>

(b)

图14-8 例14-10图

解 运算电路如图 14-8(b) 所示。

(1) 当  $i_{\mathrm{S}}(t)=\varepsilon(t)\mathrm{A}$  时，

---

336

第十四章 线性动态电路的复频域分析

$$
\begin{array}{l} I _ {s} (s) = \frac {1}{s} \\ U (s) = Z (s) I _ {\mathrm{s}} (s) = \frac {R \cdot \frac {1}{s C}}{R + \frac {1}{s C}} \cdot \frac {1}{s} \\ = \frac {1}{s C \left(s + \frac {1}{R C}\right)} = \frac {R}{s} - \frac {R}{s + \frac {1}{R C}} \\ \end{array}
$$

其反变换为

$$
u (t) = \mathscr {L} ^ {- 1} [ U (\dot {s}) ] = R (1 - \mathrm{e} ^ {- \frac {1}{R C} t}) \varepsilon (t) \mathrm{V}
$$

(2) 当  $i_{\mathrm{s}}(t)=\delta(t)\mathrm{A}$  时，

$$
I _ {s} (s) = 1
$$

$$
U (s) = Z (s) I _ {s} (s) = \frac {R \cdot \frac {1}{s C}}{R + \frac {1}{s C}}
$$

其反变换为

$$
u (t) = \frac {1}{C} \mathrm{e} ^ {- \frac {1}{R C} t} \varepsilon (t) \mathrm{V}
$$

以上结果分别为 RC 并联电路的阶跃响应和冲激响应。用拉氏变换法求得的结果与第七章的结果相同。

例 14-11 图 14-9(a) 所示电路中, 电路原处于稳态, t=0 时将开关 S 闭合, 求换路后的  $u_{L}(t)$ , 已知  $u_{S1}=2e^{-2t}V, u_{S2}=5V, R_{1}=R_{2}=5\Omega, L=1H$ 。

![](../../raw/pages_0353-0384/images/page_359_image_13.jpg)

<details>
<summary>text_image</summary>

S
R1
R2
(t=0)
iL
+
us1
-
L
uL
-
+
us2
-
</details>

(a)

![](../../raw/pages_0353-0384/images/page_359_image_15.jpg)

<details>
<summary>text_image</summary>

R₁
+
-
2/s+2.
Uₗ(s)
①
sL
-
Li(0_)
+
-
①
R₂
+
-
5/s
-
</details>

(b)

图14-9 例14-11图

解 与图 14-9(a) 相对应的运算电路见图 14-9(b), 其中

$$
\mathscr {L} \left[ u _ {\mathrm{S1}} \right] = \mathscr {L} \left[ 2 \mathrm{e} ^ {- 2 t} \right] = \frac {2}{s + 2}
$$

$$
\mathcal {L} \left[ u _ {\mathrm{s2}} \right] = \mathcal {L} \left[ 5 \right] = \frac {5}{s}
$$

---

§ 14-5 应用拉普拉斯变换法分析线性电路

337

电感电流的初始值为

$$
i _ {L} (0 _ {-}) = \frac {u _ {\mathrm{S2}}}{R _ {2}} = 1 \mathrm{A}
$$

应用节点法求解。设①点为参考节点，节点电压 $U_{\mathrm{n1}}(s)$ 就是 $U_{L}(s)$ 。有

$$
\left(\frac {1}{R _ {1}} + \frac {1}{R _ {2}} + \frac {1}{s L}\right) U _ {L} (s) = \frac {\frac {2}{s + 2}}{R _ {1}} + \frac {\frac {5}{s}}{R _ {2}} - \frac {L i (0 _ {-})}{s L}
$$

代入已知数据,得

$$
\left(\frac {2}{5} + \frac {1}{s}\right) U _ {L} (s) = \frac {2}{5 (s + 2)} + \frac {1}{s} - \frac {1}{s}
$$

$$
U _ {L} (s) = \frac {2 s}{(s + 2) (2 s + 5)}
$$

$$
u _ {L} (t) = \mathscr {L} ^ {- 1} [ U _ {L} (s) ] = (- 4 \mathrm{e} ^ {- 2 t} + 5 \mathrm{e} ^ {- 2. 5 t}) \mathrm{V} \quad (t \geqslant 0)
$$

例 14-12 图 14-10(a) 所示电路中, 已知  $R_{1}=R_{2}=1\ \Omega, L_{1}=L_{2}=0.1\ H, M=0.05\ H$  激励为直流电压  $U_{s}=1\ V, t=0$  时开关闭合, 试求换路后的电流  $i_{1}(t)$  和  $i_{2}(t)$ 。

![](../../raw/pages_0353-0384/images/page_360_image_11.jpg)

<details>
<summary>text_image</summary>

S
R₁
+
uₛ
-
i₁
M
L₁
L₂
i₂
R₂
</details>

(a)

![](../../raw/pages_0353-0384/images/page_360_image_13.jpg)

<details>
<summary>text_image</summary>

R₁
+
1/s
-
I₁(s)
sL₁
sM
sL₂
I₂(s)
R₂
</details>

(b)

图14-10 例14-12图

解 图 14-10(b) 为与图 14-10(a) 相应的运算电路。列出回路电流方程

$$
(R _ {1} + s L _ {1}) I _ {1} (s) - s M I _ {2} (s) = \frac {1}{s}
$$

$$
- s M I _ {1} (s) + (R _ {2} + s L _ {2}) I _ {2} (s) = 0
$$

代入已知数据,可得

$$
(1 + 0, 1 s) I _ {1} (s) - 0. 0 5 s I _ {2} (s) = \frac {1}{s}
$$

$$
- 0. 0 5 s I _ {1} (s) + (1 + 0. 1 s) I _ {2} (s) = 0
$$

解得

$$
I _ {1} (s) = \frac {0 . 1 s + 1}{s (0 . 7 5 \times 1 0 ^ {- 2} s ^ {2} + 0 . 2 s + 1)}
$$

$$
I _ {2} (s) = \frac {0 . 0 5 s}{0 . 7 5 \times 1 0 ^ {- 2} s ^ {2} + 0 . 2 s + 1}
$$

![](../../raw/pages_0353-0384/images/page_360_image_25.jpg)

<details>
<summary>natural_image</summary>

Pure technical line drawing of intersecting lines and shapes without any text, numbers, or symbols
</details>

---

338

第十四章 线性动态电路的复频域分析

$$
i _ {1} (t) = (1 - 0. 5 \mathrm{e} ^ {- 6. 6 7 t} - 0. 5 \mathrm{e} ^ {- 2 0 t}) \mathrm{A} \quad (t \geqslant 0)
$$

$$
i _ {2} (t) = 0. 5 (\mathrm{e} ^ {- 6. 6 7 t} - \mathrm{e} ^ {- 2 0 t}) \mathrm{A} \quad (t \geqslant 0)
$$

例 14-13 电路如图 14-11(a) 所示, 开关 S 原来闭合, t=0 时打开, 求换路后电路中的电流及电感元件上的电压。

解 $L_{1}$ 中的初始电流为 $\frac{U_{\mathrm{s}}}{R_1} = 5\mathrm{A},\mathrm{S}$ 打开后的运算如图14-11(b)所示，故

$$
I (s) = \frac {\frac {1 0}{s} + 5 L _ {1}}{R _ {1} + R _ {2} + s (L _ {1} + L _ {2})} = \frac {1 0 + 1 . 5 s}{s (5 + 0 . 4 s)}
$$

$$
= \frac {3 . 7 5 s + 2 5}{s (s + 1 2 . 5)} = \frac {2}{s} + \frac {1 . 7 5}{s + 1 2 . 5}
$$

$$
i (t) = (2 + 1. 7 5 \mathrm{e} ^ {- 1 2. 5 t}) \mathrm{A} \quad (t \geqslant 0)
$$

电流随时间变化的曲线如图 14-11(c) 所示。本题中  $L_{1}$  原有电流 5 A,  $L_{2}$  中没有电流，但开关打开后， $L_{1}$  和  $L_{2}$  的电流在  $t=0_{+}$ 时都被强制为同一电流，其数值为  $i(0_{+})=3.75\mathrm{~A}$ 。

![](../../raw/pages_0353-0384/images/page_361_image_11.jpg)

<details>
<summary>text_image</summary>

R₁ 2 Ω L₁ 0.3 H R₂ 3 Ω
+ Uₛ=10 V S L₂ 0.1 H
-
</details>

(a)

![](../../raw/pages_0353-0384/images/page_361_image_13.jpg)

<details>
<summary>text_image</summary>

I(s)
R₁
sL₁
L₁i₁(0₋)
+
R₂
10/s
-
sL₂
</details>

(b)

![](../../raw/pages_0353-0384/images/page_361_chart_15.jpg)

<details>
<summary>line</summary>

| t/s | i/A |
| --- | --- |
| 0 | 3.75 |
| ~100 | ~2.2 |
</details>

(c)

图14-11 例14-13图

可见两个电感的电流都发生了跃变。由于电流的跃变，电感 $L_{1}$ 和 $L_{2}$ 的电压 $u_{L_{1}}$ 和 $u_{L_{2}}$ 中将有冲激函数出现。电压 $u_{L_{1}}$ 和 $u_{L_{2}}$ 可求得如下:

$$
\begin{array}{l} U _ {L _ {1}} (s) = 0. 3 s I (s) - 1. 5 \\ = 0. 6 + \frac {0 . 3 s \times 1 . 7 5}{s + 1 2 . 5} - 1. 5 \\ = - \frac {6 . 5 6}{s + 1 2 . 5} - 0. 3 7 5 \\ \end{array}
$$

---

§ 14-5 应用拉普拉斯变换法分析线性电路

339

$$
U _ {L _ {2}} (s) = 0. 1 s I (s) = 0. 2 + \frac {0 . 1 7 5 s}{s + 1 2 . 5}
$$

$$
= - \frac {2 . 1 9}{s + 1 2 . 5} + 0. 3 7 5
$$

$$
u _ {L _ {1}} (t) = [ - 6. 5 6 \mathrm{e} ^ {- 1 2. 5 t} \varepsilon (t) - 0. 3 7 5 \delta (t) ] \mathrm{V}
$$

$$
u _ {L _ {2}} (t) = [ - 2. 1 9 \mathrm{e} ^ {- 1 2. 5 t} \dot {\varepsilon} (t) + 0. 3 7 5 \delta (t) ] \mathrm{V}
$$

$$
u _ {L _ {1}} (t) + u _ {L _ {2}} (t) = - 8. 7 5 \mathrm{e} ^ {- 1 2. 5 t} \varepsilon (t) \mathrm{V}
$$

可见  $u_{L_{1}} + u_{L_{2}}$  中并无冲激函数出现，这是因为虽然  $L_{1}$ 、 $L_{2}$  中的电流发生了跃变，因而分别有冲激电压出现，但两者大小相同而方向相反，故在整个回路中，不会出现冲激电压，保证满足 KVL。

从这个实例中可以看出,由于拉氏变换式中下限取 0,故自动地把冲激函数考虑进去,因此无须先求  $t=0_{+}$  时的跃变值。

例 14-14 图 14-12(a) 所示为含有受控源的零状态电路, 试求电容电压  $u_{c}(t)$ 。已知激励为  $u_{s}(t)=20\sin t\varepsilon(t)V$ 。

![](../../raw/pages_0353-0384/images/page_362_image_10.jpg)

图14-12 例14-14图

解 已知电路为零状态电路, $t \geqslant 0$ 时运算电路如图14-12(b)所示。以 $I_{1}(s)$ 、 $I_{2}(s)$ 为变量列得电路的KVL方程为

$$
\left(1 + 1 + \frac {1}{s}\right) I _ {1} (s) - \left(\frac {1}{s} + 1\right) I _ {2} (s) = U _ {\mathrm{S}} (s)
$$

$$
- \left(\frac {1}{s} + 1\right) I _ {1} (s) + \left(1 + \frac {1}{s} + \frac {1}{s}\right) I _ {2} (s) = - 2 U _ {c} (s)
$$

而 $U_{c}(s) = \frac{1}{s} [I_{1}(s) - I_{2}(s)]$

联立求解得

$$
U _ {c} (s) = \frac {1}{s ^ {2} + s + 1} U _ {\mathrm{s}} (s)
$$

而 $U_{\mathrm{s}}(s) = \frac{20}{s^2 + 1}$

---

340

第十四章 线性动态电路的复频域分析

所以 $U_{G}(s) = \frac{20}{(s^{2} + s + 1)(s^{2} + 1)} = 20\left(\frac{s + 1}{s^{2} + s + 1} -\frac{s}{s^{2} + 1}\right)$

$$
= 2 0 \left[ \frac {s + \frac {1}{2}}{\left(s + \frac {1}{2}\right) ^ {2} + \left(\frac {\sqrt {3}}{2}\right) ^ {2}} + \frac {1}{\sqrt {3}} \frac {\frac {\sqrt {3}}{2}}{\left(s + \frac {1}{2}\right) ^ {2} + \left(\frac {\sqrt {3}}{2}\right) ^ {2}} - \frac {s}{s ^ {2} + 1} \right]
$$

求 $U_{c}(s)$ 的反变换,则有

$$
u _ {c} (t) = \mathscr {L} ^ {- 1} [ U _ {c} (s) ] = 2 0 \mathrm{e} ^ {- \frac {1}{2} t} \left[ \cos \left(\frac {\sqrt {3}}{2} t\right) + \frac {1}{\sqrt {3}} \sin \left(\frac {\sqrt {3}}{2} t\right) \right] - 2 0 \cos t
$$

即 $u_{c}(t) = \left\{20\mathrm{e}^{-\frac{1}{2} t}\left[\cos \left(\frac{\sqrt{3}}{2} t\right) + \frac{1}{\sqrt{3}}\sin \left(\frac{\sqrt{3}}{2} t\right)\right] - 20\cos t\right\} \varepsilon (t)$ V.

第十四章采用拉普拉斯变换法分析动态电路，与第七章直接在时域通过微分方程求解分析不同，拉普拉斯变换法是建立动态电路的复频域模型，通过复数代数方程求解，先求得电路的复频域响应(象函数)，再通过拉普拉斯反变换求得电路的时域响应。对于动态电路的分析，还可以采用第十五章介绍的状态方程法。可见，同一电路问题可以采用不同方法获得解决，所谓条条道路通罗马。

## §14-6 网络函数的定义

在第十一章指出,线性电路在单一正弦激励下达到稳态时,其响应相量与激励相量之比定义为网络函数。这里讨论在 s 域的网络函数。

线性时不变电路在单一电源激励下,其零状态响应  $r(t)$  的象函数  $R(s)$  与激励  $e(t)$  的象函数  $E(s)$  之比定义为该电路的网络函数  $H(s)$ , 即

$$
H (s) \stackrel {\text {def}} {=} \frac {R (s)}{E (s)} \tag {14-14}
$$

由于激励  $E(s)$  可以是独立的电压源或独立的电流源, 响应  $R(s)$  可以是电路中任意两点之间的电压或任意一支路的电流, 故网络函数可能是驱动点阻抗(导纳)、转移阻抗(导纳)、电压转移函数或电流转移函数。

根据网络函数的定义,若  $E(s)=1$ , 则  $R(s)=H(s)$ , 即网络函数就是该响应的象函数, 而当  $E(s)=1$  时,  $e(t)=\delta(t)$ , 所以网络函数的原函数  $h(t)$  是电路的单位冲激响应, 即

$$
h (t) = \mathscr {L} ^ {- 1} [ H (s) ] \tag {14-15}
$$

例14-15 图14-13(a)中电路激励为 $i_{\mathrm{s}}(t) = \delta (t)$，求冲激激励下的电容电压 $u_{C}(t)$。

解 图 14-13(b)为其运算电路,由于此冲激响应与冲激电流激励属于同一端口,因而网络函数为驱动点阻抗,即

$$
H (s) = \frac {R (s)}{E (s)} = \frac {U _ {c} (s)}{1} = Z (s) = \frac {1}{s C + G} = \frac {1}{C} \cdot \frac {1}{s + \frac {1}{R C}}
$$

---

§ 14-6 网络函数的定义

341

$$
h (t) = u _ {C} (t) = \mathscr {L} ^ {- 1} [ H (s) ] = \mathscr {L} ^ {- 1} \left[ \frac {1}{C} \cdot \frac {1}{s + \frac {1}{R C}} \right] = \frac {1}{C} \mathrm{e} ^ {- \frac {1}{R C} t} \varepsilon (t)
$$

此结果与第七章所得的相同。

![](../../raw/pages_0353-0384/images/page_364_image_4.jpg)

<details>
<summary>text_image</summary>

i_S
G = 1/R
u_C + C
-
</details>

(a)

![](../../raw/pages_0353-0384/images/page_364_image_6.jpg)

<details>
<summary>text_image</summary>

I_s(s)
G
U_C(s) +
-
sC
</details>

(b)

图14-13 例14-15图

例14-16 图14-14(a)所示电路为一低通滤波电路，激励是电压源 $u_{1}(t)$ 。已知$L_{1} = 1.5\mathrm{H},C_{2} = \frac{4}{3}\mathrm{F},L_{3} = 0.5\mathrm{H},R = 1\Omega$ 。求电压转移函数 $H_{1}(s) = \frac{U_{2}(s)}{U_{1}(s)}$ 和驱动点导纳函数 $H_{2}(s) = \frac{I_{1}(s)}{U_{1}(s)}$ 。

![](../../raw/pages_0353-0384/images/page_364_image_10.jpg)

<details>
<summary>text_image</summary>

i₁(t) L₁ L₃
u₁(t) C₂ R i₂(t)
+ u₂(t)
</details>

(a)

![](../../raw/pages_0353-0384/images/page_364_image_12.jpg)

<details>
<summary>text_image</summary>

I₁(s) sL₁ sL₃
U₁(s) I₁(s) 1/sC₂ I₂(s) R I₂(s)
+ U₂(s)
</details>

(b)

图14-14 例14-16图

解 给定电路的运算电路如图 14-14(b) 所示。用回路电流法列出回路电流  $I_{1}(s)$  和  $I_{2}(s)$  的方程, 有

$$
\left(s L _ {1} + \frac {1}{s C _ {2}}\right) I _ {1} (s) - \frac {1}{s C _ {2}} I _ {2} (s) = U _ {1} (s)
$$

$$
- \frac {1}{s C _ {2}} I _ {1} (s) + \left(s L _ {3} + \frac {1}{s C _ {2}} + R\right) I _ {2} (s) = 0
$$

解得

$$
I _ {1} (s) = \frac {L _ {3} C _ {2} s ^ {2} + R C _ {2} s + 1}{D (s)} U _ {1} (s)
$$

$$
I _ {2} (s) = \frac {1}{D (s)} U _ {1} (s)
$$

其中 $D(s) = L_{1}L_{3}C_{2}s^{3} + RL_{1}C_{2}s^{2} + (L_{1} + L_{3})s + R$

而 $U_{2}(s) = RI_{2}(s)$

1. 工程图

---

342

第十四章 线性动态电路的复频域分析

代入数据后得

$$
D (s) = s ^ {3} + 2 s ^ {2} + 2 s + 1
$$

电压转移函数为

$$
H _ {1} (s) = \frac {U _ {2} (s)}{U _ {1} (s)} = \frac {1}{s ^ {3} + 2 s ^ {2} + 2 s + 1} = \frac {1}{(s + 1) (s ^ {2} + s + 1)}
$$

驱动点导纳函数为

$$
H _ {2} (s) = \frac {I _ {1} (s)}{U _ {1} (s)} = \frac {2 s ^ {2} + 4 s + 3}{3 (s ^ {3} + 2 s ^ {2} + 2 s + 1)}
$$

由以上的例题及网络函数的定义,可见对于由  $R、L(M)$ 、C 及受控源等元件组成的电路,网络函数是 s 的实系数有理函数,其分子和分母多项式的根或为实数或为共轭复数。另外,可以看出网络函数中不会出现激励的象函数。

根据网络函数的定义,还可以应用卷积定理求电路响应。从式(14-14)可知,网络响应  $R(s)$  为

$$
R (s) = E (s) H (s) \tag {14-16}
$$

求  $R(s)$  的拉氏反变换, 得到时域中的响应

$$
r (t) = \mathscr {L} ^ {- 1} [ E (s) H (s) ] = \int_ {0} ^ {t} e (t - \xi) h (\xi) \mathrm{d} \xi \tag {14-17}
$$

这里 $e(t)$ 为外施激励的时间函数形式，$h(t)$ 为网络的冲激响应，给定任何激励函数后，就可以求该网络的零状态响应。所以可以通过求网络函数 $H(s)$ 与任意激励的象函数 $E(s)$ 之积 $[R(s) = E(s)H(s)]$ 的拉氏反变换求得该网络在任何激励下的零状态响应。

## §14-7 网络函数的极点和零点

由于网络函数  $H(s)$  的分子和分母都是 s 的多项式, 故其一般形式可写为

$$
\begin{array}{l} H (s) = \frac {N (s)}{D (s)} = \frac {b _ {m} s ^ {m} + b _ {m - 1} s ^ {m - 1} + \cdots + b _ {0}}{a _ {n} s ^ {n} + a _ {n - 1} s ^ {n - 1} + \cdots + a _ {0}} \\ = H _ {0} \frac {\left(s - z _ {1}\right) \left(s - z _ {2}\right) \cdots \left(s - z _ {i}\right) \cdots \left(s - z _ {m}\right)}{\left(s - p _ {1}\right) \left(s - p _ {2}\right) \cdots \left(s - p _ {j}\right) \cdots \left(s - p _ {n}\right)} \\ = H _ {0} \frac {\prod_ {i = 1} ^ {m} (s - z _ {i})}{\prod_ {j = 1} ^ {n} (s - p _ {j})} \tag {14-18} \\ \end{array}
$$

其中 $H_0$ 为一常数，$z_1, z_2, \cdots, z_i, \cdots, z_m$ 是 $N(s) = 0$ 的根，$p_1, p_2, \cdots, p_j, \cdots, p_n$ 是 $D(s) = 0$ 的根。当 $s = z_i$ 时 $H(s) = 0$，故 $z_1, z_2, \cdots, z_i, \cdots, z_m$ 称为网络函数的零点。当 $s = p_j$ 时，$D(s) = 0, H(s)$ 将趋近无限大，故 $p_1, p_2, \cdots, p_j, \cdots, p_n$ 称为网络函数的极点。如果 $N(s)$ 和 $D(s)$ 分别有重根，则称之为重零点和重极点。

---

§ 14-7 网络函数的极点和零点

343

网络函数的零点和极点可能是实数、虚数或复数。如果以复数 $s$ 的实部 $\sigma$ 为横轴，虚部 $\mathrm{j}\omega$ 为纵轴，就得到一个复频率平面，简称为复平面或 $s$ 平面。在复平面上把 $H(s)$ 的零点用“$\circ$”表示，极点用“$\times$”表示，就得到网络函数的零、极点分布图。

例 14-17 图 14-15 所示电路含理想运算放大器, 已知  $u_{\mathrm{s}}(t)=2\varepsilon(t)\mathrm{V}$ , 试求电压转移函数  $H(s)=\frac{U_{2}(s)}{U_{s}(s)}$ , 并在复平面上绘出其零、极点图。

![](../../raw/pages_0353-0384/images/page_366_image_4.jpg)

<details>
<summary>text_image</summary>

1/2 F
C2
R3
0.5 Ω
① 1 F
C1
③
R2 1 Ω
uS(t)
+
-
R1
②
+
+
u2(t)
-
</details>

图14-15 例14-17图

解 对节点①、③分别列节点电压方程

$$
\begin{array}{l} \left(\frac {1}{R _ {1}} + \frac {1}{R _ {2}} + s C _ {1} + s C _ {2}\right) U _ {1} (s) - s C _ {1} U _ {3} (s) - s C _ {2} U _ {2} (s) = \frac {U _ {s} (s)}{R _ {1}} \\ - s C _ {1} U _ {1} (s) + \left(s C _ {1} + \frac {1}{R _ {3}}\right) U _ {3} (s) - \frac {1}{R _ {3}} U _ {2} (s) = 0 \\ \end{array}
$$

根据理想运算放大器的性质有

$$
U _ {3} (s) = 0
$$

解得 $U_{2}(s) = \frac{-\frac{C_{1}}{R_{1}}sU_{s}(s)}{s^{2}C_{1}C_{2} + s\frac{(C_{1} + C_{2})}{R_{3}} + \left(\frac{1}{R_{1}} + \frac{1}{R_{2}}\right)\frac{1}{R_{3}}}$

代入已知参数

$$
H (s) = \frac {U _ {2} (s)}{U _ {\mathrm{s}} (s)} = \frac {- 2 s}{s ^ {2} + 6 s + 8}
$$

该网络函数有1个零点， $z_{1} = 0$ ；有2个极点， $p_1 = -2, p_2 = -4$ 。其零、极点图如图14-16所示。

零、极点在 s 平面上的分布与网络的时域响应和正弦稳态响应有着密切的关系，后两节中将详细分析。

---

344

第十四章 线性动态电路的复频域分析

![](../../raw/pages_0353-0384/images/page_367_image_3.jpg)

<details>
<summary>text_image</summary>

jω
-4 -2 O σ
</details>

图14-16 例14-17零、极点图

## §14-8 极点、零点与冲激响应

根据网络函数的定义可知,电路的零状态响应的象函数

$$
R (s) = H (s) E (s) = \frac {N (s)}{D (s)} \cdot \frac {P (s)}{Q (s)}
$$

式中 $H(s) = \frac{N(s)}{D(s)}, E(s) = \frac{P(s)}{Q(s)}$，而 $N(s), D(s), P(s), Q(s)$ 都是 $s$ 的多项式。用部分分式法求响应的原函数时，$D(s)Q(s) = 0$ 的根将包含 $D(s) = 0$ 和 $Q(s) = 0$ 的根。响应中包含 $Q(s) = 0$ 的根的那些项属于强制分量，而包含 $D(s) = 0$ 的根（即网络函数的极点）的那些项则是自由分量或瞬态分量。

若网络函数为真分式且分母具有单根,则网络的冲激响应为

$$
h (t) = \mathcal {L} ^ {- 1} [ H (s) ] = \mathcal {L} ^ {- 1} \left[ \sum_ {i = 1} ^ {n} \frac {K _ {i}}{s - p _ {i}} \right] = \sum_ {i = 1} ^ {n} K _ {i} \mathrm{e} ^ {p _ {i} t} \tag {14-19}
$$

式中 $p_i$ 为 $H(s)$ 的极点。从式(14-19)可以看出，当 $p_i$ 为负实根时，$\mathrm{e}^{p_i t}$ 为衰减指数函数；当 $p_i$ 为正实根时，$\mathrm{e}^{p_i t}$ 为增长的指数函数；而且 $|p_i|$ 越大，衰减或增长的速度越快。这说明若 $H(s)$ 的极点都位于负实轴上，则 $h(t)$ 将随 $t$ 的增大而衰减，这种电路是稳定的；若有一个极点位于正实轴上，则 $h(t)$ 将随 $t$ 的增长而增长，这种电路是不稳定的。当极点 $p_i$ 为共轭复数时，根据式(14-19)可知 $h(t)$ 是以指数曲线为包络线的正弦函数，其实部的正或负确定增长或衰减的正弦项。当 $p_i$ 为虚根时，则将是纯正弦项。图14-17画出了网络函数的极点分别为负实数、正实数、虚数以及共轭复数时，对应的时域响应的波形。总之，只要极点位于左半平面，则 $h(t)$ 必随时间增长而衰减，故电路是稳定的。所以一个实际的线性电路，其网络函数的极点一定位于左半平面。

从式(14-19)还可以看出, $p_{i}$ 仅由电路的结构及元件值确定,因而将 $p_{i}$ 称为该电路变量的自然频率或固有频率, $p_{i}$ 也称为该电路的一个固有频率。因此,电路的固有频率就是该电路所有变量的固有频率。

由于一般情况下  $h(t)$  的特性就是时域响应中自由分量的特性,而强制分量的特点

---

§ 14-8 极点、零点与冲激响应

345

又仅仅决定于激励的变化规律,所以,根据  $H(s)$  的极点分布情况和激励的变化规律不难预见时域响应的全部特点。

![](../../raw/pages_0353-0384/images/page_368_image_3.jpg)

<details>
<summary>text_image</summary>

jω
O
t
O
t
O
σ
O
t
O
t
</details>

图14-17 极点与冲激响应的关系

例 14-18 RLC 串联电路接通恒定电压源  $U_{s}$ ，如图 14-18(a) 所示。根据网络函数  $H(s)=\frac{U_{c}(s)}{U_{s}(s)}$  的极点分布情况分析  $u_{c}(t)$  的变化规律。

![](../../raw/pages_0353-0384/images/page_368_image_6.jpg)

<details>
<summary>text_image</summary>

S(t=0)
R
L
Us
+
-
C
+
uc
-
</details>

(a)

![](../../raw/pages_0353-0384/images/page_368_image_8.jpg)

<details>
<summary>text_image</summary>

jω
p₁'
p₁
jωₐ
p₂"
p₁"
O
σ
p₂
p₂'
</details>

(b)

图14-18 例14-18图

![](../../raw/pages_0353-0384/images/page_368_image_11.jpg)

<details>
<summary>natural_image</summary>

Pure technical line drawing of intersecting lines and shapes without any text, numbers, or symbols
</details>

---

346

第十四章 线性动态电路的复频域分析

解 $H(s) = \frac{U_{c}(s)}{U_{s}(s)} = \frac{1}{R + sL + \frac{1}{sC}}\cdot \frac{1}{sC}$

$$
= \frac {1}{s ^ {2} L C + s R C + 1} = \frac {1}{L C} \frac {1}{\left(s - p _ {1}\right) \left(s - p _ {2}\right)}
$$

(1) 当  $0 < R < 2 \sqrt{\frac{L}{C}}$  时,  $p_{1,2} = -\delta \pm j \omega_{d}$ , 其中

$$
\delta = \frac {R}{2 L}, \omega_ {\mathrm{d}} = \sqrt {\omega_ {0} ^ {2} - \delta^ {2}}, \omega_ {0} = \frac {1}{\sqrt {L C}}
$$

这时 $H(s)$ 的极点位于左半平面，如图14-18(b)中的 $p_1, p_2$，因此 $u_c(t)$ 的自由分量 $u_c''(t)$ 为衰减的正弦振荡，其包络线的指数为 $\mathrm{e}^{-\delta t}$，振荡角频率为 $\omega_{\mathrm{d}}$ 且极点离开虚轴越远，振荡衰减越快。

（2）当 R=0 时， $\delta=0,\omega_{d}=\omega_{0}$ ，故  $p_{1,2}^{\prime}=\pm\mathrm{j}\omega_{0}$ ，这说明  $H(s)$  的极点位于虚轴上，因此， $u_{c}^{\prime\prime}(t)$  为等幅振荡且  $\omega_{d}$  的绝对值越大，等幅振荡的振荡频率越高。

(3) 当  $R > 2 \sqrt{\frac{L}{C}}$  时, 有

$$
\begin{array}{l} p _ {1} ^ {\prime \prime} = - \frac {R}{2 L} + \sqrt {\left(\frac {R}{2 L}\right) ^ {2} - \frac {1}{L C}} \\ p _ {2} ^ {\prime \prime} = - \frac {R}{2 L} - \sqrt {\left(\frac {R}{2 L}\right) ^ {2} - \frac {1}{L C}} \\ \end{array}
$$

此时  $H(s)$  的极点位于负实轴上，因此  $u_{c}^{\prime\prime}(t)$  是由 2 个衰减速度不同的指数函数组成。且极点离原点越远， $u_{c}^{\prime\prime}(t)$  衰减越快。

$u_{c}(t)$ 中的强制分量 $u_{c}^{\prime}(t)$ 取决于激励的情况,本例中 $u_{c}^{\prime}(t)=U_{s}$ 。

## §14-9 极点、零点与频率响应

如果用相量法求图 14-14(a) 所示电路在正弦稳态情况下的电压转移函数, 则图 14-14(b) 中的 $sL_{1}、\frac{1}{sC_{2}}$ 和 $sL_{3}$ 将分别是 $\mathrm{j}\omega L_{1}、\frac{1}{\mathrm{j}\omega C_{2}}$ 和 $\mathrm{j}\omega L_{3}$, 输入电压 $U_{1}(s)$ 和输出电压 $U_{2}(s)$ 将是相量 $\dot{U}_{1}$ 和 $\dot{U}_{2}$, 而回路电流将是相量 $\dot{I}_{1}$ 和 $\dot{I}_{2}$。不难求得

$$
\dot {I} _ {2} = \frac {1}{D (\mathrm{j} \omega)} \dot {U} _ {1}
$$

其中  $D(j\omega)=L_{1}L_{3}C_{2}(j\omega)^{3}+RL_{1}C_{2}(j\omega)^{2}+(L_{1}+L_{2})j\omega+R$

代入数据后,有

$$
\frac {\dot {U} _ {2}}{\dot {U} _ {1}} = \frac {1}{(\mathrm{j} \omega) ^ {3} + 2 (\mathrm{j} \omega) ^ {2} + 2 (\mathrm{j} \omega) + 1}
$$

---

§ 14-9 极点、零点与频率响应

347

可见,若把例14-16的解 $H_{1}(s)$ 中的s用jω代替,则 $H_{1}(j\omega)=\frac{\dot{U}_{2}}{\dot{U}_{1}}$ 。就是说,在 $s=j\omega$ 处计算所得网络函数 $H_{1}(s)$ 即 $H_{1}(j\omega)$ ,而 $H_{1}(j\omega)$ 是角频率为 $\omega$ 时正弦稳态情况下的输出相量与输入相量之比。

同理,有

$$
H _ {2} (\mathrm{j} \omega) = H _ {2} (s) \mid_ {s = \mathrm{j} \omega} = \frac {\dot {I} _ {1}}{\dot {U} _ {1}}
$$

上述结论在一般情况下也成立。所以，如果令网络函数  $H(s)$  中复频率 s 等于  $j\omega$ ，分析  $H(j\omega)$  随  $\omega$  变化的情况就可以预见相应的转移函数或驱动点函数在正弦稳态情况下随  $\omega$  变化的特性。

对于某一固定角频率  $\omega, H(j\omega)$  通常是一个复数, 即可以表示为

$$
H (\mathrm{j} \omega) = | H (\mathrm{j} \omega) | \mathrm{e} ^ {\mathrm{j} \varphi} = | H (\mathrm{j} \omega) | / \varphi (\mathrm{j} \omega) \tag {14-20}
$$

式中 $|H(\mathrm{j}\omega)|$ 为网络函数在频率 $\omega$ 处的模值，而 $\varphi = \arg [H(\mathrm{j}\omega)]$ 为网络函数在频率 $\omega$ 处的相位。将 $|H(\mathrm{j}\omega)|$ 随 $\omega$ 变化的关系称为幅值频率响应，简称幅频响应；$\arg [H(\mathrm{j}\omega)]$ 随 $\omega$ 变化的关系称为相位频率响应，简称相频特性。显然，这里关于 $H(\mathrm{j}\omega)$ 的定义和讨论与第十一章的内容是一致的。根据式(14-18)有

$$
H (\mathrm{j} \omega) = H _ {0} \frac { \prod_ {i = 1} ^ {m} (\mathrm{j} \omega - z _ {i})}{ \prod_ {j = 1} ^ {n} (\mathrm{j} \omega - p _ {j})}
$$

于是有

$$
\mid H (\mathrm{j} \omega) \mid = H _ {0} \frac {\prod_ {i = 1} ^ {m} \mid (\mathrm{j} \omega - z _ {i}) \mid}{\prod_ {j = 1} ^ {n} \mid (\mathrm{j} \omega - p _ {j}) \mid} \tag {14-21}
$$

$$
\arg \left[ H (\mathrm{j} \omega) \right] = \sum_ {i = 1} ^ {m} \arg \left(\mathrm{j} \omega - z _ {i}\right) - \sum_ {j = 1} ^ {n} \arg \left(\mathrm{j} \omega - p _ {j}\right)
$$

所以若已知网络函数的极点和零点，则按式(14-21)便可以计算对应的频率响应，同时还可以通过在 $s$ 平面上作图的方法定性描绘出频率响应。

例 14-19 图 14-19 为 RC 串联电路, 试定性分析以电压  $u_{2}$  为输出时该电路的频率响应。

解 以 $u_{2}$ 为电路变量的网络函数为

$$
H (s) = \frac {U _ {2} (s)}{U _ {1} (s)} = \frac {\frac {1}{R C}}{s + \frac {1}{R C}}
$$

![](../../raw/pages_0353-0384/images/page_370_image_17.jpg)

<details>
<summary>text_image</summary>

R
+
u₁
-
C
+
u₂
-
</details>

图14-19 例14-19图

---

348

第十四章 线性动态电路的复频域分析

其极点  $p_{1}=-\frac{1}{RC}$ ，如图 14-20(a). 所示。

将  $H(s)$  中 s 用  $j\omega$  代替, 得

$$
H (\mathrm{j} \omega) = \frac {\frac {1}{R C}}{\mathrm{j} \omega + \frac {1}{R C}}
$$

$H(\mathrm{j}\omega)$ 在 $\omega = \omega_{1},\omega_{2}$ 和 $\omega_{3}$ 时的模值分别为 $\frac{1}{RC}$ 除以图14-20(a)中的线段长度 $M_{1},M_{2}$ 和$M_3$ ，对应的相位分别为同图中的 $\theta_{1},\theta_{2}$ 和 $\theta_{3}$ 的负值。随 $\omega$ 从零沿虚轴向 $\infty$ 增长时，$|H(\mathrm{j}\omega)|$ 趋于零，而相位从零趋近- $90^{\circ}$ 。由此定性画出的幅频特性和相频特性分别如图14-20(b)和(c)所示。

![](../../raw/pages_0353-0384/images/page_371_image_7.jpg)

<details>
<summary>text_image</summary>

jω
jω₃
M₃
jω₂
M₂
jω₁
M₁
θ₁ θ₂ θ₃
-1/RC O σ
</details>

(a)

![](../../raw/pages_0353-0384/images/page_371_chart_9.jpg)

<details>
<summary>line</summary>

| 0 | 1 |
| --- | --- |
| \(\omega1\) | ~0.85 |
| \(\omega2\) | ~0.65 |
| \(\omega3\) | ~0.45 |
</details>

(b)

![](../../raw/pages_0353-0384/images/page_371_chart_11.jpg)

<details>
<summary>line</summary>

| Point | \(\omega\) | \(\theta\) |
| --- | --- | --- |
| Start | 0 | 0 |
| \(\omega_{1}\) | \(\omega_{1}\) | ~\(\pi/2\) |
| \(\omega_{2}\) | \(\omega_{2}\) | ~\(\pi/4\) |
| \(\omega_{3}\) | \(\omega_{3}\) | ~\(\pi/8\) |
</details>

(c)

图14-20 $RC$ 串联电路的频率响应

可以看出，该电路具有低通特性。当 $\omega = 0$ 时，$\frac{\dot{U}_2}{\dot{U}_1} = 1 / 0^\circ$；$\omega = \frac{1}{RC}$ 时，$\frac{\dot{U}_2}{\dot{U}_1} = \frac{1}{1 + j} = \frac{1}{\sqrt{2}} / -45^\circ$，即 $\frac{U_2}{U_1} = 0.707$，相当于 $\omega = 0$ 时模值的 0.707，此频率有时称为低通滤波电路的

---

§ 14-9 极点、零点与频率响应

349

截止频率,用  $\omega_{c}$  表示,而 0 到  $\omega_{c}$  的频率范围称为通频带。

例 14-20 图 14-21(a) 所示为 RLC 串联电路, 设电容电压为输出电压  $u_{2}$ , 电压转移函数  $H(s)=\frac{U_{2}(s)}{U_{1}(s)}$ ; 试根据该网络函数的极点和零点, 定性地绘出  $H(j\omega)$ 。

解 $H(s) = \frac{U_2(s)}{U_1(s)} = \frac{\frac{1}{sC}}{R + sL + \frac{1}{sC}}$

$$
\begin{array}{l} = \frac {1}{L C} \frac {1}{(s - p _ {1}) (s - p _ {2})} \\ = H _ {0} \frac {1}{(s - p _ {1}) (s - p _ {2})} \\ \end{array}
$$

令 $s = \mathrm{j}\omega$ ，有

$$
\frac {\dot {U} _ {2}}{\dot {U} _ {1}} = H (\mathrm{j} \omega) = H _ {0} \frac {1}{(\mathrm{j} \omega - p _ {1}) (\mathrm{j} \omega - p _ {2})}
$$

设极点为一对共轭复数,即

$$
p _ {1, 2} = - \frac {R}{2 L} \pm \mathrm{j} \sqrt {\frac {1}{L C} - \left(\frac {R}{2 L}\right) ^ {2}} = - \delta \pm \mathrm{j} \omega_ {\mathrm{d}}
$$

式中 $\omega_{\mathrm{d}} = \sqrt{\omega_0^2 - \delta^2}$，而 $\omega_0 = \frac{1}{\sqrt{LC}} = \sqrt{\omega_{\mathrm{d}}^2 + \delta^2}$。当 $\omega = \omega_{1}$ 时，有[如图14-21(b)所示]

$$
\mid H (\mathrm{j} \omega_ {1}) \mid = \frac {H _ {0}}{\mid \mathrm{j} \omega_ {1} - p _ {1} \mid \mid \mathrm{j} \omega_ {1} - p _ {2} \mid} = \frac {H _ {0}}{M _ {1} M _ {2}}
$$

$$
\arg \bigl [ H (\mathrm{j} \omega) \bigr ] = - (\theta_ {1} + \theta_ {2})
$$

定性绘出幅频特性和相频特性如图 14-21(c)(d) 所示。

从上述分析中可以看出, 当 $p_1, p_2$ 远离虚轴, 如图 14-21(b) 所示位置时, 随 $\omega$ 变化的 $M_1$ 和 $M_2$ 的变化几乎相等, 可以看到没有一个极点对频率响应起主要作用。如果极点位置如图 14-21(e) 所示, 即极点 $p_1, p_2$ 接近 j$\omega$ 轴, 则在 j$\omega$ 与 $p_1$ 之间的向量 $M_1$ 的长度和角度对 $|H(j\omega)|$ 和 $\arg[H(j\omega)]$ 都产生较大的影响, 而 $M_2$ 却改变较少。经分析计算可得到, 当 $\omega \approx \omega_0$ 时, $|H(j\omega)|$ 达到峰值, 而 $\omega = \omega_0 = \frac{1}{\sqrt{LC}}$ 为 RLC 串联电路的谐振角频率。因此, 当极点为共轭复数时, 极点到坐标原点的距离与极点的实部之比对网络的频率响应影响很大, 有时把此值的一半, 即 $\frac{\omega_0}{2\delta}$ 定义为极点的品质因数, 以 $Q_p$ 表示。对于二阶电路

---

350

第十四章 线性动态电路的复频域分析

$$
Q _ {p} = \frac {\omega_ {0}}{2 \delta} = \frac {\omega_ {0} L}{R} = \frac {1}{R} \sqrt {\frac {L}{C}} = Q
$$

可以看出  $Q_{p}=Q$ ，而 Q 即回路的品质因数。

![](../../raw/pages_0353-0384/images/page_373_image_5.jpg)

<details>
<summary>text_image</summary>

R
L
+
u₁
-
C
+
u₂
-
</details>

(a)

![](../../raw/pages_0353-0384/images/page_373_image_7.jpg)

<details>
<summary>text_image</summary>

jω
P₁
θ₁
M₁
O
σ
M₂
θ₂
P₂
</details>

(b)

![](../../raw/pages_0353-0384/images/page_373_chart_9.jpg)

<details>
<summary>line</summary>

| 0 | 1 |
| --- | --- |
| ~0.25 | ~0.9 |
| ~0.5 | ~0.6 |
| ~0.75 | ~0.3 |
| 1 | ~0.1 |
</details>

(c)

![](../../raw/pages_0353-0384/images/page_373_chart_11.jpg)

<details>
<summary>line</summary>

| \(\omega\) | \(arg[H(j\omega)]\) |
| --- | --- |
| 0 | 0 |
| \(\omega_{0}\) | \(\pi/2\) |
| \(>\omega_{0}\) | \(-\pi\) |
</details>

(d)

![](../../raw/pages_0353-0384/images/page_373_image_13.jpg)

<details>
<summary>text_image</summary>

jω
p₁
M₁
θ₁
O
σ
M₂
θ₂
p₂
</details>

(e)

![](../../raw/pages_0353-0384/images/page_373_chart_15.jpg)

<details>
<summary>line</summary>

| 0 | 1 | 1 |
| --- | --- | --- |
| \(\omega0\) | ~0.8 | ~1.4 |
</details>

(f)

图14-21 例14-20图

根据第十一章讨论可知,对例14-20中的电路,当 $Q_{p}<\frac{1}{\sqrt{2}}$ 时, $|H(j\omega)|$ 随 $\omega$ 的增长而单调减小,如图14-21(c)所示,而当 $Q_{p}$ 增大时, $|H(j\omega)|$ 出现峰值,如图14-21(f)所示,且峰值随 $Q_{p}$ 的增大而增大,峰值对应的频率值 $\omega$ 随 $Q_{p}$ 的增大而趋于 $\omega_{0}$ 。

---

习题

351

1. 工程图

![](../../raw/pages_0353-0384/images/page_374_image_3.jpg)

## 思考题

14-1 在应用拉普拉斯变换法分析含有耦合电感的电路时,一种方法是直接分析,一种是用去耦等效电路分析,试比较这两种方法在处理附加电源的方法上有何不同。

14-2 试比较经典法和运算法两种方法,总结一下什么情况宜用经典法,什么情况宜用运算法。

14-3 当激励是冲激函数时,试比较用经典法和拉普拉斯变化法求解的结果是否完全相同。为什么？

14-4 求拉普拉斯反变换,除了本章介绍的部分分式展开法外,试采用复变函数中的方法。

14-5 试分析网络函数的零、极点在复平面不同位置时,对网络函数的影响。

14-6 对于线性电路,我们总可以获得某个网络函数,例如它是电路中一条支路上的电压与电压源电压之比。请说明在相同激励位置施加正弦电压激励时,若电路达到稳态,在响应位置处电压与网络函数的关系。

![](../../raw/pages_0353-0384/images/page_374_image_11.jpg)

## 习题

14-1 求下列各函数的象函数:

(1) $f(t) = 1 - \mathrm{e}^{-at}$

(2) $f(t) = \sin (\omega t + \varphi)$

(3) $f(t) = \mathrm{e}^{-at}(1 - at)$

(4) $f(t) = \frac{1}{a} (1 - \mathrm{e}^{-at})$

(5) $f(t) = t^2$

(6) $f(t) = t + 2 + 3\delta (t)$

(7) $f(t) = t\cos (at)$

(8) $f(t) = \mathrm{e}^{-at} + at - 1$

14-2 求下列各函数的原函数:

(1) $\frac{(s + 1)(s + 3)}{s(s + 2)(s + 4)}$

(2) $\frac{2s^2 + 16}{(s^2 + 5s + 6)(s + 12)}$

(3) $\frac{2s^2 + 9s + 9}{s^2 + 3s + 2}$

(4) $\frac{s^3}{(s^2 + 3s + 2)s}$

14-3 求下列各函数的原函数:

(1) $\frac{1}{(s + 1)(s + 2)^2}$

(2) $\frac{(s + 1)}{s^3 + 2s^2 + 2s}$

(3) $\frac{s^2 + 6s + 5}{s(s^2 + 4s + 5)}$

(4) $\frac{s}{(s^2 + 1)^2}$

---

352

第十四章 线性动态电路的复频域分析

14-4 题 14-4 图 (a)(b)(c) 所示电路原已达稳态, t=0 时把开关 S 合上, 分别画出运算电路。

![](../../raw/pages_0353-0384/images/page_375_image_4.jpg)

<details>
<summary>text_image</summary>

1 H
- 5 V +
1 Ω
S
2 Ω
2 F
10 V +
-
2 H
1 Ω
+
1 V -
1 F
+
6 V -
2 Ω
</details>

(a)

![](../../raw/pages_0353-0384/images/page_375_image_6.jpg)

<details>
<summary>text_image</summary>

2 A
1 Ω
1 H
1 H
S
+
1 V
-
1 F
</details>

(b)

![](../../raw/pages_0353-0384/images/page_375_image_8.jpg)

<details>
<summary>text_image</summary>

0.5 H
1H
1H
1Ω
S
1F
1F
3Ω
+
-
10 V
</details>

(c)

题14-4图

14-5 题 14-5 图所示电路原处于零状态, t=0 时合上开关 S, 试求电流  $i_{L}$ 。
14-6 电路如题 14-6 图所示, 已知  $i_{L}(0_{-}) = 0 \mathrm{~A}, t = 0$  时将开关 S 闭合, 求 t > 0 时的  $u_{L}(t)$ 。

![](../../raw/pages_0353-0384/images/page_375_image_14.jpg)

<details>
<summary>text_image</summary>

S
(t=0)
50 Ω
+
50 V
-
1.33 H
iL
100 μF
-
</details>

题 14-5 图

![](../../raw/pages_0353-0384/images/page_375_image_16.jpg)

<details>
<summary>text_image</summary>

4Ω
2u₁ +
S
(t=0)
10e⁻ᵗ V
+
-
4Ω
u₁ +
-
1 H
uₗ
-
</details>

题14-6图

14-7 电路如题 14-7 图所示, 设电容上原有电压  $U_{c0}=100\ V$ , 电源电压  $U_{s}=200\ V, R_{1}=30\ \Omega, R_{2}=10\ \Omega, L=0.1\ H, C=1\ 000\ \mu F$ 。求 S 合上后电感中的电流  $i_{L}(t)$ 。
14-8 题 14-8 图所示电路中的储能元件均为零初始值, $u_{s}(t)=5\varepsilon(t)\mathrm{V}$ , 在下列条件下求  $U_{1}(s)$ :

(1) $r = -3\Omega_{\circ}$.
(2)  $r=3\ \Omega_{0}$

---

习题

353

![](../../raw/pages_0353-0384/images/page_376_image_2.jpg)

<details>
<summary>text_image</summary>

R₁
iₗ
L
Uₛ
+
-
S
-
C
Uc₀
+
R₂
</details>

题14-7图

![](../../raw/pages_0353-0384/images/page_376_image_4.jpg)

<details>
<summary>text_image</summary>

i₁ 1 Ω
+ uₛ -
1 H
1 Ω
+
- ri₁ +
1 Ω
u₁ 1 F
-
2 Ω
</details>

题14-8图

14-9 题 14-9 图所示电路中， $i_{\mathrm{S}} = 2 \sin (1000 t) \mathrm{~A}, R_{1} = R_{2} = 20 \Omega, C = 1000 \mu \mathrm{F}, t = 0$ 时合上开关 S，用运算法求 $u_{C}(t)$ 。
14-10 题 14-10 图所示电路中  $L_{1}=1\ H, L_{2}=4\ H, M=2\ H, R_{1}=R_{2}=1\ \Omega, U_{s}=1\ V$ ，电感中原无磁场能量。t=0 时合上开关 S，用运算法求  $i_{1}, i_{2}$ 。

![](../../raw/pages_0353-0384/images/page_376_image_9.jpg)

<details>
<summary>text_image</summary>

i_S
R_1
C
+
u_C
-
R_2
S
</details>

题14-9图

![](../../raw/pages_0353-0384/images/page_376_image_11.jpg)

<details>
<summary>text_image</summary>

S
R₁
+
Uₛ
-
i₁
L₁
M
L₂ i₂
R₂
</details>

题 14-10 图

14-11 题图 14-11 所示电路, 当 t<0 时开关 S 打开, 电路已稳定; 当 t=0 时闭合开关 S。求当 t>0 时的电流  $i_{2}(t)$ 。

![](../../raw/pages_0353-0384/images/page_376_image_14.jpg)

<details>
<summary>text_image</summary>

+
10 V
-
2.5 Ω
S
2.5 Ω
3 H
2 H
i₂(t)
3 H
2.5 Ω
</details>

题14-11图

14-12 题图 14-12 所示电路含理想运算放大器, 已知 $R_{1} = 1 \mathrm{k} \Omega, R_{2} = 2 \mathrm{k} \Omega, C_{1} = 1 \mu \mathrm{F}, C_{2} = 2 \mu \mathrm{F}, u_{\mathrm{S}}(t) = 2 \varepsilon(t) \mathrm{~V}$, 试求电压 $u_{2}(t)$。
14-13 题图 14-13 所示电路含理想变压器, 已知 $R = 1 \Omega, C_1 = 1 \mathrm{~F}, C_2 = 2 \mathrm{~F}$, $i_{\mathrm{S}}(t) = \mathrm{e}^{-t} \varepsilon(t) \mathrm{~V}$, 试求电路的零状态响应 $u(t)$。

---

图 3-1

354

第十四章 线性动态电路的复频域分析

![](../../raw/pages_0353-0384/images/page_377_image_3.jpg)

<details>
<summary>text_image</summary>

i₁(t)
C₁
R₁
R₂
C₂
uₛ(t)
+
-
∞
+
+
u₂(t)
</details>

题 14-12 图

![](../../raw/pages_0353-0384/images/page_377_image_5.jpg)

<details>
<summary>text_image</summary>

i_S(t)
+
u(t)
-
R
1:2
C_1
C_2
</details>

题 14-13 图

14-14 题 14-14 图(a)所示电路激励  $u_{\mathrm{s}}(t)$  的波形如题 14-14 图(b)所示, 已知  $R_{1}=6\Omega, R_{2}=3\Omega, L=1\mathrm{H}, \mu=1$ , 求电路的零状态响应  $i_{L}(t)$ 。

![](../../raw/pages_0353-0384/images/page_377_image_8.jpg)

<details>
<summary>text_image</summary>

uS(t)
+
-
R1
+
uL(t)
-
L
R2
+
μuL(t)
-
iL(t)
</details>

(a)

![](../../raw/pages_0353-0384/images/page_377_chart_10.jpg)

<details>
<summary>line</summary>

| t/s | uS(t)/V |
| --- | --- |
| 0 | 0 |
| 1 | 1 |
</details>

(b)

题 14-14 图

14-15 题 14-15 图所示各电路在 t=0 时合上开关 S，用运算法求  $i(t)$  及  $u_{c}(t)$ 。

![](../../raw/pages_0353-0384/images/page_377_image_14.jpg)

<details>
<summary>text_image</summary>

100 V
+
-
S
3 μF
i
3 μF
+
uc
-
</details>

(a)

![](../../raw/pages_0353-0384/images/page_377_image_16.jpg)

<details>
<summary>text_image</summary>

2 Ω
0.5 F
S
+
4 V
-
1 F
1 F
i
+
uC
-
</details>

(b)

题14-15图

14-16 电路如题14-16图所示，已知 $u_{\mathrm{S1}}(t) = \varepsilon (t)\mathrm{V},u_{\mathrm{S2}}(t) = \delta (t)\mathrm{V}$ ，试求 $u_{1}(t)$ 和 $u_{2}(t)$ 。

![](../../raw/pages_0353-0384/images/page_377_image_20.jpg)

<details>
<summary>text_image</summary>

1 Ω
1 Ω
+
us1
-
1 F
+
u1
-
1 F
+
u2
-
1 Ω
+
us2
-
</details>

题14-16图

---

习题

355

14-17 电路如题 14-17 图所示, 已知 $u_{\mathrm{S}}(t) = [\varepsilon(t) + \varepsilon(t - 1) - 2\varepsilon(t - 2)] \mathrm{~V}$, 求 $i_{L}(t)$。
14-18 电路如题 14-18 图所示, 开关 S 原是闭合的, 电路处于稳态。若 S 在 t=0 时打开, 已知  $U_{S}=2\ V, L_{1}=L_{2}=1\ H, R_{1}=R_{2}=1\ \Omega$ 。试求  $t\geqslant0$  时的  $i_{1}(t)$  和  $u_{L_{2}}(t)$ 。

![](../../raw/pages_0353-0384/images/page_378_image_5.jpg)

<details>
<summary>text_image</summary>

1 Ω
+
us
-
5 H
iL
- 5 Ω
</details>

题 14-17 图

![](../../raw/pages_0353-0384/images/page_378_image_7.jpg)

<details>
<summary>text_image</summary>

+ uL2 -
R2
i1
L2
+
us
-
R1
L1
S(t=0)
</details>

题 14-18 图

14-19 题 14-19 图所示电路中 $U_{\mathrm{s}}$ 为恒定值, $u_{C_2}(0_-) = 0$, 开关闭合前电路已达稳态, $t = 0$ 时 S 闭合, 求开关闭合后, 电容电压 $u_{C_1}$ 和 $u_{C_2}$, 电流 $i_{C_1}$ 和 $i_{C_2}$。
14-20 题 14-20 图所示电路中两电容原来未充电，在 t=0 时将开关 S 闭合，已知  $U_{S}=10\ V, R=5\ \Omega, C_{1}=2\ F, C_{2}=3\ F$ 。求  $t\geqslant0$  时的  $u_{C_{1}}, u_{C_{2}}$  及  $i_{1}, i_{2}, i_{0}$ 。

![](../../raw/pages_0353-0384/images/page_378_image_12.jpg)

<details>
<summary>text_image</summary>

R
+
Us
-
iC1
+
uc1
-
C1
S
(t=0)
iC2
+
uc2
-
C2
</details>

题 14-19 图

![](../../raw/pages_0353-0384/images/page_378_image_14.jpg)

<details>
<summary>text_image</summary>

S
(t=0)
+
Us
-
i₁
+
uC₁
-
C₁
i
R
i₂
u_C₂
+
C₂
-
</details>

题 14-20 图

14-21 电路如题 14-21 图所示, 已知电容 $C_{1}$ 和 $C_{2}$ 原带电荷, 方向如图所示, $C_{1} = 3 \mathrm{~F}, q_{c_{1}}(0_{-}) = 15 \mathrm{~C}, C_{2} = 6 \mathrm{~F}, q_{c_{2}}(0_{-}) = 60 \mathrm{~C}, t = 0$ 时, 开关 S 闭合, 求开关 S 闭合后电压 $u(t)$。

![](../../raw/pages_0353-0384/images/page_378_image_17.jpg)

<details>
<summary>text_image</summary>

10 V
+
-
5 Ω
qC1(0_)
+
C1
-
uC1
+
-
uC2
qC2(0_)
+
C2
-
uC2
u(t)
+
10uC2
-
S
</details>

题 14-21 图

1. 用 $\mathrm{H}_{2}$ 气体中加入一个液体，使气体浓度从 $\mathrm{H}_{2}$ 气体中的 $\mathrm{H}_{2}$ 气体的体积逐渐减小。

---

356

第十四章 线性动态电路的复频域分析

14-22 绘出 $H(s) = \frac{2s^2 - 12s + 16}{s^3 + 4s^2 + 6s + 3}$ 的零、极点图。
14-23 试求题 14-23 图所示线性一端口网络的驱动点阻抗  $Z(s)$  的表达式，并在 s 平面上绘出极点和零点。已知  $R=1\Omega, L=0.5H, C=0.5F$ 。

![](../../raw/pages_0353-0384/images/page_379_image_6.jpg)

<details>
<summary>text_image</summary>

L
R
</details>

(a)

![](../../raw/pages_0353-0384/images/page_379_image_8.jpg)

<details>
<summary>text_image</summary>

R
L
C
</details>

(b)

![](../../raw/pages_0353-0384/images/page_379_image_10.jpg)

<details>
<summary>text_image</summary>

R
L
C
R
</details>

(c)

题 14-23 图

14-24 求题 14-24 图所示各电路的驱动点阻抗  $Z(s)$  的表达式，并在 s 平面上绘出极点和零点。

![](../../raw/pages_0353-0384/images/page_379_image_14.jpg)

<details>
<summary>text_image</summary>

1 Ω
3 F
Z₁ →
2 H
4 Ω
</details>

(a)

![](../../raw/pages_0353-0384/images/page_379_image_16.jpg)

<details>
<summary>text_image</summary>

0.5 H
Zi → 3u1 1 Ω + u1 -
1 F
</details>

(b)

题 14-24 图

14-25 题 14-25 图所示为一线性电路, 输入电流源的电流为  $i_{s}$ 。

(1) 试计算驱动点阻抗  $Z_{\mathrm{d}}(s)=\frac{U_{1}(s)}{I_{\mathrm{s}}(s)}$ 。
(2) 试计算转移阻抗  $Z_{1}(s)=\frac{U_{2}(s)}{I_{s}(s)}$ 。
(3) 在 s 平面上绘出  $Z_{\mathrm{d}}(s)$  和  $Z_{\mathrm{t}}(s)$  的极点和零点。

![](../../raw/pages_0353-0384/images/page_379_image_24.jpg)

<details>
<summary>text_image</summary>

+
i_s
u_1
-
96/55 Ω
0.2 H
96/125 H
1/11 F
+
u_2
-
</details>

题 14-25 图

14-26 电路如题 14-26 图所示, 已知 $u_{\mathrm{S}}(t) = 4\varepsilon(t)\mathrm{~V}$。(1) 求网络函数 $H(s) = \frac{U_{\mathrm{o}}(s)}{U_{\mathrm{a}}(s)}$。(2) 绘出 $H(s)$ 的零、极点图。

---

习题

357

1. 用 $\mathrm{H}_2\mathrm{O}$ 气体分解出氢气的气体，用于吸收和处理过程中的气体。

![](../../raw/pages_0353-0384/images/page_380_image_3.jpg)

<details>
<summary>text_image</summary>

1 Ω
+
us(t)
-
+
uc=2F
-
2uc
2F uO(t)
+
-
</details>

题 14-26 图

14-27 题 14-27 图所示为 RC 电路, 求它的转移函数  $H(s)=\frac{U_{o}(s)}{U_{i}(s)}$ 。

14-28 题 14-28 图所示电路中, $L = 0.2 \mathrm{H}, C = 0.1 \mathrm{~F}, R_{1} = 6 \Omega, R_{2} = 4 \Omega, u_{\mathrm{s}}(t) = 7 \mathrm{e}^{-2 t} \mathrm{V}$, 求 $R_{2}$ 中的电流 $i_{2}(t)$, 并求网络函数 $H(s) = \frac{I_{2}(s)}{U_{s}(s)}$ 及单位冲激响应。

![](../../raw/pages_0353-0384/images/page_380_image_7.jpg)

<details>
<summary>text_image</summary>

R₁
C₁
+
u₁
R₂
C₂
uₒ
-
</details>

题14-27图

![](../../raw/pages_0353-0384/images/page_380_image_9.jpg)

<details>
<summary>text_image</summary>

L
C
+
us
-
R1
i2
R2
</details>

题14-28图

14-29 已知网络函数为

(1)  $H(s)=\frac{2}{s-0.3}$ 。
(2) $H(s) = \frac{s - 5}{s^2 - 10s + 125}$。
(3)  $H(s)=\frac{s+10}{s^{2}+20s+500}$ 。

试定性作出单位冲激响应的波形。

14-30 设某线性电路的冲激响应 $h(t) = \mathrm{e}^{-t} + 2\mathrm{e}^{-2t}$，试求相应的网络函数，并绘出零、极点图。

14-31 设网络的冲激响应为

(1)  $h(t)=\delta(t)+\frac{3}{5}e^{-t}$ 。
(2)  $h(t)=\mathrm{e}^{-at}\sin(\omega t+\theta)$ 。
(3)  $h(t)=\frac{3}{5}\mathrm{e}^{-t}-\frac{7}{9}t\mathrm{e}^{-3t}+3t_{0}$

---

358

第十四章 线性动态电路的复频域分析

试求相应的网络函数的极点。

14-32 画出与题 14-32 图所示零、极点分布相应的幅频响应  $\left|H(j\omega)\right|-\omega$  曲线。

![](../../raw/pages_0353-0384/images/page_381_image_5.jpg)

题 14-32 图

14-33 已知电路如题 14-33 图所示, 求网络函数  $H(s)=\frac{U_{2}(s)}{U_{a}(s)}$ , 定性画出幅频特性和相频特性示意图。
14-34 题 14-34 图所示电路为 RLC 并联电路, 试用网络函数的图解法分析  $H(s)=\frac{U_{2}(s)}{I_{8}(s)}$  的频率响应特性。

![](../../raw/pages_0353-0384/images/page_381_image_10.jpg)

<details>
<summary>text_image</summary>

1 Ω
+
us
-
1 F
1 Ω
-
1 F
+
u2
-
</details>

题 14-33 图

![](../../raw/pages_0353-0384/images/page_381_image_12.jpg)

<details>
<summary>text_image</summary>

i_S
R
L
C
+
u_2
-
</details>

题 14-34 图

14-35 题 14-35 图所示电路, 试求:

![](../../raw/pages_0353-0384/images/page_381_image_15.jpg)

<details>
<summary>text_image</summary>

1 F
+ 1 Ω 1 Ω
u₁ + u₂ 1 F + 2u₂ u₃
- - -
- -
</details>

题 14-35 图

---

习题

359

(1) 网络函数  $H(s)=\frac{U_{3}(s)}{U_{1}(s)}$ ，并绘出幅频特性示意图。
(2) 冲激响应  $h(t)$ 。

14-36 求题 14-36 图所示电路的电压转移函数 $H(s) = \frac{U_{\mathrm{o}}(s)}{U_{\mathrm{i}}(s)}$，设运放是理想的。

![](../../raw/pages_0353-0384/images/page_382_image_7.jpg)

<details>
<summary>text_image</summary>

1
sC₁
R₁
R₂
- ∞
+
1
sC₂
Ui(s)
Uₒ(s)
-
</details>

题 14-36 图

14-37 题 14-37 图所示电路为一低通滤波器, 若已知冲激响应为

$$
h \left(t\right) = \left[ \sqrt {2} \mathrm{e} ^ {- \frac {\sqrt {2}}{2} t} \sin \left(\frac {1}{\sqrt {2}} t\right) \right] \varepsilon \left(t\right)
$$

求:(1)L、C值。

(2) 幅频响应  $\left|H(j\omega)\right|-\omega$  曲线。

14-38 电路如题 14-38 图所示, 已知激励  $u(t)=10\mathrm{e}^{-at}\left[\varepsilon(t)-\varepsilon(t-1)\right]\mathrm{V}$ , 试用卷积定理求电流  $i(t)$ 。

![](../../raw/pages_0353-0384/images/page_382_image_14.jpg)

<details>
<summary>text_image</summary>

L
+
u₁ C C R u₂
-
</details>

题14-37图

![](../../raw/pages_0353-0384/images/page_382_image_16.jpg)

<details>
<summary>text_image</summary>

2 Ω
u(t)
+
-
i(t)
1 H
</details>

题14-38图

\* 14-39 电路如题 14-39 图所示, 网络 N 为线性无源网络, 已知其网络函数 $H(s) = \frac{I(s)}{U(s)} = \frac{s}{s^2 + 2s + 2}$。

(1) 给出该网络的一种结构及合适的元件值。
(2) 判断该网络冲激响应的性质。

14-40 电路如题 14-40 图所示, 网络函数  $H(s)=\frac{U(s)}{I(s)}$ , 其零、极点分布如题 14-40 图 (b) 所示, 且  $H(0)=1$ ,

![](../../raw/pages_0353-0384/images/page_382_image_23.jpg)

<details>
<summary>text_image</summary>

I(s)
+
U(s)
N
-
</details>

题14-39图

---

360

第十四章 线性动态电路的复频域分析

求 R、L、C 的值。

![](../../raw/pages_0353-0384/images/page_383_image_4.jpg)

<details>
<summary>text_image</summary>

I(s)
+
U(s)
-
C
L
R
</details>

(a)

![](../../raw/pages_0353-0384/images/page_383_chart_6.jpg)

<details>
<summary>contour</summary>

| \(\sigma\) | \(j\omega\) |
| --- | --- |
| -2 | 0 |
| -1 | 1/2 |
| 0 | 0 |
| \(\sigma\) | 0 |
</details>

(b)

题14-40图

14-41 电路如题图 14-41 所示, 已知 $R_{1} = R_{2} = 1 \Omega, C = \frac{1}{2} \mathrm{~F}, L = 2 \mathrm{~H}, g = \frac{1}{2} \mathrm{~S}$。

(1) 求电压转移函数  $H(s)=\frac{U_{o}(s)}{U_{s}(s)}$  及其冲激响应。
(2) 定性绘出  $\left|H(j\omega)\right|-\omega$  及  $\arg[H(j\omega)]-\omega$  曲线。

![](../../raw/pages_0353-0384/images/page_383_image_13.jpg)

第十四章部分习题答案

![](../../raw/pages_0353-0384/images/page_383_image_15.jpg)

<details>
<summary>text_image</summary>

R₁
① L
②
+ uₛ C + u₁ - gu₁ R₂ + u₀ -
-
</details>

题 14-41 图
