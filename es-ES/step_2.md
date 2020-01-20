## Crear preguntas

Vas a empezar por crear preguntas aleatorias que el jugador tendrá que contestar.

\--- task \---

Abre un nuevo proyecto en Scratch.

**Online:** abre un nuevo proyecto en [rpf.io/scratch-new](http://rpf.io/scratch-new){:target="_blank"}.

**Offline:** abre un nuevo proyecto en el editor offline.

Si necesitas descargar e instalar el editor offline de Scratch, puedes encontrarlo en [rpf.io/scratchoff](http://rpf.io/scratchoff){:target="_blank"}.

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
al hacer clic en la bandera verde
dar a [número 1 v] el valor (número aleatorio entre (2) y (12))
dar a [número 2 v] el valor (número aleatorio entre (2) y (12))
```

\--- /task \---

\--- task \---

Add code to `ask`{:class="block3sensing"} the player for the answer, and then `say for 2 seconds`{:class="block3looks"} whether the answer was right or wrong:

![screenshot](images/giga-sprite.png)

```blocks3
al hacer clic en la bandera verde
dar a [número 1 v] el valor (número aleatorio entre (2) y (12))
dar a [número 2 v] el valor (número aleatorio entre (2) y (12))

+ preguntar (unir (número 1)(unir [ x ] (número 2))) y esperar
+ si <(respuesta) = ((número 1)*(número 2))> entonces
+ decir [¡sí! :)] durante (2) segundos
+ si no
+ decir [no :(] durante (2) segundos
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
por siempre
fin
```

\--- /hint \---

\--- hint \---

Here is what your code should look like:

```blocks3
al hacer clic en la bandera verde
+ por siempre
    dar a [número 1 v] el valor (número aleatorio entre (2) y (12))
    dar a [número 2 v] el valor (número aleatorio entre (2) y (12))
    preguntar (unir (número 1)(unir [ x ] (número 2))) y esperar
    si <(respuesta) = ((número 1)*(número 2))> entonces
        decir [¡sí! :)] durante (2) segundos
    si no
        decir [no :(] durante (2) segundos
    fin
fin
```

\--- /hint \---

\--- /hints \---

\--- /task \---