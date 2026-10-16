# 38 Elektromagnetische Wellen

原始 PDF 第 422–433 页。

38

Elektromagnetische Wellen

## 38.1 Ausbreitung elektromagnetischer Wellen entlang von Leitungen

Elektrische Leitungen dienen dem weiträumigen Transport elektromagnetischer Energie und besitzen einen Hin- und einen Rückleiter. Bleiben die Querschnitte dieser beiden Einzelleiter und ihre Anordnung zueinander über ihre ganze Länge unverändert, handelt es sich also um zwei parallele und im Wesentlichen gerade verlaufende Leiter, spricht man von einer homogenen Doppelleitung. Beispiele dafür sind die als Verbindung zwischen Antenne und Fernsehgerät verwendeten Koaxial- oder Paralleldrahtleitungen.

Im Gegensatz zu Schaltkreisen, bei denen die Ausbreitungsgeschwindigkeit von elektrischen Signalen kaum eine Rolle spielt, hängt bei Leitungen infolge ihrer großen räumlichen Ausdehnung der Strom- und Spannungsverlauf nicht nur von der Zeit, sondern auch vom Ort ab. Für ihn gelten, wie unten gezeigt wird, die besonders für die Nachrichtentechnik wichtigen Wellengleichungen

$$
\frac {\partial^ {2} u}{\partial x ^ {2}} = \frac {1}{c ^ {2}} \frac {\partial^ {2} u}{\partial t ^ {2}} \tag {38.1}
$$

**(Telegrafengleichungen der verlustfreien Leitung).**

$$
\frac {\partial^ {2} i}{\partial x ^ {2}} = \frac {1}{c ^ {2}} \frac {\partial^ {2} i}{\partial t ^ {2}} \tag {38.2}
$$

Spannung und Stromstärke breiten sich also als zeitlich periodische Vorgänge wellenförmig mit der Geschwindigkeit $c$ entlang der Leitung aus und weisen damit auch eine räumliche Periodizität auf (vgl. 36.1 und 36.2).

**Herleitung der Wellengleichungen.** Es wird ein Leitungsstück der Länge dx betrachtet (Bild 38.1a). Die mit dem Magnetfeld verknüpften induktiven Eigenschaften werden durch den Induktivitätsbelag $L ^ { \prime } =$ Induktivität/Längeneinheit und die mit dem elektrischen Feld verbundenen kapazitiven Eigenschaften durch den Kapazitätsbelag $C ^ { \prime } = \mathrm { K a p a z i t i t { \acute { a } t } / I }$ ängeneinheit angegeben. Damit hat die Länge dx der Leitung die Induktivität $\mathbf { d } L = L ^ { \prime }$ dx und die Kapazität $\mathbf { d } C = C ^ { \prime }   \mathbf { d } x$

Eine zeitliche Änderung des Stromes erzeugt nach (30.7) in der Längsinduktivität eine Induktionsspannung $- L ^ { \prime }   \mathbf { d } x   ( \partial i / \partial t )$ , d. h.

$$
\mathrm{d} u = \frac {\partial u}{\partial x} \mathrm{d} x = - L ^ {\prime} \mathrm{d} x \frac {\partial i}{\partial t} \quad \text {bzw.} \quad \frac {\partial u}{\partial x} = - L ^ {\prime} \frac {\partial i}{\partial t}. \tag {38.3}
$$

Eine zeitliche Änderung der Spannung ruft von und zur Querkapazität einen Ladungsfluss (Strom) der Größ $\mathbf { \partial } \mathbf { e } - \partial Q / \partial t = - C ^ { \prime }$ dx (∂u/∂t) hervor, d. h.

$$
\mathrm{d} i = \frac {\partial i}{\partial x} \mathrm{d} x = - C ^ {\prime} \mathrm{d} x \frac {\partial u}{\partial t} \quad \text {bzw.} \quad \frac {\partial i}{\partial x} = - C ^ {\prime} \frac {\partial u}{\partial t}. \tag {38.4}
$$

Durch partielle Differenziation der Ausgangsgleichungen (38.3) und (38.4) nach x bzw. t und Elimination der Wellenfunktion i bzw. u findet man die Wellengleichungen (38.1) und (38.2) mit

$$
c = \frac {1}{\sqrt {L ^ {\prime} C ^ {\prime}}} \quad (\text {Phasengeschwindigkeit von Spannungs- und Stromwellen}). \tag {38.5}
$$

---

420

38 Elektromagnetische Wellen

![](../../raw/pages_0417-0448/images/page_422_image_2.jpg)

Bild 38.1 a) Leitungsstück der Länge dx, b) dessen elektromagnetischer Feldverlauf in der Querschnittsebene

Lösungen der Telegrafengleichungen (38.1) und (38.2) sind die in x-Richtung fortschreitenden harmonischen Spannungs- und Stromwellen (36.2)

$$
u = u _ {0} \sin \left[ \omega \left(t - \frac {x}{c}\right) \right] \quad \text {und} \quad i = i _ {0} \sin \left[ \omega \left(t - \frac {x}{c}\right) \right].
$$

Den Zusammenhang zwischen den Wellenfunktionen u und i erhält man durch Einsetzen der Lösungen z. B. in (38.3):

$$
- \frac {\omega u _ {0}}{c} \cos \left[ \omega \left(t - \frac {x}{c}\right) \right] = - \omega L ^ {\prime} i _ {0} \cos \left[ \omega \left(t - \frac {x}{c}\right) \right] \quad \text {bzw.} \quad u _ {0} = c L ^ {\prime} i _ {0} = \sqrt {\frac {L ^ {\prime}}{C ^ {\prime}}} i _ {0}.
$$

Damit sind Spannungs- und Stromverlauf einer fortschreitenden Welle einander proportional:

$$
u = Z i \quad \text {mit} \quad Z = \sqrt {\frac {L ^ {\prime}}{C ^ {\prime}}} \quad (\text {Wellenwiderstand}). \tag {38.6}
$$

Da die Leitungen nicht unendlich lang sind, werden der Wellenausbreitung durch deren Abschluss an den Leitungsenden zusätzliche Randbedingungen auferlegt. So wird eine fortschreitende Welle nur dann am Ende nicht reflektiert, wenn auch dort die Bedingung (38.6) erfüllt ist. Das geschieht durch einen OHMschen Widerstand $R = Z ,$ über den die beiden Leiter der Doppelleitung miteinander verbunden sind. Man spricht dann von einem reflexionsfreien Abschluss, wobei die gesamte von der Welle transportierte Energie im Abschlusswiderstand R in JOULEsche Wärme umgewandelt wird. Bricht dagegen die Leitung ab, so muss dort $i = 0$ sein $( L e e r l a u f ) ;$ werden die Leiter an einer Stelle überbrückt, so gilt dort $u = 0$ (Kurzschluss). Es tritt dann Reflexion der Welle am Leitungsende auf, vergleichbar mit dem festen bzw. losen Ende bei mechanischen Wellen (s. 36.4).

Mit zwei parallel angeordneten Drähten, einer sog. **LECHER-Leitung**, lässt sich gut demonstrieren, dass sich hinlaufende und die am Ende reflektierte Welle zu einer stehenden Welle überlagern, die in $\lambda / 2 \cdot$ Abständen Schwingungsknoten besitzt. Im Leerlauf-Fall muss dann ein Stromknoten, im Kurzschluss-Fall ein Spannungsknoten am Ende liegen. Auf der ganzen Leitung sind Spannung u und Strom i räumlich und zeitlich um $\pi / 2$ phasenverschoben, analog den Größen Schallwechseldruck $\tilde { p }$ und Schallschnelle $\nu$ (vgl. 37.5) bei Schallwellen. Legt man eine Glimmröhre quer über beide Drähte und verschiebt sie längs der LECHER-Leitung, so leuchtet sie an bestimmten Stellen, den Spannungsbäuchen (Stromknoten) hell auf. Überbrückt man dagegen die beiden Drähte mit einer Glühlampe, so leuchtet diese an den dazwischen liegenden Stellen, den Strombäuchen (Spannungsknoten). Ähnlich wie z. B. schwingende Luftsäulen der Längen λ/4 und λ/2 resonanzfähige Systeme darstellen (s. Bild 37.6), werden auch Leitungsstücke der Längen λ/4 und λ/2 anstelle von Schwingkreisen in der Hochfrequenztechnik verwendet.

---

38.2 Ausbreitung elektromagnetischer Wellen im freien Raum

421

Bei hohen Frequenzen verläuft wegen des Skineffektes (s. 32.2) das elektromagnetische Feld zwischen den Leitern und die Phasengeschwindigkeit der Wellenvorgänge ist gleich

$$
c = \frac {1}{\sqrt {\varepsilon \mu}} = \frac {1}{\sqrt {\varepsilon_ {\mathrm{r}} \varepsilon_ {0} \mu_ {\mathrm{r}} \mu_ {0}}},
$$

d. h. von der Geometrie der Leiteranordnung unabhängig. Die Abhängigkeit von den Materialeigenschaften des Zwischenmediums $( \varepsilon _ { \mathrm { r } } ,   \mu _ { \mathrm { r } } )$ zeigt, dass der Strom- und Spannungsverlauf nur eine Begleiterscheinung der eigentlichen elektromagnetischen Welle ist, die außerhalb der Leiter in einem Medium mit Isolatoreigenschaften existiert. In der Tat benötigen elektromagnetische Wellen zur Ausbreitung nicht unbedingt eine Führung durch metallische Leiter, sondern breiten sich auch frei im Raum aus, wie in den folgenden Abschnitten gezeigt wird.

## Beispiel 38.1:

Auf einer Leitung, deren Ausgang kurzgeschlossen ist, werden eingangsseitig mit einem Hochfrequenzgenerator stehende Wellen erzeugt. Bestimme die Laufzeit τ der Leitung, wenn für die Frequenzen $f = 7,143   MHz ;$ 14,286MHz; 21,429MHz; ... Spannungsknoten am Eingang festgestellt werden!

Lösung: Es befinden sich Spannungsknoten am Ausgang und für Leitungslängen $l = \lambda / 2 ;   \lambda ;$ $3 \lambda / 2 ; \ldots = n \lambda / 2$ am Eingang. $\tau = l / c = n \lambda / ( 2 c ) = n / ( 2 f ) = 7 0   \mathrm { { \bf n s } } .$ □

## 38.2 Ausbreitung elektromagnetischer Wellen im freien Raum

MAXWELL (1865) hat mit der Einführung des Verschiebungsstromes die Theorie, welche die elektromagnetischen Erscheinungen auf der Grundlage von Feldern erklärt, zu einem relativen Abschluss geführt (vgl. 32.3). Für den freien Raum, wo Leitungsströme fehlen $( j = 0 )$ , konnte er aus den universell gültigen Feldgleichungen (32.4) und (32.5)

$$
\oint \boldsymbol {H} \cdot \mathrm{d} \boldsymbol {r} = \frac {\mathrm{d}}{\mathrm{d} t} \int \boldsymbol {D} \cdot \mathrm{d} \boldsymbol {A}; \quad \oint \boldsymbol {E} \cdot \mathrm{d} \boldsymbol {r} = - \frac {\mathrm{d}}{\mathrm{d} t} \int \boldsymbol {B} \cdot \mathrm{d} \boldsymbol {A}
$$

(I. und II. MAXWELLsche Gleichung) die Möglichkeit der wellenförmigen Ausbreitung elektromagnetischer Felder nachweisen und die Eigenschaften dieser Wellen theoretisch ableiten. So lässt sich zeigen, dass aus den obigen Feldgleichungen zusammen mit den Materialgleichungen (32.6)

$$
\boldsymbol {D} = \varepsilon \boldsymbol {E}; \quad \boldsymbol {B} = \mu \boldsymbol {H}
$$

für die zeitlichen und räumlichen Änderungen des E- und H-Feldes Wellengleichungen vom gleichen Typ (36.7) folgen, wie wir sie für mechanische Wellen kennen gelernt haben, und zwar bei Ausbreitung in x-Richtung die Wellengleichungen

$$
\frac {\partial^ {2} E _ {y}}{\partial x ^ {2}} = \varepsilon \mu \frac {\partial^ {2} E _ {y}}{\partial t ^ {2}} \quad \begin{array}{l} (\text {fur die y - Komponente der} \\ \text {elektrischen Feldstärke} \boldsymbol {E}), \end{array} \tag {38.7}
$$

$$
\frac {\partial^ {2} H _ {z}}{\partial x ^ {2}} = \varepsilon \mu \frac {\partial^ {2} H _ {z}}{\partial t ^ {2}} \quad \begin{array}{l} (\text {fur die z - Komponente der} \\ \text {magnetischen Feldstärke} \boldsymbol {H}). \end{array} \tag {38.8}
$$

Dies bedeutet aber, dass elektromagnetische Schwingungen nicht am Ort verbleiben, sondern sich mit einer endlichen und konstanten Phasengeschwindigkeit $c = 1 / \sqrt { \varepsilon \mu }$ im Raum fortpflanzen.

---

422

38 Elektromagnetische Wellen

**Herleitung der Wellengleichungen (38.7) und (38.8).** Im Raum sollen zeitlich veränderliche elektrische und magnetische Felder existieren. Betrachtet wird ein Volumenelement im kartesischen Koordinatensystem mit den Kantenlängen dx, dy und dz. Das Koordinatensystem wird so festgelegt, dass das magnetische Feld $H = H _ { z }$ in Richtung der z-Achse orientiert ist (Bild 38.2). So liefern für das geschlossene Wegintegral der magnetischen Feldstärke entlang der Würfelkanten dx und dz nur die Wegstrecken in z-Richtung Beiträge:

$$
\oint \boldsymbol {H} \cdot \mathrm{d} \boldsymbol {r} = \left(H _ {z} + \frac {\partial H _ {z}}{\partial x} \mathrm{d} x\right) \mathrm{d} z - H _ {z} \mathrm{d} z = \frac {\partial H _ {z}}{\partial x} \mathrm{d} x \mathrm{d} z.
$$

Der elektrische Fluss durch die Würfelfläche, die vom magnetischen Wirbel umrandet wird, beträgt

$$
\int \boldsymbol {D} \cdot \mathrm{d} \boldsymbol {A} = - D _ {y} \mathrm{d} x \mathrm{d} z.
$$

Das Minuszeichen steht, weil die Normalenrichtung der Fläche durch die Bewegungsrichtung einer im Umlaufssinn der Fläche betätigten Rechtsschraube festgelegt ist, also D und dA die entgegengesetzte Richtung haben. Nach der I. MAXWELLschen Gleichung (s. o.) folgt aus den beiden letzten Integralen mit $D _ { y } = \varepsilon E _ { y }$

$$
\frac {\partial H _ {z}}{\partial x} = - \varepsilon \frac {\partial E _ {y}}{\partial t}, \tag {38.9}
$$

wobei die totalen Zeitableitungen d/dt, da sie sich hier allein auf die zeitliche Änderung der Feldgrößen beziehen, durch partielle Ableitungen ∂/∂t ersetzt wurden.

Ein zeitlich veränderliches elektrisches Feld $E = E _ { y } ( t )$ erzeugt also ein dazu senkrechtes magnetisches Feld $H = H _ { z } ( x )$ , dessen Feldstärke sich in x-Richtung ändert.

![](../../raw/pages_0417-0448/images/page_424_image_10.jpg)

<details>
<summary>text_image</summary>

Hz
Hz + ∂Hz/∂x dx
φH·dF
Ey
dz
Ey + ∂Ey/∂x dx
φE·dF
dy
z
y
x
</details>

Bild 38.2 Modell zur Herleitung der Wellengleichung. Die y-Komponente von E hat an der Stelle x den Wert $E _ { y }$ , an der Stelle x +dx den Wert $E _ { y } + ( \partial E _ { y } / \partial x )$ dx. Entsprechendes gilt für die z-Komponente von H an den Stellen x und $x   +   \mathrm { d } x$

Da das elektrische Feld seinerseits nicht über die gesamte Fläche konstant ist, ergibt das Wegintegral der elektrischen Feldstärke

$$
\oint \boldsymbol {E} \cdot \mathrm{d} \boldsymbol {r} = \left(E _ {y} + \frac {\partial E _ {y}}{\partial x} \mathrm{d} x\right) \mathrm{d} y - E _ {y} \mathrm{d} y = \frac {\partial E _ {y}}{\partial x} \mathrm{d} x \mathrm{d} y
$$

ebenfalls einen von null verschiedenen Wirbel. Der magnetische Fluss durch die Fläche, die vom elektrischen Wirbel umrandet wird, beträgt

$$
\int \boldsymbol {B} \cdot \mathrm{d} \boldsymbol {A} = B _ {z} \mathrm{d} x \mathrm{d} y.
$$

---

38.2 Ausbreitung elektromagnetischer Wellen im freien Raum

423

Nach der II. MAXWELLschen Gleichung (s. o.) folgt daraus mit $B _ { z } = \mu H _ { z } ;$

$$
\frac {\partial E _ {y}}{\partial x} = - \mu \frac {\partial H _ {z}}{\partial t}. \tag {38.10}
$$

Ein zeitlich veränderliches magnetisches Feld $H = H _ { z } ( t )$ erzeugt also ein dazu senkrechtes elektrisches Feld, das sich in x-Richtung ändert.

Wird nun (38.9) nach t und (38.10) nach x partiell differenziert, so folgt daraus die eindimensionale Wellengleichung (38.7). Wird umgekehrt (38.9) nach x und (38.10) nach t partiell differenziert, so folgt die analoge Wellengleichung (38.8).

Eine elektromagnetische Welle besteht also aus zeitlich und räumlich periodischen Änderungen der elektrischen und magnetischen Feldstärke. Die Wellengleichungen (38.7) und (38.8) und damit auch die MAXWELLschen Gleichungen werden daher durch den bekannten Ansatz (36.2) für eine in x-Richtung fortschreitende Welle erfüllt (s. Bild 38.3):

$$
E _ {y} = E _ {0} \sin \left[ \omega \left(t - \frac {x}{c}\right) \right] \quad (\text {Feldstärkeverlauf der ehenen} \tag {38.11}
$$

$$
H _ {z} = H _ {0} \sin \left[ \omega \left(t - \frac {x}{c}\right) \right] \quad \text {harmonischen elektromagnetischen Welle).} \tag {38.12}
$$

Dabei müssen die Phasengeschwindigkeit $c$ und die Amplituden $E _ { 0 }$ und $H _ { 0 }$ der elektrischen und magnetischen Feldstärke noch bestimmten Bedingungen genügen (s. u.).

![](../../raw/pages_0417-0448/images/page_425_image_10.jpg)

<details>
<summary>text_image</summary>

z
y
c
E
H
S
k
x
</details>

Bild 38.3 In x-Richtung fortschreitende linear polarisierte elektromagnetische Welle

**Eigenschaften elektromagnetischer Wellen.** Wird die Gleichung (38.11) in (38.7) bzw. (38.12) in (38.8) eingesetzt (vgl. 36.2), so folgt

$$
c = \frac {1}{\sqrt {\varepsilon \mu}} \quad (\text {Phasengeschwindigkeit elektromagnetischer Wellen}). \tag {38.13}
$$

Wie bei mechanischen Wellen lässt sich die Ausbreitungsgeschwindigkeit auf Materialeigenschaften des Ausbreitungsmediums $( \varepsilon , \mu )$ zurückführen. Jedoch ist die Ausbreitung elektromagnetischer Wellen nicht an das Vorhandensein eines Stoffes gebunden. Im Vakuum mit $\varepsilon = \varepsilon _ { 0 } = 8 , 8 5 4   1 8 8   \cdot   1 0 ^ { - 1 2 } \mathrm { A }   \cdot   \mathrm { s } / ( \mathrm { V }   \cdot   \mathrm { m } )$ und $\mu = \mu _ { 0 } \approx 4 \pi   \cdot   1 0 ^ { - 7 } \mathrm { V }   \cdot   \mathrm { s } / ( \mathrm { A }   \cdot   \mathrm { m } )$ ist die Phasengeschwindigkeit

$$
c _ {0} = \frac {1}{\sqrt {\varepsilon_ {0} \mu_ {0}}} = 2 9 9 7 9 2 4 5 8 \mathrm{m/s} \quad (\text {Vakuum - Lichtgeschwindigkeit}). \tag {38.14}
$$

## Elektromagnetische Wellen breiten sich im Vakuum mit Lichtgeschwindigkeit aus.

Für alle nichtleitenden Stoffe ist die Dielektrizitätszahl $\varepsilon / \varepsilon _ { 0 } = \varepsilon _ { \mathrm { r } } > 1$ und in guter Näherung $\mu = \mu _ { 0 } ;$ also gilt für die Lichtgeschwindigkeit im Stoff $c < c _ { 0 }$ . Das Verhältnis der Phasengeschwindigkeiten (38.14) und (38.13)

$$
n = \frac {c _ {0}}{c} = \sqrt {\varepsilon_ {\mathrm{r}}} > 1 \quad (\text {MAXWELLSche   Relation}) \tag {38.15}
$$

---

424

38 Elektromagnetische Wellen

definiert die **Brechzahl** als neue Materialeigenschaft. Messungen bestätigen die Beziehung (38.15) für hinreichend große Wellenlängen (s. Bild 39.1).

Der in Ausbreitungsrichtung x zeigende Wellenzahlvektor (36.22) k und die Feldvektoren $E =$ $E _ { y }$ und $H = H _ { z }$ stehen wie die Koordinatenachsen paarweise aufeinander senkrecht (Bild 38.3).

**In elektromagnetischen Wellen schwingen elektrische und magnetische Feldstärke senkrecht zueinander und beide senkrecht zur Ausbreitungsrichtung (Transversalwellen).**

Die durch Schwingungsrichtung der elektrischen Feldstärke (E) und Ausbreitungsrichtung der Welle (k) aufgespannte Ebene heißt **Schwingungsebene**. Eine elektromagnetische Welle mit nur einer Schwingungsebene nennt man linear polarisiert.

Die gegenseitige Kopplung des E- und des H-Feldes beschreiben die Gleichungen (38.9) und (38.10). Setzt man (38.11) und (38.12) in (38.10) ein, so ergibt sich

$$
- \frac {\omega}{c} E _ {0} \cos \left[ \omega \left(t - \frac {x}{c}\right) \right] = - \mu \omega H _ {0} \cos \left[ \omega \left(t - \frac {x}{c}\right) \right]
$$

$$
E _ {0} = c \mu H _ {0} = \sqrt {\frac {\mu}{\varepsilon}} H _ {0} = Z H _ {0}
$$

mit (38.13) $c = 1 / \sqrt { \varepsilon \mu }$ und dem Proportionalitätsfaktor

$$
Z = \sqrt {\frac {\mu}{\varepsilon}} \quad \text {(Wellenwiderstand).}
$$

Für das Vakuum ist $Z _ { 0 } = \sqrt { \mu _ { 0 } / \varepsilon _ { 0 } } = 3 7 6 { , } 7 3   \Omega$ . Da elektrische und magnetische Feldstärke an jedem Ort gleichzeitig ihr Maximum oder ihren Nullwert durchlaufen, gilt im ganzen Raum für die Beträge der Feldstärken

$$
E = Z H \quad \text {bzw.} \quad E = c \mu H = c B. \tag {38.16}
$$

**Im freien Raum (fern von einer Strahlungsquelle) sind elektrische und magnetische Feldstärke einander proportional und schwingen mit gleicher Phase.**

**POYNTING-Vektor.** Die Energie des Wellenfeldes setzt sich aus der elektrischen Feldenergie (Energiedichte (24.13) $w _ { \mathrm { e } } = \varepsilon E ^ { 2 } / 2 )$ und der magnetischen Feldenergie (Energiedichte (30.11) $w _ { \mathrm { m } } = \mu H ^ { 2 } / 2 )$ zusammen. Aus (38.16) folgt mit $Z ^ { 2 } = \mu / \varepsilon$ die Gleichheit der Energiedichten $w _ { \mathrm { e } } = w _ { \mathrm { m } }$ und damit $w = w _ { \mathbf { e } } + w _ { \mathbf { m } } = \varepsilon E ^ { 2 } = \mu H ^ { 2 } = E H / c$ . Diese Energiedichte strömt mit der Geschwindigkeit $c ,$ so dass als Energieflussdichte (37.10) folgt

$$
S = w c = \frac {1}{Z} E ^ {2} = Z H ^ {2} = E H \quad (\text {Strahlungsintensität}). \tag {38.17}
$$

Multipliziert man die Feldstärken E und H vektoriell miteinander, so erhält man den in Ausbreitungsrichtung der elektromagnetischen Welle zeigenden Vektor

$$
\boldsymbol {S} = \boldsymbol {E} \times \boldsymbol {H} \quad (\text {POYNTING - Vektor}).
$$

S gibt die strömende elektromagnetische Feldenergie nach Betrag und Richtung an, die $\mathrm { 1 m ^ { 2 } }$ Fläche in 1s senkrecht durchsetzt.

---

38.3 Erzeugung und Nachweis elektromagnetischer Wellen

425

## Beispiel 38.2:

Guter Rundfunkempfang ist bei der Empfangsintensität $S = 1 0 ^ { - 1 2 } \mathrm { W / m ^ { 2 } }$ möglich. Man berechne die elektrische und magnetische Empfangsfeldstärke.

Lö<u>sung</u>: Aus (38.17) und mit $Z _ { 0 } \approx 3 7 7 \Omega$ für Vakuum folgen $E = \sqrt { S Z _ { 0 } } \approx 2 0   \mu \mathrm { V / m }$ und $H =$ $\sqrt { S / Z _ { 0 } } \approx 5 0   \mathrm { n A / m }$ . Der Abfall der Feldstärke mit der Entfernung von einem Sender bestimmt dessen Reichweite. □

## 38.3 Erzeugung und Nachweis elektromagnetischer Wellen

**Elektrische Dipolstrahlung.** Elektromagnetische Wellen gehen von Erregerzentren aus, die im Vergleich zum Ausbreitungsraum eine geringe Ausdehnung haben. Dabei ist das **Nahfeld**, in dem der Vorgang der Wellenablösung von einem schwingungsfähigen elektrischen System erfolgt, vom **Fernfeld** zu unterscheiden, in dem die abgelösten Wellen unbeeinflusst vom Erregerzentrum sich ausbreiten und weiter existieren.

![](../../raw/pages_0417-0448/images/page_427_image_7.jpg)

Bild 38.4 Übergang vom geschlossenen zum offenen Schwingkreis (E elektrische Feldstärke, H magnetische Feldstärke)

Die bekannte Grundform eines schwingungsfähigen elektrischen Systems ist der aus Induktivität L und Kapazität C bestehende **geschlossene Schwingkreis**, bei dem sich magnetisches und elektrisches Feld, räumlich voneinander getrennt, wechselseitig hervorbringen (Bild 38.4a). Eine nennenswerte Streuung von Feldlinien in den freien Raum findet nicht statt. Um die Eigenfrequenz (34.2) $f _ { 0 } = 1 / ( 2 \pi \sqrt { L C } )$ zu erhöhen, müssen die Werte L und C verkleinert werden. Das kann durch Verringern der Windungszahl an der Spule bis auf eine einzige Windung und durch Verkleinern der Elektroden sowie durch Vergrößern ihres Abstandes am Kondensator geschehen (Bild 38.4b).

Auch ein **Dipol** (gerader Leiter bestimmter Länge, Bild 38.4c) stellt noch einen Schwingkreis dar; denn in und um ihn herum spielen sich prinzipiell die gleichen Vorgänge ab wie in einem geschlossenen Schwingkreis (vgl. 34.1). Erhält das eine Dipolende eine positive und das andere eine negative Aufladung, baut sich dazwischen ein elektrisches Feld auf. In der Folge wird die Aufladung durch Stromfluss im Dipol ausgeglichen, wobei das elektrische Feld zusammenbricht. Dafür existiert bei Ladungsausgleich das an den Stromfluss gebundene Magnetfeld um den Dipol. Der Zusammenbruch dieses Magnetfeldes hält den Stromfluss bis zur umgepolten Aufladung der Enden aufrecht usw. Vom geschlossenen Schwingkreis unterscheidet sich der Dipol durch sein elektrisches und magnetisches Streufeld im Raum. Man spricht daher auch vom **offenen Schwingkreis** oder – im technischen Sprachgebrauch – von einer **Antenne**.

---

426

38 Elektromagnetische Wellen

Ein Feld, das aufgebaut wird, entfernt sich auch gleichzeitig mit der Geschwindigkeit c vom Dipol. In der darauf folgenden Halbperiode, durch umgepolte Aufladung der Dipolenden oder durch Stromfluss in Gegenrichtung gekennzeichnet, können die entstehenden Gegenfelder die schon weiter entfernten Felder der vorhergehenden Halbperiode nicht mehr vollständig rückgängig machen. Damit entsteht ein vom Dipol wegeilendes Wechselfeld im Raum, das im weiteren Verlauf von den Vorgängen am Dipol unabhängig ist, da es von diesen nicht mehr eingeholt wird. Als Momentaufnahmen der elektrischen Feldverteilung zeigt Bild 38.5 einzelne Phasen der Feldablösung vom Dipol. Bild 38.6 stellt das gesamte Strahlungsfeld räumlich dar.

![](../../raw/pages_0417-0448/images/page_428_image_3.jpg)

<details>
<summary>text_image</summary>

Diagram showing five sequential stages of a closed-loop system with positive and negative charges, likely representing magnetic or electrical field distribution.
</details>

Bild 38.5 Ausbreitungsphasen des elektrischen Feldes um einen schwingenden Dipol

![](../../raw/pages_0417-0448/images/page_428_image_5.jpg)

<details>
<summary>text_image</summary>

Diagram illustrating electromagnetic field lines and induced current with labeled electric and magnetic field vectors
</details>

Bild 38.6 Räumliches Strahlungsfeld um einen schwingenden Dipol (E elektrische Feldstärke, H magnetische Feldstärke)

Ein offener Schwingkreis unterscheidet sich also von einem geschlossenen dadurch, dass nicht nur eine Dämpfung seiner Schwingungen infolge dauernder Umwandlung von elektrischer Energie in Wärme im OHMschen Widerstand des Kreises erfolgt, sondern noch eine Dämpfung durch **Abstrahlung** von Energie in den Raum hinzukommt. Ein einfacher Sender besteht daher aus einem Oszillator, der ungedämpfte Schwingungen erzeugt (s. 34.3) und die Antenne über geeignete Koppelglieder zu erzwungenen Schwingungen anregt.

Der Energiefluss Φ durch eine geschlossene Oberfläche, welche die Antenne umschließt, entspricht der **Strahlungsleistung** P **der Antenne** (= abgegebene Energie/Zeit):

$$
\Phi = P = R _ {\mathrm{S}} I ^ {2}. \tag {38.18}
$$

Analog zur Leistung in elektrischen Schaltkreisen ist P dem Quadrat des Antennenstromes proportional; $R _ { \mathbb { S } }$ (mit der Dimension eines Widerstandes) wird Strahlungswiderstand genannt. Für elektrische Schaltkreise wirkt der Strahlungswiderstand einer angeschlossenen Antenne wie ein OHMscher Widerstand, der Energie umsetzt.

Genaue, von H. HERTZ durchgeführte Überlegungen ergaben mit λ als Wellenlänge der Dipolstrahlung und $Z _ { 0 }$ als Wellenwiderstand des Vakuums

$$
R _ {\mathrm{S}} = \frac {2 \pi}{3} Z _ {0} \left(\frac {l}{\lambda}\right) ^ {2} \quad \text {f ü r A n t e n n e n l ä n g e n} l \ll \lambda . \tag {38.19}
$$

Jedes Leiterstück, das von einem Wechselstrom durchflossen wird, stellt im Prinzip eine Antenne dar. Nur sind bei niedrigen Frequenzen (λ groß) im Allgemeinen die abgestrahlten Leistungen gegenüber den OHMschen Verlusten zu vernachlässigen; es gilt $R _ { \mathrm { S } } \ll R .$ Nach (38.18)

---

38.4 Die Entdeckung der elektromagnetischen Wellen

427

und (38.19) kann die Abstrahlung einer bestimmten Leistung bei vorgegebener Stromstärke umso leichter erreicht werden, je kürzer die Wellenlänge ist; denn umso kleiner ist auch die notwendige Antennenlänge. Nähert sich die Antennenlänge dem Wert $l = \lambda / 2$ , gerät der Dipol als offener Schwingkreis in Resonanz, und der Strahlungswiderstand erreicht ein relatives Maximum $R _ { \mathrm { S } } \approx 7 0 \Omega$ . Ein solcher λ/2-Dipol stellt die Standardausführung einer Antenne dar.

**Empfang elektromagnetischer Wellen.** Alle elektrischen Feldlinien enden auf Leiteroberflä- chen senkrecht. Gelangt ein elektrisches Feld an einen passiven Leiter, lässt sich diese Bedingung nur durch Ladungsverschiebungen auf dem Leiter (Influenz), gleichbedeutend mit einem kurzzeitigen Stromfluss, erfüllen. Bei einer elektromagnetischen Welle ändern sich Feldstärke und Feldrichtung laufend mit der Zeit, und es muss daher in einem vom Wellenfeld getroffenen Leiter ein dauernder Wechselstrom gleicher Frequenz fließen, den es nachzuweisen gilt.

Der Nachweis von elektromagnetischen Wellen geschieht durch **Empfänger**, die z. B. mit ak tiven Bauelementen (Transistoren, Operationsverstärker) bestückt sind. Zur Aufnahme der Welle dient wieder eine Antenne (z. B. λ/2-Dipol), die direkt oder über Verstärkerstufen mit Schwingkreisen gekoppelt ist, deren Eigenfrequenz mit der Schwingungsfrequenz der Welle mittelbar oder unmittelbar übereinstimmt bzw. darauf abgestimmt wird. Gerät ein solcher Schwingkreis in Resonanz, wurde die Antenne von einer elektromagnetischen Welle zugeordneter Frequenz erregt.

Zur Übertragung von Tonschwingungen, Telegrafiezeichen oder Bildern wird die Amplitude oder die Frequenz elektromagnetischer Schwingungen vom Sender im Takt der Information verändert. Dieser Vorgang der (Amplituden- oder Frequenz-)**Modulation** wird im Empfänger durch den umgekehrten Vorgang der **Demodulation** rückgängig gemacht, womit die Information selbst wieder zur Verfügung steht. Sie kann dann z. B. mit einem Lautsprecher in Schallwellen umgewandelt oder in einem Rasterbild sichtbar gemacht werden.

## 38.4 Die Entdeckung der elektromagnetischen Wellen (H. Hertz, 1888)

Mit der Ausarbeitung der Theorie der wellenmäßigen Ausbreitung elektrischer und magnetischer Felder durch MAXWELL war die Frage noch nicht eindeutig beantwortet, ob Felder in der Natur real existieren oder nur hilfreiche Modelle darstellen. Zwar war die gegenseitige Beeinflussung von Leiterkreisen über größere Entfernungen bekannt; es war jedoch nicht gesichert, ob zwischen Ursache und Wirkung (wie im folgenden Beispiel) eine Zeitdifferenz lag.

Ein primärer Stromstoß in einem Leiterkreis 1 soll in einem Leiterkreis 2 einen sekundären Stromfluss induzieren. Erfolgt die Ausbreitung der Wirkung mit endlicher Geschwindigkeit, so kann der Stromfluss im Leiter 1 beendet sein, während er gleichzeitig im Leiter 2 noch nicht begonnen hat. Sind in der Zwischenzeit beide Leiter stromlos, muss der Vorgang zwischen den beiden Leitern als Feld weiter existieren.

Bei periodischen elektromagnetischen Vorgängen der Frequenz f ist der Beweis für eine endliche Ausbreitungsgeschwindigkeit c = f λ gleichbedeutend mit dem Nachweis einer endlichen Wellenlänge λ. H. HERTZ gelang der experimentelle Nachweis von elektromagnetischen Wellen endlicher Wellenlänge mit sehr einfachen technischen Hilfsmitteln an stehenden Wellen in eindrucksvoller Weise:

---

428

38 Elektromagnetische Wellen

Als Sender (zur Erzeugung) freier elektromagnetischer Wellen diente ein Dipol (offener Schwing kreis, Bild 38.4c), der mit einem Funkeninduktor immer aufs Neue zu freien gedämpften elektrischen Schwingungen angeregt wurde. Die Eigenfrequenz, von HERTZ berechnet, wird durch die Abmessungen der verwendeten Dipolausführung bestimmt. Zur Erzeugung eines stehenden Wellenfeldes ließ er die vom Sendedipol ausgehenden Wellen an einem Metallschirm reflektieren und in sich zurücklaufen. Da Metalloberflächen die elektrische Feldstärke kurzschließen $( \pmb { E } = 0 )$ , muss sich dort stets ein Schwingungsknoten befinden. Als Empfänger (zum Nachweis) wurde ein auf Resonanz abgestimmter Dipol (Drahtschleife mit Unterbrechung, Bild 38.4b) benutzt; mit ihm wurden die Schwingungsknoten und -bäuche des Wellenfeldes abgetastet. Den Grad der erzwungenen Erregung des Empfängerdipols beurteilte HERTZ nach der Intensität von Funken, die an der winzigen Unterbrechung auftraten und mit einer Lupe beobachtet wurden. Das Ausmessen der Knotenabstände λ/2 erlaubte HERTZ die Bestimmung der Wellenlänge, die je nach Eigenfrequenz $f _ { 0 }$ des Sendedipols bei $\lambda \lessapprox$ 1m lagen. Der Wert $c = f _ { 0 } \lambda$ ergab innerhalb der Fehlergrenzen die Lichtgeschwindigkeit.

Weiter wurden durch die HERTZschen Versuche folgende Eigenschaften elektromagnetischer Wellen nachgewiesen:

a) Reflexion an Metallflächen und ihre Bündelung durch Metall-Hohlspiegel;
b) Brechung an großen Prismen aus dielektrischem Material (Pech). Die Ablenkung der Ausbreitungsrichtung bestätigte die MAXWELLsche Relation (38.15);
c) lineare Polarisation der vom Dipol abgestrahlten Wellen und ihre Transversalität: Ein Gitter aus parallelen Drähten mit einem Drahtabstand ≪ λ ist für elektromagnetische Wellen undurchlässig, wenn ihre Schwingungsrichtung (E-Vektor) parallel zur Drahtrichtung verläuft, und durchlässig, wenn ihre Schwingungsrichtung senkrecht auf der Drahtrichtung steht.

Neben den physikalischen Grunderkenntnissen wurde durch HERTZ eine technische Entwick lung eingeleitet, die im drahtlosen Nachrichtenverkehr, in der Radartechnik, im Fernsehen und im Internet heute ihren derzeitigen Höchststand erreicht hat. Mit seinen Versuchen gelang es ihm zugleich auch, die von MAXWELL aufgestellte elektromagnetische Lichttheorie zu belegen, weil er gleichzeitig nachwies, dass die auf elektrischem Wege erzeugten Wellen alle vom Licht bekannten Eigenschaften haben.

## 38.5 Das elektromagnetische Spektrum

Die elektromagnetischen Wellen umfassen ein ungeheuer großes Erscheinungsgebiet, dessen einheitliche Merkmale nur schrittweise erkannt wurden. Schließlich sind Erzeugung, Erscheinung und Wirkung der elektromagnetischen Wellen je nach ihrer Frequenz f bzw. Wellenlänge λ verschieden. Heute ist der ganze Bereich von 0 bis etwa $1 0 ^ { 2 4 }$ Hz, zum Teil mit Überschneidungen der Erzeugungs- und Untersuchungsmethoden, lückenlos bekannt (s. Bild 38.7).

**Elektrische Wellen.** Den unteren Frequenz- bzw. oberen Wellenlängenbereich des elektromagnetischen Spektrums bis $\lambda \approx 1 0 ^ { - 4 }$ m (s. Bild 38.7a) umfassen die auf elektrotechnischem Wege erzeugten Wellen. Davon werden zur Energieversorgung die Gleichströme (als Grenzfall mit $f = 0$ und $\lambda \to \infty )$ und die technischen Wechselströme (überwiegend mit $f = 5 0   \mathrm { H z } )$ genutzt und in Dynamomaschinen erzeugt. Auch der leitungsgebundene Energietransport in den Verteilernetzen zwischen Erzeuger und Verbraucher wird stets von elektromagnetischen Feldern begleitet.

---

38.5 Das elektromagnetische Spektrum

429

Es ist in der Technik üblich, die zu elektromagnetischen Wechselfeldern gehörenden Wechselströme und -spannungen in einen Niederfrequenz- (NF-) und einen Hochfrequenz- (HF-) Bereich einzuteilen. Zum **NF-Bereich** gehören die elektrischen Vorgänge der Elektroakustik und des Telefonverkehrs, die Informationen der umgesetzten Schallwellen $( f = 1 6   \mathrm { H z }   .$ ..20kHz) übertragen, sowie die meist aperiodischen Vorgänge des Telegrafieverkehrs und der Datenübertragung sowie der Mess-, Steuerungs- und Regelungstechnik.

Für den **HF-Bereich** ist charakteristisch, dass die an Leitungen gebundenen elektromagnetischen Felder auch durch Antennen in den freien Raum abgestrahlt werden können (Funkwellen). Die dazu notwendigen Antennenlängen liegen in der Größenordnung der Wellenlänge λ. Da die technische Realisierung Grenzen setzt, sind auch die Wellenlängen freier elektromagnetischer Wellen nach oben begrenzt. Zum HF-Bereich zählt man die Langwellen (LW, $\lambda = 1 0 ^ { 4 } \ldots 1 0 ^ { 3 }   \mathrm { m } )$ , die Mittelwellen (MW, $\lambda = 1 0 ^ { 3 } \ldots 1 0 ^ { 2 }   \mathrm { m } )$ , die Kurzwellen (KW, $\lambda = 1 0 ^ { 2 } \ldots 1 0   \mathrm { m } )$ und die Ultrakurzwellen (UKW, VHF, $\lambda = 10 \ldots 1  m$ . Diese Einteilung hat, historisch bedingt, natürlich relativen Charakter.

![](../../raw/pages_0417-0448/images/page_431_image_4.jpg)

Bild 38.7 Elektromagnetisches Spektrum mit den elektrischen Wellen (a) und der atomaren elektromagnetischen Strahlung (b)

Der angrenzende Bereich der **Mikrowellen** unterscheidet sich vom HF-Bereich vor allem durch seine speziellen Schwingkreise (Leitungs- und Topfkreise, Hohlraumresonatoren) sowie im Aufbau seiner Oszillator- und Verstärkerschaltungen. Die Ausbreitung von Mikrowellen ist streng geradlinig und zeigt eine gute Bündelfähigkeit. Dadurch können Richtfunkverbindungen statt Leitungsverbindungen hergestellt werden. Nach ihrer Wellenlänge teilt man die Mikrowellen in Dezimeterwellen (UHF, $\lambda = 1 \ldots 0, 1  m$ , Zentimeterwellen (SHF, $\lambda = 0,1\ldots0,01$ m) und Millimeterwellen (EHF, $\lambda = 0,01\ldots0,001\mathrm{m}$ ein. Darüber hinaus ist es gelungen, elektromagnetische Wellen bis zu einer Wellenlänge von $\lambda \approx 1 0 ^ { - 4 }$ m auf elektrischem Wege zu erzeugen. Die untere Grenze ist durch die kleinen Abmessungen der schwingenden Systeme gegeben, die technisch realisierbar sind.

**Atomare elektromagnetische Strahlung.** Elektromagnetische Wellen werden auch von Stoffen, deren atomare Bausteine sich in einem überhöhten Energiezustand befinden, spontan

---

430

38 Elektromagnetische Wellen

mit einer gewissen Wahrscheinlichkeit ausgesandt. Das beim Übergang vom höheren zum tieferen Energiezustand frei werdende Energiequantum wird als elektromagnetische Strahlung emittiert (vgl. 44.2). Aus dem Entstehungsmechanismus folgt ein wesentlicher Unterschied ge genüber den von Antennen abgestrahlten Funkwellen: Während ein Sender beliebig lange in Betrieb sein kann, ist die Dauer eines Emissionsaktes im atomaren Bereich sehr kurz. Bei etwa $1 0 ^ { - 8 }$ s Leuchtdauer lösen sich mit $c \approx 3   \cdot   1 0 ^ { 8 }$ m/s als Lichtgeschwindigkeit Wellenzüge von einigen Metern Länge ab. Die einzelnen Emissionsakte erfolgen unabhängig voneinander, daher sind ihre Phasen und ihre Schwingungsebenen beliebig verteilt.

Erhitzte Körper emittieren hauptsächlich **Infrarot-(IR-)Strahlung**, die der Mensch als Wärmestrahlung empfindet (vgl. 42.1). Mit speziellen Messverfahren und -geräten kann sie ab $\lambda \approx 0 , 4   \mathrm { m m }$ experimentell nachgewiesen werden und reicht damit bereits in das Gebiet der elektrischen Wellen (vgl. Bild 38.7). Nach der kurzwelligen Seite schließt sich der schmale Bereich des **sichtbaren Lichts** von $\lambda \approx 780 \ldots 380    nm$ mit der Farbfolge rot, orange, gelb, grün, blau, violett an. NEWTON erkannte, dass weißes Sonnenlicht eine Mischung dieser Farbkomponenten ist. Farben sind jedoch keine physikalische Eigenschaft der Strahlung. Vielmehr ge stattet der Gesichtssinn als Orientierungshilfe in der Umwelt eine Strahlungsbewertung nach der Wellenlänge. Es folgt die **Ultraviolett-(UV-)Strahlung**, die überwiegend bei Beschuss von Atomen mit schnellen Ionen und Elektronen in Gas-, Funken- und Bogenentladungen entsteht (s. 27.3).

Dringen Elektronen hoher Energie in einen Stoff ein, wird **RÖNTGENstrahlung** emittiert (vgl. 44.11). Mit einer RÖNTGENröhre erreicht man Wellenlängen von $\lambda \approx 1 0 ^ { - 1 1 }$ m. Durch Beschleunigung der Elektronen auf kreisförmigen Bahnen in dem als Betatron bezeichneten Elektronenbeschleuniger erhält man besonders „harte“ RÖNTGENstrahlen bis $\lambda \approx 5 \cdot 1 0 ^ { - 1 4 }   \mathrm { m }$

Die vom Atomkern emittierte elektromagnetische Strahlung wird als **Gammastrahlung** bezeichnet (vgl. 48.2). Elektromagnetische Strahlung mit Wellenlängen $\lambda < 1 0 ^ { - 1 5 }$ m wurde bisher nur als eine Komponente der kosmischen Strahlung nachgewiesen. Sie entsteht als Folge von Reaktionen der Atomkerne und der Elementarteilchen im Weltall.

Je kürzer die Wellenlänge der elektromagnetischen Strahlung wird, umso mehr nähern sich die physikalischen Eigenschaften diskontinuierlich emittierter Wellenzüge denen von Teilchen an. Die Größen Amplitude und Wellenlänge verlieren immer mehr an Bedeutung zu Gunsten des vom Wellenzug transportierten Energie- und Impulsquantums (vgl. 43.1).

## Aufgaben

**38.1** a) Wie groß sind die Wellenlängen, die UKW-Radiosender bei $f _ { 1 } = 1 0 0 { , } 6 \mathrm { M H z }$ und Mittelwellensender bei $f _ { 2 } = 6 0 0   \mathrm { k H z }$ mit ihren Programmen ausstrahlen? b) Bei welcher Frequenz arbeiten „Radarfallen“, deren Wellenlänge $\lambda = 3 { , } 2$ cm beträgt?
**38.2** Moderne Smartphones der 3. und 4. Generation (3G bzw. 4G) unterstützen die Mobilfunkstandards LTE (Long Term Evolution) 0,8GHz, 1,8GHz und 2,6GHz. Wie groß sind die Wellenlängen der von einer Mobilfunkbasisstation ausgesandten und von einem Smartphone empfangenen elektromagnetischen Strahlung dieser Bänder?
