## Flera spel

Nu ska du lägga till en "Play" -knapp så att spelaren kan spela ditt spel många gånger.

\--- task \---

Create a new 'Play' button sprite that the player needs to click to start a new game.

You can draw the sprite yourself, or edit a sprite from the library.

![Picture of the play button](images/brain-play.png)

\--- /task \---

\--- task \---

Add this code to your button sprite:

![Button sprite](images/button-sprite.png)

```blocks3
    när flaggan klickade
    visar

    när den här sprite klickade
    hide
    broadcast (start v)
```

\--- /task \---

The new code includes another `broadcast`{:class="block3events"} block, which sends the message 'start'.

The new code makes the 'Play' button sprite show when when player clicks on the flag. When the player clicks on the button sprite, the sprite hides and then broadcasts a message that other sprites can react to.

At the moment, the character sprite starts asking questions when the player clicks the flag. Change your game's code so that character sprite starts asking questions when it receives the 'start' `broadcast`{:class="block3events"}.

\--- task \---

Select your character sprite and, in its code section, replace the `when flag clicked`{:class="block3events"} block with a `when I receive start`{:class="block3events"} block.

![Character sprite](images/giga-sprite.png)

```blocks3
<br />- när flaggan klickade
+ när jag mottar [start v]
set [number 1 v] till (välj slumpvis (2) till (12))
set [nummer 2 v] till (välj slumpvis (2) till (12) )
fråga (ansluta (nummer 1) (gå med i [x] (nummer 2))) och vänta
om <(svar) = ((nummer 1) * (nummer 2))> då
    säga [ja! :)] för (2) sekunder
annars
    säga [nope :(] för (2) sekunder
slutet
```

\--- / uppgift \---

\--- task \---

Click the green flag, and then click on the new 'Play' button to test whether it works. You should see that the game doesn't start before you click on the button.

\--- /task \---

Can you see that the timer starts when the green flag is clicked, instead of when the game starts?

![Timer has started](images/brain-timer-bug.png)

\--- task \---

Can you change the code for the timer so that the timer starts when the player clicks on the button?

\--- / uppgift \---

\--- uppgift \---

Add code to your button sprite so that the button shows again at the end of each game.

![Button sprite](images/button-sprite.png)

```blocks3
    när jag får [end v]
    show
```

\--- /task \---

\--- task \---

Test the 'Play' button by playing a couple of games. The button should show at the end of each game.

To test the game more quickly, you can change the value of `time`{:class="block3variables"} so that each game is only a few seconds long.

![Stage](images/stage-sprite.png)

```blocks3
    sätt [tid v] till [10]
```

\--- /task \---

\--- task \---

You can change how the button looks when the mouse pointer hovers over it.

![Button](images/button-sprite.png)

```blocks3
    när flaggan klickade
    visa
    alltid
    om <touching (mouse-pointer v)?> sedan
        sätt [fisheye v] effekt till (30)
    annat
        set [fisheye v] effekt till (0)
    slutet
    slutet
```

![screenshot](images/brain-fisheye.png)

\--- /task \---