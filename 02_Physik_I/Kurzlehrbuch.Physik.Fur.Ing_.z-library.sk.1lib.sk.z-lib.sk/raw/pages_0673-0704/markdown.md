in Abb. 27.11c gleich der Vektorsumme der drei Zeiger für die Spannungen $V _ { R } ,   V _ { C }$ und $V _ { L }$ in Abb. 27.11b ist.

Diese Forderung illustriert Abb. 27.11d: Der Zeiger für $\mathcal { E } _ { \mathrm { m } }$ ist gleich der Summe der drei Zeiger für $V _ { R } , \; V _ { C }$ und $V _ { L } .$ . Da die beiden Zeiger für $V _ { L }$ und $V _ { C }$ entgegengesetzt gerichtet sind, können wir die Vektorsumme vereinfachen, indem wir zunächst $V _ { L }$ und $V _ { C }$ zu einem einzelnen Zeiger $V _ { L } - V _ { C }$ vereinen. Anschließend bilden wir die Summe aus diesem Zeiger und dem Zeiger für $V _ { R ^ { 1 } }$ . Diese Summe muss wie in der Abbildung dargestellt gleich dem Zeiger für $\mathcal { E } _ { \mathrm { m } }$ sein.

Beide Dreiecke in Abb. 27.11d sind rechtwinklig; nach dem Satz des Pythagoras gilt daher

$$
\mathcal {E} _ {\mathrm{m}} ^ {2} = V _ {R} ^ {2} + (V _ {L} - V _ {C}) ^ {2}. \tag {27.48}
$$

Mithilfe der Angaben aus Tab. 27.2 können wir die Amplituden auch durch die Stromamplitude und die Widerstände ausdrücken:

$$
\mathcal {E} _ {\mathrm{m}} ^ {2} = (I R) ^ {2} + (I X _ {L} - I X _ {C}) ^ {2}. \tag {27.49}
$$

Damit folgt für die Stromamplitude

$$
I = \frac {\mathcal {E} _ {\mathrm{m}}}{\sqrt {R ^ {2} + (X _ {L} - X _ {C}) ^ {2}}}  . \tag {27.50}
$$

Den Nenner in dieser Gleichung bezeichnet man als **Impedanz** $Z$ (oder den **Scheinwiderstand**) des Stromkreises für die antreibende Kreisfrequenz $\omega _ { \mathrm { a } } !$ :

$$
Z = \sqrt {R ^ {2} + (X _ {L} - X _ {C}) ^ {2}} \quad (\text {Definition der Impedanz}). \tag {27.51}
$$

Damit können wir Gl. 27.50 in der Form

$$
I = \frac {\mathcal {E} _ {\mathrm{m}}}{Z} \tag {27.52}
$$

schreiben. Wenn wir nun noch $X _ { L }$ und $X _ { C }$ nach den Gln. 27.34 bzw. 27.41 ersetzen, wird aus Gl. 27.50

$$
I = \frac {\mathcal {E} _ {\mathrm{m}}}{\sqrt {R ^ {2} + (\omega_ {\mathrm{a}} L - 1 / (\omega_ {\mathrm{a}} C)) ^ {2}}} \quad \text {(Stromamplitude)}. \tag {27.53}
$$

Die Hälfte unseres Ziels haben wir damit erreicht: Wir haben einen Ausdruck für die Stromstärke I als Funktion der antreibenden Spannung und der Komponenten des in Reihe geschalteten RLC-Kreises erhalten.

Die Stromamplitude I hängt nach Gl. 27.53 von der Differenz zwischen $\omega _ { \mathrm { a } } L$ und $1 / ( \omega _ { \mathrm { a } } C )$ bzw. nach Gl. 27.50 von der Differenz zwischen $X _ { L }$ und $X _ { C }$ ab. Welcher dieser beiden Widerstände größer ist, spielt dabei keine Rolle, da die Differenz quadratisch in die Stromamplitude eingeht.

Bei dem in diesem Abschnitt betrachteten Strom handelt es sich um den Dauerstrom, der sich nach längerer Zeit einstellt. Beim Einschalten einer Spannungsquelle kann ein kurzer Start- oder Einschaltstrom auftreten. Seine Dauer (bevor er in den Dauerstrom übergeht) hängt von den Zeitkonstanten $\tau _ { L }   =   L / R$ und $\tau _ { C } = R C$ ab, mit denen die induktiven und kapazitiven Komponenten des Stromkreises „eingeschaltet“ werden. Ein solcher Einschaltstrom kann sehr groß werden und beispielsweise einen Motor beim Anlassen zerstören, wenn er nicht bereits beim Entwurf der elektrischen Schaltkreise berücksichtigt wird.

## Die Phasenkonstante

Aus dem rechtwinkligen Zeigerdreieck in Abb. 27.11d sowie Tab. 27.2 entnehmen wir die Beziehung

$$
\tan \varphi = \frac {V _ {L} - V _ {C}}{V _ {R}} = \frac {I X _ {L} - I X _ {C}}{I R} \tag {27.54}
$$

![](images/page_673_image_1.jpg)

bzw.

$$
\tan \varphi = \frac {X _ {L} - X _ {C}}{R} \quad (\text {Phasenkonstante}). \tag {27.55}
$$

Damit haben wir auch unser zweites Ziel erreicht: Wir haben eine Gleichung für die Phasenkonstante $\varphi$ in einem Reihen-RLC-Kreis hergeleitet. Je nach den relativen Werten von $X _ { L }$ und $X _ { C }$ können wir drei Situationen unterscheiden:

1. $X _ { L } > X _ { C } ;$ In diesem Fall sagt man, der Schaltkreis habe induktiven Charakter. Nach Gl. 27.55 ist $\varphi$ für diesen Schaltkreis positiv, der Zeiger für I rotiert daher stets hinter dem Zeiger für $\mathcal { E } _ { \mathrm { m } }$ (Abb. 27.12a). In einem Liniendiagramm von  und i als Funktionen der Zeit erhält man einen Graphen wie in Abb. 27.12b. (Dieser Fall wird auch durch die Abb. 27.11c und d beschrieben.)
2. $X _ { C }   >   X _ { L }$ : In diesem Fall hat der Schaltkreis kapazitiven Charakter. Nach Gl. 27.55 ist $\varphi$ für diesen Schaltkreis negativ, der Zeiger für I rotiert demzufolge vor dem Zeiger für $\mathcal { E } _ { \mathrm { m } }$ (Abb. 27.12c). Trägt man  und i als Funktion der Zeit auf, erhält man das Liniendiagramm aus Abb. 27.12d.
3. $X _ { C } = X _ { L } ;$ In diesem Fall sagt man, der Schaltkreis befinde sich in Resonanz. Diesen Zustand behandeln wir im kommenden Abschnitt. Nach Gl. 27.55 gilt für einen solchen Schaltkreis $\varphi = 0 ^ { \circ }$ , die Zeiger für $\mathcal { E } _ { \mathrm { m } }$ und I liegen folglich übereinander und rotieren gemeinsam (Abb. 27.12e). Das Liniendiagramm für  und i als Funktion der Zeit hat die in Abb. 27.12f dargestellte Form.

Zur Illustration wollen wir nochmals die beiden Extremfälle betrachten: In dem rein induktiven Stromkreis aus Abb. 27.10a ist $X _ { L }$ von null verschieden und $X _ { C } =$ $R = 0$ . Nach Gl. 27.55 ist dann $\varphi = + 9 0 ^ { \circ }$ (der größtmögliche Werte für 𝜑), im Einklang mit Abb. 27.10c. In dem rein kapazitiven Stromkreis aus Abb. 27.9a ist $X _ { C }$ von null verschieden und $X _ { L } = R = 0$ . Nach Gl. 27.55 ist hier $\varphi = - 9 0 ^ { \circ }$ (der kleinstmögliche Wert für $\varphi )$ , was auch aus dem Liniendiagramm in Abb. 27.9c zu erkennen ist.

## Resonanz

Gleichung 27.53 gibt uns die Stromamplitude I eines RLC-Kreises als Funktion der Kreisfrequenz $\omega _ { \mathrm { a } }$ der äußeren Wechselspannung an. Für einen gegebenen Wirkwiderstand R nimmt diese Amplitude ihren Maximalwert an, wenn der Term $\omega _ { \mathrm { a } } L -$ $1 / ( \omega _ { \mathrm { a } } C )$ im Nenner null wird, also für

$$
\omega_ {\mathrm{a}} L = \frac {1}{\omega_ {\mathrm{a}} C}
$$

![](images/page_674_chart_2.jpg)

<details>
<summary>line</summary>

| \(\omega a/\omega\) | R = \(10 \Omega\) | R = \(30 \Omega\) | R = \(100 \Omega\) |
| --- | --- | --- | --- |
| 0.90 | ~0.05 | ~0.02 | ~0.01 |
| 0.95 | ~0.15 | ~0.10 | ~0.05 |
| 1.00 | ~1.00 | ~0.45 | ~0.15 |
| 1.05 | ~0.15 | ~0.10 | ~0.05 |
| 1.10 | ~0.05 | ~0.02 | ~0.01 |
</details>

oder

$$
\omega_ {\mathrm{a}} = \frac {1}{\sqrt {L C}} \quad (\text {maximaler Strom} I). \tag {27.56}
$$

Dies ist gleichzeitig die natürliche Kreisfrequenz ω eines RLC-Kreises. I wird also maximal, wenn die Kreisfrequenz der angelegten Spannung gleich der natürlichen Kreisfrequenz ist – d. h. im Resonanzfall. Die Bedingung für Resonanz und eine maximale Stromamplitude in einem Reihen-RLC-Kreis ist daher

$$
\omega_ {\mathrm{a}} = \omega = \frac {1}{\sqrt {L C}} \quad (\text {Resonanz}). \tag {27.57}
$$

Abbildung 27.13 zeigt drei Resonanzkurven für sinusförmig angetriebene Schwingungen von drei Reihen-RLC-Kreisen, die sich nur in ihrem Wirkwiderstand R unterscheiden. In allen Kurven erreicht die Stromamplitude für $\omega _ { \mathrm { a } } / \omega = 1 \mathrm { , } 0 0$ ihr Maximum, allerdings nimmt die maximale Amplitude mit zunehmendem R ab. (Der Maximalwert ist immer gleich $\mathcal { E } _ { \mathrm { m } } / R ,$ wie die Gln. 27.51 und 27.52 zeigen.) Außerdem nimmt die Breite der Kurven (die in Abb. 27.13 jeweils in halber Maximalhöhe gemessen wurde) mit zunehmendem R stark zu.

Um die Kurven in Abb. 27.13 physikalisch zu interpretieren, betrachten wir die Widerstände $X _ { L }$ und $X _ { C }$ als Funktionen der angelegten Kreisfrequenz $\omega _ { \mathrm { a } }$ . Wir beginnen bei Werten weit unterhalb der natürlichen Kreisfrequenz ω. In diesem Fall ist der induktive Widerstand $X _ { L } ~ ( = \omega _ { \mathrm { a } } L )$ sehr klein und der kapazitive Widerstand $X _ { C } \left( = 1 / \omega _ { \mathrm { a } } C \right)$ sehr groß. Der Stromkreis ist also überwiegend kapazitiv und die Impedanz ist vorwiegend durch den großen Wert von $X _ { C }$ bestimmt. Der Strom ist aus diesem Grund klein.

Mit zunehmendem $\omega _ { \mathrm { a } }$ dominiert $X _ { C }$ zwar zunächst weiterhin, nimmt aber allmählich ab, wohingegen $X _ { L }$ zunimmt. Die Abnahme von $X _ { C }$ verringert die Impedanz, der Strom nimmt daher zu, wie man auf der linken Seite der Resonanzkurven in Abb. 27.13 erkennt. Wenn $X _ { L }$ und $X _ { C }$ schließlich gleich groß sind, ist $\omega _ { \mathrm { a } } = \omega ,$ der Strom ist maximal und der Stromkreis befindet sich in Resonanz.

Wenn $\omega _ { \mathrm { a } }$ weiter zunimmt, steigt auch $X _ { L }$ weiter und überwiegt schließlich über das immer kleiner werdende $X _ { C ^ { \prime } }$ . Die Impedanz steigt nun wegen $X _ { L }$ und der Strom nimmt ab, wie man auf der rechten Seite der Kurven in Abb. 27.13 erkennt.

Zusammenfassend können wir sagen: Die niederfrequente Seite einer Resonanzkurve wird vorwiegend durch den kapazitiven Widerstand bestimmt, die hochfrequente Seite durch den induktiven Widerstand. Genau in der Mitte der Kurve tritt Resonanz auf.

## KONTROLLFRAGE 7

Die kapazitiven und induktiven Widerstände dreier RLC-Wechselstromkreise seien: (1) 50 Ω∕100 Ω, (2) 100 Ω∕50 Ω und (3) 50 Ω∕50 Ω. (a) In welchem der Fälle eilt der Strom der angelegten Spannung nach, in welchem der Fälle eilt er voran und in welchem der Fälle sind Strom und Spannung in Phase? (b) Welcher der Stromkreise befindet sich in Resonanz?

## Abb. 27.13

Resonanzkurven für den RLC-Kreis aus Abb. 27.7 mit $L   =   1 0 0   \mu \mathrm { H } ,$ $C = 1 0 0   \mathrm { p F }$ und drei verschiedenen Werten für R. Die Amplitude I des Wechselstroms hängt von der Differenz zwischen der antreibenden Frequenz $\omega _ { \mathrm { a } }$ und der natürlichen Kreisfrequenz ω ab. Die horizontalen Pfeile an den Kurven zeigen die Breite der Kurven in halber Höhe und sind ein Maß für die Schärfe der Resonanz. Links von $\omega _ { \mathrm { a } } / \omega = 1 \mathrm { , } 0 0$ ist der Stromkreis vorwiegend kapazitiv mit $X _ { C } > X _ { L } ;$ rechts davon ist er überwiegend induktiv mit $X _ { L } > X _ { C }$

## 27.5 Leistung in Wechselstromkreisen

![](images/page_675_image_2.jpg)

## Lernziele

Nach dem Durcharbeiten dieses Abschnitts sollten Sie in der Lage sein, . . .

• den Zusammenhang zwischen Amplituden und Effektivwerten von Wechselstromgrößen wie Strom und Spannung zu verstehen,
den sinusförmigen Verlauf von Strom und Spannung an dem Bauelement zu skizzieren, wenn eine Wechselspannung an einen Widerstand, einen Kondensator oder eine Induktivität angelegt wird, und in dem Diagramm die Spitzenund Effektivwerte des Stroms bzw. der Spannung zu identifizieren,
• die Beziehung zwischen gemittelter Leistung $P _ { \mathrm { g e m } }$ , Effektivwert des Stroms $I _ { \mathrm { e f f } }$ und Widerstand R anzuwenden,
• die Leistung aller Bauelemente in einem periodisch angetriebenen RLC-Kreis zu berechnen,
• zu erklären, was in einem angetriebenen RLC-Kreis im stationären Zustand mit der mittleren gespeicherten Energie sowie der vom Generator in den Stromkreis eingebrachten Energie geschieht,
• die Beziehung zwischen dem Leistungsfaktor cos 𝜑, dem Widerstand R und der Impedanz Z anzuwenden,
• die Beziehung zwischen der gemittelten Leistung $P _ { \mathrm { g e m } } ,$ dem Effektivwert $\mathcal { E } _ { \mathrm { e f f } }$ der Spannung, dem Effektivwert $I _ { \mathrm { e f f } }$ des Stroms und dem Leistungsfaktor cos 𝜑 anzuwenden,
• zu verstehen, welcher Leistungsfaktor erforderlich ist, um die Energieübertragungsrate auf einen Lastwiderstand (also die dort anfallende Leistung) zu maximieren.

![](images/page_675_image_14.jpg)

## Schlüsselideen

• In einem Reihen-RLC-Kreis ist die gemittelte Leistung $P _ { \mathrm { g e m } }$ des Generators gleich der Produktionsrate von thermischer Energie im Widerstand (also der dortigen Wärmeleistung):

$$
P _ {\mathrm{gem}} = I _ {\mathrm{eff}} ^ {2} R = I _ {\mathrm{eff}} \mathcal {E} _ {\mathrm{eff}} \cos \varphi .
$$

• Die Effektivwerte hängen mit den Amplituden bzw. Spitzenwerten der Wechselstromgrößen gemäß

$$
I _ {\mathrm{eff}} = \frac {I}{\sqrt {2}} \quad \mathrm{bzw.} \quad \mathcal {E} _ {\mathrm{eff}} = \frac {\mathcal {E} _ {\mathrm{m}}}{\sqrt {2}}
$$

zusammen. Der Term cos 𝜑 heißt Leistungsfaktor des Stromkreises.

## 27.5.1 Leistung in Wechselstromkreisen

In dem RLC-Kreis aus Abb. 27.7 ist der Wechselstromgenerator die Energiequelle. Ein Teil der von ihm gelieferten Energie wird im elektrischen Feld des Kondensators gespeichert, ein Teil im Magnetfeld der Spule und ein Teil wird im Wirkwider stand in Wärmeenergie umgewandelt. Im Dauerbetrieb – den wir hier annehmen – bleibt die mittlere Energie im Kondensator und in der Spule konstant. Im Wesentlichen fließt die Energie des Wechselstromgenerators dann in den Wirkwiderstand, wo sie in Wärmeenergie umgewandelt (dissipiert) wird.

Für die momentane Leistung, d. h. die Rate, mit der Energie in einem bestimmten Augenblick im Wirkwiderstand dissipiert wird, erhalten wir mithilfe der Gln. 22.22 und 27.25

$$
P = i ^ {2} R = [ I \sin (\omega_ {\mathrm{a}} t - \varphi) ] ^ {2} R = I ^ {2} R \sin^ {2} (\omega_ {\mathrm{a}} t - \varphi). \tag {27.58}
$$

Die mittlere Leistung am Wirkwiderstand erhalten wir durch Mittelung von Gl. 27.58 über die Zeit. Der Mittelwert von sin θ (wobei θ eine beliebige Variable ist) über eine ganze Periode verschwindet (Abb. 27.14a), aber der Mittelwert von $\sin ^ { 2 } \theta$ ist gleich 1/2 (Abb. 27.14b). (Man kann in Abb. 27.14b erkennen, dass die schattierte Fläche unter der Kurve oberhalb der gestrichelten horizontalen Linie bei sin<sup>2</sup> $^ { 2 } \theta = + 1 / 2$ exakt gleich der nicht schattierten Fläche unterhalb dieser Linie ist.) Damit erhalten wir aus Gl. 27.58

$$
P _ {\mathrm{gem}} = \frac {I ^ {2} R}{2} = \left(\frac {I}{\sqrt {2}}\right) ^ {2} R. \tag {27.59}
$$

Die Größe $I / \sqrt { 2 }$ bezeichnet man als **quadratisches Mittel** oder **Effektivwert** des Stroms i:

$$
I _ {\mathrm{eff}} = \frac {I}{\sqrt {2}} \quad (\text {Effektivwert des Stroms}). \tag {27.60}
$$

Damit wird Gl. 27.59 zu

$$
P _ {\mathrm{gem}} = I _ {\mathrm{eff}} ^ {2} R \quad (\text {mittlere Leistung}). \tag {27.61}
$$

Gleichung 27.61 hat dieselbe mathematische Form wie Gl. 26.22 $( P = i ^ { 2 } R )$ . Das zeigt uns, dass wir die mittlere Leistung (Energiedissipationsrate) eines Wechselstromkreises auf dieselbe Weise wie bei einem Gleichstromkreis berechnen können, wenn wir für den Strom seinen Effektivwert einsetzen.

Ebenso wie für den Strom können wir auch für die Spannungen Effektivwerte einführen:

$$
V _ {\text {eff}} = \frac {V}{\sqrt {2}} \quad \text {und} \quad \mathcal {E} _ {\text {eff}} = \frac {\mathcal {E} _ {\mathrm{m}}}{\sqrt {2}} \quad \text {(Effektivwerte der Spannungen). (27.62)}
$$

Messgeräte für Wechselstromschaltungen wie Amperemeter und Voltmeter sind gewöhnlich so kalibriert, dass sie die Effektivwerte $I _ { \mathrm { e f f } }$ und $\mathcal { E } _ { \mathrm { e f f } }$ anzeigen. Wenn Sie also ein Voltmeter in eine gewöhnliche Steckdose stecken und 230 V ablesen, handelt es sich dabei um den Effektivwert der Spannung. Der maximale Momentanwert der Spannung an dieser Steckdose ist ${ \sqrt { 2 } } \cdot ( 2 3 0   \mathrm { V } ) = 3 2 5   \mathrm { V } .$

Der Proportionalitätsfaktor $1 / \sqrt { 2 }$ ist in den Gln. 27.60 und 27.62 für alle drei Größen derselbe, daher können wir die Gln. 27.52 und 27.50 auch in die Form

$$
I _ {\mathrm{eff}} = \frac {\mathcal {E} _ {\mathrm{eff}}}{Z} = \frac {\mathcal {E} _ {\mathrm{eff}}}{\sqrt {R ^ {2} + (X _ {L} - X _ {C}) ^ {2}}} \tag {27.63}
$$

bringen. In dieser Form werden wir diese Beziehung meist verwenden.

Mit dieser Gleichung können wir auch Gl. 27.61 in eine äquivalente und oft verwendete Form bringen. Dazu schreiben wir zunächst

$$
P _ {\mathrm{gem}} = \frac {\mathcal {E} _ {\mathrm{eff}}}{Z} I _ {\mathrm{eff}} R = \mathcal {E} _ {\mathrm{eff}} \mathrm{I} _ {\mathrm{eff}} \frac {R}{Z}. \tag {27.64}
$$

Aus Abb. 27.11d, Tab. 27.2 und Gl. 27.52 können wir jedoch ablesen, dass $R / Z$ gerade der Kosinus der Phasenkonstante 𝜑 ist:

$$
\cos \varphi = \frac {V _ {R}}{\mathcal {E} _ {\mathrm{m}}} = \frac {I R}{I Z} = \frac {R}{Z}. \tag {27.65}
$$

Damit erhalten wir Gl. 27.64 in der Form

$$
P _ {\mathrm{gem}} = \mathcal {E} _ {\mathrm{eff}} I _ {\mathrm{eff}} \cos \varphi \quad \text {(mittlere Leistung)}. \tag {27.66}
$$

Den Faktor cos 𝜑 in dieser Gleichung bezeichnet man als **Leistungsfaktor**. Da cos $\varphi = \cos ( - \varphi )$ ist, hängt Gl. 27.66 nicht vom Vorzeichen der Phasenkonstante 𝜑 ab.

![](images/page_676_chart_22.jpg)

<details>
<summary>line</summary>

| \(\theta\) | sin \(\theta\) |
| --- | --- |
| 0 | 0 |
| ~\(0.5\pi\) | +1 |
| \(\pi\) | 0 |
| ~\(1.5\pi\) | -1 |
| \(2\pi\) | 0 |
| ~\(2.5\pi\) | +1 |
| \(3\pi\) | 0 |
</details>

(a)

![](images/page_676_chart_24.jpg)

<details>
<summary>area</summary>

| \(\theta\) | \(sin^{2}\theta\) |
| --- | --- |
| 0 | 0 |
| ~\(0.5\pi\) | +1 |
| \(\pi\) | 0 |
| ~\(1.5\pi\) | +1 |
| \(2\pi\) | 0 |
| ~\(2.5\pi\) | +1 |
| \(3\pi\) | 0 |
</details>

(b)

## Abb. 27.14

(a) Die Auftragung von sin θ als Funktion von $\theta ;$ der Mittelwert über eine ganze Periode ist null. (b) Die Auftragung von sin<sup>2</sup> θ als Funktion von θ; der Mittelwert über eine Periode ist 1/2.

Wenn die dem Lastwiderstand in einem RLC-Kreis zugeführte Leistung möglichst groß sein soll, sollte der Leistungsfaktor cos 𝜑 möglichst nahe bei eins liegen. Das ist gleichbedeutend mit der Forderung, dass die Phasenkonstante $\varphi$ in Gl. 27.25 möglichst nahe bei null liegen soll. Einen stark induktiven Charakter eines Stromkreises können wir durch die Reihenschaltung von Kapazitäten abschwä- chen. (Schaltet man zusätzliche Kapazitäten in Reihe mit bereits vorhandenen Kapazitäten, so wird die Gesamtkapazität $C _ { \mathrm { E r s } }$ dieser Reihe kleiner und damit $X _ { C }   { \bf g r } { \ddot { \bf o } } \cdot$ ßer.) Die resultierende Abnahme von $C _ { \mathrm { E r s } }$ verkleinert daher die Phasenkonstante und erhöht den Leistungsfaktor in Gl. 27.66. Diese Eigenschaft wird von Elektrizitätswerken ausgenutzt, die in ihren Stromkreisen an geeigneten Stellen zusätzliche Kondensatoren in Reihe schalten.

## KONTROLLFRAGE 8

(a) Angenommen, der Strom in einem Reihen-RLC-Kreis an einer sinusförmigen Wechselspannung eilt dieser Spannung voran. Sollte man die Kapazität erhöhen oder verringern, um die Leistung am Wirkwiderstand zu erhöhen? (b) Wird sich durch diese Veränderung die Resonanzfrequenz des Stromkreises der angelegten Wechselspannungsfrequenz nähern oder sich von ihr entfernen?

## 27.6 Transformatoren

![](images/page_677_image_5.jpg)

## Lernziele

Nach dem Durcharbeiten dieses Abschnitts sollten Sie in der Lage sein, . . .

• zu erklären, warum bei der Spannungsübertragung in Überlandleitungen der Strom gering und die Spannung hoch sein sollte,
• die Aufgaben der Transformatoren an den Enden einer solchen Leitung zu beschreiben,
• die Energiedissipation in einer Hochspannungsleitung zu berechnen,
• die Primär- und Sekundärseite eines Transformators zu identifizieren,
• die Beziehung zwischen Spannungen und Windungszahlen auf den beiden Seiten eines Transformators anzuwenden,
• zwischen einem Aufwärts- und einem Abwärtstransformator zu unterscheiden,
• die Beziehung zwischen Strömen und Windungszahlen auf den beiden Seiten eines Transformators anzuwenden,
• die Beziehung zwischen der in einen Transformator hineingesteckten und der aus ihm herauskommenden Leistung zu kennen,
• den äquivalenten Ersatzwiderstand aus Sicht der Primärseite eines Transformators anzugeben,
• die Beziehung zwischen äquivalentem Ersatzwiderstand und realem Widerstand anzuwenden,
• die Rolle des Transformators bei der Impedanzanpassung zu erläutern.

![](images/page_677_image_20.jpg)

## Schlüsselideen

Ein idealer Transformator ist ein ringförmiger Eisenkern, auf dessen einer Seite eine Primärspule mit $N _ { \mathrm { p } }$ Windungen und auf dessen anderer Seite eine Se kundärspule mit $N _ { s }$ Windungen gewickelt ist. Wenn die Primärspule an einen Wechselstromgenerator angeschlossen wird, gilt folgende Beziehung zwischen den Windungszahlen beider Spulen und der Primär- und Sekundärspannung:

$$
V _ {\mathrm{s}} = V _ {\mathrm{p}} \frac {N _ {\mathrm{s}}}{N _ {\mathrm{p}}} \quad \text {(Transformation der Spannungen)}.
$$

• Für die Ströme durch die Spulen gilt entsprechend

$$
I _ {\mathrm{s}} = I _ {\mathrm{p}} \frac {N _ {\mathrm{p}}}{N _ {\mathrm{s}}} \quad \text {(Transformation der Ströme)}.
$$

• Der äquivalente Ersatzwiderstand des Sekundärkreises (aus Sicht des Primärkreises bzw. des Generators) ist

$$
R _ {\mathrm{Ers}} = \left(\frac {N _ {\mathrm{p}}}{N _ {\mathrm{s}}}\right) ^ {2} R,
$$

wobei R der Lastwiderstand am Sekundärkreis ist. Das Verhältnis $N _ { \mathrm { p } } / N _ { \mathrm { s } }$ nennt man das Übersetzungsverhältnis des Transformators.

## 27.6.1 Transformatoren

## Anforderungen an die Energieübertragung

Enthält ein Wechselstromkreis nur einen Wirkwiderstand, so ist der Leistungsfaktor in Gl. 27.66 cos $0 ^ { \circ } = 1$ und die angelegte Wechselspannung $\mathcal { E } _ { \mathrm { e f f } }$ ist gleich dem Effektivwert der Spannung $\mathcal { E } _ { \mathrm { e f f } }$ am Lastwiderstand. Wenn durch den Lastwiderstand ein Strom mit dem Effektivwert $I _ { \mathrm { e f f } }$ fließt, ist die mittlere Leistung

$$
P _ {\mathrm{gem}} = \mathcal {E} I = I V. \tag {27.67}
$$

(In dieser Gleichung und dem Rest dieses Abschnitts folgen wir der gängigen Praxis und lassen die Indizierung $\mathrm { { _ { v } e f f ^ { \omega } } }$ weg. Techniker und Ingenieure sind es gewohnt, alle zeitabhängigen Ströme und Spannungen durch ihre Effektivwerte anzugeben, die auch von den Messgeräten angezeigt werden.) Eine vorgegebene elektrische Leistung lässt sich nach dieser Gleichung auf viele verschiedene Arten realisieren, angefangen bei vergleichsweise großen Strömen I und kleinen Spannungen V bis hin zum umgekehrten Fall kleiner Ströme und großer Spannungen. Die Voraussetzung ist nur, dass das Produkt IV aus Strom und Spannung den erforderlichen Wert hat.

Im Rahmen der öffentlichen Stromversorgung ist es aus Sicherheitsgründen sowie der Möglichkeit einfacherer Konstruktionen wünschenswert, sowohl am Erzeugerende (dem Kraftwerk) als auch am Verbraucherende (den Haushalten oder der Industrie) vergleichsweise niedrige Spannungen zu verwenden. Niemand hätte gerne einen elektrischen Toaster oder eine elektrische Kindereisenbahn im Haus, die bei 10 kV betrieben wird. Andererseits sollte die Übertragung der elektrischen Energie vom Kraftwerk zum Verbraucher bei möglichst niedrigen Strömen (und damit der höchstmöglichen Spannung) erfolgen, damit der Ohmsche Verlust $I ^ { 2 } R$ in den Leitungen möglichst gering bleibt.

Betrachten wir als Beispiel die 735-kV-Hochspannungsleitung vom Wasserkraftwerk La Grande 2 in Quebec nach Montreal, die über eine Entfernung von rund 1000 km führt. Angenommen, der Strom beträgt 500 A und der Leistungsfaktor liegt nahe bei eins. Nach Gl. 27.67 gilt dann für die mittlere übermittelte Leistung

$$
P _ {\mathrm{gem}} = \mathcal {E} I = (7, 3 5 \cdot 1 0 ^ {5} \mathrm{V}) (5 0 0 \mathrm{A}) = 3 6 8 \mathrm{MW}.
$$

Der Wirkwiderstand der Hochspannungsleitungen beträgt rund 0,220 Ω/km. Auf eine Entfernung von 1000 km beträgt der Gesamtwiderstand daher 220 Ω. Aufgrund dieses Widerstands geht im Mittel eine Leistung

$$
P _ {\mathrm{gem}} = I ^ {2} R = (5 0 0 \mathrm{A}) ^ {2} (2 2 0 \Omega) = 5 5, 0 \mathrm{MW}
$$

verloren, was ungefähr 15 % der Gesamtleistung ausmacht.

Angenommen, wir würden nun den Strom verdoppeln und die Spannung halbieren. Am Erzeugerende käme dann immer noch eine Leistung von 368 MW an, aber die Verlustleistung wäre jetzt

$$
P _ {\mathrm{gem}} = I ^ {2} R = (1 0 0 0 \mathrm{A}) ^ {2} (2 2 0 \Omega) = 2 2 0 \mathrm{MW},
$$

was ungefähr 60 % der Gesamtleistung entspricht. Daraus ergibt sich die allgemeine Regel: Für die Übertragung elektrischer Energie über längere Strecken wähle man immer die größtmögliche Spannung und den kleinstmöglichen Strom!

![](images/page_678_image_19.jpg)

<details>
<summary>natural_image</summary>

Silhouette of a modern city skyline at dusk with water reflection, no visible text or symbols
</details>

## Abb. 27.15

Am 9. November 1965 um 5 Uhr 17 morgens wurde in einem Elektrizitätswerk in der Nähe der Niagarafälle durch ein defektes Relais ein Stromkreisunterbrecher der Hochspannungsleitung geöffnet, wodurch der Strom automatisch auf andere Leitungen umgelenkt wurde. Durch die Überlastung dieser Leitungen wurden weitere Stromkreisunterbrecher geöffnet. Innerhalb von Minuten kam es zu einem weiträumigen Stromausfall in großen Teilen New Yorks, New Englands und Ontarios.

![](images/page_679_image_1.jpg)

<details>
<summary>text_image</summary>

ΦB
Vp
Np
Ns
S
R
Primärseite
Sekundärseite
</details>

Abb. 27.16

Ein idealer Transformator (zwei um einen Eisenring gewickelte Spulen) in einem einfachen Transformatorschaltkreis. Der Wechselstromgenerator erzeugt in der linken Spule (der Primärspule) einen Strom. Die rechte Spule (die Sekundärspule) ist bei geschlossenem Schalter S mit einem Wirkwiderstand R verbunden.

## Der ideale Transformator

Die Forderung nach der Verwendung von Hochspannung für die Energieübertragung steht im Widerspruch zu dem Wunsch, dem Endverbraucher aus Sicherheitsgründen nur eine möglichst geringe Spannung zur Verfügung zu stellen. Man benötigt also ein Gerät, mit dem man die Wechselspannung zur Übertragung anheben und zum Gebrauch wieder absenken kann, sodass das Produkt aus Strom und Spannung im Wesentlichen konstant bleibt. Ein solches Gerät ist ein **Transformator**. Er enthält keine beweglichen Teile, sondern arbeitet auf der Grundlage des Faradayschen Induktionsgesetzes; aus diesem Grund existiert kein entsprechendes Gerät für Gleichstrom.

Der ideale Transformator in Abb. 27.16 besteht aus zwei Wicklungen (Spulen) mit unterschiedlichen Windungszahlen um zwei Abschnitte eines ringförmigen Eisenkerns. (Zwischen den Wicklungen und dem Eisenkern befindet sich eine Isolierung.) Die Primärwicklung mit einer Windungszahl $N _ { \mathrm { p } }$ ist mit einem Wechselstromgenerator verbunden, der eine Momentanspannung

$$
\mathcal {E} = \mathcal {E} _ {\mathrm{m}} \sin \omega t \tag {27.68}
$$

liefert. Die Sekundärwicklung mit $N _ { s }$ Windungen ist bei geschlossenem Schalter S mit einem Lastwiderstand R verbunden. Wir gehen zunächst davon aus, dass der Schalter geöffnet und der Stromkreis unterbrochen ist; durch die Sekundärspule fließt also noch kein Strom. Außerdem nehmen wir an, dass die Wirkwiderstände in der Primär- und Sekundärwicklung vernachlässigbar sind, ebenso wie Energieverluste durch magnetische Hystereseeffekte im Eisenkern. Gute Hochleistungstransformatoren haben einen Energieverlust von unter 1 $\% ,$ unsere Annahmen sind also berechtigt.

Unter diesen Bedingungen ist die Primärwicklung eine reine Induktivität und der Primärkreis entspricht dem Stromkreis aus Abb. 27.10a. Der (sehr kleine) Primärstrom, manchmal auch Magnetisierungsstrom $I _ { \mathrm { M a g } }$ genannt, eilt der Primärspannung $V _ { \mathrm { p } }$ um $9 0 ^ { \circ }$ nach. Der Leistungsfaktor des Primärkreises (= cos 𝜑 in Gl. 27.66) ist null, sodass vom Generator keine Leistung auf den Transformator übertragen wird.

Der kleine Primärwechselstrom $I _ { \mathrm { M a g } }$ induziert jedoch in dem Eisenkern einen alternierenden magnetischen Fluss $\phi _ { B } ^ { \phantom { \dagger } } .$ Der Eisenkern bündelt den Fluss und führt ihn durch die Sekundärwicklung, wo er eine Spannung induziert. Nach dem Faradayschen Induktionsgesetz (Gl. 26.6) ist die induzierte Spannung $\mathcal { E } _ { \mathrm { W } }$ pro Windung für die Primär- und die Sekundärwicklung gleich. Außerdem ist die Spannung $V _ { \mathrm { p } }$ an der Primärwicklung gleich der angelegten Wechselspannung und die Spannung $V _ { s }$ in der Sekundärwicklung ist gleich der induzierten Spannung in der Sekundärwicklung. Es gilt daher

$$
\mathcal {E} _ {\mathrm{W}} = \frac {\mathrm{d} \varPhi_ {B}}{\mathrm{d} t} = \frac {V _ {\mathrm{p}}}{N _ {\mathrm{p}}} = \frac {V _ {\mathrm{s}}}{N _ {\mathrm{s}}}
$$

und somit

$$
V _ {\mathrm{s}} = V _ {\mathrm{p}} \frac {N _ {\mathrm{s}}}{N _ {\mathrm{p}}} \quad (\text {Transformation der Spannung}). \tag {27.69}
$$

Für $N _ { \mathrm { s } } > N _ { \mathrm { p } }$ spricht man von einem Aufwärtstransformator, weil die Primärspannung $V _ { \mathrm { p } }$ auf eine höhere Spannung $V _ { s }$ transformiert wird. Entsprechend spricht man für $N _ { \mathrm { s } } < N _ { \mathrm { p } }$ von einem Abwärtstransformator.

Solange der Schalter offen bzw. der Stromkreis unterbrochen ist, wird keine Energie vom Generator auf den Rest des Stromkreises übertragen. Nun schließen wir den Schalter S und verbinden den Sekundärkreis mit der Wirklast R. Im Allge meinen enthält der Sekundärkreis auch induktive und kapazitive Elemente, doch hier betrachten wir nur den Wirkwiderstand R. In diesem Fall wird Energie vom Generator übertragen, was wir nun untersuchen wollen.

Wenn der Schalter S geschlossen wird, passieren mehrere Dinge:

1. Im Sekundärkreis fließt ein Wechselstrom $I _ { s } ,$ wodurch an der Wirklast mit der Leistung $I _ { s } ^ { 2 } R \left( = V _ { s } ^ { 2 } / R \right)$ Energie verbraucht wird.
2. Dieser Strom erzeugt seinen eigenen alternierenden magnetischen Fluss im Ei senkern, der (nach dem Faradayschen Gesetz und der Lenzschen Regel) eine entgegengesetzt gerichtete Spannung in den Primärwicklungen induziert.
3. Die Spannung $V _ { \mathrm { p } }$ im Primärkreis kann sich jedoch aufgrund dieser induzierten Spannung nicht ändern, da sie immer gleich der angelegten Wechselspannung vom Generator sein muss. An dieser Tatsache kann auch die Schließung des zweiten Stromkreises nichts ändern.
4. Zur Aufrechterhaltung der Spannung $V _ { \mathrm { p } }$ erzeugt der Generator einen Wechselstrom $I _ { \mathrm { p } }$ zusätzlich zu $I _ { \mathrm { M a g } }$ im Primärkreis. Der Betrag und die Phasenkonstante von $I _ { \mathrm { p } }$ haben gerade solche Werte, dass die von $I _ { \mathrm { p } }$ im Primärkreis induzierte Spannung die von $I _ { \mathrm { s } }$ induzierte Spannung aufhebt. Da die Phasenkonstante von $I _ { \mathrm { p } }$ im Gegensatz zu der von $I _ { \mathrm { M a g } }$ nicht $9 0 ^ { \circ }$ ist, kann dieser Strom $I _ { \mathrm { p } }$ Energie auf den Primärkreis übertragen.

Wir wollen eine Beziehung zwischen $I _ { s }$ und $I _ { \mathrm { p } }$ finden. Anstatt jedoch den zuvor be schriebenen komplizierten Prozess im Detail zu verfolgen, nutzen wir einfach die Energieerhaltung. Der Generator überträgt Energie mit der Leistung $I _ { \mathrm { p } }   V _ { \mathrm { p } }$ auf den Primärkreis. Der Primärkreis überträgt (über das alternierende Magnetfeld zwischen den beiden Spulen) wiederum Energie mit der Leistung $I _ { s }   V _ { s }$ auf den Sekun därkreis. Da wir einen Verlust an Energie bei diesem Prozess explizit ausschließen wollten, folgt aus der Energieerhaltung

$$
I _ {\mathrm{p}} V _ {\mathrm{p}} = I _ {\mathrm{s}} V _ {\mathrm{s}}.
$$

Wir ersetzen $V _ { s }$ nach Gl. 27.69 und erhalten so

$$
I _ {\mathrm{s}} = I _ {\mathrm{p}} \frac {N _ {\mathrm{p}}}{N _ {\mathrm{s}}} \quad (\text {Transformation des Stroms}). \tag {27.70}
$$

Der Strom $I _ { s }$ auf der Sekundärseite unterscheidet sich also um das Übersetzungsverhältnis $N _ { \mathrm { p } } / N _ { \mathrm { s } }$ von dem Strom $I _ { \mathrm { p } }$ auf der Primärseite.

Der Strom $I _ { \mathrm { p } }$ im Primärkreis beruht auf der Wirklast R auf der Sekundärseite. Um $I _ { \mathrm { p } }$ zu berechnen, setzen wir $I _ { \mathrm { s } } = V _ { \mathrm { s } } / R$ in Gl. 27.70 ein und substituieren $V _ { s }$ aus Gl. 27.69; auf diese Weise erhalten wir

$$
I _ {\mathrm{p}} = \frac {1}{R} \left(\frac {N _ {\mathrm{s}}}{N _ {\mathrm{p}}}\right) ^ {2} V _ {\mathrm{p}}. \tag {27.71}
$$

Diese Gleichung hat die Form $I _ { \mathrm { p } } = V _ { \mathrm { p } } / R ^ { \prime }$ mit

$$
R ^ {\prime} = \left(\frac {N _ {\mathrm{p}}}{N _ {\mathrm{s}}}\right) ^ {2} R. \tag {27.72}
$$

$R ^ { \prime }$ ist ein effektiver Wirkwiderstand (manchmal spricht man auch von einem reduzierten Widerstand), wie er vom Generator auf der Primärseite „gesehen“ wird. Der Generator liefert die Spannung $V _ { \mathrm { p } }$ und erzeugt den Strom $I _ { \mathrm { p } } ,$ als ob er mit einem Wirkwiderstand $R ^ { \prime }$ verbunden wäre.

## Impedanzanpassung

Gleichung 27.72 gibt einen Hinweis auf eine weitere Anwendungsmöglichkeit des Transformators. Damit ein Generator Energie mit optimaler Leistung auf eine Wirklast übertragen kann, müssen der Widerstand im Generator und der Lastwi derstand gleich sein. Eine entsprechende Beziehung existiert auch für Wechselstromkreise, nur dass in diesem Fall die Impedanzen anstelle der Wirkwiderstände zwischen Generator und Belastung gleich sein müssen; man bezeichnet dies als Impedanzanpassung. Diese Bedingung ist oft nicht erfüllt. So hat beispielsweise bei einer Stereoanlage der Verstärker eine hohe Impedanz, während die Lautsprecher eine niedrige Impedanz haben. Die Impedanzen lassen sich jedoch angleichen, indem man sie über einen Transformator mit einem geeignet gewählten Übersetzungsverhältnis $N _ { \mathrm { p } } / N _ { \mathrm { s } }$ koppelt.

## KONTROLLFRAGE 9

Eine Wechselspannungsquelle habe einen kleineren Widerstand als die Wirklast. Zur Erhöhung der Leistungsübertragung vom Generator zum Verbraucher wird zwischen beide Stromkreise ein Transformator geschaltet. (a) Sollte $N _ { s }$ in diesem Fall größer oder kleiner als $N _ { \mathrm { p } }$ sein? (b) Wird der Transformator dadurch zu einem Aufwärts- oder einem Abwärtstransformator?

## 27.7 Zusammenfassung

**Energieübertragung in einem LC-Kreis** In einem oszillierenden LC-Kreis fließt die Energie periodisch zwischen dem elektrischen Feld des Kondensators und dem Magnetfeld der Spule hin und her. Die Momentanwerte der beiden Energieformen sind

$$
U _ {E} = \frac {q ^ {2}}{2 C} \quad \text {und} \quad U _ {B} = \frac {L i ^ {2}}{2}, \tag {27.1,27.2}
$$

wobei $q$ der Momentanwert der Ladung auf dem Kondensator und i der Momentanwert des Stroms durch die Spule sind. Die Gesamtenergie $U = U _ { E } + U _ { B }$ bleibt konstant.

**Ladungs- und Stromschwingungen in einem LC-Kreis** Aus der Energieerhaltung folgt die Differenzialgleichung einer LC-Schwingung (ohne Wirkwiderstand):

$$
L \frac {\mathrm{d} ^ {2} q}{\mathrm{d} t ^ {2}} + \frac {1}{C} q = 0 \quad (L C \text {-Schwingungen}). \tag {27.11}
$$

Die Lösung dieser Gleichung lautet

$$
q (t) = Q \cos (\omega t + \varphi) \quad \text {(Ladung)}, \tag {27.12}
$$

wobei $Q$ die Ladungsamplitude (maximale elektrische Ladung auf dem Kondensator) ist. Für die Kreisfrequenz ω der Schwingung gilt

$$
\omega = \frac {1}{\sqrt {L C}}. \tag {27.14}
$$

Die Phasenkonstante $\varphi$ in Gl. 27.12 folgt aus den Anfangsbedingungen (zum Zeitpunkt $t = 0 )$ des Systems.

Der Momentanwert des Stroms i in diesem Schwingkreis folgt der Gleichung

$$
i (t) = - \omega Q \sin (\omega t + \varphi) \quad \text {(Strom)} \tag {27.13}
$$

mit der Stromamplitude $I = \omega Q$

**Gedämpfte Schwingungen** Die Schwingungen in einem LC-Kreis sind gedämpft, wenn der Stromkreis zusätzlich eine dissipative Komponente R enthält. In diesem Fall lautet die Differenzialgleichung

$$
L \frac {\mathrm{d} ^ {2} q}{\mathrm{d} t ^ {2}} + R \frac {\mathrm{d} q}{\mathrm{d} t} + \frac {1}{C} q = 0 \quad (R L C \text {-Kreis}). \tag {27.20}
$$

Die Lösung dieser Gleichung ist

$$
q (t) = Q \mathrm{e} ^ {- \mathrm{Rt} / (2 L)} \cos (\omega^ {\prime} t + \varphi) \tag {27.21}
$$

mit

$$
\omega^ {\prime} = \sqrt {\omega^ {2} - (R / 2 L) ^ {2}}. \tag {27.22}
$$

Wir betrachten nur den Fall kleiner Wirkwiderstände R und daher geringer Dämpfung. In diesem Fall gilt $\omega ^ { \prime } \approx \omega .$

**Wechselstromkreise; erzwungene Schwingung** Ein Reihen-RLC-Kreis kann durch eine von außen angelegte Wechselspannung

$$
\mathcal {E} = \mathcal {E} _ {\mathrm{m}} \sin \omega_ {\mathrm{a}} t \tag {27.24}
$$

zu einer erzwungenen Schwingung mit einer antreibenden Kreisfrequenz $\omega _ { \mathrm { a } }$ angeregt werden. Der durch die Quellenspannung erzeugte Strom ist

$$
i (t) = I \sin (\omega_ {\mathrm{a}} t - \varphi), \tag {27.25}
$$

wobei $\varphi$ die Phasenkonstante des Stroms bezeichnet.

**Resonanz** Die Stromamplitude I eines Reihen-RLC-Kreises, der durch eine sinusförmige Quellenspannung angetrieben wird, erreicht ihren Maximalwert, wenn die antreibende Kreisfrequenz $\omega _ { \mathrm { a } }$ gleich der natürlichen Kreisfrequenz des Stromkreises ist (Resonanzfall). In diesem Fall sind $X _ { C } = X _ { L }$ und $\varphi = 0 ;$ Strom und Quellenspannung sind also in Phase.

**Die einzelnen Komponenten des Stromkreises** Eine Wechselspannung an einem Wirkwiderstand hat die Amplitude $V _ { R } = I R .$ Strom und Potenzial sind in Phase.

Für eine Kapazität gilt $V _ { C } = I X _ { C } ,$ wobei $X _ { C } = 1 / ( \omega _ { \mathrm { a } } C )$ der **kapazitive Widerstand** ist. Der Strom eilt der Spannung um 90° voraus $\left( \varphi = - 9 0 ^ { \circ } = - \pi / 2   \mathrm { r a d } \right)$

Für eine Induktivität gilt $V _ { L } = I X _ { L }$ , wobei $X _ { L } = \omega _ { \mathrm { a } } L$ der **induktive Widerstand** ist. Der Strom eilt der Spannung um $9 0 ^ { \circ }$ nach $\left( \varphi = + 9 0 ^ { \circ } = + \pi / 2   \mathrm { r a d } \right)$

**Reihen-RLC-Kreise** Für eine Reihen-RLC-Schaltung mit einer angelegten Wechselspannung gemäß Gl. 27.24 und einem Strom gemäß Gl. 27.25 gilt

$$
\begin{array}{l} I = \frac {\mathcal {E} _ {\mathrm{m}}}{\sqrt {R ^ {2} + (X _ {L} - X _ {C}) ^ {2}}} \\ = \frac {\mathcal {E} _ {\mathrm{m}}}{\sqrt {R ^ {2} + \left(\omega_ {\mathrm{a}} L - 1 / \left(\omega_ {\mathrm{a}} C\right)\right) ^ {2}}} \quad \text {(Stromamplitude)} \tag {27.50, 27.53} \\ \end{array}
$$

und

$$
\tan \varphi = \frac {X _ {L} - X _ {C}}{R} \quad (\text {Phasenkonstante}). \tag {27.55}
$$

Die Impedanz Z eines Wechselstromkreises ist durch

$$
Z = \sqrt {R ^ {2} + (X _ {L} - X _ {C}) ^ {2}} \qquad (\text {Impedanz}) \tag {27.51}
$$

definiert. Damit lässt sich Gl. 27.50 in der Form $I = \mathcal { E } _ { \mathrm { m } } / Z$ schreiben.

**Leistung** In einer RLC-Reihenschaltung ist die **mittlere Leistung** $P _ { \mathrm { g e m } }$ des Generators gleich der Erzeugungsrate von Wärmeenergie im Wirkwiderstand:

$$
P _ {\mathrm{gem}} = I _ {\mathrm{eff}} ^ {2} R = \mathcal {E} _ {\mathrm{eff}} I _ {\mathrm{eff}} \cos \varphi . \tag {27.61,27.66}
$$

## 27.8 Fragen

**1.** Ein geladener Kondensator und eine Spule werden zum Zeitpunkt t = 0 miteinander verbunden. Zu welchem Zeitpunkt (ausgedrückt durch die Periode T der resultierenden Schwingungen) erreichen die folgenden Größen ihren Maximalwert: (a) $U _ { B } ,$ (b) der magnetische Fluss durch die Spule, (c) $\mathrm { d } i / \mathrm { d } t$ und (d) die Spannung an der Spule?
**2.** Für welche Werte der Phasenkonstante 𝜑 in Gl. 27.12 erhält man zur Zeit $t = 0$ die Situationen (a), (c), (e) bzw. (g) aus Abb. 27.1?
**3.** Abbildung 27.F3 zeigt drei LC-Kreise mit identischen Spulen und Kondensatoren. Ordnen Sie die Schwingkreise in absteigender Reihenfolge nach der Zeit, die die Kondensatoren während der Schwingungszyklen zur vollständigen Entladung benötigen.

![](images/page_682_image_17.jpg)

Abb. 27.F3

Der Index $\mathrm { _ { v } e f f ^ { \omega } }$ steht für Effektivwert. Die Effektivwerte hängen mit den Amplituden über die Beziehungen $I _ { \mathrm { e f f } } = I / \sqrt { 2 } ,   \mathcal { E } _ { \mathrm { e f f } } = V / \sqrt { 2 }$ und $\mathcal { E } _ { \mathrm { e f f } } = \mathcal { E } _ { \mathrm { m } } / \sqrt { 2 }$ zusammen. Den Term cos 𝜑 bezeichnet man als **Leistungsfaktor** des Stromkreises.

**Transformatoren** Ein (idealer) Transformator besteht aus einem ringförmigen Eisenkern, um den eine Primärspule mit $N _ { \mathrm { p } }$ Windungen und eine Sekundärspule mit $N _ { s }$ Windungen gewickelt sind. Die Primärspule ist mit einem Wechselstromgenerator verbunden. Primär- und Sekundärspannung hängen gemäß

$$
V _ {\mathrm{s}} = V _ {\mathrm{p}} \frac {N _ {\mathrm{s}}}{N _ {\mathrm{p}}} \quad \text {(Transformation der Spannung)} \tag {27.69}
$$

zusammen. Für die Ströme in den Spulen gilt

$$
I _ {\mathrm{s}} = I _ {\mathrm{p}} \frac {N _ {\mathrm{p}}}{N _ {\mathrm{s}}} \quad (\text {Transformation des Stroms}). \tag {27.70}
$$

Der Wirkwiderstand R auf der Sekundärseite wird vom Generator effektiv als

$$
R ^ {\prime} = \left(\frac {N _ {\mathrm{p}}}{N _ {\mathrm{s}}}\right) ^ {2} R \tag {27.72}
$$

wahrgenommen. Das Verhältnis $N _ { \mathrm { p } } / N _ { \mathrm { s } }$ bezeichnet man als das Übersetzungsverhältnis des Transformators.

**4.** Abbildung 27.F4 zeigt den Verlauf der Kondensatorspannung in zwei LC-Kreisen 1 und 2 mit zwei identischen Kondensatoren und derselben maximalen Ladung Q. Sind (a) die Induktivität L und (b) der Scheitelwert des Stroms I in Stromkreis 1 größer oder kleiner als in Stromkreis 2, oder sind sie gleich?

![](images/page_682_chart_28.jpg)

<details>
<summary>line</summary>

| t | vC (Curve 1) | vC (Curve 2) |
| --- | --- | --- |
| 0 | ~0.5 | ~-1.5 |
| 1 | ~1.5 | ~-0.5 |
| 2 | ~0.5 | ~1.5 |
| 3 | ~-1.5 | ~0.5 |
| 4 | ~-1.5 | ~-1.5 |
| 5 | ~0.5 | ~-0.5 |
| 6 | ~1.5 | ~0.5 |
| 7 | ~0.5 | ~1.5 |
| 8 | ~-1.5 | ~0.5 |
| 9 | ~-1.5 | ~-1.5 |
| 10 | ~0.5 | ~-0.5 |
| 11 | ~1.5 | ~0.5 |
| 12 | ~0.5 | ~1.5 |
| 13 | ~-1.5 | ~0.5 |
| 14 | ~-1.5 | ~-1.5 |
| 15 | ~0.5 | ~-0.5 |
| 16 | ~1.5 | ~0.5 |
| 17 | ~0.5 | ~1.5 |
| 18 | ~-1.5 | ~0.5 |
| 19 | ~-1.5 | ~-1.5 |
| 20 | ~0.5 | ~-0.5 |
| 21 | ~1.5 | ~0.5 |
| 22 | ~0.5 | ~1.5 |
| 23 | ~-1.5 | ~0.5 |
| 24 | ~-1.5 | ~-1.5 |
| 25 | ~0.5 | ~-0.5 |
| 26 | ~1.5 | ~0.5 |
| 27 | ~0.5 | ~1.5 |
| 28 | ~-1.5 | ~0.5 |
| 29 | ~-1.5 | ~-1.5 |
| 30 | ~0.5 | ~-0.5 |
| 31 | ~1.5 | ~0.5 |
| 32 | ~0.5 | ~1.5 |
| 33 | ~-1.5 | ~0.5 |
| 34 | ~-1.5 | ~-1.5 |
| 35 | ~0.5 | ~-0.5 |
| 36 | ~1.5 | ~0.5 |
| 37 | ~0.5 | ~1.5 |
| 38 | ~-1.5 | ~0.5 |
| 39 | ~-1.5 | ~-1.5 |
| 40 | ~0.5 | ~-0.5 |
| 41 | ~1.5 | ~0.5 |
| 42 | ~0.5 | ~1.5 |
| 43 | ~-1.5 | ~0.5 |
| 44 | ~-1.5 | ~-1.5 |
| 45 | ~0.5 | ~-0.5 |
| 46 | ~1.5 | ~0.5 |
| 47 | ~0.5 | ~1.5 |
| 48 | ~-1.5 | ~0.5 |
| 49 | ~-1.5 | ~-1.5 |
| 50 | ~0.5 | ~-0.5 |
| 51 | ~1.5 | ~0.5 |
| 52 | ~0.5 | ~1.5 |
| 53 | ~-1.5 | ~0.5 |
| 54 | ~-1.5 | ~-1.5 |
| 55 | ~0.5 | ~-0.5 |
| 56 | ~1.5 | ~0.5 |
| 57 | ~0.5 | ~1.5 |
| 58 | ~-1.5 | ~0.5 |
| 59 | ~-1.5 | ~-1.5 |
| 60 | ~0.5 | ~-0.5 |
| 61 | ~1.5 | ~0.5 |
| 62 | ~0.5 | ~1.5 |
| 63 | ~-1.5 | ~0.5 |
| 64 | ~-1.5 | ~-1.5 |
| 65 | ~0.5 | ~-0.5 |
| 66 | ~1.5 | ~0.5 |
| 67 | ~0.5 | ~1.5 |
| 68 | ~-1.5 | ~0.5 |
| 69 | ~-1.5 | ~-1.5 |
| 70 | ~0.5 | ~-0.5 |
| 71 | ~1.5 | ~0.5 |
| 72 | ~0.5 | ~1.5 |
| 73 | ~-1.5 | ~0.5 |
| 74 | ~-1.5 | ~-1.5 |
| 75 | ~0.5 | ~-0.5 |
| 76 | ~1.5 | ~0.5 |
| 77 | ~0.5 | ~1.5 |
| 78 | ~-1.5 | ~0.5 |
| 79 | ~-1.5 | ~-1.5 |
| 80 | ~0.5 | ~-0.5 |
| 81 | ~1.5 | ~0.5 |
| 82 | ~0.5 | ~1.5 |
| 83 | ~-1.5 | ~0.5 |
| 84 | ~-1.5 | ~-1.5 |
| 85 | ~0.5 | ~-0.5 |
| 86 | ~1.5 | ~0.5 |
| 87 | ~0.5 | ~1.5 |
| 88 | ~-1.5 | ~0.5 |
| 89 | ~-1.5 | ~-1.5 |
| 90 | ~0.5 | ~-0.5 |
| 91 | ~1.5 | ~0.5 |
| 92 | ~0.5 | ~1.5 |
| 93 | ~-1.5 | ~0.5 |
| 94 | ~-1.5 | ~-1.5 |
| 95 | ~0.5 | ~-0.5 |
| 96 | ~1.5 | ~0.5 |
| 97 | ~0.5 | ~1.5 |
| 98 | ~-1.5 | ~0.5 |
| 99 | ~-1.5 | ~-1.5 |
| 100 | — | — |

Note: The label 'vc' is positioned above the y-axis at the top left.
</details>

Abb. 27.F4

**5.** Die Ladungen auf den Kapazitäten in zwei LC-Schwingkreisen variieren folgendermaßen mit der Zeit: (1) $q =$ 2 cos 4t, (2) $q = 4$ cos t, (3) $q = 3$ cos 4t (q in Coulomb und t in Sekunden). Ordnen Sie die Stromkreise in absteigender Reihenfolge nach (a) der Stromamplitude und (b) der Periode.

**6.** Angenommen, Sie erhöhen in einem LC-Schwingkreis mit einer gegebenen maximalen Ladung Q die Induktivität. Wie verhalten sich (a) die Stromamplitude und (b) die

maximale magnetische Energie $U _ { B } ;$ bleiben sie gleich, nehmen sie zu oder nehmen sie ab?
**7.** Eine Wechselspannung mit einer bestimmten Spannungsamplitude werde nacheinander an einen Wirkwiderstand, einen Kondensator und eine Spule angeschlossen. In allen drei Fällen wird anschließend die Wechselspannungsfrequenz $f _ { \mathrm { a } }$ verändert und die Amplitude I des Stroms in dem Schaltkreis gemessen und gegen die Frequenz aufgetragen. Welche der drei Kurven in Abb. 27.F7 entspricht welchem Schaltkreis?

![](images/page_683_chart_4.jpg)

<details>
<summary>line</summary>

| Category | Value |
| --- | --- |
| I (constant) | b |
| Curve a | Starts at high value, decreases rapidly, approaches zero as fa increases |
| Curve b | Constant value across the range of fa |
| Curve c | Increases linearly from zero to higher values as fa increases |
</details>

Abb. 27.F7

**8.** Die Werte der Phasenkonstante in vier RLC-Kreisen mit einer antreibenden sinusförmigen Wechselspannung sind (1) −15°, (2) +35°, (3) $\pi / 3$ rad und (4) −π∕6 rad. (a) Für welchen Fall ist die Belastung überwiegend kapazitiv? (b) In welchem Fall eilt der Strom der Wechselspannung nach?
**9.** Abbildung 27.F9 zeigt den Strom i und die angelegte Spannung  eines in Reihe geschalteten RLC-Kreises. (a) Eilt der Strom der Spannung voraus oder nach? (b) Ist die Belastung überwiegend kapazitiv oder induktiv? (c) Ist die Kreisfrequenz $\omega _ { \mathrm { a } }$ der angelegten Spannung größer oder kleiner als die natürliche Kreisfrequenz ω?

![](images/page_683_chart_9.jpg)

<details>
<summary>line</summary>

| Category | i | E |
| --- | --- | --- |
| Peak | ~0.8 | ~1.0 |
| Trough | ~-0.8 | ~-0.8 |
</details>

Abb. 27.F9

Fragen 9 und 11.

**10.** Die drei Zeigerdiagramme in Abb. 27.F10 entsprechen ähnlichen Situationen wie in Abb. 27.12. Ist die Kreisfrequenz der angelegten Spannung in den einzelnen Fällen größer als die Resonanzkreisfrequenz des Schaltkreises, ist sie kleiner oder ist sie gleich?

![](images/page_683_image_13.jpg)

![](images/page_683_image_14.jpg)

![](images/page_683_image_15.jpg)

Abb. 27.F10

**11.** Abbildung 27.F9 zeigt den Strom i und die angelegte Spannung  eines Reihen-RLC-Kreises. Wie verhält sich die Kurve für den Strom relativ zu der Kurve für die angelegte Spannung, wenn wir (a) L, (b) C und (c) $\omega _ { \mathrm { a } }$ etwas erhöhen? Verschiebt sich die Kurve nach links oder rechts? Wird die Amplitude größer oder kleiner?
**12.** Abbildung 27.F12 zeigt den Strom i und die angelegte Spannung  einer Reihen-RLC-Schaltung. (a) Ist die Phasenkonstante positiv oder negativ? (b) Muss L größer oder kleiner werden, wenn die Leistung am Wirkwiderstand zunehmen soll? (c) Sollte für den gleichen Fall C zu- oder abnehmen?

![](images/page_683_chart_20.jpg)

<details>
<summary>line</summary>

| t | E | i |
| --- | --- | --- |
| 0 | ~-1.5 | ~-0.8 |
| 1 | ~0.5 | ~-0.2 |
| 2 | ~1.8 | ~0.3 |
| 3 | ~0.5 | ~0.8 |
| 4 | ~-1.2 | ~0.5 |
| 5 | ~-1.8 | ~-0.2 |
| 6 | ~-0.5 | ~-0.8 |
| 7 | ~1.2 | ~-0.5 |
| 8 | ~2.5 | ~0.2 |
</details>

Abb. 27.F12

**13.** Kurve a in Abb. 27.F13 zeigt die Impedanz Z eines angetriebenen RC-Stromkreises in Abhängigkeit von der antreibenden Kreisfrequenz $\omega _ { \mathrm { a } } .$ Die anderen beiden Kurven sind ähnlich, aber für andere Werte von Widerstand R und Kapazität C. Ordnen Sie die drei Kurven in absteigender Reihenfolge nach dem jeweiligen Wert von R.

![](images/page_683_chart_23.jpg)

<details>
<summary>line</summary>

| \(\omega d\) | Curve a (Z) | Curve b (Z) | Curve c (Z) |
| --- | --- | --- | --- |
| Low | High | High | High |
| Medium | Low | Medium | Medium |
| High | Low | Low | Low |
</details>

Abb. 27.F13

**14.** (a) Entspricht das Zeigerdiagramm in Abb. 27.F14 einer Wechselspannungsquelle, die mit einem Widerstand, einem Kondensator oder einer Induktivität verbunden ist? (b) Wird die Länge des Stromzeigers größer oder kleiner, wenn die Winkelgeschwindigkeit des Zeigers zunimmt (die Diagrammskala bleibt gleich)?

![](images/page_683_image_26.jpg)

Abb. 27.F14

# 28 Magnetismus und Materie

## 28.1 Der Gaußsche Satz für Magnetfelder

## Physikalische Motivation

Dieses Kapitel zeigt, wie breit die Physik aufgestellt ist: Es reicht von den physikalischen Grundlagen der elektrischen und magnetischen Felder bis zu ganz praktischen Anwendungen von magnetischen Materialien. Zuerst schließen wir die grundlegende Diskussion der elektrischen und magnetischen Felder ab – als krö nenden Höhepunkt besprechen wir die vier fundamentalen Maxwellschen Gleichungen, die den überwiegenden Teil der letzten elf Kapitel dieses Buchs auf den Punkt bringen.

Danach diskutieren wir Wissenschaft und Technik von magnetischen Materialien. Viele Wissenschaftler und Ingenieure verbringen ihr Berufsleben damit, deren Natur zu entschlüsseln und neue nützliche Anwendungen zu finden. Sie fragen sich, warum Erde und Sonne ein magnetisches Feld haben, sie (und Sie!) dagegen nicht. Es gibt zahllose Anwendungen preiswerter magnetischer Werkstoffe in Autos, Küchen, Büros oder Krankenhäusern, und oft tauchen magnetische Materialien auch dort auf, wo man kaum mit ihnen rechnen würde. Sollten Sie beispielsweise ein Tattoo tragen und eine MRT-Untersuchung (Magnetresonanz-Tomografie) über sich ergehen lassen müssen, werden Sie vielleicht feststellen, dass die dort eingesetzten starken Magnetfelder merklich an Ihrer Haut ruckeln, da die für Tä- towierungen verwendete Tinte manchmal magnetische Teilchen enthält. Ein anderes Beispiel sind Frühstücksflocken, die als „mit Eisen angereichert“ beworben werden – sie enthalten tatsächlich kleine Eisenkügelchen und lassen sich mit einem Haushaltsmagneten aus der Frühstücksschüssel herausfischen!

## 28.1.1 Der Gaußsche Satz für Magnetfelder

Die magnetischen Eigenschaften eines Materials entstehen in seinen Atomen und Elektronen. Wir wollen aber zunächst von der makroskopischen Ebene ausgehen und beginnen daher mit dem Stabmagneten in Abb. 28.1. Wir hatten bereits gesehen, dass sich Eisenfeilspäne entlang der Magnetfeldlinien anordnen und uns so zeigen, wie die Feldlinien verlaufen. Das Zusammenlaufen der Linien an den Enden des Magneten zeigt, dass das eine Ende eine Quelle der Feldlinien ist (hier entspringt das Feld) und das andere eine Senke der Feldlinien (hier verschwindet das Feld). Die Quelle nennen wir den Nordpol des Magneten und das entgegengesetzte Ende (die Senke) den Südpol. Der Magnet mit seinen beiden Polen ist ein Beispiel für einen magnetischen Dipol.

Angenommen, wir brechen einen Stabmagneten auseinander wie ein Stück Kreide (Abb. 28.2). Man sollte meinen, dass wir auf diese Weise (wenn wir es geschickt anstellen) einen isolierten Pol erhalten sollten, einen Monopol. Das gelingt jedoch nicht – selbst wenn wir den Magneten bis in seine einzelnen Atome und sogar in die Atomkerne und Elektronen zerlegen könnten. Stets besteht jedes Bruchstück aus einem Nord- und einem Südpol. Wir schließen daraus:

![](images/page_684_image_8.jpg)

![](images/page_684_image_9.jpg)

<details>
<summary>natural_image</summary>

Illustration of magnetic field lines around a vertical bar labeled 'S', with no text or symbols present.
</details>

Abb. 28.1 Ein Stabmagnet ist ein magnetischer Dipol. Eisenfeilspäne zeigen hier den Verlauf der magnetischen Feldlinien [Quelle: Richard Megna/Fundamental Photographs].

![](images/page_685_image_1.jpg)

<details>
<summary>text_image</summary>

N
S
N
S
N
S
</details>

Abb. 28.2

Wenn wir einen Magneten zerbrechen, ist jedes Bruchstück selbst wieder ein vollständiger Magnet mit Nord- und Südpol.

![](images/page_685_image_4.jpg)

<details>
<summary>text_image</summary>

Fläche II
N
Fläche I
S
B
</details>

Abb. 28.3

Die Feldlinien für das Magnetfeld B⃗ eines kurzen Stabmagneten. Die roten Linien zeigen Schnitte durch geschlossene, dreidimensionale Gaußsche Oberflächen.

![](images/page_685_image_7.jpg)

Das einfachste magnetische System ist ein magnetischer Dipol. Magnetische Monopole existieren nicht (nach heutigem Wissensstand).

Der Gaußsche Satz ist nichts weiter als eine formale Fassung der Feststellung, dass keine magnetischen Monopole existieren. Er besagt, dass der gesamte magnetische Fluss durch eine geschlossene Gaußsche Fläche verschwindet:

$$
\varPhi_ {B} = \oint \vec {B} \cdot \mathrm{d} \vec {A} = 0. \tag {28.1}
$$

Zum Vergleich betrachten wir noch einmal den Gaußschen Satz für elektrische Felder (Abschn. 28.2):

$$
\varPhi_ {E} = \oint \vec {E} \cdot \mathrm{d} \vec {A} = \frac {q _ {\text {innen}}}{\varepsilon_ {0}}.
$$

In beiden Fällen wird über eine geschlossene Gaußsche Oberfläche integriert. Der Gaußsche Satz für elektrische Felder besagt, dass dieses Integral (der gesamte Fluss des elektrischen Felds durch die Oberfläche) proportional zur Gesamtladung $q _ { \mathrm { i n n e n } }$ ist, die von der Oberfläche umschlossen wird. Der Gaußsche Satz für Magnetfelder besagt, dass der Fluss des Magnetfelds durch eine solche Oberfläche verschwindet, da es keine „magnetischen Ladungen“ (keine magnetischen Monopole) gibt, die von der Oberfläche umschlossen werden könnten. Die einfachste magnetische Struktur, die existiert und folglich von einer Oberfläche eingeschlossen werden kann, sind magnetische Dipole, die aus einer Quelle und einer Senke des magnetischen Felds bestehen. Der Fluss des Magnetfelds in die Oberfläche hinein muss deshalb immer genau gleich groß sein wie der Fluss aus ihr heraus, also muss der Gesamtfluss stets null sein.

Der Gaußsche Satz für Magnetfelder gilt auch für kompliziertere Systeme als magnetische Dipole und er gilt sogar dann, wenn die Oberfläche nicht das gesamte System umgibt. Die Gaußsche Fläche II in der Nähe des Stabmagneten in Abb. 28.3 umschließt keine Pole, sodass wir sofort sagen können, dass der Gesamtfluss des magnetischen Felds durch sie null sein muss. Die Oberfläche I macht da mehr Schwierigkeiten. Es sieht so aus, als ob sie nur den Nordpol des Magneten umschlösse, da sie zwar dessen Bezeichnung $_ { p } \mathrm { N } ^ { \alpha }$ enthält, nicht aber die Bezeichnung ${ } _ { p } S ^ { \alpha }$ des Südpols. Aber mit der unteren Begrenzung dieser Fläche muss ein magnetischer Südpol verbunden sein, da hier die Feldlinien in die Oberfläche eintreten. (Der eingeschlossene Teil des Magneten entspricht einem der Bruchstücke des Stabmagneten aus Abb. 28.2.) Auch Oberfläche I umschließt somit einen magnetischen Dipol und der Gesamtfluss des Magnetfelds durch sie ist null.

## KONTROLLFRAGE 1

Die Abbildung zeigt vier geschlossene Oberflächen mit flachen oberen und unte ren Abschlüssen und gekrümmten Seiten. Die Tabelle zeigt die Flächeninhalte $A _ { \mathrm { o } }$ und $A _ { \mathfrak { u } }$ der oberen bzw. unteren Abschlüsse sowie die Feldstärken $B _ { \mathrm { o } }$ und $B _ { \mathrm { u } }$ der homogenen und senkrechten Magnetfelder durch sie in willkürlichen, aber konsistenten Einheiten. Ordnen Sie die Oberflächen in absteigender Reihenfolge nach dem magnetischen Fluss durch ihre gekrümmten Seiten.

| Oberfläche | $A_{o}$ | $B_{o}$ | $A_{u}$ | $B_{u}$ |
| --- | --- | --- | --- | --- |
| a | 2 | 6, nach außen | 4 | 3, nach innen |
| b | 2 | 1, nach innen | 4 | 2, nach innen |
| c | 2 | 6, nach innen | 2 | 8, nach außen |
| d | 2 | 3, nach außen | 3 | 2, nach außen |

![](images/page_685_image_18.jpg)

(a)

![](images/page_685_image_20.jpg)

(b)

![](images/page_685_image_22.jpg)

(c)

![](images/page_685_image_24.jpg)

(d)

## 28.2 Induzierte magnetische Felder

## Lernziele

Nach dem Durcharbeiten dieses Abschnitts sollten Sie in der Lage sein, . . .

• zu verstehen, dass ein veränderlicher elektrischer Fluss ein magnetisches Feld induziert,
• das Maxwellsche Induktionsgesetz anzuwenden, um aus der Änderungsgeschwindigkeit des elektrischen Flusses durch eine geschlossene Schleife das um diese induzierte Magnetfeld zu bestimmen,
• die Feldlinien des induzierten magnetischen Felds innerhalb eines Kondensators mit parallelen kreisförmigen Platten zu skizzieren, der gerade geladen wird, und die Richtung der elektrischen und magnetischen Feldvektoren anzugeben,
• das Ampère-Maxwellsche Gesetz auf den allgemeinen Fall induzierter magnetischer Felder anzuwenden.

## Schlüsselideen

• Ein veränderlicher elektrischer Fluss induziert ein magnetisches Feld:

$$
\oint \vec {B} \cdot \mathrm{d} \vec {s} = \mu_ {0} \varepsilon_ {0} \frac {\mathrm{d} \varPhi_ {E}}{\mathrm{d} t} \quad (\text {Maxwellsches Induktionsgesetz}).
$$

Diese Beziehung gibt den Zusammenhang zwischen der zeitlichen Ableitung des elektrischen Flusses $\Phi _ { E }$ durch eine geschlossene Schleife und dem um sie induzierten magnetischen Feld an.

• Das Ampèresche Gesetz $\oint \vec { B } \cdot \mathrm { d } \vec { s } = \mu _ { 0 } i _ { \mathrm { u m } }$ beschreibt das Magnetfeld aufgrund des von einer geschlossenen Schleife umschlossenen Stroms $i _ { \mathrm { u m } }$ . Beide Gesetze lassen sich zu einer einzigen Gleichung kombinieren:

$$
\oint \vec {B} \cdot \mathrm{d} \vec {s} = \mu_ {0} \varepsilon_ {0} \frac {\mathrm{d} \varPhi_ {E}}{\mathrm{d} t} + \mu_ {0} i _ {\mathrm{um}} \quad (\text {Ampère - Maxwellsches Gesetz}).
$$

## 28.2.1 Induzierte magnetische Felder

In Kapitel 26 hatten wir gesehen, dass ein veränderlicher magnetischer Fluss ein elektrisches Feld induziert, und hatten das Faradaysche Induktionsgesetz in der Form

$$
\oint \vec {E} \cdot \mathrm{d} \vec {s} = - \frac {\mathrm{d} \varPhi_ {B}}{\mathrm{d} t} \tag {28.2}
$$

erhalten. Dabei ist $\vec { E }$ das elektrische Feld, das entlang einer geschlossenen Schleife durch den sich ändernden magnetischen Fluss $\varPhi _ { B }$ im Inneren dieser Schleife induziert wird. Da Symmetrieargumente in der Physik häufig sehr nützlich sind, könnten wir nun fragen, ob die Induktion auch in umgekehrter Richtung erfolgen kann, d. h., ob ein sich ändernder elektrischer Fluss vielleicht auch ein Magnetfeld induzieren kann.

Die Antwort auf diese Frage ist ja. Auch die Gleichung, die diese Induktion beschreibt, ist nahezu symmetrisch zu Gl. 28.2. Sie wird oft (nach James Clerk Maxwell) als Maxwellsches Induktionsgesetz bezeichnet:

$$
\oint \vec {B} \cdot \mathrm{d} \vec {s} = \mu_ {0} \varepsilon_ {0} \frac {\mathrm{d} \varPhi_ {E}}{\mathrm{d} t}. \tag {28.3}
$$

Hier ist $\vec { B }$ das Magnetfeld, das entlang einer geschlossenen Schleife durch den sich ändernden elektrischen Fluss $\Phi _ { E }$ im Inneren dieser Schleife induziert wird.

Als Beispiel für diese Art der Induktion betrachten wir das Laden eines Plattenkondensators mit kreisförmigen Platten (Abb. 28.4a). (Obwohl wir uns aus

![](images/page_686_image_24.jpg)

![](images/page_686_image_25.jpg)

![](images/page_686_image_26.jpg)

<details>
<summary>text_image</summary>

+ E -
+ - 1
+ - -
+ - -
+ - -
+ - -
+ - -
+ - -
+ - -
+ - -
+ - -
+ - -
+ - -
+ - -
+ - -
+ - -
+ - -
+ - -
+ - -
+ - -
+ - -
+ - -
+ - -
+ - -
+ - -
+ - -
+ - -
+ - -
+ - -
+ - -
+ - -
+ - -
+ - -
+ - -
+ - -
+ - -
i → i →
</details>

(a)

![](images/page_686_image_28.jpg)

<details>
<summary>text_image</summary>

2
1
B
E
r
R
B
B
</details>

(b)

## Abb. 28.4

(a) Ein zylindrischer Plattenkondensator beim Laden mit einem konstanten Strom i von der Seite. (b) Blick aus dem Innenraum des Kondensators auf die rechte Platte. Das elektrische Feld E⃗ ist homogen, zeigt in die Seite (auf die Platte zu) und die Feldstärke steigt während des Ladevorgangs an. Das durch dieses veränderliche elektrische Feld induzierte Magnetfeld B⃗ ist an vier Punkten auf einem Kreis mit Radius r gezeigt (r kleiner als der Plattenradius R).

![](images/page_687_image_1.jpg)

<details>
<summary>text_image</summary>

R
r
E
B
E
B
E
</details>

Abb. 28.5

Ein homogenes Magnetfeld B⃗ in einem kreisförmigen Raumbereich. Das Feld zeigt in die Seite hinein und nimmt zu. Das von diesem Magnetfeld induzierte elektrische Feld $\vec { E }$ ist an vier Punkten auf einem Kreis eingezeichnet.

praktischen Gründen auf diese Anordnung konzentrieren werden, induziert ein veränderlicher elektrischer Fluss natürlich immer ein Magnetfeld, egal in welcher Anordnung.) Wir nehmen an, dass die Ladung auf den Platten durch einen kon stanten Strom i in den Zuleitungen stetig steigt, wodurch auch die Feldstärke des elektrischen Felds zwischen den Platten stetig zunimmt.

Abbildung 28.4b zeigt den Blick aus dem Innenraum des Kondensators auf die rechte Platte aus Abb. 28.4a; das elektrische Feld zeigt hier in die Seite hinein. Wir betrachten jetzt eine kreisförmige Schleife durch Punkt 1 in Abb. 28.4a und $^ \mathrm { b , }$ die kleiner ist als die Platten und konzentrisch zu ihnen. Da das elektrische Feld durch die Schleife sich ändert, muss sich auch der elektrische Fluss durch sie ändern. Nach Gl. 28.3 induziert dieser veränderliche elektrische Fluss ein Magnetfeld um die Schleife.

Experimente zeigen, dass tatsächlich ein Magnetfeld $\vec { B }$ in der eingezeichneten Richtung um eine solche Schleife induziert wird. Das induzierte Feld hat an allen Punkten um die Schleife dieselbe Feldstärke, ist also rotationssymmetrisch um die zentrale Achse des Kondensators.

Nun betrachten wir eine weitere, größere kreisförmige Schleife, z. B. durch Punkt 2 in Abb. 28.4a und b. Auch um diese Schleife wird ein Magnetfeld induziert. Solange das elektrische Feld sich ändert, wird also sowohl innerhalb der Platten als auch außerhalb ein magnetisches Feld zwischen den Platten induziert. Sobald das elektrische Feld sich nicht mehr ändert, verschwindet das induzierte Magnetfeld.

Obwohl die Gln. 28.3 und 28.2 einander sehr ähneln, unterscheiden sie sich in zwei Punkten. Erstens tauchen in Gl. 28.3 die beiden zusätzlichen Größen $\mu _ { 0 }$ und $\varepsilon _ { 0 }$ auf, die jedoch nur damit zusammenhängen, dass wir in den Gleichungen das SI-System benutzen. Zweitens fehlt in Gl. 28.3 das Minuszeichen aus Gl. 28.2. Das bedeutet, dass das induzierte elektrische Feld $\vec { E }$ und das induzierte Magnetfeld $\vec { B }$ in entgegengesetzte Richtungen zeigen, wenn sie auf ansonsten sehr ähnliche Weise erzeugt werden. Um diesen Unterschied zu erkennen, betrachten wir Abb. 28.5, in der ein zunehmendes, in die Seite gerichtetes Magnetfeld $\vec { B }$ ein elektrisches Feld $\vec { E }$ induziert. Das induzierte Feld $\vec { E }$ ist im Gegenuhrzeigersinn gerichtet, entgegen dem induzierten Magnetfeld $\vec { B }$ aus Abb. 28.4b.

## Das Ampère-Maxwellsche Gesetz

Wir erinnern uns, dass die linke Seite aus Gl. 28.3, das Integral über das Skalarprodukt $\vec { B }$ ⋅ d⃗s über eine geschlossene Schleife, auch in einer anderen Gleichung auftritt – dem Ampèreschen Gesetz:

$$
\oint \vec {B} \cdot \mathrm{d} \vec {s} = \mu_ {0} i _ {\mathrm{um}}. \tag {28.4}
$$

Hier ist $i _ { \mathrm { u m } }$ der von der Schleife umschlossenen Strom. Beide Gleichungen beschreiben ein induziertes Magnetfeld (das einmal durch einen Strom erzeugt wird und einmal durch ein veränderliches elektrisches Feld) und haben genau dieselbe Form. Wir können die Gleichungen daher zum Ampère-Maxwellschen Gesetz kombinieren:

$$
\oint \vec {B} \cdot \mathrm{d} \vec {s} = \mu_ {0} \varepsilon_ {0} \frac {\mathrm{d} \varPhi_ {E}}{\mathrm{d} t} + \mu_ {0} i _ {\mathrm{um}}. \tag {28.5}
$$

Wenn ein Strom fließt, der elektrische Fluss sich aber nicht ändert (z. B. im Fall eines konstanten Stroms in einem Leiter), ist der erste Term auf der rechten Seite von Gl. 28.5 null und die Gleichung reduziert sich auf Gl. 28.4, das Ampèresche Gesetz. Wenn sich umgekehrt der elektrische Fluss ändert, aber kein Strom fließt (wie zwischen den Platten eines Kondensators beim Laden), ist der zweite Term auf der rechten Seite von Gl. 28.5 null und die Gleichung reduziert sich auf Gl. 28.3, das Maxwellsche Induktionsgesetz.

## KONTROLLFRAGE 2

Die Abbildung zeigt Auftragungen der elektrischen Feldstärke E gegen die Zeit für vier homogene elektrische Felder in identischen kreisförmigen Raumbereichen wie in Abb. 28.4b. Ordnen Sie die Felder in absteigender Reihenfolge nach der Feldstärke der induzierten Magnetfelder am Rand dieses Bereichs.

## 28.3 Der Verschiebungsstrom und die Maxwell-Gleichungen

## Lernziele

Nach dem Durcharbeiten dieses Abschnitts sollten Sie in der Lage sein, . . .

zu verstehen, dass man den Beitrag des veränderlichen elektrischen Flusses im Ampère-Maxwellschen Gesetz einem gedachten elektrischen Strom zuordnen kann, dem sogenannten $_ { p } \mathrm { V }$ erschiebungsstrom“, was die Formulierung vereinfacht,
• zu verstehen, dass nach diesem Konzept beim Laden oder Entladen eines Kondensators ein homogen über die Platten verteilter Verschiebungsstrom zwischen den Platten „fließt“,
• die Beziehung zwischen der zeitlichen Änderung des elektrischen Flusses und dem zugehörigen Verschiebungsstrom anzuwenden,
den Zusammenhang zwischen dem Verschiebungsstrom und dem realen Strom für einen Kondensator beim Laden oder Entladen anzugeben und zu verstehen, dass es nur dann einen Verschiebungsstrom gibt, wenn sich das elektrische Feld im Kondensator ändert,
• das Magnetfeld in einem Gebiet mit Verschiebungsstrom zu bestimmen, indem Sie einen Strom durch einen fiktiven Draht annehmen,
• das magnetische Feld von realen und Verschiebungsströmen mithilfe des Ampère-Maxwellschen Gesetzes zu berechnen,
• die magnetischen Feldlinien aufgrund des Verschiebungsstroms beim Laden oder Entladen eines Kondensators zu skizzieren,
• die Maxwellschen Gleichungen anzugeben und die Bedeutung aller vier Gleichungen zu verstehen.

![](images/page_688_chart_16.jpg)

<details>
<summary>line</summary>

| Category | Trend |
| --- | --- |
| a | Downward sloping line |
| b | Downward sloping line |
| c | Downward sloping line |
| d | Horizontal line |
</details>

![](images/page_688_image_17.jpg)

## Schlüsselideen

• In einem veränderlichen elektrischen Feld definieren wir einen gedachten Verschiebungsstrom als

$$
i _ {\mathrm{V}} = \varepsilon_ {0} \frac {\mathrm{d} \varPhi_ {E}}{\mathrm{d} t}.
$$

• Das Ampère-Maxwellsche Gesetz lautet dann

$$
\oint \vec {B} \cdot \mathrm{d} \vec {s} = \mu_ {0} (i _ {\mathrm{V,um}} + i _ {\mathrm{um}}) \qquad (\text {Ampère - Maxwellsches Gesetz}),
$$

![](images/page_688_image_23.jpg)

wobei $i _ { \mathrm { V , u m } }$ den von der Integrationsschleife umschlossenen Verschiebungsstrom darstellt.

Das Konzept des Verschiebungsstroms ermöglicht es uns, uns einen kontinuierlichen Stromfluss durch einen Kondensator vorzustellen. Allerdings ist ein Verschiebungsstrom nicht mit einem Ladungstransport verbunden.
– Die Maxwellschen Gleichungen in Tab. 28.1 fassen alle Aspekte des Elektromagnetismus einschließlich der Optik zusammen.

![](images/page_689_image_1.jpg)

<details>
<summary>text_image</summary>

i
+
-
iV
i
</details>

(a)

![](images/page_689_image_3.jpg)

<details>
<summary>text_image</summary>

i
+
B
B
i
-
B
</details>

Feld des Stroms i

Feld des Stroms i<sub>V</sub>

Feld des Stroms i

(b)

## Abb. 28.6

(a) Der Verschiebungsstrom $i _ { \mathrm { V } }$ zwischen den Platten eines Kondensators, der durch einen Strom i geladen wird.
(b) Die Rechte-Hand-Regel zur Bestimmung der Richtung des Magnetfelds um einen stromführenden Leiter (wie z. B. auf der linken Seite) liefert auch die Richtung des Magnetfelds um einen Verschiebungsstrom (Mitte).

## 28.3.1 Der Verschiebungsstrom

Wenn wir die beiden Terme auf der rechten Seite von Gl. 28.5 vergleichen, sehen wir, dass das Produkt $\varepsilon _ { 0 } ( \mathrm { d } \varPhi _ { E } / \mathrm { d } t )$ die Dimension eines Stroms haben muss. Es wird häufig als fiktiver Strom $i _ { \mathrm { V } }$ betrachtet, den man als **Verschiebungsstrom** bezeichnet:

$$
i _ {\mathrm{V}} = \varepsilon_ {0} \frac {\mathrm{d} \varPhi_ {E}}{\mathrm{d} t}. \tag {28.6}
$$

Der Begriff $_ { p } \mathrm { V }$ erschiebung“ ist insofern unglücklich gewählt, als hier nichts wirklich verschoben wird, aber der Begriff ist historisch bedingt und allgemein etabliert. Mit dieser Definition lautet das Ampère-Maxwellsche Gesetz nun

$$
\oint \vec {B} \cdot \mathrm{d} \vec {s} = \mu_ {0} i _ {\mathrm{V,um}} + \mu_ {0} i _ {\mathrm{um}}, \tag {28.7}
$$

wobei $i _ { \mathrm { V , u m } }$ der von der Leiterschleife umschlossene Verschiebungsstrom ist.

Wir betrachten wieder den Ladevorgang eines Kondensators mit kreisförmigen Platten (Abb. 28.6a). Der reale Strom i, der die Platten lädt, verändert das elektrische Feld $\vec { E }$ zwischen den Platten; diese Änderung des Felds bewirkt einen fiktiven Verschiebungsstrom $i _ { \mathrm { V } }$ zwischen den Platten. Wir wollen nun einen Zusammenhang zwischen den beiden Strömen – dem realen Ladestrom und dem fiktiven Verschiebungsstrom – herstellen.

Zwischen der Ladung $q$ auf den Platten und der elektrischen Feldstärke $E$ zwischen den Platten gilt zu jedem Zeitpunkt die Beziehung aus Gl. 21.4,

$$
q = \varepsilon_ {0} A E, \tag {28.8}
$$

wenn A die Fläche der Platte ist. Um den realen Strom i zu erhalten, differenzieren wir Gl. 28.8 nach der Zeit und bekommen

$$
\frac {\mathrm{d} q}{\mathrm{d} t} = i = \varepsilon_ {0} A \frac {\mathrm{d} E}{\mathrm{d} t}. \tag {28.9}
$$

Den Verschiebungsstrom $i _ { \mathrm { V } }$ erhalten wir aus Gl. 28.6. Wenn wir annehmen, dass das elektrische Feld $E$ zwischen den Platten homogen ist, dann können wir den elektrischen Fluss in dieser Gleichung durch EA ersetzen. Gleichung 28.6 wird dann zu

$$
i _ {\mathrm{V}} = \varepsilon_ {0} \frac {\mathrm{d} \varPhi_ {E}}{\mathrm{d} t} = \varepsilon_ {0} \frac {\mathrm{d} (E A)}{\mathrm{d} t} = \varepsilon_ {0} A \frac {\mathrm{d} E}{\mathrm{d} t}. \tag {28.10}
$$

Durch Vergleich der Gln. 28.9 und 28.10 sehen wir, dass der reale Strom $i ,$ der den Kondensator lädt, und der fiktive Verschiebungsstrom $i _ { \mathrm { V } }$ gleich groß sind:

$$
i _ {\mathrm{V}} = i. \tag {28.11}
$$

Wir können den fiktiven Verschiebungsstrom $i _ { \mathrm { V } }$ folglich als Fortsetzung des realen Stroms i von der einen Platte durch den Zwischenraum zwischen den Platten auf die andere Platte auffassen. Da das elektrische Feld homogen über die Platten verteilt ist, gilt dasselbe auch für den Verschiebungsstrom $i _ { \mathrm { V } } ,$ , wie in Abb. 28.6a durch die Pfeile angedeutet ist. Obwohl in Wirklichkeit keine Ladung über den Zwischenraum zwischen den Platten transportiert wird, kann die Vorstellung eines fiktiven Stroms $i _ { \mathrm { V } }$ uns helfen, schnell Richtung und Betrag eines induzierten Magnetfelds zu bestimmen.

## Die Bestimmung des induzierten Magnetfelds

In Kapitel 25 hatten wir die Richtung des von einem realen Strom erzeugten Magnetfelds mithilfe der Rechte-Hand-Regel aus Abb. 25.4 bestimmt. Dieselbe Regel können wir nun auch anwenden, um die Richtung des von dem fiktiven Verschiebungsstrom $i _ { \mathrm { V } }$ induzierten Magnetfelds zu bestimmen. Das Vorgehen ist in Abb. 28.6b am Beispiel eines Kondensators illustriert.

Mithilfe des Verschiebungsstroms $i _ { \mathrm { V } }$ können wir auch die Feldstärke des Ma gnetfelds bestimmen, das ein Kondensator mit runden parallelen Platten mit dem Radius R beim Laden erzeugt. Dazu stellen wir uns den Zwischenraum zwischen den Platten einfach als runden Draht der Dicke R vor, in dem der fiktive Strom $i _ { \mathrm { V } }$ fließt. Dann folgt aus Gl. 25.22 für die Feldstärke des Magnetfelds im Inneren des Kondensators im Abstand r von der Mittelachse

$$
B = \left(\frac {\mu_ {0} i _ {\mathrm{V}}}{2 \pi R ^ {2}}\right) r. \tag {28.12}
$$

Analog erhalten wir aus Gl. 25.19 für die Feldstärke des Magnetfelds außerhalb des Kondensators im Abstand r von der Mittelachse

$$
B = \frac {\mu_ {0} i _ {\mathrm{V}}}{2 \pi r}. \tag {28.13}
$$

## KONTROLLFRAGE 3

Das Bild zeigt einen Blick aus dem Zwischenraum zwischen den Platten eines Plattenkondensators auf eine der Platten. Die gestrichelten Linien zeigen vier Integrationswege (Weg b folgt dem Rand der Platte). Ordnen Sie die Wege in absteigender Reihenfolge nach dem Wert des Integrals ∮ B⃗ ⋅ d⃗s entlang ihres Umfangs während der Entladung des Kondensators.

![](images/page_690_image_8.jpg)

<details>
<summary>text_image</summary>

c
b
a
d
</details>

## 28.3.2 Die Maxwell-Gleichungen

Bevor wir elektromagnetische Wellen und ihre Ausbreitung untersuchen, wollen wir in diesem Abschnitt die wichtigsten Grundgleichungen der Elektrodynamik zusammenstellen. Das gekoppelte System der vier grundlegenden Gleichungen des Elektromagnetismus ist als die integrale Form der Maxwell-Gleichungen bekannt (Tab. 28.1).

Für viele Anwendungen und speziell auch für die numerische Behandlung auf modernen Computern erweist es sich als sehr nützlich, die in der Tabelle aufgeführten **Maxwell-Gleichungen in Integralform** in ein System gekoppelter, partieller Differenzialgleichungen umzuformen. Das Konzept der partiellen Ableitungen besagt, dass bei der Ableitung einer Funktion F(x, $y , z , t )$ mehrerer Variablen beispielsweise nach x alle anderen Variablen festgehalten, d. h. als konstant betrachtet werden (vgl. Anhang D):

$$
\frac {\partial F}{\partial x} \equiv \left. \frac {\partial F}{\partial x} \right| _ {y, z, t = \mathrm{const}}.
$$

TABELLE 28.1: Die Maxwell-Gleichungen.<sup>a</sup>)

| Bezeichnung | Gleichung |  | Anmerkung |
| --- | --- | --- | --- |
| Gaußscher Satz für elektrische Felder | $\oint \vec{E} \cdot d\vec{A} = q_{innen}/\varepsilon_0$ | (28.14a) | verknüpft elektrischen Gesamtfluss mit umschlossener Gesamtladung |
| Gaußscher Satz für Magnetfelder | $\oint \vec{B} \cdot d\vec{A} = 0$ | (28.14b) | verknüpft magnetischen Gesamtfluss mit umschlossener magnetischer Gesamtladung |
| Faradaysches Gesetz | $\oint \vec{E} \cdot d\vec{s} = -\frac{d\Phi_B}{dt}$ | (28.14c) | verknüpft induziertes elektrisches Feld mit Änderung des magnetischen Flusses |
| Ampère-Maxwellsches Gesetz | $\oint \vec{B} \cdot d\vec{s} = -\mu_0\varepsilon_0\frac{d\Phi_E}{dt} = \mu_0i_{um}$ | (28.14d) | verknüpft induziertes magnetisches Feld mit Änderung des elektrischen Flusses und Strom |

a) Wir betrachten hier den Fall, dass keine dielektrischen oder magnetischen Substanzen anwesend sind.

In partiellen Differenzialgleichungen treten partielle Ableitungen nach verschiedenen Variablen auf, $\mathrm { z .   B .   } \partial F / \partial t$ und $\partial F / \partial x .$ . Weiterhin verwenden wir die Vektorableitungen Divergenz (div) und Rotation (rot; siehe auch hierzu Anhang D).

Damit erhalten wir die Maxwell-Gleichungen in Differenzialform als

$$
\operatorname{div} \vec {E} = \frac {\rho}{\varepsilon_ {0}}, \tag {28.15a}
$$

$$
\operatorname{div} \vec {B} = 0, \tag {28.15b}
$$

$$
\mathrm{rot} \vec {E} + \frac {\partial \vec {B}}{\partial t} = 0, \tag {28.15c}
$$

$$
\mathrm{rot} \vec {B} - \mu_ {0} \varepsilon_ {0} \frac {\partial \vec {E}}{\partial t} = \mu_ {0} \vec {j}. \tag {28.15d}
$$

Hierbei bezeichnet $\rho$ immer die elektrische Ladungsdichte und $\vec { j }$ ist die elektrische Stromdichte.

Weiterhin finden Sie in Anhang D, dass die Divergenz eines Vektorfelds gerade dessen Quellenfeld liefert. Damit sehen wir aus Gl. 28.15a, dass die elektrische Ladungsdichte $\rho$ die Quelle des elektrischen Felds $\vec { E }$ ist. Gleichung 28.15b hingegen zeigt, dass das magnetische Feld $\vec { B }$ keine Quellen besitzt.

Die physikalische Interpretation der Rotation identifiziert rot $\vec { E }$ mit den Wirbeln des Vektorfelds ${ \vec { E } } .$ Demzufolge besagt Gl. 28.15c, dass die zeitliche Änderung (Ableitung nach der Zeit) des Magnetfelds $\vec { B }$ ein elektrisches Wirbelfeld erzeugt. Analog sehen wir an Gl. 28.15d, dass sowohl ein sich zeitlich änderndes elektrisches Feld als auch ein fließender elektrischer Strom $\vec { j }$ ein magnetisches Wirbelfeld erzeugen.

Insgesamt erklären die Maxwell-Gleichungen zahlreiche elektromagnetische Erscheinungen, angefangen bei der Frage, warum Kompassnadeln nach Norden zeigen, bis hin zu der Frage, warum ein Auto anspringt, wenn man den Zündschlüssel dreht (oder die aus heutiger Sicht ebenso interessante Frage, wie das Auto „spürt“, dass Sie auf den Funkschlüssel drücken, um die Türen zu öffnen). Sie sind die Grundlage zahlloser elektromagnetischer Geräte wie Elektromotoren, Funksender und -empfänger, Festnetz- oder Mobiltelefone, Radargeräte und Mikrowellenöfen, um nur einige wenige Beispiele zu nennen.

Viele der seit Kapitel 17 vorgestellten Gleichungen lassen sich aus den Maxwell-Gleichungen herleiten. Außerdem sind sie auch Voraussetzung für die vielen Gleichungen in diesem Kapitel sowie in den nachfolgenden Kapiteln, in denen wir uns mit Optik beschäftigen.

## 28.4 Magnete

![](images/page_691_image_13.jpg)

## Lernziele

Nach dem Durcharbeiten dieses Abschnitts sollten Sie in der Lage sei $1 , \ldots$

• Magneteisensteine zu erkennen,
• zu verstehen, dass das Erdmagnetfeld annähernd ein Dipolfeld ist, und die ungefähre Lage der geomagnetischen Pole der Erde anzugeben,
• Deklination und Inklination des Erdmagnetfelds anzugeben.

![](images/page_691_image_20.jpg)

## Schlüsselideen

• Die Erde ist annähernd ein magnetischer Dipol, dessen Achse etwas gegen die Rotationsachse der Erde geneigt ist. Der magnetische Südpol liegt dabei auf der Nordhalbkugel (in der kanadischen Arktis).
• Die Feldrichtung an einem Ort wird durch die Felddeklination (den Winkel zwischen der horizontalen Feldkomponente und der geografischen Nordrichtung) und die Feldinklination (den Winkel zwischen der Horizontalen und der Feldrichtung) angegeben.

## 28.4.1 Magnete

Die ersten bekannten Magnete waren Magneteisensteine, natürlich magnetisierte Steine. Als die Griechen und Chinesen in der Antike solche Steine fanden, wunderten sie sich über die scheinbar magische Fähigkeit der Steine, Metalle über kurze Entfernungen anzuziehen. Erst viel später lernten sie, Magneteisenstein in Kompassen als Hilfe zur Orientierung einzusetzen.

Heute sind Magnete und magnetische Materialien aus unserem Leben nicht mehr wegzudenken. Wir finden sie in nahezu allen elektronischen Geräten, in Kreditkarten, Kopfhörern und in den Druckfarben für Banknoten. Sogar manche Frühstückszerealien, die mit besonders hohem Eisengehalt werben, enthalten winzige magnetische Partikel (die man mit einem Magneten aus einer Aufschwemmung mit Wasser herausfischen kann). Viel wichtiger ist jedoch, dass die moderne Elektronikindustrie (inklusive Computer- und Musikindustrie) ohne magnetische Materialien nicht existieren würde.

## Der Erdmagnetismus

Die Erde ist ein riesiger Magnet; für Punkte in der Nähe der Erdoberfläche können wir uns das Magnetfeld der Erde näherungsweise als das Feld eines großen Stabma gneten – eines magnetischen Dipols – vorstellen, der durch den Mittelpunkt der Erde verläuft. Abbildung 28.7 zeigt eine idealisierte, symmetrische Darstellung des Dipolfelds ohne die durch die Wirkung des Sonnenwinds verursachte Verzerrung.

Da das Magnetfeld der Erde das eines magnetischen Dipols ist, ist damit auch ein magnetisches Dipolmoment $\vec { \mu }$ verbunden. Für das idealisierte Feld aus Abb. 28.7 beträgt das Dipolmoment $8 , 0 \cdot 1 0 ^ { 2 2 }   \mathrm { J / T } ;$ es schließt einen Winkel von $^ { 1 1 , 5 ^ { \circ } }$ mit der Rotationsachse der Erde (RR′) ein. Die Dipolachse (MM′) zeigt in die Richtung des Dipolmoments und schneidet die Erdoberfläche am geomagnetischen Nordpol in der kanadischen Arktis und am geomagnetischen Südpol in der Antarktis. Die Feldlinien des Magnetfelds B treten auf der Südhalbkugel aus der Erde aus und auf der Nordhalbkugel wieder in die Erde ein. Der Pol auf der Nordhalbkugel der Erde, den wir üblicherweise als „geomagnetischen Nordpol“ kennen, ist damit in Wirklichkeit der Südpol des magnetischen Dipols Erde.

Die Richtung des Magnetfelds an einem beliebigen Punkt auf der Erdoberflä- che wird meist durch zwei Winkel angegeben. Die **Deklination** ist der Winkel (nach rechts oder links) zwischen der horizontalen Komponente des Magnetfelds und der Nordrichtung (der Richtung zum 90. Breitengrad). Die **Inklination** ist der Winkel (nach oben oder unten) zwischen der Horizontalen und der Feldrichtung.

Magnetometer messen diese Winkel und die Feldstärke sehr genau; mit einem Kompass und einem Inklinationsmesser geht es jedoch auch einfacher. Ein Kompass ist ein nadelförmiger Magnet, der so aufgehängt ist, dass er sich frei um eine vertikale Achse drehen kann. Wenn er waagrecht gehalten wird, zeigt der Nordpol der Nadel in Richtung des magnetischen Nordpols der Erde (der ja in Wirklichkeit ein magnetischer Südpol ist). Der Winkel zwischen der Nadel und der Nordrichtung ist die Deklination des Felds. Ein Inklinationsmesser ist ein ähnlicher Magnet, der diesmal aber frei um eine horizontale Achse rotieren kann. Wenn man seine vertikale Rotationsebene (mithilfe eines Kompasses) nach Norden ausrichtet, dann ist der Winkel zwischen der Nadel des Inklinationsmessers und der Horizontalen die Inklination.

In Wirklichkeit können Richtung und Stärke des Magnetfelds auf der Erdoberfläche deutlich von dem idealen Dipolfeld aus Abb. 28.7 abweichen. Zum Beispiel liegt der Punkt, an dem das Magnetfeld senkrecht auf der Erdoberfläche (einwärts) steht, nicht etwa am geomagnetischen Nordpol im äußersten Nordosten von Kanada, sondern dieser sogenannte arktischer Magnetpol befindet sich im Nordpolarmeer, mehrere hundert Kilometer nördlich der kanadischen Nordküste.

![](images/page_692_image_11.jpg)

<details>
<summary>text_image</summary>

geo-
magnetischer
Nordpol
M
R
S
N
B
geografischer
Nordpol
R'
M'
</details>

Abb. 28.7 Das Magnetfeld der Erde als Dipolfeld. Die Dipolachse MM′ liegt in einem Winkel von 11,5° zur Rotationsachse RR′ der Erde. Der Südpol des Dipols liegt auf der Nordhalbkugel der Erde.

## Abb. 28.8

Ein Magnetprofil des Meeresbodens zu beiden Seiten des Mittelatlantischen Rückens. Der Meeresboden wird in dem Rücken aus heißem Magma gebildet und bewegt sich auf beiden Seiten von dem Rücken weg. Die

Magnetisierung des Meeresbodens speichert die magnetische Umgebung zur Zeit der Erstarrung des Magmas. Ungefähr alle Million Jahre wechselt das Erdmagnetfeld seine Richtung.

![](images/page_693_image_4.jpg)

<details>
<summary>text_image</summary>

mittelatlantischer Rücken
Alter
(Millionen Jahre)
3,0 2,0 0,7 0,7 2,0 3,0
seitliche Verschiebung
Magma
</details>

Außerdem variiert das Magnetfeld an einem beliebigen Punkt der Erdoberfläche mit der Zeit, und zwar schon über einen Zeitraum von einigen Jahren messbar und über Zeiträume von einigen 100 Jahren ganz wesentlich. Zum Beispiel änderte sich die Richtung, in die Kompassnadeln in London zeigten, zwischen 1580 und 1820 um 35°.

Trotz dieser lokalen Variationen ändert sich das mittlere Dipolfeld über solche relativ kurzen Zeiträume nur langsam. Änderungen über längere Zeiträume lassen sich durch Untersuchung der schwachen Magnetisierung des Meeresbodens zu beiden Seiten des Mittelatlantischen Rückens verfolgen (Abb. 28.8). Der Meeresboden entstand dort aus Magma, das aus dem Erdinneren nach oben stieg, erstarrte und seither mit einer Geschwindigkeit von einigen Zentimetern pro Jahr von dem Rücken weggezogen wird. Beim Erstarren wurde das Magma durch das Erdmagnetfeld magnetisiert und speicherte so die Richtung des Erdmagnetfelds zum Zeitpunkt des Erstarrens. Die Untersuchung der Magnetisierung des Meeresbodens zeigt, dass das Erdmagnetfeld seine Richtung etwa alle Million Jahre umgedreht hat. Die Ursache für diese Umkehrung muss in Instabilitäten des sogenannten Geodynamos im zähflüssigen Erdkern liegen, dessen Funktion aber noch lange nicht voll verstanden ist.

## 28.5 Der Magnetismus von Elektronen

![](images/page_693_image_8.jpg)

## Lernziele

Nach dem Durcharbeiten dieses Abschnitts sollten Sie in der Lage sein, . . .

• zu verstehen, dass der Spindrehimpuls (kurz Spin) und das damit verbundene magnetische Dipolmoment fundamentale Eigenschaften des Elektrons (und ebenso von Proton und Neutron) sind,
• die Beziehung zwischen Spinvektor $\vec { S }$ und zugehörigem magnetischem Dipolmoment $\vec { \mu } _ { s }$ anzuwenden,
• zu verstehen, dass $\vec { S }$ und $\vec { \mu } _ { s }$ nicht vollständig beobachtet (gemessen) werden können, sondern nur ihr Betrag und eine ihrer Komponenten entlang einer gewählten Achse (meist der z-Achse) bestimmt werden können,
• zu verstehen, dass die beobachtbaren Komponenten $S _ { z }$ und $\mu _ { s , z }$ quantisiert sind und was das bedeutet,
• die Beziehung zwischen $S _ { z }$ und der magnetischen Spinquantenzahl $m _ { s }$ anzuwenden,
• die Spinorientierungen $\mathrm { { \mathfrak { p } } u p } ^ { \alpha }$ und „down“ eines Elektrons voneinander zu unterscheiden,
• die z-Komponente $\mu _ { s , z }$ des von einem Spin erzeugten magnetischen Dipolmoments zu bestimmen und sowohl als Absolutwert als auch als Vielfaches des Bohrschen Magnetons $\mu _ { \mathrm { B } }$ anzugeben,
• die Orientierungsenergie U eines Elektronenspins in einem äußeren magnetischen Feld zu anzugeben,
• zu verstehen, dass ein Elektron in einem Atom einen Bahndrehimpuls $\vec { L } _ { \mathrm { B a h n } }$ und ein zugehöriges magnetisches Bahndipolmoment $\vec { \mu } _ { \mathrm { B a h n } }$ hat,

• die Beziehung zwischen dem Bahndrehimpuls $\vec { L } _ { \mathrm { B a h n } }$ und dem zugehörigen magnetischen Dipolmoment $\vec { \mu } _ { \mathrm { B a h n } }$ anzuwenden,
• zu verstehen, dass $\vec { L } _ { \mathrm { B a h n } }$ und $\vec { \mu } _ { \mathrm { B a h n } }$ nicht vollständig beobachtet (gemessen) werden können, sondern nur ihre Komponenten entlang einer gewählten Achse (meist der z-Achse) bestimmt werden können,
• die Beziehung zwischen $L _ { \mathrm { B a h n } , i }$ und der Bahndrehimpulsquantenzahl $m _ { l }$ anzuwenden.
• die z-Komponente $\mu _ { \mathrm { B a h n } , z }$ des von einem Bahndrehimpuls erzeugten magnetischen Dipolmoments zu bestimmen und sowohl als Absolutwert als auch als Vielfaches des Bohrschen Magnetons $\mu _ { \mathrm { B } }$ anzugeben,
• die Orientierungsenergie U eines Atoms aufgrund des Bahndrehimpulses seiner Elektronen in einem äußeren magnetischen Feld zu bestimmen,
• den Betrag des magnetischen Moments eines (klassischen) geladenen Teilchens zu berechnen, das sich mit konstanter Winkelgeschwindigkeit auf einer Kreisbahn bewegt,
• das klassische Ringstrommodell eines kreisenden Elektrons sowie die auf einen solchen Ringstrom in einem inhomogenen Magnetfeld wirkenden Kräfte zu beschreiben,
• die Unterschiede zwischen Diamagnetismus, Paramagnetismus und Ferromagnetismus erklären zu können.

## Schlüsselideen

• Ein Elektron hat einen als $, \mathrm{Spim}^{\omega}$ bezeichneten intrinsischen Drehimpuls ${ \vec { S } } ,$ der mit dem magnetischen Dipolmoment $\vec { \mu } _ { s }$ verbunden ist:

$$
\vec {\mu} _ {s} = - \frac {e}{m} \vec {S}.
$$

• Wenn man die Komponente von $\vec { S }$ entlang der z-Achse misst, kann man nur die Werte

$$
S _ {z} = m _ {s} \frac {h}{2 \pi} \quad \text {mit} \quad m _ {s} = \pm \frac {1}{2}
$$

erhalten. Dabei ist $h   =   6 { , } 6 3   \cdot   1 0 ^ { - 3 4 }   \mathrm { J }$ ⋅ s die Plancksche Konstante (oder das Plancksche Wirkungsquantum).

• Entsprechend gilt

$$
\mu_ {z} = \pm \frac {e h}{4 \pi m} = \pm \mu_ {\mathrm{B}}
$$

mit dem Bohrschen Magneton

$$
\mu_ {\mathrm{B}} = \frac {e h}{4 \pi m} = 9, 2 7 \cdot 1 0 ^ {- 2 4}   \mathrm{J/T}.
$$

• Die Energie $U ,$ die mit der Orientierung des Spinmoments in einem äußeren Magnetfeld $\vec { B } _ { \mathrm { e x t } }$ verbunden ist, beträgt

$$
U = - \vec {\mu} _ {s} \cdot \vec {B} _ {\mathrm{ext}} = - \mu_ {s, z} \cdot B _ {\mathrm{ext}}.
$$

• Ein Elektron in einem Atom besitzt noch einen weiteren Drehimpuls, den Bahndrehimpuls $\vec { L } _ { \mathrm { B a h n } }$ . Das damit verbundene magnetische Dipolmoment beträgt

$$
\vec {\mu} _ {\mathrm{Bahn}} = - \frac {e}{2 m} \vec {L} _ {\mathrm{Bahn}}.
$$

• Auch der Bahndrehimpuls ist quantisiert und kann nur die folgenden Messwerte zwischen den Grenzen $\pm m _ { \mathrm { m a x } }$ annehmen:

$$
L _ {\mathrm{Bahn}, z} = m _ {l} \frac {h}{2 \pi} \quad \mathrm{mit} \quad m _ {l} = 0, \pm 1, \pm 2, \dots , \pm m _ {\mathrm{max}}.
$$

![](images/page_694_image_27.jpg)

• Das zugehörige magnetische Dipolmoment ist

$$
\mu_ {\mathrm{Bahn}, z} = - m _ {l} \frac {e h}{4 \pi m} = - m _ {l} \mu_ {\mathrm{B}}.
$$

• Die Energie $U ,$ die mit der Orientierung des magnetischen Bahnmoments in einem äußeren Magnetfeld $\vec { B } _ { \mathrm { e x t } }$ verbunden ist, beträgt

$$
U = - \vec {\mu} _ {\mathrm{Bahn}} \cdot \vec {B} _ {\mathrm{ext}} = - \mu_ {\mathrm{Bahn}, z} \cdot B _ {\mathrm{ext}}.
$$

## 28.5.1 Der Magnetismus von Elektronen

Die magnetischen Eigenschaften von Materialien, egal ob von Magneteisenstein oder von Computerfestplatten, lassen sich immer auf die darin enthaltenen Elektronen zurückführen. Eine Möglichkeit, wie Elektronen ein Magnetfeld erzeugen können, haben wir bereits kennen gelernt: Wenn wir sie als elektrischen Strom durch einen Draht schicken, bewirkt ihre Bewegung ein Magnetfeld um den Draht. Es gibt aber noch zwei weitere Möglichkeiten, die beide damit zu tun haben, dass Elektronen sich wie kleine magnetische Dipole verhalten. Eine genaue Erklärung dieser Tatsache kann jedoch nur die Quantenphysik geben, die über den in diesem Buch behandelten Stoff hinausgeht, sodass wir vorerst die Ergebnisse nur skizzieren können.

## Das magnetische Dipolmoment des Spins

Elektronen besitzen einen intrinsischen Drehimpuls, den **Spindrehimpuls** oder einfach **Spin** $\vec { S } ;$ mit diesem Spin ist das **magnetische Spindipolmoment** $\vec { \mu } _ { s }$ (meist einfach als **Spinmoment** bezeichnet) verbunden. (Intrinsisch bedeutet in diesem Zusammenhang, dass $\vec { S }$ und $\vec { \mu } _ { s }$ fundamentale Eigenschaften eines Elektrons sind, ähnlich wie Masse oder Ladung.) $\vec { S }$ und $\vec { \mu } _ { s }$ hängen über

$$
\vec {\mu} _ {s} = - \frac {e}{m} \vec {S} \tag {28.16}
$$

zusammen, wobei $e$ die Elementarladung $( 1 , 6 0 \cdot 1 0 ^ { - 1 9 }   \mathrm { C } )$ und m die Masse des Elektrons $( 9 { , } 1 1 \cdot 1 0 ^ { - 3 1 }$ kg) sind. Das Minuszeichen zeigt, dass $\vec { \mu } _ { s }$ und $\vec { S }$ entgegengesetzt gerichtet sind.

Der Spin $\vec { S }$ unterscheidet sich von den Drehimpulsen aus Kapitel $7$ in zweierlei Hinsicht:

1. Der Spindrehimpuls $\vec { S }$ ist selbst nicht messbar; nur sein Betrag und seine Komponente bezüglich einer frei gewählten Achse lassen sich messen.
2. Die Komponenten von $\vec { S }$ sind quantisiert oder gequantelt, d. h. auf bestimmte diskrete Werte beschränkt. Genauer gesagt kann die Messung einer Komponente von $\vec { S }$ nur einen von zwei Werten ergeben, die sich nur im Vorzeichen unterscheiden.

Wir wollen annehmen, dass wir die Komponente von $\vec { S }$ entlang der z-Achse eines Koordinatensystems messen. Dann kann die gemessene Komponente $S _ { z }$ nur die Werte

$$
S _ {z} = m _ {s} \frac {h}{2 \pi} = m _ {s} \hbar \quad \text {mit} \quad m _ {s} = \pm \frac {1}{2} \tag {28.17}
$$

annehmen, wobei $m _ { s }$ als magnetische Spinquantenzahl bezeichnet wird und $h =$ $6 { , } 6 3 \cdot 1 0 ^ { - 3 4 } \mathrm { J } \cdot \mathrm { s }$ die in der Quantenphysik allgegenwärtige Plancksche Konstante (auch als Plancksches Wirkungsquantum bezeichnet) ist (vgl. Gl. 34.3). Die Kombination $h / ( 2 \pi )$ tritt in Gleichungen so häufig auf, dass man ihr ein spezielles Symbol ℏ (gesprochen „h quer“) gibt und sie manchmal auch als reduziertes Plancksches Wirkungsquantum bezeichnet.

Die Vorzeichen in Gl. 28.17 geben die Richtung von $S _ { z }$ bezüglich der z-Achse an. Wenn $S _ { z }$ in die positive z-Richtung zeigt, ist $m _ { s } = + 1 / 2$ und wir bezeichnen den Zustand als spin $u p .$ Wenn $S _ { z }$ in die negative z-Richtung zeigt, ist $m _ { s } = - 1 / 2$ und wir bezeichnen den Zustand als spin down.

Das magnetische Spinmoment $\vec { \mu } _ { s }$ des Elektrons ist ebenfalls nicht messbar, nur seine Komponente entlang einer Achse. Auch diese ist gequantelt und kann nur zwei Werte mit gleichem Betrag, aber unterschiedlichem Vorzeichen annehmen. Die Komponente $\mu _ { s , z }$ entlang der z-Achse hängt mit der Spinkomponente $S _ { z }$ über

$$
\mu_ {s, z} = - \frac {e}{m} S _ {z}
$$

zusammen. Wenn wir $S _ { z }$ aus Gl. 28.17 in diese Gleichung einsetzen, erhalten wir

$$
\mu_ {s, z} = \pm \frac {e h}{4 \pi m}, \tag {28.18}
$$

wobei das Plus- bzw. Minuszeichen dem Zustand mit $\mu _ { s , z }$ parallel bzw. antiparallel zur $z - \mathrm { A }$ chse entsprechen.

Die Größe auf der rechten Seite von Gl. 28.18 wird als Bohrsches Magneton $\mu _ { \mathrm { B } }$ bezeichnet:

$$
\mu_ {\mathrm{B}} = \frac {e h}{4 \pi m} = 9, 2 7 \cdot 1 0 ^ {- 2 4}   \mathrm{J/T}  . \tag {28.19}
$$

$\mu _ { \mathrm { B } }$ wird verwendet, um die magnetischen Spinmomente von Elektronen und anderen Elementarteilchen anzugeben. Für ein Elektron ist die gemessene z-Komponente des Spins

$$
\left| \mu_ {s, z} \right| = 1 \cdot \mu_ {\mathrm{B}}. \tag {28.20}
$$

(Die exakte Quantentheorie des Elektrons, die Quantenelektrodynamik, zeigt, dass $\mu _ { s , z }$ in Wirklichkeit etwas größer als $1 \mu _ { \mathrm { B } }$ ist, aber das wollen wir für den Moment vernachlässigen.)

Wenn wir ein Elektron in ein äußeres Magnetfeld $\vec { B } _ { \mathrm { e x t } }$ bringen, dann führt die Orientierung seines Spinmoments $\vec { \mu } _ { s }$ relativ zu dem äußeren Feld zu einer potenziellen Energie $U$ (genau wie das im Fall des magnetischen Moments $\vec { \mu }$ einer Stromschleife in einem Feld $\vec { B } _ { \mathrm { e x t } }$ der Fall war). Aus Gl. 24.33 entnehmen wir, dass die potenzielle Energie des Elektrons durch

$$
U = - \vec {\mu} _ {s} \cdot \vec {B} _ {\mathrm{ext}} = - \mu_ {s, z} B _ {\mathrm{ext}} \tag {28.21}
$$

gegeben ist, wenn die Richtung des Felds $B _ { \mathrm { e x t } }$ die z-Achse definiert.

Wenn wir uns das Elektron als mikroskopisch kleine Kugel vorstellen (was es nicht ist!), können wir den Spin ${ \vec { S } } ,$ das magnetische Spinmoment $\vec { \mu } _ { s }$ und das dadurch verursachte magnetische Dipolfeld $\vec { \vec { B } }$ wie in Abb. 28.9 darstellen. Obwohl $\mathrm { { , } s p i n ^ { \omega } }$ auf Englisch so viel wie „sich drehen“ bedeutet, rotiert das Elektron nicht etwa wie ein kleiner Kreisel. Wie kann aber etwas einen Drehimpuls haben, ohne wirklich zu rotieren? Diese Frage kann uns wieder nur die Quantenphysik beantworten.

Auch Protonen und Neutronen besitzen einen intrinsischen Drehimpuls, der als Spin bezeichnet wird, und damit auch ein intrinsisches magnetisches Spinmoment. Bei einem Proton zeigen die beiden Vektoren in dieselbe Richtung, bei einem Neutron sind sie entgegengesetzt gerichtet. Da die Beiträge dieser magnetischen Momente zum magnetischen Gesamtmoment eines Atoms ungefähr 1000-mal kleiner sind als die der Elektronen, werden wir sie hier nicht weiter betrachten.

## KONTROLLFRAGE 4

Die Abbildung zeigt die Orientierung der Spins zweier Teilchen in einem äußeren Magnetfeld $\vec { B } _ { \mathrm { e x t ^ { * } } } ^ { \mathrm { ~   ~ } }$ (a) Welche Spinorientierung hat die niedrigere potenzielle Energie, wenn die Teilchen Elektronen sind? (b) Welche Spinorientierung hat die niedrigere potenzielle Energie, wenn die Teilchen Protonen sind?

![](images/page_696_image_20.jpg)

<details>
<summary>text_image</summary>

B
S
μs
</details>

Abb. 28.9

Der Spin $\vec { S } ,$ das magnetische Spinmoment $\vec { \mu } _ { s }$ und das magnetische Dipolfeld $\vec { B }$ eines als mikroskopisch kleine Kugel dargestellten Elektrons.

![](images/page_696_image_23.jpg)

<details>
<summary>text_image</summary>

S_z
(1)
B_ext
(2)
S_z
</details>

## Das magnetische Dipolmoment des Bahndrehimpulses

Außer ihrem Spin besitzen Elektronen in einem Atom noch einen weiteren Drehimpuls, den **Bahndrehimpuls** $\vec { L } _ { \mathrm { B a h n } }$ . Zu ihm gehört ein magnetisches Bahndi**polmoment** $\vec { \mu } _ { \mathrm { B a h n } }$ (meist einfach als **Bahnmoment** bezeichnet) mit

$$
\vec {\mu} _ {\mathrm{Bahn}} = - \frac {e}{2 m} \vec {L} _ {\mathrm{Bahn}}. \tag {28.22}
$$

Das Minuszeichen zeigt wieder an, dass Bahndrehimpuls und magnetisches Mo ment in entgegengesetzte Richtungen zeigen.

Der Bahndrehimpuls $\vec { L } _ { \mathrm { B a h n } }$ ist nicht messbar; wie beim Spin kann nur seine Komponente entlang einer Achse gemessen werden, und diese Komponente ist gequantelt. Die z-Komponente des Bahndrehimpulses kann nur die Werte

$$
L _ {\mathrm{Bahn}, z} = m _ {l} \frac {h}{2 \pi} = m _ {l} \hbar \quad \mathrm{mit} \quad m _ {l} = 0, \pm 1, \pm 2, \dots , \pm m _ {\mathrm{max}} \tag {28.23}
$$

annehmen, wobei $m _ { l }$ die magnetische Quantenzahl des Bahndrehimpulses ist und $, m_{ max }  \text{" }$ den maximal erlaubten Betrag von $m _ { l }$ bedeutet. Die Vorzeichen in Gl. 28.23 zeigen die Richtung von $L _ { \mathrm { B a h n } , z }$ entlang der z-Achse an.

Auch das magnetische Bahnmoment $\vec { \mu } _ { \mathrm { B a h n } }$ ist nicht komplett messbar, sondern wieder nur sein Betrag und seine Komponente bezüglich der z-Achse, die wiederum gequantelt ist. Wenn wir Gl. 28.22 für die Komponente entlang derselben z-Achse wie oben schreiben und $L _ { \mathrm { B a h n } , z }$ aus Gl. 28.23 einsetzen, erhalten wir für die z-Komponente $\mu _ { \mathrm { B a h n } , z }$ des magnetischen Bahnmoments

$$
\mu_ {\mathrm{Bahn}, z} = - m _ {l} \frac {e h}{4 \pi m} \tag {28.24}
$$

bzw. in Einheiten des Bohrschen Magnetons

$$
\mu_ {\mathrm{Bahn}, z} = - m _ {l} \mu_ {\mathrm{B}}. \tag {28.25}
$$

Wenn sich ein Atom in einem äußeren Magnetfeld $\vec { B } _ { \mathrm { e x t } }$ befindet, führt die Orien tierung des magnetischen Bahnmoments jedes einzelnen Elektrons in dem Atom relativ zum äußeren Feld zu einer potenziellen Energie

$$
U = - \vec {\mu} _ {\mathrm{Bahn}} \cdot \vec {B} _ {\mathrm{ext}} = - \mu_ {\mathrm{Bahn}, z} B _ {\mathrm{ext}}, \tag {28.26}
$$

wobei die Richtung von $\vec { B } _ { \mathrm { e x t } }$ wieder die $z - \mathrm { A }$ chse festlegt.

Obwohl wir in den vergangenen Abschnitten stets das Wort „Bahn“ verwendet haben, kreisen die Elektronen in Wirklichkeit nicht um den Atomkern wie z. B. Planeten um die Sonne. Wie kann aber ein Elektron einen Bahndrehimpuls haben, ohne wirklich auf einer Bahn um ein Zentrum zu kreisen? Auch hier lässt sich nur mit der Quantenphysik eine sinnvolle Antwort angeben.

## Das Ringstrommodell für Elektronenbahnen

Wir können Gl. 28.22 mithilfe einer klassischen (d. h. nicht quantenphysikalischen) Argumentation herleiten, indem wir annehmen, dass sich das Elektron auf einer Kreisbahn bewegt, deren Radius viel größer als der Radius eines Atoms ist (daher der Name „Ringstrommodell“). Diese Herleitung gilt jedoch nicht für ein Elektron in einem Atom (dafür brauchen wir wirklich die Quantenphysik).

Wir stellen uns ein Elektron vor, das sich wie in Abb. 28.10 gezeigt mit konstanter Geschwindigkeit v im Gegenuhrzeigersinn auf einer Kreisbahn mit dem Radius r bewegt. Die Bewegung der negativen Ladung des Elektrons entspricht einem konventionellen Strom i (mit positiver Ladung), der – wie ebenfalls in Abb. 28.10 angedeutet – im Uhrzeigersinn fließt. Für den Betrag des magnetischen Bahnmoments eines solchen Ringstroms erhalten wir aus Gl. 24.30 mit $N = 1$

$$
\mu_ {\mathrm{Bahn}} = i A, \tag {28.27}
$$

![](images/page_697_image_20.jpg)

<details>
<summary>text_image</summary>

z
L_Bahn
r
A
-i
-e
v
μ_Bahn
</details>

Abb. 28.10

Ein Elektron bewegt sich mit konstanter Geschwindigkeit v auf einer Kreisbahn mit Radius r, die eine Fläche A umschließt. Der Bahndrehimpuls des Elektrons ist $\vec { L } _ { \mathrm { B a h n } }$ und das damit verbundene magnetische Bahnmoment $\vec { \mu } _ { \mathrm { B a h n } } .$ . Dem im Gegenuhrzeigersinn umlaufenden negativ geladenen Elektron entspricht ein Strom i (positiver Ladungsträger) im Uhrzeigersinn.

wenn A die von der Schleife umschlossene Fläche ist. Nach der Rechte-Hand-Regel aus Abb. 25.18 zeigt dieses magnetische Bahnmoment in Abb. 28.10 nach unten.

Um Gl. 28.27 zu benutzen, benötigen wir den Strom i. Elektrischer Strom ist allgemein die Geschwindigkeit, mit der eine Ladung durch einen bestimmten Punkt transportiert wird. In unserem Fall benötigt die Ladung e die Zeit $T = 2 \pi r / \nu$ , um den Kreis einmal zu umrunden, folglich ist

$$
i = \frac {\text {Ladung}}{\text {Zeit}} = \frac {e}{2 \pi r / \nu}  . \tag {28.28}
$$

Wenn wir dieses Ergebnis und die Fläche $A = \pi r ^ { 2 }$ in Gl. 28.27 einsetzen, bekommen wir

$$
\mu_ {\mathrm{Bahn}} = \frac {e}{2 \pi r / \nu} \pi r ^ {2} = \frac {e \nu r}{2}. \tag {28.29}
$$

Um den Bahndrehimpuls $\vec { L } _ { \mathrm { B a h n } }$ des Elektrons zu erhalten benutzen wir Gl. 7.16, $\vec { \ell } = m ( \vec { r } \times \vec { \nu } )$ . Da ⃗r und v⃗ senkrecht aufeinander stehen, hat $\vec { L } _ { \mathrm { B a h n } }$ den Betrag

$$
L _ {\mathrm{Bahn}} = m r v \sin 9 0 ^ {\circ} = m r v. \tag {28.30}
$$

$\vec { L } _ { \mathrm { B a h n } }$ zeigt in Abb. 28.10 nach oben (siehe auch Abb. 7.10). Wir kombinieren nun die Gln. 28.29 und 28.30, verallgemeinern das Ergebnis auf Vektoren und zeigen die entgegengesetzten Richtungen der Vektoren durch ein Minuszeichen an. So erhalten wir die Beziehung

$$
\vec {\mu} _ {\mathrm{Bahn}} = - \frac {e}{2 m} \vec {L} _ {\mathrm{Bahn}},
$$

also genau Gl. 28.22. Wir haben damit aus einer klassischen (nicht quantenme chanischen) Analyse sowohl nach Betrag als auch nach Richtung dasselbe Resultat erhalten wie aus der Quantenphysik. Man kann sich nun fragen, warum diese Herleitung, die ja auch für ein Elektron in einem Atom das richtige Resultat liefert, hier trotzdem nicht gelten soll. Die Antwort ist, dass die klassische Betrachtungsweise auch Ergebnisse liefert, die im Widerspruch zu den experimentellen Befunden stehen, sie kann daher nur in den Fällen herangezogen werden, in denen sie durch die Quantenphysik bestätigt werden.

## Das Ringstrommodell in einem inhomogenen Feld

Wir betrachten wieder ein Elektron auf einer Kreisbahn als Ringstrom wie in Abb. 28.10. Dieses Mal denken wir uns die Schleife jedoch in einem inhomogenen Magnetfeld wie in Abb. 28.11a. (Zum Beispiel könnten wir das divergierende Feld in der Nähe des Nordpols des Magneten aus Abb. 28.3 verwenden.) Mit dieser modifizierten Anordnung wollen wir die folgenden Abschnitte vorbereiten, in denen wir die Kräfte untersuchen, die auf magnetische Substanzen in inhomogenen Magnetfeldern wirken. Dabei werden wir die Elektronenbahnen in den Atomen als winzige Ringströme analog zu Abb. 28.11a auffassen.

Wir nehmen an, dass das äußere Magnetfeld entlang der Kreisbahn des Elektrons einen konstanten Betrag hat und dass es überall denselben Winkel zur Senkrechten einschließt (Abb. 28.11b und d). Außerdem nehmen wir an, dass alle Elektronen in einem Atom entweder im Gegenuhrzeigersinn (Abb. 28.11b) oder im Uhrzeigersinn (Abb. 28.11d) kreisen. Für beide Bewegungsrichtungen sind der entsprechende konventionelle Strom i in der Stromschleife sowie das durch ihn hervorgerufene magnetische Bahnmoment $\vec { \mu } _ { \mathrm { B a h n } }$ eingezeichnet. Die Abb. 28.11c und e zeigen jeweils zwei Längenelemente dL⃗ an entgegengesetzten Punkten der Schleife, die in die Richtung des Stroms i zeigen. An diesen Längenelementen ist jeweils auch das äußere Feld $\vec { B } _ { \mathrm { e x t } }$ und die auf dL⃗ wirkende magnetische Kraft $\mathrm { d } \vec { F }$ eingezeichnet. Dazu erinnern wir uns, dass auf einen Strom i entlang eines Längenelements dL⃗ in

![](images/page_698_image_15.jpg)

<details>
<summary>text_image</summary>

B$_{ext}$
</details>

(a)

![](images/page_698_image_17.jpg)

<details>
<summary>text_image</summary>

B_ext
B_ext
μ_Bahn
-i
-e
B_ext
</details>

![](images/page_698_image_18.jpg)

<details>
<summary>text_image</summary>

(b)
→
B_ext
×
dF
→
dL
→
(b)
→
B_ext
×
dF
→
dL
→
</details>

![](images/page_698_image_19.jpg)

<details>
<summary>text_image</summary>

B_ext
μ_Bahn
-e
i
(d)
B_ext
dL
dF
(e)
B_ext
dL
dF
</details>

## Abb. 28.11

Ein Ringstrommodell für ein Elektron auf einer Bahn in einem Atom im inhomogenen Magnetfeld $\vec { B } _ { \mathrm { e x t } ^ { * } }$ (b) Eine Ladung −e bewegt sich im Gegenuhrzeigersinn; der entsprechende konventionelle Strom i im Uhrzeigersinn. (c) Die magnetischen Kräfte $\check { \mathrm { d } } \vec { F }$ auf der linken bzw. rechten Seite der Leiterschleife, aus der Schleifenebene gesehen. Die resultierende Kraft auf die Schleife zeigt nach oben. (d) Die Ladung −e bewegt sich im Uhrzeigersinn. (e) Die resultierende Kraft auf die Schleife zeigt nach unten.

einem Magnetfeld $\vec { B } _ { \mathrm { e x t } }$ nach Gl. 24.25 eine Kraft

$$
\mathrm{d} \vec {F} = i \mathrm{d} \vec {L} \times \vec {B} _ {\text {ext}} \tag {28.31}
$$

wirkt.

Mithilfe von Gl. 28.31 können wir sehen, dass die Kraft $\mathrm { d } \vec { F }$ auf der linken Seite in Abb. 28.11c nach rechts oben zeigen muss. Auf der rechten Seite ist $\mathrm { d } \vec { F }$ gleich groß und zeigt nach links oben. Da die Winkel beider Kräfte zur Vertikalen identisch sind, gleichen sich die horizontalen Komponenten dieser beiden Kräfte genau aus, während sich die vertikalen Komponenten addieren. Dasselbe gilt für alle anderen Paare von gegenüberliegenden Punkten in der Schleife, daher muss die resultierende Kraft auf die Stromschleife in Abb. 28.11b nach oben zeigen. Analog erhalten wir für die Situation in Abb. 28.11d eine nach unten gerichtete resultierende Kraft.

Wir werden diese beiden Resultate in Kürze verwenden, wenn wir das Verhalten magnetischer Substanzen in inhomogenen Magnetfeldern untersuchen.

## 28.5.2 Magnetische Materialien

Jedes Elektron in einem Atom besitzt ein magnetisches Bahnmoment und ein magnetisches Spinmoment, die sich vektoriell addieren. Die Resultierende dieser beiden Vektoren addiert sich vektoriell zu den entsprechenden Resultierenden aller anderen Elektronen in dem Atom, und die Resultierenden der einzelnen Atome in einer Probe addieren sich wiederum vektoriell zu einer Resultierenden für die gesamte Probe. Wenn die Kombination all dieser einzelnen Dipolmomente ein Magnetfeld ergibt, ist die Probe magnetisch.

Wir unterscheiden grundsätzlich drei Arten von Magnetismus:

1. **Diamagnetismus** tritt in allen Substanzen auf; er ist aber so schwach, dass er normalerweise nicht mehr zu beobachten ist, wenn ein Material auch eine der beiden anderen Arten von Magnetismus zeigt. Beim Diamagnetismus werden in den Atomen einer Probe schwache magnetische Dipolmomente erzeugt, wenn sie in ein externes Magnetfeld $\vec { B } _ { \mathrm { e x t } }$ gebracht wird; die Kombination dieser Dipolmomente bewirkt eine schwache Magnetisierung der Probe. Die Dipolmomente und damit auch das resultierende Magnetfeld verschwinden, wenn das äußere Feld $\vec { B } _ { \mathrm { e x t } }$ entfernt wird. Üblicherweise bezeichnet man als diamagnetische Materialien nur die Substanzen, die keine andere Art von Magnetismus zeigen.
2. **Paramagnetismus** tritt in Materialien auf, die Übergangsmetalle, Lanthanoide oder Actinoide enthalten (siehe das Periodensystem auf der vorderen Umschlagseite). Alle Atome aus diesen Gruppen besitzen ein permanentes magnetisches Dipolmoment, die verschiedenen Dipolmomente sind in einer Probe aber zufällig angeordnet, sodass die Probe insgesamt kein resultierendes magnetisches Dipolmoment besitzt. Ein externes Magnetfeld $\vec { B } _ { \mathrm { e x t } }$ kann die ato maren Dipolmomente jedoch (teilweise) ausrichten und so ein resultierendes magnetisches Dipolmoment der Probe erzeugen. Die Ausrichtung und damit das Dipolmoment verschwinden, sobald das äußere Feld entfernt wird. Als paramagnetische Materialien bezeichnet man meist Materialien, die vorwiegend Paramagnetismus zeigen.
3. **Ferromagnetismus** ist eine Eigenschaft von Eisen, Nickel und einigen anderen Elementen (sowie von Verbindungen und Legierungen dieser Elemente). Einige der Elektronen in diesen Materialien richten ihre permanenten magnetischen Dipolmomente parallel zueinander aus und erzeugen so Bereiche mit starken resultierenden magnetischen Dipolmomenten in der Probe. Ein externes Feld $\vec { B } _ { \mathrm { e x t } }$ kann die resultierenden Dipolmomente dieser Bereiche ausrichten und so eine starke Magnetisierung einer Probe bewirken; diese Magnetisierung bleibt zumindest teilweise bestehen, wenn $\vec { B } _ { \mathrm { e x t } }$ wieder entfernt wird. In der Regel verwendet man den Begriff ferromagnetisches Material oder sogar den üblicheren Begriff magnetisches Material für Substanzen, die vorwiegend Ferromagnetismus zeigen.

In den nächsten drei Abschnitten werden wir diese drei Arten von Magnetismus näher betrachten.

## 28.6 Diamagnetismus

## Lernziele

Nach dem Durcharbeiten dieses Abschnitts sollten Sie in der Lage sein, . . .

• zu verstehen, dass und wie in einer diamagnetischen Substanz in einem äußeren Magnetfeld ein magnetisches Dipolmoment entsteht, und die relative Orientierung von Moment und äußerem Feld anzugeben,
• die auf eine diamagnetische Substanz in einem inhomogenen magnetischen Feld wirkende Kraft sowie die daraus resultierende Bewegung zu beschreiben.

## Schlüsselideen

• Diamagnetische Materialien zeigen nur dann ein magnetisches Verhalten, wenn sie in ein äußeres Magnetfeld gebracht werden. Sie bilden dann magnetische Dipole, die sich entgegen der äußeren Feldrichtung ausrichten.
• In einem inhomogenen Magnetfeld werden diamagnetische Materialien aus den Gebieten mit großer Feldstärke herausgetrieben.

![](images/page_700_image_13.jpg)

![](images/page_700_image_14.jpg)

## 28.6.1 Diamagnetismus

Wir können die quantenphysikalische Erklärung des Diamagnetismus noch nicht diskutieren, aber wir können mithilfe des Ringstrommodells aus den Abb. 28.10 und 28.11 eine klassische Erklärung für ihn geben. Zunächst nehmen wir an, dass ein Elektron in einem Atom eines diamagnetischen Materials nur entweder im Uhrzeigersinn wie in Abb. 28.11d oder im Gegenuhrzeigersinn wie in Abb. 28.11b kreisen kann. Der fehlende Magnetismus in Abwesenheit eines äußeren Magnetfelds $\vec { B } _ { \mathrm { e x t } }$ zeigt, dass das Atom kein resultierendes magnetisches Dipolmoment besitzt. Daraus folgt, dass vor dem Anlegen von $\vec { B } _ { \mathrm { e x t } }$ gleich viele Elektronen im Atom in die eine wie in die andere Richtung kreisen. Damit gleichen sich die Summe der nach oben gerichteten Dipolmomente und die Summe der nach unten gerichteten Dipolmomente im Atom genau aus.

Nun schalten wir das inhomogene Magnetfeld aus Abb. 28.11a ein. $\vec { B } _ { \mathrm { e x t } }$ ist nach oben gerichtet, aber divergierend (die Feldlinien streben auseinander). Wir können das zum Beispiel erreichen, indem wir den Strom durch einen Elektromagneten allmählich erhöhen oder indem wir den Nordpol eines Stabmagneten immer näher an das betrachtete Atom bringen. Wenn sich die Feldstärke des äußeren Felds von null auf den Endwert $\vec { B } _ { \mathrm { e x t } }$ im stationären Zustand ändert, wird nach dem Faradayschen Gesetz und der Lenzschen Regel ein im Uhrzeigersinn gerichtetes elektrisches Feld um die Bahnschleife des kreisenden Elektrons induziert. Wir wollen nun betrachten, wie dieses induzierte elektrische Feld die kreisenden Elektronen in Abb. 28.11b und d beeinflusst.

In Abb. 28.11b wird das im Gegenuhrzeigersinn umlaufende Elektron von dem induzierten elektrischen Feld beschleunigt. Wenn $\vec { B } _ { \mathrm { e x t } }$ seinen Maximalwert erreicht, erreicht auch das Elektron seine maximale Geschwindigkeit. Das bedeutet, dass der Strom i und das von ihm verursachte nach unten gerichtete magnetische Dipolmoment $\vec { \mu }$ ebenfalls zunehmen.

In Abb. 28.11d wird das im Uhrzeigersinn kreisende Elektron durch das im Uhr zeigersinn orientierte elektrische Feld abgebremst. In diesem Fall müssen die Ge schwindigkeit des Elektrons, der Strom i und das aufwärts gerichtete magnetische Dipolmoment $\vec { \mu }$ alle abnehmen. Durch Einschalten des Felds $\vec { B } _ { \mathrm { e x t } }$ haben wir also dem Atom ein nach unten gerichtetes resultierendes magnetisches Dipolmoment gegeben. Dieses Resultat träfe auch zu, wenn das Magnetfeld homogen wäre.

![](images/page_701_image_1.jpg)

<details>
<summary>natural_image</summary>

Close-up of a small frog inside a transparent circular container (no text or symbols visible)
</details>

Abb. 28.12

Ein Frosch schwebt in einem Magnetfeld, das von einem Strom in einer vertikalen Zylinderspule unter dem Tier erzeugt wird. Die aufwärts gerichtete Kraft des inhomogenen Magnetfelds auf das diamagnetische Tier gleicht die abwärts gerichtete Schwerkraft aus. Der Frosch fühlt sich dabei etwa so, als würde er im Wasser schweben [Quelle: Lijnis Nelemans/CC-SA-3.0].

![](images/page_701_image_4.jpg)

![](images/page_701_image_5.jpg)

![](images/page_701_image_6.jpg)

![](images/page_701_image_7.jpg)

Die Inhomogenität des Magnetfelds beeinflusst das Atom aber auch. Da der Strom i in Abb. 28.11b zunimmt, nimmt auch die aufwärts gerichtete Kraft $\mathrm { d } \vec { F }$ in Abb. 28.11c zu und damit die aufwärts gerichtete Kraft auf die Stromschleife. In Abb. 28.11d nimmt der Strom i ab, folglich nimmt auch die abwärts gerichtete Kraft $\mathrm { d } \vec { F }$ in Abb. 28.11e ab und damit die abwärts gerichtete Kraft auf die Stromschleife. Durch das Anlegen des inhomogenen Magnetfelds $\vec { B } _ { \mathrm { e x t } }$ haben wir also eine resultierende Kraft auf das Atom erzeugt, die von der Gegend des stärkeren Magnetfelds weg zeigt.

Wir haben jetzt zwar mit fiktiven Elektronenbahnen (Ringströmen) argumentiert, haben dabei aber genau das Verhalten abgeleitet, das diamagnetische Substanzen in einem inhomogenen Magnetfeld tatsächlich zeigen: Wenn wir das Magnetfeld wie in Abb. 28.11 anlegen, erhält die Probe ein nach unten gerichtetes magnetisches Dipolmoment und erfährt eine nach oben gerichtete Kraft. Wenn das Feld abgeschaltet wird, verschwinden sowohl das Dipolmoment als auch die Kraft. Dabei muss das externe Feld nicht wie gezeigt anliegen; analoge Argumente gelten für beliebige Orientierungen von $\vec { B } _ { \mathrm { e x t } }$ . Allgemein gilt:

![](images/page_701_image_10.jpg)

Eine diamagnetische Probe erhält in einem äußeren Magnetfeld $\vec { B } _ { \mathrm { e x t } }$ ein magnetisches Dipolmoment, das dem äußeren Feld entgegengesetzt ist. Wenn das äußere Feld inhomogen ist, wird die Probe aus dem Bereich größerer Feldstärke heraus- und in den Bereich kleinerer Feldstärke hineingedrängt.

Der Frosch in Abb. 28.12 ist diamagnetisch (wie jedes andere Lebewesen auch). In dem divergierenden Magnetfeld in der Nähe des oberen Endes eines stromdurchflossenen Solenoids wird jedes seiner Atome nach oben abgestoßen, weg von dem Bereich des stärkeren Magnetfelds am Ende des Solenoids. Das Tier bewegt sich daher so weit aufwärts in den Bereich des schwächeren Magnetfelds, bis die aufwärts gerichtete magnetische Kraft gerade die abwärts gerichtete Schwerkraft ausgleicht und er schwebt. Wenn wir eine hinreichend große Zylinderspule bauen könnten, könnten wir damit auch Menschen aufgrund ihres Diamagnetismus frei in der Luft schweben lassen.

## KONTROLLFRAGE 5

Die Abbildung zeigt zwei diamagnetische Kugeln in der Nähe des Südpols eines Stabmagneten. Sind (a) die magnetischen Kräfte und (b) die magnetischen Dipolmomente der Kugeln auf den Magneten zu oder von ihm weg gerichtet? (c) Ist die magnetische Kraft auf Kugel 1 größer, gleich groß oder kleiner als die auf Kugel 2?

## 28.7 Paramagnetismus

## Lernziele

Nach dem Durcharbeiten dieses Abschnitts sollten Sie in der Lage sein, . . .

• zu verstehen, dass und in welche Richtung sich die magnetischen Momente in einer paramagnetischen Substanz in einem äußeren Magnetfeld ausrichten,
• die Kraft auf eine paramagnetische Substanz in einem inhomogenen magnetischen Feld anzugeben und die aus ihr resultierende Bewegung zu beschreiben,
• die Beziehung zwischen der Magnetisierung M einer paramagnetischen Substanz, dem gemessenen magnetischen Moment und dem Volumen des Stoffs anzuwenden,
• die Magnetisierung M einer Probe mithilfe des Curieschen Gesetzes mit ihrer Temperatur $T ,$ ihrer Curie-Konstante C und dem Betrag B des externen Felds in Beziehung zu setzen,
• anhand einer gegebenen Magnetisierungskurve für ein paramagnetisches Ma terial die Temperaturabhängigkeit der Magnetisierung bei einem bestimmten magnetischen Feld zu erklären,

• die magnetische Orientierungsenergie einer paramagnetischen Probe bei gegebener Temperatur und gegebenem Magnetfeld mit der Energie der thermischen Bewegung zu vergleichen.

## Schlüsselideen

Paramagnetische Materialien enthalten Atome mit einem permanenten magnetischen Dipolmoment. Diese Momente sind in einer Probe jedoch normalerweise zufällig orientiert und ergeben kein nach außen wahrnehmbares magnetisches Moment. Wird das Material jedoch in ein äußeres magnetisches Feld gebracht, richten sich die Dipole in Feldrichtung aus und es tritt eine messbare Magnetisierung auf.

• Die Magnetisierung M gibt an, wie stark die Momente in einem gegebenen Volumen $\bar { V }$ ausgerichtet sind:

$$
M = \frac {\text {gemessenes magnetisches Moment}}{V}.
$$

• Eine vollständige Ausrichtung (Sättigung) aller N Dipole im Volumen ergibt den Maximalwert $M _ { \operatorname* { m a x } } = N \mu / V$ der Magnetisierung.

• Für kleine Werte des Verhältnisses $B _ { \mathrm { e x t } } / T$ gilt

$$
M = C \frac {B _ {\mathrm{ext}}}{T} \quad \text {(Curiesches Gesetz)};
$$

dabei sind $T$ die absolute Temperatur und C die Curie-Konstante des betrachteten Materials.

• In einem inhomogenen äußeren Feld wird ein paramagnetisches Material in Bereiche mit größerer magnetischer Feldstärke gezogen.

## 28.7.1 Paramagnetismus

In paramagnetischen Substanzen heben sich die verschiedenen magnetischen Spin- und Bahnmomente der Elektronen in den Atomen nicht gegenseitig auf, sondern addieren sich vektoriell und geben dem Atom ein resultierendes permanentes magnetisches Dipolmoment $i \vec { \mu } .$ In Abwesenheit eines externen Magnetfelds sind diese magnetischen Dipole in einer Probe jedoch zufällig orientiert und das resultierende Dipolmoment der Probe ist daher null. Wenn die Probe aber in ein externes Magnetfeld $\vec { B } _ { \mathrm { e x t } }$ gebracht wird, so tendieren die individuellen Dipolmomente der Atome dazu, sich parallel zum äußeren Feld auszurichten und geben so der Probe ein resultierendes magnetisches Moment. Die parallele Ausrichtung zum äußeren Feld ist das Gegenteil dessen, was wir bei diamagnetischen Proben hergeleitet hatten.

![](images/page_702_image_14.jpg)

Eine paramagnetische Substanz, die in ein äußeres Magnetfeld $\vec { B } _ { \mathrm { e x t } }$ gebracht wird, entwickelt ein magnetisches Dipolmoment in Richtung von $\vec { B } _ { \mathrm { e x t } }$ . Wenn das Feld inhomogen ist, wird die Probe in den Bereich höherer Feldstärke hineingezogen.

Wenn die Ausrichtung der magnetischen Dipolmomente vollständig wäre, besä- ße eine paramagnetische Probe mit N Atomen ein resultierendes Dipolmoment in der Größenordnung $N \mu .$ . Stöße zwischen den Atomen aufgrund der thermischen Bewegung stören die Ausrichtung jedoch und verringern das tatsächliche Dipolmoment der Probe.

Als Maß für die Bedeutung der thermischen Bewegung können wir zwei Energien vergleichen. Aus Gl. 15.23 erhalten wir für die mittlere kinetische Energie eines Atoms bei einer Temperatur $T$ einen Wert von $K = ( 3 / 2 ) k T ,$ , wobei k die Boltz mann-Konstante ist $\bar { ( } 1 , 3 8 \cdot 1 0 ^ { - 2 3 }   \mathrm { J / K ) }$ und $T$ die Temperatur in Kelvin (nicht in

![](images/page_702_image_18.jpg)

Grad Celsius!). Aus Gl. 24.33 erhalten wir eine Energiedifferenz $\Delta U _ { B } = 2 \mu B _ { \mathrm { e x t } }$ zwischen der parallelen und der antiparallelen Ausrichtung des magnetischen Dipolmoments eines Atoms und des äußeren Felds. Wie wir weiter unten zeigen werden, gilt selbst für gewöhnliche Temperaturen und Feldstärken $K \gg \Delta U _ { B } .$ . Der Energietransfer durch Stöße zwischen den Atomen kann daher die Ausrichtung der magnetischen Dipolmomente empfindlich stören und hält so das magnetische Dipolmoment einer Probe deutlich unter dem erwarteten Wert von $N \mu .$

Das Ausmaß der Ausrichtung der magnetischen Dipolmomente in einer paramagnetischen Probe können wir durch das Verhältnis ihres resultierenden magnetischen Dipolmoments zu ihrem Volumen V ausdrücken. Die resultierende Vektorgröße, das magnetische Dipolmoment pro Volumeneinheit, ist die **Magnetisierung** M⃗ der Probe; ihr Betrag ist

$$
M = \frac {\text {gemessenes magnetisches Moment}}{V}. \tag {28.32}
$$

M hat die Einheit Ampere pro Meter $( \mathrm { A } / \mathrm { m } )$ . Die vollständige Ausrichtung aller magnetischen Dipolmomente, als Sättigung der Probe bezeichnet, entspricht dem Maximalwert $M _ { \operatorname* { m a x } } = N \mu / V .$

1895 entdeckte Pierre Curie, dass die Magnetisierung einer Probe direkt proportional zur Feldstärke des angelegten Magnetfelds $\vec { B } _ { \mathrm { e x t } }$ und umgekehrt proportional zur Temperatur $T$ ist:

$$
M = C \frac {B _ {\mathrm{ext}}}{T}. \tag {28.33}
$$

Gleichung 28.33 ist als Curiesches Gesetz bekannt; C ist die Curie-Konstante. Das Curiesche Gesetz steht im Einklang mit unserem bisherigen Kenntnisstand – wie wir bereits wissen, richtet ein stärkeres Feld $B _ { \mathrm { e x t } }$ die magnetischen Dipole in der Probe stärker aus und vergrößert dadurch $M ,$ während eine steigende Temperatur $T$ die Ausrichtung durch verstärkte thermische Bewegung stört und M folglich verringert. Streng genommen ist das Gesetz aber nur eine Näherung, die solange gilt, wie das Verhältnis $B _ { \mathrm { e x t } } / T$ nicht zu groß wird.

Abbildung 28.13 zeigt das Verhältnis $M / M _ { \mathrm { m a x } }$ als Funktion von $B _ { \mathrm { e x t } } / T$ für das Salz Kaliumchromsulfat, in dem die Chrom-Ionen für den Paramagnetismus verantwortlich sind. Diese Art der Darstellung wird als Magnetisierungskurve bezeichnet. Auf der linken Seite, bis etwa $B _ { \mathrm { e x t } } / \dot { T } = 0 , 5   \mathrm { T / K } ,$ beschreibt die Gerade aus dem Curieschen Gesetz die Messwerte gut; danach werden die Abweichungen aber groß. Die Kurve, die alle Messwerte gut beschreibt, basiert auf der Quantenphysik. Die Messpunkte auf der rechten Seite, in der Nähe der Sättigung, sind experimentell sehr schwer zu bestimmen, da hierfür selbst bei niedrigen Temperaturen sehr hohe Feldstärken notwendig sind (etwa das 100 000-Fache des Erdmagnetfelds).

Abb. 28.13

Eine Magnetisierungskurve für Kaliumchromsulfat, ein paramagnetisches Salz. Aufgetragen ist das Verhältnis der Magnetisierung M zur maximalen Magnetisierung $M _ { \mathrm { m a x } }$ des Salzes gegen das Verhältnis $\overset { \mathrm { m a x } } { B } _ { \mathrm { e x t } } / T$ der Feldstärke des äußeren Felds und der Temperatur. Das Curiesche Gesetz beschreibt die Daten auf der linken Seite der Kurve gut; die Vorhersage aus der Quantentheorie stimmt für alle Werte (nach W.E. Henry).

![](images/page_703_chart_11.jpg)

<details>
<summary>scatter</summary>

| Bext/T (T/K) | 1,30 K | 2,00 K | 3,00 K | 4,21 K |
| --- | --- | --- | --- | --- |
| ~0.25 | — | — | ~0.22 | ~0.16 |
| ~0.35 | ~0.32 | — | ~0.38 | ~0.27 |
| ~0.45 | ~0.45 | — | ~0.48 | ~0.39 |
| ~0.55 | ~0.52 | — | ~0.58 | ~0.48 |
| ~0.65 | — | — | ~0.65 | ~0.58 |
| ~0.75 | — | — | ~0.72 | ~0.65 |
| ~0.85 | — | — | ~0.76 | ~0.72 |
| ~0.95 | — | — | ~0.81 | ~0.76 |
| ~1.15 | — | — | ~0.85 | ~0.83 |
| ~1.35 | — | — | ~0.88 | ~0.86 |
| ~1.55 | — | ~0.91 | — | — |
| ~1.75 | — | ~0.93 | — | — |
| ~1.95 | ~0.94 | — | — | — |
| ~2.15 | — | ~0.96 | — | — |
| ~2.35 | — | ~0.97 | — | — |
| ~2.75 | ~0.99 | — | — | — |
| ~3.75 | 1.00 | — | — | — |
</details>