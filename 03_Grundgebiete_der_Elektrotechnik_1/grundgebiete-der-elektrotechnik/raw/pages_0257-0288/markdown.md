![](images/page_256_image_2.jpg)

<details>
<summary>text_image</summary>

(1)
(2)
(3)
Φ₁
Φ₂
Φ₃
Fluss vernachlässigen!
Uges
B
</details>

Abb. 6.8: Teilflüsse bei mehreren Windungen.

## 6.1.4 Weitere Formen des Induktionsgesetzes

Sind mehrere Windungen hintereinander geschaltet und ist jede Windung von einem anderen Teil- oder Bündelfluss durchsetzt (Bild 6.8), so addieren sich die nach Gl. (6.2) induzierten Teilspannungen:

$$
u = u _ {1} + u _ {2} + u _ {3} = - \frac {\mathrm{d} \varPhi_ {1}}{\mathrm{d} t} - \frac {\mathrm{d} \varPhi_ {2}}{\mathrm{d} t} - \frac {\mathrm{d} \varPhi_ {3}}{\mathrm{d} t} = - \frac {\mathrm{d}}{\mathrm{d} t} \left(\varPhi_ {1} + \varPhi_ {2} + \varPhi_ {3}\right).
$$

Die Summe der Teilflüsse bezeichnet man als den verketteten magnetischen Fluss, Induktionsfluss oder Gesamtfluss und schreibt:

$$
\Psi = \Phi_ {1} + \Phi_ {2} + \Phi_ {3}.
$$

Damit hat man

$$
u = - \frac {\mathrm{d} \Psi}{\mathrm{d} t} \tag {6.10}
$$

und für eine Spule mit N Windungen, bei der die N Bündelflüsse gleich sind:

$$
u \approx - N \frac {\mathrm{d} \varPhi}{\mathrm{d} t}. \tag {6.11}
$$

## 6.1.5 Eine Folgerung aus dem Induktionsgesetz

Die in den früheren Abschnitten 3 und 4 behandelten elektrischen Felder waren wirbelfrei. Elektrische Felder, die durch Induktionswirkungen entstehen – also mit Magnetfeldern verknüpft sind, die sich zeitlich ändern –, sind nach Gl. (6.7) nicht wirbelfrei. Damit ist das Linienintegral der elektrischen Feldstärke nicht mehr wegunabhängig (Bild 6.9):

$$
\oint_ {L} \vec {E} \cdot \mathrm{d} \vec {s} = \int_ {(1) A} ^ {B} \vec {E} \cdot \mathrm{d} \vec {s} + \int_ {(2) B} ^ {A} \vec {E} \cdot \mathrm{d} \vec {s} = - \frac {\mathrm{d} \varPhi}{\mathrm{d} t}
$$

![](images/page_257_image_2.jpg)

<details>
<summary>text_image</summary>

(1)
Φ
A
B
(2)
</details>

Abb. 6.9: Zur Wegabhängigkeit des Integrals $\int _ { A } ^ { B } { \vec { E } } \cdot \mathsf { d } { \vec { s } }$

oder

$$
\int_ {(1) A} ^ {B} \vec {E} \cdot \mathrm{d} \vec {s} = \int_ {(2) A} ^ {B} \vec {E} \cdot \mathrm{d} \vec {s} - \frac {\mathrm{d} \varPhi}{\mathrm{d} t}.
$$

Diese Tatsache ist z. B. in der Messtechnik zu beachten, wenn es etwa darum geht, den Spannungsabfall an einem stromdurchflossenen Leiter zwischen den Punkten P und Q zu bestimmen (Bild 6.10). Wird die Messleitung entlang der Linie (1) verlegt, so zeigt das Messinstrument die Spannung $u _ { 1 }$ an; bei der gestrichelt dargestellten Leitungsführung (2) die Spannung $u _ { 2 }$ . Die beiden Spannungen unterscheiden sich um $\mathsf { d } \varPhi / _ { \mathsf { d } t } ,$ , wobei $\Phi$ die Differenz der von den Schleifen (1) und (2) umfassten Flüsse ist.

Die Größe $\mathsf { d } \varPhi / _ { \mathsf { d } t }$ und damit ein möglicher Messfehler wird besonders groß, wenn entweder das Magnetfeld sehr stark ist oder aber die Änderungsgeschwindigkeit des Flusses. Der erste Fall begegnet einem vor allem in der Hochstromtechnik, der zweite in der Hochfrequenztechnik.

## Beispiel 6.2: Rotierende Leiterschleife im Magnetfeld.

Aus einem Stück Draht mit dem ohmschen Widerstand R formt man eine rechteckige Schleife und versetzt sie in langsame, gleichförmige Drehbewegung mit n Umdrehungen pro Sekunde. Die Rotationsachse stehe senkrecht auf der Richtung des zeitlich konstanten, homogenen Magnetfeldes B, in welches die Schleife ganz hineintaucht (Bild 6.11).

a) Welche Wärmeverlustleistung entsteht in der Schleife?
b) Welches Drehmoment muss man dabei in den verschiedenen Stellungen überwinden?

![](images/page_257_image_13.jpg)

<details>
<summary>text_image</summary>

P (1)
u2(t) u1(t)
(2)
Φ(t)
i(t)
Q
</details>

Abb. 6.10: Messtechnische Anwendung zu Bild 6.9.

![](images/page_258_image_2.jpg)

<details>
<summary>text_image</summary>

B
a
b
φ
ω
</details>

Abb. 6.11: Rotierende Leiterschleife im Magnetfeld.

## Lösung:

$$
\begin{array}{l} \Phi = B a b \sin \underbrace {\omega t} _ {\varphi} \rightarrow u (t) = - \frac {\mathrm{d} \Phi}{\mathrm{d} t} = - \omega B a b \cos \omega t \\ i (t) = - \frac {\omega B a b}{R} \cos \omega t \quad \text { mit } \quad \omega = 2 \pi n. \\ \end{array}
$$

**a)** Leistung
b) Drehmoment $M _ { \mathrm { e l } } = P / \omega = \frac { \omega } { R } \left( B a b \right) ^ { 2 } \cos ^ { 2 } \omega t \qquad \mathrm { P r o b e } \left( M = - M _ { \mathrm { e l } } \right) ;$

$$
M = 2 \cdot F \cdot \frac {a}{2} \cos \omega t = a b i B \cos \omega t = - a b \frac {\omega B a b}{R} \cdot B \cos^ {2} \omega t = - \frac {\omega}{R} (B a b) ^ {2} \cos^ {2} \omega t.
$$

## 6.2 Die magnetische Feldenergie

## 6.2.1 Die zum Aufbau des Feldes erforderliche Energie

Zur Bestimmung der magnetischen Energie kann eine Anordnung nach Bild 6.12 be trachtet werden. Dabei soll der Eisenring einen so geringen Querschnitt im Vergleich zu den anderen Abmessungen haben, dass die magnetische Feldstärke im Ring als örtlich konstant angesehen werden kann. Zum Aufbau des Feldes ist Energie erforderlich, die von der Spannungsquelle geliefert wird. Um zu einer Energiebilanz zu kommen, stellt man zuerst die Maschengleichung unter Einbeziehung des Induktionsgesetzes nach Gl. (6.11) auf. Bei der im Bild gekennzeichneten Umlaufrichtung folgt:

![](images/page_258_image_13.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph LR
  A["Current i"] --> B["Resistor R"]
  C["Voltage u"] --> D["Magnetic Flux Φ"]
  E["Eisen Node N"] --> F["External Loop A"]
  B --> D
  D --> E
```
</details>

Abb. 6.12: Zur Bestimmung der magnetischen Feldenergie.

$$
- u + i R = - N \frac {\mathrm{d} \varPhi}{\mathrm{d} t}.
$$

Multipliziert man diese Gleichung mit i dt, so erhält man

$$
- u i \mathrm{d} t + i ^ {2} R \mathrm{d} t = - N i \mathrm{d} \varPhi .
$$

Hierbei ist der erste Summand die von der Spannungsquelle gelieferte elektrische Energie. Das Minuszeichen weist im Verbraucherzählpfeilsystem auf eine Energieabga be hin. Der zweite Summand stellt die im Widerstand in Wärme umgesetzte Energie dar. Der Term auf der rechten Seite muss die zum Aufbau des Magnetfeldes benötigte Energie sein, da weitere Energieformen hier nicht auftreten. Daraus folgt

$$
\mathrm{d} W _ {\mathrm{m}} = N i \mathrm{d} \Phi = i N A \mathrm{d} B. \tag {6.12}
$$

Der Index m wird im Folgenden weggelassen, da jetzt nur die magnetische Energie betrachtet wird und Verwechslungen nicht möglich sind. Der Zusammenhang zwischen dem Strom und der magnetischen Feldstärke ist für die vorliegende Anordnung durch Gl. (5.11) bekannt. Somit folgt aus Gl. (6.12):

$$
\mathrm{d} W = 2 \pi \varrho H A \mathrm{d} B.
$$

Hierin ist 2πϱA offensichtlich das Volumen des Eisenkerns, so dass sich ergibt:

$$
\mathrm{d} W = V H \mathrm{d} B
$$

oder

$$
W = V \int_ {0} ^ {B _ {\mathrm{e}}} H \mathrm{d} B. \tag {6.13}
$$

Hier bedeutet $B _ { \mathsf { e } }$ den Endwert der Flussdichte, der sich nach dem Aufbau des Magnetfeldes eingestellt hat. Für die Energie pro Volumen, also $w = W / _ { V } ,$ gilt

$$
w = \int_ {0} ^ {B _ {\mathrm{e}}} H \mathrm{d} B. \tag {6.14}
$$

Der analoge Ausdruck für das elektrische Feld ist in Bild 3.31 durch die schraffierte Fläche gekennzeichnet.

Bis jetzt wurde ein homogenes Magnetfeld vorausgesetzt. Im inhomogenen Fall ist noch über das Volumen zu integrieren:

$$
W = \int_ {V} w \mathrm{d} V. \tag {6.15}
$$

Das Integral Gl. (6.14) lässt sich, wenn die Permeabilität konstant ist, leicht auswerten:

$$
w = \int_ {0} ^ {B _ {\mathrm{e}}} \frac {B}{\mu} \mathrm{d} B = \frac {1}{2} \frac {B _ {\mathrm{e}} ^ {2}}{\mu}.
$$

Man lässt bei $B _ { \mathsf { e } }$ jetzt den Index e weg und notiert mit $B = \mu H$ insgesamt drei Ausdrücke für die magnetische **Energiedichte**:

$$
w = \frac {1}{2} \mu H ^ {2} = \frac {1}{2} B H = \frac {1}{2} \frac {B ^ {2}}{\mu}. \tag {6.16}
$$

Diese Ausdrücke entsprechen denen, die für das elektrische Feld durch Gl. (3.44) hergeleitet wurden.

## 6.2.2 Die Hystereseverluste

Wird bei einem Eisenkern mit der Kennlinie nach Bild 5.12 die magnetische Erregung von einem Endwert $H _ { \mathrm { e } }$ auf null verringert, so gewinnt man die magnetische Energie vollständig zurück. Anders ist es bei ferromagnetischen Stoffen, die die Erscheinung der Hysterese zeigen.

Das soll an Hand von Bild 6.13 erläutert werden. Die magnetische Feldstärke sei zunächst null. Ausgehend vom Zustand A wird H bis zu einem Endwert $H _ { \mathrm { e } }$ vergrößert. Dabei ist eine Arbeit aufzuwenden, die der waagerecht schraffierten Fläche entspricht.

![](images/page_260_image_10.jpg)

<details>
<summary>text_image</summary>

-Hₑ
C
A
B
Hₑ
</details>

Abb. 6.13: Hystereseverluste.

Beim Verringern der Feldstärke von $H _ { \mathrm { e } }$ auf null (Punkt C) wird Energie zurückgewonnen, die durch die senkrecht schraffierte Fläche gekennzeichnet ist. Lässt man nun H auf $- H _ { \mathrm { e } }$ anwachsen, so ist wieder Arbeit aufzuwenden, dargestellt durch die waagerecht schraffierte Fläche links von der Ordinatenachse. Bei der Rückkehr zum Ausgangspunkt A gewinnt man etwas Energie zurück, gekennzeichnet durch die senkrecht schraffierte Fläche. Insgesamt tritt also ein Energieverlust beim Durchlaufen der Hystereseschleife auf, der genau der von der Schleife umschlossenen Fläche entspricht. Derartige Verluste nennt man **Hystereseverluste**.

## 6.3 Induktivitäten

## 6.3.1 Die Selbstinduktivität

Betrachtet werden soll eine Leiterschleife, die an eine Quelle angeschlossen ist, die eine sich zeitlich ändernde Spannung liefert (Bild 6.14). Dann sind auch der sich einstellende Strom und das mit diesem verknüpfte Magnetfeld zeitlich veränderlich. Das Magnetfeld wirkt nach dem Induktionsgesetz bzw. der Lenzschen Regel auf die Leiterschleife zurück. Nach den Gln. (6.2) und (6.8) stellt sich ein solcher Strom ein, dass die Summe der Spannungen auf dem Umlauf L gleich der zeitlichen Abnahme des umfassten Flusses wird. Im vorliegenden Fall ergibt sich für einen Umlauf entlang der Leiterschleife im Sinne des eingezeichneten Pfeils bei Beachtung der Rechtsschraubenregel:

$$
- u + i R = - \frac {\mathrm{d} \varPhi}{\mathrm{d} t}. \tag {6.17}
$$

Zwischen dem Fluss $\Phi$ und dem Strom i besteht nach Abschnitt 5.6 oft ein linearer Zusammenhang. Dann setzt man

$$
\Phi = L \cdot i, \tag {6.18}
$$

wobei der Proportionalitätsfaktor L die **Selbstinduktivität** der Schleife genannt wird. Damit lässt sich Gl. (6.17) schreiben als

$$
- u + i R + L \frac {\mathrm{d} i}{\mathrm{d} t} = 0.
$$

Für diesen Zusammenhang kann man ein Ersatzschaltbild angeben, in dem die Wirkung der räumlich ausgedehnten Leiterschleife durch Schaltkreissymbole dargestellt wird (Bild 6.15). Die Selbstinduktivität kann man also als Schaltkreiselement auffassen, bei dem der Zusammenhang zwischen Spannung und Strom durch

![](images/page_261_image_12.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph LR
  u["u"] --> i["i"]
  i --> U(("Umlauf"))
  R["R"] --> U
  U --> \nΦ["Φ"]
```
</details>

Abb. 6.14: Stromdurchflossene Leiterschleife; Selbstinduktivität.

![](images/page_262_image_2.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph LR
  A["i"] --> B["R"]
  B --> C["L"]
  C --> D["u_L"]
  E(("u")) --> A
  style A fill:#fff,stroke:#333
  style B fill:#fff,stroke:#333
  style C fill:#fff,stroke:#333
  style D fill:#fff,stroke:#333
```
</details>

Abb. 6.15: Elektrisches Ersatzschaltbild der stromdurchflossenen Leiterschleife in Bild 6.14.

$$
u _ {L} = L \frac {\mathrm{d} i}{\mathrm{d} t} \tag {6.19}
$$

gegeben ist. Genauso wie bei elektrischen Widerständen sind den Größen Strom und Spannung Zählpfeile gleicher Richtung zuzuordnen.

Besteht die Leiterschleife aus N Windungen, so ist in den Gln. (6.17) und (6.18) an Stelle von Φ der Gesamtfluss $\Psi$ einzusetzen oder NΦ, wenn alle Windungen den gleichen Fluss umfassen:

$$
\Psi = L i \quad \text {bzw.} \quad N \Phi = L i . \tag {6.20}
$$

Formt man NΦ unter Berücksichtigung des Ohm’schen Gesetzes des magnetischen Kreises gemäß

$$
N \Phi = N \Theta \Lambda = N N i \Lambda = N ^ {2} \Lambda i
$$

um, so folgt durch Vergleich mit Gl. (6.20) für den Zusammenhang zwischen der Selbstinduktivität und dem magnetischen Leitwert:

$$
L = N ^ {2} \Lambda . \tag {6.21}
$$

## 6.3.2 Die Gegeninduktivität

Ist neben der einen stromdurchflossenen Leiterschleife nach Bild 6.14 in nicht allzu großer Entfernung noch eine zweite, gleichartige Leiterschleife vorhanden (Bild 6.16), so werden sich die Leiterschleifen über die mit ihnen verknüpften magnetischen Felder gegenseitig beeinflussen. Das Induktionsgesetz auf beide Schleifen angewendet ergibt

![](images/page_262_image_15.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph LR
  u1["u1"] --> i1["i1"]
  i1 --> R1["R1"]
  R1 --> u1
  u1 --> i2["i2"]
  i2 --> u2["u2"]
  u2 --> i2
  u2 --> R2["R2"]
  R2 --> u2
  u2 --> R2
  R2 --> \nFif1["\nFif1"] --> R1
  R1 --> \nFif2["\nFif2"] --> R1
  R1 --> \nFif3["\nFif3"] --> R1
  R1 --> \nFif4["\nFif4"] --> R1
  R1 --> \nFif5["\nFif5"] --> R1
  R1 --> \nFif6["\nFif6"] --> R1
  R1 --> \nFif7["\nFif7"] --> R1
  R1 --> \nFif8["\nFif8"] --> R1
  R1 --> \nFif9["\nFif9"] --> R1
  R1 --> \nFif10["\nFif10"] --> R1
  R1 --> \nFif11["\nFif11"] --> R1
  R1 --> \nFif12["\nFif12"] --> R1
  R1 --> \nFif13["\nFif13"] --> R1
  R1 --> \nFif14["\nFif14"] --> R1
  R1 --> \nFif15["\nFif15"] --> R1
  R1 --> \nFif16["\nFif16"] --> R1
  R1 --> \nFif17["\nFif17"] --> R1
  R1 --> \nFif18["\nFif18"] --> R1
  R1 --> \nFif19["\nFif19"] --> R1
  R1 --> \nFif20["\nFif20"] --> R1
  R1 --> \nFif21["\nFif21"] --> R1
  R1 --> \nFif22["\nFif22"] --> R1
  R1 --> \nFif23["\nFif23"] --> R1
  R1 --> \nFif24["\nFif24"] --> R1
  R1 --> \nFif25["\nFif25"] --> R1
  R1 --> \nFif26["\nFif26"] --> R1
  R1 --> \nFif27["\nFif27"] --> R1
  R1 --> \nFif28["\nFif28"] --> R1
  R1 --> \nFif29["\nFif29"] --> R1
  R1 --> \nFif30["\nFif30"] --> R1
  R1 --> \nFif31["\nFif31"] --> R1
  R1 --> \nFif32["\nFif32"] --> R1
  R1 --> \nFif33["\nFif33"] --> R1
  R1 --> \nFif34["\nFif34"] --> R1
  R1 --> \nFif35["\nFif35"] --> R1
  R1 --> \nFif36["\nFif36"] --> R1
  R1 --> \nFif37["\nFif37"] --> R1
  R1 --> \nFif38["\nFif38"] --> R1
  R1 --> \nFif39["\nFif39"] --> R1
  R1 --> \nFif40["\nFif40"] --> R1
  R1 --> \nFif41["\nFif41"] --> R1
  R1 --> \nFif42["\nFif42"] --> R1
  R1 --> \nFif43["\nFif43"] --> R1
  R1 --> \nFif44["\nFif44"] --> R1
  R1 --> \nFif45["\nFif45"] --> R1
  R1 --> \nFif46["\nFif46"] --> R1
  R1 --> \nFif47["\nFif47"] --> R1
  R1 --> \nFif48["\nFif48"] --> R1
  R1 --> \nFif49["\nFif49"] --> R1
  R1 --> \nFif50["\nFif50"] --> R1
  R1 --> \nFif51["\nFif51"] --> R1
  R1 --> \nFif52["\nFif52"] --> R1
  R1 --> \nFif53["\nFif53"] --> R1
  R1 --> \nFif54["\nFif54"] --> R1
  R1 --> \nFif55["\nFif55"] --> R1
  R1 --> \nFif56["\nFif56"] --> R1
  R1 --> \nFif57["\nFif57"] --> R1
  R1 --> \nFif58["\nFif58"] --> R1
  R1 --> \nFif59["\nFif59"] --> R1
  R1 --> \nFif60["\nFif60"] --> R1
  u2_((2)) -.-> i2_((2))
  u2_((2)) -.-> i2_((2))
```
</details>

Abb. 6.16: Zwei magnetisch gekoppelte Leiterschleifen.

$$
\begin{array}{l} - u _ {1} + i _ {1} R _ {1} = - \frac {\mathrm{d} \varPhi_ {1}}{\mathrm{d} t}, \\ - u _ {2} + i _ {2} R _ {2} = - \frac {\mathrm{d} \varPhi_ {2}}{\mathrm{d} t}. \tag {6.22} \\ \end{array}
$$

Die Flüsse $\Phi _ { 1 }$ und $\Phi _ { 2 }$ werden jetzt von beiden Strömen verursacht. Unterstellt man wieder einen linearen Zusammenhang zwischen Strömen und Flüssen, so kann man $\Phi _ { 1 }$ und $\Phi _ { 2 }$ als Summe von Teilflüssen darstellen. Ist der Beitrag des Stromes $i _ { 1 }$ zum Fluss in Schleife 1

$$
\Phi_ {1 1} = L _ {1 1} i _ {1} \tag {6.23}
$$

und der Beitrag des Stromes $i _ { 2 }$ zum Fluss in derselben Schleife

$$
\Phi_ {1 2} = L _ {1 2} i _ {2}, \tag {6.24}
$$

so folgt der Gesamtfluss in Schleife 1:

$$
\Phi_ {1} = \Phi_ {1 1} + \Phi_ {1 2} = L _ {1 1} i _ {1} + L _ {1 2} i _ {2}. \tag {6.25}
$$

Entsprechend ergibt sich für den Fluss in Schleife 2:

$$
\Phi_ {2} = \Phi_ {2 1} + \Phi_ {2 2} = L _ {2 1} i _ {1} + L _ {2 2} i _ {2}. \tag {6.26}
$$

Die hier eingeführten Proportionalitätsfaktoren $L _ { 1 1 }$ und $L _ { 2 2 }$ sind die Selbstinduktivitä- ten der Schleifen 1 und 2. Man kann schreiben

$$
L _ {1 1} = L _ {1} \quad \text {und} \quad L _ {2 2} = L _ {2}. \tag {6.27}
$$

Die Größen $L _ { 1 2 }$ und $L _ { 2 1 }$ nennt man die Gegeninduktivitäten zwischen den beiden Schleifen. Wie in Abschnitt 6.3.3 gezeigt wird, sind beide Größen gleich; üblich ist die Bezeichnung

$$
L _ {1 2} = L _ {2 1} = M. \tag {6.28}
$$

Setzt man die Gln. (6.25) und (6.26) unter Beachtung der Gln. (6.27) und (6.28) in Gl. (6.22) ein, so erhält man

$$
\begin{array}{l} - u _ {1} + i _ {1} R _ {1} = - L _ {1} \frac {\mathrm{d} i _ {1}}{\mathrm{d} t} - M \frac {\mathrm{d} i _ {2}}{\mathrm{d} t}, \\ - u _ {2} + i _ {2} R _ {2} = - L _ {2} \frac {\mathrm{d} i _ {2}}{\mathrm{d} t} - M \frac {\mathrm{d} i _ {1}}{\mathrm{d} t}. \tag {6.29} \\ \end{array}
$$

Indem man in der ersten Gleichung den Term $M ^ { \mathrm { d } i _ { 1 } } / \mathrm { d } t$ hinzufügt und wieder abzieht, in der zweiten Zeile entsprechend mit dem Summanden $M   \mathrm { d } i _ { 2 } \big / \mathrm { d } t$ verfährt, kann man durch zweckmäßiges Zusammenfassen folgende Gleichungen erhalten:

$$
\begin{array}{l} - u _ {1} + R _ {1} i _ {1} + (L _ {1} - M) \frac {\mathrm{d} i _ {1}}{\mathrm{d} t} + M \frac {\mathrm{d} (i _ {1} + i _ {2})}{\mathrm{d} t} = 0, \\ - u _ {2} + R _ {2} i _ {2} + (L _ {2} - M) \frac {\mathrm{d} i _ {2}}{\mathrm{d} t} + M \frac {\mathrm{d} (i _ {1} + i _ {2})}{\mathrm{d} t} = 0. \tag {6.30} \\ \end{array}
$$

Diese Gleichungen lassen sich durch die Ersatzschaltung nach Bild 6.17 darstellen.

Hat man an Stelle der Schleifen 1 und 2 jetzt Wicklungen mit $N _ { 1 }$ bzw. $N _ { 2 }$ Windungen, so muss in den Gln. (6.22) bis (6.26) der Fluss $\Phi$ jeweils durch den Gesamtfluss Ψ ersetzt werden. Unter der Annahme, dass jedes Mal alle Windungen den gleichen Fluss umfassen, wird z. B. aus der linken Seite von Gl. (6.24), ein unverzweigter magnetischer Kreis vorausgesetzt:

$$
\Psi_ {1 2} = N _ {1} \varPhi_ {1 2} = N _ {1} (\varTheta_ {2} \varLambda) = N _ {1} N _ {2} \varLambda i _ {2}.
$$

Für die rechte Seite schreibt man wegen Gl. (6.28) $M i _ { 2 }$ und erhält durch Vergleich:

$$
M = N _ {1} N _ {2} \Lambda . \tag {6.31}
$$

Es fehlt noch eine Maßeinheit für L (bzw. M).

Mit Gl. (6.18) wird

$$
[ L ] = \frac {[ \varPhi ]}{[ I ]} = \frac {\mathrm{Vs}}{\mathrm{A}} = \Omega \mathrm{s},
$$

wofür man abkürzend schreibt

$$
1 \Omega \mathrm{s} = 1 \text {Henry} = 1 \mathrm{H}.
$$

## 6.3.3 Die magnetische Energie eines Systems stromdurchflossener Leiterschleifen

Zunächst soll die magnetische Energie berechnet werden, die das Feld einer Spule mit der Induktivität L speichert, wenn durch die Spulenwicklung der Strom I fließt. Man geht wie in Abschnitt 3.8.1 von der Beziehung

$$
W _ {\mathrm{m}} = \int_ {0} ^ {\infty} u (t) i (t)   \mathrm{d} t
$$

aus und setzt für die Spannung, die an der Spule anliegt, gemäß Gl. (6.19)

$$
u = L \frac {\mathrm{d} i}{\mathrm{d} t}
$$

ein. Dann wird

$$
W _ {\mathrm{m}} = \int_ {0} ^ {\infty} L \frac {\mathrm{d} i}{\mathrm{d} t} i \mathrm{d} t = \int_ {0} ^ {I} L i \mathrm{d} i.
$$

![](images/page_264_image_19.jpg)

<details>
<summary>text_image</summary>

i₁
R₁ L₁-M L₂-M R₂ i₂
u₁ M u₂
</details>

Abb. 6.17: Ersatzschaltbild zu Bild 6.16.

Hierbei bedeutet I den zeitlich konstanten Spulenstrom. Ist L konstant, was hier vorausgesetzt wird, dann folgt

$$
W _ {\mathrm{m}} = \frac {1}{2} L I ^ {2}. \tag {6.32}
$$

Hat man zwei Spulen mit den Induktivitäten $L _ { 1 }$ und $L _ { 2 }$ und sind die zugehörigen Ströme $I _ { 1 }$ und $I _ { 2 }$ , so werden die Energien

$$
W _ {1} = \frac {1}{2} L _ {1} I _ {1} ^ {2} \quad \text {und} \quad W _ {2} = \frac {1}{2} L _ {2} I _ {2} ^ {2}
$$

gespeichert, solange zwischen beiden Spulen keine magnetische Kopplung besteht.

Nun soll berechnet werden, wie sich die Energie ändert, wenn eine solche Kopplung vorliegt. Die Zählrichtungen beziehen sich auf Bild 6.16. Die ohmschen Widerstände sollen aber vernachlässigt werden. Damit werden die Spannungsgleichungen (6.17) unter Berücksichtigung der Gln. (6.25) und (6.26):

$$
u _ {1} = L _ {1} \frac {\mathrm{d} i _ {1}}{\mathrm{d} t} + L _ {1 2} \frac {\mathrm{d} i _ {2}}{\mathrm{d} t},
$$

$$
u _ {2} = L _ {2} \frac {\mathrm{d} i _ {2}}{\mathrm{d} t} + L _ {2 1} \frac {\mathrm{d} i _ {1}}{\mathrm{d} t}. \tag {6.33}
$$

Innerhalb des Zeitintervalls dt geben die Spannungsquellen die Energien ab:

$$
u _ {1} i _ {1} \mathrm{d} t = L _ {1} i _ {1} \mathrm{d} i _ {1} + L _ {1 2} i _ {1} \mathrm{d} i _ {2},
$$

$$
u _ {2} i _ {2} \mathrm{d} t = L _ {2} i _ {2} \mathrm{d} i _ {2} + L _ {2 1} i _ {2} \mathrm{d} i _ {1}.
$$

Es können zwei Fälle unterschieden werden:

**Fall a:** In Spule 1 fließt schon der Endwert des Stromes, also $i _ { 1 } = I _ { 1 }$ und $\mathbf { d } i _ { 1 } = 0$ . In Spule 2 soll der Strom von Null auf den Endwert $I _ { 2 }$ vergrößert werden. Damit wird der gesamte Energiezuwachs

$$
\mathrm{d} W _ {\mathrm{a}} = u _ {1} I _ {1} \mathrm{d} t + u _ {2} i _ {2} \mathrm{d} t = L _ {1 2} I _ {1} \mathrm{d} i _ {2} + L _ {2} i _ {2} \mathrm{d} i _ {2}
$$

und nach Integration über $\mathrm { d } i _ { 2 }$ von Null bis $I _ { 2 }$ :

$$
W _ {\mathrm{a}} = L _ {1 2} I _ {1} I _ {2} + \frac {1}{2} L _ {2} I _ {2} ^ {2}.
$$

Die gesamte Energie des Systems ist demnach gleich der Summe aus dem Energiebeitrag $1 / _ { 2 } L _ { 1 } I _ { 1 } ^ { 2 }$ , der nur von $I _ { 1 }$ abhängt, und dem soeben ermittelten Anteil $W _ { \mathbf { a } }$ , also

$$
W _ {\mathrm{ges}} = \frac {1}{2} L _ {1} I _ {1} ^ {2} + L _ {1 2} I _ {1} I _ {2} + \frac {1}{2} L _ {2} I _ {2} ^ {2}. \tag {6.34}
$$

**Fall b:** In Spule 2 hat sich bereits der Endwert des Stromes eingestellt: $i _ { 2 } = I _ { 2 } ; \mathbf { d } i _ { 2 } = 0 .$ In Spule 1 wächst der Strom von Null auf $I _ { 1 }$ . Damit ergibt sich ein Energiezuwachs von

$$
\mathrm{d} W _ {\mathrm{b}} = u _ {1} i _ {1} \mathrm{d} t + u _ {2} I _ {2} \mathrm{d} t = L _ {1} i _ {1} \mathrm{d} i _ {1} + L _ {2 1} i _ {2} \mathrm{d} i _ {1}
$$

und nach Integration:

$$
W _ {\mathrm{b}} = \frac {1}{2} L _ {1} I _ {1} ^ {2} + L _ {2 1} I _ {2} I _ {1}.
$$

Die gesamte Energie ergibt sich in Analogie zu Gl. (6.34) zu:

$$
W _ {\mathrm{ges}} = \frac {1}{2} L _ {2} I _ {2} ^ {2} + L _ {2 1} I _ {2} I _ {1} + \frac {1}{2} L _ {1} I _ {1} ^ {2}. \tag {6.35}
$$

Da die Energie des Systems nicht davon abhängen kann, in welcher Reihenfolge die Ströme ihre Endwerte erreichen, müssen die mit den Gln. (6.34) und (6.35) bezeichneten Ausdrücke übereinstimmen, womit

$$
L _ {1 2} = L _ {2 1} \tag {6.36}
$$

wird. Diesen Zusammenhang nennt man den **Umkehrungssatz**. Verwendet man gemäß Gl. (6.28) die Abkürzung M, so folgt für die magnetische Energie des betrachteten Systems:

$$
W _ {\mathrm{m}} = \frac {1}{2} L _ {1} I _ {1} ^ {2} + M I _ {1} I _ {2} + \frac {1}{2} L _ {2} I _ {2} ^ {2}. \tag {6.37}
$$

Es lässt sich zeigen, dass für ein System aus n stromdurchflossenen Leiterschleifen die Formel gilt:

$$
W _ {\mathrm{m}} = \frac {1}{2} \sum_ {\mu = 1} ^ {n} \sum_ {\nu = 1} ^ {n} L _ {\mu \nu} I _ {\mu} I _ {\nu}. \tag {6.38}
$$

Darin bedeutet dann $L _ { \mu \mu }$ die Selbstinduktivität der $\mu \cdot$ ten Leiterschleife und $L _ { \mu \nu } = L _ { \nu \mu }$ die Gegeninduktivität zwischen der μ-ten und der ν-ten Schleife.

## Beispiel 6.3: Ersatzinduktivität.

Gegeben ist ein magnetischer Kreis mit zwei Spulen. Ihre Induktivitäten sind $L _ { 1 }$ und $L _ { 2 }$ und zwischen beiden Spulen besteht die Gegeninduktivität M, Bild 6.18. Die magnetischen Flüsse sollen vollständig im Eisen verlaufen. Damit enthalten $L _ { 1 } , L _ { 2 }$ , M die Wirkung des Eisens.

a) Wie groß ist die in diesem Kreis gespeicherte magnetische Energie?
b) Jetzt werden beide Spulen hintereinander geschaltet, und zwar so, dass α) $\boldsymbol{i}_{1}=\boldsymbol{i}_{2}, \boldsymbol{\beta}) \boldsymbol{i}_{1}=-\boldsymbol{i}_{2}$ ist.

Wie müsste jeweils die Induktivität einer Ersatzspule gewählt werden, damit bei gleichem Strom die gleiche magnetische Energie gespeichert wird?

![](images/page_266_image_19.jpg)

<details>
<summary>text_image</summary>

i₁
M
Eisen
L₁
L₂
i₂
</details>

Abb. 6.18: Eisenkern mit zwei Wicklungen und zugeordneten Induktivitäten: Gegeninduktivität M sowie Selbstinduktivitäten $L _ { 1 }$ und $L _ { 2 }$

## Lösung:

b) 1/2Lα i<sup>2</sup><sub>1</sub> = 1/2L1i<sup>2</sup><sub>1</sub> + Mi<sup>2</sup><sub>1</sub> + 1/2L2i<sup>2</sup><sub>1</sub>

$$
\rightarrow L _ {\alpha} = L _ {1} + L _ {2} + 2 M,
$$

entsprechend

$$
\rightarrow L _ {\beta} = L _ {1} + L _ {2} - 2 M.
$$

## 6.3.4 Methoden zur Berechnung von Selbst- und Gegeninduktivitäten

Geht man von den durch die Gln. (6.13) und (6.19) gegebenen Definitionen aus, so kann man Selbst- und Gegeninduktivitäten über die magnetischen Flüsse ausrechnen:

$$
L = \frac {\Phi}{I} \tag {6.39}
$$

und

$$
M \equiv L _ {1 2} = \frac {\Phi_ {1 2}}{I _ {2}}. \tag {6.40}
$$

Im Fall der Selbstinduktivität hat man sich also einen Strom in der betrachteten, ge schlossenen Leiterschleife vorzugeben und dann den Fluss zu bestimmen, der genau eine Fläche durchsetzt, die die Leiterschleife aufspannt. Im Fall der Gegeninduktivität gibt man sich einen Strom in einer der beiden Leiterschleifen vor und berechnet den Fluss, der von der zweiten Leiterschleife umfasst wird. Hat man es nicht mit der Windungszahl eins zu tun, sondern mit N bzw. $N _ { 1 }$ und $N _ { 2 } ,$ , so kann man zunächst – wie beschrieben – mit der Windungszahl eins rechnen und nachträglich die Windungszahlen gemäß den Gln. (6.21) und (6.31) ergänzen. Voraussetzung ist dabei, dass alle Windungen einer Wicklung den gleichen Fluss umfassen.

Die hier beschriebene Vorgehensweise führt nicht zum Erfolg, wenn man den Fluss nicht eindeutig der Leiterschleife zuordnen kann, die ihn umfasst. Dann geht man von den Gln. (6.32) bzw. (6.37) aus und hat z. B. für die Selbstinduktivität

$$
L = \frac {2 W _ {\mathrm{m}}}{I ^ {2}}. \tag {6.41}
$$

Man nimmt also einen bestimmten Strom an, ermittelt mit einer der in Abschnitt 6.2.1 angegebenen Formeln die zugehörige Feldenergie und bildet den Quotienten gemäß Gl. (6.41). Wir betrachten als erste Anwendung die Doppelleitung nach Bild 5.4. Da der magnetische Fluss in Beispiel 5.7 schon bestimmt wurde, liefert Gl. (6.39) sofort für die Induktivität pro Länge:

$$
\frac {L}{l} = L ^ {\prime} = \frac {\mu_ {0}}{\pi} \ln \frac {d}{\varrho_ {0}}. \tag {6.42}
$$

Als zweites Beispiel soll ein Koaxialkabel nach Bild 6.19 behandelt und dabei die Gl. (6.41) angewendet werden. Die gesamte magnetische Energie besteht aus drei Anteilen: der im Innenleiter, im Luftraum und im Außenleiter gespeicherten Energie.

Für den Innenleiter erhält man mit dem aus Beispiel 5.5 bekannten H und Gl. (6.16):

$$
\begin{array}{l} W _ {1} = \frac {1}{2} \mu_ {1} \int H ^ {2} \mathrm{d} V \quad \text { mit } \quad \mathrm{d} V = 2 \pi \varrho \cdot \mathrm{d} \varrho \cdot l, \\ W _ {1} = \frac {I ^ {2} \mu_ {1} l}{2 \cdot 2 \pi \varrho_ {1} ^ {4}} \int_ {0} ^ {\varrho_ {1}} \varrho^ {3} \mathrm{d} \varrho = \frac {\mu_ {1} I ^ {2} l}{1 6 \pi}. \\ \end{array}
$$

Demnach ist wegen Gl. (6.41):

$$
L _ {1} ^ {\prime} = \frac {\mu_ {1}}{8 \pi}.
$$

Für den Luftraum zwischen Außen- und Innenleiter ergibt sich auf gleiche Weise mit dem nach Gl. (5.11) bekannten H:

$$
W _ {2} = \frac {I ^ {2} \mu_ {2} l}{2 \cdot 2 \pi} \int_ {\varrho_ {1}} ^ {\varrho_ {2}} \frac {\mathrm{d} \varrho}{\varrho} = \frac {I ^ {2} \mu_ {2} l}{2 \cdot 2 \pi} \ln \frac {\varrho_ {2}}{\varrho_ {1}}.
$$

Damit folgt

$$
L _ {2} ^ {\prime} = \frac {\mu_ {2}}{2 \pi} \ln \frac {\varrho_ {2}}{\varrho_ {1}}. \tag {6.43}
$$

Auf die Bestimmung von $L _ { 3 } ^ { \prime }$ wird hier verzichtet.

Die dem Luftraum zugeordnete Induktivität kann man auch über den Fluss ausrechnen:

$$
\begin{array}{l} \Phi_ {2} = \mu_ {2} \int_ {A} H \mathrm{d} A \quad \text {mit} \quad \mathrm{d} A = l \mathrm{d} \varrho , \\ \Phi_ {2} = \frac {\mu_ {2} I l}{2 \pi} \int_ {\varrho_ {1}} ^ {\varrho_ {2}} \frac {\mathrm{d} \varrho}{\varrho} = \frac {\mu_ {2} I l}{2 \pi} \ln \frac {\varrho_ {2}}{\varrho_ {1}}. \\ \end{array}
$$

Mit $L ^ { \prime } = \varPhi / ( I \cdot l )$ entsteht daraus das bereits vorliegende Ergebnis für $L _ { 2 } ^ { \prime }$

![](images/page_268_image_14.jpg)

<details>
<summary>text_image</summary>

dρ
ρ
I ⊗ μ₁
μ₂ = μ₀
μ₃
dV = 2πρ · dρ · l
</details>

Abb. 6.19: Koaxialkabel: Selbstinduktivität.

**Anmerkung** Bei einem Vergleich von Gl. (3.35) mit Gl. (6.43) und von Gl. (3.38) mit Gl. (6.42) fällt auf, dass jeweils die Ausdrücke im Nenner mit denen im Zähler übereinstimmen. Damit folgt für das Produkt aus $C ^ { \prime }$ und $L ^ { \prime }$ das bemerkenswerte Ergebnis

$$
C ^ {\prime} L ^ {\prime} = \varepsilon \mu ,
$$

das auch für beliebige Leitungsanordnungen gültig ist. Das kann hier jedoch nicht bewiesen werden.

Zum Schluss soll die Gegeninduktivität zwischen den in Bild 6.20 skizzierten Doppelleitungen bestimmt werden. Zuerst ermittelt man den Beitrag $\phi _ { 2 a }$ des stromdurchflossenen Leiters a zum Gesamtfluss, wobei über die im Bild mit A bezeichnete Fläche zwischen $\varrho _ { a c }$ und $\varrho _ { a d }$ integriert wird. Damit ist die gleiche Rechnung durchzuführen wie in Beispiel 5.7 und man erhält für den auf die Länge bezogenen Fluss:

$$
\Phi_ {2 a} ^ {\prime} = \frac {\mu_ {0} I _ {1}}{2 \pi} \ln \frac {\varrho_ {a d}}{\varrho_ {a c}}.
$$

Entsprechend ist der Beitrag von Leiter b

$$
\Phi_ {2 b} ^ {\prime} = \frac {\mu_ {0} I _ {1}}{2 \pi} \ln \frac {\varrho_ {b d}}{\varrho_ {b c}}
$$

und dann der Gesamtfluss $\phi _ { 2 1 }$ (als Differenz der Teilflüsse, da diese die Schleife 2 nicht in gleicher Richtung durchsetzen):

$$
\varPhi_ {2 1} ^ {\prime} = \frac {\mu_ {0} I _ {1}}{2 \pi} \ln \frac {\varrho_ {a d} \varrho_ {b c}}{\varrho_ {a c} \varrho_ {b d}}.
$$

Mit $\varPhi _ { 2 1 } ^ { \prime } = M ^ { \prime } i _ { 1 }$ – analog zu Gl. (6.24) – wird

$$
M ^ {\prime} = \frac {\mu_ {0}}{2 \pi} \ln \frac {\varrho_ {a d} \varrho_ {b c}}{\varrho_ {a c} \varrho_ {b d}}. \tag {6.44}
$$

Selbstinduktivitäten und im Allgemeinen auch Gegeninduktivitäten werden als positive Größen angesehen. Das ergibt sich bei der Herleitung zwangsweise, wenn man die Zählrichtungen des Flusses (Φ bzw. $\phi _ { 2 1 } )$ und des zugehörigen Stromes (I bzw. $I _ { 1 } )$ einander im Sinne der Rechtsschraubenregel zuordnet. Ist diese Zuordnung für bestimmte Zahlenwerte in der eben hergeleiteten Gleichung nicht gegeben, so erhält man für M einen negativen Zahlenwert.

![](images/page_269_image_14.jpg)

<details>
<summary>text_image</summary>

I₁ a
ρₐₐ
c
Φ₂ₐ
ρₐₐ
b
ρbc
A
d
ρbd
a,b ≡ Schleife 1
c,d ≡ Schleife 2
</details>

Abb. 6.20: Zwei Doppelleitungen: Gegeninduktivität.

## 6.4 Magnetische Feldkräfte

## 6.4.1 Die Berechnung von Kräften über die Energie

Es sollen jetzt Kräfte mit Hilfe des Prinzips der virtuellen Verschiebung bestimmt werden. Man geht ähnlich vor wie in Abschnitt 3.8.2 und geht von der Anordnung nach Bild 6.21 aus. Vorausgesetzt wird, dass die Stromquelle einen konstanten Strom I liefert, die Leitungen widerstandsfrei sind, der rechts dargestellte senkrechte Leiterstab sich in x-Richtung reibungsfrei bewegen kann und schließlich der Übergangswiderstand zwischen dem Leiterstab und den waagerecht angeordneten Leiterschienen verschwin dend klein sei.

Energie kommt in der skizzierten Anordnung in drei Formen vor: als magnetische Feldenergie $W _ { \mathrm { m } }$ , als mechanische Energie $W _ { \mathrm { m e c h } }$ , dargestellt durch die potentielle Energie des Gewichts $G ,$ und als elektrische Energie der Stromquelle $W _ { \mathrm { e } }$ . Lässt man eine Verschiebung des Leiterstabes um dx nach rechts zu, wobei die Bewegung langsam erfolgen soll, so ändert sich die Gesamtenergie des Systems nicht:

$$
\mathrm{d} W _ {\mathrm{ges}} = \mathrm{d} (W _ {\mathrm{e}} + W _ {\mathrm{mech}} + W _ {\mathrm{m}}) = \mathrm{d} W _ {\mathrm{e}} + \mathrm{d} W _ {\mathrm{mech}} + \mathrm{d} W _ {\mathrm{m}} = 0.
$$

Mit der in Bild 6.21 festgelegten Zählrichtung für x ergibt sich eine Zunahme der mechanischen Energie:

$$
\mathrm{d} W _ {\text {mech}} = F _ {x} \mathrm{d} x.
$$

![](images/page_270_image_10.jpg)

<details>
<summary>text_image</summary>

I = konst
Umlauf
B
Fx
x
dx
dx
G = Fx
u
</details>

Abb. 6.21: Zur Herleitung der Kraft mit Hilfe des Prinzips der virtuellen Verschiebung bei I = konst.

Auch die magnetische Energie $1 / _ { 2 } L I ^ { 2 }$ erfährt eine Zunahme

$$
\mathrm{d} W _ {\mathrm{m}} = \frac {1}{2} I ^ {2} \mathrm{d} L,
$$

da die Induktivität der Schleife sich vergrößert. I ist nach Voraussetzung konstant. Mit den hier eingeführten Richtungen von u und I muss die Energieänderung der Stromquelle als Abnahme aufgefasst werden, also wird (im Verbraucherzählpfeilsystem)

$$
\mathrm{d} W _ {\mathrm{e}} = - u I \mathrm{d} t.
$$

Wendet man jetzt das Induktionsgesetz auf einen Umlauf im Uhrzeigersinn an, so folgt bei Beachtung der Rechtsschraubenregel

$$
- u = - \frac {\mathrm{d} \varPhi}{\mathrm{d} t}
$$

oder mit $\varPhi = L I ;$

$$
u = I \frac {\mathrm{d} L}{\mathrm{d} t}.
$$

Die Abnahme der elektrischen Energie wird also

$$
\mathrm{d} W _ {\mathrm{e}} = - I ^ {2} \mathrm{d} L.
$$

Die Summe der drei als Zunahmen definierten Energieänderungen ergibt dann

$$
F _ {x} \mathrm{d} x + \frac {1}{2} I ^ {2} \mathrm{d} L - I ^ {2} \mathrm{d} L = 0
$$

oder

$$
F _ {x} = \frac {1}{2} I ^ {2} \frac {\mathrm{d} L}{\mathrm{d} x}.
$$

Setzen wir für $1 / _ { 2 } I ^ { 2 }$ dL wieder d $W _ { \mathrm { m } }$ , so lautet die Endformel

$$
F _ {x} = \frac {\mathrm{d} W _ {\mathrm{m}} ^ {(I)}}{\mathrm{d} x}. \tag {6.45}
$$

Der hochgestellte Index (I) soll darauf hinweisen, dass bei der Herleitung der Formel ein konstanter Strom vorausgesetzt wurde.

## Beispiel 6.4: Kraft auf Traverse eines Schalters.

Die beiden Leiter einer nach links sehr langen Doppelleitung sind durch den in Bild 6.22 schraffiert dargestellten Leiter, bei dem es sich $z , B ,$ um die Traverse eines Schalters handeln kann, leitend miteinander verbunden. Welche Kraft wirkt auf die Traverse? (Voraussetzung: $\varrho _ { 0 } \ll d )$

## Lösung:

Die Kraft soll mit Gl. (6.45) berechnet werden:

$$
F _ {x} = \frac {\mathrm{d} W _ {\mathrm{m}} ^ {(I)}}{\mathrm{d} x} = \frac {\mathrm{d}}{\mathrm{d} x} \left(\frac {1}{2} L I ^ {2}\right) = \frac {1}{2} I ^ {2} \frac {\mathrm{d} L (x)}{\mathrm{d} x}.
$$

![](images/page_272_image_2.jpg)

Abb. 6.22: Kraft auf Traverse eines Schalters.

Für L(x) setzen wir

$$
L (x) = L ^ {\prime} \cdot x + K,
$$

wobei $L ^ { \prime }$ der für die Doppelleitung hergeleitete Ausdruck nach Gl. (6.42) ist und K einen nicht von x abhängigen Korrekturterm bedeutet, der das Randfeld am rechten Leiterende erfasst. Damit ergibt sich

$$
F _ {x} = \frac {1}{2} I ^ {2} L ^ {\prime} = \frac {\mu I ^ {2}}{2 \pi} \ln \frac {d}{\varrho_ {0}}.
$$

## 6.4.2 Kräfte bei Elektromagneten

Betrachtet wird der in Bild 6.23 dargestellte magnetische Kreis, der als Teil eines Schaltrelais aufgefasst werden kann. Wie in Abschnitt 5.6.2 sollen vorgegeben sein: die Durchflutung $\theta   =   N I _ { \mathrm { i } }$ , die mittlere Länge des Eisenweges $l _ { \mathrm { E } } ,$ die Länge des Luftspalts $l _ { \mathrm { L } }$ und der konstante Querschnitt A. Vernachlässigt wird wieder die Streuung. Somit gilt $B _ { \mathrm { E } } = B _ { \mathrm { L } } = B .$ . Die Kraft soll über die Energieänderung, also mit Gl. (6.45) berechnet werden. Gesucht ist ein Ausdruck für die gesamte magnetische Feldenergie, die hier aus zwei Anteilen besteht: der im Luftspalt und der im Eisen gespeicherten Energie. Mit Gl. (6.16) ergibt sich

$$
W _ {\mathrm{m}} = A l _ {\mathrm{L}} \frac {1}{2} \frac {B ^ {2}}{\mu_ {0}} + A l _ {\mathrm{E}} \frac {1}{2} \frac {B ^ {2}}{\mu_ {\mathrm{E}}} = \frac {(A B) ^ {2}}{2} \left(\frac {l _ {\mathrm{L}}}{\mu_ {0} A} + \frac {l _ {\mathrm{E}}}{\mu_ {\mathrm{E}} A}\right) = \frac {\varPhi^ {2}}{2} \left(\frac {l _ {\mathrm{L}}}{\mu_ {0} A} + \frac {l _ {\mathrm{E}}}{\mu_ {\mathrm{E}} A}\right) = \frac {\varPhi^ {2}}{2} R _ {\mathrm{mges}}.
$$

![](images/page_272_image_11.jpg)

<details>
<summary>text_image</summary>

Θ = NI
Fₓ
lₗ lₗ - x
x
Gelenk
</details>

Abb. 6.23: Elektromagnet; Kraftberechnung.

Hierin ist der Fluss Φ durch die gegebene Größe Θ auszudrücken. Mit dem Ohm’schen Gesetz des magnetischen Kreises gemäß Gl. (5.26) folgt

$$
W _ {\mathrm{m}} = \frac {\Theta^ {2}}{2} \frac {1}{\frac {l _ {\mathrm{L}}}{\mu_ {0} A} + \frac {l _ {\mathrm{E}}}{\mu_ {\mathrm{E}} A}} = \frac {\Theta^ {2}}{2 R _ {\mathrm{mges}}}.
$$

Hierin kann $l _ { \mathrm { L } }$ jetzt als Veränderliche aufgefasst werden. Mit der gewählten Zählrichtung (Bild 6.23) wird $l _ { \mathrm { L } } \to l _ { \mathrm { L } } - x$ und damit wegen Gl. (6.45), wenn $\mu _ { \mathrm { E } }$ als konstant angesehen wird:

$$
F _ {x} = \frac {\Theta^ {2}}{2} \frac {\frac {1}{\mu_ {0} A}}{\left(\frac {l _ {\mathrm{L}} - x}{\mu_ {0} A} + \frac {l _ {\mathrm{E}}}{\mu_ {\mathrm{E}} A}\right) ^ {2}} = \frac {\Theta^ {2}}{2} \frac {- 1}{R _ {\mathrm{mges}} ^ {2}} \frac {\mathrm{d} R _ {\mathrm{mges}}}{\mathrm{d} x}.
$$

Die Kraft für $x = 0$ erhält man mit Gl. (5.26)

$$
F _ {x} = \frac {1}{2} \frac {\Phi^ {2}}{\mu_ {0} A} = \frac {1}{2} \frac {B ^ {2}}{\mu_ {0}} A. \tag {6.46}
$$

Daraus lesen wir für die Kraft pro Fläche ab:

$$
\frac {F _ {x}}{A} = \frac {1}{2} \frac {B ^ {2}}{\mu_ {0}}. \tag {6.47}
$$

Daraus lassen sich noch zwei weitere Ausdrücke (wie bei Gl. (6.16)) herleiten.

## 6.5 Ampère-Maxwell’sches-Durchflutungsgesetz

Das bisher betrachtete Durchflutungsgesetz in der Form von Gl. (5.14) oder (5.15b) ist noch nicht ganz vollständig. Dies soll das folgende Gedankenexperiment zeigen. Betrachtet wird der Aufladevorgang eines Plattenkondensators gemäß Bild 6.24.

Die Platten des Kondensators haben die Fläche A und den Abstand d. Durch diesen Abstand ist der Stromkreis nicht geschlossenen. Dennoch ist ein Stromfluss in den Zuleitungen des Kondensators messbar und das Durchflutungsgesetz nach Gl. (5.14) ergibt ein Magnetfeld um den Leiter

$$
\oint_ {L} \vec {H} \cdot \mathrm{d} \vec {s} = i.
$$

Zwischen den beiden Plattenflächen fließt aber kein elektrischer Strom. Hierfür liefert das Durchflutungsgesetz

$$
\oint_ {L} \vec {H} \cdot \mathrm{d} \vec {s} = 0.
$$

Das magnetische Feld müsste also plötzlich verschwinden, so wie es in Bild 6.24 dargestellt ist. Dies steht aber im Widerspruch zu den experimentellen Erkenntnissen. In aufwändigen Versuchen konnten magnetische Felder zwischen den Platten nachgewiesen werden, die immer dann entstehen, wenn sich durch einen Auflade- oder Entladevorgang eine Ladungsänderung im Kondensator ergibt.

![](images/page_274_image_2.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph LR
  subgraph Left Path
  A["i"] --> B["H"]
  B --> C["H"]
  C --> D["Q+"]
  D --> E["E"]
  E --> F["Q-"]
  F --> G["A"]
  G --> H["i"]
  H --> I["H"]
  I --> J["H"]
  end
  subgraph Right Path
  K["i"] --> L["H"]
  L --> M["H"]
  M --> N["Q-"]
  N --> O["d"]
  O --> P["d"]
  end
```
</details>

Abb. 6.24: Aufladen eines Plattenkondensators; eingetragen sind nur die magnetischen Feldlinien, die sich aufgrund der Durchflutungsgleichung (5.14) ergeben.

**Anmerkung** Das ist nicht der einzige Widerspruch, tatsächlich wird ohne Maxwells Erweiterung auch das Gesetz der Ladungserhaltung verletzt, darauf soll aber an dieser Stelle nicht weiter eingegangen werden.

Den oben genannten Widerspruch gilt es jetzt aufzulösen. Durch den Strom i ändert sich die Ladung auf den Kondensatorplatten. Über die Beziehung $Q = C U$ gilt damit für den Plattenkondensator

$$
i = \frac {\mathrm{d} Q}{\mathrm{d} t} = \frac {\mathrm{d}}{\mathrm{d} t} \left(\varepsilon A \frac {U}{d}\right).
$$

Mit der elektrischen Feldstärke $E = U / _ { d }$ wird

$$
i = \frac {\mathrm{d} Q}{\mathrm{d} t} = \varepsilon A \frac {\mathrm{d} E}{\mathrm{d} t}. \tag {6.48}
$$

Das heißt, die zeitliche $\ddot { \mathbf { A } }$ nderung des elektrischen Feldes entspricht in ihrer Wirkung einem »fiktiven Stromfluss« zwischen den Platten. Diesen fiktiven Strom hat Maxwell als Verschiebungsstrom $i _ { \mathrm { V } }$ bezeichnet und damit das bisherige Durchflutungsgesetz ergänzt

$$
\oint_ {L} \vec {H} \cdot \mathrm{d} \vec {s} = i + i _ {\mathrm{V}}. \tag {6.49}
$$

Seine Interpretation dieses Zusammenhangs ist: Der Strom fließt in den Zuleitungen und in den Kondensatorplatten als Leitungsstrom i und zwischen den Platten als Verschiebungsstrom $i _ { \mathrm { V } }$ . Der Verschiebungsstrom bewirkt genauso wie der Leitungsstrom ein magnetisches Feld, so wie es in Bild 6.25 dargestellt ist. Der am Anfang dieses Abschnitts genannte Widerspruch ist somit behoben.

Verallgemeinert lässt sich Gleichung (6.48) unter Verwendung der vektoriellen Feldgrößen schreiben als

$$
\vec {j} _ {\mathrm{V}} = \varepsilon \frac {\partial \vec {E}}{\partial t} = \frac {\partial \vec {D}}{\partial t}. \tag {6.50}
$$

![](images/page_275_image_2.jpg)

<details>
<summary>flowchart</summary>

This diagram illustrates a signal processing system with two parallel waveforms (Q+ and Q-) and their corresponding transfer functions, showing the flow of energy through filters and filtering.
</details>

Abb. 6.25: Verschiebungsstromdichte und magnetisches Feld beim Auf- oder Entladevorgang eines Plattenkondensators.

Die zeitliche Ableitung wird als partielle Ableitung gekennzeichnet, da im allgemeinen Fall das elektrische Feld noch von den Ortskoordinaten abhängen kann. Maxwell nannte die Dichte des Verschiebungsstroms **Verschiebungsstromdichte**. Ergänzt man nun das bisherige Durchflutungsgesetz (5.15b) durch die Verschiebungsstromdichte erhält man

$$
\oint_ {\partial A} \vec {H} \cdot \mathrm{d} \vec {s} = \int_ {A} \left(\vec {J} + \frac {\partial \vec {D}}{\partial t}\right) \cdot \mathrm{d} \vec {A}. \tag {6.51}
$$

In dieser erweiterten Form ist das Durchflutungsgesetz Teil der Maxwell’schen Gleichungen und wird **Ampère-Maxwell’sches Durchflutungsgesetz** genannt.

## 6.6 Das System der Maxwell’schen Gleichungen

Die bisher vorgestellten Gleichungen (3.20), (5.21), (6.7) und (6.51) bilden das System der Maxwell’schen Gleichungen in der Integralform ab. Die Maxwell’schen Gleichungen lassen sich allerdings auch in ihrer Differenzialform darstellen.

Integral- und Differenzialformen der Maxwell’schen Gleichungen sind äquivalent. Die Integralformen sind häufig einfacher interpretierbar und eignen sich daher für das Verständnis und die Herleitung der Maxwell’schen Gleichungen in der Lehre. Für die Beschreibung und Lösung komplexer Probleme, insbesondere mittels numerischer Feldberechnungen, ist in der Regel aber die Differenzialform besser geeignet.

Für die Schreibweise in Differenzialform wird in der Regel der Nabla-Operator verwendet. Der Nabla-Operator ist ein Vektor-Differenzialoperator, dessen Anwendung auf eine Feldgröße partiell Ableitungen nach den Orts-Koordinaten durchführt. In kartesischen Koordinaten ist der Nabla-Operator definiert durch

$$
\vec {\nabla} = \left(\frac {\partial}{\partial x}, \frac {\partial}{\partial y}, \frac {\partial}{\partial z}\right) ^ {\mathrm{T}} = \vec {e} _ {x} \frac {\partial}{\partial x} + \vec {e} _ {y} \frac {\partial}{\partial y} + \vec {e} _ {z} \frac {\partial}{\partial z}. \tag {6.52}
$$

Neben der Schreibweise mit dem Nabla-Operator gibt es die Bezeichnungen **grad**, **div** und **rot**. Sie geben an, in welcher Form der Nabla-Operator wirkt; ob dieser einen Gradienten oder eine Divergenz bildet, oder eine Rotation mit einem Vektorfeld ausführt. Zum Beispiel entsprechen

$$
\vec {\nabla} \phi := \operatorname{grad} \phi , \quad \vec {\nabla} \cdot \vec {D} := \operatorname{div} \vec {D} \quad \text {und} \quad \vec {\nabla} \times \vec {E} := \operatorname{rot} \vec {E}.
$$

Mit Hilfe von mathematischen Sätzen (Integralsätze von Gauß, Green und Stokes) und Methoden der Vektor-Differenzialrechnung können die integralen Formen in ihre jeweilige differenzielle Form überführt werden. Auf eine explizite Herleitung wird hier jedoch verzichtet.

Maxwell’sche Gleichungen in Integral- und Differenzialform:

$$
\oint_ {\partial A} \vec {E} \cdot \mathrm{d} \vec {s} = - \int_ {A} \frac {\partial \vec {B}}{\partial t} \cdot \mathrm{d} \vec {A} \quad \Leftrightarrow \quad \vec {\nabla} \times \vec {E} = - \frac {\partial \vec {B}}{\partial t} \tag {6.53}
$$

$$
\oint_ {\partial A} \vec {H} \cdot \mathrm{d} \vec {s} = \int_ {A} \left(\vec {J} + \frac {\partial \vec {D}}{\partial t}\right) \cdot \mathrm{d} \vec {A} \quad \Leftrightarrow \quad \vec {\nabla} \times \vec {H} = \vec {J} + \frac {\partial \vec {D}}{\partial t} \tag {6.54}
$$

$$
\oint_ {\partial V} \vec {D} \cdot \mathrm{d} \vec {A} = \int_ {V} \rho \mathrm{d} V \quad \Leftrightarrow \quad \vec {\nabla} \cdot \vec {D} = \rho \tag {6.55}
$$

$$
\oint_ {\partial V} \vec {B} \cdot \mathrm{d} \vec {A} = 0 \quad \Leftrightarrow \quad \vec {\nabla} \cdot \vec {B} = 0 \tag {6.56}
$$

Ergänzt werden diese vier Gleichungen durch die drei Materialgleichungen (3.16), (4.5) und (5.12):

$$
\vec {D} = \varepsilon \vec {E}, \quad \vec {J} = \gamma \vec {E}, \quad \vec {B} = \mu \vec {H}.
$$

Wie bereits gesagt, sind die beiden Formen völlig äquivalent. Nur für das Verständnis sind daher im Folgenden die Aussagen der Maxwell’schen Gleichungen nach ihren beiden Formen in Worte gefasst; die physikalische Bedeutung ist aber jeweils identisch.

## Faraday-Maxwell’sches-Induktionsgesetz (6.53)

Die Differenzialform sagt aus, dass ein zeitlich sich änderndes magnetisches Feld ein elektrisches Wirbelfeld hervorruft. Die Integralform ergibt, dass ein zeitlich sich änderndes magnetisches Feld, was durch eine Fläche hindurch tritt, bis auf das negative Vorzeichen in seiner Wirkung identisch ist mit dem elektrischen Feld entlang des Randes dieser Fläche.

## Ampère-Maxwell’sches-Durchflutungsgesetz (6.54)

Die Differenzialform sagt aus, dass die Wirbel des magnetischen Feldes sowohl durch einen elektrischen Strom als auch durch ein zeitlich sich änderndes elektrisches Feld hervorgerufen werden. Die Integralform gibt an, dass ein magnetisches Feld entlang des Randes einer Fläche durch die Leitungs- und Verschiebungsstromdichten hervorgerufen wird, die durch diese Fläche hindurch treten.

## Gauß’sches elektrisches Gesetz (6.55)

Die Differenzialform besagt, dass die elektrischen Ladungen die Quellen und Senken des elektrischen Feldes sind. Die Integralform liefert die Aussage, dass der elektrische Fluss durch die geschlossene Oberfläche eines Volumens gleich der Ladung ist, die von diesem Volumen eingeschlossen wird.

## Gauß’sches magnetisches Gesetz (6.56)

Die Differenzialform besagt, dass das magnetische Feld quellenfrei ist. Das bedeutet, dass keine magnetischen Monopole existieren. Die Integralform erläutert, dass sich der gesamte magnetische Fluss, der durch die geschlossene Oberfläche eines Volumens fließt, in seiner Wirkung aufhebt.

## Weiterführende Literatur

## Lehrbücher

[1] W. Ameling. Grundlagen der Elektrotechnik. Band I: 4. Aufl., Band II: 2. Aufl. Braunschweig: Vieweg, 1988/1984.
[2] H. Benzinger und U. Weyh. Die Grundlagen der Gleichstromlehre (Lehrbuch). 3. Aufl. München: Oldenbourg, 1990.
[3] K. J. Binns und P. J. Lawrenson. Analysis and Computation of Electric and Magnetic Field Problems. Oxford: Pergamon Press, 1973.
[4] S. Blume. Theorie elektromagnetischer Felder. 3. Aufl. Heidelberg: Hüthig, 1991.
[5] E. Böhmer. Elemente der angewandten Elektronik. 15. Aufl. Braunschweig: Vieweg, 2007.
[6] G. Bosse. Grundlagen der Elektrotechnik. Band I: Elektrostatisches Feld und Gleichstrom, Band II: Magnetisches Feld und Induktion, Band III: Wechselstromlehre, Vierpol- u. Leitungstheorie, Band IV: Drehstrom, Ausgleichsvorgänge in linearen Netzen. Band I: 3. Aufl., Band II: 4. Aufl., Band III: 3. Aufl., Band IV: 2. Aufl. Berlin: Springer, 1996.
[7] L. O. Chua, C. A. Desoer und E. S. Kuh. Linear and Nonlinear Circuits. New York: McGraw-Hill, 1987.
[8] H. Clausert. Elektrotechnische Grundlagen der Informatik. München: Oldenbourg, 1995.
[9] C. A. Desoer und E. S. Kuh. Basic Circuit Theory. 16th printing Singapore: McGraw-Hill, 1987.
[10] E. Döring. Werkstoffe der Elektrotechnik. 2. Aufl. Braunschweig: Vieweg, 1988.
[11] J. A. Edminister. Elektrische Netzwerke. 2. Aufl. London: McGraw-Hill, 1990.
[12] H. Elschner. Grundlagen der Elektrotechnik/Elektronik. Band 1 + 2. Berlin: Verlag Technik, 1990/91.
[13] H. Fricke und P. Vaske. Elektrische Netzwerke. 17. Aufl. Stuttgart: Teubner, 1982.
[14] H. Frohne, K.-H. Löcherer, H. Müller, Th. Harriehausen, D. Schwarzenau: Moeller Grundlagen der Elektrotechnik. 22. Aufl. Stuttgart: Teubner, 2011.
[15] A. Führer, K. Heidemann und W. Nerreter. Grundgebiete der Elektrotechnik. Band l + 2, 8. Aufl. München: Hanser, 2006.
[16] H. Grafe, J. Loose und H. Kühn. Grundlagen der Elektrotechnik. Band I: Gleichspannungstechnik, Band II: Wechselspannungstechnik. Band I: 13. Aufl., Band II: 9. Aufl. Heidelberg: Hüthig, 1989/1987.
[17] O. Greuel. Mathematische Ergänzungen und Aufgaben für Elektrotechniker. 12. Aufl. München, Wien: Hanser, 1990.
[18] W. H. Hayt and J. A. Buck. Engineering Electromagnetics. 7.ed. Tokyo: McGraw-Hill, 2005.
[19] W. Herzog. Elektrizität und Elektrotechnik, Teil l + 2. Heidelberg: Hüthig, 1979.
[20] W. Hilberg. Grundlagen elektronischer Schaltungen. 2. Aufl. München: Oldenbourg, 1992.
[21] H. Hofmann. Das elektromagnetische Feld. 3. Aufl. Wien: Springer, 1986.
[22] HÜTTE. Die Grundlagen der Ingenieurwissenschaften. H. Czichos (Hrsg.). 34. Aufl. Berlin: Springer, 2012.
[23] K. Küpfmüller, W. Mathis, A. Reibiger. Theoretische Elektrotechnik und Elektronik. 18. Aufl. Berlin: Springer, 2008.
[24] K. Lunze. Einführung in die Elektrotechnik (Lehrbuch). 13. Aufl. Heidelberg: Hüthig, 1991.
[25] R. Paul. Elektrotechnik. Band I: Elektrische Erscheinungen und Felder, Band II: Netzwerke. Band I: 3. Aufl., Band II: 3. Aufl. Berlin: Springer, 1993/94.
[26] E. Philippow. Grundlagen der Elektrotechnik. 10. Aufl. Berlin: Verlag Technik, 2000.
[27] G. Piefke. Feldtheorie, Band I-III. Mannheim: Bibliographisches Institut, 1973–1977.
[28] A. Prechtl. Vorlesungen über die Grundlagen der Elektrotechnik. Band 1 + 2. 2. Aufl. Wien: Springer, 2006/2007.
[29] R. Pregla. Grundlagen der Elektrotechnik. Band I: 4. Aufl., Band II: 3. Aufl. Heidelberg: Hüthig, 1990.
[30] F. Seifert. Elektrotechnik für Informatiker. 2. Aufl. Berlin: Springer, 1991.
[31] K. Simonyi. Kulturgeschichte der Physik. 2. Aufl. Thun: Verlag Harri Deutsch, 1995.
[32] K. Simonyi. Theoretische Elektrotechnik. 10. Aufl. Leipzig: J. A. Barth, 1993.
[33] U. Tietze und Ch. Schenk. Halbleiter-Schaltungstechnik. 13. Aufl. Berlin: Springer, 2010.
[34] R. Unbehauen. Grundlagen der Elektrotechnik. Band l + 2: 5. Aufl. Berlin: Springer, 1999.
[35] P. Vaske. Berechnung von Gleichstromschaltungen. 5. Aufl. Stuttgart: Teubner, 1991.
[36] U. Weyh. Feldlehre. Die Grundlagen der Lehre vom elektrischen und magnetischen Feld (Lehrbuch). 4. Aufl. München: Oldenbourg, 1993.
[37] I. Wolff. Grundlagen und Anwendungen der Maxwellschen Theorie, Band I + II. 2. Aufl. Mannheim: Bibliographisches Institut, 1991/92.
[38] I. Wolff. Grundlagen der Elektrotechnik. Teil 1: Das elektrische und das magnetische Feld. 7. Aufl. Aachen: Verlag Nellissen-Wolff, 2004.

## Aufgabensammlungen und Arbeitsbücher

[39] C. Gierl, K. Golde, O. Haas, S. Paul, C. Spieker. Aufgaben zur Elektrotechnik 2. München: Oldenbourg, 2013.
[40] O. Haas, C. Spieker. Aufgaben zur Elektrotechnik 1. München: Oldenbourg, 2012.
[41] G. Hagmann. Aufgabensammlung zu den Grundlagen der Elektrotechnik. 12. Aufl. Wiesbaden: Aula-Verlag, 2006.
[42] H. Lindner. Elektroaufgaben. Band I: Gleichstrom, Band II: Wechselstrom, Band III: Leitungen, Vierpole, Fourier-Analyse, Laplace-Transformation. Band I: 29. Aufl., Band II: 24. Aufl., Band III: 6. Aufl. München: Hanser, 2010.
[43] K. Lunze. Berechnung elektrischer Stromkreise (Arbeitsbuch). 15. Aufl. Heidelberg: Hüthig, 1990.
[44] K. Lunze und E. Wagner. Einführung in die Elektrotechnik (Arbeitsbuch). 7. Aufl. Heidelberg: Hüthig, 1991.
[45] H. Mattes. Übungskurs Elektrotechnik. Band 1: Felder und Gleichstromnetze, Band 2: Wechselstromrechnung. Berlin: Springer, 1992/94.
[46] G. Wiesemann. Übungen in Grundlagen der Elektrotechnik, Band II: Magnetfeld und Anwendungen des Induktionsgesetzes. 2. Aufl. Berlin: Springer, 1995.
[47] G. Wiesemann und W. Mecklenbräuker. Übungen in Grundlagen der Elektrotechnik, Band I: Elektrostatisches Feld, Gleichstrom und Netzanalyse. 2. Aufl. Berlin: Springer, 1995.

## Handbücher, Normen, Allgemeines

[48] F. A. Brockhaus. Brockhaus Naturwissenschaften und Technik (3 Bände). Mannheim: F. A. Brockhaus, 2002.
[49] K. Budig. Fachwörterbuch Elektrotechnik/Elektronik (Deutsch-Engl./Engl.-Deutsch). 6. Aufl. Berlin: Langenscheidt Fachverlag, 2002.
[50] Hrsg. Bureau International des Poids et Mesures (BIPM). The International System of Units (SI). 9. Aufl. Paris: BIPM 2019. ISBN 978-92-822-2272-0 (Franz. Original).
[51] DIN Deutsches Institut für Normung e.V. Einheiten und Begriffe für physikalische Größen (DIN Taschenbuch 22). 9. Aufl. Berlin: Beuth, 2009.
[52] DUDEN Informatik. Mannheim: Bibliographisches Institut, 2003.
[53] M. Klein. Einführung in die DIN-Normen. 14. Aufl. Stuttgart: Teubner, 2009.
[54] Hrsg. bisher C. Rint; neu hrsgg. v. Lacroix u. Motz u. Paul u. Reuber. Handbuch der Informationstechnik und Elektronik. Heidelberg: Hüthig, 1989.
[55] H. Netz. Formeln der Elektrotechnik und Elektronik. 2. Aufl. München: Hanser, 1991.
[56] E. Philippow. Taschenbuch Elektrotechnik. Band 1: Allgemeine Grundlagen. 3. Aufl. München: Hanser, 1986.
[57] Hrsg. Physikalisch-Technische Bundesanstalt, Nationales Metrologieinstitut. PTB-Infoblatt – Das neue Internationale Einheitensystem (SI). Braunschweig: 2019. https://www.ptb.de/cms/fileadmin/internet/presse\_aktuelles/broschueren/intern\_einheiten-system/Das\_neue\_Internationale\_Einheitensystem.pdf (Zugriff am 19. Dezember 2021).
[58] Hrsg. Physikalisch-Technische Bundesanstalt, Nationales Metrologieinstitut. Die gesetzlichen Einheiten in Deutschland. 2. Aufl. Braunschweig: 2020. https://www.ptb.de/cms/fileadmin/internet/presse\_aktuelles/broschueren/intern\_einheiten-system/Die\_gesetzlichen\_Einheiten.pdf (Zugriff am 19. Dezember 2021).
[59] E. Tiesinga, P. Mohr, D. Newell, B. Taylor. 2018 CODATA Recommended Values of the Fundamental Constants of Physics and Chemistry. Special Publication (NIST SP), National Institute of Standards and Technology, Gaithersburg, MD, [online], 2019. https://tsapps.nist.gov/publication/get\_pdf.cfm?pub\_id=928211 (Accessed December 19, 2021).

## Stichwortverzeichnis

Abgleichbedingung 29

Abhängigkeit

– lineare 80

Addition

– algebraische 155

– vektorielle 154

Äquipotenzialfläche 171, 180, 212

Akkumulator 45, 46

Alkali-Mangan-Element 47

Ampere 2, 221

Amperemeter 31

Amperesekunde 7

Analog-Digital-Wandler 34

Anion 6

anisotrop 162

Anliegerleitwert 76

Anliegerwiderstand 75

Anpassung 60

– Leistungsanpassung 62

– Spannungsanpassung 62

– Stromanpassung 62

– Überanpassung 62

– Unteranpassung 62

Antenne 170

Anzeige

– analoge 32

– digitale 34

Anzeigefehler 33

Arbeit 3

Arbeitsgerade 65, 116

Arbeitspunkt 118

– instabiler 118

– stabiler 119

Atommodell 6

Aufpunkt 166

Ausgangswiderstand 113

Basis 109

Batterie

– Autobatterie 57

– Trockenbatterie 46, 47

Baum 83

– vollständiger 83, 90

Baumzweig 84

Belastungsstrom 48

Bernstein 5

Berührungsspannung 210

Betriebspunkt

– stabil 119

Bewegungsinduktion 242

Bezugsspannung 115

Blei-Sammler 46

Brechungsgesetz

– Elektrostatik 193

– Magnetfeld 230

– Strömungsfeld 212

Brücke

– abgeglichen 29

– unabgeglichen 77

Brückenschaltung 28, 77

Bügel

– stromdurchflossener 207

Bündelfluss 247

CODATA 1

Coulomb 7

Coulomb’sches Gesetz 152, 165, 171

DAU siehe Digital-Analog-Umsetzer

Dauermagnet 237

diamagnetisch 221

Dielektrikum 178

– nicht ideal 207

Dielektrizitätskonstante siehe Permittivität

Dielektrizitätszahl siehe Permittivität

Digital-Analog-Umsetzer 91

Digitalisierung 34

Dimension 5

Diode 62

– Tunneldiode 62

– Z-Diode 63

Dipol 166, 214

– magnetischer 214

Dipolmoment

– elektrisches 167

– magnetisches 214

Divergenz 267

Doppelleitung 180, 258

Drehspulmesswerk 32, 220

Dreieck 73

Dreieck-Stern-Transformation 74

Dreiecksleitwert 76

Dreieckwiderstand 76

Driftgeschwindigkeit 9

Durchflutung 224

Durchflutungsgesetz 223, 224, 232

Eingangs-Offsetspannung 113

Eingangswiderstand 113

– negativer 148

Einheit 1

elektrische Ladung 5, 13

Elektrode 171

Elektrolyt 8, 18

Elektromagnet 263

Elektrometerverstärker 113, 122

Elektromotorische Kraft (EMK) 22

Elektron 6

– Geschwindigkeit 9

Elektronengas 8, 170

Elektronenwolke 8

Elektrostatik 157

Elementarladung 6

Elementarmagnet 221

Emitter 109

Energie 3

– elektrische 13

– kinetische 9

– magnetische 249

– potenzielle 10

Energiedichte

– elektrische 186

– magnetische 251

Erder 210

Erdfeld

– magnetisches 217

Erdübergangswiderstand 211

Erdungsproblem 209

Erregung

– elektrische 162

– magnetische 220, 251

Ersatzinduktivität 257

Ersatzspannungsquelle 51, 91

Ersatzstromquelle 53

Ersatzzweipol 51

Erzeuger 10

Erzeugerspannung 23

Feinstrukturkonstante 162, 221

Feld 151

– elektrisches 155

– elektrostatisches 155, 187

– homogenes 151

– inhomogenes 151

– radialsymmetrisches 168

– wirbelfreies 157

Feldberechnung 179

Feldenergie

– magnetische 261

Feldgröße 151

– skalare 151

– vektorielle 151

Feldkonstante

– elektrische 162

– magnetische 220

Feldkräfte

– magnetische 261

Feldlinie 151

Feldstärke

– elektrische 154

– magnetische 220, 240

– Überlagerung 154

ferromagnetisch 221, 251

Flächenladung 213

Fluss

– elektrischer 163

– magnetischer 229, 241

Flussdichte

– elektrische 162

– magnetische 216

Fremdfeld 154

Fünfeck 83

– vollständiges 83

Gauß’scher Satz der Elektrostatik 164, 191, 230

Gegeninduktivität 254

Gegenkopplung 113, 116

– invertierende 120

– nichtinvertierende 122

Gegenkopplungsfaktor 142, 149

Gegenkopplungsschaltung 113

Gegenkopplungsverhalten 142

Generator

– Drehstrom 46

Generator-Spannung 23

Gesamtleistung 56

Gesetz von Biot-Savart 226

GK siehe Gegenkopplung

Gleichspannung 46

Gleichstrom 7

Gleichtaktverstärkung 113

Glühlampe 62

Gradient 159, 267

Graph 83

Grenzfläche 191, 212

Grenzschicht 230

Größe

– physikalische 1

Gruppenschaltung 27

Größengleichung 4

Halbkugelerder 211

Halbleiter 8, 18

Heißleiter 62

Henry 255

Hüllfläche 163, 204

Hüllkugel 165, 209

Hysterese 128, 222

Hystereseschleife 128, 222

Hystereseverluste 252

Hüllenintegral 164

Induktionsgesetz 241

Induktionskonstante 215

Influenz 170

Innenwiderstand 48, 52, 53, 106

– Messwerk 40

Integral

– wegunabhängig 157

invertierend 116

Ion 6

Isolierstoffe 18

isotrop 161

Kästchenmethode 185

Kaltleiter 62

Kapazität 172

Kation 6

Kirchhoff’sche Gleichung

– erste 19, 78

– zweite 21, 78

Kirchhoff’sches Gesetz siehe Kirchhoff’sche Gleichung

Klassengenauigkeit 33

Klassenzeichen 33

Knoten 19

– Großknoten 20

Knotenanalyse 78, 96, 103, 196

Knotengleichung 19, 79

Knotenleitwert 76, 98

Koaxialkabel 177, 207

Koeffizientenglied

– bipolares 136

Koerzitivfeldstärke 222

Kohle 18

Kohle-Zink-Element 47

Kollektor 109

Komparator 115

– invertierender 115

– nichtinvertierend 116

Kondensator 171

– Aufladung 189

– Brückenschaltung 197

– Energie 187

– Ladungsausgleich 201

– Parallelschaltung 172

– Reihenschaltung 172

– Schaltsymbol 172

Kondensatorschaltungen 194

– Aufladung 194

– Ladungsausgleich 198

Kopplungsleitwert 98

Kopplungswiderstand 86

Kraft 3, 152

– elektrostatisches Feld 187

– magnetisches Feld 240

– stromdurchflossener Leiter 215

Kraftdichte 190

Kreis

– magnetischer 255

Kreuzprodukt 217

Kugelkondensator 176, 213

Kugelschalen

– konzentrische 213

Kurzschlussstrom 48

Ladung 7

– magnetische 215

Ladungsträger 8

Länge 2

Leerlaufspannung 48

Leerlaufverstärkung 113

Leerlaufversuch 48

Legierung 16, 18

Leistung 3, 14

Leistungsanpassung 62

Leistungsdichte 206

Leiter 8, 204

– dünner 180

– stromführender 223

Leiterschleife 219, 241

– rotierende 248

– stromdurchflossene 252

Leitfähigkeit 212

– elektrische 12

Leitungsstrom 265

Leitwert 12, 16

– magnetischer 231, 232

Leitwertmatrix 99

Lenzsche Regel 242

linear 47, 80

Linienintegral 157

Linienladung 167, 191

Linienladungsdichte 167

Magnet 214

Magnetfeld 9

– inhomogen 250

– stationäres 214

– zeitlich änderndes 241

magnetischer Kreis 231, 238

Magnetisierungskennlinie 221

Magnetnadel 216

Masche 78

Maschenstrom 85

Masse 2

Maßsystem

– elektrostatisches 153

Maxwell’sche Gleichungen 266

– Durchflutungsgesetz 264, 266

– Induktionsgesetz 242, 245

Messbereichsendwert 34

Messbereichserweiterung 35, 41

– Spannung 38

– Strom 35

Messgenauigkeit 32, 35

Messinstrument 33

– analoges 32

– digitales 34

Messung

– Gleichstrom 32

– Leistungsbedarf 32

– spannungsrichtig 41

– stromrichtig 41

– Wechselstrom 32

Messwerkwiderstand 32

Messwertkorrektur 41

Metall 8

Mitkopplung 113, 116, 137

– invertierende 118, 123

– nichtinvertierende 116, 126

Mitkopplungsfaktor 142, 149

Mitkopplungsschaltung 128

Mitkopplungsverhalten 142

MK siehe Mitkopplung

MKSA-System 1

Moment

– magnetisches 221

Multimeter 40

Nabla-Operator 266

Negativ-Impedanz-Konverter 148

Netz

– dreimaschig 78

– ebenes 84

– lineares 49, 78

Netzumwandlung 76

Neukurve 221

Neutron 6

NIC siehe Negativ-Impedanz-Konverter

nichtinvertierend 116

Nichtleiter 8

Nickel-Cadmium-Element 47

Nordpol 214

Normalkomponente 191, 230

npn-Transistor 109

Nutzleistung 56

Ohm 12

Ohm’sches Gesetz 15, 49, 78

– magnetischer Kreis 233, 253

Operationsverstärker 108

– idealer 113

– realer 114

– Schaltsymbol 114

– Schaltungen 113

– Verstärkerschaltungen 113

– Verstärkungskennlinie 114

Parallelschaltung 25

paramagnetisch 221

Permeabilität 215, 220

– relative 221

Permeabilitätskonstante 215

Permittivität 153, 162, 191

– relative 162, 163

Plattenkondensator 173

pnp-Transistor 109

Polstärke 214

Potenzialfläche 206

Potenzialfunktion 158, 167

Prinzip der Materialisierung 180

Prinzip der virtuellen Verschiebung 187, 261

Proton 6

Punktladung 165

– im Magnetfeld 219

Quantisierung 34, 35

Quelle

– gesteuerte 106

– ideale 47, 106

– lineare 49

Quellen-Zweipol 51

Quellenfeld 151

Quellenfreiheit 229

Quellengerade 65

Quellenspannung 10, 47

Quellpunkt 166

RC-Schaltung 199

Rechtsschraubenregel 216, 218

Referenzsspannung 115

Reihenschaltung 23, 24

Reinmetalle 17

Remanenz 222

resistance 16

resistor 16

Rotation 267

Rückkopplung 113

– Grundschaltungen 116

– Prinzipien 113, 116

Ruheinduktion 242

Sättigung 222

Schalter 36, 92, 194, 262

Schalthysterese 128

Schaltung

– invertierende 116

– nichtinvertierende 116

– Symmetrie 30

Scherung 236

Scherungsgerade 236

Schmitt-Trigger 128

– invertierender 130

– nichtinvertierender 129

Schrittspannung 210

Selbsthaltung 128

Selbstinduktivitaet 252

SI

– Einheiten 1, 221

– Système International 1

Siemens 12

Skala

– lineare 32

Skalarprodukt 156

Skalenendwert 32

Spannung

– elektrische 10

– induzierte 241

Spannungs-Stabilisierung 67

Spannungsabfall 10

Spannungskorrektur 42

Spannungsmessgerät 31

Spannungsmessung 31

Spannungsquelle 46

– lineare 47

– spannungsgesteuerte 106

– stromgesteuerte 106

Spannungsteiler 25

– -regel 50

– belasteter 50

– unbelasteter 25

Spannungsübertragungsfunktion 120

Spule 32

– stromdurchflossene 232

Steilheit 111

Stern 73

Stern-Dreieck-Transformation 73, 75

Sternschaltung 73

Sternwiderstand 75

Streufeld 232

Strom

– abhängiger 85

– elektrischer 6, 8

– unabhängiger 85

Strom-Spannungs-Kennlinie 62

Stromdichte

– elektrische 203, 228

Stromfluss 9

Stromkorrektur 41

Strommessgerät 31

Strommessung 31

Stromquelle

– spannungsgesteuerte 106

– invertierende 146

– stromgesteuerte 106

Stromrichtung

– konventionelle 7

– technische 7

Stromstärke 2, 6

Stromteiler 27

– -regel 50

Subtrahierer 131

Südpol 214

Superpositionsprinzip 71, 166

Tangentialkomponente 192, 230

Teilfluss 247

Temperatur 2, 15

Temperaturbeiwert 17

Tesla 217

Topologische Grundbegriffe 83

Transistor 109

– Ersatzschaltbild 110

– Kennlinien 111

– Ausgangskennlinienfeld 110

– Eingangskennlinie 110

– Schaltsymbol 110

– Verstärker 111

Tripelpunkt 3

Überlagerungssatz 71, 154

Übersteuerung 121

Übersteuerungsgrenzen 146

Umfangswiderstand 75

Umkehraddierer 131

Umkehrungssatz 257

Umkehrverstärker 117, 120, 133

Umlaufanalyse 78, 85, 87, 103

Umlaufgleichung 21, 80

Umlaufstrom 85

Umlaufwiderstand 86

Unabhängigkeit

– lineare 80

Urkilogramm 2

Verbindungszweig 84

Verbraucher 10

Vergleicher 115

Verschiebungsstrom 265

Verschiebungsstromdichte 266

Verstärkerkennlinie 117

Verstärkerschaltung 106

Vieleckschaltung 73

Vielfach-Instrument 36

Vielfach-Messgerät 36

Viereck 73

– vollständiges 83

Vierer-Stern 73

VKL siehe Verstärkerkennlinie

Vollausschlagsspannung 34

Vollausschlagsstrom 32

vollständiges Differenzial 158

Voltmeter 31

Vorsatzzeichen 3

Wärmemenge 3

Wechselstrom 7

Widerstand 11

– differenzieller 11

– innerer 31, 47

– magnetischer 232

– spezifischer 12

– temperaturabhängiger 17

Widerstandsmatrix 87

Widerstandsmessung 42

Wirbelfeld 151

Wirkungsgrad 56

– Energie 56

– Leistung 56

Zählpfeilsystem 45

– Erzeuger- 45

– Verbraucher- 45

Zeit 2

Zweig 83

Zweigspannung 83

Zweigstrom 83

Zweipol

– Äquivalenz 55

– linearer 44

– nichtlinearer 62

Zylinder 168

Zylinderspule 224