## ಬಹು ಆಟಗಳು

ಈಗ ನೀವು ಒಂದು ಸೇರಿಸಲು ಹೊರಟಿದ್ದೀರಿ 'Play' button, ಆದ್ದರಿಂದ ಆಟಗಾರನು ನಿಮ್ಮ ಆಟವನ್ನು ಸಾಕಷ್ಟು ಬಾರಿ ಆಡಬಹುದು.

--- task ---

ಹೊಸದನ್ನು ರಚಿಸಿ 'Play' button sprite ಆಟಗಾರನಿಗೆ ಅಗತ್ಯವಿರುವ click ಹೊಸ ಆಟವನ್ನು ಪ್ರಾರಂಭಿಸಲು.

ನೀವು sprite ಅನ್ನು ನೀವೇ ಸೆಳೆಯಬಹುದು, ಅಥವಾ library(ಲೈಬ್ರರಿಯಿಂದ) sprite ಅನ್ನು ಸಂಪಾದಿಸಿ.

![Picture of the play button](images/brain-play.png)

--- /task ---

--- task ---

ಈ ಕೋಡ್ ಅನ್ನು ನಿಮ್ಮೊಂದಿಗೆ ಸೇರಿಸಿ button sprite:

![Button sprite](images/button-sprite.png)

```blocks3
    when flag clicked
    show

    when this sprite clicked
    hide
    broadcast (start v)
```

--- /task ---

ಹೊಸ ಕೋಡ್ ಇನ್ನೊಂದನ್ನು ಒಳಗೊಂಡಿದೆ `broadcast`{:class="block3events"} ಬ್ಲಾಕ್, ಅದು ಸಂದೇಶವನ್ನು ಕಳುಹಿಸುತ್ತದೆ 'start'.

ಹೊಸ ಕೋಡ್ ಆಟಗಾರನು ಧ್ವಜದ ಮೇಲೆ ಕ್ಲಿಕ್ ಮಾಡಿದಾಗ 'play' button sprite ಪ್ರದರ್ಶನವನ್ನು ಮಾಡುತ್ತದೆ. ಆಟಗಾರನು button sprite ಮೇಲೆ ಕ್ಲಿಕ್ ಮಾಡಿದಾಗ, sprite ಮರೆಮಾಡುತ್ತದೆ ಮತ್ತು ನಂತರ ಇತರ spries ಪ್ರತಿಕ್ರಿಯಿಸಬಹುದಾದ ಸಂದೇಶವನ್ನು ಪ್ರಸಾರ ಮಾಡುತ್ತದೆ.

ಈ ಸಮಯದಲ್ಲಿ, ಆಟಗಾರ ಧ್ವಜವನ್ನು ಕ್ಲಿಕ್ ಮಾಡಿದಾಗ ಅಕ್ಷರ sprite ಪ್ರಶ್ನೆಗಳನ್ನು ಕೇಳಲು ಪ್ರಾರಂಭಿಸುತ್ತಾನೆ. ನಿಮ್ಮ ಆಟದ ಕೋಡ್ ಅನ್ನು ಬದಲಾಯಿಸಿ ಇದರಿಂದ ಅಕ್ಷರ sprite ಅದನ್ನು ಸ್ವೀಕರಿಸಿದಾಗ ಪ್ರಶ್ನೆಗಳನ್ನು ಕೇಳಲು ಪ್ರಾರಂಭಿಸುತ್ತದೆ 'start' `broadcast`{:class="block3events"}.

--- task ---

ನಿಮ್ಮ ಅಕ್ಷರ ಸ್ಪ್ರೈಟ್ ಅನ್ನು ಆಯ್ಕೆ ಮಾಡಿ ಮತ್ತು ಅದರ ಕೋಡ್ ವಿಭಾಗದಲ್ಲಿ, ಬದಲಿಸಿ `when flag clicked`{:class="block3events"} ಬ್ಲಾಕ್ ಒಂದು `when I receive start`{:class="block3events"} ಬ್ಲಾಕ್.

![Character sprite](images/giga-sprite.png)

```blocks3
- when flag clicked
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

--- /task ---

--- task ---

ಕ್ಲಿಕ್ ಮಾಡಿ green flag, ತದನಂತರ ಹೊಸದನ್ನು ಕ್ಲಿಕ್ ಮಾಡಿ 'Play' button ಅದು ಕಾರ್ಯನಿರ್ವಹಿಸುತ್ತದೆಯೇ ಎಂದು ಪರೀಕ್ಷಿಸಲು. ನೀವು button ಕ್ಲಿಕ್ ಮಾಡುವ ಮೊದಲು ಆಟವು ಪ್ರಾರಂಭವಾಗುವುದಿಲ್ಲ ಎಂದು ನೀವು ನೋಡಬೇಕು.

--- /task ---

Timer(ಟೈಮರ್) ಪ್ರಾರಂಭವಾದಾಗ ನೀವು ನೋಡಬಹುದು green flag ಕ್ಲಿಕ್ ಮಾಡಲಾಗಿದೆ, ಆಟ ಪ್ರಾರಂಭವಾದ ಬದಲು?

![Timer has started](images/brain-timer-bug.png)

--- task ---

ಟೈಮರ್ಗಾಗಿ ನೀವು ಕೋಡ್ ಅನ್ನು ಬದಲಾಯಿಸಬಹುದೇ ಆದ್ದರಿಂದ ಆಟಗಾರನು button ಕ್ಲಿಕ್ ಮಾಡಿದಾಗ ಟೈಮರ್ ಪ್ರಾರಂಭವಾಗುತ್ತದೆ?

--- /task ---

--- task ---

ನಿಮ್ಮ ಬಟನ್ sprite‌ಗೆ ಕೋಡ್ ಸೇರಿಸಿ ಇದರಿಂದ ಪ್ರತಿ ಆಟದ ಕೊನೆಯಲ್ಲಿ ಬಟನ್ ಮತ್ತೆ ತೋರಿಸುತ್ತದೆ.

![Button sprite](images/button-sprite.png)

```blocks3
    when I receive [end v]
    show
```

--- /task ---

--- task ---

ಪರೀಕ್ಷಿಸಿ 'Play' ಬಟನ್ ಒಂದೆರಡು ಆಟಗಳನ್ನು ಆಡುವ ಮೂಲಕ. ಬಟನ್ ಪ್ರತಿ ಆಟದ ಕೊನೆಯಲ್ಲಿ ತೋರಿಸಬೇಕು.

ಆಟವನ್ನು ಹೆಚ್ಚು ವೇಗವಾಗಿ ಪರೀಕ್ಷಿಸಲು, ನೀವು ಅದರ ಮೌಲ್ಯವನ್ನು ಬದಲಾಯಿಸಬಹುದು `time`{:class="block3variables"} ಆದ್ದರಿಂದ ಪ್ರತಿ ಆಟವು ಕೆಲವೇ ಸೆಕೆಂಡುಗಳಷ್ಟು ಉದ್ದವಾಗಿರುತ್ತದೆ.

![Stage](images/stage-sprite.png)

```blocks3
    set [time v] to [10]
```

--- /task ---

--- task ---

ಯಾವಾಗ ಬಟನ್ ಕಾಣುತ್ತದೆ ಎಂಬುದನ್ನು ನೀವು ಬದಲಾಯಿಸಬಹುದು mouse pointer ಅದರ ಮೇಲೆ ಸುಳಿದಾಡುತ್ತದೆ.

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

![screenshot](images/brain-fisheye.png)

--- /task ---