## Kérdések létrehozása

Először véletlenszerű kérdéseket hoz létre, amelyeket a játékosnak meg kell válaszolnia.

\--- feladat \---

Nyisson meg egy új Scratch projektet.

**Online:** open a new online Scratch project at [rpf.io/scratch-new](http://rpf.io/scratch-new){:target="_blank"}.

**Offline:** új projektet nyit meg az offline szerkesztőben.

Ha le kell töltenie és telepítenie kell a Scratch offline szerkesztőt, akkor azt [rpf.io/scratchoff](http://rpf.io/scratchoff){: target = "_ blank"} címen találja meg.

\--- / feladat \---

\--- task \---

Add a character sprite and a backdrop for your game. You can choose any you like! Here's an example:

![screenshot](images/brain-setting.png)

\--- /task \---

\--- task \---

Make sure you have your character sprite selected. Create two new variables, called `number 1`{:class="block3variables"} and `number 2`{:class="block3variables"}, to store the numbers for the quiz questions.

![screenshot](images/giga-sprite.png)

![screenshot](images/brain-variables.png)

[[[generic-scratch3-add-variable]]]

\--- / feladat \---

\--- task \---

Add code to your character sprite to set both of the `variables`{:class="block3variables"} to a `random`{:class="block3operators"} number between 2 and 12.

![screenshot](images/giga-sprite.png)

```blocks3
amikor a zászló a
kattint, a [szám 1 v] -ra állította (véletlenszerűen (2) - (12))
állítsa be a [2-es szám] -t (válassza ki a véletlenszerű (2) - (12) -et)
```

\--- /task \---

\--- task \---

Add code to `ask`{:class="block3sensing"} the player for the answer, and then `say for 2 seconds`{:class="block3looks"} whether the answer was right or wrong:

![screenshot](images/giga-sprite.png)

```blocks3
amikor a jelző
kattint, a [szám 1 v] -ra állította (véletlenszerűen (2) - (12))
állítsa be a [2-es szám] -t (véletlenszerű (2) -ig (12))

+ kérje (csatlakozzon (1. szám)) (csatlakozzon az [x] -hez (2-es szám))) és várjon
+, ha <(válasz) = ((1-es szám) * (2. szám))> majd
+ mondja [igen! :)] (2) másodpercig
+
+ mondjuk [nem :(] (2) másodpercig
+ vége
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
örökre
vég
```

\--- /hint \---

\--- hint \---

Here is what your code should look like:

```blocks3
amikor a jelző

+ örökre
    állított be [1-es szám] -ra (véletlenszerű (2) -ig (12))
    állítsa be a [2-es számot] a (véletlenszerű (2) -ig (12))
    kérjen (csatlakozzon (szám) 1) (csatlakozzon az [x] -hez (2-es szám))) és várjon
    ha <(válasz) = ((1-es szám) * (2. szám))> majd
        mondja [igen! :)] (2) másodpercig
    más
        mondjuk [no :(] (2) másodperc
    vég
végére
```

\--- /hint \---

\--- /hints \---

\--- /task \---