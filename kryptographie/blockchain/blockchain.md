## Blockchain

Wir beginnen:

[Kryptographische Hashfunktion](https://andersbrownworth.com/blockchain/hash)

---

Wir erweitern die Eingabe zu einem Block.
Der Data-Teil ist jetzt in 3 Teile unterteilt und der Hash beginnt mit 4 Nullen. Weil der
Hash dieses Blocks mit 4 Nullen beginnt, nennen wir den Block *valid* oder *signiert*. Sobald man Daten
eingibt, ist der Block nicht mehr valid (rote Umrandung). Jetzt muss man die Nonce (Number used once)
so verändern, damit der Block wieder valid wird. Das ist das Mining.

[Block](https://andersbrownworth.com/blockchain/block)

---

Ein Blockchain ist eine Kette solcher Blöcke. Jeder Block (außer dem ersten) enthält den Hash des Vorgängers.
Wenn wir die Daten eines Blocks verändern, machen wir auch alle folgenden Blöcke invalid.

[Blockchain](https://andersbrownworth.com/blockchain/blockchain)

---

Damit wir keine Bank benötigen, gibt es die Blockchain nicht nur einmal, sondern jeder Anwender hat eine Kopie.
Wenn eine Blockchain irgendwo verändert wird, dann sehen wir an den letzten Hashwerten der Mehrheit, 
dass da was nicht stimmt.

[Verteilung](https://andersbrownworth.com/blockchain/distributed)

----

Im nächsten Schritt machen wir die Daten sinnvoller durch die Einführung von Transaktionen.
Auch hier würden wir merken, wenn in der Vergangenheit ein Wert geändert wird. In der Blockchain wird
nicht notiert, wieviel jeder aktuell auf seinem Konto hat, sondern es werden nur Transaktionen vermerkt.

[Tokens](https://andersbrownworth.com/blockchain/tokens)

---

Durch Coinbase-Transaktionen entsteht neues Geld. Wir können zurückverfolgen, ob Jackson $2 an Alexa zahlen kann.

[Coinbase](https://andersbrownworth.com/blockchain/coinbase)

---

Es muss noch dafür gesorgt werden, dass die Transaktions-Einträge nicht von Unbefugten gemacht werden können.
Dazu nutzen wir:

[Public/Private Keys](https://andersbrownworth.com/blockchain/public-private-keys/keys)

----

Jetzt können wir Nachrichten signieren.

[Signatures](https://andersbrownworth.com/blockchain/public-private-keys/signatures)

----

Statt einer Nachricht können wir auch eine Transaktion signieren.
Sender und Empfänger der Transaktion sind jetzt die public keys der Beteiligten.

[Transaction](https://andersbrownworth.com/blockchain/public-private-keys/transaction)

----

Diese Technik verwenden wir jetzt in der Blockchain.
In einem Block sind keine Namen mehr, sondern nur noch public keys und Signaturen. Wenn jetzt ein Betrag
geändert wird, wird nicht nur der Block invalid, sondern auch die Signatur. Die Signatur ist auch durch mining
nicht zu reparieren.

[Blockchain](https://andersbrownworth.com/blockchain/public-private-keys/blockchain)

------

## Zusammenfassung und weitere Details 

Die Kontonummer des Empfängers ist der öffentliche Schlüssel des Empfängers, genauer: der Hash des öffentlichen Schlüssels.

Alle Transaktionen werden in einem fälschungssicheren Rechnungsbuch festgehalten. Transaktionen werden an alle Teilnehmer im Netzwerk verteilt (distributed ledger). Teilnehmer sammeln diese Transaktionen in "Transaction Pools" und können diese (oder Teile davon) zu Blöcken verschweißen. Teilnehmer, die Blöcke generieren, heißen "Miner". 

So wie eine Transaktion nur valid ist, wenn es vom Sender signiert ist, so ist ein Block nur valid
wenn da ein proof-of-work ist. Der proof-of-work ist das Generieren eines bestimmten Hashwerts.

Jeder Block hat den Hash des vorherigen Blocks in seinem Header, damit ist die Reihenfolge eindeutig. Jeder Block enthält zu Beginn noch einen Eintrag: den block reward. 
Durch diesen Eintrag erhält der Miner neue Bitcoins "aus dem Nichts" als Belohnung für die geleistete Arbeit.

Die Miners hören auf Transaktionen, die sie zu Blöcken zusammenfassen, die Anwender hören auf neue upgedatete Blockchains, die von den Miners kommen. Wenn man zwei widersprüchliche Blockchains empfängt, wählt man den, in den die meiste Arbeit gesteckt wurde (die Länge der Kette).

Die Schwierigkeit des proof-of-work wird ab und zu geändert, so dass es im Schnitt 10 Minuten dauert, bis ein neuer Block entsteht. Die Block rewards werden immer kleiner, es begann mit 50 BTC im Januar 2009
Alle 210000 Blöcke (ca. alle 4 Jahre) wird der reward halbiert.
210000 * (50 + 25 + 12.5 + 6.25 + ...) = 21,000,000 ist die Obergrenze für alle Bitcoins.
Die Miners leben dann nur von Transaction Fees. Jeder Block kann ca. 2400 Transaktionen enthalten. Soll die eigene Transaktion in einen Block aufgenommen werden, ist es von Vorteil, ein incentive an die Miner zu geben.  (VISA: 1700 Transaktionen pro Sekunde)

---- 


## Links

[Erster Hinweis von Satoshi Nakamoto](https://www.mail-archive.com/cryptography%40metzdowd.com/msg09959.html)  - 
[Das Originalpaper von Satoshi Nakamoto](https://bitcoin.org/bitcoin.pdf) 

[Erster Einkauf mit Bitcoins](https://bitcointalk.org/index.php?topic=137.msg1195)

[Michael Nielsen: How the bitcoin protocol actually works](https://michaelnielsen.org/ddi/how-the-bitcoin-protocol-actually-works/) - Sehr gute und lesbare Beschreibung

[MIT Opencourseware - Blockchain and Money](https://ocw.mit.edu/courses/sloan-school-of-management/15-s12-blockchain-and-money-fall-2018/) - eine ganze MIT Vorlesung zum Thema

----
Youtube

[3Blue1Brown - But how does bitcoin actually work](https://www.youtube.com/watch?v=bBC-nXj3Ng4) - auf jeden Fall ansehen <br>

[How Bitcoin Works Under the Hood](https://www.youtube.com/watch?v=Lx9zgZCMqXE&t=261s) - mit weiteren technischen Details


------









