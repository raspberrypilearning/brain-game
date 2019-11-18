## Wielokrotne gry

Teraz dodasz przycisk „Graj”, aby gracz mógł grać w twoją grę wiele razy.

--- task --- Utwórz nowego duszka przycisku „Graj”, którą gracz musi kliknąć, aby rozpocząć nową grę.

Możesz samemu narysować duszka lub edytować duszka z biblioteki.

![Obraz przycisku odtwarzania](images/brain-play.png)

--- /task ---

--- task --- Dodaj ten kod do swojego duszka przycisku:

![Przycisk duszka](images/button-sprite.png)

```blocks3
    kiedy kliknięto zieloną flagę
    pokaż

kiedy ten duszek kliknięty
    ukryj
    nadaj komunikat (start v)
```

--- /task ---

Nowy kod zawiera kolejny blok `nadaj komunikat`{:class="block3events"}, który wysyła komunikat „start”.

Nowy kod sprawia, że duszek „Graj” pojawia się, gdy gracz kliknie zieloną flagę. Gdy gracz kliknie przycisk duszka, duszek ukrywa się, a następnie wysyła komunikat, na który inne duszki mogą zareagować.

W tej chwili duszek postaci zaczyna zadawać pytania, gdy gracz kliknie flagę. Zmień kod swojej gry, aby duszek postaci zaczynał zadawać pytania, gdy `otrzyma komunikat`{:class="block3events"} „start”.

--- task --- Wybierz swojego duszka postaci i w sekcji jego kodu, zamień blok `kiedy kliknięto zieloną flagę`{:class="block3events"} na blok `kiedy otrzymam wiadomość`{:class="block3events"}.

![Duszek postaci](images/giga-sprite.png)

```blocks3
- kiedy kliknięto zieloną flagę
+ kiedy otrzymam [start v]
ustaw [liczba 1 v] na (losuj liczbę od (2) do (12))
ustaw [liczba 2 v] na (losuj liczbę od (2) do (12))
zapytaj (połącz (liczba 1) i (połącz [ x ] i (liczba 2))) i czekaj
jeżeli <(odpowiedź) = ((liczba 1) * (liczba 2))> to 
  powiedz [tak! :)] przez (2) sekund
w przeciwnym razie 
  powiedz [niestety :(] przez (2) sekund
koniec
```

--- /task ---

--- task ---

Kliknij zieloną flagę, a następnie kliknij nowy przycisk „Graj”, aby sprawdzić, czy działa. Zauważ, że gra nie uruchamia się przed kliknięciem przycisku.

--- /task ---

Czy widzisz, że licznik czasu uruchamia się po kliknięciu zielonej flagi, a nie w momencie rozpoczęcia gry?

![Licznik czasu został uruchomiony](images/brain-timer-bug.png)

--- task ---

Czy możesz zmienić kod licznika czasu tak, aby zaczął odliczanie, gdy gracz kliknie przycisk?

--- /task ---

--- task --- Dodaj kod do duszka przycisku, aby przycisk pojawiał się ponownie na końcu każdej gry.

![Duszek przycisku](images/button-sprite.png)

```blocks3
    kiedy otrzymam [koniec v]
    pokaż
```

--- /task ---

--- task ---

Przetestuj przycisk „Graj”, grając w kilka gier. Przycisk powinien pojawić się na końcu każdej gry.

Aby przyspieszyć testowanie gry, możesz zmienić wartość `czas`{:class="block3variables"} tak, aby każda gra trwała tylko kilka sekund.

![Scena](images/stage-sprite.png)

```blocks3
    ustaw [czas v] na [10]
```

--- /task ---

--- task --- Możesz zmienić wygląd przycisku, gdy gracz najedzie na niego wskaźnikiem myszy.

![Przycisk](images/button-sprite.png)

```blocks3
    kiedy kliknięto zieloną flagę
    pokaż
    zawsze 
    jeżeli <dotyka (wskaźnik myszy)> to 
         ustaw efekt [rybie oko v] na (30)
    w przeciwnym razie
          ustaw efekt [rybie oko v] na (0)
    end
end
```

![zrzut ekranu](images/brain-fisheye.png) --- /task ---