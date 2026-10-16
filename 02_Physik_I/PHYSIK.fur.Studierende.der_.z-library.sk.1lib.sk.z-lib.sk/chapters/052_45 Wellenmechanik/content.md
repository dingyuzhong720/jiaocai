# 45 Wellenmechanik

原始 PDF 第 554–561 页。

45

Wellenmechanik

## 45.1 Die Schrödinger-Gleichung

Die Theorie von DE BROGLIE (1924), wonach einem Teilchen jedweder Art mit dem Impuls $p =$ mv eine Materiewelle der Wellenlänge $\lambda = h / p$ zugeordnet ist, ermöglichte nur die Beschreibung der Bewegung eines freien Mikroteilchens durch eine Welle. Über die örtliche und zeitliche Änderung der Amplitude der DE-BROGLIE-Wellen von freien Teilchen und insbesondere von Teilchen in Kraftfeldern, z. B. eines Elektrons im COULOMB-Feld des Atomkerns, macht diese Theorie keine Aussage. Die Weiterentwicklung der DE-BROGLIEschen Theorie in dieser Richtung gelang SCHRÖDINGER (1926) durch Aufstellung einer Wellengleichung, welche (bei Vorgabe bestimmter Randbedingungen) automatisch auf die für die Quantenphysik typische Existenz diskreter Energiezustände gebundener Teilchen führt. Diese Wellengleichung, die eine Grundlage der **Quantenmechanik** bildet, lautet

$$
- \frac {\hbar^ {2}}{2 m} \triangle \psi + (V - E) \psi = 0 \quad (\text {stationäre SCHRÖDINGER - Gleichung}) \tag {45.1}
$$

mit m als Masse, $E$ als Gesamtenergie, V als potenzieller Energie des Teilchens und $\hbar = h / ( 2 \pi )$ Als solches wollen wir im Folgenden ein Elektron betrachten. Gleichung (45.1) beschreibt dann die Ortsabhängigkeit der **Wellenfunktion des Elektrons** $\psi ( x , y , z )$ , über deren physikalische Natur sie allerdings keine Aussage macht. $\triangle$ ist der LAPLACE-Operator; in einem räumlichen kartesischen Koordinatensystem hat dieser die Form $\triangle \equiv \partial ^ { 2 } / \partial x ^ { 2 } + \partial ^ { 2 } / \partial y ^ { 2 } + \partial ^ { 2 } / \partial z ^ { 2 }$

**Herleitung.** Ausgangspunkt sind die PLANCK-EINSTEIN-Beziehung (43.1) $E = h f = \hbar \omega$ und die DE-BROGLIE-Beziehung (43.20) $p = h / \lambda = \hbar k ,$ die jedem freien Mikroteilchen mit der Energie E und dem Impuls $p$ eine harmonische Materiewelle (vgl. Gleichung (36.25))

$$
\Psi = \Psi_ {0} \mathrm{e} ^ {- \mathrm{j} (\omega t - k x)} \tag {45.2}
$$

mit der Kreisfrequenz $\omega = 2 \pi f$ und der Wellenzahl $k = 2 \pi / \lambda$ zuordnet. Zur mathematischen Darstellung der Materiewelle wird hier die komplexe Form (45.2) verwendet, aus der sich der bisher bekannte Ausdruck (36.2) für die harmonische Welle mit Hilfe der EULERschen Formel (31.5) gewinnen lässt. Da zwischen Energie $E = E _ { \mathbf { k } } = m \nu ^ { 2 } / 2$ und Impuls $p = m v$ eines freien (nichtrelativistischen) Teilchens der Masse m nach (7.15) der Zusammenhang $E = p ^ { 2 } / ( 2 m )$ besteht, muss zwischen Kreisfrequenz und Wellenzahl der zugehörigen Materiewelle die Beziehung

$$
\omega = \frac {\hbar}{2 m} k ^ {2} \quad (\text {Dispersionsrelation für Materiewellen}) \tag {45.3}
$$

gelten, wie sich durch Einsetzen der Gleichungen ineinander leicht zeigen lässt. Die Dispersionsrelation $( 4 5 . 3 ) \; \omega = \omega ( k )$ ist eine quadratische Funktion von k und unterscheidet sich damit deutlich von derjenigen $\omega = c k$ für elektromagnetische Wellen im Vakuum (s. 39.2). Dies hat zur Folge, dass die Phasengeschwindigkeit (39.2) der Materiewelle $c = \omega / k = \pi \hbar / ( m \lambda )$ von ihrer Wellenlänge abhängt. Materiewellen zeigen also im Vakuum Dispersion, d. h., freie Materiewellengruppen oder Wellenpakete sind räumlich nicht stabil, sondern zerfließen im Laufe der Zeit. Als Gruppengeschwindigkeit (39.3) einer Materiewellengruppe, $c _ { \mathrm { g } } = \mathbf { d } \omega / \mathbf { d } k ,$ , erweist sich nach (45.3) die Teilchengeschwindigkeit:

---

552

45 Wellenmechanik

$c _ { \mathrm { g } } = \hbar k / m = p / m = \nu$ . Materiewellen genügen auf Grund der Dispersionsbeziehung (45.3) einer anderen Wellengleichung, als sie zum Beispiel für elektromagnetische Wellen im Vakuum gilt. Zur Ermittlung der Wellengleichung werden die partiellen Ableitungen der Wellenfunktion (45.2) gebildet:

$$
\frac {\partial \Psi}{\partial t} = - \mathrm{j} \omega \Psi_ {0} \mathrm{e} ^ {- \mathrm{j} (\omega t - k x)} = - \mathrm{j} \omega \Psi , \tag {45.4a}
$$

$$
\frac {\partial \Psi}{\partial x} = \mathrm{j} k \Psi_ {0} \mathrm{e} ^ {- \mathrm{j} (\omega t - k x)} = \mathrm{j} k \Psi , \quad \frac {\partial^ {2} \Psi}{\partial x ^ {2}} = \mathrm{j} k \frac {\partial \Psi}{\partial x} = - k ^ {2} \Psi . \tag {45.4b,c}
$$

Stellt man (45.4a) nach $\omega$ und $(45.4c)$ nach $k ^ { 2 }$ um und setzt die erhaltenen Ausdrücke in die Dispersionsrelation (45.3) für ω und $k ^ { 2 }$ ein, erhält man die eindimensionale Wellengleichung

$$
- \frac {\hbar^ {2}}{2 m} \frac {\partial^ {2} \Psi}{\partial x ^ {2}} = \mathrm{j} \hbar \frac {\partial \Psi}{\partial t}. \tag {45.5}
$$

Im Unterschied zur Wellengleichung vom Typ (36.7), zu dem auch die Wellengleichungen (38.7) und (38.8) für elektromagnetische Felder gehören, enthält (45.5) neben der imaginären Einheit j nur die erste Zeitableitung der Wellenfunktion.

Die dreidimensionale Bewegung eines Teilchens mit den Impulskomponenten $p _ { x } ,   p _ { y } ,   p _ { z }$ in einem Kraftfeld mit der potenziellen Energie $V = V ( x , y , z ; t )$ hat die Energie $E = E _ { \mathbf { k } } + E _ { \mathbf { p } } = p ^ { 2 } / ( 2 m ) + V = ( p _ { x } ^ { 2 } +$ $p _ { y } ^ { 2 }   +   p _ { z } ^ { 2 } ) / ( 2 m )   +   \stackrel { \circ } { V }$ . Mit der entsprechenden Erweiterung der DE-BROGLIE-Beziehung (43.20) für dreidimensionale Materiewellen $\pmb { p } = \hbar \pmb { k } ,$ wobei k der Wellenzahlvektor mit den Komponenten $k _ { x } ,   k _ { y } ,   k _ { z }$ ist (vgl. 36.5), folgt daraus der wellenmechanische Energieausdruck $E = \hbar \omega = \hbar ^ { 2 } ( \tilde { k _ { x } ^ { 2 } } + k _ { y } ^ { 2 } + k _ { z } ^ { 2 } ) / ( 2 m ) + V .$ Fordert man nun, dass für jede einzelne Komponente von k eine Beziehung der Form (45.4c) zwischen $k _ { x } ^ { 2 } , k _ { y } ^ { 2 } , k _ { z } ^ { 2 }$ und der jeweiligen zweiten Ableitung von $\Psi$ nach x, y bzw. z besteht, so geht dieser Energieausdruck mit (45.4a) und (45.4c) in die dreidimensionale Wellengleichung

$$
- \frac {\hbar^ {2}}{2 m} \left(\frac {\partial^ {2} \Psi}{\partial x ^ {2}} + \frac {\partial^ {2} \Psi}{\partial y ^ {2}} + \frac {\partial^ {2} \Psi}{\partial z ^ {2}}\right) + V \Psi = \mathrm{j} \hbar \frac {\partial \Psi}{\partial t} \quad \begin{array}{l} (\text {zeitabhängige} \\ \text {SCHRÖDINGER - Gleichung}) \end{array} \tag {45.6}
$$

über. Hängt die potenzielle Energie V nicht von der Zeit ab, so ist die Energie E konstant. Die Wellenfunktion zeigt in diesem Fall wie in (45.2) die periodische Zeitabhängigkeit einer harmonischen Schwingung $\mathbf { e } ^ { - \mathrm { j } \omega t }$ mit der Kreisfrequenz $\omega = E / \hbar$ und einer nur vom Ort abhängigen Wellenfunktion $\psi = \psi ( x , y , z )$ als Faktor: $\Psi = \mathrm { e } ^ { - \mathrm { j } E t / \hbar \bar { \mathrm { ~ } } } \psi ( x , y , z )$ . Eingesetzt in (45.6) ergibt sich nach entsprechender Umformung die stationäre SCHRÖDINGER-Gleichung (45.1). Die Lösungen von (45.6) bzw. (45.1) sind im Allgemeinen keine ebenen Wellen der Form (45.2) mehr, sondern sog. Wellenpakete oder, wie im Falle gebundener Teilchen in einem stationären Potenzial, stehende Wellen (s. 45.2).

**Interpretation der Wellenfunktion.** Die Wellenfunktion $\psi$ spiegelt die Wellennatur des Elektrons wider; sie selbst kann nicht anschaulich interpretiert werden. Einen anschaulichen Sinn hat nur das Quadrat ihres Betrages $| \psi | ^ { 2 } = \psi \psi ^ { * }$ ; dabei ist $\psi ^ { * }$ die konjugiert komplexe Funktion. Genaue Untersuchungen ergaben, dass $| \psi | ^ { 2 }$ wie folgt statistisch zu deuten ist: Die Größe

$$
\mathrm{d} w = | \psi | ^ {2} \mathrm{d} \tau = | \psi | ^ {2} \mathrm{d} x \mathrm{d} y \mathrm{d} z \tag {45.7}
$$

gibt die Wahrscheinlichkeit dafür an, das Elektron im Volumenelement dτ um den Raumpunkt $x , y , z$ vorzufinden. Demzufolge ist $| \psi | ^ { 2 }$ die **Wahrscheinlichkeitsdichte** für den „Aufenthalt“des Elektrons an einem bestimmten Ort. Diese Eigenschaft der ψ-Funktion spiegelt die zweite, korpuskulare Seite im Verhalten der Mikroteilchen wider. Das Produkt von $| \psi | ^ { \tilde { 2 } }$ mit der Elektronenladung $e$ gibt die **Ladungsdichte** $\varrho$ am betreffenden Ort an: $\varrho ( x , y , z ) = e | \psi ( x , y , z ) | ^ { 2 }$ Das Elektron bildet demnach eine über den ganzen Raum mit unterschiedlicher Dichte verteilte Ladungswolke (richtiger: „Wahrscheinlichkeitswolke“). Aus (45.6) und der Wahrscheinlichkeitsdefinition folgt, dass ψ der Bedingung

$$
w = \int_ {(\tau)} | \psi | ^ {2} \mathrm{d} \tau = 1 \quad (\text {Normierungsbedingung für die} \psi \text {-Funktion}) \tag {45.8}
$$

---

45.2 Elektron im Kastenpotenzial

553

genügen muss, was bedeutet, dass sich das Elektron, entsprechend der Wahrscheinlichkeit 1, mit Sicherheit im betrachteten (Gesamt-)Volumen τ aufhält.

Die SCHRÖDINGER-Gleichung (45.1) beansprucht allgemeine Gültigkeit, d. h., dass auch die Gesetze der klassischen Mechanik in ihr enthalten sind, und zwar als Sonderfall, wenn die Abmessungen der in Frage kommenden Körper (Teilchen) ihre DE-BROGLIE-Wellenlängen wesentlich übersteigen, was mit dem Übergang zu makroskopischen Teilchen der Fall ist (vgl. 43.5). Deshalb kann die Grundgleichung der Quantenmechanik nur im Bereich der Mikrophy sik angewandt werden; hier spiegelt sie die objektive Realität richtig (oder, wie man zu sagen pflegt, adäquat) wider. In der Makrophysik ist ihre Anwendung i. Allg. bedeutungslos, weil sie Resultate liefert, die sich praktisch nicht von denen der klassischen Mechanik unterscheiden.

## 45.2 Elektron im Kastenpotenzial

Wir betrachten ein Elektron, das gezwungen ist, sich in einem winzigen „Kasten“ der linearen Ausdehnung l zu bewegen, wie er durch den Verlauf der potenziellen Energie V (x) gemäß Bild 45.1a gegeben ist. Als ein solcher Potenzialkasten oder Potenzialtopf kann z. B. ein Metallstück angesehen werden, das die Leitungselektronen in einem bestimmten Raumbereich ein schließt, den sie nicht ohne Weiteres verlassen können (vgl. 26.1). Um gänzlich zu verhindern, dass das Elektron aus dem Kasten entweicht, nehmen wir an, dass zwischen den Wänden, also im Gebiet $0 \leq x \leq l ,$ die potenzielle Energie $V = 0$ ist und an den Wänden bei $x = 0$ und $x = l$ sowie außerhalb des Kastens V gegen unendlich geht. Wir erhalten so eine rechteckige „Potenzialmulde“ mit unendlich hohen Wänden. Da damit die Wahrscheinlichkeit, das Elektron außerhalb des Kastens anzutreffen, null ist, muss die Elektronen-Wellenfunktion an den Wänden gegen null gehen, d. h. $\psi ( x ) = 0$ für $x = 0$ und x = l. Für das Gebiet zwischen den Wänden lautet die SCHRÖDINGER-Gleichung (45.1) mit $\hbar = h / ( 2 \pi )$

$$
\frac {\mathrm{d} ^ {2} \psi}{\mathrm{d} x ^ {2}} + \frac {8 \pi^ {2} m _ {\mathrm{e}}}{h ^ {2}} E \psi = 0. \tag {45.9}
$$

![](../../raw/pages_0545-0576/images/page_555_image_7.jpg)

Bild 45.1 Verlauf der potenziellen Energie V des Elektrons a) entsprechend einem eindimensionalen „Potenzialkasten“, b) im Wasserstoffatom. $E _ { 1 }$ niedrigstes Energieniveau

Sie kann durch den Ansatz

$$
\psi (x) = \psi_ {0} \sin k x \quad (k = 2 \pi / \lambda \quad \text {Wellenzahl}) \tag {45.10}
$$

befriedigt werden; denn durch Differenzieren und Einsetzen erhält man für die Gesamtenergie $E = h ^ { 2 } k ^ { 2 } / ( 8 \pi ^ { 2 } m _ { \mathrm { e } } )$ , woraus mit der DE-BROGLIE-Beziehung $h / \lambda = h k / ( 2 \pi ) = m _ { \mathrm { e } } \nu$ folgt $E = m _ { \mathrm { e } } \nu ^ { 2 } / 2 = E _ { \mathrm { k } }$ . Nun sind aber durch den Lösungsansatz (45.9) gleichzeitig auch die oben

---

554

45 Wellenmechanik

genannten Randbedingungen $\psi ( 0 ) = 0$ und $\psi ( l ) = 0$ zu erfüllen. So ergibt die zweite Randbedingung $\psi _ { 0 }$ sin $kl = 0, \mathrm{d.h.} kl = n\pi$ , woraus für die Wellenzahl k folgende diskrete **Eigenwerte** folgen:

$$
k _ {n} = n \frac {\pi}{l} \quad \text {mit} \quad n = 1, 2, 3, \dots \tag {45.11}
$$

Für die Energie (s. o.) ergibt sich damit eine Reihe diskreter **Energieeigenwerte**

$$
E _ {n} = \frac {h ^ {2}}{8 \pi^ {2} m _ {\mathrm{e}}} k _ {n} ^ {2} = \frac {h ^ {2}}{8 m _ {\mathrm{e}} l ^ {2}} n ^ {2}. \tag {45.12}
$$

Das bedeutet, dass ein Teilchen, welches in einem Potenzialkasten „eingeschlossen“ ist, nur die Quantenwerte der Energie (45.11) annehmen kann. Durch Einführung von (45.10) in (45.9) werden die sog. **Eigenfunktionen** $\psi _ { n } ( x ) = \psi _ { 0 } \sin ( n \pi x / l )$ bestimmt, deren Amplitude aus der Normierungsbedingung (45.7) folgt:

$$
\int_ {0} ^ {l} \psi_ {n} ^ {2} (x) \mathrm{d} x = \psi_ {0} ^ {2} \int_ {0} ^ {l} \sin^ {2} \frac {n \pi x}{l} \mathrm{d} x = \psi_ {0} ^ {2} \frac {l}{2} = 1; \quad \psi_ {0} = \sqrt {\frac {2}{l}}.
$$

Ganz analog den Eigenschwingungen einer Saite (vgl. 36.4) beschreiben die Eigenfunktionen $\psi _ { 1 } ,   \psi _ { 2 } ,   \psi _ { 3 } ,   . .$ . stehende Elektronenwellen, für die wegen (45.10) und $k = 2 \pi / \lambda$ gilt $\lambda / 2 = l ,$ $l / 2 , l / 3 , \ldots$ Die ersten drei Eigenfunktionen und ihre Quadrate sind in Bild 45.2 dargestellt. Die Kurven $\psi _ { n } ^ { 2 } ( x )$ veranschaulichen die Verteilung der Wahrscheinlichkeit, das Elektron an diesem oder jenem Ort x innerhalb des Kastens bei verschiedenen Energiewerten zu „finden“. Wie man erkennt, ist die Wahrscheinlichkeit, im energetisch niedrigsten Zustand (Grundzustand $n = 1 )$ das Teilchen in der Mitte des Kastens anzutreffen, am größten und für die Wände des Kastens null.

![](../../raw/pages_0545-0576/images/page_556_image_9.jpg)

Bild 45.2 Die den drei niedrigsten Energiezuständen zugeordneten stehenden Elektronenwellen $\psi _ { n }$ und die zugehörigen Wahrscheinlichkeitsdichten $\psi _ { n } ^ { 2 }$

Dieses Ergebnis unterscheidet sich wesentlich von dem bei einem makroskopischen Teilchen zu erwartenden. Ein solches Teilchen können wir offensichtlich mit der gleichen Wahrscheinlichkeit an jedem beliebigen Ort des Kastens antreffen, entsprechend einem Verlauf der Kurve für die Wahrscheinlichkeitsdichte parallel zur x-Achse. Es zeigt sich ferner, dass bei einer

---

45.3 Das wellenmechanische Bild des Atoms

555

Vergrößerung der Teilchenenergie (Anwachsen der Quantenzahl $n )$ die Maxima der Kurve $\psi _ { n } ^ { 2 }$ immer näher aneinander rücken, so dass für sehr große Werte n auch eine Verteilung erhalten wird, die einem makroskopischen Teilchen entspricht.

Die niedrigste Energie, die das Elektron überhaupt haben kann, ist nach (45.11) diejenige für $n = 1$ , also $E _ { 1 } = h ^ { 2 } / ( 8 m _ { \mathrm { e } } l ^ { 2 } )$ , die Nullpunktsenergie (vgl. 43.6, Beisp. 2). Das im Kasten befindliche Elektron muss mindestens diese Nullpunktsenergie aufweisen, da es Elektronenzustände mit niedrigerer Energie nicht gibt. Nach der klassischen Theorie würde das Elektron immer dann elektromagnetische Wellen abstrahlen, wenn es gegen die Wand „prallt“ (denn dort ist es beschleunigt), und dies so lange, bis die kinetische Energie null erreicht ist. Die Tatsache aber, dass ein „Herunterfallen“ in einen energetisch niedrigeren Zustand nicht möglich ist, erklärt, warum quantenmechanisch das Wasserstoffatom stabil im Energiezustand $E _ { 1 }$ (Grundzustand) verbleiben kann.

**Elektron im Coulomb-Potenzial des Wasserstoffkerns.** Die Gleichung (45.11) für die Energieniveaus des Elektrons im Kastenpotenzial unterscheidet sich wesentlich von der Gleichung (44.9) für die Energieniveaus des Wasserstoffatoms. Der Grund dafür ist der andersartige Verlauf des Potenzials im Feld des Wasserstoffkerns. Dieses bzw. die potenzielle Energie V ist hier eine Funktion des Abstandes des Elektrons vom Kern und wird – wie in Abschnitt 44.3 gezeigt wurde – durch

$$
V (r) = - \frac {e ^ {2}}{4 \pi \varepsilon_ {0} r} \tag {45.13}
$$

beschrieben. Den Verlauf dieses Potenzials zeigt Bild 45.1b. Um die genauen Werte für die Energieniveaus im H-Atom zu erhalten, muss man die SCHRÖDINGER-Gleichung (45.1) für das COULOMB-Potenzial (45.12) lösen; dies ist eine Aufgabe der höheren Mathematik. Die Rechnung führt (ohne jede Zusatzannahme, wie dies in der älteren Quantentheorie in Form der BOHRschen Postulate erforderlich war) zu den gleichen Energieniveaus für das H-Atom, wie sie durch Gleichung (44.9) beschrieben werden. Außer der Quantelung der Energie durch die Hauptquantenzahl n erhält man jedoch zusätzlich die richtige Quantelung des Bahndrehimpulses des Elektrons hinsichtlich seines Betrages und seiner Projektion auf die z-Richtung, ausgedrückt durch die Quantenzahlen l und $m _ { l }$ (<sup>s</sup>. 44.4 und 44.5).

## 45.3 Das wellenmechanische Bild des Atoms

Die Anwendung der Wellenmechanik auf die Elektronen im Atom führte zu einem prinzipiell neuen Atommodell, welches frei ist von den Mängeln, die dem auf der NEWTONschen Mechanik und der älteren (PLANCKschen) Quantentheorie basierenden BOHRschen Atommodell noch anhafteten. Die Interpretation der Wellenfunktion ψ bzw. ihres Betragsquadrates $| \psi | ^ { 2 }$ als Wahrscheinlichkeitsdichte für den „Aufenthalt“ des Elektrons an einer bestimmten Stelle innerhalb des Atoms bzw. für die Verteilung der Dichte der „Elektronenwolke“ (vgl. 45.1) bietet die Möglichkeit, sich eine gewisse Vorstellung vom Wellenmodell des Atoms zu machen. Denn die Gestalt der Elektronenwolke ist typisch für einen bestimmten Elektronenzustand, gekennzeichnet durch die Quantenzahlen $n ,$ l und $m _ { l }$ , und vermittelt ein anschauliches Bild davon, wo sich das Elektron im Atom bevorzugt aufhält und welche Gebiete es meidet.

In Bild 45.3 unten ist die Ladungsdichte $e | \psi | ^ { 2 }$ für drei verschiedene Zustände des H-Atoms veranschaulicht, und zwar in den beiden ersten Bildern für zwei Zustände mit n = 1 und $n = 2$ , de-

---

556

45 Wellenmechanik

nen der Bahndrehimpuls l = 0 zukommt (sog. s-Zustand). Zustände mit dem Bahndrehimpuls null kommen in der BOHRschen Theorie (im Gegensatz zur Erfahrung) nicht vor. Das dritte Bild veranschaulicht einen Zustand mit n = 2 und l = 1 (p-Zustand). In allen drei Fällen ist $m _ { l } = 0$ Dabei hat man sich die Bilder um die vertikal in der Zeichenebene liegende Symmetrieachse rotierend zu denken, d. h., die Elektronenwolke ist in allen stabilen, stationären Zuständen des Atoms rotationssymmetrisch zum Kern. Die drehimpulsfreien s-Zustände bilden sogar eine sphärisch-symmetrische Wolke; bei ihnen zeigt $| \psi | ^ { 2 }$ also in allen räumlichen Richtungen die gleiche räumliche Verteilung.

![](../../raw/pages_0545-0576/images/page_558_image_3.jpg)

Bild 45.3 Radiale Verteilung der Elektronendichte $e | \psi | ^ { 2 }$ (gestrichelte Kurven) und der Elektronen-Aufenthaltswahrscheinlichkeit $| \psi | ^ { 2 }$ dτ (ausgezogene Kurven) für drei verschiedene Zustände des H-Atoms. Darunter: Zugehörige Modellbilder der Elektronendichte (sog. Orbitale)

Das Atom wird so als ein System stehender räumlicher Wellen beschrieben, analog zu den Eigenschwingungen mechanischer Gebilde, wie Stäbe, Platten und anderer Körper, für die ebenfalls nur ganz bestimmte diskrete Werte der Frequenz, die Eigenfrequenzen, möglich sind. An stelle der Knotenpunkte eines schwingenden Stabes im eindimensionalen und der Knotenlinien einer schwingenden Membrane im zweidimensionalen Fall (CHLADNIsche Klangfiguren, vgl. 36.4) erscheinen im räumlichen Gebilde des Atoms Knotenflächen, für die $| \psi | ^ { 2 } = 0$ gilt, wo das Elektron also nicht anzutreffen ist.

In Bild 45.3 oben ist für die darunter abgebildeten Zustände des H-Atoms durch die gestrichelten Kurven die radiale Verteilung der Elektronendichte $e | \psi | ^ { 2 }$ in Einheiten $a _ { \mathrm { H } }$ , des Radius der innersten BOHRschen Bahn (44.8), dargestellt. Der 1s-Zustand entspricht dem Grundzustand. Man erkennt, dass die Wellenfunktion ψ des Elektrons in diesem Fall eine stehende Welle ist, die ihr Maximum im Zentrum des Atoms hat und die zum „Rande“ des Atoms hin abfällt. Die ausgezogenen Kurven beschreiben den Verlauf der Größe $4 \pi r ^ { 2 } | \psi | ^ { 2 } ;$ sie gibt nach (45.6) d $w = | \psi | ^ { 2 } 4 \pi \tilde { r ^ { 2 } }$ dr die Wahrscheinlichkeit dafür an, das Elektron in einer Kugelschicht der Fläche $4 \pi r ^ { 2 }$ und der Dicke dr anzutreffen. Die dick ausgezogenen Abszissenabschnitte geben die Lage der Maxima der Aufenthaltswahrscheinlichkeit an.

Wie man sieht, hält sich das Elektron mit überwiegender Wahrscheinlichkeit in einem Abstand vom Kern auf, der gleich dem Radius der zugehörigen BOHRschen Bahn (44.7) $r _ { n } = a _ { \mathrm { H } } n ^ { 2 }$ ist. Dies trifft besonders für den 1s- und 2p-Zustand zu, weniger gut hingegen für den 2s Zustand, dem in der SOMMERFELDschen Erweiterung des BOHRschen Atommodells (vgl. 44.4) keine kreisförmige, sondern eine elliptische Elektronenbahn zukommt.

**Orbitale.** Die dem Elektron durch das wellenmechanische Modell zugewiesenen Aufenthaltsräume im Atom nennt man Orbitale (Bild 45.3, jeweils unten). Sie übernehmen gewisserma-

---

45.4 Der Tunneleffekt

557

ßen die Rolle der Elektronenbahnen des BOHRschen Modells. Wie man aus dem Bild erkennt, sind die Orbitale 1s und 2s kugelsymmetrisch, während das Orbital im Zustand 2p eine hantelförmige Gestalt annimmt, d. h., dass sich das Elektron mit gleicher Wahrscheinlichkeit in der einen oder anderen Hälfte des Orbitals $2 \mathrm { p }$ befinden kann. Entsprechend den drei Achsenrichtungen des Koordinatensystems kann dieses Orbital drei verschiedene, energetisch gleichwertige räumliche Lagen einnehmen, bei denen die „Hantel“ in $x - , y -$ oder z-Richtung orientiert ist, entsprechend den Einzelzuständen $2 \mathbf { p } _ { x } , 2 \mathbf { p } _ { y } , 2 \mathbf { p } _ { z } ,$ deren Orbitalformen von großer Bedeutung für das Verständnis der Atombindung (vgl. 12.3) sind.

## 45.4 Der Tunneleffekt

Im weiter oben behandelten Beispiel eines Teilchens im Potenzialkasten (Bild 45.1a) kann das Teilchen nicht aus dem Kasten entweichen, da es als Welle an den steilen Innenwänden vollständig reflektiert wird, was zur Bildung einer stehenden Welle im Kasten führt (stationärer Zustand). Anders verhält es sich, wenn sich das Teilchen in einem Potenzialtopf bestimmter Höhe und von nicht zu großer Wanddicke bewegt. Die Topfwand soll der Einfachheit halber die in Bild 45.4a dargestellte Form eines rechteckigen Potenzialwalls der Höhe $V _ { 0 }$ und der Breite a haben. Im Gegensatz zur klassischen Physik, wonach ein Teilchen der Energie $E < V _ { 0 }$ niemals in der Lage wäre, über den Wall hinweg in den Raum außerhalb des Potenzialtopfes zu gelangen, führt die wellenmechanische Behandlung dieses Problems zu dem Ergebnis, dass es für das Teilchen auch jenseits des Potenzialwalls eine von null verschiedene Aufenthaltswahrscheinlichkeit gibt.

![](../../raw/pages_0545-0576/images/page_559_image_5.jpg)

<details>
<summary>text_image</summary>

V(x)
V₀
ΔE
E
a)
x
ψ(x)
b)
0
a
x
</details>

## Bild 45.4 Tunneleffekt:

a) Vom Teilchen der Energie E „durchtunnelter“ rechteckiger Potenzialwall der Höhe $V _ { 0 }$ und der Breite $^ { a , }$
b) exponentielles Abklingen der Wellenfunktion ψ(x) innerhalb des Potenzialwalls

Läuft ein Teilchen der Masse m mit der Energie E an der Stelle $x = 0$ gegen den Potenzialwall an, so klingt die Wellenfunktion (45.9) innerhalb des Potenzialwalls infolge Dämpfung wie eine aperiodische Schwingung exponentiell ab gemäß

$$
\psi (x) \sim \mathrm{e} ^ {- x q \sqrt {V _ {0} - E}} \quad \text {mit} \quad q = \sqrt {8 \pi^ {2} m / h ^ {2}}. \tag {45.14}
$$

Das Verhältnis der Amplitudenquadrate der Welle vor und hinter dem Potenzialwall ist der **Durchgangskoeffizient**

$$
D = \frac {| \psi (a) | ^ {2}}{| \psi (0) | ^ {2}} = \mathrm{e} ^ {- 2 a q \sqrt {V _ {0} - E}}. \tag {45.15}
$$

---

558

45 Wellenmechanik

Dieser gibt an, mit welcher Wahrscheinlichkeit ein auf den Wall auftreffendes Teilchen diesen durchdringt. Bei Anwendung klassischer Vorstellungen scheint es, als ob sich das Teilchen in der Höhe E einen „Tunnel“ durch den Potenzialwall bohrte. Die Durchlässigkeit solcher Potenzialschwellen wird daher als **Tunneleffekt** bezeichnet. Sie wird, wie man Gleichung (45.15) entnimmt, mit wachsender Tunnellänge a, Teilchenmasse m und Höhe des Potenzialberges über dem Tunnel $\Delta E = V _ { 0 } - E$ rasch unmessbar klein.

Eine Reihe physikalischer Vorgänge konnte erst auf der Grundlage des Tunneleffekts erklärt werden, so z. B. der α-Zerfall des Uran 238 als Folge der natürlichen Radioaktivität. Bei diesem Prozess muss ein α-Teilchen (Heliumkern mit zweifach positiver Elementarladung), das durch die Kernkräfte im Innern des Atomkerns gehalten wird, die durch die COULOMB-Abstoßung der übrigen 90 positiven Elementarladungen des Urankerns hervorgerufene Potenzialschwelle von innen nach außen „durchtunneln“ (vgl. 48.1).

![](../../raw/pages_0545-0576/images/page_560_image_4.jpg)

<details>
<summary>text_image</summary>

z
y
x
I
</details>

Bild 45.5 Prinzip des Raster-Tunnel-Mikroskops

Eine Anwendung des Tunneleffekts als Analysenmethode an Objekten im Nanometer-Bereich ist das **Raster-Tunnel-Mikroskop** (Bild 45.5). Mit Hilfe eines piezoelektrischen Stellelements wird eine Sonde aus Platin/Iridium oder Wolfram in z-Richtung auf 1 bis 2nm (!) an die Oberfläche einer elektrisch leitenden Probe herangeführt. Bei diesem Abstand „überlappt“ sich die Elektronenwolke des Atoms an der Sondenspitze mit der des Atoms an der gegenüberliegenden Probenoberfläche. Beim Anlegen einer geringen Spannung zwischen Sonde und Probe können die Elektronen den geringen Abstand zwischen den beiden Atomen, welcher für die Elektronen eine Potenzialbarriere darstellt, durchtunneln. Es entsteht ein „Tunnelstrom“, dessen Stärke empfindlich vom Abstand zwischen Sonde und Probe und damit vom Höhenrelief der abgetasteten Oberfläche abhängt. Indem die Sonde rasterartig in x- und y-Richtung über die Probenoberfläche mit subatomarer Rasterweite geführt wird, kann eine Abbildung der Probenoberfläche erzeugt werden, welche die atomare Struktur des Probenmaterials deutlich erkennen lässt.

## Beispiel 45.1:

Gesucht ist die radiale Verteilung I(r ) des Tunnelstromes von der Probenoberfläche zur Sondenspitze eines Raster-Tunnel-Mikroskops, wobei das Probenmaterial eine Elektronenaustrittsarbeit von $W _ { \mathrm { a } } = V _ { 0 } - E = 4   \mathrm { e V }$ (vgl. Bild 45.4a) und die Sondenspitze die Form eines Rotationsparaboloids $z = r ^ { 2 } / ( 2 R )$ mit $R = 100    nm$ hat (vgl. Bild 45.5)! Wie groß ist das laterale Auflösungsvermögen des Raster-Tunnel-Mikroskops?

Lösung: Mit $a = z$ und $\varkappa = \sqrt { 8 \pi ^ { 2 } m _ { \mathrm { e } } ( V _ { 0 }   -   E ) / h ^ { 2 } } = \sqrt { 8 \pi ^ { 2 } m _ { \mathrm { e } } W _ { \mathsf { a } } / h ^ { 2 } }$ ergibt sich für den Durchgangskoeffizienten $(45.15)\;D=\mathrm{e}^{-2\varkappa z}$ . Für die radiale Stromverteilung $I ( r ) = I _ { 0 } D$ erhält man daraus mit $z = r ^ { 2 } / ( 2 R )$ eine GAUSS-Verteilung $I ( r ) = C  { \mathrm { e } } ^ { - r ^ { 2 } / ( 2 \sigma ^ { 2 } ) }$ mit der Standardabweichung $\sigma = \sqrt { R / ( 2 \varkappa ) } ;$ ; das laterale Auflösungsvermögen beträgt $\sigma = 2 { , } 2 \mathrm { n m }$ □
