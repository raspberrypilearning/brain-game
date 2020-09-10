## গ্রাফিক্স যুক্ত করুন

এখনো পর্যন্ত ক্যারেক্টর sprite প্লেয়ার এর দেওয়া উত্তরে কেবলমাত্র হ্যা বা না বলে `yes! :)` or `no :(`. কিছু গ্রাফিক্স যোগ করুন যাতে প্লেয়ার বুঝতে পারে তার দেওয়া উত্তর সঠিক না ভুল.

--- task ---

'রেজাল্ট' নামে একটি নতুন sprite তৈরি করুন এবং এটিকে একটি 'টিক / চেক' এবং একটি 'ক্রস' কস্টিউম দিন.

![Sprite with tick and cross costumes](images/brain-result.png)

--- /task ---

--- task ---

আপনার ক্যারেক্টর sprite এর কোডটি এমন পরিবর্তন করুন যাতে প্লেয়ারকে কিছু বলার পরিবর্তে`broadcasts`{:class="block3events"} 'এটি ব্রডকাস্ট করে 'সঠিক' অথবা 'ভুল'.

![Character sprite](images/giga-sprite.png)

```blocks3
if <(answer) = ((number 1)*(number 2))> then

- say [yes! :)] for (2) seconds
+ broadcast (correct v)
else
- say [nope :(] for (2) seconds
+ broadcast (wrong v)
end
```

--- /task ---

--- task ---

এখন আপনি এই বার্তাগুলি ব্যবহার করতে পারেন টিক 'বা' ক্রস কস্টিউম দেখানোর জন্য `show`{:class="block3looks"}. 'নিচের কোড টি রেজাল্ট sprite এ যোগ করুন:

![Result sprite](images/result-sprite.png)

```blocks3
    when I receive [correct v]
    switch costume to (tick v)
    show
    wait (1) seconds
    hide

    when I receive [wrong v]
    switch costume to (cross v)
    show
    wait (1) seconds
    hide

    when flag clicked
    hide
```

--- /task ---

--- task ---

আপনার গেমটি আবার পরীক্ষা করুন। আপনি যখনই কোনও প্রশ্নের সঠিক উত্তর দিয়েছেন তখনই আপনার 'টিক'টি দেখা উচিত, এবং যখনই আপনি ভুল উত্তর দেন তখন ক্রস দেখা উচিত!

![Tick for correct, cross for wrong answer](images/brain-test-answer.png)

--- /task ---

আপনি কি দেখতে পারছেন যে কোড `when I receive correct`{:class="block3events"} এবং `when I receive wrong`{:class="block3events"} প্রায় এক ই রকম দেখতে?

সুতরাং আপনি আপনার কোডটি আরও সহজেই পরিবর্তন করতে পারবেন, আপনি একটি কাস্টম ব্লক তৈরি করতে যাচ্ছেন।.

--- task ---

'রেজাল্ট' sprite নির্বাচন করুন. এরপর ক্লিক করুন `My Blocks`{:class="block3myblocks"}, এবং তারপরে ক্লিক করুন **Make a Block**. একটি নতুন ব্লক তৈরি করুন এবং এটিকে নাম দিন `animate`{:class="block3myblocks"}.

![Result sprite](images/result-sprite.png)

![Create a block called animate](images/brain-animate-function.png)

--- /task ---

--- task ---

এই কোড টি `show`{:class="block3looks"} and `hide`{:class="block3looks"} এবং রেজাল্ট স্প্রিট কে সরান `animate`{:class="block3myblocks"} ব্লক পর্যন্ত:

![Result sprite](images/result-sprite.png)

```blocks3
define animate
show
wait (1) seconds
hide
```

--- /task ---

--- task ---

নিশ্চিত করুন যে আপনি এই `show`{:class="block3looks"} এবং `hide`{:class="block3looks"} ব্লক দুটি কে এমনভাবে সরিয়েছেন যে তারা **both** of the `switch costume`{:class="block3looks"} ব্লকের নিচে থাকে.

তারপর যোগ করুন `animate`{:class="block3myblocks"} ব্লক টিকে পরবর্তী দুটি ব্লক এর নিচে `switch costume`{:class="block3looks"}. আপনার কোড টি এইরকম দেখতে হওয়া উচিত:

![Result sprite](images/result-sprite.png)

```blocks3
    when I receive [correct v]
    switch costume to (tick v)
    animate:: custom

    when I receive [wrong v]
    switch costume to (cross v)
    animate:: custom
```

--- /task ---

কাস্টম `animate`{:class="block3myblocks"} ব্লক রাখার জন্য, আপনি যদি এখন 'result' sprite এর কস্টিউম টি দীর্ঘ বা স্বল্প সময়ের জন্য দেখাতে চান তবে আপনার কোডটিতে একটি পরিবর্তন করতে হবে।.

--- task ---

আপনার কোডটি পরিবর্তন করুন যাতে 'টিক্' বা 'ক্রস' কস্টিউম 2 সেকেন্ডের জন্য প্রদর্শিত হয়।.

--- /task ---

--- task ---

'টিক্' বা 'ক্রস' কস্টিউম দেখানো `showing`{:class="block3looks"} বা লুকানোর `hiding`{:class="block3looks"} পরিবর্তে কোড ব্লক পরিবর্তন করতে পারেন `animate`{:class="block3myblocks"} যাতে কস্টিউম গুলি ম্লান হয়ে যায় পরিস্থিতি অনুযায়ী.

![Result sprite](images/result-sprite.png)

```blocks3
    define animate
    set [ghost v] effect to (100)
    show
    repeat (25)
        change [ghost v] effect by (-4)
    end
    hide
```

--- /task ---

আপনি কি 'টিক' বা 'ক্রস' গ্রাফিক্সের অ্যানিমেশনটি উন্নত করতে পারেন? কস্টিউম গুলি ম্লান হয়ে যাওয়ার জন্য আপনি কোড যুক্ত করতে পারেন, বা আপনি অন্য সুন্দর ইফেক্ট গুলি ব্যবহার করতে পারেন:

![screenshot](images/brain-effects.png)