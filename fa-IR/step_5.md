## بازی های چندگانه

حالا شما قصد دارید یک دکمه Play را اضافه کنید تا بازیکن بتواند بازی شما را چند بار بازی کند.

\--- task \---

Create a new 'Play' button sprite that the player needs to click to start a new game.

You can draw the sprite yourself, or edit a sprite from the library.

![Picture of the play button](images/brain-play.png)

\--- /task \---

\--- task \---

Add this code to your button sprite:

![Button sprite](images/button-sprite.png)

```blocks3
    زمانی که پرچم روی آن کلیک کنید
    نمایش

    زمانی که این صحنه کلیک کرد
    پنهان
    پخش (شروع V)
```

\--- /task \---

The new code includes another `broadcast`{:class="block3events"} block, which sends the message 'start'.

The new code makes the 'Play' button sprite show when when player clicks on the flag. When the player clicks on the button sprite, the sprite hides and then broadcasts a message that other sprites can react to.

At the moment, the character sprite starts asking questions when the player clicks the flag. Change your game's code so that character sprite starts asking questions when it receives the 'start' `broadcast`{:class="block3events"}.

\--- task \---

Select your character sprite and, in its code section, replace the `when flag clicked`{:class="block3events"} block with a `when I receive start`{:class="block3events"} block.

![Character sprite](images/giga-sprite.png)

```blocks3
<br />- هنگامی که پرچم
+ هنگام دریافت [شروع v]
تنظیم [شماره 1 V] به (انتخاب تصادفی (2) به (12))
مجموعه [شماره 2 V] به (انتخاب تصادفی (2) به (12) )
بپرسید (پیوستن (شماره 1) (پیوستن به [x] (شماره 2))) و صبر کنید
اگر <(پاسخ) = ((شماره 1) * (شماره 2))> سپس
    می گویند [بله! :)) برای (2) ثانیه
دیگر
    می گویند [nope :(] برای (2) ثانیه
پایان
```

\--- /وظیفه \---

\--- task \---

Click the green flag, and then click on the new 'Play' button to test whether it works. You should see that the game doesn't start before you click on the button.

\--- /task \---

Can you see that the timer starts when the green flag is clicked, instead of when the game starts?

![Timer has started](images/brain-timer-bug.png)

\--- task \---

Can you change the code for the timer so that the timer starts when the player clicks on the button?

\--- /وظیفه \---

\--- وظیفه \---

Add code to your button sprite so that the button shows again at the end of each game.

![Button sprite](images/button-sprite.png)

```blocks3
    زمانی که من [پایان v]
    نمایش را دریافت می کنم
```

\--- /task \---

\--- task \---

Test the 'Play' button by playing a couple of games. The button should show at the end of each game.

To test the game more quickly, you can change the value of `time`{:class="block3variables"} so that each game is only a few seconds long.

![Stage](images/stage-sprite.png)

```blocks3
    تنظیم [زمان V] به [10]
```

\--- /task \---

\--- task \---

You can change how the button looks when the mouse pointer hovers over it.

![Button](images/button-sprite.png)

```blocks3
    زمانی که پرچم روی
    کلیک نمایش داده می شود
    برای همیشه
    اگر <touching (mouse-pointer v)?> سپس
        تنظیم [fisheye v] به (30)
    دیگر
        تنظیم [اثر fisheye v] به (0)
    پایان
    پایان
```

![screenshot](images/brain-fisheye.png)

\--- /task \---