handelt es sich demnach um die oft verwendete Emitterschaltung. Als Steuerspannungen mit dem Emitter als gemeinsame Bezugselektrode fungieren im Eingangskreis die Basis-Emitter-Spannung $U _ { \mathrm { B E } }$ und im Ausgangskreis die Kollektor-Emitter-Spannung $U _ { \mathrm { C E } }$ . Eine Änderung der Stromstärke im Eingangskreis um $\Delta I _ { \mathrm { B } }$ hat eine Stromstärkeänderung $\Delta I _ { \mathrm { C } }$ im Ausgangskreis zur Folge. Die entsprechende Abhängigkeit $I _ { \mathrm { C } } = f ( U _ { \mathrm { C E } } , I _ { \mathrm { B } } )$ beschreibt das in Bild 31.12b für $I _ { \mathrm { B } }$ als Parameter dargestellte **(Ausgangs-)Kennlinienfeld** des Transistors. Als Maß für die Verstärkung bestimmt man das Verhältnis der Stromänderung im Ausgangskreis zu der im Eingangs kreis

$$
\beta = \frac {\Delta I _ {\mathrm{C}}}{\Delta I _ {\mathrm{B}}} \quad \text {bei} \quad U _ {\mathrm{CE}} = \text {const} \quad (\text {Stromverstärkung des Transistors}). \tag {31.21}
$$

Bild 31.12c zeigt einen **einstufigen Transistorverstärker**. Der Arbeitspunkt A des Transistors wird durch den Basiswiderstand $R _ { \mathrm { B } }$ , den Arbeitswiderstand $R _ { \mathrm { C } }$ und die Betriebsspannung $U _ { \mathrm { b } }$ festgelegt. Die Anwendung des KIRCHHOFFschen Maschensatzes (25.18) auf den Ausgangskreis definiert die Arbeitsgerade $U _ { \mathrm { C E } }   +   R _ { \mathrm { C } } I _ { \mathrm { C } } = U _ { \mathrm { b } }$ (Bild 31.12b) mit dem Abszissenschnittpunkt $U _ { \mathrm { C E } } = U _ { \mathrm { b } } ~ ( I _ { \mathrm { C } } = 0$ gesetzt, Transistor gesperrt) und dem Ordinatenschnittpunkt $I _ { \mathrm { C } } = U _ { \mathrm { b } } / R _ { \mathrm { C } }$ $( U _ { \mathrm { C E } } = 0$ gesetzt, Transistor leitend). Alle zeitveränderlichen elektrischen Größen folgen in ihrem Verlauf genau der Arbeitsgeraden durch den Arbeitspunkt A. Die A bestimmende Basisstromstärke wird durch den Basiswiderstand eingestellt: $U _ { \mathrm { B E } } + R _ { \mathrm { B } } I _ { \mathrm { B } } = U _ { \mathrm { b } }$ . Aus dem Kennlinienfeld entnimmt man, dass schon eine geringe Änderung der Basisstromstärke $\Delta I _ { \mathrm { B } }$ , entsprechend einer kleinen Änderung der Eingangsspannung ∆U<sub>BE</sub>, eine große Änderung des Kollektorstromes $\Delta I _ { \mathrm { C } }$ und damit eine große Änderung der Ausgangsspannung $\Delta U _ { \mathrm { C E } } = U _ { \mathsf { b } } - R _ { \mathrm { C } } \Delta I _ { \mathrm { C } }$ bewirkt.

Der **Unipolartransistor** (Feldeffekttransistor, MOSFET) besteht aus einheitlichem Halbleitermaterial mit einer z. B. n-leitenden Verbindung von sehr geringem Kanalquerschnitt zwischen Source- und Drain-Elektrode, deren Leitfähigkeit durch ein äußeres elektrisches Feld verändert werden kann. Die isoliert aufgesetzte Gate-Elektrode saugt bei positiver Aufladung zusätzlich Elektronen in den Kanal und drängt bei negativer Aufladung Elektronen aus diesem heraus.

Ist die geforderte Verstärkung nicht mit einem einzigen Transistor zu erreichen, werden meh rere Stufen hintereinander geschaltet. Das Ausgangssignal der vorangehenden Stufe liefert das Eingangssignal für die folgende. Dabei kann die Kopplung zwischen beiden galvanisch (über eine leitende Verbindung), induktiv (z. B. über einen Transformator) oder kapazitiv (über Kondensatoren wie in Bild 31.12c) erfolgen. Über kapazitive und induktive Koppelglieder werden nur Wechselströme und Wechselspannungen übertragen.

Schaltungen mit diskreten Bauelementen, die auf Leiterplatten angeordnet sind, werden meist nur noch bei der Verarbeitung von Signalen größerer Leistung benutzt. Kommt es nur auf die Verarbeitung von Informationen an, haben sich die **integrierten Schaltkreise** $( C h i p s )$ durchgesetzt. Die gesamte Schaltung befindet sich in Form einer Mikrostruktur von Funktionselementen (Widerstände, Kapazitäten, pn-Übergänge, Transistoren, Sensoren u. a.) in oder auf einem Halbleiter-Einkristallplättchen. Ein unmittelbarer Zugriff auf die einzelnen Funktionselemente ist in der Mikroelektronik nicht mehr möglich.

## 32.1 Wirbel des magnetischen Feldes. Verschiebungsstrom

Ein von Gleichstrom durchflossener Leiter werde zu einem bestimmten Zeitpunkt durch einen schmalen Luftspalt unterbrochen. Die Anordnung stellt dann einen Kondensator dar, dessen Flächen Ladungen unterschiedlichen Vorzeichens tragen (Bild 32.1). Die elektrischen Flusslinien des D-Feldes im Luftspalt entspringen in den positiven Ladungen auf der einen und enden in den negativen Ladungen auf der anderen Leiterendfläche. Der elektrische Fluss Ψ ist der Ladungsmenge $Q$ auf jeder der beiden Kondensatorflächen gleich (vgl. 23.6):

$$
Q = \Psi = \int \boldsymbol {D} \cdot \mathrm{d} \boldsymbol {A} \tag {32.1}
$$

![](images/page_353_image_5.jpg)

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

![](images/page_354_image_8.jpg)

Bild 32.2 a) Induktion eines magnetischen Wirbelfeldes H durch ein zeitlich veränderliches elektrisches Feld D (I. maxwellsche Gleichung); b) Induktion eines elektrischen Wirbelfeldes E durch ein zeitlich veränderliches magnetisches Feld B (II. maxwellsche Gleichung); c) Skineffekt

Ebenso wie für den Leitungsstrom gilt auch für den Verschiebungsstrom zur Festlegung des Richtungssinns des ihn umgebenden magnetischen Wirbels H die Rechte-Hand-Regel (vgl. 28.3). Anstelle der Richtung des Leitungsstromes ist dabei die Richtung der Änderung des elektrischen Feldes ∆D zu betrachten. Bild 32.2a veranschaulicht eine positive Änderung (Zunahme) des elektrischen Feldes (∆D und D sind in diesem Fall gleichgerichtet) und das zugehörige magnetische Wirbelfeld.

## 32.2 Wirbel des elektrischen Feldes. Wirbelströme. Skineffekt

Während ein elektrostatisches Feld wirbelfrei ist (vgl. 23.4), entsteht nach dem FARADAYschen Induktionsgesetz in einem ringförmigen Leiter als Folge der zeitlichen Änderung eines von ihm umspannten Magnetfeldes ein elektrisches Wirbelfeld $E _ { \mathrm { i n d } }$ . Dieses Wirbelfeld ist auch ohne Anwesenheit des Leiters vorhanden, der Leiter dient lediglich dem experimentellen Nachweis des entstehenden elektrischen Feldes (Bild 32.2b) bzw. der zugehörigen Induktionsspannung. Die Spannung kann nach (23.14) als Linienintegral der elektrischen Feldstärke entlang des Wirbels (geschlossener Umlauf) dargestellt werden, womit aus dem Induktionsgesetz (30.1) folgt:

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

3. mit $\boldsymbol { j } \neq 0 ,   \dot { \boldsymbol { B } } \neq 0 ,   | \dot { \boldsymbol { D } } | \ll | \boldsymbol { j } | ( \dot { \boldsymbol { D } } \approx 0 )$ die **Elektrodynamik quasistationärer Ströme**. Solche nahezu stationären elektromagnetischen Erscheinungen ergeben sich, wenn ihre zwar hohe, aber endliche Ausbreitungsgeschwindigkeit für die Vorgänge in den Leitersystemen noch keine Rolle spielt. Die Vernachlässigung des Verschiebungsstromes gegenüber dem Leitungsstrom ist gerechtfertigt, weil dabei die Rückwirkung seines magnetischen Wirbelfeldes auf die elektrischen Vorgänge bis zu hohen Frequenzen gering bleibt;
4. mit $\dot { \boldsymbol { B } } \neq 0 ,   \dot { \boldsymbol { D } } \neq 0$ die **elektromagnetischen Wellen**. Die MAXWELLschen Gleichungen ergeben eine Wellengleichung, welche die Ausbreitung elektromagnetischer Felder in Form von Wellen mit konstanter Ausbreitungsgeschwindigkeit und endlicher Wellenlänge beschreibt (vgl. Kapitel 38). Da auch das Licht eine elektromagnetische Wellenerscheinung ist, folgt hieraus der Zusammenhang zwischen Elektrodynamik und Wellenoptik (s. Kapitel 41).

## 32.4 Relativistische Elektrodynamik

Elektrische und magnetische Kräfte sind nur verschiedene Erscheinungsformen ein und desselben Phänomens, der elektromagnetischen Wechselwirkung. Mit Hilfe der speziellen Relativitätstheorie (vgl. 6.1) lässt sich zeigen, dass ein rein elektrostatisches Feld in einem Bezugssystem Σ einem Beobachter, der sich relativ zu Σ geradlinig gleichförmig bewegt (Bezugssystem $\Sigma ^ { \prime } )$ , als Überlagerung eines elektrischen und eines magnetischen Feldes erscheint, welche von diesem auch experimentell festgestellt werden. Ebenso sieht ein Beobachter, der sich relativ zu einem rein magnetostatischen Feld bewegt, zusätzlich ein überlagertes elektrisches Feld.

Dass wir gewohnheitsmäßig (und aus pragmatischen Gründen auch berechtigt) elektrostatisches und magnetostatisches Feld unterscheiden, liegt daran, dass wir unser Laborsystem, in dem die vorhandenen Felder über Kraftwirkungen gemessen werden, als bevorzugt betrachten. In ihm stoßen sich zwei ruhende Ladungen q und Q gleichen Vorzeichens im Abstand r auf Grund des COULOMBschen Gesetzes (23.27) mit der Kraft $F _ { \mathrm { C } } = q Q / ( 4 \pi \varepsilon _ { 0 } r ^ { 2 } )$ ab. q befindet sich also im elektrischen Feld der Ladung Q mit der Feldstärke $E = Q / ( 4 \pi \varepsilon _ { 0 } r ^ { 2 } )$ bzw. umgekehrt (Bild 32.3a).

![](images/page_357_image_8.jpg)

Bild 32.3 Elektromagnetische Wechselwirkung a) im Laborsystem Σ, b) im mitbewegten Bezugssystem $\Sigma ^ { \prime }$

Bewegen sich q und Q im festen Abstand r mit der Geschwindigkeit v parallel nebeneinander her (Bild 32.3a), so stellen sie noch zusätzlich zwei Stromelemente dar, die je einen magnetischen Wirbel um die Bahnkurve erzeugen, dem die jeweils andere Ladung ausgesetzt ist. Ein Stromelement I dl (Länge dl, Querschnitt A) habe das Volumen d $V = A \mathbf { d } l .$ Nach (26.2) folgt mit der Raumladungsdichte $\varrho = \mathbf { d } Q / \mathbf { d } V ;   I \mathbf { d } l = j A \mathbf { d } l = j \mathbf { d } V = \varrho \nu \mathbf { d } V = \nu \mathbf { d } Q$ . Eine Ladung Q, die sich mit der Geschwindigkeit v bewegt, erzeugt nach dem BIOT-SAVARTschen Gesetz (28.9) im senkrechten Abstand r (d. h. $\varphi = 9 0 ^ { \circ } )$ die magnetische Feldstärke $H = Q \nu / ( 4 \pi r ^ { 2 } )$ bzw. die Induktion $B = \mu _ { 0 } H = \mu _ { 0 } Q \nu / ( 4 \pi r ^ { 2 } )$ Dort befindet sich die Ladung $q ,$ auf sie wirkt die $\mathrm { L o } \cdot$ RENTZ-Kraft (28.22) $F _ { \mathrm { L } } = q \nu B = \mu _ { 0 } q Q \nu ^ { 2 } / ( 4 \pi r ^ { 2 } )$ . Sie bewirkt, dass sich die beiden bewegten Ladungen gegenseitig anziehen. (Zwei gleich gerichtete Ströme ziehen sich an.) Da zwischen $Q$ und $q$ außerdem die COULOMBsche Abstoßungskraft wirkt, ergibt sich die Gesamtkraft, die elektromagnetische Wechselwirkungskraft, als Differenz

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

## Teil VI

# Wellen

# Mechanische und elektromagnetische Schwingungen und Wellen

Anhand vieler Experimente lässt sich zeigen, dass Systeme, deren stabiler Gleichgewichtszustand von außen gestört wurde, meist nicht einfach in ihre ursprüngliche Lage zurückkehren, sondern um diese hin- und herschwingen. Den schwingenden Körpern ist gemeinsam, dass sie zeitlich periodische Auslenkungen aus ihrer Gleichgewichtslage erfahren, als Folge eines Wechselspiels von Trägheits- und Rückstellkräften.

Schwingungen erweisen sich als Vorgänge, die periodisch eine Energieform in eine andere umund wieder zurückverwandeln. Bei mechanischen Schwingungen, z. B. die einer elastischen Feder mit einem daran befestigten Massekörper, wird fortwährend potenzielle Energie der Feder in kinetische Energie der Masse verwandelt und umgekehrt. Ähnliche Energieumwandlungen vollziehen sich auch bei den elektrischen Schwingungen, bei denen sich elektrische und magnetische Feldenergie periodisch ineinander umwandeln.

Aus der Vielfalt der möglichen Formen von Schwingungen hebt sich ein Schwingungstyp deutlich ab; er ist dadurch gekennzeichnet, dass er sich durch eine einfache Sinusfunktion beschreiben lässt (Sinusschwingung). Wie sich noch herausstellen wird, handelt es sich dabei um den physikalisch einfachsten Fall einer Schwingung; sie heißt **harmonische Schwingung**.

Eine freie Schwingung eines schwingungsfähigen Systems entsteht nach einem einmaligen äußeren Anstoß. Infolge unvermeidlich auftretender Energieverluste des Systems ist eine freie Schwingung auch stets eine gedämpfte Schwingung. Die freie ungedämpfte Schwingung ist ein Idealfall, der sich mathematisch besonders einfach behandeln lässt.

## 33.1 Lineare Federschwingungen

Ein linearer Federschwinger besteht im Modell aus einer Schraubenfeder und einem angehängten Massekörper (Bild 33.1). Diese beiden Elemente schaffen die Voraussetzung für das Zustandekommen einer Schwingung. Die von der Feder und dem Schwerefeld der Erde ausgeübten Kräfte halten sich in einer bestimmten Lage (Ruhelage) das Gleichgewicht. Bei einer Störung dieses Zustandes, z. B. einer Auslenkung u nach oben, wird die Feder zusätzlich gestaucht und übt auf die Masse eine rücktreibende Kraft F aus, welche die Auslenkung wieder rückgängig macht. Dabei wird die Masse beschleunigt und schwingt infolge ihrer Trägheit über die Ruhelage hinaus. Jetzt wird die Feder gedehnt und die Bewegung der Masse bis zum Stillstand verzögert. Dann läuft der Vorgang in umgekehrter Richtung ab usw.

![](images/page_360_image_5.jpg)

<details>
<summary>text_image</summary>

m
ω₀
ω₀t
φ
φ₀
u(t)
0
φ₀
- u₀
ω₀t
π
2π
Ruhe-
lage
</details>

Bild 33.1 Ein linearer Federschwinger beschreibt eine harmonische Schwingung.

Einfache Versuche zeigen, dass für nicht zu große Auslenkungen der Feder aus der Ruhelage die rücktreibende Federkraft F der Auslenkung u direkt proportional und ihr entgegengerichtet ist (s. auch Bild 4.5):

$$
F = - k u \quad (\text {Kraftgesetz der harmonischen Schwingung}). \tag {33.1}
$$

**Die rücktreibende Kraft ist bei einer elastischen Feder der Auslenkung aus der Ruhelage proportional.**

Der Proportionalitätsfaktor k heißt **Federkonstante** oder **Richtgröße**; seine Einheit ist $[ k ] =$ 1N/m.

Da die rücktreibende Kraft eine Beschleunigung $\mathbf { d } ^ { 2 } u / \mathbf { d } t ^ { 2 }$ des Massekörpers bewirkt, folgt mit der NEWTONschen Bewegungsgleichung (4.13) $F = m ( \mathbf { d } ^ { 2 } u / \mathbf { d } t ^ { 2 } )$ aus (33.1)

$$
m \frac {\mathrm{d} ^ {2} u}{\mathrm{d} t ^ {2}} + k u = 0 \quad \begin{array}{l} (\text {Bewegungsgleichung der} \\ \text {ungedämpften harmonischen Schwingung}). \end{array} \tag {33.2}
$$

Außer dem linearen Federschwinger führen auch andere Schwingungsvorgänge auf die gleiche Differenzialgleichung (33.2). Man abstrahiert deshalb vom speziellen Beispiel und nennt Systeme, die harmonische Schwingungen ausführen, **harmonische Oszillatoren**.

Die Bewegung des elastischen Federschwingers entspricht genau der Bewegung der Projektion eines mit konstanter Winkelgeschwindigkeit $\omega _ { 0 }$ auf einem Kreis vom Radius $u _ { 0 }$ umlaufenden Punktes (Bild 33.1). Die **Elongation** (momentane Auslenkung) u des Schwingers zum Zeitpunkt t ist gleich dem zum **Phasenwinkel** $\varphi = \omega _ { 0 } t + \varphi _ { 0 }$ gehörigen Ordinatenwert:

$$
u (t) = u _ {0} \sin (\omega_ {0} t + \varphi_ {0}) \quad \begin{array}{l} \text {(Weg - Zeit - Gesetz der} \\ \text {harmonischen Schwingung).} \end{array} \tag {33.3}
$$

Die Konstante $u _ { 0 }$ heißt **Amplitude** (auch Schwingungsweite, Scheitelwert oder Spitzenwert). Der Phasenwinkel $\varphi$ setzt sich im Allgemeinen aus zwei Teilen zusammen, aus der Anfangs**phase** (Phasenkonstante) $\varphi _ { 0 }$ , welche die Anfangslage des schwingenden Körpers zum Zeitpunkt $t = 0$ angibt, und dem Winkel $\omega _ { 0 } t ,$ den der mit der Winkelgeschwindigkeit $\omega _ { 0 }$ auf der Kreisbahn umlaufende Punkt in der Zeit t überstreicht. Lässt man den Beginn der Zeitzählung (Zeitpunkt $t = 0 )$ mit jenem Augenblick zusammenfallen, in dem der schwingende Körper gerade durch seine Ruhelage geht $( u = 0 )$ , so ist in diesem Fall $\varphi _ { 0 } = 0$ , und man erhält anstelle von (33.3) $u ( t ) = u _ { 0 } \sin \omega _ { 0 } t$

Die Winkelgeschwindigkeit $\omega _ { 0 }$ der Kreisbewegung, deren Projektion auf die u-Achse die harmonische Schwingung ergibt, heißt **Kreisfrequenz**. Während der Zeitdauer einer vollen Schwingung, der **Periodendauer** T , durchläuft der zugeordnete Punkt den Winkel $\varphi = 3 6 0 ^ { \circ } \equiv$ $2 \pi = \omega _ { 0 } T ,$ d. h., es ist $\omega _ { 0 } = 2 \pi / T$ . Ist N die Anzahl der Umläufe bzw. Schwingungen in der Zeit t, so ist $f _ { 0 } = N / t$ die Anzahl der Schwingungen je Zeiteinheit, die **Eigenfrequenz**. Mit der Periodendauer $T = t / N = 1 / f _ { 0 }$ folgt somit

$$
\omega_ {0} = 2 \pi f _ {0} = \frac {2 \pi}{T} \quad (\text {Eigenkreisfrequenz}). \tag {33.4}
$$

Einheit der Frequenz:

$\omega _ { 0 }$ bzw. $f _ { 0 }$ sind bei einem harmonischen Oszillator von der Schwingungsamplitude $u _ { 0 }$ unabhängig und haben einen für jeden speziellen harmonischen Oszillator charakteristischen konstanten Wert. Die Eigenfrequenz eines Oszillators gestattet unter anderem, den Zeitablauf durch Abzählen von Perioden zu bestimmen, und spielt in der Zeitmessung eine entscheidende Rolle (vgl. Definition der Sekunde in Abschnitt 3.1).

Die Schwingungsdifferenzialgleichung (33.2) wird, wie man sich leicht überzeugt, durch den Ansatz (33.3) gelöst, aber nur für einen ganz bestimmten Wert von $\omega _ { 0 }$ , den sog. Eigenwert. Bildet man nämlich die Ableitungen

$$
\frac {\mathrm{d} u}{\mathrm{d} t} = \omega_ {0} u _ {0} \cos (\omega_ {0} t + \varphi_ {0}), \tag {33.5a}
$$

$$
\frac {\mathrm{d} ^ {2} u}{\mathrm{d} t ^ {2}} = - \omega_ {0} ^ {2} u _ {0} \sin (\omega t + \varphi_ {0}) = - \omega_ {0} ^ {2} u \tag {33.5b}
$$

und setzt diese in (33.2) ein, so ergibt sich $- m \omega _ { 0 } ^ { 2 } u + k u = 0 ,$ d. h.

$$
\omega_ {0} = \sqrt {\frac {k}{m}} \quad (\text {Eigenkreisfrequenz des Federschwingers}), \tag {33.6}
$$

woraus mit (33.4) folgt

$$
f _ {0} = \frac {1}{2 \pi} \sqrt {\frac {k}{m}}; \quad T = \frac {1}{f _ {0}} = 2 \pi \sqrt {\frac {m}{k}} \quad \text {(Eigenfrequenz} f _ {0} \text {und Perioden- dauer} T \text {des Federschwingers).} \tag {33.7}
$$

u0 und $\varphi _ { 0 }$ sind die Integrationskonstanten im Weg-Zeit-Gesetz (33.3), die bei der Lösung der Differenzialgleichung (33.2) auftreten. Sie ergeben sich aus den sog. **Anfangsbedingungen** des Bewegungsablaufs. Meist wählt man den Zeitpunkt $t = 0$ als Beginn des Ablaufs und schreibt dafür eine bestimmte Auslenkung $u _ { 0 } = u ( 0 )$ und eine bestimmte Geschwindigkeit $\nu _ { 0 } = \dot { u } ( 0 )$ vor. Wird z. B. der Oszillator um die Strecke $u _ { \mathrm { m } }$ statisch ausgelenkt und zum Zeitpunkt t = 0 freigegeben, so muss nach (33.3) und (33.5a) gelten

$$
u (0) = u _ {\mathrm{m}} = u _ {0} \sin \varphi_ {0}; \quad \dot {u} (0) = 0 = \omega_ {0} u _ {0} \cos \varphi_ {0}.
$$

Daraus folgt $\varphi _ { 0 } = \pi / 2 ,   u _ { 0 } = u _ { \mathrm { m } }$ und damit als spezielles Weg-Zeit-Gesetz (33.3)

$$
u (t) = u _ {\mathrm{m}} \cos \omega_ {0} t.
$$

Erhält in einem anderen Fall der Oszillator in seiner Ruhelage zum Zeitpunkt $t = 0$ die Anfangsgeschwindigkeit $\nu _ { 0 } ,$ , so muss gelten

$$
u (0) = 0 = u _ {0} \sin \varphi_ {0}; \quad \dot {u} (0) = v _ {0} = \omega_ {0} u _ {0} \cos \varphi_ {0}.
$$

Daraus folgt $\varphi _ { 0 } = 0 ,   u _ { 0 } = \nu _ { 0 } / \omega _ { 0 }$ und damit aus (33.3)

$$
u (t) = \frac {v _ {0}}{\omega_ {0}} \sin \omega_ {0} t.
$$

## Beispiele 33.1:

1. Mit welcher Eigenfrequenz kann ein Pkw mit der Leermasse $m = 9 0 0$ kg auf Grund seiner Federung schwingen, wenn sich die Karosserie bei einer Belastung mit einer Masse $m _ { 1 } = 2 5 0   \mathrm { k g }$ um 35mm senkt?

Lösung: Wegen $m _ { 1 } g   +   F = 0$ (Gewichtskraft und Federkraft halten sich das Gleichgewicht) folgt aus (33.1) für die Ri<u>chtgröße d</u>er Federung $k = - F / u = m _ { 1 } g / u$ und damit aus (33.7) die Eigenfrequenz zu $f _ { 0 } = \sqrt { m _ { 1 } g / ( m u ) } / ( 2 \pi ) = 1 { , } 4   \mathrm { H z }$

2. Zu welchen Zeitpunkten $t \geq 0$ sind nach (33.3) Elongation u, Geschwindigkeit v und Beschleunigung a einer schwingenden Punktmasse am größten, und wie groß sind ihre Maximalwerte? $( u _ { 0 } = 1 \mathrm { m } ; \omega _ { 0 } = 2 \pi \mathrm { s } ^ { - 1 } ; \varphi _ { 0 } = 0 . )$ \_

Lösung: Aus (33.3) liest man unmittelbar ab, dass die Elongation immer dann am größten ist, wenn der Sinus seine Extremwerte ±1 annimmt; dies ist für $\omega _ { 0 } t = \pi / 2 , 3 \pi / 2 , 5 \pi / 2 , \dots , \mathbf { d } .   \mathbf { h }$ . zu den Zeitpunkten $t = 1 / 4 ,   3 / 4 ,   5 / 4 ,   \ldots$ Sekunden der Fall. Die Elongation beträgt dann ±u<sub>0</sub> = ±1m. Nach (33.5a) ergeben sich die Extremwerte von v für cos $\omega _ { 0 } t = \pm 1 , \mathbf { d } . \mathbf { h }$ . für $\omega _ { 0 } t = 0 , \pi ,$ $2 \pi , \ldots$ bzw. $t = 0 ,   1 / 2 ,   1 ,   3 / 2 ,   . .$ . Sekunden, also jedes Mal beim Hindurchschwingen durch die Ruhelage, zu $\nu _ { \mathrm { m } } = \pm \omega _ { 0 } u _ { 0 } = \pm 6 { , } 2 8 \mathrm { m / s }$ . Die Beschleunigung folgt nach (33.5b) im Zeitverlauf der Elongation; erreicht also ihre Extremwerte wie Letztere in den Umkehrpunkten der Schwingung. Ihr größter Wert ist $a _ { \mathrm { m } } = \pm \omega _ { 0 } ^ { 2 } u _ { 0 } = \pm ( 2 \pi ) ^ { 2 } \cdot 1 \mathrm { m / s } ^ { 2 } = \pm 3 9 . 4 \mathrm { m / s } ^ { 2 }$ □

## Aufgabe

**33.1** Man denke sich in der Erdkugel eine Bohrung von Pol zu Pol, in die man eine Masse m hineinfallen lässt. Welche Periodendauer T der sich einstellenden Schwingung der Masse zwischen den Polen würde man feststellen? Wie groß ist ihre Geschwindigkeit im Erdmittelpunkt? – Anleitung: Nach (22.12) ist wie in (33.1) die rücktreibende Kraft F der Auslenkung $u ( = r )$ proportional. Auf der Erdoberfläche ist $k R = m g$ (Erdradius $R = 6380    km$

## 33.2 Energiebilanz des harmonischen Oszillators

Bei allen ungedämpften schwingungsfähigen Systemen findet eine periodische reversible Umwandlung von potenzieller in kinetische Energie (und umgekehrt) statt. Quantitativ wird die Energiebilanz des linearen Federschwingers aus der Kräftebilanz (33.2)

$$
m \ddot {u} + k u = 0 \quad \left(\text {mit der Beschleunigung} \ddot {u} \equiv \frac {\mathrm{d} ^ {2} u}{\mathrm{d} t ^ {2}}\right)
$$

gewonnen. Nach der sog. Energiemethode multipliziert man diese Gleichung mit der Geschwindigkeit u˙ ≡ du/dt und erhält, wie man leicht überprüft,

$$
(m \ddot {u} + k u) \dot {u} = \frac {\mathrm{d}}{\mathrm{d} t} \left(\frac {m}{2} \dot {u} ^ {2} + \frac {k}{2} u ^ {2}\right) = 0.
$$

Da die zeitliche Ableitung des rechten Klammerausdrucks gleich null ist, ist dieser selbst eine konstante Größe (Erhaltungsgröße)

$$
\frac {m}{2} \dot {u} ^ {2} + \frac {k}{2} u ^ {2} = E = \text {const}, \tag {33.8}
$$

nämlich gleich der Gesamtenergie oder **Schwingungsenergie** des (abgeschlossenen) Systems. Der geschwindigkeitsabhängige Anteil m $\dot { u } ^ { 2 } / 2$ ist die kinetische Energie $E _ { \mathrm { k } }$ , der ortsabhängige Anteil $k u ^ { 2 } / 2$ nach (7.14) die potenzielle Energie $E _ { \mathrm { p } }$ . Damit formuliert Gleichung (33.8) den

## Energieerhaltungssatz: In jeder Schwingungsphase ist die Summe aus kinetischer und potenzieller Energie konstant und gleich der Gesamtenergie des Oszillators.

Nach den Gleichungen (33.3) und (33.5a) sowie mit (33.6) $\omega _ { 0 } = \sqrt { k / m }$ ergibt sich

$$
E _ {\mathrm{k}} = \frac {m}{2} \dot {u} ^ {2} = \frac {k}{2 \omega_ {0} ^ {2}} \dot {u} ^ {2} = \frac {k}{2} u _ {0} ^ {2} \cos^ {2} (\omega_ {0} t + \varphi_ {0}), \tag {33.9}
$$

$$
E _ {\mathrm{p}} = \frac {k}{2} u ^ {2} = \frac {k}{2} u _ {0} ^ {2} \sin^ {2} (\omega_ {0} t + \varphi_ {0}). \tag {33.10}
$$

Damit ist nach (33.8)

$$
E = \frac {k}{2} u _ {0} ^ {2} \left[ \cos^ {2} (\omega_ {0} t + \varphi_ {0}) + \sin^ {2} (\omega_ {0} t + \varphi_ {0}) \right] = \frac {k}{2} u _ {0} ^ {2} = \text {const.} \tag {33.11}
$$

Der konstante Wert der Gesamtenergie $E ,$ den der Energieerhaltungssatz fordert, ist also der Richtgröße k und dem Quadrat der Amplitude $u _ { 0 } ^ { 2 }$ proportional.

![](images/page_364_image_3.jpg)

Bild 33.2 Energiebilanz des harmonischen Oszillators a) in Abhängigkeit von der Zeit, b) anhand des Verlaufs der potenziellen Energie (W Arbeit zum Anstoß einer Schwingung)

In Bild 33.2a sind $E _ { \mathrm { k } } , E _ { \mathrm { p } }$ und E gemäß Gleichung (33.9), (33.10) und (33.11) grafisch dargestellt. Während die Schwingung mit der Eigenfrequenz $\omega _ { 0 }$ erfolgt, pulsieren kinetische und potenzielle Energie als quadratische Größen mit der doppelten Frequenz $2 \omega _ { 0 }$ um einen zeitlichen Mittelwert zwischen 0 und $E = E _ { \mathrm { k } }   +   E _ { \mathrm { p } }$ . Das ist ohne Weiteres verständlich, denn energetisch sind z. B. die beiden Umkehrpunkte der Schwingung oder die Nulldurchgänge in beiden Richtungen völlig gleichwertig, während sie bei Auslenkung u und Geschwindigkeit u˙ das umgekehrte Vorzeichen tragen. Die grafische Darstellung demonstriert den sog.

## Virialsatz:

**Die Gesamtenergie eines Oszillators entfällt im zeitlichen Mittel zu gleichen Teilen auf kinetische und potenzielle Energie.**

Stellt man die potenzielle Energie (33.10) in Abhängigkeit von der Auslenkung grafisch dar (Bild 33.2b), so lässt sich die Bewegung des harmonischen Oszillators auch als Bewegung eines Teilchens in einer **Potenzialmulde** begreifen. Natürlich braucht dann die Bindung an eine Ruhelage nicht notwendig auf elastischen Kräften zu beruhen. Es genügt als Voraussetzung für ein schwingungsfähiges System, dass eine Potenzialmulde und eine Trägheit vorhanden sind. Da jedes Teilchen in einer stabilen Gleichgewichtslage sich zugleich in einer Potenzialmulde befindet (vgl. Bilder 10.9 und 13.2), wird es bei kleinen Auslenkungen $( E _ { \mathrm { p } } \sim u ^ { 2 } )$ harmonische und bei großen Auslenkungen anharmonische Schwingungen ausführen können.

## 33.3 Drehschwingungen

Ein starrer Körper sei um eine raumfeste Achse mit dem Trägheitsmoment J drehbar gelagert und durch eine Spiralfeder mit der Halterung verbunden (Bild 33.3a). Wird der Körper aus seiner Ruhelage ausgelenkt, so übt die Spiralfeder auf den Körper ein rücktreibendes Drehmoment M aus, das dem Drehwinkel $\varphi$ proportional und seinem Drehsinn entgegengerichtet ist:

$$
M = - D \varphi \quad \begin{array}{l} (\text {Grundgesetz der ungedämpften} \\ \text {harmonischen Drehschwingung}). \end{array} \tag {33.12}
$$

![](images/page_365_image_2.jpg)

Bild 33.3 a) Drehschwinger (ϕ Drehwinkel); b) elastische Scherung eines schwingenden Zylinders

Wird der Körper anschließend sich selbst überlassen, so dreht er zurück und schwingt infolge seiner Trägheit über die Ruhelage hinaus. Da nach (11.8) mit (3.34) das Drehmoment $J \alpha =$ $J ( \mathbf { d } ^ { 2 } \varphi / \mathbf { d } t ^ { 2 } )$ ist (mit $\alpha = { \bf d } ^ { 2 } \varphi / { \bf d } t ^ { 2 }$ als Winkelbeschleunigung), ergibt sich aus Gleichung (33.12)

$$
J \frac {\mathrm{d} ^ {2} \varphi}{\mathrm{d} t ^ {2}} + D \varphi = 0 \quad \begin{array}{l} (\text {Bewegungsgleichung der} \\ \text {ungedämpften harmonischen Drehschwingung}). \end{array} \tag {33.13}
$$

D bezeichnet wieder die Federkonstante, hier speziell die **Winkelrichtgröße**. Dividiert man Gleichung (33.13) durch $J ,$ so erhält man deren Normalform (in der der Faktor vor der zweiten Ableitung eins ist):

$$
\frac {\mathrm{d} ^ {2} \varphi}{\mathrm{d} t ^ {2}} + \omega_ {0} ^ {2} \varphi = 0 \quad \text {mit}
$$

$$
\omega_ {0} = \frac {2 \pi}{T} = \sqrt {\frac {D}{J}} \quad \begin{array}{l} (\text {Eigenkreisfrequenz} \omega_ {0} \text {der} \\ \text {ungedämpften Drehschwingung}). \end{array} \tag {33.14}
$$

Drehschwingungen werden häufig benutzt, um unbekannte Trägheitsmomente J und Winkelrichtgrößen $D$ aus der Periodendauer experimentell zu bestimmen. Meist bedient man sich eines horizontalen Drehtisches, an dessen vertikaler Drehachse eine Spiralfeder angreift, oder eines vertikal ausgespannten Drahtes, der am unteren Ende mit einer Auflage- oder Anhängevorrichtung belastet ist und Torsionsschwingungen ausführen kann.

**Torsion eines elastischen Zylinders.** Ein Draht hat kreisförmigen Querschnitt und kann in lauter koaxiale, ineinander geschobene Hohlzylinder von differenziell dünner Wandstärke zerlegt werden (s. Bild 33.3b). Bei einer Verdrehung eines Stückes der Länge l um den Winkel $\varphi$ erleidet ein Hohlzylinder im Abstand $r$ von der Mittelachse eine Scherung um den Winkel $\gamma .$ Der Kreisbogen zwischen den Punkten $P _ { 1 }$ und $P _ { 2 }$ beträgt $\varphi r \approx \gamma l .$ Die an jedem der Hohlzylinder tangential angreifende Kraft dF erzeugt in der Querschnittsfläche d $A = 2 \pi r$ dr die Schubspannung

$$
\tau = \frac {\mathrm{d} F}{\mathrm{d} A} = G \gamma = G \frac {\varphi}{l} r,
$$

entsprechend dem Zusammenhang (13.12) zwischen Schubspannung τ und Scherung γ (G Schubmodul). τ steigt linear von der Mittelachse $r = 0$ nach außen an. Aus der am Hohlzylinder tangential angreifenden Kraft dF kann das wirkende Drehmoment berechnet werden:

$$
\mathrm{d} M = r \mathrm{d} F = G \frac {\varphi}{l} r ^ {2} \mathrm{d} A = 2 \pi G \frac {\varphi}{l} r ^ {3} \mathrm{d} r.
$$

Das gesamte auf die Querschnittsfläche A mit dem Drahtradius R ausgeübte Drehmoment ist

$$
M = \int_ {A} \mathrm{d} M = 2 \pi G \frac {\varphi}{l} \int_ {0} ^ {R} r ^ {3} \mathrm{d} r = \frac {\pi G R ^ {4}}{2 l} \varphi = D \varphi .
$$

Das rücktreibende Drehmoment auf einen angehängten Körper ist gleich $- D \varphi$ , die Winkelrichtgröße beträgt $D = \pi G R ^ { 4 } / ( 2 l )$

## Beispiel 33.2:

Die Periodendauer eines Drehschwingers vergrößere sich nach Befestigung einer Zusatzmasse mit bekanntem Trägheitsmoment $J_{1} = 10^{-3}  kg  \cdot  m ^{2}$ von $T _ { 0 } = 8 { , } 4 1 { \mathrm { s } }$ auf $T _ { 1 } = 1 1 , 1 8   \mathrm { s }$ . Man berechne das Trägheitsmoment J des ursprünglichen Schwingers und die Winkelrichtgröße $D$

Lösung: Es gilt nach (33.14) $T _ { 0 } = 2 \pi \sqrt { J / D }$ und $T _ { 1 } = 2 \pi \sqrt { ( J + J _ { 1 } ) / D }$ . Eliminiert man einmal $D$ und einmal J aus den Bestimmungsgleichungen, so ergibt sich:

$$
J = J _ {1} \frac {T _ {0} ^ {2}}{T _ {1} ^ {2} - T _ {0} ^ {2}} = 1, 3 0 \cdot 1 0 ^ {- 3} \mathrm{kg} \cdot \mathrm{m} ^ {2}; \quad D = \frac {4 \pi^ {2} J _ {1}}{T _ {1} ^ {2} - T _ {0} ^ {2}} = 7, 2 8 \cdot 1 0 ^ {- 4} \mathrm{N} \cdot \mathrm{m}.
$$

![](images/page_366_image_9.jpg)

## Aufgaben

**33.2** Ein starrer Körper ist in seinem Schwerpunkt an einem Draht aufgehängt. Ein äußeres Drehmoment von 35Nm verdreht den Körper um einen Winkel von $1 5 ^ { \circ }$ . Nach dem Loslassen führt dieser als Torsionspendel 90 Schwingungen je Minute aus. Man bestimme das Massenträgheitsmoment J des Körpers bezüglich seiner Drehachse!

**33.3** Ein Massekörper mit dem Trägheitsmoment $J = 2 , 5 \cdot 1 0 ^ { - 3 }   \mathrm { k g } \cdot \mathrm { m } ^ { 2 }$ wird an einem Stahldraht aufgehängt und in Torsionsschwingungen versetzt. Bestimme aus der gemessenen Periodendauer $T = 3 { , } 8 { \mathrm {   s } }$ den Schubmodul G des Stahles! Drahtlänge $l = 2 , 4 0   \mathrm { m }$ Drahtdurchmesser $2 R = 1 , 2   \mathrm { m m }$

## 33.4 Pendelschwingungen

Pendel schwingen im Schwerefeld der Erde. Das **mathematische Pendel** denkt man sich als Punktmasse $m ,$ die an einem masselosen Faden aufgehängt ist. Bei Experimenten versucht man, diesen Voraussetzungen möglichst nahe zu kommen. Das **physikalische** (oder auch physische) **Pendel** ist ein starrer Körper, der um eine feste Achse drehbar gelagert ist. Bild 33.4 zeigt die beiden Ausführungen. Da der Faden des mathematischen Pendels immer gespannt bleibt, kann man ihn als starr betrachten. Mit dieser Voraussetzung gelingt es, sowohl die Schwingungen des mathematischen als auch die des physikalischen Pendels einheitlich zu behandeln.

Das rücktreibende Drehmoment bei ausgelenktem Pendel beträgt nach (10.4)

$$
M = - m g s \sin \varphi
$$

und ist dem Drehsinn des Auslenkungswinkels $\varphi$ entgegengerichtet (Minuszeichen). Allgemein sind Pendelschwingungen mit großen Auslenkungen anharmonische Schwingungen. Beschränkt man sich jedoch auf kleine Auslenkungswinkel, so kann

$$
\sin \varphi \approx \varphi \quad \text {und somit} \quad M = - m g s \varphi \tag {33.15}
$$

gesetzt werden (Linearisierung, „Kleine-Winkel-Näherung“). Das Drehmoment – und auch die Bewegungsgleichung – hat damit die Form (33.12). Es gelten also alle Beziehungen für Drehschwingungen auch für Pendelschwingungen kleiner Ausschläge, wenn als Winkelrichtgröße $D = m g s$ gesetzt wird. Man erhält damit nach (33.14)

$$
T = 2 \pi \sqrt {\frac {J}{m g s}} \quad (\text {Periodendauer des physikalischen Pendels}). \tag {33.16}
$$

Die Größe des Trägheitsmoments J beträgt für das mathematische Pendel, bei dem der Schwerpunktabstand s mit der Pendellänge l identisch ist, nach (11.2) $J = m l ^ { 2 }$ . Aus (33.16) folgt damit

$$
T = 2 \pi \sqrt {\frac {l}{g}} \quad (\text {Periodendauer des mathematischen Pendels}). \tag {33.17}
$$

Die Periodendauer eines harmonischen Pendels ist von der Pendellänge, nicht aber von der Pendelmasse oder der Amplitude abhängig.

![](images/page_367_image_7.jpg)

Bild 33.4 Mathematisches (a) und physikalisches Pendel (b)

Für größere Auslenkungswinkel gilt die Näherung (33.15) sin $\varphi \approx \varphi$ und damit (33.16) bzw. (33.17) nicht mehr, es schwingt anharmonisch. Infolgedessen wird die Periodendauer $T$ von der Amplitude $\varphi _ { 0 }$ abhängig (s. Abschnitt 35.5). Es ist

$$
T (\varphi_ {0}) = 2 \pi \sqrt {\frac {l}{g}} \left(1 + \frac {1}{1 6} \varphi_ {0} ^ {2} + \frac {1 1}{3 0 7 2} \varphi_ {0} ^ {4} + \dots\right), \tag {33.18}
$$

wobei $\varphi _ { 0 }$ in Radiant (vgl. Abschnitt 3.7) einzusetzen ist. Für $\varphi _ { 0 } = 5 ^ { \circ } , 1 0 ^ { \circ } , 2 0 ^ { \circ }$ liegt $T$ etwa 0,05%, 0,19%, $0 , 7 7 \%$ über dem durch Gleichung (33.16) bzw. (33.17) gegebenen Wert.

Wie aus (33.16) und (33.17) hervorgeht, ist die Periodendauer eines physikalischen Pendels der eines mathematischen Pendels genau dann gleich, wenn

$$
l = \frac {J}{m s} \quad (\text {reduzierte Pendellänge}) \tag {33.19}
$$

ist. Trägt man beim physikalischen Pendel vom Drehpunkt aus auf einer Geraden durch den Schwerpunkt die Strecke der reduzierten Pendellänge (33.19) ab, wie in Bild 33.4b dargestellt, so erhält man den **Schwingungsmittelpunkt**.

## Die Periodendauer eines physikalischen Pendels bleibt unverändert, wenn man Drehpunkt und Schwingungsmittelpunkt vertauscht.

Das zeigt die folgende Rechnung: Mit dem Trägheitsmoment $J s$ um die parallele Achse durch den Schwerpunkt ist nach dem STEINERschen Satz (11.4) $J = J _ { S } + m s ^ { 2 }$ und damit die reduzierte Pendellänge (33.19) um den Drehpunkt

$$
l = \frac {J _ {S}}{m s} + s. \tag {33.20}
$$

Die reduzierte Pendellänge um den Schwingungsmittelpunkt ist

$$
l ^ {\prime} = \frac {J _ {S}}{m (l - s)} + (l - s).
$$

Nach Einsetzen von $( l - s ) = J _ { S } / ( m s )$ aus Gleichung (33.20) ergibt sich schließlich

$$
l ^ {\prime} = s + \frac {J _ {S}}{m s} = l.
$$

Beim **Reversionspendel** wird eine zwischen Drehpunkt und Schwingungsmittelpunkt bewegliche Zusatzmasse so lange verschoben, bis die Periodendauern bei Schwingungen um beide Drehpunkte gleich sind. Deren Abstand ist dann gleich der reduzierten Pendellänge (33.19). Das Reversionspendel erlaubt somit auf der Grundlage von (33.16) eine genauere Messung der Schwerebeschleunigung g als ein Fadenpendel.

## Beispiel 33.3:

Wie lang ist ein dünner Stab, der um seinen Endpunkt mit der Periodendauer $T = 2 s$ schwingt? Lösung: Nach (33.17) folgt für die reduzierte Pendellänge $l = g   T ^ { 2 } / ( 4 \pi ^ { 2 } ) = 0 , 9 9 4   \mathrm { m } \approx 1   \mathrm { m }$ . Ein mathematisches Pendel dieser Länge, dessen Halbschwingung also 1s dauert, heißt Sekundenpendel. Nach Beispiel 11.2/1 ist für die Stablänge L das Trägheitsmoment bezüglich einer Drehachse um das Stabende, d. h. im Schwerpunktabstand $s = L / 2$ , gleich $J = m L ^ { 2 } / 3$ . Nach (33.19) folgt damit $l = 2 L / 3$ bzw. $L = 3 l / 2 = 1 { , } 4 9 1 { \mathrm {   m } } \approx 1 { , } 5 0 { \mathrm {   m } }$ . Das heißt, die Schwingung um das Stabende hat die gleiche Periodendauer wie die um den Schwingungsmittelpunkt, welcher um 1/3 der Stablänge vom anderen Ende entfernt liegt. □

## 33.5 Freie gedämpfte Schwingungen

Da ein schwingungsfähiges System niemals vollständig abgeschlossen ist, wird ihm durch Kopplung zu angrenzenden Medien laufend Schwingungsenergie entzogen. Abstrahlung von Energie (z. B. als Schallwellen von einer schwingenden Saite) und Reibung führen dazu, dass die Schwingungsamplitude $u _ { 0 }$ mit der Zeit immer kleiner wird, bis die Schwingung schließlich ganz aufhört. Man spricht dann von einer **gedämpften Schwingung**.

Die Bewegungsgleichung für die freie gedämpfte Schwingung gewinnt man, wenn in der Bewegungsgleichung für die ungedämpfte Schwingung (33.2) noch eine **Reibungskraft** berücksichtigt wird. Reibungskräfte sind bei langsamer Bewegung in einem bremsenden Medium oft der Geschwindigkeit du/dt proportional und ihr stets entgegengerichtet, weil sie grundsätzlich jede Bewegung verzögern (vgl. STOKESsches Reibungsgesetz (15.18)). Die Reibungskraft ist also von der Form $- \beta ( \mathbf { d } u / \mathbf { d } t )$ , mit $\beta = \mathrm{const}$ , und muss zur rücktreibenden Federkraft −ku in (33.1) addiert werden. Auf diese Weise erhält man

$$
m \frac {\mathrm{d} ^ {2} u}{\mathrm{d} t ^ {2}} + \beta \frac {\mathrm{d} u}{\mathrm{d} t} + k u = 0 \quad \begin{array}{l} (\text {Bewegungsgleichung der} \\ \text {gedämpften Schwingung}). \end{array} \tag {33.21}
$$

Die allgemeine Lösung dieser Differenzialgleichung lautet

$$
u (t) = u _ {0} \mathrm{e} ^ {- \delta t} \sin (\omega t + \varphi_ {0}) \tag {33.22}
$$

mit $\delta = \beta / ( 2 m )$ als **Dämpfungskonstante** (Abklingkonstante) und

$$
\omega = \sqrt {\omega_ {0} ^ {2} - \delta^ {2}} = \frac {2 \pi}{T} \quad \begin{array}{l l} & (\text {Kreisfrequenz der} \\ & \text {gedämpften Schwingung}). \end{array} \tag {33.23}
$$

ω<sub>0</sub> ist die Eigenkreisfrequenz des Oszillators, z. B. (33.6) oder (33.14).

Die Energieverluste führen also zu einer ständigen Abnahme der Amplitude $u _ { 0 } \mathbf { e } ^ { - \delta t }$ und zu einer Verringerung der Frequenz bzw. einer Zunahme der Periodendauer $T ,$

Die Richtigkeit von (33.23) überprüfe man durch Einsetzen der Lösung (33.22) und deren Ableitungen

$$
\frac {\mathrm{d} u}{\mathrm{d} t} = - \delta u _ {0} \mathrm{e} ^ {- \delta t} \sin (\omega t + \varphi_ {0}) + \omega u _ {0} \mathrm{e} ^ {- \delta t} \cos (\omega t + \varphi_ {0}),
$$

$$
\frac {\mathrm{d} ^ {2} u}{\mathrm{d} t ^ {2}} = (\delta^ {2} - \omega^ {2}) u _ {0} \mathrm{e} ^ {- \delta t} \sin (\omega t + \varphi_ {0}) - 2 \delta \omega u _ {0} \mathrm{e} ^ {- \delta t} \cos (\omega t + \varphi_ {0})
$$

in die Differenzialgleichung (33.21).

Ist die Auslenkung zu einem beliebigen Zeitpunkt t nach (33.22) $u ( t )$ , so ist sie nach Ablauf einer Periode wegen (33.22)

$$
\begin{array}{l} u (t + T) = u _ {0} \mathrm{e} ^ {- \delta (t + T)} \sin [ \omega (t + T) + \varphi_ {0} ] \\ = u _ {0} \mathrm{e} ^ {- \delta (t + T)} \sin (\omega t + \varphi_ {0}) = u (t) \cdot \mathrm{e} ^ {- \delta T}. \\ \end{array}
$$

Den natürlichen Logarithmus des Quotienten $u ( t ) / u ( t + T )$ aus zwei aufeinander folgenden phasengleichen Schwingungszuständen $( \mathbf { z } , \mathbf { B } .$ den Amplituden $u _ { n }$ und $u _ { n + 1 }$ mit $n = 1 , 2 , \ldots )$

$$
\ln \frac {u (t)}{u (t + T)} = \ln \frac {u _ {n}}{u _ {n + 1}} = \delta T = \Lambda \tag {33.24}
$$

bezeichnet man als **logarithmisches Dekrement Λ**. Es stellt ein anschauliches Maß für die Dämpfung eines Oszillators dar und kann experimentell einfach bestimmt werden.

**Schwache und starke Dämpfung.** Die Konstanten $u _ { 0 }$ und $\varphi _ { 0 }$ sind in der allgemeinen Lö- sung (33.22) zunächst unbestimmt. Um den Bewegungsablauf eindeutig angeben zu können, werden sie aus den Anfangsbedingungen ermittelt. Erhält z. B. die Masse des linearen Federschwingers zum Zeitpunkt $t = 0$ in seiner Ruhelage die Anfangsgeschwindigkeit $\nu _ { 0 }$ , so gilt

$$
u (0) = 0 = u _ {0} \sin \varphi_ {0}; \quad \dot {u} (0) = v _ {0} = u _ {0} (- \delta \sin \varphi_ {0} + \omega \cos \varphi_ {0}).
$$

Daraus folgt $\varphi _ { 0 } = 0 ,   u _ { 0 } = \nu _ { 0 } / \omega = \nu _ { 0 } / \sqrt { \omega _ { 0 } ^ { 2 } - \delta ^ { 2 } }$ und der Bewegungsablauf (Bild 33.5a)

$$
u (t) = \frac {v _ {0}}{\sqrt {\omega_ {0} ^ {2} - \delta^ {2}}} \mathrm{e} ^ {- \delta t} \sin \sqrt {\omega_ {0} ^ {2} - \delta^ {2}} t \quad (\text {Schwingfall} \delta <   \omega_ {0}). \tag {33.25}
$$

![](images/page_370_chart_2.jpg)

<details>
<summary>line</summary>

| Time (t) | u (a) | u (b) | u (c) |
| --- | --- | --- | --- |
| 0 | 0 | 0 | 0 |
| Peak 1 | \(u_{1}\) | — | — |
| Trough 1 | — | \(u_{1}\) | — |
| Peak 2 | \(u_{2}\) | — | — |
| Trough 2 | — | \(u_{2}\) | — |
| Peak 3 | \(u_{3}\) | — | — |
| Trough 3 | — | \(u_{3}\) | — |
| Peak 4 | \(u_{4}\) | — | — |
| Trough 4 | — | \(u_{4}\) | — |
| End of period | \(u_{\delta t}\) | \(u_{\delta t}\) | \(u_{\delta t}\) |
</details>

Bild 33.5 Freie gedämpfte Schwingungen für verschiedene Dämpfung bei gleichen Anfangsbedingungen $u ( 0 ) = 0$ und $\dot { u } ( 0 ) = \nu _ { 0 } { : }$ a) schwache Dämpfung: $\delta < \omega _ { 0 }$ (Schwingfall) b) starke Dämpfung: $\delta > \omega _ { 0 }$ (Kriechfall) c) $\delta = \omega _ { 0 }$ (aperiodischer Grenzfall)

Allerdings gilt der zeitliche Verlauf (33.25) nur für den sog. **Schwingfall**, der sich bei schwacher Dämpfung, d. h. $\delta < \omega _ { 0 }$ , ergibt. Vom Schwingfall unterscheidet sich grundsätzlich der sog. **Kriechfall**, in den die Bewegung bei starker Dämpfung, d. h. für $\delta > \omega _ { 0 }$ , übergeht. Er soll jetzt mit den oben formulierten Anfangsbedingungen behandelt werden.

Weil das Argument der Sinusfunktion in (33.25) $\sqrt { \omega _ { 0 } ^ { 2 }   -   \delta ^ { 2 } } t$ für $\delta > \omega _ { 0 }$ in die imaginäre Grö- ße $\mathrm { j }   \sqrt { \delta ^ { 2 }   -   \omega _ { 0 } ^ { 2 } } t = \mathrm { j }   x$ übergeht und damit seinen anschaulichen Sinn verliert, ersetzt man die trigonometrische Sinusfunktion mit Hilfe der Beziehung sin j $\mathrm { i } x = \mathrm { j }$ sinhx durch die hyperbolische Sinusfunktion. So erhält man den Bewegungsablauf (Bild 33.5b)

$$
u (t) = \frac {v _ {0}}{\sqrt {\delta^ {2} - \omega_ {0} ^ {2}}} \mathrm{e} ^ {- \delta t} \sinh \sqrt {\delta^ {2} - \omega_ {0} ^ {2}} t \quad (\text {Kriechfall} \delta > \omega_ {0}). \tag {33.26}
$$

Einen unperiodischen Verlauf liefert auch der sog. **aperiodische Grenzfall** für $\delta = \omega _ { 0 }$ . Mit

$$
\omega = \sqrt {\omega_ {0} ^ {2} - \delta^ {2}} \quad \text {und} \quad \lim _ {\omega \to 0} \frac {\sin \omega t}{\omega} = t
$$

erhält man aus (33.25) bei gleichen Anfangsbedingungen für diesen Bewegungsablauf (Bild 33.5c)

$$
u (t) = v _ {0} t \mathrm{e} ^ {- \delta t} \quad (\text {aperiodischer Grenzfall} \delta = \omega_ {0}). \tag {33.27}
$$

In der Technik wird dieser Fall angestrebt, wenn (z. B. bei Messinstrumenten) der stationäre Endzustand in kürzester Zeit ohne vorherige Schwingungen erreicht werden soll.

## Beispiel 33.4:

Wie groß ist ein kurzzeitiger Kraftstoß (= Anfangsimpuls $p _ { 0 } = m \nu _ { 0 } )$ , der einem Schwingungssystem aus der Ruhelage die maximale Auslenkung $u _ { 1 } = 5 ,$ 6cm erteilt? (Periodendauer $T =$ 1,8s; logarithmisches Dekrement $A = 3 { , } 0 ;$ Masse $m = 4 { , } 5   \mathrm { g . ) }$

Lösung: Mit (33.23) $\omega = \sqrt { \omega _ { 0 } ^ { 2 }   -   \delta ^ { 2 } }$ bestimmt man nach (33.25) für das erste Maximum aus du/d $t = \nu _ { 0 }   \mathbf { e } ^ { - \delta t } [ - ( \delta / \omega )$ sinωt+cosωt] = 0 dessen Zeitpunkt $t = t _ { 1 }$ . Man erhält mit (33.23) und (33.24) tanω $t _ { 1 } = \omega / \delta = 2 \pi / \Lambda , \omega t _ { 1 } = 1$ ,1253 und aus (33.25) mit (33.23) $\nu _ { 0 } = u _ { 1 } ( 2 \pi / T )   \mathbf { e } ^ { ( \Lambda / 2 \pi ) \omega t _ { 1 } } /$ sinω $t _ { 1 }$ . Damit wird $p _ { 0 } = m v _ { 0 } = 1 . 6 7 \cdot 1 0 ^ { - 3 }   \mathrm { N } \cdot \mathrm { s }$

Dieses Messprinzip wird beim **ballistischen Galvanometer** angewendet, mit dem Stromstöße (= Ladungsmengen, vgl. Abschnitt 23.1) und Spannungsstöße (= Magnetflüsse, vgl. Abschnitt 30.1) gemessen werden. Sie sind den Galvanometer-Maximalausschlägen $u _ { \mathrm { m } }$ proportional, wenn die Periodendauer T des Instruments groß gegen die Dauer des Messvorgangs ist (s. nachfolgende Aufgabe 33.4). □

## Aufgaben

**33.4** Man zeige, dass im aperiodischen Grenzfall (Bild 33.5c) die Fläche unter der $u ( t )$ -Kurve $\int _ { 0 } ^ { \infty } \stackrel { \circ } { u ( t ) } \mathrm { d } t   \mathsf { a } )$ für δ = const proportional zum Maximum $u ( t _ { \mathrm { m } } ) = u _ { \mathrm { m } } , \mathsf { b } )$ für $v _ { 0 } = \mathbf { c o n s t }$ proportional zum Quadrat des Maximums $u _ { \mathrm { m } } ^ { 2 }$ ist.
**33.5** Bild 33.5a stelle die mit einem Oszillographen (Zeitbasis: 10 µs/cm) aufgenommene Abklingkurve eines Schwingers in Originalgröße dar. Man bestimme Frequenz $f$ und Dämpfungskonstante $\delta . - A n l e i t u n g { : }$ Man entnehme zunächst $T$ (zweckmäßig aus der Mittelung über vier Perioden) und bestimme daraus $f .$ Aus $u _ { 1 }$ und $u _ { 2 }$ erhält man $\delta$ nach (33.24).

## 33.6 Erzwungene Schwingungen

Wird ein schwingungsfähiges System permanent von außen angeregt, ohne dass es auf den Erreger zurückwirken kann, so spricht man von erzwungenen Schwingungen. So stellt $\mathbf { z } , \mathbf { B } .$ eine von einem Motor angetriebene, nicht ausgewuchtete Welle einen Schwinger dar, der bei zu fester Kopplung an das Fundament der Maschine dieses zum Mitschwingen bringt. In diesem Fall ist die Welle der Erreger (Oszillator), das Fundament der Mitschwinger (Resonator).

![](images/page_371_chart_9.jpg)

<details>
<summary>line</summary>

| Time Interval | Signal Type | Description |
| --- | --- | --- |
| 0~4π | Input | Sinusoidal wave (x0) |
| 4π~8π | Output | Sinusoidal wave (u) |
| 8π~12π | Output | Sinusoidal wave (u) |
| \(\omega t\) | Output | Horizontal axis variable |
| \(\varphi\) | Output | Vertical distance between peaks of the two signals |
</details>

Bild 33.6 Erzeugung erzwungener Schwingungen u(t) durch Aufprägen von Erregerauslenkungen x(t)

Einfache Experimente zeigen, dass nach Einsetzen der Erregung ein Einschwingvorgang durchlaufen wird, der anschließend in den stationären eingeschwungenen Zustand übergeht, in dem die erzwungene Schwingung $u ( t )$ bei konstanter Amplitude der Erregerschwingung $x ( t )$ dieser mit gleicher Frequenz, jedoch mit einer Phasenverschiebung $\varphi$ zeitlich nachläuft (Bild 33.6).

Der lineare Federschwinger ist der periodischen Erregung $x ( t ) = x _ { 0 }$ sinωt ausgesetzt, die durch Drehbewegung des Antriebs mit der Winkelgeschwindigkeit ω hervorgerufen wird. Damit wird die Aufhängung der Feder um x verschoben und die Feder um den Betrag $u   -   x$ gestaucht oder gedehnt. Die rücktreibende Federkraft auf die Masse m beträgt daher $- k ( u   -   x )$ statt $- k u$ bei der freien Schwingung. Die Kräftebilanz für die erzwungene gedämpfte Schwingung lautet somit anstelle von (33.21)

$$
m \frac {\mathrm{d} ^ {2} u}{\mathrm{d} t ^ {2}} + \beta \frac {\mathrm{d} u}{\mathrm{d} t} + k u = k x (t) \quad \text {bzw.} = F (t) \quad \begin{array}{l} \text {(Bewegungsgleichung der}\\ \text {erzwungenen gedämpften}\\ \text {Schwingung)} \end{array} \tag {33.28}
$$

für beliebige zeitabhängige Erregerkräfte $F ( t )$ . Mit $\delta = \beta / ( 2 m )$ und $\omega _ { 0 } ^ { 2 } = k / m$ (vgl. Abschnitt 33.5) folgt daraus die inhomogene Differenzialgleichung

$$
\frac {\mathrm{d} ^ {2} u}{\mathrm{d} t ^ {2}} + 2 \delta \frac {\mathrm{d} u}{\mathrm{d} t} + \omega_ {0} ^ {2} u = \omega_ {0} ^ {2} x = \omega_ {0} ^ {2} x _ {0} \sin \omega t. \tag {33.29}
$$

Mit dem periodischen Lösungsansatz für den eingeschwungenen Zustand

$$
u = u _ {0} \sin (\omega t - \varphi) = u _ {0} (\sin \omega t \cos \varphi - \cos \omega t \sin \varphi)
$$

erhält man nach zweimaligem Differenzieren, Einsetzen in (33.28) und Vergleich der Koeffizienten von sinωt und cosωt das Gleichungssystem

$$
(\omega_ {0} ^ {2} - \omega^ {2}) \cos \varphi + 2 \delta \omega \sin \varphi = \frac {\omega_ {0} ^ {2} x _ {0}}{u _ {0}} \tag {33.30a}
$$

$$
- (\omega_ {0} ^ {2} - \omega^ {2}) \sin \varphi + 2 \delta \omega \cos \varphi = 0 \tag {33.30b}
$$

für $u _ { 0 }$ und $\varphi .$ Aus (33.30a) und (33.30b) folgt nach Quadrieren und Addieren für das Verhältnis von erregter Amplitude $u _ { 0 }$ und Erregeramplitude $x _ { 0 } ;$

$$
\frac {u _ {0}}{x _ {0}} = \frac {\omega_ {0} ^ {2}}{\sqrt {(\omega_ {0} ^ {2} - \omega^ {2}) ^ {2} + (2 \delta \omega) ^ {2}}} = \frac {\omega_ {0} ^ {2}}{\omega_ {0} ^ {2} - \omega^ {2}} \cos \varphi \qquad (\text {Amplitudengang}) \tag {33.31}
$$

und aus (33.30b) für die Phasenverschiebung $\varphi$ zwischen der erzwungenen Schwingung $u ( t )$ und der Erregerschwingung $x ( t )$ :

$$
\tan \varphi = \frac {2 \delta \omega}{\omega_ {0} ^ {2} - \omega^ {2}} \quad \text {fur} 0 \leq \varphi \leq \pi \quad (\text {Phasengang}). \tag {33.32}
$$

Den **Amplitudengang** (33.31) einer erzwungenen Schwingung in Abhängigkeit von der Erregerfrequenz ω für verschiedene Dämpfungskonstanten $\delta$ zeigt Bild 33.7a. Für niedrige Frequenzen $\omega \ll \omega _ { 0 }$ sind Erregerschwingung und erregte Schwingung annähernd gleich. Mit zunehmender Frequenz steigt die Amplitude der erzwungenen Schwingung bis zu einem Maximum an und fällt für hohe Frequenzen $\omega \gg \omega _ { 0 }$ auf null ab. Die zum Maximum gehörige Frequenz $\omega _ { \mathrm { r e s } }$ erhält man durch Nullsetzen der ersten Ableitung des Amplitudengangs (33.31) nach $\omega ;$ es ergibt sich

$$
\omega_ {\mathrm{res}} = 2 \pi f _ {\mathrm{res}} = \sqrt {\omega_ {0} ^ {2} - 2 \delta^ {2}} \quad (\text {Resonanzkreisfrequenz}). \tag {33.33}
$$

Man beobachtet die für erzwungene Schwingungen charakteristische Erscheinung der

## Resonanz:

**Die Amplitude der erzwungenen Schwingungen weist für nicht zu große Dämpfungen stets ein Maximum auf, wenn die Erregerfrequenz in unmittelbarer Nähe der** Eigenfrequenz des Mitschwingers liegt (Resonanzbedingung: $\omega \approx \omega _ { 0 } )$

Bei geringer Dämpfung „erzwingen“ kleine Erregungen für $\omega = \omega _ { \mathrm { r e s } }$ sehr hohe Amplituden, ohne Dämpfung sogar unendlich große. Die damit verbundene Zerstörung des Systems bezeichnet man als Resonanzkatastrophe. Durchläuft aber z. B. eine Maschine beim Anlassen rasch den Resonanzbereich noch während des Einschwingvorganges, so bleiben die großen Resonanzamplituden ohne beeinträchtigende Wirkung auf den Resonator.

![](images/page_373_image_6.jpg)

Bild 33.7 a) Amplitudengang und b) Phasenverschiebung der erzwungenen Schwingung in Abhängigkeit von der Erregerfrequenz $\omega$ (in Pfeilrichtung nimmt die Dämpfung δ zu und die Resonanzkreisfrequenz (33.33) ab); $\omega _ { 0 }$ Eigenfrequenz der ungedämpften Schwingung des erregten Systems.

Der Phasenwinkel der erzwungenen Schwingung bleibt für $\omega = \omega _ { 0 }$ nach (33.32) um eine Viertelperiode $( \varphi = \pi / 2 )$ hinter der Erregerschwingung zurück. Der Resonator geht daher bei der Eigenkreisfrequenz $\omega = \omega _ { 0 }$ mit maximaler Geschwindigkeit durch die Gleichgewichtslage, wenn der Oszillator seine größte Auslenkung zeigt (Bild 33.6). Die Geschwindigkeit der Masse und die Oszillatorauslenkung sind dann als Vektoren immer gleichgerichtet, so dass die Bewegung der Masse in jeder Lage über elastische Kraftwirkungen der Feder angetrieben wird.

## Die großen Amplituden im Resonanzfall entstehen durch permanente Energiezufuhr in jeder Schwingungslage.

Für $\omega < \omega _ { 0 }$ ist nach (33.32) tan $\varphi > 0$ , und die **Phasenverschiebung** $\varphi$ der erzwungenen Schwingung gegenüber der Erregerschwingung ist für kleine Dämpfungskonstanten $\delta$ und bei größerem $\delta$ für sehr niedrige Erregerfrequenzen $( \omega \ll \omega _ { 0 } )$ klein (Bild 33.7b). Für $\omega > \omega _ { 0 }$ ist tan $\varphi < 0 ,$ , und $\varphi$ nähert sich sowohl für kleines $\delta$ als auch für $\omega \gg \omega _ { 0 }$ dem Wert $\pi .$ Bei geringer Dämpfung kann daher ein Phasensprung von gleichphasigen $( \varphi \approx 0 )$ zu gegenphasigen Schwingungen $( \varphi \approx \pi )$ beobachtet werden, wenn die Erregerfrequenz wächst und $\omega _ { 0 }$ überstreicht. Phasenverschiebungen lassen sich experimentell über LISSAJOUS-Figuren (s. Abschnitt 35.3) ermitteln.

## Beispiele 33.5:

1. Rotierende Maschinenwellen erleiden infolge auftretender Fliehkräfte eine elastische Durchbiegung (s. Bild 33.8). Die Welle trage eine exzentrische Schwungmasse $m = 5 6 0   \mathrm { k g }$ mit dem Schwerpunktabstand x von der Wellenachse und dem Schwerpunktabstand u von der Drehachse. Die Durchbiegung $( u   -   x )$ sei der im Schwerpunkt angreifenden Fliehkraft proportional. Die Richtgröße für die Durchbiegung der Welle beträgt $k = 1 , 0 3 \cdot 1 0 ^ { 6 }   \mathrm { N / m }$ . Man bestimme die kritische Drehzahl $n ,$ bei der Resonanz mit der Eigenfrequenz der Welle auftritt.

![](images/page_374_image_4.jpg)

<details>
<summary>text_image</summary>

m
x
u
ω
</details>

Bild 33.8 Durchbiegung einer rotierenden Maschinenwelle bei Resonanz

Lösung: Aus (33.33) $\omega _ { \mathrm { r e s } } = \omega _ { 0 }$ folgt $\delta = 0$ . Nach (5.6) und (33.1) ist $F = m \omega ^ { 2 } u = k ( u - x )$ und daher

$$
u = x \frac {\omega_ {0} ^ {2}}{\omega_ {0} ^ {2} - \omega^ {2}}.
$$

u geht gegen ∞, wenn $\omega \rightarrow \omega _ { 0 } = \sqrt { k / m } = 4 2 { , } 9 { \sf s } ^ { - 1 }$ , d. h. $n = \omega / ( 2 \pi ) = 6 { , } 8 { \mathrm { s } } ^ { - 1 }$ . Nach Überschreiten der kritischen Drehzahl läuft die Welle wieder ruhig; sie „zentriert“ sich selbst.

2. Wie groß ist die Resonanzüberhöhung $( u _ { 0 } / x _ { 0 } ) _ { \mathrm { m a x } }$ für die Welle aus Beispiel 33.5/1, wenn die Dämpfungskonstante $\delta = 1 5   \mathrm { s } ^ { - 1 }$ beträgt?

Lösung: Durch Einsetzen von $\omega ^ { 2 } = \omega _ { \mathrm { r e s } } ^ { 2 } = \omega _ { 0 } ^ { 2 }   -   2 \delta ^ { 2 }$ in (33.31) folgt

$$
\left(\frac {u _ {0}}{x _ {0}}\right) _ {\max} = \frac {1}{2 \delta} \frac {\omega_ {0} ^ {2}}{\sqrt {\omega_ {0} ^ {2} - \delta^ {2}}} \quad (\text {Resonanzüberhöhung}). \tag {33.34}
$$

Mit $\omega _ { 0 } ^ { 2 } = 1 8 3 9   \mathrm { s } ^ { - 2 }$ und $\delta ^ { 2 } = 2 2 5   \mathrm { s } ^ { - 2 }$ erhält man $( u _ { 0 } / x _ { 0 } ) _ { \mathrm { m a x } } = 1 { , } 5 3$ , entsprechend 53%.

## Aufgaben

**33.6** Ein Schwinger mit der Eigenkreisfrequenz $\omega _ { 0 } = 1 5 \mathrm { , } 7   \mathrm { s } ^ { - 1 }$ und der Dämpfungskonstante $\delta = 0 , 7 8 6   \mathrm { s } ^ { - 1 }$ wird durch eine Erregerschwingung der Amplitude $x _ { 0 } = 5$ mm mit der Kreisfrequenz $\omega = 1 4 { , } 9 3 4 { \mathrm {   s } } ^ { - 1 }$ anregt. a) Mit welcher Phasenverschiebung und mit welcher Amplitude folgt die erregte Schwingung der Erregerschwingung? b) Bei welcher Erregerkreisfrequenz $\omega _ { \mathrm { r e s } }$ tritt Resonanz auf, und wie groß ist die Resonanzamplitude?
**33.7** Wie groß muss die Dämpfungskonstante $\delta$ (verglichen mit der Eigenfrequenz $\omega _ { 0 }$ der ungedämpften Schwingung) mindestens sein, damit eine Resonanzerscheinung ausbleibt (vgl. Bild 33.7a)?
**33.8** Man drücke die Phasenverschiebung $\varphi _ { \mathrm { r e s } }$ bei Resonanz durch $\omega _ { 0 }$ und $\delta$ aus.

## 34.1 Der geschlossene Schwingkreis

Eine Parallelschaltung eines Kondensators (Kapazität C) und einer Spule (Induktivität L) bezeichnet man als geschlossenen **Schwingkreis**. Wurde der Kondensator in Bild 34.1 bei Schalterstellung 1 aufgeladen, kann sich die im Kondensator gespeicherte Ladung +Q und −Q durch einen Stromfluss i über die Spule ausgleichen, sobald der Schalter in Stellung 2 gebracht wird. Spannung und elektrische Feldstärke des Kondensators nehmen ab, und gleichzeitig baut sich mit dem durch die Spule fließenden Strom ein Magnetfeld auf. Die Zunahme des magnetischen Flusses induziert eine Gegenspannung, welche nur ein gebremstes Anwachsen des Stromes zulässt. Sind Spannung und elektrische Feldstärke des Kondensators null, haben Strom und magnetische Feldstärke in der Spule ihren größten Wert erreicht. Die elektrische Feldenergie ist vollständig in magnetische Feldenergie umgewandelt. Mit dem Ladungsausgleich entfällt die Ursache des Entladestroms, und das Magnetfeld muss zusammenbrechen. Die Abnahme des Magnetflusses induziert eine Spannung, die jetzt so gerichtet ist, dass der Strom in gleicher Richtung weiterfließt und nur allmählich abnehmen kann. Gleichzeitig wird der Kondensator mit umgekehrter Polarität erneut aufgeladen. Spannung und elektrische Feldstärke steigen entgegengesetzt zur Ausgangsrichtung an und erreichen ihren größten Wert, wenn das Magnetfeld verschwunden ist. Dann wiederholt sich der Vorgang mit umgekehrter Richtung und im weiteren Verlauf periodisch.

**Im Schwingkreis findet eine periodische gegenseitige Umwandlung von elektrischer und magnetischer Feldenergie statt (elektromagnetische Schwingung).**

![](images/page_375_image_5.jpg)

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

Tabelle 34.1 Analogiebeziehungen zwischen Größen für Translations-, Rotations- und elektrische Schwingungen

<table><tr><td></td><td>Translations-schwingungen</td><td>Rotationsschwin-gungen</td><td>elektrische Schwingungen</td></tr><tr><td>kinetische Energie</td><td> $\frac{m}{2} \dot{u}^{2}$ </td><td> $\frac{J}{2} \dot{\varphi}^{2}$ </td><td> $\frac{L}{2} i^{2}$ </td></tr><tr><td>potenzielle Energie</td><td> $\frac{k}{2} u^{2}$ </td><td> $\frac{D}{2} \varphi^{2}$ </td><td> $\frac{1}{2C} q^{2}$ </td></tr><tr><td rowspan="2">zeitabhängige Größen</td><td> $\dot{u}$ </td><td> $\dot{\varphi}$ </td><td> $\dot{q} = i$ </td></tr><tr><td> $u$ </td><td> $\varphi$ </td><td> $q = \int i \, dt$ </td></tr><tr><td rowspan="3">zeitunabhängige Konstanten</td><td> $m$ </td><td> $J$ </td><td> $L$ </td></tr><tr><td> $\beta$ </td><td> $\beta_{\varphi}$ </td><td> $R$ </td></tr><tr><td> $k$ </td><td> $D$ </td><td> $1/C$ </td></tr><tr><td>Eigenkreisfrequenz</td><td> $\omega_{0} = \sqrt{\frac{k}{m}}$ </td><td> $\omega_{0} = \sqrt{\frac{D}{J}}$ </td><td> $\omega_{0} = \frac{1}{\sqrt{LC}}$ </td></tr><tr><td>Dämpfungskonstante</td><td> $\delta = \frac{\beta}{2m}$ </td><td> $\delta = \frac{\beta_{\varphi}}{2J}$ </td><td> $\delta = \frac{R}{2L}$ </td></tr></table>

## 34.2 Strom- und Spannungsresonanz

Ebenso wie bei mechanischen Oszillatoren kann man auch das Mitschwingen von elektrischen Schwingkreisen durch Erregung von außen erzwingen. Da man eine Induktivität L und eine Kapazität C parallel oder in Reihe schalten kann, sind zwei Möglichkeiten der Anregung zu unterscheiden. Bild 34.2 zeigt einen Parallelkreis, der durch einen eingespeisten Wechselstrom i(t), und einen Reihenkreis, der durch eine angelegte Wechselspannung u(t) von außen zu erzwungenen Schwingungen angeregt wird. Beide Quellen seien ideal, d. h., die zeitlichen Verläufe von u(t) und i(t) werden durch die internen Vorgänge im Schwingkreis nicht beeinflusst.

![](images/page_377_image_6.jpg)

Bild 34.2 Anregung a) eines Parallelschwingkreises durch eine Wechselstromquelle mit $i = I_{0} \sin \omega t,  b$ eines Reihenschwingkreises durch eine Wechselspannungsquelle mit $u = U _ { 0 }$ sinωt zu erzwungenen Schwingungen.

**Parallelschwingkreis** (Bild 34.2a). Der fremderregte Parallelkreis entspricht im zeitlichen Ablauf seiner erzwungenen Schwingungen dem fremderregten Federschwinger (Bild 33.7). Durch den Wechselstrom $i = i _ { 0 } \sin \omega t$ wird dem Kondensator C fortwährend Ladung $q = \int i   \mathbf { d } t \; \mathbf { z } \mathbf { u } -$ und abgeführt, so wie beim Federschwinger durch den Erregerausschlag $x = x _ { 0 }$ sinωt dauernd der Aufhängepunkt seiner Feder bewegt wird. $q$ und x sind entsprechende permanente Störungen des Gleichgewichtszustandes, denen Ausgleichsvorgänge des Schwingungssystems folgen, die jedoch vom Rhythmus der Störungen synchronisiert werden. Stimmt aber die Periodendauer des Wechselstroms und der Eigenschwingung überein (Resonanz), beginnt die Ladungszufuhr durch die Stromquelle immer in dem Moment, wenn die Kapazität C gerade mit der Entladung über die Induktivität L beginnt. Daher steigen die Stromamplituden der er zwungenen Schwingung und die Schwingungsenergie von Periode zu Periode an (Einschwingvorgang), bis die gleichzeitig steigenden Energieverluste im OHMschen Widerstand R die laufend zugeführten Energiemengen gerade kompensieren (eingeschwungener Zustand).

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

![](images/page_379_image_12.jpg)

Bild 34.3 Amplitudengang (links, in nicht normierter Darstellung) und Phasenverschiebung (rechts) des Reihenschwingkreises in Abhängigkeit von der Erregerfrequenz ω (in Pfeilrichtung nimmt die Dämpfung δ zu.)

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

**Fremderregung (Verstärkerprinzip).** Eine kleine Wechselspannung $u _ { 1 }$ an der Basis des Transistors führt zu periodischen Schwankungen des Kollektorstromes um seinen Mittelwert, d. h., dem Gleichstrom $I _ { \mathrm { C } }$ ist ein Wechselstrom i überlagert. Er bildet den Erregerwechselstrom für den Schwingkreis, der erzwungene Schwingungen in Stromresonanz ausführt (vgl. 34.2). Auch die Kollektorspannung erleidet infolge Spannungsabfall an Induktivität L und Kapazität C periodische Schwankungen um den Wert der Betriebsspannung $U _ { \mathrm { b } } ,$ d. h., der Kollektorgleichspannung $U _ { \mathrm { b } }$ ist eine Wechselspannung $u _ { 2 }$ überlagert. Das Verhältnis von Ausgangs- zu Eingangswechselspannung definiert die Spannungsverstärkung

$$
V = \frac {u _ {2}}{u _ {1}}. \tag {34.13}
$$

Die zur Verstärkung notwendige Energie wird der Betriebsspannungsquelle entzogen.

![](images/page_381_image_5.jpg)

Bild 34.4 a) Fremderregte Verstärkerschaltung, b) meissnersche Rückkopplungsschaltung mit Transistoren

Zur **Selbsterregung** eines Schwingkreises mit einer Verstärkerstufe ist es notwendig, den Gleichlauf von Erregung und Schwingung zu gewährleisten, also den Kollektorwechselstrom durch die Schwingungsfrequenz selbst zu steuern und die Energieeinspeisung in der richtigen Phasenlage vorzunehmen. Das gelang erstmals mit der MEISSNERschen Rückkopplungsschaltung durch eine Rückführungsschleife vom Ausgang auf den Eingang einer Verstärkerstufe (Bild 34.4b). Dabei sind Schwingkreisspule (L) und Basiskreis- oder Rückkopplungsspule $( L _ { \mathrm { R } } )$ induktiv wie Primär- und Sekundärwicklung eines Transformators gekoppelt. Dadurch wird die Schwingwechselspannung im Verhältnis der Windungszahlen unterteilt, so dass der Bruchteil von Primär- zu Sekundärspannung des „Transformators

$$
\ddot {u} = \frac {u _ {1}}{u _ {2}} \tag {34.14}
$$

als Steuerwechselspannung auf die Basis des Transistors gelangt. Der darauf einsetzende Kollektorwechselstrom i regt den Schwingkreis erneut und im weiteren Verlauf über die Rückführungsschleife periodisch an. Die richtige Phasenlage wird durch entsprechende Polung der Basiskreisspule erreicht.

Die Selbsterregung wird entweder durch den Einschaltvorgang oder durch kleine statistische Schwankungen des Kollektorstromes in Gang gebracht und der Schwingkreis zu Eigenschwingungen angestoßen. Die kleinen Anfangsamplituden schaukeln sich wie in Bild 33.7 durch fortwährende Verstärkung in einem Einschwingvorgang zum stationären eingeschwungenen Zustand auf. Beide Vorgänge lassen sich mit einem Oszillographen gut demonstrieren.

Zum Aufrechterhalten einer ungedämpften Schwingung genügt es, wenn das Produkt von (34.5) und (34.6) $V \ddot { u } = 1$ ist. Zum Einschwingen muss $V \ddot { u } > 1$ sein. Daraus folgt:

Eine große Zahl von Schwingschaltungen beruht auf dem Rückkopplungsprinzip: Ein Bruchteil der Ausgangsspannung (-energie) eines Verstärkers wird auf den Eingang zurückgeführt und reproduziert nach Verstärkung die ungedämpfte Schwingung.

# Überlagerung harmonischer Schwingungen

Es kann vorkommen, dass Körper oder Teilchen zwei (oder mehrere) harmonische Schwingungen gleichzeitig ausführen. So folgt die Ladung eines Fahrzeuges gleichzeitig den Federschwingungen aller Radaufhängungen. Üben die Schwingungen keinen Einfluss aufeinander aus, wird die beobachtete Bewegung durch die Resultierende der Auslenkungen der einzelnen Schwingungen bestimmt. In diesem Fall spricht man von **ungestörter Überlagerung** (oder von **Superposition**) **von Schwingungen**. Es genügt, die Überlagerung von Schwingungen längs gleicher Richtung und längs aufeinander senkrechter Richtungen zu behandeln. Andere Fälle können auf diese zurückgeführt werden.

## 35.1 Überlagerung zweier Schwingungen längs gleicher Richtung

Haben zwei gegebene Schwingungen (33.3)

$$
u _ {1} = u _ {0} \sin (\omega_ {1} t + \varphi_ {1}) \quad \text {und} \quad u _ {2} = u _ {0} \sin (\omega_ {2} t + \varphi_ {2})
$$

gleiche Richtung und der Einfachheit halber auch gleiche Amplitude, dann ist ihre Summe gleich ihrer Resultierenden (skalare Superposition). Es ist nach der trigonometrischen Beziehung sinα+sin $\beta = 2 \cos \left[ ( \alpha - \beta ) / 2 \right]$ sin $[ ( \alpha + \beta ) / 2 ]$ :

$$
u = u _ {1} + u _ {2} = 2 u _ {0} \cos \left(\frac {\omega_ {1} - \omega_ {2}}{2} t + \frac {\varphi_ {1} - \varphi_ {2}}{2}\right) \sin \left(\frac {\omega_ {1} + \omega_ {2}}{2} t + \frac {\varphi_ {1} + \varphi_ {2}}{2}\right).
$$

Mit den Differenzen $\Delta \omega = \omega _ { 1 } - \omega _ { 2 } ,   \Delta \varphi = \varphi _ { 1 } - \varphi _ { 2 }$ sowie den Mittelwerten $\overline { { \omega } } = ( \omega _ { 1 } + \omega _ { 2 } ) / 2$ und $\overline { { \varphi } } = ( \varphi _ { 1 } + \varphi _ { 2 } ) / 2$ ergibt sich

$$
u = 2 u _ {0} \cos \left(\frac {\Delta \omega}{2} t + \frac {\Delta \varphi}{2}\right) \sin (\overline {{\omega}} t + \overline {{\varphi}}). \tag {35.1}
$$

Dieses Ergebnis wird nun diskutiert.

**Überlagerung von Schwingungen gleicher Frequenz und verschiedener Phase.** Ist $\omega _ { 1 } = \omega _ { 2 } =$ ω, d. h. $\Delta \omega = 0$ , so lautet (35.1)

$$
u = 2 u _ {0} \cos \frac {\Delta \varphi}{2} \sin (\omega t + \overline {{\varphi}}). \tag {35.2}
$$

Die Amplitude $2 u _ { 0 } \cos ( \Delta \varphi / 2 )$ der resultierenden harmonischen Schwingung hängt von der Phasendifferenz der beiden Teilschwingungen ab (s. Bild 35.1). Sie hat

a) ihren größten Wert $2 u _ { 0 }$ , wenn $\Delta \varphi = 0 , \pm 2 \pi , \pm 4 \pi , \dots \mathrm { i s t ,   d .   h . }$ , wenn die Maxima der beiden Teilschwingungen zusammenfallen;

b) den Wert null, wenn $\Delta \varphi = \pm \pi , \pm 3 \pi , \pm 5 \pi , . .$ . ist, d. h., wenn gleich große Maxima und Minima der beiden Teilschwingungen zusammenfallen.

![](images/page_383_chart_3.jpg)

<details>
<summary>line</summary>

| Waveform | Phase Shift \((\pi)\) |
| --- | --- |
| Left | 1/12 |
| Middle | 2/2 |
| Right | \(11/12 \pi\) |
</details>

Bild 35.1 Überlagerung zweier Schwingungen gleicher Frequenz mit kleiner Phasendifferenz $\Delta \varphi \rightarrow 0$ (links), mit $\Delta \varphi = \pi / 2$ (Mitte) und $\Delta \varphi \rightarrow \pi$ (rechts)

Der letztere Fall, wo sich zwei Schwingungen „gegenseitig auslöschen“, spielt bei den Interferenzerscheinungen eine große Rolle (s. Kapitel 41 Wellenoptik). Sind die Amplituden der Teilschwingungen verschieden, entsteht statt „Auslöschung“ ein Minimum der Überlagerung.

**Die Resultierende zweier harmonischer Schwingungen gleicher Richtung und gleicher Frequenz ist wieder eine harmonische Schwingung, deren Amplitude von der Phasendifferenz der Teilschwingungen abhängt.**

**Überlagerung von Schwingungen verschiedener Frequenz.** Die resultierende Schwingung ist wegen $\omega _ { 1 } \neq \omega _ { 2 }$ keine harmonische Schwingung. Unterscheiden sich die Frequenzen der Teilschwingungen sehr stark $( \mathrm { z .   B .   } \omega _ { 1 } \gg \omega _ { 2 } )$ , sind beide auch in der Resultierenden noch deutlich zu erkennen (s. Bild 35.2a).

Wenn sich bei der Überlagerung zweier harmonischer Schwingungen deren Frequenzen nur wenig unterscheiden, d. h. $\omega _ { 1 } \approx \omega _ { 2 } \approx \overline { { \omega } }$ mit $| \omega _ { 1 } - \omega _ { 2 } | = \Delta \omega \ll \overline { { \omega } }$ , liegt der wichtige Spezialfall einer Schwebung vor (Bild 35.2b). Für $\varphi _ { 1 } = \varphi _ { 2 } = 0$ erhält man dann aus (35.1)

$$
u = 2 u _ {0} \cos \left(\frac {\Delta \omega}{2} t\right) \sin \overline {{\omega}} t \qquad (\text {Schwebung}). \tag {35.3}
$$

![](images/page_383_chart_10.jpg)

<details>
<summary>line</summary>

| Waveform | Frequency Component | Amplitude Range |
| --- | --- | --- |
| a) | \(\omega1=10\omega2\) | ~ -2 to 2 |
| b) | \(7\omega1=8\omega2\) | ~ -2 to 2 |
</details>

Bild 35.2 Resultierende der Überlagerung zweier Schwingungen a) verschiedener Frequenz $\omega _ { 1 } \gg \omega _ { 2 }$ , b) nahezu gleicher Frequenz $\omega _ { 1 } \approx \omega _ { 2 }$ (Schwebung)