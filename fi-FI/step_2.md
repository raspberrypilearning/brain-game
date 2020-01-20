## Luo kysymyksiä

Aloitatte luomalla satunnaisia kysymyksiä, jotka pelaajan on vastattava.

\--- tehtävä \---

Avaa uusi Scratch-projekti.

**Online:** open a new online Scratch project at [rpf.io/scratch-new](http://rpf.io/scratch-new){:target="_blank"}.

**Offline:** avaa uuden projektin offline-editorissa.

Jos haluat ladata ja asentaa Scratch offline -editorin, löydät sen osoitteesta [rpf.io/scratchoff](http://rpf.io/scratchoff){: target = "_ blank"}.

\--- / tehtävä \---

\--- task \---

Add a character sprite and a backdrop for your game. You can choose any you like! Here's an example:

![screenshot](images/brain-setting.png)

\--- /task \---

\--- task \---

Make sure you have your character sprite selected. Create two new variables, called `number 1`{:class="block3variables"} and `number 2`{:class="block3variables"}, to store the numbers for the quiz questions.

![screenshot](images/giga-sprite.png)

![screenshot](images/brain-variables.png)

[[[generic-scratch3-add-variable]]]

\--- / tehtävä \---

\--- task \---

Add code to your character sprite to set both of the `variables`{:class="block3variables"} to a `random`{:class="block3operators"} number between 2 and 12.

![screenshot](images/giga-sprite.png)

```blocks3
kun lippu napsautti
asettaa [numero 1 v] (valitse satunnainen (2) - (12))
aseta [numero 2 v] (valitse satunnainen (2) - (12))
```

\--- /task \---

\--- task \---

Add code to `ask`{:class="block3sensing"} the player for the answer, and then `say for 2 seconds`{:class="block3looks"} whether the answer was right or wrong:

![screenshot](images/giga-sprite.png)

```blocks3
kun lippu napsautti
asettaa [numero 1 v] (valitse satunnainen (2) - (12))
aseta [numero 2 v] (valitse satunnainen (2) - (12))

+ kysy (liity (numero 1)) (liity [x] (numero 2))) ja odota
+, jos <(vastaus) = ((numero 1) * (numero 2))> sitten
+ sanoa [kyllä! :)] (2) sekunnille
+ muuta
+ sanoa [no :(] (2) sekunnille
+ loppuun
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
ikuisesti
loppuun
```

\--- /hint \---

\--- hint \---

Here is what your code should look like:

```blocks3
kun lippu napsautti

+ ikuisesti
    aseta [numero 1 v] (valitse satunnainen (2) - (12))
    aseta [numero 2 v] (valitse satunnainen (2) - (12))
    kysy (liity 1) (liity [x] (numero 2))) ja odota
    jos <(vastaus) = ((numero 1) * (numero 2))> sitten
        sanoa [kyllä! :)] (2) sekunnin ajan
    muu
        sanoa [no :(] (2) sekunnin
    pään
loppuun
```

\--- /hint \---

\--- /hints \---

\--- /task \---