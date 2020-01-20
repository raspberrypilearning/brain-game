## Crea preguntes

Començaràs creant preguntes aleatòries que el jugador ha de respondre.

\--- tasca \---

Obriu un nou projecte Scratch.

**Online:** open a new online Scratch project at [rpf.io/scratch-new](http://rpf.io/scratch-new){:target="_blank"}.

**Desconnectat:** obre un nou projecte a l'editor fora de línia.

Si necessiteu descarregar i instal·lar l'editor Scratch offline, podeu trobar-lo a [rpf.io/scratchoff](http://rpf.io/scratchoff){: target = "_ blank"}.

\--- / tasca \---

\--- task \---

Add a character sprite and a backdrop for your game. You can choose any you like! Here's an example:

![screenshot](images/brain-setting.png)

\--- /task \---

\--- task \---

Make sure you have your character sprite selected. Create two new variables, called `number 1`{:class="block3variables"} and `number 2`{:class="block3variables"}, to store the numbers for the quiz questions.

![screenshot](images/giga-sprite.png)

![screenshot](images/brain-variables.png)

[[[generic-scratch3-add-variable]]]

\--- / tasca \---

\--- task \---

Add code to your character sprite to set both of the `variables`{:class="block3variables"} to a `random`{:class="block3operators"} number between 2 and 12.

![screenshot](images/giga-sprite.png)

```blocks3
quan l'indicador fa clic a
estableix [número 1 v] a (seleccioneu aleatòries (2) a (12))
conjunt [número 2 v] a (seleccioneu aleatòries (2) a (12))
```

\--- /task \---

\--- task \---

Add code to `ask`{:class="block3sensing"} the player for the answer, and then `say for 2 seconds`{:class="block3looks"} whether the answer was right or wrong:

![screenshot](images/giga-sprite.png)

```blocks3
quan l'indicador fa clic a
estableix [número 1 v] a (seleccioneu aleatòries (2) a (12))
conjunt [número 2 v] a (seleccioneu aleatòries (2) a (12))

+ pregunteu (uniu-vos (número 1) (uniu-vos [x] (número 2))) i espereu
+ si <(resposta) = ((número 1) * (número 2))> i
+ digueu [sí! :)] per (2) segons
+ més
+ dir [no :(] per (2) segons
+ final
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
per sempre
final
```

\--- /hint \---

\--- hint \---

Here is what your code should look like:

```blocks3
quan es fa clic a la bandera

+ per sempre
    conjunt [número 1 v] a (seleccioneu aleatòries (2) a (12))
    conjunt [número 2 v] a (seleccioneu aleatòries (2) a (12))
    pregunteu (uniu-vos (nombre 1) (uniu-vos [x] (número 2)) i espereu
    si <(resposta) = ((número 1) * (número 2))> i
        digueu [sí! :)] durant (2) segons
    més
        digue [no :(] per (2) segons
    final
final
```

\--- /hint \---

\--- /hints \---

\--- /task \---