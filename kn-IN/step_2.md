## ಪ್ರಶ್ನೆಗಳನ್ನು ರಚಿಸಿ

ನೀವು ರಚಿಸುವ ಮೂಲಕ ಪ್ರಾರಂಭಿಸಲಿದ್ದೀರಿ ರ್ಯಾಂಡಮ್ ಆಟಗಾರನು ಉತ್ತರಿಸಬೇಕಾದ ಪ್ರಶ್ನೆಗಳು.

\--- task \---

ಹೊಸದನ್ನು ತೆರೆಯಿರಿ Scratch ಯೋಜನೆ.

**ಆನ್‌ಲೈನ್:** ಹೊಸ ಆನ್‌ಲೈನ್ ತೆರೆಯಿರಿ Scratch ನಲ್ಲಿ ಯೋಜನೆ [rpf.io/scratch-new](http://rpf.io/scratch-new){:target="_blank"}.

**ಆಫ್‌ಲೈನ್:** ಹೊಸ ಯೋಜನೆಯನ್ನು ತೆರೆಯಿರಿ offline editor.

ನಿಮಗೆ ಅಗತ್ಯವಿದ್ದರೆ ಡೌನ್ಲೋಡ್ ಮತ್ತು ಇನ್ಸ್ಟಾಲ್ Scratch offline editor, ನೀವು ಅದನ್ನು ಕಾಣಬಹುದು [rpf.io/scratchoff](http://rpf.io/scratchoff){:target="_blank"}.

\--- /task \---

\--- task \---

ನಿಮ್ಮ ಆಟಕ್ಕೆ ಕ್ಯಾರೆಕ್ಟರ್ sprite ಮತ್ತು ಹಿನ್ನೆಲೆ ಸೇರಿಸಿ. ನೀವು ಇಷ್ಟಪಡುವದನ್ನು ನೀವು ಆಯ್ಕೆ ಮಾಡಬಹುದು! ಒಂದು ಉದಾಹರಣೆ ಇಲ್ಲಿದೆ:

![screenshot](images/brain-setting.png)

\--- /task \---

\--- task \---

ನಿಮ್ಮ ಕ್ಯಾರೆಕ್ಟರ್ sprite ಅನ್ನು ನೀವು ಆಯ್ಕೆ ಮಾಡಿಕೊಂಡಿದ್ದೀರಿ ಎಂದು ಖಚಿತಪಡಿಸಿಕೊಳ್ಳಿ. ಎರಡು ಹೊಸದನ್ನು ರಚಿಸಿ variables, ಎಂದು ಕರೆಯಲಾಗುತ್ತದೆ `number 1`{:class="block3variables"} ಮತ್ತು `number 2`{:class="block3variables"}, ರಸಪ್ರಶ್ನೆ ಪ್ರಶ್ನೆಗಳಿಗೆ ಸಂಖ್ಯೆಗಳನ್ನು ಸಂಗ್ರಹಿಸಲು.

![screenshot](images/giga-sprite.png)

![screenshot](images/brain-variables.png)

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- task \---

ಎರಡನ್ನೂ ಹೊಂದಿಸಲು ನಿಮ್ಮ ಕ್ಯಾರೆಕ್ಟರ್ spriteಗೆ ಕೋಡ್ ಸೇರಿಸಿ `variables`{:class="block3variables"} ಗೆ `random`{:class="block3operators"} 2 ಮತ್ತು 12 ರ ನಡುವಿನ ಸಂಖ್ಯೆ.

![screenshot](images/giga-sprite.png)

```blocks3
when flag clicked
set [number 1 v] to (pick random (2) to (12))
set [number 2 v] to (pick random (2) to (12))
```

\--- /task \---

\--- task \---

ಇದಕ್ಕೆ ಕೋಡ್ ಸೇರಿಸಿ `ask`{:class="block3sensing"} ಉತ್ತರಕ್ಕಾಗಿ ಆಟಗಾರ, ತದನಂತರ `say for 2 seconds`{:class="block3looks"} ಉತ್ತರ ಸರಿ ಅಥವಾ ತಪ್ಪಾಗಿರಲಿ:

![screenshot](images/giga-sprite.png)

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

ನಿಮ್ಮ ಯೋಜನೆಯನ್ನು ಎರಡು ಬಾರಿ ಪರೀಕ್ಷಿಸಿ: ಒಂದು ಪ್ರಶ್ನೆಗೆ ಸರಿಯಾಗಿ ಉತ್ತರಿಸಿ, ಮತ್ತು ಇನ್ನೊಂದು ತಪ್ಪಾಗಿ ಉತ್ತರಿಸಿ.

\--- /task \---

\--- task \---

ಒಂದು ಸೇರಿಸಿ `forever`{:class="block3control"} ಈ ಕೋಡ್‌ನ ಸುತ್ತಲೂ ಲೂಪ್ ಮಾಡಿ, ಇದರಿಂದಾಗಿ ಆಟವು ಆಟಗಾರನಿಗೆ ಸತತವಾಗಿ ಸಾಕಷ್ಟು ಪ್ರಶ್ನೆಗಳನ್ನು ಕೇಳುತ್ತದೆ.

\--- hints \---

\--- hint \---

ನೀವು ಸೇರಿಸಬೇಕಾಗಿದೆ `forever`{:class="block3control"} ಬ್ಲಾಕ್, ಮತ್ತು ಹೊರತುಪಡಿಸಿ ಎಲ್ಲಾ ಕೋಡ್ ಅನ್ನು ಹಾಕಿ `when flag clicked`{:class="block3control"} ಬ್ಲಾಕ್ ಅದರೊಳಗೆ.

\--- /hint \---

\--- hint \---

ನಿಮಗೆ ಅಗತ್ಯವಿರುವ ಬ್ಲಾಕ್ ಗಳು ಇಲ್ಲಿವೆ:

```blocks3
forever
end
```

\--- /hint \---

\--- hint \---

ನಿಮ್ಮ ಕೋಡ್ ಹೇಗಿರಬೇಕು ಎಂಬುದು ಇಲ್ಲಿದೆ:

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