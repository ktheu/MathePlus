## Sicheres Email 

Download [Gpg4Win](https://www.gpg4win.de/index-de.html). <br>

Wir wählen eine möglichst schmale Installation, d.h. keine Integration in Outlook und keine
Integration in den Explorer, nur das Basisprogramm (GnuPG) und die Benutzeroberfläche (Kleopatra).

<img src='bild1.png' width="500">

---

Nach der Installation Kleopatra starten. Auf der Willkommenseite *Neues Schlüsselpaar* wählen, dann
Name und Email eintragen, *Passphrase* (= Passwort) ankreuzen und auf *erstellen* klicken.

<img src='bild14.png' width="500">

Die Passphrase dient zur Sicherung des Schlüssels auf dem lokalen PC und spielt für die eigentliche Verschlüsselung
der Nachrichten keine Rolle. Sie soll verhindern, dass Unbefugte, die Zugang zum PC (und damit über Gpg4Win zum privaten Schlüssel) erhalten, Nachrichten entschlüsseln können.

Nach der Schlüsselgenerierung auf *Abschließen*  klicken. 


---

### Den öffentlichen Schlüssel an den Kommunikationspartner schicken

Den Schlüssel anklicken und *exportieren* wählen.

<img src='bild15.png' width="700">


Die erzeugte Datei enthält den öffentlichen Schlüssel, das Wort *public* kommt im Dateinamen vor, z.B: *name_0xFE3EA1A0_public.asc*. Diese Datei mit normalem email als Dateianhang an die Kommunikationspartner verschicken (bleibt manchmal leider im Spam-Filter hängen) oder an geeigneter Stelle zum Download zur Verfügung stellen (z.B. in einem Teams-Raum).


----



### Import des öffentlichen Schlüssel des Kommunikationspartners

Wir erhalten von Malte eine email, in der er uns seinen öffentlichen Schlüssel in Form eines Dateianhangs zuschickt: *Malte Riedberg_0x00D0788A_public.asc*. Wir klicken auf importieren und wählen die erhaltene Datei.

<img src='bild16.png' width="700">


----

 Wir können zunächst nicht sicher sein, dass diese email wirklich von Malte stammt oder vielleicht unterwegs verändert wurde. Deswegen erscheint der Hinweis, dass der öffentliche Schlüssel, den wir erhalten haben, beglaubigt werden muss (seine Authentizität muss sicher gestellt sein). Wir machen das in einem späteren Schritt und klicken hier auf *nein*. Der Schlüssel von Malte erscheint in der Übersicht als *nicht beglaubigt*.


----

### Beglaubigung des öffentlichen Schlüssel des Kommunikationspartners

 Da wir Malte (und seine Stimme) kennen, lassen wir uns von ihm bei einer MS-Teams Sitzung (oder per Telefon) den Fingerprint seines öffentlichen Schlüssels vorlesen. 
 Wir selektieren den Schlüssel von Malte, dann rechter Mausklick und *Details* wählen:

 Malte liest die ersten 8 und die letzten 8 Zeichen des Fingerprints seines öffentlichen Schlüssels vor. Wenn diese Zeichen mit denen übereinstimmen, die wir beim Fingerprint sehen, können wir sicher sein, dass der öffentliche Schlüssel von Malte während des email-Transports nicht verändert wurde.
und klicken auf *Beglaubigen* (wir benötigen dazu unsere Passphrase).

 <img src='bild17.png' width="600">

 ----

 ### Eine verschlüsselte email an den Kommunikationspartner schicken 

 Da wir bei der Installation keine Integration mit z.B Outlook gewählt haben, können wir  verschlüsselte Dateien nur als Anhang verschicken. Wir können den zu verschlüsselnden Text also nicht direkt in Outlook eingeben, sondern schreiben ihn in ein Word-Dokument oder eine einfache Textdatei. 

 Wir wählen Maltes Schlüssel, klicken auf *Signieren/Verschlüsseln* und wählen die Datei aus, die wir verschlüsseln wollen. In dem dann erscheinenden Fenster *Dateien signieren/verschlüsseln* wählen wir *Für andere verschlüsseln* und selektieren dort Maltes öffentlichen Schlüssel. 
 Wenn wir *Für mich verschlüsseln* selektiert lassen, können außer Malte auch wir die Nachricht wieder entschlüsseln. Ganz unten steht der Name der Ausgabedatei vom Typ *gpg*. 
 Wir klicken auf *Signieren/Verschlüsseln*. 

 <img src='bild18.png' width="401">

 Die verschlüsselte Datei können wir jetzt als Anhang mit einem normalen email verschicken. 

 ---

 ### Eine erhaltene Datei entschlüsseln

 Wir klicken auf  *Entschlüsseln/Überprüfen* und wählen die zu entschlüsselnde gpg-Datei.

Die erhaltene Datei enthält nicht nur die verschlüsselte Nachricht, sondern auch die Signatur des Senders. Um diese zu überprüfen, muss der Empfänger den öffentlichen Schlüssel des Senders importiert haben. Damit wird sichergestellt, dass die Nachricht wirklich vom Sender kommt. 
Wenn der Empfänger auf diese Sicherheit verzichten kann, kann er die Entschlüsselung auch ohne den öffentlichen Schlüssel des Senders durchführen. 
Es kommt dann eine Warnung, aber die Entschlüsselung funktioniert trotzdem.

---


### Öffentlichen Schlüssel ansehen

Wenn wir in der Kleopatra-Übersicht auf unsere Benutzerkennung klicken und dann Exportieren wählen, sehen wir den öffentlichen Schlüssel.

 <img src='bild19.png' width="400">


 Der öffentliche Schlüssel für die email-Adresse khtheuer@stiftsgymnasium.de zum Download ist 
 [hier](./Karlheinz-Theuer-0xFE3EA1A0-public.asc)
 
 -----

 Für MacOS kann die [GPGSuite](https://gpgtools.org/) verwendet werden.





 