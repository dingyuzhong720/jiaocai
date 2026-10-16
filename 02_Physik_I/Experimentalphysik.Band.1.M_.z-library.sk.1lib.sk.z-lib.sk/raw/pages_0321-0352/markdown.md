Die rasche Dämpfung beim aperiodischen Grenzfall hat eine besondere Bedeutung für technische Anwendungen, bei denen meist unerwünschte Schwingungen des Systems verhindert werden sollen.<sup>19</sup>

## 5.2.4 Die Energie der Schwingungsbewegung

In einem abgeschlossenen System bleibt die Summe aus kinetischer und potenzieller Energie erhalten, also $E _ { \mathrm { g e s a m t } } = E _ { \mathrm { k i n } } + E _ { \mathrm { p o t } } = \mathrm { c o n s t } .$

Wird der harmonische Oszillator daher von außen nicht beeinflusst, so gilt:

1 Ist der ungedämpfte harmonische Oszillator ein abgeschlossenes System, so bleibt seine Gesamtenergie erhalten.

Für die kinetische und die potenzielle Energie des harmonischen Oszillators gilt

$$
E _ {\mathrm{kin}} = \frac {1}{2} m \dot {x} ^ {2}, E _ {\mathrm{pot}} = - \int_ {0} ^ {x} F (x) d x = - \int_ {0} ^ {x} (- k x) d x = \frac {1}{2} k x ^ {2}. \tag {I-5.113}
$$

Der Energiesatz $\frac { 1 } { 2 }   m \dot { x } ^ { 2 } + \frac { 1 } { 2 }   k x ^ { 2 } =$ const. gibt mit $x(t) = A \cos \left( \omega_0 t + \varphi \right)$

$$
\begin{array}{l} \underbrace {A ^ {2} \frac {m \omega_ {0} ^ {2}}{2} \sin^ {2} \left(\omega_ {0} t + \varphi\right)} _ {E _ {\mathrm{kin}}} + \underbrace {A ^ {2} \frac {k}{2} \cos^ {2} \left(\omega_ {0} t + \varphi\right)} _ {E _ {\mathrm{pot}}} = \\ = A ^ {2} \frac {m}{2} \frac {k}{m} \sin^ {2} (\omega_ {0} t + \varphi) + A ^ {2} \frac {k}{2} \cos^ {2} (\omega_ {0} t + \varphi) = \\ = \frac {A ^ {2}}{2} \cdot k = \frac {A ^ {2}}{2} m \omega_ {0} ^ {2} = \text {const.} \tag {I-5.114} \\ \end{array}
$$

Über eine Schwingungsperiode gemittelt erhält man so

$$
\bar {E} _ {\mathrm{kin}} = A ^ {2} \frac {m \omega_ {0} ^ {2}}{4} \underbrace {=} _ {\omega_ {0} ^ {2} = \frac {k}{m}} A ^ {2} \frac {k}{4} = \bar {E} _ {\mathrm{pot}}. \tag {I-5.115}
$$

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">19 Noch schneller kehrt der MP für praktische Zwecke zur Ruhelage zurück, wenn er einmal gerade noch merklich durch die Nulllage hindurchschwingt (weitere Nulldurchgänge sind wegen der starken Dämpfung nicht mehr beobachtbar)! Dies wird bei Messgeräten mit Federrückstellung angewendet (schwach unterkritische Dämpfung: ω0 wenig größer als γ<sup>2</sup>).</span></small>

Für $t = \frac { - \varphi } { \omega _ { 0 } }$ ist $E _ { \mathrm { p o t } } ^ { \mathrm { m a x } } = A ^ { 2 } \; \frac { k } { 2 }$ und $E _ { \mathrm { k i n } } = 0$ (maximal ausgelenkte Position); für $t = \frac { -   \varphi } { \omega _ { 0 } } + \frac { \pi } { 2 }$ ist $E_{\mathrm{kin}}^{\mathrm{max}} = A^{2} \frac{m \omega_{0}^{2}}{2} = A^{2} \frac{k}{2} = E_{\mathrm{pot}}^{\mathrm{max}}$ und $E _ { \mathrm { p o t } } = 0$ (Durchlaufen der Ruheposition).

Die Erhaltungsgröße des Energiesatzes ist also $E _ { \mathrm { k i n } } ^ { \mathrm { m a x } } = E _ { \mathrm { p o t } } ^ { \mathrm { m a x } } = \mathrm { c o n s t } .$ (Abb. I-5.23).

![](images/page_321_chart_4.jpg)

<details>
<summary>line</summary>

| Point | Energy Value |
| --- | --- |
| E_gesamt | E_kin^max = E_pot^max = 1/2 m \(\omega_{0}^{2}A^{2}\) |
| E_pot | E_kin = 1/2 kx² |
| E_kin | E_pot = 1/4 m \(\omega_{0}^{2}A^{2}\) |
| E_kin | E_kin = 1/2 m x² |
</details>

Abb. I-5.23: Kinetische und potenzielle Energie beim ungedämpften harmonischen Oszillator als Funktion des Ausschlags.

Die Energie des <u>gedämpften Oszillators</u> nimmt dagegen mit $e ^ { - 2 \gamma t }$ ab $\left( \dot { x } ^ { 2 } \propto e ^ { - 2 \gamma \bar { t } } \right)$ . Für sehr schwach gedämpfte Schwingungen ist $\boldsymbol { \omega } ^ { \prime } \approx \boldsymbol { \omega } _ { 0 }$ und es gilt näherungsweise

$$
E _ {\text {ged.}} = \frac {1}{2} m \dot {x} _ {\text {ged.}} ^ {2} + \frac {1}{2} k x _ {\text {ged.}} ^ {2} \approx e ^ {- 2 \gamma t} \left(\underbrace {\frac {1}{2} m \dot {x} _ {\text {unged.}} ^ {2} + \frac {1}{2} k x _ {\text {unged.}} ^ {2}} _ {= E _ {\text {unged.}}}\right). \tag {I-5.116}
$$

Das System des gedämpften Oszillators ist also nicht abgeschlossen, sondern es wird Energie nach außen abgegeben.

Der Energieverlust des gedämpften Oszillators tritt als eine bisher nicht betrachtete Energieform, nämlich als Wärmeenergie, in der Umgebung des schwingenden Systems in Erscheinung.

In unserem Experiment des in einer zähen Flüssigkeit schwingenden $M P$ am Beginn von Abschnitt 5.2 erwärmt sich die dämpfende Flüssigkeit etwas.

Wir untersuchen nun, wie sich die Summe aus kinetischer und potenzieller Energie W zeitlich ändert

$$
\frac {d W}{d t} = \frac {d}{d t} \left(\frac {m}{2} \dot {x} ^ {2} + \frac {1}{2} k x ^ {2}\right) = m \dot {x} \ddot {x} + k x \dot {x} \tag {I-5.117}
$$

und erkennen, dass die rechte Seite die Summe des mit ẋ multiplizierten ersten und dritten Terms der Bewegungsgleichung des gedämpften harmonischen Oszillators darstellt (Gl. I-5.85). Wir multiplizieren daher diese Schwingungsgleichung des gedämpften Oszillators mit ẋ und erhalten für die Abnahme der Gesamtenergie mit $\beta = 2   \gamma m$ aus Gl. (I-5.86)

$$
\frac {d W}{d t} = m \dot {x} \ddot {x} + k x \dot {x} = - 2 \gamma m \dot {x} ^ {2}. \tag {I-5.118}
$$

Um die pro Schwingungsperiode in Wärme umgewandelte Energie $W _ { T } ( t )$ zu erhalten, betrachten wir die Energieänderung in einer Schwingungsperiode T

$$
E (t) = \frac {m}{2} \omega_ {0} ^ {2} A ^ {2} (t) = \frac {m}{2} \omega_ {0} ^ {2} A _ {0} ^ {2} e ^ {- 2 \gamma t} \cos^ {2} (\omega^ {\prime} t + \varphi),
$$

$$
\begin{array}{l} E (t + T) = \frac {m}{2} \omega_ {0} ^ {2} A _ {0} ^ {2} e ^ {- 2 \gamma (t + T)} = \frac {m}{2} \omega_ {0} ^ {2} A _ {0} ^ {2} e ^ {- 2 \gamma t} \cdot e ^ {- 2 \gamma T} \cos^ {2} (\omega^ {\prime} t + \varphi + T) = \\ = E (t) \cdot \mathrm{e} ^ {- 2 \gamma T}. \tag {I-5.119} \\ \end{array}
$$

Daraus erhalten wir $W _ { T }$ , wobei wir für sehr schwache Dämpfung $\left( \gamma \ll \omega _ { 0 } \right.$ und $\gamma \cdot \mathrm { T }$ $\ll 1 )$ mit $1 - e ^ { - x } \approx x$ näherungsweise setzen $1 - e ^ { - 2 \gamma T } = 2 \gamma T :$

$$
\begin{array}{l} W _ {T} = E (t) - E (t + T) = \frac {m}{2} \omega_ {0} ^ {2} A _ {0} ^ {2} e ^ {- 2 \gamma t} \cdot (\underbrace {1 - e ^ {- 2 \gamma T}} _ {\approx 2 \gamma T = T / \tau}) \approx \\ \approx \frac {m}{2} \omega_ {0} ^ {2} A _ {0} ^ {2} e ^ {- 2 \gamma t} \cdot 2 \gamma T = \frac {m}{2} \omega_ {0} ^ {2} A _ {0} ^ {2} e ^ {- \frac {t}{\tau}} \frac {T}{\tau} = \frac {1}{\tau} \underbrace {\frac {m}{2} \omega_ {0} ^ {2} A _ {0} ^ {2} e ^ {- \frac {t}{\tau}}} _ {\bar {E} (t) = \bar {E} _ {\mathrm{kin}} (t) + \bar {E} _ {\mathrm{pot}} (t)} \cdot T = \\ = \frac {\bar {E} (t)}{\tau} \cdot T. \tag {I-5.120} \\ \end{array}
$$

Dabei wurde $2 \gamma = { \frac { 1 } { \tau } }$ gesetzt, wobei τ die Energierelaxationszeit ist.

Die Reibungsverluste steigen in diesem Fall also proportional zur Dämpfungskonstante $\gamma$ bzw. indirekt proportional zur Energierelaxationszeit an.

Ein für praktische Schwingungsprobleme (Akustik, Hochfrequenztechnik) viel verwendeter Begriff für die Bewertung der Dämpfung einer Schwingung ist die Oszillatorgüte $Q ,$ in der Hochfrequenztechnik ‚Kreisgüte‘ genannt. Die Oszillatorgüte ist definiert durch (für kleine Dämpfung ist ja $\omega ^ { \prime } = \omega _ { 0 } )$

$$
Q = 2 \pi \frac {\text {Mittelwert der gespeicherten Energie}}{\text {mittlerer Energieverlust in einer Periode}} = \frac {2 \pi \bar {E} (t)}{W _ {T}} = \frac {2 \pi \bar {E} (t)}{\frac {\bar {E} (t)}{\tau} \cdot T}, \tag {I-5.121}
$$

also

$$
Q = 2 \pi \frac {\tau}{T} = \omega_ {0} \tau = \frac {\omega_ {0}}{2 \gamma} \quad \begin{array}{l l} & \text {Oszillatorgüte} = \\ & \text {Kreisgüte} = \text {Gütefaktor} \\ & (\text {quality factor, Q - factor}). \end{array} \tag {I-5.122}
$$

Die Oszillatorgüte ist gleich dem 2 π-fachen der Anzahl der Schwingungen in der Relaxationszeit der Energie. Die Relaxationszeit τ ist dabei die Zeit, in der die Energie des Oszillators auf den Bruchteil $1 / e$ gefallen ist.

Oszillatorgüte schwingender Systeme.

| schwingendes System | Oszillatorgüte Q |
| --- | --- |
| Klaviersaite, Geige, Erdbeben | $10^{3}$ |
| angeregtes Atom | $10^{7}$ |
| angeregter Fe$^{57}$ Atomkern | $3 \cdot 10^{12}$ |

## 5.3 Erzwungene Schwingung und Resonanz

## 5.3.1 Periodische Anregung, komplexe und reelle Amplituden der erzwungenen Schwingung

Ein schwingungsfähiges System kann von außen zu Schwingungen angeregt werden. Wir lassen dazu auf unseren gedämpft schwingenden $M P$ eine periodische äußere Kraft $F _ { a } = F _ { 0 } \cdot e ^ { i \omega t }$ wirken. Damit erhalten wir folgende Schwingungsgleichung

$$
\ddot {x} + 2 \gamma \dot {x} + \omega_ {0} ^ {2} x = a _ {0} \cdot e ^ {i \omega t} \quad \text {mit} \quad a _ {0} = \frac {F _ {0}}{m} (\text {reell}), \tag {I-5.123}
$$

wobei $a _ { 0 }$ die Beschleunigungsamplitude der äußeren Kraft ist. Dies ist eine lineare, inhomogene DG. Die allgemeine Lösung erhalten wir als Summe der allgemeinen Lösung der zugehörigen homogenen DG (allgemeine Lösung der gedämpften Schwingung) und einer partikulären Lösung der inhomogenen DG.

Wir nehmen als allgemeine Lösung der homogenen DG die Lösung für einen schwach gedämpften Oszillator (Gl. I-5.91) und als spezielle Lösung der inhomogenen DG eine periodische Schwingung mit der äußeren Anregungsfrequenz ω

$$
x (t) = e ^ {- \gamma t} \big [ c \cdot e ^ {i \omega^ {\prime} t} + c ^ {\star} \cdot e ^ {- i \omega^ {\prime} t} \big ] + c ^ {\prime} \cdot e ^ {i \omega t} \quad \mathrm{mit} \quad \omega^ {\prime} \equiv \sqrt {\omega_ {0} ^ {2} - \gamma^ {2}}. \qquad \mathrm{(I-5.124)}
$$

Der erste Summand stellt den Einschwingvorgang dar, der weitgehend durch die Eigenfrequenz $\omega _ { 0 }$ des schwingenden Systems bestimmt wird. Er ist in der musikalischen Akustik für die Klangfarbe der Musikinstrumente mitverantwortlich. Dieser Schwingungsanteil der erzwungenen Schwingung klingt mit $e ^ { - \gamma t }$ ab. Der zweite Summand, der nach Abklingen des Einschwingvorgangs bestehen bleibt, stellt den eigentlichen, stationären Schwingungsvorgang der erzwungenen Schwingung dar, der von der Anregungsfrequenz ω bestimmt wird.

Wir betrachten daher im Folgenden nur mehr den stationären Schwingungsfall, nehmen also an, dass der Einschwingvorgang bereits abgeklungen ist.

Als Lösungsansatz verwenden wir $x ( t ) = c ^ { \prime } \cdot e ^ { i \omega t }$ , bilden $\dot { x } = i \omega c ^ { \prime } \cdot e ^ { i \omega t }$ und $\ddot { \boldsymbol { x } } = - \boldsymbol { \omega } ^ { 2 } \boldsymbol { c } ^ { \prime } \cdot \boldsymbol { e } ^ { i \omega t }$ und setzen in die Bewegungsgleichung ein

$$
\left(- \omega^ {2} c ^ {\prime} + 2 i \gamma \omega c ^ {\prime} + \omega_ {0} ^ {2} c ^ {\prime}\right) \cdot e ^ {i \omega t} = a _ {0} \cdot e ^ {i \omega t}. \tag {I-5.125}
$$

Es gilt also $c ^ { \prime } ( \omega _ { 0 } ^ { 2 } - \omega ^ { 2 } + 2 i \gamma \omega ) = a _ { 0 }$ bzw.

$$
\begin{array}{l} c ^ {\prime} = \frac {a _ {0}}{\omega_ {0} ^ {2} - \omega^ {2} + 2 i \gamma \omega} = \frac {a _ {0} (\omega_ {0} ^ {2} - \omega^ {2} - 2 i \gamma \omega)}{(\omega_ {0} ^ {2} - \omega^ {2}) ^ {2} + (2 \gamma \omega) ^ {2}} = \\ = \frac {a _ {0} (\omega_ {0} ^ {2} - \omega^ {2}) - 2 i a _ {0} \gamma \omega}{(\omega_ {0} ^ {2} - \omega^ {2}) ^ {2} + (2 \gamma \omega) ^ {2}} = a - i b = \left| c ^ {\prime} \right| e ^ {i \varphi} \tag {I-5.126} \\ \end{array}
$$

mit

$$
a = \frac {a _ {0} (\omega_ {0} ^ {2} - \omega^ {2})}{(\omega_ {0} ^ {2} - \omega^ {2}) ^ {2} + (2 \gamma \omega) ^ {2}} \quad \text {für den Realteil der Amplitude} \tag {I-5.127}
$$

und

$$
b = \frac {2 a _ {0} \gamma \omega}{\left(\omega_ {0} ^ {2} - \omega^ {2}\right) ^ {2} + (2 \gamma \omega) ^ {2}} \quad \text { für   ihren   Imaginärteil, } \tag {I-5.128}
$$

wobei $\left| \boldsymbol{c}^{\prime} \right| = \sqrt{\boldsymbol{a}^{2} + \boldsymbol{b}^{2}}$ ; tan $\varphi = { \frac { - b } { a } }$ (also φ = −arc tan (b/a)) mit $b > 0$ und

$$
a \left\{ \begin{array}{l l} > 0 & \text {fur} \omega_ {0} ^ {2} > \omega^ {2} \quad \Rightarrow \quad \tan \varphi <   0; \quad 0 \geq \varphi > - \frac {\pi}{2} \\ = 0 & \text {fur} \omega_ {0} ^ {2} = \omega^ {2} \quad \Rightarrow \quad \tan \varphi = \mp \infty ; \quad \varphi = - \frac {\pi}{2} \\ <   0 & \text {fur} \omega_ {0} ^ {2} <   \omega^ {2} \quad \Rightarrow \quad \tan \varphi > 0; \quad - \frac {\pi}{2} > \varphi \geq - \pi . \end{array} \right.
$$

Aus

$$
\left| c ^ {\prime} \right| ^ {2} = a ^ {2} + b ^ {2} = \frac {a _ {0} ^ {2} \left[ (\omega_ {0} ^ {2} - \omega^ {2}) ^ {2} + (2 \gamma \omega) ^ {2} \right]}{\left[ (\omega_ {0} ^ {2} - \omega^ {2}) ^ {2} + (2 \gamma \omega) ^ {2} \right] ^ {2}}, \tag {I-5.129}
$$

folgt die reelle Amplitude der erzwungenen Schwingung

$$
A _ {\mathrm{stat}} = \left| c ^ {\prime} \right| = \frac {a _ {0}}{\sqrt {\left(\omega_ {0} ^ {2} - \omega^ {2}\right) ^ {2} + \left(2 \gamma \omega\right) ^ {2}}}  . \tag {I-5.130}
$$

Als stationäre Lösung der DG Gl. (I-5.123) ergibt sich also

$$
x (t) = \left| c ^ {\prime} \right| \cdot e ^ {i (\omega t + \varphi)}. \tag {I-5.131}
$$

Es zeigt sich wegen des negativen Phasenwinkels $\varphi ,$ dass die erzwungene Schwingung gegen die Erregerschwingung zurückbleibt. $\left| c ^ { \prime } \right| = A _ { \mathrm { s t a t } }$ ist der Betrag der Amplitude der erzwungenen Schwingung im stationären Schwingfall. Es ergeben sich zwei Anteile der komplexen Amplitude, wobei der Realteil im Bereich abseits der Resonanzstelle $\left( \left| \omega _ { 0 } ^ { 2 } - \omega ^ { 2 } \right| \gg \gamma \omega \right)$ , der Imaginärteil in der Nähe der Resonanzstelle $( \omega \approx \omega _ { 0 } )$ dominiert.

Die Amplitude der erzwungenen Schwingung $A _ { s t a t }$ hängt also außer von der Amplitude $a _ { 0 }$ der äußeren Kraft noch von der Erregerfrequenz $\omega ,$ der Eigenfrequenz des schwingenden Systems $\omega _ { 0 }$ und der Dämpfung $\gamma$ ab.

Die Darstellung der Amplituden der Erregerschwingung und der dadurch erzwungenen Schwingung sowie ihre Phasenlage erfolgt in der komplexen Zahlenebene (Abb. I-5.24):

![](images/page_325_image_9.jpg)

<details>
<summary>text_image</summary>

Im
a
-a
-φ
c'
Re
</details>

Abb. I-5.24: Amplituden der Erregerschwingung und der resultierenden erzwungenen Schwingung sowie ihre Phasenlage zueinander.

Die Phasenlage zwischen der erregenden und der erzwungenen Schwingung (Abb. I-5.25) ist gegeben durch

$$
\tan \varphi = \frac {- b}{a} = \frac {- 2 \gamma \omega}{\omega_ {0} ^ {2} - \omega^ {2}}. \tag {I-5.132}
$$

Das Vorzeichen von tan $\varphi$ hängt von $( \omega _ { 0 } ^ { 2 } - \omega ^ { 2 } )$ ab und wechselt beim Durchgang durch die Stelle $\omega _ { 0 } = \omega$ (Resonanzstelle) von −∞ auf +∞, der Winkel $\varphi$ bleibt jedoch aus Stetigkeitsgründen weiterhin negativ mit $\varphi < - \pi / 2$ bei positivem tan $\varphi$ . Er ändert sich von $\varphi = 0$ für $\omega = 0$ über $\varphi = - \pi / 2$ für $\omega = \omega _ { 0 }$ bis $\varphi = - \pi$ für $\omega \to \infty .$ Bei verschwindender Dämpfung $\gamma ~ = 0$ sind beide Schwingungen für $\omega ^ { 2 } < \omega _ { 0 } ^ { 2 }$ in Phase $\left( \varphi = 0 \right)$ , für $\omega ^ { 2 } \succ \omega _ { 0 } ^ { 2 }$ in Gegenphase $\left( \varphi = - \pi \right)$ ; bei $\omega = \omega _ { 0 }$ springt die Phase $\mathbf { u m } - { \boldsymbol { \pi } } .$

![](images/page_326_chart_3.jpg)

<details>
<summary>line</summary>

| \(\omega/\omega_{0}\) | \(\gamma=0.05\) | \(\gamma=0.10\) | \(\gamma=0.15\) | \(\gamma=0.30\) | \(\gamma=0.50\) | \(\gamma=1.00\) |
| --- | --- | --- | --- | --- | --- | --- |
| 0 | 0 | 0 | 0 | 0 | 0 | 0 |
| 1 | \(-\pi/2\) | \(-\pi/2\) | \(-\pi/2\) | \(-\pi/2\) | \(-\pi/2\) | \(-\pi/2\) |
| 2 | ~-0.85 | ~-0.95 | ~-1.05 | ~-1.15 | ~-1.25 | ~-1.35 |
</details>

Abb. I-5.25: Phasenlage φ zwischen der erzwungenen Schwingung und der Erregerschwingung für verschiedene Werte der Dämpfungskonstante $\gamma .$

## 5.3.2 Resonanz

Wir fragen: Wann wird die Amplitude $A _ { \mathrm { s t a t } }$ der stationären erzwungenen Schwingung maximal?

Dazu bilden wir die erste Ableitung von $| c ^ { \prime } |$ nach der Anregungsfrequenz ω und setzen Null

$$
\begin{array}{l} \frac {\partial}{\partial \omega} \Bigg (a _ {0} \left[ (\omega_ {0} ^ {2} - \omega^ {2}) ^ {2} + (2 \gamma \omega) ^ {2} \right] ^ {- \frac {1}{2}} \Bigg) = \\ = - \frac {1}{2} a _ {0} \left[ \left(\omega_ {0} ^ {2} - \omega^ {2}\right) ^ {2} + (2 \gamma \omega) ^ {2} \right] ^ {- \frac {3}{2}} \left[ 2 \left(\omega_ {0} ^ {2} - \omega^ {2}\right) \cdot (- 2 \omega) + 4 \gamma \omega \cdot 2 \gamma \right] = \\ = \frac {a _ {0} \left(2 \omega (\omega_ {0} ^ {2} - \omega^ {2}) - 4 \gamma^ {2} \omega\right)}{\left[ (\omega_ {0} ^ {2} - \omega^ {2}) ^ {2} + (2 \gamma \omega) ^ {2} \right] ^ {\frac {3}{2}}} = \frac {a _ {0} \cdot 2 \omega \left((\omega_ {0} ^ {2} - \omega^ {2}) - 2 \gamma^ {2}\right)}{\left[ (\omega_ {0} ^ {2} - \omega^ {2}) ^ {2} + (2 \gamma \omega) ^ {2} \right] ^ {\frac {3}{2}}} = 0 \tag {I-5.133} \\ \end{array}
$$

Auch bei sehr kleiner Dämpfung bleibt der Nenner endlich und ungleich Null, der Zähler muss also verschwinden. Daher muss gelten

$$
\omega_ {0} ^ {2} - \omega_ {R} ^ {2} - 2 \gamma^ {2} = 0 \tag {I-5.134}
$$

und damit

$$
\omega_ {R} = \sqrt {\omega_ {0} ^ {2} - 2 \gamma^ {2}} <   \omega_ {0} \quad \text {Resonanzfrequenz} \tag {I-5.135}
$$

mit $\omega _ { R } < \omega _ { 0 }$ für $\gamma \neq 0$

Bei sehr kleiner Dämpfung $\gamma \ll \omega _ { 0 }$ liegt die Resonanzfrequenz sehr dicht bei der Eigenfrequenz, also $\omega _ { R } \approx \omega _ { 0 }$ , und für $\omega = \omega _ { 0 }$ kommt es für $\gamma = 0$ (keine Dämpfung) zur Resonanzkatastrophe mit $A _ { \mathrm { s t a t } } \to \infty$

Der Maximalwert der Amplitude beträgt

$$
\begin{array}{l} A _ {\max} = \frac {a _ {0}}{\sqrt {\left(\omega_ {0} ^ {2} - \omega_ {R} ^ {2}\right) ^ {2} + \left(2 \gamma \omega_ {R}\right) ^ {2}}} \stackrel {{=}} {{=}} \frac {a _ {0}}{\sqrt {\left(2 \gamma^ {2}\right) ^ {2} + 4 \gamma^ {2} \left(\omega_ {0} ^ {2} - 2 \gamma^ {2}\right)}} = \\ = \frac {a _ {0}}{2 \gamma \sqrt {\omega_ {0} ^ {2} - \gamma^ {2}}} \approx \frac {a _ {0} \tau}{\omega_ {0}} \tag {I-5.136} \\ \end{array}
$$

mit $\tau = \frac { 1 } { 2 \gamma }$ (Relaxationszeit der Energieabnahme).<sup>20</sup>

Für $\omega = 0$ (statische Auslenkung $A _ { 0 } )$ ist $A_{0} = \frac{a_{0}}{\omega_{0}^{2}} = \frac{F_{0}/m}{k/m} = \frac{F_{0}}{k}$ (Gl. I-5.130) und es ergibt sich daher (Gl. I-5.122)

$$
\frac {A _ {\max}}{A _ {0}} = \omega_ {0} \tau = Q. \tag {I-5.137}
$$

Das Verhältnis $A _ { \mathrm { m a x } } / A _ { 0 }$ heißt Resonanzüberhöhung und ist also gleich der Oszillatorgüte.

Für $\gamma \rightarrow 0$ (ungedämpfte Schwingung) gilt $A _ { \mathrm { m a x } } \to \infty$ (Resonanzkatastrophe). Wegen des Einschwingvorgangs tritt $A _ { \operatorname* { m a x } } \to$ ∞ aber erst für $t \rightarrow$ ∞ ein, es handelt sich also um eine ‚vorhersagbare Katastrophe‘.

Es zeigt sich, dass die Resonanzkurven (Abb. I-5.26) asymmetrisch um $\omega _ { 0 }$ liegen, die Asymmetrie steigt mit $\frac { \gamma } { \omega }$ .21

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">20 Durch Elimination von γ<sup>2</sup> aus den Beziehungen für ω<sub>R</sub> und A<sub>max</sub> ergibt sich: 1 A<sub>max</sub> = A<sub>0</sub> . 1 − (ωR / ω0)2</span></small>

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">21 Eine analoge Rechnung zeigt, dass die Geschwindigkeit des Massenpunktes υ = ẋ= |c′ |iω ei(ωt +φ) unabhängig von der Dämpfung γ stets für ω<sub>vR</sub> = ω<sub>0</sub> das Maximum besitzt (υ<sub>max</sub> = a<sub>0</sub> / 2 γ = a<sub>0</sub>τ).</span></small>

![](images/page_328_chart_2.jpg)

<details>
<summary>line</summary>

| \(\gamma\) | \(\omega/R/\omega_{0}\) | \(Astat/A_{0}\) |
| --- | --- | --- |
| 0.05 | 1 | ~10 |
| 0.10 | 1 | ~5 |
| 0.15 | 1 | ~3.5 |
| 0.30 | 1 | ~1.7 |
| 0.50 | 1 | ~1.2 |
| 1.00 | 1 | ~1.1 |
</details>

Abb. I-5.26: Resonanzkurven der erzwungenen Schwingung für verschiedene Werte der Dämpfungskonstante γ. Die Maxima liegen auf einer zwischen $\omega / \omega _ { 0 } = 0 \quad ( A _ { \mathrm { s t a t } } / A _ { 0 } = 1 )$ und $\omega / \omega _ { 0 } = 1 \quad ( A _ { \mathrm { s t a t } } / A _ { 0 } = \infty )$ rasch ansteigenden Kurve: $A _ { \mathrm { m a x } } = A _ { 0 } \frac { 1 } { 1 - \left( \omega _ { R } / \omega _ { 0 } \right) ^ { 2 } } .$

Wir bemerken einen kleinen Unterschied der Resonanzfrequenz $\omega _ { R } = \sqrt { \omega _ { 0 } ^ { 2 } - 2 { \boldsymbol { \gamma } } ^ { 2 } }$ zur Eigenfrequenz des schwach gedämpften Oszillators, bei dem $\boldsymbol { \omega } ^ { \prime } = \sqrt { \boldsymbol { \omega } _ { 0 } ^ { 2 } - \boldsymbol { \gamma } ^ { 2 } }$ war.

## 5.3.3 Energiebilanz der erzwungenen Schwingung

Wie beim gedämpften Oszillator multiplizieren wir die Bewegungsgleichung (Gl. I-5.123) mit ẋ, um die zeitliche Energieänderung zu sehen

$$
\underbrace {m \dot {x} \ddot {x} + k x \dot {x}} _ {\substack {\text {gesamte} \\ \text {Energieänderung} \\ \text {pro Zeit} = d E _ {\mathrm{ges}} / d t \\ (\text {siehe Gl. I - 5.117})}} = \underbrace {- 2 \gamma m \dot {x} ^ {2}} _ {\substack {\text {Energieverlust} \\ \text {durch Reibung} \\ \text {pro Zeit}}} + \underbrace {F (t) \cdot \dot {x}} _ {\substack {\text {von außen} \\ \text {zugeführte Energie} \\ \text {pro Zeit}}}.\tag{I - 5.138}
$$

Im stationären Zustand muss die Gesamtenergie konstant sein, also $E _ { \mathrm { g e s } } = \mathrm { c o n s t } .$ und damit mxẋ ̈ $+ k x { \dot { x } } = 0$ . Mit $F ( t ) = a _ { 0 }$ cos ωt und $x(t) = \left| c' \right| \cos \left( \omega t - \varphi \right)$ folgt mit Gl. (I-5.130)

$$
F (t) \cdot \dot {x} = 2 \gamma m \dot {x} ^ {2} = \frac {2 \gamma m a _ {0} ^ {2} \omega^ {2}}{\left(\omega_ {0} ^ {2} - \omega^ {2}\right) ^ {2} + \left(2 \gamma \omega\right) ^ {2}} \sin^ {2} (\omega t - \varphi). \tag {I-5.139}
$$

Im stationären Fall der erzwungenen Schwingung wird also die gesamte von außen durch die Erregungskraft zugeführte Energie in Reibungswärme umgewandelt.

Für den Resonanzfall $\omega \cong \omega _ { 0 } ,   \varphi = - \pi / 2$ gilt

$$
F (t) \cdot \dot {x} = \frac {m a _ {0} ^ {2}}{2 \gamma} \cdot \sin^ {2} \left(\omega t - \frac {\pi}{2}\right), \text {im Zeitmittel:} P = \langle F (t) \dot {x} \rangle = \frac {m a _ {0} ^ {2}}{4 \gamma}. \tag {I-5.140}
$$

Im Falle kleiner Dämpfung muss also bei Resonanz von der erregenden Kraft eine größere Leistung P erbracht werden als im Falle großer Dämpfung, da das Geschwindigkeitsquadrat mit fallender Dämpfung mit $1 / \gamma ^ { 2 }$ wächst (Gl. I-5.141). Für die Geschwindigkeit gilt im Resonanzfall

$$
\dot {x} = - \frac {a _ {0}}{2 \gamma} \sin \left(\omega t - \frac {\pi}{2}\right) = \frac {a _ {0}}{2 \gamma} \cos \omega t. \tag {I-5.141}
$$

Die Geschwindigkeit ist daher bei kleiner Dämpfung $\gamma$ sehr groß und für den hohen Leistungsaufwand im Resonanzfall verantwortlich.

Erregende Kraft und Geschwindigkeit sind im Resonanzfall in Phase, während die Auslenkung x um $\pi / 2$ nacheilt. Um zu möglichst großen Ausschlägen zu kom men, stößt man daher die Schaukel immer im Nulldurchgang an, wenn die Geschwindigkeit maximal und die treibende Kraft mit ihr in Phase ist.<sup>22</sup>

## 5.4 Gekoppelte Oszillatoren

Besteht zwischen schwingungsfähigen Systemen eine Wechselwirkung, sodass die Schwingung eines Systems von der Schwingung des anderen beeinflusst wird, so spricht man von gekoppelten Oszillatoren (coupled oscillators); die Beeinflussung erfolgt durch Kopplungsglieder. Gekoppelte Oszillatoren haben in der Physik eine große Bedeutung, da die Schwingungsenergie von einem System auf das andere übertragen werden kann und es so zur Ausbreitung von Wellen kommt, wenn viele Schwinger beteiligt sind.

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">22 Allerdings liegt im Falle einer angestoßenen Schaukel keine sinusförmige Antriebskraft vor, sondern ein Kraftpuls. Die Grundfrequenz in der Fourierzerlegung des Kraftpulses muss mit der Eigenfrequenz ω<sub>0</sub> der Schaukel übereinstimmen, denn zur Grundfrequenz gehört die größte Kraftamplitude a<sub>1</sub> (≡ a<sub>0</sub> in obiger Bezeichnung).</span></small>

![](images/page_330_image_2.jpg)

<details>
<summary>text_image</summary>

k₁
m₁
k₁₂
m₂
k₂
0 → x₁
0 → x₂
</details>

Abb. I-5.27: Zwei Federpendel mit den Punktmassen $m _ { 1 }$ und $m _ { 2 }$ und den Federkonstanten $k _ { 1 }$ und $k _ { 2 } ,$ sind durch eine Koppelfeder mit der Federkonstante $k _ { 1 2 }$ (Kopplungskonstante) gekoppelt.

Wir betrachten 2 Federpendel mit den Punktmassen $m _ { 1 }$ und $m _ { 2 }$ und den Federkonstanten $k _ { 1 }$ und $k _ { 2 } ,$ die durch eine Koppelfeder mit der Federkonstante $k _ { 1 2 }$ (Kopplungskonstante) gekoppelt sind (Abb. I-5.27).

Die Ausdehnung der mittleren Feder hängt von der jeweiligen Position $x _ { i }$ beider Massenpunkte ab, dadurch hängt auch die Kraft auf jeden MP nicht nur von seiner eigenen Position ab, sondern auch von der Position des anderen MP.

Für die Bewegungsgleichungen der beiden MP ergibt sich $( x _ { 1 } , x _ { 2 }$ Auslenkungen aus der Ruhelage)

$$
\left. \begin{array}{l} m _ {1} \ddot {x} _ {1} = - k _ {1} x _ {1} - k _ {1 2} (x _ {1} - x _ {2}) \\ m _ {2} \ddot {x} _ {2} = - k _ {2} x _ {2} - k _ {1 2} (x _ {2} - x _ {1}) \end{array} \right\}. \tag {I-5.142}
$$

Dies sind gekoppelte Differentialgleichungen, sie enthalten die Auslenkungen $x _ { 1 }$ und $x _ { 2 }$ beider Massenpunkte.

Wenn wir annehmen, dass die beiden Oszillatoren gleiche Massen und gleiche Federkonstanten haben, dass also gilt $m _ { 1 } = m _ { 2 } = m$ und $k _ { 1 }   = k _ { 2 } = k _ { 3 }$ so ist eine Entkopplung der Gleichungen leicht möglich<sup>23</sup>

$$
m \ddot {x} _ {1} = - k x _ {1} - k _ {1 2} (x _ {1} - x _ {2})
$$

$$
m \ddot {x} _ {2} = - k x _ {2} - k _ {1 2} (x _ {2} - x _ {1}). \tag {I-5.143}
$$

Die Gleichungen werden addiert bzw. subtrahiert, das ergibt

$$
m (\ddot {x} _ {1} + \ddot {x} _ {2}) = - k (x _ {1} + x _ {2})
$$

$$
m (\ddot {x} _ {1} - \ddot {x} _ {2}) = - k (x _ {1} - x _ {2}) - 2 k _ {1 2} (x _ {1} - x _ {2}). \tag {I-5.144}
$$

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">23 Mit entsprechendem mathematischem Aufwand ist eine Entkopplung selbst eines N-Teilchensystems immer möglich!</span></small>

Wir führen neue Variablen durch neue Koordinaten ein

$$
\xi^ {+} = \frac {1}{2} (x _ {1} + x _ {2}) \quad \text {und} \quad \xi^ {-} = \frac {1}{2} (x _ {1} - x _ {2}) \tag {I-5.145}
$$

also

$$
\xi^ {+} + \xi^ {-} = x _ {1} \quad \text {und} \quad \xi^ {+} - \xi^ {-} = x _ {2}. \tag {I-5.146}
$$

und erhalten

$$
m \ddot {\xi} ^ {+} = - k \xi^ {+}
$$

$$
m \ddot {\xi} ^ {-} = - (k + 2 k _ {1 2}) \xi^ {-}. \tag {I-5.147}
$$

Damit sind die $D G ^ { \flat } s$ entkoppelt!

Als Lösungen in den neuen Koordinaten $\xi ^ { + }$ und $\xi ^ { - }$ setzen wir folgende harmonische Schwingungen an

$$
\xi^ {+} (t) = A _ {1} \cdot \cos (\omega_ {1} t + \varphi_ {1})
$$

$$
\xi^ {-} (t) = A _ {2} \cdot \cos (\omega_ {2} t + \varphi_ {2}). \tag {I-5.148}
$$

Dabei gilt (Gl. I-5.147) $\omega_{1}^{2}=\frac{k}{m}\bmod\omega_{2}^{2}=\frac{k+2k_{12}}{m}$

Die Schwingungen des gekoppelten Systems ergeben sich als Überlagerung der Schwingungen $\xi ^ { + } ( t )$ und $\xi ^ { - } ( t )$ mit den Frequenzen $\omega _ { 1 }$ und $\omega _ { 2 }$ , den Normalschwingungen (= Fundamentalschwingungen, normal modes). Die nicht miteinander gekoppelten Koordinaten $\boldsymbol { \xi } ^ { + } = \frac { \boldsymbol { x } _ { 1 } + \boldsymbol { x } _ { 2 } } { 2 }$ und $\boldsymbol { \xi } ^ { - } = \frac { \boldsymbol { X } _ { 1 } - \boldsymbol { X } _ { 2 } } { 2 }$ heißen Normalkoordinaten des gekoppelten Systems.

Welche Schwingungen führt das gekoppelte System in den üblichen Raumkoordinaten $x _ { 1 }$ und $x _ { 2 }$ aus?

Wir nehmen vereinfachend an, dass die beiden Amplituden $A _ { 1 }$ und $A _ { 2 }$ gleich sind und setzen $A _ { 1 }   =   A _ { 2 }   =   A$

Damit erhalten wir für die Schwingung der Massenpunkte mit $x _ { 1 } = \xi ^ { + } + \xi ^ { - }$ und $x _ { 2 } = \xi ^ { + } - \xi ^ { - }$

$$
\begin{array}{l} x _ {1} = A \left[ \cos \left(\omega_ {1} t + \varphi_ {1}\right) + \cos \left(\omega_ {2} t + \varphi_ {2}\right) \right] = \\ = 2 A \left[ \cos \frac {\omega_ {1} t + \omega_ {2} t + \varphi_ {1} + \varphi_ {2}}{2} \cos \frac {\omega_ {1} t + \varphi_ {1} - \omega_ {2} t - \varphi_ {2}}{2} \right] = \\ = 2 A \cos \left(\underbrace {\frac {\omega_ {1} - \omega_ {2}}{2}} _ {\text {Schwebungs- frequenz}} t + \frac {\varphi_ {1} - \varphi_ {2}}{2}\right) \cos \left(\frac {\omega_ {1} + \omega_ {2}}{2} t + \frac {\varphi_ {1} + \varphi_ {2}}{2}\right) \tag {I-5.149} \\ \end{array}
$$

und

$$
\begin{array}{l} x _ {2} = A \left[ \cos \left(\omega_ {1} t + \varphi_ {1}\right) - \cos \left(\omega_ {2} t + \varphi_ {2}\right) \right] = \\ = - 2 A \sin \left(\frac {\omega_ {1} - \omega_ {2}}{2} t + \frac {\varphi_ {1} - \varphi_ {2}}{2}\right) \sin \left(\frac {\omega_ {1} + \omega_ {2}}{2} t + \frac {\varphi_ {1} + \varphi_ {2}}{2}\right). \tag {I-5.150} \\ \end{array}
$$

Es ergeben sich also Schwebungen, die um $\pi / 2$ gegeneinander phasenverschoben sind, sodass sich ein Pendel in Ruhe befindet, wenn das andere maximal ausgelenkt ist (Abb. I-5.28).

![](images/page_332_chart_5.jpg)

<details>
<summary>line</summary>

| Time (t) | x1(t) | x2(t) |
| --- | --- | --- |
| 0 | 1 | 0 |
| \(\pi/2\) | 0 | 0 |
| \(\pi/2\) | 1 | 1 |
</details>

Abb. I-5.28: Auf die Maximalauslenkung normierte Auslenkungen $x _ { 1 }$ und $x _ { 2 }$ der beiden gekoppelten Pendel als Funktion der Zeit. Es ergeben sich Schwebungsschwingungenen, die um $\pi / 2$ gegeneinander phasenverschoben sind: Ein Pendel befindet sich in Ruhe, wenn das andere gerade maximal ausgelenkt ist.

Wie sehen die Normalschwingungen $\xi ^ { + } ( t )$ und $\xi ^ { - } ( t )$ der gekoppelten Oszillatoren (Lösungen von Gl. I-5.147) sowie die zugehörigen Auslenkungen $x _ { 1 }$ und $x _ { 2 }$ aus?

Wir setzen zuerst die Anfangsbedingungen so, dass beide Massen um denselben Betrag ausgelenkt werden, die Koppelung also nicht beansprucht wird. Dann gilt wegen der Identität der beiden Schwinger, dass beide Massen gleichphasig mit der gleichen Frequenz $\omega _ { 1 } = { \sqrt { \frac { k } { m } } }$ schwingen (Abb. I-5.29, links), also

$$
x _ {1} (t) = A \cdot \cos \left(\sqrt {k / m} \cdot t + \varphi\right) \quad \text {und} \quad x _ {2} (t) = A \cdot \cos \left(\sqrt {k / m} \cdot t + \varphi\right). \tag {I-5.151}
$$

Für $\xi ^ { + }$ und $\xi ^ { - }$ folgt in diesem Falle

$$
\xi^ {+} (t) = \frac {1}{2} \left(x _ {1} + x _ {2}\right) = x _ {1} (t) = A \cos \left(\omega_ {1} t + \varphi_ {1}\right) \tag {I-5.152}
$$

und

$$
\xi^ {-} = \frac {1}{2} \left(x _ {1} - x _ {2}\right) = 0. \tag {I-5.153}
$$

![](images/page_333_image_6.jpg)

Abb. I-5.29: Gleichphasige (links) und gegenphasige (rechts) Normalschwingung der gekoppelten Pendel.

Wählen wir dagegen die Anfangsbedingungen so, dass beide Massen genau gegenphasig schwingen (Abb. I-5.29, rechts), dass also gilt $x _ { 1 } ( t ) = - x _ { 2 } ( t )$ mit Frequenz

$$
\omega_ {2} = \sqrt {\frac {k + 2 k _ {1 2}}{m}} = \sqrt {\omega_ {1} ^ {2} + \frac {2 k _ {1 2}}{m}}, \text {so ist}
$$

$$
x _ {1} (t) = A \cdot \cos \left(\sqrt {\omega_ {1} ^ {2} + 2 k _ {1 2} / m} \cdot t + \varphi\right) \text {und}
$$

$$
x _ {2} (t) = - A \cdot \cos \left(\sqrt {\omega_ {1} ^ {2} + 2 k _ {1 2} / m} \cdot t + \varphi\right) \tag {I-5.154}
$$

und es gilt jetzt

$$
\xi^ {+} = \frac {1}{2} (x _ {1} + x _ {2}) = 0 \tag {I-5.155}
$$

und

$$
\xi^ {-} (t) = \frac {1}{2} \left(x _ {1} - x _ {2}\right) = - x _ {2} (t) = A \cos \left(\omega_ {2} t + \varphi_ {2}\right). \tag {I-5.156}
$$

Beide Pendel schwingen also genau gegenphasig mit der höheren Frequenz $\omega _ { 2 } .$

Die N Teilchen eines gekoppelten Systems von z. B. Atomen oder Molekülen eines Festkörpers mit 3 N Freiheitsgraden (siehe Band VI, Kapitel „Festkörperphysik“, Abschnitt 2.5) führen bei kleinen Auslenkungen aus der Ruhelage harmonische Schwingungen aus, wobei i. Allg. 3 N verschiedene Frequenzen, eine für jeden Freiheitsgrad, möglich sind (Normalschwingungen = Eigenschwingungen). Im Gegensatz zu den tatsächlichen Schwingungen der einzelnen Atome sind die fiktiven Normalschwingungen völlig unabhängig voneinander, also entkoppelt.

## 5.5 Mechanische Wellen (mechanical waves)

Sind Massenpunkte z. B. durch Bindungskräfte mit anderen, räumlich benachbarten, gekoppelt, so kann sich die Schwingung eines Massenpunktes so weit im Raum ausbreiten, als es angekoppelte Massenpunkte gibt.

1 Bei der Ausbreitung von Wellen wird Schwingungsenergie räumlich transportiert. Wir sprechen auch von Strahlung, z. B. Schallstrahlung.

Die Ausbreitungsgeschwindigkeit der Wellen hängt von der Kopplung und der Masse der schwingenden Systeme ab.

## 5.5.1 Ebene Wellen (plane waves), Phasengeschwindigkeit (phase velocity)

Wir nehmen also jetzt an, dass der ganze Raum mit gekoppelten Oszillatoren gefüllt sei und betrachten nicht nur den Schwingungszustand an einem gewissen Punkt, sondern an allen Punkten des Raumes.

Wir nehmen zunächst vereinfachend an, dass ein sich in x-Richtung ausbreitender Schwingungszustand von der y- und z-Koordinate unabhängig sei, also nur eine Funktion von x ist. Eine Welle liegt vor, wenn an der Stelle x dieselbe Schwingungsbewegung besteht wie am Ort $x = 0$ , von der sie sich nur durch eine Phasenverschiebung unterscheidet, die der endlichen Ausbreitungsgeschwindigkeit υ der Phase entspricht.<sup>24</sup> Gemäß unserer Annahme hängt der Schwingungszustand der

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">24 Der Schwingungszustand eines angekoppelten Atoms ist nach dem Vorhergehenden eine erzwungene Schwingung mit der Frequenz ω, die von der erregenden Kraft der Schwingungsbewegung herrührt. ω<sub>0</sub> hingegen ist die Eigenfrequenz des angekoppelten Atoms. Die Phasenverschiebung der Schwingung aufeinanderfolgender angekoppelter Atome und damit die Ausbreitungsge-</span></small>

Welle nur von der Koordinate in der Ausbreitungsrichtung ab, ist also für jeden Punkt jeder Ebene normal zur Ausbreitungsrichtung gleich, wir sprechen dann von einer ebenen Welle ( plane wave).

Am Ort $x = 0$ herrsche zur Zeit t der folgende periodische Schwingungszustand als Folge eingeprägter Kräfte

$$
u (0, t) = u _ {0} \cos (\omega t). \tag {I-5.157}
$$

Durch die Phasenverzögerung, die sich durch die endliche Ausbreitungsgeschwindigkeit υ der Phase (= Schwingungszustand) ergibt, herrscht am Ort $x \neq 0$ jener Schwingungszustand, der am Ort $x = 0$ zur früheren Zeit $t = { \frac { x } { \nu } }$ geherrscht hat <sup>25</sup>

$$
u (x, t) = u _ {0} \cos \left[ \underbrace {\omega \left(t - \frac {x}{v}\right)} _ {\text {Phase}} \right]. \tag {I-5.158}
$$

Diese harmonische Welle wird also durch eine Wellenfunktion (wave function) u(x,t) beschrieben, die eine periodische Funktion der Zeit (am gleichen Ort, Abb. I-5.30) und eine periodische Funktion des Ortes zu einem bestimmten Zeitpunkt (Moment aufnahme im ganzen Raum, Abb. I-5.31) ist.

![](images/page_335_chart_8.jpg)

<details>
<summary>line</summary>

| Time (t) | Value (u) |
| --- | --- |
| 0 | ~-1.5 |
| t | 0 |
| t+T | 0 |
</details>

Abb. I-5.30: Eindimensionale harmonische Welle, betrachtet am festen Ort $X = X _ { 0 }$ als Funktion der Zeit.

Die Wellenlänge λ ist der Abstand zwischen zwei benachbarten Punkten desselben Schwingungszustandes, also derselben Phase, zu einem bestimmten Zeitpunkt.

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">schwindigkeit der Welle hängt wesentlich vom Verhältnis der erregenden Frequenz ω zur Eigenfrequenz ω<sub>0</sub> ab und erklärt so das Auftreten der Dispersion.</span></small>

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">25 t = x/υ ist die Zeit, die die Erregung braucht, um von x = 0, an den Ort x zu gelangen.</span></small>

![](images/page_336_chart_2.jpg)

<details>
<summary>line</summary>

| Feature | Value |
| --- | --- |
| Phase Shift (t) | t = t0 |
| Phase Shift (t) | t = t1 |
| Period (λ) | N/A |
| X-axis range | 0 ~ \(\lambda\) |
| Y-axis range | 0 ~ u |
</details>

Abb. I-5.31: Eindimensionale harmonische Welle, betrachtet als Momentaufnahme zu den Zeitpunkten $t = t _ { 0 }$ (durchgezogen) und $t = t _ { 1 }$ (punktiert).

Wir betrachten einen Momentanwert der Wellenfunktion zum Zeitpunkt $t = 0$ am Ort $X = X _ { 0 }$

$$
u (x _ {0}, 0) = u _ {0} \cos \left[ \omega \left(- \frac {x _ {0}}{\nu}\right) \right]. \tag {I-5.159}
$$

An der Stelle $x = x _ { 0 } + \lambda$ muss der gleiche Schwingungszustand herrschen, also gelten

$$
\cos \left[ \omega \left(- \frac {(x _ {0} + \lambda)}{\nu}\right) \right] = \cos \left[ \omega \left(- \frac {x _ {0}}{\nu}\right) \right]. \tag {I-5.160}
$$

Die Argumente der Winkelfunktionen müssen sich daher um 2 π unterscheiden

$$
\frac {\omega x _ {0}}{\nu} + \frac {\omega \lambda}{\nu} = \frac {\omega x _ {0}}{\nu} + 2 \pi \tag {I-5.161}
$$

und wir erhalten

$$
\frac {\omega \lambda}{\nu} = 2 \pi \quad \text {bzw.} \quad \nu = \frac {\omega}{2 \pi} \lambda = \nu \cdot \lambda .
$$

Das ist die für die Wellenlehre grundlegende Gleichung für die Ausbreitungsgeschwindigkeit υ der Phase, die in abgeänderter Form – siehe Fußnote – auch Dispersionsrelation (dispersion relation) genannt wird:<sup>26</sup>

$$
v _ {\mathrm{ph}} = \nu \cdot \lambda \tag {I-5.162}
$$

1 Die Phasengeschwindigkeit einer Welle ist gleich dem Produkt aus Frequenz und Wellenlänge.

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">26 Allgemein versteht man unter der Dispersionsrelation die Abhängigkeit der Kreisfrequenz ω = 2 πν von der Wellenzahl k = 2 π/λ, also ω = ω(k). Da die Phasengeschwindigkeit in materiellen Meω υph(k) 2 π dien von k abhängt, also υph = υph(k), ist hier also ω = ⋅υ h(k) = k⋅υ h(k) = ω(k) 2 π λ λ Dispersionsrelation.</span></small>

Wir definieren als Wellenzahl (wave number) $k = \frac { 2 \pi } { \lambda }$ und erhalten damit für die Phasengeschwindigkeit $\nu _ { \mathrm { p h } }$

$$
\nu_ {\mathrm{ph}} = \nu \cdot \lambda = \nu \cdot \frac {2 \pi}{k} = \frac {\omega}{k}.
$$

Damit können wir die Dispersionsrelation auch schreiben als

$$
v _ {\mathrm{ph}} (k) = \frac {\omega}{k} \quad \text {Dispersionsrelation (dispersion relation).} \tag {I-5.163}
$$

Wir kommen damit zu einer einfacheren und symmetrischeren Form der Wellenfunktion:

$$
u (x, t) = u _ {0} \cos (\omega t - k x) \quad \begin{array}{l} \text {Wellenfunktion (wave function)} \\ \text {einer ebenen Welle in x - Richtung.} \end{array} \tag {I-5.164}
$$

Die vollständige Beschreibung einer Welle, die keine reine Sinuswelle sein muss, erfordert wie bei der Schwingung eine Summe aus Sinus- und Kosinusfunktionen und kann auch in komplexer Darstellung erfolgen

$$
\begin{array}{l} u (x, t) = \sum_ {i} \left(A _ {i} \cos \left(\omega_ {i} t - k _ {i} x\right) + B _ {i} \sin \left(\omega_ {i} t - k _ {i} x\right)\right) = \\ = \sum_ {i} \left(c _ {i} e ^ {i (\omega_ {i} t - k _ {i} x)} + c _ {i} ^ {\star} e ^ {- i (\omega_ {i} t - k _ {i} x)}\right). \tag {I-5.165} \\ \end{array}
$$

Meist schreibt man für einen Wellenzug verkürzt

$$
u _ {i} (x, t) = A _ {i} \cos \left(\omega_ {i} t - k _ {i} x\right) = c _ {i} e ^ {i (\omega_ {i} t - k _ {i} x)} \tag {I-5.166}
$$

mit $c _ { i } = a _ { i } + i   b _ { i }$ und $\left| c _ { i } \right| = \sqrt { a _ { i } ^ { 2 } + b _ { i } ^ { 2 } }$ und versteht darunter stillschweigend $\operatorname { R e } \left( c _ { i } \cdot e ^ { i ( \omega _ { i } t - k _ { i } x ) } \right)$ . Mit $c _ { i } = \left| c _ { i } \right| e ^ { i \varphi _ { i } }$ , tan $\varphi _ { i } = { \frac { b _ { i } } { a _ { i } } }$ wird

$$
u _ {i} (x, t) = \left| c _ {i} \right| e ^ {i (\omega_ {i} t - k _ {i} x + \varphi_ {i})} \quad \text { bzw. }
$$

$$
u _ {i} (x, t) = \mathrm{Re} \left| c _ {i} \right| e ^ {i (\omega_ {i} t - k _ {i} x + \varphi_ {i})} = \left| c _ {i} \right| \cos \left(\omega_ {1} t - k _ {i} x + \varphi_ {i}\right); \tag {I-5.167}
$$

eine komplexe Amplitude ist also gleichbedeutend mit der Einführung eines Phasenwinkels.

## 5.5.2 Die Gruppengeschwindigkeit

Die Phasengeschwindigkeit kann bei der Wellenausbreitung in Medien von der Wellenlänge abhängen (Dispersion), dann gilt also $\nu _ { \mathrm { p h } } = \nu _ { \mathrm { p h } } ( \omega ) = \nu _ { \mathrm { p h } } ( \lambda )$ und es breiten sich Wellenzüge mit unterschiedlicher Wellenlänge auch mit unterschiedlicher Phasengeschwindigkeit aus. Ein weiteres Problem besteht darin, dass Naturvorgänge, die stets einen Anfang haben, nicht durch harmonische Funktionen beschrieben werden können, weil Sinus- und Kosinusfunktionen definitionsgemäß weder Anfang noch Ende besitzen. Die Berechtigung zur Beschreibung von Naturvorgängen mit harmonischen Funktionen beruht auf dem Fourierschen Integraltheorem, nach dem auch eine unperiodische Funktion durch Überlagerung von harmonischen Funktionen beschrieben werden kann. Die Wellenfunktion kann damit als Summe von unendlich vielen harmonischen Teilwellen (= Partialwellen, partial waves) dargestellt werden, die man Wellenpaket (= Wellengruppe, wave packet) nennt.

**Beispiel:** Wir betrachten die einfachste denkbare Wellengruppe, bestehend aus zwei Wellenzügen k und l mit den Wellenlängen $\lambda _ { k }$ und $\lambda _ { l } = \lambda _ { k } + \Delta \lambda$ die sich mit unterschiedlichen Phasengeschwindigkeiten

$$
\nu_ {\mathrm{ph}} ^ {k} = \nu_ {k} \cdot \lambda_ {k} = \frac {1}{T _ {k}} \lambda_ {k} \quad \text {und} \quad \nu_ {\mathrm{ph}} ^ {l} = \nu_ {l} \cdot \lambda_ {l} = \frac {1}{T _ {l}} (\lambda_ {k} + \Delta \lambda)
$$

ausbreiten. Die ‚längere‘ l-Welle habe die größere Phasengeschwindigkeit (das entspricht der normalen Dispersion in der Optik, siehe Band IV, Kapitel „Wellenoptik“, Abschnitt 1.3.3) und ihre Phase laufe in der gleichen Zeit weiter vor (in der Zeichnung unten nach rechts), als die Phase der k-Welle. Im Zeitraum Δt überhole die schnelle l-Welle die k-Welle um Δλ. Die Differenzgeschwindigkeit $\Delta \upsilon _ { \mathrm { p h } }$ der beiden Wellen ergibt sich also zu

$$
\Delta \nu_ {\mathrm{ph}} = \nu_ {\mathrm{ph}} ^ {l} - \nu_ {\mathrm{ph}} ^ {k} = \frac {\Delta \lambda}{\Delta t} \quad \text {und} \quad \Delta t = \frac {\Delta \lambda}{\Delta \nu_ {\mathrm{ph}}}.
$$

Wir betrachten die beiden Wellen k und l zur Zeit t: Zu diesem Zeitpunkt sollen beide Wellen in der Ebene A die gleiche Phase haben, nämlich beide ein Auslenkungsmaximum. Dort liegt damit zur Zeit t das Energiezentrum der Wellengruppe, die aus den beiden Einzelwellen k und l besteht. Zu diesem Zeitpunkt liegt in der Ebene B das Maximum der l-Welle um Δλ zurück.

Wir betrachten jetzt beide Wellen k und l zum Zeitpunkt $t + \Delta t .$ Im Zeitraum Δt überholt die schnelle l-Welle die langsamere k-Welle gerade um Δλ und das Energiezentrum der Wellengruppe liegt jetzt (siehe Zeichnung) in der Ebene B. Auf die mit der Geschwindigkeit $\nu _ { p h } ^ { k }$ weiterlaufende Phase A der k-Welle bezogen (wir ‚sitzen‘ quasi als Beobachter in der langsameren k-Welle) läuft also das Energiezentrum der Wellengruppe in der Zeit $\Delta t$ von A nach B, also um $\lambda _ { k }$ zurück (in der Zeichnung nach links), und zwar mit der Geschwindigkeit $\frac { \lambda _ { k } } { \Delta t } \underset { \nu o n   o b e n } { = } \lambda _ { k } \frac { \Delta \nu _ { \mathrm { p h } } } { \Delta \lambda }$ eingesetzt

![](images/page_339_chart_2.jpg)

<details>
<summary>line</summary>

| Feature | Description |
| --- | --- |
| Top Signal | v_ph^k |
| Bottom Signal | v_ph^l |
| X-axis Range | x |
| Y-axis Range | u |
| Peak 1 Position | B |
| Peak 1 Width | \(\lambda_k\) |
| Peak 2 Position | A |
| Peak 2 Width | \(\lambda_l\) |
| Welle k Position | w |
| Welle l Position | w |
| Welle l Width | \(\Delta\lambda\) |
| Welle l Height | \(v_\)ph^l > v_ph^k |
</details>

Da die Phase A der k-Welle aber mit $\nu _ { \mathrm { p h } } = \nu _ { \mathrm { p h } } ^ { k }$ weiterläuft (nach rechts), bewegt sich das Energiezentrum dazu um $\lambda _ { k } \frac { \Delta \upsilon _ { \mathrm { p h } } } { \Delta \lambda }$ langsamer, es gilt also für $\nu _ { \mathtt { g r } }$ die Geschwindigkeit des Energiezentrums, $\left| \nu _ { \mathrm { g r } } = \nu _ { \mathrm { p h } } - \lambda   \frac { \Delta \nu _ { \mathrm { p h } } } { \Delta \lambda } \right|$ bzw. im Grenzübergang differenziell kleiner Wellenlängenunterschiede

$$
\upsilon_ {\mathrm{gr}} = \upsilon_ {\mathrm{ph}} - \lambda \frac {d \upsilon_ {\mathrm{ph}}}{d \lambda}.
$$

Diese Ausbreitungsgeschwindigkeit des Energiezentrums einer Wellengruppe nennt man Gruppengeschwindigkeit (group velocity) $\nu _ { \mathtt { g r } }$

Der Differentialquotient $\frac { d \upsilon _ { \mathrm { p h } } } { d \lambda }$ beschreibt, wie sich die Phasengeschwindigkeit mit der Wellenlänge ändert und heißt Dispersion (dispersion).

Für die allgemeine Ableitung der Gruppengeschwindigkeit gehen wir von einer zeitlich beschränkten harmonischen Schwingung, also von einem Wellen-Puls aus. Bei Dispersion haben unterschiedliche Wellenlängen (und Frequenzen) der Fourierkomponenten eine unterschiedliche Ausbreitungsgeschwindigkeit, daher ändert sich die Form des Pulses im Laufe der Ausbreitung, er ‚zerfließt‘.

Wir betrachten wieder den einfachsten Fall einer Wellengruppe, die nur aus zwei Teilwellen besteht, die sich um $\Delta \omega$ in der Frequenz und Δk in der Wellenzahl unterscheiden

$$
u _ {1} (x, t) = u _ {0} \cos (\omega t - k x)
$$

$$
u _ {2} (x, t) = u _ {0} \cos \left((\omega + \Delta \omega) t - (k + \Delta k) x\right). \tag {I-5.168}
$$

Wir überlagern die beiden Wellen

$$
\begin{array}{l} u _ {1} + u _ {2} = 2 u _ {0} \cos \left(\frac {(2 \omega + \Delta \omega) t - (2 k + \Delta k) x}{2}\right) \cos \left(\frac {\Delta \omega}{2} t - \frac {\Delta k}{2} x\right) = \\ = 2 u _ {0} \cos \left(\left(\omega + \frac {\Delta \omega}{2}\right) t - \left(k + \frac {\Delta k}{2}\right) x\right) \cos \left(\frac {\Delta \omega}{2} t - \frac {\Delta k}{2} x\right). \tag {I-5.169} \\ \end{array}
$$

Unter der Annahme, dass sich die beiden Wellenzüge nur wenig in λ und damit auch in ω und k voneinander unterscheiden, dass also gilt $\Delta \omega \ll \omega$ und $\Delta k \ll k ,$ kann ohne wesentlichen Fehler geschrieben werden

$$
u _ {1} + u _ {2} = 2 u _ {0} \cos \left(\frac {\Delta \omega}{2} t - \frac {\Delta k}{2} x\right) \cos (\omega t - k x) = A \cdot \cos (\omega t - k x)
$$

$$
\mathrm{mit} \quad A = 2 u _ {0} \cos \left(\frac {\Delta \omega}{2} t - \frac {\Delta k}{2} x\right). \tag {I-5.170}
$$

Wir erhalten also für die Wellengruppe bestehend aus zwei nur wenig unterschiedlichen, harmonischen Wellen wieder eine harmonische Welle mit der Frequenz ω und der Wellenzahl k, jedoch mit einer sich räumlich und zeitlich (langsam) ändernden Amplitude. Bei einer Momentaufnahme (t = const.) oder bei festgehaltenem Ort (x = const.) ergibt sich eine Schwebung. Die Amplitude der Wellengruppe breitet sich selbst wellenförmig aus. Während für die Ausbreitungsgeschwindigkeit der Phase gilt $\nu _ { \mathrm { p h } } = \frac { \omega } { k }$ , gilt für die Ausbreitungsgeschwindigkeit der Amplitude A, also des Energiezentrums der Welle und damit der Gruppengeschwindigkeit entsprechend Gl. (I-5.170) analog $\nu _ { \mathrm { g r } } = \frac { \Delta \omega } { \Delta k }$ . Für beliebig kleine $\Delta \omega$ und $\Delta k ,$ das heißt für unendlich benachbarte Teilwellen, gilt daher

$$
\left. \begin{array}{l l} v _ {\mathrm{gr}} = \frac {d \omega}{d k} & \text {Gruppengeschwindigkeit (group velocity)} \\ v _ {\mathrm{ph}} = \frac {\omega}{k} & \text {Phasengeschwindigkeit (phase velocity).} \end{array} \right\} \quad \begin{array}{l} \text {Man beachte} \\ \text {die Analogie!} \end{array}
$$

Diese Ausbreitungsgeschwindigkeit der Amplitude A des Wellenpaketes ist die Gruppengeschwindigkeit des Wellenpakets u.

Wir können diese Form der Gruppengeschwindigkeit umschreiben

$$
\begin{array}{l} \omega = v _ {\mathrm{ph}} (k) \cdot k \\ \Rightarrow \quad \upsilon_ {\mathrm{gr}} = \frac {d \omega}{d k} = \upsilon_ {\mathrm{ph}} + k \cdot \frac {d \upsilon_ {\mathrm{ph}}}{d k}. \\ \end{array}
$$

Mit $k = \frac { 2 \pi } { \lambda }$ folgt

$$
d k = - \frac {2 \pi}{\lambda^ {2}} \cdot d \lambda .
$$

Oben eingesetzt erhalten wir

$$
\nu_ {\mathrm{gr}} = \frac {d \omega}{d k} = \nu_ {\mathrm{ph}} - \frac {2 \pi}{\lambda} \cdot \frac {d \nu_ {\mathrm{ph}}}{\frac {2 \pi}{\lambda^ {2}} d \lambda} = \nu_ {\mathrm{ph}} - \lambda \frac {d \nu_ {\mathrm{ph}}}{d \lambda} \tag {I-5.171}
$$

Es sind offenbar drei Fälle möglich: Die Gruppengeschwindigkeit kann kleiner, größer oder gleich der Phasengeschwindigkeit der Partialwellen sein, je nachdem, ob die Dispersion $\frac { d \upsilon _ { \mathrm { p h } } } { d \lambda }$ größer Null (normale Dispersion), kleiner (anomale Dispersion) oder gleich Null ist (keine Dispersion).

Grundsätzlich ist nur die Gruppengeschwindigkeit von Wellen experimentell bestimmbar, da man messbare Signale nur durch Aus- und Einschalten einer Welle geben kann, nicht aber durch die einzelnen Wellenberge oder Wellentäler einer unbegrenzten Welle, die von den benachbarten Bergen und Tälern nicht zu unterscheiden sind.

In der obigen Ableitung der Gruppengeschwindigkeit wurde nur die einfachste Möglichkeit einer Wellengruppe betrachtet, die nur aus zwei Teilwellen besteht. Man kann aber zeigen, dass das Ergebnis auch gilt, wenn die Wellengruppe aus unendlich vielen Teilwellen besteht, deren Frequenzen und Wellenzahlen ein Wertespektrum annehmen, also sich auch kontinuierlich ändern können.

Wie bereits in Abschnitt 5.1.3 gesehen, kann das Fouriersche Integraltheorem auf unperiodische raum-zeitliche Funktionen $u ( x , t )$ ausgedehnt werden

$$
u (x, t) = \frac {1}{2 \pi} \int_ {- \infty} ^ {+ \infty} F (k) \cdot e ^ {i (\omega (k) t - k x)} d k \quad \text {Fourierintegral des Pulsspektrums} F (k) \tag {I-5.172}
$$

$$
F (k) = \int_ {- \infty} ^ {+ \infty} u (x, t) \cdot e ^ {- i (\omega (k) t - k x)} d x \quad \begin{array}{l} \text {Fouriertransformierte} = \text {Amplituden-} \\ \text {spektrum eines Pulses} u (x, t). \end{array} \tag {I-5.173}
$$

Die Fouriertransformierte $F ( k )$ stellt das Amplitudenspektrum der durch $u ( x , t )$ beschriebenen Wellengruppe dar. Im Allgemeinen führt die Darstellung des sich ausbreitenden Wellenpaketes (Pulses) nur in einem kleinen Raumbereich zu merklichen Amplituden und verschwindet überall sonst im Raum durch destruktive Interferenz. Dies führt dazu, dass das Amplitudenspektrum $F ( k )$ nur in einem sehr kleinen Bereich um ein mittleres $k _ { 0 }$ von Null verschieden ist (Abb. I-5.32).<sup>27</sup>

![](images/page_342_chart_7.jpg)

<details>
<summary>line</summary>

| k | F(k) |
| --- | --- |
| \(-\Delta k\) | ~0 |
| \(k_{0}\) | Peak |
| \(+\Delta k\) | ~0 |
</details>

Abb. I-5.32: Fouriertransformierte F(k) (= Amplitudenspektrum) der Wellengruppe $u ( x , t )$

In diesem Fall kann man für das Wellenpaket in guter Näherung schreiben

$$
u (x, t) = \frac {1}{2 \pi} \int_ {k _ {0} - \Delta k} ^ {k _ {0} + \Delta k} F (k) \cdot e ^ {i (\omega t - k x)} d k. \tag {I-5.174}
$$

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">27 Hier gilt wieder die Reziprozität: Je breiter der Puls, desto schmäler das Amplitudenspektrum und umgekehrt.</span></small>

Wir beziehen jetzt die Wellenzahlen und Frequenzen der Teilwellen auf jene mit der größten Amplitude $F ( k _ { 0 } )$ , den Schwerpunkt des Wellenpaketes und können so schreiben

$$
k = k _ {0} + (k - k _ {0}) \quad \text {und} \quad \omega = \omega_ {0} + (\omega - \omega_ {0}) \tag {I-5.175}
$$

und entwickeln jetzt $\omega = \omega ( k )$ in sehr kleiner Umgebung von $k _ { 0 }$

$$
\omega = \omega \Big (k _ {0} + (k - k _ {0}) \Big) = \omega (k _ {0}) + \frac {d \omega}{d k} \bigg | _ {k _ {0}} (k - k _ {0}) = \omega_ {0} + \frac {d \omega}{d k} \bigg | _ {k _ {0}} (k - k _ {0}). \tag {I-5.176}
$$

Für k und $\omega$ in u (Gl. I-5.174) eingesetzt ergibt dies näherungsweise

$$
\begin{array}{l} u (x, t) \approx \frac {1}{2 \pi} \int_ {k _ {0} - \Delta k} ^ {k _ {0} + \Delta k} F (k) \cdot e ^ {i \left(\omega_ {0} t + \frac {d \omega}{d k} \Big | _ {k _ {0}} (k - k _ {0}) t - k _ {0} x - (k - k _ {0}) x\right)} d k = \\ = \frac {1}{2 \pi} \int_ {k _ {0} - \Delta k} ^ {k _ {0} + \Delta k} F (k) \cdot e ^ {i \left(\frac {d \omega}{d k} \right| _ {k _ {0}} (k - k _ {0}) t - (k - k _ {0}) x)} \cdot e ^ {i (\omega_ {0} t - k _ {0} x)} d k = \\ = F ^ {\prime} (x, t) \cdot e ^ {i (\omega_ {0} t - k x)} \tag {I-5.177} \\ \end{array}
$$

mit

$$
F ^ {\prime} (x, t) = \frac {1}{2 \pi} \int_ {k _ {0} - \Delta k} ^ {k _ {0} + \Delta k} F (k) \cdot e ^ {i \left(\frac {d \omega}{d k} \right| _ {k _ {s}} (k - k _ {0}) t - (k - k _ {0}) x)} d k \tag {I-5.178}
$$

als neuer Amplitudenfunktion des Wellenpaketes, $s ^ { 2 8 }$ deren Schwerpunkt sich an der Stelle befindet, an der sich die Phasen $\varphi = \frac { d \omega } { d k } \Bigg | _ { k _ { 0 } } ( k - k _ { 0 } ) t - ( k - k _ { 0 } ) x .$ der Teilwellen mit k nicht ändern, also konstruktiv interferieren. Dies ergibt die Bedingung ${ \frac { d \varphi } { d k } } = \left( { \frac { d \omega } { d k } }   t - x \right) = 0$ für den Ort des Maximums der Amplitudenfunktion, das sich also mit der Geschwindigkeit $\nu _ { \mathtt { g r } } = { \frac { x } { t } }$ , also mit

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">28 Hätten wir auch noch den zweiten Term in der Entwicklung, , mitgenommen, dk2 2 dann hätte sich gezeigt, dass die Halbwertsbreite von F′(x,t) mit der Zeit anwächst, das Wellenpaket also bei seiner Ausbreitung mit der Geschwindigkeit υ<sub>gr</sub> „zerfließt“.</span></small>

$$
\nu_ {\mathrm{gr}} = \frac {d \omega (k)}{d k} \Bigg | _ {k _ {0}} \tag {I-5.179}
$$

in der x-Richtung ausbreitet.

## 5.5.3 Die Wellengleichung

Wir sind bisher von ebenen Wellen ausgegangen, die sich in x-Richtung ausbreiten. Wir wollen jetzt zunächst die Ausbreitung von ebenen Wellen mit beliebiger Ausbreitungsrichtung im Raum betrachten.

Zur Beschreibung der Ausbreitungsrichtung verwenden wir den Wellenvektor $\vec { k } = \left\{ k _ { x } , k _ { y } , k _ { z } \right\}$ mit dem Betrag der Wellenzahl $k = \left| { \vec { k } } \right| = { \frac { 2 \pi } { \lambda } }$ und der Richtung senkrecht zu den Wellenflächen, also den Flächen gleicher Phase.

Wir betrachten die Ortsvektoren $\vec { r } _ { 1 }$ und $\vec { r } _ { 2 }$ zu zwei Punkten einer Ebene normal zur Ausbreitungsrichtung $\vec { k } ,$ also einer Phasenfläche (wavefront) (Abb. I-5.33). Ihr Differenzvektor $\vec { r } _ { 2 } - \vec { r } _ { 1 }$ muss in dieser Ebene liegen, sein Skalarprodukt mit dem Wellenvektor muss daher verschwinden

$$
\vec {k} \cdot (\vec {r} _ {1} - \vec {r} _ {2}) = 0 \quad \text {bzw.} \quad \vec {k} \cdot \vec {r} _ {1} = \vec {k} \cdot \vec {r} _ {2}. \tag {I-5.180}
$$

![](images/page_344_image_9.jpg)

<details>
<summary>text_image</summary>

z
d
r₂
r₂ - r₁
Phasenflächen
r₁
O
y
x
k
</details>

Abb. I-5.33: Phasenflächen ebener Wellen mit beliebiger Ausbreitungsrichtung im Raum.

Flächen konstanter Phase, die Phasenflächen, werden daher charakterisiert durch

$$
\vec {k} \cdot \vec {r} = \text {const.} = k \cdot r \cdot \cos (\vec {k}, \vec {r}) = k \cdot d \tag {I-5.181}
$$

mit d als Abstand der Phasenflächen vom Ursprung und der Wellenzahl $k   =   2   \pi / \lambda$

Für die Darstellung einer ebenen Welle mit beliebiger Ausbreitungsrichtung im Raum folgt dann mit derselben Argumentation wie in Abschnitt 5.5.1

$$
u (\vec {r}, t) = u _ {0} \cos \left(\omega t - \vec {k r}\right) \triangleq c \cdot e ^ {i (\omega t - \vec {k r})} = c \Big (e ^ {i (\omega t - k d)} \Big) \tag {I-5.182}
$$

Wellenfunktion einer ebenen Welle mit beliebiger Ausbreitungsrichtung $\vec { k }$

Die Phasengeschwindigkeit $\nu _ { \mathrm { p h } }$ ergibt sich aus $\frac { d } { d t } \left( \omega t - k d \right) = 0$ wieder zu (Gl. I-5.163)

$$
v _ {\mathrm{ph}} = \frac {\omega}{k}.
$$

Wir suchen jetzt nach jener Differentialgleichung (DG), für die ebene Wellen eine Lösung darstellen. Dazu setzen wir zunächst eine ganz allgemeine Wellenfunktion für ebene skalare Wellen $\mathbf { a } \mathbf { n } ^ { 2 9 }$

$$
u (\vec {r}, t) = A \cdot f (\omega t - \vec {k} \vec {r}) = A \cdot f (g) \tag {I-5.183}
$$

mit

$$
g = \omega t - \vec {k r} = \omega t - k _ {x} x - k _ {y} y - k _ {z} z.
$$

Dabei ist $f ( g )$ eine beliebige, zweimal differenzierbare Funktion. Auch diese allgemeine Funktion $f ( g )$ breitet sich in der $\vec { k } -$ Richtung mit der Phasengeschwindigkeit $\nu _ { \mathrm { p h } } = \frac { \omega } { k }$ aus und da die Phasenflächen $( \omega t - \vec { k } \vec { r } )$ = const. senkrecht zu $\vec { k }$ liegen, sind es wieder ebene Wellen.

Wir differenzieren zuerst zweimal nach den Ortskoordinaten

$$
\begin{array}{l} \frac {\partial u}{\partial x} = A \cdot \frac {d f}{d g} \frac {\partial g}{\partial x} = - A \cdot f ^ {\prime} (g) \cdot \left[ \frac {\partial}{\partial x} \left(k _ {x} x + k _ {y} y + k _ {z} z\right) \right] = \\ = - A \cdot f ^ {\prime} (g) \cdot \left(k _ {x} \underbrace {\frac {\partial x}{\partial x}} _ {= 1}\right) = - A \cdot k _ {x} \cdot f ^ {\prime} (g) \\ \frac {\partial^ {2} u}{\partial x ^ {2}} = - A \cdot k _ {x} \cdot f ^ {\prime \prime} (g) \frac {\partial g}{\partial x} = A \cdot k _ {x} ^ {2} \cdot f ^ {\prime \prime} (g) \tag {I-5.184} \\ \end{array}
$$

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">29 Ein Beispiel für skalare Wellen sind die Druckwellen (= Schallwellen) in einem Gas (z. B. Luft).</span></small>

analog für die y- und z-Koordinate

$$
\frac {\partial^ {2} u}{\partial y ^ {2}} = A \cdot k _ {y} ^ {2} \cdot f ^ {\prime \prime} (g), \frac {\partial^ {2} u}{\partial z ^ {2}} = A \cdot k _ {z} ^ {2} \cdot f ^ {\prime \prime} (g) \tag {I-5.185}
$$

und dann zweimal nach der Zeit

$$
\frac {\partial u}{\partial t} = A f ^ {\prime} (g) \frac {\partial g}{\partial t} = A \cdot \omega \cdot f ^ {\prime} (g)
$$

$$
\frac {\partial^ {2} u}{\partial t ^ {2}} = A \cdot \omega \cdot f ^ {\prime \prime} (g) \frac {\partial g}{\partial t} = A \cdot \omega^ {2} \cdot f ^ {\prime \prime} (g). \tag {I-5.186}
$$

Die Summation der zweifachen Ortsableitungen ergibt den Laplace-Operator Δu

$$
\frac {\partial^ {2} u}{\partial x ^ {2}} + \frac {\partial^ {2} u}{\partial y ^ {2}} + \frac {\partial^ {2} u}{\partial z ^ {2}} = \Delta u = A \cdot f ^ {\prime \prime} (g) (k _ {x} ^ {2} + k _ {y} ^ {2} + k _ {z} ^ {2}) = A \cdot k ^ {2} \cdot f ^ {\prime \prime} (g). ^ {3 0} \tag {I-5.187}
$$

Aus der zweifachen Zeitableitung folgt

$$
f ^ {\prime \prime} (g) = \frac {1}{A \cdot \omega^ {2}} \frac {\partial^ {2} u}{\partial t ^ {2}}. \tag {I-5.188}
$$

Wir erhalten durch Elimination von $f ^ { \prime \prime } ( g )$

$$
\frac {\Delta u}{A k ^ {2}} = \frac {1}{A \omega^ {2}} \cdot \frac {\partial^ {2} u}{\partial t ^ {2}} \tag {I-5.189}
$$

und so

$$
\Delta u = A \cdot k ^ {2} \cdot \frac {1}{A \cdot \omega^ {2}} \frac {\partial^ {2} u}{\partial t ^ {2}} = \frac {k ^ {2}}{\omega^ {2}} \frac {\partial^ {2} u}{\partial t ^ {2}} = \frac {1}{v _ {\mathrm{ph}} ^ {2}} \frac {\partial^ {2} u}{\partial t ^ {2}} \tag {I-5.190}
$$

mit $\nu _ { \mathrm { p h } } = { \frac { \omega } { k } } .$

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">30 Hieraus ist zu ersehen, dass wir die 2. Ableitungen bilden mussten, um im Ergebnis den richtungsunabhängigen Betrag kdes Ausbreitungsvektors zu erhalten.</span></small>

Damit haben wir eine sehr allgemeine DG erhalten, der alle skalaren, ebenen Wellenfunktionen $f ( \omega t - \vec { k } \vec { r } )$ genügen

$$
\Delta u = \frac {1}{\nu_ {\mathrm{ph}} ^ {2}} \frac {\partial^ {2} u}{\partial t ^ {2}} \quad \begin{array}{l} \text {allgemeine Wellengleichung (wave equation)} \\ \text {für ebene skalare Wellenfunktionen.} ^ {3 1} \end{array} \tag {I-5.191}
$$

Liegt statt einer ebenen Skalarwelle eine ebene Vektorwelle vor, so gilt die Wellengleichung für jede der drei Komponenten

$$
\Delta \vec {u} = \frac {1}{v _ {\mathrm{ph}} ^ {2}} \frac {\partial^ {2} \vec {u}}{\partial t ^ {2}} \quad \begin{array}{l l} & \text {allgemeine Wellengleichung} \\ & \text {für ebene vektorielle Wellenfunktionen.} ^ {3 2} \end{array} \tag {I-5.192}
$$

Eine mögliche Lösung dieser Gleichung stellen harmonische Wellen dar (Gl. I-5.182):

$$
\vec {u} (\vec {r}, t) = \vec {u} _ {0} \cos \left(\omega t - \vec {k} \vec {r}\right) \triangleq \vec {c} \cdot e ^ {i (\omega t - \vec {k} \vec {r})}. ^ {3 3}
$$

Die Wellengleichung für die Vektorwelle zerfällt also in drei unabhängige skalare Wellengleichungen für die drei Raumkomponenten.

Ist der Vektor u⇀stets parallel zur Ausbreitungsrichtung, so sprechen wir von einer reinen longitudinalen Welle (longitudinal wave).<sup>34</sup>

Hat u⇀dagegen keine Komponente in der Ausbreitungsrichtung, sondern ist stets normal dazu, sprechen wir von einer reinen Transversalwelle (transverse wave).<sup>35</sup> u⇀kann dann in zwei Teilkomponenten zerlegt werden, die parallel zu jenen Achsrichtungen sind, die senkrecht auf die Ausbreitungsrichtung stehen. Besteht keine Phasendifferenz zwischen diesen beiden Komponenten des Vektors u⇀, so ist die gesamte Auslenkung bei gleicher Phasengeschwindigkeit der Komponenten an jedem Ort linear. Es handelt sich um eine linear polarisierte (linearly polarized) Welle, die Schwingungsebene des Vektors u⇀wird von der Ausbreitungsrichtung und der Schwingungsrichtung gebildet. Diese Ebene wird auch Polarisationsebene (plane of polarization) genannt. Bei einer Phasendifferenz zwischen den beiden Komponenten bleibt die Schwingungsebene nicht konstant, sondern dreht sich um die Ausbreitungsrichtung.

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">31 Die Gleichung wurde nur für ebene Wellen abgeleitet, sie gilt aber für jeden Wellenvorgang, da sich dieser immer durch Überlagerung ebener Wellen darstellen läßt.</span></small>

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">32 Für den Laplace-Operator einer vektoriellen Größe siehe Kapitel „Deformierbare Körper“, Abschnitt 4.3.2, Anmerkung zu Gl. (I-4.58).</span></small>

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">33 Aus der obigen Ableitung ist ersichtlich, dass jede zweimal differenzierbare Funktion f (ωt − k⇀r⇀) – wovon wir ja bei unserer Ableitung der DG ausgegangen sind – eine Lösung der Wellengleichung ist. Sie wird als d’Alembertsche Lösung bezeichnet (nach Jean-Baptiste le Rond d’Alembert, 1717−1783). Die Phasenflächen (ωt − k⇀r⇀) = const. bewegen sich mit der Phasengeschwindigkeit ω υph k in k⇀-Richtung. Die Funktion f (ωt − k⇀r⇀) = kf (υ ht − d) mit d = k⇀r⇀verschiebt sich ohne zu „zerfließen“ in der k⇀-Richtung weiter, denn bei der Ableitung der d’Alembertschen Lösung ist vorausgesetzt, dass die Phasengeschwindigkeit <sup>υ</sup>ph = const. ist. Wenn dies nicht der Fall ist (wie in materiellen Medien), dann muss die Funktion f in n Teile zerlegt werden, für die die zugehörigen Phasengeschwindigkeiten <sup>υ</sup>ph,n wieder konstant sind und die n Teile müssen wieder zur Gesamtlö- sung addiert werden. Dieser Vorgang wird bei der Fouriersynthese praktiziert.</span></small>

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">34 Z. B. die Welle der Auslenkung in einer Schallwelle.</span></small>

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">35 Z. B. die Scherwelle in einem Kristall oder die Feldstärken in elektromagnetischen Wellen.</span></small>

Überlagern sich zwei zueinander senkrecht stehende, linear polarisierte Wellen, die also normal zur Ausbreitungsrichtung schwingen, so breitet sich i. Allg. (Phasendifferenz $\Delta \varphi \neq 0 )$ eine elliptisch polarisierte (eliptically polarized) Welle aus. Ein Spezialfall davon ist die zirkular polarisierte (circularly polarized wave) Welle, wenn die beiden sich überlagernden Wellen um $\pm \pi / 2$ gegeneinander phasenverschoben und die Amplituden gleich sind (links- bzw. rechtszirkular polarisierte (left- and right circularly polarized) Wellen). Siehe dazu auch Band III, Kapitel „Wechselstromkreis und elektromagnetische Schwingungen und Wellen“, Abschnitt 5.5.3 ‚Polarisation elektromagnetischer Wellen‘ und Band IV, Kapitel „Wellenoptik“, Abschnitt 1.4.2.

## Kugelwellen (siehe dazu auch Abschnitt 5.6.5)

In vielen Fällen, z. B. bei Schallwellen, bei denen die Erregung meist in einem Bereich erfolgt, der klein gegen die Wellenlänge ist, breiten sich Wellen im Raum von einem Erregerzentrum ausgehend gleichförmig in allen Richtungen aus und bilden kugelförmige Wellenfronten, die überall senkrecht auf der Ausbreitungsrichtung stehen (Abb. I-5.34).<sup>36</sup> Wir sprechen von einer Kugelwelle (spherical wave).

![](images/page_348_image_6.jpg)

<details>
<summary>text_image</summary>

r₁
r₂
λ
vₚₕ
</details>

Abb. I-5.34: Bei einer Kugelwelle breiten sich Wellen mit kugelförmigen Wellenfronten von einem Erregerzentrum ausgehend gleichförmig in alle Richtungen aus. Ihre Intensität I nimmt mit $1 / r ^ { 2 }$ ab.

$$
\begin{array}{l} I _ {1} = \frac {\bar {P}}{4 \pi r _ {1} ^ {2}}, I _ {2} = \frac {\bar {P}}{4 \pi r _ {2} ^ {2}} \\ \Rightarrow \frac {I _ {1}}{I _ {2}} = \frac {r _ {2} ^ {2}}{r _ {1} ^ {2}} \quad (\text {siehe Text }) \\ \end{array}
$$

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">36 Streng gilt dies aber nur, wenn der Erreger eine mit der Frequenz ν pulsierende Kugel ist.</span></small>

Im Kapitel „Mechanik deformierbarer Körper“, Abschnitt 4.3.6, Beispiel ‚Radialströmung‘ wurde gezeigt, dass im Falle einer kugelsymmetrischen Potenzialfunktion Φ(r) (Φ(r) hängt nur von r ab), die Laplace-Gleichung folgende Gestalt annimmt:

$$
\Delta \Phi = \frac {\partial^ {2} \Phi}{\partial r ^ {2}} + \frac {2}{r} \frac {\partial \Phi}{\partial r} = \frac {1}{r} \frac {\partial^ {2}}{\partial r ^ {2}} (r \cdot \Phi). \tag {I-5.193}
$$

Die Wellengleichung lautet also in diesem Fall (r ist eine unabhängige Variable, die nicht von t abhängt!)

$$
\Delta u (r, t) = \frac {1}{r} \frac {\partial^ {2}}{\partial r ^ {2}} (r \cdot u) = \frac {1}{v _ {\mathrm{ph}} ^ {2}} \frac {\partial^ {2} u}{\partial t ^ {2}} \Rightarrow \frac {\partial^ {2} (r u)}{\partial r ^ {2}} = \frac {r}{v _ {\mathrm{ph}} ^ {2}} \frac {\partial^ {2} u}{\partial t ^ {2}} = \frac {1}{v _ {\mathrm{ph}} ^ {2}} \frac {\partial^ {2} (r \cdot u)}{\partial t ^ {2}}. \tag {I-5.194}
$$

Das ist aber die eindimensionale Wellengleichung für die neue Wellenfunktion $( r \cdot u )$ , deren Lösung in Form der d’Alembertschen Lösung vorliegt:

$$
r \cdot u = f (\omega t - k r) \Rightarrow u = \frac {1}{r} f (\omega t - k r). \tag {I-5.195}
$$

Im Falle einer harmonischen Kugelwelle kann daher die Wellenfunktion in folgender Weise angeschrieben werden

$$
u (x, t) = \frac {A}{r} \cos (\omega t - k r) = \frac {A}{r} e ^ {i (\omega t - k r)} \quad \begin{array}{l l} & \text {Wellenfunktion} \\ & \text {einer Kugelwelle.} \end{array} \tag {I-5.196}
$$

Die Intensität I einer Welle in einem bestimmten Raumpunkt ist die Leistung (Energie pro Zeit), die durch die Einheitsfläche senkrecht zur Ausbreitungsrichtung in diesem Punkt hindurchtritt. Da sich bei einer Kugelwelle die von der Quelle ausgesandte Energie in alle Richtungen gleichmäßig mit der Geschwindigkeit $\nu _ { \mathrm { p h } }$ ausbreitet, muss diese Energie in jeder Entfernung r vom Erregerzentrum gleichmäßig über die Kugelflächen $4   \pi r ^ { 2 }$ verteilt sein und es muss im stationären Zustand für die Intensität im Abstand r gelten

$$
I _ {r} = \frac {\bar {P}}{4 \pi r ^ {2}}, \quad \text {also} \quad I \propto \frac {1}{r ^ {2}} \quad \begin{array}{l} (\bar {P} \dots \text {mittlere, von der Quelle} \\ \text {ausgestrahlte Leistung).} \end{array} \tag {I-5.197}
$$

In Abschnitt 5.5.5 (Gl. I-5.231) wird gezeigt, dass die Intensität einer Welle andererseits proportional zum Quadrat der Schwingungsamplitude ist. Da diese gleich $\frac { A } { r }$ beträgt, nimmt also die Intensität mit ${ \frac { 1 } { r ^ { 2 } } }   \mathsf { a b }$ , wie dies gerade gezeigt wurde.

## 5.5.4 Ausbreitung von mechanischen Wellen

Da in (idealen) Flüssigkeiten und Gasen der Schermodul $G = 0$ ist, sind nur longitu dinale oder skalare Wellen möglich.<sup>37</sup> Die Kopplung zwischen den schwingenden Molekülen erfolgt in Fluiden durch lokale Druck- und Dichteänderungen. Schallwellen in Flüssigkeiten und Gasen zeichnen sich dadurch aus, dass die auftreten den Geschwindigkeiten gegenüber ihren zeitlichen und räumlichen Ableitungen so klein sind, dass Produkte dieser Größen mit υ⇀vernachlässigt werden können. Man kann daher in der Eulergleichung (siehe Kapitel „Mechanik deformierbarer Körper“, Abschnitt 4.3.2, Gl. I-4.57) den Vektor-Gradiententerm weglassen und erhält, wenn keine äußeren Kräfte wirken, die linearisierte Eulergleichung

$$
\frac {\partial \vec {v}}{\partial t} = - \frac {1}{\rho} \vec {\nabla} P. \tag {I-5.198}
$$

Wir untersuchen zuerst Wellen in kompressiblen Medien (Gasen) und nehmen dazu an, dass durch kleine Dichteschwankungen Abweichungen $\Delta \bar { \rho }$ vom Durchschnittswert $\bar { \rho }$ verursacht werden, setzen also

$$
\rho = \bar {\rho} \Big (1 + \delta (t, x, y, z) \Big) \tag {I-5.199}
$$

mit $\delta = \frac { \rho - \overline { { \rho } } } { \overline { { \rho } } } = \frac { \Delta \rho } { \overline { { \rho } } }$ , der relativen Dichteschwankung und $\vec { \upsilon } = \bar { \vec { \upsilon } } + \delta \vec { \upsilon } .$

Setzen wir das in die Kontinuitätsgleichung $\frac { \partial \rho } { \partial t } + \mathrm { d i v } ( \rho \vec { v } ) = 0 ,$ (Kapitel „Mechanik deformierbarer Körper“, Abschnitt 4.3.1, Gl. I-4.48) ein und vernachlässigen die gegen 1 kleine Größe $\delta ,$ so folgt

$$
\begin{array}{l} \frac {\partial \rho}{\partial t} + \mathrm{div} (\rho \vec {v}) = \frac {\partial (\bar {\rho} + \bar {\rho} \delta)}{\partial t} + \mathrm{div} (\bar {\rho} \vec {v} + \bar {\rho} \delta \vec {v}) = \\ = \underbrace {\frac {\partial \bar {\rho}}{\partial t}} _ {= 0, \bar {\rho} = \text {const.}} + \underbrace {\delta \frac {\partial \bar {\rho}}{\partial t}} _ {= 0} + \bar {\rho} \frac {\partial \delta}{\partial t} + \operatorname{div} \bar {\rho} \vec {v} + \underbrace {\operatorname{div} \bar {\rho} \delta \vec {v}} _ {\substack {\text {vernachlässigt, da}\\ \text {sehr klein gegen}\\ \text {den vorhergehenden}\\ \text {Term}}} = \\ = \bar {\rho} \frac {\partial \delta}{\partial t} + \bar {\rho} \operatorname{div} \vec {v} = 0 ^ {3 8} \tag {I-5.200} \\ \end{array}
$$

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">37 Eine Ausnahme stellen die Oberflächenwellen von Wasser dar, bei denen die Oberflächenspannung und die Schwerkraft eine rücktreibende Querkraft erzeugen und daher Transversalwellen in der Oberflächenschicht ermöglichen. In diesen Oberflächenwellen führen die Wassermoleküle Kreisbewegungen aus, diese Wellen zeigen außerdem Dispersion.</span></small>

<small><span class="docvortex-page-footnote" data-block-type="page_footnote" style="color:#6b7280">38 Im Folgenden bezeichnen wir die mittlere Geschwindigkeit υ⇀wieder mit υ⇀.</span></small>

und damit

$$
\frac {\partial \delta}{d t} + \operatorname{div} \vec {v} = 0 \quad \text {Kontinuitätsgleichung im Schallfeld.} \tag {I-5.201}
$$

Wir wollen im Folgenden in der Eulergleichung den Druckgradienten $\vec { \nabla } P$ durch den Gradienten der Dichteschwankungen $\vec { \nabla } \delta$ ersetzen, um zu einer Differentialgleichung für $\delta$ zu gelangen.

Da die Dichteschwankungen zwischen $\rho$ und $\bar { \rho }$ während der Gasschwingungen so rasch erfolgen, dass kein Temperaturausgleich stattfinden kann, müssen wir statt der isothermen Gasgleichung (Boyle-Mariotte) die adiabatische Gasgleichung (Poissongleichung) (siehe Band II, Kapitel „Physik der Wärme“, Abschnitt 1.3.1.2.4) mit dem Adiabatenkoeffizienten $\kappa = \frac { C _ { P } } { c _ { V } }$ verwenden

$$
P \cdot V ^ {\kappa} = \text {const.} \quad \Rightarrow \quad P \cdot V ^ {\kappa} = \bar {P} \cdot \bar {V} ^ {\kappa} \tag {I-5.202}
$$

und mit $V \propto \frac { 1 } { \rho }$

$$
\frac {P}{\bar {P}} = \left(\frac {\rho}{\bar {\rho}}\right) ^ {\kappa} = \left(\frac {\bar {\rho} + \bar {\rho} \delta}{\bar {\rho}}\right) ^ {\kappa} = (1 + \delta) ^ {\kappa} \underset {\text {Taylor}} {=} (1 + \kappa \delta). \tag {I-5.203}
$$

Damit wird

$$
P = \bar {P} + \bar {P} \kappa \delta \text {und} \operatorname{grad} P = \bar {P} \cdot \kappa \cdot \operatorname{grad} \delta . \tag {I-5.204}
$$

Unter neuerlicher Vernachlässigung von Produkten kleiner Größen ergibt sich

$$
\frac {1}{\rho} \operatorname{grad} P = \frac {1}{\bar {\rho} + \underbrace {\bar {\rho} \delta} _ {\approx 0}} \operatorname{grad} P = \frac {1}{\bar {\rho}} \bar {P} \cdot \kappa \cdot \operatorname{grad} \delta . \tag {I-5.205}
$$

In die Eulergleichung (I-5.198) eingesetzt erhalten wir

$$
\frac {\partial \vec {v}}{\partial t} = - \frac {1}{\rho} \vec {\nabla} P = - \frac {1}{\bar {\rho}} \bar {P} \kappa \cdot \vec {\nabla} \delta . \tag {I-5.206}
$$

Um $\bar { v }$ aus der Eulergleichung und der Kontinuitätsgleichung zu eliminieren, differenzieren wir die Kontinuitätsgleichung (I-5.201) nochmals nach $t ,$ wobei wir beachten, dass die zeitliche und die örtliche Differentiation vertauscht werden kann