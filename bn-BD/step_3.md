## একটি টাইমার যোগ করুন

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
পুনরাবৃত্তি করুন < >

শেষ

অপেক্ষা (1) সেকেন্ড

পরিবর্তন [সময় ভ] দ্বারা (1)

(সময়)

ফ্ল্যাগটি ক্লিক করলে

<() = ()>

সেট [সময় v] থেকে [0]
```

\--- /hint \---

\--- hint \---

Here is the what your new code should look like:

```blocks3
যখন পতাকাটি
সেট [সময় v] থেকে [30]টিতে
পুনরাবৃত্তি হয় <(সময়) = (0)>
    অপেক্ষা (1) সেকেন্ড
    পরিবর্তন [সময় v] দ্বারা (-1)
শেষ
```

\--- /hint \---

\--- /hints \---

\--- /কাজ \---

\--- কাজ \---

Create a `broadcast`{:class="block3control"} that sends the message 'end'. A `broadcast`{:class="block3control"} is like an announcement over a loudspeaker: it can be heard by all of your sprites. Add the `broadcast`{:class="block3control"} block to the end of the timer code so that the code will send and 'end' message when the `time`{:class="block3variables"} has counted down to `0`.

![Stage sprite](images/stage-sprite.png)

```blocks3
    সম্প্রচার (শেষ v)
```

\--- /task \---

\--- task \---

Select your character sprite and add some code so that the sprite `stops the other scripts`{:class="block3control"} when it receives the `end`{:class="block3control"} message.

![Giga sprite](images/giga-sprite.png)

```blocks3
    যখন আমি পাই [শেষ v]
    স্টপ [স্প্রিট v অন্যান্য স্ক্রিপ্ট]
```

\--- /task \---

\--- task \---

Test your game again. It should continue to ask questions until the timer has counted down to 0.

\--- /task \---