# 18 Elektrische Felder

原始 PDF 第 447–468 页。

# 18 Elektrische Felder

## 18.1 Das elektrische Feld

## Physikalische Motivation

Aus dem vorhergehenden Kapitel wissen wir, dass zwischen zwei benachbarten elektrisch geladenen Teilchen eine elektrostatische Kraft wirkt. Wir kennen auch die Richtung dieser Kraft und können ihren Betrag berechnen, sofern wir die beteiligten Ladungen und ihren Abstand voneinander kennen. Eine Frage bleibt dabei jedoch offen: Woher „weiß“ die eine Ladung von der Anwesenheit der anderen? Wie können sie eine Kraft aufeinander ausüben, obwohl sie sich nicht berühren?

Die Physik sammelt Beobachtungen über unsere Welt, beispielsweise Betrag und Richtung einer Kraft auf ein geladenes Teilchen. Es ist dann ihre Aufgabe, Erklä- rungen für das zu liefern, was sie beobachtet. In dem folgenden Kapitel werden wir uns eine physikalische Antwort auf die offene Frage nach der Kraftwirkung ohne direkten Kontakt erarbeiten.

Das Konzept, das uns diese Antwort liefern kann, ist das des elektrischen Felds. Ein geladenes Teilchen erzeugt in seiner Umgebung – insbesondere auch im Vakuum, wo keinerlei andere Teilchen vorhanden sind – ein elektrisches Feld. Wenn wir nun ein weiteres geladenes Teilchen in die Umgebung des ersten bringen, dann spürt dieses das elektrische Feld des ersten und „erfährt“ auf diese Weise von dessen Existenz. Das erste Teilchen übt die Kraft auf das zweite folglich nicht durch direkten physischen Kontakt aus (wie Sie es tun würden, wenn Sie eine Tasse auf dem Tisch verschieben wollten). Die Kraft wird vielmehr über das von dem ersten Teilchen erzeugte elektrische Feld vermittelt (etwa so, als ob Sie die Tasse nicht direkt verschieben, sondern an dem Tischtuch ziehen, auf dem die Tasse steht).

Unsere Ziele in diesem Kapitel sind (1) das elektrische Feld zu definieren, (2) zu erläutern, wie man es für verschiedene Anordnungen von geladenen Teilchen und Gegenständen berechnen kann und (3) zu beschreiben, welche Wirkungen ein elektrisches Feld auf geladene Teilchen haben kann.

![](../../raw/pages_0417-0448/images/page_446_image_7.jpg)

## 18.1.1 Das elektrische Feld

In der Physik und in den Ingenieurwissenschaften werden zahlreiche unterschiedliche Felder verwendet. Beispielsweise hat die Temperatur der Luft an jedem Punkt eines Raums einen bestimmten Wert. Man kann diesen Wert an einem bestimmten Punkt oder an vielen Punkten messen, indem man ein Thermometer an die jeweiligen Punkte bringt. Eine auf diese Weise gemessene räumliche Verteilung von Temperaturwerten bezeichnen wir als Temperaturfeld. In ganz entsprechender Weise kann man von einem Druckfeld in der Erdatmosphäre sprechen, einer räumlichen Verteilung von Luftdruckwerten in der Atmosphäre, wobei jedem Raumpunkt ein eindeutiger Druckwert zugeordnet wird. Die beiden genannten Felder sind Beispiele für skalare Felder, da sowohl Druck als auch Temperatur skalare Größen sind.

Halliday Physik für natur- und ingenieurwiss. Studiengänge, 3. Auflage. D. Halliday, R. Resnick und J. Walker. © 2020 WILEY-VCH Verlag GmbH & Co. KGaA. Published 2020 by WILEY-VCH Verlag GmbH & Co. KGaA.

433

---

18 Elektrische Felder

![](../../raw/pages_0417-0448/images/page_447_image_1.jpg)

Abb. 18.1

(a) Eine positive Probeladung $q _ { 0 }$ wird an den Punkt P in der Nähe eines geladenen Körpers gebracht, wo eine elektrostatische Kraft $\vec { \bar { F } }$ auf die Probeladung wirkt. (b) Das von dem geladenen Körper im Punkt P erzeugte elektrische Feld E⃗.

Das elektrische Feld dagegen ist ein Vektorfeld: Jedem Punkt des Raums um einen geladenen Körper ist ein bestimmter Vektor zugeordnet. Man kann das elektrische Feld an einem bestimmten Punkt in der Umgebung eines geladenen Körpers, beispielsweise im Punkt P in Abb. 18.1a, in der folgenden Weise definieren: Wir bringen zunächst eine positive Punktladung $q _ { 0 } ,$ die wir als Probeladung bezeichnen, an den Punkt P. Nun messen wir die elektrostatische Kraft $\vec { F }$ auf diese Probeladung. Schließlich definieren wir das elektrische Feld, welches durch den geladenen Körper im Punkt P erzeugt wird, als

$$
\vec {E} = \frac {\vec {F}}{q _ {0}}. \tag {18.1}
$$

Damit ist der Betrag des elektrischen Felds $\vec { E }$ im Punkt P gegeben durch $E = F / q _ { 0 }$ Die Richtung von $\vec { E }$ ist die Richtung der elektrostatischen Kraft $\vec { F }$ auf eine positive Probeladung. Wir stellen das elektrische Feld im Punkt P mit einem Pfeil dar, dessen Ausgangspunkt am Punkt $\mathrm { p }$ „angeheftet“ ist und dessen Spitze in Feldrichtung zeigt (Abb. 18.1b). Ein Feld ist in einem Raumbereich definiert, wenn es in jedem Punkt des Raumbereichs definiert ist.

Die SI-Einheit des elektrischen Felds ist Newton pro Coulomb (N/C). Tabelle 18.1 fasst typische Werte von elektrischen Feldern in verschiedenen physikalischen Situationen zusammen.

TABELLE 18.1:

Elektrische Feldstärken.

| Ort des Felds | Betrag (N/C) |
| --- | --- |
| an der Oberfläche eines Urankerns | $3 \cdot 10^{21}$ |
| innerhalb eines Wasserstoffatoms bei einem Radius von $5,29 \cdot 10^{-11}$ m | $5 \cdot 10^{11}$ |
| elektrischer Durchbruch in Luft | $3 \cdot 10^{6}$ |
| auf der Trommel eines Fotokopierers | $10^{5}$ |
| in der Nähe eines statisch aufgeladenen Kamms | $10^{3}$ |
| in der unteren Atmosphäre | $10^{2}$ |
| in der Anschlussleitung eines Haushaltsgeräts | $10^{-2}$ |

Obwohl wir zur Definition des elektrischen Felds eine positive Probeladung angenommen haben, existiert das Feld natürlich auch unabhängig von dieser Probeladung. Das Feld im Punkt P (Abb. 18.1b) beispielsweise war bereits vorhanden, bevor die Probeladung an diesen Punkt gebracht wurde und ist es auch weiterhin, sobald die Probeladung an ihrem Platz sitzt (Abb. 18.1a). (Wir nehmen bei unserer Definition natürlich an, dass das Vorhandensein der Probeladung die Ladungsverteilung auf dem geladenen Körper und damit das elektrische Feld, das wir eigentlich definieren wollen, nicht verändert.)

In den folgenden Abschnitten werden wir uns damit befassen, die elektrischen Felder zu berechnen, die von verschiedenen Ladungsverteilungen erzeugt werden, sowie die Kräfte auf Ladungen zu bestimmen, die sich in elektrischen Feldern befinden. Zunächst jedoch gehen wir auf eine zweckmäßige Art der Veranschaulichung elektrischer Felder ein.

## 18.1.2 Elektrische Feldlinien

Michael Faraday, der im 19. Jahrhundert den Begriff des elektrischen Felds ent wickelt hat, stellte sich den Raum um einen geladenen Körper als angefüllt mit Kraftlinien vor. Obwohl man heute weiß, dass diesen **elektrischen Feldlinien** keine physikalische Realität zukommt, so sind sie doch sehr hilfreich, wenn man sich den räumlichen Verlauf von elektrischen Feldern veranschaulichen will.

434

---

18.1 Das elektrische Feld

18

Zwischen den elektrischen Feldlinien und den Vektoren des elektrischen Felds besteht der folgende Zusammenhang: (1) In jedem Punkt des Raums ist die Richtung des Felds $\vec { \cal { E } }$ in diesem Punkt gegeben durch die Richtung der Tangente an die durch diesen Punkt verlaufende Feldlinie. Verläuft die Feldlinie durch einen Punkt geradlinig, so ist die Feldrichtung mit der Richtung der Feldlinie identisch. (2) Man zeichnet die Feldlinien in der Weise, dass die Feldliniendichte, also die Anzahl von Feldlinien, die durch eine senkrecht zu den Linien gewählte Einheitsfläche hindurchtreten, proportional ist zum Betrag von E⃗. Diese zweite Konvention bedeutet anschaulich, dass die elektrische Feldstärke E in Bereichen mit höherer Feldliniendichte größer ist, in Bereichen mit geringerer Feldliniendichte entsprechend kleiner.

In Abb. 18.2a ist eine homogen negativ geladene Kugel zu sehen. Bringen wir eine positive Punktladung an einen Raumpunkt in der Umgebung der Kugel, so wirkt eine zum Mittelpunkt der Kugel gerichtete elektrostatische Kraft auf die Probeladung. Dies bedeutet, dass die elektrischen Feldvektoren in allen Punkten in der Umgebung der Kugel stets radial zur Kugel ausgerichtet sind. Diese räumliche Verteilung der Feldvektoren wird sehr gut durch die in Abb. 18.2b eingezeichneten Feldlinien veranschaulicht, die in jedem Punkt parallel zu den Vektoren der Kraft und des elektrischen Felds stehen. Darüber hinaus erkennt man am Auseinanderlaufen der Feldlinien, dass die elektrische Feldstärke mit zunehmendem Abstand von der Kugel immer geringer wird.

Wäre die Kugel von Abb. 18.2 homogen positiv geladen, so wären die Vektoren des elektrischen Felds und die Feldlinien in allen Punkten in der Umgebung der Kugel radial von der Kugel weg gerichtet. Wir können somit die folgende Regel formulieren:

![](../../raw/pages_0449-0480/images/page_448_image_5.jpg)

Elektrische Feldlinien beginnen bei einer positiven Ladung und zeigen zu einer negativen Ladung hin, wo sie enden.

Abbildung 18.3a zeigt einen Teil einer unendlich ausgedehnten, nichtleitenden Platte, die auf der Vorderseite eine homogene Verteilung positiver Ladung trägt. Bringt man eine positive Probeladung an einen beliebigen Raumpunkt vor der Platte, so ist die resultierende elektrostatische Kraft auf die Probeladung senkrecht von der Platte weg gerichtet, da sich alle Kraftkomponenten parallel zur Platte aus Symmetriegründen gegenseitig auslöschen. Damit steht auch der Vektor des elektrischen Felds in jedem Raumpunkt beiderseits der Platte senkrecht auf der Platte gerichtet (Abb. 18.3b und c). Da die Ladung homogen über die Platte verteilt ist, haben alle Feldvektoren den gleichen Betrag. Ein solches elektrisches Feld, das in jedem Raumpunkt gleichen Betrag und gleiche Richtung hat, nennen wir homogen.

Natürlich ist keine real existierende geladene Platte – beispielsweise eine Plastikplane – unendlich ausgedehnt. Betrachtet man jedoch einen Raumbereich in der Nähe der Mitte einer real existierenden Platte (und nicht etwa in der Nähe ihrer Kanten), so kann man in guter Näherung von einem Feldlinienverlauf ausgehen, wie er in Abb. 18.3b und c dargestellt ist.

![](../../raw/pages_0449-0480/images/page_448_image_9.jpg)

<details>
<summary>text_image</summary>

positive
Probeladung
F
(a)
</details>

![](../../raw/pages_0449-0480/images/page_448_image_10.jpg)

<details>
<summary>text_image</summary>

Diagram illustrating electric field lines and particle interaction with labeled vectors E and X
</details>

(b)

![](../../raw/pages_0449-0480/images/page_448_image_12.jpg)

<details>
<summary>natural_image</summary>

Pure diagram of parallel light rays passing through a central vertical line, no text or symbols present
</details>

(c)

![](../../raw/pages_0449-0480/images/page_448_image_14.jpg)

(a)

![](../../raw/pages_0449-0480/images/page_448_image_16.jpg)

<details>
<summary>text_image</summary>

elektrische
Feldlinien
E
(b)
</details>

## Abb. 18.2

(a) Die auf eine positive Probeladung in der Nähe einer homogenen, kugelförmigen Verteilung negativer Ladung wirkende elektrostatische Kraft
(b) Der elektrischen Feldvektor am Ort der Probeladung und die elektrischen Feldlinien im Raum um die Ladungsverteilung. Die Feldlinien enden an der negativen Ladung – ihr Ursprung ist bei entfernten, hier nicht dargestellten positiven Ladungen zu denken.

## Abb. 18.3

(a) Die elektrostatische Kraft $\vec { F }$ auf eine positive Probeladung in der Nä- he einer sehr großen, nichtleitenden Platte, die auf ihrer Vorderseite eine gleichförmig verteilte positive Ladung trägt. (b) Der elektrische Feldvektor $\vec { E }$ am Ort der Probeladung und die elektrischen Feldlinien im Raum nahe der Platte. Die Feldlinien sind von der positiv geladenen Platte weg gerichtet. (c) Seitenansicht von (b).

435

---

18 Elektrische Felder

![](../../raw/pages_0449-0480/images/page_449_image_1.jpg)

## Abb. 18.4

Feldlinien um zwei gleich große, positive Punktladungen. Die beiden Ladungen stoßen einander ab. (Die Feldlinien enden bei weit entfernten, negativen Ladungen.) Sie können sich das eigentlich dreidimensionale Feldlinienbild vorstellen, indem Sie sich das hier gezeigte ebene Muster um eine Achse gedreht denken, die in der Papierebene liegt und durch die beiden Ladungen verläuft. Man bezeichnet deshalb dieses dreidimensionale Feldlinienmuster sowie auch das elektrische Feld, welches von ihm beschrieben wird, als rotationssymmetrisch um diese Achse. In einem Punkt einer Feldlinie ist der Vektor des elektrischen Felds in diesem Punkt gezeichnet. Beachten Sie dabei, dass dieser Vektor zur Feldlinie in diesem Punkt tangential ist.

## Abb. 18.5

Darstellung der Feldlinien um zwei nah benachbarte Ladungen, eine positive und eine gleich große negative Ladung. Die Ladungen ziehen einander an. Das Feldlinienbild im Raum um die beiden Ladungen ist rotationssymmetrisch um eine Achse, die in der Papierebene liegt und durch die beiden Ladungen verläuft. In einem Punkt einer Feldlinie ist der Vektor des elektrischen Felds in diesem Punkt gezeichnet; er ist tangential zur Feldlinie durch den Punkt.

Abbildung 18.4 zeigt den Feldlinienverlauf in der Umgebung zweier benachbarter positiver Punktladungen, Abb. 18.5 das Feldlinienbild für zwei Ladungen mit gleichem Betrag, aber unterschiedlichen Vorzeichen. Diese Ladungsanordnung bezeichnet man als einen **elektrischen Dipol**. Obwohl wir nur selten quantitativen Gebrauch von Feldlinienbildern machen, so sind sie doch außerordentlich nützlich, um sich die Feldverhältnisse zu veranschaulichen. Man kann förmlich „sehen“, wie die Ladungen in Abb. 18.4 sich abstoßen oder wie sie sich in Abb. 18.5 anziehen.

## 18.2 Das elektrische Feld einer Punktladung

![](../../raw/pages_0449-0480/images/page_449_image_8.jpg)

## Lernziele

Nach dem Durcharbeiten dieses Abschnitts sollten Sie in der Lage sein, . . .

• den Vektor $\vec { E }$ des elektrischen Felds an einem Punkt in der Umgebung eines positiv oder negativ geladenen Teilchens zu skizzieren,
• für einen beliebigen Punkt im elektrischen Feld eines geladenen Teilchens den Zusammenhang zwischen der Feldstärke $E ,$ dem Betrag |q| der Ladung und dem Abstand r zwischen gewähltem Punkt und Ladung anzugeben,
• zu verstehen, dass die hier angegebene Gleichung für die elektrische Feldstärke nur für Punktladungen gilt, nicht für ausgedehnte geladene Objekte,
• falls an einem Punkt mehrere elektrische Felder vorhanden sind, die einzelnen Feldvektoren zu skizzieren und das Gesamtfeld durch Vektoraddition (nicht skalare Addition) der einzelnen Felder zu berechnen.

![](../../raw/pages_0449-0480/images/page_449_image_16.jpg)

## Schlüsselideen

• Die Feldstärke des elektrischen Felds $\vec { E } ,$ das von einem Teilchen mit der Ladung q erzeugt wird, beträgt in einer Entfernung r von dem Teilchen

$$
E = \frac {1}{4 \pi \varepsilon_ {0}} \frac {| q |}{r ^ {2}}.
$$

• Die Vektoren des elektrischen Felds eines positiv geladenen Teilchens zeigen alle von dem Teilchen weg. Die Vektoren des elektrischen Felds eines negativ geladenen Teilchens zeigen alle auf das Teilchen zu.
Wenn an einem Punkt mehrere elektrische Felder existieren, die von unterschiedlichen geladenen Teilchen erzeugt werden, ergibt sich das Gesamtfeld als Vektorsumme der einzelnen elektrischen Felder: Für elektrische Felder gilt das Superpositionsprinzip.

436

---

18.2 Das elektrische Feld einer Punktladung

18

## 18.2.1 Das elektrische Feld einer Punktladung

Um das elektrische Feld in einem beliebigen Punkt mit dem Abstand r von einer Punktladung $q$ (oder einem geladenen Teilchen) zu bestimmen, denken wir uns eine positive Probeladung $q _ { 0 }$ an diesen Punkt gebracht. Mit dem Coulomb-Gesetz (Gl. 17.4) berechnen wir den Betrag F der elektrostatischen Kraft auf $q _ { 0 }$ zu

$$
F = \frac {1}{4 \pi \varepsilon_ {0}} \frac {| q | | q _ {0} |}{r ^ {2}}. \tag {18.2}
$$

Hat $q$ positives Vorzeichen, so zeigt der Kraftvektor $\vec { F }$ von der Ladung weg, anderenfalls zeigt er direkt zur Ladung hin. Den Betrag des elektrischen Feldvektors erhalten wir aus Gl. 18.1:

$$
E = \frac {F}{q _ {0}} = \frac {1}{4 \pi \varepsilon_ {0}} \frac {| q |}{r ^ {2}}. \tag {18.3}
$$

Feldrichtung und Kraftrichtung sind identisch. Da wir bei unserer Überlegung keine weiteren Annahmen über den Ort der Probeladung $q _ { 0 }$ gemacht haben, ist der Betrag des elektrischen Felds in einem beliebigen Punkt in der Umgebung der Punktladung $q$ durch Gl. 18.3 gegeben. Abbildung 18.6 zeigt das elektrische Feld um eine positive Punktladung in Vektordarstellung (ohne Feldlinien).

Auf einfache Weise erhält man das resultierende elektrische Feld mehrerer Punktladungen: Bringen wir eine positive Probeladung $q _ { 0 }$ in die Nähe von n Punktladungen $q _ { 1 } , q _ { 2 } , \ldots , q _ { n } ,$ so ergibt sich die resultierende Kraft auf die Probeladung nach Gl. 17.7 zu

$$
\vec {F} _ {0} = \vec {F} _ {0 1} + \vec {F} _ {0 2} + \dots + \vec {F} _ {0 n}.
$$

Daraus folgt nach Gl. 18.1 für das resultierende elektrische Feld am Ort der Probeladung

$$
\vec {E} = \frac {\vec {F} _ {0}}{q _ {0}} = \frac {\vec {F} _ {0 1}}{q _ {0}} + \frac {\vec {F} _ {0 2}}{q _ {0}} + \dots + \frac {\vec {F} _ {0 n}}{q _ {0}} = \vec {E} _ {1} + \vec {E} _ {2} + \dots + \vec {E} _ {n}. \tag {18.4}
$$

$\vec { E } _ { \mathrm { i } }$ bezeichnet das elektrische Feld, das die Punktladung i erzeugen würde, wäre sie allein vorhanden. Gleichung 18.4 zeigt uns, dass das Superpositionsprinzip für elektrische Felder genauso gilt wie für elektrostatische Kräfte.

## KONTROLLFRAGE 1

Die Abbildung zeigt ein Proton p und ein Elektron e auf einer x-Achse. Welche Richtung hat das vom Elektron erzeugte Feld (a) im Punkt S, (b) im Punkt R? Welche Richtung hat das resultierende elektrische Feld (c) im Punkt R, (d) im Punkt S?

## KONTROLLFRAGE 2

Die Abbildung zeigt vier Anordnungen von Punktladungen, die vom Ursprung des Koordinatensystems jeweils gleich weit entfernt seien. Ordnen Sie die vier Fälle nach dem Betrag des resultierenden elektrischen Felds im Ursprung.

![](../../raw/pages_0449-0480/images/page_450_image_17.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph TD
  Center(("+")) --> Node1["Node 1"]
  Node1 --> Node2["Node 2"]
  Node2 --> Node3["Node 3"]
  Node3 --> Node4["Node 4"]
  Node4 --> Node5["Node 5"]
  Node5 --> Node6["Node 6"]
  Node6 --> Node7["Node 7"]
  Node7 --> Node8["Node 8"]
  Node8 --> Node9["Node 9"]
  Node9 --> Node10["Node 10"]
  Node10 --> Node11["Node 11"]
  Node11 --> Node12["Node 12"]
  Node12 --> Node13["Node 13"]
  Node13 --> Node14["Node 14"]
  Node14 --> Node15["Node 15"]
  Node15 --> Node16["Node 16"]
  Node16 --> Node17["Node 17"]
  Node17 --> Node18["Node 18"]
```
</details>

Abb. 18.6

Vektoren des elektrischen Felds an verschiedenen Punkten um eine positive Punktladung.

![](../../raw/pages_0449-0480/images/page_450_image_20.jpg)

![](../../raw/pages_0449-0480/images/page_450_chart_21.jpg)

<details>
<summary>scatter</summary>

| Point | X | Y |
| --- | --- | --- |
| 1 | 2q | 0 |
| 2 | -3q | 0 |
| 3 | -5q | -5q |
</details>

(a)

![](../../raw/pages_0449-0480/images/page_450_chart_23.jpg)

<details>
<summary>scatter</summary>

| X | Y |
| --- | --- |
| -2q | -5q |
| 3q | 0 |
</details>

(b)

![](../../raw/pages_0449-0480/images/page_450_image_25.jpg)

<details>
<summary>text_image</summary>

y
4q
-q
x
5q
</details>

(c)

![](../../raw/pages_0449-0480/images/page_450_image_27.jpg)

<details>
<summary>text_image</summary>

y
-q
x
q
-4q
4q
</details>

(d)

437

---

18 Elektrische Felder

## 18.3Das elektrischeFeldeines Dipols

![](../../raw/pages_0449-0480/images/page_451_image_2.jpg)

## Lernziele

Nach dem Durcharbeiten dieses Abschnitts sollten Sie in der Lage sein, . . .

• einen elektrischen Dipol zu zeichnen, seine Ladungen (Beträge und Vorzeichen) anzugeben und Dipolachse und Richtung des elektrischen Dipolmoments zu markieren,
• die Richtung des elektrischen Felds an einem beliebigen Punkt auf der Dipolachse (auch zwischen den Ladungen) anzugeben,
• zu beschreiben, wie die Gleichung für das elektrische Feld eines elektrischen Dipols aus den Gleichungen für das elektrische Feld der beiden Einzelladungen hervorgeht,
die elektrischen Felder eines einzelnen geladenen Teilchens und eines elektrischen Dipols daraufhin zu vergleichen, wie schnell sie mit der Entfernung abnehmen (d. h. anzugeben, welches Feld schneller abnimmt),
• die Beziehung zwischen dem Betrag $p$ des Dipolmoments, dem Abstand d seiner Ladungen und dem Betrag q der Ladungen anzugeben,
• für einen weit entfernten Punkt auf einer Dipolachse die Beziehung zwischen der elektrischen Feldstärke E, dem Abstand z vom Zentrum des Dipols und dem Betragp des Dipolmoments zu kennen.

![](../../raw/pages_0449-0480/images/page_451_image_12.jpg)

## Schlüsselideen

• Ein elektrischer Dipol besteht aus zwei Ladungen mit gleichem Betrag $q ,$ aber entgegengesetzten Vorzeichen in einem kleinen Abstand d voneinander.
• Das elektrische Dipolmoment $\vec { p }$ hat den Betrag qd und zeigt von der negativen zur positiven Ladung.
• Der Betrag des elektrischen Felds, das ein elektrischer Dipol an einem entfernten Punkt auf der Dipolachse (die durch beide Teilchen verläuft) erzeugt, berechnet sich aus dem Betragp des Dipolmoments zu

$$
E = \frac {1}{2 \pi \varepsilon_ {0}} \frac {p}{z ^ {3}},
$$

wobei z die Entfernung des betreffenden Punkts vom Zentrum des Dipols ist.

• Aufgrund der $1 / z ^ { 3 }$ -Abhängigkeit von der Entfernung nimmt die Feldstärke eines elektrischen Dipols schneller ab als die Feldstärke der einzelnen Ladungen, die den Dipol bilden (diese nehmen wie $1 / r ^ { 2 }$ ab).

## 18.3.1Das elektrischeFeldeines elektrischen Dipols

Abbildung 18.7a zeigt zwei geladene Teilchen, deren Ladungen den gleichen Betrag, aber entgegengesetzte Vorzeichen haben. Die Teilchen seien in einem Abstand d voneinander fixiert. Wie wir schon bei Abb. 18.5 angemerkt haben, nennt man diese Ladungskonfiguration einen elektrischen Dipol. Wir wollen das elektrische Feld dieses Dipols in einem Punkt P berechnen, der auf der Verbindungslinie der beiden Ladungen, der Dipolachse, liegt und einen Abstandz vom Mittelpunkt des Dipols hat.

Aus Symmetriegründen muss das resultierende elektrische Feld $\vec { E }$ im Punkt P ebenso wie die Felder $\vec { E } _ { ( + ) }$ und $\vec { E } _ { ( - ) } ,$ die von den beiden Dipolladungen im Punkt P erzeugt werden, auf der Dipolachse liegen, die wir deshalb als z-Achse wählen. Wenden wir das auch für elektrische Felder geltende Superpositionsprinzip an, so erhalten wir den BetragE des elektrischen Felds im Punkt P zu

$$
\begin{array}{l} E = E _ {(+)} - E _ {(-)} = \frac {1}{4 \pi \varepsilon_ {0}} \frac {q}{r _ {(+)} ^ {2}} - \frac {1}{4 \pi \varepsilon_ {0}} \frac {q}{r _ {(-)} ^ {2}} \\ = \frac {q}{4 \pi \varepsilon_ {0} \left(z - \frac {1}{2} d\right) ^ {2}} - \frac {q}{4 \pi \varepsilon_ {0} \left(z + \frac {1}{2} d\right) ^ {2}}. \tag {18.5} \\ \end{array}
$$

438

---

18.3 Das elektrische Feld eines Dipols

18

Diesen Ausdruck können wir auch auf die Form

$$
E = \frac {q}{4 \pi \varepsilon_ {0} z ^ {2}} \left[ \left(1 - \frac {d}{2 z}\right) ^ {- 2} - \left(1 + \frac {d}{2 z}\right) ^ {- 2} \right] \tag {18.6}
$$

bringen. Normalerweise ist man an der elektrischen Wirkung eines Dipols nur in Entfernungen interessiert, die groß sind im Vergleich zu den Abmessungen des Dipols, also für $z \gg d .$ Bei solch großen Entfernungen kann man in Gl. 18. $5   d / 2 z \ll 1$ annehmen und die beiden in den eckigen Klammern stehenden Ausdrücke mithilfe der binomischen Reihe (Anhang D) entwickeln. Man erhält so

$$
\left[ \left(1 - \frac {d}{2 z}\right) ^ {- 2} - \left(1 + \frac {d}{2 z}\right) ^ {- 2} \right] \approx \left[ \left(1 + \frac {2 d}{2 z (1 !)} + \dots\right) - \left(1 - \frac {2 d}{2 z (1 !)} + \dots\right) \right]
$$

und

$$
E = \frac {q}{4 \pi \varepsilon_ {0} z ^ {2}} \left[ \left(1 + \frac {d}{z} + \dots\right) - \left(1 - \frac {d}{z} + \dots\right) \right]. \tag {18.7}
$$

Die weggelassenen Terme der Reihenentwicklungen von Gl. 18.7 enthalten höhere Potenzen von $d / z .$ Da nach unserer Annahme $d / z \ll 1$ gilt, nehmen die Beiträge dieser Terme zur Summe der Reihe rasch ab und wir können sie bei einer Berechnung des elektrischen Felds in großen Entfernungen vom Dipol vernachlässigen. In dieser Näherung erhält Gl. 18.7 die Form

$$
E = \frac {q}{4 \pi \varepsilon_ {0} z ^ {2}} \frac {2 d}{z} = \frac {1}{2 \pi \varepsilon_ {0}} \frac {q d}{z ^ {3}}. \tag {18.8}
$$

Das Produkt $q d ,$ welches die beiden wesentlichen Eigenschaften eines elektrischen Dipols, nämlich den Betrag der beteiligten Ladungen sowie deren Abstand enthält, ist der Betrag $p$ einer vektoriellen Größe $\vec { p } ,$ dem **elektrischen Dipolmoment** des Dipols. Die Einheit des Dipolmoments ist Coulomb mal Meter (C m). Damit wird Gl. 18.8 zu

$$
E = \frac {1}{2 \pi \varepsilon} \frac {p}{z ^ {3}}. \tag {18.9}
$$

Man wählt die Richtung von $\vec { p }$ als die Richtung vom negativen Ende des Dipols zum positiven Ende, wie in Abb. 18.7b dargestellt. Der Dipolmomentvektor $\vec { p }$ gibt die Orientierung des Dipols im Raum an.

Gleichung 18.9 liefert nur das Produkt $p ,$ nicht jedoch die beiden Faktoren q und $d$ separat. Dies bedeutet, dass man aus einer Messung des Dipolfelds an einem weit vom Dipol entfernten Ort nur das Produkt von $q$ und $d$ erhält, nicht jedoch die beiden Faktoren separat. So bliebe das Dipolfeld an weit entfernten Orten unverändert, würde man beispielsweise $q$ verdoppeln und gleichzeitig d halbieren. Man erkennt daraus, dass das Dipolmoment die wesentliche physikalische Eigenschaft eines Dipols ist.

Obwohl Gl. 18.9 streng genommen nur für Punkte anwendbar ist, die auf der Dipolachse liegen und außerdem weit vom Dipol entfernt sind, so zeigt doch eine genauere Untersuchung, dass die Proportionalität zu $1 / r ^ { 3 }$ für alle Punkte des Raums um einen Dipol gilt, sofern sie nur hinreichend weit vom Dipol entfernt sind (r bezeichnet die Entfernung zwischen einem Punkt im Raum und dem Mittelpunkt des Dipols.).

Vergleicht man Abb. 18.7 und das Feldlinienbild von Abb. 18.5, so erkennt man, dass das Dipolfeld $\vec { E }$ in Punkten, die weit vom Dipol entfernt auf der Dipolachse liegen, immer die Orientierung des Dipolmomentvektors $\vec { p }$ hat. Diese Aussage gilt unabhängig davon, ob der Punkt P in Abb. 18.7a oberhalb oder unterhalb des Dipols liegt.

Wie man aus Gl. 18.9 erkennt, nimmt das Dipolfeld um einen Faktor 8 ab, wenn man sich doppelt so weit vom Dipol entfernt, das Feld einer einzelnen Punktla-

![](../../raw/pages_0449-0480/images/page_452_image_17.jpg)

<details>
<summary>text_image</summary>

z
→ E(+)
P
→ E(-)
r(+)
r(-)
r
+q
d
Dipol-
mittelpunkt
-q
(a)
(b)
</details>

Abb. 18.7

(a) Ein elektrischer Dipol. Die Feldvektoren $\vec { E } _ { ( + ) }$ und $\vec { E } _ { ( - ) }$ im Punkt P auf der Dipolachse beschreiben die von den beiden Ladungen $+ q$ und −q des Dipols hervorgerufenen elektrischen Felder. Der Abstand zwischen dem Punkt P und der Ladung +q des Dipols sei $r _ { ( + ) } ,$ der Abstand zwischen P und der Ladung $- q$ sei $r _ { ( - }$ ). (b) Das Dipolmoment $\vec { p }$ des Dipols ist ein Vektor, der von der negativen zur positiven Ladung zeigt.

439

---

18 Elektrische Felder

dung (Gl. 18.3) dagegen nur um einen Faktor 4. Das Feld eines Dipols nimmt also mit der Entfernung rascher ab als das Feld einer Einzelladung. Eine physikalische Begründung für dieses Verhalten kann man darin sehen, dass ein Dipol aus großer Entfernung betrachtet wie ein Paar von betragsgleichen, entgegengesetzten Ladungen erscheint, die sich fast in demselben Raumpunkt befinden, sodass sich ihre Felder in weit entfernten Punkten fast – aber eben nicht vollständig – auslöschen.

## 18.4 Elektrisches Feld einer linearen Ladungsverteilung

![](../../raw/pages_0449-0480/images/page_453_image_3.jpg)

## Lernziele

Nach dem Durcharbeiten dieses Abschnitts sollten Sie in der Lage sein, . . .

• für homogene Ladungsverteilungen die lineare Ladungsdichte λ einer linearen Ladungsverteilung, die Flächenladungsdichte σ einer Ladung auf einer Oberflä- che und die Volumenladungsdichte ρ einer über ein Volumen verteilten Ladung zu berechnen,
das elektrische Feld an einem Punkt in der Nähe einer homogenen linearen Ladungsverteilung zu berechnen, indem Sie die Verteilung in infinitesimale bzw. differenzielle Ladungselemente dq aufspalten und dann die differenziellen elektrischen Feldvektoren an dem betreffenden Punkt aufzuintegrieren,
• zu erläutern, wie man die Berechnung des elektrischen Felds an einem Punkt in der Nähe einer homogenen linearen Ladungsverteilung durch Symmetrieüberlegungen vereinfachen kann.

![](../../raw/pages_0449-0480/images/page_453_image_10.jpg)

## Schlüsselideen

• Die Gleichung für das von einem geladenen Teilchen erzeugte elektrische Feld gilt nicht für geladene ausgedehnte Objekte mit kontinuierlichen Ladungsverteilungen.
Um das elektrische Feld eines geladenen ausgedehnten Objekts an einem bestimmten Punkt zu bestimmen, betrachten wir zunächst das elektrische Feld aufgrund eines infinitesimalen bzw. differenziellen Ladungselements dq in dem Objekt, wobei das Element klein genug sein soll, dass wir die Gleichung für geladene Teilchen anwenden können. Anschließend integrieren wir die differenziellen Feldvektoren dE⃗ aller derartigen Ladungselemente.
• Da die einzelnen Feldelemente dE⃗ unterschiedliche Beträge besitzen und in verschiedene Richtungen zeigen, untersuchen wir zuerst, ob die Symmetrie des Systems dazu führt, dass sich gewisse Komponenten der Felder gegenseitig auslö- schen, was die Integration erheblich vereinfachen kann.

## 18.4.1 Das elektrische Feld einer linearen Ladungsverteilung

Wir haben bisher elektrische Felder betrachtet, wie sie von einer einzelnen oder höchstens von einigen wenigen Punktladungen erzeugt werden. Im Folgenden untersuchen wir dagegen elektrische Felder von Ladungsverteilungen, die wir uns als Mengen sehr vieler, eng benachbarter Punktladungen vorstellen, die entlang einer Linie, über eine Oberfläche oder in einem Raumvolumen verteilt sind. Wir betrachten solche makroskopischen Ladungsverteilungen dann als **kontinuierlich**, also nicht mehr aus diskreten Ladungen zusammengesetzt. Mathematisch behandelt man die elektrischen Felder von solchen kontinuierlichen Ladungsverteilungen mit den Mitteln der Infinitesimalrechnung. Im vorliegenden Abschnitt berechnen wir das elektrische Feld einer kontinuierlichen, linearen Ladungsverteilung, im folgenden Abschnitt das Feld einer geladenen Oberfläche. Schließlich werden wir im folgenden Kapitel das elektrische Feld innerhalb einer homogen geladenen Kugel betrachten.

440

---

18.4 Elektrisches Feld einer linearen Ladungsverteilung

18

Wenn wir kontinuierliche Ladungsverteilungen betrachten, behandeln wir die Ladung auf einem Körper sinnvollerweise als eine Ladungsdichte und nicht als eine Gesamtladung. So beschreiben wir beispielsweise eine lineare Ladungsverteilung durch Angabe einer linearen Ladungsdichte $\lambda ,$ deren Dimension Ladung pro Einheitslänge ist mit der SI-Einheit Coulomb pro Meter. Tabelle 18.2 fasst die übrigen Ladungsdichten zusammen, die wir verwenden werden.

Abbildung 18.8 zeigt einen dünnen Ring mit Radius $R ,$ der eine homogen verteilte positive lineare Ladungsdichte λ trägt. Der Ring soll beispielsweise aus Plastik oder einem anderen Isolator bestehen, sodass man die Ladungen auf dem Ring als ortsfest annehmen kann. Welches elektrische Feld $\vec { E }$ erzeugt diese ringförmige Ladungsverteilung an einem Punkt P, der in einer Entfernung z von der Ebene des Rings auf dessen Symmetrieachse liegt?

Mit Gl. 18.3 können wir diese Aufgabe offensichtlich nicht lösen. Dennoch lässt sich die Situation auf den Fall in Gl. 18.3 beschriebenen Fall einer Punktladung reduzieren, wenn wir uns den Ring in infinitesimale bzw. differenzielle Ladungselemente unterteilt denken, die alle so klein sind, dass wir sie als Punktladungen behandeln können. Nun summieren (eigentlich: integrieren) wir vektoriell alle Feldbeiträge, die von den differenziellen Ladungselementen im Punkt P erzeugt werden, und erhalten so das resultierende, von der ringförmigen Ladungsverteilung im Punkt P erzeugte Feld.

Jedes differenzielle Ladungselement habe die differenzielle Bogenlänge ds. Mit der linearen Ladungsdichte λ, der Ladung pro Einheitslänge auf dem Ring, kann man die differenzielle Ladung eines Ladungselements in der Form

$$
\mathrm{d} q = \lambda \mathrm{d} s \tag {18.10}
$$

schreiben. Diese differenzielle Ladung erzeugt in der Entfernung r im Punkt P ein differenzielles elektrisches Feld dE⃗. Behandelt man das Ladungselement als Punktladung, so folgt mit den Gln. 18.10 und 18.3 für den Betrag von dE⃗

$$
\mathrm{d} E = \frac {1}{4 \pi \varepsilon_ {0}} \frac {\mathrm{d} q}{r ^ {2}} = \frac {1}{4 \pi \varepsilon_ {0}} \frac {\lambda \mathrm{d} s}{r ^ {2}}. \tag {18.11}
$$

Aus Abb. 18.8 liest man $r ^ { 2 } = z ^ { 2 } + R ^ { 2 }$ ab, woraus mit Gl. 18.11

$$
\mathrm{d} E = \frac {1}{4 \pi \varepsilon_ {0}} \frac {\lambda \mathrm{d} s}{(z ^ {2} + R ^ {2})} \tag {18.12}
$$

folgt. Abbildung 18.8 zeigt, dass $\mathrm { d } \vec { E }$ einen Winkel θ mit der Symmetrieachse des Rings, unserer z-Achse, einschließt. Wir zerlegen den Vektor daher in Komponenten parallel und senkrecht zu dieser Achse.

Jedes Ladungselement des Rings erzeugt im Punkt P einen differenziellen Feldbeitrag d $\vec { \lfloor E \rfloor } ,$ dessen Betrag durch Gl. 18.12 gegeben ist. Die Komponenten aller Vektoren dE⃗ parallel zur Symmetrieachse sind einander in Betrag und Richtung gleich. Die Komponenten senkrecht zur Achse haben alle den gleichen Betrag, zeigen aber in unterschiedliche Richtungen. Jedoch existiert für jede beliebig herausgegriffene senkrechte Komponente eine andere, die exakt entgegengesetzt ist, sodass ihre Vektorsumme null wird. Da dies für jedes beliebige Paar senkrechter Komponenten gilt, löschen sich die Feldbeiträge senkrecht zur Symmetrieachse des Rings aus.

Wir brauchen deshalb nur die Komponenten der Feldbeiträge dE⃗ zu berücksichtigen, die parallel zur Symmetrieachse gerichtet sind, sodass sich der Betrag des resultierenden Felds in P einfach als Summe ihrer Beträge ergibt.

Die Parallelkomponente von $\mathrm { d } \vec { E }$ in Abb. 18.8 hat den Betrag dE cos θ. Damit lesen wir aus der Skizze ab:

$$
\cos \theta = \frac {z}{r} = \frac {z}{\sqrt {z ^ {2} + R ^ {2}}} . \tag {18.13}
$$

Aus den Gln. 18.13 und 18.12 erhalten wir nun für die Parallelkomponente von dE⃗

$$
\mathrm{d} E \cos \theta = \frac {z \lambda}{4 \pi \varepsilon_ {0} (z ^ {2} + R ^ {2}) ^ {3 / 2}} \mathrm{d} s. \tag {18.14}
$$

TABELLE 18.2:

Ladungsdichten.

| Name | Symbol | SI-Einheit |
| --- | --- | --- |
| Ladung | $q$ | C |
| lineare | $\lambda$ | C/m |
| Ladungsdichte |  |  |
| Flächenladungs- dichte | $\sigma$ | $C/m^{2}$ |
| Raumladungs- dichte | $\rho$ | $C/m^{2}$ |

![](../../raw/pages_0449-0480/images/page_454_image_21.jpg)

<details>
<summary>text_image</summary>

dE cos θ
θ
P
r
z
R
ds
dE
</details>

Abb. 18.8

Eine ringförmige und homogene Verteilung positiver Ladung. Ein differenzielles Längenelement ds des Rings (hier stark vergrößert gezeichnet) trägt die differenzielle Ladung dq. Dieses Ladungselement erzeugt im Punkt P ein elektrisches Feld $\mathrm { d } { \vec { E } } .$ Die Komponente dieses Felds in Richtung der Symmetrieachse des Rings beträgt dE cos θ.

441

---

18 Elektrische Felder

Um nun die von allen Ladungselementen erzeugten Parallelkomponenten dE cos θ zusammenzufassen, integrieren wir Gl. 18.14 über den Umfang des Rings, also von $s = 0$ bis $s = 2 \pi R$ . Da s im Ausdruck von Gl. 18.14 die einzige Variable ist, kann man alle übrigen Größen vor das Integral ziehen:

$$
E = \int \mathrm{d} E \cos \theta = \frac {z \lambda}{4 \pi \varepsilon_ {0} (z ^ {2} + R ^ {2}) ^ {3 / 2}} \int_ {0} ^ {2 \pi R} \mathrm{d} s = \frac {z \lambda (2 \pi R)}{4 \pi \varepsilon_ {0} (z ^ {2} + R ^ {2}) ^ {3 / 2}}. \tag {18.15}
$$

Da λ die Ladung pro Einheitslänge auf dem Ring angibt, ist der Faktor λ(2πR) in Gl. 18.15 identisch mit der Gesamtladung q des Rings. Damit bekommen wir

$$
E = \frac {q z}{4 \pi \varepsilon_ {0} (z ^ {2} + R ^ {2}) ^ {3 / 2}}. \tag {18.16}
$$

Auch bei negativer – statt, wie angenommen, positiver – Ladung des Rings ist der Betrag des elektrischen Felds im Punkt P durch Gl. 18.16 gegeben. Der Feldvektor zeigt nun jedoch zum Ring hin.

Überprüfen wir die Anwendbarkeit von Gl. 18.16 für einen Punkt auf der Ringachse, der so weit vom Ring entfernt ist, dass $z \gg R$ gilt. In diesem Fall kann man den Ausdruck $z ^ { 2 } + R ^ { 2 }$ in Gl. 18.16 durch $z ^ { 2 }$ annähern, und Gl. 18.16 wird zu

$$
E = \frac {1}{4 \pi \varepsilon_ {0}} \frac {q}{z ^ {2}}. \tag {18.17}
$$

Dies ist ein plausibles Ergebnis, da der Ring aus sehr großer Entfernung als Punkt ladung erscheint. Ersetzen wir z in Gl. 18.17 durch $r ,$ so erhalten wir Gl. 18.3, den Ausdruck für den Betrag des elektrischen Felds einer Punktladung.

Als Nächstes überprüfen wir Gl. 18.16 für den Mittelpunkt des Rings, also für $z = 0$ . Aus Gl. 18.16 folgt, dass das Feld in diesem Punkt verschwindet, d. h. $E = 0$ Auch dieses Ergebnis ist plausibel, denn bringen wir eine Probeladung in die Mitte des Rings, so ist die resultierende elektrostatische Kraft auf die Ladung null: Die von jedem einzelnen Ladungselement auf dem Ring verursachte Kraft auf die Probeladung wird kompensiert durch die Kraft des im Ring direkt gegenüberliegenden Ladungselements. Ist aber die resultierende Kraft auf die Probeladung null, so gilt dies nach Gl. 18.1 auch für das elektrische Feld.

## LÖSUNGSSTRATEGIEN

**Strategie 1: Felder linearer Ladungsverteilungen** Hier sind einige nützliche Regeln für die Bestimmung des von einer linearen Ladungsverteilung, die gekrümmt oder geradlinig sein kann, in einem Punkt P erzeugten elektrischen Felds E⃗. Die Vorgehensweise besteht in allen Fällen darin, ein differenzielles Ladungselement dq herauszugreifen, den von ihm erzeugten Feldbeitrag dE⃗ zu bestimmen und schließlich diesen Beitrag über die gesamte Länge der Ladungsverteilung zu integrieren.

• Schritt 1: Bei einer ringförmigen Ladungsverteilung wählen Sie als Länge ds eines differenziellen Ladungselements die Bogenlänge des Kreisbogens. Ist die Ladungsverteilung dagegen geradlinig, so legen Sie eine x-Achse fest, die mit der Ladungsverteilung zusammenfällt, und wählen dx als Länge eines Ladungsele ments. Fertigen Sie eine Zeichnung an und heben Sie darin das gewählte Längenelement hervor.
• Schritt 2: Setzen Sie die Ladung dq eines Ladungselements über eine lineare Ladungsdichte λ in Beziehung zur Länge des Elements: $\mathsf { d } q = \lambda$ ds oder d $. q = \lambda$ dx. Behandeln Sie $\mathrm { d } q$ und λ als positive Größen, auch dann, wenn die betrachtete Ladung negativ ist. (Das Vorzeichen der Ladung behandeln wir im nächsten Schritt.)
• Schritt 3: Berechnen Sie mithilfe von Gl. 18.3 den vom Ladungselement dq im fraglichen Punkt P erzeugten differenziellen Feldbeitrag $\mathrm { d } { \vec { E } } ,$ wobei Sie q in

442

---

18.4 Elektrisches Feld einer linearen Ladungsverteilung

18

Gl. 18.3 entweder durch λ ds oder λ dx ersetzen. Zeichnen Sie in Ihrer Skizze im Punkt P den Vektor d $1 \vec { E }$ ein; er ist senkrecht vom Ladungselement dq weg gerichtet, falls die Ladung positiv ist, anderenfalls zeigt er direkt auf das Ladungselement hin.

• Schritt 4: Nutzen Sie eventuell vorhandene Symmetrien zur Vereinfachung des Problems! Liegt beispielsweise der Punkt P auf einer Symmetrieachse der Ladungsverteilung, so zerlegen Sie den vom Ladungselement $\mathrm { d } q$ erzeugten Feldbeitrag $\mathrm { d } \vec { E }$ in Komponenten parallel und senkrecht zu dieser Symmetrieachse. Betrachten Sie dann ein zweites Ladungselement $\mathrm { d } \boldsymbol { q } ^ { \prime } ,$ das bezüglich der Symmetrieachse der Ladungsverteilung symmetrisch zu dq liegt. Zeichnen Sie dann auch den Feldbeitrag $\mathrm { d } \vec { E } ^ { \prime }$ , der von diesem zweiten Ladungselement erzeugt wird, im Punkt P ein und zerlegen Sie ihn in Komponenten. Aus Symmetriegründen finden sich dann zwei Komponenten der beiden Feldbeiträge, die einander kompensieren und deshalb nicht mehr weiter berücksichtigt werden müssen. Wir nennen sie verschwindende Komponenten. Summieren Sie dann die verbleibenden, nichtverschwindenden Komponenten für alle Ladungselemente durch Integration.
• Schritt 5: Für die folgenden vier charakteristischen Typen homogener linearer Ladungsverteilungen sieht Schritt 4 z. B. so aus:

Ring Der Punkt P liegt auf der Symmetrieachse des Rings, wie in Abb. 18.8 dargestellt. Ersetzen Sie $r ^ { 2 }$ im Ausdruck für dE durch $\bar { z ^ { 2 }   +   R ^ { 2 } }$ wie in Gl. 18.12. Drücken Sie die nicht verschwindende Komponente von dE⃗ durch θ aus. Dadurch erscheint cos $\theta$ in der Gleichung. θ ist jedoch für alle Ladungselemente gleich und deshalb keine Variable. Ersetzen Sie dann cos θ nach Gl. 18.13. Integrieren Sie abschließend über s, wobei Sie die Integrationsgrenzen so wählen, dass der gesamte Ring erfasst wird.
Kreisbogen Der Punkt P liegt im Krümmungsmittelpunkt des Bogens, wie in Abb. Ü18.3 im Übungsbuch dargestellt. Drücken Sie die nicht verschwindende Komponente von dE⃗ durch θ aus. Dadurch erscheint entweder sin θ oder cos θ in der Gleichung. Reduzieren Sie die Anzahl der Variablen (noch sind s und θ Variablen), indem Sie ds durch rθ ausdrücken. Integrieren Sie abschlie ßend über θ wie in Beispielaufgabe 18.3 im Übungsbuch vom einen Ende des Kreisbogens zum anderen.
Gerade Linie Der Punkt P liegt, wie in Abb. 18.9a dargestellt, auf einer Verlängerung der Ladungsverteilung. Ersetzen Sie r im Ausdruck für dE durch x. Integrieren Sie über x vom einen Ende der Ladungslinie bis zum anderen.
Gerade Linie Der Punkt P liegt, wie in Abb. 18.9b dargestellt, außerhalb der Ladungsachse in einer Entfernung y. Ersetzten Sie r im Ausdruck für dE durch einen Ausdruck in x und y. Liegt der Punkt P auf der Mittelsenkrechten der Ladungslinie, so leiten Sie einen Ausdruck zur Berechnung der nichtverschwindenden Komponente von dE her. Dadurch tritt entweder sin θ oder cos θ auf. Eliminieren Sie eine der beiden verbleibenden Variablen x und $\theta ,$ nämlich x, indem Sie die jeweilige trigonometrische Funktion durch ihre Definition, d. h. einen Ausdruck in x und $y ,$ ersetzen. Integrieren Sie abschließend über x, vom einen Ende der Ladungslinie zum anderen. Liegt der Punkt P, wie in Abb. 18.9c dargestellt, nicht symmetrisch zur Ladungslinie, so integrieren Sie separat erst die Komponente d $| E _ { x }$ über $x ,$ und dann $\mathrm { d } E _ { y }$ über $y .$ Sind die beiden Komponenten $E _ { x }$ und $E _ { y }$ bekannt, so berechnen Sie daraus in bekannter Weise Betrag und Richtung des Vektors $\vec { E } .$

• Schritt 6: In allen Fällen ist das Ergebnis der Integration je nach Wahl der Reihenfolge der Integrationsgrenzen einmal positiv, einmal negativ. Falls ein negatives Ergebnis auftreten sollte, so vernachlässigen Sie das Vorzeichen. Soll das Ergebnis in Abhängigkeit von der Gesamtladung Q der Ladungsverteilung ausgedrückt werden, so ersetzen Sie λ durch $Q / L$ , wobei L die Länge der Verteilung bezeichnet. Bei einer ringförmigen Ladungsverteilung ist L der Umfang des Rings.

![](../../raw/pages_0449-0480/images/page_456_image_12.jpg)

## Abb. 18.9

(a) Der Punkt P liegt auf der Achse einer linearen Ladungsverteilung.
(b) Hier liegt der Punkt P auf der vertikalen Symmetrieachse einer linearen Ladungsverteilung im Abstand y von der Verteilung. (c) Wie (b), nur mit dem Unterschied, dass P nicht auf der vertikalen Symmetrieachse liegt.

443

---

18 Elektrische Felder

## KONTROLLFRAGE 3

Die Abbildung zeigt drei nichtleitende Stäbe. Einer von ihnen ist zu einem halben Kreisring gebogen, die beiden anderen sind gerade. Jeder der Stäbe trägt auf seiner oberen Hälfte eine homogen verteilte Ladung vom Betrag Q, auf der unteren Hälfte eine Ladung mit gleichen Betrag und gleichem oder ungleichem Vorzeichen. Welches ist in jedem der drei Fälle die Richtung des resultierenden elektrischen Felds im Punkt P?

![](../../raw/pages_0449-0480/images/page_457_image_3.jpg)

(a)

![](../../raw/pages_0449-0480/images/page_457_image_5.jpg)

<details>
<summary>text_image</summary>

+Q
+Q
P
x
y
</details>

(b)

![](../../raw/pages_0449-0480/images/page_457_image_7.jpg)

<details>
<summary>text_image</summary>

+Q
-Q
P
x
y
</details>

(c)

## 18.5 Das elektrische Feld einer geladenen Scheibe

![](../../raw/pages_0449-0480/images/page_457_image_10.jpg)

## Lernziele

Nach dem Durcharbeiten dieses Abschnitts sollten Sie in der Lage sein, . . .

• eine homogen geladene Scheibe zu skizzieren und die Richtung des elektrischen Felds auf der Symmetrieachse für positive und negative Ladungen anzugeben,
mithilfe der Gleichung für das elektrische Feld auf der Mittelachse eines homogen geladenen Rings eine Gleichung für das elektrische Feld auf der Mittelachse einer homogen geladenen Scheibe herzuleiten,
• für Punkte auf der Mittelachse einer homogen geladenen Scheibe die Beziehung zwischen der Oberflächenladungsdichte σ, dem Scheibenradius R und dem Abstand z zwischen Punkt und Scheibe anzugeben.

![](../../raw/pages_0449-0480/images/page_457_image_17.jpg)

## Schlüsselideen

• Auf der Mittelachse durch eine homogen geladene Scheibe beträgt die elektrische Feldstärke

$$
E = \frac {\sigma}{2 \varepsilon_ {0}} \left(1 - \frac {z}{\sqrt {z ^ {2} + R ^ {2}}}\right).
$$

Dabei sind z der Abstand des betrachteten Punkts vom Scheibenmittelpunkt, R der Radius und σ die Flächenladungsdichte der Scheibe.

## 18.5.1 Das elektrische Feld einer geladenen Scheibe

Abbildung 18.10 zeigt eine kreisförmige Plastikscheibe vom Radius R, die auf ihrer Oberseite eine positive Ladung mit der homogenen Dichte σ trägt (siehe Tab. 18.2). Welches elektrische Feld erzeugt die Ladung der Scheibe in einem Punkt P, der in einer Entfernung z auf der Mittelachse der Scheibe liegt?

Unser Lösungsansatz ist es, uns die Scheibe in eine sehr große Anzahl konzentrischer, geladener Ringe zerlegt zu denken und das resultierende elektrische Feld im Punkt P durch Summation (Integration) der Feldbeiträge sämtlicher Ringe zu berechnen. Abbildung 18.10 zeigt einen dieser Ringe mit Radius r und differenzieller Breite dr. Die Ladung pro Einheitsfläche ist durch die Ladungsdichte σ gegeben, sodass die Ladung des Rings

$$
\mathrm{d} q = \sigma \mathrm{d} A = \sigma (2 \pi r \mathrm{d} r) \tag {18.18}
$$

beträgt. Dabei bezeichnet dA ein differenzielles Flächenelement des Rings.

444

---

18.5 Das elektrische Feld einer geladenen Scheibe

18

Die Aufgabe, das elektrische Feld eines Ladungsrings zu berechnen, haben wir bereits gelöst: Ersetzen wir $q$ in Gl. 18.16 durch dq von Gl. 18.18 sowie R durch $r ,$ so erhalten wir einen Ausdruck für den differenziellen Feldbeitrag $\mathrm { d } E ,$ den die Ladung des Rings im Punkt P erzeugt:

$$
\mathrm{d} E = \frac {z \sigma 2 \pi r \mathrm{d} r}{4 \pi \varepsilon_ {0} (z ^ {2} + r ^ {2}) ^ {3 / 2}}
$$

oder

$$
\mathrm{d} E = \frac {\sigma z}{4 \varepsilon_ {0}} \frac {2 r \mathrm{d} r}{(z ^ {2} + r ^ {2}) ^ {3 / 2}}. \tag {18.19}
$$

Wir erhalten nun E durch Integration von Gl. 18.19 über die gesamte Oberfläche der Scheibe, also durch Integration bezüglich der Variable r in den Grenzen $r = 0$ und $r = R$ . Beachten Sie, dass dabei z eine Konstante ist. Wir erhalten auf diese Weise

$$
E = \int \mathrm{d} E = \frac {\sigma z}{4 \varepsilon_ {0}} \int_ {0} ^ {R} (z ^ {2} + r ^ {2}) ^ {- 3 / 2} 2 r \mathrm{d} r. \tag {18.20}
$$

Zur Berechnung dieses Integrals bringen wir es auf die Form $\int X ^ { m }   \mathrm { d } X ,$ indem wir $\begin{array} { r } { X = ( z ^ { 2 } + r ^ { 2 } ) ,   \stackrel { \circ } { m } = - \frac { 3 } { 2 } } \end{array}$ und folglich $\mathsf { d } X = 2 r$ dr substituieren. Damit nimmt das Integral die Form

$$
\int X ^ {m} \mathrm{d} X = \frac {X ^ {m + 1}}{m + 1}
$$

an, und Gl. 18.20 wird zu

$$
E = \frac {\sigma z}{4 \varepsilon_ {0}} \left[ \frac {(z ^ {2} + r ^ {2}) ^ {- 1 / 2}}{- \frac {1}{2}} \right] _ {0} ^ {R}. \tag {18.21}
$$

Berechnen wir Gl. 18.21 in den Integrationsgrenzen, so erhalten wir nach einigen Umstellungen

$$
E = \frac {\sigma}{2 \varepsilon_ {0}} \left(1 - \frac {z}{\sqrt {z ^ {2} + R ^ {2}}}\right) \tag {18.22}
$$

für den Betrag des elektrischen Felds, das eine kreisförmige geladene Scheibe in einem Punkt ihrer Symmetrieachse erzeugt. (Bei der Ausführung der Integration haben wir $z \geq 0$ angenommen.)

Im Grenzfall $R \to \infty$ bei endlichem Wert von z geht der zweite Term in den Klammern in Gl. 18.22 gegen null und die Gleichung reduziert sich auf

$$
E = \frac {\sigma}{2 \varepsilon_ {0}}. \tag {18.23}
$$

Dieser Ausdruck beschreibt das elektrische Feld einer unendlich ausgedehnten, homogen verteilten Ladung, die auf einer Seite einer nichtleitenden Platte, bei spielsweise einer Plastikplatte, sitzt. Abbildung 18.3 zeigt den Verlauf der elektrischen Feldlinien für eine solche Anordnung.

Man erhält Gl. 18.23 auch, wenn man z in Gl. 18.22 gegen null gehen lässt, wäh rend R endlich bleibt. Physikalisch kann man dies dahingehend interpretieren, dass sich das Feld einer nur endlich ausgedehnten Scheibe in oberflächennahen Punkten dem Feld einer unendlich ausgedehnten Scheibe annähert.

![](../../raw/pages_0449-0480/images/page_458_image_19.jpg)

<details>
<summary>text_image</summary>

dE
P
z
dr
r
R
</details>

Abb. 18.10

Eine positive Ladung sei homogen über eine Scheibe mit dem Radius R verteilt. Ein herausgegriffener Ring habe einen Radius r sowie eine differenzielle Breite dr in radialer Richtung. Die Ladung auf diesem Ring erzeugt in einem Punkt P auf der Scheibenachse den differenziellen elektrischen Feldbeitrag dE⃗.

445

---

18 Elektrische Felder

## 18.6 Punktladung im elektrischen Feld

![](../../raw/pages_0449-0480/images/page_459_image_2.jpg)

## Lernziele

Nach dem Durcharbeiten dieses Abschnitts sollten Sie in der Lage sein, . . .

für ein geladenes Teilchen in einem externen (von anderen Ladungen erzeugten) elektrischen Feld die Beziehung zwischen dem elektrischen Feld E⃗ am Ort des Teilchens, der Teilchenladung und der auf das Teilchen wirkenden elektrostatischen Kraft $\vec { F }$ eine Aussage über die relativen Richtungen von Kraft und Feld zu treffen,
• den Millikan-Versuch zur Bestimmung der Elementarladung zu erläutern,
• das Funktionsprinzip von Tintenstrahldruckern zu erklären.

![](../../raw/pages_0449-0480/images/page_459_image_9.jpg)

## Schlüsselideen

• In einem externen elektrischen Feld wirkt auf ein Teilchen mit der Ladung q die elektrostatische Kraft

$$
\vec {F} = q \vec {E}.
$$

• Für positive Ladungen $+ q$ zeigt der Kraftvektor in dieselbe Richtung wie der Feldvektor. Für negative Ladungen −q zeigt der Kraftvektor entgegen der Richtung des Feldvektors (das Minuszeichen in der Gleichung bewirkt die Umkehrung der Richtung im zum Feldvektor).

## 18.6.1 Punktladung im elektrischen Feld

In den vorangegangenen Abschnitten haben wir die erste unserer Fragestellungen bearbeitet: Welches elektrische Feld erzeugt eine vorgegebene Ladungsverteilung im umgebenden Raum? Im Folgenden werden wir uns nun mit der zweiten Fragestellung beschäftigen: Wie verhält sich ein geladenes Teilchen im elektrischen Feld anderer, stationärer oder nur sehr langsam bewegter Ladungen?

Wie wir wissen, wirkt auf das Teilchen eine elektrostatische Kraft, gegeben durch

$$
\vec {F} = q \vec {E}, \tag {18.24}
$$

wobei $q$ die (vorzeichenbehaftete) Ladung des Teilchens bezeichnet. $\vec { E }$ ist ein elektrisches Feld, das andere Ladungen am Ort des betrachteten Teilchens erzeugen. Verwechseln Sie dieses Feld nicht mit dem vom Teilchen selbst erzeugten Feld! Zur Unterscheidung der beiden Felder bezeichnet man das Feld, welches nach Gl. 18.24 auf das Teilchen wirkt, auch als externes Feld. Ein geladenes Teilchen oder ein geladener Körper bleibt durch das von ihm selbst erzeugte Feld unbeeinflusst. In Worten besagt Gl. 18.24 Folgendes:

![](../../raw/pages_0449-0480/images/page_459_image_19.jpg)

Die elektrostatische Kraft $\vec { F }$ auf ein geladenes Teilchen, das sich in einem äußeren elektrischen Feld $\vec { E }$ befindet, hat die Richtung des Felds, falls die Ladung des Teilchens positiv ist. Ist die Ladung des Teilchens dagegen negativ, so zeigen Feld und Kraft in entgegengesetzte Richtungen.

![](../../raw/pages_0449-0480/images/page_459_image_21.jpg)

<details>
<summary>text_image</summary>

y
E
x
e
</details>

## KONTROLLFRAGE 4

(a) Welche Richtung hat die elektrostatische Kraft auf das in der Abbildung dargestellte Elektron im eingezeichneten elektrischen Feld? (b) In welche Richtung beschleunigt das Elektron, wenn es sich vor seinem Eintritt in das elektrische Feld parallel zu y-Achse bewegte? (c) Wenn sich das Elektron stattdessen anfänglich parallel zur x-Achse nach rechts bewegt hat, wird dann seine Geschwindigkeit beim Eintritt in das elektrische Feld zunehmen, abnehmen oder konstant bleiben?

446

---

18.6 Punktladung im elektrischen Feld

18

## Die Messung der Elementarladung

Gleichung 18.24 war die Grundlage einer Messung der Elementarladung e durch den amerikanischen Physiker Robert A. Millikan in den Jahren 1910–1913. In Abb. 18.11 ist die von ihm verwendete Versuchsanordnung schematisch dargestellt. Beim Einsprühen winziger Öltröpfchen in die Kammer A werden einige von ihnen positiv oder negativ aufgeladen. Wir betrachten ein Tröpfchen, das abwärts durch die kleine Öffnung in der Mitte von Platte $\mathrm { P } _ { 1 }$ in die Kammer C driftet, und nehmen an, das Tröpfchen trage eine negative Ladung $q .$

Solange der Schalter S geöffnet ist, hat die Batterie keinen Einfluss auf die Potenzialverhältnisse in der Kammer C. Schließt man den Schalter, sodass nun auch der positive Pol der Batterie mit der Kammer C verbunden ist, so erzeugt die Batterie einen Überschuss positiver Ladung auf der leitenden Platte $\mathrm { P } _ { 1 }$ sowie einen Überschuss negativer Ladung auf der leitenden Platte $\mathrm { P } _ { 2 } .$ In der Kammer $C ,$ zwischen den geladenen Platten, besteht nun ein nach unten gerichtetes elektrisches Feld ${ \vec { E } } .$ Nach Gl. 18.24 übt dieses Feld auf ein geladenes Teilchen eine Kraft aus, die seine Bewegung beeinflusst. Insbesondere wirkt auf ein negativ geladenes Öltröpfchen eine nach oben gerichtete Kraft und das Tröpfchen driftet in Richtung dieser Kraft.

Millikan beobachtete mithilfe eines Mikroskops jeweils ein einzelnes, geladenes Tröpfchen, maß seine Driftgeschwindigkeit sowohl mit als auch ohne äußeres elektrisches Feld und bestimmte so den Einfluss der Ladung des Tröpfchens auf dessen Bewegung. Dabei beobachtete er, dass die Ladungsmenge auf den Tröpfchen in jedem Fall durch eine Beziehung der Form

$$
q = n e \quad \text {fur} \quad n = 0, \pm 1, \pm 2, \pm 3, \dots , \tag {18.25}
$$

gegeben war, wobei sich der Faktor e als eine fundamentale Naturkonstante erwies, die Elementarladung mit dem Betrag $1 { , } 6 0 2 \cdot 1 0 ^ { - 1 9 }   ($ C. Dieses als Millikan-Versuch berühmt gewordene Experiment war der erste überzeugende Beweis dafür, dass die elektrische Ladung quantisiert ist, und Millikan erhielt zusammen mit anderen Physikern für seine Arbeit den Nobelpreis für Physik des Jahrs 1922. Moderne Methoden zur Messung der Elementarladung bedienen sich einer Vielzahl miteinander verflochtener experimenteller Techniken und liefern wesentlich genauere, aber qualitativ gleiche Ergebnisse.

## Tintenstrahldrucker

Der wachsende Bedarf an schnellen Druckern mit hoher Druckqualität hat in den 1980er und 1990er Jahren die Suche nach einer Alternative zu damals üblichen Drucktechniken motiviert, die durch Anschlag einer mit Tinte benetzten Druckmatrize auf das zu bedruckende Papier arbeiteten. Eine dieser Alternativen ist der Aufbau einzelner Buchstaben durch gezieltes Aufsprühen winziger Tintentropfen auf das Papier.

Abbildung 18.12 zeigt die Bewegung eines negativ geladenen Tintentröpfchens zwischen zwei elektrisch leitenden Ablenkplatten, zwischen denen ein nach unten gerichtetes, homogenes elektrisches Feld E⃗ besteht. Nach Gl. 18.24 wird das Tröpfchen nach oben abgelenkt und trifft schließlich auf den Papierbogen, wobei die Stärke der Ablenkung und damit der Ort des Auftreffens auf dem Papier durch die Feldstärke $\vec { E }$ und die Ladung $q$ des Tröpfchens bestimmt wird.

Bei der technischen Realisierung dieses Prinzips hält man das Feld $\vec { E }$ konstant und steuert die Stärke der Ablenkung durch gezielte Ladung des Tröpfchens in einer Ladeeinheit, die das Tröpfchen durchläuft, bevor es die Ablenkplatten erreicht. Diese Ladeeinheit wird durch ein elektronisches Signal angesteuert, welches die Information über das zu druckende Muster enthält.

![](../../raw/pages_0449-0480/images/page_460_image_12.jpg)

<details>
<summary>text_image</summary>

Öl-
nebel
A
P1
Öl-
tröpfchen
C
P2
elektrisch
isolierende
Kammer-
wand
Mikroskop
S
+
-
B
</details>

Abb. 18.11

Millikans Versuchsanordnung zur Messung der Elementarladung e. Driftet ein geladenes Öltröpfchen aus der Kammer A durch die kleine Öffnung in der Platte $\mathrm { P _ { 1 } }$ in den Bereich $C ,$ so kann man die Bewegung des Tröpfchens durch ein elektrisches Feld beeinflussen, welches durch Betätigen des Schalters S ein- oder ausgeschaltet wird. Mithilfe des Mikroskops kann man das Tröpfchen beobachten und seine Bewegung unter dem Einfluss des elektrischen Felds messen.

![](../../raw/pages_0449-0480/images/page_460_image_15.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph LR
  G["G"] --> C["C"]
  C --> E["Eingangs-signal"]
  E --> F["Ablenk-platten"]
  F --> P["Papier"]
```
</details>

Abb. 18.12

So funktioniert ein Tintenstrahldrucker: Tintentröpfchen werden im Zerstäuber G erzeugt und im Bereich C mit Ladung belegt. Ein Spannungssignal des Rechners steuert die Ladungsbelegung der Tröpfchen und legt damit fest, wie stark diese jeweils in einem elektrischen Feld abgelenkt werden und an welchem Punkt des Papiers sie deshalb schließlich auftreffen.

447

---

18 Elektrische Felder

![](../../raw/pages_0449-0480/images/page_461_image_1.jpg)

Abb. 18.13

Langzeitbelichtung eines kleinen Drahts, der an einen Hochspannungstransformator angeschlossen ist [Quelle: Chris Collura, www.skychaser.com].

## Elektrischer Durchbruch und Funken

Wenn die elektrische Feldstärke in der Luft einen gewissen kritischen Wert $E _ { \mathrm { k } }$ überschreitet, kommt es zu einem sogenannten elektrischen Durchbruch, bei dem das Feld Elektronen aus den Luftmolekülen herausschlägt. Dadurch wird die Luft leitfähig und die freigesetzten Elektronen werden sofort vom Feld beschleunigt. Auf ihrem Weg kollidieren sie mit Luftmolekülen und regen diese zum Leuchten an. Wir nehmen diese leuchtende Wegstrecken als Funken wahr. Abbildung 18.13 zeigt Funken, die sich über dem nicht isolierten Ende eines stark geladenen elektrischen Kabels bilden.

## 18.7 Ein Dipol in einem elektrischen Feld

![](../../raw/pages_0449-0480/images/page_461_image_7.jpg)

## Lernziele

Nach dem Durcharbeiten dieses Abschnitts sollten Sie in der Lage sein, . . .

in einer Skizze eines elektrischen Dipols in einem äußeren elektrischen Feld die Richtung des Felds, die Richtung des Dipolmoments, die Richtung der elektrostatischen Kräfte auf die beiden Enden des Dipols sowie die Richtung anzugeben, in die diese Kräfte den Dipol drehen wollen, und den Betrag der Gesamtkraft auf den Dipol anzugeben,
das Drehmoment auf einen elektrischen Dipol in einem externen elektrischen Feld aus dem Kreuzprodukt des Dipolmomentvektors und des elektrischen Feldvektors in Betrag-Winkel- und Einheitsvektoren-Schreibweise zu berechnen,
• für einen elektrischen Dipol in einem externen elektrischen Feld die Beziehung zwischen der potenziellen Energie des Dipols im Feld und der von einem Drehmoment bei der Drehung des Dipols verrichteten Arbeit anzugeben,
• die potenzielle Energie eines elektrischen Dipols in einem externen elektrischen Feld aus dem Skalarprodukt des Dipolmomentvektors und des elektrischen Feldvektors in Betrag-Winkel- und Einheitsvektoren-Schreibweise zu berechnen,
• für einen elektrischen Dipol in einem externen elektrischen Feld die Winkel anzugeben, bei denen seine potenzielle Energie minimal bzw. maximal wird,
• für einen elektrischen Dipol in einem externen elektrischen Feld die Winkel anzugeben, bei denen das auf ihn wirkende Drehmoment minimal bzw. maximal wird.

![](../../raw/pages_0449-0480/images/page_461_image_17.jpg)

## Schlüsselideen

• Das Drehmoment auf einen elektrischen Dipol mit dem Dipolmoment $\vec { p }$ in einem externen elektrischen Feld $\vec { E }$ ist durch das Kreuzprodukt aus Dipolmoment- und Feldvektor gegeben:

$$
\vec {\tau} = \vec {p} \times \vec {E}.
$$

• Mit der Orientierung eines Dipolmoments in einem äußeren elektrischen Feld ist eine potenzielle Energie U verknüpft, die durch das Skalarprodukt aus Dipolmoment- und Feldvektor gegeben ist:

$$
U = - \vec {p} \cdot \vec {E}.
$$

• Wenn sich die Orientierung eines Dipols in einem äußeren elektrischen Feld ändert, verrichtet das elektrische Feld die Arbeit

$$
W = - \Delta U.
$$

Wenn diese $\ddot { \mathrm { A r } }$ nderung der Orientierung von einer äußeren Vorrichtung bewirkt wird, verrichtet diese Vorrichtung die Arbeit $W _ { \mathrm { a } } = - W$

448

---

18.7 Ein Dipol in einem elektrischen Feld

18

## 18.7.1 Ein Dipol im elektrischen Feld

Wir haben das Dipolmoment $\vec { p }$ eines elektrischen Dipols definiert als einen Vek tor, der vom negativen zum positiven Ende des Dipols zeigt. Wie wir im Folgenden sehen werden, wird das Verhalten eines Dipols in einem homogenen äußeren elektrischen Feld $\vec { E }$ vollständig durch die beiden Vektoren $\vec { E }$ und $\vec { p }$ beschrieben, was bedeutet, dass man keinerlei Einzelheiten über die innere Struktur des Dipols benötigt.

Das Wassermolekül $\left(  H _{2} O  \right)$ bildet einen elektrischen Dipol. Die schwarzen Punkte in Abb. 18.14 deuten den Sauerstoffkern (mit acht Protonen) sowie die beiden Wasserstoffkerne (mit jeweils einem Proton) an. Die Aufenthaltsbereiche der Elektronen sind farbig schattiert.

Die drei Atomkerne im Wassermolekül liegen, bedingt durch die Bindungsgeometrie der beteiligten Atome, nicht auf einer Linie, sondern bilden einen Winkel von etwa 105°. Das Molekül hat deshalb eine „Sauerstoffseite“ und eine „Wasserstoffseite“. Die insgesamt zehn Elektronen des Moleküls zeigen die Tendenz, sich näher beim Sauerstoffkern als bei den beiden Wasserstoffkernen aufzuhalten, wodurch die Sauerstoffseite des Moleküls geringfügig stärker negativ geladen ist als die Wasserstoffseite. Folglich existiert ein elektrisches Dipolmoment $\vec { p } ,$ das parallel zur Symmetrieachse des Moleküls zur Wasserstoffseite gerichtet ist (Abb. 18.14). Ein Wassermolekül verhält sich in einem äußeren elektrischen Feld gerade so, wie man es von dem idealisierten elektrischen Dipol aus Abb. 18.7 erwarten würde.

Um dieses Verhalten kennenzulernen, betrachten wir nun einen solchen idealisierten Dipol in einem homogenen, äußeren elektrischen Feld $\vec { E }$ (Abb. 18.15a). Dabei nehmen wir an, dass der Dipol aus zwei Punktladungen vom Betrag q mit entgegengesetzten Vorzeichen besteht, die im Abstand d voneinander fixiert sind. Der Winkel zwischen dem Dipolmoment $\vec { p }$ und dem Feld $\vec { E }$ sei $\theta .$

Auf jedes der beiden Enden des Dipols wirken elektrostatische Kräfte. Da wir das elektrische Feld als homogen angenommen haben, sind diese Kräfte einander entgegengesetzt gerichtet (Abb. 18.15a) und haben den gleichen Betrag $F = q E .$ Einzig aufgrund der Homogenität des $F e l d s$ ist die resultierende elektrostatische Kraft auf den Dipol null, sodass sich der Massenschwerpunkt des Dipols nicht bewegt. Andererseits erzeugen die Kräfte auf die beiden Enden des Dipols ein resultierendes Drehmoment $\vec { \tau }$ bezüglich einer Achse durch seinen Schwerpunkt. Der Schwerpunkt liegt auf der Verbindungslinie der beiden Ladungen des Dipols in einer Entfernung x vom einen Ende und damit im Abstand $d   -   x$ vom anderen Ende. Mit von Gl. $6 . 2 8   ( \tau = r F$ sin 𝜑) ist der Betrag des resultierenden Drehmoments

$$
\tau = F x \sin \theta + F (d - x) \sin \theta = F d \sin \theta . \tag {18.26}
$$

Wir können den Betrag des Drehmoments $\vec { \tau }$ auch ausdrücken durch die Beträ- ge $E$ des elektrischen Felds und $p = q d$ des Dipolmoments. Dazu ersetzen wir $F$ in Gl. 18.26 durch $q E$ sowie d durch $p / q$ und erhalten

$$
\tau = p E \sin \theta . \tag {18.27}
$$

In Vektorform lautet diese Gleichung

$$
\vec {\tau} = \vec {p} \times \vec {E}. \tag {18.28}
$$

Die Vektoren $\vec { p }$ und $\vec { E }$ sind in Abb. 18.15b markiert. Das auf den Dipol wirkende Drehmoment versucht, den Vektor $\vec { p } \mathrm { ~ - ~ }$ und damit den ganzen Dipol – in Richtung des Felds $\vec { E }$ auszurichten, also den Winkel $\theta$ zu verringern. In der Situation von Abb. 18.15 ist dies eine Drehung im Uhrzeigersinn. Wie wir in Kapitel 6 besprochen haben, kann man ein Drehmoment, das eine Drehung im Uhrzeigersinn verursacht, darstellen, indem man seinem Betrag ein Minuszeichen hinzufügt. In dieser Schreibweise gilt dann für das in Abb. 18.15 wirkende Drehmoment

$$
\tau = - p E \sin \theta . \tag {18.29}
$$

![](../../raw/pages_0449-0480/images/page_462_image_15.jpg)

<details>
<summary>text_image</summary>

positive Seite
Wasserstoff
P
105°
Sauerstoff
Wasserstoff
negative Seite
</details>

Abb. 18.14

Schematische Darstellung eines Wassermoleküls: Die kleinen schwarzen Punkte repräsentieren die Atomkerne, während die farbigen Flächen die Aufenthaltsbereiche der Elektronen andeuten sollen. Das elektrische Dipolmoment $\vec { p }$ des Moleküls ist von der (negativ geladenen) Seite des Sauerstoffatoms zur (positiv geladenen) Seite der beiden Wasserstoffatome gerichtet.

![](../../raw/pages_0449-0480/images/page_462_image_18.jpg)

<details>
<summary>text_image</summary>

d
+q
F
p
θ
S
-q
E
(a)
</details>

![](../../raw/pages_0449-0480/images/page_462_image_19.jpg)

Abb. 18.15

(a) Ein elektrischer Dipol in einem homogenen elektrischen Feld ${ \vec { E } } .$ Der Dipol besteht aus zwei gleich großen, entgegengesetzten Punktladungen, die im Abstand d relativ zueinander fixiert sind. (b) Ein elektrisches Feld E⃗ übt ein Drehmoment τ auf den Dipol aus. Dieses Drehmoment τ ist ein Vektor, der senkrecht zur Papierebene steht und in sie hinein zeigt. (Einen senkrecht in die Papierebene hinein gerichteten Vektor symbolisiert man durch das Zeichen $\otimes - \mathrm { S i e }$ können sich darunter die Federn am Pfeilschaft des von ihnen fortfliegenden Vektorpfeils vorstellen.)

449

---

18 Elektrische Felder

## Potenzielle Energie eines elektrischen Dipols im elektrischen Feld

Mit der Orientierung eines elektrischen Dipols relativ zu einem elektrischen Feld ist eine potenzielle Energie verbunden. Ein Dipol in einem äußeren Feld hat die geringste potenzielle Energie, wenn er sich in seiner Gleichgewichtsorientierung befindet, sein Dipolmoment $\vec { p }$ also parallel zum elektrischen Feld ausgerichtet ist (da in diesem Fall $\vec { \tau } = \vec { p } \times \vec { E } = 0$ gilt). In allen davon abweichenden Orientierungen ist die potenzielle Energie größer. Ein Dipol verhält sich deshalb ähnlich wie ein Pendel: Ein Pendel hat die geringste potenzielle Gravitationsenergie in seiner Gleichgewichtslage, also bei der Auslenkung null. Um ein Pendel oder einen Dipol aus der Gleichgewichtslage zu entfernen, muss Arbeit von außen aufgewendet werden.

In jeder physikalischen Situation, in der eine potenzielle Energie auftritt, ist man in der Wahl derjenigen Systemkonfiguration mit der potenziellen Energie null, also in der Wahl des Nullpunkts der potenziellen Energie, vollkommen frei, da nur den Differenzen potenzieller Energien eine physikalische Bedeutung zukommt. Wie sich herausstellt, nimmt der Ausdruck für die potenzielle Energie eines elektrischen Dipols in einem äußeren elektrischen Feld seine einfachste Form an, wenn man der Orientierung des Dipols senkrecht zur Feldrichtung, also dem Winkel 90° in Abb. 18.15a, die potenzielle Energie null zuordnet. Mithilfe von Gl. 4.1 $( \Delta U = - W )$ kann man nun die potenzielle Energie $U$ des Dipols bei einer beliebigen anderen Orientierung relativ zur Feldrichtung ermitteln, indem man die Arbeit berechnet, die das Feld am Dipol verrichtet, wenn er aus seiner senkrechten Position (90°) in die Position $\theta$ gedreht wird. Unter Verwendung von Gl. 6.39 $\left( W = \int \tau   \mathrm { d } \theta \right)$ und Gl. 18.29 erhält man so die potenzielle Energie U des Dipols bei einem Winkel θ relativ zur Feldrichtung:

$$
U = - W = - \int_ {9 0 ^ {\circ}} ^ {0} \tau \mathrm{d} \theta = \int_ {9 0 ^ {\circ}} ^ {0} p E \sin \theta \mathrm{d} \theta . \tag {18.30}
$$

Ausführen der Integration ergibt

$$
U = - p E \cos \theta \tag {18.31}
$$

und in Vektorform erhalten wir dann

$$
U = - \vec {p} \cdot \vec {E}. \tag {18.32}
$$

Die Gln. 18.31 und 18.32 bedeuten, dass die potenzielle Energie eines Dipols im elektrischen Feld ihren geringsten Wert $U = - p E$ annimmt, wenn die beiden Vektoren $\vec { p }$ und $\vec { E }$ den Winkel $\theta = 0$ einschließen, also dieselbe Richtung haben (parallel sind). Die potenzielle Energie des Dipols ist dagegen am größten $( U = p E )$ bei einem Winkel $\theta = 1 8 0 ^ { \circ }$ , wenn also $\vec { p }$ und $\vec { \cal { E } }$ einander entgegengesetzt (antiparallel) gerichtet sind.

Wird ein Dipol aus einer initialen Orientierung $\theta _ { \mathrm { i } }$ in eine finale Orientierung $\theta _ { \mathrm { f } }$ gedreht, so verrichtet das elektrische Feld an ihm die Arbeit

$$
W = - \Delta U = - (U _ {\mathrm{f}} - U _ {\mathrm{i}}), \tag {18.33}
$$

wobei $U _ { \mathrm { i } }$ und $U _ { \mathrm { f } }$ nach Gl. 18.32 berechnet werden. Wird die Drehung des Dipols durch ein äußeres Drehmoment bewirkt, so ist die vom äußeren Drehmoment am Dipol verrichtete Arbeit $W _ { \mathrm { a } }$ das Negative der vom Feld am Dipol verrichteten Arbeit

$$
W _ {\mathrm{a}} = - W = (U _ {\mathrm{f}} - U _ {\mathrm{i}}). \tag {18.34}
$$

450

---

18.8 Zusammenfassung

18

## KONTROLLFRAGE 5

Die Abbildung zeigt vier verschiedene Orientierungen eines Dipols in einem äußeren elektrischen Feld. Ordnen Sie die vier Fälle nach (a) dem Betrag des auf den Dipol wirkenden Drehmoments sowie (b) dem Betrag der potenziellen Energie des Dipols.

![](../../raw/pages_0449-0480/images/page_464_image_4.jpg)

<details>
<summary>chemical</summary>

Diagram of a charged particle interaction with labeled angles θ and energy levels E
</details>

## 18.8 Zusammenfassung

**Elektrisches Feld** Ein Ansatz zur Erklärung der elektrostatischen Kraft zwischen zwei Ladungen ist die Annahme, dass jede Ladung ein elektrostatisches Feld im sie umgebenden Raum aufbaut. In diesem Bild wird die auf eine Ladung wirkende elektrostatische Kraft verursacht durch das am Ort der Ladung wirkende elektrische Feld der jeweils anderen Ladung.

**Definition des elektrischen Felds** Das elektrische Feld $\vec { E }$ in einem Raumpunkt ist definiert durch die elektrostatische Kraft ${ \vec { F } } ,$ die auf eine positive Probeladung $q _ { 0 }$ in diesem Punkt wirken würde:

$$
\vec {E} = \frac {\vec {F}}{q _ {0}}. \tag {18.1}
$$

**Elektrische Feldlinien** Elektrische Feldlinien sind ein Mittel zur Veranschaulichung der räumlichen Verteilung von Richtung und Betrag eines elektrischen Felds. Der Vektor des elektrischen Felds ist in jedem Punkt tangential zur Feldlinie durch diesen Punkt. Die Dichte der Feldlinien in einem Raumbereich ist proportional zum Betrag des elektrischen Felds in diesem Bereich. Feldlinien beginnen bei positiven Ladungen und enden bei negativen Ladungen.

**Feld einer Punktladung** Das elektrische Feld $\vec { E }$ einer Punktladung $q$ in einem Raumpunkt mit dem Abstand $r$ von der Ladung ist gegeben durch

$$
E = \frac {1}{4 \pi \varepsilon_ {0}} \frac {| q |}{r ^ {2}}. \tag {18.3}
$$

Dieses Feld ist radial von der Ladung weg gerichtet, wenn die Ladung positives Vorzeichen hat, anderenfalls zeigt es direkt auf die Punktladung.

**Feld eines elektrischen Dipols** Ein elektrischer Dipol besteht aus zwei Ladungen vom gleichen Betrag $q ,$ aber mit entgegengesetztem Vorzeichen, die in einem kleinen Abstand $d$ voneinander fixiert sind. Das **Dipolmoment** $\vec { p }$ eines Dipols hat den Betrag qd, liegt als Vektor auf der Verbindungslinie der beiden Ladungen und zeigt von der negativen zur positiven Ladung. Der Betrag des von einem elektrischen Dipol in einem weit entfernten Punkt auf der

Dipolachse (der Verbindungslinie der beiden Ladungen) erzeugten elektrischen Felds ist gegeben durch

$$
E = \frac {1}{2 \pi \varepsilon_ {0}} \frac {p}{z ^ {3}}. \tag {18.9}
$$

Darin bezeichnet $z$ die Entfernung zwischen dem fragli chen Punkt und dem Mittelpunkt des Dipols.

**Elektrisches Feld einer kontinuierlichen Ladungsverteilung** Beim allgemeinen Verfahren zur Berechnung des elektrischen Felds einer kontinuierlichen Ladungsverteilung denkt man sich die Gesamtladung der Verteilung in differenzielle Ladungselemente zerlegt, behandelt diese als Punktladungen und integriert dann die differenziellen Feldbeiträge der einzelnen Ladungselemente.

**Kraft auf eine Punktladung im elektrischen Feld** Bringt man eine Punktladung $q$ in ein von anderen Ladungen erzeugtes elektrisches Feld $\vec { E } ,$ so wirkt auf die Ladung die elektrostatische Kraft

$$
\vec {F} = q \vec {E}. \tag {18.24}
$$

Diese Kraft hat dieselbe Richtung wie $\vec { E } ,$ wenn die Ladung positiv ist, anderenfalls ist sie antiparallel zur Feldrichtung.

**Dipol im elektrischen Feld** Auf einen elektrischen Dipol mit dem Dipolmoment $\vec { p }$ wirkt in einem elektrischen Feld $\vec { E }$ ein Drehmoment $\vec { \tau } ,$ das gegeben ist durch

$$
\vec {\tau} = \vec {p} \times \vec {E}. \tag {18.28}
$$

Mit der Orientierung des Dipols relativ zur Feldrichtung ist eine potenzielle Energie U verbunden mit

$$
U = - \vec {p} \cdot \vec {E}. \tag {18.32}
$$

Diese potenzielle Energie ist definitionsgemäß null, wenn Dipolmoment $\vec { p }$ und Feld $\vec { E }$ senkrecht aufeinander stehen; sie wird minimal $\left( U = - p E \right)$ , wenn die beiden Vektoren parallel, und maximal $( U = p E )$ , wenn sie einander entgegengesetzt gerichtet sind.

451

---

18 Elektrische Felder

## 18.9 Fragen

**1.** Abbildung 18.F1 zeigt drei elektrische Feldlinien. Welche Richtung hat die elektrostatische Kraft auf eine positive Probeladung (a) im Punkt A, (b) im Punkt B? (c) In welchem Punkt (A oder B) wird die Beschleunigung der Probeladung größer sein, wenn diese losgelassen wird?

![](../../raw/pages_0449-0480/images/page_465_image_3.jpg)

<details>
<summary>text_image</summary>

y
A
x
B
</details>

Abb. 18.F1

**2.** Abbildung 18.F2a zeigt zwei geladene Teilchen. (a) In welchem Bereich auf der Verbindungsachse der Teilchen gibt es einen – nicht im Unendlichen liegenden – Punkt, in dem das resultierende elektrische Feld der beiden Ladungen null ist: links von den beiden Teilchen, rechts davon oder zwischen ihnen? (b) Gibt es einen – nicht im Unendlichen liegenden – Punkt außerhalb der Verbindungsachse, in dem das resultierende Feld verschwindet?

![](../../raw/pages_0449-0480/images/page_465_image_6.jpg)

![](../../raw/pages_0449-0480/images/page_465_image_7.jpg)

Abb. 18.F2

Fragen 2 und 3.

**3.** Abbildung 18.F2b zeigt ein Elektron und zwei Protonen, die in gleichen Abständen auf einer Achse liegen. In welchem Bereich der Achse gibt es einen – nicht im Unendlichen liegenden – Punkt, an welchem das resultierende elektrische Feld null ist: links von allen Teilchen, rechts davon, zwischen den beiden Protonen oder zwischen dem Elektron und dem benachbarten Proton?
**4.** Abbildung 18.F4 zeigt zwei quadratische Anordnungen geladener Teilchen. Die beiden Quadrate, deren Mittelpunkte im Punkt P zusammenfallen, sind gegeneinander gedreht. Die Abstände der Teilchen entlang der Kanten betragen jeweils entweder d oder $d / 2 .$ Ermitteln Sie Betrag und Richtung des effektiven resultierenden Felds im Punkt P.

![](../../raw/pages_0449-0480/images/page_465_image_13.jpg)

<details>
<summary>text_image</summary>

+6q
-2q
+3q
-3q
+2q
P
-q
-q
-q
+2q
-3q
+3q
-2q
+6q
</details>

Abb. 18.F4

**5.** In Abb. 18.F5 sind zwei Teilchen mit der Ladung −q symmetrisch zur y-Achse angeordnet. Jedes der beiden Teilchen erzeugt im Punkt P auf der y-Achse ein elektrisches Feld. (a) Sind die Beträge dieser beiden Felder im Punkt P einander gleich? (b) Zeigen die Felder auf die sie jeweils erzeugende Ladung hin oder von ihr weg? (c) Ist der Betrag des resultierenden elektrischen Felds im Punkt P gleich der Summe der Beträge E der beiden Teilfelder, also gleich 2E? (d) Löschen sich die x-Komponenten der beiden Teilfelder aus oder verstärken sie sich? (e) Löschen sich die y-Komponenten der beiden Teilfelder aus oder verstärken sie sich? (f ) Hat das resultierende Feld im Punkt P die Richtung der sich auslöschenden oder der sich verstärkenden Komponenten? (g) Welche Richtung hat das resultierende Feld?

![](../../raw/pages_0449-0480/images/page_465_image_16.jpg)

<details>
<summary>text_image</summary>

y
P
-q
-q
x
d
d
</details>

Abb. 18.F5

**6.** Drei mit gleichem Krümmungsradius kreisförmig gebogene, nichtleitende Stäbe sind homogen geladen. Stab A hat die Ladung +2Q und spannt einen Winkel von 30° auf, Stab B trägt eine Ladung +6Q und spannt einen Winkel von $9 0 ^ { \circ }$ auf, Stab C schließlich trägt die Ladung +4Q und spannt einen Winkel von 60° auf. Ordnen Sie die Stäbe nach dem Wert ihrer linearen Ladungsdichte.
**7.** Der in Abb. 18.F7a abgebildete, kreisförmig gebogene Plastikstab trägt eine homogen verteilte Ladung +Q und erzeugt in seinem Krümmungsmittelpunkt (dem Ursprung des Koordinatensystems) ein elektrisches Feld vom Betrag E. Wie in den Abb. 18.F7b, c und d dargestellt, fügt man nacheinander weitere zu einem Viertelkreis gebogene

![](../../raw/pages_0449-0480/images/page_465_image_21.jpg)

<details>
<summary>text_image</summary>

y
x
</details>

(a)

![](../../raw/pages_0449-0480/images/page_465_image_23.jpg)

<details>
<summary>text_image</summary>

y
x
</details>

(b)

![](../../raw/pages_0449-0480/images/page_465_image_25.jpg)

<details>
<summary>text_image</summary>

y
x
</details>

(c)

![](../../raw/pages_0449-0480/images/page_465_image_27.jpg)

<details>
<summary>natural_image</summary>

Simple geometric diagram showing a circle centered at the origin with x and y axes (no labels or text)
</details>

(d)

Abb. 18.F7

452

---

18.9 Fragen

18

und ebenfalls jeweils mit der Ladung +Q geladene Stäbe hinzu, bis ein vollständiger Kreis entstanden ist. Betrachten Sie zusätzlich noch eine weitere Anordnung (e), die sich von (d) nur dadurch unterscheidet, dass der Stab im vierten Quadranten die negative Ladung −Q trägt. Ordnen Sie diese fünf Fälle nach dem Betrag des im Ursprung jeweils erzeugten elektrischen Felds.

**8.** Wie in Abb. 18.F8 dargestellt bewegt sich ein Elektron e durch eine kleine Öffnung in der Platte A hindurch auf die Platte B zu. Ein homogenes elektrisches Feld im Raum zwischen den beiden Platten bremst das Elektron, ohne es abzulenken. (a) Welche Richtung hat das Feld? (b) Vier weitere Teilchen bewegen sich ebenfalls, wie in der Abbildung dargestellt, durch kleine Öffnungen der Platten in den Plattenzwischenraum hinein. Drei von ihnen tragen die Ladun-$\mathrm { g e n }   +   q _ { 1 } , + q _ { 2 }$ und $- q _ { 3 } ,$ Das vierte Teilchen, mit n bezeichnet, ist ein Neutron und verhält sich elektrisch neutral. Wie ändert sich die Teilchengeschwindigkeit in jedem dieser vier Fälle beim Eintritt in das elektrische Feld?

![](../../raw/pages_0449-0480/images/page_466_image_4.jpg)

<details>
<summary>text_image</summary>

e
+q₁
n
A
B
+q₂
-q₃
</details>

Abb. 18.F8

**9.** Abbildung 18.F9 zeigt die Flugbahn eines negativ geladenen Teilchens 1 durch einen rechteckigen Bereich, in dem ein homogenes elektrisches Feld herrscht. Das Teilchen wird in der Papierebene nach oben abgelenkt. (a) Ist das Feld nach oben, unten, links oder rechts gerichtet? (b) Drei weitere geladene Teilchen nähern sich wie dargestellt dem Feldbereich. Welche von ihnen werden nach oben, welche nach unten abgelenkt?

![](../../raw/pages_0449-0480/images/page_466_image_7.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph LR
  A["3"] --> B["Output 1"]
  C["4"] --> B
  D["2"] --> E["Output 2"]
  B --> F["Transition Path"]
  E --> F
  F --> G["Final Output"]
```
</details>

Abb. 18.F9

**10.** (a) Betrachten Sie noch einmal die Situation von Kontrollfrage 5: Ist die vom Feld am Dipol verrichtete Arbeit positiv, negativ oder null, wenn der Dipol von der Orientierung 1 in die Orientierung 2 gedreht wird? (b) Ist die vom Feld am Dipol verrichtete Arbeit größer, kleiner oder die gleiche wie in Frage (a), wenn man den Dipol aus der Orientierung 1 in die Orientierung 4 dreht?
**11.** Vier verschiedene Orientierungen eines elektrischen Dipols in einem elektrischen Feld haben die potenziellen Energien $(1) $- 5 U _ { 0 } ,$ (2) $- 7 U _ { 0 } ,$ (3) $3 U _ { 0 }$$ und (4) $5 U _ { 0 } ,$ wobei $U _ { 0 }$ positiv sei. Ordnen Sie die vier Fälle nach (a) der Grö- ße des Winkels zwischen dem Dipolmoment $\vec { p }$ und dem elektrischen Feld E⃗, (b) dem Betrag des auf den Dipol wirkenden Drehmoments.

**12.** Läuft man an einem trockenen Tag über bestimmte Arten von Teppichen und greift dann nach einem metallenen Türgriff oder – um mehr Spaß zu haben – nach jemandes Nacken, so springt oft ein Funke über. Wie entsteht dieser Funke? (Man kann die Intensität – die Helligkeit und das Geräusch – der Entladung vergrößern, wenn man statt der Hand einen Finger oder einen scharfkantigen Metallgegenstand, beispielsweise einen Schlüssel, verwendet. Ahnen Sie, warum?)
**13.** Abbildung 18.F13 zeigt drei Anordnungen elektrischer Feldlinien. Ein Proton wird jeweils bei Punkt A aus der Ruhe losgelassen und bis Punkt B durch das elektrische Feld beschleunigt. Die Punkte A und B haben in allen drei Anordnungen denselben Abstand voneinander. Ordnen Sie die Anordnungen in absteigender Reihenfolge nach dem Impuls des Protons am Punkt B.

![](../../raw/pages_0449-0480/images/page_466_image_15.jpg)

(a)

![](../../raw/pages_0449-0480/images/page_466_image_17.jpg)

(b)

![](../../raw/pages_0449-0480/images/page_466_image_19.jpg)

(c)

Abb. 18.F13

**14.** Abbildung 18.F14 zeigt vier Situationen, in denen vier geladene Teilchen in gleichen Abständen links und rechts von einem zentralen Punkt liegen; ihre Ladungen sind angegeben. Ordnen Sie die Situationen in absteigender Reihenfolge nach dem Betrag des resultierenden elektrischen Felds am zentralen Punkt.

![](../../raw/pages_0449-0480/images/page_466_image_23.jpg)

Abb. 18.F14

**15.** Abbildung 18.F15 zeigt zwei identische kreisförmige, nichtleitende Ringe, deren Mittelpunkte auf einer Linie senkrecht zur Ringebene liegen. Die Ringe tragen eine homogen über den gesamten Umfang verteilte Ladung und erzeugen daher jeweils ein elektrisches Feld an allen Punkten auf der Linie. Gegeben sind drei Situationen, in denen die Ladungen auf den Ringen A und B (1) $q _ { 0 }$ und $q _ { 0 } , ( 2 )   -   q _ { 0 }$ und $- q _ { 0 }$ und $( 3 ) - q _ { 0 }$ und $q _ { 0 }$ betragen. Ordnen Sie die Situationen in absteigender Reihenfolge nach der resultierenden elektrischen Feldstärke an dem Punkt (a) $\mathrm { P } _ { 1 }$ auf halber Strecke zwischen den Ringen, (b) $\mathrm { P } _ { 2 }$ im Zentrum von Ring B und (c) $\mathrm { P } _ { 3 }$ rechts von Ring B.

453

---

18 Elektrische Felder

![](../../raw/pages_0449-0480/images/page_467_image_1.jpg)

<details>
<summary>text_image</summary>

P₁
Ring A
P₂
Ring B
P₃
</details>

Abb. 18.F15

**16.** Abbildung 18.F16 zeigt zwei Scheiben und einen flachen Ring mit jeweils gleicher Ladung Q. Ordnen Sie die Objekte in absteigender Reihenfolge nach der elektrischen Feldstärke an den Punkten P (die immer in derselben vertikalen Höhe liegen).

![](../../raw/pages_0449-0480/images/page_467_image_4.jpg)

(a)

![](../../raw/pages_0449-0480/images/page_467_image_6.jpg)

<details>
<summary>text_image</summary>

P
2R
</details>

(b)

![](../../raw/pages_0449-0480/images/page_467_image_8.jpg)

<details>
<summary>text_image</summary>

P
R
2R
</details>

(c)

Abb. 18.F16

**17.** Wenn drei elektrische Dipole nebeneinander liegen, spürt jeder von ihnen die elektrischen Felder der beiden anderen; als Folge besitzt das System aus drei Dipolen eine bestimmte potenzielle Energie. Abbildung 18.F17 zeigt zwei mögliche derartige Anordnungen. Die Dipole haben alle denselben Betrag des elektrischen Dipolmoments und die Abstände zwischen benachbarten Dipolen sind gleich. Welcher Anordnung besitzt die größere potenzielle Energie?

![](../../raw/pages_0449-0480/images/page_467_image_12.jpg)

(a)

![](../../raw/pages_0449-0480/images/page_467_image_14.jpg)

(b)

Abb. 18.F17

**18.** Abbildung 18.F18 zeigt drei Stäbe mit derselben Ladung Q, die gleichförmig über ihre gesamte Länge verteilt ist. Die Stäbe a (Länge L) und b (Länge $L / 2 )$ sind gerade und die Punkte P liegen jeweils auf der Höhe ihrer Mittelpunkte. Stab c (Länge $L / 2 )$ ist zu einem geschlossenen Kreis um Punkt P gebogen. Ordnen Sie die Stäbe in absteigender Reihenfolge nach der elektrischen Feldstärke an den Punkten P.

![](../../raw/pages_0449-0480/images/page_467_image_18.jpg)

<details>
<summary>text_image</summary>

P
L
P
L/2
L/2
P
</details>

(a)

(b)

(c)

Abb. 18.F18

**19.** Abbildung 18.F19 zeigt fünf Protonen, die in einem homogenen elektrischen Feld mit den gezeigten Anfangsgeschwindigkeiten (Betrag und Richtung) gestartet werden. Ordnen Sie die Protonen in absteigender Reihenfolge nach dem Betrag ihrer Beschleunigungen aufgrund des Felds.

![](../../raw/pages_0449-0480/images/page_467_image_24.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph LR
  A["E"] --> B["3 m/s"]
  B --> C["a 10 m/s"]
  C --> D["b"]
  D --> E["c 16 m/s"]
  E --> F["5 m/s"]
  F --> G["d"]
  G --> H["7 m/s"]
  H --> I["e"]
```
</details>

454
