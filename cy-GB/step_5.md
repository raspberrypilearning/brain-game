## Gemau lluosog

Fe wnawn ni ychwanegu botwm ‘chwarae’ i dy gêm fel dy fod di’n gallu chwarae sawl gwaith.

\--- task \--- Bydd angen creu corlun botwm ‘Chwarae’, sef beth fydd y chwareuwr yn clicio i ddechrau gêm newydd.

Fe alli di ei lunio dy hunan, neu olygu corlun o lyfrgell Scratch.

![Picture of the play button](images/brain-play.png)

\--- /task \---

\--- task \--- Ychwanega'r côd yma i gorlun dy fotwm:

![Button sprite](images/button-sprite.png)

```blocks3
    when flag clicked
    show

    when this sprite clicked
    hide
    broadcast (start v)
```

\--- /task \---

Mae'r côd newydd yma yn cynnwys bloc arall `darlledu`{:class="block3events"}, sydd yn anfon neges i 'ddechrau'.

Mae'r côd newydd yn gwneud i'r corlun 'Chwarae' ymddangos pan mae'r chwareuwr yn clicio ar y faner. Pan fydd y botwm yn cael ei glicio, fe fydd yn cuddio a darlledu neges fydd yn cychwyn y gêm.

Ar hyn o bryd, mae'r cymeriad yn gofyn cwestiynau pan mae'r chwareuwr yn clicio ar y faner. Bydd angen i ti olygu côd dy gymeriad fel bod y gêm yn cychwyn pan mae’n derbyn neges `dechrau`{:class="block3events"}.

\--- task \--- Dewisa dy gymeriad, ac yn yr adran gôd, ailosoda `pan fo baner wedi ei glicio`{:class="block3events"} gyda `pan dderbyniaf dechrau`{:class="block3events"}.

![Character sprite](images/giga-sprite.png)

```blocks3
<br />- when flag clicked
+ when I receive [start v]
set [number 1 v] to (pick random (2) to (12))
set [number 2 v] to (pick random (2) to (12))
ask (join (number 1)(join [ x ] (number 2))) and wait
if &lt;(answer) = ((number 1)*(number 2))&gt; then
    say [yes! :)] for (2) seconds
else
    say [nope :(] for (2) seconds
end
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

\--- task \--- Add code to your button sprite so that the button shows again at the end of each game.

![Button sprite](images/button-sprite.png)

```blocks3
    when I receive [end v]
    show
```

\--- /task \---

\--- task \---

Test the 'Play' button by playing a couple of games. The button should show at the end of each game.

To test the game more quickly, you can change the value of `time`{:class="block3variables"} so that each game is only a few seconds long.

![Stage](images/stage-sprite.png)

```blocks3
    set [time v] to [10]
```

\--- /task \---

\--- task \--- You can change how the button looks when the mouse pointer hovers over it.

![Button](images/button-sprite.png)

```blocks3
    when flag clicked
    show
    forever
    if <touching (mouse-pointer v)?> then
        set [fisheye v] effect to (30)
    else
        set [fisheye v] effect to (0)
    end
    end
```

![screenshot](images/brain-fisheye.png) \--- /task \---