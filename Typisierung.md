**Datentypen**: Ein Datentyp ist eine Zusammenfassung von Objektmengen mit den darauf definierten Operationen.

**Stark/Schwache Typisierung**: Man bezeichnet nun eine Sprache, wie Python, als *stark Typisiert* wenn sich der Datentyp eines Wertes nicht mehr ändern lässt. Heißt ein Text ist und bleibt ein Text und kann nicht als Zahl interpretiert werden. Dies hat den Vorteil, dass mögliche Programmierfehler bereits sehr früh im ausführungsprozess gefunden werden können.
Ist dies hingegen möglich spricht man von *schwacher Typisierung*.

**Statische/Dynamische Typisierung**: Bei Statischer Typisierung muss der Datentyp einer Variable bereits während der Compilierung bekannt sein. Bei der dynamischen Typisierung erfolgt die Zuweisung des Datentyp erst während der Laufzeit.

**Coercion vs. Conversion**: Coercion beschreibt dabei die implizite Konvertierung von Datentypen. Diese wird von Python oft automatisch erledigt und ist vor allem beim Rechnen mit Zahlen benötigt:
1 - 3 -> ist eine ganze Zahl -> /2 -> ist eine rationale Zahl -> sqrt(x) -> ist eine komplexe Zahl. Bei Conversion hingegen beschreibt die explizite Konvertierung von einem Datentyp in einen anderen. Ein Beispiel ist hierbei die Konvertierung von Text in eine Zahl.

**Funktionen zur Conversion**: 

| Ziel-Typ | Funktion |
| ---- | ---- |
| int | `int(val[,basis=10])`, `ord(char)` |
| float | `float(val)` |
| complex | `complex(val)` |
| bool | `bool(val)` |
| str | `repr(val)`, `ascii(val)`, `str(val)` |
| str | `byte_1.decode(encoding='utf-8')` |
| str | `hex(int)`, `oct(int)`, `bin(int)`, `chr(int)` |