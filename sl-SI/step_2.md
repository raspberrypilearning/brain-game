## Ustvari vprašanja

Začni z ustvarjanjem naključnih vprašanj, na katera mora igralec odgovoriti.

\--- task \---

Ustvari nov Scratch projekt.

**S povezavo:** odpri nov spletni Scratch projekt na [rpf.io/scratch-new](http://rpf.io/scratch-new){:target="_blank"}.

**Brez povezave:** odprite nov projekt v namiznem Scratch urejevalniku.

Če želiš prenesti in namestiti Namizni Scratch, ga lahko najdeš na [rpf.io/scratchoff](http://rpf.io/scratchoff){: target = "_ blank"}.

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
ko kliknemo na zastavico
nastavi [število 1 v] na (naključno število (2) in (12))
nastavi [število 2 v] na (naključno število (2) in (12))
```

\--- /task \---

\--- task \---

Add code to `ask`{:class="block3sensing"} the player for the answer, and then `say for 2 seconds`{:class="block3looks"} whether the answer was right or wrong:

![screenshot](images/giga-sprite.png)

```blocks3
ko kliknemo na zastavico
nastavi [število 1 v] na (naključno število (2) in (12))
nastavi [število 2 v] na (naključno število (2) in (12))

+ vprašaj (združi(število1)(združi[ x ] (število 2))) in počakaj
+ če <(odgovor) = ((število 1)*(število 2))> potem
+ reci [da! :)] za (2) sekund
+ sicer
+ reci [ne :(] za (2) sekund
+ konec
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
ponavljaj
konec
```

\--- /hint \---

\--- hint \---

Here is what your code should look like:

```blocks3
ko kliknemo na zastavico

+ ponavljaj
  nastavi [število 1 v] na (naključno število (2) in (12))
  nastavi [število 2 v] na (naključno število (2) in (12))
  vprašaj (združi(število1)(združi[ x ] (število 2))) in počakaj
  če <(odgovor) = ((število 1)*(število 2))> potem
    reci [da! :)] za (2) sekund
  sicer
    reci [ne :(] za (2) sekund
konec
```

\--- /hint \---

\--- /hints \---

\--- /task \---