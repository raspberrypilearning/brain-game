## Jocuri multiple

Acum, vei adăuga un buton "Play", astfel încât jucătorul să poată juca jocul tău de mai multe ori.

\--- task \---

Create a new 'Play' button sprite that the player needs to click to start a new game.

You can draw the sprite yourself, or edit a sprite from the library.

![Picture of the play button](images/brain-play.png)

\--- /task \---

\--- task \---

Add this code to your button sprite:

![Button sprite](images/button-sprite.png)

```blocks3
    când dăm click pe steagul verde
    arată

    când dăm click pe personaj 
    ascunde
    difuzează (începe v)
```

\--- /task \---

The new code includes another `broadcast`{:class="block3events"} block, which sends the message 'start'.

The new code makes the 'Play' button sprite show when when player clicks on the flag. When the player clicks on the button sprite, the sprite hides and then broadcasts a message that other sprites can react to.

At the moment, the character sprite starts asking questions when the player clicks the flag. Change your game's code so that character sprite starts asking questions when it receives the 'start' `broadcast`{:class="block3events"}.

\--- task \---

Select your character sprite and, in its code section, replace the `when flag clicked`{:class="block3events"} block with a `when I receive start`{:class="block3events"} block.

![Character sprite](images/giga-sprite.png)

```blocks3
<br />- atunci când dau click pe steagul verde
+ când primesc [start v]
setează [number 1 v] la (alegeți aleatoriu de la (2) la (12))
setează [numărul 2 v] la (alegeți aleatoriu de la (2) la (12))
cere (adaugă (numărul 1)(adaugă [x] (numărul 2))) și așteaptă
dacă <(răspuns) = ((numărul 1) * (numărul 2))> apoi
    spun [da! :)] pentru (2) secunde
altceva
    spune [nu :(] pentru (2) secunde
sfarsit
```

\--- /task \---

\--- task \---

Click the green flag, and then click on the new 'Play' button to test whether it works. You should see that the game doesn't start before you click on the button.

\--- /task \---

Can you see that the timer starts when the green flag is clicked, instead of when the game starts?

![Timer has started](images/brain-timer-bug.png)

\--- task \---

Can you change the code for the timer so that the timer starts when the player clicks on the button?

\--- /task \---

\--- task \---

Add code to your button sprite so that the button shows again at the end of each game.

![Button sprite](images/button-sprite.png)

```blocks3
    când primesc [sfârșit v]
    arată
```

\--- /task \---

\--- task \---

Test the 'Play' button by playing a couple of games. The button should show at the end of each game.

To test the game more quickly, you can change the value of `time`{:class="block3variables"} so that each game is only a few seconds long.

![Stage](images/stage-sprite.png)

```blocks3
    setați ora [v] la [10]
```

\--- /task \---

\--- task \---

You can change how the button looks when the mouse pointer hovers over it.

![Button](images/button-sprite.png)

```blocks3
    când pavilionul apăsat
    arată
    pentru totdeauna
    dacă <touching (mouse-pointer v)?> apoi
        setați [fishheye v] effect to (30)
    altceva
        set [efect fisheye v] efect la (0)
    sfârșitul

```

![screenshot](images/brain-fisheye.png)

\--- /task \---