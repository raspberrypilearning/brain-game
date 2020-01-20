## প্রশ্ন তৈরি করুন

আপনি প্লেয়ার উত্তর দিতে চান যে এলোমেলো প্রশ্ন তৈরি করে শুরু করতে যাচ্ছি।

\--- কাজ \---

একটি নতুন স্ক্র্যাচ প্রকল্প খুলুন।

**Online:** open a new online Scratch project at [rpf.io/scratch-new](http://rpf.io/scratch-new){:target="_blank"}.

**অফলাইন:** অফলাইন সম্পাদকটিতে একটি নতুন প্রকল্প খুলুন।

আপনি যদি স্ক্র্যাচ অফলাইন সম্পাদক ডাউনলোড এবং ইনস্টল করতে চান তবে আপনি এটি [rpf.io/scratchoff](http://rpf.io/scratchoff)এ পাবেন: {target = "_ blank"}।

\--- /কাজ \---

\--- task \---

Add a character sprite and a backdrop for your game. You can choose any you like! Here's an example:

![screenshot](images/brain-setting.png)

\--- /task \---

\--- task \---

Make sure you have your character sprite selected. Create two new variables, called `number 1`{:class="block3variables"} and `number 2`{:class="block3variables"}, to store the numbers for the quiz questions.

![screenshot](images/giga-sprite.png)

![screenshot](images/brain-variables.png)

[[[generic-scratch3-add-variable]]]

\--- /কাজ \---

\--- task \---

Add code to your character sprite to set both of the `variables`{:class="block3variables"} to a `random`{:class="block3operators"} number between 2 and 12.

![screenshot](images/giga-sprite.png)

```blocks3
যখন পতাকা
সেট [সংখ্যা 1 ভি] ক্লিক করে (র্যান্ডম (2) থেকে (12))
সেট [সংখ্যা 2 ভি] থেকে (র্যান্ডম (2) থেকে (12) বাছাই করুন)
```

\--- /task \---

\--- task \---

Add code to `ask`{:class="block3sensing"} the player for the answer, and then `say for 2 seconds`{:class="block3looks"} whether the answer was right or wrong:

![screenshot](images/giga-sprite.png)

```blocks3
যখন পতাকা ক্লিক
সেট [1 নম্বর বনাম] এ (র্যান্ডম (2) এর (12) বাছাই)
সেট [NUMBER 2 বনাম] এ (বাছাই র্যান্ডম (2) এর (12))

+ + জিজ্ঞাসা করুন (1 নম্বর যোগদানের () ([x] (সংখ্যা 2) যোগ দিন) এবং অপেক্ষা করুন
+ যদি <(উত্তর) = ((সংখ্যা 1) * (সংখ্যা 2))> তারপর
+ বলুন [হ্যাঁ! :)] জন্য (2) সেকেন্ড
+ অন্য
+ বলুন [না :(] (2) সেকেন্ড
+ শেষ
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
চিরতরে
শেষ
```

\--- /hint \---

\--- hint \---

Here is what your code should look like:

```blocks3
যখন পতাকাটি

+ সর্বদা
    সেট [সংখ্যা 1 ভি] তে ক্লিক করে (র্যান্ডম (2) থেকে (12))
    সেট [সংখ্যা 2 ভি] থেকে (র্যান্ডম (2) থেকে (12) বাছাই করুন)
    জিজ্ঞাসা করুন (যোগ দিন (যোগ করুন 1) (যোগদানের [X] (নম্বর 2))) এবং অপেক্ষা করুন
    যদি <(উত্তর) = ((নম্বর 1) * (সংখ্যা 2))> তারপর
        বলে [হ্যাঁ! :)] জন্য (2) সেকেন্ড
    অন্য
        বলুন [না :(] (2) সেকেন্ড
    শেষ
শেষ
```

\--- /hint \---

\--- /hints \---

\--- /task \---