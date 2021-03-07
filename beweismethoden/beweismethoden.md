
### Beweismethoden

Die verschiedenen Beweismethoden werden an Beispielen aus 
der Zahlentheorie gezeigt.

#### Grundbegriffe der Zahlentheorie

$\mathbb{N}$ : natürliche Zahlen = 1, 2, 3, ...  <br>
$n, m \in \mathbb{N}$ : n und m sind natürliche Zahlen <br>
$m | n: m$ teilt $n, n$  ist Vielfaches von $m, 
 \exists k \in \mathbb{N}: n \cdot k = m$ <br>
$m$ ist echter Teiler von $n$, falls $1 < k < m$ <br>


Zwei natürliche Zahlen heißen *teilerfremd*, wenn sie nur die 1 als gemeinsamen
Teiler besitzen.

Eine natürliche Zahl größer eins, die nur durch sich selbst und durch 1 teilbar ist, heißt *Primzahl*
Eine Zahl heißt *prim*, wenn sie eine Primzahl ist, andernfalls heißt sie *zusammengesetzt*.

Die *Goldbachsche Vermutung (1742)* ist bis heute ungelöst: <br>
*Jede gerade Zahl größer 2 ist die Summe zweier Primzahlen*.

Die Vermutung, dass es unendlich viele *Primzahlzwillinge* gibt, ist bis heute ungelöst. <br>
(3,5), (5,7), (9,11), ...

**Satz:** (*Euklisches Lemma*) <br>
Teilt eine Primzahl $p$ ein Produkt $a \cdot b$ natürlicher Zahlen, so teilt $p$ einen (oder
beide) der Faktoren $a$ oder $b$.

**Theorem:** (*Eindeutige Primfaktorzerlegung*) <br>
Jede natürliche Zahl größer 1 lässt sich als Produkt von Primzahlen schreiben,
und diese Primfaktorzerlegung ist bis auf die Reihenfolge der Faktoren
eindeutig.

#### Direkter Beweis

Mathematische Sätze sind meist als $A \Rightarrow B$ formuliert. Lies: 'Aus A folgt B' oder 'A impliziert B' oder 'Wenn A wahr ist, dann ist auch B wahr'.

Beim *direkten* Beweis geht man davon aus, dass A wahr ist und folgert durch eine Kette gültiger Argumente, dass dann auch B wahr ist.

Wir gliedern den Beweis:
-  Formulierung der *Voraussetzung*.
-  Formulierung der *Behauptung*.
-  eigentlicher Beweis. 

Es gibt auch Sätze, die als $A \Leftrightarrow B$ formuliert sind.
Lies: A gilt genau dann, wenn B gilt. <br>
In diesem Fall müssen beide Implikationen gezeigt werden.

#### Hinreichende und notwendige Bedingung

Gilt die Implikation $A \Rightarrow B$, so nennt man A eine *hinreichende Bedingung* für B und B eine *notwendige Bedingung* für A.

Beispiel: A = 'n ist Vielfaches von 4', B = 'n ist gerade'.

#### Indirekter Beweis 

Will man einen Satz $A \Rightarrow B$ beweisen, so kann man auch seine
Kontraposition $\lnot B \Rightarrow \lnot A$ beweisen.

#### Widerspruchsbeweis

Man geht davon aus, dass die zu beweisende Aussage falsch ist
und führt dies zu einem Widerspruch, z.B. zu einem absurden Resultat wie $1 < 0$, oder etwa dass gleichzeitig $A$ und $\lnot A$ wahr ist. Somit erweist sich die Annahme, die zu beweisende Aussage sei falsch, als nicht haltbar, woraus die Wahrheit der Aussage folgt.

Der erste bekannt Widerspruchsbeweis stammt von Euklid:

*$\sqrt{2}$ ist eine irrationale Zahl, also nicht durch einen Bruch darstellbar.*

#### Vollständige Induktion

Die vollständige Induktion ist ein Beweisverfahren, das in folgender Situation angewendet wird: Zu jeder natürlichen Zahl n ist eine Aussage
A(n) gegeben, deren Gültigkeit man beweisen will.

Die Aussagen A(n) sind für alle n ∈ N wahr, wenn man Folgendes zeigen kann:

- (IA) Induktionsanfang: A(1) ist wahr.
- (IS) Induktionsschritt: Wenn A(n) für ein n wahr ist, dann stimmt auch A(n+1).

Die Annahme, dass A(n) wahr ist, heißt Induktionsvoraussetzung (IV).