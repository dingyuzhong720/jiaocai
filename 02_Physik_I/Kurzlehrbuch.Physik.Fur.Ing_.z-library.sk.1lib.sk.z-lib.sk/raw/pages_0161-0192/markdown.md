![](images/page_160_image_2.jpg)

<details>
<summary>text_image</summary>

Achse
Spindel
z
</details>

(a)

![](images/page_160_image_4.jpg)

(b)

![](images/page_160_image_6.jpg)

<details>
<summary>text_image</summary>

Achse
z
ω
</details>

(c)

## Abb. 6.5

(a) Eine Schallplatte dreht sich um eine Achse, die mit der Spindel des Plattentellers zusammenfällt. (b) Die Winkelgeschwindigkeit der rotierenden Schallplatte kann als Vektor ω⃗ dargestellt werden, welcher auf der Drehachse liegt und in diesem Fall nach unten zeigt. (c) Die Richtung des Vektors ω⃗ ermitteln wir mithilfe der Rechte-Hand-Regel: Die Finger der rechten Hand krümmen sich um die Drehachse und zeigen in Drehrichtung. Dann weist ω⃗ in die gleiche Richtung wie der ausgestreckte Daumen.

Umdrehungen pro Minute) im Uhrzeigersinn auf einem Plattenteller dreht. Die Winkelgeschwindigkeit lässt sich als Vektor ω⃗ darstellen, der in Richtung der Drehachse zeigt (Abb. 6.5b). Die Länge des Vektors geben wir auf einer geeigneten Skala an (z. B. 1 mm je 1 U/min). Zur Festlegung der Richtung von ω⃗ verwenden wir die **Rechte-Hand-Regel**: Krümmen Sie die Finger Ihrer rechten Hand um die Drehachse des rotierenden Körpers (Abb. 6.5c), wobei die Finger in die Drehrichtung weisen. Dann strecken Sie Ihren Daumen aus; er zeigt in die gleiche Richtung wie der Vektor der Winkelgeschwindigkeit. Dreht sich die Schallplatte in die entgegengesetzte Richtung wie in Abb. 6.5a, dann zeigt ω⃗ nach oben, wovon Sie sich mithilfe Ihrer rechten Hand leicht überzeugen können. Auf diese Weise gibt der Vektor sowohl die „Stärke“ der Rotation also auch die Lage der Drehachse an, die Definition ist also tatsächlich sinnvoll.

Winkelgrößen als Vektoren aufzufassen ist etwas gewöhnungsbedürftig. Instinktiv erwarten wir, dass sich ein Körper in Richtung des Geschwindigkeitsvektors bewegt, was hier nicht der Fall ist: Der starre Körper rotiert um die Richtung dieses Vektors. Soweit es reine Rotationen betrifft, definiert der Vektor ω⃗ die Drehachse, nicht die Bewegungsrichtung. Damit definiert er, wie gesagt, die Rotationsbewegung vollständig. Außerdem erfüllt er alle in der Vektorrechnung gültigen Regeln (vgl. Anhang D). Dies gilt ebenfalls für den Vektor der Winkelbeschleunigung α⃗. Zur Unterscheidung von gewöhnlichen Vektoren bezeichnet man diese Größen auch als axiale Vektoren.

In diesem Kapitel sprechen wir nur über Rotationen um eine festgelegte Achse. In diesen Fällen benötigen wir die Vektordarstellung von Winkelgeschwindigkeit und -beschleunigung nicht unbedingt, sondern wir können beide Größen durch ihre Beträge ω und α darstellen und die Richtung mit einem Minuszeichen (im Uhrzeigersinn) oder Pluszeichen (entgegengesetzt dazu) angeben. Das Pluszeichen wird meist nicht ausgeschrieben.

Vorsicht geboten ist bei der Behandlung des Drehwinkels: Er darf (falls er nicht sehr klein ist) nicht als Vektor betrachtet werden, obwohl wir ihm einen Betrag und eine Richtung zuordnen können, wie wir es in Abb. 6.5 für die Winkelgeschwindigkeit getan haben. Der Grund dafür ist folgender: Damit man eine Größe als Vektor darstellen kann, muss sie auch die Gesetze der Vektoraddition befolgen. Eines von ihnen besagt, dass sich die Reihenfolge, in der man zwei Vektoren addiert, nicht auf das Ergebnis auswirken darf. Auf den Drehwinkel trifft das nicht zu, wie an einem Beispiel gezeigt werden soll.

Betrachten wir Abb. 6.6. Ein waagerecht liegendes Buch wird zweimal um je 90° gedreht, erst in der Reihenfolge gemäß Abb. 6.6a, dann in der Reihenfolge gemäß Abb. 6.6b. Die Drehwinkel sind also gleich, die Reihenfolgen verschieden. Wie Sie sich überzeugen können, erhält man zwei verschiedene Orientierungen des Buchs. Die Addition zweier Drehwinkel hängt demnach von der Reihenfolge der Summanden ab, weshalb es sich nicht um Vektoren handeln kann.

![](images/page_160_image_15.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph LR
  subgraph a["(a)"]
  A["Block with X, Y, Z axes"] --> B["Physical Surface"]
  end
  subgraph b["(b)"]
  B --> C["Physical Surface"]
  end
```
</details>

Abb. 6.6

Ausgehend von der waagerechten Anfangslage (oben) wird ein Buch zweimal um 90° gedreht, und zwar (a) erst um die waagerechte x-Achse, dann um die senkrechte y-Achse und (b) in umgekehrter Reihenfolge.

## 6.2 Rotation mit konstanter Winkelbeschleunigung

![](images/page_161_image_2.jpg)

## Lernziele

Nach dem Durcharbeiten dieses Abschnitts sollten Sie in der Lage sein, . . .

• die Beziehungen zwischen Winkelposition, Drehwinkel, Winkelgeschwindig keit, Winkelbeschleunigung und Zeit für Bewegungen mit konstanter Winkelbeschleunigung anzugeben und anzuwenden.

![](images/page_161_image_6.jpg)

## Schlüsselideen

• Der Fall konstanter Winkelbeschleunigung $( \alpha = \mathrm { c o n s t . } )$ ist ein wichtiger Spezialfall der Rotationsbewegung. Die zugehörigen kinematischen Gleichungen lauten

$$
\begin{array}{l} \omega = \omega_ {0} + \alpha t, \\ \theta - \theta_ {0} = \omega_ {0} t + \frac {1}{2} \alpha t ^ {2}, \\ \omega^ {2} = \omega_ {0} ^ {2} + 2 \alpha (\theta - \theta_ {0}), \\ \theta - \theta_ {0} = \frac {1}{2} (\omega_ {0} + \omega) t, \\ \theta - \theta_ {0} = \omega t - \frac {1}{2} \alpha t ^ {2}. \\ \end{array}
$$

## 6.2.1 Rotation mit konstanter Winkelbeschleunigung

Bewegungen mit konstanter linearer Beschleunigung (z. B. das Fallen eines Körpers) sind wichtige Spezialfälle der reinen Translation. Tabelle 1.1 fasste einige der hierfür geltenden Gleichungen zusammen.

Bewegungen mit konstanter Winkelbeschleunigung sind analog Spezialfälle der reinen Rotation, für die ähnliche Gleichungen Gültigkeit besitzen. Wir werden diese Beziehungen hier nicht herleiten, sondern sie lediglich den Gleichungen für die Translation gegenüberstellen, wobei die linearen Größen gegen die Winkelgrößen ausgetauscht werden. Beide Sätze von Gleichungen finden Sie in Tab. 6.1 (Gln. 1.9 bis 1.16 sowie Gln. 6.9 bis 6.13).

Wie Sie sich erinnern werden, sind die Gln. 1.9 und 1.13 die grundlegenden Be ziehungen für Bewegungen mit konstanter linearer Beschleunigung. Alle anderen aufgeführten Zusammenhänge lassen sich daraus herleiten. In ähnlicher Weise grundlegend sind die Gln. 6.9 und 6.10 für Bewegungen mit konstanter Winkelbeschleunigung. Um eine Aufgabe zu lösen, die eine solche Bewegung beinhaltet, brauchen Sie nur diejenige Gleichung aus der Liste auszuwählen, deren Unbekann te der in der Aufgabe gefragten Variable entspricht. Sie sollten allerdings versuchen, mit den Gln. 6.9 und 6.10 auszukommen, wie es in Beispielaufgabe 6.4 im Übungsbuch vorgeführt wird.

TABELLE 6.1:

Bewegungsgleichungen für konstante Linear- bzw. Winkelbeschleunigung.

<table><tr><td>Gl.</td><td>Gleichung für beschleunigte Translation</td><td colspan="2">unbekannte Variable</td><td>Gleichung für beschleunigte Rotation</td><td>Gl.</td></tr><tr><td>1.9</td><td> $\nu = \nu_0 t + at$ </td><td> $x - x_0$ </td><td> $\theta - \theta_0$ </td><td> $\omega = \omega_0 + \alpha t$ </td><td>6.9</td></tr><tr><td>1.13</td><td> $x - x_0 = \nu_0 t + \frac{1}{2} at^2$ </td><td> $\nu$ </td><td> $\omega$ </td><td> $\theta - \theta_0 = \omega_0 t + \frac{1}{2} \alpha t^2$ </td><td>6.10</td></tr><tr><td>1.14</td><td> $\nu^2 = \nu_0^2 + 2a(x - x_0)$ </td><td> $t$ </td><td> $t$ </td><td> $\omega^2 = \omega_0^2 + 2\alpha(\theta - \theta_0)$ </td><td>6.11</td></tr><tr><td>1.15</td><td> $x - x_0 = \frac{1}{2} (\nu_0 + \nu)t$ </td><td> $a$ </td><td> $\alpha$ </td><td> $\theta - \theta_0 = \frac{1}{2} (\omega_0 + \omega)t$ </td><td>6.12</td></tr><tr><td>1.16</td><td> $x - x_0 = \nu t - \frac{1}{2} at^2$ </td><td> $\nu_0$ </td><td> $\omega_0$ </td><td> $\theta - \theta_0 = \omega t - \frac{1}{2} \alpha t^2$ </td><td>6.13</td></tr></table>

## KONTROLLFRAGE 2

Die Winkelposition θ(t) eines rotierenden Körpers sei gegeben durch (a) $\theta = 3 t { - 4 } ,$ (b) $\theta = - 5 \bar { t ^ { 3 } } + 4 t ^ { 2 } + 6 , ( \mathrm { c } ) \theta = 2 / t ^ { 2 } - 4 / t .$ und (d) $\theta = 5 t ^ { 2 } - 3$ . Auf welche dieser Situationen können die in Tab. 6.1 angegebenen Gleichungen angewendet werden?

## 6.3 Beziehungen zwischen den Variablen für lineare Bewegung und Rotation

## Lernziele

Nach dem Durcharbeiten dieses Abschnitts sollten Sie in der Lage sein, . . .

für einen starren Körper, der sich um eine feste Achse dreht, Beziehungen zwischen den Winkelvariablen des Körpers (Winkelposition, Winkelgeschwindigkeit und Winkelbeschleunigung) und den linearen Variablen (Position, Geschwindigkeit und Beschleunigung) eines Teilchens an einer beliebigen Position innerhalb des Körpers anzugeben,
tangentiale und radiale Beschleunigungen zu unterscheiden und beide sowohl für eine Erhöhung als auch für eine Abnahme der Winkelgeschwindigkeit in einer Skizze eines um eine Achse rotierenden Körpers für ein beliebiges Teilchen innerhalb des Körpers einzeichnen zu können.

![](images/page_162_image_11.jpg)

## Schlüsselideen

• Ein Punkt in einem starren rotierenden Körper im senkrechten Abstand r von der Drehachse bewegt sich auf einer Kreisbahn mit Radius r um diese Achse. Wenn der Körper sich um einen Winkel θ dreht, bewegt sich der Punkt entlang eines Kreisbogens der Länge

$$
s = \theta r \quad (\theta \text {im Bogenma} \beta)
$$

• Die lineare Geschwindigkeit v⃗ eines solchen Punkts verläuft tangential zu diesem Kreis; der Betrag v seiner linearen Geschwindigkeit ist

$$
\nu = \omega r \quad (\omega \text {im Bogenma} \beta),
$$

![](images/page_162_image_17.jpg)

wobei ω die Winkelgeschwindigkeit (in rad/s) des Körpers und damit auch des Punkts ist.

• Die lineare Beschleunigung a⃗ des Punkts besitzt sowohl tangentiale als auch radiale Komponenten. Die tangentiale Komponente ist

$$
\alpha_ {\mathrm{t}} = \alpha r \qquad (\text {Bogenma} \beta),
$$

wobei α der Betrag der Winkelbeschleunigung (in rad/s<sup>2</sup>) des Körpers ist. Die radiale Komponente von a⃗ ist

$$
a _ {\mathrm{r}} = \frac {\nu^ {2}}{r} = \omega^ {2} r \qquad (\text {Bogenmaß}).
$$

• Bei einer gleichförmigen Kreisbewegung ist die Periode T der Bewegung für den Punkt und den Körper

$$
T = \frac {2 \pi r}{\nu} = \frac {2 \pi}{\omega} \qquad (\text {Bogenmaß}).
$$

## 6.3.1 Beziehungen zwischen den Variablen für lineare Bewegung und Rotation

In Abschn. 1.10 diskutierten wir die gleichförmige Kreisbewegung: Ein Teilchen bewegt sich mit der konstanten Geschwindigkeit v auf einer Kreisbahn um eine Achse. Rotiert ein starrer Körper, etwa ein Karussell, um eine Achse, so beschreibt jedes seiner Teilchen eine derartige Kreisbahn. Da die Teilchen unbeweglich miteinander verbunden sind, benötigen sie für einen vollständigen Umlauf alle die gleiche Zeit; anders ausgedrückt, alle Teilchen bewegen sich mit gleicher Winkelgeschwindigkeit ω.

Je größer jedoch der Abstand eines Teilchens von der Drehachse ist, desto grö- ßer ist auch der Umfang seiner Kreisbahn – das bedeutet, umso größer muss seine lineare Geschwindigkeit v sein. Sie können diesen Zusammenhang nachprüfen, wenn Sie Karussell fahren: Gleichgültig, wie weit Ihr Platz von der Mitte des Karussells entfernt ist, Sie bewegen sich stets mit der gleichen Winkelgeschwindigkeit. Ihre lineare Geschwindigkeit nimmt hingegen merklich zu, wenn Sie nach außen rücken.

Häufig benötigt man Beziehungen zwischen den Variablen s, v und a für die lineare Bewegung eines Teilchens innerhalb eines rotierenden Körpers und den Variablen θ, ω und α für die Rotation des gesamten Körpers. Der Zusammenhang zwischen beiden Variablensätzen ist durch r gegeben, den senkrechten (d. h. entlang einer Senkrechten zur Achse gemessenen) Abstand des betreffenden Punkts von der Rotationsachse. Gleichzeitig ist r der Radius der Kreisbahn, die das einzelne Teilchen um die Achse beschreibt.

![](images/page_163_image_5.jpg)

<details>
<summary>text_image</summary>

Kreisbahn
von P
Dreh-
achse
P
y
x
r
v
</details>

(a)

## Der Ort

Überstreicht die Bezugslinie eines starren Körpers einen Drehwinkel θ, so bewegt sich ein Punkt im Abstand r von der Drehachse um eine Strecke s entlang eines Kreisbogens; s ist gegeben durch Gl. 6.1:

$$
s = \theta r. \tag {6.14}
$$

Vorsicht: Diese Beziehung zwischen einer linearen und einer Rotationsvariablen gilt nur, wenn der Winkel θ in Bogenmaß angegeben wird. (Tatsächlich ist Gl. 6.14 die Definition der Winkelmessung in Bogenmaß!)

![](images/page_163_image_11.jpg)

<details>
<summary>text_image</summary>

y
P
a_t
a_r
Drehachse
x
</details>

(b)

## Die Geschwindigkeit

Die Ableitung von Gl. 6.14 nach der Zeit (bei konstantem r) liefert

$$
\frac {\mathrm{d} s}{\mathrm{d} t} = \frac {\mathrm{d} \theta}{\mathrm{d} t} r.
$$

Wie Sie sofort bemerken werden, ist ds∕dt der Betrag der linearen Geschwindig keit des betrachteten Punkts, und $\mathrm { d } \theta / \mathrm { d } t$ ist die Winkelgeschwindigkeit ω des rotierenden Körpers. Also gilt

$$
\nu = \omega r. \tag {6.15}
$$

Der rotierende Körper aus Abb. 6.2 von oben im Querschnitt gesehen.
Jeder Punkt (z. B. P) bewegt sich auf einer Kreisbahn um die Drehachse. (a) Die lineare Geschwindig-
keit ⃗v jedes Punkts zeigt in Richtung der Tangente an die Kreisbahn in diesem Punkt. (b) Die lineare Beschleunigung eines Punkts hat in der Regel zwei Komponenten, eine radiale $( a _ { \mathrm { r } } )$ und eine tangentiale $( a _ { \mathrm { t } } )$

Auch hier ist Vorsicht geboten: Die Winkelgeschwindigkeit ω ist in Bogenmaß anzugeben.

Gleichung 6.15 besagt Folgendes: Während die Winkelgeschwindigkeit ω aller Punkte innerhalb eines starren Körpers gleich ist, nimmt die lineare Geschwindigkeit v mit dem Abstand r von der Drehachse zu. Abbildung 6.7a führt Ihnen vor Augen, dass die lineare Geschwindigkeit stets tangential zur Kreisbahn des jeweiligen Punkts gerichtet ist.

Ist die Winkelgeschwindigkeit ω eines starren Körpers konstant, so ist gemäß Gl. 6.15 auch die lineare Geschwindigkeit jedes seiner Punkte konstant. Das bedeutet, alle Punkte bewegen sich gleichförmig auf Kreisbahnen. Die Periode T der Kreisbewegung jedes einzelnen Punkts und des starren Körpers insgesamt ist gegeben durch Gl. 1.41:

$$
T = \frac {2 \pi r}{\nu}. \tag {6.16}
$$

In Worten besagt diese Gleichung: Die Zeit für einen vollständigen Umlauf eines Punkts ist gegeben durch die Länge der entsprechenden Kreisbahn 2πr geteilt durch die Geschwindigkeit, mit der diese Strecke zurückgelegt wird. Setzen wir v aus Gl. 6.15 ein und kürzen $r ,$ so ergibt sich

$$
T = \frac {2 \pi}{\omega}. \tag {6.17}
$$

Diese (wieder nur in Bogenmaß gültige!) Gleichung besagt, dass die Zeit für einen Umlauf gegeben ist durch den Drehwinkel $2 \pi ,$ der dabei überstrichen wird, geteilt durch die Winkelgeschwindigkeit, mit welcher der Drehwinkel durchlaufen wird.

## Die Beschleunigung

Die Ableitung von Gl. 6.15 nach der Zeit (wiederum bei konstantem r) liefert

$$
\frac {\mathrm{d} \nu}{\mathrm{d} t} = \frac {\mathrm{d} \omega}{\mathrm{d} t} r. \tag {6.18}
$$

Hier stoßen wir auf eine Schwierigkeit. In Gl. 6.18 steht der Ausdruck dv∕dt nur für den Teil der linearen Beschleunigung, der für die Änderung des Betrags v der linearen Geschwindigkeit ⃗v sorgt. Wie ⃗v selbst wirkt dieser Teil der Beschleunigung tangential zur Kreisbahn des fraglichen Punkts, weshalb wir ihn als tangentiale Komponente $a _ { \mathrm { t } }$ der linearen Beschleunigung bezeichnen:

$$
a _ {\mathrm{t}} = \alpha r \tag {6.19}
$$

mit $\alpha = \mathsf { d } \omega / \mathsf { d } t .$ (Die Winkelbeschleunigung α in Gl. 6.19 muss in Bogenmaß angegeben werden.)

Zusätzlich besitzt jedes Teilchen, das sich auf einer Kreisbahn bewegt, Gl. 1.40 zufolge eine radiale Komponente der linearen Beschleunigung $\alpha _ { \mathrm { r } } = \nu ^ { 2 } / r$ (radial zur Achse gerichtet). Diese Komponente ist für Änderungen der Richtung von $\vec { \nu }$ verantwortlich. Wir setzen v aus Gl. 6.15 ein und schreiben für die radiale Komponente:

$$
a _ {\mathrm{r}} = \frac {\nu^ {2}}{r} = \omega^ {2} r. \tag {6.20}
$$

Wie Abb. 6.7b veranschaulicht, besteht die lineare Beschleunigung eines Punkts innerhalb eines rotierenden starren Körpers im Allgemeinen also aus zwei Komponenten. Die radial nach innen gerichtete Komponente $a _ { \mathrm { r } }$ (Gl. 6.20) ist stets von null verschieden, wenn die Winkelgeschwindigkeit des Körpers von null verschieden ist. Die tangentiale Komponente $a _ { \mathrm { t } }$ (Gl. 6.19) ist von null verschieden, wenn die Winkelbeschleunigung von null verschieden ist.

## KONTROLLFRAGE 3

Eine Fliege sitzt auf dem Rand eines rotierenden Karussells. Die Winkelgeschwin digkeit des Systems Fliege–Karussell ist konstant. Ist (a) die Radialbeschleunigung und (b) die Tangentialbeschleunigung der Fliege verschieden von null? Sind (c) Radialbeschleunigung und (d) Tangentialbeschleunigung der Fliege verschieden von null, während das Karussell bremst?

## LÖSUNGSSTRATEGIEN

**Strategie 1: Einheiten für die Variablen der Rotation** Von Gl. 6.1 $( \theta = s / r )$ a n haben wir alle Winkelgrößen, die gemeinsam mit linearen Größen in Gleichungen auftreten, in Bogenmaß angegeben (Drehwinkel in Radiant bzw. rad, Winkelgeschwindigkeiten in rad/s oder rad/min, Winkelbeschleunigungen in rad $/ s ^ { 2 }$ oder rad/min<sup>2</sup>). Dies gilt insbesondere für die Gln. 6.14–6.15, 6.17, 6.19 und 6.20. Die einzigen Ausnahmen von dieser Forderung bilden Gleichungen, in denen ausschließlich winkelbezogene Größen auftreten, etwa die Gln. 6.9–6.13 in Tab. 6.1. Hier steht es Ihnen frei, Winkel in Grad oder Umdrehungen anzugeben statt in Bogenmaß, solange Sie die Einheiten konsistent verwenden.

Kommen in einer Gleichung Winkel in Bogenmaß vor, so müssen Sie die „dimensionslose“ Einheit rad während des Rechenwegs nicht unbedingt mitnehmen, wie es bei anderen Einheiten erforderlich ist – eigentlich ist der Winkel im Bogenmaß einfach nur eine Zahl. Orientieren Sie sich einfach am Kontext.

## 6.4 Die kinetische Energie der Rotation

![](images/page_165_image_5.jpg)

## Lernziele

Nach dem Durcharbeiten dieses Abschnitts sollten Sie in der Lage sein, . . .

• das Trägheitsmoment eines Teilchens für die Rotation um eine Achse zu bestimmen,
• das Trägheitsmoment eines Systems von Teilchen für die Rotation um eine gemeinsame Achse zu bestimmen,
• die kinetische Energie der Rotation eines Körpers aus seinem Trägheitsmoment und seiner Winkelgeschwindigkeit zu berechnen.

![](images/page_165_image_12.jpg)

## Schlüsselideen

• Die kinetische Energie eines starren Körpers, der um eine feste Achse rotiert, ist

$$
K = \frac {1}{2} I \omega^ {2} \qquad (\text {Bogenmaß}),
$$

wobei I das Trägheitsmoment des Körpers ist, das für ein System von diskreten Teilchen definiert ist durch

$$
I = \sum m _ {i} r _ {i} ^ {2}.
$$

## 6.4.1 Die kinetische Energie der Rotation

Das schnell rotierende Blatt einer Kreissäge besitzt infolge dieser Drehbewegung ganz ohne Zweifel kinetische Energie. Wie können wir diese Energie formulieren? Wenden wir die gewohnte Formel $\tilde { K } = { \textstyle { \frac { 1 } { 2 } } } m \nu ^ { 2 }$ auf das Sägeblatt als Ganzes an, so erhalten wir lediglich die kinetische Energie des Schwerpunkts – und diese ist gleich null.

Stattdessen müssen wir das Sägeblatt (und jeden anderen rotierenden starren Körper) als Anordnung von Teilchen mit verschiedenen Geschwindigkeiten betrachten. Wir können dann die kinetischen Energien aller Teilchen aufsummieren und erhalten daraus die kinetische Gesamtenergie des Körpers. Formal bedeutet dies

$$
K = \frac {1}{2} m _ {1} \nu_ {1} ^ {2} + \frac {1}{2} m _ {2} \nu_ {2} ^ {2} + \frac {1}{2} m _ {3} \nu_ {3} ^ {2} + \dots ,
$$

also

$$
K = \sum \frac {1}{2} m _ {i} v _ {i} ^ {2}, \tag {6.21}
$$

mit $m _ { i }$ als Masse der i-ten Teilchens und $\nu _ { i }$ als dessen Geschwindigkeit. Summiert wird über alle Teilchen, die der Körper enthält.

Bei der Anwendung von Gl. 6.21 haben wir ein wesentliches Problem: $\nu _ { i }$ ist nicht für alle Teilchen gleich groß. Die Lösung ist, v aus Gl. 6.15 $( \nu = \omega r )$ einzusetzen:

$$
K = \sum \frac {1}{2} m _ {i} (\omega r _ {i}) ^ {2} = \frac {1}{2} \left(\sum m _ {i} r _ {i} ^ {2}\right) \omega^ {2}, \tag {6.22}
$$

denn ω ist für alle Teilchen gleich.

Der Klammerausdruck auf der rechten Seite von Gl. 6.22 gibt an, wie die Masse des rotierenden Körpers um die Drehachse verteilt ist. Wir nennen diese Größe das **Trägheitsmoment** I des Körpers bezüglich der jeweiligen Achse. Für einen bestimmten starren Körper und eine bestimmte Achse ist I eine Konstante. (Ohne die Angabe dieser Achse ist ein Wert von I physikalisch sinnlos!)

Wir schreiben also für das Trägheitsmoment

$$
I = \sum m _ {i} r _ {i} ^ {2}. \tag {6.23}
$$

und setzen dies in Gl. 6.22 ein, wodurch sich die gesuchte Beziehung für die kinetische Energie ergibt:

$$
K = \frac {1}{2} I \omega^ {2}. \tag {6.24}
$$

Weil wir bei der Herleitung von Gl. 6.24 auf die Beziehung $\nu = \omega r$ zurückgegriffen haben, muss ω in Bogenmaß angegeben werden. Die SI-Einheit von I ist Kilogramm mal Quadratmeter $( \mathrm { k g } \cdot \mathrm { m } ^ { 2 } )$

Gleichung 6.24 gibt die kinetische Energie eines starren Körpers bei der reinen Rotation an und ist damit das Analogon zu der Beziehung $\bar { K } = { \textstyle \frac { 1 } { 2 } } M \nu _ { S } ^ { 2 }$ für die kinetische Energie eines starren Körpers bei der reinen Translation. In beiden Formeln findet sich der Faktor 1/2. An die Stelle der Masse M tritt in der Gleichung für die Rotation das Trägheitsmoment $I ,$ das die Masse und deren Verteilung in sich vereint. Schließlich enthalten beide Gleichungen eine quadratische Geschwindigkeit (der Translation bzw. Rotation). Die kinetische Energie der Translation unterscheidet sich nicht von der kinetischen Energie der Rotation – wir haben lediglich, in Abhängigkeit von der Bewegungsform, verschiedene Ausdrücke für dieselbe Energieform.

Wie bereits bemerkt, fließt in das Trägheitsmoment eines Körpers nicht nur seine Masse, sondern auch deren Verteilung ein. Ein Beispiel dafür, das Sie sofort nachvollziehen können, ist folgendes: Lassen Sie einen länglichen Gegenstand (eine Stange, einen Holzstab oder etwas Ähnliches) erst um seine Längs-, dann um seine Querachse rotieren (Abb. 6.8a bzw. b). Die Masse des Gegenstands ändert sich dabei offensichtlich nicht, aber mit Sicherheit empfinden Sie die erste Rotation als viel leichter. Die Masse befindet sich in diesem Fall näher an der Rotationsachse als im zweiten Fall. Folglich ist das Trägheitsmoment des Stabs bei der Rotation um die Längsachse deutlich kleiner als bei der Rotation um die Querachse. Je kleiner sein Trägheitsmoment ist, desto leichter lässt sich ein Körper drehen.

## KONTROLLFRAGE 4

Die nebenstehende Zeichnung zeigt drei kleine Kugeln, die sich um eine senkrechte Achse drehen. Gegeben ist jeweils der senkrechte Abstand zwischen der Achse und dem Mittelpunkt der Kugel. Ordnen Sie die Kugeln nach ihrem Trägheitsmoment bezüglich dieser Achse, beginnend mit dem größten Wert.

![](images/page_166_image_18.jpg)

<details>
<summary>text_image</summary>

(a)
Drehachse
(b)
</details>

Abb. 6.8

Ein langer Stab lässt sich viel leichter um seine Längsachse drehen (a) als um seine Querachse (b). Der Grund dafür ist, dass die Masse in (a) näher an der Drehachse liegt als in (b).

![](images/page_166_chart_21.jpg)

<details>
<summary>bubble</summary>

| Position | Distance (m) | Weight (kg) |
| --- | --- | --- |
| Top | 1 | 36 |
| Middle | 2 | 9 |
| Bottom | 3 | 4 |
</details>

## 6.5 Die Berechnung des Trägheitsmoments

![](images/page_167_image_2.jpg)

## Lernziele

Nach dem Durcharbeiten dieses Abschnitts sollten Sie in der Lage sein, . . .

• das Trägheitsmoment eines Körpers zu bestimmen, sofern er in Tab. 6.2 aufgeführt ist,
• das Trägheitsmoment eines Körpers durch Integration über alle Massenelemente zu berechnen,
• den Steinerschen Satz für die Rotation um eine Achse anzuwenden, die nicht durch den Schwerpunkt des Körpers verläuft.

![](images/page_167_image_9.jpg)

## Schlüsselideen

• Das Trägheitsmoment I eines Körpers ist für ein System von einzelnen Teilchen als

$$
I = \sum m _ {i} r _ {i} ^ {2}
$$

und für Körper mit einer kontinuierlichen Masseverteilung als

$$
I = \int r ^ {2} \mathrm{d} m
$$

definiert. Dabei bezeichnen r bzw. $r _ { i }$ die senkrechten Abstände des jeweiligen Teilchens bzw. Volumenelements von der Rotationsachse und die Summe bzw. Integration verläuft über alle Teilchen bzw. das gesamte Volumen des Körpers (über alle Massenelemente).

• Der Steinersche Satz stellt eine Beziehung zwischen dem Trägheitsmoment I eines Körpers um eine beliebige Achse zu seinem Trägheitsmoment $I _ { \mathrm { S } }$ um eine dazu parallele Achse durch seinen Schwerpunkt her:

$$
I = I _ {\mathrm{S}} + M h ^ {2},
$$

wobei M die Masse des Körpers und h der senkrechte Abstand der beiden Achsen ist. Anschaulich ist h der Abstand, um den die Rotationsachse gegen die dazu parallele Achse durch den Schwerpunkt des Körpers verschoben ist.

## 6.5.1 Die Berechnung des Trägheitsmoments

Besteht ein starrer Körper nur aus wenigen Teilchen, so können wir sein Trägheitsmoment bezüglich einer gegebenen Achse mithilfe von Gl. 6.23 $( I = \textstyle \sum m _ { i } \widetilde { r _ { i } ^ { 2 } } )$ berechnen. Das bedeutet, wir bilden das Produkt $m r ^ { 2 }$ für jedes einzelne Teilchen und summieren anschließend die Produkte. (Wie Sie sich erinnern, ist r der senkrechte Abstand eines Teilchens von der jeweiligen Drehachse.)

Besteht ein starrer Körper hingegen aus sehr vielen Teilchen (handelt es sich also um eine kontinuierliche Verteilung von Materie, etwa in Form einer Frisbeescheibe), so kann man Gl. 6.23 nur mithilfe eines Computers auswerten. Stattdessen ersetzen wir die Summe in dieser Gleichung durch ein Integral und definieren das Trägheitsmoment des Körpers als

$$
I = \int r ^ {2} \mathrm{d} m. \tag {6.25}
$$

In Tab. 6.2 finden Sie Lösungen dieser Gleichung für neun häufig auftretende Formen von Objekten bezüglich der angegebenen Drehachsen.

## Der Steinersche Satz

Gesucht ist das Trägheitsmoment I eines Körpers der Masse m bezüglich einer gegebenen Achse. Prinzipiell können wir I stets durch Integration von Gl. 6.25 ermitteln. Wir können den Rechenweg aber deutlich abkürzen, wenn wir bereits das Trägheitsmoment $I _ { \mathrm { S } }$ des Körpers bezüglich einer Achse kennen, die durch den Schwerpunkt und parallel zur interessierenden Achse verläuft. Es sei h der senkrechte Abstand zwischen der gegebenen Achse und der Achse durch den Schwer punkt (denken Sie daran, dass der folgende Algorithmus nur gilt, wenn diese Achsen parallel verlaufen!). Das Trägheitsmoment I bezüglich der gegebenen Achse ist dann

TABELLE 6.2:

Einige Trägheitsmomente bei der Rotation.

<table><tr><td><img src="images/page_168_table_image_4_1.jpg"/></td><td><img src="images/page_168_table_image_4_2.jpg"/></td><td><img src="images/page_168_table_image_4_3.jpg"/></td></tr><tr><td><img src="images/page_168_table_image_4_4.jpg"/></td><td><img src="images/page_168_table_image_4_5.jpg"/></td><td><img src="images/page_168_table_image_4_6.jpg"/></td></tr><tr><td><img src="images/page_168_table_image_4_7.jpg"/></td><td><img src="images/page_168_table_image_4_8.jpg"/></td><td><img src="images/page_168_table_image_4_9.jpg"/></td></tr></table>

$$
I = I _ {\mathrm{S}} + M h ^ {2}. \tag {6.26}
$$

Im Folgenden werden wir diesen **Steinerschen Satz** herleiten und anschließend in Kontrollfrage 5 sowie Beispielaufgabe 6.6 im Übungsbuch anwenden.

## Herleitung des Steinerschen Satzes

Der Schwerpunkt eines in zufälliger Weise geformten Körpers, dessen Querschnitt Sie in Abb. 6.9 sehen, liege im Ursprung O eines xy-Koordinatensystems. Nun betrachten wir eine Achse senkrecht zur Querschnittsebene durch O und eine zweite, zur ersten parallele Achse, die durch einen Punkt P verläuft. Die Koordinaten von P seien a und b.

Es sei dm ein Massenelement mit den allgemeinen Koordinaten x und y. Das Trägheitsmoment des Körpers bezüglich der Achse durch P ist dann gemäß Gl. 6.25:

$$
I = \int r ^ {2} \mathrm{d} m = \int [ (x - a) ^ {2} + (y - b) ^ {2} ] \mathrm{d} m,
$$

![](images/page_168_image_12.jpg)

<details>
<summary>text_image</summary>

y
dm
Drehachse
durch P
r
y - b
P
x - a
h
b
O
x
Schwer-
punkt
Drehachse
durch den
Schwerpunkt
</details>

Abb. 6.9

Querschnitt eines starren Körpers, der Schwerpunkt befindet sich im Ursprung O. Der Steinersche Satz (Gl. 6.26) gibt die Beziehung zwischen dem Trägheitsmoment des Körpers bezüglich einer Achse durch O und dem Trägheitsmoment bezüglich einer Achse durch einen Punkt P an, der sich im Abstand h vom Schwerpunkt befindet. Beide Achsen stehen senkrecht auf der Ebene des Querschnitts.

![](images/page_169_image_1.jpg)

<details>
<summary>text_image</summary>

(1)
(2)
(3) (4)
</details>

was wir auch in der Form

$$
I = \int (x ^ {2} + y ^ {2}) \mathrm{d} m - 2 a \int x \mathrm{d} m - 2 b \int y \mathrm{d} m + \int (a ^ {2} + b ^ {2}) \mathrm{d} m, \tag {6.27}
$$

schreiben können. Aus der Definition des Schwerpunkts (Gl. 5.9) entnehmen wir, dass die beiden mittleren Integrale die Koordinaten des Schwerpunkts angeben (multipliziert mit einem konstanten Faktor) und deshalb jeweils gleich null sein müssen. Weiterhin ist $x ^ { 2 } + y ^ { 2 } = R ^ { 2 }$ mit R als Abstand zwischen O und dm, weshalb das erste Integral schlicht gleich $I _ { S }$ ist, das Trägheitsmoment des Körpers bezüglich einer durch seinen Schwerpunkt verlaufenden Achse. Wie uns ein Blick auf Abb. 6.9 sagt, ist der letzte Term in Gl. 6.27 gleich $M h ^ { 2 }$ mit M als Gesamtmasse des Körpers. Wir können Gl. 6.27 folglich auf Gl. 6.26 zurückführen, welche wir herleiten wollten.

## KONTROLLFRAGE 5

Die Zeichnung zeigt ein flaches, quaderförmiges Objekt (etwa ein Buch) mit vier verschiedenen Drehachsen, die alle senkrecht auf der Deckfläche des Objekts stehen. Ordnen Sie die Achsen nach dem zugehörigen Trägheitsmoment des Objekts, beginnend mit dem größten Wert.

## 6.6 Das Drehmoment

![](images/page_169_image_8.jpg)

## Lernziele

Nach dem Durcharbeiten dieses Abschnitts sollten Sie in der Lage sein, . . .

• zu verstehen, dass ein Drehmoment auf einen Körper von einer Kraft hervorgerufen wird, die an einem Punkt außerhalb der Drehachse angreift,
• ein Drehmoment aus (a) dem Winkel zwischen dem Orts- und dem Kraftvektor, (b) der Richtung und dem Hebel der Kraft oder (c) der Komponente der Kraft senkrecht zum Ortsvektor zu berechnen,
• zu verstehen, dass für die Berechnung eines Drehmoments immer auch die zugehörige Drehachse angegeben sein muss,
• zu verstehen, dass einem Drehmoment je nach der Richtung, in der es den Körper um die Rotationsachse drehen möchte, ein positives oder negatives Vorzeichen zugewiesen wird (im Uhrzeigersinn = negativ),
• das resultierende Drehmoment zu berechnen, wenn mehr als ein Drehmoment auf einen Körper wirkt.

![](images/page_169_image_17.jpg)

## Schlüsselideen

• Ein Drehmoment versucht, einen Körper aufgrund einer Kraft $\vec { F }$ um eine Rotationsachse zu drehen. Wenn die Kraft $\vec { F }$ an einem Punkt angreift, der durch den Ortsvektor $\vec { r }$ relativ zur Rotationsachse gegeben ist, ist der Betrag des Drehmoments

$$
\tau = r F _ {\mathrm{t}} = r _ {\perp} F = r F \sin \varphi ,
$$

wobei $F _ { \mathrm { t } }$ die Komponente von $\vec { F }$ senkrecht zu $\vec { r }$ ist und 𝜑 der Winkel zwischen ⃗r und $\vec { F } .$ Die Größe $r _ { \perp }$ ist der senkrechte Abstand zwischen der Drehachse und einer gedachten Verlängerung des Kraftvektors. Diese Verlängerung ist die Richtung der Kraft $\vec { F } ; r _ { \perp }$ wird der Hebelarm von $\vec { F }$ genannt. Entsprechend ist r der Hebelarm von $F _ { \mathrm { t } }$

• Die SI-Einheit des Drehmoments ist das Newtonmeter (N ⋅ m). Ein Drehmo ment τ ist positiv, wenn es versucht, einen ruhenden Körper gegen den Uhrzeigersinn zu drehen, und negativ, wenn es versucht, den Körper im Uhrzeigersinn zu drehen.

## 6.6.1 Das Drehmoment

Eine Türklinke ist stets so weit wie möglich vom Scharnier der Tür entfernt, und das aus gutem Grund. Wollen Sie eine schwere Tür öffnen, so müssen Sie natürlich eine Kraft aufwenden. Wichtig ist aber nicht nur der Betrag dieser Kraft, sondern auch der Angriffspunkt und die Richtung ihrer Wirkung. Drücken Sie in der Nähe des Scharniers oder unter einem Winkel gegen die Tür, der erheblich von $9 0 ^ { \circ }$ bezüglich der Türfläche abweicht, so müssen Sie wesentlich mehr Kraft aufwenden, als wenn Sie Ihre Kraft in der Nähe der Klinke und senkrecht zur Türfläche ansetzen.

In Abb. 6.10a sehen Sie den Querschnitt eines Körpers, der ungehindert um eine auf dem Querschnitt senkrecht stehende Achse durch O rotieren kann. Am Punkt $\mathrm { P } _ { \mathrm { r } }$ dessen Position relativ zu O durch den Ortsvektor $\boldsymbol { \cdot } \vec { r }$ gegeben ist, greift eine Kraft $\vec { F }$ an. Die Richtungen der Vektoren $\vec { F }$ und $\vec { r }$ schließen miteinander einen Winkel 𝜑 ein. (Der Einfachheit halber betrachten wir nur Kräfte, deren Komponente parallel zur Drehachse gleich null ist; das bedeutet, $\vec { F }$ liegt in der Papierebene.)

Wir wollen nun untersuchen, in welcher Weise $\vec { F }$ eine Rotation des Körpers um die angegebene Achse bewirkt. Dazu lösen wir $\vec { F }$ in zwei Komponenten auf (Abb. 6.10b). Eine davon, die radiale Komponente $F _ { \mathbf { r } } ,$ zeigt in Richtung von $\vec { r }$ und erzeugt keine Rotation, denn sie wirkt entlang einer Linie, die durch O verläuft. (Drücken Sie von einer Kante aus in Richtung des Scharniers gegen eine Tür, um sich zu überzeugen, dass sich die Tür dann nicht dreht.) Die tangentiale Komponente $F _ { \mathrm { t } }$ von $\vec { F }$ steht senkrecht au $\vec { r } _ { \vec { r } _ { r } } ^ { \rightarrow }$ ihr Betrag ist $F _ { \mathrm { t } } = F$ sin 𝜑. Diese Komponente ist für die Rotation verantwortlich. (Drücken Sie senkrecht gegen eine Tür, bewegt sie sich.)

Ob und wie effektiv die Anwendung der Kraft $\vec { F }$ eine Rotation bewirkt, hängt – wie bereits bemerkt – nicht nur vom Betrag ihrer tangentialen Komponente $F _ { \mathrm { t } }$ $\mathrm { a b } ,$ sondern auch vom Abstand zwischen dem Angriffspunkt der Kraft und O. Um beide Faktoren zu erfassen, definieren wir ihr Produkt als das **Drehmoment** τ (für englisch „torque“):

$$
\tau = r F \sin \varphi . \tag {6.28}
$$

Zwei äquivalente Schreibweisen dieser Definition sind

$$
\tau = r (F \sin \varphi) = r F _ {\mathrm{t}} \tag {6.29}
$$

und

$$
\tau = (r \sin \varphi) F = r _ {\perp} F \tag {6.30}
$$

mit $r _ { \perp }$ als senkrechtem Abstand zwischen der Rotationsachse in O und der Verlängerung der Richtung des Vektors $\vec { F }$ (siehe Abb. 6.10c). Diese Verlängerungslinie ist die **Richtung der Kraft** $\vec { F }$ und $r _ { \perp }$ ist der **Hebelarm** von F. Wie Sie Abb. 6.10 entnehmen können, ist $r ,$ der Betrag von $\vec { r } ,$ gleich dem Hebelarm der Komponente $F _ { \mathrm { t } }$ von ${ \vec { F } } .$

Das Drehmoment lässt sich als „drehende Wirkung“ der Kraft $\vec { F }$ auffassen. Wenn Sie ein Objekt wie einen Schraubenzieher oder einen Drehmomentschlüssel mithilfe einer Kraft in Rotation versetzen, so wenden Sie ein Drehmoment an. Die SI-Einheit des Drehmoments ist Newton mal Meter (N ⋅ m) bzw. Newtonmeter (Nm). (Vorsicht: Die gleiche Einheit gilt für die Arbeit. Arbeit und Drehmoment sind aber verschiedene Größen, die nicht verwechselt werden dürfen. Oft gibt man eine $\mathrm { A r } -$ beit in J (1 J = 1 N ⋅ m) an, für Drehmomente darf diese Einheit hingegen nicht verwendet werden.)

Im folgenden Kapitel werden wir das Drehmoment allgemeiner als vektorielle Größe diskutieren (und dann auch sehen, dass beim Drehmoment Kraft und Weg auf andere Weise multipliziert werden als bei der Arbeit). Da wir uns im Augenblick auf Drehbewegungen um einzelne Achsen beschränken, müssen wir das Drehmoment noch nicht als Vektor formulieren. Wir ordnen ihm stattdessen ein positives oder negatives Vorzeichen zu, je nachdem, in welche Richtung sich ein ruhender Körper zu drehen beginnt, wenn dieses Drehmoment auf ihn wirkt. Rotiert der Körper im Uhrzeigersinn, so ist das Drehmoment negativ und umgekehrt (siehe zu dieser Vereinbarung Abschn. 6.1).

![](images/page_170_image_15.jpg)

Abb. 6.10 (a) Eine Kraft $\vec { F }$ greift im Punkt P eines starren Körpers an, der ungehindert um eine Achse durch O rotieren kann. Diese Achse steht senkrecht auf der hier abgebildeten Querschnittsebene. (b) Das zu dieser Kraft gehö- rende Drehmoment ist gegeben durch $( r ) ( F$ sin 𝜑) oder äquivalent durch $r F _ { \mathrm { t } } ,$ wobei $F _ { \mathrm { t } }$ die tangentiale Komponente von $\vec { F }$ ist. (c) Eine weitere Schreibweise für das Drehmoment ist $r _ { \perp } F$ mit $r _ { \perp }$ als Hebelarm von ${ \vec { F } } .$

![](images/page_171_chart_1.jpg)

<details>
<summary>line</summary>

| Component | Force Direction |
| --- | --- |
| F1 | Downward |
| F2 | Upward |
| F3 | Downward |
| F4 | Upward |
</details>

Drehmomente befolgen das in Kapitel 2 eingeführte Superpositionsprinzip: Wirken auf einen Körper mehrere Drehmomente, so ergibt sich das **resultierende Drehmoment** $\tau _ { \mathrm { g e s } }$ als Summe der einzelnen Beiträge.

## KONTROLLFRAGE 6

Die Skizze zeigt einen Meterstab (von oben gesehen), der sich um den markierten Punkt (Position 20 für 20 cm) drehen kann. Alle fünf waagerecht am Stab angreifenden Kräfte haben den gleichen Betrag. Ordnen Sie die Kräfte nach dem Drehmoment, das sie bewirken, beginnend mit dem größten Wert.

## 6.7 Das zweite Newtonsche Gesetz für die Rotation

![](images/page_171_image_7.jpg)

## Lernziele

Nach dem Durcharbeiten dieses Abschnitts sollten Sie in der Lage sein, . . .

• das zweite Newtonsche Gesetz für die Rotation anzuwenden, um eine Bezie hung zwischen dem resultierenden Drehmoment auf einen Körper, dessen Träg heitsmoment und der Rotationsbeschleunigung aufzustellen, wobei alle Größen auf dieselbe Rotationsachse bezogen sein müssen.

![](images/page_171_image_11.jpg)

## Schlüsselideen

• Das Analogon des zweiten Newtonschen Gesetzes für die Rotation ist

$$
\tau_ {\mathrm{ges}} = I \alpha ,
$$

wobei $\tau _ { \mathrm { g e s } }$ das auf ein Teilchen oder einen starren Körper wirkende resultierende Drehmoment ist, I ist das Trägheitsmoment des Teilchens bzw. Körpers um die Drehachse und α die resultierende Winkelbeschleunigung um diese Achse.

## 6.7.1 Das zweite Newtonsche Gesetz für die Rotation

![](images/page_171_image_17.jpg)

<details>
<summary>text_image</summary>

y
Ft
F
φ
m
Fr
r
Stab
θ
O
Drehachse
x
</details>

Abb. 6.11

Ein einfacher starrer Körper, der nur um eine durch O verlaufende Achse rotieren kann. Er besteht aus einem Teilchen der Masse m, befestigt an einem Ende eines masselosen Stabs der Länge r. Durch das Einwirken einer Kraft $\vec { F }$ beginnt die Anordnung zu rotieren.

Wie wir im vorangegangenen Abschnitt gesehen haben, kann ein Drehmoment die Rotation eines starren Körpers bewirken. Wir suchen nun einen Zusammenhang zwischen dem resultierenden Drehmoment $\tau _ { \mathrm { g e s } } ,$ das an einem Körper angreift, und der Winkelbeschleunigung α bezüglich der Rotationsachse, die es verursacht. Dabei gehen wir wie beim zweiten Newtonschen Gesetz $( F _ { \mathrm { g e s } } = m a )$ für die Beschleunigung a eines Körpers der Masse m vor, auf den eine Kraft $F _ { \mathrm { g e s } }$ entlang einer Koordinatenachse wirkt. Wir ersetzen $F _ { \mathrm { g e s } }$ durch $\tau _ { \mathrm { g e s } } ,$ m durch I und a durch α. Dann haben wir bereits das zweite Newtonsche Gesetz für die Drehbewegung:

$$
\tau_ {\mathrm{ges}} = I \alpha \quad (\text {Bogenma} \beta). \tag {6.31}
$$

## Herleitung von Gl. 6.31

Betrachten wir zunächst die einfache, in Abb. 6.11 dargestellte Situation. Der starre Körper besteht hier aus einem einzelnen Teilchen der Masse m, befestigt an einem masselosen Stab der Länge r. Der Stab kann nur um eine Achse rotieren, die durch sein anderes Ende verläuft und senkrecht auf der Papierebene steht. Folglich kann das Teilchen nur eine Kreisbahn beschreiben, durch deren Mittelpunkt die Drehachse führt.

Auf das Teilchen wirkt nun eine Kraft ${ \vec { F } } .$ Da sich das Teilchen nur auf der Kreisbahn bewegen kann, wird es ausschließlich durch die tangentiale Komponente $F _ { \mathrm { t } }$ der Kraft (die Komponente, die tangential zur Kreisbahn gerichtet ist) beschleunigt. Den Zusammenhang zwischen $F _ { \mathrm { t } }$ und der tangentialen Beschleunigung $a _ { \mathrm { t } }$ schreiben wir gemäß dem zweiten Newtonschen Gesetz auf als

$$
F _ {\mathrm{t}} = m a _ {\mathrm{t}}.
$$

Aus Gl. 6.29 folgt für das auf das Teilchen wirkende Drehmoment

$$
\tau = F _ {\mathrm{t}} r = m a _ {\mathrm{t}} r.
$$

Mithilfe von Gl. 6.19 $( a _ { \mathrm { t } } = \alpha r )$ schreiben wir dafür

$$
\tau = m (\alpha r) r = (m r ^ {2}) \alpha . \tag {6.32}
$$

Der Klammerausdruck auf der rechten Seite von Gl. 6.32 ist gleich dem Trägheitsmoment des Körpers bezüglich der Drehachse (siehe Gl. 6.23). So verkürzt sich Gl. 6.32 zu

$$
\tau = I \alpha \quad (\text {Bogenma} \beta). \tag {6.33}
$$

Für den Fall, dass mehr als eine Kraft an dem Teilchen angreift, verallgemeinern wir Gl. 6.33:

$$
\tau_ {\mathrm{ges}} = I \alpha \quad (\text {Bogenma} \beta). \tag {6.34}
$$

Diese Gleichung wollten wir herleiten. Sie gilt für beliebige um eine feste Achse rotierende starre Körper, weil sich jeder derartige Körper als Anordnung unverrückbar miteinander verbundener einzelner Teilchen behandeln lässt.

## KONTROLLFRAGE 7

Der skizzierte Meterstab kann um den angegebenen Punkt links von der Mitte des Stabs rotieren. Zwei Kräfte ${ \vec { F } } _ { 1 }$ und $\vec { F } _ { 2 }$ greifen waagerecht an dem Stab an; nur ${ \vec { F } } _ { 1 }$ ist eingezeichnet. Die Kraft $\vec { \bar { F } } _ { 2 }$ wirkt am rechten Ende, senkrecht zum Stab. (a) In welche Richtung muss $\vec { F } _ { 2 }$ zeigen und (b) wie groß muss $F _ { 2 }$ relativ zu $F _ { 1 }$ sein, wenn sich der Stab nicht drehen soll?

![](images/page_172_image_15.jpg)

<details>
<summary>text_image</summary>

Drehpunkt
F₁
</details>

## 6.8 Arbeit und kinetische Energie der Rotation

## Lernziele

Nach dem Durcharbeiten dieses Abschnitts sollten Sie in der Lage sein, . . .

• die von einem Drehmoment an einem rotierenden Körper verrichtete Arbeit durch Integration des Drehmoments über den Drehwinkel zu berechnen,
aus der Beziehung zwischen Arbeit und kinetischer Energie eine Relation zwischen der von einem Drehmoment verrichteten Arbeit und der daraus resultierenden Änderung der kinetischen Rotationsenergie eines Körpers aufzustellen,
• die von einem konstanten Drehmoment verrichtete Arbeit aus dem Drehwinkel des Körpers zu bestimmen,
• die von einem Drehmoment erbrachte Leistung aus der Rate zu berechnen, mit der es Arbeit verrichtet,
• die momentane Leistung eines Drehmoments zu einem gegebenen Zeitpunkt aus dem Drehmoment und der Winkelgeschwindigkeit zu diesem Zeitpunkt zu bestimmen.

![](images/page_172_image_25.jpg)

## Schlüsselideen

• Die Gleichungen für die verrichtete Arbeit und die erbrachte Leistung bei Rotationsbewegungen entsprechen denjenigen, die wir aus der Translationsbewegung kennen; sie lauten

$$
W = \int_ {\theta_ {\mathrm{i}}} ^ {\theta_ {\mathrm{f}}} \tau   \mathrm{d} \theta
$$

![](images/page_172_image_29.jpg)

und

$$
P = \frac {\mathrm{d} W}{\mathrm{d} t} = \tau \omega .
$$

• Wenn τ konstant ist, reduziert sich das Integral auf

$$
W = \Delta \theta = \tau (\theta_ {\mathrm{f}} - \theta_ {\mathrm{i}}).
$$

• Die Beziehung zwischen Arbeit und kinetischer Energie lautet für Rotationsbewegungen

$$
\Delta K = K _ {\mathrm{f}} - K _ {\mathrm{i}} = \frac {1}{2} I \omega_ {\mathrm{f}} ^ {2} - \frac {1}{2} I \omega_ {\mathrm{f}} ^ {2} = W.
$$

## 6.8.1 Arbeit und kinetische Energie der Rotation

Bewirkt eine Kraft F die Beschleunigung eines starren Körpers der Masse m entlang einer Koordinatenachse, so verrichtet sie, wie wir in Kapitel 3 diskutiert haben, an diesem Körper eine Arbeit W. Dabei kann sich die kinetische Energie des Körpers $\begin{array} { r } { K = \frac { 1 } { 2 } m \nu ^ { \hat { 2 } } } \end{array}$ ändern. Nehmen wir an, nur diese Energieform des Körpers ändere sich. Dann können wir gemäß Gl. 3.10 folgenden Zusammenhang zwischen $\Delta K$ und der Arbeit W formulieren:

$$
\Delta K = K _ {\mathrm{f}} - K _ {\mathrm{i}} = \frac {1}{2} m v _ {\mathrm{f}} ^ {2} - \frac {1}{2} m v _ {\mathrm{i}} ^ {2} = W. \tag {6.35}
$$

Ist die Bewegung auf die x-Achse beschränkt (eindimensional), so berechnen wir die Arbeit mithilfe von Gl. 3.30:

$$
W = \int_ {x _ {\mathrm{i}}} ^ {x _ {\mathrm{f}}} F \mathrm{d} x. \tag {6.36}
$$

Bei konstanter Kraft F ist dann $W = F d$ mit d als Verschiebung des Körpers. Die Rate, mit der die Arbeit verrichtet wird, ist die Leistung, zu berechnen mithilfe der Gln. 3.41 und 3.46:

$$
P = \frac {\mathrm{d} W}{\mathrm{d} t} = F \nu . \tag {6.37}
$$

Betrachten wir nun den analogen Fall bei einer Rotationsbewegung. Beschleunigt ein Drehmoment die Rotation eines starren Körpers um eine feste Achse, so verrichtet es dabei die Arbeit W. Dabei kann sich die kinetische Energie der Rotation des Körpers $\begin{array} { r } { K = \frac { 1 } { 2 } I \omega ^ { 2 } } \end{array}$ ändern. Wieder nehmen wir an, alle anderen Energieformen des Körpers seien konstant. Analog zu Gl. 6.35 formulieren wir dann einen Zusammenhang zwischen ΔK und der verrichteten Arbeit, wobei nun die kinetische Energie der Rotation einfließt:

$$
\Delta K = K _ {\mathrm{f}} - K _ {\mathrm{i}} = \frac {1}{2} I \omega_ {\mathrm{f}} ^ {2} - \frac {1}{2} I \omega_ {\mathrm{i}} ^ {2} = W. \tag {6.38}
$$

I ist das Trägheitsmoment des Körpers bezüglich der festen Achse; $\omega _ { \mathrm { i } }$ und $\omega _ { \mathrm { f } }$ sind die Winkelgeschwindigkeit des Körpers vor bzw. nach Verrichtung der Arbeit.

Die Arbeit berechnen wir mit der folgenden, zu Gl. 6.36 äquivalenten Beziehung:

$$
W = \int_ {\theta_ {\mathrm{i}}} ^ {\theta_ {\mathrm{f}}} \tau \mathrm{d} \theta . \tag {6.39}
$$

Hier ist τ das Drehmoment, welches die Arbeit W verrichtet; $\theta _ { \mathrm { i } }$ und $\theta _ { \mathrm { f } }$ bezeichnen die Winkelpositionen des Körpers vor bzw. nach der Verrichtung der Arbeit. Bei konstantem τ verkürzt sich Gl. 6.39 zu

$$
W = \tau (\theta_ {\mathrm{f}} - \theta_ {\mathrm{i}}). \tag {6.40}
$$

TABELLE 6.3: Gleichungen für die Rotation und ihre Äquivalente für die Translation.

<table><tr><td colspan="2">Reine Translation (feste Richtung)</td><td colspan="2">Reine Rotation (feste Achse)</td></tr><tr><td>Ort</td><td>x</td><td>Winkelposition</td><td> $\theta$ </td></tr><tr><td>Geschwindigkeit</td><td> $\nu = dx/dy$ </td><td>Winkelgeschwindigkeit</td><td> $\omega = d\theta/dt$ </td></tr><tr><td>Beschleunigung</td><td> $a = d\nu/dt$ </td><td>Winkelbeschleunigung</td><td> $\alpha = d\omega/dt$ </td></tr><tr><td>Masse</td><td>m</td><td>Trägheitsmoment</td><td>I</td></tr><tr><td>Zweites Newtonsches Gesetz</td><td> $F_{ges} = ma$ </td><td>Zweites Newtonsches Gesetz</td><td> $\tau_{ges} = I\alpha$ </td></tr><tr><td>Arbeit</td><td> $W = \int F \, dx$ </td><td>Arbeit</td><td> $W = \int \tau \, d\theta$ </td></tr><tr><td>Kinetische Energie</td><td> $K = \frac{1}{2}mv^{2}$ </td><td>Kinetische Energie</td><td> $K = \frac{1}{2}I\omega^{2}$ </td></tr><tr><td>Leistung (konstante Kraft)</td><td> $P = F\nu$ </td><td>Leistung (konstantes Drehmoment)</td><td> $P = \tau\omega$ </td></tr><tr><td>Arbeit und Energie</td><td> $W = \Delta K$ </td><td>Arbeit und Energie</td><td> $W = \Delta K$ </td></tr></table>

Die Rate, mit der die Arbeit verrichtet wird, ist die Leistung. Wir berechnen sie mit der zu Gl. 6.37 äquivalenten Beziehung

$$
P = \frac {\mathrm{d} W}{\mathrm{d} t} = \tau \omega . \tag {6.41}
$$

Tabelle 6.3 stellt die Gleichungen für die Rotation eines starren Körpers um eine feste Achse den entsprechenden Beziehungen für die Translation gegenüber.

## Herleitung der Gln. 6.38–6.41

Betrachten wir noch einmal die Situation in Abb. 6.11: Die Kraft $\vec { F }$ wirkt auf einen starren Körper, bestehend aus einem einzelnen Teilchen der Masse m, befestigt an einem Ende eines masselosen Stabs. Der Körper beginnt zu rotieren; während der Rotation verrichtet $\vec { F }$ an dem Körper eine Arbeit. Nehmen wir an, $\vec { F }$ beeinflusse nur eine einzige Energieform des Körpers, nämlich die kinetische Energie. Dann können wir Gl. 6.35 anwenden:

$$
\Delta K = K _ {\mathrm{f}} - K _ {\mathrm{i}} = W. \tag {6.42}
$$

Mit $\begin{array} { r } { K = \frac { 1 } { 2 } m \nu ^ { 2 } } \end{array}$ und $\nu = \omega r$ (Gl. 6.15) schreiben wir diese Beziehung in der Form

$$
\Delta K = \frac {1}{2} m r ^ {2} \omega_ {\mathrm{f}} ^ {2} - \frac {1}{2} m r ^ {2} \omega_ {\mathrm{i}} ^ {2} = W. \tag {6.43}
$$

Aus Gl. 6.23 folgt für das Trägheitsmoment dieses (aus einem Teilchen bestehenden) Körpers $\bar { I = m r ^ { 2 } }$ . Wir setzen dies in Gl. 6.43 ein:

$$
\Delta K = \frac {1}{2} I \omega_ {\mathrm{f}} ^ {2} - \frac {1}{2} I \omega_ {\mathrm{i}} ^ {2} = W.
$$

Damit haben wir Gl. 6.38 für einen starren, aus einem Teilchen bestehenden Körper hergeleitet. Die Beziehung gilt für jeden starren Körper bei der Rotation um eine feste Achse.

Als zweiten Schritt wollen wir nun einen Zusammenhang zwischen der an dem Körper in Abb. 6.11 verrichteten Arbeit W und dem Drehmoment τ herstellen, das infolge der Kraft $\vec { F }$ auf den Körper wirkt. Bewegt sich das Teilchen eine Strecke ds auf seiner Kreisbahn, so wird es nur von der tangentialen Komponente $F _ { \mathrm { t } }$ der Kraft beschleunigt; das bedeutet, nur $F _ { \mathrm { t } }$ verrichtet an dem Teilchen Arbeit. Diese Arbeit dW schreiben wir als $F _ { \mathrm { t } }$ ds und ersetzten ds durch r dθ mit dθ als dem Winkel, den das Teilchen während des Durchlaufens von ds überstreicht. Es gilt also:

$$
\mathrm{d} W = F _ {\mathrm{t}} r \mathrm{d} \theta . \tag {6.44}
$$

Wie ein Blick auf Gl. 6.29 zeigt, ist das Produkt $F _ { \mathrm { t } } r$ gleich dem Drehmoment τ, und wir können anstelle von Gl. 6.44 schreiben:

$$
\mathrm{d} W = \tau \mathrm{d} \theta . \tag {6.45}
$$

Die während des Durchlaufens eines endlichen Drehwinkels (von $\theta _ { \mathrm { i } }$ bis $\theta _ { \mathrm { f } } )$ geleistete Arbeit ist damit gleich:

$$
W = \int_ {\theta_ {\mathrm{i}}} ^ {\theta_ {\mathrm{f}}} \tau \mathrm{d} \theta .
$$

Dies ist Gl. 6.39, aus der Gl. 6.40 unmittelbar hervorgeht. Sie gilt für jeden starren Körper, der um eine feste Achse rotiert.

Die Leistung der Rotationsbewegung erhalten wir aus Gl. 6.45:

$$
P = \frac {\mathrm{d} W}{\mathrm{d} t} = \tau \frac {\mathrm{d} \theta}{\mathrm{d} t} = \tau \omega ,
$$

womit wir bei Gl. 6.41 angelangt sind.

## 6.9 Zusammenfassung

**Winkelposition** Um die Rotation eines starren Körpers um eine feste Achse, die **Dreh**- oder **Rotationsachse**, zu beschreiben, denken wir uns eine **Bezugslinie** senkrecht zu dieser Achse, die mit dem Körper rotiert. Wir messen die Winkelposition θ dieser Linie relativ zu einer festgelegten Richtung (der Winkelposition null). Wird θ in **Bogenmaß** angegeben, so gilt

$$
\theta = \frac {s}{r} \tag {6.1}
$$

mit s als Bogenlänge auf einer Kreisbahn mit dem Radius $r ,$ die beim Überstreichen des Winkels θ durchlaufen wird. Der Zusammenhang zwischen den Winkelangaben in Bogenmaß, Grad und Umdrehungen ist gegeben durch

$$
1 \mathrm{U} = 3 6 0 ^ {\circ} = 2 \pi \mathrm{rad}. \tag {6.2}
$$

**Drehwinkel** Ändert sich die Winkelposition eines rotierenden Körpers bezüglich einer Achse von $\theta _ { 1 }$ nach $\theta _ { 2 } ,$ so bezeichnen wir $\Delta \theta$ mit

$$
\Delta \theta = \theta_ {2} - \theta_ {1} \tag {6.4}
$$

als Drehwinkel. Er ist positiv für Rotationen entgegen dem Uhrzeigersinn und negativ für Rotationen im Uhrzeigersinn.

**Winkelgeschwindigkeit** Dreht sich ein Körper in einem Zeitintervall $\Delta t$ um einen Winkel $\Delta \theta ,$ so ist die mittlere Winkelgeschwindigkeit $\omega _ { \mathrm { g e m } }$ gegeben durch

$$
\omega_ {\mathrm{gem}} = \frac {\Delta \theta}{\Delta t}. \tag {6.5}
$$

Die momentane Winkelgeschwindigkeit ω des Körpers ist

$$
\omega = \frac {\mathrm{d} \theta}{\mathrm{d} t}. \tag {6.6}
$$

Sowohl $\omega _ { \mathrm { g e m } }$ als auch ω sind vektorielle Größen. Ihre Richtungen werden mithilfe der **Rechte-Hand-Regel** (Abb. 6.5) ermittelt. Sie sind positiv für Rotationen entgegen dem Uhrzeigersinn und negativ für Rotationen im Uhrzeigersinn.

**Winkelbeschleunigung** Ändert sich die Winkelgeschwindigkeit eines rotierenden Körpers innerhalb eines Zeitintervalls $\Delta t = t _ { 2 } - t _ { 1 }$ von $\omega _ { 1 }$ nach $\omega _ { 2 } ,$ so ist die mittlere Winkelbeschleunigung $\alpha _ { \mathrm { g e m } }$ des Körpers gleich

$$
\alpha_ {\mathrm{gem}} = \frac {\omega_ {2} - \omega_ {1}}{t _ {2} - t _ {1}} = \frac {\Delta \omega}{\Delta t}. \tag {6.7}
$$

Die momentane Winkelbeschleunigung α ist entsprechend

$$
\alpha = \frac {\mathrm{d} \omega}{\mathrm{d} t}. \tag {6.8}
$$

$\alpha _ { \mathrm { g e m } }$ und α sind Vektoren.

**Bewegungsgleichungen für die gleichmäßig beschleunigte Rotation** Die Rotation mit konstanter Winkelbeschleunigung α ist ein wichtiger Spezialfall der allgemeinen Drehbewegung. Die zugehörigen Bewegungsgleichungen, zusammengefasst in Tab. 6.1, sind

$$
\omega = \omega_ {0} + \alpha t, \tag {6.9}
$$

$$
\theta - \theta_ {0} = \omega_ {0} t + \frac {1}{2} \alpha t ^ {2}, \tag {6.10}
$$

$$
\omega^ {2} = \omega_ {0} ^ {2} + 2 \alpha (\theta - \theta_ {0}), \tag {6.11}
$$

$$
\theta - \theta_ {0} = \frac {1}{2} (\omega_ {0} + \omega) t, \tag {6.12}
$$

$$
\theta - \theta_ {0} = \omega t - \frac {1}{2} \alpha t ^ {2}. \tag {6.13}
$$

**Beziehungen zwischen den Variablen für lineare Bewegung und Rotation** Ein Punkt innerhalb eines rotierenden starren Körpers, der sich in einem senkrechten Abstand r von der Drehachse befindet, bewegt sich auf einer Kreisbahn mit dem Radius r. Überstreicht der Körper einen Drehwinkel $\theta ,$ so legt der Punkt auf dem Kreisbogen die Strecke

$$
s = \theta r \tag {6.14}
$$

zurück (θ in Bogenmaß).

Die lineare Geschwindigkeit v⃗ des Punkts zeigt in Richtung der Tangente an den Kreis in diesem Punkt. Der Betrag dieser Geschwindigkeit ist gegeben durch

$$
\nu = \omega r \tag {6.15}
$$

mit $\omega$ als Betrag der Winkelgeschwindigkeit in rad/s. Die lineare Beschleunigung $\vec { a }$ des Punkts hat eine tangentiale und eine radiale Komponente. Die tangentiale Komponente ist

$$
a _ {\mathrm{t}} = \alpha r \tag {6.19}
$$

mit α als Betrag der Winkelbeschleunigung in rad $/ \mathbf { s } ^ { 2 } .$ . Die radiale Komponente von $\vec { a }$ ist

$$
a _ {\mathrm{r}} = \frac {\nu^ {2}}{r} = \omega^ {2} r. \tag {6.20}
$$

Bewegt sich der Punkt gleichförmig auf einer Kreisbahn, so ist $T$ die Periode der Bewegung des Punkts und des Körpers mit

$$
T = \frac {2 \pi r}{\nu} = \frac {2 \pi}{\omega} \tag {6.16,6.17}
$$

und ω in rad/s.

**Kinetische Energie und Trägheitsmoment der Rotation** Die kinetische Energie K eines Körpers bei der Rotation um eine feste Achse ist gegeben durch:

$$
K = \frac {1}{2} I \omega^ {2} \tag {6.24}
$$

mit ω in rad/s und I als Trägheitsmoment des Körpers bezüglich dieser Achse, definiert durch

$$
I = \sum m _ {i} r _ {i} ^ {2} \tag {6.23}
$$

für ein System diskreter Teilchen und durch

$$
I = \int r ^ {2} \mathrm{d} m \tag {6.25}
$$

für eine kontinuierliche Masseverteilung. In diesen Gleichungen bezeichnen r und $r _ { i }$ den senkrechten Abstand jedes Massenelements von der Drehachse.

**Steinerscher Satz** Der Steinersche Satz gibt die Beziehung zwischen dem Trägheitsmoment I eines Körpers bezüglich einer beliebigen Achse und dem Trägheitsmoment $I _ { \mathrm { S } }$ dieses Körpers bezüglich einer zur ersten parallelen, aber durch den Schwerpunkt des Körpers verlaufenden Achse an:

$$
I = I _ {\mathrm{S}} + M h ^ {2}. \tag {6.26}
$$

h ist der senkrechte Abstand zwischen beiden Achsen.

**Drehmoment** Erzeugt eine Kraft $\vec { F }$ eine Drehbewegung um eine Achse, so spricht man von einem Drehmoment. Greift $\vec { F }$ an einem Punkt an, der durch den Ortsvektor $\vec { r }$ bezüglich der Achse definiert ist, so ist der Betrag des Drehmoments gegeben durch:

$$
\tau = r F _ {\mathrm{t}} = r _ {\perp} F = r F \sin \varphi \tag {6.28-6.30}
$$

mit $F _ { \mathrm { t } }$ als Komponente von $\vec { F }$ senkrecht zu $1 \vec { r }$ und 𝜑 als Winkel zwischen den Richtungen von $\vec { r }$ und ${ \vec { F } } .$ Die Größe $r _ { \perp } ,$ der Hebelarm von ${ \vec { F } } ,$ ist der senkrechte Abstand zwischen der Drehachse und der Verlängerung des Vektors $\vec { F }$ durch eine Linie (die **Richtung der Kraft**). Analog ist r der Hebelarm von $F _ { \mathrm { r } }$ .

Die SI-Einheit des Drehmoments ist das Newtonmeter (N ⋅ m). Ein Drehmoment τ ist positiv, wenn es einen ruhenden Körper gegen den Uhrzeigersinn in Rotation versetzt, und negativ, wenn die Bewegung im Uhrzeigersinn erfolgt.

**Zweites Newtonsches Gesetz für die Drehbewegung** Das zweite Newtonsche Gesetz für die Drehbewegung ist:

$$
\tau_ {\mathrm{ges}} = I \alpha , \tag {6.34}
$$

mit $\tau _ { \mathrm { g e s } }$ als resultierendem Drehmoment, das auf einen Massepunkt oder einen festen Körper wirkt, I als Trägheitsmoment des Massepunkts oder Körpers bezüglich der Drehachse und α als resultierender Winkelbeschleunigung bezüglich dieser Achse.

**Arbeit und kinetische Energie der Rotation** Die Gleichungen, mit denen wir die Arbeit und die kinetische Energie der Rotation berechnen, entsprechen den für die Translation gültigen Beziehungen und lauten

$$
W = \int_ {\theta_ {\mathrm{i}}} ^ {\theta_ {\mathrm{f}}} \tau \mathrm{d} \theta \tag {6.39}
$$

sowie

$$
P = \frac {\mathrm{d} W}{\mathrm{d} t} = \tau \omega . \tag {6.41}
$$

Bei konstantem Drehmoment τ vereinfacht sich Gl. 6.39 zu

$$
W = \tau (\theta_ {\mathrm{f}} - \theta_ {\mathrm{i}}). \tag {6.40}
$$

Der Zusammenhang zwischen Arbeit und kinetischer Energie der Rotation ist gegeben durch

$$
\Delta K = K _ {\mathrm{f}} - K _ {\mathrm{i}} = \frac {1}{2} I \omega_ {\mathrm{f}} ^ {2} - \frac {1}{2} I \omega_ {\mathrm{i}} ^ {2} = W. \tag {6.38}
$$

## 6.10 Fragen

**1.** In Abb. 6.F1b sehen Sie den Graphen der Winkelposition der in Abb. 6.F1a gezeigten rotierenden Scheibe als Funktion der Zeit. Ist die Winkelgeschwindigkeit der Scheibe positiv, negativ oder null bei (a) $t   =   1   \mathrm { s } ,$ (b) $t   =   2   \mathrm { s } _ { i }$ (c) $t = 3   \mathrm { s } ?$ (d) Ist die Winkelbeschleunigung der Scheibe positiv oder negativ?

![](images/page_177_image_3.jpg)

<details>
<summary>text_image</summary>

Drehachse
</details>

(a)

![](images/page_177_chart_5.jpg)

<details>
<summary>line</summary>

| t (s) | \(\theta (\)rad) |
| --- | --- |
| 1 | 0 |
| 2 | Peak |
| 3 | 0 |
</details>

(b)

Abb. 6.F1

**2.** In Abb. 6.F2 sehen Sie einen Graphen der Winkelgeschwindigkeit der in Abb. 6.F1a gezeigten rotierenden Scheibe als Funktion der Zeit. Geben Sie die Drehrichtung (a) zu Beginn und (b) am Ende der Messung an! (c) Kommt die Scheibe vorübergehend zum Stillstand? (d) Ist die Winkelbeschleunigung positiv oder negativ? (e) Ist die Winkelbeschleunigung konstant oder ändert sie sich?

![](images/page_177_image_9.jpg)

<details>
<summary>text_image</summary>

ω
t
</details>

Abb. 6.F2

**3.** Halten Sie Ihren rechten Arm nach unten neben den Körper, die Handfläche zeigt zum Oberschenkel. Das Handgelenk wird während den folgenden Aktionen relativ zum Arm nicht bewegt. (1) Heben Sie den Arm bis zur Waagerechten nach vorne; (2) führen Sie ihn waagerecht zur Seite, bis er direkt nach rechts zeigt, und (3) senken Sie ihn wieder nach unten ab. Ihre Handfläche zeigt nun nach vorne. Beginnen Sie noch einmal von vorn, wobei Sie diesmal aber erst den Arm zur Seite, dann nach vorne und dann wieder in die Ausgangsposition bringen. Warum zeigt Ihre Handfläche jetzt nicht nach vorne?
**4.** Die folgenden Ausdrücke geben Winkelgeschwindigkeiten ω(t) an. In welchen Fällen können Sie die in Tab. 6.1 aufgeführten Gleichungen anwenden? (a) $\omega = 3 ;$ (b) $\omega =$ $4t^{2}+2t-6;( c ) \; \omega = 3t - 4;( d ) \; \omega = 5t^{2}-3$ mit ω jeweils in rad/s und t in s.
**5.** Abbildung 6.F5 zeigt einen Graphen der Winkelgeschwindigkeit als Funktion der Zeit für die rotierende Scheibe aus Abb. 6.F1a. Ordnen Sie für einen Punkt auf dem Rand der Scheibe die vier Zeitpunkte a, b, c und d nach dem Betrag (a) der Tangentialbeschleunigung und (b) der Radialbeschleunigung, beginnend jeweils mit dem größten Wert.

![](images/page_177_chart_16.jpg)

<details>
<summary>line</summary>

| Time (t) | Frequency \((\omega)\) |
| --- | --- |
| 0 | 0 |
| a | ~0.5 |
| b | ~1.0 |
| c | ~1.0 |
| d | 0 |
</details>

Abb. 6.F5

**6.** In Abb. 6.F6 sehen Sie eine Momentaufnahme einer entgegen dem Uhrzeigersinn rotierenden Scheibe in Draufsicht. Die Winkelgeschwindigkeit ω der Scheibe nimmt allmählich ab (die Scheibe wird langsamer, aber ihre Drehrichtung ändert sich nicht). Am linken Rand eingezeichnet ist ein Insekt, das sich mit der Scheibe gemeinsam bewegt. Geben Sie für den Zeitpunkt der Aufnahme die Richtung (a) der Radialbeschleunigung und (b) der Tangentialbeschleunigung des Insekts an.

![](images/page_177_image_19.jpg)

<details>
<summary>natural_image</summary>

Circular diagram with x and y axes intersecting at origin, showing radial lines and a central circle (no text or symbols)
</details>

Abb. 6.F6

**7.** In Abb. 6.F7 ist eine Anordnung aus drei kleinen Kugeln gleicher Masse skizziert, welche an einem masselosen Stab in den angegebenen Abständen befestigt sind. Betrachten Sie die Trägheitsmomente der Rotation dieser

Anordnung um jede der drei Kugeln. Ordnen Sie die Kugeln nach dem zugehörigen Trägheitsmoment, beginnend mit dem größten Wert.

![](images/page_177_image_23.jpg)

Abb. 6.F7

**8.** Abbildung 6.F8a zeigt in Draufsicht einen waagerechten Balken, der sich um eine Achse drehen kann, die durch den eingezeichneten Punkt führt (senkrecht zur Papierebene). Auf den Balken wirken zwei horizontale Kräfte, aber der Balken bewegt sich nicht. Nun wird der Winkel zwischen $\vec { F } _ { 2 }$ und dem Balken ausgehend von 90° allmählich verkleinert. Muss der Betrag von $\vec { F } _ { 2 }$ steigen, sinken oder gleich bleiben, damit der Balken weiterhin still steht?

![](images/page_177_image_26.jpg)

(a)

![](images/page_177_image_28.jpg)

<details>
<summary>text_image</summary>

Drehachse
F₁
F₂
φ
</details>

(b)

Abb. 6.F8

Fragen 8 und 9.

**9.** Abbildung 6.F8b zeigt in Draufsicht einen waagerechten Balken, der durch die Wirkung zweier horizontal an den Enden angreifender Kräfte $\vec { F } _ { 1 }$ und $\vec { F } _ { 2 }$ in Rotation um eine Achse durch den angegebenen Punkt versetzt wird. Die Richtung von $\vec { F } _ { 2 }$ schließt mit dem Balken einen Winkel $\varphi$ ein. Ordnen Sie folgende Werte von $\varphi$ nach dem zugehöri gen Betrag der Winkelbeschleunigung des Balkens, beginnend mit dem größten Wert: 90°, 70° und 110°.
**10.** In Abb. 6.F10 sehen Sie von oben, wie fünf Kräfte glei chen Betrags auf ein (reichlich seltsames) Karussell einwirken. Es handelt sich dabei um ein Quadrat, das um einen Punkt P rotieren kann, welcher sich in der Mitte einer Seite befindet. Ordnen Sie die Kräfte nach dem Betrag des Drehmoments, das sie bezüglich Punkt P erzeugen, beginnend mit dem größten Wert.

![](images/page_178_image_5.jpg)

<details>
<summary>text_image</summary>

F₅
F₄
F₁
P
F₃
F₂
</details>

Abb. 6.F10

**11.** In Abb. 6.F11 sehen Sie eine Scheibe, die wie ein $\mathrm { K a } -$ russell um ihren Mittelpunkt rotiert, wobei zwei Kräfte ${ \vec { F } } _ { 1 }$ und ${ \vec { F } } _ { 2 }$ wirken. Während der Rotation (mit konstanter Geschwindigkeit gegen den Uhrzeigersinn) bleiben die angegebenen Winkel der Kräfte unverändert. Nun verkleinern wir den Winkel $\theta$ von ${ \vec { F } } _ { 1 }$ , wobei der Betrag der Kraft gleich bleibt. (a) Müssen wir den Betrag von $\vec { F } _ { 2 } ^ { \mathrm { ~   ~ } }$ gleichzeitig verringern, vergrößern oder konstant halten, wenn die Winkelgeschwindigkeit bei dieser Aktion konstant bleiben soll? Versetzt (b) die Kraft ${ \vec { F } } _ { 1 }$ allein und (c) die Kraft $\vec { F } _ { 2 }$ allein die Scheibe in Rotation gegen den oder im Uhrzeigersinn?

![](images/page_178_image_8.jpg)

<details>
<summary>text_image</summary>

F₁
θ
F₂
</details>

Abb. 6.F11

**12.** In Abb. 6.F12 sehen Sie den Graphen der Winkelgeschwindigkeit ω eines Karussells, das mit einer variablen Kraft angetrieben wird, in Abhängigkeit von der Zeit t. Die Beträge der Steigung des Graphen in den Zeitabschnitten 1, 3, 4 und 6 sind gleich. (a) In welchem Intervall führt die wirkende Kraft Energie vom Karussell ab? (b) Ordnen Sie die Zeitintervalle nach der Arbeit, die jeweils durch Einwirken der Kraft am Karussell verrichtet wird, beginnend mit dem größten positiven und endend mit dem größten negativen Wert. (c) Ordnen Sie die Intervalle nach der Rate, mit der die wirkende Kraft Energie überträgt, beginnend mit der größten Rate zum Karussell, endend mit der größten Rate vom Karussell weg.

![](images/page_178_chart_12.jpg)

<details>
<summary>line</summary>

| t | \(\omega\) |
| --- | --- |
| 0 | 0 |
| 1.5 | Peak |
| 2.5 | Peak |
| 3.5 | 0 |
| 4.5 | Minimum |
| 5.5 | Minimum |
| 6.5 | 0 |
</details>

Abb. 6.F12

**13.** Abbildung 6.F13 zeigt Auftragungen der Winkelposition $\theta$ gegen die Zeit t für drei Fälle, in denen eine Scheibe wie ein Karussell gedreht wird. In jedem Fall wechselt die Drehrichtung bei einer bestimmten Winkelposition $\theta _ { \mathrm { W } }$ Bestimmen Sie für jeden Fall, (a) ob man von $\theta = 0$ durch eine Drehung im Uhrzeigersinn oder gegen den Uhrzeigersinn nach $\theta _ { \mathrm { W } }$ gelangt, (b) ob ω vor, nach oder bei $t = 0$ null ist und (c) ob α positiv, negativ oder null ist.

![](images/page_178_chart_15.jpg)

<details>
<summary>line</summary>

| t | Green Line \((\theta)\) | Blue Line \((\theta)\) | Purple Line \((\theta)\) |
| --- | --- | --- | --- |
| 0 | \(90{}^{\circ}\) | ~\(35{}^{\circ}\) | ~\(45{}^{\circ}\) |
| ~1.57 | — | — | ~\(-45{}^{\circ}\) |
</details>

Abb. 6.F13

**14.** Auf den Rand einer Scheibe, die sich wie ein Karussell drehen kann, wird eine Kraft ausgeübt, um die Winkelgeschwindigkeit der Scheibe zu verändern. Ihre Anfangs- bzw. Endwinkelgeschwindigkeiten in vier Versuchen sind (a) −2 rad/s, 5 rad/s, (b) 2 rad/s, 5 rad/s, (c) −2 rad $/ \mathbf { s } ,$ $^ { - 5 }$ rad/s und (d) 2 rad $/ s , - 5$ rad/s. Ordnen Sie die Versuche in absteigender Reihenfolge nach der von dem durch die Kraft bewirkten Drehmoment an der Scheibe verrichteten Arbeit.
**15.** Abbildung 6.F15 zeigt eine homogene Metallplatte, die quadratisch war, bevor ein Viertel herausschnitten wurde. Ordnen Sie die drei beschrifteten Punkte in absteigender Reihenfolge nach dem Trägheitsmoment der Platte bezüglich einer Rotation um eine senkrechte Achse durch den jeweiligen Punkt.

![](images/page_178_image_20.jpg)

Abb. 6.F15

**16.** Abbildung 6.F16 zeigt drei flache Scheiben (mit dem selben Radius), die sich wie Karussells um ihre Mittelpunkte drehen können. Jede Scheibe besteht aus denselben zwei Materialien, von denen das eine dichter als das andere ist (Dichte ist Masse pro Volumeneinheit). Bei den Scheiben 1 und 3 bildet das dichtere Material die äußere Hälfte der Flä- che der Scheibe; bei Scheibe 2 bildet dieses Material die innere Hälfte der Fläche der Scheibe. Nun werden tangential zu den Scheiben identische Kräften ausgeübt, wie gezeigt entweder am äußeren Rand oder an der Grenzfläche der beiden Materialien. Ordnen Sie die Scheiben in absteigender Reihenfolge (a) nach dem Drehmoment um die Scheibenmitte, (b) nach ihrem Trägheitsmoment bezüglich der Scheibenmitte und (c) nach der resultierenden Winkelbeschleunigung der Scheibe.

![](images/page_179_image_2.jpg)

<details>
<summary>text_image</summary>

dichter
F
</details>

Scheibe 1

![](images/page_179_image_4.jpg)

<details>
<summary>text_image</summary>

weniger dicht
F
</details>

Scheibe 2

![](images/page_179_image_6.jpg)

Scheibe 3

## Abb. 6.F16

**17.** Abbildung 6.F17a zeigt einen Meterstab, der zur Hälfte aus Holz und zur Hälfte aus Stahl besteht und an seinem hölzernen Ende bei O drehbar gelagert ist. An seinem stählernen Ende bei a wirkt eine Kraft F⃗. In Abb. 6.F17b ist der Stab umgedreht und ist jetzt an seinem stählernen Ende bei O′ drehbar gelagert; dieselbe Kraft F⃗ wirkt jetzt an seinem hölzernen Ende bei a′. Ist die resultierende Winkelbeschleunigung im Fall von Abb. 6.F17a größer als, kleiner als oder gleich groß wie in Abb. 6.F17b?

![](images/page_179_image_11.jpg)

## Abb. 6.F17

**18.** Abbildung 6.F18 zeigt drei Scheiben mit homogener Massenverteilung; die Radien R und die Massen M sind angegeben. Jede Scheibe kann sich um ihre Mittelachse (senkrecht zur Scheibenfläche und durch ihre Mitte) drehen. Ordnen Sie die Scheiben in absteigender Reihenfolge nach ihren Trägheitsmomenten bezüglich ihrer Mittelachsen.

![](images/page_179_image_14.jpg)

<details>
<summary>natural_image</summary>

Three metallic circular objects with gradient shading, arranged vertically (no text or symbols)
</details>

R :1 m 2 m 3 m M:26 kg 7 kg 3 kg

(a)

(b)

(c)

Abb. 6.F18

# 7 Rollbewegung, Drehmoment und Drehimpuls

## 7.1 Die Rollbewegung

## Physikalische Motivation

Wie wir in Kap. 10 diskutiert haben, macht die Untersuchung von Rotationen einen wesentlichen Teil der Physik aus. Die wichtigste Anwendung dieses Aspekts der Physik ist wohl die Rollbewegung von Rädern und ähnlichen Objekten. Diese Anwendung ist seit Jahrtausenden eine der Grundlagen der menschlichen Zivilisation. Als die Menschen der Osterinsel das Material für ihre riesigen Steinstatuen aus dem Steinbruch brachen und über die Insel bewegten, schleppten sie es vermutlich über Baumstämme, die als Rollen dienten. Viel später, als Siedler im 18. und 19. Jahrhundert auf dem Zug nach Westen durch Amerika fuhren, rollte ihr Besitz zunächst auf Planwagen, später dann mit der Eisenbahn – immer aber auf Rädern. Heutzutage ist unsere Welt – ob wir es mögen oder nicht – voller Autos, Lastwagen, Motorräder, Fahrräder und anderer rollender Fahrzeuge.

Die Physik und Technik der Rollbewegung ist so alt, dass man meinen könn-$\mathbf { t e } ,$ hier gäbe es keine neuen Ideen mehr zu entdecken. Trotzdem wurden solche großen wirtschaftlichen Erfolge wie Skateboards oder Inline-Skates erst vor relativ kurzer Zeit erfunden. Straßenrodeln ist ein ganz neuer Trend, und der selbstbalancierende Segway (Abb. 7.1) hat das Potenzial, die Art und Weise zu verändern, wie wir uns in Städten fortbewegen. Neue Anwendungen der Rollbewegung sind immer noch für eine Überraschung gut. Als Einstieg in die dafür relevante Physik wollen wir zuerst die Rollbewegung als solche verstehen.

## Abb. 7.1

Der selbstbalancierende Segway Personal Transporter wird mittlerweile auch bei der Polizei eingesetzt. Fotoaufnahme beim Bürgerfest im Rahmen der offiziellen Feiern zum 20. Tag der Deutschen Einheit vom 1.–3. Oktober 2010 in Bremen, hier auf dem Grasmarkt vor dem Neuen Rathaus [Quelle: Jocian/CC-AS-3.0].

## 7.1.1 Die Rollbewegung als Mischung aus Translation und Rotation

Wir betrachten das Rad eines Fahrrads, das mit konstanter Geschwindigkeit in einer reinen Rollbewegung (d. h. ohne zu gleiten) an uns vorbeifährt. Wie Sie Abb. 7.2 entnehmen können, bewegt sich der Schwerpunkt O des Rads mit der konstanten Geschwindigkeit $\nu _ { \mathrm { S } }$ vorwärts. Auch der Punkt P auf der Straße, der mit dem Rad in Kontakt steht, bewegt sich mit $\nu _ { S } ,$ sodass er sich stets direkt unter O befindet.

Während eines Zeitintervalls t legen sowohl O als auch P die Strecke s zurück. Aus der Sicht des Radfahrers dreht sich das Rad um einen Winkel θ um seinen Mittelpunkt, wobei der Punkt auf dem Reifen, der die Straße bei $t = 0$ berührte, einen Bogen mit der Länge s durchläuft. Gleichung 6.14 gibt die Beziehung zwischen der Bogenlänge s und dem Drehwinkel θ als Funktion des Radius R des Rads an:

$$
s = \theta R. \tag {7.1}
$$

![](images/page_180_image_11.jpg)

![](images/page_180_image_12.jpg)

<details>
<summary>natural_image</summary>

Two police officers in uniform and helmets standing beside a seotroller on a cobblestone street (no visible text or symbols)
</details>

![](images/page_180_image_13.jpg)

<details>
<summary>text_image</summary>

O
v_S
θ
v_S
P
s
P
s
</details>

## Abb. 7.2

Der Schwerpunkt O eines rollenden Rads legt eine Strecke s mit der Geschwindigkeit $\vec { \nu } _ { \mathrm { S } }$ zurück, während sich das Rad um einen Winkel θ dreht. Der Punkt P, in dem das Rad die Straße berührt, bewegt sich dabei um dieselbe Strecke s.

## Abb. 7.3

Das Rollen eines Rads als Überlagerung einer reinen Translation und einer reinen Rotation. (a) Reiner Rotationsanteil: Alle Punkte des Rads bewegen sich mit derselben Winkelgeschwindigkeit ω. Alle Punkte auf der Außenkante bewegen sich mit derselben linearen Geschwindigkeit $\nu = \nu _ { S } .$ Eingezeichnet sind die linearen Geschwindigkeiten v⃗ zweier solcher Punkte, oben (T) und unten (P). (b) Reiner Translationsanteil: Alle Punkte des Rads bewegen sich mit derselben linearen Geschwindigkeit $\vec { \nu } _ { \mathrm { S } }$ wie der Mittelpunkt nach rechts. (c) Rollbewegung als Mischung von (a) und (b).

(a) reine Rotation

![](images/page_181_image_4.jpg)

<details>
<summary>text_image</summary>

v⃗ = v⃗_S
T
ω
O
P
v⃗ = -v⃗_S
</details>

![](images/page_181_image_5.jpg)

(b) reine Translation

![](images/page_181_image_7.jpg)

<details>
<summary>text_image</summary>

v⃗ = v⃗_S
T
v⃗_S
O
P
v⃗ = v⃗_S
</details>

![](images/page_181_image_8.jpg)

(c) Rollbewegung

![](images/page_181_image_10.jpg)

<details>
<summary>text_image</summary>

T
ω
O
P
v = 2v_S
v_S
v = -v_S + v_S = 0
</details>

Die lineare Geschwindigkeit $\nu _ { \mathrm { S } }$ des Radmittelpunkts ist gegeben durch ds∕dt. (Die Mitte des Rads soll der Einfachheit halber gleichzeitig dessen Schwerpunkt sein – d. $\mathrm { h } _ { \star } ,$ wir nehmen an, das Rad habe eine homogene Massenverteilung.) Die Winkelgeschwindigkeit ω des Rads bezüglich seines Mittelpunkts ist dθ∕dt. Wir leiten Gl. 7.1 nach der Zeit ab (wobei R konstant gehalten wird) und erhalten für das reine Rollen (ohne Gleiten)

$$
\nu_ {S} = \omega R. \tag {7.2}
$$

Abbildung 7.3 interpretiert die Rollbewegung eines Rads als Überlagerung einer reinen Translation und einer reinen Rotation. In Abb. 7.3a sehen Sie den reinen Rotationsanteil (mit fest stehender Drehachse): Jeder Punkt des Rads dreht sich mit der Winkelgeschwindigkeit ω um die Achse. Wie Sie sich erinnern werden, haben wir diese Art der Bewegung ausführlich in Kap. 10 besprochen. Die lineare Geschwindigkeit $\nu _ { S }$ jedes Punkts an der Außenkante des Rads ist durch Gl. 7.2 gegeben. Abbildung 7.3b zeigt den reinen Translationsanteil (das Rad bewegt sich vorwärts, ohne sich zu drehen): Jeder Punkt des Rads bewegt sich mit der Geschwindigkeit $\nu _ { \mathrm { S } }$ nach rechts.

Die tatsächliche Rollbewegung des Rads (Abb. 7.3c) lässt sich nun als Mischung der Anteile in den Abb. 7.3a und 7.3b beschreiben. Wie Sie erkennen können, ist der untere Teil des Rads (Punkt P) stationär, während sich der obere Teil (Punkt T) schneller bewegt als alle anderen Punkte auf dem Rand des Rads, nämlich mit der Geschwindigkeit $2 \nu _ { \mathrm { S } } ,$ Abbildung 7.4, ein Foto eines rollenden Rads, veranschaulicht Ihnen dieses Ergebnis: Die Speichen im unteren Bereich des Rads sind schärfer abgebildet als diejenigen im oberen Bereich, woraus Sie folgern können, dass sich die oberen Speichen schneller bewegen als die unteren.

Analog zu Abb. 7.3 lässt sich die Bewegung jedes beliebigen runden Körpers, der ohne zu gleiten über eine Fläche rollt, in einen Translations- und einen Rotationsanteil trennen.

![](images/page_181_image_16.jpg)

<details>
<summary>natural_image</summary>

Black and white photo of a bicycle wheel rim (no text or symbols visible)
</details>

Abb. 7.4 Foto eines rollenden Rads. Die Speichen im oberen Teil des Rads sind weniger scharf abgebildet, weil sie sich schneller bewegen als die Speichen im unteren Teil (siehe Abb. 7.3c) [Quelle: Alice Halliday].

## 7.1.2 Die Rollbewegung als reine Rotation

Abbildung 7.5 legt eine alternative Interpretation der Rollbewegung nahe: als reine Rotation um eine Achse, die stets durch den Berührungspunkt zwischen Straße und Rad verläuft. Entsprechend betrachten wir das Rollen jetzt als reine Rotation um eine Achse durch P (Abb. 7.3c), senkrecht zur Papierebene. Die in Abb. 7.5 eingezeichneten Vektoren stellen dann die momentanen Geschwindigkeiten der zugehörigen Punkte auf dem Rand des Rads dar. Welche Winkelgeschwindigkeit bezüglich dieser Achse ordnet ein ruhender Beobachter einem rollenden Rad zu? Dieselbe Winkelgeschwindigkeit ω, so lautet die Antwort, die er auch für eine reine Rotation um eine Achse durch den Schwerpunkt des Rads angeben würde.

Um diese Antwort nachzuprüfen, wollen wir die lineare Geschwindigkeit des höchsten Punkts des rollenden Rads aus der Sicht eines ruhenden Beobachters in der beschriebenen Weise berechnen. Der Radius des Rads sei R, folglich beträgt der Abstand zwischen T und P in Abb. 7.5 2R, und die lineare Geschwindigkeit in T ist durch Gl. 7.2 gegeben:

$$
\nu_ {\mathrm{T}} = \omega (2 R) = 2 (\omega R) = 2 \nu_ {\mathrm{S}}.
$$

Dies stimmt, wie Sie sofort sehen, mit Abb. 7.3c überein. In analoger Weise können Sie nun die linearen Geschwindigkeiten in den Punkten O und P, wie sie Abb. 7.3c angibt, nachrechnen.

## KONTROLLFRAGE 1

Ein Clown fährt auf einem Fahrrad durch die Manege. Der Radius des Vorderrads ist nur halb so groß wie der des Hinterrads. (a) Ist die lineare Geschwindigkeit des höchsten Punkts des Hinterrads größer als, kleiner als oder ebenso groß wie die Geschwindigkeit des höchsten Punkts des Vorderrads? (b) Ist die Winkelge schwindigkeit des Hinterrads größer als, kleiner als oder ebenso groß wie diejenige des Vorderrads?

## 7.2 Kräfte und die kinetische Energie der Rollbewegung

## Lernziele

Nach dem Durcharbeiten dieses Abschnitts sollten Sie in der Lage sein, . . .

• die kinetische Energie eines Körpers für eine reine Rollbewegung als Summe der kinetischen Energie der Translation des Schwerpunkts und der kinetischen Energie der Rotation um den Schwerpunkt zu berechnen,
• die Beziehung zwischen der Arbeit an einem reibungslos rollenden Objekt und der Änderung seiner kinetischen Energie anzugeben und anzuwenden,
• für eine reine Rollbewegung (ohne Gleiten) mithilfe der Energieerhaltung eine Beziehung zwischen der anfänglichen Energie und der Energie zu einem späteren Zeitpunkt anzugeben,
• ein Kräftediagramm eines beschleunigenden Körpers zu skizzieren, der auf einer horizontalen Fläche oder einer geneigten Ebene aufwärts- oder abwärtsrollt,
• die Beziehung zwischen der Beschleunigung des Schwerpunkts und der Winkelbeschleunigung anzugeben und anzuwenden,
• für eine Rollbewegung eines Objekts auf einer geneigten Ebene die Beziehung zwischen der Beschleunigung des Objekts, seinem Trägheitsmoment und dem Neigungswinkel der Ebene anzuwenden.

![](images/page_182_image_19.jpg)

<details>
<summary>text_image</summary>

T
O
</details>

Drehachse in P

## Abb. 7.5

Die Rollbewegung kann als reine Rotation mit der Winkelgeschwindigkeit ω um eine Achse betrachtet werden, die stets durch P führt. Die Vektoren geben die momentanen linearen Geschwindigkeiten ausgewählter Punkte auf dem Rand des Rads an. Sie erhalten diese Vektoren durch eine Kombination des Translations- und des Rotationsanteils in Abb. 7.3.

![](images/page_182_image_23.jpg)

![](images/page_183_image_1.jpg)

## Schlüsselideen

• Ein rollendes Rad besitzt die kinetische Energie

$$
K = \frac {1}{2} I _ {\mathrm{S}} \omega^ {2} + \frac {1}{2} M \nu_ {\mathrm{S}} ^ {2},
$$

wobei $I _ { \mathrm { S } }$ das Trägheitsmoment des Rads um seinen Schwerpunkt ist und M seine Masse.

• Wenn das Rad beschleunigt wird, aber noch rollt, ohne zu gleiten, hängt die Beschleunigung ${ \vec { a } } _ { S }$ des Schwerpunkts gemäß

$$
a _ {S} = \alpha R
$$

mit der Winkelbeschleunigung α um die Mittelachse zusammen.

• Wenn ein Rad eine geneigte Ebene mit dem Neigungswinkel θ abwärtsrollt, ist seine Beschleunigung entlang einer x-Achse parallel zu der Ebene

$$
a _ {\mathrm{S}, x} = - \frac {g \sin \theta}{1 + I _ {\mathrm{S}} / (M R ^ {2})}.
$$

## 7.2.1 Die kinetische Energie der Rollbewegung

Wir wollen nun die kinetische Energie eines rollenden Rads aus der Sicht eines ruhenden Beobachters ermitteln. Betrachten wir das Rollen als reine Rotation um eine Achse durch P (siehe Abb. 7.5), so liefert uns Gl. 6.24

$$
K = \frac {1}{2} I _ {\mathrm{p}} \omega^ {2} \tag {7.3}
$$

mit ω als Winkelgeschwindigkeit des Rads und $I _ { \mathrm { P } }$ als Trägheitsmoment der Rotation um die Achse durch P. Aus dem Steinerschen Satz $( \mathrm { G l . }   6 . 2 6 , I = I _ { \mathrm { S } }   +   M h ^ { 2 } )$ folgt dann

$$
I _ {\mathrm{P}} = I _ {\mathrm{S}} + M R ^ {2}, \tag {7.4}
$$

wobei M die Masse des Rads ist und $I _ { \mathrm { S } }$ das Trägheitsmoment der Rotation um eine Achse durch den Schwerpunkt. Der Radius R entspricht dem senkrechten Abstand h. Wir setzen Gl. 7.4 in Gl. 7.3 ein und erhalten so

$$
K = \frac {1}{2} I _ {\mathrm{S}} \omega^ {2} + \frac {1}{2} M R ^ {2} \omega^ {2},
$$

woraus mithilfe von Gl. $7 . 2 \: ( \nu _ { S } = \omega R )$ folgt

$$
K = \frac {1}{2} I _ {\mathrm{S}} \omega^ {2} + \frac {1}{2} M \nu_ {\mathrm{S}} ^ {2}. \tag {7.5}
$$

Den Term $\frac { 1 } { 2 } I _ { S } \omega ^ { 2 }$ können wir als kinetische Energie der Rotation des Rads um eine Achse durch seinen Schwerpunkt (Abb. 7.3a) interpretieren; $\frac { 1 } { 2 } M \nu _ { S } ^ { 2 }$ ist die kinetische Energie der Translationsbewegung des Schwerpunkts des Rads (Abb. 7.3b). Wir merken uns die folgende Regel:

![](images/page_183_image_21.jpg)

Ein rollendes Objekt besitzt zwei Formen kinetischer Energie: die Rotationsenergie $\frac { 1 } { 2 } \dot { I _ { S } \omega ^ { 2 } }$ infolge der Rotation um seinen Schwerpunkt und die Translationsenergie $\frac { 1 } { 2 } M \bar { \nu _ { S } ^ { 2 } }$ infolge der Translation seines Schwerpunkts.

## 7.2.2 Die Kräfte bei der Rollbewegung

## Rollen und Reibung

Ein Rad, das mit konstanter Geschwindigkeit rollt wie in Abb. 7.2 gezeigt, gleitet am Berührungspunkt P nicht. Folglich wirken dort keine Reibungskräfte. Wird das Rad hingegen durch eine resultierende Kraft beschleunigt oder verzögert, so verursacht diese Kraft eine Beschleunigung ${ \vec { a } } _ { S }$ des Schwerpunkts in der Bewe gungsrichtung. Sie bewirkt außerdem, dass sich das Rad schneller oder langsamer dreht – d. h., sie verursacht auch eine Winkelbeschleunigung α bezüglich des Schwerpunkts. Damit das Rad durch die Wirkung dieser Beschleunigungen nicht zu gleiten beginnt, muss dem eine Reibungskraft in Punkt P entgegenwirken.

Solange das Rad nicht gleitet, handelt es sich dabei um eine statische Reibungskraft (Haftreibung) ${ \vec { f } } _ { s } .$ Die Beträge der linearen Beschleunigung ${ \vec { a } } _ { S }$ und der Winkelbeschleunigung α können wir dann durch Ableiten von Gl. 7.2 nach der Zeit (bei konstantem $R )$ zueinander in Beziehung setzen. Auf der linke Seite ist $\mathrm { d } \nu _ { \mathrm { S } } / \mathrm { d } t$ gleich $a _ { S } ,$ auf der rechten Seite ist dω∕dt gleich α. Für reines (gleitfreies) Rollen gilt demnach

$$
a _ {S} = \alpha R. \tag {7.6}
$$

Sobald das Rad gleitet, wirkt in P eine kinetische Reibungskraft (Gleitreibung) $\vec { f } _ { \mathrm { k } }$ und wir können Gl. 7.6 nicht mehr anwenden. Unsere folgende Diskussion werden wir auf das reine Rollen beschränken.

In Abb. 7.6 sehen Sie ein Rad, das über eine ebene Fläche rollt und dabei beschleunigt wird (denken Sie an ein Fahrrad zu Beginn eines Rennens). In Folge der Beschleunigung droht Punkt $\mathrm { P } _ { \mathrm { r } }$ der tiefste Punkt des Rads, nach links zu rutschen. Dem wirkt in P eine nach rechts gerichtete Reibungskraft entgegen. Solange das Rad nicht gleitet, handelt es sich um eine statische Reibungskraft ${ \vec { f } } _ { s } ,$ und wir können Gl. 7.6 anwenden. (Ohne das Wirken der Reibungskräfte wären Radrennen ziemlich langweilig, weil kein Rennfahrer vom Fleck käme.)

Um mit Abb. 7.6 die Verzögerung eines Rads zu beschreiben, sind zwei Änderungen anzubringen: Sowohl die Beschleunigung ${ \vec { a } } _ { S }$ des Schwerpunkts als auch die Reibungskraft $\vec { f } _ { s }$ in Punkt P müssen dann nach links zeigen.

## Die Rollbewegung auf einer geneigten Ebene

In Abb. 7.7 sehen Sie, wie ein runder, homogener Körper mit der Masse M und dem Radius R entlang einer x-Achse von einer Ebene abrollt, die relativ zur Waagerechten um einen Winkel θ geneigt ist. Gesucht ist ein Ausdruck für die Beschleunigung $a _ { \mathrm { S } , x }$ des Körpers während des Abrollens. Um die Aufgabe zu lösen, verwenden wir das zweite Newtonsche Gesetz sowohl in linearer als auch in Winkelschreibweise $( F _ { \mathrm { g e s } } = M a \mathrm { b z w . } \tau _ { \mathrm { g e s } } = I \alpha )$

Zunächst zeichnen wir die wirkenden Kräfte ein (vgl. Abb. 7.7):

1. Die Schwerkraft $\vec { F } _ { \mathrm { G } }$ wirkt senkrecht nach unten. Der zugehörige Vektor beginnt im Schwerpunkt des Körpers. Die Komponente der Kraft entlang der x-Achse ist $F _ { \mathrm { G } }$ sin $\theta$ (äquivalent zu Mg sin θ).
2. Senkrecht zur Ebene der Rampe wirkt eine Normalkraft $\vec { N } .$ Sie greift am Berührungspunkt P an, der zugehörige Vektor wurde in Abb. 7.7 jedoch so weit nach oben verschoben, dass er ebenfalls im Schwerpunkt beginnt.
3. Im Berührungspunkt P greift die statische Reibungskraft $\vec { f } _ { s }$ an, deren Richtung die Rampe aufwärts zeigt. (Sie erkennen, warum dies so ist: Ohne das Wirken der Reibung würde der Körper die Rampe abwärts gleiten. Um dies zu verhindern, muss die Kraft die Rampe hinauf wirken.)

Das zweite Newtonsche Gesetz für die x-Komponenten der Kräfte in Abb. 7.7 $( F _ { \mathrm { g e s } , x } = m a _ { x } )$ können wir nun wie folgt formulieren:

$$
f _ {\mathrm{s}} - M g \sin \theta = M a _ {\mathrm{S}, x}. \tag {7.7}
$$

Dieser Ausdruck enthält zwei Unbekannte, $f _ { S }$ und $a _ { S , x ^ { \ast } }$ (Wir können nicht davon ausgehen, dass $f _ { S }$ den Maximalwert $f _ { \mathrm { s , m a x } }$ erreicht. Wir wissen lediglich, dass der Betrag von $f _ { S }$ gerade ausreicht, um das Abwärtsgleiten des Körpers zu verhindern.)

![](images/page_184_image_18.jpg)

<details>
<summary>text_image</summary>

u_S
P
f_s
</details>

Abb. 7.6

Ein Rad rollt ohne zu gleiten über eine waagerechte Fläche, wobei eine lineare Beschleunigung ${ \vec { a } } _ { \mathrm { S } _ { \mathrm { s } } }$ wirkt. Eine statische Reibungskraft $f _ { s }$ wirkt in P dem Wegrutschen dieses Punkts nach links entgegen.

![](images/page_184_image_21.jpg)

<details>
<summary>text_image</summary>

N
F_G sin θ
R
f_s
x
P
θ
θ
F_G cos θ
F_G
</details>

Abb. 7.7

Ein runder, homogener Körper mit dem Radius R rollt von einer geneigten Ebene ab. Auf den Körper wirken die Gravitationskraft $\vec { F } _ { \mathrm { G } } ,$ eine Normalkraft $\vec { N }$ und eine die Rampe aufwärts zeigende Reibungskraft ${ \vec { f } } _ { \mathrm { s } } .$ (Der Übersichtlichkeit halber wurde der Vektor N⃗ so verschoben, dass sein Anfangspunkt auf dem Schwerpunkt liegt.

Wir wollen nun das zweite Newtonsche Gesetz in Winkelschreibweise auf die Rotation des Körpers um seinen Schwerpunkt anwenden. Zunächst notieren wir mithilfe von $\mathrm { G l . } \; 6 . 3 0 \; ( \tau = r _ { \perp } F )$ die Drehmomente bezüglich dieses Punkts. Die Reibungskraft $\vec { f } _ { s }$ mit dem Hebelarm $R$ erzeugt das Drehmoment $R f _ { S } ;$ es ist positiv, denn es bewirkt eine Rotation des Körpers gegen den Uhrzeigersinn (siehe Abb. 7.7). Die Hebelarme der Kräfte $\vec { F } _ { \mathrm { G } }$ und $\vec { N }$ sind null, folglich erzeugen diese Kräfte kein Drehmoment. Wir formulieren also das zweite Newtonsche Gesetz $( \tau _ { \mathrm { g e s } } = I \alpha )$ bezüglich einer Achse durch den Schwerpunkt des Körpers:

$$
R f _ {\mathrm{s}} = I _ {\mathrm{S}} \alpha . \tag {7.8}
$$

Auch diese Gleichung enthält zwei Unbekannte: $f _ { S }$ und $\alpha ,$

Da es sich hier um eine reine Rollbewegung handelt, können wir mithilfe von Gl. $7 . 6 \; ( a _ { \mathrm { S } } = \alpha R )$ die unbekannten Größen $a _ { \mathrm { S } , x }$ und α zueinander in Beziehung setzen. Hierbei ist allerdings Vorsicht geboten, weil $a _ { \mathrm { S } , x }$ negativ ist (in negative x-Richtung zeigt), α dagegen positiv (gegen den Uhrzeigersinn). Wir setzen also $- \alpha _ { S , x / R }$ für α in Gl. 7.8 ein und lösen nach $f _ { S }$ auf:

$$
f _ {\mathrm{s}} = - I _ {S} \frac {a _ {\mathrm{S} , x}}{R ^ {2}}. \tag {7.9}
$$

Nun setzen wir noch die rechte Seite dieser Gleichung für $f _ { S }$ in Gl. 7.7 ein und erhalten

$$
a _ {S, x} = - \frac {g \sin \theta}{1 + I _ {S} / (M R ^ {2})}. \tag {7.10}
$$

Mithilfe dieser Gleichung können wir die lineare Beschleunigung $a _ { \mathrm { S } , x }$ eines beliebigen Körpers beim Abrollen von einer um den Winkel θ bezüglich der Waagerechten geneigten Ebene berechnen.

## KONTROLLFRAGE 2

Zwei identische Scheiben A und B rollen mit gleicher Geschwindigkeit über den Boden. Scheibe A rollt eine geneigte Ebene hinauf und erreicht die maximale Hö- he h. Scheibe B rollt eine ebensolche Ebene hinauf, wobei aber keinerlei Reibungskräfte wirken. Erreicht B die gleiche, eine geringere oder eine größere Höhe als A?

## 7.3 Das Jo-Jo

![](images/page_185_image_12.jpg)

## Lernziele

Nach dem Durcharbeiten dieses Abschnitts sollten Sie in der Lage sein, . . .

• ein Kräftediagramm für ein Jo-Jo zu skizzieren, das sich an seiner Schnur nach oben oder unten bewegt,
• zu verstehen, dass ein Jo-Jo im Prinzip ein Objekt ist, das auf einer geneigten Ebene mit einem Neigungswinkel von 90° aufwärts- oder abwärtsrollt,
• für ein Jo-Jo, das sich an seiner Schnur aufwärts oder abwärts bewegt, die Beziehungen zwischen seiner Beschleunigung und seinem Trägheitsmoment anzugeben,
• die Spannung (Seilkraft) in der Schnur eines Jo-Jos anzugeben, während es sich aufwärts oder abwärts bewegt.

![](images/page_185_image_20.jpg)

## Schlüsselideen

• Ein Jo-Jo, das sich an seiner Schnur aufwärts oder abwärts bewegt, kann als Rad behandelt werden, das sich auf einer geneigten Ebene mit dem Neigungswinkel 90° bewegt.

## 7.3.1 Das Jo-Jo

Ein Jo-Jo ist ein Physiklabor für die Hosentasche. Rollt es eine Strecke h abwärts, so verliert es die potenzielle Energie mgh, gewinnt aber dafür kinetische Energie der Translation $( \frac { 1 } { 2 } m \nu _ { \mathrm { S } } ^ { 2 } )$ und der Rotation $( \frac { 1 } { 2 } I _ { \mathrm { S } } \omega ^ { 2 } )$ . Rollt das Jo-Jo wieder aufwärts, so verliert es kinetische und gewinnt potenzielle Energie.

Bei einer modernen Variante ist das untere Ende des Fadens nicht fest an die Achse der Rolle gebunden, sondern nur darum geschlungen. Kommt die Rolle am Ende des Fadens an, so übt der Faden eine aufwärts gerichtete Kraft auf die Achse aus. Die Rolle fährt fort sich zu drehen (die Achse rotiert innerhalb der Fadenschlinge), wobei sie nur kinetische Energie der Rotation besitzt. Das Jo-Jo „schläft“, bis Sie es „aufwecken“, indem Sie den Faden kurz nach oben ziehen, wodurch er sich wieder auf die Achse wickelt und die Rolle aufwärts zu steigen beginnt. Die kinetische Energie der Rotation der Rolle in der Fadenschlinge (und damit die maximale „Schlafzeit“ des Jo-Jos) können Sie deutlich steigern, indem Sie die Rolle zu Beginn nach unten werfen, ihr also Anfangs(winkel)geschwindigkeiten $\nu _ { \mathrm { S } }$ bzw. ω verschieden von null verleihen.

Wir suchen nun einen Ausdruck für die lineare Beschleunigung $a _ { \mathrm { S } }$ eines abwärts abrollenden Jo-Jos. Dazu könnten wir das zweite Newtonsche Gesetz anwenden, analog zu unserem Vorgehen im Fall des von einer Rampe abrollenden Körpers (Abb. 7.7). Unsere Analyse unterscheidet sich von diesem Fall nur in wenigen Punkten:

1. Das Jo-Jo rollt keine um einen mehr oder weniger flachen Winkel θ geneigte Ebene hinab, sondern es rollt an einem senkrecht hängenden Faden $\left( \theta = 9 0 ^ { \circ } \right)$
2. Das Jo-Jo rollt nicht auf seinem Außenrand, sondern auf einer Achse, die sich beim Radius $R _ { 0 }$ befindet (siehe Abb. 7.8a).
3. Das Jo-Jo wird nicht von einer Reibungskraft $\vec { f } _ { s }$ gebremst, sondern von einer Seilkraft bzw. Spannung ${ \vec { T } } ,$ welche der Faden ausübt (siehe Abb. 7.8b).

Diese Analyse führt uns wieder zu Gl. 7.10. Wir ändern deshalb in dieser Gleichung lediglich die Notation und setzen $\theta = 9 0 ^ { \circ }$ . So erhalten wir für die lineare Beschleunigung:

$$
a _ {\mathrm{S}} = - \frac {g}{1 + I _ {\mathrm{S}} / (M R _ {0} ^ {2})} \tag {7.11}
$$

mit $I _ { S }$ als Trägheitsmoment für die Rotation des Jo-Jos um seine Mittelachse und M als Masse des Jo-Jos. Wenn das Jo-Jo am Faden wieder aufwärtssteigt, wirkt die selbe abwärtsgerichteteBeschleunigung, weil sich die in Abb. 7.8b eingezeichneten Kräfte nicht verändert haben.

## 7.4 Eine erweiterte Definition des Drehmoments

## Lernziele

Nach dem Durcharbeiten dieses Abschnitts sollten Sie in der Lage sein, . . .

• zu verstehen, dass das Drehmoment eine Vektorgröße ist,
• zu verstehen, dass bei der Berechnung eines Drehmoments immer der Punkt angegeben werden muss, auf den es sich bezieht,
• das von einer Kraft auf ein Teilchen ausgeübte Drehmoment zu berechnen, indem Sie das Kreuzprodukt des Ortsvektors des Teilchens und des Kraftvektors entweder in Einheitsvektoren- oder in Betrag-Winkel-Schreibweise bilden,
• die Rechte-Hand-Regel für Kreuzprodukte anzuwenden, um die Richtung eines Drehmomentvektors zu bestimmen.

![](images/page_186_image_21.jpg)

<details>
<summary>text_image</summary>

R
R₀
(a)
T
R₀
Fₖ
(b)
</details>

Abb. 7.8

(a) Querschnitt eines Jo-Jos. Der Faden, dessen Dicke wir vernachlässigen wollen, ist um eine Achse mit dem Radius $R _ { 0 }$ gewickelt. (b) Kräftediagramm für das fallende Jo-Jo. Gezeigt ist nur die Achse.

![](images/page_186_image_24.jpg)

![](images/page_187_image_1.jpg)

## Schlüsselideen

• In drei Dimensionen ist das Drehmoment eine Vektorgröße, die relativ zu einem Bezugspunkt (üblicherweise dem Ursprung des gewählten Koordinatensystems) als

$$
\vec {\tau} = \vec {r} \times \vec {F}
$$

definiert ist, wobei $\vec { F }$ eine Kraft ist, die auf ein Teilchen wirkt, und $\vec { r }$ ein Ortsvektor, der die Position des Teilchens relativ zu dem Bezugspunkt angibt.

• Der Betrag von $\vec { \tau }$ ist durch

$$
\tau = r F \sin \varphi = r F _ {\perp} = r _ {\perp} F
$$

gegeben, wobei $\varphi$ der Winkel zwischen $\vec { F }$ und $\vec { r }$ ist, $F _ { \perp }$ die Komponente von $\vec { F }$ senkrecht zu $\vec { r }$ und $r _ { \perp }$ der Hebelarm von ${ \vec { F } } .$

• Die Richtung von $\stackrel { \rightarrow } { \tau } = \stackrel { \rightarrow } { r } \times \stackrel { \rightarrow } { F }$ kann durch die Rechte-Hand-Regel für Kreuzprodukte bestimmt werden.

## 7.4.1 Ein erweiterter Blick auf das Drehmoment

In Kap. 10 hatten wir das Drehmoment τ eines starren, um eine feste Achse drehbaren Körpers definiert. Jeder Punkt des Körpers muss sich dabei auf einer Kreisbahn um diese Achse bewegen. Wir erweitern unsere Definition nun auf ein einzelnes Teilchen, das sich entlang eines beliebigen Wegs relativ zu einem festen Punkt (anstelle einer festen Achse) bewegt. Dieser Weg muss jetzt keine Kreisbahn mehr sein, weshalb wir das Drehmoment als Vektor τ⃗ mit beliebiger Richtung formulieren müssen.

Abbildung 7.9a zeigt ein solches Teilchen in einem Punkt A der xy-Ebene. Eine Kraft $\vec { F }$ wirkt in dieser Ebene auf das Teilchen, dessen Ort relativ zum Ursprung O durch den Ortsvektor $\vec { r }$ gegeben ist. Das relativ zum festen Punkt O auf das Teilchen wirkende Drehmoment τ⃗ ist definiert als

$$
\vec {\tau} = \vec {r} \times \vec {F}. \tag {7.12}
$$

Das hier auftretende Vektorprodukt (oder Kreuzprodukt) berechnen wir mithilfe der in Anhang D gegebenen Regeln. Um die Richtung von $\vec { \tau }$ zu ermitteln, verschieben wir den Vektor $\vec { F }$ (ohne Änderung der Richtung), bis die Anfangspunkte der im Vektorprodukt auftretenden Vektoren übereinander zu liegen kommen (siehe Abb. 7.9b). Dann wenden wir die Rechte-Hand-Regel an (Abb. 6.5c) und krümmen die Finger der rechten Hand von $\vec { r }$ (dem ersten Vektor) nach $\vec { F }$ (dem zweiten Vektor). Der ausgestreckte rechte Daumen zeigt nun in die Richtung von ⃗τ. In Abb. 7.9b ist dies die positive Richtung der z-Achse.

Nun ist noch der Betrag von $\vec { \tau }$ zu berechnen. Dazu verwenden wir die allgemeine Beziehung c = ab sin $\varphi$ (vgl. Anhang D) und erhalten

$$
\tau = r F \sin \varphi , \tag {7.13}
$$

Abb. 7.9 Zur Definition des Drehmoments: (a) Eine Kraft F⃗ in der xy-Ebene wirkt auf ein Teilchen im Punkt A. (b) Diese Kraft erzeugt ein Drehmoment $\vec { \tau } = \vec { r } \times \vec { F }$ relativ zu O auf das Teilchen. Die Rechte-Hand-Regel für Kreuzprodukte ergibt, dass ⃗τ in positiver z-Richtung zeigt. Der Betrag von ⃗τ ist gegeben durch $r F _ { \perp }$ (b) bzw. $r _ { \perp } F$ (c).

![](images/page_187_image_18.jpg)

<details>
<summary>text_image</summary>

z
O
y
r
A
φ
F
x
</details>

(a)

![](images/page_187_image_20.jpg)

<details>
<summary>text_image</summary>

z
τ (= r × F)
F (Anfangspunkt auf den Ursprung verschoben)
O
φ
y
r
F⊥
φ
A
φ
F
x
</details>

(b)

![](images/page_187_image_22.jpg)

<details>
<summary>text_image</summary>

z
τ
O
y
r⊥
r
φ
A
F
x
Richtung der Kraft
F
</details>

(c)

mit $\varphi$ als Winkel zwischen den Richtungen von $\vec { r }$ und $\vec { F }$ (wenn die Anfangspunkte der Vektoren aufeinander liegen). Aus Abb. 7.9b entnehmen wir, dass sich Gl. 7.13 auch in der Form

$$
\tau = r F _ {\perp} \tag {7.14}
$$

aufschreiben lässt mit $F _ { \perp } = F$ sin 𝜑 als senkrecht zu $\vec { r }$ stehender Komponente von ${ \vec { F } } .$ Aus Abb. 7.9c folgt als alternative Schreibweise von Gl. 7.13

$$
\tau = r _ {\perp} F \tag {7.15}
$$

mit $r _ { \perp } = r$ sin 𝜑 als Hebelarm von $\vec { F }$ (dem senkrechten Abstand zwischen O und der Richtung der Kraft $\vec { F } )$ .

## KONTROLLFRAGE 3

Der Ortsvektor ⃗r eines Teilchens zeigt in die positive Richtung der z-Achse. In wel cher Richtung wirkt eine Kraft, die ein Drehmoment (a) von null, (b) in negativer x-Richtung und (c) in negativer y-Richtung auf dieses Teilchen erzeugt?

## LÖSUNGSSTRATEGIEN

**Strategie 1: Vektorprodukte und Drehmomente** Gleichung 7.13 ist die erste Anwendung des Vektorprodukts (Kreuzprodukts), die wir kennenlernen. Die entsprechenden Rechenregeln können Sie in Anhang D nachlesen.

Denken Sie daran, dass ein Drehmoment nur sinnvoll ist, wenn es bezüglich eines Punkts (für die Rotation um eine Achse durch diesen Punkt) angegeben wird. Von der Lage dieses Punkts hängt unter Umständen sowohl der Betrag als auch die Richtung des Drehmoments ab. In Beispielaufgabe 7.2 im Übungsbuch haben wir die Drehmomente bezüglich des Ursprungs O berechnet. Sie können sofort zeigen, dass alle drei Drehmomente bezüglich des Punkts A (des Orts des Teilchens) null sind, weil dann stets r = 0 ist.

## 7.5 Der Drehimpuls

## Lernziele

Nach dem Durcharbeiten dieses Abschnitts sollten Sie in der Lage sein, . . .

![](images/page_188_image_15.jpg)

• zu verstehen, dass der Drehimpuls eine Vektorgröße ist,
• zu verstehen, dass zur Berechnung eines Drehimpulses immer der zugehörige Bezugspunkt angegeben werden muss,
• den Drehimpuls eines Teilchens aus dem Vektorprodukt des Ortsvektors des Teilchens und seines Impulsvektors entweder in Einheitsvektoren- oder Betrag-Winkel-Schreibweise zu berechnen,
• die Rechte-Hand-Regel für Vektorprodukteanzuwenden, um die Richtung eines Drehimpulsvektors zu bestimmen.

![](images/page_188_image_21.jpg)

## Schlüsselideen

• Der Drehimpuls $\vec { \ell }$ eines Teilchens mit dem Impuls $\vec { p } ,$ der Masse m und der linearen Geschwindigkeit ⃗v ist eine relativ zu einem Bezugspunkt (üblicherweise dem Ursprung) definierte Vektorgröße:

$$
\vec {\ell} = \vec {r} \times \vec {p} = m (\vec {r} \times \vec {\nu}).
$$

• Der Betrag von $\vec { \ell }$ ist durch

$$
\begin{array}{l} \ell = r m \nu \sin \varphi \\ = r p _ {\perp} = r m v _ {\perp} \\ = r _ {\perp} p = r _ {\perp} m \nu \\ \end{array}
$$

![](images/page_189_image_1.jpg)

<details>
<summary>text_image</summary>

z
ℓ (= r × p)
p (Anfangspunkt
auf den Ursprung
verschoben)
O
φ
r
y
A
p₁
φ
φ
p
x
</details>

(a)

![](images/page_189_image_3.jpg)

<details>
<summary>text_image</summary>

z
ℓ
O
y
r₁
r
φ₁
A
p
x
Verlängerung von p
</details>

(b)

Abb. 7.10

Zur Definition des Drehimpulses: Ein Teilchen, das sich durch den Punkt $\mathbf { A }$ bewegt, besitzt den linearen Impuls $\vec { p } ^ {   } = m \vec { \nu } ,$ wobei der Vektor $\vec { p }$ in der xy-Ebene liegt. Der Drehimpuls des Teilchens bezüglich O ist gegeben durch $\vec { \ell } = \vec { r } \times \vec { p } .$ Wie die Rechte-Hand-Regel ergibt, zeigt der Drehimpulsvektor hier in die positive z-Richtung. Der Betrag von $\vec { \ell }$ ist gegeben (a) durch $\ell = r p _ { \perp } = r m \nu _ { \perp }$ und (b) durch $\ell = r _ { \perp } p = r _ { \perp } m \nu$

gegeben, wobei $\varphi$ der Winkel zwischen $\vec { r }$ und $\vec { p }$ ist und $p _ { \perp }$ und $\nu _ { \perp }$ die Komponenten von $\vec { p }$ bzw. v⃗ senkrecht zu $\vec { r }$ sind. $r _ { \perp }$ ist der senkrechte Abstand zwischen dem Bezugspunkt und der Verlängerung von $\vec { p } .$ .

• Die Richtung von $\vec { \ell }$ ist durch die Rechte-Hand-Regel gegeben: Halten Sie Ihre rechte Hand $\mathbf { S O } ,$ dass die Finger in Richtung von $\vec { r }$ zeigen und drehen Sie die Hand um die Handfläche, bis sie in Richtung von $\vec { p }$ zeigen. Der ausgestreckte Daumen zeigt dann in die Richtung von $\vec { \ell } .$

## 7.5.1 Der Drehimpuls

Wie wir in den vergangenen Kapiteln gesehen haben, sind der lineare Impuls $\vec { p }$ und der zugehörige Impulserhaltungssatz leistungsfähige Hilfsmittel bei der Lö- sung vieler Aufgaben. Mit ihrer Hilfe können wir z. B. das Ergebnis eines Zusammenstoßes zwischen zwei Autos vorhersagen, ohne über Einzelheiten des Ablaufs der Kollision Bescheid zu wissen. In diesem Abschnitt wollen wir das Analogon von $\vec { p }$ für die Rotation einführen. Am Ende dieses Kapitels lernen wir den Erhaltungssatz für diese neue Größe kennen.

Abbildung 7.10 zeigt ein Teilchen mit der Masse m und dem linearen Impuls $\vec { p } = m \vec { \nu } ,$ , das sich durch den Punkt A in der xy-Ebene bewegt. Der **Drehimpuls** $\vec { \ell }$ dieses Teilchens relativ zu O ist definiert als die vektorielle Größe

$$
\vec {\ell} = \vec {r} \times \vec {p} = m (\vec {r} \times \vec {\nu}), \tag {7.16}
$$

mit $\vec { r }$ als Ortsvektor des Teilchens relativ zu O. Bewegt sich das Teilchen bezüglich $\mathrm { O }$ in der Richtung seines Impulses $\vec { p } = m \vec { \nu } ,$ , so rotiert der Ortsvektor $\vec { r }$ um O. Vorsicht: Auch ein Teilchen, das selbst nicht um O rotiert, kann einen Drehimpuls bezüglich O besitzen! Ein Vergleich der Gln. 7.12 und 7.16 zeigt, dass sich der Drehimpuls zum linearen Impuls verhält wie das Drehmoment zur Kraft. Die SI-Einheit des Drehimpulses ist $\mathrm { k g } \cdot \mathrm { m } ^ { 2 } / \mathrm { s }$ (äquivalent zu J ⋅ s).

Um die Richtung des Drehimpulsvektors $\vec { \ell }$ in Abb. 7.10 zu ermitteln, verschieben wir den Vektor $\vec { p } ,$ bis sein Anfangspunkt im Ursprung O liegt. Dann wenden wir die Rechte-Hand-Regel für Vektorproduktean und krümmen die Finger von $\boldsymbol { \cdot } \vec { r }$ nach $\vec { p } .$ Der ausgestreckte Daumen zeigt dann in Richtung von $\vec { \ell } ,$ nämlich in die positive z-Richtung (Abb. 7.10). Diese positive Richtung ist konsistent mit einer Rotation des Ortsvektors $\vec { r }$ des Teilchens gegen den Uhrzeigersinn um die z-Achse, wenn sich das Teilchen weiterbewegt. (Würde $\vec { \ell }$ in negative z-Richtung zeigen, so drehte sich ⃗r im Uhrzeigersinn um die z-Achse.)

Mithilfe der allgemeinen Beziehung $c = a b$ sin $\varphi$ (vgl. Anhang D) berechnen wir nun den Betrag von $\vec { \ell } .$ Dazu schreiben wir

$$
\ell = r m \nu \sin \varphi , \tag {7.17}
$$

mit $\varphi$ als Winkel zwischen $\vec { r }$ und $\vec { p }$ (wenn die Anfangspunkte beider Vektoren aufeinander liegen). Aus Abb. 7.10a entnehmen wir, dass wir Gl. 7.17 auch in der Form

$$
\ell = r p _ {\perp} = r m v _ {\perp} \tag {7.18}
$$

ausdrücken können, mit $p _ { \perp }$ als Komponente von $\vec { p }$ senkrecht zu $\vec { r }$ und $\nu _ { \perp }$ als Komponente von $\vec { \nu }$ senkrecht zu $\vec { r } .$ Aus Abb. 7.10b folgt alternativ

$$
\ell = r _ {\perp} p = r _ {\perp} m \nu \tag {7.19}
$$

mit $r _ { \perp }$ als senkrechtem Abstand zwischen O und der Verlängerung von $\vec { p } .$

Wie das Drehmoment ist auch der Drehimpuls nur bei Angabe eines Bezugs punkts sinnvoll. Läge das Teilchen in Abb. 7.10 nicht in der xy-Ebene oder läge der lineare Impuls $\vec { p }$ des Teilchens nicht ebenfalls in dieser Ebene, so wäre der Drehim puls $\vec { \ell }$ nicht parallel zur $z - \mathrm { A }$ chse. Die Richtung des Drehimpulsvektors steht stets senkrecht auf der Ebene, die vom Ortsvektor $\xrightarrow [ \vec { r } ] { - }$ und vom Vektor des linearen Impulses $\vec { p }$ aufgespannt wird.

## KONTROLLFRAGE 4

In Teil (a) der Skizze sehen Sie zwei Teilchen 1 und 2, die sich in entgegengesetzten Richtungen um einen Punkt O bewegen. Die Radien der beiden Kreisbahnen sind gleich 2 m und 4 m. In Teil (b) bewegen sich zwei Teilchen 3 und 4 geradlinig in gleicher Richtung, wobei ihre Wege 4 m bzw. 2 m senkrecht von O entfernt sind. Teilchen 5 entfernt sich direkt von O. Alle fünf Teilchen haben gleiche Massen und gleiche Geschwindigkeiten. (a) Ordnen Sie die Teilchen nach dem Betrag des Drehimpulses bezüglich O, beginnend mit dem größten Wert. (b) Welche Teilchen haben einen negativen Drehimpuls bezüglich O?

![](images/page_190_image_4.jpg)

<details>
<summary>text_image</summary>

1
O
2
</details>

(a)

![](images/page_190_image_6.jpg)

<details>
<summary>text_image</summary>

3
O
5
4
</details>

(b)

## 7.6 Das zweite Newtonsche Gesetz in Winkelschreibweise

## Lernziele

Nach dem Durcharbeiten dieses Abschnitts sollten Sie in der Lage sein, . . .

• das zweite Newtonsche Gesetz in Winkelschreibweise anzuwenden, um aus dem auf ein Teilchen wirkenden Drehmoment die resultierende Änderungsrate seines Drehimpulses zu berechnen (alle Größen auf denselben Bezugspunkt bezogen).

![](images/page_190_image_12.jpg)

## Schlüsselideen

Nach dem Durcharbeiten dieses Abschnitts sollten Sie in der Lage sein, . . .

• Das zweite Newtonsche Gesetz für ein Teilchen kann in Winkelschreibweise in der Form

$$
\vec {\tau} _ {\mathrm{ges}} = \frac {\mathrm{d}\vec {\ell}}{\mathrm{d} t}
$$

geschrieben werden, wobei $\vec { \tau } _ { \mathrm { g e s } }$ das gesamte (resultierende) Drehmoment auf das Teilchen und $\vec { \ell }$ sein Drehimpuls ist.

![](images/page_190_image_18.jpg)

## 7.6.1 Das zweite Newtonsche Gesetz in Winkelschreibweise

Das zweite Newtonsche Gesetz für ein Teilchen in der Form

$$
\vec {F} _ {\mathrm{ges}} = \frac {\mathrm{d} \vec {p}}{\mathrm{d} t} \tag {7.20}
$$

drückt die fundamentale Beziehung zwischen Kraft und linearem Impuls eines einzelnen Teilchens aus. Wir haben die Parallelen zwischen linearen und Winkelgrö ßen hinreichend diskutiert, um annehmen zu können, dass eine ähnlich enge Beziehung zwischen Drehmoment und Drehimpuls besteht. Ausgehend von Gl. 7.20 vermuten wir, dass diese Beziehung

$$
\vec {\tau} _ {\mathrm{ges}} = \frac {\mathrm{d} \vec {\ell}}{\mathrm{d} t} \tag {7.21}
$$

lautet. Tatsächlich ist Gl. 7.21 das zweite Newtonsche Gesetz für ein einzelnes Teilchen, formuliert mit winkelabhängigen Größen:

![](images/page_191_image_1.jpg)

Die Vektorsumme aller Drehmomente, die auf ein Teilchen wirken, ist gleich der zeitlichen Änderungsrate des Drehimpulses dieses Teilchens.

Achtung: Gl. 7.21 ist nur dann physikalisch sinnvoll, wenn die Drehmomente τ⃗ und der Drehimpuls $\vec { \ell }$ in Bezug auf denselben Punkt angegeben werden!

## Herleitung von Gl. 7.21

Unser Ausgangspunkt ist Gl. 7.16, die Definition des Drehimpulses eines einzelnen Teilchens:

$$
\vec {\ell} = m (\vec {r} \times \vec {\nu}),
$$

mit $1   \vec { r }$ als Ortsvektor und v⃗ als Geschwindigkeit des Teilchens. Wir leiten beide Seiten dieser Gleichung nach $t   \mathrm { a b ^ { 1 ) } }$ und erhalten

$$
\frac {\mathrm{d} \vec {\ell}}{\mathrm{d} t} = m \left(\vec {r} \times \frac {\mathrm{d} \vec {v}}{\mathrm{d} t} + \frac {\mathrm{d} \vec {r}}{\mathrm{d} t} \times \vec {v}\right). \tag {7.22}
$$

In diesem Ausdruck ist $\mathrm { d } \vec { \nu } / \mathrm { d } t$ die Beschleunigung $\vec { a }$ des Teilchens und $\mathrm { d } \vec { r } / \mathrm { d } t$ ist dessen Geschwindigkeit v⃗. Wir können Gl. 7.22 folglich in der Form

$$
\frac {\mathrm{d} \vec {\ell}}{\mathrm{d} t} = m (\vec {r} \times \vec {a} + \vec {\nu} \times \vec {\nu})
$$

schreiben. Das Vektorprodukt eines Vektors mit sich selbst ist null, weil der Winkel zwischen den beiden Faktoren notwendigerweise gleich null ist: $\vec { \nu } \times \vec { \nu } = 0 .$ . Es gilt also

$$
\frac {\mathrm{d} \vec {\ell}}{\mathrm{d} t} = m (\vec {r} \times \vec {a}) = \vec {r} \times m \vec {a}.
$$

Mithilfe des zweiten Newtonschen Gesetzes, $\vec { F } _ { \mathrm { g e s } }   =   m \vec { a } ,$ ersetzen wir nun ma⃗ durch die Vektorsumme der Kräfte, die auf das Teilchen wirken:

$$
\frac {\mathrm{d} \vec {\ell}}{\mathrm{d} t} = \vec {r} \times \vec {F} _ {\mathrm{ges}} = \sum (\vec {r} \times \vec {F}). \tag {7.23}
$$

Das Summenzeichen $\sum$ besagt hier, dass wir die Vektorprodukte ⃗r× $\vec { F } \sum$ aller Kräfte aufsummieren müssen. Aus Gl. 7.12 wissen wir aber, dass jedes derartige Vektorprodukt gleich dem zu einer Kraft gehörigen Drehmoment ist. Gleichung 7.23 sagt deshalb aus:

$$
\vec {\tau} _ {\mathrm{ges}} = \frac {\mathrm{d} \vec {\ell}}{\mathrm{d} t}.
$$

Dies entspricht genau Gl. 7.21.

## KONTROLLFRAGE 5

Die Skizze zeigt den Ortsvektor ⃗r eines Teilchens in einem bestimmten Augenblick. Eingezeichnet sind vier mögliche Richtungen einer Kraft, welche das Teilchen beschleunigt (alle liegen in der xy-Ebene). (a) Ordnen Sie die Varianten nach der bewirkten zeitlichen Änderungsrate des Drehimpulses bezüglich Punkt O, beginnend mit dem größten Wert. (b) In welchem Fall ergibt sich eine negative Änderungsrate bezüglich O?

1) Achten Sie beim Ableiten eines Vektorprodukts darauf, die Reihenfolge der beiden beteiligten Größen (hier ⃗r und ⃗v) nicht zu ändern; siehe dazu auch Anhang D.

![](images/page_191_image_21.jpg)

<details>
<summary>text_image</summary>

F₂
F₃
F₁
F₄
r
O
x
y
</details>