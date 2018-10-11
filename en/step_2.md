## Creating questions

Let's start by creating random questions for the player to answer.

--- task ---

Open a new Scratch project.

**Online:** Open a new online Scratch project at [rpf.io/scratchon](http://rpf.io/scratchon).

**Offline:** Open a new project in the offline editor.
If you need to download the Scratch offline editor you will find it at [rpf.io/scratchoff](http://rpf.io/scratchoff).

--- /task ---

--- task ---
Choose a character and a backdrop for your game. You can choose any you like! Here's an example:

![screenshot](images/brain-setting.png)

--- /task ---

--- task ---
Make sure you have your character sprite selected. Create two new variables called `number 1`{:class="blockdata"} and `number 2`{:class="blockdata"}. These variables will store the numbers that will be multiplied together.

![screenshot](images/giga-sprite.png)
![screenshot](images/brain-variables.png)

--- /task ---

--- task ---
Add code to your character to set both of these variables to a `random`{:class="blockoperators"} number between 2 and 12.

![screenshot](images/giga-sprite.png)

```blocks
	when flag clicked
	set [number 1 v] to (pick random (2) to (12))
	set [number 2 v] to (pick random (2) to (12))
```

--- /task ---

--- task ---
You can then ask the player for the answer, and let them know if they were right or wrong. Add this code:

![screenshot](images/giga-sprite.png)

```blocks
	when flag clicked
	set [number 1 v] to (pick random (2) to (12))
	set [number 2 v] to (pick random (2) to (12))
	+ ask (join (number 1)(join [ x ] (number 2))) and wait
	+ if <(answer) = ((number 1)*(number 2))> then
		+ say [yes! :)] for (2) secs
	+ else
		+ say [nope :(] for (2) secs
	+ end
```
--- /task ---

--- task ---
Test your project twice, answering one question correctly and one with the wrong answer.
--- /task ---

--- task ---
Add a `forever`{:class="blockcontrol"} loop around this code, so that the player is asked lots of questions in a row.
--- /task ---
