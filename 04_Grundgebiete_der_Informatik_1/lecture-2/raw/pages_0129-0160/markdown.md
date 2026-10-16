## Schleifen in C++ mit Iteratoren

C++

```cpp
#include <iostream>
#include <algorithm>
#include <vector>
#include <string>
using namespace std;

void show(vector<int> c, string str) {cout<<str<<": "; for(auto e: c) cout<<e<<' ';cout<<endl<<endl;}

int main( void )
{
    vector<int> v = {1, 2, 2, 5, 6, 7};
    show(v,"Ausgangslage");

    // 1. Loop: using a copy of the value
    for(auto elm : v) { elm++; }
    show(v,"1. Loop");
    // 2. Loop: using the reference
    for(auto& elm : v) { elm++; }
    show(v,"2. Loop");
    // 3. Loop: using the reference and const
    // for(const auto& elm : v) { elm++; }
    // -> error: increment of read-only reference 'elm'
    // 4. Loop: using for_each
    for_each(v.begin(), v.end(), [](int elm) { elm++; });
    show(v,"4. Loop");
    // 5. Loop: using classic for-loop and an iterator of a container
    for(auto it = v.begin(); it != v.end(); ++it) { (*it)++; };
    show(v,"5. Loop");
    return 0;
}
```

**129**

© T. Gemmeke, IDS, RWTH

A variable can also hold a set (i.e., a collection of objects) - we call such variable a container. In the simplest form this can be a vector or an array, that is a linear arrangement of the objects in memory. We will learn more about other data structures in the later chapters.

The $\mathbf { 1 ^ { s t } }$ for-loop iterates through all elements of the container. The current element is copied into elm. This is basically a for-each operation.

In the $2 ^ { \mathbf { n d } }$ example, elm contains a copy-by-reference of the element in the container, i.e., the int values in the vector cannot be modified. It uses a copy by reference, which is good practice especially for large objects such that no temporary copy has to be created. In principle, elements of a vector could now be modified.

The additional type specifier const prevents this again in the $\mathbf { 3 ^ { r d } }$ loop.

The $4 ^ { \mathbf { f h } }$ loop uses an explicit for\_each expression.

Finally, the $\mathbf { 5 ^ { t h } }$ loop uses a classic for construct, but with an iterator variable. An alternative would be using the index:

## Mehrdimensionale Arrays

| Stunde | Mo | Di | Mi | Do | Fr |
| --- | --- | --- | --- | --- | --- |
| 1 | Mathe | Politik | Bio | Mathe | Politik |
| 2 | Mathe | Kunst | Deutsch | Mathe | Kunst |
| 3 | Deutsch | Informatik | Sport | Deutsch | Informatik |
| 4 | Englisch | Informatik | Sport | Englisch | Informatik |
| 5 | Sport | Mathe | Physik | Sport | Mathe |
| 6 | Sport | Mathe | Physik | Sport | Mathe |

• Beispiel: Stundenplan
• 2‐dimensionales Array (**Matrix**) als Datenstruktur
Elemente vom Typ String
• Indizes:
– Stunden (int)
– Wochentage Mo‐Fr (?)
– enum tag\_typ {Mo, Di, Mi, Do, Fr}
– **Aufzählungstyp**: deklariert Mo, ..., Fr als symbolische Konstanten
– **Intern**: Mo = 0, Di = 1, ..., Fr = 4

**130**

© T. Gemmeke, IDS, RWTH; R. Leupers, SSS

Arrays sind in C die direkte Entsprechung von mathematischen Vektoren. Häufig sind auch matrixartige Strukturen zu programmieren. Hierfür können Arrays beliebig viele **Dimensionen** bekommen (d.h. 2 für Matrizen).

Im Beispiel wird ein **Aufzählungstyp** (enum) zur Matrix-Indizierung eingesetzt. Dies sind benutzerdefinierte Typen, die in erster Linie der besseren Programmlesbarkeit und –wartbarkeit dienen. Ein „enum“ ersetzt int-Konstanten durch lesbare Symbole (hier: Wochentage). Der Compiler (nicht der Präprozessor wie bei #define) ersetzt die Symbole dann durch die konkreten Konstanten. Standardmäßig beginnt die Nummerierung der enum-Konstanten bei 0, der Programmierer kann jedoch bei Bedarf auch manuell andere Werte festlegen.

Mehrdimensionale Arrays

```c
#define STUNDEN 6
#define TAGE 5
#define MA "Mathe"
#define DE "Deutsch"
#define SP "Sport"
/* ... */
enum tag_typ {Mo, Di, Mi, Do, Fr};
int main (void)
{
    char* plan[STUNDEN][TAGE];
    int tag, stunde;
    /* ... */

/* ... */
plan[0][Mo] = MA;
/* ... */
plan[5][Mo] = SP;
/* ... */
plan[5][Fr] = MA;

printf("Stundenplanabfrage:\n");
scanf("%d",&tag);
scanf("%d",&stunde);

if ((tag > Fr) || (stunde > STUNDEN))
    printf("Ungültig");
else
    printf("Fach = %s", plan[stunde-1][tag];
return 0;
}
```

| Stunde | Mo | Di | Mi | Do | Fr |
| --- | --- | --- | --- | --- | --- |
| 1 | Mathe | Politik | Bio | Mathe | Politik |
| 2 | Mathe | Kunst | Deutsch | Mathe | Kunst |
| 3 | Deutsch | Informatik | Sport | Deutsch | Informatik |
| 4 | Englisch | Informatik | Sport | Englisch | Informatik |
| 5 | Sport | Mathe | Physik | Sport | Mathe |
| 6 | Sport | Mathe | Physik | Sport | Mathe |

| Stundenplanabfrage: |
| --- |
| > 2 |
| > 4 |
| Fach = Sport |

**131**

© T. Gemmeke, IDS, RWTH; R. Leupers, SSS

Unten rechts ist eine **Beispiel-Ein/Ausgabe** gezeigt. Tag 2 bezeichnet „Mi“(siehe enum-Deklaration), so dass für Stunde 3 wie zu erwarten „Sport“ausgegeben wird. Man beachte, dass intern „stunde-1“ zur Indizierung verwendet wird, da (s.o.) die Indizierung immer bei 0 beginnt. Andererseits wäre es für den Stundenplanbenutzer unkomfortabel 0-5 statt 1-6 für die Indizierung zu verwenden.

## Beispiel: Matrixmultiplikation

ሺ𝑁 ൈ 𝑁ሻ‐Matrizen:
• **Produkt** ergibt sich aus:

$$
A = (a _ {i j}), B = (b _ {i j})
$$

$$
c _ {i j} = \sum_ {k = 1} ^ {N} a _ {i k} \cdot b _ {k j}
$$

• **Geschachtelte** Schleifen

– Iteration über Zeilen 𝑖 ൌ 1 … 𝑁
– Für jedes 𝑖: Iteration über Spalten 𝑗 ൌ 1 … 𝑁
– Für jedes ሺ𝑖,𝑗ሻ: Bilde Skalarprodukt von 𝐴‐Zeile 𝑖 und 𝐵‐Spalte 𝑗

C/C++ gestattet eine beliebige Anzahl von **Dimensionen** für Arrays
Elemente liegen stets benachbart im Speicher

![](images/page_131_image_14.jpg)

```txt
typedef int matrix[N][N];
matrix a, b, c;
for (i=0; i<N; i++)
    for (j=0; j<N; j++) {
        c[i][j] = 0;
        for (k=0; k<N; k++)
            c[i][j] += a[i][k]*b[k][j];
    }
```

**132**

© T. Gemmeke, IDS, RWTH; R. Leupers, SSS

Für die (NxN)-Matrizen wird ein neuer Typ **matrix** mit N Zeilen und N Spalten definiert. Die einzelnen Elemente sind vom Typ int. Die Variablen A, B und C werden vom Typ matrix deklariert. Bei der Berechnung des Matrixprodukts laufen die Indizes in jeder Dimension wieder von 0 bis N-1.

Werden weitere Dimensionen benötigt, so müssen in der Deklaration mehrere eckige Klammern angegeben werden. Beim Zugriff auf die Elemente werden dann auch mehrere Indizes benötigt.

## 5. Datentypen

5.1 Arrays
**5.2 Strukturen**
5.3 Abstrakte Datentypen
5.4 Klassen

**133**

© T. Gemmeke, IDS, RWTH; R. Leupers, SSS

## Strukturen

• **Struktur** (oder: struct, record): Zusammenfassung einer Gruppe von Variablen zu einer **Einheit**
**Unterschied** zum Array: Adressierung innerhalb einer Struktur per Namen, nicht per Index
Bsp. (s.o.): geometrischer Punkt struct point { float x, y; };
Allgemeine Form einer struct‐Deklaration: – struct ID { Variablendeklaration\* } – Beliebige Variablendeklarationen (auch structs) – ID heißt structure tag
• struct‐Deklaration oft in Verbindung mit typedef: struct point { float x, y; } p1,p2; oder typedef struct point { float x, y; } Point; Point p1, p2;

**134**

© T. Gemmeke, IDS, RWTH; R. Leupers, SSS

Bei **Strukturen** handelt es sich um eine Zusammenfassung mehrerer Datentypen zu einem größeren. Im Gegensatz zu Arrays können in Strukturen unterschiedliche Datentypen zusammengestellt und gespeichert werden.

Beispiel:

```javascript
/* Definition der Struktur ,person' */
struct person
{
    int id;
    char vorname[20], nachname[20];
    char telnr[15];
    int alter;
};
```

Um eine Variable H des Typs struct person anzulegen, geben Sie einfach an struct person H;

Zum Zugriff auf eine Komponente der Struktur gibt man den Namen der Struktur-Variablen an (im folgenden Beispiel also H), einen Punkt und danach den Bezeichner der Komponente:

H.alter = 32;

Operationen auf Strukturen

<div class="docvortex-algorithm" style="white-space: pre-wrap; font-family:monospace;">
typedef struct person
    { char name[100], vorname[100];
        struct datum { int tag,monat,jahr; } gebdatum;
    } Person;
Person p1, p2, *p_ptr;
• Kopieren:
    p1 = p2;  /* kopiert alle Komponenten auf einmal */
• Adressberechnung:
    p_ptr = &amp;p1;
• Komponentenzugriff direkt (Operator „.“):
    p2.gebdatum.jahr = 1950;
• Komponentenzugriff per Zeiger (Operator „-&gt;“):
    p_ptr-&gt;gebdatum.monat = 12;
    // "p-&gt;" entspricht "(*p)."
</div>

**135**

© T. Gemmeke, IDS, RWTH; R. Leupers, SSS

Der eventuell etwas lästige Gebrauch von struct kann schon bei der Definition der Struktur vermieden werden. Der Definition ist ein **typedef** voranzustellen. Der Definition folgt dann ein gültiger (und auch eindeutiger) C-Name, in diesem Beispiel „Person“.

Der Zugriff auf Komponenten von „Person“ über eine Zeigervariable p\_ptr, der die Adresse der Strukturvariablen p1 zugewiesen wird, kann über den **Pfeil-Operator** (->) oder über den **Dereferenzierungs-Operator** (\*) geschehen:

<div class="docvortex-algorithm" style="white-space: pre-wrap; font-family:monospace;">
p_ptr-&gt;gebdatum.tag = 30;
    ist identisch zu
(*p_ptr).gebdatum.tag = 30;
</div>

## Array von structs

Mit Arrays und structs lassen sich beliebige **komplexe Datenstrukturen** aufbauen
Bsp.: **Bundesliga‐Tabelle**
• **Übung**: Neuberechnung nach Spieltag‐Ergebniseingabe

<table><tr><td colspan="2"></td><td>SP</td><td>S</td><td>U</td><td>N</td><td>T</td><td>DIFF</td><td>PKT</td></tr><tr><td>1</td><td>Bayern München</td><td>3</td><td>3</td><td>0</td><td>0</td><td>10:0</td><td>10</td><td>9</td></tr><tr><td>2</td><td>Arminia Bielefeld</td><td>3</td><td>2</td><td>1</td><td>0</td><td>7:3</td><td>4</td><td>7</td></tr><tr><td>3</td><td>VfL Bochum</td><td>3</td><td>2</td><td>1</td><td>0</td><td>6:4</td><td>2</td><td>7</td></tr><tr><td>4</td><td>Eintracht Frankfurt</td><td>3</td><td>2</td><td>1</td><td>0</td><td>4:2</td><td>2</td><td>7</td></tr><tr><td>5</td><td>Hamburger SV</td><td>3</td><td>2</td><td>0</td><td>1</td><td>3:2</td><td>1</td><td>6</td></tr><tr><td>6</td><td>FC Schalke 04</td><td>3</td><td>1</td><td>2</td><td>0</td><td>7:4</td><td>3</td><td>5</td></tr><tr><td>7</td><td>Bayer Leverkusen</td><td>3</td><td>1</td><td>1</td><td>1</td><td>3:1</td><td>2</td><td>4</td></tr><tr><td>8</td><td>VfL Wolfsburg</td><td>3</td><td>1</td><td>1</td><td>1</td><td>5:5</td><td>0</td><td>4</td></tr><tr><td>9</td><td>VfB Stuttgart</td><td>3</td><td>1</td><td>1</td><td>1</td><td>4:5</td><td>-1</td><td>4</td></tr><tr><td>10</td><td>Werder Bremen</td><td>3</td><td>1</td><td>1</td><td>1</td><td>3:6</td><td>-3</td><td>4</td></tr><tr><td>11</td><td>MSV Duisburg</td><td>3</td><td>1</td><td>0</td><td>2</td><td>4:5</td><td>-1</td><td>3</td></tr><tr><td>12</td><td>Hertha BSC</td><td>3</td><td>1</td><td>0</td><td>2</td><td>3:4</td><td>-1</td><td>3</td></tr><tr><td>13</td><td>Borussia Dortmund</td><td>3</td><td>1</td><td>0</td><td>2</td><td>5:7</td><td>-2</td><td>3</td></tr><tr><td>14</td><td>Karlsruher SC</td><td>3</td><td>1</td><td>0</td><td>2</td><td>3:5</td><td>-2</td><td>3</td></tr><tr><td>15</td><td>1. FC Nürnberg</td><td>3</td><td>1</td><td>0</td><td>2</td><td>2:4</td><td>-2</td><td>3</td></tr><tr><td>16</td><td>Hannover 96</td><td>3</td><td>1</td><td>0</td><td>2</td><td>2:5</td><td>-3</td><td>3</td></tr><tr><td>17</td><td>Energie Cottbus</td><td>3</td><td>0</td><td>1</td><td>2</td><td>1:5</td><td>-4</td><td>1</td></tr><tr><td>18</td><td>Hansa Rostock</td><td>3</td><td>0</td><td>0</td><td>3</td><td>1:6</td><td>-5</td><td>0</td></tr></table>

```txt
typedef struct team {
  char *name;
  int SP,S,U,N,T1,T2,DIFF,PKT;
} Team;

Team liga[18]; /* 0...17 */
/* ... */
liga[5].name = "FC Schalke 04";
liga[13].DIFF = liga[13].T1-liga[13].T2;
/* ... */
```

**136**

© T. Gemmeke, IDS, RWTH; R. Leupers, SSS

Im Beispiel wird eine Struktur „Team“ als Typ definiert. Im Anschluss erfolgt die Deklaration einer Variablen „liga“ als 18-elementiges **Array von Teams**.

Mit Hilfe des Index greift man innerhalb des Arrays auf genau ein Strukturelement vom Typ Team zu, welches dann wiederum über den Punkt-Operator den Zugriff auf einzelne Komponenten erlaubt.

## 5. Datentypen

5.1 Arrays
5.2 Strukturen
**5.3 Abstrakte Datentypen**
5.4 Klassen

**137**

© T. Gemmeke, IDS, RWTH; R. Leupers, SSS

## Abstrakte Datentypen

C++

**Def**.: Ein **abstrakter Datentyp** (**ADT**) ist ein Datentyp (eine Menge von Werten und eine Sammlung von Operationen auf diesen Werten), der nur über eine Schnittstelle zugänglich ist.

[Sedgewick, Algorithmen in C++]

• Menge set

```cpp
#include <iostream>
#include <set>
#include <algorithm> // required for set_union
using namespace std;

int main( void )
{
    set<int> s = {1, 2, 2};
    set<int> t = {7, 2, 4, 1};

    set<int> r;
    set_union(s.begin(), s.end(), t.begin(), t.end(), inserter(r, r.begin());

    // print the contents of the sets
    cout << "s: "; for(auto elm : s) cout << elm << ' '; cout << endl;
    cout << "t: "; for(auto elm : t) cout << elm << ' '; cout << endl;
    cout << "r: "; for(auto elm : r) cout << elm << ' '; cout << endl;

    return 0;
}
```

**138**

© T. Gemmeke, IDS, RWTH

set\_union is a method to create the union of two sets.

It requires the first and last element of the two sources as well as an iterator pointing to the next position for insertion.

The input sets have to occur in a sorted fashion when iterating through them.

Related operations are the **difference of sets** and their **intersection**.

The method merge combines both input sets including duplicates. To see this effect, the target container has to be a vector as duplicates get automatically removed in a set.

## 5. Datentypen

5.1 Arrays
5.2 Strukturen
5.3 Abstrakte Datentypen

## 5.4 Klassen

i (De)Konstruktor
ii Public vs. private
iii Vererbung
iv Abstrakte Klassen
v Überladen von Operatoren

**139**

© T. Gemmeke, IDS, RWTH; R. Leupers, SSS

## Abstrakte Datentypen

C++

## Klassen und Methoden

```cpp
#include <string>
#include <iostream>
using namespace std;

class Member {
    public:
        string status = "public";
};

int main( void ) {

    Member someone;

    cout << someone.status << endl;

    return 0;
}
```

**140**

© T. Gemmeke, IDS, RWTH

A class is introduced with the keyword class followed by its name. You can have various variables and methods declared. A variable or method can be referenced using the object identifier followed by a ‘.’ and the corresponding method or variable.

Please note: a class declaration is always concluded by a ‘;’ – this goes back to the concept of struct declarations that can have objects be defined at the end (after the closing curly bracket).

## 5. Datentypen

5.1 Arrays
5.2 Strukturen
5.3 Abstrakte Datentypen

**5.4 Klassen**

**i (De)Konstruktor**
ii Public vs. private
iii Vererbung
iv Abstrakte Klassen
v Überladen von Operatoren

**141**

© T. Gemmeke, IDS, RWTH; R. Leupers, SSS

## Klassen

C++

(De)Constructor

```cpp
#include <string>
#include <iostream>
using namespace std;

class Member {
    public:
        string status;
    // constructor
    Member() { status = "starter"; }
    Member( string val ) : status(val) {}
    // (de)constructor
    ~Member() { cout << "... a member left the pack." << endl; }
    void show_status( void ) {
        cout << "Membership status: " << status << endl;
    }
};
void sub( void ) {
    cout << "> Entering function 'sub'" << endl;
    Member pers("gold");
    pers.show_status();
    cout << "> About to leave 'sub'" << endl;
}
int main( void ) {
    cout << "> Starting in 'main'" << endl;
    Member someone;
    someone.show_status();
    sub();
    cout << "> About to leave 'main'" << endl;
    return 0;
}
```

**142**

© T. Gemmeke, IDS, RWTH

The class name itself acts as **constructor**, which is called when an object of that class is created. When the object is deleted, the **deconstructor** method is called, which has a preceding ‘\~’ in front of the class name.

In this example, we use polymorphism to enable variations of the created object – a default way and one that provides a specific status. Constructor and deconstructor can be omitted if nothing is to be done on creation or deletion of an object.

The shown example highlights the concept of the **scope** of objects and their automatic deletion, once they leave a scope. Leaving the function sub results in an automatic call of the deconstrutor of the object stored in pers (which is of the Member class).

## 5. Datentypen

5.1 Arrays
5.2 Strukturen
5.3 Abstrakte Datentypen

## 5.4 Klassen

i (De)Konstruktor
**ii Public vs. private**
iii Vererbung
iv Abstrakte Klassen
v Überladen von Operatoren

**143**

© T. Gemmeke, IDS, RWTH; R. Leupers, SSS

## Klassen

C++

## • Klassenelemente: public vs. private

```cpp
#include <string>
#include <iostream>
using namespace std;

class Member {
    public:
        string statusA = "public"; // public Variable
    private:
        string statusB = "secret"; // private Variable
};

int main( void ) {

    Member someone;

    cout << someone.statusA << endl;
    cout << someone.statusB << endl;

    return 0;
}
```

error: ‘std::string Member::statusB’ is private within this context

**144**

© T. Gemmeke, IDS, RWTH

The variables and methods declared that are either private or public. **Private** ones are only accessible to other elements of the class itself. In this example, we cannot directly access the variable statusB of the class Member.

## Klassen

C++

• Klassenelemente: public vs. private

```cpp
#include <string>
#include <iostream>
using namespace std;

class Member {
    private:
        string status = "unknown"; // Private Variable

    public:
        // public methods
        void show_status( void ) {
            cout << "Status: " << status << endl;
        }
        void update_status( string new_status ) {
            status = new_status;
        }
};

int main( void ) {

    Member someone;

    someone.show_status();
    someone.update_status("gold");
    someone.show_status();

    return 0;
}
```

Private Variablen werden mit sogenannten get und set Methoden verarbeitet.

**145**

© T. Gemmeke, IDS, RWTH

To access the **private** variable, we define a public method. This way the contents is protected against inadvertent manipulations.

In general, there should be related get and set methods to manipulate private objects.

## 5. Datentypen

5.1 Arrays
5.2 Strukturen
5.3 Abstrakte Datentypen

## 5.4 Klassen

i (De)Konstruktor
ii Public vs. private
**iii Vererbung**
iv Abstrakte Klassen
v Überladen von Operatoren

**146**

© T. Gemmeke, IDS, RWTH; R. Leupers, SSS

## Klassen

C++

## • Vererbung

Weiterführung des Beispiels: Die Funktion main auf der vorrangegangen Folie wird durch den Code auf dieser Folie ersetzt.

```cpp
...

class Student : public Member {
    public:
        Student() { // constructor
            Member::update_status("Student");
        }
};

int main( void ) {
    Member someone;
    Student pers;

    someone.show_status();
    pers.show_status();

    return 0;
}
```

**147**

© T. Gemmeke, IDS, RWTH

**Inheritance** is a key element of object-oriented programming. We have a base class, that we re-use in multiple sub-classes and their potential derivation thereof.

## Klassen

C++

## • Vererbung

... und noch einen Schritt ...

```cpp
...

class Prof : public Member {
    public:
        Prof() { // constructor
            Member::update_status("Professor");
        }
};

int main( void ) {
    Member someone;
    Student persA;
    Prof persB;

    someone.show_status();
    persA.show_status();
    persB.show_status();

    return 0;
}
```

**148**

© T. Gemmeke, IDS, RWTH

Apparently, multiple sub-classes can inherit from the same base class.

## Polymorphie

C++

## Dynamische Auswahl der Methode

```cpp
#include <string>
#include <iostream>
using namespace std;

class Being {
    public:
        string name;
        Being() {}
        Being( string str ) { name = str; }
        virtual void show( void ) { cout << "'" << name << "' is an unknown being." << endl << endl; }
};

class Insect : public Being {
    public:
        Insect( string str ) { name = str; }
        void show( void ) override { cout << "The '" << name << "' is an insect." << endl << endl; }
};

class Mammal : public Being {
    public:
        Mammal( string str ) { name = str; }
        void show( void ) override { cout << "The '" << name << "' is a mammal." << endl << endl; }
};

int main( void )
{
    Being* b; // pointer to the base class
    string in;

    while( 1 ) {
        cout << "Enter the type of being (i: insect, m: mammal): ";
        cin >> in;
        cout << endl;

        if( in[0] == 'i' ) b = new Insect("ant");
        else if( in[0] == 'm' ) b = new Mammal("cat");
        else b = new Being(in);

        b->show(); // method show is dynamically selected
    }
    return 0;
}
```

**149**

© T. Gemmeke, IDS, RWTH

At this point, we know the essential elements to introduce **dynamic polymorphism** - a concept where the binding of a function call with an appropriate declaration happens during run-time.

To enable this, we introduce the keyword virtual in the base class to label methods that should be considered for this. This triggers the compiler to create a table of potential methods to be used.

A typical application of this is handling objects of the base or derived class with the same code as shown in the given example:

We declare a pointer to an object of the base class. Depending on the user input, either an object of the base class or any of the two derived classes is created.

The call of show is then dynamically bound to the (sub-)class the base class of the object the pointer is pointing to, i.e., the class of the handled object determines during run-time the binding of show.

## 5. Datentypen

5.1 Arrays
5.2 Strukturen
5.3 Abstrakte Datentypen

## 5.4 Klassen

i (De)Konstruktor
ii Public vs. private
iii Vererbung
**iv Abstrakte Klassen**
v Überladen von Operatoren

**150**

© T. Gemmeke, IDS, RWTH; R. Leupers, SSS

## Abstrakte Klassen

C++

Beispiel: Schnittstellendefinition

```cpp
#include <string>
#include <iostream>
using namespace std;

class Being {
    public:
        string name;
        Being() {}
        Being( string str ) { name = str; }
        virtual void show() = 0; // Definition einer rein virtuellen Methode
};

class Insect : public Being {
    public:
        Insect( string str ) { name = str; }
        void show() { cout << "The '" << name << "' is an insect." << endl << endl; }
};

class Mammal : public Being {
    public:
        Mammal( string str ) { name = str; }
        void show() { cout << "The '" << name << "' is a mammal." << endl << endl; }
};

int main( void )
{
    Being* b: // pointer to the base class
    string in;

    while( 1 ) {
        cout << "Enter the type of being (i: insect, m: mammal): ";
        cin >> in;
        cout << endl;

    if( in[0] == 'i' ) b = new Insect("ant");
    else b = new Mammal(in);

    b->show();
}
return 0;
}
```

**151**

© T. Gemmeke, IDS, RWTH

The declaration of purely virtual methods (as shown in this example) leads to **abstract classes**.

They can be used as before, but not to generate an object.

A typical application case is the definition of **interfaces**. The specific implementation is realized in a sub class, in which all virtual methods have to be declared, otherwise the sub class remains virtual.

## 5. Datentypen

5.1 Arrays
5.2 Strukturen
5.3 Abstrakte Datentypen

## 5.4 Klassen

i (De)Konstruktor
ii Public vs. private
iii Vererbung
iv Abstrakte Klassen
**v Überladen von Operatoren**

**152**

© T. Gemmeke, IDS, RWTH; R. Leupers, SSS

## Überladen von Operatoren

C++

• 1 + 1 = …?!

```cpp
#include <iostream>
#include <vector>
using namespace std;

class myInt {
    public:
        int x;
        myInt() { x = 0; };
        myInt( int val ) : x(val){};
        myInt& operator+(const myInt& val) {
            myInt* o = new myInt(this->x + val.x + 1);
            return *o;
        }
        myInt& operator=(const myInt& rhs) {
            x = rhs.x;
            return *this;
        }
        friend ostream& operator<<(ostream& os, const myInt& val) {
            os << val.x;
            return os;
        }
};

int main( void )
{
    myInt a = 1, b = 1;

    cout << "a = " << a << "; b = " << b << " => a+b = " << a+b <-

    return 0;
}
```

**153**

Quiz: Was ist das Ergebnis von 1+1? 0, 1, 2, oder 3?

© T. Gemmeke, IDS, RWTH

## Überladen von Operatoren

C++

• Vereinigungsmenge (‚union‘) zweier Vektoren mit dem ‘+’‐Operator

```cpp
#include <iostream>
#include <vector>
#include <algorithm>
using namespace std;

vector<int>& operator+(const vector<int>& a, const vector<int>& b) {
    vector<int>* res = new vector<int>();
    res->insert(res->begin(), a.begin(), a.end());
    res->insert(res->end(), b.begin(), b.end());
    // Let's have the vector sorted
    sort(res->begin(), res->end());
    // ... and remove all duplicate.
    // Note: the vector has to be sorted for unique to work
    // Note: unique does not shrink the vector length, so we add a call to erase
    res->erase( unique( res->begin(), res->end() ), res->end() );
    return *res;
}

int main( void )
{
    vector<int> s = {1, 2, 2};
    vector<int> t = {4, 5, 6};

    vector<int> r = s+t;

    // fancy: for(const auto& elm : ...
    for(auto elm : r) cout << elm << ' ';
    cout << endl;

    return 0;
}
```

**154**

Anmerkung: der ADT set bietet diese Funktionalität ...

© T. Gemmeke, IDS, RWTH

This example overloads the ‘+’ operator to generate a union of two vectors.

Please note: the ADT set provides this functionality.

## Überladen von Operatoren

C++

## • Stream

```cpp
#include <string>
#include <iostream>
using namespace std;

class Graphic {
    public:
        string name;
        Graphic() { name = "generic object"; }
};

ostream& operator<<(ostream& os, const Graphic& gr) {
            os << gr.name;
            return os;
}

int main( void ) {

    Graphic a;

    cout << "This is a '" << a <<的目的" << endl;

    return 0;
}
```

**155**

© T. Gemmeke, IDS, RWTH

Operators can be **overloaded** – it is a way of static polymorphism.

In this example, it is used to define the representation of an object of the class graphic in a stream. In this way, we can define a class specific representation of an object when used with a standard operator.

## Überladen von Operatoren

C++

• Stream

```cpp
class Point : public Graphic {
    public:
        int x0, y0;
        Point( int a, int b ) : x0(a), y0(b) { name = "Point"; }
};
class Line : public Graphic {
    public:
        int x0, y0, x1, y1;
        Line( int a, int b, int c, int d) : x0(a), y0(b), x1(c), y1(d) { name = "Line"; }
};

ostream& operator<<(ostream& os, const Point& gr) {
            os << gr.name << " at (" << gr.x0 << ", " << gr.y0 << ")";
            return os;
}
ostream& operator<<(ostream& os, const Line& gr) {
            os << gr.name << " from (" << gr.x0 << ", " << gr.y0 << ")";
            os << " -> (" << gr.x1 << ", " << gr.y1 << ")";
            return os;
}

int main( void ) {
    Graphic a;
    Point b(1,2);
    Line c(3,4,5,6);

    cout << "This is a '" << a <<的目的 << endl;
    cout << "This is a '" << b <<的目的 << endl;
    cout << "This is a '" << c <<的目的 << endl;

    return 0;
}
```

**156**

© T. Gemmeke, IDS, RWTH

This example is meant to highlight the advantage of using streams as opposed to calls to printf. The stream expression in main is identical for all three data types.

(Please note: the code of this slide should replace the declaration of main on the previous slide.)

## Überladen von Operatoren

C++

## • Functor

Funktoren werden häufig in der Methode transform genutzt. Diese wendet den Funktor auf alle Elemente aus einem vorgegebenen Bereich an.

```cpp
#include <iostream>
using namespace std;

class Modulo {
    private:
        long mod;
    public:
        Modulo(long val) : mod(val) {}

        long operator()(long x) {
            return x%mod;
        }

        friend ostream& operator<<(ostream& os, const Modulo& x) {
            os << x.mod;
            return os;
        }
};

int main( void )
{
    Modulo m(5);
    cout << "129 mod " << m << " = " << m(129) << endl;
    cout << "127 mod " << m << " = " << m(127) << endl;

    return 0;
}
```

**157**

© T. Gemmeke, IDS, RWTH

The overload of the function call operator ‘()’ is called a **functor**.

A functor is frequently used with the method transform, which applies the functor to elements withing a specified range.

## Überladen von Operatoren

C++

• Beispiel: Functor translate

<div class="docvortex-algorithm" style="white-space: pre-wrap; font-family:monospace;">
#include &lt;iostream&gt;
#include &lt;algorithm&gt;
#include &lt;string&gt;
#include &lt;vector&gt;
using namespace std;

class translate {
    private:
        vector&lt;string&gt; ge = {"eins","zwei","drei","vier"};
        vector&lt;string&gt; en = {"one","two","three","four"};
        vector&lt;string&gt; fr = {"un","deux","trois","quatre"};
        vector&lt;string&gt;* source;
        vector&lt;string&gt;* target;
    public:
        translate(string str) { // constructor
            switch( str[0] ) {
                case 'G': source = &amp;ge; break;
                case 'E': source = &amp;en; break;
                case 'F': source = &amp;fr; break;
            }
            switch( str[2] ) {
                case 'G': target = &amp;ge; break;
                case 'E': target = &amp;en; break;
                case 'F': target = &amp;fr; break;
            }
        }
        string operator() (string word) { // overloading of function call operator ()
            string res = word;
            auto it = find(source-&gt;begin(), source-&gt;end(), word);
            size_t i = distance(source-&gt;begin(), it);
            if( i&lt;source-&gt;size() &amp;&amp; i&lt;target-&gt;size() ) res = (*target)[i];
            return res;
        }
};

int main( void ) {
    vector&lt;string&gt; number = {"vier", "eins", "zwei", "four", "trois"};
    for( auto elm : number ) cout &lt;&lt; ' ' &lt;&lt; elm; cout &lt;&lt; endl;

    transform(number.begin(), number.end(), number.begin(), translate("GeEn"));
    for( auto elm : number ) cout &lt;&lt; ' ' &lt;&lt; elm; cout &lt;&lt; endl;

    return 0;
}
</div>

**158**

© T. Gemmeke, IDS, RWTH

The method transform calls the constructor of translate in translate("GeEn"), which returns an object of this class with a specific initialization that encodes the intended translation – let’s call it temp. This temporary object is used to infer a unary function (as required by transform) that is called with the function call operator () and the current element of the vector number as parameter. Due to the overloading, we execute temp(elm), which performs the actual translation.

## 6. Analyse von Algorithmen

## 6.1 Laufzeitanalyse

6.2 𝒪‐Notation für Wachstumsordnungen
6.3 Beispiel: Exponentialfunktion
6.4 Beispiel: Suchen in Arrays

**159**

© T. Gemmeke, IDS, RWTH; R. Leupers, SSS

## Analyse von Algorithmen

Für jedes Problem gibt es **viele mögliche** Algorithmen und Implementierungen
Häufig gesucht: **effizienteste/schnellste** Implementierung
• Wie wird diese bestimmt?

```c
#define n 10

/* ... */

    int fact, count;

    fact = 1;

    for (count = 1; count <= n; count++) {
        fact *= count;
    }

    printf("factorial(%d) = %d", n, fact);
```

– Algorithmenentwicklung ist ein **kreativer** Prozess

– **Analyse** eines gegebenen Algorithmus mittels **Wachstumsordnungen**

• Bsp.: Fakultätsfunktion

Factorial: 𝑛! ൌ 1 ⋅ 2 ⋅ … ⋅ 𝑛 ൌ ∏ 𝑖 ௡௜ୀଵ

**160**

© T. Gemmeke, IDS, RWTH; R. Leupers, SSS

Da es für das gleiche Problem nicht nur viele mögliche unterschiedliche Algorithmen, sondern auch unterschiedlichste Darstellungen für denselben Algorithmus in Form von Programmen gibt, ist es das Ziel, Algorithmen miteinander vergleichen zu können. Dies nennt man **Komplexitätsanalyse von Algorithmen.** Die Komplexität kann als Maß für die **Effizienz** eines Algorithmus herangezogen werden.

Kriterien für die Analyse sind häufig **Laufzeit** und **Speicherplatzbedarf**. Die Komplexität wird ausgedrückt in Abhängigkeit von der Menge und Größe der bearbeiteten Daten.

Im obigen Beispiel ist die Berechnung der Fakultätsfunktion (hier: Fakultät von 10) dargestellt.