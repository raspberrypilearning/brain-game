## Add a timer

--- task ---
Create a countdown timer on the stage, using a variable called `time`{:class="blockdata"}. The timer should count down from 30 seconds to 0 seconds.

![Stage sprite](images/stage-sprite.png)

[[[generic-scratch-timer]]]
--- /task ---

--- task ---
Create a broadcast called `end`{:class="blockcontrol"}. A broadcast is like an announcement over a loudspeaker - it can be 'heard' by all of your sprites. Add the broadcast block to the end of the timer code so that it will broadcast when the timer reaches 0.

![Stage sprite](images/stage-sprite.png)

```blocks
    broadcast [end v]
```
--- /task ---

--- task ---
Go back to your character sprite and add some code to stop the scripts when the `end`{:class="blockcontrol"} broadcast is received.

![Giga sprite](images/giga-sprite.png)

```blocks
    when I receive [end v]
    stop [other scripts in sprite v]
```
--- /task ---

--- task ---
Test your project again - you should be able to continue asking questions until the time runs out.
--- /task ---
