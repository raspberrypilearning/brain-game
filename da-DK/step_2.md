## Lav spørgsmål

Du skal begynde med at oprette tilfældige spørgsmål, som spilleren skal svare på.

\--- task \---

Åbn et nyt Scratch-projekt.

**Online:** open a new online Scratch project at [rpf.io/scratch-new](http://rpf.io/scratch-new){:target="_blank"}.

**Offline:** Åbn et nyt projekt i offline-editoren.

Hvis du skal downloade og installere Scratch offline editoren, kan du finde den på [rpf.io/scratchoff](http://rpf.io/scratchoff){: target = "_ blank"}.

\--- /task \---

\--- task \---

Add a character sprite and a backdrop for your game. You can choose any you like! Here's an example:

![screenshot](images/brain-setting.png)

\--- /task \---

\--- task \---

Make sure you have your character sprite selected. Create two new variables, called `number 1`{:class="block3variables"} and `number 2`{:class="block3variables"}, to store the numbers for the quiz questions.

![screenshot](images/giga-sprite.png)

![screenshot](images/brain-variables.png)

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- task \---

Add code to your character sprite to set both of the `variables`{:class="block3variables"} to a `random`{:class="block3operators"} number between 2 and 12.

![screenshot](images/giga-sprite.png)

```blocks3
når flag klikket
sæt [nummer 1 v] til (vælg tilfældigt (2) til (12))
sæt [nummer 2 v] til (vælg tilfældigt (2) til (12))
```

\--- /task \---

\--- task \---

Add code to `ask`{:class="block3sensing"} the player for the answer, and then `say for 2 seconds`{:class="block3looks"} whether the answer was right or wrong:

![screenshot](images/giga-sprite.png)

```blocks3
når flag klikker
sæt [nummer 1 v] til (vælg tilfældigt (2) til (12))
sæt [nummer 2 v] til (vælg tilfældigt (2) til (12))

+ spørg (join [x] (nummer 2))) og vent
+ hvis <(svar) = ((nummer 1) * (nummer 2))> så
+ siger [ja! :)] for (2) sekunder
+ ellers
+ siger [nej :(] for (2) sekunder
+ ende
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
for evigt
ende
```

\--- /hint \---

\--- hint \---

Here is what your code should look like:

```blocks3
når flag klikker

+ for evigt
    sæt [nummer 1 v] til (vælg tilfældigt (2) til (12))
    sæt [nummer 2 v] til (vælg tilfældigt (2) til (12))
    spørg 1) (join [x] (nummer 2))) og vent
    hvis <(svar) = ((nummer 1) * (nummer 2))> så
        siger [ja! :)] for (2) sekunder
    andet
        siger [nej :(] for (2) sekunder
    ende
ende
```

\--- /hint \---

\--- /hints \---

\--- /task \---