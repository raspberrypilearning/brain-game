## Fragen zusammenstellen

Du beginnst damit, zufällige Aufgaben zu erzeugen, die der Spieler beantworten soll.

\--- task \---

Erstelle ein neues Scratch-Projekt.

**Online:** open a new online Scratch project at [rpf.io/scratch-new](http://rpf.io/scratch-new){:target="_blank"}.

**Offline:** Erstelle im Offline-Editor ein neues Projekt.

Wenn du den Scratch-Offline-Editor herunterladen und installieren möchtest, findest du diesen unter [rpf.io/scratchoff](http://rpf.io/scratchoff){:target="_blank"}.

\--- /task \---

\--- task \--- Füge in dein Spiel eine Spielfigur und einen Hintergrund ein. Du kannst frei wählen! Hier ein Beispiel:

![Screenshot](images/brain-setting.png)

\--- /task \---

\--- task \--- Achte darauf, dass du deine Spielfigur ausgewählt hast. Erstelle zwei neue Variablen mit der Bezeichnung `Zahl 1`{:class="block3variables"} und `Zahl 2`{:class="block3variables"}, um die Zahlen für deine Quizfragen zu speichern.

![screenshot](images/giga-sprite.png) ![Screenshot](images/brain-variables.png)

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- task \--- Füge deiner Spielfigur Programmblöcke hinzu, damit du beiden `Variablen`{:class="block3variables"} eine `Zufallszahl`{:class="block3operators"} zwischen 2 und 12 zuordnen kannst.

![Screenshot](images/giga-sprite.png)

```blocks3
Wenn die grüne Flagge angeklickt
setze [Zahl 1 v] auf (Zufallszahl von (2) bis (12))
setze [Zahl 2 v] auf (Zufallszahl von (2) bis (12))
```

\--- /task \---

\--- task \--- Stelle dem Spieler mit dem Programmblock`frage`{:class="block3sensing"} eine Frage die dieser beantworten soll. Mit dem Programmblock `sage für 2 Sekunden`{:class="block3looks"} gibst du an, ob die Antwort richtig oder falsch war:

![Screenshot](images/giga-sprite.png)

```blocks3
when flag clicked
set [number 1 v] to (pick random (2) to (12))
set [number 2 v] to (pick random (2) to (12))

+ ask (join (number 1)(join [ x ] (number 2))) and wait
+ if <(answer) = ((number 1)*(number 2))> then
+ say [yes! :)] for (2) seconds
+ else
+ say [no :(] for (2) seconds
+ end
```

\--- /task \---

\--- task \---

Überprüfe dein Projekt indem du einmal die Frage richtig und einmal falsch beantwortest.

\--- /task \---

\--- task \---

Füge eine `wiederhole fortlaufend` Schleife um die bisherigen Blöcke, sodass dem Spieler eine Menge Fragen hintereinander gestellt werden.

\--- hints \--- \--- hint \---

Du musst einen `wiederhole fortlaufend`{:class="block3control"} Programmblock hinzufügen und den gesamten Code außer `wenn Fahne angeklickt wird`{:class="block3control"} in diese Schleife geben.

\--- /hint \--- \--- hint \--- Here is the block you need:

```blocks3
forever
end
```

\--- /hint \--- \--- hint \--- So sollte dein Programmiercode aussehen:

```blocks3
when flag clicked

+ forever
    set [number 1 v] to (pick random (2) to (12))
    set [number 2 v] to (pick random (2) to (12))
    ask (join (number 1)(join [ x ] (number 2))) and wait
    if <(answer) = ((number 1)*(number 2))> then
        say [yes! :)] for (2) seconds
    else
        say [no :(] for (2) seconds
    end
end
```

\--- /hint \--- \--- /hints \---

\--- /task \---