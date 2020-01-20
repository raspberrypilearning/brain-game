## Diversos jocs

Ara, afegireu un botó "Reproduir", perquè el jugador pugui jugar moltes vegades.

\--- task \---

Create a new 'Play' button sprite that the player needs to click to start a new game.

You can draw the sprite yourself, or edit a sprite from the library.

![Picture of the play button](images/brain-play.png)

\--- /task \---

\--- task \---

Add this code to your button sprite:

![Button sprite](images/button-sprite.png)

```blocks3
    quan es fa clic a l'indicador
    mostra

    quan es fa clic a aquest sprite
    ocultar
    emissions (inici v)
```

\--- /task \---

The new code includes another `broadcast`{:class="block3events"} block, which sends the message 'start'.

The new code makes the 'Play' button sprite show when when player clicks on the flag. When the player clicks on the button sprite, the sprite hides and then broadcasts a message that other sprites can react to.

At the moment, the character sprite starts asking questions when the player clicks the flag. Change your game's code so that character sprite starts asking questions when it receives the 'start' `broadcast`{:class="block3events"}.

\--- task \---

Select your character sprite and, in its code section, replace the `when flag clicked`{:class="block3events"} block with a `when I receive start`{:class="block3events"} block.

![Character sprite](images/giga-sprite.png)

```blocks3
<br />- quan es fa clic a la bandera
+ quan rebo [inici v]
conjunt [número 1 v] a (seleccioneu aleatòries (2) a (12))
establir [número 2 v] a (seleccioneu aleatòries (2) a (12) )
pregunteu (uniu-vos (número 1) (uniu-vos [x] (número 2))) i espereu
si <(resposta) = ((nombre 1) * (número 2))> i
    digueu [sí! :)] per (2) segons
més
    digue [nope :(] per (2) segons
final
```

\--- / tasca \---

\--- task \---

Click the green flag, and then click on the new 'Play' button to test whether it works. You should see that the game doesn't start before you click on the button.

\--- /task \---

Can you see that the timer starts when the green flag is clicked, instead of when the game starts?

![Timer has started](images/brain-timer-bug.png)

\--- task \---

Can you change the code for the timer so that the timer starts when the player clicks on the button?

\--- / tasca \---

\--- tasca \---

Add code to your button sprite so that the button shows again at the end of each game.

![Button sprite](images/button-sprite.png)

```blocks3
    quan rebo l'exhibició [final v]

```

\--- /task \---

\--- task \---

Test the 'Play' button by playing a couple of games. The button should show at the end of each game.

To test the game more quickly, you can change the value of `time`{:class="block3variables"} so that each game is only a few seconds long.

![Stage](images/stage-sprite.png)

```blocks3
    estableixi [temps v] en [10]
```

\--- /task \---

\--- task \---

You can change how the button looks when the mouse pointer hovers over it.

![Button](images/button-sprite.png)

```blocks3
    quan es fa clic a la bandera
    mostren
    per sempre
    si <touching (mouse-pointer v)?> i
        defineixen [fisheye v] efecte a (30)
    més
        conjunt [fisheye v] efecte a (0)
    final
    final
```

![screenshot](images/brain-fisheye.png)

\--- /task \---