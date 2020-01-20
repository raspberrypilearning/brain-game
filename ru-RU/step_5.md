## Несколько игр

Теперь вы собираетесь добавить кнопку «Играть», чтобы игрок мог играть в вашу игру много раз.

\--- task \---

Create a new 'Play' button sprite that the player needs to click to start a new game.

You can draw the sprite yourself, or edit a sprite from the library.

![Picture of the play button](images/brain-play.png)

\--- /task \---

\--- task \---

Add this code to your button sprite:

![Button sprite](images/button-sprite.png)

```blocks3
    когда щёлкнут по зелёному флагу
    показаться

    когда спрайт нажат
    спрятаться
    передать (start v)
```

\--- /task \---

The new code includes another `broadcast`{:class="block3events"} block, which sends the message 'start'.

The new code makes the 'Play' button sprite show when when player clicks on the flag. When the player clicks on the button sprite, the sprite hides and then broadcasts a message that other sprites can react to.

At the moment, the character sprite starts asking questions when the player clicks the flag. Change your game's code so that character sprite starts asking questions when it receives the 'start' `broadcast`{:class="block3events"}.

\--- task \---

Select your character sprite and, in its code section, replace the `when flag clicked`{:class="block3events"} block with a `when I receive start`{:class="block3events"} block.

![Character sprite](images/giga-sprite.png)

```blocks3
<br />- когда флаг щелкнул
+, когда я получил [start v]
установите [number 1 v] в (выберите random (2) в (12))
установите [number 2 v] в (выберите random (2) в (12) )
спросить (присоединиться (номер 1) (присоединиться к [x] (номер 2))) и ждать
если <(ответ) = ((номер 1) * (номер 2))> затем
    сказать [да! :)] в течение (2) секунд
иначе
    произнесите [nope :(] в течение (2) секунд
конца
```

\--- / задача \---

\--- task \---

Click the green flag, and then click on the new 'Play' button to test whether it works. You should see that the game doesn't start before you click on the button.

\--- /task \---

Can you see that the timer starts when the green flag is clicked, instead of when the game starts?

![Timer has started](images/brain-timer-bug.png)

\--- task \---

Can you change the code for the timer so that the timer starts when the player clicks on the button?

\--- / задача \---

\--- задача \---

Add code to your button sprite so that the button shows again at the end of each game.

![Button sprite](images/button-sprite.png)

```blocks3
    когда я получу [конец v]
    шоу
```

\--- /task \---

\--- task \---

Test the 'Play' button by playing a couple of games. The button should show at the end of each game.

To test the game more quickly, you can change the value of `time`{:class="block3variables"} so that each game is only a few seconds long.

![Stage](images/stage-sprite.png)

```blocks3
    установите [время v] на [10]
```

\--- /task \---

\--- task \---

You can change how the button looks when the mouse pointer hovers over it.

![Button](images/button-sprite.png)

```blocks3
    когда флажок установлен,
    показывает
    навсегда
    если <touching (mouse-pointer v)?> то
        установите для эффекта [fisheye v] значение (30)
    иначе для
        установите для эффекта [fisheye v] значение (0)
    end
    end
```

![screenshot](images/brain-fisheye.png)

\--- /task \---