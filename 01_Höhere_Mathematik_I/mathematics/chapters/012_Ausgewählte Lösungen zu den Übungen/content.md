# Ausgewählte Lösungen zu den Übungen

原始 PDF 第 233–240 页。

# Anhang B

# Ausgewählte Lösungen zu den Übungen

## B.1 Die reellen Zahlen

## B.1.1 Eine axiomatische Beschreibung der reellen Zahlen

Beweis von Satz 1.2.3 (i). Der Beweis für (i) ist analog zu dem für (ii): Schritt 1: Hier zeigen wir, dass es mindestens eine Zahl x gibt, so dass

$$
a + x = b. \tag {B.1.1}
$$

Der natürliche „Kandidat“ ist  $x := -a + b$ . Wir rechnen

$$
\begin{array}{l} a + x \quad = \quad a + (- a + b) \\ \stackrel {(\mathrm{A} 2)} {=} (a - a) + b \\ \stackrel {(\mathrm{A} 4)} {=} \quad 0 + b \\ \stackrel {(\mathrm{A} 1)} {=} b + 0 \\ \stackrel {(\mathrm{A} 3)} {=} b. \\ \end{array}
$$

Also löst $x$ die Gleichung (B.1.1).

Schritt 2: Hier zeigen wir, dass es maximal eine solche Zahl gibt. Angenommen, x und  $\tilde{x}$  sind zwei Lösungen von (B.1.1).

$$
\begin{array}{l} a + x = a + \tilde {x} \\ \Rightarrow \quad (a + x) - a = a + \tilde {x} - a \\ \stackrel {(\mathrm{A} 1)} {\Rightarrow} \quad (x + a) - a = (\tilde {x} + a) - a \\ \stackrel {(\mathrm{A} 2)} {\Rightarrow} \quad x + (a - a) = \tilde {x} + (a - a) \\ \stackrel {(\mathrm{A} 4)} {\Rightarrow} \quad x + 0 = \tilde {x} + 0 \\ \stackrel {(\mathrm{A} 3)} {\Rightarrow} \quad x = \tilde {x}. \\ \end{array}
$$

□

---

HMI ETech/Phys

WS 2021-22

Seite 228

## B.1.2 Einige Elementare Ungleichungen

Lösung zur Übung 1.5.3. Bei 2% Wertverlust im Jahr hat man nach n Jahren mit einem Anfangskapital von 1000 €

$$
1 0 0 0 \cdot (1 - 0. 0 2) ^ {n} \stackrel {\text {Satz 1.5.2}} {\geq} 1 0 0 0 \cdot (1 - n \cdot 0. 0 2) = 1 0 0 0 - 2 0 \cdot n
$$

Unser Kapital soll auf jeden Fall nicht weniger als 500 € betragen, also immer größer gleich 500 € sein.

$$
1 0 0 0 - 2 0 \cdot n \geq 5 0 0 \Leftrightarrow n \leq 2 5
$$

Also halten wir einen jährlichen Werteverlust von 2% mindestens 25 Jahren durch. Da nun hier das n sehr groß ist, können wir uns denken, dass die Approximation keine besonders gute Approximation ist. Tatsächlich ergibt eine genaue Rechnung  $n \geq \log(0,5)/\log(0,98) \approx 34$ .

## B.2 Allgemeine Konvergenz und Divergenz

Lösung zur Übung 4.2.9.

Zu (i): Aus der Definition 4.2.1 folgt sofort, dass $\{a_n - a\}_{n=1}^{\infty}$ eine Nullfolge ist, die nach Satz 4.1.7 beschränkt ist. Das heißt, es existiert $s$ und $\sigma$, so dass

$$
\sigma \leq a _ {n} - a \leq s \quad \text { für   alle } n \in \mathbb {N}.
$$

Daraus folgt die Beschränktheit:

$$
\sigma + a \leq a _ {n} \leq s + a \quad \text {fur alle} n \in \mathbb {N}.
$$

Zu (ii): Der Beweis ist ähnlich. Nach Satz 4.1.7 ist

$$
\{\alpha (a _ {n} - a) + \beta (b _ {n} - b) \} _ {n = 1} ^ {\infty} = \{\alpha a _ {n} + \beta b _ {n} - (\alpha a + \beta b) \} _ {n = 1} ^ {\infty}
$$

eine Nullfolge. Nach Definition 4.2.1 ist somit $\{\alpha a_n + \beta b_n\}_{n=1}^{\infty}$ konvergent mit Grenzwert $\alpha a + \beta b$.

Zu (iii): Für den Grenzwert von  $\{|a_{n}|\}_{n=1}^{\infty}$  nutzen wir die umgekehrte Dreiecksungleichung um zu zeigen, dass  $\{|a_{n}|-|a|\}_{n=1}^{\infty}$  eine Nullfolge ist. Mit der Definition dieser folgt dann sofort die Aussage. Sei  $\varepsilon>0$  gegeben, so folgt aus der Vorraussetzung, dass es ein  $N\in N$  gibt, so dass  $|a_{n}-a|<\varepsilon$  für alle n>N und damit ist

$$
\left| \left| a _ {n} \right| - \left| a \right| \right| \leq \left| a _ {n} - a \right| <   \varepsilon \quad \text { für   alle } n > N.
$$

Also ist $\{|a_n| - |a|\}_{n=1}^{\infty}$ eine Nullfolge, was zu zeigen war.

Für den Grenzwert von  $\{\sqrt{|a_{n}|}\}_{n=1}^{\infty}$  sei  $a\neq0$ , für a=0 haben wir die Relation schon in 4.1.7 gezeigt. Wie eben, sei  $\varepsilon>0$  gegben, wir wählen N sodass  $|a_{n}-a|<\sqrt{|a|}\cdot\varepsilon$  für

---

HMI ETech/Phys

WS 2021-22

Seite 229

alle n > N, was nach Vorraussetzung möglich ist. Damit ist

$$
\left| \sqrt {| a _ {n} |} - \sqrt {| a |} \right| = \left| \frac {\left(\sqrt {| a _ {n} |} - \sqrt {| a |}\right) \left(\sqrt {| a _ {n} |} + \sqrt {| a |}\right)}{\sqrt {| a _ {n} |} + \sqrt {| a |}} \right| = \left| \frac {| a _ {n} | - | a |}{\sqrt {| a _ {n} |} + \sqrt {| a |}} \right| <   \epsilon .
$$

Im letzten Schritt haben wir  $\sqrt{|a_{n}|}$  weggestrichen, da es positiv ist. Somit wird der Gesamtausdruck größer, wenn wir einen Term aus dem Nenner wegstreichen.

Zu (iv): Die Folge

$$
\begin{array}{l} \{(a _ {n} - a) \cdot (b _ {n} - b) \} _ {n = 1} ^ {\infty} = \{a _ {n} \cdot b _ {n} - a _ {n} \cdot b - b _ {n} \cdot a + a \cdot b \} _ {n = 1} ^ {\infty} \\ = \{a _ {n} \cdot b _ {n} - a _ {n} \cdot b + a \cdot b - a \cdot b - b _ {n} \cdot a + a \cdot b \} _ {n = 1} ^ {\infty} \\ = \{a _ {n} \cdot b _ {n} + (a - a _ {n}) \cdot b + (b - b _ {n}) \cdot a - a \cdot b \} _ {n = 1} ^ {\infty} \\ \end{array}
$$

ist nach Satz 4.1.7 eine Nullfolge.

Nach Definition 4.2.1 ist somit $\{a_n \cdot b_n + (a - a_n) \cdot b + (b - b_n) \cdot a\}_{n=1}^{\infty}$ konvergent mit Grenzwert $a \cdot b$.

Da  $\{(a-a_{n})\cdot b\}_{n=1}^{\infty}$  und  $\{(b-b_{n})\cdot a\}_{n=1}^{\infty}$  nach Vorraussetzung mit 4.1.7 Nullfolgen sind, folgt sofort mit (ii) die zu zeigende Eigenschaft (iv).

Zu (v): Nach Satz 4.1.7 ist  $\{(a_{n}-a)\cdot c_{n}\}_{n=1}^{\infty}$  eine Nullfolge, somit beschränkt. Da die Summe zweier beschränkter Folgen beschränkt ist (was wir gleich zeigen) und  $\{a\cdot c_{n}\}_{n=1}^{\infty}$  offenbar beschränkt ist, folgt, dass  $\{a\cdot c_{n}\}_{n=1}^{\infty}$  beschränkt ist.

$$
\sigma_ {d} <   d _ {n} <   s _ {d} \quad \text { für   alle } n \in \mathbb {N}
$$

$$
\sigma_ {e} <   e _ {n} <   s _ {e} \quad \text {fur alle} n \in \mathbb {N}
$$

Daraus folgt sofort, dass die Folge der Summanden  $\{d_{n}+e_{n}\}_{n=1}^{\infty}$  durch  $\sigma_{d}+\sigma_{e}$  und  $s_{d}+s_{e}$  beschränkt ist.

Zu (vi): Die Konvergenz zeigen wir wie bei den Beweisen zu (iii). Sei $\varepsilon > 0$ gegeben. Wir wählen $N \in \mathbb{N}$, so dass $|a_n - a| < \min\left\{\frac{a^2}{2} \cdot \epsilon, \frac{|a|}{2}\right\}$ für alle $n > N$

$$
\left| \frac {1}{a _ {n}} - \frac {1}{a} \right| = \left| \frac {a - a _ {n}}{a \cdot a _ {n}} \right| <   \left| \frac {a - a _ {n}}{a \cdot (a - a / 2)} \right| = \left| \frac {2 (a - a _ {n})}{a ^ {2}} \right| <   \epsilon .
$$

![](../../raw/pages_0225-0240/images/page_234_image_17.jpg)

Lösung zur Übung 4.2.10. Wir setzen

$$
x _ {n} := \sqrt [ n ]{n}.
$$

---

HMI ETech/Phys

WS 2021-22

Seite 230

Aus

$$
(x _ {n}) ^ {n} = n
$$

folgt  $x_{n} > 1$  für n > 1. Also können wir  $x_{n} = 1 + h_{n}$  für  $h_{n} > 0$  schreiben. Dann ist in der Gleichung

$$
n = (1 + h _ {n}) ^ {n}
$$

jeder Term in der binomischen Erweiterung der rechten Seite positiv. Insbesondere gilt

$$
n > \binom{n}{2} h _ {n} ^ {2} = \frac {n (n - 1)}{2} h _ {n} ^ {2}.
$$

Aus

$$
0 <   h _ {n} <   \frac {2}{n - 1}
$$

und dem Vergleichskriterium folgt

$$
h _ {n} \rightarrow 0 \quad \text {und somit} \quad \sqrt [ n ]{n} = 1 + h _ {n} \rightarrow 1 \quad \text {für} n \rightarrow \infty .
$$

## B.3 Grenzwerte und Stetigkeit reeller Funktionen

## B.3.1 Grenzwerte von Funktionen

Lösung zur Übung 5.1.5. Nach Definition 5.1.1 konvergiert die auf V definierte Funktion  $g(x)$  genau dann gegen  $y_{0}$  in  $x_{0}$ , wenn für jede Folge  $\{x_{n}\}_{n=1}^{\infty}$  mit

$$
x _ {n} \neq x _ {0}, \quad x _ {n} \in V, \quad \lim _ {n \to \infty} x _ {n} = x _ {0} \tag {B.3.1}
$$

$\lim_{n\to \infty}g(x_n) = y_0$ ist. Sei nun eine beliebige Folge $\{x_{n}\}_{n = 1}^{\infty}$ gegeben, die diese Vorraussetzungen (B.3.1) erfüllt. Da $f,g,h$ nach Vorraussetzung auf einer Umgebung $V$ von $x_0$ definiert sind, $f(x)\leq g(x)\leq h(x)$ für alle $x$ aus $V$ ist und jedes Folgenglied $x_{n}\in V$ ist, gilt

$$
f (x _ {n}) \leq g (x _ {n}) \leq h (x _ {n})
$$

für alle Folgenglieder  $x_{n}$ . Nun folgt mit der Vorraussetzung  $\lim_{x\to x_{0}}f(x)=\lim_{x\to x_{0}}h(x)=y_{0}$ , dass

$$
\lim _ {n \to \infty} f (x _ {n}) = \lim _ {n \to \infty} h (x _ {n}) = y _ {0}.
$$

---

HMI ETech/Phys

WS 2021-22

Seite 231

Nach dem Sandwichkriterium für Folgen 4.2.7 ist auch $\lim_{n\to \infty}g(x_n) = y_0$. Somit konvergiert $g(x_{n})$ für die gewählte Folge. Da diese beliebig war, konvergiert $g(x_{n})$ für alle Folgen mit (B.3.1) gegen $y_0$.

Lösung zur Übung 5.3.11. Wir definieren $f(x) := \sin(1/x) - \exp(-x)$ und bemerken, dass sie stetig auf $(0, \infty)$ (aber nicht auf $[0, \infty)$) ist. Dann suchen wir zwei Punkte, zwischen denen wir eine Nullstelle “einklammern” (also, finden) können. In $x = 1/\pi$ gilt

$$
f (1 / \pi) = \sin (\pi) - \exp (- 1 / \pi) = - \exp (- 1 / \pi) <   0. \tag {B.3.2}
$$

Jetzt brauchen wir einen Punkt, wo die Funktion positiv ist. In  $4/\pi$  berechnen wir

$$
f (4 / \pi) = \sin (\pi / 4) - \exp (- 4 / \pi). \tag {B.3.3}
$$

Wir schätzen nach oben mit

$$
\exp (- 4 / \pi) <   \exp (- 1) = \frac {1}{e} <   \frac {1}{2}
$$

ab. Ersetzen in (B.3.3) ergibt

$$
f (4 / \pi) \geq \frac {1}{\sqrt {2}} - \frac {1}{2} > 0. \tag {B.3.4}
$$

Da $f$ auf $[1/\pi, 4/\pi]$ stetig ist und (B.3.2), (B.3.4) erfüllt, liefert der Zwischenwertsatz Existenz eines Punktes $x_* \in [1/\pi, 4/\pi]$ wo $f(x_*) = 0$.

## B.4 Unendliche Reihen

## B.4.1 Potenzreihen

Lösung zur Übung 7.4.3. Gefordert ist eine Abschätzung für

$$
| e ^ {x} - (x + 1) |
$$

auf $x \in (0, \frac{1}{2})$.

Zunächst betrachten wir das Taylorpolynom erster Ordnung von  $\exp(\cdot)$  in Punkt  $x_{0}=0$ , welches mit Definition 7.4.1 wie folgt ist:

$$
T _ {1} (x; 0) = 1 + x
$$

Da die $\exp (\cdot)$ Funktion auf $\mathbb{R}$ unendlich oft stetig differenzierbar ist, was aus Beispiel

---

HMI ETech/Phys

WS 2021-22

Seite 232

② aus Kapitel 6.3 sowie Übung 5.2.3 folgt, können wir Satz 7.4.2 anwenden:

$$
R _ {1} (x; 0) = \frac {e ^ {c}}{2} x ^ {2} \quad \text {mit} c \in [ 0, x ] \text {und} x \in \left(0, \frac {1}{2}\right)
$$

Somit ist

$$
| e ^ {x} - (x + 1) | = \left| 1 + x + \frac {e ^ {c}}{2} x ^ {2} - (x + 1) \right| = \left| \frac {e ^ {c}}{2} x ^ {2} \right| <   \frac {\sqrt {e}}{8}.
$$

Dabei haben wir im letzten Schritt benutzt, dass die  $\exp(\cdot)$  Funktion sowie das Monom  $x^{2}$  streng monoton steigend auf  $(0,\frac{1}{2})$  sind. ☐

## B.5 Lineare Algebra

## B.5.1 Einleitung und erste Definition

Lösung zur Übung 8.1.14.

① Wir stellen fest, dass

$$
\binom{1}{1} \quad \text {und} \quad \binom{1}{0}
$$

nach Definition 8.1.5 linear unabhänging sind. Nach lemma 8.1.13 bilden sie eine Basis von $\mathbb{R}^2$. Da wir in der zu finden Basis den Vektor $(1,0)^T$ darstellen wollen, ist es nur sinnvoll, mit diesem die Basis zu bilden, also

$$
\underline {{v}} = \binom{1}{0}.
$$

Nun ist die Darstellung von  $\begin{pmatrix}1\\0\end{pmatrix}$  in dieser Basis einfach  $\begin{pmatrix}0\\1\end{pmatrix}$ . Natürlich ist diese Lösung nicht eindeutig!

② Wir denken wieder an die Definition 8.1.5 und suchen einen weiteren, linear unabhängigen Vektor. Da wir an einer möglichst einfachen Lösung interessiert sind, stellen wir fest, dass mit $\underline{v}_3 = (1,0,0)^T$ die Vektoren $\underline{v}_1$, $\underline{v}_2$ und $\underline{v}_3$ linear unabhängig sind.

Sei nun  $\underline{x}=(x_{1},x_{2},x_{3})^{T}\in\mathbb{R}$  gegeben. Wir suchen  $\alpha_{1},\alpha_{2}$  und  $\alpha_{3}$ , so dass:

$$
\underline {{x}} = \alpha_ {1} \underline {{v}} _ {1} + \alpha_ {2} \underline {{v}} _ {2} + \alpha_ {3} \underline {{v}} _ {3} = \alpha_ {1} \left( \begin{array}{c} 1 \\ 1 \\ 1 \end{array} \right) + \alpha_ {2} \left( \begin{array}{c} 3 \\ 0 \\ 2 \end{array} \right) + \alpha_ {3} \left( \begin{array}{c} 1 \\ 0 \\ 0 \end{array} \right)
$$

---

HMI ETech/Phys

WS 2021-22

Seite 233

Die Lösung lässt sich nun leicht ablesen:

$$
\alpha_ {1} = x _ {2}, \alpha_ {2} = \frac {x _ {3} - x _ {2}}{2} \text {und} \alpha_ {3} = x _ {1} - x _ {2} - 3 \frac {x _ {3} - x _ {2}}{2} = x _ {1} + \frac {x _ {2}}{2} - \frac {3}{2} x _ {3}.
$$

## B.5.2 Lineare Abbildung

Lösung zur Übung 8.2.3. Dass $B_{L} \subseteq W$ folgt aus der Definition von Bild. Dass $\underline{0} \in B_{L}$ folgt aus Linearität, da

$$
L (\underline {{0}}) = L (0 \underline {{v}} _ {1} + 0 \underline {{v}} _ {2}) = 0 L (\underline {{v}} _ {1}) + 0 L (\underline {{v}} _ {2}) = 0 \quad \text {fur alle} \underline {{v}} _ {1}, \underline {{v}} _ {2} \in V. \tag {B.5.1}
$$

Andererseits, wenn  $\underline{a},\underline{b}\in B_{L}$ , dann gibt es  $\underline{v}_{1},\underline{v}_{2}\in V$  so dass

$$
L (\underline {{v}} _ {1}) = \underline {{a}}, \qquad L (\underline {{v}} _ {2}) = \underline {{b}}.
$$

Für beliebige $\alpha, \beta \in \mathbb{R}$ folgt, dass

$$
L (\alpha \underline {{v}} _ {1} + \beta \underline {{v}} _ {2}) = \alpha L (\underline {{v}} _ {1}) + \beta L (\underline {{v}} _ {2}) = \alpha \underline {{a}} + \beta \underline {{b}}.
$$

Also ist $\alpha\underline{a} +\beta\underline{b}\in B_{L}$. Somit haben wir gezeigt, dass $B_{L}$ ein Teilraum von $W$ ist.

Jetzt wenden wir und  $K_{L}$  zu. Analog folgt aus der Definition von Kern, dass  $K_{L} \subseteq V$ . Dass  $0 \in K_{L}$  folgt aus (B.5.1), oben. Schließlich bemerken wir, dass für  $c, d \in K_{L}$  gilt

$$
L (\underline {{c}}) = \underline {{0}}, \qquad L (\underline {{d}}) = \underline {{0}},
$$

und somit gilt für beliebige  $\alpha, \beta \in R$ , dass

$$
L (\alpha \underline {{c}} + \beta \underline {{d}}) = \alpha L (\underline {{c}}) + \beta L (\underline {{d}}) = \alpha \underline {{0}} + \beta \underline {{0}} = \underline {{0}}.
$$

Also ist $\alpha\underline{c} +\beta\underline{d}\in K_{L}$. Damit haben wir gezeigt, dass $K_{L}$ ein Teilraum von $V$ ist. $\square$

Lösung zur Übung 8.2.7. Man prüft leicht nach, dass V ein Vektorraum über R ist. Als Nächstes müssen wir zeigen, dass P eine lineare Abbildung ist. Dazu sei  $\alpha_{1}, \alpha_{2} \in R, v_{1}, v_{2} \in V$ .

$$
\begin{array}{l} P (\alpha_ {1} v _ {1} + \alpha_ {2} v _ {2}) (x) = \frac {\alpha_ {1} v _ {1} (x) + \alpha_ {2} v _ {2} (x) + \alpha_ {1} v _ {1} (- x) + \alpha_ {2} v _ {2} (- x)}{2} \\ = \alpha_ {1} \frac {v _ {1} (x) + v _ {1} (- x)}{2} + \alpha_ {2} \frac {v _ {2} (x) + \alpha_ {2} v _ {2} (- x)}{2} \\ = \alpha_ {1} P (v _ {1}) (x) + \alpha_ {2} P (v _ {2}) (x). \\ \end{array}
$$

---

HMI ETech/Phys

WS 2021-22

Seite 234

Nun bleibt noch zu zeigen, dass  $P^{2}=P$  ist. Dazu sei  $v\in V$ . Wir wenden P zweimal an:

$$
\begin{array}{l} \left(P ^ {2} v\right) (x) = \left(P (P v)\right) (x) = P \left(\frac {v (x) + v (- x)}{2}\right) = \frac {\frac {v (x) + v (- x)}{2} + \frac {v (- x) + v (- (- x))}{2}}{2} \\ = \frac {v (x) + v (- x)}{2} = (P v) (x). \\ \end{array}
$$

Damit ist gezeigt, dass P eine Projektion ist.

## B.5.3 Lineare Gleichungssysteme

Teillösung zur Übung 8.4.6. Bild( $\underline{A}$ ) ist

$$
\mathrm{Sp} \left\{\left( \begin{array}{c} 1 \\ 0 \\ - 1 \end{array} \right), \left( \begin{array}{c} 0 \\ 1 \\ - 1 \end{array} \right) \right\}.
$$

![](../../raw/pages_0225-0240/images/page_239_image_9.jpg)
