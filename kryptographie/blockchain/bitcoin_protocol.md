## Bitcoin Protocol

[Quelle](https://michaelnielsen.org/ddi/how-the-bitcoin-protocol-actually-works/)

Digitale Währung scheint unmöglich: wenn Alice einen String von Bits als Geld benutzen kann, wer soll sie
daran hindern, diesen String zu kopieren? (Problem 1)

Selbst wenn das gelöst ist: wie verhindern wir, dass jemand anderes diesen Bitstring nachmacht und ihn statt Alice benutzt? (Problem 2)

#### Infocoin

Infocoin soll ein erster Entwurf für eine digitale Währung sein. Nehmen wir an, wir hätten das Problem 2 irgendwie gelöst. 

Alice Bob 1 Infocoin geben: Sie schreibt den Text: Ich, Alice, gebe Bob einen infocoin. Sie signiert diesen Text mit ihrem privaten key und sendet ihn an die Welt.

Jeder kann Alice public key nutzen, um zu verifizieren, dass Alice Bob einen infocoin gegeben hat.

Damit ist sichergestellt, dass Alice wirklich behauptet hat, dass sie an Bob einen infocoin gegeben hat.

Kein anderer als Alice konnte so eine Nachricht erstellen. Aber jeder könnte die Nachricht kopieren, nachdem
Alice die Nachricht veröffentlicht hat.

Ein infocoin besteht also aus dieser signierten Nachricht.

Damit eine signierte Nachricht nicht mehrfach verwendet werden kann, könnte man die Nachricht um eine 
Seriennummer (serial number) für die infocoins erweitern. Die Nachricht würde jetzt lauten:

Ich, Alice, gebe Bob einen infocoin mit serial number 8740348.

To make this scheme work we need a trusted source of serial numbers for the infocoins. One way to create such a source is to introduce a bank. This bank would provide serial numbers for infocoins, keep track of who has which infocoins, and verify that transactions really are legitimate.

In more detail, let’s suppose Alice goes into the bank, and says “I want to withdraw one infocoin from my account”. The bank reduces her account balance by one infocoin, and assigns her a new, never-before used serial number, let’s say 1234567. Then, when Alice wants to transfer her infocoin to Bob, she signs the message “I, Alice, am giving Bob one infocoin, with serial number 1234567”. But Bob doesn’t just accept the infocoin. Instead, he contacts the bank, and verifies that: (a) the infocoin with that serial number belongs to Alice; and (b) Alice hasn’t already spent the infocoin. If both those things are true, then Bob tells the bank he wants to accept the infocoin, and the bank updates their records to show that the infocoin with that serial number is now in Bob’s possession, and no longer belongs to Alice.

Sowas wäre möglich. Aber man möchte ohne Bank auskommen.

Alle sind die Bank - jeder 

 In Bitcoin proper, a transaction is not considered confirmed until: (1) it is part of a block in the longest fork, and (2) at least 5 blocks follow it in the longest fork. In this case we say that the transaction has “6 confirmations”. 

An important variant on double spending is if Alice = Bob, i.e., Alice tries to spend a coin with Charlie which she is also “spending” with herself (i.e., giving back to herself). This sounds like it ought to be easy to detect and deal with, but, of course, it’s easy on a network to set up multiple identities associated with the same person or organization, so this possibility needs to be considered. In this case, Alice’s strategy is to wait until Charlie accepts the infocoin, which happens after the transaction has been confirmed 6 times in the longest chain. She will then attempt to fork the chain before the transaction with Charlie, adding a block which includes a transaction in which she pays herself:



Unfortunately for Alice, it’s now very difficult for her to catch up with the longer fork. Other miners won’t want to help her out, since they’ll be working on the longer fork. And unless Alice is able to solve the proof-of-work at least as fast as everyone else in the network combined – roughly, that means controlling more than fifty percent of the computing power – then she will just keep falling further and further behind

We can, for example, imagine a scenario in which Alice controls one percent of the computing power, but happens to get lucky and finds six extra blocks in a row, before the rest of the network has found any extra blocks. In this case, she might be able to get ahead, and get control of the block chain. But this particular event will occur with probability 1/100^6 = 10^{-12}. A more general analysis along these lines shows that Alice’s probability of ever catching up is infinitesimal, unless she is able to solve proof-of-work puzzles at a rate approaching all other miners combined.

Of course, this is not a rigorous security analysis showing that Alice cannot double spend. It’s merely an informal plausibility argument. The original paper introducing Bitcoin did not, in fact, contain a rigorous security analysis, only informal arguments along the lines I’ve presented here. The security community is still analysing Bitcoin, and trying to understand possible vulnerabilities. You can see some of this research listed here, and I mention a few related problems in the “Problems for the author” below. At this point I think it’s fair to say that the jury is still out on how secure Bitcoin is.

I believe have the answer to your third question.

The raw block data that each miner is trying to solve contains a generation transaction. That transaction is where their coins are sent if they solve that block. Because miners competing against each other want their coins to be sent to different addresses, and those addresses are hashed together with their nonce, it does not matter if everyone starts their nonce from zero. The added randomness from differing generation transaction addresses prevents each miner from working in the same space as others.

