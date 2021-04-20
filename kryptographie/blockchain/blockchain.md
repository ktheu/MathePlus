https://demoblockchain.org/ 


https://btc.com/

Kontoinhaber: verfügen über Paar kryptographischer Schlüssel (öffentlich, privat)
Öffentliche Schlüssel sind die Kontonummern. Kontrolliert mit privatem Schlüssel das Konto
Wird gemacht: Privater Schlüssel ausdrucken und in Tresor legen (print a paper wallet for bitcoins)

Input = Output + Transaktionsgebühr

P2PK = Pay to Public Key - der Output wird direkt an den öffentlichen Schlüssel adressiert.
P2PKH = Pay to Public Key Hash - der Output wird an den Hash des öffentlichen Schlüssels geschickt (heute)

Alle Transaktionen müssen in einem fälschungssicheren Rechnungsbuch festgehalten werden.
Transaktionen werden an alle Teilnehmer im Netzwerk verteilt.
Teilnehmer sammeln diese in "Transaction Pools" und können diese (Teile davon, hohe Transaktionsgebühren werden bevorzugt).
zu Blöcken verschweißen. Teilnehmer, die Blöcke generieren, heißen "Miner". 
Die erste Transaktion schafft neue Bitcoins "aus dem Nichts"
als Belohnung für die vom Miner geleistete Arbeit.

Bitcoin-Block Aufbau: Merkle-Baum ist eine effiziente Methode zum Verifizieren von Transaktionen. Mit einem einzigen Hash, kann die Integrität aller Transaktionen geprüft werden. Die Blätter des Merkle Baumes - die Transaktionen - werden gehasht und die Zweige werden solange miteinander verhashed, bis es nur noch eine Wurzel gibt. 

Double Spends können nicht vollständig verhindert werden. Transaktion wird nicht direkt naWch der Aufnahme in einen Block als gültig anerkannt. Die Wahrscheinlichkeit, dass ein doublespend Angriff erfolgreich ist, sinkt mit der Zeit. Nach n=6 weiteren Blöcken, wird ein Block anerkannt.

So wie eine Transaktion nur valid ist, wenn es vom Sender signiert ist, so ist ein Block nur valid
wenn da ein proof of work ist.
Jeder Block hat den Hash des vorherigen Blocks in seinem Header, damit ist die Reihenfolge eindeutig. 
Jeder Block enthält zu Beginn noch einen Eintrag: den Block reward für die Mühe des proofs of work.
So entstehen neue Bitcoins (ohne Sender/Signatur

Die Miners hören auf Transaktions, die sie zu Blöcken zusammenfassen, die Anwender hören auf neue upgedatete Blockchains, die von den Miners kommen. Wenn man zwei widersprüchliche Blockchains empfängt, wählt man den, in den die meiste Arbeit gesteckt wurde (die Länge der Chains)

Die Anzahl der Nullen wird ab und zu gewechselt, so dass es im Schnitt 10 Minuten dauert, bis ein neuer
Block entstanden ist. Die Block rewards werden immer kleiner, es begann mit 50 BTC im Januar 2009
Alle 210000 Blöcke (ca. alle 4 Jahre) wird der reward halbiert.
210000(50 + 25 + 12.5 + 6.25 + ...) = 21,000,000
Die Miners leben dann nur von Transaction Fee. 
Jeder Block kann ca. 2400 Transaktionen enthalten. Deshalb ist es manchmal gut, ein incentive an die Miner zu geben, den eigenen Block zu verarbeiten. (VISA: 1700 Transaktionen pro Sekunde)
