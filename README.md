# Funktionsübersicht

* [ABS](#abs)
* [ADD](#add)
* [AND](#and)
* [BOOL](#bool)
* [CEIL](#ceil)
* [DAY](#day)
* [DIFFERENCE_IN_DAYS](#difference_in_days)
* [DIFFERENCE_IN_YEARS](#difference_in_years)
* [DIVIDE](#divide)
* [EQ](#eq)
* [EXISTS](#exists)
* [FLOOR](#floor)
* [GT](#gt)
* [GTE](#gte)
* [IF_THEN_ELSE](#if_then_else)
* [JOIN](#join)
* [JOIN_ALL](#join_all)
* [LENGTH](#length)
* [LIKE](#like)
* [LT](#lt)
* [LTE](#lte)
* [MAX](#max)
* [MIN](#min)
* [MONTH](#month)
* [MULTIPLY](#multiply)
* [NOT](#not)
* [NUM](#num)
* [OR](#or)
* [PROD](#prod)
* [STR](#str)
* [SUBSTRING](#substring)
* [SUBTRACT](#subtract)
* [SUM](#sum)
* [YEAR](#year)

---

## ABS

### Beschreibung

Berechnet den Absolutwert der angegebenen Zahl.

### Syntax

```ts
["ABS", <zahl>] => number
```

### Argumente

| | Name | Typ |
| --- | --- | --- |
| Argument 1 | zahl | number

### Beispiele

#### Ohne berechenbares Ergebnis

```ts
["ABS"] => undefined
["ABS", undefined] => undefined
["ABS", true] => undefined
["ABS", "3"] => undefined
["ABS", [3]] => undefined
["ABS", 2, 3] => undefined
```

#### Korrekte Aufrufe mit Ergebnis

```ts
["ABS", 5] => 5
["ABS", -34] => 34
["ABS", 5.434] => 5.434
["ABS", -3.141] => 3.141
```

[zur Funktionsübersicht](#funktionsübersicht)

---

## ADD

### Beschreibung

Berechnet die Summe der angegebenen Zahlen.

### Syntax

```ts
["ADD", <summandA>, <summandB>] => number
```

### Argumente

| | Name | Typ |
| --- | --- | --- |
| Argument 1 | summandA | number
| Argument 2 | summandB | number

### Beispiele

#### Ohne berechenbares Ergebnis

```ts
["ADD"] => undefined
["ADD", 3] => undefined
["ADD", 3, undefined] => undefined
["ADD", 3, true] => undefined
["ADD", 4, "3"] => undefined
["ADD", [3,4]] => undefined
```

#### Korrekte Aufrufe mit Ergebnis

```ts
["ADD", 2, 3] => 5
["ADD", 23.34, 15.65] => 38.99
["ADD", 0.1, 0.2] => 0.3
["ADD", 34, -16] => 18
```

[zur Funktionsübersicht](#funktionsübersicht)

---

## AND

### Beschreibung

Berechnet die Konjunktion der beiden angegebenen Wahrheitswerte.

### Syntax

```ts
["AND", <wertA>, <wertB>] => boolean
```

### Argumente

| | Name | Typ |
| --- | --- | --- |
| Argument 1 | wertA | boolean
| Argument 2 | wertB | boolean

### Beispiele

#### Ohne berechenbares Ergebnis

```ts
["AND"] => undefined
["AND", undefined] => undefined
["AND", true] => undefined
["AND", false] => undefined
["AND", [true,true]] => undefined
["AND", true, true, true] => undefined
["AND", true, false, undefined] => undefined
```

#### Korrekte Aufrufe mit Ergebnis

```ts
["AND", undefined, undefined] => false
["AND", undefined, false] => false
["AND", undefined, true] => false
["AND", true, undefined] => false
["AND", false, undefined] => false
["AND", false, false] => false
["AND", true, false] => false
["AND", false, true] => false
["AND", true, true] => true
```

[zur Funktionsübersicht](#funktionsübersicht)

---

## BOOL

### Beschreibung

Berechnet den Wahrheitswert vom angegebenen Wert

### Syntax

```ts
["BOOL", <wert>] => boolean
```

### Argumente

| | Name | Typ |
| --- | --- | --- |
| Argument 1 | wert | boolean

### Beispiele

#### Ohne berechenbares Ergebnis

```ts
["BOOL"] => undefined
["BOOL", true, false] => undefined
["BOOL", [true]] => undefined
["BOOL", "true"] => undefined
```

#### Korrekte Aufrufe mit Ergebnis

```ts
["BOOL", undefined] => false
["BOOL", false] => false
["BOOL", true] => true
```

[zur Funktionsübersicht](#funktionsübersicht)

---

## CEIL

### Beschreibung

Berechnet den aufgerundeten Wert der angegebenen Zahl.

### Syntax

```ts
["CEIL", <zahl>] => number
```

### Argumente

| | Name | Typ |
| --- | --- | --- |
| Argument 1 | zahl | number

### Beispiele

#### Ohne berechenbares Ergebnis

```ts
["CEIL"] => undefined
["CEIL", undefined] => undefined
["CEIL", true] => undefined
["CEIL", "3"] => undefined
["CEIL", [3.3]] => undefined
["CEIL", 3.3, 1.5] => undefined
```

#### Korrekte Aufrufe mit Ergebnis

```ts
["CEIL", 5] => 5
["CEIL", 33.3] => 34
["CEIL", -0.5] => 0
["CEIL", -5.2] => -5
```

[zur Funktionsübersicht](#funktionsübersicht)

---

## DAY

### Beschreibung

Berechnet den Tag vom angegebenen Datum.

### Syntax

```ts
["DAY", <datum>] => number
```

### Argumente

| | Name | Typ |
| --- | --- | --- |
| Argument 1 | datum | date

### Beispiele

#### Ohne berechenbares Ergebnis

```ts
["DAY"] => undefined
["DAY", undefined] => undefined
["DAY", true] => undefined
["DAY", ["2018-04-20"]] => undefined
["DAY", "2018-04-20", "2018-04-24"] => undefined
["DAY", "2019-04-33"] => undefined
```

#### Korrekte Aufrufe mit Ergebnis

```ts
["DAY", "2019-08-19T17:52:09.125Z"] => 19
["DAY", "2019-08-14"] => 14
["DAY", "2019-04"] => 1
["DAY", "2019"] => 1
```

[zur Funktionsübersicht](#funktionsübersicht)

---

## DIFFERENCE_IN_DAYS

### Beschreibung

Berechnet die Tage zwischen den angegebenen Daten.

### Syntax

```ts
["DIFFERENCE_IN_DAYS", <datumA>, <datumB>] => number
```

### Argumente

| | Name | Typ |
| --- | --- | --- |
| Argument 1 | datumA | date
| Argument 2 | datumB | date

### Beispiele

#### Ohne berechenbares Ergebnis

```ts
["DIFFERENCE_IN_DAYS"] => undefined
["DIFFERENCE_IN_DAYS", undefined] => undefined
["DIFFERENCE_IN_DAYS", true] => undefined
["DIFFERENCE_IN_DAYS", ["2018-04-20","2018-04-24"]] => undefined
["DIFFERENCE_IN_DAYS", undefined, "2018-04-20"] => undefined
["DIFFERENCE_IN_DAYS", "2018-04-20", undefined] => undefined
["DIFFERENCE_IN_DAYS", "2018-04-20"] => undefined
```

#### Korrekte Aufrufe mit Ergebnis

```ts
["DIFFERENCE_IN_DAYS", "2019-06-19", "2019-06-19"] => 0
["DIFFERENCE_IN_DAYS", "2019-08-19", "2019-08-17"] => 2
["DIFFERENCE_IN_DAYS", "2019-08-17", "2019-08-19"] => 2
["DIFFERENCE_IN_DAYS", "2019-08-17", "2019-09-19"] => 33
```

[zur Funktionsübersicht](#funktionsübersicht)

---

## DIFFERENCE_IN_YEARS

### Beschreibung

Berechnet die Jahre zwischen den angegebenen Daten.

### Syntax

```ts
["DIFFERENCE_IN_YEARS", <datumA>, <datumB>] => number
```

### Argumente

| | Name | Typ |
| --- | --- | --- |
| Argument 1 | datumA | date
| Argument 2 | datumB | date

### Beispiele

#### Ohne berechenbares Ergebnis

```ts
["DIFFERENCE_IN_YEARS"] => undefined
["DIFFERENCE_IN_YEARS", undefined] => undefined
["DIFFERENCE_IN_YEARS", true] => undefined
["DIFFERENCE_IN_YEARS", ["2018-04-20","2018-04-24"]] => undefined
["DIFFERENCE_IN_YEARS", undefined, "2018-04-20"] => undefined
["DIFFERENCE_IN_YEARS", "2018-04-20", undefined] => undefined
["DIFFERENCE_IN_YEARS", "2018-04-20"] => undefined
```

#### Korrekte Aufrufe mit Ergebnis

```ts
["DIFFERENCE_IN_YEARS", "2014-06-19", "2014-11-19"] => 0
["DIFFERENCE_IN_YEARS", "2016-08-19", "2019-08-17"] => 3
["DIFFERENCE_IN_YEARS", "2019-08-17", "2011-08-19"] => 8
```

[zur Funktionsübersicht](#funktionsübersicht)

---

## DIVIDE

### Beschreibung

Berechnet den Quotienten der angegebenen Zahlen.

### Syntax

```ts
["DIVIDE", <dividend>, <divisor>] => number
```

### Argumente

| | Name | Typ |
| --- | --- | --- |
| Argument 1 | dividend | number
| Argument 2 | divisor | number

### Beispiele

#### Ohne berechenbares Ergebnis

```ts
["DIVIDE"] => undefined
["DIVIDE", 3] => undefined
["DIVIDE", 3, undefined] => undefined
["DIVIDE", 3, true] => undefined
["DIVIDE", 4, "3"] => undefined
["DIVIDE", [3,4]] => undefined
["DIVIDE", 2, 0] => undefined
```

#### Korrekte Aufrufe mit Ergebnis

```ts
["DIVIDE", 6, 2] => 3
["DIVIDE", 6.25, 2.5] => 2.5
["DIVIDE", 0.2, 0.1] => 2
["DIVIDE", -3, 1.5] => -2
```

[zur Funktionsübersicht](#funktionsübersicht)

---

## EQ

### Beschreibung

Prüft die angegebenen Zahlen auf Gleichheit.

### Syntax

```ts
["EQ", <zahlA>, <zahlB>] => boolean
```

### Argumente

| | Name | Typ |
| --- | --- | --- |
| Argument 1 | zahlA | number
| Argument 2 | zahlB | number

### Beispiele

#### Ohne berechenbares Ergebnis

```ts
["EQ"] => undefined
["EQ", 3] => undefined
["EQ", 3, true] => undefined
["EQ", 4, "3"] => undefined
["EQ", [3,4]] => undefined
```

#### Korrekte Aufrufe mit Ergebnis

```ts
["EQ", undefined, undefined] => false
["EQ", 3, undefined] => false
["EQ", 3, 3] => true
["EQ", 0, 0] => true
["EQ", 3, -3] => false
["EQ", -1.23456, -1.23456] => true
```

[zur Funktionsübersicht](#funktionsübersicht)

---

## EXISTS

### Beschreibung

Berechnet den Wahrheitswert für die Existenz des angegebenen Wertes.

### Syntax

```ts
["EXISTS", <wert>] => boolean
```

### Argumente

| | Name | Typ |
| --- | --- | --- |
| Argument 1 | wert | any

### Beispiele

#### Ohne berechenbares Ergebnis

```ts
["EXISTS"] => undefined
["EXISTS", 3, 4] => undefined
```

#### Korrekte Aufrufe mit Ergebnis

```ts
["EXISTS", undefined] => false
["EXISTS", false] => true
["EXISTS", true] => true
["EXISTS", 42] => true
["EXISTS", ""] => true
["EXISTS", "Hallo"] => true
["EXISTS", [42]] => true
```

[zur Funktionsübersicht](#funktionsübersicht)

---

## FLOOR

### Beschreibung

Berechnet den aufgerundeten Wert der angegebenen Zahl.

### Syntax

```ts
["FLOOR", <zahl>] => number
```

### Argumente

| | Name | Typ |
| --- | --- | --- |
| Argument 1 | zahl | number

### Beispiele

#### Ohne berechenbares Ergebnis

```ts
["FLOOR"] => undefined
["FLOOR", undefined] => undefined
["FLOOR", true] => undefined
["FLOOR", "3"] => undefined
["FLOOR", [3.3]] => undefined
["FLOOR", 3.3, 1.5] => undefined
```

#### Korrekte Aufrufe mit Ergebnis

```ts
["FLOOR", 5] => 5
["FLOOR", 33.3] => 33
["FLOOR", -0.5] => -1
["FLOOR", -5.2] => -6
```

[zur Funktionsübersicht](#funktionsübersicht)

---

## GT

### Beschreibung

Prüft die angegebenen Zahlen auf eine Größer-als-Beziehung.

### Syntax

```ts
["GT", <zahlA>, <zahlB>] => boolean
```

### Argumente

| | Name | Typ |
| --- | --- | --- |
| Argument 1 | zahlA | number
| Argument 2 | zahlB | number

### Beispiele

#### Ohne berechenbares Ergebnis

```ts
["GT"] => undefined
["GT", 3] => undefined
["GT", 3, true] => undefined
["GT", 4, "3"] => undefined
["GT", [3,4]] => undefined
["GT", undefined, undefined] => undefined
["GT", 3, undefined] => undefined
```

#### Korrekte Aufrufe mit Ergebnis

```ts
["GT", 3, 3] => false
["GT", 0, 0] => false
["GT", 1.23, 1.22] => true
["GT", 1.23, 1.23] => false
["GT", -1.23, -1.23] => false
["GT", -1.23, -1.24] => true
```

[zur Funktionsübersicht](#funktionsübersicht)

---

## GTE

### Beschreibung

Prüft die angegebenen Zahlen auf eine Größergleich-als-Beziehung.

### Syntax

```ts
["GTE", <zahlA>, <zahlB>] => boolean
```

### Argumente

| | Name | Typ |
| --- | --- | --- |
| Argument 1 | zahlA | number
| Argument 2 | zahlB | number

### Beispiele

#### Ohne berechenbares Ergebnis

```ts
["GTE"] => undefined
["GTE", 3] => undefined
["GTE", 3, true] => undefined
["GTE", 4, "3"] => undefined
["GTE", [3,4]] => undefined
["GTE", undefined, undefined] => undefined
["GTE", 3, undefined] => undefined
```

#### Korrekte Aufrufe mit Ergebnis

```ts
["GTE", 3, 3] => true
["GTE", 0, 0] => true
["GTE", 1.23, 1.23] => true
["GTE", 1.23, 1.24] => false
["GTE", -1.23, -1.22] => false
["GTE", -1.23, -1.23] => true
```

[zur Funktionsübersicht](#funktionsübersicht)

---

## IF_THEN_ELSE

### Beschreibung

Berechnet sich abhängig von der "bedingung". Ist die Bedingung 'wahr' ist das Ergebnis der "dann" ansonsten der "sonst" Wert.

### Syntax

```ts
["IF_THEN_ELSE", <bedingung>, <dann>, <sonst>] => any
```

### Argumente

| | Name | Typ |
| --- | --- | --- |
| Argument 1 | bedingung | boolean
| Argument 2 | dann | any
| Argument 3 | sonst | any

### Beispiele

#### Ohne berechenbares Ergebnis

```ts
["IF_THEN_ELSE"] => undefined
["IF_THEN_ELSE", true, 4] => undefined
["IF_THEN_ELSE", true, 3, 4, 5] => undefined
["IF_THEN_ELSE", true, undefined, 5] => undefined
["IF_THEN_ELSE", false, 4, undefined] => undefined
```

#### Korrekte Aufrufe mit Ergebnis

```ts
["IF_THEN_ELSE", true, 4, undefined] => 4
["IF_THEN_ELSE", false, undefined, 5] => 5
["IF_THEN_ELSE", undefined, "left", "right"] => right
["IF_THEN_ELSE", false, "left", "right"] => right
["IF_THEN_ELSE", true, "left", "right"] => left
```

[zur Funktionsübersicht](#funktionsübersicht)

---

## JOIN

### Beschreibung

Berechnet die Verkettung der beiden Zeichenketten. Ist ein Trennzeichen angegeben wird dies zwischen den Zeichenketten eingefügt.

### Syntax

```ts
["JOIN", <trennzeichen>, <zeichenketteA>, <zeichenketteB>] => string
```

### Argumente

| | Name | Typ |
| --- | --- | --- |
| Argument 1 | trennzeichen | string
| Argument 2 | zeichenketteA | string
| Argument 3 | zeichenketteB | string

### Beispiele

#### Ohne berechenbares Ergebnis

```ts
["JOIN"] => undefined
["JOIN", "-"] => undefined
["JOIN", "-", "Hallo"] => undefined
["JOIN", "-", undefined, undefined] => undefined
["JOIN", "-", "Hallo", true] => undefined
["JOIN", "-", "Hallo", 1] => undefined
["JOIN", "-", "Hallo", "Welt", "!"] => undefined
["JOIN", "-", ["Hallo","Welt"]] => undefined
["JOIN", ["-","Hallo","Welt"]] => undefined
```

#### Korrekte Aufrufe mit Ergebnis

```ts
["JOIN", "-", "Hallo", undefined] => Hallo
["JOIN", "-", undefined, "Hallo"] => Hallo
["JOIN", undefined, "Hallo", "Welt"] => HalloWelt
["JOIN", "-+-", "Hallo", "Welt"] => Hallo-+-Welt
```

[zur Funktionsübersicht](#funktionsübersicht)

---

## JOIN_ALL

### Beschreibung

Berechnet die Verkettung von der Liste von Zeichenketten. Ist ein Trennzeichen angegeben wird dies zwischen den Zeichenketten eingefügt.

### Syntax

```ts
["JOIN_ALL", <trennzeichen>, <zeichenketten>] => string
```

### Argumente

| | Name | Typ |
| --- | --- | --- |
| Argument 1 | trennzeichen | string
| Argument 2 | zeichenketten | array&lt;string&gt;

### Beispiele

#### Ohne berechenbares Ergebnis

```ts
["JOIN_ALL"] => undefined
["JOIN_ALL", "-"] => undefined
["JOIN_ALL", "-", undefined] => undefined
["JOIN_ALL", "-", "Hallo"] => undefined
["JOIN_ALL", "-", "Hallo", "Welt"] => undefined
["JOIN_ALL", undefined, [""]] => undefined
```

#### Korrekte Aufrufe mit Ergebnis

```ts
["JOIN_ALL", "-+-", ["Hallo",""]] => Hallo
["JOIN_ALL", undefined, ["Hallo",null]] => Hallo
["JOIN_ALL", undefined, ["Hallo","Welt","!"]] => HalloWelt!
["JOIN_ALL", " ", ["Hallo","Welt","!"]] => Hallo Welt !
["JOIN_ALL", "-+-", ["Hallo",null,"Welt","","!"]] => Hallo-+-Welt-+-!
```

[zur Funktionsübersicht](#funktionsübersicht)

---

## LENGTH

### Beschreibung

Berechnet die Länge der angegebenen Zeichenkette.

### Syntax

```ts
["LENGTH", <zeichenkette>] => number
```

### Argumente

| | Name | Typ |
| --- | --- | --- |
| Argument 1 | zeichenkette | string

### Beispiele

#### Ohne berechenbares Ergebnis

```ts
["LENGTH"] => undefined
["LENGTH", undefined] => undefined
["LENGTH", true] => undefined
["LENGTH", 42] => undefined
["LENGTH", ["Hallo"]] => undefined
["LENGTH", "Hallo", "Welt"] => undefined
```

#### Korrekte Aufrufe mit Ergebnis

```ts
["LENGTH", ""] => 0
["LENGTH", "Hi"] => 2
["LENGTH", "Hallo Welt"] => 10
```

[zur Funktionsübersicht](#funktionsübersicht)

---

## LIKE

### Beschreibung

Prüft die angegebenen Zeichenketten auf Gleichheit (ohne Berücksichtigung der Groß- und Kleinschreibung).

### Syntax

```ts
["LIKE", <zeichenketteA>, <zeichenketteB>] => boolean
```

### Argumente

| | Name | Typ |
| --- | --- | --- |
| Argument 1 | zeichenketteA | string
| Argument 2 | zeichenketteB | string

### Beispiele

#### Ohne berechenbares Ergebnis

```ts
["LIKE"] => undefined
["LIKE", "Hi"] => undefined
["LIKE", true, "Hi"] => undefined
["LIKE", 3, "Hi"] => undefined
["LIKE", ["Hi","Hi"]] => undefined
["LIKE", "Hi", "Hi", "Hi"] => undefined
```

#### Korrekte Aufrufe mit Ergebnis

```ts
["LIKE", undefined, undefined] => false
["LIKE", undefined, "Ho"] => false
["LIKE", "Hi", undefined] => false
["LIKE", "Hallo", "Hallo"] => true
["LIKE", "HALLO", "hallo"] => true
["LIKE", "alles ANDERS", "ALLES anders"] => true
```

[zur Funktionsübersicht](#funktionsübersicht)

---

## LT

### Beschreibung

Prüft die angegebenen Zahlen auf eine Kleiner-als-Beziehung.

### Syntax

```ts
["LT", <zahlA>, <zahlB>] => boolean
```

### Argumente

| | Name | Typ |
| --- | --- | --- |
| Argument 1 | zahlA | number
| Argument 2 | zahlB | number

### Beispiele

#### Ohne berechenbares Ergebnis

```ts
["LT"] => undefined
["LT", 3] => undefined
["LT", 3, true] => undefined
["LT", 4, "3"] => undefined
["LT", [3,4]] => undefined
["LT", undefined, undefined] => undefined
["LT", 3, undefined] => undefined
```

#### Korrekte Aufrufe mit Ergebnis

```ts
["LT", 3, 3] => false
["LT", 0, 0] => false
["LT", 1.23, 1.24] => true
["LT", 1.23, 1.23] => false
["LT", -1.23, -1.23] => false
["LT", -1.23, -1.22] => true
```

[zur Funktionsübersicht](#funktionsübersicht)

---

## LTE

### Beschreibung

Prüft die angegebenen Zahlen auf eine Kleinergleich-als-Beziehung.

### Syntax

```ts
["LTE", <zahlA>, <zahlB>] => boolean
```

### Argumente

| | Name | Typ |
| --- | --- | --- |
| Argument 1 | zahlA | number
| Argument 2 | zahlB | number

### Beispiele

#### Ohne berechenbares Ergebnis

```ts
["LTE"] => undefined
["LTE", 3] => undefined
["LTE", 3, true] => undefined
["LTE", 4, "3"] => undefined
["LTE", [3,4]] => undefined
["LTE", undefined, undefined] => undefined
["LTE", 3, undefined] => undefined
```

#### Korrekte Aufrufe mit Ergebnis

```ts
["LTE", 3, 3] => true
["LTE", 0, 0] => true
["LTE", 1.23, 1.23] => true
["LTE", 1.23, 1.22] => false
["LTE", -1.23, -1.24] => false
["LTE", -1.23, -1.23] => true
```

[zur Funktionsübersicht](#funktionsübersicht)

---

## MAX

### Beschreibung

Berechnet das Maximum der angegebenen Zahlen.

### Syntax

```ts
["MAX", <zahlA>, <zahlB>] => number
```

### Argumente

| | Name | Typ |
| --- | --- | --- |
| Argument 1 | zahlA | number
| Argument 2 | zahlB | number

### Beispiele

#### Ohne berechenbares Ergebnis

```ts
["MAX"] => undefined
["MAX", 3] => undefined
["MAX", 3, undefined] => undefined
["MAX", 3, true] => undefined
["MAX", 4, "3"] => undefined
["MAX", [3,4]] => undefined
```

#### Korrekte Aufrufe mit Ergebnis

```ts
["MAX", 2, 3] => 3
["MAX", 23.34, 15.65] => 23.34
["MAX", -15, -16] => -15
["MAX", 0.1, 0.1] => 0.1
```

[zur Funktionsübersicht](#funktionsübersicht)

---

## MIN

### Beschreibung

Berechnet das Minimum der angegebenen Zahlen.

### Syntax

```ts
["MIN", <zahlA>, <zahlB>] => number
```

### Argumente

| | Name | Typ |
| --- | --- | --- |
| Argument 1 | zahlA | number
| Argument 2 | zahlB | number

### Beispiele

#### Ohne berechenbares Ergebnis

```ts
["MIN"] => undefined
["MIN", 3] => undefined
["MIN", 3, undefined] => undefined
["MIN", 3, true] => undefined
["MIN", 4, "3"] => undefined
["MIN", [3,4]] => undefined
```

#### Korrekte Aufrufe mit Ergebnis

```ts
["MIN", 2, 3] => 2
["MIN", 23.34, 15.65] => 15.65
["MIN", -15, -16] => -16
["MIN", 0.1, 0.1] => 0.1
```

[zur Funktionsübersicht](#funktionsübersicht)

---

## MONTH

### Beschreibung

Berechnet den Monat vom angegebenen Datum.

### Syntax

```ts
["MONTH", <datum>] => number
```

### Argumente

| | Name | Typ |
| --- | --- | --- |
| Argument 1 | datum | date

### Beispiele

#### Ohne berechenbares Ergebnis

```ts
["MONTH"] => undefined
["MONTH", undefined] => undefined
["MONTH", true] => undefined
["MONTH", ["2018-04-20"]] => undefined
["MONTH", "2018-04-20", "2018-04-24"] => undefined
["MONTH", "2019-04-33"] => undefined
```

#### Korrekte Aufrufe mit Ergebnis

```ts
["MONTH", "2019-08-19T17:52:09.125Z"] => 8
["MONTH", "2019-06-14"] => 6
["MONTH", "2019-04"] => 4
["MONTH", "2019"] => 1
```

[zur Funktionsübersicht](#funktionsübersicht)

---

## MULTIPLY

### Beschreibung

Berechnet die Multiplikation der angegebenen Zahlen.

### Syntax

```ts
["MULTIPLY", <faktorA>, <faktorB>] => number
```

### Argumente

| | Name | Typ |
| --- | --- | --- |
| Argument 1 | faktorA | number
| Argument 2 | faktorB | number

### Beispiele

#### Ohne berechenbares Ergebnis

```ts
["MULTIPLY"] => undefined
["MULTIPLY", 3] => undefined
["MULTIPLY", 3, undefined] => undefined
["MULTIPLY", 3, true] => undefined
["MULTIPLY", 4, "3"] => undefined
["MULTIPLY", [3,4]] => undefined
```

#### Korrekte Aufrufe mit Ergebnis

```ts
["MULTIPLY", 2, 0] => 0
["MULTIPLY", 6, 2] => 12
["MULTIPLY", 2.5, 2.5] => 6.25
["MULTIPLY", 0.2, -0.1] => -0.02
```

[zur Funktionsübersicht](#funktionsübersicht)

---

## NOT

### Beschreibung

Berechnet die Negation vom angegeben Wahrheitswert.

### Syntax

```ts
["NOT", <wert>] => boolean
```

### Argumente

| | Name | Typ |
| --- | --- | --- |
| Argument 1 | wert | boolean

### Beispiele

#### Ohne berechenbares Ergebnis

```ts
["NOT"] => undefined
["NOT", undefined, false] => undefined
["NOT", true, undefined] => undefined
["NOT", false, true] => undefined
["NOT", [true]] => undefined
["NOT", "true"] => undefined
```

#### Korrekte Aufrufe mit Ergebnis

```ts
["NOT", undefined] => true
["NOT", false] => true
["NOT", true] => false
```

[zur Funktionsübersicht](#funktionsübersicht)

---

## NUM

### Beschreibung

Berechnet die Zahl vom angegebenen Wert

### Syntax

```ts
["NUM", <zahl>] => number
```

### Argumente

| | Name | Typ |
| --- | --- | --- |
| Argument 1 | zahl | number

### Beispiele

#### Ohne berechenbares Ergebnis

```ts
["NUM"] => undefined
["NUM", undefined] => undefined
["NUM", true] => undefined
["NUM", "3"] => undefined
["NUM", [3]] => undefined
["NUM", 3, 4] => undefined
```

#### Korrekte Aufrufe mit Ergebnis

```ts
["NUM", 1.23] => 1.23
["NUM", -411.23] => -411.23
```

[zur Funktionsübersicht](#funktionsübersicht)

---

## OR

### Beschreibung

Berechnet die Disjunktion der beiden angegebenen Wahrheitswerte.

### Syntax

```ts
["OR", <wertA>, <wertB>] => boolean
```

### Argumente

| | Name | Typ |
| --- | --- | --- |
| Argument 1 | wertA | boolean
| Argument 2 | wertB | boolean

### Beispiele

#### Ohne berechenbares Ergebnis

```ts
["OR"] => undefined
["OR", undefined] => undefined
["OR", true] => undefined
["OR", false] => undefined
["OR", [true,true]] => undefined
["OR", true, true, true] => undefined
["OR", true, false, undefined] => undefined
```

#### Korrekte Aufrufe mit Ergebnis

```ts
["OR", undefined, undefined] => false
["OR", undefined, false] => false
["OR", undefined, true] => true
["OR", true, undefined] => true
["OR", false, undefined] => false
["OR", false, false] => false
["OR", true, false] => true
["OR", false, true] => true
["OR", true, true] => true
```

[zur Funktionsübersicht](#funktionsübersicht)

---

## PROD

### Beschreibung

Berechnet das Produkt von der Liste von Zahlen.

### Syntax

```ts
["PROD", <faktoren>] => number
```

### Argumente

| | Name | Typ |
| --- | --- | --- |
| Argument 1 | faktoren | array&lt;number&gt;

### Beispiele

#### Ohne berechenbares Ergebnis

```ts
["PROD"] => undefined
["PROD", undefined] => undefined
["PROD", 3] => undefined
["PROD", []] => undefined
["PROD", [3,"3",4]] => undefined
["PROD", [3,true,4]] => undefined
["PROD", [3,null,4]] => undefined
```

#### Korrekte Aufrufe mit Ergebnis

```ts
["PROD", [3,4]] => 12
["PROD", [1,2,3,4,5]] => 120
["PROD", [0.1,-0.2]] => -0.02
```

[zur Funktionsübersicht](#funktionsübersicht)

---

## STR

### Beschreibung

Berechnet die Zeichenkette vom angegebenen Wert

### Syntax

```ts
["STR", <zeichenkette>] => string
```

### Argumente

| | Name | Typ |
| --- | --- | --- |
| Argument 1 | zeichenkette | string

### Beispiele

#### Ohne berechenbares Ergebnis

```ts
["STR"] => undefined
["STR", undefined] => undefined
["STR", ""] => undefined
["STR", false] => undefined
["STR", 3] => undefined
["STR", ["Hallo"]] => undefined
["STR", "Hi", "Ho"] => undefined
```

#### Korrekte Aufrufe mit Ergebnis

```ts
["STR", "Hi"] => Hi
["STR", "H A L L O"] => H A L L O
```

[zur Funktionsübersicht](#funktionsübersicht)

---

## SUBSTRING

### Beschreibung

Berechnet eine Teilzeichenkette der angegebenen Zeichenketten. Begonnen wird beim Index "start" (0 für das erste Zeichen) und es werden "länge" (oder alle restlichen, falls das weniger Zeichen sein sollten) Zeichen extrahiert.

### Syntax

```ts
["SUBSTRING", <start>, <länge>, <zeichenkette>] => string
```

### Argumente

| | Name | Typ |
| --- | --- | --- |
| Argument 1 | start | number
| Argument 2 | länge | number
| Argument 3 | zeichenkette | string

### Beispiele

#### Ohne berechenbares Ergebnis

```ts
["SUBSTRING"] => undefined
["SUBSTRING", undefined, undefined, undefined] => undefined
["SUBSTRING", undefined, undefined, "Hallo"] => undefined
["SUBSTRING", 2, undefined, "Hallo"] => undefined
["SUBSTRING", undefined, 3, "Hallo"] => undefined
["SUBSTRING", 0] => undefined
["SUBSTRING", 0, 3] => undefined
["SUBSTRING", 0, 3, "Hallo", "Welt"] => undefined
["SUBSTRING", [0,3,"Hallo"]] => undefined
["SUBSTRING", 0, true, "Hallo"] => undefined
["SUBSTRING", 0, "3", "Hallo"] => undefined
```

#### Korrekte Aufrufe mit Ergebnis

```ts
["SUBSTRING", 0, 5, "Hallo Welt!"] => Hallo
["SUBSTRING", 3, 6, "Hallo Welt!"] => lo Wel
```

[zur Funktionsübersicht](#funktionsübersicht)

---

## SUBTRACT

### Beschreibung

Berechnet die Differenz der angegebenen Zahlen.

### Syntax

```ts
["SUBTRACT", <minuend>, <subrahend>] => number
```

### Argumente

| | Name | Typ |
| --- | --- | --- |
| Argument 1 | minuend | number
| Argument 2 | subrahend | number

### Beispiele

#### Ohne berechenbares Ergebnis

```ts
["SUBTRACT"] => undefined
["SUBTRACT", 3] => undefined
["SUBTRACT", 3, undefined] => undefined
["SUBTRACT", 3, true] => undefined
["SUBTRACT", 4, "3"] => undefined
["SUBTRACT", [3,4]] => undefined
```

#### Korrekte Aufrufe mit Ergebnis

```ts
["SUBTRACT", 12, 3] => 9
["SUBTRACT", 23.34, 15.65] => 7.69
["SUBTRACT", 0.3, 0.2] => 0.1
["SUBTRACT", 34, -16] => 50
```

[zur Funktionsübersicht](#funktionsübersicht)

---

## SUM

### Beschreibung

Berechnet die Summe von der Liste von Zahlen.

### Syntax

```ts
["SUM", <summanden>] => number
```

### Argumente

| | Name | Typ |
| --- | --- | --- |
| Argument 1 | summanden | array&lt;number&gt;

### Beispiele

#### Ohne berechenbares Ergebnis

```ts
["SUM"] => undefined
["SUM", undefined] => undefined
["SUM", 3] => undefined
["SUM", []] => undefined
["SUM", [3,"3",4]] => undefined
["SUM", [3,true,4]] => undefined
["SUM", [3,null,4]] => undefined
```

#### Korrekte Aufrufe mit Ergebnis

```ts
["SUM", [1,2,3,4,5]] => 15
["SUM", [1,-2,3,-4]] => -2
["SUM", [0.1,0.2]] => 0.3
```

[zur Funktionsübersicht](#funktionsübersicht)

---

## YEAR

### Beschreibung

Berechnet das Jahr vom angegebenen Datum.

### Syntax

```ts
["YEAR", <datum>] => number
```

### Argumente

| | Name | Typ |
| --- | --- | --- |
| Argument 1 | datum | date

### Beispiele

#### Ohne berechenbares Ergebnis

```ts
["YEAR"] => undefined
["YEAR", undefined] => undefined
["YEAR", true] => undefined
["YEAR", ["2018-04-20"]] => undefined
["YEAR", "2018-04-20", "2018-04-24"] => undefined
["YEAR", "2019-12-33"] => undefined
```

#### Korrekte Aufrufe mit Ergebnis

```ts
["YEAR", "2019-08-19T17:52:09.125Z"] => 2019
["YEAR", "2015-08-14"] => 2015
["YEAR", "2011-04"] => 2011
["YEAR", "2010"] => 2010
```

[zur Funktionsübersicht](#funktionsübersicht)
