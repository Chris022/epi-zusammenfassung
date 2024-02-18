**Schritte der Software Entwicklung**: 
- *0*: das Problem beschreiben. Mit z.B. Lastenheft - beschreibt Anforderungen, und Pflichtenheft - beschreibt wie ein diese Anforderungen umgesetzt werden sollen.
- *1*: Beschreibung analysieren und Lösungsidee entwickeln und Beschreibung der benötigten Algorithmen und Datenstrukturen.
- *2*: Programmieren
- *3*: Testen des Programms
- *4*: Dokumentation des Programms

**Modularisierung**: Ein Modul ist ein abgeschlossener Teil Software, bestehend aus mehreren Teilprogrammen und den Datenstrukturen. In Python ist ein Modul einfach ein File. Funktionen daraus können dann mittels `import file_name` importiert und dann mit `file_name.function_name()` genutzt werden. Alternativ kann auch so importiert werden `form file_name import function_name` und so genutzt werden: `function_name()`. Soll code in einem Modul nur ausgeführt werden, wenn das file aufgerufen wird und nicht wenn es importiert wird so nutzt man die Schranke:
```python
if __name__ == "__main__":
	pass
```
