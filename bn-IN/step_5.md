## একাধিক গেম

এখন আপনি একটি 'প্লে' বোতাম যুক্ত করতে যাচ্ছেন, যাতে প্লেয়ারটি আপনার গেমটি বহুবার খেলতে পারে.

--- task ---

একটি নতুন 'play' বোতাম sprite তৈরি করুন যা নতুন গেম শুরু করতে খেলোয়াড়কে ক্লিক করতে হবে.

আপনি নিজেই sprite আঁকতে পারেন, বা লাইব্রেরি থেকে একটিsprite নিয়ে এডিট করে নিতে পারেন.

![Picture of the play button](images/brain-play.png)

--- /task ---

--- task ---

আপনার বাটন sprite এ এই কোড যুক্ত করুন:

![Button sprite](images/button-sprite.png)

```blocks3
    when flag clicked
    show

    when this sprite clicked
    hide
    broadcast (start v)
```

--- /task ---

নতুন কোডটিতে আরও একটি `broadcast`{:class="block3events"} ব্লক অন্তর্ভুক্ত রয়েছে, যা 'স্টার্ট' বার্তা প্রেরণ করে.

প্লেয়ার যখন পতাকাটিতে ক্লিক করে তখন নতুন কোডটি 'play' বোতামের sprite প্রদর্শন করে. প্লেয়ারটি বোতামের sprite এ ক্লিক করলে sprite টি লুকায় এবং তারপরে এমন একটি বার্তা সম্প্রচার করে যাতে অন্যান্য sprite গুলি প্রতিক্রিয়া জানাতে পারে.

এই মুহুর্তে, প্লেয়ার পতাকাটিতে ক্লিক করলে ক্যারেক্টার sprite প্রশ্ন জিজ্ঞাসা শুরু করে. আপনার গেমের কোডটি পরিবর্তন করুন যাতে ক্যারেক্টার sprite প্রশ্ন জিজ্ঞাসা শুরু করে যখন এটি 'start' `broadcast`{:class="block3events"} নির্দেশ পায়.

--- task ---

Select your character sprite and, in its code section, replace the `when flag clicked`{:class="block3events"} block with a `when I receive start`{:class="block3events"} block.

![Character sprite](images/giga-sprite.png)

```blocks3
- when flag clicked
+ when I receive [start v]
set [number 1 v] to (pick random (2) to (12))
set [number 2 v] to (pick random (2) to (12))
ask (join (number 1)(join [ x ] (number 2))) and wait
if <(answer) = ((number 1)*(number 2))> then
    say [yes! :)] for (2) seconds
else
    say [nope :(] for (2) seconds
end
```

--- /task ---

--- task ---

সবুজ পতাকাটি ক্লিক করুন এবং তারপরে এটি 'কাজ করে' কিনা তা পরীক্ষা করতে নতুন 'play' বোতামে ক্লিক করুন। আপনার দেখতে হবে যে আপনি বোতামটি ক্লিক করার আগে গেমটি শুরু হচ্ছে না।.

--- /task ---

আপনি কি দেখতে পাচ্ছেন যে খেলাটি শুরু হওয়ার পরিবর্তে সবুজ পতাকাটি ক্লিক করা হলে টাইমার শুরু হয়?

![Timer has started](images/brain-timer-bug.png)

--- task ---

আপনি কি টাইমারটির জন্য কোডটি পরিবর্তন করতে পারেন যাতে প্লেয়ার বোতামে ক্লিক করলে টাইমার শুরু হয়?

--- /task ---

--- task ---

আপনার বোতাম স্প্রাইটে কোড যুক্ত করুন যাতে প্রতিটি গেমের শেষে বোতামটি আবার দেখায়.

![Button sprite](images/button-sprite.png)

```blocks3
    when I receive [end v]
    show
```

--- /task ---

--- task ---

বেশ কয়েকটি গেম খেলে 'Play' বোতামটি পরীক্ষা করুন। প্রতিটি গেমের শেষে বোতামটি প্রদর্শন করা উচিত.

গেমটি আরও দ্রুত পরীক্ষা করতে, আপনি `time`{:class="block3variables"} এর মান পরিবর্তন করতে পারেন, যাতে প্রতিটি গেম মাত্র কয়েক সেকেন্ড দীর্ঘ হয়.

![Stage](images/stage-sprite.png)

```blocks3
    set [time v] to [10]
```

--- /task ---

--- task ---

মাউস পয়েন্টার এটির উপরে চলে গেলে আপনি বোতামটি কীভাবে দেখায় তা পরিবর্তন করতে পারেন.

![Button](images/button-sprite.png)

```blocks3
    when flag clicked
    show
    forever
    if <touching (mouse-pointer v)?> then
        set [fisheye v] effect to (30)
    else
        set [fisheye v] effect to (0)
    end
    end
```

![screenshot](images/brain-fisheye.png)

--- /task ---