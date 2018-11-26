## Adding graphics

Instead of your character just saying `yes! :)` or `nope :(` to the player, let's add some graphics that will let the player know how they are doing.

--- task ---
Create a new sprite called 'Result', containing both a 'tick' and a 'cross' costume.

![Sprite with tick and cross costumes](images/brain-result.png)

--- /task ---

--- task ---
Change your character's code, so that instead of telling the player how they did, it broadcasts `correct`{:class="blockevents"} and `wrong`{:class="blockevents"} messages instead.

![Character sprite](images/character-sprite.png)

```blocks
    if <(answer) = ((number 1)*(number 2))> then
	   - say [yes! :)] for (2) secs
       + broadcast [correct v]
	else
	   - say [nope :(] for (2) secs
       + broadcast [wrong v]
	end
```

--- /task ---

--- task ---
You can now use these messages to show the 'tick' or 'cross' costume. Add this code to your new 'Result' sprite:

![Result sprite](images/result-sprite.png)

```blocks
    when I receive [correct v]
    switch costume to [tick v]
    show
    wait (1) secs
    hide

    when I receive [wrong v]
    switch costume to [cross v]
    show
    wait (1) secs
    hide

    when flag clicked
    hide
```

--- /task ---

--- task ---
Test out your game again. You should see a tick whenever you get a question correct, and a cross whenever you get one wrong!

![Tick for correct, cross for wrong answer](images/brain-test-answer.png)

--- /task ---


Have you noticed that the code for `when I receive correct`{:class="blockevents"} and `when I receive wrong`{:class="blockevents"} is nearly identical? Let's create a custom block to make it easier for you to make changes to your code.

--- task ---
On your 'Result' sprite, click `More Blocks`{:class="blockmoreblocks"}, and then 'Make a Block'. Create a new block called `animate`{:class="blockmoreblocks"}.

![Create a block called animate](images/brain-animate-function.png)
--- /task ---

--- task ---
Move the code to show and hide the result sprite into your new animation block:

![Result sprite](images/result-sprite.png)

```blocks
define animate
show
wait (1) secs
hide
```
--- /task ---

--- task ---
Now remove the other blocks and add the block `animate`{:class="blockmoreblocks"} to happen after the costume switch:

![Result sprite](images/result-sprite.png)

```blocks
    when I receive [correct v]
    switch costume to [tick v]
    animate:: custom

    when I receive [wrong v]
    switch costume to [cross v]
    animate:: custom
```

--- /task ---

If you want to show the tick and the cross for a longer or shorter time, you only need to make one change to your code.

--- task ---
Change your code so that the tick or cross displays for 2 seconds.
--- /task ---

--- task ---
Instead of just showing and hiding the tick and the cross, you could change your animation function, so that the graphics fade in.

![Result sprite](images/result-sprite.png)

```blocks
	define animate
	set [ghost v] effect to (100)
	show
	repeat (25)
		change [ghost v] effect by (-4)
	end
	hide
```
--- /task ---

Can you improve the animation of your graphics? You could code the tick and cross so that they fade out as well as fade in. Or, you could use other cool effects:

![screenshot](images/brain-effects.png)
