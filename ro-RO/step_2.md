## Creează întrebări

Vei începe prin a crea întrebări aleatorii la care jucătorul trebuie să răspundă.

\--- task \---

Deschide un nou proiect Scratch.

**Online:** deschide un nou proiect Scratch la [rpf.io/scratch-new](http://rpf.io/scratch-new){:target="_blank"}.

**Offline:** deschide un nou proiect în editorul offline.

Dacă trebuie să descărci și să instalezi editorul offline Scratch, îl poți găsi la [rpf.io/scratchoff](http://rpf.io/scratchoff){: target = "_ blank"}.

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
când se dă clic pe steagul verde
setează [numărul 1 v] pentru a (alege aleatoriu (2) până la (12))
setează [numărul 2 v] pentru a (alege aleatoriu (2) până la (12))
```

\--- /task \---

\--- task \---

Add code to `ask`{:class="block3sensing"} the player for the answer, and then `say for 2 seconds`{:class="block3looks"} whether the answer was right or wrong:

![screenshot](images/giga-sprite.png)

```blocks3
când se dă click pe pictograma steag
setează [numărul 1 v] pentru a (alege aleatoriu (2) până la (12))
setează [numărul 2 v] pentru a (alege aleatoriu (2) până la (12))

+ cere (adaugă (numărul 1) (adaugă [x] (numărul 2))) și așteaptă 
+ dacă <(răspuns) = ((numărul 1) * (numărul 2))> apoi
+ spune [da! :)] pentru (2) secunde
+ altceva
+ spune [no :(] pentru (2) secunde
+ sfârșit
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
pentru totdeauna
sfârșit
```

\--- /hint \---

\--- hint \---

Here is what your code should look like:

```blocks3
când se dă click pe pictograma steag

setează [numărul 1 v] pentru a (alege aleatoriu (2) până la (12))
setează [numărul 2 v] pentru a (alege aleatoriu (2) până la (12))
+ intreabă (adaugă (numărul 1) (adaugă [x] (numărul 2))) și așteaptă 
+ dacă <(răspuns) = ((numărul 1) * (numărul 2))> apoi
+ spune [da! :)] pentru (2) secunde
    altceva
        spune [no :(] pentru (2) secunde
    sfârșit
sfârșit
```

\--- /hint \---

\--- /hints \---

\--- /task \---