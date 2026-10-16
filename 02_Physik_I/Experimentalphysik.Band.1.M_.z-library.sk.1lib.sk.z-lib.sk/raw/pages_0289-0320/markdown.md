mit

$$
\left| c \right| = \sqrt {c \cdot c ^ {\star}} = \frac {1}{2} \sqrt {C _ {1} ^ {2} + C _ {2} ^ {2}} = \sqrt {a ^ {2} + b ^ {2}} \tag {I-5.31}
$$

und

$$
\tan \varphi = \frac {\operatorname{Im} c}{\operatorname{Re} c} = \frac {b}{a}, ^ 6 \tag {I-5.32}
$$

wobei $c = a + i b$

Zu einer weiteren Schreibweise gelangt man, indem man in Gl. (I-5.4) $C _ { 1 }   =$ A cos $\varphi$ und $C _ { 2 } = - A$ sin $\varphi$ setzt und cos $( \alpha + \beta ) =$ cos α sin $. \beta -$ sin $\alpha$ sin $\beta$ verwendet:

$$
x (t) = A \cdot \cos (\omega_ {0} t + \varphi) \tag {I-5.33}
$$

mit

$$
A = \sqrt {C _ {1} ^ {2} + C _ {2} ^ {2}} = 2 \left| c \right|, \quad \tan \varphi = - \frac {C _ {2}}{C _ {1}} = \frac {b}{a}. \tag {I-5.34}
$$

Die Bewegung des harmonischen Oszillators (= Schwingung eines MP unter der Wirkung einer harmonischen Kraft) lässt sich also in vier völlig äquivalenten Weisen angeben:

1

<table><tr><td>1. Gl. (I-5.12)</td><td> $x(t) = C_1 \cos(\omega_0 t) + C_2 \sin(\omega_0 t)$ </td><td rowspan="3">Die vier äquivalentenDarstellungender Bewegungdes ungedämpften</td></tr><tr><td>2. Gl. (I-5.33)</td><td> $x(t) = A \cos(\omega_0 t + \varphi)$ </td></tr><tr><td>3. Gl. (I-5.22)</td><td> $x(t) = ce^{i\omega_0 t} + c^* e^{-i\omega_0 t}$ </td></tr><tr><td>4. Gl. (I-5.30)</td><td> $x(t) = |c| \left[ e^{i(\omega_0 t + \varphi)} + e^{-i(\omega_0 t + \varphi)} \right]$ </td><td>harmonischenOszillators</td></tr></table>

Mit Hilfe der Eulerschen Formeln erkennt man, dass auch die beiden letzten Gleichungen reelle Werte für $x ( t )$ liefern. In jedem Fall treten 2 Integrationskonstanten auf, durch die die Amplitude und die Phasenlage der Schwingung bestimmt sind: $C _ { 1 }$ und $C _ { 2 } , A$ und $\varphi , c$ bzw. $c ^ { * } ,   \left| c \right|$ und $\varphi . ^ { 7 }$

$$
\cos \varphi + i \sin \varphi \Rightarrow \cos \varphi = \frac {C _ {1}}{\sqrt {C _ {1} ^ {2} + C _ {2} ^ {2}}}, \quad \sin \varphi = \frac {- C _ {2}}{\sqrt {C _ {1} ^ {2} + C _ {2} ^ {2}}} \Rightarrow \tan \varphi = - \frac {C _ {2}}{C _ {1}} = \frac {b}{a}.
$$

7 In der komplexen Amplitude c bzw. c\* sind bereits 2 Konstanten, nämlich |c| und φ enthalten; c und c\* sind nicht unabhängig voneinander!

**Anmerkung:** Aus der Darstellung 4 ersieht man, dass der Realteil beider Summanden mit der Darstellung 2 übereinstimmt (man benützt die Eulerschen Formeln). Es wird daher oft anstelle von Darstellung 2 die Darstellung $A \cdot e ^ { i ( \omega _ { o }   t   +   \varphi ) }$ bzw. $A \cdot e ^ { - i ( \omega _ { 0 } t + \varphi ) }$ mit der stillschweigenden Übereinkunft benützt, dass im Endergebnis nur der Realteil zu verwenden ist!

## Veranschaulichung des Schwingungsvorganges im Zeigerdiagramm

Man kann komplexe Zahlen $z = c = \left| c \right| \cdot e ^ { i \varphi }$ in der Gaußschen (= komplexen) Zahlenebene darstellen, die von der imaginären Achse (Ordinate) und der reellen Achse (Abszisse) aufgespannt wird (Abb. I-5.2):

![](images/page_289_image_5.jpg)

<details>
<summary>text_image</summary>

Im
|c|
z = c = |c|e^{i\varphi} = a + ib (Zeiger der komplexen Zahl)
b
φ
a
Re
a = Re(c) = |c| cos φ,
b = Im(c) = |c| sin φ
</details>

Abb. I-5.2: Darstellung einer komplexen Zahl $z = c$ als „Zeiger“ (blau) in der Gaußschen Zahlenebene.

Für die Koeffizienten der komplexen Zahl $c = \left| c \right| e^{i \varphi} = a + i b$ gilt:

$$
a = \operatorname{Re} (c) = | c | \cos \varphi , \quad b = \operatorname{Im} (c) = | c | \sin \varphi . \tag {I-5.35}
$$

Für unsere komplexen Lösungen der Schwingungsgleichung (Versionen 3 und 4) lassen wir den Punkt $c = a + i b$ mit der Winkelgeschwindigkeit $\omega = 2 \pi \nu = 2 \pi / T$ als „Zeiger“ in der Gaußschen Zahlenebene rotieren, wobei der positive Drehsinn gegen den Uhrzeiger läuft (Abb. I-5.3).

Zu einem beliebigen Zeitpunkt gilt für die Projektion auf die reelle Achse

$$
a = \operatorname{Re} (c) = | c | \cos (\omega t + \varphi), \tag {I-5.36}
$$

für die Projektion auf die imaginäre Achse

$$
b = \mathrm{Im} (c) = | c | \sin (\omega t + \varphi). \tag {I-5.37}
$$

Zusätzlich rotiert die zu c konjugiert komplexe Größe $c ^ { \star }$ mit umgekehrtem Umlaufsinn. Beide rotieren mit der Frequenz $\nu = \omega / 2 \pi = 1 / T .$

![](images/page_290_image_2.jpg)

<details>
<summary>text_image</summary>

Im
positiver Drehsinn
= Antiuhrzeigersinn
t = 0
c = a + ib
φ
ωt + φ
Re
c* = a - ib
</details>

Abb. I-5.3: Darstellung der Zeitabhängigkeit in der Gaußschen Zahlenebene. Der $, \mathrm { Z e i g e r } ^ { \omega } c = a + i b$ (blau) rotiert bei positivem Drehsinn gegen den Uhrzeiger $( c ^ { \star } = a - i b$ rotiert dann im Uhrzeigersinn).

$\varphi$ ist der Phasenwinkel, den der im positiven Sinn (Gegenuhrzeigersinn) rotierende Zeiger c zum Zeitpunkt $t = 0$ mit der positiven reellen Achse einschließt.

Wir entnehmen also der komplexen Darstellung

$$
c = \left| c \right| e ^ {i (\omega t + \varphi)} = \left| c \right| \underbrace {e ^ {i \omega t}} _ {\text {Zeitfaktor Phasen - faktor}} \underbrace {e ^ {i \varphi}} \tag {I-5.38}
$$

$| c |$ , als Betrag des Zeigers,

$( \omega   t + \varphi )$ , die Phase und

$\varphi ,$ den Phasenwinkel als Phase zum Zeitpunkt $t = 0$

Die Summe der rotierenden Zeiger $\big | c \big | \big [ e ^ { i ( \omega t + \varphi ) } + e ^ { - i ( \omega t + \varphi ) } \big ]$ oder $c \cdot e ^ { i \omega t } + c ^ { \star } \cdot e ^ { - i \omega t }$ gibt die gesamte reelle Lösung der Schwingungsgleichung, da sich die Imaginärteile wegheben.

Die Vorteile der komplexen Schreibweise sind:

1. die einfache Differentiation von $e ^ { i \omega t }$ durch Multiplikation der Zeigerlänge mit $\omega$ und Drehung um $+ 9 0 ^ { \circ }$ (Multiplikation mit $+ i ,$ denn $i = e ^ { i \frac { \pi } { 2 } }$ , Abb. I-5.4 und Abb. I-5.5) und
2. die bequeme Zeigeraddition ohne Benutzung der umständlichen Additionstheoreme (siehe dazu Abb. I-5.8).

![](images/page_291_image_2.jpg)

<details>
<summary>text_image</summary>

i·c = -b + ia
Im
+90°
c = a + ib
Re
-90°
-i·c = b - i·a
</details>

Abb. I-5.4: Multiplikation einer komplexen Zahl mit der imaginären Einheit $j \left( \mathsf{b} z \mathsf{w}, - \mathsf{j} \right)$ : Drehung um $+ 90^{\circ} \left( - 90^{\circ} \right)$ in der Zahlenebene.

![](images/page_291_chart_4.jpg)

<details>
<summary>other</summary>

| Parameter | Definition |
| --- | --- |
| Geschwindigkeit: u(t) | \(i \cdot \omega_{0} \cdot c \cdot e^{i\omega_{0}t} = \omega_{0} \cdot c \cdot e^{i(\omega_{0}t + \pi/2)}\) |
| Beschleunigung: \(i \cdot i \cdot \omega_{0}^{2} \cdot c \cdot e^{i\omega_{0}t} = \omega_{0}^{2} \cdot c \cdot e^{i(\omega_{0}t + \pi)}\) | Der Liefer bei Re=0 |
| Weg: x(t) | \(c \cdot e^{i\omega_{0}t}\) |
</details>

Abb. I-5.5: Vorteil der komplexen Darstellung. Die Differentiation nach der Zeit wird in der Gaußschen Zahlenebene sehr einfach: Multiplikation der Zeigerlänge mit $\omega _ { 0 }$ und Drehung um $+ 9 0 ^ { \circ }$ Hier als Beispiel: Weg, Geschwindigkeit, Beschleunigung.

Aus dem Zeigerdiagramm ist sofort ersichtlich, dass die Geschwindigkeit $\nu ( t )$ dem Ausschlag $x ( t )$ um $\pi / 2 ,$ die Beschleunigung um π vorauseilt.

## Das Weg-Zeit-Diagramm

Die zeitliche Bewegung des harmonischen Oszillators kann zeitaufgelöst dargestellt werden (Abb. I-5.6).

Dabei ist die Schwingungsdauer $T = \frac { 2 \pi } { \omega _ { 0 } }$ die Zeit zwischen zwei gleichen Schwingungszuständen. Die maximale Auslenkung A heißt Amplitude.

![](images/page_292_image_2.jpg)

<details>
<summary>text_image</summary>

T = 2 π/ω₀
x = A cos (ω₀t + φ)
A
A
t = -φ/ω₀ = -t₀
-A
</details>

Abb. I-5.6: Zeitaufgelöste Darstellung der Bewegung des ungedämpften harmonischen Oszillators.

$$
A = x _ {\max} \quad \Rightarrow \quad \cos (\omega_ {0} t + \varphi) = 1 \quad \Rightarrow \quad t = \frac {- \varphi}{\omega_ {0}} \text { für } x = A.
$$

Für die Bewegung des schwingenden Systems (z. B. des MP) hat sich ergeben (Darstellungsversion 2, Gl. I-5.33)

$$
x (t) = A \cos \left(\omega_ {0} t + \varphi\right) = A \cos \left[ \omega_ {0} (t + \underbrace {\varphi / \omega_ {0}} _ {t _ {0}}) \right].
$$

Das Argument des Kosinus, also $( \omega _ { 0 }   t + \varphi )$ , nennt man die Phase (phase) der Schwingung. Sie gibt den augenblicklichen Schwingungszustand an. φ ist der Phasenwinkel (= Phasenkonstante, phase angle or phase constant), er gibt den Anfangszustand der Schwingung bei $t = 0$ an. Ist der Phasenwinkel $\varphi \neq 0$ , so wird die maximale Auslenkung nicht für t = 0 bzw. $n \cdot T$ erreicht, sondern bei

$$
t = - \frac {\varphi}{\omega_ {0}} + n T \underbrace {=} _ {T = \frac {2 \pi}{\omega_ {0}}} - \frac {\varphi}{\omega_ {0}} + \frac {2 n \pi}{\omega_ {0}} = \frac {1}{\omega_ {0}} (2 n \pi - \varphi). \tag {I-5.39}
$$

In der obigen Abb. I-5.6 läuft die Schwingung schon zur Zeit $t = - \varphi / \omega _ { 0 } = - t _ { 0 }$ durch das Maximum, bei $t = 0$ ist es bereits überschritten, die Auslenkung ist wieder kleiner als die Amplitude.

## Harmonische Schwingung bei beliebiger Auslenkung im Raum

Die bisher betrachtete harmonische Schwingung war eindimensional, da die Anfangsgeschwindigkeit $\vec { v } _ { 0 }$ (falls vorhanden) in der Richtung der Auslenkung $\vec { r } _ { 0 }$ erfolgte. Gilt für kleine Auslenkungen in einer beliebigen Richtung r⇀wieder eine rücktreibende Kraft proportional zur Auslenkung, hier also proportional zum Ortsvektor $\vec { r } ~ ( \vec { F } = - k \vec { r }$ , der Ursprung des Koordinatensystems liege im Ruhepunkt des MP), so weist die rücktreibende Kraft ständig zum Ursprung des Koordinatensystems, ist also eine Zentralkraft und die resultierende Bewegung eine Zentralbewegung mit konstantem Drehimpuls $\big ( \vec { L } = 0$ , wenn die Anfangsgeschwindigkeit zum Zentrum oder vom Zentrum weg weist):

$$
\ddot {\vec {r}} (t) + \frac {k}{m} \vec {r} (t) = 0. \tag {I-5.40}
$$

Mit dem Ansatz $\vec { r } ( t ) = \vec { c } e ^ { \lambda t }$ und $\omega _ { 0 } ^ { 2 } = \frac { k } { m }$ ergibt sich damit die Bewegung des $M P$ zu

$$
\vec {r} (t) = \vec {c} e ^ {i \omega_ {0} t} + \vec {c} ^ {\star} e ^ {- i \omega_ {0} t} \quad \text {oder} \quad \vec {r} (t) = \vec {C} _ {1} \cos (\omega_ {0} t) + \vec {C} _ {2} \sin (\omega_ {0} t). \tag {I-5.41}
$$

Die Konstanten sind jetzt Vektoren, die wieder aus den Anfangsbedingungen folgen:

$$
\vec {r} (0) = \vec {r} _ {0}, \quad \dot {\vec {r}} (0) = \vec {v} _ {0} \quad \Rightarrow \quad \vec {C} _ {1} = \vec {r} _ {0}, \quad \vec {C} _ {2} = \frac {1}{\omega_ {0}} \vec {v} _ {0}
$$

und man erhält als allgemeine Lösung

(I-5.42)

$$
\vec {r} (t) = \vec {r} _ {0} \cos (\omega_ {0} t) + \frac {\vec {v} _ {0}}{\omega_ {0}} \sin (\omega_ {0} t) = \underbrace {\frac {\vec {r} _ {0}}{\left| \vec {r} _ {0} \right|}} _ {\vec {e} _ {\vec {r} _ {0}}} \cdot \left| \vec {r} _ {0} \right| \cos (\omega_ {0} t) + \underbrace {\frac {\vec {v} _ {0}}{\left| \vec {v} _ {0} \right|}} _ {\vec {e} _ {\vec {v} _ {0}}} \frac {\left| \vec {v} _ {0} \right|}{\omega_ {0}} \sin (\omega_ {0} t).
$$

Der Vektor $\vec { r } ( t )$ setzt sich offensichtlich aus zwei Vektoren zusammen, die in Richtung der (ausgelenkten) Anfangslage und der Anfangsgeschwindigkeit weisen und deren Beträge periodische Funktionen der Zeit mit der gleichen Frequenz sind.

Wir wählen als Ursprung des Koordinatensystems die Ruhelage des $M P$ und führen zwei schiefwinkelige Koordinatenachsen $\xi$ und $\eta$ mit den Einheitsvektoren $\vec { e } _ { \vec { r } _ { 0 } }$ und $\vec { e } _ { \vec { v } _ { 0 } }$ in Richtung der Anfangslage und der Anfangsgeschwindigkeit ein (Abb. I-5.7).

In diesem Koordinatensystem hat der MP folgende Koordinaten

$$
\xi = r _ {0} \cos (\omega_ {0} t), \eta = (\nu_ {0} / \omega_ {0}) \sin (\omega_ {0} t), \tag {I-5.43}
$$

da die $\xi -$ Achse in die Richtung der Auslenkung (Anfangslage) zeigt und die $\eta \mathbf { - A }$ chse in die Richtung der Anfangsgeschwindigkeit. Daraus folgt

$$
\xi / r _ {0} = \cos \left(\omega_ {0} t\right) \quad \text {und} \quad \eta \omega_ {0} / \nu_ {0} = \sin \left(\omega_ {0} t\right).
$$

Beide Gleichungen quadriert und addiert ergeben als Bahnkurve

$$
\frac {\xi^ {2} (t)}{r _ {0} ^ {2}} + \frac {\eta^ {2} (t)}{\nu_ {0} ^ {2} (1 / \omega_ {0} ^ {2})} = 1, \tag {I-5.44}
$$

in der die Zeit nicht mehr explizit, sondern nur als Parameter aufscheint.

![](images/page_294_image_2.jpg)

<details>
<summary>text_image</summary>

z
η
e⃗_v₀
y
x
ξ
e⃗_F₀
</details>

Abb. I-5.7: Bahnkurve des MP bei beliebiger Auslenkung im Raum.

Wir sehen damit, dass der MP eine Ellipse beschreibt, wobei $\vec { r } _ { 0 }$ und $\vec { v } _ { 0 }$ in die Richtung konjugierter Durchmesser zeigen. Es handelt sich also um eine ebene Bewegung im Raum, wie es von einer Zentralbewegung verlangt wird (siehe Kapitel „Mechanik des Massenpunktes, Anhang A1.2 ‚Das Keplerproblem‘).<sup>8</sup>

## 5.1.2 Überlagerung von harmonischen Schwingungen (superposition of harmonic oscillations)

Die Schwingungsgleichung des harmonischen Oszillators ist eine lineare DG (sie folgt ja unmittelbar aus dem linearen 2. Newtonschen Axiom (Newton 2) mit einem linearen Kraftansatz).

1 Für lineare Differentialgleichungen gilt das Superpositionsprinzip: Die Summe von Lösungen ist wieder eine Lösung der Differentialgleichung. Sind also $f ( x )$ und $g ( x )$ Lösungen (mögliche Zustände des Systems), dann gilt dies auch für $c _ { 1 }   f ( x ) + c _ { 2 }   g ( x )$ mit $c _ { 1 }$ und $c _ { 2 }$ als Konstanten.

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">8 Auch bei der Planetenbewegung weist die wirkende Kraft ständig auf ein Zentrum (die Sonne) hin, sie ist allerdings im Gegensatz zum Oszillator proportional zu 1/r<sup>2</sup>. Dennoch resultiert wieder eine elliptische Bahn! Jetzt liegt aber das Kraftzentrum in einem Ellipsenbrennpunkt, während es beim harmonischen Oszillator im Ellipsenmittelpunkt liegt. Die Geschwindigkeiten in den Scheitelpunkten (‚Perihel‘ und ‚Aphel‘) sind bei der Planetenbewegung unterschiedlich, beim Oszillator gleich. Zur Planetenbewegung siehe Kapitel „Mechanik des Massenpunktes“, Anhang A1.2.</span></small>

Wir können also entweder Lösungen mit Hilfe der Additionstheoreme der Winkelfunktionen finden oder vorhandene Lösungen in der komplexen Zahlenebene addieren.

## Eindimensionale Schwingungen

Wir nehmen an, dass alle Auslenkungen in dieselbe Richtung erfolgen.

Für die einzelne Schwingung gilt

$$
x _ {1} (t) = A _ {1} \cos \left(\omega_ {1} t + \varphi_ {1}\right). \tag {I-5.45}
$$

Für eine Summe von n Schwingungen ergibt sich daher

$$
x (t) = \sum_ {n} x _ {n} (t) = \sum_ {n} A _ {n} \cos \left(\omega_ {n} t + \varphi_ {n}\right). \tag {I-5.46}
$$

Die Summenschwingung ist also abhängig von den Amplituden $A _ { n }$ , den Frequenzen $\omega _ { n }$ und den Phasenwinkeln $\varphi _ { n }$

## a) Zwei Schwingungen gleicher Frequenz

$$
x _ {1} (t) = A _ {1} \cos (\omega t + \varphi_ {1}), x _ {2} (t) = A _ {2} \cos (\omega t + \varphi_ {2}) \tag {I-5.47}
$$

Für die Summenschwingung gilt

$$
x (t) = x _ {1} (t) + x _ {2} (t) = A \cos (\omega t + \varphi), \tag {I-5.48}
$$

wie eine umständliche Umrechnung unter Benützung der Additionstheoreme zeigt.

Es ergibt sich also eine Schwingung gleicher Frequenz, aber anderer Amplitude und Phase als jener der Teilschwingungen (ausgenommen, wenn $\varphi _ { 1 }   = \varphi _ { 2 } )$ . Sehr einfach gestaltet sich diese Addition als Zeigeraddition im Zeigerdiagramm; sie liefert Betrag und Richtung, also auch den Phasenwinkel $\varphi$ (Abb. I-5.8).

Für die Amplitude und die Phase der zusammengesetzten Schwingung (Abb. I-5.9) gilt

$$
(\text {aus dem Kosinussatz}) \quad A = \sqrt {A _ {1} ^ {2} + A _ {2} ^ {2} + 2 A _ {1} A _ {2} \cos \left(\varphi_ {2} - \varphi_ {1}\right)}, \tag {I-5.49}
$$

$$
\tan \varphi = \frac {A _ {1} \sin \varphi_ {1} + A _ {2} \sin \varphi_ {2}}{A _ {1} \cos \varphi_ {1} + A _ {2} \cos \varphi_ {2}}, \tag {I-5.50}
$$

also Quotient der Summen der Projektionen von $A _ { 1 }$ und $A _ { 2 }$ auf die $X ^ { - }$ bzw. y-Achse.

![](images/page_296_image_2.jpg)

<details>
<summary>text_image</summary>

Im
x = x₁ + x₂
A₂ x₂ A x₁
A₁
φ₂ φ φ₁
Re
</details>

Abb. I-5.8: Im Zeigerdiagramm gestaltet sich die Addition von Schwingungen sehr einfach: Die Summe ergibt sich wie bei der ‚normalen‘ Vektoraddition und liefert Betrag und Richtung, also auch den Phasenwinkel.

![](images/page_296_chart_4.jpg)

<details>
<summary>line</summary>

| Component | Description |
| --- | --- |
| Solid Line | \(x = A_1 + x_2 = A cos(\omega t + \varphi)\) |
| Dashed Line | \(x_1 = A_1 cos(\omega t + \varphi_1)\) |
| Dashed Line | \(x_2 = A_2 cos(\omega t + \varphi_2)\) |
</details>

Abb. I-5.9: Überlagerung zweier Schwingungen gleicher Richtung und gleicher Frequenz, aber unterschiedlicher Amplitude und Phase. Die Summenschwingung (durchgezogen blau) hat wieder die gleiche Frequenz, aber andere Amplitude und Phase als die Teilschwingungen.

## b) Schwingungen unterschiedlicher Frequenz

Bildet man die Summe zweier Schwingungen unterschiedlicher Frequenz, aber gleicher Amplitude und gleicher Phase

$$
x _ {1} (t) = A \cos (\omega_ {1} t), x _ {2} (t) = A \cos (\omega_ {2} t), \tag {I-5.51}
$$

so erhält man unter Verwendung des Additionstheorems

$$
\cos \alpha + \cos \beta = 2 \cos \frac {\alpha - \beta}{2} \cos \frac {\alpha + \beta}{2}
$$

(Abb. I-5.10):

$$
x = x _ {1} + x _ {2} = 2 A \cos \left(\frac {\omega_ {1} - \omega_ {2}}{2} t\right) \cos \left(\frac {\omega_ {1} + \omega_ {2}}{2} t\right). \tag {I-5.52}
$$

![](images/page_297_chart_2.jpg)

<details>
<summary>line</summary>

| Component | Formula |
| --- | --- |
| Top plot | \(x1 = A cos(\omega t)\) |
| Middle plot | \(x2 = A cos(2 \omega t)\) |
| Bottom plot | \(x1 + x2 = 2 A cos[(1/2)\omega t] cos[(3/2)\omega t]\) |
</details>

Abb. I-5.10: Überlagerung zweier Schwingungen $x _ { 1 } = A \cos \left( \omega t \right)$ und $x _ { 2 } = A$ cos (2 ωt) in gleicher Richtung. Das Ergebnis zeigt, dass in der Summenschwingung die Schwingung 2 A cos [(3/2) ωt] mit cos [(1/2) ωt] moduliert ist.

Wenn ein sehr kleiner Frequenzunterschied vorliegt, die Frequenzdifferenz $\Delta \omega$ also sehr viel kleiner als die Mittelfrequenz ω̅ ist, wenn also gilt

$$
\Delta \omega = \omega_ {1} - \omega_ {2} \ll \frac {1}{2} \left(\omega_ {1} + \omega_ {2}\right) = \bar {\omega}, \tag {I-5.53}
$$

dann kann die Schwingung als Schwingung mit der Mittelfrequenz $\bar { \omega }$ aufgefasst werden, deren Amplitude $A(t) = 2A\cos\frac{\Delta\omega}{2}$ t eine langsam veränderliche Funktion der Zeit ist. Eine derartige Schwingung mit sich langsam periodisch verändernder Amplitude nennt man Schwebung (beats, Abb. I-5.11). Es gilt

$$
x _ {S} = 2 A \cos \frac {\Delta \omega}{2} t \cdot \cos \bar {\omega} t \quad \text {mit} \quad \Delta \omega = \omega_ {1} - \omega_ {2}, \bar {\omega} = \frac {1}{2} \left(\omega_ {1} + \omega_ {2}\right). \tag {I-5.54}
$$

Die Schwingung 2 A cos $\bar { \omega } t$ ist mit der Funktion cos $\frac { \Delta \omega } { 2 }$ t moduliert. Für $t = 0$ ist 2 A cos $\left( { \frac { \Delta \omega } { 2 } } \cdot 0 \right) = 2 A$ ; der nächste Zeitpunkt $t _ { 1 } ,$ für den $\left| 2 A \cos \frac{\Delta \omega}{2} t_1 \right| = 2 A$ wird, ist $t _ { 1 } = T _ { S } = \frac { 2 \pi } { \Delta \omega }$ . Die Zeitpunkte $t _ { n }$ , für die die Schwingungsamplitude maximal wird, sind also $t _ { n } = n \cdot \frac { 2 \pi } { \Delta \omega } , n = 0 , 1 , 2 ,$ …

![](images/page_298_chart_2.jpg)

<details>
<summary>line</summary>

| Time (t) | Signal (x(t)) |
| --- | --- |
| Start | ~0.8 |
| Peak 1 | ~1.0 |
| T_S | 0 |
| Peak 2 | ~1.0 |
| T_S + T_S | 0 |
| End | ~0.8 |
</details>

Abb. I-5.11: Bei Überlagerung zweier Schwingungen mit kleinem Frequenzunterschied $( \Delta \omega \ll \bar { \omega } )$ tritt eine Schwebung auf.

Die Schwebungsfrequenz $\nu _ { S } \quad ( T _ { S } = \frac { 1 } { \nu _ { S } }$ … Abstand zweier Schwebungsmaxima/ -minima) beträgt

$$
v _ {S} = \frac {1}{T _ {S}} = \frac {\Delta \omega}{2 \pi}. \tag {I-5.55}
$$

Schwebungen sind gut beobachtbar (in der Akustik gut hörbar) und dienen zum Abgleichen von Frequenzen (z. B. zum Stimmen von Instrumenten, die Töne sind gleich, wenn die Schwebung verschwindet).

1 Bei eindimensionaler Überlagerung zweier Schwingungen mit kleinem Frequenzunterschied $( \Delta \omega \ll \bar { \omega } )$ tritt eine Schwebung auf.
4 Zwei Stimmgabeln gleicher Frequenz sind an einem Schenkel mit einem kleinen Spiegel versehen. Sie sind Stimmgabel rotierender parallel zueinander orientiert und Spiegel werden elektromagnetisch zu Laser Schwingungen angeregt. Von einem Lichtstrahl (z. B. Laser) werden die Spiegel an beiden Stimmgabeln hintereinander beleuchtet. Der Lichtstrahl wird vom Spiegel der ersten Stimmgabel auf die zweite Gabel gelenkt und von dort über einen senkrecht zur Bewegungsrichtung der Stimmgabeln rotierenden Spiegel (Würfelspiegel) auf einen Schirm geworfen.

![](images/page_298_image_10.jpg)

<details>
<summary>text_image</summary>

λ(t₁)
λ(t₂)
</details>

Man sieht am Schirm das Summensignal der sich überlagernden Schwingungen der beiden Stimmgabeln zeitlich aufgelöst. Anschließend wird eine der beiden Stimmgabeln durch Verschiebung einer kleinen Masse auf einer Zinke leicht verstimmt: Es ist eine Schwebung zu beobachten.

## Zweidimensionale Überlagerung von Schwingungen

Wir summieren jetzt zwei zueinander normale Schwingungen gleicher Frequenz

$$
x (t) = A _ {1} \cos (\omega t), y (t) = A _ {2} \cos (\omega t + \varphi). \tag {I-5.56}
$$

Dabei ist $\varphi$ die relative Phasenverschiebung zwischen den beiden Schwingungen.

Um zur Bahnkurve der zusammengesetzten Schwingung zu gelangen, wird die Zeit eliminiert. Dazu bilden wir mit dem Additionstheorem $x / A_{1} = \cos \left( \omega t \right)$ und $y / A_{2} = \cos \left( \omega t \right)$ cos φ − sin (ωt) sin $\varphi .$ .

Für cos (ωt) in $y / A _ { 2 }$ wird $x / A _ { 1 }$ eingesetzt

$$
y / A _ {2} = (x / A _ {1}) \cos \varphi - \sin (\omega t) \sin \varphi \tag {I-5.57}
$$

$$
\Rightarrow \sin (\omega t) \sin \varphi = (x / A _ {1}) \cos \varphi - y / A _ {2}. \tag {I-5.58}
$$

Quadrieren unter Verwendung von sin $1^{2}\left ( \omega t \right ) = 1 - \cos^{2}\left ( \omega t \right ) = 1 - \frac{x^{2}}{A_{1}^{2}}$ gibt

$$
\left(1 - \frac {x ^ {2}}{A _ {1} ^ {2}}\right) \sin^ {2} \varphi = \frac {x ^ {2}}{A _ {1} ^ {2}} \cos^ {2} \varphi - \frac {2 x y}{A _ {1} A _ {2}} \cos \varphi + \frac {y ^ {2}}{A _ {2} ^ {2}} \tag {I-5.59}
$$

und damit

$$
\sin^ {2} \varphi = \frac {x ^ {2}}{A _ {1} ^ {2}} + \frac {y ^ {2}}{A _ {2} ^ {2}} - \frac {2 x y}{A _ {1} A _ {2}} \cos \varphi \tag {I-5.60}
$$

bzw.

$$
\frac {x ^ {2}}{A _ {1} ^ {2} \sin^ {2} \varphi} + \frac {y ^ {2}}{A _ {2} ^ {2} \sin^ {2} \varphi} - \frac {2 x y \cos \varphi}{A _ {1} A _ {2} \sin^ {2} \varphi} = 1. \tag {I-5.61}
$$

Mit den Abkürzungen $A = A _ { 1 }$ sin $\varphi$ und $B = A _ { 2 }$ sin $\varphi$ erhalten wir schließlich

$$
\frac {x ^ {2}}{A ^ {2}} + \frac {y ^ {2}}{B ^ {2}} - \frac {2 x y \cos \varphi}{A B} = 1. \tag {I-5.62}
$$

Das ist die Gleichung einer Ellipse, die gegen das Achsenkreuz um einen Winkel ψ gedreht ist $\left( \tan 2\psi = \frac{2A_{1}A_{2}\cos\varphi}{A_{1}^{2} - A_{2}^{2}} \right)$ und die Bahnkurve unseres schwingenden MP in der x-y-Ebene beschreibt (Abb. I-5.12).

![](images/page_300_image_2.jpg)

<details>
<summary>text_image</summary>

A₁ ≠ A₂
φ = 0°
φ = 60°
x
y
B
A₂
A
φ = 90°
</details>

Abb. I-5.12: Bahnkurven des MP für die Überlagerung zweier Schwingungen gleicher Frequenz, aber unterschiedlicher Amplitude, die normal zueinander sind. Die Phasen unterscheiden sich um den Winkel φ.

## Spezialfälle:

1. $\varphi = 0 : \Rightarrow x / A _ { 1 } = y / A _ { 2 }$ oder $y = ( A _ { 2 } / A _ { 1 } ) \; x$ .
Das ist die Gleichung einer Geraden durch den Ursprung (Abb. I-5.13).
2. $\varphi = ( \pi / 2 ) = 9 0 ^ { \circ } ; \Rightarrow \cos \varphi = 0$ und sin $\varphi = 1$ , also $A = A _ { 1 } ,   B = A _ { 2 }$ und es gilt $x ^ { 2 } / A _ { 1 } ^ { 2 } + y ^ { 2 } / A _ { 2 } ^ { 2 } = 1$ . Das ist eine Ellipse in Hauptlage und für den Fall $A _ { 1 }   =   A _ { 2 }$ (gleiche Amplituden der sich normal überlagernden Schwingungen) ergibt sich ein Kreis (Abb. I-5.13).

$$
A _ {1} = A _ {2}
$$

![](images/page_300_image_10.jpg)

<details>
<summary>text_image</summary>

φ = 0°
φ = 45°
φ = 90°
φ = 135°
</details>

Abb. I-5.13: Bahnkurven des MP für die Überlagerung zweier Schwingungen gleicher Frequenz und gleicher Amplitude, die normal zueinander sind. Die Phasen unterscheiden sich um den Winkel φ.

4

![](images/page_300_image_13.jpg)

<details>
<summary>natural_image</summary>

Simple white oval shape on black background, no text or symbols present
</details>

Die beiden Stimmgabeln des vorherigen Experiments gleicher Frequenz werden nun normal zueinander orientiert und wieder zu Schwingungen angeregt. Der Lichtstrahl, der von den Spiegeln beider Stimmgabeln kommt, wird jetzt direkt auf den Schirm geworfen. Man sieht am Schirm das Summensignal beider schwingenden Stimmgabeln, eine allgemeine Ellipse.

![](images/page_301_image_2.jpg)

<details>
<summary>natural_image</summary>

Abstract geometric pattern with concentric grid lines on a dark background (no text or symbols)
</details>

Jetzt wird wieder eine der beiden Stimmgabeln leicht gegen die andere verstimmt. Damit schwingen die Stimmgabeln mit den leicht unterschiedlichen Frequenzen $\omega _ { 1 }$ und $\omega _ { 2 } ;$ Es ergibt sich am Schirm eine komplizierte Bahnkurve und nur dann eine geschlossene Kurve, wenn das Verhältnis der Frequenzen $\omega _ { 1 } / \omega _ { 2 }$ rational ist. Bei irrationalen Verhältnissen der Frequenzen erfüllt die Bahnkurve im Laufe der Zeit die ganze Fläche des Rechteckes mit den Seiten 2 $\prime A _ { 1 }$ und $2   A _ { 2 } ,$

Die geschlossenen Bahnkurven für rationale Frequenzverhältnisse nennt man nach Jules Antoine Lissajous (1822–1880) ‚Lissajous-Figuren‘ (Abb. I-5.14).

![](images/page_301_image_5.jpg)

<details>
<summary>text_image</summary>

Δφ = φ₁ - φ₂
0°	45°	90°	135°	180°
1					\/
1/2					8	8
1/3						
2/3
</details>

Abb. I-5.14: Lissajous-Figuren für verschiedene rationale Frequenzverhältnisse und Phasendifferenzen.

Lissajous-Figuren können beim elastischen Schwingen von Stahlstäben unterschiedlichen Querschnitts (Quadrat, Rechteck, Kreis) sichtbar gemacht werden (Wheatstonesches Kaleidophon). Die unterschiedliche Biegesteifigkeit in den verschiedenen Schwingungsrichtungen führt zu Lissajous-Figuren, wenn man das obere Stabende beobachtet.

![](images/page_301_image_8.jpg)

## 5.1.3 Zerlegung von periodischen und unperiodischen Funktionen, Fourieranalyse und Fouriertransformation

Wir haben gesehen: Wenn N harmonische Schwingungen mit unterschiedlichen Amplituden $A _ { n } ,$ Frequenzen $\omega _ { n }$ und Anfangsphasen $\varphi _ { n }$ überlagert werden, so ergibt sich für die Summenschwingung (Gl. I-5.46)

$$
x (t) = \sum_ {n = 1} ^ {N} A _ {n} \cos (\omega_ {n} t + \varphi_ {n}).
$$

Diese Summenfunktion ist bei rationalen Frequenzverhältnissen immer noch periodisch und hat die Periodendauer $T   =   2   \pi / \omega _ { g } ,$ wobei $\omega _ { g }$ der größte gemeinsame Teiler aller beteiligten Frequenzen ist (Abb. I-5.15).

![](images/page_302_image_6.jpg)

Abb. I-5.15: Überlagerung von 5 Schwingungen gleicher Amplitude der Frequenzen nω bzw. $( 2 \; n - 1 ) \omega$ für $n = 1, 2, 3, 4, 5.$ . Die Amplitude der Summenfunktion ist verkleinert. (Nach W. Demtröder, Experimentalphysik 1: Mechanik und Wärme, Springer 1998.)

Gilt $z. B.  \omega_{n} = n \cdot \omega_{1}$ mit $n = \mathtt { g a n z } ,$ so ist die Periode von $x ( t ) T = 2   \pi / \omega _ { 1 }$

Für $\omega_{1}=4\ \omega,\ \omega_{2}=6\ \omega,\ \omega_{3}=10$ ω wäre $T = 2   \pi / 2   \omega = \pi / \omega$

Als Umkehrung gilt das Fouriersche Theorem (nach Joseph Fourier, 1768–1830):

1

Jede periodische Funktion f(t) mit $f ( t ) = f ( t + T )$ lässt sich in Summen von harmonischen Schwingungen (Sinus- und Kosinusfunktionen) zerlegen, für deren Frequenzen $\omega _ { n } = n . \omega _ { 1 }$ gilt, die also ganzzahlige Vielfache der Grundfrequenz $\omega _ { 1 } = \frac { 2 \pi } { T } .$ sind:

$$
\begin{array}{l} f (t) = A _ {0} + \sum_ {n = 1} ^ {\infty} A _ {n} \cos \left(n \omega_ {1} t - \varphi_ {n}\right) = \\ = \frac {a _ {0}}{2} + \sum_ {n = 1} ^ {\infty} a _ {n} \cos (n \omega_ {1} t) + \sum_ {n = 1} ^ {\infty} b _ {n} \sin (n \omega_ {1} t) \tag {I-5.63} \\ \end{array}
$$

Fourierreihenzerlegung (= Fourierreihe, Fourier series)

mit

$$
a _ {0} = 2 A _ {0}, \quad a _ {n} = A _ {n} \cos \varphi_ {n} \quad \text {und} \quad b _ {n} = A _ {n} \sin \varphi_ {n}.
$$

Dabei ist $\omega _ { 1 }$ die Grundfrequenz, die höherfrequenten Anteile n $\omega _ { 1 }$ nennt man Oberschwingungen. Die Koeffizienten $a _ { n }$ und $b _ { n }$ sind die Fourierkoeffizienten (Fourier coefficients) der Fourierzerlegung. Die Form des gesamten Schwingungsvorgangs ist durch die Amplituden $A _ { n }$ und die Phasen $\varphi _ { n }$ oder durch die $a _ { n }$ und $b _ { n }$ eindeutig bestimmt.

Mit der komplexen Schreibweise erhält man unter Beachtung von

$$
\cos \alpha = \frac {1}{2} \left(e ^ {i \alpha} + e ^ {- i \alpha}\right) \quad \text {und} \quad \sin \alpha = \frac {1}{2 i} \left(e ^ {i \alpha} - e ^ {- i \alpha}\right)
$$

$$
f (t) = \frac {a _ {0}}{2} + \sum_ {n = 1} ^ {\infty} e ^ {i n \omega_ {1} t} \underbrace {\left[ \frac {1}{2} \left(a _ {n} - i b _ {n}\right) \right]} _ {c _ {n}, n > 0} + \sum_ {n = - \infty} ^ {- 1} e ^ {i n \omega_ {1} t} \underbrace {\left[ \frac {1}{2} \left(a _ {- n} + i b _ {- n}\right) \right]} _ {c _ {n}, n <   0}. ^ {9} \tag {I-5.64}
$$

Setzen wir $c _ { 0 } = a _ { 0 } / 2 ,$ , so können wir die beiden Summen von 1 bis $\infty$ und von −∞ bis −1 in eine Summe von −∞ bis +∞ zusammenfügen und erhalten schließlich

$$
f (t) = \sum_ {n = - \infty} ^ {+ \infty} c _ {n} e ^ {i n \omega_ {1} t}. \tag {I-5.65}
$$

$$
\begin{array}{l} \left. \begin{array}{l} 9 a _ {n} \cos (n \omega_ {1} t) = \frac {1}{2} \left(a _ {n} e ^ {i n \omega_ {1} t} + a _ {n} e ^ {- i n \omega_ {1} t}\right) \\ b _ {n} \sin (n \omega_ {1} t) = \frac {1}{2 i} \left(b _ {n} e ^ {i n \omega_ {1} t} - b _ {n} e ^ {- i n \omega_ {1} t}\right) \end{array} \right\} \Rightarrow a _ {n} \cos (n \omega_ {1} t) + b _ {n} \sin (n \omega_ {1} t) = \\ = \underbrace {e ^ {i n \omega_ {1} t} \left[ \frac {1}{2} \left(a _ {n} - i b _ {n}\right) \right] + e ^ {- i n \omega_ {1} t} \left[ \frac {1}{2} \left(a _ {n} + i b _ {n}\right) \right]} _ {n > 0} = \underbrace {e ^ {i n \omega_ {1} t} \left[ \frac {1}{2} \left(a _ {n} - i b _ {n}\right) \right]} _ {n > 0} + \underbrace {e ^ {i n \omega_ {1} t} \left[ \frac {1}{2} a _ {- n} + i b _ {- n}\right)} _ {n <   0} \\ \end{array}
$$

Der Zusammenhang der komplexen Koeffizienten $c _ { n }$ mit den reellen Koeffizienten $a _ { n }$ und $b _ { n }$ , bzw. $A _ { n }$ und $\varphi _ { n }$ , ist daher so gegeben:

$$
c _ {n} = \left\{ \begin{array}{l l} \frac {1}{2} \left(a _ {n} - i b _ {n}\right) & \text {fur} n > 0 \\ \frac {a _ {0}}{2} & \text {fur} n = 0, A _ {n} = \sqrt {a _ {n} ^ {2} + b _ {n} ^ {2}}, \tan \varphi_ {n} = \frac {b _ {n}}{a _ {n}} \\ \frac {1}{2} \left(a _ {- n} + i b _ {- n}\right) & \text {fur} n <   0 \end{array} \right\}. ^ {1 0} \tag {I-5.66}
$$

$$
\Rightarrow \quad a _ {0} = 2 c _ {0}, \quad a _ {n} = c _ {n} + c _ {- n}, \quad b _ {n} = i (c _ {n} - c _ {- n}), \quad 1 \leq n \leq \infty .
$$

## Bestimmung der Amplituden

Um den Koeffizienten der m-ten Komponente zu finden, wird die Fourierzerlegung mit $e ^ { - i m \omega _ { 1 } t }$ multipliziert (dadurch wird, wie sich später zeigt, der Koeffizient $c _ { m }$ ausgewählt) und über eine ganze Periode integriert

$$
\int_ {0} ^ {T} f (t) e ^ {- i m \omega_ {1} t} d t = \int_ {0} ^ {T} \sum_ {n = - \infty} ^ {+ \infty} c _ {n} e ^ {i n \omega_ {1} t} e ^ {- i m \omega_ {1} t} d t = \sum_ {n = - \infty} ^ {+ \infty} \int_ {0} ^ {T} c _ {n} e ^ {i (n - m) \omega_ {1} t} d t \tag {I-5.67}
$$

Unter Beachtung von $\int   e ^ { a x } d x = { \frac { 1 } { a } } e ^ { a x }$ und $\omega _ { 1 }   =   2   \pi / T$ (im Nenner lassen wir dann $\omega _ { 1 }$ stehen) gilt

$$
\int_ {0} ^ {T} e ^ {i (n - m) \omega_ {1} t} d t = \frac {1}{i (n - m) \omega_ {1}} \left(e ^ {i (n - m) \omega_ {1} T} - 1\right) = \frac {e ^ {2 \pi i (n - m)} - 1}{i (n - m) \omega_ {1}}. \tag {I-5.68}
$$

Für den Fall $n \neq m$ folgt n − m = k = ganz und es ergibt sich

$$
\frac {e ^ {2 k \pi i} - 1}{i (n - m) \omega_ {1}} = 0 \tag {I-5.69}
$$

(d. h. $e ^ { i n \omega _ { 1 } t }$ und $e ^ { i m \omega _ { 1 } t }$ sind orthogonal 11), da gilt $e ^ { 2 k \pi i } = 1$

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">10 c<sub>n</sub> und c−n sind also konjugiert komplexe Zahlen: c<sub>n</sub> = c−n\* , a–n = a<sub>n</sub>, b–n = b<sub>n</sub>.</span></small>

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">11 Wenn das Integral zweier Funktionen f(t) und g(t) über den ‚Grundbereich‘ von t verschwindet (wie bei unseren Exponential- und Winkelfunktionen), dann nennt man die beiden Funktionen in Anlehnung an das Verschwinden des Skalarprodukts zweier senkrecht stehender Vektoren ‚orthogonal‘.</span></small>

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">Anmerkung: Die eben behandelten Funktionen (Winkelfunktionen bzw. komplexe Exponentialfunktionen stellen zwar die wichtigsten, aber nicht die einzigen orthogonalen Funktionensysteme</span></small>

Für den Fall $n = m$ folgt sofort

$$
\int_ {0} ^ {T} e ^ {i \cdot 0} d t = T. \tag {I-5.70}
$$

Es bleibt also in der Reihe nur der Term mit $c _ { n } = c _ { m }$ über<sup>12</sup> und wir erhalten also

$$
\int_ {0} ^ {T} f (t) e ^ {- i m \omega_ {1} t} d t = c _ {m} \cdot T = c _ {n} \cdot T \tag {I-5.71}
$$

(da ja $n = m )$ . Für den Fourierkoeffizienten gilt daher

$$
c _ {n} = \frac {1}{T} \int_ {0} ^ {T} f (t) e ^ {- i n \omega_ {1} t} d t. \tag {I-5.72}
$$

Die gesamte Fourierzerlegung kann also in komplexer Darstellung so geschrieben werden:

$$
f (t) = \sum_ {n = - \infty} ^ {\infty} c _ {n} e ^ {i n \omega_ {1} t} \quad \text {mit} \quad c _ {n} = \frac {1}{T} \int_ {0} ^ {T} f (t) e ^ {- i n \omega_ {1} t} d t. \tag {I-5.73}
$$

Über den bereits oben angegebenen Zusammenhang zwischen den komplexen und den reellen Koeffizienten (Gl. I-5.66) erhält man die reellen Amplituden des Fourierspektrums in Gl. (I-5.63):

$$
\text {fur} n = 0: \quad a _ {0} = 2 c _ {0}, \qquad \text {fur} n > 0: \quad a _ {n} = c _ {n} + c _ {- n} \quad \text {und} \quad b _ {n} = i (c _ {n} - c _ {- n}).
$$

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">dar. In der Quantenmechanik sind es vor allem die Legendreschen und die Laguerreschen Funktionen (beim Wasserstoffatom), die Hermiteschen Polynome (beim harmonischen Oszillator), wie überhaupt die Lösungen der so genannten Eigenwertgleichungen, also partieller Differentialgleichungen mit bestimmten Randwertbedingungen. Es sind dies orthogonale Funktionensysteme, mit deren Hilfe beliebige Funktionen als unendliche Reihen – wie oben mit Hilfe der Winkelfunktionen – dargestellt werden können. Sie stellen die Basisvektoren eines so genannten Hilbertraumes dar. Beispielsweise sind die oben betrachteten imaginären Exponentialfunktionen die Lösungen für die Eigenwertgleichung (also die Eigenfunktionen) der z-Komponente des Drehimpulses eines Elektrons im Zentralkraftfeld.</span></small>

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">12 Dies ist eine Folge der Orthogonalität der verwendeten Exponentialfunktionen, sodass allgemein T gilt e i(n−m)ω1tdt = T⋅ δnm. Dabei ist δmn das Kronecker Symbol: δmn = 1 für m = n, δmn = 0 für m ≠ n. 0</span></small>

Somit ergibt sich das Fourierspektrum eines mit T periodischen Vorgangs als Linienspektrum mit scharfen Linien bei ganzzahligen Vielfachen der Grundfrequenz $\omega _ { 1 }   =   2   \pi / T$ mit den Amplituden $( \mathrm { L i a g e n } ^ { \mathfrak { c } } ) a _ { n }$ und $b _ { n }$ (Abb. I-5.16).

![](images/page_306_chart_3.jpg)

<details>
<summary>spectrogram</summary>

| Category | Value |
| --- | --- |
| \(F(\omega)\) at 4π/T | High |
| \(F(\omega)\) at 6π/T | Medium |
| \(F(\omega)\) at 14π/T | Low |
</details>

Abb. I-5.16: Zerlegung eines periodischen Vorgangs in eine Fourierreihe.

**Beispiel:** Fourieranalyse einer Rechteckschwingung.

$$
f (t) = \left\{ \begin{array}{l l} A & \text {fur} 0 \leq t \leq T / 2 \\ 0 & \text {fur} T / 2 \leq t \leq T \end{array} : \right.
$$

![](images/page_306_chart_7.jpg)

<details>
<summary>line</summary>

| Time (t) | Value (f(t)) |
| --- | --- |
| 0 | A |
| T/2 | 0 |
| T | A |
| 2T | 0 |
</details>

Fourierzerlegung:

$$
f (t) = \sum_ {- \infty} ^ {+ \infty} c _ {n} e ^ {i n \omega_ {1} t}
$$

Koeffizienten:

$$
\begin{array}{l} c _ {0} = \frac {1}{T} \int_ {0} ^ {T} f (t) e ^ {0} d t = \frac {1}{T} \int_ {0} ^ {T / 2} A d t = \frac {A}{T} \left| t \right| _ {0} ^ {T / 2} = \frac {A}{T} \cdot \frac {T}{2} = \frac {A}{2} \\ c _ {1} = \frac {A}{T} \int_ {0} ^ {T / 2} e ^ {- i \omega_ {1} t} d t = \frac {A}{T} \left(- \frac {1}{i \omega_ {1}} e ^ {- i \omega_ {1} t}\right) \Bigg | _ {0} ^ {T / 2} = - \frac {A}{T} \frac {T}{2 \pi i} \left(e ^ {- \frac {2 \pi i}{T} \frac {T}{2}} - 1\right) = \\ = - \frac {A}{2 \pi i} \left(\underbrace {e ^ {- i \pi}} _ {- 1} - 1\right) = \frac {A}{\pi i} \\ \end{array}
$$

$$
c _ {- 1} = \frac {A}{2 \pi i} \left(\underbrace {e ^ {i \pi}} _ {- 1} - 1\right) = - \frac {A}{\pi i} \quad (\text {folgt auch daraus, dass} c _ {- n} = c _ {n} ^ {\star}).
$$

$$
\begin{array}{l} c _ {2} = \frac {A}{T} \int_ {0} ^ {T / 2} e ^ {- 2 i \omega_ {1} t} d t = \frac {A}{T} \left(- \frac {1}{2 i \omega_ {1}} e ^ {- 2 i \omega_ {1} t}\right) \Bigg | _ {0} ^ {T / 2} = - \frac {A}{T} \frac {T}{4 \pi i} \left(e ^ {\frac {- 4 \pi i}{T} \frac {T}{2}} - 1\right) = \\ = - \frac {A}{4 \pi i} \left(\underbrace {e ^ {- 2 \pi i}} _ {+ 1} - 1\right) = 0. \\ \end{array}
$$

Allgemein gilt:

$$
c _ {n} = \frac {A}{T} \int_ {0} ^ {T / 2} e ^ {- i n \omega_ {1} t} d t = \frac {A}{T} \left(\frac {- 1}{i n \omega_ {1}} e ^ {- i n \omega_ {1} t}\right) \bigg | _ {0} ^ {T / 2} = \frac {- A}{i 2 n \pi} \Big (e ^ {- i n \pi} - 1\left. \right)
$$

$$
\mathrm{Da} e ^ {\pm i 2 m \pi} = 0; e ^ {- i (2 m - 1) \pi} = - 1; e ^ {- i (- 2 m + 1) \pi} = - 1; m = 1, 2, 3, \dots
$$

ergibt sich

$$
\left. \begin{array}{l} c _ {2 m} = 0 \\ f u r n > 0 \quad c _ {2 m - 1} = \frac {A}{(2 m - 1) i \pi} \\ f u r n <   0 \quad c _ {- 2 m + 1} = \frac {A}{(- 2 m + 1) i \pi} \end{array} \right\} \Rightarrow c _ {n} = - c _ {- n}
$$

$$
\text {fur} n = 2 m \quad c _ {2 m} = 0, c _ {0} = \frac {A}{2}.
$$

In unserem Beispiel ergeben sich damit folgende reelle Koeffizienten:

$$
a _ {0} / 2 = A / 2, \quad a _ {n \neq 0} = c _ {n} + c _ {- n} = 0, \quad b _ {n = \text {gerade}} = 0,
$$

$$
b _ {n = \text {ungerade}} = i (c _ {n} - c _ {- n}) = i \cdot 2 c _ {2 m - 1} = \frac {i \cdot 2 A}{(2 m - 1) i \pi} = \frac {2 A}{(2 m - 1) \pi},
$$

also

$$
b _ {1} = \frac {2 A}{\pi}, b _ {3} = \frac {2 A}{3 \pi} (\mathrm{da} m = 2), b _ {5} = \frac {2 A}{5 \pi} (m = 3), \mathrm{usw.}, b _ {2} = 0, b _ {4} = 0, \mathrm{usw.}
$$

![](images/page_308_image_2.jpg)

## Ausdehnung auf unperiodische Funktionen

f(t) sei jetzt eine unperiodische Funktion. Wir lassen daher die Periode T in der Fourierzerlegung gegen ∞ gehen.

Für eine endliche Periode T gilt

$$
\frac {1}{T} = \nu_ {1} = \frac {\omega_ {1}}{2 \pi}, \tag {I-5.74}
$$

der Abstand der Frequenzen in der Fourierreihe ist

$$
\Delta \omega = (n + 1) \omega_ {1} - n \omega_ {1} = \omega_ {1}. \tag {I-5.75}
$$

Für $T   =   \frac { 2 \pi } { \omega _ { 1 } }   \rightarrow$ ∞ gilt daher $\omega _ { 1 } \to 0 , \mathrm { d . h . } \omega _ { 1 }$ wird differentiell klein, also

$\omega _ { 1 } = \Delta \omega \rightarrow d \omega .$ . Die in der Fourierreihe auftretenden Frequenzen $n \cdot \omega _ { 1 }$ liegen nun unendlich dicht, sodass $n \cdot \omega _ { 1 }$ zu einer stetigen Variablen ω wird, also $n \cdot \omega _ { 1 } \rightarrow \omega _ { 1 }$ jetzt kontinuierlich.

Der im Fourierkoeffizienten vor dem Integral stehende Faktor ${ \frac { 1 } { T } } = { \frac { \omega _ { 1 } } { 2 \pi } }$ geht für $T   \to   \infty$ über in lim $\frac{1}{T} = \lim_{\omega_1 \to 0} \frac{\omega_1}{2\pi} = \frac{d\omega}{2\pi} = d\nu$ T%∞

Also:

$$
\frac {1}{T} \longrightarrow d \nu = \frac {d \omega}{2 \pi}. \tag {I-5.76}
$$

Wir schreiben noch einmal die Fourierreihe mit eingesetzten Fourierkoeffizienten an, wobei wir aus Gründen der Übersichtlichkeit beim Übergang $T \to \infty$ die Zeitgrenzen von {0,T} auf {−T/2, T/2} ändern (‚Zeitverschiebung‘):

$$
\begin{array}{l} f (t) = \sum_ {- \infty} ^ {\infty} c _ {n} e ^ {i n \omega_ {1} t} = \sum_ {- \infty} ^ {\infty} \left[ \frac {1}{T} \int_ {- T / 2} ^ {T / 2} f (t) e ^ {- i n \omega_ {1} t} d t \right] e ^ {i n \omega_ {1} t} = \\ = \sum_ {- \infty} ^ {\infty} \left[ \int_ {- T / 2} ^ {T / 2} f (t) e ^ {- i n \omega_ {1} t} d t \right] e ^ {i n \omega_ {1} t} \underbrace {\frac {\Delta \omega}{2 \pi}} _ {= 1 / T} = \frac {1}{2 \pi} \sum_ {- \infty} ^ {\infty} \underbrace {\left[ \int_ {- T / 2} ^ {T / 2} f (t) e ^ {- i n \omega_ {1} t} d t \right]} _ {c _ {n}} e ^ {i n \omega_ {1} t} \Delta \omega . \tag {I-5.77} \\ \end{array}
$$

Beim Grenzübergang $T \to \infty$ gilt

$$
\sum_ {- \infty} ^ {+ \infty} \rightarrow \int_ {- \infty} ^ {+ \infty}, \Delta \omega \rightarrow d \omega , n \omega_ {1} \rightarrow \omega , c _ {n} \rightarrow F (\omega) = \int_ {- \infty} ^ {+ \infty} f (t) e ^ {- i \omega t} d t, \tag {I-5.78}
$$

das heißt, die Fourierkoeffizienten $c _ { n }$ werden nun zu einer stetigen Funktion $F ( \nu )$ der Frequenz ν bzw. $F ( \omega )$ der Frequenz ω (Fouriersches Integraltheorem)

$$
f (t) = \int_ {- \infty} ^ {+ \infty} F (\nu) e ^ {i 2 \pi \nu t} d \nu = \frac {1}{2 \pi} \int_ {- \infty} ^ {+ \infty} F (\omega) e ^ {i \omega t} d \omega \quad \begin{array}{l l} & \text {Fourierintegral} \\ & (\text {Fourier integral}). \end{array} \tag {I-5.79}
$$

Hierbei ist

$$
F (\omega) \equiv \int_ {- \infty} ^ {+ \infty} f (t) e ^ {- i \omega t} d t \quad \begin{array}{l l} & \text {die Fouriertransformierte} \\ & \text {der Funktion} f (t) \\ & (= \text {Dichte des Spektrums oder} \\ & \text {Spektralfunktion, Fourier transform).} ^ {1 3} \end{array} \tag {I-5.80}
$$

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">13 So wie man bei der Fourierreihe von der reellen zur komplexen Darstellung und umgekehrt wechseln kann (siehe Gl. I-5.64–Gl. I-5.73), – physikalische Realität besitzt nur die reelle Darstellung, die komplexe ist aber mathematisch weit vorteilhafter – so kann man auch vom komplexen Fourierintegral mit seinem komplexen Spektrum zur reellen Darstellung durch die Kosinustransformierte</span></small>

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">∞ Fcos (ω) = ∫f (t) cos ωtdt und die Sinustransformierte : 0</span></small>

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">Aus $F ( \omega ) = \frac { 1 } { 2 } \left[ F _ { \mathrm { c o s } } \left( \omega \right) - i F _ { \mathrm { s i n } } \right]$ (ω)] folgt: $F _ { \mathrm { c o s } } \left( \omega \right) = F ( \omega ) + F ^ { * } ( \omega ) ;   F _ { \mathrm { s i n } } \left( \omega \right) = i [ F ( \omega ) - F ^ { * } ( \omega ) ]$ , womit die reellen Kosinus- und Sinustransformierten aus der komplexen Fouriertransformierten gewonnen sind.</span></small>

F(ν)dν bzw. F(ω)dω entspricht also den früheren Entwicklungskoeffizienten (Fourierkoeffizienten) der periodischen Funktion. Man beachte, dass die Dimension der Variablen $\omega = { \frac { 2 \pi } { T } }$ der Fouriertransformierten reziprok zur Zeit t ist, also reziprok zur Dimension der Variablen des Fourierintegrals: Man spricht von ‚Reziprozität‘.

In der Praxis liegt eigentlich immer eine zeitlich begrenzte harmonische Schwingung vor, sie besitzt einen Anfang und ein Ende, es handelt sich also um einen ‚Puls‘. Davon kann keine Fourierreihenzerlegung in harmonische Schwingungen angegeben werden. Es ist aber durch Bildung des Fourierintegrals möglich, die Frequenzverteilung des Schwingungsvorgangs zu ermitteln (Abb. I-5.17). Je kürzer der Puls, umso breiter wird der zur Beschreibung nötige Frequenzbereich, je länger der Schwingungsvorgang andauert, umso schmäler wird sein Frequenzbereich.

![](images/page_310_chart_4.jpg)

<details>
<summary>spectrogram</summary>

| Parameter | Value |
| --- | --- |
| X-axis label | t |
| Y-axis label | f(t) |
| X-axis range | 0 ~ \(\omega\) |
| X-axis peak (unperiodischer Vorgang) | \(T\) |
| X-axis peak (kontinuierliches Frequenzspektrum) | \(F(\omega)\) |
| X-axis point | \(2\pi/T\) |
</details>

Abb. I-5.17: Zerlegung eines unperiodischen Vorgangs in ein Fourierintegral.

Die Fouriertransformierte einer reinen, zeitlich unbegrenzten Sinusschwingung der Frequenz $\omega _ { 1 }$ ergibt eine unendlich schmale, unendlich hohe Funktion $F ( \omega )$ , die um die Frequenz $\omega _ { 1 }$ zentriert ist. Sie wird δ-Funktion genannt.<sup>14</sup> Ein zeitlich konstanter Wert für f(t) ergibt als Transformierte eine δ-Funktion bei $\omega = 0$ , und umgekehrt (Abb. I-5.18).<sup>15</sup>

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">14 Die δ-Funktion ist überall Null außer an der Stelle x = 0 und es gilt: $\int \limits _ { - \infty } ^ { + \infty } \delta ( x )   d x = 1 .$ . Sie besitzt +∞ daher folgende wichtige Eigenschaft: ∫f (x)⋅δ (x − x0) dx = f (x0), sie bildet also die Funktion f(x) −∞ auf ihren Wert an der Stelle x<sub>0</sub> ab, sie ist ein Funktional (wie z. B. auch jedes bestimmte Integral). +∞ Mit x<sub>0</sub> = 0 gilt daher: ∫f (x) ⋅ δ (x) dx = f (0).</span></small>

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">15 Die nachfolgend angegebenen Fouriertransformierten (= Spektralfunktionen) folgen sofort aus der Integraldarstellung der δ-Funktion: δ(ω) = 1 ∞ e −iωt dt. Denn: 2 π −∞</span></small>

![](images/page_311_image_2.jpg)

Abb. I-5.18: Fouriertransformation einer reinen, zeitlich unbegrenzten Sinusschwingung (oben) und eines zeitlich konstanten Wertes (unten).

In anderen Bereichen der Physik, z. B. in der Wellenlehre (Akustik, Wellenoptik), wird häufig noch das Fourierintegral einer Ortsfunktion $f ( x )$ über $2   \pi / \lambda$ gebildet (λ ist die Wellenlänge einer periodischen Ortsfunktion), die Fouriertransformierte ist dann eine Funktion von $\frac { 2 \pi } { \lambda } = k _ { x }$ im reziproken Raum: Man spricht von Transformationspaaren (auch von ‚Dualität‘ oder ‚dualen Räumen‘).

$$
f(t)\leftrightarrow \underbrace{F(\omega)}_{\substack{\text{Frequenzspektrum}\\ \text{Energiespektrum} (E = \hbar \omega)}} = \text{Fouriertransformierte der Zeitfunktion}, \tag{I - 5.81}
$$

Kreisfrequenz $\omega = 2   \pi / T = 2$ π v und Zeit t sind ein duales Paar.

$$
f (x) \leftrightarrow \underbrace {F \left(k _ {x}\right)} _ {\text {Impulsspektrum} (p = \hbar k)} = \text {Fouriertransformierte der Ortsfunktion}, \tag {I-5.82}
$$

Wellenzahl $k _ { x } = 2   \pi / \lambda   ( \lambda$ … Wellenlänge) und Ort x sind ein duales Paar und es gilt

$$
f (x) = \frac {1}{2 \pi} \int_ {- \infty} ^ {+ \infty} F (k _ {x}) e ^ {i k _ {x} x} d k _ {x} \quad \text {mit} \quad F (k _ {x}) = F \left(\frac {2 \pi}{\lambda_ {x}}\right) = \int_ {- \infty} ^ {+ \infty} f (x) e ^ {- i k _ {x} x} d x. \tag {I-5.83}
$$

$$
F (\omega) = \underbrace {\int_ {- \infty} ^ {+ \infty} \frac {1}{2 \pi} e ^ {i \omega_ {1} t}} _ {f (t)} e ^ {- i \omega t} d t = \frac {1}{2 \pi} \int_ {- \infty} ^ {+ \infty} e ^ {- i (\omega - \omega_ {1}) t} d t = \delta (\omega - \omega_ {1}) \quad \text {und} \quad F (\omega) = \underbrace {\int_ {- \infty} ^ {+ \infty} \frac {1}{2 \pi} e ^ {- i \omega t}} _ {f (t)} d t = \delta (\omega).
$$

Für die ‚Fläche‘, die die δ-Funktion umschließt, gilt $\int \limits _ { - \infty } ^ { } \delta ( \omega - \omega _ { 1 } ) d \omega = 1$ . Außer der Stelle $\omega = \omega _ { 1 }$ ist die Funktion überall Null, woraus folgt, dass ihre Höhe an dieser Stelle ∞ ist.

Sowohl ω⋅t als auch $k _ { x } \cdot x$ sind dimensionslos, wie es sein muss, wenn sie als Exponent von e auftreten.

Es gilt folgende Analogie:

$$
2 \pi / T = (\text {Kreis}) \text {frequenz} \omega \text {mit} [ 1 / T ] = \mathrm{s} ^ {- 1}; 2 \pi / \lambda = (\text {Kreis}) \text {wellenzahl} k \text {mit} [ 1 / \lambda ] = \mathrm{m} ^ {- 1}.
$$

## 5.2 Der freie, gedämpfte Oszillator

## 4

Die Kugel hängt wieder an einer Spiralfeder in Ruhe, taucht aber jetzt in ein Becherglas mit einer zähen Flüssigkeit ein (z. B. Glycerin). Wird die Kugel a) aus der Ruhelage nach unten gestoßen oder b) langsam aus der Ruheposition etwas nach unten gezogen und dann losgelassen, so beginnt die Kugel wieder um die Ruhelage zu schwingen, die Amplitude der Schwingung nimmt aber mit jeder Schwingung stark ab und die Kugel kommt nach einigen wenigen Schwingungen wieder zur Ruhe.

![](images/page_312_image_8.jpg)

Die Änderung der Auslenkung eines MP wird also nicht nur durch die rücktreibende Federkraft bestimmt, sondern auch durch die Reibungskraft, wenn energieverzehrende (dissipative) Prozesse vorliegen.

Für den Reibungswiderstand einer Kugel in Flüssigkeiten gilt im Falle stationä- rer Bewegung näherungsweise das Stokessche Widerstandsgesetz für zähe Flüssigkeiten (vergleiche Kapitel „Mechanik deformierbarer Körper“, Abschnitt 4.3.7.2) $F _ { R } = - 6   \pi \eta n \nu$ . Dabei ist r der Radius einer Kugel, die von einer mit der Geschwindig keit υ strömenden Flüssigkeit der Zähigkeit η umströmt wird oder sich mit υ durch eine ruhende Flüssigkeit bewegt. (Die Schwingung ist aber keine stationäre Bewegung!)

Ganz allgemein setzt man eine Reibungskraft proportional zur Geschwindigkeit υ des sich bewegenden Körpers an,<sup>16</sup> solange diese Geschwindigkeiten hinreichend klein sind.<sup>17</sup> Bei eindimensionaler Bewegung in der x-Richtung gilt mit $\beta$ als Reibungskoeffizient:

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">16 Es gibt kein allgemeingültiges Reibungsgesetz. Die Erfahrung zeigt aber, dass die Reibungskraft stets den Betrag der Geschwindigkeit eines bewegten Körpers verkleinert und entgegengesetzt zur Richtung der Geschwindigkeit wirkt. Dies ist eine notwendige Folge der dissipativen Reibungsprozesse.</span></small>

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">17 Tritt bei der Bewegung des Körpers Wirbelbildung auf (Auto, Flugzeug), so ist die Widerstandskraft zu υproportional.</span></small>

$$
\vec {F} _ {R} = - \beta \dot {x} \vec {e} _ {x}. \tag {I-5.84}
$$

Außerdem wirkt wie bisher die rücktreibende Federkraft (Abschnitt 5.1.1, Gl. I-5.1)

$$
\vec {F} = - k x \vec {e} _ {x}.
$$

In Newton 2 eingesetzt ergibt das $m { \ddot { x } } = - k x - \beta { \dot { x } }$ und wir erhalten

$$
\ddot {x} + \frac {\beta}{m} \dot {x} + \frac {k}{m} x = 0. \tag {I-5.85}
$$

Wir setzen wie früher $\frac { k } { m } \equiv \omega _ { 0 } ^ { 2 }$ und jetzt zusätzlich $2   \gamma = { \frac { \beta } { m } } ,$

$$
\gamma = \frac {\beta}{2 m} \text {ist die dabei die Dämpfungskonstante}. \tag {I-5.86}
$$

So erhalten wir die Schwingungsgleichung des gedämpften Oszillators

$$
\ddot {x} + 2 \gamma \dot {x} + \omega_ {0} ^ {2} x = 0. \tag {I-5.87}
$$

Mit demselben Lösungsansatz wie für die ungedämpfte Schwingung $( \mathbf { A } \mathbf { b } -$ schnitt 5.1.1, Gl. I-5.14)

$$
x (t) = c e ^ {\lambda t}
$$

und $\dot { x } = c \lambda e ^ { \lambda t }$ und $\ddot { x } = c \lambda ^ { 2 } e ^ { \lambda t }$ ergibt sich die Bestimmungsgleichung (= charakteristische Gleichung) für λ zu

$$
\lambda^ {2} + 2 \gamma \lambda + \omega_ {0} ^ {2} = 0. \tag {I-5.88}
$$

Die Lösung dieser quadratischen Gleichung liefert $\lambda _ { 1 , 2 } = - \boldsymbol { \gamma } \pm \sqrt { \boldsymbol { \gamma } ^ { 2 } - \boldsymbol { \omega } _ { 0 } ^ { 2 } }$ und damit die allgemeine Lösung der Schwingungsgleichung

$$
x (t) = e ^ {- \gamma t} \left[ c _ {1} \cdot e ^ {\sqrt {\gamma^ {2} - \omega_ {0} ^ {2}} \cdot t} + c _ {2} \cdot e ^ {- \sqrt {\gamma^ {2} - \omega_ {0} ^ {2}} \cdot t} \right]. \tag {I-5.89}
$$

Das zeitliche Verhalten von $x ( t )$ hängt ganz wesentlich von $( \pmb { \gamma } ^ { 2 } - \omega _ { 0 } ^ { 2 } )$ ab und es lassen sich drei Fälle unterscheiden:

## 5.2.1 $\gamma ^ { 2 } < \omega _ { 0 } ^ { 2 } , \Leftrightarrow \beta ^ { 2 } < 4$ km, schwache Dämpfung (underdamped)

$\omega _ { 0 } ^ { 2 }$ ist größer als $\gamma ^ { 2 } ,$ , wir schreiben daher die Wurzel λ so:

$$
\lambda_ {1, 2} = - \gamma \pm \sqrt {- (\omega_ {0} ^ {2} - \gamma^ {2})} = - \gamma \pm \sqrt {- \omega^ {\prime 2}} = - \gamma \pm i \cdot \omega^ {\prime}, \tag {I-5.90}
$$

wobei wir für $\sqrt { \omega _ { 0 } ^ { 2 } - \gamma ^ { 2 } } \equiv \omega ^ { \prime }$ gesetzt haben. λ ist also in diesem Fall komplex.

Damit wird die allgemeine Lösung zu

$$
x (t) = e ^ {- \gamma t} (c e ^ {i \omega^ {\prime} t} + c ^ {\star} e ^ {- i \omega^ {\prime} t}) = A _ {0} e ^ {- \gamma t} \cos (\omega^ {\prime} t + \varphi). \tag {I-5.91}
$$

Die Koeffizienten c und $c ^ { * }$ sind jetzt wieder zueinander konjugiert komplexe Zahlen. In der komplexen Zahlenebene bedeutet diese Gleichung (Abb. I-5.19): Der Punkt $\vec { r } _ { c }$ läuft auf einer logarithmischen Spirale im Gegenuhrzeigersinn gegen den Nullpunkt (analog der Punkt $\vec { r } _ { c ^ { * } }$ im Uhrzeigersinn).

![](images/page_314_image_6.jpg)

<details>
<summary>text_image</summary>

r̅c* = c* e^{t(-γ-iω')}
r̅c = c e^{t(-γ+iω')}
δ = arccos(γ/ω₀) = const.
Im
Re
d r̅
φ
δ
δ
δ
δ
δ
δ
δ
δ
δ
δ
δ
δ
δ
δ
δ
δ
δ
δ
δ
δ
δ
δ
δ
δ
δ
δ
δ
δ
δ
δ
δ
δ
δ
δ
δ
δ
δ
δ
δ
δ
δ
δ
δ
δ
δ
δ
δ
δ
δ
δ
ε
ε
ε
ε
ε
ε
ε
ε
ε
ε
ε
ε
ε
ε
ε
ε
ε
ε
ε
ε
ε
ε
ε
ε
ε
ε
ε
ε
ε
ε
ε
ε
ε
ε
ε
ε
ε
ε
ε
ε
ε
ε
ε
ε
ε
ε
ε
ε
ε
ε
α
</details>

Abb. I-5.19: Darstellung der komplexen Kurven $\vec { r } _ { c }$ (rechts) und $\vec { r } _ { c } ^ { \mathrm { ~   ~ * ~ } }$ (links) der Gl. (I-5.91) in der komplexen Zahlenebene.

**Beispiel:** Berechnung des Winkels $\delta$ zwischen einer beliebigen Geraden durch den $\mathrm { { , } } \mathrm { { P o l } ^ { \mathrm { { e q } } } }$ einer logarithmischen Spirale und der Tangente an die Kurve im Schnittpunkt mit der Geraden, als Beispiel für das Rechnen mit der komplexen Exponentialfunktion.

Gesucht ist der Winkel $\delta = \angle ( \vec { r } , - d \vec { r } )$ .

Es gilt (mit c = 1):

$$
\vec {x} (t) = \vec {r} = e ^ {t (- \gamma + i \omega^ {\prime})}
$$

und damit

$$
d \vec {r} = \frac {d \vec {r}}{d t} d t = d t \underbrace {(- \gamma + i \omega^ {\prime})} _ {k \cdot e ^ {i \varphi}} \cdot \underbrace {e ^ {t (- \gamma + i \omega^ {\prime})}} _ {\vec {r}} = k \vec {r} \cdot e ^ {i \varphi} \cdot d t, ^ {1 8} \quad \varphi = \angle (\vec {r}, d \vec {r}),
$$

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">18 Die Multiplikation von r⇀mit k⋅e<sup>iφ</sup> bedeutet eine Streckung mit k und eine Drehung um φ.</span></small>

wobei die Exponentialdarstellung einer komplexen Zahl benutzt wurde:

$$
a + i b = \sqrt {a ^ {2} + b ^ {2}} \cdot e ^ {i \varphi} = k \cdot e ^ {i \varphi} \quad \text {mit} \quad \tan \varphi = \frac {b}{a}.
$$

In unserem Fall ist mit $k \cdot e ^ { i \varphi } = - \gamma + i \omega ^ { \prime } \rightarrow \tan \varphi = - \frac { \omega ^ { \prime } } { \gamma }$ , wobei $\varphi$ der Winkel zwischen $\vec { r }$ und $d \vec { r }$ ist. Für $\delta$ gilt $\delta = \pi - \varphi$ also tan $\delta = \tan \left( \pi - \varphi \right) = - \tan \varphi = \frac{\omega'}{\gamma}$ Daraus erhalten wir wegen

$$
\cos \alpha = \frac {1}{\sqrt {1 + \tan^ {2} \alpha}} \rightarrow \cos \delta = \frac {1}{\sqrt {1 + \tan^ {2} \delta}} = \frac {1}{\sqrt {1 + \frac {\omega^ {\prime 2}}{\gamma^ {2}}}} = \frac {\gamma}{\sqrt {\underbrace {\gamma^ {2} + \omega^ {\prime 2}} _ {\omega_ {0} ^ {2}}}} = \frac {\gamma}{\omega_ {0}}
$$

und damit $\delta = \operatorname { a r c c o s } \frac { \gamma } { \omega _ { 0 } }   .$

Es ergibt sich also wieder eine harmonische Schwingung cos $\left( \omega ^ { \prime } t + \varphi \right)$ , die aber mit der Funktion $f ( t ) = A ( t ) = A _ { 0 } \cdot e ^ { - \gamma t }$ moduliert ist, das heißt, die Amplitude A nimmt von ihrem Ausgangswert $A _ { 0 }$ bei $t = 0$ exponentiell mit der Zeit ab. Die Gesamtbewegung ist daher nicht mehr harmonisch, man nennt sie quasiharmonisch (Abb. I-5.20).

![](images/page_315_chart_8.jpg)

<details>
<summary>line</summary>

| Parameter | Value |
| --- | --- |
| Function | \(A(t) = A0e^(-\gamma t)\) |
| Period (T) | \(2\pi / \sqrt{\omega0^{2} - \gamma^{2}}\) |
| Period (1/\(\gamma\)) | N/A |
</details>

Abb. I-5.20: Zeitaufgelöste Bewegung des gedämpft schwingenden $M P$ für die Fälle: a) aus der Ruhelage gestoßen (blau) und b) aus der Ruhelage ausgelenkt und losgelassen (schwarz).

Die dabei auftretende Kreisfrequenz $\boldsymbol { \omega } ^ { \prime } = \sqrt { \boldsymbol { \omega } _ { 0 } ^ { 2 } - \boldsymbol { \gamma } ^ { 2 } }$ ist trotz gleicher Rückstellkraft kleiner als bei der ungedämpften Schwingung.

γ muss die Dimension einer reziproken Zeit haben: nach der Zeit $\tau   { = }   1 / \gamma$ ist die Einhüllende der gedämpften Schwingung auf $1 / e$ des Ausgangswertes gefallen $\left( A _ { 0 } e ^ { - \gamma \tau } = A _ { 0 } \frac { 1 } { e } \Rightarrow \tau = \frac { 1 } { \gamma } \right) .$

Für das Verhältnis zweier aufeinander folgender Ausschläge, die genau eine Schwingungsperiode $T = \frac { 2 \pi } { \omega ^ { \prime } } .$ auseinander liegen, gilt

$$
x (t) = A _ {0} e ^ {- \gamma t} \cos (\omega^ {\prime} t + \varphi)
$$

$$
x (t + T) = A _ {0} e ^ {- \gamma t} e ^ {- \gamma T} \cos (\omega^ {\prime} t + \varphi), \tag {I-5.92}
$$

da $e ^ { x + y } = e ^ { x } \cdot e ^ { y }$ und cos $\left[ \omega ( t + T ) + \varphi \right] = \cos \left( \omega t + \varphi \right)$

Damit ergibt sich für das Verhältnis der Ausschläge

$$
\frac {x (t + T)}{x (t)} = e ^ {- \gamma T}. \tag {I-5.93}
$$

Man nennt den Logarithmus des Kehrwerts dieses Verhältnisses der Ausschläge

$$
\ln \left[ \frac {x (t)}{x (t + T)} \right] = \boldsymbol {\gamma} \cdot T \equiv \delta \quad \text {logarithmisches Dekrement.} \tag {I-5.94}
$$

Wenn die Dämpfung klein ist, kann man für die Schwingungsdauer jene der ungedämpften Schwingung einsetzen und erhält

$$
\delta = \gamma \cdot T \approx 2 \pi \gamma \frac {1}{\omega_ {0}} = 2 \pi \gamma \sqrt {\frac {m}{k}} = 2 \pi \frac {\beta}{2 m} \sqrt {\frac {m}{k}} = \frac {\pi \beta}{\sqrt {m k}}. \tag {I-5.95}
$$

Das logarithmische Dekrement $\delta$ hängt also von allen drei die Schwingung bestimmenden Konstanten m, k und $\beta$ ab.

## 5.2.2 $\gamma ^ { 2 } > \omega _ { 0 } ^ { 2 } , \Leftrightarrow \beta ^ { 2 } > 4$ km, starke Dämpfung (overdamped)

Die Wurzeln der charakteristischen Gleichung sind jetzt reell

$$
\lambda_ {1, 2} = - \gamma \pm \sqrt {\gamma^ {2} - \omega_ {0} ^ {2}} = - \gamma \pm \alpha \quad \text {mit} \quad \alpha = \sqrt {\gamma^ {2} - \omega_ {0} ^ {2}} <   \gamma . \tag {I-5.96}
$$

Die allgemeine Lösung lautet daher

$$
x (t) = e ^ {- \gamma t} \left[ C _ {1} \cdot e ^ {\alpha t} + C _ {2} \cdot e ^ {- \alpha t} \right]. \tag {I-5.97}
$$

Die beiden Exponentialfunktionen der Lösung sind jetzt reell, daher sind auch die beiden Konstanten reell. Wegen $\gamma > \alpha$ ist auch der erste Summand eine fallende Exponentialfunktion $x _ { 1 } ( t ) = C _ { 1 } e ^ { ( \alpha - \gamma )   t }$

Zur Bestimmung der Koeffizienten aus den Anfangsbedingungen wählen wir zunächst $x ( t = 0 ) = x ( 0 ) = 0$ und $\dot { x } ( t = 0 ) = \dot { x } ( 0 ) = \upsilon _ { 0 } ,$ , das heißt wir stoßen den MP aus seiner Ruhelage heraus. Damit ergibt sich

$$
C _ {1} + C _ {2} = 0, \quad \text {also} \quad C _ {2} = - C _ {1}. \tag {I-5.98}
$$

Aus

$$
\dot {x} = - \gamma e ^ {- \gamma t} [ C _ {1} e ^ {\alpha t} + C _ {2} e ^ {- \alpha t} ] + e ^ {- \gamma t} [ C _ {1} \alpha e ^ {\alpha t} - C _ {2} \alpha e ^ {- \alpha t} ] \tag {I-5.99}
$$

erhält man $\dot { x } ( 0 ) = - \gamma ( C _ { 1 } + C _ { 2 } ) + \alpha ( C _ { 1 } - C _ { 2 } ) = \upsilon _ { 0 }$ . Der erste Term der Summe verschwindet (Gl. I-5.98), sodass gilt

$$
C _ {1} - C _ {2} = 2   C _ {1} = \frac {\nu_ {0}}{\alpha}. \tag {I-5.100}
$$

Für die Koeffizienten gilt also

$$
C _ {1} = \frac {\nu_ {0}}{2 \alpha}, C _ {2} = - \frac {\nu_ {0}}{2 \alpha}. \tag {I-5.101}
$$

Für die Bewegung des MP ergibt sich daher

$$
x (t) = \frac {\upsilon_ {0}}{2 \alpha} e ^ {- \gamma t} [ e ^ {\alpha t} - e ^ {- \alpha t} ]. \tag {I-5.102}
$$

Wir verwenden die Definition $\sinh ( x ) = { \frac { 1 } { 2 } } \left( e ^ { x } - e ^ { - x } \right)$ und erhalten schließlich für die Bewegung

$$
x (t) = \frac {\upsilon_ {0}}{\alpha} e ^ {- \gamma t} \sinh (\alpha t). \tag {I-5.103}
$$

Die Schwingung besteht jetzt aus einer anfänglichen Auslenkung, die langsam gegen Null geht. Wegen $\alpha < \gamma$ wird $x   =   0$ für $t \to \infty ;$ Da $[ e ^ { \alpha t }   -   e ^ { -   \alpha t } ]$ stets positiv ist, tritt keine quasiperiodische Oszillation mehr auf, sondern es wird nur mehr ein einziges Maximum des Ausschlags durchlaufen, es ist ein aperiodischer Kriechfall (Abb. I-5.21).

Lassen wir andererseits den MP von einer ausgelenkten Anfangslage $x _ { 0 }$ los, so ist $x ( 0 ) = x _ { 0 } ,   \dot { x } ( 0 ) = \upsilon _ { 0 } = 0$

$$
\text {Damit wird} C _ {1} + C _ {2} = x _ {0} \text {und} \dot {x} (0) = - \gamma (\underbrace {C _ {1} + C _ {2}} _ {x _ {0}}) + \alpha (\underbrace {C _ {1} - C _ {2}} _ {2 C _ {1} - x _ {0}}) = 0.
$$

Man erhält $C _ { 1 } = \frac { \chi _ { 0 } } { 2 \alpha } \; ( \alpha + \gamma )$ und $C _ { 2 } = \frac { x _ { 0 } } { 2 \alpha } \; ( \alpha - \gamma )$ und damit die zeitliche Bewegung zu

$$
x (t) = e ^ {- \gamma t} \frac {\chi_ {0}}{2 \alpha} \left[ (\alpha + \gamma) e ^ {\alpha t} + (\alpha - \gamma) e ^ {- \alpha t} \right]. \tag {I-5.104}
$$

In diesem Fall ‚kriecht‘ der MP also in die Ruhelage zurück, ohne dass er ein Maximum der Auslenkung durchläuft (Abb. I-5.22).

![](images/page_318_chart_4.jpg)

<details>
<summary>line</summary>

| Function | Peak Value |
| --- | --- |
| \(\nu_{0}te^{-}\gamma^{t}\) | ~High |
| \(\nu_{0}/\alpha e^{-}\gamma^{t}\)sinh(αt) | ~Medium |
</details>

Abb. I-5.21: Kriechfall (blaue Kurve) und aperiodischer Grenzfall (schwarz strichliert, siehe Abschnitt 5.2.3), wenn der MP aus der Ruhelage gestoßen wird $\alpha = 0 , 8 ; \gamma = 1 )$

![](images/page_318_chart_6.jpg)

<details>
<summary>line</summary>

| t | \(e^(-\gamma t)/2\alpha\) | \(x_{0}(1+\gamma t)e^{-\gamma t}\) |
| --- | --- | --- |
| 0 | ~1.0 | ~1.0 |
| High | Decreasing | Decreasing |
</details>

Abb. I-5.22: Kriechfall (blaue Kurve) und aperiodischer Grenzfall (strichliert, siehe Abschnitt 5.2.3), wenn der MP von der ausgelenkten Anfangslage $x _ { 0 }$ losgelassen wird $( \alpha = 0 , 8 ; \gamma = 1 )$

5.2.3 $\gamma ^ { 2 } = \omega _ { 0 } ^ { 2 } , \Leftrightarrow \beta ^ { 2 } = 4 \mathrm { k m } , \alpha = \sqrt { \gamma ^ { 2 } - \omega _ { 0 } ^ { 2 } } = 0 ,$ **, kritische Dämpfung (= aperiodischer Grenzfall, critically damped)**

Die Wurzeln λ der charakteristischen Gleichung sind jetzt entartet; da der Wurzelterm $\sqrt { \gamma ^ { 2 } - \omega _ { 0 } ^ { 2 } }$ verschwindet, gilt

$$
\lambda_ {1} = \lambda_ {2} = - \gamma \equiv \lambda . \tag {I-5.105}
$$

Es muss aber immer noch zwei Integrationskonstanten geben. Um sie zu bestimmen, setzen wir eine Lösung mit einem zeitabhängigen Vorfaktor im verbleibenden Rest der allgemeinen Lösung an

$$
x (t) = C (t) e ^ {\lambda t}. \tag {I-5.106}
$$

Durch differenzieren erhalten wir

$$
\dot {x} (t) = \dot {C} e ^ {\lambda t} + C \lambda e ^ {\lambda t} \quad \text {und} \quad \ddot {x} (t) = \ddot {C} e ^ {\lambda t} + \dot {C} \lambda e ^ {\lambda t} + C \lambda^ {2} e ^ {\lambda t} + \dot {C} \lambda e ^ {\lambda t}.
$$

In die Bewegungsgleichung $( \ddot { x } + 2 \gamma \dot { x } + \omega _ { 0 } ^ { 2 } x = 0$ , Gl. I-5.87) eingesetzt ergibt das

$$
\ddot {C} + \dot {C} (\underbrace {2 \lambda + 2 \gamma} _ {= 0}) + C (\underbrace {\lambda^ {2} + 2 \lambda \gamma + \omega_ {0} ^ {2}} _ {= 0}) = 0, \tag {I-5.107}
$$

da ja gilt: $\gamma = \omega _ { 0 }$ (kritisch gedämpft) und daher $\lambda = - \gamma = - \omega _ { 0 } .$

Damit ist $\ddot { C } = 0$ und es folgt $\dot { C } = \frac { d C } { d t } =$ const. mit der Lösung

$$
C = C _ {1} \cdot t + C _ {2}. \tag {I-5.108}
$$

Die allgemeine Lösung sieht daher so aus

$$
x (t) = (C _ {1} \cdot t + C _ {2}) e ^ {- \gamma t}. \tag {I-5.109}
$$

Für den Fall des MP, der aus der Ruhelage $( x = 0 )$ gestoßen wird $( \dot { x } ( 0 ) = \upsilon _ { 0 } )$ , erhalten wir für die Konstanten $C _ { 1 }$ und $C _ { 2 }$

$$
x (0) = C _ {2} = 0 \quad \text {und} \quad \dot {x} (0) = C _ {1} e ^ {- \gamma \cdot 0} - \gamma (C _ {1} \cdot 0 + C _ {2}) e ^ {- \gamma \cdot 0} = C _ {1} = v _ {0}. \tag {I-5.110}
$$

Damit wird die zeitliche Bewegung zu

$$
x (t) = v _ {0} t \cdot e ^ {- \gamma t}, \tag {I-5.111}
$$

sie ist also wieder aperiodisch, der MP kehrt aber in diesem Fall nach Durchlaufen einer maximalen Auslenkung schnellstmöglich in seine Ruhelage zurück: aperiodischer Grenzfall (Abb. I-5.20, schwarz strichlierte Kurve).

Wird der MP aus der Anfangslage $x _ { 0 } \neq 0$ losgelassen, gilt also jetzt $x ( 0 ) = x _ { 0 }$ und $\dot { x } ( 0 ) = v _ { 0 } = 0$ , so ergibt sich als Lösungsfunktion

$$
x (t) = x _ {0} (1 + \gamma t) e ^ {- \gamma t}, \tag {I-5.112}
$$

es wird kein Maximum mehr durchlaufen, da die 1. Ableitung für alle t negativ ist. Auch in diesem Fall erfolgt die Rückkehr in die Ruhelage maximal rasch (Abb. I-5.21, schwarz strichlierte Kurve).