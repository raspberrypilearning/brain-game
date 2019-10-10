## Mehrfach spielen

Jetzt wirst du eine Taste "Spielen" hinzufügen, damit der Spieler dein Spiel mehrmals spielen kann.

--- task --- Erstelle eine neue Figur - eine 'Spielen'-Taste, auf die der Spieler klicken muss, um ein neues Spiel zu starten.

Du kannst die Figur selbst zeichnen oder eine Figur aus der Bibliothek verwenden.

![Bild der Schaltfläche "Spielen"](images/brain-play.png)

--- /task ---

--- task --- Füge deiner Spielen Knopf Figur diesen Code hinzu:

![Taste-Figur](images/button-sprite.png)

```blocks3
    Wenn die grüne Flagge angeklickt wird
    zeige dich

    Wenn diese Figur angeklickt wird
    verstekce dich
    sende (Start v) an alle
```

--- /task ---

Der neue Code enthält einen weiteren `sende an alle`{:class="block3events"} Block, der die Nachricht 'Start' sendet.

Der neue Code zeigt die 'Spielen' Taste, nachdem der Spieler auf die grüne Flagge klickt. Wenn der Spieler auf die Figur Spielen klickt, versteckt sich diese Figur und sendet eine Nachricht an alle anderen Figuren, damit diese darauf reagieren können.

In dem Moment, in dem die Giga-Figur die Nachricht 'Start' empfängt, fängt sie an eine Frage zu stellen. Ändere den Code des Spiels, damit die Giga Figur beginnt Fragen zu stellen, wenn es die `gesendete Nachricht`{:class="block3events"} 'Start' empfängt.

--- task --- Wähle die Giga-Figur aus und ersetze den Code `Wenn die grüne Flagge angeklickt wird`{:class="block3events"} Block durch einen `wenn ich Start empfange`{:class="block3events"} Block.

![Giga-Figur](images/giga-sprite.png)

```blocks3
<br />- wenn die grüne Flagge angeklickt wird
+ Wenn ich [Start v] empfange
setze [Zahl 1 v] auf (Zufallszahlen von (2) bis (12))
setze [Zahl 2 v] auf (Zufallszahlen von (2) bis (12))
frage (verbinde (Zahl 1) und (verbinde [ x ] und (Zahl 2))) und warte
wenn <(Antwort) = ((Zahl 1)*(Zahl 2))> dann
    sage [Genau! :)] für (2) Sekunden
sonst
    sage [nein :(] für (2) Sekunden 
ende
```

--- /task ---

--- task ---

Um die Änderungen zu testen, klicke auf die grüne Flagge und anschließend auf die neue Taste "Spielen". Das Spiel sollte nicht starten, bevor man auf die Schaltfläche klickt.

--- /task ---

Siehst du, dass der Countdown sofort startet, wenn die grüne Flagge geklickt wird und nicht erst, wenn die Taste "Spielen" gedrückt wird?

![Countdown ist gestartet](images/brain-timer-bug.png)

--- task ---

Kannst du den Code für den Coutdown ändern, damit der Countdown erst beginnt, wenn der Spieler auf die "Spielen" Taste gedrückt hat?

--- /task ---

--- task --- Füge Code zu deiner Spielen-Knopf Figur hinzufügen, so dass die Schaltfläche am Ende jedes Spiels wieder angezeigt wird.

![Tasten-Figur](images/button-sprite.png)

```blocks3
    Wenn ich [Ende v] empfange
    zeige dich
```

--- /task ---

--- task ---

Teste die Taste 'Spielen', indem du ein paar Spiele spielst. Die Taste sollte am Ende jedes Spiels wieder angezeigt werden.

Um das Spiel schneller zu testen, kannst du den Wert der Variabel `Zeit`{:class="block3variables"} ändern, damit jedes Spiel nur ein paar Sekunden dauert.

![Bühne](images/stage-sprite.png)

```blocks3
    setze [Zeit v] auf [10]
```

--- /task ---

--- task --- Du kannst das Aussehen der "Spielen" Schaltfläche ändern, wenn sich der Mauszeiger darüber befindet.

![Taste](images/button-sprite.png)

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

![Screenshot](images/brain-fisheye.png) --- /task ---