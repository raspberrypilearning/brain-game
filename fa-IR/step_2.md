## ایجاد سوالات

شما با ایجاد سوالات تصادفی که بازیکن باید پاسخگو باشد شروع می شود.

\--- وظیفه \---

پروژه جدید خراش را باز کنید.

**Online:** open a new online Scratch project at [rpf.io/scratch-new](http://rpf.io/scratch-new){:target="_blank"}.

**آفلاین:** پروژه جدید را در ویرایشگر آفلاین باز کنید.

اگر شما نیاز به دانلود و نصب ویرایشگر آفلاین Scratch دارید، می توانید آن را در [rpf.io/scratchoff](http://rpf.io/scratchoff){: target = "_ blank"} پیدا کنید.

\--- /وظیفه \---

\--- task \---

Add a character sprite and a backdrop for your game. You can choose any you like! Here's an example:

![screenshot](images/brain-setting.png)

\--- /task \---

\--- task \---

Make sure you have your character sprite selected. Create two new variables, called `number 1`{:class="block3variables"} and `number 2`{:class="block3variables"}, to store the numbers for the quiz questions.

![screenshot](images/giga-sprite.png)

![screenshot](images/brain-variables.png)

[[[generic-scratch3-add-variable]]]

\--- /وظیفه \---

\--- task \---

Add code to your character sprite to set both of the `variables`{:class="block3variables"} to a `random`{:class="block3operators"} number between 2 and 12.

![screenshot](images/giga-sprite.png)

```blocks3
هنگامی که پرچم روی دکمه
تنظیم [شماره 1 V] به (انتخاب تصادفی (2) به (12))
مجموعه [شماره 2 V] به (انتخاب تصادفی (2) به (12))
```

\--- /task \---

\--- task \---

Add code to `ask`{:class="block3sensing"} the player for the answer, and then `say for 2 seconds`{:class="block3looks"} whether the answer was right or wrong:

![screenshot](images/giga-sprite.png)

```blocks3
وقتی پرچم با کلیک بر روی
تنظیم [شماره 1 V] به (انتخاب تصادفی (2) به (12))
مجموعه [شماره 2 V] به (انتخاب تصادفی (2) به (12))

+ درخواست (پیوستن (شماره 1) (پیوستن به [x] (شماره 2))) و منتظر
+ اگر <(پاسخ) = ((شماره 1) * (شماره 2))> سپس
+ می گویند [بله! :)) برای (2) ثانیه
+ دیگر
+ می گویند [no :(] برای (2) ثانیه
+ پایان
```

\--- /task \---

\--- task \---

Test your project twice: answer one question correctly, and the other incorrectly.

\--- /task \---

\--- task \---

Add a `forever`{:class="block3control"} loop around this code, so that the game asks the player lots of questions in a row.

\--- hints \---

\--- hint \---

You need to add a `forever`{:class="block3control"} block, and put all of the code except the `when flag clicked`{:class="block3control"} block into it.

\--- /hint \---

\--- hint \---

Here is the block you need:

```blocks3
برای همیشه
پایان
```

\--- /hint \---

\--- hint \---

Here is what your code should look like:

```blocks3
هنگامی که پرچم روی

+ برای همیشه کلیک کنید
    مجموعه [شماره 1 V] به (انتخاب تصادفی (2) به (12))
    مجموعه [شماره 2 V] به (انتخاب تصادفی (2) به (12))
    درخواست (پیوستن 1) (پیوستن به [x] (شماره 2))) و منتظر
    اگر <(پاسخ) = ((شماره 1) * (شماره 2))> سپس
        می گویند [بله! :) برای (2) ثانیه
    دیگر
        می گویند [no :(] برای (2) ثانیه
    پایان
پایان
```

\--- /hint \---

\--- /hints \---

\--- /task \---