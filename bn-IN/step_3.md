## একটি টাইমার যোগ করুন

\--- task \---

`time`{:class="block3variables"} নামে একটি নতুন ভেরিয়েবলের সাহায্যে স্টেজের একটি কাউন্টডাউন টাইমার তৈরি করুন} টাইমারটি 30 সেকেন্ডে শুরু হয়েকমতে কমতে ০ সেকেন্ড অবধি চলবে.

![Stage sprite](images/stage-sprite.png)

\--- hints \---

\--- hint \---

একটি `ভেরিয়েবল`তৈরি করুন</code>{:class="block3variables"}, এটিকে 'সময়' বলুন এবং এর মান `30</0>সেট করুন.</p>

<p>এরপর কোড <code>time`{:class="block3variables"} যোগ করুন ৩০ সেকেন্ড থেকে ০ পর্যন্ত গণনা করার জন্য. এই কাজের জন্য, বিয়োগ করুন `1` থেকে `time`{:class="block3variables"} every `1` second এবং `time`{:class="block3variables"} equals `0`হওয়া পর্যন্ত এই পুনরাবৃত্তি করুন.

\--- /hint \---

\--- hint \---

আপনার যেগুলি ব্লকগুলি দরকার তা এখানে রয়েছে:

```blocks3
repeat until < >

end

wait (1) seconds

change [time v] by (1)

(time)

when flag clicked

<() = ()>

set [time v] to [0]
```

\--- /hint \---

\--- hint \---

নতুন কোডটি দেখতে এমন হওয়া উচিত:

```blocks3
when flag clicked
set [time v] to [30]
repeat until <(time) = (0)>
    wait (1) seconds
    change [time v] by (-1)
end
```

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

একটি `broadcast`{:class="block3control"} কোড তৈরি করুন: যা 'end;বার্তাটি 'দেয়. একটি `broadcast`{:class="block3control"} লাউডস্পিকারের মাধ্যমে ঘোষণার মতো: এটি আপনার সমস্ত sprite স্প্রিট শুনতে পাবে. টাইমার কোডের শেষে `broadcast`{:class="block3control"}` ব্লক যুক্ত করুন যাতে কোডটি <code>time`{:class="block3variables"} কোডটি গণনা করে <0>0</code> হলে 'end; বার্তা প্রেরণ করবে.

![Stage sprite](images/stage-sprite.png)

```blocks3
    broadcast (end v)
```

\--- /task \---

\--- task \---

আপনার ক্যারেক্টার sprite নির্বাচন করুন এবং কিছু কোড যুক্ত করুন যাতে sprite `অন্যান্য স্ক্রিপ্টগুলি` বন্ধ করে দেয় যখন এটি `end`{:class="block3control"} বার্তাটি পায়.

![Giga sprite](images/giga-sprite.png)

```blocks3
    when I receive [end v]
    stop [other scripts in sprite v]
```

\--- /task \---

\--- task \---

আপনার গেমটি আবার পরীক্ষা করুন। টাইমার 0 পর্যন্ত গণনা না করা অবধি প্রশ্ন জিজ্ঞাসা করা অব্যাহত থাকা উচিত.

\--- /task \---