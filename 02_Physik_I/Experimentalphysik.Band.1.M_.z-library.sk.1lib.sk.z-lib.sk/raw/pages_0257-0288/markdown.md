samte Wirbelbewegung der Flüssigkeit, auch für die Zirkulation, da ja gilt (Stokesscher Satz)

$$
\Gamma = \oint_ {C} \vec {v} d \vec {s} = \int_ {A} \mathrm{rot} \vec {v} d \vec {f} = 2 \int_ {A} \vec {\Omega} d \vec {f}. ^ {3 2} \tag {I-4.100}
$$

Der Wirbelvektor $\vec { \Omega } ( \vec { r } )$ ist in idealen Flüssigkeiten als Anfangsbedingung vorgegeben, da er, wie gleich gezeigt wird, in einer idealen Flüssigkeit nicht entstehen kann.

Wir schreiben nochmals die Eulergleichung (I-4.57) unter Verwendung des Satzes aus der Vektoranalysis (in Abschnitt 4.3.5) ohne externe Kräfte an, um nur jene Eigenschaften der Flüssigkeit zu betrachten, die mit der Wirbelbewegung zusammenhängen

$$
\left(\frac {\partial \vec {v}}{\partial t} + (\vec {v} \cdot \vec {\nabla}) \vec {v}\right) = \frac {\partial \vec {v}}{\partial t} + \underbrace {\frac {1}{2} \vec {\nabla} v ^ {2} - \vec {v} \times (\vec {\nabla} \times \vec {v})} _ {= (\vec {v} \cdot \vec {\nabla}) \vec {v}} = - \frac {1}{\rho} \vec {\nabla} P. \tag {I-4.101}
$$

Bilden wir nun die Rotation der Eulergleichung

$$
\underbrace {\operatorname{rot} \left(\frac {\partial \vec {v}}{\partial t}\right)} _ {= \frac {\partial}{\partial t} (\operatorname{rot} \vec {v})} + \underbrace {\operatorname{rot} \left(\frac {1}{2} \vec {\nabla} v ^ {2}\right)} _ {\text {rot grad} \vec {v} ^ {2} \equiv 0} - \underbrace {\operatorname{rot} \left(\vec {v} \times \underbrace {\vec {\nabla} \times \vec {v}} _ {\text {rot} \vec {v} = 2 \Omega}\right)} _ {= \vec {\nabla} \times (\vec {v} \times \operatorname{rot} \vec {v})} = \underbrace {- \operatorname{rot} \left(\frac {1}{\rho} \vec {\nabla} P\right)} _ {\text {rot grad} P \equiv 0} = 0 \tag {I-4.102}
$$

und setzen nach Gl. (I-4.98) für rot $\vec { \upsilon } = 2   \vec { \Omega }$ ein, so folgt als Wirbelgleichung

$$
\frac {\partial \vec {\Omega}}{\partial t} + \vec {\nabla} \times (\vec {\Omega} \times \vec {v}) = 0 \quad \text {Wirbelgleichung.} \tag {I-4.103}
$$

a) ideale Flüssi keit ohne Wirbel ldeale Flussigkeit ohne Wirbel:

Entsprechend dieser Annahme muss gelten (Gl. I-4.98): $\vec { \Omega } = \frac { 1 } { 2 }   \mathrm { { \bf { r o t } } }   \vec { v } = 0 .$ und daher $\frac { \partial \bar { \Omega } } { \partial t } = 0$ , also

## 1 Eine wirbelfreie ideale Flüssigkeit bleibt für alle Zeiten wirbelfrei.

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">32 Auch wenn in einer Strömung rot υ⇀überall verschwindet (ausgenommen an singulären Linien), kann die Zirkulation von Null verschieden sein, nämlich dann, wenn der Integrationsweg eine Singularität umfasst.</span></small>

b) ideale Flüssigkeit mit Wirbeln:

Die Wirbelbewegung wird durch die Sätze von Thomson (William Thomson, später Lord Kelvin (eigentlich Baron Kelvin of Largs), 1824–1907) und Helmholtz (Hermann von Helmholtz, 1821–1894) beschrieben, wobei die Wirbelvektoren $\vec { \Omega }$ als zu einem Zeitpunkt $t _ { 0 }$ vorgegebene Größen aufzufassen sind, also als Anfangsbedingungen.

Ohne Beweis sei hier der Thomsonsche Satz von der Erhaltung der Zirkulation angeführt:

Die Zirkulation Γ längs einer im Laufe der Zeit aus denselben Flüssigkeitsteilchen bestehenden geschlossenen Kurve (‚flüssige Linie‘ <sup>33</sup>) ist zeitlich konstant (konservative äußere Kräfte vorausgesetzt).

Es gilt also: $\frac { d \Gamma } { d t } = 0 \; \Rightarrow \; \Gamma =$ const. für eine flüssige Linie.

Analog zu den Stromlinien können wir im Strömungsfeld der Flüssigkeit Kurven bilden, deren Tangentenrichtung an jedem Ort mit der augenblicklichen Richtung des Wirbelvektors Ω⇀ zusammenfällt, die Wirbellinien.

Eine Wirbelröhre (Abb. I-4.19, siehe auch Abb. I-4.17) ist eine schlauchartige Fläche, die von Wirbellinien gebildet wird. Der flüssige Inhalt aus rotierenden Flüssigkeitsteilchen einer Wirbelröhre heißt Wirbelfaden. Für sehr dünne Wirbelröhren ist Ω⇀ über den Querschnitt A const.

![](images/page_257_image_10.jpg)

<details>
<summary>text_image</summary>

2\u03c9 = rot \u03b7
dA
</details>

Abb. I-4.19: Wirbelröhre (Oberfläche) bzw. Wirbelfaden (flüssiger Inhalt).

Wir bezeichnen als Wirbelstärke (vorticity) $W _ { A }$ in der Fläche A

$$
W _ {A} = \frac {1}{2} \Big | \mathrm{rot}   \vec {\upsilon} _ {A} \Big | \cdot A = \Big | \vec {\Omega} _ {A} \Big | \cdot A = \Omega_ {A} \cdot A, \tag {I-4.104}
$$

das ist der Fluss der Wirbellinien durch den Querschnitt A des Wirbelfadens.

1858 entdeckte Helmholtz aus der Analogie zur Elektrodynamik (Magnetfeld von Strömen) seine Wirbelsätze.

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">33 Eine ‚flüssige Linie‘ bewegt sich mit der Flüssigkeit mit und zerreißt dabei nicht!</span></small>

## 1 Helmholtzsche Wirbelsätze:

$$
\bar {\Omega} = \frac {1}{2} \operatorname{rot} \vec {v} \quad \Rightarrow \underbrace {\operatorname{div} \bar {\Omega}} _ {\substack {\text {Quellergiebigkeit} \\ \text {für den Wirbelvektor}}} = \frac {1}{2} \operatorname{div} \operatorname{rot} \vec {v} \equiv 0. ^ {3 4} \tag{I - 4.105}
$$

Es existieren also weder Quellen noch Senken für die Wirbellinien, die Wirbellinien $/ / \vec { \Omega }$ sind daher stets geschlossene Linien oder reichen bis ins Unendliche oder an die Behälterwand.

2. Die Wirbelstärke $W _ { A } = \Omega \cdot A$ der Wirbelfäden ist in einer idealen Flüssigkeit längs einer Wirbelröhre zeitlich und örtlich konstant. In einer idealen Flüssigkeit können Wirbel also weder entstehen noch vergehen.
3. Jeder Wirbelfaden besteht dauernd aus denselben rotierenden Flüssigkeitsteilchen, da durch seine Mantelfläche keine Wirbellinien ein- oder austreten. Er wandert also mit der Flüssigkeit mit.

In zähen Flüssigkeiten können allerdings Wirbel entstehen, verändert werden und wieder vergehen.

## 4.3.7.2 Reibungsbehaftete (zähe) Flüssigkeiten

In reibungsfreien Flüssigkeiten können also keine Wirbel gebildet werden. Sie sind entweder schon vorhanden oder die Flüssigkeit bleibt wirbelfrei. In Flüssigkeiten mit starker Reibung tritt laminare Strömung auf, das ist eine Strömung, bei der sich die Stromlinien nicht vermischen, also keine Turbulenz auftritt. Die Bildung von Wirbeln geschieht dagegen in Flüssigkeiten mit kleiner Reibung an jenen Stellen, an denen der Geschwindigkeitsgradient besonders groß ist, d. h. an <u>Wänden und Hindernissen</u>. Die großen Geschwindigkeitsgradienten führen zu starken Tangentialkräften zwischen benachbarten Flüssigkeitsschichten und auf diese Weise zur Bildung von makroskopischen Wirbeln.

## a) Laminare (= ‚schlichte‘) Strömung

Die Flüssigkeit kann in glatte Schichten zerlegt werden, die mit differentiell steigender Geschwindigkeit aneinander vorbei gleiten. Gleichmäßige Strömung ohne Turbulenz und makroskopische Wirbelbildung ist zu erwarten, wenn die Reibungs-

$$
\text {div rot} \vec {v} = \underbrace {\vec {\nabla} \cdot (\vec {\nabla} \times \vec {v})} _ {\text {, Spatprodukt} ^ {*}} = \left| \begin{array}{c c c} \frac {\partial}{\partial x} & \frac {\partial}{\partial y} & \frac {\partial}{\partial z} \\ \frac {\partial}{\partial x} & \frac {\partial}{\partial y} & \frac {\partial}{\partial z} \\ v _ {x} & v _ {y} & v _ {z} \end{array} \right| \equiv 0, \text {denn eine Determinante verschwindet, wenn zwei}
$$

Zeilen gleich sind.

kräfte zwischen den Flüssigkeitsmolekülen groß gegen die beschleunigenden Kräfte sind, d. h. bei kleinen Strömungsgeschwindigkeiten. Im einfachsten Fall gleiten parallele Flüssigkeitsschichten mit gleicher Strömungsrichtung aneinander vorbei. Durch die inneren Reibungskräfte übt die schneller fließende Schicht auf die angrenzende eine Beschleunigung aus (Reibungskräfte $\propto \nu )$ , indem sie diese mitzunehmen versucht, während die langsamere Schicht die schnellere hemmt. Nach Newton ist diese in bewegten, zähen Flüssigkeiten auftretende Scherspannung proportional zur Fläche A der sich berührenden Schichten und der Änderung der Strömungsgeschwindigkeit senkrecht zur Strömung $\left( \tau \propto \frac { \partial \upsilon _ { x } } { \partial z } \right)$

Wir betrachten den einfachen Fall einer zähen Flüssigkeit, die horizontal, parallel zur x-Achse strömt und deren Geschwindigkeit sich in Richtung der $z - \mathbf { A }$ chse verändert. Für die Scherspannung gilt dann

$$
\vec {F} _ {\text {Reibung}} = \eta \cdot A \cdot \frac {d \vec {v}}{d z}. ^ {3 5} \tag {I-4.106}
$$

Die Reibungskraft hat hier die Richtung der positiven $x - A$ chse.

$\eta$ ist wieder der Koeffizient der dynamischen Zähigkeit (Viskosität).

Laminare Strömung bildet sich $\mathbf { z } , \mathbf { B } ,$ bei langsamem Durchfluss zäher Flüssigkeiten durch Rohre mit kreisförmigem Querschnitt aus. An der Rohrwand haftet die Flüssigkeit, die Geschwindigkeit nimmt daher zur Rohrachse hin zu, $\frac { d \nu } { d r }$ <sub>ist</sub> daher negativ (Abb. I-4.20), für $r = 0$ ist $\nu = \nu _ { \mathrm { m a x } }$

![](images/page_259_image_8.jpg)

<details>
<summary>text_image</summary>

r
\bar{v} = \frac{1}{2} v_{max}
P_1
P_2
x
l
</details>

Abb. I-4.20: Laminare Strömung einer langsam fließenden, zähen Flüssigkeit durch ein Rohr mit kreisförmigem Querschnitt.

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">35 Um die Reibungskraft auf ein Volumenelement dV = dx⋅dy⋅dz zu berechnen multipliziert man gemäß der bewährten ‚Viskositätshypothese‘ die Komponenten des Tensors der Deformationsgeschwindigkeit mit 2 η. Dadurch ergibt sich der Tensor der Reibungsspannungen. Durch Umrechnung der Oberflächenkräfte auf Volumenskräfte erhält man schließlich die weiter oben (Abschnitt 4.3.2, Gl. I-4.58) für die Navier-Stokes-Gleichung (I-4.59) verwendete Beziehung ΔF⇀Reibung = η⋅Δυ⇀ΔV.</span></small>

Es bildet sich ein parabolisches Strömungsprofil aus und für den Flüssigkeitsstrom $I = \frac{V}{t} \left( = \mathrm{pro} \right)$ Zeiteinheit durch ein Rohr strömende Flüssigkeitsmenge) gilt das Hagen-Poiseuillesche Gesetz (nach dem Ingenieur Gotthilf Heinrich Ludwig Hagen, 1797–1884 und dem Arzt Jean Louis Marie Poiseuille, 1797–1869):

$$
I = \frac {\pi \cdot R ^ {4}}{8 \eta} \cdot \frac {\Delta P}{l} \quad \text {Hagen - Poiseuillesche Gesetz.} \tag {I-4.107}
$$

Dabei ist R der Rohrradius, l die Rohrlänge, $\Delta P$ die Druckdifferenz und $\eta$ die dynamische Zähigkeit.<sup>36</sup>

Die durch ein Rohr strömende Flüssigkeitsmenge ist also zur vierten Potenz des Rohrradius proportional, jeder Millimeter zählt!

## Beispiel: Der menschliche Blutkreislauf.

Dass die in Rohrsystemen strömende Flüssigkeitsmenge zur vierten Potenz des Rohrradius proportional ist, hat auch eine Bedeutung für den Blutkreislauf unseres Körpers: Die Regulation der Blutzirkulation erfolgt durch Variation des Kapillardurchmessers. Bei Muskelbetätigung z. B. erfolgt eine Erweiterung der Kapillaradern und den Blutspeichern Milz und Leber wird Blut entzogen und an die Orte des Verbrauchs geführt. Unser Kapillarsystem hat eine Länge von ca. $1 0 ^ { 5 }$ km, das entspricht etwa dem 2,5-fachen Erdumfang. Der Kapillardurchmesser liegt zwischen $5   \mu \mathrm { m }$ und $3 0   \mu \mathrm { m }$ das Gesamtvolumen des Kapillarsystems ist aber größer als das Blutvolumen von ca. 5 l, da nicht alle Körperregionen gleichzeitig gleichstark mit Blut gefüllt sind.

Mit einer mittleren Strömungsgeschwindigkeit υ̅ kann man für den Flüssigkeitsstrom $I = \bar { \boldsymbol { \upsilon } } \cdot \boldsymbol { R } ^ { 2 } \pi$ setzen und erhält für die Kraft auf die Rohrwand pro Längeneinheit mit Gl. (I-4.107)

$$
\frac {F}{l} = \frac {\Delta P \cdot R ^ {2} \pi}{l} = 8 \eta \cdot \frac {\bar {\nu} \cdot R ^ {2} \pi \cdot R ^ {2} \pi}{\pi R ^ {4}} = 8 \pi \eta \bar {\nu}. \tag {I-4.108}
$$

Mit Hilfe der Navier-Stokes Gleichung (I-4.59) und einigem mathematischen Aufwand lässt sich der Reibungswiderstand einer Kugel vom Radius $r ,$ die sich mit der konstanten Geschwindigkeit υ durch eine zähe Flüssigkeit bewegt, näherungsweise berechnen:

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">36 Bei genauerer Betrachtung stellt sich heraus, dass der Wirbelvektor Ω⇀ bei der Strömung durch ein horizontales Rohr nicht verschwindet, sondern dass die strömende Flüssigkeit aus geschlossenen Wirbelringen besteht, die normal zur Ausbreitungsrichtung liegen. Diese Rotationsbewegung der Flüssigkeitsteilchen führt zusammen mit der Verzerrungsbewegung zu dem Geschwindigkeitsfeld mit geraden Stromlinien.</span></small>

$$
\vec {F} _ {r} = - 6 \pi \eta r \vec {v} \quad \text {Stokessches Widerstandsgesetz.} \tag {I-4.109}
$$

Anwendungen dieses Gesetzes (nach Sir George Gabriel Stokes, 1819–1903, irischer Mathematiker und Physiker) finden sich in der Bewegung von Aerosolen (Schwebeteilchen in der Luft) und z. B. von Öltröpfchen bei der Bestimmung der Elementarladung mit der Millikan-Methode (siehe Band III, Kapitel „Elektrostatik“, Abschnitt 1.1.2).

## b) Turbulenz, Reynoldssche Zahl

Wenn die Strömungsgeschwindigkeit einen kritischen Wert übersteigt, reicht der dämpfende Einfluss der Reibung nicht mehr aus und es kommt zur Vermischung der Stromlinien und zur Wirbelbildung, also zur Turbulenz.

Turbulente Strömung ist folgendermaßen charakterisiert:

die Ausströmgeschwindigkeit ist nicht mehr proportional zur Druckdifferenz, sondern wächst langsamer an;
die Werte für Strömungsgeschwindigkeit und Druck an einem bestimmten Ort sind zeitlich nicht konstant, sondern schwanken um einen Mittelwert;
die Bahnen der einzelnen Teilchen verlaufen nicht mehr geradlinig, es kommt zu einer Vermischung der Teilchenbahnen.

Offensichtlich kann die Position eines Flüssigkeitsteilchens in diesem Fall nicht mehr vorausgesagt werden. Dies ist eine Folge der Nichtlinearität der Eulerschen Bewegungsgleichung, also eine Folge der nichtlinearen Dynamik (siehe Band II, Kapitel „Nichtlineare Dynamik und Chaos“).

Der zu erwartende Strömungszustand einer Flüssigkeit, laminar oder turbulent, wird durch eine charakteristische, dimensionslose Größe, die Reynoldssche Zahl (nach dem britischen Physiker Osborne Reynolds, 1842–1912) bestimmt, die durch das Verhältnis der Beschleunigungsarbeit (kinetische Energie) zur Reibungsarbeit gegeben ist:

$$
\begin{array}{l} R e = \frac {\text {Beschleunigungsarbeit}}{\text {Reibungsarbeit}} = \frac {\text {Beschleunigungskraft}}{\text {Reibungskraft}} = \frac {m \cdot a}{\eta \cdot \frac {v}{l} A} = \\ = \frac {\rho l ^ {3} \cdot \frac {l}{t ^ {2}}}{\eta \cdot \frac {l}{l t} \cdot l ^ {2}} = \frac {\rho l ^ {2}}{\eta t} = \frac {\rho l v}{\eta} = R e \\ \end{array}
$$

$$
R e = \frac {l \cdot \rho \cdot v}{\eta} \quad R e y n o l d s s c h e Z a h l. \tag {I-4.110}
$$

Dabei ist l der Rohrdurchmesser oder eine gewählte charakteristische Länge (z. B. Flügeltiefe) eines umströmten Hindernisses, $\rho$ die Flüssigkeitsdichte, υ die Strö- mungsgeschwindigkeit und $\eta$ die Zähigkeit der Flüssigkeit.

Kleines Re bedeutet starke Reibung und es ergibt sich laminare Strömung, großes Re bedeutet Überwiegen der kinetischen Energie und damit Turbulenz und Wirbelbildung. Für den Umschlag von laminarer zu turbulenter Strömung gibt es eine relativ scharfe untere Grenze von Re. Diese kritische Reynoldszahl $R e ^ { \mathrm { k r i t } }$ hat je nach Geometrie des um- oder durchströmten Körpers einen experimentell zu bestimmenden Wert. Beim Durchströmen von Rohren liegt er zwischen 1000 und 2000. In glatten Rohren gilt $R e ^ { \mathrm { k r i t } } = 1 1 6 0$ . Für das Umströmen von Flügelprofilen oder Schiffskörpern gilt andererseits $R e ^ { ^ { \mathrm { k r i t } } }   \approx 1 0 ^ { ^ 6 }$

Die Reynoldssche Zahl hat eine entscheidende Bedeutung bei der Ausführung von Strömungsmessungen an Modellen in Windkanälen. Die Strömungsformen von Original und Modell sind nur dann ähnlich, wenn das Verhältnis von Trägheitskraft zu Reibungskraft, also die Reynoldszahl, in beiden Fällen gleich ist.

## 4.3.8 Oberflächenspannung und Kapillarität

Wie wir gesehen haben, zeigen reale Flüssigkeiten als Folge der Wechselwirkung ihrer Moleküle untereinander und mit den Molekülen anderer Stoffe (z. B. Gefäß- oder Rohrwand) eine „innere“ Reibung, die zur Viskosität der Flüssigkeit führt (siehe Abschnitt 4.3.2, Gl. I-4.58 und Abschnitt 4.3.7.2). Diese molekularen Wechselwir kungen (siehe dazu auch den Abschnitt über die chemischen Bindungen in Band VI, Kapitel „Festkörperphysik“, Abschnitt 2.1) werden unter den Begriffen Kohä- sion<sup>37</sup> und Adhäsion<sup>38</sup> zusammengefasst. Unter Kohäsion versteht man die attraktive Wechselwirkung<sup>39</sup> zwischen den Molekülen eines Fluids, die mit der Entfernung rasch abnehmen und daher im gasförmigen Zustand vernachlässigbar sind. Die Adhäsion beschreibt den mechanischen Zusammenhalt an einer Grenzschicht zwischen Flüssigkeiten und Feststoffen oder auch zwischen zwei unterschiedlichen Flüssigkeiten (z. B. $\mathrm { H } _ { 2 } \mathrm { O } / \mathrm { H g } )$ , die durch molekulare Wechselwirkungen zwischen den Molekü- len dieser beiden Substanzen in der Grenzflächenschicht hervorgerufen wird.

## 4.3.8.1 Spezifische Oberflächenenergie, spezifische Grenzflächenenergie, Oberflächenspannung, Grenzflächenspannung

Die Moleküle an der Oberfläche einer Flüssigkeit oder eines Festkörpers, die an Vakuum oder ein Gas (z. B. Luft) grenzen, erfahren aus der äußeren Hälfte der

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">37 Nach lat. cohaerere: zusammenhängen.</span></small>

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">38 Nach lat. adhaerere: anhaften.</span></small>

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">39 Diese Wechselwirkungen sind elektrischer Natur, die Massenanziehung ist im atomaren und molekularen Bereich vernachlässigbar. Im astronomischen Bereich sind dagegen die elektrischen Wechselwirkungen elektrisch neutraler Teilchen, z. B. von Molekülen, (van der Waals WW ∝ r<sup>−6</sup>, siehe Band VI, Kapitel „Festkörperphysik“, Abschnitt 2.1.1.3) wegen der hier riesigen interatomaren Abstände gegen die Massenanziehung zu vernachlässigen.</span></small>

Wirkungssphäre der Molekularkräfte (van der Waals Kräfte mit $E _ { \mathrm { p o t } } \propto r ^ { - 6 } ,$ , siehe Band VI, Kapitel „Festkörperphysik“, Abschnitt 2.1.1.3) von ca. 100 Moleküldurchmessern praktisch keine Anziehungskräfte, sodass auf jedes Oberflächenmolekül ein Zug nach innen resultiert. Um also ein Molekül vom Inneren an die Oberfläche zu bringen, ist gegen diesen Zug eine reversible Arbeit aufzuwenden. Die Oberflä- che ist daher Sitz von potenzieller Energie, die pro Flächeneinheit als spezifische Oberflächenenergie<sup>40</sup> (specific surface energy = surface free energy), σ bezeichnet wird.<sup>41</sup>

Einheit der spezifischen Oberflächenenergie σ: $[ \sigma ] = \mathrm { J m } ^ { - 2 } = \mathrm { N m } ^ { - 1 }$ . Als „praktische“ Einheit, die handlichere Zahlen ergibt, wird 10 $^{-3}\mathrm{~Jm}^{-2}=10^{-3}\mathrm{~Nm}^{-1}$ verwendet. σ ist – unabhängig von der Gestalt der Oberfläche – eine für jede Substanz positive, temperaturabhängige Größe.

<table><tr><td colspan="2">Werte von  $\sigma$  in  $10^{-3}$  Jm $^{-2}$ </td><td colspan="2">bei  $T$ </td></tr><tr><td>Wasser</td><td>72,82</td><td>20 °C</td><td></td></tr><tr><td>Schwefelkohlenstoff</td><td>32,4</td><td>20 °C</td><td></td></tr><tr><td>Essigsäure</td><td>27,7</td><td>20 °C</td><td></td></tr><tr><td>Tetrachlorkohlenstoff</td><td>26,7</td><td>20 °C</td><td></td></tr><tr><td>Benzol</td><td>29,2</td><td>20 °C</td><td></td></tr><tr><td>Mineralöl</td><td>36</td><td>20 °C</td><td></td></tr><tr><td>Quecksilber</td><td>474</td><td>20 °C</td><td></td></tr><tr><td>Glas</td><td>300–500</td><td>20 °C</td><td></td></tr><tr><td>Acrylglas (= Plexiglas)</td><td>36</td><td>20 °C</td><td></td></tr><tr><td>Teflon</td><td>18–20</td><td>20 °C</td><td></td></tr><tr><td>Aluminium</td><td>1140 ± 200</td><td>200 °C</td><td>fest</td></tr><tr><td>Kupfer</td><td>1710 ± 100</td><td>1000 °C</td><td>fest</td></tr><tr><td>Eisen</td><td>2150 ± 320</td><td>1380 °C</td><td>fest</td></tr><tr><td>Stahl</td><td>29–50</td><td>20 °C</td><td>fest</td></tr></table>

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">40 Thermodynamisch exakt: spezifische freie Oberflächenenthalpie, das ist die Arbeit, die erforderlich ist, um reversibel bei konstantem Druck und konstanter Temperatur die Oberfläche A = 1 m zu erzeugen.</span></small>

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">41 Ein Schnitt senkrecht zur Oberfläche zeigt, dass auf dieser an beiden Seiten des Schnitts Moleküle vorhanden sind (etwa halb so viele wie im Inneren), die einen Zusammenhalt (eine Normalspannung als Zug- oder Druckspannung) parallel zur Oberfläche bewirken, der sich als Oberflächenspannung bemerkbar macht. In zur Oberfläche senkrechter Richtung fehlen den unmittelbaren Oberflächenmolekülen ihre „molekularen Partner“, sodass in dieser Richtung keine Normalspannung vorhanden ist – sie wächst aber nach innen bis zum Verschwinden der Grenzschicht in einer Tiefe von ca. 100 Moleküldurchmessern an. Die Kraftwirkung auf ein Molekül in der Oberflächenschicht ist also – im Gegensatz zum Flüssigkeitsinneren – richtungsabhängig; die Normalspannung in der Flüssigkeits oberfläche ist ein zweistufiger Tensor mit zwei ungleichen Hauptwerten (Diagonalelement nach Hauptachsentransformation), im Inneren der Flüssigkeit sind die Hauptwerte gleich, das Tensorellip soid wird zur Kugel. Im Gegensatz zu elastischen Membranen (z. B. aus Gummi) ändert sich die Oberflächenspannung bei einer Verzerrung nicht! Allerdings wird dann der Krümmungsdruck (siehe Ab schnitt 4.3.8.2) wichtig (vgl. einen Wasserläufer auf der Wasseroberfläche).</span></small>

![](images/page_264_image_2.jpg)

<details>
<summary>text_image</summary>

G
L
A
B
L
h
F
Lamelle (Fläche A)
Flüssigkeitsoberfläche
Flüssigkeit
</details>

Abb. I-4.21: Drahtbügelmethode nach Lenard zur Messung der spezifischen Oberflächenenergie von Flüssigkeiten.

Die Werte von $\sigma$ für feste Stoffe schwanken erheblich wegen unterschiedlicher Reinheit und Bearbeitung der Oberfläche.

σ von Flüssigkeiten kann z. B. nach Lenard<sup>42</sup> mit Hilfe einer Waage aus der Zugkraft F einer Lamelle ermittelt werden, die an einem dünnen $\left( \emptyset \approx 5   \mu \mathrm { m } \right)$ horizontalen Drahtstück AB der Länge L (≈ 4 cm) hängt. Das Drahtstück ist in einem rechteckigen Rahmen fest montiert (Gesamtgewicht eingetaucht: G), der nach dem Eintauchen in die Flüssigkeit etwas hochgezogen wird (Abb. I-4.21). Es gilt (vgl. weiter unten Gl. I-4.116)

$$
\sigma = \frac {F}{2 L}, ^ {4 3} \tag {I-4.111}
$$

da die Lamelle ja zwei Oberflächen besitzt.<sup>44</sup> Einheit von $\sigma : [ \sigma ] = \mathrm { J } \mathrm { m } ^ { - 2 } = \mathrm { N } \mathrm { m } ^ { - 1 }$ . Für die Zugkraft F gilt:

$$
F = G (\text {mit Lamelle}) - \left[ G (\text {ohne Lamelle} + \text {Lamellengewicht} ^ {4 5}) \right]. \tag {I-4.112}
$$

Grenzen zwei kondensierte Phasen α und $\beta$ aneinander, dann ist auch in diesem Fall die Trennfläche Sitz potenzieller Energie, die jetzt von den beiden Stoffen α und $\beta$ abhängt und pro Flächeneinheit als spezifische Grenzflächenenergie $\sigma _ { \alpha \beta }$ bezeichnet wird (Einheit wieder $[ \sigma _ { \alpha \beta } ] = \mathrm { J } \mathfrak { m } ^ { - 2 } )$ . Auch hier (siehe Fußnote 34) folgt wieder für den Rand der Grenzfläche eine einwärts wirkende, die Grenzfläche zu verkleinern suchende Grenzflächenspannung $F _ { C } ^ { \alpha \beta } = \sigma _ { \alpha \beta }$ mit $\left[ F _ { C } ^ { \alpha \beta } \right] = \mathrm { J m } ^ { - 2 } = \mathrm { N m } ^ { - 1 }$ Sie ist immer kleiner als die größere der beiden kombinierenden Oberflächenspannungen.

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">42 Philipp Eduard Anton Lenard, 1862–1947, österreichisch-ungarischer Physiker; für seine Arbeiten über Kathodenstrahlen erhielt er 1905 den Nobelpreis.</span></small>

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">43 Für ein Linienelement dL⇀ einer gekrümmten Berandung gilt für die wirkende Zugkraft dF⇀= 2 σ (dL⇀× n⇀σ), wobei n⇀σ den Einheitsvektor der Oberflächennormale bedeutet.</span></small>

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">44 Wenn der Bügel bis zur Höhe h über die Flüssigkeitsoberfläche gehoben wird, ist die verrichtete F Arbeit W = F ⋅h = σ⋅2 A = σ⋅2 Lh ⇒ σ = (F ist ja unabhängig von A, also auch von h, vgl. 2 L Fußnote 33).</span></small>

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">45 Dieses kann vernachlässigt werden, wenn man – wie üblich – kurz vor dem Abreißen der Lamelle misst, wenn sie schon extrem dünn ist.</span></small>

**Anmerkung:** Die spezifische Grenzflächenenergie $\sigma _ { \alpha \beta }$ hat in der Festkörper- und Materialphysik eine große Bedeutung, da die technisch wichtigen Werkstoffe ein mehrphasiges Gefüge besitzen, also Ausscheidungen (precipitates, „Teilchen“) enthalten, die eine sehr große innere Oberfläche darstellen (siehe Band VI, Kapitel „Festkörperphysik“, Abschnitt 2.2.6.4). Damit ist eine große innere Energie verbunden, die bei genügend hoher Temperatur – beim Einsetzen der Atomdiffusion – dadurch abgebaut wird, dass durch Diffusionsprozesse die „Teilchen“ wachsen, ihre Anzahl aber entsprechend verkleinert wird, wodurch die innere Oberfläche und damit auch die innere Energie abnehmen. Dieser Prozess wird als Vergröbe rung bezeichnet – er ist meist unerwünscht, da er zu einer Entfestigung der Werk stoffe führen kann.

**Beispiel:** Spreitung (spreading), Benetzung, Nichtbenetzung.

Ein Flüssigkeitstropfen $( \sigma _ { F l } )$ wird im Schwerefeld auf eine ebene, horizontale Platte $( \sigma _ { F l , f e s t } )$ gebracht; die Grenzflächenenergie zwischen Flüssigkeit und Platte ist $\sigma _ { F l , f e s t }$ Längs der aus Symmetriegründen kreisförmigen Begrenzungslinie bildet sich im Kräftegleichgewicht ein Randwinkel $\theta$ aus, dessen Größe zur Einteilung der Erscheinungen dient.

$$
\theta = 0
$$

$$
\begin{array}{c} \text {Spreitung} \\ = \text {vollständige Benetzung} \\ \text {Beispiel: Wasser auf Glas} \end{array}
$$

$$
0 <   \theta \leq 9 0^\circ
$$

$$
\text{Benetzung}
$$

$$
90^\circ <  \theta \leq 180^\circ
$$

$$
\text {Nichtbenetzung}
$$

$$
\begin{array}{l} \text {z.B.: Mineralöl auf Stahl} \\ \text {oder Plexiglas} \end{array}
$$

$$
\text {z.B. Quecksilber auf Glas}
$$

![](images/page_265_image_14.jpg)

<details>
<summary>text_image</summary>

Flüssigkeit (σFl)
Feststoff (σfest)
</details>

![](images/page_265_image_15.jpg)

<details>
<summary>text_image</summary>

σ_fest
σ_Fl
θ
σ_Fl, fest
</details>

![](images/page_265_image_16.jpg)

<details>
<summary>text_image</summary>

σFl
θ
σfest
σFl, fest
</details>

Es gilt (vgl. z. B. mittleres Bild):

$$
\sigma_ {f e s t} = \sigma_ {F l, f e s t} + \sigma_ {F l} \cos \theta
$$

$$
\text {Youngsche Gleichung,}
$$

(nach Thomas Young 1773–1829, englischer Augenarzt und Physiker).

Es folgt, dass für $\sigma _ { f e s t } > \sigma _ { F l } + \sigma _ { F l , f e s t }$ kein Gleichgewicht längs der Randlinie möglich ist und die Flüssigkeit bis zu einer monomolekuaren Schicht auseinandergezogen wird (Spreitung) mit $\theta = 0$

Der Randwinkel θ ist die bestimmende Größe für die in allen Lebensbereichen wichtige Kapillarität (siehe Abschnitt 4.3.8.3). Für große Tropfen nimmt die Oberfläche in genügender Entfernung von der Randkurve die Gestalt einer horizontalen Ebene als Äquipotenzialfläche im Schwerefeld an.

Betrachtet man eine Flüssigkeitsmenge, die keinen äußeren Kräften unterworfen ist, so nimmt diese die Form einer Kugel an, da sie in diesem Fall die kleinste mögliche Oberfläche, also die geringste potenzielle Energie besitzt. Ein Beispiel dafür sind fallende Wassertropfen. Die potenzielle Energie der Flüssigkeitsmenge enthält daher einen Anteil, der zur Oberfläche und einen Anteil, der zum Volumen proportional ist. Die Oberflächenenergie wird umso wichtiger, je kleiner das Volumen, also je kleiner die betrachtete Flüssigkeitsmenge ist. Für die Oberflächenenergie einer beliebigen Fläche A können wir also ansetzen:

$$
E _ {\mathrm{pot}} ^ {O} = \sigma \cdot A. \tag {I-4.113}
$$

Die Proportionalitätskonstante $\sigma$ ist die spezifische Oberflächenenergie (siehe Fuß- note 33) mit der Einheit $[ \sigma ] = \mathrm { J } \mathfrak { m } ^ { - 2 }$

Wir wollen jetzt zeigen, dass aufgrund der Oberflächenenergie (bzw. der Grenzflächenenergie) längs eines beliebigen Randes einer ebenen Oberfläche (Grenzflä- che) eine konstante Zugkraft pro Längeneinheit ${ \vec { F } } _ { C }$ normal zur Randkurve wirkt. Dazu grenzen wir auf einer Flüssigkeitsoberfläche ein Stück ab, das durch die geschlossene Kurve C begrenzt wird. Bei einer Vergrößerung der Oberfläche geht diese Kurve C in C′ über (Abb. I-4.22).

![](images/page_266_image_7.jpg)

<details>
<summary>text_image</summary>

δn
ds
Fc ds
C
δA
C'
</details>

Abb. I-4.22: Vergrößerung eines Stücks der ebenen Flüssigkeitsoberfläche. Die Randkurve C geht in C′ über.

Die Arbeit, die zur Vergrößerung der Oberfläche durch die differentielle senkrechte Verschiebung δn⇀von C notwendig ist, muss gegen eine Kraft pro Längeneinheit ${ \vec { F } } _ { C }$ verrichtet werden, die entlang der Randkurve Csenkrecht zu dieser angreift und die Oberfläche aus energetischen Gründen zu verkleinern sucht (Einheit: $[ F _ { C } ] = \mathrm { N m } ^ { - 1 }$ Verschiebt man ein Linienelement ds der Randkurve um $\delta \vec { n }$ in der Oberfläche in Richtung der Normalen von $C ,$ so beträgt die gesamte zur Verschiebung von C verrichtete Arbeit δW

$$
\delta W = \oint_ {C} F _ {C} d s \delta n \tag {I-4.114}
$$

mit $\vec { F } _ { C } / /   \delta \vec { n }$ . Diese Arbeit steckt im Oberflächenzuwachs $\delta A = \oint _ { C } d s d n$ mit $d \vec { s } \perp \delta \vec { n }$ als potenzielle Energie. Daraus folgt

$$
\delta W = \oint_ {C} \sigma d s d n. \tag {I-4.115}
$$

Die beiden Beziehungen Gl. (I-4.114) und Gl. (I-4.115) für δW gelten für alle Kurven C. Daher folgt

$$
\underline {{F _ {C} = \sigma}}. ^ {4 6} \tag {I-4.116}
$$

Ebenso wie $\sigma$ ist auch $F _ { C }$ eine längs der Kurve C konstante Größe, die nicht von der Ausdehnung der umrandeten Fläche A abhängt.

Die Randspannung $F _ { C }$ (Kraft pro Längeneinheit) längs der Begrenzungslinie C der Oberfläche A ist also numerisch der spezifischen Oberflächenenergie σ gleich; daher wird $\sigma$ auch als Oberflächenspannung bezeichnet und synonym zu spezifische Oberflächenenergie verwendet. Die Oberflächenspannung ist also (auch) eine Kraft pro Längeneinheit (Einheit: $[ F _ { C } ] = \mathrm { N m } ^ { - 1 }$ .

## 4.3.8.2 Normaldruck gekrümmter Oberflächen

Betrachten wir zunächst eine zylindrische, also einfach gekrümmte Oberfläche und die Kräfte, die an einem Flächenelement $d s _ { 1 } d s _ { 2 }$ angreifen, das von zwei Mantellinien $( d s _ { 1 } )$ und von zwei dazu senkrechten Kurven $( d s _ { 2 } )$ begrenzt wird (Abb. I-4.23).

Die Kräfte, die an den beiden Linienelementen $d s _ { 2 }$ angreifen, liegen in der Oberfläche parallel zu den Mantellinien. Sie erzeugen daher keine Kraft senkrecht zur Oberfläche. Die an den Linienelementen $d s _ { 1 }$ angreifenden Kräfte schließen dagegen den Winkel dφ miteinander ein und erzeugen daher für kleine Winkel dφ die Kraft $d F _ { 1 } = 2 F _ { C } d s _ { 1 }$ sin $\frac { d \varphi } { 2 } = F _ { C } d s _ { 1 } d \varphi .$ . Ist $R _ { 1 }$ der Krümmungsradius der zylindrischen Oberfläche, so gilt mit $d \varphi = { \frac { d s _ { 2 } } { R _ { 1 } } }$

$$
d F _ {1} = F _ {C} \frac {d s _ {1} d s _ {2}}{R _ {1}} = \frac {F _ {C} d A}{R _ {1}} = \frac {\sigma d A}{R _ {1}} \tag {I-4.117}
$$

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">46 Diese Gleichung wurde bereits bei der Besprechung der Drahtbügelmethode verwendet (Gl. I-4.111).</span></small>

![](images/page_268_image_2.jpg)

<details>
<summary>text_image</summary>

Fcds₁
Fcds₂
R₁
dφ
ds₂
dF₁
dF
Fcds₁
ds₁
dA
dφ
</details>

Abb. I-4.23: Zur Ableitung des Krümmungsdrucks.

und damit für den Druck („Krümmungsdruck“)

$$
P _ {1} = \frac {d F _ {1}}{d A} = \frac {\sigma}{R _ {1}}. \tag {I-4.118}
$$

Im Falle einer doppelt gekrümmten Fläche wird das Flächenelement durch zwei Paare benachbarter Hauptkrümmungslinien begrenzt. Da die beiden Hauptkrümmungslinienpaare aufeinander normal stehen, kann die obige Betrachtung einer zylindrische Oberfläche für jedes das Flächenelement begrenzende Linienpaar durchgeführt werden und die sich ergebende, gesamte Kraft normal zum Flächenelement wird

$$
d F = \sigma \Bigg (\frac {1}{R _ {1}} + \frac {1}{R _ {2}} \Bigg) d A. \tag {I-4.119}
$$

Damit ergibt sich für den Normaldruck

$$
P = \sigma \left(\frac {1}{R _ {1}} + \frac {1}{R _ {2}}\right). \tag {I-4.120}
$$

$R _ { 1 }$ und $R _ { 2 } ,$ die beiden Hauptkrümmungsradien, sind positiv zu nehmen, wenn der Krümmungsmittelpunkt im Inneren der Flüssigkeit liegt. Die Krümmungsdruckkraft weist immer von der konkaven Seite der Oberfläche weg.

Flüssigkeitslamellen, z. B. eine Seifenblase, bestehen aus zwei eng benachbarten parallelen Oberflächen. Sind keine äußeren Kräfte vorhanden (Vernachlässigung der Schwerkraft), dann nimmt jeder Tropfen und auch die Blase aus Symmetriegründen Kugelgestalt an. Für eine Seifenblase gilt daher $R _ { 1 } = R _ { 2 } = R$ und es herrscht im Inneren der Druck

$$
P = 2 \sigma \left(\frac {1}{R} + \frac {1}{R}\right) = \frac {4 \sigma}{R}. ^ {4 7} \tag {I-4.121}
$$

Für einen Flüssigkeitstropfen mit nur einer Oberflächenschicht gilt

$$
P = \frac {2 \sigma}{R}. \tag {I-4.122}
$$

Sind die Tröpfchen sehr klein (Nebel), dann wird der Innendruck P und mit ihm auch der Dampfdruck $P _ { D }$ groß (siehe dazu Band II, Kapitel „Physik der Wärme“, Abschnitt 1.3.3.1). Für $\mathrm { H } _ { 2 } \mathrm { O }$ wird bei 2 R = 1 μm der Innendruck $P = 2.92    bar  =$ $2.92 \cdot 10^{5}   Pa  = 292   kPa$ und bei $T   =   2 0 \; ^ { \circ } \mathrm { C }$ der Dampfdruck $P_{D}=2,95P_{D,0}\left ( P_{D,0}= \right.$ Dampfdruck bei $T = 2 0 ~ ^ { \circ } \mathrm { C }$ und P = 1 bar), was für die Keimbildung von Bedeutung ist.<sup>48</sup>

Für begrenzte Flüssigkeitslamellen (z. B. innerhalb eines beliebig verbogenen Drahtringes ausgespannt) ist der Druck auf beiden Seiten der Lamelle gleich und somit die Druckdifferenz in jedem Punkt der Fläche gleich Null, also $P = \sigma \left( \frac { 1 } { R _ { 1 } } + \frac { 1 } { R _ { 2 } } \right) = 0 .$ . Daraus folgt unmittelbar $R _ { 1 } = - R _ { 2 }$ . Eine derartige Fläche heißt Minimalfläche, sie besteht nur aus Sattelpunkten.

## 4.3.8.3 Kapillarität

In der Praxis wird eine Flüssigkeit meist von einer Gefäßwand begrenzt, die aus der Flüssigkeitsoberfläche eine Randkurve ausschneidet (Abb. I-4.24).

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">47 Dieser Druck folgt auch aus der Energieerhaltung bei der reversiblen isotherm-isobaren Vergrö- ßerung (siehe dazu Band II, Kapitel „Physik der Wärme“, Abschnitt 1.3.1.2) der kugelförmigen Blase um das Volumen dV = 4 RπdR durch Einblasen des Luftvolumens dV beim Druck P, wobei die Arbeit PdV = P4 R<sup>2</sup>πdR verrichtet wird. Diese Arbeit geht nicht verloren, da keine dissipativen Kräfte vorhanden sind, und wird als innere Energie U<sub>0</sub> = σdA in der um dA = 8 RπdR vergrößerten Oberflä- 4 σ che gespeichert. ⇒ P⋅4 RπdR = 2 σ8 RπdR ⇒ P (Die innere Volumsenergie der Luft UV R ändert sich ja bei diesem Prozess nicht! U<sub>V</sub> dV wird durch das isobar-isotherme Einblasen geliefert). 48 Es gilt (siehe dazu R. Becker, 1961. Theorie der Wärme. Heidelberger Taschenbücher Band 10, PD,R MR 2σ Springer, Berlin, S. 59 f.) ln mit RGas = universelle Gaskonstante und der relati-P⏟⏟⏟⏟⏟⏟⏟⏟⏟⏟⏟⏟⏟⏟⏟⏟⏟ D,R = ∞ ρRGasTR = P<sub>D</sub>,0 ven Molekülmasse von Wasser M<sub>R</sub> = 18.</span></small>

![](images/page_270_image_2.jpg)

Abb. I-4.24: Randwinkel θ einer benetzenden (links, z. B. Plexiglas-Mineralöl) und einer nicht benetzenden Flüssigkeit (rechts, z. B. Glas-Hg).

An der Berührungsfläche der Flüssigkeit mit der Wand bewirkt die Adhäsion eine Grenzflächenspannung $\sigma _ { W F }$ , die vom Material der Wand und von der Flüssigkeit abhängt.<sup>49</sup> Im Gleichgewicht müssen die in der Wand liegende Komponente der Oberflächenspannung $\sigma _ { F }$ cos $\theta$ der freien Flüssigkeit und die Grenzflächenspannung $\sigma _ { W F }$ der Oberflächenspannung entlang der Wand $\sigma _ { W }$ das Gleichgewicht halten.<sup>50</sup>

Ist $\theta$ der Randwinkel zwischen Wand und Flüssigkeit, so muss im Gleichgewicht gelten (vgl. die Youngsche Gleichung in Abschnitt 4.3.8.1, Beispiel Spreitung, Benetzung, Nichtbenetzung):

$$
\sigma_ {F} \cos \theta + \sigma_ {W F} = \sigma_ {W} \tag {I-4.123}
$$

bzw.

$$
\cos \theta = \frac {\sigma_ {W} - \sigma_ {W F}}{\sigma_ {F}}. \tag {I-4.124}
$$

Im Fall einer benetzenden Flüssigkeit mit dem Randwinkel $\theta < 90^{\circ} \left( \Rightarrow \cos \theta > 0 \right)$ ist $\sigma _ { W } - \sigma _ { W F } > 0$ . Gilt $\sigma _ { W } - \sigma _ { W F } > \sigma _ { F }$ , so besteht nach Gl. (I-4.124) in der Randkurve kein Gleichgewicht und die Flüssigkeit überzieht (benetzt) die ganze Wand: Die Flüssigkeit bildet auf der ganzen Wand einen dünnen Film und es gilt $\theta = 0$ . Auch bei einer senkrechten Wand ist die gegen die Schwerkraft zu verrichtende Arbeit vernachlässigbar klein, wenn der Film genügend dünn ist.

Die Gestalt der Meridiankurve (Oberflächenprofil) wird vom Randwinkel $\theta$ ausgehend durch das Zusammenwirken des Krümmungsdrucks $P = \sigma \Bigg ( \frac { 1 } { R _ { 1 } } + \frac { 1 } { R _ { 2 } } \Bigg )$ (siehe

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">49 Streng genommen ist auch die Oberflächenspannung einer Flüssigkeit eine Grenzflächenspannung zu ihrem eigenen Dampf.</span></small>

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">50 Die Normalkomponente wird von der festen Wand kompensiert.</span></small>

Abschnitt 4.3.8.2, Gl. I-4.120) und des hydrostatischen Drucks (Abschnitt 4.3.3, Gl. I-4.64) $P _ { \mathrm { s t a t } } = \rho g z$ bestimmt. In einiger Entfernung von der Wand ist nur mehr der hydrostatische Druck wirksam und die Oberfläche wird eine Äquipotenzialfläche im Schwerefeld, also eine Horizontalebene.

In einem engen Rohr führt dies bei einer benetzenden Flüssigkeit zum Ansteigen der Flüssigkeitssäule gegenüber dem Flüssigkeitsniveau außerhalb des Rohres, bei einer nicht benetzenden Flüssigkeit zu einer Depression der Flüssigkeitssäule. In einem engen Rohr ist der Meniskus (Flüssigkeitsoberfläche) in guter Nä- herung kugelförmig und daher gilt für den zum Kugelmittelpunkt gerichteten Normaldruck der Flüssigkeitsoberfläche nach Abschnitt 4.3.8.2, Gl. (I-4.122) mit $R _ { 1 } = R _ { 2 } = R$ cos θ:

$$
P _ {R} = \frac {2 \sigma}{R} \cos \theta . \tag {I-4.125}
$$

Dieser Druck hält dem von der Gewichtskraft der Flüssigkeitssäule erzeugten Druck $P _ { G } = \rho _ { F } g h ( \rho _ { F } \ldots$ spezifisches Gewicht der Flüssigkeit, $g$ … Betrag der Erdbeschleunigung, h … Steighöhe der Flüssigkeitssäule) das Gleichgewicht.

$$
h = \frac {2 \sigma \cos \theta}{R \rho_ {F} g} \quad \begin{array}{l l} & \text {Steighöhe bzw.} \\ & \text {Kapillardepression.} \end{array} \tag {I-4.126}
$$

Die maximale Steighöhe stellt sich also bei vollständig benetzenden Flüssigkeiten $\left( \theta = 0 ^ { \circ } \right)$ ein:

$$
h _ {\max} = \frac {2 \sigma}{R \rho_ {F} g}. ^ {5 1} \tag {I-4.127}
$$

h bzw. $h _ { \mathrm { m a x } }$ können zur Messung der Oberflächenspannung (= spezifische Grenzflä- chenenergie) σ verwendet werden.

Zusammen mit der Osmose (gerichteter Fluss von Molekülen durch eine halbdurchlässige Trennschicht) ist die Kapillarität für das Hochsteigen der Pflanzensäfte und den Wassernachschub von den Wurzeln verantwortlich. Die Saugwirkung von Papier, Dochten und Schwämmen ist ebenfalls eine Folge der Kapillarität.

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">51 Diese Beziehung folgt auch aus dem Energiesatz: Zum Heben der Flüssigkeitssäule der Länge h (m = ρFRπh ) vom Bezugsniveau bis zur Höhe h ist die Arbeit W = mgh = ρFgRπhaufzuwenden. Gewonnen wird die Energie, die durch die Reduzierung der Flüssigkeitsoberfläche um A = 2 Rπh frei wird. ⇒ ρFgR2πh2= 2 Rπhσ ⇒ h<sub>max</sub> 2 σ RρFg</span></small>

**Beispiel:** Steighöhe in einem engen Rohr.

![](images/page_272_image_3.jpg)

<details>
<summary>text_image</summary>

Druck in Punkt 2 =
= Druck im Bezugsniveau = P₀
P₀ = R / cos θ
r
θ
Pr
θ
2R
h
P₀ = Luftdruck
Bezugsniveau
2
</details>

Für eine nichtbenetzende Flüssigkeit wird in der allgemeinen Gleichung (I-4.126) cos $\theta < 0 ,$ h wird negativ (Kapillardepression).

## Zusammenfassung

1. Wir unterscheiden 4 Aggregatzustände der uns umgebenden Materie, die drei klassischen fest, flüssig und gasförmig und den plasmaartigen Aggregatzustand. Sie sind eine Folge der Stärke der interatomaren Wechselwirkung im Verhältnis zur kinetischen Energie ihrer Bestandteile, also zur Temperatur.
2. Die elastische Verformung fester Körper unter dem Einfluss äußerer Spannungen kann im allgemeinen Fall anisotroper Stoffe (Kristalle) durch die allgemeine Form des Hookeschen Gesetzes beschrieben werden

$$
\sigma_ {\mu} = \sum_ {\nu = 1} ^ {6} C _ {\mu \nu} \cdot \varepsilon_ {\nu}.
$$

Die $\sigma _ { \mu }$ sind die 6 Komponenten des symmterischen Spannungstensors, die $\varepsilon _ { \nu }$ sind die 6 Komponenten des symmetrischen Deformationstensors und $C _ { \mu \nu }$ ist der symmetrische Elastizitätstensor, der für die niederste Kristallsymmetrie (triklin) 21 unabhängige elastische Konstanten enthält. Im kubischen Kristallsystem sind nur mehr 3 Konstanten unabhängig $(C_{11}, C_{12}, C_{44})$ , im isotropen Festkörper nur mehr $2 \left( C _ { 1 1 } , C _ { 4 4 } \right)$ . Vier elastische Konstanten sind für das Experiment von besonderer Bedeutung:

| Der Elastizitätsmodul $E$ | $E = \frac{d\sigma}{d\varepsilon}$ | $(\sigma \dots \text{Normalspannung}, \varepsilon = \frac{\Delta l}{l}),$ |
| --- | --- | --- |
| der Schubmodul $G$ | $G = \frac{d\tau}{d\alpha}$ | $(\tau \dots \text{Schubspannung}, \alpha \dots \text{Scherwinkel}),$ |
| die Poissonzahl $\mu$ | $\mu = \frac{\frac{\Delta d}{d}}{\frac{\Delta l}{l}}$ |  |

und

der Kompressionsmodul K bzw. die Kompressibilität κ

3. In idealen Flüssigkeiten und Gasen (Fluiden) treten keine Scherkräfte auf, der Schubmodul $G = 0$
4. Die Strömung (Stromdichte: $\vec { j } = \rho \cdot \vec { v } )$ in Fluiden wird durch 3 Felder beschrieben: das Dichtefeld $\rho ( \vec { r } , \vec { t } )$ , das Geschwindigkeitsfeld $\vec { v } ( \vec { r } _ { \mathrm { { } } } ,   t )$ und das Druckfeld $P ( \vec { r } , t )$ . Zur Lösung stehen 3 Gleichungen zur Verfügung:

Die Kontinuitätsgleichung

die Eulergleichung

und

die polytrope Zustandsgleichung $P \cdot V ^ { n } = { \mathrm { c o n s t . } }$

mit n als Polytropenexponent $\left( n   \geq   0 \right.$ , abhängig von der vorliegenden Zustandsänderung).

5. Als Anwendung ergaben sich:

Der hydrostatische Druck

die barometrische Höhenformel

die Bernoulli-Gleichung

und

die Laplace-Gleichung für die Potenzialströmung mit $\vec { v } = \vec { \nabla } \cdot \Phi \left( \vec { r } \right)$

$$
\Delta \Phi = 0.
$$

6. Für die Wirbelströmung einer idealen Flüssigkeit gilt die Wirbelgleichung

$$
\frac {\partial \vec {\Omega}}{\partial t} + \vec {\nabla} \times (\vec {\Omega} \times \vec {v}) = 0, \quad \text {wobei} \vec {\Omega} = \frac {1}{2} \operatorname{rot} \vec {v} \quad (\text {Wirbelvektor}).
$$

Die Strömungsverhältnisse bei Wirbelströmung werden in folgenden Sätzen zusammengefasst:

$\frac { \partial \bar { \Omega } } { \partial t } = 0$ , Wirbel können weder entstehen noch vergehen;

die Zirkulation $\varGamma   =   \int \limits _ { C }   \vec { \upsilon } d \vec { s }$ ist zeitlich konstant (Thomsonscher Satz).

Helmholtzsche Wirbelsätze:

a) $\underbrace { \mathbf { d i v }   \vec { \Omega } } _ { \begin{array} { l } { Q u e l l e r g i e b i g k e i t } \\ { f \ddot { u } r d e n \; W i r b e l v e k t o r } \end{array} } = 0$ , es gibt weder Quellen noch Senken für Wirbel;

b) die Wirbelstärke $W _ { \mathrm { A } } = \Omega \cdot A$ der Wirbelfäden ist zeitlich und örtlich konstant;
c) die Wirbelfäden bestehen dauernd aus denselben rotierenden Flüssigkeitsteilchen.

7. In zähen Fluiden gilt das Hagen-Poiseuillesche Gesetz für den Flüssigkeitsstrom $I = { \frac { V } { t } } .$

$$
I = \frac {\pi \cdot R ^ {4}}{8 \eta} \cdot \frac {\Delta P}{l},
$$

das wichtig für die Blutzirkulation unseres Körpers ist.

8. Der Reibungswiderstand eines kugelförmigen Teilchens beträgt

$$
\vec {F} _ {R} = - 6 \pi \eta R \vec {\nu}.
$$

9. Ob bei einer Strömung laminares oder turbulentes Strömungsverhalten vorliegt, kann durch Bestimmung der Reynoldsschen Zahl abgeschätzt werden

$$
R e = \frac {r \cdot \rho \cdot v}{\eta}.
$$

In glatten Rohren gilt für den Umschlag von laminarer zu turbulenter Strö- mung $R e ^ { \mathrm { k r i t } } = 1 1 6 0$

## Übungen:

1. a) Zeige, dass die Volumenänderung eines Stabes bei einem einachsigen Zugversuch durch $\Delta V / V = \sigma / E \cdot ( 1 - 2   \mu )$ gegeben ist, wobei $\sigma$ die Zugspannung, E der Elastizitätsmodul und $\mu$ die Poissonsche Querkontraktionszahl ist.
b) Zeige, dass für eine isostatische = allseitige Kompression mit dem Druck P gilt

$$
\Delta V / V = - 3 P / E \cdot (1 - 2 \mu).
$$

2. Gegeben sei ein Verbundwerkstoff, der aus lamellenförmigen Phasen mit den elastischen Dehnungsmoduln (Young’s moduli) $E _ { 1 }$ und $E _ { 2 }$ und gleicher Poissonscher Querkonzentrationszahl $\mu$ besteht. Überlege den effektiven Dehnungsmodul $E _ { \mathrm { e f f } }$ wenn der Werkstoff wie in der Abbildung in der Art a) bzw. b) belastet wird. Wie ist das Verhalten in beiden Fällen, wenn eine Phase elastisch wesentlich weicher ist als die andere, z. B. $E _ { 1 } \gg E _ { 2 }$ . (Im Fall a) wird angenommen, dass die Deck- und die Grundfläche auch nach der Belastung eben bleiben).

a)

![](images/page_275_image_12.jpg)

<details>
<summary>text_image</summary>

F
D
d
</details>

b)

![](images/page_275_image_14.jpg)

<details>
<summary>text_image</summary>

F
</details>

3. Eine massive zylindrische Stahlsäule ist 3,5 m lang und hat einen Durchmesser von 10 cm. Wie groß ist ihre Längenabnahme, wenn sie eine Last von 80 t trägt? Ihr Dehnungsmodul betrage $E = 2 , 2 0 \cdot 1 0 ^ { 1 1 }   \mathrm { P a }$
4. Der Kompressionsmodul K von Quecksilber beträgt $2 { , } 8 \cdot { 1 0 } ^ { 1 0 }$ Pa. Berechne die Volumenkontraktion von $1 6 0 0 \; \mathrm { c m } ^ { 3 }$ Quecksilber, wenn es einem Druck von $1 { , } 4 \cdot 1 0 ^ { 6 }   \mathrm { P a }$ unterworfen wird.
5. Anwendung der Bernoulli-Gleichung: Wenn Wasser schnell strömt, dann kann der Druck so weit erniedrigt werden, dass er kleiner als der Gleichgewichtsdampfdruck des Wassers wird. In diesem Fall bilden sich Dampfblasen. Dieses als Kavitation bekannte Phänomen ist in der Schiffstechnik unerwünscht, da es zur Verminderung des Wirkungsgrades, zu Vibrationen und zu Beschädigungen z. B. an den Spitzen schnell drehender Schiffsschrauben führt.
Wie groß muss die Strömungsgeschwindigkeit sein, damit in 2 m Tiefe Kavitation auftritt? (Dichte von Wasser: $1000\;\mathrm{kg/m^{3}}$ Gleichgewichtsdampfdruck $P _ { \mathrm { H } _ { 2 } \mathrm { O } } = 2 3 { , } 3$ mbar bei $2 0 ~ ^ { \circ } \mathrm { C } ;$ auf der Wasseroberfläche laste eine Stan dardatmosphäre = 1 bar ${ = }   1 0 ^ { 5 }   \mathrm { P a } )$
6. Ein Stück Glasröhre, das einen äußeren Durchmesser von 4 cm und einen inneren Durchmesser von 3,5 cm besitzt, steht senkrecht mit einem Ende in Wasser eingetaucht. Wie groß ist die nach unten gerichtete Kraft auf die Röhre als Folge der Oberflächenspannung? Die Oberflächenspannung von Wasser gegen Luft beträgt $\sigma = 0 , 0 7 4 \mathrm { N / m }$ Annahme: Das Wasser benetzt das Glas vollständig und die Oberflächenspannung Wasser–Glas ist vernachlässigbar.
7. Ein Fass mit dem Durchmesser von 1 m ist mit Glyzerin $\left( \rho_{F} = 1260  kg m ^{-3} \right)$ gefüllt. Dessen Viskosität wird dadurch bestimmt, dass man eine Stahlkugel mit dem Durchmesser $2 r = 6$ mm $\left( \rho_{s} = 7800   kg   m ^{-3} \right)$ im Glyzerin sinken lässt und die konstante Sinkgeschwindigkeit von $v = 9    cm    s ^{-1}$ misst. Wie groß ist die Viskosität $\eta \ell$

## Anhang 1 Gleichgewicht im elastischen Körper: Grundgleichung der Elastostatik

Wir betrachten ein endliches Volumen V im isotropen elastischen Körper (Abb. I-4.25):

![](images/page_277_image_4.jpg)

<details>
<summary>text_image</summary>

dV
\vec{f}_v dV
V
O
\vec{\sigma} df = (\vec{\sigma} \cdot \vec{n}) df
\vec{n}
\vec{df} = \vec{n} df
</details>

Abb. I-4.25: Endliches Volumen V in einem isotropen elastischen Körper.

Im Inneren wirken auf jedes Volumenelement dV die Massenkräfte (z. B. die Schwerkraft im Erdschwerefeld) $d \vec { F } = \vec { f } _ { V }   d V \left( \vec { f } _ { V } \ldots \right.$ Kraftdichte, $[ f _ { V } ] = \mathrm { N } / \mathrm { m } ^ { 3 } )$ und an der Oberfläche O auf jedes Oberflächenelement df die Spannungskräfte σ⇀df (im Inneren annullieren sich alle Spannungskräfte an den Oberflächen der Volumenelemente dV). Im statischen Gleichgewicht (GG) muss die Summe aller Kräfte Null sein, daher gilt

$$
\int_ {V} \vec {f} _ {V} d V + \oint_ {O} \vec {\sigma} d f = 0. \tag {I-4.128}
$$

Die Spannung $\bar { \sigma }$ auf der Oberfläche im Flächenelement df mit der Normalen n⇀folgt aus dem Spannungstensor $\tilde { \sigma }$ (Abschnitt 4.2.4, Gl. I-4.30)

$$
\begin{array}{l} \vec {\sigma} = \tilde {\sigma} \cdot \vec {n} = \underbrace {\left(\sigma_ {1} n _ {x} + \tau_ {6} n _ {y} + \tau_ {5} n _ {z}\right)} _ {= \vec {P} _ {1} \cdot \vec {n}} \vec {e} _ {x} + \underbrace {\left(\tau_ {6} n _ {x} + \sigma_ {2} n _ {y} + \tau_ {4} n _ {z}\right)} _ {= \vec {P} _ {2} \cdot \vec {n}} \vec {e} _ {y} + \\ + \underbrace {\left(\tau_ {5} n _ {x} + \tau_ {4} n _ {y} + \sigma_ {3} n _ {z}\right)} _ {= \vec {P} _ {3} \cdot \vec {n}} \vec {e} _ {z}. \tag {I-4.129} \\ \end{array}
$$

Damit folgt für die x-Komponente von Gl. (I-4.128): (I-4.130)

$$
\int_ {V} f _ {V x}   d V + \oint_ {O} \vec {P} _ {1} \cdot \vec {n} \cdot d f = \int_ {V} f _ {V x}   d V + \oint_ {O} \vec {P} _ {1} \cdot d \vec {f} \underbrace {=} _ {\substack {\text {Gaußscher} \\ \text {Satz}}} \int_ {V} f _ {V x}   d V + \int_ {V} \operatorname{div} \vec {P} _ {1}   d V = 0
$$

und damit

$$
f _ {V x} + \mathrm{div} \vec {P} _ {1} = f _ {V x} + \frac {\partial \sigma_ {1}}{\partial x} + \frac {\partial \tau_ {6}}{\partial y} + \frac {\partial \tau_ {5}}{\partial z} = 0 \tag {I-4.131}
$$

sowie zwei analoge Gleichungen für die y- und z-Koordinaten.

Werden in diesen drei Gleichungen die Spannungen $( \sigma _ { i } ,   \tau _ { i } )$ unter Benützung des Hookeschen Gesetzes durch die Verzerrungen $( \varepsilon _ { i } , \gamma _ { \mathrm { i } } )$ bzw. die Verschiebungen $\vec { s } = \{ u , v , w \} = \tilde { \varepsilon } \cdot \vec { r }$ ausgedrückt, so ergibt sich schließlich<sup>52</sup> die fundamentale Beziehung zwischen der Kraftdichte $\vec { f } _ { V }$ und den Verschiebungen $\vec { s } = \{ v , v , w \}$ zu

$$
\vec {f} _ {V} + \frac {E}{2 (1 + \mu)} \left\{\Delta \vec {s} + \frac {\mu}{1 - 2 \mu} \operatorname{grad} \operatorname{div} \vec {s} \right\} = 0 \tag {I-4.132}
$$

Ist die äußere Kraftdichte $\vec { f } _ { V }$ vorgegeben, so können mit Gl. (I-4.132) unter Berücksichtigung der Randbedingungen die Verschiebungen s⇀berechnet werden.

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">52 Die Komponenten des Deformationstensors ε ̃ können aus den Verschiebungen s⇀= {u,υ,w} nach Gl. (I-4.38) berechnet werden. Damit wird die Dimension des zweiten Terms der nachfolgenden N m N [F ] Gl. (I-4.132) zu = [ fV] und stimmt daher mit dem ersten Term, der Kraftdichte, 2 [V ] m m m überein.</span></small>

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">53 Gl. (I-4.132) ist der statische Spezialfall der allgemeinen Grundgleichung der Elastokinetik: f⇀V + E {Δs⇀+ μ grad div s⇀} ∂2 s⇀ Das ist die bestimmende Gleichung der linearen 2 (1 + μ) 1 − 2 μ ∂t2 Mechanik elastischer Körper, die auch die Wellenausbreitung in elastischen Medien beschreibt. Genauere Darstellung in H. Stephani und G. Kluge, Theoretische Mechanik; Punkt- und Kontinuumsmechanik. Spektrum Akademischer Verlag, Heidelberg 1995.</span></small>

## 5 Mechanische Schwingungen und Wellen (oscillations and waves)

**Einleitung:** Mechanische Schwingungen, die sich als Wellen in einem Medium im Raum ausbreiten können, stellen ein fundamentales Kapitel der Mechanik dar. Im Gegensatz zu den hier untersuchten mechanischen Wellen breiten sich elektromagnetische Wellen ohne vermittelndes Medium im leeren Raum aus (Band III, Kapitel „Wechselstromkreis und elektromagnetische Schwingungen und Wellen“).

Die einfachste Schwingungsform stellt der (ungedämpfte) „Harmonische Oszillator“ dar: Ein Massenpunkt wird aus der Ruhelage ausgelenkt und führt nun fortwährend harmonische Schwingungen aus, wenn auf ihn nur eine Kraft wirkt, die ihn in die ursprüngliche Position zurücktreibt und deren Stärke proportional zur Auslenkung ist. Wirkt zusätzlich eine Reibungskraft, so klingen die Schwingungen exponentiell ab. Wird die Schwingung von außen durch eine periodische Kraft angetrieben („erzwungen“), so kommt es – abhängig von der Dämpfung – zu überhöhten Schwingungsamplituden (Resonanz), wenn die Frequenz der Anregung mit der Eigenfrequenz des Oszillators nahezu übereinstimmt.

Schwingungen können sich überlagern (Superpositionsprinzip) und sind i. Allg. wieder durch eine periodische Funktion darstellbar. Umgekehrt lässt sich jede periodische Funktion als Summe von harmonischen Schwingungen darstellen (Fourierzerlegung); die Amplituden dieser Teilschwingungen sind die Fourierkoeffizienten. Diese Zerlegung kann auf unperiodische Funktionen ausgedehnt werden (Fourierintegral); die Amplitudenfunktion ist dann kontinuierlich (Fouriertransformierte). Wird das Fourierintegral nicht von einer Zeitfunktion, sondern von einer Ortsfunktion gebildet, dann ist die Fouriertransformierte eine Funktion im reziproken k⇀-Raum.

Ist ein schwingender Massenpunkt mit benachbarten Massenpunkten gekoppelt, z. B. durch ein elastisches Medium, so kann sich die Schwingung als Welle im Raum ausbreiten und es wird Schwingungsenergie räumlich transportiert. Für die Ausbreitungsgeschwindigkeit der Phase („augenblicklicher Schwingungszustand“) einer Welle gilt $\nu _ { p h } = \nu \cdot \lambda = \frac { \omega } { k }$ . Hängt die Phasengeschwindigkeit von der Wellenlänge ab (Dispersion), so verliert sie ihre Bedeutung für die Ausbreitung eines tatsächlichen Wellenvorgangs, der immer einen Anfang und ein Ende hat, und die Gruppengeschwindigkeit $\nu _ { g r } = \frac { d \omega } { d k } = \nu _ { p h } - \lambda   \frac { d \nu _ { p h } } { d \lambda }$ tritt an ihre Stelle. Sie beschreibt die Ausbreitungsgeschwindigkeit des Energiezentrums einer Wellengruppe und somit auch die jeglicher Information.

Zur Lösung eines Wellenproblems, also zur Bestimmung der Wellenfunktion, muss die Wellengleichung unter den gegebenen Randbedingungen gelöst werden. Damit lässt sich zeigen, dass die Transversalschwingungen einer beidseitig fest eingespannten Saite stehende Wellen sind, deren diskrete Frequenzen bzw. Wellenlängen vom Abstand der Einspannung abhängen. Analog ergibt die Lösung der Wellengleichung für Materiewellen, der Schrödingergleichung, stehende Materiewellen, die einem Materieteilchen zugeordnet werden, wenn es in einem unendlich tiefen Potenzialtopf eingesperrt ist (Band V, Kapitel „Atomphysik“).

Die Akustik beschäftigt sich mit der Erzeugung und Übertragung von Schall; Schallwellen werden z. B. bei der menschlichen Stimmbildung erzeugt, von der Luft als Medium übertragen und vom menschlichen Ohr empfangen, also gehört. Bewegt sich die Schallquelle oder der Schallempfänger, so ergibt sich am Ort des Empfängers eine Frequenzänderung, die unterschiedlich ausfällt, je nachdem, ob sich die Quelle oder der Empfänger bewegt (akustischer Dopplereffekt). An der Ausbreitung elektromagnetischer Wellen ist dagegen kein Medium beteiligt, daher tritt dieser Unterschied dort nicht auf (Band II, Kapitel „Relativistische Mechanik“).

Wenn ein physikalisches System mit Trägheit und Rückstellkraft (Massenpunkt, starrer Körper, Atom oder Molekül usw.) aus seiner Ruhelage = stabile Gleichgewichtslage ausgelenkt wird, beginnt es um seine Ruhelage zu schwingen.

4

![](images/page_280_image_6.jpg)

Eine Kugel hängt an einer Spiralfeder in Ruhe.<sup>1</sup>

Wird die Kugel a) aus der Ruheposition nach unten gestoßen oder b) langsam aus der Ruhelage etwas nach unten gezogen und dann losgelassen, beginnt die Kugel um die Ruhelage (Pfeil) zu schwingen.

Die Frage ist nun: Welche Parameter bestimmen die Schwingungsfrequenz, wie sieht der zeitliche Ablauf der Bewegung der Kugel aus, wie lange schwingt die Kugel?

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">1 Die Feder erfüllt bei diesem Versuch zwei Funktionen: Erstens kompensiert sie nach entsprechender Vordehnung die Gewichtskraft der Kugel, sodass das System im Potenzialminimum zur Ruhe kommt; zweitens dient sie im Schwingfall als Energiespeicher (siehe Abschnitt 5.2.4).</span></small>

Schwingungen sind nicht nur in der Mechanik wichtig, sondern auch in allen anderen Bereichen der Physik (Elektrodynamik und Optik, Strahlung und Atomphysik, Kernphysik, Festkörperphysik). Schwingungen können zur Ausbreitung von Wellen führen, wenn eine große Anzahl an Oszillatoren (= Schwingern) aneinander ‚gekoppelt‘ sind, d. h. wenn von einem schwingenden System auf das nächste Energie übertragen werden kann.

Eine Reihe von gleichartigen Fadenpendeln sei durch dünne Fäden miteinander verbunden, an denen kleine Massen hängen (Kopplung). Wenn das erste Pendel etwas ausgelenkt und losgelassen wird, überträgt sich die Pendelschwingung der Reihe nach auf die nächsten Pendel und das erste Pendel kommt zur Ruhe. Es breitet sich eine Welle der Ausschläge aus, mit der Energie transportiert wird. Ist das letzte Pendel der Reihe in Schwingung geraten, überträgt es seine Energie zurück auf das vorletzte usf., die Welle wird reflektiert.<sup>2</sup>

![](images/page_281_image_4.jpg)

Zwei gekoppelte Pendel: Links sind beide Pendel in Ruhe. In der Mitte wird das rechte Pendel ausgelenkt und losgelassen, das linke ist in Ruhe. Das rechte Pendel schwingt und gibt Energie an das linke Pendel ab, das langsam zu schwingen beginnt. Nach einiger Zeit kommt das rechte Pendel zur Ruhe und das linke schwingt voll (rechtes Bild). Dann gibt es seine Energie langsam wieder an das rechte Pendel zurück, sein Ausschlag wird immer kleiner, während das rechte wieder zur vollen Schwingung ausholt.

In der Akustik wird die Erzeugung, Ausbreitung und Absorption von Wellen studiert, die in den Hörbereich fallen (Schallwellen). Musikinstrumente besitzen spezielle schwingende Systeme (Saite, Federzunge, Luftsäule mit Wirbelschneide bei Pfeifen und Flöte usw.), die Schallwellen einer spezifischen Zusammensetzung (Klangfarbe etc.) erzeugen, die dann durch geeignete ‚Resonanzkörper‘ verstärkt bzw. modifiziert werden.

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">2 Die tatsächlich auftretende Bewegungsform hängt wesentlich vom Verhältnis der Koppelkraft zur Rückstellkraft der Pendel ab. Der beschriebene Vorgang gilt für „sehr weiche“ Kopplung (weak coupling); bei „sehr harter“ Kopplung (strong coupling) wird die Stoßenergie sehr rasch an die folgenden Pendel weitergeleitet, sodass ein „Schallpuls“ (sound pulse wave) durch die Kette läuft, dem sich noch eine pendelnde Schwerpunktsbewegung überlagert, deren Größe von der Dauer der Stoßkraft (Auslenkung) abhängt.</span></small>

## 5.1 Ungedämpfte harmonische Schwingungen (undamped harmonic oscillations)

## 5.1.1 Der freie, ungedämpfte harmonische Oszillator (simple harmonic oscillator)

‚Harmonisch‘ (griechisch) heißt: Im Einklang befindlich, wohlklingend, ausgewogen im Verhältnis und hat mit dem Wohlklang entsprechend zusammengesetzter, akustischer harmonischer Schwingungen zu tun.

Ein Massenpunkt (MP) befinde sich in der Ruhelage bei $x = 0$ . Wird der MP aus der Ruhelage ausgelenkt, wirkt (außer der Schwerkraft, die wir beiseite lassen, sie wird durch die Aufhängung und die Federvordehnung kompensiert) die rücktreibende Kraft der Feder (Abb. I-5.1).

![](images/page_282_image_6.jpg)

<details>
<summary>text_image</summary>

x = 0
x
</details>

Abb. I-5.1: Der $M P$ (blau) hängt an einer sehr leichten Feder, sodass die Federbewegung unberücksichtigt bleiben kann.

Ist die Auslenkung so klein, dass die Verformung der Feder im Hookeschen Bereich bleibt, in dem die Federkraft proportional zur Auslenkung ist (siehe Kapitel „Mechanik deformierbarer Körper“, Abschnitt 4.2.1), so sprechen wir von einer harmonischen Kraft. Dasselbe gilt auch für die Atome eines Festkörpers, die im Kristallgitter entsprechend der Temperatur um ihre Ruhelage schwingen.<sup>3</sup> Die rücktreibenden Kräfte sind eine Folge der interatomaren Wechselwirkungen (WW) und können in erster Näherung als harmonisch, also als proportional zur Auslenkung, angenommen werden. Wir setzen die wirkende, rücktreibende Kraft für kleine Auslenkungen x daher so an

$$
\vec {F} = - k \cdot x \cdot \vec {e} _ {x}, \quad [ k ] = \mathrm{Nm} ^ {- 1}. \tag {I-5.1}
$$

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">3 Die Schwingungen sind allerdings nur bei sehr niedriger Temperatur (sehr kleiner Auslenkung) harmonisch. (Siehe Band VI, Kapitel „Festkörperphysik“, Abschnitt 2.4.1).</span></small>

Den Proportionalitätsfaktor k nennen wir Federkonstante. Sie beschreibt die Stärke der rücktreibenden Kraft (Stärke der interatomaren WW).

Wie kommen wir zur Bewegung, die der MP ausführt? Wir setzen in die Bewegungsgleichung (= 2. Newtonsches Axiom = Newton 2) ein (siehe Kapitel „Mechanik des Massenpunktes“, Abschnitt 2.2.1). Hier ist die Bewegung eindimensional (wenn wir in der Richtung der Federachse auslenken) und Newton 2 führt auf eine lineare, homogene Differentialgleichung (DG)

$$
- k \cdot x (t) = m \frac {d ^ {2} x (t)}{d t ^ {2}}, \quad \text {bzw.} \quad m \ddot {x} (t) + k x (t) = 0 \tag {I-5.2}
$$

$$
\Rightarrow \quad \ddot {x} (t) + \frac {k}{m} x (t) = 0 \quad \begin{array}{l} \text {Schwingungsgleichung des ungedämpften} \\ \text {harmonischen Oszillators.} \end{array} \tag {I-5.3}
$$

![](images/page_283_image_6.jpg)

Die zeitlich aufgelöste Bewegung eines harmonischen Oszillators kann so gewonnen werden: Auf der Tafel wird zunächst die eindimensionale Schwingung horizontal mit der Kreide ausgeführt (ganz links). Dann wird die Tafel bei fortgesetzter Schwingungsbewegung der Kreidehand gleichmäßig nach oben geschoben. Es ergibt sich eine etwa sinusförmige Kreidelinie.

Da die zweite Ableitung einer Sinusfunktion bis auf das Vorzeichen gleich der Funktion selbst ist, wählen wir daher als Ansatz für die allgemeine Lösung der DG eine Kombination aus Sinus- und Kosinusschwingungen<sup>4</sup> mit zunächst unbekannter Kreisfrequenz $\omega = 2 \pi \nu$

$$
\text { Lösungsansatz: } \quad x (t) = C _ {1} \cos (\omega t) + C _ {2} \sin (\omega t). \tag {I-5.4}
$$

Einmal und zweimal differenziert ergibt

$$
\frac {d x}{d t} = - C _ {1} \omega \sin (\omega t) + C _ {2} \omega \cos (\omega t) \tag {I-5.5}
$$

$$
\frac {d ^ {2} x}{d t ^ {2}} = - C _ {1} \omega^ {2} \cos (\omega t) - C _ {2} \omega^ {2} \sin (\omega t), \tag {I-5.6}
$$

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">4 Dies ist gleichbedeutend mit einer Sinusschwingung mit einer willkürlichen Phasenkonstante.</span></small>

und in die Bewegungsgleichung eingesetzt folgt

$$
- C _ {1} \omega^ {2} \cos (\omega t) - C _ {2} \omega^ {2} \sin (\omega t) + \frac {k}{m} C _ {1} \cos (\omega t) + \frac {k}{m} C _ {2} \sin (\omega t) = 0
$$

und damit

$$
\begin{array}{l} C _ {1} \cos (\omega t) \left(\frac {k}{m} - \omega^ {2}\right) + C _ {2} \sin (\omega t) \left(\frac {k}{m} - \omega^ {2}\right) = \\ = \left(\frac {k}{m} - \omega^ {2}\right) \underbrace {\left(C _ {1} \cos (\omega t) + C _ {2} \sin (\omega t)\right)} _ {x (t)} = 0 \tag {I-5.7} \\ \end{array}
$$

also

$$
\left(\frac {k}{m} - \omega^ {2}\right) \cdot x (t) = 0. \tag {I-5.8}
$$

Für eine tatsächliche Schwingung um die Ruhelage kann $x ( t )$ nicht dauernd verschwinden. Daher ist diese Gleichung nur erfüllt, wenn gilt

$$
\omega^ {2} = \frac {k}{m} \equiv \omega_ {0} ^ {2}. \tag {I-5.9}
$$

Damit wird die Schwingungsgleichung zu

$$
\ddot {x} + \omega_ {0} ^ {2} x = 0
$$

(I-5.10)

Für die gesuchte Kreisfrequenz ω ergibt sich also eine feste Eigenfrequenz $\omega _ { 0 }$ der Schwingung, die nur von der rücktreibenden Kraft, also der Federkonstante, und der Masse des schwingenden Systems abhängt, nicht aber von der Auslenkung (im Rahmen kleiner Auslenkungen, wie vorausgesetzt).

Für die Dauer T einer Schwingungsperiode (Zeit zwischen zwei gleichen Schwingungszuständen) ergibt sich mit

$$
\begin{array}{l} \omega_ {0} = 2 \pi \nu_ {0} = 2 \pi / T = \sqrt {\frac {k}{m}} \\ T = 2 \pi \sqrt {\frac {m}{k}}. \tag {I-5.11} \\ \end{array}
$$

Die Schwingungsdauer sieht für andersartige Oszillatoren (z. B. Schwerependel oder Drehpendel) analog aus: unter der Wurzel im Zähler eine Trägheitskonstante und im Nenner eine Kraftkonstante.<sup>5</sup>

Damit erhalten wir die allgemeine Lösung der Bewegungsgleichung des MP, also seine zeitliche Bewegung

$$
x (t) = C _ {1} \cos (\omega_ {0} t) + C _ {2} \sin (\omega_ {0} t). \tag {I-5.12}
$$

Es verbleibt die Aufgabe, die Konstanten $C _ { 1 }$ und $C _ { 2 }$ zu bestimmen. Wir benützen dazu die Anfangsbedingungen.

Zur Zeit $t = 0$ sei der $M P$ an der Stelle $x ( 0 ) = x _ { 0 }$ und habe die Geschwindigkeit $\upsilon ( 0 ) = \dot { x } ( 0 ) = \upsilon _ { 0 }$ . Wir setzen in der Lösung $t = 0 ;$

$$
x (0) = C _ {1} \cos (0) + C _ {2} \sin (0) = x _ {0} \quad \Rightarrow \quad C _ {1} = x _ {0}
$$

$$
\dot {x} (0) = - C _ {1} \omega_ {0} \sin (0) + C _ {2} \omega_ {0} \cos (0) = v _ {0} \quad \Rightarrow \quad C _ {2} = v _ {0} / \omega_ {0}.
$$

Damit erhalten wir die endgültige Lösung der Differentialgleichung für die Bewegung des MP zu

$$
x (t) = x _ {0} \cos (\omega_ {0} t) + \frac {\nu_ {0}}{\omega_ {0}} \sin (\omega_ {0} t) \quad \text {Bewegung des schwingenden MP.} \tag {I-5.13}
$$

## Andere Vorgehensweise zur Lösung der Bewegungsgleichung

Lösungsansatz: (I-5.14)

denn die Exponentialfunktion reproduziert sich bei der Differentiation.

c und λ sind zunächst unbestimmte Konstanten, die auch komplex sein können.

Einmal und zweimal nach der Zeit differenziert unter Beachtung von $\frac{d}{dx}\left(e^{ax}\right)=ae^{ax}$ liefert

$$
\dot {x} = c \lambda e ^ {\lambda t}, \quad \ddot {x} = c \lambda^ {2} e ^ {\lambda t}. \tag {I-5.15}
$$

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">5 Beim Schwerependel $\left( T = 2 \pi { \sqrt { l / g } } \right)$ fällt die Masse m heraus, da sie auch in der Kraftkonstanten auftritt. Beim Drehpendel sind m durch das Trägheitsmoment Θ und k durch das Direktionsmoment (= Richtmoment, Winkelrichtkraft) D\* zu ersetzen. (Siehe Kapitel „Mechanik deformierbarer Körper“, Abschnitt 4.2.2).</span></small>

Eingesetzt in die Bewegungsgleichung ergibt sich

$$
c \lambda^ {2} e ^ {\lambda t} + \frac {k}{m} c e ^ {\lambda t} = 0. \tag {I-5.16}
$$

Die Exponentialfunktion $e ^ { \lambda t }$ kann nicht verschwinden und damit auch nicht $c \cdot e ^ { \lambda t }$ Es bleibt also

$$
\lambda^ {2} + \frac {k}{m} = 0 \tag {I-5.17}
$$

Wir setzen $k / m = \omega _ { 0 } ^ { 2 }$ und erhalten die charakteristische Gleichung zur Bestimmung von λ

$$
\lambda^ {2} + \omega_ {0} ^ {2} = 0. \tag {I-5.18}
$$

Die Auflösung dieser quadratischen Gleichung nach λ ergibt

$$
\lambda_ {1} = i \omega_ {0}
$$

$$
\lambda_ {2} = - i \omega_ {0}. \tag {I-5.19}
$$

Eingesetzt in den Lösungsansatz

$$
x _ {1} (t) = c _ {1} e ^ {i \omega_ {0} t}, \quad x _ {2} (t) = c _ {2} e ^ {- i \omega_ {0} t} \tag {I-5.20}
$$

erhält man die allgemeine Lösung, sie muss 2 verfügbare Konstanten besitzen:

$$
x (t) = c _ {1} e ^ {i \omega_ {0} t} + c _ {2} e ^ {- i \omega_ {0} t}. \tag {I-5.21}
$$

Dabei sind $c _ { 1 }$ und $c _ { 2 }$ komplexe Konstanten. Das Ergebnis, also die Bewegung des $M P ,$ muss aber reell sein. Da $e ^ { i \omega _ { 0 } t }$ und $e ^ { - i \omega _ { 0 } t }$ zueinander konjugiert komplex sind, müssen die beiden Konstanten daher auch zueinander konjugiert komplex sein, damit $x ( t )$ reell wird, also

$$
c _ {2} = c _ {1} ^ {\star} = c ^ {\star} \text {und} c _ {1} = c _ {2} ^ {\star} = c
$$

mit $c = a + i b ,   c ^ { \star } = a - i b ,   a ,   b .$ … reell.

Damit wird die Lösung zu

$$
x (t) = c e ^ {i \omega_ {0} t} + c ^ {\star} e ^ {- i \omega_ {0} t}. \tag {I-5.22}
$$

Die Bestimmung der reellen Konstanten a und b des Real- und Imaginärteils der komplexen Koeffizienten erfolgt wieder aus den Anfangsbedingungen $x ( 0 ) = x _ { 0 }$ und $\dot { x } ( 0 ) = \upsilon ( 0 ) = \upsilon _ { 0 }$

Aus (I-5.23)

also (I-5.24)

$$
\dot {x} (0) = i \cdot c \cdot \omega_ {0} \cdot e ^ {i \omega_ {0} \cdot 0} - i \cdot c ^ {\star} \cdot \omega_ {0} \cdot e ^ {- i \omega_ {0} \cdot 0} = i \omega_ {0} (c - c ^ {\star}) = v _ {0}.
$$

$$
c - c ^ {\star} = a + i b - a + i b = 2 i b = \frac {v _ {0}}{i \omega_ {0}} \quad \Rightarrow \quad b = - v _ {0} / 2 \omega_ {0}, \tag {I-5.25}
$$

also (I-5.26)

Um zu zeigen, dass diese Form der Lösung mit der vorhergehenden übereinstimmt, setzen wir die Konstanten in die Lösung ein und benützen die Eulerschen Formeln $e ^ { i z } = \cos ( z ) + i \sin ( z )$ und $e ^ { - i z } = \cos ( z ) - i$ sin(z):

$$
\begin{array}{l} x (t) = (a + i b) e ^ {i \omega_ {0} t} + (a - i b) e ^ {- i \omega_ {0} t} = \left(\frac {x _ {0}}{2} - i \frac {v _ {0}}{2 \omega_ {0}}\right) e ^ {i \omega_ {0} t} + \left(\frac {x _ {0}}{2} + i \frac {v _ {0}}{2 \omega_ {0}}\right) e ^ {- i \omega_ {0} t} = \\ = \left(\frac {x _ {0}}{2} - i \frac {\nu_ {0}}{2 \omega_ {0}}\right) \left[ \cos \left(\omega_ {0} t\right) + i \sin \left(\omega_ {0} t\right) \right] + \left(\frac {x _ {0}}{2} + i \frac {\nu_ {0}}{2 \omega_ {0}}\right) \left[ \cos \left(\omega_ {0} t\right) - i \sin \left(\omega_ {0} t\right) \right] = \\ = \frac {x _ {0}}{2} \cos (\omega_ {0} t) + \frac {\nu_ {0}}{2 \omega_ {0}} \sin (\omega_ {0} t) + \frac {x _ {0}}{2} \cos (\omega_ {0} t) + \frac {\nu_ {0}}{2 \omega_ {0}} \sin (\omega_ {0} t) = \\ = x _ {0} \cos (\omega_ {0} t) + \frac {\nu_ {0}}{\omega_ {0}} \sin (\omega_ {0} t). \tag {I-5.27} \\ \end{array}
$$

⇒ Das Ergebnis stimmt mit dem vorhergehenden überein, es handelt sich also um völlig äquivalente Beschreibungen!

Der Vergleich mit den Konstanten $C _ { 1 }$ und $C _ { 2 }$ der Gleichung (I-5.4) ergibt unter Beachtung der Gleichungen (I-5.23) und (I-5.25)

$$
C _ {1} = x _ {0} = c + c ^ {\star} = 2 a, \quad C _ {2} = v _ {0} / \omega_ {0} = i (c - c ^ {\star}) = - 2 b. \tag {I-5.28}
$$

Eine andere Darstellung von c und $c ^ { \star }$ ist die ‚Polardarstellung‘ einer komplexen Zahl (siehe Abb. I-5.2)

$$
c = | c | \cdot e ^ {i \varphi}, \quad c ^ {\star} = | c | \cdot e ^ {- i \varphi}. \tag {I-5.29}
$$

Sie führt auf

$$
x (t) = \left| c \right| \left[ e ^ {i (\omega_ {0} t + \varphi)} + e ^ {- i (\omega_ {0} t + \varphi)} \right] \tag {I-5.30}
$$