## Dodaj licznik czasu

\--- task \--- Utwórz licznik czasu na scenie za pomocą nowej zmiennej o nazwie `czas`{:class="block3variables"}. Licznik powinien rozpoczynać się na 30 sekundach i odliczać do 0 sekund.

![Duszek sceny](images/stage-sprite.png)

\--- hints \--- \--- hint \---

Utwórz `zmienną`{:class="block3variables"}, nazwij ją „czas” i ustaw jej wartość na `30`.

Następnie dodaj kod, aby odliczać `czas`{:class="block3variables"} do 0 w ciągu 30 sekund. Aby to zrobić, odejmuj `1` od zmiennej `czas`{:class="block3variables"} co `1` sekundę i powtarzaj to do chwili gdy `czas`{:class="block3variables"} jest równy `0`.

\--- /hint \--- \--- hint \--- poniżej masz bloczki, których będziesz potrzebować:

```blocks3
powtarzaj aż < >

koniec

czekaj (1) sekund

zmień [czas v] o (-1)

(czas)

kiedy kliknięto zieloną flagę

<() = ()>

ustaw [czas v] na [30]
```

\--- /hint \--- \--- hint \--- Oto jak powinien wyglądać twój nowy kod:

```blocks3
kiedy kliknięto zieloną flagę
ustaw [czas v] na [30]
powtarzaj, aż <(czas) = (0)>
    czekaj (1) sekund
    zmień [czas v] o (-1)
koniec
```

\--- /hint \--- \--- /hints \---

\--- /task \---

\--- task \---

Utwórz `nadawanie komunikatu`{:class="block3control"}, które wyśle komunikat „koniec”. `Nadawanie komunikatu`{: class="block3control"} jest jak zapowiedź przez głośnik: będzie usłyszane przez wszystkie duszki. Dodaj blok `nadaj komunikat`{:class="block3control"} na końcu kodu licznika czasu, aby kod wysłał komunikat "koniec", gdy `czas`{:class="block3variables"} odliczył do `0`.

![Duszek sceny](images/stage-sprite.png)

```blocks3
    nadaj komunikat (koniec v)
```

\--- /task \---

\--- task \--- Wybierz duszek postaci i dodaj trochę kodu, aby duszek `zatrzymał inne skrypty`{:class="block3control"} po otrzymaniu wiadomości `koniec`{:class="block3control"}.

![Giga duszek](images/giga-sprite.png)

```blocks3
    kiedy otrzymam [koniec v]
zatrzymaj [inne skrypty duszka v]
```

\--- /task \---

\--- task \---

Sprawdź swoją grę ponownie. Pytania powiiny być zadawane, aż licznik odlicza do zera.

\--- /task \---