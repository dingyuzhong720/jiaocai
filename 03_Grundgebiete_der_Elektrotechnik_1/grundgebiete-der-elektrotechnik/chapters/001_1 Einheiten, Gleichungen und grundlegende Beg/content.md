# 1 Einheiten, Gleichungen und grundlegende Begriffe

原始 PDF 第 11–24 页。

## 1 Einheiten, Gleichungen und grundlegende Begriffe

## 1.1 Einheitensysteme

## 1.1.1 Maßsysteme

Um eine physikalische Größe messen zu können, muss der Größe eine Einheit zuge ordnet werden. Messen bedeutet dann, dass ein Zahlenwert bestimmt wird, welcher angibt, wie oft die zugeordnete Einheit in der zu messenden Größe enthalten ist.

Durch die physikalischen Gesetzmäßigkeiten, die einen Zusammenhang zwischen den physikalischen Größen herstellen, lässt sich die Anzahl der zugeordneten Einheiten auf wenige Grundeinheiten beschränken. Die Grundeinheiten sind Bestandteil des internationalen Einheitensystems **SI** (Système International). Durch den Beschluss der 26. Generalkonferenz für Maß und Gewicht erfolgte eine grundlegende Veränderung des SI, welche am 20. Mai 2019 in Kraft trat. Seitdem ist keine SI-Einheit mehr von veränderlichen Größen oder Objekten bestimmt. Jede Einheit lässt sich jetzt aus einer Kombination von sieben fest definierten Konstanten herleiten. Diese sieben physikalischen Konstanten sind seit der Messkampagne 2018 des **CODATA** (Committee on Data for Science and Technology) als exakt definiert. Ihre Werte sind mit den zugehörigen SI-Einheiten in der Tabelle 1.1 wiedergegeben.

Tab. 1.1: Die sieben physikalischen Konstanten des SI mit ihren seit der Messkampagne 2018 des CODATA als exakt definierten Werten, veröffentlicht am 20. Mai 2019, dem Tag des Messens.

<table><tr><td colspan="2">Konstante</td><td>exakter Wert</td></tr><tr><td> $\Delta v_{Cs}$ </td><td>Frequenz des Hyperfeinstrukturübergangs des Grundzustands im Caesium-133-Atom  $^{133}Cs$ </td><td>9 192 631 770  $s^{-1}$ </td></tr><tr><td> $c$ </td><td>Lichtgeschwindigkeit</td><td>299 792 458 m  $s^{-1}$ </td></tr><tr><td> $h$ </td><td>Planksches Wirkungsquantum</td><td>6,626 070 15  $\cdot$   $10^{-34}$  kg  $m^{2}$   $s^{-1}$ </td></tr><tr><td> $e$ </td><td>Elementarladung</td><td>1,602 176 634  $\cdot$   $10^{-19}$  A s</td></tr><tr><td> $k_{B}$ </td><td>Boltzmann-Konstante</td><td>1,380 649  $\cdot$   $10^{-23}$  kg  $m^{2}$   $s^{-2}$   $K^{-1}$ </td></tr><tr><td> $N_{A}$ </td><td>Avogadro-Konstante</td><td>6,022 140 76  $\cdot$   $10^{23}$  mol $^{-1}$ </td></tr><tr><td> $K_{cd}$ </td><td>Photometrisches Strahlungsäquivalent für die monochromatische Strahlung der Frequenz 540 THz (grünes Licht)</td><td>683 cd sr  $s^{3}$   $kg^{-1}$   $m^{-2}$ </td></tr></table>

In der Elektrotechnik hat sich das **MKSA-System** (Meter, Kilogramm, Sekunde, Ampere) weitgehend durchgesetzt, das von den Grundgrößen Länge, Masse, Zeit und Stromstärke ausgeht. Außerdem wird zur Beschreibung thermischer Vorgänge die Temperatur als fünfte Grundgröße benötigt. Das MKSA-System ist Teil des SI.

https://doi.org/10.1515/9783110631586-001

---

2

1 Einheiten, Gleichungen und grundlegende Begriffe

## 1.1.2 Die Grundgrößen des SI

Die für die Elektrotechnik fünf wichtigen Grundgrößen des SI sind wie folgt definiert:

1. **Die Zeit**: Die SI-Einheit für die Zeit ist die Sekunde mit dem Einheitenzeichen s. Die Sekunde ist das 9 192 631 770-fache der Periodendauer der Strahlung beim Übergang zwischen zwei bestimmten Energieniveaus des Atoms von Cäsium 133

$$
1 \mathrm{s} = \frac {9 1 9 2 6 3 1 7 7 0}{\Delta v _ {\mathrm{Cs}}}.
$$

2. **Die Länge**: Die SI-Einheit für die Länge ist der Meter mit dem Einheitenzeichen m. Der Meter ist über den festen Zahlenwert der Lichtgeschwindigkeit definiert. Ein Meter ist die Strecke, die das Licht im Vakuum während 1/299 792 458 s durchläuft. Dabei ist die Einheit der Sekunde mit Hilfe der Konstanten $\Delta \nu _ { C s }$ definiert

$$
1 \mathrm{m} = 1 \frac {c}{2 9 9 7 9 2 4 5 8} \mathrm{s} = 1 \frac {9 1 9 2 6 3 1 7 7 0}{2 9 9 7 9 2 4 5 8} \frac {c}{\Delta v _ {\mathrm{Cs}}}.
$$

3. **Die Masse**: Die SI-Einheit für die Masse ist das Kilogramm mit dem Einheitenzeichen kg. Die Masse wird durch den festen Zahlenwert des Plank’schen Wirkungsquantums h bestimmmt, wobei die Einheiten für den Meter und die Sekunde über die Konstanten c und $\Delta \nu _ { C s }$ definiert sind

$$
\begin{array}{l} 1 \mathrm{kg} = 1 \frac {h}{6 , 6 2 6 0 7 0 1 5 \cdot 1 0 ^ {- 3 4}} \frac {\mathrm{s}}{\mathrm{m} ^ {2}} \\ = 1 \frac {(2 9 9 7 9 2 4 5 8) ^ {2}}{6 , 6 2 6 0 7 0 1 5 \cdot 1 0 ^ {- 3 4} \cdot 9 1 9 2 6 3 1 7 7 0} \frac {h \cdot \Delta v _ {\mathrm{Cs}}}{c ^ {2}}. \\ \end{array}
$$

Die bis 2019 gültige Definition nach der DIN 1301 lautet: 1 Kilogramm (= 1 kg) ist bestimmt durch die Masse des in Sèvres aufbewahrten »Urkilogramms«.

4. **Die elektrische Stromstärke**: Die SI-Einheit für die Stromstärke ist das Ampere mit dem Einheitenzeichen A. Die Stromstärke ist durch den festen Zahlenwert der Elementarladung e bestimmt, wobei hier die Einheit Sekunde durch die Konstante $\Delta \nu _ { \mathrm { C s } }$ definiert ist

$$
\begin{array}{l} 1 \mathrm{A} = 1 \frac {e}{1 , 6 0 2 1 7 6 6 3 4 \cdot 1 0 ^ {- 1 9}} \frac {1}{\mathrm{s}} \\ = 1 \frac {e \cdot \Delta v _ {\mathrm{Cs}}}{1 , 6 0 2 1 7 6 6 3 4 \cdot 1 0 ^ {- 1 9} \cdot 9 1 9 2 6 3 1 7 7 0}. \\ \end{array}
$$

Die bis 2019 gültige Definition nach der DIN 1301 lautet: 1 Ampere (= 1 A) ist definiert durch die Stärke eines zeitlich konstanten Stromes durch zwei geradlinige, parallele, unendlich lange Leiter von vernachlässigbar kleinem Querschnitt, die einen Abstand von 1 m haben und zwischen denen die durch den Strom hervorgerufene Kraft im leeren Raum pro 1 m Leitungslänge $2 \cdot 1 0 ^ { - 7 }$ kg m $s ^ { - 2 }$ beträgt.

5. **Die Temperatur**: Die SI-Einheit für die Temperatur ist das Kelvin mit dem Einheitenzeichen K. Das Kelvin wird durch den festen Zahlenwert der Boltzmann-Konstante $k _ { \mathrm { B } }$ bestimmt. Wobei die Einheiten für das Kilogramm, den Meter und

---

1.1 Einheitensysteme

3

die Sekunde jeweils über die Konstanten h, c und $\Delta \nu _ { C s }$ definiert werden

$$
\begin{array}{l} 1 \mathrm{K} = 1 \frac {1 , 3 8 0 6 4 9 \cdot 1 0 ^ {- 2 3}}{k _ {\mathrm{B}}} \frac {\mathrm{kgm} ^ {2}}{\mathrm{s} ^ {2}} \\ = 1 \frac {1 , 3 8 0 6 4 9 \cdot 1 0 ^ {- 2 3}}{6 , 6 2 6 0 7 0 1 5 \cdot 1 0 ^ {- 3 4} \cdot 9 1 9 2 6 3 1 7 7 0} \frac {\Delta v _ {\mathrm{Cs}} \cdot h}{k _ {\mathrm{B}}}. \\ \end{array}
$$

Die bis 2019 gültige Definition nach der DIN 1301 lautet: 1 Kelvin (= 1 K) ist der 273,15te Teil der Differenz zwischen der Temperatur des absoluten Nullpunkts und der Temperatur, bei der die drei Zustandsformen des Wassers gleichzeitig auftreten (Tripelpunkt).

Der Zusammenhang zwischen der Kelvintemperatur T und der Celsiustemperatur ϑ ist gegeben durch

$$
\vartheta = T - 2 7 3, 1 5 \mathrm{K}.
$$

## 1.1.3 Einige abgeleitete Einheiten

1. **Die Kraft:** Wegen des Zusammenhangs Kraft = Masse × Beschleunigung definiert man:

$$
1 \mathrm{kg} \cdot 1 \frac {\mathrm{m}}{\mathrm{s} ^ {2}} = 1 \text {Newton} = 1 \mathrm{N}.
$$

Die Kraft 1 Newton erteilt also der Masse 1 kg die Beschleunigung von $1   \mathrm { { m }   s } ^ { - 2 }$

2. **Arbeit, Energie, Leistung:** Für die Einheit der Arbeit = Kraft × Weg schreibt man:

$$
1 \mathrm{N} \cdot 1 \mathrm{m} = 1 \text {Joule} = 1 \mathrm{J}.
$$

Demnach muss eine Arbeit von 1 J aufgewendet werden, wenn ein Körper mit der Kraft 1 N um 1 m verschoben wird.

**Die Leistung** = Arbeit pro Zeit erhält die Einheit

$$
\frac {1 \mathrm{Nm}}{1 \mathrm{s}} = \frac {1 \mathrm{J}}{1 \mathrm{s}} = 1 \mathrm{Watt} = 1 \mathrm{W}.
$$

3. **Wärmemenge:** Da es sich bei der Wärmemenge um eine Energie handelt, braucht keine neue Einheit definiert zu werden. Häufig begegnet man noch der älteren Einheit Kalorie ( cal). Mit einer Kalorie ist diejenige Energie gemeint, die man braucht, um 1 g Wasser von $^ { 1 4 ,   5   ^ { \circ } \mathrm { C } }$ auf $^ { 1 5 , 5 } ^ { \circ } \mathrm { C }$ zu erwärmen. Experimentell ergibt sich der Zusammenhang

$$
1 \mathrm{cal} \approx 4, 1 8 6 \mathrm{Ws}.
$$

In vielen praktischen Fällen sind die bis jetzt eingeführten Einheiten unhandlich. Sie können entweder zu groß oder zu klein sein. Dann kann vor die Einheit eines der in Tabelle 1.2 angegebenen Vorsatzzeichen gesetzt werden.

---

4

1 Einheiten, Gleichungen und grundlegende Begriffe

Tab. 1.2: Gebräuchliche Vorsatzzeichen und ihre Zehnerpotenzen.

<table><tr><td colspan="2">Vorsatzzeichen</td><td>Zehnerpotenz</td><td colspan="2">Vorsatzzeichen</td><td>Zehnerpotenz</td></tr><tr><td>Y</td><td>Yotta</td><td> $10^{24}$ </td><td>d</td><td>Dezi</td><td> $10^{-1}$ </td></tr><tr><td>Z</td><td>Zetta</td><td> $10^{21}$ </td><td>c</td><td>Zenti</td><td> $10^{-2}$ </td></tr><tr><td>E</td><td>Exa</td><td> $10^{18}$ </td><td>m</td><td>Milli</td><td> $10^{-3}$ </td></tr><tr><td>P</td><td>Peta</td><td> $10^{15}$ </td><td>μ</td><td>Mikro</td><td> $10^{-6}$ </td></tr><tr><td>T</td><td>Tera</td><td> $10^{12}$ </td><td>n</td><td>Nano</td><td> $10^{-9}$ </td></tr><tr><td>G</td><td>Giga</td><td> $10^{9}$ </td><td>p</td><td>Piko</td><td> $10^{-12}$ </td></tr><tr><td>M</td><td>Mega</td><td> $10^{6}$ </td><td>f</td><td>Femto</td><td> $10^{-15}$ </td></tr><tr><td>k</td><td>Kilo</td><td> $10^{3}$ </td><td>a</td><td>Atto</td><td> $10^{-18}$ </td></tr><tr><td>h</td><td>Hekto</td><td> $10^{2}$ </td><td>z</td><td>Zepto</td><td> $10^{-21}$ </td></tr><tr><td>da</td><td>Deka</td><td> $10^{1}$ </td><td>y</td><td>Yocto</td><td> $10^{-24}$ </td></tr></table>

## 1.2 Schreibweise von Gleichungen

## 1.2.1 Größengleichungen

Gleichungen werden in der Elektrotechnik im Allgemeinen als Größengleichungen geschrieben. Gleichungen dieser Form haben den Vorteil, dass sie für beliebige Einheiten richtig sind. Man hat dabei die physikalische Größe als Produkt aus Zahlenwert und Einheit in die Gleichung einzusetzen. Man schreibt z. B. für das Formelzeichen a:

$$
a = \{a \} \cdot [ a ]
$$

wobei $\{ a \}$ den Zahlenwert der Größe a bedeutet und [a] ihre Einheit. Zahlenwert und Einheit sind wie algebraische Größen zu behandeln.

Als Beispiel sei hier der Ausdruck für die Energie angegeben, die aufzuwenden ist, um einen Körper der Masse m und der spezifischen Wärmekapazität c um die Temperaturdifferenz $\Delta \vartheta$ zu erwärmen:

$$
W = c \cdot m \cdot \Delta \vartheta .
$$

Die Anwendung dieser Gleichung führt immer zu richtigen Ergebnissen, wenn man nur jede der Größen $W , c , m , \Delta \theta$ als Produkt aus Zahlenwert und Einheit auffasst. Beim Zusammenfassen der Einheiten auf der rechten Seite der Gleichung muss sich eine Energieeinheit ergeben

$$
[ W ] = [ c ] \cdot [ m ] \cdot [ \Delta \vartheta ] = \frac {\mathrm{J}}{\mathrm{kg} \cdot \mathrm{K}} \cdot \mathrm{kg} \cdot \mathrm{K} = \mathrm{J}.
$$

Das Rechnen mit Größengleichungen hat demnach auch den Vorteil, dass mögliche Fehler durch Einheitenkontrolle gefunden werden können. Diese einfache Methode zur Kontrolle von Gleichungen wird wärmstens empfohlen.

---

1.3 Die elektrische Ladung

5

## 1.2.2 Der Begriff Dimension

Will man deutlich machen, in welcher Form die Grundgrößen in die abgeleiteten Größen eingehen, so verwendet man den Begriff Dimension (dim) und schreibt z. B. für die Geschwindigkeit v als Quotient aus dem Weg l und der Zeit t:

$$
\dim (v) = \frac {\dim (l)}{\dim (t)}.
$$

Im SI heißen die Dimensionen wie ihre Grundgrößen, sie werden gekennzeichnet durch aufrechte, serifenlose Großbuchstaben, wie hier z. B. für das MKSA-System:

Länge: dim(l) = L, Masse: dim(m) = M, Zeit: dim(t) = T, Stromstärke: dim(I) = I.

Allgemein ergibt sich die Dimension einer aus diesen vier Grundgrößen abgeleiteten beliebigen Größe Q durch

$$
\dim (Q) = \mathsf {L} ^ {\alpha} \cdot \mathsf {M} ^ {\beta} \cdot \mathsf {T} ^ {\gamma} \cdot \mathsf {I} ^ {\delta} \qquad \text {mit} \quad \alpha , \beta , \gamma , \delta \in \mathbb {Z}
$$

mit der abgeleiteten Einheit

$$
[ Q ] = \mathrm{m} ^ {\alpha} \cdot \mathrm{kg} ^ {\beta} \cdot \mathrm{s} ^ {\gamma} \cdot \mathrm{A} ^ {\delta}.
$$

Für die Geschwindigkeit v ergibt sich zum Beispiel

$$
\dim (\nu) = \mathsf {L} ^ {1} \cdot \mathsf {M} ^ {0} \cdot \mathsf {T} ^ {- 1} \cdot \mathsf {I} ^ {0} \quad \text {und} \quad [ \nu ] = \mathsf {m} ^ {1} \cdot \mathsf {k g} ^ {0} \cdot \mathsf {s} ^ {- 1} \cdot \mathsf {A} ^ {0}.
$$

## 1.3 Die elektrische Ladung

Bestimmte elektrische Phänomene, die man mit einem geriebenen Bernsteinstab vorführen kann, sind schon seit dem Altertum bekannt. Das griechische Wort für Bernstein (= Elektron) hat der Elektrizität ihren Namen gegeben. Elektrizität kann nicht direkt be griffen werden. Sie ist nur durch ihre Erscheinungen erkennbar. Von einem geriebenen Bernsteinstab berührte Holundermarkkügelchen stoßen sich untereinander ab. Werden sie anschließend in die Nähe eines geriebenen Glasstabes gebracht, so zieht er sie zunächst an, stößt sie nach der Berührung jedoch ab. Diese Beobachtungen lassen sich nicht mit den aus der Mechanik bekannten Gravitationskräften erklären. Vielmehr han delt es sich hier um die Wirkungen einer neuen Größe, die man die **elektrische Ladung** nennt. Da zwischen Ladungen anziehende und abstoßende Kräfte auftreten können, muss es zwei verschiedene Ladungsarten bzw. Ladungen mit unterschiedlichen Vorzeichen geben. Willkürlich ordnet man den Ladungen eines geriebenen Glasstabes das positive Vorzeichen zu, den Ladungen eines geriebenen Bernsteinstabes das negative Vorzeichen. Damit lässt sich die oben beschriebene Erfahrungstatsache so formulieren: Gleichnamige Ladungen stoßen sich ab, ungleichnamige ziehen sich an.

---

6

1 Einheiten, Gleichungen und grundlegende Begriffe

![](../../raw/pages_0001-0032/images/page_15_image_2.jpg)

<details>
<summary>text_image</summary>

1. Schale
7. Schale
Hülle
Kern
○ Neutron
⊕ Proton
⊖ Elektron
</details>

Abb. 1.1: Das Bohr’sche Atommodell.

Ladungen lassen sich nicht in beliebig kleine Teilladungen aufteilen. Es gibt vielmehr eine kleinste Ladungsmenge, die so genannte **Elementarladung** e. Eine beliebige Ladung ist immer ein ganzzahliges Vielfaches $(n = 1,2,\cdots \infty)$ dieser Elementarladung:

$$
Q = n \cdot e \quad \text {mit} \quad n \in \mathbb {N}. \tag {1.1}
$$

Das Atom besteht aus einem Kern und einer Hülle. Den Kern bilden **Protonen**, die jeweils die Ladung +e tragen, und **Neutronen**, die ungeladen sind. Die den Kern auf bis zu sieben Schalen umkreisenden **Elektronen**, die alle die Ladung −e haben, stellen die Atomhülle dar. Die Ladungen von Kern und Hülle sind gleich groß, jedoch von entgegengesetztem Vorzeichen, so dass das Atom insgesamt elektrisch neutral ist. Als Träger der Masse des Atoms ist im Wesentlichen der Kern anzusehen, da die Elektro nen eine etwa 1840-mal kleinere Masse als die Protonen und die Neutronen besitzen. Das hier skizzierte Atommodell in Bild 1.1 geht auf die Vorstellungen von Nils Bohr zurück und wird wegen der nahe liegenden Analogie als Bohr’sches Planetenmodell des Atoms bezeichnet. Die Elektronen eines Atoms sind umso stärker an den Kern»gebunden«, je geringer der Abstand zwischen Kern und Elektron ist. Bei manchen Stoffen lassen sich Elektronen der äußersten Schale wegen der geringeren Bindekräfte aus dem Atomverband herauslösen. Es entsteht ein positives **Ion** (= Kation). Nimmt dagegen die äußerste Schale Elektronen auf, so erhält man ein negatives Ion (= Anion).

## 1.4 Der elektrische Strom

Der Strom kann mit einer Flüssigkeitsmenge verglichen werden, die innerhalb einer bestimmten Zeit einen gegebenen Querschnitt durchströmt. Die Stärke der Strömung charakterisiert man durch den Quotienten aus Menge und Zeit und nennt ihn die Stromstärke oder einfach den Strom. Zusätzlich ist der Strom durch seine Richtung gekennzeichnet. Entsprechend definiert man den **elektrischen Strom**:

$$
I _ {\mathrm{m}} = \frac {\Delta Q}{\Delta t}. \tag {1.2}
$$

---

1.4 Der elektrische Strom

7

Dabei bedeuten ∆Q die innerhalb des Zeitraums ∆t durch den betrachteten Querschnitt hindurchtretende Ladung und $I _ { \mathbf { m } }$ die mittlere Stromstärke während des Zeitraums ∆t. Wenn zu gleichen Zeitintervallen $\Delta t$ unterschiedliche Ladungen gehören, gibt man den Augenblickswert des Stromes an:

$$
i (t) = \lim _ {\Delta t \to 0} \frac {\Delta Q}{\Delta t} = \frac {\mathrm{d} Q}{\mathrm{d} t}. \tag {1.3}
$$

Löst man die Gl. (1.2) nach der Ladung auf, erhält man die während des Zeitraums ∆t transportierte Ladung:

$$
\Delta Q = I _ {\mathrm{m}} \Delta t. \tag {1.4}
$$

Ist die Stromstärke während des Zeitraums $\Delta t$ konstant, so schreibt man an Stelle des Mittelwertes $I _ { \mathbf { m } }$ einfach I:

$$
\Delta Q = I \Delta t. \tag {1.5}
$$

Bei beliebigem zeitlichen Verlauf des Stromes kann die Ladung, die zwischen den Zeitpunkten $t _ { 1 }$ und $t _ { 2 }$ durch den betrachteten Querschnitt hindurchtritt, wegen Gl. (1.3) durch folgende Integration bestimmt werden:

$$
Q = \int_ {t _ {1}} ^ {t _ {2}} i (t) \mathrm{d} t. \tag {1.6}
$$

Zeitlich konstante Größen werden durch große Buchstaben gekennzeichnet (z. B. Strom I), zeitlich veränderliche Größen dagegen durch kleine Buchstaben (z. B. Strom i). Die durch die Gln. (1.2) bis (1.6) beschriebenen Zusammenhänge werden in Bild 1.2 veranschaulicht, und zwar einmal für einen zeitlich konstanten Strom, man spricht hier von einem **reinen Gleichstrom**. Im anderen Fall ist der Strom eine periodische Funktion mit der Periode T, wobei innerhalb dieser Periode genau so viel Ladung in der einen wie in der anderen Richtung, im Mittel also gar keine Ladung transportiert wird. Einen solchen Strom nennt man einen **reinen Wechselstrom**. Da die Ladung nach Gleichung (1.1) ein Vielfaches der Elementarladung e, bzw. nach Gleichung (1.6) die zeitliche Integration des Stromes ist, ist die Einheit Ladung gleich der Einheit der Elementarladung

$$
[ \Delta Q ] = [ n ] [ e ] = [ I ] [ \Delta t ] = 1 \mathrm{A} \cdot 1 \mathrm{s}.
$$

Damit ist die Einheit der Ladung 1 Amperesekunde. Da diese Einheit häufig vorkommt, hat sie einen speziellen Namen erhalten:

$$
1 \mathrm{As} = 1 \text {Coulomb} = 1 \mathrm{C}.
$$

Dem elektrischen Strom ist willkürlich eine Richtung zugeordnet worden: Man be trachtet die Bewegungsrichtung positiver Ladungsträger als die positive Stromrichtung und spricht auch von der **konventionellen** oder **technischen Stromrichtung**. Die Bewegungsrichtung der negativen Elektronen wie z. B. in einer Elektronenröhre stimmt

---

8

1 Einheiten, Gleichungen und grundlegende Begriffe

![](../../raw/pages_0001-0032/images/page_17_chart_2.jpg)

<details>
<summary>line</summary>

| Time (t) | Q(t) | i(t) |
| --- | --- | --- |
| 0 | 0 | Positive Peak |
| t1 | Steigung | Negative Trough |
| T/2 | Steigung | Zero Crossing |
| T | Steigung | Positive Peak |
</details>

Abb. 1.2: Zusammenhang zwischen transportierter Ladung und Stromstärke. (a) reiner Gleichstrom (b) reiner Wechselstrom.

dann also nicht mit der konventionellen Stromrichtung überein (Bild 1.3). Man teilt die Stoffe nach ihrer Fähigkeit, den Strom zu leiten, in **Leiter**, **Nichtleiter** und **Halbleiter** ein. Zu den Leitern gehören die Metalle und die Elektrolyte (Säuren und Salzlösungen). Bei diesen Stoffen sind die Ladungsträger frei beweglich. Halbleiter unterscheiden sich in dieser Hinsicht nicht von den Leitern, nur ist die Dichte der frei beweglichen Ladungsträger um Zehnerpotenzen geringer. Beispiele für Halbleiter sind Silizium, Germanium, Selen. Nichtleiter besitzen dagegen keine frei beweglichen Ladungsträger. Hier sind nur geringe Ladungsverschiebungen oder Drehungen (bei Dipolen) möglich. Als Beispiele für Nichtleiter seien genannt: Porzellan, Gummi, Hartpapier.

Die frei beweglichen Ladungsträger in Metallen bewegen sich ungeordnet auf Zickzackbahnen (»Elektronengas«, »Elektronenwolke«). Ein Strom durch den Leiter kommt erst zustande, wenn sich dieser statistisch verteilten Bewegung eine Bewegung in einer Vorzugsrichtung überlagert (Driftbewegung).

Der elektrische Strom ist im Wesentlichen durch drei Wirkungen gekennzeichnet:

![](../../raw/pages_0001-0032/images/page_17_image_7.jpg)

Abb. 1.3: a) Konventionelle Stromrichtung; b) Bewegungsrichtung der Elektronen in einer Elektronenröhre.

---

1.5 Die elektrische Spannung

9

1. Jeder Strom ist von einem Magnetfeld begleitet (Bild 1.4). Seine Wirkung lässt sich z. B. zur Messung durch ein Drehspulinstrument auswerten.
2. Der Stromfluss ist vor allem bei den Elektrolyten mit einem Stofftransport verbunden. Früher wurde die Einheit der Stromstärke durch das sog. »Silberampere«definiert, d. h. durch die bei Stromfluss innerhalb einer gewissen Zeit aus einer Silbersalzlösung ausgeschiedene Menge Silber.
3. Ein von einem Strom durchflossener Leiter erwärmt sich. Diese Wirkung wird bei der Strommessung durch Hitzdrahtamperemeter ausgenutzt.

## Beispiel 1.1: Geschwindigkeit freier Elektronen im Leiter.

Durch einen Kupferdraht mit dem Querschnitt $A = 50    mm ^2$ fließt der Strom $I = 2 0 0   \mathrm { A }$ Wie groß ist die mittlere Geschwindigkeit (Driftgeschwindigkeit) der freien Elektronen, wenn deren Dichte $N = 8 , 5 \cdot 1 0 ^ { 1 9 }   \mathrm { m m } ^ { - 3 }$ beträgt?

## Lösung:

Der Weg ∆x wird in der Zeit ∆t zurückgelegt. Während dieser Zeit wird die Ladung

$$
\Delta Q = I \Delta t \quad \text { mit } \quad \Delta Q = e N \Delta x A
$$

transportiert (Bild 1.5). Damit folgt

$$
\frac {\Delta x}{\Delta t} = \nu = \frac {I}{e N A} \approx 0, 3 \frac {\mathrm{mm}}{\mathrm{s}}.
$$

## 1.5 Die elektrische Spannung

Im letzten Abschnitt wurde die Frage nach der Ursache für den elektrischen Strom offengelassen. Es liegt nahe, dass eine Kraft erforderlich ist, um die Ladungen im Leiter zu bewegen, und dass mit der Bewegung ein Energieumsatz verbunden ist. Das wird verdeutlicht an Hand von Bild 1.6, in dem zwei Ladungen $Q$ und $q$ dargestellt sind. Haben beide Ladungen gleiches Vorzeichen, so stoßen sie sich nach Abschnitt 1.3 ab. Bei einer Bewegung der Ladung q von A nach B nimmt die potentielle Energie dieser Ladung ab, etwa von $W _ { A }$ auf $W _ { B }$ . Die Energiedifferenz wird in kinetische Energie umgewandelt. Damit ist der Vorgang analog zur Bewegung einer Masse im Schwerefeld der Erde: Ein von A nach B fallender Stein gewinnt eine kinetische Energie, die gleich

![](../../raw/pages_0001-0032/images/page_18_image_15.jpg)

<details>
<summary>text_image</summary>

magnetische
Feldlinie
S
I
Magnetnadel richtet
sich aus.
N
</details>

Abb. 1.4: Magnetische Wirkung des elektrischen Stromes.

---

10

1 Einheiten, Gleichungen und grundlegende Begriffe

![](../../raw/pages_0001-0032/images/page_19_image_2.jpg)

<details>
<summary>text_image</summary>

I
Δx
I
</details>

Abb. 1.5: Zur Berechnung der Driftgeschwindigkeit.

![](../../raw/pages_0001-0032/images/page_19_image_4.jpg)

<details>
<summary>text_image</summary>

+q
A
B
+Q
(q, Q > 0)
</details>

Abb. 1.6: Zur Änderung der potentiellen Energie beim Verschieben der Ladung q von A nach B.

der Abnahme seiner potentiellen Energie ist. So wie diese potentielle Energie der Masse proportional ist, so erweist sich die potentielle Energie des Ladungsträgers als der Ladung proportional:

$$
W _ {A} - W _ {B} \sim q.
$$

Man führt als Proportionalitätsfaktor auf der rechten Seite die **elektrische Spannung** ein, die mit U bezeichnet wird. Damit haben wir

$$
\frac {W _ {A} - W _ {B}}{q} = \frac {W _ {A B}}{q} = U _ {A B}, \tag {1.7}
$$

wobei der Index bei U ausdrückt, dass die Spannung zwischen den Punkten A und B gemeint ist.

Ganz allgemein nennt man eine Einrichtung, in der die bewegten Ladungen potentielle Energie abgeben, einen **Verbraucher** und den Quotienten nach Gl. (1.7) den **Spannungsabfall** U (oder einfach die Spannung U an dem Verbraucher). Einrichtungen, die die potentielle Energie der Ladungen erhöhen, bezeichnet man als **Erzeuger** , Spannungsquellen oder Generatoren und die gemäß Gl. (1.7) definierte Spannung als **Quellenspannung** $U _ { \mathrm { q } }$ oder U.

Die Ausdrücke Verbraucher und Erzeuger haben sich eingebürgert, obwohl in ihnen Energie weder verbraucht noch erzeugt, sondern nur in andere Energieformen umgesetzt wird, z. B. elektrische Energie in Wärme im stromdurchflossenen Leiter oder mechanische in elektrische Energie in der Dynamomaschine.

Die Richtung der Spannung wählt man bei einem Verbraucher im Allgemeinen genauso wie die des Stromes. (Die möglichen Zuordnungen kommen in Abschnitt 2.4.1 zur Sprache.) Damit gibt der Spannungspfeil die Bewegungsrichtung der positiven Ladungsträger bei Abgabe potentieller Energie an. Bei Zunahme der potentiellen Energie – also bei Generatoren – ist konsequenterweise der Spannungspfeil entgegengesetzt zum Strompfeil einzutragen (Bild 1.7). Den Anschlussklemmen von Verbrauchern und Generatoren ordnet man Vorzeichen zu, und zwar so, dass außerhalb des Generators der Strom vom positiven zum negativen Pol oder Anschluss fließt, somit innerhalb des

---

1.6 Der elektrische Widerstand

11

![](../../raw/pages_0001-0032/images/page_20_image_2.jpg)

Abb. 1.7: Richtung von Strom und Spannung bei Verbrauchern und Erzeugern.

Generators vom negativen zum positiven Anschluss (Bild 1.7). Die Spannung ist bei Verbrauchern und Generatoren stets vom Pluspol zum Minuspol gerichtet. Aus Gl. (1.7) ergibt sich eine mögliche Einheit der Spannung zu

$$
[ U ] = \frac {[ W ]}{[ q ]} = \frac {1 \mathrm{J}}{1 \mathrm{As}} = \frac {1 \mathrm{W}}{1 \mathrm{A}},
$$

wofür man abkürzend schreibt:

$$
\frac {1 \mathrm{W}}{1 \mathrm{A}} = 1 \mathrm{Volt} = 1 \mathrm{V}.
$$

## 1.6 Der elektrische Widerstand

Um einen elektrischen Strom durch einen Leiter zu treiben, ist Energie erforderlich, da der Leiter der freien Bewegung der Ladungen einen Widerstand entgegensetzt. Je größer der Strom durch den Leiter (Bild 1.8) werden soll, desto größer muss im allgemeinen die Spannung zwischen den Leiterenden A und B sein. Man definiert als **Widerstand** $R _ { \mathrm { A B } }$ des Leiters den Quotienten aus Spannung $U _ { \mathrm { A B } }$ und Strom I:

$$
R _ {\mathrm{AB}} = \frac {U _ {\mathrm{AB}}}{I}. \tag {1.8}
$$

Dieser Quotient kann vom Strom abhängen, aber auch konstant sein (s. Abschnitt 2.1.1). In manchen Fällen, z. B. zur Charakterisierung nichtlinearer Zweipole (Abschnitt 2.5.1), ist es zweckmäßig, mit einem **differenziellen Widerstand** $r _ { \mathrm { A B } }$ zu arbeiten, der so definiert ist:

$$
r _ {\mathrm{AB}} = \frac {\mathrm{d} U _ {\mathrm{AB}}}{\mathrm{d} I}. \tag {1.9}
$$

Eine Einheit des Widerstandes kann aus Gl. (1.8) hergeleitet werden:

$$
[ R ] = \frac {[ U ]}{[ I ]} = \frac {1 \mathrm{V}}{1 \mathrm{A}}.
$$

![](../../raw/pages_0001-0032/images/page_20_image_15.jpg)

Abb. 1.8: Zur Definition des Widerstandes $R _ { \mathsf { A B } }$

---

12

1 Einheiten, Gleichungen und grundlegende Begriffe

Für den Quotienten schreibt man abkürzend

$$
1 \frac {\mathrm{V}}{\mathrm{A}} = 1 \mathrm{Ohm} = 1 \Omega .
$$

Den Kehrwert des Widerstandes R nennt man den **Leitwert** G

$$
G = \frac {1}{R} \tag {1.10}
$$

mit der möglichen Einheit $\Omega ^ { - 1 }$ , die einen speziellen Namen erhalten hat:

$$
\frac {1}{\Omega} = 1 \text {Siemens} = 1 \mathrm{S}.
$$

Bei einem homogenen Leiter von gleichbleibendem Querschnitt A und der Länge l ist der Widerstand erfahrungsgemäß der Länge proportional und dem Querschnitt umgekehrt proportional:

$$
R \sim \frac {l}{A}.
$$

Den Proportionalitätsfaktor auf der rechten Seite nennt man den **spezifischen Widerstand** $\varrho$ des Leitermaterials, seinen Kehrwert bezeichnet man als die **elektrische Leitfähigkeit** $\gamma .$ Damit hat man

$$
R = \varrho \frac {l}{A} = \frac {l}{\gamma A}. \tag {1.11}
$$

Für die Leitfähigkeit werden vielfach auch die Bezeichnungen $\sigma$ und κ verwendet. Wir halten uns jedoch hier wie an anderen Stellen an die Empfehlungen von DIN 1304 und ziehen die Bezeichnung γ vor.

Als Einheiten für die Größen ϱ und γ lassen sich mit (1.11) herleiten:

$$
[ \varrho ] = \frac {[ R ] [ A ]}{[ l ]} = \frac {\Omega \mathrm{m} ^ {2}}{\mathrm{m}} = \Omega \mathrm{m}
$$

$$
[ \gamma ] = \frac {[ l ]}{[ R ] [ A ]} = \frac {\mathrm{m}}{\Omega \mathrm{m} ^ {2}} = \frac {\mathrm{S}}{\mathrm{m}}.
$$

## Beispiel 1.2: »Widerstandsnormal«.

Ein Quecksilberfaden von 1 mm<sup>2</sup> Querschnitt soll als »Widerstandsnormal« dienen und den Widerstand 1 Ω haben. Wie lang muss der Faden sein, wenn der spezifische Widerstand von Quecksilber 0,958 $\Omega \frac { \mathrm { m m } ^ { 2 } } { \mathrm { m } }$ beträgt?

## Lösung:

Gl. (1.11) wird nach l aufgelöst:

$$
l = \frac {R A}{\varrho} = \frac {1 \Omega \cdot 1 \mathrm{mm} ^ {2}}{0 , 9 5 8 \Omega \frac {\mathrm{mm} ^ {2}}{\mathrm{m}}} \approx 1, 0 4 \mathrm{m}.
$$

---

1.7 Energie und Leistung

13

## 1.7 Energie und Leistung

Wird eine elektrische Ladung von einem Punkt zu einem anderen bewegt und besteht zwischen diesen beiden Punkten die zeitlich konstante Spannung U, so ist diese Bewegung nach Gl. (1.7) mit einem Energieumsatz von

$$
W = Q U \tag {1.12}
$$

verbunden. Ist nun die Spannung nicht mehr zeitlich konstant, so dass während eines ersten Zeitintervalls $\Delta t _ { 1 }$ die von der Ladung $\Delta Q _ { 1 }$ durchlaufene Spannung $U _ { 1 }$ beträgt und im nächsten Zeitintervall $\Delta t _ { 2 }$ dann zu der Ladung $\Delta Q _ { 2 }$ die Spannung $U _ { 2 }$ gehört usw., so erhält man an Stelle von Gl. (1.12):

$$
W = U _ {1} \Delta Q _ {1} + U _ {2} \Delta Q _ {2} + \dots \tag {1.13}
$$

Durchläuft z. B. die Ladung $\Delta Q _ { 1 }$ die Spannung $U _ { 1 }$ in der Zeit $\Delta t _ { 1 }$ , so kann man für $\Delta Q _ { 1 }$ wegen Gl. (1.5) auch schreiben:

$$
\Delta Q _ {1} = I _ {1} \Delta t _ {1}.
$$

Entsprechendes gilt für die anderen Summanden in Gl. (1.13), so dass folgt:

$$
W = U _ {1} I _ {1} \Delta t _ {1} + U _ {2} I _ {2} \Delta t _ {2} + \dots = \sum_ {k} U _ {k} I _ {k} \Delta t _ {k}.
$$

Hierbei werden $U _ { k }$ und $I _ { k }$ während der Zeitintervalle $\Delta t _ { k }$ als konstant angesehen (daher große Buchstaben). Geht man zum Grenzwert der Summe $( \Delta t _ { k } \rightarrow 0 )$ und damit zum Integral über, so erhält man die zwischen den Zeitpunkten $t _ { 1 }$ und $t _ { 2 }$ umgesetzte elektrische Energie:

$$
W = \int_ {t _ {1}} ^ {t _ {2}} u (t) i (t) \mathrm{d} t. \tag {1.14}
$$

Für den Sonderfall eines reinen Gleichstroms (u und i sind konstant) wird die im Zeitraum t umgesetzte Energie

$$
W = U I t. \tag {1.15}
$$

Eine mögliche Einheit der Energie ergibt sich wegen Gl. (1.15) zu

$$
[ W ] = [ U ] [ I ] [ t ] = 1 \mathrm{V} \cdot 1 \mathrm{A} \cdot 1 \mathrm{s} = 1 \mathrm{Ws} = 1 \mathrm{J},
$$

womit wir uns in Übereinstimmung mit Abschnitt 1.1.3 befinden. Für viele Zwecke, z. B. bei einem Energieversorger, ist die Maßeinheit Ws zu klein, dann verwendet man oft die Einheit Kilowattstunde:

$$
1 \mathrm{kWh} = 3, 6 \cdot 1 0 ^ {6} \mathrm{Ws}.
$$

---

14

1 Einheiten, Gleichungen und grundlegende Begriffe

Gelegentlich braucht man die folgenden Umrechnungen:

$$
1 \mathrm{Ws} = 0, 1 0 2 \mathrm{kp} \mathrm{m} = 0, 2 3 9 \mathrm{cal},
$$

$$
1 \mathrm{kWh} = 8 6 0 \mathrm{kcal}.
$$

In Abschnitt 1.1.3 wurde die Leistung als Arbeit pro Zeit definiert, also

$$
P = \frac {W}{t},
$$

womit nach Gl. (1.15) für Gleichstrom herauskommt

$$
P = U I. \tag {1.16}
$$

Ist die Leistung eine zeitlich veränderliche Größe, so wird der zeitliche Mittelwert der im Zeitraum ∆t umgesetzten Leistung

$$
P _ {\mathrm{m}} = \frac {\Delta W}{\Delta t}
$$

und der Augenblickswert

$$
p (t) = \lim _ {\Delta t \to 0} \frac {\Delta W}{\Delta t} = \frac {\mathrm{d} W}{\mathrm{d} t}. \tag {1.17}
$$
