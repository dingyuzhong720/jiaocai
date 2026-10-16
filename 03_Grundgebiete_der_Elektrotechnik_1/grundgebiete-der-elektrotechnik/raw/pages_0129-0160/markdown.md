![](images/page_128_chart_2.jpg)

<details>
<summary>line</summary>

| Point | uA | uD |
| --- | --- | --- |
| S1 | uA1 | uD1 |
| S'' | uAmin | uD'' |
| u*A2 | uA2 | uD2 |
| u*D2 | uA2 | uD3 |
| u*D3 | uA2 | uD3 |
| u*D3 | uAmax | uD3 |
| S' | uAmax | uD' |
| \(\Delta u'A\) | — | — |
</details>

Abb. 2.124: Zur Stabilität und Instabilität von Arbeitspunkten bei Mitkopplung.

maximal zum Wert $U _ { \mathrm { A m a x } }$ , so dass sich schließlich der Schnittpunkt $S ^ { \prime }   ( u _ { \mathrm { D } } ^ { \prime } ;   U _ { \mathrm { A m a x } } )$ ergibt. Dieser Schnittpunkt ist stabil. Eine kurzzeitige Erhöhung von $u _ { \mathrm { A } }$ über $U _ { \mathrm { A } }$ max hinaus kann vom Verstärker auch durch die hierdurch bewirkte Erhöhung von $u _ { \mathrm { D } }$ nicht aufrechterhalten werden. Eine kurzzeitige Verminderung von $u _ { \mathrm { A } }$ um $\Delta u _ { \mathrm { A } } ^ { \prime }$ auf den Wert $U _ { \mathrm { A m a x } } - \Delta u _ { \mathrm { A } } ^ { \prime }$ kann der Verstärker nur dann aufrechterhalten, wenn $u _ { \mathrm { D } } = u _ { \mathrm { D } 3 }$ ist. Der Spannungsteiler bewirkt aber beim Wert $u _ { \mathrm { A } } = U _ { \mathrm { A m a x } } - \Delta u _ { \mathrm { A } } ^ { \prime }$ , dass $u _ { \mathrm { D } }$ wieder über $u _ { \mathrm { D 3 } }$ hinaus auf $u _ { \mathrm { { D 3 } } } ^ { * }$ anwächst. Bei diesem Wert muss der Verstärker aber zu $u _ { \mathrm { A } } = U _ { \mathrm { A } }$ max zurückkehren. Das heißt: überlagert sich im Betriebsfall $S ^ { \prime }$ der Ausgangsspannung eine Störung, so führt dies wieder in den ursprünglichen Zustand zurück: $S ^ { \prime }$ ist stabil. Geht man übrigens bei der Betrachtung des Betriebszustandes $S _ { 1 }$ von einer Abnahme des Wertes $u _ { \mathrm { A 1 } }$ aus, so führt auch dies aus dem Zustand $u _ { \mathrm { D 1 } } , u _ { \mathrm { A 1 } }$ heraus in einen stabilen Betriebspunkt $( S ^ { \prime \prime } )$

Falls $\nu _ { 0 }$ kleiner als die Arbeitsgeradensteigung einer Mitkopplungsschaltung ist (Bild 2.125), so haben alle Arbeitsgeraden jeweils nur einen einzigen Schnittpunkt mit der Verstärkerkennlinie (VKL). Dieser Arbeitspunkt ist stabil, wie sich durch eine Überlegung zeigen lässt ähnlich der für den Punkt $S _ { 1 }$ in Bild 2.124.

Gleichartige Überlegungen zeigen außerdem, dass der Schnittpunkt der Verstärkerkennlinie mit einer fallenden Arbeitsgeraden – also negativer Steigung – (Gln. (2.120), (2.123)) für die Gegenkopplungsschaltungen in Bild 2.122a, b stabil ist, ganz gleich ob er innerhalb oder außerhalb des Bereiches $U _ { \mathrm { D u } } < u _ { \mathrm { D } } < U _ { \mathrm { D o } }$ liegt.

![](images/page_129_chart_2.jpg)

<details>
<summary>line</summary>

| Point | uD | uA |
| --- | --- | --- |
| 1 | ~0.25 | -3.5 |
| 2 | ~0.45 | -0.5 |
| 3 | ~0.75 | 0.5 |
| 4 | ~1.0 | 3.5 |
</details>

Abb. 2.125: Mitkopplung mit nur stabilen Arbeitspunkten.

## 2.9.4 Spannungsübertragungsfunktion $\pmb { u } _ { \mathsf { A } } = \pmb { f } ( \pmb { u } _ { \mathsf { E } } )$

## 2.9.4.1 Gegenkopplungsschaltungen

## Invertierende Gegenkopplung (Umkehrverstärker)

Wenn eine Arbeitsgerade (Gl. (2.120)) die Verstärkerkennlinie im Bereich der linearen Verstärkung $( U _ { \mathrm { D u } } < u _ { \mathrm { D } } < U _ { \mathrm { D o } } )$ schneidet, so kann man in Gl. (2.120) $u _ { \mathrm { D } }$ durch $u _ { \mathrm { A } } / \nu _ { 0 }$ ersetzen. Damit wird

$$
u _ {\mathrm{A}} = - \frac {R _ {1} + R _ {2}}{R _ {1}} \cdot \frac {u _ {\mathrm{A}}}{\nu_ {0}} - \frac {R _ {2}}{R _ {1}} u _ {\mathrm{E}}
$$

und mit der Abkürzung $R _ { 2 } / _ { R _ { 1 } } = r$

$$
v = \frac {u _ {\mathrm{A}}}{u _ {\mathrm{E}}} = \frac {- r}{1 + \frac {1 + r}{\nu_ {0}}} . \tag {2.124a}
$$

v bezeichnet man als die Gesamtverstärkung des Umkehrverstärkers. In dem wichtigen Fall sehr großer Leerlaufverstärkung $\nu _ { 0 } \left( \nu _ { 0 } \gg 1 + r \right)$ gilt

$$
\lim _ {v _ {0} \to \infty} \frac {u _ {\mathrm{A}}}{u _ {\mathrm{E}}} = - r = - \frac {R _ {2}}{R _ {1}}. \tag {2.124b}
$$

In diesem Fall hängt also v nur vom Verhältnis $R _ { 2 } / _ { R _ { 1 } }$ ab, d. h. von externen Widerständen. Durch die Gegenkopplung kann man die (Gesamt-)Verstärkung begrenzen und vom Wert $\nu _ { 0 }$ unabhängig machen. Statt der Gl. (2.124b) schreibt man die Näherung

$$
\frac {u _ {\mathrm{A}}}{u _ {\mathrm{E}}} \approx - r. \tag {2.124c}
$$

Diese Schreibweise ist besonders verbreitet, aber etwas missverständlich, weil die Voraussetzung $\nu _ { 0 } \to \infty$ unerwähnt bleibt. Ist z. B. $r   =   1 0 0$ und $\nu _ { 0 }   =   1 0$ , so ergibt

Gl. (2.124a) den Wert $\nu = - 9$ , während die Näherungsgleichung (2.124c) zu dem falschen Ergebnis $\nu \approx - 1 0 0$ führen würde. Die Gleichung (2.124a) bestätigt, dass bei reiner Gegenkopplung immer $\nu < \nu _ { 0 }$ bleiben muss. Über $\nu _ { 0 }$ hinaus kann die Gesamtverstärkung nur erhöht werden in Mitkopplungsschaltungen (Beispiel 2.40c; $\nu _ { 0 } = 3$ wird durch MK zu $\nu = 5$ , also $\nu > \nu _ { 0 } )$ und bei Kombination von MK und GK, falls dort die MK überwiegt (Beispiel 2.41d; hier ist z. B. für $\nu _ { 0 } = 2$ die Gesamtverstärkung $\nu = u _ { \mathrm { A } } / _ { u _ { \mathrm { E } } } = 2 , 5 )$

Die Näherungsgleichung (2.124c) lässt sich auch sehr einfach direkt herleiten. Mit $\nu _ { 0 } \to \infty$ wird $u _ { \mathrm { D } } \approx 0$ , solange nur Betriebsfälle im Bereich der linearen Verstärkung betrachtet werden (Bild 2.126).

Dieses vereinfachende Vorgehen lohnt sich immer dann, wenn die Gesamtverstärkung v eines nichtübersteuerten, gegengekoppelten Verstärkers mit großem $\nu _ { 0 }$ näherungsweise zu berechnen ist. Die Gl. (2.124a) kann auch in der Form

$$
u _ {\mathrm{A}} = - \frac {r}{1 + \frac {1 + r}{v _ {0}}} u _ {\mathrm{E}} \tag {2.125}
$$

geschrieben werden. Bild 2.127 zeigt diesen Zusammenhang $u _ { \mathrm { A } } = f ( u _ { \mathrm { E } } )$ und berücksichtigt zugleich, dass $U _ { \mathrm { A m i n } } \leq u _ { \mathrm { A } } \leq U _ { \mathrm { A m a x } }$ sein muss, dass also die gestrichelten Teile der durch Gl. (2.125) beschriebenen Gerade nicht gelten.

Das Bild 2.127 veranschaulicht, dass die in Gl. (2.125) beschriebene Proportionalität zwischen $u _ { \mathrm { A } }$ und $u _ { \mathrm { E } }$ nur im Bereich $U _ { \mathtt { E u } } \leq u _ { \mathtt { E } } \leq U _ { \mathtt { E o } }$ gilt, hierbei ist

$$
U _ {\mathrm{Eu}} = - \frac {U _ {\mathrm{Amax}}}{r} \left(1 + \frac {1 + r}{v _ {0}}\right) \approx - \frac {U _ {\mathrm{Amax}}}{r} \tag {2.126a}
$$

$$
U _ {\mathrm{E0}} = - \frac {U _ {\mathrm{A} \min}}{r} \left(1 + \frac {1 + r}{v _ {0}}\right) \approx - \frac {U _ {\mathrm{A} \min}}{r}. \tag {2.126b}
$$

**Übersteuerung:** Treten Werte $u _ { \mathrm { E } } < U _ { \mathrm { E u } }$ oder $u _ { \mathrm { E } } > U _ { \mathrm { E } _ { 0 } }$ auf, so wird der Umkehrverstärker »übersteuert«. Ein- und Ausgangssignal sind dann nicht mehr proportional zueinander (Begrenzung des Ausgangssignals $u _ { \mathrm { A } } )$ . Bild 2.128 gibt hierfür ein Beispiel. Wenn die Amplitude (Scheitelwert) der zeitlich sinusförmigen Spannung $u _ { \mathrm { E } } ( t )$ größer als $4   \mathrm { V }$ ist, so ist die Ausgangsspannung $u _ { \mathrm { A } } ( t )$ nicht mehr sinusförmig. Die Gln. (2.126) zeigen, dass der Bereich, in dem $u _ { \mathrm { E } }$ linear verstärkt wird, umso größer ist, je kleiner r ist (Bild 2.129).

![](images/page_130_image_11.jpg)

<details>
<summary>text_image</summary>

E
i1
R1
u1 ≈ uE
N
R2
u2 ≈ -uA
i2
A
uE
iN = 0
uD ≈ 0
-
+
uA
</details>

Abb. 2.126: Umkehrverstärker.

$$
i _ {1} = i _ {2}; u _ {1} / R _ {1} = u _ {2} / R _ {2};
$$

$$
u _ {\mathrm{E}} / R _ {1} \approx - u _ {\mathrm{A}} / R _ {2};
$$

$$
\boxed {u _ {\mathrm{A}} / u _ {\mathrm{E}} \approx - R _ {2} / R _ {1}} = - r.
$$

![](images/page_131_chart_2.jpg)

<details>
<summary>line</summary>

| uE | uA |
| --- | --- |
| <UEu | U_Amax |
| UEu | U_Amax |
| UEo | U_Amin |
| >UEo | U_Amin |
</details>

Abb. 2.127: Gesamtverstärkung $\boldsymbol { u } _ { \mathsf { A } } = f _ { } ( \boldsymbol { u } _ { \mathsf { E } } )$ des Umkehrverstärkers.

![](images/page_131_image_4.jpg)

Abb. 2.128: Lineare Verstärkung und Übersteuerung beim Umkehrverstärker.

## Nichtinvertierende Gegenkopplung (Elektrometerverstärker)

Beim Elektrometerverstärker in Bild 2.122b ergeben sich ebenso wie beim Umkehrverstärker fallende Arbeitsgeraden (Gl. (2.123)). Falls sie die Verstärkerkennlinie im

![](images/page_131_image_8.jpg)

<details>
<summary>text_image</summary>

u_A
r
u_E
</details>

Abb. 2.129: Abhängigkeit der Gesamtverstärkung des Umkehrverstärkers vom Widerstandsverhältnis $r = R _ { 2 } / _ { R _ { 1 } }$

Bereich linearer Verstärkung schneiden $( u _ { \mathrm { D } } = u _ { \mathrm { A } } \big / _ { \nu _ { 0 } } )$ , so wird mit $r = R _ { 4 } \big / _ { R _ { 3 } }$

$$
v = \frac {u _ {\mathrm{A}}}{u _ {\mathrm{E}}} = \frac {1 + r}{1 + \frac {1 + r}{v _ {0}}} \tag {2.127a}
$$

und

$$
\lim _ {\nu_ {0} \to \infty} \frac {u _ {\mathrm{A}}}{u _ {\mathrm{E}}} = 1 + r \tag {2.127b}
$$

oder für $\nu _ { 0 } \rightarrow$ ∞ einfach

$$
\frac {u _ {\mathrm{A}}}{u _ {\mathrm{E}}} \approx 1 + r, \tag {2.127c}
$$

was man auch hier direkt aus der Annahme $u _ { \mathrm { D } } \approx 0$ herleiten kann (Bild 2.130a).

Die Gl. (2.127a) zeigt, dass auch beim Elektrometerverstärker ebenso wie beim Umkehrverstärker der Betrag der Gesamtverstärkung v mit r zunimmt (Bild 2.131a), wobei die Grenzen für die Gültigkeit der Gleichung selbstverständlich ebenfalls bei $U _ { \mathrm { A m a x } }$ und $U _ { \mathrm { A m i n } }$ liegen (Bild 2.131b).

Falls $\nu _ { 0 }$ sehr groß ist, kann die Gesamtverstärkung v beim Elektrometerverstärker den Wert 1 nicht unterschreiten, vgl. Gl. (2.127c). Für die Grenzen $U _ { \mathrm { E u } }$ und $U _ { \mathrm { E 0 } }$ , zwischen denen $u _ { \mathrm { E } }$ linear verstärkt wird, gilt:

$$
U _ {\mathrm{Eu}} = \frac {1 + \frac {1 + r}{v _ {0}}}{1 + r} U _ {\mathrm{Amin}} \approx \frac {1}{1 + r} U _ {\mathrm{Amin}} \tag {2.128a}
$$

$$
U _ {\mathrm{Eo}} = \frac {1 + \frac {1 + r}{v _ {0}}}{1 + r} U _ {\mathrm{Amax}} \approx \frac {1}{1 + r} U _ {\mathrm{Amax}}. \tag {2.128b}
$$

**Anmerkung** Das Zusammenspiel des Verstärkers mit dem Rückkopplungsnetzwerk beschreibt man bei nichtinvertierender Gegenkopplung mit Hilfe eines Rückkopplungs-Zweitores (Bild 2.130b), an dessen Eingang die Verstärkerausgangsspannung $u _ { \mathrm { A } }$ liegt und das den Übertragungsfaktor k hat. Im Bereich linearer Verstärkung $( u _ { \mathrm { a } } = \nu _ { 0 } u _ { \mathrm { D } } )$ gilt wegen $u _ { \mathrm { E } } = u _ { \mathrm { D } } + k u _ { \mathrm { A } }$

$$
u _ {\mathrm{E}} = \frac {u _ {\mathrm{A}}}{v _ {0}} + k u _ {\mathrm{A}} \quad u n d \quad \frac {u _ {\mathrm{A}}}{u _ {\mathrm{E}}} = \frac {v _ {0}}{1 + k v _ {0}}.
$$

## 2.9.4.2 Mitkopplungsschaltungen

## Invertierende Mitkopplung

In Bild 2.132b sind Arbeitsgeraden der Schaltung in Bild 2.132a für verschiedene Werte $u _ { \mathrm { E } }$ eingezeichnet (Gl. (2.122)). Geht man davon aus, dass zunächst $u _ { \mathrm { E } } = u _ { \mathrm { E 1 } }$ ist, so gilt im einzigen Schnittpunkt $\mathrm { V K L / A G }$ , den es in diesem Fall gibt, $u _ { \mathrm { A } } = U _ { \mathrm { A m a x } }$

Erhöht man $u _ { \mathrm { E } }$ bis zum Wert $u _ { \mathrm { E } }   =   u _ { \mathrm { E } 4 }$ , so bleibt $u _ { \mathrm { A } } = U _ { \mathrm { A m a x } }$ . Geht man über $u _ { \mathrm { E 4 } }$ hinaus, so wird nur noch ein Schnittpunkt $\mathrm { V K L / A G }$ bei $u _ { \mathrm { A } } = U _ { \mathrm { A m i n } }$ möglich. Überschreitet $u _ { \mathrm { E } }$ den Wert $u _ { \mathrm { E 4 } }$ , so springt $u _ { \mathrm { A } }$ von $U _ { \mathrm { A m a x } }$ auf $U _ { \mathrm { A m i n } } , u _ { \mathrm { E 4 } }$ wird mit $U _ { \mathrm { E a b } }$ bezeichnet. Vermindert man danach $u _ { \mathrm { E } }$ wieder, so bleibt $u _ { \mathrm { A } } = U _ { \mathrm { A m i n } }$ , bis $u _ { \mathrm { E } }$ den Wert

a

![](images/page_133_image_3.jpg)

<details>
<summary>text_image</summary>

uE
uD ≈ 0↓
+
-
iN = 0
R3
R4
uA
u3 ≈ uE
ua
uA/u3 = (R3 + R4)/R3; [ua/ue ≈ (R3 + R4)/R3] = 1 + r
</details>

b)

![](images/page_133_image_5.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph LR
  Input["uE"] --> A["Ausgang"]
  A --> B["Rückkopplungs-Zweitor"]
  B --> C["R4"]
  C --> D["Eingang"]
  D --> E["k = (R3/R3+R4) = xG"]
  E --> F["uA = v0uD"]
```
</details>

Abb. 2.130: Elektrometerverstärker.

a)

![](images/page_133_chart_8.jpg)

<details>
<summary>line</summary>

| uE | uA |
| --- | --- |
| < U_E u | U_A min |
| U_E u | 0 |
| U_E o | U_A max |
| > U_E o | U_A max |
</details>

b)

![](images/page_133_chart_10.jpg)

<details>
<summary>line</summary>

| Category | uA (Curve 1) | uA (Curve 2) | uA (Curve 3) | uA (Curve 4) |
| --- | --- | --- | --- | --- |
| Leftmost point | U_A min | — | — | — |
| Center intersection | 0 | 0 | 0 | 0 |
| Rightmost point | U_A max | U_A max | U_A max | U_A max |
</details>

Abb. 2.131: Gesamtverstärkung $u _ { \mathsf { A } } = f _ { } ( u _ { \mathsf { E } } )$ des Elektrometerverstärkers.

![](images/page_134_image_2.jpg)

Abb. 2.132: Invertierender Schmitt-Trigger: a) Schaltung; b) Kennlinie.

![](images/page_134_chart_4.jpg)

<details>
<summary>wireframe</summary>

| Parameter | Description |
| --- | --- |
| uA | Output Voltage (Vertical axis) |
| uE | Input Voltage (Horizontal axis) |
| U_Amax | Maximum Output Voltage threshold |
| U_Eauf | Upper reference voltage level |
| U_Eab | Lower reference voltage level |
| U_Amin | Minimum Output voltage threshold |
</details>

Abb. 2.133: Schalthysterese beim invertierenden Schmitt-Trigger.

$u _ { \mathrm { E } 2 }$ erreicht hat. Erst wenn $u _ { \mathrm { E } 2 }$ unterschritten wird, ist nur noch ein Schnittpunkt $\mathrm { V K L / A G }$ bei $u _ { \mathrm { A } } = U _ { \mathrm { A m a x } }$ möglich. Unterschreitet $u _ { \mathrm { E } }$ den Wert $u _ { \mathrm { E } 2 }$ , so springt $u _ { \mathrm { A } }$ von $U _ { \mathrm { A m i n } }$ auf $U _ { \mathrm { A m a x } } ,   u _ { \mathrm { E } 2 }$ wird mit $U _ { \mathrm { E a u f } }$ bezeichnet.

Falls also $u _ { \mathrm { E } }$ im Bereich $U _ { \mathrm { E a b } }   <   u _ { \mathrm { E } }   <   U _ { \mathrm { E a u f } }$ liegt, kann $u _ { \mathrm { A } }$ je nach Vorzustand den Wert $U _ { \mathrm { A m a x } }$ oder $U _ { \mathrm { A m i n } }$ annehmen. Dieses Hysterese-Verhalten ist in Bild 2.133 dargestellt.

Die Berechnung von $U _ { \mathrm { E a u f } }$ ergibt sich aus der folgenden Überlegung: Direkt vor dem Aufwärtssprung der Ausgangsspannung $u _ { \mathrm { A } }$ ist

$$
u _ {\mathrm{E}} = U _ {\mathrm{Eauf}}, \quad u _ {\mathrm{A}} = U _ {\mathrm{Amin}}, \quad u _ {\mathrm{D}} = U _ {\mathrm{Amin}} / v _ {0}.
$$

In Bild 2.132b sieht man, dass die Arbeitsgerade mit $u _ { \mathrm { E } } = U _ { \mathrm { E a u f } }$ durch $P _ { \mathbf { u } }$ geht und $P _ { \mathbf { u } }$ die Koordinaten $U _ { \mathrm { A m i n } } / \nu _ { 0 }$ und $U _ { \mathrm { A m i n } }$ hat. Dies setzt man in die Arbeitsgeradengleichung (2.122) ein, so dass mit $r = R _ { 4 } \big / _ { R _ { 3 } }$ gil<sup>t</sup>:

$$
U _ {\mathrm{A} \min} = (1 + r) \frac {U _ {\mathrm{A} \min}}{\nu_ {0}} + (1 + r) U _ {\mathrm{E} \text {auf}}
$$

$$
U _ {\mathrm{Eauf}} = U _ {\mathrm{Amin}} \frac {1 - \frac {1 + r}{v _ {0}}}{1 + r} \approx \frac {1}{1 + r} U _ {\mathrm{Amin}}. \tag {2.129a}
$$

Entsprechend ergibt sich aus der Betrachtung des Punktes $P _ { 0 } ,$ durch den die Arbeitsgerade beim Anwachsen von $u _ { \mathrm { E } }$ direkt vor dem $u _ { \mathrm { A } } { \mathrm { - } } \mathbf { A }$ bwärtssprung hindurchgeht,

$$
U _ {\mathrm{Eab}} = U _ {\mathrm{Amax}} \frac {1 - \frac {1 + r}{v _ {0}}}{1 + r} \approx \frac {1}{1 + r} U _ {\mathrm{Amax}}. \tag {2.129b}
$$

Die Näherungsgleichungen gelten unter der Voraussetzung, dass $\nu _ { 0 }$ sehr groß ist.

## Nichtinvertierende Mitkopplung

In Bild 2.134b sind die Arbeitsgeraden der Schaltung in Bild 2.134a eingezeichnet (Gl. (2.119)). Für $u _ { \mathrm { E } } = u _ { \mathrm { E 1 } }$ gibt es nur einen Schnittpunkt $\mathrm { V K L / A G }$ (bei $u _ { \mathrm { A } } = U _ { \mathrm { A m i n } }$ Wächst $\begin{array} { r } { \pmb { u } _ { \mathrm { E } }   \mathtt { a m } , } \end{array}$ , so kommt es für $u _ { \mathrm { E } } = u _ { \mathrm { E } 4 }$ zum Aufwärtssprung der Ausgangsspannung $u _ { \mathrm { A } }$ . Zum Abwärtssprung kommt es dann erst wieder, wenn $u _ { \mathrm { E } }$ auf den Wert $u _ { \mathrm { E } } = u _ { \mathrm { E } 2 }$ sinkt. Dieses Hystereseverhalten des Verlaufes $u _ { \mathrm { A } } = f ( u _ { \mathrm { E } } )$ ist in Bild 2.135 dargestellt.

Direkt vor dem Aufwärtssprung der Ausgangsspannung $u _ { \mathrm { A } }$ ist

$$
u _ {\mathrm{E}} = U _ {\mathrm{Eauf}}, \quad u _ {\mathrm{A}} = U _ {\mathrm{Amin}}, \quad u _ {\mathrm{D}} = \frac {U _ {\mathrm{Amin}}}{\nu_ {0}}.
$$

Eingesetzt in die Arbeitsgeradengleichung (2.119) folgt mit $r = R _ { 2 } \big / _ { R _ { 1 } }$

$$
U _ {\mathrm{A} \min} = (1 + r) \frac {U _ {\mathrm{A} \min}}{\nu_ {0}} - r U _ {\mathrm{E} \text {auf}}
$$

$$
U _ {\mathrm{Eauf}} = - \frac {1 - \frac {1 + r}{v _ {0}}}{r} U _ {\mathrm{Amin}} \approx - \frac {U _ {\mathrm{Amin}}}{r}. \tag {2.130a}
$$

a)

![](images/page_136_image_3.jpg)

<details>
<summary>text_image</summary>

E
R₁
P
R₂
A
uE
uD
+
-
N
uA
</details>

![](images/page_136_image_4.jpg)

<details>
<summary>text_image</summary>

b)
uA
uE1
uE2
uE3
uE4
uE5
UA max
UA min
uD
</details>

Abb. 2.134: Nichtinvertierender Schmitt-Trigger: a) Schaltung; b) Kennlinie.

Aus der Betrachtung des Abwärtssprunges folgt entsprechend:

$$
U _ {\mathrm{Eab}} = - \frac {1 - \frac {1 + r}{v _ {0}}}{r} U _ {\mathrm{Amax}} \approx - \frac {U _ {\mathrm{Amax}}}{r}. \tag {2.130b}
$$

Die Näherungsgleichungen gelten auch hier unter der Bedingung, dass $\nu _ { 0 }$ sehr groß ist. Vergleicht man die Gln. (2.126a) mit (2.130b) sowie (2.126b) mit (2.130a), so zeigt sich, dass für $\nu _ { 0 } \rightarrow$ ∞ beim Vertauschen von P und N in Schaltung 2.122d $U _ { \mathrm { E a u f } }$ zu $U _ { \mathrm { E 0 } }$ und $U _ { \mathrm { E a b } }$ zu $U _ { \mathrm { E u } }$ wird. Aus dem Vergleich der Gln. (2.128a) mit (2.129a) sowie (2.128b) mit (2.129b) geht hervor, dass für $\nu _ { 0 } \rightarrow$ ∞ beim Vertauschen von P und N in Schaltung 2.122c $U _ { \mathrm { E a u f } }$ zu $U _ { \mathrm { E u } }$ und $U _ { \mathrm { E a b } }$ zu $U _ { \mathrm { E 0 } }$ wird.

![](images/page_137_chart_2.jpg)

<details>
<summary>wireframe</summary>

| Feature | Description |
| --- | --- |
| uA | Output Voltage (Vertical Axis) |
| uE | Input Voltage (Horizontal Axis) |
| U_A max | Maximum Voltage Level |
| U_E ab | Lower Bound Voltage Level |
| U_E auf | Upper Bound Voltage Level |
| U_A min | Minimum Voltage Level |
</details>

Abb. 2.135: Schalthysterese beim nichtinvertierenden Schmitt-Trigger.

![](images/page_137_image_4.jpg)

<details>
<summary>text_image</summary>

R1
P
R2
uE
uD
+
-
N
Ur
uA
</details>

Abb. 2.136: Nichtinvertierender Schmitt-Trigger mit Referenzspannung $U _ { \mathrm { { f } } }$

## 2.9.4.3 Dimensionierung von Schmitt-Triggern

Bei den Mitkopplungsschaltungen in den Bildern 2.132 und 2.134 kann man z. B. für $u _ { \mathrm { E } }   =   0$ nicht ohne weiteres angeben, wie groß $u _ { \mathrm { A } }$ wird. Ist bei der Schaltung 2.134 zunächst $u _ { \mathrm { E } } > U _ { \mathrm { E a u f } }$ (Bild 2.135) und vermindert man $u _ { \mathrm { E } }$ auf den Wert $u _ { \mathrm { E } } = 0 ,$ , so ergibt sich $u _ { \mathrm { A } } = U _ { \mathrm { A m a x } }$ . Ist dagegen zunächst $u _ { \mathrm { E } } < U _ { \mathrm { E a b } }$ und erhöht man dann $u _ { \mathrm { E } }$ auf den Wert $u _ { \mathrm { E } } = 0$ , so ergibt sich $u _ { \mathrm { A } } = U _ { \mathrm { A m i n } }$ . Die Schaltung besitzt also eine Eigenschaft, die man als **Selbsthaltung** oder Hysterese bezeichnet, in Analogie zu dem Zusammenhang, der die magnetischen Feldgrößen H und B im Eisen miteinander verknüpft.

Das Spannungsteilerverhältnis $r ~ ( R _ { 2 } \big / _ { R _ { 1 } }$ bzw. $R _ { 4 } / _ { R _ { 3 } } )$ legt die Breite der Hystereseschleife fest und eine hinzugefügte Referenzspannung $U _ { \mathrm { r } }$ (Bild 2.136) verschiebt diese Schleife nach links oder rechts. Man kann also auch die Lage und die Breite der (Schalt-)Hysterese vorgeben und daraus die Werte $r$ und $U _ { \mathrm { r } }$ berechnen; so kommt man zu Dimensionierungsvorschriften für Mitkopplungsschaltungen mit Schalthysterese, die auch als Schmitt-Trigger bezeichnet werden.

## Nichtinvertierender Schmitt-Trigger

Für den Knoten P (Schaltung in Bild 2.136) gilt entsprechend den Regeln der Knotenanalyse (mit $G _ { 1 } = { ^ { 1 } / _ { R _ { 1 } } } ,   G _ { 2 } = { ^ { 1 } / _ { R _ { 2 } } } )$

$$
- G _ {1} u _ {\mathrm{E}} + (G _ {1} + G _ {2}) (u _ {\mathrm{D}} + u _ {\mathrm{r}}) - G _ {2} u _ {\mathrm{A}} = 0. \tag {2.131}
$$

Direkt vor dem Aufwärtssprung von $u _ { \mathrm { A } }$ ist

$$
u _ {\mathrm{E}} = U _ {\mathrm{Eauf}}, \quad u _ {\mathrm{A}} = U _ {\mathrm{Amin}}, \quad u _ {\mathrm{D}} = U _ {\mathrm{Amin}} / v _ {0}. \tag {2.132a,b,c}
$$

Wenn man sich auf den Fall $\nu _ { 0 } \rightarrow$ ∞ beschränkt, so gilt statt Gl. (2.132c) $u _ { \mathrm { D } } \approx 0$ . Setzt man dies und die Gln. (2.132a,b) in die Arbeitsgeradengleichung (2.131) ein, so wird

$$
- G _ {1} U _ {\mathrm{Eauf}} + (G _ {1} + G _ {2}) U _ {\mathrm{r}} - G _ {2} U _ {\mathrm{Amin}} = 0. \tag {2.133a}
$$

Entsprechend führt die Betrachtung des Abwärtssprunges von $u _ { \mathrm { A } }$ zu

$$
- G _ {1} U _ {\mathrm{Eab}} + (G _ {1} + G _ {2}) U _ {\mathrm{r}} - G _ {2} U _ {\mathrm{Amax}} = 0. \tag {2.133b}
$$

Multiplikation der Gln. (2.133) mit $R _ { 2 }$ liefert

$$
\begin{array}{l} - \left(\frac {R _ {2}}{R _ {1}}\right) U _ {\mathrm{Eauf}} + \left(1 + \frac {R _ {2}}{R _ {1}}\right) U _ {\mathrm{r}} - U _ {\mathrm{Amin}} = 0 (2.134a) \\ - \left(\frac {R _ {2}}{R _ {1}}\right) U _ {\mathrm{Eab}} + \left(1 + \frac {R _ {2}}{R _ {1}}\right) U _ {\mathrm{r}} - U _ {\mathrm{Amax}} = 0. (2.134b) \\ \end{array}
$$

Sind $U _ { \mathrm { r } }$ und $R _ { 2 } / _ { R _ { 1 } }$ gegeben, so kann man die Gln. (2.134) als Bestimmungsgleichungen für $U _ { \mathrm { E a u f } }$ und $U _ { \mathrm { E a b } }$ benutzen:

$$
U _ {\mathrm{Eauf}} = \left(1 + \frac {R _ {1}}{R _ {2}}\right) U _ {\mathrm{r}} - \frac {R _ {1}}{R _ {2}} U _ {\mathrm{Amin}}, \tag {2.135a}
$$

$$
U _ {\mathrm{Eab}} = \left(1 + \frac {R _ {1}}{R _ {2}}\right) U _ {\mathrm{r}} - \frac {R _ {1}}{R _ {2}} U _ {\mathrm{Amax}}. \tag {2.135b}
$$

Falls aber $U _ { \mathrm { E a u f } }$ und UE b $U _ { \mathrm { E a b } }$ vorgegeben werden, so können die Gln. (2.134) zur Bestimmung von $U _ { \mathrm { r } }$ und $R _ { 2 } / _ { R _ { 1 } }$ die<sup>nen</sup>:

$$
\frac {R _ {2}}{R _ {1}} = \frac {U _ {\mathrm{A} \max} - U _ {\mathrm{A} \min}}{U _ {\mathrm{E} \text {auf}} - U _ {\mathrm{E} \text {ab}}}, \tag {2.136a}
$$

$$
U _ {\mathrm{r}} = \frac {U _ {\mathrm{A} \max} U _ {\mathrm{E} \text {auf}} - U _ {\mathrm{A} \min} U _ {\mathrm{E} \text {ab}}}{(U _ {\mathrm{A} \max} + U _ {\mathrm{E} \text {auf}}) - (U _ {\mathrm{A} \min} + U _ {\mathrm{E} \text {ab}})}. \tag {2.136b}
$$

## Beispiel 2.37: Schalthysterese eines nichtinvertierenden Schmitt-Triggers.

In der Schaltung in Bild 2.136 sind die beiden Widerstände gegeben. Für die Verstärkerkennlinie des Operationsverstärkers gilt

$$
U _ {\mathrm{A} \max} = 1 0 \mathrm{V}, U _ {\mathrm{A} \min} = - 1 0 \mathrm{V}, v _ {0} = 1 0 ^ {5}.
$$

![](images/page_139_image_2.jpg)

Abb. 2.137: Asymmetrische Schalthysterese bei nichtinvertierender Mitkopplung.

Abkürzung: $R _ { 2 } / _ { R _ { 1 } } = r .$

Die Kennlinien $u _ { \mathrm { A } } = f ( u _ { \mathrm { E } } )$ sollen skizziert werden für

$$
\mathrm{a)} U _ {\mathrm{r}} = 0, \mathrm{b)} U _ {\mathrm{r}} = 5 \mathrm{V}, \mathrm{c)} U _ {\mathrm{r}} = 1 0 \mathrm{V}.
$$

Hierbei sind jeweils die Fälle $r = 1$ und $r = 2$ darzustellen.

## Lösung:

Die Gln. (2.135) ergeben die in Bild 2.137 ablesbaren Verläufe.

## Invertierender Schmitt-Trigger

Für den Knoten P (Schaltung in Bild 2.138) gilt (mit $G _ { 3 } = 1 / R _ { 3 } , \; G _ { 4 } = 1 / R _ { 4 }$

$$
\begin{array}{l} - G _ {3} U _ {\mathrm{r}} + (G _ {3} + G _ {4}) u _ {\mathrm{P}} - G _ {4} u _ {\mathrm{A}} = 0 \\ - G _ {3} U _ {\mathrm{r}} + (G _ {3} + G _ {4}) (u _ {\mathrm{E}} + u _ {\mathrm{D}}) - G _ {4} u _ {\mathrm{A}} = 0. \tag {2.137} \\ \end{array}
$$

Direkt vor dem Aufwärtssprung der Ausgangsspannung UA $u _ { \mathrm { A } }$ gelten auch hier die Gln. (2.132a,b) und mit $\nu _ { 0 } \to \infty$ auch $u _ { \mathrm { D } } \approx 0$

Eingesetzt in die Arbeitsgeradengleichung (2.137) ergibt sich dann

$$
- G _ {3} U _ {\mathrm{r}} + (G _ {3} + G _ {4}) U _ {\mathrm{Eauf}} - G _ {4} U _ {\mathrm{Amin}} = 0 \tag {2.138a}
$$

und entsprechend aus der Betrachtung des Abwärtssprunges von $u _ { \mathrm { A } }$

$$
- G _ {3} U _ {\mathrm{r}} + (G _ {3} + G _ {4}) U _ {\mathrm{Eab}} - G _ {4} U _ {\mathrm{Amax}} = 0. \tag {2.138b}
$$

Die Multiplikation der Gln. (2.138) mit $R _ { 4 }$ führt zu

$$
- \frac {R _ {4}}{R _ {3}} U _ {\mathrm{r}} + \left(1 + \frac {R _ {4}}{R _ {3}}\right) U _ {\mathrm{Eauf}} - U _ {\mathrm{Amin}} = 0 \tag {2.139a}
$$

$$
- \frac {R _ {4}}{R _ {3}} U _ {\mathrm{r}} + \left(1 + \frac {R _ {4}}{R _ {3}}\right) U _ {\mathrm{Eab}} - U _ {\mathrm{Amax}} = 0. \tag {2.139b}
$$

Sind $U _ { \mathrm { r } }$ und $R _ { 4 } / _ { R _ { 3 } }$ gegeben, so kann man die Gln. (2.139) als Bestimmungsgleichungen für $U _ { \mathrm { E a u f } }$ und $U _ { \mathrm { E a b } }$ benutzen:

$$
U _ {\mathrm{Eauf}} = \frac {U _ {\mathrm{Amin}} + \frac {R _ {4}}{R _ {3}} U _ {\mathrm{r}}}{1 + \frac {R _ {4}}{R _ {3}}} , \tag {2.140a}
$$

$$
U _ {\mathrm{Eab}} = \frac {U _ {\mathrm{Amax}} + \frac {R _ {4}}{R _ {3}} U _ {\mathrm{r}}}{1 + \frac {R _ {4}}{R _ {3}}} . \tag {2.140b}
$$

Werden dagegen $U _ { \mathrm { E a u f } }$ und $U _ { \mathrm { E a b } }$ vorgegeben, so kann das Gleichungspaar (2.139) zur Bestimmung von $U _ { \mathrm { r } }$ und $R _ { 4 } / _ { R _ { 3 } }$ die<sup>nen</sup>:

$$
\frac {R _ {4}}{R _ {3}} = \frac {U _ {\mathrm{A} \max} - U _ {\mathrm{A} \min}}{U _ {\mathrm{E} \mathrm{ab}} - U _ {\mathrm{E} \mathrm{auf}}} - 1, \tag {2.141a}
$$

$$
U _ {\mathrm{r}} = \frac {U _ {\mathrm{A} \max} U _ {\mathrm{E} \text {auf}} - U _ {\mathrm{A} \min} U _ {\mathrm{E} \text {ab}}}{(U _ {\mathrm{A} \max} + U _ {\mathrm{E} \text {auf}}) - (U _ {\mathrm{A} \min} + U _ {\mathrm{E} \text {ab}})} . \tag {2.141b}
$$

## 2.9.4.4 Anwendungen des Umkehrverstärkers

Die Verbindung des Ausgangs mit dem invertierenden Eingang (Umkehrverstärker-Prinzip, invertierende Gegenkopplung) ist in vielen wichtigen Schaltungen enthalten. Beispiele hierfür sind der Umkehraddierer und der Subtrahierer.

![](images/page_140_image_15.jpg)

<details>
<summary>text_image</summary>

uE
Ur
=
R3
P
uD
+
-
R4
uP
uA
</details>

Abb. 2.138: Invertierender Schmitt-Trigger mit Referenzspannung $U _ { \mathrm { r } }$

![](images/page_141_image_2.jpg)

<details>
<summary>text_image</summary>

E0
R10
E1
R11
R2
A
uE0
uE1
E2
R12
N
iN
+
-
uD
uA
uE2
</details>

Abb. 2.139: Umkehraddierer.

## Umkehraddierer

In der Schaltung in Bild 2.139 ergibt sich für den Knoten N mit $i _ { \mathrm { N } } = 0$ aus der Knotenanalyse:

$$
- \frac {u _ {\mathrm{E0}}}{R _ {1 0}} - \frac {u _ {\mathrm{E1}}}{R _ {1 1}} - \frac {u _ {\mathrm{E2}}}{R _ {1 2}} + \left(\frac {1}{R _ {1 0}} + \frac {1}{R _ {1 1}} + \frac {1}{R _ {1 2}} + \frac {1}{R _ {2}}\right) (- u _ {\mathrm{D}}) - \frac {u _ {\mathrm{A}}}{R _ {2}} = 0.
$$

Im Bereich linearer Verstärkung, d. h. für $U_{ Amin } < u_{ A } < U_{ Amax }$ , gilt $u _ { \mathrm { D } } = u _ { \mathrm { A } } / v _ { 0 }$ , mit $\nu _ { 0 } \rightarrow$ ∞ also $u _ { \mathrm { D } } \approx 0$ , so dass dann

$$
u _ {\mathrm{A}} = - \left(\frac {R _ {2}}{R _ {1 0}} u _ {\mathrm{E0}} + \frac {R _ {2}}{R _ {1 1}} u _ {\mathrm{E1}} + \frac {R _ {2}}{R _ {1 2}} u _ {\mathrm{E2}}\right) \tag {2.142}
$$

wird. Die Ausgangsspannung ist also eine (mit −1 multiplizierte) Summe aller drei Eingangsspannungen, wobei diese mit den Faktoren $R _ { 2 } / _ { R _ { 1 0 } }$ usw. bewertet werden. Setzt man $R _ { 1 0 } = R _ { 1 1 } = R _ { 1 2 } = R _ { 2 }$ , so werden alle drei Gewichtsfaktoren gleich 1:

$$
u _ {\mathrm{A}} = - (u _ {\mathrm{E0}} + u _ {\mathrm{E1}} + u _ {\mathrm{E2}})  . \tag {2.143}
$$

Wenn der Verstärker im linearen Bereich $( u _ { \mathrm { D } } = u _ { \mathrm { A } } \big / _ { \nu _ { 0 } } )$ arbeitet und überdies $\nu _ { 0 } \to \infty$ so wird das Potential des invertierenden Eingangs N praktisch auf Null festgehalten. Dadurch werden die Eingänge $\mathtt { E } _ { 0 } , \mathtt { E } _ { 1 } , \mathtt { E } _ { 2 }$ voneinander entkoppelt. Selbstverständlich kann die Zahl n der Eingänge größer als drei sein. Gl. (2.142) wird dann entsprechend durch weitere Summanden ergänzt.

## Subtrahierer

Die Knotenanalyse liefert für die Knoten N und P (Bild 2.140):

|  | $u_{E0}$ | $u_{E1}$ | $u_{N}$ | $u_{P}$ | $u_{A}$ |  |
| --- | --- | --- | --- | --- | --- | --- |
| N | $-G_1$ | 0 | $G_1 + G_2$ | 0 | $-G_2$ | 0 |
| P | 0 | $-G_3$ | 0 | $G_3 + G_4$ | 0 | 0 |

![](images/page_142_image_2.jpg)

<details>
<summary>text_image</summary>

E0 R1 N R2 A
uE0 iN -
uD iP +
P R3 P R4 uA
E1 uE1
</details>

Abb. 2.140: Subtrahierer.

(mit der Voraussetzung $i_{\mathrm{N}} = 0, i_{\mathrm{P}} = 0$ für den idealen Operationsverstärker). Aus Gl. (2.144b) folgt

$$
u _ {\mathrm{P}} = \frac {G _ {3}}{G _ {3} + G _ {4}} u _ {\mathrm{E1}}
$$

und wegen $u _ { \mathrm { D } } = 0$ ist $u _ { \mathrm { N } } = u _ { \mathrm { P } }$ , also

$$
u _ {\mathrm{N}} = \frac {G _ {3}}{G _ {3} + G _ {4}} u _ {\mathrm{E1}}.
$$

Setzt man dies in Gl. (2.144a) ein, so entsteht

$$
\begin{array}{l} - G _ {1} u _ {\mathrm{E0}} + (G _ {1} + G _ {2}) \frac {G _ {3}}{G _ {3} + G _ {4}} u _ {\mathrm{E1}} = G _ {2} u _ {\mathrm{A}} \\ - u _ {\mathrm{E0}} + \frac {1 + \frac {R _ {1}}{R _ {2}}}{1 + \frac {R _ {3}}{R _ {4}}} u _ {\mathrm{E1}} = \frac {R _ {1}}{R _ {2}} u _ {\mathrm{A}} \\ u _ {\mathrm{A}} = \frac {R _ {2}}{R _ {1}} \left[ \frac {1 + \frac {R _ {1}}{R _ {2}}}{1 + \frac {R _ {3}}{R _ {4}}} u _ {\mathrm{E} 1} - u _ {\mathrm{E} 0} \right]. \tag {2.145} \\ \end{array}
$$

Wählt man $R _ { 3 } \big / _ { R _ { 4 } }   =   R _ { 1 } \big / _ { R _ { 2 } }$ , so erhalten beide Eingangsspannungen den gleichen Gewichtsfaktor:

$$
u _ {\mathrm{A}} = \frac {R _ {2}}{R _ {1}} \left[ u _ {\mathrm{E} 1} - u _ {\mathrm{E} 0} \right]. \tag {2.146}
$$

Es wird also die mit $R _ { 2 } / _ { R _ { 1 } }$ multiplizierte Differenz zweier Spannungen gebildet.

## 2.9.5 Kombination von invertierender mit nichtinvertierender Gegenkopplung

Bei einem Umkehrverstärker (Bild 2.126) entsteht die Gegenkopplung durch die Verbindung A–N, das invertierende Verhalten durch die Verbindung E–N. Verbindet man zusätzlich E mit P (Bild 2.141), so hängt es von den beiden Spannungsteilerverhältnissen

$$
\frac {R _ {1}}{R _ {1} + R _ {2}} \quad \text {und} \quad \frac {R _ {3}}{R _ {3} + R _ {4}}
$$

ab, ob invertierendes oder nichtinvertierendes Gegenkopplungsverhalten überwiegt: siehe Beispiel 2.37.

## Beispiel 2.38: Kombination von invertierender mit nichtinvertierender Gegenkopplung.

In Bild 2.141 sind die vier Widerstände gegeben. Für die Verstärkungskennlinie $u _ { \mathrm { a } } = f ( u _ { \mathrm { D } } )$ des Operationsverstärkers gilt:

$$
U _ {\mathrm{A} \max} = 1 0 \mathrm{V}; \qquad U _ {\mathrm{A} \min} = - 1 0 \mathrm{V}; \qquad \nu_ {0} = 1 0 ^ {5}.
$$

Zweckmäßige Abkürzungen:

$$
r _ {\mathrm{N}} = \frac {R _ {2}}{R _ {1}}, \qquad r _ {\mathrm{P}} = \frac {R _ {4}}{R _ {3}}.
$$

a) Unter der Voraussetzung $u _ { \mathrm { D } } \approx 0   ( d .   h .$ für den Bereich linearer Verstärkung) ist $u _ { a } / _ { u _ { e } }$ zu berechnen.
b) Die Übertragungskennlinien $u _ { \mathrm { A } } = f ( u _ { \mathrm { E } } )$ sollen für folgende fünf Fälle skizziert werden:

$$
r _ {\mathrm{P}} = \infty (d. h. R _ {3} = 0)
$$

$$
r _ {\mathrm{P}} = 2; 1; 0, 5; 0.
$$

In allen Fällen ist $r _ { \mathrm { N } } = 1$

## Lösung:

**a)** Wegen $u _ { \mathrm { D } } = 0$ wird $u _ { 1 } = u _ { 3 }$ , mit der Spannungsteilerregel also

$$
\frac {u _ {\mathrm{A}}}{u _ {\mathrm{E}}} = \frac {r _ {\mathrm{P}} - r _ {\mathrm{N}}}{1 + r _ {\mathrm{P}}} . \tag {2.147}
$$

![](images/page_143_image_19.jpg)

<details>
<summary>text_image</summary>

E
R1
u1
uE - uA
R2
A
u3
N
-
uD
+
P
R3
uA
R4
</details>

Abb. 2.141: Kombination von invertierender mit nichtinvertierender Gegenkopplung.

![](images/page_144_chart_2.jpg)

<details>
<summary>line</summary>

| uE | uA (rP=0) | uA (rP=0.5) | uA (rP=1) | uA (rP=2) | uA \((rP \to \infty)\) |
| --- | --- | --- | --- | --- | --- |
| 0 | -10 V | -10 V | -10 V | 0 V | 0 V |
| ~0.5 | -10 V | -10 V | 0 V | 0 V | 0 V |
| ~1.0 | -10 V | -10 V | 0 V | 0 V | 0 V |
| ~1.5 | -10 V | -10 V | 0 V | 0 V | 0 V |
| ~2.0 | -10 V | -10 V | 0 V | 0 V | 0 V |
| ~2.5 | -10 V | -10 V | 0 V | 0 V | 0 V |
| ~3.0 | -10 V | -10 V | 0 V | 0 V | 0 V |
| ~3.5 | -10 V | -10 V | 0 V | 0 V | 0 V |
| ~4.0 | -10 V | -10 V | 0 V | 0 V | 0 V |
| ~4.5 | -10 V | -10 V | 0 V | 0 V | 0 V |
| ~5.0 | -10 V | -10 V | 0 V | 0 V | 0 V |
| ~5.5 | -10 V | -10 V | 0 V | 0 V | 0 V |
| ~6.0 | -10 V | -10 V | 0 V | 0 V | 0 V |
| ~6.5 | -10 V | -10 V | 0 V | 0 V | 0 V |
| ~7.0 | -10 V | -10 V | 0 V | 0 V | 0 V |
| ~7.5 | -10 V | -10 V | 0 V | 0 V | 0 V |
| ~8.0 | -10 V | -10 V | 0 V | 0 V | 0 V |
| ~8.5 | -10 V | -10 V | 0 V | 0 V | 0 V |
| ~9.0 | -10 V | -10 V | 0 V | 0 V | 0 V |
| ~9.5 | -10 V | -10 V | 0 V | 0 V | 0 V |
| ~10.0 | -10 V | -10 V | 0 V | 0 V | 0 V |
| ~1.5 | -10 V | -10 V | 0 V | 0 V | 0 V |
| ~2.0 | -10 V | -10 V | 0 V | 0 V | 0 V |
| ~2.5 | -10 V | -10 V | 0V (rP=2) | 0V (rP=2) | 0V (rP→\(\infty)\) |
| ~3.0 | -10 V | -10 V | +10V (rP=2) | +10V (rP=2) | +10V (rP→\(\infty)\) |
| ~3.5 | -10 V | -10V (rP=2) | +10V (rP=2) | +10V (rP=2) | +10V (rP→\(\infty)\) |
| ~4.0 | -10V (rP=2) | +10V (rP=2) | +10V (rP=2) | +10V (rP=2) | +10V (rP→\(\infty)\) |
| ~4.5 | -10V (rP=2) | +10V (rP=2) | +10V (rP=2) | +10V (rP=2) | +10V (rP→\(\infty)\) |
| ~5.0 | -10V (rP=2) | +10V (rP=2) | +10V (rP=2) | +10V (rP=2) | +10V (rP→\(\infty)\) |
| ~5.5 | -10V (rP=2) | +10V (rP=2) | +10V (rP=2) | +10V (rP=2) | +10V (rP→\(\infty)\) |
| ~6.0 | -10V (rP=2) | +10V (rP=2) | +10V (rP=2) | +10V (rP=2) | +10V (rP→\(\infty)\) |
| ~6.5 | -10V (rP=2) | +10V (rP=2) | +10V (rP=2) | +10V (rP=2) | +10V (rP→\(\infty)\) |
| ~7.0 | -10V (rP=2) | +10V (rP=2) | +10V (rP=2) | +10V (rP=2) | +10V (rP→\(\infty)\) |
</details>

Abb. 2.142: Gesamtverstärkung der Schaltung 2.141.

![](images/page_144_image_4.jpg)

<details>
<summary>text_image</summary>

E
R1
uN
R2
A
N
uD
+
-
R5
uE
P
R3
uP
R4
uA
</details>

Abb. 2.143: Bipolares Koeffizientenglied.

$$
\begin{array}{l} \frac {R _ {1}}{R _ {1} + R _ {2}} (u _ {\mathrm{E}} - u _ {\mathrm{A}}) = \frac {R _ {3}}{R _ {3} + R _ {4}} u _ {\mathrm{E}} \\ \frac {1}{1 + r _ {\mathrm{N}}} (u _ {\mathrm{E}} - u _ {\mathrm{A}}) = \frac {1}{1 + r _ {\mathrm{P}}} u _ {\mathrm{E}} \\ \end{array}
$$

b)

| $r_{\mathrm{P}}$ | $\infty$ | 2 | 1 | 0,5 | 0 |
| --- | --- | --- | --- | --- | --- |
| $u_{\mathrm{A}}/u_{\mathrm{E}}$ | 1 | 1/3 | 0 | -1/3 | -1 |

Diese Tabelle ergibt sich aus Gl. (2.147) mit $r _ { \mathrm { N } } = 1$ ; grafisch dargestellt ist das Ergebnis in Bild 2.142.

Das Bild 2.142 zeigt, dass in der Schaltung 2.141 die Gesamtverstärkung zwar positiv oder negativ werden kann, dass ihr Betrag aber nie größer als 1 wird, wenn $r _ { \mathrm { N } } = 1$ ist. Wählt man für $r _ { \mathrm { N } }$ einen beliebigen Wert, so ändert sich auch der Betrag der im Fall $r _ { \mathrm { P } } = 0$ erreichbaren, negativen Gesamtverstärkung: $u _ { \mathrm { A } } / _ { u _ { \mathrm { E } } } = - r _ { \mathrm { N } }$ . D. h. die Schaltung ist bei $r _ { \mathrm { P } } = 0$ ein einfacher Umkehrverstärker. Der Höchstwert, den $u _ { \mathrm { A } } / _ { u _ { \mathrm { E } } }$ err<sup>eicht</sup> (für $r _ { \mathrm { P } } \to \infty )$ , ist bei allen Werten $r _ { \mathrm { N } }$ der gleiche: $u _ { \mathrm { A } } / _ { u _ { \mathrm { E } } } = 1$

Diese Einschränkung gilt für das bipolare Koeffizientenglied nicht (Bild 2.143, durch Hinzufügung von $R _ { 5 }$ aus Bild 2.141 hervorgegangen). Im Beispiel 2.38 wird die Gesamtverstärkung eines bipolaren Koeffizientengliedes berechnet.

## Beispiel 2.39: Bipolares Koeffizientenglied.

In Bild 2.143 sind die Widerstände $R _ { 1 } \ldots R _ { 5 }$ gegeben. Für die Verstärkungskennlinie $u _ { \mathrm { A } } = f ( u _ { \mathrm { D } } )$ des Operationsverstärkers gilt:

$$
U _ {\mathrm{A} \max} = 1 0 \mathrm{V} = - U _ {\mathrm{A} \min}; \quad \nu_ {0} = 1 0 ^ {5}.
$$

a) Unter der Voraussetzung $u _ { \mathrm { D } } \approx 0 ,$ , d. h. für den Bereich linearer Verstärkung, ist $u _ { \mathrm { A } } / _ { u _ { \mathrm { E } } }$ zu berechnen.
b) In dieses Ergebnis sollen die Abkürzungen

$$
a = \frac {R _ {4}}{R _ {3} + R _ {4}} \quad u n d \quad r = \frac {R _ {2}}{R _ {1}}
$$

sowie die nur für $r \geq 1$ erfüllbare Bedingung $R _ { 5 } = R _ { 2 } \big / ( r - 1 )$ eingeführt werden.

c) Die Übertragungskennlinien $u _ { \mathrm { A } } = f ( u _ { \mathrm { E } } )$ sollen mit $r = 1 0$ für die fünf Fälle

$$
a = 0; 0, 2 5; 0, 5; 0, 7 5; 1
$$

skizziert werden.

## Lösung:

**a)** Knotenanalyse für die Punkte N und P:

|  | $u_{\text{E}}$ | $u_{\text{N}}$ | $u_{\text{P}}$ | $u_{\text{A}}$ |  |
| --- | --- | --- | --- | --- | --- |
| N | $-G_1$ | $G_1 + G_2 + G_5$ | 0 | $-G_2$ | 0 |
| P | $-G_3$ | 0 | $G_3 + G_4$ | 0 | 0 |

Aus Gl. (2.148b) folgt mit $u _ { \mathrm { N } } = u _ { \mathrm { P } } \left( \mathrm { a u s } \; u _ { \mathrm { D } } = 0 \right)$

$$
u _ {\mathrm{N}} = \frac {G _ {3}}{G _ {3} + G _ {4}} u _ {\mathrm{E}}.
$$

Setzt man dies in Gl. (2.148a) ein und berücksichtigt die Vorschrift $R _ { 5 } = R _ { 2 } \big / ( r - 1 )$ , die übrigens gleichbedeutend ist mit $G _ { 5 } = G _ { 1 } - G _ { 2 }$ , so entsteht

$$
u _ {\mathrm{E}} \left[ - G _ {1} + \frac {G _ {3}}{G _ {3} + G _ {4}} (G _ {1} + G _ {2} + G _ {5}) \right] = G _ {2} u _ {\mathrm{A}},
$$

$$
\frac {u _ {\mathrm{A}}}{u _ {\mathrm{E}}} = - \frac {G _ {1}}{G _ {2}} + \frac {G _ {3}}{G _ {3} + G _ {4}} \left[ \frac {G _ {1}}{G _ {2}} + 1 + \frac {G _ {5}}{G _ {2}} \right].
$$

**b)** mit den Abkürzungen a und r:

$$
\frac {u _ {\mathrm{A}}}{u _ {\mathrm{E}}} = - r + a (r + 1 + r - 1) = \underline {{r (2 a - 1)}}. \tag {2.149}
$$

![](images/page_146_chart_2.jpg)

<details>
<summary>line</summary>

| uE/V | uA/V (a=0) | uA/V (a=0.25) | uA/V (a=0.5) | uA/V (a=0.75) | uA/V (a=1) |
| --- | --- | --- | --- | --- | --- |
| -2 | 0 | 0 | 0 | 0 | 0 |
| 0 | 0 | 0 | 0 | 0 | 0 |
| 2 | 0 | 0 | 0 | 0 | 0 |
| 2.5 | 10 | ~9.5 | ~8.5 | ~6.5 | ~-3.5 |
| 3 | 10 | 10 | 10 | 10 | 10 |
</details>

Abb. 2.144: Spannungsverstärkung des bipolaren Koeffizientengliedes.

c) Mit $r = 1 0$ wird $u _ { \mathrm { A } } / _ { u _ { \mathrm { E } } } = 1 0   ( 2 a - 1 )$ :

| a | 0 | 0,25 | 0,5 | 0,75 | 1 |
| --- | --- | --- | --- | --- | --- |
| $u_{\text{A}}/u_{\text{E}}$ | -10 | -5 | 0 | 5 | 10 |

Die grafische Darstellung hierzu ist in Bild 2.144 zu finden.

## 2.9.6 Kombination von invertierender mit nichtinvertierender Mitkopplung

Bei der Schaltung in Bild 2.134a entsteht die Mitkopplung durch die Verbindung $\mathrm { A } { - } \mathrm { P } ,$ das nichtinvertierende Verhalten durch die Verbindung E–P. Verbindet man außerdem E mit N (Bild 2.145), so hängt es auch hier (Beispiel 2.39) von den beiden Spannungsteilerverhältnissen

$$
\frac {R _ {1}}{R _ {1} + R _ {2}} \quad \text {und} \quad \frac {R _ {3}}{R _ {3} + R _ {4}}
$$

bzw. von $R _ { 2 } / _ { R _ { 1 } }$ und $R _ { 4 } / _ { R _ { 3 } }$ ab, ob invertierendes oder nichtinvertierendes Verhalten überwiegt.

## Beispiel 2.40: Kombination von invertierender mit nichtinvertierender Mitkopplung.

Für die Verstärkungskennlinie des in Bild 2.145 dargestellten Operationsverstärkers gilt:

$$
U _ {\mathrm{A} \max} = - U _ {\mathrm{A} \min} = 8 \mathrm{V}; \quad \nu_ {0} = 1 0 ^ {5}.
$$

Die vier Widerstände sind gegeben; als Abkürzungen sollen verwendet werden:

$$
r _ {\mathrm{P}} = \frac {R _ {2}}{R _ {1}}; \quad r _ {\mathrm{N}} = \frac {R _ {4}}{R _ {3}}.
$$

Die Funktion $u _ { \mathrm { A } } = f ( u _ { \mathrm { E } } )$ ist zu skizzieren für

a) $r _ { \mathrm { P } } = 1 ;   r _ { \mathrm { N } } = 9$
b) $r _ { \mathrm { P } } = 1 ;   r _ { \mathrm { N } } = 1 / 9$
c) Für die zulässigen Spannungen an den Eingängen P, N gilt: $| u _ { \mathbb { P } } | < U _ { \mathbb { S } } ; | u _ { \mathbb { N } } | < U _ { \mathbb { S } }$ . Auf welchen Bereich muss $u _ { \mathrm { E } }$ daher in den Fällen a und b beschränkt werden?

**Lösung:**

$$
\text {Aus} \quad u _ {\mathrm{D}} + u _ {1} = u _ {3}
$$

$$
u _ {\mathrm{D}} + \frac {R _ {1}}{R _ {1} + R _ {2}} (u _ {\mathrm{E}} - u _ {\mathrm{A}}) = \frac {R _ {3}}{R _ {3} + R _ {4}} u _ {\mathrm{E}}
$$

ergibt sich die Arbeitsgeradengleichung

$$
u _ {\mathrm{A}} = \frac {r _ {\mathrm{N}} - r _ {\mathrm{p}}}{1 + r _ {\mathrm{N}}} u _ {\mathrm{E}} + (1 + r _ {\mathrm{p}}) u _ {\mathrm{D}}. \tag {2.150}
$$

Direkt vor dem Aufwärtssprung gilt $u_{\mathrm{D}} = 0, u_{\mathrm{A}} = U_{\mathrm{Amin}}, u_{\mathrm{E}} = U_{\mathrm{Eand}}$ . Gl. (2.150) stellt zwischen diesen Werten den Zusammenhang

$$
U _ {\mathrm{A} \min} = \frac {r _ {\mathrm{N}} - r _ {\mathrm{P}}}{1 + r _ {\mathrm{N}}} U _ {\mathrm{E} \text {auf}} \tag {2.151a}
$$

her. Direkt vor dem Abwärtssprung gilt $u_{\mathrm{D}} = 0,   u_{\mathrm{A}} = U_{\mathrm{Amax}},   u_{\mathrm{E}} = U_{\mathrm{Eab}}$ . Zwischen diesen Werten stellt die Gl. (2.150) den Zusammenhang

$$
U _ {\mathrm{A} \min} = \frac {r _ {\mathrm{N}} - r _ {\mathrm{P}}}{1 + r _ {\mathrm{N}}} U _ {\mathrm{E} \mathrm{ab}} \tag {2.151b}
$$

her. Zusammengefasst und nach $U _ { \mathrm { E a u f } }$ bzw. $U _ { \mathrm { E a b } }$ aufgelöst gilt:

$$
U _ {\text {Eauf} \text {(ab)}} = \frac {1 + r _ {\mathrm{N}}}{r _ {\mathrm{N}} - r _ {\mathrm{p}}} U _ {\text {Amin} \text {(max)}} \tag {2.152}
$$

a) $U_{\mathrm{Eauf}}=\frac{1+9}{9-1}U_{\mathrm{Amin}}=\mp10\mathrm{V}.$
b) $U _ { \mathrm { E a u f } } = \frac { 1 + 1 / 9 } { 1 / 9 - 1 } U _ { \mathrm { A m i n } } = \pm 1 0 \mathrm { V } .$

Die Ergebnisse a) und b) sind in Bild 2.146 zusammengefasst.

![](images/page_147_image_21.jpg)

<details>
<summary>text_image</summary>

E
R1
u1
uE - uA
R2
A
P
+ U_S = 10 V
uD
-
N
u3
R3
R4
-U_S
uA
uE
</details>

Abb. 2.145: Kombination von invertierender mit nichtinvertierender Mitkopplung.

![](images/page_148_image_2.jpg)

Abb. 2.146: Schalthysterese der Schaltung 2.145.

## c) Beschränkung von uE:

Im Fall a) ist der Bereich $-11,1 V  < u_{ E } < 11,1 V$
im Fall b) ist der Bereich $- 1 2   \mathrm { V } < u _ { \mathrm { E } } < 1 2   \mathrm { V }$ zulässig.

Geht man in der Schaltung in Bild 2.145 von einer Leerlaufverstärkung $\nu _ { 0 }$ des Operationsverstärkers aus, die kleiner als das Verhältnis $R _ { 2 } / _ { R _ { 1 } }$ ist, so kommt es trotz der Verbindung A–P und obwohl keine Verbindung A–N existiert, nicht mehr zu Mitkopplungsverhalten. Die Schaltung verhält sich wie eine Gegenkopplungsschaltung, wobei allerdings $\nu > \nu _ { 0 }$ werden kann, was bei den durch die Verbindung A–N entstehenden Gegenkopplungsschaltungen nicht möglich ist. Dort ist immer $| \boldsymbol { v } | < \nu _ { 0 }$ (Beispiel 2.40).

## Beispiel 2.41: Vergrößerung der linearen Verstärkung durch Mitkopplung $( \pmb { v } > \pmb { v } _ { 0 } )$

Für die Schaltung 2.145 soll gelten:

$$
U _ {\mathrm{A} \max} = - U _ {\mathrm{A} \min} = 1 0 \mathrm{V}; \frac {R _ {2}}{R _ {1}} = 5.
$$

Außerdem ist die Abkürzung $a   =   R _ { 4 } / ( R _ { 3 }   +   R _ { 4 } )$ einzuführen. Berechnet und skizziert werden soll $u _ { \mathrm { A } } = f ( u _ { \mathrm { E } } )$ für folgende vier Fälle:

## Lösung:

Aufstellung der Knotengleichungen für N und P (Knotenanalyse):

|  | $u_{\text{E}}$ | $u_{\text{P}}$ | $u_{\text{N}}$ | $u_{\text{A}}$ |  |
| --- | --- | --- | --- | --- | --- |
| P | $-G_1$ | $G_1 + G_2$ | 0 | $-G_2$ | 0 |
| N | $-G_3$ | 0 | $G_3 + G_4$ | 0 | 0 |

Aus Gl. (2.153b) folgt $u _ { \mathrm { N } } = a   u _ { \mathrm { E } }$ . Damit wird

$$
u _ {\mathrm{P}} = u _ {\mathrm{N}} + u _ {\mathrm{D}} = a u _ {\mathrm{E}} + u _ {\mathrm{D}}.
$$

Setzt man dies in die Gl. (2.153a) ein, so erhält man die Gleichung für die Arbeitsgeradenschar:

$$
- G _ {1} u _ {\mathrm{E}} + (G _ {1} + G _ {2}) (a u _ {\mathrm{E}} + u _ {\mathrm{D}}) - G _ {2} u _ {\mathrm{A}} = 0
$$

$$
G _ {2} u _ {\mathrm{A}} = (G _ {1} + G _ {2}) u _ {\mathrm{D}} + [ (G _ {1} + G _ {2}) a - G _ {1} ] u _ {\mathrm{E}}
$$

$$
u _ {\mathrm{A}} = \left(\frac {R _ {2}}{R _ {1}} + 1\right) u _ {\mathrm{D}} + \left[ \left(\frac {R _ {2}}{R _ {1}} + 1\right) a - \frac {R _ {2}}{R _ {1}} \right] u _ {\mathrm{E}} \tag {2.154a}
$$

$$
\text {speziell mit} R _ {2} / _ {R _ {1}} = 5 \text {also:} u _ {\mathrm{A}} = 6 u _ {\mathrm{D}} + (6 a - 5) u _ {\mathrm{E}}. \tag {2.154b}
$$

Die Gl. (2.154a) beschreibt Arbeitsgeraden mit der (positiven) Steigung $R _ { 2 } \big / _ { R _ { 1 } }   +   1$ (Bild 2.147).

Ist $R _ { 2 } / _ { R _ { 1 } } + 1 < \nu _ { 0 }$ (Fall 1), so entsteht Mitkopplungsverhalten. Die Schnittpunkte AG/VKL sind instabil (Abschnitt 2.9.3), falls sie im Bereich $U _ { \mathrm { D u } } < u _ { \mathrm { D } } < U _ { \mathrm { D o } }$ liegen. Ist dagegen $R _ { 2 } / _ { R _ { 1 } } + 1 > \nu _ { 0 }$ (Fall 2), so gibt es immer nur einen Schnittpunkt. Dieser ist auch dann stabil, wenn er im Bereich $U _ { \mathrm { D u } } < u _ { \mathrm { D } } < U _ { \mathrm { D o } }$ liegt. Die Schaltung wirkt dann wie eine Gegenkopplungsschaltung.

Bei Mitkopplungsverhalten $( R _ { 2 } / _ { R _ { 1 } } + 1 < \nu _ { 0 } ;$ Fälle a und b) kommt es zum Abwärtssprung, wenn gilt

$$
u _ {\mathrm{A}} = U _ {\mathrm{Amax}}, u _ {\mathrm{D}} = U _ {\mathrm{Amax}} / v _ {0}, u _ {\mathrm{E}} = U _ {\mathrm{Eab}}.
$$

Setzt man dies in die Arbeitsgeradengleichung ein, so wird

$$
U _ {\mathrm{A} \max} = \left(\frac {R _ {2}}{R _ {1}} + 1\right) \frac {U _ {\mathrm{A} \max}}{\nu_ {0}} + \left[ \left(\frac {R _ {2}}{R _ {1}} + 1\right) a - \frac {R _ {2}}{R _ {1}} \right] U _ {\mathrm{Eab}} \tag {2.155}
$$

$$
U _ {\text {Eab} \text {(auf)}} = U _ {\underset {\text {(min)}} {\operatorname{Amax}}} \frac {1 - \frac {1}{v _ {0}} \left(\frac {R _ {2}}{R _ {1}} + 1\right)}{a \left(\frac {R _ {2}}{R _ {1}} + 1\right) - \frac {R _ {2}}{R _ {1}}} . \tag {2.156}
$$

![](images/page_149_chart_16.jpg)

<details>
<summary>line</summary>

| uD | uA (Upper Bound) | uA (Lower Bound) |
| --- | --- | --- |
| 0 | U_A_max | U_A_min |
| U_D_u | U_D_u | — |
| U_D_o | U_D_o | — |
| >U_D_o | U_A_max | U_A_min |
</details>

Abb. 2.147: Mitkopplungs-Arbeitsgeraden unterschiedlicher Steigung.

Zum Aufwärtssprung kommt es bei $u_{\mathrm{A}}=U_{\mathrm{Amin}}, u_{\mathrm{D}}=U_{\mathrm{Amin}} / _{V_{0}}, u_{\mathrm{E}}=U_{\mathrm{Eand}}$ . Das führt zu einer entsprechenden Formel wie für $U _ { \mathrm { E a b } }$ (untere Indizes in Gl. (2.156)).

Bei Gegenkopplungsverhalten $( R _ { 2 } / _ { R _ { 1 } } + 1 > \nu _ { 0 }$ : Fälle c und d) gilt im Bereich linearer Verstärkung $u _ { \mathrm { D } } = u _ { \mathrm { A } } \big / _ { \nu _ { 0 } }$ . Setzt man dies in die Gl. (2.154a) ein, so entsteht (ähnlich wie Gl. (2.155)):

$$
u _ {\mathrm{A}} = \left(\frac {R _ {2}}{R _ {1}} + 1\right) \frac {u _ {\mathrm{A}}}{v _ {0}} + \left[ \left(\frac {R _ {2}}{R _ {1}} + 1\right) a - \frac {R _ {2}}{R _ {1}} \right] u _ {\mathrm{E}}
$$

und daraus

$$
v = \frac {a \left(\frac {R _ {2}}{R _ {1}} + 1\right) - \frac {R _ {2}}{R _ {1}}}{1 - \frac {1}{\nu_ {0}} \left(\frac {R _ {2}}{R _ {1}} + 1\right)} \quad \text {fur} \quad U _ {\mathrm{A} \min} <   u _ {\mathrm{A}} <   U _ {\mathrm{A} \max}. \tag {2.157}
$$

a) Es gilt $R_{2}/_{R_{1}} + 1 = 6 < \nu_{0} \rightarrow$ ∞: Mitkopplungsverhalten. Die Gl. (2.156) ergibt $U_{\mathrm{E\;auf}} = -U_{\mathrm{E\;ab}} = 2\mathrm{V}.$
b) Auch hier ist $R_{2}/_{R_{1}}+1=6<\nu_{0}\rightarrow$ ∞: Mitkopplungsverhalten. $U_{\mathrm{E\;auf}} = -U_{\mathrm{E\;ab}} = 5\mathrm{~V}.$ Die Kennlinien $u _ { \mathrm { A } } = f ( u _ { \mathrm { E } } )$ sind in Bild 2.148a für die Fälle a und b zusammengefasst.
c) Es ist $R _ { 2 } / _ { R _ { 1 } } + 1 = 6 > \nu _ { 0 } = 3$ : Gegenkopplungsverhalten.
Für den Bereich der linearen Verstärkung ergibt sich aus Gl. (2.157): $u _ { \mathrm { A } } / _ { u _ { \mathrm { E } } } = 5$
d) Hier ist ebenfalls $R _ { 2 } / _ { R _ { 1 } } + 1 = 6 > \nu _ { 0 } = 3 ;$ Gegenkopplungsverhalten. $u _ { \mathrm { A } } / _ { u _ { \mathrm { E } } } = 2$

Für die Fälle c und d sind die Kennlinien $u _ { \mathrm { A } } = f ( u _ { \mathrm { E } } )$ in Bild 2.148b zusammengefasst. Im Fall c wird die Gesamtverstärkung größer als die Leerlaufverstärkung: $u _ { \mathrm { A } } \big / _ { u _ { \mathrm { E } } } > \nu _ { 0 }$ Der gleiche Effekt tritt auch im Beispiel 2.41d auf. Wenn $\nu _ { 0 } = 1 0 \big / _ { 3 }$ ist, wird $u _ { \mathrm { A } } / _ { u _ { \mathrm { E } } } \infty$

![](images/page_150_image_14.jpg)

Abb. 2.148: Mit- und Gegenkopplungsverhalten der Schaltung 2.145.

## 2.9.7 Kombination von Gegenkopplung und Mitkopplung

## 2.9.7.1 Mit- und Gegenkopplungsfaktor

In Schaltungen, in denen A sowohl mit P als auch mit N verbunden ist (Bild 2.149), hängt es (falls $\nu _ { 0 } \to \infty )$ nur von den Spannungsteiler-Verhältnissen

$$
x _ {\mathrm{M}} = \frac {R _ {1}}{R _ {1} + R _ {2}} \quad (\text {Mitkopplungsfaktor}) \tag {2.158a}
$$

und

$$
x _ {\mathrm{G}} = \frac {R _ {3}}{R _ {3} + R _ {4}} \quad (\text {Gegenkopplungsfaktor}) \tag {2.158b}
$$

ab, ob der Mit- oder der Gegenkopplungseffekt überwiegt:

$$
x _ {\mathrm{M}} > x _ {\mathrm{G}}: \text {Mitkopplungsverhalten}
$$

$$
x _ {\mathrm{M}} <   x _ {\mathrm{G}}: \text {Gegenkopplungsverhalten.}
$$

Dies wird im Beispiel 2.41 gezeigt. Es wird außerdem vorgeführt, wie es sich auswirkt, wenn die Leerlaufverstärkung $\nu _ { 0 }$ nicht unendlich groß wird. In diesem Fall kann die Gegenkopplung überwiegen, obwohl $x _ { \mathrm { M } } > x _ { \mathrm { G } }$ ist.

## Beispiel 2.42: Gesamtverstärkung bei Kombination von Gegen- und Mitkopplung.

Die Kennlinie $u _ { \mathrm { A } } = f ( u _ { \mathrm { D } } )$ des Operationsverstärkers $( V K L )$ in Bild 2.149 hat die Kennwerte $U_{ Amax } = +10 V$ und $U_{ Amin } = -10 V;$ für die Leerlaufverstärkung $u _ { \mathrm { A } } \big / _ { u _ { \mathrm { D } } } = \nu _ { 0 }   g i l t { \mathrm { : } }$

$$
1 \leq v _ {0} \leq 1 0 ^ {6}.
$$

a) Berechnen Sie die Gesamtverstärkung $\nu _ { \mathrm { g e s } } = u _ { \mathrm { A } } / _ { u _ { \mathrm { E } } }$ und berücksichtigen Sie dabei, dass $\nu _ { 0 }$ grundsätzlich nur endlich groß ist. Hierbei sind die Abkürzungen $x _ { M }$ und $x _ { \mathrm { G } }$ wie in den Gln. (2.158) einzuführen. Es soll – ohne weitere Untersuchung – vorausgesetzt werden, dass die Schaltung linear verstärkt und der Operationsverstärker nur in dem Bereich arbeitet, in dem $u _ { \mathrm { A } } = v _ { 0 } u _ { \mathrm { D } }$ ist.
b) Skizzieren Sie die Kennlinien $u_{\mathrm{A}} = f(u_{\mathrm{E}})   f_{\mathrm{M}} r   x_{\mathrm{M}} = 0,5;   x_{\mathrm{G}} = 0,8$ in den Fällen $\nu _ { 0 } = 1 0 ^ { 6 } ; \; 1 0 ; \; ^ { 1 0 } / _ { 3 } ; \; 2 ; \; 1$

![](images/page_151_image_18.jpg)

<details>
<summary>text_image</summary>

E
iE
R1
P
R2
A
uE
uD
+
-
A
uA
R3
N
R4
</details>

Abb. 2.149: Kombination von Mit- und Gegenkopplungsschaltung.

c) Skizzieren Sie die Kennlinien $u_{\mathrm{A}} = f(u_{\mathrm{E}})   f_{\mathrm{M}}   r_{\mathrm{M}} = 0,5;   x_{\mathrm{G}} = 0,5$ in den Fällen $\nu _ { 0 } = 1 0 ^ { 6 } ; \; 1 0 ; \; 1 0 / _ { 3 } ; \; 2 ; \; 1$
d) Skizzieren Sie die Kennlinien $u_{\mathrm{A}} = f(u_{\mathrm{E}})   f_{\mathrm{M}}   r_{\mathrm{M}} = 0,5;   x_{\mathrm{G}} = 0,2$ in den Fällen $\nu _ { 0 }   =   1 0 / _ { 3 } ; 2$ ; 1. Wie verhält sich die Schaltung mit $x _ { \mathrm { M } } = 0 , 5$ und $x _ { G } = 0 , 2$ , falls $\nu _ { 0 } > 1 0 \slash { } _ { 3 }$ wird, z. B. $\nu _ { 0 } = 1 0 ?$

## Lösung:

**a)** Mit Hilfe der Knotenanalyse stellen wir die Gleichungen für die Knoten P und N (Schaltung 2.149) auf:

|  | $u_{\text{E}}$ | $u_{\text{P}}$ | $u_{\text{N}}$ | $u_{\text{A}}$ |  |
| --- | --- | --- | --- | --- | --- |
| P | $-G_1$ | $G_1 + G_2$ | 0 | $-G_2$ | 0 |
| N | 0 | 0 | $G_3 + G_4$ | $-G_4$ | 0 |

Aus Gl. (2.159b) ergibt sich: $\boldsymbol { u } _ { \mathrm { N } } = G _ { 4 } \big / _ { ( G _ { 3 } \mathrm { ~ + ~ } G _ { 4 } ) } \boldsymbol { u } _ { \mathrm { A } } = \boldsymbol { x } _ { \mathrm { G } } \boldsymbol { u } _ { \mathrm { A } }$ . Setzt man dies in die Gl. (2.159a) ein und berücksichtigt

$$
u _ {\mathrm{P}} = u _ {\mathrm{N}} + u _ {\mathrm{D}} = u _ {\mathrm{N}} + \frac {u _ {\mathrm{A}}}{\nu_ {0}},
$$

so erhält man

$$
\begin{array}{l} - G _ {1} u _ {\mathrm{E}} + (G _ {1} + G _ {2}) \left(x _ {G} u _ {\mathrm{A}} + \frac {u _ {\mathrm{A}}}{v _ {0}}\right) - G _ {2} u _ {\mathrm{A}} = 0 \\ - \frac {R _ {2}}{R _ {1}} u _ {\mathrm{E}} + \left(\frac {R _ {2}}{R _ {1}} + 1\right) \left(x _ {\mathrm{G}} + \frac {1}{v _ {0}}\right) u _ {\mathrm{A}} - u _ {\mathrm{A}} = 0 \\ \end{array}
$$

$$
u _ {\mathrm{A}} \left[ \frac {1}{x _ {\mathrm{M}}} \left(x _ {\mathrm{G}} + \frac {1}{v _ {0}}\right) - 1 \right] = \frac {R _ {2}}{R _ {1}} u _ {\mathrm{E}} = \frac {1 - x _ {\mathrm{M}}}{x _ {\mathrm{M}}} u _ {\mathrm{E}}
$$

$$
\frac {u _ {\mathrm{A}}}{u _ {\mathrm{E}}} = \frac {1 - x _ {\mathrm{M}}}{x _ {\mathrm{G}} - x _ {\mathrm{M}} + \frac {1}{v _ {0}}} = \frac {v _ {0} (1 - x _ {\mathrm{M}})}{v _ {0} (x _ {\mathrm{G}} - x _ {\mathrm{M}}) + 1}. \tag {2.160a,b}
$$

Eliminiert man aus den Gln. (2.159) und $u _ { \mathrm { P } } = u _ { \mathrm { N } } + u _ { \mathrm { D } }$ die Spannungen $u _ { \mathrm { P } }$ und $u _ { \mathrm { N } }$ , so erhält man die Arbeitsgeradengleichung

$$
u _ {\mathrm{A}} = \frac {1 - x _ {\mathrm{M}}}{x _ {\mathrm{G}} - x _ {\mathrm{M}}} u _ {\mathrm{E}} - \frac {u _ {\mathrm{D}}}{x _ {\mathrm{G}} - x _ {\mathrm{M}}} . \tag {2.161}
$$

Sie zeigt, dass die Arbeitsgeraden $u _ { \mathrm { A } } = f ( u _ { \mathrm { D } } )$ für $x _ { \mathrm { G } } > x _ { \mathrm { M } }$ negative Steigung haben, dass dann also die Gegenkopplung überwiegt. Für $x _ { \mathsf { G } } < x _ { \mathsf { M } }$ ist die Steigung der Arbeitsgeraden positiv: dann überwiegt im Falle $\nu _ { 0 } \rightarrow$ ∞ der Mitkopplungseffekt. Er überwiegt auch, falls $\nu _ { 0 }$ nur endlich ist, und zwar so lange, wie $\nu _ { 0 }$ größer als die Steigung der Arbeitsgeraden ist (Bild 2.147).

Dies geht auch aus einer Betrachtung der linearen Gesamtverstärkung $u _ { \mathrm { A } } / _ { u _ { \mathrm { E } } }$ der Gl. (2.160a) hervor. Der Nenner

$$
x _ {\mathrm{G}} - x _ {\mathrm{M}} + \frac {1}{\nu_ {0}}
$$

wird für $x _ { \mathrm { M } } - x _ { G } = 1 \big / \nu _ { 0 }$ gleich Null und die Gesamtverstärkung damit theoretisch unendlich groß. Hier haben wir es offensichtlich mit dem Grenzfall für die Gültigkeit der

Gl. (2.160a) zu tun. Wird $x _ { \mathrm { M } } > x _ { \mathrm { G } } = 1 \big / _ { \nu _ { 0 } } ,$ so kann demnach die Gl. (2.160a) nicht mehr gelten und der Mitkopplungseffekt dominiert nun.

Die Arbeitsgeradengleichung (2.161) bestätigt außerdem, dass die Steigung der $\mathrm { A G } ^ { 1 } / ( x _ { \mathrm { M } } - x _ { \mathrm { G } } )$ ist, in dem beschriebenen Grenzfall also Leerlaufverstärkung $\nu _ { 0 }$ und AG-Steigung übereinstimmen:

$$
v _ {0} = \frac {1}{x _ {\mathrm{M}} - x _ {\mathrm{G}}} . \tag {2.162}
$$

Betrachtet man daraufhin die Fälle b, c und d der Aufgabenstellung, so sieht man, dass in allen Fällen der Nenner $x _ { \mathrm { G } } - x _ { \mathrm { M } } + 1 \big / \nu _ { 0 }$ pos<sup>itiv</sup> ist und daher Gl. (2.160) anwendbar bleibt. Nur für $x_{\mathrm{M}} = 0,5;x_{\mathrm{G}} = 0,2;v_{0} = 10$ ist $x _ { \mathsf { G } } - x _ { \mathsf { M } } + 1 \big / _ { \nu _ { 0 } } < 0$ und somit Gl. (2.160) wegen des Überwiegens des Mitkopplungseffektes nicht anwendbar.

**b)** Mit den für $x _ { \mathrm { G } } , x _ { \mathrm { M } }$ und $\nu _ { 0 }$ gegebenen Werten ergibt sich aus Gl. (2.160b):

$$
\frac {u _ {\mathrm{A}}}{u _ {\mathrm{E}}} = \frac {0 , 5 v _ {0}}{0 , 3 v _ {0} + 1}
$$

| $v_{0}$ | $10^{6}$ | 10 | 10/3 | 2 | 1 |
| --- | --- | --- | --- | --- | --- |
| $u_{A}/u_{E}$ | 5/3 | 5/4 | 5/6 | 5/8 | 5/13 |

In Bild 2.150 sind die Funktionen $u _ { \mathrm { A } } = f ( u _ { \mathrm { E } } )$ grafisch dargestellt.

$\mathbf { c } )$ Mit den für $x _ { \mathrm { G } } , x _ { \mathrm { M } }$ und $\nu _ { 0 }$ gegebenen Werten ergibt sich aus Gl. (2.160b):

$$
\frac {u _ {\mathrm{A}}}{u _ {\mathrm{E}}} = 0, 5 \nu_ {0}
$$

| $v_{0}$ | $10^{6}$ | 10 | 10/3 | 2 | 1 |
| --- | --- | --- | --- | --- | --- |
| $u_{\text{A}}/u_{\text{E}}$ | $5 \cdot 3^{5}$ | 5 | 5/3 | 1 | 0,5 |

Die Ergebnisse sind in Bild 2.151 dargestellt.

$$
\frac {u _ {\mathrm{A}}}{u _ {\mathrm{E}}} = \frac {0 , 5 v _ {0}}{1 - 0 , 3 v _ {0}}
$$

| $v_{0}$ | 10/3 | 2 | 1 |
| --- | --- | --- | --- |
| $u_{A}/u_{E}$ | $\infty$ | 5/2 | 5/7 |

![](images/page_153_chart_16.jpg)

<details>
<summary>line</summary>

| uE (V) | uA (V) |
| --- | --- |
| -20 | 10 |
| -10 | 10 |
| 0 | 0 |
| 10 | 10 |
| 20 | 10 |
</details>

Abb. 2.150: Spannungsverstärkung der Schaltung 2.149 bei überwiegender Gegenkopplung.

**d)** In diesem Fall ist $x _ { \mathrm { G } }   <   x _ { \mathrm { M } _ { 1 } }$ , so dass die Gl. (2.160) nur für $\nu _ { 0 }   <   1 \big / ( x _ { \mathrm { M } } - x _ { \mathrm { G } } )   =   1 0 \big / 3$ anwendbar bleibt (Bild 2.152a).

Wollte man die Formel (2.160) auch auf den Fall $x_{\mathrm{M}} = 0,5; x_{\mathrm{G}} = 0,2; v_{0} = 10$ anwenden, so erhielte man $u _ { \mathrm { A } } / _ { u _ { \mathrm { E } } } = - 2 , 5$ , also eine negative Gesamtverstärkung bei einer nichtinvertierenden Schaltung. Nichtinvertierend, weil E mit P, aber nicht mit N verbunden ist (Bild 2.149). Das ist ein deutlicher Hinweis darauf, dass der Wert −2,5 nicht stimmen kann.

Im Anschluss an die Arbeitsgeradengleichung (2.161) ist dargestellt worden, dass nun der Mitkopplungseffekt überwiegt. Es entsteht die in Abschnitt 2.9.3 beschriebene Hysterese mit dem Aufwärtssprung bei

$$
u _ {\mathrm{A}} = U _ {\mathrm{A} \min}, \quad u _ {\mathrm{D}} = \frac {U _ {\mathrm{A} \min}}{\nu_ {0}}, \quad u _ {\mathrm{E}} = U _ {\mathrm{E} \text {auf}}.
$$

Setzt man diese Werte in Gl. (2.161) ein, so wird

$$
\begin{array}{l} U _ {\mathrm{Amin}} = \frac {1 - x _ {\mathrm{M}}}{x _ {\mathrm{G}} - x _ {\mathrm{M}}} U _ {\mathrm{Eauf}} - \frac {\frac {U _ {\mathrm{Amin}}}{\nu_ {0}}}{x _ {\mathrm{G}} - x _ {\mathrm{M}}} \\ - 1 0 \mathrm{V} = \frac {1 - 0 , 5}{0 , 2 - 0 , 5} U _ {\mathrm{Eauf}} - \frac {\frac {- 1 0 \mathrm{V}}{1 0}}{0 , 2 - 0 , 5} \\ U _ {\mathrm{Eauf}} = \underline {{4 \mathrm{V}}}. \\ \end{array}
$$

Entsprechend wird $U _ { \mathrm { E a b } } = - 4   \mathrm { V }$ (Bild 2.152b).

**Anmerkung** Praktisch auftreten können kleine Werte $\nu _ { 0 }   z , B _ { \bullet }$ , wenn man Verstärker aus diskreten Bauelementen aufbaut oder statt des Operationsverstärkers einen Elektrometerverstärker (Bild 2.130b) mit kleinem Wert $\nu _ { \mathrm { g e s } }$ verwendet.

![](images/page_154_chart_10.jpg)

<details>
<summary>line</summary>

| uE (V) | uA (V) |
| --- | --- |
| -20 | 0 |
| -10 | 0 |
| 0 | 0 |
| 10 | 0 |
| 20 | 0 |
| -20 | 10 |
| -10 | 10 |
| 0 | 10 |
| 10 | 10 |
| 20 | 10 |
| -20 | 10/3 |
| -10 | 10/3 |
| 0 | 10/3 |
| 10 | 10/3 |
| 20 | 10/3 |
| -20 | 1 |
| -10 | 1 |
| 0 | 1 |
| 10 | 1 |
| 20 | 1 |
| -20 | -10 |
| -10 | -10 |
| 0 | -10 |
| 10 | -10 |
| 20 | -10 |
</details>

Abb. 2.151: Spannungsverstärkung der Schaltung 2.149 im Falle $X _ { \mathsf { G } } = X _ { \mathsf { M } }$

![](images/page_155_image_2.jpg)

Abb. 2.152: Spannungsübertragung der Schaltung 2.149 bei überwiegender Mitkopplung.

## 2.9.7.2 Spannungsgesteuerte Stromquelle

In der Schaltung in Bild 2.153 überwiegt die Gegenkopplung in jedem Fall (d. h. auch bei beliebig hoher Leerlaufverstärkung $\nu _ { 0 } )$ die Mitkopplung, denn es gilt

$$
x _ {\mathrm{G}} = \frac {R _ {\mathrm{N}}}{R _ {\mathrm{N}} + a R _ {\mathrm{N}}} = \frac {1}{1 + a} \quad \text {und}
$$

$$
x _ {\mathrm{M}} = \frac {\frac {R _ {\mathrm{P}} R _ {5}}{R _ {\mathrm{P}} + R _ {5}}}{\frac {R _ {\mathrm{P}} R _ {5}}{R _ {\mathrm{P}} + R _ {5}} + a R _ {\mathrm{P}}} = \frac {1}{1 + a \left(1 + \frac {R _ {\mathrm{P}}}{R _ {5}}\right)}; \quad \text {also ist} \quad x _ {\mathrm{G}} > x _ {\mathrm{M}}.
$$

## Beispiel 2.43: Invertierende spannungsgesteuerte Stromquelle (Übersteuerungsgrenzen).

In der Schaltung 2.153 ist die Gegenkopplung stärker als die Mitkopplung. Innerhalb eines bestimmten Bereiches

$$
U _ {\mathrm{Eu}} \leq u _ {\mathrm{E}} \leq U _ {\mathrm{Eo}}
$$

![](images/page_155_image_11.jpg)

<details>
<summary>text_image</summary>

E
RN
N
aRN
uD
+
-
P
A
RP
aRP
R5
i5
uA
uE
</details>

Abb. 2.153: Invertierende spannungsgesteuerte Stromquelle.

kann die Schaltung also linear verstärken. Vereinfachend soll $\nu _ { 0 } \to \infty$ gesetzt werden, so dass $u _ { \mathrm { D } } = 0$ ist, wenn der Verstärker nicht übersteuert wird.

a) Wie hängt beim nichtübersteuerten Verstärker $i _ { 5 }$ von $u _ { \mathrm { E } }$ und den Widerständen ab?
b) Wie hängen die Aussteuerungsgrenzen $U _ { \mathrm { E 0 } }$ und $U _ { \mathrm { E u } }$ von den Widerständen und $U _ { \mathrm { A m a x } }   a b ?$
c) Es sei $a = 1 , R _ { \mathrm { P } } = 1   \mathrm { k } \Omega ;   U _ { \mathrm { E }   \mathrm { o } } = - U _ { \mathrm { E }   \mathrm { u } } = 1   \mathrm { V } .$
Wie groß darf $R _ { 5 }$ höchstens werden, wenn die $f i i r   i _ { 5 }$ unter $a )$ berechnete Gleichung gelten soll?

## Lösung:

**a)** Aufstellung der Gleichungen für die Knoten N und P (Knotenanalyse):

|  | $u_{\text{E}}$ | $u_{\text{N}}$ | $u_{\text{P}}$ | $u_{\text{A}}$ |  |
| --- | --- | --- | --- | --- | --- |
| N | $-G_{\text{N}}$ | $G_{\text{N}} + G_{\text{N}}/a$ | 0 | $-G_{\text{N}}/a$ | 0 |
| P | 0 | 0 | $G_{\text{P}} + G_{\text{P}}/a + G_{5}$ | $-G_{\text{P}}/a$ | 0 |

Aus Gl. (2.163b) folgt

$$
u _ {\mathrm{A}} = a \left(1 + \frac {1}{a} + \frac {G _ {5}}{G _ {\mathrm{P}}}\right) u _ {\mathrm{P}}. \tag {2.163c}
$$

Setzt man dies in die Gl. (2.163a) ein, so wird mit $u _ { \mathrm { N } } = u _ { \mathrm { P } }$

$$
\begin{array}{l} - u _ {\mathrm{E}} + \left[ \left(1 + \frac {1}{a}\right) - \left(1 + \frac {1}{a} + \frac {G _ {5}}{G _ {\mathrm{P}}}\right) \right] u _ {\mathrm{P}} = 0 \\ u _ {\mathrm{P}} = \frac {u _ {\mathrm{E}}}{1 + \frac {1}{a} - \frac {1}{a} - 1 - \frac {G _ {5}}{G _ {\mathrm{P}}}} = - \frac {G _ {\mathrm{P}}}{G _ {5}} u _ {\mathrm{E}} = - \frac {R _ {5}}{R _ {\mathrm{P}}} u _ {\mathrm{E}} \\ \end{array}
$$

und wegen $\boldsymbol { i } _ { 5 } = \boldsymbol { u } _ { \mathrm { P } } \big / _ { R _ { 5 } }$ wird

$$
i _ {5} = - \frac {u _ {\mathrm{E}}}{R _ {\mathrm{p}}} . \tag {2.164}
$$

Betrachtet man $R _ { 5 }$ als Lastwiderstand und $i _ { 5 }$ als den Ausgangsstrom, so ergibt sich das erstaunliche Resultat, dass der Ausgangsstrom zwar zur Eingangsspannung proportional ist, aber vom Widerstandswert $R _ { 5 }$ selbst gar nicht abhängt. Selbstverständlich kann kein Strom vom Betrag $u _ { \mathrm { E } } / _ { R _ { \mathrm { P } } }$ in $R _ { 5 }$ erzwungen werden, wenn $R _ { 5 }$ sehr groß wird $( \mathrm { z .   B .   }   R _ { 5 } \to \infty )$ . Für $R _ { 5 }$ muss es also eine Obergrenze geben, nach deren Überschreiten Gl. (2.164) nicht mehr gelten kann, weil der Verstärker dann nicht mehr im Bereich linearer Verstärkung $[ U _ { \mathrm { D u } } < u _ { \mathrm { D } } < U _ { \mathrm { D o } } ]$ arbeitet und daher die zur Berechnung von Gl. (2.164) vorausgesetzte Annahme $u _ { \mathrm { D } } = 0$ , bzw. $u _ { \mathrm { N } } = u _ { \mathrm { P } }$ , ungültig wird. Außerdem gelten auch – wie schon beim einfachen Umkehrverstärker – für $u _ { \mathrm { E } }$ Grenzen. In welchen Grenzen sich $R _ { \mathrm { P } }$ und $u _ { \mathrm { E } }$ bewegen dürfen, wenn der Verstärker nicht übersteuert werden soll, zeigen die Aufgabenpunkte b und c.

**b)** Aus Gl. (2.163c) und $u _ { \mathrm { P } } = u _ { \mathrm { N } }$ ergibt sich

$$
u _ {\mathrm{N}} = \frac {\frac {1}{a}}{1 + \frac {1}{a} + \frac {G _ {5}}{G _ {\mathrm{P}}}} u _ {\mathrm{A}}.
$$

Setzt man dies in die Gl. (2.163a)

$$
0 = - G _ {\mathrm{N}} U _ {\mathrm{E}} + \left(G _ {\mathrm{N}} + \frac {G _ {\mathrm{N}}}{a}\right) U _ {\mathrm{N}} - \frac {G _ {\mathrm{N}}}{a} U _ {\mathrm{A}}
$$

ein, so erhält man für den linearen Zusammenhang zwischen $u _ { \mathrm { A } }$ und $u _ { \mathrm { E 1 } }$ :

$$
u _ {\mathrm{E}} = \left[ \frac {\frac {1}{a}}{1 + \frac {1}{a} + \frac {G _ {5}}{G _ {\mathrm{P}}}} \left(1 + \frac {1}{a}\right) - \frac {1}{a} \right] u _ {\mathrm{A}} = - \frac {\frac {G _ {5}}{G _ {\mathrm{P}}}}{1 + \frac {1}{a} + \frac {G _ {5}}{G _ {\mathrm{P}}}} \frac {u _ {\mathrm{A}}}{a}
$$

$$
u _ {\mathrm{E}} = \frac {- \frac {R _ {\mathrm{P}}}{R _ {5}}}{1 + a + a \frac {R _ {\mathrm{P}}}{R _ {5}}} u _ {\mathrm{A}}. \tag {2.165}
$$

Speziell an den Grenzen des linearen Verstärkungsbereiches gilt damit

$$
U _ {\mathrm{Eu} _ {(o)}} = \frac {- \frac {R _ {\mathrm{P}}}{R _ {5}}}{1 + a + a \frac {R _ {\mathrm{P}}}{R _ {5}}} U _ {\mathrm{Amax} _ {(\min)}}. \tag {2.166a,b}
$$

**c)** Mit der Abkürzung $r = R _ { \mathrm { P } } \big / _ { R _ { 5 } }$ gilt

$$
\frac {U _ {\mathrm{Eo}}}{- U _ {\mathrm{Amin}}} = \frac {r}{1 + a + a r},
$$

und wegen $-U_{ Amin } = U_{ Amax }$ daher

$$
\frac {U _ {\mathrm{Eo}}}{U _ {\mathrm{Amax}}} = \frac {r}{1 + a + a r}. \tag {2.167}
$$

Mit den Werten $U_{\mathrm{E}0}=1\mathrm{V}, U_{\mathrm{Amax}}=13\mathrm{V}; a=1; R_{\mathrm{P}}=1$ kΩ wird

$$
\frac {1 \mathrm{V}}{1 3 \mathrm{V}} = \frac {r}{1 + 1 + r}
$$

$$
2 + r = 1 3 r; \quad r = R _ {\mathrm{P}} / R _ {5} = 1 / 6
$$

$$
R _ {5} = 6 R _ {\mathrm{P}} = 6 \mathrm{k} \Omega .
$$

Unter den gegebenen Bedingungen darf $R _ { 5 }$ den Wert 6 kΩ nicht überschreiten. Bei größeren Werten kommt es zur Übersteuerung.

## 2.9.7.3 Negativer Eingangswiderstand

Der Eingangswiderstand

$$
R _ {\mathrm{E}} = \frac {u _ {\mathrm{E}}}{i _ {\mathrm{E}}}
$$

der Schaltung in Bild 2.149 kann negativ werden (Beispiel 2.42).

## Beispiel 2.44: Negativ-Impedanz-Konverter (NIC).

$R _ { 1 } , R _ { 2 } , R _ { 3 } , R _ { 4 }$ und $U_{\mathrm{Amax}} = -U_{\mathrm{Amin}} = 12   \mathrm{V}$ sind gegeben. Für die Leerlaufverstärkung soll gelten: $\nu _ { 0 } \to \infty ;$ die Schaltung ist in Bild 2.149 dargestellt.

a) Geben Sie das Spannungsverhältnis $u _ { \mathrm { A } } / _ { u _ { \mathrm { E } } }$ unt<sup>er</sup> der Voraussetzung an, dass die Gegenkopplung überwiegt und der Verstärker nicht übersteuert wird, so dass mit $u _ { \mathrm { D } } \approx 0$ gerechnet werden kann.
Wie hängt in diesem Fall $R _ { \mathrm { E } } = u _ { \mathrm { E } } \big / _ { i _ { \mathrm { E } } }$ von $R _ { 1 } , R _ { 2 } , R _ { 3 } , R _ { 4 }$ ab?
b) Welche Bedingung müssen die Widerstände erfüllen, damit die Gegenkopplung überwiegt?
c) Für die Werte $R_{1}=R_{2}=10 \mathrm{k}\Omega; R_{3}=20 \mathrm{k}\Omega, R_{4}=10$ kΩ überwiegt die Gegenkopplung. Welche Bedingung muss uE erfüllen, damit für diesen Fall der Verstärker nicht übersteuert wird, und wie groß wird hierbei $R _ { \mathrm { E } } ?$
d) Geben sie für den Fall $R_{1}=R_{2}=10 \mathrm{k}\Omega; R_{3}=20 \mathrm{k}\Omega, R_{4}=10 \mathrm{k}\Omega$ den Eingangswiderstand $R _ { \mathrm { E } }   f \ddot { u } r$ zwei Werte von $u _ { \mathrm { E } }   a n ,$ bei denen der Verstärker übersteuert wird.

## Lösung:

**a)** Aus Beispiel 2.42 kann das Ergebnis übernommen werden. Dort war wegen $u _ { \mathrm { D } } \approx 0$

$$
\frac {u _ {\mathrm{A}}}{u _ {\mathrm{E}}} = \frac {1 - x _ {\mathrm{M}}}{x _ {\mathrm{G}} - x _ {\mathrm{M}} + \frac {1}{\nu_ {0}}}.
$$

Setzt man nun für die Leerlaufverstärkung $\nu _ { 0 } \rightarrow$ ∞ ein, so erhält man

$$
\frac {u _ {\mathrm{A}}}{u _ {\mathrm{E}}} = \frac {1 - x _ {\mathrm{M}}}{x _ {\mathrm{G}} - x _ {\mathrm{M}}} . \tag {2.168}
$$

Für den Mitkopplungsfaktor $x _ { M }$ und den Gegenkopplungsfaktor $x _ { \mathrm { G } }$ werden die Definitionen nach Gl. (2.158) verwendet:

$$
x _ {\mathrm{M}} = \frac {R _ {1}}{R _ {1} + R _ {2}} \quad (\text {Mitkopplungsfaktor}),
$$

$$
x _ {\mathrm{G}} = \frac {R _ {3}}{R _ {3} + R _ {4}} \quad \text {(Gegenkopplungsfaktor)}.
$$

Setzt man diese beiden Gleichungen nun in (2.168) ein, so erhält man

$$
\frac {u _ {\mathrm{A}}}{u _ {\mathrm{E}}} = \frac {R _ {2} (R _ {3} + R _ {4})}{R _ {2} R _ {3} - R _ {1} R _ {4}}. \tag {2.169}
$$

Zur Bestimmung des Eingangsstroms $i _ { \mathrm { E } }$ wählt man in Bild 2.149 den Umlauf

$$
0 = - u _ {\mathrm{E}} + i _ {\mathrm{E}} \cdot (R _ {1} + R _ {2}) + u _ {\mathrm{A}}. \tag {2.170}
$$

Man erhält somit

$$
i _ {\mathrm{E}} = \frac {u _ {\mathrm{E}} - u _ {\mathrm{A}}}{R _ {1} + R _ {2}} = \frac {u _ {\mathrm{E}}}{R _ {1} + R _ {2}} \cdot \left[ \frac {x _ {\mathrm{G}} - 1}{x _ {\mathrm{G}} - x _ {\mathrm{M}}} \right] = \frac {R _ {4} \cdot u _ {\mathrm{E}}}{R _ {1} R _ {4} - R _ {2} R _ {3}}. \tag {2.171}
$$

Der Eingangswiderstand wird dann

$$
R _ {\mathrm{E}} = \frac {u _ {\mathrm{E}}}{i _ {\mathrm{E}}} = \frac {R _ {1} R _ {4} - R _ {2} R _ {3}}{R _ {4}}. \tag {2.172}
$$

**b)** Die Gegenkopplung überwiegt für $x _ { \mathrm { G } } > x _ { \mathrm { M } }$ (Beispiel 2.41a), d. h. für

$$
\frac {R _ {3}}{R _ {3} + R _ {4}} > \frac {R _ {1}}{R _ {1} + R _ {2}}
$$

bzw.

$$
\frac {R _ {2}}{R _ {1}} > \frac {R _ {4}}{R _ {3}}. \tag {2.173}
$$

c) Es ist $R _ { 2 } / _ { R _ { 1 } } = 1$ und $R_{4}/_{R_{3}} = 0,5;$ die Bedingung nach Gl. (2.173) ist also erfüllt und die Gl. (2.168) ist anwendbar:

$$
\frac {u _ {\mathrm{A}}}{u _ {\mathrm{E}}} = \frac {1 - \frac {1}{2}}{\frac {2}{3} - \frac {1}{2}} = \underline {{3}}.
$$

Die Ausgangsspannung $u _ { \mathrm { A } }$ erreicht also ihre Grenzen $U_{ Amin } = -12   V$ und $U_{ Amax } = 12   V$ bei $u _ { \mathrm { E } } = \pm 4   \mathrm { V }$ (Bild 2.154). Damit der Verstärker nicht übersteuert wird, muss demnach gelten:

$$
- 4 \mathrm{V} \leq u _ {\mathrm{E}} \leq + 4 \mathrm{V}.
$$

Als Eingangswiderstand ergibt sich $R _ { \mathrm { E } } = - 1 0   \mathrm { k } \Omega$

**d)** Bei Übersteuerung ist $u _ { \mathrm { D } } \neq 0$ und $| u _ { \mathrm { A } } | = 1 2   \mathrm { V } ;$ damit ergibt sich mit $x _ { \mathrm { M } } = 1 / _ { 2 }$ und $x _ { \mathrm { G } } = 2 / _ { 3 }$ aus Gleichung (2.161)

$$
\pm 1 2 \mathrm{V} = \frac {1 - \frac {1}{2}}{\frac {2}{3} - \frac {1}{2}} u _ {\mathrm{E}} - \frac {u _ {\mathrm{D}}}{\frac {2}{3} - \frac {1}{2}} = 3 u _ {\mathrm{E}} - 6 u _ {\mathrm{D}}.
$$

Der Eingangstrom wird dann gemäß Gleichung (2.170)

$$
i _ {\mathrm{E}} = \frac {u _ {\mathrm{E}} - u _ {\mathrm{A}}}{R _ {1} + R _ {2}} = \frac {u _ {\mathrm{E}} \mp 1 2 \mathrm{V}}{2 0 \mathrm{k} \Omega}.
$$

Zum Beispiel ergeben sich für

$$
\begin{array}{l} u _ {\mathrm{E}} = \pm 6 \mathrm{V}: \quad u _ {\mathrm{D}} = \pm 1 \mathrm{V}, \quad i _ {\mathrm{E}} = \mp 0, 3 \mathrm{mA}, \quad R _ {\mathrm{E}} = - 2 0 \mathrm{k} \Omega \quad \text {und} \\ u _ {\mathrm{E}} = \pm 8 \mathrm{V}: \quad u _ {\mathrm{D}} = \pm 2 \mathrm{V}, \quad i _ {\mathrm{E}} = \mp 0, 2 \mathrm{mA}, \quad R _ {\mathrm{E}} = - 4 0 \mathrm{k} \Omega. \\ \end{array}
$$

![](images/page_159_chart_17.jpg)

<details>
<summary>line</summary>

| uE | uA |
| --- | --- |
| -4 V | -12 V |
| 0 V | 0 V |
| 4 V | 12 V |
</details>

Abb. 2.154: Grenzen der linearen Verstärkung eines NIC.