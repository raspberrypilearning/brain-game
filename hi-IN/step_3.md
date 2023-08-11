## टाइमर जोड़ें

\--- task \---

`time`{:class="block3variables"} नाम के एक नये चर की मदद से स्टेज पर एक उलटी गिनती वाला टाइमर बनाएं। टाइमर 30 सेकंड से शुरू होना चाहिए और 0 सेकंड तक गिना जाना चाहिए।

![स्टेज स्प्राइट](images/stage-sprite.png)

\--- hints \---

\--- hint \---

एक `variable`{:class=" block3variables"} बनाएं, इसे 'time' नाम दें, और इसका मान `30` निर्धारित करें।

फिर 30 सेकंड के अंदर `time`{:class="block3variables"} को 0 तक गिनने का कोड जोड़ें। ऐसा करने के लिए, हर `1` सेकंड में `time`{:class="block3variables"} में से `1` घटाएँ, और इसे तब तक दोहराएं जब तक `time`{:class="block3variables"} `0` के बराबर नही हो जाता।

\--- /hint \---

\--- hint \---

इन ब्लॉक्स की आपको आवश्यकता होगी:

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

यहाँ दिखाया गया है कि आपका कोड कैसा दिखना चाहिए:

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

एक `broadcast`{:class="block3control"} बनाएं जो 'end' (अंत) संदेश भेजता है। एक `broadcast`{:class="block3control"} लाउडस्पीकर पर एक घोषणा की तरह है: इसे आपके सभी sprite (स्प्राइट्स) द्वारा सुना जा सकता है। `broadcast`{:class="block3control"} ब्लाक टाइमर कोड के अंत में जोड़ें ताकि जब `time`{:class="block3variables"} `0` तक गिना जा चुका हो तब कोड एक 'end' संदेश भेजेगा।

![स्टेज स्प्राइट](images/stage-sprite.png)

```blocks3
    broadcast (end v)
```

\--- /task \---

\--- task \---

अपना पात्र स्प्राइट चुने और फिर कोड जोड़े ताकि वह स्प्राइट `stops the other scripts`{:class="block3control"} जब वह स्प्राइट को `end`{:class="block3control"} सन्देश मिल जाता है।

![गीगा स्प्राइट](images/giga-sprite.png)

```blocks3
    when I receive [end v]
    stop [other scripts in sprite v]
```

\--- /task \---

\--- task \---

अपने खेल का फिर से परीक्षण करें। जब तक टाइमर 0 तक नहीं गिना जाता है तब तक यह सवाल पूछना जारी रखना चाहिए।

\--- /task \---