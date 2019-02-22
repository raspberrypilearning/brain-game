## Dodaj grafikę

W tej chwili postać sprite po prostu mówi `tak! :)` lub `no :(` do odpowiedzi gracza Dodaj grafikę, aby gracz wiedział, czy odpowiedź jest poprawna czy niepoprawna.

\--- task \---

Utwórz nowy duszek o nazwie "Wynik" i nadaj mu "tyknięcie / czek" i kostium "krzyżowy".

![Sprite z kostiumami kleszczowymi i krzyżowymi](images/brain-result.png)

\--- /task \---

\--- task \---

Zmień kod swojego duszka, aby zamiast mówić coś do gracza, `nadawało`{: class = "block3events"} wiadomości "poprawne" lub "złe".

![Charakter sprite](images/giga-sprite.png)

```blocks3
jeśli <(odpowiedź) = ((numer 1) * (numer 2))> to

- powiedz [tak! :)] przez (2) sekundy
+ nadawanie (poprawne v)
inne
- powiedz [nope :(] przez (2) sekundy
+ transmisja (zła v)
koniec
```

\--- /task \---

\--- task \---

Teraz można korzystać z tych wiadomości do `koncert`{: class = „”} block3looks do „tick” i „krzyż” kostium. Dodaj następujący kod do ikonki "Wynik":

![Sprite wynik](images/result-sprite.png)

```blocks3
    kiedy otrzymam strój [prawidłowy v]
    do (tick v)
    show
    wait (1) seconds
    hide

    kiedy otrzymam [wrong v]
    switch costume to (cross v)
    show
    wait (1) seconds
    ukryj

    po kliknięciu flagi
    ukryj
```

\--- /task \---

\--- task \--- Sprawdź swoją grę ponownie. Powinieneś zobaczyć zaznaczenie za każdym razem, gdy poprawnie odpowiesz na pytanie, oraz krzyżyk za każdym razem, gdy odpowiesz nieprawidłowo!

![Zaznacz dla poprawności, krzyż dla złej odpowiedzi](images/brain-test-answer.png)

\--- /task \---

Czy widzisz, że kod dla `gdy otrzymam poprawne`{: class = "block3events"} i `gdy otrzymam błędne`{: class = "block3events"} jest prawie identyczny?

Aby łatwiej zmienić kod, utworzysz własny blok.

\--- task \---

Wybierz ikonkę "Wynik". Następnie kliknij `Moje bloki`{: class = "block3myblocks"}, a następnie **Utwórz blok**. Utwórz nowy blok i nazwij go `animate`{: class = "block3myblocks"}.

![Sprite wynik](images/result-sprite.png)

![Utwórz blok o nazwie animacja](images/brain-animate-function.png)

\--- /task \---

\--- task \--- Przenieś kod do `show`{: class = "block3looks"} i `ukryj`{: class = "block3looks"} ikonkę "Wynik" do `animacji`{: class = " block3myblocks "} block:

![Sprite wynik](images/result-sprite.png)

```blocks3
define animuj
pokaż
czekaj (1) sekundy
ukryj
```

\--- /task \---

\--- task \--- Upewnij się, że usunąłeś `show`{: class = "block3looks"} i `ukryj`{: class = "block3looks"} bloki poniżej **obu** z `zmiany kostiumu`{: class = "block3looks"} bloki.

Następnie dodaj blok `animate`{: class = "block3myblocks"} poniżej obu bloków `przełącznika`{: class = "block3looks"}. Twój kod powinien wyglądać teraz tak:

![Sprite wynik](images/result-sprite.png)

```blocks3
    kiedy otrzymam strój [prawidłowy v]
    do (tick v)
    animate :: custom

    gdy otrzymam [niewłaściwy v]
    przełącznik kostiumu do (cross v)
    animate :: custom
```

\--- /task \---

Ze względu na blok niestandardowy `animacja`{: class = "block3myblocks}}, musisz tylko dokonać jednej zmiany w kodzie, jeśli chcesz pokazać kostiumy duszków" Wynik "na dłuższy lub krótszy czas.

\--- task \---

Zmień swój kod, tak aby wyświetlał kostiumy "tick" lub "cross" przez 2 sekundy.

\--- /task \---

\--- task \--- Zamiast `pokazując`{: class = "block3looks"} i `ukrywając`{: class = "block3looks"} kostiumy "tick" lub "cross", możesz zmienić swoje `animowanych`{: class = "block3myblocks"} zablokuj, aby kostiumy zniknęły.

![Sprite wynik](images/result-sprite.png)

```blocks3
    define animuj
    ustaw efekt [duch v] na (100)
    pokaż
    powtórz (25)
        zmień efekt [duch v] przez (-4)
    koniec
    ukryj
```

\--- /task \---

Czy możesz poprawić animację grafiki "kleszczowej" lub "krzyżowej"? Możesz dodać kod, aby również kostiumy zanikły, lub możesz użyć innych fajnych efektów:

![zrzut ekranu](images/brain-effects.png)