Für jedes Vektorfeld v mit divv = 1 läßt sich das Volumen $V(B)$ durch ein Oberflächenintegral berechnen; etwa mit $\mathbf{v} = x\mathbf{e}_{1}$:

$$
V (B) = \iiint_ {B} d V = \iint_ {S} (x \mathbf {e} _ {1} \cdot \mathbf {n}) d O.
$$

Speziell ergibt sich für die obere Hälfte der Einheitskugel

$$
V (B) = \iint_ {x ^ {2} + y ^ {2} \leq 1} \frac {x ^ {2}}{\sqrt {1 - x ^ {2} - y ^ {2}}} d x d y = \pi \int_ {0} ^ {1} \frac {r ^ {3} d r}{\sqrt {1 - r ^ {2}}} = \frac {2}{3} \pi .
$$

Bemerkung. Ist div v = 0 in einem Bereich B, erfüllt B die Voraussetzungen des Divergenzsatzes und läßt sich die Oberfläche von B stetig auf einen Punkt in B zusammenziehen, ohne daß dabei B verlassen wird, dann gibt es ein Vektorfeld w, das sog. Vektorpotential von v, so daß rot w = v (→ Band 2).

## \* 5.5 Einige Anwendungen der Integralsätze.

① Die Kontinuitätsgleichung der Hydrodynamik.

Sei v das Geschwindigkeitsfeld einer strömenden Flüssigkeit der (auch zeitlich variablen) Massendichte  $\rho$ . Ferner sei B ein regulärer Testbereich (im Strömungsgebiet) mit der Oberfläche S.

![](images/page_512_image_10.jpg)

<details>
<summary>text_image</summary>

B
v
</details>

Abb. 259 - Strömung

Durch das Oberflächenelement $dO$ tritt pro Zeiteinheit das Flüssigkeitsvolumen $(\mathbf{v} \cdot \mathbf{n}) dO$ hindurch. Die gesamte durch $S$ aus $B$ herausströmende Masse beträgt demnach $\iint_{S} \rho \mathbf{v} \cdot \mathbf{n} dO$.

Wird in B keine Masse erzeugt oder vernichtet, so ist die zeitliche Änderung der Masse auch durch  $-\frac{d}{dt}\iiint_{B}\rho dV$  gegeben (mit dem Minuszeichen, da der Massenfluß aus B heraus betrachtet wird), d.h. es gilt (mit den nötigen Voraussetzungen für §1, Satz 1.1)

$$
\iint_ {S} (\rho \mathbf {v} \cdot \mathbf {n}) d O + \iiint_ {B} \frac {\partial \rho}{\partial t} d V = 0.
$$

Mit dem Divergenzsatz ergibt das

$$
\iint_ {B} \left[ \mathrm{div} (\rho \mathbf {v}) + \frac {\partial \rho}{\partial t} \right] d V = 0 .
$$

Da diese Gleichung für beliebige Testbereiche B gilt, folgt mit den Regularitätsvoraussetzungen für jeden Punkt x die Kontinuitätsgleichung

$$
\mathrm{div} (\rho \mathbf {v}) + \frac {\partial \rho}{\partial t} = 0 ,
$$

die in der Hydrodynamik eine wichtige Rolle spielt.

Für eine stationäre (zeitunabhängige) Strömung gilt insbesondere  $\rho_{t}=0$ , also  $\mathrm{div}(\rho\mathbf{v})=0$ . Ist die Flüssigkeit inkompressibel (d.h.  $\rho=const$ ), dann gilt  $\rho_{t}=0$ ,  $\mathrm{div}(\rho\mathbf{v})=\rho\mathrm{div}\mathbf{v}$  und somit  $\mathrm{div}\mathbf{v}=0$ ; d.h. das Geschwindigkeitsfeld einer inkompressiblen Flüssigkeit ist quellenfrei.

② Die Wärmeleitungsgleichung.

In einem homogenen, erwärmten Körper der konstanten Massendichte  $\rho$  und konstanter spezifischer Wärme  $\sigma$  herrsche zur Zeit t im Punkt  $(x,y,z)$  die Temperatur  $U = U(x,y,z,t)$ . Dann speichert ein Volumenelement dV die Wärmemenge  $dW = \sigma U \rho dV$  und die Gesamtwärme W in einem (regulären) Teilbereich B mit Oberfläche S beträgt

$$
W = \iiint_ {B} \sigma \rho U d V.
$$

Der mit fortschreitender Zeit stattfindende Wärmeaustausch  $\frac{dW}{dt}$  wird als Wärmefluß durch die Oberfläche S gedeutet und berechnet sich nach einem Gesetz von FOURIER aus

$$
\frac {d W}{d t} = \iint_ {S} k (\operatorname{grad} U \cdot \mathbf {n}) d O
$$

mit einer Konstanten $k$, der Wärmeleitfähigkeit des Materials. (Hierin ist grad $U$ nur bezüglich der Ortskoordinaten $x, y, z$ zu bilden.) Mit dem Divergenzsatz und Satz 1.1 aus §1 folgt nun

$$
\begin{array}{l} \iiint_ {B} \rho \sigma \frac {\partial U}{\partial t} d V = \frac {d W}{d t} = \iint_ {S} k (\operatorname{grad} U \cdot \mathbf {n}) d O \\ = \iiint_ {B} k (\operatorname{div} \operatorname{grad} U) d V \\ \end{array}
$$

für jedes Testvolumen B. Damit ergibt sich die Wärmeleitungsgleichung

$$
\frac {\partial U}{\partial t} = \frac {k}{\sigma \rho} \left(\frac {\partial^ {2} U}{\partial x ^ {2}} + \frac {\partial^ {2} U}{\partial y ^ {2}} + \frac {\partial^ {2} U}{\partial z ^ {2}}\right) = \frac {k}{\sigma \rho} \Delta U.
$$

③ Die MAXWELL-Gleichungen.

In einer zu ① und ② analogen Weise kann man aus den experimentell entdeckten Grundgesetzen der Elektrizitätslehre die nach J.C. MAXWELL (1831–1879) benannten Hauptgleichungen des elektromagnetischen Feldes herleiten. (Heute werden diese Gleichungen meist an den Beginn der Elektrodynamik gestellt und daraus alle anderen Gesetze abgeleitet.) Das elektromagnetische Feld wird – in der Regel – durch 5 vom Ort x und von der Zeit t abhängige Vektorfelder beschrieben,

die elektrische Feldstärke E, die magnetische Feldstärke H,

die elektrische Flußdichte (Verschiebungsdichte) D,

die magnetische Induktion B und die elektrische Stromdichte J.

In SI-Einheiten lautet das FARADAYSche Induktionsgesetz (für jeden geschlossenen Weg C)

$$
\oint_ {C} \mathbf {E} \cdot d \mathbf {x} = - \frac {\partial}{\partial t} \int_ {S} \mathbf {B} \cdot \mathbf {n} d O \tag {7}
$$

und die Formel von BIOT-SAVART-AMPERE in der von MAXWELL 1865 korrigierten Form

$$
\oint_ {C} \mathbf {H} \cdot d \mathbf {x} = \int_ {S} \mathbf {J} \cdot \mathbf {n} d O + \int_ {S} \frac {\partial}{\partial t} \mathbf {D} \cdot \mathbf {n} d O. \tag {8}
$$

Hierbei stellt S ein reguläres Flächenstück dar, das von C (im Sinne des Satzes von STOKES) berandet wird. Der zweite Summand der rechten Seite, der im Gesetz von Ampere für stationäre Felder fehlt, wird seit MAXWELL Verschiebungsstrom genannt.

![](images/page_514_image_7.jpg)

<details>
<summary>text_image</summary>

E
C
S
B
E
</details>

Abb. 260 - Faraday-Gesetz

![](images/page_514_image_9.jpg)

<details>
<summary>text_image</summary>

J
H
S
C
H
</details>

Abb. 261 - Ampere-Gesetz

Wendet man den Satz von STOKES auf die Kurvenintegrale in (7) und (8) an, so hat man für alle zulässigen Testbereiche S

$$
\begin{array}{l} \int_ {S} \mathrm{rot}   \mathbf {E} \cdot \mathbf {n} d O = - \frac {\partial}{\partial t} \int_ {S} \mathbf {B} \cdot \mathbf {n} d O , \\ \int_ {S} \mathrm{rot} \mathbf {H} \cdot \mathbf {n} d O = \int_ {S} (\mathbf {J} + \frac {\partial}{\partial t} \mathbf {D}) \cdot \mathbf {n} d O. \\ \end{array}
$$

Mit den nötigen Voraussetzungen für Satz 1.1 von §1 kann $\frac{\partial}{\partial t}$ unter das Integral gezogen werden, und es folgen für jeden Punkt

$$
\mathrm{rot} \mathbf {E} + \frac {\partial}{\partial t} \mathbf {B} = \mathbf {0}; \quad \mathrm{rot} \mathbf {H} = \mathbf {J} + \frac {\partial}{\partial t} \mathbf {D}. \tag {9}
$$

Da div rot v = 0 für alle  $C^{2}$ -Vektorfelder v gilt, folgt hieraus

$$
\frac {\partial}{\partial t} \operatorname{div} \mathbf {B} = 0, \quad \operatorname{div} (\mathbf {J} + \frac {\partial}{\partial t} \mathbf {D}) = 0.
$$

Damit gelangt man mit den physikalischen Gesetzen für elektrische und magnetische Ladungen,

$$
\operatorname{div} \mathbf {D} = \rho \quad (\text {COULOMB - Gesetz,} \rho \text {Ladungsdichte}),
$$

$$
\operatorname{div} \mathbf {B} = 0 \quad (\text {keine freie magnetische Ladung}),
$$

zu den Kontinuitätsgleichungen :

$$
\mathrm{div}   J + \frac {\partial \rho}{\partial t} = 0 \quad ; \qquad \mathrm{div}   \mathbf {B} = 0 \tag {10}
$$

(9), (10) heißen MAXWELL-Gleichungen der Elektrodynamik.

In homogenen Medien gelten die Stoffgleichungen

$$
\mathbf {J} = \sigma \mathbf {E}; \quad \mathbf {D} = \epsilon \mathbf {E}; \quad \mathbf {B} = \mu \mathbf {H}
$$

(Elektrische Leitfähigkeit $\sigma$, Permitivität $\epsilon$, Permeabilität $\mu$); damit reduzieren sich (9) und (10) zu vier Bestimmungsgleichungen für $\mathbf{E}$ und $\mathbf{H}$:

$$
\mathrm{rot} \mathbf {E} + \mu \frac {\partial}{\partial t} \mathbf {H} = \mathbf {0}; \quad \mathrm{div} (\sigma \mathbf {E} + \epsilon \frac {\partial}{\partial t} \mathbf {E}) = 0;
$$

$$
\mathrm{rot} \mathbf {H} = \sigma \mathbf {E} + \epsilon \frac {\partial}{\partial t} \mathbf {E}; \quad \mathrm{div} \mathbf {H} = 0.
$$

Ist die Ladungsdichte $\rho = 0$, d.h. div $\mathbf{E} = 0$, so folgen die allgemeinen Wellengleichungen ($\rightarrow$ Kap. 7, §4, letztes Beispiel, in dem $\sigma = 0$)

$$
\mu \epsilon \mathbf {H} _ {t t} + \sigma \mu \mathbf {H} _ {t} = \Delta \mathbf {H} \quad \text {und} \quad \mu \epsilon \mathbf {E} _ {t t} + \sigma \mu \mathbf {E} _ {t} = \Delta \mathbf {E}.
$$

\* 5.6 Orthogonale krummlinige Koordinaten liegen vor, wenn für eine Koordinatentransformation (→ 5.3)

$$
\mathbf {x} (u, v, w) = x (u, v, w) \mathbf {e} _ {1} + y (u, v, w) \mathbf {e} _ {2} + z (u, v, w) \mathbf {e} _ {3}
$$

in jedem Punkt die Tangentialvektoren  $x_{u}$ ,  $x_{v}$  und  $x_{w}$  paarweise orthogonal sind ( $e_{1}, e_{2}, e_{3}$  bezeichnen die Basisvektoren des kartesischen Koordinatensystems). Mit den Maßstabsfaktoren

$$
h _ {1} := | \mathbf {x} _ {u} |, \quad h _ {2} := | \mathbf {x} _ {v} |, \quad h _ {3} := | \mathbf {x} _ {w} |
$$

erhält man mit

$$
\mathbf {x} _ {u} = h _ {1} \mathbf {e} _ {u}, \quad \mathbf {x} _ {v} = h _ {2} \mathbf {e} _ {v}, \quad \mathbf {x} _ {w} = h _ {3} \mathbf {e} _ {w} \tag {11}
$$

in jedem Punkt ein orthogonales Dreibein ( $e_{u}$ ,  $e_{v}$ ,  $e_{w}$ ); dieses ist rechtsorientiert, wenn man die Reihenfolge von u, v, w geeignet wählt:

$$
| \mathbf {e} _ {u} | = | \mathbf {e} _ {v} | = 1; \quad \mathbf {e} _ {u} \cdot \mathbf {e} _ {v} = 0; \quad \mathbf {e} _ {w} = \mathbf {e} _ {u} \times \mathbf {e} _ {v}. \tag {12}
$$

Beispiel 1. Zylinderkoordinaten.

$$
u = r, \quad v = \varphi , \quad w = z; \quad h _ {1} = 1, \quad h _ {2} = r, \quad h _ {3} = 1,
$$

und in bezug auf die kartesische Basis

$$
\mathbf {e} _ {r} = \left( \begin{array}{c} \cos \varphi \\ \sin \varphi \\ 0 \end{array} \right) ; \mathbf {e} _ {\varphi} = \left( \begin{array}{c} - \sin \varphi \\ \cos \varphi \\ 0 \end{array} \right) ; \mathbf {e} _ {z} = \left( \begin{array}{c} 0 \\ 0 \\ 1 \end{array} \right).
$$

Der Ortsvektor eines Punktes hat in seiner  $(\mathbf{e}_{r},\mathbf{e}_{\varphi},\mathbf{e}_{z})$ -Basis die Darstellung  $x=r\mathbf{e}_{r}+z\mathbf{e}_{z}\quad(\rightarrow Abb.~262)$ .

## Beispiel 2. Kugelkoordinaten.

$$
u = r, \quad v = \psi , \quad w = \varphi ; \quad h _ {1} = 1, \quad h _ {2} = r, \quad h _ {3} = r \sin \psi,
$$

und in bezug auf die kartesische Basis

$$
\mathbf {e} _ {r} = \left( \begin{array}{c} \cos \varphi \sin \psi \\ \sin \varphi \sin \psi \\ \cos \psi \end{array} \right) ; \mathbf {e} _ {\psi} = \left( \begin{array}{c} \cos \varphi \cos \psi \\ \sin \varphi \cos \psi \\ - \sin \psi \end{array} \right) ; \mathbf {e} _ {\varphi} = \left( \begin{array}{c} - \sin \varphi \\ \cos \varphi \\ 0 \end{array} \right).
$$

Der Ortsvektor hat die Darstellung  $x = r e_{r}$  ( $\rightarrow$  Abb. 263).

![](images/page_516_image_7.jpg)

<details>
<summary>text_image</summary>

z
e_z
r
e_φ
x
z
e_r
φ
x
y
</details>

Abb. 262 - Zylinderkoordinaten

![](images/page_516_image_9.jpg)

<details>
<summary>text_image</summary>

z
ψ
e_r
e_ψ
x
φ
e_φ
y
x
</details>

Abb. 263 - Kugelkoordinaten

Wegen (11) und (12) ist

$$
\frac {\hat {c} (x , y , z)}{\hat {c} (u , v , w)} = h _ {1} \cdot h _ {2} \cdot h _ {3},
$$

d.h. für das Volumenelement gilt

$$
d V = h _ {1} h _ {2} h _ {3} d u d v d w.
$$

Bezogen auf  $(\mathbf{e}_{u},\mathbf{e}_{r},\mathbf{e}_{w})$  hat das Differential dx die Komponenten  $h_{1}du$ ,  $h_{2}dv$ ,  $h_{3}dv$ ; denn mit der Kettenregel ist

$$
d \mathbf {x} = \mathbf {x} _ {u} d u + \mathbf {x} _ {v} d v + \mathbf {x} _ {w} d w = h _ {1} \mathbf {e} _ {u} d u + h _ {2} \mathbf {e} _ {v} d v + h _ {3} \mathbf {e} _ {w} d w . \tag {13}
$$

Damit ist das Bogenelement wegen (12)

$$
d s = \sqrt {d \mathbf {x} \cdot d \mathbf {x}} = \sqrt {h _ {1} ^ {2} d u ^ {2} + h _ {2} ^ {2} d v ^ {2} + h _ {3} ^ {2} d w ^ {2}}.
$$

Ein reguläres Flächenstück S hat im  $(u,v,w)$ -Koordinatensystem die Darstellung

$$
u = u (s, t), \quad v = v (s, t), \quad w = w (s, t)
$$

mit  $(s,t) \in D \subseteq \mathbb{R}^{2}$ . Mit der Kettenregel und (11) ergibt sich aus  $\mathbf{x} = \mathbf{x}(u(s,t), v(s,t), w(s,t))$ :

$$
\mathbf {x} _ {s} = \mathbf {x} _ {u} u _ {s} + \mathbf {x} _ {v} v _ {s} + \mathbf {x} _ {w} w _ {s} = h _ {1} u _ {s} \mathbf {e} _ {u} + h _ {2} v _ {s} \mathbf {e} _ {v} + h _ {3} w _ {s} \mathbf {e} _ {w},
$$

$$
\mathbf {x} _ {t} = h _ {1} u _ {t} \mathbf {e} _ {u} + h _ {2} v _ {t} \mathbf {e} _ {v} + h _ {3} w _ {t} \mathbf {e} _ {w}.
$$

Man hat damit als vektorielles Oberflächenelement auf S

$$
\mathbf {x} _ {s} \times \mathbf {x} _ {t} d s d t = \left(h _ {2} h _ {3} \frac {\partial (v , w)}{\partial (s , t)} \mathbf {e} _ {u} + h _ {3} h _ {1} \frac {\partial (w , u)}{\partial (s , t)} \mathbf {e} _ {v} + h _ {1} h _ {2} \frac {\partial (u , v)}{\partial (s , t)} \mathbf {e} _ {w}\right) d s d t
$$

und als skalares Oberflächenelement auf S

$$
d O = \sqrt {\left(h _ {2} h _ {3} \frac {\partial (v , w)}{\partial (s , t)}\right) ^ {2} + \left(h _ {3} h _ {1} \frac {\partial (w , u)}{\partial (s , t)}\right) ^ {2} + \left(h _ {1} h _ {2} \frac {\partial (u , v)}{\partial (s , t)}\right) ^ {2}} d s d t.
$$

Für die Koordinatenflächen u = const, v = const bzw. w = const erhält man als Oberflächenelemente

$$
\begin{array}{l} d \mathbf {A} _ {1} = d A _ {1} \mathbf {e} _ {u} = (h _ {2} h _ {3} d v d w) \mathbf {e} _ {u}, \\ d \mathbf {A} _ {2} = d A _ {2} \mathbf {e} _ {r} = (h _ {3} h _ {1} d w d u) \mathbf {e} _ {r}, \\ d \mathbf {A} _ {3} = d A _ {3} \mathbf {e} _ {w} = (h _ {1} h _ {2} d u d v) \mathbf {e} _ {w}. \\ \end{array}
$$

Für eine skalare Funktion  $f = F(u, v, w)$  und ein Vektorfeld

$$
\mathbf {v} = V _ {1} (u, v, w) \mathbf {e} _ {u} + V _ {2} (u, v, w) \mathbf {e} _ {v} + V _ {3} (u, v, w) \mathbf {e} _ {w}
$$

gelten die Formeln:

$$
\begin{array}{l} \text {grad} f = \frac {1}{h _ {1}} \frac {\partial F}{\partial u} \mathbf {e} _ {u} + \frac {1}{h _ {2}} \frac {\partial F}{\partial v} \mathbf {e} _ {v} + \frac {1}{h _ {3}} \frac {\partial F}{\partial w} \mathbf {e} _ {w}, \\ \quad \operatorname{div} \mathbf {v} = \frac {1}{h _ {1} h _ {2} h _ {3}} \left[ \frac {\partial}{\partial u} (h _ {2} h _ {3} V _ {1}) + \frac {\partial}{\partial v} (h _ {3} h _ {1} V _ {2}) + \frac {\partial}{\partial w} (h _ {1} h _ {2} V _ {3}) \right], \\ \quad \operatorname{rot} \mathbf {v} = \frac {1}{h _ {2} h _ {3}} \left(\frac {\partial (h _ {3} V _ {3})}{\partial v} - \frac {\partial (h _ {2} V _ {2})}{\partial w}\right) \mathbf {e} _ {u} + \frac {1}{h _ {3} h _ {1}} \left(\frac {\partial (h _ {1} V _ {1})}{\partial w} - \frac {\partial (h _ {3} V _ {3})}{\partial u}\right) \mathbf {e} _ {v} \\ \quad \quad + \frac {1}{h _ {1} h _ {2}} \left(\frac {\partial (h _ {2} V _ {2})}{\partial u} - \frac {\partial (h _ {1} V _ {1})}{\partial v}\right) \mathbf {e} _ {w}, \\ \quad \Delta f = \frac {1}{h _ {1} h _ {2} h _ {3}} \left[ \frac {\partial}{\partial u} \left(\frac {h _ {2} h _ {3}}{h _ {1}} \frac {\partial F}{\partial u}\right) + \frac {\partial}{\partial v} \left(\frac {h _ {1} h _ {3}}{h _ {2}} \frac {\partial F}{\partial v}\right) + \frac {\partial}{\partial w} \left(\frac {h _ {1} h _ {2}}{h _ {3}} \frac {\partial F}{\partial w}\right) \right]. \end{array} \tag {14}
$$

Beweis. Ergeben sich die Formeln für div v und rot v aus den Sätzen von GAUSS und STOKES, indem man die Integrale auf  $(u,v,w)$ -Koordinaten transformiert, so sieht man unmittelbar mit

$$
d f = \mathrm{grad}   f \cdot d \mathbf {x} = \frac {\partial F}{\partial u} d u + \frac {\partial F}{\partial v} d v + \frac {\partial F}{\partial w} d w
$$

und dx aus (13) und Komponentenvergleich die Darstellung für grad f. □

Beispiel. In kartesischen Koordinaten ist das Vektorfeld $\mathbf{v} = (y, -x, 1)^T$ und der Zylindermantel $S: x^2 + y^2 = 1$, $0 \leq z \leq 1$, gegeben. Als Komponenten von $\mathbf{v}$ in Kugelkoordinaten ergeben sich

$$
V _ {1} = \mathbf {v} \cdot \mathbf {e} _ {r} = \left( \begin{array}{c} r \sin \psi \sin \varphi \\ - r \sin \psi \cos \varphi \\ 1 \end{array} \right) \cdot \left( \begin{array}{c} \cos \varphi \sin \psi \\ \sin \varphi \sin \psi \\ \cos \psi \end{array} \right) = \cos \psi
$$

und analog  $V_{2} = v \cdot e_{\psi} = -\sin \psi$  und  $V_{3} = v \cdot e_{\varphi} = -r \sin \psi$ ;

$$
\mathbf {v} = \cos \psi   \mathbf {e} _ {r} - \sin \psi   \mathbf {e} _ {\psi} - r \sin \psi   \mathbf {e} _ {\varphi}.
$$

Aus den Formeln (14) folgt

$$
\mathrm{div} \mathbf {v} = \frac {1}{r ^ {2} \sin \psi} \left[ (r ^ {2} \sin \psi V _ {1}) _ {r} + (r \sin \psi V _ {2}) _ {\psi} + (r V _ {3}) _ {\varphi} \right] = 0.
$$

Um den Fluß von v durch S in Kugelkoordinaten zu berechnen, benötigt man die Darstellung von S in Kugelkoordinaten:

$x^{2} + y^{2} = r^{2}\sin^{2}\psi = 1 \text{ ergibt } r = \frac{1}{\sin\psi} \text{ und aus } 0 \leq z \leq 1 \text{ erhält man }$
$\frac{\pi}{4} \leq \psi \leq \frac{\pi}{2}, \text{ so daß } S = \left\{ (r, \psi, \varphi) = \left( \frac{1}{\sin s}, s, t \right); \frac{\pi}{4} \leq s \leq \frac{\pi}{2}, 0 \leq t < 2\pi \right\}.$

Damit ist in Kugelkoordinaten

$$
\begin{array}{l} \iint_ {S} \mathbf {v} \cdot d \mathbf {O} = \int_ {t = 0} ^ {2 \pi} \int_ {s = \pi / 4} ^ {\pi / 2} \left(V _ {1} h _ {2} h _ {3} - V _ {2} h _ {3} h _ {1} \frac {\partial r}{\partial s}\right) d s d t \\ = 2 \pi \int_ {\pi / 4} ^ {\pi / 2} \left(\cos s \cdot \frac {1}{\sin^ {2} s} \cdot \sin s - \sin s \cdot \frac {\cos s}{\sin^ {2} s}\right) d s = 0. \\ \end{array}
$$

## Aufgaben

1. Man berechne den geometrischen Schwerpunkt

a) des Tetraeders $\{(x,y,z)\in\mathbb{R}^{3};0\leq x,0\leq y,0\leq z,x+y+z\leq1\}$,
b) des Kegels $\{(x,y,z)\in\mathbb{R}^{3};0\leq x^{2}+y^{2}\leq a^{2}z^{2},0\leq z\leq h\},0\leq a,h.$

2. Man berechne $\iiint_{V} \sin zdV$ über

das Tetraeder mit den Seitenflächen

$$
x = 0, y = 0, z = 0, x + y + 2 z = 1.
$$

3. Aus der Kugel  $x^{2} + y^{2} + z^{2} \leq 4a^{2}$  wird das zylindrische Loch  $x^{2} + y^{2} \leq 2ax$  ausgebohrt. Wie groß ist das Restvolumen?

![](images/page_518_image_17.jpg)

<details>
<summary>text_image</summary>

1/2
z
1
1
y
x
</details>

4. Welcher Körper besitzt als axiales Trägheitsmoment zur z-Achse ( $\alpha > 0$ )

$$
I _ {z} = \int_ {0} ^ {h} \int_ {- z \tan \alpha} ^ {z \tan \alpha} \int_ {- \sqrt {z ^ {2} \tan^ {2} \alpha - y ^ {2}}} ^ {\sqrt {z ^ {2} \tan^ {2} \alpha - y ^ {2}}} (x ^ {2} + y ^ {2}) d x d y d z \quad ?
$$

Man berechne  $I_{z}$  mittels Zylinderkoordinaten.

5. Man berechne das Volumen des Körpers $K$, der durch die drei Flächen $x = y^2 + z^2$; $x = y$; $z = 0$ begrenzt wird.

6. Man berechne das axiale Trägheitsmoment $I_z = \iiint\limits_{V} (x^2 + y^2) dV$ für

a) die obere Halbkugel vom Radius $a$ und Mittelpunkt $O$ (Kugelkoordinaten!), b) den Torus aus 4.2d (Toruskoordinaten, $\rightarrow$ §4, Aufgabe 2).

7. Die Kugelschale $H = \left\{ \mathbf{y} \in \mathbb{R}^3 ; R_1 \leq |\mathbf{y}| \leq R_2 \right\}$, $0 < R_1 < R_2$, ist elektrisch homogen geladen. Für das Potential im Raumpunkt $\mathbf{x}$ gilt dann

$$
\Phi (\mathbf {x}) = \iiint_ {H} \frac {d y _ {1} d y _ {2} d y _ {3}}{| \mathbf {x} - \mathbf {y} |}.
$$

a) Mit $r = |\mathbf{x}|$, $\rho = |\mathbf{y}|$ und Übergang zu Kugelkoordinaten zeige man, daß $\Phi(\mathbf{x}) = V(r)$ mit

$$
V (r) = \int_ {0} ^ {\pi} \int_ {0} ^ {2 \pi} \int_ {R _ {1}} ^ {R _ {2}} \frac {\rho^ {2} \sin \psi}{\sqrt {\rho^ {2} + r ^ {2} - 2 r \rho \cos \psi}} d \rho d \varphi d \psi .
$$

b) Man berechne  $V(r)$  und skizziere  $V(r)$  für  $R_{1}=2$ ,  $R_{2}=4$ .

(Fallunterscheidung: $0 \leq r \leq R_{1}$, $R_{1} \leq r \leq R_{2}$, $R_{2} \leq r$.)

8. Gegeben ist der gerade Kreiskegel $S$ aus 4.2a und das Vektorfeld $\mathbf{v} = (xz, xy, -z)^T$. Man berechne und vergleiche die Ergebnisse (Divergenzsatz!):

a) $\iiint_{S} \operatorname{div} \mathbf{v} dV$,

b) $\iint_{\hat{c} S} \mathbf{v} \cdot d\mathbf{O}$

(dO weist ins Äußere von S).

9. Gilt der Satz von Gauß auch für ein Vektorfeld mit Singularität, wenn man an dieser Stelle das Volumenintegral als uneigentlich interpretiert?

Man berechne dazu explizit für die Kugel  $x^{2} + y^{2} + z^{2} \leq 1$

$\iint_{|\mathbf{x}|=1}\mathbf{v}\cdot\mathbf{n}dO\quad(\mathbf{n}\text{ äußere Normale})\quad\text{und}\quad\lim_{\epsilon\to0}\iiint_{\epsilon<|\mathbf{x}|<1}\text{div}\mathbf{v}dV\quad\text{für}$

a) $\mathbf{v} = \frac{\mathbf{x}}{|\mathbf{x}|}$,

b) $\mathbf{v} = -\frac{\mathbf{x}}{|\mathbf{x}|^3}$

(Gravitationsfeld).

## Knobelecke

Wieviele Kanten und Flächenstücke beranden den abgebildeten „Möbius-Ring“? Ist er zweiseitig, d.h. orientierbar?

![](images/page_519_image_22.jpg)

<details>
<summary>natural_image</summary>

Abstract black-and-white circular pattern with concentric rings and speckled texture (no text or symbols)
</details>

# Literaturverzeichnis

Die nachfolgende Liste enthält neben einer Auswahl an Lehrbüchern zur Ergänzung und Vertiefung des behandelten Stoffes auch Aufgabensammlungen und Handbücher.

- ANSORGE, R., H.-J. OBERLE: Mathematik für Ingenieure 1 – 2, Akademie Verlag, Berlin 1994
- AUMANN, G.: Höhere Mathematik I – III, B.I.-Wissenschaftsverlag, Mannheim 1970-71
- BAULE, B.: Die Mathematik des Naturforschers und Ingenieurs I, II, Harri Deutsch, Thun/Frankfurt 1979
- Bosch, K.: Mathematik-Taschenbuch, Oldenbourg, München 1989
- BRONSTEIN, I.N., K.A. SEMENDJAJEW: Taschenbuch der Mathematik, Harri Deutsch, Thun/Frankfurt 1994
- BURG, K., H. HAF, F. WILLE: Höhere Mathematik für Ingenieure I – IV, Teubner, Stuttgart 1992-94
- COURANT, R.: Vorlesungen über Differential- und Integralrechnung I, II, Springer 1971-72
- DALLMANN, H., K.-H. ELSTER: Einführung in die Höhere Mathematik 1 – 3, Gustav Fischer, Jena 1991
- DRESZER, J.: Mathematik-Handbuch für Technik und Naturwissenschaften, Harri Deutsch, Thun/Frankfurt 1975
- FELDMANN, C. ET AL.: Repetitorium der Ingenieurmathematik 1 - 3, Eigenverlag, Hannover 1989-91
- FICHTENHOLZ, G.M.: Differential- und Integralrechnung I – III, Deutscher Verlag der Wissenschaften, Berlin 1989
- v. FINKENSTEIN, K.: Grundkurs Mathematik für Ingenieure, Teubner, Stuttgart 1991
- FISCHER, G.: Lineare Algebra, Vieweg, Braunschweig 1986
- FORSTER, O.: Analysis 1 - 3, Vieweg, Braunschweig 1983-84
- GIERING, O., H. SEYBOLD: Konstruktive Ingenieurgeometrie, Hanser, München 1987
- GÜNTER, N.M., R.O. KUSMIN: Aufgabensammlung zur Höheren Mathematik I, II, Deutscher Verlag der Wissenschaften, Berlin 1980
- HÄMMERLIN, G., K.-H. HOFFMANN: Numerische Mathematik, Springer-Lehrbuch, Springer 1994
- HEINHOLD, J. ET AL.: Einführung in die Höhere Mathematik 1 – 4, Hanser, München 1976-80
- HEUSER, H.: Lehrbuch der Analysis 1, 2, Teubner, Stuttgart 1993
- JÄNICH, K.: Lineare Algebra, Springer-Lehrbuch, Springer 1993
- JEFFREY, A.: Mathematik für Naturwissenschaftler und Ingenieure 1, 2, Verlag Chemie, Weinheim 1978-80
- Joos, G., E.W. RICHTER: Höhere Mathematik für den Praktiker, Harri Deutsch, Thun/Frankfurt 1994
- KIRCHGÄSSNER, K., K. RITTER, P. WERNER: Höhere Mathematik I – III, Skriptum, Eigenverlag, Stuttgart 1980-94.
- KOECHER, M.: Lineare Algebra und analytische Geometrie, Grundwissen Mathematik 2, Springer 1992
- KÖNIGSBERGER, K.: Analysis 1, 2, Springer Lehrbuch, Springer 1992-93
- KREYSZIG, E.: Advanced Engineering Mathematics, J. Wiley, New York 1993
- MARTENSEN, E.: Analysis I - V, B.I.-Wissenschaftsverlag, Mannheim 1972-92
- NEUNZERT, H. (HRSG.): Analysis 1, 2,
  Mathematik für Physiker und Ingenieure, Springer-Lehrbuch, Springer 1993
- NIEDERDRENK, K., H. YSERENTANT: Funktionen einer Veränderlichen, Rechnerorientierte Ingenieurmathematik, Vieweg, Braunschweig 1987
- SAUER, R.: Ingenieurmathematik 1, 2, Springer 1968-69
- PRESS, W.H. ET AL.: Numerical Recipes in Pascal, Cambridge University Press 1989
- STOER, J.: Einführung in die Numerische Mathematik I, Springer-Lehrbuch, Springer 1994
- STOER, J., R. BULIRSCH: Einführung in die Numerische Mathematik II, Springer-Lehrbuch, Springer 1990
- STRUBECKER, K.: Einführung in die Höhere Mathematik I – IV, Oldenbourg, München 1966-90
- TÖRNIG, W., P. SPELLUCCI: Numerische Mathematik für Ingenieure und Physiker 1,2, Springer 1988-90
- TRINKAUS, H.L.: Probleme? Höhere Mathematik! Aufgabensammlung, Mathematik für Physiker und Ingenieure, Springer-Lehrbuch, Springer 1993
- WALTER, W.: Analysis I, II, Springer-Lehrbuch, Springer 1991-92
- ZURMÜHL, R., S. FALK: Matrizen, 1. Teil: Grundlagen, 2. Teil: Numerische Methoden, Springer 1992

## Anhang: Pascal-Programme

```txt
program Horner(input, output);
const maxgrad = 50;
var    N, I      : integer;
        A, C      : array[0..maxgrad] of real;
        B      : real;
begin
    write('Polynomgrad = '); read(N);
    for   I:=N downto O do
        begin write(I:2,'.Koeffizient = '); read(A[I]); end;
    write('b = '); read(B);
    C[N]:=A[N];
    for I:=N-1 downto O do C[I]:=C[I+1]*B+A[I];
    writeln('f(',b,') = ',C[O]);
end.
```

```txt
program HORNERvollstaendig(input,output);
const maxgrad = 50;
var    N,I,K    : integer;
      C,A       : array[O..maxgrad]   of real;
      B       : real;
begin
    write('Polynomgrad = '); read(N);
    for I:=N downto O do
      begin write(I:2,'.Koeffizient = '); read(A[I]); end;
    write('b = '); read(B);
    for K:=0 to N do  C[K]:=A[K];
    writeln('f(x)= ');
    for K:= 0 to N-1 do
      begin C[N]:=A[N];
        for I:= N-1 downto K do C[I]:=C[I+1]*B+C[I];
        writeln (C[K],'*(x-b)^',K:2,' +');
      end;
    writeln(A[N], '*(x-b)^', N:2);
end.
```

```pascal
program NEWTONinter(input,output);
const maxgrad = 50;
var I,K,N : integer;
    P,X,H,Z,U : real;
    F : array[l..maxgrad] of real;
begin
    write('Grad = '); read(N); write('Step = '); read(H);
    write('XO = '); read(Z);
    for I:=0 to N do begin write('F',I:2,' = '); read(F[I]); end;
    for I:=1 to N do for K:=N downto I do F[K]:=(F[K]-F[K-1])/I/H;
    write('p(x) for x = '); read(X); P:=F[N]; U:=X-Z;
    for I:=N-1 downto O do P:=P*(U-I*H)+F[I];
    writeln(P);
end.
```

```matlab
program Bisektion(input,output);
const EPS = 1.OE-06;
var    A,B,Fa,Fb : real;

function Fn(x:real):real; begin Fn:=x*(x*x*x*x+1)+1; end;

procedure Bisect(var A,B,Fa,Fb: real);
var C,Fc :   real;
begin
    C:=(A+B)*0.5; Fc:=Fn(C);
    if Fc*Fa<=0 then begin B:=C; Fb:=Fc; end
        else begin A:=C; Fa:=Fc; end;
end;

begin
    write('A = '); read(A); writeln; write('B = '); read(B); writeln;
    Fa:=Fn(A); Fb:=Fn(B);
    if Fa*Fb>0 then begin writeln('f(a)*f(b) positiv!'); halt; end;
    while abs(A-B)>=EPS do Bisect(A,B,Fa,Fb);
    writeln('Nullstelle im Intervall:[',A,'',B,']');
end.

program NEWTONverf(input,output);
const EPS = 1.OE-5;
var    Dx,X,Xa,Fl :   real;

function F(x:real):real; begin F:=((x+1)*x+2)*x+1; end;

begin
    repeat
        begin
            Dx:=EPS;
            if abs(X)>EPS then Dx:=X*EPS;
            Fl:=F(X); X:=X+Dx; Dx:=-F(X)*Dx/(F(X)-Fl);
            X:=X+Dx; Xa:=abs(X);
            if Xa<=1 then Xa:=1;
        end;
    until (abs(Dx)<(EPS*Xa)) or (abs(F(X))<EPS);
writeln(X);
end.

program KubischeSpline(input,output);
const max = 50;
var    M,N,I,K      :integer;
        X,Y,B,C,D     :array[0..max] of real;
        R,S,Q,Z,T     :real;
begin
    write('Punktezahl = '); read(N); writeln;
    N:=N-1;
    for I:=0 to N do
        begin
            write('X',I:2,' = '); read(X[I]); writeln;
            write('Y',I:2,' = '); read(Y[I]); writeln;
```

```pascal
end;
M:=N-1; S:=0;
for I:=0 to M do
    begin
        D[I]:=X[I+1]-X[I]; R:=(Y[I+1]-Y[I])/D[I]; C[I]:=R-S; S:=R;
    end;
S:=0; R:=0; C[0]:=0; C[N]:=0;
for I:=1 to M do
    begin
        C[I]:=C[I]+R*C[I-1]; B[I]:=(X[I-1]-X[I+1])*2-R*S;
        S:=D[I]; R:=S/B[I];
    end;
for I:=M downto l do C[I]:=(D[I]*C[I+1]-C[I])/B[I];
for I:=1 to M do
    begin
        S:=D[I]; R:=C[I+1]-C[I]; D[I]:=R/S; C[I]:=C[I]*3;
        B[I]:=(Y[I+1]-Y[I])/S-(C[I]+R)*S;
    end;
write('S(x) for x = ');read(Z); writeln;
if (X[N]-X[O])=0 then Q:=0
            else Q:=(X[N]-X[O])/abs(X[N]-X[O]);
K:=-1;
repeat I:=K; K:=K+1; until (Q*Z<Q*X[K]) or (K=N) ;
Q:=Z-X[I]; T:=((D[I]*Q+C[I])*Q+B[I])*Q+Y[I]; writeln(T);
end.

program ROMBERG(input,output);
const EPS = 1.OE-7;
var    I                      : array[0..7] of real;
    Ia,S,Fl,A,B,H,X,Q     : real;
    K,J,N                 : integer;

function F(x:real) : real; begin F:= ln(x)/x; end;

begin
    write('Grenze A = '); read(A); writeln;
    write('Grenze B = '); read(B); writeln;
    H:=B-A; N:=1; X:=1; Fl:=F(X); X:=B; I[0]:=H*(Fl+F(X))/2;
    for K:=1 to 7 do
        begin
            S:=0; H:=H/2; N:=2*N; Q:=1; J:=1;
            while J<N do
                begin X:=A+J*H; S:=S+F(X); J:=J+2; end;
            I[K]:=I[K-1]/2+S*H;
            for J:=K-1 downto O do
                begin Q:=4*Q; I[J]:=I[J+1]+(I[J+1]-I[J])/(Q-1); end;
            writeln(I[O]); Ia:=abs(I[O]);
            if Ia<1 then Ia:=1;
            if abs(I[1]-I[O])<EPS*Ia then begin writeln(I[O]); halt; end;
        end;
    writeln(I[O]);
end.
```

```txt
program VollstElliptInt(input,output);
const pi = 3.14159265359;
    EPS = 1.0E-9;
var Al,Bl,E,K,A,B,C,D: real;

begin
    write('K= '); read(K); writeln;
    if K<1 then
        begin
            A:=1; B:=sqrt(1-K*K);
            C:=K; D:=2; E:=C*C;
            repeat
                begin
                    Al:=(A+B)/2; Bl:=sqrt(A*B); C:=(A-B)/2;
                    E:=E+D*C*C; A:=Al; B:=Bl;D:=2*D;
                end;
            until C<EPS;
            writeln('K(k)= ',pi/2/A);
            writeln('E(k)= ',pi/2/A*(1-E/2));
        end
    else writeln('fail');
end.

program GAUSS(input,output);
const maxdim = 50;
    EPS = 1.0E-09;
type Typ1 = array[0..maxdim,0..maxdim] of real;
    Typ2 = array[0..maxdim] of real;
    Typ3 = array[0..maxdim] of integer;
var L,K,I,J,N,M,S,V,U,P : integer;
        A : Typ1;
        B,C : Typ2;
        F : Typ3;
        Y,X,D : real;
        E : char;

procedure Scalar1(U,V,I:integer; A:Typ1; B:Typ2; X:real; var Y:real);
begin
    Y:=X; while U<=V do begin Y:=Y+A[I,U]*B[U]; U:=U+1; end;
end;

procedure Scalar2(K,U,V: integer; A: Typ1; X: real; var Y: real);
begin
    Y:=X; while K>0 do begin K:=K-1; Y:=Y+A[U,K]*A[K,V]; end;
end;

begin
    write('DIMENSION N = '); read(N); writeln;
    M:=N-1;
    writeln('A ZEILENWEISE');
    for I:=1 to N do
        begin
            for J:=1 to N do
                begin write('A',I:2,J:2,' = '); read(A[I-1,J-1]); end;
```

```pascal
writeln;
    end;
for I:=0 to M do
    begin
        Y:=0;
        for S:=0 to M do Y:=A[I,S]*A[I,S]+Y;
        if Y=0 then writeln('A singulaer') else C[I]:=1/sqrt(Y);
    end;
D:=1;
for K:=0 to M do
    begin
        L:=K; X:=0;
        for I:=K to M do
            begin
                Scalar2(K,I,K,A,-A[I,K],Y);
                A[I,K]:=-Y; Y:=abs(Y*C[I]);
                if Y>X then begin X:=Y; L:=I; end;
            end;
        if L<>K then
            begin
                D:=-D;
                for J:=0 to M do
                    begin Y:=A[K,J]; A[K,J]:=A[L,J]; A[L,J]:=Y; end;
                    F[L]:=F[K];
                end;
        F[K]:=L; D:=D*A[K,K];
        if X<EPS then exit;
        if K<M then for J:=K+1 to M do
            begin Scalar2(K,K,J,A,-A[K,J],Y); A[K,J]:=-Y/A[K,K]; end;
        end;
if abs(D)<EPS then begin writeln('A singulaer'); halt; end;
writeln('D=',D);
repeat
    writeln('RECHTE SEITE');
    for I:=1 to N do
        begin write('B',I:2,' = '); read(B[I-1]); writeln; end;
    for I:=0 to M do
        begin
            P:=F[I];
            if I<>P then begin X:=B[I]; B[I]:=B[P]; B[P]:=X; end;
        end;
    for I:=0 to M do
        begin Scalar1(0,I-1,I,A,B,B[I],Y); B[I]:=-Y/A[I,I]; end;
    for I:=M downto O do
        begin Scalar1(I+1,M,I,A,B,B[I],Y); B[I]:=-Y; end;
    writeln('ERGEBNIS:');
    for I:=1 to N do writeln('X',I:2,'=',B[I-1]);
    writeln('Neue rechte Seite (j/n) '');read(E);
until E='n';
end.
```

```txt
program LEVERRIER(input, output);
const   max = 50;
type   Typl = array[0..max, 0..max] of real;
```

```csv
var    I,J,K,L,N  : integer;
        A,B           : Typ1;
        X,S           : real;

procedure Shift;
var   I  : integer;
begin
    S:=0;
    for I:=1 to N do  S:=S+B[I,I];
    S:=S/K; writeln('C',K:2,' = ',-S); K:=K+1;
    for I:=1 to N do  B[I,I]:=B[I,I]-S;
end;

begin
    write('DIMENSION N = '); read(N); writeln;
    writeln('A ZEILENWEISE');
    for I:=1 to N do
        begin
            for J:=1 to N do
                begin
                    write('A',I:2,J:2,' = '); read(A[I,J]); B[I,J]:=A[I,J];
                end;
        end;
    writeln('C',O:2,' = ',l:2); K:=1;
    while K<=N-2 do
        begin
            Shift;
            for J:=1 to N do
                begin
                    for I:=1 to N do B[I,O]:=B[I,J];
                    for I:=1 to N do
                        begin
                            X:=0;
                            for L:=1 to N do X:=X+A[I,L]*B[L,0];
                            B[I,J]:=X;
                        end;
                    end;
            end;
        Shift; S:=0;
        for L:=1 to N do S:=S+A[1,L]*B[L,l];
        writeln ('C',K:2,' = ',-S);
end.

program Jacobi(input,output);
const maxgrad = 50;
type  Typ1     = array[l..maxgrad,l..maxgrad] of real;
var    K,W,U,N,M,I,J,P,Q,V,X      : integer;
        A,B                      : Typ1;
        S,R,F,G,E,C,D          : real;

procedure Rot(C,D: real; U,V,W,X: integer; var A: Typ1);
var    F,G: real;
begin G:=A[U,V]; F:=A[W,X]; A[W,X]:=C*F-D*G; A[U,V]:=D*F+C*G; end;
```

```pascal
begin
    write('DIMENSION N = '); read(N); M:=N-1;
    for I:=0 to M do
        begin
            for J:=I to M do
                begin
                    if I=J then B[I,I]:=1
                    else begin B[I,J]:=0; B[J,I]:=0; end;
                    write('A',I+1:2,J+1:2,' = '); read(A[I,J]);
                end;
            end;
        repeat
        S:=0;
        for P:=0 to M-1 do
            begin
                for Q:=P+1 to M do
                    begin
                        R:=A[P,Q]; F:=A[P,P]; G:=A[Q,Q]; A[P,Q]:=0;
                        if (abs(R)+abs(F)<=abs(F)) and
                            (abs(R)+abs(G)<=abs(G)) then R:=0
                        else
                            begin
                                E:=(G-F)/2/R;
                                if E=0 then E:=1
                                else
                                    if E>0 then E:=l/(E+sqrt(1+E*E))
                                    else          E:=l/(E-sqrt(1+E*E));
                                C:=l/sqrt(1+E*E); D:=C*E;
                                A[P,P]:=F-E*R; A[Q,Q]:=G+E*R;
                                if P>0 then
                                    for I:=0 to P-1 do Rot(C,D,I,Q,I,P,A);
                                if Q<>P+1 then
                                    for K:=P+1 to Q-1 do Rot(C,D,K,Q,P,K,A);
                                if Q<>M then
                                    for J:=Q+1 to M do Rot(C,D,Q,J,P,J,A);
                                for J:=0 to M do Rot(C,D,Q,J,P,J,B);
                            end;
                            S:=S+abs(R);
                        end;
                    end;
until S=0;
for I:=0 to M do writeln('X',I+1:2,' = ',A[I,I]);
for I:=0 to M do
    begin
        writeln(I+1:2,'.Eigenvektor:');
        for J:=0 to M do writeln(B[I,J]);
    end;
end.
```

```txt
program BAIRSTOW(input,output);
label Start;
const maxgrad = 50;
EPS=1.OE-07;
```

```pascal
Steps=30;
var N,M,I,K : integer;
B,C : array[O..maxgrad] of real;
U,V,S,BK,BK1,BK2,CK,CK1,CK2,Det : real;

procedure Quadr_gleichg(var U,V: real);
var X,Y,W : real;
begin
X:=U/2; Y:=X*X+V; W:=sqrt(abs(Y));
if Y=0 then writeln('doppelte Wurzel:',X)
else
begin
write('2 Wurzeln:');
if Y>0 then
begin
if X>=0 then writeln(X+W,',',-V/(X+W))
else writeln(X-W,',',-V/(X-W));
end
else writeln(X,'+-i*',W);
end;
end;

begin
write('Polynomgrad = '); read(N); writeln;M:=N;
for I:=0 to N do
begin write('a',I:2,' = '); read(B[I]); writeln; end;
while M>2 do
Start: begin
write('Startwert UO = '); read(U); writeln;
write('Startwert VO = '); read(V); writeln;
S:=0;
repeat
BK:=0; BK1:=0; CK:=0; CK1:=0;
for K:=0 to M-1 do
begin
CK2:=CK1; CK1:=CK; BK2:=BK1; BK1:=BK;
BK:=B[K]+U*BK1+V*BK2;
C[K]:=BK;
CK:=BK+U*CK1+V*CK2;
end;
BK2:=BK1; BK1:=BK; BK:=B[M]+U*BK1+V*BK2; C[M]:=BK;
Det:=CK1*CK1-CK2*CK;
if Det=0 then
begin writeln('Neue Startwerte!’); goto Start; end;
U:=U+(BK*CK2-BK1*CK1)/Det; V:=V+(BK1*CK-BK*CK1)/Det;
S:=S+1;
if S=Steps then
begin writeln('Neue Startwerte!’); goto Start; end;
until abs(BK1)+abs(BK)<EPS;
Quadr_gleichg(U,V); M:=M-2;
for K:=0 to M do B[K]:=C[K];
end;
if M=1 then writeln('reelle Wurzel: ',-B[1]/B[0])
else begin U:=-B[1]/B[0]; V:=-B[2]/B[0]; Quadr_gleichg(U,V); end;
end.
```

```matlab
program NLSQ(input,output);
const M = 6;
    N = 3;
    P = 4;
type Typ1 = array[0..N] of real;
    Typ2 = array[0..M] of real;
    Typ3 = array[0..M,0..P] of real;
var X : Typ1;
    F,T,Y : Typ2;
    A : Typ3;
    I,L,J : integer;
    Lambda,FO,FK,D,B,C,Dl,Bl,Cl : real;
```

```txt
function Fn(D,B,C: real;T: Typ2;Y: Typ2;var F: Typ2): real;
var I : integer;
    Q : real;
begin
    Q:=0;
    for I:=1 to M do
        begin F[I]:=Y[I]-D-B*exp(C*T[I]); Q:=Q+F[I]*F[I]; end;
    Fn:=sqrt(Q);
end;

procedure Linfit(var X: Typ1; var A: Typ3);
var I,J,K          : integer;
    S,F,V          : real;
begin
    for I:=1 to N do
    begin
        S:=0;
        for J:=I to M do S:=S+A[J,I]*A[J,I];
        if S=0 then
            begin writeln('Matrix singulaer'); halt; end;
        V:=sqrt(S);
        if A[I,I]>0 then V:=-V;
        X[I]:=V; F:=S-V*A[I,I]; A[I,I]:=A[I,I]-V;
        for K:=I+1 to N+1 do
            begin
                S:=0;
                for J:=I to M do S:=S+A[J,I]*A[J,K];
                S:=S/F;
                for J:=I to M do A[J,K]:=A[J,K]-A[J,I]*S;
            end;
    end;
    X[N]:=A[N,N+1]/X[N];
    for I:=N-1 downto 1 do
        begin
            S:=A[I,N+1];
            for J:=I+1 to N do S:=S-A[I,J]*X[J];
            X[I]:=S/X[I];
        end;
end;
```

```pascal
begin
    for I:=l to M do
        begin write('t(i)= '); read(T[I]); write('y(i)= '); read(Y[I]);
        end;
    write('a,b,c ='); read(D,B,C);
    FK:=Fn(D,B,C,T,Y,F); FO:=FK; L:=0;
    repeat
        for I:=l to M do
            begin
                A[I,1]:=l; A[I,2]:=exp(C*T[I]);
                A[I,3]:=B*T[I]*exp(C*T[I]); A[I,4]:=F[I];
            end;
        Linfit(X,A); Lambda:=l;
        repeat
            Dl:=D+Lambda*X[1]; Bl:=B+Lambda*X[2];
            Cl:=C+Lambda*X[3]; FK:=Fn(Dl,Bl,Cl ,T,Y,F);
            if FK<FO then exit;
            Lambda:=Lambda/2;
        until Lambda<0.002;
        if Lambda<0.002 then exit;
        if FK<FO then begin D:=Dl; B:=Bl; C:=Cl; FO:=FK; end;
        L:=L+1;
    until L=30;
    writeln('Steps,a,b,c =',L,D,B,C);
end.
```

## Namen- und Sachverzeichnis

## Abbildung 2

Abbildungsmatrix 313, 324

abgeschlossene Menge 373

abgeschlossenes Intervall 4

abhängige Variable 258

Abkühlungszeit 151

Ableitung 112

Ableitungsregeln 115, 116, 361, 386, 387

Abschätzung, a posteriori 133

absolut konvergente Reihen 216

absolutes Maximum, Minimum 121

Absolutglieder eines Gleichungssystems
254

Abstand Gerade-Gerade 37

— im $\mathbb{R}^n$ 373

— Punkt-Ebene 39

— Punkt-Gerade 36

abstoßender Fixpunkt 100

Achse des Systems 50

Achsenabschnittsform 40

Additionstheorem 77, 78, 155

Adjunkte einer Matrix 308

Affensattel 396

affine Koordinaten 478, 493

affines Koordinatensystem 322

ähnliche Matrizen 325

algebraische Vielfachheit 327

allgemeine Lösung 258

alternierend 303

alternierende Reihen 214

— harmonische Reihe 99, 213

Ampère 423, 499

Amplitude 83

amplitudenmodulierte Schwingung 88

Angriffspunkt 47

Annuität 11

Anstieg der Tangente 113

— einer Funktion 385

anziehender Fixpunkt 100

Arbeit 443

Arbeitsintegral 443

Archimedische Spirale 198, 200

Arcuscosinus-Funktion 143

Arcuscotangens 145

Arcussinus-Funktion 143

Arcustangens 145, 168

Area cosinus hyperbolicus 156

Area sinus hyperbolicus 156, 178

Argument 2

arithmetisch-geometrisches Mittel 210

arithmetische Folge 89

Assoziativgesetz 19

Astroide 192, 201

Asymptote 106

ausgleichende Lösung 404

Ausgleichsrechnung 403

axiales Moment 462, 490

## Bairstow 73

Bairstow-Verfahren 384

barometrische Höhenformel 154

Basis 281

— für Kern A 294

Basisergänzung 283

Basiswechsel 420

Basiswinkel 321

Batterie-Ladestrom 179

bedingt konvergente Reihen 216

begleitendes Dreibein 362

Belegungsfunktion 370

Bernoulli-Ungleichung 6

Bernoulli-Zahlen 242

beschränkte Folgen 89

— Funktionen 89

— Mengen 4, 375

Bessel 431, 435

Bessel-Differentialgleichung 432

Bessel-Funktion 248, 431, 435

Betrag einer Zahl 5, 55

— eines Vektors 20, 315

Beugung am Spalt 84, 111

Bezier 486

Bezier-Bernstein 370

Biegekomponente eines Moments 366

Biegelinie 138

biegeweiche Membran 390, 403

bijektiv 2

bikubische Splines 487

Bild 2, 359

Bildraum 359

Binomialkoeffizient 8

Binomialreihe 232

binomische Formel 9

Binormalenvektor 362

Biot 190

Biot-Savart-Ampere 499

Bisektionsverfahren 109

Blindwiderstand 56

Blockmatrizen 291

Bogenelement 362, 501

Bogenlänge 361, 439

Bogenmaß 14

Boltzmann 188

Breitenkreise 470

CAD 43, 370, 486

Cantor 1

Cardanus 318

Cardioide 192, 199, 206

Cassini-Kurven 415

Cauchy 99, 237

Cauchy-Hauptwert 189

Cauchy-Kriterium 99, 213

Cauchy-Produkt 219

Cauchy-Schwarz-Ungleichung 315

charakteristisches Polynom 326

Cholesky 354

$C^k$ -Funktion 377, 418

Cosinus hyperbolicus 155

Cosinusfunktion 14, 76, 116

Cosinussatz 15, 43

Cotangens 78

Coulomb 422, 476, 499

Cramer-Regel 307

Dandelin-Kugel 44

De L'Hospital 127

De Moivre-Formeln 80

Definitionsbereich 2, 71, 359

Descartes 11, 201

Determinante 299, 302

Determinantenform einer Ebenengleichung 39

Dezibel 159

Diagonale 272

Diagonalelement 272

Diagonalisierung 332

— nichtorthogonale 348

— orthogonale 342

Diagonalmatrix 273

Differential 501

Differentialquotient 112

Differentiationsregeln 114, 115, 361, 378, 386, 387

differentieller Widerstand 159

Differenzengleichung, lineare 235

Differenzenquotient 112

differenzierbare Funktion 112

Dimension 284

Dimensionsanalyse 263

Dipolströmung 428

direktes Produkt 2

Dirichlet 225

disjunkt 2

Distributivgesetz 23, 28

divergente Folge 89

Divergenz 424, 496

Divergenzsatz 495

dividierte Differenzen 66

Dodekaeder 33, 358

Doppelintegral 456

Doppelseitenband-Modulation 88

Drehachse 319

Drehellipsoid-Koordinaten 493

Drehfläche 470

Drehgeschwindigkeitsvektor 357

Drehgruppe 333

Drehimpuls 358

Drehkörper 205, 494

Drehmatrix 319

Drehmatrix mit Euler-Winkel 322

Drehspiegelung 335, 337

Drehstreckung 81

Drehstromleitung 87

Drehung 16, 17, 81, 318, 421

Drehwinkel 319

Drei-Punkte-Gleichung der Ebene 38,
39

Dreiecksmatrix 272

Dreiecksungleichung 5, 20, 315

Dreifachintegral 489

Drillungswiderstand 467

Durchdringungskörper 461

Durchschnitt 1

Ebene, Parameterdarstellung 469

Ebenengleichungen 38

Effektivwert 178

$e$ -Funktion 98, 148

Eigenraum 327

Eigenschwingungen 329

Eigenvektor 326

Eigenwert einer Matrix 326

einfach zusammenhängend 448

Einflußzahlen 264

Einheitsmatrix 268

Einheitsvektor 20, 315

einparametrige Lösungsschar 262

Einstein 158, 245

Einzelkräfte 47

Eisblume 91

Elastizitätsmodul 382

elektrische Feldstärke 391, 498

— Flußdichte 498

— Stromdichte 498

Elektromagnetische Wellen 427

Element einer Menge 1

elementare Zeilenumformungen 256

— Spaltenumformungen 286

Elementarmatrix 287

Ellipse 12, 191, 200, 345

Ellipsoid 344

elliptische Funktion 177

— Koordinaten 478

elliptischer Punkt 396

elliptisches Integral 177, 246

endlich erzeugt 283

endlichdimensional 283

Energiesatz 445

Entier-Funktion 103

Entwicklungspunkt einer Potenzreihe
233

Epizykloide 192, 368

Ersatzwiderstand 56

erweiterte Koeffizientenmatrix 256

erzeugende Funktion 235

Erzeugendensystem 278

Euklidischer Algorithmus für Polynome
71

Euler 79, 98, 148

Euler-Zahl e 96, 97

Euler-Zahlen 244

Evolute 197

Exponentialfunktion 98, 148

— zur Basis a 153

exponentielle Sättigung 151

Extrapolation 208

Extremum, Extremstelle 121, 401

Extremwert-Test 125, 126, 239, 399, 401

Fachwerke 261, 264

Faktorisierung eines Polyboms 63

Fakultät 7

Faraday 499

Fechner 153

Federbein 369

Fehlerfunktion 176, 245

Fehlerrechnung 382

Feldlinie 421

Fermat-Prinzip 122

Fibonacci 236

Fixpunkt einer Funktion 131

— einer Rekursion 100

Fixpunktiteration 132

Fläche, implizit 372

— explizit 372

— Parameterdarstellung 467

— zweiseitig 482

— orientierbar 482

— regulär 468, 469

— Rand 469

Flächenelement 456

Flächeninhalt 454, 456, 476

flacher Punkt 396

Flächennormale 468

Fluß eines Vektorfeldes 444, 480

Folge, implizit 88

— explizit 88

— konvergent 89

— monoton 95

— beschränkt 90

Formel, binomische 9

— polynomische 11

Fourier 498

Fourier-Reihe 212

Fraktal 91

freie Parameter 258

— Variable 258, 260

freies Moment 49

Frenet 367

Frequenz 83

Fresnel 246

Fubini 430, 459, 490

Fundamentalsatz der Algebra 72

Funktion, Definition 2, 58, 359, 418

— stetige 106, 418

— gleichmäßig stetige 375

— differenzierbare 112

— total differenzierbare 379

— linear approximierbare 379

— partiell differenzierbare 376

—rationale 69

— ganz rationale 69

— implizite 397

— gerade 59

— ungerade 59

— periodische 82

— monotone 60

— beschränkte 89

— partielle 374

— vektorwertige 418

Funktionaldeterminante 477, 492

Funktionalmatrix 407, 419

Funktionswert 2

Gamma-Funktion 188, 434

Gasgesetz 154

Gauß 137, 210, 255, 403

Gauß-Integralsatz 495

Gauß-Jordan-Verfahren 292

Gauß'sche Elimination 256

Gauß-Normalgleichung 404

Gebiet 13, 445

Gebietsintegral 456

gebundene Vektoren 47

gebundener Nullvektor 47

geführte Bewegung 443

gegenphasige Schwingung 329

Geiger 153

geometrische Folge 89, 90

— Progression 11

— Reihe 91, 213, 230

— Vielfachheit 327

geometrischer Schwerpunkt 440, 463, 490

gerade Funktion 59

Geradengleichungen 34

Gesamtwiderstand 56

Geschwindigkeit 114

Gewichtsfaktoren 207

gleichmäßig konvergent 221

gleichmäßige Stetigkeit 108, 375

gleichphasige Schwingung 329

Gleichrichtwert 178

Gleichung, lineare 265

— quadratische 55

Gleichungssystem, lineares 245

— nichtlineares 382, 403

— überbestimmtes 403

Glieder einer Folge 88

— einer Reihe 212

globales Maximum, Minimum 121, 413

Gradient 377, 424

Gradientenfeld 445

Gradientenverfahren 391

Graph 371

— einer Funktion 12, 371

— Parameterdarstellung 191, 470

Grassmann-Identität 29

Gravitationskraft 167, 422

Green 464, 482

Grenzwert einer Folge 89

— einer Funktion 103, 374

Grenzwert-Regeln 93, 104

Grenzwertvertauschung 430

größter gemeinsamer Teiler 71

Grundintegrale 167

Guldin 206, 474, 494

Hagen 423

Hakenintegral 450

Halbwertszeit 151

Hängebrücke 169

harmonische Fuynktion 466

— Reihe 92, 213

— Schwingung 83

Hauptachsensystem 340

Hauptachsentransformation 341

Hauptnormalenvektor 362

Hauptsatz der Differential- und Integralrechnung 165

Hauptspannungen 357

Hauptspannungsrichtungen 357, 412

Hauptuntermatrizen 353

Hauptwert 79

Hermite 190

Heron 310

Hertz 417

Herzlinie 192, 199

Hesse 39

Hesse-Matrix 395

Hesse-Normalform 39

Hexaeder-Gruppe 337

Höhenlinien einer Landkarte 372

homogenes lineares Gleichungssystem
254

Homomorphismus 311, 313

Hooke 329, 357

— sches Gesetz 118, 124

Horner 62

Horner-Darstellung eines Polynoms 62

Horner-Schema 62

Householder 406

Hyperbel 12, 345

Hyperbelfunktionen 155

hyperbolischer Punkt 396

Hyperboloid, einschalig 344, 348, 351

— zweischalig 344

Hyperfläche 371

— zweiter Ordnung 343

Hypotrochoide 211

Hypozykloide 192

identische Abbildung 2, 312

Ikosaeder 33, 358

imaginäre Achse 53

Imaginärteil 53

Impedanz 56

implizite Funktion 397

indefinit 351

Infimum 5

inhomogenes lineares Gleichungssystem
254

injektiv 2

Inklusion 1

inkompressibel 498

innerer Punkt 373

inneres Produkt 315

Integrabilitätsbedingung 449

Integral, bestimmtes 162

— unbestimmtes 166

— elliptisches 177

— vollständig elliptisches 202, 210

— uneigentliches 185

— Kurven- 435

— Flächen- 474

— Gebiets- 456

— Volumen- 489

Integraldarstellung von Funktionen 168, 176, 430, 431

Integralfunktion 165

Integralmittel 165, 178, 457

Integralsatz von

— Gauss 495

— Green 464

— Stokes 842

Integralsinus 176, 246, 248

Integrationsbereich, ebener 455

— räumlicher 488

Integrationsgrenzen 162

Integrationskonstante 166, 451

Integrationsregeln 164, 169, 439, 457, 489

Interpolation 66

— mit Kreis 392

Interpolationsform eines Polynoms 66

Intervalle 4

Invarianten einer Matrix 330

Inverse 270, 292, 308

inverse Abbildung 314

— Matrix 270

invertierbare Abbildung 314

invertierbare Matrix 270, 304

Invertierbarkeits-Test 304

Jacobi 353

Jacobi-Determinante 477, 492

Jacobi-Matrix 407, 419

Kardioide 192, 199, 206

kartesische Basis 20

kartesisches Blatt 201

— Koordinatensystem 11, 17

Kegel 344

Kegelschnitte, Determinantenform 309

— Kepler-Form 201

— Normalformen 345

Kegelstumpf 471

Keilnut 26

Kennlinie 159

Kepler 169, 201

Kepler-Gleichung 415

Keplersche Faßregel 209

Kern einer Matrix 277

Kettenlinie 155, 169

Kettenmatrix 313

Kettenregel 116, 387

Keulen der Charakteristik einer Antenne 203

KFZ-Federbein 369

KFZ-Radlager 417

kinematisch unbestimmt 262

Kirchhoff 56

Kirchhoff-Regeln 261

Klothoide 369

Knicklinie 248

Knotenlinie 390

Koch-Eisblume 91

Koeffizienten einer Potenzreihe 226

— eines Gleichungssystems 254

Koeffizientenmatrix 254

Koeffizientenvergleich 61, 180, 234, 236

Kombination 10

Kombinatorik 10

Kommutativgesetz 19

kompakt 375

Komplement 1

komplexe Amplitude 83

— Schwingung 83

— Zahl 53, 79

— Zahlenebene 53

komplexer Widerstand 56

Komponente 21

Komponenten einer Matrix 250

Komponentenfunktionen 418

Komposition linearer Abbildungen 313, 134

— von Funktionen 60, 116

Kompositum 420

konjugierte komplexe Zahl 54

konservativ 445

konstante Funktion 58

kontinuierliche Verzinsung 96

Kontinuitätsgleichung 497, 500

konvergente Folgen 89

Konvergenzintervall 227

Konvergenzradius 226

konvex 126

konvexes Gebiet 394

Koordinate 21

Koordinaten, kartesische 17, 20

— affine 322

— Polar- 80, 197, 388

— Kugel- 388, 493

— Zylinder- 493

— elliptische 478

— hyperbolische 479

— krummlinige 492, 500

Koordinatenabbildung 313, 321

Koordinatendarstellung einer Ebene 39

— eines Vektors 21

Koordinatenfläche 492

Koordinatengleichung einer Geraden 35, 44

Koordinatenlinien 477

Koordinatensystem 11, 17, 477

Koordinatentransformation 321, 492

Koordinatenvektor 313, 321

Koordinatenwechsel 323

Kräftepaar 49

Kraftsystem 48

Kraftvektor 47

Kreis 191

Kreisfrequenz 83

Kreisfunktionen 75, 116

Kreiskegel 205

Kreissehnenviereck 25, 416

Kreistangente 25

Kreisteilung 82

Krümmung 126, 195, 363

Krümmungskreis 196

Krümmungsradius 196

Krümmungsvektor 363

Kugel im $\mathbb{R}^n$ 375

Kugel-Loxodrome 486

Kugelkoordinaten 25, 388, 493, 504

Kühlturm 485

Kummer 221

Kurve, explizit 12, 191

— implizit 12, 371

— Parameterdarstellung 190, 360

— entgegengesetzt durchlaufen 438, 442

— regulär 361

Kurvendiskussion 130

Kurvenintegral 435, 436, 442

Kurvenlänge 194

Kurvenstück 361

L'Hospital-Regel 127

Ladung 461, 476

Lagrange 237

Lagrange-Identität 29, 42

Lagrange-Multiplikator 410

Lagrange-Multiplikatorregel 410

Lambert 486

laminare Rohrströmung 423

Länge eines Kurvenstücks 194

— eines Vektors 315

Längenelement 204

längentreu 317

Laplace 388, 424

Laplace-Operator 388

leere Menge 1

Legendre-Polynome 75, 120, 178, 248

Leibniz 112, 119, 299

Leibniz-Regel 119, 432

Leibniz-Sektorformel 200

Leistungsanpassung 110

Lemniskate 202, 415

Leverrier 332

Lie 367

linear abhängig 279

—approximierbar 379,418

— unabhängig 31, 279

lineare Abbildung 311

— Approximation 113, 380, 418

— Ausgleichsprobleme 404

— Funktion 58

— Hülle 277

linearer Raum 275

— Teilraum 276

lineares Gleichungssystem 254

Linearfaktor eines Polynoms 63

Linearkombination 277

Linearschwinger 329

linksseitiger Grenzwert 103

Lissajous 86, 202

logarithmische Ableitung 120

— Spirale 367

Logarithmus zur Basis a 154

Logarithmusfunktion 152, 154, 168

logistisches Gesetz 160

lokales Extremum 121

Lorentz 351

Lösbarkeitsentscheidung 260

Lösbarkeitstest 260

LR-Zerlegung 293

M-Test 224

magnetische Feldstärke 498

— Induktion 498

— Wirbel 423

magnetischer Wirbel 423

Mantelfläche 205

Majorante 218

Masse 439, 461, 476, 490

Massenausgleich 2. Ordnung 264

Massenelement 439

Massenmittelpunkt 440, 462, 476, 490

Maßstabsfaktoren 500

Matrix, Typ 251

— Adjunkte 308

— ähnlich 325

— erweiterte 256

— quadratische 270

— Dreiecks- 272

— Diagonal- 273

— invertierbare 270

— symmetrische 270

— schiefsymmetrische 270

— Invarianten 330

— Rang 259, 288

— Signatur 350

— Spur 319

— Spaltenstufenform 280

— Zeilenstufenform 257, 280

— Spaltendarstellung 251

— Zeilendarstellung 251

Matrixgleichungen 293

Maximum unter Nebenbedingung 408

Maximum, Maximalstelle 108, 121, 375, 400, 401, 408

Maxwell 427, 498

Maxwell-Gleichungen 498

Mercator 485

Meridian 470

Methode der kleinsten Quadrate 403

metrischen Fundamentalgrößen 469

Minimum 108, 121, 375, 400, 401, 408

Minimum unter Nebenbedingung 408

Mittelpunkt einer Quadrik 346

Mittelwertsatz 123, 165, 439, 457

Möbius-Band 482, 487, 504

Modulationsfrequenz 88

Modulationsgrad 88

modulierte Amplitude 85

— Schwingung 85

Molwärme 129

Moment einer Kraft 29

— eines gebundenen Vektors 47

— eines Kraftsystems 48

Momente 439, 462, 476, 490

Momentengleichung einer Geraden 36,
45

monoton fallend 60, 123

— wachsend 60, 123

monotone Folgen 95

Monotoniekriterium 95

Multiplikationssatz für Determinanten
304

Nabla-Operator 427

Nachdifferenzieren 117

natürliche Basis 253, 282

natürlicher Parameter 366

natürliche Spline-Funktion 136

natürlicher Logarithmus 152

n-Blatt 202

negativ definit 351

Neil 197, 366

Netzwerk 254

Netzwerke mit Wechselstrom 56

Newton 66, 112, 422, 445

Newton-Verfahren 133

— mehrdimensional 382

nichtlineare Ausgleichsprobleme 404, 406

— Gleichungen 382

nichtorthogonale Diagonalisierung 348

nilpotente Matrix 338

Niveaufläche 372

Niveauhyperflächen 371

Niveaumengen 371

Normalbereich 458

Normale 193

Normalengleichung einer Ebene 39

— der Tangente 393

— der Tangentialebene 393

Normalenvektor 39

Normalform einer Quadrik 343, 344, 345

Normalkomponente 444, 480

Normalspannung 357, 412

Normalverteilung 479

normierter Vektor 315

n-te Wurzel 81, 141

Nullabbildung 312

Nullfolge 89

Nullmatrix 253

Nullmenge 454, 488

Nullphase 83

Nullstelle eines Polynoms 63

— $\ell$-fache 63

Nullstellen-Test 109

Nullvektor 253

numerische Integration 206

— Quadratur 206

Nutation 358

Nuttal 153

Obere Schranke 4

Oberflächenelement 473, 501, 502

Oberflächenintegral 474, 480

Obersummen 162

offene Menge 373

offenes Intervall 4

Ohmsches Gesetz 118

Oktaeder 33

Operator 311

orientierbare Fläche 482

orthogonale Abbildung 316

— Diagonalisierung 342

— Gruppe 333

— Matrix 316

— Vektoren 22, 316

— Zerlegung 25

orthogonales Netz 469

Orthogonalitätsrelationen 174, 178

orthonormale Vektoren 316

Orthonormierungsverfahren 320

Ortsvektor 20, 322

o-Symbol 379

Parabel 12, 345

parabolischer Punkt 396

Paraboloid, elliptisch 344

— hyperbolisch 156, 344

Parallelfach 31

Parallelogrammregel 19

Parallelverschiebung 336

Parameter 34, 191

Parameterdarstellung ebener Kurven 191

— eines Kurvenstücks 361

— eines Flächenstücks 468

Parameterintegrale 430, 433

Parameterlinien 468

Partialbruchzerlegung 179, 181

Partialbrüche 180

Partialsummen 212

partiell differenzierbar 376, 418

partielle Ableitung 376

— Integration 170

partikuläre Lösung 258

Pascal 11

Pascal-Dreieck 9

periodische Funktionen 82

Peripheriewinkel 25

Permutation 7

Phase 79, 83

Planck 158, 187

Poiseuille 423

Poisson 154

Pol 71

Pol des Polarkoordinatensystems 197

Polarachse 198

Polardarstellung ebener Kurven 197

— eines Kegelschnitts 201

— komplexer Zahlen 79

polare Momente 462

Polarkoordinaten 197, 388, 478

Polarwinkel 197

Polynom vom Grad n 61

Polynomdivision 69, 181

Polynomfaktorisierung 72, 73

polynomische Formel 11

positiv definit 351

Positivitätstest 352

Potential eines Dipols 247

Potential, eines Vektorfeldes 445

Potentialabfall 445

Potentialberechnung 450, 451

Potentialdifferenz 446

Potentialfeld 445

Potentialfunktion 445

Potenzen 6, 54, 142, 268

Potenzfunktion 142

Potenzreihe 212, 226

PQ-Normalform 289

prismatischer Stab 429

Produktdarstellung eines Polynoms 68

Produktregel 115, 361, 419

Projektion 312, 374

Pseudo-Inverse 299

Punkte 322

punktierte Ebene 448

Punktkoordinaten 322

Punktspiegelung 317

punktweise konvergent 221

QR-Zerlegung 321

quadratische Ergänzung 59, 347, 351

— Form 339

— Funktion 58

— Gleichungen 55

quadratisches Mittel 404

— Polynom 339

Quadrik 343

Quelldichte 424, 496

Quelle 496

quellfrei, quellenfrei 425, 496

Quotientenkriterium 218

Quotientenregel 115

Radialkomponente 202

radioaktiver Zerfall 151

Rakete 178

Rand einer Menge 373

Rang einer Matrix 259, 289

rationale Funktion 69

rationalen Nullstellen eines Polynoms 64

Raute 416

Realteil 53

Rechte-Hand-Regel 27

rechtsseitiger Grenzwert 103

Rechtssystem 17, 26

Reduktion zur Vektorschraube 50

reelle Achse 53

Regenbogen 148

Regression, Ausgleichsrechnung 403

reguläre Bereiche im $\mathbb{R}^3$ 488

— ebene Bereiche 455

reguläres Flächenstück 468

— Kurvenstück 361

Reihe, konvergente 212

— absolut konvergente 216

— bedingt konvergente 216

— alternierende 214

— alternierend harmonische 99

— geometrische 91, 231

— harmonische 92

— von Funktionen 221

— gleichmäßig konvergente 221

— Taylor- 239

Reihendarstellung 231, 240

rein imaginäre Zahlen 53

rein quadratische Form 339

reine Schwingung 83

Rekursion 6, 89, 91, 171, 177

relatives Extremum 121

Rennbahnkurve 415

Restglied, nach Cauchy 237

— nach Lagrange 237, 395

Restgliedabschätzung 208

Restriktion 3

Richtcharakteristik einer Antenne 203

Richtungsableitung 385

Richtungscosinus 23, 25

Riemann 161

Riemann-meßbar 454, 488

Riemann-Summe 161, 436, 455

Rodrigues 120

Rohrströmung 423

Romberg 208

Rotation 424, 484

Rotationsanteil der linearen Approximation 425

Rotationsenergie 358

Rotationskörper 204

Rotationstensor 429

Rückwärtssubstitution 257, 260

Sarrus 29, 301

Sattelpunkt 401

Savart 190

Schalldruck 379

Scheinkräfte 443

Scheinwiderstand 56

Scherung 314

schiefsymmetrische Matrix 270

Schmidt 320, 341

Schmiegebene 363

Schmiegquadrik 396

Schrankensatz 108

Schraubenfeder 369, 415

Schraubregel 27

Schraubung 336

Schubkurbelgetriebe 147

Schubspannung 357

Schwarz 378

schwarzer Körper 187

Schwebung 85

Schwebungsfrequenz 85

Schwerpunkt 440, 463, 490

Schwingung 83, 329

Schwingungsdauer 83, 248

Schwingungszahl 83

Sehnenviereck 25, 416

Sehnenwinkel 25

Seilkurve 169

Sektorfläche 199

2-Sekunden-Pendel 210

semidefinit 351

Senke 496

Signatur einer Matrix 350

Silizium-Gleichrichterdiode 159

Simpson-Regel 209

simultan diagonalisierbar 338

singuläre Stellen einer Kurve 366

Sinus hyperbolicus 155

Sinusfunktion 14, 76, 116

Sinuskegel 389

Sinusparaboloid 390

Sinussatz 15, 43

skalare Komponente 441

Skalarenfeld 370, 421

skalares Flächenelement 473, 502

Skalarprodukt 23, 315

Snellius 148

Spaltendarstellung des Produkts 267

— einer Matrix 251

Spaltenrang 289

Spaltenraum einer Matrix 286

Spaltenstufenform 280

Spaltenvektoren 250

Spaltenvektorraum 275

Spaltfunktion 107, 111

Spannungsabfall 443

Spannungsanpassung 110

Spannungsfeld 391

Spannungstensor 312, 330, 339, 429

Spannungsvektor 312, 429

Spat 314

Spatprodukt 30

spezielle Lösung 258

spezielle orthogonale Gruppe 333

Sphäre 412, 471

sphärische Trigonometrie 42

sphärisches Dreieck 42

Spiegelung 317

Spiegelungsgesetz 122

Spirale 367

Spline-Funktion 135, 487

Spur einer Matrix 319

— eines Kurvenstücks 361

St. Venant 467

Stabkräfte 262

Stabwerk 262

Stammfunktion 165, 445

stationäre Strömung 498

stationärer Punkt 122, 401, 402

statisch unbestimmt 262

statisches Moment 440

Stefan 188

Steigungsparameter 50

stetig partiell differenzierbar 376, 418

stetige Fortsetzung 107

— Funktion 106, 107, 374, 418

Stoffgleichungen 500

Stokes 482, 487, 499

Strahlung 158

strikte Ungleichung 3

stückweise reguläre Fläche 469

stückweise stetig 161

Stützpunkte 65

Summe einer unendlichen Reihe 212

Summendarstellung eines Polynoms 61

Superpositionsprinzip 48, 83

Supremum 4

surjektiv 2

Sylvester 350

symmetrische Matrix 270

Sägezahn 179

Tangens 78

Tangens hyperbolicus 155

Tangente 113

Tangentenanstieg 113

Tangenteneinheitsvektor 362

Tangentenvektor 362

Tangentialebene 380, 392, 468

Tangentialvektor 360

Tangentenwinkel 25

Taylor 237, 339

Taylor-Form eines Polynoms 240

Taylor-Formel 237, 395

Taylor-Polynom 237, 395

Taylor-Reihe 239

Teiler eines Polynoms 70

— größter gemeinsamer 71

Teilfolge 92

Teilmenge 1

Tetraeder 30, 33, 308, 311, 358

Torsion 364

Torsionskomponente eines Moments 366

Torsionsvektor 364

Torus 205, 471

total differenzierbar 379, 418

totale Ableitung 379

Trägerfrequenz 88

Trägheitsmoment 343, 440, 490

Trägheitstensor 343, 357

Transformation 311

Transformationsformel für Gebietsin-
tegrale 477

— für Volumenintegrale 492

transponierte Matrix 269

Transversalkomponente 202

— schwingung 403

Trapez-Regel 207

trignometrische Identitäten 77, 82

triviale Linearkombination 277

— Lösung 255

Tschebyschev-Polynome 144, 160

Typ einer Elementarmatrix 286

— einer Matrix 250

überbestimmtes Gleichungssystem 403

Überlagerung von Schwingungen 83, 84

Umgebung 4, 89, 373

Umkehrabbildung 2

Umkehrfunktion 139

Umordnung 219

Umparametrisierung auf Bogenlänge
366

unabhängige Variable 258

unbestimmtes Integral 166

uneigentliches Integral 185

uneigentlicher Grenzwert 90

Unendlich 4

unendliche Reihe 212

ungerade Funktion 59

Ungleichung 3

untere Schranke 4

Unterraum 276

Untersummen 162

Urbildraum 359

Van der Waals 69, 126, 415

Vandermonde 307

Variation 10

Vektor 18, 275

Vektorfeld 421

vektorielles Bogenelement 362, 442

— Flächenelement 480, 501

Vektorpotential 450, 497

Vektorprodukt 27

Vektorraum, Definition 275

Vektorraumhomomorphismus 311

Vektorschraube 50

Vektorwinder 48, 49

Vereinigung 1

Vergleichskriterium 94, 105, 186, 217

Verhulst 102

Verschiebungsdichte 498

Verschiebungsstrom 499

Verzerrungstensor 429

Vielfachheit einer Nullstelle 63

— eines Eigenwerts 327

Vierpol 312

Vieta 74

Viviani-Fenster 368, 453, 486

vollständige Entwicklung der Determinante 302

vollständige Induktion 6

vollständiges elliptisches Integral 202,
210, 246, 368

Vollständigkeitsaxiom 5

Volumen 488, 490

— des n-Spats 314