## टाइमर जोड़ें

\--- task \--- `समय`{:class="block3variables"} नाम के एक नये चर की मदद से स्टेज पर एक उलटी गिनती वाला टाइमर बनाएं। टाइमर 30 सेकंड से शुरू होना चाहिए और 0 सेकंड तक गिना जाना चाहिए।

![Stage sprite](images/stage-sprite.png)

\--- hints \--- \--- hint \---

एक ` चर ` {"class =" block3variables "} बनाएं, इसे 'समय' नाम दें, और इसका मान ` 30 ` निर्धारित करें।

फिर 30 सेकंड के अंदर ` समय ` {:class="block3variables"} को 0 तक गिनने का कोड जोड़ें। ऐसा करने के लिए, हर `1` सेकंड में ` समय ` {:class="block3variables"} में से `1` घटाएँ, और इसे तब तक दोहराएं जब तक ` समय `{:class="block3variables"} `0` के बराबर नही हो जाता।

\--- /hint \--- \--- hint \--- ये है वो ब्लॉक जिसकी आपको आवश्यकता है:

```blocks3
दोहराते रहें जब तक < >

अंत

(1) सेकंड प्रतीक्षा करें

(1) se [समय v] बदलें

(समय)

जब झंडा क्लिक किया

<() = ()>

[समय v] को [0] स्थिर करें
```

\--- /hint \--- \--- hint \--- यहाँ दिखाया गया है कि आपका कोड कैसा दिखना चाहिए:

```blocks3
जब ध्वज पर क्लिक किया
[समय v] को [30] स्थिर करें
दोहराएं जब तक <(समय) = (0)>
    (1) सेकंड प्रतीक्षा करें
    (-1) से [समय v] बदलें 
अंत
```

\--- /hint \--- \--- /hints \---

\--- /task \---

\--- task \---

एक ` प्रसारण ` {:class="block3control"} बनायें जो 'अंत' संदेश भेजता है। `प्रसारण`{:class="block3control"} एक लाउड्स्पीकर पर घोषणा की तरह है: यह आपके सभी स्प्राइट्स द्वारा सुना जा सकता है। Add the `broadcast`{:class="block3control"} block to the end of the timer code so that the code will send and 'end' message when the `time`{:class="block3variables"} has counted down to `0`.

![Stage sprite](images/stage-sprite.png)

```blocks3
    broadcast (end v)
```

\--- /task \---

\--- task \--- Select your character sprite and add some code so that the sprite `stops the other scripts`{:class="block3control"} when it receives the `end`{:class="block3control"} message.

![Giga sprite](images/giga-sprite.png)

```blocks3
    when I receive [end v]
    stop [other scripts in sprite v]
```

\--- /task \---

\--- task \---

Test your game again. It should continue to ask questions until the timer has counted down to 0.

\--- /task \---