# 8. Lineare Datentypen

原始 PDF 第 229–260 页。

## 8. Lineare Datentypen

**8.1 Listen**
8.2 Stacks
8.3 Queues

229

© T. Gemmeke, IDS, RWTH; R. Leupers, SSS

---

## Mengendarstellung

• **Problemstellung**: Verwaltung einer Menge von Objekten $A   =   \{ a _ { 1 } , \ldots , a _ { n } \}$ vom Typ T

• Gewünschte **Operationen**:

– Suchen, Einfügen und Entfernen von Elementen
– Vereinigung und Durchschnitt zweier Mengen 𝐴𝐴 und 𝐵𝐵

• Prinzipiell wäre ein **Array** als Datenstruktur geeignet
• Jedoch zwei Probleme:

– **Einfügen** eines neuen Elementes an einer bestimmten Position erfordert aufwendige **Umordnung**
– **Größe** der Menge muss **statisch** feststehen (Bspw. Deklaration: T A[100]; erlaubt max. 100 Elemente)

![](../../raw/pages_0225-0256/images/page_229_image_13.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph LR
  Input["Input"] -->|"Verschieben"| Output["Output"]
```
</details>

230

© T. Gemmeke, IDS, RWTH; R. Leupers, SSS

---

Verkettete Listen

**Def**.: Eine **(verkettete) Liste** ist entweder leer oder besteht aus einer Referenz auf einen **Knoten**, der ein Element und eine Referenz auf eine verkettete Liste enthält.

• Verwendung von **Zeigern** (siehe Kap. 3)
• Modellierung eines **Knotens** für ein Element vom Typ T:
typedef struct node {T\* data; struct node\* next; } \*nodeptr;
• data ist Zeiger auf Listenelement vom Typ T
next ist Zeiger auf Nachfolgerknoten

![](../../raw/pages_0225-0256/images/page_230_image_9.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph LR
  A["nodeptr"] --> B["Next"]
  B --> C["Object vom Typ T"]
  C --> D["Data"]
  D --> E["Next"]
  E --> F["Rest-Liste"]
  F -.-> G["Final Output"]
```
</details>

231

© T. Gemmeke, IDS, RWTH; R. Leupers, SSS

---

Verkettete Listen

• Liste im **Speicher** (vgl. Kap. 3)
• Liste = 1. Element + Restliste
Darstellung einer leeren Liste: #define NULL 0
Zeigerwert NULL bedeutet, dass der Zeiger „nirgendwohin“ zeigt
Speicherzugriff per NULL-Zeiger ist **unzulässig**, führt i.A. zum Programmabsturz

![](../../raw/pages_0225-0256/images/page_231_image_7.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph LR
  A["Input"] --> B["Block 1"]
  B --> C["Block 2"]
  C --> D["NULL"]
  D --> E["Final Output"]
```
</details>

Adr.

![](../../raw/pages_0225-0256/images/page_231_image_9.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph TD
  A["Data"] --> B["Next"]
  B --> C["Data"]
  C --> D["Next"]
  D --> E["T"]
```
</details>

232

© T. Gemmeke, IDS, RWTH; R. Leupers, SSS

---

Listenoperationen

• Definition des Datentyps **Liste**, Elemente vom Typ T

```c
typedef struct node {
    T* data;
    struct node* next; } Node, *nodeptr;

typedef struct list {
    nodeptr first, last; } List, *listptr;
```

![](../../raw/pages_0225-0256/images/page_232_image_3.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph LR
  A["L.first"] --> B["Step 1"]
  B --> C["Step 2"]
  C --> D["NULL"]
```
</details>

• Erzeugung einer **leeren Liste** und **Leerheitstest**

```c
List L;
void Init(listptr L)
{
    L->first = NULL; L->last = NULL;
}

int IsEmpty(List L)
{
    return (L.first == NULL && L.last == NULL);
}
```

233

© T. Gemmeke, IDS, RWTH; R. Leupers, SSS

---

Listenoperationen

• **Einfügen** eines neuen Listenelements vom Typ T am Listenanfang

![](../../raw/pages_0225-0256/images/page_233_image_2.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph LR
  A["Input Block"] --> B["Output Block"]
  B --> C["Input Block"]
  C --> D["Output Block"]
  D --> E["Result Output"]
```
</details>

Funktion „malloc“ (siehe Kap. 3) stellt dynamisch Speicherplatz auf dem Heap bereit
Funktion „sizeof“ berechnet die erforderliche Anzahl von Bytes (hier z.B. insges. 8 Bytes bei 32-Bit-Zeigern)

```c
nodeptr newnode(T* item)
{
    nodeptr np;

    np = (nodeptr)malloc(sizeof(Node));
    np->data = item;
    np->next = NULL;

    return np;
}
```

234

© T. Gemmeke, IDS, RWTH; R. Leupers, SSS

---

Einfügen am Listenanfang

```txt
void AppendFirst(T* item, listptr L)
{
    nodeptr np = newnode(item);
    if (IsEmpty(*L)) {
        L->first = np; L->last = np;
    } else {
        np->next = L->first;
        L->first = np;
    }
}
```

![](../../raw/pages_0225-0256/images/page_234_image_2.jpg)

235

© T. Gemmeke, IDS, RWTH; R. Leupers, SSS

---

Einfügen am Listenende

```txt
void AppendLast(T* item, listptr L)
{
    nodeptr np = newnode(item);
    if (IsEmpty(*L)) {
        L->first = np; L->last = np;
    } else {
        L->last->next = np;
        L->last = np;
    }
}
```

![](../../raw/pages_0225-0256/images/page_235_image_2.jpg)

236

© T. Gemmeke, IDS, RWTH; R. Leupers, SSS

---

Prüfen ob Element in Liste enthalten

```cpp
int IsIn(T* item, List L)
{
    nodeptr np;
    if (IsEmpty(L)) return 0; // false
    np = L.first;
    while (np != NULL) {
        if (Equal(np->data, item)) return 1; // true
        np = np->next;
    }
    return 0; // false
}
```

![](../../raw/pages_0225-0256/images/page_236_image_2.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph LR
  Input["Input"] --> Block1["Block 1"]
  Block1 --> Block2["Block 2"]
  Block2 --> Output["NULL"]
```
</details>

• **Laufzeit** bei N-elementiger Liste:

– Best case: O(1)
– Worst case: O(N)
– Average case: O(N/2) = O(N)

237

© T. Gemmeke, IDS, RWTH; R. Leupers, SSS

---

Einfügen hinter ein bestimmtes Listenelement

```c
// item2 hinter item1 einfügen
void InsertBehind(T* item1,
  T* item2, listptr L)
{
  nodeptr np, newnp;

  if (!IsIn(item1,*L)) {
    printf(„Fehler!“); return;
  }

  np = L->first;
  while (np != NULL) {
    if (Equal(np->data,item1)) {
      newnp = newnode(item2);
      newnp->next = np->next;
      np->next = newnp;
      if (np == L->last) {
        L->last = newnp;
      }
      break;
    }
    np = np->next;
  }
}
```

![](../../raw/pages_0225-0256/images/page_237_image_2.jpg)

238

© T. Gemmeke, IDS, RWTH; R. Leupers, SSS

---

## Löschen eines Listenelementes

```c
void Delete(T* item, listptr L)
{
    nodeptr np1, np2;

    if (IsEmpty(*L)) return;
    np1 = L->first;
    if (Equal(np1->data,item)) {
        L->first = np1->next;
        if (L->first == NULL)
            L->last = NULL;
        free(np1);
        return;
    }
    np2 = np1->next;
    while (np2 != NULL) {
        if (Equal(np2->data,item)) {
            np1->next = np2->next;
            if (np2 == L->last)
                L->last = np1;
            free(np2);
            break;
        }
        np1 = np2;
        np2 = np2->next;
    }
}
```

![](../../raw/pages_0225-0256/images/page_238_image_2.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph LR
  A["np1"] --> B["Block 1"]
  B --> C["np2"]
  C --> D["Block 2"]
  D --> E["NULL"]
```
</details>

![](../../raw/pages_0225-0256/images/page_238_image_3.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph LR
  A["np1"] --> B["Block 1"]
  B --> C["np2"]
  C --> D["Block 2"]
  D --> E["NULL"]
```
</details>

239

© T. Gemmeke, IDS, RWTH; R. Leupers, SSS

---

Zusammenfügen zweier Listen

• Falls Liste als Mengendarstellung: entspricht **Vereinigung**
• Evtl. **Mehrfachvorkommen** von Elementen ausschließen

L1:

![](../../raw/pages_0225-0256/images/page_239_image_5.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph LR
  A["Stage 1"] --> B["Stage 2"]
  B --> C["Stage 3"]
  C --> D["L2:"]
  D --> E["Stage 4"]
  E --> F["NULL"]
```
</details>

```c
listptr Union(listptr L1, listptr L2)
{
    if (IsEmpty(*L2)) return L1;
    if (IsEmpty(*L1)) return L2;

    L1->last->next = L2->first;
    L1->last = L2->last;

    return L1;
}
```

240

© T. Gemmeke, IDS, RWTH; R. Leupers, SSS

---

Schnittmengenberechnung mittels Listen

```c
listptr Intersect(listptr L1, listptr L2)
{
    nodeptr np;
    listptr L = (listptr)malloc(sizeof(List));
    Init(L);
    np = L1->first;
    while (np != NULL) {
        if (IsIn(np->data, *L2)) AppendLast(np->data, L);
        np = np->next;
    }
    return L;
}
```

L1:

![](../../raw/pages_0225-0256/images/page_240_image_3.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph LR
  A["A"] --> B["B"]
  B --> C["C"]
  C --> D["D"]
  D --> E["E"]
  E --> NULL["NULL"]
```
</details>

L2:

![](../../raw/pages_0225-0256/images/page_240_image_5.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph LR
  A["B"] --> B["D"]
  B --> C["E"]
  C --> D["G"]
  D --> E["NULL"]
```
</details>

L:

![](../../raw/pages_0225-0256/images/page_240_image_7.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph LR
  A["B"] --> B["D"]
  B --> C["E"]
  C --> D["NULL"]
```
</details>

241

© T. Gemmeke, IDS, RWTH; R. Leupers, SSS

---

## 8. Lineare Datentypen

8.1 Listen
**8.2 Stacks**
8.3 Queues

242

© T. Gemmeke, IDS, RWTH; R. Leupers, SSS

---

Stacks

**Def**.: Ein **Stack** (Stapel) ist ein ADT, der folgende Grundoperationen unterstützt:

1. Einfügen eines neuen Elementes $( , \mathsf { P u s h } ^ { n } )$
2. Entfernen des zuletzt eingefügten Elementes $( , P o p ^ { n } )$

• Stacks sind eine **grundlegende Datenstruktur** in vielen Anwendungen

– Ablagesystem auf Professorenschreibtisch
– Compiler-Frontend (Analyse des Quellprogramms)
– Abarbeitung von C-Funktionsaufrufen

Aufgrund der Pop-Operation auch als **LIFO-Datenstruktur** bezeichnet (last in, first out)

Stack als ADT, d.h. **verschiedene Implementierungen** möglich (z.B. Listen und Arrays)

243

© T. Gemmeke, IDS, RWTH; R. Leupers, SSS

---

Push und Pop

push D

push EC

push B

push A

**stack**

![](../../raw/pages_0225-0256/images/page_243_image_6.jpg)

244

© T. Gemmeke, IDS, RWTH; R. Leupers, SSS

---

Beispiel: Laufzeit-Stack für C-Funktionsaufrufe

• Siehe auch Kap. 5
Funktion f wird durch Aufruf von g **unterbrochen** und später **fortgesetzt**
g kann ihrerseits **weitere Funktionen** aufrufen
Umgebung zur Programmausführung muss einen **Stack noch aktiver Funktionen** verwalten
• **Funktionsaufruf** = Push
• **Funktionsende** = Pop

![](../../raw/pages_0225-0256/images/page_244_image_9.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph TD
  A["Statement f₁"] --> B["Statement f₂"]
  B --> C["Aufruf"]
  C --> D["Statement g₁"]
  D --> E["Statement g₂"]
  E --> F["Statement f₃"]
  F --> G["Statement f₄"]
  E --> H["Rücksprung"]
```
</details>

**Zeit**

245

© T. Gemmeke, IDS, RWTH; R. Leupers, SSS

---

## Beispiel: Laufzeit-Stack für C-Funktionsaufrufe

```c
void f(void)
{
    g();
}

void g(void)
{
    h();
}

void h(void)
{
    i();
}

void i(void)
{
}

int main(void)
{
    f();
    g();
    h();

    return 0;
}
```

<strong><u>main</u></strong>

f <strong><u>main</u></strong>

g f <strong><u>main</u></strong>

h g f <strong><u>main</u></strong>

i h g f <strong><u>main</u></strong>

h g f <strong><u>main</u></strong>

g f <strong><u>main</u></strong>

f <strong><u>main</u></strong> <strong><u>main</u></strong>

g <strong><u>main</u></strong>

h g <strong><u>main</u></strong>

i h g <strong><u>main</u></strong>

h g <strong><u>main</u></strong>

g <strong><u>main</u></strong> <strong><u>main</u></strong>

h <strong><u>main</u></strong>

i h <strong><u>main</u></strong> <strong><u>main</u></strong>

246

© T. Gemmeke, IDS, RWTH; R. Leupers, SSS

---

Stack-Implementierung durch Listen

Elemente auf Stack = Listenelemente
• Push = Einfügen am Listenanfang
• Pop = Entfernen des ersten Elementes
• Stack für beliebigen Elementtyp T:

```c
List L;

void Push(T* item,listptr L)
{
    AppendFirst(item, L);
}

T* Pop(listptr L)
{
    T* item;
    if (IsEmpty(*L)) return NULL;

    item = L->first->data;
    Delete(item, L);
    return item;
}
```

![](../../raw/pages_0225-0256/images/page_246_image_7.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph TD
  A["Stage 1"] --> B["Intermediate 1"]
  B --> C["Intermediate 2"]
  C --> D["Intermediate 3"]
  D --> E["Final Stage"]
```
</details>

247

© T. Gemmeke, IDS, RWTH; R. Leupers, SSS

---

Stack-Implementierung durch Arrays

• Vorgabe der **max. Stack-Größe** notwendig
Elemente auf Stack = Arrayelemente
„**top**“ verweist stets auf das nächste freie Element (top = „**Stack-Pointer**“)
Push = Einfügen und Erhöhen von top um 1
Pop = Entfernen und Erniedrigen von top um 1
Prüfen auf **Überlauf** (im Gegensatz zu Listen!)

```c
#define MAX 100
typedef struct stk
{ T* elems[MAX]; int top; } stack;

void Init(stack* s)
{ s->top = 0; }

int IsEmpty(stack s)
{ return (s.top == 0); }

void Push(T* item,stack* s)
{
    if (s->top == MAX)
        printf(„Stack voll!“);
    s->elems[s->top] = item;
    s->top++;
}

T* Pop(stack* s)
{
    if (IsEmpty(*s)) return NULL;
    s->top--;
    return s->elems[s->top];
}
```

248

© T. Gemmeke, IDS, RWTH; R. Leupers, SSS

---

Beispiel-Anwendung

• Auswertung geklammerter **arithmetischer Ausdrücke**
– z.B. (( 6 \* ( 4 \* 28)) + ( 9 - (( 12 / 4) \* 2)))

**Innere Ausdrücke** vor äußeren auszuwerten

• Speicherung von Zwischenergebnissen notwendig

• **Zwei Stacks**: Operanden- und Operatorstack

Abarbeitung eines Ausdrucks **von links nach rechts**:

$\mathcal { N } ^ { ( 1 ) } ;$ keine Aktion
– Operand: Push auf Operandenstack
– Operator: Push auf Operatorstack
– „)“: Pop des obersten Operators, Pop der obersten beiden Operanden, Ausdruck auswerten, Push Ergebnis auf Operandenstack

249

© T. Gemmeke, IDS, RWTH; R. Leupers, SSS

---

Beispiel

$$
((6 * (4 * 2 8)) + (9 - ((1 2 / 4) * 2)))
$$

Operandenstack

| 6 |
| --- |
| 6 4 |
| 6 4 28 |
| 6 112 |
| 672 |
| 672 9 |
| 672 9 12 |
| 672 9 12 4 |
| 672 9 3 |
| 672 9 3 2 |
| 672 9 6 |
| 672 3 |
| 675 |

Operatorstack

| * |
| --- |
| ** |
| * |
| (leer) |
| + |
| +- |
| +-/ |
| +- |
| +-* |
| +- |
| +(leer) |

250

© T. Gemmeke, IDS, RWTH; R. Leupers, SSS

---

## 8. Lineare Datentypen

8.1 Listen
8.2 Stacks
**8.3 Queues**

251

© T. Gemmeke, IDS, RWTH; R. Leupers, SSS

---

Queues

## Def.: Eine Queue (Warteschlange) ist ein ADT, der folgende Grundoperationen unterstützt:

1. Einfügen eines neuen Elementes $( , P u t ^ { n } )$
2. Entfernen des zuerst eingefügten Elementes $( \mathrm { { , } } \mathrm { { G e t } } ^ { n } )$

• Verbreitete Datenstruktur, z.B.
– Warteschlange von auszuführenden Prozessen
– Kommunikationspuffer z.B. für Druckaufträge
• **FIFO-Prinzip**: first in, first out („zuerst gekommen, zuerst bedient“)

![](../../raw/pages_0225-0256/images/page_251_image_11.jpg)

<details>
<summary>text_image</summary>

DELZER
nach Originalrezept
Gelo!
E's
</details>

252

© T. Gemmeke, IDS, RWTH; R. Leupers, SSS

---

Put und Get

put D

put C

put B

put A

![](../../raw/pages_0225-0256/images/page_252_image_5.jpg)

<details>
<summary>text_image</summary>

queue
D
C
B
A
</details>

get → A

253

© T. Gemmeke, IDS, RWTH; R. Leupers, SSS

---

Put und Get

**queue**

![](../../raw/pages_0225-0256/images/page_253_image_2.jpg)

get → B

254

© T. Gemmeke, IDS, RWTH; R. Leupers, SSS

---

Put und Get

![](../../raw/pages_0225-0256/images/page_254_image_1.jpg)

<details>
<summary>text_image</summary>

queue
D
C
</details>

get → C

255

© T. Gemmeke, IDS, RWTH; R. Leupers, SSS

---

Queue-Implementierung durch Listen

• Queue-Elemente = Listenelemente
• Put = Einfügen am Listenende
• Get = Entfernen des ersten Elementes
• Queue für beliebigen Elementtyp T:

```c
List L;

void Put(T* item,listptr L)
{
    AppendLast(item, L);
}

T* Get(listptr L)
{
    T* item;

    if (IsEmpty(*L)) return NULL;

    item = L->first->data;
    Delete(item, L);

    return item;
}
```

![](../../raw/pages_0225-0256/images/page_255_image_7.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph TD
  A["Stage 1"] --> B["Intermediate 1"]
  B --> C["Intermediate 2"]
  C --> D["Intermediate 3"]
  D --> E["Final Stage"]
```
</details>

256

© T. Gemmeke, IDS, RWTH; R. Leupers, SSS

---

## Queue-Implementierung durch Arrays

Betrachte **Dynamik** von Queues im Vergleich zu Stacks in Array-Implementierung:

![](../../raw/pages_0257-0288/images/page_256_chart_2.jpg)

<details>
<summary>bar_stacked</summary>

| Category | Value 1 | Value 2 | Value 3 | Value 4 | Value 5 | Value 6 | Value 7 |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Row 1 | Blue | Light Green | Light Green | Light Green | Light Green | Light Green | Light Green |
| Row 2 | Blue | Blue | Light Green | Light Green | Light Green | Light Green | Light Green |
| Row 3 | Blue | Light Green | Light Green | Light Green | Light Green | Light Green | Light Green |
| Row 4 | Blue | Blue | Blue | Light Green | Light Green | Light Green | Light Green |
| Row 5 | Blue | Blue | Light Green | Light Green | Light Green | Light Green | Light Green |
</details>

**Stack**: verwendet tendenziell immer den gleichen Speicherbereich

![](../../raw/pages_0257-0288/images/page_256_chart_4.jpg)

<details>
<summary>bar_stacked</summary>

| Category | Segment 1 (Dark Blue) | Segment 2 (Light Blue) |
| --- | --- | --- |
| Row 1 | ~30% | ~70% |
| Row 2 | ~35% | ~65% |
| Row 3 | ~40% | ~60% |
| Row 4 | ~45% | ~55% |
| Row 5 | ~50% | ~50% |
</details>

**Queue**: „wandert“tendenziell immer weiter nach rechts, daher schlechte Speicherausnutzung

257

© T. Gemmeke, IDS, RWTH; R. Leupers, SSS

---

Queue-Implementierung durch Arrays

• Lösung: **ringförmiges** Array bzw. **zyklische** Adressierung

![](../../raw/pages_0257-0288/images/page_257_chart_2.jpg)

<details>
<summary>donut</summary>

| Category | Value |
| --- | --- |
| 1 | Blue dot |
| 2 | Blue dot |
| 3 | Blue dot |
| 4 | Blue dot |
| 5 | Blue dot |
| 6 | Blue dot |
| 7 | Blue dot |
| 8 | Blue dot |
| 9 | Blue dot |
| 10 | Blue dot |
| 11 | Blue dot |
| 12 | Blue dot |
| 13 | Blue dot |
| 14 | Blue dot |
| 15 | Blue dot |
| 16 | Blue dot |
| 17 | Blue dot |
| 18 | Blue dot |
| 19 | Blue dot |
| 20 | Blue dot |
</details>

258

© T. Gemmeke, IDS, RWTH; R. Leupers, SSS

---

## Queue-Implementierung durch Arrays

Zwei **Zeiger** (Array-Indizes) first und last verweisen auf aktuellen Anfang (-1) und Ende (+1) der Queue
Verwendung des Modulo-Operators (%) zur **zyklischen Adressierung**
Prüfung auf **Über- und Unterlauf** (overflow, underflow) erforderlich

```c
#define MAX 100

typedef struct q
{ T* elems[MAX];
  int first, last; } queue;

void Init(queue* q)
{
  q->first = 0;
  q->last = 1;
}

void Put(T* item,queue* q)
{
  if (q->last == q->first) overflow();
  else {
    q->elems[q->last] = item;
    q->last = (q->last+1) % MAX;
  }
}

T* Get(queue* q)
{
  q->first = (q->first+1) % MAX;
  if (q->first == q->last) underflow();
  else return q->elems[q->first];
}
```

259

© T. Gemmeke, IDS, RWTH; R. Leupers, SSS

---

Beispiel-Ablauf

![](../../raw/pages_0257-0288/images/page_259_image_1.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph TD
  A["Top Bar"] --> B["Second Bar"]
  B --> C["Third Bar"]
  C --> D["Fourth Bar"]
  D --> E["Bottom Bar"]
```
</details>

![](../../raw/pages_0257-0288/images/page_259_image_2.jpg)

<details>
<summary>flowchart</summary>

```mermaid
graph TD
  A["first"] --> B["last"]
  B --> C["frei"]
  C --> D["verwendet"]
```
</details>

260

© T. Gemmeke, IDS, RWTH; R. Leupers, SSS
