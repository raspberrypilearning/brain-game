## প্রশ্ন তৈরি করুন

খেলোয়াড়কে উত্তর দিতে হবে এমন এলোমেলো প্রশ্ন তৈরি করার মধ্য দিয়ে আপনি গেম শুরু করুন.

\--- task \---

একটি নতুন Scratch প্রকল্প খুলুন.

**Online:** open a new online Scratch project at [rpf.io/scratch-new](https://rpf.io/scratch-new){:target="_blank"}.

**Offline:** offline editor এ একটি নতুন প্রজেক্ট খুলুন.

If you need to download and install the Scratch offline editor, you can find it at [rpf.io/scratchoff](https://rpf.io/scratchoff){:target="_blank"}.

\--- /task \---

\--- task \---

আপনার গেমের জন্য একটি ক্যারেক্টার sprite এবং একটি ব্যাকড্রপ যুক্ত করুন। আপনি আপনার পছন্দ মত যে কোন চয়ন করতে পারেন! এখানে একটি উদাহরণ:

![screenshot](images/brain-setting.png)

\--- /task \---

\--- task \---

আপনার ক্যারেক্টার sprite নির্বাচন করা আছে তা নিশ্চিত করুন।. কুইজের প্রশ্নের জন্য সংখ্যাগুলি সংরক্ষণ করতে, দুটি নতুন ভেরিয়েবল তৈরি করুন, `number 1`{:class="block3variables"} এবং `number 2`{:class="block3variables"}.

![screenshot](images/giga-sprite.png)

![screenshot](images/brain-variables.png)

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- task \---

আপনার ক্যারেক্টার sprite এর সাথে কোড যোগ করুন যাতে উভয় `variables`{:class="block3variables"} `random`{:class="block3operators"} 2 এবং 12 এর মধ্যে থাকে.

![screenshot](images/giga-sprite.png)

```blocks3
when flag clicked
set [number 1 v] to (pick random (2) to (12))
set [number 2 v] to (pick random (2) to (12))
```

\--- /task \---

\--- task \---

দুটি কোড যোগ করুন এক তো প্লেয়ার কে উত্তর দেওয়ার জন্য `ask`{:class="block3sensing"} আর একটা হলো কিছু সময় বাদে, ধরুন ২ সেকেন্ড, </code>{:class="block3looks"} বলার জন্য যে উত্তর টি ঠিক ভুল:

![screenshot](images/giga-sprite.png)

```blocks3
when flag clicked
set [number 1 v] to (pick random (2) to (12))
set [number 2 v] to (pick random (2) to (12))

+ ask (join (number 1)(join [ x ] (number 2))) and wait
+ if <(answer) = ((number 1)*(number 2))> then
+ say [yes! :)] for (2) seconds
+ else
+ say [no :(] for (2) seconds
+ end
```

\--- /task \---

\--- task \---

আপনার প্রকল্পটি দু'বার পরীক্ষা করুন: একটি প্রশ্নের সঠিক উত্তর দিন, এবং অন্যটি ভুল করে।.

\--- /task \---

\--- task \---

আপনার কোড এর এর চারপাশে এই `forever`{:class="block3control"} লুপ টি ব্যবহার করুন, যাতে গেম এ প্লেয়ার কে অনেক প্রশ্ন জিজ্ঞাসা করা হয়.

\--- hints \---

\--- hint \---

এবার এই ব্লক টি `forever`{:class="block3control"} যোগ করুন এবং এই `when flag clicked`{:class="block3control"}কোড টি বাদে অন্যান্য শোন্ কোড যোগ করুন.

\--- /hint \---

\--- hint \---

আপনার যে blocks দরকার তা এখানে রয়েছে:

```blocks3
forever
end
```

\--- /hint \---

\--- hint \---

এখানে আপনার কোড টি এইরকম দেখতে হওয়া উচিত:

```blocks3
when flag clicked

+ forever
    set [number 1 v] to (pick random (2) to (12))
    set [number 2 v] to (pick random (2) to (12))
    ask (join (number 1)(join [ x ] (number 2))) and wait
    if <(answer) = ((number 1)*(number 2))> then
        say [yes! :)] for (2) seconds
    else
        say [no :(] for (2) seconds
    end
end
```

\--- /hint \---

\--- /hints \---

\--- /task \---