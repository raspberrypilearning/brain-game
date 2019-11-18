## Utwórz pytania

Zaczniesz od stworzenia losowych pytań, na które gracz musi odpowiedzieć.

\--- task \---

Otwórz nowy projekt Scratch.

**Online:** otwórz nowy projekt Scratch na stronie [rpf.io/scratch-new](http://rpf.io/scratch-new){:target="_blank"}.

**Offline:** otwórz nowy projekt w edytorze offline.

Jeśli musisz pobrać i zainstalować edytor Scratch, znajdziesz go na stronie [rpf.io/scratchoff](http://rpf.io/scratchoff){:target="_blank"}.

\--- /task \---

\--- task \--- Dodaj duszka postaci i tło dla swojej gry. Możesz wybrać, co chcesz! Oto przykład:

![zrzut ekranu](images/brain-setting.png)

\--- /task \---

\--- task \--- Upewnij się, że wybrałeś duszka postaci. Utwórz dwie nowe zmienne, o nazwie `liczba 1`{:class="block3variables"} i `liczba 2`{:class="block3variables"}, aby przechowywać liczby na potrzeby quizu.

![zrzut ekranu](images/giga-sprite.png) ![zrzut ekranu](images/brain-variables.png)

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- task \--- Dodaj kod do duszka swojej postaci, aby ustawić obie `zmienne`{:class="block3variables"} na `losowe`{class="block3operators"} liczby z zakresu od 2 do 12.

![zrzut ekranu](images/giga-sprite.png)

```blocks3
kiedy kliknięto zieloną flagę
ustaw [liczba 1 v] na (losuj liczbę od (2) do (12))
ustaw [liczba 2 v] na (losuj liczbę od (2) do (12))
```

\--- /task \---

\--- task \--- Dodaj kod do `zapytaj`{:class="block3sensing"} gracza o odpowiedź, a następnie `powiedz przez 2 sekundy`{:class="block3looks"}, czy odpowiedź była poprawna czy zła:

![zrzut ekranu](images/giga-sprite.png)

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

Przetestuj swój projekt dwa razy: odpowiedz na jedno pytanie poprawnie, a drugie błędnie.

\--- /task \---

\--- task \---

Otocz swój kod pętlą `zawsze`{:class="block3control"}, tak, aby gra zadawała graczowi wiele pytań z rzędu.

\--- hints \--- \--- hint \---

Musisz dodać blok pętli `zawsze`{:class="block3control"} i umieścić w nim cały kod z wyjątkiem bloku `kiedy kliknięto zieloną flagę`{:class="block3control"}.

\--- /hint \--- \--- hint \--- poniżej masz bloki, których będziesz potrzebować:

```blocks3
zawsze

koniec
```

\--- /hint \--- \--- hint \--- Tak powinien wyglądać twój kod:

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

\--- /hint \--- \--- /hints \---

\--- /task \---