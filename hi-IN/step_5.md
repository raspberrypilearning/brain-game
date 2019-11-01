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

जब खिलाड़ी ध्वज पर क्लिक करता है तो नया कोड 'खेलें' बटन स्प्राइट शो करता है। When the player clicks on the button sprite, the sprite hides and then broadcasts a message that other sprites can react to.

At the moment, the character sprite starts asking questions when the player clicks the flag. Change your game's code so that character sprite starts asking questions when it receives the 'start' `broadcast`{:class="block3events"}.

\--- task \--- Select your character sprite and, in its code section, replace the `when flag clicked`{:class="block3events"} block with a `when I receive start`{:class="block3events"} block.

![पात्र स्प्राइट](images/giga-sprite.png)

```blocks3
<br />- when flag clicked
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

\--- /task \---

\--- task \---

Click the green flag, and then click on the new 'Play' button to test whether it works. You should see that the game doesn't start before you click on the button.

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