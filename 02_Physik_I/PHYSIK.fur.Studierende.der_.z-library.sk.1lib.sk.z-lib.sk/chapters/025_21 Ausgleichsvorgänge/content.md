# 21 Ausgleichsvorgänge

原始 PDF 第 246–253 页。

21

Ausgleichsvorgänge

## 21.1 Wärmeleitung

Befinden sich zwei Stellen eines Körpers auf unterschiedlichen Temperaturen, so wird sich nach dem II. Hauptsatz der vorhandene Temperaturunterschied im Laufe der Zeit ausgleichen, indem eine bestimmte Wärmemenge Q von der wärmeren zur kälteren Stelle übergeht. Diese Erscheinung bezeichnet man als Wärmeleitung.

**Wärmeleitung ist ein durch Temperaturunterschiede hervorgerufener Energietransport.**

![](../../raw/pages_0225-0256/images/page_245_image_5.jpg)

Bild 21.1 Wärmeleitung a) durch eine einschichtige, b) durch eine zweischichtige Wand; c) zu- und abfließender Wärmestrom für eine differenziell dünne Schicht

Betrachten wir die stationäre (d. h. zeitlich konstant erfolgende) Wärmeleitung durch eine ebene Wand der Fläche A und der Dicke l (Bild 21.1a), so ist die übertragene Wärmeenergie Q direkt proportional der Temperaturdifferenz $\Delta T = T _ { 1 } - T _ { 2 }$ , der Wandfläche A und der Zeit t, aber indirekt proportional der Wanddicke l:

$$
Q = \lambda \frac {A t \Delta T}{l}. \tag {21.1}
$$

Der Proportionalitätsfaktor λ heißt **Wärmeleitfähigkeit** (Einheit: $1 \mathrm { W } / ( \mathrm { m } \cdot \mathrm { K } )$ und ist eine Stoffkonstante. Hieraus ergibt sich analog zum Massenstrom (15.2)

$$
\Phi = \frac {\mathrm{d} Q}{\mathrm{d} t} \equiv \dot {Q} = \lambda \frac {A \Delta T}{l} \quad (\text {Warmestrom}). \tag {21.2}
$$

Einheit: [Φ] = 1J/s = 1W.

Damit wird die **Wärmestromdichte**

$$
j _ {\mathrm{W}} = \frac {\mathrm{d} \varPhi}{\mathrm{d} A} = \lambda \frac {\Delta T}{l}; \quad \text {Einheit:} \quad [ j _ {\mathrm{W}} ] = 1 \mathrm{W/m} ^ {2}. \tag {21.3}
$$

---

244

21 Ausgleichsvorgänge

Analog dem elektrischen Widerstand (25.8) bezeichnet man den Ausdruck

$$
R _ {\lambda} = \frac {1}{\lambda} \frac {l}{A}, \quad \text {Einheit:} \quad [ R _ {\lambda} ] = 1 \mathrm{K/W}, \tag {21.4}
$$

als **Wärmeleitwiderstand**. Damit folgt nun für den Wärmestrom aus (21.2) die dem OHMschen Gesetz der Elektrizitätslehre entsprechende Beziehung

$$
\Phi = \frac {\Delta T}{R _ {\lambda}} \quad \text {oder} \quad \Delta T = R _ {\lambda} \Phi . \tag {21.5}
$$

Für eine zweischichtige Wand (Bild 21.1b) addieren sich die Wärmeleitwiderstände (21.4) der einzelnen Schichten, und man erhält für den effektiven Wärmestrom

$$
\Phi = A \frac {T _ {1} - T _ {3}}{\frac {l _ {1}}{\lambda_ {1}} + \frac {l _ {2}}{\lambda_ {2}}}. \tag {21.6}
$$

Ist das Temperaturgefälle nicht – wie in Bild 21.1a, b – linear, sondern in x-Richtung veränderlich, so lautet das Wärmeleitungsgesetz (21.3)

$$
j _ {\mathrm{W}} = - \lambda \frac {\mathrm{d} T}{\mathrm{d} x} \quad \text {oder} \quad \boldsymbol {j} _ {\mathrm{W}} = - \lambda \operatorname{grad} T \quad \begin{array}{l} (\text {FOURIERSches} \\ \text {Wärmeleitungsgesetz}). \end{array} \tag {21.7}
$$

dT /dx (bzw. $\Delta T / l$ in Gleichung (21.3)) nennt man den Temperaturgradienten. Das negative Vorzeichen drückt aus, dass mit zunehmendem Wärmeweg $x \; ( \mathbf { d } x > 0 )$ die Temperatur $T$ abnimmt (d $( T < 0 )$

Der gesamte, einem Körper zu- und von ihm abfließende Wärmestrom ergibt sich aus (21.2) und (21.3), wenn man über die gesamte Körperoberfläche $A _ { 0 }$ integriert. Dieser muss gleich der zeitlichen Änderung der Wärmeenergie des betreffenden Körpers mit der Masse m und der spezifischen Wärmekapazität c sein. Folglich gilt

$$
\dot {Q} = \oint_ {A _ {0}} \boldsymbol {j} _ {\mathrm{W}} \cdot \mathrm{d} \boldsymbol {A} = c m \frac {\mathrm{d} T}{\mathrm{d} t} \quad (\text {Bilanzgleichung für Wärmeströme}). \tag {21.8}
$$

Diese Gleichung drückt den Satz von der Erhaltung der Wärmeenergie aus und kann als Kontinuitätsgleichung für Wärmeströme angesehen werden. Für einen nur in x-Richtung fließenden Wärmestrom (Bild 21.1c) durch eine differenziell dünne Schicht der Masse dm $= \varrho A$ dx (ϱ Dichte) nimmt die Bilanzgleichung (21.8) die Form an:

$$
c \varrho A \mathrm{d} x \frac {\mathrm{d} T}{\mathrm{d} t} = [ j _ {\mathrm{W}} - (j _ {\mathrm{W}} + \mathrm{d} j _ {\mathrm{W}}) ] A \quad \text {oder} \quad \frac {\mathrm{d} T}{\mathrm{d} t} = - \frac {1}{c \varrho} \frac {\mathrm{d} j _ {\mathrm{W}}}{\mathrm{d} x}.
$$

Setzen wir für $j _ { \mathrm { W } }$ den FOURIERschen Ausdruck (21.7) ein und schreiben – da T sowohl vom Ort als auch von der Zeit abhängt – anstelle des Differenzialzeichens (d) das Symbol ∂ für die sog. partielle Ableitung, so erhalten wir die partielle Differenzialgleichung

$$
\frac {\partial T}{\partial t} = \frac {\lambda}{c \varrho} \frac {\partial^ {2} T}{\partial x ^ {2}} \quad (\text {eindimensionale Wärmeleitungsgleichung}). \tag {21.9}
$$

Der Quotient $\lambda / ( c \varrho ) = a$ wird als **Temperaturleitfähigkeit** bezeichnet (Einheit: $1 \mathrm { m } ^ { 2 } / \mathrm { s } )$ . Die Lösungen von Gleichung (21.9) beschreiben die Wärmeausbreitung in Form des örtlich und zeitlich veränderlichen Temperaturfeldes $T = T ( x ,   t )$

---

21.1 Wärmeleitung

245

Ersetzt man in Gleichung (21.9) t durch −t, so wechselt die linke Seite der Gleichung ihr Vorzeichen, sie ist also gegenüber einer Zeitumkehr-Transformation nicht invariant. Folglich beschreibt sie Vorgänge, die nicht umkehrbar, also in Übereinstimmung mit der Aussage des II. Hauptsatzes irreversibel sind (vgl. Abschnitt 19.4).

Im **stationären** Fall sind die Temperaturunterschiede zeitlich konstant, d. h., es ist $\partial T / \partial t =$ 0. Dies bedeutet nach Gleichung (21.8), dass zu- und abgeführter Wärmestrom gleich groß und durch die Beziehung (21.2) gegeben sind. Es wird also stets genauso viel Wärme ab- wie zugeführt (Fließgleichgewicht).

Als ein wichtiges Beispiel für einen **instationären** Vorgang ist in Bild 21.2 die Lösung der Wärmeleitungsgleichung (21.9)

$$
T (x, t) = T _ {0} + (T _ {1} - T _ {0}) \sqrt {\frac {t _ {0}}{t}} \mathrm{e} ^ {- \frac {x ^ {2}}{4 a t}} \quad \text {mit} \quad a = \frac {\lambda}{c \varrho} \tag {21.10}
$$

für die Ausbreitung einer anfänglich punktförmigen Wärmequelle in einem unendlich langen, dünnen Stab dargestellt (z. B. Lötstelle oder Schweißnaht).

![](../../raw/pages_0225-0256/images/page_247_chart_7.jpg)

<details>
<summary>contour</summary>

| Time Interval | Peak Height (T) |
| --- | --- |
| T(x, t0) | ~1.0 |
| T(x, t1 > t0) | ~0.6 |
| T(x, t2 > t1) | ~0.4 |
| T(x, t3 > t2) | ~0.3 |
</details>

Bild 21.2 Orts- und zeitabhängiger Temperaturverlauf eines an einer eng begrenzten Stelle bei $x = 0$ kurzzeitig auf $T _ { 1 }$ erwärmten langen dünnen Stabes der Temperatur $T _ { 0 }$ beschrieben durch die sich als Lösung der Wärmeleitungsgleichung (21.9) ergebende Gauss-Funktion (21.10)

Die Wärmeleitfähigkeit fester Körper wird durch zwei verschiedene Mechanismen verursacht. Zum einen führt die thermische Energie zu kollektiven Schwingungen der Gitterbausteine (Gitterschwingungen), die als **Phononen** bezeichnet werden und die bei ihrer Bewegung durch einen Kristall Wärmeenergie mit sich führen. Die von diesem Prozess herrührende Phononen-Wärmeleitfähigkeit $\lambda _ { \mathrm { p } }$ ist von Störungen des Kristallgitters abhängig, die die Phononenausbreitung behindern. Zum anderen sind die im Festkörper vorhandenen beweglichen Ladungsträger (meist Elektronen) zugleich Träger thermischer Energie. Die darauf beruhende elektronische Wärmeleitfähigkeit $\lambda _ { \mathbf { e } }$ ist daher bei den Metallen mit der elektrischen Leitfähigkeit κ durch das WIEDEMANN-FRANZsche Gesetz

$$
\frac {\lambda_ {\mathrm{e}}}{\varkappa} = \mathrm{const} \cdot T
$$

verbunden (vgl. 26.1). Es gilt $\lambda = \lambda _ { \mathrm { e } } + \lambda _ { \mathrm { p } }$

Die Dominanz der elektronischen Komponente der Wärmeleitfähigkeit führt bei Metallen zu großen λ-Werten, während in Halbleitern und Isolatoren wegen der geringen Ladungsträgerkonzentration die Wärmeleitung im Wesentlichen durch Phononen vermittelt wird. Noch geringer sind die Wärmeleitfähigkeiten von zusammengesetzten Stoffen, wie z. B. Holz, von Flüssigkeiten (außer Quecksilber!) und Gasen (vgl. Tabelle 21.1).

---

246

21 Ausgleichsvorgänge

Tabelle 21.1 Wärmeleitfähigkeit einiger Stoffe bei 300 K in $J/(s \mathrm{~m} \mathrm{~K}) = W/(m \mathrm{~K})$

<table><tr><td colspan="2">Wärmeleiter</td><td colspan="2">Wärmeisolatoren</td><td colspan="2">Flüssigkeiten</td><td colspan="2">Gase</td></tr><tr><td>Aluminium</td><td>230</td><td>Glas</td><td>1,0 ... 1,2</td><td>Ethanol</td><td>0,17</td><td>Helium</td><td>0,144</td></tr><tr><td>Kupfer</td><td>380</td><td>Glaswolle</td><td>0,04 ... 0,05</td><td>Benzol</td><td>0,17</td><td>Kohlendioxid</td><td>0,014</td></tr><tr><td>Messing</td><td>110</td><td>Holz</td><td>0,14 ... 0,20</td><td>Glycerin</td><td>0,29</td><td>Luft</td><td>0,023</td></tr><tr><td>Silber</td><td>420</td><td>Polystyrol</td><td>0,15 ... 0,17</td><td>Quecksilber</td><td>8,37</td><td>Wasserstoff</td><td>0,173</td></tr><tr><td>Stahl</td><td>55</td><td>Ziegelstein</td><td>0,4 ... 0,6</td><td>Wasser</td><td>0,59</td><td>Vakuum</td><td>0</td></tr></table>

## Beispiele 21.1:

1. Welche Temperatur $T _ { 2 }$ hat die Grenzfläche innerhalb der zweischichtigen Wand von Bild 21.1b bei gegebenen Außentemperaturen $T _ { 1 }$ und $T _ { 3 }$ und stationärer Wärmeleitung?

Lösung: Durch Gleichsetzen von zu- und abgeführtem Wärmestrom nach Gleichung (21.2), $\phi _ { \mathrm { z u } } = \lambda _ { 1 } ( T _ { 1 } - T _ { 2 } ) / l _ { 1 } = \phi _ { \mathrm { a b } } = \lambda _ { 2 } ( T _ { 2 } - T _ { 3 } ) / l _ { 2 }$ , ergibt sich nach Umstellung

$$
T _ {2} = \frac {\Lambda_ {1} T _ {1} + \Lambda_ {2} T _ {3}}{\Lambda_ {1} + \Lambda_ {2}} \quad \text {mit} \quad \Lambda_ {1} = \frac {\lambda_ {1}}{l _ {1}} \quad \text {und} \quad \Lambda_ {2} = \frac {\lambda_ {2}}{l _ {2}}.
$$

2. Ein kugelförmiger Behälter vom Radius $R = 1 { , } 5$ m empfängt durch Sonneneinstrahlung den Wärmestrom $\dot { Q } = 6 W ,$ der im stationären Zustand durch Wärmeleitung vollständig an die ihn umgebende Luft (Wärmeleitfähigkeit $\lambda = 0 , 0 2 5 \mathrm { W } / ( \mathrm { m } \cdot \mathrm { K } )$ abgeführt wird. Welche Oberflä- chentemperatur erreicht der Behälter, wenn die Lufttemperatur weit weg vom Behälter $2 0   ^ { \circ } \mathbf { C }$ beträgt? Wie groß ist die Lufttemperatur in 4m Entfernung von der Behälteroberfläche?

Lösung: Der durch eine konzentrische Kugelfläche $A = 4 \pi r ^ { 2 }$ um den Behälter abfließende Wärmestrom ist für beliebige Radien $r \geq R$ gleich groß und beträgt $j _ { \mathrm { W } } A = j _ { \mathrm { W } } 4 \pi r ^ { 2 } = \dot { Q }$ . Für die Wärmestromdichte $j _ { \mathrm { W } }$ beim Radius r gilt das FOURIERsche Wärmeleitungsgesetz (21.7) $j _ { \mathrm { W } } = - \lambda \mathrm { d } T / \mathrm { d } r$ , womit man erhält:

$$
- 4 \pi r ^ {2} \lambda \frac {\mathrm{d} T}{\mathrm{d} r} = \dot {Q} \quad \text {oder} \quad \mathrm{d} T = - \frac {\dot {Q}}{4 \pi \lambda r ^ {2}} \mathrm{d} r.
$$

Mit $T = T ( r )$ beim Radius r und $T = T _ { \infty } = 2 9 3 , 1 5 \mathrm { K }$ für $r \to \infty$ erhält man durch Integration

$$
\int_ {T (r)} ^ {T _ {\infty}} \mathrm{d} T = - \frac {\dot {Q}}{4 \pi \lambda} \int_ {r} ^ {\infty} \frac {\mathrm{d} r}{r ^ {2}} \quad \text {bzw.} \quad T (r) = T _ {\infty} + \frac {\dot {Q}}{4 \pi \lambda r}.
$$

Die Temperatur an der Behälteroberfläche beträgt somit $T ( R ) = T _ { \infty } + { \dot { Q } } / ( 4 \pi \lambda R ) = 3 0 5 { , } 8 8   \mathrm { K } ( =$ $^ { 3 2 , 7   ^ { \circ } \mathrm { C } ) }$ und in $r_{1}=4m+1,5m=5,5$ m Entfernung $T(r_{1}) = 296, 62  K ( = 23, 5 ^{\circ} C )$ □

## 21.2 Wärmeübergang, Wärmedurchgang, Konvektion

Unter **Wärmeübergang** versteht man die Übertragung von Wärmeenergie von einem festen Körper auf eine Flüssigkeit oder ein Gas bzw. in umgekehrter Richtung. An der Übergangsstelle tritt ein mehr oder weniger stark ausgeprägter Temperaturgradient auf (Bild 21.3a). Der Wärmestrom Φ ist der Größe der Begrenzungsfläche A und der zwischen beiden Medien herrschenden Temperaturdifferenz $\Delta T = T _ { 1 } - T _ { 2 }$ proportional; es gilt

$$
\Phi = \alpha A \Delta T \quad (\alpha \text {Wärmeübergangskoeffizient, Einheit:} 1 \mathrm{W} / (\mathrm{m} ^ {2} \cdot \mathrm{K}). \tag {21.11}
$$

---

21.2 Wärmeübergang, Wärmedurchgang, Konvektion

247

α hängt von der Oberflächenbeschaffenheit (Rauigkeit) der Wand und der Bewegung der Flüssigkeiten bzw. Gase ab.

![](../../raw/pages_0225-0256/images/page_249_image_3.jpg)

Bild 21.3 a) Wärmeübergang, b) Wärmedurchgang

**Wärmedurchgang.** Sind Gase oder Flüssigkeiten durch eine feste Wand getrennt (Bild 21.3b), so findet zunächst ein Wärmeübergang vom Gas (von der Flüssigkeit) auf die Wand, danach Wärmeleitung in der Wand und anschließend wieder Wärmeübergang an das andere Gas (die andere Flüssigkeit) statt. Für den resultierenden Wärmestrom gilt wie bei Gleichung (21.11)

$$
\Phi = k A \Delta T \quad (k \text {Wärmedurchgangskoeffizient,} E i n h e i t: 1 \mathrm{W} / (\mathrm{m} ^ {2} \cdot \mathrm{K}). \tag {21.12}
$$

Entsprechend den drei Teilprozessen erhält man für eine ebene Wand der Dicke l aus der Addition der Wärmewiderstände

$$
\frac {1}{k} = \frac {1}{\alpha_ {1}} + \frac {1}{\alpha_ {2}} + \frac {l}{\lambda}. \tag {21.13}
$$

**Konvektion (Wärmemitführung).** Diese tritt bei Flüssigkeiten und Gasen auf und beruht auf der Entstehung von Dichteunterschieden infolge ungleichmäßiger Erwärmung, wodurch es zur Ausbildung einer Flüssigkeits- oder Gasströmung kommt (freie Konvektion). Dabei führen die Moleküle des strömenden Mediums thermische Energie mit sich. So z. B. steigt erwärmte Luft infolge des Auftriebs nach oben, statt ihrer sinkt kältere zu Boden usw. Konvektive Wärmeübertragung finden wir bei Wärmetauschern (Gegenstromprinzip), bei der Zentralheizung, bei meteorologischen Vorgängen u. a. Bei erzwungener Konvektion wird durch äußere Kräfte (Umwälzpumpe, Ventilator) eine Zwangsströmung erzeugt. Da der Temperaturausgleich bei Konvektion bedeutend schneller vonstatten geht als bei Wärmeleitung, sind Maßnahmen der Wärmedämmung häufig mit der Verhinderung von Konvektion verbunden (z. B. Doppelfenster, Schaumstoffe u. a.). Bei Glasgefäßen mit Vakuummantel (Thermosbehälter, DEWAR-Gefäß) wird Konvektion und Wärmeleitung vermieden.

Eine weitere Form der Wärmeübertragung, die sich vom Wesen her grundlegend von den hier besprochenen Erscheinungen des Wärmetransports unterscheidet, ist die **Wärmestrahlung**. Sie wird erst in Abschnitt 42.1 behandelt.

## Beispiel 21.2:

Berechne die Zeit, in der sich ein Behälter von $A = 1 { , } 5 \mathrm { m } ^ { 2 }$ Oberfläche und $V = 0 , 3   \mathrm { m } ^ { 3 }$ Wasserinhalt, spezifische Wärmekapazität $c = 4.19    kJ/(kg \cdot  K)$ , von seiner Anfangsinnentemperatur $\vartheta _ { 1 } = 8 0   ^ { \circ } \mathrm { C }$ auf $\vartheta _ { 2 } = 5 0   ^ { \circ } \mathrm { C }$ abkühlt, wenn sein Wärmedurchgangskoeffizient $k = 1 0 W / ( m ^ { 2 } \cdot K )$ und die Außentemperatur $\vartheta _ { \mathsf { a } } = 2 0   ^ { \circ } \mathrm { C }$ beträgt.

---

248

21 Ausgleichsvorgänge

Lösung: Bei der momentanen Behältertemperatur ϑ besteht nach (21.8) und (21.12) zwischen der Abnahme der inneren Energie des Wassers und dem nach außen abfließenden Wärmestrom die Bilanzgleichung cm $( \mathbf { d } \vartheta / \mathbf { d } t ) = k A ( \vartheta _ { \mathrm { a } } - \vartheta )$ . Umgestellt nach dt und beidseitig integriert zwischen den Grenzen $\vartheta = \vartheta _ { 1 }$ zur Zeit $t = 0$ und $\vartheta = \vartheta _ { 2 }$ zur Zeit t, ergibt

$$
t = \frac {c m}{k A} \int_ {\vartheta_ {1}} ^ {\vartheta_ {2}} \frac {\mathrm{d} \vartheta}{\vartheta_ {\mathrm{a}} - \vartheta} = \frac {c m}{k A} \ln \frac {\vartheta_ {1} - \vartheta_ {\mathrm{a}}}{\vartheta_ {2} - \vartheta_ {\mathrm{a}}} = 1 6, 1 \mathrm{h}.
$$

## Aufgabe

**21.1** Berechne den Wärmedurchgangskoeffizienten k einer $l = 3 8$ cm dicken Ziegelwand, deren Wärmeübergangskoeffizienten innen $\alpha _ { 1 } = 6 \mathrm { W } / ( \mathrm { m } ^ { 2 } \cdot \mathrm { K } )$ und außen $\alpha _ { 2 } = 1 8 W /$ $( \mathbf { m } ^ { 2 } \cdot \mathbf { K } )$ betragen und deren Wärmeleitfähigkeit den Wert $\lambda = 0 , 7 \mathrm { W } / ( \mathrm { m } \cdot \mathrm { K } )$ hat! Welche Heizleistung P ist bei einer Außentemperatur von $- 1 0   ^ { \circ } \mathbf { C }$ und einer Wandfläche von $5 0   \mathrm { m } ^ { 2 }$ erforderlich, um eine Zimmertemperatur von $2 0   ^ { \circ } \mathbf { C }$ aufrechtzuerhalten?

## 21.3 Diffusion

Zu den thermisch bedingten Transportphänomenen, wie der Wärmeleitung, gehört auch die Diffusion. Schichtet man ein leichteres Gas (oder eine Flüssigkeit) über ein schwereres (über eine schwerere Flüssigkeit), so durchmischen sich beide im Laufe der Zeit, indem die Molekü- le ineinander diffundieren (vgl. 19.5). Obwohl die Moleküle für sich regellos statistische Bewegungen (komplizierte Zickzackbahnen wie in Bild 18.1) ausführen, so tritt doch insgesamt ein Massenstrom in Richtung geringerer Dichte auf. Diese Diffusion findet auch statt, wenn die Konzentration $c = n / V =$ Stoffmenge/Volumen eines Gases, gemessen in $\mathrm { m o l } / \mathrm { m } ^ { 3 }$ , von Ort zu Ort verschieden ist.

## Diffusion ist ein Massentransport, der Dichte- bzw. Konzentrationsunterschiede von Teilchen durch mikroskopische Bewegung derselben ausgleicht.

Beträgt das Konzentrationsgefälle auf die Entfernung l (bzw. dx bei nichtlinearem Gefälle) gleich $( c _ { 1 } - c _ { 2 } ) / l = \Delta c / l$ bzw. dc/dx, so gilt im stationären Fall für den **Stoffmengenstrom** $I _ { n }$ das zum Wärmeleitungsgesetz (21.2) bzw. (21.7) analoge Gesetz

$$
I _ {n} = \frac {\mathrm{d} n}{\mathrm{d} t} = D \frac {A \Delta c}{l} \quad \text {bzw.} \quad I _ {n} = j _ {n} A; \quad \text {Einheit:} [ I _ {n} ] = 1 \mathrm{mol/s} \tag {21.14}
$$

mit der **Diffusionsstromdichte**

$$
j _ {n} = \frac {\mathrm{d} I _ {n}}{\mathrm{d} A} = - D \frac {\mathrm{d} c}{\mathrm{d} x}; \quad E i n h e i t: [ j _ {n} ] = 1 \mathrm{mol} / (\mathrm{m} ^ {2} \cdot \mathrm{s}) \tag {21.15}
$$

oder – analog zum Wärmeleitungsgesetz (21.7) – vektoriell

$$
\boldsymbol {j} _ {n} = - D \operatorname{grad} c \quad (\textbf {1 . F I C K S c h e s G e s e t z}). \tag {21.16}
$$

Der Proportionalitätsfaktor D heißt **Diffusionskoeffizient**. Dieser hat für Gase einen Wert von etwa $\bar { 1 0 ^ { - 5 } } \mathrm { m } ^ { 2 } / \mathrm { s }$ , für Flüssigkeiten von rund $1 0 ^ { - 1 0 }  { \mathrm { { m } } ^ { 2 } }$ /s und für Festkörper von ca. $1 0 ^ { - 2 0 }   \mathrm { m } ^ { 2 } / \mathrm { s } .$

---

21.3 Diffusion

249

Für die im Allgemeinen orts- und zeitabhängige Konzentration $c = c ( x ,   t )$ gilt die zur Wärmeleitungsgleichung (21.9) analoge eindimensionale Diffusionsgleichung

$$
\frac {\partial c}{\partial t} = D \frac {\partial^ {2} c}{\partial x ^ {2}} \quad (2. \text {FICKsches Gesetz}). \tag {21.17}
$$

Dieses Gesetz folgt aus einer dem Massenerhaltungssatz entsprechenden Bilanzgleichung in Verbindung mit dem 1. FICKschen Gesetz (21.16). Im stationären Fall, d. h. für $\partial c / \partial t = 0$ , ist der Diffusionsstrom (21.14) und somit auch der Konzentrationsunterschied ∆c zeitlich konstant.

Die Diffusionsgleichung (21.17) hat dieselben mathematischen Eigenschaften wie die Wärmeleitungsgleichung (21.9). Demzufolge beschreibt Bild 21.2 auch die örtliche und zeitliche Ausbreitung einer zum Zeitpunkt $t = t _ { 0 }$ bei $x = 0$ konzentrierten Teilchenwolke, wenn man T durch die Konzentration c und die Temperaturleitfähigkeit a durch den Diffusionskoeffizienten $D$ ersetzt. Für die mittlere Entfernung L, bis zu der sich die Teilchenwolke zum Zeitpunkt t durch Diffusion ausgebreitet hat, lässt sich hiernach aus Bild 21.2 sofort die wichtige Beziehung

$$
L = \sqrt {2 D t} \quad (\text {Diffusionsentfernung}) \tag {21.18}
$$

ablesen. Setzt man L gleich der Abmessung des Gebietes mit Konzentrationsunterschieden, so erhält man aus (21.18) die für den Konzentrationsausgleich charakteristische Ausgleichszeit.

Befindet sich das Medium, in dem Diffusion stattfindet, nicht in Ruhe, sondern bewegt es sich mit der allen Teilchen gemeinsamen Driftgeschwindigkeit $\nu ,$ dann überlagert sich dem Diffusionsstrom (21.14) ein **Drift-** oder **Konvektionsstrom** $I _ { n \mathrm { K } } = c \nu A .$ Die gesamte Stromdichte ist dann

$$
j _ {n} = - D \frac {\mathrm{d} c}{\mathrm{d} x} + c v, \quad \text {vektoriell} \quad \boldsymbol {j} _ {n} = - D \operatorname{grad} c + c \boldsymbol {v}. \tag {21.19}
$$

Findet Diffusion unter dem Einfluss äußerer Kräfte statt, z. B. des Schwerefeldes oder eines elektrischen Feldes, dann gilt für die von der Kraft F auf ein Molekül hervorgerufene Driftoder Wanderungsgeschwindigkeit v in Gleichung (21.19) die Beziehung $\nu = \beta F$ . Die sog. Beweglichkeit $\beta$ der Teilchen ist mit dem Diffusionskoeffizienten D durch

$$
\beta = \frac {D}{k T} \quad \text {(EINSTEIN - Beziehung)} \tag {21.20}
$$

verknüpft (k BOLTZMANN-Konstante). Im stationären Zustand kompensieren sich Diffusionsund Driftstrom gerade, so dass sich eine aus der Bedingung $j _ { n } = - D ( { \bf d } c / { \bf d } x ) + c \nu = 0$ folgende stationäre Konzentrationsverteilung $c = c ( x )$ einstellt. Beispiele für einen solchen dynamischen Gleichgewichtszustand sind die Ladungsträgerkonzentration an einem pn-Übergang in Halbleitern (vgl. 46.4) und der Konzentrationsabfall in Gasen oder Lösungen im Schwerefeld (Sedimentation).

Der Wert des Diffusionskoeffizienten D hängt nicht nur von der diffundierenden Komponente ab, sondern auch von der Temperatur sowie vom Stoff (der Matrix), in dem die Diffusion erfolgt. Der Diffusionskoeffizient von Gasen ist über die Beziehung $D = \varLambda \overline { { \nu } } / 3$ mit der mittleren freien Weglänge Λ gemäß der Gleichung (18.29) und der mittleren thermischen Geschwindigkeit $\overline { { \nu } }$ gemäß (18.19) der Gasmoleküle verknüpft. Diffusionsvorgänge in Festkörpern sind über die Beziehung

$$
D = D _ {0} \mathrm{e} ^ {- \frac {E}{k T}} \quad (\text {ARRHENIUS - Gleichung}) \tag {21.21}
$$

---

250

21 Ausgleichsvorgänge

mit $D _ { 0 }$ als einer Konstanten und E als Aktivierungsenergie stark temperaturabhängig. Sie nehmen mit der Temperatur zu. So z. B. kann man eine Legierung durch Glühen homogenisieren. Auch bei Anlauf-, Oxidations- und Verzunderungsvorgängen spielt die Diffusion der Metallatome und ihrer Reaktionspartner eine dominierende Rolle. Einen großen Einfluss haben Diffusionserscheinungen beim Härten und Sintern, bei der Korrosion, Rekristallisation und anderen metallurgischen Prozessen. Von erheblicher Bedeutung sind Diffusionsprozesse auch in vielen anderen Bereichen der stoffwandelnden Industrie sowie bei der Isotopentrennung und bei der Dotierung von Halbleitern.

## Beispiele 21.3:

1. In einem Stahltank von $V = 0 ,   5   \mathrm { m } ^ { 3 }$ Fassungsvermögen, $A = 3   \mathrm { m } ^ { 2 }$ Oberfläche und $l = 2$ mm Wandstärke befindet sich Druckwasserstoff bei $2 5   ^ { \circ } \mathbf { C } .$ a) Wie groß ist der Stoffmengenstrom $I _ { n }$ von Wasserstoff durch die Tankwand infolge von Diffusion, wenn die Wasserstoffkonzentration an der inneren Oberfläche $c _ { 1 } = 1 , 5 \mathrm { k m o l } / \mathrm { m } ^ { 3 }$ , an der äußeren Oberfläche $c _ { 2 } = 0$ und der Diffusionskoeffizient $D = 0 , 3 \cdot 1 0 ^ { - 1 2 }   \mathrm { m } ^ { 2 } / \mathrm { s }$ beträgt? b) Man berechne den Mengenverlust von Wasserstoff und den damit verbundenen Druckabfall nach 24h unter der Voraussetzung, dass das Konzentrationsgefälle für diesen Zeitraum als konstant betrachtet werden kann!

Lösung: a) Aus dem Konzentrationsgefälle auf die Entfernung $l , ( c _ { 1 } - c _ { 2 } ) / l = 7 5 0 \mathrm { k m o l } / \mathrm { m } ^ { 4 }$ , folgt für den Stoffmengenstrom nach dem 1. FICKschen Gesetz (21.14) $I _ { n } = 6 { , } 7 5 \cdot 1 0 ^ { - 1 0 }$ kmol/s.

b) Der Mengenverlust nach $t = 24    h  = 86   400    s$ beträgt $\Delta n = I _ { n } t = 0 { , } 0 5 8 3$ mol. Mit der allgemeinen Zustandsgleichung (16.20) folgt für den damit verbundenen Druckabfall $\Delta p = \Delta n R T / V =$ 289Pa.

2. Berechne die stationäre Konzentrationsverteilung von diffundierenden Teilchen im homogenen Schwerefeld!

Lösung: Der durch die Schwerkraft $F = - \mu g$ (µ Molekülmasse) hervorgerufenen Sinkbewegung mit der Geschwindigkeit $\nu = \beta F = - \beta \mu g$ wirkt der durch das vertikale Konzentrationsgefälle bedingte Diffusionsstrom (21.15) entgegen. Im stationären Zustand gilt mit (21.19)

$$
j _ {n} = - D \frac {\mathrm{d} c}{\mathrm{d} x} - c \beta \mu g = 0 \quad \text {oder} \quad \frac {\mathrm{d} c}{c} = - \frac {\beta \mu g}{D} \mathrm{d} x.
$$

Beidseitig integriert zwischen den Grenzen $c = c _ { 0 }$ für $x = 0$ und c in der Höhe x ergibt

$$
\ln \frac {c}{c _ {0}} = - \frac {\beta \mu g}{D} x \quad \text {oder} \quad c = c _ {0} \mathrm{e} ^ {- \frac {\beta \mu g}{D} x}. \tag {21.22}
$$

Die Konzentration nimmt exponentiell mit der Höhe ab.

## Aufgaben

**21.2** Berechne die Strecke L, um die sich ein Molekül a) in einem Gas, b) in einer Flüssigkeit und c) in einem Festkörper durch Diffusion in 24h von seinem Ausgangsort entfernt! Verwende die auf Seite 244 unten angegebenen Werte der Diffusionskoeffizienten!

**21.3** Leite durch Vergleich der Konzentrationsverteilung (21.22) im obigen Beispiel 21.3/2 mit der für ein ideales Gas aus der barometrischen Höhenformel (14.9) resultierenden Verteilung die EINSTEIN-Beziehung (21.20) $\beta = D / ( k T )$ zwischen Beweglichkeit $\beta$ und Diffusionskoeffizient D her!
