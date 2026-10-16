# 11 Dynamik des starren Körpers

原始 PDF 第 119–130 页。

11

Dynamik des starren Körpers

## 11.1 Bewegung eines frei beweglichen Körpers bei Einwirkung einer Kraft

Greift an einem Körper eine Kraft F an, so lässt sich diese durch ein Drehmoment bezüglich des Schwerpunkts und eine im Schwerpunkt angreifende Einzelkraft ersetzen. Um dies zu zeigen, werden im Schwerpunkt S (Bild 11.1) zwei zu F parallele, entgegengesetzt gleiche Kräfte F und $- \boldsymbol { F } ^ { \prime }$ angefügt, deren Betrag mit dem von F übereinstimmt. An der Gesamtwirkung auf den Körper ändert sich dadurch nichts. F und $- \boldsymbol { F } ^ { \prime }$ bilden zusammen ein Kräftepaar, das nach (10.8) und (10.9) dem Drehmoment $\boldsymbol { M } = \boldsymbol { r } \times \boldsymbol { F }$ vom Betrage M = F l äquivalent ist. Es verbleibt die im Schwerpunkt angreifende Einzelkraft $F ^ { \prime }$ . Daraus folgt, dass die Bewegung eines Körpers durch Überlagerung einer Rotation um den Schwerpunkt und einer Translation beschrieben werden kann.

![](../../raw/pages_0097-0128/images/page_118_image_4.jpg)

<details>
<summary>text_image</summary>

-F'
S
l
r
F'
F'
</details>

Bild 11.1 Umformung einer Einzelkraft in eine im Schwerpunkt angreifende Kraft und ein Kräftepaar

Greifen am Körper mehrere Kräfte $F _ { i }$ an, so kann jede von ihnen analog behandelt werden. Es wirkt dann eine im Schwerpunkt angreifende resultierende Kraft $\boldsymbol { F } = \sum \boldsymbol { F } _ { i } ^ { \prime } = \sum \boldsymbol { F } _ { i }$ und ein Drehmoment $\boldsymbol { M } = \sum \boldsymbol { r } _ { i } \times \boldsymbol { F } _ { i }$ um eine durch den Schwerpunkt gehende Achse.

## 11.2 Kinetische Energie der Drehbewegung. Massenträgheitsmoment

Eine Punktmasse $m ,$ die sich im Abstand r um eine feste Achse A mit gleich bleibender Winkelgeschwindigkeit ω dreht (Bild 11.2), hat die kinetische Energie (Rotationsenergie)

$$
E _ {\mathrm{k}} = \frac {1}{2} m v ^ {2} = \frac {1}{2} m (\omega r) ^ {2} = \frac {1}{2} (m r ^ {2}) \omega^ {2} = \frac {1}{2} J \omega^ {2}. \tag {11.1}
$$

Die darin vorkommende Größe

$$
J = m r ^ {2}, \quad \text {Einheit:} \quad [ J ] = 1 \mathrm{kg} \cdot \mathrm{m} ^ {2} \tag {11.2}
$$

nennt man das **Massenträgheitsmoment** der umlaufenden Punktmasse.

Zur Berechnung des Trägheitsmoments eines starren Körpers denken wir uns diesen in viele kleine Massenelemente $\Delta m _ { i }$ zerlegt, die von der Drehachse A den Abstand $r _ { i }$ haben (Bild

---

11.2 Kinetische Energie der Drehbewegung. Massenträgheitsmoment

117

![](../../raw/pages_0097-0128/images/page_119_image_2.jpg)

<details>
<summary>text_image</summary>

A
r
m
ω
</details>

Bild 11.2 Auf einer Kreisbahn umlaufende Punktmasse

![](../../raw/pages_0097-0128/images/page_119_image_4.jpg)

<details>
<summary>text_image</summary>

A
r_i
Δm_i
</details>

Bild 11.3 Zum Massenträgheitsmoment eines starren Körpers

11.3). J ergibt sich dann als Summe oder – bei Annahme einer kontinuierlichen Massenverteilung mit differenziell kleinen Massenelementen $\mathbf { d } m = \varrho \mathbf { d } V$ (ϱ konstante Massendichte) – als Integral der Trägheitsmomente aller Massenelemente:

$$
J = \sum \Delta m _ {i} r _ {i} ^ {2} \quad \text {bzw.} \quad J = \int r ^ {2} \mathrm{d} m \quad (\text {Massenträgheitsmoment}). \tag {11.3}
$$

Wie aus Gl. (11.1) hervorgeht, spielt das Trägheitsmoment bei der Drehbewegung eines Körpers eine analoge Rolle wie die Masse bei fortschreitender Bewegung. J ist aber außer von der Masse zusätzlich von der Form und den Abmessungen des Körpers sowie von der Massenverteilung im Körper und der Lage der Drehachse abhängig.

## Das Massenträgheitsmoment kennzeichnet den Bewegungswiderstand eines um eine vorgegebene Achse rotierenden Körpers gegenüber einer Änderung der Drehzahl.

Für das **Trägheitsmoment eines Zylinders (Kreisscheibe)** mit homogener Massenverteilung bei Rotation um die Zylinderachse erhält man, wenn als Massenelement ein Hohlzylinder mit dem Innenradius r und der Dicke dr gewählt wird (Bild 11.4), also $\mathrm{d}m = \varrho \mathrm{d}V = 2\pi \varrho h r \mathrm{d}r$ (h Höhe des Zylinders bzw. Dicke der Kreisscheibe), nach Gl. (11.3)

$$
J = 2 \pi \varrho h \int_ {0} ^ {R} r ^ {3} \mathrm{d} r = \frac {\pi}{2} \varrho h R ^ {4} \qquad (R \text {Zylinderradius}).
$$

Da $\pi \varrho R ^ { 2 } h = m$ die Masse des Zylinders ist, folgt $J = ( 1 / 2 )   m R ^ { 2 }$

![](../../raw/pages_0097-0128/images/page_119_image_13.jpg)

<details>
<summary>text_image</summary>

dr
r
h
R
</details>

Bild 11.4 Zur Berechnung des Massenträgheitsmoments eines um seine Symmetrieachse rotierenden Zylinders bzw. Hohlzylinders

Für den **Hohlzylinder** sind in der obigen Rechnung der Innenradius r und der Außenradius R als Integrationsgrenzen zu wählen. Man erhält mit $m = \pi \varrho h ( R ^ { 2 } - r ^ { 2 } )$

$$
J = \frac {\pi}{2} \varrho h (R ^ {4} - r ^ {4}) = \frac {\pi}{2} \varrho h (R ^ {2} + r ^ {2}) (R ^ {2} - r ^ {2}) = \frac {1}{2} m (R ^ {2} + r ^ {2}).
$$

---

118

11 Dynamik des starren Körpers

Bei einem sehr dünnwandigen Hohlzylinder ist $r \approx R$ und somit $J \approx m R ^ { 2 }$

Die Trägheitsmomente bezüglich einer Schwerpunktachse sind für die **Kugel** $J = ( 2 / 5 )   m R ^ { 2 }$ für den Quader $J = ( 1 / 1 2 ) m ( a ^ { 2 } + b ^ { 2 } )$ mit a und b als Kantenlängen senkrecht zur Drehachse, für den **langen dünnen Stab** $J = ( 1 / 1 2 )   m l ^ { 2 }$ (l Stablänge).

## Beispiel 11.1:

Berechne die Endgeschwindigkeit, die ein zylindrischer Körper (Masse $m ,$ Radius R) hat, nachdem er aus der Höhe h auf einer schiefen Ebene herabgerollt ist (Bild 11.5)!

Lösung: Beim Herabrollen wandelt sich seine potenzielle Energie mg h in Bewegungsenergie um, wobei letztere sich aus der kinetischen Energie der Translation $m \nu ^ { 2 } / 2$ und der kinetischen Energie der Rotation um den Schwerpunkt $\bar { J \omega ^ { 2 } / 2 }$ zusammensetzt. Nach dem Energiesatz gilt daher mit $\nu = \omega R$ (Rollbedingung):

$$
m g h = \frac {m v ^ {2}}{2} + \frac {J \omega^ {2}}{2} = \frac {v ^ {2}}{2} \left(m + \frac {J}{R ^ {2}}\right); \quad \nu = \sqrt {\frac {2 g h}{1 + [ J / (m R ^ {2}) ]}}.
$$

Für einen Vollzylinder mit $J = m R ^ { 2 } / 2$ wird $\nu = \sqrt { 4 g h / 3 }$ , für einen sehr dünnwandigen Hohlzylinder mit $J = m R ^ { 2 }$ wird $\nu = { \sqrt { g h } } .$ Der Hohlzylinder rollt also langsamer als der Vollzylinder, obwohl die Masse beider Körper gleich groß ist. Dieses Beispiel zeigt deutlich, dass die Energie der Rotationsbewegung entscheidend von der Massenverteilung im Körper abhängig ist, was in den unterschiedlichen Trägheitsmomenten zum Ausdruck kommt. □

![](../../raw/pages_0097-0128/images/page_120_image_9.jpg)

<details>
<summary>text_image</summary>

R
mg
h
</details>

Bild 11.5 Auf schiefer Ebene herabrollender Zylinder

![](../../raw/pages_0097-0128/images/page_120_image_11.jpg)

<details>
<summary>text_image</summary>

A
s
S
</details>

Bild 11.6 Zum steinerschen Satz

Wenn der Zylinder nicht rollt, sondern reibungsfrei auf der Ebene herabgleitet, entfällt der Rotationsanteil der kinetischen Energie (entsprechend $J = 0$ in ob<u>iger</u> Gleichung), und es ergibt sich die bekannte Endgeschwindigkeit für den freien Fall $\nu = \sqrt { 2 g h }$ , vgl. (3.10).

**Satz von STEINER.** Rotiert ein Körper mit der Winkelgeschwindigkeit ω um eine innerhalb oder außerhalb desselben verlaufende Achse A, die nicht durch den Schwerpunkt S geht (Bild 11.6), so führt einerseits S eine translatorische Bewegung auf einer Kreisbahn mit der Geschwindig keit $v = \omega s$ um A aus (s Abstand zwischen A und S), wobei man sich die gesamte Masse des Körpers in S vereinigt zu denken hat, zum anderen dreht sich der Körper mit der gleichen Winkelgeschwindigkeit um die zu A parallele, durch S gehende Achse. Dementsprechend ergibt sich die kinetische Energie der Bewegung als Summe aus Translations- und Rotationsenergie zu

$$
E _ {\mathrm{k}} = \frac {m v ^ {2}}{2} + \frac {J _ {S} \omega^ {2}}{2} = \frac {1}{2} (m s ^ {2} + J _ {S}) \omega^ {2} = \frac {1}{2} J _ {A} \omega^ {2}.
$$

---

11.3 Arbeit und Leistung bei der Drehbewegung. Grundgesetz der Dynamik

119

Der in Klammern stehende Ausdruck ist das zur Achse A gehörige Trägheitsmoment $J _ { A }$ , während $J _ { S }$ das Trägheitsmoment bezüglich der Schwerpunktachse bezeichnet. Es ist also

$$
J _ {A} = J _ {S} + m s ^ {2} \quad (\text {STEINERScher Satz}). \tag {11.4}
$$

## STEINERscher Satz:

**Das Trägheitsmoment eines Körpers setzt sich additiv zusammen aus dem Trägheitsmoment** $J _ { S }$ **bezüglich der Schwerpunktachse und dem Trägheitsmoment** $\pmb { m s ^ { 2 } }$ **der im Schwerpunkt vereinigt gedachten Gesamtmasse m des Körpers bezüglich der zur Schwerpunktachse parallelen Drehachse im Abstand s (Bild 11.6).**

Ist also $J _ { S }$ bekannt, so kann das Trägheitsmoment in Bezug auf jede andere zur Schwerpunktachse parallele Achse nach diesem Satz berechnet werden.

## Beispiele 11.2:

1. Wie groß ist das Trägheitsmoment einer 2m langen Stange (Masse 4,5kg), wenn sie sich um ihren Endpunkt dreht?

Lösung: Mit $J _ { S } = m l ^ { 2 } / 1 2$ (s. oben) ist nach Gl. (11.4)

$$
J = \frac {m l ^ {2}}{1 2} + m \left(\frac {l}{2}\right) ^ {2} = \frac {m l ^ {2}}{3} = 4 J _ {S} = 6 \mathrm{kg} \cdot \mathrm{m} ^ {2}.
$$

2. Mit welcher Geschwindigkeit trifft der Endpunkt eines ursprünglich senkrecht stehenden Bleistiftes (Länge $l = 1 7   \mathrm { c m } )$ beim Umfallen auf die Tischplatte auf?

Lösung: Gleichsetzen von potenzieller Energie mg l/2 (= Arbeit beim Anheben der im Schwerpunkt vereinigt gedachten Masse des Bleistiftes auf die Höhe des Schwerpunkts l/2) und kinetischer Energie $J { \omega } ^ { 2 } / 2$ mit $J = m l ^ { 2 } / 3$ (s. Beispiel 11.2/1) beim Auftreffen sowie $\omega = \nu / l$ ergibt $\nu = \sqrt { 3 g l } = 2 \mathrm { , } 2$ 4m/s $( \approx 8   \mathrm { k m / h } )$ und mit $\nu = \sqrt { 2 a l }$ für die (Tangential-)Beschleunigung $a = 1 , 5 g = 1 4 , 7 \mathrm { m } / \mathrm { s } ^ { 2 }$ . Diese Werte sind größer als bei einem freien Fall aus der Höhe l und somit die Ursache, weshalb z. B. Schornsteine beim Umfallen auseinanderbrechen können. □

## Aufgabe

**11.1** Löse die im obigen Beispiel 11.1 behandelte Aufgabe des auf der schiefen Ebene herabrollenden Zylinders, indem als Drehachse die auf der schiefen Ebene aufliegende Mantellinie des Zylinders gewählt wird (Anwendung des STEINERschen Satzes))!

## 11.3 Arbeit und Leistung bei der Drehbewegung. Grundgesetz der Dynamik

Bei der Drehbewegung eines Körpers um eine fest mit ihm verbundene Achse wird seine jeweilige Lage durch den Drehwinkel ϕ gegen eine willkürlich gewählte Anfangslage beschrieben, und es haben alle Teilchen des Körpers dieselbe Winkelgeschwindigkeit $\omega = \mathbf { d } \varphi / \mathbf { d } t \equiv { \dot { \varphi } }$ und dieselbe Winkelbeschleunigung $\alpha = \mathbf { d } \omega / \mathbf { d } t \equiv { \dot { \omega } } = { \ddot { \varphi } } .$ . Zurückgelegte Weglänge s, Geschwindigkeit v und Beschleunigung a eines Körperteilchens sind von dessen Abstand r von der Drehachse wie folgt abhängig (vgl. Gleichungen (3.37)):

$$
s = r \varphi ; \quad v = r \omega ; \quad a = r \alpha .
$$

---

120

11 Dynamik des starren Körpers

Die **Arbeit bei der Drehbewegung** berechnet sich mit dem Drehmoment $M = F r \; \mathbf { z } \mathbf { u }$

$$
\mathrm{d} W = F \mathrm{d} s = F r \mathrm{d} \varphi = M \mathrm{d} \varphi ; \quad W = \int M \mathrm{d} \varphi . \tag {11.5}
$$

Aus ihr folgt für die Leistung nach Gl. (7.9)

$$
P = \frac {\mathrm{d} W}{\mathrm{d} t} = M \frac {\mathrm{d} \varphi}{\mathrm{d} t} = M \omega \qquad (\text {Momentanleistung}). \tag {11.6}
$$

Der verrichteten Arbeit W entspricht (bei fehlenden Reibungswiderständen) ein gleich großer Zuwachs an kinetischer Energie (Gl. (11.1)), der – bezogen auf die Zeit – gleich der Leistung (Gl. (11.6)) sein muss:

$$
P = \frac {\mathrm{d} E _ {\mathrm{k}}}{\mathrm{d} t} = \frac {\mathrm{d}}{\mathrm{d} t} \left(\frac {J}{2} \omega^ {2}\right) = J \omega \dot {\omega} = M \omega . \tag {11.7}
$$

Hieraus entnimmt man als Bewegungsgleichung für den rotierenden Körper

$$
M = J \dot {\omega} = J \alpha \quad \begin{array}{l} (\text {Grundgesetz der Dynamik} \\ \text {für die Rotationsbewegung}). \end{array} \tag {11.8}
$$

Bei gleichmäßig beschleunigter Drehbewegung, d. h. bei konstantem Drehmoment M, ist die Winkelbeschleunigung $\alpha = ( \omega   -   \omega _ { 0 } ) /   t$ (ω0 Anfangswinkelgeschwindigkeit) und damit

$$
M = J \frac {\omega - \omega_ {0}}{t}. \tag {11.9}
$$

Der Gl. (11.8) entspricht das Grundgesetz $F = m a$ für die fortschreitende Bewegung. Die vorstehenden Betrachtungen spiegeln die völlige Analogie der Größen und Gesetzmäßigkeiten der Rotationsbewegung zu denen der Translationsbewegung wider.

Die folgende Tabelle 11.1 gibt eine entsprechende Übersicht.

Tabelle 11.1 Analoge Größen für Translations- und Rotationsbewegung

| Translation |  | Rotation |  |
| --- | --- | --- | --- |
| Weg | s | Drehwinkel | $\varphi$ |
| Geschwindigkeit | $v = \dot{s}$ | Winkelgeschwindigkeit | $\omega = \dot{\varphi}$ |
| Beschleunigung | $a = \dot{v} = \ddot{s}$ | Winkelbeschleunigung | $\alpha = \dot{\omega} = \ddot{\varphi}$ |
| Masse | m | Trägheitsmoment | J |
| Impuls | $p = mv$ | Drehimpuls | $L = J\omega$ |
| Kraft | $F = ma$ | Drehmoment | $M = J\alpha$ |
| $Arbeit^1$ | $W = Fs$ | $Arbeit^1$ | $W = M\varphi$ |
| $Leistung^1$ | $P = Fv$ | $Leistung^1$ | $P = M\omega$ |
| kinetische Energie | $E_k = \frac{m}{2}v^2$ | Rotationsenergie | $E_k = \frac{J}{2}\omega^2$ |

1 Die angegebenen Beziehungen gelten nur für einen ganz speziellen Fall (vgl. 7.1 und 7.2).

## Beispiele 11.3:

1. Eine Schwungscheibe $(J = 1000   kg  \cdot  m ^2)$ wird durch ein konstantes Drehmoment vom Betrag $M = 2000    N  \cdot  m$ für die Dauer von 20s in Rotation versetzt. Wie groß ist die kinetische

---

11.4 Der Drehimpuls (Drall). Drehimpulserhaltungssatz

121

Energie der Scheibe nach dieser Zeit, und wie groß ist die aufgebrachte Leistung am Ende des Beschleunigungsvorganges?

Lösung: Aus Gl. (11.9) folgt $\omega = M t / J$ und damit aus Gl. (11.1) $E _ { \mathrm { k } } = M ^ { 2 }   t ^ { 2 } / ( 2 J ) = 8   \cdot   1 0 ^ { 5 }   \mathrm { N }   \cdot   \mathrm { m } .$ Die Endleistung ergibt sich mit Gl. (11.7) zu $P = M ^ { 2 } t / J = 8 \cdot 1 0 ^ { 4 }   \mathrm { N } \cdot \mathrm { m } / \mathrm { s } = 8 0   \mathrm { k W } .$

2. Leistungsmessung mit dem PRONYschen Zaum: Wie groß ist die Leistung eines Motors, der bei einer Anpresskraft der Bremsbacken an die Welle von $F = 5 3 0 \mathrm { N }$ eine Drehzahl von $n =$ $9 0 0   \mathrm { m i n } ^ { - 1 }$ hat? Radius der Welle $r = 0,10    m ;$ Reibungszahl $\mu = 0 { , } 4 0$

Lösung: Das durch die Reibungskraft (4.28) hervorgerufene bremsende Drehmoment beträgt $M = F _ { \mathrm { R } } r = \mu F r . \mathrm { M i t }   \omega = 2 \pi n   ( n = 1 5   \mathrm { s } ^ { - 1 } )$ folgt aus Gl. (11.7) $P = 2 \pi \mu F r n \approx 2   \mathrm { k W } .$ □

## 11.4 Der Drehimpuls (Drall). Drehimpulserhaltungssatz

Die Bewegungsgleichung (Gl. (11.8)) für die Drehbewegung eines starren Körpers lautet für ein konstantes Trägheitsmoment J in vektorieller Form

$$
\boldsymbol {M} = J \frac {\mathrm{d} \boldsymbol {\omega}}{\mathrm{d} t} = \frac {\mathrm{d} (J \boldsymbol {\omega})}{\mathrm{d} t} = \frac {\mathrm{d} \boldsymbol {L}}{\mathrm{d} t} \quad (\text {Grundgesetz der Drehbewegung}) \tag {11.10}
$$

in Analogie zum 2. NEWTONschen Axiom (4.9) $\boldsymbol { F } = \mathrm { d } \boldsymbol { p } / \mathrm { d } t$ . Die hier eingeführte vektorielle Grö- ße

$$
\boldsymbol {L} = J \omega , \quad \text {Einheit:} \quad [ L ] = 1 \mathrm{N} \cdot \mathrm{m} \cdot \mathrm{s} \tag {11.11}
$$

heißt **Drehimpuls** oder **Drall**. Der Drehimpuls L ist – wie das Drehmoment M (vgl. Bild 10.3) – ein axialer Vektor, dessen Richtung mit der des Vektors der Winkelgeschwindigkeit ω übereinstimmt (Rechtsschraube, vgl. Bild 3.12). Im Gegensatz zu den sog. freien Vektoren, die beliebig parallelverschoben werden können, ist ein axialer Vektor immer an die Drehachse gebunden.

Das Grundgesetz der Drehbewegung (Gl. (11.10)) sagt aus:

**Die zeitliche Änderung des Drehimpulses eines um eine feste Achse drehbaren Körpers ist gleich dem Gesamtdrehmoment aller am Körper angreifenden äußeren Kräfte.**

Für $M = 0$ ist nach Gl. (11.10) dL/dt = 0, d. h. L = const. Es gilt somit der

**Drehimpulserhaltungssatz: Wirken auf ein rotierendes System von außen keine Drehmomente, so bleibt sein Drehimpuls nach Größe und Richtung konstant.**

Für ein abgeschlossenes System mehrerer Körper gilt analog dem Impulserhaltungssatz (vgl. 9.1), dass der Gesamtdrehimpuls (Vektorsumme aller Einzeldrehimpulse $J _ { i } \omega _ { i } )$ stets konstant bleibt.

**Experimente zum Drehimpulserhaltungssatz:** 1. Einer auf einem Drehschemel sitzenden Versuchsperson (Bild 11.7) werde ein rotierendes Rad (z. B. von einem Fahrrad, dessen Felgen mit Blei beschwert

---

122

11 Dynamik des starren Körpers

sind) übergeben, und zwar so, dass die Drehachse horizontal, also senkrecht zur Achse des Drehschemels steht. Beim Aufrichten des Rades (Parallelstellen der Achsen) beginnt der Schemel im entgegengesetzten Sinn wie das Rad zu rotieren. Umkehr der Radachse um 180◦ bewirkt Umkehr des Drehsinns des Schemels. Erklärung: In dem Maße, wie die Radachse aus der horizontalen Lage gebracht wird, tritt eine Drehimpulskomponente in Richtung der Schemelachse auf. Da der Gesamtdrehimpuls des abgeschlossenen Systems Rad – Versuchsperson, der ursprünglich gleich null war, nicht geändert werden darf, muss die Versuchsperson einen der Richtung nach entgegengesetzten Drehimpuls erhalten.

![](../../raw/pages_0097-0128/images/page_124_image_3.jpg)

<details>
<summary>natural_image</summary>

Two silhouettes showing a person performing seated barbell exercise, one using a lever and the other holding a stick (no text or symbols)
</details>

Bild 11.7 Experiment zur Demonstration des Drehimpulserhaltungssatzes

2. Eine auf dem Drehschemel sitzende Person, welche mit ausgestreckten Armen in jeder Hand eine kleine Hantel hält, werde durch Anstoßen in Drehbewegung versetzt. Beim Anziehen der Arme zur Brust hin vergrößert sich infolge des kleiner werdenden Trägheitsmoments die Winkelgeschwindigkeit der Drehbewegung; das Produkt aus J und ω, der Drehimpuls L, bleibt ungeändert.

Der Drehimpuls ist nicht nur für ausgedehnte Körper definiert, sondern auch für einzelne Teilchen, die sich auf beliebigen gekrümmten Bahnen (z. B. Ellipsen) um ein Drehzentrum bewegen. Für eine Punktmasse m, die sich auf einer Kreisbahn mit konstanter Geschwindigkeit $v = \omega   r$ bewegt, folgt aus Gl. (11.11) mit Gl. (11.2):

$$
L = m r ^ {2} \omega = r m v = r p \tag {11.12}
$$

mit dem Impuls der Punktmasse $p = m v .$ Vektoriell lautet Gl. (11.12):

$$
\boldsymbol {L} = \boldsymbol {r} \times \boldsymbol {p} = m \boldsymbol {r} \times \boldsymbol {v} \quad \begin{array}{l} (\text {Vektor des Bahndrehimpulses} \\ \text {einer Punktmasse}). \end{array} \tag {11.13}
$$

Mit dieser Form des Drehimpulses L lässt sich das 2. KEPLERsche Gesetz, der Flächensatz (s. Abschnitt 8.1), unmittelbar aus dem Drehimpulserhaltungssatz L = const ableiten, indem $| \boldsymbol { L } | / ( 2 m ) = | \boldsymbol { r } \times \boldsymbol { v } | / 2 =$ $| \boldsymbol { r } \times \mathrm { d } \boldsymbol { r } / \mathrm { d } t | / 2 = \mathrm { d } A / \mathrm { d } t$ als „überstrichene Fläche pro $\mathrm { Z e i t ^ { \it { a } } }$ interpretiert wird.

## Beispiele 11.4:

1. Auf einem Drehschemel sitzt – wie in Bild 11.7 – eine Person und hält bei ausgestreckten Armen in jeder Hand, 75cm von der Drehachse des Schemels entfernt, eine Hantel von 2kg Masse. Person und Schemel werden durch einen einmaligen Anstoß so in Drehung versetzt, dass in jeder Sekunde eine halbe Umdrehung stattfindet. Wie ändert sich die Drehzahl, wenn die Person die Hanteln beiderseits um 65cm zur Brust hin anzieht? Trägheitsmoment von Person und Schemel: $J _ { \mathrm { P } } = 1 . 9 5 \mathrm { k g } \cdot \mathrm { m } ^ { 2 } , J _ { \mathrm { S } } = 0 . 2 7 \mathrm { k g } \cdot \mathrm { m } ^ { 2 }$ . Reibung wird vernachlässigt.

Lösung: Mit m als Masse einer Hantel, $r _ { 1 } = 0 , 7 5 \mathrm { m }$ und $r_{2}=0.10  m$ als Entfernungen der Hanteln von der Drehachse in den beiden Positionen der Hanteln ergeben sich die zugehörigen

---

11.5 Kreiselbewegungen. Freie Achsen

123

Gesamt-Trägheitsmomente (Schemel, Person mit Hanteln) zu $J_{1} = J_{\mathrm{P}} + J_{\mathrm{S}} + 2mr_{1}^{2} = 4.47\mathrm{kg} \cdot \mathrm{m}^{2}$ und $J_{2}=J_{\mathrm{P}}+J_{\mathrm{S}}+2mr_{2}^{2}=2,26\mathrm{kg}\cdot\mathrm{m}^{2}$ . Nach dem Drehimpulserhaltungssatz gilt mit Gl. (11.11) $L = J _ { 1 } \omega _ { 1 } = J _ { 2 } \omega _ { 2 } = \mathbf { c o n s t }$ , woraus mit $\omega = 2 \pi n$ für die Drehzahlen folgt: $n _ { 2 } = ( J _ { 1 } / J _ { 2 } ) n _ { 1 } \approx 2 n _ { 1 }$ Die Drehzahl erhöht sich also von anfänglich $n _ { 1 } = 0 { , } 5   \mathrm { s } ^ { - 1 }$ auf $n _ { 2 } = 1   \mathrm { s } ^ { - 1 }$ (Pirouetten-Effekt).

2. Zwei Schwungräder mit den Trägheitsmomenten $J _ { 1 }$ und $J _ { 2 }$ drehen sich gleichsinnig mit den Winkelgeschwindigkeiten $\omega _ { 1 }$ und $\omega _ { 2 }$ . Durch eine Reibkupplung werden sie aneinander angekuppelt. a) Berechne die gemeinsame Winkelgeschwindigkeit ω der Schwungräder nach dem Ankuppeln! b) Wie ändert sich dabei die kinetische Energie des Systems? c) Wie müsste das Verhältnis $\omega _ { 1 } : \omega _ { 2 }$ sein, wenn nach dem Ankuppeln Stillstand eintreten soll? d) Wie groß ist im Fall c) die in Wärme umgewandelte Energie?

## Lösung:

a) Der Vorgang ist ein Analogon zum vollkommen unelastischen Stoß (vgl. 9.2). Es gilt der Drehimpulserhaltungssatz, d. h., es ist mit Gl. (11.11) $J _ { 1 } \omega _ { 1 } + J _ { 2 } \omega _ { 2 } = ( J _ { 1 } + J _ { 2 } ) \omega$ , woraus sich ω berechnet.
b) Die Änderung der kinetischen Energie erhält man durch formale Übertragung der Gleichung (9.12) (mit $\varepsilon = 0 )$ auf den hier vorliegenden unelastischen „Drehstoß“ zu

$$
\Delta E _ {\mathrm{rot}} = \frac {J _ {1} J _ {2}}{2 (J _ {1} + J _ {2})} (\omega_ {1} - \omega_ {2}) ^ {2}.
$$

c) Für $\omega = 0$ folgt aus a) $\omega _ { 1 } : \omega _ { 2 } = - ( J _ { 2 } : J _ { 1 } )$ mit $\omega _ { 2 } < 0$ , d. h. gegensinnige Rotation. d) Die gesamte ursprünglich vorhandene Rotationsenergie wird in Wärme umgewandelt. Die erzeugte Wärmemenge beträgt daher nach Gl. (11.1) $Q = J _ { 1 } \omega _ { 1 } ^ { 2 } / 2 + J _ { 2 } \omega _ { 2 } ^ { 2 } / 2$

3. Nach dem BOHRschen Atommodell „besteht“ ein Wasserstoffatom aus einem Proton als Atomkern und einem Elektron, welches den Atomkern umkreist. Das Elektron (Masse $m _ { \mathrm { e } } =$ $^ { 9 , 1 \cdot 1 0 ^ { - 3 1 } }$ kg) hat im Grundzustand die kinetische Energie $E _ { \mathrm { k 1 } } = 2 , 1 8 \cdot 1 0 ^ { - 1 8 }$ und den Bahndrehimpuls $L _ { 1 } = 1 { , } 0 5 { \cdot } 1 0 ^ { - 3 4 } \mathrm { J }$ · s. Man bestimme den Radius $r _ { 1 }$ des H-Atoms! Wie groß ist $L _ { n }$ auf der n-ten Elektronenbahn, wenn für diese gilt $r _ { n } = n ^ { 2 } r _ { 1 }$ und $\nu _ { n } = \nu _ { 1 } / n ? \; ( n = 1 , 2 , 3 , \ldots )$

Lösung: Aus dem Bahndrehimpuls in Gl. (11.12) $L _ { 1 } = m _ { \mathrm { e } } \nu _ { 1 } r _ { 1 }$ und der kinetischen Energie des Elektrons $E _ { \mathrm { k 1 } } = m _ { \mathrm { e } } v _ { \mathrm { 1 } } ^ { 2 } / 2$ erhält man durch Elimination von $\nu _ { 1 }$ den sog. BOHRschen Radius $r _ { 1 } = L _ { 1 } / \sqrt { 2 m _ { \mathrm { e } } E _ { \mathrm { k 1 } } } = 0 . 5 3 \cdot 1 0 ^ { - 1 0 }   \mathrm { { r } }$ m. Analog dazu folgt mit $E _ { \mathbf { k } n } = m _ { \mathbf { e } } \nu _ { n } ^ { 2 } / 2 = E _ { \mathbf { k } 1 } / n ^ { 2 } ;   L _ { n } =$ $r _ { n } { \sqrt { 2 m _ { \mathbf { e } } E _ { \mathbf { k } n } } } = n ^ { 2 } r _ { 1 } { \sqrt { 2 m _ { \mathbf { e } } E _ { \mathbf { k } 1 } / n ^ { 2 } } } = n r _ { 1 } { \sqrt { 2 m _ { \mathbf { e } } E _ { \mathbf { k } 1 } } } = n L _ { 1 }$ . Für den Drehimpuls des Elektrons sind also nur ganzzahlige Vielfache des kleinsten Drehimpulses $L _ { 1 }$ möglich (Drehimpulsquantelung, vgl. 44.3). □

## 11.5 Kreiselbewegungen. Freie Achsen

Der im vorangegangenen Abschnitt dargelegte Zusammenhang zwischen Drehmoment und Drehimpuls lässt sich anschaulich am **Kreisel** demonstrieren. Unter einem Kreisel verstehen wir einen starren Körper, der sich völlig frei oder um höchstens einen Punkt, in dem er festgehalten wird, dreht. Er hat drei Freiheitsgrade der Rotation um diesen Punkt, wobei die Drehachse im Zeitablauf ihre Lage im Raum und relativ zum Kreisel ändern kann.

Jeder Körper hat zwei aufeinander senkrechte, durch den Schwerpunkt gehende Achsen, von denen die eine zum größten, die andere zum kleinsten Trägheitsmoment gehört. Zusammen

---

124

11 Dynamik des starren Körpers

mit einer dritten Achse, die auf den beiden anderen senkrecht steht, bilden sie die sog. **Hauptträgheitsachsen** oder **Hauptachsen** des Körpers. Sie sind fest mit dem Körper verbunden. Jede Symmetrieachse ist auch Hauptträgheitsachse.

Sind $x , y , z$ die Koordinaten eines rechtwinkligen Koordinatensystems, das mit den Hauptträgheitsachsen des Körpers zusammenfällt, so gehorchen die zu diesen Achsen gehörigen Hauptträgheitsmomente $J _ { 1 } , J _ { 2 }$ und $J _ { 3 }$ der Beziehung

$$
J _ {1} x ^ {2} + J _ {2} y ^ {2} + J _ {3} z ^ {2} = 1, \tag {11.14}
$$

die hier nicht hergeleitet werden kann. Dies ist die Gleichung eines Ellipsoids, des sog. Trägheitsellipsoids des Körpers, mit den Halbachsen

$$
a = \frac {1}{\sqrt {J _ {1}}}, \quad b = \frac {1}{\sqrt {J _ {2}}}, \quad c = \frac {1}{\sqrt {J _ {3}}}. \tag {11.15}
$$

Dabei können zwei oder auch alle drei Hauptträgheitsmomente gleich sein. Im ersten Fall sprechen wir von einem **symmetrischen Kreisel**, im zweiten Fall von einem **Kugelkreisel**. So ist jeder auf einer Drehmaschine gefertigte Körper ein symmetrischer Kreisel; sein Trägheitsellipsoid ist ein Rotationsellipsoid, da zwei Halbachsen gleich groß sind. Die Symmetrieachse des Kreisels wird **Figurenachse** genannt.

![](../../raw/pages_0097-0128/images/page_126_image_8.jpg)

<details>
<summary>text_image</summary>

-F_L
ω
S
-F_Z
a)
F_Z
-F_Z
FL
b)
ω
F_Z
-F_Z
c)
ω
F_Z
</details>

Bild 11.8 Einfluss der Zentrifugalkräfte auf die Stabilität der Drehbewegung einer Kreisscheibe a) um eine beliebig orientierte Schwerpunktachse b) um die Hauptachse mit dem größten Trägheitsmoment c) um die Hauptachse mit dem kleinsten Trägheitsmoment

Bild 11.8a zeigt eine Kreisscheibe, die um eine Schwerpunktachse rotiert, die keine Symme trieachse, also keine Hauptträgheitsachse, ist. Die infolge der Rotation auftretenden Fliehkräfte $F _ { Z }$ und $- F _ { Z }$ bilden ein Kräftepaar, dessen Moment, das sog. Zentrifugalmoment, bewirkt, dass der Kreisel sich um die im Schwerpunkt S senkrecht auf der Zeichenebene stehende Achse dreht. Hat der Kreisel die Endlage b) in Bild 11.8 erreicht, so verschwindet wegen der nun in einer Wirkungslinie liegenden Zentrifugalkräfte das Zentrifugalmoment, und die Rotation kann stabil erfolgen. Bei fester Achsenlagerung wird das Zentrifugalmoment durch ein entgegengesetztes Drehmoment aufgehoben, das durch Zwangskräfte in der Achse erzeugt wird (Lagerreaktion $F _ { \mathrm { L } }$ , Bild 11.8a).

Diese Überlegungen zeigen, dass der Körper eine stabile Drehbewegung nur um solche Achsen ausführen kann, für die das Drehmoment der Zentrifugalkräfte verschwindet. Dies ist nur bei der Rotation des Körpers um die Achse seines größten oder kleinsten Trägheitsmoments der Fall, entsprechend Bild 11.8b und c. Die Drehachse braucht dann nicht mehr in Lagern gehaltert zu werden, weshalb diese stabilen Drehachsen als **freie Achsen** bezeichnet werden.

---

11.6 Bewegung des symmetrischen Kreisels

125

**Die Drehachsen eines starren Körpers, auf welche dieser keinerlei Kraftwirkung infolge von Fliehkräften ausübt, heißen freie Achsen. Es sind dies die durch den Schwerpunkt gehenden, zum größten und kleinsten Trägheitsmoment des Körpers gehörigen Drehachsen.**

Dies kann an folgendem einfachen Experiment demonstriert werden (Bild 11.9): Wird ein quaderförmiger Körper derart nach oben geworfen, dass er sich um jeweils eine seiner drei Symmetrieachsen 1, 2 oder 3 dreht, so zeigt sich, dass er eine stabile Drehbewegung nur um die Achse 1 mit dem größten und die Achse 3 mit dem kleinsten Trägheitsmoment ausführt, während er um die Achse 2 mit dem mittleren Trägheitsmoment torkelt (labile Bewegung).

![](../../raw/pages_0097-0128/images/page_127_image_4.jpg)

<details>
<summary>natural_image</summary>

Line drawing of a hand holding a rectangular object next to a 3D block with numbered components (no text or symbols)
</details>

Bild 11.9 Starrer Körper mit zugehörigen Hauptträgheitsachsen 1, 2 und 3. Die Achsen 1 und 3 sind freie Achsen.

Eine wirklich stabile Drehachse ist allerdings nur die zum größten Trägheitsmoment gehörige (Bild 11.8b); denn in diese Lage stellt sich der Körper bei einer Störung der Drehbewegung stets auch dann ein, wenn er um die an sich stabile Achse 3 seines kleinsten Trägheitsmoments rotiert. Jede Störung dieser stabilen Lage ruft sofort ein Drehmoment hervor, das die ursprüngliche Lage wieder herzustellen versucht.

## 11.6 Bewegung des symmetrischen Kreisels

**Kräftefreier Kreisel.** Greifen am Kreisel keine seinen Bewegungszustand ändernden Kräfte bzw. Drehmomente an, so wird er als kräftefrei bezeichnet. Kräftefreiheit kann durch eine spezielle Konstruktion erreicht werden, bei der der Schwerpunkt mit dem Unterstützungspunkt des Kreisels zusammenfällt.

Das Fehlen äußerer Kräfte hat die Erhaltung von Energie (hier nur Rotationsenergie) und Drehimpuls zur Folge. Da der Drehimpuls ein Vektor ist, ergibt sich daraus, dass dieser bei noch so komplizierten Kreiselbewegungen sowohl dem Betrage als auch der Richtung nach konstant bleibt. Die durch den Kreiselschwerpunkt in Richtung des Drehimpulsvektors L weisende Gerade mit unveränderlicher Richtung bezeichnet man daher als raumfeste Impulsachse (s. Bild 11.10).

Die Symmetrieachse des Kreisels mit dem größten Trägheitsmoment $J _ { 1 }$ , die Figurenachse, braucht aber bei der Kreiselbewegung nicht unbedingt mit der raumfesten Impulsachse L zusammenzufallen, sondern sie kann auf einem Kegelmantel um den im Raum feststehenden Vektor L umlaufen. Man nennt diese Bewegung des kräftefreien Kreisels **Nutation**. Fallen zu Beginn der Kreiselbewegung Figurenachse und Drehimpulsachse zusammen, so erfolgt die Drehbewegung nutationsfrei, d. h., die Figurenachse behält ihre Richtung im Raum bei.

Die Achse, um welche in einem bestimmten Augenblick die Drehung des Kreisels erfolgt, ist jedoch im Allgemeinen weder die Figurenachse noch die Impulsachse, sondern eine dritte Achse, die als momentane Drehachse bezeichnet wird. D. h., der Vektor der Winkelgeschwindigkeit

---

126

11 Dynamik des starren Körpers

ω der Drehbewegung des Kreisels um diese Achse muss nicht mit der Figurenachse des Kreisels zusammenfallen. Zu einer solchen Bewegung kommt es zum Beispiel, wenn der um seine Figurenachse rotierende Kreisel einen seitlichen Stoß erhält. Der Vektor der Winkelgeschwin digkeit ω erhält dadurch eine zusätzliche Komponente und fällt dann weder mit der Figuren achse noch mit der Drehimpulsachse zusammen. Da nur die Drehimpulsachse eine raumfeste Achse ist, führen daher bei der Kreiselbewegung sowohl die Figurenachse als auch die momentane Drehachse (ω) Bewegungen um die raumfeste Impulsachse (L) aus (Bild 11.10).

![](../../raw/pages_0129-0160/images/page_128_image_3.jpg)

<details>
<summary>text_image</summary>

Figurenachse
J1
L
ω1
ω2
L2
J2
Figurenachse
Gangpol-
kegel
Rastpolkegel
Rasmfeste
impulsachse
momentane
Drehachse
rasmfeste
impulsachse
momentane
Drehachse
Nutations
kegel
</details>

Bild 11.10 Achsen bei der Drehbewegung des kräftefreien Kreisels (Nutation)

Um diese komplizierte Bewegung näher zu analysieren, zerlegt man den Vektor $\pmb { \omega } ,$ der also im Allgemeinen nicht die Richtung der Figurenachse hat, in seine beiden aufeinander senkrecht stehenden Komponenten $\omega _ { 1 }$ in Richtung der Figurenachse mit dem größten Trägheitsmoment $J _ { 1 }$ und $\omega _ { 2 }$ in Richtung der zweiten Hauptträgheitsachse mit dem kleinsten Trägheitsmoment $J _ { 2 }$ (Bild 11.10 links). Die Bewegung wird damit in zwei unabhängige Rotationsbewegungen um die entsprechenden Hauptträgheitsachsen zerlegt. Da die Trägheitsmomente $J _ { 1 }$ und $J _ { 2 }$ in diesen Achsenrichtungen im Allgemeinen verschieden sind, fällt der gemäß Gl. (11.11) aus den Komponenten $L _ { 1 } = J _ { 1 } \pmb { \omega } _ { 1 }$ und $L _ { 2 } = J _ { 2 } \pmb { \omega } _ { 2 }$ vektoriell zusammengesetzte Drehimpuls L nicht in die Richtung der momentanen Drehachse (ω).

Figurenachse, raumfeste Impulsachse und momentane Drehachse liegen stets in einer Ebene. Da sich der Kreisel momentan um die gezeichnete, in ihrer Lage gegenüber dem Kreisel dauernd veränderliche ω-Achse dreht, die Figurenachse also momentan eine Drehung um diese Achse ausführt, und weil die raumfeste Impulsachse ihre Richtung beibehält und diese drei Achsen stets in einer Ebene liegen, folgt, dass bei der Nutation des Kreisels Figurenachse und momentane Drehachse dauernd die raumfeste Impulsachse umkreisen. Dabei beschreibt die momentane Drehachse im festen Raum den Rastpolkegel, gegenüber der beweglichen Figurenachse den Gangpolkegel, so dass der Gangpolkegel auf dem Rastpolkegel abrollt. Beim nutationsfreien Kreisel fallen alle drei Achsen zusammen, die Figurenachse behält ihre Richtung im Raum bei und alle drei Kegel entarten in eine Gerade in Richtung dieser Achse.

**Kreisel unter Einwirkung äußerer Kräfte.** In Bild 11.11 ist ein Kreisel (rotierendes Rad) mit horizontal gelegener Drehachse dargestellt, der nicht kräftefrei ist, da er außerhalb seines Schwerpunkts S in O unterstützt ist. Unter der Wirkung der in S angreifenden Schwerkraft F kippt jedoch der Kreisel nicht nach unten ab, wie es bei fehlender Rotation der Fall wäre, sondern die Figurenachse weicht einer solchen Bewegung seitlich aus, indem sie sich horizontal mit konstanter Winkelgeschwindigkeit $\omega _ { \mathrm { P } }$ dreht. Diese Bewegung des Kreisels nennt man **Präzession**.

Die Präzessionsbewegung kommt dadurch zustande, dass die in S angreifende Schwerkraft F in Bezug auf den Unterstützungspunkt O ein Drehmoment M erzeugt, das wegen Gl. (11.10)

---

11.6 Bewegung des symmetrischen Kreisels

127

$M = \mathbf { d } \mathbf { L } / \mathbf { d } t$ in der Zeit dt eine Änderung des Drehimpulses d $\mathbf { I } L = M \mathbf { d } t$ hervorruft. Der Vektor dL hat dabei die Richtung von M und setzt sich mit L zum veränderten Drehimpuls $\pmb { L } ^ { \prime } = \pmb { L }   +   \pmb { \mathrm { d } } \pmb { L }$ zusammen, in dessen Richtung sich die Kreiselachse immer wieder neu einstellt.

Die Winkelgeschwindigkeit der Präzession $\omega _ { \mathrm { P } } = \mathbf { d } \varphi / \mathbf { d } t$ kann wie folgt ermittelt werden: Der Betrag |dL| berechnet sich wegen seiner Kleinheit als Bogen eines Kreises mit dem Radius |L| zu d $L = L \mathbf { d } \varphi$ . Damit erhalten wir für den Betrag des wirkenden Drehmoments

$$
M = \frac {\mathrm{d} L}{\mathrm{d} t} = L \frac {\mathrm{d} \varphi}{\mathrm{d} t} = L \omega_ {\mathrm{P}}, \tag {11.16}
$$

woraus mit Gl. (11.11) folgt

$$
\omega_ {\mathrm{P}} = \frac {M}{L} = \frac {M}{J \omega} \quad (\text {Winkelgeschwindigkeit der Präzession}). \tag {11.17}
$$

Dabei sind J das Trägheitsmoment des Kreisels bezüglich seiner Figurenachse und ω die Winkelgeschwindigkeit der Rotation des Kreisels um die Figurenachse. Der Kreisel präzediert also umso schneller, je langsamer er um seine Achse rotiert und je größer das einwirkende Drehmoment ist.

![](../../raw/pages_0129-0160/images/page_129_image_8.jpg)

<details>
<summary>text_image</summary>

ωP
M
0
S
L' = L + dL
dφ
L
dL
F
</details>

Bild 11.11 Bewegung eines außerhalb des Schwerpunkts unterstützten Kreisels (Präzession)

![](../../raw/pages_0129-0160/images/page_129_image_10.jpg)

<details>
<summary>text_image</summary>

L
S
dL
F
</details>

Bild 11.12 Präzession eines Kinderkreisels

Bei dem in Bild 11.12 dargestellten Kreisel, dessen Achse mit der Richtung der Schwerkraft $F = m g$ den Winkel $\alpha$ einschließt und dessen Schwerpunkt vom Unterstützungspunkt den Abstand s hat, ist das wirksame Drehmoment von der Größe $M = m g$ s sinα. Der Kreisel kippt nicht unter der Wirkung seines Gewichts, sondern seine Figurenachse läuft, indem sie der Schwerkraft senkrecht ausweicht, auf einem Kegelmantel um.

**Anwendungen.** Die Eigenschaften des Kreisels werden besonders in der modernen Luftfahrt- und Raketentechnik genutzt. Ein mit hoher Drehzahl um seine vertikal gerichtete Figurenachse rotierender Kreisel behält seine gegenüber Störungen sehr unempfindliche Lage mit großer Genauigkeit bei und dient beim Blindflug als künstlicher Horizont. Die Kombination zweier solcher Kreisel, die für die Einhaltung des Horizontal- und Geradeausfluges sorgen, nennt man Autopilot. Ähnliche Anordnungen benutzt man auch zur Steuerung ballistischer Raketen. Eine weitere, lange bekannte Anwendung ist der Kreiselkompass. Es handelt sich um einen Kreisel, der so aufgehängt ist, dass er sich vertikal und horizontal drehen kann (kardanische Aufhängung). Seine Achse verläuft horizontal und weicht den wirkenden vertikalen Kräften so lange horizontal aus, bis sie in Richtung des Meridians verläuft; sie zeigt dann die geografische Nord-Süd-Richtung an.
