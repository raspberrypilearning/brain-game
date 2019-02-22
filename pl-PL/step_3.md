## Dodaj licznik czasu

\--- task \--- Utwórz timer na stole montażowym za pomocą nowej zmiennej o nazwie `time`{: class = "block3variables"}. Licznik powinien rozpoczynać się po 30 sekundach i odliczać do 0 sekund.

![Sprite sceny](images/stage-sprite.png)

\--- hints \--- \--- hint \---

Utwórz `zmienną`{: class = "block3variables"}, nazwij ją "time" i ustaw jej wartość na `30`.

Następnie dodaj kod, aby liczyć `czas`{: class = "block3variables"} do 0 w ciągu 30 sekund. Aby to zrobić, odejmuj `1` od `czasu`{: class = "block3variables"} co `1` sekund, i powtarzaj to do `czasu`{: class = "block3variables"} jest równe `0`.

\--- / wskazówka \--- \--- podpowiedź \--- Oto bloki, których potrzebujesz:

```blocks3
powtórz do < >

koniec

czekaj (1) sekundy

zmieniaj [czas v] o (1)

(czas)

gdy flaga kliknie

<() = ()>

ustaw [czas v] na [0]
```

\--- / wskazówka \--- \--- podpowiedź \--- Oto, jak powinien wyglądać twój nowy kod:

```blocks3
kiedy flaga kliknęła
ustaw [czas v] na [30]
powtórz, aż <(czas) = (0)>
    czekaj (1) sekundy
    zmień [czas v] o (-1)
koniec
```

\--- /hint \--- \--- /hints \---

\--- /task \---

\--- task \---

Utwórz transmisję ``{: class = "block3control"}, która wyśle komunikat "koniec". A `broadcast`{: class = "block3control"} jest jak zapowiedź nad głośnikiem: może być słyszalny przez wszystkie twoje duszki. Dodaj blok `broadcast`{: class = "block3control"} na końcu kodu timera, aby kod wysłał i komunikat "end", gdy `czas`{: class = "block3variables"} odliczał do `0`.

![Sprite sceny](images/stage-sprite.png)

```blocks3
    broadcast (koniec v)
```

\--- /task \---

\--- task \--- Wybierz duszę postaci i dodaj trochę kodu, aby sprite `zatrzymał inne skrypty`{: class = "block3control"} po otrzymaniu wiadomości `end`{: class = "block3control"} .

![Giga duszek](images/giga-sprite.png)

```blocks3
    kiedy otrzymam [koniec v]
zatrzymaj [inne skrypty duszka v]
```

\--- /task \---

\--- task \---

Sprawdź swoją grę ponownie. Powinien nadal zadawać pytania, aż licznik odlicza do zera.

\--- /task \---