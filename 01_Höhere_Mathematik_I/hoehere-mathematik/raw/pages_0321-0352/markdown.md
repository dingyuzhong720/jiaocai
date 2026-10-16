② gilt  $\tilde{E}^{T} = \tilde{E}$ , für  $\tilde{E}$  vom Typ ③ ist auch  $\tilde{E}^{T}$  eine Elementarmatrix vom Typ ③, hierfür gilt det  $\tilde{E} = 1 = \det \tilde{E}^{T}$  ( $\rightarrow$  (5)). □

Folgerungen aus dem Multiplikationssatz.

a)  $\det(AB) = \det(BA)$
b) $\operatorname{det}(A^k) = (\operatorname{det} A)^k \quad (k \in \mathbb{N})$
c) $\det (A^{-1}) = (\det A)^{-1}$, falls $A$ invertierbar
d) $\det (C^{-1}AC) = \det A$ , für alle invertierbaren $C\in \mathbb{R}^{n\times n}$
e) Der Kästchensatz. Für eine Blockmatrix (→ 4.4) der Form

$$
A = \left( \begin{array}{c c} B & C \\ 0 & D \end{array} \right) \quad \text {bzw.} \quad A = \left( \begin{array}{c c} B & 0 \\ C & D \end{array} \right)
$$

mit $k \times k$-Matrix $B$, $(n-k) \times (n-k)$-Matrix $D$, 0 Nullmatrix und $C$ jeweils vom passenden Typ gilt

$$
\det A = \det B \det D.
$$

Beweis. a):  $\det(AB) = \det A \det B = \det B \det A = \det(BA)$ .

b):  $\det(A^{k}) = (\det A)(\det A^{k-1}) = \cdots = (\det A)^{k}$ .
c): $1 = \det E = \det A^{-1}A = (\det A^{-1})(\det A)$.
d): $\operatorname{det}(C^{-1}AC) = \operatorname{det}(AC)C^{-1} = \operatorname{det}A$.
e): Man rechnet leicht

$$
\left( \begin{array}{c c} B & C \\ 0 & D \end{array} \right) = \left( \begin{array}{c c} E & 0 \\ 0 & D \end{array} \right) \left( \begin{array}{c c} B & C \\ 0 & E \end{array} \right)
$$

nach, mit jeweils $E$ vom passenden Typ. Der zweite Faktor kann mit elementaren Zeilenumformungen vom Typ ③ (welche die Determinante nicht ändern) in $\begin{pmatrix} B & 0 \\ 0 & E \end{pmatrix}$ umgewandelt werden. Aus det $\begin{pmatrix} B & 0 \\ 0 & E \end{pmatrix} = \det B$, det $\begin{pmatrix} E & 0 \\ 0 & D \end{pmatrix} = \det D$ (einfache Übung) und dem Multiplikationssatz folgt nun die Behauptung.

5.4 Die Entwicklung von det A nach einer beliebigen Zeile oder Spalte. Die Matrix  $\tilde{A} = (\mathbf{a}_{j}, \mathbf{a}_{1}, \ldots, \mathbf{a}_{j-1}, \mathbf{a}_{j+1}, \ldots, \mathbf{a}_{n})$  entsteht aus  $A = (\mathbf{a}_{1}, \ldots, \mathbf{a}_{j}, \ldots, \mathbf{a}_{n})$  durch j - 1 sukzessive Vertauschungen benachbarter Spalten. Also gilt det  $\tilde{A} = (-1)^{j-1}$  det A. Entwickelt man andererseits erneut det  $\tilde{A}$  mit (4), dann ergibt sich die sogenannte Entwicklung von det A nach der j-ten Spalte:

$$
\det A = \sum_ {i = 1} ^ {n} (- 1) ^ {i + j} \alpha_ {i j} \det A _ {i j}
$$

wobei  $A_{ij}$  die  $(n-1)\times(n-1)$ -Matrix bezeichnet, die aus A durch Streichen der i-ten Zeile und j-ten Spalte entsteht. Wegen det  $A^{T} = \det A$  hat man ebenso die Entwicklung von det A nach der i-ten Zeile:

$$
\boxed {\det A = \sum_ {j = 1} ^ {n} (- 1) ^ {i + j} \alpha_ {i j} \det A _ {i j}.}
$$

5.5 Beispiele. Zur Berechnung von det A (für n > 3) ist es zweckmäßig, zuerst mit elementaren Umformungen möglichst viele Nullen zu erzeugen. Dabei sind die Regeln (5) zu beachten.

Beispiel 1. (→ (8e))

$$
\det \left( \begin{array}{c c c c c} 1 & 3 & - 5 & 1 & 4 \\ 4 & 2 & 2 & 0 & - 3 \\ 0 & 0 & 1 & 2 & 3 \\ 0 & 0 & 0 & 4 & 5 \\ 0 & 0 & 0 & 0 & - 6 \end{array} \right) = \det \left( \begin{array}{c c} 1 & 3 \\ 4 & 2 \end{array} \right) \det \left( \begin{array}{c c c} 1 & 2 & 3 \\ 0 & 4 & 5 \\ 0 & 0 & - 6 \end{array} \right) = 2 4 0. \quad \square
$$

Beispiele 2.  $\det\begin{pmatrix}1&2&3\\2&1&1\\3&3&4\end{pmatrix}=0$   $(\mathbf{z}_{3}=\mathbf{z}_{1}+\mathbf{z}_{2})$ ;

$\operatorname*{det}\left(\begin{array}{ccc}0 & 2 & 3\\ 0 & 1 & 4\\ 1 & 2 & -1 \end{array}\right) = +\alpha_{31}\operatorname*{det}A_{31} = 1\cdot \operatorname*{det}\left( \begin{array}{cc}2 & 3\\ 1 & 4 \end{array} \right) = 5;$

$\operatorname*{det}\left(\begin{array}{ccc}1 & 2 & 3 & 4\\ 0 & 4 & 1 & 2\\ 0 & 1 & 3 & -1\\ -1 & 2 & 0 & 1 \end{array}\right) = \operatorname*{det}\left(\begin{array}{c|cc}1 & 2 & 3 & 4\\ \hline 0 & 4 & 1 & 2\\ 0 & 1 & 3 & -1\\ 0 & 4 & 3 & 5 \end{array}\right) = \operatorname*{det}\left(\begin{array}{ccc}4 & 1 & 2\\ 1 & 3 & -1\\ 4 & 3 & 5 \end{array}\right) = 45,$

die Matrix ist invertierbar; sowohl Zeilen als auch Spalten sind linear unabhängig.

Beispiel 3. (Die Vandermonde-Determinante)

$$
\begin{array}{l} = (y - x) (z - x) \det \left( \begin{array}{c c} 1 & y + x \\ 1 & z + x \end{array} \right) = (y - x) (z - x) \det \left( \begin{array}{c c} 1 & y \\ 1 & z \end{array} \right) \\ = (y - x) (z - x) (z - y) . \\ \end{array}
$$

$\operatorname*{det}\left( \begin{array}{ccc}1 & x & x^2\\ 1 & y & y^2\\ 1 & z & z^2 \end{array} \right) = \operatorname*{det}\left( \begin{array}{ccc}1 & x & x^2\\ 0 & y - x & y^2 -x^2\\ 0 & z - x & z^2 -x^2 \end{array} \right) = \operatorname*{det}\left( \begin{array}{ccc}y - x & y^2 -x^2\\ z - x & z^2 -x^2 \end{array} \right)$

Analog

$$
\det \left( \begin{array}{c c c} 1 & x _ {1}, \dots , & x _ {1} ^ {n - 1} \\ 1 & x _ {2}, \dots , & x _ {2} ^ {n - 1} \\ \vdots & \vdots & \vdots \\ 1 & x _ {n}, \dots , & x _ {n} ^ {n - 1} \end{array} \right) = \prod_ {1 \leq i <   j \leq n} (x _ {j} - x _ {i}).
$$

wobei auf der rechten Seite das Produkt über alle Differenzen  $x_{j}-x_{i}$  mit i<j zu bilden ist. Diese Determinante ist genau dann $\neq 0$, wenn die $x_{1},\ldots ,x_{n}$ paarweise verschieden sind.

Diese nach A. VANDERMONDE (1735–1796) benannte Determinante bzw. Matrix tritt beispielsweise bei der Polynominterpolation auf, wenn man die Koeffizienten des Polynoms  $p(x) = a_{0} + a_{1}x + \cdots + a_{n-1}x^{n-1}$  mit  $p(x_{i}) = y_{i} \quad (1 \leq i \leq n)$  aus dem Gleichungssystem  $a_{0} + x_{i}a_{1} + x_{i}^{2}a_{2} + \cdots + x_{i}^{n-1}a_{n-1} = y_{i} \quad (1 \leq i \leq n)$  berechnet.

Beispiel 4. Mit Rechenschema Ⓓ zur LR-Zerlegung (→ 4.4) berechnet man

$$
A = \left( \begin{array}{c c c} 1 & 2 & 3 \\ 2 & 1 & 0 \\ 1 & 0 & 2 \end{array} \right) = \left( \begin{array}{c c c} 1 & & 0 \\ & 1 & \\ * & & 1 \end{array} \right) \left( \begin{array}{c c c} 1 & & * \\ & - 3 & \\ 0 & & 3 \end{array} \right)
$$

also gilt $\det A = \det L\det R = \det R = -9$

## 5.6 Anwendungen.

① Die Cramer-Regel (G. CRAMER, 1704 - 1752). Mit einer invertierbaren Matrix $A = (\mathbf{a}_1, \ldots, \mathbf{a}_n) \in \mathbb{R}^{n \times n}$ und $\mathbf{b} \in \mathbb{R}^n$ hat das Gleichungssystem $Ax = \mathbf{b}$ die Lösung

$$
x _ {i} = \frac {1}{\det A} \det (\mathbf {a} _ {1}, \dots , \mathbf {a} _ {i - 1}, \mathbf {b}, \mathbf {a} _ {i + 1}, \dots , \mathbf {a} _ {n}) \tag {9}
$$

(die i-te Spalte von A wird durch b ersetzt),  $1 \leq i \leq n$ .

Beweis. Wir tragen $\mathbf{b}=Ax=\sum x_{i}\mathbf{a}_{i}$ anstelle von $\mathbf{a}_{1}$ ein und verwenden die Linearität von det in der ersten Spalte:

$$
\begin{array}{l} \det (\mathbf {b}, \mathbf {a} _ {2}, \dots , \mathbf {a} _ {n}) = \det (x _ {1} \mathbf {a} _ {1} + \dots + x _ {n} \mathbf {a} _ {n}, \mathbf {a} _ {2}, \dots , \mathbf {a} _ {n}) \\ = \sum_ {i = 1} ^ {n} x _ {i} \det (\mathbf {a} _ {i}, \mathbf {a} _ {2}, \dots , \mathbf {a} _ {n}) \\ = x _ {1} \det (\mathbf {a} _ {1}, \dots , \mathbf {a} _ {n}) = x _ {1} \det A, \\ \end{array}
$$

die anderen Summanden sind Null, weil jeweils zwei gleiche Spalten vorhanden sind;  $x_{2},\ldots,x_{n}$  ebenso. ☐

Man sollte (9) nicht zur vollständigen Auflösung eines Systems mit vielen Unbekannten verwenden (Rechenaufwand)! Die Formel ist aber gut geeignet zur Berechnung einzelner Unbekannter und besonders günstig zur Weiterverarbeitung, wenn im Gleichungssystem zusätzliche Parameter enthalten sind.

## Beispiele.

$$
\begin{array}{l} 1. \quad 2 x + 3 y = \quad 3 \\ 5 x - 7 y = - 1 \end{array} \Longrightarrow x = \frac {\det \left( \begin{array}{c c} 3 & 3 \\ - 1 & - 7 \end{array} \right)}{\det \left( \begin{array}{c c} 2 & 3 \\ 5 & - 7 \end{array} \right)} = \frac {1 8}{2 9}, \quad y = \frac {\det \left( \begin{array}{c c} 2 & 3 \\ 5 & - 1 \end{array} \right)}{\det \left( \begin{array}{c c} 2 & 3 \\ 5 & - 7 \end{array} \right)} = \frac {1 7}{2 9}.
$$

2. Man benötigt nur  $x_{2}$  aus folgendem  $4 \times 4$ -Gleichungssystem:

$$
\begin{array}{r l} 5 x _ {1} + 3 x _ {2} + 2 x _ {3} & = 4 \\ - 3 x _ {1} + 5 x _ {2} + 6 x _ {3} - 5 x _ {4} & = 1 \\ 3 x _ {2} + x _ {3} - x _ {4} & = 0 \\ 5 x _ {1} + 3 x _ {2} + 4 x _ {3} + x _ {4} & = 0 \end{array} \implies x _ {2} = \frac {\det \left( \begin{array}{c c c c} 5 & 4 & 2 & 0 \\ - 3 & 1 & 6 & - 5 \\ 0 & 0 & 1 & - 1 \\ 5 & 0 & 4 & 1 \end{array} \right)}{\det \left( \begin{array}{c c c c} 5 & 3 & 2 & 0 \\ - 3 & 5 & 6 & - 5 \\ 0 & 3 & 1 & - 1 \\ 5 & 3 & 4 & 1 \end{array} \right)} = - \frac {9 5}{1 5 6}.
$$

![](images/page_323_image_6.jpg)

② Die Adjunkte von $A$. Sei zunächst $A \in \mathbb{R}^{n \times n}$ invertierbar und $A^{-1} = (\beta_{ij}) = (\mathbf{b}_1, \ldots, \mathbf{b}_n)$, dann erfüllt $\mathbf{b}_j$ wegen $AA^{-1} = (Ab_1, \ldots, Ab_n) = E = (\mathbf{e}_1, \ldots, \mathbf{e}_n)$ das Gleichungssystem $Ab_j = \mathbf{e}_j$. Bestimmt man die $i$-te Komponente $\beta_{ij}$ von $\mathbf{b}_j$ mit der Cramer-Regel (9) und entwickelt den Zähler nach der $i$-ten Spalte ($\rightarrow$ 5.4), dann ergibt sich

$$
\beta_ {i j} = \frac {1}{\det A} \det (\mathbf {a} _ {1}, \dots , \mathbf {a} _ {i - 1}, \mathbf {e} _ {j}, \mathbf {a} _ {i + 1}, \dots , \mathbf {a} _ {n}) = \frac {1}{\det A} (- 1) ^ {i + j} \det A _ {j i}.
$$

Man beachte die Änderung der Indexreihenfolge ( $A_{ij}$  ist die Matrix, die aus A durch Streichen der i-ten Zeile und j-ten Spalte entsteht).

Man nennt $A^{*} := (\alpha_{ij}^{*})$ mit $\alpha_{ij}^{*} = (-1)^{i+j} \det A_{ji}$ die Adjunkte von $A$. Sie stellt bis auf einen Faktor die inverse Matrix von $A$ dar:

$$
A ^ {- 1} = \frac {1}{\det A} A ^ {*} = \frac {1}{\det A} \left((- 1) ^ {i + j} \det A _ {j i}\right) _ {i j}. \tag {10}
$$

Beachte.  $A^{*}$  ist auch im Falle det A = 0 definiert. In numerischen Rechnungen mit großem n sind in jedem Falle die Verfahren aus 4.4 vorzuziehen.

③ Flächeninhalte und Volumina ( $\rightarrow$  5.1). Ein Tetraeder im  $R^{3}$  mit den Eckpunkten  $A_{i} = (x_{i}, y_{i}, z_{i})$   $(1 \leq i \leq 4)$  hat das Volumen  $V = \frac{1}{6} |\det(\mathbf{a}, \mathbf{b}, \mathbf{c})|$  mit  $a = \overrightarrow{A_{1}A_{2}}$ ,  $b = \overrightarrow{A_{1}A_{3}}$ ,  $c = \overrightarrow{A_{1}A_{4}}$ .

Eine leichte Umformung der Determinante ergibt eine „4-Punkte-Formel“

$$
V = \frac {1}{6} \left| \det \left( \begin{array}{c c c c} 1 & x _ {1} & y _ {1} & z _ {1} \\ 1 & x _ {2} & y _ {2} & z _ {2} \\ 1 & x _ {3} & y _ {3} & z _ {3} \\ 1 & x _ {4} & y _ {4} & z _ {4} \end{array} \right) \right|.
$$

④ Kegelschnitte. Ein Kegelschnitt in der  $(x,y)$ -Ebene hat eine Gleichung der Form

$$
a _ {1} x ^ {2} + a _ {2} y ^ {2} + a _ {3} x y + a _ {4} x + a _ {5} y + a _ {6} = 0,
$$

in der nicht alle Koeffizienten $a_{i}$ Null sind. Da ein Koeffizient zu 1 normiert werden kann, sind im allgemeinen zur Bestimmung der Koeffizienten 5 verschiedene Punkte auf der Kurve erforderlich. Die Punkte $A_{i} = (x_{i}, y_{i})$ $(1 \leq i \leq 5)$ und der „allgemeine“ Punkt $X = (x, y)$ auf dem Kegelschnitt liefern ein lineares Gleichungssystem

$$
\begin{array}{l} a _ {1} x ^ {2} + a _ {2} y ^ {2} + a _ {3} x y \quad + a _ {4} x \quad + a _ {5} y \quad + a _ {6} = 0 \\ a _ {1} x _ {1} ^ {2} + a _ {2} y _ {1} ^ {2} + a _ {3} x _ {1} y _ {1} + a _ {4} x _ {1} + a _ {5} y _ {1} + a _ {6} = 0 \\ \begin{array}{c c c} \cdot & & \cdot \\ \cdot & & \cdot \\ \cdot & & \cdot \end{array} \\ a _ {1} x _ {5} ^ {2} + a _ {2} y _ {5} ^ {2} + a _ {3} x _ {5} y _ {5} + a _ {4} x _ {5} + a _ {5} y _ {5} + a _ {6} = 0 \\ \end{array}
$$

für  $a_{1},\ldots,a_{6}$ . Da dieses eine von Null verschiedene Lösung besitzt, muß die Determinante der Koeffizientenmatrix Null sein. Das ergibt die sogenannte

5-Punkte-Gleichung für den allgemeinen Kegelschnitt

$$
\det \left( \begin{array}{c c c c c c} x ^ {2} & y ^ {2} & x y & x & y & 1 \\ x _ {1} ^ {2} & y _ {1} ^ {2} & x _ {1} y _ {1} & x _ {1} & y _ {1} & 1 \\ \vdots & \vdots & \vdots & \vdots & \vdots & \vdots \\ x _ {5} ^ {2} & y _ {5} ^ {2} & x _ {5} y _ {5} & x _ {5} & y _ {5} & 1 \end{array} \right) = 0.
$$

Bemerkung. Spezielle Kegelschnitte sind durch weniger als 5 Punkte festgelegt. So hat beispielsweise ein Kreis die Gleichung  $a(x^{2} + y^{2}) + bx + cy + d = 0$ , er ist durch 3 verschiedene Punkte festgelegt. Genau wie zuvor ergibt sich:

$$
\det \left( \begin{array}{c c c c} x ^ {2} + y ^ {2} & x & y & 1 \\ x _ {1} ^ {2} + y _ {1} ^ {2} & x _ {1} & y _ {1} & 1 \\ x _ {2} ^ {2} + y _ {2} ^ {2} & x _ {2} & y _ {2} & 1 \\ x _ {3} ^ {2} + y _ {3} ^ {2} & x _ {3} & y _ {3} & 1 \end{array} \right) = 0
$$

ist die Gleichung des Kreises durch die Punkte  $(x_{i}, y_{i})$ , i = 1, 2, 3.

Beispiel. Der Kreis durch die Punkte  $(0,0)$ ,  $(1,3)$ ,  $(2,-1)$  hat die Gleichung

$$
\det \left( \begin{array}{c c c c} x ^ {2} + y ^ {2} & x & y & 1 \\ 0 & 0 & 0 & 1 \\ 1 0 & 1 & 3 & 1 \\ 5 & 2 & - 1 & 1 \end{array} \right) = - \det \left( \begin{array}{c c c} x ^ {2} + y ^ {2} & x & y \\ 5 & 2 & - 1 \\ 1 0 & 1 & 3 \end{array} \right) = 0,
$$

also: $7(x^{2} + y^{2}) - 25x - 15y = 0$.

Weitere, besonders wichtige Anwendungen werden in den folgenden Paragraphen behandelt.

## Aufgaben

1. Man berechne die Determinanten der Matrizen

$$
\left( \begin{array}{c c} r \cos \alpha & - r \sin \alpha \\ r \sin \alpha & r \cos \alpha \end{array} \right)  , \qquad \left( \begin{array}{c c c} 1 / 2 & 1 / 3 & 1 / 4 \\ 1 / 3 & 1 / 4 & 1 / 5 \\ 1 / 4 & 1 / 5 & 1 / 6 \end{array} \right)  , \qquad \left( \begin{array}{c c c c} 1 & 1 & 1 & 1 \\ 2 & a & a & a \\ 2 & 3 & b & b \\ 2 & 3 & 4 & c \end{array} \right)  ,
$$

a) mittels Entwicklung nach der ersten Zeile;
b) mittels elementarer Umformungen bis zur oberen Dreiecksgestalt.

2. Man berechne die Determinante der Matrizen

$$
\left( \begin{array}{c c c c} 1 & 0 & - 1 & 2 \\ 2 & 1 & 2 & 1 \\ - 3 & 1 & 0 & 1 \\ 2 & 2 & 0 & - 1 \end{array} \right), \quad \left( \begin{array}{c c c c} 1 / 2 & 1 / 3 & 1 / 4 & 1 / 5 \\ 1 / 3 & 1 / 4 & 1 / 5 & 1 / 6 \\ 1 / 4 & 1 / 5 & 1 / 6 & 1 / 7 \\ 1 / 5 & 1 / 6 & 1 / 7 & 1 / 8 \end{array} \right), \quad \left( \begin{array}{c c c c c c} 2 & 0 & 0 & 0 & 0 & 1 \\ 1 & 2 & 0 & 0 & 0 & 1 \\ 3 & 1 & 2 & 0 & 0 & 1 \\ 0 & 3 & 1 & 2 & 0 & 1 \\ - 5 & 0 & 3 & 1 & 2 & 1 \\ 1 & 1 & 1 & 1 & 1 & 1 \end{array} \right).
$$

3. Man löse mit der Cramer-Regel Ax = b mit

$$
A = \left( \begin{array}{c c c c} 2 & - 1 & 0 & 1 \\ 2 & 2 & 0 & 1 \\ - 4 & - 4 & 3 & 0 \\ - 2 & 2 & 1 & 0 \end{array} \right), \quad \mathbf {b} = \left( \begin{array}{c} 3 \\ 4 \\ 1 \\ 2 \end{array} \right).
$$

4. Man beweise

$$
\text {a)} \det \left( \begin{array}{c c c c c c c c} 1 & 2 & 3 & 4 & \dots & n - 2 & n - 1 & n \\ 2 & 3 & 4 & & \dots & n - 1 & n & 1 \\ 3 & 4 & & & \dots & n & 1 & 2 \\ \vdots & & & & & & & \vdots \\ n & 1 & 2 & & \dots & n - 3 & n - 2 & n - 1 \end{array} \right) = (- 1) ^ {\frac {n (n - 1)}{2}} \frac {(n + 1) n ^ {n - 1}}{2}.
$$

$$
\text {b)} \det \left( \begin{array}{c c c c c} 1 & 1 & 1 & \dots & 1 \\ 1 & 2 & 3 & \dots & n \\ 1 & 2 ^ {2} & 3 ^ {2} & \dots & n ^ {2} \\ \vdots & & & & \vdots \\ 1 & 2 ^ {n - 1} & 3 ^ {n - 1} & \dots & n ^ {n - 1} \end{array} \right) = 1! 2! 3! \dots (n - 1)!.
$$

5. Man gebe für die Gleichungen einer Ebene durch 3 Punkte im $\mathbb{R}^3$ eine Darstellung mittels $4\times 4$-Determinate.
6. Man beweise für zwei Spaltenvektoren $\mathbf{a},\mathbf{b}\in\mathbb{R}^{n}$

$$
\det (E + \mathbf {a b} ^ {T}) = 1 + \mathbf {a} ^ {T} \mathbf {b} \quad \text {und} \quad \det (\alpha E + \mathbf {a b} ^ {T}) = \alpha^ {n - 1} (\alpha + \mathbf {a} ^ {T} \mathbf {b}), \alpha \in \mathbb {R}.
$$

7. a) Für die Fläche eines ebenen Dreiecks mit den Seiten $a, b, c$ gilt bekanntlich die HERON-Formel:

$$
F = \sqrt {s (s - a) (s - b) (s - c)} \quad \text { mit } \quad s = \frac {1}{2} (a + b + c) .
$$

Man rechne nach, daß hierfür die folgende Formel gilt:

$$
F ^ {2} = - \frac {1}{1 6} \det \left( \begin{array}{c c c c} 0 & a ^ {2} & b ^ {2} & 1 \\ a ^ {2} & 0 & c ^ {2} & 1 \\ b ^ {2} & c ^ {2} & 0 & 1 \\ 1 & 1 & 1 & 0 \end{array} \right) .
$$

b) Für das Volumen $V$ des Tetraeders mit den Kantenlängen $a, b, c, p, q, r$ (Reihenfolge aus der Skizze) gilt:

$$
V ^ {2} = \frac {1}{2 ^ {5} \cdot 3 ^ {2}} \det \left( \begin{array}{c c c c c} 0 & a ^ {2} & b ^ {2} & c ^ {2} & 1 \\ a ^ {2} & 0 & r ^ {2} & q ^ {2} & 1 \\ b ^ {2} & r ^ {2} & 0 & p ^ {2} & 1 \\ c ^ {2} & q ^ {2} & p ^ {2} & 0 & 1 \\ 1 & 1 & 1 & 1 & 0 \end{array} \right) .
$$

![](images/page_326_image_5.jpg)

<details>
<summary>text_image</summary>

a
F
b
c
</details>

![](images/page_326_image_6.jpg)

<details>
<summary>text_image</summary>

a
b
c
q
r
p
</details>

Welchen Inhalt hat der Tetraeder mit den Kantenlängen

$a = 1cm; b = 2cm; c = 3cm; p = 4cm; q = 3cm$ und $r = 2cm$?

8. Seien $y_i : \mathbb{R} \to \mathbb{R}$ ($i = 1,2,3$) dreimal differenzierbar und Lösungen der linearen Differentialgleichung $y_i'''(x) + a_1(x)y_i''(x) + a_2(x)y_i'(x) + a_3(x)y_i(x) = 0$

und $W(x) := \det \left( \begin{array}{cc} y_1(x) & y_2(x) & y_3(x) \\ y_1'(x) & y_2'(x) & y_3'(x) \\ y_1''(x) & y_2''(x) & y_3''(x) \end{array} \right)$ die sog. WRONSKI-Determinante.

Man zeige $\frac{d}{dx} W(x) = -a_1(x)W(x)$.

## §6. Lineare Abbildungen und Eigenwerte

Nach den linearen Gleichungssystemen behandeln wir nun als zweiten wichtigen Anwendungsbereich der Matrizen die linearen Abbildungen. Im  $R^{n}$  sind das die Zuordnungen  $x \mapsto Ax$  ( $x \in R^{n}$  und fester  $n \times n$ -Matrix A). Im Hinblick auf allgemeine Anwendungen ist es aber erforderlich, die grundlegenden Begriffe und Bezeichnungen in beliebigen Vektorräumen und unabhängig von speziellen Basen zu formulieren.

6.1 Lineare Abbildungen. Seien $V, W$ Vektorräume über $\mathbb{R}$. Mit einer Abbildung $f: V \to W$ („von $V$ in $W$“) wird jedem Vektor $\mathbf{v} \in V$ ein eindeutig bestimmter Vektor $\mathbf{w} = f(\mathbf{v}) \in W$, das sogenannte $f$-Bild von $\mathbf{v}$ zugeordnet.

Definition. Eine Abbildung  $f : V \rightarrow W$  heißt linear, wenn gilt:

(L.1) $f$ ist homogen; d.h. $f(\alpha \mathbf{v}) = \alpha f(\mathbf{v})$ für alle $\alpha \in \mathbb{R}$, $\mathbf{v} \in V$,

(L.2) $f$ ist additiv; d.h. $f(\mathbf{u} + \mathbf{v}) = f(\mathbf{u}) + f(\mathbf{v})$ für alle $\mathbf{u},\mathbf{v}\in V$.

Andere Bezeichnungen für eine lineare Abbildung sind: lineare Transformation, linearer Operator, Vektorraumhomomorphismus.

Gleichwertig mit (L.1), (L.2) ist

$$
f (\alpha_ {1} \mathbf {v} _ {1} + \dots + \alpha_ {n} \mathbf {v} _ {n}) = \alpha_ {1} f (\mathbf {v} _ {1}) + \dots + \alpha_ {n} f (\mathbf {v} _ {n}) \tag {1}
$$

für alle $\alpha_{i}\in\mathbb{R},\;\mathbf{v}_{i}\in V\quad(1\leq i\leq n;n\in\mathbb{N})$,

was besagt, daß das f-Bild jeder Linearkombination gleich der entsprechenden Linearkombination der einzelnen f-Bilder ist.

Beispiele. Lineare Abbildungen sind:

1. Die Nullabbildung  $0: V \rightarrow V$ ,  $0(\mathbf{v}) := \mathbf{0}$ .
2. Die identische Abbildung $\operatorname{Id}: V \to V$, $\operatorname{Id}(\mathbf{v}) := \mathbf{v}$.
3. Die Projektion  $p_{i}: R^{n} \rightarrow R$ ,  $p_{i}(x) := x_{i}$  (i-te Komponente von x).
4. Die Multiplikation mit einer festen  $m \times n$ -Matrix A

$$
l: \mathbb {R} ^ {n} \to \mathbb {R} ^ {m}, \quad l (\mathbf {x}) := A \mathbf {x}.
$$

5. Der Differentiationsoperator $\frac{d}{dx}:\mathcal{C}^{1}(I)\to\mathcal{C}^{0}(I),\quad\frac{d}{dx}f(x):=f^{\prime}(x).\quad\mathcal{C}^{0}(I)$ bzw. $\mathcal{C}^{1}(I)$ bezeichnet den Vektorraum aller auf dem Intervall $I\subseteq\mathbb{R}$ stetigen bzw. stetig differenzierbaren Funktionen.

6. Das Integral $f \mapsto \int_{a}^{b} f(x) dx$, $f \in \mathscr{C}^0(a, b)$.

Keine linearen Abbildungen sind:

7. Die Parallelverschiebung $t_a : V \to V$, $t_a(\mathbf{v}) := \mathbf{v} + \mathbf{a}$ (mit festem Vektor $\mathbf{a} \neq 0$).

8.  $f : R_{2} \to R_{2}$ ,  $f(x, y) := (x^{2}, x + y)$  (quadratisch in der 1. Komponente).

Lineare Abbildungen in der Technik:

9. Die Werkstoffbeanspruchung eines elastischen Körpers, auf den von außen Kräfte wirken, wird in der linearen Elastostatik durch den Spannungstensor S beschrieben. Dieser bestimmt für jeden inneren Punkt P eine lineare Abbildung, die den Normalenrichtungen n von (idealisierten) Schnittebenen E

![](images/page_327_image_18.jpg)

<details>
<summary>text_image</summary>

E
t
n
P
</details>

Abb. 146 - Dreiachsiger Spannungszustand

durch $P$ den Spannungsvektor $\mathbf{t} \in \mathbb{R}^3$ zuordnet, d.h. in kartesischen Koordinaten:

$$
\mathbf {t} = S \mathbf {n} \quad \text {mit} \quad S = \left( \begin{array}{c c c} \sigma_ {x} & \tau_ {x y} & \tau_ {x z} \\ \tau_ {x y} & \sigma_ {y} & \tau_ {y z} \\ \tau_ {x z} & \tau_ {y z} & \sigma_ {z} \end{array} \right) .
$$

Für $|\mathbf{n}| = 1$ ist $\mathbf{t} := \lim_{\Delta A \to 0} \frac{1}{\Delta A} \mathbf{k}_{\Delta A}$, wenn $\mathbf{k}_{\Delta A}$ die Kraft bezeichnet, die auf ein Flächenstück in $E$ mit Schwerpunkt $P$ und Flächeninhalt $\Delta A$ wirkt ($\rightarrow$ Aufg. 7, §7).

10. Für einen linearen elektrischen Vierpol (→ Abb. 147) gilt zwischen Ein- und Ausgang die Beziehung

$$
\binom{u _ {1}}{i _ {1}} = A \binom{u _ {2}}{i _ {2}}
$$

mit der Kettenmatrix

$$
A = \left( \begin{array}{c c} \frac {R _ {2} + R _ {3}}{R _ {2}} & R _ {3} \\ \frac {R _ {1} + R _ {2} + R _ {3}}{R _ {1} R _ {2}} & \frac {R _ {1} + R _ {3}}{R _ {1}} \end{array} \right). \quad \square
$$

![](images/page_328_image_4.jpg)

<details>
<summary>text_image</summary>

i₁
u₁
R₁
R₃
R₂
i₂
u₂
</details>

Abb. 147 - Vierpol

Man verifiziert leicht, daß zu linearen Abbildungen $f, g : V \to W$ und $\alpha \in \mathbb{R}$ auch die Summe $f + g : V \to W$, $(f + g)(\mathbf{v}) := f(\mathbf{v}) + g(\mathbf{v})$, und das $\alpha$-fache $\alpha f : V \to W$, $(\alpha f)(\mathbf{v}) := \alpha f(\mathbf{v})$, linear sind. Mit dieser Addition und skalaren Multiplikation ist die Menge aller linearen Abbildungen von $V$ in $W$

$$
\mathrm{Hom} (V, W) := \{f ; f: V \to W \text {linear} \}
$$

selbst wieder ein $\mathbb{R}$-Vektorraum (Raum der Homomorphismen).

Auch sieht man leicht ein, daß die Hintereinanderausführung („Komposition“) zweier linearer Abbildungen insgesamt ebenfalls linear ist; d.h., für zwei lineare Abbildungen $f:V\to W$, $g:U\to V$ ist auch

$$
f \circ g: U \to W, \quad (f \circ g) (\mathbf {u}) := f (g (\mathbf {u})),
$$

linear.

Ist $V$ ein endlichdimensionaler $\mathbb{R}$-Vektorraum und $B = (\mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_n)$ eine Basis von $V$, dann läßt sich jeder Vektor $\mathbf{v} \in V$ eindeutig in der Form $\mathbf{v} = \alpha_1 \mathbf{v}_1 + \cdots + \alpha_n \mathbf{v}_n$ mit $\alpha_i \in \mathbb{R}$ darstellen. Man nennt

$$
\mathbf {v} _ {B} := \left( \begin{array}{c} \alpha_ {1} \\ \vdots \\ \alpha_ {n} \end{array} \right) \in \mathbb {R} ^ {n} \quad (\text {falls} \mathbf {v} = \sum_ {i = 1} ^ {n} \alpha_ {i} \mathbf {v} _ {i}) \tag {2}
$$

den Koordinatenvektor von $\mathbf{v} \in V$ bezüglich $B$. Die lineare Abbildung $\mathbf{v} \mapsto \mathbf{v}_B$ (von $V$ in $\mathbb{R}^n$) heißt Koordinatenabbildung bzgl. $B$. Mit ihr überträgt man Probleme aus $V$ zur rechnerischen Behandlung in den $\mathbb{R}^n$ und umgekehrt mit der (inversen) Abbildung $(\alpha_1, \ldots, \alpha_n)^T \to \alpha_1 \mathbf{v}_1 + \cdots + \alpha_n \mathbf{v}_n$ nach $V$ zurück.

6.2 $V = W = \mathbb{R}^n$. Von nun an betrachten wir nur noch lineare Abbildungen des $\mathbb{R}^n$ in sich. Diese lassen sich in einfacher Weise durch Matrizen beschreiben. Es wurde bereits erwähnt, daß mit einer festen $n \times n$-Matrix $A$ die Abbildung $\mathbf{x} \mapsto A\mathbf{x}$ linear ist. Jede lineare Abbildung des $\mathbb{R}^n$ sieht so aus!

## Satz 6.1. Darstellung einer linearen Abbildung in der natürlichen Basis.

Gegeben sei eine lineare Abbildung $f: \mathbb{R}^{n} \to \mathbb{R}^{n}$. Mit der Matrix $F = (f(\mathbf{e}_{1}), \ldots, f(\mathbf{e}_{n}))$, deren Spalten aus den Bildern der natürlichen Basisvektoren bestehen, gilt

$$
f (\mathbf {x}) = F \mathbf {x}.
$$

Man nennt F die Abbildungsmatrix von f bezüglich der natürlichen Basis.

Beweis. Für  $x = x_{1}e_{1} + \cdots + x_{n}e_{n}$  folgt mit (1) und der Multiplikationsformel (8) aus §2 bereits die Behauptung:  $f(\mathbf{x}) = x_{1}f(\mathbf{e}_{1}) + \cdots + x_{n}f(\mathbf{e}_{n}) = F\mathbf{x}$ . ☐

Man beachte: Wegen $A = (A\mathbf{e}_1, A\mathbf{e}_2, \ldots, A\mathbf{e}_n)$ ist die Matrix $A \in \mathbb{R}^{n \times n}$ die Abbildungsmatrix der linearen Abbildung $l : \mathbb{R}^n \to \mathbb{R}^n$, $l(\mathbf{x}) = A\mathbf{x}$, bzgl. der natürlichen Basis. Die Darstellung in einer anderen Basis erfolgt in 6.4.

Beispiel. Die Abbildung $f:\mathbb{R}^{3}\to\mathbb{R}^{3}$, $f((x,y,z)^{T})=(x,y+2z,z)^{T}$ ist linear, sie besitzt bezüglich $(\mathbf{e}_{1},\mathbf{e}_{2},\mathbf{e}_{3})$ die Abbildungsmatrix

$$
F = (f (\mathbf {e} _ {1}), f (\mathbf {e} _ {2}), f (\mathbf {e} _ {3})) = \left( \begin{array}{c c c} 1 & 0 & 0 \\ 0 & 1 & 2 \\ 0 & 0 & 1 \end{array} \right), \text {d.h.} f (\mathbf {x}) = \left( \begin{array}{c c c} 1 & 0 & 0 \\ 0 & 1 & 2 \\ 0 & 0 & 1 \end{array} \right) \mathbf {x}.
$$

f beschreibt eine Scherung des  $R^{3}$ , bei der alle Vektoren mit z = 0 auf sich abgebildet werden. Allgemein bezeichnet man die lineare Abbildung

$$
f: \mathbb {R} ^ {3} \to \mathbb {R} ^ {3}, f (\mathbf {x}) = \mathbf {x} + (\mathbf {b} \cdot \mathbf {x}) \mathbf {a},
$$

als Scherung in Richtung a senkrecht zu b, wenn a, b zwei Vektoren des  $R^{3}$  mit  $a \cdot b = 0$  bezeichnen. Die Abbildungsmatrix lautet  $E + ab^{T}$ . ☐

![](images/page_329_image_8.jpg)

<details>
<summary>text_image</summary>

b
Δ x (b·x) a
f(x)
a
</details>

Abb. 148 - Scherung

Sind $f, g: \mathbb{R}^n \to \mathbb{R}^n$ lineare Abbildungen mit den Abbildungsmatrizen $F = (f(\mathbf{e}_1), \ldots, f(\mathbf{e}_n))$, $G = (g(\mathbf{e}_1), \ldots, g(\mathbf{e}_n))$, dann gehört zur zusammengesetzten linearen Abbildung $f \circ g: \mathbb{R}^n \to \mathbb{R}^n$, $(f \circ g)(\mathbf{x}) = f(g(\mathbf{x}))$ (erst $g$, dann $f$ anwenden), die Abbildungsmatrix $FG$ (das Matrizenprodukt). Denn nach Satz 6.1 gilt $f(g(\mathbf{x})) = Fg(\mathbf{x}) = F(G\mathbf{x}) = (FG)\mathbf{x}$. Ebenso verifiziert man sofort, daß zu $f + g$ und $\alpha f$ die Abbildungsmatrizen $F + G$ und $\alpha F$ gehören.

Eine lineare Abbildung $f: \mathbb{R}^{n} \to \mathbb{R}^{n}$ heißt invertierbar (oder umkehrbar), wenn es zu jedem $\mathbf{y} \in \mathbb{R}^{n}$ genau ein $\mathbf{x} \in \mathbb{R}^{n}$ gibt mit $f(\mathbf{x}) = \mathbf{y}$ (vgl. Kap. 1, §1). Man sieht sofort wegen $f(\mathbf{x}) = F\mathbf{x}$, daß $f$ genau dann invertierbar ist, wenn die Abbildungsmatrix $F$ invertierbar ist. In diesem Fall hat die zu $f$ inverse Abbildung $f^{-1}: \mathbb{R}^{n} \to \mathbb{R}^{n}$ ($f(\mathbf{x})$ wird unter $f^{-1}$ wieder auf $\mathbf{x}$ abgebildet) die Abbildungsmatrix $F^{-1}$; d.h. $f^{-1}(\mathbf{x}) = F^{-1}\mathbf{x}$.

Geometrische Eigenschaften der linearen Abbildung $f:\mathbb{R}^{n}\to\mathbb{R}^{n}$ spiegeln sich in algebraischen Eigenschaften der Abbildungsmatrix $F$, $f(\mathbf{x})=F\mathbf{x}$, wieder:

Die Änderung des Volumens. Zu n Vektoren  $b_{1},\ldots,b_{n}$  des  $R^{n}$  bezeichnet man die Menge aller Linearkombinationen

$$
\lambda_ {1} \mathbf {b} _ {1} + \dots + \lambda_ {n} \mathbf {b} _ {n} \quad \text {mit} \quad 0 \leq \lambda_ {i} \leq 1 (i = 1, \dots , n)
$$

als $n$-Spat (mit den Kanten $\mathbf{b}_{1},\ldots,\mathbf{b}_{n}$). Ein 2-Spat ist ein (evtl. ausgeartetes) Parallelogramm, ein 3-Spat mit linear unabhängigen Kanten stellt einen „gewöhnlichen“ Spat dar. In Übereinstimmung mit den Verhältnissen in $\mathbb{R}^{2}$, $\mathbb{R}^{3}$ ($\rightarrow$ §5.1) nennt man $V = |\det(\mathbf{b}_{1},\ldots,\mathbf{b}_{n})|$ das Volumen des von $\mathbf{b}_{1},\ldots,\mathbf{b}_{n}$ aufgespannten $n$-Spats.

Unter einer linearen Abbildung  $f : R^{n} \rightarrow R^{n}$  mit der Abbildungsmatrix F wird der von $\mathbf{b}_{1},\ldots,\mathbf{b}_{n}\in\mathbb{R}^{n}$ aufgespannte $n$-Spat abgebildet auf den $n$-Spat mit den Kanten $f(\mathbf{b}_{1}),\ldots,f(\mathbf{b}_{n})$. Wegen $f(\mathbf{b}_{i})=F\mathbf{b}_{i}$ und den Formeln (8, §2), (6, §5) ergibt sich für das Volumen $V_{1}$ des Bildspats

$$
\begin{array}{l} V _ {1} = | \det (f (\mathbf {b} _ {1}), \dots , f (\mathbf {b} _ {n})) | = | \det (F \mathbf {b} _ {1}, \dots , F \mathbf {b} _ {n}) | \\ = | \det F (\mathbf {b} _ {1}, \dots , \mathbf {b} _ {n}) | = | \det F \det (\mathbf {b} _ {1}, \dots , \mathbf {b} _ {n}) | = | \det F | \cdot V. \\ \end{array}
$$

Demnach ist $|\det F|$ der Volumenverzerrungsfaktor der linearen Abbildung $f$. Man nennt $f$ volumentreu, wenn $|\det F| = 1$ gilt. Die im obigen Beispiel betrachtete Scherung ist volumentreu ($\rightarrow$ §5, Aufg. 6).

## 6.3 Längen und Winkel im $\mathbb{R}^{n}$; Orthogonalität.

Definition. Seien $\mathbf{x},\mathbf{y}\in \mathbb{R}^n$ , $\mathbf{x} = (x_1,\dots,x_n)^T$ , $\mathbf{y} = (y_{1},\dots,x_{n})^{T}$ . Die Zahl

$$
\mathbf {x} \cdot \mathbf {y} := \mathbf {x} ^ {T} \mathbf {y} = x _ {1} y _ {1} + x _ {2} y _ {2} + \dots + x _ {n} y _ {n}
$$

heißt Skalarprodukt (oder inneres Produkt) der Vektoren x, y, und

$$
| \mathbf {x} | := \sqrt {\mathbf {x} \cdot \mathbf {x}} = \sqrt {x _ {1} ^ {2} + x _ {2} ^ {2} + \cdots + x _ {n} ^ {2}}
$$

heißt Betrag (oder Länge) des Vektors x.

x ist normiert (oder Einheitsvektor), wenn  $|x| = 1$ .

Beispiele. $\mathbf{x} = \begin{pmatrix} 2 \\ 0 \\ 1 \\ 4 \end{pmatrix}, \mathbf{y} = \begin{pmatrix} -1 \\ 3 \\ 5 \\ -3 \end{pmatrix} \Rightarrow \mathbf{x} \cdot \mathbf{y} = 2 \cdot (-1) + 0 \cdot 3 + 1 \cdot 5 + 4 \cdot (-3) = -9,$

$|x| = \sqrt{2^2 + 1^2 + 4^2} = \sqrt{21} \approx 4.582576$, $|y| = \sqrt{1 + 9 + 25 + 9} \approx 6.633250$. Die Vektoren $e_i$ der natürlichen Basis sind Einheitsvektoren; zu jedem Vektor $x \neq 0$ ist $\frac{1}{|x|}x$ normiert.

Rechenregeln (wie in $\mathbb{R}^2$, $\mathbb{R}^3$): Für alle $\mathbf{x}, \mathbf{y}, \mathbf{z} \in \mathbb{R}^n$ und alle $\alpha \in \mathbb{R}$ gilt:

a)  $x \cdot y = y \cdot x$ ,

b) $\alpha (\mathbf{x}\cdot \mathbf{y}) = (\alpha \mathbf{x})\cdot \mathbf{y} = \mathbf{x}\cdot (\alpha \mathbf{y}),$

c) $\mathbf{x} \cdot (\mathbf{y} + \mathbf{z}) = \mathbf{x} \cdot \mathbf{y} + \mathbf{x} \cdot \mathbf{z}$,

d) $\mathbf{x} \cdot \mathbf{x} > 0$ für alle $\mathbf{x} \neq \mathbf{0}$, (3)

e)  $|x| = 0 \iff x = 0$ ,

f) $|\alpha \mathbf{x}| = |\alpha ||\mathbf{x}|$,

g)  $|x \cdot y| \leq |x||y|$  (CAUCHY-SCHWARZsche Ungleichung),

h) $|\mathbf{x} + \mathbf{y}| \leq |\mathbf{x}| + |\mathbf{y}|$ (Dreiecksungleichung).

Beweis g): Die Ungleichung ist erfüllt für $\mathbf{y} = \mathbf{0}$. Sei also $\mathbf{y} \neq \mathbf{0}$. Für alle $\lambda \in \mathbb{R}$ folgt aus a)-d) $0 \leq (\mathbf{x} - \lambda \mathbf{y}) \cdot (\mathbf{x} - \lambda \mathbf{y}) = \mathbf{x} \cdot \mathbf{x} - 2\lambda (\mathbf{x} \cdot \mathbf{y}) + \lambda^2 \mathbf{y} \cdot \mathbf{y}$.

Die Wahl $\lambda = \frac{\mathbf{x} \cdot \mathbf{y}}{|\mathbf{y}|^2}$ ergibt $0 \leq (\mathbf{x} \cdot \mathbf{x})(\mathbf{y} \cdot \mathbf{y}) - (\mathbf{x} \cdot \mathbf{y})^2$, das ist die Behauptung. h): Mit g) folgt

$$
\begin{array}{l} | \mathbf {x} + \mathbf {y} | ^ {2} = (\mathbf {x} + \mathbf {y}) \cdot (\mathbf {x} + \mathbf {y}) = | \mathbf {x} | ^ {2} + 2 \mathbf {x} \cdot \mathbf {y} + | \mathbf {y} | ^ {2} \\ \leq | \mathbf {x} | ^ {2} + 2 | \mathbf {x} | | \mathbf {y} | + | \mathbf {y} | ^ {2} = (| \mathbf {x} | + | \mathbf {y} |) ^ {2}. \\ \end{array}
$$

Aufgrund der Ungleichung (3g) gilt für  $x \neq 0$ ,  $y \neq 0$  stets  $-1 \leq \frac{x \cdot y}{|x||y|} \leq 1$ , deshalb gibt es genau einen Winkel  $\varphi$  mit  $0 \leq \varphi \leq \pi$  und  $\cos \varphi = \frac{x \cdot y}{|x||y|}$ .

Definition. Für $\mathbf{x},\mathbf{y}\neq\mathbf{0}$ nennt man $\nmid(\mathbf{x},\mathbf{y}):=\varphi=\arccos\frac{\mathbf{x}\cdot\mathbf{y}}{|\mathbf{x}||\mathbf{y}|}\quad(0\leq\varphi\leq\pi)$ den Winkel zwischen $\mathbf{x}$ und $\mathbf{y}$. Ferner nennt man $\mathbf{x},\mathbf{y}\in\mathbb{R}^{n}$ orthogonal, wenn $\mathbf{x}\cdot\mathbf{y}=0$ gilt. Der Nullvektor ist orthogonal zu allen Vektoren des $\mathbb{R}^{n}$.

## Definition.

a) Eine lineare Abbildung $f: \mathbb{R}^{n} \to \mathbb{R}^{n}$ heißt orthogonal, wenn sie das Skalarprodukt invariant läßt; d.h. wenn für alle $\mathbf{x}, \mathbf{y} \in \mathbb{R}^{n}$ gilt:

$$
f (\mathbf {x}) \cdot f (\mathbf {y}) = \mathbf {x} \cdot \mathbf {y}.
$$

b) Eine Matrix $A \in \mathbb{R}^{n \times n}$ heißt orthogonal, wenn gilt:

$$
A ^ {T} A = E \quad (\text {also} A ^ {T} = A ^ {- 1}).
$$

c) Eine Basis $B = (\mathbf{b}_1, \ldots, \mathbf{b}_n)$ heißt orthogonal, wenn die Vektoren $\mathbf{b}_i$ paarweise orthogonal sind; d.h., wenn für $i \neq j$ gilt

$$
\mathbf {b} _ {i} \cdot \mathbf {b} _ {j} = 0.
$$

Die Basis B heißt orthonormal, wenn sie orthogonal ist und alle Basisvektoren normiert sind; d.h.,

$$
\mathbf {b} _ {i} \cdot \mathbf {b} _ {j} = 0 \quad f u r \quad i \neq j \quad \text {und} \quad | \mathbf {b} _ {i} | = 1.
$$

## Beispiele.

1. Die natürliche Basis  $(\mathbf{e}_{1},\ldots,\mathbf{e}_{n})$  ist eine Orthonormalbasis des  $R^{n}$ .
2. Sind $\mathbf{a},\mathbf{b}\in\mathbb{R}^{3}$ orthonormal, $\mathbf{a}\cdot\mathbf{b}=0$, $|\mathbf{a}|=|\mathbf{b}|=1$, dann ist $(\mathbf{a},\mathbf{b},\mathbf{c})$ mit $\mathbf{c}:=\mathbf{a}\times\mathbf{b}$ stets eine orthonormales Rechtssystem des $\mathbb{R}^{3}$ ($\rightarrow$ Kap. 1, §4).

Den Zusammenhang zwischen diesen drei Orthogonalitätsbegriffen klärt

Satz 6.2. Für eine Matrix $A \in \mathbb{R}^{n \times n}$ sind äquivalent:

a) A ist orthogonal.
b)  $(Ax)\cdot(Ay)=\mathbf{x}\cdot\mathbf{y}$  für alle  $x,y\in R^{n}$ .
c) Die Spalten von A bilden eine orthonormale Basis des $\mathbb{R}^{n}$.

Insbesondere ist eine lineare Abbildung $f: \mathbb{R}^{n} \to \mathbb{R}^{n}$ genau dann orthogonal, wenn die Abbildungsmatrix $F = (f(\mathbf{e}_{1}), \ldots, f(\mathbf{e}_{n}))$ orthogonal ist.

Beweis. a) $\Rightarrow$ b): Aus $A^T A = E$ folgt

$$
(A \mathbf {x}) \cdot (A \mathbf {y}) = (A \mathbf {x}) ^ {T} (A \mathbf {y}) = \mathbf {x} ^ {T} A ^ {T} A \mathbf {y} = \mathbf {x} ^ {T} E \mathbf {y} = \mathbf {x} ^ {T} \mathbf {y} = \mathbf {x} \cdot \mathbf {y}.
$$

b) $\Rightarrow$ c): Für $\mathbf{x} = \mathbf{e}_i$, $\mathbf{y} = \mathbf{e}_j$ und $\mathbf{a}_i := A\mathbf{e}_i$ (i-te Spalte von $A$) ergibt sich

$$
\mathbf {a} _ {i} \cdot \mathbf {a} _ {j} = \mathbf {e} _ {i} ^ {T} \mathbf {e} _ {j} = \left\{ \begin{array}{l l} 1 & , \text {falls} i = j \\ 0 & , \text {falls} i \neq j \end{array} \right..
$$

c) $\Rightarrow$ a): Aus $\mathbf{a}_i \cdot \mathbf{a}_i = \mathbf{a}_i^T \mathbf{a}_i = 1$ und $\mathbf{a}_i \cdot \mathbf{a}_j = \mathbf{a}_i^T \mathbf{a}_j = 0$ (falls $i \neq j$) folgt mit der Produktformel (4, §2) für die Matrix $A$ die Gleichung $A^T A = E$.

## Bemerkungen.

1. Für eine orthogonale Matrix $A$ ist die Inverse sehr einfach zu berechnen. Es gilt (definitionsgemäß!) $A^{-1} = A^{T}$.

2. $A^T A = E \iff AA^T = E$ ($\rightarrow$ (10), §2) $\iff$ Die Zeilen von $A$ sind orthogonal; wobei das Skalarprodukt (und jeder damit verbundene Begriff) für Zeilenvektoren $\mathbf{x}, \mathbf{y} \in \mathbb{R}_n$ durch $\mathbf{x} \cdot \mathbf{y} := \mathbf{xy}^T$ definiert ist.

3. $A \in \mathbb{R}^{n \times n}$ orthogonal $\Rightarrow$ det $A = \pm 1$.

Denn aus $A^T A = E$ folgt $1 = \det E = \det A^T \det A = (\det A)^2$.

4. Jede orthogonale lineare Abbildung  $f : R^{n} \rightarrow R^{n}$  ist

volumentreu, da  $|\det F| = 1$  (F Abbildungsmatrix von f) ( $\rightarrow$  Bem 3.),

längentreu , da  $|f(\mathbf{x})| = \sqrt{f(\mathbf{x}) \cdot f(\mathbf{x})} = \sqrt{\mathbf{x} \cdot \mathbf{x}} = |\mathbf{x}|$ ,

winkeltreu , da  $\cos\angle(f(\mathbf{x}),f(\mathbf{y}))=\frac{f(\mathbf{x})\cdot f(\mathbf{y})}{|f(\mathbf{x})||f(\mathbf{y})|}=\frac{\mathbf{x}\cdot\mathbf{y}}{|\mathbf{x}||\mathbf{y}|}=\cos\angle(\mathbf{x},\mathbf{y})$ .

6.4 Speziell: Spiegelungen und Drehungen sind neben den Parallelverschiebungen die wichtigsten längentreuen Abbildungen. Sie sind nur dann linear, wenn sie den Ursprung auf sich abbilden.

(a) Spiegelungen im Raum. Dazu gehört die Punktspiegelung $s: \mathbf{x} \mapsto -\mathbf{x}$ mit der Matrix $S = -E$. Interessanter sind jedoch die Spiegelungen an Ebenen durch den Ursprung:

Ist $\mathbf{a} = (a_{1}, a_{2}, a_{3})^{T}$ ein Einheitsvektor, dann lautet die Spiegelung an der Ebene $\mathbf{a} \cdot \mathbf{x} = 0$:

$$
s: \mathbb {R} ^ {3} \to \mathbb {R} ^ {3}, s (\mathbf {x}) = \mathbf {x} - 2 (\mathbf {x} \cdot \mathbf {a}) \mathbf {a}.
$$

Man bestätigt leicht $s(\mathbf{x})\cdot s(\mathbf{y}) = \mathbf{x}\cdot \mathbf{y}$ und $s(s(\mathbf{x})) = \mathbf{x}$, daher ist die Abbildungsma-trix $S$ wegen $S^{-1} = S = S^T$ stets eine symmetrische und orthogonale Matrix:

![](images/page_332_image_21.jpg)

<details>
<summary>text_image</summary>

a
x
-(x·a)a
S(x)
</details>

Abb. 149 - Spiegelung im $\mathbb{R}^3$

$$
S = (s (\mathbf {e} _ {1}), s (\mathbf {e} _ {2}), s (\mathbf {e} _ {3})) = \left( \begin{array}{c c c} 1 - 2 a _ {1} ^ {2} & - 2 a _ {2} a _ {1} & - 2 a _ {3} a _ {1} \\ - 2 a _ {1} a _ {2} & 1 - 2 a _ {2} ^ {2} & - 2 a _ {3} a _ {2} \\ - 2 a _ {1} a _ {3} & - 2 a _ {2} a _ {3} & 1 - 2 a _ {3} ^ {2} \end{array} \right) = E - 2 \mathbf {a} \mathbf {a} ^ {T}.
$$

Für diese Spiegelungen im $\mathbb{R}^{3}$ gilt det $S = -1$ ($\rightarrow$ §5, Aufg. 6).

⑥ Drehungen der Ebene um den Nullpunkt lauten in kartesischen Koordinaten

$$
d: \mathbb {R} ^ {2} \rightarrow \mathbb {R} ^ {2}, \quad d \binom{x}{y} = \binom{x \cos \varphi - y \sin \varphi}{x \sin \varphi + y \cos \varphi}, \quad \text {Drehwinkel} \varphi ,
$$

(→ Kap. 1, §3.4). Die Abbildung d ist linear mit der orthogonalen Abbildungsmatrix (der „Drehmatrix“)

$$
D = \left( \begin{array}{c c} \cos \varphi & - \sin \varphi \\ \sin \varphi & \cos \varphi \end{array} \right), \quad \det D = 1.
$$

Wegen $\left( \begin{array}{c}x\cos \varphi -y\sin \varphi \\ x\sin \varphi +y\cos \varphi \end{array} \right) = \cos \varphi \binom{x}{y} + \sin \varphi \binom{-y}{x}$ hat man

$$
d (\mathbf {x}) = (\cos \varphi) \mathbf {x} + (\sin \varphi) \mathbf {x} ^ {*}, \tag {4}
$$

wobei  $x^{*}$  aus x durch eine positive Drehung um  $\frac{\pi}{2}$  entsteht.

© Drehungen im Raum erfolgen stets um eine Achse, diese sog. Drehachse wird durch die Wahl eines Richtungsvektors  $a \neq 0$  (auf der Achse) orientiert. a weist in die positive Achsenrichtung. Blickt man in diese Richtung, dann erfolgt eine positive Drehung (Drehwinkel  $\varphi \geq 0$ ) im Uhrzeigersinn ( $\rightarrow$  Abb. 29). Die Koordinatenachsen eines kartesischen Koordinatensystems sind stets durch die zugehörigen Basisvektoren orientiert.

a) Die Drehung um die x-Achse besitzt wegen (4) die Abbildungsgleichung

$$
d _ {1} (\mathbf {x}) = x \mathbf {e} _ {1} + (y \cos \alpha - z \sin \alpha) \mathbf {e} _ {2} + (y \sin \alpha + z \cos \alpha) \mathbf {e} _ {3}
$$

und die Abbildungsmatrix

$$
D _ {1} (\alpha) = \left( \begin{array}{c c c} 1 & 0 & 0 \\ 0 & \cos \alpha & - \sin \alpha \\ 0 & \sin \alpha & \cos \alpha \end{array} \right) .
$$

Zur Drehung um die y- bzw. z-Achse gehören die Drehmatrizen

$$
D _ {2} (\beta) = \left( \begin{array}{c c c} \cos \beta & 0 & \sin \beta \\ 0 & 1 & 0 \\ - \sin \beta & 0 & \cos \beta \end{array} \right), \quad D _ {3} (\gamma) = \left( \begin{array}{c c c} \cos \gamma & - \sin \gamma & 0 \\ \sin \gamma & \cos \gamma & 0 \\ 0 & 0 & 1 \end{array} \right).
$$

Man kann zeigen, daß sich jede Drehung um eine beliebige Achse durch den Nullpunkt als Hintereinanderausführung von Drehungen um die Koordinatenachsen darstellen läßt, d.h. für ihre Matrix $D$ lassen sich $\alpha$, $\beta$, $\gamma$ bestimmen, so daß $D = D_{3}(\gamma)D_{2}(\beta)D_{1}(\alpha)$ (erst um die $x$-Achse, dann um die $y$-Achse und schließlich um die $z$-Achse drehen). $\alpha$, $\beta$, $\gamma$ heißen die Cardan-Winkel der Drehung (benannt nach CARDANUS, 1501–1576). Die Euler-Winkel der Drehung werden in 6.6 behandelt.

b) Ist von einer Drehung $d: \mathbb{R}^3 \to \mathbb{R}^3$ der Richtungsvektor $\mathbf{a} \neq \mathbf{0}$ der Drehachse (durch den Nullpunkt) und der Drehwinkel $\varphi \geq 0$ bekannt, dann wird $d$ (in kartesischen Koordinaten) dargestellt durch

$$
d (\mathbf {x}) = (\cos \varphi) \mathbf {x} + (1 - \cos \varphi) \frac {\mathbf {x} \cdot \mathbf {a}}{| \mathbf {a} | ^ {2}} \mathbf {a} + \frac {\sin \varphi}{| \mathbf {a} |} \mathbf {a} \times \mathbf {x}. \tag {5}
$$

Beweis. Wir zerlegen  $x = x_{a} + r$  mit der Komponente  $x_{a}$  in Achsenrichtung und  $r = x - x_{a}$ . Der Vektor  $x_{a}$  bleibt bei der Drehung fest, r geht nach (4) über in

$$
d (\mathbf {r}) = (\cos \varphi) \mathbf {r} + (\sin \varphi) \mathbf {r} ^ {*}
$$

mit dem aus r durch eine (positive) Drehung um $\frac{\pi}{2}$ gewonnenen Vektor $\mathbf{r}^{*} = \frac{1}{|\mathbf{a}|} \mathbf{a} \times \mathbf{r}$. Mit $d(\mathbf{x}) = \mathbf{x}_{\mathbf{a}} + d(\mathbf{r})$ folgt (5) aus Formel (6, Kap 1., §5). □

![](images/page_334_image_6.jpg)

<details>
<summary>text_image</summary>

a
φ
x
d(x)
r = x - (a·x) a
r* = a × x
</details>

Abb. 150 - Drehung im $\mathbb{R}^3$, $|a| = 1$

Die Abbildungsmatrix (die Drehmatrix) $D$ bezüglich der gegebenen kartesi- schen Basis lautet (mit $\mathbf{a} = (a_1, a_2, a_3)^T$ und $|\mathbf{a}| = 1$):

$$
\left( \begin{array}{c} \cos \varphi + (1 - \cos \varphi) a _ {1} ^ {2}, \quad (1 - \cos \varphi) a _ {1} a _ {2} - a _ {3} \sin \varphi , (1 - \cos \varphi) a _ {1} a _ {3} + a _ {2} \sin \varphi \\ (1 - \cos \varphi) a _ {1} a _ {2} + a _ {3} \sin \varphi , \quad \cos \varphi + (1 - \cos \varphi) a _ {2} ^ {2}, \quad (1 - \cos \varphi) a _ {2} a _ {3} - a _ {1} \sin \varphi \\ (1 - \cos \varphi) a _ {1} a _ {3} - a _ {2} \sin \varphi , (1 - \cos \varphi) a _ {2} a _ {3} + a _ {1} \sin \varphi , \quad \cos \varphi + (1 - \cos \varphi) a _ {3} ^ {2} \end{array} \right)
$$

Da die aus $\mathbf{e}_{1}$, $\mathbf{e}_{2}$, $\mathbf{e}_{3}$ durch Drehung entstandenen Vektoren $\mathbf{e}_{1}^{\prime}=d(\mathbf{e}_{1})$, $\mathbf{e}_{2}^{\prime}=d(\mathbf{e}_{2})$, $\mathbf{e}_{3}^{\prime}=d(\mathbf{e}_{3})$ ebenfalls eine kartesische Basis bilden, gilt sicher „$\Rightarrow$“ in der Charakterisierung

$$
D \text {ist Drehmatrix} \quad \Longleftrightarrow \quad D ^ {T} D = E \text {und} \det D = 1.
$$

Die Aussage „←“, daß jede orthogonale  $3 \times 3$ -Matrix D mit det D = 1 eine Drehung beschreibt, wird erst in 6.8 gezeigt werden.

Ist eine Drehmatrix $D = (d_{ij}) \neq E$ vorgegeben, so findet man aus obiger Matrixdarstellung zu (5) den Drehwinkel $\varphi \geq 0$ mit der Formel

$$
\cos \varphi = \frac {1}{2} (\text {Spur} D - 1), \text {Spur} D := d _ {1 1} + d _ {2 2} + d _ {3 3}. \tag {6}
$$

Die Drehachsenrichtung $\mathbf{a} = (a_{1}, a_{2}, a_{3})^{T}$, $|\mathbf{a}| = 1$, ergibt sich aus

$$
\mathbf {a} = \frac {1}{2 \sin \varphi} \left( \begin{array}{l} d _ {3 2} - d _ {2 3} \\ d _ {1 3} - d _ {3 1} \\ d _ {2 1} - d _ {1 2} \end{array} \right), \text {falls} \varphi \neq \pi . \tag {7}
$$

$$
\boxed { \begin{array}{l} (D - E) \mathbf {a} = \mathbf {0} \text {oder explizit} \\ \mathbf {a} = \frac {1}{2 \sin \varphi} \left( \begin{array}{c} d _ {3 2} - d _ {2 3} \\ d _ {1 3} - d _ {3 1} \\ d _ {2 1} - d _ {1 2} \end{array} \right), \text {falls} \varphi \neq \pi . \end{array} }
$$

Beispiel. Nach einer Drehung um die x-Achse mit  $\alpha=\frac{\pi}{6}$  wird noch um die z-Achse mit  $\gamma=\frac{\pi}{4}$  gedreht. Zur resultierenden Abbildung gehört die Abbildungsmatrix

$$
D = D _ {3} (\frac {\pi}{4}) D _ {1} (\frac {\pi}{6}) = \frac {1}{2} \left( \begin{array}{c c c} \sqrt {2} & - \frac {1}{2} \sqrt {6} & \frac {1}{2} \sqrt {2} \\ \sqrt {2} & \frac {1}{2} \sqrt {6} & - \frac {1}{2} \sqrt {2} \\ 0 & 1 & \sqrt {3} \end{array} \right) .
$$

So wird beispielsweise der Punkt $P = (1, 1, 1)$ - genauer: der Ortsvektor $\overrightarrow{OP} = \begin{pmatrix} 1 \\ 1 \\ 1 \end{pmatrix}$ - abgebildet auf $P' = (x', y', z')$ mit

$$
\left( \begin{array}{c} x ^ {\prime} \\ y ^ {\prime} \\ z ^ {\prime} \end{array} \right) = D \left( \begin{array}{c} 1 \\ 1 \\ 1 \end{array} \right) = \left( \begin{array}{c} \frac {1}{4} (3 \sqrt {2} - \sqrt {6}) \\ \frac {1}{4} (\sqrt {2} + \sqrt {6}) \\ \frac {1}{2} (\sqrt {3} + 1) \end{array} \right) .
$$

Mit den Drehmatrizen $D_{3}$, $D_{1}$ ist auch $D$ orthogonal und es gilt det $D = 1$. Nach dem noch zu beweisenden Satz ($\rightarrow$ 6.8) stellt deshalb $D$ eine Drehung dar, deren Drehwinkel $\varphi \geq 0$ mit (6) zu bestimmen ist:

$$
\cos \varphi = \frac {1}{2} (\text {Spur} D - 1) = \frac {1}{2} (\frac {1}{2} \sqrt {2} + \frac {1}{4} \sqrt {6} + \frac {1}{2} \sqrt {3} - 1),
$$

also $\varphi = 53.64743528^{\circ}$ ， $\sin \varphi = 0.805384813$

Aus (7) liest man die Achsenrichtung ab:

$$
\mathbf {a} = (0. 5 2 9 9 0 4 0 7 5, 0. 2 1 9 4 9 3 4 5 4, 0. 8 1 9 1 6 0 7 2 5) ^ {T}.
$$

6.5 Das Schmidtsche Orthonormierungsverfahren (E. SCHMIDT, 1876-1959) ermöglicht den Übergang von einer beliebigen Basis zu einer günstigen Orthonormalbasis.

Wir gehen aus von linear unabhängigen Vektoren $\mathbf{b}_{1},\ldots,\mathbf{b}_{k}\in\mathbb{R}^{n}\ (k\leq n)$ und berechnen daraus der Reihe nach eine Orthonormalbasis $\mathbf{c}_{1},\ldots,\mathbf{c}_{k}$ der linearen Hülle Lin $(\mathbf{b}_{1},\ldots,\mathbf{b}_{k})$.

Man setzt $\mathbf{c}_1 := \frac{1}{|\mathbf{b}_1|} \mathbf{b}_1$ und berechnet die zu $\mathbf{c}_1$ orthogonale Komponente $\mathbf{c}_2' = \mathbf{b}_2 - (\mathbf{b}_2 \cdot \mathbf{c}_1)\mathbf{c}_1$ von $\mathbf{b}_2$. Normierung ergibt $\mathbf{c}_2 := \frac{1}{|\mathbf{c}_2'|} \mathbf{c}_2'$. Weiter wird nun der zu $\mathbf{c}_1$ und $\mathbf{c}_2$ orthogonale Vektor $\mathbf{c}_3' = \mathbf{b}_3 - (\mathbf{b}_3 \cdot \mathbf{c}_2)\mathbf{c}_2 - (\mathbf{b}_3 \cdot \mathbf{c}_1)\mathbf{c}_1$ berechnet und normiert: $\mathbf{c}_3 := \frac{1}{|\mathbf{c}_3'|} \mathbf{c}_3'$.

![](images/page_335_image_14.jpg)

<details>
<summary>text_image</summary>

b₁
c₁
c₂
c₂'
b₂
</details>

Abb. 151 - Orthonormierung in $\mathbb{R}^2$

Etc.: $\mathbf{c}_4' = \mathbf{b}_4 - (\mathbf{b}_4 \cdot \mathbf{c}_3)\mathbf{c}_3 - (\mathbf{b}_4 \cdot \mathbf{c}_2)\mathbf{c}_2 - (\mathbf{b}_4 \cdot \mathbf{c}_1)\mathbf{c}_1$, $\mathbf{c}_4 := \frac{1}{|\mathbf{c}_4'|}\mathbf{c}_4, \ldots,$

bis $\mathbf{c}_k^{\prime} = \mathbf{b}_k - \sum_{i=1}^{k-1} (\mathbf{b}_k \cdot \mathbf{c}_i) \mathbf{c}_i$, $\mathbf{c}_k = \frac{1}{|\mathbf{c}_k'|} \mathbf{c}_k^{\prime}$.

In jedem Schritt wird ein zu den vorher berechneten  $c_{i}$  orthogonaler Vektor vom Betrag 1 bestimmt und man sieht leicht, daß  $c_{1},\ldots,c_{k}\in\operatorname{Lin}(\mathbf{b}_{1},\ldots,\mathbf{b}_{k})$  linear unabhängig sind.

Bemerkungen. 1. Ein Beispiel und eine Anwendung dieses Verfahrens behandeln wir in 7.2.

2. Für eine invertierbare $n \times n$-Matrix $B = (\mathbf{b}_1, \ldots, \mathbf{b}_n)$ ergibt das Orthonormierungsverfahren (für $\mathbf{b}_1, \ldots, \mathbf{b}_n$) die Zerlegung $Q = BR$, bzw. $B = QR^{-1}$, mit der orthogonalen Matrix $Q = (\mathbf{c}_1, \ldots, \mathbf{c}_n)$ und einer oberen Dreiecksmatrix $R$. Diese sog. $QR$-Zerlegung wird in vielen numerischen Verfahren bevorzugt, da die Transformation $\mathbf{x} \mapsto Q\mathbf{x}$ längentreu ist.

6.6 Basiswechsel, Koordinatentransformation. Es ist zu unterscheiden zwischen den Koordinaten eines Vektors bezüglich einer Basis und den Koordinaten eines Punktes in einem affinen Koordinatensystem.

(a) Vektorkoordinaten. Sei $B = (\mathbf{b}_1, \ldots, \mathbf{b}_n)$ eine (beliebige) Basis des $\mathbb{R}^n$, die wir gleichzeitig als invertierbare $n \times n$-Matrix ansehen. Die eindeutig bestimmten Koeffizienten $x_i' \in \mathbb{R}$ der Zerlegung $\mathbf{x} = x_1' \mathbf{b}_1 + \cdots + x_n' \mathbf{b}_n$ heißen Koordinaten des Vektors $\mathbf{x} \in \mathbb{R}^n$, und man nennt

$$
\mathbf {x} _ {B} = \mathbf {x} ^ {\prime} = \left( \begin{array}{c} x _ {1} ^ {\prime} \\ x _ {2} ^ {\prime} \\ \vdots \\ x _ {n} ^ {\prime} \end{array} \right), \quad \text {falls} \mathbf {x} = x _ {1} ^ {\prime} \mathbf {b} _ {1} + \dots + x _ {n} ^ {\prime} \mathbf {b} _ {n},
$$

den Koordinatenvektor von $\mathbf{x} \in \mathbb{R}^{n}$ bezüglich $B$. Die Koordinatenabbildung $\mathbf{x} \mapsto \mathbf{x}_{B}$ ist linear ($\rightarrow$ 6.1). Aus der nützlichen Multiplikationsformel (8, §2) ergibt sich sofort

$$
x _ {1} ^ {\prime} \mathbf {b} _ {1} + \dots + x _ {n} ^ {\prime} \mathbf {b} _ {n} = B \left( \begin{array}{c} x _ {1} ^ {\prime} \\ \vdots \\ x _ {n} ^ {\prime} \end{array} \right) = B \mathbf {x} _ {B}.
$$

Damit gilt für die Koordinatentransformation beim

$$
\begin{array}{l} \text {Basiswechsel von} (\mathbf {e} _ {1}, \dots , \mathbf {e} _ {n}) \text {nach} B = (\mathbf {b} _ {1}, \dots , \mathbf {b} _ {n}): \\ \text {Substitutionsformel:} \quad \mathbf {x} = B \mathbf {x} _ {B}, \\ \text {Transformationsformel:} \quad \mathbf {x} _ {B} = B ^ {- 1} \mathbf {x} \quad (\mathbf {x}, \mathbf {x} _ {B} \in \mathbb {R} ^ {n}). \end{array} \tag {8}
$$

Beispiel. Die Euler-Winkel  $\psi$ ,  $\theta$ ,  $\varphi$  einer Drehung des  $R^{3}$  sind ( $\rightarrow$  Abb. 152) durch drei Drehungen vom Typ  $D_{1}$  und  $D_{3}$  erklärt:

① Drehung um die  $x_{3}$ -Achse mit Winkel  $\psi$ ,
② Drehung um das Bild der  $x_{1}$ -Achse mit Winkel  $\theta$ ,
③. Drehung um das Bild der  $x_{3}$ -Achse mit Winkel  $\varphi$ .

Im Gegensatz zu den Cardan-Winkeln (→ 6.4, Beisp. 3) ist diese Bestimmung nicht auf ein ortsfestes, sondern im 2. und 3. Schritt auf ein gedrehtes Koordinatensystem bezogen. In diesem Falle stellt man einen festen Vektor x durch seine Koordinatenvektoren x', x'', x''' in den 3 gedrehten Basen dar und erhält mit (8)

![](images/page_337_image_3.jpg)

<details>
<summary>text_image</summary>

x₃
x₃′′
x₂′′
θ
O
φ
x₁′′
x₁
x₂
</details>

Abb. 152 - Euler-Winkel

$$
\text {①.} \mathbf {x} = D _ {3} (\psi) \mathbf {x} ^ {\prime}, \quad \text {②.} \mathbf {x} ^ {\prime} = D _ {1} (\theta) \mathbf {x} ^ {\prime \prime}, \quad \text {③.} \mathbf {x} ^ {\prime \prime} = D _ {3} (\varphi) \mathbf {x} ^ {\prime \prime \prime}.
$$

Setzt man ③. in ②. und ②. in ①. ein, so folgt

$$
\mathbf {x} = D _ {3} (\psi) D _ {1} (\theta) D _ {3} (\varphi) \mathbf {x} ^ {\prime \prime \prime}.
$$

Dies ist die Substitutionsformel (8) für die durch $d$ gedrehte Basis. In der Basis $\mathbf{e}_1$, $\mathbf{e}_2$, $\mathbf{e}_3$ hat daher $d$ die Darstellung $\mathbf{x} \mapsto D_3(\psi)D_1(\psi)D_3(\varphi)\mathbf{x}$ mit der Abbildungsmatrix

$$
\left( \begin{array}{c c c} \cos \psi \cos \varphi - \sin \psi \cos \theta \sin \varphi & - \cos \psi \sin \varphi - \sin \psi \cos \theta \cos \varphi & \sin \psi \sin \theta \\ \sin \psi \cos \varphi + \cos \psi \cos \theta \sin \varphi & - \sin \psi \sin \varphi + \cos \psi \cos \theta \cos \varphi & - \cos \psi \sin \theta \\ \sin \theta \sin \varphi & \sin \theta \cos \varphi & \cos \theta \end{array} \right)  .
$$

⑥ Punktkoordinaten. Begriffe der anschaulichen Geometrie des $\mathbb{R}^{3}$ werden in den $\mathbb{R}^{n}$ übernommen. Die Zeilen-$n$-Tupel $X = (x_{1}, \ldots, x_{n})$, $x_{i} \in \mathbb{R}$, nennt man Punkte des $n$-dimensionalen reellen Punktraumes $\mathbb{R}_{n}$. Zu jedem Punkt $X = (x_{1}, \ldots, x_{n})$ gehört der Vektor $\mathbf{x} = \begin{pmatrix} x_{1} \\ \vdots \\ x_{n} \end{pmatrix} \in \mathbb{R}^{n}$ - und umgekehrt. Ist $P = (p_{1}, \ldots, p_{n})$ ein fester Punkt, dann heißt

$$
\overrightarrow {P X} := \mathbf {x} - \mathbf {p} = \left( \begin{array}{c} x _ {1} - p _ {1} \\ x _ {2} - p _ {2} \\ \vdots \\ x _ {n} - p _ {n} \end{array} \right)
$$

Ortsvektor des Punktes X in bezug auf P. Demnach ist  $x = \overrightarrow{OX}$  der Ortsvektor des Punktes X in bezug auf den Nullpunkt  $\mathbf{0} = (0, \ldots, 0)$ .

Definition. Ein affines Koordinatensystem $K = (P; \mathbf{b}_1, \ldots, \mathbf{b}_n)$ des Punktraumes $\mathbb{R}_n$ besteht aus einem festen Bezugspunkt $P = (p_1, \ldots, p_n)$ und einer Basis $B = (\mathbf{b}_1, \ldots, \mathbf{b}_n)$ des $\mathbb{R}^n$. Die Koordinaten $x_i'$ des Ortsvektors $\overrightarrow{PX}$ bezüglich der Basis $B$,

$$
\overrightarrow {P X} = x _ {1} ^ {\prime} \mathbf {b} _ {1} + \dots + x _ {n} ^ {\prime} \mathbf {b} _ {n},
$$

heißen Koordinaten des Punktes X im Koordinatensystem K; man schreibt  $X_{K} = (x_{1}', \ldots, x_{n}')$ .

![](images/page_338_image_2.jpg)

<details>
<summary>text_image</summary>

e₁
O
e₂
X
b₃
OP
P
b₂
b₁
</details>

Abb. 153 - Affine Koordinaten

Die Definitionen und (8) ergeben

$$
\left( \begin{array}{c} x _ {1} ^ {\prime} \\ x _ {2} ^ {\prime} \\ \vdots \\ x _ {n} ^ {\prime} \end{array} \right) = (\mathbf {x} - \mathbf {p}) _ {B} = B ^ {- 1} \left( \begin{array}{c} x _ {1} - p _ {1} \\ x _ {2} - p _ {2} \\ \vdots \\ x _ {n} - p _ {n} \end{array} \right). \tag {9}
$$

Wir fassen dies für den wichtigen Spezialfall n = 3 noch einmal zusammen:

## Satz 6.3. Koordinatenwechsel im Raum.

Übergang vom kartesischen „Inertialsystem“ $I = (O; \mathbf{e}_1, \mathbf{e}_2, \mathbf{e}_3)$ zum affinen (i.a. schiefwinkligen) Koordinatensystem $K = (P; \mathbf{b}_1, \mathbf{b}_2, \mathbf{b}_3)$.

Ist $P = (p_1, p_2, p_3) \in \mathbb{R}_3$, $(\mathbf{b}_1, \mathbf{b}_2, \mathbf{b}_3) = B \in \mathbb{R}^{3 \times 3}$ die Darstellung bezüglich $I$ und sind $(x_1, x_2, x_3)$ und $(x_1', x_2', x_3')$ die $I$- bzw. $K$-Koordinaten des Punktes $X$, so gilt mit $\mathbf{x} := \begin{pmatrix} x_1 \\ x_2 \\ x_3 \end{pmatrix}$, $\mathbf{x}' := \begin{pmatrix} x_1' \\ x_2' \\ x_3' \end{pmatrix}$ und $\mathbf{p} := \begin{pmatrix} p_1 \\ p_2 \\ p_3 \end{pmatrix}$:

Substitutionsformel:  $x = Bx' + p$ ,

Transformationsformel: $\mathbf{x}' = B^{-1}(\mathbf{x} - \mathbf{p})$.

Bemerkungen. 1. Genügt eine Fläche im $\mathbb{R}^3$ in $I$-Koordinaten der Gleichung $Q(\mathbf{x}) = 0$, so hat sie mit der Substitutionsformel im $K$-System die Darstellung $Q(B\mathbf{x}' + \mathbf{p}) = 0$ ($\rightarrow$ 7.3, 7.4).

2. Bei der Parallelverschiebung des initialen Achsenkreuzes in den neuen Ursprung P erhält X die neuen Koordinaten  $x_{i}^{\prime}=x_{i}-p_{i}\quad(i=1,2,3)$ .
3. Bei der Drehung des Achsenkreuzes mit der Drehmatrix  $D = (D\mathbf{e}_{1}, D\mathbf{e}_{2}, D\mathbf{e}_{3})$  erhält X die neuen Koordinaten

$$
\left( \begin{array}{c} x _ {1} ^ {\prime} \\ x _ {2} ^ {\prime} \\ x _ {3} ^ {\prime} \end{array} \right) = D ^ {- 1} \left( \begin{array}{c} x _ {1} \\ x _ {2} \\ x _ {3} \end{array} \right) = D ^ {T} \left( \begin{array}{c} x _ {1} \\ x _ {2} \\ x _ {3} \end{array} \right) .
$$

Aufgrund dieser Transformationsformel wird von manchen Autoren die Inverse  $D^{-1} = D^{T}$  als Drehmatrix dieser Koordinatentransformation bezeichnet.

Beispiel.  $(\mathbf{e}_{1}^{\prime},\mathbf{e}_{2}^{\prime},\mathbf{e}_{3}^{\prime})$  entstehe aus  $(\mathbf{e}_{1},\mathbf{e}_{2},\mathbf{e}_{3})$  durch die Drehung  $D = D_{3}(\frac{\pi}{4})D_{1}(\frac{\pi}{6})$  ( $\rightarrow$  6.4). Wird das gedrehte Koordinatensystem noch in den Punkt  $P = (1,2,3)$  verschoben, dann hat der Punkt  $X = (x,y,z)$  im neuen Koordinatensystem  $(P;\mathbf{e}_{1}^{\prime},\mathbf{e}_{2}^{\prime},\mathbf{e}_{3}^{\prime})$  die Koordinaten

$$
\left( \begin{array}{c} x ^ {\prime} \\ y ^ {\prime} \\ z ^ {\prime} \end{array} \right) = D ^ {T} \left( \begin{array}{c} x - 1 \\ y - 2 \\ z - 3 \end{array} \right) = \frac {1}{2} \left( \begin{array}{c c c} \sqrt {2} & \sqrt {2} & 0 \\ - \frac {1}{2} \sqrt {6} & \frac {1}{2} \sqrt {6} & 1 \\ \frac {1}{2} \sqrt {2} & - \frac {1}{2} \sqrt {2} & \sqrt {3} \end{array} \right) \left( \begin{array}{c} x - 1 \\ y - 2 \\ z - 3 \end{array} \right),
$$

d.h.

$$
\begin{array}{l} x ^ {\prime} = \frac {1}{2} (\sqrt {2} (x - 1) + \sqrt {2} (y - 2)) \\ y ^ {\prime} = \frac {1}{2} (- \frac {1}{2} \sqrt {6} (x - 1) + \frac {1}{2} \sqrt {6} (y - 2) + (z - 3)) \\ z ^ {\prime} = \frac {1}{2} (\frac {1}{2} \sqrt {2} (x - 1) - \frac {1}{2} \sqrt {2} (y - 2) + \sqrt {3} (z - 3)). \\ \end{array}
$$

(c) Abbildungsmatrix. Zu jeder $n \times n$-Matrix $A$ gehört die lineare Abbildung $f: \mathbb{R}^n \to \mathbb{R}^n$, $f(\mathbf{x}) = A\mathbf{x}$, dabei ist $A$ die Abbildungsmatrix von $f$ bezüglich der natürlichen Basis ($\rightarrow$ Satz 6.1). Der Wechsel zu einer anderen Basis bringt zusätzliche Erkenntnisse:

Definition. Seien $f:\mathbb{R}^{n}\to\mathbb{R}^{n}$ eine lineare Abbildung und $B=(\mathbf{b}_{1},\ldots,\mathbf{b}_{n})$ eine Basis des $\mathbb{R}^{n}$. Die Matrix

$$
C := (f (\mathbf {b} _ {1}) _ {B}, \dots , f (\mathbf {b} _ {n}) _ {B}),
$$

in deren Spalten die Koordinatenvektoren (bzgl. B) der Bilder $f(\mathbf{b}_{i})$ stehen, heißt Abbildungsmatrix von $f$ bezüglich $B$.

Satz 6.4. Die Änderung der Abbildungsmatrix beim Basiswechsel.

Es seien A eine $n \times n$-Matrix und $B = (\mathbf{b}_1, \ldots, \mathbf{b}_n)$ eine Basis des $\mathbb{R}^n$. Die Abbildungsgleichung $\mathbf{y} = A\mathbf{x}$ lautet in Koordinaten bezüglich $B$

$$
\mathbf {y} _ {B} = (A \mathbf {x}) _ {B} = C \mathbf {x} _ {B} \tag {10}
$$

mit der Abbildungsmatrix $C = ((A\mathbf{b}_1)_B, \ldots, (A\mathbf{b}_n)_B)$.

Ferner gilt

$$
C = B ^ {- 1} A B . \tag {11}
$$

Beweis. Aus $\mathbf{x} = \sum_{i=1}^{n} x_i' \mathbf{b}_i$ folgt $(A\mathbf{x})_B = \sum_{i=1}^{n} x_i'(A\mathbf{b}_i)_B = ((A\mathbf{b}_1)_B, \ldots, (A\mathbf{b}_n)_B)\mathbf{x}_B$. Daher ist in (10) $C = ((A\mathbf{b}_1)_B, \ldots, (A\mathbf{b}_n)_B)$ zu setzen. Mit Transformationsformel (8) ergibt sich hieraus $C = (B^{-1} A\mathbf{b}_1, \ldots, B^{-1} A\mathbf{b}_n) = B^{-1} A(\mathbf{b}_1, \ldots, \mathbf{b}_n) = B^{-1} AB$.

Beispiel 1. Sei (→ 6.4, ⓐ) $S \in \mathbb{R}^{3 \times 3}$ die Abbildungsmatrix der Spiegelung $s(\mathbf{x}) = \mathbf{x} - 2(\mathbf{x} \cdot \mathbf{a})\mathbf{a} = S\mathbf{x}$ an der zu $\mathbf{a} \in \mathbb{R}^3$, $|\mathbf{a}| = 1$, orthogonalen Ebene.

Wir gehen über zu einer anderen kartesischen Basis $B = (\mathbf{a}, \mathbf{b}, \mathbf{a} \times \mathbf{b})$ mit einem Einheitsvektor $\mathbf{b}$ orthogonal zu $\mathbf{a}$. Aus

$$
s (\mathbf {a}) = - \mathbf {a}, s (\mathbf {b}) = \mathbf {b}, s (\mathbf {a} \times \mathbf {b}) = \mathbf {a} \times \mathbf {b}
$$

liest man sofort die Abbildungsmatrix $S'$ bezüglich $B$ ab:

$$
S ^ {\prime} = \left( \begin{array}{c c c} - 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{array} \right) .
$$

In Koordinaten bezüglich $B$ wird die Spiegelung einfach durch $\mathbf{y}' = S' \mathbf{x}'$ beschrieben. Ferner gilt $S' = B^{-1} SB$.

Beispiel 2. Wir betrachten die in 6.4, Beispiel 3 behandelte Drehung $d(\mathbf{x}) = D\mathbf{x}$ (mit der $3 \times 3$-Drehmatrix $D$) bezüglich einer kartesischen Basis $B = (\mathbf{a}, \mathbf{b}, \mathbf{c})$ mit dem Einheitsvektor $\mathbf{a}$ in Richtung der Drehachse. Mit (4) gilt

$$
d (\mathbf {a}) = \mathbf {a}, \quad d (\mathbf {b}) = (\cos \varphi) \mathbf {b} + (\sin \varphi) \mathbf {c}, \quad d (\mathbf {c}) = (- \sin \varphi) \mathbf {b} + (\cos \varphi) \mathbf {c}.
$$

Hieraus liest man die Abbildungsmatrix bezüglich B ab:

$$
D ^ {\prime} = \left( \begin{array}{c c c} 1 & 0 & 0 \\ 0 & \cos \varphi & - \sin \varphi \\ 0 & \sin \varphi & \cos \varphi \end{array} \right) .
$$

Es gilt  $(D\mathbf{x})_{B}=D^{\prime}\mathbf{x}_{B}$  und  $D^{\prime}=B^{-1}DB$ .

In §7 und in den Aufgaben sind weitere Beispiele angegeben.

Definition. Zwei $n \times n$-Matrizen $A$, $C$ heißen ähnlich, wenn es eine invertierbare $n \times n$-Matrix $B$ gibt, so daß gilt $C = B^{-1}AB$.

In Satz 6.4 ist die geometrische Bedeutung der Ähnlichkeit beschrieben. Am Beispiel der Spiegelung und der Drehung wurde deutlich, daß eine verhältnismäßig komplizierte Abbildung mit Matrix A bezüglich einer „passenden“ Basis eine Abbildungsmatrix  $C = B^{-1} AB$  von recht einfacher Gestalt hat. Welche Eigenschaften der neuen Basis bewirken diese Vereinfachung?

Sei $A \in \mathbb{R}^{n \times n}$, $B = (\mathbf{b}_1, \ldots, \mathbf{b}_n)$ eine Basis des $\mathbb{R}^n$ mit $A\mathbf{b}_1 = \lambda\mathbf{b}_1$ ($\lambda \in \mathbb{R}$). Dann ist $(A\mathbf{b}_1)_B = \lambda\mathbf{e}_1$ die erste Spalte der Abbildungsmatrix $C$, über die anderen Spalten ist noch nichts Näheres bekannt. Immerhin hat man – gemäß Satz 6.4 – schon folgende „Vereinfachung“:

$$
B ^ {- 1} A B = \left( \begin{array}{c c c c c} \lambda & * & * & \dots & * \\ 0 & * & * & \dots & * \\ 0 & * & * & \dots & * \\ \vdots & \vdots & \vdots & & \vdots \\ 0 & * & * & \dots & * \end{array} \right) \tag {12}
$$

(an den \*-Stellen stehen die Koordinaten von $A\mathbf{b}_2, \ldots, A\mathbf{b}_n$ bezüglich $B$). Falls auch $A\mathbf{b}_2 = \mu\mathbf{b}_2$ gilt ($\mu \in \mathbb{R}$), dann steht auf der rechten Seite von (12) in der zweiten Spalte der Vektor $\mu\mathbf{e}_2 = (0, \mu, 0, \ldots, 0)^T$.

Die Fragestellung nach solchen Basisvektoren nennt man das algebraische Eigenwertproblem. Es tritt beispielsweise in der Elastomechanik auf bei der Bestimmung der Hauptspannungsrichtungen.

6.7 Eigenwerte, Eigenvektoren. Da die Behandlung des algebraischen Eigenwertproblems eng verbunden ist mit der Nullstellenbestimmung von Polynomen, lassen wir von jetzt an auch komplexe Zahlen als Skalare und Matrizen (also auch Zeilen- und Spaltenvektoren) mit komplexen Koeffizienten zu. Die bisherigen Ausführungen über Vektoren und Matrizen bleiben unverändert gültig, wenn R durch C ersetzt wird.

Definition. Eine Zahl $\lambda\in\mathbb{C}$ heißt Eigenwert einer Matrix $A\in\mathbb{C}^{n\times n}$, wenn es wenigstens einen Spaltenvektor $\mathbf{b}\in\mathbb{C}^{n}$, $\mathbf{b}\neq\mathbf{0}$, gibt mit

$$
A \mathbf {b} = \lambda \mathbf {b}.
$$

Jeder Vektor  $b \neq 0$ , der diese Gleichung erfüllt, heißt Eigenvektor von A zum Eigenwert  $\lambda$ .

## Beispiele.

1. Die Matrix $A = \begin{pmatrix} 0 & -1 & 0 \\ -1 & -1 & 1 \\ 0 & 1 & 0 \end{pmatrix}$ hat den Eigenwert $\lambda = -2$ mit zugehörigem Eigenvektor $\mathbf{b} = \begin{pmatrix} 1 \\ 2 \\ -1 \end{pmatrix}$; denn es gilt $A\mathbf{b} = -2\mathbf{b}$ und $\mathbf{b} \neq \mathbf{0}$.

2. Jede Drehmatrix $D \in \mathbb{R}^{3 \times 3}$ hat den Eigenwert 1, jeder Vektor $\neq \mathbf{0}$ parallel zur Drehachse ist Eigenvektor.

Zur Berechnung der Eigenwerte einer  $n \times n$ -Matrix betrachtet man (mit einer Variablen  $\lambda$ ) das charakteristische Polynom von A

$$
\chi_ {A} (\lambda) := \det (A - \lambda E).
$$

Diese Determinante ist explizit zu berechnen und das Ergebnis nach fallenden  $\lambda$ -Potenzen zu ordnen. Man erhält

$$
\chi_ {A} (\lambda) = (- \lambda) ^ {n} + (\text {Spur} A) (- \lambda) ^ {n - 1} + \dots + \det A \tag {13}
$$

wobei Spur A, die Spur von A, definiert ist durch

$$
\begin{array}{r l} \text {Spur} A := & a _ {1 1} + a _ {2 2} + \dots + a _ {n n} \\ (= & \text {Summe der Diagonalelemente von} A). \end{array}
$$

Satz 6.5. Es ist $\lambda \in \mathbb{C}$ genau dann ein Eigenwert der $n \times n$-Matrix $A$, wenn $\lambda$ eine Nullstelle des charakteristischen Polynoms $\chi_A$, d.h., wenn $\det (A - \lambda E) = 0$ ist.

Beweis. Es ist $\lambda\in\mathbb{C}$ genau dann Eigenwert, wenn das homogene lineare Gleichungssystem $(A-\lambda E)\mathbf{x}=\mathbf{0}$ eine von Null verschiedene Lösung besitzt. Das ist nach Satz 1.1 genau dann der Fall, wenn $\operatorname{Rang}(A-\lambda E)<n$, also wenn det $(A-\lambda E)=0$ gilt ($\rightarrow$ Satz 5.3). (Diese Ergebnisse gelten auch über $\mathbb{C}$.) □

Die Berechnung der Eigenwerte und Eigenvektoren erfolgt daher in 2 Schritten:

1. Schritt. Man bestimmt die (verschiedenen) Nullstellen $\lambda_{1},\ldots,\lambda_{r}$ der „charakteristischen Gleichung“ $\chi_{A}(\lambda)=\det(A-\lambda E)=0$, was gleichbedeutend ist mit der Erstellung der Produktdarstellung des charakteristischen Polynoms

$$
\chi_ {A} (\lambda) = (\lambda_ {1} - \lambda) ^ {k _ {1}} (\lambda_ {2} - \lambda) ^ {k _ {2}} \dots (\lambda_ {r} - \lambda) ^ {k _ {r}} \tag {14}
$$

(→ Kap. 2, 2.2, der Leitkoeffizient von $\chi_{A}$ ist $(-1)^{n}$).

$\lambda_{1},\ldots,\lambda_{r}$ sind die Eigenwerte von A. Die Vielfachheit $k_{i}$ der Nullstelle $\lambda_{i}$ heißt algebraische Vielfachheit des Eigenwertes $\lambda_{i}$. Demnach besitzt jede Matrix n nicht notwendig verschiedene Eigenwerte; jeder Eigenwert kommt dabei so oft vor, wie seine algebraische Vielfachheit angibt.

2. Schritt. Zu jedem Eigenwert $\lambda_{i}$ ($1 \leq i \leq r$) berechnet man den Lösungsraum des homogenen linearen Gleichungssystems $(A - \lambda_{i}E)\mathbf{x} = \mathbf{0}$. Jede Lösung $\neq \mathbf{0}$ ist ein Eigenvektor zu $\lambda_{i}$.

$$
V (\lambda_ {i}) := \{\mathbf {b} \in \mathbb {C} ^ {n}; (A - \lambda_ {i} E) \mathbf {b} = \mathbf {0} \} = \operatorname{Kern} (A - \lambda_ {i} E)
$$

heißt Eigenraum zum Eigenwert $\lambda_{i}$ ($1 \leq i \leq r$). Man nennt Dim $V(\lambda_{i})$ (die Dimension des Eigenraumes) die geometrische Vielfachheit des Eigenwertes $\lambda_{i}$. Algebraische und geometrische Vielfachheit stimmen im allgemeinen nicht überein ($\rightarrow$ Beispiel 1c und Aufgabe 14).

Bemerkung. Wird die rechte Seite von (14) ausmultipliziert und das Ergebnis mit (13) verglichen, erhält man

$$
\begin{array}{c} \text {Spur} A = k _ {1} \lambda_ {1} + \dots + k _ {r} \lambda_ {r}, \\ \det A = \lambda_ {1} ^ {k _ {1}} \lambda_ {2} ^ {k _ {2}} \dots \lambda_ {r} ^ {k _ {r}}, \\ \text {mit den verschiedenen Eigenwerten} \lambda_ {i} \text {der algebraischen Vielfachheit} k _ {i} (1 \leq i \leq r). \end{array} \tag {15}
$$

Formel (15) ist nützlich für Rechenkontrollen; sie erlaubt außerdem eine leichte Berechnung eines Eigenwerts, wenn alle anderen bekannt sind.

Beispiel 1. Gegeben $A = \begin{pmatrix} a & b \\ c & d \end{pmatrix} \in \mathbb{R}^{2 \times 2}$.

1. Schritt.

$$
\begin{array}{l} \chi_ {A} (\lambda) = \det \left( \begin{array}{c c} a - \lambda & b \\ c & d - \lambda \end{array} \right) = \lambda^ {2} - (a + d) \lambda + (a d - b c) \\ = \lambda^ {2} - (\operatorname{Spur} A) \lambda + \det A = (\lambda - \lambda_ {1}) (\lambda - \lambda_ {2}), \\ \end{array}
$$

wobei  $\lambda_{1}$ ,  $\lambda_{2}$  mit der Lösungsformel für  $\chi_{A}(\lambda)=0$  bestimmt wird.

2. Schritt. Mit jedem Eigenwert  $\lambda_{i}$  (i = 1, 2) wird

$$
\left( \begin{array}{c c} a - \lambda_ {i} & b \\ c & d - \lambda_ {i} \end{array} \right) \binom{x}{y} = \binom{0}{0}
$$

gelöst und jeweils eine Basis des Lösungsraumes angegeben.

Im Falle n = 2 gibt es somit vier verschiedene Fälle:

(a) $\lambda_1, \lambda_2 \in \mathbb{R}, \lambda_1 \neq \lambda_2,$
b) $\lambda_{1} = \lambda_{2}\in \mathbb{R}$, geometrische Vielfachheit 2,
(c) $\lambda_{1} = \lambda_{2}\in \mathbb{R}$, geometrische Vielfachheit 1,
(d) $\lambda_2 = \overline{\lambda}_1 \in \mathbb{C}, \lambda_1 \notin \mathbb{R}$.

Konkrete Zahlenbeispiele zu jedem dieser Fälle:

① $A = \begin{pmatrix} 1 & 2 \\ 2 & 1 \end{pmatrix}$ hat die Eigenwerte $\lambda_1 = -1$, $\lambda_2 = 3$, $V(\lambda_1)$, $V(\lambda_2)$ sind eindimensional mit den Basisvektoren $\mathbf{b}_1 = \begin{pmatrix} -1 \\ 1 \end{pmatrix}$, $\mathbf{b}_2 = \begin{pmatrix} 1 \\ 1 \end{pmatrix}$.

b $A = \left( \begin{array}{cc}3 & 0\\ 0 & 3 \end{array} \right)$ hat die Eigenwerte $\lambda_1 = \lambda_2 = 3$ mit Eigenraum $V(\lambda_1) = \mathbb{R}^2$
(c)  $A = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix}$  hat die Eigenwerte  $\lambda_{1} = \lambda_{2} = 2$  (algebraische Vielfachheit 2);
der Eigenraum  $V(\lambda_{1}) = \left\{\alpha \begin{pmatrix} 1 \\ 0 \end{pmatrix}; \alpha \in \mathbb{R}\right\}$  ist eindimensional (geometrische Vielfachheit 1).

(d)  $A = \begin{pmatrix} \cos \varphi & -\sin \varphi \\ \sin \varphi & \cos \varphi \end{pmatrix}$  hat die beiden konjugiert komplexen Eigenwerte
 $\lambda_{1} = \cos \varphi + i \sin \varphi, \lambda_{2} = \cos \varphi - i \sin \varphi, \text{ also keinen reellen Eigenwert (falls } \varphi \neq 0, \pm\pi, \pm2\pi, \ldots) \text{ und daher auch keinen reellen Eigenvektor. Die komplexen Eigenräume sind}$

$$
V (\lambda_ {1}) = \left\{\alpha \binom{1}{- i}; \alpha \in \mathbb {C} \right\}, V (\lambda_ {2}) = \left\{\alpha \binom{1}{i}; \alpha \in \mathbb {C} \right\}. \tag {$\square$}
$$

Beispiel 2. Jede obere (analog untere) Dreiecksmatrix

$$
A = \left( \begin{array}{c c c c} \alpha_ {1} & * & \dots & * \\ 0 & \alpha_ {2} & \ddots & \vdots \\ \vdots & \ddots & \ddots & * \\ 0 & \dots & 0 & \alpha_ {n} \end{array} \right)
$$

hat die Eigenwerte $\alpha_{1},\ldots ,\alpha_{n}$ ; denn es gilt

$$
\chi_ {A} (\lambda) = \det (A - \lambda E) = (\alpha_ {1} - \lambda) (\alpha_ {2} - \lambda) \dots (\alpha_ {n} - \lambda)
$$

(→ Satz 5.1). Die zugehörigen Eigenräume sind die Lösungsräume von  $(A - \alpha_{i}E)\mathbf{x} = \mathbf{0}$ , sie hängen ganz wesentlich von den \*-Stellen in A ab. Ist speziell A eine Diagonalmatrix (also alle \*-Stellen gleich Null), dann ist  $e_{i}$  ein Eigenvektor zum Eigenwert  $\alpha_{i}$  ( $1 \leq i \leq n$ ). □

## Beispiel 3.

Zwei Linearschwinger mit Massen  $m_{1}$ ,  $m_{2}$  und gleicher Federkonstan- ten  $c_{1}$  sind über eine dritte Fe- der der Konstante  $c_{2}$  gekoppelt. Das Gesetz von HOOKE liefert für die Auslenkungen  $s_{1}(t)$ ,  $s_{2}(t)$  die Bewegungsgleichungen

![](images/page_344_image_7.jpg)

<details>
<summary>text_image</summary>

s₂
s₁
</details>

Abb. 154 - Linearschwinger

$$
\binom{\ddot {s} _ {1}}{\ddot {s} _ {2}} + A \binom{s _ {1}}{s _ {2}} = \binom{0}{0} \quad \text {mit} \quad A = \left( \begin{array}{c c} \frac {c _ {1} + c _ {2}}{m _ {1}} & - \frac {c _ {2}}{m _ {1}} \\ - \frac {c _ {2}}{m _ {2}} & \frac {c _ {1} + c _ {2}}{m _ {2}} \end{array} \right)
$$

$(m_{1},m_{2},c_{1}>0,c_{2}\geq0).$

Der Ansatz

$$
\binom{s _ {1} (t)}{s _ {2} (t)} = (\cos \omega t) \binom{v _ {1}}{v _ {2}} = (\cos \omega t) \mathbf {v}
$$

führt wegen  $\cos\omega t\neq0$  auf das Eigenwertproblem

$$
A \mathbf {v} = \omega^ {2} \mathbf {v}.
$$

Schreibt man abkürzend

$$
A = \left( \begin{array}{c c} w _ {1} ^ {2} & - k _ {1} ^ {2} \\ - k _ {2} ^ {2} & w _ {2} ^ {2} \end{array} \right) ,
$$

so lauten die Eigenwerte

$$
\lambda_ {1, 2} = \frac {1}{2} (w _ {1} ^ {2} + w _ {2} ^ {2}) \pm \sqrt {\frac {1}{4} (w _ {1} ^ {2} - w _ {2} ^ {2}) ^ {2} + k _ {1} ^ {2} k _ {2} ^ {2}}.
$$

Die Eigenwerte sind stets reell und wegen  $w_{1}^{2} \geq k_{1}^{2}$  und  $w_{2}^{2} \geq k_{2}^{2}$  positiv, d.h. man hat zwei sogenannte Eigenschwingungen mit den Frequenzen  $\omega_{1,2} = \sqrt{\lambda_{1,2}}$ . Jede Lösung der Bewegungsgleichungen kann als Superposition dieser beiden Eigenschwingungen geschrieben werden.

Besonders einfach ist der Fall  $m_{1}=m_{2}=m$  mit symmetrischem A :

$$
\begin{array}{l} \omega_ {1} = \sqrt {\frac {c _ {1}}{m}} \quad , \quad \mathbf {v} _ {1} = \binom{1}{1} \\ \omega_ {2} = \sqrt {\frac {c _ {1} + 2 c _ {2}}{m}}, \quad \mathbf {v} _ {2} = \binom{1}{- 1} \\ \end{array}
$$

(gleichphasige Schwingung)

(gegenphasige Schwingung)

□

Im folgenden Satz stellen wir nützliche Beobachtungen zusammen.

Satz 6.6. Sei $A \in \mathbb{C}^{n \times n}$.

a) Besitzt A den Eigenvektor b zum Eigenwert λ, dann haben

$$
\alpha A, A ^ {m}, A + \beta E, p (A) := \alpha_ {m} A ^ {m} + \dots + \alpha_ {1} A + \alpha_ {0} E
$$

ebenfalls den Eigenvektor b, jedoch jeweils zum Eigenwert

$$
\alpha \lambda , \lambda^ {m}, \lambda + \beta , p (\lambda) = \alpha_ {m} \lambda^ {m} + \dots + \alpha_ {1} \lambda + \alpha_ {0}.
$$

b) A und die Transponierte  $A^{T}$  haben dasselbe charakteristische Polynom, deshalb besitzen sie dieselben Eigenwerte (jedoch i.a. mit verschiedenen Eigenräumen).
c) Die ähnlichen Matrizen A und  $B^{-1}AB$  haben dasselbe charakteristische Polynom und deshalb dieselben Eigenwerte; b ist genau dann Eigenvektor von A, wenn  $B^{-1}b$  Eigenvektor von  $B^{-1}AB$  ist.
d) Es ist A genau dann invertierbar, wenn alle Eigenwerte ≠ 0 sind. Ist λ ein Eigenwert von A mit Eigenvektor b, dann ist λ⁻¹ Eigenwert von A⁻¹ mit demselben Eigenvektor b.

Beweis. a): Aus $A\mathbf{b} = \lambda \mathbf{b}$ folgt $p(A)\mathbf{b} = p(\lambda)\mathbf{b}$.

b): $\operatorname{det}(A^T - \lambda E) = \operatorname{det}(A - \lambda E)^T = \operatorname{det}(A - \lambda E) \quad (\rightarrow \text{Satz 5.3b})$.

c): $\det (B^{-1}AB - \lambda E) = \det B^{-1}(A - \lambda E)B = \det B^{-1}\det (A - \lambda E)\det B = \det (A - \lambda E)$ $(\rightarrow (8),\S 5)$.

d): det  $A = \lambda_{1}^{k_{1}} \cdots \lambda_{r}^{k_{r}} \neq 0$  ( $\rightarrow 15$ )  $\Longleftrightarrow$  alle  $\lambda_{i} \neq 0$ .

Ferner: $A\mathbf{b} = \lambda \mathbf{b}\Rightarrow \frac{1}{\lambda}\mathbf{b} = A^{-1}\mathbf{b}$

Bemerkung. Die Koeffizienten des charakteristischen Polynoms  $\chi_{A}(\lambda)=c_{n}(-\lambda)^{n}+c_{n-1}(-\lambda)^{n-1}+\cdots+c_{1}(-\lambda)+c_{0}$  sind Invarianten der  $n\times n$ -Matrix A, bzw. Invarianten der zugehörigen linearen Abbildung  $x\mapsto Ax$ , da sie sich gemäß Satz 6.4 und Satz 6.6, Teil c, bei einem Basiswechsel nicht ändern.

## Beispiel.

$$
A = (\alpha_ {i j}) \in \mathbb {R} ^ {3 \times 3}, \chi_ {A} (\lambda) = - \lambda^ {3} + c _ {2} \lambda^ {2} - c _ {1} \lambda + c _ {0} = (\lambda_ {1} - \lambda) (\lambda_ {2} - \lambda) (\lambda_ {3} - \lambda).
$$

$$
c _ {2} = \operatorname{Spur} A = a _ {1 1} + a _ {2 2} + a _ {3 3} = \lambda_ {1} + \lambda_ {2} + \lambda_ {3},
$$

$$
c _ {1} = \det \left| \begin{array}{l l} a _ {1 1} & a _ {1 2} \\ a _ {2 1} & a _ {2 2} \end{array} \right| + \det \left| \begin{array}{l l} a _ {1 1} & a _ {1 3} \\ a _ {3 1} & a _ {3 3} \end{array} \right| + \det \left| \begin{array}{l l} a _ {2 2} & a _ {2 3} \\ a _ {3 2} & a _ {3 3} \end{array} \right| = \lambda_ {1} \lambda_ {2} + \lambda_ {1} \lambda_ {3} + \lambda_ {2} \lambda_ {3},
$$

$$
c _ {0} = \det A = \lambda_ {1} \lambda_ {2} \lambda_ {3}.
$$

$c_{0}, c_{1}, c_{2}$ sind Invarianten der linearen Abbildung $f(\mathbf{x}) = A\mathbf{x}, \mathbf{x} \in \mathbb{R}^{3}$. Das bedeutet speziell für den Spannungstensor ($\rightarrow$ 6.1, Beisp. 9), der in einem kartesischen Koordinatensystem durch die Matrix

$$
S = \left( \begin{array}{c c c} \sigma_ {x} & \tau_ {x y} & \tau_ {x z} \\ \tau_ {x y} & \sigma_ {y} & \tau_ {y z} \\ \tau_ {x z} & \tau_ {y z} & \sigma_ {z} \end{array} \right)
$$

dargestellt wird, daß in jedem anderen Koordinatensystem (mit gleichem Ursprung) die den Größen

$$
c _ {2} = \sigma_ {x} + \sigma_ {y} + \sigma_ {z},
$$

$$
c _ {1} = \sigma_ {x} \sigma_ {y} + \sigma_ {x} \sigma_ {z} + \sigma_ {y} \sigma_ {z} - \tau_ {x y} ^ {2} - \tau_ {x z} ^ {2} - \tau_ {y z} ^ {2},
$$

$$
c _ {0} = \det S
$$

entsprechenden Werte gleich sind.

Zur Berechnung eines maximalen Systems linear unabhängiger Eigenvektoren der Matrix A genügt es, jeweils eine Basis der Eigenräume zu den einzelnen Eigenwerten zu bestimmen. Denn es gilt

Satz 6.7. Eigenvektoren  $b_{1},\ldots,b_{r}$  zu paarweise verschiedenen Eigenwerten  $\lambda_{1},\ldots,\lambda_{r}$  der Matrix A sind linear unabhängig.

Beweis. Aus  $\alpha_{1}b_{1}+\cdots+\alpha_{r}b_{r}=0$  folgt durch Multiplikation mit A (von links)  $\lambda_{1}\alpha_{1}b_{1}+\cdots+\lambda_{r}\alpha_{r}b_{r}=0$ . Aus beiden Gleichungen ergibt sich

$$
(\lambda_ {1} - \lambda_ {2}) \alpha_ {2} \mathbf {b} _ {2} + \dots + (\lambda_ {1} - \lambda_ {r}) \alpha_ {r} \mathbf {b} _ {r} = \mathbf {0}.
$$

Ebenso (Multiplikation mit A und Vergleich) folgt hieraus

$$
(\lambda_ {1} - \lambda_ {3}) (\lambda_ {2} - \lambda_ {3}) \alpha_ {3} \mathbf {b} _ {3} + \dots + (\lambda_ {1} - \lambda_ {r}) (\lambda_ {2} - \lambda_ {r}) \alpha_ {r} \mathbf {b} _ {r} = \mathbf {0},
$$

etc. Man gelangt schließlich zu  $(\lambda_{1}-\lambda_{r})(\lambda_{2}-\lambda_{r})\cdots(\lambda_{r-1}-\lambda_{r})\alpha_{r}\mathbf{b}_{r}=\mathbf{0}$ , woraus  $\alpha_{r}=0$  folgt. Dies gibt rückwärts eingesetzt  $\alpha_{r-1}=\cdots=\alpha_{1}=0$ . ☐

Besonders günstige Verhältnisse liegen vor, wenn es im $\mathbf{C}^{n}$ eine Basis gibt, die vollständig aus Eigenvektoren der Matrix $A\in\mathbf{C}^{n\times n}$ besteht.

Satz 6.8. Besitzt eine Matrix $A \in \mathbb{C}^{n \times n}$ n linear unabhängige Eigenvektoren $\mathbf{b}_1, \ldots, \mathbf{b}_n$, $A\mathbf{b}_i = \lambda_i\mathbf{b}_i$, mit den nicht notwendig verschiedenen Eigenwerten $\lambda_1, \ldots, \lambda_n$, dann bringt die Transformationsmatrix

$$
B := (\mathbf {b} _ {1}, \mathbf {b} _ {2}, \dots , \mathbf {b} _ {n})
$$

(mit den Eigenvektoren als Spalten) die Matrix A auf Diagonalform; d.h., es gilt, wenn die Reihenfolge der $\lambda_{i}$ und der $\mathbf{b}_{i}$ übereinstimmt,

$$
B ^ {- 1} A B = \left( \begin{array}{c c c c c} \lambda_ {1} & 0 & 0 & \dots & 0 \\ 0 & \lambda_ {2} & 0 & \dots & 0 \\ 0 & 0 & & & \vdots \\ \vdots & \vdots & \ddots & & 0 \\ 0 & 0 & \dots & 0 & \lambda_ {n} \end{array} \right) =: D.
$$

Beweis. $\rightarrow$ (12), oder direkt: $AB = (Ab_{1},\dots,Ab_{n}) = (\lambda_{1}b_{1},\dots,\lambda_{n}b_{n}) = BD$. $\square$

Die „Diagonalisierung“ gemäß Satz 6.8 bringt beachtliche Rechenvorteile mit sich. Etwa bei der Berechnung der k-ten Potenzen von A :

$$
\begin{array}{l} A ^ {k} = (B D B ^ {- 1}) ^ {k} = (B D B ^ {- 1}) (B D B ^ {- 1}) \dots (B D B ^ {- 1}) = B D ^ {k} B ^ {- 1} \\ = B \left( \begin{array}{c c c} \lambda_ {1} ^ {k} & & \\ & \lambda_ {2} ^ {k} & 0 \\ & & \ddots \\ & 0 & & \lambda_ {n} ^ {k} \end{array} \right) B ^ {- 1}. \\ \end{array}
$$

Beispiel.  $A = \begin{pmatrix} -2 & -8 & -12 \\ 1 & 4 & 4 \\ 0 & 0 & 1 \end{pmatrix}$

1. Schritt : Die Eigenwerte.

$$
\det (A - \lambda E) = (1 - \lambda) (\lambda - 2) \lambda = 0 \Rightarrow \lambda_ {1} = 0, \lambda_ {2} = 1, \lambda_ {3} = 2.
$$

2. Schritt: Die Eigenvektoren. Es sind drei homogene lineare Gleichungssysteme  $(A-\lambda_{i}E)\mathbf{x}=0$  (i=1,2,3) zu lösen. In diesem Fall ergeben sich eindimensionale Eigenräume

$$
V (\lambda_ {i}) = \{\alpha \mathbf {b} _ {i}; \alpha \in \mathbb {R} \} \text {mit} \mathbf {b} _ {1} = \left( \begin{array}{c} 4 \\ - 1 \\ 0 \end{array} \right), \mathbf {b} _ {2} = \left( \begin{array}{c} 4 \\ 0 \\ - 1 \end{array} \right), \mathbf {b} _ {3} = \left( \begin{array}{c} 2 \\ - 1 \\ 0 \end{array} \right).
$$

3. Schritt: Die Diagonalisierung. Mit der (invertierbaren) Transformationsmatrix

$$
B = (\mathbf {b} _ {1}, \mathbf {b} _ {2}, \mathbf {b} _ {3}) = \left( \begin{array}{c c c} 4 & 4 & 2 \\ - 1 & 0 & - 1 \\ 0 & - 1 & 0 \end{array} \right)
$$

ergibt sich $B^{-1}AB = \begin{pmatrix} 0 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 2 \end{pmatrix} =: D$, bzw. $A = BDB^{-1}$. Damit berechnen wir beispielsweise $A^{100}$:

$$
\begin{array}{l} A ^ {1 0 0} = B D ^ {1 0 0} B ^ {- 1} = \left( \begin{array}{r r r} 4 & 4 & 2 \\ - 1 & 0 & - 1 \\ 0 & - 1 & 0 \end{array} \right) \left( \begin{array}{c c c} 0 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 2 ^ {1 0 0} \end{array} \right) \left( \begin{array}{r r r} \frac {1}{2} & 1 & 2 \\ 0 & 0 & - 1 \\ - \frac {1}{2} & - 2 & - 2 \end{array} \right) \\ = \left( \begin{array}{c c c} - 2 ^ {1 0 0} & - 2 ^ {1 0 2} & - 4 - 2 ^ {1 0 2} \\ 2 ^ {9 9} & 2 ^ {1 0 1} & 2 ^ {1 0 1} \\ 0 & 0 & 1 \end{array} \right) . \\ \end{array}
$$

Die numerische Berechnung der Eigenwerte und Eigenvektoren einer Matrix ist i.a. ein schwieriges Problem. Man vermeidet dabei den Weg über die charakteristische Gleichung (→Programm JACOBI, §7). Zur Unterstützung von Handrechnungen dient das folgende Programm zur Bestimmung der Koeffizienten des Polynoms det(λE - A) für eine n × n-Matrix A, das auf den französischen Astronomen U. LEVERRIER (1811 - 1877) zurückgeht.

(Man beachte: Der Koeffzient von  $\lambda^{n}$  ist stets 1!)

```txt
'---- Programm LEVERRIER----
Print "DIMENSION N=";
Input N
Dim A(N,N),B(N,N)
Print "A ZEILENWEISE"
For I=1 To N
    For J=1 To N
        Print "A"+Str$(I)+Str$(J);
        Input A(I,J)
        B(I,J)=A(I,J)
    Next J
Next I
For K=1 To N-2
    Exit If N=2
    Gosub Shift
    For J=1 To N
        For I=1 To N
            B(I,O)=B(I,J)
        Next I
        For I=1 To N
            X=0
            For L=1 To N
                X=X+A(I,L)*B(L,O)
            Next L
            B(I,J)=X
        Next I
    Next J
Next K
```

\* 6.8 Die orthogonale Gruppe. Wir geben weitere wichtige Eigenschaften orthogonaler $n \times n$-Matrizen (insbesondere für $n = 2,3$) an.

Definition. Die Menge aller orthogonalen  $n \times n$ -Matrizen,

$$
O (n) := \left\{A \in \mathbb {R} ^ {n \times n}, A ^ {T} A = E \right\},
$$

heißt orthogonale Gruppe des $\mathbb{R}^{n}$, und die Teilmenge

$$
S O (n) := \left\{A \in \mathbb {R} ^ {n \times n}; A ^ {T} A = E \text {und} \det A = 1 \right\},
$$

heißt spezielle orthogonale Gruppe oder Drehgruppe.

Man verifiziert leicht anhand der Definitionen:

(16) $A, B \in O(n)$ (bzw. $SO(n)$) $\Rightarrow A^{-1}$, $AB \in O(n)$ (bzw. $SO(n)$).

## Satz 6.9.

a) $O(2)$ besteht aus allen Matrizen der Form $(\varphi \in \mathbb{R})$

$$
A = \left( \begin{array}{c c} \cos \varphi & - \sin \varphi \\ \sin \varphi & \cos \varphi \end{array} \right), \text {falls} \det A = 1, \text {bzw.}
$$

$$
A = \left( \begin{array}{c c} - \cos \varphi & \sin \varphi \\ \sin \varphi & \cos \varphi \end{array} \right), \text {falls} \det A = - 1.
$$

b) Zu  $A \in O(3)$  gibt es ein kartesisches Koordinatensystem  $K = (0; \mathbf{e}_{1}^{\prime}, \mathbf{e}_{2}^{\prime}, \mathbf{e}_{3}^{\prime})$ , in der die orthogonale Abbildung  $x \mapsto Ax$ , dargestellt wird durch

$$
\mathbf {x} ^ {\prime} \mapsto \left( \begin{array}{c c c} \cos \varphi & - \sin \varphi & 0 \\ \sin \varphi & \cos \varphi & 0 \\ 0 & 0 & \epsilon \end{array} \right) \mathbf {x} ^ {\prime} \quad \text {mit} \epsilon = \det A.
$$

Äquivalent hierzu ist die Aussage

$$
\left( \begin{array}{c c c} \cos \varphi & - \sin \varphi & 0 \\ \sin \varphi & \cos \varphi & 0 \\ 0 & 0 & \det A \end{array} \right) = P ^ {T} A P
$$

mit der orthogonalen Matrix $P = (\mathbf{e}_1', \mathbf{e}_2', \mathbf{e}_3')$, det $P = 1$.

c) $A \in SO(3) \iff A$ ist eine Drehmatrix $(\rightarrow 6.4)$.

## Beweis.

a): Für $A = \begin{pmatrix} a & b \\ c & d \end{pmatrix}$ mit det $A = 1$ und $A^T = A^{-1}$ muß $d = a$, $b = -c$ und $a^2 + c^2 = 1$ sein, d.h. die Spitze des Zeigers $\begin{pmatrix} a \\ c \end{pmatrix}$ liegt auf dem Einheitskreis (um 0), also gibt es $\varphi$ mit $a = \cos \varphi$, $c = \sin \varphi$.

Im Fall det A = -1 betrachtet man die orthogonale Matrix

$$
A _ {1} := \left( \begin{array}{c c} - 1 & 0 \\ 0 & 1 \end{array} \right) A \quad \text {mit} \det A _ {1} = 1.
$$

b): 1. Fall: $A \in SO(3)$, d.h. $A^T A = E$, $\det A = 1$.

Dann hat $A$ den Eigenwert $\lambda = 1$.

Denn $\det (A - E) = (\det A^T)(\det (A - E)) = \det (A^T A - A^T) = \det (E - A^T) =$ $\det (E - A) = (-1)^3\det (A - E)$ , also $\det (A - 1\cdot E) = 0$

Sei  $e_{3}^{\prime}$  ein normierter Eigenvektor von A zum Eigenwert 1. Dazu wählen wir eine kartesische Basis  $P = (\mathbf{e}_{1}^{\prime}, \mathbf{e}_{2}^{\prime}, \mathbf{e}_{3}^{\prime})$ . Da A orthogonal ist, sind auch die Bilder  $Ae_{1}^{\prime}$ ,  $Ae_{2}^{\prime}$  orthogonal zu  $e_{3}^{\prime} = Ae_{3}^{\prime}$ . Das bedeutet

$$
\begin{array}{l} A \mathbf {e} _ {1} ^ {\prime} = a \mathbf {e} _ {1} ^ {\prime} + b \mathbf {e} _ {2} ^ {\prime} \\ A \mathbf {e} _ {2} ^ {\prime} = c \mathbf {e} _ {1} ^ {\prime} + d \mathbf {e} _ {2} ^ {\prime} \\ A \mathbf {e} _ {3} ^ {\prime} = \mathbf {e} _ {3} ^ {\prime} \\ \end{array}
$$

mit gewissen Zahlen $a, b, c, d$. Man erhält deshalb ($\rightarrow$ Satz 6.4)

$$
C = \left( \begin{array}{c c c} a & c & 0 \\ b & d & 0 \\ 0 & 0 & 1 \end{array} \right) = P ^ {T} A P
$$

(man beachte $P^{-1} = P^T$). Da mit $A$ auch $C$ und deshalb $\begin{pmatrix} a & b \\ c & d \end{pmatrix}$ orthogonal ist und $\det\begin{pmatrix} a & b \\ c & d \end{pmatrix} = \det C = \det A = 1$ gilt, folgt die Beh. aus a). $\mathbf{x} \mapsto A\mathbf{x}$ ist eine Drehung um die in Richtung $\mathbf{e}_3'$ weisende Achse (durch den Nullpunkt) mit dem Winkel $\varphi$. Damit ist auch c) bewiesen.

2. Fall: $A \in O(3)$, $\det A = -1$.

In diesem Fall gehe man über zur orthogonalen Matrix

$$
\tilde {A} = \left( \begin{array}{c c c} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & - 1 \end{array} \right) A \quad \text {mit} \det \tilde {A} = 1.
$$

$x \mapsto Ax$ ist eine Drehspiegelung, d.h. darstellbar als eine Drehung, gefolgt von einer Spiegelung ( $\rightarrow$ Aufg. 9).

Folgerung. Die Hintereinanderausführung zweier Drehungen des  $R^{3}$  – um i.a. verschiedene Achsen durch den Nullpunkt – ergibt eine Drehung; d.h. sind  $D_{1}$ ,  $D_{2}$  Drehmatrizen, so ist auch  $D = D_{1}D_{2}$  eine Drehmatrix. (Drehwinkel und Drehachse von D werden mit (6) und (7) bestimmt, → Bsp. in 6.4.)

## Aufgaben

1. Welche der Abbildungen  $f_{i}: R^{3} \rightarrow R^{3}$  sind linear?

a) $f_{1}(x_{1},x_{2},x_{3}) = (\sin x_{1},x_{2} + x_{3},0),$
b) $f_{2}(x_{1},x_{2},x_{3}) = (2x_{1} + x_{2},3x_{2},x_{1} + x_{2}^{2}),$
c) $f_{3}(x_{1},x_{2},x_{3}) = (3x_{3} + 2x_{2},x_{3} + x_{1},x_{2} - 5x_{1}),$
d)  $f_{4}(x_{1},x_{2},x_{3})=(x_{1},x_{2}+1,x_{3})$ ,
e) $f_{5}(x_{1},x_{2},x_{3}) = (x_{1} - x_{2},17x_{3},x_{1} + x_{2} + x_{3}).$

Wie lautet gegebenenfalls die Abbildungsmatrix?

2. Für die linearen Abbildungen $f_1, f_2 : \mathbb{R}^3 \to \mathbb{R}^3$ berechne man den Bildraum, Kern $f_i$, $f_1 \circ f_2$, $f_2 \circ f_1$, $(f_1 \circ f_1 - \mathrm{Id}) \circ (f_2 - 3\mathrm{Id})$, $f_1^{-1}$;

$$
f _ {1} (x _ {1}, x _ {2}, x _ {3}) = (3 x _ {1}, x _ {1} - x _ {2}, 2 x _ {1} + x _ {2} + x _ {3}),
$$

$$
f _ {2} (x _ {1}, x _ {2}, x _ {3}) = (x _ {1} - x _ {2}, 2 x _ {1} + x _ {3}, 0)  .
$$

3. Gegeben sind drei lineare Abbildungen im  $R^{3}$ :

$\sigma : \text{Spiegelung an der Ebene } x + 4y + 8z = 0 ;$
$\tau : \text{Scherung längs } \mathbf{a} = (1,2,-3)^T \text{ senkrecht } \mathbf{b} = (1,1,1)^T : \mathbf{x} \mapsto \mathbf{x} + (\mathbf{x} \cdot \mathbf{b})\mathbf{a} ;$
$\delta : \text{Drehung um die } y\text{-Achse um } \alpha = \frac{\pi}{6} \text{ mit anschließender Drehung um die } z\text{-Achse um } \gamma = \frac{\pi}{4} .$

Man bestimme

a) die Abbildungsmatrizen S, T, D;
b) jeweils das Bild des Punktes (1,2,3);

c) die Matrizen  $S^{-1}$  und  $T^{-1}$  über die Umkehrabbildungen ;
d) die Drehachse und den Drehwinkel von $\delta$;
e) die Koordinaten des Punktes  $(1,2,-3)$  bezüglich der gedrehten Basis  $(D\mathbf{e}_{1}, D\mathbf{e}_{2}, D\mathbf{e}_{3})$ .

4. Man bestätige, daß $B = (\mathbf{a}, \mathbf{b}, \mathbf{c})$ mit $\mathbf{a} = (1, 1, 1)^T$, $\mathbf{b} = (1, 1, 0)^T$, $\mathbf{c} = (0, 1, 2)^T$ eine Basis des $\mathbb{R}^3$ bestimmt und berechne $\mathbf{x}_B$ für $\mathbf{x} = (1, 2, 3)^T$.

5. Die gegebene Matrix A kann auf zwei Weisen zu einer orthogonalen Matrix ergänzt werden; wie lauten diese?

$$
A = \left( \begin{array}{c c c} 1 / \sqrt {3} & 1 / \sqrt {2} & 1 / \sqrt {6} \\ * & - 1 / \sqrt {2} & * \\ * & 0 & * \end{array} \right)
$$

a) Man berechne jeweils die Determinante von $A$.

b) Für den Fall einer Drehung bestimme man die Drehachse und den Drehwinkel; falls eine Spiegelung vorliegt, die Ebene, an der gespiegelt wird.

c) Wie lauten jeweils die Koordinaten des Punktes (1,2,3) in der Basis  $(A\mathbf{e}_{1}, A\mathbf{e}_{2}, A\mathbf{e}_{3})$ ?

6. Zwei orthogonale Abbildungen $p$ und $q$ des $\mathbb{R}^3$ sind zu betrachten, die jeweils aus zwei Elementar-Abbildungen zusammengesetzt sind:

## Abbildung p

①. Drehung um die z-Achse mit Winkel  $\varphi$ ,

②. Spiegelung an der Ebene y = 0 .

## Abbildung q

① Drehung um die z-Achse mit Winkel  $\varphi$ ,
②. Spiegelung am Bild der Ebene
$y = 0$ .

a) Man bestimme die Abbildungsmatrix der beiden Spiegelungen sowohl

\- im Inertialsystem $I = (O; \mathbf{e}_1, \mathbf{e}_2, \mathbf{e}_3)$, als auch

\- im gedrehten System $B$, das aus $I$ durch ①. entsteht.

b) Man leite daraus die Abbildungsmatrizen von $p$ und $q$ in $I$ und $B$ ab. Welcher Typ von Abbildung liegt jeweils vor?

7. Durch geeignete Verschiebung des Koordinatenursprungs im  $R^{3}$  ist jede Abbildung  $x \mapsto Dx + c$ , die aus einer Drehung und einer anschließenden Parallelverschiebung entsteht, stets als Schraubung darstellbar:

$$
\mathbf {y} \mapsto D \mathbf {y} + v \mathbf {a},
$$

wobei a,  $|a| = 1$ , die Achsenrichtung der Drehmatrix D und v den Vorschub bezeichnet.

![](images/page_351_image_27.jpg)

<details>
<summary>text_image</summary>

O
m
a
Dx+c = m+Dy+va
y
φ
x
Dy
va
</details>

Man bestimme die Achsenrichtung a, den Vorschub v und den Drehwinkel δ der Abbildung

$$
\mathbf {x} \mapsto \frac {1}{\sqrt {2}} \left( \begin{array}{c c c} 1 & - 1 & 0 \\ 1 & 1 & 0 \\ 0 & 0 & \sqrt {2} \end{array} \right) \mathbf {x} + \left( \begin{array}{c} 1 \\ 2 \\ 3 \end{array} \right).
$$

8. Das kartesische  $(x,y,z)$ -Koordinatensystem wird zuerst  $45^{\circ}$  um die y-Achse und dann  $45^{\circ}$  um das Bild der z-Achse gedreht. Welche Koordinaten  $(\xi,\eta,\zeta)$  besitzt der Punkt  $(x,y,z)=(1,2,3)$  in der neuen Basis?