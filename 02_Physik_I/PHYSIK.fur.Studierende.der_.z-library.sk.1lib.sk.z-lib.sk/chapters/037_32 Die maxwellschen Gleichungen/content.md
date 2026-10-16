# 32 Die maxwellschen Gleichungen

原始 PDF 第 354–359 页。

32

Die maxwellschen Gleichungen

## 32.1 Wirbel des magnetischen Feldes. Verschiebungsstrom

Ein von Gleichstrom durchflossener Leiter werde zu einem bestimmten Zeitpunkt durch einen schmalen Luftspalt unterbrochen. Die Anordnung stellt dann einen Kondensator dar, dessen Flächen Ladungen unterschiedlichen Vorzeichens tragen (Bild 32.1). Die elektrischen Flusslinien des D-Feldes im Luftspalt entspringen in den positiven Ladungen auf der einen und enden in den negativen Ladungen auf der anderen Leiterendfläche. Der elektrische Fluss Ψ ist der Ladungsmenge $Q$ auf jeder der beiden Kondensatorflächen gleich (vgl. 23.6):

$$
Q = \Psi = \int \boldsymbol {D} \cdot \mathrm{d} \boldsymbol {A} \tag {32.1}
$$

![](../../raw/pages_0353-0384/images/page_353_image_5.jpg)

<details>
<summary>text_image</summary>

Diagram illustrating magnetic field lines and current direction in a magnetic field, showing parallel loops with labeled vectors H and j.
</details>

Bild 32.1 Zur Entstehung des Verschiebungsstromes

Während nun ein Gleichstrom nicht durch den Luftspalt im Leiter hindurchtritt, setzt sich dagegen ein Wechselstrom durch den Spalt hindurch fort. Sein periodischer Richtungswechsel der fließenden Ladungen bewirkt ein ständiges Auf- und Entladen der Kondensatorflächen, d. h., es fließt ständig ein periodischer Ladestrom auf eine Fläche zu und von der anderen weg. Die zeitliche Änderung der Ladung auf den Kondensatorflächen ist gleich dem im Leiter zuund abfließenden Strom $i ,$ der sich nach (25.1) und (25.5) aus (32.1) durch Differenziation nach der Zeit ergibt zu

$$
i = \int \boldsymbol {j} \cdot \mathrm{d} \boldsymbol {A} = \frac {\mathrm{d} Q}{\mathrm{d} t} = \frac {\mathrm{d} \Psi}{\mathrm{d} t} = \frac {\mathrm{d}}{\mathrm{d} t} \int \boldsymbol {D} \cdot \mathrm{d} \boldsymbol {A} = \int \dot {\boldsymbol {D}} \cdot \mathrm{d} \boldsymbol {A}. \tag {32.2}
$$

Man nennt die Änderungsgeschwindigkeit der Verschiebungsdichte $\dot { D }$ die Verschiebungsstromdichte und $\mathbf { d } \varPsi / \mathbf { d } t = \int { \dot { \pmb D } }   \cdot   \mathbf { d } { \pmb A }$ den **Verschiebungsstrom**. Nach (32.2) sind Leitungsstrom i und Verschiebungsstrom gleich. Demnach setzt sich die Leitungsstromdichte als Verschiebungsstromdichte im Luftspalt stetig fort:

$$
\boldsymbol {j} = \frac {\mathrm{d} \boldsymbol {D}}{\mathrm{d} t} = \dot {\boldsymbol {D}} \quad (\text {Leitungsstromdichte} = \text {Verschiebungsstromdichte}).
$$

Wir können uns dann die Lücke im Stromfluss in Bild 32.1 geschlossen denken, wenn wir im Bereich des Luftspaltes $j$ durch $\dot { D }$ ersetzen. Es gibt also in diesem Sinne nur geschlossene elektrische Ströme.

MAXWELL erkannte, dass ebenso wie der Leitungsstrom auch der Verschiebungsstrom in seiner Umgebung ein magnetisches Wirbelfeld erzeugt (Bild 32.2a). Im Durchflutungsgesetz (28.5)

---

352

32 Die maxwellschen Gleichungen

ist deshalb bei zeitlich veränderlichen elektrischen Feldern zur Leitungsstromdichte j die Verschiebungsstromdichte $\dot { D }$ zu addieren (sog. MAXWELLsche Ergänzung):

$$
\oint \boldsymbol {H} \cdot \mathrm{d} \boldsymbol {r} = \int (\boldsymbol {j} + \dot {\boldsymbol {D}}) \cdot \mathrm{d} \boldsymbol {A} \quad \text {(I. MAXWELLSche Gleichung).} \tag {32.3}
$$

Diese Gleichung gilt auch im Vakuum und in elektrisch nichtleitenden Stoffen (Dielektrika), wo es keinen Leitungsstrom gibt. In diesem Fall folgt wegen j = 0 aus (32.3)

$$
\oint \boldsymbol {H} \cdot \mathrm{d} \boldsymbol {r} = \frac {\mathrm{d}}{\mathrm{d} t} \int \boldsymbol {D} \cdot \mathrm{d} \boldsymbol {A} = \int \dot {\boldsymbol {D}} \cdot \mathrm{d} \boldsymbol {A}. \tag {32.4}
$$

Diese Gleichung bringt zusätzlich zum Durchflutungsgesetz die folgende wichtige physikalische Tatsache zum Ausdruck:

## Jedes zeitlich veränderliche elektrische Feld erzeugt ein magnetisches Wirbelfeld.

![](../../raw/pages_0353-0384/images/page_354_image_8.jpg)

Bild 32.2 a) Induktion eines magnetischen Wirbelfeldes H durch ein zeitlich veränderliches elektrisches Feld D (I. maxwellsche Gleichung); b) Induktion eines elektrischen Wirbelfeldes E durch ein zeitlich veränderliches magnetisches Feld B (II. maxwellsche Gleichung); c) Skineffekt

Ebenso wie für den Leitungsstrom gilt auch für den Verschiebungsstrom zur Festlegung des Richtungssinns des ihn umgebenden magnetischen Wirbels H die Rechte-Hand-Regel (vgl. 28.3). Anstelle der Richtung des Leitungsstromes ist dabei die Richtung der Änderung des elektrischen Feldes ∆D zu betrachten. Bild 32.2a veranschaulicht eine positive Änderung (Zunahme) des elektrischen Feldes (∆D und D sind in diesem Fall gleichgerichtet) und das zugehörige magnetische Wirbelfeld.

## 32.2 Wirbel des elektrischen Feldes. Wirbelströme. Skineffekt

Während ein elektrostatisches Feld wirbelfrei ist (vgl. 23.4), entsteht nach dem FARADAYschen Induktionsgesetz in einem ringförmigen Leiter als Folge der zeitlichen Änderung eines von ihm umspannten Magnetfeldes ein elektrisches Wirbelfeld $E _ { \mathrm { i n d } }$ . Dieses Wirbelfeld ist auch ohne Anwesenheit des Leiters vorhanden, der Leiter dient lediglich dem experimentellen Nachweis des entstehenden elektrischen Feldes (Bild 32.2b) bzw. der zugehörigen Induktionsspannung. Die Spannung kann nach (23.14) als Linienintegral der elektrischen Feldstärke

---

32.2 Wirbel des elektrischen Feldes. Wirbelströme. Skineffekt

353

entlang des Wirbels (geschlossener Umlauf) dargestellt werden, womit aus dem Induktionsgesetz (30.1) folgt:

$$
\oint \boldsymbol {E} _ {\mathrm{ind}} \cdot \mathrm{d} \boldsymbol {r} = u _ {\mathrm{ind}} = - \frac {\mathrm{d} \varPhi}{\mathrm{d} t}.
$$

Dabei gibt der magnetische Fluss (28.12) $\varPhi = \int \pmb { B } \cdot \mathrm { d } \pmb { A }$ die Gesamtheit der Flusslinien des $B \cdot$ Feldes durch die vom Integrationsweg eingeschlossene Fläche A an. Somit wird

$$
\oint \boldsymbol {E} \cdot \mathrm{d} \boldsymbol {r} = - \frac {\mathrm{d}}{\mathrm{d} t} \int \boldsymbol {B} \cdot \mathrm{d} \boldsymbol {A} = - \int \dot {\boldsymbol {B}} \cdot \mathrm{d} \boldsymbol {A} \quad (\text {II. MAXWELLSche Gleichung}). \tag {32.5}
$$

## Jedes zeitlich veränderliche Magnetfeld erzeugt ein elektrisches Wirbelfeld.

Gleichung (32.5) weist eine bemerkenswerte Analogie zur I. MAXWELLschen Gleichung in der Form (32.4) auf. Jedoch ergibt sich der Richtungssinn des elektrischen Wirbels E wegen der LENZschen Regel (negatives Vorzeichen) hier nach der Linke-Hand-Regel. In Bild 32.2b ist eine positive Änderung (Zunahme) des Magnetfeldes mit dem zugehörigen elektrischen Wirbelfeld dargestellt.

**Wirbelströme.** Findet der Induktionsvorgang in einem leitfähigen Medium statt, erzeugt das elektrische Wirbelfeld nach dem OHMschen Gesetz Wirbelströme mit der Stromdichteverteilung $\pmb { j } = \varkappa \pmb { E }$ (κ elektrische Leitfähigkeit). Sie entstehen in einem Metallkörper, wenn dieser von einem magnetischen Wechselfeld durchsetzt oder in einem inhomogenen Magnetfeld bewegt wird. Ein Teil der dabei aufgewandten elektromagnetischen oder mechanischen Energie wird verzehrt und irreversibel in Wärme umgewandelt (Wirbelstromverluste).

Um die Ausbildung von Wirbelströmen stark einzuschränken, baut man Eisenkerne von Transformatoren, Läufer von Elektromotoren u. a. nicht aus kompakten Metallkörpern, sondern setzt sie aus untereinander isolierten Blechen quer zur Wirbelstromrichtung zusammen. Spulenkerne für die Hochfrequenztechnik werden aus schlecht leitenden magnetischen Werkstoffen (z. B. als Pulverkerne) hergestellt. In der Praxis werden Wirbelströme auch zur Dämpfung oder Bremsung von Bewegungen genutzt, da diese nach der LENZschen Regel stets so gerichtet sind, dass sie die verursachende Bewegung hemmen (Wirbelstrombremse).

**Skineffekt.** In wechselstromführenden Leitern werden durch das um die Leiterachse zirkulare magnetische Wechselfeld bei höheren Frequenzen im Leiter selbst Wirbelströme hervorgerufen. Diese induzierten Ströme fließen an der Oberfläche in Richtung des Leiterstromes und im Innern des Leiters der Stromrichtung entgegen (Bild 32.2c). Durch Auslöschung innen und Verstärkung außen ergibt sich eine ungleichmäßige Stromverteilung über den Leiterquerschnitt derart, dass <u>der G</u>esamtstrom nur in einer dünnen Oberflächenschicht mit der Eindringtiefe $d \approx 1 / \sqrt { \pi \mu \varkappa f }$ fließt (Haut- oder Skineffekt) mit $\mu$ als magnetischer Permeabilität, $\varkappa$ elektrischer Leitfähigkeit und $f$ als Frequenz des Wechselstromes. Dadurch ist der wirksame Stromquerschnitt stark herabgesetzt, und der elektrische Widerstand des Leiters nimmt merklich zu. Um dieser störenden Erscheinung entgegenzuwirken, vergrößert man die Oberfläche des Leiters, indem man ihn aus zahlreichen, gegeneinander isolierten und verdrillten Drähten herstellt, die gleich oft innen und außen zu liegen kommen (Hochfrequenzlitze). Auch versilbert man häufig die Leiteroberflächen, da es nur auf deren Leitfähigkeit ankommt, oder man ersetzt den massiven Leiter durch ein dünnwandiges Rohr.

---

354

32 Die maxwellschen Gleichungen

## 32.3 Elektromagnetisches Feld. System der maxwellschen Gleichungen

Bei Berücksichtigung der zeitlichen Änderungen sowohl des elektrischen als auch des magnetischen Feldes sowie von vorhandenen Leitungsströmen wird die enge Kopplung der elektrischen und magnetischen Größen deutlich. Nach der I. und II. MAXWELLschen Gleichung (32.3) und (32.5) treten elektrische und magnetische Erscheinungen räumlich und zeitlich zusammen auf. Durch wechselseitige Erzeugung entsteht z. B. aus einem elektrischen ein magnetisches Wechselfeld und daraus wiederum ein elektrisches Wechselfeld usw., so dass wir von einem einheitlichen elektromagnetischen Feld sprechen. Das folgende vollständige System der Feldgleichungen, von denen jede in den vorangegangenen Abschnitten einzeln behandelt wurde, bildet das theoretische Fundament der **Elektrodynamik**:

$$
\oint \boldsymbol {D} \cdot \mathrm{d} \boldsymbol {A} = Q, \quad (2 3. 2 2) \quad \oint \boldsymbol {B} \cdot \mathrm{d} \boldsymbol {A} = 0; \tag {28.13}
$$

$$
\oint \boldsymbol {E} \cdot \mathrm{d} \boldsymbol {r} = - \int \dot {\boldsymbol {B}} \cdot \mathrm{d} \boldsymbol {A}, \quad (3 2. 5) \quad \oint \boldsymbol {H} \cdot \mathrm{d} \boldsymbol {r} = \int (\boldsymbol {j} + \dot {\boldsymbol {D}}) \cdot \mathrm{d} \boldsymbol {A}; \quad (3 2. 3)
$$

$$
\boldsymbol {D} = \varepsilon_ {0} \boldsymbol {E} + \boldsymbol {P}, \quad (2 4. 7) \quad \boldsymbol {B} = \mu_ {0} \boldsymbol {H} + \boldsymbol {J}. \tag {29.2}
$$

Diese Gleichungen beschreiben die wechselseitige Erzeugung der Felder D, E, B und H bei gegebener Ladungsverteilung $Q ,$ Stromdichte j, elektrischer Polarisation P und magnetischer Polarisation J.

Elektromagnetische Felder üben gemäß (23.2) und (28.22) auf Ladungsträger q die Kräfte

$$
\boldsymbol {F} = q (\boldsymbol {E} + \boldsymbol {v} \times \boldsymbol {B})
$$

aus, die nach den Gesetzen der Mechanik Verschiebungen bzw. Bewegungen der Ladungen hervorrufen. Damit kommt es jedoch im Allgemeinen zu einer Rückwirkung auf die Felder selbst. Diese Einflüsse werden durch die sog. Materialgleichungen $\pmb { P } = \pmb { P } ( \pmb { E } ) , \pmb { J } = \pmb { J } ( \pmb { H } )$ und $\pmb { j } = \pmb { j } ( \pmb { E } )$ beschrieben, die meist in der Form (24.6), (29.2) und (25.10)

$$
\boldsymbol {D} = \varepsilon \boldsymbol {E}, \quad \boldsymbol {B} = \mu \boldsymbol {H}, \quad \boldsymbol {j} = \varkappa \boldsymbol {E} \tag {32.6}
$$

erfasst werden.

Neben den obigen MAXWELLschen Gleichungen in Integralform gibt es noch eine weitere Darstellung in differenzieller Form:

$$
\operatorname{div} \boldsymbol {D} = \varrho , \quad \operatorname{div} \boldsymbol {B} = 0, \quad \operatorname{rot} \boldsymbol {E} = - \dot {\boldsymbol {B}}, \quad \operatorname{rot} \boldsymbol {H} = \boldsymbol {j} + \dot {\boldsymbol {D}}. \tag {32.7}
$$

Diese Gleichungen gewinnt man, indem die auftretenden Oberflächenintegrale in äquivalente Volumenintegrale durch den GAUSSschen Integralsatz sowie die Umlauf-Wegintegrale in Oberflächenintegrale mittels des STOKESschen Integralsatzes umgeformt werden. Die Vektorfelder H und E werden dabei durch ihre Wirbelstärken rot H bzw. rotE und die Vektorfelder D und B durch ihre Quellstärken divD bzw. divB repräsentiert. Sie beschreiben die Beziehungen zwischen den Vektoren punktuell.

Das allgemeine Gleichungssystem der Elektrodynamik enthält als Sonderfälle

1. mit $\dot { D } = 0$ und $\dot { \boldsymbol B } = 0$ die **Elektrostatik** und **Magnetostatik**. Dies führt zu einer Entkopplung der Gleichungen derart, dass elektrostatische und magnetostatische Felder vollkommen unabhängig voneinander existieren, wenn zum einen eine Ladungsverteilung Q, zum anderen eine magnetische Polarisation J oder eine Stromverteilung j vorliegt;
2. mit $j \neq 0,   \dot{B} = 0,   \dot{D} = 0$ die **Elektrodynamik stationärer Ströme**. Die Stromverteilung wird über das OHMsche Gesetz $\pmb { j } = \varkappa \pmb { E }$ aus der elektrischen Feldstärke bestimmt. Da magnetostatische Felder nicht auf die elektrischen Ströme zurückwirken, bilden sie lediglich deren Begleiterscheinung;

---

32.4 Relativistische Elektrodynamik

355

3. mit $\boldsymbol { j } \neq 0 ,   \dot { \boldsymbol { B } } \neq 0 ,   | \dot { \boldsymbol { D } } | \ll | \boldsymbol { j } | ( \dot { \boldsymbol { D } } \approx 0 )$ die **Elektrodynamik quasistationärer Ströme**. Solche nahezu stationären elektromagnetischen Erscheinungen ergeben sich, wenn ihre zwar hohe, aber endliche Ausbreitungsgeschwindigkeit für die Vorgänge in den Leitersystemen noch keine Rolle spielt. Die Vernachlässigung des Verschiebungsstromes gegenüber dem Leitungsstrom ist gerechtfertigt, weil dabei die Rückwirkung seines magnetischen Wirbelfeldes auf die elektrischen Vorgänge bis zu hohen Frequenzen gering bleibt;
4. mit $\dot { \boldsymbol { B } } \neq 0 ,   \dot { \boldsymbol { D } } \neq 0$ die **elektromagnetischen Wellen**. Die MAXWELLschen Gleichungen ergeben eine Wellengleichung, welche die Ausbreitung elektromagnetischer Felder in Form von Wellen mit konstanter Ausbreitungsgeschwindigkeit und endlicher Wellenlänge beschreibt (vgl. Kapitel 38). Da auch das Licht eine elektromagnetische Wellenerscheinung ist, folgt hieraus der Zusammenhang zwischen Elektrodynamik und Wellenoptik (s. Kapitel 41).

## 32.4 Relativistische Elektrodynamik

Elektrische und magnetische Kräfte sind nur verschiedene Erscheinungsformen ein und desselben Phänomens, der elektromagnetischen Wechselwirkung. Mit Hilfe der speziellen Relativitätstheorie (vgl. 6.1) lässt sich zeigen, dass ein rein elektrostatisches Feld in einem Bezugssystem Σ einem Beobachter, der sich relativ zu Σ geradlinig gleichförmig bewegt (Bezugssystem $\Sigma ^ { \prime } )$ , als Überlagerung eines elektrischen und eines magnetischen Feldes erscheint, welche von diesem auch experimentell festgestellt werden. Ebenso sieht ein Beobachter, der sich relativ zu einem rein magnetostatischen Feld bewegt, zusätzlich ein überlagertes elektrisches Feld.

Dass wir gewohnheitsmäßig (und aus pragmatischen Gründen auch berechtigt) elektrostatisches und magnetostatisches Feld unterscheiden, liegt daran, dass wir unser Laborsystem, in dem die vorhandenen Felder über Kraftwirkungen gemessen werden, als bevorzugt betrachten. In ihm stoßen sich zwei ruhende Ladungen q und Q gleichen Vorzeichens im Abstand r auf Grund des COULOMBschen Gesetzes (23.27) mit der Kraft $F _ { \mathrm { C } } = q Q / ( 4 \pi \varepsilon _ { 0 } r ^ { 2 } )$ ab. q befindet sich also im elektrischen Feld der Ladung Q mit der Feldstärke $E = Q / ( 4 \pi \varepsilon _ { 0 } r ^ { 2 } )$ bzw. umgekehrt (Bild 32.3a).

![](../../raw/pages_0353-0384/images/page_357_image_8.jpg)

Bild 32.3 Elektromagnetische Wechselwirkung a) im Laborsystem Σ, b) im mitbewegten Bezugssystem $\Sigma ^ { \prime }$

Bewegen sich q und Q im festen Abstand r mit der Geschwindigkeit v parallel nebeneinander her (Bild 32.3a), so stellen sie noch zusätzlich zwei Stromelemente dar, die je einen magnetischen Wirbel um die Bahnkurve erzeugen, dem die jeweils andere Ladung ausgesetzt ist. Ein Stromelement I dl (Länge dl, Querschnitt A) habe das Volumen d $V = A \mathbf { d } l .$ Nach (26.2) folgt mit der Raumladungsdichte $\varrho = \mathbf { d } Q / \mathbf { d } V ;   I \mathbf { d } l = j A \mathbf { d } l = j \mathbf { d } V = \varrho \nu \mathbf { d } V = \nu \mathbf { d } Q$ . Eine Ladung Q,

---

356

32 Die maxwellschen Gleichungen

die sich mit der Geschwindigkeit v bewegt, erzeugt nach dem BIOT-SAVARTschen Gesetz (28.9) im senkrechten Abstand r (d. h. $\varphi = 9 0 ^ { \circ } )$ die magnetische Feldstärke $H = Q \nu / ( 4 \pi r ^ { 2 } )$ bzw. die Induktion $B = \mu _ { 0 } H = \mu _ { 0 } Q \nu / ( 4 \pi r ^ { 2 } )$ Dort befindet sich die Ladung $q ,$ auf sie wirkt die $\mathrm { L o } \cdot$ RENTZ-Kraft (28.22) $F _ { \mathrm { L } } = q \nu B = \mu _ { 0 } q Q \nu ^ { 2 } / ( 4 \pi r ^ { 2 } )$ . Sie bewirkt, dass sich die beiden bewegten Ladungen gegenseitig anziehen. (Zwei gleich gerichtete Ströme ziehen sich an.) Da zwischen $Q$ und $q$ außerdem die COULOMBsche Abstoßungskraft wirkt, ergibt sich die Gesamtkraft, die elektromagnetische Wechselwirkungskraft, als Differenz

$$
F = F _ {\mathrm{C}} - F _ {\mathrm{L}} = \frac {q Q}{4 \pi \varepsilon_ {0} r ^ {2}} \left(1 - \varepsilon_ {0} \mu_ {0} \nu^ {2}\right) = \frac {q Q}{4 \pi \varepsilon_ {0} r ^ {2}} \left(1 - \frac {\nu^ {2}}{c ^ {2}}\right) \tag {32.8}
$$

mit der Lichtgeschwindigkeit im Vakuum (38.14) $c = 1 / \sqrt { \varepsilon _ { 0 } \mu _ { 0 } }$ . Für einen Beobachter, der sich zusammen mit den Ladungen $Q$ und $q$ bewegt (System $\Sigma ^ { \prime } )$ , ruhen die Ladungen, und die magnetische Wirkung von bewegten Ladungen tritt überhaupt nicht auf (Bild 32.3b).

Die magnetische Kraft ist eine unmittelbare Folge der relativistischen Zeitdilatation (s. Abschnitt 6.2). Danach erscheint ein im Bezugssystem $\Sigma ^ { \prime }$ ablaufendes Zeitintervall d $1 t ^ { \prime }$ einem Beobachter im System $\Sigma$ gedehnt auf $\mathbf { d } t = \mathbf { d } t ^ { \prime } / \sqrt { 1   -   ( \nu / c ) ^ { 2 } }$ . Für den A<u>bstand de</u>r Ladungen senkrecht zur Bewegungsrichtung gilt $r = r ^ { \prime }$ , womit d $\mathbf { l } r / \mathbf { d } t = ( \mathbf { d } r ^ { \prime } / \mathbf { d } t ^ { \prime } ) { \sqrt { 1 - ( \nu / c ) ^ { 2 } } }$ fo<sub>lgt</sub> und

$$
\frac {\mathrm{d} ^ {2} r}{\mathrm{d} t ^ {2}} = \frac {\mathrm{d} ^ {2} r ^ {\prime}}{\mathrm{d} t ^ {\prime 2}} \left(1 - \frac {v ^ {2}}{c ^ {2}}\right).
$$

Die Beschleunigung in $\Sigma$ ist also um den Faktor $[ 1 { - } ( \nu / c ) ^ { 2 } ]$ kleiner als in $\Sigma ^ { \prime }$ . Nach Multiplikation mit $m _ { 0 }$ kann man daraus direkt auf die wirkenden Kräfte (32.8) schließen.

Bei den bisherigen Überlegungen tritt das magnetische Feld als Sonderfall des elektrischen Feldes bewegter Ladungen auf. Jedoch kann auch das durch Gleichströme verursachte magnetostatische Feld um einen (elektrisch neutralen) Leiter herum, wie bekannt, allein auftreten. Denn im Laborsystem $\Sigma$ des Leiters ergeben die frei beweglichen Leitungselektronen mit der Ladungsdichte $\varrho _ { - }$ und die unbeweglichen (positiven) Gitterionen mit der Ladungsdichte $\varrho _ { + }$ zusammen die Ladungsdichte $\varrho = \varrho _ { + } + \varrho _ { - } = 0$ , d. h., vom Leiter geht kein makroskopisches elektrisches Feld aus.

Anders liegen die Verhältnisse, wenn sich der Beobachter relativ zum Leiter bewegt. Erfolgt die Bewegung mit der Driftgeschwindigkeit $\nu$ der Elektronen, so ruhen für ihn die Elektronen, während sich die Gitterionen mit v in entgegengesetzter Richtung bewegen. Infolge der relativistischen Längenkontraktion (6.12) und der damit verbundenen Volumen<u>verkleine</u>rung erhöht sich daher für die Gitterionen die Ladungsdichte von $\varrho _ { + }$ auf $\varrho _ { + } ^ { \prime } = \varrho _ { + } / \sqrt { 1 - ( \nu / c ) ^ { 2 } }$ . Für die Elektronen hingegen, die sich relativ zum Laborsystem $\Sigma$ des Leiters bewegen und dort daher bereits der Längenkontraktion unterliegen, wird diese beim Übergang auf das mitbewegte System $\Sigma ^ { \prime }$ , in dem sie ruhen, unwirksam, und die Ladungsdichte verringert sich von $\varrho _ { - }$ auf $\varrho _ { - } ^ { \prime } = \varrho _ { - } \sqrt { 1 - ( \nu / c ) ^ { 2 } }$ . Dem Beobachter in $\Sigma ^ { \prime }$ erschei<u>nt daher</u> der Leiter nicht mehr elektrisch neutral, sondern wegen $\varrho ^ { \prime } = \varrho _ { + } ^ { \prime } + \varrho _ { - } ^ { \prime } = \varrho _ { + } ( \nu / c ) ^ { 2 } / \sqrt { 1 - ( \nu / c ) ^ { 2 } } > 0$ (mit $\varrho _ { - } = - \varrho _ { + } ,   \mathrm { s . o . } )$ positiv geladen. Zusätzlich zum zirkularen Magnetfeld um den Leiter herum beobachtet er also noch ein vom Leiter ausgehendes, radial nach außen gerichtetes elektrisches Feld.
