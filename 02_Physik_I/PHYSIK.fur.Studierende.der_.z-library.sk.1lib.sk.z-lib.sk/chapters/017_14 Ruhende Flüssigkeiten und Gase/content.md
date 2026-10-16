# 14 Ruhende Flüssigkeiten und Gase

原始 PDF 第 147–158 页。

14

Ruhende Flüssigkeiten und Gase

## 14.1 Druck in Flüssigkeiten (hydrostatischer Druck)

Da Flüssigkeitsteilchen frei gegeneinander verschiebbar sind, verlagern sie sich bei Einwirkung äußerer Kräfte so, dass sich die Flüssigkeitsoberfläche stets senkrecht zur wirkenden Kraft einstellt (s. Beispiel 14.1). Zur Beschreibung der kräftemäßigen Beanspruchung einer Flüssigkeit (oder eines Gases) wird deshalb anstelle des Kraftvektors eine skalare Größe, der **Druck** p, benutzt, der als Quotient aus der in Richtung der Flächennormalen angreifenden, flächenhaft verteilten Kraft F und der Größe dieser Fläche A definiert ist:

$$
p = \frac {F}{A} \quad \text {bzw.} \quad p = \frac {\mathrm{d} F}{\mathrm{d} A} \quad (\mathbf {D r u c k}). \tag {14.1}
$$

Außerhalb des SI ist als allgemein anwendbare Druckeinheit auch das B a r (bar) zugelassen: 1bar = $1 0 ^ { 5 }$ Pa. Für den Blutdruck ist auch noch die Einheit 1mm $\mathbf { \nabla } \cdot \mathbf { H } \mathbf { g } = 1 3 3 , 3$ Pa zulässig.

Wird auf eine Flüssigkeit, die sich im Innern eines Gefäßes befindet, mittels eines belasteten Kolbens ein Druck $p = F / A$ ausgeübt (Bild 14.1), so breitet sich dieser in der Flüssigkeit allseitig in gleicher Stärke aus; es gilt der Satz von der allseitigen Gleichheit des hydrostatischen Drucks, das

**Gesetz von PASCAL: Überall im Innern einer Flüssigkeit sowie an der Gefäßwand ist, unabhängig von deren Neigung, der Druck gleich.**

![](../../raw/pages_0129-0160/images/page_146_image_8.jpg)

<details>
<summary>text_image</summary>

F
A
p
</details>

Bild 14.1 Kolbendruck

![](../../raw/pages_0129-0160/images/page_146_image_10.jpg)

<details>
<summary>text_image</summary>

F₁
A₁
p
F₂
A₂
p
</details>

Bild 14.2 Prinzip der Hydraulik

**Prinzip der Hydraulik** (Bild 14.2). Zwei Zylinder unterschiedlichen Querschnitts $A _ { 2 } > A _ { 1 }$ , die durch ein Rohr miteinander verbunden und mit Wasser oder Öl gefüllt sind, werden durch verschiebbare Kolben abgeschlossen. Greift am Kolben des engen Zylinders die Kraft $F _ { 1 }$ an, entsteht ein Druck $p = F _ { 1 } / A _ { 1 }$ , infolgedessen der Kolben des zweiten Zylinders gehoben wird. Da der Druck in beiden Zylindern gleich ist, also $p = F _ { 1 } / A _ { 1 } = F _ { 2 } / A _ { 2 }$ , folgt damit für die Kraft $F _ { 2 } = F _ { 1 } A _ { 2 } / A _ { 1 } ;$ d. h., die von diesem Kolben ausgeübte Kraft ist im Verhältnis der Kolbenquerschnitte größer.

---

14.2 Schweredruck. Auftrieb. Schwimmstabilität

145

**Kompressibilität.** Durch allseitigen (hydrostatischen) Druck wird das Volumen einer Flüssigkeit geringfügig verringert. Dabei zeigt sich, dass innerhalb gewisser Grenzen die relative Volumenänderung $\Delta V / V$ der Druckänderung $\Delta p$ proportional ist: $\Delta V / V = - \varkappa \Delta p$ . Das negative Vorzeichen ergibt sich daraus, dass einer Druckzunahme $( \Delta p > 0 )$ eine Volumenabnahme $( \Delta V < 0 )$ entspricht. Analog zu den Festkörpern (vgl. 13.2) folgt somit als Maß für die Zusammendrückbarkeit einer Flüssigkeit die Größe

$$
\varkappa = - \frac {1}{V} \frac {\Delta V}{\Delta p} \quad \text {bzw.} \quad \varkappa = - \frac {1}{V} \frac {\mathrm{d} V}{\mathrm{d} p} \quad (\text {Kompressibilität}). \tag {14.2}
$$

Die Kompressibilität von Flüssigkeiten ist temperaturabhängig und übersteigt die von festen Körpern um ein bis zwei Zehnerpotenzen. So z. B. ist sie bei Wasser ${ \bf \Phi } ( 2 0   ^ { \circ } \mathrm { C } ,$ niedrige Drücke) etwa $5 \cdot 1 0 ^ { - 1 0 }   \mathrm { P a } ^ { - 1 }$ und damit rund 100-mal größer als die von Stahl.

## Beispiel 14.1:

Eine Flüssigkeit, die sich in einem zylindrischen Gefäß befindet, wird in Rotation um die $\mathrm { Z y }$ linderachse versetzt. Die Flüssigkeitsoberfläche nimmt dadurch eine nach innen gewölbte rotationssymmetrische Form an. Durch welche mathematische Funktion wird das Oberflächenprofil in der Schnittfläche durch die Zylinderachse beschrieben?

![](../../raw/pages_0129-0160/images/page_147_image_7.jpg)

<details>
<summary>text_image</summary>

y
x
P
mω²x
α
mg
F
0
x
</details>

Bild 14.3 Rotationsparaboloid als Oberfläche einer rotierenden Flüssigkeit

Lösung: Da die resultierende Kraft aus Schwerkraft und Zentrifugalkraft stets senkrecht zur Flüssigkeitsoberfläche gerichtet ist, gilt für den Anstieg der Tangente im Punkt P von Bild 14.3:

$$
\frac {\mathrm{d} y}{\mathrm{d} x} = \tan \alpha = \frac {m \omega^ {2} x}{m g},
$$

woraus folgt:

$$
y = \frac {\omega^ {2}}{g} \int_ {0} ^ {x} x \mathrm{d} x = \frac {\omega^ {2}}{2 g} x ^ {2} \quad (\text {Parabel}).
$$

## 14.2 Schweredruck. Auftrieb. Schwimmstabilität

Als Schweredruck einer Flüssigkeit in der von der Flüssigkeitsoberfläche aus gemessenen Tiefe h (Niveauhöhe, Bild 14.4) bezeichnet man den Druck, der durch die Gewichtskraft der darüber liegenden Flüssigkeitssäule hervorgerufen wird. Bei inkompressiblen Flüssigkeiten ist die Dichte $\varrho$ unabhängig von der Tiefe. Die Gewichtskraft einer (prismatischen) Flüssigkeitssäule ist mit $A$ als Bodenfläche und $V = A h$ als deren Volumen

$$
G _ {\mathrm{Fl}} = m g = \varrho V g = \varrho A h g,
$$

---

146

14 Ruhende Flüssigkeiten und Gase

womit sich für den Druck ergibt

$$
p = \frac {G _ {\mathrm{Fl}}}{A} = \varrho g h \quad (\text {Schweredruck in einer Flüssigkeit}). \tag {14.3}
$$

Der Schweredruck wächst also proportional zur Niveauhöhe h (Bild 14.4) und ist dem PAS-CALschen Gesetz zufolge (vgl. Abschnitt 14.1) unabhängig von der Neigung der seitlichen Begrenzungsflächen des Gefäßes und damit von der Gefäßform. Daher sind die auf jeweils gleiche Bodenflächen A bei gleicher Flüssigkeitshöhe h ausgeübten Kräfte unabhängig von der Gefäßform gleich (hydrostatisches Paradoxon, Bild 14.5).

![](../../raw/pages_0129-0160/images/page_148_image_5.jpg)

<details>
<summary>text_image</summary>

h
0
p_h
p
h
</details>

Bild 14.4 Schweredruck in einer Flüssigkeit

![](../../raw/pages_0129-0160/images/page_148_image_7.jpg)

<details>
<summary>text_image</summary>

A
A
A
h
</details>

Bild 14.5 Hydrostatisches Paradoxon: Die Kräfte auf die Bodenflächen A sind gleich.

In einem offenen Behälter ist der Druck an einer bestimmten Messstelle der darin befindlichen Flüssigkeit gleich der Summe aus dem Schweredruck (14.3) und dem Druck der umgebenden Atmosphäre $p _ { 0 }$ (Luftdruck). Wenn die Flüssigkeit in einem geschlossenen Behälter unter einem Überdruck $p _ { \mathbf { \hat { u } } }$ gegenüber dem äußeren Luftdruck $p _ { 0 }$ steht (z. B. Kolbendruck), so ist der Gesamtdruck

$$
p = \varrho g h + p _ {0} + p _ {\ddot {\mathrm{u}}} \quad \text {(hydrostatischer Druck)}.
$$

Dabei ist $p$ der absolute Druck, d. h. gemessen vom absoluten Nulldruck, entsprechend 100% Vakuum.

Zur **Messung des atmosphärischen Luftdrucks** benutzte TORRICELLI (1643) eine einseitig geschlossene Glasröhre, welche mit Quecksilber $( \varrho = 1 3 , 5 4 6   \mathrm { g } / \mathrm { c m } ^ { 3 } )$ gefüllt und danach mit der Öffnung nach unten in ein Gefäß mit Quecksilber gebracht wurde (Quecksilberbarometer). Die Quecksilbersäule in der Röhre stellt sich dann in einer solchen Höhe h über dem Spiegel im Gefäß ein, dass ihr Schweredruck dem äußeren Luftdruck $p _ { 0 }$ das Gleichgewicht hält. Bei Normalluftdruck (vgl. Abschnitt 14.4) ist h ≈ 760mm und somit nach Gleichung (14.3) $p _ { 0 } \approx 1 . 0 1 \cdot 1 0 ^ { 5 } \mathrm { P a } = 1 0 1 0 \mathrm { h P a }$

**Auftrieb.** Taucht ein (prismatisch angenommener) Körper in eine Flüssigkeit völlig ein (Bild 14.6), dann wirken auf seine Begrenzungsflächen Kräfte, die dem jeweils herrschenden Schweredruck zuzuschreiben sind. Die Kräfte auf die Seitenflächen kompensieren sich. Die Differenz der Kräfte auf Grund- und Deckfläche ist mit (14.3)

$$
F _ {\mathrm{A}} = F _ {2} - F _ {1} = (p _ {2} - p _ {1}) A = \varrho_ {\mathrm{Fl}} g (h _ {2} - h _ {1}) A = \varrho_ {\mathrm{Fl}} V g = m _ {\mathrm{Fl}} g,
$$

wobei $\varrho _ { \mathrm { F I } }$ die Dichte der Flüssigkeit, V das Volumen des Körpers und $\varrho _ { \mathrm { F l } } V = m _ { \mathrm { F l } }$ somit die Masse der vom Körper verdrängten Flüssigkeit ist. Die resultierende, nach oben gerichtete Kraft ist damit

$$
F _ {\mathrm{A}} = \varrho_ {\mathrm{Fl}} V g = m _ {\mathrm{Fl}} g = G _ {\mathrm{Fl}} \quad (\text {Auftriebskraft}). \tag {14.4}
$$

---

14.2 Schweredruck. Auftrieb. Schwimmstabilität

147

![](../../raw/pages_0129-0160/images/page_149_image_2.jpg)

<details>
<summary>text_image</summary>

F₁
h₁
h₂
A
F₂
</details>

Bild 14.6 Auftrieb als Folge der Druckdifferenz zwischen Bodenund Deckfläche des Körpers

## ARCHIMEDisches Prinzip:

**Die Auftriebskraft ist gleich der Gewichtskraft des vom Körper verdrängten Flüssigkeitsvolumens.**

Ist die Auftriebskraft eines vollständig eingetauchten Körpers größer als dessen Gewichtskraft $G ,$ so taucht er so weit auf, bis G gleich der Gewichtskraft der verdrängten Flüssigkeit $G _ { \mathrm { F I } }$ ist; der Körper **schwimmt**. Ist $F _ { \mathrm { A } } = G ,$ so **schwebt** der Körper, ist $F _ { \mathrm { A } } < G ,$ **sinkt** er zu Boden.

Der durch den Auftrieb verursachte scheinbare Gewichtsverlust eines Tauchkörpers kann zur Bestimmung der Dichte einer Flüssigkeit benutzt werden (MOHRsche Waage, vgl. das nachfolgende Beispiel 14.2/3, Aräometer). Andererseits lässt sich bei bekannter Dichte der Flüssigkeit aus dem Auftrieb das Volumen eines unregelmäßig geformten Körpers und daraus mittels Wä- gung dessen Dichte ermitteln (hydrostatische Waage, vgl. das nachfolgende Beispiel 14.2/2).

Für den Auftrieb in Gasen gilt Gleichung (14.4) sinngemäß. Hingegen gilt für den Schweredruck eines Gases nicht die lineare Abhängigkeit (14.3) von der Höhe h (vgl. 14.4).

**Stabilität beim Schwimmen.** Der Angriffspunkt der Schwerkraft ist der Schwerpunkt S eines schwimmenden Körpers, der Angriffspunkt der Auftriebskraft dagegen der Schwerpunkt der verdrängten Flüssigkeit $S _ { \mathrm { { H } } }$ . In der Gleichgewichtslage (Bild 14.7a) fallen die Wirkungslinien der beiden Kräfte zusammen, das resultierende Drehmoment des Kräftepaares ist null. Bei Stö- rung des Gleichgewichts erzeugt das Kräftepaar ein Drehmoment $M = \boldsymbol{r} \times \boldsymbol{F}_{\mathrm{A}}$ (r Vektor von S nach $S _ { \mathrm { F l } } )$ , das den Körper in die Gleichgewichtslage zurückdreht (aufrichtet) oder aus ihr entfernt (kippt), je nachdem, ob der Auftriebsvektor die Mittelebene des Körpers oberhalb oder unterhalb des Schwerpunkts S schneidet (Bild 14.7b und c). Im ersten Fall ist die Schwimmlage stabil, im zweiten instabil. Der Schnittpunkt M des Auftriebsvektors mit der Mittelebene heißt Metazentrum.

![](../../raw/pages_0129-0160/images/page_149_image_10.jpg)

<details>
<summary>text_image</summary>

a)
b)
c)
</details>

Bild 14.7 Stabilität eines schwimmenden Körpers (M Metazentrum)

---

148

14 Ruhende Flüssigkeiten und Gase

## Beispiele 14.2:

1. Ein Ballon mit einem Volumen von $5 0 0 \mathrm { m } ^ { 3 }$ soll eine Masse von 250kg tragen. Welche Dichte muss das Füllgas haben? Dichte der Luft bei $15^{\circ}C:\varrho_{ L }=1,23 kg/m ^3$

Lösung: Die Tragkraft eines Ballons ist gleich der Gewichtskraft der verdrängten Luft (Auftriebskraft) abzüglich der Gewichtskraft des Füllgases, also $F = ( \varrho _ { \mathrm { L } } - \varrho _ { \mathrm { G a s } } ) g V = m g .$ . Hieraus erhält man $\varrho_{\mathrm{Gas}} = \varrho_{\mathrm{L}} - (m/V) = 0.73   \mathrm{kg/m^3}$ (Maximalwert), z. B. heiße Luft von rund $3 2 0   ^ { \circ } \mathbf { C }$ mit $\varrho \approx 0 . 6   \mathrm { k g / m ^ { 3 } }$

2. Zur Bestimmung der Dichte eines festen Körpers mittels der hydrostatischen Waage wird der Körper einmal in Luft gewogen (Masse m) und ein zweites Mal nach Einhängen in eine Flüssigkeit bekannter Dichte ϱ<sub>Fl</sub> (scheinbare Masse $m ^ { \prime } )$ . Berechne aus $m ,$ $m ^ { \prime }$ und $\varrho _ { \mathrm { F I } }$ die Dichte des Körpers ϱ<sub>K</sub>!

Lösung: Der Gewichtsverlust des Körpers in der Flüssigkeit ist gleich der Auftriebskraft, also $( m - m ^ { \prime } ) g = \varrho _ { \mathrm { F l } } V g$ , woraus mit $V = m / \varrho _ { \mathrm { K } }$ folgt $\varrho _ { \mathrm { K } } = \varrho _ { \mathrm { F l } } m / ( m - m ^ { \prime } )$

3. Die Bestimmung der Dichte einer Flüssigkeit kann auf gleiche Weise wie in Beispiel 14.2/2 erfolgen, wenn anstelle des festen Körpers ein Tauchkörper (kleines verschlossenes Glasgefäß) verwendet wird, welcher mit der Flüssigkeit von unbekannter Dichte $\varrho _ { \mathrm { F I } }$ voll gefüllt wird (MOHRsche Waage). Da die Masse des leeren Tauchkörpers bekannt ist, kann aus m und $m ^ { \prime }$ für dessen Inhalt nach o. g. Beziehung die Dichte $\varrho _ { \mathrm { F I } }$ bestimmt werden.

4. In Beispiel 14.2/2 zur Dichtebestimmung eines festen Körpers wurde bei der Wägung der Auftrieb des Körpers in der Luft (bei Verwendung einer Balkenwaage auch derjenige der Wä- gestücke) vernachlässigt. Eine genauere Messung unter Berücksichtigung des Luftauftriebs ist mit dem **Pyknometer** (Glasgefäß) möglich: Mit einer Zweischalen-Balkenwaage werden drei Wägungen durchgeführt, mit denen 1. die scheinbare Masse (in Luft) des Körpers $m ^ { \prime } ,$ 2. des vollständig mit Wasser (Dichte $\varrho_{\mathrm{W}} = 0,9982   \mathrm{g} / \mathrm{cm}^{3}$ bei $2 0   ^ { \circ } \mathrm { C } )$ gefüllten Pyknometers $m _ { 1 } ^ { \prime } , 3$ . des mit dem Körper gefüllten und mit Wasser wieder vollständig aufgefüllten Pyknometers $m _ { 2 } ^ { \prime }$ ermittelt wird. Aus drei Gleichungen, mit denen jeweils ein Gleichgewicht zwischen den scheinbaren Massen von Gegenständen auf der einen und Wägestücken auf der anderen Waagschale hergestellt wird, erhält man als Dichte des untersuchten Körpers

$$
\varrho = \frac {m ^ {\prime} \varrho_ {\mathrm{W}} - (m _ {2} ^ {\prime} - m _ {1} ^ {\prime}) \varrho_ {\mathrm{L}}}{m ^ {\prime} - (m _ {2} ^ {\prime} - m _ {1} ^ {\prime})} \quad (\varrho_ {\mathrm{L}} \text {Dichte der Luft bei} 2 0 ° \mathrm{C} = 1, 2 0 5 \cdot 1 0 ^ {- 3} \mathrm{g/cm} ^ {3}).
$$

Bei der ersten Messung zeigt die Waage anhand der aufgelegten Wägestücke $m ^ { \prime } = 5 { , } 6 7 1   \mathrm { g } ,$ bei der zweiten Messung $m _ { 1 } ^ { \prime } = 1 8 0 { , } 1 1 9$ g und bei der dritten Messung $m_{2}^{\prime}=182,060  g an$ . Damit erhält man $\varrho = 1 , 5 1 7   \mathrm { g } / \mathrm { c m } ^ { 3 }$ □

## Aufgaben

**14.1** Etwa zeitgleich mit der Erfindung des Quecksilberbarometers durch TORRICELLI baute der Magdeburger Bürgermeister OTTO VON GUERICKE zur Messung des Luftdrucks ein Wasserbarometer. Welche Höhe hat dessen Wassersäule?
**14.2** Wenn man von der Erdoberfläche aus um 30m emporsteigt, verringert sich der Luftdruck um etwa 4hPa. Welcher Wert für die Dichte der Luft folgt hieraus?
**14.3** Der aus dem Wasser ragende Teil eines Eisberges hat das Volumen $V _ { 0 } = 1 0 ^ { 4 }   \mathrm { m } ^ { 3 }$ . Wie viel Prozent des Gesamtvolumens V des Eisberges befinden sich unter Wasser, und wie groß ist die Masse des Eisberges? Dichte des Eises $\varrho_{\mathrm{E}} = 0.93 \cdot 10^{3}   \mathrm{kg/m^{3}};$ Dichte des Meerwassers $\rho_{\mathrm{M}}=1,03 \cdot 10^{3} \mathrm{~kg} / \mathrm{m}^{3}$

---

14.3 Druck in Gasen. Zusammenhang zwischen Druck, Volumen und Dichte

149

## 14.3 Druck in Gasen. Zusammenhang zwischen Druck, Volumen und Dichte

Der Druck der Gase auf die Gefäßwandung ist, wie in Abschnitt 18.2 näher untersucht wird, die Folge der Wärmebewegung der Gasmoleküle und der damit verbundenen elastischen Stö- $\beta e$ derselben gegen die Wand. Aus dieser einfachen Vorstellung heraus lässt sich eine Aussage über den Zusammenhang zwischen Druck und Volumen eines Gases leicht gewinnen: Im selben Verhältnis, wie das Volumen des Gases verringert wird, muss – da die Gesamtzahl der Moleküle erhalten bleibt – bei gleich bleibender Temperatur die Stoßzahl je Flächen- und Zeiteinheit und damit der Gasdruck anwachsen. Durch das Experiment wird diese Überlegung vollauf bestätigt: Wird ein Gas vom Ausgangsvolumen $V _ { 0 }$ auf das Volumen $V = V _ { 0 } / 2$ zusammengedrückt, so steigt der mittels eines an das Gefäß angeschlossenen Manometers gemessene Gasdruck von seinem ursprünglichen Wert $p _ { 0 }$ auf den Wert $p = 2 p _ { 0 }$ an. Bei Kompression auf ein Drittel des Ausgangsvolumens wächst der Druck auf das Dreifache usw. Druck und Volumen eines Gases sind einander umgekehrt proportional. Es gilt somit das

## Gesetz von BOYLE-MARIOTTE:

**Das Produkt aus Druck und Volumen eines Gases ergibt bei gleich bleibender Temperatur stets den gleichen Wert.**

$$
p V = p _ {0} V _ {0} \quad \text {oder} \quad p V = \text {const.} \tag {14.5}
$$

Der Wert der Konstante hängt von der Temperatur und von der Gasmenge ab. Der Beweis für dieses Gesetz, welches streng nur für das ideale Gas (vernachlässigbares Eigenvolumen der Gasmoleküle, keine Anziehungskräfte zwischen den Molekülen) gilt, wird später auf der Grundlage der kinetischen Gastheorie gegeben (vgl. 18.2).

Mit der Dichte des Gases $\varrho = m / V$ folgt aus (14.5) $p m / \varrho = p _ { 0 } m / \varrho _ { 0 }$ . Da die Masse des Gases unverändert bleibt, erhält man

$$
\frac {p}{p _ {0}} = \frac {\varrho}{\varrho_ {0}} \quad \text {oder} \quad \frac {p}{\varrho} = \text {const.} \tag {14.6}
$$

## Der Druck und die Dichte eines Gases sind bei konstanter Temperatur einander proportional.

Die Kompressibilität $\varkappa$ eines idealen Gases bei konstanter Temperatur berechnet sich nach (14.2) mit (14.5)

$$
V = \frac {\mathrm{const}}{p} \quad \text {und} \quad \frac {\mathrm{d} V}{\mathrm{d} p} = - \frac {\mathrm{const}}{p ^ {2}} = - \frac {V}{p}
$$

zu

$$
\varkappa = - \frac {1}{V} \frac {\mathrm{d} V}{\mathrm{d} p} = \frac {1}{p} \quad (\text {isothermeKompressibilitat des idealen Gases}). \tag {14.7}
$$

Die isotherme Kompressibilität eines idealen Gases ist also gleich dem reziproken Wert seines Drucks; sie ist somit für alle idealen Gase gleichen Drucks gleich.

---

150

14 Ruhende Flüssigkeiten und Gase

Zur **Druckmessung** in Gasen benutzt man vorzugsweise Flüssigkeitsmanometer (U-Rohr-Manometer) in offener oder geschlossener Form (Bild 14.8). Der eine Schenkel ist an das Gasgefäß angeschlossen, in dem der zu messende Druck $p _ { 1 }$ herrscht. Ist der andere Schenkel offen, so wird durch die Höhe der Flüssigkeitssäule h die Druckdifferenz $p _ { 1 } - p _ { 2 }$ gegen den atmosphä- rischen Luftdruck $p _ { 2 }$ gemessen. Im geschlossenen Manometer wird durch h unmittelbar der Gasdruck $p _ { 1 }$ gemessen. Die Skalenteilung ist beim geschlossenen Manometer nicht linear, da die Luft im geschlossenen Schenkel mit steigendem Druck zunehmend komprimiert wird und dabei ihre Kompressibilität nach (14.7) immer mehr abnimmt.

![](../../raw/pages_0129-0160/images/page_152_image_3.jpg)

Bild 14.8 a) Offenes, b) geschlossenes Flüssigkeitsmanometer

## Beispiel 14.3:

Eine Sauerstoffflasche von 40 Litern steht gegenüber dem äußeren Luftdruck von 1000hPa unter einem Überdruck von 2,5MPa. Wie viel Sauerstoff entweicht beim Öffnen der Flasche?

Lösung: Der Druck in der Flasche ist gleich der Summe aus Überdruck und Luftdruck, also $p_{1} = (2,5 + 0,1)  MPa  = 2,6  MPa$ . Nach dem Entweichen steht das Gas unter dem Luftdruck $p _ { 2 } =$ 0,1MPa und hat nach (14.5) das Volumen $V _ { 2 } = p _ { 1 } V _ { 1 } / p _ { 2 } = 1 0 4 0 \mathrm { l }$ . Da das Volumen $V _ { 1 } = 4 0 1$ i n der Flasche zurückbleibt, entweichen also 1000l. □

## Aufgabe

**14.4** Auf welchen Bruchteil verringert sich im obigen Beispiel 14.3 die Dichte des Sauerstoffs beim Entspannen?

## 14.4 Schweredruck in Gasen. Barometrische Höhenformel

Der atmosphärische **Luftdruck** ergibt sich wie der Schweredruck bei den Flüssigkeiten aus der Gewichtskraft der über dem Erdboden ruhenden Luftsäule. Seine Berechnung kann jedoch nicht nach der entsprechenden Beziehung (14.3) $p = \varrho g h$ erfolgen, da wegen der im Vergleich zu den Flüssigkeiten großen Kompressibilität der Luft deren Dichte mit zunehmender Bodennähe stetig anwächst. Die obige Beziehung kann daher nur auf eine geringe Höhendifferenz dh angewandt werden, innerhalb der die Dichte $\varrho$ näherungsweise als konstant angesehen werden darf. Einer Höhenabnahme −dh entspricht dann eine Druckzunahme der Größe

$$
\mathrm{d} p = - \varrho g \mathrm{d} h.
$$

Sind $p$ und $\varrho$ Druck und Dichte in der Höhe h und $p _ { 0 }$ und $\varrho _ { 0 }$ Druck und Dichte in Meeresspiegelhöhe $( h = 0 )$ , so folgt (konstante Temperatur in jeder Höhe vorausgesetzt) mit (14.6)

---

14.4 Schweredruck in Gasen. Barometrische Höhenformel

151

$\varrho = \varrho _ { 0 } p / p _ { 0 }$ aus obiger Gleichung nach Umstellung und anschließender Integration

$$
\int_ {p _ {0}} ^ {p} \frac {\mathrm{d} p}{p} = - \frac {\varrho_ {0} g}{p _ {0}} \int_ {0} ^ {h} \mathrm{d} h, \quad \ln \frac {p}{p _ {0}} = - \frac {\varrho_ {0} g h}{p _ {0}}, \tag {14.8}
$$

$$
p = p _ {0} \mathrm{e} ^ {- \frac {\varrho_ {0} g h}{p _ {0}}} \quad \begin{array}{l} (\text {barometrische Höhenformel bei} \\ \text {konstantem Temperaturverlauf}). \end{array} \tag {14.9}
$$

Man erkennt hieraus, dass der Schweredruck p eines Gases (unter Voraussetzung gleicher Temperatur in allen Höhen) mit zunehmender Höhe h exponentiell abfällt (Bild 14.9), im Gegensatz zu einer Flüssigkeit mit einem linearen Abfall (vgl. Bild 14.4). Es lässt sich daher keine scharfe Grenze für die Atmosphäre angeben.

![](../../raw/pages_0129-0160/images/page_153_chart_6.jpg)

<details>
<summary>line</summary>

| h | p |
| --- | --- |
| 0 | \(p_{0}\) |
| \(h_{1}/_{2}\) | \(p_{0}/2\) |
| \(2h_{1}/_{2}\) | \(p_{0}/4\) |
| \(3h_{1}/_{2}\) | \(p_{0}/8\) |
| \(4h_{1}/_{2}\) | \(p_{0}/8\) |
</details>

Bild 14.9 Abfall des atmosphärischen Drucks mit zunehmender Höhe h entsprechend der barometrischen Höhenformel (14.9); $h _ { 1 / 2 } = 5 { , } 5 4$ km („Halbwertshöhe“)

In der barometrischen Höhenformel (14.9) erhält man im Exponenten mit

$$
p _ {0} = 1, 0 1 3   2 5 \cdot 1 0 ^ {5}   \mathrm{Pa} = 1 0 1 3, 2 5   \mathrm{hPa} \quad \text {(Normalluftdruck)} \tag {14.10}
$$

und der in Bodennähe bei $0   ^ { \circ } \mathbf { C }$ herrschenden Luftdichte $\varrho_{0}=1,293   kg/m ^{3}$ den Zahlenwert $\varrho _ { 0 } g / p _ { 0 } = 1 { , } 2 5 2 \cdot 1 0 ^ { - 4 }   \mathrm { m } ^ { - 1 }$ . Für $p = p _ { 0 } / 2$ folgt damit aus Gleichung (14.8) für die sog. Halb**wertshöhe** $h _ { 1 / 2 } = \ln 2 / ( \varrho _ { 0 } g / p _ { 0 } ) = 0 , 6 9 3 2 / ( 1 , 2 5 2 \cdot 1 0 ^ { - 4 }   \mathrm { m } ^ { - 1 } ) = 5 , 5 4   \mathrm { k m }$ , was bedeutet, dass – entsprechend einer Eigenart der Exponentialfunktion – der Luftdruck nach jeweils 5,54km Höhenzuwachs auf die Hälfte des vorangegangenen Wertes abfällt (vgl. Bild 14.9).

Die Wirkung des Luftdrucks in der Atmosphäre wurde erstmals 1657 in eindrucksvoller Weise durch OTTO VON GUERICKE mit seinen „Magdeburger Halbkugeln“ demonstriert (Bild 14.10): Zwei Halbkugelschalen aus Kupfer, deren Durchmesser 60cm betrug, wurden unter Zwischenlegen eines Lederringes luftdicht aneinander gelegt und mittels der ebenfalls von GUERICKE erfundenen Vakuum-Luftpumpe nahezu luftleer gepumpt. Der nur noch von außen wirkende Luftdruck presst die Halbkugeln mit der Kraft $F = p _ { 0 } \pi r ^ { 2 } \approx 1 0 ^ { 5 }   \mathrm { P a }   \cdot   3 , 1 4   \cdot   ( 3 0   \cdot   1 0 ^ { - 2 }   \mathrm { m } ) ^ { 2 } \approx 2 8   3 0 0   \mathrm { N }$ zusammen. Je 8 Pferde zu beiden Seiten waren nicht in der Lage, die Halbkugeln voneinander zu trennen.

![](../../raw/pages_0129-0160/images/page_153_image_12.jpg)

<details>
<summary>natural_image</summary>

Illustration of horse-drawn carriage with riders and figures on a banner (no text or symbols)
</details>

Bild 14.10 Historisches Experiment Otto von Guerickes zur Demonstration des Luftdrucks, in neuerer Zeit mehrfach wiederholt in Regie der Otto-von-Guericke-Gesellschaft e. V. zu Magdeburg

---

152

14 Ruhende Flüssigkeiten und Gase

## Beispiel 14.4:

Wie groß ist das Volumen V eines Ballons in 15km Höhe, wenn seine Gasfüllung in Meereshöhe das Volumen $V _ { 0 }$ hat? Temperatur- und andere Nebeneinflüsse seien vernachlässigt.

Lösung: Die Drücke $p _ { 0 }$ in Meereshöhe und $p$ in 15km Höhe sind für das Füllgas und die Luft gleich. Nach (14.5) ist $p / p _ { 0 } = V _ { 0 } / V$ , womit aus (14.9) mit $\varrho _ { 0 } g / p _ { 0 } = 1 { , } 2 5 2 \cdot 1 0 ^ { - 4 }   \mathrm { m } ^ { - 1 }$ (s. o.) folgt $V _ { 0 } / V = \mathbf { e } ^ { - \varrho _ { 0 } g h / p _ { 0 } } = 0 { , } 1 5 3 ;$ also $V = 6 { , } 5 4 V _ { 0 }$ □

## 14.5 Erscheinungen an Grenzflächen. Kohäsion und Adhäsion

Am Zustandekommen der bisher besprochenen Eigenschaften von Flüssigkeiten und Gasen ist die Gesamtheit aller Teilchen eines stofflich in sich homogenen Systems, einer sog. **Phase**, beteiligt. Liegen mehrere Phasen nebeneinander vor (z. B. der ungelöste feste Bodenkörper und seine flüssige Lösung; die in einer Emulsion schwebenden Öltröpfchen und die Grundflüssigkeit; die einzelnen kristallinen Bestandteile einer Legierung), so berühren sie sich in den Phasengrenzen. Grenzflächen flüssiger und fester Körper gegenüber der Gasphase bezeichnet man schlechthin als Oberflächen.

Zwischen den Molekülen einer Phase bestehen Anziehungskräfte, die **Kohäsionskräfte**, die bei den festen Körpern vor allem deren Festigkeitseigenschaften bestimmen. Eine geringe Kohä- sion besteht auch zwischen den Molekülen der Gase, wodurch der Unterschied zwischen dem idealen Gas, bei dem diese Kräfte fehlen, und dem realen Gas bedingt ist.

An der Grenzfläche zweier verschiedener Phasen treten ebenfalls zwischenmolekulare Kräfte, die **Adhäsionskräfte**, auf. Sie bewirken das Aneinanderhaften verschiedener Körper. Die Adhäsion ist die Ursache der Benetzung, der Ausbreitung eines Tropfens auf der Oberfläche einer anderen Flüssigkeit, des Anhaftens von Kreide usw. Alle diese Erscheinungen sind auf das Verhalten der in unmittelbarer Nähe der Grenzfläche befindlichen Moleküle zurückzuführen.

## 14.6 Spezifische Oberflächenenergie, Oberflächenspannung

Zwischen den Molekülen einer Flüssigkeit wirken Kohäsionskräfte, die einen begrenzten Wirkungsbereich haben. Im Innern der Flüssigkeit heben sich die auf ein Molekül wirkenden Kräfte gegenseitig auf, weil es dort allseitig von gleichartigen Molekülen umgeben ist. An der Oberfläche dagegen fehlt eine nach außen gerichtete Anziehungskraft (bzw. es wirken dort lediglich die wesentlich schwächeren Kräfte der Moleküle des angrenzenden Gases), so dass innerhalb einer dünnen Oberflächenschicht, deren Dicke gleich der molekularen Wirkungssphäre (ungefähr $1 0 ^ { - 8 } \mathrm { m ) }$ ist, an den Molekülen eine senkrecht ins Innere der Flüssigkeit gerichtete resultierende Kraft angreift (Bild 14.11). Diese Kraft wird, auf die Flächeneinheit bezogen, Binnendruck oder Kohäsionsdruck genannt.

Um die Oberfläche einer Flüssigkeit zu vergrößern, müssen Moleküle aus deren Innern an die Oberfläche gebracht werden. Dazu muss Arbeit gegen den Kohäsionsdruck verrichtet werden. Die Moleküle an der Flüssigkeitsoberfläche haben daher potenzielle Energie (Oberflächenener-$g i e )$ . Die gesamte Zunahme der Oberflächenenergie $\Delta E$ ist der Oberflächenvergrößerung $\Delta A$ proportional:

$$
\Delta E = \sigma \Delta A. \tag {14.11}
$$

---

14.6 Spezifische Oberflächenenergie, Oberflächenspannung

153

$\sigma = \Delta E / \Delta A$ ist die **spezifische Oberflächenenergie**. Da ein System immer bestrebt ist, den stabilen Gleichgewichtszustand kleinster potenzieller Energie einzunehmen, sind Flüssigkeitsoberflächen stets Minimalflächen. Flüssigkeitstropfen oder Gasbläschen nehmen von selbst Kugelgestalt an, da die Kugel unter allen Körpern gleichen Volumens die kleinste Oberfläche hat. Flüssigkeitsoberflächen verhalten sich ähnlich wie gespannte Gummimembranen.

![](../../raw/pages_0129-0160/images/page_155_image_3.jpg)

<details>
<summary>natural_image</summary>

Grid of circles with directional arrows and a central cross symbol (no text or labels)
</details>

Bild 14.11 Modell zur Deutung der Oberflächenenergie

![](../../raw/pages_0129-0160/images/page_155_image_5.jpg)

<details>
<summary>natural_image</summary>

3D wireframe diagram of a hemispherical surface with directional arrows indicating flow or force (no text or symbols)
</details>

Bild 14.12 Zur Erklärung der Oberflächenspannung

An jeder Begrenzungslinie einer Flüssigkeitsoberfläche (oder eines Teilstücks von ihr) greifen Kräfte tangential zur Oberfläche an, die senkrecht auf der Begrenzungslinie stehen und ins Innere des Oberflächenstücks gerichtet sind (Bild 14.12). Zur Verschiebung eines Stücks der Begrenzungslinie von der Länge l um ds, d. h. zur Vergrößerung des Oberflächenstücks um d $A = l \mathbf { d } s$ , ist eine Arbeit d $W = F$ ds gegen diese Kräfte zu verrichten. Die Oberflächenenergie steigt um d $E = \mathbf { d } W$ , und es ist nach (14.11)

$$
\sigma = \frac {\mathrm{d} W}{\mathrm{d} A} = \frac {F \mathrm{d} s}{l \mathrm{d} s} = \frac {F}{l} \quad \begin{array}{l} (\text {spezifische Oberflächenenergie,} \\ \text {Oberflächenspannung).} \end{array} \tag {14.12}
$$

Die spezifische Oberflächenenergie σ ist somit gleich dem auf die Längeneinheit der Begrenzungslinie bezogenen Betrag der Oberflächenkraft. σ wird daher auch als **Oberflächenspannung** bezeichnet.

Die Messung der Oberflächenspannung σ kann mittels der **Bügelmethode** (Bild 14.13) erfolgen: Man zieht den Drahtbügel mit dem quer gespannten Messdraht AB der Länge l aus der Oberfläche der in einem Schälchen befindlichen Flüssigkeit heraus, wobei die Flüssigkeitslamelle ABC D hochgezogen wird. Aus der mit Hilfe einer Federwaage gemessenen Kraft F, bei der die Lamelle reißt, und aus der Randlänge 2l (Vorder- und Rückseite des Messdrahtes) kann nach (14.12) die Oberflächenspannung zu $\sigma = F / ( 2 l )$ bestimmt werden.

![](../../raw/pages_0129-0160/images/page_155_image_11.jpg)

<details>
<summary>text_image</summary>

F
A l B
D C
</details>

Bild 14.13 Bügelmethode zur Messung der Oberflächenspannung σ ABC D: Aus der Flüssigkeitsoberfläche DC am Messdraht AB hochgezogene Flüssigkeitslamelle; F = zu messende Abreißkraft der Lamelle

**Druck in der Seifenblase. Kohäsionsdruck.** Die bei einer Änderung des Radius r einer Seifenblase (Oberfläche $A = 4 \pi r ^ { 2 } )$ um ∆r verrichtete Arbeit ist $\Delta W = F \Delta r = 4 \pi r ^ { 2 } \Delta p \Delta r$ , wobei $\Delta p = p _ { \mathrm { i } } - p _ { \mathrm { a } }$ der Überdruck in der Blase $( p _ { \mathrm { i } }$ Innendruck) gegenüber dem Außendruck $p _ { \mathrm { a } }$ ist. Aus Gleichgewichtsgründen muss diese Arbeit gleich der Änderung der Oberflächenenergie infolge Vergrößerung der zwei Oberflächen (innen und außen) sein. Mit $\Delta A = 8 \pi r \Delta r$ (dies folgt durch Differenziation aus $\left[ A = 4 \pi r ^ { 2 } \right)$ ist also nach (14.11) $\Delta W = 2 \sigma \cdot 8 \pi r \Delta r$ . Durch Gleichsetzen beider Ausdrücke für $\Delta W$ erhält man

$$
\Delta p = \frac {4 \sigma}{r} \quad (\text {Überdruck in der Seifenblase}). \tag {14.13}
$$

---

154

14 Ruhende Flüssigkeiten und Gase

Infolge der Oberflächenkräfte herrscht also in einer nach außen konvexen (bzw. konkaven) Flüssigkeitsoberfläche von Kugelgestalt gegenüber dem Außendruck der in das Innere (bzw. nach außen) gerichtete Überdruck

$$
\Delta p = \frac {2 \sigma}{r} \quad (\text {Kohäsionsdruck}). \tag {14.14}
$$

Ein solcher Überdruck herrscht z. B. im Innern eines kugelförmigen Flüssigkeitstropfens.

## 14.7 Benetzung und Kapillarwirkung

Sind in einer Grenzschicht Festkörper/Flüssigkeit die Adhäsionskräfte zwischen den Molekü- len des Festkörpers und der Flüssigkeit sehr viel größer als die Kohäsionskräfte zwischen den Flüssigkeitsmolekülen, so breitet sich die Flüssigkeit auf der Oberfläche des festen Körpers aus (vollkommene Benetzung), im anderen Fall, wenn die Kohäsionkräfte überwiegen, zieht sie sich zu mehr oder weniger flachen Tropfen zusammen (unvollkommene Benetzung, Bild 14.14). In jeder Grenzfläche herrscht eine **Grenzflächenspannung** $\sigma _ { i j }$ , auch in der Grenze zwischen Festkörper und Gasphase. Die Indizes i, j = 1, 2, 3 bezeichnen die beiden in Kontakt stehenden Phasen. Im Gleichgewicht muss die Summe der Horizontalkomponenten von $\sigma _ { 1 3 } , \sigma _ { 1 2 }$ und $\sigma _ { 2 3 }$ verschwinden, und es stellt sich zwischen Flüssigkeitsoberfläche und fester Unterlage ein bestimmter **Randwinkel** ϑ ein. Es gilt dann für die **Haftspannung** $\sigma _ { 1 3 } - \sigma _ { 2 3 } \colon$

$$
\sigma_ {1 3} - \sigma_ {2 3} = \sigma_ {1 2} \cos \vartheta \quad (\text {Kapillaritätsgesetz}). \tag {14.15}
$$

Die Grenzflächenspannungen gegenüber dem festen Körper $\sigma _ { 1 3 }$ und $\sigma _ { 2 3 }$ lassen sich einzeln nicht messen, wohl aber der Randwinkel ϑ und die Oberflächenspannung $\sigma _ { 1 2 }$

Die gleichen Verhältnisse wie beim Flüssigkeitstropfen finden wir beim Hochziehen bzw. Herabdrücken einer Flüssigkeit an einer Wand vor. Die Flüssigkeit benetzt die Wand wie in Bild 14.14a und 14.15a, wenn $0 ^ { \circ } \leq \vartheta \leq 9 0 ^ { \circ }$ ist. Im Grenzfall vollständiger Benetzung $( \vartheta = 0 ^ { \circ } ,   \mathrm { z . B . }$ im Fall Wasser an Glas) bedeckt eine Flüssigkeitsschicht die gesamte feste Oberfläche. Für $9 0 ^ { \circ } < \vartheta \leq 1 8 0 ^ { \circ }$ wird die Wand nicht benetzt, entsprechend Bild 14.14b und 14.15b.

Die Benetzungserscheinungen sind ursächlich wichtig für die Wirkung der Waschmittel, der Schwimmaufbereitung von Erzen, der Herstellung von Emulsionen u. a.

![](../../raw/pages_0129-0160/images/page_156_image_11.jpg)

Bild 14.14 Flüssigkeitstropfen auf fester Unterlage: a) unvollkommene Benetzung; b) keine Benetzung

**Kapillare Steighöhe.** In engen Röhren (Haarröhrchen, Kapillaren) mit dem Radius r steigt im Fall $\vartheta   <   9 0 ^ { \circ }$ eine Flüssigkeit bis zu einer bestimmten Höhe h, und es bildet sich eine nach unten gewölbte Flüssigkeitsoberfläche, ein konkaver Meniskus (Bild 14.15a). Diese Erscheinung heißt kapillare Hebung oder Kapillaraszension. Hier halten sich die von der Oberflächenspannung

---

14.7 Benetzung und Kapillarwirkung

155

![](../../raw/pages_0129-0160/images/page_157_image_2.jpg)

Bild 14.15 a) Kapillare Hebung (Kapillaraszension) benetzender Flüssigkeiten; b) kapillare Senkung (Kapillardepression) nichtbenetzender Flüssigkeiten

σ bewirkte, am Umfang des Meniskus (Länge $l = 2 \pi r )$ angreifende Kraft (14.12) $F = \sigma l = 2 \pi r \sigma$ und das Gewicht der angehobenen Flüssigkeitssäule $G = m _ { \mathrm { F l } } g = \varrho V g = \varrho \pi r ^ { 2 } h g$ das Gleichgewicht. Durch Gleichsetzen folgt für die Steighöhe $h = 2 \sigma / ( \varrho g r )$ . Diese Beziehung ergibt sich auch aus der Forderung, dass der Kohäsionsdruck (14.14) des kugelförmig angenommenen Meniskus gleich dem Schweredruck (14.3) sein muss:

$$
2 \sigma / r = \varrho g h \quad \text { oder } \quad h = 2 \sigma / (\varrho g r).
$$

Bei nicht vollständiger Benetzung ist die Steighöhe h vom Randwinkel ϑ abhängig. Man erhält, wenn in obiger Beziehung für die Oberflächenspannung σ, welche mit $\sigma _ { 1 2 }$ in Bild 14.14a identisch ist, die wahre Haftspannung gemäß Gleichung (14.15) σcosϑ gesetzt wird:

$$
h = \frac {2 \sigma \cos \vartheta}{\varrho g r} \quad (\text {kapillare Steighöhe}). \tag {14.16}
$$

Hieraus geht hervor, dass bei nichtbenetzenden Flüssigkeiten (z. B. Quecksilber), bei denen ϑ ein stumpfer Winkel ist, wegen cos $\vartheta < 0$ eine negative Steighöhe auftritt, entsprechend einer Absenkung des Meniskus. Die Flüssigkeit steht dann in der Kapillare niedriger als im übrigen Niveau, und der Meniskus ist im Gegensatz zur Kapillaraszension konvex (Kapillardepression, Bild 14.15b). Die Steighöhe ist, wie aus (14.16) hervorgeht, dem Radius der Kapillare umgekehrt proportional.

Mit (14.16) erhält man zugleich eine Methode, um die Oberflächenspannung σ oder bei deren Kenntnis den Randwinkel ϑ zu messen (Steighöhenmethode). Die Kapillaraszension ist Ursache des Aufsteigens von Flüssigkeiten in allen porösen Körpern, wie Ziegelsteinen, Dochten, Pflanzenfasern, Holz usw.

## Beispiele 14.5:

1. Wie groß ist die gegen die Oberflächenspannung zu verrichtende Arbeit, wenn 1 Liter Wasser $( \sigma = 0 , 0 7 4 \mathrm { N / m } )$ mittels eines Zerstäubers in lauter Tröpfchen von 0,1mm Durchmesser vollständig zerstäubt wird?

Lösung: Da das Volumen eines Tröpfchens gleich 4 $\pi r ^ { 3 } / 3 \approx 5   \cdot   1 0 ^ { - 1 3 }   \mathrm { m } ^ { 3 }$ ist, beträgt die Anzahl der zu bildenden Tröpfchen $1 0 ^ { - 3 }   \mathrm { m } ^ { 3 } / ( 5   \cdot   1 0 ^ { - \widetilde { 1 3 } }   \mathrm { m } ^ { 3 } ) = 2   \cdot   1 0 ^ { 9 }$ , die zusammen eine Oberfläche von $6 0   \mathrm { m } ^ { 2 }$ (!) haben. Demgegenüber kann die ursprüngliche Oberfläche des Wassers vernachlässigt werden. Mit $\Delta A = 6 0   \mathrm { m } ^ { 2 }$ folgt aus (14.11) für die Arbeit $\Delta W \approx 4 { , } 5 \mathrm { J }$

2. Was geschieht, wenn eine kleine Seifenblase durch ein Röhrchen mit einer größeren verbunden wird, so dass ein Überströmen der Luft erfolgen kann?

Lösung: Da nach (14.13) der Überdruck im Innern einer Seifenblase umso größer ist, je kleiner ihr Radius ist, wird die Luft aus der kleinen Blase in die große strömen, so dass sich diese weiter vergrößert, während sich die kleine vollständig zusammenzieht. □

## Aufgabe

**14.5** An der Ausflussöffnung einer Pipette (Radius der Öffnung $R = 0 , 5   \mathrm { m m }$ befindet sich ein kugelförmiger Wassertropfen $\sigma = 0 , 0 7 4 \mathrm { N / m }$ , Dichte $\varrho = 1   \mathrm{kg/dm^3}$ . Welchen Durchmesser kann der Tropfen maximal haben, bevor er abreißt?
