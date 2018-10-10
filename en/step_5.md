## Multiple games

Let's add a 'play' button to your game, so that you can play lots of times.

--- task ---
Create a new 'Play' button sprite, which your player will click to start a new game. You can draw it yourself, or edit a sprite from the Scratch library.

![screenshot](images/brain-play.png)

--- /task ---

--- task ---
Add this code to your new button.

![Button sprite](images/button-sprite.png)

```blocks
	when flag clicked
	show

	when this sprite clicked
	hide
	broadcast [start v]
```

--- /task ---

This code shows the play button when your project is started. When the button is clicked, it is hidden and then broadcasts a message that will start the game.

Now you need the game to start when the character receives the `start`{:class="blockevents"} message, instead of when the flag is clicked.

--- task ---
In your character sprite, replace the `when flag clicked`{:class="blockevents"} code with `when I receive start`{:class="blockevents"}.

![Giga sprite](images/giga-sprite.png)

```blocks
	- when flag clicked
    + when I receive [start v]
	set [number 1 v] to (pick random (2) to (12))
	set [number 2 v] to (pick random (2) to (12))
	ask (join (number 1)(join [ x ] (number 2))) and wait
	if <(answer) = ((number 1)*(number 2))> then
		say [yes! :)] for (2) secs
	else
		say [nope :(] for (2) secs
	end
```
--- /task ---

--- task ---
Click the green flag and then click your new play button to test it. You should see that the game doesn't start until the button is clicked.
--- /task ---

Did you notice that the timer starts when the green flag is clicked, and not when the game starts?

![screenshot](images/brain-timer-bug.png)

--- task ---
Can you change the timer so that it starts when the button is pressed?
--- /task ---

--- task ---
Click on the stage, and replace the `stop all`{:class="blockcontrol"} block with an `end`{:class="blockevents"} message.

![screenshot](images/brain-end.png)
--- /task ---

--- task ---
You can now add code to your button, to show it again at the end of each game.

```blocks
	when I receive [end v]
	show
```
--- /task ---

--- task ---
You'll also need to stop your character asking questions at the end of each game:

```blocks
	when I receive [end v]
	stop [other scripts in sprite v]
```
--- /task ---

--- task ---
Test your play button by playing a couple of games. You should notice that the play button shows after each game. To make testing easier, you can shorten each game, so that it only lasts a few seconds.

```blocks
	set [time v] to [10]
```

--- /task ---

--- task ---
You can even change how the button looks when the mouse hovers over it.

```blocks
	when flag clicked
	show
	forever
	if <touching [mouse-pointer v]?> then
		set [fisheye v] effect to (30)
	else
		set [fisheye v] effect to (0)
	end
	end
```

![screenshot](images/brain-fisheye.png)
--- /task ---
