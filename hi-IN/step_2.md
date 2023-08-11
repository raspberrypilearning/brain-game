## प्रश्न बनाना

आइए हम खिलाड़ी द्वारा उत्तर देने के लिए अनियमित प्रश्न बनाने से शुरू करते हैं।

\--- task \---

एक नया Scratch प्रोजेक्ट खोलें।

**Online:** open a new online Scratch project at [rpf.io/scratch-new](https://rpf.io/scratch-new){:target="_blank"}.

**ऑफ़लाइन:** ऑफ़लाइन एडिटर में एक नया प्रोजेक्ट खोलें।

If you need to download and install the Scratch offline editor, you can find it at [rpf.io/scratchoff](https://rpf.io/scratchoff){:target="_blank"}.

\--- /task \---

\--- task \---

अपने खेल के लिए पात्र स्प्राइट और एक पृष्ठभूमि जोड़ें। आप अपनी पसंद का कोई भी चुन सकते हैं! यहाँ एक उदाहरण है:

![स्क्रीनशॉट](images/brain-setting.png)

\--- /task \---

\--- task \---

सुनिश्चित करें कि आपका पात्र स्प्राइट चुना हुआ है। प्रश्नोत्तरी (क्विज़) के सवालों के लिए संख्याओं को संग्रहीत करने के लिए, दो नए चर (variables/वेरिएबल्स), ` number 1` {:class="block3variables"} और `number 2`{:class="block3variables"} बनाएं।

![स्क्रीनशॉट](images/giga-sprite.png)

![स्क्रीनशॉट](images/brain-variables.png)

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- task \---

दोनों `variables`{:class="block3variables"} का मान 2 और 12 के बीच एक `random`{:class="block3operators"} संख्या निर्धारित करने के लिए कोड लिखें।

![स्क्रीनशॉट](images/giga-sprite.png)

```blocks3
when flag clicked
set [number 1 v] to (pick random (2) to (12))
set [number 2 v] to (pick random (2) to (12))
```

\--- /task \---

\--- task \---

खिलाड़ी से उत्तर पूछने के लिए `ask`{:class="block3sensing"} और बताने के लिए कि उत्तर सही था या नही, `say for 2 seconds`{:class="block3looks"} कोड जोड़ें।

![स्क्रीनशॉट](images/giga-sprite.png)

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

अपने प्रोजेक्ट का दो बार परीक्षण करें: एक बार प्रश्न का सही उत्तर दें, और दूसरी बार गलत।

\--- /task \---

\--- task \---

इस कोड के इर्द-गिर्द `forever`{:class="block3control"} लूप जोड़ें, ताकि खेल एक शृंखला में खिलाड़ी से बहुत सारे प्रश्न पूछ सके।

\--- hints \---

\--- hint \---

आपको एक `forever`{:class="block3control"} ब्लाक जोड़ना है, और `when flag is clicked`{:class="block3control"} ब्लाक को छोड़कर बाक़ी सारा कोड इसमें रखना है।

\--- /hint \---

\--- hint \---

इन ब्लॉक्स की आपको आवश्यकता होगी:

```blocks3
forever
end
```

\--- /hint \---

\--- hint \---

आपका कोड ऐसा दिखना चाहिए:

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