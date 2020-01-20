## Création des questions

Tu vas commencer par créer des questions aléatoires auxquelles le joueur doit répondre.

\--- task \---

Ouvre un nouveau projet Scratch.

**En ligne:** ouvre un nouveau projet Scratch en ligne sur [rpf.io/scratch-new](http://rpf.io/scratch-new) {:target="_blank"}.

**Hors ligne:** ouvre un nouveau projet dans l'éditeur hors ligne.

Si tu dois télécharger et installer l'éditeur hors ligne Scratch, tu peux le trouver à [rpf.io/scratchoff](http://rpf.io/scratchoff){:target="_blank"}.

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
lorsque le drapeau est cliqué
définir [numéro 1 v] sur (choisir au hasard (2) sur (12))
définir [numéro 2 v] sur (choisir au hasard (2) à (12))
```

\--- /task \---

\--- task \---

Add code to `ask`{:class="block3sensing"} the player for the answer, and then `say for 2 seconds`{:class="block3looks"} whether the answer was right or wrong:

![screenshot](images/giga-sprite.png)

```blocks3
lorsque le drapeau est cliqué 
définir [numéro 1 v] sur (choisir au hasard (2) à (12))
définir [numéro 2 v] sur (choisir au hasard (2) à (12))

+ demander (rejoindre (numéro 1) (rejoindre [x] (numéro 2))) et attendre
+ si <(réponse) = ((numéro 1) * (numéro 2))> alors
+ dire [oui!] :)] pendant (2) secondes
+ sinon
+ dire [non :(] pendant (2) secondes
+ fin
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
répéter indéfiniment
fin
```

\--- /hint \---

\--- hint \---

Here is what your code should look like:

```blocks3
lorsque le drapeau est cliqué

+ répéter indéfiniment
    définir [numéro 1 v] sur (choisir au hasard (2) à (12))
    définir [numéro 2 v] sur (choisir au hasard (2) à (12))
    demander (rejoindre (numéro 1)(rejoindre [x] (numéro 2))) et attendre
    si <(réponse) = ((numéro 1) * (numéro 2))> alors
        dire [oui!] :)] pendant (2) secondes
    sinon
        dire [non :(] pendant (2) secondes
    fin
fin
```

\--- /hint \---

\--- /hints \---

\--- /task \---