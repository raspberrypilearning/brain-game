## Grafiken hinzufügen

Im Moment sagt die Giga-Figur nur `Genau! :)` oder `nein :(` als Reaktion auf die Antworten des Spielers. Füge ein Paar Grafiken hinzu die zeigen, ob die Antwort richtig oder falsch ist.

\--- task \---

Erstelle eine neue Figur namens "Ergebnis", die sowohl ein "grünes Häkchen" als auch ein "rotes Kreuz" Kostüm enthält.

![Figur mit Richtig und Falsch Kostüm](images/brain-result.png)

\--- /task \---

\--- task \---

Ändere den Code der Giga-Figur so, dass sie, anstatt etwas zum Spieler zu sagen, eine `Nachricht sendet` {: class = "block3events"}, mit dem Inhalt "Richtig" oder "Falsch".

![Giga-Figur](images/giga-sprite.png)

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

Du kannst nun diese Nachrichten verwenden, um zum entsprechenden Richtig oder Falsch `Kostüm zu wechseln`{: class = "block3looks"}. Füge der Figur "Ergenbis" den folgenden Code hinzu:

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

\--- task \---

Test your game again. You should see the tick whenever you answer a question correctly, and the cross whenever you answer incorrectly!

![Tick for correct, cross for wrong answer](images/brain-test-answer.png)

\--- /task \---

Can you see that the code for `when I receive correct`{:class="block3events"} and `when I receive wrong`{:class="block3events"} is nearly identical?

So you can change your code more easily, you are going to create a custom block.

\--- task \---

Select the 'Result' sprite. Then click on `My Blocks`{:class="block3myblocks"}, and then on **Make a Block**. Create a new block and call it `animate`{:class="block3myblocks"}.

![Result sprite](images/result-sprite.png)

![Create a block called animate](images/brain-animate-function.png)

\--- /task \---

\--- task \---

Move the code to `show`{:class="block3looks"} and `hide`{:class="block3looks"} the 'Result' sprite into the `animate`{:class="block3myblocks"} block:

![Result sprite](images/result-sprite.png)

```blocks3
define animiere
zeige dich
warte (1) Sekunde
verstecke dich
```

\--- /task \---

\--- task \---

Make sure you have removed the `show`{:class="block3looks"} and `hide`{:class="block3looks"} blocks below **both** of the `switch costume`{:class="block3looks"} blocks.

Then add the `animate`{:class="block3myblocks"} block below both of the `switch costume`{:class="block3looks"} blocks. Your code should now look like this:

![Result sprite](images/result-sprite.png)

```blocks3
    wenn ich [Richtig v] empfange
    wechsle zu Kostüm (Richtig v)
    aminiere:: eigen

    wenn ich [Falsch v] empfange
    wechsle zu Kostüm (Falsch v)
    animiere:: eigen
```

\--- /task \---

Because of the custom `animate`{:class="block3myblocks"} block, you now only need to make one change to your code if you want to show the 'Result' sprite's costumes a longer or shorter time.

\--- task \---

Change your code so that the 'tick' or 'cross' costumes display for 2 seconds.

\--- /task \---

\--- task \---

Instead of `showing`{:class="block3looks"} and `hiding`{:class="block3looks"} the 'tick' or 'cross' costumes, you could change your `animate`{:class="block3myblocks"} block so that the costumes fade in.

![Result sprite](images/result-sprite.png)

```blocks3
    definiere animiere
    setze Effekt [Durchsichtigkeit v] auf (100)
    zeige dich
    wiederhole (25) mal
        ändere Effekt [Durchsichtigkeit v] um (-4)
    ende
    verstecke dich
```

\--- /task \---

Can you improve the animation of the 'tick' or 'cross' graphics? You could add code to make the costumes fade out as well, or you could use other cool effects:

![screenshot](images/brain-effects.png)