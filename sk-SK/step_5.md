## Viacnásobné hry

Teraz pridáte tlačidlo "Prehrať", aby hráč mohol hrať vašu hru veľa krát.

\--- task \---

Create a new 'Play' button sprite that the player needs to click to start a new game.

You can draw the sprite yourself, or edit a sprite from the library.

![Picture of the play button](images/brain-play.png)

\--- /task \---

\--- task \---

Add this code to your button sprite:

![Button sprite](images/button-sprite.png)

```blocks3
    keď klaksón klikne
    zobrazí

    keď tento sprite klikol
    skryť
    vysielanie (štart v)
```

\--- /task \---

The new code includes another `broadcast`{:class="block3events"} block, which sends the message 'start'.

The new code makes the 'Play' button sprite show when when player clicks on the flag. When the player clicks on the button sprite, the sprite hides and then broadcasts a message that other sprites can react to.

At the moment, the character sprite starts asking questions when the player clicks the flag. Change your game's code so that character sprite starts asking questions when it receives the 'start' `broadcast`{:class="block3events"}.

\--- task \---

Select your character sprite and, in its code section, replace the `when flag clicked`{:class="block3events"} block with a `when I receive start`{:class="block3events"} block.

![Character sprite](images/giga-sprite.png)

```blocks3
<br />- ak príznak ukážete
+ keď dostanem [start v]
nastaviť [číslo 1 v] na (vybrať náhodné (2) až (12))
nastaviť [číslo 2 v] )
pýtať (join (číslo 1) (pripojiť [x] (číslo 2))) a počkajte
v prípade <(odpoveď) = ((číslo 1) * (číslo 2))> potom
    povedať [áno! :)] za (2) sekundy
inak
    povedal [nope :(] za (2) sekundy
koniec
```

\--- / úloha \---

\--- task \---

Click the green flag, and then click on the new 'Play' button to test whether it works. You should see that the game doesn't start before you click on the button.

\--- /task \---

Can you see that the timer starts when the green flag is clicked, instead of when the game starts?

![Timer has started](images/brain-timer-bug.png)

\--- task \---

Can you change the code for the timer so that the timer starts when the player clicks on the button?

\--- / úloha \---

\--- úloha \---

Add code to your button sprite so that the button shows again at the end of each game.

![Button sprite](images/button-sprite.png)

```blocks3
    keď dostanem [end v]
    show
```

\--- /task \---

\--- task \---

Test the 'Play' button by playing a couple of games. The button should show at the end of each game.

To test the game more quickly, you can change the value of `time`{:class="block3variables"} so that each game is only a few seconds long.

![Stage](images/stage-sprite.png)

```blocks3
    nastavte čas [v] na [10]
```

\--- /task \---

\--- task \---

You can change how the button looks when the mouse pointer hovers over it.

![Button](images/button-sprite.png)

```blocks3
    keď vlajka klikne
    zobrazí
    navždy
    ak <touching (mouse-pointer v)?> potom
        nastaviť [rybie oko] efekt na (30)
    iný
        nastaviť [rybie oko] efekt na (0)
    koniec
    koniec
```

![screenshot](images/brain-fisheye.png)

\--- /task \---