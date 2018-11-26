## Add a timer

--- task ---
Create a countdown timer on the stage, using a variable called `time`{:class="blockdata"}. The time should begin at 30 seconds and count down to 0 seconds.

![Stage sprite](images/stage-sprite.png)

--- hints ---
--- hint ---
Create a `variable`{:class="blockdata"} called time which begins at 30 seconds and counts down to 0 seconds. To do this, subtract 1 from the timer every 1 second, and repeat this until the timer equals 0.
--- /hint ---
--- hint ---
Here are the blocks you will need:

```blocks
repeat until < >

end

wait (1) secs

change [time v] by (1)

(time)

when flag clicked

<() = ()>

set [time v] to [0]
```
--- /hint ---
--- hint ---
Here is the code you will need:
```blocks
when flag clicked
set [time v] to [30]
repeat until <(time) = (0)>
    wait (1) secs
    change [time v] by (-1)
end
```
--- /hint ---
--- /hints ---

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
