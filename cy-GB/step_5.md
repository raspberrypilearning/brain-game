## Gemau lluosog

Fe wnawn ni ychwanegu botwm ‘chwarae’ i dy gêm fel dy fod di’n gallu chwarae sawl gwaith.

\--- task \---

Create a new 'Play' button sprite that the player needs to click to start a new game.

You can draw the sprite yourself, or edit a sprite from the library.

![Picture of the play button](images/brain-play.png)

\--- /task \---

\--- task \---

Add this code to your button sprite:

![Button sprite](images/button-sprite.png)

```blocks3
    pan fo'r flag werdd yn cael ei glicio
dangos

pan gaiff y ciplun yma ei glicio
cuddio
darlledu (start v)
```

\--- /task \---

The new code includes another `broadcast`{:class="block3events"} block, which sends the message 'start'.

The new code makes the 'Play' button sprite show when player clicks on the flag. When the player clicks on the button sprite, the sprite hides and then broadcasts a message that other sprites can react to.

At the moment, the character sprite starts asking questions when the player clicks the flag. Change your game's code so that character sprite starts asking questions when it receives the 'start' `broadcast`{:class="block3events"}.

\--- task \---

Select your character sprite and, in its code section, replace the `when flag clicked`{:class="block3events"} block with a `when I receive start`{:class="block3events"} block.

![Character sprite](images/giga-sprite.png)

```blocks3
<br />- pan fo'r flag werdd yn cael ei glicio
+ pan rwy'n derbyn [start v]
gosod [rhif 1 v] i (dewis ar hap (2) i (12))
gosod [rhif 2 v] i (dewis ar hap (2) i (12))
gofyn (uno (rhif 1) (uno [ x ] (rhif 2))) ac aros
os <(ateb) = ((rhif 1) * (rhif 2))> yna 
  dweud [Ie! :)] am (2) eiliad
fel arall 
  dweud [Na :(] am (2) eiliad
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

\--- task \---

Add code to your button sprite so that the button shows again at the end of each game.

![Button sprite](images/button-sprite.png)

```blocks3
    pan rwy'n derbyn [end v]
dangos
```

\--- /task \---

\--- task \---

Test the 'Play' button by playing a couple of games. The button should show at the end of each game.

To test the game more quickly, you can change the value of `time`{:class="block3variables"} so that each game is only a few seconds long.

![Stage](images/stage-sprite.png)

```blocks3
    gosod [amser v] i [10]
```

\--- /task \---

\--- task \---

You can change how the button looks when the mouse pointer hovers over it.

![Button](images/button-sprite.png)

```blocks3
    pan fo'r flag werdd yn cael ei glicio
dangos
am byth 
  os <cyffwrdd (mouse-pointer v) ?> yna 
    gosod effaith [fisheye v] effaith i (30)
  fel arall 
    gosod effaith [fisheye v] effaith i (0)
  end
end
```

![screenshot](images/brain-fisheye.png)

\--- /task \---