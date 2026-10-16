# Kapitel 1 – Zahlen und Vektoren

原始 PDF 第 17–73 页。

# Kapitel 1

# Zahlen und Vektoren

## §1. Mengen und Abbildungen

1.1 Mengen. Zur Festlegung von Bezeichnungen erinnern wir zuerst an einige Begriffe aus der Mengenlehre. Von G. CANTOR stammt folgende Erklärung (1895):

Unter einer Menge verstehen wir jede Zusammenfassung von bestimmten wohlunterschiedenen Objekten unserer Anschauung oder unseres Denkens zu einem Ganzen.

Wir werden Mengen mit Großbuchstaben bezeichnen. Die Objekte der Menge A werden die Elemente von A genannt. Man schreibt  $a \in A$  (bzw.  $a \notin A$ ), wenn das Objekt a ein (bzw. kein) Element von A ist.

$$
A = \left\{a _ {1}, a _ {2}, \dots , a _ {n} \right\}
$$

kennzeichnet eine Menge mit endlich vielen Elementen (endliche Menge). Hierbei kommt es nicht auf die Reihenfolge der Elemente an. Die häufigste Beschreibung einer Menge X geschieht durch die Angabe einer Eigenschaft E, die genau allen Elementen von X zukommt. In diesem Fall schreibt man

$$
X = \left\{x ; x \text {hat die Eigenschaft} E \right\},
$$

bzw.  $X = \{ x \in A ; x \text{ hat die Eigenschaft } E \}$ ,

wenn besonders hervorgehoben werden soll, daß die in X zusammengefaßten Elemente sämtlich in der Grundmenge A liegen.

Zur Vermeidung von Fallunterscheidungen wird die leere Menge ∅ eingeführt; sie enthält kein Element.

B heißt Teilmenge von A, in Zeichen  $B \subseteq A$ , wenn jedes Element von B auch ein Element von A ist. Man nennt die Mengen gleich, i.Z. A = B, wenn sowohl  $B \subseteq A$  als auch  $A \subseteq B$  gilt. Beziehungen der Form  $B \subseteq A$  heißen (Mengen-)Inklusionen; die strikte Inklusion  $B \subsetneq A$  bedeutet  $B \subseteq A$  und es gibt wenigstens ein  $a \in A$  mit  $a \notin B$ .

1.2 Mengenoperationen. Für je zwei Mengen A und B sind der Durchschnitt  $A \cap B$ , die Vereinigung  $A \cup B$  und das Komplement  $A \setminus B$  definiert durch

$$
\begin{array}{l} A \cap B := \{x; x \in A \text {und} x \in B \}; \\ A \cup B := \{x; x \in A \text {oder} x \in B \}; \\ A \setminus B := \{x; x \in A \text {und} x \notin B \}. \\ \end{array}
$$

K. Meyberg et al., Höhere Mathematik

© Springer-Verlag Berlin Heidelberg 1998

---

2

1. Zahlen und Vektoren

(Das Zeichen := bzw. =: bedeutet Gleichheit per definitionem, wobei der Doppelpunkt bei dem zu definierenden Ausdruck steht.)

![](../../raw/pages_0001-0032/images/page_17_image_3.jpg)

Abb. 1 - Venn-Diagramme

Zwei Mengen A und B, die kein gemeinsames Element besitzen, heißen disjunkt, d.h. für sie gilt  $A \cap B = \emptyset$ . Als direktes (oder kartesisches) Produkt der Mengen A und B bezeichnet man die Paarmenge

$$
A \times B := \left\{(a, b); a \in A, b \in B \right\},
$$

wobei es in $(a,b)$ auf die Reihenfolge der Elemente ankommt, d.h. $(a,b) = (a',b')$ genau dann, wenn $a = a'$ und $b = b'$. Entsprechend werden geordnete $n$-Tupel $(a_1,a_2,\ldots ,a_n)$ und $(b_{1},b_{2},\ldots ,b_{n})$ mit Elementen $a_i,b_i\in A_i$ $(i = 1,2,\dots,n)$ als gleich bezeichnet, wenn sie „komponentenweise“ übereinstimmen, also wenn $a_{i} = b_{i}$ gilt für $i = 1,2,\dots,n$. Das direkte Produkt der Mengen $A_{1},A_{2},\ldots ,A_{n}$ ist

$$
A _ {1} \times A _ {2} \times \dots \times A _ {n} := \left\{\left(a _ {1}, a _ {2}, \dots , a _ {n}\right); a _ {i} \in A _ {i} \quad (i = 1, 2, \dots , n) \right\}.
$$

Im Fall  $A_{1}=A_{2}=\cdots A_{n}=A$  schreibt man dafür  $A^{n}$ .

1.3 Abbildungen. $A$ und $B$ seien Mengen. Eine Abbildung (oder Funktion) $f$ von $A$ in (oder nach) $B$, in Zeichen $f: A \to B$ (oder elementweise $x \mapsto f(x)$, $x \in A$), ist eine Vorschrift, die jedem Element $x \in A$ genau ein Element $f(x) \in B$ zuordnet. Man nennt $A$ den Definitionsbereich und die Elemente von $A$ die Argumente der Abbildung $f$; $f(x)$ heißt das Bild von $x$ unter $f$ (oder Funktionswert von $f$ an der Stelle $x$). Gehören zu verschiedenen Argumenten stets verschiedene Bilder (d.h. $x_1 \neq x_2 \Rightarrow f(x_1) \neq f(x_2)$, bzw. äquivalent dazu: $f(x_1) = f(x_2) \Rightarrow x_1 = x_2$), dann heißt $f$ injektiv. Für jede Teilmenge $C \subseteq A$ bezeichnet man $f(C) := \{f(x); x \in C\}$ als Bild von $C$ unter $f$ und das ganze Bild $f(A)$ als Wertebereich von $f$. Im Fall $f(A) = B$ sagt man, $f$ ist eine Abbildung von $A$ auf $B$ oder $f$ ist surjektiv. Man nennt die Abbildung $f: A \to B$ bijektiv, wenn sie sowohl surjektiv als auch injektiv ist. Es ist also $f: A \to B$ genau dann bijektiv, wenn es zu jedem Element $y \in B$ genau ein $x \in A$ gibt mit $y = f(x)$. In diesem Fall existiert die mit $f^{-1}: B \to A$ bezeichnete Umkehrabbildung, mit der jedem $y \in B$ das durch $y = f(x)$ eindeutig bestimmte $x \in A$ zugeordnet wird. Die auf jeder Menge $A$ erklärte Abbildung $Id: A \to A$, $Id(x) := x$ für alle $x \in A$, heißt identische Abbildung (oder Identität) auf $A$.

Zwei Abbildungen $f: A \to B$ und $g: C \to D$ sind genau dann gleich, i.Z. $f = g$, wenn gilt $A = C$, $B = D$ und $f(x) = g(x)$ für alle $x \in A$. Durch

---

§2. Die reellen Zahlen

3

Einschränkung des Definitionsbereiches einer Abbildung $f: A \to B$ auf eine Teilmenge $A_0 \subseteq A$ gewinnt man die Restriktion

$$
f \mid A _ {0}: A _ {0} \rightarrow B, (f \mid A _ {0}) (x) := f (x) \text { für   alle } x \in A _ {0}.
$$

![](../../raw/pages_0001-0032/images/page_18_image_4.jpg)

<details>
<summary>text_image</summary>

f: A → B
x
A
f(x)
B
</details>

Abb. 2 - $f: A \to B$

## §2. Die reellen Zahlen

2.1 Bezeichnungen. Die Menge aller reellen Zahlen wird mit R bezeichnet. Besonders gekennzeichnete Teilmengen von R sind

$$
\mathbb {N} = \{1, 2, 3, 4, \dots \} \quad (\text {Menge der natürlichen Zahlen}),
$$

$$
\mathbb {N} _ {0} = \mathbb {N} \cup \{0 \},
$$

$$
\mathbb {Z} = \{\dots , - 3, - 2, - 1, 0, 1, 2, 3, \dots \} \quad (\text {Menge der ganzen Zahlen}),
$$

$$
\mathbb {Q} = \left\{\frac {m}{n}; m, n \in \mathbb {Z}, n \neq 0 \right\} \quad (\text {Menge der rationalen Zahlen}).
$$

Neben den rationalen Zahlen, die man auch charakterisieren kann als diejenigen reellen Zahlen mit einer endlichen oder periodisch unendlichen Dezimalbruchdarstellung, gibt es in $\mathbb{R}$ die irrationalen Zahlen, die eine unendliche nichtperiodische Dezimalbruchdarstellung besitzen. Der periodische Dezimalbruch $c = 0.\overline{b_1b_2\ldots b_k} = 0.b_1b_2\ldots b_kb_1b_2\ldots b_kb_1b_1\ldots$ hat die „gewöhnliche“ Bruchdarstellung

$$
c = \frac {b _ {1} b _ {2} \dots b _ {k}}{\underbrace {9 9 \dots 9} _ {k - m a l}}; \text {denn} 1 0 ^ {k} c - c = b _ {1} b _ {2} \dots b _ {k}.
$$

Beispiele. Die Zahlen $\frac{16}{37}$, 0.12123, $0.17\overline{314} = 0.17314314$ ... sind rational, 0.12345 ..., 0.101001000 ..., $\sqrt{2} = 1.4142$ ... sind irrational. Es gilt

$$
0. \overline {{3 1 4}} = \frac {3 1 4}{9 9 9}, 0. 1 7 \overline {{3 1 4}} = \frac {1 7}{1 0 0} + \frac {3 1 4}{1 0 0 \cdot 9 9 9}.
$$

Zur Veranschaulichung von $\mathbb{R}$ dient die bekannte, von - nach + orientierte Zahlengerade, auf der jeder Punkt genau einer Zahl entspricht.

2.2 Ungleichungen. Unter einer Ungleichung (für Zahlen  $x, y \in R$ ) verstehen wir einen Größenvergleich der Form x < y (x ist kleiner als y, strikte Ungleichung) oder  $x \leq y$  (x ist kleiner oder gleich y, nicht strikte Ungleichung); eine andere Schreibweise hierfür ist y > x oder  $y \geq x$ . Die Ungleichung  $x \leq y$

---

4

1. Zahlen und Vektoren

(bzw. $x < y$) gibt eine Abschätzung der Zahl $x$ nach oben durch $y$ an, oder auch eine Abschätzung der Zahl $y$ nach unten durch $x$. In der Praxis (und in diesem Buch) wird überwiegend mit Ungleichungen der Form $x \leq y$ gearbeitet, ohne darauf zu achten, welcher der beiden hierin enthaltenen Fälle $x < y$ oder $x = y$ tatsächlich vorliegt; wesentlich ist die Aussage „$x$ ist nicht größer als $y$“.

Für Abschätzungen einer Summe und eines Produkts sind

$$
x \leq y, a \leq b \implies x + a \leq y + b,
$$

$$
x \leq y, 0 \leq a \implies x a \leq y a
$$

zu beachten. Ferner gilt

$$
x \leq y \iff - y \leq - x,
$$

$$
0 <   x \leq y \iff 0 <   \frac {1}{y} \leq \frac {1}{x}.
$$

Beispiel.  $-3a-2\leq5\leq-3a+4$   $\Longleftrightarrow$   $(-3a\leq7$  und  $1\leq-3a)$   $\Longleftrightarrow$

$$
- \frac {1}{3} \geq a \geq - \frac {7}{3}.
$$

![](../../raw/pages_0001-0032/images/page_19_image_11.jpg)

2.3 Intervalle. Seien $a, b \in \mathbb{R}$ mit $a < b$. Die Menge $[a, b] := \{x \in \mathbb{R} ; a \leq x \leq b\}$ heißt abgeschlossenes Intervall mit Randpunkten $a, b$. Im offenen Intervall $(a, b) := \{x \in \mathbb{R} ; a < x < b\}$ sind $a, b$ nicht enthalten. Analog sind die halboffenen Intervalle $(a, b]$ und $[a, b)$ definiert.

Zur Vermeidung von Fallunterscheidungen ist es günstig, noch zwei Symbole  $-\infty,\infty$  (minus Unendlich, Unendlich) einzuführen und hierfür  $-\infty < x < \infty$  für alle  $x \in R$  festzulegen.  $(-\infty,a] := \{x \in \mathbb{R} ; x \leq a\}, (b,\infty) := \{x \in \mathbb{R} ; b < x\}$ . Analog  $(-\infty,a), [b,\infty)$ . Auch  $\mathbb{R} = (-\infty,\infty)$  fällt damit unter die offenen Intervalle. Das offene Intervall  $(a - \varepsilon, a + \varepsilon)$  (mit  $\varepsilon > 0$ ) heißt  $\varepsilon$ -Umgebung der Zahl (des Punktes)  $a \in R$ .

2.4 Schranken. Man nennt eine Menge $S$ reeller Zahlen nach oben beschränkt, wenn es eine Zahl $b \in \mathbb{R}$ gibt, so daß $S \subseteq (-\infty, b]$. In diesem Fall heißt $b$ eine obere Schranke von $S$. Ganz entsprechend nennt man $a \in \mathbb{R}$ eine untere Schranke von $S$, und $S$ nach unten beschränkt, wenn $S \subseteq [a, \infty)$. Die Menge $S \subseteq \mathbb{R}$ heißt beschränkt, wenn sie eine untere Schranke $a$ und eine obere Schranke $b$ besitzt. In diesem Fall gilt $S \subseteq [a, b]$.

Ist $S \subseteq \mathbb{R}$ nach oben beschränkt, so nennen wir die kleinste obere Schranke $s$ das Supremum von $S$, in Zeichen $s = \sup S$. Ebenso wie die anderen Schranken braucht sup $S$ nicht der Menge $S$ anzugehören; jedoch gibt es zu jeder beliebig kleinen Zahl $\varepsilon > 0$ ein $x \in S$ mit $s - \varepsilon < x \leq s$. Andernfalls würde $x \leq s - \varepsilon$ für alle $x \in S$ gelten und wir hätten die noch kleinere Schranke $s - \varepsilon$.

Beispiel 1. $\sup [a,b] = \sup (a,b) = b$

![](../../raw/pages_0001-0032/images/page_19_image_17.jpg)

Beispiel 2. $\sup \{x\in \mathbb{Q};x^2 < 2\} = \sqrt{2}$

![](../../raw/pages_0001-0032/images/page_19_image_19.jpg)

---

§2. Die reellen Zahlen

5

Es ist keineswegs selbstverständlich, daß die Menge der oberen Schranken von  $S \subseteq (-\infty, b]$  eine kleinste Zahl enthält. Dieses ist aber eine der Grundannahmen über die reellen Zahlen:

Das Vollständigkeitsaxiom. Jede nach oben beschränkte Menge reeller Zahlen besitzt ein Supremum.

Damit hat auch jede nach unten beschränkte Menge $U \subseteq \mathbb{R}$ eine größte untere Schranke (ein Infimum, i.Z. inf $U$). Man bestätigt leicht die Beziehung

$$
\inf U = - \sup \left\{- u; u \in U \right\}.
$$

Beispiel. $\inf \left\{1 + \frac{1}{n}; n \in \mathbb{N}\right\} = 1$.

2.5 Der Betrag $|a|$ einer reellen Zahl $a \in \mathbb{R}$ ist definiert durch

$$
\boxed | a | := \left\{ \begin{array}{c l} a, & \text {falls} a \geq 0 \\ - a, & \text {falls} a <   0. \end{array} \right.\}
$$

Die folgenden Rechenregeln für Beträge ergeben sich unmittelbar aus der Definition:

$$
- | a | \leq a \leq | a |, \quad | - a | = | a |,
$$

$$
| a b | = | a | | b |, \quad \left| \frac {a}{b} \right| = \frac {| a |}{| b |} \quad (\text {falls} b \neq 0),
$$

und $|a| \leq b \iff -b \leq a \leq b$.

Aus  $-|a| \leq a \leq |a|$  und  $-|b| \leq b \leq |b|$  folgt  $-(|a| + |b|) \leq a + b \leq |a| + |b|$ . Also gilt für alle  $a, b \in R$ :

$$
| a + b | \leq | a | + | b | \quad (\text {Dreiecksungleichung}). \tag {1}
$$

Es ist $|a - b|$ der Abstand der zu $a$ und $b$ gehörenden Punkte auf der Zahlengeraden; also gilt für alle $x, a, \varepsilon \in \mathbb{R}$, $\varepsilon > 0$:

$$
| x - a | \leq \varepsilon \iff a - \varepsilon \leq x \leq a + \varepsilon . \tag {2}
$$

$$
\mathbb {R} \quad a - \varepsilon \quad a \quad a + \varepsilon
$$

$$
\text {Abb. 3 - Das Intervall} \{x \in \mathbb {R}; | x - a | \leq \varepsilon \}.
$$

Wird für eine Zahl $a \in \mathbb{R}$ ein Näherungswert $\bar{a}$ angegeben, so bedeutet die Schreibweise $a = \bar{a} \pm \varepsilon$ dasselbe wie $|a - \bar{a}| \leq \varepsilon$.

Beispiel.  $\bar{a}=1.414215$  ist ein Näherungswert für  $a=\sqrt{2}$ . Es gilt  $\bar{a}^{2}\geq2$ , folglich  $\frac{2}{\bar{a}}\leq\sqrt{2}\leq\bar{a}$  und damit  $|\bar{a}-\sqrt{2}|\leq|\bar{a}-\frac{2}{\bar{a}}|\leq0.000003$  oder  $\sqrt{2}=1.414215\pm3\cdot10^{-6}$ .

---

6

1. Zahlen und Vektoren

2.6 Die vollständige Induktion. Die Gültigkeit einer Aussage  $A(n)$  für jede ganze Zahl  $n \geq n_{0}$  mit vollständiger Induktion nachzuweisen bedeutet:

1. Der Induktionsbeginn: Man zeigt, daß  $A(n)$  für  $n = n_{0}$  gilt.
2. Der Schluß von n auf  $n+1$ : Für ein beliebiges  $n \geq n_{0}$  setzt man die Gültigkeit von  $A(n)$  voraus (Induktionsvoraussetzung) und leitet daraus die Gültigkeit von  $A(n+1)$  ab.

Können beide Schritte ausgeführt werden, dann gilt $A(n)$ für alle $n \geq n_0$. Denn nach dem ersten Schritt gilt $A(n_0)$, nach dem zweiten Schritt $A(n_0 + 1)$ und ebenso (immer wieder Schluß von $n$ auf $n + 1$) $A(n_0 + 2)$, $A(n_0 + 3)$, ...

Beispiel 1.

$$
1 + 2 + \dots + n = \frac {n (n + 1)}{2} \qquad (n \in \mathbb {N}).
$$

Beweis mit vollständiger Induktion. Induktionsbeginn $n = 1: 1 = \frac{1 \cdot 2}{2}$. Schluß von $n$ auf $n + 1$: Sei $n \in \mathbb{N}$ (beliebig) und die Formel richtig für dieses $n$. Dann folgt $1 + 2 + \cdots + n + (n + 1) = \frac{n(n + 1)}{2} + n + 1 = \frac{(n + 1)(n + 2)}{2}$. Das ist die zu beweisende Formel für $n + 1$. Sie gilt also für alle $n \in \mathbb{N}$.

Beispiel 2. Die Bernoulli-Ungleichung. Für $h \in \mathbb{R}$ und alle $n \in \mathbb{N}$ gilt

(3) $(1+h)^{n}\geq1+nh,\quad\text{falls }h\geq-1.$

Beweis mit vollständiger Induktion. Induktionsbeginn $n = 1: (1 + h)^{1} \geq 1 + 1 \cdot h$. Schluß von $n$ auf $n + 1$:

Aus  $(1+h)^{n} \geq 1 + nh$  (Induktionsvoraussetzung) und  $1 + h \geq 0$  folgt

$$
(1 + h) ^ {n + 1} \geq (1 + n h) (1 + h) \geq 1 + (n + 1) h.
$$

Definition durch Rekursion. Diese Methode beruht auf dem Prinzip der vollständigen Induktion: Eine Größe $A_{n}$ wird für alle $n \in \mathbb{N}_{0}$ dadurch definiert, daß man

1.  $A_{0}$  festlegt,
2.  $A_{k}$  für  $k \leq n$  als bekannt ansieht und  $A_{n+1}$  durch diese ausdrückt.

Beispiel 3. Die Potenzen $a^n$ für eine beliebige Basiszahl $a \in \mathbb{R}$ und Exponenten $n \in \mathbb{N}_0$ werden definiert durch $a^0 := 1$; $a^{n+1} := a^n a$.

Beispiel 4. Die Fakultäten. Zu $n \in \mathbb{N}_0$ wird $n!$ (lies: $n$ Fakultät) definiert durch $0! := 1$; $(n+1)! := n!(n+1)$. Demnach gilt

$$
n! = \left\{ \begin{array}{c l} n (n - 1) (n - 2) \dots 2 \cdot 1 & , n \geq 1, \\ 1 & , n = 0. \end{array} \right.
$$

---

§2. Die reellen Zahlen

7

So ist etwa $6! = 1 \cdot 2 \cdot 3 \cdot 4 \cdot 5 \cdot 6 = 720$, $9! = 362880$. Die Fakultäten werden mit wachsendem $n$ schnell sehr groß.

Als Permutationen einer Menge A bezeichnet man die bijektiven Abbildungen von A auf sich. Ist A endlich mit den n verschiedenen Elementen  $\{a_{1},\ldots,a_{n}\}$ , so interpretiert man eine Permutation von A als Zuordnung der  $a_{i}$  zu den n verschiedenen Plätzen

$$
\begin{array}{c} (\quad * \quad , \quad * \quad , \quad \dots \quad , \quad *) \\ \uparrow \quad \uparrow \quad \uparrow \\ 1. \text {Platz} \quad 2. \text {Platz} \quad \text {n - ter Platz} \end{array}
$$

so daß auf jeden Platz genau ein Element kommt; etwa  $(a_{1}, a_{2}, \ldots, a_{n})$  oder  $(a_{3}, a_{1}, a_{2}, a_{4}, \ldots, a_{n})$ . Für jedes  $n \in N$  gilt:

(4) Jede n-elementige Menge besitzt genau n! verschiedene Permutationen.

Beweis mit vollständiger Induktion. Induktionsbeginn: (4) gilt für $n = 1$. Schluß von $n$ auf $n + 1$: Es gibt (nach Induktionsvoraussetzung) $n!$ Permutationen von $\{a_1, \ldots, a_{n+1}\}$ mit $a_1$ an der ersten Stelle. Ebensoviele mit $a_1$ an der zweiten Stelle, etc.; das sind insgesamt $n!(n + 1) = (n + 1)!$ verschiedene Permutationen.

Beispiel 5. Das Summen- und Produktzeichen. Für die Summe und das Produkt der Zahlen $a_{m}, a_{m+1}, \ldots, a_{n} \in \mathbb{R}$ (mit $m \leq n$) schreibt man

$$
\boxed {a _ {m} + a _ {m + 1} + \dots + a _ {n} = \sum_ {k = m} ^ {n} a _ {k}, \quad a _ {m} \cdot a _ {m + 1} \dots a _ {n} = \prod_ {k = m} ^ {n} a _ {k}.}
$$

Die Definition durch Rekursion ersetzt die Pünktchen:

$$
\sum_ {k = m} ^ {m} a _ {k} := a _ {m}, \quad \sum_ {k = m} ^ {n + 1} a _ {k} := \left(\sum_ {k = m} ^ {n} a _ {k}\right) + a _ {n + 1}.
$$

Man beachte die Unabhängigkeit vom Summationsindex, $\sum_{k=m}^{n} a_k = \sum_{i=m}^{n} a_i$, ferner $\sum_{k=m}^{n} a_k = \sum_{k=m}^{l} a_k + \sum_{k=l+1}^{n} a_k \quad (m \leq l \leq n)$. Analoges gilt für das Produktzeichen. Z. B. ist $\sum_{k=1}^{n} k = \frac{n(n+1)}{2} \quad (\rightarrow \text{Bsp. 1}), \quad \prod_{k=1}^{n} k = n!$ $(\rightarrow \text{Bsp. 3})$ und es gilt die geometrische Summenformel:

$$
\boxed {\sum_ {k = 0} ^ {n} q ^ {k} = 1 + q + q ^ {2} + \dots + q ^ {n} = \left\{ \begin{array}{c l} \frac {1 - q ^ {n + 1}}{1 - q} & , \text {falls} q \neq 1, \\ n + 1 & , \text {falls} q = 1. \end{array} \right.} \tag {5}
$$

---

8

1. Zahlen und Vektoren

Zum Beweis multipliziere man die Gleichung im Falle  $q \neq 1$  mit 1 - q durch.

Mit vollständiger Induktion erhält man aus der Dreiecksungleichung (1):

$$
\left| \sum_ {k = m} ^ {n} a _ {k} \right| \leq \sum_ {k = m} ^ {n} \left| a _ {k} \right|. \tag {6}
$$

2.7 Binomialkoeffizienten und die binomische Formel. Für zwei ganze Zahlen $n, k$ mit $0 \leq k \leq n$ bezeichnet man die ganze Zahl - lies: $n$ über $k$-

$$
\boxed {\binom {n} {k} := \frac {n !}{k ! (n - k) !} = \frac {n (n - 1) \cdot \dots \cdot (n - k + 1)}{k !}} \tag {7}
$$

als Binomialkoeffizient. Der Name rührt von der binomischen Formel her (→ Satz 2.2), die Bedeutung beruht auf

Satz 2.1. Eine Menge mit n Elementen besitzt  $\binom{n}{k}$  verschiedene k-elementige Teilmengen. Mit anderen Worten: Es gibt  $\binom{n}{k}$  Möglichkeiten, aus insgesamt n Objekten genau k auszuwählen.

Beweis. Man findet sämtliche $k$-elementigen Teilmengen der Menge $S = \{a_1, a_2, \ldots, a_n\}$ - die $a_i$ paarweise verschieden - wenn man aus allen $n!$ Anordnungen nur jeweils die ersten $k$ Elemente nimmt. Die durch die Anordnung (Permutation) $(a_{i_1}, a_{i_2}, \ldots, a_{i_k}, \ldots, a_{i_n})$ bestimmte Teilmenge $\{a_{i_1}, \ldots, a_{i_k}\}$ von $S$ tritt dabei $k!(n-k)!$ - mal auf.

Beispiel 1. Im Lotto „6 aus 49“ gibt es

$$
\binom {4 9} {6} = \frac {4 9 \cdot 4 8 \cdot 4 7 \cdot 4 6 \cdot 4 5 \cdot 4 4}{1 \cdot 2 \cdot 3 \cdot 4 \cdot 5 \cdot 6} = 1 3 9 8 3 8 1 6
$$

verschiedene Möglichkeiten 6 „Richtige“ zu ziehen (→ Aufg. 9).

Aus der Definition (7) liest man sofort die Beziehung

$$
\binom{n}{k} = \binom{n}{n - k}
$$

und einfache Sonderfälle ab:

$$
\binom {n} {0} = \binom {n} {n} = 1, \quad \binom {n} {1} = \binom {n} {n - 1} = n, \quad \binom {n} {2} = \binom {n} {n - 2} = \frac {n (n - 1)}{2}.
$$

Ebenso bestätigt man mit (7) die Rekursionsformel

$$
\binom {n + 1} {k} = \binom {n} {k - 1} + \binom {n} {k}. \tag {8}
$$

Damit lassen sich die Binomialkoeffizienten durch Additionen berechnen:

---

§2. Die reellen Zahlen

9

Beginnend mit $n = 1$ schreibt man die Zahlen $\binom{n}{0}, \binom{n}{1}, \ldots, \binom{n}{n}$ in eine Zeile; dabei ist erstes und letztes Element durch $\binom{n}{0} = \binom{n}{n} = 1$ bestimmt.

Die Zahlen $\binom{n+1}{k}$ der nächsten Zeile werden „auf Lücke“ gesetzt (→ Schema). Man beginnt mit der etwas nach links versetzten $1 = \binom{n+1}{0}$ und berechnet die folgenden Zahlen nach (8) als Summe der beiden darüber stehenden Zahlen. Die Zeile wird mit $1 = \binom{n+1}{n+1}$ abgeschlossen. Auf diese Weise entsteht das sogenannte Pascal-Dreieck.

$$
\begin{array}{l} \binom{1}{k}: \quad 1 \quad 1 \\ \binom {2} {k}: \quad 1 \quad 2 \quad 1 \\ \binom {3} {k}: \quad 1 \quad 3 \quad 3 \quad 1 \\ \binom {4} {k}: \quad 1 \quad 4 \quad 6 \quad 4 \quad 1 \\ \(\binom {5} {k}: \quad 1 \quad 5 \quad 10 \quad 10 \quad 5 \quad 1 + \\ \(\binom {6} {k}: \quad 1 \quad 6 \quad 1 5 \quad 2 0 \quad 1 5 \quad 6 \quad 1 \\ \end{array}
$$

Satz 2.2. Die binomische Formel. Für beliebige Zahlen $a, b \in \mathbb{R}$ und jede ganze Zahl $n \geq 0$ gilt

$$
(a + b) ^ {n} = \sum_ {k = 0} ^ {n} \binom {n} {k} a ^ {n - k} b ^ {k} .
$$

Beweis. Beim Ausmultiplizieren kommt $b^k$ so oft vor, wie man $k$ Faktoren aus $n$ Faktoren auswählen kann, also $\binom{n}{k}$-mal ($\rightarrow$ Satz 2.1). $a^{n-k}$ stammt aus den anderen $n-k$ Faktoren.

Beispiel 2. $(a + b)^{5} = a^{5} + 5a^{4}b + 10a^{3}b^{2} + 10a^{2}b^{3} + 5ab^{4} + b^{5}$.

Beispiel 3.  $(1+x)^{n}=\sum_{k=0}^{n}\binom{n}{k}x^{k}=1+nx+\frac{n(n-1)}{2}x^{2}+\cdots+nx^{n-1}+x^{n}.$  ☐

Beispiel 4. $2^{n} = (1 + 1)^{n} = \sum_{k=0}^{n}\binom{n}{k} = \binom{n}{0} + \binom{n}{1} + \cdots +\binom{n}{n}.$

Diese Formel hat eine schöne Anwendung: Eine Menge mit n Elementen hat  $2^{n}$  verschiedene Teilmengen ( $\rightarrow$  Satz 2.1, die leere Menge wird als 0-elementige Menge mitgezählt). □

## Aufgaben

1. Man schreibe $\sum_{k=1}^{n} 47 \cdot 10^{-2k}$ als Dezimalbruch. Welchen Bruch liefert die Summenformel der geometrischen Reihe?

---

10

1. Zahlen und Vektoren

2. Man ermittle sämtliche reellen Lösungen und skizziere die zugehörigen Bereiche auf dem Zahlenstrahl:

a) $\sqrt{2x - 4} -\sqrt{x - 1} = 1$ ;

b) $3 - x < 4 - 2x$;

c) $x^{3} - x^{2} < 2x - 2$;

d) $||x| - |-5| < 1$;

3. Skizziere die Bereiche der  $(x,y)$ -Ebene, für welche

a) $|x| \leq |y|$;

b) $|x| + |y| \leq 1$.

4. Welche reellen Zahlen x erfüllen

a) $|x + 1| - |x - 1| = 1$;

b) $\frac{1}{x} < \frac{1}{x + 1}$;

c) $6x^{2} - 13x + 6 < 0$ ;

d) $\sqrt{7x + 15} -\sqrt{10 - 2x} = \sqrt{1 + 5x}$ ?

5. Man skizziere die Bereiche der  $(x, y)$ -Ebene:

a) $|x| + |y| = 2$;

b) $|x| \leq 5$ und $|y| \leq 5$;

c) $|x| \leq 5$ oder $|y| \leq 5$.

6. a) Man berechne den Wert des Binomialkoeffizienten  $\begin{pmatrix}753\\750\end{pmatrix}$ .

b) Verifiziere am Pascalschen Dreieck  $\binom{6}{3} = \binom{2}{2} + \binom{3}{2} + \binom{4}{2} + \binom{5}{2}$  und beweise mittels vollständiger Induktion die Rekursionsformel

$$
\binom {n + k} {k} = \binom {k - 1} {k - 1} + \binom {k} {k - 1} + \dots + \binom {n + k - 1} {k - 1}.
$$

7. Man bestätige mittels vollständiger Induktion für  $n \in N$ :

a) $\sum_{k=0}^{n} a^{k} b^{n-k} = \frac{a^{n+1} - b^{n+1}}{a - b}$, falls $a \neq b$.

b) $\sum_{k=1}^{n} k^2 = \frac{n(n+1)(2n+1)}{6}$.

8. Hypothekenrechnung.

Ein Darlehen über 100 TDM wird am Ende eines jeden Jahres konstant mit der Rate A getilgt und die Restschuld mit 7% verzinst. Wie groß muß die Annuität A sein, wenn das Darlehen nach genau 20 Jahren zurückbezahlt sein soll?

9. Die 5 Grundaufgaben der Kombinatorik.

Aus einem Alphabet mit n verschiedenen Buchstaben sollen Worte der Länge k gebildet werden. Man zeige: Abhängig davon, ob Buchstaben wiederholt auftreten dürfen und ob man nach der Reihenfolge der Buchstaben unterscheidet, ist die Anzahl der verschiedenen Möglichkeiten wie folgt gegeben:

a) Variationen (nach Reihenfolge wird unterschieden):

$n^{k}$ , mit Wiederholung,

$n(n-1)\cdots(n-k+1)$ , ohne Wiederholung  $(k\leq n)$ ,

$\frac{k!}{k_{1}!\cdots k_{n}!}$ , mit festgelegter Auswahl: der r-te Buchstabe kommt  $k_{r}$ -mal vor,  $0 \leq k_{r} \leq k$ ,  $r = 1, \ldots, n$ ,  $k_{1} + \cdots + k_{n} = k$ .

b) Kombinationen (nach Reihenfolge wird nicht unterschieden):

$\binom{n+k-1}{k}$ , mit Wiederholung,

$\binom{n}{k}$ , ohne Wiederholung  $(k \leq n)$ .

(Hilfe im Fall von Wiederholungen: Man setze im Alphabet zwischen die Buchstaben je ein „|“ und über jeden für das Wort ausgewählten Buchstaben ein „×“. Wie viele verschiedene  $(n-1+k)$ -stellige Muster  $||\times\times\ldots|\times|\times$  gibt es?)

---

§3. Die Ebene

11

10. Beim Rommé spielt man mit 110 Karten; sechs davon sind Joker. Zu Beginn eines Spieles erhält jeder Spieler genau 12 Karten in die Hand; in wieviel Prozent aller möglichen Fälle sind darunter (a) genau zwei bzw. (b) mindestens ein Joker?

11. Zählprobleme der Statistik.

Zur Beantwortung der Frage, ob in mehr als 60% aller Fälle von vier Geschwistern mindestens zwei im gleichen Monat geboren sind, bieten sich zwei Lösungswege an:

a) Man unterscheidet die Individuen und zählt die Variationen, wie sich 12 Geburtsmonate auf 4 Personen verteilen lassen ( $\rightarrow$ Aufg. 9a).
b) Man unterscheidet die Personen nicht und zählt die möglichen 4-elementigen Kombinationen aus dem „Alphabet“ der 12 Monate (→ Aufg. 9b).

Sind die Variationen in a) oder die Kombinationen in b) gleich wahrscheinlich?

12. Die polynomische Formel. Man zeige mit Aufg. 9a für $k, n \in \mathbb{N}$

$$
(a _ {1} + a _ {2} + \dots + a _ {n}) ^ {k} = \sum_ {k _ {1} + \dots + k _ {n} = k} \frac {k !}{k _ {1} ! \cdots k _ {n} !} a _ {1} ^ {k _ {1}} \dots a _ {n} ^ {k _ {n}}.
$$

## §3. Die Ebene

3.1 Kartesische Koordinatensysteme. In einer Ebene E, die wir uns o.E. als Zeichenebene vorstellen, entsteht ein kartesisches Koordinatensystem

(→ Abb. 4, benannt nach RENÉ DESCARTES, 1596 – 1650) durch Vorgabe eines Punktes O und zweier aufeinander senkrecht stehender Zahlengeraden, der x- und der y-Achse, deren Nullpunkt jeweils in O liegt. Dabei muß die y-Achse durch eine positive Drehung (gegen den Uhrzeigersinn) aus der x-Achse hervorgehen.

Fällt man für einen (beliebigen) Punkt $P_{0} \in E$ die Lote auf die Achsen, so bestimmen die beiden Fußpunkte die x- bzw. y-Koordinate $x_{0}$ bzw. $y_{0}$

![](../../raw/pages_0001-0032/images/page_26_chart_15.jpg)

<details>
<summary>scatter</summary>

| Point | x-Achse | y-Achse |
| --- | --- | --- |
| \(P_{0}\) | \(x_{0}\) | \(y_{0}\) |
</details>

Abb. 4 – Ein kartesisches Koordinatensystem

von  $P_{0}$  und man schreibt  $P_{0} = (x_{0}, y_{0})$ . Der Punkt  $O = (0, 0)$  heißt Nullpunkt oder Ursprung des Koordinatensystems.

Nach Festlegung eines kartesischen Koordinatensystems gibt es zu jedem Zahlenpaar  $(x,y)\in\mathbb{R}^{2}$  genau einen Punkt  $X\in E$  mit  $X=(x,y)-$  und umgekehrt. Man kann somit Teilmengen von  $R^{2}$  (etwa Lösungsmengen von Gleichungen oder Ungleichungen) als Punktmengen in E veranschaulichen und umgekehrt geometrische Gebilde (Kurven oder Gebiete in E) durch Funktionen, Gleichungen oder Ungleichungen beschreiben.

---

12

1. Zahlen und Vektoren

Beispiel 1. Der Graph einer Funktion. Sei $I \subseteq \mathbb{R}$ und $f : I \to \mathbb{R}$ eine Funktion. Die Punktmenge

$$
G _ {f} := \{(x, y); x \in I, y = f (x) \} = \{(x, f (x)); x \in I \}
$$

in der mit einem kartesischen Koordinatensystem versehenen Ebene heißt der Graph der Funktion $f$ oder die Kurve $y = f(x)$. Der Graph der Funktion $y = f(x - x_0) + y_0$ entsteht aus $G_f$ durch die Parallelverschiebung der Ebene, die den Punkt $(0,0)$ nach $(x_0, y_0)$ bringt. Dabei bleibt das Koordinatensystem fest. Die folgenden Kapitel bringen zahlreiche konkrete Beispiele.

![](../../raw/pages_0001-0032/images/page_27_chart_5.jpg)

<details>
<summary>line</summary>

| Feature | Description |
| --- | --- |
| Function | y = f(x) |
| X-axis | x |
| Y-axis | y |
| Curve | Wertebereich f(D) |
| Definition | Definitionsbereich D |
</details>

Abb. 5a - Die Kurve $y = f(x)$

![](../../raw/pages_0001-0032/images/page_27_chart_7.jpg)

<details>
<summary>line</summary>

| Point | X | Y |
| --- | --- | --- |
| 1 | 0 | 0 |
| 2 | (x₀, y₀) | ~0.3 |
| 3 | — | ~0.5 |
| 4 | — | ~0.6 |
| 5 | — | ~0.9 |
</details>

Abb. 5b - Die Kurve $y = f(x - x_0) + y_0$

Beispiel 2. Kurven – Lösungsmengen von Gleichungen. Sei $C \subseteq E$ eine Kurve und – nach Wahl eines kartesischen Koordinatensystems – $X = (x, y)$ ein (beliebiger) Punkt auf $C$. Wird die zwischen $x$ und $y$ bestehende Abhängigkeit auf die Form $F(x, y) = 0$ gebracht, d.h.

$$
C = \left\{(x, y); F (x, y) = 0 \right\},
$$

dann nennt man  $F(x,y)=0$  die Gleichung der Kurve C.

a) Die Gerade durch die Punkte  $A = (a_{1}, a_{2})$  und  $B = (b_{1}, b_{2})$  ( $A \neq B$ ) hat die Gleichung

$$
(b _ {2} - a _ {2}) (x - a _ {1}) - (b _ {1} - a _ {1}) (y - a _ {2}) = 0.
$$

b) Der Kreis um  $A = (a_{1}, a_{2})$  mit dem Radius r hat die Gleichung

$$
(x - a _ {1}) ^ {2} + (y - a _ {2}) ^ {2} = r ^ {2}.
$$

c) Es ist

$$
\frac {x ^ {2}}{a ^ {2}} + \frac {y ^ {2}}{b ^ {2}} = 1, \quad \frac {x ^ {2}}{a ^ {2}} - \frac {y ^ {2}}{b ^ {2}} = 1, \quad y ^ {2} - 2 p x = 0
$$

die „Normalgleichung“ einer Ellipse, einer Hyperbel bzw. einer Parabel (a > 0, b > 0, p ≠ 0; → Kap. 6, §7).

□

---

§3. Die Ebene

13

![](../../raw/pages_0001-0032/images/page_28_image_2.jpg)

<details>
<summary>text_image</summary>

y
b
a x
-a y
a x
y
45°
2p x
</details>

Abb. 6 - Ellipse, Hyperbel, Parabel

## Beispiel 3. Gebiete - Lösungsmengen von Ungleichungen.

a) Das Gebiet (die Halbebene) unterhalb (oberhalb) der Geraden  $3x + 2y = 2$  ist die Lösungsmenge der Ungleichung  $3x + 2y < 2$  ( $3x + 2y > 2$ ). Wenn die Gerade zum Gebiet gehört, ist < durch ≤ (bzw. > durch ≥) zu ersetzen.
b) Die Ungleichung  $\frac{x^{2}}{3} + \frac{y^{2}}{5} < 1$  (bzw. > 1) besitzt als Lösungsmenge das Innere (bzw. Äußere) der Ellipse  $\frac{x^{2}}{3} + \frac{y^{2}}{5} = 1$ .
c) Wegen $|x - y| \leq 3 \iff -3 \leq x - y \leq 3$ besteht die Lösungsmenge der Ungleichung $|x - y| \leq 3$ aus dem Durchschnitt der beiden Halbebenen $x - y \leq 3$ (alle Punkte oberhalb und auf der Geraden $x - y = 3$) und $-3 \leq x - y$ (alle Punkte unterhalb und auf der Geraden $y = x + 3$).

□

![](../../raw/pages_0001-0032/images/page_28_image_10.jpg)

<details>
<summary>text_image</summary>

3x+2y=2
y
1
3x+2y>2
-3x+2y<2
x
1
y
y=x+3
y=x-3
1y-x1≤3
x
</details>

Abb. 7 – Lösungsmengen von Ungleichungen.

Regeln: 1. Zur Lösung einer Ungleichung der Form $F(x,y) < 0$ bestimme man zuerst die Kurve $F(x,y) = 0$; die Lösungsmenge liegt ganz auf einer Seite dieser Kurve (vorausgesetzt, $F$ ist stetig, $\rightarrow$ Kap. 7).

2. Die Lösung eines Systems von Ungleichungen  $F_{1}(x,y) < 0$ ,  $F_{2}(x,y) < 0$ , ...,  $F_{n}(x,y) < 0$  ist der Durchschnitt der einzelnen Lösungsmengen; sie wird stückweise berandet von den Kurven  $F_{i}(x,y) = 0 \quad (i = 1, \ldots, n)$  (ebenfalls unter der Voraussetzung, daß die  $F_{i}$  stetig sind).

---

14

1. Zahlen und Vektoren

3.2 Winkel. Der Winkel  $\alpha$  entstehe durch Drehung eines Zeigers um einen Punkt der Ebene. Die Länge des zugehörigen Einheitskreisbogens sei  $\ell$  ( $\rightarrow$  Abb. 8).

![](../../raw/pages_0001-0032/images/page_29_image_3.jpg)

Abb. 8 – Das Bogenmaß eines Winkels

Wir nennen $\ell$, bzw. $-\ell$, das Bogenmaß von $\alpha$ und schreiben $\alpha = \ell$, bzw. $\alpha = -\ell$, wenn die Drehung im positiven Sinn (gegen Uhrzeigersinn), bzw. im Uhrzeigersinn, erfolgt. Ein Winkel von $a^o$ besitzt bei positiver Orientierung das Bogenmaß $x = \frac{\pi}{180} a$ mit der Kreiszahl

$$
\pi = 3. 1 4 1 5 9 2 6 5 3 5 8 9 7 9 3 2 3 8 4 6 2 6 4 3 \dots \approx \frac {2 2}{7}.
$$

$2\pi$ ist der Umfang des Einheitskreises. Der zu $\alpha = \ell$ gehörende Kreisbogen mit dem Radius $r$ hat die Länge $\ell r$ ($\rightarrow$ Kap. 4, §5). Mit jeder vollen Umdrehung wird der Winkel (genauer: das Bogenmaß des Winkels) um $2\pi$ vergrößert oder verkleinert.

3.3 Sinus, Cosinus. Wird in der mit kartesischen  $(x,y)$ -Koordinaten ver-

sehenen Ebene der vom Ursprung zum Punkt (1,0) weisende Zeiger um den Winkel  $\alpha$  gedreht ( $\alpha$  im Bogenmaß,  $\alpha > 0$ : gegen den Uhrzeigersinn bzw.  $\alpha < 0$ : im Uhrzeigersinn), dann bewegt sich die Spitze auf dem Einheitskreis (um O) bis zu einem Punkte P, dessen Koordinaten mit  $\cos \alpha$ ,  $\sin \alpha$  bezeichnet werden:  $P = (\cos \alpha, \sin \alpha)$ .

Die derart für alle $\alpha\in\mathbb{R}$ erklärten Funktionen $\alpha\mapsto\cos\alpha,\quad\alpha\mapsto\sin\alpha$ heißen Cosinus- bzw. Sinusfunktion.

Wir benötigen diese „Kreisfunktionen“ vorerst nur für Dreiecksberechnungen und für die Darstellung von Drehungen der Ebene; die weiterführende Behandlung erfolgt in Kap 2, §3.

![](../../raw/pages_0001-0032/images/page_29_image_12.jpg)

<details>
<summary>text_image</summary>

y
P = (cos α, sin α)
sin α
α
cos α
1
x
</details>

Abb. 9 - $x(\alpha) = \cos \alpha$, $y(\alpha) = \sin \alpha$

---

§3. Die Ebene

15

Hat der sich drehende Zeiger die Länge r, dann liegt nach der Drehung um  $\alpha$  aufgrund der Ähnlichkeit der Dreiecke  $\Delta ORP$  und  $\Delta OSQ$  die Spitze in  $Q = (a, b)$  mit

(1) $a = r\cos \alpha, b = r\sin \alpha.$

Diese Formeln sind Grundlage aller Dreiecksberechnungen, sie bedeuten, etwas anders gelesen, daß im rechtwinkligen Dreieck  $\Delta OSQ$  mit der Hypotenuse r, den Katheten a (Ankathete), b (Gegenkathete) die Beziehungen

![](../../raw/pages_0001-0032/images/page_30_image_5.jpg)

<details>
<summary>text_image</summary>

Q=(a,b)
r
P
sin α
cos α
O
R 1
S
b
a
</details>

Abb. 10 - $a = r\cos \alpha$, $b = r\sin \alpha$

(2) $\frac{a}{r} = \cos \alpha, \quad \frac{b}{r} = \sin \alpha$

gelten (wobei zur Dreiecksberechnung die Winkel positiv gemessen werden). Für den anderen Winkel $\beta = \star OQS$ gilt dementsprechend $\cos \beta = \frac{b}{r}$, $\sin \beta = \frac{a}{r}$.

In einem beliebigen Dreieck  $\Delta ABC$  ( $\rightarrow$  Abb. 11) gelten

der Cosinussatz:

$$
a ^ {2} = b ^ {2} + c ^ {2} - 2 b c \cos \alpha ;
$$

(3) der Sinussatz:

$$
\frac {\sin \alpha}{a} = \frac {\sin \beta}{b} = \frac {\sin \gamma}{c}.
$$

![](../../raw/pages_0001-0032/images/page_30_image_14.jpg)

<details>
<summary>text_image</summary>

C
b
γ
a
h_c
β
A
α
c
B
</details>

Abb. 11 - Cosinus-, Sinussatz

Zum Beweis des Sinussatzes betrachte man eine Höhe, etwa  $h_{c}$ . Hierfür gilt  $b \sin \alpha = h_{c} = a \sin \beta$ , etc. Den Cosinussatz beweisen wir in 5.2.

Anhand der Definition und (2) sind leicht einige Funktionswerte anzugeben:

| x | 0 | $\frac{\pi}{6}$ | $\frac{\pi}{4}$ | $\frac{\pi}{3}$ | $\frac{\pi}{2}$ |
| --- | --- | --- | --- | --- | --- |
| cos x | 1 | $\frac{1}{2}\sqrt{3}$ | $\frac{1}{2}\sqrt{2}$ | $\frac{1}{2}$ | 0 |
| sin x | 0 | $\frac{1}{2}$ | $\frac{1}{2}\sqrt{2}$ | $\frac{1}{2}\sqrt{3}$ | 1 |

![](../../raw/pages_0001-0032/images/page_30_image_19.jpg)

Abb. 12 – Einige Sinus-, Cosinuswerte

---

16

1. Zahlen und Vektoren

## 3.4 Drehungen.

① Drehung des Koordinatensystems. Das kartesische  $(x', y')$ -Koordinatensystem entstehe aus dem  $(x, y)$ -System durch eine Drehung um den Ursprung mit dem Winkel  $\alpha (\rightarrow$  Abb. 13). Hat ein Punkt X im ursprünglichen System die Koordinaten  $(x, y)$  und im gedrehten System die Darstellung  $X = (x', y')$ , so gelten die Transformationsformeln

$$
\begin{array}{l l} x = x ^ {\prime} \cos \alpha - y ^ {\prime} \sin \alpha & x ^ {\prime} = x \cos \alpha + y \sin \alpha \\ y = x ^ {\prime} \sin \alpha + y ^ {\prime} \cos \alpha & y ^ {\prime} = - x \sin \alpha + y \cos \alpha \\ X \text {im ursprünglichen System;} & X \text {im gedrehten System} \end{array} \tag {4}
$$

## Beweis.

$$
O Q = x ^ {\prime}, Q X = y ^ {\prime},
$$

$$
x = O S - R S = x ^ {\prime} \cos \alpha - y ^ {\prime} \sin \alpha ,
$$

$$
y = R T + T X = x ^ {\prime} \sin \alpha + y ^ {\prime} \cos \alpha .
$$

Eine Drehung um $-\alpha$ führt vom $(x', y')$-System zum $(x, y)$-System zurück; deshalb ergibt sich das rechte Formelpaar aus dem linken durch Vertauschung von $x$ mit $x'$, $y$ mit $y'$ und der Substitution $\alpha$ durch $-\alpha$ (und umgekehrt). Man beachte dabei $\cos(-\alpha) = \cos \alpha$, $\sin(-\alpha) = -\sin \alpha$.

![](../../raw/pages_0001-0032/images/page_31_image_10.jpg)

<details>
<summary>text_image</summary>

y
x
T
Q
x'
y'
O
x
R
S
x
</details>

Abb. 13 - Koordinatendrehung

Beispiel. Drehung des Koordinatensystems um  $\alpha = \frac{\pi}{6}$  (Linksdrehung). Der Punkt  $X = (x, y)$  hat im gedrehten System die Darstellung  $X = (x', y')$  mit

$$
x ^ {\prime} = \frac {1}{2} \sqrt {3} x + \frac {1}{2} y, \quad y ^ {\prime} = - \frac {1}{2} x + \frac {1}{2} \sqrt {3} y.
$$

Speziell: $M = (2,3)$ erhält die neuen Koordinaten $M = (\sqrt{3} + \frac{3}{2}, -1 + \frac{3}{2}\sqrt{3})$. Deshalb besitzt der Kreis $(x - 2)^2 + (y - 3)^2 = 25$ im gedrehten Koordinatensystem die Darstellung

$$
(x ^ {\prime} - (\sqrt {3} + \frac {3}{2})) ^ {2} + (y ^ {\prime} - (\frac {3}{2} \sqrt {3} - 1)) ^ {2} = 2 5.
$$

Die „Umkehrformeln“

$$
x = \frac {1}{2} \sqrt {3} x ^ {\prime} - \frac {1}{2} y ^ {\prime}, \quad y = \frac {1}{2} x ^ {\prime} + \frac {1}{2} \sqrt {3} y ^ {\prime}
$$

ergeben für die Parabel  $y = x^{2}$  im neuen System die Darstellung

$$
\frac {3}{4} x ^ {\prime 2} - \frac {1}{2} \sqrt {3} x ^ {\prime} y ^ {\prime} + \frac {1}{4} y ^ {\prime 2} - \frac {1}{2} x ^ {\prime} - \frac {\sqrt {3}}{2} y ^ {\prime} = 0.
$$

□

---

§4. Vektoren

17

⑥ Drehung der Ebene. Wir halten nun das kartesische Koordinatensystem fest und bilden jeden Punkt $X = (x, y)$ durch eine Drehung mit Winkel $\alpha$ um den Ursprung auf $X' = (x', y')$ ab. Dieser Bildpunkt besitzt in dem Koordinatensystem, das sich mit derselben Drehung aus dem $(x, y)$-System ergibt, die Koordinaten $(x, y)$; demnach folgt aus (4) durch Vertauschung von $x$ mit $x'$ und $y$ mit $y'$:

Die Drehung der Ebene um den Winkel  $\alpha$  (bei festem Koordinatensystem)

$$
(x, y) \mapsto (x ^ {\prime}, y ^ {\prime}) \tag {5}
$$

$$
x ^ {\prime} = x \cos \alpha - y \sin \alpha
$$

$$
y ^ {\prime} = x \sin \alpha + y \cos \alpha .
$$

Beispiel. Durch Drehung um $\alpha = \frac{\pi}{6}$ geht der Punkt $M = (2,3)$ über in $M' = (\sqrt{3} - \frac{3}{2}, 1 + \frac{3}{2}\sqrt{3})$, der Kreis $(x - 2)^2 + (y - 3)^2 = 25$ in den Kreis $\left(x - (\sqrt{3} - \frac{3}{2})\right)^2 + \left(y - (1 + \frac{3}{2}\sqrt{3})\right)^2 = 25$ und die Parabel $C: y = x^2$ in die Parabel $C'$ mit der Gleichung $\frac{3}{4}x^2 + \frac{1}{2}\sqrt{3}xy + \frac{1}{4}y^2 + \frac{1}{2}x - \frac{1}{2}\sqrt{3}y = 0$.

![](../../raw/pages_0033-0064/images/page_32_image_8.jpg)

<details>
<summary>text_image</summary>

y
M'
O
C'
M
C
x'
30°
1
x
</details>

Abb. 14 - Drehung einer Parabel

## §4. Vektoren

4.1 Kartesische Koordinatensysteme im Raum bestehen aus drei sich in einem Punkt O (Nullpunkt oder Ursprung) rechtwinklig schneidenden Zahlengeraden gleicher Längeneinheit und jeweils mit dem Nullpunkt im Schnittpunkt O. Man bezeichnet sie als x-, y- und z-Achse, derart, daß diese Achsen ein Rechtssystem bilden; d.h. die Drehung der positiven x-Achse um 90° in die positive y-Achse, zusammen mit einer Verschiebung in Richtung der positiven z-Achse muß eine Rechtsschraubung darstellen (→ Abbn. 15, 29).

Die drei durch je zwei Achsen bestimmten Ebenen heißen Koordinatenebenen, bzw.  $(x,y)$ -Ebene,  $(y,z)$ -Ebene und  $(z,x)$ -Ebene. Die Koordinaten  $x_{0}$ ,  $y_{0}$ ,  $z_{0}$  eines Punktes  $P_{0}$  gewinnt man aus den Schnittpunkten der entsprechenden Achsen mit den zu den Koordinatenebenen parallelen Ebenen durch  $P_{0}$

---

18

1. Zahlen und Vektoren

(→ Abb. 15). Man schreibt $P_{0}=(x_{0},y_{0},z_{0})$. Zu jedem Koordinatentripel gibt es genau einen Punkt des Raumes – und umgekehrt.

![](../../raw/pages_0033-0064/images/page_33_image_3.jpg)

Abb. 15 – Ein kartesisches Koordinatensystem im Raum

4.2 Vektoren. Zu je zwei Punkten P und Q des Raumes gibt es genau eine Parallelverschiebung (des Raumes), die P nach Q bringt (abbildet). Diese Verschiebung wird mit  $\overrightarrow{PQ}$  bezeichnet und heißt „Vektor von P nach Q“. Das Wort „Vektor“ bedeutet so viel wie „Träger“;  $\overrightarrow{PQ}$ , „trägt“ P nach Q. Der Vektor  $\overrightarrow{PQ}$  wird dargestellt durch einen Pfeil, der von P nach Q zeigt (seine Länge ist der Abstand des Punktes P von Q). Wird unter  $\overrightarrow{PQ}$  ein anderer Punkt R nach S verschoben, dann hat offenbar  $\overrightarrow{RS}$  dieselbe Wirkung wie  $\overrightarrow{PQ}$ ; d.h.  $\overrightarrow{PQ} = \overrightarrow{RS}$ . Zwei gleich lange und gleich gerichtete Pfeile im Raum stellen somit denselben Vektor dar. Anstelle „der Pfeil  $\vec{a}$  repräsentiert einen Vektor“ sagt man kurz „ $\vec{a}$  ist ein Vektor“ und berücksichtigt, daß  $\vec{a}$  im Raum frei parallel verschoben werden kann und nicht an einen festen Anfangspunkt gebunden ist.

Den zu  $\vec{a}$  gleich langen, aber entgegengesetzt gerichteten Vektor bezeichnen wir mit  $-\vec{a}$ ; er macht die durch  $\vec{a}$  bewirkte Parallelverschiebung rückgängig. Für  $\vec{a} = \overrightarrow{PQ}$  gilt  $-\vec{a} = \overrightarrow{QP}$ .

![](../../raw/pages_0033-0064/images/page_33_image_7.jpg)

Abb. 16 - Die zu $\vec{a}$, $\vec{b}$ entgegengesetzten Vektoren $-\vec{a}$, $-\vec{b}$.

Zur Vermeidung von Fallunterscheidungen wird der Nullvektor $\vec{0}$ eingeführt. $\vec{0}$ bezeichnet die „Verschiebung“ des Raumes, bei der gar nichts bewegt wird; d.h. $\vec{0} = \overrightarrow{PP}$ für jeden Punkt $P$.

4.3 Die Addition von Vektoren. Führt man zwei Parallelverschiebungen, erst $\vec{a} = \overrightarrow{PQ}$, dann $\vec{b} = \overrightarrow{QR}$, hintereinander aus, so ergibt sich wieder eine Parallelverschiebung, nämlich $\vec{c} = \overrightarrow{PR}$ ($\rightarrow$ Abb. 17a). Wir nennen $\vec{c}$ die Summe von $\vec{a}$ und $\vec{b}$ und schreiben $\vec{c} = \vec{a} + \vec{b}$.

---

§4. Vektoren

19

Haben die Pfeile  $\vec{a}$ ,  $\vec{b}$  gleichen Anfangspunkt, so gewinnt man die Summe  $\vec{a}+\vec{b}$  (geometrisch) nach der Parallelogrammregel ( $\rightarrow$  Abb. 17b).

![](../../raw/pages_0033-0064/images/page_34_image_3.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph TD
  P["P"] --> Q["Q"]
  Q -->|a| P
  Q -->|b| R["R"]
  P --> C["c"]
  C --> R
```
</details>

Abb. 17a - $\overrightarrow{PQ} +\overrightarrow{QR} = \overrightarrow{PR}$

![](../../raw/pages_0033-0064/images/page_34_image_5.jpg)

<details>
<summary>text_image</summary>

a
b
a + b
b
</details>

Abb. 17b - Parallelogrammregel

Offenbar gelten für beliebige Vektoren  $\vec{a}$ ,  $\vec{b}$ ,  $\vec{c}$  die folgenden Rechenregeln:

$$
\begin{array}{c c} \vec {a} + \vec {0} = \vec {a}, & \vec {a} + (- \vec {a}) = \vec {0}, \\ \vec {a} + \vec {b} = \vec {b} + \vec {a} & (\text {Kommutativgesetz}), \\ \vec {a} + (\vec {b} + \vec {c}) = (\vec {a} + \vec {b}) + \vec {c} & (\text {Assoziativgesetz}). \end{array} \tag {1}
$$

Die Summe  $\vec{a}_{1} + \vec{a}_{2} + \cdots + \vec{a}_{n}$  ist derjenige Vektor  $\vec{s} (\rightarrow$  Abb. 18a), der vom Anfangspunkt zum Endpunkt der aus  $\vec{a}_{1}, \vec{a}_{2}, \ldots, \vec{a}_{n}$  gebildeten Vektorkette zeigt. Die Differenz von Vektoren wird erklärt durch

$$
\vec {a} - \vec {b} := \vec {a} + (- \vec {b}).
$$

![](../../raw/pages_0033-0064/images/page_34_image_11.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph LR
  A["A"] -->|"a1"| A
  A -->|"s"| E["E"]
  A -->|"a2"| A
  A -->|"a_n"| E
  E -->|"a_n"| A
```
</details>

Abb. 18a - $\vec{s} = \sum \vec{a}_i$

![](../../raw/pages_0033-0064/images/page_34_image_13.jpg)

<details>
<summary>text_image</summary>

a-b
-b
a
b
a+b
</details>

Abb. 18b - Vektordifferenz

Die Rechenregeln (1) garantieren, daß wir mit „+“ und „-“ so umgehen dürfen, wie wir es vom Rechnen mit Zahlen gewöhnt sind.

4.4 Die skalaren Vielfachen eines Vektors. Zu einer reellen Zahl $\alpha \geq 0$ und einem Vektor $\vec{a}$ bezeichnet $\alpha\vec{a}$ (das $\alpha$-fache von $\vec{a}$) denjenigen Vektor, der dieselbe Richtung hat wie $\vec{a}$, aber die $\alpha$-fache Länge. Im Fall $\alpha < 0$ setzt man $\alpha\vec{a} := -(|\alpha|\vec{a})$. Sonderfälle dieser Festlegung sind $0\vec{a} = \vec{0}$ und $\alpha\vec{0} = \vec{0}$ für jede Zahl $\alpha$ und jeden Vektor $\vec{a}$. Für die auf diese Weise erklärte Multiplikation eines Vektors mit einem Skalar (einer Zahl) gelten offensichtlich die

---

20

1. Zahlen und Vektoren

Rechenregeln $(\alpha, \beta \in \mathbb{R})$ :

$$
\begin{array}{c} \alpha (\beta \vec {a}) = (\alpha \beta) \vec {a}, \\ \alpha (\vec {a} + \vec {b}) = \alpha \vec {a} + \alpha \vec {b}, \\ (\alpha + \beta) \vec {a} = \alpha \vec {a} + \beta \vec {a}. \end{array} \tag {2}
$$

![](../../raw/pages_0033-0064/images/page_35_image_4.jpg)

<details>
<summary>text_image</summary>

1.5 ā
đ̄
0.5 ā
-2 ā
- Ł
-0.75 ā
</details>

Abb. 19 - Skalare Vielfache

4.5 Der Betrag. Die Länge eines Vektors  $\vec{a}$  (das ist für  $\vec{a} = \overrightarrow{PQ}$  die Länge der Strecke  $\overrightarrow{PQ}$ ) nennt man seinen Betrag und schreibt dafür  $|\vec{a}|$  (oft auch  $||\vec{a}||$ ). Der Nullvektor hat keine positive Länge, d.h.  $|\vec{0}| = 0$ . Die Rechenregeln

$$
\begin{array}{c c} \boxed {| \alpha \vec {a} | = | \alpha | | \vec {a} |,} & \text {insbesondere} | - \vec {a} | = | \vec {a} |, \\ | \vec {a} + \vec {b} | \leq | \vec {a} | + | \vec {b} | & (\text {Dreiecksungleichung}) \end{array} \tag {3}
$$

folgen direkt aus den Definitionen. Die Dreiecksungleichung liest man aus der Abb. 17 ab. In (3) bedeutet  $|\alpha|$  den Betrag der reellen Zahl  $\alpha (\rightarrow 2.5)$ .

Ein Vektor vom Betrag 1 heißt Einheitsvektor.

Zu jedem Vektor $\vec{a} \neq \vec{0}$ gehört der Einheitsvektor in Richtung $\vec{a}: \quad \vec{a}_0 := \frac{1}{|\vec{a}|} \vec{a}$.

4.6 Vektoren im Koordinatensystem. Wir legen im Raum ein kartesisches Koordinatensystem mit Ursprung O fest. Dadurch werden gleichzeitig drei ausgezeichnete Vektoren gegeben, nämlich die Einheitsvektoren  $\vec{e}_{1}$ ,  $\vec{e}_{2}$ ,  $\vec{e}_{3}$  (oft auch i, j, k oder  $\vec{e}_{x}$ ,  $\vec{e}_{y}$ ,  $\vec{e}_{z}$  bezeichnet) in Richtung der positiven x-, y-, bzw. z-Achse ( $\rightarrow$  Abb. 20). Wir nennen ( $\vec{e}_{1}, \vec{e}_{2}, \vec{e}_{3}$ ) eine kartesische Basis und bezeichnen das Koordinatensystem mit

$$
(O; \vec {e} _ {1}, \vec {e} _ {2}, \vec {e} _ {3}).
$$

Der Vektor $\vec{a} = \overrightarrow{OA}$ heißt Ortsvektor des Punktes $A = (a_{1}, a_{2}, a_{3})$; er ist, wie die Abb. 20 zeigt, eindeutig zerlegbar als Summe $\vec{a} = a_{1}\vec{e}_{1} + a_{2}\vec{e}_{2} + a_{3}\vec{e}_{3}$. Abkürzend schreibt man (bei festgelegtem Koordinatensystem)

$$
\vec {a} = \left( \begin{array}{c} a _ {1} \\ a _ {2} \\ a _ {3} \end{array} \right): \Longleftrightarrow \vec {a} = a _ {1} \vec {e} _ {1} + a _ {2} \vec {e} _ {2} + a _ {3} \vec {e} _ {3} = \overrightarrow {O A} \quad \text {mit} \quad A = (a _ {1}, a _ {2}, a _ {3}). \tag {4}
$$

---

§4. Vektoren

21

Man nennt $a_{i}\vec{e}_{i}$ die Komponente von $\vec{a}$ in $\vec{e}_{i}$-Richtung ($i = 1,2,3$) und die Zahlen $a_{i} \in \mathbb{R}$ die Koordinaten des Vektors $\vec{a}$ (bezüglich $(O; \vec{e}_{1}, \vec{e}_{2}, \vec{e}_{3})$).

![](../../raw/pages_0033-0064/images/page_36_image_3.jpg)

<details>
<summary>text_image</summary>

Z
A=(a₁,a₂,a₃)
a₁e₁
a₂e₂
a₃e₃
X
Y
</details>

Abb. 20 - $\vec{a} = a_{1}\vec{e}_{1} + a_{2}\vec{e}_{2} + a_{3}\vec{e}_{3}$

Für einen Vektor  $\vec{a}$  in allgemeiner Lage, etwa  $\vec{a} = \overrightarrow{PQ}$  mit  $P = (p_{1}, p_{1}, p_{3})$  und  $Q = (q_{1}, q_{2}, q_{3})$  gilt

$$
\begin{array}{l} \overrightarrow {P Q} = \overrightarrow {O Q} - \overrightarrow {O P} = q _ {1} \vec {e} _ {1} + q _ {2} \vec {e} _ {2} + q _ {3} \vec {e} _ {3} - p _ {1} \vec {e} _ {1} - p _ {2} \vec {e} _ {2} - p _ {3} \vec {e} _ {3} \\ = (q _ {1} - p _ {1}) \vec {e} _ {1} + (q _ {2} - p _ {2}) \vec {e} _ {2} - (q _ {3} - p _ {3}) \vec {e} _ {3}. \\ \end{array}
$$

Das ergibt die Koordinatendarstellung

$$
\boxed {\vec {a} = \overrightarrow {P Q} = \left( \begin{array}{l} q _ {1} - p _ {1} \\ q _ {2} - p _ {2} \\ q _ {3} - p _ {3} \end{array} \right), \text {falls} P = (p _ {1}, p _ {2}, p _ {3}), Q = (q _ {1}, q _ {2}, q _ {3}).} \tag {5}
$$

Die Summe von Vektoren und die skalaren Vielfachen lassen sich aus der Koordinatendarstellung (4) bzw. (5) sehr einfach berechnen:

$$
\vec {a} = \sum_ {i = 1} ^ {3} a _ {i} \vec {e} _ {i}, \vec {b} = \sum_ {i = 1} ^ {3} b _ {i} \vec {e} _ {i} \implies \vec {a} + \vec {b} = \sum_ {i = 1} ^ {3} (a _ {i} + b _ {i}) \vec {e} _ {i}, \alpha \vec {a} = \sum_ {i = 1} ^ {3} (\alpha a _ {i}) \vec {e} _ {i}, \alpha \in \mathbb {R}.
$$

Folglich gilt

$$
\boxed { \begin{array}{l} \left( \begin{array}{c} a _ {1} \\ a _ {2} \\ a _ {3} \end{array} \right) + \left( \begin{array}{c} b _ {1} \\ b _ {2} \\ b _ {3} \end{array} \right) = \left( \begin{array}{c} a _ {1} + b _ {1} \\ a _ {2} + b _ {2} \\ a _ {3} + b _ {3} \end{array} \right), \alpha \left( \begin{array}{c} a _ {1} \\ a _ {2} \\ a _ {3} \end{array} \right) = \left( \begin{array}{c} \alpha a _ {1} \\ \alpha a _ {2} \\ \alpha a _ {3} \end{array} \right). \end{array} } \tag {6}
$$

Mit dem Satz von Pythagoras liest man direkt aus Abb. 20 ab:

$$
\boxed {| \vec {a} | = \sqrt {a _ {1} ^ {2} + a _ {2} ^ {2} + a _ {3} ^ {2}}, \text {falls} \vec {a} = a _ {1} \vec {e} _ {1} + a _ {2} \vec {e} _ {2} + a _ {3} \vec {e} _ {3}.} \tag {7}
$$

Beispiel. Für $\vec{a} = \begin{pmatrix} 2 \\ 0 \\ -3 \end{pmatrix}$, $\vec{b} = \begin{pmatrix} 0.5 \\ -1 \\ 6 \end{pmatrix}$ ist $\vec{a} + \vec{b} = \begin{pmatrix} 2.5 \\ -1 \\ 3 \end{pmatrix}$, $5\vec{a} = \begin{pmatrix} 10 \\ 0 \\ -15 \end{pmatrix}$,

---

22

1. Zahlen und Vektoren

$$
2 \vec {a} - 3 \vec {b} = \left( \begin{array}{c} 2. 5 \\ 3 \\ - 2 4 \end{array} \right) \text {und} | \vec {a} | = \sqrt {1 3}, | \vec {b} | = \sqrt {3 7 . 2 5}, | \vec {a} + \vec {b} | = \sqrt {1 6 . 2 5}.
$$

Hinweis: Den Koordinatenwechsel, also den Übergang von einem kartesischen Koordinatensystem zu einem anderen, behandeln wir in Kap. 6, 6.6.

## §5. Produkte

5.1 Der Winkel zwischen zwei Vektoren. Trägt man zwei von 0 verschiedene Vektoren $\vec{a}$, $\vec{b}$ von einem Punkt $P$ aus ab, so bezeichnet man den kleineren der beiden positiv gemessenen Winkel, den die Pfeile $\vec{a}$ und $\vec{b}$ im Scheitel $P$ bilden, als Winkel zwischen $\vec{a}$ und $\vec{b}$, i.Z. $\star(\vec{a},\vec{b})$, mit $0 \leq \star(\vec{a},\vec{b}) \leq \pi$:

![](../../raw/pages_0033-0064/images/page_37_image_6.jpg)

<details>
<summary>text_image</summary>

Mathematical diagram showing vector transformations with labeled arrows and a point in a circle, likely from algebraic or geometric context.
</details>

Abb. 21 - ✝(a,b)

Aus Abb. 21 liest man direkt als Rechenregeln ab:

a)  $\nmid(\vec{a},\vec{b})=\nmid(\vec{b},\vec{a})$ ,
b)  $\nmid(\vec{a},t\vec{a})=0,\text{ falls }t>0,$
c)  $\not\prec(\vec{a},t\vec{a})=\pi,$  falls t<0,
d) $\nmid (-\vec{a},\vec{b}) = \pi -\nmid (\vec{a},\vec{b}).$

Man nennt $\vec{a}$ orthogonal (senkrecht) zu $\vec{b}$, i.Z. $\vec{a} \perp \vec{b}$, wenn $\not\asymp (\vec{a}, \vec{b}) = \frac{\pi}{2}$. Obwohl zwischen dem Nullvektor $\vec{0}$ und $\vec{a}$ kein Winkel erklärt wird, sagt man dennoch – zur Vermeidung von Fallunterscheidungen ($\rightarrow$ 5.2 (3)) – $\vec{0}$ ist orthogonal zu jedem beliebigen Vektor; d.h. $\vec{0} \perp \vec{a}$ für alle $\vec{a}$.

![](../../raw/pages_0033-0064/images/page_37_image_15.jpg)

<details>
<summary>text_image</summary>

a
b
(a, b)=0
a
b
(a, b)=π
a
b
(a, b)=π/2
a
y
π-y
-b
</details>

Abb. 22 - Verschiedene Winkel

---

§5. Produkte

23

## 5.2 Das Skalarprodukt  $\vec{a} \cdot \vec{b}$  der Vektoren  $\vec{a}$  und  $\vec{b}$  ist definiert durch

$$
\vec {a} \cdot \vec {b} := \left\{ \begin{array}{c l} | \vec {a} | | \vec {b} | \cos \nmid (\vec {a}, \vec {b}) & , \text {falls} \vec {a} \neq 0 \text {und} \vec {b} \neq 0 \\ 0 & , \text {falls} \vec {a} = \vec {0} \text {oder} \vec {b} = \vec {0} \end{array} \right.
$$

Das Skalarprodukt  $\vec{a}\cdot\vec{b}$ , auch inneres Produkt genannt, ist eine Zahl (= Skalar). Andere gebräuchliche Schreibweisen für  $\vec{a}\cdot\vec{b}$  sind  $\vec{a}\vec{b}$ ,  $<\vec{a},\vec{b}>$  oder  $s(\vec{a},\vec{b})$ .

Beispiele. Die Vektoren $\vec{e}_{i}$ einer kartesischen Basis ($\rightarrow$ 4.6) sind stets Einheitsvektoren und paarweise orthogonal, d.h.

$$
\vec {e} _ {1} \cdot \vec {e} _ {1} = \vec {e} _ {2} \cdot \vec {e} _ {2} = \vec {e} _ {3} \cdot \vec {e} _ {3} = 1, \tag {1}
$$

$$
\vec {e} _ {1} \cdot \vec {e} _ {2} = \vec {e} _ {2} \cdot \vec {e} _ {3} = \vec {e} _ {3} \cdot \vec {e} _ {1} = 0.
$$

Wegen $|\vec{e}_i| = 1$ gilt für einen beliebigen
Vektor $\vec{a} = a_1\vec{e}_1 + a_2\vec{e}_2 + a_3\vec{e}_3$ stets

$$
\begin{array}{l} \vec {a} \cdot \vec {e} _ {i} = | \vec {a} | \cos \nmid (\vec {a}, \vec {e} _ {i}) \tag {2} \\ = a _ {i} \quad (i = 1, 2, 3) . \\ \end{array}
$$

(2)

Dies liest man mit $\varphi_{i}=\star(\vec{a},\vec{e}_{i})$ direkt aus Abb. 23 ab. Damit erhält man

![](../../raw/pages_0033-0064/images/page_38_image_12.jpg)

<details>
<summary>text_image</summary>

|a|cos φ₃
φ₃
φ₂
φ₁
e₃
a
e₂
e₁
|a|cos φ₂
|a|cos φ₁
</details>

Abb. 23 - Richtungscosinus

$$
\vec {a} = (\vec {a} \cdot \vec {e} _ {1}) \vec {e} _ {1} + (\vec {a} \cdot \vec {e} _ {2}) \vec {e} _ {2} + (\vec {a} \cdot \vec {e} _ {3}) \vec {e} _ {3}.
$$

Die Faktoren $\cos \angle (\vec{a},\vec{e}_i)$ nennt man Richtungscosinus von $\vec{a}$, sie sind nach (2) genau die Kooordinaten des Einheitsvektors in Richtung $\vec{a}$, insbesondere gilt

$$
\cos^ {2} \nmid (\vec {a}, \vec {e} _ {1}) + \cos^ {2} \nmid (\vec {a}, \vec {e} _ {2}) + \cos^ {2} \nmid (\vec {a}, \vec {e} _ {3}) = 1.
$$

Rechenregeln für das Skalarprodukt:

a) $\vec{a} \cdot \vec{b} = \vec{b} \cdot \vec{a}$ (Kommutativgesetz),

b) $(\alpha \vec{a})\cdot \vec{b} = \vec{a}\cdot (\alpha \vec{b}) = \alpha (\vec{a}\cdot \vec{b})$ (für $\alpha \in \mathbb{R}$),

(3) c) $(\vec{a} +\vec{b})\cdot \vec{c} = \vec{a}\cdot \vec{c} +\vec{b}\cdot \vec{c}$ (Distributivgesetz),

d) $\vec{a} \cdot \vec{b} = 0 \iff \vec{a}$ orthogonal zu $\vec{b}$ (Orthogonalitätstest),

e) $|\vec{a}| = \sqrt{\vec{a} \cdot \vec{a}}$.

Beweis. a), b), d) und e) ergeben sich direkt aus der Definition. c) ist für $\vec{c} = \vec{0}$ trivial erfüllt. Im Falle $\vec{c} \neq \vec{0}$ legen wir o. E. die positive $x$-Achse in Richtung $\vec{c}$, dann ist $\vec{c} = \alpha \vec{e}_1$ mit $\alpha > 0$ und mit (2), (3b) und §4 (6) ergibt sich direkt

$$
\vec {a} \cdot \vec {c} = \alpha a _ {1}, \quad \vec {b} \cdot \vec {c} = \alpha b _ {1}, \quad (\vec {a} + \vec {b}) \cdot \vec {c} = \alpha (a _ {1} + b _ {1}).
$$

---

24

1. Zahlen und Vektoren

Wegen (3b) und (3c) darf man Skalarprodukte wie gewohnt ausmultiplizieren (man sagt, das Skalarprodukt ist linear in beiden Faktoren):

$$
\begin{array}{l} (a _ {1} \vec {u} _ {1} + a _ {2} \vec {u} _ {2} + \dots + a _ {n} \vec {u} _ {n}) \cdot (b _ {1} \vec {v} _ {1} + b _ {2} \vec {v} _ {2} + \dots + b _ {m} \vec {v} _ {m}) = \tag {4} \\ = a _ {1} b _ {1} (\vec {u} _ {1} \cdot \vec {v} _ {1}) + \dots + a _ {n} b _ {m} (\vec {u} _ {n} \cdot \vec {v} _ {m}). \\ \end{array}
$$

Beachte. Im allg. ist  $(\vec{a} \cdot \vec{b})\vec{c}$  verschieden von  $\vec{a}(\vec{b} \cdot \vec{c}) = (\vec{b} \cdot \vec{c})\vec{a}$ . Der eine Vektor ist parallel zu  $\vec{c}$ , der andere parallel zu  $\vec{a}$ .

Anwendung. Beweis des Cosinussatzes ( $\rightarrow$  §3 (3),  $\rightarrow$  Abb. 11). Im Dreieck  $\Delta ABC$  gilt  $\overrightarrow{BC} = \overrightarrow{AC} - \overrightarrow{AB}$  und  $\alpha = \not\preceq (\overrightarrow{AB}, \overrightarrow{AC})$ . Mit (3c) und (3e) folgt

$$
\begin{array}{l} a ^ {2} = | \overrightarrow {B C} | ^ {2} = | \overrightarrow {A C} - \overrightarrow {A B} | ^ {2} = (\overrightarrow {A C} - \overrightarrow {A B}) \cdot (\overrightarrow {A C} - \overrightarrow {A B}) \\ = | \overrightarrow {A C} | ^ {2} + | \overrightarrow {A B} | ^ {2} - 2 \overrightarrow {A B} \cdot \overrightarrow {A C} = b ^ {2} + c ^ {2} - 2 b c \cos \alpha . \\ \end{array}
$$

Die Koordinatendarstellung $\vec{a} = \sum a_i\vec{e}_i = \begin{pmatrix} a_1 \\ a_2 \\ a_3 \end{pmatrix}, \quad \vec{b} = \sum b_i\vec{e}_i = \begin{pmatrix} b_1 \\ b_2 \\ b_3 \end{pmatrix}$ der Vektoren $\vec{a}$, $\vec{b}$ bezüglich einer kartesischen Basis ($\vec{e}_1, \vec{e}_2, \vec{e}_3$) ermöglicht mit (1) und (4) einfache Berechnungen von $\vec{a} \cdot \vec{b}$ und $\cos \star (\vec{a}, \vec{b})$:

a) $\vec{a} \cdot \vec{b} = a_{1}b_{1} + a_{2}b_{2} + a_{3}b_{3},$ $|\vec{a}| = \sqrt{a_1^2 + a_2^2 + a_3^2}$,

b) $\cos \angle (\vec{a},\vec{b}) = \frac{\vec{a}\cdot\vec{b}}{|\vec{a}||\vec{b}|} = \frac{a_1b_1 + a_2b_2 + a_3b_3}{\sqrt{a_1^2 + a_2^2 + a_3^2}\sqrt{b_1^2 + b_2^2 + b_3^2}},$ falls $\vec{a},\vec{b}\neq \vec{0}$

(5) insbesondere die Richtungscosinus

c) $\cos \star (\vec{a},\vec{e}_i) = \frac{a_i}{\sqrt{a_1^2 + a_2^2 + a_3^2}}$ $(i = 1,2,3)$

für die Basisvektoren $\vec{e}_1 = \begin{pmatrix} 1 \\ 0 \\ 0 \end{pmatrix}$, $\vec{e}_2 = \begin{pmatrix} 0 \\ 1 \\ 0 \end{pmatrix}$, $\vec{e}_3 = \begin{pmatrix} 0 \\ 0 \\ 1 \end{pmatrix}$.

Beispiele. 1. In kartesischen Koordinaten berechnen wir mit (5) für

$$
\vec {a} = \left( \begin{array}{c} 2 \\ - 4 \\ 0 \end{array} \right), \vec {b} = \left( \begin{array}{c} 6 \\ 3 \\ 4 \end{array} \right), \vec {c} = \left( \begin{array}{c} 1 \\ 0 \\ - 1 \end{array} \right):
$$

$\vec{a} \cdot \vec{b} = 2 \cdot 6 - 4 \cdot 3 + 0 \cdot 4 = 0$ ; also sind $\vec{a}$ und $\vec{b}$ orthogonal.

$\vec{a} \cdot \vec{c} = 2 \cdot 1 + (-4) \cdot 0 + 0 \cdot (-1) = 2$ und $|\vec{a}| = \sqrt{20}$, $|\vec{c}| = \sqrt{2}$. Damit ergibt sich $\cos \nmid (\vec{a}, \vec{c}) = \frac{2}{\sqrt{20} \sqrt{2}} = \frac{1}{\sqrt{10}}$; d.h. im Bogenmaß $\nmid (\vec{a}, \vec{c}) = 1.2490458\ldots$.

$\cos \nmid (\vec{b},\vec{e}_1) = \frac{6}{\sqrt{61}},\quad \cos \nmid (\vec{b},\vec{e}_2) = \frac{3}{\sqrt{61}},\quad \cos \nmid (\vec{b},\vec{e}_3) = \frac{4}{\sqrt{61}};\mathrm{d.h.}\mathrm{im}\mathrm{Bo}-$ genmaB $\nmid (\vec{b},\vec{e}_1) = 0.694738\dots ,\nmid (\vec{b},\vec{e}_2) = 1.17655\dots ,\nmid (\vec{b},\vec{e}_3) = 1.03311\dots .$

---

§5. Produkte

25

2. Sehnen- und Tangentenwinkel am Kreis. Die Gleichung  $x^{2} + y^{2} - 1 = 2ay$  bestimmt für jedes  $a \in R$  einen Kreis durch die Punkte  $A = (-1,0)$  und  $B = (1,0)$  mit Mittelpunkt  $M = (0,a)$ . Ist  $C = (x,y)$  ein weiterer Punkt auf dem Kreis, so ergibt sich mit (5b) für den Winkel  $\gamma$  im  $\Delta ABC$  ( $\rightarrow$  Abb. 24a)

$$
\cos \gamma = \frac {(x - 1) (x + 1) + y ^ {2}}{\sqrt {(x + 1) ^ {2} + y ^ {2}} \cdot \sqrt {(x - 1) ^ {2} + y ^ {2}}} = \frac {x ^ {2} + y ^ {2} - 1}{\sqrt {(x ^ {2} + y ^ {2} - 1) ^ {2} + 4 y ^ {2}}}.
$$

Mit  $x^{2} + y^{2} - 1 = 2ay$  erhält man die konstanten Werte

$$
\cos \gamma = \frac {a}{\sqrt {1 + a ^ {2}}}, \text {falls} y > 0 \quad \text {und} \quad \cos \gamma = \frac {- a}{\sqrt {1 + a ^ {2}}}, \text {falls} y <   0.
$$

Daraus liest man zweierlei ab:

— Auf jedem Kreisbogen über AB ist der Peripheriewinkel γ konstant.
— Gegenüberliegende Winkel in einem Kreissehnenviereck ergänzen sich zu π.

Der Vektor $\vec{t} = \frac{1}{|\overrightarrow{AB}|^2}\overrightarrow{AB} +\frac{1}{|\overrightarrow{BC}|^2}\overrightarrow{BC} = \frac{y}{(x - 1)^2 + y^2}\left( \begin{array}{c}a\\ 1 \end{array} \right)$ hat stets die

Richtung der Kreistangente in $B$, da $\overrightarrow{MB} \cdot \vec{t} = 0$. Der Winkel zwischen der Tangente in $B$ und der Sehne $\overline{AB}$ ist damit ebenfalls $\gamma$.

![](../../raw/pages_0033-0064/images/page_40_image_12.jpg)

<details>
<summary>text_image</summary>

y
C
γ
M
-1
a
A
π-γ
B
x
t
γ
</details>

Abb. 24a - Sehnen-, Tangentenwinkel

![](../../raw/pages_0033-0064/images/page_40_image_14.jpg)

<details>
<summary>text_image</summary>

e₃
ψ
x
φ
e₁
e₂
</details>

Abb. 24b - Kugelkoordinaten

3. Die Kugelkoordinaten $(r, \psi, \varphi)$ eines Vektor $\vec{x}$ sind bezüglich einer kartesischen Basis $(\vec{e}_1, \vec{e}_2, \vec{e}_3)$ wie folgt definiert $(\rightarrow \text{Abb. 24b})$: $r := |\vec{x}|$, $\psi := \nmid (\vec{x}, \vec{e}_3)$, $\varphi := \text{Winkel der Drehung von } \vec{e}_1$ in Richtung $x_1\vec{e}_1 + x_2\vec{e}_2$, $(0 \leq \varphi < 2\pi)$.

Wegen (5c) ist $r \cos \psi = x_3$ und $r \sin \psi = r \sqrt{1 - \cos^2 \psi} = |x_1 \vec{e}_1 + x_2 \vec{e}_2|$, d.h.

$$
x _ {1} = r \sin \psi \cos \varphi , x _ {2} = r \sin \psi \sin \varphi , x _ {3} = r \cos \psi.
$$

Anwendung: Orthogonale Zerlegung. Vom Ort unabhängige Kräfte werden in der Physik als Vektoren dargestellt. Bewegt sich ein Massenpunkt unter der Kraft  $\vec{K}$  vom Punkt P zum Punkt Q, so ist

$$
A = \vec {K} \cdot \vec {s} = | \vec {K} |   | \vec {s} |   \cos \nmid (\vec {K}, \vec {s}) \quad \text {mit} \quad \vec {s} := \overrightarrow {P Q}
$$

die dabei geleistete Arbeit. Stellt man K als Summe einer Kraftkomponente  $\vec{K}_{\hat{s}}$  in Richtung  $\vec{s}$  und einer dazu senkrechten Komponente  $\vec{K}_{\hat{s}}^{\perp}$  dar, so ist A alleine durch  $\vec{K}_{\hat{s}}$  bestimmt. Man definiert daher allgemein:

---

26

1. Zahlen und Vektoren

Orthogonale Zerlegung von  $\vec{a}$  längs  $\vec{b}$ , falls  $\vec{b} \neq \vec{0}$ .

$$
\vec {a} = \vec {a} _ {\vec {b}} + \vec {a} _ {\vec {b}} ^ {\perp} \quad \text {mit den Komponenten}
$$

(6)

$$
\begin{array}{l} \vec {a} _ {\vec {b}} := \frac {\vec {a} \cdot \vec {b}}{| \vec {b} | ^ {2}} \vec {b} \quad \text {in Richtung} \vec {b} \text {und} \\ \vec {a} _ {\vec {b}} ^ {\perp} := \vec {a} - \frac {\vec {a} \cdot \vec {b}}{| \vec {b} | ^ {2}} \vec {b} \quad \text {orthogonal zu} \vec {b} \quad (\rightarrow (1 2)). \\ \end{array}
$$

![](../../raw/pages_0033-0064/images/page_41_image_6.jpg)

<details>
<summary>text_image</summary>

a
a\u2081b
a\u2081b
b
</details>

![](../../raw/pages_0033-0064/images/page_41_image_7.jpg)

<details>
<summary>text_image</summary>

a
a⊥
b
a
b
</details>

Abb. 25 - Orthogonale Zerlegung

Beweis. Offenbar weist $\vec{a}_{\vec{b}}$ in Richtung $\vec{b}$ und es gilt $\vec{a} = \vec{a}_{\vec{b}} + \vec{a}_{\vec{b}}^{\perp}$. Der Orthogonalitätstest (3d) zeigt $\vec{a}_{\vec{b}}^{\perp} \perp \vec{b}$; denn $\vec{a}_{\vec{b}}^{\perp} \cdot \vec{b} = \vec{a} \cdot \vec{b} - \frac{\vec{a} \cdot \vec{b}}{|\vec{b}|^{2}} (\vec{b} \cdot \vec{b}) = 0$.

## Beispiele.

1. In jeder kartesischen Basis  $(\vec{e}_{1},\vec{e}_{2},\vec{e}_{3})$  gilt für  $\vec{a}=a_{1}\vec{e}_{1}+a_{2}\vec{e}_{2}+a_{3}\vec{e}_{3}$  einfach  $\vec{a}_{\vec{e}_{1}}=a_{1}\vec{e}_{1}$  und  $\vec{a}_{\vec{e}_{1}}^{\perp}=a_{2}\vec{e}_{2}+a_{3}\vec{e}_{3}$ . Analog für  $\vec{e}_{2}$  und  $\vec{e}_{3}$ .
2. $\vec{a} = \begin{pmatrix} 2 \\ 3 \\ 1 \end{pmatrix}, \vec{b} = \begin{pmatrix} -1 \\ 0 \\ 1 \end{pmatrix} \implies \vec{a}_{\vec{b}} = \frac{-1}{2}\vec{b} = \begin{pmatrix} 0.5 \\ 0 \\ -0.5 \end{pmatrix}, \vec{a}_{\vec{b}}^{\perp} = \vec{a} -\vec{a}_{\vec{b}} = \begin{pmatrix} 1.5 \\ 3 \\ 1.5 \end{pmatrix}.$
3. Keilnut-Reibung. Durch Ausformung einer keilförmigen Nut läßt sich

die Haftreibung zwischen zwei Maschinenteilen erhöhen: Die Belastung $\vec{K}$ ruft senkrecht zu den Berührflächen die Gegenkräfte $\vec{k}$ und $\vec{h}$ hervor. Für die orthogonalen Zerlegungen von $\vec{k}$ und $\vec{h}$ längs $\vec{K}$ gelten die Gleichgewichtsbedingungen:

in Richtung  $\vec{K}:\vec{k}_{\vec{K}}+\vec{h}_{\vec{K}}+\vec{K}=\vec{0}$ ,
orthogonal zu  $\vec{K}:\vec{k}_{\vec{K}}^{\perp}+\vec{h}_{\vec{K}}^{\perp}=\vec{0}$ .

![](../../raw/pages_0033-0064/images/page_41_image_17.jpg)

<details>
<summary>text_image</summary>

K
k
α
β
h
</details>

Abb. 26 - Keilnut

Mit den Winkeln  $\alpha$ ,  $\beta$  aus Abb. 26 heißt dies

$$
| \vec {k} | \sin \alpha + | \vec {h} | \sin \beta = | \vec {K} | \quad \text {bzw.} \quad | \vec {k} | \cos \alpha - | \vec {h} | \cos \beta = 0.
$$

Löst man dies nach $|\vec{k}|$ und $|\vec{h}|$ auf, so ergibt sich sich mit dem Reibungskoeffizienten $\mu$ für die Keilnut-Reibungszahl $\mu'$

---

§5. Produkte

27

$$
\mu^ {\prime} := \mu \frac {| \vec {k} | + | \vec {h} |}{| \vec {K} |} = \mu \frac {\cos \alpha + \cos \beta}{\sin (\alpha + \beta)}
$$

(→ Kap. 2, 3(5)). Für $\alpha = \beta$ erhält man $\mu' = \frac{\mu}{\sin \alpha} > \mu$, falls $\alpha \neq 0$.

□

5.3 Das Vektorprodukt  $\vec{a} \times \vec{b}$  zweier Vektoren  $\vec{a}$  und  $\vec{b}$  ist der Vektor mit folgenden Eigenschaften:

a)  $\vec{a} \times \vec{b} = \vec{0}$ , falls  $\vec{a} = \vec{0}$  oder  $\vec{b} = \vec{0}$  oder  $\vec{a}$  parallel zu  $\vec{b}$ .
b) In allen anderen Fällen ist  $\vec{a} \times \vec{b}$  derjenige Vektor,

① der senkrecht auf  $\vec{a}$  und  $\vec{b}$  steht,
② mit dem  $(\vec{a},\vec{b},\vec{a}\times\vec{b})$  ein Rechtssystem darstellt ( $\rightarrow$  Abb. 28, Rechte-Hand-Regel) und
③ dessen Betrag gleich dem Flächeninhalt F des von  $\vec{a}$ ,  $\vec{b}$  aufgespannten Parallelogramms ist ( $\rightarrow$  Abb. 27).

![](../../raw/pages_0033-0064/images/page_42_image_13.jpg)

<details>
<summary>text_image</summary>

F = |a||b| sin φ
a⃗
b⃗
a⃗×b⃗
</details>

Abb. 27 - Vektorprodukt

![](../../raw/pages_0033-0064/images/page_42_image_15.jpg)

<details>
<summary>text_image</summary>

a
b
a×b
</details>

Abb. 28 - Rechte-Hand-Regel

Zur Festlegung der Richtung von  $\vec{a} \times \vec{b}$  hat man zwei Hilfsmittel:

Die Rechte-Hand-Regel: Die ausgestreckte rechte Hand mit Zeigefinger in $\vec{a}$-Richtung wird über den kleineren Winkel in Richtung $\vec{b}$ geschlossen; der abgespreizte Daumen zeigt in Richtung $\vec{a} \times \vec{b}$. M.a.W.: Weist von der rechten Hand der gestreckte Zeigefinger in Richtung $\vec{a}$ und der abgewinkelte Mittelfinger in Richtung $\vec{b}$, so zeigt der zum Zeigefinger rechtwinklig abgespreizte Daumen in Richtung $\vec{a} \times \vec{b}$ ($\rightarrow$ Abb. 28).

Die Schraubregel: Eine aus der  $\vec{a}$ -Richtung über den kleineren Winkel in  $\vec{b}$ -Richtung gedrehte Rechtsschraube mit Drehachse senkrecht zu  $\vec{a}$ ,  $\vec{b}$  verschiebt sich in Richtung  $\vec{a} \times \vec{b}$  ( $\rightarrow$  Abb. 29a).

Für den Betrag des Vektors $\vec{a} \times \vec{b}$ gilt laut Definition

$$
| \vec {a} \times \vec {b} | = | \vec {a} |   | \vec {b} |   \sin \nless (\vec {a}, \vec {b}). \tag {7}
$$

---

28

1. Zahlen und Vektoren

Beispiele. Für die Vektoren  $\vec{e}_{1}$ ,  $\vec{e}_{2}$ ,  $\vec{e}_{3}$  einer kartesischen Basis gilt stets

$$
\vec {e} _ {1} \times \vec {e} _ {1} = \vec {0}, \quad \vec {e} _ {1} \times \vec {e} _ {2} = \vec {e} _ {3}, \quad \vec {e} _ {1} \times \vec {e} _ {3} = - \vec {e} _ {2},
$$

$$
\vec {e} _ {2} \times \vec {e} _ {1} = - \vec {e} _ {3}, \quad \vec {e} _ {2} \times \vec {e} _ {2} = \vec {0}, \quad \vec {e} _ {2} \times \vec {e} _ {3} = \vec {e} _ {1}, \tag {8a}
$$

$$
\vec {e} _ {3} \times \vec {e} _ {1} = \vec {e} _ {2}, \quad \vec {e} _ {3} \times \vec {e} _ {2} = - \vec {e} _ {1}, \quad \vec {e} _ {3} \times \vec {e} _ {3} = \vec {0},
$$

$$
\vec {e} _ {3} \times \vec {b} = - b _ {2} \vec {e} _ {1} + b _ {1} \vec {e} _ {2}, \quad \text {falls} \vec {b} = b _ {1} \vec {e} _ {1} + b _ {2} \vec {e} _ {2} + b _ {3} \vec {e} _ {3}. \tag {8b}
$$

Beweis. (8a) folgt direkt aus der Definition und der Rechte-Hand-Regel. Für (8b) betrachte man die zu $\vec{e}_3$ senkrechte Komponente von $\vec{b}$, d.i. $b_1\vec{e}_1 + b_2\vec{e}_2$ ($\rightarrow$ Abb. 29b), sie besitzt die Länge $|\vec{b}|\sin \times (\vec{e}_3,\vec{b})$ und geht durch eine Drehung um $\alpha = +\frac{\pi}{2}$ in der $(x_1,x_2)$-Ebene in den Vektor $-b_2\vec{e}_1 + b_1\vec{e}_2$ über ($\rightarrow$ 3.4 (5)). Dieser Vektor erfüllt wegen (7) die Forderungen ①, ②, ③.

![](../../raw/pages_0033-0064/images/page_43_image_8.jpg)

<details>
<summary>text_image</summary>

a⃗×b⃗
b⃗
</details>

Abb. 29a - Schraubregel

![](../../raw/pages_0033-0064/images/page_43_image_10.jpg)

<details>
<summary>text_image</summary>

b
e₃
b₁e₁+b₂e₂
-b₂e₁+b₁e₂
</details>

Abb. 29b - Konstruktion von $\vec{e}_3 \times \vec{b}$

Beachte. Die $\times$-Multiplikation ist nicht assoziativ, da i.a. $\vec{a} \times (\vec{b} \times \vec{c}) \neq (\vec{a} \times \vec{b}) \times \vec{c}$. So ist z.B. $-\vec{e}_2 = \vec{e}_1 \times \vec{e}_3 = \vec{e}_1 \times (\vec{e}_1 \times \vec{e}_2) \neq (\vec{e}_1 \times \vec{e}_1) \times \vec{e}_2 = \vec{0}$.

Rechenregeln für das Vektorprodukt:

a) $\vec{a} \times \vec{a} = \vec{0}$, $\vec{a} \times \vec{b} = -(\vec{b} \times \vec{a})$,

b) $\alpha (\vec{a}\times \vec{b}) = (\alpha \vec{a})\times \vec{b} = \vec{a}\times (\alpha \vec{b})$ (für $\alpha \in \mathbb{R}$),

c) $\vec{a} \times (\vec{b} + \vec{c}) = \vec{a} \times \vec{b} + \vec{a} \times \vec{c}$

(9)  $(\vec{a} + \vec{b}) \times \vec{c} = \vec{a} \times \vec{c} + \vec{b} \times \vec{c}$  (Distributivgesetze),

d) $\vec{a} \times \vec{b} = \vec{0} \iff \vec{a} = \vec{0}$ oder $\vec{b} = \vec{0}$ oder $\vec{a}$, $\vec{b}$ parallel (Parallelitätstest),

e) $|\vec{a}\times \vec{b}|^2 = |\vec{a}|^2 |\vec{b}|^2 -(\vec{a}\cdot \vec{b})^2$

Beweis. a), b), d) und e) ergeben sich leicht aus der Definition, wobei für e) nur  $(\sin\varphi)^{2}=1-(\cos\varphi)^{2}$  zu beachten ist. Wegen  $\vec{a}\times\vec{b}=-(\vec{b}\times\vec{a})$  braucht nur eines der Distributivgesetze nachgewiesen zu werden. O.E. wählen wir  $\vec{a}=\alpha\vec{e}_{3}$  mit  $\alpha\geq0$  in einer kartesischen Basis  $(\vec{e}_{1},\vec{e}_{2},\vec{e}_{3})$ . Damit kann man c) explizit mit b) und (8b) nachrechnen.

---

§5. Produkte

29

Aufgrund des Distributivgesetzes lassen sich Produkte in gewohnter Weise ausmultiplizieren (das Vektorprodukt ist in jedem Faktor linear):

$$
(a _ {1} \vec {u} _ {1} + \dots + a _ {n} \vec {u} _ {n}) \times (b _ {1} \vec {v} _ {1} + \dots + b _ {m} \vec {v} _ {m}) = a _ {1} b _ {1} (\vec {u} _ {1} \times \vec {v} _ {1}) + \dots + a _ {n} b _ {m} (\vec {u} _ {n} \times \vec {v} _ {m}).
$$

Insbesondere erhält man in einer kartesischen Basis  $(\vec{e}_{1},\vec{e}_{2},\vec{e}_{3})$  mit (8a) für  $\vec{a}=a_{1}\vec{e}_{1}+a_{2}\vec{e}_{2}+a_{3}\vec{e}_{3}$  und  $\vec{b}=b_{1}\vec{e}_{1}+b_{2}\vec{e}_{2}+b_{3}\vec{e}_{3}$

$$
\vec {a} \times \vec {b} = (a _ {2} b _ {3} - a _ {3} b _ {2}) \vec {e} _ {1} + (a _ {3} b _ {1} - a _ {1} b _ {3}) \vec {e} _ {2} + (a _ {1} b _ {2} - a _ {2} b _ {1}) \vec {e} _ {3}.
$$

In anderer Schreibweise:

(10)

$$
\left( \begin{array}{c} a _ {1} \\ a _ {2} \\ a _ {3} \end{array} \right) \times \left( \begin{array}{c} b _ {1} \\ b _ {2} \\ b _ {3} \end{array} \right) = \left( \begin{array}{c} a _ {2} b _ {3} - a _ {3} b _ {2} \\ a _ {3} b _ {1} - a _ {1} b _ {3} \\ a _ {1} b _ {2} - a _ {2} b _ {1} \end{array} \right).
$$

Als Gedächtnisstütze schreibt man (10) oft in Form einer formalen 3-reihigen Determinante, die nach der Regel von SARRUS auszuwerten ist (→ Kap. 6, 5.1):

$$
\left( \begin{array}{c} a _ {1} \\ a _ {2} \\ a _ {3} \end{array} \right) \times \left( \begin{array}{c} b _ {1} \\ b _ {2} \\ b _ {3} \end{array} \right) = \left| \begin{array}{c c c} \vec {e} _ {1} & a _ {1} & b _ {1} \\ \vec {e} _ {2} & a _ {2} & b _ {2} \\ \vec {e} _ {3} & a _ {3} & b _ {3} \end{array} \right|.
$$

Zwei nützliche Identitäten bestätigt man leicht mit (10) (→ Aufg. 2):

a) $\vec{a}\times (\vec{b}\times \vec{c}) = (\vec{a}\cdot \vec{c})\vec{b} - (\vec{a}\cdot \vec{b})\vec{c}$ (Grassmann)

b) $(\vec{a}\times \vec{b})\cdot (\vec{c}\times \vec{d}) = (\vec{a}\cdot \vec{c})(\vec{b}\cdot \vec{d}) - (\vec{b}\cdot \vec{c})(\vec{a}\cdot \vec{d})$ (Lagrange)

Speziell ergibt sich durch Vergleich von (11a) mit (6) für  $\vec{b} \neq \vec{0}$  eine Produktform für die orthogonale Komponente von  $\vec{a}$  längs  $\vec{b}$ :

$$
\vec {a} _ {\vec {b}} ^ {\perp} = \frac {1}{| \vec {b} | ^ {2}} b \times (\vec {a} \times b)  . \tag {12}
$$

Beispiel 1. Der Flächeninhalt eines Dreiecks $ABC$ ist $F = \frac{1}{2} \left| \overrightarrow{AB} \times \overrightarrow{AC} \right|$.

Für  $A = (1, 2, 3)$ ,  $B = (-2, 0, 4)$ ,  $C = (-1, -1, 2)$  ergibt sich mit (9e)

$$
F = \frac {1}{2} \left| \left( \begin{array}{c} - 3 \\ - 2 \\ 1 \end{array} \right) \times \left( \begin{array}{c} - 2 \\ - 3 \\ - 1 \end{array} \right) \right| = \frac {1}{2} \sqrt {1 4 \cdot 1 4 - 1 1 ^ {2}} = \frac {1}{2} \sqrt {7 5} = 4. 3 3 0 1 2 7 \dots . \quad \square
$$

Beispiel 2. Das Moment einer Einzelkraft $\vec{K}$, die im Punkt $A$ angreift, ist in bezug auf den Ursprung durch $\vec{m}_O := \overrightarrow{OA} \times \vec{K}$ gegeben (Einheit ist Nm, $\to \S7$).

Für  $A = (1, 2, 3)$  und  $\vec{K} = \begin{pmatrix} -1 \\ 0 \\ 4 \end{pmatrix}$  erhält man  $\vec{m}_{O} = \begin{pmatrix} 8 \\ -7 \\ 2 \end{pmatrix}$ .

---

30

1. Zahlen und Vektoren

5.4 Das Spatprodukt. Eine Kombination aus Skalarprodukt und Vektorprodukt ist das aus je drei Vektoren gebildete Spatprodukt

$$
[ \vec {a}, \vec {b}, \vec {c} ] := \vec {a} \cdot (\vec {b} \times \vec {c}).
$$

Satz 5.1. Der von den Vektoren $\vec{a}$, $\vec{b}$, $\vec{c}$ aufgespannte Spat ($\rightarrow$ Abb. 30a, auch Parallelflach oder Parallelepiped genannt) hat das Volumen

$$
V = | \left[ \vec {a}, \vec {b}, \vec {c} \right] |.
$$

Beweis. Die Grundfläche mit den Kanten $\vec{b}$, $\vec{c}$ hat den Flächeninhalt $F = |\vec{b} \times \vec{c}|$ ($\rightarrow$ Def. des $\times$-Produkts). Die Höhe $h$ des Spats bezüglich dieser Grundfläche beträgt $h = |\vec{a}_{\vec{b} \times \vec{c}}|$ mit der Komponente von $\vec{a}$ in Richtung des auf der Grundfläche senkrecht stehenden Vektors $\vec{b} \times \vec{c}$. Mit (6) ergibt sich $h = \left|\frac{\vec{a} \cdot (\vec{b} \times \vec{c})}{|\vec{b} \times \vec{c}|^2} \vec{b} \times \vec{c}\right|$ und damit $V = F \cdot h = |\vec{a} \cdot (\vec{b} \times \vec{c})|$.

![](../../raw/pages_0033-0064/images/page_45_image_7.jpg)

<details>
<summary>text_image</summary>

b × c
h
a
F
b
c
</details>

Abb. 30a - Spat

![](../../raw/pages_0033-0064/images/page_45_image_9.jpg)

<details>
<summary>text_image</summary>

b x c
h
a
b
c
</details>

Abb. 30b - Tetraeder

## Folgerungen.

① Das Volumen eines Tetraeders mit den Kanten  $\vec{a}$ ,  $\vec{b}$ ,  $\vec{c}$  beträgt

$$
V _ {T e t r} = \frac {1}{6} V _ {S p a t} = \frac {1}{6} | [ \vec {a}, \vec {b}, \vec {c} ] |.
$$

② TEST für lineare Unabhängigkeit.

Die Vektoren  $\vec{a}, \vec{b}, \vec{c}$  sind nicht parallel zu einer Ebene (man sagt, sie sind linear unabhängig)  $\Longleftrightarrow [\vec{a}, \vec{b}, \vec{c}] \neq 0.$

③ TEST für Rechtssystem.

$(\vec{a},\vec{b},\vec{c})$ ist ein Rechtssystem $\Longleftrightarrow [\vec{a},\vec{b},\vec{c}] > 0.$

Beweis. ① „Tetraedervolumen = $\frac{1}{3} \cdot$ Grundfläche $\cdot$ Höhe“ ($\rightarrow$ Abb. 30b).
② Nur dann bilden  $\vec{a}$ ,  $\vec{b}$ ,  $\vec{c}$  die Kanten eines echten Spats mit Volumen  $\neq 0$ .
③ An einer Skizze erkennt man, daß  $(\vec{a},\vec{b},\vec{c})$  genau dann ein Rechtssystem ist,

---

§5. Produkte

31

wenn der Winkel zwischen $\vec{a}$ und $\vec{b} \times \vec{c}$ spitz ist, d.h. wenn $0 \leq \nmid (\vec{a}, \vec{b} \times \vec{c}) \leq \frac{\pi}{2}$ gilt. Das ist gleichbedeutend mit $\vec{a} \cdot (\vec{b} \times \vec{c}) = |\vec{a}| |\vec{b} \times \vec{c}|\cos \nmid (\vec{a}, \vec{b} \times \vec{c}) > 0$.

Für  $\vec{a} = \sum a_{i}\vec{e}_{i}$ ,  $\vec{b} = \sum b_{i}\vec{e}_{i}$  und  $\vec{c} = \sum c_{i}\vec{e}_{i}$  (in kartesischen Koordinaten) erhält man mit (10) und (5a)

$$
[ \vec {a}, \vec {b}, \vec {c} ] = a _ {1} (b _ {2} c _ {3} - b _ {3} c _ {2}) + a _ {2} (b _ {3} c _ {1} - b _ {1} c _ {3}) + a _ {3} (b _ {1} c _ {2} - b _ {2} c _ {1}). \tag {13}
$$

Dies ist der Wert einer dreireihigen Determinante (→ Kap. 6, §5), nämlich

$$
[ \vec {a}, \vec {b}, \vec {c} ] = \left| \begin{array}{c c c} a _ {1} & b _ {1} & c _ {1} \\ a _ {2} & b _ {2} & c _ {2} \\ a _ {3} & b _ {3} & c _ {3} \end{array} \right| .
$$

Beispiel 1. Für die Vektoren $\vec{a} = \begin{pmatrix} 1 \\ 2 \\ 3 \end{pmatrix}$, $\vec{b} = \begin{pmatrix} -2 \\ 0 \\ -2 \end{pmatrix}$, $\vec{c} = \begin{pmatrix} 2 \\ -1 \\ -2 \end{pmatrix}$ ergibt sich aus (13) $[\vec{a},\vec{b},\vec{c}] = -12$. $\vec{a}$, $\vec{b}$, $\vec{c}$ spannen einen Spat mit Volumen $V_{Spat} = 12$ und ein Tetraeder mit Volumen $V_{Tetr} = 2$ auf.

Beispiel 2. Für $\vec{v}_1 = \frac{\sqrt{2}}{4}\left( \begin{array}{c} -1 \\ \sqrt{3} \\ 2 \end{array} \right)$, $\vec{v}_2 = -\frac{1}{2}\left( \begin{array}{c}\sqrt{3} \\ 1 \\ 0 \end{array} \right)$, $\vec{v}_3 = \frac{\sqrt{2}}{4}\left( \begin{array}{c}1 \\ -\sqrt{3} \\ 2 \end{array} \right)$ gilt $|\vec{v}_i| = 1$, $\vec{v}_i \cdot \vec{v}_j = 0$, für $i \neq j$ und $[\vec{v}_1, \vec{v}_2, \vec{v}_3] = 1$. $\vec{v}_1$, $\vec{v}_2$, $\vec{v}_3$ bilden ein Rechtssystem, sie stellen die Basisvektoren eines gedrehten kartesischen Koordinatensystems dar ($\rightarrow$ Kap. 6, 6.6).

Beispiel 3. Nichtorthogonale Zerlegung (→ Abb. 31). Die drei Stäbe eines Tragbockes führen von der Spitze S in Richtung der drei Einheitsvektoren $\vec{a} = \vec{e}_1$, $\vec{b} = \frac{1}{\sqrt{2}} \begin{pmatrix} 1 \\ -1 \\ 0 \end{pmatrix}$, $\vec{c} = \frac{1}{\sqrt{11}} \begin{pmatrix} 1 \\ 1 \\ -3 \end{pmatrix}$. In S zieht die Kraft $\vec{K} = 60\mathrm{N} \begin{pmatrix} 0 \\ 1 \\ -1 \end{pmatrix}$ und ruft in A, B, C die Lagerreaktionen $\vec{K}_A = \alpha \vec{a}$, $\vec{K}_B = \beta \vec{b}$, $\vec{K}_C = \gamma \vec{c}$ hervor. $\alpha, \beta, \gamma$ ergeben sich aus der Gleichgewichtsbedingung

$$
\vec {K} + \vec {K} _ {A} + \vec {K} _ {B} + \vec {K} _ {C} = \vec {K} + \alpha \vec {a} + \beta \vec {b} + \gamma \vec {c} = \vec {0}.
$$

Multipliziert man diese Gleichung der Reihe nach mit $\vec{b} \times \vec{c}$, $\vec{c} \times \vec{a}$, $\vec{a} \times \vec{b}$ skalar durch, so verschwinden je zwei Summanden ($\rightarrow$ Definition von $\times$ ①)

$$
(\vec {b} \times \vec {c}) \cdot \vec {K} + \alpha (\vec {b} \times \vec {c}) \cdot \vec {a} = 0 \quad \Longrightarrow \quad \alpha = - \frac {[ \vec {K} , \vec {b} , \vec {c} ]}{[ \vec {a} , \vec {b} , \vec {c} ]} = - 2 0   \mathrm{N},
$$

$$
(\vec {c} \times \vec {a}) \cdot \vec {K} + \beta (\vec {c} \times \vec {a}) \cdot \vec {b} = 0 \quad \Longrightarrow \quad \beta = - \frac {[ \vec {K} , \vec {c} , \vec {a} ]}{[ \vec {b} , \vec {c} , \vec {a} ]} = 4 0 \sqrt {2}   \mathrm{N},
$$

$$
(\vec {a} \times \vec {b}) \cdot \vec {K} + \gamma (\vec {a} \times \vec {b}) \cdot \vec {c} = 0 \quad \Longrightarrow \quad \gamma = - \frac {[ \vec {K} , \vec {a} , \vec {b} ]}{[ \vec {c} , \vec {a} , \vec {b} ]} = - 2 0 \sqrt {1 1} \mathrm{N}. \quad \square
$$

---

32

1. Zahlen und Vektoren

![](../../raw/pages_0033-0064/images/page_47_image_2.jpg)

<details>
<summary>text_image</summary>

K
→
→
→
→
A
C
B
</details>

Abb. 31 - Tragbock

![](../../raw/pages_0033-0064/images/page_47_image_4.jpg)

<details>
<summary>text_image</summary>

D
C
z
y
x
A
B
</details>

Abb. 32 - Würfel

Beispiel 4. Das größte Quadrat in einem Würfel. Im Würfel $W$ ($\rightarrow$ Abb. 32) mit den 8 Ecken $(\pm 1, \pm 1, \pm 1)$ sind auf den Würfelkanten 4 Punkte ausgewählt $(-1 \leq a, b \leq 1)$: $A = (1, a, -1)$, $B = (b, 1, -1)$, $C = (-1, -a, 1)$, $D = (-b, -1, 1)$. Die vier Punkte liegen stets in einer Ebene, da

$$
\begin{array}{l} [ \overrightarrow {A B}, \overrightarrow {B C}, \overrightarrow {C D} ] = \left[ \left( \begin{array}{c} b - 1 \\ 1 - a \\ 0 \end{array} \right), \left( \begin{array}{c} - 1 - b \\ - a - 1 \\ 2 \end{array} \right), \left( \begin{array}{c} - b + 1 \\ - 1 + a \\ 0 \end{array} \right) \right] \\ = 2 (b - 1) (1 - a) + 2 (1 - a) (1 - b) = 0. \\ \end{array}
$$

ABCD ist stets ein Parallelogramm, da  $\overrightarrow{AB} = -\overrightarrow{CD}$  und  $\overrightarrow{AD} = \overrightarrow{BC}$ . Der Flächeninhalt ist

$$
F = | \overrightarrow {A B} \times \overrightarrow {B C} | = 2 \sqrt {(1 - a) ^ {2} + (1 - b) ^ {2} + (1 - a b) ^ {2}}.
$$

ABCD ist eine Raute, wenn  $\overrightarrow{AC} \cdot \overrightarrow{BD} = 0$ , dh.  $1 + a + b = 0$ . ABCD ist ein Quadrat, wenn zusätzlich  $|\overrightarrow{AC}| = |\overrightarrow{BD}|$ , d.h.  $a^{2} = b^{2}$ ; das ist nur dann der Fall, wenn  $a = b = -\frac{1}{2}$ . Dieses Quadrat hat den Flächeninhalt  $\frac{9}{2}$ . ☐

## Aufgaben.

1. $P_{1}, P_{2}, \ldots, P_{6}$ seien die Ecken eines regulären Sechsecks im Raum.

a) Man suche Bedingungen, welche die Länge und die gegenseitige Lage der Vektoren  $\overrightarrow{P_{1}P_{2}}$  und  $\overrightarrow{P_{2}P_{3}}$  bestimmen!
b) Man bestimme  $P_{3}, P_{4}, P_{5}$  und  $P_{6}$  für den Fall, daß

$$
P _ {1} = O, P _ {2} = (\sqrt {3}, 1, 0) \text {und} \vec {e} _ {1} \perp \overrightarrow {P _ {2} P _ {3}}.
$$

![](../../raw/pages_0033-0064/images/page_47_image_17.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph LR
  P1["P1"] --> P2["P2"]
  P2 --> P3["P3"]
  P3 --> P4["P4"]
  P4 --> P5["P5"]
  P5 --> P6["P6"]
```
</details>

2. Man rechne (11) explizit mittels (10) für den Fall $\vec{a} = \vec{e}_3$, $\vec{b} = \alpha \vec{e}_1 + \beta \vec{e}_2$ nach. Welche trivialen Fälle bleiben dann noch zu diskutieren?

---

§5. Produkte

33

3. Man bestätige  $[\vec{a},\vec{b},\vec{c}]=[ \vec{b},\vec{c},\vec{a}] = [\vec{c},\vec{a},\vec{b}]$  und  $[\vec{b},\vec{a},\vec{c}] = -[\vec{a},\vec{b},\vec{c}]$ .

4. Im Würfel mit den 8 Ecken (±1, ±1, ±1) bestimme man die Einheitsvektoren $\vec{d}_1, \ldots, \vec{d}_4$ in Richtung der vier Raumdiagonalen, für welche $\vec{e}_3 \cdot \vec{d}_i > 0$ ($i = 1, 2, 3, 4$) und berechne alle Winkel, die zwischen den $\vec{d}_i$ möglich sind.

5. Man berechne für die Vektoren des $\mathbb{R}^3$

$$
\vec {x} = \left( \begin{array}{c} 0 \\ 1 \\ 2 \end{array} \right), \quad \vec {y} = \left( \begin{array}{c} 2 \\ 1 \\ 0 \end{array} \right), \quad \vec {z} = \left( \begin{array}{c} 3 \\ 0 \\ 4 \end{array} \right)
$$

![](../../raw/pages_0033-0064/images/page_48_image_6.jpg)

<details>
<summary>text_image</summary>

z
y
x
d₄
d₃
d₁
d₂
</details>

a) die orthogonale Zerlegung von  $\vec{x}$  längs  $\vec{y}$  bzw. längs  $\vec{z}$ ,

b) folgende Ausdrücke und gebe eine geometrische Deutung:

$$
(\vec {x} \cdot \vec {y}) \vec {y};
$$

$$
(\vec {x} + \vec {y}) \times (\vec {x} - \vec {y});
$$

$$
(\vec {x} \times \vec {y}) \times \vec {z} - \vec {x} \times (\vec {y} \times \vec {z});
$$

$$
[ \vec {x}, \vec {y}, \vec {z} ];
$$

$$
(\vec {x} + \vec {y} + 2 \vec {z}) \cdot \vec {z};
$$

$$
(4 \vec {x} \cdot \vec {y}) \vec {z} - (\vec {y} \cdot 3 \vec {z}) \vec {x} .
$$

6. Ein Massenpunkt P bewegt sich mit konstanter Winkelgeschwindigkeit  $\omega$  auf einer Kreisbahn (Mittelpunkt O, Radius r). Der Ortsvektor  $\vec{x}$ , der Geschwindigkeitsvektor  $\vec{v}$  und der Winkelgeschwindigkeitsvektor  $\vec{\omega}$  ( $|\vec{\omega}| = \omega$ ) bilden ein Rechtssystem, der Beschleunigungsvektor ist  $\vec{a} = -\omega^{2}\vec{x}$ .

Man zeige mit  $|\vec{v}| = \omega r$

$$
\vec {v} = \vec {\omega} \times \vec {x}, \quad \vec {a} = \vec {\omega} \times (\vec {\omega} \times \vec {x}).
$$

![](../../raw/pages_0033-0064/images/page_48_image_18.jpg)

<details>
<summary>text_image</summary>

ω
0
x
P
v
</details>

7. Die 5 regulären konvexen Polyeder (konvexe Polyeder mit kongruenten Seitenflächen).

| Polyeder | Seitenflächen | Kanten | Ecken |
| --- | --- | --- | --- |
| Tetraeder | 4 gleichseitige Dreiecke | 6 | 4 |
| Würfel | 6 Quadrate | 12 | 8 |
| Oktaeder | 8 gleichseitige Dreiecke | 12 | 6 |
| Dodekaeder | 12 reguläre Fünfecke | 30 | 20 |
| Ikosaeder | 20 gleichseitige Dreiecke | 30 | 12 |

![](../../raw/pages_0033-0064/images/page_48_image_21.jpg)

Ist das Oktaeder mit den Ecken  $(\pm1,0,0)$ ,  $(0,\pm1,0)$ ,  $(0,0,\pm1)$  und das Tetraeder mit den Ecken  $(1,1,1)$ ,  $(1,-1,-1)$ ,  $(-1,-1,1)$ ,  $(-1,1,-1)$  regulär? Man berechne die Volumeninhalte.

---

34

1. Zahlen und Vektoren

## §6. Geraden und Ebenen

## 6.1 Parameterdarstellungen einer Geraden.

Ein Punkt $X$ liegt genau dann

auf der Geraden $g$ durch $A$ in Richtung $\vec{c}$, $\vec{c} \neq 0$ ($\rightarrow$ Abb. 33), wenn $\overrightarrow{AX}$ parallel ist zu $\vec{c}$; d.h., wenn es eine Zahl $t \in \mathbb{R}$ gibt mit $\overrightarrow{AX} = t\vec{c}$. Man sagt hierzu: $g$ hat die

$$
\boxed { \begin{array}{c} \text {Punkt - Richtungsgleichung} \\ \overrightarrow {A X} = t \vec {c}, t \in \mathbb {R}. \end{array} } \tag {1}
$$

![](../../raw/pages_0033-0064/images/page_49_image_7.jpg)

<details>
<summary>text_image</summary>

τc
A
S
P̅A
X
P̅X
P
mₚ
</details>

Abb. 33 - Gerade durch A längs  $\vec{c}$

Die in (1) auftretende Variable $t$ nennt man einen Parameter; zu jedem Parameterwert $t = t_0$ gehört genau ein Punkt $X_0$ auf $g$ mit $\overrightarrow{AX_0} = t_0\vec{c} -$ und umgekehrt.

Wegen  $\overrightarrow{AX} = \overrightarrow{PX} - \overrightarrow{PA}$  läßt sich g in bezug auf einen beliebigen Punkt P darstellen durch

$$
\boxed {\overrightarrow {P X} = \overrightarrow {P A} + t \vec {c}, t \in \mathbb {R}.} \tag {2}
$$

Wird nun im Raum ein kartesisches Koordinatensystem  $(O;\vec{e}_{1},\vec{e}_{2},\vec{e}_{3})$  festgelegt und wird  $\vec{c}=c_{1}\vec{e}_{1}+c_{2}\vec{e}_{2}+c_{3}\vec{e}_{3}$  durch 2 verschiedene Punkte  $A=(a_{1},a_{2},a_{3})$ ,  $B=(b_{1},b_{2},b_{3})$  bestimmt – d.h.  $c_{i}=b_{i}-a_{i}$ , i=1,2,3 – dann geht (2) – mit P=O – über in

$$
\boxed {\overrightarrow {O X} = \overrightarrow {O A} + t \vec {c} = \overrightarrow {O A} + t (\overrightarrow {O B} - \overrightarrow {O A}), t \in \mathbb {R}} \tag {3}
$$

und ein Komponentenvergleich ergibt für die Geradenpunkte  $X = (x_{1}, x_{2}, x_{3})$  die drei Gleichungen

$$
\begin{array}{l l} \text {(4a)} & x _ {i} = a _ {i} + t c _ {i}, t \in \mathbb {R} \quad (i = 1, 2, 3) \quad \text {Punkt - Richtungs - Gl.} \\ \text {bzw.} & \\ \text {(4b)} & x _ {i} = a _ {i} + t (b _ {i} - a _ {i}), t \in \mathbb {R} \quad (i = 1, 2, 3) \quad \text {Zwei Punkte - Gl.} \end{array}
$$

Jede der Formeln (1)-(4b) nennt man eine Parameterdarstellung von $g$.

Beispiel. Die Gerade g durch  $A = (1,0,-1)$  in Richtung  $\vec{c} = \vec{e}_{1} + \vec{e}_{2} + 2\vec{e}_{3}$  hat eine Parameterdarstellung

$$
\left( \begin{array}{c} x _ {1} \\ x _ {2} \\ x _ {3} \end{array} \right) = \left( \begin{array}{c} 1 \\ 0 \\ - 1 \end{array} \right) + t \left( \begin{array}{c} 1 \\ 1 \\ 2 \end{array} \right), t \in \mathbb {R}.
$$

---

§6. Geraden und Ebenen

35

In Komponenten lautet sie:

$$
x _ {1} = 1 + t, \quad x _ {2} = t, \quad x _ {3} = - 1 + 2 t.
$$

Zu den Parameterwerten $t = 1, -1, 5$ gehören die Geradenpunkte $B_1 = (2, 1, 1)$, $B_2 = (0, -1, -3)$, $B_3 = (6, 5, 9)$. Demnach besitzt $g$ ebenfalls die Parameterdarstellung (Zwei-Punkte-Gleichung in Komponenten)

$$
x _ {1} = 6 - 6 t, x _ {2} = 5 - 6 t, x _ {3} = 9 - 1 2 t.
$$

6.2 Die Koordinatengleichungen einer Geraden. Löst man jede der Gleichungen aus (4b) nach t auf und setzt die Ausdrücke gleich, so erhält man für die Gerade durch  $A = (a_{1}, a_{2}, a_{3})$  und  $B = (b_{1}, b_{2}, b_{3})$  eine parameterfreie Darstellung mit zwei Gleichungen:

## Koordinatengleichungen der Geraden durch $A, B$

a) $\frac{x_1 - a_1}{b_1 - a_1} = \frac{x_2 - a_2}{b_2 - a_2} = \frac{x_3 - a_3}{b_3 - a_3}$, falls $a_i \neq b_i$ ($i = 1, 2, 3$),
b) $\frac{x_1 - a_1}{b_1 - a_1} = \frac{x_2 - a_2}{b_2 - a_2}, x_3 = a_3,$ falls $b_{3} = a_{3}, b_{1} \neq a_{1}, b_{2} \neq a_{2},$

(5) $\frac{x_3 - a_3}{b_3 - a_3} = \frac{x_1 - a_1}{b_1 - a_1}, x_2 = a_2,$ falls $b_{2} = a_{2}, b_{3} \neq a_{3}, b_{1} \neq a_{1},$

$$
\frac {x _ {2} - a _ {2}}{b _ {2} - a _ {2}} = \frac {x _ {3} - a _ {3}}{b _ {3} - a _ {3}}, x _ {1} = a _ {1}, \quad \text {falls} b _ {1} = a _ {1}, b _ {2} \neq a _ {2}, b _ {3} \neq a _ {3},
$$

c) $x_{1} = a_{1}, x_{2} = a_{2}$, falls $b_{1} = a_{1}, b_{2} = a_{2}, b_{3} \neq a_{3}$,

$x_{3} = a_{3}, x_{1} = a_{1}$, falls $b_{3} = a_{3}, b_{1} = a_{1}, b_{2} \neq a_{2}$,

$x_{2} = a_{2}, x_{3} = a_{3}$, falls $b_{2} = a_{2}, b_{3} = a_{3}, b_{1} \neq a_{1}$.

Aus der parameterfreien Zwei-Punkte-Form für $g$ findet man über $t := \frac{x_i - a_i}{b_i - a_i}$ mit dem Index $i$, für den $b_i \neq a_i$ gilt, zur Parameterform (4b) zurück.

Beispiel 1. Die Gerade $x_{1}=4-9t$, $x_{2}=2$, $x_{3}=1+t$ ($t\in\mathbb{R}$) hat die zwei Koordinatengleichungen

$$
\frac {4 - x _ {1}}{9} = x _ {3} - 1, x _ {2} = 2.
$$

Beispiel 2. Die Gerade mit den Koordinatengleichungen $\frac{x_1 - 3}{5} = \frac{x_2 + 1}{7}$, $x_3 = 4$ besitzt die Parameterdarstellung

$$
x _ {1} = 3 + 5 t, x _ {2} = - 1 + 7 t, x _ {3} = 4;
$$

sie geht durch die Punkte  $(3,-1,4)$  und  $(8,6,4)$ .

□

---

36

1. Zahlen und Vektoren

6.3 Die Momentengleichung der Geraden g durch A in Richtung  $\vec{c}$  ( $\rightarrow$  Abb. 33) lautet für einen beliebigen Bezugspunkt P :

(6)

Momentengleichung

$$
\overrightarrow {P X} \times \vec {c} = \vec {m} _ {P} \quad \text {mit} \quad \vec {m} _ {P} = \overrightarrow {P A} \times \vec {c}.
$$

Es ist nämlich $\overrightarrow{AX} = \overrightarrow{PX} - \overrightarrow{PA}$ genau dann parallel zu $\vec{c}$, wenn $\overrightarrow{AX} \times \vec{c} = (\overrightarrow{PX} - \overrightarrow{PA}) \times \vec{c} = \vec{0}$ gilt ($\rightarrow$ §5 (9d)).

Die Darstellung (6) ist insbesondere dann zweckmäßig, wenn $g$ die Wirkungslinie der Kraft $\vec{c}$ ist, die bezüglich $P$ das Moment $\vec{m}_P = \overrightarrow{PA} \times \vec{c}$ besitzt ($\to \S7$). Nach §5 (12) ist

$$
\overrightarrow {P S} = \frac {1}{| \vec {c} | ^ {2}} \vec {c} \times (\overrightarrow {P A} \times \vec {c}) = \frac {1}{| \vec {c} | ^ {2}} \vec {c} \times \vec {m} _ {P} \tag {7}
$$

der Lotvektor von P auf g und demnach

$$
\overrightarrow {P X} = \frac {1}{| \vec {c} | ^ {2}} \vec {c} \times \vec {m} _ {P} + t \vec {c}, t \in \mathbb {R},
$$

eine Parameterdarstellung der durch die Momentengleichung (6) dargestellten Geraden g.

Beispiel. Im kartesischen Koordinatensystem  $(O;\vec{e}_{1},\vec{e}_{2},\vec{e}_{3})$  hat die durch

$$
\left( \begin{array}{c} x _ {1} \\ x _ {2} \\ x _ {3} \end{array} \right) \times \left( \begin{array}{c} 1 \\ 2 \\ 3 \end{array} \right) = \left( \begin{array}{c} - 1 \\ - 1 \\ 1 \end{array} \right)
$$

bestimmte Gerade $g$ die Richtung $\vec{c} = \begin{pmatrix} 1 \\ 2 \\ 3 \end{pmatrix}$. Ferner ist $\overrightarrow{OS} = \frac{1}{|\vec{c}|^2} \vec{c} \times \vec{m} = \frac{1}{14} \begin{pmatrix} 1 \\ 2 \\ 3 \end{pmatrix} \times \begin{pmatrix} -1 \\ -1 \\ 1 \end{pmatrix} = \frac{1}{14} \begin{pmatrix} 5 \\ -4 \\ 1 \end{pmatrix}$ der Lotvektor vom Ursprung $O$ auf $g$, insbesondere $S = \frac{1}{14}(5, -4, 1)$ ein Geradenpunkt. Demnach lautet eine Parameter-darstellung von $g: x_1 = \frac{5}{14} + t$, $x_2 = -\frac{2}{7} + 2t$, $x_3 = \frac{1}{14} + 3t$.

6.4 Abstand Punkt-Gerade. Der Lotvektor vom Punkt $P$ auf die Gerade $g$ durch $A$ in Richtung $\vec{c}$ ist $\overrightarrow{PS} = \frac{1}{|\vec{c}|^2}\vec{c} \times (\overrightarrow{PA} \times \vec{c})$ ($\rightarrow$ Abb. 33 und (7)), sein Betrag gibt den Abstand $d$ des Punktes $P$ von $g$ an; also gilt

(8)

$$
\boxed {d = \frac {| \overrightarrow {P A} \times \vec {c} |}{| \vec {c} |} .}
$$

---

§6. Geraden und Ebenen

37

Beispiel. Der Abstand des Punktes  $P = (15, -2, 6)$  von der Geraden g :  $x_{1} = 1 + t$ ,  $x_{2} = 1 - t$ ,  $x_{3} = 2$  beträgt

$$
\begin{array}{l} d = \frac {1}{\sqrt {1 ^ {2} + 1 ^ {2}}} \left| \left( \begin{array}{c} - 1 4 \\ 3 \\ - 4 \end{array} \right) \times \left( \begin{array}{c} 1 \\ - 1 \\ 0 \end{array} \right) \right| \\ = \frac {1}{\sqrt {2}} \sqrt {(- 4) ^ {2} + (- 4) ^ {2} + 1 1 ^ {2}} = \sqrt {\frac {1 5 3}{2}} \approx 8. 7 4 6. \\ \end{array}
$$

6.5 Abstand Gerade-Gerade. Der Abstand d der beiden Geraden

$$
g _ {1}: \quad \overrightarrow {O X} = \overrightarrow {O A} + t \vec {u},
$$

$$
g _ {2}: \quad \overrightarrow {O X} = \overrightarrow {O B} + t \vec {v} \quad (t \in \mathbb {R}, \vec {u}, \vec {v} \neq \vec {0})
$$

ist gegeben durch

a) $d = \frac{|\overrightarrow{AB} \times \vec{u}|}{|\vec{u}|}$, falls $\vec{u}, \vec{v}$ parallel sind, b) $d = \frac{|\overrightarrow{AB}, \vec{u}, \vec{v}|}{|\vec{u} \times \vec{v}|}$, falls $\vec{u} \times \vec{v} \neq \vec{0}$.

Beweis. Im ersten Fall wird der Abstand mit (8) berechnet. Im andern Fall ($\vec{u}$, $\vec{v}$ nicht parallel) ist $d$ der Betrag der Komponente von $\overrightarrow{AB}$ in Richtung des Vektors $\vec{n} := \vec{u} \times \vec{v}$, der auf $\vec{u}$ und $\vec{v}$ senkrecht steht ($\rightarrow$ Abb. 34). Mit Formel (6) aus §5 - für $\vec{a} = \overrightarrow{AB}$, $\vec{b} = \vec{u} \times \vec{v}$ - folgt die Behauptung.

![](../../raw/pages_0033-0064/images/page_52_image_10.jpg)

<details>
<summary>text_image</summary>

B
g₂
AB
d
A
v
u
g₁
</details>

Abb. 34 - Abstand zweier Geraden

Beispiel. Die Geraden

$$
g _ {1}: \quad x _ {1} = 2 + 3 t, x _ {2} = 4, x _ {3} = - 1 + t
$$

$$
g _ {2}: \quad x _ {1} = t, x _ {2} = 1 + t, x _ {3} = 5 - 3 t
$$

haben den Abstand

$$
d = \frac {1}{| \vec {u} \times \vec {v} |} | [ \overrightarrow {A B}, \vec {u}, \vec {v} ] | = \frac {1}{\left| \left( \begin{array}{c} 3 \\ 0 \\ 1 \end{array} \right) \times \left( \begin{array}{c} 1 \\ 1 \\ - 3 \end{array} \right) \right|} \left| \left| \begin{array}{c c c} - 2 & 3 & 1 \\ - 3 & 0 & 1 \\ 6 & 1 & - 3 \end{array} \right| \right| = \frac {1 0}{\sqrt {1 1 0}}. \quad \square
$$

Folgerung aus (9): Die nicht parallelen Geraden  $g_{1}$ ,  $g_{2}$  schneiden sich genau

---

38

1. Zahlen und Vektoren

dann, wenn $d = 0$, d.h. $[\overrightarrow{AB}, \vec{u}, \vec{v}] = 0$ ist. Der eindeutig bestimmte Schnittpunkt $X_S$ erfüllt $\overrightarrow{OX_S} = \overrightarrow{OA} + t_1\vec{u} = \overrightarrow{OB} + t_2\vec{v}$ mit gewissen Zahlen $t_1, t_2 \in \mathbb{R}$. Multipliziert man diese Beziehung vektoriell mit $\vec{u}$ bzw. $\vec{v}$ durch, so ergibt sich $t_1\vec{u} \times \vec{v} = \overrightarrow{AB} \times \vec{v}$ und $t_2\vec{u} \times \vec{v} = \overrightarrow{AB} \times \vec{u}$. Da $\vec{u} \times \vec{v} \neq \vec{0}$ ist, kann hieraus leicht $t_1$ und $t_2$ abgelesen werden; damit ist $X_S$ bestimmt.

Beispiel. Für die beiden Geraden $g_1 : x_1 = 0$, $x_2 = 2t$, $x_3 = 1 + t$ und $g_2 : x_1 = 1 + t$, $x_2 = 2$, $x_3 = 3 + t$ gilt $\vec{u} \times \vec{v} = \begin{pmatrix} 2 \\ 1 \\ -2 \end{pmatrix}$, $\overrightarrow{AB} = \begin{pmatrix} 1 \\ 2 \\ 2 \end{pmatrix}$. Damit ist $[\overrightarrow{AB}, \vec{u}, \vec{v}] = 0$, $t_1 = 1$, $t_2 = -1$ und $X_S = (0, 2, 2)$ der Schnittpunkt.

## 6.6 Parameterdarstellungen einer Ebene. Wir betrachten die Ebene E

mit dem „Aufpunkt“ A und den (von 0 verschiedenen und nicht parallelen) Richtungsvektoren $\vec{u}$, $\vec{v}$ ($\rightarrow$ Abb. 35). Ein Raumpunkt X liegt genau dann auf E, wenn sich der Vektor $\overrightarrow{AX}$ darstellen läßt in der Form $\overrightarrow{AX} = t\vec{u} + s\vec{v}$ mit Zahlen $t, s \in \mathbb{R}$. D.h. man hat (mit den beiden Parametern $t, s \in \mathbb{R}$) die

![](../../raw/pages_0033-0064/images/page_53_image_6.jpg)

<details>
<summary>text_image</summary>

F
A
A
X
S
P
C
C1
</details>

Abb. 35 - Die Ebene E

$$
\text {Parameterdarstellung von} E \quad \overrightarrow {A X} = t \vec {u} + s \vec {v} \quad (t, s \in \mathbb {R}). \tag {10}
$$

Wird ein kartesisches Koordinatensystem  $(O;\vec{e}_{1},\vec{e}_{2},\vec{e}_{3})$  festgelegt, so daß  $A=(a_{1},a_{2},a_{3})$ ,  $\vec{u}=u_{1}\vec{e}_{1}+u_{2}\vec{e}_{2}+u_{3}\vec{e}_{3}$ ,  $\vec{v}=v_{1}\vec{e}_{1}+v_{2}\vec{e}_{2}+v_{3}\vec{e}_{3}$ , dann ist (10) äquivalent zu den 3 Koordinatengleichungen

$$
x _ {i} = a _ {i} + t u _ {i} + s v _ {i} \quad (i = 1, 2, 3; t, s \in \mathbb {R}). \tag {10a}
$$

Werden $\vec{u}$ und $\vec{v}$ durch die drei verschiedenen Punkte $A = (a_{1}, a_{2}, a_{3})$, $B = (b_{1}, b_{2}, b_{3})$, $C = (c_{1}, c_{2}, c_{3})$ bestimmt, $\vec{u} = \overrightarrow{AB}$, $\vec{v} = \overrightarrow{AC}$ (d.h. $u_{i} = b_{i} - a_{i}$, $v_{i} = c_{i} - a_{i}$), dann geht (10a) über in die

Drei-Punkte-Gleichung der Ebene E

$$
x _ {i} = a _ {i} + t (b _ {i} - a _ {i}) + s (c _ {i} - a _ {i}) \quad (i = 1, 2, 3; t, s \in \mathbb {R}) \tag {10b}
$$

mit $A = (a_{1}, a_{2}, a_{3})$, $B = (b_{1}, b_{2}, b_{3})$, $C = (c_{1}, c_{2}, c_{3})$.

---

§6. Geraden und Ebenen

39

6.7 Parameterfreie Darstellungen einer Ebene. Ein Punkt X liegt genau dann auf E (E wie in 6.6, → Abb. 35), wenn die Vektoren  $\overrightarrow{AX}$ ,  $\vec{u} = \overrightarrow{AB}$ ,  $\vec{v} = \overrightarrow{AC}$  zu E parallel sind; genau in diesem Fall gilt ( $\rightarrow$  5.4)

(11)

$$
\left[ \overrightarrow {A X}, \overrightarrow {A B}, \overrightarrow {A C} \right] = 0.
$$

Dieses ist eine parameterfreie Drei-Punkte-Formel für $E$ in Determinantenform. (11) bedeutet, daß $\overrightarrow{AX} \cdot (\overrightarrow{AB} \times \overrightarrow{AC}) = 0$. $\vec{n} := \overrightarrow{AB} \times \overrightarrow{AC}$ steht also senkrecht auf $E$; man nennt ihn daher einen Normalenvektor von $E$ und

(12)

$$
\overrightarrow {A X} \cdot \vec {n} = 0 \quad (A \text {Aufpunkt,} \vec {n} \text {Normalenvektor von} E)
$$

eine Normalengleichung von $E$. In kartesischen Koordinaten entsteht hieraus für $X = (x_1, x_2, x_3)$, $A = (a_1, a_2, a_3)$ und $\vec{n} = n_1 \vec{e}_1 + n_2 \vec{e}_2 + n_3 \vec{e}_3$ die

$$
\begin{array}{l} \text {Koordinatendarstellung von E} \\ n _ {1} x _ {1} + n _ {2} x _ {2} + n _ {3} x _ {3} = c \quad \text {mit} c := a _ {1} n _ {1} + a _ {2} n _ {2} + a _ {3} n _ {3} = \overrightarrow {O A} \cdot \vec {n}. \end{array} \tag {13}
$$

Wird $E$ wie in (12) bzw. (13) durch einen Aufpunkt $A$ und einen Normalenvektor $\vec{n}$ gegeben und ist $P$ ein

beliebiger Raumpunkt, dann stimmt der Lotvektor  $\overrightarrow{PS}$  von P auf E überein mit der Komponente von  $\overrightarrow{PA}$  in Richtung  $\vec{n}$ .

Also gilt (→ §5 (6))

$$
\overrightarrow {P S} = \frac {\overrightarrow {P A} \cdot \vec {n}}{| \vec {n} | ^ {2}} \vec {n}. \tag {14}
$$

Insbesondere ist der

![](../../raw/pages_0033-0064/images/page_54_image_15.jpg)

<details>
<summary>text_image</summary>

P
S
d
P
n
</details>

Abb. 36 - Der Abstand P von E

(15)

Abstand des Punktes P von der Ebene E

$$
d = | \overrightarrow {P S} | = \frac {| \overrightarrow {P A} \cdot \vec {n} |}{| \vec {n} |}.
$$

Ist $|\vec{n}| = 1$, so gibt bereits $d = |\overrightarrow{PA} \cdot \vec{n}|$ den Abstand von $P$ und $E$. Man nennt die Darstellung (13) nach O. L. HESSE (1811–1874, 1868 TH München)

HESSE-Normalform der Ebene E

$$
n _ {1} x _ {1} + n _ {2} x _ {2} + n _ {3} x _ {3} = c, \quad \text {wenn} n _ {1} ^ {2} + n _ {2} ^ {2} + n _ {3} ^ {2} = 1 \text {und} c \geq 0.
$$

---

40

1. Zahlen und Vektoren

Man gelangt von einer beliebigen Koordinatendarstellung (13) von $E$ nach Division durch $\pm\sqrt{n_{1}^{2}+n_{2}^{2}+n_{3}^{2}}$ zur HESSE-Normalform.

Ist  $n_{1}x_{1} + n_{2}x_{2} + n_{3}x_{3} = c$  in HESSE-Normalform, so gilt:

1. Der Normalenvektor  $\vec{n}=n_{1}\vec{e}_{1}+n_{2}\vec{e}_{2}+n_{3}\vec{e}_{3}$  weist, wird er in einem Punkt von E angetragen, vom Nullpunkt weg.
2. Es ist $c$ der Abstand des Nullpunkts von $E$.
3. Ein beliebiger Punkt $P$ hat von $E$ den Abstand $d = |c - \overrightarrow{OP} \cdot \vec{n}|$.
4. Falls $O \notin E$, gilt

$$
c - \overrightarrow {O P} \cdot \vec {n} > 0 \iff O, P \text {liegen auf derselben Seite von} E,
$$

$$
c - \overrightarrow {O P} \cdot \vec {n} <   0 \iff E \text {trennt} O \text {und} P.
$$

Beweis. Formel (14) mit $P = O$ zeigt $\overrightarrow{OS} = (\overrightarrow{OA} \cdot \vec{n})\vec{n} = c\vec{n}$, woraus man sofort 1. und 2. abliest. Die anderen beiden Behauptungen ergeben sich ebenfalls aus (14) ($\rightarrow$ Abb. 36): $\overrightarrow{PS} = [(\overrightarrow{OA} - \overrightarrow{OP}) \cdot \vec{n}] \vec{n} = (c - \overrightarrow{OP} \cdot \vec{n}) \cdot \vec{n}$.

Bringt man die Koordinatendarstellung (13) einer nicht durch den Nullpunkt gehenden Ebene auf die Form

$$
a _ {1} x _ {1} + a _ {2} x _ {2} + a _ {3} x _ {3} = 1 \quad (A c h s e n a b s c h n i t t s f o r m),
$$

so kann man daraus sofort die „Achsenabschnitte“ (d.h. die Durchstoßpunkte der Achsen durch $E$, $\rightarrow$ Abb. 37) ablesen:

$$
A _ {1} = (\frac {1}{a _ {1}}, 0, 0),
$$

$$
A _ {2} = (0, \frac {1}{a _ {2}}, 0),
$$

$$
A _ {3} = (0, 0, \frac {1}{a _ {3}}),
$$

sofern alle  $a_{i} \neq 0$ . Im Fall  $a_{1} = 0$  ist E parallel zur  $x_{1}$ -Achse;
entsprechendes gilt für  $a_{2} = 0$ ,  $a_{3} = 0$

![](../../raw/pages_0033-0064/images/page_55_image_19.jpg)

<details>
<summary>text_image</summary>

A₃
A₂
A₁
</details>

Abb. 37 - Die Achsenabschnitte von $E$

Schließlich sei noch bemerkt, daß man aus einer (beliebigen) Koordinatendarstellung $n_{1}x_{1} + n_{2}x_{2} + n_{3}x_{3} = c$ der Ebene $E$ leicht eine Parameterdarstellung findet. Ist etwa $n_{3} \neq 0$, dann kann man $x_{1} = t$, $x_{2} = s$ (beliebig aus $\mathbb{R}$) wählen und $x_{3}$ aus $x_{3} = \frac{1}{n_{3}}(c - n_{1}t - n_{2}s)$ berechnen. Das ergibt bereits die Parameterdarstellung

$$
\left( \begin{array}{c} x _ {1} \\ x _ {2} \\ x _ {3} \end{array} \right) = \left( \begin{array}{c} 0 \\ 0 \\ \frac {c}{n _ {3}} \end{array} \right) + t \left( \begin{array}{c} 1 \\ 0 \\ - \frac {n _ {1}}{n _ {3}} \end{array} \right) + s \left( \begin{array}{c} 0 \\ 1 \\ - \frac {n _ {2}}{n _ {3}} \end{array} \right)
$$

---

§6. Geraden und Ebenen

41

der Ebene; sie enthält den Aufpunkt $A = (0,0,\frac{c}{n_3})$ und die Richtungsvektoren $\vec{u} = \vec{e}_1 - \frac{n_1}{n_3}\vec{e}_3$, $\vec{v} = \vec{e}_2 - \frac{n_2}{n_3}\vec{e}_3$.

Beispiel. Gegeben sei $E$ durch $3x_{1} - 5x_{2} + \sqrt{2} x_{3} = -5$.

Die HESSESche Normalform hiervon ist  $-\frac{1}{2}x_{1}+\frac{5}{6}x_{2}-\frac{\sqrt{2}}{6}x_{3}=\frac{5}{6}$ .

Der Abstand des Ursprungs von $E$ beträgt $\frac{5}{6}$. Der Punkt $P = (4, 5, 6)$ hat von $E$ den Abstand $|d|$ mit $d = c - \overrightarrow{OP} \cdot \vec{n} = \frac{5}{6} - (-\frac{4}{2} + \frac{25}{6} - \frac{6\sqrt{2}}{6}) = 0.08088 \ldots$. Weil $d > 0$, liegen $O$ und $P$ auf derselben Seite von $E$. Ferner ist $x_1 = t$, $x_2 = s$, $x_3 = \frac{1}{2}\sqrt{2}(-5 - 3t + 5s) \quad (s, t \in \mathbb{R})$ eine Parameterdarstellung von $E$; diese liefert den Aufpunkt $A = (0, 0, -\frac{5}{2}\sqrt{2})$ und die Richtungsvektoren

$$
\vec {u} = \left( \begin{array}{c} 1 \\ 0 \\ - \frac {3}{2} \sqrt {2} \end{array} \right), \vec {v} = \left( \begin{array}{c} 0 \\ 1 \\ \frac {5}{2} \sqrt {2} \end{array} \right).
$$

6.8 Die Gerade als Schnitt zweier Ebenen. Eine Gerade g kann man auffassen als Schnittgerade zweier nicht paralleler Ebenen

$$
E _ {1}: \quad n _ {1} x _ {1} + n _ {2} x _ {2} + n _ {3} x _ {3} = c _ {1},
$$

$$
E _ {2}: \quad m _ {1} x _ {1} + m _ {2} x _ {2} + m _ {3} x _ {3} = c _ {2}.
$$

Das Vektorprodukt der beiden Normalenvektoren $\vec{n}=\sum n_{i}\vec{e}_{i},\quad\vec{m}=\sum m_{i}\vec{e}_{i}$ ist parallel zu beiden Ebenen, zeigt also in Richtung der Schnittgeraden. Kennt man einen Punkt $A$ auf $g$, dann besitzt man sofort mit

$$
\overrightarrow {O X} = \overrightarrow {O A} + t (\vec {n} \times \vec {m})
$$

eine Parameterdarstellung der Schnittgeraden $g$.

Man beachte, daß sowohl (5) als auch die sich aus (6) durch Komponentenvergleich ergebenden Gleichungen – nach Umformung – die Gerade g als Schnittgerade von Ebenen beschreiben.

6.9 Die Winkel zwischen zwei Ebenen und zwischen einer Ebene und einer Geraden. Die Winkel zwischen zwei sich schneidenden Ebenen stimmen überein mit den beiden Winkeln, welche die dazu senkrecht verlaufenden Normalenrichtungen einschließen. Sind also  $\vec{n}_{1}$ ,  $\vec{n}_{2}$  Normalenvektoren der Ebenen  $E_{1}$ ,  $E_{2}$ , dann sind  $\varphi_{1}$ , eindeutig bestimmt durch

$$
\cos \varphi_ {1} = \frac {| \vec {n} _ {1} \cdot \vec {n} _ {2} |}{| \vec {n} _ {1} | | \vec {n} _ {2} |}, \quad 0 \leq \varphi_ {1} \leq \frac {\pi}{2}, \tag {16}
$$

und $\varphi_{2}=\pi-\varphi_{1}$ die beiden (positiv gemessenen) Winkel zwischen $E_{1}$ und $E_{2}$. In der Regel wird nur $\varphi_{1}$ als „der Winkel zwischen $E_{1}$ und $E_{2}$“ bezeichnet.

---

42

1. Zahlen und Vektoren

Als Winkel zwischen einer Geraden g in Richtung $\vec{c}$ und einer Ebene E mit Normalenvektor $\vec{n}$ bezeichnet man den Winkel zwischen $\vec{c}$ und der zu $\vec{n}$ orthogonalen Komponente $\frac{1}{|\vec{n}|^2}\vec{n} \times (\vec{c} \times \vec{n})$ ($\rightarrow$ §5 (12)) von $\vec{c}$. Für diesen Winkel $\varphi$ gilt (Skizze!) $\varphi = \frac{\pi}{2} - \star (\vec{c}, \vec{n})$ und somit ($\rightarrow$ Kap. 2, §3 (4))

![](../../raw/pages_0033-0064/images/page_57_image_3.jpg)

<details>
<summary>text_image</summary>

n
φ
g
</details>

Abb. 38 - Winkel Gerade-Ebene

(17)

Winkel zwischen Gerade und Ebene

$$
\sin \varphi = \frac {| \vec {n} \cdot \vec {c} |}{| \vec {n} | \cdot | \vec {c} |}.
$$

Beispiel 1. Sphärische Trigonometrie. Auf der Einheitskugel $\{X;|\overrightarrow{OX}|=1\}$ im Raum sind durch drei Punkte $A$, $B$, $C$ mit den Ortsvektoren $\vec{a}$, $\vec{b}$, $\vec{c}$ die drei Ecken eines sphärischen Dreiecks gegeben.

Die Seiten $a, b, c$ des Dreiecks sind diejenigen Großkreisbögen $BC, CA, AB$, für die $0 \leq a, b, c \leq \pi$ erfüllt ist. Daher gilt

(18)

$$
\cos a = \vec {b} \cdot \vec {c}, \quad \cos b = \vec {c} \cdot \vec {a}, \quad \cos c = \vec {a} \cdot \vec {b},
$$

$$
\sin a = | \vec {b} \times \vec {c} |, \quad \sin b = | \vec {c} \times \vec {a} |, \quad \sin c = | \vec {a} \times \vec {b} |.
$$

Die Winkel $\alpha, \beta, \gamma$ des Dreiecks sind als Schnittwinkel der Großkreisebenen durch $a, b, c$ bestimmt,

$$
\alpha = \nmid (O A B, O A C), \quad \beta = \nmid (O B C, O B A), \quad \gamma = \nmid (O C A, O C B),
$$

daher ergibt sich mit der LAGRANGE-Identität (→ §5, (11b)) aus (16):

$$
\cos \alpha = \frac {(\vec {a} \times \vec {b}) \cdot (\vec {a} \times \vec {c})}{| \vec {a} \times \vec {b} | \cdot | \vec {a} \times \vec {c} |} = \frac {(\vec {a} \cdot \vec {a}) (\vec {b} \cdot \vec {c}) - (\vec {b} \cdot \vec {a}) (\vec {a} \cdot \vec {c})}{| \vec {a} \times \vec {b} |   | \vec {a} \times \vec {c} |} .
$$

![](../../raw/pages_0033-0064/images/page_57_image_17.jpg)

<details>
<summary>text_image</summary>

C
a
b
Q
c
A
B
</details>

![](../../raw/pages_0033-0064/images/page_57_image_18.jpg)

<details>
<summary>text_image</summary>

O
b
a
c
ā
α
A
B
C
b'
β
r
</details>

Abb. 39 – Sphärische Dreiecke

---

§6. Geraden und Ebenen

43

Setzt man  $\vec{a} \cdot \vec{a} = 1$  und (18) ein, so erhält man den

1. Cosinussatz der sphärischen Trigonometrie
 $\cos a = \cos c \cos b + \cos \alpha \sin c \sin b$ .

Analog bestätigt man vektoriell den

2. Cosinussatz der sphärischen Trigonometrie
 $\cos \alpha = -\cos \beta \cos \gamma + \cos a \sin \gamma \sin \beta$ .

und den

Sinussatz der sphärischen Trigonometrie

$$
\frac {\sin a}{\sin \alpha} = \frac {\sin b}{\sin \beta} = \frac {\sin c}{\sin \gamma}
$$

![](../../raw/pages_0033-0064/images/page_58_image_9.jpg)

## Beispiel 2. Grundaufgaben des CAD.

Von der Einheitskugel mit Mittelpunkt (0,0,1) soll ein Schrägriß in der Ebene  $x_{3}=0$  bestimmt werden, indem man parallel zur Richtung  $\vec{e}_{1}+\vec{e}_{2}-2\vec{e}_{3}$  beleuchtet. Die Abbildungsgleichung ergibt sich aus der Parameterdarstellung des Lichtstrahls durch den Punkt  $X=(x,y,z)$ :

![](../../raw/pages_0033-0064/images/page_58_image_12.jpg)

<details>
<summary>text_image</summary>

z
(x,y,z)
y
x
(ξ,η,0)
</details>

Abb. 40 - Schrägriß

$\begin{pmatrix} x_{1} \\ x_{2} \\ x_{3} \end{pmatrix} = \begin{pmatrix} x \\ y \\ z \end{pmatrix} + t \begin{pmatrix} 1 \\ 1 \\ -2 \end{pmatrix}, t \in \mathbb{R}$. Dieser trifft die Ebene $x_{3} = 0$ für $t = \frac{z}{2}$ in dem Bildpunkt mit den Koordinaten $x_{1} = \xi, x_{2} = \eta, x_{3} = 0$, wobei

$$
\xi = x + \frac {z}{2}, \qquad \eta = y + \frac {z}{2}.
$$

Diese beiden Gleichungen stellen eine lineare Abbildung des  $R^{3}$  in den  $R^{2}$  dar ( $\rightarrow$  Kap. 6). Um den Umriß des Schattens zu bestimmen, bringen wir den Projektionsstrahl mit der Kugel  $x^{2} + y^{2} + (z - 1)^{2} = 1$  zum Schnitt

$$
(\xi + t) ^ {2} + (\eta + t) ^ {2} + (- 2 t - 1) ^ {2} = 1
$$

und erhalten eine quadratische Gleichung für t :

$$
6 t ^ {2} + (2 \xi + 2 \eta + 4) t + (\xi^ {2} + \eta^ {2}) = 0.
$$

In Umrißpunkten trifft der Lichtstrahl die Kugel genau in einem Punkt, daher muß in diesen Punkten die Diskriminante  $(2\xi + 2\eta + 4)^{2} - 4 \cdot 6 \cdot (\xi^{2} + \eta^{2})$

---

44

1. Zahlen und Vektoren

verschwinden. Diese Bedingung stellt bereits die Gleichung des Umrisses dar:

$$
5 \xi^ {2} + 5 \eta^ {2} - 2 \xi \eta - 4 \xi - 4 \eta - 4 = 0.
$$

Das ist eine Ellipse mit Mittelpunkt  $\left(\frac{1}{2},\frac{1}{2}\right)$ , deren Achsen um  $45^{\circ}$  gedreht sind und deren Brennpunkt im Nullpunkt liegt (DANDELIN-Kugel). ☐

## Darstellungen und Umrechnungen für Ebenen im Raum

Darstellungen: ( $X = (x, y, z)$  Punkt auf der Ebene,  $\vec{x} := \overrightarrow{OX}$ )

① Parameterdarstellung :

$$
\begin{array}{l} \vec {x} = \vec {a} + t \vec {b} + s \vec {c}, \quad t, s \in \mathbb {R}; \quad \vec {b} \times \vec {c} \neq \vec {0} \\ \vec {a} = \overrightarrow {O A}, A \text {Aufpunkt}; \vec {b}, \vec {c} \text {Richtungsvektoren} \\ \end{array}
$$

![](../../raw/pages_0033-0064/images/page_59_image_9.jpg)

<details>
<summary>text_image</summary>

n
A
x
x₀
O
x
</details>

② Koordinatengleichung :

(a) $ax + by + cz + d = 0$; $(a, b, c) \neq (0, 0, 0)$
b) $\vec{n} \cdot (\vec{x} - \vec{x}_0) = 0$; $\vec{n} \neq \vec{0}$
(c) $\vec{n}_0\cdot \vec{x} = d_0$ ; $|\vec{n}_0| = 1$ , $d_0\geq 0$ (HESSE-Normalform)

## Umrechnung :

$$
\text {①} \rightarrow \text {②}: \left(\begin{array}{c}a\\b\\c\end{array}\right) = \vec {n} = \vec {b} \times \vec {c}; \vec {x} _ {0} = \vec {a}; d = - \vec {n} \cdot \vec {x} _ {0};.
$$

②a → ① : Nach x auflösen, falls $a \neq 0$ (nach y für $b \neq 0$ bzw. nach z für $c \neq 0$) und y, z (x, z bzw. x, y) als Parameter s, t nehmen.
Für die Ebene x - y = 5 z.B.:

$$
\begin{array}{r c l} x - y = 5 & & x = 5 + t \\ y = t & \Rightarrow & y = \quad t \\ z = s & & z = \quad s \end{array} \quad \Rightarrow \quad \vec {x} = \left( \begin{array}{c} 5 \\ 0 \\ 0 \end{array} \right) + t \left( \begin{array}{c} 1 \\ 1 \\ 0 \end{array} \right) + s \left( \begin{array}{c} 0 \\ 0 \\ 1 \end{array} \right)
$$

$$
\textcircled {2 a} \rightarrow \textcircled {2 b}: \vec {n} = \left(\begin{array}{c}a\\b\\c\end{array}\right); \quad \vec {x} _ {0} = \left(\begin{array}{c}- d / a\\0\\0\end{array}\right), \vec {x} _ {0} = \left(\begin{array}{c}0\\- d / b\\0\end{array}\right), \vec {x} _ {0} = \left(\begin{array}{c}0\\0\\- d / c\end{array}\right),
$$

(jeweils für den Fall  $a \neq 0$ ,  $b \neq 0$ ,  $c \neq 0$ )

$$
\textcircled {2 b} \rightarrow \textcircled {2 a}: d = - \vec {n} \cdot \vec {x} _ {0}; \left(\begin{array}{c}a\\b\\c\end{array}\right) = \vec {n}.
$$

$$
\textcircled {2 b} \rightarrow \textcircled {2 c}: d _ {0} = | \vec {n} \cdot \vec {x} _ {0} | / | \vec {n} |; \vec {n} _ {0} = (s g n (\vec {n} \cdot \vec {x} _ {0}) / | \vec {n} |) \cdot \vec {n}.
$$

$$
\text {②a} \rightarrow \text {②c}: d _ {0} = | d | / \sqrt {a ^ {2} + b ^ {2} + c ^ {2}}; \vec {n} _ {0} = (- (\operatorname{sgn} (d)) / \sqrt {a ^ {2} + b ^ {2} + c ^ {2}}) \left(\begin{array}{c}a\\b\\c\end{array}\right).
$$

$$
② \mathrm{c} \rightarrow ② \mathrm{a}: \text {Skalarprodukt explizit ausrechnen - (nicht relevant) .}
$$

$$
② \mathrm{c} \rightarrow ② \mathrm{b}: \vec {n} = \vec {n} _ {0}, \vec {x} _ {0} \text {wie in} ② \mathrm{a} \rightarrow ② \mathrm{b} \text {bestimmen - (nicht relevant) .}
$$

---

§6. Geraden und Ebenen

45

## Darstellungen und Umrechnungen für Geraden im Raum

Darstellungen: ( $X = (x, y, z)$  Punkt auf der Geraden g,  $\vec{x} := \overrightarrow{OX}$ )

① Parameterdarstellung :

$$
\vec {x} = \vec {a} + t \vec {b}, t \in \mathbb {R}; \vec {b} \neq \vec {0}
$$

$\vec{a} = \overrightarrow{OA}, A = (a_{1}, a_{2}, a_{3})$  Aufpunkt ;  $\vec{b}$  Richtungsvektor

② Koordinatengleichungen :

$$
g: \left\{ \begin{array}{l l} \vec {n} _ {1} \cdot \vec {x} = d _ {1} & ; \quad \vec {n} _ {1} \neq \vec {0} \\ \vec {n} _ {2} \cdot \vec {x} = d _ {2} & ; \quad \vec {n} _ {2} \neq \vec {0}, \vec {n} _ {1} \times \vec {n} _ {2} \neq \vec {0} \end{array} \right.
$$

(Darstellung als Schnitt zweier Ebenen)

![](../../raw/pages_0033-0064/images/page_60_image_10.jpg)

<details>
<summary>text_image</summary>

g
k
l₀
0
m
</details>

③ Momentengleichung :

$$
\vec {x} \times \vec {k} = \vec {m}; \vec {k} \neq \vec {0} \text {mit} \vec {k} \cdot \vec {m} = 0
$$

( g ist Wirkungslinie der Kraft  $\vec{k}$  mit Moment  $\vec{m}$  bzgl. O )

oder

$\overrightarrow{PX} \times \vec{k} = \vec{m}_P$ mit Moment $\vec{m}_P = \vec{m} - \overrightarrow{OP} \times \vec{k}$ bzgl. $P$

## Umrechnung:

① → ② : $b_1 \neq 0$, $b_2 \neq 0$ und $b_3 \neq 0 \Rightarrow g: \frac{x - a_1}{b_1} = \frac{y - a_2}{b_2} = \frac{z - a_3}{b_3} (= t)$.

$$
b _ {1} = 0, b _ {2} \neq 0 \text {und} b _ {3} \neq 0 \Rightarrow g: \frac {y - a _ {2}}{b _ {2}} = \frac {z - a _ {3}}{b _ {3}}, x = a _ {1}.
$$

$$
b _ {1} = 0, b _ {2} = 0 \text {und} b _ {3} \neq 0 \Rightarrow g: x = a _ {1}, y = a _ {2}.
$$

(Analog die anderen Möglichkeiten)

② → ① : $\vec{b} = \vec{n}_1 \times \vec{n}_2$. Für $\vec{a}$ setze man in ②

x = 0, falls  $b_{1} \neq 0$ ; y = 0, falls  $b_{2} \neq 0$ ; z = 0, falls  $b_{3} \neq 0$  und löse ② auf nach y, z (x, z bzw. x, y)

$$
g: \left\{ \begin{array}{l} 3 x + 7 y + 9 z - 5 = 0 \\ 2 x + 4 y + 8 z - 6 = 0 \end{array} \right. \Rightarrow \vec {b} = \left( \begin{array}{c} 3 \\ 7 \\ 9 \end{array} \right) \times \left( \begin{array}{c} 2 \\ 4 \\ 8 \end{array} \right) = \left( \begin{array}{c} 2 0 \\ - 6 \\ - 2 \end{array} \right).
$$

$$
b _ {3} \neq 0 \Rightarrow z = 0 \Rightarrow \left\{ \begin{array}{l} 3 x + 7 y = 5 \\ 2 x + 4 y = 6 \end{array} \Rightarrow \vec {a} = \left( \begin{array}{c} 1 1 \\ - 4 \\ 0 \end{array} \right) \right..
$$

① → ③ : $\vec{k} = \vec{b}$; $\vec{m} = \vec{a} \times \vec{b}$.

③ → ① : $\vec{b} = \vec{k}$ ; $\vec{a} = \vec{l}_O$, wobei allg. $\vec{l}_P = \frac{1}{|\vec{k}|^2} (\vec{k} \times \vec{m}_P)$ das Lot von $P$ auf $g$.

② → ③ : $\vec{k} = \vec{n}_1 \times \vec{n}_2$ ; $\vec{m} = d_2\vec{n}_1 - d_1\vec{n}_2$.

( Beachte: $\vec{m} = \vec{x}\times (\vec{n}_1\times \vec{n}_2) = (\vec{x}\cdot \vec{n}_2)\vec{n}_1 - (\vec{x}\cdot \vec{n}_1)\vec{n}_2$ )

③ → ② : Produkt ausschreiben, 2 der 3 skalaren Gleichungen sind nicht vom Typ 0 = 0, sie bestimmen eine Darstellung ② .

$$
\vec {x} \times \left( \begin{array}{c} 1 \\ 2 \\ 3 \end{array} \right) = \left( \begin{array}{c} - 1 \\ - 1 \\ 1 \end{array} \right) \Rightarrow \left( \begin{array}{c} 3 y - 2 z \\ z - 3 x \\ 2 x - y \end{array} \right) = \left( \begin{array}{c} - 1 \\ - 1 \\ 1 \end{array} \right) \Rightarrow g: \left\{ \begin{array}{l} 3 y - 2 z + 1 = 0 \\ z - 3 x + 1 = 0 \end{array} . \right.
$$

---

46

1. Zahlen und Vektoren

## Aufgaben

1. Die kartesischen Koordinaten der Ecken eines Tetraeders $\Delta$ im $\mathbb{R}^3$ seien

$$
A _ {1} = (1, 1, 1), A _ {2} = (1, - 1, - 1), A _ {3} = (- 1, - 1, 1), A _ {4} = (- 1, 1, - 1).
$$

Man bestimme

a) das Volumen des Tetraeders $\Delta$,
b) eine Parameterdarstellung der Höhe durch  $A_{4}$ ,
c) eine Gleichung für die Ebene $E$ durch $A_{1}, A_{2}, A_{3}$,
d) das gemeinsame Lot und den Abstand der Kanten $\overline{A_{1}A_{2}}$, $\overline{A_{3}A_{4}}$.

![](../../raw/pages_0033-0064/images/page_61_image_11.jpg)

<details>
<summary>text_image</summary>

A₁
A₂
A₃
A₄
a
b
c
</details>

2. Man bestimme das gemeinsame Lot und den kürzesten Abstand der beiden Geraden im  $R^{3}$ :

$$
\vec {x} \times \left( \begin{array}{c} 0 \\ 0 \\ 1 \end{array} \right) = \left( \begin{array}{c} 2 \\ - 2 \\ 0 \end{array} \right) \quad \text {und} \quad \vec {x} = t \left( \begin{array}{c} 2 \\ - 1 \\ 2 \end{array} \right), t \in \mathbb {R}.
$$

3. Im  $R^{3}$  sind die Ebene E : x = y und die Gerade g : 10 - 2x = -5y = 10z gegeben.

- Man bestimme eine Parameterdarstellung für $E$.
- Unter welchem Winkel trifft die Gerade g auf die Ebene E ?

4. Im $\mathbb{R}^3$ sollen sich die beiden Geraden $g_1$ und $g_2$ schneiden:

$$
g _ {1} : x - 1 = \frac {y + 1}{2} = - \frac {z + 1}{\lambda}; \quad g _ {2} : x + 2 = y - 1 = z.
$$

a) Wie groß muß λ sein ?
b) Welche Koordinaten hat der Schnittpunkt ?
c) In welcher Ebene liegen $g_{1}$ und $g_{2}$?
d) Wie groß ist der Schnittwinkel zwischen  $g_{1}$  und  $g_{2}$ ?

5. Gesucht ist die Gerade im Raum, die durch den Punkt O geht und mit den drei Ebenen

$$
3 x - 4 y = 0, \quad y = 0, \quad z = 0
$$

gleiche Winkel einschließt. Wie groß ist dieser Winkel ?

6. Die Gerade $g_1$ trifft die Punkte $(1, -1, 1)$ und $(-1, -1, -1)$, die Gerade $g_2$ geht durch $(-1, 1, 1)$ und $(1, 1, -1)$. Man berechne die Schnittpunkte mit der Ebene $x_3 = c$ und deren Verbindungsgerade $g_c$. Man bestätige, daß jede dieser Geraden $g_c$ auf der Fläche $F : x_1 + x_2x_3 = 0$ liegt. Auf $F$ liegt eine zweite Geradenschar, welche?

![](../../raw/pages_0033-0064/images/page_61_image_29.jpg)

<details>
<summary>text_image</summary>

g₁
z
y
x
g₂
</details>

---

§7. Gebundene Vektoren

47

7. a) Welche Entfernung $a$ auf der Erdkugel haben NEW YORK (41° n.B., 74° w.B.) und LISSABON (38° n.B., 9° w.B.) ?
(Hilfe: Berechne die Ortsvektoren von NY und L im skizzierten Ko-ordinatensystem mit Erdradius R = 6367 km)
b) Unter welchem Winkel γ schneidet der Großkreisbogen von New York nach Lissabon den Meridian in New York?

![](../../raw/pages_0033-0064/images/page_62_image_6.jpg)

<details>
<summary>text_image</summary>

z
N
δ
a
NY
L
38°
41°
65°
x
y
</details>

8. Man bestimme den Schattenriß des Würfels $\{(x,y,z)\in\mathbb{R}^{3}\mid x|\leq1,|y|\leq1,0\leq z\leq2\}$ unter der Projektion (18) ($\rightarrow$ Abb. 40).

## §7. Gebundene Vektoren

\* 7.1 Gebundene Vektoren. Die bisher betrachteten Vektoren sind „frei“ in dem Sinne, daß sie im ganzen Raum parallel verschiebbar sind; in der Mechanik beschreibt man damit räumlich homogene Kräfte und Momente. Zur Darstellung von „Einzelkräften“, die punktförmig an einem starren Körper angreifen und nur längs ihrer Wirkungslinie verschoben werden dürfen, benötigt man den Begriff des – an eine Gerade – gebundenen Vektors im Raum:

Definition. Unter einem gebundenen Vektor versteht man ein Paar  $(\vec{k}, g)$  mit einem freien Vektor  $\vec{k}$  und einer Geraden g, die -falls  $\vec{k} \neq \vec{0}$  - in Richtung  $\vec{k}$  verläuft. Der Nullvektor  $\vec{k} = \vec{0}$  zusammen mit einer beliebigen Geraden heißt gebundener Nullvektor.

Im Hinblick auf die ausschließliche Anwendung in der Mechanik nennen wir  $\vec{k}$  Kraftvektor, g Wirkungslinie und jeden Punkt A der Geraden g Angriffspunkt des gebundenen Vektors. Ist P ein beliebiger Punkt des Raumes und A ein Angriffspunkt, so heißt

![](../../raw/pages_0033-0064/images/page_62_image_12.jpg)

<details>
<summary>text_image</summary>

P
A
k
m
g
</details>

Abb. 41 - Gebundener Vektor

$$
\vec {m} _ {P} := \overrightarrow {P A} \times \vec {k} \tag {1}
$$

das Moment des gebundenen Vektors im Punkt P. Die Momentengleichung der Wirkungslinie lautet (→ 6.3)

$$
\overrightarrow {P X} \times \vec {k} = \vec {m} _ {p}.
$$

---

48

1. Zahlen und Vektoren

## Definition.

1. Als Wirkung des gebundenen Vektors im Punkt $P$ definieren wir das geordnete Paar „freier“ Vektoren $(\vec{k},\vec{m}_{P})$.
2. Zwei gebundene Vektoren sind gleich, wenn es einen Punkt P gibt, in dem sie die gleiche Wirkung, d.h. den gleichen Kraftvektor und das gleiche Moment besitzen.

Kennt man die Wirkung  $(\vec{k},\vec{m}_{P})$  im Punkt P, so erhält man die Wirkung in einem beliebigen anderen Punkt Q durch

$$
(\vec {k}, \vec {m} _ {Q}) = (\vec {k}, \vec {m} _ {P} - \overrightarrow {P Q} \times \vec {k}). \tag {2}
$$

Beweis. Ist A ein Angriffspunkt des gebundenen Vektors, so gilt

$$
\vec {m} _ {Q} = \overrightarrow {Q A} \times \vec {k} = (\overrightarrow {P A} - \overrightarrow {P Q}) \times \vec {k} = \vec {m} _ {P} - \overrightarrow {P Q} \times \vec {k}.
$$

Beispiel. Der Kraftvektor $\vec{k} = \begin{pmatrix} 1 \\ -1 \\ 1 \end{pmatrix}$ greife im Punkt $A = (0,1,2)$ an; dann ist seine Wirkung im Punkt $O = (0,0,0)$:

$$
\left(\binom{1}{- 1}, \binom{0}{1} \times \binom{1}{- 1}\right) = \left(\binom{1}{- 1}, \binom{3}{2} _ {- 1}\right).
$$

Für die Wirkung im Punkt  $P = (-1, -1, -1)$  ergibt sich

$$
\left(\left( \begin{array}{c} 1 \\ - 1 \\ 1 \end{array} \right), \left( \begin{array}{c} 3 \\ 2 \\ - 1 \end{array} \right) - \left( \begin{array}{c} - 1 \\ - 1 \\ - 1 \end{array} \right) \times \left( \begin{array}{c} 1 \\ - 1 \\ 1 \end{array} \right)\right) = \left(\left( \begin{array}{c} 1 \\ - 1 \\ 1 \end{array} \right), \left( \begin{array}{c} 5 \\ 2 \\ - 3 \end{array} \right)\right).
$$

\* 7.2 Ein System gebundener Vektoren ist eine endliche Menge gebundener Vektoren. In der Mechanik beschreibt man damit in der Regel ein System von Einzelkräften, die an einem starren Körper angreifen (Kraftsystem).

## Definition.

1. Ein System von zwei gebundenen Vektoren heißt Vektorwinder.
2. Besteht das System aus n gebundenen Vektoren und sind  $(\vec{k}_{1},\vec{m}_{1P})$ , ...,  $(\vec{k}_{n},\vec{m}_{nP})$  deren Wirkungen im Punkt P, so ist nach dem Superpositionsprinzip die Wirkung des Systems im Punkt P das Vektorpaar

$$
(\vec {k}, \vec {m} _ {P}) := (\sum_ {i = 1} ^ {n} \vec {k} _ {i}, \sum_ {i = 1} ^ {n} \vec {m} _ {i P}). \tag {3}
$$

$\vec{k}$ heißt resultierender Kraftvektor, $\vec{m}_{P}$ Moment des Systems im Punkt P. Die Addition von Wirkungen in einem Punkt P ist erklärt durch

$$
(\vec {k} _ {1}, \vec {m} _ {1 P}) + (\vec {k} _ {2}, \vec {m} _ {2 P}) := (\vec {k} _ {1} + \vec {k} _ {2}, \vec {m} _ {1 P} + \vec {m} _ {2 P}).
$$

---

§7. Gebundene Vektoren

49

3. Zwei Systeme von gebundenen Vektoren heißen äquivalent, wenn es einen Punkt P gibt, in welchem beide Systeme die gleiche Wirkung besitzen.

Für die Wirkung des Systems in einem anderen Punkt $Q$ erhält man mit (2) und §5(8c) sofort

$$
(\vec {k}, \vec {m} _ {Q}) = (\vec {k}, \vec {m} _ {P} - \overrightarrow {P Q} \times \vec {k}). \tag {4}
$$

Satz 7.1. Zwei Systeme von gebundenen Vektoren sind genau dann äquivalent, wenn sie in jedem Punkt P jeweils das gleiche Moment besitzen.

Beweis. Seien  $(\vec{k},\vec{m}_{P})$  und  $(\vec{k}^{\prime},\vec{m}_{P}^{\prime})$  die Wirkungen der Systeme im Punkt P, dann folgt aus  $\vec{k}=\vec{k}^{\prime}$  und  $\vec{m}_{P}=\vec{m}_{P}^{\prime}$  für einen beliebigen Punkt Q

$$
\vec {m} _ {Q} = \vec {m} _ {P} - \overrightarrow {P Q} \times \vec {k} = \vec {m} _ {P} ^ {\prime} - \overrightarrow {P Q} \times \vec {k} ^ {\prime} = \vec {m} _ {Q} ^ {\prime}.
$$

Umgekehrt folgt aus $\vec{m}_{Q}=\vec{m}_{Q}^{\prime}$ für jeden Punkt $Q$ sofort $\vec{m}_{P}=\vec{m}_{P}^{\prime}$ und damit $\overrightarrow{PQ}\times(\vec{k}-\vec{k}^{\prime})=\vec{0}$. Dies ist für beliebiges $\overrightarrow{PQ}$ nur möglich, falls $\vec{k}=\vec{k}^{\prime}$. □

Satz 7.2. Jedes System von gebundenen Vektoren ist äquivalent zu einem Vektorwinder.

Beweis. Sei P ein beliebiger Punkt, dann stellt  $(\vec{k},\vec{m}_{P})$  nur dann die Wirkung eines gebundenen Vektors dar, wenn

$$
\vec {k} \cdot \vec {m} _ {P} = 0 \quad \text {und} \quad (\vec {k} = \vec {0} \Rightarrow \vec {m} _ {P} = \vec {0}). \tag {5}
$$

Für die Wirkung eines Kraftsystems ist (5) im allg. nicht erfüllt, daher zerlegen wir die Wirkung

$$
(\vec {k}, \vec {m} _ {P}) = (\vec {l}, \vec {m} _ {P}) + (\vec {k} - \vec {l}, \vec {0}), \tag {6}
$$

wobei $\vec{l} \neq \vec{0}$ senkrecht zu $\vec{m}_{P}$ aber sonst beliebig gewählt ist. $(\vec{k} - \vec{l}, \vec{0})$ ist Wirkung eines gebundenen Vektors mit Angriffspunkt $P$.

Definition. Ein Vektorwinder mit der Wirkung  $(\vec{0},\vec{m}_{P})$  im Punkt P heißt freies Moment.

Aus der Zerlegung

$$
(\vec {0}, \vec {m} _ {P}) = (\vec {l}, \vec {m} _ {P}) + (- \vec {l}, \vec {0})
$$

mit  $\vec{l} \neq \vec{0}$  und  $\vec{l} \cdot \vec{m}_{P} = 0$  erkennt man, daß ein freies Moment stets einem Paar von gebundenen Vektoren äquivalent ist, deren Kraftvektoren gleichen Betrag und entgegengesetzte Richtung besitzen (Kräftepaar). Die Bezeichnung „frei“ rechtfertigt

Satz 7.3. Ein freies Moment hat in jedem Punkt die gleiche Wirkung.

---

50

1. Zahlen und Vektoren

Beweis. Wegen $\vec{k} = \vec{0}$ ist $\overrightarrow{QP} \times \vec{k} = \vec{0}$, d.h. mit (4) ist $\vec{m}_Q = \vec{m}_P$ für alle Punkte $Q$.

## \* 7.3 Die Reduktion eines Systems gebundener Vektoren.

(a) Reduktion im Punkt $P$: Die Darstellung (6) eines Vektorwinders ist nicht eindeutig, daher bevorzugt man in der Mechanik eine eindeutiger Zerlegung der Wirkung in $P$

$$
(\vec {k}, \vec {m} _ {P}) = (\vec {k}, \vec {0}) + (\vec {0}, \vec {m} _ {P}). \tag {7}
$$

Ist $(\vec{k},\vec{m}_{P})$ die Wirkung eines Systems gebundener Vektoren in $P$ so heißt (7) Reduktion des Systems in $P$. Für ein Kraftsystem ist $(\vec{k},\vec{0})$ die Wirkung der resultierenden Kraft mit Angriffspunkt $P$, $(\vec{0},\vec{m}_{P})$ das resultierende Moment in $P$. Äquivalente Systeme besitzen in jedem Punkt des Raumes jeweils die gleiche Reduktion.

⑥ Reduktion zur Vektorschraube. Hat ein System gebundener Vektoren in einem Punkt A die Wirkung  $(\vec{k},\vec{m}_{A})$  mit  $\vec{k}\neq\vec{0}$  und  $\vec{m}_{A}=p\vec{k}$ , so sagt man, das System wirkt in A als Vektorschraube mit Steigungsparameter p.

Satz 7.4. Ein System gebundener Vektoren, das in einem (beliebigen) Punkt P die Wirkung $(\vec{k},\vec{m}_{P})$ mit $\vec{k}\neq \vec{0}$ besitzt, wirkt in jedem Punkt der Geraden

$$
g: \quad \overrightarrow {P X} = \frac {1}{| \vec {k} | ^ {2}} \vec {k} \times \vec {m} _ {P} + t \vec {k}, \quad t \in \mathbb {R} \tag {8}
$$

als Vektorschraube mit dem Steigungsparameter

$$
p = \frac {1}{| \vec {k} | ^ {2}} \vec {k} \cdot \vec {m} _ {P}.
$$

Man nennt g die Achse des Systems, sie ist eindeutig bestimmt.

Beweis. Wir zerlegen $\vec{m}_{P}$ orthogonal längs $\vec{k}$ ($\rightarrow$ §5 (6)),

$$
\vec {m} _ {P} = \vec {m} _ {\vec {k}} + \vec {m} _ {\vec {n}} \quad \text {mit} \quad \vec {m} _ {\vec {k}} = \frac {\vec {k} \cdot \vec {m} _ {P}}{| \vec {k} | ^ {2}} \vec {k}. \tag {9}
$$

Das Moment in einem Punkt A besitzt gemäß (4) die Zerlegung

$$
\vec {m} _ {A} = \vec {m} _ {P} - \overrightarrow {P A} \times \vec {k} = \vec {m} _ {\vec {k}} + (\vec {m} _ {\vec {n}} - \overrightarrow {P A} \times \vec {k}),
$$

woraus man einerseits ersieht, daß $\vec{m}_{\vec{k}}$ unabhängig ist von $P$ und andererseits, daß $\vec{m}_A$ genau dann parallel ist zu $\vec{k}$, wenn $A$ auf der Geraden $\overrightarrow{PX} \times \vec{k} = \vec{m}_{\vec{n}}$ liegt. Wegen $\vec{k} \times \vec{m}_{\vec{n}} = \vec{k} \times \vec{m}_P$ besitzt diese (eindeutig bestimmte) Gerade $g$ die angegebene Parameterdarstellung ($\rightarrow$ 6.3). Für jeden Punkt $A$ auf $g$ gilt $\vec{m}_A = \vec{m}_{\vec{k}} = p\vec{k}$ mit $p = \frac{\vec{k} \cdot \vec{m}_P}{|\vec{k}|^2}$ ($\rightarrow$ Abb. 42a).

---

§7. Gebundene Vektoren

51

Die Reduktion eines Systems gebundener Vektoren zur Vektorschraube:

1. Schritt: Wahl eines Bezugspunktes $P$.
2. Schritt: Berechnung der Wirkungen  $(\vec{k}_{i},\vec{m}_{iP})$  in P mit (1).
3. Schritt: Berechnung der Wirkung des Systems in $P$ mit (3).
4. Schritt: Ist  $\vec{k} = \vec{0}$ , so ist das System äquivalent zu einem freien Moment.
Falls $\vec{k} \neq \vec{0}$, dann wirkt das System in jedem Punkt der Achse (8) als Vektorschraube mit Steigungsparameter $p = \frac{1}{|\vec{k}|^2} \vec{k} \cdot \vec{m}_P$. Mit (9) gilt

$$
(\vec {k}, \vec {m} _ {P}) = (\vec {k}, \vec {m} _ {\vec {n}}) + (\vec {0}, \vec {m} _ {\vec {k}}).
$$

![](../../raw/pages_0065-0096/images/page_66_image_10.jpg)

<details>
<summary>text_image</summary>

L
A
g
1/|k-1|^2 k × m_P
P
m_P
m_n
m_k
k
</details>

Abb. 42a - Vektorschraube

![](../../raw/pages_0065-0096/images/page_66_image_12.jpg)

<details>
<summary>text_image</summary>

z
mₖ
L
M₁
M₂
k₁
Q₁
Q₂
x
y
k
k₂
</details>

Abb. 42b - Reduktion eines Kraftsystems

Beispiel. Gegeben ist das System zweier gebundener Vektoren mit Kraftvektoren $\vec{k}_{1}=\begin{pmatrix}2\\0\\0\end{pmatrix},\vec{k}_{2}=\begin{pmatrix}0\\0\\-2\end{pmatrix}$ und den Angriffspunkten $Q_{1}=(0,-1,0)$, $Q_{2}=(1,0,0)$ ($\rightarrow$ Abb. 42b). Im Punkt $O=(0,0,0)$ sind die Wirkungen

$$
\begin{array}{l} \left(\left( \begin{array}{c} 2 \\ 0 \\ 0 \end{array} \right), \left( \begin{array}{c} 0 \\ - 1 \\ 0 \end{array} \right) \times \left( \begin{array}{c} 2 \\ 0 \\ 0 \end{array} \right)\right) = \left(\left( \begin{array}{c} 2 \\ 0 \\ 0 \end{array} \right), \left( \begin{array}{c} 0 \\ 0 \\ 2 \end{array} \right)\right) , \\ \left(\left( \begin{array}{c} 0 \\ 0 \\ - 2 \end{array} \right), \left( \begin{array}{c} 1 \\ 0 \\ 0 \end{array} \right) \times \left( \begin{array}{c} 0 \\ 0 \\ - 2 \end{array} \right)\right) = \left(\left( \begin{array}{c} 0 \\ 0 \\ - 2 \end{array} \right), \left( \begin{array}{c} 0 \\ 2 \\ 0 \end{array} \right)\right) . \\ \end{array}
$$

---

52

1. Zahlen und Vektoren

Das System hat in O die Wirkung

$$
\left(\left( \begin{array}{c} 2 \\ 0 \\ 0 \end{array} \right) + \left( \begin{array}{c} 0 \\ 0 \\ - 2 \end{array} \right), \left( \begin{array}{c} 0 \\ 0 \\ 2 \end{array} \right) + \left( \begin{array}{c} 0 \\ 2 \\ 0 \end{array} \right)\right) = \left(\left( \begin{array}{c} 2 \\ 0 \\ - 2 \end{array} \right), \left( \begin{array}{c} 0 \\ 2 \\ 2 \end{array} \right)\right).
$$

Mit $\vec{m}_{\vec{k}} = \frac{-4}{8}\left( \begin{array}{c}2\\ 0\\ -2 \end{array} \right) = \left( \begin{array}{c} - 1\\ 0\\ 1 \end{array} \right)$ lautet die Reduktion zur Vektorschraube

$$
(\vec {\mathbf {k}}, \vec {\mathbf {m}} _ {\mathrm{P}}) = \left(\left( \begin{array}{c} 2 \\ 0 \\ - 2 \end{array} \right), \left( \begin{array}{c} 1 \\ 2 \\ 1 \end{array} \right)\right) + \left(\vec {0}, \left( \begin{array}{c} - 1 \\ 0 \\ 1 \end{array} \right)\right) .
$$

Der Lotvektor von $O$ auf die Achse ist $\frac{1}{8}\begin{pmatrix}2\\ 0\\ -2\end{pmatrix}\times\begin{pmatrix}1\\ 2\\ 1\end{pmatrix}=\begin{pmatrix}1/2\\ -1/2\\ 1/2\end{pmatrix}$, die Parameterdarstellung der Achse ist

$$
\overrightarrow {O A} = \left( \begin{array}{c} 1 / 2 \\ - 1 / 2 \\ 1 / 2 \end{array} \right) + \mathfrak {t} \left( \begin{array}{c} 2 \\ 0 \\ - 2 \end{array} \right), \quad \mathfrak {t} \in \mathbb {R}.
$$

Der Steigungsparameter ist  $p = \frac{-4}{8} = -\frac{1}{2} < 0$ , daher liegt eine Linksschraube vor.

## Aufgaben

1. In den Ecken  $P_{1} = (0,0,2)$ ,  $P_{2} = (0,1,0)$ ,  $P_{3} = (-1,0,0)$  einer dreieckigen Platte wirken in Abhängigkeit von  $\alpha$  die Einzelkräfte

$$
\vec {k} _ {1} = \left( \begin{array}{c} \alpha \\ - \alpha \\ 1 \end{array} \right), \quad \vec {k} _ {2} = \left( \begin{array}{c} \alpha \\ \alpha \\ - 1 \end{array} \right), \quad \vec {k} _ {3} = \left( \begin{array}{c} \alpha \\ \alpha \\ 1 \end{array} \right).
$$

![](../../raw/pages_0065-0096/images/page_67_image_12.jpg)

<details>
<summary>text_image</summary>

k₁
P₁
g₁
k₂
P₂
g₂
k₃
g₃
P₃
</details>

a) Für welche Werte von  $\alpha$  ist das Kraftsystem äquivalent zu einer Einzelkraft, wie lautet diese?
b) Man reduziere das Kraftsystem für jedes $\alpha$ auf eine Vektorschraube. Für welche $\alpha$ ist der Drehsinn positiv?

2. Darstellung eines freien Moments als Hebel. Man rechne nach, daß ein freies Moment mit der Wirkung (0, m) stets äquivalent ist zu einem Kräftepaar mit den Kraftvektoren

$$
\vec {k} _ {1} = \vec {m} \times \vec {e}, \quad \vec {k} _ {2} = - \vec {m} \times \vec {e}
$$

![](../../raw/pages_0065-0096/images/page_67_image_18.jpg)

<details>
<summary>text_image</summary>

m
k₁
O
e
A
k₂
</details>

und den Angriffspunkten $O$ und $A$, wobei $\vec{e} = \overrightarrow{OA}$, $|\vec{e}| = 1$ und $\vec{e} \cdot \vec{m} = 0$.

---

§8. Die komplexen Zahlen

53

## §8. Die komplexen Zahlen

8.1 Die Menge der komplexen Zahlen. In der mit einem kartesischen  $(x,y)$ -Koordinatensystem versehenen Ebene stellen die Punkte der x-Achse die reellen Zahlen dar. Wir gehen dazu über, auch alle anderen Punkte der Ebene als „Zahlen“ aufzufassen. Dazu schreiben wir den Punkt  $z = (x,y)$

(genauer: das den Punkt repräsentierende Zahlenpaar) in der Form

$$
z = x + i y
$$

und nennen ihn eine komplexe Zahl mit Realteil Re z := x und Imaginärteil Im z := y. Die x-Achse heißt reelle Achse, die y-Achse wird imaginäre Achse genannt. Abkürzend schreibt man  $x = x + i0 = (x, 0)$  (das sind die reellen Zahlen auf der reellen Achse) und  $iy = 0 + iy = (0, y)$

![](../../raw/pages_0065-0096/images/page_68_image_7.jpg)

<details>
<summary>text_image</summary>

y
imaginäre Achse
ix
iz=-y+ix
iy
z=x+iy
i
1
x
reelle Achse
x
</details>

Abb. 43 - Komplexe Ebene

(das sind die sogenannten rein imaginären Zahlen auf der imaginären Achse). Die Menge aller komplexen Zahlen wird mit C bezeichnet.

$$
\mathbb {C} := \left\{x + i y; x, y \in \mathbb {R} \right\}.
$$

Zwei komplexe Zahlen  $z = x + iy$  und  $w = u + iv$  (mit  $x, y, u, v \in R$ ) sind genau dann gleich, wenn x = u und y = v gilt. Ist nichts anderes gesagt, so sind in  $z = x + iy$  die Zahlen x, y reell. Es ist üblich, den vom Ursprung O nach z weisenden Zeiger (Ortsvektor) ebenfalls mit z zu bezeichnen. Die Ebene, deren Punkte als komplexe Zahlen aufgefaßt werden, heißt komplexe Zahlenebene.

8.2 Die vier Grundrechenarten in $\mathbb{C}$. Die Summe und die Differenz komplexer Zahlen ist durch

$$
(x + i y) + (u + i v) := (x + u) + i (y + v)
$$

$$
(x + i y) - (u + i v) := (x - u) + i (y - v)
$$

definiert. Sie entspricht der Vektor-Summe bzw. Differenz der zugehörigen Zeiger ( $\rightarrow$  §4).

Die Zahl $ix \in \mathbb{C}$ entsteht aus $x \in \mathbb{R} \subseteq \mathbb{C}$ ($\rightarrow$ Abb. 43) durch eine positive Drehung (gegen Uhrzeigersinn) des zugehörigen Zeigers um den Winkel $\frac{\pi}{2}$. Die Multiplikation in $\mathbb{C}$ wird nun so erklärt, daß generell der Zeiger $i \cdot z$ aus $z$ durch eine positive Drehung um $\frac{\pi}{2}$ hervorgeht. Wenn das überhaupt möglich ist, wird man $i^2 = i \cdot i = -1$ festlegen müssen. Deshalb wird das Produkt zweier

---

54

1. Zahlen und Vektoren

komplexer Zahlen definiert durch

$$
\begin{array}{c} (x + i y) \cdot (u + i v) := (x u - y v) + i (x v + y u), \\ \text {insbesondere} i ^ {2} = - 1. \end{array}
$$

Beachte: Addition, Subtraktion und Multiplikation werden formal wie gewohnt ausgeführt; dabei ist nur $i^{2} = -1$ zu beachten. Die Ergebnisse werden in die Form $a + ib$ ($a, b \in \mathbb{R}$) gebracht. Wegen $i(x + iy) = -y + ix$ stellt $z \mapsto iz$ wie gewünscht die positive Drehung um den Nullpunkt um $\frac{\pi}{2}$ dar ($\rightarrow$ Abb. 43). Die Potenzen $z^{n}$ ($z \in \mathbb{C}$, $n = 0, 1, 2, \ldots$) sind wie üblich durch $z^{0} := 1$, $z^{1} := z$, $z^{n+1} := z^{n}z$ erklärt. Auch in $\mathbb{C}$ gilt die binomische Formel ($\rightarrow$ Satz 2.2)

$$
(z + w) ^ {n} = \sum_ {k = 0} ^ {n} \binom {n} {k} z ^ {k} w ^ {n - k} \quad (n \in \mathbb {N}).
$$

Beispiel. $(3 + 0.5i)(2 - 4i) + (i - 1)^{3} = 6 + i - 12i - 2i^{2} + i^{3} - 3i^{2} + 3i - 1 = 10 - 9i$

Die Division durch $w \in \mathbb{C}$, $w \neq 0$, ist in $\mathbb{C}$ wie folgt erklärt. Man schreibt $q = \frac{z}{w} (= z : w)$, wenn $wq = z$ gilt. Für $z = x + iy$ und $w = u + iv \neq 0$ berechnet man

$$
\frac {x + i y}{u + i v} = \frac {(x + i y) (u - i v)}{(u + i v) (u - i v)} = \frac {x u + y v}{u ^ {2} + v ^ {2}} + \frac {y u - x v}{u ^ {2} + v ^ {2}} i.
$$

Beachte: Durch die Erweiterung mit u - iv wird der Nenner reell.

Beispiele. $\frac{1}{4 - 5i} = \frac{4 + 5i}{(4 - 5i)(4 + 5i)} = \frac{4}{41} +\frac{5}{41} i;$

$$
\frac {8 - i}{7 - i} = \frac {(8 - i) (7 + i)}{4 9 + 1} = \frac {5 7}{5 0} + \frac {1}{5 0} i.
$$

Durch $z^{-n} := \frac{1}{z^n}$ ($z \neq 0, n \in \mathbb{N}$) sind die Potenzen mit negativen Exponenten erklärt. Man verifiziert leicht, daß in $\mathbb{C}$ die üblichen, aus $\mathbb{R}$ bekannten Rechengesetze gelten; etwa $zw = wz$, $z(ws) = (zw)s$, $z(w + s) = zw + zs$, $z^{m+n} = z^m z^n$ ($z \neq 0; m, n \in \mathbb{Z}$) und andere. Auch in $\mathbb{C}$ ist eine Division durch 0 nicht möglich.

## 8.3 Die Konjugation und der Betrag komplexer Zahlen.

Man nennt  $\bar{z}=x-iy$  ( $x,y\in R$ ) die zu  $z=x+iy$  konjugierte komplexe Zahl.

Beispiele.  $\bar{i} = -i, \bar{2} = 2, \overline{4 + 2i} = 4 - 2i, \overline{3 - 2i} = 3 + 2i.$

Für den Übergang $z \mapsto \bar{z}$ zu konjugiert komplexen Zahlen (das ist die Spiegelung an der rellen Achse) gelten die folgenden Rechenregeln:

---

§8. Die komplexen Zahlen

55

$$
\overline {{z + w}} = \overline {{z}} + \overline {{w}}; \overline {{z w}} = \overline {{z}} \overline {{w}}; (\frac {\overline {{z}}}{\overline {{w}}}) = \frac {\overline {{z}}}{\overline {{w}}} \quad (w \neq 0);
$$

$$
\overline {{\bar {z}}} = z; \operatorname{Re} z = \frac {1}{2} (z + \bar {z}); \operatorname{Im} z = \frac {1}{2 i} (z - \bar {z}).
$$

Die Länge des Zeigers  $z = x + iy$  wird mit  $|z|$  bezeichnet und heißt Betrag der komplexen Zahl. Man rechnet leicht nach:

$$
| z | = \sqrt {x ^ {2} + y ^ {2}} = \sqrt {z \bar {z}}, \quad \text {falls} z = x + i y;
$$

$$
| z w | = | z | | w |; \left| \frac {z}{w} \right| = \frac {| z |}{| w |} \quad (w \neq 0); | \bar {z} | = | z |.
$$

Ferner gilt die Dreiecksungleichung  $|z + w| \leq |z| + |w|$ , die sich leicht mit vollständiger Induktion auf n Summanden verallgemeinern läßt.

$$
\left| \sum_ {k = 1} ^ {n} z _ {k} \right| \leq \sum_ {k = 1} ^ {n} \left| z _ {k} \right|. \tag {1}
$$

Beispiele. $|i| = |-i| = 1$; $|2 + 3i| = \sqrt{4 + 9} = \sqrt{13}$;

$$
| (2 + 3 i) (1 + i) | = | 2 + 3 i | | 1 + i | = \sqrt {1 3} \sqrt {2} = \sqrt {2 6}.
$$

8.4 Anwendungen: a Quadratische Gleichungen. Ursprünglich wurden die komplexen Zahlen zur einheitlichen Behandlung der quadratischen Gleichungen

$$
a x ^ {2} + b x + c = 0 \quad (\text {mit} a, b, c \in \mathbb {R}, a \neq 0) \tag {2}
$$

eingeführt. Die Gleichung $x^{2} + 1 = 0$ hat offenbar in $\mathbb{R}$ keine Lösung, wohl aber in $\mathbb{C}$, nämlich $x = \pm \sqrt{-1} = \pm i$, und es gilt $x^{2} + 1 = (x - i)(x + i)$.

Allgemein gilt: Die Gleichung (2) besitzt in C die beiden (nicht notwendig verschiedenen) Lösungen

$$
x _ {1} = - \frac {b}{2 a} + \frac {1}{2 a} \sqrt {b ^ {2} - 4 a c}, \quad x _ {2} = - \frac {b}{2 a} - \frac {1}{2 a} \sqrt {b ^ {2} - 4 a c}, \tag {3}
$$

wobei $\sqrt{d}$ die positive Quadratwurzel von $d\in\mathbb{R}$ bezeichnet, sofern $d>0$, andernfalls $\sqrt{d}=i\sqrt{-d}$. Ferner bestätigt man leicht durch Nachrechnen

$$
a x ^ {2} + b x + c = a (x - x _ {1}) (x - x _ {2}).
$$

Beispiele. 1. Für die quadratische Gleichung $x^{2} + \sqrt{2}x + 1 = 0$ ergeben sich mit (3) die beiden Lösungen: $x_{1} = \frac{\sqrt{2}}{2}(-1 + i)$ und $x_{2} = \frac{\sqrt{2}}{2}(-1 - i)$.

2. Damit hat  $x^{4} + 1 = (x^{2} + \sqrt{2}x + 1)(x^{2} - \sqrt{2}x + 1) = 0$  die vier komplexen Lösungen:

$$
x _ {1} = \frac {\sqrt {2}}{2} (1 + i), x _ {2} = \frac {\sqrt {2}}{2} (1 - i), x _ {3} = \frac {\sqrt {2}}{2} (- 1 + i) \text {und} x _ {4} = \frac {\sqrt {2}}{2} (- 1 - i).\quad \square
$$

---

56

1. Zahlen und Vektoren

Bemerkung. Bei der numerischen Lösung einer quadratischen Gleichung per Computer sollte man (wegen der Rechnung mit endlich vielen Dezimalstellen) auf die mögliche Auslöschung führender Stellen achten. Dies tritt immer dann auf, falls $b^{2} - 4ac > 0$ und $|ac|$ sehr klein ist, und zwar in (3) bei $x_{1}$, falls $b > 0$, bzw. $x_{2}$, falls $b < 0$ ($\rightarrow$ Kap. 7, 2.5, Procedure Quadr-Gleichg).

⑥ Netzwerke mit Wechselstrom.. In Wechselstromkreisen hat man Spannungen $u(t)$ und Ströme $j(t)$, die zeitlich sinus- bzw. cosinusförmigen Verlauf besitzen,

$$
u (t) = u _ {0} \cos (\omega t + \alpha), j (t) = j _ {0} \cos (\omega t + \beta).
$$

Diese reellen Augenblickswerte faßt man auf als Realteile der komplexen Augenblickswerte

$$
U (t) = u _ {0} [ \cos (\omega t + \alpha) + i \sin (\omega t + \alpha) ],
$$

$$
I (t) = j _ {0} [ \cos (\omega t + \beta) + i \sin (\omega t + \beta) ].
$$

Der Vorteil dieser Betrachtungsweise ergibt sich bei den linearen Grundelementen, bei denen der Widerstand unabhängig von der Stromstärke ist (Ohmscher Widerstand, Kapazität, Induktivität). Für diese kann man nämlich in der komplexen Schreibweise einheitlich das Ohmsche Gesetz

$$
U (t) = Z I (t)
$$

beweisen mit einem konstanten komplexen Widerstand Z, der wie folgt erklärt ist:

![](../../raw/pages_0065-0096/images/page_71_image_11.jpg)

<details>
<summary>text_image</summary>

Widerstand R Z = R
Kapazität C Z = 1 / iωC = -1 / ωC i
Induktivität L Z = iωL .
</details>

Ein lineares Netzwerk ist ein Stromkreis, der diese drei Elemente in irgendeiner Zusammensetzung enthält. Mit den KIRCHHOFFschen Regeln ergibt sich für die Zusammenschaltung zweier komplexer Widerstände $Z_1$, $Z_2$ als Gesamtwider-

stand (Ersatzwiderstand): Z bei

Reihenschaltung

$$
Z = Z _ {1} + Z _ {2},
$$

Parallelschaltung

$$
\frac {1}{Z} = \frac {1}{Z _ {1}} + \frac {1}{Z _ {2}}, Z = \frac {Z _ {1} Z _ {2}}{Z _ {1} + Z _ {2}}.
$$

![](../../raw/pages_0065-0096/images/page_71_image_18.jpg)

Abb. 44 – Schaltungen

Zum komplexen Widerstand Z heißen Re Z Wirkwiderstand, Im Z Blindwiderstand und |Z| Scheinwiderstand oder Impedanz.

---

§8. Die komplexen Zahlen

57

Beispiel. An der elektrischen Schaltung (→ Abb. 45) mit $R_{1}=48\Omega$, $R_{2}=22\Omega$, $C=20\mu F$, $L=155mH$ wird eine Wechselspannung $U_{i}$ von $U_{eff}=220V$ und 50Hz angelegt. Der komplexe Widerstand des Stromkreises ist

$$
\begin{array}{l} Z = \frac {\left(R _ {1} - \frac {i}{\omega C}\right) (R _ {2} + i \omega L)}{\left(R _ {1} - \frac {i}{\omega C}\right) + (R _ {2} + i \omega L)} \\ = \frac {\left[ R _ {1} ^ {2} R _ {2} + R _ {1} R _ {2} ^ {2} + R _ {1} L ^ {2} \omega^ {2} + \frac {R _ {2}}{\omega^ {2} C ^ {2}} \right] + i \left[ R _ {1} ^ {2} \omega L - \frac {R _ {2} ^ {2}}{\omega C} + \frac {L}{\omega C ^ {2}} - \frac {\omega L ^ {2}}{C} \right]}{(R _ {1} + R _ {2}) ^ {2} + \left(\omega L - \frac {1}{\omega C}\right) ^ {2}} \\ \approx (4 3. 5 6 + i   5 2. 1 1) \Omega . \\ \end{array}
$$

Damit fließt der Effektivstrom  $I_{eff} = \frac{U_{eff}}{|Z|} \approx 3.24A$ , da  $|Z| \approx 67.92\Omega$ .

Legt man eine Wechselspannung mit der Frequenz 104.41Hz an, so verhält sich der Stromkreis wie ein ohmscher (reeller) Widerstand; denn für

$$
\omega^ {2} L C = \frac {L - C R _ {2} ^ {2}}{L - C R _ {1} ^ {2}}
$$

verschwindet Im Z ; dh.  $Z \approx 126\Omega$ .

![](../../raw/pages_0065-0096/images/page_72_image_8.jpg)

<details>
<summary>text_image</summary>

L
R₂
C
R₁
U
</details>

Abb. 45 - Stromkreis

In späteren Kapiteln werden zahlreiche weitere Anwendungen der komplexen Zahlen behandelt ( $\rightarrow$  Kap. 2, §3, Kap. 3, 1.10, Kap. 6, §1 und Band 2, Kap. 10).
