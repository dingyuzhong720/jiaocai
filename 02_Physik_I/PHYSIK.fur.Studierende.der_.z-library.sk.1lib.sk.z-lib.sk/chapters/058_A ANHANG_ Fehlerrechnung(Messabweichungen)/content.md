# A ANHANG: Fehlerrechnung(Messabweichungen)

原始 PDF 第 621–632 页。

A

## ANHANG: Fehlerrechnung (Messabweichungen)

## A.1 Arten und Ursachen von Messabweichungen

Jeder physikalische Messwert ist mit einer mehr oder weniger großen Messabweichung behaftet. Der wahre Wert einer Messgröße X bleibt deshalb, trotz vielfach wiederholter Messungen, prinzipiell unbekannt. Messabweichungen (früher allgemein als Messfehler bezeichnet) werden zum einen hervorgerufen durch objektive (vom Beobachter unabhängige) Einflussfaktoren, wie z. B. Schwankungen von Temperatur, Luftdruck, elektrischer Spannung u. a., zum anderen durch subjektive Faktoren, die vom Beobachter abhängen, wie Übung, Sehschärfe, Schätzvermögen usw. Nach der Art ihrer Auswirkung auf den Messwert unterscheidet man zwischen systematischen und zufälligen (statistischen) Abweichungen, die beide subjektiv wie objektiv bedingt sein können.

**Systematische Messabweichungen** haben ihre Ursache im Messverfahren (Fehlanzeigen der Instrumente infolge falscher Eichung oder ungenügender Kalibrierung, falsches Messprinzip, konstante einseitige Abweichung von den vorgeschriebenen Versuchsbedingungen oder Vernachlässigung bestimmter, stets gleich bleibender Einflüsse auf das Experiment, z. B. des Luftauftriebs bei Präzisionswägungen u. a.). Sie bewirken, dass die Messwerte stets um einen annähernd konstanten Betrag und in gleicher Richtung (plus oder minus) vom wahren Wert der Messgröße X abweichen. Systematische Messabweichungen sind daher auch durch Wiederholung der Messung nicht zu erkennen und im Mittelwert von Messreihen in vollem Umfang mit enthalten (misst man beispielsweise mit einem falsch kalibrierten Maßstab, so bleibt das Ergebnis auch bei oftmaliger Messung falsch). Sie sind aber prinzipiell vermeidbar, wenn auch oft nur mit beträchtlichem experimentellen Aufwand und großer messtechnischer Erfahrung.

**Zufällige Messabweichungen** vom wahren Wert X schwanken nach Größe und Vorzeichen; sie sind für den einzelnen Messwert grundsätzlich unbekannt und machen ihn unsicher. Die se nicht vermeidbare Zufallsstreuung der Messwerte wird mit statistischen Methoden abge schätzt (s. Abschnitt A.3). Zufällige Messabweichungen werden durch Ungenauigkeiten beim Ablesen von Messinstrumenten, z. B. beim Schätzen von Skalenteilenzwischenwerten, durch regellose Störungen der Messbedingungen, wie z. B. Schwankungen der Netzspannung, zeitliche Anzeigeschwankungen digitaler Messinstrumente um den eigentlichen Messwert u. a., hervorgerufen. Ihr Einfluss kann reduziert werden, wenn die betreffende Größe unter möglichst gleichen Bedingungen mehrmals gemessen wird. In diesem Fall dient der arithmetische Mittelwert aus den einzelnen Messwerten als Messergebnis. Wird eine Größe nur einmal gemessen, so kann die zufällige Abweichung nur pauschal abgeschätzt werden (vgl. A.2).

**Systematische Messabweichungen sind durch eine einseitige Abweichung vom wahren Wert der Messgröße gekennzeichnet, zufällige Messabweichungen führen bei Abwesenheit systematischer Abweichungen zu Schwankungen um den wahren Wert.**

---

A.2 Ermittlung von Messergebnis und Messabweichung

619

## A.2 Ermittlung von Messergebnis und Messabweichung

Die Messabweichung setzt sich aus der systematischen und der zufälligen (statistischen) Abweichung zusammen, welche getrennt voneinander zu ermitteln sind. Die Summe aus beiden ergibt die mögliche Größtabweichung, welche für die Messgenauigkeit maßgebend ist.

**Korrektion.** Die durch ein Messgerät verursachte systematische Abweichung wird durch Ver gleich der Anzeige des Gerätes mit der eines (sehr viel genaueren) Normalgerätes festgestellt. Durch eine Messung mit dem Normalgerät erhält man den als „richtig“ geltenden (konventionell richtigen) Wert $x _ { \Gamma } ,$ der als sehr guter Näherungswert für den wahren Wert X der Messgröße angesehen werden darf. Anstelle der einmaligen Anzeige x des zu prüfenden Messgerä- tes ermittelt man, um zufällige Abweichungen (Messwertstreuung) möglichst auszuschließen, besser den arithmetischen Mittelwert x einer Wiederholmessreihe, bestehend aus den n Einzelmesswerten $x _ { 1 } , x _ { 2 } , \ldots , x _ { n } ;$

$$
\overline {{x}} = \frac {1}{n} \sum_ {i = 1} ^ {n} x _ {i} \qquad (\text {Mittelwert}). \tag {A.1}
$$

Die festgestellte systematische Abweichung ist dann $A = { \overline { { x } } } - x _ { \mathrm { { r } } }$ , und für den richtigen Wert folgt damit $x _ { \mathrm { r } } = { \overline { { x } } } - A = { \overline { { x } } } + K$ , wobei $K = - A$ die (positive oder negative) Korrektion darstellt, mit der jeder vom zu prüfenden Messgerät angezeigte Wert x bzw. erhaltene Mittelwert x der Wiederholmessreihe (durch Addition derselben) zu berichtigen ist.

## Beispiel A.1:

Mit einem Flüssigkeitsthermometer (Skalenteilungswert $^ { 0 , 1   ^ { \circ } \mathrm { C ) } }$ wird als Mittelwert einer Wiederholmessreihe eine Temperatur von $\overline { { \vartheta } } = 2 0 { , } 1 5   ^ { \circ } \mathrm { C }$ erhalten. Als richtiger Wert wird mit einem Normalthermometer (Platinwiderstandsthermometer) $\vartheta _ { \mathrm { r } } = 2 0 { , } 0 1   ^ { \circ } \mathrm { C }$ ermittelt. Die festgestellte systematische Abweichung der Anzeige des Flüssigkeitsthermometers ist $A = \overline { { \partial } } - \partial _ { \mathrm { r } } = 0 , 1 4 \mathrm { K } ,$ womit sich als Korrektion $K = - 0 , 1 4   \mathrm { K }$ ergibt. Jeder mit dem Flüssigkeitsthermometer (zu groß) gemessene Wert ist zwecks Ausschaltung der systematischen Abweichung durch Addition von K zu berichtigen. □

Ganz entsprechend ist auch eine durch äußere Einflüsse oder ein bestimmtes (u. U. falsches) Messprinzip hervorgerufene systematische Abweichung, welche häufig durch Rechnung ermittelt werden kann, zu korrigieren.

## Beispiel A.2:

Wird bei der Wägung eines Körpers, z. B. zur Bestimmung seiner Dichte $\varrho = m / V$ (m Masse, V Volumen des Körpers), die Auftriebskraft in der umgebenden Luft nicht berücksichtigt, so wird dessen Masse nach dem ARCHIMEDischen Prinzip (vgl. 14.2) um die Masse der durch den Körper verdrängten Luft $\varrho _ { \mathrm { L } } V \left( \varrho _ { \mathrm { L } } \right.$ Dichte der Luft) zu klein gemessen, also zu $m   -   \varrho _ { \mathrm { L } } V$ . Entsprechendes gilt bei Verwendung einer Zweischalen-Analysenwaage auch für die auf der anderen Waagschale befindlichen Wägestücke mit der Masse $m ^ { * }$ , dem Volumen $V ^ { * }$ und der Dichte $\varrho ^ { * }$ so dass folgende Gleichgewichtsbedingung gilt:

$$
m - \varrho_ {\mathrm{L}} V = m ^ {*} - \varrho_ {\mathrm{L}} V ^ {*} \quad \text {bzw.} \quad m = m ^ {*} + \varrho_ {\mathrm{L}} (V - V ^ {*}).
$$

Die durch den Luftauftrieb bewirkte systematische Abweichung vom zu bestimmenden Wert m ist also $\boldsymbol { A } = - \varrho _ { \mathrm { L } } ( \boldsymbol { V } - \boldsymbol { V } ^ { * } )$ und somit die „Korrektion“ $K = \varrho _ { \mathrm { L } } ( V - V ^ { * } )$ , welche zur Masse der

---

620

A ANHANG: Fehlerrechnung (Messabweichungen)

aufgelegten Wägestücke zu addieren ist. Da im Allgemeinen nicht $V ^ { * }$ , sondern die Dichte $\varrho ^ { * }$ der Wägestücke bekannt ist, erhält man nach Umformung obiger Beziehung

$$
m = m ^ {*} \left(1 - \frac {\varrho_ {\mathrm{L}}}{\varrho^ {*}}\right) + \varrho_ {\mathrm{L}} V \quad \text {oder} \quad \varrho = \frac {m ^ {*}}{V} \left(1 - \frac {\varrho_ {\mathrm{L}}}{\varrho^ {*}}\right) + \varrho_ {\mathrm{L}}.
$$

**Fehlergrenze.** Die Ermittlung der Korrektion ist für Messeinrichtungen unter Laborbedingungen, insbesondere unter Praktikumsbedingungen, sowie in der betrieblichen Messtechnik nicht ohne Weiteres möglich. Als systematische Abweichung wird daher im Allgemeinen die vom Hersteller des Messgerätes garantierte, in Normen oder Eichordnungen festgelegte und/oder am Gerät angegebene Fehlergrenze angesetzt. Sie gibt an, innerhalb welcher Grenzen der vom Messgerät angezeigte Wert x vom „richtigen Wert“ $x _ { \mathrm { r } } \left( \mathbf { s } .   \mathbf { o } . \right)$ nach oben oder unten abweichen darf.

Viele Messeinrichtungen sind hinsichtlich ihrer Fehlergrenze in **Genauigkeitsklassen** eingeteilt, z. B. analoge elektrische Messgeräte u. a. in die Klassen $^ { 0 , 0 5 ; 0 , 1 ; 0 , 5 ; 1 ; 1 , 5 . }$ Die Klasse gibt hier an, wie viel Prozent vom jeweiligen Messbereichs-Endwert bzw. der Skalenteilung die systematische Abweichung des angezeigten Wertes maximal beträgt. Bei digitalen Messgeräten setzt sich die systematische Abweichung aus mindestens zwei Anteilen zusammen, einem Grundfehler der jeweiligen Baugruppe in Prozent des Messwertes und einem Digitalisierungsfehler, angegeben in digit (kleinster Ziffernschritt), $2.B.0,4\%+3.$ . Gelegentlich kommt noch ein Betrag hinzu, der wie bei analogen Messgeräten in Prozent des Messbereichs-Endwertes angegeben wird. Die entsprechenden Angaben finden sich jeweils in den Bedienungsanleitungen der Messgeräte.

**Größtabweichung.** Zusätzlich zur systematischen Abweichung ist im Messergebnis die zufällige Abweichung zu berücksichtigen. Bei nur einmaliger Messung mit einem analogen Messgerät wird für diese pauschal in der Regel ein halber Skalenteilungswert angesetzt, ebenso, wenn eine Größe nur wenige Male gemessen wird (s. unten stehendes Beispiel A.3/2). Wird zur Erhö- hung der Genauigkeit die gesuchte Größe in einer Messreihe aus mindestens fünf Messungen bestimmt, und weisen die Messwerte eine Streubreite auf, die mit der Fehlergrenze des Messgerätes vergleichbar ist, wird die zufällige Abweichung auf statistischem Wege nach Gleichung (A.5) ermittelt. Bei digitalen Messgeräten wird die zufällige Abweichung aus den die Fehlergrenze überschreitenden zeitlichen Schwankungen des Anzeigewertes abgeschätzt (s. Beispiel A.3/3 unten).

Die Summe aus systematischer und zufälliger Messabweichung ergibt die Größtabweichung $\Delta x$ des Messwertes x vom wahren Wert X. Dieser liegt dann mit Sicherheit im Intervall $( x -$ $\Delta x ) \leq X \leq ( x   +   \Delta x )$ , d. h., es gilt $X = x   \pm   \Delta x$ oder, wenn wir anstelle des Einzelmesswertes x wie oben den besseren, von Messwertstreuung weitgehend freien Mittelwert $( \mathrm { A . 1 } )$ aus mehreren Messungen benutzen,

$$
X = \overline {{x}} \pm \Delta x \quad \text {oder} \quad X = \overline {{x}} \left(1 \pm \frac {\Delta x}{\overline {{x}}}\right) \qquad (\text {Messergebnis}). \tag {A.2}
$$

Aussagekräftiger als die absolute Abweichung $\Delta x$ ist oft die relative Abweichung $\Delta x / \overline { { x } }$ bzw. prozentuale Abweichung $( 1 0 0 \cdot \Delta x / \overline { { x } } ) \% ,   \mathrm { z .   B } .$ beim Vergleich verschiedener Messmethoden bzw. der Messgenauigkeit verschiedener Messgrößen (s. Beispiel A.3/1 unten).

**Rechengenauigkeit.** Da Messwerte Näherungswerte sind, werden ihre Zahlenwerte gerundet. Dabei ist die Anzahl der geltenden Ziffern im Zahlenwert der Ergebnisgröße abhängig von der

---

A.3 Zufallsstreuung von Messwerten

621

Größe der Messabweichung. Als geltende Ziffern eines Näherungswertes bezeichnet man alle Ziffern außer den Nullen, die links von der ersten von null verschiedenen Ziffer stehen. Die Zahlen $3 8 { , } 2 ;   0 { , } 0 0 4   8 5$ und 0,680 haben jeweils drei geltende Ziffern. Die Messabweichung wird im Endergebnis grundsätzlich nur mit einer oder zwei geltenden Ziffern angegeben; dabei ist stets aufzurunden. Der Zahlenwert der Ergebnisgröße ist dann bis auf diejenige Stelle genau anzugeben, auf die sich die letzte der geltenden Ziffern der (gerundeten) Messabweichung noch auswirkt, also z. B. $2 5 { , } 3 1 \pm 0 { , } 5 4$ oder gerundet $^ { 2 5 , 3 \pm 0 , 6 }$ (nicht $^ { 2 5 , 3 \pm 0 , 5 4 }$ oder $^ { 2 5 , 3 1 2   \pm   0 , 5 4 ) }$

## Beispiele A.3:

1. Eine Strecke L von a) 10cm; b) 1km soll auf 1mm genau ausgemessen werden. Wie viel Prozent Messabweichung dürfen bei dem jeweils verwendeten Längenmessgerät maximal zugelassen werden?

Lösung: Die relative Abweichung beträgt im Fall a) $\Delta L / L = 0 , 0 1$ , entsprechend 1%. Diese Genauigkeit ist mit einfachen Längenmessgeräten zu realisieren. Im Fall b) ergibt sich dagegen eine relative Abweichung von nur $1 0 ^ { - 6 }$ , d. h. 0,0001%! Eine solche Genauigkeit ist nur bei Verwendung von Präzisionslängenmessgeräten (z. B. Laserentfernungsmesser) zu erreichen.

2. Ein elektrischer Spannungsmesser der Genauigkeitsklasse 1,5 habe einen Messbereich von 100V bei einem Skalenteilungswert von 1V. Dreimalige Messung einer Spannung U mit diesem Gerät ergab die Werte 81, 80 und 80,5V. Wie lautet das Messergebnis?

Lösung: Die Fehlergrenze beträgt 1,5% von 100V, also 1,5V (systematische Abweichung). Hinzu kommen $0 { , } 5 \mathrm { V } \left( = 1 / 2 \right.$ Skalenteilungswert) als zufällige Abweichung, womit sich als Größtabweichung $\Delta U = 2 { , } 0 \mathrm { V }$ ergibt. Mit dem Mittelwert (A.1) $\overline { { U } } = 8 0 \mathrm { , } 5 \mathrm { V }$ erhalten wir nach (A.2) $U = ( 8 0 , 5 \pm 2 , 0 ) \mathrm { V } = 8 0 , 5 ( 1 \pm 0 , 0 2 5 ) \mathrm { V } ,$ entsprechend 2,5% Abweichung. Das Messergebnis sagt aus, dass der wahre Wert der gemessenen Spannung zwischen 78,5 und 82,5V liegt.

3. In einem Kalorimeter (s. Abschnitt 17.1) wird zur Messung der Mischungstemperatur ϑ ein Digitalthermometer benutzt, als dessen Fehlergrenze $G = 0,06K + 0,02\% + 1$ angegeben ist. Der kleinste Ziffernschritt beträgt 0,1K. Die Thermometeranzeige lautet $^ { 5 2 , 1   ^ { \circ } \mathrm { C } , }$ wobei während der Anzeige Schwankungen um diesen Wert von 1 digit beobachtet werden. Wie lautet das Messergebnis?

Lösung: Die größtmögliche systematische Abweichung, entsprechend G, beträgt $0 , 0 6 \mathrm { K } + 0 , 0 1 \mathrm { K }$ $( = 0 { , } 0 2 ^ { \circ }$ % von $52,1^{\circ}C)+0,1K(=1\mathrm{d}\mathrm{g}\mathrm{i}t)\approx0,2K$ . Da die Anzeigeschwankungen noch innerhalb der Fehlergrenze liegen, braucht eine zusätzliche zufällige Abweichung nicht berücksichtigt zu werden. Es ist also $\Delta \vartheta = 0 { , } 2 \mathrm { K }$ (Größtabweichung), womit als Messergebnis folgt $\vartheta = ( 5 2 { , } 1 \pm$ $^ { 0 , 2 )   ^ { \circ } \mathrm { C } }$ oder $\vartheta = 5 2 , 1 ( 1 \pm 0 , 0 0 4 ) ^ { \circ } \mathrm { C } ,$ entsprechend 0,4% Abweichung. □

## A.3 Zufallsstreuung von Messwerten

Ziel der folgenden Überlegungen ist es, aus den in einer Messreihe ermittelten n Messwerten $x _ { i } = x _ { 1 } , x _ { 2 } , \ldots , x _ { n }$ Aussagen über die zufällige Messabweichung zu gewinnen. Messreihen sind nur sinnvoll, wenn die betreffende Größe mindestens fünfmal gemessen wird und der Streubereich der Einzelmesswerte $x _ { i }$ größer ist als die Fehlergrenze des Messgerätes. Anderenfalls liegt der wahre Wert der Messgröße mit Sicherheit innerhalb des durch die Fehlergrenze vorgegebenen Bereiches.

---

622

A ANHANG: Fehlerrechnung (Messabweichungen)

![](../../raw/pages_0609-0640/images/page_624_chart_2.jpg)

<details>
<summary>histogram</summary>

| Interval | Frequency |
| --- | --- |
| 9.975~9.98 | 2 |
| 9.98~9.99 | 5 |
| \(9.99~10.00\) | 9 |
| \(10.00~10.01\) | \(\sigma\) |
| \(10.01~10.02\) | \(\sigma\) |
| \(10.02~10.03\) | 10 |
| \(10.03~10.04\) | 8 |
| \(10.04~10.05\) | 3 |
</details>

Bild A.1 Histogramm der Häufigkeitsverteilung $w ( x _ { i } )$ einer Messreihe aus 50 Messungen (Messwerte $x _ { i }$ nach Tabelle $\mathsf { A } . 2 )$ sowie die zugehörige Kurve der gaussschen Normalverteilung nach Gleichung (A.3) für $\mu = \overline { { x } } = 1 0 { , } 0 0 6$ und $\sigma = s = 0 { , } 0 1 5$

Trägt man die Messwerte $x _ { i }$ wie in Bild A.1 auf der Abszisse eines Koordinatensystems auf und unterteilt man dieselbe in lauter kleine, gleichgroße Intervalle $\Delta x ,$ so gilt für die Anzahl der Messwerte $\Delta n _ { i }$ , die in das Intervall zwischen $x _ { i }$ und $x _ { i } + \Delta x$ fallen:

$$
\Delta n _ {i} = w (x _ {i}) n \Delta x.
$$

Diese Zahl hängt, wie leicht einzusehen, von der Anzahl n der Messungen insgesamt sowie von der Intervallbreite $\Delta x$ ab, ganz entscheidend aber noch von einer Verteilungsfunktion $w ( x _ { i } )$ welche angibt, wie sich die Messwerte $x _ { i }$ auf die einzelnen Intervalle verteilen. Das Produkt $w ( x _ { i } )   \Delta x = \Delta n _ { i } / n$ ist ein Maß für die Wahrscheinlichkeit (relative Häufigkeit), mit der ein im Intervall zwischen $x _ { i }$ und $x _ { i } + \Delta x$ liegender Wert gemessen wird.

Trägt man über dem jeweiligen Intervall $\Delta x$ balkenförmig die relative Häufigkeit $\Delta n _ { i } / n$ der in das Intervall fallenden Messwerte auf, so erhält man das Histogramm der Messreihe (Bild A.1). Wird die Anzahl der Messungen vergrößert und die Intervallteilung zunehmend verfeinert, nä- hert sich die Verteilung der Messwerte in vielen Fällen immer mehr einer „Glockenkurve“ an, die durch

$$
w (x) = \frac {1}{\sigma \sqrt {2 \pi}} \mathrm{e} ^ {- \frac {(x - \mu) ^ {2}}{2 \sigma^ {2}}} \quad (\text {GAUSSsche Normalverteilung}) \tag {A.3}
$$

beschrieben wird. Die Funktion $w ( x )$ ist zum häufigsten $W e r t ,$ dem Erwartungswert $\mu ,$ symmetrisch und durch den Faktor $1 / \sqrt { 2 \pi \sigma ^ { 2 } }$ auf die Wahrscheinlichkeit $\int \limits _ { - \infty } ^ { \infty } w ( x )   \mathrm { d } x = 1 .$ normiert, entsprechend der Bedingung, dass zwischen −∞ und +∞ 100% der Messwerte x liegen müssen. Die Größe $\sigma$ (bzw. die sog. **Varianz** $\sigma ^ { 2 } )$ ist ein Maß für die Breite der Verteilung w(x) und wird als Streumaß für die zufällige Abweichung eines Messwertes $x _ { i }$ vom Erwartungswert $\mu$ benutzt.

Die GAUSS-Kurve gibt die Verhältnisse für $n \to \infty$ wieder; im Allgemeinen kann diese Voraussetzung für $n \gtrapprox 2 0 0$ als erfüllt gelten. In der Praxis ist jedoch die Anzahl der Messwerte meist wesentlich kleiner. In diesem Fall lassen sich für den Erwartungswert $\mu$ und die Varianz $\sigma ^ { 2 }$ bzw.

---

A.3 Zufallsstreuung von Messwerten

623

σ aus der gemessenen Häufigkeitsverteilung $w ( x _ { i } )$ Schätzwerte angeben. Nach GAUSS ist der beste Schätzwert für $\mu$ der arithmetische Mittelwert x nach Gleichung (A.1) und für $\sigma$ die sog. **Standardabweichung**

$$
s = \sqrt {\frac {1}{n - 1} \sum_ {i = 1} ^ {n} (x _ {i} - \overline {{x}}) ^ {2}} = \sqrt {\frac {1}{n - 1} \left(\sum_ {i = 1} ^ {n} x _ {i} ^ {2} - n \overline {{x}} ^ {2}\right)}. \tag {A.4}
$$

(Hinweis: Mittelwert $\overline { { x } }$ und Standardabweichung s lassen sich mit Hilfe eines Taschenrechners im Statistik-Modus bequem berechnen.)

Tabelle A.1 Student-Faktor t

<table><tr><td rowspan="2">Anzahl der Messungen n</td><td colspan="4">Vertrauensniveau</td></tr><tr><td>68,3%</td><td>95,4%</td><td>99,73%</td><td>99,994%</td></tr><tr><td>2</td><td>1,321</td><td>4,527</td><td>19,21</td><td>125,7</td></tr><tr><td>3</td><td>1,197</td><td>3,307</td><td>9,219</td><td>32,62</td></tr><tr><td>4</td><td>1,142</td><td>2,869</td><td>6,620</td><td>17,45</td></tr><tr><td>5</td><td>1,111</td><td>2,649</td><td>5,507</td><td>12,28</td></tr><tr><td>10</td><td>1,053</td><td>2,284</td><td>3,957</td><td>6,568</td></tr><tr><td>15</td><td>1,034</td><td>2,181</td><td>3,586</td><td>5,481</td></tr><tr><td>20</td><td>1,026</td><td>2,133</td><td>3,422</td><td>5,036</td></tr><tr><td>50</td><td>1,010</td><td>2,051</td><td>3,157</td><td>4,367</td></tr><tr><td>100</td><td>1,005</td><td>2,025</td><td>3,077</td><td>4,177</td></tr><tr><td>250</td><td>1,002</td><td>2,010</td><td>3,030</td><td>4,069</td></tr><tr><td>∞</td><td>1,000</td><td>2,000</td><td>3,000</td><td>4,000</td></tr></table>

Bei einer geringen Anzahl von Wiederholungsmessungen ist der Mittelwert $\overline { { x } }$ als Schätzwert für den Erwartungswert $\mu ,$ der dem wahren Wert X der Messgröße am nächsten kommt, sehr ungenau. Denn nicht nur der einzelne Messwert $x _ { i }$ streut um den wahren Wert $X _ { 1 }$ sondern auch der Mittelwert $\overline { { x } }$ einer Messreihe. Für dessen zufällige Abweichung gilt mit (A.4)

$$
\Delta \overline {{x}} = \frac {t s}{\sqrt {n}} \quad (\text {Streubreite des Mittelwertes, zufällige Messabweichung}). \tag {A.5}
$$

Dabei ist t ein vom Werteumfang n und von der geforderten statistischen Sicherheit, dem sog. **Vertrauensniveau**, abhängiger Wichtungsfaktor (nach STUDENT), der aus Tabelle A.1 zu entnehmen ist. Lässt man z. B. eine Abweichung des Erwartungswertes $\mu$ vom wahren Wert nach beiden Seiten von der Größe der Standardabweichung $\sigma = s \mathbf { z } \mathbf { u } ,$ , so beträgt das Vertrauensniveau 68,3% (Flächeninhalt unter der GAUSS-Kurve im Intervall $\mu \pm \sigma$ , Bild A.1). Für das Streuintervall $\mu \pm 2 \sigma$ , wenn also vom Erwartungswert $\cdot \mu$ weiter weg liegende, weniger häufig vorkommende Messwerte noch mit erfasst werden, ergibt sich ein Vertrauensniveau von 95,4% und für $\mu   \pm   3 \sigma$ ein solches von 99,7%.

Mit der zufälligen Abweichung (A.5) erhält man als Messergebnis für die Größe X bei Abwesenheit systematischer Abweichungen:

$$
X = \overline {{x}} \pm \Delta \overline {{x}} = \overline {{x}} \pm \frac {t s}{\sqrt {n}}. \tag {A.6}
$$

---

624

A ANHANG: Fehlerrechnung (Messabweichungen)

Das Intervall zwischen $\overline { { x } }   - t s / \sqrt { n }$ und $\overline { { x } } + t s / \sqrt { n }$ wird **Vertrauensbereich** des Mittelwertes genannt; die beiden Werte sind die untere und obere Vertrauensgrenze.

## Beispiel A.4:

Die Schwingungsdauer T eines Sekundenpendels (Dauer einer Halbschwingung $T / 2 = 1   \mathrm { s } )$ soll zum Zwecke der Messung der Fallbeschleunigung g (vgl. Abschnitt A.4) möglichst genau bestimmt werden. Dazu wird eine Messreihe mit 50 Messwerten aufgenommen (Tabelle A.2).

Tabelle A.2 Messreihe für die Schwingungsdauer T

| $x_i$s | $x_i - \overline{x}$$10^{-3} \text{s}$ | $(x_i - \overline{x})^2$$10^{-6} \text{s}^2$ | $x_i$s | $x_i - \overline{x}$$10^{-3} \text{s}$ | $(x_i - \overline{x})^2$$10^{-6} \text{s}^2$ |
| --- | --- | --- | --- | --- | --- |
| 9,972 | -34 | 1156 | 10,006 | 0 | 0 |
| 9,975 | -31 | 961 | 10,008 | +2 | 4 |
|  |  |  | 10,008 | +2 | 4 |
| 9,980 | -26 | 676 | 10,009 | +3 | 9 |
| 9,982 | -24 | 576 |  |  |  |
| 9,985 | -21 | 441 | 10,010 | +4 | 16 |
| 9,987 | -19 | 361 | 10,012 | +6 | 36 |
| 9,988 | -18 | 324 | 10,012 | +6 | 36 |
|  |  |  | 10,012 | +6 | 36 |
| 9,991 | -15 | 225 | 10,014 | +8 | 64 |
| 9,992 | -14 | 196 | 10,014 | +8 | 64 |
| 9,993 | -13 | 169 | 10,015 | +9 | 81 |
| 9,995 | -11 | 121 | 10,015 | +9 | 81 |
| 9,995 | -11 | 121 | 10,017 | +11 | 121 |
| 9,995 | -11 | 121 | 10,019 | +13 | 169 |
| 9,997 | -9 | 81 |  |  |  |
| 9,997 | -9 | 81 | 10,020 | +14 | 196 |
| 9,998 | -8 | 64 | 10,020 | +14 | 196 |
|  |  |  | 10,022 | +16 | 256 |
| 10,000 | -6 | 36 | 10,023 | +17 | 289 |
| 10,000 | -6 | 36 | 10,023 | +17 | 289 |
| 10,003 | -3 | 9 | 10,024 | +18 | 324 |
| 10,003 | -3 | 9 | 10,026 | +20 | 400 |
| 10,003 | -3 | 9 | 10,028 | +22 | 484 |
| 10,004 | -2 | 4 |  |  |  |
| 10,004 | -2 | 4 | 10,030 | +24 | 576 |
| 10,005 | -1 | 1 | 10,032 | +26 | 676 |
| 10,005 | -1 | 1 | 10,032 | +26 | 676 |

$$
\begin{array}{l} \sum x _ {i} = 5 0 0, 3 \mathrm{s}, \quad \overline {{x}} = 5 0 0, 3 \mathrm{s} / 5 0 = 1 0, 0 0 6 \mathrm{s}, \quad \sum (x _ {i} - \overline {{x}}) = 0 \mathrm{s}, \\ \sum (x _ {i} - \overline {{x}}) ^ {2} = 1 0   8 6 6 \cdot 1 0 ^ {- 6}   \mathrm{s} ^ {2}, \quad s = \sqrt {\frac {1}{n - 1} \sum (x _ {i} - \overline {{x}}) ^ {2}} = 0, 0 1 5   \mathrm{s}. \\ \end{array}
$$

---

A.4 Fehlerfortpflanzung

625

Jeder Messwert $x _ { i }$ gibt die Dauer von 10 aufeinander folgenden Halbschwingungen an; es ist also $x _ { i } = 5 T _ { i }$ oder $T _ { i } = x _ { i } / 5$ . Die Messwerte sind in der Tabelle nicht in der Reihenfolge ihrer Beobachtung aufgeführt, sondern nach der Größe geordnet und in Gruppen zusammengefasst, entsprechend der Intervallteilung $| \Delta x | = 0 , 0 1 \mathrm { s }$ in Bild A.1, in dem das Histogramm der Messreihe dargestellt ist. Systematische Fehler der elektronischen Zeitmesseinrichtung werden ausgeschlossen.

Gesucht ist die Standardabweichung und der Vertrauensbereich des Mittelwertes für ein Vertrauensniveau von 95%. Wie lautet das Messergebnis für die Schwingungsdauer T ?

Lösung: Aus den in der Tabelle A.2 aufgeführten 50 Messwerten $x _ { i }$ folgt als Mittelwert (A.1) $\overline { { x } } = 1 0 , 0 0 6   \mathrm { s }$ . Die Standardabweichung (A.4) wird damit $s = 0 { , } 0 1 5   { \mathrm { s } } .$ . Für das geforderte Vertrauensniveau ist nach Tabelle A.1 der STUDENT-Faktor $t \approx 2$ . Damit erhält man als zufällige Abweichung des Mittelwertes (A.5) $\Delta \overline{x} = 0,005    s$ (es ist stets aufzurunden) und somit als Vertrauensbereich $\overline { { x } } \pm \Delta \overline { { x } } = ( 1 0 { , } 0 0 6 \pm 0 { , } 0 0 5 )$ s. Es ist also $\overline { { T } } = \overline { { x } } / 5 = 2 \mathrm { , } 0 0 1$ s und $\Delta \overline { { T } } = \Delta \overline { { x } } / 5 = 0 ,   0 0 1   \mathrm { s } ,$ womit als Messergebnis für die Schwingungsdauer $T = \overline { { T } }   +   \Delta \overline { { T } } = ( 2 { , } 0 0 1   \pm   0 { , } 0 0 1 )$ s folgt. Bei Vorhandensein einer systematischen Abweichung (Berücksichtigung z. B. durch die Fehlergrenze G der Messeinrichtung, vgl. A.2) ergäbe sich nach (A.2) $T = \overline { { T } } + \Delta T$ mit der Größtabweichung $\Delta T = \Delta \overline { { T } }   +   G .$ □

## A.4 Fehlerfortpflanzung

Viele physikalische Größen können nicht direkt gemessen werden, sondern müssen aus anderen Größen, die einer direkten Messung zugänglich sind und mit der gesuchten Größe in einem funktionalen Zusammenhang stehen, berechnet werden (indirekte Messung; Beispiel: Bestimmung des elektrischen Widerstandes R aus Messungen zusammengehöriger Werte von Spannung U und Stromstärke I nach dem OHMschen Gesetz $R = U / I )$ . Da jede der direkten Messgrößen mit Messabweichungen behaftet ist, entsteht die Frage, wie sich die Abweichungen $\Delta x , \Delta y , \Delta z , . .$ . der Eingangsgrößen $x , y , z , \ldots ,$ von denen jede zur Erhöhung der Genauigkeit nötigenfalls durch eine Messreihe zu ermitteln ist, auf die gesuchte Größe $F = F ( x , y , z , \ldots )$ auswirken („fortpflanzen“). Gesucht ist also die Abweichung ∆F als Funktion von $\Delta x , \Delta y , \Delta z . . . .$

**Einmalige Messung.** Werden die Eingangsgrößen $x , y , z , \ldots$ nur einmal gemessen, so dass eine statistische Auswertung entfällt und für jede von ihnen nur eine Größtabweichung abgeschätzt werden kann (vgl. Abschnitt A.2), so berechnet sich die Größtabweichung der zusammengesetzten Größe F nach dem linearen Fehlerfortpflanzungsgesetz

$$
\Delta F = \left| \frac {\partial F}{\partial x} \right| \Delta x + \left| \frac {\partial F}{\partial y} \right| \Delta y + \left| \frac {\partial F}{\partial z} \right| \Delta z + \dots . \tag {A.7}
$$

Darin sind $\partial F / \partial x , \partial F / \partial y , . .$ . die partiellen Ableitungen der Funktion F nach den jeweiligen unabhängigen Variablen $x , y , \ldots$ Man bildet $z . \mathrm { B . ~ } \partial F / \partial x$ , indem man F nach x differenziert und dabei alle übrigen Variablen $y , z , \ldots$ . wie Konstanten behandelt. $\Delta x , \Delta y , \Delta z , . .$ . sind wie die Ableitungen in $(\mathrm { A . 7 ) }$ als absolute Beträge (positive Werte) einzusetzen.

Häufig vorkommende Sonderfälle von Gleichung (A.7) sind:

Größtabweichung von Summen und Differenzen. Es liege eine Abhängigkeit der Form

$$
F (x, y, z, \dots) = a x + b y + c z + \dots \quad \text {(lineare Funktion)}
$$

---

626

A ANHANG: Fehlerrechnung (Messabweichungen)

mit $a , b , c , \ldots$ . als Konstanten vor. Dann ist die absolute Abweichung von $F ;$

$$
\Delta F = | a | \Delta x + | b | \Delta y + | c | \Delta z + \dots , \tag {A.8}
$$

also gleich der Summe der mit den Beträgen der Koeffizienten multiplizierten absoluten Abweichungen der Einzelmessgrößen.

Größtabweichung von Produkten und Quotienten. Die Abhängigkeit sei von der Form

$$
F (x, y, z, \dots) = a x ^ {\alpha} y ^ {\beta} z ^ {\gamma} \dots \quad (\text {Potenzprodukt});
$$

$a , \alpha , \beta , \gamma , \ldots$ sind positive oder negative Konstanten. Dann ist die relative Abweichung von $F ;$

$$
\frac {\Delta F}{F} = | \alpha | \frac {\Delta x}{x} + | \beta | \frac {\Delta y}{y} + | \gamma | \frac {\Delta z}{z} + \dots , \tag {A.9}
$$

also gleich der Summe der mit den Beträgen der Potenzexponenten multiplizierten relativen Abweichungen der Einzelmessgrößen. Da die Vorzeichen der Potenzexponenten also keine Rolle spielen, ist es für die relative Abweichung der zusammengesetzten Größe gleichgültig, ob es sich bei dieser um ein Produkt oder um einen Quotienten handelt.

## Beispiel A.5:

Die Dichte eines Metallzylinders von 10mm Durchmesser und 15mm Höhe ist zu bestimmen. Dazu werden mit einer Bügelmessschraube die Werte des Durchmessers und der Hö- he zu $D = 1 0 , 0 0 6   \mathrm { m m }$ und $h = 14, 992    mm$ mit einer geschätzten Größtabweichung von $\Delta D =$ $\Delta h = 0 , 0 1 5   \mathrm { m m }$ gemessen und mittels einer Analysenwaage die Masse des $\mathrm { Z y }$ linders zu $m =$ 9265,2mg mit $\Delta m = 1$ mg ermittelt. Wie lautet das Messergebnis für die Dichte $\varrho ^ { 2 }$

Lösung: Aus $\varrho = 4 m / ( \pi D ^ { 2 } h ) \equiv ( 4 / \pi ) m ^ { \alpha } D ^ { \beta } h ^ { \gamma }$ mit $\alpha = 1 , \beta = - 2$ und $\gamma = - 1$ folgt nach dem linearen Fehlerfortpflanzungsgesetz $( \mathrm { A } . 9 ) { : }   \Delta \varrho / \varrho = \Delta m / m { + } 2 \Delta D / D { + } \Delta h / h .$ Aus den Messwerten für $m , D$ und $h$ erhält man $\varrho = 7 , 8 5 9   \mathrm { m g / m m ^ { 3 } }$ sowie $\Delta \varrho / \varrho = 0 , 0 0 3$ und somit $\Delta \varrho = 0 , 0 0 3 \varrho =$ $0 , 0 2 4   \mathrm { m g } / \mathrm { m m } ^ { 3 }$ . Es ist also gerundet $\varrho = ( 7 , 8 6   \pm   0 , 0 3 )   \mathrm { g } / \mathrm { c m } ^ { 3 }$ (Stahl). Aus dem Ausdruck für $\Delta \varrho / \varrho$ geht hervor, dass der Zylinderdurchmesser D besonders genau gemessen werden muss, um die Abweichung in $\varrho$ klein zu halten. □

**Messreihen.** Wurden bei der indirekten Messung einer Größe $F ( x , y , z , \ldots )$ die Eingangsgrö- ßen $x , y , z , \ldots$ . durch je eine Messreihe ermittelt, so werden deren zufällige Abweichungen $\left( \mathrm{A}.5 \right) \Delta \overline{x}, \Delta \overline{y}, \Delta \overline{z}, \cdots$ , wenn diese voneinander unabhängig sind, nach dem quadratischen (GAUSSschen) Fehlerfortpflanzungsgesetz

$$
\Delta \overline {{F}} = \sqrt {\left(\frac {\partial F}{\partial x} \Delta \overline {{x}}\right) ^ {2} + \left(\frac {\partial F}{\partial y} \Delta \overline {{y}}\right) ^ {2} + \left(\frac {\partial F}{\partial z} \Delta \overline {{z}}\right) ^ {2} + \dots}
$$

zur zufälligen Abweichung der Messgröße $F$ von ihrem Mittelwert $\overline { { F } } = F ( \overline { { x } } , \overline { { y } } , \overline { { z } } )$ zusammengesetzt. $\Delta \overline { { F } }$ ist auf jeden Fall nicht größer als die gewöhnliche Summe $(\mathrm { A . 7 ) }$ . Die direkte Verwendung vorstehender Formel ist in der Praxis meist ziemlich unbequem. Auch hier ist es daher einfacher, zunächst die relative Abweichung $\Delta \overline { { F } } / \overline { { F } }$ zu berechnen und daraus dann mit dem aus den Mittelwerten $\overline { { x } } , \overline { { y } } , \overline { { z } } , . .$ . berechneten Funktionswert $\overline { { F } }$ die Abweichung $\Delta \overline { { F } }$ Für ein Potenzprodukt $F = a x ^ { \alpha } y ^ { \beta } z ^ { \gamma } \ldots   ( a , \alpha , \beta , \gamma , \ldots$ . Konstanten) erhält man, wie sich leicht zeigen lässt, analog zu (A.9)

$$
\frac {\Delta \overline {{F}}}{\overline {{F}}} = \sqrt {\left(\alpha \frac {\Delta \overline {{x}}}{\overline {{x}}}\right) ^ {2} + \left(\beta \frac {\Delta \overline {{y}}}{\overline {{y}}}\right) ^ {2} + \left(\gamma \frac {\Delta \overline {{z}}}{\overline {{z}}}\right) ^ {2} + \dots} \tag {A.10}
$$

---

A.5 Geradenausgleich (lineare Regression). Korrelation

627

## Beispiel A.6:

Aus Messungen der Länge l und der Schwingungsdauer T eines Fadenpendels soll die Fallbeschleunigung g bestimmt werden. Dazu wird ein Sekundenpendel $( T / 2 = 1   \mathrm { s } )$ benutzt. Für dieses wurde die Schwingungsdauer in Abschnitt A.3 (Beispiel A.4) als Mittelwert einer Messreihe zu $\overline { { T } } = 2 { , } 0 0 1$ s mit einer zufälligen Abweichung von $\Delta \overline { { T } } = 0 { , } 0 0 1$ s ermittelt. Mehrmalige Ausmessung der Pendellänge ergibt $\overline { { l } } = 9 9 5 \mathrm { , } 0$ mm mit $\Delta \overline { { l } } = 0$ ,8mm. Keine systematische Abweichungen. Wie lautet das Messergebnis für $g _ { \bullet } ^ { 2 }$

Lösung: Aus (33.17) $T = 2 \pi \sqrt { l / g }$ folgt $g = 4 \pi ^ { 2 } l ^ { \alpha } T ^ { \beta }$ mit $\alpha = 1$ und $\beta = - 2$ , womit man nach (A.10) $\Delta \overline { { g } } / \overline { { g } } = \sqrt { ( \Delta \overline { { l } } / \overline { { l } } ) ^ { 2 } + ( 2 \Delta \overline { { T } } / \overline { { T } } ) ^ { 2 } } = 0 { , } 0 0 1 3$ erhält. Dabei ist $\overline { { g } } = 4 \pi ^ { 2 } \overline { { l } } / \overline { { T } } ^ { 2 } = 9 , 8 1 0 4   \mathrm { m } / \mathrm { s } ^ { 2 }$ , somit $\Delta \overline { { g } } = 0 ,   0 0 1 3   \overline { { g } } \approx 0 ,   0 2   \mathrm { m } / \mathrm { s } ^ { 2 }$ (es wird bei der Abweichung stets aufgerundet). Das Ergebnis lautet also $g = ( 9 , 8 1 \pm 0 , 0 2 )   \mathrm { m } / \mathrm { s } ^ { 2 } = 9 , 8 1 ( 1 \pm 0 , 0 0 2 )   \mathrm { m } / \mathrm { s } ^ { 2 }$ , entsprechend 0,2% Messabweichung.

## A.5 Geradenausgleich (lineare Regression). Korrelation

Wurde eine Größe y in Abhängigkeit von einer Größe x gemessen und grafisch in einem Diagramm dargestellt, entsteht häufig die Frage, durch welche mathematische Funktion $y = f ( x )$ die gesuchte Abhängigkeit beschrieben werden kann bzw. ob – besonders im Fall stark streuender Messwerte – überhaupt ein Zusammenhang zwischen den untersuchten Größen besteht. Man erkennt aber sofort, wenn durch die Messpunkte eine Gerade gelegt werden kann, wenn also zwischen den Variablen eine lineare Abhängigkeit

$$
y = a + b x \tag {A.11}
$$

vermutet wird. Mit dem Lineal wird dann mitunter einfach nach Augenmaß eine Gerade zwischen den Messpunkten hindurchgezogen.

Aufgabe der Ausgleichsrechnung ist es, eine objektive Methode zu finden, die es erlaubt, die Parameter a und b in (A.11) so zu bestimmen, dass die Ausgleichsgerade allen Punkten am nächsten kommt. Im Sinne der GAUSSschen Ausgleichsforderung ist dies dann der Fall, wenn die Quadratsumme der Abstände der Messpunkte von der Geraden in y-Richtung ein Minimum wird. Die x-Koordinaten der Messpunkte werden als frei von Abweichungen angesehen.

Haben wir n Messpunkte $( x _ { i } , y _ { i } )$ , so berechnen sich die Bestwerte der Parameter in (A.11) zu

$$
a = \overline {{y}} - b \overline {{x}}, \quad b = \frac {\overline {{x y}} - \overline {{x}} \cdot \overline {{y}}}{\overline {{x ^ {2}}} - (\overline {{x}}) ^ {2}} \quad \text {(Parameter der Ausgleichsgeraden)} \tag {A.12}
$$

mit den Abkürzungen für die Mittelwerte (alle Summen von $i = 1$ bis $n )$ :

$$
\overline {{x}} = \frac {1}{n} \sum x _ {i}, \quad \overline {{y}} = \frac {1}{n} \sum y _ {i}, \quad \overline {{x y}} = \frac {1}{n} \sum x _ {i} y _ {i}, \quad \overline {{x ^ {2}}} = \frac {1}{n} \sum x _ {i} ^ {2}
$$

sowie in (A.13)

$$
\overline {{(\Delta y) ^ {2}}} = \frac {1}{n} \sum (\Delta y _ {i}) ^ {2} \qquad \mathrm{mit} \qquad \Delta y _ {i} = a + b x _ {i} - y _ {i}.
$$

(Hinweis: Mit einem Taschenrechner im Statistik-Modus lassen sich die Parameter (A.12) a und b leicht berechnen.)

---

628

A ANHANG: Fehlerrechnung (Messabweichungen)

Die Abweichungen $\Delta y _ { i }$ der Ordinatenmesswerte $y _ { i }$ von der Ausgleichsgeraden wirken sich sowohl auf ihren Ordinatenabschnitt a als auch auf ihre Steigung b aus. Für deren mittlere Abweichungen gilt:

$$
\overline {{s}} _ {a} = \overline {{s}} _ {b} \sqrt {\overline {{x ^ {2}}}}, \quad \overline {{s}} _ {b} = \sqrt {\frac {1}{n - 2} \frac {\overline {{(\Delta y) ^ {2}}}}{\overline {{x ^ {2}}} - (\bar {x}) ^ {2}}} \quad \text {(mittlere Abweichung der Parameter der Ausgleichsgeraden).} \tag {A.13}
$$

Viele nichtlineare Zusammenhänge lassen sich durch geeignete mathematische Umformungen in lineare umwandeln. So liefert allgemein jede Potenzfunktion im doppelt-logarithmischen Koordinatensystem und jede Exponentialfunktion in einfach-logarithmischer Darstellung der Ordinate eine Gerade, auf welche die vorstehenden Betrachtungen sinngemäß anzuwenden sind.

**Korrelation.** Wird im Unterschied zu oben x als abhängig von $y$ betrachtet, wobei jetzt die Ordinatenwerte $y _ { i }$ als genau und die Abszissenwerte $x _ { i }$ als fehlerbehaftet angesehen werden, so ergibt sich eine zweite Ausgleichsgerade $x = a ^ { \prime } + b ^ { \prime } y .$ . Die beiden Geraden heißen erste und zweite Regressionsgerade, ihre Anstiegsfaktoren b und $b ^ { \prime }$ sind die Regressionskoeffizienten. Analog zu (A.11) erhält man

$$
a ^ {\prime} = \overline {{x}} - b ^ {\prime} \overline {{y}}, \qquad b ^ {\prime} = \frac {\overline {{x y}} - \overline {{x}} \cdot \overline {{y}}}{\overline {{y ^ {2}}} - (\overline {{y}}) ^ {2}}. \tag {A.14}
$$

Die beiden Regressionsgeraden schneiden sich im Schwerpunkt $( \overline { { x } } , \overline { { y } } )$ des Punkthaufens und bilden eine Schere (Bild A.2); sie ist umso enger, je straffer der Zusammenhang zwischen den betrachteten Größen x und y ist. Die Schere schließt sich, wenn ein streng linearer, also funktionaler Zusammenhang besteht. Der Grad des Zusammenhangs wird quantitativ durch den (linearen) Korrelationskoeffizienten r angegeben. Dieser ist das geometrische Mittel aus den Regressionskoeffizienten b und $b ^ { \prime } ;$

$$
r = \sqrt {b b ^ {\prime}} = \frac {\overline {{x y}} - \overline {{x}} \cdot \overline {{y}}}{\sqrt {[ \overline {{x ^ {2}}} - (\overline {{x}}) ^ {2} ] [ \overline {{y ^ {2}}} - (\overline {{y}}) ^ {2} ]}} \quad \text {(Korrelationskoeffizient).} \tag {A.15}
$$

r ist unabhängig von den Einheiten der Messgrößen und kann alle Werte zwischen −1 und +1 annehmen. Es bedeutet

$r = \pm 1$ : Es besteht streng lineare Abhängigkeit zwischen x und y gemäß Gleichung (A.11), für $r = + 1$ mit positivem Anstieg, für $r = - 1$ mit negativem Anstieg der Ausgleichsgeraden;

$0 { , } 8 < | r | \leq 1 ;$ Mit großer Wahrscheinlichkeit besteht eine Korrelation zwischen x und y;

$0 \leq | r | < 0 { , } 5 { : }$ Ein linearer Zusammenhang ist unwahrscheinlich bis ausgeschlossen.

## Beispiele A.7:

1. Thermische Ausdehnung. Die Länge l eines Stabes, die bei $0   ^ { \circ } \mathbf { C }$ den Wert $l _ { 0 }$ hat, wird bei verschiedenen Temperaturen $\vartheta   ( \mathrm { i n }   ^ { \circ } \mathbf { C } )$ gemessen. Es wird lineare Ausdehnung nach der Beziehung $l = l _ { 0 } ( 1 + \alpha \vartheta )$ vorausgesetzt; α ist der lineare Ausdehnungskoeffizient des Stabmaterials. Die Messwerte sind in Tabelle A.3, Spalte 1 und 2, zusammengestellt. Die Größen $l _ { 0 }$ und α einschließlich ihrer mittleren Abweichungen sind zu bestimmen. Trage zur Veranschaulichung die gemessene Abhängigkeit $l = l ( \vartheta )$ in einem Koordinatensystem auf!

Lösung: Die Messpunkte müssten in der grafischen Darstellung recht gut auf einer Geraden liegen, deren Gleichung (A.11) lautet: $l = a + b \vartheta$ mit $a = l _ { 0 }$ als Ordinatenabschnitt und $b =$

---

A.5 Geradenausgleich (lineare Regression). Korrelation

629

Tabelle A.3 Thermische Ausdehnung eines Stabes $\left( \Delta l_{i} = a + b \partial_{i} - l_{i};   a = l_{0},   b = \alpha l_{0} \right)$

| $\vartheta_{i}$°C | $l_{i}$mm | $\vartheta_{i}^{2}$(°C)$^{2}$ | $\vartheta_{i}l_{i}$mm·°C | $a+b\vartheta_{i}$mm | $\Delta l_{i}$$10^{-2}$mm | $(\Delta l_{i})^{2}$$10^{-4}$mm$^{2}$ |
| --- | --- | --- | --- | --- | --- | --- |
| 10 | 800,1 | 100 | 8001 | 800,08 | -2 | 4 |
| 30 | 800,4 | 900 | 24012 | 800,42 | +2 | 4 |
| 50 | 800,8 | 2500 | 40040 | 800,76 | -4 | 16 |
| 70 | 801,0 | 4900 | 56070 | 801,10 | +10 | 100 |
| 90 | 801,5 | 8100 | 72135 | 801,44 | -6 | 36 |

$$
\sum \vartheta_ {i} = 2 5 0 ^ {\circ} \mathrm{C}, \quad \sum l _ {i} = 4 0 0 3, 8 ^ {\circ} \mathrm{C}, \quad \sum \vartheta_ {i} ^ {2} = 1 6 5 0 0 (^ {\circ} \mathrm{C}) ^ {2}, \quad \sum \vartheta_ {i} l _ {i} = 2 0 0 2 5 8 ^ {\circ} \mathrm{C} \cdot \mathrm{mm},
$$

$$
\sum \Delta l _ {i} = 0, \quad \sum (\Delta l _ {i}) ^ {2} = 1 6 0 \cdot 1 0 ^ {- 4} \mathrm{mm} ^ {2}
$$

$$
\overline {{\vartheta}} = 5 0 ^ {\circ} \mathrm{C}, \quad \overline {{l}} = 8 0 0, 7 6 \mathrm{mm}, \quad \overline {{\vartheta^ {2}}} = 3 3 0 0 (^ {\circ} \mathrm{C}) ^ {2}, \quad \overline {{\vartheta l}} = 4 0 0 5 1, 6 ^ {\circ} \mathrm{C} \cdot \mathrm{mm}, \quad \overline {{\Delta l ^ {2}}} = 3 2 \cdot 1 0 ^ {- 4} \mathrm{mm} ^ {2}
$$

$\alpha l _ { 0 }$ als Anstieg. Statt der erforderlichen zwei Messungen haben wir $^ { 5 , }$ also 3 überschüssige (Kontroll-)Messungen. Daher sind wir in der Lage, nicht nur $l _ { 0 }$ und α zu bestimmen, sondern auch deren mittlere Abweichungen. Mit den in der untersten Zeile von Tabelle A.3 angegebenen Mittelwerten erhalten wir nach (A.12) $a = l _ { 0 } = 7 9 9 { , } 9 1$ mm und $b = \alpha l_{0} = 0.017    mm  \cdot  K ^{-1}$ Daraus folgt für den Ausdehnungskoeffizienten $\alpha = b / l _ { 0 } = b / a = 2 1 , 2 5 \cdot 1 0 ^ { - 6 } \mathrm { K } ^ { - 1 }$ . Für die mittleren Abweichungen (A.13) errechnet man $\overline { { s } } _ { b } = 1 . 1 5 \cdot 1 0 ^ { - 3 }   \mathrm { m m } \cdot \mathrm { K } ^ { - 1 }$ und $\overline { { s } } _ { a } = 6 { , } 6 2 \cdot 1 0 ^ { - 2 }$ mm. Die mittlere Abweichung von $\alpha = b /$ a muss aus $\overline { { s } } _ { b }$ und $\overline { { s } } _ { a }$ nach dem quadratischen Fehlerfortpflanzungsgesetz (vgl. vorigen Abschnitt)

$$
\overline {{s}} _ {\alpha} = \sqrt {\left(\frac {\partial \alpha}{\partial a} \overline {{s}} _ {a}\right) ^ {2} + \left(\frac {\partial \alpha}{\partial b} \overline {{s}} _ {b}\right) ^ {2}}
$$

berechnet werden, woraus für die relative Abweichung folgt:

$$
\frac {\overline {{s}} _ {\alpha}}{\alpha} = \sqrt {\left(\frac {\overline {{s}} _ {a}}{a}\right) ^ {2} + \left(\frac {\overline {{s}} _ {b}}{b}\right) ^ {2}} \approx \frac {\overline {{s}} _ {b}}{b} = 6, 7 6 \cdot 1 0 ^ {- 2}
$$

(wegen $\overline { { s } } _ { a } / a   \approx   8   \cdot   1 0 ^ { - 5 }   \ll   \overline { { s } } _ { b } / b )$ . Somit wird $\overline { { s } } _ { \alpha } = 6 , 7 6 \cdot 1 0 ^ { - 2 } \alpha = 1 , 4 4 \cdot 1 0 ^ { - 6 } \mathrm { K } ^ { - 1 }$ . Das Messergebnis lautet: $l _ { 0 } = a \pm \overline { { s } } _ { a } = ( 7 9 9 , 9 1 \pm 0 , 0 7 )$ mm; $\alpha = ( b / a ) \pm \overline { { s } } _ { \alpha } = ( 2 1 { , } 3 \pm 1 { , } 5 ) \cdot 1 0 ^ { - 6 }   \mathrm { K } ^ { - 1 } = 2 1 { , } 3 \cdot 1 0 ^ { - 6 } ( 1 \pm 1 ) \cdot 1 0 ^ { - 6 }   \mathrm { K } ^ { - 1 }$ $0 { , } 0 7 ) \mathrm { K ^ { - 1 } }$ , entsprechend einer Abweichung in α von 7%.

Tabelle A.4 0,2-Dehngrenze x und Zugfestigkeit y für 16 Chargen eines hochfesten Stahles

| Proben-Nr. | $x_i/10^2$ MPa | $y_i/10^2$ MPa | Proben-Nr. | $x_i/10^2$ MPa | $y_i/10^2$ MPa |
| --- | --- | --- | --- | --- | --- |
| 1 | 7,95 | 10,55 | 9 | 8,2 | 11,7 |
| 2 | 9,05 | 10,5 | 10 | 9,25 | 11,6 |
| 3 | 8,25 | 10,4 | 11 | 7,8 | 10,1 |
| 4 | 8,2 | 10,35 | 12 | 8,5 | 11,4 |
| 5 | 9,2 | 11,45 | 13 | 8,0 | 10,95 |
| 6 | 8,6 | 10,9 | 14 | 8,85 | 11,1 |
| 7 | 8,6 | 11,2 | 15 | 9,65 | 12,3 |
| 8 | 10,5 | 12,3 | 16 | 8,05 | 10,6 |
