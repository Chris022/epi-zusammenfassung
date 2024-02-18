**SyntaxError**: Treten auf immer wenn ungültiger Pythoncode geschrieben wird.

**IndexError**: Tritt auf wenn man auf einen nicht existierenden Index zugreifen will - nicht beim slicing!

**KeyError**: Wenn man mittels Indexierung auf einen nicht vorhanden Key in einem Dict zugreifen will - nicht bei `.get(key)`

**NameError**: Wenn man auf eine nicht definierte Variable zugreifen will.

**AttributeError**: Wenn man auf ein Attribut eines Objektes zugreifen will, welches nicht existiert, also Methoden aber auch wirkliche Atribute.

**RecursionError** Bei unendlicher Rekursion

**TypeError** Bei Fehlern beim konvertieren von Daten z.B. `int("a")` aber auch wenn man einer operation oder Funktion einen Wert von ungültigen Typ übergibt z.B.: `1 + "a"` oder `len()`