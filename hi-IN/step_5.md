## मल्टीप्ल गेम्ज़

अब आप एक 'खेलें' बटन जोड़ने जा रहे हैं, ताकि खिलाड़ी आपके खेल को कई बार खेल सके।

\--- task \--- एक नया 'खेलें' बटन स्प्राइट बनाएं जो खिलाड़ी को नया गेम शुरू करने के लिए क्लिक करने की आवश्यकता हो।

आप स्वयं स्प्राइट को बना सकते हैं, या लाइब्रेरी से स्प्राइट को संपादित कर सकते हैं।

![Picture of the play button](images/brain-play.png)

\--- /task \---

\--- task \--- इस कोड को अपने बटन स्प्राइट में जोड़ें:

![Button sprite](images/button-sprite.png)

```blocks3
    जब ध्वज क्लिक किया
    दिखाएँ

    जब यह स्प्राइट क्लिक किया
    छिपाएँ
    प्रसारण (प्रारंभ v)
```

\--- /task \---

नए कोड में एक और `प्रसारण` {:class="block3events"} ब्लॉक शामिल है, जो 'प्रारंभ' संदेश भेजता है।

जब खिलाड़ी ध्वज पर क्लिक करता है तो नया कोड 'खेलें' बटन स्प्राइट शो करता है। जब खिलाड़ी बटन स्प्राइट पर क्लिक करता है, तो स्प्राइट छिप जाता है और फिर एक संदेश प्रसारित करता है जिस पर अन्य स्प्राइट प्रतिक्रिया कर सकते हैं।

अब, खिलाड़ी के झंडे पर क्लिक करते ही चरित्र स्प्राइट सवाल पूछना शुरू कर देता है। अपने गेम के कोड को बदलें ताकि जब चरित्र स्प्राइट को 'शुरू करें' `प्रसारित करें`{:class="block3events"} प्राप्त हो तो वो सवाल पूछना शुरू करे।

\--- task \--- अपने चरित्र स्प्राइट का चयन करें और, इसके कोड अनुभाग में, `जब झंडा क्लिक किया`{:class="block3events"} ब्लॉक को `जब मुझे शुरू करें प्राप्त हो`{:class="block3events"} ब्लाक से बदल दें।

![पात्र स्प्राइट](images/giga-sprite.png)

```blocks3
<br />- जब झंडा क्लिक किया
+ जब मुझे प्राप्त हो [शुरू करें v ]
[संख्या 1 v] को (यादृच्छिक (2) से (12) के बीच चुने) स्थिर करें 
[संख्या 2 v] को (यादृच्छिक (2) से (12) के बीच चुने) स्थिर करें
पूछें (जोड़ें (संख्या 1) (जोड़ें [x] (संख्या 2))) और प्रतीक्षा करें 
यदि <(उत्तर) = ((संख्या 1) * (संख्या 2))> तो
   कहें [हाँ! :)] (2) सेकंड के लिए
अन्यथा
   कहें [नहीं :(] (2) सेकंड के लिए
अंत
```

\--- /task \---

\--- task \---

हरे झंडे पर क्लिक करें, और फिर यह जाँच करने के लिए नए 'खेलें' बटन पर क्लिक करें कि यह काम कर रहा है। आपको यह दिखना चाहिए कि बटन पर क्लिक करने से पहले खेल शुरू नहीं होता है।

\--- /task \---

Can you see that the timer starts when the green flag is clicked, instead of when the game starts?

![Timer has started](images/brain-timer-bug.png)

\--- task \---

Can you change the code for the timer so that the timer starts when the player clicks on the button?

\--- /task \---

\--- task \--- Add code to your button sprite so that the button shows again at the end of each game.

![Button sprite](images/button-sprite.png)

```blocks3
    when I receive [end v]
    show
```

\--- /task \---

\--- task \---

Test the 'Play' button by playing a couple of games. The button should show at the end of each game.

To test the game more quickly, you can change the value of `time`{:class="block3variables"} so that each game is only a few seconds long.

![Stage](images/stage-sprite.png)

```blocks3
    set [time v] to [10]
```

\--- /task \---

\--- task \--- You can change how the button looks when the mouse pointer hovers over it.

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

![स्क्रीनशॉट](images/brain-fisheye.png) \--- /task \---