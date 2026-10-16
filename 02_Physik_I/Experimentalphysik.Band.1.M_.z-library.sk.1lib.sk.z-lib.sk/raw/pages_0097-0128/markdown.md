Die kinetische Energie lässt sich in zwei Teile zerlegen. Wir führen ein zweites Koordinatensystem mit seinem Ursprung $O ^ { \prime }$ im Massenmittelpunkt mit dem Ortsvektor $\vec { r } _ { S }$ ein und bezeichnen alle darauf bezogenen Ortsvektoren mit ${ \vec { r } } ^ { \prime } ,$ Es gilt offenbar

$$
\vec {r} _ {i} = \vec {r} _ {S} + \vec {r} _ {i} ^ {\prime} \tag {I-2.72}
$$

und damit

$$
\left(\frac {d \vec {r} _ {i}}{d t}\right) ^ {2} = \left(\frac {d \vec {r} _ {S}}{d t}\right) ^ {2} + 2 \frac {d \vec {r} _ {S}}{d t} \frac {d \vec {r} _ {i} ^ {\prime}}{d t} + \left(\frac {d \vec {r} _ {i} ^ {\prime}}{d t}\right) ^ {2}. \tag {I-2.73}
$$

In den Ausdruck für die kinetische Energie eingesetzt folgt somit

$$
\sum_ {i} \frac {1}{2} m _ {i} \left(\frac {d \vec {r} _ {i}}{d t}\right) ^ {2} = \frac {1}{2} \left(\frac {d \vec {r} _ {S}}{d t}\right) ^ {2} \sum_ {i} m _ {i} + \frac {d \vec {r} _ {S}}{d t} \sum_ {i} m _ {i} \frac {d \vec {r} _ {i} ^ {\prime}}{d t} + \frac {1}{2} \sum_ {i} m _ {i} \left(\frac {d \vec {r} _ {i} ^ {\prime}}{d t}\right) ^ {2}. \tag {I-2.74}
$$

Aus $\vec { r } _ { i } = \vec { r } _ { S } + \vec { r } _ { i } ^ { \prime }$ folgt durch Multiplikation mit $\frac { m _ { i } } { M }$ und Summation über alle Teilchen

$$
\underbrace {\frac {1}{M} \sum_ {\vec {r} _ {S}} m _ {i} \vec {r} _ {i}} = \underbrace {\frac {\vec {r} _ {S}}{M} \sum_ {\vec {r} _ {S}} m _ {i}} + \frac {1}{M} \sum_ {i} m _ {i} \vec {r} _ {i} \tag {I-2.75}
$$

und daher

$$
\begin{array}{l} \sum_ {i} m _ {i} \vec {r} _ {i} ^ {\prime} = 0 \\ \Rightarrow \quad \sum m _ {i} \frac {d \vec {r} _ {i}}{d t} = 0 \tag {I-2.76} \\ \end{array}
$$

und der zweite Summand in Gl. (I-2.74) verschwindet. Es bleibt

$$
\sum_ {i} \frac {1}{2} m _ {i} \left(\frac {d r _ {i}}{d t}\right) ^ {2} = \underbrace {\frac {1}{2} M \left(\frac {d \bar {r} _ {S}}{d t}\right) ^ {2}} _ {E _ {\text {kin}} \text {der Gesamtmasse im Schwerpunkt}} + \underbrace {\frac {1}{2} \sum_ {i} m _ {i} \left(\frac {d \bar {r} _ {i} ^ {\prime}}{d t}\right) ^ {2}} _ {E _ {\text {kin}} \text {der Bewegung relativ zum Schwerpunkt}}. \tag {I-2.77}
$$

1 Die kinetische Energie des Teilchensystems ist die Summe aus der Translationsenergie der Gesamtmasse im Schwerpunkt und der Bewegungsenergie des Systems relativ zum Schwerpunkt.

Wir nehmen jetzt an, dass die inneren Kräfte konservativ sind, sich also eine potenzielle Energie (und damit auch ein Potenzial) definieren lässt. Die potenzielle Energie $U _ { j i }$ der zwischen zwei Teilchen j und i wirkenden Kraft ist eine Funktion der Entfernung, das heißt der Koordinaten der beiden MP. Die auf das Teilchen i wirkende Kraft ergibt sich, wenn wir uns das Teilchen j fest denken und das Teilchen i im skalaren Feld der potenziellen Energie $U _ { j i }$ verschieben:

$$
\vec {F} _ {j i} = - \operatorname{grad} _ {i} U _ {j i} \quad \text {und ebenso} \quad \vec {F} _ {i j} = - \vec {F} _ {j i} = - \operatorname{grad} _ {j} U _ {j i}. \tag {I-2.78}
$$

Bei einer kleinen Verschiebung der Teilchen j und i werden die Arbeiten $\vec { F } _ { j i } \cdot d \vec { r } _ { i } + \vec { F } _ { i j } \cdot d \vec { r } _ { j } = \vec { F } _ { j i } ( d r _ { i } - d \vec { r } _ { j } ) = \vec { F } _ { j i } \cdot d \vec { r } _ { j i } = - d U _ { j i }$ verrichtet. $U _ { j i }$ hängt von den 6 Koordinaten beider Teilchen ab, das totale Differential $d U _ { j i }$ ergibt daher die negative Summe der Arbeiten $\vec { F } _ { j i } \cdot d \vec { r } _ { j i }$ . Damit können wir für die inneren Kräfte mit der inneren potenziellen Energie $U _ { j i }$ schreiben, wenn wir beachten, dass wegen $U _ { j i } = U _ { i j }$ (die potenzielle Energie hängt nur vom Abstand $r _ { j i } = r _ { i j }$ eines Teilchens ab) in der Doppelsumme jedes dU doppelt gezählt wird

$$
\sum_ {i \neq j} \sum_ {j \neq i} \vec {F} _ {j i} d \vec {r} _ {j i} = - \frac {1}{2} \sum_ {i \neq j} \sum_ {j \neq i} d U _ {j i}. \tag {I-2.79}
$$

Lassen sich auch die äußeren Kräfte von einer potenziellen Energie ableiten, so wird der Energiesatz der Mechanik zu (siehe auch Abschnitt 2.2.4, Gl. I-2.40)

$$
E _ {\mathrm{kin}} + \sum_ {i} U _ {i} + \frac {1}{2} \sum_ {i \neq j} \sum_ {j \neq i} U _ {j i} = E _ {\mathrm{kin}} ^ {0} + \sum_ {i} U _ {i} ^ {0} + \frac {1}{2} \sum_ {i \neq j} \sum_ {j \neq i} U _ {j i} ^ {0} = \text {const.} \tag {I-2.80}
$$

Die Summe aus der kinetischen, der äußeren und der inneren potenziellen Energie eines Teilchensystems ist konstant, wenn sowohl die äußeren als auch die zwischen den Teilchen wirkenden inneren Kräfte konservativ sind.

## Zusammenfassung

1. Das Modell des Massenpunktes (Teilchen mit Masse, aber ohne Volumen und Struktur) bewährt sich bei vielen einfachen Problemen der Kinematik und Dynamik.
2. Die allgemeine Bewegung eines Teilchens erfolgt auf einer allgemeinen Kurve im Raum. Die Beschleunigung, die das Teilchen erfährt, kann in einen zur Bahn tangentialen und einen dazu normalen, zum Krümmungsmittelpunkt weisenden Anteil zerlegt werden:

$$
\vec {a} = \frac {d \vec {v}}{d t} = \frac {d v}{d t} \vec {e} _ {t} + v \frac {d \vec {e} _ {t}}{d t} = \frac {d v}{d t} \vec {e} _ {t} + \frac {v ^ {2}}{\rho} \vec {e} _ {n} = \vec {a} _ {t} + \vec {a} _ {n}
$$

Dabei ist $\rho = \frac { 1 } { \sqrt { \left( \frac { d ^ { 2 } \bar { r } } { { d s } ^ { 2 } } \right) ^ { 2 } } }$ der augenblickliche Krümmungsradius der Teilchen-

bahn.

3. Die Bewegung des Teilchens auf einer Kreisbahn ist <u>immer</u> beschleunigt. Auch wenn keine tangentiale Beschleunigung erfolgt, <u>muss</u> eine Zentripetalbeschleunigung vorhanden sein, die zum Zentrum der Kreisbahn gerichtet ist und das Teilchen auf der Bahn hält.
4. Die Newtonsche Bewegungsgleichung definiert die Kraft als Ursache der Bewegungsänderung; quantitativ gilt mit $\vec { p } = m _ { t } \vec { \upsilon }$ als Bewegungsgröße bzw. Impuls $( m _ { t }$ … träge Masse):

$$
\vec {F} = \frac {d \vec {p}}{d t} = \dot {\vec {p}} = m _ {t} \cdot \dot {\vec {v}} = m _ {t} \cdot \vec {a}
$$

5. In einem abgeschlossenen System treten Kräfte immer paarweise und entgegengesetzt gerichtet auf (actio = reactio)!

6. Genaue Messungen haben die Gültigkeit der Äquivalenz von träger und schwerer Masse bis auf eine relative Abweichung von ${ 1 0 } ^ { - 1 2 }$ ergeben:

$$
m _ {s} = m _ {t} = m.
$$

Ein homogenes Gravitationsfeld ist daher völlig äquivalent zu einem gleichförmig beschleunigten Bezugssystem (Einsteinsches Äquivalenzprinzip).

7. Für ein Teilchen ist sein Bahndrehimpuls und das Drehmoment in Bezug auf ein- und denselben Koordinatenursprung folgendermaßen definiert:

Bahndrehimpuls:

Drehmoment:

und es gilt

8. Die Arbeit ist das Wegintegral der Kraft, sie ist für einen freien MP gleich der Änderung der kinetischen Energie des Teilchens:

$$
W = \int_ {P _ {1}} ^ {P _ {2}} \vec {F} d \vec {r} = \frac {1}{2} m (\nu_ {2} ^ {2} - \nu_ {1} ^ {2}) = \Delta E _ {\mathrm{kin}}
$$

9. Für konservative Kraftfelder gilt:

$$
\oint \vec {F} d \vec {r} = 0 \quad \Leftrightarrow \quad \mathrm{rot} \vec {F} = 0
$$

In diesem Fall der Wegunabhängigkeit der Arbeit zwischen zwei Punkten kann jedem Raumpunkt eine potenzielle Energie als negativer Wert jener Arbeit zugeschrieben werden, die notwendig ist, um das Teilchen von einem gewählten Nullpunkt aus zum Raumpunkt zu verschieben. Das vektorielle Kraftfeld kann daher durch das skalare Feld der potenziellen Energie beschrieben werden. Aus rot $( \operatorname { g r a d } u ) = { \vec { \nabla } } \times { \vec { \nabla } } u \equiv 0$ (Vektoranalysis) folgt, dass alle Gradientenfelder

konservativ sind und aus der Definition der potenziellen Energie $V = - \int \limits _ { P _ { 0 } } ^ { P } \vec { F } d \vec { r }$ ergibt sich daher

$$
\vec {F} = - \mathrm{grad} V = - \vec {\nabla} V.
$$

10. In einem abgeschlossenen System konservativer Kräfte bleibt die Summe aus kinetischer und potenzieller Energie (die Gesamtenergie) erhalten.
11. In Inertialsystemen gilt der Trägheitssatz:

für $\vec { F } = 0 \Rightarrow \vec { p } = \mathrm { c o n s t . }$ Zu einem Inertialsystem gleichförmig bewegte Bezugssysteme sind auch Inertialsysteme. Dies gilt nicht für beschleunigte Bezugssysteme, in denen Trägheitskräfte $( = { \mathrm { S c h e i n k r i g f t e } } )$ auftreten, die nur von der Beschleunigung des Bezugssystems herrühren und nicht durch eine fundamentale WW verursacht sind.

12. In einem beschleunigten Bezugssystem sind im allgemeinen Fall folgende Kräfte wirksam:

$$
\begin{array}{l} \vec {F} ^ {\prime} = m \cdot \vec {a} ^ {\prime} = \vec {F} _ {\text {physikalisch}} + \vec {F} _ {\text {Trägheit}} = \\ = \bar {F} _ {\text {physikalisch}} + \bar {F} _ {\text {transversal}} + \bar {F} _ {\text {Coriolis}} + \bar {F} _ {\text {zentrifugal}} + \bar {F} _ {\text {linear}} \\ \end{array}
$$

Dabei treten neben der ’physikalisch’ wirkenden Kraft noch vier Scheinkräfte auf:

die Transversalkraft

$$
\vec {F} _ {\text {transversal}} = - m \left(\dot {\vec {\omega}} \times \vec {r} ^ {\prime}\right),
$$

die das Teilchen transversal zum momentanen Ortsvektor $\vec { r } ^ { \prime }$ beschleunigt,

die Corioliskraft

$$
\vec {F} _ {\text {Coriolis}} = - 2 m (\vec {\omega} \times \vec {v} ^ {\prime}),
$$

die in der Drehebene, also senkrecht zu $\vec { \omega } ,$ , aber normal auf die Geschwindigkeit $\nu ^ { \prime }$ des Teilchens in $\Sigma ^ { \prime }$ wirkt,

die Zentrifugalkraft

$$
\vec {F} _ {\text {zentrifugal}} = - \left(\vec {\omega} \times (\vec {\omega} \times \vec {r} ^ {\prime})\right),
$$

die vom Drehzentrum radial nach außen wirkt, und

die Linearkraft

$$
\vec {F} _ {\text {linear}} = - m \cdot \vec {A} _ {\text {linear}},
$$

wenn das sich drehende System $\Sigma ^ { \prime }$ zusätzlich noch linear beschleunigt ist.

13. Teilchensysteme:

Massenmittelpunkt:

$$
\vec {r} _ {S} = \frac {1}{M} \sum_ {i} m _ {i} \vec {r} _ {i},
$$

Bewegung des Massenmittelpunkts:

$$
\sum_ {i} \vec {F} _ {i} = M \frac {d ^ {2} \vec {r} _ {S}}{d t ^ {2}},
$$

Erhaltung des linearen Gesamtimpulses eines abgeschlossenen Teilchensystems:

Aus

$$
\sum_ {i} \vec {F} _ {i} = 0 \quad \Rightarrow \quad \sum_ {i} m _ {i} \vec {v} _ {i} = M \vec {v} _ {S} = M \frac {d \vec {r} _ {S}}{d t} = \text {const.},
$$

Gesamtdrehimpuls:

Drehimpulssatz:

Erhaltung des Gesamtdrehimpulses eines abgeschlossenen Teilchensystems:

Aus

Erhaltung der Gesamtenergie eines abgeschlossenen Teilchensystems:

$$
E _ {\mathrm{kin}} + \sum_ {i} U _ {i} + \frac {1}{2} \sum_ {i \neq j} \sum_ {j \neq i} U _ {j i} = E _ {\mathrm{kin}} ^ {0} + \sum_ {i} U _ {i} ^ {0} + \frac {1}{2} \sum_ {i \neq j} \sum_ {j \neq i} U _ {j i} ^ {0} = \text {const.}
$$

Dabei sind $U _ { i }$ die potenzielle Energie des i-ten Teilchens aufgrund der äußeren Kräfte und $U _ { j i }$ die innere potenzielle Wechselwirkungsenergie der Teilchen i und j.

## Übungen:

Eine Autokolonne fährt mit einer Geschwindigkeit von 100 km/h (80 km/h, 130 km/h) auf einer Autobahn. Welchen Abstand müssen die Fahrzeuge einhalten, damit das jeweils hintere Fahrzeug nicht auf das vordere auffährt, wenn dieses plötzlich auf ein festes Hindernis stößt? Notwendige Daten: Im Mittel beträgt die maximale Bremsverzögerung 8 ms , während die Reaktionszeit im Mittel 1,4 s beträgt.

2. Eine Rakete startet aus der Ruhe vertikal nach oben. In der ersten Beschleunigungsphase von $t _ { 1 }   = 6 0 \; \mathrm { s }$ erfährt sie eine konstante Beschleunigung von $a_{1}=40\  ms ^{-2}$ Unmittelbar anschließend folgt die zweite Beschleunigungsphase einer Dauer von $t _ { 2 } = 2 0 ~ \mathrm { s }$ mit $a_{2}=90\;{\rm{ms}}^{-2}$ Anschließend fliegt sie mit konstanter Geschwindigkeit weiter.

Welche Höhe und Geschwindigkeit erreicht die Rakete am Ende der ersten und der zweiten Beschleunigungsphase? Nach welchem Gesetz wächst anschließend die Höhe der Rakete? Skizziere Beschleunigungs-, Geschwin digkeits- und Ort-Zeit-Diagramme.

3. Eine in sträflichem Leichtsinn rechtwinkelig und horizontal aus einem fahrenden Zug geworfene Bierflasche fällt auf eine 4 m unter dem Abwurfpunkt liegende Wiese und schlägt 20 m (in Fahrtrichtung gemessen) vom Abwurfpunkt und 8 m vom Bahnkörper entfernt auf. Mit welcher Geschwindigkeit

a) fährt der Zug?
b) wird die Flasche abgeworfen?
c) trifft die Flasche auf den Erdboden?

4. a) Wie groß ist die Reichweite einer Kanone (Luftreibung vernachlässigt), die eine Granate mit der Mündungsgeschwindigkeit υ unter einem Visierwinkel α (Winkel zwischen Sehlinie und Visierlinie) abfeuert?

b) Bei welchem Winkel ist die Reichweite am größten?

c) Wie groß ist der Visierwinkel einer Kanone, die eine Granate mit einer Mündungsgeschwindigkeit von $4 0 0 \; \mathrm { m / s }$ auf ein Ziel auf demselben Niveau in 5000 m Entfernung abfeuert?

5. Die Pedale eines Fahrrades werden mit einer Drehzahl von $2    { \boldsymbol { s } } ^ { - 1 }$ getreten.

a) Welche Winkelgeschwindigkeit ergibt sich für die Hinterachse, wenn das Kettenrad und der Zahnkranz 44 bzw. 20 Zähne besitzen?
b) Wie groß sind bei einem Raddurchmesser von 0,7 m die momentane Geschwindigkeit der Hinterachse und des jeweils höchsten Punktes des Hinterrades?
c) Wie viele km legt der Radfahrer in der Stunde zurück?

6. Ein Supertanker mit 400 000 t Wasserverdrängung fährt mit 15 kn Geschwindigkeit auf Südkurs auf der geographischen Breite $3 0 ^ { \circ }$

a) Wie groß ist die auf das Schiff wirkende Corioliskraft?
(1 kn = 1 Knoten = 1 Seemeile pro Stunde. 1 Seemeile entspricht einer Bogenminute am Äquator oder 1,853 km)
b) Gäbe es keine Reibung, wie lange müsste eine genauso große Kraft wirken, um den anfänglich ruhenden Tanker auf 15 kn zu beschleunigen?

7. Ein oben offener, leerer Eisenbahnwaggon der Masse $m _ { 0 }   =   1 5 \mathrm { ~ t ~ }$ bewege sich reibungsfrei mit $v_{0} = 2    ms ^{-1}$ Während der Bewegung fällt aus einem (ruhenden) Greifbagger senkrecht von oben Sand mit der Masse $m _ { 1 }   =   1$ t in den Wagen.

a) Wie groß sind die Geschwindigkeit des beladenen Wagens und die kine tische Energie des Wagens vor und nach der Beladung?
b) Anschließend wird der Wagen nach unten durch eine Klappe entleert. Wie groß sind danach Geschwindigkeit und kinetische Energie des Wagens?

Hinweis:

Der Energiesatz gilt bei der Beladung nicht (inelastischer Stoß), wohl aber bei der Entladung!

Der Impulssatz gilt immer und reicht zur Berechnung der Geschwindigkeiten und kinetischen Energien aus.

## Anhang 1 Gravitation und Planetenbewegung

## A1.1 Das Gravitationsgesetz

Zur Zeit Newtons waren die Keplerschen Gesetze der Planetenbewegung (siehe Abschnitt 2.2.2) als empirische Tatsache bekannt. Man wusste, dass die Beschleunigung eines Planeten als Massenpunkt auf seiner elliptischen Umlaufbahn um die (als ruhend angenommene) Sonne entgegen der Richtung des Ortsvektors des umlaufenden Planeten im Bezugssystem der Sonne erfolgte und umgekehrt proportional zum Quadrat des Betrags des Ortsvektors, also dem Abstand Sonne–Planet, war:

$$
\vec {a} = - \frac {k}{r ^ {2}} \vec {e} _ {r}, \tag {I-2.81}
$$

wobei $r = \left| { \vec { r } } \right|$ der Betrag des Ortsvektors $\bar { r }$ des umlaufenden Planeten im Bezugssystem der Sonne, k die Proportionalitätskonstante und $\vec { e } _ { r }$ der Einheitsvektor in Richtung des Ortsvektors ist. Newton erkannte, dass dies mit seiner Kraftdefinition $\vec { F } = m \cdot \vec { a }$ als Folge einer Anziehungskraft $\vec { \bar { F } } _ { 1 2 }$ auf den Planeten (Masse $m _ { 1 } )$ durch die Sonne (Masse $m _ { 2 } )$ geschrieben werden konnte $( r _ { 1 2 }$ Abstand Sonne–Planet, $\vec { e } _ { 1 2 }$ Einheitsvektor in Richtung Sonne–Planet)

$$
\vec {F} _ {1 2} = - \frac {k \cdot m _ {1}}{r _ {1 2} ^ {2}} \vec {e} _ {1 2} \quad \text {Kraft auf den „punktförmigen“} ^ {3 3} \text {Planeten} m _ {1}. \tag {I-2.82}
$$

Entsprechend dem 3. Newtonschen Axiom $( a c t i o = r e a c t i o )$ wirkt aber auch die gleich große, entgegengesetzt gerichtete Kraft vom Planeten auf die Sonne

$$
\vec {F} _ {2 1} = - \vec {F} _ {1 2} = + \frac {k ^ {\prime} \cdot m _ {2}}{r _ {1 2} ^ {2}} \vec {e} _ {1 2} \quad \text {Kraft auf die „punktförmige“ Sonne} m _ {2}. \tag {I-2.83}
$$

Damit folgt

$$
\vec {F} _ {1 2} + \vec {F} _ {2 1} = \left(k ^ {\prime} \cdot m _ {1} - k \cdot m _ {2}\right) \frac {\vec {e} _ {1 2}}{r _ {1 2} ^ {2}} = 0,
$$

das heißt

$$
k ^ {\prime} \cdot m _ {1} = k \cdot m _ {2}.
$$

Diese Gleichung kann durch

$$
k = \gamma m _ {2} \quad \text {und} \quad k ^ {\prime} = \gamma m _ {1}
$$

erfüllt werden, wobei jetzt $\gamma$ eine universelle Konstante ist, die nicht von den einander anziehenden Massen abhängt; es ist die Gravitationskonstante. Damit ergibt sich

$$
\bar {F} _ {1 2} = - \bar {F} _ {2 1} = - \gamma \frac {m _ {1} \cdot m _ {2}}{r _ {1 2} ^ {2}} \vec {e} _ {1 2} \quad \begin{array}{l l} & \text {Newtonsches Gravitationsgesetz} \\ & (= \text {Massenanziehungsgesetz}, \\ & \text {Newton's law of gravitation}). \end{array} \tag {I-2.84}
$$

Die Bestimmung der Gravitationskonstante ist aus zwei Gründen nicht einfach:

1. ist die Stärke der Gravitationswechselwirkung sehr klein (sie ist ja mit einer Kopplungskonstanten von ca. ${ 1 0 } ^ { - 4 1 }$ die schwächste der vier fundamentalen Wechselwirkungen, vgl. Kapitel „Einleitung“, Abschnitt 1.1);

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">33 „punktförmig“ bedeutet: der Abstand der beiden Körper ist viel größer als ihre Ausdehnung.</span></small>

2. kann die Wechselwirkung mit störenden Massen nicht abgeschirmt werden. Die Gravitationskonstante wurde zum ersten Mal (indirekt) im 1798 von Henry Cavendish (britischer Naturwissenschaftler, 1731–1810, Cavendish-Experiment: siehe Anhang A1.4) bestimmt. Ihr heute anerkannter Wert ist

$$
\gamma = (6, 6 7 4 3 0 \pm 0, 0 0 0 1 5) \cdot 1 0 ^ {- 1 1} \mathrm{m} ^ {3} \mathrm{kg} ^ {- 1} \mathrm{s} ^ {- 2} \quad \begin{array}{l} \text {Gravitationskonstante} \\ (\text {gravitational constant}). ^ {3 4} \end{array}
$$

Newtons entscheidende Verallgemeinerung war nun anzunehmen, dass dieses Kraftgesetz nicht nur für die Planetenbewegung, sondern für zwei beliebige Massen gelte und auch für den $\scriptstyle { \pmb { \mathscr { v } } } ^ { \mathrm { { I } } }$ freien Fall“ auf der Erdoberfläche verantwortlich sei. Aus einem Vergleich der Erdbeschleunigung an der Erdoberfläche und der Beschleunigung des Mondes infolge der Erdanziehung konnte er die Mondbeschleunigung berechnen und einer Bestimmung aus der Mondumlaufzeit gegenüberstellen. Die Übereinstimmung bestätigte die Übertragung des Gravitationsgesetzes auf beliebige Massen.

**Beispiel:** Berechnung der Beschleunigung $\left| a _ { M } \right|$ des Mondes auf seiner Umlaufbahn.

Die Erde (Masse $m _ { E }$ Erdradius R) erteilt einem auf ihrer Oberfläche befindlichen Massenpunkt (MP mit Masse m′) die Beschleunigung (aus $m ^ { \prime } \cdot \left| a _ { E } \right| = \gamma   \frac { m ^ { \prime } m _ { E } } { R ^ { 2 } } ) ^ { 3 5 }$

$$
\left| a _ {E} \right| = \frac {\gamma m _ {E}}{R ^ {2}} = g,
$$

g … Erdbeschleunigung.

Andererseits gilt für die Beschleunigung des Mondes (Masse $m _ { M } )$ auf seiner Bahn infolge der Erdanziehung mit einer Entfernung Erde–Mond von etwa 60 R und daher $( m _ { M } \cdot | a _ { M } | = \gamma   { \frac { m _ { M }   m _ { E } } { 6 0 ^ { 2 } R ^ { 2 } } } )$

$$
\left| a _ {M} \right| = \frac {\gamma m _ {E}}{6 0 ^ {2} R ^ {2}}.
$$

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">34 Wert nach „Committee on Data for Science and Technology (CODATA)“ 2018.</span></small>

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">35 Eine radialsymmetrische Massenverteilung wirkt für einen Punkt außerhalb, wie ein Massen punkt mit der im Zentrum vereinigt gedachten Gesamtmasse. Siehe dazu das analoge Problem der elektrischen Feldstärke im Außenraum einer geladenen Kugel, Band III, Kapitel „Elektrostatik“, Abschnitt 1.3.</span></small>

Aus beiden Gleichung erhält man

$$
\frac {\left| a _ {M} \right|}{\left| a _ {E} \right|} = \frac {\left| a _ {M} \right|}{g} = \frac {1}{6 0 ^ {2}},
$$

also $\left| a _ { M } \right| = \frac { g } { { 6 0 } ^ { 2 } }$ und mit $g = 9 , 8 1   \mathrm { m s } ^ { - 2 }$ ergibt sich

$$
\left| a _ {M} \right| \cong 2, 7 \cdot 1 0 ^ {- 3} \mathrm{ms} ^ {- 2}.
$$

Die erforderliche Beschleunigung des Mondes lässt sich kinematisch aus der Mondumlaufzeit bestimmen. Dazu nehmen wir in guter Näherung an, dass der Mond auf einer Kreisbahn mit dem Radius $r = 6 0   R$ mit konstanter Winkelgeschwindigkeit $\omega = \left| { \vec { \omega } } \right|$ umläuft. Dann gilt für die Zentripetalbeschleunigung des Mondes nach Gl. (I-2.15), da seine Bahnbeschleunigung (Tangentialbeschleunigung) bei konstanter Winkelgeschwindigkeit ja gleich Null ist

$$
\left| a _ {n} \right| = r \omega^ {2} = 6 0 R \omega^ {2}.
$$

Für den Zusammenhang von Winkelgeschwindigkeit und Umlaufszeit gilt

$$
\omega = \frac {2 \pi}{T}
$$

und mit $T \equiv 2 7 { , } 3$ Tage (siderische $\mathrm{Umlauffziit})=27,3\cdot 24\cdot 3600\ \mathrm{s}=2,36\cdot 10^{6}\ \mathrm{s}$ und $R = 6 , 3 7 \cdot { 1 0 } ^ { 6 }$ m erhält man so für $\left| a _ { M } \right|$ in Übereinstimmung mit dem oben aus dem Gravitationsgesetz bestimmten Wert

$$
\left| a _ {M} \right| = 6 0. 6, 3 7 \cdot 1 0 ^ {6} \cdot \left(\frac {2 \pi}{2 , 3 6 \cdot 1 0 ^ {6}}\right) ^ {2} \cong 2, 7 \cdot 1 0 ^ {- 3} \mathrm{ms} ^ {- 2}.
$$

Die Anwendung des Gravitationsgesetzes auf beliebige Massen ist daher gerechtfertigt.

Während in der geschichtlichen Entwicklung zunächst die exakten astronomischen Beobachtungen Tycho de Brahes (Tycho Brahe, genannt Tycho de Brahe, 1546–1601) standen, die von Kepler empirisch zu den drei Gesetzen der Planetenbewe gung zusammengefasst wurden (1609 erstes und zweites Gesetz, 1619 drittes Gesetz) und später (1686) zu Newtons (universellem) Gravitationsgesetz als tieferer Ursache führten, kann man die Keplerschen Gesetze aus der Gültigkeit des Gravitationsgesetzes ableiten, man spricht dann vom Keplerproblem.

## A1.2 Das Keplerproblem<sup>36</sup>

Wir betrachten die Bewegung eines Planeten (Masse m) im Kraftfeld der als ruhend angenommenen Sonne (Masse M), wobei wir den Ursprung des Koordinatensystems in den Sonnenmittelpunkt legen.<sup>37</sup>

Wir erinnern uns zunächst, dass für die konservative Gravitationskraft gelten muss (Abschnitt 2.2.3, Gl. I-2.36)

$$
\vec {F} _ {G} = - \gamma \frac {M \cdot m}{r ^ {2}} \frac {\vec {r}}{r} = - m \cdot \mathrm{grad} V _ {G} = - m \cdot \vec {\nabla} V _ {G},
$$

wobei der Ortsvektor r⇀des Planeten von der Sonne weg gemessen wird.

Das aus dem Gravitationsgesetz folgende Gravitationspotenzial ist daher für $V _ { G } ( \infty ) = 0$

$$
V _ {G} = \frac {E _ {\mathrm{pot}} ^ {G}}{m} = - \int_ {\infty} ^ {r} \frac {\vec {F} _ {G}}{m} d \vec {r} = \gamma M \int_ {\infty} ^ {r} \frac {d r}{r ^ {2}} = - \gamma M \left(\frac {1}{r}\right) \Bigg | _ {\infty} ^ {r} = - \gamma \frac {M}{r} \quad \text {Gravitations-}\tag {I-2.85}
$$

Außerdem ist die Gravitationskraft eine Zentralkraft und es muss daher außer der Erhaltung der Gesamtenergie des Planeten. $\cdot ^ { 3 8 }$ auch der Drehimpuls $\vec { L } = \vec { r } \times \vec { p }$ erhalten bleiben $1 ^ { 3 9 }$ Wir legen die z-Achse in Richtung von $\vec { L }$ und transformieren auf Polarkoordinaten r und $\varphi$ in der Ebene $\perp \vec { L }$ mit $x = r$ ⋅cos $\varphi$ und $y = r$ ⋅sin $\varphi$

Der Ortsvektor zum Planeten ist $\vec { r } = r \cdot \vec { e } _ { r }$ und daher seine Geschwindigkeit

$$
\dot {\vec {r}} = \dot {r} \cdot \vec {e} _ {r} + r \cdot \frac {d \vec {e} _ {r}}{d t} = \dot {r} \cdot \vec {e} _ {r} + r \cdot \dot {\varphi} \cdot \vec {e} _ {\varphi}, ^ {4 0} \tag {I-2.86}
$$

wenn ${ \vec { e } } _ { \varphi }$ der Einheitsvektor der Drehung um den Winkel $\varphi$ ist (er weist in die Richtung senkrecht zu $\vec { r } )$ . Damit ergibt sich für den Impuls $\vec { p } = m \dot { \vec { r } }$

$$
\vec {p} = m \cdot \dot {r} \cdot \vec {e} _ {r} + m \cdot r \cdot \dot {\varphi} \cdot \vec {e} _ {\varphi} \tag {I-2.87}
$$

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">36 Sieht man die Sonne nicht als ruhend an, so muss man statt einer das Problem beschreibenden Bewegungsgleichung zwei ansetzen – das Zweikörperproblem.</span></small>

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">37 Ganz korrekt wäre es, die Bewegung von Sonne und Planet um den gemeinsamen Schwerpunkt zu betrachten. Bei dem Massenverhältnis Sonne : Erde wie 3,33⋅ 10<sup>5</sup>: 1 kann die Sonne in sehr guter Näherung als ruhend angenommen werden.</span></small>

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">38 V<sub>G</sub> ist ja ein konservatives Potenzial.</span></small>

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">39 Also gilt stets: r⇀⊥ L⇀und p⇀⊥ L⇀⇒ die Bewegung erfolgt in einer Ebene senkrecht zu L⇀.</span></small>

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">40 Aus e⇀r2= 1 folgt e⇀r ⋅ e⇀̇r = 0 ⇒ e⇀̇r ⊥ e⇀r ⇒ e⇀̇r ∝ e⇀φ ; mit |de⇀r | = dφ folgt e⇀̇r = de⇀r de⇀r ⋅e⇀φ = dφ e⇀φ dt dt dt</span></small>

und damit für den Drehimpuls mit $\vec { e } _ { r } \times \vec { e } _ { r } = 0$ und $\vec { e } _ { r } \times \vec { e } _ { \varphi } = \vec { e } _ { z }$

$$
\vec {L} = \vec {r} \times \vec {p} = r \vec {e} _ {r} \times m r \dot {\varphi} \vec {e} _ {\varphi} = m r ^ {2} \dot {\varphi} \vec {e} _ {z} = \text {const.} \tag {I-2.88}
$$

wegen $\frac { d \vec { L } } { d t } = \vec { D } = \vec { r } \times \vec { F } _ { G } = \vec { r } \times \vec { e } _ { r } \vec { F } _ { G } = 0 .$ (Zentralkraft).

Daraus erhalten wir mit $\left| { \vec { L } } \right| = L$

$$
\dot {\varphi} = \frac {L}{m r ^ {2}}. \tag {I-2.89}
$$

Für die kinetische Energie erhalten wir in Polarkoordinaten

$$
E _ {\mathrm{kin}} = \frac {\bar {p} ^ {2}}{2 m} = \frac {m \dot {r} ^ {2}}{2} + \frac {m r ^ {2} \varphi^ {2}}{2} = \frac {m \dot {r} ^ {2}}{2} + \frac {L ^ {2}}{2 m r ^ {2}} = \frac {m v ^ {2}}{2} \tag {I-2.90}
$$

und damit für die Gesamtenergie, die jetzt nur mehr von r abhängt

$$
E = \frac {m v ^ {2}}{2} - \gamma \frac {M m}{r} = \overbrace {\frac {m \dot {r} ^ {2}}{2} + \underbrace {\frac {L ^ {2}}{2 m r ^ {2}}} _ {V _ {\mathrm{eff}}} - \gamma \frac {M m}{r}} ^ {E _ {\mathrm{kin}}} = \overbrace {\frac {m \dot {r} ^ {2}}{2}} ^ {E _ {\mathrm{kin,rad}}} + V _ {\mathrm{eff}} (r) = \text {const.} \tag {I-2.91}
$$

mit der effektiven potenziellen Energie („effektives Potenzial“)

$$
V _ {\mathrm{eff}} (r) = \frac {L ^ {2}}{2 m r ^ {2}} + m V _ {G} (r) = \frac {L ^ {2}}{2 m r ^ {2}} - \gamma \frac {M m}{r}. ^ {4 1} \tag {I-2.92}
$$

Die graphische Darstellung (Abb. I-2.18) der drei Energieterme liefert sofort die Grenzwerte von r für den Fall der gebundenen Bewegung $( E < 0 )$

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">² 41 wird als „Zentrifugalpotenzial“ bezeichnet (siehe das analoge Problem des α-Teilchens im 7 2 m r Coulombfeld in Anhang 2, Abschnitt A2.4.1 und in Band V, Kapitel „Atomphysik“, Anhang 3). In der Literatur wird oft unkorrekt die potenzielle Energie als Potenzial bezeichnet, auch beim Gravitationspotenzial. Das Potenzial ist gleich der potenziellen Energie pro Masseneinheit (bzw. pro Ladungseinheit im elektrischen Feld) und ist daher eine Eigenschaft des Kraftfeldes, unabhängig von der Masse (bzw. Ladung) des Probekörpers.</span></small>

![](images/page_108_chart_2.jpg)

<details>
<summary>line</summary>

| Parameter | Value |
| --- | --- |
| E, V (Y-intercept) | 0 |
| r (X-intercept) | ~1.5 |
| E_eff (Y-intercept) | 0 |
| r_min: Perihel \((r^{2}\) = 0) | ~0.3 |
| E_kin,rad > 0 | ~0.4 |
| E_max: Aphel \((r^{2}\) = 0) | ~0.6 |
| E = (m/r^2 / 2 + V_eff) | ~1.5 |
</details>

Abb. I-2.18: Energieverhältnisse der Keplerbewegung: nur für $E < 0$ ergibt sich eine periodische Bewegung zwischen $r _ { \mathrm { m a x } }$ und $r _ { \mathrm { m i n } } ,$ den Radien, an denen $\dot { r } = 0$ gilt.

Zur Ableitung des ersten Keplerschen Gesetzeszt gehen wir von der Energieerhaltung aus (Gl. I-2.91), ermitteln $\dot { r }$ zu

$$
\dot {r} = \frac {d r}{d t} = \pm \sqrt {\frac {2}{m} (E - V _ {\mathrm{eff}} (r))} = \pm \sqrt {2 \cdot \frac {E}{m} + \frac {2 \gamma M}{r} - \frac {L ^ {2}}{m ^ {2} r ^ {2}}} \tag {I-2.93}
$$

und suchen die Bahngleichung $r = r ( \varphi )$ . Dazu eliminieren wir die Zeit unter Verwendung der Drehimpulserhaltung. Mit $\dot { \varphi } = \frac { L } { m r ^ { 2 } }$ , also $d \varphi = { \frac { d t \cdot L } { m r ^ { ^ 2 } } }$ erhalten wir so die Differentialgleichung für die Planetenbahn

$$
\frac {d r}{d \varphi} = \frac {m r ^ {2}}{L} \cdot \frac {d r}{d t} = \pm \frac {r ^ {2}}{\frac {L}{m}} \sqrt {2 \cdot \frac {E}{m} + \frac {2 \gamma M}{r} - \frac {\left(\frac {L}{m}\right) ^ {2}}{r ^ {2}}}.\tag {I-2.94}
$$

Für die Lösung findet man<sup>42</sup>

$$
r (\varphi) = \frac {p}{1 + \varepsilon \cos (\varphi)}, \tag {I-2.95}
$$

das ist die Polardarstellung eines Kegelschnitts, wobei der Pol im Brennpunkt liegt (siehe Abb. I-2.19 für den gebundenen Zustand mit $\varepsilon < 1 )$ . In unserem Fall gilt also für den „Parameter“ p

**42** Zunächst setzen wir der einfacheren Schreibung halber $\frac{E}{m}=c\ \text { and }\ \frac{L}{m}=h$ und erhalten so aus Gl. (I-2.94) $d \varphi = \pm   \frac { \displaystyle \frac { h } { r ^ { ^ 2 } } } { \displaystyle \sqrt { 2 c + \frac { 2 \gamma M } { r } - \frac { h ^ { ^ 2 } } { r ^ { ^ 2 } } } }   d r .$ . Der Radikand im Nenner wird in die Differenz zweier

Quadrate umgeschrieben, wodurch die Integration sofort möglich ist: $2c + \frac{2\gamma M}{r} - \frac{h^{2}}{r^{2}} = \alpha^{2} - u^{2}$ mit $\alpha ^ { 2 } = 2 c + \frac { \gamma ^ { 2 } M ^ { 2 } } { h ^ { 2 } } = \mathrm { c o n s t . } , \qquad u ^ { 2 } = \left( \frac { \gamma M } { h } - \frac { h } { r } \right) ^ { 2 } = \frac { \gamma ^ { 2 } M ^ { 2 } } { h ^ { 2 } } - \frac { 2 \gamma M } { r } + \frac { h ^ { 2 } } { r ^ { 2 } } ;$ mit $d u = { \frac { h } { r ^ { ^ 2 } } }   d r$ folgt

$d \varphi = \pm \; \frac { d u } { \sqrt { \alpha ^ { ^ 2 } - u ^ { ^ 2 } } }$ und somit bei der Wahl des <u>negativen</u> Vorzeichens $\varphi + \underbrace{k}_{\substack{Integrations - \\ konstante}} = \arccos \frac{u}{\alpha} \Rightarrow$

$u = \frac{\gamma M}{h} - \frac{h}{r} = \alpha \cdot \cos\left( \varphi + k \right) \Rightarrow r\left( \varphi \right) = \frac{h}{\frac{\gamma M}{h} - \alpha\cos\left( \varphi + k \right)} = \frac{\frac{h^{2}}{\gamma M}}{1 - \frac{\alpha h}{\gamma M} \cdot \cos\left( \varphi + k \right)}$ . Messen wir den

Winkel φ vom Minimalwert des Radius $( , \mathrm { P e r i h e l } ^ { \mathrm { { e } } } )$ weg, dann wird $k = \pi$ für $\varphi = 0$ . Damit erhalten wir die Polardarstellung eines Kegelschnitts mit cos $( \varphi + \pi ) = - \cos { ( \varphi ) }$

$$
r (\varphi) = \frac {p}{1 + \varepsilon \cos (\varphi)}
$$

mit dem „Parameter“ $p = \frac{h^{2}}{\gamma M} = \frac{L^{2}}{\gamma m^{2}M}$ und der „numerischen Exzentrizität“

$\varepsilon = \frac{\alpha h}{\gamma M} = \frac{h}{\gamma M} \sqrt{2 \frac{E}{m} + \frac{\gamma^2 M^2}{h^2}} = \sqrt{1 + \frac{2Ep}{\gamma m M}}$ . Dasselbe Ergebnis hätte sich auch ergeben, wenn wir das positive Vorzeichen der Wurzel gewählt hätten. Für k wäre dann $\frac{3\pi}{2}$ zu wählen, damit an Stelle von cos $( \varphi + k )$ das sich jetzt ergebende sin $( \varphi + k ) = \cos \left( \varphi - { \frac { \pi } { 2 } } + k \right)$ für $\varphi = 0$ den Wert −1 annimmt, denn dann ist wieder sin $\ln(\varphi + k) = \cos\left(\varphi - \frac{\pi}{2} + \frac{3\pi}{2}\right) = \cos(\varphi + \pi) = -\cos(\varphi)$

![](images/page_110_image_2.jpg)

<details>
<summary>text_image</summary>

Aphel
F₂
b
a
ε = e/a
e
p
φ
S = F₁
Perihel
r̃(φ)
P
d\u0304
d\u0304 = 1/2 r̃ × d\u0304 ⇒ d\u0304/dt = 1/2 r̃ × v̄ = 1/2 m L̅ = const.
</details>

Abb. I-2.19: 1. Keplersches Gesetz: Die Planetenbahnen des Sonnensystems sind $( E < 0 )$ Ellipsen, in deren einem Brennpunkt die Sonne steht.

$$
p = \frac {L ^ {2}}{\gamma m ^ {2} M} \quad \text {Parameter der Ellipsenbahn} \tag {I-2.96}
$$

und die „numerische Exzentrizitä $t ^ { \varepsilon } \varepsilon$

$$
\varepsilon = \sqrt {1 + \frac {2 E p}{\gamma m M}} = \sqrt {1 + \frac {2 E L ^ {2}}{m (\gamma m M) ^ {2}}} \quad \begin{array}{l} \text {numerische Exzentrizität} \\ \text {der Ellipsenbahn.} \end{array} \tag {I-2.97}
$$

Für $\varepsilon < 1$ ergibt sich so eine Ellipse, für $\varepsilon = 1$ eine Parabel und für $\varepsilon > 1$ eine Hyperbel. Der gebundene Zustand der Ellipsenbahn mit $E < 0$ ergibt sich also, wenn die kinetische Energie des Himmelskörpers kleiner ist als der Betrag der potenziellen Energie, wenn also gilt

$$
\frac {1}{2} m v ^ {2} <   \gamma \frac {m M}{r}. \tag {I-2.98}
$$

In diesem Fall wird die Gesamtenergie $E = { \frac { 1 } { 2 } }   m   \upsilon ^ { 2 } - \gamma   { \frac { m   M } { r } }$ daher negativ.

Damit ist das erste Keplersche Gesetz abgeleitet:

## 1 Die Planetenbahnen des Sonnensystems sind Ellipsen, in deren einem Brennpunkt die Sonne steht.<sup>43</sup>

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">43 Die Erdbahn ist fast kreisförmig: a = 1 AE (= Astronomische Einheit) = 149,59787⋅ 10<sup>6</sup>km; ε = 0,0162 ⇒ b = a√1 − ε2= 149,578⋅ 106 km . Nur die Venusbahn ist mit ε = 0,0068 noch kreisähnlicher. Die höchste Exzentrizität weist die Merkurbahn mit ε = 0,2056 auf.</span></small>

Die für die Planetenbahn wichtigen Parameter sind die große Halbachse $a = { \frac { p } { 1 - \varepsilon ^ { 2 } } } = -   { \frac { \gamma   m   M } { 2 E } }$ ,44 sie hängt nur von der Gesamtenergie E ab, nicht vom Bahndrehimpuls L, und die kleine Halbachse $b = \frac{p}{\sqrt{1 - \varepsilon^{2}}} = \frac{L}{\sqrt{- 2mE}},$ sie ist bei vorgegebener Energie –E proportional zu L.

Unter Verwendung der beiden Ellipsenachsen a und b erhält man für die numerische Exzentrizität $\varepsilon = \frac{e}{a} = \frac{\sqrt{a^{2} - b^{2}}}{a} = \sqrt{1 - \frac{b^{2}}{a^{2}}}$ und für den Parameter

$$
p = a (1 - \varepsilon^ {2}) = a \left(1 - \left[ 1 - \frac {b ^ {2}}{a ^ {2}} \right]\right) = \frac {b ^ {2}}{a}. \tag {I-2.99}
$$

Die große Halbachse a hängt nur von der Gesamtenergie E ab, umgekehrt hängt die Gesamtenergie $E = -   { \frac { \gamma   m   M } { 2   a } }$ <sub>nur</sub> von der großen Halbachse a ab; alle Ellipsenbahnen mit gleich großer Halbachse a haben daher unabhängig von der kleinen Achse b, also unabhängig vom konstanten Drehimpuls L, dieselbe Energie.<sup>46</sup>

Für $E = \left( { \frac { m   \upsilon ^ { 2 } } { 2 } } - { \frac { \gamma   m   M } { r } } \right) \rightarrow 0 .$ gilt sowohl für die Halbachse $a \rightarrow \infty$ als auch für die Exzentrizität $\varepsilon \to 1$ , die Bahnkurve wird zur Parabel. Besitzt also ein Körper an der Oberfläche eines Zentralkörpers der Masse M und dem Radius R eine Geschwindigkeit $\upsilon \geq \upsilon _ { F l } = \sqrt { \frac { 2 \gamma M } { R } }$ , der Fluchtgeschwindigkeit (escape speed), dann verlässt der Körper den Zentralkörper unabhängig davon, unter welchem Winkel zur Oberfläche er startet. Für $\nu < \nu _ { F l }$ wird die Bahn zur Ellipse $( \varepsilon < 1 )$ , für $\nu > \nu _ { F l }$ zur Hyperbel $( \varepsilon > 1 )$

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">44 Aus der Ellipsengleichung (I-2.95) ergibt sich für φ = 0 und r(0) = a − e (siehe Abb. I-2.18): r(0) = a − aε = a(1 − ε) = p ⇒ a = p = p . Aus Gl. (I-2.97) folgt 1 − ε2 = 2 Ep 1 + ε (1 − ε) (1 + ε) γ mM p γ mM a = 2 2 E 1 − ε</span></small>

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">2 2 45 Es gilt: b<sup>2</sup>= a2− e2= a2− a2ε2= a2(1 − ε<sup>2</sup>) = p (1 − ε2) = p ⇒ (1 − ε2)2 (1 − ε2)</span></small>

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">p L2√γ mML2√γ mM√γ m2ML b = = √1 − ε2γ m2M√−2 Epγ m2M√−2 E⋅L√−2 mE</span></small>

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">46 Diese Tatsache war für die Sommerfeldsche Erweiterung des Bohrschen Atommodells wichtig (vgl. Band V, Kapitel „Atomphysik“, Abschnitt 2.2.4 und Anhang 1).</span></small>

**Beispiel:** Verschiedene Fluchtgeschwindigkeiten.

Erde: $M_{E}=5,98 \cdot 10^{24} \mathrm{~kg}, \quad R_{E}=6,37 \cdot 10^{6} \mathrm{~m} \Rightarrow$

$$
\nu_ {F l} = \sqrt {\frac {2 \cdot 6 , 6 7 \cdot 1 0 ^ {- 1 1} \cdot 5 , 9 8 \cdot 1 0 ^ {2 4}}{6 , 3 7 \cdot 1 0 ^ {6}}} = 1, 1 2 \cdot 1 0 ^ {4} \mathrm{ms} ^ {- 1}
$$

Sonne: $M _ { S } = 1 , 9 9 \cdot { 1 0 } ^ { 3 0 }$ kg, $R_{S}=6,96 \cdot 10^{8}  m  \Rightarrow$

$$
v _ {F l} = \sqrt {\frac {2 \cdot 6 , 6 7 \cdot 1 0 ^ {- 1 1} \cdot 1 , 9 9 \cdot 1 0 ^ {3 0}}{6 , 9 6 \cdot 1 0 ^ {8}}} = 6, 1 8 \cdot 1 0 ^ {5} \mathrm{ms} ^ {- 1}
$$

Mond: $M _ { M } = 7 , 3 4 \cdot { 1 0 } ^ { 2 2 }$ kg, $R_{M}=1,74 \cdot 10^{6}  m  \Rightarrow$

$$
\nu_ {F l} = \sqrt {\frac {2 \cdot 6 , 6 7 \cdot 1 0 ^ {- 1 1} \cdot 7 , 4 3 \cdot 1 0 ^ {2 2}}{1 , 7 4 \cdot 1 0 ^ {6}}} = 2, 3 8 \cdot 1 0 ^ {3} \mathrm{ms} ^ {- 1}
$$

Wir haben schon in Abschnitt 2.2.2 gesehen, dass für eine Zentralkraft gilt

$$
\vec {r} \times \underbrace {m \frac {d ^ {2} \vec {r}}{d t ^ {2}}} _ {\vec {F} \uparrow \downarrow \vec {r}} = m \cdot \vec {r} \times \frac {d ^ {2} \vec {r}}{d t ^ {2}} = 0 \quad \Rightarrow \quad \vec {r} \times \frac {d ^ {2} \vec {r}}{d t ^ {2}} = \frac {d}{d t} \left(\vec {r} \times \frac {d \vec {r}}{d t}\right) = 0
$$

und durch Integration (Gl. I-2.24)

$$
\vec {r} \times \frac {d \vec {r}}{d t} = 2 \vec {c} = \text { const. }
$$

Damit ist die vom Fahrstrahl (Abstand Planet–Sonne) in der Zeiteinheit überstrichene, orientierte Fläche, die Flächengeschwindigkeit

$$
\frac {d \vec {A}}{d t} = \frac {1}{2} (\vec {r} \times \frac {d \vec {r}}{d t}) = \frac {1}{2 m} \vec {L} = \vec {c} \tag {I-2.100}
$$

konstant. Dieser Flächensatz ist das zweite Keplersche Gesetz:

1 In gleichen Zeiten überstreicht der Fahrstrahl (Abstand Planet–Sonne) gleiche Flächen.

Der Flächeninhalt A einer Ellipse ist $A = \pi \cdot a \cdot b$ und mit $b = \sqrt{a \cdot p} = (a \cdot p)^{\gamma_2}$

$$
A = \pi a ^ {3 / 2} p ^ {1 / 2}.
$$

Der Flächensatz (Gl. I-2.100) liefert andererseits nach Integration mit $T$ als Umlaufzeit

$$
A = T \cdot \frac {L}{2 m}.
$$

Wir setzen gleich und quadrieren:

$$
\pi^ {2} a ^ {3} p = T ^ {2} \frac {L ^ {2}}{4 m ^ {2}}
$$

oder mit Gl. (I-2.96)

$$
\frac {a ^ {3}}{T ^ {2}} = \frac {L ^ {2}}{4 \pi^ {2} m ^ {2} p} = \frac {\gamma M}{4 \pi^ {2}}. \tag {I-2.101}
$$

Das Verhältnis $a ^ { 3 } / T ^ { 2 }$ ist damit gleich einer von den Planeten unabhängigen Eigenschaft des Sonnensystems und es gilt somit für zwei beliebige Planeten

$$
a _ {1} ^ {3}: a _ {2} ^ {3} = T _ {1} ^ {2}: T _ {2} ^ {2}. \tag {I-2.102}
$$

Das ist das dritte Keplersche Gesetz:

Die Quadrate der Umlaufzeiten zweier Planeten um die Sonne verhalten sich wie die dritten Potenzen der großen Halbachsen ihrer Ellipsenbahnen.<sup>47</sup>

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">47 In dieser einfachen Form gilt das Gesetz nur für unendlich große Sonnenmasse (keine Sonnenbewegung um den gemeinsamen Schwerpunkt von Sonne und Planet). Bei der exakten Berechung als Zweikörperproblem ist in den dynamischen Beziehungen m durch die reduzierte m M Masse μ = zu ersetzen. Im Kraft- und Potenzialausdruck bleibt m natürlich unverändert m + M (vgl. Gl. (I-2.92): Im ersten Term rechts ist m durch μ zu ersetzen, nicht aber im zweiten Term, 3 a der die potenzielle Energie darstellt). Die obige Beziehung lautet daher genau: T2 2 L 2 μ γ m M γ m M (m + M) a 3 4 π μ p = 11 hängt auch von der Planetenmasse m ab, 4 π2μ2 L2 4 π 2 m M T2 m + M das 3. Keplersche Gesetz ist nur eine Näherung, die aber für m ≪ M sehr gut erfüllt ist.</span></small>

## A1.3 Bestimmung der Erdbeschleunigung

## A1.3.1 Das mathematische, ebene Pendel (simple pendulum)

Schon Newton bestimmte 1686 mit einem Schwerependel die Erdbeschleunigung und fand, dass die Schwingungsdauer nicht vom verwendeten Pendelmaterial abhängt.

Zur Bestimmung der Schwingung eines idealisierten Pendels (mathematisches Pendel) betrachten wir einen Massenpunkt (MP), der an einem masselosen, gespannten Faden im Erdschwerefeld um einen Aufhängepunkt schwingt. Auf den MP wirkt einerseits die Schwerkraft $\vec { F } _ { G } = m \cdot \vec { g }$ , andererseits die Fadenspannung $\vec { F } _ { S }$ , die der Komponente ${ \vec { F } } _ { n }$ der Schwerkraft in Fadenrichtung (Normalkomponente) sowie der Zentrifugalkraft $\vec { F } _ { z f } = m   \frac { \upsilon ^ { 2 } } { r }   \vec { r } _ { 0 } \; ( \vec { r } _ { 0 } =$ Einheitsvektor in Richtung Aufhängepunkt – Massenpunkt) gerade die Waage hält und dadurch den $M P$ auf die Kreisbahn zwingt (Zwangsbedingung).<sup>48</sup> Beschleunigend wirkt daher nur die Tangentialkomponente $\vec { F } _ { t } = m \cdot g \cdot \sin \varphi$ , die dazu führt, dass sich die Bogenlänge $\vec { s }$ mit der Zeit ändert und zwar sich bis zur Vertikallage $( x = 0 )$ verkleinert, sich dann infolge der erreichten kinetischen Energie bis zum maximalen Ausschlag gegen die wirkende Kraft $\vec { F } _ { t }$ vergrößert usf. Die beschleunigende Kraft $\vec { F } _ { t }$ ist also immer entgegen $\vec { s }$ gerichtet.

Entsprechend Abb. I-2.20 muss gelten

$$
m \frac {d ^ {2} s}{d t ^ {2}} = - m g \sin \varphi . \tag {I-2.103}
$$

Mit $s = l \cdot \varphi$ können wir dies in Polarkoordinaten überführen

$$
l m \ddot {\varphi} = - m g \sin \varphi \tag {I-2.104}
$$

und erhalten die Bewegungsgleichung

$$
\ddot {\varphi} + \frac {g}{l} \sin \varphi = 0 \quad \begin{array}{l} \text {Bewegungsgleichung des} \\ \text {mathematischen ebenen Kreispendels.} \end{array} \tag {I-2.105}
$$

Das ist eine nichtlineare Differentialgleichung (DG) 2. Ordnung (siehe Band II, Kapitel „Nichtlineare Dynamik und Chaos“, Abschnitt 2.1.3). Diese Bewegungsgleichung stimmt nicht mit der Schwingungsgleichung des harmonischen Oszillators überein! Nur für den Fall sehr kleiner Auslenkwinkel $\varphi ,$ , für den sin $\varphi \equiv \varphi$ gesetzt werden kann, gilt

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">48 In Fadenrichtung kann sich m nicht bewegen, daher muss die Summe aller Kräfte in dieser Richtung Null sein: F⇀S + F⇀n + F⇀zf = 0 (Abb. I-2.20).</span></small>

![](images/page_115_image_2.jpg)

<details>
<summary>text_image</summary>

y
x
l
φ
Fs = -(mv²/r + mg cos φ) Fadenspannung
m
Fzf = -mv²/r Zentrifugalkraft
s
φ
Fn = mg cos φ Schwerkraft in Fadenrichtung
Ft = mg sin φ
FG = m·g
</details>

Abb. I-2.20: Das mathematische, ebene Pendel. Zur einfacheren Darstellung sind nur die Beträge der wirkenden Kräfte dargestellt. Die Radialkraft $\vec { F } _ { n } + \vec { F } _ { z f }$ wird von der Fadenspannung $\bar { F } _ { S }$ aufgenommen.

$$
\ddot {\varphi} + \frac {g}{l} \varphi = 0 \quad \begin{array}{l} \text {Bewegungsgleichung des} \\ \text {mathematischen ebenen Kreispendels} \\ \text {für sehr kleine Ausschlagswinkel} \varphi , \end{array} \tag {I-2.106}
$$

was zur Schwingungsgleichung des harmonischen Oszillators analog ist (vgl. Kapitel $\mathbf { , } \mathbf { M }$ echanische Schwingungen und Wellen“, Abschnitt 5.1.1). Der Vergleich mit $\ddot { x } + \omega _ { 0 } ^ { 2 }   x = 0$ zeigt, dass in diesem Fall für die Frequenz des mathematischen Pendels gilt

$$
\omega_ {0} = \frac {2 \pi}{T _ {0}} = \sqrt {\frac {g}{l}} \tag {I-2.107}
$$

und damit für die Schwingungsdauer

$$
T _ {0} = 2 \pi \sqrt {\frac {l}{g}}. ^ {4 9} \tag {I-2.108}
$$

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">49 Diese Beziehung wurde erstmals 1673 von Christiaan Huygens (1629–1695) angegeben.</span></small>

Durch Messung der Schwingungsdauer kann also der Betrag der Erdbeschleunigung g gemessen werden.

## A1.3.2 Das physikalische Pendel (physical pendulum)

In diesem Fall schwingt kein Massenpunkt sondern ein starrer Körper um eine raum- und körperfeste Achse (Abb. I-2.21).

![](images/page_116_image_5.jpg)

<details>
<summary>text_image</summary>

-F_{zf} = -m \vec{s} \omega^2
Lagerkraft in O: -m \cdot \vec{g} - m \vec{s} \omega^2
O
s = |\vec{s}|
\vec{r}
dm
d\vec{F}_{zf} = dm \cdot \vec{r} \cdot \omega^2
\vec{g}
\vec{F}_{zf}
\vec{F}_{G} = m \cdot \vec{g}
\varphi
s \cdot \sin \varphi
Die d\vec{F}_{zf} besitzen keine Komponente senkrecht zu \vec{r} und bewirken daher keine Drehung. Ihre vereinigte Wirkung wird durch die Reaktionskraft -F_{zf} = \sum_{i} dm_i r_i \omega^2 in O kompensiert. Im Körper werden dadurch elastische Spannungen hervorgerufen.
Es gilt: F_{zf} = \int_{m} dm \vec{r} \omega^2 = \omega^2 \underbrace{\int_{m} \vec{r} dm}_{= m \vec{s}} = \omega^2 m \vec{s}
</details>

Abb. I-2.21: Das physikalische Pendel.

Zur Beschreibung der Bewegung benützen wir die Bewegungsgleichung $\dot { \bar { L } } = \bar { D }$ Die körperfeste Drehachse durch O legen wir in die z-Achse (normal zur Papierebene); damit liegt auch der Vektor der Winkelgeschwindigkeit $\vec { \omega } = \{ 0 , 0 , \omega _ { z } = \dot { \varphi } \}$ in der z-Achse. Die Komponenten des Drehimpulses sind daher (siehe Kapitel „Mechanik des starren Körpers“, Abschnitt 3.3.4) gemäß der Beziehung $\vec { L } = \tilde { I }   \cdot \vec { \omega }   ^ { 5 0 }$

$$
L _ {x} = I _ {x z} \dot {\varphi}, \quad L _ {y} = I _ {y z} \dot {\varphi}, \quad L _ {z} = I _ {z z} \dot {\varphi}. ^ {5 1} \tag {I-2.109}
$$

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">50 I ̃ ist der Trägheitstensor.</span></small>

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">51 Weist φ̇ in die Richtung einer Hauptachse des Körpers, dann sind nur mehr die diagonalen Trägheitsmomente I<sub>xx</sub>, I<sub>yy</sub>, I<sub>zz</sub> ungleich Null (siehe Kapitel „Mechanik des starren Körpers“, Abschnitt 3.3.2, Gl. 3.31) und es gilt: L<sub>x</sub> = L<sub>y</sub> = 0, L<sub>z</sub> = I<sub>zz</sub>φ̇ = I<sub>c</sub>φ̇ (Bewegung um eine freie Achse).</span></small>

Die Schwerkraft $\vec { F } _ { G } = m \cdot \vec { g }$ greift im Massenmittelpunkt (Schwerpunkt) an und verursacht ein bewegendes Drehmoment um die $z - \mathbf { A } ($ chse (s … Abstand des Schwerpunkts von der Drehachse)

$$
\vec {D} _ {z} = - m g s \cdot \sin \varphi \cdot \vec {e} _ {z}. \tag {I-2.110}
$$

Als Bewegungsgleichung erhalten wir so

$$
\dot {L} _ {z} = I _ {z z} \ddot {\varphi} = - m g s \cdot \sin \varphi \tag {I-2.111}
$$

bzw. mit $I _ { z z } = I _ { O }$ als Trägheitsmoment um die z-Achse

$$
\ddot {\varphi} + \frac {m g s}{I _ {O}} \sin \varphi = 0 ^ {5 2} \quad \begin{array}{l} \text {Bewegungsgleichung des} \\ \text {physikalischen Pendels.} \end{array} \tag {I-2.112}
$$

Diese Gleichung stimmt mit jener des mathematischen Pendels überein, wenn man

$$
\frac {1}{l} = \frac {m s}{I _ {O}} \tag {I-2.113}
$$

setzt.

Für den Fall sehr kleiner Auslenkungen kann man wieder sin $\varphi \equiv \varphi$ setzen und erhält durch Vergleich mit der Schwingungsgleichung des harmonischen Oszillators für die Schwingungsdauer

$$
T ^ {O} = 2 \pi \sqrt {\frac {I _ {O}}{D ^ {*}}} = 2 \pi \sqrt {\frac {I _ {O}}{m g s}} = 2 \pi \sqrt {\frac {l _ {r} ^ {O}}{g}} \quad \begin{array}{l} \text {Schwingungsdauer des} \\ \text {physikalischen Pendels} \\ \text {für kleine Ausschläge,} \end{array} \tag {I-2.114}
$$

wenn man mit $D ^ { \star } = m g s$ das Direktionsmoment bezeichnet. Die Schwingungsdauer $T _ { 0 }$ eines mathematischen Pendels stimmt mit jener des physikalischen $T ^ { o }$ überein, wenn für seine Pendellänge entsprechend Gl. (I-2.113) gilt

$$
l = l _ {r} ^ {O} = \frac {I _ {O}}{m s} \quad \text {reduzierte Pendellänge um} O. \tag {I-2.115}
$$

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">52 Damit erhält man aus den Drehimpulsbeziehungen Gl. (I-2.109) noch zwei weitere periodisch wechselnde Drehmomente D<sub>x</sub> = L̇x = I<sub>xz</sub>φ̈ um die x-Achse und D<sub>y</sub> = L̇y = I<sub>yz</sub>φ̈ um die y-Achse. Da aber die Bewegung nur um die z-Achse möglich ist, werden diese beiden Drehmomente durch gegengleiche Drehmomente in den Lagern der Drehachse („Reaktionsmomente“) aufgehoben. Diese bewirken aber eine erhöhte Lagerreibung und damit eine starke Dämpfung der Drehschwingung. Der Pendelkörper sollte daher immer um eine freie Achse, also um eine Achse größten oder kleinsten Trägheitsmoments, schwingen (siehe dazu Kapitel „Mechanik des starren Körpers“, Abschnitt 3.3.7).</span></small>

**Beispiel:** Reduzierte Pendellänge eines einfachen Kugelpendels mit masselosem Aufhängefaden.

![](images/page_118_image_3.jpg)

<details>
<summary>text_image</summary>

O
z
S
2ρ
m
</details>

Trägheitsmoment um $O$ (nach dem Steinerschen Satz, siehe „Mechanik des starren Körpers“, Abschnitt 3.3.5): $I _ { O } = m   z ^ { 2 } + { \frac { 2 } { 5 } }   m   \rho ^ { 2 } \Rightarrow$ reduzierte Pendellänge

$$
l _ {r} ^ {O} = \frac {I _ {O}}{m z} = \frac {1}{m z} \Bigg (m z ^ {2} + \frac {2}{5} m \rho^ {2} \Bigg) = z + \frac {2}{5} \frac {\rho^ {2}}{z} = z \Bigg (1 + \frac {2}{5} \frac {\rho^ {2}}{z ^ {2}} \Bigg)
$$

$\Rightarrow$ Eine Kugel von 5 cm Durchmesser an einem 1 m langen Faden besitzt eine reduzierte Pendellänge von

$$
l _ {r} ^ {O} = 1 0 0 \left(1 + \frac {2}{5} \cdot \frac {2 , 5 ^ {2}}{1 0 0 ^ {2}}\right) = 1 0 0, 0 2 5 \mathrm{cm} \Rightarrow \frac {T ^ {O}}{T _ {0}} = \sqrt {\frac {l _ {r} ^ {O}}{1 0 0}} = \sqrt {\frac {1 0 0 , 0 2 5}{1 0 0}} = 1, 0 0 0 1 2 5
$$

$\Rightarrow$ wird das Kugelpendel als mathematisches Pendel behandelt, beträgt der Fehler 0,125 ‰!

## A1.3.3 Das Reversionspendel <sup>53</sup>

Schwingungszeiten eines Pendels können zwar sehr genau gemessen werden, der einfache Zusammenhang mit der Erdbeschleunigung ergibt sich aber nur in der Näherung sin $\varphi \equiv \varphi$ . Außerdem müssen neben der Schwingungsdauer auch die Pendellänge oder der Schwerpunktsabstand gemessen werden. Zur genauen Bestimmung der Erdbeschleunigung verwendet man daher ein Reversionspendel. Die ses ist mit zwei Aufhängeschneiden ausgestattet, deren Abstand reguliert werden kann. Es gestattet eine sehr genaue Ermittlung der reduzierten Pendellänge $l _ { r } ^ { o }$

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">53 Erdacht von Johann Gottlieb Friedrich von Bohnenberger (1765–1831), ausgeführt und angewendet von Henry Kater (1777–1835): das „Kater Pendulum“. Das Reversionspendel war lange Zeit das wichtigste Instrument zur Bestimmung der Erdbeschleunigung.</span></small>

![](images/page_119_image_2.jpg)

<details>
<summary>text_image</summary>

m
O
s
l_r^o
S
l_r^o - S
A
x
y
</details>

Abb. I-2.22: Ein physikalisches Pendel mit zwei vertauschbaren Achsen bei O und A im Abstand der reduzierten Pendellänge $l _ { r } ^ { o } .$ .

Wir betrachten nochmals ein physikalisches Pendel und denken uns seine reduzierte Pendellänge $l _ { r } ^ { o }$ vom Drehpunkt O aus in Richtung des Schwerpunkts S bis zum Endpunkt A aufgetragen (Abb. I-2.22).

Jetzt vertauschen wir den bisherigen Drehpunkt O mit A, sodass das Pendel jetzt um A schwingt. Die neue reduzierte Pendellänge für diese Schwingung ist jetzt

$$
l _ {r} ^ {A} = \frac {I _ {A}}{m (l _ {r} ^ {O} - s)}. \tag {I-2.116}
$$

Nach dem Steinerschen Satz gilt allgemein für das Trägheitsmoment $I _ { A ^ { \prime } }$ bei der Drehung um eine Achse A′, die nicht durch den Schwerpunkt geht und zur Schwerpunktsachse A parallel ist (siehe Kapitel „Mechanik des starren Körpers“, Abschnitt 3.3.5)

$$
I _ {A ^ {\prime}} = \underbrace {I _ {A}} _ {\substack {\text {Trägheitsmoment um} \\ \text {Schwerpunktsachse}}} + \underbrace {l ^ {2} m} _ {\substack {\text {Trägheitsmoment der} \\ \text {Gesamtmasse in Sum A ^ {\prime}}}} \tag{I - 2.117}
$$

und daher im vorliegenden Fall für

$$
I _ {A} = \underbrace {I _ {S}} _ {\substack {\text {Trägheitsmoment um} \\ \text {Schwerpunktsachse}}} + \underbrace {(l _ {r} ^ {O} - s) ^ {2} m} _ {\substack {\text {Trägheitsmoment der} \\ \text {Gesamtmasse in Sum A}}}. \tag{I - 2.118}
$$

Für $l _ { r } ^ { A }$ ergibt sich daher

$$
l _ {r} ^ {A} = \frac {I _ {S} + (l _ {r} ^ {O} - s) ^ {2} \cdot m}{m (l _ {r} ^ {O} - s)} = l _ {r} ^ {O} - s + \frac {I _ {S}}{m (l _ {r} ^ {O} - s)}. \tag {I-2.119}
$$

Für $l _ { r } ^ { o }$ ergibt sich mit dem Steinerschen Satz

$$
l _ {r} ^ {O} = \frac {I _ {O}}{m s} = \frac {I _ {S} + s ^ {2} m}{m s} = s + \frac {I _ {S}}{m s} \tag {I-2.120}
$$

und daher

$$
l _ {r} ^ {O} - s = \frac {I _ {S}}{m s}. \tag {I-2.121}
$$

Das setzen wir in den obigen Ausdruck für $l _ { r } ^ { A }$ (Gl. I-2.119) ein und erhalten

$$
l _ {r} ^ {A} = l _ {r} ^ {O}. \tag {I-2.122}
$$

Vertauscht man also den Drehpunkt O mit A, so ändert sich die reduzierte Pendellänge nicht. Damit sind aber auch die beiden Schwingungsdauern gleich, also

$$
T ^ {A} = T ^ {O} \quad \text {Bedingung für das Reversionspendel.} \tag {I-2.123}
$$

Um die Erdbeschleunigung also genau zu messen, hängt man das Reversionspendel abwechselnd an seinen beiden Schneiden auf und reguliert den Schneidenabstand, bis die Schwingungsdauer für beide Aufhängungen genau gleich ist (Abb. I-2.23). Dann ist der leicht messbare Schneidenabstand gleich der reduzierten Pendellänge $l _ { r }$ und es gilt

$$
T = 2 \pi \sqrt {\frac {l _ {r}}{g}}. \tag {I-2.124}
$$

Hieraus kann nun $g$ mit großer Genauigkeit ermittelt werden.

Die Erdbeschleunigung $g$ ist wegen der Erdrotation, der Ortsabhängigkeit des Erdradius aufgrund der Abplattung und der ungleichmäßigen Dichteverteilung vom Ort abhängig. Ein Normwert $g _ { n }$ wurde 1901 international auf den exakten Wert

$$
g _ {n} = 9, 8 0 6 6 5 \mathrm{ms} ^ {- 2}
$$

festgelegt (Normalbeschleunigung). Er galt ursprünglich für Meereshöhe bei einer geographischen Breite von $\varphi = 4 5 ^ { \circ }$ . Wegen der später festgestellten Schwereanomalien (ungleich verteilte Massen im Geoid) ist die Normalbeschleunigung eine willkürliche Festlegung. Sie wirkt in Richtung der Normalen zum Geoid.

![](images/page_121_image_3.jpg)

<details>
<summary>text_image</summary>

Sch 1 (O)
S
s
l_r^O - s
l_r^O = l_r^A
Sch 2 (A)
g
</details>

Abb. I-2.23: Schematische Zeichnung eines Reversionspendels. Gesamte Systemmasse: m.

## A1.4 Bestimmung der Gravitationskonstante

Henry Cavendish (1731–1810) wollte mit einer von John Michell (1724–1793; englischer Naturphilosoph und Geologe) etwa 1760 konstruierten und gebauten Apparatur die Dichte der Erde bestimmen („die Welt abwiegen“). Seine Messwerte wurden erst mehr als 100 Jahre später von Boys (Sir Charles Vernon Boys, 1855–1944) für eine Bestimmung der Gravitationskonstante des Newtonschen Gravitationsgesetzes benützt (C. V. Boys, Nature **50**, 571 (1894)). Zu ihrer Bestimmung muss die Gravitationswirkung zweier bekannter Massen gemessen werden. Die Anordnung von Cavendish war ein „Massendipol“ (Hantel, dumbbell) aus kleinen Bleikugeln als Drehpendel, der mit zwei großen Bleikugeln außen in Wechselwirkung trat (Abbn. I-2.24 und I-2.25)

Wurden die großen Kugeln den kleinen genähert (Abstand der Kugelzentren $r = 230\  mm$ , konnte über den Spiegel durch Verschiebung eines Lichtzeigers auf einer Skala (bzw. die Verschiebung des Nullpunkts bei schwingender Messung) eine Drehung des Pendels gegen die Fadentorsion beobachtet werden. Im Gleichgewicht muss das Drehmoment durch die Massenanziehung $D _ { G r } = l \cdot F = l \cdot \gamma { \frac { m \cdot M } { r ^ { 2 } } }$

![](images/page_122_image_2.jpg)

<details>
<summary>text_image</summary>

l = 180 cm
r = 23 cm
m = 0,73 kg
M = 158 kg
</details>

Abb. I-2.24: Das Cavendish Experiment, 1798: Ein Drehpendel mit zwei kleinen Bleikugeln (blau) wird durch zwei große Bleikugeln (grau) ausgelenkt. Ein Lichtstrahl wird an einem fest mit dem Pendel verbundenen Spiegel reflektiert und zeigt die Auslenkung auf einer Skala.

![](images/page_122_image_4.jpg)

<details>
<summary>text_image</summary>

G H p H G
m
M M
P
r r
F F
K
L
T A E E A
S D W W D T
B C R R C B G
G
</details>

Abb. I-2.25: Schnittzeichnung durch die von Cavendish benützte Drehwaage mit Bleikugeln von 51 mm Durchmesser und $m = 0 , 7 3$ kg in einem Abstand von l = 1,8 m. Die großen Bleikugeln (300 mm Durchmesser, $M = 158    kg$ waren auf einem drehbaren Rahmen montiert. (Nach H. Cavendish, Philosophical Transactions of the Royal Society of London, 88, 469 (1798).)

![](images/page_123_image_2.jpg)

<details>
<summary>natural_image</summary>

Historical illustration of a person operating a large mechanical device with a crane, surrounded by brick and foliage (no visible text or symbols)
</details>

Abb. I-2.26: Radierung, die Cavendish bei der Bestimmung der Gravitationskonstante mit seinem Drehpendel zeigt.

gleich dem Drehmoment durch die Fadentorsion, also dem Produkt aus Direktionsmoment $D ^ { \star } = \frac { \pi } { 2 }   \frac { G \cdot R ^ { 4 } } { L }   ( G )$ … Torsionsmodul des Aufhängedrahtes, R … Drahtdurchmesser, L … Drahtlänge) und Drehwinkel $\varphi$ sein (siehe Kapitel „Mechanik deformierbarer Körper“, Abschnitt 4.2.2), also

$$
D _ {G r} = l \cdot \gamma \frac {m \cdot M}{r ^ {2}} = D _ {T} = D ^ {\star} \cdot \varphi . \tag {I-2.125}
$$

Cavendish bestimmte das Direktionsmoment $D ^ { * }$ seines Drehpendels aus der gemessenen Schwingungsdauer von ca. 7 Minuten (siehe Abschnitt A1.3.2, Gl. I-2.114):

$$
T = 2 \pi \sqrt {\frac {I}{D ^ {*}}}
$$

(Abb. I-2.26).

Unter Vernachlässigung der Masse des Dreharms gegen die Masse der Kugeln folgt für das Trägheitsmoment I der als punktförmig angenommenen Massen m (siehe Kapitel „Mechanik des starren Körpers“, Abschnitt 3.3.4)

$$
I _ {A} = m \left(\frac {l}{2}\right) ^ {2} + m \left(\frac {l}{2}\right) ^ {2} = \frac {2 m l ^ {2}}{4} = \frac {m l ^ {2}}{2} \tag {I-2.126}
$$

und damit

$$
T = 2 \pi \sqrt {\frac {m l ^ {2}}{2 D ^ {*}}} \tag {I-2.127}
$$

bzw.

$$
D ^ {\star} = 4 \pi^ {2} \frac {m l ^ {2}}{2 T ^ {2}}. \tag {I-2.128}
$$

In die Gleichung der Drehmomente Gl. (I-2.125) eingesetzt, kann nach der Gravitationskonstante aufgelöst werden

$$
\gamma = \frac {D ^ {*} r ^ {2} \varphi}{l m M} = \frac {2 \pi^ {2} l r ^ {2}}{M T ^ {2}} \varphi . \tag {I-2.129}
$$

Bei bekanntem $\gamma$ können die Erdmasse und die Erddichte bestimmt werden, wenn man die Gewichtskraft, die auf eine Masse an der Erdoberfläche wirkt, der Gravitationswechselwirkung mit der Erdmasse gleichsetzt, also

$$
F _ {G} ^ {m} = m \cdot g = \gamma \frac {m M _ {E}}{r _ {E} ^ {2}} \tag {I-2.130}
$$

(g … Erdbeschleunigung, $M _ { E }$ … Erdmasse, $r _ { E }$ … Erdradius), woraus sich

$$
M _ {E} = \frac {g \cdot r _ {E} ^ {2}}{\gamma} \quad \text {und} \quad \rho_ {E} = \frac {M _ {E}}{4 \pi r _ {E} ^ {3} / 3} = \frac {3 g}{4 \pi r _ {E} \gamma} \tag {I-2.131}
$$

ergeben.<sup>54</sup>

Cavendish rechnete die Gravitationskonstante nicht explizit aus, sondern bestimmte aus den Verhältniszahlen nur die Dichte der Erde zu $\rho_{E}=5,448\  g\  cm ^{-3}=$ $5 , 4 4 8 \cdot 1 0 ^ { 3 } \mathrm { k g } \mathrm { m } ^ { - 3 }$ .55

Aus dem korrigierten Ergebnis der Erddichte (siehe Fußnote 55) bestimmte Boys 1894 den Wert der Gravitationskonstanten zu

$$
\gamma = g \frac {r _ {E} ^ {2}}{M _ {E}} = 6, 7 4 \cdot 1 0 ^ {- 1 1} \mathrm{m} ^ {3} \mathrm{kg} ^ {- 1} \mathrm{s} ^ {- 2}, \tag {I-2.132}
$$

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">54 Der Erdradius r<sub>E</sub> war durch die erstmals von Tycho Brahe (1589) und Snellius (1615) vorgenommene und später vervollkommnete Gradmessung mittels Triangulation bereits hinreichend bekannt – Gradmessung in Peru (1735–1744) und Lappland (1736–1737) im Auftrage der Academie des Sciences de l’Institut de France (der „Pariser Akademie der Wissenschaften“). Mit dem heutigen mittleren Erdradius r<sub>E</sub>,mittel = 6371 km, einer mittleren Erdbeschleunigung von g = 9,82 m s und der Gravitationskonstante von γ = 6,674 mkg s ergibt sich die Erdmasse zu ME = 5,9723 ⋅ 10 kg. 55 Durch einen Fehler, den Francis Baily (1774–1844) später in der Rechnung fand, war das Ergebnis von Cavendish ρ<sub>E</sub> = 5,48 ± 0,038 g cm (heute: ρE = 5,515 g cm ).</span></small>

einen Wert, der auf 1 % genau mit dem derzeit akzeptierten Wert von

$$
\gamma = (6, 6 7 4 3 0 \pm 0, 0 0 0 1 5) \cdot 1 0 ^ {- 1 1} \mathrm{m} ^ {3} \mathrm{kg} ^ {- 1} \mathrm{s} ^ {- 2} \tag {I-2.132a}
$$

übereinstimmt.<sup>56</sup>

Die Experimente wurden 1896 von Eötvös (Loránd Eötvös, 1848–1919, ungarischer Physiker) mit höherer Präzision wiederholt; Eötvös untersuchte auch in den Jahren ab 1890 bis 1915 mit Hilfe eines Drehpendels, dessen eine Masse aus Platin, die andere aus 8 verschiedenen Stoffen bestand, die Gleichheit von träger und schwerer Masse mit großer Genauigkeit und fand so, dass träge und schwere Masse innerhalb der Messgenauigkeit übereinstimmen. Dicke (Robert Henry Dicke, 1916–1997, US-amerikanischer Physiker) zeigte 1964 in einem aufwendigen Experiment mit einem Drehpendel, das aus drei Massen bestand, zwei aus Aluminium, einer aus Gold,<sup>57</sup> dass der Unterschied in der Gravitationswechselwirkung von Aluminium und Gold kleiner als $( 1 . 3 \pm 1 . 0 ) \cdot { 1 0 } ^ { ^ { - 1 1 } }$ ist, fand also mit hoher Genauigkeit, dass die Gravitationswechselwirkung stoffunabhängig und damit keine Körpereigenschaft ist (P. G. Roll, R. Krotkov und R. H. Dicke, Annals of Physics **26**, 442 (1964)).

Eine sehr genaue Messung der Gravitationskonstanten erfolgte 2000 an der University of Washington in Seattle, USA. Als Pendel wurde in diesem Fall eine flache Platte aus Pyrexglas verwendet, die in einer Vakuumkammer auf einem Torsionsfaden hängend im Zentrum eines Drehtisches angebracht ist, auf dem vier Attraktormassen befestigt sind (Abb. I-2.27).

Wenn sich der Tisch mit konstanter Umdrehungsgeschwindigkeit $\omega _ { \alpha }$ dreht, wird auf das Pendel entsprechend der Gravitationswechselwirkung mit den Attraktormassen ein sinusförmiges Drehmoment ausgeübt. Nun wird die Kammer samt Pendel und Torsionsfaden so hin- und hergedreht $( \omega _ { i } ( t ) )$ , dass die Verdrehung des Pendels relativ zur Kammer minimal ist. In diesem Fall ist die Drehbeschleunigung $\dot { \omega } _ { i } ( t )$ der Vakuumkammer gleich der Drehbeschleunigung des Pendels durch die Gravitationswechselwirkung und diese kann aus der mit $\dot { \omega } _ { i } ( t )$ pendelnden Drehbe wegung der Kammer bestimmt werden. Da der Aufhängefaden praktisch nicht tordiert wird, spielen seine Torsionseigenschaften wie etwa seine Anelastizität keine Rolle. Mit dieser Anordnung wurde die Gravitationskonstante zu

$$
\gamma = (6, 6 7 4 2 1 5 \pm 0, 0 0 0 0 9 2) \cdot 1 0 ^ {- 1 1} \mathrm{m} ^ {3} \mathrm{kg} ^ {- 1} \mathrm{s} ^ {- 2}
$$

bestimmt. Als Erd- und Sonnenmasse ergeben sich daraus

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">56 Wert für 2018 vom Committee on Data for Science and Technology (CODATA) (gültig seit 20. Mai 2019).</span></small>

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">57 Das Drehpendel mit den gleichschweren, aber aus verschiedenen Stoffen bestehenden Kugeln war senkrecht zum Meridian aufgehängt und sollte daher eine Verdrehung erleiden, wenn die Zentrifugalkraft, die ja der trägen Masse proportional ist, zufolge der Erdrotation auf die beiden Kugeln differiert. Der Unterschied erwies sich als kleiner als 10 . Dieses Ergebnis war eine fundamentale Stützung für die allgemeine Relativitätstheorie.</span></small>

![](images/page_126_image_2.jpg)

Abb. I-2.27: Apparat eines modernen Cavendish Experiments. (Nach J. H. Gundlach und S. M. Merkowitz, Physical Review Letters 85, 2869 (2000).)

$$
M _ {E} = (5, 9 7 2 2 4 5 \pm 0, 0 0 0 0 8 2) \cdot 1 0 ^ {2 4} \mathrm{kg}
$$

$$
M _ {S} = (1, 9 8 8 4 3 5 \pm 0, 0 0 0 0 2 7) \cdot 1 0 ^ {3 0} \mathrm{kg}.
$$

Neueste Messungen im MOE Key Laboratory of Fundamental Physical Quantities Measurements, School of Physics der Huazhong University of Science and Technology, Wuhan, China, wurden mit zwei voneinander unabhängigen Bestimmungsmethoden durchgeführt, von denen angenommen wird, dass sie nicht die gleichen systematischen Fehler enthalten: einmal mit der Schwingungsmethode an einem Torsionspendel, einmal wie gerade oben unter Benützung der Wirkung einer Drehbeschleunigung. Die in dieser Weise bestimmten Werte der Graviationskonstanten sind (Qing Li et al., Nature, **560**, 582 (2018)): $( 6 , 6 7 4 1 8 4 \pm 0 , 0 0 0 0 7 8 ) \cdot 1 0 ^ { - 1 1 }   \mathrm { m } ^ { 3 }   \mathrm { k g } ^ { - 1 }   \mathrm { s } ^ { - 2 }$ (Schwingung) und $( 6 , 6 7 4 4 8 4 \pm 0 , 0 0 0 0 7 8 ) \cdot 1 0 ^ { - 1 1 }   \mathrm { m } ^ { 3 }   \mathrm { k g } ^ { - 1 }   \mathrm { s } ^ { - 2 }$ (Drehbeschleunigung).

In jüngerer Zeit wurde auch der Versuch unternommen, das $1 / r ^ { 2 }$ Verhalten des Gravitationsgesetzes auf sehr kleinen Längenskalen (10 mm bis 55 μm) zu überprü- fen.<sup>58</sup> In diesem „Molybdän-Scheibenexperiment“ (auch „Eöt-Wash-Experiment“genannt, D. J. Kapner, T. S. Cook, E. G. Adelberger, J. H. Gundlach, B. R. Heckel, C. D. Hoyle und H. E. Swanson, Physical Review Letters **98**, 021101 (2007)) hängt an einem dünnen, 80 cm langen Wolframfaden eine Molybdänscheibe mit 42 kreisförmigen Löchern und bildet ein Drehpendel (Detektorscheibe). Knapp unter dieser Detektorscheibe befinden sich zwei starr miteinander verbundene Molybdänscheiben, das Attraktorsystem, das mit konstanter Winkelgeschwindigkeit rotieren kann: die obere Scheibe des Attraktors ist gleich dick wie die Detektorscheibe und hat auch 42 Löcher; die untere Scheibe ist dicker, weist nur 21, aber doppelt so große Löcher auf und ist gegen die obere um einen Winkel von $3 6 0 / 4 2 ^ { \circ }$ verdreht, sodass die Löcher der unteren Scheibe gerade unter den massiven Zwischenstegen der oberen Scheibe liegen (Abb. I-2.28). Die Löcher in den Scheiben erhöhen die Empfindlichkeit des Systems für die horizontalen Gravitationskräfte zwischen den Scheiben (als fehlende Masse können die Löcher als „negative Masse“ angesehen werden). Bei geeigneter Größe und Anordnung der Löcher in den beiden gleichdicken Scheiben ist die Gravitationswechselwirkung bei rotierendem Attraktor durch den Wechsel zwischen übereinander liegenden Massenbereichen (Zwischenstegen) und masselosen Löchern kurzzeitig höher und wieder niedriger. Dies würde zur Schwingung der Detektorscheibe führen, wenn sich die obere Attraktorscheibe dreht. Wird aber die Dicke der unteren Attraktorscheibe geeignet gewählt, so tritt gerade keine Torsionsschwingung auf, wenn das $1 / r ^ { 2 }$ Gesetz gilt. Die sehr genaue Untersuchung als Funktion der Distanz der Scheiben ergab keine Abweichungen vom $1 / r ^ { 2 }$ -Verhalten bis zu einem Scheibenabstand von 55 μm, der Messgrenze dieser Anordnung.

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">58 Zur Erklärung kosmologischer Effekte (dunkle Materie, kosmologische Konstante) wurden Ideen entwickelt, die in die Richtung einer schwächer werdenden Gravitationskraft weisen, wenn die Abstände in die Größenordnung einer kritischen Länge von 85 μm kommen.</span></small>

![](images/page_127_image_2.jpg)

<details>
<summary>text_image</summary>

5 cm
Detektorscheibe
Attraktorsystem
</details>

Abb. I-2.28: Eöt-Wash-Experiment zum Nachweis des $1 / r ^ { 2 } .$ -Verhaltens der Gravitation: Schematische Darstellung der verwendeten ‚missing mass torsion balance‘. Die drei kleinen Kugeln dienen zur kontinuierlichen Kalibrierung des Drehmoments der Detektorscheibe durch Gravitationswechselwirkung mit drei großen Kugeln außerhalb der Apparatur. (Nach D. J. Kapner, T. S. Cook, E. G. Adelberger, J. H. Gundlach, B. R. Heckel, C. D. Hoyle und H. E. Swanson, Physical Review Letters 98, 021101 (2007).)