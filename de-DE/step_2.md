## Fragen entwerfen

Beginnen wir damit, zufällige Fragen zu erzeugen, die der Spieler beantworten soll.

\--- task \---

Erstelle ein neues Scratch-Projekt.

**Online:** öffne ein neues Online Scratch Projekt über [rpf.io/scratch-new](http://rpf.io/scratch-new){:target="_blank"}.

**Offline:** Öffne im Scratch Offline Editor ein neues Projekt.

Wenn du den Scratch Offline Editor herunterladen und installieren möchtest, findest du diesen unter [rpf.io/scratchoff](http://rpf.io/scratchoff){:target="_blank"}.

\--- /task \---

\--- task \--- Wähle eine Figur und einen Bühnenbild für dein Spiel. Du kannst selbst entscheiden welche dir gefallen! Hier ein Beispiel:

![Screenshot](images/brain-setting.png)

\--- /task \---

\--- task \--- Achte darauf, dass du deine Figur ausgewählt hast. Erstelle zwei neue Variablen mit der Bezeichnung `Zahl 1`{:class="block3variables"} und `Zahl 2`{:class="block3variables"}, um die Werte für deine Quizfragen zu speichern.

![Screenshot](images/giga-sprite.png) ![Screenshot](images/brain-variables.png)

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- task \--- Füge deiner Figur Code hinzu, damit beiden `Variablen`{:class="block3variables"} eine `Zufallszahl`{:class="block3operators"} zwischen 2 und 12 zugeordnet wird.

![Screenshot](images/giga-sprite.png)

```blocks3
Wenn die grüne Flagge angeklickt wird
setze [Zahl 1 v] auf (Zufallszahl von (2) bis (12))
setze [Zahl 2 v] auf (Zufallszahl von (2) bis (12))
```

\--- /task \---

\--- task \--- Stelle dem Spieler mit dem Block `frage und warte`{:class="block3sensing"} eine Frage die dieser beantworten soll. Mit dem Block `sage für 2 Sekunden`{:class="block3looks"} gibst du an, ob die Antwort richtig oder falsch war:

![Screenshot](images/giga-sprite.png)

```blocks3
Wenn die grüne Flagge angeklickt wird
setze [Zahl 1 v] auf (Zufallszahl von (2) bis (12))
setze [Zahl 2 v] auf (Zufallszahl von (2) bis (12))
frage (verbinde (Zahl 1)(verbinde [x] (Zahl 2))) und warte
falls <(Antwort) = ((Zahl 1)*(Zahl 2))> dann
sage [Genau! :)] für (2) Sekunden
+ sonst
+ sage [Nein :(] für (2) Sekunden
+ ende
```

\--- /task \---

\--- task \---

Überprüfe dein Projekt in dem du einmal die Frage richtig und einmal falsch beantwortest.

\--- /task \---

\--- task \---

Füge eine `wiederhole fortlaufend` Schleife um die bisherigen Blöcke, sodass dem Spieler eine Menge Fragen hintereinander gestellt werden.

\--- hints \--- \--- hint \---

Du musst einen `wiederhole fortlaufend`{:class="block3control"} Block hinzufügen, in dem der gesamten Code unterhalb der `wenn Fahne angeklickt wird`{:class="block3control"} eingehängt wird, so dass dieser Code fortlaufend wiederholt wird.

\--- /hint \--- \--- hint \--- Hier sind die Code Blöcke die du brauchst:

```blocks3
wiederhole fortlaufend
ende
```

\--- /hint \--- \--- hint \--- So sollte dein Code Block aussehen:

```blocks3
Wenn die grüne Flagge angeklickt wird

setze [Zahl 1 v] auf (Zufallszahl von (2) bis (12))
setze [Zahl 2 v] auf (Zufallszahl von (2) bis (12))
frage (verbinde (Zahl 1)(verbinde [x] (Zahl 2))) und warte
falls <(Antwort) = ((Zahl 1)*(Zahl 2))> dann
sage [Genau! :)] für (2) Sekunden
sonst
sage [Nein :(] für (2) Sekunden
ende
```

\--- /hint \--- \--- /hints \---

\--- /task \---