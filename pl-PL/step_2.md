## Twórz pytania

Zaczniesz od stworzenia losowych pytań, na które gracz musi odpowiedzieć.

\--- task \---

Otwórz nowy projekt Scratch.

**Online:** open a new online Scratch project at [rpf.io/scratch-new](http://rpf.io/scratch-new){:target="_blank"}.

**Offline:** otwórz nowy projekt w edytorze offline.

Jeśli musisz pobrać i zainstalować edytor Scratcha, znajdziesz go na stronie [rpf.io/scratchoff](http://rpf.io/scratchoff){:target="_blank"}.

\--- /task \---

\--- task \--- Dodaj sprite postaci i tło dla swojej gry. Możesz wybrać, co chcesz! Oto przykład:

![zrzut ekranu](images/brain-setting.png)

\--- /task \---

\--- task \--- Upewnij się, że wybrałeś ikonkę postaci. Utwórz dwie nowe zmienne, o nazwie `numer 1`{: class = "block3variables"} i `numer 2`{: class = "block3variables"}, aby przechowywać numery pytań do quizów.

![zrzut ekranu](images/giga-sprite.png) ![zrzut ekranu](images/brain-variables.png)

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- task \--- Dodaj kod do swojej postaci sprite'a, aby ustawić obie `zmienne`{: class = "block3variables"} na `losowe`{class = "block3operators"} z zakresu od 2 do 12.

![zrzut ekranu](images/giga-sprite.png)

```blocks3
kiedy flaga kliknęła
ustaw [numer 1 v] na (wybierz losowo (2) do (12))
ustaw [numer 2 v] na (wybierz losowo (2) do (12))
```

\--- /task \---

\--- task \--- Dodaj kod do `ask`{: class = "block3sensing"} gracza do odpowiedzi, a następnie `powiedz na 2 sekundy`{: class = "block3looks"}, czy odpowiedź była właściwa lub źle:

![zrzut ekranu](images/giga-sprite.png)

```blocks3
kiedy flaga kliknęła
ustaw [numer 1 v] na (wybierz losowo (2) do (12))
ustaw [numer 2 v] na (wybierz losowo (2) do (12))

+ zapytaj (dołącz (numer 1) (dołącz [x] (numer 2))) i poczekaj
+, jeśli <(odpowiedź) = ((numer 1) * (numer 2))> następnie
+ powiedz [tak! :)] przez (2) sekundy
+ jeszcze
+ powiedzieć [nie :(] przez (2) sekundy
+ koniec
```

\--- /task \---

\--- task \---

Przetestuj swój projekt dwa razy: odpowiedz jedno pytanie poprawnie, a drugi niepoprawnie.

\--- /task \---

\--- task \---

Dodaj pętlę `zawsze`{: class = "block3control"} wokół tego kodu, tak, aby gra zadaje graczowi wiele pytań z rzędu.

\--- hints \--- \--- hint \---

Musisz dodać blok `zawsze`{: class = "block3control"} i umieścić w nim cały kod z wyjątkiem `gdy flaga kliknęła`{: class = "block3control"}.

\--- / wskazówka \--- \--- podpowiedź \--- Oto blok, którego potrzebujesz:

```blocks3
na zawsze
koniec
```

\--- /hint \--- \--- hint \--- Tak powinien wyglądać twój kod:

```blocks3
kiedy flaga kliknęła

+ na zawsze
    ustaw [numer 1 v] na (wybierz losowo (2) do (12))
    ustaw [numer 2 v] na (wybierz losowo (2) do (12))
    zapytaj (dołącz (liczba 1) (dołącz [x] (numer 2)) i poczekaj
    jeśli <(odpowiedź) = ((numer 1) * (numer 2))> a następnie
        powiedz [tak! :)] przez (2) sekundy
    jeszcze
        powiedzieć [nie :(] przez (2) sekund
    koniec
koniec
```

\--- /hint \--- \--- /hints \---

\--- /task \---