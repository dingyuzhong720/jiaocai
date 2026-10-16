# 13 Der deformierbare feste Körper

原始 PDF 第 137–146 页。

13

Der deformierbare feste Körper

## 13.1 Elastische Verformung. Hookesches Gesetz

Ein Körper heißt elastisch, wenn in ihm bei einer durch äußere Kräfte hervorgerufenen $\ddot { \mathrm { A n } } .$ derung seines Volumens oder seiner Gestalt Reaktionskräfte wachgerufen werden, die diese Änderung rückgängig zu machen suchen. Eine durch eine äußere Kraft bewirkte elastische Verformung (Deformation) des Körpers verschwindet also nach Wegnahme der angreifenden Kraft, sie ist reversibel.

Wird ein an einem Ende festgehaltener Stab (z. B. aus Metall) von gleichförmigem Querschnitt A und der Länge $l _ { 0 }$ durch die Kraft $F$ auf die Länge $l = l _ { 0 } + \Delta l$ elastisch gedehnt (Bild 13.1), dann ist die Längenänderung $\Delta l$ der angreifenden Kraft sowie der Anfangslänge des Stabes direkt und dem Stabquerschnitt indirekt proportional:

$$
\Delta l = \alpha \frac {F l _ {0}}{A} \quad (\alpha \text {Stoffkonstante}). \tag {13.1}
$$

Man bezeichnet die auf die Ausgangslänge $l _ { 0 }$ bezogene Längenänderung

$$
\varepsilon = \frac {\Delta l}{l _ {0}} = \frac {l - l _ {0}}{l _ {0}} \tag {13.2}
$$

als (elastische) **Dehnung**. Sie ist dimensionslos. Die auf den Querschnitt bezogene, senkrecht zur Oberfläche des Körpers angreifende (Zug- oder Druck-)Kraft

$$
\sigma = \frac {F}{A}, \qquad E i n h e i t: [ \sigma ] = 1 \mathrm{N} / \mathrm{m} ^ {2} = 1 \text {Pascal(Pa)}, \tag {13.3}
$$

heißt **Spannung** oder genauer **Normalspannung**. Positive Spannungen werden als Zugspannungen, negative als Druckspannungen definiert. In (13.1) ist α der Dehnungskoeffizient; sein Kehrwert $1 / \alpha = E$ ist der **Elastizitätsmodul**. Dieser hat nach (13.1) die gleiche Einheit wie die Spannung $\sigma .$ . Mit (13.2) und (13.3) wird aus (13.1):

$$
\varepsilon = \alpha \sigma \quad \text {oder} \quad \sigma = E \varepsilon \quad (\text {HOOKESches Gesetz}). \tag {13.4}
$$

## Dehnung und Spannung sind bei elastischen Verformungen einander proportional.

Die elastischen Eigenschaften fester Körper finden ihre Erklärung in den **Bindungskräften**, die die Bausteine (Atome, Ionen, Moleküle) im Kristallgitter zusammenhalten. Diese Kräfte sind elektrostatischer Natur und setzen sich aus einem dem COULOMB-Gesetz (23.26) gehorchenden anziehenden (negativen) Anteil $F _ { 1 }$ und einem abstoßenden (positiven) Anteil $F _ { 2 }$ zusammen. Aus der Überlagerung beider resultiert eine Wechselwirkungskraft $F = F _ { 1 } + F _ { 2 }$ , die als Funktion des gegenseitigen Abstandes r der Gitterbausteine den im Bild 13.2 gezeichneten Verlauf aufweist und durch die Beziehung

$$
F (r) = F _ {1} (r) + F _ {2} (r) = - \frac {a}{r ^ {2}} + \frac {b}{r ^ {n}} \quad (a, b, n \text {Konstanten})
$$

beschrieben werden kann. Bei den Metallen ist $n \approx 3 ,$ bei Ionenkristallen, z. B. NaCl, etwa 9.

---

13.1 Elastische Verformung. Hookesches Gesetz

135

Im Atomabstand $r = r _ { 0 }$ , der sog. Gitterkonstante, halten sich Anziehungs- und Abstoßungskraft das Gleichgewicht, d. h., es ist $F = 0$ . Man erkennt, dass eine durch eine äußere Zugkraft hervorgerufene Dehnung des Gitters (Vergrößerung des Atomabstandes) als Reaktion überwiegende Anziehung, eine durch eine Druckkraft hervorgerufene Annäherung der Atome eine stark anwachsende Abstoßung bewirkt (wegen der zunehmenden Durchdringung der Elektronenhüllen benachbarter Atome).

![](../../raw/pages_0129-0160/images/page_137_image_3.jpg)

<details>
<summary>text_image</summary>

l₀
d₀
d
l
F
</details>

Bild 13.1 Elastische Dehnung eines Stabes unter der Wirkung einer Zugkraft F

![](../../raw/pages_0129-0160/images/page_137_chart_5.jpg)

<details>
<summary>line</summary>

| r | F | F1 |
| --- | --- | --- |
| 0 | >F | 0 |
| r0 | 0 | 0 |
| r | 0 | ~-F1 |
</details>

Bild 13.2 Kraftwirkungen zwischen den Gitterbausteinen als Funktion ihres gegenseitigen Abstandes $r \; ( r _ { 0 }$ Gleichgewichtsabstand $= \mathsf { { , G i t t e r - } }$ konstante“)

Für kleine Deformationen $\varepsilon = \Delta r / r _ { 0 }$ kann die Kraftkurve in der Umgebung der Gleichgewichtslage durch die Tangente angenähert werden, deren (negativer) Anstieg $\mathbf { d } F / \mathbf { d } r$ an der Stelle $r _ { 0 }$ dem Elastizitätsmodul E entspricht. An dem nichtlinearen Verlauf der Kraftkurve erkennt man, dass das HOO-KEsche Gesetz (13.4) nur für kleine Deformationen erfüllt ist; bei größeren Deformationen ergibt sich im Fall einer Druckbeanspruchung ein größerer, bei Zugbeanspruchung ein kleinerer Elastizitätsmodul.

## Beispiele 13.1:

1. Welche Zugspannung σ wäre erforderlich, um einen Stab auf das Doppelte seiner Anfangslänge $l _ { 0 }$ elastisch zu dehnen?

Lösung: Für $l = 2 l _ { 0 }$ wird nach $( 1 3 . 2 ) \; \varepsilon = 1$ , entsprechend einer Dehnung von 100%. Aus (13.4) folgt damit für die zugehörige Spannung $\sigma = E$ . Berücksichtigt man jedoch, dass z. B. für Stahl $E \approx 2 \cdot 1 0 ^ { 1 1 }   \mathrm { P a } = 2 \cdot 1 0 ^ { 5 }$ MPa ist und die Spannung, bis zu der das HOOKEsche Gesetz (13.4) gilt, je nach Stahlsorte z. B. nur 200MPa beträgt, so erkennt man, dass bei diesem Material eine rein elastische Dehnung von maximal nur $\varepsilon = \sigma / E = { 1 0 } ^ { - 3 }$ , entsprechend 0,1%, möglich ist. Bei höheren als zu dieser Dehnung gehörigen Spannungen $( \sigma > E / 1 0 ^ { 3 } )$ tritt plastische Verformung und danach der Bruch ein (vgl. 13.7).

2. Man berechne aus oben stehender Gleichung für die Wechselwirkungskraft $F ( r )$ für Stahl a) den Gleichgewichtsabstand $r _ { 0 }$ (Atomabstand in der kubischen Elementarzelle); b) die maximale Anziehungskraft $F _ { \mathrm { m a x } }$ der Atome, die Kohäsionskraft des Gitters; sie muss überwunden werden, um die Gitterbausteine voneinander zu trennen. Im vorliegenden Fall ist $a =$ $2.8 \cdot 10^{-27}    N  \cdot  m ^2;   b = 8.0 \cdot 10^{-37}    N  \cdot  m ^3;   n = 3$

Lösung: a) Aus $F ( r _ { 0 } ) = 0$ folgt: $r _ { 0 } ^ { n - 2 } = r _ { 0 } = b / a = 2 { , } 9 \cdot 1 0 ^ { - 1 0 }   \mathrm { m } \approx 0 { , } 2 9   \mathrm { n m } .$ b) $F _ { \mathrm { m a x } }$ ist die Kraft im Minimum der Kraftkurve $F ( r )$ von Bild 13.2. Man erhält sie durch Nullsetzen der Ableitung

$$
\frac {\mathrm{d} F (r)}{\mathrm{d} r} = \frac {2 a}{r ^ {3}} - \frac {n b}{r ^ {4}},
$$

---

136

13 Der deformierbare feste Körper

woraus mit $b = r _ { 0 } a ( \mathbf { s } .   \mathbf { o } . )$ zunächst für den zugehörigen Atomabstand folgt $r _ { \mathrm { m a x } } = n b / ( 2 a ) =$ $n r _ { 0 } \approx 8 . 7 \cdot 1 0 ^ { - 1 0 }   \mathrm { m } = 0 . 8 7$ nm. Dies in $F ( r )$ eingesetzt, ergibt:

$$
F (r _ {\mathrm{max}}) = F _ {\mathrm{max}} = - \frac {a}{(n r _ {0}) ^ {2}} \left(1 - \frac {1}{n}\right) \approx - 2, 5 \cdot 1 0 ^ {- 9}   \mathrm{N} = - 2, 5   \mathrm{nN} <   0 \quad (\text {Anziehung}).
$$

3. Berechne aus oben stehender Gleichung für die Gitterkraft $F ( r )$ den Elastizitätsmodul $E$ von Stahl! Konstanten $a , b$ und n wie in Beispiel 13.1/2.

Lösung: Wie oben beschrieben, erhält man E aus dem Anstieg der Tangente d $F ( r ) / \mathbf { d } r$ (s. Beispiel 13.1/2b) an die Kraftkurve $F ( r )$ beim Gleichgewichtsabstand $r = r _ { 0 }$ . Mit $r _ { 0 } = b / a \; ( \mathrm { s . o . } )$ wird

$$
\frac {\mathrm{d} F (r _ {0})}{\mathrm{d} r} = \frac {2 a}{r _ {0} ^ {3}} \left(1 - \frac {n}{2}\right).
$$

Da der E-Modul gemäß Gleichung (13.3) und (13.4) von der Dimension einer Spannung (Kraft F durch Fläche A) ist und auf die Wechselwirkung zweier Atome im kubischen Kristallgitter die Fläche $A = r _ { 0 } ^ { 2 }$ (Würfelfläche der Elementarzelle) entfällt, woraus d $A = 2 r _ { 0 }$ · dr folgt, erhält man

$$
E = \frac {\mathrm{d} F (r _ {0})}{\mathrm{d} A} = \frac {\mathrm{d} F (r _ {0})}{\mathrm{d} r} \frac {\mathrm{d} r}{\mathrm{d} A} = \frac {a}{r _ {0} ^ {4}} \left(1 - \frac {n}{2}\right) \approx 2 \cdot 1 0 ^ {1 1} \mathrm{Pa} = 2 0 0 \mathrm{GPa}.
$$

## 13.2 Querkontraktion. Kompressibilität

Erfahrungsgemäß erleidet der Durchmesser d eines Stabes bei der elastischen Dehnung eine Veränderung; er verringert sich bei Zugbeanspruchung (s. Bild 13.1) und vergrößert sich bei Druck. Durch den Quotienten aus der **Querdehnung** $\varepsilon _ { \mathrm { Q } } = - \Delta d / d _ { 0 } = - ( d - d _ { 0 } ) / d _ { 0 }$ und der Längsdehnung (13.2) wird eine zweite Elastizitätskonstante definiert:

$$
\nu = \frac {\varepsilon_ {\mathrm{Q}}}{\varepsilon} = - \frac {\Delta d}{d _ {0}}: \frac {\Delta l}{l _ {0}} \quad (\text {POISSONScheQuerkontraktionszahl}). \tag {13.5}
$$

Die **Volumenänderung** des (prismatisch angenommenen) Stabes mit dem Anfangsvolumen $V _ { 0 } = d _ { 0 } ^ { 2 } l _ { 0 }$ ist daher bei elastischer Deformation

$$
\begin{array}{l} \Delta V = (d _ {0} + \Delta d) ^ {2} (l _ {0} + \Delta l) - d _ {0} ^ {2} l _ {0} \\ = [ d _ {0} ^ {2} + 2 d _ {0} \Delta d + (\Delta d) ^ {2} ] (l _ {0} + \Delta l) - d _ {0} ^ {2} l _ {0} \\ \approx d _ {0} ^ {2} \Delta l + 2 l _ {0} d _ {0} \Delta d \\ \end{array}
$$

bei Vernachlässigung der kleinen Größen $\Delta d \Delta l$ und $( \Delta d ) ^ { 2 }$ . Für die relative Volumenänderung folgt somit unter Berücksichtigung von (13.2) und (13.5)

$$
\frac {\Delta V}{V _ {0}} = \frac {\Delta V}{d _ {0} ^ {2} l _ {0}} = \frac {\Delta l}{l _ {0}} + 2 \frac {\Delta d}{d _ {0}} = \frac {\Delta l}{l _ {0}} \left(1 + 2 \frac {\Delta d}{d _ {0}}: \frac {\Delta l}{l _ {0}}\right) = \varepsilon (1 - 2 \nu). \tag {13.6}
$$

Mit (13.4) erhält man damit für den sog. einachsigen Spannungszustand (Zugstab)

$$
\frac {\Delta V}{V _ {0}} = \frac {1 - 2 \nu}{E} \sigma . \tag {13.7}
$$

---

13.3 Elastisches Verhalten bei Scherbeanspruchung

137

Wird auf einen Körper ein **allseitiger (hydrostatischer) Druck** $- \sigma = \Delta p$ ausgeübt, so ist die Volumenänderung dreimal so groß, und es gilt somit anstelle von (13.7)

$$
\frac {\Delta V}{V _ {0}} = - \frac {3 (1 - 2 \nu)}{E} \Delta p = - \varkappa \Delta p. \tag {13.8}
$$

Für die auf die Druckzunahme $\Delta p$ bezogene relative Volumenabnahme $- \Delta V / V _ { 0 }$ folgt hieraus

$$
\varkappa = - \frac {1}{V _ {0}} \frac {\Delta V}{\Delta p} = \frac {3 (1 - 2 \nu)}{E} = \frac {1}{K} \quad (\text {Kompressibilität}). \tag {13.9}
$$

Der reziproke Wert $1 / \varkappa = K$ heißt **Kompressionsmodul**. Dieser ist ein Maß für die Volumenelastizität fester und flüssiger Stoffe. Da das Volumen aller Körper durch Druck verkleinert wird $( \Delta V < 0 \mathrm { f i r } \Delta p > 0 )$ , ist stets

$$
\varkappa > 0 \quad \text {und daher nach (13.9)} \quad \nu <   0, 5. \tag {13.10}
$$

Der Wert der Querkontraktionszahl ν liegt also stets zwischen 0 und 0,5 (z. B. Stahl 0,28; Aluminiumlegierungen 0,34).

## Beispiele 13.2:

1. Für welchen Wert der POISSONschen Querkontraktionszahl ν ist bei einer Deformation des Körpers dessen Volumenänderung gleich null?

Lösung: Nach (13.8) verschwindet die sog. Volumendilatation $\Delta V / V _ { 0 }$ für $\nu = 0 . 5$ . Solange sich das Material elastisch verformt, ist jedoch nach (13.10) stets $\nu < 0 { , } 5$ . Der Grenzfall $\nu = 0 , 5$ liegt bei ideal plastischem Materialverhalten vor (vgl. 13.6).

2. Welche Volumenabnahme erfährt ein Würfel aus Aluminium $(E = 74 \mathrm{GPa}; \nu = 0, 34)$ mit 10cm Kantenlänge, wenn man ihn in 1000m Meerestiefe bringt? Je Meter Meerestiefe nimmt der allseitige Druck um 10kPa zu.

Lösung: Mit $V _ { 0 } = 1 0 ^ { - 3 }   \mathrm { m } ^ { 3 } ,   \Delta p = 1 0 ^ { 7 }$ Pa und $\varkappa = 1 , 3 0 \cdot 1 0 ^ { - 1 1 }   \mathrm { P a } ^ { - 1 }$ folgt aus (13.8) und (13.9): $\Delta V = - \varkappa V _ { 0 } \Delta p = - 1 { , } 3 0 \cdot 1 0 ^ { - 7 }   \mathrm { m } ^ { 3 } \approx - ( 5   \mathrm { m m } ) ^ { 3 }$ □

## Aufgabe

**13.1** Ein zylindrischer Zugstab aus Stahl (Durchmesser $d_{0}; E = 206 \mathrm{GPa}; \nu = 0,28$ werde durch eine Zugspannung von 200MPa elastisch gedehnt. Um wie viel Promille verringert sich dadurch der Stabquerschnitt?

## 13.3 Elastisches Verhalten bei Scherbeanspruchung

Durch Kräfte, die tangential zu der Ebene gerichtet sind, an der sie angreifen (sog. Scherungskräfte oder Schubkräfte), wird die Gestalt (nicht aber das Volumen) eines elastisch isotropen Festkörpers geändert. So z. B. erfährt ein Würfel durch sie die in Bild 13.3 gezeigte Deformation, die als **Scherung** bezeichnet wird. Sie ist gegeben durch das Verhältnis $s / l = \tan \gamma \approx \gamma ,$ , also durch den Winkel, um den die senkrechten Kanten des Würfels gedreht werden. Auch sie ist reversibel, sofern die Kräfte ein bestimmtes Maß nicht übersteigen. Die auf die Angriffsfläche A bezogene Tangentialkraft F ist die **Schubspannung**

$$
\tau = \frac {F}{A}; \quad \text {Einheit:} \quad [ \tau ] = 1 \mathrm{N} / \mathrm{m} ^ {2} = 1 \mathrm{Pa}. \tag {13.11}
$$

---

138

13 Der deformierbare feste Körper

Zwischen ihr und der durch sie bewirkten elastischen Scherung γ besteht analog zum HOOKE-schen Gesetz (13.4) bei kleinen Werten von $\gamma$ Proportionalität:

$$
\tau = G \gamma \quad (\text {HOOKEsches Gesetz für Scherbeanspruchung}). \tag {13.12}
$$

![](../../raw/pages_0129-0160/images/page_140_image_4.jpg)

<details>
<summary>text_image</summary>

s
F
l
γ
</details>

Bild 13.3 Elastische Scherung eines Würfels unter der Wirkung einer Tangentialkraft

![](../../raw/pages_0129-0160/images/page_140_image_6.jpg)

<details>
<summary>text_image</summary>

A
A'
Ft
τφ
F
φ
Fn
σφ
</details>

Bild 13.4 Kräfte und Spannungen am Zugstab

Die Materialkonstante G heißt **Schub-, Scher-** oder **Torsionsmodul** und ist ein Maß für die Gestaltelastizität fester Körper. Bei elastisch isotropen festen Körpern lässt sich $G ,$ wie in 13.6 gezeigt wird, durch E und ν ausdrücken.

## 13.4 Der einachsige Spannungszustand

Wir betrachten in einem Stab mit dem Querschnitt A, der durch eine Kraft F bzw. durch die Spannung $\sigma = F / \lrcorner$ A auf Zug beansprucht ist (Bild 13.4), eine zur Zeichenebene senkrechte Flä- che $A ^ { \prime } ,$ deren Normale mit der Richtung der angreifenden Kraft den Winkel $\varphi$ einschließt, und fragen nach den Spannungen, die an dieser Fläche angreifen. Dazu denken wir uns den Teil des Stabes rechts von $A ^ { \prime }$ fortgenommen und die Wirkung dieses Teiles durch eine in Richtung des Stabes nach rechts wirkende Kraft $F$ ersetzt, die auf die Fläche $A ^ { \prime }$ gleichmäßig verteilt ist. $F$ kann nun in eine Komponente $F _ { \mathbf { n } }$ senkrecht und eine Komponente $F _ { \mathbf { t } }$ parallel zur Ebene $A ^ { \prime }$ zerlegt werden. Es ist

$$
F _ {\mathrm{n}} = F \cos \varphi , \quad F _ {\mathrm{t}} = F \sin \varphi . \tag {13.13}
$$

Mit A als der zur Stabachse senkrechten Querschnittsfläche ist die unter dem Winkel $\varphi$ gegenüber A geneigte Schnittfläche $A' = A / \cos \varphi$ . Wir erhalten mit (13.3) für die an der Ebene $A ^ { \prime }$ angreifende Normalspannung $\sigma _ { \varphi }$ und nach (13.11) für die in $A ^ { \prime }$ wirkende Schubspannung $\tau _ { \varphi } \cdot$

$$
\sigma_ {\varphi} = \frac {F _ {\mathrm{n}}}{A ^ {\prime}} = \frac {F}{A} \cos^ {2} \varphi = \sigma \cos^ {2} \varphi \tag {13.14}
$$

$$
\tau_ {\varphi} = \frac {F _ {\mathrm{t}}}{A ^ {\prime}} = \frac {F}{A} \sin \varphi \cos \varphi = \frac {\sigma}{2} \sin 2 \varphi . \tag {13.15}
$$

Die Normalspannung $\sigma _ { \varphi }$ für eine Orientierung der Fläche $A ^ { \prime } ,$ für die keine Schubspannung $\tau _ { \varphi }$ auftritt, bezeichnet man als **Hauptspannung** $\sigma _ { 1 }$ . Mit sin $2 \varphi = 0$ und somit $\varphi = 0$ ergibt sie sich hier zu $\sigma _ { 1 } = F / A = \sigma$ . Für einen allgemeinen dreiachsigen Spannungszustand, wie er sich im Innern eines Körpers bei komplizierter Beanspruchung ausbilden kann, ergeben sich drei

---

13.5 Dreiachsiger Spannungs- und Dehnungszustand

139

zueinander senkrechte Hauptspannungen $\sigma _ { 1 } , \sigma _ { 2 }$ und $\sigma _ { 3 }$ (Bild 13.5). Sie greifen senkrecht an den Flächen eines würfelförmigen Volumenelements an, wobei dieses dann in Bezug auf den Körper so orientiert ist, dass die Schubspannungen τ in den Würfelflächen verschwinden.

## Beispiel 13.3:

Wie groß ist in einem Stab, der durch die Spannung σ auf Zug beansprucht wird, die maximale Schubspannung $\tau _ { \mathrm { m a x } } ,$ und unter welchem Winkel $\varphi$ gegenüber der Zugrichtung wird sie wirksam? Wie groß ist die senkrecht dazu, d. h. auf die unter dem betreffenden Winkel geneigte Ebene wirkende Normalspannung $\sigma _ { \varphi } ?   -   L { \ddot { o } } s u n g ;$ Aus (13.15) folgt, dass die Schubspannung $\tau _ { \varphi }$ für sin $1 2 \varphi = 1$ , d. h. $\varphi = 4 5 ^ { \circ }$ , ihren Maximalwert $\tau _ { \mathrm { m a x } } = \sigma / 2$ annimmt. Nach (13.14) wird damit gleichfalls $\sigma _ { \varphi } = \sigma / 2$ □

## 13.5 Dreiachsiger Spannungs- und Dehnungszustand

Wir betrachten ein würfelförmiges Volumenelement im Innern eines durch äußere Kräfte beanspruchten Bauteils, an dessen Würfelflächen senkrecht zu diesen die Zugspannungen $\sigma _ { 1 } , \sigma _ { 2 } , \sigma _ { 3 }$ (Hauptspannungen) eines dreiachsigen Spannungszustandes angreifen (Bild 13.5). In $\sigma _ { 1 }$ -Richtung erzeugt zum einen $\sigma _ { 1 }$ nach dem HOOKEschen Gesetz (13.4) die Dehnung $( 1 / E ) \sigma _ { 1 }$ (E Elastizitätsmodul), zum anderen bewirken in derselben Richtung die dazu senkrechten Spannungen $\sigma _ { 2 }$ und $\sigma _ { 3 }$ nach (13.5) die Querkontraktionen $- ( \nu / E ) \sigma _ { 2 }$ und $- ( \nu / E ) \sigma _ { 3 }$ (ν Querdehnzahl), womit sich die Gesamtdehnung $\varepsilon _ { 1 }$ in $\sigma_{1} -  Richutung  - und$ entsprechend die Dehnungen $\varepsilon _ { 2 }$ und $\varepsilon _ { 3 }$ in $\sigma _ { 2 } .$ - und $\sigma _ { 3 }$ -Richtung – ergeben zu

$$
\varepsilon_ {1} = \frac {1}{E} [ \sigma_ {1} - \nu (\sigma_ {2} + \sigma_ {3}) ] \tag {13.16a}
$$

$$
\varepsilon_ {2} = \frac {1}{E} [ \sigma_ {2} - \nu (\sigma_ {3} + \sigma_ {1}) ] \tag {13.16b}
$$

$$
\varepsilon_ {3} = \frac {1}{E} [ \sigma_ {3} - \nu (\sigma_ {1} + \sigma_ {2}) ] \tag {13.16c}
$$

(HOOKEsches Gesetz für den dreiachsigen Spannungs- und Dehnungszustand). Zugspannungen und Dehnungen erhalten positives, Druckspannungen und Verkürzungen negatives Vorzeichen.

![](../../raw/pages_0129-0160/images/page_141_image_11.jpg)

<details>
<summary>text_image</summary>

σ₁
σ₂
σ₃
σ₂
σ₁
σ₃
</details>

Bild 13.5 Räumlicher Spannungszustand mit den Hauptspannungen $\sigma _ { 1 } , \sigma _ { 2 } , \sigma _ { 3 }$

## Beispiel 13.4:

Welche Spannung $\sigma _ { 3 }$ muss wie in Bild 13.5 an einem Würfel aus Aluminium $( \nu \approx 1 / 3 )$ angreifen, wenn an diesem gleichzeitig die Zugspannungen $\sigma _ { 1 } = 1 0 0   \mathrm { M P a }$ und $\sigma _ { 2 } = 5 0$ MPa anliegen und die Würfelform erhalten bleiben soll?

---

140

13 Der deformierbare feste Körper

Lösung: $\sigma _ { 3 }$ muss die durch die Zugspannungen $\sigma _ { 1 }$ und $\sigma _ { 2 }$ senkrecht zu ihnen gerichtete Querkontraktion $\varepsilon _ { 3 } = - ( \nu / E ) ( \sigma _ { 1 } + \sigma _ { 2 } )$ , welche eine Formänderung des Würfels bewirken würde, kompensieren, also $\varepsilon _ { 3 } = 0$ , woraus nach (13.16c) folgt $\sigma _ { 3 } = \nu ( \sigma _ { 1 }   +   \sigma _ { 2 } ) = 5 0   \mathrm { M P a } \; ( > 0 , \mathrm { Z u g } )$ . Der ebene Dehnungszustand hat also einen räumlichen Spannungszustand zur Folge. □

## Aufgabe

**13.2** Wie lautet das verallgemeinerte HOOKEsche Gesetz $( 1 3 . 1 6 \mathrm { a , } \mathrm { b , } \mathrm { c } )$ für den zweiachsigen Spannungszustand $( \mathbf { z } , \mathbf { B } .$ in der Ebene eines Bleches), b) für den einachsigen Spannungszustand (z. B. im Zugstab)?

## 13.6 Zusammenhang zwischen Schubmodul, Elastizitätsmodul und poissonscher Querkontraktionszahl

Wir betrachten innerhalb des Zugstabes ein würfelförmiges Volumenelement mit der Kantenlänge 1, dessen in Bild 13.6 gezeichnete Ebenen senkrecht zur Zeichenebene orientiert sind und mit der Zugrichtung BD den Winkel $\varphi = 4 5 ^ { \circ }$ einschließen. Als Folge der wirkenden Schubspannungen $\tau _ { \varphi } ,$ die nach (13.15) in diesem Fall ihren maximalen Wert $\sigma / 2$ annehmen, erhält

![](../../raw/pages_0129-0160/images/page_142_image_7.jpg)

<details>
<summary>text_image</summary>

A
α
B
C
D
</details>

Bild 13.6 Gestaltänderung eines Würfels bei Schubdeformation

der Würfel durch Verlängerung in Richtung des Zuges und durch Verkürzung senkrecht dazu eine rhombische Form. Der vorher rechte Winkel bei B ist in den Winkel $ABC = \alpha$ übergegangen. Nach (13.12) $\tau = G \gamma$ ist die Schubspannung der Winkeländerung γ (s. Bild 13.3) proportional, die hier $\gamma = 9 0 ^ { \circ } - \alpha$ beträgt. Aus Bild 13.6 folgt mit der Dehnung ε in Richtung BD und der Querverkürzung νε in Richtung $A C ;$

$$
\tan {\frac {\alpha}{2}} = \frac {\overline {{A C}}}{\overline {{B D}}} = \frac {1 - \nu \varepsilon}{1 + \varepsilon} \approx 1 - \nu \varepsilon - \varepsilon = 1 - \varepsilon (1 + \nu),
$$

und mit der trigonometrischen Beziehung

$$
\tan (\alpha_ {1} - \alpha_ {2}) = \frac {\tan \alpha_ {1} - \tan \alpha_ {2}}{1 + \tan \alpha_ {1} \tan \alpha_ {2}}
$$

wird

$$
\frac {\gamma}{2} \approx \tan \frac {\gamma}{2} = \tan \left(4 5 ^ {\circ} - \frac {\alpha}{2}\right) = \frac {1 - [ 1 - \varepsilon (1 + \nu) ]}{1 + [ 1 - \varepsilon (1 + \nu) ]} = \frac {\varepsilon (1 + \nu)}{2 - \varepsilon \nu - \varepsilon} \approx \frac {\varepsilon (1 + \nu)}{2},
$$

$$
\gamma_ {4 5 ^ {\circ}} \approx \varepsilon (1 + \nu),
$$

wobei durch den Index $4 5 ^ { \circ }$ angedeutet ist, dass die Scherung entlang einer zur Zugrichtung unter dem Winkel $4 5 ^ { \circ }$ stehenden Ebene erfolgt. Fernerhin ist mit (13.12) und (13.4)

$$
\gamma_ {4 5 ^ {\circ}} = \varepsilon (1 + \nu) = \frac {\tau_ {4 5 ^ {\circ}}}{G} = \frac {\sigma}{2 G} = \frac {E \varepsilon}{2 G},
$$

---

13.7 Plastische Verformung. Spannungs-Dehnungs-Diagramm

141

woraus sich die dritte wichtige elastische Konstante G berechnet zu

$$
G = \frac {E}{2 (1 + \nu)} \quad (\text {Schubmodul}). \tag {13.17}
$$

Bei der Herleitung dieser Gleichung wurde davon ausgegangen, dass die elastischen Moduln E, G und ν von der Richtung im Körper unabhängig sind (isotroper Körper). Dies trifft jedoch nicht auf die Kristalle zu, welche elastisch anisotrop sind, weshalb für sie Gleichung (13.17) nicht gilt. Wohl aber kann sie auf die technischen Metalle und Legierungen angewandt werden, welche aus einer Vielzahl mikroskopisch kleiner Kriställchen (Kristallite, Körner) bestehen. Bei diesen sog. polykristallinen Stoffen mittelt sich wegen der statistisch regellosen räumlichen Lage der zahlreichen Kristallite der Anisotropieeffekt praktisch heraus (Quasiisotropie).

## 13.7 Plastische Verformung. Spannungs-Dehnungs-Diagramm

Wird ein Metallstab wie in Bild 13.1 durch eine anwachsende äußere Kraft F auf $\mathtt { Z u g }$ oder Druck belastet und werden die dabei auftretenden Dehnungen $\varepsilon = \Delta l / l _ { 0 }$ in Abhängigkeit von der jeweils wirkenden Spannung $\sigma = F / A$ (A momentaner Stabquerschnitt) grafisch darge-

![](../../raw/pages_0129-0160/images/page_143_chart_7.jpg)

<details>
<summary>line</summary>

| Parameter | Value |
| --- | --- |
| Re | Peak Stress |
| \(\sigma_\)el | Elastic Modulus |
| \(\sigma_1\) | Peak Stress |
| R_m | Ultimate Tensile Strength |
| Bruch | Bruch |
| \(\tan \beta\) | \(\triangle E\) |
</details>

## Bild 13.7 Spannungs-Dehnungs-Diagramm:

(a) wahre (auf die jeweils aktuelle Querschnittsfläche A des Zugstabes bezogene) Spannungs-Dehnungs-Kurve $\sigma = F / A = f ( \varepsilon ) ;$
(b) scheinbare (auf den Ausgangsquerschnitt $A _ { 0 }$ des Zugstabes bezogene) Spannungs-Dehnungs-Kurve $F / A _ { 0 } = g ( \varepsilon ) ;   R _ { \mathrm { e } }$ Streckgrenze, $R _ { \mathrm { m } }$ Zugfestigkeit, E Elastizitätsmodul

stellt, so erhält man das **(wahre) Spannungs-Dehnungs-Diagramm** $\sigma = f ( \varepsilon )$ , welches das Verformungsverhalten eines Materials für eine konstante Temperatur und eine konstante Verformungsgeschwindigkeit bis hin zum Bruch beschreibt (Bild 13.7, Kurvenzug a). Es fällt auf, dass ab einer materialspezifischen Spannung $\sigma = R _ { \mathbf { e } } ,$ der sog. Streckgrenze, deutliche Abweichungen von dem durch das HOOKEsche Gesetz (13.4) $\sigma = E \varepsilon$ beschriebenen linear-elastischen Materialverhalten auftreten. Der Grund dafür ist, dass das Metall in diesem Belastungsbereich zusätzlich zu den elastischen Dehnungen, welche bei Entlastung wieder verschwinden, in zunehmendem Maße größere bleibende, sog. **plastische** Dehnungen erleidet. Man spricht dann von Fließen des Metalls. Diese Eigenschaft wird bei allen technologischen Formgebungsverfahren, wie z. B. Walzen, Pressen und Schmieden, praktisch genutzt.

**Plastizität ist die Eigenschaft von Festkörpern, sich unter der Wirkung einer Kraft irreversibel zu verformen und diese Form nach der Einwirkung beizubehalten.**

---

142

13 Der deformierbare feste Körper

Experimente haben ergeben, dass es berechtigt ist, elastische Dehnung $\varepsilon _ { \mathrm { e l } } = \sigma / E$ und plastische Dehnung $\varepsilon _ { \mathrm { p l } }$ zur Gesamtdehnung $\varepsilon = \varepsilon _ { \mathrm { e l } } + \varepsilon _ { \mathrm { p l } }$ zusammenzufassen. Den bei einer beliebigen Spannung $\sigma _ { 1 }$ vorhandenen plastischen Dehnungsanteil erhält man, indem in Bild 13.7 die zur HOOKEschen Gerade parallele, durch $\sigma _ { 1 }$ gehende Gerade gezeichnet wird, welche bei Entlastung des Stabes von $\sigma _ { 1 }$ auf null durchlaufen würde. Ihr Abszissenabschnitt markiert die Aufteilung der Gesamtdehnung bei $\sigma _ { 1 }$ in elastischen und plastischen Dehnungsanteil. Bei solchen Metallen, bei denen keine so ausgeprägte Streckgrenze $R _ { \mathbf { e } }$ wie in Bild 13.7, sondern ein kontinuierlicher Übergang von der HOOKEschen Geraden zum gekrümmten Kurvenverlauf auftritt, wird als Streckgrenze diejenige Spannung $\sigma _ { 1 }$ definiert, bei der $\varepsilon _ { \mathrm { p l } } = 0 ,$ 2% beträgt (sog. 0,2-Dehngrenze $R _ { \mathrm { p 0 , 2 } } )$

Im **technischen Zugversuch** wird ein Last-Verlängerungs-Diagramm $F = f ( \Delta l )$ von einer genormten Zugprobe aufgenommen, welches der scheinbaren Spannungs-Dehnungs-Kurve (b) in Bild 13.7 $F / A _ { 0 } = g ( \varepsilon )$ mit $A _ { 0 }$ als Ausgangsquerschnitt des Zugstabes entspricht. Der Wert im Kurvenmaximum, d. h. bei der Maximalkraft, wird als **Zugfestigkeit** $R _ { \mathrm { m } }$ bezeichnet. Die wahre Spannungs-Dehnungs-Kurve (a), $\sigma = F / A = f ( \varepsilon )$ , kann nicht unmittelbar aufgezeichnet werden, da sich während der Verformung im plastischen Bereich der Zugstab lokal mehr oder weniger stark einschnürt, wodurch der Stabquerschnitt A an dieser Stelle mit zunehmender Verformung abnimmt und dadurch die Zugspannung $\sigma$ bis zum Bruch stetig ansteigt, während die von der Zugprüfmaschine angezeigte Last F (Kurve (b)) ein Maximum durchläuft und danach wieder abfällt.

**Mikroskopische Erklärung der Plastizität.** Es ist experimentell gesichert, dass die plastische Verformung ohne Volumenänderung erfolgt $( \Delta V = 0 )$ . Hieraus ergibt sich nach (13.9) für plastisches Materialverhalten $\nu = 0 , 5$ . Aus der Volumenkonstanz folgt nach 13.3, dass für die plas tische Verformung, bei der also nur Gestaltänderungen auftreten, allein die Schubspannungen τ verantwortlich sind. In der Tat konnte beim Studium der Vorgänge, die sich im Kristallgitter des Festkörpers bei plastischer Deformation abspielen, nachgewiesen werden, dass der Verformungsprozess in einem **Abgleiten** ganzer Kristallbereiche entlang kristallografisch definierter Ebenen, den Gleitebenen, und ausgewählter kristallografischer Richtungen, den Gleitrichtungen, besteht, wobei das Kristallgitter erhalten bleibt. Dabei spielt für den Gleitmechanismus ein bestimmter Typ von Gitterbaufehlern, die **Versetzung**, eine entscheidende Rolle (TAYLOR, OROWAN, POLANYI, 1934).

![](../../raw/pages_0129-0160/images/page_144_image_5.jpg)

Bild 13.8 Plastische Verformung durch Gleitung: a) Idealkristall (kubisch primitives Gitter); b) Kristall nach Einwanderung einer Stufenversetzung von rechts her; c) ungestörter Endzustand des Kristalls nach Durchlauf der Versetzung durch den Kristall

In Bild 13.8a ist ein perfekt gebauter Kristall ohne irgendwelche Störungen in der regelmäßigen Anordnung der Gitterbausteine, ein sog. Idealkristall, schematisch dargestellt, wobei die Ato-

---

13.8 Härte fester Körper

143

me als Kugeln gezeichnet sind. Ein durch eine sog. Stufenversetzung gestörter Kristall (Realkristall) unterscheidet sich vom Idealkristall dadurch, dass eine Gitterebene im Innern des Kristalls aufhört (Bild 13.8b). Die im Kristall verlaufende Randlinie solch einer „eingeschobenen“ Gitterebene bezeichnet man als **Versetzungslinie**. Diese kann schon durch eine verhältnismäßig niedrige Schubspannung durch das Kristallgitter hindurchbewegt werden, wodurch die zu beiden Seiten der Gleitebene (in der die Versetzungslinie wandert) liegenden Kristallbereiche um genau einen Atomabstand gegeneinander verschoben werden. Ist die Versetzungslinie aus dem Kristall ausgetreten, so ist das Gitter wieder ohne Störung (Bild 13.8c); zurückgeblieben ist aber eine (nur äußerlich wahrnehmbare) Gestaltänderung des Kristalls.

## 13.8 Härte fester Körper

Die Härte gehört zu den praktisch wichtigsten mechanischen Eigenschaften fester Körper. Man versteht unter Härte den Widerstand, den ein Festkörper einem mechanischen Eingriff, z. B. beim Ritzen, Reiben, Schleifen oder Eindrücken eines Probekörpers in die Prüfkörperoberfläche, entgegengesetzt. Physikalisch ist die Härte jedoch nicht eindeutig definierbar, da sie von der jeweiligen Versuchsdurchführung, z. B. Dauer und Geschwindigkeit der Krafteinwirkung, abhängt.

Maßgebend für die Härte eines Materials sind dessen elastisch-plastische bzw. elastisch viskose Eigenschaften, die auch seine Sprödigkeit (Eigenschaft zu brechen, ehe eine merkliche plastische Verformung einsetzt) charakterisieren und von der Fließgrenze (Streckgrenze) und der Bruchgrenze (Zugfestigkeit) des Materials abhängen (s. 13.7, Spannungs-Dehnungs-Diagramm).

Die erste Härteskala, die größere Bedeutung erlangte, basiert auf der Ritzhärte und wurde 1822 von MOHS empirisch aufgestellt. In ihr sind 10 Härtegrade für bestimmte Mineralien festgelegt, von denen sich der Reihe nach jedes Mineral mit dem nächstfolgenden ritzen lässt. Für technische Anwendungen auf Metalle ist die MOHS-Härte nicht geeignet, da die einzelnen Härtestufen zu weit auseinander liegen und untereinander nicht den gleichen Abstand aufweisen. Eine realistischere Bewertung der Härteunterschiede liefert die „absolute Härte“, bei der der Schleifaufwand ermittelt wird.

Die in der Technik am häufigsten angewandten Verfahren beruhen auf der Bestimmung der Eindruckhärte, darunter die BRINELL- und die VICKERS-Härte, bei denen ein Eindrückkörper (gehärtete Stahlkugel bzw. Diamantspitze in Form einer vierseitigen Pyramide) mit einer bestimmten Prüfkraft F während einer festgelegten Einwirkdauer in das zu prüfende Material eingedrückt und die dadurch in der Oberfläche entstehende Eindruckfläche A (Kugel- bzw. Pyramidenkalotte) ausgemessen wird. Der Quotient F/A wird dann als Härte (HB bzw. HV) definiert und ohne Einheit angegeben.

Bei Metallen ist vielfach das Verhältnis zwischen der Zugfestigkeit $R _ { \mathrm { m } }$ und der Eindruckhärte H (nach BRINELL bzw. VICKERS) konstant. Es gilt z. B. für Kohlenstoffstähle $R _ { \mathrm { m } } \approx 0 , 3 6 \cdot H$ und für legierte Stähle $R _ { \mathrm { m } } \approx 0 , 3 4 \cdot H$ . Diese häufig angewandten Beziehungen erlauben eine näherungsweise Bestimmung der Härte aus der Zugfestigkeit bzw. umgekehrt.
