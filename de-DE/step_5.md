## Mehrmals spielen

Jetzt wirst du eine Schaltfläche "Spielen" hinzufügen, damit der Spieler dein Spiel viele Male spielen kann.

\--- task \--- Erstelle eine neue 'Spielen' Knopf Figur, auf den der Spieler klicken muss, um ein neues Spiel zu starten.

Du kannst die Figur selbst zeichnen oder eine Figur aus der Bibliothek verwenden.

![Bild der Schaltfläche "Spielen"](images/brain-play.png)

\--- /task \---

\--- task \--- Füge deiner Spielen Knopf Figur diesen Code hinzu:

![Spielen Figur](images/button-sprite.png)

```blocks3
    Wenn die grüne Flagge angeklickt wird
    zeige dich

    Wenn diese Figur angeklickt wird
    verstekce dich
    sende (Start v) an alle
```

\--- /task \---

Der neue Code enthält einen weiteren `sende an alle`{:class="block3events"} Block, der die Nachricht 'Start' sendet.

Der neue Code zeigt den 'Spielen' Knopf, wenn der Spieler auf die grüne Flagge klickt. Wenn der Spieler auf die Spielen Knopf Figur klickt, versteckt sich diese Figur und sendet eine Nachricht an alle anderen Figuren, damit diese darauf reagieren können.

In dem Moment, in dem die Spiel-Figur die Nachricht 'Start' empfängt, fängt sie an eine Frage zu stellen. Ändere den Code des Spiels, damit die Spiel Figur beginnt Fragen zu stellen, `wenn ich Nachricht empfange`{:class="block3events"} 'Start'.

\--- task \--- Wähle deine Spiel-Figur aus und ersetzen den Code `Wenn die grüne Flagge angeklickt wird` {: class = "block3events"} Block durch einen `wenn ich Start empfange` {: class = "block3events"} Block.

![Spieler Figur](images/giga-sprite.png)

```blocks3
<br />- wenn die grüne Flagge angeklickt wird
+ Wenn ich [Start v] empfange
setze [Zahl 1 v] auf (Zufallszahlen von (2) bis (12))
setze [Zahl 2 v] auf (Zufallszahlen von (2) bis (12))
frage (verbinde (Zahl 1) und (verbinde [ x ] und (Zahl 2))) und warte
wenn &lt;(Antwort) = ((Zahl 1)*(Zahl 2))&gt; dann
    sage [Genau! :)] für (2) Sekunden
sonst
    sage [nein :(] für (2) Sekunden 
ende
```

\--- /task \---

\--- task \---

Um die Änderungen zu testen, klicke auf die grüne Flagge und anschließend auf die neue Schaltfläche "Spielen". Das Spiel sollte nicht nicht startet, bevor auf die Schaltfläche klickt wird.

\--- /task \---

Siehst du, dass der Countdown sofort startet, wenn die grüne Flagge geklickt wird und nicht erst, wenn die Schaltfläche "Spielen" gerückt wird?

![Countdown hat gestartet](images/brain-timer-bug.png)

\--- task \---

Kannst du den Code für den Coutdown ändern, damit der Countdown erst beginnt, wenn der Spieler auf den "Spielen" Knopf gedrückt hat?

\--- /task \---

\--- task \--- Füge Code zu deiner Spielen-Knopf Figur hinzufügen, so dass die Schaltfläche am Ende jedes Spiels wieder angezeigt wird.

![Spielen Figur](images/button-sprite.png)

```blocks3
    Wenn ich [Ende v] empfange
    zeige dich
```

\--- /task \---

\--- task \---

Teste den 'Spielen'-Knopf, indem du ein paar Spiele spielst. Der Knopf sollte am Ende jedes Spiels wieder angezeigt werden.

Um das Spiel schneller testen zu können, kannst du den Wert der Variablen `Zeit`{:class="block3variables" ändern, damit jedes Spiel nur ein paar Sekunden lang ist.

![Bühne](images/stage-sprite.png)

```blocks3
    setze [Zeit v] auf [10]
```

\--- /task \---

\--- task \--- Du kannst das Aussehen der "Spielen" Schaltfläche ändern, wenn sich der Mauszeiger darüber befindet.

![Schaltfäche](images/button-sprite.png)

```blocks3
    Wenn die grüne Flagge angeklickt wird
    zeige dich 
    wiederhole fortlaufend
    falls <touching (mouse-pointer v)?> dann
        setze Effekt [Fischauge v] auf (30)
    sonst
        setze Effekt [Fischauge v] auf (0)
    ende
    ende
```

![Screenshot](images/brain-fisheye.png) \--- /task \---