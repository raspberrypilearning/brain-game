## Lag spørsmål

Du skal begynne med å lage tilfeldige spørsmål som spilleren må svare på.

\--- oppgave \---

Åpne et nytt Scratch-prosjekt.

**Online:** open a new online Scratch project at [rpf.io/scratch-new](http://rpf.io/scratch-new){:target="_blank"}.

**Frakoblet:** Åpne et nytt prosjekt i offline-editoren.

Hvis du trenger å laste ned og installere Scratch offline editoren, kan du finne den på [rpf.io/scratchoff](http://rpf.io/scratchoff){: target = "_ blank"}.

\--- / oppgave \---

\--- task \---

Add a character sprite and a backdrop for your game. You can choose any you like! Here's an example:

![screenshot](images/brain-setting.png)

\--- /task \---

\--- task \---

Make sure you have your character sprite selected. Create two new variables, called `number 1`{:class="block3variables"} and `number 2`{:class="block3variables"}, to store the numbers for the quiz questions.

![screenshot](images/giga-sprite.png)

![screenshot](images/brain-variables.png)

[[[generic-scratch3-add-variable]]]

\--- / oppgave \---

\--- task \---

Add code to your character sprite to set both of the `variables`{:class="block3variables"} to a `random`{:class="block3operators"} number between 2 and 12.

![screenshot](images/giga-sprite.png)

```blocks3
når flagget klikket
sett [nummer 1 v] til (velg tilfeldig (2) til (12))
sett [nummer 2 v] til (velg tilfeldig (2) til (12))
```

\--- /task \---

\--- task \---

Add code to `ask`{:class="block3sensing"} the player for the answer, and then `say for 2 seconds`{:class="block3looks"} whether the answer was right or wrong:

![screenshot](images/giga-sprite.png)

```blocks3
når flagget klikket
sett [nummer 1 v] til (velg tilfeldig (2) til (12))
sett [nummer 2 v] til (velg tilfeldig (2) til (12))

+ spør (bli med [x] (nummer 2))) og vent
+ hvis <(svar) = ((nummer 1) * (nummer 2))> så
+ si [ja! :)] for (2) sekunder
+ annet
+ si [nei :(] for (2) sekunder
+ slutt
```

\--- /task \---

\--- task \---

Test your project twice: answer one question correctly, and the other incorrectly.

\--- /task \---

\--- task \---

Add a `forever`{:class="block3control"} loop around this code, so that the game asks the player lots of questions in a row.

\--- hints \---

\--- hint \---

You need to add a `forever`{:class="block3control"} block, and put all of the code except the `when flag clicked`{:class="block3control"} block into it.

\--- /hint \---

\--- hint \---

Here is the block you need:

```blocks3
for alltid
ende
```

\--- /hint \---

\--- hint \---

Here is what your code should look like:

```blocks3
når flagget klikkte

+ for alltid
    sett [tall 1 v] til (velg tilfeldig (2) til (12))
    sett [nummer 2 v] til (velg tilfeldig (2) til (12))
    spør 1) (bli med [x] (nummer 2))) og vent
    hvis <(svar) = ((nummer 1) * (nummer 2))> så
        si [ja! :)] for (2) sekunder
    annet
        si [nei :(] for (2) sekunder
    ende
ende
```

\--- /hint \---

\--- /hints \---

\--- /task \---