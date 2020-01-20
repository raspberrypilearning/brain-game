## اضافه کردن گرافیک

در حال حاضر، شخصیت ادعا فقط می گوید `بله! :)` یا `no :(` به پاسخ بازیکن. اضافه کردن برخی از گرافیک به اجازه بازیکن می دانم که آیا پاسخ آنها صحیح و یا نادرست است.

\--- وظیفه \---

یک قاتل جدید به نام «نتیجه» ایجاد کنید و یک تیک / چک و یک صحنه «صلیب» بدهید.

![قهرمان با لباس تیک و کراس](images/brain-result.png)

\--- /وظیفه \---

\--- وظیفه \---

رمز عبور شخصی خود را تغییر دهید به طوری که، به جای اینکه چیزی را به بازیکن بگوید، `پخش`{: class = "block3events"} پیام "صحیح" یا "اشتباه" است.

![امضا شخصیت](images/giga-sprite.png)

```blocks3
اگر <(جواب) = ((شماره 1) * (شماره 2))> سپس

- می گویند [بله! (2) ثانیه
+ پخش (درست V)
دیگر
- می گویند [nope :(] برای (2) ثانیه پخش
+ (اشتباه V)
پایان
```

\--- /وظیفه \---

\--- وظیفه \---

حالا شما می توانید از این پیام ها به `نشان دهید`{: class = "block3looks"} صحنه "تیک" یا "صلیب". کد زیر را به فیلد "نتیجه" اضافه کنید:

![نتیجه جستجو](images/result-sprite.png)

```blocks3
    هنگامی که من دریافت می کنم [صحیح V]
    لباس سوئیچ به (تیک V)
    نشان می دهد
    صبر کنید (1) ثانیه
    پنهان

    زمانی که من دریافت [اشتباه V]
    سوئیچ لباس (عبور V)
    نشان می دهد
    صبر کنید (1) ثانیه
    پنهان

    زمانی که پرچم
    پنهان را کلیک کرد
```

\--- /وظیفه \---

\--- task \---

Test your game again. You should see the tick whenever you answer a question correctly, and the cross whenever you answer incorrectly!

![Tick for correct, cross for wrong answer](images/brain-test-answer.png)

\--- /task \---

Can you see that the code for `when I receive correct`{:class="block3events"} and `when I receive wrong`{:class="block3events"} is nearly identical?

So you can change your code more easily, you are going to create a custom block.

\--- task \---

Select the 'Result' sprite. Then click on `My Blocks`{:class="block3myblocks"}, and then on **Make a Block**. Create a new block and call it `animate`{:class="block3myblocks"}.

![Result sprite](images/result-sprite.png)

![Create a block called animate](images/brain-animate-function.png)

\--- /task \---

\--- task \---

Move the code to `show`{:class="block3looks"} and `hide`{:class="block3looks"} the 'Result' sprite into the `animate`{:class="block3myblocks"} block:

![Result sprite](images/result-sprite.png)

```blocks3
تعریف کردن
نمایش
انتظار (1) ثانیه
پنهان کردن
```

\--- /task \---

\--- task \---

Make sure you have removed the `show`{:class="block3looks"} and `hide`{:class="block3looks"} blocks below **both** of the `switch costume`{:class="block3looks"} blocks.

Then add the `animate`{:class="block3myblocks"} block below both of the `switch costume`{:class="block3looks"} blocks. Your code should now look like this:

![Result sprite](images/result-sprite.png)

```blocks3
    هنگامی که من دریافت می کنم [صحیح v]
    سوئیچ لباس به (تیک V)
    تحریک و خوشنویسی :: سفارشی

    هنگامی که من دریافت [اشتباه v]
    سوئیچ لباس به (تقسیم V)
    تحریک و تشجیع :: سفارشی
```

\--- /task \---

Because of the custom `animate`{:class="block3myblocks"} block, you now only need to make one change to your code if you want to show the 'Result' sprite's costumes a longer or shorter time.

\--- task \---

Change your code so that the 'tick' or 'cross' costumes display for 2 seconds.

\--- /وظیفه \---

\--- task \---

Instead of `showing`{:class="block3looks"} and `hiding`{:class="block3looks"} the 'tick' or 'cross' costumes, you could change your `animate`{:class="block3myblocks"} block so that the costumes fade in.

![Result sprite](images/result-sprite.png)

```blocks3
    تعریف تعریف
    تنظیم [اثر روح v] به (100)
    نمایش
    تکرار (25)
        تغییر [روح v] اثر توسط (-4)
    پایان
    پنهان
```

\--- /task \---

Can you improve the animation of the 'tick' or 'cross' graphics? You could add code to make the costumes fade out as well, or you could use other cool effects:

![screenshot](images/brain-effects.png)