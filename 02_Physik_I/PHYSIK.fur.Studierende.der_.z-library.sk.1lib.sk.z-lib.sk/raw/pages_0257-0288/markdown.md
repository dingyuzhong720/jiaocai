sie einmünden, sprechen wir daher von einem **Quellenfeld**. Andererseits können Feldlinien auch in sich geschlossen verlaufen, so dass es für sie keinen Anfang und kein Ende, d. h. keine Quellen, gibt. Solche geschlossenen Feldlinien heißen Wirbel, die zugehörigen Felder **Wirbelfelder** (Bild 22.1c).

Hinsichtlich der zeitlichen Veränderung von Feldern unterscheiden wir stationäre oder statische Felder, in denen die Feldstärke überall zeitlich konstant ist, und Wechselfelder mit zeitlich (periodisch oder unperiodisch) sich ändernder Feldstärke.

## 22.2 Gravitationsfeldstärke, Gravitationspotenzial

Nach dem 2. NEWTONschen Axiom führt das Kraftfeld $\pmb { F } = m \pmb { \alpha }$ zur Beschleunigung a der trägen Masse m. In einem Gravitationsfeld der Feldstärke G wirkt nach (22.1) auf die schwere Masse m die Kraft $\pmb { F } = m \pmb { G }$ . Auf Grund der Gleichheit von träger und schwerer Masse (s. 4.4) ist daher die Beschleunigung einer Masse im Gravitationsfeld gleich der Gravitationsfeldstärke:

$$
\boldsymbol {a} = \boldsymbol {G}. \tag {22.3}
$$

Da auf der Erdoberfläche die Feldkraft (22.1) gleich der Gewichtskraft $m \pmb { g }$ ist, ist somit die Gravitationsfeldstärke G mit dem Vektor der Schwerebeschleunigung (Fallbeschleunigung) g identisch.

Zur Darstellung des Gravitationsfeldes erinnern wir uns an das NEWTONsche Gravitationsgesetz (8.2), wonach sich zwei Massen m und M wechselseitig mit einer Kraft anziehen, die dem Produkt beider Massen direkt und dem Quadrat ihres Abstandes umgekehrt proportional ist. Befindet sich M im Koordinatenursprung, so ist die an m angreifende Kraft F stets zum Ursprung (auf das Kraftzentr<u>um M) ger</u>ichtet. Der von M nach m weisende Ortsvektor $\pmb { r } = x \pmb { i } + y \pmb { j } + z \pmb { k }$ vom Betrag $r = { \sqrt { x ^ { 2 } + y ^ { 2 } + z ^ { 2 } } }$ definiert den Einheitsvektor $\boldsymbol { r } / r = \boldsymbol { e } _ { l }$ in radialer Richtung (vom Kraftzentrum weg).

Somit gilt für den Vektor der **Gravitationskraft** nach (8.2)

$$
\boldsymbol {F} = - F \boldsymbol {e} _ {r} = - \frac {\gamma m M}{r ^ {2}} \boldsymbol {e} _ {r}, \quad \text {Betrag} \quad F = \frac {\gamma m M}{r ^ {2}} \tag {22.4}
$$

mit der Gravitationskonstanten (8.3) $\gamma = 6 , 6 7 4 \cdot 1 0 ^ { - 1 1 } \mathrm { N } \cdot \mathrm { m } ^ { 2 } / \mathrm { k g } ^ { 2 }$

Wegen (22.1) folgt damit als **Gravitationsfeldstärke** im Abstand r von der Masse M

$$
\boldsymbol {G} = \frac {\boldsymbol {F}}{m} = - G \boldsymbol {e} _ {r} = - \frac {\gamma M}{r ^ {2}} \boldsymbol {e} _ {r}, \quad \text {Betrag} \quad G = \frac {\gamma M}{r ^ {2}}. \tag {22.5}
$$

Die Feldlinien verlaufen radialsymmetrisch zum Kraftzentrum M hin (Bild 22.2). Ein solches Feld nennt man Zentralfeld, die zugehörige Kraft Zentralkraft. Die Feldstärke (22.5) nimmt ebenso wie die Schwerkraft (22.4) umgekehrt proportional zum Quadrat des Abstandes r von der Masse M ab (Bild 22.3a).

![](images/page_257_image_2.jpg)

<details>
<summary>text_image</summary>

M
P₁ (1)
P₂
(2)
V₁
V₂
G
</details>

Bild 22.2 Verlauf der Feldlinien des Gravitationsfeldes G und zweier Äquipotenzialflächen $V _ { 1 }$ und $V _ { 2 }$ in der Umgebung einer Punktmasse M

![](images/page_257_image_4.jpg)

Bild 22.3 Gravitationsfeldstärke $G ( r )$ (Bildteil a) und Gravitationspotenzial $V ( r )$ (Bildteil b) außerhalb $\left( r > R \right)$ und innerhalb $\left( r < R \right)$ einer Massenkugel vom Radius R, z. B. der Erde

(1) Verlauf außerhalb der Massenkugel (gleich dem Verlauf für eine Punktmasse M)

(2) idealer Verlauf bei konstanter Dichte

(3) realer Verlauf infolge Dichtezunahme der Erde von außen nach innen

**Potenzielle Energie, Gravitationspotenzial.** In Abschnitt 8.2 wurde die Arbeit berechnet, die aufgewandt werden muss, um einen Körper (Masse m) – wie in Bild 22.2 gezeigt – zwischen zwei Punkten $P _ { 1 }$ und $P _ { 2 }$ mit den Entfernungen $r _ { 1 }$ und $r _ { 2 }$ vom Kraftzentrum (Masse M) weg zu verschieben (Wegintegral der Kraft); sie beträgt (vgl. Gl. (8.6))

$$
W = - \int_ {r _ {1}} ^ {r _ {2}} \boldsymbol {F} \cdot \mathrm{d} \boldsymbol {r} = \gamma m M \left(\frac {1}{r _ {1}} - \frac {1}{r _ {2}}\right). \tag {22.6}
$$

Da es sich bei der Schwerkraft um ein konservatives Kraftfeld handelt (vgl. 7.1), wird der gleiche Betrag (22.6) an Arbeit wieder zurückgewonnen, wenn der Körper auf einem beliebigen Weg (etwa entlang (2) im Bild 22.2) von $P _ { 2 }$ nach $P _ { 1 }$ zurückgeführt wird, d. h., die insgesamt bei einem geschlossenen Umlauf verrichtete Arbeit ist null. Für das sog. Umlauf-Wegintegral der Kraft F bzw. der Feldstärke G gilt also

$$
\oint \boldsymbol {G} \cdot \mathrm{d} \boldsymbol {r} = 0 \quad (\text {Bedingung für die Wirbelfreiheit des Gravitationsfeldes}). \tag {22.7}
$$

Die Arbeit W lässt sich, wie bekannt, als Differenz der potenziellen Energie des Körpers in den Entfernungen $r _ { 1 }$ und $r _ { 2 }$ darstellen: $W = E _ { \mathrm { p } } ( r _ { \mathrm { 2 } } ) - E _ { \mathrm { p } } ( r _ { \mathrm { 1 } } )$ . Damit folgt aus (22.6), wenn der Nullpunkt der potenziellen Energie ins Unendliche verlegt wird, also $E _ { \mathrm { p } } ( r _ { 2 } ) = 0$ für $r _ { 2 } \to \infty ,$ für eine beliebige Entfernung $r _ { 1 } = r$ der Masse m vom Kraftzentrum M:

$$
E _ {\mathrm{p}} (r) = - \int_ {\infty} ^ {r} \boldsymbol {F} \cdot \mathrm{d} \boldsymbol {r} = - \frac {\gamma m M}{r} \quad \begin{array}{l l} & (\text {potenzielle Energie eines} \\ & \text {Körpers im Gravitationsfeld}). \end{array} \tag {22.8}
$$

Das heißt, die potenzielle Energie ist im gesamten Feld negativ, sie nimmt mit zunehmender Entfernung r vom Kraftzentrum zu und wird im Unendlichen null. Man verbindet mit dem Grenzwert $E _ { \mathrm { p } } ( r \to \infty ) = 0$ die Vorstellung, dass dort wegen $\pmb { G } \rightarrow 0$ die Bindung an das Kraftzentrum aufhört und die Masse m aus dem Zentralfeld „befreit“ ist.

Wird die Gleichung (22.8) durch die Probemasse m dividiert, so erhält man die vom Körper unabhängige Feldgröße

$$
V (r) = \frac {E _ {\mathrm{p}} (r)}{m} = - \int_ {\infty} ^ {r} \boldsymbol {G} \cdot \mathrm{d} \boldsymbol {r} = - \frac {\gamma M}{r} \quad (\text {Gravitationspotenzial}). \tag {22.9}
$$

**Das Potenzial im Gravitationsfeld im Abstand r von einer Zentralmasse ist derjenigen Arbeit zahlenmäßig gleich, die gewonnen wird, wenn 1 kg Masse aus dem Unendlichen in den Abstand r gelangt.**

Aus (22.9) geht hervor, dass für $r = \mathbf { c o n s t }$ ein konstanter Wert des Potenzials V erhalten wird. Diese Flächen gleichen Potenzials, die sog. **Äquipotenzialflächen** $V = \mathbf { c o n s t } ,$ sind demnach konzentrische Kugeln um die felderzeugende Masse M (im Bild 22.2 mit $V _ { 1 }$ und $V _ { 2 }$ bezeichnet); sie werden von den Feldstärkevektoren G senkrecht durchsetzt. Äquipotenzialflächen des Schwerefeldes der Erde sind z. B. die Wasseroberflächen der Ozeane. Wird eine Masse auf einer solchen Potenzialfläche verschoben, so ist in Gleichung (22.6) $r _ { 1 } = r _ { 2 }$ und daher $W = 0$

## Bei einer Verschiebung auf einer Äquipotenzialfläche wird keine Arbeit verrichtet.

Das Gravitationspotenzial beschreibt – ähnlich wie die Feldstärke – die Intensität des Gravitationsfeldes in allen Raumpunkten (s. Bild 22.3b). Die Einführung des Potenzials bedeutet eine wesentliche Vereinfachung der Beschreibung von Vektorfeldern: Während für die Darstellung eines Kraftfeldes mit seinen drei Komponenten des Feldstärkevektors drei Ortsfunktionen erforderlich sind, genügt für das (skalare) Potenzial eine einzige. An die Stelle des Kraftfeldes $F ( r )$ bzw. $\mathbf { G } ( \pmb { r } )$ tritt so das **Potenzialfeld** $V ( { \pmb r } )$

Beim Fortschreiten im Feld G um die Strecke dr ändert sich nach (22.9) das Potenzial um d $V = - \pmb { G } \cdot \mathrm { d } \pmb { r } = - | \pmb { G } |   | \mathrm { d } \pmb { r } |$ cosα. Beim Fortschreiten auf einer Äquipotenzialfläche ist der Winkel α zwischen G und dr gleich $9 0 ^ { \circ }$ und demzufolge d $1 V = 0$ , entsprechend $V = \mathrm { c o n s t } ( \mathrm { s . o . } )$ Beim Fortschreiten um |dr | = ds senkrecht zu einer Äquipotenzialfläche, d. h. also entlang einer Feldlinie, ist $\alpha = 0 ^ { \circ }$ bzw. 180◦, und die Änderung des Potenzials dV (Abnahme bzw. Zunahme) erreicht mit cos $\alpha = \pm 1$ ihr Extremum.

**Der Vektor, der im Feld stets in Richtung der stärksten Zunahme des Potenzials V zeigt, heißt „Gradient des Potenzials“ (gradV ).**

Die Feldstärke weist also (wegen des Minuszeichens in obiger Gleichung) stets in Richtung des stärksten Potenzialgefälles, womit gilt

$$
\boldsymbol {G} (\boldsymbol {r}) = - \operatorname{grad} V (\boldsymbol {r}) \quad \text {(Feldstärke als negativer Gradient des Potenzials)} \tag {22.10}
$$

sowie $\mathbf { d } V = \mathbf { g r a d }   V \cdot \mathbf { d } \mathbf { r } = | \mathbf { g r a d }   V |   \mathbf { d } s \cdot \cos \alpha$ . In Feldrichtung $( \alpha   =   0 ^ { \circ } )$ ist |grad $V | = \mathbf { d } V / \mathbf { d } s ,$ grad $V = \left( \mathbf { d } V / \mathbf { d } s \right) \pmb { e }$ und nach $( 2 2 . 1 0 ) \; { \pmb G } = - ( { \bf d } V / { \bf d } s )   { \pmb e } .$

Fasst man im Gebirge Linien gleicher Höhe über dem Meeresspiegel als Potenziallinien auf, so lassen sich orthogonal dazu Falllinien (Feldlinien) konstruieren, entlang derer die Höhe am schnellsten abnimmt. Diese Linien folgen stets der Kraftwirkung, also fließen darauf auch Wasserläufe, Geröll, Gletscher usw. zu Tal.

## Beispiel 22.1:

Berechne aus $E _ { \mathrm { p } } = m g l$ h Gravitationspotenzial und -feldstärke auf der Erdoberfläche!

Lösung: Nach obigen Ausführungen ist $V = E _ { \mathrm { p } } / m = g h$ , grad $V = \left( \mathbf { d } V / \mathbf { d } h \right) \pmb { e } = g \pmb { e }$ und nach $( 2 2 . 1 0 ) ~ { \pmb G } = - g { \pmb e } .$ . Mit dem Einheitsvektor e in Höhenrichtung ist $G = \mathrm{const}$ ein homogenes Feld in Lotrichtung. □

## 22.3 Massen als Senken des Gravitationsfeldes

In einem Strömungsfeld (vgl. 15.1) stellt die Stromliniendichte (= Anzahl der Stromlinien/Querschnittsfläche A, welche senkrecht durchflutet wird) ein Maß für den Betrag des Vektors der Massenstromdichte $j _ { \mathrm { m } }$ dar, und der gesamte durch eine beliebige Fläche hindurchtretende Fluss, die Stromstärke $I _ { \mathbf { m } } ,$ berechnet sich nach (15.5) zu $I _ { \mathrm { m } } = \int \boldsymbol { j } _ { \mathrm { m } } \cdot \mathrm { d } \boldsymbol { A } .$ Analog ist im Gravitationsfeld die Feldlinienzahl je Flächeneinheit ein Maß für die Gravitationsfeldstärke G, und durch eine Fläche A geht der Fluss

$$
\varPhi_ {\mathrm{G}} = \int_ {(A)} \boldsymbol {G} \cdot \mathrm{d} \boldsymbol {A} \qquad (\text {Gravitationsfluss}).
$$

Denkt man sich um die im vorigen Abschnitt betrachtete Zentralmasse M im Abstand r eine Kugelfläche (mit nach außen orientierten Flächenvektoren dA) gelegt, so wird diese von den Feldlinien senkrecht von außen nach innen durchdrungen (Bild 22.2). Der Betrag der Feldstärke ist auf der Kugeloberfläche überall konstant. Mit (22.5) $G = \gamma M / r ^ { 2 }$ und der Oberfläche der Kugel $A = 4 \pi r ^ { 2 }$ erhält man für den Gravitationsfluss durch deren Oberfläche (und allgemein durch jede geschlossene Fläche):

$$
\Phi_ {\mathrm{G}} = \oint \boldsymbol {G} \cdot \mathrm{d} \boldsymbol {A} = \oint G \mathrm{d} A \cos 1 8 0 ^ {\circ} = - G \oint \mathrm{d} A = - G A = - 4 \pi \gamma M. \tag {22.11}
$$

Man erkennt: Der Gravitationsfluss wird nur von der Stoffmenge (der Masse M) im Innern des umschlossenen Gebietes bestimmt und ist von deren Verteilung unabhängig. Die Anzahl der aus dem Unendlichen kommenden Feldlinien könnte man auch durch Abzählen der Masseneinheiten bestimmen, auf denen sie jeweils enden. Alle weiteren Massen außerhalb liefern keinen Beitrag zum betrachteten Gravitationsfluss. Gäbe es einen Himmelskörper, der innen hohl ist, würden sich im Innern alle Gravitationswirkungen gegenseitig aufheben, und es würde dort Schwerelosigkeit herrschen.

Die Gravitationsfeldstärke im Innern der Erdkugel (oder eines anderen Himmelskörpers) im Abstand r vom Mittelpunkt wird also nur durch die Masse der konzentrischen Innenkugel vom Radius r bestimmt. Bei konstanter Dichte $\varrho _ { \mathrm { E } }$ ist diese $M ( r ) = 4 \pi r ^ { 3 } \varrho _ { \mathrm { E } } / 3$ , und nach (22.5) wird

$$
G (r) = \gamma \frac {4 \pi \varrho_ {\mathrm{E}}}{3} r \quad \text {bzw.} \quad G (r) = \frac {g}{R} r \tag {22.12}
$$

mit $G ( R ) = 4 \pi \gamma \varrho _ { \mathrm { E } } R / 3 = g$ als Gravitationsfeldstärke an der Erdoberfläche. Während also die Feldstärke im Innern einer homogenen Kugel proportional zu r wächst, nimmt sie außerhalb mit $1 / r ^ { 2 }$ ab (s. Bild 22.3a).

## Beispiele 22.2:

1. Die Kenntnis der Feldstärke- und Dichteverteilung $G ( r )$ und $\varrho ( r )$ im Innern von ausgedehnten Massen ermöglicht in der Geo- und Astrophysik die Berechnung der Drücke in Himmelskörpern. Analog zu Abschnitt 14.4 nimmt der Schweredruck $p$ in einer Kugel von innen nach außen gemäß $\mathbf { d } p = - \varrho G \mathbf { d } r$ bis auf den Wert null an der Kugeloberfläche ab. Berechne für konstant angenommene Dichte $\varrho _ { \mathrm { E } } = 5 , 5 \cdot 1 0 ^ { 3 }   \mathrm { k g / m ^ { 3 } }$ den Druckverlauf im Erdinnern und den Druck im Erdmittelpunkt! Erdradius $R = 6 3 8 0$ km; $g = 9 . 8 1   \mathrm { m } / \mathrm { s } ^ { 2 }$

Lösung: Mit (22.12) folgt

$$
p = - \varrho_ {\mathrm{E}} \int_ {R} ^ {r} G \mathrm{d} r = \frac {\varrho_ {\mathrm{E}} g}{2 R} (R ^ {2} - r ^ {2})
$$

und hiernach $p ( r = 0 ) = \varrho _ { \mathrm { E } } g R / 2 = 1 . 7 2 \cdot 1 0 ^ { 1 1 }   \mathrm { P a } = 1 7 2   \mathrm { G P a } \quad ( = 1 . 7 2   \mathrm { M b a r } ) !$

2. Man berechne den Verlauf des Gravitationspotenzials $V ( r )$ innerhalb einer Massenkugel von konstanter Dichte (Kurve 2 in Bild 22.3b).

Lösung: An der Kugeloberfläche ist nach (22.9) $V ( R ) = - \gamma M / R$ bzw. $V ( R ) = - g R$ wegen (22.5) $G ( R ) = g = \gamma M / R ^ { 2 }$ . Für die Verschiebungsarbeit je Masseneinheit im inneren Gravitationsfeld vom Radius r bis an die Oberfläche erhält man mit (22.12)

$$
\frac {W}{m} = V (R) - V (r) = - \int_ {r} ^ {R} \boldsymbol {G} \cdot \mathrm{d} \boldsymbol {r} = \int_ {r} ^ {R} G \mathrm{d} r = \frac {g}{R} \int_ {r} ^ {R} r \mathrm{d} r = \frac {g}{2 R} (R ^ {2} - r ^ {2});
$$

$$
V (r) = V (R) - \frac {W}{m} = - g R - \frac {g}{2 R} \left(R ^ {2} - r ^ {2}\right) = - \frac {g}{2 R} \left(3 R ^ {2} - r ^ {2}\right).
$$

3. Wie groß sind Gravitationspotenzial und potenzielle Energie im Erdmittelpunkt, wenn diese an der Erdoberfläche gleich null sind?

Lösung: Allgemein gilt für den Zusammenhang zwischen dem Potenzial $V ( r )$ und der Feldstärke $\mathbf { G } ( \boldsymbol { r } )$ , d. h., die Umkehrung von Gl. (22.10):

$$
V (r) = - \int \boldsymbol {G} (\boldsymbol {r}) \cdot \mathrm{d} \boldsymbol {r} + C = \int G (r) \mathrm{d} r + C,
$$

wobei $\boldsymbol { G } ( \boldsymbol { r } ) = - G ( r ) \boldsymbol { r } / r$ verwendet wurde und C eine Integrationskonstante ist, welche sich aus der für das Potenzial vorgegebenen Randbedingung ergibt. Mit (22.12) folgt $V ( r ) =$ $g r ^ { 2 } / ( 2 R ) + C .$ . An der Erdoberfläche $r = R$ soll das Potenzial $V ( R ) = 0$ sein; daraus ergibt sich $C = - g R / 2$ , womit folgt $V ( r ) = - g ( R ^ { 2 } - r ^ { 2 } ) / ( 2 R )$ , für den Erdmittelpunkt $r = 0 { : } V _ { 0 } = - g R / 2$ und nach (22.9) $E _ { \mathrm { p } } = - m g R / 2$ □

## 22.4 Grundaussagen der allgemeinen Relativitätstheorie

Trägheit und Schwere sind zwei Eigenschaften der Masse, die nicht notwendig miteinander identisch sein müssen. Nach der durch Präzisionsmessungen nachgewiesenen quantitativen Gleichheit von träger und schwerer Masse (vgl. 3.4, 4.4 und 8.1) kann jedoch durch kein physikalisches Experiment entschieden werden, ob das in einem beschleunigten Bezugssystem (wie z. B. im Raumschiff von Bild 5.2 bei Start und Landung) veränderte Gewicht von Körpern auf Gravitationswirkungen oder auf Trägheitskräfte (vgl. 5.1 und 5.2) zurückzuführen ist. Die Verallgemeinerung dieser Aussage auf jegliche physikalische Vorgänge in Gravitationsfeldern wird ausgedrückt als

## EINSTEINsches Äquivalenzprinzip:

**Das Gravitationsfeld in einem Inertialsystem ist hinsichtlich beliebiger physikali scher Wirkungen den Trägheitskräften in einem beschleunigten System (Nichtinertialsystem) äquivalent.**

Als fundamentales Prinzip bildet es die Grundlage für die von EINSTEIN (1915) aufgestellte **allgemeine Relativitätstheorie**, die eine Erweiterung der für unbeschleunigte Bezugssysteme (Inertialsysteme) gültigen speziellen Relativitätstheorie (s. Kapitel 6) auf beschleunigte Bezugssysteme darstellt, in denen Trägheitskräfte auftreten.

Als Beispiel soll der Einfluss eines Gravitationsfeldes auf den Gang von Uhren bzw. auf die Zeitdauer physikalischer Ereignisse untersucht werden. Dazu betrachten wir ein parallel zur x-Achse eines ruhenden Systems Σ orientiertes Gravitationsfeld, in dem zwei Uhren mit den Koordinaten $x _ { 1 }$ und $x _ { 2 }$ sowie den unterschiedlichen Zeiten $\Delta t _ { 1 }$ und $\Delta t _ { 2 }$ ruhen. Nach EINSTEIN ersetzen wir das Gravitationsfeld durch eine beschleunigte Bewegung von Σ gegenüber einem Inertialsystem $\Sigma ^ { \prime }$ (vgl. Bild 5.1). Die Uhren in $\Sigma$ passieren nacheinander mit unterschiedlichen Geschwindigkeiten $\nu _ { 1 }$ und $\nu _ { 2 }$ eine in $\Sigma ^ { \prime }$ ruhende Uhr, die infolg<u>e der relat</u>ivistische<u>n Zeitdilat</u>ation (6.11) für beide Uhren die gleiche Zeit $\Delta t ^ { \prime }$ anzeigt: $\Delta t ^ { \prime } = \Delta t _ { 1 } / \sqrt { 1 - ( \nu _ { 1 } ^ { 2 } / c ^ { 2 } ) } = \Delta t _ { 2 } / \sqrt { 1 - ( \nu _ { 2 } ^ { 2 } / c ^ { 2 } ) }$ . Mit dem Energiesatz im Schwerefeld $\nu _ { 1 } ^ { 2 } / 2   +   V _ { 1 } = \nu _ { 2 } ^ { 2 } / 2   +   V _ { 2 } = 0$ (s. 7.4 und 22.2, wobei am Potenzialnullpunkt $( V = 0 ) ~ \nu = 0$ gesetzt wurde und somit das Potenzial V im gesamten Feld negativ ist), können wir nun die Geschwindigkeiten durch die Gravitationspotenziale $V _ { 1 }$ und $V _ { 2 }$ in den Orten $x _ { 1 }$ bzw. $x _ { 2 }$ des ruhenden Systems $\Sigma$ ausdrücken, $\nu _ { 1 } ^ { 2 } = - 2 V _ { 1 } ,   \nu _ { 2 } ^ { 2 } = - 2 V _ { 2 }$ , und erhalten damit

$$
\Delta t _ {2} = \Delta t _ {1} \sqrt {\frac {1 + (2 V _ {2} / c ^ {2})}{1 + (2 V _ {1} / c ^ {2})}} \approx \Delta t _ {1} \left(1 + \frac {V _ {2} - V _ {1}}{c ^ {2}}\right) \quad (\text {gravitative Zeitdilatation}). \tag {22.13}
$$

Nach dieser Beziehung laufen physikalische Vorgänge in Orten unterschiedlichen Gravitationspotenzials verschieden schnell ab. So zeigt eine im Feld einer Zentralmasse (22.9) im Abstand $r _ { 2 }$ ruhende Uhr mit $V _ { 2 } = - \gamma M / r _ { 2 }$ gegenüber eine<u>r im feldfreien</u> Raum ruhenden Uhr, $V _ { 1 } = V ( r _ { 1 } \to \infty ) = 0$ , nach (22.13) die Zeitdilatation $\Delta t _ { 2 } = \Delta t _ { 1 } \sqrt { 1   -   2 \gamma M / ( c ^ { 2 } r _ { 2 } ) }$ , d. h. $\Delta t _ { 2 } < \Delta t _ { 1 }$ , Uhren im Schwerefeld gehen langsamer. Dieser als gravitative Zeitdilatation bezeichnete Effekt ist auch die Ursache der gravitativen Rotverschiebung, die eine elektromagnetische Welle der Frequenz $f$ im Gravitationsfeld erfährt. Mit $f _ { 1 } = 1 / \Delta t _ { 1 } , f _ { 2 } = 1 / \Delta t _ { 2 }$ beträgt sie $f _ { 1 } = f _ { 2 } \sqrt { ( 1   +   2 V _ { 2 } / c ^ { 2 } ) / ( 1   +   2 V _ { 1 } / c ^ { 2 } ) }$ bzw. im Feld der Zentralmasse $f _ { 1 } = f _ { 2 } \sqrt { 1 - 2 \gamma M / ( c ^ { 2 } r _ { 2 } ) }$ , so dass eine von $r _ { 2 }$ nach außen emittierte Lichtwelle der Frequenz $f _ { 2 }$ eine Rotverschiebung $f _ { 1 } < f _ { 2 }$ erfährt (s. 43.4). Für $r _ { 2 } \leq R _ { \mathrm { S } }$ mit $R _ { \mathrm { S } } = 2 \gamma M / c ^ { 2 }$ als dem sog. SCHWARZSCHILDradius ist $f_{1} = 0;$ von M kann keine Strahlungsenergie mehr entweichen, sie bildet ein sog. **schwarzes Loch**.

Auch der allgemein-relativistische Effekt der Lichtablenkung im Schwerefeld einer Zentral masse wie z. B. der Sonne wird durch das EINSTEINsche Äquivalenzprinzip erklärt. Da Licht aufgrund der Energie-Masse-Beziehung (7.21) $E = m c ^ { 2 }$ sowohl eine schwere als auch träge Masse zukommt, erfährt ein Lichtstrahl eine gravitative Anziehung im Schwerefeld in Form einer gekrümmten Bahn. Diese kann ebenfalls auf die ablenkende Wirkung von Trägheitskräften in einem gravitationsfreien aber beschleunigten Bezugssystem zurückgeführt werden. Für den Ablenkwinkel α eines Lichtstrahls, der eine Zentralmasse im Abstand r passiert, ergibt sich mit $\alpha \approx ( V _ { 2 } ( \infty )   -   V _ { 1 } ( r ) ) / c ^ { 2 } = \gamma M / ( c ^ { 2 } r )$ eine ähnliche Abhängigkeit wie in (22.13). Das exakte Resultat ist $\alpha = 4 \gamma M / ( c ^ { 2 } r )$ , womit für den Fall der Ablenkung am Sonnenrand der Wert $\alpha = 1 { , } 7 5 4 ^ { \prime \prime }$ (Winkelsekunden) resultiert, der sehr gut mit gemessenen Werten zwischen $^ { 1 , 6 1 } ^ { \prime \prime }$ und $^ { 2 , 2 4 ^ { \prime \prime } }$ übereinstimmt.

Diese durch die Anwesenheit von Massen im Raum hervorgerufenen Bahnkrümmungen der Lichtstrahlen und Körperbewegung sind nach EINSTEIN Ausdruck einer Krümmung des vierdimensionalen Raum-Zeit-Kontinuums, im Unterschied zum flachen oder EUKLIDischen vierdimensionalen Raum-Zeit-Kontinuum der speziellen Relativitätstheorie. Die Gravitation wird so zu einer geometrischen Eigenschaft des Raumes.

![](images/page_262_image_4.jpg)

<details>
<summary>natural_image</summary>

3D wireframe diagram of a curved surface with grid lines and a small object at the base (no text or symbols)
</details>

Bild 22.4 Veranschaulichung der Krümmung des Raumes durch eine Gummimembran, die von einer Masse M (links) und einer zweiten Masse, die nur ein Zehntel von M beträgt (rechts) deformiert wird

Zur Verdeutlichung sei hier auf die in Abschnitt 22.1 beschriebene Gummimembran verwiesen, die als Modellvorstellung für eine gekrümmte zweidimensionale Welt dienen kann. Wird an einer Stelle der waagrecht ausgespannten Membran eine Kugel aufgelegt – wie in Bild 22.4 veranschaulicht, so kommt es aufgrund ihrer Schwerkraft in der Umgebung zu einer Deformation des ’‘Raumes“ in Form einer flach auslaufenden Delle, deren Krümmung mit zunehmender Entfernung von der Kugel stetig abnimmt, entsprechend zur Abnahme der Schwerkraft mit der Entfernung von der Zentralmasse, die eine Senke des Gravitationsfeldes bildet (s. 22.3 und Bild 22.2). Eine zweite Kugel von sehr viel kleinerer Masse, die – im Bild rechts zu sehen – sich am Hang der Membrandelle, d. h. im Einflussbereich der ersten Kugel, befindet, wird aufgrund der auf sie wirkenden „Hangabtriebskraft“ zum untersten Punkt der Delle, dem Ort der ersten (schweren) Kugel als Zentralmasse, hin beschleunigt, analog zur Wirkung der durch die Raumkrümmung verursachten Massenanziehungskraft.

**Zum Einheitensystem.** Im Zusammenhang mit der Behandlung des elektrischen Feldes macht es sich erforderlich, das System der mechanischen Basiseinheiten durch Hinzunahme einer neuen Basiseinheit aus dem Bereich des Elektromagnetismus zu erweitern. Das Internationale Einheitensystem (SI) setzt die Einheit der elektrischen Stromstärke, das **Ampere (A)**, als unabhängige Basiseinheit zusätzlich zu den mechanischen Basiseinheiten **Meter, Kilogramm** und **Sekunde** fest (MKSA-System). Alle anderen Einheiten elektromagnetischer Größen leiten sich dann aus den genannten vier Basiseinheiten ab. Der Zusammenhang zwischen den abgeleiteten Einheiten für mechanische und elektrische Größen ist durch die folgende Beziehung zwischen den **Energieeinheiten** gegeben:

$$
1 \mathrm{J} = 1 \mathrm{N} \cdot \mathrm{m} = 1 \mathrm{kg} \cdot \mathrm{m} ^ {2} \cdot \mathrm{s} ^ {- 2} = 1 \mathrm{W} \cdot \mathrm{s} = 1 \mathrm{V} \cdot \mathrm{A} \cdot \mathrm{s} \tag {23.1}
$$

mit den abgeleiteten Einheiten J o u l e (J) für die Arbeit bzw. Energie, N e w t o n (N) für die Kraft, W a t t (W) für die Leistung und $\mathrm { ~ V ~ o ~ l ~ t ~ } ( \mathrm { V } )$ für die elektrische Spannung (vgl. 23.4). Die Einheit der elektrischen Ladung, von der wir im Folgenden ausgehen, ist wegen der Definition für die elektrische Stromstärke (25.3) 1 Amperesekunde (A · s) = 1 C o u l o m b (C). Ein Strom von 1 Ampere entnimmt z. B. einer Batterie je Sekunde die Ladung 1 Coulomb.

## 23.1 Die elektrische Ladung. Ladungsnachweis

Elektrische Ladungen haben ihren Ursprung in der Existenz der beiden subatomaren Teilchen **Proton** und **Elektron**. Diese Teilchen kommen in jedem Stoff vor und verkörpern die kleinsten Mengen der beiden sich durch das Vorzeichen unterscheidenden Arten von Elektrizität, der positiven im Falle des Protons und der negativen im Falle des Elektrons.

Ladungen haben die Eigenschaft, **abstoßende** bzw. **anziehende Kräfte** aufeinander auszuüben, je nachdem, ob es sich um die Wechselwirkung zweier gleichartiger (gleichnamiger) bzw. zweier ungleichartiger (ungleichnamiger) Ladungsträger handelt. Die Größe einer elektrischen Ladung kann durch die Kraftwirkung gemessen werden, die von ihr auf eine andere Ladung ausgeübt wird.

## Zwei austauschbare Ladungen sind einander gleich, wenn eine dritte bei gleicher Anordnung auf beide nacheinander die gleiche Kraft ausübt.

Diese Erfahrungstatsachen bilden die Grundlage der **Elektrostatik**, desjenigen Zweiges der Physik, der sich mit den Kräften zwischen ruhenden elektrischen Ladungen infolge der von ihnen ausgehenden elektrischen Felder und den durch diese Kräfte bedingten Gleichgewichtszuständen beschäftigt. Erste genauere Versuche zur Elektrostatik hat OTTO VON GUERICKE um 1660 angestellt und 1672 publiziert.

Elektron und Proton tragen je eine vom Betrag gleich große elektrische Ladung

$$
e = 1, 6 0 2   1 7 6   6 3 4 \cdot 1 0 ^ {- 1 9}   \mathrm{C} \qquad \text {(Elementarladung)}.
$$

Sie ist bei den Elektronen an die (Ruh-)Masse $m _ { \mathrm { e } } = 9 , 1 0 9   3 8 2 \cdot 1 0 ^ { - 3 1 }$ kg gebunden; somit ist

$$
\frac {e}{m _ {\mathrm{e}}} = - 1, 7 5 8   8 2 0 \cdot 1 0 ^ {1 1}   \frac {\mathrm{C}}{\mathrm{kg}} \quad \text {(spezifische Ladung des Elektrons).}
$$

Für die Existenz einer kleinsten negativen Elektrizitätsmenge, eines „Atoms der Elektrizität“mit der Ladung −e, spricht eine Reihe experimenteller Befunde, wie z. B. die FARADAYschen Gesetze der Elektrolyse (vgl. 26.4), wonach die Ionen als Träger der Elektrizität stets ganzzahlige Vielfache dieser Ladung besitzen, weiterhin die Aufklärung der Natur der Katodenstrahlen (vgl. 27.2), die sich als aus den Atomen des Katodenmaterials kommende kleinste negative Elektrizitätsträger erwiesen. Die erste zuverlässige Messung der Elementarladung e gelang MILLIKAN 1910 (vgl. 23.3).

Da die Atome aus einer ebenso großen Zahl von Teilchen mit positiver Ladung wie solchen mit negativer Ladung „bestehen“, bedeutet die **Aufladung** eines Körpers die Vermehrung der Elektrizitätsteilchen einer Art. Der Körper, der Elektronen abgibt, behält eine positive Überschussladung; der Körper, in dem sich Elektronen ansammeln, wird negativ geladen. Aus Atomen, die Elektronen abgeben (bzw. aufnehmen), entstehen positive (bzw. negative) Ionen. Man kann also niemals eine Ladung eines Vorzeichens allein erzeugen; es gilt vielmehr für die Elektrizität der

## Ladungserhaltungssatz: In einem abgeschlossenen System bleibt die Summe aus darin enthaltenen positiven und negativen Ladungen konstant.

Die Stärke der Bindung der Elektronen an die Atome ist in den verschiedenen Stoffen unterschiedlich. In den **Isolatoren** (Glas, Hartgummi u. ä.) sind die Elektronen fest an die Atome gebunden und daher im Stoff nicht ohne Weiteres verschiebbar, so dass von außen aufgebrachte Ladungen dort haften bleiben, wo sie zugeführt werden. In **Metallen** hingegen sind stets ein oder mehrere Elektronen je Atom, die sog. Leitungselektronen, frei beweglich und unter der Wirkung elektrischer Kräfte leicht verschiebbar. Wegen dieser Eigenschaft sind die Metalle **elektrische Leiter** (vgl. 26.1).

**Ladungsnachweis.** Für die Messung elektrischer Ladungen werden Elektrometer benutzt. Das BRAUNsche Elektrometer (Bild 23.1a) besteht aus einem geerdeten Metallgehäuse, in das die Messelektrode isoliert eingeführt ist. Diese trägt einen Metallbügel mit daran befestigtem Zeiger. Wird eine elektrische Ladung auf die Messelektrode und damit auf das Anzeigesystem übertragen, so schlägt der Zeiger aus, da er jetzt Ladungen des gleichen Vorzeichens wie der Bügel trägt und deshalb vom Bügel abgestoßen wird. Der Ausschlag wächst monoton mit der aufs Elektrometer übertragenen Ladung. Um die Empfindlichkeit zu steigern, werden Elektrometer meist mit einem konstanten Hilfsfeld ausgestattet, das sich beim Einfadenelektrometer (Bild 23.1b) zwischen den Platten eines Kondensators nach Anschluss einer Spannungsquelle ausbildet. An der zu messenden Ladung auf dem Metallfaden greift eine Kraft an, die eine mikroskopisch beobachtbare Durchbiegung des Fadens bewirkt.

![](images/page_265_image_2.jpg)

Bild 23.1 a) Braunsches Elektrometer, b) Einfadenelektrometer

Beim ballistischen Galvanometer wird der Körper, dessen Ladung gemessen werden soll, über ein dazwischen geschaltetes Drehspulgalvanometer (zu dessen Funktionsprinzip vgl. 28.6) entladen. Ist die Entladungsdauer klein gegenüber der Schwingungsdauer des Galvanometers, so ruft der bei der Entladung auftretende Stromstoß einen Endausschlag des Galvanometers hervor, welcher der zu messenden Ladung proportional ist (s. das Beispiel 33.4).

## 23.2 Ladungen als Quellen bzw. Senken des elektrischen Feldes

Statische elektrische Felder haben ihren Ursprung in ruhenden elektrischen Ladungen. Zur modellmäßigen Darstellung der Felder bedienen wir uns nach FARADAY (1852) des Kraftlinienoder Feldlinienbildes (vgl. 22.1), welches ein anschauliches Bild der Verteilung der Feldstärke vermittelt. Die Feldlinien beschreiben den Weg, auf dem man fortschreiten muss, um immer der Richtung der elektrischen Feldstärke zu folgen. Sie geben so in allen Punkten des Raumes die Kraftwirkungsrichtungen auf weitere, in das Feld gebrachte elektrische Ladungen an. Den Feldverlauf kann man sichtbar machen, wenn in das elektrische Feld eine Glasplatte gebracht und diese mit kleinen Gipskriställchen bestreut wird, die sich unter der Wirkung des elektrischen Feldes – ähnlich wie Eisenfeilspäne im Magnetfeld – in Richtung des Feldes ordnen.

Die Feldlinien eines elektrostatischen Feldes beginnen und enden stets in elektrischen Ladungen. Als Richtungssinn der Feldlinien wird die Richtung von der positiven zur negativen Ladung festgelegt. Es gibt demnach hier keine in sich geschlossenen Feldlinien (Wirbel):

**Das elektrostatische Feld ist ein wirbelfreies Quellenfeld. Die positiven Ladungen sind die Quellen, die negativen Ladungen die Senken (negative Quellen) des elektrischen Feldes.**

Betrachten wir eine einzelne positive **Punktladung** (Bild 23.2a), so erzeugt diese (analog zum Gravitationsfeld einer Punktmasse in Bild 22.2) ein radialsymmetrisches Feld. Die polar entgegengesetzte (negative) Ladung denken wir uns in sehr großer Entfernung („im Unendlichen“). Bei einer negativen Punktladung sind die Feldlinien zur Ladung hin gerichtet. Die Feldlinienbilder zwischen zwei ungleichnamigen bzw. gleichnamigen Punktladungen (Bild 23.2b und c) ergeben sich durch Überlagerung zweier radialsymmetrischer Felder entsprechender Richtung.

Die Feldlinienbilder lassen aus der Dichte des Feldlinienverlaufs unmittelbar Rückschlüsse auf den Betrag der Feldstärke an verschiedenen Punkten des Feldes zu:

**Je dichter die elektrischen Feldlinien verlaufen, umso stärker ist an der betreffenden Stelle das Feld.**

![](images/page_266_image_4.jpg)

Bild 23.2 Feldlinienbild a) einer Punktladung, b) zweier ungleichnamiger Punktladungen (elektrischer Dipol), c) zweier gleichnamiger Punktladungen. Die Feldlinien durchdringen die Äquipotenzialflächen $\varphi = \mathsf { c o n s t }$ (dünne Linien) senkrecht; vgl. Abschnitt 23.4.

Bei inhomogenen Feldern wie in Bild 23.2 nimmt somit in den Richtungen, in denen die Feldlinien auseinander laufen, die Feldstärke ab, in entgegengesetzter Richtung zu. In homogenen Feldern, in denen die Feldlinien überall parallel in gleichem Abstand voneinander verlaufen, ist die Feldstärke räumlich nach Betrag und Richtung konstant.

## 23.3 Kraftwirkungen des elektrischen Feldes. Elektrische Feldstärke

Elektrische Felder üben Kräfte auf elektrisch geladene Körper aus. Diese Kraftwirkungen charakterisieren das elektrische Feld als Kraftfeld. Zur „Ausmessung“ eines elektrischen Feldes benutzt man eine Probeladung q, die so klein gewählt wird, dass sie das zu untersuchende Feld nicht wesentlich stört. Man kann nun den Feldverlauf prinzipiell dadurch bestimmen, dass man an den verschiedenen Orten des felderfüllten Raumes die Kraft F auf diese Probeladung nach Betrag und Richtung misst. Diese Kraft hängt aber außer von der Stärke des Feldes noch von der kleinen (bekannten) Probeladung q ab. Um eine reine Feldgröße zu erhalten, muss deshalb die gemessene Kraft noch durch die Größe der Probeladung dividiert werden.

**Die elektrische Feldstärke ist gleich dem Quotienten aus der auf eine Probeladung wirkenden Feldkraft und der Probeladung.**

$$
\boldsymbol {E} = \frac {\boldsymbol {F}}{q}; \quad \text {Einheit:} [ E ] = 1 \frac {\mathrm{N}}{\mathrm{C}} = 1 \frac {\mathrm{Nm}}{\mathrm{Cm}} = 1 \frac {\mathrm{Ws}}{\mathrm{Asm}} = 1 \frac {\mathrm{VAs}}{\mathrm{Asm}} = 1 \frac {\mathrm{V}}{\mathrm{m}};
$$

$$
\boldsymbol {F} = q \boldsymbol {E} \quad (\text {Feldkraft}). \tag {23.2}
$$

Feldkraft F und Feldstärke E haben in jedem Punkt des Raumes die Richtung der Tangente an die Feldlinie.

Die Kraftwirkung des elektrischen Feldes auf Ladungen wird bei der **MILLIKAN-Methode** (1910) zur Bestimmung der Größe der Elementarladung e ausgenutzt (Bild 23.3): Im (homogenen) Feld eines Plattenkondensators werden kleine Öltröpfchen mit einem Mikroskop beobachtet, die durch Zerstäuben von Öl erzeugt werden, wodurch sie sich auf kleine ganzzahlige Vielfache der Elementarladung ze aufladen. Aus der Sinkgeschwindigkeit der Tröpfchen im ungeladenen Kondensator $( E = 0 )$ wird deren Radius bzw. Masse m bestimmt (s. Kugelfallviskosimeter, Beispiel 15.2/2). Legt man dann eine veränderliche Spannung an den Kondensator, so findet man Feldstärken $E ,$ für die einzelne Tröpfchen in der Schwebe gehalten werden, bei denen also die Feldkraft der Gewichtskraft das Gleichgewicht hält: $z e E = m g$ . Die größte Feldstärke, bei der noch Tröpfchen schweben, entspricht $z = 1$ und liefert die Größe ihrer Ladung $e \approx 1 { , } 6 { \cdot } 1 0 ^ { - 1 9 } \mathrm { C }$

![](images/page_267_image_3.jpg)

<details>
<summary>text_image</summary>

+ + + + +
→
→
→
→
→
→
→
→
←zeE
mg
</details>

Bild 23.3 Millikan-Methode zur Bestimmung der Elementarladung e

**Dipol im elektrischen Feld.** An einem Dipol, bestehend aus den im Abstand l befindlichen gleich großen, aber ungleichnamigen punktförmigen Ladungen −q und +q, deren Positionen im elektrischen Feld $\boldsymbol { E } = \boldsymbol { E } ( \boldsymbol { r } )$ durch die Ortsvektoren $r _ { 1 }$ und $r _ { 2 }$ beschrieben sein mögen, greifen die Kräfte $\pmb { F } _ { 1 } = - q \pmb { E } _ { 1 }$ und $\pmb { F } _ { 2 } = \pm q \pmb { E } _ { 2 }$ an. Diese bewirken eine resultierende Kraft

$$
\boldsymbol {F} = \boldsymbol {F} _ {1} + \boldsymbol {F} _ {2} = (- q \boldsymbol {E} _ {1}) + (+ q \boldsymbol {E} _ {2}) = q (\boldsymbol {E} _ {2} - \boldsymbol {E} _ {1}) = q \Delta \boldsymbol {E} \tag {23.3}
$$

sowie ein resultierendes Drehmoment (10.5)

$$
\boldsymbol {M} = \boldsymbol {r} _ {1} \times \boldsymbol {F} _ {1} + \boldsymbol {r} _ {2} \times \boldsymbol {F} _ {2} = \boldsymbol {r} _ {1} i \times (- q \boldsymbol {E} _ {1}) + \boldsymbol {r} _ {2} \times (+ q \boldsymbol {E} _ {2}). \tag {23.4}
$$

Im homogenen Feld (Bild 23.4a) ist $\boldsymbol{E}_{1}=\boldsymbol{E}_{2}=\boldsymbol{E}$ . Die resultierende Kraft (23.3) verschwindet, und es verbleibt nach (23.4) nur das Drehmoment

$$
\boldsymbol {M} = q (\boldsymbol {r} _ {2} - \boldsymbol {r} _ {1}) \times \boldsymbol {E} = q \boldsymbol {l} \times \boldsymbol {E} = \boldsymbol {p} \times \boldsymbol {E} \tag {23.5}
$$

vom Betrage $M = q l E$ sinα, das darauf hinwirkt, den Dipol in die Feldrichtung zu drehen.

![](images/page_267_image_12.jpg)

Bild 23.4 Dipol a) im homogenen Feld, b) im inhomogenen Feld

Der von der negativen zur positiven Ladung weisende Vektor in Gleichung (23.5)

$$
\boldsymbol {p} = q \boldsymbol {l}, \quad \text {Einheit:} [ p ] = 1 \mathrm{C} \cdot \mathrm{m} = 1 \mathrm{A} \cdot \mathrm{s} \cdot \mathrm{m}, \tag {23.6}
$$

heißt **elektrisches Dipolmoment**. Zeigt der Vektor der Dipolachse l in Richtung des homoge nen Feldes $( \alpha = 0 ^ { \circ } )$ , so wird das Drehmoment $M = 0$ , und der Dipol befindet sich im stabilen Gleichgewicht. Zeigt die Dipolachse l entgegen der Feldrichtung $( \alpha = 1 8 0 ^ { \circ } )$ , ist ebenfalls $M = 0$ , jedoch befindet sich dann der Dipol in einem labilen Gleichgewicht (s. Beispiel 23.1/2). Im inhomogenen Feld dagegen, in dem die Feldstärke nach Betrag und Richtung von Ort zu Ort verschieden ist, kann sich ein Dipol nicht im Gleichgewicht befinden. Selbst wenn er sich wie in Bild 23.4b in Feldrichtung einstellt, wodurch das Drehmoment verschwindet, verbleibt wegen $\Delta \boldsymbol{E} = \boldsymbol{E}_{2} - \boldsymbol{E}_{1} \neq 0$ eine resultierende Kraft (23.3), die in diesem Falle den Dipol in das Feld hineintreibt. Dies führt u. a. zur **Ion-Dipol-Wechselwirkung:** Anlagerung von neutralen Molekülen mit großem Dipolmoment an Ionen, die z. B. bei Wasser mit $H _2 O + H ^+\rightarrow  H _3 O ^+$ beginnt (Hydratation).

## Beispiele 23.1:

1. Welche Feldstärke E bzw. Spannung (23.15) $U = E d$ ist bei der MILLIKAN-Methode an den Kondensatorplatten von Bild 23.3 (Abstand $d = 5   \mathrm { m m }$ erforderlich, um ein Öltröpfchen (Durchmesser $2R = 1\mu m;$ Dichte $\varrho = 0 , 8 6   \mathrm { g } / \mathrm { c m } ^ { 3 }$ , welches eine elektrische Ladung vom Dreifachen der Elementarladung e trägt, in Luft in der Schwebe zu halten?

Lösung: Die Auftriebskraft des Tröpfchens kann vernachlässigt werden. Aus dem Gleichgewicht von Feldkraft und Schwerkraft $3 e E = 3 e U / d = m g$ folgt mit $\varrho = 0 , 8 6 \cdot 1 0 ^ { 3 }   \mathrm { k g / m } ^ { 3 }$ $R =$ $0 { , } 5 \cdot { { 1 0 } ^ { - 6 } }$ m und $d = 5 \cdot 1 0 ^ { - 3 }$ m als Tröpfchenmasse $m = \varrho ( 4 / 3 ) \pi R ^ { 3 } = 4 { , } 5 \cdot 1 0 ^ { - 1 6 }$ kg und damit $E = 9 { , } 2   \mathrm { k V / m }$ bzw. $U = 4 6 \mathrm { V } .$

2. Man berechne die potenzielle Energie eines Dipols mit dem Dipolmoment $\pmb { p }$ in einem homogenen äußeren Feld $E = \mathbf{const}$ (Bild 23.4a) und beurteile die stabile und die labile Gleichgewichtslage.

Lösung: Zur Berechnung können analog (22.8) entweder aus dem Unendlichen $- q$ nach $P _ { 1 }$ und $+ q$ nach $P _ { 2 }$ verschoben werden, oder man denkt sich in $P _ { 1 }$ eine Ladungstrennung $( - q ) +$ $q = 0$ und führt +q nach $P _ { 2 }$ :

$$
\begin{array}{l} E _ {\mathrm{p}} = - \int_ {\infty} ^ {P _ {1}} (- q \boldsymbol {E}) \cdot \mathrm{d} \boldsymbol {r} - \int_ {\infty} ^ {P _ {2}} (+ q \boldsymbol {E}) \cdot \mathrm{d} \boldsymbol {r} = - \int_ {P _ {1}} ^ {\infty} q \boldsymbol {E} \cdot \mathrm{d} \boldsymbol {r} - \int_ {\infty} ^ {P _ {2}} q \boldsymbol {E} \cdot \mathrm{d} \boldsymbol {r} \\ = - \int_ {P _ {1}} ^ {P _ {2}} q \boldsymbol {E} \cdot \mathrm{d} \boldsymbol {r} = - q \boldsymbol {E} \cdot (\boldsymbol {r} _ {2} - \boldsymbol {r} _ {1}) = - q \boldsymbol {l} \cdot \boldsymbol {E} = - \boldsymbol {p} \cdot \boldsymbol {E}. \\ \end{array}
$$

Die potenzielle Energie $E _ { \mathbf { p } } = - { \pmb { p } } \cdot { \pmb { E } } = - p E$ cosα hat für $\alpha = 0 ^ { \circ }$ ihr Minimum (stabiles Gleichgewicht, vgl. Abschnitt 10.5) und für $\alpha = 1 8 0 ^ { \circ }$ ihr Maximum (labiles Gleichgewicht). □

## Aufgabe

**23.1** Bei einem elektrischen Pendel hängt ein kleines geladenes Kügelchen an einem isolierenden Faden in einem horizontalen homogenen elektrischen Feld. Durch die Kraftwirkung des elektrischen Feldes erfolgt eine statische Auslenkung des Kügelchens um einen Winkel α aus der Lotrichtung. Wie groß ist die elektrische Feldstärke, wenn die spezifische Ladung des Kügelchens $q / m = 3 0 0   \mu \mathrm { C } / \mathrm { k g }$ beträgt und $\alpha = 2 2 ^ { \circ }$ ist? Gleichgewicht herrscht, wenn die Resultierende aus horizontaler Feldkraft $q E$ und vertikaler Gewichtskraft $m \pmb { g }$ in Richtung des Fadens zeigt und so durch dessen Spannkraft kompensiert wird.

## 23.4 Elektrostatisches Potenzial. Spannung

Um in einem äußeren elektrostatischen Feld die Ladung $q ,$ an der das Feld mit der Kraft $q E$ angreift, von $P _ { 1 }$ nach $P _ { 2 }$ zu verschieben (Bild 23.5), ist nach (7.3) die Arbeit

$$
W = - \int_ {P _ {1}} ^ {P _ {2}} \boldsymbol {F} \cdot \mathrm{d} \boldsymbol {r} = - q \int_ {P _ {1}} ^ {P _ {2}} \boldsymbol {E} \cdot \mathrm{d} \boldsymbol {r} \quad (\text {Verschiebungsarbeit im elektrischen Feld}) \tag {23.7}
$$

zu verrichten. Da das elektrostatische Feld ebenso wie das Gravitationsfeld wirbelfrei ist (vgl. 22.2), muss das Umlauf-Wegintegral verschwinden:

$$
\oint \boldsymbol {E} \cdot \mathrm{d} \boldsymbol {r} = 0 \quad \begin{array}{l} (\text {Bedingung für die Wirbelfreiheit} \\ \text {des elektrostatischen Feldes}). \end{array} \tag {23.8}
$$

Deshalb kann das wirbelfreie Vektorfeld E durch eine skalare Ortsfunktion $\varphi ( \pmb { r } )$ beschrieben werden, deren Nullpunkt bei Zentralfeldern $( \mathbf { z } , \mathbf { B } .$ von Punktladungen) im Unendlichen festgelegt wird, bei elektrischen Geräten bzw. Anlagen jedoch meist am Gehäuse bzw. auf dem Erdboden (Nullpotenzial). Diese Funktion $\varphi$ heißt **elektrostatisches Potenzial**. Analog zum Gravitationspotenzial (22.9) ist das elektrostatische Potenzial im Punkt $P$ des Feldes definiert durch

$$
\varphi (P) = - \int_ {\infty} ^ {P} \boldsymbol {E} \cdot \mathrm{d} \boldsymbol {r} \quad (\text {elektrostatisches Potenzial}). \tag {23.9}
$$

Im Feld $\pmb { E } = E \pmb { e }$ folgt für eine sehr kleine Verschiebung $| \mathbf { d } \boldsymbol { r } | = \mathbf { d } s$ als Potenzialänderung dϕ = $- \mathbf { \nabla } E \cdot \mathbf { d } \mathbf { r } = - E$ ds cosα. Bei einer Verschiebung in Richtung des Feldes $( \alpha = 0 ^ { \circ } )$ ist dann analog zu (22.10)

$$
\boldsymbol {E} = - \frac {\mathrm{d} \varphi}{\mathrm{d} s} \boldsymbol {e} = - \operatorname{grad} \varphi \quad \begin{array}{l} (\text {elektrische Feldstärke als} \\ \text {Gradient des Potenzials} \varphi). \end{array} \tag {23.10}
$$

![](images/page_269_image_11.jpg)

Bild 23.5 Zum Potenzial- und Spannungsbegriff im elektrostatischen Feld: a) Die Verschiebungsarbeit zwischen zwei Punkten des Feldes ist unabhängig vom Weg; b) Berechnung der Spannungen zwischen je zwei Punkten im homogenen Feld (s. Beispiel 23.2)

Die Feldstärke erhält man also durch Bildung des negativen Gradienten von ϕ (vgl. 22.2). Es handelt sich dabei um einen Vektor, der im Feld stets die Richtung der maximalen Abnahme des Potenzials angibt; diese Richtung entspricht dem Verlauf der Feldstärke E. Mit Hilfe des Potenzials (23.9) lässt sich die Verschiebungsarbeit (23.7) wie folgt schreiben:

$$
W = - q \left(\int_ {P _ {1}} ^ {\infty} \boldsymbol {E} \cdot \mathrm{d} \boldsymbol {r} + \int_ {\infty} ^ {P _ {2}} \boldsymbol {E} \cdot \mathrm{d} \boldsymbol {r}\right) = q (\varphi_ {2} - \varphi_ {1}) = E _ {\mathrm{p}} (P _ {2}) - E _ {\mathrm{p}} (P _ {1}), \tag {23.11}
$$

entsprechend einer Änderung der potenziellen Energie $E _ { \mathrm { p } }$ der Ladung $q$ zwischen den Feldpunkten $P _ { 1 }$ und $P _ { 2 }$ . Hieraus folgt:

**Das elektrostatische Potenzial in einem Punkt des elektrostatischen Feldes ist gleich dem Quotienten aus der potenziellen Energie einer Probeladung in diesem Punkt und der Probeladung.**

$$
\varphi = \frac {E _ {\mathrm{p}}}{q} \quad \text {Einheit:} [ \varphi ] = 1 \frac {\mathrm{Nm}}{\mathrm{As}} = 1 \frac {\mathrm{Ws}}{\mathrm{As}} = 1 \mathrm{Volt(V).} \tag {23.12}
$$

Die Potenzialdifferenz $\Delta \varphi = \varphi _ { 2 } - \varphi _ { 1 } = U$ nennt man **Spannung** zwischen den Punkten $P _ { 1 }$ und $P _ { 2 }$ des Feldes. Aus (23.11) folgt somit:

**Die Spannung zwischen zwei Punkten des elektrostatischen Feldes ist gleich dem Quotienten aus der Arbeit, die zur Verschiebung einer Probeladung zwischen diesen Punkten erforderlich ist, und der Probeladung.**

$$
U = \frac {W}{q} \quad \text {Einheit:} \quad [ U ] = 1 \frac {\mathrm{Nm}}{\mathrm{As}} = 1 \mathrm{V}. \tag {23.13}
$$

Die Energieaufnahme einer Ladung hängt somit nur von der durchlaufenen Spannung U ab. Durchläuft ein Teilchen mit der Elementarladung $q = e = 1 { , } 6 0 2   1 7 6   6 3 4   { \cdot }   1 0 ^ { - 1 9 }   \mathrm { C }$ die Spannung von 1V, so beträgt seine Energiezunahme

$$
\textbf{1 Elektronvolt (eV)} = 1,602   176   634 \cdot 10^{-19}   \text{J}.
$$

Nach (23.7) und (23.13) ist die Spannung gleich dem negativen Linienintegral über die elektrische Feldstärke zwischen den Feldpunkten $P _ { 1 }$ und $P _ { 2 }$ :

$$
U = - \int_ {P _ {1}} ^ {P _ {2}} \boldsymbol {E} \cdot \mathrm{d} \boldsymbol {r} = \varphi_ {2} - \varphi_ {1} = \Delta \varphi \quad (\text {Spannung}). \tag {23.14}
$$

Für ein homogenes Feld, in welchem E überall konstant ist, erhält man $\boldsymbol { U } = - \boldsymbol { E } \cdot \boldsymbol { l } ,$ wobei l der Vektor von $P _ { 1 }$ nach $P _ { 2 }$ ist. Sieht man vom Vorzeichen der Spannung ab, so wird

$$
U = E l \cos \alpha = E d \quad \text {bzw.} \quad E = \frac {U}{d} \tag {23.15}
$$

mit l als Entfernung zwischen $P _ { 1 }$ und $P _ { 2 }$ und l cos $\alpha = d$ als Länge ihrer Projektion auf die Feldrichtung.

Alle Punkte gleichen Potenzials, zwischen denen also die Spannung null herrscht, liegen auf geschlossenen Flächen, den **Äquipotenzialflächen**. Sie umschließen die felderzeugenden Ladungen. Bei jeder Verschiebung dr einer Probeladung q auf einer solchen Fläche braucht nach (23.11) wegen $\varphi _ { 2 } = \varphi _ { 1 }$ keine Arbeit verrichtet zu werden, weshalb das skalare Produkt E · dr verschwindet, gleichbedeutend damit, dass die Feldstärke E auf der Verschiebung dr und somit auf der Äquipotenzialfläche $\varphi = \mathrm { c o n s t }$ senkrecht steht (Bild 23.2).

## Die elektrischen Feldlinien verlaufen überall senkrecht zu den Äquipotenzialflächen.

Mathematisch wird dieser Sachverhalt durch die Eigenschaft des Gradienten, stets senkrecht auf den Linien (bzw. Flächen) $\varphi = \mathrm { c o n s t }$ zu stehen, in Gleichung (23.10) ausgedrückt.

## Beispiel 23.2:

Wie groß sind in einem homogenen elektrischen Feld der Feldstärke $E = 10    kN/m$ die Spannungen zwischen dem Punkt A im Bild 23.5b und den übrigen Eckpunkten $B \ldots F$ eines regulären Sechsecks von 2cm Seitenlänge?

Lösung: AB, C F und DE liegen auf Äquipotenzialflächen in jeweils gleichen Abständen: $U _ { A B } =$ 0; $U _ { A C } = U _ { A F }$ und $U _ { A D } = U _ { A E } = 2   U _ { A F }$ . Es genügt, $U _ { A F }$ zu berechnen. Die Projektion des Abstandes AF auf die Feldrichtung hat die Länge $d = 2    cm  \cdot \cos 30^{\circ} = 1.73    cm$ . Nach (23.15) ist $U _ { A F } = E d = 1 7 3   \mathrm { V } .$ □

## 23.5 Elektrische Ladungen auf Leitern. Influenz

Ein Leiter ist ein Stoff, in dem sich elektrische Ladungsträger (Elektronen, Ionen) unter der Wirkung eines elektrischen Feldes frei bewegen können. Bringt man an eine Stelle des Leiters eine Ladungsmenge aus sehr vielen gleichnamigen beweglichen Einzelladungen q, so bewirken die abstoßenden Kräfte F zwischen diesen Ladungsträgern, dass sie sich so weit als möglich voneinander entfernen und an der Oberfläche des Leiters sammeln. Die Ladungsverteilung an der Leiteroberfläche ist durch das Gleichgewicht der elektrostatischen Kräfte $( F = 0 )$ bestimmt. Daraus folgt wegen (23.2) $\boldsymbol { F } = q \boldsymbol { E }$ , dass sich in einem (abgeschlossenen) Leiter kein elektrostatisches Feld aufrechterhalten lässt. Wegen $E = 0$ ist nach (23.10) das Potenzial $\varphi$ überall konstant.

$$
\text {In einem Leiter ist} \begin{array}{l} \text {die Feldstärke} \\ \text {das Potenzial} \end{array} \text {des elektrostatischen Feldes} \begin{array}{l} E = 0 \\ \varphi = \text {const.} \end{array}
$$

Die an der Oberfläche eines geladenen Leiters versammelten Ladungsträger befinden sich erst dann im Gleichgewicht, wenn der Feldstärkevektor außerhalb des Leiters senkrecht zur Oberfläche gerichtet ist. Solange das nicht der Fall ist, existiert eine Kraftkomponente tangential zur Oberfläche, unter deren Wirkung sich die frei beweglichen Ladungen bis zum Verschwinden dieser Komponente verschieben.

## Elektrische Feldlinien, die auf einem Leiter entspringen oder enden, stehen senkrecht auf der Leiteroberfläche.

Daher braucht bei einer Verschiebung einer Ladung entlang der Oberfläche, senkrecht zur Kraft des äußeren elektrischen Feldes, keine Arbeit verrichtet zu werden. Die Leiteroberfläche befindet sich also auf konstantem Potenzial; sie ist eine Äquipotenzialfläche des Außenfeldes (vgl. 23.4).

Da sich im Innern eines massiven leitenden Körpers weder Ladungen noch Feld befinden, ändern sich die elektrischen Verhältnisse nicht, wenn man ihn durch seine leitfähige Körperhülle ersetzt. So ist in einer geladenen Hohlkugel die Feldstärke null und das Potenzial konstant und gleich dem der Kugeloberfläche. Auf diese Weise lassen sich Räume gegen statische elektrische Felder abschirmen, indem man sie mit elektrisch leitenden Wänden umgibt. Meist genügt zur Abschirmung schon ein nicht zu weitmaschiges Drahtnetz (FARADAY-Käfig).

![](images/page_272_image_3.jpg)

Bild 23.6 Influenzversuch: a) Influenz in einer Metallplatte bzw. in zwei aufeinanderliegenden Blechen; b) Ladungstrennung im Feld; c) Messung der influenzierten Ladung

**Influenz.** Bringt man einen ungeladenen Leiter, z. B. eine ebene Metallplatte, in ein äußeres elektrisches Feld, so wird in ihm infolge der elektrostatischen Kräfte, die das Feld auf die Leitungselektronen im Metall ausübt, eine Ladungstrennung derart hervorgerufen, dass die eine Leiteroberfläche eine negative, die gegenüberliegende Oberfläche eine gleich große positive Aufladung erfährt (Bild 23.6a). Diese Erscheinung nennt man Influenz; der Leiter wird dabei **polarisiert**. Verwendet man anstelle einer Metallplatte zwei aufeinander liegende Bleche (Bild 23.6a), die dann aber im Feld getrennt (Bild 23.6b) und so aus dem Feld herausgeführt werden (Bild 23.6c), so erhält das eine Blech eine positive, das andere eine gleich große negative Ladung. Die Feldstärke zwischen den beiden Blechen ist dabei dem Betrage nach gleich der des influenzierenden Feldes. Die Größe der auf einem Blech influenzierten Ladung Q, die man z. B. mit Hilfe eines ballistischen Galvanometers messen kann (vgl. Abschnitt 23.1), hängt davon ab, wie viele Feldlinien N auf der Leiteroberfläche enden: Q ∼ N. Da nach 23.2 die (Flächen-)Dichte der Feldlinien N/A dem Betrag der Feldstärke E proportional ist, N/A ∼ E oder $N \sim E A$ , wobei A die Fläche des Bleches ist, gilt

$$
Q = \varepsilon_ {0} E A \quad \text {bzw.} \quad \mathrm{d} Q = \varepsilon_ {0} E \mathrm{d} A. \tag {23.16}
$$

Dabei ist $\varepsilon _ { 0 }$ ein Proportionalitätsfaktor, die elektrische Feldkonstante oder **Influenzkonstante**. Diese Größe muss experimentell bestimmt werden; man erhält

$$
\varepsilon_ {0} = 8, 8 5 4   1 8 8 \cdot 1 0 ^ {- 1 2} \mathrm{A} \cdot \mathrm{s} / (\mathrm{V} \cdot \mathrm{m}) \quad \text {(Influenzkonstante).} \tag {23.17}
$$

Die Stärke elektrischer Felder kann also außer durch Kraftwirkungen auf Ladungen gemäß Gleichung (23.2) $E = F / q$ auch durch ein Experiment wie in Bild 23.6 gemessen werden; nach (23.16) erhält man aus der im Leiter influenzierten Ladung Q für die Komponente der elektrischen Feldstärke senkrecht zur Leiteroberfläche $E = Q / ( \varepsilon _ { 0 } A )$

## 23.6 Elektrischer Fluss, Flussdichte

Die Gesamtheit der Feldlinien, die ein Flächenstück A des felderfüllten Raumes senkrecht durchsetzen, nennt man (in Analogie zur Strömungsmechanik) den **elektrischen Fluss** Ψ. Dieser kann in einem Influenzversuch (Bild 23.6) gemessen werden: Da jede Feldlinie in einer Ladung entspringt bzw. endet, ist die in einer Leiteroberfläche durch Influenz gebundene elektrische Ladung Q ein Maß für den in diese Fläche eintretenden bzw. aus ihr austretenden elektrischen Fluss; wir setzen daher $\Psi = Q$

Auf diese Weise lässt sich neben der elektrischen Feldstärke E eine weitere Feldgröße einführen, die anschaulich durch die Anzahl der Feldlinien je Flächeneinheit gegeben ist:

$$
D = \frac {\mathrm{d} \Psi}{\mathrm{d} A} = \frac {\mathrm{d} Q}{\mathrm{d} A} \quad (\text {elektrische Flussdichte, Verschiebungsdichte}) \tag {23.18}
$$

$$
\text {Einheit:} \quad [ D ] = 1 \frac {\mathrm{C}}{\mathrm{m} ^ {2}} = 1 \frac {\mathrm{As}}{\mathrm{m} ^ {2}}.
$$

Auf einer Leiteroberfläche stimmt nach oben Gesagtem der Betrag der Verschiebungsdichte D mit der Ladungsbedeckung des Leiters σ überein:

$$
\sigma = \frac {\mathrm{d} Q}{\mathrm{d} A} \quad (\text {Ladungsbedeckung, Flächenladungsdichte}). \tag {23.19}
$$

Die Verschiebungsdichte ist ebenso wie die Feldstärke ein Vektor; sie ist wegen (23.16) und (23.18) dem Betrage nach gleich $D = \varepsilon _ { 0 } E$ , also der Feldstärke proportional, und überdies ihr gleich gerichtet. Es gilt deshalb

$$
\boldsymbol {D} = \varepsilon_ {0} \boldsymbol {E} \quad (\text {Verschiebungsdichte im Vakuum}). \tag {23.20}
$$

![](images/page_273_image_10.jpg)

Bild 23.7 Elektrischer Fluss $\Psi$ durch eine geschlossene Fläche $A ,$ die im Fall a) ein Gebiet mit Quellen (Ladung $Q )$ , im Fall b) ein quellenfreies Gebiet umschließt.

Der elektrische Fluss durch eine beliebig orientierte Fläche A ergibt sich aus (23.18) – analog Bild 15.3 und zugehöriger Gleichung (15.5) – zu

$$
\Psi = \int \boldsymbol {D} \cdot \mathrm{d} \boldsymbol {A} \quad (\text {elektrischer Fluss}). \tag {23.21}
$$

Legt man um eine oder mehrere Ladungen $Q _ { i }$ eine geschlossene, ansonsten aber beliebig geformte Fläche A (Bild 23.7a), so ist der durch sie hindurchgehende elektrische Fluss gleich der Summe der von der Fläche eingeschlossenen Ladungen als Quellen (oder Senken) des elektrischen Feldes:

$$
\Psi = \oint_ {(A)} \boldsymbol {D} \cdot \mathrm{d} \boldsymbol {A} = \sum_ {i} Q _ {i} \quad (\text {GAUSSsches Gesetz der Elektrostatik}). \tag {23.22}
$$

Liegen die Ladungen außerhalb der geschlossenen Fläche (Bild 23.7b), so verschwindet das Oberflächenintegral (23.22), da in diesem Falle in den von der Fläche umhüllten Raum ebenso viele Feldlinien eintreten wie austreten.

## 23.7 Das elektrische Zentralfeld (Punktladung und Punktladungssystem)

Denken wir uns eine Kugel vom Radius r um eine Punktladung Q als Mittelpunkt gelegt, so ist die Dichte der Feldlinien auf der Kugeloberfläche überall gleich groß, d. h., der Betrag der Verschiebungsdichte D ist auf der Kugeloberfläche konstant, und die Feldlinien durchsetzen die Kugelfläche überall senkrecht. Der Fluss durch die Kugelfläche ist dann nach (23.22)

$$
\Psi = \oint \boldsymbol {D} \cdot \mathrm{d} \boldsymbol {A} = \varepsilon_ {0} \oint E \mathrm{d} A = \varepsilon_ {0} E \oint \mathrm{d} A = \varepsilon_ {0} E (4 \pi r ^ {2}) = Q,
$$

woraus für den Betrag der elektrischen Feldstärke im Abstand r von der Punktladung Q folgt:

$$
E = E (r) = \frac {Q}{4 \pi \varepsilon_ {0} r ^ {2}}. \tag {23.23}
$$

Da die elektrischen Feldlinien radialsymmetrisch zu der im Koordinatenursprung angenommenen Ladung verlaufen (vgl. Bild 23.2a), wird der Vektor der elektrischen Feldstärke am Ort r des Feldes durch

$$
\boldsymbol {E} (\boldsymbol {r}) = \frac {Q}{4 \pi \varepsilon_ {0} r ^ {2}} \boldsymbol {e} _ {r} \quad \begin{array}{l} \text {(elektrische Feldstärke} \\ \text {einer Punktladung)} \end{array} \tag {23.24}
$$

beschrieben mit $\pmb { e } _ { r } = \pmb { r } / r$ als Einheitsvektor in radialer Richtung. Der Richtungssinn von E ergibt sich aus dem Vorzeichen von Q. Damit folgt nach (23.9)

$$
\varphi (r) = - \int_ {\infty} ^ {r} \boldsymbol {E} \cdot \mathrm{d} \boldsymbol {r} = \frac {Q}{4 \pi \varepsilon_ {0} r} \quad \begin{array}{l} (\text {elektrostatisches Potenzial} \\ \text {einer Punktladung}). \end{array} \tag {23.25}
$$

Die Äquipotenzialflächen sind konzentrische Kugelflächen mit Q als Mittelpunkt.

Die hier angegebenen Beziehungen für Feldstärke und Potenzial sind auch für eine geladene (Voll-)Kugel vom Radius R gültig, sofern $r \geq R$ ist; denn:

## Eine elektrisch geladene Kugel wirkt für einen außerhalb oder auf ihrer Oberfläche liegenden Punkt so, als sei die gesamte Ladung in ihrem Mittelpunkt vereinigt.

Befinden sich im Raum mehrere Punktladungen $Q _ { 1 } , \ldots , Q _ { n }$ (Punktladungssystem wie z.B. in Bild 23.2b und c), so wird das elektrische Feld über die Berechnung des elektrostatischen Potenzials bestimmt. Dabei gilt das Superpositionsprinzip: Das resultierende Potenzial an einem beliebigen Ort ergibt sich durch Addition der Einzelpotenziale $\varphi _ { i }$ , die von den Ladungen $Q _ { i }$ gemäß Gleichung (23.25) in den Abständen $r _ { i }$ unabhängig voneinander aufgebaut werden:

$$
\varphi = \frac {1}{4 \pi \varepsilon_ {0}} \left(\frac {Q _ {1}}{r _ {1}} + \frac {Q _ {2}}{r _ {2}} + \dots + \frac {Q _ {n}}{r _ {n}}\right) = \frac {1}{4 \pi \varepsilon_ {0}} \sum_ {i = 1} ^ {n} \frac {Q _ {i}}{r _ {i}}. \tag {23.26}
$$

Wenn keine Punktladungen, sondern flächenhaft bzw. räumlich verteilte Ladungen vorliegen, wird die **Flächenladungsdichte** $\sigma = \mathbf { d } Q / \mathbf { d } A$ bzw. die **Raumladungsdichte** $\varrho = \mathbf { d } Q / \mathbf { d } V$ verwendet. An die Stelle der Ladungen $Q _ { i }$ treten $\mathbf { d } Q = \sigma$ dA bzw. $\mathbf { d } Q = \varrho \mathbf { d } V$ , und statt der Summation (23.26) wird über die gesamte geladene Fläche bzw. das gesamte geladene Volumen integriert:

$$
\varphi = \frac {1}{4 \pi \varepsilon_ {0}} \int \frac {\sigma \mathrm{d} A}{r} \quad \text {bzw.} \quad \varphi = \frac {1}{4 \pi \varepsilon_ {0}} \int \frac {\varrho \mathrm{d} V}{r}.
$$

**Kraftwirkungen zwischen Ladungen.** Die Kraft zwischen zwei punktförmigen Ladungen q und Q ist diejenige Kraft, welche die Ladung q im Feld der Ladung Q erfährt, nach Gleichung (23.2) $\boldsymbol { F } = q \boldsymbol { E }$ mit der Feldstärke (23.24) also

$$
\boldsymbol {F} = \frac {1}{4 \pi \varepsilon_ {0}} \frac {q Q}{r ^ {2}} \boldsymbol {e} _ {r}, \quad \text {Betrag} \quad F = \frac {1}{4 \pi \varepsilon_ {0}} \frac {q Q}{r ^ {2}} \quad (\text {COULOMBSches Gesetz}). \tag {23.27}
$$

Bei gleichen Vorzeichen von $q$ und Q sind F und der Einheitsvektor $\pmb { e } _ { r }$ , der von Q nach $q$ zeigt, gleich gerichtet, und wir beobachten Abstoßung; bei ungleichen Vorzeichen sind F und $\boldsymbol { e } _ { r }$ entgegengerichtet, und wir erhalten Anziehung. Dieses Gesetz wurde zuerst von COULOMB (1785) auf Grund von genauen Messungen gefunden:

## Die zwischen zwei Punktladungen (geladenen Kugeln) wirkende Kraft ist dem Produkt beider Ladungen proportional und nimmt mit dem Quadrat ihres Abstandes (Mittelpunktabstandes) ab.

## Beispiele 23.3:

1. Man berechne für das Wasserstoffatom das Verhältnis von elektrostatischer Anziehungskraft und Gravitationskraft zwischen Proton und Elektron, die je eine Elementarladung tragen $( m _ { \mathrm { p } } = 1 . 6 7 3 \cdot 1 0 ^ { - 2 7 }   \mathrm { k g } ;   m _ { \mathrm { e } } = 9 . 1 0 9 \cdot 1 0 ^ { - 3 1 }   \mathrm { k g } ;   e = 1 . 6 0 2 \cdot 1 0 ^ { - 1 9 }   \mathrm { C } )$

Lösung: Mit der COULOMB-Kraft (23.27) $F _ { \mathrm { C } } = e ^ { 2 } / ( 4 \pi \varepsilon _ { 0 } r ^ { 2 } )$ und der Gravitationskraft (22.4) $F _ { \mathrm { G } } =$ $\gamma m _ { \mathrm { p } } m _ { \mathrm { e } } / r ^ { 2 }$ erhält man $F _ { \mathrm { C } } : F _ { \mathrm { G } } = e ^ { 2 } / ( 4 \pi \varepsilon _ { 0 } ) : \gamma m _ { \mathrm { p } } m _ { \mathrm { e } } \approx 2   \cdot   1 0 ^ { 3 9 }$ ! Die elektrostatischen Kräfte sind also ungleich stärker als die Gravitationskräfte, was (trotz vieler formaler Analogien zwischen elektrischem Feld und Gravitationsfeld) auf ihre unterschiedliche Natur hinweist.

2. Welches ist der kleinste Abstand, bis zu dem sich ein beim radioaktiven Zerfall des Poloniums entstehendes α-Teilchen dem Kern eines Goldatoms annähern kann, wenn es sich mit der Energie $E _ { \alpha } = 7   \mathrm { M e V }$ direkt auf ihn zu bewegt? (RUTHERFORD-Streuung, Bild 44.1). Welchen Wert erreicht die Abstoßungskraft im Punkt der größten Annäherung, wo das Teilchen am Kern „reflektiert“ wird? Ladung des α-Teilchens $q   =   2 e$ , Ladung des Au-Kerns $Q = Z e$ mit der Ordnungszahl $Z = 79; \varepsilon_{0} = 8.854 \cdot 10^{-12}    C/(V  \cdot  m )$

Lösung: Beim Anflug des α-Teilchens auf den Au-Kern büßt es seine gesamte kinetische Energie $E _ { \alpha }$ ein, erhält dafür aber zunehmend potenzielle Energie, die im kernnächsten Abstand $r _ { \mathrm { m i n } }$ nach (23.12) und (23.25) gleich $E _ { \mathrm { p } } = q Q / ( 4 \pi \varepsilon _ { 0 } r _ { \mathrm { m i n } } ) = 2 Z e ^ { 2 } / ( 4 \pi \varepsilon _ { 0 } r _ { \mathrm { m i n } } )$ ist. Aus $E _ { \mathtt { P } } = E _ { \alpha }$ folgt mit der Energieeinheit $\mathrm{1eV} = 1.602 \cdot 10^{-19} \mathrm{J}$

$$
r _ {\min} = \frac {Z e ^ {2}}{2 \pi \varepsilon_ {0} E _ {\alpha}} = 3, 2 5 \cdot 1 0 ^ {- 1 4} \mathrm{m} \quad \text {und nach (23.27)} \quad F _ {\max} = \frac {2 Z e ^ {2}}{4 \pi \varepsilon_ {0} r _ {\min} ^ {2}} \approx 3 4 \mathrm{N}.
$$

$r _ { \mathrm { m i n } }$ ist von der Größenordnung des Kernradius.

## Aufgaben

**23.2** Berechne die Kraft, mit der sich zwei kugelförmige Gaswolken anziehen, die sich in 1000m Abstand voneinander befinden und jeweils aus 1mol einfach positiver bzw. negativer Ionen bestehen!
**23.3** Welche Arbeit muss beim Heranführen einer Punktladung $q = 2 \cdot 1 0 ^ { - 8 } \mathrm { C }$ aus dem Unendlichen zu einem Punkt verrichtet werden, der 1cm von der Oberfläche einer Kugel mit dem Radius $R = 1$ cm und der Flächenladungsdichte $\sigma = 1 0 ^ { - 5 } \mathrm { C } / \mathrm { m } ^ { 2 }$ entfernt ist?

## 23.8 Kapazität. Kondensatoren

Bringt man auf eine leitende Kugel eine Ladung $Q ,$ so verteilt sie sich auf der Kugeloberfläche, da infolge der elektrostatischen Abstoßung gleichnamige Ladungsträger so weit wie möglich auseinander streben. Das davon ausgehende D-Feld endet auf benachbarten Leitern, an den Raumwänden, auf der Erdoberfläche oder im Unendlichen und influenziert dort insgesamt die Ladung $- Q$ (Senken). Enden alle Feldlinien im Unendlichen, wo das Potenzial $\varphi ( \infty ) = 0$ herrscht, so liegt die Kugeloberfläche (Radius R) als Sitz der Ladung Q auf der Spannung (Potenzialdifferenz) $U = \varphi ( R ) - \varphi ( \infty ) = \varphi ( R )$ . Nach (23.25) ist daher $U = Q / ( 4 \pi \varepsilon _ { 0 } R ) = Q / C$ mit

$$
C = 4 \pi \varepsilon_ {0} R \quad (\text {Kapazität der frei stehenden Kugel}). \tag {23.28}
$$

Eine solche Proportionalität $Q \sim U$ zwischen Ladung und Spannung gilt für jede Anordnung von isoliert aufgestellten Leitern (Konduktoren). Der Proportionalitätsfaktor $C ,$ die **Kapazität** des Leiters, ist eine lediglich durch seine Geometrie (Abmessungen, Gestalt, Anordnung) bestimmte Größe. Es gilt somit

$$
C = \frac {Q}{U} \quad (\text {Kapazität, allgemein}). \tag {23.29}
$$

Die Kapazität C kennzeichnet das „Fassungsvermögen“ eines Leiters für elektrische Ladungen bei einer bestimmten Spannung. So besitzt auch jedes Elektrometer (vgl. Bild 23.1) eine bestimmte Kapazität, weshalb damit nicht nur Ladungen, sondern wegen $Q \sim U$ auch Spannungen gemessen werden können, wenn es in Volt geeicht wird (elektrostatisches Voltmeter). Aus der Definitionsgleichung (23.29) folgt als

$$
\text {Einheit der Kapazität:} \quad [ C ] = \frac {[ Q ]}{[ U ]} = 1 \frac {C}{V} = 1 \frac {\mathrm{As}}{\mathrm{V}} = 1 \text {Farad (F) .}
$$

## Ein Leiter der Kapazität 1 Farad (F) wird durch die Ladung 1 Coulomb (1 $\mathbf { C } = \mathbf { 1 } \; \mathbf { A } \; \mathbf { s } )$ auf eine Spannung von 1 Volt (V) aufgeladen.

Da 1F in der Praxis eine sehr große Einheit darstellt, werden Kapazitäten von Kondensatoren üblicherweise in Mikrofarad $( 1   \mu \mathrm { F } = 1 0 ^ { - 6 }   \mathrm { F } )$ , Nanofarad $( 1   \mathrm { n F } = 1 0 ^ { - 9 }   \mathrm { F } )$ oder Pikofarad $( 1 { \tt p F } =$ $1 0 ^ { - 1 2 } \mathrm { F ) }$ angegeben.

**Kondensatoren.** Stellen wir einer isoliert aufgestellten Metallplatte eine zweite Platte gleicher Größe im Abstand d gegenüber, die leitend mit der Erde verbunden ist, so entsteht ein Plattenkondensator. Wird die Konduktorplatte aufgeladen, so verlaufen die elektrischen Feldlinien alle zur gegenüberliegenden Kondensatorplatte, da auf dieser eine entgegengesetzt gleiche La dung durch Influenz gebunden wird. Als Ladung des Kondensators bezeichnet man diejenige, die eine Platte trägt.

Zwischen den Kondensatorplatten bildet sich bei kleinem Plattenabstand d (im Verhältnis zur Plattengröße A) ein homogenes elektrisches Feld aus, dessen Feldstärke nach (23.15)

$$
E = \frac {U}{d} = \text {const} \quad \text {(Feldstärke im Plattenkondensator)} \tag {23.30}
$$

ist. Die auf der geerdeten Kondensatorplatte der Fläche A durch das elektrische Feld influenzierte Ladung Q lässt sich nun über die elektrische Verschiebungsdichte (23.18) und (23.20) angeben zu

$$
Q = D A = \varepsilon_ {0} E A = \frac {\varepsilon_ {0} A}{d} U,
$$

woraus mit Gleichung (23.29) folgt

$$
C = \frac {\varepsilon_ {0} A}{d} \quad (\text {Kapazität des leeren Plattenkondensators}). \tag {23.31}
$$

Aus der Beziehung (23.31) geht hervor: Je kleiner der Plattenabstand, umso größer ist die Kapazität des Kondensators. Da sich bei einer Veränderung des Plattenabstandes die Ladung auf den Platten und damit die Feldstärke nicht ändert, nimmt die Spannung zwischen den Platten $U = E d$ bei Vergrößerung ihres Abstandes zu.

Allgemein wird jede Vorrichtung, die zur Speicherung einer elektrischen Ladung dient, als Kondensator bezeichnet, sie ist also nicht an die Plattenform gebunden. Jeder Kondensator besteht aus zwei gegeneinander isoliert in einem bestimmten Abstand angeordneten Leitern, z. B. beim Zylinderkondensator aus zwei konzentrischen Zylinderflächen mit unterschiedlichen Radien (Koaxialkabel, Leidener Flasche). Große Kapazitäten lassen sich nach (23.31) durch große Leiterflächen A erreichen. Dazu werden übereinander liegende Metall- und Isolierpapierfolien zusammen aufgewickelt (Wickelkondensatoren). Eine Erhöhung von C wird auch durch kleinstmögliche Elektrodenabstände d erzielt. Dazu kann die isolierende Oxidschicht genutzt werden, mit der sich Metalle überziehen, wenn sie mit einem Elektrolyten in Berührung kommen (Elektrolytkondensatoren). Schließlich steigt auch die Kapazität, wenn durch eine geeignete Isolierschicht zwischen den Leiterflächen die elektrische Verschiebungsdichte bei gleicher Feldstärke gegenüber dem Vakuum erhöht wird (Keramikkondensatoren); vgl. 24.2.

**Schaltung von Kondensatoren.** Für zwei parallel geschaltete Kondensatoren (Bild 23.8a) ist $U = U _ { 1 } = U _ { 2 }$ , und die Ladungen addieren sich: $Q = Q _ { 1 } + Q _ { 2 } = U C _ { 1 } + U C _ { 2 } = U C$ . Die Gesamtkapazität hat deshalb die Größe $C = C _ { 1 } + C _ { 2 }$ , allgemein

$$
C = \sum_ {i} C _ {i} \quad (\text {Gesamtkapazität} C \text {bei Parallelschaltung}). \tag {23.32}
$$

Bei zwei in Reihe geschalteten Kondensatoren (Bild 23.8b) liegen nur die linke Platte von $C _ { 1 }$ und die rechte Platte von $C _ { 2 }$ an der Spannung U. Die „inneren“ Platten laden sich durch Influenz auf, so dass beide Kondensatoren jeweils die gleiche Ladung tragen: $Q = Q _ { 1 } = Q _ { 2 }$ . Die Teilspannungen addieren sich zu $U = U _ { 1 } + U _ { 2 } = Q / C _ { 1 } + Q / C _ { 2 } = Q / C$ . Die Gesamtkapazität C berechnet sich somit hier nach $1 / C = 1 / C _ { 1 }   +   1 / C _ { 2 }$ , allgemein

$$
\frac {1}{C} = \sum_ {i} \frac {1}{C _ {i}} \quad (\text {Gesamtkapazität} C \text {bei Reihenschaltung}). \tag {23.33}
$$

![](images/page_277_image_12.jpg)

<details>
<summary>chemical</summary>

Simple electrical circuit diagram with two capacitors and a voltage source labeled U
</details>

![](images/page_277_image_13.jpg)

<details>
<summary>text_image</summary>

C₁ C₂
b) U
</details>

Bild 23.8 a) Parallelschaltung, b) Reihenschaltung von zwei Kondensatoren

## Beispiele 23.4:

1. Auf die 1cm voneinander entfernten Platten eines luftleeren Kondensators der Kapazität $C _ { 1 } = 1 0 0   \mathrm { p F }$ wird aus einer Spannungsquelle die Ladung $Q = 2 2  { \mathbf { n } }  { \mathrm { C } }$ aufgebracht. Danach wird der Kondensator wieder von der Spannungsquelle abgeklemmt. a) Welche Spannung $U _ { 1 }$ liegt am Kondensator, und wie groß ist die Feldstärke $E _ { 1 }$ im Kondensatorraum? b) Welche Werte nehmen Kapazität, Spannung und Feldstärke an, wenn der Plattenabstand auf $d _ { 2 } = 2$ cm vergrößert wird? c) Wie verändern sich Spannung, Kapazität, Ladung und Feldstärke, wenn der Kondensator beim Auseinanderziehen der Platten nicht von der Spannungsquelle getrennt, sondern an ihr belassen wird?

Lösung: Nach Gleichung (23.29) folgt $U _ { 1 } = Q / C _ { 1 } = 2 2 0 \mathrm { V }$ und nach Gleichung (23.30) $E _ { 1 } =$ $U_{1}/d_{1}=22\mathrm{kV/m}$ . b) Die Kapazität des leeren Plattenkondensators berechnet sich nach Gleichung (23.31) zu $C = \varepsilon _ { 0 } A / d ,$ also nimmt die Kapazität bei einer Verdopplung des Plattenabstandes auf die Hälfte ab: $C_{2} = 50    pF$ Die Vergrößerung des Plattenabstandes lässt die darauf befindlichen Ladungen unberührt, somit gilt $U_{2}=Q/C_{2}=440V$ , die Feldstärke bleibt ebenso unverändert (wegen der gleichbleibenden Flussdichte $D = Q / A = \varepsilon _ { 0 } E )$ $E _ { 2 } = U _ { 2 } / d _ { 2 } = 2 2 \mathrm { k V } / \mathrm { m } = E _ { 1 }$ . c) Jetzt sorgt die Spannungsquelle dafür, dass die Spannung konstant bleibt, also $U_{3}=U_{1}=220 V$ . Weiterhin gilt: $C _ { 3 } = C _ { 2 } = 5 0   \mathrm { p F }$ , woraus $Q _ { 3 } = C _ { 3 } U _ { 3 } = 1 1   \mathrm { n C }$ folgt; es fließen Ladungen über die Spannungsquelle vom Kondensator ab. Die Feldstärke sinkt wegen der abgeflossenen Ladungen auf $E _ { 3 } = U _ { 3 } / d _ { 3 } = 1 1   \mathrm { k V / m }$

2. Die Flächenladungsdichte eines Plattenkondensators mit der Plattengröße $A = 1   \mathrm { d m } ^ { 2 }$ betrage $\sigma = 5 { , } 3   \mu \mathrm { C / m } ^ { 2 }$ . Ein Elektron erlangt beim Durchlaufen des Weges von einer Platte zur anderen eine Geschwindigkeit von $3 , 2 5 \cdot 1 0 ^ { 7 }   \mathrm { m } / \mathrm { s }$ . Wie groß ist die Kapazität des Kondensators? Man bestimme die Feldstärke im Kondensator und den Plattenabstand. Ruhmasse des Elektrons $m _ { \mathrm { e } } = 9 , 1 1 \cdot 1 0 ^ { - 3 1 }   \mathrm { k g } ;   e = 1 , 6 0 2 \cdot 1 0 ^ { - 1 9 }   \mathrm { C } ;   \varepsilon _ { 0 } = 8 , 8 5 4 \cdot 1 0 ^ { - 1 2 }   \mathrm { C } / ( \mathrm { V } \cdot \mathrm { m } )$

Lösung: Nach (23.19) ist $\sigma = Q / A$ , woraus für die Ladung auf einer Kondensatorplatte folgt $Q = \sigma A = 5 { , } 3 \cdot 1 0 ^ { - 8 } \mathbf { C }$ . Die beim Durchlaufen des Plattenabstandes vom Elektron aufgenommene kinetische Energie $m _ { \mathrm { e } } \upsilon ^ { 2 } / 2$ ist gleich der Arbeit zur Überwindung der Potenzialdifferenz (Spannung) U, also mit $| q | = e$ nach (23.13) gleich $e U ;$ daraus folgt $U = m_{\mathrm{e}} v^{2} / (2e) = 3 \mathrm{kV}. \mathrm{So} \cdot$ mit wird nach (23.29) $C = Q / U = 1 . 8 \cdot 1 0 ^ { - 1 1 } \mathrm { F } = 1 8 \mathrm { p F } .$ . Aus (23.18) und (23.20) folgt $E = D / \varepsilon _ { 0 } =$ $\sigma / \varepsilon_{0} = 600    kN/m$ und mit (23.15) $d = U / E = 5    mm$ □

## Aufgaben

**23.4** Man bestimme die Kapazität $C _ { \mathrm { E } }$ der Erdkugel (Radius 6380km). Um wie viel ändert sich das Potenzial der Erdkugel, wenn man ihr eine Ladung von 1C überträgt?
**23.5** Auf eine Kugel von 8cm Durchmesser werde eine elektrische Ladung von $4 { , } 4 5 { \cdot } 1 0 ^ { - 7 }$ <sub>C</sub> gebracht. Welche Spannung erhält sie dadurch gegen Erde?

## Das elektrische Feld in Isolatoren (Dielektrika)

## 24.1 Elektrische Polarisation der Dielektrika. Piezoelektrizität

Die elektrischen Erscheinungen werden durch die Anwesenheit von Stoffen beeinflusst und unterscheiden sich daher von denen im Vakuum. Die Unterschiede liegen in der Struktur der Stoffe begründet. Alle Stoffe sind aus Atomen bzw. Molekülen aufgebaut, die ihrerseits aus positiv und negativ geladenen Teilchen bestehen. Von besonderer Bedeutung sind dabei die Elektronen, die bei Isolatoren, den sog. **Dielektrika**, im Gegensatz zu Leitern nur innerhalb der Atome oder Moleküle verschiebbar sind. Infolge der Kräfte eines äußeren Feldes, die an den Elektronen und positiven Atomkernen des Moleküls angreifen, findet eine Verschiebung der Elektronenhüllen derart statt, dass die Schwerpunkte der positiven und negativen Ladungen nicht mehr zusammenfallen. Die Moleküle werden im elektrischen Feld zu elektrischen Dipolen. Ihr influenziertes Dipolmoment $\pmb { p }$ ist bei nicht zu starken Feldern der äußeren Feldstärke $E _ { 0 }$ proportional:

$$
\boldsymbol {p} = \alpha \boldsymbol {E} _ {0}. \tag {24.1}
$$

α ist die **Polarisierbarkeit** der Moleküle und hängt nur von deren Art ab. Man nennt diese Erscheinung **Verschiebungspolarisation**, da sie auf einer Ladungsverschiebung beruht. Sie tritt bei allen Stoffen auf.

Viele Stoffe bestehen aus Molekülen, die von Natur aus permanente elektrische Dipole sind. Diese zeigen zusätzlich eine sog. **Orientierungspolarisation**. Sie besteht darin, dass die ohne äußeres Feld völlig regellos orientierten Dipolmoleküle sich unter dem Einfluss eines äußeren Feldes vorzugsweise in Feldrichtung einstellen (vgl. 23.3). Dadurch wird ein resultierendes Dipolmoment in Feldrichtung erzeugt, das (bei nicht zu starken Feldern) ebenfalls der äußeren Feldstärke $E _ { 0 }$ proportional, jedoch wegen der desorientierenden Wirkung der Wärmebewegung zur Temperatur umgekehrt proportional ist: $\pmb { p } \sim E _ { 0 } / T$

Bild 24.1a veranschaulicht die Polarisation eines Dielektrikums im Feld eines Plattenkondensators. Die Dipolachsen bilden Ketten in Feldrichtung, so dass sich im Innern des Stoffes die jeweils einander gegenüberliegenden ungleichnamigen Dipolladungen kompensieren, während an der Oberfläche des Dielektrikums unkompensierte freie Ladungen auftreten. Diese Oberflächenladungen sind auf der Seite, wo das äußere Feld eintritt, negativ, dort wo es austritt, positiv. Dadurch wird im Stoff ein Gegenfeld hervorgerufen, um welches das äußere Feld im Innern des Stoffes geschwächt wird. Befinden sich im Volumen V des Dielektrikums N Moleküle, von denen jedes ein elementares Dipolmoment $\pmb { p }$ besitzt, so ergibt die Dipoldichte die **elektrische Polarisation P** des Dielektrikums:

$$
\boldsymbol {P} = \frac {N}{V} \boldsymbol {p} = n \boldsymbol {p} = n \alpha \boldsymbol {E} _ {0} \tag {24.2}
$$

![](images/page_280_image_2.jpg)

Bild 24.1 Entstehung freier Oberflächenladungen infolge Polarisation der Moleküle a) durch ein elektrisches Feld, b) durch eine mechanische Druckbeanspruchung (piezoelektrischer Effekt)

Die Polarisation P ist, wie auch ihre Einheit zeigt, betragsmäßig gleich der Flächenladungsdichte (23.19) $\sigma = \mathbf { d } Q / \mathbf { d } A$ der freien Oberflächenladungen des Dielektrikums. Polarisation und Oberflächenladungen verschwinden nach Abschalten des äußeren Feldes. Nur in Ausnahmefällen, bei den sog. **Elektreten**, bleibt auch dann eine permanente Polarisation erhalten.

**Piezoelektrizität.** Bestimmte Kristalle, z. B. Quarz $\mathrm { ( S i O _ { 2 } ) }$ , lassen sich auch rein mechanisch durch eine Druck-, Zug- oder Schubspannung, also ohne ein äußeres elektrisches Feld, polarisieren. Dazu wird eine dünne Platte senkrecht zu einer sog. **polaren Achse** des Kristallgitters aus einem größeren Einkristall herausgeschnitten. Komprimiert man z. B. eine Quarzplatte in Richtung dieser polaren Achse (Bild 24.1b), so verschieben sich die positiven (Silicium-) und die negativen (Sauerstoff-)Ionen aus ihren Normallagen im Kristallgitter so, dass ihre Ladungsschwerpunkte nicht mehr zusammenfallen und dadurch Dipole entstehen. Im Innern der Kristalle kompensieren sich die Ladungen dieser Dipole; nur auf der einen Grenzfläche entsteht ein Überschuss an positiver und auf der gegenüberliegenden Seite ein Überschuss an negativer Ladung (longitudinaler piezoelektrischer Effekt). Eine geringere Polarisation zeigt der senkrecht zur polaren Achse auftretende transversale piezoelektrische Effekt. Quarze werden als Sensoren zu Druck-, Kraft- und Beschleunigungsmessungen sowie in der Elektroakustik für Mikrofone, Tonabnehmer u. a. verwendet.

Bringt man eine Quarzplatte durch Aufladen der Grenzflächen in ein elektrisches Feld, so dehnt bzw. kontrahiert sie sich in Richtung der polaren Achse. Dieser reziproke piezoelektrische Effekt wird bei den sog. **Schwingquarzen** zur Frequenzstabilisierung von Oszillatorschwingungen (z. B. bei Uhren, Sendern usw.) oder zur Erzeugung von Ultraschall genutzt.

## 24.2 Permittivität (Dielektrizitätskonstante), elektrische Suszeptibilität

Es soll nun untersucht werden, welche Erscheinungen durch das Einbringen eines Dielektrikums in ein elektrisches Feld auftreten. Wir gehen von folgendem Experiment aus: Füllt man den Raum zwischen den Platten eines geladenen und von der Spannungsquelle wieder abgetrennten Kondensators mit einem Dielektrikum, so sinkt die Spannung U am Kondensator. Wird das Dielektrikum wieder entfernt, so steigt die Spannung wieder auf den ursprünglichen Wert. Da sich die auf den Kondensatorplatten vorhandene Ladung Q durch das Einbringen des Dielektrikums nicht geändert haben kann, muss wegen (23.29) $U = Q / C$ durch Anwesenheit des Dielektrikums die Kapazität C des Kondensators erhöht worden sein. Das Verhältnis der durch das Dielektrikum vergrößerten Kapazität $C$ eines Kondensators zu seiner Vakuum-Kapazität $C _ { 0 }$ definiert den Stoffwert

$$
\varepsilon_ {\mathrm{r}} = \frac {C}{C _ {0}} \quad (\text {Permittivitäts- oder Dielektrizitätszahl}). \tag {24.3}
$$

Da in diesem Experiment die Ladung konstant bleibt, ändert sich auch die Verschiebungsdichte $D = Q / A$ nicht. Es gilt mit $U _ { 0 }$ bzw. U als Spannung am Kondensator ohne bzw. mit Dielektrikum: $Q = C _ { 0 } U _ { 0 } = C U$ , also $U _ { 0 } = ( C / C _ { 0 } )   U = \varepsilon _ { \mathrm { r } } U$ oder $U = U _ { 0 } / \varepsilon _ { \mathrm { r } }$ . Die Spannung am Kondensator fällt also durch das Einbringen des Dielektrikums $( \varepsilon _ { \mathrm { r } } > 1 )$ ab. Wegen (23.30), $U = E d$ mit d als Plattenabstand, gilt dies auch für die elektrische Feldstärke:

$$
\boldsymbol {E} = \frac {1}{\varepsilon_ {\mathrm{r}}} \boldsymbol {E} _ {0} \quad \text {oder} \quad \boldsymbol {E} _ {0} = \varepsilon_ {\mathrm{r}} \boldsymbol {E}. \tag {24.4}
$$

## Bei gleich bleibender Ladungsverteilung ist die Feldstärke im Dielektrikum um den Faktor $\mathbf { 1 } / \varepsilon _ { \mathbf { r } }$ kleiner als die Feldstärke im Vakuum.

Diese Schwächung der Feldstärke im Stoff wird durch das Gegenfeld $E _ { \mathrm { P } }$ der durch Polarisation des Dielektrikums hervorgerufenen freien Oberflächenladungen (Bild 24.1a) bewirkt. Die Feldstärke im Stoff E ergibt sich somit aus der Überlagerung von Vakuum-Feldstärke $E _ { 0 }$ und ihr entgegengerichteter Polarisationsfeldstärke $E _ { \mathrm { P } }$ (Bild 24.2):

$$
\boldsymbol {E} = \frac {\boldsymbol {E} _ {0}}{\varepsilon_ {\mathrm{r}}} = \boldsymbol {E} _ {0} + \boldsymbol {E} _ {\mathrm{P}}. \tag {24.5}
$$

![](images/page_281_image_9.jpg)

Bild 24.2 Polarisation eines Dielektrikums $( \varepsilon _ { \mathrm { r } } = 2 ) { \mathrm { : } }$ a) elektrisches Feld $E _ { 0 }$ ohne $\mathsf { S t o f f } ; \mathsf { b } )$ das infolge Polarisation im Stoff sich ausbildende Feld der Oberflächenladungen $E _ { \mathrm { P } } ; \mathtt { c } )$ resultierendes Feld im Stoff $\boldsymbol{E} = \boldsymbol{E}_{0} + \boldsymbol{E}_{\mathrm{P}} = \boldsymbol{E}_{0} / \varepsilon_{\mathrm{r}}$

Dieser Abfall der Feldstärke tritt nicht ein, wenn man obiges Experiment so abwandelt, dass der Kondensator während des Einbringens des Dielektrikums an der Spannungsquelle angeschlossen bleibt. Auf diese Weise wird die Spannung und damit die Feldstärke im Kondensator konstant gehalten. Da sich durch das Dielektrikum die Kapazität des Kondensators nach (24.3) um den Faktor $\varepsilon _ { \mathrm { r } }$ erhöht, muss zur Konstanthaltung der Spannung wegen $U = Q / C$ auch die Ladung auf den Kondensatorplatten durch Nachfließen von der Spannungsquelle von $Q$ auf $\varepsilon _ { \mathrm { r } } Q$ zunehmen. Damit wächst auch die Verschiebungsdichte $D = Q / A$ auf das $\varepsilon _ { \mathrm { { \bf { r } } ^ { \prime } } }$ -fache dieses Wertes, und es gilt jetzt anstelle von Gleichung (23.20)

$$
\boldsymbol {D} = \varepsilon_ {\mathrm{r}} \varepsilon_ {0} \boldsymbol {E} = \varepsilon \boldsymbol {E} \quad (\text {Verschiebungsdichte im Dielektrikum}) \tag {24.6}
$$

mit der **Permittivität** oder **Dielektrizitätskonstante** $\varepsilon = \varepsilon _ { \mathrm { r } } \varepsilon _ { 0 }$

Die Differenz der durch das Dielektrikum vergrößerten Verschiebungsdichte (24.6) zur Verschiebungsdichte bei derselben Feldstärke im Vakuum $( \varepsilon _ { \mathrm { r } } = 1 )$ ist somit

$$
\boldsymbol {P} = \boldsymbol {D} - \varepsilon_ {0} \boldsymbol {E} = (\varepsilon_ {\mathrm{r}} - 1) \varepsilon_ {0} \boldsymbol {E} = \chi_ {\mathrm{e}} \varepsilon_ {0} \boldsymbol {E} \quad \text {(elektrische Polarisation).} \tag {24.7}
$$

Der Proportionalitätsfaktor $\chi _ { \mathrm { e } } = \varepsilon _ { \mathrm { r } }   -   1$ heißt **elektrische Suszeptibilität** des Stoffes. P ist diejenige Verschiebungsdichte, die zur Kompensation der durch das äußere Feld im Dielektrikum erzeugten freien Oberflächenladungen erforderlich ist (vgl. 24.1).

Aus Gleichung (24.5) erhalten wir für die Feldstärke $E _ { \mathrm { P } }$ des Gegenfeldes, erzeugt durch die freien Oberflächenladungen auf dem Dielektrikum:

$$
\boldsymbol {E} _ {\mathrm{P}} = \boldsymbol {E} - \boldsymbol {E} _ {0} = (1 - \varepsilon_ {\mathrm{r}}) \boldsymbol {E} = - \chi_ {\mathrm{e}} \boldsymbol {E}. \tag {24.8}
$$

Wie man sieht, gilt mit (24.7) $\boldsymbol { P } = - \varepsilon _ { 0 } \boldsymbol { E } _ { \mathrm { P } } , \mathrm { d . h . } , \boldsymbol { E } _ { \mathrm { P } }$ ist die zur Polarisation P gehörige Feldstärke; man nennt sie **Elektrisierung**.

Für Stoffe ist $\varepsilon _ { \mathrm { r } } > 1$ und damit $\chi _ { \mathrm { e } } = \varepsilon _ { \mathrm { r } } - 1 > 0 ;$ im Vakuum ist $\varepsilon _ { \mathrm { r } } = 1$ und $\chi _ { \mathrm { e } } = 0$ . Die $\varepsilon _ { \mathrm { r } } \mathrm { - W e r t e }$ der Gase sind wegen der geringen Moleküldichte nur sehr wenig größer als 1 und daher die Suszeptibilitäten sehr klein (einige $1 0 ^ { - 3 } )$ . Deshalb gelten die in Abschnitt 23 für das Vakuum abgeleiteten Gesetzmäßigkeiten in sehr guter Näherung auch für Luft. Bei festen Isolierstoffen und vielen Flüssigkeiten liegt $\varepsilon _ { \mathrm { r } }$ meist in der Größenordnung von $2 \ldots 1 0 ,$ , für Stoffe mit permanenten Dipolmolekülen jedoch vielfach erheblich höher (z. B. bei Wasser mit $\varepsilon _ { \mathrm { { r } } } = 8 1 )$

Bei Stoffen, deren Moleküle eine unsymmetrische Anordnung der inneren Ladungen und damit ein permanentes Dipolmoment aufweisen, hat die elektrische Suszeptibilität $\chi _ { \mathrm { e } }$ zwei Anteile, die den beiden Arten von Polarisation, Verschiebungs- und Orientierungspolarisation (vgl. 24.1), entsprechen. Der nicht temperaturabhängige Anteil, welcher durch die Verschiebungspolarisation hervorgerufen wird und allen Stoffen eigen ist, heißt **dielektrische** Suszeptibilität; der durch die Orientierungspolarisation verursachte temperaturabhängige Anteil heißt **paraelektrische** Suszeptibilität (analog zu „diamagnetisch“ und „paramagnetisch“, vgl. 29.1).

## 24.3 Verhalten von D und E an der Grenzfläche zweier Medien

Zwei verschiedene Stoffe mit den Permittivitäten $\varepsilon _ { 1 }$ und $\varepsilon _ { 2 }$ (z. B. Vakuum mit $\varepsilon _ { 1 } = \varepsilon _ { 0 }$ und Stoff mit $\varepsilon _ { 2 } > \varepsilon _ { 0 } )$ sollen eine gemeinsame Grenzfläche haben. Tritt ein elektrisches Feld vom Stoff 1 in den Stoff 2 über, so muss das Verhältnis von Verschiebungsdichte zu Feldstärke $D / E =$ ε zwangsläufig einen Sprung erleiden. Welche der beiden Feldgrößen D und E sich an der Grenzfläche wie stark ändert, hängt von der Einfallsrichtung der Feldlinien ab.

Stellen wir z. B. zwischen die Platten eines geladenen Kondensators parallel zu diesen eine dielektrische Platte einheitlicher Dicke, die den Kondensatorraum nicht vollständig ausfüllt, so haben D und E bezogen auf eine Grenzfläche des Dielektrikums nur Normalkomponenten $( D ^ { \mathrm { n } }$ und $E ^ { \mathrm { n } } )$ . Der elektrische Fluss $\Psi$ durch ein Grenzflächenstück A wird im gesamten Kondensator nur durch die Ladungsbelegung $Q$ auf den Kondensatorplatten bestimmt und ist demzufolge vor und hinter der Grenzfläche gleich, nach (23.18) $\Psi = D _ { 1 } ^ { \mathfrak { n } } A = D _ { 2 } ^ { \mathfrak { n } } A ,$ d. h., es ist $D _ { 1 } ^ { \mathrm { n } } = D _ { 2 } ^ { \mathrm { n } }$ . Die Normalkomponente von D hat also innerhalb des ganzen Kondensators den gleichen Wert. Aber auch bei schrägem Durchgang des Feldes durch die Grenzfläche gilt

$$
D _ {1} ^ {\mathrm{n}} = D _ {2} ^ {\mathrm{n}}, \quad \text {d.h.} \quad \varepsilon_ {1} E _ {1} ^ {\mathrm{n}} = \varepsilon_ {2} E _ {2} ^ {\mathrm{n}}. \tag {24.9}
$$

## Die Normalkomponente der Verschiebungsdichte tritt stetig durch eine Grenzfläche zwischen verschiedenen Stoffen.

Im Gegensatz dazu hat, wie auch aus Bild 24.2 hervorgeht, die Normalkomponente der elektrischen Feldstärke $E ^ { \mathrm { n } }$ in den freien Oberflächenladungen des polarisierten Dielektrikums zusätzliche Quellen und Senken, in denen Feldlinien beginnen oder enden, und sie erleidet daher beim Übergang vom einen Medium in das andere nach (24.9) einen Sprung: $E _ { 2 } ^ { \mathbf { n } } = ( \varepsilon _ { 1 } / \varepsilon _ { 2 } )   E _ { 1 } ^ { \mathbf { n } }$

Stellt man die dielektrische Platte im Kondensator $\mathbf { s o } ,$ dass das elektrische Feld parallel zur Grenzfläche verläuft, so haben jetzt D und E bezogen auf diese nur Tangentialkomponenten $( D ^ { \mathrm { t } }$ und $E ^ { \mathrm { t } } )$ . Die Spannung U zwischen zwei im Abstand d auf der Grenzfläche gelegenen Punkten $P _ { 1 }$ und $P _ { 2 }$ muss unabhängig davon sein, ob die Distanz d im Medium 1 oder im Medium 2 durchlaufen wird, d. h., es muss nach (23.15) gelten $U = E _ { 1 } ^ { \mathsf { t } } d = E _ { 2 } ^ { \mathsf { t } } d ,$ also $E _ { 1 } ^ { \mathrm { t } } = E _ { 2 } ^ { \mathrm { t } }$ . Aber auch bei schrägem Durchtritt des Feldes durch die Grenzfläche gilt

$$
E _ {1} ^ {\mathrm{t}} = E _ {2} ^ {\mathrm{t}}, \quad \text {d.h.} \quad \frac {D _ {1} ^ {\mathrm{t}}}{\varepsilon_ {1}} = \frac {D _ {2} ^ {\mathrm{t}}}{\varepsilon_ {2}}. \tag {24.10}
$$

## Die Tangentialkomponente der Feldstärke tritt stetig durch eine Grenzfläche zwischen verschiedenen Stoffen.

Die Tangentialkomponente der Verschiebungsdichte D erleidet daher einen Sprung. Aus diesen Gesetzmäßigkeiten geht hervor, dass die E- und D-Linien beim Übertritt in ein Medium mit größerer Permittivität ε eine Brechung vom Grenzflächenlot weg erfahren.

## Beispiele 24.1:

1. Ein Plattenkondensator (Plattengröße $A = 5   \mathrm { c m } ^ { 2 }$ , Plattenabstand d = 1mm) ist mit Glimmer $( \varepsilon _ { \mathrm { r } } = 7 )$ ausgefüllt. Er wird auf eine Spannung von $U = 5 0 0 \mathrm { V }$ aufgeladen. Wie groß sind a) die Feldstärke E und b) die Verschiebungsdichte D im Kondensatorraum, c) die Ladung Q auf einer Platte, d) die Polarisation P des Glimmers und e) die infolge der Polarisation auf dem Glimmer entstandenen freien Oberflächenladungen $Q _ { \mathrm { P } } ?$

Lösung: Es ist a) nach (23.15) $E = U / d = 500    eV/m ;  b$ nach (24.6) mit $\varepsilon _ { 0 } = 8 , 8 5 4 \cdot 1 0 ^ { - 1 2 }   \mathrm { C } / ( \mathrm { V m } ) ;$ $D = 3 1   \mu \mathrm { C } / \mathrm { m } ^ { 2 } ; \mathrm { c } )$ nach (23.18) $Q = DA = 15 , 5 \mathrm{nC} ;$ d) nach (24.7) $P = 2 6 , 6 \mu \mathrm { C } / \mathrm { m } ^ { 2 } ; \mathrm { e } ) P = Q _ { \mathrm { P } } / A ,$ d. h. $Q_{\mathrm{P}} = PA = 13,3\mathrm{n}C = Q - Q_{0}$ , wobei $Q_{0}=D_{0}A=\varepsilon_{0}EA=2,2\mathrm{nC}$ die Plattenladung des leeren Kondensators ist.

2. Zwischen die Platten eines leeren Kondensators (Plattenabstand $d = 8   \mathrm { m m }$ wird eine Glasplatte $( \varepsilon _ { \mathrm { r } } = 7 { , } 5 )$ der Dicke $x = d / 2$ eingeführt. a) In welchem Verhältnis wird dadurch die Kapazität des Kondensators vergrößert? b) Wie groß ist der Spannungsabfall im Luftraum $( \varepsilon _ { \mathrm { r L } } \approx 1 )$ und in der Glasplatte bei einer Aufladung der Kondensatorplatten auf 2500V?

Lösung: a) Nach (24.9) ist die Normalkomponente der Verschiebungsdichte D im Glas- und Luftraum gleich: $\varepsilon _ { \mathrm { r } } E _ { \mathrm { G } } = \varepsilon _ { \mathrm { r L } } E _ { 0 } \approx E _ { 0 }$ , d. h. $E _ { \mathrm { G } } \approx E _ { 0 } / \varepsilon _ { \mathrm { r } }$ . Die Spannung zwischen den Kondensatorplatten ist die Summe aus den Spannungsabfällen in Luft und Glas, nach (23.15) also

$$
U = E _ {0} (d - x) + E _ {\mathrm{G}} x = E _ {0} (d - x) + \frac {E _ {0}}{\varepsilon_ {\mathrm{r}}} x = E _ {0} \left(d - x \frac {\varepsilon_ {\mathrm{r}} - 1}{\varepsilon_ {\mathrm{r}}}\right).
$$

Ohne Glasplatte $( x = 0 )$ ist $U _ { 0 } = E _ { 0 } d .$ . Wegen $C / C _ { 0 } = U _ { 0 } / U$ wird somit die Kapazität durch die Platte im Verhältnis d $: [ d - x ( \varepsilon _ { \mathrm { r } } - 1 ) / \varepsilon _ { \mathrm { r } } ] = 1 , 7 6$ vergrößert. Bei vollständiger Ausfüllung mit dem Dielektrikum $( x = d )$ wird dieser Faktor gleich $\varepsilon _ { \mathrm { r } } , \mathbf { b } )$ Aus obiger Beziehung erhält man mit $U = 2 5 0 0 \mathrm { V }$ durch Umstellung zunächst $E _ { 0 } = U / [ d - x ( \varepsilon _ { \mathrm { r } } - 1 ) / \varepsilon _ { \mathrm { r } } ] = 5 5 1$ ,5V/mm und hieraus die Spannungsabfälle $U _ { \mathrm { L } } = E _ { 0 }   ( d - x ) = 2 2 0 6 \mathrm { V }$ in der Luftschicht und $U _ { \mathrm { G } } = ( E _ { 0 } / \varepsilon _ { \mathrm { r } } )   x = 2 9 4 \mathrm { V }$ in der Glasplatte. Man erkennt, dass bei fast vollständiger Ausfüllung mit dem Dielektrikum im verbleibenden Luftspalt sehr hohe Spannungen bzw. Feldstärken auftreten können.

3. Im Unterschied zu Beispiel 24.1/2 sei jetzt der Raum zwischen den Kondensatorplatten über deren gesamten Abstand $d ,$ jedoch nur zu einem Teil X der Plattenfläche A mit dem Dielektrikum aufgefüllt. In welchem Verhältnis vergrößert sich die Kapazität des Kondensators für den Fall, dass die Hälfte des Kondensatorraumes mit Glas gefüllt ist? Werte für d und $\varepsilon _ { \mathrm { r } }$ wie im obigen Beispiel 24.1/2.

Lösung: In diesem Fall verlaufen die Feldlinien parallel zur Grenzfläche des Dielektrikums, weshalb nach (24.10) die Tangentialkomponente der elektrischen Feldstärke im Glas- und Luftraum gleich ist, nämlich überall $E = U / d ,$ , während die Verschiebungsdichten in Glas und Luft die Werte $D _ { \mathrm { G } } = \varepsilon _ { \mathrm { r } } \varepsilon _ { 0 } E = \varepsilon _ { \mathrm { r } } \varepsilon _ { 0 } U / d$ und $D _ { \mathrm { L } } = \varepsilon _ { 0 } E = \varepsilon _ { 0 } U / d$ annehmen. Die auf den Kondensatorplatten gespeicherte Ladung Q teilt sich auf die beiden an Glas und Luft angrenzenden Plattenflächenanteile X und $( A   -   X )$ wie folgt auf:

$$
Q = D _ {\mathrm{G}} X + D _ {\mathrm{L}} (A - X) = \frac {\varepsilon_ {0} U}{d} [ A + X (\varepsilon_ {\mathrm{r}} - 1) ] = C U.
$$

Hieraus folgt mit (23.31) $C _ { 0 } = \varepsilon _ { 0 } A / d$ (Kapazität des leeren Kondensators):

$$
C = \frac {A + X (\varepsilon_ {\mathrm{r}} - 1)}{A} C _ {0} = 4, 2 5 C _ {0}.
$$

## Aufgaben

**24.1** Zeige mit Hilfe der Beziehung (23.31) unter Beachtung von Gleichung (24.3), dass sich die Kapazität C eines nach obigem Beispiel 24.1/2 mit einem Dielektrikum teilweise gefüllten Kondensators als Gesamtkapazität einer Reihenschaltung (23.33) aus gefülltem und leerem Kondensator berechnen lässt!
**24.2** Zeige analog wie in Aufgabe 24.1, dass sich die Kapazität eines nach obigem Beispiel 24.1/3 mit einem Dielektrikum teilweise gefüllten Kondensators als Gesamtkapazität einer Parallelschaltung (23.32) aus gefülltem und leerem Kondensator berechnen lässt!

## 24.4 Energieinhalt des elektrischen Feldes

Einfache Experimente zeigen, dass jeder geladene Kondensator einen Energiespeicher darstellt. Um die Aufladung $q$ eines Plattenkondensators um den Betrag dq zu erhöhen, muss die Ladungsmenge dq von der einen Kondensatorplatte gegen die Feldkräfte zur anderen verschoben werden. Bei der am Kondensator anliegenden Spannung $U = q / C$ ist die dafür aufzuwendende Verschiebungsarbeit nach (23.13)

$$
\mathrm{d} W = U \mathrm{d} q = \frac {q}{C} \mathrm{d} q.
$$

Denken wir uns die Aufladung des Kondensators von Anfang an portionsweise jeweils durch sehr kleine Ladungsmengen dq vorgenommen, so ist für das Aufbringen der Gesamtladung Q die Arbeit

$$
W = \frac {1}{C} \int_ {0} ^ {Q} q \mathrm{d} q = \frac {1}{2 C} Q ^ {2} = \frac {1}{2} C U ^ {2} = \frac {1}{2} Q U \tag {24.11}
$$

erforderlich; sie stellt die im Kondensator **gespeicherte Energie** dar.

Um zu verdeutlichen, dass es sich um Energie im elektrischen Feld handelt, setzen wir in Gleichung (24.11) für das homogene Feld des Plattenkondensators nach (23.18) $Q = D A$ und nach (23.15) $U = E d$ . Mit $A d = V$ als Volumen des felderfüllten Raumes zwischen den Kondensatorplatten folgt

$$
W _ {\mathrm{e}} = \frac {1}{2} D E V \quad (\text {elektrische Feldenergie}). \tag {24.12}
$$

Teilt man $W _ { \mathbf { e } }$ durch das felderfüllte Volumen $V ,$ so erhält man

$$
w _ {\mathrm{e}} = \frac {W _ {\mathrm{e}}}{V} = \frac {1}{2} D E = \frac {1}{2} \varepsilon E ^ {2} = \frac {1}{2} \varepsilon_ {\mathrm{r}} \varepsilon_ {0} E ^ {2} \quad \begin{array}{l} (\text {Energiedichte des} \\ \text {elektrischen Feldes}). \end{array} \tag {24.13}
$$

Diese Gleichung, welche der Einfachheit halber nur für ein homogenes Feld hergeleitet wurde, hat keinen Bezug mehr zum Kondensator; sie besitzt in dieser Form allgemeine Gültigkeit für beliebige, auch zeitlich veränderliche elektrische Felder sowohl im Vakuum als auch im stofferfüllten Raum. Da sie auch für den leeren (stofffreien) Raum gilt, muss das raumerfüllende Feld selbst Träger der Energie sein (FARADAY, MAXWELL).

## Beispiele 24.2:

1. Ein Fotoblitzkondensator von $1 0 0 0   \mu \mathrm { F }$ wird auf 220V aufgeladen. Wie groß ist die im Feld gespeicherte Energie? Welche Leistung wird beim Entladen über die Fotoblitzlampe bei 1ms Blitzdauer umgesetzt?

Lösung: Nach (24.11) ist die Energie $W _ { \mathrm { e } } = C U ^ { 2 } / 2 \approx 2 4 \mathsf { W }   \cdot   \mathsf { s } ,$ die Leistung $P = W / t = 24  kW$ Die in Kondensatoren speicherbare Energie ist gering $( 2 4 W \cdot s \approx 7 \cdot 1 0 ^ { - 6 } \mathrm { k W h } ! )$ . Bei schneller Entladung können jedoch, wie man sieht, große Leistungen auftreten.

2. Man berechne auf Grund der Modellannahme, dass für ein kugelförmig gedachtes Elektron die seiner Masse $m _ { \mathbf { e } }$ zukommende relativistische Ruhenergie (7.20) $E _ { 0 } = m _ { \mathrm { e } } c ^ { 2 }$ dem Energieinhalt seines elektrischen Feldes genau entspricht, den Radius des Elektrons.

Lösung: Mit (24.11) und (23.28) ist $W _ { \mathrm { e } } = Q ^ { 2 } / ( 2 C ) = e ^ { 2 } / ( 8 \pi \varepsilon _ { 0 } r _ { \mathrm { e } } ) = m _ { \mathrm { e } } c ^ { 2 }$ , woraus sich mit den entsprechenden Konstanten $r _ { \mathrm { e } } = 1 { , } 4 { \cdot } 1 0 ^ { - 1 5 }$ m errechnet. Man beachte, dass $r _ { \mathrm { e } }$ mit den Radien von Proton und Neutron nach (47.2) für die Massenzahl $A = 1$ übereinstimmt. Nimmt man weiter an, dass sich die Ruhenergie auf Feldenergie und Kohäsionsenergie (welche die auseinander strebenden Ladungsteile zusammenhält) gemäß $2 W _ { \mathrm { e } } = m _ { \mathrm { e } } c ^ { 2 }$ aufteilt, folgt

$$
r _ {\mathrm{e}} = 2, 8 \cdot 1 0 ^ {- 1 5}   \mathrm{m} \qquad (\text {klassischer Elektronenradius}).
$$

□

## 25.1 Das stationäre elektrische Feld in einem Leiter

Im Unterschied zum elektrostatischen Feld eines isoliert aufgestellten, elektrisch geladenen Leiters, welches nur außerhalb des Leiters existiert, die Feldstärke E im Leiterinnern also stets gleich null ist (vgl. 23.5), kann ein **stationäres elektrisches Feld** im Innern eines Leiters, z. B. in einem Metalldraht, aufrechterhalten werden, wenn bei ständiger Energiezufuhr von außen Ladungen an der einen Seite zu- und an der anderen wieder abgeführt werden. Dazu muss der Leiter mit seinen beiden Enden an eine konstante Spannungsquelle angeschlossen werden. Das elektrische Feld im Leiter greift an den Leitungselektronen mit der Kraft $\pmb { F } = - e \pmb { E }$ an und bewirkt eine gerichtete Bewegung der Ladungsträger, d. h., im geschlossenen Kreis fließt über den Leiter ein **stationärer elektrischer Strom (Gleichstrom)**. Dieser ist verknüpft mit einem ständigen Transport elektrischer Ladungen, einer dauernden Wärmeentwicklung und einem magnetischen Feld um den Leiter herum (vgl. 28.3). Durch diese wesentlichen Eigenschaften, zu denen noch mechanische, chemische und Lichtwirkungen hinzukommen, ist der elektrische Strom beobachtbar und messbar.

Ein **elektrischer Stromkreis**, der aus Spannungsquelle und Leiter besteht, ist mit einem Flüssigkeitskreislauf vergleichbar, der sich aus einer Zirkulationspumpe und einem geschlossenen Leitungssystem zusammensetzt. Der in Flussrichtung monoton fallende Flüssigkeitsdruck ist ein mechanisches Analogon zum elektrischen Potenzial; Druckdifferenzen zwischen zwei Punkten entsprechen Potenzialdifferenzen oder elektrischen Spannungen. Man spricht von Druckabfall und Spannungsabfall. Die von der Zirkulationspumpe erzeugte Druckdifferenz zwischen Ansaug- und Ausstoßöffnung entspricht der Spannung zwischen den Polklemmen der Spannungsquelle, die geförderte Flüssigkeitsmenge (in kg/s) der **elektrischen Stromstärke** (in C/s).

## 25.2 Stromstärke, Spannung, Widerstand. Ohmsches Gesetz

Die Stärke eines elektrischen Stromes wird durch die transportierte Ladungsmenge je Zeiteinheit ausgedrückt:

$$
I = \frac {\mathrm{d} Q}{\mathrm{d} t} \quad (\text {elektrische Stromstärke}). \tag {25.1}
$$

Die bei der Stromstärke I in der Zeitspanne $t = t _ { 2 } - t _ { 1 }$ transportierte Ladung beträgt somit

$$
Q = \int_ {t _ {1}} ^ {t _ {2}} I \mathrm{d} t \quad (\text {Elektrizitätsmenge}). \tag {25.2}
$$

Zeitlich konstante Ströme heißen **Gleichströme**; für sie vereinfachen sich (25.1) und (25.2) zu

$$
I = \frac {Q}{t}; \quad Q = I t. \tag {25.3}
$$

Bezogen auf die Fläche, durch die der Strom hindurchtritt, ergibt sich die Stromdichte $j ,$ ein Vektor vom Betrag

$$
j = \frac {\mathrm{d} I}{\mathrm{d} A} \quad \text {bzw.} \quad j = \frac {I}{A} \quad (\text {Stromdichte}); \tag {25.4}
$$

Analog zur Massenstromstärke (15.5) ist dann die Stromstärke durch eine beliebige Fläche, deren Flächennormale mit der Richtung von $j$ den Winkel α einschließt (Bild 15.3), gegeben durch das Skalarprodukt aus Stromdichtevektor und Flächenelementvektor

$$
I = \int \boldsymbol {j} \cdot \mathrm{d} \boldsymbol {A} \quad \text {bzw.} \quad I = \boldsymbol {j} \cdot \boldsymbol {A} = j A \cos \alpha . \tag {25.5}
$$

Die konventionelle Stromrichtung ist so festgelegt, dass der Strom vom Pluspol der Spannungsquelle über den äußeren Stromkreis zum Minuspol der Spannungsquelle fließt (Bild 25.1). So stimmt diese Stromrichtung mit der Bewegungsrichtung positiver Ladungsträger durch die Kraftwirkung eines elektrischen Feldes überein, während sich negative Ladungsträ- ger, wie z. B. Elektronen, entgegengesetzt zur so definierten Stromrichtung bewegen.

![](images/page_287_image_9.jpg)

<details>
<summary>text_image</summary>

- +
U
A
I
R
V
</details>

Bild 25.1 Einfacher elektrischer Stromkreis mit Spannungsquelle U, Widerstand R, Strommesser $( A )$ und Spannungsmesser (V). Strom fließt vom Pluspol (langer Strich) zum Minuspol (kurzer Strich) der Spannungsquelle.

Die Ladungsträger verlieren im Leiter laufend potenzielle Energie, die irreversibel in Wärmeenergie umgewandelt wird. Dieser Energieverlust rührt daher, dass die Ladungsträger bei ihrer Bewegung durch den Leiter infolge Wechselwirkung mit den Gitteratomen eine Art Reibungskraft erfahren, die sich darin äußert, dass jeder Leiter dem elektrischen Strom I einen „bremsenden“ **Widerstand** R entgegensetzt. Um gegen diesen Widerstand einen konstanten Strom (Gleichstrom) aufrechtzuerhalten, muss von der Spannungsquelle konstanter Spannung U (Gleichspannung) her eine ständige Energiezufuhr erfolgen.

Wird die Spannung U n-fach erhöht oder der Widerstand R n-fach geteilt, steigt der Strom auf das n-fache. Dieser Zusammenhang zwischen Strom, Spannung und Widerstand findet seinen Ausdruck als

## OHMsches Gesetz:

**Die Stromstärke, die durch einen konstanten elektrischen Widerstand fließt, ist der an ihm anliegenden Spannung proportional.**

$$
I = \frac {U}{R} \quad \text {mit} \quad R = \text {const} \quad (\text {OHmsches Gesetz}). \tag {25.6}
$$