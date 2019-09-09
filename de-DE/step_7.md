## Grafische Anzeigen hinzufügen

Im Moment sagt die Spieler-Figur nur `Genau! :)` oder `nein :(` als Reaktion auf die Antworten des Spielers. Füge ein Paar Grafiken hinzu, um den Spieler zu zeigen, ob seine Antwort richtig oder falsch ist.

\--- task \---

Erstelle eine neue Figur namens "Ergebnis", die sowohl ein "grünes Häkchen" als auch ein "rotes Kreuz" Kostüm enthält.

![Figur mit Richtig und Falsch Kostüm](images/brain-result.png)

\--- /task \---

\--- task \---

Ändere den Code deiner Spieler-Figur so ab, dass anstatt etwas zum Spieler zu sagen eine `Nachricht gesendet` {: class = "block3events"} wird, mit den Inhalten "Richtig" oder "Falsch".

![Spieler-Figur](images/giga-sprite.png)

```blocks3
falls <(answer) = ((Zahl 1)*(Zahl 2))> dann

- sage [Genau! :)] für (2) Sekunden
+ sende (Richtig v) an alle
sonst
- sage [nein :(] für (2) Sekunden
+ sende (Falsch v) an alle
ende
```

\--- /task \---

\--- task \---

Du kannst nun diese Nachrichten verwenden, um zum entsprechenden Richtig oder Falsch `Kostüm zu wechseln`{: class = "block3looks"}. Fügen der Figur "Ergenbis" den folgenden Code hinzu:

![Ergebnis Figur](images/result-sprite.png)

```blocks3
    wenn ich [Richtig v] empfange
    wechsle zu Kostüm (Richtig v)
    zeige dich
    warte (1) Sekunde
    verstecke dich

    wenn ich [Falsch v] empfange
    wechsle zu Kostüm (Falsch v)
    zeige dich
    warte (1) Sekunde
    verstecke dich

    wenn die grüne Flagge angeklickt wird
    verstecke dich
```

\--- /task \---

\--- task \--- Teste dein Spiel erneut. Du solltest den grünen OK Haken sehen, wenn du eine Frage richtig beantwortest, und das rote Flasch Kreuz, wenn du falsch antwortest!

![Richtig für richtige und Falsch für falsche Antwort](images/brain-test-answer.png)

\--- /task \---

Hast du bemerkt, dass der Code für die `Wenn ich Richtig empfange`{:class="blockevents"} und `Wenn ich Falsch empfange`{:class="blockevents"} Blöcke nahezu identisch ist?

Dafür gibt es benutzerdefinierten Blöcke, damit du deinen Code einfacher ändern kannst.

\--- task \---

Wählen die Figur "Ergebnis" aus. Anschließend klicke auf `Meine Blöcke`{:class="block3myblocks"}, und schließlich auf **Neuer Block** unter "Meine Blöcke". Erstelle einen neuen Block und nenne ihn `animieren`{:class="block3myblocks"}.

![Ergebnis-Figur](images/result-sprite.png)

![Erstelle einen Block namens animiere](images/brain-animate-function.png)

\--- /task \---

\--- task \--- Verschiebe den Code `zeige dich`{:class="block3looks"} und `verstecke dich`{:class="block3looks"} aus der 'Ergebnis' Figur in den `animire`{:class="block3myblocks"} Block:

![Ergebnis-Figur](images/result-sprite.png)

```blocks3
define animiere
ziege dich
warte (1) Sekunde
verstecke dich
```

\--- /task \---

\--- task \--- Stelle sicher, dass die `zeige dich`{:class="block3looks"} und `verstecke dich`{:class="block3look"} Blöcke in **beiden** `wechsle zu Kostüm`{:class="block3looks"} Blöcken entfernt sind.

Füge anschließend den neuen `animiere`{:class="block3myblocks"} Block unter die beiden Blöcken des `wechsle zu Kostüm`{:class="block3look"} Blocks hinzu. Dein Code sollte nun wie folgt aussehen:

![Ergebnis-Figur](images/result-sprite.png)

```blocks3
    wenn ich [Richtig v] empfange
    wechsle zu Kostüm (Richtig v)
    aminiere:: eigen

    wenn ich [Falsch v] empfange
    wechsle zu Kostüm (Falsch v)
    animiere:: eigen
```

\--- /task \---

Der Vorteil des benutzerdefinierten Block `animieren`{:class="block3myblocks"} ist, dass jede Änderung am Code nur noch einmal vorgenommen werden muss, wenn beispielsweise die 'Ergebnis' Figur länger oder kürzer anzeigen werden soll.

\--- task \---

Ändere deinen Code so, dass die Kostüme 'Richtig' oder 'Falsch' für 2 Sekunden angezeigt werden.

\--- /task \---

\--- task \--- Anstatt das "Richtig" oder "Falsch" Kostüm `zeigen` {: class = "block3looks"} und `verstecken` {: class = "block3looks"} zu lassen, kannst du den `animiere` {: class = "block3myblocks"} Block ändern, so dass sich die Kostüme ein- und ausblenden.

![Ergebnis-Figur](images/result-sprite.png)

```blocks3
    definiere animiere
    setze Effekt [Durchsichtigkeitv] auf (100)
    zeige dich
    wiederhiole (25) mal
        ändere Effekt [Durchsichtigkeit v] um (-4)
    ende
    vertecke dich
```

\--- /task \---

Kannst du die Animation der 'Richtig' oder 'Falsch'-Grafiken verbessern? Du kannst Code hinzufügen, um die Kostüme auch auszublenden, oder auch andere coole Effekte verwenden:

![Screenshot](images/brain-effects.png)