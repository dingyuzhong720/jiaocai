# Titel, Vorwort und Inhaltsverzeichnis

原始 PDF 第 1–16 页。

Springer-Lehrbuch

---

## Springer

Berlin

Heidelberg

New York

Barcelona

Budapest

Hongkong

London

Mailand

Paris

Santa Clara

Singapur

Tokio

---

Kurt Meyberg · Peter Vachenauer

# Höhere Mathematik 1

Differential- und Integralrechnung
Vektor- und Matrizenrechnung

Vierte, korrigierte Auflage
Mit 450 Abbildungen

![](../../raw/pages_0001-0032/images/page_2_image_4.jpg)

Springer

---

Professor Dr. Kurt Meyberg

Dr. Peter Vachenauer

Zentrum Mathematik

der Technischen Universität München

Arcisstraße 21

D-80333 München

e-mail:

(meyberg|vach)@mathematik.tu-muenchen.de

Mathematics Subject Classification (1991):

00A05, 00-01, 00A06

ISBN-13: 978-3-540-63688-5

e-ISBN-13: 978-3-642-97724-4

DOI: 10.1007/978-3-642-97724-4

Die Deutsche Bibliothek – CIP-Einheitsaufnahme

Meyberg, Kurt: Höhere Mathematik/Kurt Meyberg; Peter Vachenauer. – Berlin; Heidelberg; New York; Barcelona;

Budapest; Hongkong; London; Mailand; Paris; Santa Clara; Singapur; Tokio: Springer

(Springer-Lehrbuch)

1. Differential- und Integralrechnung, Vektor- und Matrizenrechnung. - 4. Aufl. - 1997

ISBN-13: 978-3-540-63688-5

Dieses Werk ist urheberrechtlich geschützt. Die dadurch begründeten Rechte, insbesondere die der Übersetzung, des Nachdrucks, des Vortrags, der Entnahme von Abbildungen und Tabellen, der Funksendung, der Mikroverfilmung oder der Vervielfältigung auf anderen Wegen und der Speicherung in Datenverarbeitungsanlagen, bleiben, auch bei nur auszugsweiser Verwertung, vorbehalten. Eine Vervielfältigung dieses Werkes oder von Teilen dieses Werkes ist auch im Einzelfall nur in den Grenzen der gesetzlichen Bestimmungen des Urheberrechtsgesetzes der Bundesrepublik Deutschland vom 9. September 1965 in der jeweils geltenden Fassung zulässig. Sie ist grundsätzlich vergütungspflichtig. Zuwiderhandlungen unterliegen den Strafbestimmungen des Urheberrechtsgesetzes.

© Springer-Verlag Berlin Heidelberg 1991, 1993, 1995, 1998

Datenkonvertierung: Universitätsdruckerei H. Stürtz AG, Würzburg

SPIN: 10652532

44/3143 - 5 4 3 2 1 0 - Gedruckt auf säurefreiem Papier

---

# Vorwort zur vierten Auflage

Für diese Auflage haben wir nur geringe Textänderungen vorgenommen und vor allem weitere hartnäckige Druckfehler beseitigt sowie den Text in mehreren Passagen verständlicher gestaltet. Auf viele dieser Stellen wurden wir wieder vor allem durch die freundlichen Hinweise aufmerksam gemacht, für die wir uns sehr herzlich bedanken möchten.

Auch in Zukunft werden wir uns über jeden wohlwollenden Verbesserungsvorschlag freuen und ihn im gegebenen Rahmen berücksichtigen.

München, im August 1997

Kurt Meyberg Peter Vachenauer

## Vorwort zur ersten Auflage

Dieses zweibändige Lehrbuch ist aus den Vorlesungen und Übungen der Verfasser zur Höheren Mathematik für Ingenieure der Fachrichtungen Maschinenbau und Elektrotechnik an der Technischen Universität München hervorgegangen. Es ist in erster Linie als kompakter Begleittext zur viersemestrigen Grundvorlesung für die Studenten der Ingenieurwissenschaften und anderer technischphysikalischer Studienfächer (etwa Physik, Technomathematik und Informatik) konzipiert.

Da die moderne Technik vom Ingenieur immer umfassendere und tiefere mathematische Kentnisse verlangt, gehen wir an einigen Stellen über den üblichen Vorlesungsstoff der Grundkurse hinaus oder stellen einige Themen gründlicher dar, als es in den Vorlesungen möglich ist. Das betrifft im vorliegenden Band insbesondere in Kapitel 6 den Ausflug in die abstrakte Welt der Vektorräume und in allen Kapiteln die stärkere Berücksichtigung der wichtigsten numerischen Aspekte. Damit ist dieses Buch auch für Studenten höherer Semester zur Fortbildung und für den Praktiker als Nachschlagewerk geeignet.

Die in Kapitel 1 dargestellte Vektorrechnung, insbesondere die Behandlung gebundener Vektoren, ist den Bedürfnissen der Technischen Mechanik angepaßt, sie kann für andere Fachrichtungen abgekürzt oder ausgelassen werden. Andererseits besteht die Notwendigkeit, die algebraischen und numerischen Methoden bereits in den Grundkursen stärker zu berücksichtigen. Die Lineare Algebra in Kapitel 6 ist unabhängig vom Vorhergehenden und kann vorgezogen, eventuell parallel mit den Kapiteln 2 – 5 behandelt werden.

Der Praktiker erwartet von der Mathematik nicht nur Erkenntnis, sondern Resultate. Wir berücksichtigen die für ihn besonders wichtige algorithmische Seite der Mathematik durch im Druck hervorgehobene Überblicke mit detaillierten Rechenschemata. Sie enthalten – in Schritten aufgegliedert – die Methoden zum Lösen konkreter Aufgaben und können nicht zuletzt als Repetitorium zur Prüfungsvorbereitung dienen.

---

VI

Vorwort zur ersten Auflage

Ferner fügen wir eine größere Zahl von Programmen ein, die auf erprobten numerischen Algorithmen fußen. Wir haben uns zur Darstellung dieser Programme für die Programmiersprache GfA-Basic entschieden, da diese einerseits die zugrundeliegenden Algorithmen besonders gut erkennen läßt, andererseits aufgrund ihrer Strukturierung vom etwas geübten Programmierer leicht in jede höhere Sprache übersetzt werden kann. In erster Linie ist aber an den Einsatz der Programme auf studienbegleitenden Taschen- oder Kleinrechnern gedacht.

Für den verständnisvollen Umgang mit den mathematischen Modellen der Physik und der Technik reicht die Fähigkeit im Anwenden fertiger Rezepte natürlich nicht aus. Unerläßlich ist auch die Kenntnis der mathematischen Grundlagen und vielfältigen Methoden, mit denen sie behandelt werden. Wir haben deshalb alle wesentlichen Beweise ausgeführt. Der Studienanfänger kann einen Teil dieser Beweise und die mit \* gekennzeichneten Abschnitte beim ersten Durcharbeiten auslassen; er sollte sich dafür verstärkt mit den zahlreichen ausführlich vorgerechneten Beispielen und den einfacheren Übungsaufgaben beschäftigen. Der etwas geübtere Leser wird die straffe Darstellung der anspruchsvolleren Beweise sicher schätzen. Für ihn sollten auch die schwierigeren Aufgaben eine Herausforderung bedeuten.

Die Verfasser sind den Kollegen und Mitarbeitern an der Technischen Universität München sehr dankbar, die durch ihre Hilfe, manch guten Rat und viele Gespräche über Inhalte und Darstellung der „Ingenieurmathematik“ zum Entstehen dieses Buches beigetragen haben. Insbesondere danken wir Prof. Dr.CHR. REINSCH, Prof. Dr. H.J. KROLL, Dr. S. WALCHER, Dipl. Math. M. BINDER, Dipl. Math. H. GRADL, Dipl. Math. R. NIEMCZYK, Dipl. Math. ST. SAUTTER und Dipl. Math. A. HUNDEMER, sie haben die Teile des Manuskripts gelesen, zahlreiche Druckfehler entdeckt und wertvolle Verbesserungsvorschläge beigetragen.

Die Druckqualität sollte zur guten Verständlichkeit bestmöglich, der Preis studentenfreundlich sein, daher wurden die Druckvorlagen mit der hochauflösenden TEX-Monotype-Variante der H. STUERTZ AG erzeugt. Daß sich dieser Entschluß trotz der anfangs zusätzlichen Pionierarbeit doch gelohnt hat, ist vor allem das Verdienst von Frau cand.math. I.ABOLD; sie hat den TEX-Quelltext mit Präzision, Geschmack und viel Einfallsreichtum erstellt und dabei nie ihre liebenswürdige Geduld verloren. Ihr gilt unser besonderer Dank.

Ein Teil der Abbildungen konnte von cand.ing. R. MATTUSCHAT auf einem 3D-CAD-Rechensytem am Lehrstuhl für Konstruktion im Maschinenbau erstellt werden. Wir danken Prof. Dr. K. EHRLENSPIEL für das freundliche Entgegenkommen. Ebenso dankend erwähnen wir die Studentinnen und Studenten T. ERIS, K. MATTUSCHAT und Frau cand.inf. A. SCHRAMM, die zusammen mit CHR. VACHENAUER die Skizzen für die übrigen Graphiken hingebungs- und kunstvoll auf den Bildschirm des ATARI-ST umsetzten.

Schließlich gilt unser Dank auch dem Springer-Verlag für die stets vorbildliche Zusammenarbeit, speziell Herrn Dr. J. HEINZE, der die verschiedenen Entstehungsphasen dieses Buches mit lebhaft förderndem Interesse, Geduld und fachmännischem Rat verfolgt hat.

München, im September 1989

Kurt Meyberg Peter Vachenauer

---

## Inhaltsverzeichnis

## Kapitel 1. Zahlen und Vektoren.... 1

## §1. Mengen und Abbildungen.... 1

1.1 Mengen - 1.2 Mengenoperationen - 1.3 Abbildungen

## §2. Die reellen Zahlen.... 3

2.1 Bezeichnungen – 2.2 Ungleichungen – 2.3 Intervalle – 2.4 Schranken – 2.5 Der Betrag – 2.6 Die vollständige Induktion – 2.7 Binomialkoeffizienten und die binomische Formel – Aufgaben

## §3. Die Ebene.... 11

3.1 Kartesische Koordinatensysteme - 3.2 Winkel - 3.3 Sinus, Cosinus - 3.4 Drehungen

## §4. Vektoren 17

4.1 Kartesische Koordinatensysteme im Raum – 4.2 Vektoren – 4.3 Die Addition von Vektoren – 4.4 Die skalaren Vielfachen eines Vektors – 4.5 Der Betrag – 4.6 Vektoren im Koordinatensystem

## §5. Produkte 22

5.1 Der Winkel zwischen zwei Vektoren - 5.2 Das Skalarprodukt - 5.3 Das Vektorprodukt - 5.4 Das Spatprodukt - Aufgaben

## §6. Geraden und Ebenen 34

6.1 Parameterdarstellungen einer Geraden – 6.2 Die Koordinatengleichungen einer Geraden – 6.3 Die Momentengleichung der Geraden – 6.4 Abstand Punkt-Gerade – 6.5 Abstand Gerade-Gerade – 6.6 Parameterdarstellungen einer Ebene – 6.7 Parameterfreie Darstellungen einer Ebene – 6.8 Die Gerade als Schnitt zweier Ebenen – 6.9 Die Winkel zwischen zwei Ebenen und zwischen einer Ebene und einer Geraden – Aufgaben

## §7. Gebundene Vektoren 47

7.1 Gebundene Vektoren - 7.2 Ein System gebundener Vektoren - 7.3 Die Reduktion eines Systems gebundener Vektoren - Aufgaben

## §8. Die komplexen Zahlen.... 53

8.1 Die Menge der komplexen Zahlen - 8.2 Die vier Grundrechenarten in $\mathbb{C}$ - 8.3 Die Konjugation und der Betrag komplexer Zahlen - 8.4 Anwendungen

---

VIII

Inhaltsverzeichnis

## Kapitel 2. Funktionen, Grenzwerte, Stetigkeit 58

## §1. Funktionen (Grundbegriffe) 58

1.1 Funktionen - 1.2 Monotonie - 1.3 Das Rechnen mit Funktionen

## §2. Polynome und rationale Funktionen 61

2.1 Polynome - 2.2 Polynomnullstellen - Faktorisierung - 2.3 Polynominterpolation - 2.4 Der Graph - 2.5 Rationale Funktionen, Polynomdivision - 2.6 Der Definitionsbereich D - 2.7 Ergänzung: Polynome über $\mathbb{C}$ - Aufgaben

## §3. Die Kreisfunktionen 75

3.1 Definition und einfache Eigenschaften – 3.2 Die Tangens- und Cotangensfunktion – 3.3 Die Polardarstellung komplexer Zahlen – 3.4 Anwendungen der De Moivre-Formeln – 3.5 Harmonische Schwingungen – Aufgaben

## §4. Zahlenfolgen und Grenzwerte 88

4.1 Folgen - 4.2 Definition des Grenzwerts; konvergente Zahlenfolgen

## §5. Rechenregeln für Grenzwerte und Konvergenzkriterien ..... 93

5.1 Rechenregeln – 5.2 Grenzwertbestimmung durch Abschätzung – 5.3 Monotone Folgen – 5.4 Die Exponentialfunktion – 5.5 Für Fortgeschrittene: Das Cauchy-Konvergenzkriterium – Aufgaben

## §6. Funktionengrenzwerte, Stetigkeit.... 103

6.1 Definitionen - 6.2 Die 6 elementaren Methoden der Grenzwertbestimmung - 6.3 Asymptoten - 6.4 Stetigkeit - Aufgaben

## Kapitel 3. Differentiation.... 112

## §1. Die Ableitung einer differenzierbaren Funktion 112

1.1 Die Definition der Ableitung – 1.2 Die geometrische Deutung der Ableitung: Tangentenanstieg – 1.3 Die analytische Deutung der Ableitung: Lineare Approximation – 1.4 Die physikalische Deutung der Ableitung: Geschwindigkeit – 1.5 Stetigkeit ist notwendig für Differenzierbarkeit – 1.6 Differentiationsregeln – 1.7 Die Differentiation der Polynome und der rationalen Funktionen – 1.8 Die Ableitung der Kreisfunktionen – 1.9 Die Kettenregel – 1.10 Höhere Ableitungen – Aufgaben

## §2. Anwendungen der Differentiation.... 121

2.1 Maxima und Minima einer Funktion – 2.2 Der Mittelwertsatz – 2.3 Wendepunkte – 2.4 Die Regeln von De L'Hospital – 2.5 Kurvendiskussion – 2.6 Nullstellen und Fixpunkte – 2.7 Kubische Splines – Aufgaben

---

Inhaltsverzeichnis

IX

§3. Umkehrfunktionen.... 139

3.1 Grundlagen - 3.2 $n$-te Wurzel, rationale Exponenten - 3.3 Arcussinus, Arcuscosinus, Arcustangens - Aufgaben

§4. Die Exponential- und Logarithmusfunktion ...... 147

4.1 Die $e$-Funktion - 4.2 Die Kurve $y = e^{x} - 4.3$ Exponentiell wachsende bzw. fallende Prozesse - 4.4 Der natürliche Logarithmus - 4.5 Allgemeine Exponentialfunktionen und Logarithmen - 4.6 Die Hyperbelfunktionen sinh, cosh, tanh - Aufgaben

Kapitel 4. Integration.... 161

§1. Das bestimmte Integral.... 161

1.1 Die Definition des bestimmten Integrals - 1.2 Die geometrische Deutung - 1.3 Elementare Integrationsregeln und der Mittelwertsatz - 1.4 Differentiation und Integration - Aufgaben

§2. Integrationsregeln.... 169

2.1 Linearität – 2.2 Partielle Integration – 2.3 Die Substitutionsmethode – 2.4 Symmetrien beachten – 2.5 Ausblicke – Aufgaben

§3. Die Integration der rationalen Funktionen.... 179

3.1 Die Partialbruchzerlegung - 3.2 Die Integration - 3.3 Die Integration von $R(e^x) - 3.4$ Die Integration von $R\left(x, \sqrt[k]{\frac{ax + b}{cx + e}}\right)$, $ae - bc \neq 0 - 3.5$ Die Integration von $R(\sin x, \cos x) - 3.6$ Trigonometrische und hyperbolische Substitutionen - Aufgaben

§4. Uneigentliche Integrale 185

4.1 Die Definition der uneigentlichen Integrale – 4.2 Ein Konvergenz-Test – 4.3 Ein an beiden Grenzen uneigentliches Integral – 4.4 Ausnahmestellen im Innern des Integrationsintervalls – Aufgaben

§5. Kurven, Längen- und Flächenmessung.... 190

5.1 Die Parameterdarstellung – 5.2 Tangente und Normale – 5.3 Kurvenlänge – 5.4 Krümmung und Krümmungskreis – 5.5 Die Polardarstellung einer ebenen Kurve – 5.6 Flächeninhalte – Aufgaben

§6. Weitere Anwendungen des Integrals.... 204

6.1 Abkürzende Redeweisen – 6.2 Das Volumen eines Rotationskörpers – 6.3 Die Mantelfläche – Aufgaben

§7. Numerische Integration.... 206

Aufgaben

---

X

Inhaltsverzeichnis

## Kapitel 5. Potenzreihen 212

## §1. Unendliche Reihen.... 212

1.1 Grundbegriffe - 1.2 Absolute Konvergenz - Aufgaben

## §2. Reihen von Funktionen.... 221

2.1 Gleichmäßige Konvergenz – 2.2 Gleichmäßig konvergente Funktionenreihen – Aufgaben

## §3. Potenzreihen.... 226

3.1 Der Konvergenzradius - 3.2 Berechnung des Konvergenzradius -
3.3 Die Differentiation und Integration von Potenzreihen - 3.4 Die Potenzreihendarstellung einiger Funktionen - 3.5 Die Binomialreihe -
3.6 Potenzreihen mit dem Zentrum  $a \neq 0 - 3.7$  Koeffizientenvergleich – Aufgaben

## §4. Der Satz von Taylor; Taylor-Reihen.... 237

4.1 Die Taylor-Formel - 4.2 Die Taylor-Reihe - 4.3 Methoden der Reihenentwicklung - Aufgaben

## §5. Anwendungen (an Beispielen) 244

5.1 Grenzwertberechnungen – 5.2 Näherungsformeln (Approximation) – 5.3 Die Reihendarstellung und Berechnung einer Integralfunktion mit nicht elementar integrierbarem Integranden – 5.4 Potenzreihenansatz zur Lösung einfacher Differentialgleichungen – Aufgaben

## Kapitel 6. Lineare Algebra.... 250

## §1. Lineare Gleichungssysteme und Matrizen.... 250

1.1 Was ist eine Matrix? – 1.2 Addition, Subtraktion und Multiplikation mit einem Zahlenfaktor – 1.3 Lineare Gleichungssysteme und Matrizen – 1.4 Das Gaußsche Lösungsverfahren – Aufgaben

## §2. Die Matrizenmultiplikation 265

2.1 „Zeile mal Spalte“ – 2.2 Die Multiplikation zweier Matrizen –
2.3 Rechenregeln – 2.4 Die Transponierte einer Matrix – 2.5 Invertierbare Matrizen – 2.6 Diagonal- und Dreiecksmatrizen – Aufgaben

## §3. Vektorräume.... 274

3.1 Der „abstrakte“ Vektorraum – 3.2 Unterräume, Linearkombinationen, lineare Hülle – 3.3 Basis und Dimension – Aufgaben

## §4. Elementarmatrizen und elementare Umformungen.... 286

4.1 Zeilenraum und Spaltenraum - 4.2 Elementarmatrizen - 4.3 Der Rang und die $P-Q$-Normalform - 4.4 Rechenverfahren - Aufgaben

---

Inhaltsverzeichnis

XI

§5. Determinanten 299

5.1 Einführung – 5.2 Definition der Determinante einer $n \times n$-Matrix – 5.3 Rechenregeln für Determinanten – 5.4 Die Entwicklung von det $A$ nach einer beliebigen Zeile oder Spalte – 5.5 Beispiele – 5.6 Anwendungen – Aufgaben

§6. Lineare Abbildungen und Eigenwerte 311

6.1 Lineare Abbildungen - 6.2 $V = W = \mathbb{R}^n$ - 6.3 Längen und Winkel im $\mathbb{R}^n$; Orthogonalität - 6.4 Speziell: Spiegelungen und Drehungen - 6.5 Das Schmidtsche Orthonormierungsverfahren - 6.6 Basiswechsel, Koordinatentransformation - 6.7 Eigenwerte, Eigenvektoren - 6.8 Die orthogonale Gruppe - Aufgaben

§7. Symmetrische Matrizen und quadratische Formen .... 339

7.1 Quadratische Formen - 7.2 Die Hauptachsentransformation - 7.3 Quadriken - 7.4 Die nichtorthogonale Diagonalisierung einer symmetrischen Matrix - 7.5 Positiv definite Matrizen - Aufgaben

Kapitel 7. Funktionen in mehreren Variablen: Differentiation..... 359

§1. Kurven im $\mathbb{R}^n$ ...... 360

1.1 Parameterdarstellungen – 1.2 Das begleitende Dreibein, Krümmung, Torsion – 1.3 Ergänzung: Der natürliche Parameter und die Frenetschen Formeln – Aufgaben

§2. Reellwertige Funktionen mehrerer reeller Veränderlicher .... 370

2.1 Grundlagen – 2.2 Grenzwerte und Stetigkeit – 2.3 Partielle Ableitungen, der Gradient – 2.4 Die totale Ableitung und lineare Approximation – 2.5 Einfache Anwendungen – 2.6 Die Richtungsableitung, der Anstieg und die Kettenregel – Aufgaben

§3. Anwendungen der Differentiation.... 391

3.1 Die Bedeutung des Gradienten – 3.2 Approximation höherer Ordnung; die Taylor-Formel – 3.3 Implizite Funktionen – 3.4 Lokale Minima und Maxima – 3.5 Ausgleichsrechnung – 3.6 Extremwertaufgaben mit Nebenbedingungen – Aufgaben

§4. Vektorwertige Funktionen 418

4.1 Die Differentiation – 4.2 Die Kettenregel – 4.3 Räumliche Skalaren- und Vektorfelder – 4.4 Gradient, Divergenz, Rotation, Laplace-Operator – Aufgaben

---

XII

Verzeichnis der Programme

## Kapitel 8. Funktionen in mehreren Variablen: Integration ..... 430

## §1. Parameterintegrale 430

1.1 Parameterintegrale - Aufgaben

## §2. Kurvenintegrale 435

2.1 Das Kurvenintegral einer skalaren Funktion - 2.2 Anwendungen - 2.3 Die Integration eines Vektorfeldes längs einer Kurve - 2.4 Anwendungen und Beispiele - 2.5 Das Potential eines Gradientenfeldes - 2.6 Die praktische Bestimmung eines Potentials ($n = 3$) - Aufgaben

## §3. Die Integration über ebene Bereiche.... 454

3.1 Der Flächeninhalt – 3.2 Definition und einfache Eigenschaften des Doppelintegrals – 3.3 Die Berechnung des Doppelintegrals in kartesischen Koordinaten – 3.4 Weitere Anwendungen und Beispiele – 3.5 Der Satz von Green – Aufgaben

## §4. Die Integration über Flächen im Raum 467

4.1 Parameterdarstellungen – 4.2 Beispiele – 4.3 Der Flächeninhalt – 4.4 Das Oberflächenintegral einer skalaren Funktion – 4.5 Die Transformationsformel für Gebietsintegrale – 4.6 Das Oberflächenintegral eines Vektorfeldes – 4.7 Der Satz von Stokes – Aufgaben

## §5. Die Integration über dreidimensionale Bereiche.... 488

5.1 Definition und einfache Eigenschaften des Dreifachintegrals – 5.2 Einfache Anwendungsbeispiele – 5.3 Die Transformationsformel für Volumenintegrale – 5.4 Der Divergenzsatz – 5.5 Einige Anwendungen der Integralsätze – 5.6 Orthogonale krummlinige Koordinaten – Aufgaben

## Literaturverzeichnis.... 505

## Anhang: Pascal-Programme 507

## Namen- und Sachverzeichnis 517

## Verzeichnis der Programme

1. Programm HORNER.... 63

Auswertung eines Polynoms mit dem Horner-Schema

2. Programm HORNER vollstaendig.... 63

Entwicklung eines Polynoms nach Potenzen von x - b

---

Verzeichnis der Programme

XIII

3. Programm NEWTON Interpolation.... 68
Berechnung und Auswertung des Newton Interpolationspolynoms
4. Programm BISECTION.... 109
Nullstellenbestimmung (f(x) = 0, x ∈ ℝ)
5. Programm NEWTON Verfahren.... 134
Nullstellenbestimmung (f(x) = 0, x ∈ ℝ)
6. Programm KUBISCHE SPLINE.... 136
Interpolation mit kubischer Spline-Funktion
7. Programm ROMBERG Integration.... 209
Berechnung von $\int_{a}^{b} f(x) dx$ mittels Romberg-Extrapolation
8. Programm Vollst. Ellipt. Integrale.... 211
Berechnung der vollständigen elliptischen Integrale $E(k)$ und $K(k)$ mit arithmetisch-geometrischem Mittel
9. Programm GAUSS.... 296
Lösung des linearen Gleichungssystems Ax = b mit verbesserter LR-Zerlegung, Berechnung der Determinante von A
10. Programm LEVERRIER.... 333
Berechnung der Koeffizienten des Polynoms $p(\lambda) = \det(\lambda E - A)$
11. Programm JACOBI.... 354
Berechnung aller Eigenwerte und Eigenvektoren einer symmetrischen Matrix
12. Programm BAIRSTOW.... 384
Berechnung aller komplexen Nullstellen eines reellen Polynoms
13. Procedure LINFIT.... 406
Bestimmung der Ausgleichslösung eines überbestimmten linearen Gleichungssystems
14. Programm NLSQ.... 407
Bestimmung der Ausgleichslösung eines überbestimmten nichtlinearen Gleichungssystems

---

## Inhalt von Band 2

## Kapitel 9. Gewöhnliche Differentialgleichungen

§1. Einführung
§2. Spezielle Differentialgleichungen 1. Ordnung
§3. Spezielle Differentialgleichungen 2. Ordnung
§4. Existenzsätze
§5. Numerische Lösung des Anfangswertproblems 1. Ordnung
§6. Die Laplace-Transformation
§7. Lösung mittels Potenzreihenansatz
§8. DGL-Systeme und DGLn höherer Ordnung
§9. Lineare DGL-Systeme mit konstanten Koeffizienten
§10. Stabilität, periodische Lösungen
§11. Rand- und Eigenwertprobleme

## Kapitel 10. Funktionentheorie

§1. Punktmengen in der komplexen Ebene
§2. Einige elementare Funktionen
§3. Gebrochen-lineare Funktionen
§4. Potenzreihen
§5. Differentiation, analytische Funktionen
§6. Integration
§7. Anwendungen der Cauchy-Integralformel
§8. Harmonische Funktionen und das Dirichlet-Problem
§9. Laurent-Reihen und Singularitäten
§10. Residuentheorie

## Kapitel 11. Fourier-Analysis

§1. Trigonometrische Polynome und Reihen
§2. Fourier-Reihen
§3. Konvergenz der Fourier-Reihe
§4. Anwendungen (an Beispielen)
§5. Diskrete Fourier-Analysis
§6. Die Fourier-Transformation

## Kapitel 12. Partielle Differentialgleichungen

§1. Einführung
§2. Partielle Differentialgleichungen 1. Ordnung
§3. Lineare und quasilineare PDGn 2. Ordnung
§4. Trennung der Variablen
§5. Lösungen mit Laplace- und Fourier-Transformation
§6. Lösungen mit Green-Funktion

---

Inhalt von Band 2

XV

## Kapitel 13. Variationsrechnung

§1. Funktionale und Variation
§2. Die Euler-Differentialgleichung für $I(y) = \int_{a}^{b} F(x, y, y') dx$
§3. Natürliche Randbedingungen, Transversalitätsbedingung
§4. Variationsaufgaben mit allgemeineren Funktionalen
§5. Variation mit Nebenbedingungen
§6. Variationsrechnung mit Funktionen in mehreren Variablen
§7. Das Wechselspiel Variationsaufgaben – Differentialgleichungen
§8. Direkte Methoden

---

# Bezeichnungen

## 1. Die griechischen Buchstaben.

| Alpha | $\alpha$ | A | Eta | $\eta$ | H | Ny | $\nu$ | N | Tau | $\tau$ | T |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Beta | $\beta$ | B | Theta | $\vartheta$ | $\Theta$ | Xi | $\xi$ | $\Xi$ | Ypsilon | $\upsilon$ | $\Upsilon$ |
| Gamma | $\gamma$ | $\Gamma$ | Iota | $\iota$ | I | Omikron | o | O | Phi | $\varphi$ | $\Phi$ |
| Delta | $\delta$ | $\Delta$ | Kappa | $\kappa$ | K | Pi | $\pi$ | $\Pi$ | Chi | $\chi$ | X |
| Epsilon | $\varepsilon$ | E | Lambda | $\lambda$ | $\Lambda$ | Rho | $\rho$ | P | Psi | $\psi$ | $\Psi$ |
| Zeta | $\zeta$ | Z | My | $\mu$ | M | Sigma | $\sigma$ | $\Sigma$ | Omega | $\omega$ | $\Omega$ |

## 2. Wichtige Mengen.

| $\mathbb{N} = \{1,2,3,4,\ldots\}$ | Menge der natürlichen Zahlen ($\rightarrow$ S. 3), |
| --- | --- |
| $\mathbb{N}_0 = \mathbb{N} \cup \{0\}$, |  |
| $\mathbb{Z} = \{0,1,-1,2,-2,\ldots\}$ | Menge der ganzen Zahlen ($\rightarrow$ S. 3), |
| $\mathbb{Q} = \{ \frac{m}{n} ; m, n \in \mathbb{Z}, n \neq 0\}$ | Menge der rationalen Zahlen ($\rightarrow$ S. 3), |
| $\mathbb{R}$ | Menge der reellen Zahlen ($\rightarrow$ S. 3), |
| $\mathbb{R}^n$ | Menge der reellen Spaltenvektoren mit $n$Komponenten ($\rightarrow$ S. 251), |
| $\mathbb{R}_n$ | Menge der reellen Zeilenvektoren mit $n$Komponenten ($\rightarrow$ S. 251), |
| $\mathbb{R}^{m \times n}$ | Menge der reellen Matrizen mit $m$ Zeilenund $n$ Spalten ($\rightarrow$ S. 251), |
| $\mathbb{C} = \{ x + iy ; x, y \in \mathbb{R} \}$ | Menge der komplexen Zahlen ($\rightarrow$ S. 53), |
| $\mathbb{P}_n$ | Menge der reellen Polynome vom Grad $\leq n$($\rightarrow$ S. 276), |
| $\mathscr{C}^0(D, \mathbb{R})$ | Menge der auf $D \subseteq \mathbb{R}^n$ stetigen reellenFunktionen ($\rightarrow$ S. 377), |
| $\mathscr{C}^k(D, \mathbb{R})$ | Menge der auf $D \subseteq \mathbb{R}^n$ $k$-mal stetig partielldifferenzierbaren reellen Funktionen ($\rightarrow$ S. 377). |
