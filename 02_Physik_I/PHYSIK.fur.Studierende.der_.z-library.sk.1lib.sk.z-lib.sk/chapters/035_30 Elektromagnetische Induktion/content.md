# 30 Elektromagnetische Induktion

原始 PDF 第 331–337 页。

30

Elektromagnetische Induktion

## 30.1 Das faradaysche Induktionsgesetz

1831 erkannte FARADAY durch eine Reihe zielgerichteter Experimente, dass durch zeitlich veränderliche Magnetfelder elektrische Spannungen (Felder) erregt werden. Man nennt diese Erscheinung elektromagnetische Induktion. Wird zum Beispiel, wie in Bild 30.1a veranschaulicht, die in einem Magnetfeld befindliche Leiterschleife plötzlich aus dem Feld herausgezogen, so lässt sich mit einem angeschlossenen ballistischen Galvanometer (s. 23.1) ein **Spannungsstoß** $\int u _ { \mathrm { i n d } }$ dt messen (Bild 30.1b). Dieser hängt nur davon ab, wie viele Feldlinien durch die von der Leiterschleife umrandete Fläche A anfänglich hindurchtraten, er ist also durch den magnetischen Fluss $\varPhi = \int u _ { \mathrm { i n d } }$ dt innerhalb dieser Fläche gegeben. Diese Beobachtung ist bekannt als

## FARADAYsches Induktionsgesetz:

**Die induzierte Spannung in einem geschlossenen Leiterkreis, der den sich zeitlich ändernden magnetischen Fluss umrandet, ist gleich der negativen Änderungsgeschwindigkeit des magnetischen Flusses.**

$$
u _ {\mathrm{ind}} = - \frac {\mathrm{d} \varPhi}{\mathrm{d} t} \quad (\text {FARADAYSches Induktionsgesetz}). \tag {30.1}
$$

![](../../raw/pages_0321-0352/images/page_330_image_7.jpg)

Bild 30.1 a) Induktionsversuch zur Messung der magnetischen Flussdichte (Induktion) B. b) Mit einem ballistischen Galvanometer gemessener Spannungsstoß beim Herausziehen der Schleife aus dem Magnetfeld. Der magnetische Fluss Φ entspricht der Fläche unter der u(t)-Kurve, 1 bei schneller Bewegung, 2 bei langsamer Bewegung der Schleife; die Flächeninhalte unter beiden Kurven sind gleich. Vgl. Aufgabe 33.4.

Bei einer Spule mit N Windungen addieren sich die erregten Induktionsspannungen in den einzelnen Windungen zur Gesamtspannung

$$
u _ {\text {ind}} = - N \frac {\mathrm{d} \Phi}{\mathrm{d} t} \quad (\text {Induktionsspannung in einer Spule}). \tag {30.2}
$$

Auf dem oben beschriebenen und in Bild 30.1 dargestellten Prinzip beruhen die Flussmesser, wobei anstelle der Leiterbewegung auch das Magnetfeld ein- oder ausgeschaltet werden kann.

---

30.1 Das faradaysche Induktionsgesetz

329

Der dabei gemessene Spannungsstoß ist aber erst dann ein Maß für die Stärke des Magnetfeldes, wenn man ihn auf die vom Leiter umrandete und von den Feldlinien senkrecht durchsetzte Querschnittsfläche A bezieht. So erhält man eine weitere Messmethode zur Bestimmung der **magnetischen Flussdichte** oder **Induktion** (28.11) vom Betrage $B = \varPhi / A$

Im geschlossenen Leiterkreis ruft die Induktionsspannung nach dem OHMschen Gesetz einen Induktionsstrom hervor. Die induzierten Spannungen und Ströme sind im Allgemeinen (bei nichtlinearer Flussänderung) ebenfalls zeitlich veränderlich. Sie sollen, wie im Folgenden alle zeitlich veränderlichen Spannungen und Ströme, durch Kleinbuchstaben u und i gekennzeichnet werden.

Das Minuszeichen in (30.1) und (30.2) bringt den Energieerhaltungssatz zum Ausdruck, der hier speziell als **LENZsche Regel** über die Richtung der induzierten Spannungen und Ströme Auskunft gibt.

**LENZsche Regel: Der induzierte Strom ist stets so gerichtet, dass das von ihm erzeugte Magnetfeld der Ursache seiner Entstehung entgegenwirkt.**

![](../../raw/pages_0321-0352/images/page_331_image_6.jpg)

<details>
<summary>text_image</summary>

i
N
H
</details>

Bild 30.2 Zur lenzschen Regel: Sowohl bei Annäherung des Stabmagneten an den Drahtring als auch bei Entfernung desselben ist mechanische Arbeit zu verrichten.

Wird z. B. nach Bild 30.2 ein Stabmagnet mit dem Nordpol voran gegen einen Drahtring geführt, so wird in diesem ein Induktionsstrom i erregt, welcher um den Leiter herum ein Magnetfeld H erzeugt. Der Kreisstrom ist damit einem magnetischen Dipol äquivalent (s. 28.6), der seinen Nordpol auf der dem Stabmagneten zugewandten Seite hat. Daher muss bei Annäherung der gleichnamigen Magnetpole gegen die Abstoßungskraft mechanische Arbeit verrichtet werden; sie liefert die Energie für den sich ausbildenden Induktionsstrom im Drahtring. Wird der Nordpol vom Drahtring wegbewegt, kehrt sich die Stromrichtung in ihm um, so dass dem Nordpol des Magneten jetzt ein Südpol des Kreisstromes gegenübersteht, die sich gegenseitig anziehen; auch hierbei muss also Arbeit verrichtet werden.

Drückt man den magnetischen Fluss Φ nach (28.12) durch die magnetische Flussdichte B aus, so erhält das Induktionsgesetz (30.1) die Form

$$
u _ {\mathrm{ind}} = - \frac {\mathrm{d} \varPhi}{\mathrm{d} t} = - \frac {\mathrm{d}}{\mathrm{d} t} \int \boldsymbol {B} \cdot \mathrm{d} \boldsymbol {A} = - \frac {\mathrm{d}}{\mathrm{d} t} \int B \mathrm{d} A \cos \alpha . \tag {30.3}
$$

α ist der Winkel zwischen der Richtung von B und der Flächennormale der Fläche A, durch die der veränderliche magnetische Fluss Φ tritt. Aus Gleichung (30.3) lesen wir ab, dass Induktionsspannungen erzeugt werden können

1. durch zeitliche Änderung des Betrages B der magnetischen Flussdichte, z. B. infolge Ände rung des elektrischen Stromes, der das Magnetfeld erzeugt (vgl. 30.2), oder wegen (29.2) infolge Änderung der Art des Stoffes innerhalb des felderfüllten Raumes (Permeabilitätsänderung);

---

330

30 Elektromagnetische Induktion

2. durch zeitliche Änderung der Größe der Fläche A, die vom magnetischen Fluss durchsetzt wird, z. B. infolge der Bewegung eines Leiters relativ zum Magnetfeld (vgl. 30.4);
3. durch zeitliche Änderung des Winkels α zwischen Feldrichtung und Flächennormale, z. B. durch Drehen einer Leiterschleife im Magnetfeld (vgl. 30.4).

Induktionsspannungen bzw. -ströme können also entweder in relativ zum Magnetfeld ruhenden Leitern durch zeitlich veränderliche Magnetfelder (Transformatorprinzip) oder bei zeitlich konstanten Magnetfeldern durch Bewegung von Leitern relativ zum Magnetfeld (Generatorprinzip) erzeugt werden.

## Beispiel 30.1:

Der magnetische Fluss, der eine Leiterschleife durchsetzt, wächst in den ersten 2s gleichförmig von 0 auf 7Wb an, bleibt dann 3s konstant, um in den folgenden 4s gleichförmig bis auf −3Wb abzusinken. Man berechne die Spannungen, die während dieser drei Zeitintervalle in der Leiterschleife induziert werden.

Lösung: Bei einer gleichförmigen Änderung des Flusses vereinfacht sich das Induktionsgesetz (30.1) zu $u _ { \mathrm { i n d } } = - \Delta \varPhi / \Delta t$ . Während der ersten 2s wird wegen $\Delta \varPhi = 7 \mathrm { W b }$ die konstante Spannung von $- 3 { , } 5 \mathrm { V _ { i } }$ , in den letzten 4s wegen $\Delta \phi = - 1 0 \mathrm { W b }$ eine solche von +2,5V und bei konstantem magnetischen Fluss keine Spannung induziert. □

## 30.2 Selbstinduktion

Jeder stromführende Leiter ist von einem Magnetfeld umgeben, dessen Fluss der Stromstärke im Leiter proportional ist:

$$
\Phi = L I. \tag {30.4}
$$

Den Proportionalitätsfaktor L nennt man die Induktivität des Leiters. Aus der Einheitengleichung zu (30.4) folgt als

$$
\text {Einheit der Induktivität:} \quad [ L ] = [ \Phi ] / [ I ] = 1 \mathrm{V} \cdot \mathrm{s} / \mathrm{A} = 1 \text {Henry(H)}.
$$

Ist der Leiter zu einer **Spule** von N Windungen aufgewickelt, so ist bei gleicher Stromstärke der magnetische Fluss N-mal so groß. Es gilt dann anstelle von (30.4)

$$
N \Phi = L I \quad \text {bzw.} \quad N \Phi = L i. \tag {30.5}
$$

Die Induktivität eines Leiters wird nur durch seine Geometrie (Abmessungen, Gestalt) und die Art des Stoffes, der vom Magnetfeld durchsetzt wird (z. B. den Spulenkern), bestimmt.

## Beispiel 30.2:

Man berechne die Induktivität einer langen Zylinderspule (Bild 28.3a) mit $l = 5   \mathrm { c m }$ , Durchmesser $d = 6    mm ,   N = 500$

Lösung: Da das Feld im Innern der Spule hinreichend homogen ist, ergibt sich mit (30.5), (28.11) und (28.14) sowie (28.7)

$$
L = \frac {N \Phi}{I} = \frac {N B A}{I} = \frac {N \mu_ {0} H A}{I} = \frac {\mu_ {0} N ^ {2} A}{l} \quad \begin{array}{l} (\text {Induktivität einer} \\ \text {leeren Zylinderspule}). \end{array} \tag {30.6}
$$

Mit $A = \pi d ^ { 2 } / 4$ und den angegebenen Zahlenwerten folgt $L = 0 , 1 8   \mathrm { m H }$

---

30.2 Selbstinduktion

331

Ändert sich in einer Spule die elektrische Stromstärke, so ändert sich im Innern der Spule auch gleichzeitig der magnetische Fluss. Nach dem Induktionsgesetz wird deshalb in der felderzeugenden Spule selbst eine Spannung induziert (Selbstinduktion). Für sie folgt mit Gleichung (30.5) aus dem Induktionsgesetz (30.2)

$$
u _ {\mathrm{ind}} = - L \frac {\mathrm{d} i}{\mathrm{d} t} \quad (\text {Selbstinduktionsspannung}). \tag {30.7}
$$

Diese Spannung ruft in der Spule einen sekundären Induktionsstrom hervor, der nach der LENZschen Regel der primären Stromänderung entgegenwirkt. Er ist also dem Primärstrom entgegengerichtet, wenn dieser zunimmt, und gleichgerichtet, wenn dieser abnimmt. Wäre dies nicht $\mathbf { s o } ,$ käme es durch eine zufällige Erhöhung der Stromstärke zu einer fortwährenden Verstärkung des Stromes, was dem Energiesatz widersprechen würde. Infolge der Selbstinduktion kann die Stromstärke in einer Spule niemals sprunghaft, sondern immer nur mit einer gewissen zeitlichen Verzögerung ansteigen, so dass eine bestimmte Zeit vergeht, bis die Stromstärke ihren Maximalwert nahezu erreicht hat. Andererseits fließt beim plötzlichen Ausschalten des Spulenstroms der Induktionsstrom kurzzeitig weiter, wobei sehr hohe Selbstinduktionsspannungen z. B. zu Funkenentladungen an den Schaltkontakten führen.

![](../../raw/pages_0321-0352/images/page_333_image_5.jpg)

Bild 30.3 Zur Wirkung der Selbstinduktion im Stromkreis beim Einschaltvorgang (1) und beim Ausschaltvorgang (2): a) Schaltskizze, b) zeitlicher Verlauf des Stromes. Die Gleichrichterstrecke (Diode, s. 31.6) schützt den Schalter (Funkenlöschung); beim Einschaltvorgang ist sie in Sperrrichtung und beim Ausschaltvorgang in Durchlassrichtung gepolt.

Beim **Einschaltvorgang** (s. Bild 30.3a) ist die Summe aus dem Spannungsabfall an der Spule $- u _ { \mathrm { i n d } } =$ $L ( \mathbf { d } i / \mathbf { d } t )$ und dem Spannungsabfall am Widerstand Ri gleich der BetriebsspannungU<sub>0</sub>, d. h. L(di /dt)+ $R i = U _ { 0 }$ (inhomogene Differenzialgleichung für die Stromstärke). Mit $i = I _ { 0 }   -   i _ { \mathrm { i n d } }$ und $I _ { 0 } = U _ { 0 } / R = \mathrm { c o n s t }$ (Maximalwert der Stromstärke) lässt sie sich in die homogene Form $L ( \mathrm { d } i _ { \mathrm { i n d } } / \mathrm { d } t ) + R i _ { \mathrm { i n d } } = 0$ bringen, welche nach Trennung der Variablen in $\mathrm { d } i _ { \mathrm { i n d } } / i _ { \mathrm { i n d } } = - ( R / L )$ dt übergeht und mit der Anfangsbedingung $i = 0 = ( U _ { 0 } / R ) - i _ { \mathrm { i n d } }$ für $t = 0$ durch direkte Integration lösbar ist. Es ergibt sich ln $i_{\mathrm{ind}} - \ln(U_0 / R) =$ $- ( R / L )   t$ und hieraus die Lösung

$$
i = \frac {U _ {0}}{R} \left(1 - \mathrm{e} ^ {- \frac {R}{L} t}\right) = I _ {0} \left(1 - \mathrm{e} ^ {- \frac {R}{L} t}\right) \quad \begin{array}{l} (\text {Stromstärke beim} \\ \text {Einschaltvorgang}). \end{array} \tag {30.8}
$$

Man erkennt ein allmähliches Anwachsen der Stromstärke i bis zum Maximalwert $I _ { 0 }$ (Bild 30.3b, (1)). Beim **Ausschaltvorgang** $( U _ { 0 } = 0 )$ fließt dann der Induktionsstrom $i = - i _ { \mathrm { i n d } }$ über die Gleichrichterstrecke ab (bei vernachlässigbarem Widerstand der Diode, vgl. Bild 30.3a). Mit der Anfangsbedingung $i = I _ { 0 }$ für $t = 0$ ergibt sich aus $L ( { \bf d } i / { \bf d } t ) + R i = 0$ analog zu obiger Rechnung

$$
i = I _ {0} \mathrm{e} ^ {- \frac {R}{L} t} \quad \begin{array}{l} (\text {Stromstärke beim} \\ \text {Ausschaltvorgang}), \end{array} \tag {30.9}
$$

wonach beim Ausschalten des Gleichstromes die Stromstärke monoton auf null abklingt (Bild 30.3b, Kurve (2)). Die Geschwindigkeit der Stromänderung hängt in beiden Fällen wesentlich vom Quotienten $\tau = L / R$ ab, welcher die Dimension einer Zeit hat und Zeitkonstante des Stromkreises heißt.

---

332

30 Elektromagnetische Induktion

## 30.3 Energieinhalt des magnetischen Feldes

Zum Aufbau eines Magnetfeldes in einer Spule ist ein Spulenstrom erforderlich. Beim Einschalten des Stromes muss durch die Stromquelle Arbeit gegen die Wirkung der Selbstinduktion der Spule verrichtet werden. Diese Arbeit wird als **magnetische Feldenergie** im Magnetfeld der Spule gespeichert. Die Zunahme der Stromstärke i um di ist mit einer Erhöhung des magnetischen Flusses um dΦ verbunden, wobei die äußere Spannung u die Selbstinduktionsspannung (30.7) $u _ { \mathrm { i n d } } = - N ( \mathrm { d } \phi / \mathrm { d } t ) = - L ( \mathrm { d } i / \mathrm { d } t )$ kompensieren muss: $u + u _ { \mathrm { i n d } } = 0$ . Dazu ist nach (25.17) die Arbeit

$$
\mathrm{d} W = u i \mathrm{d} t = - u _ {\mathrm{ind}} i \mathrm{d} t = L \frac {\mathrm{d} i}{\mathrm{d} t} i \mathrm{d} t = L i \mathrm{d} i
$$

erforderlich. Die aufzuwendende Gesamtarbeit und damit die insgesamt im Magnetfeld gespeicherte Energie ist mit $L = \mathrm{const};$

$$
W _ {\mathrm{m}} = \int_ {0} ^ {I} L i \mathrm{d} i = \frac {1}{2} L I ^ {2} \quad (\text {magnetische Feldenergie}). \tag {30.10}
$$

Mit der Induktivität der Spule (30.6) $L = \mu _ { 0 } N ^ { 2 } A / l$ und mit (28.7) $I = H l / N$ folgt hieraus, wenn man die Feldenergie $W _ { \mathrm { m } }$ noch durch das Spulenvolumen $V = A l$ dividiert:

$$
w _ {\mathrm{m}} = \frac {1}{2} \mu_ {0} H ^ {2} = \frac {1}{2} B H \quad (\text {Energiedichte des magnetischen Feldes}). \tag {30.11}
$$

Diese Gleichung hat keinen Bezug mehr zur Spule und gilt allgemein für beliebige Magnetfelder im Vakuum. Für Stoffe mit konstanter Permeabilität ist $\mu _ { 0 }$ durch $\mu = \mu _ { \mathrm { r } } \mu _ { 0 }$ zu ersetzen.

## Beispiel 30.3:

Bestimme die Tragkraft eines als Hufeisenmagnet ausgeführten Elektromagneten (magnetisches Joch), dessen beide Polschuhe durch den zu tragenden (ferromagnetischen) Körper (Anker) zu einem magnetischen Kreis geschlossen werden. Man gehe davon aus, dass die im engen Luftspalt zwischen Polschuh und Anker vorhandene magnetische Energiedichte (30.11) gleich dem Anpressdruck $p$ zwischen Joch und Anker ist. Daten des Magnetkreises: Stromstärke $I = 4 \mathrm { A }$ , Windungszahl der Magnetspule $N = 2 0 0$ , geschlossener Eisenweg $l = 70    cm$ Eisenquerschnitt $A = 7    cm ^2;$ die Flussdichte entnehme man dem Bild 29.3a.

Lösung: Im Luftspalt ist B genauso groß wie im Eisen, so dass dort gilt $H = B / \mu _ { 0 }$ und nach (30.11) $w _ { \mathrm { m } } = p = B ^ { 2 } / ( 2 \mu _ { 0 } )$ . Die Tragkraft für beide Polflächen ist $F = 2 p A$ , also

$$
F = \frac {1}{\mu_ {0}} B ^ {2} A \quad (\text {Tragkraft eines Magnetjochs}). \tag {30.12}
$$

Mit den Zahlenwerten folgt aus (28.7) $H = N I / l = 1 1 4 3 \mathrm { A / m }$ und aus Bild 29.3a: B = 1,4T. Somit wird $F = 1 { , } 1 \mathrm { k N }$ □

## Aufgabe

**30.1** Um beim Abschalten von Spulen Funkenbildungen zwischen den Schaltkontakten zu vermeiden, werden z. B. parallel zu den Kontakten Kondensatoren geschaltet. Wie groß muss die Prüfspannung eines Funkenlöschkondensators mit $C = 4   \mu \mathrm { F }$ für eine vom Strom $I = 2 \mathrm { A }$ durchflossene Spule mit L = 1H sein? – Anleitung: Die beim Abschalten des Spulenstromes frei werdende magnetische Feldenergie muss im Kondensator als elektrische Feldenergie zwischengespeichert werden.

---

30.4 Elektromagnetische Induktion in einem bewegten Leiter

333

## 30.4 Elektromagnetische Induktion in einem bewegten Leiter

Wird ein gerades Drahtstück der Länge l senkrecht zu einem zeitlich konstanten, homogenen Magnetfeld B mit der Geschwindigkeit $\nu = \mathbf { d } s / \mathbf { d } t$ bewegt (Bild 30.4a), so überstreicht dieses in der Zeit dt das Flächenelement d $A = l \mathbf { d } s$ . Damit nimmt das Induktionsgesetz (30.1) wegen $\varPhi = B A$ die spezielle Form an:

$$
u _ {\mathrm{ind}} = - \frac {\mathrm{d} (B A)}{\mathrm{d} t} = - B \frac {\mathrm{d} A}{\mathrm{d} t} = - B l \frac {\mathrm{d} s}{\mathrm{d} t} = - B l v. \tag {30.13}
$$

Das Zustandekommen der Induktionsspannung im bewegten Leiter lässt sich wie folgt erklä- ren: Auf die frei verschiebbaren Leitungselektronen innerhalb des Drahtes, die gemeinsam mit dem Draht relativ zum Feld bewegt werden, wirkt die LORENTZ-Kraft (28.22) $\pmb { F } _ { \mathrm { L } } = - e ( \pmb { v } \times \pmb { B } )$ Dies führt während der Bewegung zu einer Ladungstrennung und damit zur Ausbildung eines elektrischen Feldes $E _ { \mathrm { i n d } }$ im Leiter. Gleichgewicht stellt sich ein, wenn die an den Elektronen angreifende resultierende Kraft $\boldsymbol { F } = - e \boldsymbol { E } _ { \mathrm { i n d } } + \boldsymbol { F } _ { \mathrm { L } } = 0$ wird bzw. $\pmb { E } _ { \mathrm { i n d } } = - ( \pmb { v } \times \pmb { B } )$ gilt. Zwischen den Leiterenden tritt demzufolge eine elektrische Induktionsspannung $u _ { \mathrm { i n d } } = E _ { \mathrm { i n d } } l$ auf. Für die Bewegung des Leiters mit der Geschwindigkeit v senkrecht zu B ergibt sich hieraus wieder Gleichung (30.13).

Werden die Leiterenden, zwischen denen eine Induktionsspannung auftritt, außerhalb des Feldes miteinander verbunden, so fließt in dem geschlossenen Kreis ein Induktionsstrom.

Am Widerstand des Kreises (Verbraucher) wird dann eine elektrische Leistung umgesetzt, die gleich der mechanischen Leistung ist, die zur Aufrechterhaltung der Bewegung des stromdurchflossenen Leiters im Magnetfeld aufgewendet werden muss.

![](../../raw/pages_0321-0352/images/page_335_image_8.jpg)

Bild 30.4 Induktion in einem im Magnetfeld bewegten Leiter a) bei Translationsbewegung, b) bei Rotationsbewegung (Prinzip des Wechselspannungsgenerators)

**Erzeugung von Wechselspannungen.** Zur laufenden Gewinnung elektrischer Energie aus mechanischer Arbeit muss eine periodische Bewegung von Leiterschleifen relativ zu einem Magnetfeld erfolgen. Ein einfaches Modell eines Wechselspannungsgenerators besteht aus einer mit konstanter Winkelgeschwindigkeit $\omega = \alpha / t$ (α Drehwinkel) rotierenden Schleife der Fläche A (Normalenvektor der Schleifenfläche mit dem Betrag A) in einem homogenen Magnetfeld der Induktion B (Bild 30.4b). Der die Leiterschleife durchsetzende magnetische Fluss Φ ändert sich dabei periodisch mit der Kreisfrequenz $\omega = 2 \pi f$ . Entsprechend (28.12) ist

$$
\varPhi = \varPhi (t) = \boldsymbol {B} \cdot \boldsymbol {A} = B A \cos \alpha = \varPhi_ {0} \cos \omega t. \tag {30.14}
$$

---

334

30 Elektromagnetische Induktion

Nach dem Induktionsgesetz (30.1) entsteht an den Schleifenenden eine **Wechselspannung**

$$
u (t) = - \frac {\mathrm{d} \varPhi}{\mathrm{d} t} = \omega \varPhi_ {0} \sin \omega t = U _ {0} \sin \omega t, \tag {30.15}
$$

deren Maximalwert $U _ { 0 } = \omega \varPhi _ { 0 } = \omega B A$ proportional zur Winkelgeschwindigkeit, magnetischen Flussdichte und Schleifenfläche ist.

## Eine gleichförmig im Magnetfeld rotierende Leiterschleife erzeugt eine harmonische Wechselspannung.

Wird am Wechselspannungsgenerator von außen ein Verbraucher mit dem Widerstand R angeschlossen, fließt ein **Wechselstrom** $i ( t ) = I _ { 0 }$ sinωt mit dem Maximalwert $I _ { 0 } = U _ { 0 } / R .$ . Bei der technischen Ausführung von Generatoren (Dynamomaschinen) sind viele Schleifen als Induktionsspulen (Anker) der Windungszahl N zur Vergrößerung der Maximalspannung $U _ { 0 } =$ ω $N \varPhi _ { 0 } = \omega N B A$ vereinigt. Der Permanentmagnet wird durch Elektromagnete ersetzt, wobei das Erregerfeld B zur Senkung des magnetischen Widerstandes bis auf kleine Luftspalte in einem geschlossenen Eisenkreis verläuft (vgl. 29.3). Da es nur auf die Relativbewegung von Leiterschleifen und Magnetfeld ankommt, werden Induktionsspulen meist am Ständer (Stator) des Generators fest verlegt, während sich die Erregerspulen auf dem Läufer (Rotor) befinden und sich an den Induktionsspulen vorbeidrehen. So kann die erzeugte Wechselspannung bequem am Ständer abgegriffen werden, während die geringen Erregerströme über Schleifringe dem Läufer zuzuführen sind.

## Beispiel 30.4:

Auf einem Tisch liegt eine kreisringförmige, isolierte Leiterschleife und darüber, entlang eines Durchmessers der Schleife, ein gerader langer Draht, durch den ein Wechselstrom $i ( t ) =$ $I _ { 0 }$ sinωt fließt. a) Welche induzierte Spannung zeigt ein an die Leiterschleife angeschlossenes Voltmeter in dieser Anordnung an? Was zeigt das Voltmeter an, wenn b) der Draht nicht durch den Schleifenmittelpunkt führt, c) der Draht den Tisch senkrecht durchsetzt?

Lösung: a) Das den Draht umgebende magnetische Wechselfeld durchsetzt die beiden halb kreisförmigen Hälften der Schleifenfläche mit den zeitlich veränderlichen Flüssen $\varPhi _ { 1 } ( t )$ und $\varPhi _ { 2 } ( t ) = - \varPhi _ { 1 } ( t )$ . Der Gesamtfluss $\varPhi _ { 1 } + \varPhi _ { 2 }$ durch die Schleife ist also zu jedem Zeitpunkt gleich null; es wird daher keine Spannung angezeigt. b) In diesem Fall ist der Gesamtfluss durch die Schleife ungleich null, und das Voltmeter zeigt eine Spannung an. c) Die magnetischen Feldlinien um den geraden Draht verlaufen jetzt in der gleichen Ebene wie die Drahtschleife (bzw. dazu parallelen Ebenen), durchsetzen diese also nicht, weshalb der Magnetfluss null ist und keine Induktionsspannung entsteht. □

## Aufgaben

**30.2** Ein gerader Draht bewegt sich mit einer Geschwindigkeit von 40cm/s senkrecht zur Drahtachse und senkrecht zu den Feldlinien durch ein 5cm breites homogenes Magnetfeld, wobei das an den Drahtenden angeschlossene Galvanometer von 1kΩ Innenwiderstand einen Strom von 10 µA anzeigt. Welche Stärke hat das Feld?
**30.3** Der Anker einer Dynamomaschine mit 1000 Windungen und einer Querschnittsfläche von $1 0 0   \mathrm { c m } ^ { 2 }$ rotiert in einem homogenen Magnetfeld um eine zum Feld senkrechte Achse mit einer Drehzahl von $6 0 0 0   \mathrm { \bar { m i n } ^ { - 1 } }$ . Wie groß muss die magnetische Flussdichte sein, damit der Scheitelwert der induzierten Spannung 100V beträgt?
