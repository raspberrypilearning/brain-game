## ಗ್ರಾಫಿಕ್ಸ್ ಸೇರಿಸಿ

ಈ ಸಮಯದಲ್ಲಿ, ಕ್ಯಾರೆಕ್ಟರ್ sprite ಕೇವಲ ಹೇಳುತ್ತದೆ `yes! :)` or `no :(` ಆಟಗಾರನ ಉತ್ತರಗಳಿಗೆ. ಅವರ ಉತ್ತರ ಸರಿಯಾಗಿದೆಯೆ ಅಥವಾ ತಪ್ಪಾಗಿದೆಯೇ ಎಂದು ಆಟಗಾರನಿಗೆ ತಿಳಿಸಲು ಕೆಲವು ಗ್ರಾಫಿಕ್ಸ್ ಸೇರಿಸಿ.

\--- task \---

ಹೊಸ sprite ಅನ್ನು ರಚಿಸಿ 'Result', ಮತ್ತು ಅದನ್ನು ನೀಡಿ 'tick/check' ಮತ್ತು 'cross' costume.

![Sprite with tick and cross costumes](images/brain-result.png)

\--- /task \---

\--- task \---

ನಿಮ್ಮ ಅಕ್ಷರ ಸ್ಪ್ರೈಟ್‌ನ ಕೋಡ್ ಅನ್ನು ಬದಲಾಯಿಸಿ ಇದರಿಂದ ಆಟಗಾರನಿಗೆ ಏನನ್ನಾದರೂ ಹೇಳುವ ಬದಲು ಅದನ್ನು ಮಾಡಿ `broadcasts`{:class="block3events"} ಸಂದೇಶಗಳು 'correct' ಅಥವಾ 'wrong'.

![Character sprite](images/giga-sprite.png)

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

ಈಗ ನೀವು ಈ ಸಂದೇಶಗಳನ್ನು ಬಳಸಬಹುದು `show`{:class="block3looks"} 'tick ಅಥವಾ 'cross' costume. ಈ ಕೆಳಗಿನ ಕೋಡ್ ಅನ್ನು ಸೇರಿಸಿ 'Result' sprite:

![Result sprite](images/result-sprite.png)

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

ನಿಮ್ಮ ಆಟವನ್ನು ಮತ್ತೆ ಪರೀಕ್ಷಿಸಿ. ನೀವು ನೋಡಬೇಕು tick ನೀವು ಪ್ರಶ್ನೆಗೆ ಸರಿಯಾಗಿ ಉತ್ತರಿಸಿದಾಗಲೆಲ್ಲಾ, ಮತ್ತು cross ನೀವು ತಪ್ಪಾಗಿ ಉತ್ತರಿಸುವಾಗಲೆಲ್ಲಾ!

![Tick for correct, cross for wrong answer](images/brain-test-answer.png)

\--- /task \---

ಇದಕ್ಕಾಗಿ ಕೋಡ್ ಅನ್ನು ನೀವು ನೋಡಬಹುದೇ? `when I receive correct`{:class="block3events"} ಮತ್ತು `when I receive wrong`{:class="block3events"} ಬಹುತೇಕ ಒಂದೇ?

ಆದ್ದರಿಂದ ನೀವು ನಿಮ್ಮ ಕೋಡ್ ಅನ್ನು ಹೆಚ್ಚು ಸುಲಭವಾಗಿ ಬದಲಾಯಿಸಬಹುದು, ನೀವು ರಚಿಸಲು ಹೊರಟಿದ್ದೀರಿ custom ಬ್ಲಾಕ್.

\--- task \---

ಆಯ್ಕೆಮಾಡಿ 'Result' ಸ್ಪ್ರೈಟ್. ನಂತರ click(ಕ್ಲಿಕ್) ಮಾಡಿ `My Blocks`{:class="block3myblocks"}, ತದನಂತರ **Make a Block**. ಹೊಸ ಬ್ಲಾಕ್ ರಚಿಸಿ ಮತ್ತು ಅದನ್ನು ಕರೆ ಮಾಡಿ `animate`{:class="block3myblocks"}.

![Result sprite](images/result-sprite.png)

![Create a block called animate](images/brain-animate-function.png)

\--- /task \---

\--- task \---

ಕೋಡ್ ಅನ್ನು ಸರಿಸಿ `show`{:class="block3looks"} ಮತ್ತು `hide`{:class="block3looks"} 'Result' sprite `animate`{:class="block3myblocks"} ಬ್ಲಾಕ್:

![Result sprite](images/result-sprite.png)

```blocks3
define animate
show
wait (1) seconds
hide
```

\--- /task \---

\--- task \---

ನೀವು ತೆಗೆದುಹಾಕಿದ್ದೀರಿ ಎಂದು ಖಚಿತಪಡಿಸಿಕೊಳ್ಳಿ `show`{:class="block3looks"} ಮತ್ತು `hide`{:class="block3looks"} ಬ್ಲಾಕ್ಸ್ ಗಳು below **both** of the `switch costume`{:class="block3looks"} ಬ್ಲಾಕ್ಸ್ ಗಳು.

ನಂತರ ಸೇರಿಸಿ `animate`{:class="block3myblocks"} ಬ್ಲಾಕ್ಸ್ ಎರಡೂ ಕೆಳಗೆ `switch costume`{:class="block3looks"} ಬ್ಲಾಕ್ಸ್ ಗಳು. ನಿಮ್ಮ ಕೋಡ್ ಈಗ ಈ ರೀತಿ ಇರಬೇಕು:

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

ಕಾರಣ ಏನೆಂದರೆ custom `animate`{:class="block3myblocks"} ಬ್ಲಾಕ್ಸ್,ನೀವು ತೋರಿಸಲು ಬಯಸಿದರೆ ನೀವು ಈಗ ನಿಮ್ಮ ಕೋಡ್‌ಗೆ ಒಂದು ಬದಲಾವಣೆಯನ್ನು ಮಾಡಬೇಕಾಗಿದೆ 'Result' sprite's costumes ದೀರ್ಘ ಅಥವಾ ಕಡಿಮೆ ಸಮಯ.

\--- task \---

ನಿಮ್ಮ ಕೋಡ್ ಅನ್ನು ಬದಲಾಯಿಸಿ ಇದರಿಂದ 'tick' ಅಥವಾ 'cross' costumes display 2 ಸೆಕೆಂಡುಗಳ ಕಾಲ.

\--- /task \---

\--- task \---

ಬದಲಾಗಿ `showing`{:class="block3looks"} and `hiding`{:class="block3looks"} 'tick' ಅಥವಾ 'cross' costumes,ನಿಮ್ಮ ಬದಲಾಯಿಸಬಹುದು `animate`{:class="block3myblocks"} ನಿರ್ಬಂಧಿಸಿ ಆದ್ದರಿಂದ costumes ಫೇಡ್ ಇನ್.

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

ನೀವು ಅನಿಮೇಷನ್ ಅನ್ನು ಸುಧಾರಿಸಬಹುದೇ 'tick' ಅಥವಾ 'cross' ಗ್ರಾಫಿಕ್ಸ್? costumes ಮಸುಕಾಗುವಂತೆ ಮಾಡಲು ನೀವು ಕೋಡ್ ಅನ್ನು ಸೇರಿಸಬಹುದು, ಅಥವಾ ನೀವು ಇತರ ತಂಪಾದ ಪರಿಣಾಮಗಳನ್ನು ಬಳಸಬಹುದು:

![screenshot](images/brain-effects.png)