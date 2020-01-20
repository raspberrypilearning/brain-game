## একাধিক গেম

এখন আপনি একটি 'প্লে' বোতাম যুক্ত করতে যাচ্ছেন, যাতে প্লেয়ার আপনার গেমটি অনেক বার খেলতে পারে।

\--- task \---

Create a new 'Play' button sprite that the player needs to click to start a new game.

You can draw the sprite yourself, or edit a sprite from the library.

![Picture of the play button](images/brain-play.png)

\--- /task \---

\--- task \---

Add this code to your button sprite:

![Button sprite](images/button-sprite.png)

```blocks3
    যখন পতাকা ক্লিক
    প্রদর্শনী

    এই পরী ক্লিক
    লুকান
    ব্রডকাস্ট (শুরু উ)
```

\--- /task \---

The new code includes another `broadcast`{:class="block3events"} block, which sends the message 'start'.

The new code makes the 'Play' button sprite show when when player clicks on the flag. When the player clicks on the button sprite, the sprite hides and then broadcasts a message that other sprites can react to.

At the moment, the character sprite starts asking questions when the player clicks the flag. Change your game's code so that character sprite starts asking questions when it receives the 'start' `broadcast`{:class="block3events"}.

\--- task \---

Select your character sprite and, in its code section, replace the `when flag clicked`{:class="block3events"} block with a `when I receive start`{:class="block3events"} block.

![Character sprite](images/giga-sprite.png)

```blocks3
<br />- যখন আমি
ক্লিক করি তখন + ফ্ল্যাগে ক্লিক করুন [শুরু v]
সেট [সংখ্যা 1 ভি] থেকে (র্যান্ডম (2) থেকে (12))
সেট [সংখ্যা 2 ভি] থেকে (র্যান্ডম (2) থেকে (12) )
জিজ্ঞাসা করুন (যোগদানের (নম্বর 1) (যোগদানের [X] (নম্বর 2))) এবং অপেক্ষা করুন
যদি <(উত্তর) = ((নম্বর 1) * (সংখ্যা 2))> তারপর
    বলে [হ্যাঁ! :)] জন্য (2) সেকেন্ড
অন্য
    বলুন [নাপ :(] জন্য (2) সেকেন্ড
শেষ
```

\--- /কাজ \---

\--- task \---

Click the green flag, and then click on the new 'Play' button to test whether it works. You should see that the game doesn't start before you click on the button.

\--- /task \---

Can you see that the timer starts when the green flag is clicked, instead of when the game starts?

![Timer has started](images/brain-timer-bug.png)

\--- task \---

Can you change the code for the timer so that the timer starts when the player clicks on the button?

\--- /কাজ \---

\--- কাজ \---

Add code to your button sprite so that the button shows again at the end of each game.

![Button sprite](images/button-sprite.png)

```blocks3
    যখন আমি [শেষ ভি]
    শো পাবেন
```

\--- /task \---

\--- task \---

Test the 'Play' button by playing a couple of games. The button should show at the end of each game.

To test the game more quickly, you can change the value of `time`{:class="block3variables"} so that each game is only a few seconds long.

![Stage](images/stage-sprite.png)

```blocks3
    সেট [সময় ভি] থেকে [10]
```

\--- /task \---

\--- task \---

You can change how the button looks when the mouse pointer hovers over it.

![Button](images/button-sprite.png)

```blocks3
    যখন ফ্ল্যাগটি
    শো
    চিরতরে ক্লিক করে
 <touching (mouse-pointer v)?> তারপর
        সেট [ফিশেয় ভি] প্রভাবটি (30)
    অন্য
        সেট [ফিশেইএ ভি] প্রভাব (0)
    শেষ
    শেষের দিকে
```

![screenshot](images/brain-fisheye.png)

\--- /task \---