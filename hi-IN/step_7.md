## ग्राफिक्स जोडें

फिलहाल, पात्र स्प्राइट खिलाड़ी के जवाब देने पर बस ` हाँ! :) ` या ` नहीं :( ` कहता है। खिलाड़ी को यह बताने के लिए कुछ ग्राफिक्स जोड़ें कि उनका उत्तर सही है या गलत।

\--- task \---

'परिणाम' नामक एक नया स्प्राइट बनाएँ, और इसे 'टिक/चेक' और 'क्रॉस' पोशाक दें।

![Sprite with tick and cross costumes](images/brain-result.png)

\--- /task \---

\--- task \---

अपना पात्र स्प्राइट कोड बदलें ताकि खिलाड़ी को कुछ कहने के बजाय, यह 'सही' या 'गलत' संदेशों को `प्रसारित करें`{:class="block3events"}।

![पात्र स्प्राइट](images/giga-sprite.png)

```blocks3
अगर <(उत्तर) = ((संख्या 1) * (संख्या 2))> तो

- कहो [हाँ! :)] (2) सेकंड के लिए
+ प्रसारित करें (सही v)
अन्यथा
- कहो [नहीं :(] (2) सेकंड के लिए
+ प्रसारित करें (गलत v)
अंत
```

\--- /task \---

\--- task \---

अब आप इन संदेशों का उपयोग करके 'टिक' या 'क्रॉस' पोशाक `दिखाएँ` {:class="block3looks"}। निम्नलिखित कोड को 'परिणाम' स्प्राइट में जोड़ें:

![Result sprite](images/result-sprite.png)

```blocks3
    जब मुझे प्राप्त हो [सही v]
    कास्टयूम को (टिक v) से बदलें
    दिखाएँ
    (1) सेकंड प्रतीक्षा करें
    छिपाएँ
   

    जब मुझे प्राप्त हो [गलत v]
   कास्टयूम को (क्रॉस v) से बदलें
    दिखाएँ
    (1) सेकंड प्रतीक्षा करें
    छिपाएँ

    जब झंडा क्लिक किया
    छिपाएँ
```

\--- /task \---

\--- task \--- Test your game again. You should see the tick whenever you answer a question correctly, and the cross whenever you answer incorrectly!

![Tick for correct, cross for wrong answer](images/brain-test-answer.png)

\--- /task \---

Can you see that the code for `when I receive correct`{:class="block3events"} and `when I receive wrong`{:class="block3events"} is nearly identical?

So you can change your code more easily, you are going to create a custom block.

\--- task \---

Select the 'Result' sprite. Then click on `My Blocks`{:class="block3myblocks"}, and then on **Make a Block**. Create a new block and call it `animate`{:class="block3myblocks"}.

![Result sprite](images/result-sprite.png)

![Create a block called animate](images/brain-animate-function.png)

\--- /task \---

\--- task \--- Move the code to `show`{:class="block3looks"} and `hide`{:class="block3looks"} the 'Result' sprite into the `animate`{:class="block3myblocks"} block:

![Result sprite](images/result-sprite.png)

```blocks3
define animate
show
wait (1) seconds
hide
```

\--- /task \---

\--- task \--- Make sure you have removed the `show`{:class="block3looks"} and `hide`{:class="block3looks"} blocks below **both** of the `switch costume`{:class="block3looks"} blocks.

Then add the `animate`{:class="block3myblocks"} block below both of the `switch costume`{:class="block3looks"} blocks. Your code should now look like this:

![Result sprite](images/result-sprite.png)

```blocks3
    when I receive [correct v]
    switch costume to (tick v)
    animate:: custom

    when I receive [wrong v]
    switch costume to (cross v)
    animate:: custom
```

\--- /task \---

Because of the custom `animate`{:class="block3myblocks"} block, you now only need to make one change to your code if you want to show the 'Result' sprite's costumes a longer or shorter time.

\--- task \---

Change your code so that the 'tick' or 'cross' costumes display for 2 seconds.

\--- /task \---

\--- task \--- Instead of `showing`{:class="block3looks"} and `hiding`{:class="block3looks"} the 'tick' or 'cross' costumes, you could change your `animate`{:class="block3myblocks"} block so that the costumes fade in.

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

\--- /task \---

Can you improve the animation of the 'tick' or 'cross' graphics? You could add code to make the costumes fade out as well, or you could use other cool effects:

![स्क्रीनशॉट](images/brain-effects.png)