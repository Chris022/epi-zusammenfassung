In diesem Abschnitt geht es um die generelle Darstellung verschiedener Zahlenwerte. Diese hat nicht direkt etwas mit dem Computer zu tun.

**Dezimalsystem** Eine Rationale Zahl schreiben wir für gewöhnlich als vorzeichenbehaftete Dezimalzahl, also in einem Stellenwertsystem zur Basis 10. Der Wert einer Dezimalzahl ist also 
$$\text{Repräsentation}=z_{m}z_{m-1}\dots z_{1}z_{0},z_{-1}z_{-2}\dots z_{-n} \quad \text{Wert}=\sum^m_{i=-n}z_{i}\cdot 10^i$$

**Stellenwertsystem - Generell** Man kann nun einen Wert auch in einem Stellenwertsystem mit jeder anderen Basis $b\in\mathbb{N}_{>1}$ darstellen. Als Ziffern stehen dabei immer die Symbole $\{ 0,\dots,b-1 \}$ zur Verfügung. Der Wert der Zahl ist dann immer
$$\text{Repräsentation}=z_{m}z_{m-1}\dots z_{1}z_{0},z_{-1}z_{-2}\dots z_{-n} \quad \text{Wert}=\sum^m_{i=-n}z_{i}\cdot b^i$$
**Binärsystem** Das Binärsystem hat eine Basis von $2$.

**Oktalsystem** Das Oktalsystem hat eine Basis von $8$. Das Praktische hierbei ist, dass je drei Stellen einer Binärzahl einer Stelle einer Oktalzahl entsprächen.

**Hexadezimalsystem** Das Hexadezimalsystem hat eine Basis von $16$. Das Praktische hierbei ist, dass je vier Stellen einer Binärzahl einer Stelle einer Oktalzahl entsprächen.

**Konvertierungstabelle** 
Da man in der Informatik wirklich regelmäßig zwischen Dual, Hexadezimal und Oktalsystem hin und her rechnen muss, lernt man die folgende Tabelle am besten auswendig.

| Bin  | Hex | Okt | Bin  | Hex |
| ---- | --- | --- | ---- | --- |
| 0000 | 0   | 0   | 1000 | 8   |
| 0001 | 1   | 1   | 1001 | 9   |
| 0010 | 2   | 2   | 1010 | A   |
| 0011 | 3   | 3   | 1011 | B   |
| 0100 | 4   | 4   | 1100 | C   |
| 0101 | 5   | 5   | 1101 | D   |
| 0110 | 6   | 6   | 1110 | G   |
| 0111 | 7   | 7   | 1111 | F   |

**Konertierung vom Dezimalsystem** Will man eine Dezimalzahl in ein anderes System umwandeln mach man dies mit Kettendivision und Kettenmultiplikation.
Kettendivison verwendet man für den Teil vor dem Komma: Sei $Z$ die Zahl in Dezimal ohne Kommastelle und $b$ die Basis des Zielsystems, so dividiert man $Z$ schrittweise durch $b$. Die Reste ergeben dann jeweils die Ziffer der niedrigsten Stelle in der neuen Zahl. Man wiederholt dies bis als Ergebnis 0 raus kommt.
$$\begin{align}
210: 8 &= 26 \ Rest \ 2 \\
26: 8 &= 3 \ Rest  \ 2 \\
3: 8 &= 0 \ Rest \ 3 \\
\text{Repräsentation} &= 322
\end{align}$$
Kettenmultiplikation verwendet man für den Teil nach dem Komma:: Sei $Z$ eine Zahl in Dezimal der Form $0,1\dots$ und $b$ die Basis des Zielsystems, so multipliziert man $Z$ schrittweise mit $b$. Tritt ein Wert größer als 1 auf, wird dessen ganzzahliger anteil wieder entfernt. Am Ende - also wenn als Ergebnis einer Multiplikation 1,0 vor kommt - ergeben alle ganzzahligen Anteile die Nachkommastellen von vorne nach hinten.$$\begin{align}
0.123 \cdot 8 &= 0 \ .984  \\
0.984 \cdot 8 &= 7 \ .872  \\
0.872 \cdot 8 &= 6 \ .976 \\
0.976 \cdot 8 &= 7 \ .808 \\
... \\
... \\ \\
\text{Repräsentation} &= 0,0767\dots
\end{align}$$
**Konvertierung ins Dezimalsystem** Will man eine Zahl zur Basis $b$ ins Dezimalsystem wandeln rechnet man einfach den Wert der jeweiligen Zahl aus. Also 
$$DecZ=\sum^m_{i=-n}z_{i}\cdot b^i$$

**Wichtige Rechenoperationen** Sei $b$ die Basis eines Stellenwertsystems und $Z$ eine Zahl in diesem System. So ist
- $Z0 = b\cdot Z$: Anfügen einer Null gleich Multiplikation mit der Basis.
- $z_{m}\dots z_{1}=Z//b$: Entfernen der letzen Stelle gleich ganzzahlige Division durch die Basis.
- Addieren, Multiplizieren und Subtrahieren(ohne Negative Zahlen) klappt dabei wie im Dezimalsystem, man muss jedoch bei Überträgen Aufpassen. z.B.: $1_{(2)}+1_{(2)}=0_{(2)} \ \text{ Übertrag: }1_{(2)}$