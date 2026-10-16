# 34 Elektrische Schwingungen

原始 PDF 第 376–382 页。

34

Elektrische Schwingungen

## 34.1 Der geschlossene Schwingkreis

Eine Parallelschaltung eines Kondensators (Kapazität C) und einer Spule (Induktivität L) bezeichnet man als geschlossenen **Schwingkreis**. Wurde der Kondensator in Bild 34.1 bei Schalterstellung 1 aufgeladen, kann sich die im Kondensator gespeicherte Ladung +Q und −Q durch einen Stromfluss i über die Spule ausgleichen, sobald der Schalter in Stellung 2 gebracht wird. Spannung und elektrische Feldstärke des Kondensators nehmen ab, und gleichzeitig baut sich mit dem durch die Spule fließenden Strom ein Magnetfeld auf. Die Zunahme des magnetischen Flusses induziert eine Gegenspannung, welche nur ein gebremstes Anwachsen des Stromes zulässt. Sind Spannung und elektrische Feldstärke des Kondensators null, haben Strom und magnetische Feldstärke in der Spule ihren größten Wert erreicht. Die elektrische Feldenergie ist vollständig in magnetische Feldenergie umgewandelt. Mit dem Ladungsausgleich entfällt die Ursache des Entladestroms, und das Magnetfeld muss zusammenbrechen. Die Abnahme des Magnetflusses induziert eine Spannung, die jetzt so gerichtet ist, dass der Strom in gleicher Richtung weiterfließt und nur allmählich abnehmen kann. Gleichzeitig wird der Kondensator mit umgekehrter Polarität erneut aufgeladen. Spannung und elektrische Feldstärke steigen entgegengesetzt zur Ausgangsrichtung an und erreichen ihren größten Wert, wenn das Magnetfeld verschwunden ist. Dann wiederholt sich der Vorgang mit umgekehrter Richtung und im weiteren Verlauf periodisch.

**Im Schwingkreis findet eine periodische gegenseitige Umwandlung von elektrischer und magnetischer Feldenergie statt (elektromagnetische Schwingung).**

![](../../raw/pages_0353-0384/images/page_375_image_5.jpg)

<details>
<summary>text_image</summary>

1
2
i
+
-
C
L
</details>

Bild 34.1 Erregung eines geschlossenen elektrischen Schwingkreises

**Herleitung der Schwingungsdifferenzialgleichung.** Induktivität und Kapazität sind im geschlossenen Schwingkreis parallel geschaltet. Daher sind die in der Spule induzierte Spannung (30.7) und die am Kondensator anliegende Spannung (23.29) gleich:

$$
u = - L \frac {\mathrm{d} i}{\mathrm{d} t} = \frac {q}{C}. \tag {34.1}
$$

Differenziation dieser Gleichung nach der Zeit und Umstellen ergeben

$$
L \frac {\mathrm{d} ^ {2} i}{\mathrm{d} t ^ {2}} + \frac {1}{C} \frac {\mathrm{d} q}{\mathrm{d} t} = 0.
$$

---

374

34 Elektrische Schwingungen

Mit $\mathbf { d } q / \mathbf { d } t \equiv i$ folgt für den Schwingkreis somit die Differenzialgleichung des harmonischen Oszillators (33.2) mit (33.6), in der m und k hier den Größen L und 1/C entsprechen:

$$
\frac {\mathrm{d} ^ {2} i}{\mathrm{d} t ^ {2}} + \omega_ {0} ^ {2} i = 0 \quad \text {mit} \quad \omega_ {0} = 2 \pi f _ {0} = \frac {1}{\sqrt {L C}}.
$$

Es ist also analog zu (33.7):

$$
T = \frac {1}{f _ {0}} = 2 \pi \sqrt {L C} \quad \begin{array}{l} (\text {Periodendauer der ungedämpften} \\ \text {elektrischen Schwingung;} \\ \text {THOMSONsche Schwingungsgleichung}). \end{array} \tag {34.2}
$$

Man gewinnt den Energieerhaltungssatz für den Schwingkreis, wenn (34.1) mit $i \equiv \mathbf { d } q / \mathbf { d } t$ multipliziert und umgeformt wird. Mit (30.10) als magnetische und (24.11) als elektrische Feldenergie folgt

$$
L i \frac {\mathrm{d} i}{\mathrm{d} t} + \frac {1}{C} q \frac {\mathrm{d} q}{\mathrm{d} t} = \frac {\mathrm{d}}{\mathrm{d} t} \left(\frac {L}{2} i ^ {2} + \frac {1}{2 C} q ^ {2}\right) = \frac {\mathrm{d} E}{\mathrm{d} t} = 0, \quad \text {d.h.} \quad E = \frac {L}{2} i ^ {2} + \frac {1}{2 C} q ^ {2} = \text {const.}
$$

**Analogiebeziehungen.** Linearer Federschwinger, Drehschwinger und elektrischer Schwing kreis zeigen ohne äußere Anregung ein völlig analoges Schwingungsverhalten und werden unter dem abstrakten Begriff des harmonischen Oszillators zusammengefasst. Die Ursache dafür, dass äußerlich so verschiedenartige Systeme sich gleichartig verhalten, liegt in derselben Struktur der Energiebilanz dieser Oszillatoren begründet. Es gilt für den

$$
\begin{array}{l l} \text {Federschwinger:} & \frac {m}{2} \dot {u} ^ {2} + \frac {k}{2} u ^ {2} = E = \text {const} \\ \text {(vgl. 33.2)} \end{array}
$$

$$
\begin{array}{l l} \text {Drehschwinger:} & \frac {J}{2} \dot {\varphi} ^ {2} + \frac {D}{2} \varphi^ {2} = E = \text {const} \\ \text {(vgl. 33.3)} \end{array}
$$

$$
\begin{array}{l l} \text {elektrischen} & \frac {L}{2} i ^ {2} + \frac {1}{2 C} q ^ {2} = E = \text {const.} \\ \text {Schwingkreis:} \end{array}
$$

Den Energieverlusten durch Reibung bei mechanischen Schwingern entspricht beim Schwing kreis die Entstehung JOULEscher Wärme in einem OHMschen Widerstand; der geschwindigkeitsproportionalen Reibungskraft in (33.21) $F _ { \mathrm { R } }   =   \beta \dot { u }$ entspricht der Spannungsabfall $u _ { R } = R \dot { q } = R i$ am Widerstand R.

Daraus lässt sich für das Schwingungsverhalten ein widerspruchsfreies System von Analogiebeziehungen aufbauen (s. Tabelle 34.1). Es genügt dann die Lösung eines Problems; die Lösung der beiden anderen kann durch formales Einsetzen der zeitabhängigen und zeitunabhängigen Größen direkt angegeben werden. Auf diese Weise können schwer darstellbare (meist mechanische) Vorgänge in technischen Anlagen, die optimiert werden sollen, durch andere (meist elektrische) Vorgänge modelliert werden. An den Modellen wird dann bei vergleichsweise geringem Aufwand das Verhalten des Systems bei Änderung verschiedener Parameter untersucht.

## Beispiel 34.1:

Mit einem Drehkondensator der veränderlichen Kapazität $C = 6 0 \dots 3 9 0   \mathrm { p F }$ soll ein Schwingkreis aufgebaut werden, dessen Eigenfrequenz das Frequenzband $f = 4 0 0   \mathrm { k H z }$ bis 1MHz überstreicht. In welchem Bereich muss die Induktivität der Spule liegen?

Lösung: Nach (34.2) ist $L = 1 / ( 4 \pi ^ { 2 } f _ { 0 } ^ { 2 } C )$ . Mit $f _ { 0 } = 4 0 0   \mathrm { k H z }$ und $C = 3 9 0   \mathrm { p F }$ ist $L = 4 0 6   \mu \mathrm { H }$ die untere Grenze; mit $f _ { 0 } = 1$ MHz und $C = 6 0   \mathrm { p F }$ ist $L = 4 2 2   \mu \mathrm { H }$ die obere Grenze. □

---

34.2 Strom- und Spannungsresonanz

375

Tabelle 34.1 Analogiebeziehungen zwischen Größen für Translations-, Rotations- und elektrische Schwingungen

<table><tr><td></td><td>Translations-schwingungen</td><td>Rotationsschwin-gungen</td><td>elektrische Schwingungen</td></tr><tr><td>kinetische Energie</td><td> $\frac{m}{2} \dot{u}^{2}$ </td><td> $\frac{J}{2} \dot{\varphi}^{2}$ </td><td> $\frac{L}{2} i^{2}$ </td></tr><tr><td>potenzielle Energie</td><td> $\frac{k}{2} u^{2}$ </td><td> $\frac{D}{2} \varphi^{2}$ </td><td> $\frac{1}{2C} q^{2}$ </td></tr><tr><td rowspan="2">zeitabhängige Größen</td><td> $\dot{u}$ </td><td> $\dot{\varphi}$ </td><td> $\dot{q} = i$ </td></tr><tr><td> $u$ </td><td> $\varphi$ </td><td> $q = \int i \, dt$ </td></tr><tr><td rowspan="3">zeitunabhängige Konstanten</td><td> $m$ </td><td> $J$ </td><td> $L$ </td></tr><tr><td> $\beta$ </td><td> $\beta_{\varphi}$ </td><td> $R$ </td></tr><tr><td> $k$ </td><td> $D$ </td><td> $1/C$ </td></tr><tr><td>Eigenkreisfrequenz</td><td> $\omega_{0} = \sqrt{\frac{k}{m}}$ </td><td> $\omega_{0} = \sqrt{\frac{D}{J}}$ </td><td> $\omega_{0} = \frac{1}{\sqrt{LC}}$ </td></tr><tr><td>Dämpfungskonstante</td><td> $\delta = \frac{\beta}{2m}$ </td><td> $\delta = \frac{\beta_{\varphi}}{2J}$ </td><td> $\delta = \frac{R}{2L}$ </td></tr></table>

## 34.2 Strom- und Spannungsresonanz

Ebenso wie bei mechanischen Oszillatoren kann man auch das Mitschwingen von elektrischen Schwingkreisen durch Erregung von außen erzwingen. Da man eine Induktivität L und eine Kapazität C parallel oder in Reihe schalten kann, sind zwei Möglichkeiten der Anregung zu unterscheiden. Bild 34.2 zeigt einen Parallelkreis, der durch einen eingespeisten Wechselstrom i(t), und einen Reihenkreis, der durch eine angelegte Wechselspannung u(t) von außen zu erzwungenen Schwingungen angeregt wird. Beide Quellen seien ideal, d. h., die zeitlichen Verläufe von u(t) und i(t) werden durch die internen Vorgänge im Schwingkreis nicht beeinflusst.

![](../../raw/pages_0353-0384/images/page_377_image_6.jpg)

Bild 34.2 Anregung a) eines Parallelschwingkreises durch eine Wechselstromquelle mit $i = I_{0} \sin \omega t,  b$ eines Reihenschwingkreises durch eine Wechselspannungsquelle mit $u = U _ { 0 }$ sinωt zu erzwungenen Schwingungen.

**Parallelschwingkreis** (Bild 34.2a). Der fremderregte Parallelkreis entspricht im zeitlichen Ablauf seiner erzwungenen Schwingungen dem fremderregten Federschwinger (Bild 33.7). Durch den Wechselstrom $i = i _ { 0 } \sin \omega t$ wird dem Kondensator C fortwährend Ladung $q = \int i   \mathbf { d } t \; \mathbf { z } \mathbf { u } -$ und abgeführt, so wie beim Federschwinger durch den Erregerausschlag $x = x _ { 0 }$ sinωt dauernd der Aufhängepunkt seiner Feder bewegt wird. $q$ und x sind entsprechende permanente Störungen des Gleichgewichtszustandes, denen Ausgleichsvorgänge des Schwingungssystems folgen, die jedoch vom Rhythmus der Störungen synchronisiert werden. Stimmt aber die Pe-

---

376

34 Elektrische Schwingungen

riodendauer des Wechselstroms und der Eigenschwingung überein (Resonanz), beginnt die Ladungszufuhr durch die Stromquelle immer in dem Moment, wenn die Kapazität C gerade mit der Entladung über die Induktivität L beginnt. Daher steigen die Stromamplituden der er zwungenen Schwingung und die Schwingungsenergie von Periode zu Periode an (Einschwingvorgang), bis die gleichzeitig steigenden Energieverluste im OHMschen Widerstand R die laufend zugeführten Energiemengen gerade kompensieren (eingeschwungener Zustand).

## Stromresonanz: Im Parallelschwingkreis werden hohe Stromstärken erzwungen, wenn dessen Eigenfrequenz mit der Erregerfrequenz übereinstimmt.

Herleitung der Schwingungsgleichung: Da die Kapazität C zur Induktivität L mit dem Widerstand R parallel geschaltet ist (Bild 34.2a), liegt an beiden dieselbe Spannung an: $u _ { L }   +   u _ { R } = u _ { C }$ . Setzt man hierin die Spannungsabfälle $u _ { L } = L ( \mathbf { d } i _ { L } / \mathbf { d } t ) , \; u _ { R } = R i _ { L }$ sowie $u _ { C } = ( 1 / C ) \int i _ { C }   \mathrm { d } t$ ein, dividiert durch L und differenziert einmal nach $t ,$ erhält man

$$
\frac {\mathrm{d} ^ {2} i _ {L}}{\mathrm{d} t ^ {2}} + \frac {R}{L} \frac {\mathrm{d} i _ {L}}{\mathrm{d} t} = \frac {1}{L C} i _ {C}.
$$

Mit Hilfe der Analogiebeziehungen in 34.1, Tabelle 34.1, und unter Berücksichtigung des Knotensatzes (25.17) $i _ { C } = i - i _ { L }$ entsteht daraus die Differenzialgleichung

$$
\frac {\mathrm{d} ^ {2} i _ {L}}{\mathrm{d} t ^ {2}} + 2 \delta \frac {\mathrm{d} i _ {L}}{\mathrm{d} t} + \omega_ {0} ^ {2} i _ {L} = \omega_ {0} ^ {2} i = \omega_ {0} ^ {2} i _ {0} \sin \omega t. \tag {34.3}
$$

Diese ist völlig analog zur Bewegungsgleichung (33.29) des zu erzwungenen Schwingungen angeregten mechanischen Federschwingers, wenn dort die momentane Auslenkung u und die äußere Erregung x durch den Spulenstrom $i _ { L } = i _ { L 0 } \sin ( \omega t - \varphi )$ und den Erregerstrom $i = i _ { 0 }$ sinωt ersetzt werden. Man beobachtet also auch hier eine **Resonanzerscheinung**. Es gelten daher für Amplitudengang und Phasenverschiebung für den Parallelschwingkreis die gleichen Abhängigkeiten (33.31) und (33.32) von der Erregerfrequenz ω wie für die erzwungene Federschwingung, entsprechend den in Bild 33.8 dargestellten Verläufen mit $i _ { L 0 } / i _ { 0 }$ anstelle von $u _ { 0 } / x _ { 0 }$ für das Verhältnis von erregter Amplitude zu Erregeramplitude sowie für die Phasenverschiebung ϕ zwischen dem Spulenstrom $i _ { L }$ und dem Erregerstrom i:

$$
\frac {i _ {L 0}}{i _ {0}} = \frac {\omega_ {0} ^ {2}}{\sqrt {(\omega_ {0} ^ {2} - \omega^ {2}) ^ {2} + (2 \delta \omega) ^ {2}}} = \frac {1}{\sqrt {(1 - \omega^ {2} L C) ^ {2} + (\omega R C) ^ {2}}} \tag {34.4}
$$

$$
\tan \varphi = \frac {2 \delta \omega}{\omega_ {0} ^ {2} - \omega^ {2}} = \frac {\omega R C}{1 - \omega^ {2} L C} \quad \text {fur} 0 \leq \varphi \leq \pi . \tag {34.5}
$$

Der innerhalb des Schwingkreises fließende Strom $i _ { L 0 }$ wird im Resonanzfall sehr viel größer als der äußere Erregerstrom $i _ { 0 } ,$ was in der Praxis durchaus zum Durchbrennen der Spulenwicklung führen kann. Anders betrachtet ist der in den Schwingkreis eingespeiste Strom betragsmäßig viel kleiner als der im Kreis fließende Strom; man nennt daher den Parallelkreis auch Sperrkreis. Bei Resonanz gilt $i _ { L 0 } \gg i _ { 0 }$ und somit $| i _ { C } | = | i - i _ { L } | \approx | i _ { L } | \gg | i |$ , Spulenstrom $i _ { L }$ und Auf- und Entladestrom des Kondensators $i _ { C }$ kompensieren sich in diesem Fall. Für die Resonanzfrequenz gilt eine zu (33/33) analoge Beziehung:

$$
\omega_ {\mathrm{res}} = 2 \pi f _ {\mathrm{res}} = \sqrt {\omega_ {0} ^ {2} - 2 \delta^ {2}} = \sqrt {\frac {1}{L C} - \frac {R ^ {2}}{2 L ^ {2}}} \quad \text {(Resonanzkreisfrequenz des Parallelschwingkreises).} \tag {34.6}
$$

Für $R \rightarrow 0$ ergibt sich das Resonanzverhalten des ungedämpften Parallelschwingkreises aus Abschnitt 34.1. Es gelten hierfür die Beziehungen $i _ { L 0 } / i _ { 0 } = 1 / ( 1 - \omega ^ { 2 } L C ) , \varphi = 0   \mathrm { u n d }   \omega _ { \mathrm { r e s } } = \omega _ { 0 } = 1 / \sqrt { L C } .$

---

34.2 Strom- und Spannungsresonanz

377

**Reihenschwingkreis** (Bild 34.2b). Induktivität bzw. Kapazität nehmen abwechselnd während einer Viertelperiode des Stromflusses Energie aus der Spannungsquelle auf und geben ihre magnetische bzw. elektrische Feldenergie in der nächsten Viertelperiode zurück. Erfolgt aber die Erregung mit $\omega = \omega _ { 0 } = 1 / \sqrt { L C }$ (Eigenfrequenz des Schwingkreises), ist die Summe beider Energieformen konstant (vgl. 34.1), so dass die Zeiten der Energieaufnahme in der Induktivität mit denen der Energieabgabe in der Kapazität und umgekehrt zusammenfallen. Nach Durchlaufen des Einschwingvorganges braucht die Spannungsquelle nur noch die im Allgemeinen geringen Energieverluste an Schwingungsenergie im OHMschen Widerstand R laufend zu ersetzen. Außerhalb des Resonanzbereiches pendelt ein Teil der Schwingungsenergie zwischen Spannungsquelle und Schwingkreis hin und her.

Diskussion des Resonanzverhaltens. Der im gesamten Kreis einheitliche Strom i ruft an der Kapazität $C ,$ dem Widerstand R und der Induktivität L die Spannungsabfälle $u _ { L } = L ( { \bf d } i / { \bf d } t ) , \; u _ { R } = R i$ und $u _ { C } = ( 1 / C ) \int$ i dt hervor. Gemäß dem Maschensatz (25.18) addieren sich die drei Spannungsabfälle zur Erregerspannung $u = u _ { 0 }$ sinωt:

$$
u _ {L} + u _ {R} + u _ {C} = L \frac {\mathrm{d} i}{\mathrm{d} t} + R i + \frac {1}{C} \int i \mathrm{d} t = u = u _ {0} \sin \omega t. \tag {34.7}
$$

Durch Differenziation nach der Zeit t und Einsetzen der Abkürzungen gemäß Tabelle 34.1 erhält man daraus die Differenzialgleichung in Normalform

$$
\frac {\mathrm{d} ^ {2} i}{\mathrm{d} t ^ {2}} + 2 \delta \frac {\mathrm{d} i}{\mathrm{d} t} + \omega_ {0} ^ {2} i = \frac {2 \delta \omega u _ {0}}{R} \cos \omega t. \tag {34.8}
$$

Ihre Lösung erfolgt analog zu (33.29) und liefert mit $\omega _ { 0 }$ und $\delta$ gemäß Tabelle 34.1:

$$
\frac {R i _ {0}}{u _ {0}} = \frac {2 \delta \omega}{\sqrt {(\omega_ {0} ^ {2} - \omega^ {2}) ^ {2} + (2 \delta \omega) ^ {2}}} = \frac {\omega R C}{\sqrt {(1 - \omega^ {2} L C) ^ {2} + (\omega R C) ^ {2}}} (= \cos \varphi) \tag {34.9}
$$

$$
\tan \varphi = \frac {\omega^ {2} - \omega_ {0} ^ {2}}{2 \delta \omega} = \frac {\omega^ {2} L C - 1}{\omega R C} \quad \text {fur} - \frac {\pi}{2} \leq \varphi \leq \frac {\pi}{2}. \tag {34.10}
$$

Bild 34.3 zeigt den Amplituden- und Phasengang der erzwungenen Schwingung. Im Gegensatz zum Parallelkreis hängt die Resonanzfrequenz hier nicht von der Dämpfung ab und ist gleich der Eigenfrequenz des ungedämpften Schwingkreises:

$$
\omega_ {\mathrm{res}} = 2 \pi f _ {\mathrm{res}} = \omega_ {0} = \frac {1}{\sqrt {L C}} \quad \begin{array}{l l} (\text {Resonanzkreisfrequenz} \\ \text {des Reihenschwingkreises}). \end{array} \tag {34.11}
$$

![](../../raw/pages_0353-0384/images/page_379_image_12.jpg)

Bild 34.3 Amplitudengang (links, in nicht normierter Darstellung) und Phasenverschiebung (rechts) des Reihenschwingkreises in Abhängigkeit von der Erregerfrequenz ω (in Pfeilrichtung nimmt die Dämpfung δ zu.)

---

378

34 Elektrische Schwingungen

Von besonderem Interesse ist hier das Verhalten der am Kondensator anliegenden Spannung $u _ { C } ~ \mathbf { g e } \cdot$ genüber der äußeren Spannung $u .$ Ersetzt man in (34.7) den Strom i mittels $i = C ( \mathbf { d } u _ { C } / \mathbf { d } t )$ und $\mathbf { d } i / \mathbf { d } t =$ $\tilde { C } ( \mathbf { d } ^ { 2 } u _ { C } / \mathbf { d } t ^ { 2 } )$ durch die Spannung $u _ { C } ,$ so ergibt sich mit den Abkürzungen aus Tabelle 34.1

$$
\frac {\mathrm{d} ^ {2} u _ {C}}{\mathrm{d} t ^ {2}} + 2 \delta \frac {\mathrm{d} u _ {C}}{\mathrm{d} t} + \omega_ {0} ^ {2} u _ {C} = \omega_ {0} ^ {2} u = \omega_ {0} ^ {2} u _ {0} \sin \omega t. \tag {34.12}
$$

Die Kondensatorspannung $u _ { C }$ im Reihenkreis gehorcht somit derselben Gleichung (34.3) wie der Spulenstrom $i _ { L }$ im Parallelkreis. Folglich gelten beim Reihenschwingkreis für den Amplitudengang und die Phasenverschiebung von $u _ { C } = u _ { C 0 } \sin ( \omega t - \varphi )$ gegenüber der Erregerspannung $u = u _ { 0 }$ sinωt die gleichen Abhängigkeiten von der Erregerfrequenz ω wie diejenigen beim Parallelschwingkreis (34.4) bzw. (34.5) für $i _ { L }$ gegenüber i. Im Fall der **Resonanz** wächst die Spannung am Kondensator $u _ { C 0 }$ stark an (was zu Durchschlägen im Kondensator führen kann); es entsteht

## Spannungsresonanz:

**Im Reihenschwingkreis fallen an Induktivität und Kapazität hohe Spannungen ab, wenn die Erregerfrequenz mit der Resonanzfrequenz übereinstimmt.**

## Beispiel 34.2:

Man berechne die Resonanzbreite $\Delta \omega$ des Reihenschwingkreises als Differenz $\omega _ { 2 } - \omega _ { 1 } \equiv \Delta$ ω derjenigen Kreisfrequenzen $\omega _ { 1 }$ und $\omega _ { 2 }$ , bei denen die Amplitude in (34.9) auf den $( 1 / { \sqrt { 2 } } )$ fachen Wert vom Maximum abfällt!

Lösung: Aus (34.9) und (34.10) leitet man cos $\varphi = 1 / \sqrt { 1 + \tan ^ { 2 } \varphi } = 2 \delta \omega / \sqrt { ( \omega _ { 0 } ^ { 2 } - \omega ^ { 2 } ) ^ { 2 } + ( 2 \delta \omega ) ^ { 2 } }$ ab, so dass $\varphi _ { 1 , 2 } = \pm 4 5 ^ { \circ }$ bzw. tan $\varphi _ { 1 , 2 } = \pm 1$ folgt. Aus (34.10) erhält man $\omega _ { 0 } ^ { 2 } - \omega _ { 1 } ^ { 2 } = 2 \delta \omega _ { 1 }$ und $\omega _ { 2 } ^ { 2 }   -   \omega _ { 0 } ^ { 2 } = 2 \delta \dot { \omega _ { 2 } }$ , deren Addition $\omega _ { 2 } ^ { 2 }   -   \omega _ { 1 } ^ { 2 } = ( \omega _ { 2 }   -   \omega _ { 1 } ) ( \omega _ { 2 }   +   \omega _ { 1 } ) = 2 \delta ( \omega _ { 2 }   +   \omega _ { 1 } )$ , also $\Delta \omega = 2 \delta = R / L$ ergibt. Den Quotienten $Q = \omega _ { 0 } / \Delta \omega = ( 1 / R ) \sqrt { L / C }$ bezeichnet man auch als Resonanzschärfe oder Güte eines Schwingkreises. □

## Aufgabe

**34.1** Aus einer Spule mit der Induktivität $L = 2 { , } 5 \mathrm { H }$ und einem Kondensator soll ein Reihenschwingkreis (s. Bild 34.2b) aufgebaut werden. Der OHMsche Widerstand der Spule einschließlich Zuleitungen beträgt $R = 3 0 0   \Omega . \mathrm { a } )$ Wie groß muss die Kapazität C des Kondensators sein, wenn Resonanz zur angelegten Wechselspannung (10V/50Hz) angestrebt wird? b) Wie groß ist das logarithmische Dekrement? c) Welcher Strom fließt durch den Schwingkreis? d) Welche Spannung liegt am Kondensator an?

## 34.3 Erzeugung ungedämpfter elektrischer Schwingungen

Die Erzeugung von elektrischen Schwingungen mit gleich bleibender Amplitude ist von großer technischer Bedeutung. Um eine ungedämpfte Schwingung aufrechtzuerhalten, muss man dem Schwingkreis in jeder Periode genau so viel Energie von außen zuführen, wie ihm durch Verluste entzogen wird. Dazu ist eine Schaltung erforderlich, welche die „Energieportionen im Takt der Eigenfrequenz des Schwingkreises einspeist. Das kann mit einem Transistor geschehen (s. Bild 34.4a).

---

34.3 Erzeugung ungedämpfter elektrischer Schwingungen

379

**Fremderregung (Verstärkerprinzip).** Eine kleine Wechselspannung $u _ { 1 }$ an der Basis des Transistors führt zu periodischen Schwankungen des Kollektorstromes um seinen Mittelwert, d. h., dem Gleichstrom $I _ { \mathrm { C } }$ ist ein Wechselstrom i überlagert. Er bildet den Erregerwechselstrom für den Schwingkreis, der erzwungene Schwingungen in Stromresonanz ausführt (vgl. 34.2). Auch die Kollektorspannung erleidet infolge Spannungsabfall an Induktivität L und Kapazität C periodische Schwankungen um den Wert der Betriebsspannung $U _ { \mathrm { b } } ,$ d. h., der Kollektorgleichspannung $U _ { \mathrm { b } }$ ist eine Wechselspannung $u _ { 2 }$ überlagert. Das Verhältnis von Ausgangs- zu Eingangswechselspannung definiert die Spannungsverstärkung

$$
V = \frac {u _ {2}}{u _ {1}}. \tag {34.13}
$$

Die zur Verstärkung notwendige Energie wird der Betriebsspannungsquelle entzogen.

![](../../raw/pages_0353-0384/images/page_381_image_5.jpg)

Bild 34.4 a) Fremderregte Verstärkerschaltung, b) meissnersche Rückkopplungsschaltung mit Transistoren

Zur **Selbsterregung** eines Schwingkreises mit einer Verstärkerstufe ist es notwendig, den Gleichlauf von Erregung und Schwingung zu gewährleisten, also den Kollektorwechselstrom durch die Schwingungsfrequenz selbst zu steuern und die Energieeinspeisung in der richtigen Phasenlage vorzunehmen. Das gelang erstmals mit der MEISSNERschen Rückkopplungsschaltung durch eine Rückführungsschleife vom Ausgang auf den Eingang einer Verstärkerstufe (Bild 34.4b). Dabei sind Schwingkreisspule (L) und Basiskreis- oder Rückkopplungsspule $( L _ { \mathrm { R } } )$ induktiv wie Primär- und Sekundärwicklung eines Transformators gekoppelt. Dadurch wird die Schwingwechselspannung im Verhältnis der Windungszahlen unterteilt, so dass der Bruchteil von Primär- zu Sekundärspannung des „Transformators

$$
\ddot {u} = \frac {u _ {1}}{u _ {2}} \tag {34.14}
$$

als Steuerwechselspannung auf die Basis des Transistors gelangt. Der darauf einsetzende Kollektorwechselstrom i regt den Schwingkreis erneut und im weiteren Verlauf über die Rückführungsschleife periodisch an. Die richtige Phasenlage wird durch entsprechende Polung der Basiskreisspule erreicht.

Die Selbsterregung wird entweder durch den Einschaltvorgang oder durch kleine statistische Schwankungen des Kollektorstromes in Gang gebracht und der Schwingkreis zu Eigenschwingungen angestoßen. Die kleinen Anfangsamplituden schaukeln sich wie in Bild 33.7 durch fortwährende Verstärkung in einem Einschwingvorgang zum stationären eingeschwungenen Zustand auf. Beide Vorgänge lassen sich mit einem Oszillographen gut demonstrieren.

Zum Aufrechterhalten einer ungedämpften Schwingung genügt es, wenn das Produkt von (34.5) und (34.6) $V \ddot { u } = 1$ ist. Zum Einschwingen muss $V \ddot { u } > 1$ sein. Daraus folgt:

Eine große Zahl von Schwingschaltungen beruht auf dem Rückkopplungsprinzip: Ein Bruchteil der Ausgangsspannung (-energie) eines Verstärkers wird auf den Eingang zurückgeführt und reproduziert nach Verstärkung die ungedämpfte Schwingung.
