## Défi: Changement de costumes

\--- task \---

Create a countdown timer on the Stage with the help of a new variable called `time`{:class="block3variables"}. The timer should begin at 30 seconds and count down to 0 seconds.

![Stage sprite](images/stage-sprite.png)

\--- hints \---

\--- hint \---

Create a `variable`{:class="block3variables"}, call it 'time', and set its value to `30`.

Then add code to count `time`{:class="block3variables"} down to 0 within 30 seconds. To do this, subtract `1` from `time`{:class="block3variables"} every `1` second, and repeat this until `time`{:class="block3variables"} equals `0`.

\--- /hint \---

\--- hint \---

Here are the blocks you need:

```blocks3
répéter jusqu'à < >

fin

attendre (1) secondes

changer [temps v] par (1)

(temps)

lorsque le drapeau est cliqué

<() = ()>

définir [temps v] sur [0]
```

\--- /hint \---

\--- hint \---

Here is the what your new code should look like:

```blocks3
lorsque le drapeau est cliqué
définir [temps v] sur [30]
répéter jusqu'à ce que <(temps) = (0)>
    attendre (1) secondes
    changer [temps v] par (-1)
fin
```

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

Create a `broadcast`{:class="block3control"} that sends the message 'end'. A `broadcast`{:class="block3control"} is like an announcement over a loudspeaker: it can be heard by all of your sprites. Add the `broadcast`{:class="block3control"} block to the end of the timer code so that the code will send an 'end' message when the `time`{:class="block3variables"} has counted down to `0`.

![Stage sprite](images/stage-sprite.png)

```blocks3
    envoyer à tous (fin v)
```

\--- /task \---

\--- task \---

Select your character sprite and add some code so that the sprite `stops the other scripts`{:class="block3control"} when it receives the `end`{:class="block3control"} message.

![Giga sprite](images/giga-sprite.png)

```blocks3
    quand je reçois [fin v] 
    stop [autres scripts du lutin v]
```

\--- /task \---

\--- task \---

Test your game again. It should continue to ask questions until the timer has counted down to 0.

\--- /task \---