## Creare domande

Inizierai creando domande casuali a cui il giocatore deve rispondere.

\--- task \---

Inizia un nuovo progetto Scratch.

**Online:** open a new online Scratch project at [rpf.io/scratch-new](http://rpf.io/scratch-new){:target="_blank"}.

**Offline:** apri un nuovo progetto nell'editor offline.

Se hai bisogno di scaricare ed installare l'editor Scratch offline, puoi trovarlo su [rpf.io/scratchoff](http://rpf.io/scratchoff){:target="_blank"}.

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
when flag clicked
set [numero 1 v] to (pick random (2) to (12))
set [numero 2 v] to (pick random (2) to (12))
```

\--- /task \---

\--- task \---

Add code to `ask`{:class="block3sensing"} the player for the answer, and then `say for 2 seconds`{:class="block3looks"} whether the answer was right or wrong:

![screenshot](images/giga-sprite.png)

```blocks3
when flag clicked
set [numero 1 v] to (pick random (2) to (12))
set [numero 2 v] to (pick random (2) to (12))

+ ask (join (numero 1)(join [ x ] (numero 2))) and wait
+ if <(answer) = ((numero 1)*(numero 2))> then
+ say [si! :)] for (2) seconds
+ else
+ say [no :(] for (2) seconds
+ end
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
forever
end
```

\--- /hint \---

\--- hint \---

Here is what your code should look like:

```blocks3
when flag clicked

+ forever
    set [numero 1 v] to (pick random (2) to (12))
    set [numero 2 v] to (pick random (2) to (12))
    ask (join (numero 1)(join [ x ] (numero 2))) and wait
    if <(answer) = ((numero 1)*(numero 2))> then
        say [si! :)] for (2) seconds
    else
        say [no :(] for (2) seconds
    end
end
```

\--- /hint \---

\--- /hints \---

\--- /task \---