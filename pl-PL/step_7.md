## Dodaj grafikę

W tej chwili duszek postaci po prostu mówi `tak! :)` lub `nie :(` na odpowiedzi gracza. Dodaj grafikę, aby poinformować gracza, czy odpowiedź jest poprawna, czy niepoprawna.

\--- task \---

Utwórz nowy duszek o nazwie „Wynik” i nadaj mu kostium „zaznaczony/sprawdzony” oraz „krzyżyk”.

![Duszek z kostiumami "zaznaczony" i "krzyżyk"](images/brain-result.png)

\--- /task \---

\--- task \---

Zmień kod duszka postaci, aby zamiast mówić coś graczowi, `nadawał komunikat`{:class="block3events"} „poprawnie” lub „niepoprawnie”.

![Duszek postaci](images/giga-sprite.png)

```blocks3
jeżeli <(odpowiedź) = ((liczba 1) * (liczba 2))> to

- powiedz [tak! :)] przez (2) sekund
+ nadaj komunikat (poprawnie v)
w przeciwnym razie
- powiedz [nie :(] przez (2) sekund
+ nadaj komunikat (niepoprawnie v)
koniec
```

\--- /task \---

\--- task \---

Teraz możesz użyć tych komunikatów do `pokazania`{:class="block3looks"} kostiumu „zaznaczony” lub „krzyżyk”. Dodaj następujący kod do duszka „Wynik”:

![Duszek wyniku](images/result-sprite.png)

```blocks3
    kiedy otrzymam [poprawnie v]
    zmień kostium na (zaznaczony v)
    pokaż
    czekaj (1) sekund
    ukryj

    kiedy otrzymam [niepoprawnie v]
    zmień kostium na (krzyżyk v)
    pokaż
    czekaj (1) sekund
    ukryj

    kiedy zielona flaga kliknięta
    ukryj
```

\--- /task \---

\--- task \--- Ponownie przetestuj grę. Powinieneś zobaczyć tyknięcie, gdy odpowiesz poprawnie na pytanie, a krzyżyk, gdy odpowiesz niepoprawnie!

![Zaznaczony dla poprawnej, krzyżyk dla złej odpowiedzi](images/brain-test-answer.png)

\--- /task \---

Czy widzisz, że kod `kiedy otrzymam [poprawnie]`{:class="block3events"} i `kiedy otrzymam [niepoprawnie]`{:class="block3events"} jest prawie identyczny?

Aby łatwiej zmienić kod, utworzysz niestandardowy blok.

\--- task \---

Wybierz duszka "Wynik". Następnie kliknij `Moje bloki`{:class="block3myblocks"}, a następnie **Utwórz blok**. Utwórz nowy blok i nazwij go `animacja`{:class="block3myblocks"}.

![Duszek wyniku](images/result-sprite.png)

![Utwórz blok o nazwie animacja](images/brain-animate-function.png)

\--- /task \---

\--- task \--- Przenieś kod, który `pokazuje`{:class="block3looks"} i `ukrywa`{:class="block3looks"} duszka „Wynik” do bloku `animacja`{:class="block3myblocks"}:

![Duszek wyniku](images/result-sprite.png)

```blocks3
definiuj animacja
pokaż
czekaj (1) sekund
ukryj
```

\--- /task \---

\--- task \--- Upewnij się, że usunąłeś bloki `pokaż`{:class="block3looks"} i `ukryj`{:class="block3looks"} poniżej **obu** bloków `zmiany kostiumu`{:class="block3looks"}.

Następnie dodaj blok `animacja`{:class="block3myblocks"} poniżej obu bloków `zmiany kostiumu`{:class="block3looks"}. Twój kod powinien wyglądać teraz tak:

![Duszek wyniku](images/result-sprite.png)

```blocks3
    kiedy otrzymam [poprawnie v]
    zmień kostium na (zaznaczony v)
    animacja:: własna

    kiedy otrzymam [niepoprawnie v]
    zmień kostium na (krzyżyk v)
    animacja:: własna
```

\--- /task \---

Ze względu na niestandardowy blok `animacja`{:class="block3myblocks}, musisz tylko dokonać jednej zmiany w kodzie, jeśli chcesz pokazać kostiumy duszka "Wynik" na dłuższy lub krótszy czas.

\--- task \---

Zmień swój kod, tak aby wyświetlał kostiumy "zaznaczony" lub "krzyżyk" przez 2 sekundy.

\--- /task \---

\--- task \--- Zamiast `pokazywania`{:class="block3looks"} i `ukrywania`{:class="block3looks"} kostiumów „zaznacz” lub „krzyżyk”, możesz zmienić `animacji`{:class="block3myblocks"}, aby kostiumy znikały.

![Duszek wyniku](images/result-sprite.png)

```blocks3
    definiuj animacja
    ustaw efekt [duch v] na (100)
    pokaż
    powtórz (25)
        zmień efekt [duch v] przez (-4)
    koniec
    ukryj
```

\--- /task \---

Czy możesz poprawić animację grafiki „zaznaczony” lub „krzyżyk”? Możesz dodać kod, aby kostiumy również zanikały, lub możesz użyć innych fajnych efektów:

![zrzut ekranu](images/brain-effects.png)