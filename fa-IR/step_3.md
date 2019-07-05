## تایمر را اضافه کنید

\--- وظیفه \--- یک تایمر شمارش معکوس در مرحله با کمک یک متغیر جدید به نام `time`{: class = "block3variables"} ایجاد کنید. تایمر باید در 30 ثانیه شروع شود و به صفر ثانیه برسد.

![صحنه صحنه](images/stage-sprite.png)

\--- نکات \--- \--- \--- اشاره

یک متغیر ``: class = "block3variables" را ایجاد کنید، آن را 'time' نامگذاری کنید و مقدار آن را به `30`.

سپس کد را برای شمارش `زمان`{: class = "block3variables"} تا 30 ثانیه اضافه کنید. برای انجام این کار `1` از `بار`{: class = "block3variables"} تفریق کنید هر `1` ثانیه و این تا `بار تکرار شود`{: class = "block3variables"} برابر با `0`.

\--- / \--- اشاره \--- \--- اشاره در اینجا بلوک شما نیاز دارید:

```blocks3
تکرار تا < >

پایان

صبر کردن (1) ثانیه

تغییر [زمان V] توسط (1)

(زمان)

هنگامی که پرچم کلیک

<() = ()>

تنظیم [زمان V] به [0]
```

\--- / hint \--- \--- hint \--- این کد جدید شما باید شبیه باشد:

```blocks3
زمانی که پرچم روی دکمه
تنظیم شد [زمان V] به [30]
تکرار تا <(زمان) = (0)>
    صبر کنید (1) ثانیه
    تغییر [زمان V] توسط (-1)
پایان
```

\--- / اشاره \--- \--- / نکات \---

\--- /وظیفه \---

\--- وظیفه \---

ایجاد یک پخش ``:: class = "block3control"} که پایان پیام را ارسال می کند. `پخش`{: class = "block3control"} مانند اعلامیه بر روی یک بلندگو است: می توان آن را با تمام یاران خود شنیده کرد. اضافه کردن `پخش`{: class = "block3control"} بلوک به انتهای کد تایمر به طوری که کد ارسال خواهد شد و پیام "پایان" زمانی که `زمان`{: class = "block3variables"} تا `شمارش 0`.

![صحنه صحنه](images/stage-sprite.png)

```blocks3
    پخش (پایان V)
```

\--- /وظیفه \---

\--- کار \--- کاراکتر کاراکتر خود را انتخاب کنید و برخی از کد را اضافه کنید تا فیلد `دیگر اسکریپتها را متوقف کند`{: class = "block3control"} هنگام دریافت پیام `end`{: class = "block3control"} .

![جیگایی](images/giga-sprite.png)

```blocks3
    وقتی که من [پایان v]
    توقف [اسکریپت های دیگر در sprite v]
```

\--- /وظیفه \---

\--- وظیفه \---

دوباره بازی تست کنید باید ادامه دهید تا سؤال شود تا زمانیکه تایمر به صفر برسد.

\--- /وظیفه \---