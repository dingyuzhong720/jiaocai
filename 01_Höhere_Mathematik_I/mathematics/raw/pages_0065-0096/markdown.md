## Definition 3.4.6

Seien $p_n(x)$ und $q_m(x)$ Polynome von Grad $n$ bzw. $m$. Dann heißt

$$
R (x) = \frac {p _ {n} (x)}{q _ {m} (x)}
$$

eine rationale Funktion. Der Definitionsbereich von R ist  $\{x\in\mathbb{R}:q_{m}(x)\neq0\}$ .

Jetzt suchen wir eine äquivalente Darstellung von R in dem Fall m < n.

## Satz 3.4.7

Sei $R(x) = \frac{p_n(x)}{q_m(x)}$, wobei $p_n$ und $q_m$ Polynome vom Grad $n$ bzw. $m$ sind und $n \geq m$. Dann gibt es Polynome $s_{n-m}$ und $t_k$, so dass für alle $x \in \mathcal{D}(R)$ gilt

$$
R (x) = s _ {n - m} (x) + \frac {t _ {k} (x)}{q _ {m} (x)}. \tag {3.4.5}
$$

Die Funktion $t_k$ ist entweder identisch Null oder ein Polynom vom Grad $k < m$.

Beweis. Der übliche Divisions-Algorithmus ergibt

$$
\begin{array}{l} \frac {p _ {n} (x)}{q _ {m} (x)} = \frac {a _ {n} x ^ {n} + a _ {n - 1} x ^ {n - 1} + \dots + a _ {1} x + a _ {0}}{b _ {m} x ^ {m} + b _ {m - 1} x ^ {m - 1} + \dots + b _ {1} x + b _ {0}} \\ = \frac {a _ {n}}{b _ {m}} x ^ {n - m} + \frac {t _ {n - 1} (x)}{q _ {m} (x)}, \tag {3.4.6} \\ \end{array}
$$

wobei

$$
t _ {n - 1} (x) = p _ {n} (x) - \frac {a _ {n}}{b _ {m}} x ^ {n - m} q _ {m} (x)
$$

vom Grad kleiner gleich n-1 ist, weil der n-te Term verschwindet. Dies wiederholt man, bis der Grad des Zählerpolynoms in (3.4.6) kleiner gleich dem Grad des Nennerpolynoms ist (also, maximal  $n-m+1$  mal). ☐

## Beispiel. Schreiben Sie

$$
R (x) = \frac {x ^ {3} + x}{x - 1}
$$

in der Form (3.4.5). Zeichnen Sie den Graphen der Funktion.

Lösung. Man erhält

$$
R (x) = x ^ {2} + x + 2 + \frac {2}{x - 1}.
$$

Für die Parabel zeichnet man

![](images/page_65_chart_4.jpg)

<details>
<summary>contour</summary>

| X | Y |
| --- | --- |
| -3 | ~8 |
| -2 | ~5.5 |
| -1 | ~2.5 |
| 0 | 2 |
| 1 | ~5.5 |
| 2 | ~8 |
</details>

Für den Restterm zeichnet man in Schritten:

![](images/page_65_chart_6.jpg)

<details>
<summary>contour</summary>

| X | Y |
| --- | --- |
| -2 | -4 |
| -1 | -1 |
| 0 | 4 |
| 1 | 1 |
| 2 | ~0.5 |
</details>

![](images/page_65_chart_7.jpg)

<details>
<summary>contour</summary>

| X | Y (Curve 1) | Y (Curve 2) |
| --- | --- | --- |
| 0 | — | -1 |
| 1 | 4 | — |
| 2 | ~1.2 | — |
| 3 | ~0.6 | — |
| 0 | — | -1 |
| 1 | — | -1 |
| 2 | — | ~-2.5 |
| 3 | — | ~-4 |
</details>

![](images/page_65_chart_8.jpg)

<details>
<summary>contour</summary>

| X | Y |
| --- | --- |
| ~1.5 | 4 |
| ~2.0 | ~2.5 |
| ~2.5 | ~1.5 |
| ~3.0 | 1 |
</details>

Die Summe ergibt:

![](images/page_65_chart_10.jpg)

<details>
<summary>contour</summary>

| X | Y |
| --- | --- |
| -1 | 0 |
| 0 | 0 |
| 1 | ~-3.5 |
</details>

Man erkennt  $\mathcal{D}(R)=\mathbb{R}\setminus\{1\}$  und  $\mathcal{W}(R)=\mathbb{R}$ .

![](images/page_65_image_12.jpg)

## 3.5 Trigonometrische Funktionen

Wir erinnern an die Funktionen

$$
\sin (x) = b, \quad \cos (x) = a, \quad \tan (x) = \frac {\sin (x)}{\cos (x)},
$$

wobei  $(a,b)$  ein Punkt des Einheitskreises ist und x der Winkel gegen den Uhrzeigersinn zwischen der x-Achse und dem Segment von  $(0,0)$  bis  $(a,b)$  ist.

![](images/page_66_image_7.jpg)

<details>
<summary>text_image</summary>

(a,b)
y
x
(0,0)
(1,0)
</details>

Wir werden ab und zu die folgenden Eigenschaften brauchen:

- $\sin (0) = 0$, $\cos (0) = 1$,
- $|\sin (x)|\leq 1$ , $|\cos (x)|\leq 1$
- sin ist ungerade, cos ist gerade,
- sin und cos sind periodisch mit Periode $2\pi$,
- $\sin^2 (x) + \cos^2 (x) = 1$,
- $\cos (x) = 1 - 2\sin^2\left(\frac{x}{2}\right)$,
- $\sin (x\pm y) = \sin (x)\cos (y)\pm \cos (x)\sin (y),$
- $\cos (x) = \sin \left(\frac{\pi}{2} - x\right)$, $\sin (x) = \cos \left(\frac{\pi}{2} - x\right)$,
- $0 < x \cos(x) < \sin(x) < x$ für $x \in (0, \frac{\pi}{2}]$.

Man definiert Arkussinus und Arkuscosinus,

$$
\arcsin : [ - 1, 1 ] \to [ - \pi / 2, \pi / 2 ] \quad \arccos : [ - 1, 1 ] \to [ 0, \pi ],
$$

als die Umkehrfunktionen von $\sin : [-\pi / 2, \pi / 2] \to [-1, 1]$ bzw. $\cos : [0, \pi] \to [-1, 1]$.

## Kapitel 4

## Zahlenfolgen

Wir werden oft mit Zahlenfolgen arbeiten müssen. Außerdem werden wir Folgen als Werkzeug benutzen, z.B. um den Grenzwert einer Funktion zu definieren.

## 4.1 Einleitung

Was ist eine Folge? Eine Folge ist eine Funktion auf N oder auf einer unendlichen Teilmenge davon.

## Definition 4.1.1

Eine auf N oder auf einer unendlichen Teilmenge von N definierte reellwertige Funktion heißt Zahlenfolge oder Folge. Statt  $n \mapsto f(n)$  schreiben wir für das Bild  $f(n)$  von n meistens  $a_{n}$ . Für  $a_{1}, a_{2}, a_{3}, \ldots$  schreiben wir auch  $\{a_{n}\}_{n=1}^{\infty}$ . Die Werte  $a_{n}$  heißen Folgenglieder.

Es ist unerheblich, dass die Nummerierung mit 1 beginnt.  $a_{5}, a_{7}, a_{12}, \ldots$  ist ebenfalls eine Folge. Wie wir schon bemerkt haben, können Folgen explizit oder rekursiv definiert werden. Als Beispiel betrachten wir

$$
a _ {n} := (- 1) ^ {n} \frac {1}{2 n}, \quad n \in \mathbb {N} \quad (\text {explizit})
$$

$$
a _ {1} = 2, a _ {n} = \frac {1}{2} \left(a _ {n - 1} + \frac {2}{a _ {n - 1}}\right), \quad n = 2, 3, 4, \dots \quad (\text {rekursiv}).
$$

Wie andere Funktionen kann eine Folge monoton, beschränkt, usw. sein.

Beispiel. Ein Ball fällt aus der Höhe h auf einen Tisch und springt bis zur Höhe 0,9h zurück usw. Bestimme die jeweiligen Sprunghöhen und den Gesamtweg, den der Ball bis zum N-ten Auftreffen zurückgelegt hat. Man erhält

$$
a _ {n} = (0, 9) ^ {n} h, \quad n = 1, 2, \dots
$$

für die Sprunghöhe nach dem n-ten Auftreffen und

$$
b _ {1} = h, \quad b _ {n} = b _ {n - 1} + 2 \cdot (0, 9) ^ {n} h, \quad n = 2, 3, 4, \dots
$$

für die Länge des Gesamtwegs bis zum n-ten Auftreffen. Wir bemerken folgendes:

- $\{a_n\}_{n=1}^{\infty}$ ist streng monoton fallend, nach oben durch $h$ beschränkt, nach unten durch 0 beschränkt.
- $\{b_n\}_{n=1}^{\infty}$ ist streng monoton wachsend und nach unten durch $h$ beschränkt. Ist $\{b_n\}_{n=1}^{\infty}$ auch nach oben beschränkt? $Ja$, wie wir jetzt zeigen.

Lemma 4.1.2. Definiere $s_n := \sum_{k=0}^{n} r^k$ für alle $n \in \mathbb{N}$ und $r \in \mathbb{R}$. Dann ist die Folge $\{s_n\}$

- nach oben unbeschränkt für $r \geq 1$,
- beschränkt für $r \in (0,1)$ und es gilt

$$
s _ {n} = \frac {1 - r ^ {n + 1}}{1 - r}. \tag {4.1.1}
$$

Beweis. Für  $r \geq 1$  ist  $s_{n} \geq \sum_{k=0}^{n} 1^{k}$ , also reicht es aus, wenn wir zeigen, dass  $\sum_{k=0}^{n} 1^{k}$  nach oben unbeschränkt ist. Da  $\sum_{k=0}^{n} 1^{k} = \underbrace{1 + 1 + \ldots + 1}_{n+1 \text{ mal}} = n + 1$ , folgt dies aus der Unbeschränktheit von N. Für  $r \in (0,1)$  rechnen wir aus

$$
\begin{array}{l} s _ {n} = 1 + r + \dots + r ^ {n}, \\ r s _ {n} = \quad r + \dots + r ^ {n} + r ^ {n + 1}, \\ \end{array}
$$

so dass

$$
(1 - r) s _ {n} = 1 - r ^ {n + 1}.
$$

Dies entspricht (4.1.1). Aus den Ungleichungen $1 - r^{n+1} < 1$ und $1 - r > 0$ folgt außerdem

$$
s _ {n} <   \frac {1}{1 - r},
$$

sodass $s_n$ nach oben beschränkt ist. (Wichtig ist, dass die rechte Seite unabhängig von $n$ ist.) Aus (4.1.1) und $r^{n+1} \leq r$ für $r \in (0,1)$ schließen wir, dass

$$
s _ {n} \geq \frac {1 - r}{1 - r} = 1,
$$

so dass  $s_{n}$  nach unten durch 1 beschränkt ist. Also ist  $s_{n}$  beschränkt.

Frage: Was passiert, wenn $r \in (-1,0)$?

Die geometrische Reihe taucht in vielen Anwendungen auf. Monotone Folgen sind einfacher als nicht monotone Folgen, aber

$$
\begin{array}{l} a _ {n} = (- 1) ^ {n} \frac {1}{2 n}, \\ g _ {n} = (- 1) ^ {n} \left(\frac {9}{1 0}\right) ^ {n} \cdot h \\ \end{array}
$$

sind einfache Beispiele nicht monotoner Folgen. Man merkt sowohl für  $\{a_{n}\}_{n=1}^{\infty}$  als auch für  $\{g_{n}\}_{n=1}^{\infty}$ , dass die Folgenglieder sich immer mehr der Zahl x = 0 nähern. Diese Beispiele sind einfach wegen der Homogenität des Absolutbetrags (siehe Satz 1.4.2) und der Form der Folgen. Z.B. erhält man

$$
| a _ {n} | = | (- 1) ^ {n} | \left| \frac {1}{2 n} \right| = \frac {1}{2 n}.
$$

Den Begriff „sich an 0 zu nähern“ machen wir explizit in der folgenden Definition.

## Definition 4.1.3

Eine Folge $\{a_n\}_{n=1}^{\infty}$ reeller Zahlen heißt Nullfolge, wenn es zu jeder Zahl $\varepsilon > 0$ ein $N = N(\varepsilon)$ in $\mathbb{N}$ gibt, so dass

$$
| a _ {n} | \leq \varepsilon \quad \text { für   alle } n \geq N (\varepsilon).
$$

Wir sagen, die Folge hat den Grenzwert Null (oder: konvergiert gegen Null), und schreiben

$$
a _ {n} \to 0 \text {f ü r} n \to \infty \quad \text {oder} \quad \lim _ {n \to \infty} a _ {n} = 0.
$$

## Notation 4.1.4

Wenn man

$$
a _ {n} \uparrow 0 \quad \text {bzw.} \quad a _ {n} \downarrow 0
$$

schreibt, bedeutet es, dass  $\{a_{n}\}_{n=1}^{\infty}$  monoton wachsend bzw. monoton fallend gegen Null für  $n \to \infty$  konvergiert. Alternativ findet man die Notation

$$
a _ {n} \nearrow 0 \quad \text {bzw.} \quad a _ {n} \searrow 0.
$$

Bemerkung. Nach der Definition ist  $\{|a_{n}|\}_{n=1}^{\infty}$  eine Nullfolge genau dann, wenn  $\{a_{n}\}_{n=1}^{\infty}$  eine Nullfolge ist.

Bemerkung. Man denkt an $\varepsilon > 0$ sehr klein und erwartet, dass $N$ im Allgemeinen sehr groß gewählt werden muss. $\varepsilon > 0$ spielt die Rolle einer Fehlertoleranz. Diese ist das Input und wird gegeben. Zurückgeliefert wird ein passendes Output $N$, so dass der Fehler für alle zukünftigen Folgenglieder kleiner gleich der Toleranz ist.

Beispiel.  $c_{n} = 200 \left( \frac{9}{10} \right)^{n}, \varepsilon = 10^{-4}$ . Dann ist  $|c_{n}| \leq \varepsilon_{0}$  für alle  $n \geq 138$ . Also gibt man zurück N = 138.

Beispiel.

$$
a _ {1} = 1,
$$

$$
a _ {2} = 0,
$$

$$
a _ {3} = \frac {1}{4},
$$

$$
a _ {4} = 0,
$$

$$
a _ {5} = 0,
$$

$$
a _ {6} = \frac {1}{4},
$$

$$
a _ {7} = 0 u s w.
$$

Wie groß auch $N \in \mathbb{N}$ ist, gibt es ein $n \geq N$, so dass $a_{n} = \frac{1}{4}$ ist. Also ist $\{a_{n}\}_{n=1}^{\infty}$ keine Nullfolge.

Bemerkung. $Ob \{b_n\}_{n=1}^{\infty}$ eine Nullfolge ist, hat nur mit dem Verhalten für große $n$ zu tun.

$$
b _ {n} = \left\{ \begin{array}{c c} 1 0 0 0 0 \cdot 5 ^ {n} & n = 1, 2, \dots , 5 0 0 \\ \left(\frac {1}{5}\right) ^ {n} & n \geq 5 0 1 \end{array} \right.
$$

ist eine Nullfolge. Dass  $\{a_{n}\}_{n=1}^{\infty}$  eine Nullfolge ist, bedeutet insbesondere nicht, dass die Folgenglieder „klein sind“, sondern dass sie für n groß genug klein sind.

Beispiel. Bestimmen Sie, ob die folgenden Folgen gegen Null konvergieren oder nicht

(1) $a_{n} = \frac{1}{n}$,
(2) $b_{n} = b + (-1)^{n}b + \frac{1}{n},\quad b\in \mathbb{R},$
(3) $c_{n} = \sqrt{n + 1} -\sqrt{n}.$

Lösung. Zu (1): Sei $\varepsilon > 0$ (beliebig klein) gegeben. Wir definieren

$$
N := \left\lceil \frac {1}{\varepsilon} \right\rceil ,
$$

wobei für  $x \in R \lceil x \rceil$  die kleinste ganze Zahl größer gleich x bezeichnet. Da  $\varepsilon > 0$ , ist  $N \in N$ . Außerdem gilt

$$
n \geq \frac {1}{\varepsilon} \quad \text { für   alle } n \in \mathbb {N} \text { mit } n \geq N,
$$

so dass

$$
\frac {1}{n} \leq \varepsilon \quad \text {fur alle} n \in \mathbb {N} \text {mit} n \geq N,
$$

wie gewünscht.

Zu (2): Für $b = 0$ haben wir schon in (1) gezeigt, dass $\{b_n\}$ eine Nullfolge ist. Wir zeigen jetzt für $b \neq 0$, dass $\{b_n\}$ keine Nullfolge ist. Für $n$ gerade ist

$$
b _ {n} = 2 b + \frac {1}{n}.
$$

Wenn b > 0, dann setzen wir  $\varepsilon := 2b$ . Dann ist

$$
| b _ {n} | = b _ {n} = 2 b + \frac {1}{n} > \varepsilon \quad \text { für   alle   gerade } n \in \mathbb {N}.
$$

Wenn $b < 0$, dann setzen wir $\varepsilon := |b|$ Für $n \geq 1 / |b|$ und gerade gilt dann

$$
| b _ {n} | = 2 | b | - \frac {1}{n} \geq | b | \geq \varepsilon .
$$

Zu (3): Die „Idee“ ist, dass

$$
\sqrt {n + 1} \approx \sqrt {n} \quad \text {für $n$ groß,}
$$

so dass $\sqrt{n+1}-\sqrt{n}$ klein ist für $n$ groß. Diese Idee müssen wir irgendwie präzise machen. Der „Trick“, der hier nützlich ist, ist das Erweitern mit Eins:

$$
\begin{array}{l} 0 \leq c _ {n} = (\sqrt {n + 1} - \sqrt {n}) \cdot \frac {\sqrt {n + 1} + \sqrt {n}}{\sqrt {n + 1} + \sqrt {n}} \\ = \frac {1}{\sqrt {n + 1} + \sqrt {n}} <   \frac {1}{\sqrt {n}}. \tag {4.1.2} \\ \end{array}
$$

Sei $\varepsilon > 0$ gegeben. Wir wählen $N = \left\lceil \frac{1}{\varepsilon^2} \right\rceil$. Dann ist

$$
c _ {n} \stackrel {(4. 1. 2)} {\leq} \frac {1}{\sqrt {n}} \leq \frac {1}{\sqrt {N}} \leq \varepsilon \quad \text {for all} n \geq N.
$$

Also ist $\{c_n\}_{n=1}^{\infty}$ eine Nullfolge.

Wie im letzten Beispiel gesehen, hilft es oft, mit einer einfacheren Folge zu vergleichen.

## Satz 4.1.5: Vergleichskriterium für Nullfolgen

Seien $\{a_{n}\}_{n = 1}^{\infty},\{b_{n}\}_{n = 1}^{\infty}$ Zahlenfolgen mit

$$
| b _ {n} | \leq | a _ {n} | \tag {4.1.3}
$$

für alle $n \in \mathbb{N}$, die größer als eine feste Zahl $N_0$ sind. Wenn $a_n \to 0$ für $n \to \infty$, dann gilt auch $b_n \to 0$ für $n \to \infty$.

Beweis. Leichte Übung.

![](images/page_71_image_22.jpg)

## Definition 4.1.6

Wenn (4.1.3) gilt, dann nennen wir $\{a_n\}_{n=1}^{\infty}$ eine Majorante von $\{b_n\}_{n=1}^{\infty}$. Man sagt, dass $\{a_n\}_{n=1}^{\infty}$ die Folge $\{b_n\}_{n=1}^{\infty}$ majorisiert.

Beispiel. Zeigen Sie, dass  $\{\alpha^{n}\}_{n=1}^{\infty}$  für  $0 < |\alpha| < 1$  eine Nullfolge ist.

Lösung. Wir wenden die Bernoullische Ungleichung an. Da $|\alpha| \in (0,1)$, ist

$$
\frac {1}{| \alpha |} = 1 + h
$$

für ein geeignetes $h > 0$. Es folgt

$$
| \alpha | ^ {n} = \frac {1}{(1 + h) ^ {n}} \leq \frac {1}{1 + n h} \leq \frac {1}{n h}.
$$

$\mathrm{Da}\left\{\frac{1}{nh}\right\}_{n=1}^{\infty}$ eine Nullfolge ist, ist auch $\{| \alpha |^{n}\}_{n=1}^{\infty}$ eine Nullfolge und somit auch $\{\alpha^{n}\}_{n=1}^{\infty}$.

Nullfolgen besitzen folgende Eigenschaften:

## Satz 4.1.7: Eigenschaften von Nullfolgen

Seien $\{a_{n}\}_{n = 1}^{\infty}$, $\{b_n\}_{n = 1}^{\infty}$ Nullfolgen und $\{c_n\}_{n = 1}^{\infty}$ eine beschränkte Folge. Dann gilt

(i)  $\{a_{n}\}_{n=1}^{\infty}$  ist beschränkt,
(ii) $\{\alpha a_n + \beta b_n\}_{n=1}^{\infty}, \alpha, \beta \in \mathbb{R}$ ist eine Nullfolge,
$(iii)\left\{\sqrt{|a_n|}\right\}_{n=1}^{\infty}\text{ist eine Nullfolge},$
$(iv)$ $\{a_n\cdot c_n\}_{n = 1}^{\infty}$ ist eine Nullfolge.

Beweis. Zu (i): Da $\{a_n\}_{n=1}^{\infty}$ eine Nullfolge ist, existiert $N \in \mathbb{N}$, so dass

$$
| a _ {n} | \leq 1 \quad \text { for   all } n \geq N.
$$

Wir setzen

$$
C := \max _ {1 \leq n \leq N} \left\{\left| a _ {n} \right| \right\} _ {n = 1} ^ {\infty} = \max \left\{\left| a _ {1} \right|, \left| a _ {2} \right|, \dots , \left| a _ {N} \right| \right\}
$$

und definieren

$$
\tilde {C} := \max \left\{C, 1 \right\}.
$$

Dann ist $|a_n| \leq \tilde{C}$ for all $n \in \mathbb{N}$.

Zu (ii): Nach der Dreiecksungleichung und der Homogenität des Absolutbetrags gilt

$$
\left| \alpha a _ {n} + \beta b _ {n} \right| \leq | \alpha | | a _ {n} | + | \beta | | b _ {n} | \quad \text {fur alle} n \in \mathbb {N}. \tag {4.1.4}
$$

Sei $\varepsilon > 0$ gegeben. Ohne Beschränkung der Allgemeinheit können wir annehmen, dass $\alpha \neq 0$ und $\beta \neq 0$. (Warum?) Da $\{a_n\}_{n=1}^{\infty}$, $\{b_n\}_{n=1}^{\infty}$ Nullfolgen sind, existieren $N_1, N_2 \in \mathbb{N}$, so dass

$$
| a _ {n} | <   \frac {\varepsilon}{2 | \alpha |} \quad \text {fur alle} n \geq N _ {1}, \qquad | b _ {n} | <   \frac {\varepsilon}{2 | \beta |} \quad \text {fur alle} n \geq N _ {2}. \tag {4.1.5}
$$

Aus (4.1.4) und (4.1.5) folgt

$$
\left| \alpha a _ {n} + \beta b _ {n} \right| \leq \frac {\varepsilon}{2} + \frac {\varepsilon}{2} = \varepsilon \quad \text {f ü r a l l e} n \geq \max \left\{N _ {1}, N _ {2} \right\}.
$$

Zu (iii): $\mathrm{Zu} \varepsilon > 0$ wählen wir $N \in \mathbb{N}$, so dass

$$
| a _ {n} | <   \varepsilon^ {2} \quad \text { für   alle } n \geq N.
$$

Zu (iv): Nach Annahme existiert $M \in \mathbb{R}$, so dass

$$
| c _ {n} | \leq M \quad \text { für   alle } n \in \mathbb {N}.
$$

Nach (ii) ist  $\{M|a_{n}|\}_{n=1}^{\infty}$  eine Nullfolge. Da  $|a_{n}\cdot c_{n}|\leq M|a_{n}|$ , schließen wir mit Satz 4.1.5, dass  $\{a_{n}\cdot c_{n}\}_{n=1}^{\infty}$  eine Nullfolge ist. ☐

Fall (iv) oben ist der einfache Fall. Sehr oft werden wir Folgenglieder der Form

$$
a _ {n} \cdot c _ {n}
$$

betrachten, wobei  $\{a_{n}\}_{n=1}^{\infty}$  eine Nullfolge ist und  $\{c_{n}\}_{n=1}^{\infty}$  eine unbeschränkte Folge ist. Die Frage ist die Rate: verschwindet  $a_{n}$  schneller oder wächst  $c_{n}$  schneller? Als Beispiel betrachten wir die Folge mit Folgengliedern

$$
n \alpha^ {n}, \quad | \alpha | <   1.
$$

Die „intuitive“ Antwort ist, dass diese Folge gegen Null konvergiert, weil „exponentielles Abfallen lineares Wachsen schlägt“. Jetzt begründen wir diese Behauptung. Die Idee ist folgende: Als wir oben gezeigt haben, dass  $\{a_{n}\}_{n=1}^{\infty}$  gegen 0 konvergiert, haben wir die Abschätzung

$$
| \alpha | ^ {n} \leq \frac {1}{h n} \quad \text { für   ein } h > 0
$$

angewendet. Hier reicht diese Abschätzung nicht aus, weil wir daraus nur

$$
| n \alpha^ {n} | \leq \frac {1}{h}
$$

erhalten. Wegen  $\frac{1}{\sqrt{|\alpha|}}>1$  können wir  $\tilde{h}$  durch

$$
\frac {1}{\sqrt {| \alpha |}} = 1 + \tilde {h}
$$

definieren und erhalten somit eine bessere Rate, wie wir jetzt zeigen.

Beweis. Sei $\tilde{h}$ durch

$$
\frac {1}{\sqrt {| \alpha |}} = 1 + \tilde {h}
$$

definiert. Dann ist  $\tilde{h} > 0$  und es gilt

$$
\begin{array}{l} | n \alpha^ {n} | = n | \alpha | ^ {n} = n \cdot \frac {1}{(1 + \tilde {h}) ^ {n}} \cdot \frac {1}{(1 + \tilde {h}) ^ {n}} \\ \leq n \cdot \frac {1}{1 + n \tilde {h}} \cdot \frac {1}{1 + n \tilde {h}} \quad (\text {Bernoullische Ungleichung}) \\ \leq n \cdot \frac {1}{(n \tilde {h}) ^ {2}} \\ = \frac {1}{n (\tilde {h}) ^ {2}}, \\ \end{array}
$$

also ist $\{n\alpha^n\}_{n=1}^{\infty}$ eine Nullfolge.

Frage: Können Sie eine noch bessere Rate des Abfallens von $\{\alpha^n\}$ erhalten? Inwiefern?

Beispiel. Ist $a_{n} = \frac{x^{n}}{n!}, x \in \mathbb{R}$, eine Nullfolge?

Lösung. Ja, Abfallen durch Fakultät schlägt exponentielles Wachstum. Wir schreiben

$$
\frac {x ^ {n}}{n !} = \underbrace {\frac {x}{1} \cdot \frac {x}{2} \cdot \dots \cdot \frac {x}{m}} _ {=: C _ {m}} \cdot \underbrace {\frac {x}{m + 1} \cdot \dots \cdot \frac {x}{n}} _ {n - m \text {Terme}}, \tag {4.1.6}
$$

wobei  $C_{m} < \infty$  für m groß aber fest (endlich) gilt. Wir wählen  $m \in N$  groß genug, so dass

$$
\left| \frac {x}{m} \right| <   \frac {1}{2}. \tag {4.1.7}
$$

Dann ist

$$
\begin{array}{l} \left| \frac {x ^ {n}}{n !} \right| \stackrel {(4. 1. 6)} {\leq} C _ {m} \cdot \left| \frac {x}{m} \right| ^ {n - m} \stackrel {(4. 1. 7)} {\leq} C _ {m} \left(\frac {1}{2}\right) ^ {n - m} \\ = C _ {m} 2 ^ {m} \left(\frac {1}{2}\right) ^ {n}. \\ \end{array}
$$

Für m fest ist  $C_{m} \cdot 2^{m}$  eine feste Zahl. Da  $\left\{\frac{1}{2^{n}}\right\}_{n=1}^{\infty}$  eine Nullfolge ist, ist auch  $\left\{\frac{x^{n}}{n!}\right\}_{n=1}^{\infty}$  eine Nullfolge. (Nach Satz 4.1.7 (ii) und Satz 4.1.5.) ☐

Bemerkung. Die Formulierung „m groß aber fest“ bedeutet, dass wir zwar je nach x m sehr groß wählen müssen. Dieses so gewählte m muss jedoch nicht mehr im Laufe des Beweises geändert werden und kann somit im Folgendem auch als etwas Festes, Gegebenes betrachtet werden. Daher ist oft die Reihenfolge in Beweisen wichtig. In diesem ist x gegeben und dann wählen wir unser m. Danach ist es nicht mehr möglich x zu ändern, der Beweis müsste dann wieder von vorne betrachtet werden.

Andere mögliche Fragen sind z.B.

$$
\frac {n ^ {3}}{n !}, \qquad \frac {x ^ {n}}{n ^ {2}}, \qquad \frac {n !}{n ^ {p} \cdot x ^ {n}}, \qquad \text {usw.}
$$

## 4.2 Allgemeine Konvergenz und Divergenz

Jetzt, da wir Nullfolgen so gut verstehen, ist es leicht konvergente Folgen im Allgemeinen zu definieren.

## Definition 4.2.1

Die Folge $\{a_{n}\}_{n=1}^{\infty}$ heißt konvergent mit Grenzwert $a$, oder $a_{n}$ konvergiert gegen $a$, wenn es ein $a \in \mathbb{R}$ gibt mit der Eigenschaft, dass die Folge $\{a_{n}-a\}_{n=1}^{\infty}$ eine Nullfolge ist. Das heißt, zu jedem $\varepsilon > 0$ gibt es ein $N \in \mathbb{N}$, so dass

$$
| a _ {n} - a | <   \varepsilon \quad \text { für   alle } n \geq N.
$$

Dann schreiben wir

$$
\lim _ {n \to \infty} a _ {n} = a \quad \text {oder} \quad a _ {n} \longrightarrow a \quad \text {für} n \to \infty .
$$

## Notation 4.2.2

Analog zur Notation für Nullfolgen schreibt man

$$
a _ {n} \uparrow a \quad \text {oder} \quad a _ {n} \nearrow a \quad \text {bzw.} \quad a _ {n} \downarrow a \quad \text {oder} \quad a _ {n} \searrow a,
$$

wenn $\{a_{n}\}_{n = 1}^{\infty}$ für $n\to \infty$ monoton wachsend bzw. monoton fallend gegen $a$ konvergiert.

## Definition 4.2.3

Die Folge $\{a_n\}_{n=1}^{\infty}$ heißt konvergent, wenn es eine Zahl $a \in \mathbb{R}$ gibt, so dass $\lim_{n \to \infty} a_n = a$. Ansonsten heißt die Folge $\{a_n\}_{n=1}^{\infty}$ divergent.

Man betrachte

$$
a _ {n} = n, \qquad b _ {n} = (- 1) ^ {n} \cdot n.
$$

Beide sind divergent, aber das Verhalten ist sehr verschieden. Um über den Unterschied reden zu können, führen wir folgende Definition ein:

## Definition 4.2.4

Wir sagen, dass $\{a_n\}_{n=1}^{\infty}$ gegen Unendlich divergiert, wenn es für jedes $M \in \mathbb{R}$ ein $N = N(M)$ gibt mit der Eigenschaft, dass

$$
a _ {n} \geq M \quad \text { für   alle } n \geq N.
$$

In diesem Fall schreiben wir

$$
a _ {n} \longrightarrow \infty \quad \text {oder} \quad \lim _ {n \to \infty} a _ {n} = \infty .
$$

Analog für  $a_{n} \longrightarrow -\infty$ . Wenn  $a_{n} \longrightarrow \infty$  oder  $a_{n} \longrightarrow -\infty$ , dann sagen wir, dass die Folge  $\{a_{n}\}_{n=1}^{\infty}$  bestimmt divergent ist. Wenn  $\{a_{n}\}_{n=1}^{\infty}$  divergent, aber nicht bestimmt divergent ist, dann sagen wir, dass die Folge unbestimmt divergent ist.

Die Folge $a_{n} = n$ von oben ist eine bestimmt divergente Folge. Beispiele unbestimmt divergenter Folgen:

$$
\{(- 1) ^ {n} \} _ {n = 1} ^ {\infty}, \qquad \{(- 1) ^ {n} \cdot n \} _ {n = 1} ^ {\infty}, \qquad \{(1 + (- 1) ^ {n}) n \} _ {n = 1} ^ {\infty}.
$$

Das Verhalten ist unterschiedlich.  $\{a_{n}\}_{n=1}^{\infty}$  ist unbestimmt divergent und beschränkt.  $\{b_{n}\}_{n=1}^{\infty}$  ist unbestimmt divergent und unbeschränkt.  $\{c_{n}\}_{n=1}^{\infty}$  ist unbestimmt divergent, nach unten beschränkt und nach oben unbeschränkt.

Bemerkung. Achtung! Bemerken Sie, dass

$$
\lim _ {n \to \infty} a _ {n} = \infty
$$

nicht impliziert, dass $\{a_n\}$ konvergent ist (weil Unendlich keine reelle Zahl ist; sehen Sie Definition 4.2.3).

## Satz 4.2.5

Der Grenzwert einer konvergenten Folge ist eindeutig bestimmt.

![](images/page_76_image_17.jpg)

Beweis. Wir nehmen an, dass  $\{a_{n}\}_{n=1}^{\infty}$  konvergent ist mit den Grenzwerten a und  $\tilde{a}$ , wobei  $a \neq \tilde{a}$  gilt. Wir definieren

$$
\varepsilon := \frac {1}{2} | a - \tilde {a} |.
$$

Da $a_{n}\rightarrow a$ konvergiert, existiert ein $N\in \mathbb{N}$, so dass

$$
| a _ {n} - a | \leq \varepsilon \quad \text { für   alle } n \geq N.
$$

Aus der Dreiecksungleichung erhält man

$$
\begin{array}{l} \left| a _ {n} - \tilde {a} \right| \geq \left| a - \tilde {a} \right| - \left| a _ {n} - a \right| \\ \geq 2 \varepsilon - \varepsilon = \varepsilon \quad \text {f ü r a l l e} n \geq N, \\ \end{array}
$$

was widerspricht, dass $a_{n}\to \tilde{a}$ für $n\to \infty$.

![](images/page_77_image_6.jpg)

## Übung 4.2.6

Schreiben Sie einen direkten Beweis.

Man erhält die folgenden Verallgemeinerungen der Sätze 4.1.5 und 4.1.7.

## Satz 4.2.7: Vergleichskriterium

Es seien $\{a_{n}\}_{n = 1}^{\infty}$, $\{b_n\}_{n = 1}^{\infty}$ und $\{c_n\}_{n = 1}^{\infty}$ Zahlenfolgen mit

$$
a _ {n} \leq b _ {n} \leq c _ {n} \quad \text {f ü r a l l e} n \geq N,
$$

für ein $N\in \mathbb{N}$ . Dann gilt

(i) Wenn $a_{n} \longrightarrow a, b_{n} \longrightarrow b, c_{n} \longrightarrow c$ für $n \to \infty$, dann ist

$$
a \leq b \leq c.
$$

(ii) (Sandwichkriterium) Wenn  $a_{n} \longrightarrow a$  und  $c_{n} \longrightarrow a$  für  $n \to \infty$  (gleiche Grenzwerte für  $a_{n}$  und  $c_{n}$ ), dann ist die Folge  $\{b_{n}\}_{n=1}^{\infty}$  konvergent und

$$
b _ {n} \longrightarrow a \quad \text { für } n \rightarrow \infty .
$$

## Satz 4.2.8: Eigenschaften konvergenter Folgen

Es seien  $\{a_{n}\}_{n=1}^{\infty}$  und  $\{b_{n}\}_{n=1}^{\infty}$  konvergente Zahlenfolgen mit Grenzwerten a bzw. b. Weiter sei  $\{c_{n}\}_{n=1}^{\infty}$  eine beschränkte Folge. Dann gilt

(i) Die Folge  $\{a_{n}\}_{n=1}^{\infty}$  ist beschränkt.
(ii) Die Folge $\{\alpha a_{n} + \beta b_{n}\}_{n = 1}^{\infty}$ mit $\alpha, \beta \in \mathbb{R}$ konvergiert gegen $\alpha a + \beta b$.
(iii) Die Folge  $\{|a_{n}|\}_{n=1}^{\infty}$  konvergiert gegen  $|a|$  und  $\{\sqrt{|a_{n}|}\}_{n=1}^{\infty}$  konvergiert gegen  $\sqrt{|a|}$ .
(iv) Die Folge  $\{a_{n} \cdot b_{n}\}_{n=1}^{\infty}$  konvergiert gegen  $a \cdot b$ .
(v) Die Folge  $\{a_{n} \cdot c_{n}\}_{n=1}^{\infty}$  ist beschränkt.

(vi) Wenn  $a_{n} \neq 0$  für alle  $n \in N$  und  $a \neq 0$ , dann gilt

$$
\frac {1}{a _ {n}} \longrightarrow \frac {1}{a} \quad \text {für} n \to \infty .
$$

## Übung 4.2.9

Beweisen Sie den Satz. (Hinweis: Die Ideen wurden schon im Abschnitt 4.1 eingeführt.)

Bemerkung. Satz 4.2.7 (ii) wird das „Sandwich“-Kriterium genannt, weil $b_n$ zwischen zwei Folgen eingeschlossen ist, wie der Käse zwischen zwei Brotscheiben.

Bemerkung. Satz 4.2.8 (v) ist scharf in dem Sinne: $\{a_n\}_{n=1}^{\infty}$ konvergent und $\{c_n\}_{n=1}^{\infty}$ beschränkt impliziert nicht, dass $\{a_n \cdot c_n\}$ konvergiert. Beispiel: $a_n = 1$ für alle $n \in \mathbb{N}$, $c_n = (-1)^n$. Die Ausnahme - wie in Satz 4.1.7 gesehen - ist, wenn $a_n \to 0$.

Bemerkung. Man sollte Satz 4.2.8 (ii) nicht für selbstverständlich halten. Wir schauen uns dazu das folgende Beispiele an. Sei $\{a_k\}_{k=1}^{\infty}$ eine Zahlenfolge. Man definiert die Folge

$$
x _ {n} := \sup \underbrace {\{a _ {k} , k \geq n \}} _ {\text {eine Menge}}
$$

und die Zahl

$$
\operatorname * {l i m s u p} _ {n \to \infty} a _ {n} := \lim _ {n \to \infty} x _ {n}.
$$

Es gilt

$$
\operatorname * {l i m s u p} _ {n \to \infty} (a _ {n} + b _ {n}) \leq \operatorname * {l i m s u p} _ {n \to \infty} a _ {n} + \operatorname * {l i m s u p} _ {n \to \infty} b _ {n},
$$

aber die linke Seite kann echt kleiner sein, zum Beispiel für

$$
a _ {n} = (- 1) ^ {n}, \qquad b _ {n} = (- 1) ^ {n + 1}.
$$

Wir schauen uns jetzt an, wie Satz 4.2.8 in den Hausaufgaben vorkommen könnte.

Beispiele. Bestimmen Sie, ob die folgenden Folgen konvergieren. Wenn ja, geben Sie den Grenzwert an. Begründen Sie Ihre Antwort.

①

$$
a _ {n} = \frac {5 n ^ {3} + 3 n - 2}{2 n ^ {3} - n},
$$

②

$$
a _ {n} = \left(\frac {1}{2}\right) ^ {n} \frac {n}{2 n + 5},
$$

③

$$
a _ {n} = \left(\frac {1}{2}\right) ^ {n} n ^ {2},
$$

④

$$
a _ {n} = \sqrt [ n ]{x}, \quad x > 0, \tag {4.2.1}
$$

⑤

$$
a _ {n} = \sqrt [ n ]{n}. \tag {4.2.2}
$$

Lösung. zu ①: Für solche rationale Funktionen von n dividieren wir durch die größte Potenz von n um die Folgenglieder in die folgende Form zu bringen:

$$
\begin{array}{l} \lim _ {n \to \infty} \frac {5 n ^ {3} + 3 n - 2}{2 n ^ {3} - n} = \lim _ {n \to \infty} \frac {5 + \frac {3}{n ^ {2}} - \frac {2}{n ^ {3}}}{2 - \frac {1}{n ^ {2}}} \\ = \frac {5 + \lim _ {n \to \infty} \frac {3}{n ^ {2}} - \lim _ {n \to \infty} \frac {2}{n ^ {3}}}{2 - \lim _ {n \to \infty} \frac {1}{n ^ {2}}} \\ = \frac {5}{2}, \\ \end{array}
$$

wobei wir Satz 4.2.8 (ii), (iv) und (vi) angewendet haben.

zu ②: Wir wenden Satz 4.2.8 (iv) an.

$$
\begin{array}{l} \lim _ {n \to \infty} \left(\frac {1}{2}\right) ^ {n} \frac {n}{2 n + 5} = \lim _ {n \to \infty} \left(\frac {1}{2}\right) ^ {n} \cdot \lim _ {n \to \infty} \frac {n}{2 n + 5} \\ = 0 \cdot \lim _ {n \to \infty} \frac {1}{2 + \frac {5}{n}} \\ = 0 \cdot \frac {1}{2} \\ = 0. \\ \end{array}
$$

Wenn man in einer ähnlichen Situation einen Ausdruck der Form „0 · ∞“ oder „0/0“ oder „∞“ erhält, muss man einen anderen Weg nehmen.

zu ③: Die oben angewendete Methode ergibt „0·∞“. Das Abfallen von  $\frac{1}{2^{n}}$  ist „stärker“

als das Wachsen von  $n^{2}$ . Wir können dies deutlich machen, wenn wir zeigen, dass

$$
2 ^ {n} > n ^ {3} \text {f ü r} n \text {g r o ß s g e n u g}, \tag {4.2.3}
$$

also für $n \geq N$ für ein $N \in \mathbb{N}$. Wenn (4.2.3) gilt, dann ist

$$
0 \leq \left(\frac {1}{2}\right) ^ {n} n ^ {2} \leq \frac {n ^ {2}}{n ^ {3}} = \frac {1}{n} \quad \text { für } n \geq N.
$$

Aus dem Vergleichskriterium für Nullfolgen und  $\frac{1}{n} \rightarrow 0$  für  $n \rightarrow \infty$  erhalten wir, dass  $\{a_{n}\}_{n=1}^{\infty}$  eine Nullfolge ist. Um (4.2.3) zu zeigen, benutzen wir vollständige Induktion. Für n = 10 ist (4.2.3) wahr. Wir nehmen an, dass (4.2.3) für ein  $N \geq 10$  gilt und müssen zeigen, dass

$$
2 ^ {N + 1} > (N + 1) ^ {3}. \tag {4.2.4}
$$

Wir rechnen

$$
2 ^ {N + 1} = 2 \cdot 2 ^ {N} \stackrel {\text {Annahme}} {>} 2 \cdot N ^ {3}.
$$

Also gilt (4.2.4) genau dann, wenn

$$
N ^ {3} > 3 N ^ {2} + 3 N + 1.
$$

Dies folgt aus den drei Relationen (die leicht nachzuweisen sind)

$$
3 N + 1 <   4 N \quad \text {fur} N > 1, \tag {4.2.5}
$$

$$
3 N ^ {2} + 4 N <   4 N ^ {2} \quad \text {fur} \mathrm{N} > 4, \tag {4.2.6}
$$

$$
N ^ {3} > 4 N ^ {2} \quad \text {fur} \mathrm{N} > 4. \tag {4.2.7}
$$

Man erhält

$$
N ^ {3} \stackrel {(4. 2. 7)} {>} 4 N ^ {2} \stackrel {(4. 2. 6)} {>} 3 N ^ {2} + 4 N \stackrel {(4. 2. 5)} {>} 3 N ^ {2} + 3 N + 1.
$$

Nach dem Prinzip der vollständigen Induktion erhalten wir, dass (4.2.3) für alle $n \in \mathbb{N}$ mit $n \geq 10$ gilt.

zu ④: Hier werden wir das Vergleichskriterium anwenden. Wir fangen mit $x \geq 1$ an. Nützlich ist, wenn man

$$
\sqrt [ n ]{x} = (1 + (\sqrt [ n ]{x} - 1)) = 1 + y _ {n}
$$

mit $y_{n}\geq 0$ für $x\geq 1$ schreibt. Also schreiben wir

$$
\begin{array}{l} x = (\sqrt [ n ]{x}) ^ {n} = (1 + (\sqrt [ n ]{x} - 1)) ^ {n} = (1 + y _ {n}) ^ {n} \\ \geq 1 + n y _ {n} = 1 + n (\sqrt [ n ]{x} - 1) \geq n (\sqrt [ n ]{x} - 1) \quad \text {(Bernoulli)}. \\ \end{array}
$$

Aus $x \geq n(\sqrt[n]{x} - 1)$ schließen wir

$$
1 \leq \sqrt [ n ]{x} \leq 1 + \frac {x}{n}.
$$

Das Vergleichskriterium ergibt

$$
\sqrt [ n ]{x} \rightarrow 1 \text {f ü r} n \rightarrow \infty \text {f ü r} x > 1.
$$

Für $x \in (0,1)$ schreiben wir

$$
\sqrt [ n ]{x} = \frac {1}{\sqrt [ n ]{\frac {1}{x}}} = \frac {1}{\sqrt [ n ]{y}}, \quad y > 1,
$$

und wenden Satz 4.2.8 an. (Der Grenzwert des Quotienten ist der Quotient der Grenzwerte.)

## Übung 4.2.10

Zeigen Sie ⑤.

Die vorherigen Beispiele waren alle schön in dem Sinne, dass wir den Grenzwert identifizieren konnten. Manchmal kann man das nicht tun. Gibt es Kriterien um zu verstehen, ob eine Folge konvergiert, ohne den Grenzwert zu wissen? Wir haben gesehen, dass konvergente Folgen beschränkt sind. Gilt die Umkehrung? Sind beschränkte Folgen konvergent? Das einfache Beispiel  $a_{n} = (-1)^{n}$  zeigt, dass dies nicht der Fall ist. Monotonie ist anscheinend auch nicht ausreichend, da  $a_{n} = n$  nicht konvergiert. Wenn man allerdings Beschränktheit und Monotonie kombiniert, hat man ein ausreichendes Kriterium gefunden.

## Satz 4.2.11

Eine monotone Zahlenfolge, die beschränkt ist, konvergiert.

Anders gesagt, wenn eine Folge divergiert, müssen die Mitglieder beliebig groß im Absolutbetrag werden oder oszillieren.

Bemerkung. Meist wenden wir den Satz direkt in folgender Form an: Eine monoton wachsende Zahlenfolge, die nach oben beschränkt ist, sowie eine monoton fallende Zahlenfolge, die nach unten beschränkt ist, konvergiert.

Beweis von Satz 4.2.11. Ohne Beschränkung der Allgemeinheit (warum?) können wir annehmen, dass $\{a_n\}_{n=1}^{\infty}$ monoton wachsend ist. Wir definieren

$$
a := \sup \left\{a _ {n}: n \in \mathbb {N} \right\}.
$$

Da $\{a_{n}\}_{n = 1}^{\infty}$ beschränkt ist, ist $a < \infty$. Außerdem gilt $a_{n} \leq a$ für alle $n \in \mathbb{N}$ (weil $a$

eine obere Schranke ist) und für jedes $\varepsilon > 0$ existiert ein $N \in \mathbb{N}$, so dass

$$
a _ {N} > a - \varepsilon
$$

(Approximations-Eigenschaft des Supremums). Da $\{a_n\}_{n=1}^{\infty}$ monoton wachsend ist, gilt

$$
a _ {n} \geq a _ {N} > a - \varepsilon \quad \text { für   alle } n \geq N.
$$

Also haben wir insgesamt: Für jedes $\varepsilon > 0$ existiert ein $N \in \mathbb{N}$, so dass

$$
a - \varepsilon \leq a _ {n} \leq a \quad \text { für   alle } n \geq N.
$$

Nach der Definition von Konvergenz haben wir

$$
a _ {n} \rightarrow a \quad \text { für } n \rightarrow \infty
$$

gezeigt.

![](images/page_82_image_12.jpg)

Woran scheitert der Beweis, wenn $\{a_n\}_{n=1}^{\infty}$ nicht monoton ist?

“A definition or theorem is not just a static statement, it is a weapon for deducing truth.”

Charles Wells, 2016

## 4.3 Die Exponentialfunktion und der Logarithmus

Wir benutzen Zahlenfolgen um die Exponentialfunktion zu definieren. Wir werden zeigen, dass für jedes  $x \in R$  der Grenzwert

$$
\lim _ {n \to \infty} \left(1 + \frac {x}{n}\right) ^ {n} \tag {4.3.1}
$$

existiert. Diesen Grenzwert (als Funktion von x) nennen wir die Exponentialfunktion:

$$
\exp (x) := \lim _ {n \to \infty} \left(1 + \frac {x}{n}\right) ^ {n}. \tag {4.3.2}
$$

Außerdem nennen wir

$$
e := \lim _ {n \to \infty} \left(1 + \frac {1}{n}\right) ^ {n} \tag {4.3.3}
$$

die Eulersche Zahl. Nachdem wir gezeigt haben, dass der Grenzwert (4.3.1) existiert, werden wir bestätigen, dass die in (4.3.2) definierte Funktion die erwarteten Eigenschaften (z.B.  $\exp(x+y)=\exp(x)\cdot\exp(y)$ ) hat. In (4.3.3) ist es wichtig zu bemerken, dass das Kleinwerden von  $1 + \frac{1}{n}$  im Wettbewerb mit dem Größerwerden der Potenz steht. Obwohl  $1 + \frac{1}{n} \rightarrow 1$  für  $n \rightarrow \infty$ , ist

$$
\lim _ {n \to \infty} \left(1 + \frac {1}{n}\right) ^ {n} \neq 1 ^ {n} = 1.
$$

Es gilt  $1 + \frac{1}{n} \downarrow 1$  und  $(1 + \alpha)^{n} \uparrow \infty$  für alle  $\alpha > 0$ . In (4.3.3) muss man zwei konkurrierende Limiten gleichzeitig betrachten.

## Satz 4.3.1

Für alle $x \in \mathbb{R}$ existiert

$$
\lim _ {n \to \infty} \left(1 + \frac {x}{n}\right) ^ {n}.
$$

Beweis. Wir definieren

$$
e _ {n} := \left(1 + \frac {x}{n}\right) ^ {n}.
$$

Das Ziel ist zu zeigen, dass  $\{e_{n}\}_{n=1}^{\infty}$  monoton wachsend und nach oben beschränkt ist für N groß genug. Als Erstes zeigen wir, dass  $\frac{e_{n+1}}{e_{n}} \geq 1$  für n groß genug. Wir bemerken, dass  $e_{n} > 0$  für n > -x. Wir schreiben

$$
\begin{array}{l} \frac {e _ {n + 1}}{e _ {n}} = \frac {\left(1 + \frac {x}{n + 1}\right) ^ {n + 1}}{\left(1 + \frac {x}{n}\right) ^ {n}} = \left(\frac {1 + \frac {x}{n + 1}}{1 + \frac {x}{n}}\right) ^ {n + 1} \cdot \left(1 + \frac {x}{n}\right) \\ = (1 + h) ^ {n + 1} \cdot \left(1 + \frac {x}{n}\right), \\ \end{array}
$$

wobei wir

$$
h := \frac {1 + \frac {x}{n + 1}}{1 + \frac {x}{n}} - 1
$$

gesetzt haben. Für n > -x gilt  $1 + \frac{x}{n} > 0$ , s.d. h > -1. In diesem Fall ergibt die Bernoulli-Ungleichung

$$
\begin{array}{l} \frac {e _ {n + 1}}{e _ {n}} \geq (1 + (n + 1) h) \left(1 + \frac {x}{n}\right) \\ = \frac {n}{n + x} \cdot \frac {n + x}{n} \\ = 1. \\ \end{array}
$$

$$
\begin{array}{l} \left[ \begin{array}{c} 1 + (n + 1) h = 1 + (n + 1) \frac {(n + 1 + x) n}{(n + 1) (n + x)} - n - 1 = \frac {n}{n + x}. \end{array} \right. \\ \lfloor \end{array}
$$

Wir brauchen noch eine obere Schranke. Da  $e_{n} = \left(1 + \frac{x}{n}\right)^{n}$  monoton wachsend ist für n > -x, ist  $\left(1 - \frac{x}{n}\right)^{n}$  monoton wachsend für n > x und deshalb ist

$$
b _ {n} := \frac {1}{\left(1 - \frac {x}{n}\right) ^ {n}}
$$

monoton fallend für n > x. Insbesondere schließen wir daraus:

$$
\{b _ {n} \colon n > x \} \text {ist nach oben beschränkt.} \tag {4.3.4}
$$

Man erhält direkt

$$
\frac {e _ {n}}{b _ {n}} = \left(1 + \frac {x}{n}\right) ^ {n} \left(1 - \frac {x}{n}\right) ^ {n} = \left(1 - \frac {x ^ {2}}{n ^ {2}}\right) ^ {n} \leq 1. \tag {4.3.5}
$$

Aus (4.3.4) und(4.3.5) folgt es, dass  $e_{n}$  für n > x nach oben beschränkt ist. Es folgt nach Satz 4.2.11, dass  $\{e_{n}\}_{n=1}^{\infty}$  konvergiert. ☐

Frage: Was können Sie über die folgenden Grenzwerte sagen?

- $\lim_{n\to \infty}\left(1 + \frac{1}{n^2}\right)^n,$
- $\lim_{n\to \infty}\left(1 + \frac{1}{n}\right)^{n^2}$,
- $\lim_{n\to \infty}\left(1 + \frac{1}{f(n)}\right)^{g(n)}.$

## Übung 4.3.2

Als alternativer Beweis, dass  $e_{n+1} > e_{n}$  für n groß genug, kann man die Ungleichung zwischen dem geometrischen und arithmetischen Mittel, auch AGM-Ungleichung genannt, verwenden; siehe (1.5.7). Verwenden Sie die AGM-Ungleichung für ein Produkt von  $(n+1)$  Faktoren, um zu zeigen, dass für  $x \in R$  und  $n \in N$  mit  $n \geq -x$ ,  $x \neq 0$ , gilt:

$$
\left(1 + \frac {x}{n}\right) ^ {n} <   \left(1 + \frac {x}{n + 1}\right) ^ {n + 1}.
$$

Jetzt bemerken wir, dass exp(·) sich „wie eine Potenz“ verhält.

## Satz 4.3.3: Eigenschaften von $\exp(\cdot)$

Für $\exp (x)$ gilt

(i)  $\exp(0)=1,$
(ii)  $\exp(x+y)=\exp(x)\cdot\exp(y)$  für alle  $x,y\in R$ ,
(iii) $\exp (x) > 0$ für alle $x\in \mathbb{R}$,

$$
(i v) \exp (- x) = \frac {1}{\exp (x)} \text { für   alle } x \in \mathbb {R}.
$$

Als Hilfsmittel für den Beweis benutzen wir:

Lemma 4.3.4. Für alle $a, b \in \mathbb{R}, n \in \mathbb{N}$ gilt

$$
a ^ {n} - b ^ {n} = (a - b) \sum_ {k = 1} ^ {n} a ^ {n - k} b ^ {k - 1}.
$$

Den Beweis des Lemmas lassen wir als Übung.

Beweis von Satz 4.3.3. (i) ist klar. (iv) folgt aus (i) und (ii). (Wie?)

zu (iii): Nach (iv) reicht es zu zeigen, dass  $\exp(x) > 0$  für  $x \geq 0$ . Nach der Bernoulli-Ungleichung gilt

$$
\exp (x) = \lim _ {n \to \infty} \left(1 + \frac {x}{n}\right) ^ {n} \geq 1 + x > 0 \quad \text { für } x \geq 0.
$$

zu (ii): Seien $x, y \in \mathbb{R}$ gegeben. Nach Satz 4.2.7 gilt

$$
\begin{array}{l} \left| \exp (x + y) - \exp (x) \exp (y) \right| = \lim _ {n \rightarrow \infty} \left|\left(1 + \frac {x + y}{n}\right) ^ {n} - \left(1 + \frac {x}{n}\right) ^ {n} \left(1 + \frac {y}{n}\right) ^ {n} \right| \\ = \lim _ {n \to \infty} \left| \left(1 + \frac {x + y}{n} - \left(1 + \frac {x}{n}\right) \left(1 + \frac {y}{n}\right)\right) \right. \\ \left. \sum_ {k = 1} ^ {n} \left(1 + \frac {x + y}{n}\right) ^ {n - k} \left(\left(1 + \frac {x}{n}\right) \left(1 + \frac {y}{n}\right)\right) ^ {k - 1} \right|, \tag {4.3.6} \\ \end{array}
$$

wobei wir Lemma 4.3.4 angewendet haben. Der erste Term auf der rechten Seite ist

$$
1 + \frac {x}{n} + \frac {y}{n} - \left(1 + \frac {x}{n} + \frac {y}{n} + \frac {x y}{n ^ {2}}\right) = - \frac {x y}{n ^ {2}}. \tag {4.3.7}
$$

Andererseits gilt für jeden Term in der Summe

$$
\begin{array}{l} \left| \left(1 + \frac {x + y}{n}\right) ^ {n - k} \left(\left(1 + \frac {x}{n}\right) \left(1 + \frac {y}{n}\right)\right) ^ {k - 1} \right| \\ \leq \left(1 + \frac {| x |}{n}\right) ^ {n - k} \left(1 + \frac {| y |}{n}\right) ^ {n - k} \left(1 + \frac {| x |}{n}\right) ^ {k - 1} \left(1 + \frac {| y |}{n}\right) ^ {k - 1} \\ = \left(1 + \frac {| x |}{n}\right) ^ {n - 1} \left(1 + \frac {| y |}{n}\right) ^ {n - 1} \\ \leq \frac {1}{\left(1 + \frac {| x |}{n}\right) \left(1 + \frac {| y |}{n}\right)} \exp (| x |) \exp (| y |) \\ \leq \exp (| x |) \exp (| y |), \tag {4.3.8} \\ \end{array}
$$

wobei wir uns in der vorletzten Gleichung an die Monotonie der Konvergenz gegen  $\exp(\cdot)$  erinnert haben. Die Dreiecksungleichung zusammen mit (4.3.6), (4.3.7) und (4.3.8) ergibt

$$
| \exp (x + y) - \exp (x) \cdot \exp (y) | \leq \lim _ {n \to \infty} \left| \frac {x y}{n ^ {2}} \cdot n \cdot \exp (| x |) \exp (| y |) \right| = 0.
$$

Da $e^{\frac{p}{q}} = \sqrt[q]{e^{p}}$ für $e = \exp(1)$ schon definiert ist, möchten wir jetzt

$$
\exp (x) \quad \text {und} \quad e ^ {x} \quad \text {für} x \in \mathbb {Q}
$$

miteinander vergleichen.

Lemma 4.3.5. Sei $x = \frac{p}{q}$ eine rationale Zahl. Dann gilt

$$
\exp (x) = e ^ {x}. \tag {4.3.9}
$$

Da (4.3.9) für alle $x \in \mathbb{Q}$ gilt, ergibt die folgende Definition Sinn.

## Definition 4.3.6

Wir definieren

$$
e ^ {x} := \exp (x) \quad \text { für   alle } x \in \mathbb {R} \setminus \mathbb {Q}.
$$

Angesichts Lemma 4.3.5 gilt

$$
e ^ {x} = \exp (x) \quad \text { für   alle } x \in \mathbb {R}.
$$

Beweis von Lemma 4.3.5. Für $p \in \mathbb{N}$ gilt

$$
\begin{array}{l} e ^ {p} = (\exp (1)) ^ {p} \\ = \underbrace {\exp (1) \cdot \exp (1) \cdot \dots \cdot \exp (1)} _ {p \text {mal}} \\ = \exp (\underbrace {1 + 1 + \dots + 1} _ {p \text {mal}}) \quad \text {(nach Satz 4.3.3 (ii))} \\ = \exp (p). \\ \end{array}
$$

Für  $x = \frac{p}{q}$  mit  $p, q \in N$  reicht es zu zeigen, dass  $(e^{x})^{q} = (\exp(x))^{q}$  ist. Da  $xq \in N$  ist, folgt aus dem vorherigen Schritt, dass

$$
\begin{array}{l} (e ^ {x}) ^ {q} = e ^ {x q} = \exp (x q) \\ = \exp (\underbrace {x + x + \dots + x} _ {q \text {Summanden}}) \\ = (\exp (x)) ^ {q}, \tag {4.3.10} \\ \end{array}
$$

wo wir Satz 4.3.3 (ii) nochmals angewendet haben. Für $x = -\frac{p}{q}$ mit $p, q \in \mathbb{N}$ erhält man

$$
\begin{array}{l} e ^ {x} = \frac {1}{e ^ {\frac {p}{q}}} \stackrel {(4. 3. 1 0)} {=} \frac {1}{\exp \left(\frac {p}{q}\right)} = \frac {1}{\exp (- x)} \\ = \exp (x) \quad (\text {nach Satz 4.3.3 (iv)}). \\ \end{array}
$$

Als Nächstes stellen wir einige Wachstumseigenschaften der Exponentialfunktion fest.

## Satz 4.3.7

Es gilt:

(i) $\exp (\cdot)$ ist streng monoton wachsend:

$$
\exp (x) <   \exp (y) \quad \text { für   alle } x, y \in \mathbb {R} \text { mit } x <   y.
$$

(ii) 1 + x ist eine untere Schranke:

$$
\exp (x) \geq 1 + x \quad \text { für   alle } x \in \mathbb {R}. \tag {4.3.11}
$$

(iii)  $\exp(\cdot)$  kann in einer Umgebung von Null durch lineares Wachstum dominiert werden:

$$
| \exp (x) - 1 | \leq \frac {| x |}{1 - | x |} \quad \text {fur alle} x \in \mathbb {R} \text {mit} | x | <   1.
$$

(iv) Für x groß wächst  $\exp(x)$  schneller als jedes Polynom:

$$
\exp (x) > x ^ {n} \quad \text { für   alle } n \in \mathbb {N} \text { und } x > 4 n ^ {2}.
$$

Insbesondere gilt

$$
\lim _ {n \to \infty} \exp (- n) = 0, \quad \lim _ {n \to \infty} \exp (n) = \infty .
$$

Beweis. zu (ii): Für  $x \leq -1$  ist  $1 + x \leq 0$ . Mit  $\exp(x) > 0$  (nach Satz 4.3.3) ist (4.3.11) erfüllt. Nach dem Beweis vom Satz 4.3.1 ist für x > -1 die Folge mit den Folgengliedern

$$
\left(1 + \frac {x}{n}\right) ^ {n}
$$

monoton wachsend. Es folgt aus der Bernoulliungleichung

$$
1 + x \leq \left(1 + \frac {x}{n}\right) ^ {n} \leq \exp (x).
$$

zu (i): Seien x < y gegeben. Es gilt

$$
\frac {\exp (x)}{\exp (y)} = \frac {1}{\exp (y - x)} \stackrel {(i i)} {\leq} \frac {1}{1 + y - x} <   1.
$$

zu (iii): Für  $x \in (-1,0)$  müssen wir

$$
1 - e ^ {x} \leq \frac {- x}{1 + x}
$$

zeigen, was äquivalent zu

$$
e ^ {x} \geq 1 + \frac {x}{1 + x}
$$

ist. Dies erhalten wir aus

$$
e ^ {x} \stackrel {(i i)} {\geq} 1 + x \geq \frac {1 + 2 x}{1 + x} = 1 + \frac {x}{1 + x}.
$$

Für  $x \in [0,1)$  müssen wir

$$
e ^ {x} - 1 \leq \frac {x}{1 - x}
$$

zeigen, also

$$
e ^ {x} \leq 1 + \frac {x}{1 - x} = \frac {1}{1 - x}.
$$

Wir erinnern an folgende Tatsache aus dem Beweis von Satz 4.3.1: Für $n > x$ gilt

$$
e ^ {x} = \lim _ {n \to \infty} \left(1 + \frac {x}{n}\right) ^ {n (4. 3. 5)} \leq \lim _ {n \to \infty} \frac {1}{\left(1 - \frac {x}{n}\right) ^ {n}} \leq \frac {1}{1 - x}, \tag {4.3.12}
$$

wobei wir die Monotonie von  $\frac{1}{\left(1-\frac{x}{n}\right)^{n}}$  für die letzte Ungleichung benutzt haben.

zu (iv): Für  $x > 4n^{2}$  ist  $\sqrt{x} > 2n$ , so dass

$$
\frac {x}{2 n} > \sqrt {x}. \tag {4.3.13}
$$

Es folgt

$$
e ^ {x} > \left(1 + \frac {x}{2 n}\right) ^ {2 n (4. 3. 1 3)} > (1 + \sqrt {x}) ^ {2 n} > (\sqrt {x}) ^ {2 n} = x ^ {n},
$$

womit die Ungleichung in (iv) gezeigt ist. Es bleibt uns zu zeigen, dass die Grenzwerte wie angegeben sind. Aus  $e^{x} \geq x + 1 > x$  erhält man

$$
0 \leq \lim _ {n \to \infty} e ^ {- n} = \lim _ {n \to \infty} \frac {1}{e ^ {n}} \leq \lim _ {n \to \infty} \frac {1}{n} = 0.
$$

Andererseits gibt es für jedes $M \in \mathbb{R}$ ein $N \in \mathbb{N}$ mit $N > M$. Man erhält

$$
e ^ {n} \stackrel {(i)} {\geq} e ^ {N} > N > M \quad \text { für   alle } n \geq N.
$$

Nach Definition 4.2.4 gilt $\lim_{n\to \infty}e^n = \infty$

![](images/page_89_image_8.jpg)

Satz 4.3.3 (iii) sagt, dass

$$
\mathcal {W} (\exp (\cdot)) \subseteq (0, \infty). \tag {4.3.14}
$$

Satz 4.3.7 (iv) macht es plausibel, dass  $\mathcal{W}(\exp(\cdot)) = (0, \infty)$ . Da wir noch nicht Grenzwerte und Stetigkeit reeller Funktionen definiert haben, brauchen wir einen fundamentaleren Beweis. Wir wenden uns an das Vollständigkeitsaxiom.

## Satz 4.3.8

Der Wertebereich der Exponentialfunktion ist  $(0, \infty)$ .

Beweis. Angesichts (4.3.14) müssen wir nur zeigen, dass  $(0,\infty)\subseteq\mathcal{W}(\exp(\cdot))$ . Sei  $y\in(0,\infty)$  beliebig. Wir müssen zeigen, dass es ein  $x\in R$  gibt, so dass  $\exp(x)=y$ . Wir definieren

$$
M := \left\{x \in \mathbb {R}: e ^ {x} <   y \right\}.
$$

Wegen $\lim_{n\to \infty}e^{-n} = 0$ ist $M$ nicht leer. Ferner ist $M$ nach oben durch $y$ beschränkt, da

$$
x <   1 + x \leq e ^ {x} \leq y \quad \text { für   alle } x \in M.
$$

Nach dem Vollständigkeitsaxiom besitzt M ein Supremum s. Wir behaupten, dass

$$
e ^ {s} = y.
$$

Da $s$ das Supremum von $M$ ist, gibt es in der Tat zu jedem $n \in \mathbb{N}$ ein Element $x_{n} \in M$, so dass

$$
s - \frac {1}{n} \leq x _ {n} \leq s \tag {4.3.15}
$$

(Approximation des Supremums). Außerdem ist  $s + \frac{1}{n} \notin M$ , weil s eine obere Schranke von M ist. Also erhalten wir aus der Monotonie der Exponentialfunktion, dass

$$
e ^ {s} e ^ {- \frac {1}{n}} = e ^ {s - \frac {1}{n}} \stackrel {(4. 3. 1 5)} {\leq} e ^ {x _ {n}} <   y \leq e ^ {s + \frac {1}{n}} = e ^ {s} e ^ {\frac {1}{n}},
$$

wobei die vorletzte Ungleichung aus  $x_{n} \in M$  und die letzte Ungleichung aus  $s + \frac{1}{n} \notin M$  folgen. Aus  $\sqrt[n]{e} \to 1$  (Sehen Sie das Beispiel in (4.2.1)) und dem Sandwichkriterium folgt

$$
y = e ^ {s}.
$$

Die Exponentialfunktion taucht bei vielen Anwendungen auf. Sie ist auch wichtig für gewöhnliche Differentialgleichungen der Form

$$
\begin{array}{l} f ^ {\prime} (x) - f (x) = 0, \\ f ^ {\prime \prime} (x) - c ^ {2} f (x) = 0, \quad c \in \mathbb {R}, \\ f ^ {\prime \prime} (x) - c ^ {2} f (x) = h (x), \quad c \in \mathbb {R}, \\ \end{array}
$$

wie wir später sehen werden.

Die Exponentialfunktion erlaubt uns, die Hyperbelfunktionen zu definieren.

## Definition 4.3.9

Für alle $x \in \mathbb{R}$ definieren wir:

Sinus Hyperbolicus

$$
\sinh (x) := \frac {\exp (x) - \exp (- x)}{2},
$$

Kosinus Hyperbolicus

$$
\cosh (x) := \frac {\exp (x) + \exp (- x)}{2},
$$

Tangens Hyperbolicus

$$
\tanh (x) := \frac {\sinh (x)}{\cosh (x)}.
$$

Da  $\exp(\cdot)$  streng monoton wachsend ist, ist sie injektiv. Also besitzt  $\exp(\cdot)$  auf  $\mathcal{W}(\exp(\cdot))$  eine Umkehrfunktion. Diese Funktion ist auch wichtig für Anwendungen und wird Logarithmus genannt.

## Definition 4.3.10

Die Umkehrfunktion der Exponentialfunktion heißt Logarithmus und wird mit  $\log(\cdot)$  bezeichnet.

Aus der Definition folgt:

## Satz 4.3.11

Für den Logarithmus gilt

$$
\mathcal {D} (\log (\cdot)) = (0, \infty) =: \mathbb {R} ^ {+}, \quad \mathcal {W} (\log (\cdot)) = \mathbb {R}.
$$

Außerdem gilt

$$
\exp (\log (y)) = y \quad \text { für   alle } y \in \mathbb {R} ^ {+},
$$

$$
\log (\exp (x)) = x \quad \text {f ü r a l l e} x \in \mathbb {R},
$$

und darüberhinaus ist

$$
\log (x) <   \log (y) \quad \text { für   alle } x, y \in \mathbb {R} ^ {+} \text { mit } x <   y.
$$

Für den Logarithmus erhalten wir die erwarteten Eigenschaften und Abschätzungen, die wir im nächsten Satz sammeln.

## Satz 4.3.12: Eigenschaften

Für $\log : \mathbb{R}^{+} \to \mathbb{R}$ gilt Folgendes:

(i) Für alle  $x, y \in R^{+}$ gilt

$$
\log (x y) = \log (x) + \log (y),
$$

$$
\log \left(\frac {x}{y}\right) = \log (x) - \log (y).
$$

(ii) Für alle  $x \in R^{+}$  und  $n \in N$  gilt

$$
\log (x ^ {n}) = n \log (x).
$$

(iii) Für alle x > -1 ist

$$
\log (1 + x) \leq x.
$$

(iv) Zu jedem $c > 0$ gibt es ein $M = M(c)$, so dass

$$
\log (x) <   c x \quad \text {f ü r a l l e} x \in \mathbb {R} ^ {+} \text {mit} x > M.
$$

Bemerkung. (iv) drückt aus, dass der Logarithmus langsamer als jede lineare Funktion wächst.

Beweis. Der Beweis basiert auf der Eigenschaft der Exponentialfunktion.

zu  $((i))$ : Wir definieren  $u := \log(x)$ ,  $v := \log(y)$ . Dann ist

$$
\begin{array}{l} \log (x y) = \log (\exp (u) \cdot \exp (v)) \\ = \log (\exp (u + v)) \\ = u + v \\ = \log (x) + \log (y). \\ \end{array}
$$

Analog ist

$$
\begin{array}{l} \log \left(\frac {x}{y}\right) = \log (x y ^ {- 1}) \\ = \log (\exp (u) (\exp (v)) ^ {- 1}) \\ = \log (\exp (u) \exp (- v)) \\ = \log (\exp (u - v)) \\ = u - v \\ = \log (x) - \log (y). \\ \end{array}
$$

zu ((ii)): Man nehme $\log(x^n) = \log(\underbrace{x \cdot x \cdot \ldots \cdot x}_{n\text{ mal}})$ und wende ((i)) an.

zu ((iii)): Dies folgt aus 1 + x ≤ exp(x).

zu  $((iv))$ : Dies sollte aus dem Wachsen von  $\exp(\cdot)$  folgen. Aus  $\exp(x) > x^{n}$  für  $x > 4n^{2}$  schließen wir

$$
x > \log (x ^ {n}) = n \log (x),
$$

so dass

$$
\log (x) <   \frac {x}{n} \text {f} \text {ür} x > 4 n ^ {2}.
$$

Für $c > 0$ gegeben wählen wir $N \in \mathbb{N}$, so dass $\frac{1}{N} < c$ und wir setzen $M = 4N^2$.

Mit Hilfe der Exponentialfunktion und des Logarithmus können wir endlich die allgemeine Potenz definieren:

## Definition 4.3.13

Für $a > 0$ und $x \in \mathbb{R}$ definieren wir

$$
a ^ {x} := \exp \big (x \log (a) \big).
$$

Die Umkehrfunktion wird der Logarithmus zur Basis $a$ genannt.

Man erhält die erwarteten Eigenschaften:

## Satz 4.3.14

Für $a, b > 0$ und $x, y \in \mathbb{R}$ gilt

(i) $(ab)^x = a^xb^x,$
$(ii)(a^{x})^{y}=a^{xy},$
(iii) $a^x a^y = a^{x + y}$.

Beweis. Übung.

## 4.4 Bolzano-Weierstraß

In diesem Abschnitt entwickeln wir ein tieferes Verständnis für Zahlenfolgen und kommen insbesondere zum Satz von Bolzano-Weierstraß. Dieses Werkzeug benötigen wir später, um das Verhalten von stetigen Funktionen zu analysieren.

Grob gesagt werden wir jetzt ausdrücken, dass, obwohl eine beschränkte Folge nicht konvergieren muss, die Folge unendlich oft nah an (mindestens) einen Punkt kommt. Als motivierendes Beispiel betrachten wir

$$
a _ {n} = (- 1) ^ {n} + \frac {1}{n},
$$

die viel „Zeit“ in einer Umgebung von -1 und viel „Zeit“ in einer Umgebung von +1 verbringt. Die Folge konvergiert nicht, aber ±1 sind besondere Punkte. Um über solche Ideen deutlich reden zu können, brauchen wir ein paar Definitionen.

## Definition 4.4.1

Eine Umgebung von $x_0 \in \mathbb{R}$ ist eine Menge $U \subseteq \mathbb{R}$, so dass

$$
U \supseteq (x _ {0} - \delta , x _ {0} + \delta) \quad \text { für   ein } \delta > 0.
$$

Eine punktierte Umgebung von  $x_{0} \in R$  ist eine Menge  $V \subseteq R$ , so dass  $V = U \setminus \{x_{0}\}$ , wobei U eine Umgebung von  $x_{0}$  ist.

Also ist eine punktierte Umgebung von  $x_{0}$  eine Menge V, so dass gilt

- $x_0 \notin V$, und
- es gibt ein $\delta > 0$, so dass $(x_0 - \delta, x_0) \cup (x_0, x_0 + \delta)$ in $V$ enthalten ist.

## Definition 4.4.2

Es sei $\{x_{n}\}_{n=1}^{\infty}$ eine Zahlenfolge. Dann heißt $x_{0} \in \mathbb{R}$ ein Häufungspunkt der Folge, wenn jede Umgebung von $x_{0}$ unendlich viele Folgenglieder enthält.

Es sei M eine Menge reeller Zahlen. Dann heißt  $x_{0} \in R$  ein Häufungspunkt der Menge, wenn jede Umgebung von  $x_{0}$  unendlich viele Elemente von M enthält.

## Beispiele.

① -1 und +1 sind Häufungspunkte von  $\left\{(-1)^{n}+\frac{1}{n}\right\}_{n=1}^{\infty}$ .
② 1 ist ein Häufungspunkt von  $(0,2)$  und von  $(1,2)$ .
③ N besitzt keine Häufungspunkte.
④ Die Menge aller Häufungspunkte von  $\{x \in Q : 0 \leq x \leq 2\}$  ist [0, 2].

Bemerkung.  $x_{0}$  ist genau dann ein Häufungspunkt von  $M \subseteq R$ , wenn jede Umgebung von  $x_{0}$  mindestens ein  $x \in M$  mit  $x \neq x_{0}$  enthält.

Bemerkung. Eine Menge heißt abgeschlossen, wenn sie alle ihre Häufungspunkte enthält. Wir sprechen ausführlich über offene und abgeschlossene Mengen in HMII (Kapitel 3).

Im Beispiel oben bemerkt man, dass, obwohl  $\left\{(-1)^{n}+\frac{1}{n}\right\}_{n=1}^{\infty}$  nicht konvergiert, die Folge der Folgenglieder mit geradem Index

$$
(- 1) ^ {2 n} + \frac {1}{2 n}
$$

doch konvergiert.

Wir möchten jetzt ähnliches Verhalten für allgemeine Folgen bemerken. Wir fangen mit einer Definition an.

## Definition 4.4.3

Es seien  $\{a_{n}\}_{n=1}^{\infty}$  eine Zahlenfolge und  $\{n_{k}\}_{k=1}^{\infty}$  eine streng monoton wachsende Folge natürlicher Zahlen. Dann heißt

$$
\{a _ {n _ {1}}, a _ {n _ {2}}, \dots , \} = \{a _ {n _ {k}} \} _ {k = 1} ^ {\infty}
$$

eine Teilfolge von  $\{a_{n}\}_{n=1}^{\infty}$ .

Also sind

$$
\left\{(- 1) ^ {2 n} + \frac {1}{2 n} \right\} _ {n = 1} ^ {\infty} \text {und} \left\{(- 1) ^ {2 n + 1} + \frac {1}{2 n + 1} \right\} _ {n = 1} ^ {\infty}
$$

konvergente Teilfolgen von  $\left\{(-1)^{n}+\frac{1}{n}\right\}_{n=1}^{\infty}$ . Als weiteres Beispiel betrachten wir

$$
\left\{\cos \left(\frac {(- 1) ^ {n} + 1}{2} \pi\right) \right\} _ {n = 1} ^ {\infty},
$$

die die konvergente Teilfolge  $\{-1, -1, -1, \ldots\}$  besitzt.

## Satz 4.4.4

Die Folge  $\{x_{n}\}_{n=1}^{\infty}$  hat  $x_{0}$  als Häufungspunkt genau dann, wenn es eine Teilfolge gibt, die gegen  $x_{0}$  konvergiert.

Beweis. (Hinrichtung): Wir nehmen zunächst an, dass  $x_{0}$  ein Häufungspunkt der Folge ist. Dann enthält  $(x_{0}-1,x_{0}+1)$  ein Folgenglied  $x_{N}, N\in N$ . Wir setzen

$$
n _ {1} := N.
$$

Analog existiert für jedes  $k \in N$  ein  $N(k) \in \mathbb{N}$ , so dass  $N(k) > N(k - 1)$  und

$$
x _ {N (k)} \in \big (x _ {0} - \frac {1}{k}, x _ {0} + \frac {1}{k} \big).
$$

Wir setzen

$$
n _ {k} = N (k).
$$

Für die Teilfolge $\{x_{n_k}\}_{k=1}^{\infty}$ so definiert gilt

$$
| x _ {n _ {k}} - x _ {0} | \leq \frac {1}{k},
$$

also konvergiert die Teilfolge gegen  $x_{0}$ .

(Rückrichtung): Wenn eine Teilfolge  $\{x_{n_{k}}\}_{k=1}^{\infty}$  gegen  $x_{0}$  konvergiert, dann gibt es für jedes  $\delta > 0$  ein  $K \in N$ , so dass

$$
x _ {n _ {k}} \in (x _ {0} - \delta , x _ {0} + \delta) \quad \text { für   alle } k \geq K.
$$

Also enthält jede Umgebung unendlich viele Folgenglieder.

Man kann auch durch Teilfolgen ein neues Konvergenz-Kriterium einführen:

## Satz 4.4.5

Die Folge $\{x_{n}\}_{n = 1}^{\infty}$ konvergiert genau dann, wenn jede Teilfolge konvergiert.

Beweis. Übung.

Bemerkung. Bemerken Sie, dass Konvergenz jeder Teilfolge einer Folge impliziert, dass jede Teilfolge den gleichen Grenzwert hat.

Die Folge  $\{n\}_{n=1}^{\infty}$ , die keinen Häufungspunkt besitzt, hat einen Mindestabstand von eins zwischen zwei beliebigen Folgengliedern. Kann eine beschränkte Folge  $\{a_{n}\}_{n=1}^{\infty}$  keinen Häufungspunkt besitzen? Können Folgenglieder alle voneinander weglaufen? Der Satz von Bolzano-Weierstraß sagt uns, dass die Antwort nein ist.