Integrierte Funktionen
======================

## abs

Die `abs` Funktion nimmt gibt den Betrag einer Zahl (integer oder floating point number) zurück.

```
>>> abs(-1)
1
>>> abs(-5)
5
>>> abs(5)
5
>>> abs(-2.5)
2.5
>>> abs(2.5)
2.5
```

## chr

Die `chr` Funktion gibt das Zeichen als String zurück, dessen Unicode Code Point als Argument übergeben wird.

```
>>> chr(65)
'A'
>>> chr(120)
'x'
```

## len

Die `len` Funktion gibt die Länge (Anzahl der Elemente) eines Objekts zurück.

```
>>> len("Hello World")
11
>>> len([4, 6, 2, 8, 4, 7])
6
```

## max

Die `max` Funktion gibt das größte der übergebenen Argumente zurück. Oder, wenn nur ein (iteriebares!) Argument übergeben wird, das größte Element dieses iterierbaren Objekts.

```
>>> max(7, -1, 9, 5)
9
>>> max('a', 'b', 'c')
'c'
>>> max([7, -1, 9, 5])
9
```

## min

Die `min` Funktion gibt das kleinste der übergebenen Argumente zurück. Oder, wenn nur ein (iteriebares!) Argument übergeben wird, das kleinste Element dieses iterierbaren Objekts.

```
>>> min(7, -1, 9, 5)
-1
>>> min('a', 'b', 'c')
'a'
>>> min([7, -1, 9, 5])
-1
```

## open

Die `open` Funktion öffnet eine Datei und gibt ein Datei Objekt zurück. Der Path der zu öffnenden Datei wird als String angegeben. 

```
>>> f = open('file.txt')
```

<!-- TODO: Genauere Informationen gibt es im Kapitel über das Lesen von Dateien. -->


## ord

Die `ord` Funktion bekommt ein String mit einem Unicode Zeichen als Argument gegeben, und gibt den Integer der dieses Zeichen repräsentiert zurück.

```
>>> ord('A')
65
>>> ord('Z')
90
>>> ord('`')
96
>>> ord('a')
97
```

## pow

Die `pow` Funktion bekommt zwei oder drei Argumente gegeben, und gibt das Ergebnis des ersten Arguments potenziert mit dem zweiten zurück. Wenn das optionale dritte Argument vorhanden ist, so wird noch der Modulo mit diesem Argument berechnet. Die Variante mit den zwei Argumenten ist äquivalent zum "power operator": `x**y`.

## print

Die `print` Funktion "druckt" Objekte standardmäßig auf die Standardausgabe, wohin gedruckt werden soll kann mit dem Keyword Argument `file` geändert werden. Mit dem Keyword Argument `sep` (default: `' '`) kann der Seperator bestimmt werden, der beim Drucken von mehreren Objekten diese trennt. Mit dem Keyword Argument `end` (default: `\n`) kann bestimmt werden, was nach dem Drucken der Objekte noch zusätzlich gedruckt werden soll.

```
>>> print("hello", "world")
hello world
>>> print("hello", "world", sep='-')
hello-world
>>> print("hello", "world", end='XXX')
hello worldXXX>>>
>>> print("hello", "world", sep='_', end='.py\n')
hello_world.py
```

## range

`range` ist eigentlich keine Funktion, sondern eine immutable Sequenz.
<!-- Trotzdem hier erklären? -->

## reversed

Die `reversed` Funktion bekommt ein sequenzielles Objekt als Argument gegeben und gibt einen invertierten Iterator zurück.

```
>>> reversed([1,2,3,4,5])
<list_reverseiterator object at 0x107262eb8>
>>> for n in reversed([1,2,3,4,5]):
...     print(n)
... 
5
4
3
2
1
```

## round

Die `round` Funktion gibt den Integer zurück, der dem gegebenen (ersten) Argument am nächsten ist. Ein optionales zweites Argument kann benutzt werden, um nicht zum nächsten Integer zu runden, sondern zu einer bestimmten Stelle nach dem Dezimalpunkt.

```
>>> round(23.3)
23
>>> round(23.123456789, 1)
23.1
>>> round(23.123456789, 4)
23.1235
>>> round(23.123456789, 8)
23.12345679
```

## sorted

Die `sorted` Funktion nimmt ein iterierbares Objekt (wie zum Beispiel eine Liste) und gibt eine neue sortierte Liste zurück. Mit dem Keyword Argument `key` kann der Schlüssel bestimmt werden, nach dem sortiert werden soll. Mit dem Keyword Argument `reverse` kann angegeben werden, ob die sortierte Liste invertiert zurückgegeben werden soll.

```
>>> sorted([5, 2, 3, 1, 4])
[1, 2, 3, 4, 5]
>>>
>>> sorted("This is a test string from Andrew".split())
['Andrew', 'This', 'a', 'from', 'is', 'string', 'test']
>>>
>>> sorted("This is a test string from Andrew".split(), key=str.lower)
['a', 'Andrew', 'from', 'is', 'string', 'test', 'This']
>>>
>>> sorted("This is a test string from Andrew".split(), key=str.lower, reverse=True)
['This', 'test', 'string', 'is', 'from', 'Andrew', 'a']
```

## str

Die `str` Funktion gibt eine String Version des übergebenen Arguments zurück.

```
>>> 1
1
>>> str(1)
'1'
```


## sum

Die `sum` Funktion gibt die Summe der Elemente eines iterierbaren Objektes zurück. Mit einem optionalen zweiten Argument kann eine Zahl festgelegt werden, die zusätzlich addiert werden soll.

```
>>> sum([1,2,3])
6
>>> sum([1,2,3], 10)
16
```