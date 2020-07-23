## ಟೈಮರ್ ಸೇರಿಸಿ

\--- task \---

ಹೊಸ ವೇರಿಯೇಬಲ್ ಸಹಾಯದಿಂದ ವೇದಿಕೆಯಲ್ಲಿ ಕೌಂಟ್ಡೌನ್ ಟೈಮರ್ ರಚಿಸಿ `time`{:class="block3variables"}. ಟೈಮರ್ 30 ಸೆಕೆಂಡುಗಳಿಂದ ಪ್ರಾರಂಭವಾಗಬೇಕು ಮತ್ತು 0 ಸೆಕೆಂಡುಗಳವರೆಗೆ ಎಣಿಸಬೇಕು.

![Stage sprite](images/stage-sprite.png)

\--- hints \---

\--- hint \---

ರಚಿಸಿ `variable`{:class="block3variables"}, ಇದನ್ನು ಕರೆಯಿರಿ 'time', ಮತ್ತು ಅದರ ಮೌಲ್ಯವನ್ನು ಹೊಂದಿಸಿ `30`.

ನಂತರ ಎಣಿಸಲು ಕೋಡ್ ಸೇರಿಸಿ `time`{:class="block3variables"} 30 ಸೆಕೆಂಡುಗಳಲ್ಲಿ 0 ಕ್ಕೆ ಇಳಿಯುತ್ತದೆ. ಇದನ್ನು ಮಾಡಲು, subtract `1` ನಿಂದ `time`{:class="block3variables"} ಪ್ರತಿಯೊಂದೂ `1` ಸೆಕೆಂಡ್, ಮತ್ತು repeat this until `time`{:class="block3variables"} ಈಕ್ವಾಲ್ಸ್ `0`.

\--- /hint \---

\--- hint \---

ನಿಮಗೆ ಅಗತ್ಯವಿರುವ ಬ್ಲಾಕ್ ಗಳು ಇಲ್ಲಿವೆ:

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

ನಿಮ್ಮ ಹೊಸ ಕೋಡ್ ಹೇಗಿರಬೇಕು ಎಂಬುದು ಇಲ್ಲಿದೆ:

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

ರಚಿಸಿ `broadcast`{:class="block3control"} ಅದು ಸಂದೇಶವನ್ನು ಕಳುಹಿಸುತ್ತದೆ 'end'. `broadcast`{:class="block3control"} ಇದು ಧ್ವನಿವರ್ಧಕದ ಮೇಲಿನ ಪ್ರಕಟಣೆಯಂತೆ: ಇದನ್ನು ನಿಮ್ಮ ಎಲ್ಲ ಸ್ಪ್ರೈಟ್‌ಗಳು ಕೇಳಬಹುದು. ಸೇರಿಸಿ `broadcast`{:class="block3control"} ಟೈಮರ್ ಕೋಡ್‌ನ ಕೊನೆಯಲ್ಲಿ ನಿರ್ಬಂಧಿಸಿ ಇದರಿಂದ ಕೋಡ್ ಕಳುಹಿಸುತ್ತದೆ ಮತ್ತು 'end' ಯಾವಾಗ ಸಂದೇಶ `time`{:class="block3variables"} ಎಣಿಕೆ ಮಾಡಲಾಗಿದೆ `0`.

![Stage sprite](images/stage-sprite.png)

```blocks3
    broadcast (end v)
```

\--- /task \---

\--- task \---

ನಿಮ್ಮ ಅಕ್ಷರ ಸ್ಪ್ರೈಟ್ ಅನ್ನು ಆಯ್ಕೆ ಮಾಡಿ ಮತ್ತು ಕೆಲವು ಕೋಡ್ ಅನ್ನು ಸೇರಿಸಿ ಇದರಿಂದ ಸ್ಪ್ರೈಟ್ `stops the other scripts`{:class="block3control"} ಅದು ಸ್ವೀಕರಿಸಿದಾಗ `end`{:class="block3control"} ಸಂದೇಶ.

![Giga sprite](images/giga-sprite.png)

```blocks3
    when I receive [end v]
    stop [other scripts in sprite v]
```

\--- /task \---

\--- task \---

ನಿಮ್ಮ ಆಟವನ್ನು ಮತ್ತೆ ಪರೀಕ್ಷಿಸಿ. ಟೈಮರ್ 0 ಕ್ಕೆ ಎಣಿಸುವವರೆಗೆ ಇದು ಪ್ರಶ್ನೆಗಳನ್ನು ಕೇಳುತ್ತಲೇ ಇರಬೇಕು.

\--- /task \---