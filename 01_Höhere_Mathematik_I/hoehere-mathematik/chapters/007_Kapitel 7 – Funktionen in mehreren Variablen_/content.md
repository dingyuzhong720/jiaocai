# Kapitel 7 – Funktionen in mehreren Variablen: Differentiation

原始 PDF 第 375–445 页。

# Kapitel 7

# Funktionen in mehreren Variablen

# Teil 1: Differentiation

In der mathematischen Behandlung von Naturvorgängen treten oft Funktionen auf, die von mehreren Variablen  $x_{1},\ldots,x_{n}$  abhängen (etwa von den Ortskoordinaten x,y,z, von der Zeit t, vom Druck  $p,\ldots$ ) und deren Wertebereich mehrdimensional ist. Zur Differentialrechnung mit diesen Funktionen benötigt man die gesamte in Kap. 6 entwickelte Lineare Algebra. Es ist daher vorteilhaft,

die $n$ Variablen zu einem variablen Spaltenvektor $\mathbf{x} = \begin{pmatrix} x_1 \\ \vdots \\ x_n \end{pmatrix} \in \mathbb{R}^n$ zusammenzufassen. Im folgenden untersuchen wir deshalb Funktionen $\mathbf{f}: D \to \mathbb{R}^m$, mit $D \subseteq \mathbb{R}^n$, die jedem Spaltenvektor $\mathbf{x} = (x_1, \ldots, x_n)^T \in D$ einen mit $\mathbf{f}(\mathbf{x})$ oder $\mathbf{f}(x_1, \ldots, x_n)$ bezeichneten Vektor in $\mathbb{R}^m$ zuordnen. Hierfür schreiben wir künftig

$$
\mathbf {f}: \mathbb {R} ^ {n} \supseteq D \to \mathbb {R} ^ {m},
$$

$$
\mathbf {x} = \left( \begin{array}{c} x _ {1} \\ \vdots \\ x _ {n} \end{array} \right) \mapsto \mathbf {f} (x _ {1}, \dots , x _ {n}) = \left( \begin{array}{c} f _ {1} (\mathbf {x}) \\ \vdots \\ f _ {m} (\mathbf {x}) \end{array} \right).
$$

$R^{n}$ heißt Urbildraum, D Definitionsbereich, $R^{m}$ Bildraum und das Bild der Funktion f ist $\mathbf{f}(D)=\{\mathbf{f}(\mathbf{x});\mathbf{x}\in D\}$. Funktionen in mehreren Variablen, insbesondere wenn der Bildraum mehrdimensional ist, werden häufig als Abbildungen oder Transformationen (aus dem $R^{n}$ in den $R^{m}$) bezeichnet.

Vereinbarung. Jede Funktion $\mathbf{f}:\mathbb{R}^{n}\supseteq D\to\mathbb{R}^{m}$, mit der Spaltenvektoren des $\mathbb{R}^{n}$ auf Spaltenvektoren des $\mathbb{R}^{m}$ abgebildet werden, ist zugleich eine Funktion, die jedem Punkt $X=(x_{1},\ldots,x_{n})$ mit zugehörigem Ortsvektor $\mathbf{x}=(x_{1},\ldots,x_{n})^{T}\in D$ den Vektor $\mathbf{f}(\mathbf{x})$ zuordnet. Wir schreiben dafür $\mathbf{f}(X):=\mathbf{f}(\mathbf{x})=\mathbf{f}(x_{1},\ldots,x_{n})$ bzw. $(x_{1},\ldots,x_{n})\mapsto\mathbf{f}(x_{1},\ldots,x_{n})$.

Statt „Punkt $X = (x_{1}, \ldots, x_{n})$ mit Ortsvektor $\mathbf{x} = \begin{pmatrix} x_{1} \\ \vdots \\ x_{n} \end{pmatrix} \in \mathbb{R}^{n}$

sagt man kurz „Punkt $\mathbf{x} \in \mathbb{R}^{n}$“. In diesem Sinne fassen wir $\mathbb{R}^{n}$ als Punktraum und jede Teilmenge $D \subseteq \mathbb{R}^{n}$ als Punktmenge auf.

Zuerst behandeln wir die Sonderfälle

$$
n = 1, \text {d.h.} \quad \mathbf {f}: \mathbb {R} \supseteq I \to \mathbb {R} ^ {m} \quad (\text {Kurven im} \mathbb {R} ^ {m}, \to \S 1),
$$

$$
m = 1, \mathrm{d.h.} \quad f: \mathbb {R} ^ {n} \supseteq D \to \mathbb {R} \quad (\text {Skalarenfelder}, \rightarrow \S 2).
$$

Der allgemeine Fall ($m > 1$, $n > 1$) läßt sich hierauf zurückführen ($\rightarrow$ §4).

K. Meyberg et al., Höhere Mathematik

© Springer-Verlag Berlin Heidelberg 1998

---

360

7. Funktionen in mehreren Variablen. Teil 1: Differentiation

## §1. Kurven im  $R^{n}$

1.1 Parameterdarstellungen. In der Praxis hat man häufig das Problem, ein geometrisches Gebilde „Kurve“ oder „Weg“ analytisch, d.h. durch Funktionen, darzustellen. In der Ebene sind bereits einige Darstellungsarten bekannt:

Die evtl. nur abschnittsweise explizite Darstellung  $y = f(x)$  als Graph einer Funktion, die Polardarstellung  $r = r(\varphi)$  ( $\rightarrow$  Kap. 4, §5), die implizite Darstellung  $F(x, y) = 0$  (etwa bei den Kegelschnitten) und die Parameterdarstellung ( $\rightarrow$  Kap. 4, §5). Für die allgemeine Behandlung eignet sich am besten die Parameterdarstellung mit der Vorstellung, daß die Kurve die Bahn eines bewegten Punktes darstellt, der zur Zeit t den Ortsvektor  $\mathbf{x}(t)$  besitzt.

Wir betrachten daher vektorwertige, auf einem Intervall $I \subseteq \mathbb{R}$ erklärte Funktionen $\mathbf{x}: I \to \mathbb{R}^n$. Jede derartige Funktion besteht aus $n$ Komponentenfunktionen $x_i: I \to \mathbb{R} \quad (1 \leq i \leq n)$, d.h.

$$
\mathbf {x} (t) = \left( \begin{array}{c} x _ {1} (t) \\ x _ {2} (t) \\ \vdots \\ x _ {n} (t) \end{array} \right), \quad t \in I.
$$

Der für die Analysis grundlegende Grenzwertbegriff wird komponentenweise erklärt:

$$
\boxed {\lim _ {t \to t _ {0}} \left( \begin{array}{c} x _ {1} (t) \\ x _ {2} (t) \\ \vdots \\ x _ {n} (t) \end{array} \right) = \left( \begin{array}{c} c _ {1} \\ c _ {2} \\ \vdots \\ c _ {n} \end{array} \right) := \lim _ {t \to t _ {0}} x _ {i} (t) = c _ {i} \quad (1 \leq i \leq n).}
$$

Dementsprechend heißt $\mathbf{x}: I \to \mathbb{R}^n$ in $t_0 \in I$ (auf $I$) stetig, bzw. differenzierbar, wenn alle Komponentenfunktionen in $t_0 \in I$ (auf $I$) stetig, bzw. differenzierbar sind. Aus gleichem Grunde ist die Ableitung komponentenweise zu berechnen.

$$
\boxed {\dot {\mathbf {x}} (t) = \frac {d}{d t} \mathbf {x} (t) = \lim _ {h \rightarrow 0} \frac {1}{h} [ \mathbf {x} (t + h) - \mathbf {x} (t) ] = \left(\begin{array}{c}\dot {x} _ {1} (t)\\\dot {x} _ {2} (t)\\\vdots\\\dot {x} _ {n} (t)\end{array}\right)}
$$

mit $\dot{x}_i(t) = \frac{d}{dt} x_i(t)$. Man nennt $\dot{\mathbf{x}}(t)$ den Tangentialvektor von $\mathbf{x}$ an der Stelle $t \in I$ ($\rightarrow$ Kap. 4, §5 für $n = 2$). Stellt $t \to \mathbf{x}(t)$ das „Weg-Zeit-Gesetz“ eines bewegten Punktes dar, dann bestimmt $\dot{\mathbf{x}}(t)$ dessen Momentangeschwindigkeit, sie ist tangential zur Bahn. Im Fall $\dot{\mathbf{x}}(t_0) = 0$ ist der Punkt zur Zeit $t = t_0$ in Ruhe.

Für vektorwertige Funktionen $\mathbf{x},\mathbf{y}:I\to\mathbb{R}^{n}$ und $\alpha,\beta\in\mathbb{R}$ bestätigt man leicht

---

§1. Kurven im  $R^{n}$

361

die folgenden Ableitungsregeln :

(1)

a) $\frac{d}{dt} (\alpha \mathbf{x}(t) + \beta \mathbf{y}(t)) = \alpha \dot{\mathbf{x}} (t) + \beta \dot{\mathbf{y}} (t)$ (Linearität),
b) $\frac{d}{dt}[\mathbf{x}(t)\cdot\mathbf{y}(t)]=\dot{\mathbf{x}}(t)\cdot\mathbf{y}(t)+\mathbf{x}(t)\cdot\dot{\mathbf{y}}(t)$
$(Produktregel für das Skalarprodukt)$,
c) $\frac{d}{dt}[\mathbf{x}(t)\times\mathbf{y}(t)]=\dot{\mathbf{x}}(t)\times\mathbf{y}(t)+\mathbf{x}(t)\times\dot{\mathbf{y}}(t)$
$(Produktregel für das \times-Produkt, n=3 ) ,$

d) $\frac{d}{dt} [\alpha(t)\mathbf{x}(t)] = \dot{\alpha}(t)\mathbf{x}(t) + \alpha(t)\dot{\mathbf{x}}(t)$ (Produktregel für Multiplikation mit skalarer Funktion).

Insbesondere folgt wegen  $|\mathbf{x}(t)|^{2} = \mathbf{x}(t) \cdot \mathbf{x}(t)$  aus (1b):

$$
| \mathbf {x} (t) | = \text {const} \quad (t \in I) \implies \mathbf {x} (t) \cdot \dot {\mathbf {x}} (t) = 0 \quad \text {fur alle} t \in I. \tag {2}
$$

Die Parameterdarstellungen eignen sich, dem Begriff „Kurve“ eine Bedeutung zu geben, die auch im  $R^{n}$  ( $n \geq 1$ ) sinnvoll ist.

Definition. Es sei $G \subseteq \mathbb{R}^n$ und $[a, b] \subseteq \mathbb{R}$ ein abgeschlossenes Intervall. Wir nennen jede stetig differenzierbare Funktion $\mathbf{x} : [a, b] \to G$ ein Kurvenstück in $G$ mit Anfangspunkt $\mathbf{x}(a)$, Endpunkt $\mathbf{x}(b)$ und der Spur $\{\mathbf{x}(t) ; a \leq t \leq b\}$. $\dot{\mathbf{x}}(a)$, $\dot{\mathbf{x}}(b)$ sind als einseitige Ableitungen zu verstehen. Ein Kurvenstück $\mathbf{x}$ heißt regulär, wenn $\dot{\mathbf{x}}(t) \neq 0$ gilt für alle $t \in [a, b]$.

Bemerkungen. 1. Unter einer Kurve versteht man eine Kette von aneinanderhängenden Kurvenstücken (→ Kap. 8, §2). Für die Differentialrechnung beschränken wir uns auf Kurvenstücke.

![](../../raw/pages_0353-0384/images/page_376_image_14.jpg)

<details>
<summary>text_image</summary>

x(a₁)
x(a₂)=x(b₁)
x(a₃)=x(b₂)
x(b₃)
x₁
x₂
</details>

Abb. 158 - Kurve

2. Statt „Spur eines Kurvenstücks“ sagt man oft kurz „ein Kurvenstück“. D.h. sowohl die Punktmenge  $\{\mathbf{x}(t); t \in [a, b]\} \subseteq R^{n}$  als auch die Funktion  $x : [a, b] \to R^{n}$  werden als Kurvenstück bezeichnet. Aus dem Zusammenhang wird stets klar sein, was gemeint ist. Steht die anschauliche Deutung im Vordergrund, dann nennt man  $x : [a, b] \to R^{n}$  eine Parameterdarstellung des Kurvenstücks  $\{\mathbf{x}(t); a \leq t \leq b\}$ .

Die zum Parameterwert $t \in [a, b]$ eines regulären Kurvenstücks $\mathbf{x} : [a, b] \to \mathbb{R}^n$ bestimmte Zahl

(3)

$$
s (t) := \int_ {a} ^ {t} | \dot {\mathbf {x}} (t) | d t
$$

heißt Bogenlänge des Kurvenstücks über  $[a,t]$ . Für n = 2,3 ist das tatsächlich

---

362

7. Funktionen in mehreren Variablen. Teil 1: Differentiation

die Länge des durch x parametrisierten Bogens „über“ [a, t], wobei gegebenenfalls mehrfaches Durchlaufen einer Schleife berücksichtigt wird.  $L(\mathbf{x}) := s(b)$  ist die Länge des Kurvenstücks x. Nach Kap. 4, Satz 1.3 gilt

$$
\frac {d s}{d t} = \dot {s} (t) = | \dot {\mathbf {x}} (t) | . \tag {4}
$$

Man nennt (→ Kap. 4, 6.1)

$$
\begin{array}{l} \boxed {d s := | \dot {\mathbf {x}} (t) | d t \text {das (skalare) Bogenelement},} \\ d \mathbf {x} := \dot {\mathbf {x}} (t) d t \text {das vektorielle Bogenelement von} \mathbf {x}. \end{array} \tag {5}
$$

$(ds \text{ ist – in erster Näherung – die im Zeitintervall } [t, t + dt] \text{ zurückgelegte Weglänge, } dx \text{ ein zum Tangentialvektor } \dot{x}(t) \text{ paralleler Vektor der Länge } ds.)$

1.2 Das begleitende Dreibein, Krümmung, Torsion. Die Bewegung eines Massenpunktes längs einer durch $\mathbf{x} : [a, b] \to \mathbb{R}^3$ parametrisierten Spur und die Auswirkung von Kräften und Momenten in den einzelnen Kurvenpunkten $\mathbf{x}(t)$ wird am besten in einem der Geometrie der Spur angepaßten begleitenden kartesischen Koordinatensystem $(\mathbf{x}(t); \mathbf{T}, \mathbf{N}, \mathbf{B})$ beschrieben, in dem sich auch die Vektoren $\mathbf{T}, \mathbf{N}, \mathbf{B}$ der kartesischen Basis mit dem Parameter $t$ verändern. Wir setzen bei Bedarf für $\mathbf{x}$ Differenzierbarkeit von jeweils benötigter Ordnung voraus, ferner sei $\dot{\mathbf{x}}(t) \neq 0$ für alle $t \in [a, b]$, d.h. $\mathbf{x}$ regular.

Ⓐ Der Tangentenvektor $\mathbf{T}(t)$. Ist $\dot{\mathbf{x}}(t) \neq 0$ so nennt man den Einheitsvektor

$$
\boxed {\mathbf {T} (t) := \frac {1}{| \dot {\mathbf {x}} (t) |} \dot {\mathbf {x}} (t) \quad \text {Tangenteneinheitsvektor}} \tag {6}
$$

oder kurz den Tangentenvektor der Kurve an der Parameterstelle $t$. Die Gleichung (Parameterdarstellung) der Kurventangente in $\mathbf{x}(t_0)$ lautet

$$
\mathbf {x} (\lambda) = \mathbf {x} (t _ {0}) + \lambda \mathbf {T} (t _ {0}) \quad (\lambda \in \mathbb {R}).
$$

⑧ Der Hauptnormalenvektor $\mathbf{N}(t)$ und der Binormalenvektor $\mathbf{B}(t)$. Ist die Kurve $\mathbf{x} : [a, b] \to \mathbb{R}^3$ zweimal (komponentenweise) stetig differenzierbar, $t \in [a, b]$ eine Parameterstelle mit $\dot{\mathbf{x}}(t) \neq \mathbf{0}$ und $\dot{\mathbf{T}}(t) \neq \mathbf{0}$, so nennt man die nach (2) zu $\mathbf{T}(t)$ orthogonalen Einheitsvektoren

$$
\begin{array}{l l} \mathbf {N} (t) := \frac {1}{| \dot {\mathbf {T}} (t) |} \dot {\mathbf {T}} (t) & \text {Hauptnormalen(einheits)vektor}, \\ \mathbf {B} (t) := \mathbf {T} (t) \times \mathbf {N} (t) & \text {Binormalen(einheits)vektor} \end{array} \tag {7}
$$

und das Rechtssystem  $(\mathbf{T}(t),\mathbf{N}(t),\mathbf{B}(t))$  das begleitende Dreibein der Kurve an

---

§1. Kurven im  $R^{n}$

363

der Parameterstelle $t$. Ferner heißt die von $\mathbf{T}(t)$ und $\mathbf{N}(t)$ aufgespannte Ebene durch $\mathbf{x}(t)$,

$$
\mathbf {r} (\lambda , \mu) = \mathbf {x} (t) + \lambda \mathbf {T} (t) + \mu \mathbf {N} (t)
$$

$(\lambda,\mu\in\mathbb{R})$ , die Schmiegebene der Kurve an der Stelle t. Man gewinnt sie als Grenzlage der Ebene durch  $\mathbf{x}(t)$  und zwei weitere Kurvenpunkte.

![](../../raw/pages_0353-0384/images/page_378_image_5.jpg)

<details>
<summary>text_image</summary>

Schmiegebene
B(t)
x(b)
x(t)
T(t)
N(t)
x(a)
</details>

Abb. 159 - Begleitendes Dreibein

© Die Krümmung. Die Änderungsrate  $\frac{1}{\Delta s}\Delta T := \frac{1}{s(t_1) - s(t)}[\mathbf{T}(t_1) - \mathbf{T}(t)]$  des Tangentenvektors, bezogen auf die Bogenlänge, beschreibt anschaulich das mittlere Krümmungsverhalten der Kurve im Parameterintervall  $[t_1, t]$  (bzw.  $[t, t_1]$ ). Mit der L'Hospital-Regel erhält man

$$
\lim _ {t _ {1} \to t} \frac {1}{\Delta s} \Delta \mathbf {T} = \frac {1}{\dot {s} (t)} \dot {\mathbf {T}} (t) \quad \text {den Krümmungsvektor},
$$

seine Länge ist mit (4)

$$
\kappa (t) := \frac {1}{\dot {s} (t)} | \dot {\mathbf {T}} (t) | = \frac {| \dot {\mathbf {T}} (t) |}{| \dot {\mathbf {x}} (t) |} \quad \text {die Krümmung}
$$

der Kurve an der Stelle $t$.

Für die Darstellung von x und x im begleitenden Dreibein (T, N, B) ergibt sich aus (4), (6) und nach der Differentiation mit (1) und (8)

$$
\begin{array}{l} \dot {\mathbf {x}} (t) = \dot {s} (t) \mathbf {T} (t), \\ \ddot {\mathbf {x}} (t) = \ddot {s} (t) \mathbf {T} (t) + \dot {s} (t) ^ {2} \kappa (t) \mathbf {N} (t). \end{array} \tag {9}
$$

## Kinematische Deutung:

Stellt $\mathbf{x} : [a, b] \to \mathbb{R}^3$ mit $\dot{\mathbf{x}}(t) \neq \mathbf{0}$ die Bewegung eines Massenpunktes dar, so ist dessen Geschwindigkeitsvektor $\dot{\mathbf{x}}(t) = \dot{s}(t)\mathbf{T}(t)$ tangential zur Bahn (in Durchlaufrichtung) und dem Betrage nach gleich der Momentangeschwindigkeit $\dot{s}(t)$. Der Beschleunigungsvektor $\ddot{\mathbf{x}}(t)$ hat $\ddot{s}(t)\mathbf{T}(t)$ als Tangential- und $\dot{s}(t)^2\kappa(t)\mathbf{N}(t)$ als Normalkomponente. Daraus liest man ab, daß

![](../../raw/pages_0353-0384/images/page_378_image_16.jpg)

<details>
<summary>text_image</summary>

B
x(t)
ẋ(t)
T
ẍ(t)
N
ṡ > 0
s̈ > 0
</details>

Abb. 160 - Kinematik

$\frac{1}{\kappa(t)}$ als Radius eines Krümmungskreises in der Schmiegebene gedeutet werden kann, falls $\kappa(t) \neq 0$.

---

364

7. Funktionen in mehreren Variablen. Teil 1: Differentiation

Mit $\mathbf{T} \times \mathbf{T} = 0$, $\mathbf{T} \times \mathbf{N} = \mathbf{B}$ ergibt (9) $\dot{\mathbf{x}}(t) \times \ddot{\mathbf{x}}(t) = \dot{s}(t)^3\kappa(t)\mathbf{B}(t)$. Wegen $|\mathbf{B}(t)| = 1$ folgt $|\dot{\mathbf{x}}(t) \times \ddot{\mathbf{x}}(t)| = \dot{s}(t)^3\kappa(t)$. Also gelten

$$
\kappa (t) = \frac {| \dot {\mathbf {x}} (t) \times \ddot {\mathbf {x}} (t) |}{| \dot {\mathbf {x}} (t) | ^ {3}}, \tag {10}
$$

$$
\mathbf {B} (t) = \frac {1}{| \dot {\mathbf {x}} (t) \times \ddot {\mathbf {x}} (t) |} \dot {\mathbf {x}} (t) \times \ddot {\mathbf {x}} (t) \tag {11}
$$

(vorausgesetzt  $\dot{\mathbf{x}}(t) \times \ddot{\mathbf{x}}(t) \neq 0$ ).

Bemerkungen. 1. Formel (10) ergibt für eine ebene Kurve $t \to \begin{pmatrix} x(t) \\ y(t) \\ 0 \end{pmatrix}$ die Krümmung $\kappa = \frac{|\dot{x}\ddot{y} - \dot{y}\ddot{x}|}{(\dot{x}^2 + \dot{y}^2)^{3/2}}$; d.h. die hier definierte Krümmung stimmt mit der in Kap. 4, 5.4 eingeführten Krümmung nur bis aufs Vorzeichen überein. (Nur falls $\dot{x}\ddot{y} - \dot{y}\ddot{x} > 0$ ist, haben $\mathbf{n}$ ($\rightarrow$ Kap. 4, 5.2) und $\mathbf{N}$ dieselbe Richtung.) 2. Aufgrund der Formel (11) bestimmt man das begleitende Dreibein $(\mathbf{T}, \mathbf{N}, \mathbf{B})$ in der Reihenfolge $\mathbf{T} = \frac{1}{|\dot{\mathbf{x}}|}\dot{\mathbf{x}}$, $\mathbf{B} = \frac{1}{|\dot{\mathbf{x}} \times \ddot{\mathbf{x}}|}\dot{\mathbf{x}} \times \ddot{\mathbf{x}}$, $\mathbf{N} = \mathbf{B} \times \mathbf{T}$.

D Die Torsion. Das Herauswinden der Kurve aus der Schmiegebene wird durch die Änderungsrate des Binormalenvektors, bezogen auf die Bogenlänge, beschrieben. Man nennt

$$
\lim _ {t _ {1} \to t} \frac {1}{s (t _ {1}) - s (t)} [ \mathbf {B} (t _ {1}) - \mathbf {B} (t) ] = \frac {1}{\dot {s} (t)} \dot {\mathbf {B}} (t) \quad \text {den Torsionsvektor}
$$

der Kurve an der Stelle $t$.

Nach (2) ist $\dot{\mathbf{B}}$ orthogonal zu $\mathbf{B}$ und wegen $\dot{\mathbf{B}} = \frac{d}{dt} (\mathbf{T} \times \mathbf{N}) = \dot{\mathbf{T}} \times \mathbf{N} + \mathbf{T} \times \dot{\mathbf{N}} = \mathbf{T} \times \dot{\mathbf{N}}$ auch orthogonal zu $\mathbf{T}$, also parallel zu $\mathbf{N}$. D.h., es gibt eine skalare Funktion $\tau = \tau(t)$ - man nennt sie die Torsion der Kurve $\mathbf{x}$ - mit

$$
\frac {1}{\dot {s} (t)} \dot {\mathbf {B}} (t) = - \tau (t) \mathbf {N} (t). \tag {12}
$$

Es gilt

$$
\tau (t) = \frac {\det \left(\dot {\mathbf {x}} (t) , \ddot {\mathbf {x}} (t) , \dddot {\mathbf {x}} (t)\right)}{| \dot {\mathbf {x}} (t) \times \ddot {\mathbf {x}} (t) | ^ {2}}. \tag {13}
$$

Beweis. Aus $\mathbf{B} \cdot \mathbf{N} = 0$ folgt $\dot{\mathbf{B}} \cdot \mathbf{N} + \mathbf{B} \cdot \dot{\mathbf{N}} = 0$, deshalb führt (12) auf $\tau = -\frac{1}{\dot{s}} \dot{\mathbf{B}} \cdot \mathbf{N} = \frac{1}{\dot{s}} \mathbf{B} \cdot \dot{\mathbf{N}}$. Auf der rechten Seite setzen wir $\mathbf{B}$ aus (11) und $\dot{\mathbf{N}}$ aus der nochmals differenzierten 2. Gleichung (9) ein und erhalten nach leichter Rechnung mit (10) die Behauptung.

Wir fassen zusammen:

---

§1. Kurven im  $R^{n}$

365

Satz 1.1. Eine dreimal differenzierbare Kurve $\mathbf{x}:[a,b]\to\mathbb{R}^{3}$ besitzt an jeder Parameterstelle $t$ mit $\dot{\mathbf{x}}(t)\times\ddot{\mathbf{x}}(t)\neq\mathbf{0}$

$$
\begin{array}{l l} \text {den Tangentenvektor} & \mathbf {T} (t) = \frac {1}{| \dot {\mathbf {x}} (t) |} \dot {\mathbf {x}} (t), \\ \text {den Binormalenvektor} & \mathbf {B} (t) = \frac {1}{| \dot {\mathbf {x}} (t) \times \ddot {\mathbf {x}} (t) |} \dot {\mathbf {x}} (t) \times \ddot {\mathbf {x}} (t), \\ \text {den Hauptnormalenvektor} & \mathbf {N} (t) = \mathbf {B} (t) \times \mathbf {T} (t), \\ \text {die Krümmung} & \kappa (t) = \frac {| \dot {\mathbf {x}} (t) \times \ddot {\mathbf {x}} (t) |}{| \dot {\mathbf {x}} | ^ {3}}, \\ \text {die Torsion} & \tau (t) = \frac {\det (\dot {\mathbf {x}} (t) , \ddot {\mathbf {x}} (t) , \dddot {\mathbf {x}} (t))}{| \dot {\mathbf {x}} (t) \times \ddot {\mathbf {x}} (t) | ^ {2}}. \end{array}
$$

Beispiel. Die neutrale Faser einer Schraubenfeder wird dargestellt durch

$$
\mathbf {x} (t) = \left( \begin{array}{c} r \cos t \\ r \sin t \\ h t \end{array} \right)
$$

mit  $0 \leq t \leq 2\pi n$ , dabei ist r der Radius,  $2\pi h$  die Ganghöhe und n die Windungszahl.

![](../../raw/pages_0353-0384/images/page_380_image_7.jpg)

<details>
<summary>text_image</summary>

z
B
T
N
x(t)
r
F
x(0)
x
y
</details>

Abb. 161 - Schraublinie

Mit $\dot{\mathbf{x}}(t) = \begin{pmatrix} -r\sin t \\ r\cos t \\ h \end{pmatrix}, \ddot{\mathbf{x}}(t) = \begin{pmatrix} -r\cos t \\ -r\sin t \\ 0 \end{pmatrix}, \ddot{\mathbf{x}}(t) = \begin{pmatrix} r\sin t \\ -r\cos t \\ 0 \end{pmatrix}$ und der

Abkürzung  $R := |\dot{\mathbf{x}}(t)| = \sqrt{r^{2} + h^{2}}$  erhält man

$$
\mathbf {T} (t) = \frac {1}{R} \left( \begin{array}{c} - r \sin t \\ r \cos t \\ h \end{array} \right); \quad \mathbf {N} (t) = \left( \begin{array}{c} - \cos t \\ - \sin t \\ 0 \end{array} \right); \quad \mathbf {B} (t) = \frac {1}{R} \left( \begin{array}{c} h \sin t \\ - h \cos t \\ r \end{array} \right).
$$

$$
\text {Krümmung} \quad \kappa (t) = \frac {r}{r ^ {2} + h ^ {2}} \quad (\text {konstant}),
$$

$$
\text { Torsion } \quad \tau (t) = \frac {h}{r ^ {2} - h ^ {2}} \quad (\text { konstant }).
$$

Eine Belastung $\mathbf{F} = -Fe_{3}$ mit der Schraubachse als Wirkungslinie ($\rightarrow$ Abb. 161, Kap. 1, 7.1) erzeugt in jedem Punkt $\mathbf{x}(t)$ das Moment

$$
\mathbf {m} (t) = - \mathbf {x} (t) \times \mathbf {F} = r F \left( \begin{array}{c} \sin t \\ - \cos t \\ 0 \end{array} \right).
$$

Dieses besitzt in der begleitenden Basis (T, N, B) die Zerlegung

$$
\mathbf {m} = (\mathbf {m} \cdot \mathbf {T}) \mathbf {T} + (\mathbf {m} \cdot \mathbf {N}) \mathbf {N} + (\mathbf {m} \cdot \mathbf {B}) \mathbf {B} = - \frac {F r ^ {2}}{R} \mathbf {T} + \frac {F r h}{R} \mathbf {B}.
$$

---

366

7. Funktionen in mehreren Variablen. Teil 1: Differentiation

Man nennt  $m_{T} := -\frac{Fr^{2}}{R}T$  die Torsionskomponente und  $m_{B} := \frac{Frh}{R}B$  die Biegekomponente des Moments. ( $\rightarrow$  Aufg. 7) ☐

## Bemerkungen.

1. Diese Ergebnisse sind nur auf reguläre Kurvenstücke $\mathbf{x} : [a, b] \to \mathbb{R}^3$ anwendbar. Besitzt $\mathbf{x}$ singuläre Stellen $t_0 \in [a, b]$ mit $\dot{\mathbf{x}}(t_0) = 0$, so sind Grenzwertbetrachtungen $t \to t_0+$ und $t \to t_0-$ durchzuführen.

Beispiel.

$$
\mathbf {x} (t) = \binom{\frac {1}{3} t ^ {3}}{\frac {1}{2} t ^ {2}}, \quad t \in \mathbb {R},
$$

ist in t = 0 singular, da |x(0)| = 0.

$$
\mathbf {T} (t) = \frac {t}{| t | \sqrt {t ^ {2} + 1}} \binom{t}{1} \quad (\text {fur} t \neq 0)
$$

strebt bei  $t \rightarrow 0-$  gegen  $T_{1} = \begin{pmatrix} 0 \\ -1 \end{pmatrix}$ ,

![](../../raw/pages_0353-0384/images/page_381_image_10.jpg)

<details>
<summary>text_image</summary>

x₂
T₂
x₁
T₁
</details>

Abb. 162 - Neilsche Parabel

bei  $t \rightarrow 0+$  gegen  $T_{2} = \begin{pmatrix} 0 \\ 1 \end{pmatrix}$ . Obwohl wegen  $\dot{x}(0) = 0$  durch  $\dot{x}$  keine Tangentenrichtung festgelegt wird, besitzt die Kurve im Ursprung eine Tangente, nämlich die y-Achse.

2. Ist  $\kappa(t)=0$  für ein Teilintervall  $\alpha\leq t\leq\beta$ , dann stellt x über  $[\alpha,\beta]$  eine Gerade dar; N, B werden dort nicht benötigt.
3. Falls  $\tau(t)=0$  für  $\alpha\leq t\leq\beta$ , dann verläuft das entsprechende Kurvenstück ganz in der Schmiegebene.

\* 1.3 Ergänzung: Der natürliche Parameter und die Frenetschen Formeln.

Für die Bewegung auf einer regulären Kurve ist die eindeutige Ortsbestimmung  $\mathbf{x}(t)$  nicht nur durch Vorgabe der „Zeit“ t, sondern auch durch den bis zu diesem Zeitpunkt zurückgelegten Weg  $s = s(t)$  möglich. Denn wegen  $\dot{s}(t) = |\dot{\mathbf{x}}(t)| > 0$  ist  $s = s(t)$  als monotone Funktion (zumindest theoretisch) eindeutig nach t auflösbar,  $t = t(s)$ .

Man sagt, die Kurve

$$
\mathbf {y}: [ 0, L ] \to \mathbb {R} ^ {3}, \quad \mathbf {y} (s) := \mathbf {x} (t (s)),
$$

entsteht aus der regulären Kurve x durch Umparametrisierung auf Bogenlänge. Offenbar besitzen x und y dieselbe Spur. Über  $\mathbf{y}(s(t)) = \mathbf{x}(t)$  kommt man zur ursprünglichen Parameterdarstellung zurück. Die Kettenregel und (3) Kap. 3, §3 ergeben

$$
\frac {d}{d s} \mathbf {y} (s) = \frac {d}{d s} \mathbf {x} (t (s)) = \dot {\mathbf {x}} (t (s)) \frac {d}{d s} t (s) = \frac {1}{\dot {s} (t (s))} \dot {\mathbf {x}} (t (s)) = \mathbf {T}.
$$

Die Bogenlänge als Parameter (man spricht vom natürlichen Parameter) ist dadurch ausgezeichnet, daß der die Kurve begleitende Tangentialvektor $\frac{d}{ds}\mathbf{y}(s)$ konstant den Betrag 1 hat; dadurch ergeben sich besonders elegante Formeln:

---

§1. Kurven im  $R^{n}$

367

Satz 1.2. Formeln von FRENET (1816-1900). Für eine dreimal stetig differenzierbare, auf Bogenlänge parametrisierte Kurve $\mathbf{y} : [0, L] \to \mathbb{R}^3$, die überall eine Krümmung $\kappa(s) \neq 0$ besitzt, gelten folgende Ableitungsformeln:

$$
\begin{array}{l} \begin{array}{l} \frac {d \mathbf {T}}{d s} = + \kappa \mathbf {N} \\ \frac {d \mathbf {N}}{d s} = - \kappa \mathbf {T} + \tau \mathbf {B} \end{array} \tag {14} \\ \frac {d \mathbf {B}}{d s} = \quad - \tau \mathbf {N} \quad . \\ \end{array}
$$

Beweis. In diesem Fall ($\dot{s}=1$, $\ddot{s}=0$) lauten die Beziehungen (6), (9) und (12) $\mathbf{T}=\frac{dy}{ds}$, $\frac{d\mathbf{T}}{ds}=\frac{d^{2}\mathbf{y}}{ds^{2}}=\kappa\mathbf{N}$, $\frac{dB}{ds}=-\tau\mathbf{N}$. Nun braucht man nur noch $\mathbf{N}=\mathbf{B}\times\mathbf{T}$ nach $s$ abzuleiten und erhält die dritte Ableitungsformel.

Damit kann man den Satz von S. LIE (1842-1899) beweisen, daß eine auf Bogenlänge parametrisierte Kurve im wesentlichen durch $\kappa = \kappa(s)$ und $\tau = \tau(s)$ bestimmt ist. Durch das Differentialgleichungssystem (14) werden $\mathbf{T}(s)$, $\mathbf{N}(s)$, $\mathbf{B}(s)$ bei Vorgabe der Anfangslage $\mathbf{T}(0)$, $\mathbf{N}(0)$, $\mathbf{B}(0)$ und stetig differenzierbarer Funktionen $\kappa, \tau : [0, L] \to \mathbb{R}$ bis auf längentreue Abbildungen eindeutig bestimmt ($\rightarrow$ Band 2, Kap. 9, §8, Aufg. 19).

Beispiel. Die Raumkurve

$$
\mathbf {x} (t) = \frac {1}{2} e ^ {t} \left( \begin{array}{c} \cos t \\ \sin t \\ \sqrt {2} \end{array} \right), t \in \mathbb {R},
$$

liegt auf dem Kegel  $2x^{2} + 2y^{2} - z^{2} = 0$  und hat als Projektion in die  $(x, y)$ -Ebene eine logarithmische Spirale  $r = \frac{1}{2}e^{\varphi}$  ( $r, \varphi$  Polarkoordinaten).

Wegen $\dot{\mathbf{x}}(t) = \frac{1}{2} e^{t}\left( \begin{array}{c}\cos t - \sin t\\ \sin t + \cos t\\ \sqrt{2} \end{array} \right)$

![](../../raw/pages_0353-0384/images/page_382_image_10.jpg)

<details>
<summary>text_image</summary>

r=be^{aφ}
y
x
b
</details>

Abb. 163 - Logarithmische Spirale

ist $s(t) = \int_{-\infty}^{t} |\dot{\mathbf{x}}(\tau)| d\tau = e^t$, d.h. $t = \ln(s)$, $s > 0$. Mit der Bogenlänge als Parameter erhält man aus der Darstellung

$$
\mathbf {y} (s) = \frac {1}{2} s \left( \begin{array}{c} \cos \ln s \\ \sin \ln s \\ \sqrt {2} \end{array} \right), s > 0:
$$

$$
\mathbf {T} = \frac {d}{d s} \mathbf {y} (s) = \frac {1}{2} \left( \begin{array}{c} \cos \ln s - \sin \ln s \\ \sin \ln s + \cos \ln s \\ \sqrt {2} \end{array} \right), \quad \frac {d}{d s} \mathbf {T} = \frac {1}{2 s} \left( \begin{array}{c} - \sin \ln s - \cos \ln s \\ \cos \ln s - \sin \ln s \\ 0 \end{array} \right),
$$

---

368

7. Funktionen in mehreren Variablen. Teil 1: Differentiation

$$
\kappa (s) = | \frac {d \mathbf {T}}{d s} | = \frac {1}{2 s} \sqrt {2},   \mathbf {N} = \frac {1}{\sqrt {2}} \left( \begin{array}{c} - \sin \ln s - \cos \ln s \\ \cos \ln s - \sin \ln s \\ 0 \end{array} \right),
$$

$$
\tau (s) = \left| \frac {d}{d s} \mathbf {N} + \kappa \mathbf {T} \right| = \frac {1}{2 s} \sqrt {2}.
$$

## Aufgaben

1. Man berechne den Winkel, unter dem alle Tangenten der Kurve

$$
x (t) = \sqrt {2}, y (t) = t ^ {2} - \frac {1}{4} \ln t, z (t) = t ^ {2} + \frac {1}{4} \ln t \quad (1 \leq t \leq 2)
$$

auf die  $(x,y)$ -Ebene treffen, und berechne ihre Bogenlänge.

2. Gegeben ist die räumliche Spirale

$$
\mathbf {x} (t) = \left( \begin{array}{c} t \cos t \\ t \sin t \\ 2 t \end{array} \right), \quad t \geq 0.
$$

Man berechne das begleitende Dreibein (T,N,B) für x. Wie groß ist die Krümmung κ und die Torsion τ im Punkt 0? Welche Kurve ergibt sich in der Projektion auf die Ebene z = 0?

![](../../raw/pages_0353-0384/images/page_383_image_11.jpg)

<details>
<summary>text_image</summary>

B
N
x
T
x
y
z
</details>

3. Man zeige, daß alle Geraden durch den Ursprung die (ebene) logarithmische Spirale $r = e^{-\varphi}$ unter konstantem Winkel treffen, wie groß ist dieser?

4. Gegeben ist die Epizykloide

$$
\mathbf {w} (t) = \binom{\cos 3 t + 3 \sin t}{3 \cos t - \sin 3 t}, \quad 0 \leq t \leq 2 \pi .
$$

a) Man bestimme die singulären Punkte ($\dot{x} = \dot{y} = 0$) und in diesen Punkten die Richtungen der Tangenten über die möglichen Grenzwerte $\lim \dot{y}(t) / \dot{x}(t)$.
b) Man berechne die Bogenlänge der Kurve und in jedem Punkt die Krümmung.
c) In welchen Punkten wird $r = |\mathbf{w}(t)|$ maximal? Skizziere w samt Durchlaufsinn.

5. Die Raumkurve (Fenster der VIVIANI)

$$
\mathbf {x} (t) = \left( \begin{array}{c} \cos t \\ \sin t \\ 2 \sin \frac {t}{2} \end{array} \right), 0 \leq t \leq 4 \pi ,
$$

entsteht durch Verschneidung des Drehzylinders $x^{2} + y^{2} = 1$ mit der Kugel $(x + 1)^{2} + y^{2} + z^{2} = 4$. Man bestätige dies, berechne $(\mathbf{T}, \mathbf{N}, \mathbf{B})$ für $t = 0$ und $t = 2\pi$ und drücke die Bogenlänge der Kurve durch das vollständige elliptische Integral

$$
E (k) = \int_ {0} ^ {\frac {\pi}{2}} \sqrt {1 - k ^ {2} \sin^ {2} \varphi} d \varphi \quad \text {aus.}
$$

![](../../raw/pages_0353-0384/images/page_383_image_23.jpg)

<details>
<summary>text_image</summary>

z
x
o
y
</details>

---

§1. Kurven im  $R^{n}$

369

6. Im Straßenbau wird der Übergang von der Geraden in eine kreisförmige Kurve durch Klothoiden-Bögen modelliert, da sie folgende natürliche Parameterdarstellung besitzen:

$\kappa = c \cdot s$ , Krümmung wächst proportional mit Bogenlänge.

![](../../raw/pages_0385-0416/images/page_384_image_4.jpg)

<details>
<summary>text_image</summary>

y
φ
x
</details>

Man bestimme daraus den Tangentenwinkel $\varphi$ als Funktion $\varphi(s)$ der Bogenlänge und stelle damit $x = x(s)$ und $y = y(s)$ als Funktionen von $s$ dar, so daß wie in der Skizze $x(0) = y(0) = y'(0) = 0$ und $x'(0) = 1$.

( Hilfe:  $\kappa = \left| \frac{d\varphi}{ds} \right|$ ;  $x'^{2} + y'^{2} = 1$ ;  $\frac{y'}{x'} = \tan \varphi$ ; Integrale für x und y sind nicht elementar lösbar ! )

7. Die neutrale Faser einer Schraubenfeder wird dargestellt durch

$$
\mathbf {x} (t) = \left( \begin{array}{c} r \cos t \\ r \sin t \\ h t \end{array} \right), \quad 0 \leq t \leq 2 n \pi
$$

(r : Radius,  $2\pi h$  : Ganghöhe, n : Windungszahl).

a) Man drücke Krümmung κ und Torsion τ von x(t) sowohl durch die Höhe H und die Länge L der Feder als auch über den Winkel α aus (vgl. Skizze).

![](../../raw/pages_0385-0416/images/page_384_image_11.jpg)

<details>
<summary>text_image</summary>

F
H
r
L
α
2πnr
H
</details>

b) Eine Belastung $F$ der Feder in Richtung der Schraubachse ruft im Federstahl primär Torsion hervor und reduziert die Höhe auf $H(F)$. Die Torsionsgleichung lautet (in erster Näherung)

$$
G J \cdot [ \tau - \tau (F) ] = F \cdot r
$$

(GJ : Torsionssteifigkeit, τ(F) : Torsion mit Last F).

Man leite daraus eine Beziehung zwischen  $H(F)$  und F her und stelle die Federrate

$$
c = \lim _ {F \to 0} \frac {F}{H - H (F)}
$$

in erster Näherung als Funktion von $r$, $L$ und $GJ$ dar $(\frac{H}{L} \ll 1)$.

c) Die Federbeine eines VW K70 (Baujahr 1972) haben die Daten

Federstahl :  $GJ = 2.24 \cdot 10^{6} N cm^{2}$ ;

Vorderachse :  $r = 7.6 \, cm$ ,  $H = 12.6 \, cm$ , n = 5.5 ;

Hinterachse :  $r = 6.3 \, cm$ ,  $H = 18.7 \, cm$ , n = 7.5 .

Berechne jeweils die Länge des Federstahls und die Federrate c.

Wie weit sinkt das Auto vorne und hinten ein, wenn es gleichmäßig mit 1500 N belastet wird?

![](../../raw/pages_0385-0416/images/page_384_image_24.jpg)

<details>
<summary>natural_image</summary>

Line drawing of a mechanical suspension or spring assembly (no text or symbols)
</details>

---

370

7. Funktionen in mehreren Variablen. Teil 1: Differentiation

8. Im CAD werden ebene Kurven durch B-Splines dargestellt, da sie eine schnelle Beeinflussung der Form durch wenige sogenannte Kontrollpunkte erlauben. Im einfachsten Fall setzt man diese Kurven aus kubischen Kurvenstücken zusammen, für die man die BEZIER-BERNSTEIN-Darstellung verwendet.

$$
\mathbf {w} (t) = (1 - t) ^ {3} \mathbf {k} _ {0} + \binom {3} {1} t (1 - t) ^ {2} \mathbf {k} _ {1} + \binom {3} {2} t ^ {2} (1 - t) \mathbf {k} _ {2} + t ^ {3} \mathbf {k} _ {3}, 0 \leq t \leq 1.
$$

![](../../raw/pages_0385-0416/images/page_385_image_4.jpg)

a) Man rechnen nach: w verbindet  $k_{0}$  und  $k_{3}$ , Tangentenrichtung in  $k_{0}$  ist  $k_{1}-k_{0}$ , in  $k_{3}$  ist sie  $k_{2}-k_{3}$ .
b) Warum liegt w ganz im (konvexen) Viereck mit den Ecken  $k_{0}$ ,  $k_{1}$ ,  $k_{2}$ ,  $k_{3}$ ? (Hilfe: Die Polynomfaktoren vor  $k_{0},\ldots,k_{3}$  sind positiv und in der Summe 1.)
c) Welche Bedingungen müssen für eine Kurve erfüllt sein, die aus zwei Bezier-Kurvenstücken  $w_{1}$ ,  $w_{2}$  zusammengestzt ist, damit  $\dot{x}$  und  $\ddot{x}$  im gemeinsamen Kontrollpunkt stetig sind?

## §2. Reellwertige Funktionen mehrerer reeller Veränderlicher.

2.1 Grundlagen. Unter einer reellen Funktion von $n$ reellen Veränderlichen versteht man eine auf einer Teilmenge $D \subseteq \mathbb{R}^n$ erklärte Funktion $f : D \to \mathbb{R}$ mit Werten in $\mathbb{R}$. Sie ordnet jedem Punkt (bzw. Vektor) $\mathbf{x} = (x_1, \ldots, x_n)^T \in D$ des Definitionsbereiches in eindeutiger Weise eine reelle Zahl $z = f(\mathbf{x}) = f(x_1, \ldots, x_n)$ zu. Für Funktionen von 2 oder 3 Veränderlichen schreibt man üblicherweise auch $f(x, y)$ bzw. $f(x, y, z)$.

Die Zuordnung $\mathbf{x} \mapsto f(x_1, \ldots, x_n)$ kann gegeben sein

1. durch eine explizite Rechenvorschrift, z.B.

$$
f (x, y) = 3 x y + 2 x + 5 y - 7 \quad (D = \mathbb {R} ^ {2}), \text { oder }
$$

$$
f (x, y, z) = e ^ {x + y} \cdot 3 z \cdot \sin (x z) + \ln (x ^ {2} + y ^ {2}) + 5 z \quad (D = \mathbb {R} ^ {3} \setminus \{0 \}),
$$

2. durch eine implizite Gleichung, z.B. bezeichne $f(x,y)$ die eindeutig bestimmte positive Lösung $z$ der Gleichung $z^{3}-xz-y=0$ ($x\in\mathbb{R}$, $y>0$),
3. durch eine kompliziertere Vorschrift, etwa in Form einer Differentialgleichung oder in Tabellenform.

Eine reellwertige Funktion $f: \mathbb{R}^{n} \supseteq D \to \mathbb{R}$ wird häufig als Skalarenfeld oder Belegungsfunktion bezeichnet, insbesondere dann, wenn jeder Punkt $\mathbf{x} \in D$ mit

---

§2. Reellwertige Funktionen mehrerer reeller Veränderlicher.

371

der Maßzahl $f(\mathbf{x})$ einer skalaren physikalischen Größe (etwa Ladungsdichte, Temperatur) „belegt“ ist.

Als besonders vorteilhaft zur Diskussion einer Funktion $f: \mathbb{R}^{n} \supseteq D \to \mathbb{R}$, erweist es sich, $f$ auf gezielt gewählten Teilbereichen von $D$ zu untersuchen. Das sind in erster Linie

\- die Niveaumengen oder Niveauhyperflächen von $f$ zum (konstanten) Niveau $c \in \mathbb{R}$:

$$
N _ {c} := \left\{\mathbf {x} \in D; f (\mathbf {x}) = c \right\},
$$

\- alle zu einer Koordinatenachse parallelen Geraden, die $D$ treffen. Man erhält damit die „partiellen“ Funktionen von $f$:

$$
x _ {i} \mapsto f (a _ {1}, \dots , a _ {i - 1}, x _ {i}, a _ {i + 1}, \dots , a _ {n})
$$

mit $a = (a_{1},\dots ,a_{n})\in D$ konstant.

Wie im Falle n = 1 läßt sich jeder Funktion  $f : D \to R$  auch der Graph

$$
\Gamma_ {f} := \left\{\left(\mathbf {x}, f (\mathbf {x})\right); \mathbf {x} \in D \right\} \subseteq \mathbb {R} ^ {n + 1}
$$

zuordnen. Er besteht aus allen Punkten  $(x_{1},\ldots,x_{n},x_{n+1})$  mit  $x_{n+1}=f(x_{1},\ldots,x_{n})$  und kann somit als Niveauhyperfläche der Funktion

$$
F (x _ {1}, \dots , x _ {n}, x _ {n + 1}) = x _ {n + 1} - f (x _ {1}, \dots , x _ {n})
$$

zum Niveau 0 angesehen werden. Wir nennen $F(x_{1},\ldots,x_{n+1})=0$ die implizite und $x_{n+1}=f(x_{1},\ldots,x_{n})$ die explizite Darstellung des Graphen $\Gamma_{f}$.

All diese Begriffe sind für n = 2 und n = 3 sehr anschaulich zu interpretieren:

$n = 2: N_{c}$ ist in der Regel eine ebene Kurve, „die Niveaukurve $f(x,y) = c$“. Man nennt $f(x,y) = c$ die implizite Gleichung (oder Darstellung) dieser Kurve. Beschreibt etwa $T = f(x,y)$ die Temperaturverteilung (Druckverteilung) auf einer Platte $D \subseteq \mathbb{R}^{2}$, dann ist $f(x,y) = T_{0}$ die Gleichung einer Isotherme (Isobare). Ist $f(x,y) = c$ nach $y$ auflösbar in der Form $y = h(x,c)$, dann nennt man dieses eine explizite Darstellung der Niveaukurve.

Beispiele. 1. Die Gerade $2x + 3y = 5$ ist die Niveaukurve der Funktion $f(x,y) = 2x + 3y$ zum Niveau $c = 5$. Die explizite Darstellung lautet $y = -\frac{2}{3}x + \frac{5}{3}$.

2. Der Kreis $x^{2} + y^{2} = r^{2} \quad (r > 0)$ ($\rightarrow$ Abb. 165) ist die Niveaukurve der Funktion $f(x, y) = x^{2} + y^{2}$ zum Niveau $r^{2}$. Diese Kurve ist nicht überall explizit durch eine einzige Funktion $y = h(x)$ darstellbar. Sie besteht vielmehr aus zwei Teilen, die explizit darstellbar sind: $y = \sqrt{r^{2} - x^{2}}$ und $y = -\sqrt{r^{2} - x^{2}}$ ($-r \leq x \leq r$). Allgemein ist ein Kegelschnitt $ax^{2} + by^{2} + cxy + dx + ey + f = 0$ die Niveaukurve eines quadratischen Polynoms in $x, y$.

3. Jeder Graph  $y = h(x)$  einer (stetigen) Funktion der einen Variablen x kann als Niveaukurve  $F(x, y) = y - f(x) = 0$  einer Funktion von zwei Veränderlichen angesehen werden.

---

372

7. Funktionen in mehreren Variablen. Teil 1: Differentiation

Im Falle $n = 2$ wird der Graph $\Gamma_{f}$ als Fläche im $\mathbb{R}^{3}$ veranschaulicht. $D$ ist Teilmenge der $(x,y)$-Ebene und über $(x,y) \in D$ liegt der Flächenpunkt $(x,y,z)$ mit $z = f(x,y)$.

Die Graphen der „partiellen“ Funktionen  $z = f(a_{1}, y)$  und  $z = f(x, a_{2})$  entstehen durch Schnitt des Graphen  $\Gamma_{f}$  mit den zur z-Achse parallelen Ebenen:  $x = a_{1}$  bzw.  $y = a_{2}$ . Zur Untersuchung des Graphen  $\Gamma_{f}$  im Punkt  $(a_{1}, a_{2})$  wird man auf diese beiden Schnittkurven zurückgreifen.

![](../../raw/pages_0385-0416/images/page_387_image_4.jpg)

<details>
<summary>text_image</summary>

x=a₁
z=f(a₁,y)
Γf
x
D
y=a₂
z=f(x,a₂)
(a₁,a₂)
</details>

Abb. 164 - Partielle Funktionen

Über der Niveaulinie $f(x,y)=c$ in $D$ liegen alle Punkte von $\Gamma_{f}$ mit derselben „Höhe“ $z=c$. Sie ist die senkrechte Projektion der Schnittkurve der Fläche $z=f(x,y)$ mit der Ebene $z=c$ in die $(x,y)$-Ebene (Höhenlinien einer Landkarte).

![](../../raw/pages_0385-0416/images/page_387_image_7.jpg)

<details>
<summary>text_image</summary>

z
z=f(x,y)
z=const.
x
y
Niveaulinie
</details>

![](../../raw/pages_0385-0416/images/page_387_image_8.jpg)

<details>
<summary>text_image</summary>

z=const.
y
x
</details>

Abb. 165 - Graph und Niveaulinie von $f(x, y) = x^2 + y^2$

n=3: $N_c$ ist (unter Zusatzvoraussetzungen an $f$) eine Fläche im $\mathbb{R}^3$, „die Niveaufläche $f(x,y,z) = c$“. Man nennt $f(x,y,z) = c$ die implizite Gleichung (oder Darstellung) dieser Fläche. Ist diese Gleichung für einen Teilbereich explizit in der Form $z = h(x,y,c)$ auflösbar, dann nennt man dieses eine explizite Darstellung des entsprechenden Flächenstücks.

![](../../raw/pages_0385-0416/images/page_387_image_11.jpg)

<details>
<summary>text_image</summary>

f=2
f=3
f=4
f=5
(2/3/4)
z
x
y
</details>

Abb. 166 - Niveauflächen von $f = 2x + 3y + 4z$

Beispiele. 1. Die Ebene $2x + 3y + 4z = 5$ ist Niveaufläche der linearen Funktion $f(x,y,z) = 2x + 3y + 4z$

2. Niveaufläche eines quadratischen Polynoms in drei Veränderlichen ist jede Quadrik  $x^{T}Ax+b^{T}x+c=0$  im  $R^{3}$ . ☐

---

§2. Reellwertige Funktionen mehrerer reeller Veränderlicher.

373

Der Graph $\Gamma_{f}$ einer Funktion von drei Variablen ist Teilmenge des $\mathbb{R}^{4}$ und daher für eine Veranschaulichung von $f$ nicht geeignet.

2.2 Grenzwerte und Stetigkeit. Begriffe der anschaulichen Geometrie des  $R^{1}$ ,  $R^{2}$ ,  $R^{3}$  wurden in Kap. 6, 6.3, für beliebige  $n \in N$  in den  $R^{n}$  übernommen. So wird der Abstand zweier Punkte  $x, y \in R^{n}$  definiert durch

$$
| \mathbf {x} - \mathbf {y} | = \sqrt {\sum_ {i = 1} ^ {n} (x _ {i} - y _ {i}) ^ {2}}.
$$

Zu festem $\mathbf{a} \in \mathbb{R}^n$ und $r > 0$ heißt die Punktmenge

$$
U _ {r} (\mathbf {a}) := \{\mathbf {x} \in \mathbb {R} ^ {n}: | \mathbf {x} - \mathbf {a} | <   r \}
$$

r-Umgebung von a.

Für $n = 1$ ist $U_{r}(a)$ das offene Intervall $a - r < x < a + r$,

für $n=2$ besteht $U_{r}(\mathbf{a})$ aus allen Punkten der Kreisscheibe mit dem Mittelpunkt $\mathbf{a}$ und Radius $r$ ohne Randpunkte,

für n = 3 ist  $U_{r}(\mathbf{a})$  eine Kugel um a mit dem Radius r ohne die Punkte der Kugeloberfläche.

Bereits für reelle, auf einem Intervall $I \subseteq \mathbb{R}$ definierte Funktionen ist nicht nur deren Verhalten im Innern von $I$, sondern auch in den Randpunkten von Bedeutung ($\rightarrow$ Kap. 2, §5 und Kap. 3). Zur Beschreibung ähnlicher Sachverhalte im $\mathbb{R}^n$ benötigen wir einige Begriffe.

Definition. Sei D eine Teilmenge des $\mathbb{R}^{n}$.

a) Ein Punkt $\mathbf{a} \in D$ heißt innerer Punkt von $D$, wenn es eine $r$-Umgebung von $\mathbf{a}$ gibt, die ganz in $D$ enthalten ist.
b) D heißt offen, wenn jeder Punkt von D ein innerer Punkt ist.
c) Ein Punkt $\mathbf{b} \in \mathbb{R}^{n}$ heißt Randpunkt von $D$, wenn jede $r$-Umgebung von $\mathbf{b}$ sowohl mindestens einen Punkt aus $D$ als auch mindestens einen nicht zu $D$ gehörenden Punkt enthält. Die Menge aller Randpunkte von $D$ heißt Rand von $D$ und wird mit $\partial D$ bezeichnet.
d) Eine Menge heißt abgeschlossen, wenn sie alle ihre Randpunkte enthält.

## Beispiele.

1. Die „offene“ Kreisscheibe (ohne Rand)

$$
K = \{(x, y); (x - x _ {0}) ^ {2} + (y - y _ {0}) ^ {2} <   r ^ {2} \}
$$

ist eine offene Menge mit dem Rand  $\partial K : (x - x_{0})^{2} + (y - y_{0})^{2} = r^{2}$ .

---

374

7. Funktionen in mehreren Variablen. Teil 1: Differentiation

2. Das „Rechteck“ $Q = \{ (x, y) ; 2 \leq x < 3, -1 < y \leq 2 \}$ ($\rightarrow$ Abb. 167a) ist weder offen noch abgeschlossen. Alle Punkte $(x, y)$ mit $2 < x < 3, -1 < y < 2$ sind innere Punkte. Der Rand enthält sowohl Punkte, die zu $Q$ gehören (etwa $(2, y)$ mit $-1 < y \leq 2$) als auch solche, die nicht zu $Q$ gehören (etwa $(x, -1)$ mit $2 \leq x \leq 3$).

Offene Mengen werden oft durch strikte Ungleichungen in der Form

$$
U = \{\mathbf {x} \in \mathbb {R} ^ {n}; g _ {1} (\mathbf {x}) <   0, \dots , g _ {r} (\mathbf {x}) <   0 \}
$$

beschrieben, wobei $g_1, \ldots, g_r$ stetige Funktionen in $n$ Veränderlichen sind. Für $\mathbf{x} \in \partial U$ gilt $g_i(\mathbf{x}) = 0$ für wenigstens ein $i$. (Kurz: $U$ wird berandet von den Hyperflächen $g_i(\mathbf{x}) = 0$.)

$$
U \cup \partial U = \left\{\mathbf {x} \in \mathbb {R} ^ {n}; g _ {1} (\mathbf {x}) \leq 0, \dots , g _ {r} (\mathbf {x}) \leq 0 \right\}.
$$

![](../../raw/pages_0385-0416/images/page_389_image_7.jpg)

<details>
<summary>text_image</summary>

y
2
1
Q
1
2
3 x
-1
</details>

Abb. 167a - Randpunkte

![](../../raw/pages_0385-0416/images/page_389_image_9.jpg)

<details>
<summary>text_image</summary>

z = f(x,y)
z=1
y
x
1
</details>

Abb. 167b - Die Parabelfalte

Definition. Sei $f:\mathbb{R}^n\supseteq D\to \mathbb{R}$ und $\mathbf{a}\in D\cup \partial D$

a) $f$ hat in a den Grenzwert $c \in \mathbb{R}$, in Zeichen

$$
\lim _ {\mathbf {x} \to \mathbf {a}} f (\mathbf {x}) = c \quad \text {(oder} f (\mathbf {x}) \to c \text {fur} \mathbf {x} \to \mathbf {a}),
$$

wenn es zu jeder (beliebig kleinen) Schranke $\epsilon > 0$ eine $r$-Umgebung $U_r(\mathbf{a})$ gibt, so daß $|f(\mathbf{x}) - c| \leq \epsilon$ für alle $\mathbf{x} \in D \cap U_r(\mathbf{a})$ gilt.

b) $f$ heißt in $\mathbf{a} \in D$ stetig, wenn $\lim_{\mathbf{x} \to \mathbf{a}} f(\mathbf{x}) = f(\mathbf{a})$ gilt.
c) $f$ heißt auf $D$ stetig, wenn $f$ in allen $\mathbf{a} \in D$ stetig ist.

Die aus Kap. 2 bekannten Rechenregeln für Grenzwerte und stetige Funktionen gelten auch hier: Summe, Produkt, Quotient stetiger Funktionen sind stetig.

Beispiel. Die Projektionen  $p_{i}: R^{n} \rightarrow R$ ,  $p_{i}(\mathbf{x}) = x_{i}$  sind stetig. Aufgrund der soeben genannten Rechenregeln ist dann auch jede lineare Funktion  $l: R^{n} \rightarrow R$ ,  $l(\mathbf{x}) = \mathbf{a}^{T} \mathbf{x} = a_{1}x_{1} + a_{2}x_{2} + \cdots + a_{n}x_{n}$ , jedes Polynom in n Variablen

$$
p (\mathbf {x}) = \sum_ {1 \leq k _ {i} \leq m} \alpha_ {k _ {1} k _ {2} \dots k _ {n}} x _ {1} ^ {k _ {1}} x _ {2} ^ {k _ {2}} \dots x _ {n} ^ {k _ {n}}
$$

und jede rationale Funktion  $f(\mathbf{x}) = \frac{p(\mathbf{x})}{q(\mathbf{x})}$  stetig, falls  $q(\mathbf{x}) \neq 0$ .

---

§2. Reellwertige Funktionen mehrerer reeller Variabler

375

Die Stetigkeit von $f(x,y)$ in $(x_0,y_0)$ ergibt sich noch nicht aus der Stetigkeit der partiellen Funktionen $x\mapsto f(x,y_0)$ und $y\mapsto f(x_0,y)$.

Gegenbeispiel. Die Parabelfalte (→ Abb. 167b)

$$
f (x, y) := \left\{ \begin{array}{c l} \frac {2 x y ^ {2}}{x ^ {2} + y ^ {4}} & , \text {falls} x > 0, \\ 0 & , \text {falls} x \leq 0. \end{array} \right.
$$

Sowohl $x \mapsto f(x,0) = 0$ als auch $y \mapsto f(0,y) = 0$ und $t \mapsto f(tu,tv) = \frac{2tuv^2}{u^2 + t^2v^4}$ ($u > 0$) sind stetig. Dagegen ist $f(x,y)$ für $y > 0$ auf der Parabel $x = y^2$ konstant 1. Daher ist $f$ unstetig in (0,0).

Definition. a) Eine Menge $D \subseteq \mathbb{R}^n$ heißt beschränkt, wenn es eine Konstante $K > 0$ gibt mit

$$
| \mathbf {x} | <   K \quad f u r a l l e \mathbf {x} \in D.
$$

b) Die abgeschlossenen und beschränkten Mengen des $\mathbb{R}^{n}$ nennt man kompakt.

Beispielsweise ist die „Vollkugel“ um a vom Radius r,

$$
U _ {r} (\mathbf {a}) := \left\{\mathbf {x} \in \mathbb {R} ^ {n}; | \mathbf {x} - \mathbf {a} | \leq r \right\},
$$

(einschließlich des Randes  $|x - a| = r$ ) kompakt.

Ebenso wie im Fall einer Variablen (→ Satz 6.5, Kap. 2) gilt (ohne Beweis):

## Satz 2.1.

a) Satz vom Minimum und Maximum. Jede auf einer kompakten Menge $D \subseteq \mathbb{R}^n$ stetige Funktion nimmt auf $D$ ein Minimum und ein Maximum an; d.h., es gibt $\mathbf{a}, \mathbf{b} \in D$ mit $f(\mathbf{b}) \leq f(\mathbf{x}) \leq f(\mathbf{a})$ für alle $\mathbf{x} \in D$.

b) Satz von der gleichmäßigen Stetigkeit. Jede auf einer kompakten Menge $D \subseteq \mathbb{R}^n$ stetige Funktion ist dort gleichmäßig stetig; d.h. zu $\epsilon > 0$ gibt es ein $\delta > 0$, so daß für alle $\mathbf{x}, \mathbf{y} \in D$ gilt

$$
| \mathbf {x} - \mathbf {y} | <   \delta \Rightarrow | f (\mathbf {x}) - f (\mathbf {y}) | <   \epsilon .
$$

Satz 2.1 ist im allgemeinen falsch, wenn $D$ nicht kompakt ist ($\rightarrow$ eine Variable). Ist nun $D$ beliebig und besitzt die stetige Funktion $f: D \to \mathbb{R}$ in jedem Randpunkt $\mathbf{a} \in \partial D$ einen Grenzwert $c(\mathbf{a}) = \lim_{\mathbf{x} \to \mathbf{a}} f(\mathbf{x})$, so wird $f$ durch

$$
\tilde {f} (\mathbf {x}) := \left\{ \begin{array}{l l} f (\mathbf {x}) & , \text {falls} \mathbf {x} \in D \\ c (\mathbf {x}) & , \text {falls} \mathbf {x} \in \partial D \end{array} \right.
$$

zu einer stetigen Funktion  $\tilde{f}: D \cup \partial D \to R$  auf der abgeschlossenen Menge  $D \cup \partial D$  fortgesetzt.

Eine wichtige Eigenschaft stetiger Funktionen ergibt sich leicht aus der Definition: Ist $f: D \to \mathbb{R}$ stetig und $f(\mathbf{a}) > 0$, dann gilt $f(\mathbf{x}) > 0$ für alle $\mathbf{x} \in D \cap U_r(\mathbf{a})$ mit geeignetem $r > 0$.

---

376

7. Funktionen in mehreren Variablen. Teil 1: Differentiation

2.3 Partielle Ableitungen, der Gradient. Sei $D \subseteq \mathbb{R}^n$ offen, $f : D \to \mathbb{R}$ und $\mathbf{a} = (a_1, a_2, \ldots, a_n) \in D$. Existiert die Ableitung der „partiellen“ Funktion

$$
x _ {i} \mapsto f (a _ {1}, \dots , a _ {i - 1}, x _ {i}, a _ {i + 1}, \dots , a _ {n})
$$

an der Stelle $x_{i}=a_{i}$, so nennt man diese die partielle Ableitung von $f$ nach $x_{i}$ im Punkte $\mathbf{a}$; sie wird mit

$$
\left. \frac {\partial f (\mathbf {x})}{\partial x _ {i}} \right| _ {\mathbf {x} = \mathbf {a}} \quad \text {oder} \quad \frac {\partial f}{\partial x _ {i}} (\mathbf {a})
$$

bezeichnet. Das Zeichen „∂“ anstelle von „d“ soll verdeutlichen, daß von einer Funktion mit mehreren Variablen das Änderungsverhalten bezüglich einer einzelnen Veränderlichen untersucht wird, wobei für das Differenzieren die anderen Variablen als Konstante anzusehen sind:

$$
\begin{array}{r l}\frac {\partial f (\mathbf {x})}{\partial x _ {i}}&:= \lim _ {t \rightarrow 0} \frac {1}{t} \left[ f (x _ {1}, \dots , x _ {i} + t, \dots , x _ {n}) - f (x _ {1}, \dots , x _ {i}, \dots , x _ {n}) \right]\\&= \lim _ {t \rightarrow 0} \frac {1}{t} \left[ f (\mathbf {x} + t \mathbf {e} _ {i}) - f (\mathbf {x}) \right]\end{array}\tag {1}
$$

Für die partiellen Ableitungen sind ebenfalls die Bezeichnungen $f_{x_i}$ üblich, bzw. $f_x, f_y, f_z, f_t, \ldots$, wenn die Variablen $x, y, z, t, \ldots$ lauten. Dementsprechend schreibt man für die höheren partiellen Ableitungen

$$
f _ {x x} = \frac {\partial^ {2} f}{\partial x ^ {2}}, \quad f _ {x y} = (f _ {x}) _ {y} = \frac {\partial}{\partial y} \left(\frac {\partial f}{\partial x}\right), \quad \text {etc.}
$$

$f$ heißt partiell differenzierbar (bzw. stetig partiell differenzierbar), wenn alle partiellen Ableitungen $f_{N_i}$ existieren (und stetig sind).

Beispiele. 1. $f(x,y) = x^{2}y^{3} + y\ln x$ $(x > 0)$

$$
f _ {x} (x, y) = 2 y ^ {3} x + \frac {y}{x}, \quad f _ {y} (x, y) = 3 x ^ {2} y ^ {2} + \ln x,
$$

$$
f _ {x x} (x, y) = 2 y ^ {3} - \frac {y}{x ^ {2}}, \quad f _ {y y} (x, y) = 6 x ^ {2} y, \quad f _ {x y} (x, y) = 6 y ^ {2} x + \frac {1}{x} = f _ {y x} (x, y).
$$

2. Der Schalldruck einer ebenen Schallwelle wird bestimmt durch

$$
p (x, y, z, t) = A \sin (\alpha x + \beta y + \gamma z - \omega t)
$$

$\frac{\partial p}{\partial x} = \alpha A \cos(\alpha x + \beta y + \gamma z - \omega t)$ beschreibt (bei fester Zeit) die Änderung in x-Richtung.

$\frac{\partial p}{\partial t} = -\omega A \cos(\alpha x + \beta y + \gamma z - \omega t)$ bestimmt am festen Ort $(x, y, z)$ die zeitliche (momentane) Änderung.

Faßt man die partiellen Ableitungen einer Funktion zu einem Vektor zusammen,

---

§2. Reellwertige Funktionen mehrerer reeller Veränderlicher.

377

so erhält man den Gradienten von $f$ an der Stelle $\mathbf{x}$:

$$
\operatorname{grad} f (\mathbf {x}) := \left( \begin{array}{c} \frac {\partial f}{\partial x _ {1}} (\mathbf {x}) \\ \frac {\partial f}{\partial x _ {2}} (\mathbf {x}) \\ \vdots \\ \frac {\partial f}{\partial x _ {n}} (\mathbf {x}) \end{array} \right) \in \mathbb {R} ^ {n}  .
$$

$\mathbf{x} \mapsto \text{grad } f(\mathbf{x})$ ist eine vektorwertige Funktion (ein „Vektorfeld“ → §4): Jedem $\mathbf{x} \in D$ wird der Vektor grad $f(\mathbf{x}) \in \mathbb{R}^{n}$ zugeordnet (vorausgesetzt, $f$ ist partiell differenzierbar).

Beispiel.  $f(x,y,z)=e^{x+2y}+2x\sin z+z^{2}xy,$

$$
\operatorname{grad} f (x, y, z) = \left( \begin{array}{c} f _ {x} (x, y, z) \\ f _ {y} (x, y, z) \\ f _ {z} (x, y, z) \end{array} \right) = \left( \begin{array}{c} e ^ {x + 2 y} + 2 \sin z + z ^ {2} y \\ 2 e ^ {x + 2 y} + z ^ {2} x \\ 2 x \cos z + 2 z x y \end{array} \right).
$$

f heißt zweimal (k-mal) partiell differenzierbar, wenn alle zweiten partiellen Ableitungen

$$
f _ {x _ {i} x _ {j}} = (f _ {x _ {i}}) _ {x _ {j}} = \frac {\hat {c}}{\hat {c} x _ {j}} \left(\frac {\hat {c} f}{\hat {c} x _ {i}}\right) \qquad (1 \leq i, j \leq n)
$$

(alle $k$-ten Ableitungen $f_{X_{i_1} \ldots X_{i_k}}$) existieren. Sind sämtliche dieser Ableitungen stetig, dann heißt $f$ zweimal (bzw. $k$-mal) stetig partiell differenzierbar.

Wir bezeichnen die Menge aller auf einer offenen Menge $D \subseteq \mathbb{R}^n$ $k$-mal stetig partiell differenzierbaren Funktionen $f : D \to \mathbb{R}$ mit $\mathscr{C}^k(D, \mathbb{R})$ und nennen $f \in \mathscr{C}^k(D, \mathbb{R})$ eine $\mathscr{C}^k$-Funktion.

$$
\mathscr {C} ^ {k} (D, \mathbb {R}) := \{f: D \rightarrow \mathbb {R}; f k \text {-mal stetig partiell differenzierbar} \}
$$

$$
\mathscr {C} ^ {0} (D, \mathbb {R}) := \{f: D \to \mathbb {R}; f \text {ist stetig} \}
$$

Im vorhergehenden ersten Beispiel sahen wir $f_{xy} = f_{yx}$. Dies ist nicht immer der Fall:

Gegenbeispiel. Es sei  $f(x,y)=\left\{\begin{array}{cc}xy\frac{x^{2}-y^{2}}{x^{2}+y^{2}} & , (x,y) \neq (0,0) \\ 0 & , (x,y) = (0,0)\end{array}\right.$ .

Da für alle $x, y \in \mathbb{R}$ stets $f(x,0) = f(0,y) = 0$, gilt $f_x(0,0) = f_y(0,0) = 0$. Für $(x,y) \neq (0,0)$ erhält man durch Differentiation

$$
f _ {x} = y \left(\frac {x ^ {2} - y ^ {2}}{x ^ {2} + y ^ {2}} + \frac {4 x ^ {2} y ^ {2}}{(x ^ {2} + y ^ {2}) ^ {2}}\right) ,
$$

$$
f _ {y} = x \left(\frac {x ^ {2} - y ^ {2}}{x ^ {2} + y ^ {2}} - \frac {4 x ^ {2} y ^ {2}}{(x ^ {2} + y ^ {2}) ^ {2}}\right) .
$$

---

378

7. Funktionen in mehreren Variablen. Teil 1: Differentiation

Damit folgt für  $f_{xy} = \frac{\partial}{\partial y} \left( \frac{\partial f}{\partial x} \right)$

$$
f _ {x y} (0, 0) = \lim _ {y \to 0} \frac {f _ {x} (0 , y) - f _ {x} (0 , 0)}{y} = \lim _ {y \to 0} \frac {- y ^ {2}}{y ^ {2}} = - 1
$$

und andererseits

$$
f _ {y x} (0, 0) = \lim _ {x \to 0} \frac {f _ {y} (x , 0) - f _ {y} (0 , 0)}{x} = \lim _ {x \to 0} \frac {x ^ {2}}{x ^ {2}} = 1.
$$

## Satz 2.2 von SCHWARZ über die Vertauschbarkeit der partiellen Ableitungen.

Für jede $\mathscr{C}^2$-Funktion $f: D \to \mathbb{R}$, $D \subseteq \mathbb{R}^n$ offen, gilt

$$
\boxed {\frac {\partial}{\partial x _ {i}} \left(\frac {\partial f}{\partial x _ {j}}\right) = \frac {\partial}{\partial x _ {j}} \left(\frac {\partial f}{\partial x _ {i}}\right) \quad (1 \leq i, j \leq n).} \tag {2}
$$

Beweis für $n = 2$. Sei $(x_0, y_0) \in D$ und $t \in \mathbb{R}$ so klein, daß das Quadrat $Q$ mit den Eckpunkten  $(x_{0}, y_{0})$ ,  $(x_{0} + t, y_{0})$ ,  $(x_{0}, y_{0} + t)$ ,  $(x_{0} + t, y_{0} + t)$  ganz in D enthalten ist. Für

$$
g (x) := f (x, y _ {0} + t) - f (x, y _ {0})
$$

gilt  $g'(x) = f_x(x, y_0 + t) - f_x(x, y_0)$  und durch Mehrfachanwendung des Mittelwertsatzes für Funktionen einer Veränderlichen folgt

![](../../raw/pages_0385-0416/images/page_393_image_13.jpg)

<details>
<summary>text_image</summary>

y
η₁
η₂
(x₀+t, y₀+t)
(x₀,y₀)
ξ₂
ξ₁
x
</details>

Abb. 168 - Zu $f_{xy} = f_{yx}$

$$
\begin{array}{l} h (t) := f (x _ {0} + t, y _ {0} + t) - f (x _ {0} + t, y _ {0}) - f (x _ {0}, y _ {0} + t) + f (x _ {0}, y _ {0}) \\ = g (x _ {0} + t) - g (x _ {0}) \\ = g ^ {\prime} (\xi_ {1}) t = [ f _ {x} (\xi_ {1}, y _ {0} + t) - f _ {x} (\xi_ {1}, y _ {0}) ] t \\ = f _ {x y} (\xi_ {1}, \eta_ {1}) t ^ {2} \\ \end{array}
$$

mit $\xi_{1}$ zwischen $x_{0}+t$ und $x_{0}$ bzw. $\eta_{1}$ zwischen $y_{0}+t$ und $y_{0}$. Ebenso - mit $\tilde{g}(y):=f(x_{0}+t,y)-f(x_{0},y)-\text{folgt } h(t)=\tilde{g}(y_{0}+t)-\tilde{g}(y_{0})=f_{yx}(\xi_{2},\eta_{2})t^{2}$ mit $(\xi_{2},\eta_{2})\in Q$ und damit

$$
f _ {x y} (\xi_ {1}, \eta_ {1}) = f _ {y x} (\xi_ {2}, \eta_ {2}).
$$

Aufgrund der Stetigkeit folgt beim Grenzübergang $t \to 0$ die Behauptung: $f_{xy}(x_0, y_0) = f_{yx}(x_0, y_0)$.

Eine Mehrfachanwendung dieses Satzes zeigt etwa für eine Funktion in x, y, z  $f_{xyx} = f_{xxy} = f_{yxx}$ ,  $f_{xyz} = f_{zyx} = f_{yzx} = \cdots$ , etc., vorausgesetzt, sämtliche vorkommenden Ableitungen sind stetig.

---

§2. Reellwertige Funktionen mehrerer reeller Veränderlicher.

379

2.4 Die totale Ableitung und lineare Approximation. Die Approximation einer Funktion durch eine (einfachere) „Ersatzfunktion“ ist ein zentrales Thema der Analysis. Zur Beschreibung der Approximationsgüte verwenden wir folgende Abkürzung:

Definition des „o-Symbols“. Für zwei Funktionen $f, g : \mathbb{R}^{n} \supseteq D \to \mathbb{R}$ und $\mathbf{x}_{0} \in D$, $k \in \mathbb{N}$, schreibt man

$$
\begin{array}{l}f (\mathbf {x}) = g (\mathbf {x}) + o (| \mathbf {x} - \mathbf {x} _ {0} | ^ {k}) \quad \text {(fur} \mathbf {x} \rightarrow \mathbf {x} _ {0})\\\text {falls} \lim _ {\mathbf {x} \rightarrow \mathbf {x} _ {0}} \frac {f (\mathbf {x}) - g (\mathbf {x})}{| \mathbf {x} - \mathbf {x} _ {0} | ^ {k}} = 0.\end{array}\tag {3}
$$

Das so definierte $o$-Symbol ist keine eindeutig festgelegte Funktion. Die Gleichung $f(\mathbf{x}) = g(\mathbf{x}) + o(|\mathbf{x} - \mathbf{x}_0|^k)$ besagt, daß der bei der Approximation von $f$ durch $g$ in der Nähe des Punktes $\mathbf{x}_0$ gemachte Fehler $R(\mathbf{x}, \mathbf{x}_0) := f(\mathbf{x}) - g(\mathbf{x})$ klein ist im Vergleich zu $|\mathbf{x} - \mathbf{x}_0|^k$, in dem Sinne, daß $\lim_{\mathbf{x} \to \mathbf{x}_0} \frac{R(\mathbf{x}, \mathbf{x}_0)}{|\mathbf{x} - \mathbf{x}_0|^k} = 0$ gilt. Insbesondere folgt

$$
\lim _ {\mathbf {x} \to \mathbf {x} _ {0}} (f (\mathbf {x}) - g (\mathbf {x})) = \lim _ {\mathbf {x} \to \mathbf {x} _ {0}} R (\mathbf {x}, \mathbf {x} _ {0}) = \lim _ {\mathbf {x} \to \mathbf {x} _ {0}} | \mathbf {x} - \mathbf {x} _ {0} | ^ {k} \frac {R (\mathbf {x} , \mathbf {x} _ {0})}{| \mathbf {x} - \mathbf {x} _ {0} | ^ {k}} = 0. \tag {4}
$$

![](../../raw/pages_0385-0416/images/page_394_image_7.jpg)

Die Approximation einer differenzierbaren Funktion einer Variablen $f: I \to \mathbb{R}$ ($I \subseteq \mathbb{R}$ ein offenes Intervall) in der Umgebung von $x_0 \in I$ durch die lineare Funktion $g(x) = f(x_0) + f'(x_0)(x - x_0)$ ($\rightarrow$ Kap. 3, §1.3) wird mit dem $o$-Symbol geschrieben als

$$
f (x) = f (x _ {0}) + f ^ {\prime} (x _ {0}) (x - x _ {0}) + o (| x - x _ {0} |) \tag {5}
$$

Für Funktionen von mehreren Variablen gewährleistet die partielle Differenzierbarkeit allein noch nicht die analoge Approximation durch lineare Funktionen ( $\rightarrow$  Aufg. 6).

Definition. Sei $D \subseteq \mathbb{R}^n$ offen. Eine Funktion $f: D \to \mathbb{R}$ heißt in $\mathbf{x}_0 \in D$ total differenzierbar (oder linear approximierbar), wenn es einen Vektor $\mathbf{a} \in \mathbb{R}^n$ mit

$$
f (\mathbf {x}) = f (\mathbf {x} _ {0}) + \mathbf {a} \cdot (\mathbf {x} - \mathbf {x} _ {0}) + o (| \mathbf {x} - \mathbf {x} _ {0} |) \tag {6}
$$

(für x nahe  $x_{0}$ ) gibt.

---

380

7. Funktionen in mehreren Variablen. Teil 1: Differentiation

Satz 2.3. Ist $f$ in $\mathbf{x}_{0}\in D$ total differenzierbar, $f(\mathbf{x}) = f(\mathbf{x}_{0}) + \mathbf{a}\cdot (\mathbf{x} - \mathbf{x}_{0}) + o(|\mathbf{x} - \mathbf{x}_{0}|)$, dann gilt:

a) $f$ ist in $\mathbf{x}_0$ stetig;
b) $\lim_{t\to 0}\frac{1}{t} [f(\mathbf{x}_0 + t\mathbf{v}) - f(\mathbf{x}_0)] = \mathbf{a}\cdot \mathbf{v}$ (für alle $\mathbf{v}\in \mathbb{R}^n$ , $\mathbf{v}\neq 0$ );
c) $f$ ist partiell differenzierbar und $\mathbf{a}$ eindeutig bestimmt als $\mathbf{a} = \operatorname{grad} f(\mathbf{x}_0)$.

Beweis. a) folgt aus (4).

b): Für Punkte der Geraden  $x_{0} + tv$  ergibt (6)  $f(\mathbf{x}_{0} + tv) - f(\mathbf{x}_{0}) = t\mathbf{a} \cdot \mathbf{v} + o(|tv|)$ . Division durch t mit anschließendem Grenzübergang  $t \to 0$  liefert die Behauptung.

c): Man nimmt $\mathbf{v} = \mathbf{e}_i$ in b) und erhält mit (1) $\frac{\partial f}{\partial x_i} (\mathbf{x}_0) = \mathbf{a} \cdot \mathbf{e}_i = a_i$ (die $i$-te Koordinate von $\mathbf{a}$).

Im Sinne der Definition (6) bedeutet also

$$
\begin{array}{l} f (\mathbf {x}) = f \left(\mathbf {x} _ {0}\right) + \operatorname{grad} f \left(\mathbf {x} _ {0}\right) \cdot \left(\mathbf {x} - \mathbf {x} _ {0}\right) + o \left(| \mathbf {x} - \mathbf {x} _ {0} |\right) \\ \text {die lineare Approximation von} f (\mathbf {x}) \text {nahe bei} \mathbf {x} _ {0}. \end{array} \tag {7}
$$

Anschauliche Deutung für $n = 2$: Die „über“ $D \subseteq \mathbb{R}^2$ liegende Fläche (der Graph) $z = f(x, y)$ wird in der Nähe

des Flächenpunktes  $(x_{0}, y_{0}, f(x_{0}, y_{0}))$  durch die Ebene

$$
\begin{array}{l} z = f (x _ {0}, y _ {0}) + f _ {x} (x _ {0}, y _ {0}) (x - x _ {0}) + \\ + f _ {y} (x _ {0}, y _ {0}) (y - y _ {0}) \\ \end{array}
$$

mit einem Fehler

$$
R (x, y) = o \left(\sqrt {(x - x _ {0}) ^ {2} + (y - y _ {0}) ^ {2}}\right)
$$

approximiert. Diese Ebene heißt Tangentialbene der Fläche $z = f(x, y)$ im Punkt $(x_0, y_0, f(x_0, y_0))$. Sie enthält sämtliche Flächentangenten ($\rightarrow$ 3.1). □

![](../../raw/pages_0385-0416/images/page_395_image_18.jpg)

<details>
<summary>text_image</summary>

Tangentialebene
z = f(x,y)
x
y
z
D
- grad f(x₀,y₀) (x₀,y₀)
</details>

Abb. 170 - Tangentialebene

Bemerkung. Über die tatsächliche Größe des Fehlers bei der Approximation von $f(\mathbf{x})$ durch $f(\mathbf{x}_{0}) + \text{grad } f(\mathbf{x}_{0}) \cdot (\mathbf{x} - \mathbf{x}_{0})$ werden wir erst in 3.2 genauere Angaben machen. Vorerst begnügen wir uns mit der qualitativen Fehlerangabe $o(|\mathbf{x} - \mathbf{x}_{0}|)$.

Satz 2.4. Jede $\mathcal{C}^{1}$-Funktion $f: D \to \mathbb{R}$ ($D \subseteq \mathbb{R}^{n}$ offen) ist auf $D$ (d.h. in allen Punkten von $D$) total differenzierbar.

Beweis für $n=2$. Sei $(x_{0},y_{0})\in D$. Für alle $(x,y)$ aus einer (hinreichend kleinen) $r$-Umgebung $U_{r}(x_{0},y_{0})\subseteq D$ gilt nach dem Mittelwertsatz für Funktionen

---

§2. Reellwertige Funktionen mehrerer reeller Veränderlicher.

381

einer Veränderlichen

$$
\begin{array}{l} f (x, y) - f (x _ {0}, y _ {0}) = f (x, y) - f (x _ {0}, y) + f (x _ {0}, y) - f (x _ {0}, y _ {0}) \\ = f _ {x} (\xi , y) (x - x _ {0}) + f _ {y} (x _ {0}, \eta) (y - y _ {0}) \\ \end{array}
$$

mit $\xi$ zwischen $x$ und $x_0$, $\eta$ zwischen $y$ und $y_0$. Es folgt

$$
f (x, y) = f (x _ {0}, y _ {0}) + \operatorname{grad} f (x _ {0}, y _ {0}) \cdot \binom{x - x _ {0}}{y - y _ {0}} + R (x, y)
$$

mit der Funktion

$$
\begin{array}{l} R (x, y) = [ f _ {x} (\xi , y) - f _ {x} (x _ {0}, y _ {0}) ] (x - x _ {0}) + [ f _ {y} (x _ {0}, \eta) - f _ {y} (x _ {0}, y _ {0}) ] (y - y _ {0}) \\ = o \left(\sqrt {(x - x _ {0}) ^ {2} + (y - y _ {0}) ^ {2}}\right). \\ \end{array}
$$

Die letzte Beziehung ergibt sich aus der Stetigkeit von  $f_{x}$  und  $f_{y}$  und aus  $\frac{|x - x_{0}|}{\sqrt{(x - x_{0})^{2} + (y - y_{0})^{2}}} \leq 1$ ,  $\frac{|y - y_{0}|}{\sqrt{(x - x_{0})^{2} + (y - y_{0})^{2}}} \leq 1$ . ☐

Beispiele. 1. In der Umgebung von (1,1) lautet die lineare Approximation der $\mathcal{C}^{1}$-Funktion $f(x,y)=x^{4}+2x^{3}y^{2}+y$:

$$
\begin{array}{l} f (x, y) = f (1, 1) + \operatorname{grad} f (1, 1) \cdot \binom{x - 1}{y - 1} + o \big (\sqrt {(x - 1) ^ {2} + (y - 1) ^ {2}} \big) \\ = 4 + 1 0 (x - 1) + 5 (y - 1) + o \left(\sqrt {(x - 1) ^ {2} + (y - 1) ^ {2}}\right). \\ \end{array}
$$

Dementsprechend ist

$$
z = 4 + 1 0 (x - 1) + 5 (y - 1)
$$

die Gleichung der Tangentialebene der Fläche  $z = x^{4} + 2x^{3}y^{2} + y$  im Flächenpunkt (1,1,4).

2. Die lineare Approximation der  $C^{1}$ -Funktion  $f(x,y,z)=e^{y+2y}+z\sin y+x$  im Nullpunkt lautet

$$
\begin{array}{l} f (x, y, z) = f (0, 0, 0) + f _ {x} (0, 0, 0) x + f _ {y} (0, 0, 0) y + f _ {z} (0, 0, 0) z + o \left(\sqrt {x ^ {2} + y ^ {2} + z ^ {2}}\right) \\ = 1 + 2 x + 2 y + o \left(\sqrt {x ^ {2} + y ^ {2} + z ^ {2}}\right). \\ \end{array}
$$

2.5 Einfache Anwendungen. Für einfache Näherungs- und Fehlerrechnungen wird in (7) der „o-Anteil“ vernachlässigt und  $f(\mathbf{x})$  in der Nähe des Punktes  $x_{0}$  durch  $f(\mathbf{x}_{0}) + \text{grad } f(\mathbf{x}_{0}) \cdot (\mathbf{x} - \mathbf{x}_{0})$  ersetzt. Man schreibt dafür

$$
f (\mathbf {x}) \approx f (\mathbf {x} _ {0}) + \text {grad} f (\mathbf {x} _ {0}) \cdot (\mathbf {x} - \mathbf {x} _ {0}). \tag {8}
$$

① Näherungsrechnung. Beispiel.  $f(x,y) = x^{y} = e^{y \ln x}$  wird in (1,3) angenähert durch  $f(x,y) \approx 1 + 3(x - 1) + 0(y - 1)$ ; speziell  $1.02^{3.01} \approx 1.06$  (der genaue Wert:  $1.02^{3.01} = 1.061418168\ldots$ ).

---

382

7. Funktionen in mehreren Variablen. Teil 1: Differentiation

② Fehlerrechnung. Werden statt der wahren Werte  $\mathbf{x} = (x_{1}, \ldots, x_{n})$  die Näherungswerte  $\mathbf{x}_{0} = (x_{01}, \ldots, x_{0n})$  gemessen, dann belasten die Meßfehler  $|\Delta x_{i}| = |x_{i} - x_{0i}|$  den Funktionswert mit dem Fehler

$$
\begin{array}{l} \left| \Delta f (\mathbf {x}) \right| = \left| f (\mathbf {x}) - f (\mathbf {x} _ {0}) \right| = \left| \operatorname{grad} f (\mathbf {x} _ {0}) \cdot (\mathbf {x} - \mathbf {x} _ {0}) + o (| \mathbf {x} - \mathbf {x} _ {0} |) \right| \\ \leq \sum_ {i = 1} ^ {n} \left| \frac {\partial f}{\partial x _ {i}} (\mathbf {x} _ {0}) \right| | \Delta x _ {i} | + o (| \mathbf {x} - \mathbf {x} _ {0} |). \\ \end{array}
$$

Sind für die einzelnen Messungen Fehlerschranken  $|\Delta x_{i}| \leq s_{i}$  bekannt, so erhält man eine ungefähre Fehlerschranke S für die Funktionswerte ( $|\Delta f(\mathbf{x})| \leq S$ )

$$
S \approx \sum_ {i = 1} ^ {n} \left| \frac {\partial f}{\partial x _ {i}} (\mathbf {x} _ {0}) \right| s _ {i}.
$$

Beispiel. Für den Elastizitätsmodul E eines Stabes mit quadratischem Querschnitt gilt beim skizzierten Versuchsaufbau

$$
E = 4 F l ^ {3} h ^ {- 1} a ^ {- 4}.
$$

![](../../raw/pages_0385-0416/images/page_397_image_8.jpg)

<details>
<summary>text_image</summary>

a
l
h
F
</details>

Abb. 171 - Biegung

Mißt man $l = 50\text{cm}$ (auf $1\%$), $a = 2\text{cm}$ (auf $1\%$), $h = 2\text{mm}$ (auf $3\%$) und $F = 130\text{N}$ (auf $0.5\%$ genau), so gibt die Fehlerrechnung (mit linearer Approximation)

$$
\begin{array}{l} \left| \frac {\Delta E}{E} \right| \approx \frac {1}{| E |} \left| E _ {F} \Delta F + E _ {l} \Delta l + E _ {h} \Delta h + E _ {a} \Delta a \right| \\ \leq | \frac {\Delta F}{F} | + 3 | \frac {\Delta l}{l} | + | - 1 | | \frac {\Delta h}{h} | + | - 4 | | \frac {\Delta a}{a} | \\ \approx 0. 1 0 5 \\ \end{array}
$$

Obiger Versuchsaufbau liefert E auf 10.5% genau, d.h.

$$
E = 2 0 3 1 2 5. 0 0 0 \pm 2 1 3 2 8. 0 0 0 \frac {\mathrm{N}}{\mathrm{mm} ^ {2}}.
$$

Direktes Auswerten von E durch Eintragen der Intervallgrenzen liefert bei den gegebenen Genauigkeiten und Maßeinheiten

$$
2 0 3 1 2 5. 0 0 0 - 2 0 1 5 9. 4 5 1 \leq E \leq 2 0 3 1 2 5. 0 0 0 + 2 2 6 0 0. 7 2 0.
$$

③ Newton-Verfahren zur näherungsweisen Lösung eines nichtlinearen Gleichungssystems im  $R^{2}$

$$
f (x, y) = 0, \quad g (x, y) = 0
$$

(mit $\mathcal{C}^1$-Funktionen $f, g$):

Mit einem Startwert (Näherungswert)  $(x_{0}, y_{0})$  ersetzt man mit (8) dieses System durch das lineare Gleichungssystem

$$
\begin{array}{l} f (x _ {0}, y _ {0}) + f _ {x} (x _ {0}, y _ {0}) (x - x _ {0}) + f _ {y} (x _ {0}, y _ {0}) (y - y _ {0}) = 0 \\ g (x _ {0}, y _ {0}) + g _ {x} (x _ {0}, y _ {0}) (x - x _ {0}) + g _ {y} (x _ {0}, y _ {0}) (y - y _ {0}) = 0, \\ \end{array}
$$

---

§2. Reellwertige Funktionen mehrerer reeller Variabler.

383

für das man im Fall

$$
\Delta := \det \left( \begin{array}{c c} f _ {x} (x _ {0}, y _ {0}) & f _ {y} (x _ {0}, y _ {0}) \\ g _ {x} (x _ {0}, y _ {0}) & g _ {y} (x _ {0}, y _ {0}) \end{array} \right) \neq 0
$$

mit der Cramerschen Regel (→ Kap. 6, 5.6) eine verbesserte Näherung

$$
\begin{array}{l} x _ {1} = x _ {0} + \frac {1}{\Delta} \det \left( \begin{array}{c c} - f (x _ {0}, y _ {0}) & f _ {y} (x _ {0}, y _ {0}) \\ - g (x _ {0}, y _ {0}) & g _ {y} (x _ {0}, y _ {0}) \end{array} \right) , \\ y _ {1} = y _ {0} + \frac {1}{\Delta} \det \left( \begin{array}{c c} f _ {x} (x _ {0}, y _ {0}) & - f (x _ {0}, y _ {0}) \\ g _ {x} (x _ {0}, y _ {0}) & - g (x _ {0}, y _ {0}) \end{array} \right) \\ \end{array}
$$

berechnet. Mit diesem Wert  $(x_{1}, y_{1})$  als Startwert kann das Verfahren wiederholt werden.

Beispiel 1. Zur Darstellung der Zahnflanken von Stirnradgetrieben verwendet man die Kreisevolvente γ

$$
\mathbf {x} (t) = \binom{r \sin t - r t \cos t}{r \cos t + r t \sin t - r}
$$

(d.i. die Ortskurve des Endpunktes eines Fadens, der von einem Kreis abgewickelt wird).

Soll γ die Punkte (0,0) und (a,b) verbinden, so führt dies auf zwei nicht-lineare Gleichungen für r und t :

$$
f (r, t) := r \sin t - r t \cos t - a = 0
$$

$$
g (r, t) := r \cos t + r t \sin t - r - b = 0.
$$

![](../../raw/pages_0385-0416/images/page_398_image_13.jpg)

<details>
<summary>text_image</summary>

y
(a,b)
x(t)
x
t
(0,-r)
</details>

Abb. 172 - Zahnflanke

Lineare Approximation von $f$ und $g$ im Punkt $(r_0, t_0)$ liefert das lineare Gleichungssystem

$$
\left( \begin{array}{c c} \sin t _ {0} - t _ {0} \cos t _ {0} & r _ {0} t _ {0} \sin t _ {0} \\ \cos t _ {0} + t _ {0} \sin t _ {0} - 1 & r _ {0} t _ {0} \cos t _ {0} \end{array} \right) \binom{r - r _ {0}}{t - t _ {0}} + \binom{f (r _ {0}, t _ {0})}{g (r _ {0}, t _ {0})} = 0.
$$

Hierbei ist die Determinante $\Delta = r_0 t_0 (\sin t_0 - t_0)$ stets $\neq 0$, sofern nur $r_0 t_0 \neq 0$. Die Lösung $(r_1, t_1)$ liefert eine verbesserte Näherung

$$
\binom{r _ {1}}{t _ {1}} = \binom{r _ {0}}{t _ {0}} - \frac {1}{\Delta} \left( \begin{array}{c c} r _ {0} t _ {0} \cos t _ {0} & - r _ {0} t _ {0} \sin t _ {0} \\ 1 - \cos t _ {0} - t _ {0} \sin t _ {0} & \sin t _ {0} - t _ {0} \cos t _ {0} \end{array} \right) \binom{f (r _ {0}, t _ {0})}{g (r _ {0}, t _ {0})}.
$$

Für  $(a,b)=(1,1)$  und die Startwerte  $(r_{0},t_{0})=(2,1.2)$  liefert ein kleines Rechnerprogramm folgende rasch konvergierenden Näherungswerte:

$$
\begin{array}{l} r _ {0} = 2 \quad t _ {0} = 1. 2 \\ r _ {1} = 2. 1 2 5 9 8 6 6 6 9 5 \quad t _ {1} = 1. 1 7 4 4 9 0 8 0 2 6 \\ r _ {2} = 2. 1 2 8 9 1 3 0 1 2 7 \quad t _ {2} = 1. 1 7 5 0 4 3 8 9 0 3 \\ r _ {3} = 2. 1 2 8 9 1 4 5 2 3 9 \quad t _ {3} = 1. 1 7 5 0 4 2 6 2 8 9 \\ \end{array}
$$

---

384

7. Funktionen in mehreren Variablen. Teil 1: Differentiation

Man beachte, daß dieses Verfahren keine eindeutige Lösung liefert: Mit dem Startwert  $(r_{0}, t_{0}) = (1, 8)$  liefert obiges Programm nach 5 Schritten die Näherung

$$
r = 0. 1 8 2 2 3, \quad t = 8. 4 3 8 1,
$$

die für die technische Aufgabenstellung nicht brauchbar ist. □

![](../../raw/pages_0385-0416/images/page_399_image_5.jpg)

<details>
<summary>text_image</summary>

Mathematical diagram showing a spiral curve in Cartesian coordinates with a shaded region and a point on the curve.
</details>

Abb. 173 - Kreisevolvente

Beispiel 2. Bairstow-Verfahren zur näherungsweisen Berechnung aller komplexen Nullstellen eines reellen Polynoms

$$
p (x) = a _ {0} x ^ {n} + a _ {1} x ^ {n - 1} + \dots + a _ {n} \quad \left(a _ {i} \in \mathbb {R}, a _ {0} \neq 0\right).
$$

Ein quadratisches Polynom $q(x) = x^{2} - ux - v$ ist genau dann ein Teiler von $p(x)$, wenn in der Zerlegung ($\rightarrow$ Kap. 2, 2.5 (7))

$$
p (x) = (x ^ {2} - u x - v) h (x) + (a x + b)
$$

die Koeffizienten $a, b$ des Restes verschwinden, d.h. wenn $u, v$ Lösungen sind von

$$
a = a (u, v) = 0, \quad b = b (u, v) = 0.
$$

Dieses Gleichungssystem, das für $n \geq 2$ stets eine Lösung in $\mathbb{R}^2$ besitzt ($\rightarrow$ Kap. 2, Satz 2.10), wird mit dem zweidimensionalen Newton-Verfahren näherungsweise gelöst. Die Berechnung von $a(u,v)$ und $b(u,v)$ erfolgt mit dem Horner-Schema ($\rightarrow$ Kap. 2, §2). Ist eine Näherungslösung $\tilde{u},\tilde{v}$ gefunden, so gibt die quadratische Gleichung $x^2 - \tilde{u} x - \tilde{v} = 0$ zwei Nullstellen von $p(x)$. Da das Horner-Schema gleichzeitig die Koeffizienten von $h(x)$ liefert, kann der Algorithmus sofort an $h(x)$ wiederholt werden.

Die Wahl von günstigen Startwerten  $u_{0}, v_{0}$  ist i.a. schwierig, daher muß mitunter mehrfach mit unterschiedlichen  $u_{0}, v_{0}$  begonnen werden.

```txt
' Programm BAIRSTOW
' ---------------------------------------------------      Repeat
Input "Polynomgrad=";N          Bk=0
Eps=1.OE-07              Bk_1=0
Steps=30                  Ck=0
M=N                     Ck_1=0
Dim B(N),C(N)                 For K=0 To M-1
For I=0 To N                    Ck_2=Ck_1
    Print "a"+Str$(I)           Ck_1=Ck
    Input B(I)                   Bk_2=Bk_1
Next I                           Bk_1=Bk
While M>2                        Bk=B(K)+U*Bk_1+V*Bk_2
    Start:                             C(K)=Bk
    Input "Startwerte UO= ,VO= ";U;V   Next K
S=0
```

---

§2. Reellwertige Funktionen mehrerer reeller Veränderlicher.

385

```txt
Bk_2=Bk_1
    Bk_1=Bk
    Bk=B(M)+U*Bk_1+V*Bk_2
    C(M)=Bk
    Det=Ck_1*Ck_1-Ck_2*Ck
    If Det=0 Then
        Print "Neue Startwerte!"
        Goto Start
    Endif
    U=U+(Bk*Ck_2-Bk_1*Ck_1)/Det
    V=V+(Bk_1*Ck-Bk*Ck_1)/Det
    S=S+1
    If S=Steps Then
        Print "Neue Startwerte!"
        Goto Start
    Endif
Until Abs(Bk_1)+Abs(Bk)<Eps
Gosub Quadr_gleichg
M=M-2
For K=0 To M
    B(K)=C(K)
Next K
Wend
If M=1 Then
    Print "rccllc Wurzel:";-B(1)/B(0)
Else
    U=-B(1)/B(0)
    V=-B(2)/B(0)
    Gosub Quadr_gleichg
Endif
End
```

![](../../raw/pages_0385-0416/images/page_400_image_3.jpg)

2.6 Die Richtungsableitung, der Anstieg und die Kettenregel. Die partiellen Ableitungen  $\frac{\partial f}{\partial x_{i}}(\mathbf{x})$  geben gemäß (1) die „momentane“ Änderung der Funktionswerte in Richtung der Koordinatenachsen (d.h. in  $e_{i}$ -Richtung) an. Es wäre unvernünftig, sich auf diese Richtungen zu beschränken.

Zu jedem Vektor $\mathbf{v} \in \mathbb{R}^{n}$, $\mathbf{v} \neq 0$, nennen wir den Grenzwert

$$
\hat {c} _ {\mathbf {v}} f (\mathbf {x}) := \lim _ {t \to 0} \frac {1}{t} [ f (\mathbf {x} + t \mathbf {v}) - f (\mathbf {x}) ] \tag {9}
$$

(sofern er existiert) die Ableitung von $f$ an der Stelle $\mathbf{x}$ längs $\mathbf{v}$. Ist $\mathbf{v}$ ein Einheitsvektor ($|\mathbf{v}| = 1$), dann heißt $\partial_{\mathbf{v}}f(\mathbf{x})$ die Richtungsableitung (oder Anstieg) von $f$ an der Stelle $\mathbf{x}$ in Richtung $\mathbf{v}$.

---

386

7. Funktionen in mehreren Variablen. Teil 1: Differentiation

Bemerkung. Für  $\partial_{\mathbf{v}}f(\mathbf{x})$  sind die Bezeichnungen  $\frac{\partial f}{\partial\mathbf{v}}(\mathbf{x})$  oder  $D_{\mathbf{v}}f(\mathbf{x})$  ebenfalls weit verbreitet.

Betrachtet man die Einschränkung von $f$ längs der Geraden $\mathbf{x}+tv$ (in Richtung $\mathbf{v}$), also $h(t):=f(\mathbf{x}+tv)$, dann gilt $\dot{h}(0)=\partial_{\mathbf{v}}f(\mathbf{x})$ und deshalb

$$
\partial_ {\mathbf {v}} f (\mathbf {x}) > 0 \Rightarrow f (\mathbf {x}) \text { nimmt in Richtung } \mathbf {v} \text { zu },
$$

$$
\partial_ {\mathbf {v}} f (\mathbf {x}) <   0 \Rightarrow f (\mathbf {x}) \text {nimmt in Richtung v ab.}
$$

Eine anschauliche Deutung für $n = 2$:

Die Schnittkurve des Graphen $z = f(x, y)$ mit der zur $z$-Achse parallelen Ebene durch die Gerade

$$
\binom{x _ {0}}{y _ {0}} + t \binom{v _ {1}}{v _ {2}}, \mathbf {v} = \binom{v _ {1}}{v _ {2}}, | \mathbf {v} | = 1,
$$

besitzt die Parameterdarstellung

$$
\mathbf {x} (t) = \left( \begin{array}{c} x _ {0} + t v _ {1} \\ y _ {0} + t v _ {2} \\ f (x _ {0} + t v _ {1}, y _ {0} + t v _ {2}) \end{array} \right)
$$

mit dem Tangentialvektor

$$
\dot {\mathbf {x}} (t) = \left( \begin{array}{c} v _ {1} \\ v _ {2} \\ \hat {c}, f (x _ {0}, y _ {0}) \end{array} \right)
$$

![](../../raw/pages_0385-0416/images/page_401_image_13.jpg)

<details>
<summary>text_image</summary>

z = f(x,y)
grad f
y
φ
(x₀,y₀)
v, |v|=1
∂_v f(x₀,y₀) = tan φ
x
</details>

Abb. 174 - Richtungsableitung

im Kurvenpunkt  $(x_{0},y_{0},f(x_{0},y_{0}))$ . Die Tangente hat in der Tat den Anstieg  $\hat{c}_{\nu}f(x_{0},y_{0})$ . ☐

Eine physikalische Deutung für $n=2$: Ein Massenpunkt überquert eine ebene Platte mit konstanter Geschwindigkeit $\mathbf{v}=(v_{1},v_{2})^{T}$ (nicht notwendig $|\mathbf{v}|=1$). Herrscht auf der Platte die Temperaturverteilung $T=f(x,y)$, so gilt für die momentane Temperaturänderung des Punktes in $(x_{0},y_{0})$

$$
\lim _ {t \to 0} \frac {1}{t} \left[ f (x _ {0} + t v _ {1}, y _ {0} + t v _ {2}) - f (x _ {0}, y _ {0}) \right] = \partial_ {\mathbf {v}} f (x _ {0}, y _ {0}).
$$

Aus den Sätzen 2.3 und 2.4 folgt:

Satz 2.5. Für jede auf der offenen Menge $D \subseteq \mathbb{R}^n$ total differenzierbare Funktion $f$ (insbesondere für $f \in \mathcal{C}^1(D, \mathbb{R})$) und für jeden Vektor $\mathbf{v} \in \mathbb{R}^n$, $\mathbf{v} \neq 0$, gilt

$$
\partial_ {\mathbf {v}} f (\mathbf {x}) = \operatorname{grad} f (\mathbf {x}) \cdot \mathbf {v} = \sum_ {i = 1} ^ {n} f _ {x _ {i}} (\mathbf {x}) v _ {i}.\tag {10}
$$

Mit $|\mathbf{v}| = 1$ stellt (10) die Richtungsableitung (bzw. den Anstieg) von $f$ an der Stelle $\mathbf{x}$ in Richtung $\mathbf{v}$ dar.

---

§2. Reellwertige Funktionen mehrerer reeller Veränderlicher.

387

Beispiele. 1. Der Anstieg der Funktion $f(x,y)=x^{2}+y^{2}$ im Punkt (1,1) in Richtung des (Einheits-) Vektors $\mathbf{v}=(\sin\alpha,\cos\alpha)^{T}$ beträgt

$$
\hat {c} _ {\mathbf {v}} f (\mathbf {x}) = \operatorname{grad} f (1, 1) \cdot \binom{\cos \alpha}{\sin \alpha} = (2, 2) \binom{\cos \alpha}{\sin \alpha} = 2 (\cos \alpha + \sin \alpha).
$$

2. Der mit der Geschwindigkeit $\mathbf{v} = (2,4,7)^{T}$ (Einheiten vernachlässigt) einen Raum mit der Temperaturverteilung $T = f(x,y,z) = 2xy + 4yz$ durchquerende Massenpunkt erfährt im Punkt (1,1,1) die momentane Temperaturänderung

$$
\hat {c} _ {\mathbf {v}} f (1, 1, 1) = \operatorname{grad} f (1, 1, 1) \cdot \left( \begin{array}{c} 2 \\ 4 \\ 7 \end{array} \right) = \left( \begin{array}{c} 2 \\ 6 \\ 4 \end{array} \right) \left( \begin{array}{c} 2 \\ 4 \\ 7 \end{array} \right) = 5 6.
$$

3. Für die durch  $A = A^{T} \in R^{n \times n}$  bestimmte quadratische Form q gilt:

$$
\boxed { \begin{array}{r l} q (\mathbf {x}) & = \mathbf {x} ^ {T} A \mathbf {x}, \\ \hat {c} _ {\mathbf {v}} q (\mathbf {x}) & = 2 (A \mathbf {x}) \cdot \mathbf {v}, \\ \operatorname{grad} q (\mathbf {x}) & = 2 A \mathbf {x}. \end{array} } \tag {11}
$$

Beweis.

$$
\begin{array}{l} \hat {c} _ {\mathbf {v}} q (\mathbf {x}) = \lim _ {t \to 0} \frac {1}{t} [ q (\mathbf {x} + t \mathbf {v}) - q (\mathbf {x}) ] \\ = \lim _ {t \to 0} (\mathbf {v} ^ {T} A \mathbf {x} + \mathbf {x} ^ {T} A \mathbf {v} + t \mathbf {v} ^ {T} A \mathbf {v}) = 2 (A \mathbf {x}) \cdot \mathbf {v}. \\ \end{array}
$$

Die physikalische Deutung der Ableitung längs v legt es nahe, das Änderungsverhalten der Funktion f längs einer im Definitionsbereich verlaufenden Kurve (Bahn eines bewegten Punktes) zu untersuchen.

Satz 2.6. Die Kettenregel. Für jede $\mathcal{C}^{1}$-Funktion $f: D \to \mathbb{R}$. $D \subseteq \mathbb{R}^{n}$ offen, und für jedes Kurvenstück $\mathbf{x}: \mathbb{R} \supseteq [a, b] \to D$ gilt

$$
\begin{array}{r l} \frac {d}{d t} f (\mathbf {x} (t)) & = \frac {d}{d t} f \left(x _ {1} (t), x _ {2} (t), \dots , x _ {n} (t)\right) \\ & = f _ {x _ {1}} (\mathbf {x} (t)) \dot {x} _ {1} (t) + \dots + f _ {x _ {n}} (\mathbf {x} (t)) \dot {x} _ {n} (t) = \operatorname{grad} f (\mathbf {x} (t)) \cdot \dot {\mathbf {x}} (t). \end{array} \tag {12}
$$

Beweis. Aus der linearen Approximation (7) in einem Kurvenpunkt $\mathbf{x}(t)$ nahe $\mathbf{x}_{0} := \mathbf{x}(t_{0})$, $f(\mathbf{x}(t)) - f(\mathbf{x}_{0}) = \text{grad } f(\mathbf{x}_{0}) \cdot (\mathbf{x}(t) - \mathbf{x}_{0}) + R(\mathbf{x}(t), \mathbf{x}_{0})$ mit dem Fehler $R(\mathbf{x}, \mathbf{x}_{0}) = o(|\mathbf{x} - \mathbf{x}_{0}|)$, ergibt sich nach Division durch $t - t_{0}$ und Grenzübergang $t \to t_{0}$ die Behauptung; denn es gilt

$$
\lim _ {t \to t _ {0}} \frac {R (\mathbf {x} (t) , \mathbf {x} _ {0})}{t - t _ {0}} = \lim _ {t \to t _ {0}} \frac {| \mathbf {x} (t) - \mathbf {x} _ {0} |}{t - t _ {0}} \cdot \frac {R (\mathbf {x} (t) , \mathbf {x} _ {0})}{| \mathbf {x} (t) - \mathbf {x} _ {0} |} = 0.
$$

Die Kettenregel benötigt man immer dann, wenn neue Variable eingeführt werden und die partiellen Ableitungen in bezug auf diese Veränderlichen zu berechnen sind.

---

388

7. Funktionen in mehreren Variablen. Teil 1: Differentiation

Beispiel 1. Polarkoordinaten im $\mathbb{R}^{2}$. Durch $x = r\cos\varphi$, $y = r\sin\varphi$ wird die Funktion $f(x,y)$, $(x,y) \in D \subseteq \mathbb{R}^{2}$, transformiert in

$$
F (r, \varphi) := f (r \cos \varphi , r \sin \varphi).
$$

Für die partiellen Ableitungen von $F$ ergibt sich aus der Kettenregel (falls $f \in \mathcal{C}^2(D)$)

$$
\begin{array}{l} F _ {r} = f _ {x} \cos \varphi + f _ {y} \sin \varphi , \\ F _ {\varphi} = f _ {x} (- r \sin \varphi) + f _ {y} (r \cos \varphi), \\ F _ {r r} = f _ {x x} \cos^ {2} \varphi + 2 f _ {x y} \cos \varphi \sin \varphi + f _ {y y} \sin^ {2} \varphi , \\ F _ {r \varphi} = f _ {x x} (- r \sin \varphi \cos \varphi) + f _ {x y} r (\cos^ {2} \varphi - \sin^ {2} \varphi) + f _ {y y} (r \sin \varphi \cos \varphi) \\ - f _ {x} \sin \varphi + f _ {y} \cos \varphi , \\ F _ {\varphi \varphi} = f _ {x x} (r ^ {2} \sin^ {2} \varphi) + 2 f _ {x y} (- r ^ {2} \cos \varphi \sin \varphi) + f _ {y y} (r ^ {2} \cos^ {2} \varphi) - f _ {x} r \cos \varphi \\ - f _ {y} r \sin \varphi . \\ \end{array}
$$

Löst man diese Beziehungen nach den partiellen Ableitungen von $f$ auf, so erhält man für $r \neq 0$

$$
\boxed { \begin{array}{l} f _ {x} = F _ {r} \cos \varphi - \frac {1}{r} F _ {\varphi} \sin \varphi \\ f _ {y} = F _ {r} \sin \varphi + \frac {1}{r} F _ {\varphi} \cos \varphi \end{array} }
$$

und für den LAPLACE-Operator

$$
\Delta f := f _ {x x} + f _ {y y} = F _ {r r} + \frac {1}{r} F _ {r} + \frac {1}{r ^ {2}} F _ {\varphi \varphi}. \tag {13}
$$

## Beispiel 2. Kugelkoordinaten im $\mathbb{R}^{3}$. Durch

$$
x = r \cos \varphi \sin \theta , y = r \sin \varphi \sin \theta , z = r \cos \theta (0 \leq \varphi <   2 \pi , 0 \leq \theta \leq \pi)
$$

erhält man für die Funktion  $f(x, y, z)$

$$
F (r, \varphi , \theta) := f (r \cos \varphi \sin \theta , r \sin \varphi \sin \theta , r \cos \theta).
$$

Mehrfache Anwendung der Kettenregel und anschließendes Auflösen ergibt für den LAPLACE-Operator

$$
\begin{array}{r l} \Delta f & := f _ {x x} + f _ {y y} + f _ {z z} = \\ & = F _ {r r} + \frac {2}{r} F _ {r} + \frac {1}{r ^ {2} \sin^ {2} \theta} F _ {\varphi \varphi} + \frac {1}{r ^ {2}} F _ {\theta \theta} + \frac {1}{r ^ {2}} (\cot \theta) F _ {\theta}. \end{array} \tag {14}
$$

---

§2. Reellwertige Funktionen mehrerer reeller Veränderlicher.

389

## Aufgaben

1. Gegeben sind die Funktionen  $f : R^{2} \rightarrow R$

$$
f (x, y) = x ^ {2} - y ^ {2}, \quad f (x, y) = \sqrt {| x y |}, \quad f (x, y) = | x | + | y |.
$$

a) Zur Veranschaulichung im  $R^{3}$  bestimme und skizziere man

- die Niveaulinien $(f(x,y) = \mathrm{const})$
- die Graphen der Einschränkungen (x = const bzw. y = const
- den Graphen $z = f(x, y)$ im Schrägbild.

$$
\text {bzw.} y / x = \text {const})
$$

b) Soweit möglich berechne man grad f und  $\Delta f = \frac{\partial^{2}f}{\partial x^{2}} + \frac{\partial^{2}f}{\partial y^{2}}$  und skizziere einige Gradienten.

2. a) Berechne die ersten und zweiten partiellen Ableitungen von

$$
f = \ln \sqrt {x ^ {2} + y ^ {2}}: \quad f = \arctan \frac {y}{x}, x \neq 0.
$$

Welchen Wert hat jeweils  $f_{xx} + f_{yy}$ ?

b) Wie lautet jeweils die Gleichung der Tangentialebene im Punkt mit $x = 2$, $y = 1$?

c) Für die Funktion  $f(x,y) = \arctan \frac{y}{x}, x \neq 0$ , bestimme man

\- den Gradienten grad $f$ im Punkt (1,2),

\- die Richtungsableitung $d, f$ im Punkt (1,2) mit $\mathbf{v}$ in Richtung von $\begin{pmatrix} 1 \\ -1 \end{pmatrix}$.

\- $\frac{dz}{dt}$, wenn $z = f(t - \sin t, 1 - \cos t)$, $t \in \mathbb{R}$.

3. Die Funktion  $z = f(p, q)$  ist definiert als die größte reelle Wurzel von

$$
z ^ {2} + p z + q = 0.
$$

Wie lautet der Definitionsbereich von $f$; wie lauten die Höhenlinien $z = \text{const.}$ und die partiellen Ableitungen $\frac{\partial z}{\partial p}, \frac{\partial z}{\partial q}$?

4. Man berechne die ersten und zweiten partiellen Ableitungen der Funktion

$$
f (x, y, z) = x \cdot e ^ {x y / z}.
$$

5. Für  $f, g : R^{n} \rightarrow R$  rechne man nach:

$$
\mathrm{grad} (f \cdot g) = g \mathrm{grad} f + f \mathrm{grad} g,
$$

$$
\Delta (f \cdot g) = f \Delta g + 2 (\operatorname{grad} f) \cdot (\operatorname{grad} g) + g \Delta f.
$$

6. Gegeben ist die Funktion (Sinuskegel)

$$
f (x, y) = \left\{ \begin{array}{c l} \frac {x ^ {3} - 3 x y ^ {2}}{x ^ {2} + y ^ {2}} & , (x, y) \neq (0, 0) \\ 0 & , (x, y) = (0, 0) \end{array} \right.
$$

- Man berechne gradf für alle $(x,y)\in\mathbb{R}$.
- Sind $f_{x}$ und $f_{y}$ in $(0,0)$ stetig?
- Besitzt $f$ in $(0,0)$ eine Tangentialebene?

![](../../raw/pages_0385-0416/images/page_404_image_34.jpg)

<details>
<summary>text_image</summary>

z
y
x
</details>

---

390

7. Funktionen in mehreren Variablen. Teil 1: Differentiation

7. Die Funktion $U = f(x, y)$, $(x, y) \in \mathbb{R}^2$, hat in Polarkoordinaten $(r, \varphi)$ die Gestalt (Sinusparaboloid):

$$
U = F (r, \varphi) = f (r \cos \varphi , r \sin \varphi) = r ^ {2} \sin 4 \varphi .
$$

Man berechne:

$-F_{r}, F_{\varphi}, F_{rr}, F_{r\varphi}, F_{\varphi r}, F_{\varphi \varphi} \text{ für } r = 0,$
- $f_{x}, f_{y}$ ausgedrückt durch $F_{r}, F_{\varphi}$,
- grad $U$ in der Basis $(\mathbf{e}_r, \mathbf{e}_{\varphi})$, ($\rightarrow$ §1, Aufgabe 5),
- $f_{xx}(0,0)$, $f_{xy}(0,0)$, $f_{yx}(0,0)$, $f_{yy}(0,0)$.
Ist $f_{yx}(0,0) = f_{xy}(0,0)$ und ist
$F_{r\varphi}(0,\varphi) = F_{\varphi r}(0,\varphi)$?

![](../../raw/pages_0385-0416/images/page_405_image_10.jpg)

<details>
<summary>text_image</summary>

z
y
x
</details>

8. Die Funktion

$$
u (x, y, t) = \sin x \cos y \cos (x + y) \cos (x - y) \cos \omega t
$$

beschreibt für $t > 0$ die Transversalschwingung einer biegeweichen Membran in dem Quadrat $|x| + |y| \leq \frac{\pi}{2}$.

a) Man zeige: u löst die Schwingungsgleichung

$$
\frac {\partial^ {2} u}{\partial t ^ {2}} = c ^ {2} \Delta u = c ^ {2} \left(\frac {\partial^ {2} u}{\partial x ^ {2}} + \frac {\partial^ {2} u}{\partial y ^ {2}}\right) .
$$

In welchem Zusammenhang stehen c und ω?

b) In welchen Punkten ist zu allen Zeiten $t$ stets $u = 0$ (Knotenlinie)?

![](../../raw/pages_0385-0416/images/page_405_image_18.jpg)

<details>
<summary>text_image</summary>

Diagram showing a wavy surface with coordinate axes labeled x, y, u and directional arrows indicating flow or field direction.
</details>

9. Die Schnittkurve K der beiden Flächen

$$
\begin{array}{l} z = f (x, y) = 2 x ^ {3} y - x ^ {2} y ^ {3} \\ z = g (x, y) = 3 x y ^ {3} + x ^ {3} y ^ {2} - 5 \\ \end{array}
$$

durchstößt die x, y-Ebene in der Nähe des Punktes  $(x_{0}, y_{0}) = (1, 1)$ . Zur Verbesserung dieses Wertes bestimme man:

a) die Tangentialebene von  $z = f(x, y)$  in  $(x_{0}, y_{0})$ ;
b) die Tangentialebene von  $z = g(x, y)$  in  $(x_{0}, y_{0})$ ;
c) den Schnittpunkt  $(x_{1},y_{1})$  der Schnittgeraden dieser beiden Ebenen mit der Ebene z = 0 ;
d) die Werte $f(x_1, y_1)$ und $g(x_1, y_1)$.

10. Man zeige: Die Funktion  $f : R^{2} \rightarrow R$

$$
f (x, y) = \left\{ \begin{array}{c l} e ^ {- y ^ {2} / x} & , x \neq 0 \\ 1 & , x = 0 \end{array} \right.
$$

ist eingeschränkt auf die Geraden $y = mx$, $m \in \mathbb{R}$, stetig.

Ist $f$ über $\mathbb{R}^2$ stetig? Man skizziere einige Niveaulinien von $f$.

---

§3. Anwendungen der Differentiation

391

## §3. Anwendungen der Differentiation

## 3.1 Die Bedeutung des Gradienten.

① Richtung des stärksten Anstiegs. Für eine $\mathcal{C}^{1}$-Funktion $f: \mathbb{R}^{n} \supseteq D \to \mathbb{R}$ ist der Anstieg im Punkt $\mathbf{x} \in D$ in Richtung eines Vektors $\mathbf{v} \in \mathbb{R}^{n}$, $|\mathbf{v}| = 1$, gegeben durch $\partial_{\mathbf{v}} f(\mathbf{x}) = \text{grad } f(\mathbf{x}) \cdot \mathbf{v} = |\text{grad } f(\mathbf{x})| \cos \alpha$, wobei $\alpha$ den Winkel zwischen $\text{grad } f(\mathbf{x})$ und $\mathbf{v}$ bezeichnet ($\rightarrow \S(10)$ und Kap. 1, §5). Dieser Anstieg ist am größten für $\cos \alpha = 1$, d.h. für $\alpha = 0$. Also gilt für $\text{grad } f(\mathbf{x}) \neq \mathbf{0}$:

Richtung von grad  $f(\mathbf{x})=$

= Richtung des maximalen Anstiegs der Funktion f in x
= Richtung mit größtem Zuwachs von f in x.

Da $f$ genau dann ansteigt, wenn $-f$ abfällt, erhält man damit gleichzeitig die Richtung des stärksten Abnehmens („Abfalls“) der

Funktionswerte, nämlich  $-\text{grad } f(\mathbf{x})$ .

Speziell ergibt sich für den Graphen einer $\mathscr{C}^{1}$-Funktion $f: \mathbb{R}^{2} \supseteq D \to \mathbb{R}$: Im Punkt $(x, y)$ erfolgt der steilste Anstieg der Fläche $z = f(x, y)$ in Richtung von $\text{grad } f(x, y)$. Die Ebene senkrecht zur $(x, y)$-Ebene durch den Flächenpunkt $(x, y, f(x, y))$ längs $\text{grad } f(x, y)$ schneidet den Graphen in der „Fallinie“.

![](../../raw/pages_0385-0416/images/page_406_image_12.jpg)

<details>
<summary>text_image</summary>

z
z = f(x,y)
(x,y,z)
f_x
f_y
-1
y
D ∃ (x,y)
grad f(x,y)
</details>

Abb. 175 - grad $f(x, y)$

Anwendungen. 1. Die elektrische Feldstärke $\mathbf{E}(\mathbf{x})$ im Punkt $\mathbf{x} \in D \subseteq \mathbb{R}^3$ hat die Richtung des stärksten Spannungsabfalls in einem elektrostatischen Spannungsfeld $U(\mathbf{x})$, da $\mathbf{E}(\mathbf{x}) = -\text{grad } U(\mathbf{x})$ ($\rightarrow$ Kap. 8, 2.5).

Beispiel. Das Potential einer Punktladung in $O$ ist $U(\mathbf{x}) = \frac{c}{|\mathbf{x}|}$, $\mathbf{x} \neq \mathbf{0}$, $c \in \mathbb{R}$, mit der Feldstärke $\mathbf{E}(\mathbf{x}) = -c \operatorname{grad} \frac{1}{|\mathbf{x}|} = \frac{c}{|\mathbf{x}|^3} \mathbf{x}$.

2. Das Gradientenverfahren zur Bestimmung von Maximum (oder Minimum) einer Funktion $f$. Ausgehend von einem Startwert $\mathbf{x}_0$ bestimmt man in Richtung von $\operatorname{grad} f(\mathbf{x}_0)$ (bzw. $-\operatorname{grad} f(\mathbf{x}_0)$) einen Punkt

$$
\mathbf {x} _ {1} = \mathbf {x} _ {0} + h \operatorname{grad} f (\mathbf {x} _ {0})
$$

mit einer dem Problem angepaßten Schrittweite h > 0 (h < 0).

Im Falle $f(\mathbf{x}_1) < f(\mathbf{x}_0)$ (bzw. $f(\mathbf{x}_1) > f(\mathbf{x}_0)$) ist man zu weit gegangen, man versucht es deshalb noch einmal mit halber Schrittweite: $\mathbf{x}_1 = \mathbf{x}_0 + \frac{h}{2} \operatorname{grad} f(\mathbf{x}_0)$.

---

392

7. Funktionen in mehreren Variablen. Teil 1: Differentiation

Ist $f(\mathbf{x}_1) > f(\mathbf{x}_0)$ (bzw. $f(\mathbf{x}_1) < f(\mathbf{x}_0)$), so nimmt man $\mathbf{x}_1$ als neuen Startwert und wiederholt das Verfahren. Auf diese Weise nähert man sich auf einem Streckenzug in $D$ einer Maximal- (bzw. Minimal-) Stelle der Funktion. Diese Stelle hängt vom gewählten Startwert ab und bestimmt nicht notwendig das globale Maximum (bzw. Minimum) von $f$ auf $D$ ($\rightarrow 3.4$).

Beispiel. Bei der Struktursynthese ebener Kurbelgetriebe stellt sich die Aufgabe, aus N Meßpunkten  $(x_{i}, y_{i})$  in der Ebene eine Kreisbahn zu rekonstruieren. Da die Punkte für N > 3 im allgemeinen nicht auf einem Kreis liegen, bestimmt man die Mittelpunktskoordinaten x, y und den Radius r als Minimalstelle der Fehlerquadratfunktion

![](../../raw/pages_0385-0416/images/page_407_image_4.jpg)

<details>
<summary>text_image</summary>

grad f(x₀)
f(x) = 1
x₀
x₁
x₂
Minimum
h < 0
f(x) = 0.5
</details>

Abb. 176 - Gradientenverfahren

![](../../raw/pages_0385-0416/images/page_407_image_6.jpg)

<details>
<summary>natural_image</summary>

Simple circular diagram with six marked points (no text or symbols)
</details>

Abb. 177 - Interpolation mit Kreis

$$
F (x, y, r) = \sum_ {i = 1} ^ {N} \left(\sqrt {(x _ {i} - x) ^ {2} + (y _ {i} - y) ^ {2}} - r\right) ^ {2}.
$$

Wählt man die Startwerte über einen Kreis, der durch drei der N Punkte  $(x_{i}, y_{i})$  geht, so liefert das Gradientenverfahren für das skizzierte Beispiel nach wenigen Schritten eine brauchbare „Lösung“. Zur Programmierung der Schrittweitenhalbierung und des Abbruchkriteriums ( $\rightarrow$  Programm NLSQ in 3.5). ☐

② Tangenten und Tangentialebene.

Sei $D \subseteq \mathbb{R}^n$ offen und $f : D \to \mathbb{R}$ eine $\mathcal{C}^1$-Funktion, dann definiert $f(\mathbf{x}) = c$ ($c \in \mathbb{R}$ konstant) eine Hyperfläche in $D$. Für jede parametrisierte Kurve $t \mapsto \mathbf{x}(t)$ auf dieser Hyperfläche gilt $f(\mathbf{x}(t)) = c \quad (t \in I)$, und mit der Kettenregel (12) von §2 folgt

$$
\mathrm{grad} f (\mathbf {x} (t)) \cdot \dot {\mathbf {x}} (t) = 0 . \tag {1}
$$

Diese Formel werten wir nun getrennt für n = 2 und n = 3 aus.

n = 2 : In jedem Punkt $(x_0, y_0)$ der Niveaukurve $f(x, y) = c$ ist grad $f(x_0, y_0)$ orthogonal zur Kurventangente. Man sagt auch,

grad  $f(x_{0}, y_{0})$  ist im Kurvenpunkt  $(x_{0}, y_{0})$  orthogonal zur Niveaukurve  $f(x, y) = c$ .

Diese Feststellung liefert für den Fall  $\text{grad } f(x_{0}, y_{0}) \neq 0$  sofort die

---

§3. Anwendungen der Differentiation

393

Normalengleichung der Tangente an die Niveaukurve $f(x,y) = c$ im Kurvenpunkt $(x_0,y_0)$:

$$
f _ {x} (x _ {0}, y _ {0}) (x - x _ {0}) + f _ {y} (x _ {0}, y _ {0}) (y - y _ {0}) = 0.
$$

Speziell ergibt dieses für den Graph $y = f(x)$ einer Funktion in einer Veränderlichen, implizit dargestellt durch $F(x,y) = y - f(x) = 0$, die Gleichung der Kurventangente grad $F(x_0,y_0) \cdot \begin{pmatrix} x - x_0 \\ y - y_0 \end{pmatrix} = 0$, also $y - y_0 - f'(x_0)(x - x_0) = 0$.

n = 3 : In jedem Punkt  $\mathbf{x}_{0} = (x_{0}, y_{0}, z_{0})$  der durch  $f(\mathbf{x}) = f(x, y, z) = c$  implizit

dargestellten Fläche ist grad  $f(\mathbf{x}_{0})$  orthogonal zu den Tangenten sämtlicher parametrisierten Flächenkurven durch diesen Punkt. Kurz: grad  $f(\mathbf{x}_{0})$  ist orthogonal zu allen Tangenten an die Fläche im Punkt  $x_{0}$ , bzw.

grad $f(\mathbf{x})$ ist in jedem Flächenpunkt orthogonal zur Niveaufläche $f(\mathbf{x}) = c$.

Die Ebene, die von den Tangenten an die Fläche in einem Flächenpunkt aufgespannt wird, heißt Tangentialebene.

![](../../raw/pages_0385-0416/images/page_408_image_9.jpg)

<details>
<summary>text_image</summary>

f(x) = c
grad f(x₀)
</details>

Abb. 178 - Tangentialebene

Ist $\operatorname{grad} f(\mathbf{x}_0) \neq \mathbf{0}$, so ist $\operatorname{grad} f(\mathbf{x}_0) \cdot (\mathbf{x} - \mathbf{x}_0) = 0$ eine Normalengleichung, d.h. explizit

Normalengleichung der Tangentialebene an die Niveaufläche
$f(x,y,z) = c$ im Flächenpunkt $(x_0, y_0, z_0)$:

$$
f _ {x} (x _ {0}, y _ {0}, z _ {0}) (x - x _ {0}) + f _ {y} (x _ {0}, y _ {0}, z _ {0}) (y - y _ {0}) + f _ {z} (x _ {0}, y _ {0}, z _ {0}) (z - z _ {0}) = 0.
$$

Speziell ergibt sich für den Graph einer $\mathcal{C}^{1}$-Funktion $z = f(x, y)$, dargestellt als Niveaufläche $F(x, y, z) = z - f(x, y) = 0$, die (bekannte, $\rightarrow$ 2.4) Gleichung der

Tangentialebene $\operatorname{grad} F(x_0, y_0, z_0) \cdot \begin{pmatrix} x - x_0 \\ y - y_0 \\ z - z_0 \end{pmatrix} = 0$, also

$$
z - z _ {0} = f _ {x} (x _ {0}, y _ {0}) (x - x _ {0}) + f _ {y} (x _ {0}, y _ {0}) (y - y _ {0}).
$$

Beispiele 1. Die Kreistangente im Punkt  $(x_{0}, y_{0})$  an  $(x - u)^{2} + (y - v)^{2} = r^{2}$  hat die Gleichung  $2(x_{0} - u)(x - x_{0}) + 2(y_{0} - v)(y - y_{0}) = 0$ . Dieses kann mit der Kreisgleichung leicht umgeformt werden zur bekannten Formel

$$
(x _ {0} - u) (x - u) + (y _ {0} - v) (y - v) = r ^ {2}.
$$

2. Das Paraboloid

$$
\frac {x ^ {2}}{a ^ {2}} + \frac {y ^ {2}}{b ^ {2}} - 2 p z = 0 \quad (p \neq 0)
$$

---

394

7. Funktionen in mehreren Variablen. Teil 1: Differentiation

besitzt im Flächenpunkt  $(x_{0}, y_{0}, z_{0})$  die Tangentialebene

$$
\frac {x _ {0} (x - x _ {0})}{a ^ {2}} + \frac {y _ {0} (y - y _ {0})}{b ^ {2}} - p (z - z _ {0}) = 0.
$$

Eine leichte Umformung erbringt

$$
\frac {x _ {0} x}{a ^ {2}} + \frac {y _ {0} y}{b ^ {2}} - p (z + z _ {0}) = 0.
$$

3.2 Approximation höherer Ordnung; die TAYLOR-Formel. Wir verallgemeinern die TAYLOR-Formel für Funktionen einer Veränderlichen (→ Kap. 5, §4) auf $\mathcal{C}^{k}$-Funktionen $f: \mathbb{R}^{n} \supseteq D \to \mathbb{R}$ in $n \geq 1$ Veränderlichen. Dazu betrachten wir für $\mathbf{x} \in D$ und $\mathbf{v} \in \mathbb{R}^{n}$ die Funktion $h(t) := f(\mathbf{x} + t\mathbf{v})$ ($0 \leq t \leq 1$) der einen reellen Variablen $t$, vorausgesetzt, die ganze $\mathbf{x}$ mit $\mathbf{x} + \mathbf{v}$ verbindende Strecke liegt in $D$. Vereinfachend setzen wir deshalb voraus, daß $D$ ein konvexes Gebiet ist, d.h.

1. D ist offen,
2. $\mathbf{x},\mathbf{y}\in D\Rightarrow \mathbf{x} + t(\mathbf{y} - \mathbf{x})\in D$ für alle $t\in [0,1]$.

![](../../raw/pages_0385-0416/images/page_409_image_10.jpg)

<details>
<summary>text_image</summary>

D
x
x+v
</details>

Abb. 179a - Konvexes Gebiet

![](../../raw/pages_0385-0416/images/page_409_image_12.jpg)

Abb. 179b - Kein konvexes Gebiet

Die Taylor-Formel für  $h(t)$  an der Stelle t = 0 lautet

$$
h (1) = h (0) + \dot {h} (0) + \frac {1}{2 !} \ddot {h} (0) + \dots + \frac {1}{k !} h ^ {(k)} (0) + \frac {1}{(k + 1) !} h ^ {(k + 1)} (\xi_ {k}) \tag {4}
$$

mit einer Zahl $\xi_{k}$ zwischen 0 und 1 ($\rightarrow$ Kap. 5, §4(1)). Die Ableitungen $h^{(l)}(t)$, bzw. $h^{(l)}(0)$, berechnen wir mit der Kettenregel. Sie lassen sich mit dem Differentialoperator

$$
\partial_ {\mathbf {v}} = v _ {1} \frac {\partial}{\partial x _ {1}} + \dots + v _ {n} \frac {\partial}{x _ {n}}
$$

übersichtlich darstellen, wobei zu beachten ist, daß

$$
\partial_ {\mathbf {v}}: \mathscr {C} ^ {l} (D, \mathbb {R}) \to \mathscr {C} ^ {l - 1} (D, \mathbb {R}), \quad f (\mathbf {x}) \mapsto \partial_ {\mathbf {v}} f (\mathbf {x}),
$$

(die Ableitung längs v) linear ist und  $\partial_{\mathbf{v}}^{l}f(\mathbf{x}) = \partial_{\mathbf{v}}(\ldots(\partial_{\mathbf{v}}f(x))\ldots)$  die l-malige Anwendung von  $\partial_{v}$  bedeutet. Man erhält

$$
\begin{array}{l} h (1) = f (\mathbf {x} + \mathbf {v}), \quad h (0) = f (\mathbf {x}), \\ \dot {h} (t) = \operatorname{grad} f (\mathbf {x} + t \mathbf {v}) \cdot \mathbf {v}, \quad \dot {h} (0) = \partial_ {\mathbf {v}} f (\mathbf {x}), \\ \ddot {h} (t) = \sum_ {i = 1} ^ {n} v _ {i} \left[ \operatorname{grad} f _ {x _ {i}} (\mathbf {x} + t \mathbf {v}) \cdot \mathbf {v} \right], \quad \ddot {h} (0) = \partial_ {\mathbf {v}} ^ {2} f (\mathbf {x}), \quad \text {etc.:} h ^ {(l)} (0) = \partial_ {\mathbf {v}} ^ {l} f (\mathbf {x}). \\ \end{array}
$$

Diese Werte in (4) eingetragen ergeben:

---

§3. Anwendungen der Differentiation

395

Satz 3.1. Die Taylor-Formel für $n$ Variable. Ist $D \subseteq \mathbb{R}^n$ ein konvexes Gebiet, $f \in \mathcal{C}^{k+1}(D, \mathbb{R})$, $\mathbf{x} \in D$, dann gilt mit $\mathbf{x} + \mathbf{v} \in D$ die Approximationsformel

$$
f (\mathbf {x} + \mathbf {v}) = f (\mathbf {x}) + \partial_ {\mathbf {v}} f (\mathbf {x}) + \frac {1}{2 !} \partial_ {\mathbf {v}} ^ {2} f (\mathbf {x}) + \dots + \frac {1}{k !} \partial_ {\mathbf {v}} ^ {k} f (\mathbf {x}) + R _ {k} (\mathbf {x}, \mathbf {v})
$$

$$
\begin{array}{l} m i t d e m R e s t g l i e d \quad R _ {k} (\mathbf {x}, \mathbf {v}) = \frac {1}{(k + 1) !} \hat {c} _ {\mathbf {v}} ^ {k + 1} f (\mathbf {x} + \xi_ {k} \mathbf {v}) \tag {5} \\ \text {mit einer Zahl} \xi_ {k} \text {zwischen 0 und 1} \quad (\partial_ {\mathbf {v}} = \sum_ {i = 1} ^ {n} v _ {i} \frac {\partial}{\partial x _ {i}}). \\ \end{array}
$$

Die Taylor-Formel dient zur Approximation von $f(\mathbf{x})$ in der Umgebung eines festen Punktes $\mathbf{x}_{0}\in D$ durch ein Polynom, das sog. Taylor-Polynom

$$
p (\mathbf {x}) := f \left(\mathbf {x} _ {0}\right) + \hat {c} _ {\mathbf {v}} f \left(\mathbf {x} _ {0}\right) + \dots + \frac {1}{k !} \hat {c} _ {\mathbf {v}} ^ {k} f \left(\mathbf {x} _ {0}\right)
$$

(mit $\mathbf{v} := \mathbf{x} - \mathbf{x}_0$). Der dabei auftretende Fehler $R_k(\mathbf{x}, \mathbf{x}_0) := f(\mathbf{x}) - p(\mathbf{x})$ geht schneller gegen Null als $|\mathbf{x} - \mathbf{x}_0|^k$; es gilt

$$
f (\mathbf {x}) = p (\mathbf {x}) + o (| \mathbf {x} - \mathbf {x} _ {0} | ^ {k}). \tag {6}
$$

Beweis für k = 2: Für den Fehler gilt (mit  $v = x - x_{0}$ ) nach der Taylor-Formel

$$
R _ {2} (\mathbf {x}, \mathbf {x} _ {0}) = \frac {1}{3 !} \hat {c} _ {\mathbf {v}} ^ {3} f (\mathbf {x} + \xi_ {2} \mathbf {v}) = \frac {1}{3 !} \sum_ {i, j, k = 1} ^ {n} v _ {i} v _ {j} v _ {l} f _ {x _ {i} x _ {j} x _ {l}} (\mathbf {x} + \xi_ {2} \mathbf {v}).
$$

Ist $f$ eine $\mathcal{C}^3$-Funktion, so ist $f_{x_i,x_j,x_l}(\mathbf{x} + \xi \mathbf{v})$ mit $\mathbf{v}\to 0$ beschränkt, ebenso $\frac{v_i}{|\mathbf{v}|}\leq 1$ für alle $i$ ($\mathbf{v}\neq 0$). Daher strebt $\frac{R_2(\mathbf{x},\mathbf{x}_0)}{|\mathbf{v}|^2} = \frac{1}{3!}\sum f_{x_i,x_j,x_l}(\mathbf{x} + \xi_2\mathbf{v})\frac{v_i}{|\mathbf{v}|}\frac{v_j}{|\mathbf{v}|} v_l$ gegen 0 ($\mathbf{v}\rightarrow 0$).

Für eine  $C^{k}$ -Funktion ( $k \geq 2$ ) heißt die nach Satz 2.2 symmetrische Matrix

$$
H _ {f} (\mathbf {x}) := (f _ {X _ {i} X _ {j}} (\mathbf {x})) = \left( \begin{array}{c c c} f _ {X _ {1} X _ {1}} (\mathbf {x}), & \dots , & f _ {X _ {1} X _ {n}} (\mathbf {x}) \\ \vdots & & \vdots \\ f _ {X _ {n} X _ {1}} (\mathbf {x}), & \dots , & f _ {X _ {n} X _ {n}} (\mathbf {x}) \end{array} \right)
$$

die HESSE-Matrix von $f$ im Punkt $\mathbf{x}$.

Wegen  $\hat{c}_{\mathbf{v}}f(\mathbf{x})=\operatorname{grad}f(\mathbf{x})\cdot\mathbf{v}$  und  $\partial_{\mathbf{v}}^{2}f(\mathbf{x})=\mathbf{v}^{T}H_{f}(\mathbf{x})\mathbf{v}$  lautet die Taylorformel (5) (mit  $x=x_{0}, v=x-x_{0}$ ) in den vielbenutzten Spezialfällen k=0,1,2 wie folgt:

---

396

7. Funktionen in mehreren Variablen. Teil 1: Differentiation

a) $f(\mathbf{x}) = f(\mathbf{x}_0) + \text{grad } f(\tilde{\mathbf{x}}) \cdot (\mathbf{x} - \mathbf{x}_0)$
    mit $\tilde{\mathbf{x}}$ auf der Strecke von $\mathbf{x}_0$ nach $\mathbf{x}$ (Mittelwertsatz),
b) $f(\mathbf{x}) = f(\mathbf{x}_0) + \mathrm{grad}f(\mathbf{x}_0)\cdot (\mathbf{x} - \mathbf{x}_0) + \frac{1}{2} (\mathbf{x} - \mathbf{x}_0)^T H_f(\mathbf{x}^*)(\mathbf{x} - \mathbf{x}_0)$ mit $\mathbf{x}^*$ auf der Strecke von $\mathbf{x}_0$ nach $\mathbf{x}$,
c) $f(\mathbf{x}) = f(\mathbf{x}_0) + \mathrm{grad}f(\mathbf{x}_0)\cdot (\mathbf{x} - \mathbf{x}_0) + \frac{1}{2} (\mathbf{x} - \mathbf{x}_0)^T H_f(\mathbf{x}_0)(\mathbf{x} - \mathbf{x}_0)$ $+o(|\mathbf{x} - \mathbf{x}_0|^2)$

## Die anschauliche Deutung von (7c) für $n = 2,3$.

n = 2: Der Graph $z = f(x, y)$ wird in einer Umgebung des Flächenpunktes $(x_0, y_0, f(x_0, y_0))$ approximiert durch die Schmiegquadrik

$$
\begin{array}{l} z = f (x _ {0}, y _ {0}) + f _ {x} (x _ {0}, y _ {0}) (x - x _ {0}) + f _ {y} (x _ {0}, y _ {0}) (y - y _ {0}) + \\ + \frac {1}{2} f _ {x x} (x _ {0}, y _ {0}) (x - x _ {0}) ^ {2} + f _ {x y} (x _ {0}, y _ {0}) (x - x _ {0}) (y - y _ {0}) + \frac {1}{2} f _ {y y} (x _ {0}, y _ {0}) (y - y _ {0}) ^ {2}. \\ \end{array}
$$

Dieses ist, falls  $H_{f}(x_{0}, y_{0}) \neq 0$ , ein Paraboloid oder ein parabolischer Zylinder. Man nennt den Flächenpunkt über  $(x_{0}, y_{0})$  flach, wenn die Schmiegquadrik eine Ebene ist  $(H_{f}(x_{0}, y_{0}) = 0)$ , der Punkt heißt elliptisch (hyperbolisch, parabolisch), wenn die Schmiegquadrik ein elliptisches Paraboloid (bzw. ein hyperbolisches Paraboloid, ein parabolischer Zylinder) ist.

![](../../raw/pages_0385-0416/images/page_411_image_10.jpg)

![](../../raw/pages_0385-0416/images/page_411_image_11.jpg)

<details>
<summary>natural_image</summary>

Pure geometric diagram showing intersecting curved and shaded planes without any text, numbers, or symbols
</details>

![](../../raw/pages_0385-0416/images/page_411_image_12.jpg)

<details>
<summary>natural_image</summary>

Pure geometric diagram showing a curved surface intersecting a plane, with no text, numbers, or symbols.
</details>

Abb. 180 - Elliptischer, hyperbolischer, parabolischer Flächenpunkt

Beispiel. Der Affensattel

$$
z = x ^ {3} - 3 x y ^ {2}
$$

hat im Punkt  $(x,y)=(0,0)$  einen Flachpunkt mit der  $(x,y)$ -Ebene als Tangentialebene. Die Hesse-Matrix lautet

$$
H _ {f} = \left( \begin{array}{c c} 6 x & - 6 y \\ - 6 y & - 6 x \end{array} \right) ,
$$

![](../../raw/pages_0385-0416/images/page_411_image_18.jpg)

<details>
<summary>natural_image</summary>

3D wireframe surface plot with x, y, z axes labeled (no numerical data or annotations)
</details>

Abb. 181 - Affensattel

ihre Determinante  $-36(x^{2} + y^{2})$  ist außerhalb von  $(0,0)$  stets < 0, d.h. jeder Punkt der Fläche mit  $(x,y) \neq (0,0)$  ist hyperbolisch. □

---

§3. Anwendungen der Differentiation

397

n = 3: Die Niveaufläche $f(x,y,z) = c$ wird in der Nähe eines Flächenpunktes $(x_0,y_0,z_0)$ approximiert durch die Quadrik

$$
\operatorname{grad} f (x _ {0}, y _ {0}, z _ {0}) \cdot \left( \begin{array}{c} x - x _ {0} \\ y - y _ {0} \\ z - z _ {0} \end{array} \right) + \frac {1}{2} \left( \begin{array}{c} x - x _ {0} \\ y - y _ {0} \\ z - z _ {0} \end{array} \right) ^ {T} H _ {f} (x _ {0}, y _ {0}, z _ {0}) \left( \begin{array}{c} x - x _ {0} \\ y - y _ {0} \\ z - z _ {0} \end{array} \right) = 0.
$$

Beispiel. Als Schmiegquadrik besitzt die Niveaufläche

$$
x \cos y + y \cos z + z \cos x = 2
$$

im Flächenpunkt (0,0,2) ein zweischaliges Hyperboloid

$$
x + (\cos 2) y + (z - 2) - x ^ {2} - (\sin 2) y (z - 2) = 0.
$$

Bemerkung. Wird (auf irgend eine Weise) eine Approximation der Form

$$
f (\mathbf {x}) = \alpha_ {0} + \sum_ {i} \alpha_ {i} (x _ {i} - x _ {0 i}) + \sum_ {i, j} \alpha_ {i j} (x _ {i} - x _ {0 i}) (x _ {j} - x _ {0 j}) + \dots + o (| \mathbf {x} - \mathbf {x} _ {0} | ^ {k})
$$

ermittelt, dann sieht man leicht durch Differenzenbildung mit der Taylor-Formel, daß es sich hierbei bereits um die Taylor-Approximation handelt. Diese Beobachtung erlaubt die Berechnung der Taylor-Approximation aus bekannten Reihenentwicklungen ( $\rightarrow$  Kap. 5, 4.3).

$$
\begin{array}{l} \text {Beispiel.} e ^ {x + y} + \sin (x y) = 1 + x + y + \frac {1}{2} (x + y) ^ {2} + \frac {1}{3 !} (x + y) ^ {3} + x y - \frac {1}{3 !} (x y) ^ {3} + \\ o ((x ^ {2} + y ^ {2}) ^ {3 / 2}). \end{array}
$$

3.3 Implizite Funktionen. Um eine Funktion $g: \mathbb{R} \supseteq D \to \mathbb{R}$ mit den Methoden der Differentialrechnung zu diskutieren, war es bis hierher im konkreten

Fall stets nötig, daß g durch einen expliziten Formelausdruck  $y = g(x)$  mit den elementaren Funktionen der Analysis ( $\rightarrow$  Kap. 2 u. 3) darstellbar ist.

Hat man dagegen den Zusammenhang zwischen x und y implizit durch eine reelle Gleichung  $f(x,y)=0$  gegeben, so ist „y als Funktion von x“ noch nicht eindeutig festgelegt, da es zu einem festen  $x_{0}$  mehrere Lösungen y von  $f(x_{0},y)=0$  geben kann.

![](../../raw/pages_0385-0416/images/page_412_image_15.jpg)

<details>
<summary>text_image</summary>

y
f(x,y)=0
y=g(x)
K
I
x
x
</details>

Abb. 182 - Implizite Funktion

Definition. Sei $f: \mathbb{R}^2 \supset D \to \mathbb{R}$. Man sagt, durch $f(x,y) = 0$ ist auf dem Intervall $I \subseteq \mathbb{R}$ eine implizite Funktion $g: I \to K$ mit Werten in $K \subseteq \mathbb{R}$ erklärt, wenn es zu jedem $x \in I$ genau ein $y \in K$ gibt mit $(x,y) \in D$ und $f(x,y) = 0$. Dieses $y$ wird mit $g(x)$ bezeichnet.

Anschaulich: Der im Rechteck  $\{(x,y); x \in I, y \in K\}$  verlaufende Bogen der Niveaulinie  $f(x,y) = 0$  ist als Graph  $y = g(x)$  darstellbar.

---

398

7. Funktionen in mehreren Variablen. Teil 1: Differentiation

Beispiele. 1. Durch $f(x,y)=3x+2y-1=0$ ($D=\mathbb{R}^{2}$) ist die implizite Funktion $g:\mathbb{R}\to\mathbb{R}$, $g(x)=\frac{1}{2}(1-3x)$ erklärt. In diesem Fall ist $f(x,y)=0$ explizit für jedes $x\in\mathbb{R}$ eindeutig nach $y$ auflösbar.

2. Durch  $f(x, y) = e^{y} + y^{3} + x^{3} + x^{2} - 1 = 0 \quad (D = \mathbb{R}^{2})$  ist ebenfalls genau eine implizite Funktion  $g : R \to R$  erklärt; denn zu jedem  $x \in R$  hat die Gleichung  $e^{y} + y^{3} = 1 - x^{2} - x^{3}$  genau eine Lösung  $y =: g(x) (h(y) := e^{y} + y^{3})$  ist strikt monoton wachsend und hat als Wertebereich R). Durch formale Manipulation kann die Gleichung  $e^{y} + y^{3} + x^{3} + x^{2} - 1 = 0$  nicht nach y aufgelöst werden. Ohne eine explizite Darstellung zu besitzen, ist daher nur die Existenz einer (eindeutig bestimmten) Funktion g gesichert mit

$$
e ^ {g (x)} + g (x) ^ {3} + x ^ {3} + x ^ {2} - 1 = 0.
$$

3. Durch  $x^{2} + y^{2} - 1 = 0$  sind implizit zwei Funktionen  $g_{1}: [-1,1] \to [0,1]$ ,  $g_{1}(x) = \sqrt{1 - x^{2}}$  und  $g_{2}: [-1,1] \to [-1,0]$ ,  $g_{2}(x) = -\sqrt{1 - x^{2}}$  erklärt. ☐

Satz 3.2 über implizite Funktionen. Sei $D \subseteq \mathbb{R}^2$ offen und $f : D \to \mathbb{R}$ stetig partiell differenzierbar. Ist $(x_0, y_0) \in D$ ein Punkt der Niveaumenge $f(x, y) = 0$ mit $f_y(x_0, y_0) \neq 0$, dann gibt es Intervalle $I \subseteq \mathbb{R}$ und $K \subseteq \mathbb{R}$ mit Mittelpunkt $x_0$ bzw. $y_0$ so daß gilt:

a) $R = \{(x,y); x \in I, y \in K\} \subseteq D$ und $f_y(x,y) \neq 0$ für alle $(x,y) \in R$.
b) Durch  $f(x,y)=0$  ist auf I eindeutig eine differenzierbare implizite Funktion  $g:I\to K$  (mit Werten in K) erklärt mit der Ableitung

$$
g ^ {\prime} (x) = - \frac {f _ {x} (x , g (x))}{f _ {y} (x , g (x))} = - \frac {f _ {x} (x , y)}{f _ {y} (x , y)} \quad \text { für   alle } x \in I . \tag {8}
$$

Beweis. Wir gehen aus von  $(x_{0}, y_{0}) = (0, 0)$  und  $f_{y}(0, 0) > 0$ , was man durch Koordinatenverschiebung und evtl. Übergang zu -f stets erreichen kann.

a): Aufgrund der Stetigkeit von  $f_{y}$  gilt  $f_{y}(x,y) > 0$  in einer ganzen Umgebung  $U = \{(x,y); x^{2} + y^{2} < c^{2}\} \quad (c > 0)$  des Nullpunkts.

b): Wir betrachten nun $f$ nur noch auf Rechtecken $\{(x,y); -\alpha \leq x \leq \alpha, -\beta \leq y \leq \beta\}$, die ganz in $U$ enthalten sind. Da die Funktion $y \to f(0,y)$ (mit $f(0,0) = 0$) echt monoton wächst ($\rightarrow$ Kap. 3), gilt $f(0,-\beta) < 0$, $f(0,\beta) > 0$ und deshalb (wegen der Stetigkeit) $f(x,-\beta) < 0$, $f(x,\beta) > 0$ für ein hinreichend kleines Intervall $-\alpha \leq x \leq \alpha$.

![](../../raw/pages_0385-0416/images/page_413_image_14.jpg)

<details>
<summary>text_image</summary>

f(x₀,y)
z
y
β
f > 0
f = 0
f < 0
-α
x₀
α
x
-β
</details>

Abb. 183 - Zum Beweis

Mit solchem  $\alpha$  wählen wir  $I := (-\alpha, \alpha)$ ,  $K := (-\beta, \beta)$ . Für  $x \in I$  ist (wieder wegen  $f_y(x, y) > 0$ ) die Funktion  $y \to f(x, y)$  echt monoton wachsend und deshalb gibt es genau ein  $y \in K$  mit  $f(x, y) = 0$ .

Das zu  $x \in I$  eindeutig bestimmte y mit  $f(x, y) = 0$  wird mit  $g(x)$  bezeichnet. Für jede Folge  $(x_{n})_{n \geq 1}$  aus I mit  $x_{n} \to x$  gilt  $g(x_{n}) \to g(x)$  (wegen  $f(x_{n}, g(x_{n})) \to$

---

§3. Anwendungen der Differentiation

399

$f(x,y)$; also ist $g$ stetig. Für $x \in I$, $y = g(x)$, $\Delta y = g(x + \Delta x) - g(x)$ und $\Delta x$ hinreichend klein gilt nach dem Mittelwertsatz ($\rightarrow$ (7a)) $f(x + \Delta x, y + \Delta y) - f(x,y) = f_x(\xi,\eta)\Delta x + f_y(\xi,\eta)\Delta y$ mit $\xi$ (bzw. $\eta$) zwischen $x$ und $x + \Delta x$ (bzw. $y$ und $y + \Delta y$). Aus $f(x,g(x)) = f(x + \Delta x,g(x + \Delta x)) = 0$ und der Stetigkeit der partiellen Ableitungen ergibt sich

$$
\frac {\Delta y}{\Delta x} = - \frac {f _ {x} (\xi , \eta)}{f _ {y} (\xi , \eta)} \rightarrow - \frac {f _ {x} (x , y)}{f _ {y} (x , y)} \quad (\text {fur} \Delta x \rightarrow 0).
$$

Bemerkung. Zu Teil b) des Satzes sagt man auch:

$f(x,y)=0$ ist um $(x_{0},y_{0})$ lokal eindeutig durch eine implizite Funktion $y=g(x)$ auflösbar. Das Wort „lokal“ bezieht sich stets auf eine nicht näher beschriebene Umgebung eines Punktes, hier $(x_{0},y_{0})$.

Nachdem die Differenzierbarkeit bewiesen ist, berechnet man die Ableitung mit der Kettenregel aus der Identität  $f(x,g(x)) = 0$  und fährt auch für die höheren Ableitungen von  $g(x)$  so fort:

$$
\begin{array}{l} f (x, g (x)) = 0 \Rightarrow f _ {x} (x, g (x)) + f _ {y} (x, g (x)) g ^ {\prime} (x) = 0 \\ \Rightarrow \quad \left(f _ {x} + f _ {y} g ^ {\prime}\right) _ {x} + \left(f _ {x} + f _ {y} g ^ {\prime}\right) _ {y} g ^ {\prime} = 0 \\ \Rightarrow \quad (f _ {x x} + f _ {y x} g ^ {\prime}) + f _ {y} g ^ {\prime \prime} + (f _ {x y} + f _ {y y} g ^ {\prime}) g ^ {\prime} = 0 \\ \end{array}
$$

etc.

Nach  $g'$  bzw.  $g''$  aufgelöst, erhält man

$$
\begin{array}{l} g ^ {\prime} (x) = - \frac {f _ {x}}{f _ {y}}; g ^ {\prime \prime} (x) = - \frac {1}{f _ {y}} \left(f _ {x x} + 2 f _ {x y} g ^ {\prime} + f _ {y y} g ^ {\prime 2}\right), \\ = - \frac {1}{f _ {y} ^ {3}} \left(f _ {x x} (f _ {y}) ^ {2} - 2 f _ {x y} f _ {x} f _ {y} + f _ {y y} (f _ {x}) ^ {2}\right). \\ \end{array}
$$

Insbesondere gilt damit in Punkten mit  $g'(x) = 0$  stets  $g''(x) = -\frac{f_{xx}(x, y)}{f_y(x, y)}$ , d.h.

Die durch $f(x,y)=0$ bestimmte implizite Funktion $y=g(x)$ hat in $(x,y)$ eine horizontale Tangente, wenn

$$
f (x, y) = 0, \quad f _ {x} (x, y) = 0, \quad f _ {y} (x, y) \neq 0.
$$

x ist eine lokale Maximumstelle, wenn  $\frac{f_{xx}(x,y)}{f_{y}(x,y)}>0$ ,

lokale Minimumstelle, wenn  $\frac{f_{xx}(x,y)}{f_{y}(x,y)} < 0.$

---

400

7. Funktionen in mehreren Variablen. Teil 1: Differentiation

Beispiel. Für die Funktion  $g(x)$  im obigen Beispiel 2 gilt

$$
g ^ {\prime} (x) = - \frac {f _ {x} (x , y)}{f _ {y} (x , y)} = - \frac {3 x ^ {2} + 2 x}{e ^ {y} + 3 y ^ {2}},
$$

wobei y durch  $f(x,y)=0$  aus x bestimmt ist. Für x=0 und  $x=-\frac{2}{3}$  ist  $g'(x)=0$ . Mit  $f_{xx}(x,y)=6x+2$  hat  $g(x)$  in 0 eine lokale Maximum- und in  $-\frac{2}{3}$  eine lokale Minimumstelle. □

![](../../raw/pages_0385-0416/images/page_415_chart_5.jpg)

<details>
<summary>line</summary>

| X | Y |
| --- | --- |
| 0 | ~1.5 |
| 0.2 | 0 |
| 0.4 | ~-0.3 |
| 0.6 | 0 |
| 0.8 | ~-0.3 |
| 1 | ~-1.5 |
</details>

Abb. 184 - $f(x, y) = e^{y} + y^{3} + x^{3} + x^{2} = 1$

Satz 3.2 gilt allgemein für $\mathcal{C}^{1}$-Funktionen $f: \mathbb{R}^{n} \supseteq D \to \mathbb{R}$ in einer Umgebung eines Punktes $(a_{1}, a_{2}, \ldots, a_{n}) \in D$ mit

$$
f (a _ {1}, a _ {2}, \dots , a _ {n}) = 0, \quad f _ {x _ {n}} (a _ {1}, \dots , a _ {n}) \neq 0:
$$

Es gibt eine Umgebung $U$ des Punktes $(a_{1},\ldots ,a_{n - 1})$ und ein offenes Intervall $K\subseteq \mathbb{R}$, das $a_{n}$ enthält, so daß gilt

a)  $R := \{(x_1, \ldots, x_{n-1}, x_n); (x_1, \ldots, x_{n-1}) \in U, x_n \in K\} \subseteq D \text{ und } f_{x_n}(\mathbf{x}) \neq 0 \text{ für alle } \mathbf{x} \in R.$
b) Zu jedem Punkt  $(x_{1},\ldots,x_{n-1})\in U$  gibt es genau eine Zahl  $x_{n}\in K$  mit  $f(x_{1},\ldots,x_{n-1},x_{n})=0$ . Durch  $x_{n}:=g(x_{1},\ldots,x_{n-1})$  ist eine partiell differenzierbare Funktion  $g:U\to K$  erklärt mit den Ableitungen

$$
\frac {\partial g}{\partial x _ {i}} (x _ {1}, \dots , x _ {n - 1}) = - \frac {f _ {x _ {i}} (x _ {1} , \dots , x _ {n})}{f _ {x _ {n}} (x _ {1} , \dots , x _ {n})} \quad (1 \leq i \leq n - 1) . \tag {9}
$$

Geometrische Deutung für $n = 3$. Die Niveaufläche $f(x, y, z) = 0$ einer $\mathcal{C}^1$-Funktion ist um jeden Flächenpunkt $(a, b, c)$ mit $f_z(a, b, c) \neq 0$ (Tangentialebene nicht parallel zur $z$-Achse) lokal darstellbar als Graph $z = g(x, y)$ einer $\mathcal{C}^1$-Funktion $g$.

Beispiel. Durch  $f(x,y,z)=x\cos y+y\cos z+z\cos x-2=0$  ist implizit eine Funktion  $z=g(x,y)$  erklärt. Es gilt  $g(0,0)=2$

$$
g _ {x} (0, 0) = - \frac {f _ {x} (0 , 0 , 2)}{f _ {z} (0 , 0 , 2)} = - \frac {\cos y - z \sin x}{- y \sin z + \cos x} \Bigg | _ {(0, 0, 2)} = - 1,
$$

$$
g _ {y} (0, 0) = - \frac {f _ {y} (0 , 0 , 2)}{f _ {z} (0 , 0 , 2)} = - \frac {- x \sin y + \cos z}{- y \sin z + \cos x} \bigg | _ {(0, 0, 2)} = - \cos 2.
$$

3.4 Lokale Minima und Maxima. Sei $f: D \to \mathbb{R}$ eine Funktion von $n$ Variablen. Ein Punkt $\mathbf{a} \in D$ heißt lokale (oder relative) Maximalstelle (bzw. Minimalstelle) von $f$, wenn es eine $r$-Umgebung $U_r(\mathbf{a}) = \{\mathbf{x} \in \mathbb{R}^n; |\mathbf{x} - \mathbf{a}| < r\}$ von $\mathbf{a}$ gibt, so daß für alle $\mathbf{x} \in U_r \cap D$ gilt:

$$
f (\mathbf {x}) \leq f (\mathbf {a}) \quad \text {(bzw.} f (\mathbf {a}) \leq f (\mathbf {x}))
$$

Gelten diese Ungleichungen jeweils für alle $\mathbf{x} \in D$, dann heißt $\mathbf{a}$ eine globale

---

§3. Anwendungen der Differentiation

401

(oder absolute) Maximal- bzw. Minimalstelle. Die Zahl  $f(\mathbf{a})$  heißt (fallweise) lokales oder globales Maximum oder Minimum. Ein Extremum oder Extremwert (lokal oder global) ist ein Minimum oder ein Maximum.

![](../../raw/pages_0417-0448/images/page_416_image_3.jpg)

<details>
<summary>text_image</summary>

z=f(x,y)
lokales Maximum
Sattelpunkte
lokales. Minimum
</details>

Abb. 185 - Extremstellen von $z = f(x, y)$

Eine der Hauptaufgaben der angewandten Analysis ist die Bestimmung der Extremalstellen einer Funktion  $f(\mathbf{x})$  auf einem Bereich D. Man schreibt hierfür

$$
f (\mathbf {x}) = \operatorname{Extr}! \quad (\mathbf {x} \in D)
$$

(bzw.  $f(\mathbf{x}) = \max!$  oder  $f(\mathbf{x}) = \min!$ ).

Je nachdem ob die Extremalstellen im Innern oder auf dem Rand von D liegen, hat man unterschiedliche Charakterisierungen:

## Satz 3.3. Lokale Extrema im Innern von $D$.

Ist $f$ auf $U_{r}(\mathbf{a})$, $\mathbf{a} \in \mathbb{R}^{n}$, eine $\mathcal{C}^{1}$-Funktion, so gilt

$$
\mathbf {a} \text {ist lokale Extremstelle von} f \Rightarrow \operatorname{grad} f (\mathbf {a}) = \mathbf {0}.
$$

Beweis. Nach Voraussetzung besitzt die reelle Funktion einer Variablen $h(t) := f(\mathbf{a} + t\mathbf{e}_i)$ in $t = 0$ eine (innere) lokale Extremalstelle. Also gilt $0 = \dot{h}(0) = \frac{\partial f}{\partial x_i}(\mathbf{a}) \quad (1 \leq i \leq n)$.

Man nennt $\mathbf{a} \in \mathbb{R}^{n}$ einen stationären Punkt von $f$, wenn $\operatorname{grad} f(\mathbf{a}) = 0$ gilt. Satz 3.3 besagt, daß man die inneren lokalen Extremalstellen unter den stationären Punkten zu suchen hat. Einen stationären Punkt, der keine Extremalstelle ist, bezeichnen wir als Sattelpunkt. Zur Identifizierung eignet sich das folgende Ergebnis.

## Satz 3.4. Extremstellen-Test für $n$ Variable.

Ist $U \subseteq \mathbb{R}^{n}$ offen, $\mathbf{a} \in U$ ein stationärer Punkt einer Funktion $f \in \mathcal{C}^{2}(U, \mathbb{R})$ und $H_{f}(\mathbf{a}) = (f_{X_{i}, X_{j}}(\mathbf{a})) \in \mathbb{R}^{n \times n}$ die Hesse-Matrix von $f$ in $\mathbf{a}$, dann gilt:

a)  $H_{f}(\mathbf{a})$  positiv definit  $\Rightarrow$  a ist lokale Minimalstelle,
b)  $H_{f}(\mathbf{a})$  negativ definit  $\Rightarrow$  a ist lokale Maximalstelle,
c)  $H_{f}(\mathbf{a})$  indefinit  $\Rightarrow$  a ist Sattelpunkt.

Beweis. Mit grad  $f(\mathbf{a}) = 0$  und (7) gilt für alle x in einer r-Umgebung von a

$$
f (\mathbf {x}) - f (\mathbf {a}) = \frac {1}{2} (\mathbf {x} - \mathbf {a}) ^ {T} H _ {f} (\mathbf {a} ^ {*}) (\mathbf {x} - \mathbf {a}) \tag {10}
$$

---

402

7. Funktionen in mehreren Variablen. Teil 1: Differentiation

mit einem $\mathbf{a}^{*}$ zwischen $\mathbf{x}$ und $\mathbf{a}$. $H_{f}(\mathbf{x})$ ist stetig und daher mit $H_{f}(\mathbf{a})$ auch in einer ganzen Umgebung von $\mathbf{a}$ positiv definit (bzw. negativ definit, bzw. indefinit). In dieser Umgebung ist die rechte Seite von (10) im Fall a) stets positiv, im Fall b) stets negativ, also $f(\mathbf{x}) \geq f(\mathbf{a})$ bzw. $f(\mathbf{x}) \leq f(\mathbf{a})$. Im Fall c) ist $f(\mathbf{x}) - f(\mathbf{a})$ in jeder Umgebung von $\mathbf{a}$ sowohl positiv als auch negativ.

Spezialfall n=2. Sei  $\mathbf{a}=(a_{1},a_{2})$  stationärer Punkt einer  $C^{2}$ -Funktion f in 2 Variablen. Unter Berücksichtigung des Positivitäts-Tests ( $\rightarrow$  Kap. 6, 7.5) liefert in diesem Fall Satz 3.4 mit der Hesse-Matrix

$$
H _ {f} (\mathbf {a}) = \left( \begin{array}{c c} f _ {x x} (\mathbf {a}) & f _ {x y} (\mathbf {a}) \\ f _ {y x} (\mathbf {a}) & f _ {y y} (\mathbf {a}) \end{array} \right)
$$

den Extremstellen-Test für 2 Variable:

$\mathbf{a} = (a_{1}.a_{2})$ stationärer Punkt, d.h. $f_{x}(\mathbf{a}) = f_{y}(\mathbf{a}) = 0$.

a)  $\det H_{f}(\mathbf{a}) > 0$ ,  $f_{xx}(\mathbf{a}) > 0 \Rightarrow \mathbf{a}$  lokale Minimalstelle,
b)  $\det H_{f}(\mathbf{a}) > 0$ ,  $f_{xx}(\mathbf{a}) < 0 \Rightarrow \mathbf{a}$  lokale Maximalstelle,
c)  $\det H_{f}(\mathbf{a}) < 0 \Rightarrow \mathbf{a} \text{ ist Sattelpunkt.}$

Beispiel 1. (n = 2). Die Funktion

$$
f (x, y) = 2 x ^ {4} + y ^ {4} - 2 x ^ {2} - 2 y ^ {2},
$$

$(x,y)\in\mathbb{R}^{2}$ , hat 9 stationäre Punkte

$\mathbf{a}_1 = (0,0)$ ， $\mathbf{a}_2 = (0,1)$

$\mathbf{a}_3 = (0, -1)$, $\mathbf{a}_4 = (\frac{1}{\sqrt{2}}, 0)$,

$\mathbf{a}_5 = \left(\frac{1}{\sqrt{2}}, 1\right), \quad \mathbf{a}_6 = \left(\frac{1}{\sqrt{2}}, -1\right),$

$\mathbf{a}_7 = \left(-\frac{1}{\sqrt{2}}, 0\right), \quad \mathbf{a}_8 = \left(-\frac{1}{\sqrt{2}}, 1\right),$

$\mathbf{a}_{9} = \left(-\frac{1}{\sqrt{2}}, - 1\right)$

![](../../raw/pages_0417-0448/images/page_417_chart_19.jpg)

<details>
<summary>surface_3d</summary>

| Axis | Range |
| --- | --- |
| x | -1.25~1.25 |
| y | -1.25~1.25 |
| z | -1.25~1.25 |
</details>

Abb. 186 - $z = 2x^{4} + y^{4} - 2x^{2} - 2y^{2}$

Für diese Punkte gilt

|  | $\mathbf{a}_{1}$ | $\mathbf{a}_{2}$ | $\mathbf{a}_{3}$ | $\mathbf{a}_{4}$ | $\mathbf{a}_{5}$ | $\mathbf{a}_{6}$ | $\mathbf{a}_{7}$ | $\mathbf{a}_{8}$ | $\mathbf{a}_{9}$ |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| $f_{xx}(\mathbf{a}_{i})$ | -4 | -4 | -4 | 8 | 8 | 8 | 8 | 8 | 8 |
| $f_{yy}(\mathbf{a}_{i})$ | -4 | 8 | 8 | -4 | 8 | 8 | -4 | 8 | 8 |
| $f_{xy}(\mathbf{a}_{i})$ | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |
| $\det H_{f}(\mathbf{a}_{i})$ | 16 | -32 | -32 | -32 | 64 | 64 | -32 | 64 | 64 |

Demnach hat $f$ bei $\mathbf{a}_{1}$ ein lokales Maximum, bei $\mathbf{a}_{5}$, $\mathbf{a}_{6}$, $\mathbf{a}_{8}$, $\mathbf{a}_{9}$ lokale Minima und Sattelpunkte in $\mathbf{a}_{2}$, $\mathbf{a}_{3}$, $\mathbf{a}_{4}$, $\mathbf{a}_{7}$.

---

§3. Anwendungen der Differentiation

403

Der Fall det  $H_{f}(\mathbf{a}) = 0$ . Hier muß man direkt das Vorzeichenverhalten von  $f(\mathbf{x}) - f(\mathbf{a})$  entweder längs Schnitten oder sogar in vollen Umgebungen von a untersuchen.

Beispiel 2 ($n = 2$). Für die Funktion $f(x, y) = (y - 2x^{2})(y - x^{2})$, $(x, y) \in \mathbb{R}^{2}$, ist $(0, 0)$ ein stationärer Punkt mit $f(0, 0) = 0$ und det $H_{f}(0, 0) = 0$. Obwohl die Funktion längs aller geraden Schnitte in $(0, 0)$ ein lokales Minimum besitzt, ist $(0, 0)$ ein Sattelpunkt, da $f(x, y) < 0$ für alle $(x, y)$ mit $x^{2} < y < 2x^{2}$ und $f(x, y) > 0$ für $y > 2x^{2}$ oder $y < x^{2}$.

Beispiel 3 (n = 3). $u(x, y, t) = \sin x \cos y \cos (x + y) \cos (x - y) \cos \omega t$ beschreibt für $t \geq 0$ die Transversalschwingung einer biegeweichen Membran in dem Quadrat $D : |x| + |y| \leq \frac{\pi}{2}$ ($\rightarrow$ §2, Aufg. 8). Wann und wo die größte Auslenkung eintritt, ist bestimmt durch grad $u(x, y, t) = 0$. Die Bedingung $u_t = 0$ führt auf

$$
\sin x \cos y \cos (x + y) \cos (x - y) \sin \omega t = 0,
$$

d.h.  $t = \frac{k\pi}{\omega} \quad (k \in \mathbb{Z})$  oder x = 0 oder  $y = \frac{\pi}{2}$  oder  $|x| + |y| = \frac{\pi}{2}$ . Letzteres ist der Rand, x = 0 ist eine Knotenlinie. Differentiation nach x bzw. y liefert

$$
\begin{array}{l} u _ {x} = \cos y \cos x [ \cos (x + y) \cos (x - y) - 2 \sin^ {2} x ] \cos \omega t, \\ u _ {y} = - \sin x \sin y [ \cos (x + y) \cos (x - y) + 2 \cos^ {2} y ] \cos \omega t. \\ \end{array}
$$

Da $\cos x$ und $\cos y$ nur im Rand verschwinden, bleibt nur der Fall $y = 0$ und $\cos^2 x - 2\sin^2 x = 0$. Das liefert die beiden Punkte $(x,y) = (\pm \arccos \sqrt{\frac{2}{3}},0)$. Für $t = \frac{k\pi}{\omega}$ ist somit die maximale Auslenkung $u = \pm \frac{2}{9}\sqrt{3}$.

\* 3.5 Ausgleichsrechnung. Sind in der Praxis die Werte gewisser Konstanten $x_{1}, \ldots, x_{n}$ aus experimentellen Messungen zu bestimmen, so treten folgende Probleme auf:

a) Jede Beobachtung birgt einen Meßfehler, daher werden zur Sicherheit stets mehr Messungen durchgeführt, als zur eindeutigen Bestimmung der  $x_{i}$  nötig sind.

b) Im allgemeinen sind die Werte  $x_{i}$  nicht unmittelbar meßbar, sondern nur implizit über die (bekannten) Gesetzmäßigkeiten des Versuchsaufbaus aus den Meßgrößen  $y_{1},\ldots,y_{m}$  ableitbar.

Nach Abschluß der Messungen liegt somit ein überbestimmtes Gleichungssystem für die  $x_{i}$  vor:

$$
y _ {1} = f _ {1} (x _ {1}, \dots , x _ {n}),
$$

$$
\vdots \quad \vdots \quad m > n. \tag {11}
$$

$$
y _ {m} = f _ {m} (x _ {1}, \dots , x _ {n}).
$$

Nimmt man an, daß jede der Größen $y_i$ mit derselben Meßunsicherheit behaftet ist, so wendet man seit C. F. GAUSS die Methode der kleinsten Quadrate an, um eine „Lösung“ x zu bestimmen, welche die unvermeidlichen Reste

---

404

7. Funktionen in mehreren Variablen. Teil 1: Differentiation

$y_{i} - f_{i}(x_{1},\ldots ,x_{n})$ gleichmäßig minimiert, d.h. für welche

$$
F (x _ {1}, \dots , x _ {n}) := \sum_ {i = 1} ^ {m} \left(y _ {i} - f _ {i} (x _ {1}, \dots , x _ {n})\right) ^ {2} = \operatorname{Min}!
$$

Man bezeichnet ein solches x als „im quadratischen Mittel beste“ oder „ausgleichende“ Lösung von (11) und unterscheidet zwischen linearen und nichtlinearen Ausgleichsproblemen, je nachdem ob alle Funktionen  $f_{i}$  linear in den  $x_{i}$  sind oder nicht.

① Lineare Ausgleichsprobleme. In diesem Falle stellt (11) ein überbestimmtes lineares Gleichungssystem dar,

$$
A \mathbf {x} = \mathbf {y}, \quad A \in \mathbb {R} ^ {m \times n}, m > n,
$$

es führt auf das Minimalproblem

(12) $F(\mathbf{x}) = |A\mathbf{x} - \mathbf{y}|^2 = \mathrm{Min}!$

mit quadratischem Polynom

$$
F (\mathbf {x}) = (A \mathbf {x} - \mathbf {y}) ^ {T} (A \mathbf {x} - \mathbf {y}) = \mathbf {x} ^ {T} A ^ {T} A \mathbf {x} - 2 \mathbf {x} ^ {T} A ^ {T} \mathbf {y} + \mathbf {y} ^ {T} \mathbf {y}.
$$

Daher ist Satz 3.3 anwendbar und man erhält als notwendige Bedingung für die Lösung von (12) mit Formel (11) aus §2

$$
\mathrm{grad} F (\mathbf {x}) = 2 A ^ {T} A \mathbf {x} - 2 A ^ {T} \mathbf {y} = \mathbf {0};
$$

das ist ein lineares $n \times n$-Gleichungssystem

(13) $A^T A\mathbf{x} = A^T\mathbf{y}$

Man nennt (13) die Gauß-Normalgleichung des linearen Ausgleichsproblems (12).

Beispiel. Wird ein Fahrzeug aus der Geschwindigkeit v auf Stillstand herabgebremst, so setzt man für den Bremsweg y eine quadratische Abhängigkeit von v an

$$
y = a v ^ {2} + b v + c.
$$

Zur Bestimmung von a, b, c werden 5 Messungen durchgeführt

| $v_{i}$[km/h] | 9 | 17 | 17 | 25 | 35 |
| --- | --- | --- | --- | --- | --- |
| $y_{i}$[m] | 3 | 9 | 5 | 14 | 23 |

Die Normalgleichung

$$
\left( \begin{array}{c c c} \sum v _ {i} ^ {4} & \sum v _ {i} ^ {3} & \sum v _ {i} ^ {2} \\ \sum v _ {i} ^ {3} & \sum v _ {i} ^ {2} & \sum v _ {i} \\ \sum v _ {i} ^ {2} & \sum v _ {i} & \sum 1 \end{array} \right) \binom{a}{b}
$$

---

§3. Anwendungen der Differentiation

405

ergibt ohne Maßeinheiten das Gleichungssystem mit Koeffizientenmatrix

$$
\left( \begin{array}{c c c c} 2 0 6 4 8 5 3 & 6 9 0 5 5 & 2 5 0 9 & 4 1 2 1 4 \\ 6 9 0 5 5 & 2 5 0 9 & 1 0 3 & 1 4 2 0 \\ 2 5 0 9 & 1 0 3 & 5 & 5 4 \end{array} \right)
$$

und eindeutiger Lösung

$$
a \approx 0. 0 1 2, b \approx 0. 2 5 9, c \approx - 0. 5 2 5.
$$

![](../../raw/pages_0417-0448/images/page_420_chart_6.jpg)

<details>
<summary>scatter</summary>

| X | Y |
| --- | --- |
| 9 | 4 |
| 17 | 5 |
| 17 | 9 |
| 25 | 14 |
| 35 | 25 |
</details>

Abb. 187 - Ausgleichende Parabel

Allgemein gilt

## Satz 3.5.

a) Das lineare Ausgleichsproblem (12) ist immer lösbar.
b) Die Lösungen von (12) und (13) stimmen überein.
c) Für zwei Lösungen  $x, x_{0}$  von (12) oder (13) gilt stets  $Ax = Ax_{0}$ .

Ist Rang A = n, so ist die Ausgleichslösung eindeutig.

Beweis. a): Da $F(\mathbf{x}) \geq 0$ für alle $\mathbf{x} \in \mathbb{R}^n$, muß jede Normalform des quadra-

tischen Polynoms  $F(\mathbf{x})$  die Gestalt  $\alpha_{1}^{2}z_{1}^{2}+\cdots+\alpha_{r}^{2}z_{r}^{2}+\gamma^{2}$  besitzen ( $\rightarrow$  Kap. 6, 7.3). Der minimale quadratische Fehler ist also  $\gamma^{2}$ , er wird in den Punkten mit den z-Koordinaten  $z_{1}=\ldots=z_{r}=0$  angenommen.

b): Mit Satz 3.3 erfüllt jede Minimalstelle $\mathbf{x}_{0}$ die Normalgleichung (13). Ist umgekehrt $\mathbf{x}_{0}$ eine Lösung von (13), so gilt $A^{T}(Ax_{0}-\mathbf{y})=\mathbf{0}$, d.h. das Residuum $\mathbf{r}=Ax_{0}-\mathbf{y}$ ist orthogonal zu allen Spalten von $A$ und damit orthogonal zu $Ax$ für jedes $\mathbf{x}\in\mathbb{R}^{n}$, folglich gilt

![](../../raw/pages_0417-0448/images/page_420_image_18.jpg)

<details>
<summary>text_image</summary>

A x₀ - y
y
O
A x₀
{A x ; x ∈ Rⁿ}
m = 3
n = 2
</details>

Abb. 188 - Lineare Ausgleichung

$$
| A \mathbf {x} - \mathbf {y} | ^ {2} = | A \mathbf {x} - A \mathbf {x} _ {0} + A \mathbf {x} _ {0} - \mathbf {y} | ^ {2} = | A \mathbf {x} - A \mathbf {x} _ {0} | ^ {2} + | \mathbf {r} | ^ {2} \geq | \mathbf {r} | ^ {2}. \tag {14}
$$

Daher nimmt  $|Ax - y|^{2}$  sein Minimum  $\gamma^{2} = r^{2}$  für  $x = x_{0}$  an.

c): Ist x eine weitere Lösung von (12), so muß mit (14)  $|Ax - Ax_{0}| = 0$  sein. Für RangA = n folgt aus  $A(\mathbf{x} - \mathbf{x}_{0}) = \mathbf{0}$  sofort  $x = x_{0}$ . ☐

Der Satz zeigt bereits zwei Wege auf, wie man im konkreten Fall die Ausgleichslösung bestimmen kann:

1. Weg (Direkte Lösung der Normalgleichung).
Berechne  $B = A^{T}A$ ,  $z = A^{T}y$  und löse  $Bx = z$  mit Gauss-Elimination.

2. Weg (Über orthogonale Transformation).

Mittels ebener Drehungen, Spiegelungen oder über das SCHMIDT-Orthogonali-

---

406

7. Funktionen in mehreren Variablen. Teil 1: Differentiation

sierungsverfahren wird sukzessive eine orthogonale Matrix P berechnet, so daß PA obere Dreiecksgestalt besitzt, d.h.

$$
P A = \binom{D}{0} \left\{ \begin{array}{l} n \\ m - n \end{array} \right., \quad D = \left( \begin{array}{c c c} ^ {*} & \ddots & * \\ 0 & & * \end{array} \right) .
$$

Mit $\mathbf{h} := P\mathbf{y} = \begin{pmatrix} \mathbf{h}_1 \\ \mathbf{h}_2 \end{pmatrix}$, $\mathbf{h}_1 \in \mathbb{R}^n$, $\mathbf{h}_2 \in \mathbb{R}^{m-n}$ folgt damit ($\rightarrow$ Kap. 6, Satz 6.2) $|A\mathbf{x} - \mathbf{y}|^2 = |PA\mathbf{x} - P\mathbf{y}|^2 = |D\mathbf{x} - \mathbf{h}_1|^2 + |\mathbf{h}_2|^2$. Das Minimum wird also erreicht, wenn $D\mathbf{x} = \mathbf{h}_1$. Dieses $n \times n$ Gleichungssystem besitzt bereits Stufenform und ist daher leicht aufzulösen.

In der Anwendung ist der zweite Weg zwar aufwendiger, aber in den numerischen Ergebnissen dafür zuverlässiger.

In der folgenden Procedure Linfit wird (nach Weg 2) Ax = y über sog. HOUSEHOLDER-Spiegelungen auf Stufenform gebracht. (Zur Vereinfachung wird die rechte Seite y als  $(n+1)$ -te Spalte einer  $m \times (n+1)$ -Matrix A(I, K) gespeichert.)

<div class="docvortex-algorithm" style="white-space: pre-wrap; font-family:monospace;">
Procedure Linfit
  ' ---- n Householder-Spiegelungen
  For I=1 To N
    S=0
    For J=I To M
      S=S+A(J,I)*A(J,I)
    Next J
    If S=0 Then
      Print "Matrix singulaer"
        End
    Endif
    V=Sqr(S)
    If A(I,I)&gt;0 Then
      V=-V
    Endif
    X(I)=V
    F=S-V*A(I,I)
    A(I,I)=A(I,I)-V
    For K=I+1 To N+1

S=0
For J=I To M
    S=S+A(J,I)*A(J,K)
Next J
S=S/F
For J=I To M
    A(J,K)=A(J,K)-A(J,I)*S
Next J
Next K
Next I
' ---- Aufloesung -------------------
X(N)=A(N,N+1)/X(N)
For I=N-1 To 1 Step -1
S=A(I,N+1)
For J=I+1 To N
    S=S-A(I,J)*X(J)
Next J
X(I)=S/X(I)
Next I

Return
</div>

② Nichtlineare Ausgleichsprobleme. In diesem Falle kann die „beste Lösung“ von (11) meist nur angenähert bestimmt werden. Das einfachste Verfahren wurde bereits im Beispiel von 3.1 vorgestellt: Man wendet das Gradientenverfahren auf die Funktion $F(\mathbf{x}) = |\mathbf{y} - \mathbf{f}(\mathbf{x})|^2$ an. In vielen Fällen ist es jedoch vorteilhafter, für einen Näherungswert $\bar{\mathbf{x}}$, der verbessert werden soll, die lineare Approximation bereits in den Gleichungen (11) durchzuführen:

---

§3. Anwendungen der Differentiation

407

<div class="docvortex-algorithm" style="white-space: pre-wrap; font-family:monospace;">
$y_{1} = f_{1}(\bar{\mathbf{x}}) + \mathrm{grad}  f_{1}(\bar{\mathbf{x}})\cdot (\mathbf{x} - \bar{\mathbf{x}}) + o(|\mathbf{x} - \bar{\mathbf{x}}|),$ $\vdots \qquad \qquad \qquad \qquad \qquad \qquad \qquad \qquad \qquad \qquad \qquad \qquad \qquad \qquad \qquad \qquad \qquad \qquad y_{m} = f_{m}(\bar{\mathbf{x}}) + \mathrm{grad}  f_{m}(\bar{\mathbf{x}})\cdot (\mathbf{x} - \bar{\mathbf{x}}) + o(|\mathbf{x} - \bar{\mathbf{x}}|).$
</div>

Anstelle von  $|\mathbf{y}-\mathbf{f}(\mathbf{x})|=\operatorname{Min!}$  wird somit das lineare Ausgleichsproblem

$$
| \mathbf {y} - \mathbf {f} (\bar {\mathbf {x}}) - \mathcal {J} _ {\mathbf {f}} (\bar {\mathbf {x}}) (\mathbf {x} - \bar {\mathbf {x}}) | ^ {2} = \min! \tag {15}
$$

gelöst, wobei die $m \times n$-Matrix $\quad \mathcal{J}_{\mathbf{f}}(\bar{\mathbf{x}}) = \begin{pmatrix} (\text{grad } f_1(\bar{\mathbf{x}}))^T \\ \vdots \\ (\text{grad } f_m(\bar{\mathbf{x}}))^T \end{pmatrix}$

die Funktional- oder Jacobi-Matrix von $\mathbf{f}:\mathbb{R}^{n}\to\mathbb{R}^{m}$ an der Stelle $\bar{\mathbf{x}}$ bezeichnet ($\rightarrow\S4$). Die Lösung $\mathbf{x}-\bar{\mathbf{x}}$ von (15) liefert dann die Richtung, in welcher der nächste verbesserte Näherungswert $\hat{\mathbf{x}}$ für die Ausgleichslösung zu suchen ist. Genauso wie beim Gradientenverfahren wird $\hat{\mathbf{x}}$ durch fortschreitende Halbierung von $\mathbf{x}-\bar{\mathbf{x}}$ so bestimmt, daß $|\mathbf{y}-\mathbf{f}(\hat{\mathbf{x}})|<|\mathbf{y}-\mathbf{f}(\bar{\mathbf{x}})|$ .

<div class="docvortex-algorithm" style="white-space: pre-wrap; font-family:monospace;">
'Programm NLSQ ------------------- Gosub F(Al,B1,Cl)
Dim F(6),X(3),A(6,4),T(6),Y(6) Exit If F&lt;FO
M=6 Lambda=Lambda/2
N=3 Until Lambda&lt;0.002
For I=1 to M Exit If (Lambda&lt;0.002)
Input "t(i), y(i)= ",T(I),Y(I) If F&lt;FO Then
Next I A=Al
Input "a,b,c= ",A,B,C B=Bl
Gosub F(A,B,C) C=Cl
FO=F FO=F
L=0 Endif
Repeat L=L+1
For I=1 To M Until L=30
A(I,1)=1 Print "Steps, a, b, c= ",L,A,B,C
A(I,2)=Exp(C*T(I)) End
A(I,3)=B*T(I)*Exp(C*T(I)) '---------------------------------------------------
A(I,4)=F(I) Procedure F(A,B,C)
Next I F=O
Gosub Linfit For I=1 To M
Lambda=1 F(I)=Y(I)-A-B*Exp(C*T(I))
Repeat F=F+F(I)*F(I)
Al=A+Lambda*X(1) Next I
Bl=B+Lambda*X(2) F=Sqr(F)
Cl=C+Lambda*X(3) Return
</div>

Beispiel. Die Temperatur y eines Körpers klingt als Funktion der Zeit t exponentiell auf einen asymptotischen Wert a ab. Für die nichtlineare Abhängigkeit

$$
y (t) = a + b e ^ {c t}
$$

---

408

7. Funktionen in mehreren Variablen. Teil 1: Differentiation

sollen die Konstanten $a, b$ [°C] und $c$ [Std$^{-1}$] durch Ausgleichsrechnung aus 6 Meßwerten bestimmt werden:

$$
\begin{array}{c c c c c c c} t _ {i} & 1 & 2 & 3 & 5 & 7 & 8 \\ \hline y _ {i} & 1 0 & 8 & 6 & 5. 5 & 5. 2 & 5 \end{array}
$$

Mit grad $f_{i}(a,b,c)^{T} = (1,e^{ct_{i}},bt_{i}e^{ct_{i}})$ liefert das Programm NLSQ für die Startwerte $a = 5$, $b = 1$, $c = -1$ nach 8 Schritten die Ausgleichslösung

$$
a \approx 5. 0 0 8 9 2, \quad b \approx 9. 6 9 1 3 6, \quad c \approx - 0. 6 4 7 9 8.
$$

In jedem Näherungsschritt wird das lineare Ausgleichsproblem mit der Procedure LINFIT gelöst.

3.6 Extremwertaufgaben mit Nebenbedingungen. In zahlreichen Extremwertaufgaben  $f(x_{1},\ldots,x_{n}) = \text{Extr!}$  ist die Menge der zulässigen Punkte  $\mathbf{x} = (x_{1},\ldots,x_{n})$  eingeschränkt durch eine oder mehrere Nebenbedingungen der Form  $g_{1}(x_{1},\ldots,x_{n}) = 0,\ldots,g_{k}(x_{1},\ldots,x_{n}) = 0$ ; d.h., die zulässigen x liegen auf einer Hyperfläche oder im Durchschnitt verschiedener Hyperflächen.

Wir behandeln zuerst den Fall $k = 1$.

Sei $M := \{ \mathbf{x} \in \mathbb{R}^n ; g(\mathbf{x}) = 0 \}$. Man sagt, $\mathbf{a} \in M$ ist eine Maximalstelle (Minimalstelle) von $f$ unter der Nebenbedingung $g(\mathbf{x}) = 0$, wenn es eine Umgebung $U_r(\mathbf{a})$ gibt, so daß $f(\mathbf{x}) \leq f(\mathbf{a})$ ($f(\mathbf{a}) \leq f(\mathbf{x})$) gilt für alle $\mathbf{x} \in U_r(\mathbf{a}) \cap M$. Die entsprechende Aufgabe kennzeichnen wir durch

$$
f (\mathbf {x}) = \operatorname{Extr}!
$$

$$
\mathrm{NB.} \quad g (\mathbf {x}) = 0.
$$

1. Methode (Die explizite Methode). Man löst, falls möglich,  $g(\mathbf{x}) = 0$  nach einer Variablen auf, sagen wir  $x_{n} = h(x_{1}, \ldots, x_{n-1})$ , und eliminiert über diese Substitution  $x_{n}$  aus f. Es entsteht das Extremalproblem ohne Nebenbedingungen:

![](../../raw/pages_0417-0448/images/page_423_image_13.jpg)

<details>
<summary>text_image</summary>

f=-2
f=-1
f=0
f=1,
grad f=0
f=0
f=-1
f=-2
f=-3
f=-3
f=-4
globales
Minimum
2 globale
Maxima
g(x,y)=0
grad g(x,y)=0
lokales Minimum
</details>

Abb. 189 - $f(x) = \mathrm{Extr!}$, $g(x) = 0$

$$
f (x _ {1}, \dots , x _ {n - 1}, h (x _ {1}, \dots , x _ {n - 1})) = \mathrm{Extr}!
$$

Beispiel. Gesucht sind die wärmsten und die kältesten Punkte auf der Sphäre  $x^{2} + y^{2} + z^{2} = 1$  bei einer Temperaturverteilung  $T(x, y, z) = xy + xz$ . Da in  $(x, y, z)$  und  $(-x, -y, -z)$  dieselbe Temperatur herrscht, genügt es, die Extremwerte auf der Hemisphäre  $x = \sqrt{1 - y^{2} - z^{2}}$  zu bestimmen.

$$
F (y, z) := T \left(x (y, z), y, z\right) = (y + z) \sqrt {1 - y ^ {2} - z ^ {2}} = \operatorname{Extr}!
$$

Auf dem Kreis $x = 0$, $y^{2} + z^{2} = 1$ gibt es keine Punkte extremaler Temperatur, dort ist $T = 0$. Für $y^{2} + z^{2} < 1$ berechnen wir über $F_{y} = F_{z} = 0$ die stationären

---

§3. Anwendungen der Differentiation

409

Punkte. Für diese muß gelten

$$
2 y ^ {2} + z ^ {2} + y z = 1, \quad y ^ {2} + 2 z ^ {2} + y z = 1.
$$

Man erhält also für  $y^{2} + z^{2} < 1$  nur die Lösungen  $y = z = \pm \frac{1}{2}$  und damit auf der Sphäre die möglichen Extremalpunkte

$$
\begin{array}{l} \mathbf {a} = \left(\frac {1}{\sqrt {2}}, \frac {1}{2}, \frac {1}{2}\right), \qquad - \mathbf {a} = \left(- \frac {1}{\sqrt {2}}, - \frac {1}{2}, - \frac {1}{2}\right), \\ \mathbf {b} = \left(\frac {1}{\sqrt {2}}, - \frac {1}{2}, - \frac {1}{2}\right), \quad - \mathbf {b} = \left(- \frac {1}{\sqrt {2}}, \frac {1}{2}, \frac {1}{2}\right). \\ \end{array}
$$

Die stetige Temperaturverteilung hat auf der Sphäre Punkte minimaler und maximaler Temperatur (→ Satz 2.1), daher sind wegen $T(\mathbf{a}) = T(-\mathbf{a}) = \frac{1}{4}\sqrt{2}$, $T(\mathbf{b}) = T(-\mathbf{b}) = -\frac{1}{4}\sqrt{2}$ die Punkte $\mathbf{a}$, $-\mathbf{a}$ die Maximalstellen, $\mathbf{b}$, $-\mathbf{b}$ die Minimalstellen.

2. Methode (Parametrisierung der Nebenbedingungen). Im Fall zweier Variablen, beispielsweise, bestimmt man eine Parameterdarstellung $x = x(t)$, $y = y(t)$, $t \in I$, der Kurve $g(x, y) = 0$ und löst für $F(t) := f(x(t), y(t))$ das gewöhnliche Extremalproblem $F(t) = \text{Extr!}$ ($\to$ Kap. 3, §2, dabei sind die Randpunkte von $I$ nicht zu vergessen!).

Die 3. Methode (die Lagrange-Multiplikatorregel) basiert auf der folgenden Beobachtung

Satz 3.6. Zu jeder Lösung a des Extremalproblems

$$
f (\mathbf {x}) = \mathrm{Extr!} \quad \mathrm{NB.} \quad g (\mathbf {x}) = 0
$$

mit  $C^{1}$ -Funktionen f, g und grad  $g(\mathbf{a}) \neq \mathbf{0}$  gibt es eine Zahl  $\lambda_{0} \in R$ , so daß gilt

$$
\operatorname{grad} f (\mathbf {a}) + \lambda_ {0} \operatorname{grad} g (\mathbf {a}) = \mathbf {0}.
$$

Beweis. Sei $\mathbf{a} = (a_{1},\ldots,a_{n})$. Wegen grad $g(\mathbf{a}) \neq \mathbf{0}$ können wir (nach evtl. Umnumerierung) $g_{x_{n}}(\mathbf{a}) \neq 0$ annehmen. Dann ist nach dem Satz über implizite Funktionen die Nebenbedingung $g(x_{1},\ldots,x_{n}) = 0$ „lokal“ (um $\mathbf{x} = \mathbf{a}$) nach $x_{n}$ auflösbar, $x_{n} = h(x_{1},\ldots,x_{n-1})$. Die Voraussetzung besagt nun, daß $f(x_{1},\ldots,x_{n-1},h(x_{1},\ldots,x_{n-1}))$ in $(a_{1},\ldots,a_{n-1})$ ein lokales Extremum besitzt. Folglich gilt ($\rightarrow$ Satz 2.6 und Satz 3.2)

$$
\begin{array}{l} 0 = f _ {x _ {i}} (\mathbf {a}) + f _ {x _ {n}} (\mathbf {a}) h _ {x _ {i}} (a _ {1}, \dots , a _ {n - 1}) \\ = f _ {x _ {i}} (\mathbf {a}) - f _ {x _ {n}} (\mathbf {a}) g _ {x _ {i}} (\mathbf {a}) g _ {x _ {n}} (\mathbf {a}) ^ {- 1} \quad (1 \leq i \leq n - 1). \\ \end{array}
$$

Mit  $\lambda_{0} := -f_{x_{n}}(\mathbf{a})g_{x_{n}}(\mathbf{a})^{-1}$  folgt die Behauptung.

Geometrische Interpretation. Unter den Annahmen von Satz 3.6 müssen die Gradienten von f und g in einem Extremalpunkt parallel sein.

---

410

7. Funktionen in mehreren Variablen. Teil 1: Differentiation

Im Falle n = 2 bedeutet dies, daß sich die Kurve  $g(\mathbf{x}) = 0$  und die Niveaulinie  $f(\mathbf{x}) = f(\mathbf{a})$  im Extremalpunkt berühren.

$\lambda_{0}$ heißt Lagrange-Multiplikator und das sich aus dem Satz ergebende Lösungsverfahren nennt man die

![](../../raw/pages_0417-0448/images/page_425_image_4.jpg)

<details>
<summary>text_image</summary>

g(x,y)=0
grad f
grad g
grad f
f=5
f=4
f=3
f=2
f=1
f=0
</details>

Abb. 190 - Lagrange-Multiplikator

## Lagrange-Multiplikatorregel:

1. Schritt. Man bildet die Hilfsfunktion

$$
L (x _ {1}, \dots , x _ {n}, \lambda) = f (x _ {1}, \dots , x _ {n}) + \lambda g (x _ {1}, \dots , x _ {n})
$$

in  $n+1$  Variablen  $x_{1},\ldots,x_{n},\lambda$  und berechnet grad L.

2. Schritt. Man bestimmt die Lösungen  $(a_{1},\ldots,a_{n},\lambda_{0})$  des i.a. nichtlinearen Gleichungssystems grad  $L(x_{1},\ldots,x_{n},\lambda)=0$ , d.h.

$$
L _ {x _ {1}} = f _ {x _ {1}} (x _ {1}, \dots , x _ {n}) + \lambda g _ {x _ {1}} (x _ {1}, \dots , x _ {n}) = 0
$$

$$
L _ {x _ {2}} = f _ {x _ {2}} (x _ {1}, \dots , x _ {n}) + \lambda g _ {x _ {2}} (x _ {1}, \dots , x _ {n}) = 0
$$

$$
\begin{array}{c c c} \cdot & \cdot & \cdot \\ \cdot & \cdot & \cdot \\ \cdot & \cdot & \cdot \end{array}
$$

$$
L _ {x _ {n}} = f _ {x _ {n}} (x _ {1}, \dots , x _ {n}) + \lambda g _ {x _ {n}} (x _ {1}, \dots , x _ {n}) = 0
$$

$$
L _ {\lambda} = \quad g (x _ {1}, \dots , x _ {n}) \quad = 0
$$

3. Schritt. Man untersucht, welche der gefundenen Werte  $(a_{1},\ldots,a_{n})$  tatsächlich Extremalstellen sind.  $\lambda_{0}$  spielt keine Rolle mehr. Die Kriterien, ob ein Extremum vorliegt oder nicht, sind äußerst unhandlich. In den meisten praktischen Problemen lassen sich die Extrema unter gefundenen Punkten „aus physikalischen Gründen“ oder durch direkten Vergleich der Funktionswerte erkennen. Schließlich sind noch die Punkte b, in denen f,g nicht differenzierbar sind oder für die grad  $g(\mathbf{b})=\mathbf{0}$  ist, getrennt zu untersuchen ( $\rightarrow$  Abb. 189).

Völlig analog verfährt man bei k (k < n) Nebenbedingungen:

Sind $f, g_{1}, \ldots, g_{k}$ $\mathcal{C}^{1}$-Funktionen und $\operatorname{grad} g_{1}(\mathbf{x}), \ldots, \operatorname{grad} g_{k}(\mathbf{x})$ für alle $\mathbf{x} \in M$, $M = \{\mathbf{x} \in \mathbb{R}^{n}; g_{1}(\mathbf{x}) = \cdots = g_{k}(\mathbf{x}) = 0\}$, linear unabhängig, dann findet man die Lösung des Extremalproblems mit den Nebenbedingungen

$$
f (x _ {1}, \dots , x _ {n}) = \mathrm{Extr}! \quad \mathrm{NB}. \quad g _ {1} (x _ {1}, \dots , x _ {n}) = \dots = g _ {k} (x _ {1}, \dots , x _ {n}) = 0
$$

unter den stationären Punkten der Lagrange-Hilfsfunktion

$$
L (x _ {1}, \dots , x _ {n}, \lambda_ {1}, \dots , \lambda_ {k}) = f (\mathbf {x}) + \lambda_ {1} g _ {1} (\mathbf {x}) + \dots + \lambda_ {k} g _ {k} (\mathbf {x}).
$$

Beispiel 1. Es ist das Volumen des größten Quaders mit achsenparallelen Kanten innerhalb des Ellipsoids  $\frac{x^{2}}{a^{2}} + \frac{y^{2}}{b^{2}} + \frac{z^{2}}{c^{2}} = 1$  zu bestimmen.

---

§3. Anwendungen der Differentiation

411

Das Problem

$$
V = (2 x) (2 y) (2 z) = 8 x y z = \max! \quad \mathrm{NB}. \quad \frac {x ^ {2}}{a ^ {2}} + \frac {y ^ {2}}{b ^ {2}} + \frac {z ^ {2}}{c ^ {2}} - 1 = 0
$$

wird mit der Multiplikatorregel gelöst.

1. Schritt. Die Hilfsfunktion: $L(x,y,z,\lambda) = 8xyz + \lambda (\frac{x^2}{a^2} +\frac{y^2}{b^2} +\frac{z^2}{c^2} -1)$.

2. Schritt.  $\operatorname{grad} L = 0$ :

$$
\begin{array}{l} L _ {x} = 8 y z + \lambda \frac {2 x}{a ^ {2}} \quad = 0 \\ L _ {y} = 8 x z + \lambda \frac {2 y}{b ^ {2}} \quad = 0 \\ L _ {z} = 8 x y + \lambda \frac {2 z}{c ^ {2}} \quad = 0 \\ L _ {\lambda} = \frac {x ^ {2}}{a ^ {2}} + \frac {y ^ {2}}{b ^ {2}} + \frac {z ^ {2}}{c ^ {2}} - 1 = 0. \\ \end{array}
$$

Multiplikation der ersten (2., 3.) Gleichung mit $x$ (bzw. $y, z$) ergibt $-4xyz = \lambda \frac{x^2}{a^2} = \lambda \frac{y^2}{b^2} = \lambda \frac{z^2}{c^2}$, also $\lambda \neq 0$ ($\lambda = 0$ führt auf die Minimallösung $V = 0$) und $\frac{3x^2}{a^2} = 1$ bzw. $x = \frac{a}{\sqrt{3}}$, $y = \frac{b}{\sqrt{3}}$, $z = \frac{c}{\sqrt{3}}$.

Das maximale Volumen beträgt  $V_{max} = \frac{8}{9}\sqrt{3}abc$ .

Beispiel 2. Es sind die Scheitelpunkte der Ellipse  $x^{2} + xy + y^{2} = 5$  zu bestimmen, das sind die Punkte mit größten oder kleinsten Abstand zum Nullpunkt:

$$
\begin{array}{l} f (x, y) = x ^ {2} + y ^ {2} = \mathrm{Extr!} \quad \mathrm{NB.} \quad x ^ {2} + x y + y ^ {2} - 5 = 0. \\ L = f + \lambda g = x ^ {2} + y ^ {2} + \lambda (x ^ {2} + x y + y ^ {2} - 5), \\ L _ {x} = 2 x + \lambda (2 x + y) \quad = 0 \\ L _ {y} = 2 y + \lambda (x + 2 y) \quad = 0 \\ L _ {\lambda} = x ^ {2} + x y + y ^ {2} - 5 = 0. \\ \end{array}
$$

Offenbar muß $\lambda \neq 0$ sein. $yL_{x} - xL_{y} = 0$ ergibt $x^{2} - y^{2} = 0$, d.h. $x = \pm y$. Aus $x = y$ folgt $x = \pm \sqrt{\frac{5}{3}}$ und aus $x = -y$ folgt $x = \pm \sqrt{5}$. Die Scheitelpunkte sind also $(\sqrt{\frac{5}{3}}, \sqrt{\frac{5}{3}})$, $(- \sqrt{\frac{5}{3}}, -\sqrt{\frac{5}{3}})$ und $(\sqrt{5}, -\sqrt{5})$, $(- \sqrt{5}, \sqrt{5})$.

## Beispiel 3.

$$
f (x _ {1}, \dots , x _ {n}) = x _ {1} ^ {2} x _ {2} ^ {2} \dots x _ {n} ^ {2} = \max! \quad \mathrm{NB}. \quad x _ {1} ^ {2} + \dots + x _ {n} ^ {2} - 1 = 0.
$$

Aus

$$
\begin{array}{l} 2 x _ {1} x _ {2} ^ {2} x _ {3} ^ {2} \dots x _ {n} ^ {2} + \lambda 2 x _ {1} = 0 \\ 2 x _ {1} ^ {2} x _ {2} x _ {3} ^ {2} \dots x _ {n} ^ {2} + \lambda 2 x _ {2} = 0 \\ 2 x _ {1} ^ {2} \dots x _ {n - 1} ^ {2} x _ {n} + \lambda 2 x _ {n} = 0 \\ x _ {1} ^ {2} + \dots + x _ {n} ^ {2} - 1 \quad = 0 \\ \end{array}
$$

: :

---

412

7. Funktionen in mehreren Variablen. Teil 1: Differentiation

folgt sofort  $-x_{1}^{2}x_{2}^{2}\cdots x_{n}^{2}=\lambda x_{1}^{2}=\lambda x_{2}^{2}=\cdots=\lambda x_{n}^{2}$ , also  $x_{i}^{2}=\frac{1}{n}$ . Wegen  $f(\mathbf{0})=0$  handelt es sich um die laut Satz 2.1 vorhandenen Maximalstellen; d.h. für alle Punkte der Sphäre  $x_{1}^{2}+\cdots+x_{n}^{2}=1$  gilt

$$
x _ {1} ^ {2} x _ {2} ^ {2} \dots x _ {n} ^ {2} \leq (\frac {1}{n}) ^ {n}.
$$

Sind $a_1, \ldots, a_n$ beliebige positive reelle Zahlen und

$$
b _ {i} ^ {2} := \frac {a _ {i}}{a _ {1} + \cdots + a _ {n}}
$$

dann gilt  $b_{1}^{2}+\cdots+b_{n}^{2}=1$  und damit  $b_{1}^{2}b_{2}^{2}\cdots b_{n}^{2}=\frac{a_{1}a_{2}\cdots a_{n}}{(a_{1}+\cdots+a_{n})^{n}}\leq(\frac{1}{n})^{n}$ , d.h.

$$
\sqrt [ n ]{a _ {1} a _ {2} \cdots a _ {n}} \leq \frac {a _ {1} + \cdots + a _ {n}}{n}.
$$

Das geometrische Mittel ist nie größer als das arithmetischen Mittel.

![](../../raw/pages_0417-0448/images/page_427_image_9.jpg)

Beispiel 4. Es werden die Extremwerte der quadratischen Form $q(\mathbf{x}) = \mathbf{x}^T A\mathbf{x}$ auf der Sphäre $\{\mathbf{x} \in \mathbb{R}^n; |\mathbf{x}| = 1\}$ gesucht $(A = A^T \in \mathbb{R}^{n \times n})$:

$$
\mathbf {x} ^ {T} A \mathbf {x} = \operatorname{Extr}! \quad \mathrm{NB}. \quad 1 - \mathbf {x} ^ {T} \mathbf {x} = 0.
$$

Mit der Lagrange-Hilfsfunktion $L(\mathbf{x},\lambda) = \mathbf{x}^T A\mathbf{x} + \lambda (1 - \mathbf{x}^T\mathbf{x})$ entsteht das Gleichungssystem $(\rightarrow \S 2,(11))$

$$
L _ {x _ {i}} = 2 \mathbf {e} _ {i} ^ {T} A \mathbf {x} - 2 \lambda x _ {i} = 0
$$

$$
L _ {\lambda} = 1 - \mathbf {x} ^ {T} \mathbf {x} = 0,
$$

welches gleichbedeutend ist mit dem Eigenwertproblem $A\mathbf{x} = \lambda \mathbf{x}$, $|\mathbf{x}| = 1$. Die Extremwerte sind also unter $q(\mathbf{x}) = \mathbf{x}^T A\mathbf{x} = \lambda \mathbf{x}^T \mathbf{x} = \lambda$ zu suchen.

Ergebnis. Der kleinste Eigenwert von $A$ ist das Minimum, der größte Eigenwert das Maximum der quadratischen Form $q(\mathbf{x}) = \mathbf{x}^T A\mathbf{x}$ auf der Sphäre $\{\mathbf{x} \in \mathbb{R}^n ; |\mathbf{x}| = 1\}$. Diese Extrema werden für die zugehörigen Eigenvektoren der Länge 1 angenommen.

Anwendung in der Mechanik. Der maximale (minimale) Wert der Normalspannung $\sigma = \mathbf{n}^{T}S\mathbf{n}$, $|\mathbf{n}| = 1$, in einem Punkt eines elastisch belasteten Körpers ist der größte (kleinste) Eigenwert des Spannungstensors $S$. Die entsprechenden Eigenvektoren bestimmen die Hauptspannungsrichtungen. ($\rightarrow$ Kap. 6, 6.1, Bsp.9 und §7, Aufg. 7).

Zusammen mit der Charakterisierung von Extremstellen im Innern eines Gebiets ( $\rightarrow$  3.4) gilt für das Extremalproblem einer Funktion f auf dem durch Hyperflächen  $g_{i}(\mathbf{x}) = 0$  begrenzten Bereich

$$
U = \{\mathbf {x} \in \mathbb {R} ^ {n}; g _ {1} (\mathbf {x}) \leq 0, \dots , g _ {r} (\mathbf {x}) \leq 0 \}:
$$

---

§3. Anwendungen der Differentiation

413

## Die Kandidaten für Extremstellen von $f:U\to\mathbb{R}$ sind

a) die Ecken von U (falls vorhanden, eindeutige Lösungen von möglichen Kombinationen  $g_{i}(\mathbf{x}) = g_{j}(\mathbf{x}) = \cdots = g_{k}(\mathbf{x}) = 0$ , sonst  $g_{l}(\mathbf{x}) < 0$ );
b) die Extremalstellen in den berandenden Kurven-, Flächen- und Hyperflächenstücken von U, die man entweder
- mit der Lagrange-Multiplikatorregel
oder
- durch Parametrisierung bzw. Einsetzen der entsprechenden Nebenbedingungen
bestimmt;
c) die stationären Stellen von $f$ im Innern von $U$:
d) die Punkte in U, in denen f nicht differenzierbar ist.

$$
\{\mathbf {x} \in \mathbb {R} ^ {n}; g _ {1} (\mathbf {x}) <   0, \dots , g _ {r} (\mathbf {x}) <   0 \};
$$

Der größte bzw. kleinste Funktionswert an den Stellen a), b), c), d) liefert das globale Maximum bzw. Minimum von f auf U.

Die Bestimmung der Ecken und der Stücke, die U beranden, ist für n > 2 meist sehr schwierig, im  $R^{2}$  über eine Skizze von U zu erledigen.

Beispiel. Gesucht sind die Extremwerte von  $f(x,y)=3x^{2}-2xy+y^{2}$  auf der Kreisscheibe  $x^{2}+y^{2}\leq1$ . Fall a) und d) treten nicht auf.

c) Lokale Extremstellen im Innern  $x^{2} + y^{2} < 1$ .

$$
f _ {x} = f _ {y} = 0; \quad \mathrm{d.h.} \quad 6 x - 2 y = 0, \quad 2 y - 2 x = 0.
$$

Es gibt nur einen stationären Punkt  $(x,y)=(0,0)$  im Innern. Da  $H_{f}(0,0)=$ 
 $=\left(\begin{array}{cc}6 & -2 \\ -2 & 2\end{array}\right)$  positiv definit ist, besitzt f in  $(0,0)$  ein lokales Minimum.

b) Die Extremstellen auf dem Rand

$$
f (x, y) = \mathrm{Extr!} \quad \mathrm{NB.} \quad x ^ {2} + y ^ {2} - 1 = 0
$$

bestimmen wir mit der Multiplikatorregel:

$$
L (x, y, \lambda) = 3 x ^ {2} - 2 x y + y ^ {2} + \lambda (x ^ {2} + y ^ {2} - 1).
$$

$$
L _ {x} = 6 x - 2 y + 2 \lambda x = 0,
$$

$$
L _ {y} = - 2 x + 2 y + 2 \lambda y = 0,
$$

$$
L _ {\lambda} = \quad x ^ {2} + y ^ {2} - 1 \quad = 0.
$$

Wie in Beispiel 4 ist ein Eigenwertproblem zu lösen: Die Eigenwerte sind $\lambda_{1}=2+\sqrt{2},\lambda_{2}=2-\sqrt{2}$, dazu die normierten Eigenvektoren

$$
\mathbf {a} = \frac {1}{\sqrt {4 - 2 \sqrt {2}}} \binom{1}{1 - \sqrt {2}}, \quad \mathbf {b} = \frac {1}{\sqrt {4 + 2 \sqrt {2}}} \binom{1}{1 + \sqrt {2}}.
$$

Globales Maximum in $\mathbf{a}, -\mathbf{a}: f(\mathbf{a}) = f(-\mathbf{a}) = \lambda_1 = 2 + \sqrt{2}$,

Globales Minimum in 0:  $f(\mathbf{0}) = 0$ .

□

---

414

7. Funktionen in mehreren Variablen. Teil 1: Differentiation

## Aufgaben

1. Man bestimme für die Funktion

$$
f (x, y) = x ^ {2} e ^ {y / 3} (y - 3) - \frac {1}{2} y ^ {2}, \quad (x, y) \in \mathbb {R} ^ {2},
$$

- $\operatorname{grad} f$ und die Hesse-Matrix $H_{f}$,
- die Taylor-Annäherung 2. Ordnung im Punkt (0,0),
- den Typ der Flächenpunkte auf dem Graphen $z = f(x, y)$ längs $x = 0$,
- die Taylor-Reihe von $f(x,y)$ samt Konvergenzbereich über die Exponentialreihe.

![](../../raw/pages_0417-0448/images/page_429_image_10.jpg)

<details>
<summary>text_image</summary>

y
y = 3.5
x = y = -.5
</details>

$$
z = x ^ {2} e x p (y / 3) (y - 3) -. 5 y ^ {2}
$$

2. Für die Funktion  $f(x, y) = y^{4} - 3xy^{2} + x^{3}$  bestimme man

a) die lokalen und die globalen Extremstellen und die Sattelpunkte,
b) die Extremwerte auf $\{(x,y):|x|\leq\frac{5}{2},|y|\leq2\}$.
c) die Taylor-Reihe im Punkt  $\left(\frac{3}{2},\frac{3}{2}\right)$ .

3. Für die Funktion

$$
f (x, y) = \left\{ \begin{array}{c l} \frac {\sin 2 \sqrt {x ^ {2} + y ^ {2}}}{\sqrt {x ^ {2} + y ^ {2}}} & , (x, y) \neq (0, 0) \\ 2 & , (x, y) = (0, 0) \end{array} \right.
$$

![](../../raw/pages_0417-0448/images/page_429_image_19.jpg)

<details>
<summary>natural_image</summary>

3D wireframe diagram of a conical structure with grid lines, no text or symbols present
</details>

bestimme man:

a) die Tangentialebene an den Graphen $z = f(x, y)$ im Punkt $(\frac{\pi}{2}, 0, 0)$.
b) die Taylor-Entwicklung bis zur 2. Ordnung in (0,0) und $(\frac{\pi}{2},0)$.

4. Man entwickel nach der Taylorformel bis zur 2. Potenz von x, y:

a)  $f(x, y) = x^{2} \sin \frac{xy}{2} \text{ um } (1, \pi),$
b)  $f(x, y) = (x^{2} - 2y^{2}) \cdot (4 + xy)^{-1/2} \text{ um } (0, 0),$
c) $f(x,y) = x^{2} - \cos (\frac{x}{y})$ in $(\pi ,1)$.

5. Man bestimme und skizziere den Bereich der Halbebene $x > 0$, in dem die Hesse-Matrix $H_{g}(x,y)$ der Funktion $g(x,y) = x^{y}$, $x > 0$, indefinit ist.

6. Man bestätige, daß  $y + 2x = e^{2y/x}$  für x > 0 zwei verschiedene Auflösungen  $y = f(x)$  besitzt und bestimme deren gemeinsamen Definitionsbereich.

Man bestimme und diskutiere die Stellen mit  $f'(x) = 0$  und skizziere beide Graphen. Wie lauten die entsprechenden Antworten für die Auflösung  $x = g(y)$ ?

7. Gegeben ist die Kurve $g(x, y) = 12y^5 - 20xy^3 + 5x^4 = 0$, $x > 0$, $y > 0$.

a) In der Umgebung welcher Punkte ist implizit eine Funktion  $y = f(x)$  bestimmt?
Berechne dort  $f' = \frac{dy}{dx}$  implizit.
b) In welchen Punkten der Kurve ist  $f' = 0$ ? Berechne für diese Kurvenpunkte den Wert von  $f''$ .

---

§3. Anwendungen der Differentiation

415

8. Die Cassini-Kurven  $N_{k}$  sind die Niveaulinien  $(f(x,y)=k)$  der Funktion

$$
f (x, y) = [ (x + 1) ^ {2} + y ^ {2} ] \cdot [ (x - 1) ^ {2} + y ^ {2} ], x, y \in \mathbb {R}.
$$

a) Auf welcher Kurve $T$ liegen die Punkte mit Tangenten parallel zur $x$-Achse?
Für welche Werte von k hat  $N_{k}$  genau 4 derartige Punkte?
b) Für den Fall $k = 1$ (Lemniskate) diskutiere man die Auflösungen nach $y$ mit maximalem Definitionsbereich und bestimme man die Tangenten in $(x, y) = (0, 0)$.
c) Für welches $k > 1$ verschwindet die Krümmung von $N_{k}$ in den Punkten mit $x = 0$ (Rennbahnkurve)?
Man skizziere die Kurve!

9. Die KEPLER-Gleichung

$$
\frac {2 \pi}{T} t = \psi - \epsilon \sin \psi
$$

bestimmt den Ort eines Planeten auf einer Ellipsenbahn in Abhängigkeit von der Zeit $t$ nach dem 2. Kepler-Gesetz ($0 < \epsilon < 1$ numerische Exzentrizität der Ellipse, $\psi = \star AOQ$, $T$ Umlaufzeit).

![](../../raw/pages_0417-0448/images/page_430_image_13.jpg)

<details>
<summary>text_image</summary>

z=f(x,y)
O
O
y
x
z
</details>

![](../../raw/pages_0417-0448/images/page_430_image_14.jpg)

<details>
<summary>text_image</summary>

y
Q
ψ
P
O
a
x
A
</details>

Man zeige, daß implizit genau eine Funktion  $\psi = \psi(t)$  definiert ist und bestimme ihre Extremstellen ( $\rightarrow$  Band 2: Kap. 9, §3, Aufg. 11 und Kap. 11, 4.5).

10. Gilt für die $\mathcal{C}^{1}$-Funktion $f: \mathbb{R}^{3} \to \mathbb{R}$ im Punkt $\mathbf{x} \quad f_{x} \neq 0$, $f_{y} \neq 0$, $f_{z} \neq 0$, so kann in einer Umgebung nach $x$, $y$ und $z$ aufgelöst werden: $x = x(y,z)$, $y = y(x,z)$, $z = z(x,y)$. Man zeige, daß für die Ableitungen dieser Funktionen

$$
\frac {\partial x}{\partial y} \cdot \frac {\partial y}{\partial z} \cdot \frac {\partial z}{\partial x} = - 1
$$

gilt und überprüfe dies an der Van-der-Waals-Gleichung  $f(p,V,T)=pV-RT$ .

11. Wird eine Schraubenfeder belastet, so ruft dies Torsion und Biegung im Werkstoff hervor. Ist F die Belastung in Richtung der Schraubachse, so sind folgende Kenngrößen der Feder Funktionen von F: Die Höhe H, der Radius r, die Windungszahl n, die Torsion τ und die Krümmung κ. Die Werte für F = 0 seien  $H_{0}$ ,  $r_{0}$ ,  $n_{0}$ ,  $\tau_{0}$  bzw.  $\kappa_{0}$ . Konstant bleiben bei Belastung L: die Länge, GJ: die Torsions- und EJ: die Biegesteifigkeit des Werkstoffes.

![](../../raw/pages_0417-0448/images/page_430_image_20.jpg)

<details>
<summary>text_image</summary>

M
M_B
M_T
F
</details>

Zerlegt man in jedem Punkt der Feder das Belastungsmoment $M^{1}$ in $M_B$: das Biege- und $M_T$: das Torsionsmoment ($\rightarrow$ Bsp. in 1.2), so erhält man drei implizite Gleichungen für $H(F)$, $r(F)$ und $n(F)$:

---

416

7. Funktionen in mehreren Variablen. Teil 1: Differentiation

Die Torsionsgleichung  $GJ(\tau_{0}-\tau)=-m_{T}$  liefert ( $\rightarrow$   $\S1$  (14))

$$
G J \cdot (\frac {H _ {0}}{L r _ {0}} \sqrt {L ^ {2} - H _ {0} ^ {2}} - \frac {H}{L r} \sqrt {L ^ {2} - H ^ {2}}) = F \cdot r \cdot \sqrt {L ^ {2} - H ^ {2}} .
$$

Die Biegegleichung  $EJ(\kappa_{0}-\kappa)=-m_{B}$  ergibt

$$
(**) E J \cdot (\frac {L ^ {2} - H _ {0} ^ {2}}{r _ {0}} - \frac {L ^ {2} - H ^ {2}}{r}) = - F \cdot r \cdot L \cdot H.
$$

$n = n(F)$ ist bestimmt durch die Beziehung

$$
(2 n \pi r) ^ {2} + H ^ {2} = L ^ {2}.
$$

a) Für welche Belastung  $F_{max}$  ergibt sich aus (\*) und (\*\*)  $H(F_{max}) = 0?$
b) Man berechne aus (\*), (\*\*), (\*\*\* ) $H'(0)$, $r'(0)$ und $n'(0)$ und bestätige (mit $\sin x_0 = \frac{H_0}{L}$) die gebräuchlichen Näherungen:

$$
H - H _ {0} \approx H ^ {\prime} (0) \cdot F = - L r _ {0} ^ {2} (\frac {\cos^ {2} \alpha_ {0}}{G J} + \frac {\sin^ {2} \alpha_ {0}}{E J}) \cdot F
$$

$$
r - r _ {0} \approx r ^ {\prime} (0) \cdot F = r _ {0} ^ {3} \sin \alpha_ {0} \left(\frac {2}{G J} - \frac {\cos 2 \alpha_ {0}}{E J \cos^ {2} \alpha_ {0}}\right) \cdot F
$$

$$
n - n _ {0} \approx n ^ {\prime} (0) \cdot F = \frac {1}{2 \pi} r _ {0} L \sin \alpha_ {0} \cos \alpha_ {0} [ \frac {1}{E J} - \frac {1}{G J} ] \cdot F.
$$

12. Man löse im  $R^{2}$

$$
f (x, y) = x ^ {2} - x y + y ^ {2} - x = \mathrm{Extr!}
$$

$$
\mathrm{NB.} \quad g (x, y) = x ^ {2} + y ^ {2} - 1 \leq 0.
$$

Ist hier auch ein Eigenwertproblem versteckt?

13. Gegeben ist die reelle Funktion $f(x, y) = \sin[\pi(x^2 + y)] + \cos(\pi y)$ über dem Bereich (der reellen Ebene) $A = \{(x, y); 0 \leq y \leq 1 - x^2\}$.

a) Man skizziere A.
b) Man bestimme die stationären Punkte von  $z = f(x, y)$  im Innern von A.
c) Man diskutiere die Funktion  $g(x) := f(x,0)$  in  $|x| \leq 1$ .
Gefragt sind: $g'(x)$, $g''(x)$, die Symmetrie zu den Achsen, die Extrema, die Wendepunkte, die Monotonie- und Konvexitätsbereiche sowie eine sorgfältige Skizze. (Hinweis: Für $u \approx .6532712$ ist $\cos u = 2u \cdot \sin u$)
d) Wo liegen die lokalen Extremstellen von $z = f(x, y)$ auf $y = 1 - x^{2}$, $y \geq 0$?
e) Man ermittle Lage und Wert der globalen Extrema von $z = f(x, y)$ auf $A$ und trage die Punkte in die Skizze von $A$ ein.

14. Die größte Raute in einem Würfel.

Für welche Werte von $a, b$ ($-1 \leq a, b \leq +1$) ist das ebene Viereck mit den vier Ecken $A = (1, a, -1)$, $B = (b, 1, -1)$, $C = (-1, -a, 1)$, $D = (-b, -1, 1)$ ein gleichseitiges mit maximalem Flächeninhalt?

Tip: Lagrange-Multiplikatorenregel verwenden!

15. Von allen Vierecken mit gegebenen Seiten a, b, c, d (in der skizzierten Reihenfolge) ist das flächengrößte stets ein Sehenviereck. Man zeige dies mittels Lagrange-Multiplikatorregel.

![](../../raw/pages_0417-0448/images/page_431_image_30.jpg)

---

§3. Anwendungen der Differentiation

417

16. Für eine Rinne mit Trapez-Querschnitt gebe man den Zusammenhang  $f(h, \alpha, A, U) = 0$  für die Höhe h, den Neigungswinkel  $\alpha$ , den Querschnittsinhalt A und U gemäß Skizze. Man löse damit für

![](../../raw/pages_0417-0448/images/page_432_image_3.jpg)

<details>
<summary>text_image</summary>

h
α
A
U
</details>

$$
0 \leq h \leq \frac {U}{2} \sin x, \quad 0 \leq x \leq \frac {\pi}{2}
$$

die Optimierungsaufgaben:

a) Maximaler Inhalt A bei vorgegebenem Umfang  $U = U_{0}!$
b) Minimaler Materialaufwand U bei festem Inhalt  $A = A_{0}!$

\- In welchem Zusammenhang stehen die Lösungen? (Dualität)

17. Ein KFZ-Radlager mit 14 Kugeln soll so vorgespannt werden, daß sich bei einer vertikalen Belastung des Innenrings mit F = 3000N eine möglichst kleine maximale Kugelpressung einstellt:

Jede Kugel des Lagers wird radial belastet, gepreßt und elastisch verformt: Die Vorspannung drückt den Innenring konzentrisch um  $e[\mu m]$  gegen den Außenring, die Last F verschiebt ihn um  $x[\mu m]$  in x-Richtung nach unten.

![](../../raw/pages_0417-0448/images/page_432_image_12.jpg)

<details>
<summary>text_image</summary>

F
φᵢ
y
F₁
F₁
x
F = ∑_{i=1}^{1.4} Fᵢ cos φᵢ
</details>

Die radiale Verformung  $\delta_{i}$  der i-ten Kugel lautet somit (in erster Näherung)

$$
\delta_ {i} = e + x \cos \varphi_ {i}, \quad i = 1, 2, \dots , 1 4.
$$

Der Zusammenhang zwischen Preßlast $F_{i}$ und Verformung $\delta_{i}$ ist nach G. HERTZ:

$$
F _ {i} = C \cdot (\delta_ {i}) _ {+} ^ {3 / 2} := \left\{ \begin{array}{c l} C \delta_ {i} ^ {3 / 2}, & \text {falls} \delta_ {i} \geq 0 \\ 0, & \text {falls} \delta_ {i} <   0 \end{array} ; \quad i = 1, 2, \dots , 1 4. \right.
$$

(C ist eine von der Form des Lagers abhängige Konstante, hier  $C = 10 \frac{N}{\mu m}^{3/2}$ .) Ist wie in der Skizze  $\varphi_{1} = 0$  und  $\varphi_{i+1} = \frac{2\pi i}{14}$ , so erhält man:

$$
F = F (e, x) = C \cdot \sum_ {i = 1} ^ {1 4} (e + x \cos \frac {\pi i}{7}) _ {+} ^ {3 / 2} \cdot \cos \frac {\pi i}{7}; \tag {*}
$$

$$
F _ {1} = F _ {1} (e, x) = C \cdot (e + x) _ {+} ^ {3 / 2}. \quad (\text {Maximale Kugellast im Lager})
$$

a) Keine Vorspannung: Setze e = 0 und berechne x aus F = 3000N.
Wie groß ist die maximale Kugellast $F_{1}(0,x)$, wie viele Kugeln sind belastet?
b) Optimale Vorspannung: Man löse die Extremwertaufgabe

$$
F _ {1} (e, x) = \mathrm{Min}!, \quad F (e, x) = 3 0 0 0 \mathrm{N}, \quad e _ {0} \geq 0, x _ {0} > 0
$$

mit der Lagrange-Multiplikatorregel!

(Hilfe: Eliminiere den Multiplikator und leite eine Gleichung für  $\frac{e}{x}$  her; diese ist mit dem Newton-Verfahren numerisch zu lösen!)

Ergebnis:  $e = 8.182\mu m$ ,  $x = 10.88\mu m$ . Die maximale Kugellast ist bei b) um 11.2% kleiner als bei a). Dafür sind stets 11 Kugeln belastet.

---

418

7. Funktionen in mehreren Variablen. Teil 1: Differentiation

## §4. Vektorwertige Funktionen

4.1 Die Differentiation. Wir betrachten Funktionen (Abbildungen), die jedem Punkt (Ortsvektor) $\mathbf{x} \in D \subseteq \mathbb{R}^{n}$ einen Vektor $\mathbf{f}(\mathbf{x}) \in \mathbb{R}^{m}$ zuordnen

$$
\mathbf {f}: \mathbb {R} ^ {n} \supseteq D \to \mathbb {R} ^ {m}, \quad \mathbf {f} (\mathbf {x}) = \left( \begin{array}{c} f _ {1} (\mathbf {x}) \\ f _ {2} (\mathbf {x}) \\ \vdots \\ f _ {m} (\mathbf {x}) \end{array} \right) = \left( \begin{array}{c} f _ {1} (x _ {1}, x _ {2}, \ldots , x _ {n}) \\ f _ {2} (x _ {1}, x _ {2}, \ldots , x _ {n}) \\ \vdots \\ f _ {m} (x _ {1}, x _ {2}, \ldots , x _ {n}) \end{array} \right)
$$

und übertragen sämtliche Begriffe aus §2 über die Komponentenfunktionen $f_i$ auf die vektorwertige Funktion $\mathbf{f}$:

Definition. Für $\mathbf{f}:\mathbb{R}^n\supseteq D\to \mathbb{R}^m$ und $\mathbf{x},\mathbf{x}_0\in D$ gilt

a) Der Grenzwert, die partielle Differentiation und die „klein-o“-Notation sind jeweils komponentenweise erklärt (→ 2.2-2.4):

$$
\lim _ {\mathbf {x} \to \mathbf {x} _ {0}} \mathbf {f} (\mathbf {x}) := \left( \begin{array}{c} \lim _ {\mathbf {x} \to \mathbf {x} _ {0}} f _ {1} (\mathbf {x}) \\ \lim _ {\mathbf {x} \to \mathbf {x} _ {0}} f _ {2} (\mathbf {x}) \\ \vdots \\ \lim _ {\mathbf {x} \to \mathbf {x} _ {0}} f _ {m} (\mathbf {x}) \end{array} \right); \qquad \frac {\partial \mathbf {f}}{\partial x _ {i}} (\mathbf {x}) := \left( \begin{array}{c} \frac {\partial f _ {1}}{\partial x _ {i}} (\mathbf {x}) \\ \frac {\partial f _ {2}}{\partial x _ {i}} (\mathbf {x}) \\ \vdots \\ \frac {\partial f _ {m}}{\partial x _ {i}} (\mathbf {x}) \end{array} \right),
$$

$$
\mathbf {f} (\mathbf {x}) = o (| \mathbf {x} - \mathbf {x} _ {0} |) \iff f _ {k} (\mathbf {x}) = o (| \mathbf {x} - \mathbf {x} _ {0} |), k = 1, 2, \dots , m.
$$

b) f ist genau dann stetig, partiell differenzierbar oder eine $\mathcal{C}^{r}$-Funktion, wenn sämtliche Komponentenfunktionen $f_{k}$ von $\mathbf{f}$, $k = 1,2,\ldots,m$, stetig, partiell differenzierbar bzw. $\mathcal{C}^{r}$-Funktionen sind.

c) f heißt in $\mathbf{x}_{0} \in D$ total differenzierbar oder linear approximierbar, wenn es eine $m \times n$-Matrix $A$ und eine ganze $r$-Umgebung $U_{r}(\mathbf{x}_{0}) = \{\mathbf{x} \in \mathbb{R}^{n} ; |\mathbf{x} - \mathbf{x}_{0}| < r\}$ in $D$ gibt, so daß für alle $\mathbf{x} \in U_{r}(\mathbf{x}_{0})$ gilt

$$
\mathbf {f} (\mathbf {x}) = \mathbf {f} (\mathbf {x} _ {0}) + A \left(\mathbf {x} - \mathbf {x} _ {0}\right) + o (| \mathbf {x} - \mathbf {x} _ {0} |) . \tag {1}
$$

Aus (1) folgt die lineare Approximierbarkeit aller Komponentenfunktionen, d.h.

$$
f _ {k} (\mathbf {x}) = f _ {k} (\mathbf {x} _ {0}) + \mathrm{grad}   f _ {k} (\mathbf {x} _ {0}) \cdot (\mathbf {x} - \mathbf {x} _ {0}) + o (| \mathbf {x} - \mathbf {x} _ {0} |) , k = 1, \dots , m .
$$

Definiert man daher die

Funktional- oder Jacobi-Matrix von f in  $x_{0}$

$$
\mathcal {J} _ {\mathbf {f}} (\mathbf {x} _ {0}) := \left( \begin{array}{c} \operatorname{grad} f _ {1} (\mathbf {x} _ {0}) ^ {T} \\ \operatorname{grad} f _ {2} (\mathbf {x} _ {0}) ^ {T} \\ \vdots \\ \operatorname{grad} f _ {m} (\mathbf {x} _ {0}) ^ {T} \end{array} \right) = \left(\frac {\partial \mathbf {f}}{\partial x _ {1}} (\mathbf {x} _ {0}), \dots , \frac {\partial \mathbf {f}}{\partial x _ {n}} (\mathbf {x} _ {0})\right) = \left(\frac {\partial f _ {i}}{\partial x _ {j}} (\mathbf {x} _ {0})\right) _ {m \times n},
$$

so ist die Matrix $A$ in (1) mit Satz 2.3 eindeutig bestimmt als $A = \mathcal{J}_{\mathbf{f}}(\mathbf{x}_0)$.

---

§4. Vektorwertige Funktionen

419

Merke. Die Zeilen der Jacobi-Matrix sind die Gradienten der Komponenten von f (als Zeilenvektoren geschrieben), die Spalten der Jacobi-Matrix sind die partiellen Ableitungen des Spaltenvektors f.

Satz 2.4 läßt sich leicht auf den Fall m > 1 übertragen. Dagegen gilt der Mittelwertsatz und damit die Taylor-Formel 3.1 für m > 1 nicht!

Satz 4.1 Sei $\mathbf{f}:\mathbb{R}^{n}\supseteq D\to \mathbb{R}^{m}$ eine $\mathcal{C}^1$ -Abbildung, dann gilt:

a) f ist für alle  $x \in D$  linear approximierbar.
b) Ist D konvex (→ 3.2), dann gibt es ein ξ, 0 < ξ < 1, so daβ

$$
\left| \mathbf {f} (\mathbf {x}) - \mathbf {f} (\mathbf {x} _ {0}) \right| \leq \left| \mathcal {J} _ {\mathbf {f}} \big (\mathbf {x} _ {0} + \xi (\mathbf {x} - \mathbf {x} _ {0}) \big) (\mathbf {x} - \mathbf {x} _ {0}) \right|.
$$

Man schreibt hierfür kurz

$$
\mathbf {f} (\mathbf {x}) \approx \mathbf {f} (\mathbf {x} _ {0}) + \mathcal {J} _ {\mathbf {f}} (\mathbf {x} _ {0}) \left(\mathbf {x} - \mathbf {x} _ {0}\right) \quad \text {mit einem Fehler} o (| \mathbf {x} - \mathbf {x} _ {0} |). \tag {2}
$$

Beispiel 1. Jede lineare Abbildung $\mathbf{f}:\mathbb{R}^{n}\to\mathbb{R}^{m}$ mit $\mathbf{f}(\mathbf{x})=A\mathbf{x}, A\in\mathbb{R}^{m\times n}$, ist total differenzierbar. Die Jacobi-Matrix ist gerade ihre Abbildungsmatrix

$$
\mathcal {J} _ {\mathbf {f}} (\mathbf {x}) = A \quad \text {fur alle} \mathbf {x} \in \mathbb {R} ^ {n}. \tag {3}
$$

Beispiel 2. Polarkoordinaten. Der Streifen $D$ der kartesischen $(r, \varphi)$-Ebene $D = \{(r, \varphi); 0 \leq r < \infty, 0 \leq \varphi < 2\pi\}$ wird mittels

$$
\mathbf {x} (r, \varphi) = \binom{r \cos \varphi}{r \sin \varphi}
$$

so auf die kartesische x-Ebene abgebildet, daß zu jedem Punkt  $x \neq 0$  genau ein  $(r, \varphi) \in D$  gehört. Die Jacobi-Matrix dieser Abbildung lautet

$$
\mathcal {J} _ {\mathbf {x}} (r, \varphi) = \left(\frac {\partial \mathbf {x}}{\partial r}, \frac {\partial \mathbf {x}}{\partial \varphi}\right) = \left( \begin{array}{c c} \cos \varphi & - r \sin \varphi \\ \sin \varphi & r \cos \varphi \end{array} \right)  .
$$

Die Ableitungsregeln bestätigt man leicht mit (1):

Für $\mathbf{x} \in \mathbb{R}^n$, $\mathbf{v}(\mathbf{x}), \mathbf{w}(\mathbf{x}) \in \mathbb{R}^m$, $f(\mathbf{x}) \in \mathbb{R}$ und $\alpha, \beta \in \mathbb{R}$ gilt

(4)

a) $\mathcal{J}_{\alpha \mathbf{v} + \beta \mathbf{w}}(\mathbf{x}) = \alpha \mathcal{J}_{\mathbf{v}}(\mathbf{x}) + \beta \mathcal{J}_{\mathbf{w}}(\mathbf{x})$
(Linearität),
b) $\mathcal{J}_f\mathbf{v}(\mathbf{x}) = f(\mathbf{x})\mathcal{J}_{\mathbf{v}}(\mathbf{x}) + \mathbf{v}(\mathbf{x})\mathcal{J}_f(\mathbf{x}) = f(\mathbf{x})\mathcal{J}_{\mathbf{v}}(\mathbf{x}) + \mathbf{v}(\mathbf{x})(\mathrm{grad}f(\mathbf{x}))^T$
(Produktregel für Multiplikation mit skalarer Funktion),
c) $\mathcal{J}_{\mathbf{v}^T\mathbf{w}}(\mathbf{x}) = \mathbf{v}(\mathbf{x})^T\mathcal{J}_{\mathbf{w}}(\mathbf{x}) + \mathbf{w}(\mathbf{x})^T\mathcal{J}_{\mathbf{v}}(\mathbf{x})$
(Produktregel für das Skalarprodukt),
d) $\mathcal{J}_{\mathbf{v}\times \mathbf{w}}(\mathbf{x}) = \mathbf{v}(\mathbf{x})\times \mathcal{J}_{\mathbf{w}}(\mathbf{x}) - \mathbf{w}(\mathbf{x})\times \mathcal{J}_{\mathbf{v}}(\mathbf{x})$
(Produktregel für das ×-Produkt, m = 3).

---

420

7. Funktionen in mehreren Variablen. Teil 1: Differentiation

Beachte. In (4b) ist der zweite Summand kein Skalarprodukt, sondern eine $m \times n$-Matrix („Spalte × Zeile“).

Das Produkt „Spaltenvektor × Matrix“ in (4d) ist spaltenweise zu verstehen.

Beispiel 3. Die quasilineare Abbildung $\mathbf{f}(\mathbf{x}) = f(\mathbf{x})A\mathbf{x}$ mit der skalaren $\mathcal{C}^1$-Funktion $f: \mathbb{R}^n \supseteq D \to \mathbb{R}$ und der konstanten Matrix $A \in \mathbb{R}^{m \times n}$ besitzt die Jacobi-Matrix

$$
\mathcal {J} _ {\mathbf {f}} (\mathbf {x}) = f (\mathbf {x}) A + (A \mathbf {x}) (\operatorname{grad} \varphi (\mathbf {x})) ^ {T}.
$$

4.2 Die Kettenregel. Zwei Abbildungen $\mathbf{f}:\mathbb{R}^{n}\supseteq D\to\mathbb{R}^{m},\mathbf{g}:\mathbb{R}^{m}\supseteq G\to\mathbb{R}^{q}$ mit $\mathbf{f}(D)\subseteq G$, nacheinander ausgeführt, ergeben das Kompositum

$$
\mathbf {g} \circ \mathbf {f}: D \to \mathbb {R} ^ {q}, \quad (\mathbf {g} \circ \mathbf {f}) (\mathbf {x}) := \mathbf {g} (\mathbf {f} (\mathbf {x})).
$$

Satz 4.2. Die Kettenregel. Sind $\mathbf{f}:\mathbb{R}^{n}\supseteq D\to\mathbb{R}^{m}$ in $\mathbf{x}_{0}\in D$ und $\mathbf{g}:\mathbb{R}^{m}\supseteq G\to\mathbb{R}^{q}$ in $\mathbf{f}(\mathbf{x}_{0})\in G$ linear approximierbar, dann ist das Kompositum $\mathbf{g}\circ\mathbf{f}$ in $\mathbf{x}_{0}$ ebenfalls linear approximierbar und es gilt

$$
\boxed {\mathcal {J} _ {\mathrm{gof}} (\mathbf {x} _ {0}) = \mathcal {J} _ {\mathrm{g}} (\mathbf {f} (\mathbf {x} _ {0})) \mathcal {J} _ {\mathrm{f}} (\mathbf {x} _ {0})} \tag {5}
$$

Beweis. Unter den Voraussetzungen folgt aus (1)

$$
\begin{array}{l} \mathbf {g} (\mathbf {f} (\mathbf {x})) = \mathbf {g} (\mathbf {f} (\mathbf {x} _ {0})) + \mathcal {J} _ {\mathbf {g}} (\mathbf {f} (\mathbf {x} _ {0})) (\mathbf {f} (\mathbf {x}) - \mathbf {f} (\mathbf {x} _ {0})) + o (| \mathbf {f} (\mathbf {x}) - \mathbf {f} (\mathbf {x} _ {0}) |) \\ = \mathbf {g} (\mathbf {f} (\mathbf {x} _ {0})) + \mathcal {J} _ {\mathbf {g}} (\mathbf {f} (\mathbf {x} _ {0})) \mathcal {J} _ {\mathbf {f}} (\mathbf {x} _ {0}) (\mathbf {x} - \mathbf {x} _ {0}) + o (| \mathbf {x} - \mathbf {x} _ {0} |) . \\ \end{array}
$$

Also ist $\mathbf{g} \circ \mathbf{f}$ in $\mathbf{x}_0$ linear approximierbar und es gilt (5).

Anwendung: Basiswechsel. Wir legen im $\mathbb{R}^{n}$ ein neues Koordinatensystem $K = (P; \mathbf{b}_{1}, \mathbf{b}_{2}, \ldots, \mathbf{b}_{n})$ fest und wählen außerdem im $\mathbb{R}^{m}$ eine neue Basis $(\mathbf{w}_{1}, \ldots, \mathbf{w}_{m})$. Der Punkt $\mathbf{x} \in \mathbb{R}^{n}$ hat im Koordinatensystem $K$ den Koordinatenvektor $\mathbf{y}$, der durch

$$
\mathbf {x} = B \mathbf {y} + \mathbf {p} \tag {6}
$$

mit der orthogonalen $n \times n$-Matrix $B = (\mathbf{b}_1, \ldots, \mathbf{b}_n)$ und $\mathbf{p} = \overrightarrow{OP}$ bestimmt ist ($\rightarrow$ Kap. 6, 6.6). Analog hat ein Vektor $\mathbf{v} \in \mathbb{R}^m$ bezüglich der Basis ($\mathbf{w}_1, \ldots, \mathbf{w}_m$) den Koordinatenvektor $\mathbf{w} \in \mathbb{R}^m$, so daß

$$
\mathbf {v} = W \mathbf {w} \tag {7}
$$

mit der invertierbaren  $m \times m$ -Matrix  $W = (\mathbf{w}_{1}, \ldots, \mathbf{w}_{m})$ .

Eine Funktion $\mathbf{f}:\mathbb{R}^{n}\supset D\to\mathbb{R}^{m}$ besitzt nach diesem Koordinaten- und Basiswechsel eine andere Darstellung $\mathbf{g}:\mathbb{R}^{n}\supset D^{*}\to\mathbb{R}^{m}$: Setzt man $\mathbf{v}=\mathbf{f}(\mathbf{x})$, so ist $\mathbf{g}$ aus (6) und (7) implizit bestimmt durch

$$
\mathbf {v} = \mathbf {f} (\mathbf {x}) = \mathbf {f} (B \mathbf {y} + \mathbf {p}) = W \mathbf {w} = W \mathbf {g} (\mathbf {y}).
$$

---

§4. Vektorwertige Funktionen

421

Diese Gleichung ist nach $\mathbf{w} = \mathbf{g}(\mathbf{y})$ auflösbar, so daß

$$
\mathbf {y} \in D ^ {*} \Longleftrightarrow \mathbf {x} = B \mathbf {y} + \mathbf {p} \in D, \tag {8}
$$

$$
\mathbf {g} (\mathbf {y}) = W ^ {- 1} \mathbf {f} (B \mathbf {y} + \mathbf {p}).
$$

Mit der Kettenregel (5) und (3) folgt sofort

$$
\mathcal {J} _ {\mathrm{g}} (\mathbf {y} _ {0}) = W ^ {- 1} \mathcal {J} _ {\mathrm{f}} (\mathbf {x} _ {0}) B, \quad \mathbf {x} _ {0} = B \mathbf {y} _ {0} + \mathbf {p}. \tag {9}
$$

Bemerkung. Mit (8) und (9) lassen sich sehr leicht Eigenschaften einer Funktion f untersuchen, die unabhängig von den gewählten Koordinatensystemen im Argument- und im Bildraum sind. Hierzu gehören die Stetigkeit, die Differenzierbarkeit und geometrische Eigenschaften von Gradient und  $J_{f}$  ( $\rightarrow$  4.3).

4.3 Räumliche Skalaren- und Vektorfelder. Der Anschauungsraum wird, wie üblich, nach Wahl eines kartesischen Koordinatensystems  $I = (O; \mathbf{e}_{1}, \mathbf{e}_{2}, \mathbf{e}_{3})$  durch  $R^{3}$  und jeder räumliche Bereich durch eine Teilmenge  $D \subseteq R^{3}$  dargestellt, wobei Punkte durch ihre Ortsvektoren charakterisiert werden. ( $\rightarrow$  Vereinbarung zu Beginn Kap. 7)

Ein Skalarenfeld (eine Belegungsfunktion) $f: \mathbb{R}^3 \supseteq D \to \mathbb{R}$ ordnet jedem Punkt $\mathbf{x} \in D$ eine Zahl $f(\mathbf{x})$ zu. Unter einem (räumlichen) Vektorfeld verstehen wir eine Funktion $\mathbf{v}: D \to \mathbb{R}^3$, die jedem Punkt $\mathbf{x} \in D$ einen Vektor $\mathbf{v}(\mathbf{x})$ zuordnet. Man stellt sich vor, daß in jedem Punkt $\mathbf{x} \in D$ der Vektor $\mathbf{v}(\mathbf{x})$ (etwa ein Kraftvektor oder ein Geschwindigkeitsvektor) angeheftet ist.

Eine Kurve in $D$ heißt Feldlinie des Vektorfeldes $\mathbf{v}$, wenn der Vektor $\mathbf{v}(\mathbf{x})$ in jedem Kurvenpunkt $\mathbf{x}$ parallel zur Kurventangente ist. Wir sprechen von einem $C^r$-Skalarenfeld $f$ bzw. $C^r$-Vektorfeld $\mathbf{v}$ auf $D$, wenn $f$ bzw. $\mathbf{v}$ $C^r$-Funktion, d.h. $r$-mal stetig partiell differenzierbar sind.

![](../../raw/pages_0417-0448/images/page_436_image_11.jpg)

<details>
<summary>text_image</summary>

v(x)
x
</details>

Abb. 191 - Vektorfeld, Feldlinien

## Beispiel 1. Die starre Drehung.

Eine Rechtsdrehung mit konstanter Winkelgeschwindigkeit ω um eine Achse durch den Nullpunkt mit Richtungsvektor  $\mathbf{a} = (a_{1}, a_{2}, a_{3})^{T}$ ,  $|a| = 1$ , wird nach Kap. 6, 6.4 dargestellt durch

$$
\begin{array}{l} \mathbf {x} (t) = (\cos \omega t) \mathbf {x} _ {0} + \\ + (1 - \cos \omega t) (\mathbf {x} _ {0} \cdot \mathbf {a}) \mathbf {a} + \\ + \sin \omega t \mathbf {a} \times \mathbf {x} _ {0}, \\ \end{array}
$$

![](../../raw/pages_0417-0448/images/page_436_image_16.jpg)

<details>
<summary>text_image</summary>

v(x)
x
</details>

Abb. 192 - Starre Drehung

---

422

7. Funktionen in mehreren Variablen. Teil 1: Differentiation

wobei  $x_{0}$  die Lage zur Zeit t = 0 bezeichnet.

Für die Geschwindigkeit $\mathbf{v}(t)=\dot{\mathbf{x}}(t)$ gilt demnach

$$
\mathbf {v} (t) = \omega (- \sin \omega t \mathbf {x} _ {0} + \sin \omega t (\mathbf {x} _ {0} \cdot \mathbf {a}) \mathbf {a} + \cos \omega t \mathbf {a} \times \mathbf {x} _ {0}) = \omega \mathbf {a} \times \mathbf {x} (t).
$$

Man nennt $\mathbf{w} = \omega\mathbf{a}$ die vektorielle Winkelgeschwindigkeit. Damit hat das Geschwindigkeitsfeld einer gleichförmigen Drehbewegung die Darstellung

$$
\mathbf {v} (\mathbf {x}) = \mathbf {w} \times \mathbf {x} = \omega \mathbf {a} \times \mathbf {x}. \tag {10}
$$

$\mathbf{x} \mapsto \mathbf{v}(\mathbf{x}) = \omega \mathbf{a} \times \mathbf{x}$ ist eine lineare Abbildung $\mathbf{x} \mapsto V\mathbf{x}$ mit konstanter Matrix $V \in \mathbb{R}^{3 \times 3}$, daher gilt ($\rightarrow$ (3) und Kap. 6, 6.1)

$$
\mathcal {J} _ {\mathbf {v}} (\mathbf {x}) = V = (\mathbf {v} (\mathbf {e} _ {1}), \mathbf {v} (\mathbf {e} _ {2}), \mathbf {v} (\mathbf {e} _ {3})) = \omega \left( \begin{array}{c c c} 0 & - a _ {3} & a _ {2} \\ a _ {3} & 0 & - a _ {1} \\ - a _ {2} & a _ {1} & 0 \end{array} \right) .
$$

Offensichtlich ist $V$ schiefsymmetrisch ($V^{T} = -V$). Daher ist insbesondere Spur $\mathcal{J}_{\mathbf{v}}(\mathbf{x}) = 0$ und damit $\operatorname{div}\mathbf{v} = 0$ für alle $\mathbf{x} \in \mathbb{R}^{3}$ ($\rightarrow 4.4$).

## Beispiel 2. Das zentrale Kraftfeld.

Eine Punktmasse M im Ursprung zieht (nach NEWTON) die Punktmasse m in  $X = (x_{1}, x_{2}, x_{3})$ ,  $x = \overrightarrow{OX}$ , mit der Gravitationskraft

$$
\mathbf {K} (\mathbf {x}) = \frac {c}{| \mathbf {x} | ^ {3}} \mathbf {x}, \quad \mathbf {x} \neq \mathbf {0},
$$

an  $(c = -\gamma mM, \gamma > 0)$ .

Handelt es sich in O und X um elektrische Ladungen der Stärke Q bzw. q, so gilt (nach COULOMB) für die elektrische Anziehungskraft dieselbe Gesetzmäßigkeit mit c = kqQ, k > 0.

![](../../raw/pages_0417-0448/images/page_437_image_15.jpg)

<details>
<summary>text_image</summary>

V(X)
X
</details>

Abb. 193 - Zentralfeld

Das zentrale Kraftfeld $\mathbf{K}(\mathbf{x})$ ist quasilinear ($\rightarrow$ Bsp. 3, 4.1), daher ergibt sich mit Ableitungsregel (4c) und der Einheitsmatrix $E \in \mathbb{R}^{3 \times 3}$ für $\mathbf{x} \neq \mathbf{0}$

$$
\begin{array}{l} \mathcal {J} _ {\mathbf {K}} (\mathbf {x}) = \mathbf {x} \left(\operatorname{grad} \frac {c}{| \mathbf {x} | ^ {3}}\right) ^ {T} + \frac {c}{| \mathbf {x} | ^ {3}} E = \frac {c}{| \mathbf {x} | ^ {5}} \left[ (\mathbf {x} ^ {T} \mathbf {x}) E - 3 \mathbf {x x} ^ {T} \right] \\ = \frac {c}{| \mathbf {x} | ^ {5}} \left( \begin{array}{c c c} x _ {2} ^ {2} + x _ {3} ^ {2} - 2 x _ {1} ^ {2} & - 3 x _ {1} x _ {2} & - 3 x _ {1} x _ {3} \\ - 3 x _ {1} x _ {2} & x _ {1} ^ {2} + x _ {3} ^ {2} - 2 x _ {2} ^ {2} & - 3 x _ {2} x _ {3} \\ - 3 x _ {1} x _ {3} & - 3 x _ {2} x _ {3} & x _ {1} ^ {2} + x _ {2} ^ {2} - 2 x _ {3} ^ {2} \end{array} \right)  . \\ \end{array}
$$

$\mathcal{J}_{\mathbf{K}}(\mathbf{x})$ ist stets eine symmetrische Matrix mit $\operatorname{Spur} \mathcal{J}_{\mathbf{K}}(\mathbf{x}) = 0$ ($\rightarrow 4.4$).

□

---

§4. Vektorwertige Funktionen

423

## Beispiel 3. Der magnetische Wirbel.

Ein gerader stromdurchflossener Draht hat die Richtung der  $e_{3}$ -Achse. Nach AMPÈRE bildet sich das magnetische Feld

$$
\mathbf {H} (\mathbf {x}) = \frac {c}{| \mathbf {x} | ^ {2} - (\mathbf {e} _ {3} \cdot \mathbf {x}) ^ {2}} \mathbf {e} _ {3} \times \mathbf {x}
$$

$$
= \frac {c}{x _ {1} ^ {2} + x _ {2} ^ {2}} \left( \begin{array}{c} - x _ {2} \\ x _ {1} \\ 0 \end{array} \right) ,
$$

$$
(x _ {1}, x _ {2}) \neq (0, 0), c > 0.
$$

![](../../raw/pages_0417-0448/images/page_438_image_7.jpg)

<details>
<summary>text_image</summary>

x
V(x)
</details>

Abb. 194 - Magnetischer Wirbel

Dieses Feld ist wieder quasilinear (→ Bsp. 3, 4.1) und mit der Ableitungsregel (4c) ergibt sich

$$
\mathcal {J} _ {\mathbf {H}} (\mathbf {x}) = \frac {c}{(x _ {1} ^ {2} + x _ {2} ^ {2}) ^ {2}} \left( \begin{array}{c c c} 2 x _ {1} x _ {2} & x _ {2} ^ {2} - x _ {1} ^ {2} & 0 \\ x _ {2} ^ {2} - x _ {1} ^ {2} & - 2 x _ {1} x _ {2} & 0 \\ 0 & 0 & 0 \end{array} \right)  .
$$

Obwohl die Feldlinien wie in Bsp. 1 Kreise sind, ist $\mathcal{J}_{\mathbf{H}}(\mathbf{x})$ hier eine symmetrische Matrix, d.h. für $(x_{1}, x_{2}) \neq (0, 0)$ ist $\operatorname{rot} \mathbf{H}(\mathbf{x}) = \mathbf{0} (\rightarrow 4.4)$. Außerdem ist für $(x_{1}, x_{2}) \neq (0, 0)$ Spur $J_{\mathbf{H}}(\mathbf{x}) = 0$, d.h. $\operatorname{div} \mathbf{H}(\mathbf{x}) = 0$.

## Beispiel 4. Die laminare Rohrströmung.

Eine zähe Flüssigkeit wird durch ein zur  $x_{2}$ -Achse koaxiales Rohr vom Radius r mit geringer Geschwindigkeit gepreßt, so daß eine laminare Strömung eintritt. Das Geschwindigkeitsfeld wurde unabhängig voneinander um 1850 von dem deutschen

![](../../raw/pages_0417-0448/images/page_438_image_14.jpg)

<details>
<summary>text_image</summary>

X
v(x)
</details>

Abb. 195 Rohrströmung

Ingenieur G. HAGEN und dem französischen Arzt POISEUILLE bestimmt zu

$$
\mathbf {v} (x _ {1}, x _ {2}, x _ {3}) = c \left( \begin{array}{c} 0 \\ r ^ {2} - x _ {1} ^ {2} - x _ {3} ^ {2} \\ 0 \end{array} \right), \qquad x _ {1} ^ {2} + x _ {3} ^ {2} \leq r ^ {2}, c > 0.
$$

Die Jacobi-Matrix berechnen wir direkt:

$$
\mathcal {J} _ {\mathbf {v}} (\mathbf {x}) = c \left( \begin{array}{c c c} 0 & 0 & 0 \\ - 2 x _ {1} & 0 & - 2 x _ {3} \\ 0 & 0 & 0 \end{array} \right), \qquad x _ {1} ^ {2} + x _ {3} ^ {2} \leq r ^ {2}.
$$

$\mathcal{J}_{\mathbf{v}}(\mathbf{x})$  ist i.a. weder symmetrisch noch schiefsymmetrisch, jedoch ist mit Spur  $J_{v}=0$  auch hier div v=0 ( $\rightarrow4.4$ ). ☐

---

424

7. Funktionen in mehreren Variablen. Teil 1: Differentiation

4.4 Gradient, Divergenz, Rotation, Laplace-Operator. Jedem $\mathscr{C}^{1}$-Skalarenfeld $f: \mathbb{R}^{3} \supseteq D \to \mathbb{R}$ wird das Vektorfeld „Gradient“ zugeordnet

$$
\operatorname{grad} f: D \to \mathbb {R} ^ {3}, \quad \operatorname{grad} f (\mathbf {x}) := \left( \begin{array}{c} \frac {\partial f}{\partial x _ {1}} (\mathbf {x}) \\ \frac {\partial f}{\partial x _ {2}} (\mathbf {x}) \\ \frac {\partial f}{\partial x _ {3}} (\mathbf {x}) \end{array} \right),
$$

jedem $\mathcal{C}^2$-Skalarenfeld $f : \mathbb{R}^3 \supseteq D \to \mathbb{R}$ mit dem Laplace-Operator $\Delta$, J.S. LAPLACE (1749 - 1827), das Skalarenfeld $\Delta f$:

$$
\Delta f: D \to \mathbb {R}, \qquad \Delta f (\mathbf {x}) = \frac {\partial^ {2} f}{\partial x _ {1} ^ {2}} (\mathbf {x}) + \frac {\partial^ {2} f}{\partial x _ {2} ^ {2}} (\mathbf {x}) + \frac {\partial^ {2} f}{\partial x _ {3} ^ {2}} (\mathbf {x}).
$$

Zu jedem $\mathcal{C}^{1}$-Vektorfeld $\mathbf{v} : \mathbb{R}^{3} \supseteq D \to \mathbb{R}^{3}$ definiert man ein Skalarenfeld „Divergenz“ div $\mathbf{v}$ und ein Vektorfeld „Rotation“ rot $\mathbf{v}$:

$$
\begin{array}{l}\operatorname{div} \mathbf {v}: D \rightarrow \mathbb {R}, \operatorname{div} \mathbf {v} (\mathbf {x}) = \frac {\partial v _ {1}}{\partial x _ {1}} (\mathbf {x}) + \frac {\partial v _ {2}}{\partial x _ {2}} (\mathbf {x}) + \frac {\partial v _ {3}}{\partial x _ {3}} (\mathbf {x})\\\operatorname{rot} \mathbf {v}: D \rightarrow \mathbb {R} ^ {3}, \operatorname{rot} \mathbf {v} (\mathbf {x}) = \left(\begin{array}{c}\frac {\partial v _ {3}}{\partial x _ {2}} (\mathbf {x}) - \frac {\partial v _ {2}}{\partial x _ {3}} (\mathbf {x})\\\frac {\partial v _ {1}}{\partial x _ {3}} (\mathbf {x}) - \frac {\partial v _ {3}}{\partial x _ {1}} (\mathbf {x})\\\frac {\partial v _ {2}}{\partial x _ {1}} (\mathbf {x}) - \frac {\partial v _ {1}}{\partial x _ {2}} (\mathbf {x})\end{array}\right).\end{array}\tag {11}
$$

Mittels Volumen- und Oberflächenintegrale zeigt man (→ Kap. 8), daß div v die „Quelldichte von v“ und rot v die „Wirbeldichte von v“ beschreibt.

Beispiele. Für die Vektorfelder der 4 Beispiele aus 4.3 gilt

|  | Starre Drehung | Zentrales Kraftfeld |
| --- | --- | --- |
| $\mathbf{v}(x)$ | $\omega \mathbf{a} \times \mathbf{x}$ | $c\|\mathbf{x}\|^{-3}\mathbf{x}$, $\mathbf{x} \neq 0$ |
| $\text{div } \mathbf{v}(\mathbf{x})$ | 0 | 0, $\mathbf{x} \neq 0$ |
| $\text{rot } \mathbf{v}(\mathbf{x})$ | $2\omega \mathbf{a}$ | 0, $\mathbf{x} \neq 0$ |

<table><tr><td></td><td colspan="2">Magnetischer Wirbel</td><td>Laminare Rohrströmung</td></tr><tr><td> $\mathbf{v}(\mathbf{x})$ </td><td colspan="2"> $\frac{c}{x_1^2 + x_2^2} \begin{pmatrix} -x_2 \\ x_1 \\ 0 \end{pmatrix}, x_1^2 + x_2^2 \neq 0$ </td><td> $c \begin{pmatrix} 0 \\ r^2 - x_1^2 - x_3^2 \\ 0 \end{pmatrix}, x_1^2 + x_3^2 \leq r^2$ </td></tr><tr><td>div  $\mathbf{v}(\mathbf{x})$ </td><td colspan="2">0,  $x_1^2 + x_2^2 \neq 0$ </td><td>0,  $x_1^2 + x_3^2 \leq r^2$ </td></tr><tr><td>rot  $\mathbf{v}(\mathbf{x})$ </td><td colspan="2">0,  $x_1^2 + x_2^2 \neq 0$ </td><td> $2c \begin{pmatrix} x_3 \\ 0 \\ -x_1 \end{pmatrix}, x_1^2 + x_3^2 \leq r^2$ </td></tr></table>

---

§4. Vektorwertige Funktionen

425

Sämtliche 4 Vektorfelder sind in ihrem Definitionsbereich quellfrei (div v = 0). Für die starre Drehung hat rot v(x) in jedem x konstant die Richtung der Drehachse und den Betrag 2ω. Der magnetische Wirbel und das zentrale Kraftfeld sind in x ≠ 0, die Rohrströmung nur längs der Rohrachse wirbelfrei. □

![](../../raw/pages_0417-0448/images/page_440_image_3.jpg)

<details>
<summary>natural_image</summary>

Geometric diagram showing a circle with eight smaller circles and an arrow indicating rotation or transformation (no text or symbols)
</details>

Abb. 196a - Starre Drehung |rot v| = 2ω

![](../../raw/pages_0417-0448/images/page_440_image_5.jpg)

<details>
<summary>natural_image</summary>

Pure geometric diagram with concentric circles and arrows, no text or symbols present
</details>

Abb. 196b - Magn.Wirbel |rot v| = 0, x ≠ 0

Bereits die Darstellung der Felder $f$, $\mathbf{v}$ hängt vom gewählten Koordinatensystem ab, aber noch vielmehr die durch partielle Ableitungen gewonnenen Felder grad $f$, $\Delta f$, div $\mathbf{v}$ und rot $\mathbf{v}$.

Im folgenden soll gezeigt werden, daß in einem festen Punkt X der Wert von div v und  $\Delta f$  sowie die durch grad f und rot v dargestellten Vektoren unabhängig vom gewählten kartesischen Koordinatensystem I sind.

Dazu die Darstellung mit der Jacobi-Matrix:

$$
\begin{array}{c} \text {grad} f (\mathbf {x} _ {0}) = \mathcal {J} _ {f} (\mathbf {x} _ {0}) ^ {T} \\ \text {div} \mathbf {v} (\mathbf {x} _ {0}) = \text {Spur} \mathcal {J} _ {\mathbf {v}} (\mathbf {x} _ {0}) \\ (\text {rot} \mathbf {v} (\mathbf {x} _ {0})) \times (\mathbf {x} - \mathbf {x} _ {0}) = [ \mathcal {J} _ {\mathbf {v}} (\mathbf {x} _ {0}) - \mathcal {J} _ {\mathbf {v}} (\mathbf {x} _ {0}) ^ {T} ] (\mathbf {x} - \mathbf {x} _ {0}). \end{array} \tag {12}
$$

Beweis. Die beiden ersten Beziehungen liest man direkt aus den Definitionen ab. Die dritte folgt aus der Tatsache, daß $S = A - A^{T}$ für jede quadratische Matrix $A$ schiefsymmetrisch ist $(S^{T} = -S)$ und für jedes $S \in \mathbb{R}^{3 \times 3}$ gilt

$$
S ^ {T} = - S \iff S = \left( \begin{array}{c c c} 0 & s _ {1 2} & s _ {1 3} \\ - s _ {1 2} & 0 & s _ {2 3} \\ - s _ {1 3} & - s _ {2 3} & 0 \end{array} \right) \iff S \mathbf {x} = \mathbf {w} \times \mathbf {x} \text {mit} \mathbf {w} = \left( \begin{array}{c} - s _ {2 3} \\ s _ {1 3} \\ - s _ {1 2} \end{array} \right).
$$

Mit $S = A - A^{T}$ ist $\mathbf{w} = \begin{pmatrix} a_{32} - a_{23} \\ a_{13} - a_{31} \\ a_{21} - a_{12} \end{pmatrix}$, so daß $\mathbf{w} = \operatorname{rot}\mathbf{v}(\mathbf{x}_0)$ für $A = \mathcal{J}_{\mathbf{v}}(\mathbf{x}_0)$ folgt.

Wegen (10) beschreibt $\mathbf{x} \mapsto S\mathbf{x} = \mathbf{w} \times \mathbf{x}$ das Geschwindigkeitsfeld einer Drehung, daher der Name „Rotation“.

Da die Zerlegung  $A = \frac{1}{2}(A + A^{T}) + \frac{1}{2}(A - A^{T})$  einer Matrix in den symmetrischen und den schiefsymmetrischen Anteil eindeutig ist, nennt man das Drehfeld

$$
\mathbf {x} \mapsto \frac {1}{2} (\operatorname{rot} \mathbf {v} (\mathbf {x} _ {0})) \times \mathbf {x}
$$

den „Rotationsanteil der linearen Approximation $\mathbf{x} \mapsto \mathcal{J}_{\mathbf{v}}(\mathbf{x}_0)\mathbf{x}^{\prime\prime}$.

---

426

7. Funktionen in mehreren Variablen. Teil 1: Differentiation

## Satz 4.2. Transformationsformeln.

Sind $I = (O; \mathbf{e}_1, \mathbf{e}_2, \mathbf{e}_3)$, $K = (P; \mathbf{b}_1, \mathbf{b}_2, \mathbf{b}_3)$ zwei kartesische Koordinatensysteme im Raum und ist $\mathbf{p} = \overrightarrow{OP} \in \mathbb{R}^3$, $B = (\mathbf{b}_1, \mathbf{b}_2, \mathbf{b}_3) \in \mathbb{R}^{3 \times 3}$ die Darstellung von $K$ bezüglich $I$, so gilt

<table><tr><td>System</td><td>I</td><td>K</td></tr><tr><td>Basis</td><td> $E = (\mathbf{e}_1, \mathbf{e}_2, \mathbf{e}_3)$ </td><td> $B = (\mathbf{b}_1, \mathbf{b}_2, \mathbf{b}_3), \quad B^T = B^{-1}$ </td></tr><tr><td>Punkt X</td><td> $\mathbf{x}^T = (x_1, x_2, x_3)$ </td><td> $\mathbf{y}^T = (y_1, y_2, y_3) = (\mathbf{x}^T - \mathbf{p}^T)B$ </td></tr><tr><td>Vektor  $\overrightarrow{XY}$ </td><td> $\mathbf{v}$ </td><td> $\mathbf{w} = B^T \mathbf{v}$ </td></tr><tr><td rowspan="2">Skalarenfeld $f : D \to \mathbb{R}$ </td><td> $f(\mathbf{x})$ </td><td> $g(\mathbf{y}) = f(B\mathbf{y} + \mathbf{p})$ </td></tr><tr><td> $\mathcal{J}_f(\mathbf{x})$ </td><td> $\mathcal{J}_g(\mathbf{y}) = \mathcal{J}_f(\mathbf{x})B$ </td></tr><tr><td>Gradient</td><td> $\text{grad } f(\mathbf{x}) = \mathcal{J}_f(\mathbf{x})^T$ </td><td> $\text{grad } g(\mathbf{y}) = B^T \text{grad } f(\mathbf{x})$ </td></tr><tr><td rowspan="2">Vektorfeld $\mathbf{v} : D \to \mathbb{R}^3$ </td><td> $\mathbf{v}(\mathbf{x})$ </td><td> $\mathbf{w}(\mathbf{y}) = B^T \mathbf{v}(B\mathbf{y} + \mathbf{p})$ </td></tr><tr><td> $\mathcal{J}_\mathbf{v}(\mathbf{x})$ </td><td> $\mathcal{J}_\mathbf{w}(\mathbf{y}) = B^T \mathcal{J}_\mathbf{v}(\mathbf{x})B$ </td></tr><tr><td>Divergenz</td><td> $\text{div } \mathbf{v}(\mathbf{x})$ </td><td> $\text{div } \mathbf{w}(\mathbf{y}) = \text{div } \mathbf{v}(\mathbf{x})$ </td></tr><tr><td>Rotation</td><td> $\text{rot } \mathbf{v}(\mathbf{x})$ </td><td> $\text{rot } \mathbf{w}(\mathbf{y}) = B^T \text{rot } \mathbf{v}(\mathbf{x})$ </td></tr></table>

Beweis. Bis auf die Divergenz und Rotation folgt alles aus den Formeln (6) - (9). Dazu setze man beim Skalarfeld $m = 1$ und $W = 1$ und beim Vektorfeld $m = n$ und $W = B$.

$$
\operatorname{div} \mathbf {w} (\mathbf {y}) = \operatorname{Spur} \mathcal {J} _ {\mathbf {w}} (\mathbf {y}) = \operatorname{Spur} (B ^ {T} \mathcal {J} _ {\mathbf {v}} (\mathbf {x}) B) = \operatorname{Spur} \mathcal {J} _ {\mathbf {v}} (\mathbf {x}) = \operatorname{div} \mathbf {v} (\mathbf {x}).
$$

(Spur A ist die Summe der Eigenwerte von A,  $B^{T}AB$  und A haben die gleichen Eigenwerte, → Kap. 6, 6.7.)

$$
\begin{array}{l} \left(\operatorname{rot} \mathbf {w} (\mathbf {y})\right) \times \mathbf {z} = \left(\mathcal {J} _ {\mathbf {w}} (\mathbf {y}) - \mathcal {J} _ {\mathbf {w}} (\mathbf {y}) ^ {T}\right) \mathbf {z} = \left[ B ^ {T} \left(\mathcal {J} _ {\mathbf {v}} (\mathbf {x}) - \mathcal {J} _ {\mathbf {v}} (\mathbf {x}) ^ {T}\right) B \right] \mathbf {z} \\ = B ^ {T} \left[ \operatorname{rot} \mathbf {v} (\mathbf {x}) \times (B \mathbf {z}) \right] = \left(B ^ {T} \operatorname{rot} \mathbf {v} (\mathbf {x})\right) \times (B ^ {T} B \mathbf {z}) \\ = \left(B ^ {T} \operatorname{rot} \mathbf {v} (\mathbf {x})\right) \times \mathbf {z}. \\ \end{array}
$$

$(B^{T}$ ist eine Drehmatrix, daher gilt $B^{T}(\mathbf{a}\times \mathbf{b}) = (B^{T}\mathbf{a})\times (B^{T}\mathbf{b}).$

Folgerung: Koordinateninvarianz. Der Wert von div v(x) ist unabhängig vom Koordinatensystem, in dem man v darstellt und die partiellen Ableitungen berechnet. Dasselbe gilt für die Richtung und die Länge von rot v(x) und grad v(x).

Unter geeigneten Differenzierbarkeitsvoraussetzungen bestätigt man leicht durch explizites Nachrechnen die

---

§4. Vektorwertige Funktionen

427

## Rechenregeln:

a) rot(grad f) = 0 „Gradientenfeld ist wirbelfrei“,
b) div(rot v) = 0 „Feld der Rotation ist quellfrei“,
c) $\operatorname{div}(\operatorname{grad} f) = \Delta f$,
d) $\operatorname{div}(f\mathbf{v}) = (\operatorname{grad} f) \cdot \mathbf{v} + f \operatorname{div} \mathbf{v}$,
e) $\operatorname{rot}(f\mathbf{v}) = (\operatorname{grad} f) \times \mathbf{v} + f \operatorname{rot}\mathbf{v}$,
f) rot(rot v) = grad(div v) - Δv (Laplace - Operator komponentenweise).

Beispiel. Nach J.C. MAXWELL gilt im Vakuum für die (zeitabhängige) elektrische Feldstärke  $\mathbf{E}(\mathbf{x},t)$  und die magnetische Feldstärke  $\mathbf{H}(\mathbf{x},t)$  (SI-Einheiten mit den Feldkonstanten  $\mu_{0}=0.4\pi\cdot10^{-6}$  H/m,  $\epsilon_{0}=8.854\cdot10^{-12}$  F/m)

$$
\mu_ {0} \frac {\partial \mathbf {H}}{\partial t} = - \operatorname{rot} \mathbf {E}, \qquad \epsilon_ {0} \frac {\partial \mathbf {E}}{\partial t} = \operatorname{rot} \mathbf {H}, \qquad \operatorname{div} \mathbf {E} = 0, \qquad \operatorname{div} \mathbf {H} = 0.
$$

Diese vier partiellen Differentialgleichungen beschreiben die zeitabhängige Koppelung zwischen den Feldern E und H. Sind  $\mathbf{E}(\mathbf{x},t)$  und  $\mathbf{H}(\mathbf{x},t)$  beide  $C^{2}$ -Vektorfelder, so kann man mit Rechenregel f) und dem Satz von Schwarz je eine Differentialgleichung für E und H alleine herleiten:

$$
\mu_ {0} \operatorname{rot} \frac {\partial \mathbf {H}}{\partial t} = \operatorname{rot} (- \operatorname{rot} \mathbf {E}) = - \big (\operatorname{grad} (\operatorname{div} \mathbf {E}) - \Delta \mathbf {E} \big) = \Delta \mathbf {E},
$$

andererseits ist mit  $c_{0}=\frac{1}{\sqrt{\mu_{0}\epsilon_{0}}}$  (Lichtgeschwindigkeit im Vakuum)

$$
\frac {\partial}{\partial t} \frac {\partial \mathbf {E}}{\partial t} = \frac {1}{\epsilon_ {0}} \frac {\partial}{\partial t} \operatorname{rot} \mathbf {H} = \frac {1}{\epsilon_ {0}} \operatorname{rot} \frac {\partial \mathbf {H}}{\partial t} = c _ {0} ^ {2} \Delta \mathbf {E}.
$$

Analog ergibt sich für $\mathbf{H}:\frac{\partial^{2}\mathbf{H}}{\partial t^{2}}=c_{0}^{2}\Delta\mathbf{H}$. D.h. jede Komponente von $\mathbf{E}$ und $\mathbf{H}$ erfüllt die 3-dimensionale Wellengleichung (Elektromagnetische Wellen)

$$
\frac {\partial^ {2} u}{\partial t ^ {2}} = c _ {0} ^ {2} \left(\frac {\partial^ {2} u}{\partial x _ {1} ^ {2}} + \frac {\partial^ {2} u}{\partial x _ {2} ^ {2}} + \frac {\partial^ {2} u}{\partial x _ {3} ^ {2}}\right).
$$

Mit dem symbolischen Vektor („Nabla-Operator“) $\nabla := \begin{pmatrix} \frac{\partial}{\partial x_1} \\ \frac{\partial}{\partial x_2} \\ \frac{\partial}{\partial x_3} \end{pmatrix}$

lassen sich die vier Felder formal als Produkte schreiben

$$
\mathrm{grad} f = \nabla f, \quad \Delta f = \nabla \cdot \nabla f,
$$

$$
\mathrm{div} \mathbf {v} = \nabla \cdot \mathbf {v}, \quad \mathrm{rot} \mathbf {v} = \nabla \times \mathbf {v}.
$$

Beim Umgang mit ∇ ist jedoch Vorsicht geboten, man kann mit diesem formalen Vektor wegen der Produktregel der Differentiation nicht immer so rechnen, wie mit „echten“ Vektoren (→ Aufg. 5).

---

428

7. Funktionen in mehreren Variablen. Teil 1: Differentiation

## Aufgaben

1. Gegeben ist die Abbildung $\mathbf{f}:\mathbb{R}^{2}\setminus\{\mathbf{0}\}\to\mathbb{R}^{2}$

$$
\mathbf {f} (\mathbf {x}) = \binom{u (x, y)}{v (x, y)} = \frac {1}{x ^ {2} + y ^ {2}} \binom{x}{y}, \quad \mathbf {x} \neq \mathbf {0}.
$$

a) Für welche Punkte x ist  $\mathbf{f}(\mathbf{x}) = \mathbf{x}$  (Fixpunkte)?
b) Man berechne die Jacobi-Matrix $\mathcal{J}_{\mathrm{f}}$. In welchen Punkten $\mathbf{x}$ ist $\mathcal{J}_{\mathrm{f}}$ invertierbar.

2. Gegeben sind vier Geschwindigkeitsfelder im  $R^{2}$  ( $r = \sqrt{x^{2} + y^{2}}$ )

$$
\mathbf {v} (\mathbf {x}) = (u (x, y), v (x, y)) ^ {T} \quad (c, \epsilon , M \text {   konstant   })
$$

- laminar, translatorisch : u = c ; v = 0 ;
- laminare Gegenströmung :  $u = c \cdot y$ ; v = 0 ;
- isolierte Quelle : $u = \epsilon \frac{x}{x^2 + y^2}$; $v = \epsilon \frac{y}{x^2 + y^2}$ ($r > 0$);
- Dipolströmung : $u = M \frac{y^2 - x^2}{(x^2 + y^2)^2}$; $v = -M \frac{2xy}{(x^2 + y^2)^2}$ ($r > 0$);

a) Man skizziere jeweils das Vektorfeld samt einigen Stromlinien.
b) Man berechne $\mathcal{J}_{\mathbf{v}}$, div $\mathbf{v}$, rot $\mathbf{v}$.

3. Gegeben sind die Vektorfelder im $\mathbb{R}^3$

a) $\mathbf{v}(\mathbf{x}) = 2xy\mathbf{e}_1 + (3z^3 +x^2)\mathbf{e}_2 + 9yz^2\mathbf{e}_3$
b) $\mathbf{v}(\mathbf{x}) = \frac{1}{|\mathbf{x}|^3}\mathbf{e}_1 - \frac{3x}{|\mathbf{x}|^5}\mathbf{x} \quad (\mathbf{x} \neq \mathbf{0})$.

Man berechne $\mathcal{J}_{\mathbf{v}}$, div $\mathbf{v}$ und rot $\mathbf{v}$.

4. In kartesischen Koordinaten ist im $\mathbb{R}^3$

$$
\mathbf {f} (\mathbf {x}) = (x ^ {2}, y ^ {2}, - x z) ^ {T}, \quad \mathbf {g} (\mathbf {x}) = (- y, x, 0) ^ {T}.
$$

Man berechne  $\nabla(\mathbf{f} \cdot \mathbf{g})$ ,  $\nabla \cdot (\mathbf{f} \times \mathbf{g})$  und  $\nabla \times (\mathbf{f} \times \mathbf{g})$ .

5. Für zwei  $C^{1}$ -Vektorfelder f, g im  $R^{3}$  hat man mit der „Nabla-Schreibweise“

$$
\mathrm{div} (\mathbf {f} \times \mathbf {g}) = \nabla \cdot (\mathbf {f} \times \mathbf {g}).
$$

Wendet man die Regeln für das Spatprodukt an, so hätte man formal die Beziehung

$\nabla\cdot(\mathbf{f}\times\mathbf{g})=\mathbf{g}\cdot(\nabla\times\mathbf{f})=-\mathbf{f}\cdot(\nabla\times\mathbf{g})$ ,

$$
\mathrm{div} (\mathbf {f} \times \mathbf {g}) = \mathbf {g} \cdot \mathrm{rot} \mathbf {f} = - \mathbf {f} \cdot \mathrm{rot} \mathbf {g}.
$$

Wie lautet die richtige Formel, die div(f × g) über die Rotation von f und g ausdrückt?

6. Gegeben sind im  $R^{2}$  mit den kartesischen Koordinaten  $(x, y)$

die Transformation von Polar- auf kartesische Koordinaten $u: (r, \varphi) \mapsto (x, y)$,

die Kurve  $\gamma(t):\mathbb{R}\to\mathbb{R}^{2}$  mit der Darstellung  $(r,\varphi)=(t^{2},\omega t)$  in Polarkoordinaten, das Skalarenfeld  $s:\mathbb{R}^{2}\to\mathbb{R}$  mit  $s(x,y)=x^{2}-y^{2}$ .

Man berechne

- die Jacobi-Matrizen $\mathcal{J}_{\gamma} = \dot{\gamma}$, $\mathcal{J}_u$ und $\mathcal{J}_s = (\text{grad } s)^T$,
- die explizite Darstellung von $s \circ u \circ \gamma$ und daraus direkt $\frac{d}{dt} s \circ u \circ \gamma$,
- mittels Kettenregel die Jacobi-Matrix von $(s\circ u)$ und $\frac{d}{dt}s\circ u\circ \gamma$

---

§4. Vektorwertige Funktionen

429

\- die Richtungsableitung von $s$ in Transversalrichtung $\mathbf{v} = \mathbf{e}_{\varphi} = (-\sin \varphi, \cos \varphi)^T$ im Kurvenpunkt $\gamma\left(\frac{\pi}{4\omega}\right)$.

7. Man berechne div grad U und rot grad U für die skalaren Felder im  $R^{3}$

a)  $U(\mathbf{x}) = z e^{x^{2} y}$ ,
b) $U(\mathbf{x}) = \frac{\mathbf{p} \cdot \mathbf{x}}{|\mathbf{x}|^3}, \mathbf{x} \neq \mathbf{0}$ (Dipolpotential mit Achsenrichtung $\mathbf{p} \in \mathbb{R}^3$).

8. Ein gerader prismatischer Stab der Länge $L$ aus elastischem homogenen Werkstoff hat als Querschnitt ein gleichseitiges Dreieck $A$ mit der Höhe $h$. Der Schwerpunkt des Stabes liegt im Koordinatenursprung (vgl. Skizze). Der Stab wird längs $z$ um den Winkel $\varphi$ verdrillt. Ein Punkt $(x,y,z)$ mit $|z|\ll\frac{L}{\varphi}$ hat nach der Torsion in guter Näherung die Koordinaten $\mathbf{x}^{*}=\mathbf{F}(\mathbf{x})$ mit

$$
x ^ {*} = x - \frac {\varphi}{L} y z
$$

(F) $y^{*} = y + \frac{\varphi}{L}xz$

$$
z ^ {s} = z + \frac {\varphi}{2 L h} (3 y ^ {2} x - x ^ {3}).
$$

![](../../raw/pages_0417-0448/images/page_444_image_11.jpg)

<details>
<summary>text_image</summary>

h
A
L
y
x
φ
z
</details>

Den Verformungszustand beschreibt das Vektorfeld der Verschiebungen $\mathbf{v}=\mathbf{x}^{*}-\mathbf{x}$:

$(I^{\prime})$ $\mathbf{v} = \mathbf{v}(\mathbf{x}) = \mathbf{F}(\mathbf{x}) - \mathbf{x}$

a) In welche Flächen verwölben sich die ebenen Schnitte $x = 0$ bzw. $z = 0$ durch die „Torsion“ F (gefragt ist die Gleichung $f(x^{*}, y^{*}, z^{*}) = 0$ und der Name des Flächentyps)? Welche Punkte in den Schnitten bleiben fest?
b) Man berechne die Funktionalmatrizen $\mathcal{J}_{\mathrm{F}}(\mathbf{x})$ und $\mathcal{J}_{\mathrm{v}}(\mathbf{x})$ und $\operatorname{div}\mathbf{v}(\mathbf{x})$, $\operatorname{rot}\mathbf{v}(\mathbf{x})$.
c) Man berechne (jeweils als Funktion von x):

den Verzerrungstensor :  $V_{\nu} = \frac{1}{2}(\mathcal{J}_{\nu} + \mathcal{J}_{\nu}^{T})$ ;

den Rotationstensor :  $R_{v} = \frac{1}{2}(\mathcal{J}_{v} - \mathcal{J}_{v}^{T})$ ;

den Spannungstensor :  $S_{v} = 2G V_{v}$ ,

(G bezeichnet den Schubmodul) ;

die Spannungsvektoren in A :  $\mathbf{p}_{A}=S,\begin{pmatrix}0\\ 1\end{pmatrix}$ .

9. Man rechne explizit für zwei Vektorfelder $\mathbf{v}(\mathbf{x}),\mathbf{w}(\mathbf{x})\in\mathcal{C}^{1}(\mathbb{R}^{3},\mathbb{R}^{3})$ nach:

$$
\boxed {\mathrm{grad} (\mathbf {v} \cdot \mathbf {w}) = \mathcal {J} _ {\mathbf {v}} ^ {T} \mathbf {w} + \mathcal {J} _ {\mathbf {w}} ^ {T} \mathbf {v}.}
$$

Zur Kontrolle setze man  $\mathbf{v}=(x,-y,xz)^{T}$  und  $\mathbf{w}=(z^{2}-y^{2},x^{2}-z^{2},y^{2}-x^{2})^{T}$ .
