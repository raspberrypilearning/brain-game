## ग्राफिक्स जोडें

फिलहाल, स्प्राइट खिलाड़ी के जवाब देने पर बस `yes! :)` या `no :(` कहता है। खिलाड़ी को यह बताने के लिए, कि उनका उत्तर सही या गलत है, कुछ ग्राफिक्स जोड़ें।

\--- task \---

'Result' नामक एक नया स्प्राइट बनाएँ, और इसे 'tick/check' और 'cross' पोशाक दें।

![स्प्राइट tick और cross पोशाक के साथ](images/brain-result.png)

\--- /task \---

\--- task \---

अपना स्प्राइट कोड बदलें ताकि खिलाड़ी को कुछ कहने के बजाय, यह 'correct' या 'wrong' संदेशों को `broadcasts`{:class="block3events"}।

![पात्र स्प्राइट](images/giga-sprite.png)

```blocks3
if <(answer) = ((number 1)*(number 2))> then

- say [yes! :)] for (2) seconds
+ broadcast (correct v)
else
- say [nope :(] for (2) seconds
+ broadcast (wrong v)
end
```

\--- /task \---

\--- task \---

अब आप इन संदेशों का उपयोग करके 'tick' या 'cross' पोशाक `show`{:class="block3looks"}। निम्नलिखित कोड को 'Result' स्प्राइट में जोड़ें:

![परिणाम स्प्राइट](images/result-sprite.png)

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

\--- /task \---

\--- task \---

फिर से अपने खेल का परीक्षण करें। जब भी आप किसी प्रश्न का सही उत्तर देते हैं तो आपको टिक, और जब भी आप गलत उत्तर देते हैं तो क्रॉस दिखाई देना चाहिए!

![सही के लिए टिक, गलत उत्तर के लिए क्रॉस](images/brain-test-answer.png)

\--- /task \---

क्या आप देख सकते हैं कि `when I receive correct`{:class="block3events"} और `when I receive wrong`{:class="block3events"} का कोड लगभग एक जैसा ही है?

इसलिए आप एक कस्टम ब्लॉक बनाने जा रहे हैं ताकि आप अपना कोड अधिक आसानी से बदल सकेंगे।

\--- task \---

'Result' स्प्राइट को चुने। फिर `My blocks`{:class="block3myblocks"} पर क्लिक करें, और फिर **Make a block** पर। एक नया ब्लॉक बनाएं और इसका नाम `animate` {:class="block3myblocks"} रखें।

![परिणाम स्प्राइट](images/result-sprite.png)

![एक एनिमेट नामक ब्लाक बनाएँ](images/brain-animate-function.png)

\--- /task \---

\--- task \---

'Result' स्प्राइट को `show`{:class="block3looks"} और `hide`{:class="block3looks"} वाला कोड को `animate`{:class="block3looks"} वाले ब्लाक में ले जाएं:

![परिणाम स्प्राइट](images/result-sprite.png)

```blocks3
define animate
show
wait (1) seconds
hide
```

\--- /task \---

\--- task \---

निश्चित करें कि आपने **both** `switch costume`{:class="block3looks"} वाले ब्लॉक्स के नीचे से `show`{:class="block3looks"} और `hide`{:class="block3looks"} वाले ब्लॉक्स हटा दियें हैं:

फिर दोनों `switch costume`{:class="block3looks"} ब्लॉक्स के नीचे `animate`{:class="block3myblocks"} ब्लाक जोड़ें। आपका कोड अब इस तरह दिखना चाहिए:

![परिणाम स्प्राइट](images/result-sprite.png)

```blocks3
    when I receive [correct v]
    switch costume to (tick v)
    animate:: custom

    when I receive [wrong v]
    switch costume to (cross v)
    animate:: custom
```

\--- /task \---

कस्टम `animate`{:class="block3myblocks"} ब्लॉक की वजह से, अब आपको सिर्फ एक चीज़ बदलना है अगर आप 'Result' स्प्राइट की पोषक को थोड़ा समय ज़्यादा या काम दिखाना चाहते है।

\--- task \---

अपना कोड बदलें ताकि 'tick' या 'cross' पोशाक 2 सेकंड के लिए प्रदर्शित हो।

\--- /task \---

\--- task \---

'Tick' और 'cross' पोशाक `showing`{:class="block3looks"} और `hiding`{:class="block3looks"} की बजाए आप अपने `animate`{:class="block3myblocks"} ब्लाक को बदल सकते हैं ताकि पोशाक फीकी पड़ते हुए विलुप्त हो जाए।

![परिणाम स्प्राइट](images/result-sprite.png)

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

क्या आप 'tick' या 'cross' ग्राफिक्स का एनीमेशन सुधर सकते हैं? आप पोशाक को फीका पड़ते हुए छिपने का कोड भी जोड़ सकते हैं, या आप अन्य आकर्षिक प्रभावों का उपयोग कर सकते हैं:

![स्क्रीनशॉट](images/brain-effects.png)