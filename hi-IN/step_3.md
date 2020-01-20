## टाइमर जोड़ें

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
दोहराते रहें जब तक < >

अंत

(1) सेकंड प्रतीक्षा करें

(1) se [समय v] बदलें

(समय)

जब झंडा क्लिक किया

<() = ()>

[समय v] को [0] स्थिर करें
```

\--- /hint \---

\--- hint \---

Here is the what your new code should look like:

```blocks3
जब ध्वज पर क्लिक किया
[समय v] को [30] स्थिर करें
दोहराएं जब तक <(समय) = (0)>
    (1) सेकंड प्रतीक्षा करें
    (-1) से [समय v] बदलें 
अंत
```

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

Create a `broadcast`{:class="block3control"} that sends the message 'end'. A `broadcast`{:class="block3control"} is like an announcement over a loudspeaker: it can be heard by all of your sprites. Add the `broadcast`{:class="block3control"} block to the end of the timer code so that the code will send and 'end' message when the `time`{:class="block3variables"} has counted down to `0`.

![Stage sprite](images/stage-sprite.png)

```blocks3
    प्रसारित करें (अंत v)
```

\--- /task \---

\--- task \---

Select your character sprite and add some code so that the sprite `stops the other scripts`{:class="block3control"} when it receives the `end`{:class="block3control"} message.

![Giga sprite](images/giga-sprite.png)

```blocks3
    जब मुझे [अंत v] मिलता है
    रोकें [स्प्राइट v में अन्य स्प्राइट्स]
```

\--- /task \---

\--- task \---

Test your game again. It should continue to ask questions until the timer has counted down to 0.

\--- /task \---