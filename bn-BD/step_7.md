## গ্রাফিক্স যোগ করুন

মুহূর্তে, চরিত্র পরী ঠিক বলেছেন `হ্যাঁ! :)` বা `নং :(` প্লেয়ারের উত্তরের জন্য। প্লেয়ারটিকে তাদের উত্তরটি সঠিক বা ভুল কিনা তা জানার জন্য কিছু গ্রাফিক্স যোগ করুন।

\--- কাজ \---

'ফলাফল' নামক একটি নতুন স্প্রাইট তৈরি করুন এবং এটি একটি 'টিক / চেক' এবং একটি 'ক্রস' পরিচ্ছদ দিন।

![টিক এবং ক্রস পোশাক সঙ্গে স্প্রাইট](images/brain-result.png)

\--- /কাজ \---

\--- কাজ \---

পরিবর্তে, এটা খেলোয়াড় কিছু বলার অপেক্ষা রাখে না, যাতে আপনার চরিত্র পরী এর কোড পরিবর্তন করুন `সম্প্রচার`{: শ্রেণি = "block3events"} বার্তা 'সঠিক' অথবা 'ভুল'।

![অক্ষর স্প্রাইট](images/giga-sprite.png)

```blocks3
যদি <(উত্তর) = ((সংখ্যা 1) * (সংখ্যা 2))> তারপর

- বলুন [হ্যাঁ! :)] জন্য (2) সেকেন্ড
+ সম্প্রচার (সঠিক v)
অন্য
- বলুন [নাপ :(] জন্য (2) সেকেন্ড
+ সম্প্রচার (ভুল v)
শেষ
```

\--- /কাজ \---

\--- কাজ \---

এখন আপনি এই বার্তাগুলি `দেখানোর জন্য`{: class = "block3looks"} টি 'টিক' বা 'ক্রস' পরিচ্ছদ ব্যবহার করতে পারেন। নিম্নলিখিত ফলাফলটি 'ফলাফল' স্প্রাইটে যুক্ত করুন:

![ফলাফল স্প্রাইট](images/result-sprite.png)

```blocks3
    যখন আমি [সঠিক v]
    সুইচ পরিচ্ছদ পেতে (টিক ভ)
    শো
    অপেক্ষা (1) সেকেন্ড
    আমি যখন পাই তখন

    
 গোপন করুন [ভুল v]
    সুইচ পরিচ্ছদ (ক্রস ভ)
    শো
    অপেক্ষা (1) সেকেন্ড



    লুকান যখন পতাকাটি 
 লুকিয়ে থাকে
```

\--- /কাজ \---

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
অ্যানিমেশন নির্ধারণ
শো
অপেক্ষা (1) সেকেন্ড
লুকান
```

\--- /task \---

\--- task \---

Make sure you have removed the `show`{:class="block3looks"} and `hide`{:class="block3looks"} blocks below **both** of the `switch costume`{:class="block3looks"} blocks.

Then add the `animate`{:class="block3myblocks"} block below both of the `switch costume`{:class="block3looks"} blocks. Your code should now look like this:

![Result sprite](images/result-sprite.png)

```blocks3
    যখন আমি [সঠিক v]
    সুইচ পরিচ্ছদটি পেতে (টিক v)
    অ্যানিমেশন :: কাস্টম

    পাই তখন [ভুল v]
    সুইচ পরিচ্ছদ (ক্রস ভ)
    অ্যানিমেশন :: কাস্টম
```

\--- /task \---

Because of the custom `animate`{:class="block3myblocks"} block, you now only need to make one change to your code if you want to show the 'Result' sprite's costumes a longer or shorter time.

\--- task \---

Change your code so that the 'tick' or 'cross' costumes display for 2 seconds.

\--- /কাজ \---

\--- task \---

Instead of `showing`{:class="block3looks"} and `hiding`{:class="block3looks"} the 'tick' or 'cross' costumes, you could change your `animate`{:class="block3myblocks"} block so that the costumes fade in.

![Result sprite](images/result-sprite.png)

```blocks3
    অ্যানিমেট নির্ধারণ
    সেট [ভূত ভী] প্রভাব থেকে (100)
    শো
    পুনরাবৃত্তি (25)
        পরিবর্তন [ভূত ভী] প্রভাব দ্বারা প্রভাবিত (-4)
    শেষ
    লুকান
```

\--- /task \---

Can you improve the animation of the 'tick' or 'cross' graphics? You could add code to make the costumes fade out as well, or you could use other cool effects:

![screenshot](images/brain-effects.png)