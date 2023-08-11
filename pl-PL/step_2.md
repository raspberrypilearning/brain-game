## Utwórz pytania

Zaczniesz od stworzenia losowych pytań, na które gracz musi odpowiedzieć.

\--- task \---

Otwórz nowy projekt Scratch.

**Online:** open a new online Scratch project at [rpf.io/scratch-new](https://rpf.io/scratch-new){:target="_blank"}.

**Offline:** otwórz nowy projekt w edytorze offline.

If you need to download and install the Scratch offline editor, you can find it at [rpf.io/scratchoff](https://rpf.io/scratchoff){:target="_blank"}.

\--- /task \---

\--- task \---

Add a character sprite and a backdrop for your game. You can choose any you like! Here's an example:

![screenshot](images/brain-setting.png)

\--- /task \---

\--- task \---

Make sure you have your character sprite selected. Create two new variables, called `number 1`{:class="block3variables"} and `number 2`{:class="block3variables"}, to store the numbers for the quiz questions.

![screenshot](images/giga-sprite.png)

![screenshot](images/brain-variables.png)

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- task \---

Add code to your character sprite to set both of the `variables`{:class="block3variables"} to a `random`{:class="block3operators"} number between 2 and 12.

![screenshot](images/giga-sprite.png)

```blocks3
kiedy kliknięto zieloną flagę
ustaw [liczba 1 v] na (losuj liczbę od (2) do (12))
ustaw [liczba 2 v] na (losuj liczbę od (2) do (12))
```

\--- /task \---

\--- task \---

Add code to `ask`{:class="block3sensing"} the player for the answer, and then `say for 2 seconds`{:class="block3looks"} whether the answer was right or wrong:

![screenshot](images/giga-sprite.png)

```blocks3
kiedy kliknięto zieloną flagę
ustaw [liczba 1 v] na (losuj liczbę od (2) do (12))
ustaw [liczba 2 v] na (losuj liczbę od (2) do (12))
+ zapytaj (połącz (liczba 1) i (połącz [ x ] i (liczba 2))) i czekaj
+ jeżeli <(odpowiedź) = ((liczba 1) * (liczba 2))> to
+ powiedz [tak!] przez 2 sekund 
+ w przeciwnym razie
+ powiedz [nie :(] przez (2) sekund
+ koniec
```

\--- /task \---

\--- task \---

Test your project twice: answer one question correctly, and the other incorrectly.

\--- /task \---

\--- task \---

Add a `forever`{:class="block3control"} loop around this code, so that the game asks the player lots of questions in a row.

\--- hints \---

\--- hint \---

You need to add a `forever`{:class="block3control"} block, and put all of the code except the `when flag clicked`{:class="block3control"} block into it.

\--- /hint \---

\--- hint \---

Here is the block you need:

```blocks3
zawsze

koniec
```

\--- /hint \---

\--- hint \---

Here is what your code should look like:

```blocks3
kiedy kliknięto zieloną flagę

+ zawsze
    ustaw [liczba1 v] na (losuj liczbę od (2) do (12))
    ustaw [liczba 2 v] na (losuj liczbę od (2) do (12))
    zapytaj (połącz (liczba 1) (połącz [x] (liczba 2)) i czekaj
    jeżeli <(odpowiedź) = ((liczba 1) * (liczba 2))> to
        powiedz [tak!] przez (2) sekund 
    w przeciwnym razie
        powiedz [nie :(] przez (2) sekund
    koniec
koniec
```

\--- /hint \---

\--- /hints \---

\--- /task \---