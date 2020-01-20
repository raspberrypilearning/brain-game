## Skapa frågor

Du ska börja med att skapa slumpmässiga frågor som spelaren måste svara på.

\--- uppgift \---

Öppna ett nytt Scratch-projekt.

**Online:** open a new online Scratch project at [rpf.io/scratch-new](http://rpf.io/scratch-new){:target="_blank"}.

**Offline:** Öppna ett nytt projekt i offline-editoren.

Om du behöver ladda ner och installera Scratch offline editoren kan du hitta den på [rpf.io/scratchoff](http://rpf.io/scratchoff){: target = "_ blank"}.

\--- / uppgift \---

\--- task \---

Add a character sprite and a backdrop for your game. You can choose any you like! Here's an example:

![screenshot](images/brain-setting.png)

\--- /task \---

\--- task \---

Make sure you have your character sprite selected. Create two new variables, called `number 1`{:class="block3variables"} and `number 2`{:class="block3variables"}, to store the numbers for the quiz questions.

![screenshot](images/giga-sprite.png)

![screenshot](images/brain-variables.png)

[[[generic-scratch3-add-variable]]]

\--- / uppgift \---

\--- task \---

Add code to your character sprite to set both of the `variables`{:class="block3variables"} to a `random`{:class="block3operators"} number between 2 and 12.

![screenshot](images/giga-sprite.png)

```blocks3
När flaggan klickade på
satt [nummer 1 v] till (välj slumpvis (2) till (12))
uppsättning [nummer 2 v] till (välj slumpvis (2) till (12))
```

\--- /task \---

\--- task \---

Add code to `ask`{:class="block3sensing"} the player for the answer, and then `say for 2 seconds`{:class="block3looks"} whether the answer was right or wrong:

![screenshot](images/giga-sprite.png)

```blocks3
När flaggan klickade på
satt [nummer 1 v] till (välj slumpvis (2) till (12))
uppsättning [nummer 2 v] till (välj slumpvis (2) till (12))

+ fråga (gå med i [x] (nummer 2))) och vänta
+ om <(svar) = ((nummer 1) * (nummer 2))> sedan
+ säg [ja! :)] för (2) sekunder
+ annat
+ säg [nej :(] för (2) sekunder
+ slut
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
för evigt
slut
```

\--- /hint \---

\--- hint \---

Here is what your code should look like:

```blocks3
när flaggan klickade

+ för alltid
    set [nummer 1 v] till (välj slumpvis (2) till (12))
    set [nummer 2 v] till (välj slumpvis (2) till (12))
    fråga 1) (gå med [x] (nummer 2))) och vänta
    om <(svar) = ((nummer 1) * (nummer 2))> då
        säga [ja! :)] för (2) sekunder
    annars
        säga [nej :(] för (2) sekunder
    slut
slut
```

\--- /hint \---

\--- /hints \---

\--- /task \---