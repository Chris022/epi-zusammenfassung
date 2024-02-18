
**Was ist ein Computer**: Eine Maschine zur Speicherung und automatischen Verarbeitung von Daten durch Angabe einer programmierbaren vorschrift.
Dabei nennen wir:
- **Hardware**: das "Unveränderbare"
- **Software**: das "Veränderbare"

**Was macht ein Computer**: Im Wesentlichen führt ein Computer lediglich Rechnungen aus und Speicher Ergebnisse.

**Elektronisch**: Ist ein Teilgebiet der Elektrotechnik und beschäftigt sich vor Allem mit ICs, Röhren und Transistoren.

**Digital**:Werte sind wert- und zeit-diskret. Vergleich Analog: Werte sind wert- und zeit-kontinuierlich.
Bei der Umwandlung (Digitalisierung) wird zeitlich Abgetastet und wertmäßig Quantisiert.

**Digitalrechner**: Arbeiten lediglich mit zwei Signalzuständen (=Bits). Ein Bit hat nur die Werte: 0 und 1.
Wichtig: Die Präzision von Berechnungen kann man aber trotzdem beliebig hoch treiben.

## Bits und Bytes
**Bit**: Ein Bit ist eine elementare Speichereinheit und beschreibt ein "An"/"Aus" bzw. "1"/"0".

**Bit-Vektor**: Ist ein Tupel von mehreren Bits.
Dabei bezeichnet man $2^{10}$ Bits als Kilo, $2^{20}$ Bits als Mega usw.

ACHTUNG. Eigentlich währen $2^{10}$ ein Kibibit und $10^3$ ein Kilobit. Aber es hat sich durchgesetzt trotzdem die obige Definition zu nutzen.
**Byte**: Ein Bit-Vektor bestehend aus 8 Bit. Ein Byte kann also 256 Zustände annehmen. Ein Byte sind dabei zwei Nibbles. Gleiche Präfixe wie bei Bit.

## Von-Neumann-Rechner
Ermöglichte es, im Vergleich zu anderen Rechnern der Zeit, sehr schnell Programmänderungen durchzuführen und ist deshalb heute die Architektur fast aller Rechner.
Der universelle Rechner basierte auf einem Schaltungskonzept mit folgenden Komponenten:
- dem Rechenwerk zur Durchführung von Rechenoperationen
- dem Speicher zum speichern von Daten und Programmen
- dem Steuerwerk zur interpretation von Anweisungen und zur Steuerung der Ausführung
- dem Eingabe/Ausgabewerk zur Ein und Ausgabe von Daten
- dem Verbindungssystem

Dabei bilden das Rechen- und Steuerwerk den CPU.

![[assets/von_neumann_architektur.png]]

Ein Programm für einen Solchen Rechner besteht dann immer aus einer Sammlung an Befehlsworte. Diese Bestehen immer aus einer Fixen Anzahl aus Bits. Wobei die ersten n Bits die Operation beschreiben. Zum Beispiel "Addiere". Diesen Teil nennt man Opcode. Es folgen dann 2 oder 3 je m große Bitvektoren die die Operanden für die Operation beschreiben.

Beispiel Befehl: Add 10 10 = 0100 1010 1010

Ein Befehls-Ausführungszyklus besteht aus der Folge:
1. Befehl aus dem Speicher holen (von der Adresse im Programmcönter) - FETCH
2. Befehl im Steuerwerk interpretieren - DECODE
3. Operanden holen - FETCH OPERANDS
4. Befehl ausführen - EXECUTE
5. Erhöhen von Programmcönter - Update PC
## Speicher
Ein optimaler Speicher sollte möglichst Schnell sein, die Daten persistent (ohne Strom) dauerhaft speichern = nicht flüchtig sein, möglichst große Kapazität haben, physikalisch möglichst klein sein, wenig Strom verbrauchen und wenig kosten.
Da dies nicht alles gleichzeitig geht, gibt es je nach Anwendung unterschiedliche Speicher.

**Register**: Diese befinden sich direkt im Prozessor und sind super schnelle (meist)flüchtige Speicher.

**Cache**: Da der Hauptspeicher meist zu langsam ist der Cache ein schnellerer Zwischenspeicher. Heute gibt es meist mehrere Caches pro CPU Kern:
- L1 - super schnell
- L2 - etwas größer
- L3 - gemeinsam für alle Kerne

**Hauptspeicher**: Der sogenannte RAM eines Computers ist der Speicher der die gerade auszuführenden Programmteile und die dabei benötigten Daten enthält.

**Sekundärspeicher**: Auf diesen kann nicht direkt durch den CPU zugegriffen werden, erfordert also Ein-/Ausgabekanäle. Speichert immer Daten die nicht im aktiven Gebrauch sind und ist persistent. Ist fast immer mit Dateisystem formatiert.

**Tertiärspeicher**: Langzeitspeicher von Daten. Meistens sehr große Speicherkapazitäten. Oft optische/magnetische Plattenspeicher.
## Geschichte
Die meisten Computer basieren auf der von-Neumann-Architektur und erfüllen somit alle Anforderungen an einen Computer und sind Turing-vollständig. Meistens haben Computer heute mehrere Prozessorkerne (=Multiprozessoren).
Wir unterscheiden zwischen CISC(Complex Instruction Set Computer) und RISC(Reduced Instruction Set Computer) Computer.

**Turing-Maschine**: Ist ein Computer welcher lediglich aus einem Magnetband und einem Lese/Schreibe Kopf besteht. Der Kopf kann Bits vom Band lesen/schreiben. Eine solche Maschine kann alles Berechenbare berechnen.
Man spricht von einem Turing-vollständigen System, wenn durch das System eine Turingmaschine simuliert werden kann.

**Analog vs Digitalcomputer**: Die Definition eines Computers ist eingeschränkt auf Digitalrechner.
Eine andere Art sind Analogrechner. Diese stellen Werte nicht als diskrete sondern als kontinuierliche Größen dar.
Genutzt werden diese um Differentialgleichungen oder Integrale zu lösen. Ein solches Programm besteht dann aus Summierens, Multiplizierer usw.