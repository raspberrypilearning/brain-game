## Grafiken hinzufügen

Im Moment sagt die Giga-Figur nur `Genau! :)` oder `nein :(` als Reaktion auf die Antworten des Spielers. Füge ein Paar Grafiken hinzu die zeigen, ob die Antwort richtig oder falsch ist.

--- task ---

Erstelle eine neue Figur namens "Ergebnis", die sowohl ein "grünes Häkchen" als auch ein "rotes Kreuz" Kostüm enthält.

![Figur mit Richtig und Falsch Kostüm](images/brain-result.png)

--- /task ---

--- task ---

Ändere den Code der Giga-Figur so, dass sie, anstatt etwas zum Spieler zu sagen, eine `Nachricht sendet`{:class="block3events"}, mit dem Inhalt "Richtig" oder "Falsch".

![Giga-Figur](images/giga-sprite.png)

```blocks3
if <(answer) = ((Zahl 1) * (Zahl 2))> then
- say [Genau! :)] for (2) seconds
+ broadcast (Richtig v)
else 
- say [Nein :(] for (2) seconds
+ broadcast (Falsch v)
end
```

--- /task ---

--- task ---

Du kannst nun diese Nachrichten verwenden, um zum entsprechenden Richtig oder Falsch `Kostüm zu wechseln`{:class="block3looks"}. Füge der Figur "Ergenbis" den folgenden Code hinzu:

![Ergebnis Figur](images/result-sprite.png)

```blocks3
when I receive [Richtig v]
switch costume to (Richtig v)
show
wait (1) seconds
hide

when I receive [Falsch v]
switch costume to (Falsch v)
show
wait (1) seconds
hide

when flag clicked
hide
```

--- /task ---

--- task ---

Teste dein Spiel erneut. Du solltest den grünen OK Haken sehen, wenn du eine Frage richtig beantwortest, und das rote Flasch Kreuz, wenn du falsch antwortest!

![Richtig für eine richtige, Falsch für eine falsche Antwort](images/brain-test-answer.png)

--- /task ---

Hast du bemerkt, dass die Codes für `Wenn ich Richtig empfange`{:class="blockevents"} und `Wenn ich Falsch empfange`{:class="blockevents"} nahezu identisch sind?

Damit du deinen Code einfacher ändern kannst, wirst du einen benutzerdefinierten Block erstellen.

--- task ---

Wählen die Figur "Ergebnis" aus. Anschließend klicke auf `Meine Blöcke`{:class="block3myblocks"}, und dann noch auf **Neuer Block**. Erstelle einen neuen Block und nenne ihn `animieren`{:class="block3myblocks"}.

![Ergebnis-Figur](images/result-sprite.png)

![Erstelle einen Block namens animiere](images/brain-animate-function.png)

--- /task ---

--- task ---

Verschiebe den Code `zeige dich`{:class="block3looks"} und `verstecke dich`{:class="block3looks"} aus der 'Ergebnis' Figur in den `animiere`{:class="block3myblocks"} Block:

![Ergebnis-Figur](images/result-sprite.png)

```blocks3
define animiere
show
wait (1) seconds
hide
```

--- /task ---

--- task ---

Stelle sicher, dass die `zeige dich`{:class="block3looks"} und `verstecke dich`{:class="block3look"} Blöcke unter **beiden** `wechsle zu Kostüm`{:class="block3looks"} Blöcken entfernt sind.

Füge anschließend den neuen `animiere`{:class="block3myblocks"} Block unter die beiden Blöcken `wechsle zu Kostüm`{:class="block3look"} hinzu. Dein Code sollte nun so aussehen:

![Ergebnis-Figur](images/result-sprite.png)

```blocks3
when I receive [Richtig v]
switch costume to (Richtig v)
animiere :: custom

when I receive [Falsch v]
switch costume to (Falsch v)
animiere :: custom
```

--- /task ---

Der Vorteil des benutzerdefinierten Block `animieren`{:class="block3myblocks"} ist, dass jede Änderung am Code nur noch einmal vorgenommen werden muss, wenn beispielsweise die 'Ergebnis' Figur länger oder kürzer angezeigt werden soll.

--- task ---

Ändere deinen Code so, dass die Kostüme 'Richtig' oder 'Falsch' für 2 Sekunden angezeigt werden.

--- /task ---

--- task ---

Anstatt das "Richtig" oder "Falsch" Kostüm `zeigen`{:class="block3looks"} und `verstecken`{:class="block3looks"}, kannst du den `animiere`{:class="block3myblocks"} Block ändern, so dass die Kostüme ein- und ausblenden.

![Ergebnis-Figur](images/result-sprite.png)

```blocks3
define animate
set [Durchsichtigkeit v] effect to (100)
show
repeat (25) 
  change [Durchsichtigkeit v] effect by (-4)
end
hide
```

--- /task ---

Kannst du die Animation der 'Richtig' oder 'Falsch'-Grafiken verbessern? Du kannst Code hinzufügen, um die Kostüme auch auszublenden, oder du kannst andere coole Effekte verwenden:

![Screenshot](images/brain-effects.png)