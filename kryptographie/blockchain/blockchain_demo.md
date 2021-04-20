## Blockchain

[Kryptographische Hashfunktion](https://andersbrownworth.com/blockchain/hash)

Wir erweitern die Eingabe zu einem Block

[Block](https://andersbrownworth.com/blockchain/block)

Der Data-Teil ist jetzt in 3 Teile unterteilt und der Hash beginnt mit 4 Nullen. Weil der
Hash dieses Blocks mit 4 Nullen beginnt, nenne wir in valid oder signiert. Sobald man Daten
eingibt, ist der Block nicht mehr valid (rote Umrandung). Jetzt muss man die Nonce (Number used once)
so verändern, damit der Block wieder valid wird. Das ist das Mining.

Ein Blockchain ist eine Kette solcher Blöcke. Wie sind sie verkettet?

[Blockchain](https://andersbrownworth.com/blockchain/blockchain)

Jeder Block enthält den Hash des Vorgängers (außer dem ersten Genesis-Block)
Wenn wir die Daten eines Blocks verändern, machen wir auch alle Folge-Blocks invalid.
Je weiter in der Vergangenheit man eine Änderung macht, desto aufwendiger wird es, die
Kette wieder valid zu kriegen.

Damit man keine Bank benötigt, gibt es die Blockchain nicht nur einmal, sondern sie ist auf
viele Anwender verteilt:

[Verteilung](https://andersbrownworth.com/blockchain/distributed)

Wenn eine Blockchain irgendwo verändert wird, dann sieht man an den letzten Hashwerten der Mehrheit, 
dass da was nicht stimmt.

Im nächsten Schritt machen wir die Daten sinnvoller durch die Einführung von Tokens für Transaktionen.

[Tokens](https://andersbrownworth.com/blockchain/tokens)

Auch hier würden wir merken, wenn in der Vergangenheit ein Wert geändert wird. In der Blockchain wird
nicht notiert, wieviel jeder aktuell auf seinen Konto hat, sondern es werden nur Transaktionen vermerkt.
Wie stellt man fest, ob Darcy wirklich $25 hat? Um das festzustellen, benötigen wir noch Coinbase Transaktions.

[Coinbase](https://andersbrownworth.com/blockchain/coinbase)

Anders erhält $100 durch eine Coinbase-Transaktion erhalten und zahlt an andere Teilnehmer. Jetzt können wir zurückverfolgen, ob Jackson $2 an Alexa zahlen kann.

Es muss noch dafür gesorgt werden, dann die Transaktions-Einträge nicht von Unbefugten gemacht werden können.
(Mallory könnte sonst einen Eintrag einfügen, dass er $10 Dollar von Alice erhält).
Dazu nutzen wir:

[Public/Private Keys](https://andersbrownworth.com/blockchain/public-private-keys/keys)

Damit können wir Nachrichten signieren.

[Signatures](https://andersbrownworth.com/blockchain/public-private-keys/signatures)

Statt einer Nachricht können wir auch eine Transaktion signieren.

[Transaction](https://andersbrownworth.com/blockchain/public-private-keys/transaction)

Sender und Empfänger der Transaktion sind jetzt die public keys der Beteiligten.

Diese Technik verwenden wir jetzt in der Blockchain
[Blockchain](https://andersbrownworth.com/blockchain/public-private-keys/blockchain)

Jetzt sind in dem Block keinen Namen mehr, sondern nur noch public keys und Signaturen. Wenn jetzt ein Betrag
geändert wird, wird nicht nur der Block invalid, sondern auch die Signatur. Die Signatur ist auch durch mining
nicht zu reparieren.

Private/public key-Paare sind sehr leicht zu generieren. Viel einfacher, als ein Konto zu eröffnen.

------

[a](https://youtu.be/bBC-nXj3Ng4?t=613)

[Miners](https://youtu.be/bBC-nXj3Ng4?t=1039)







