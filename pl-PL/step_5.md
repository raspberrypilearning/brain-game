## Wielokrotne gry

Dodajmy do gry przycisk "Zagraj", żeby móc zagrać wiele razy.

+ Stwórz nowy duszek przycisku "Zagraj", którą gracz kliknie, aby rozpocząć nową grę. Możesz narysować go samodzielnie lub edytować obraz z biblioteki Scratch.
    
    ![zrzut ekranu](images/brain-play.png)

+ Dodaj ten kod do nowego przycisku.
    
    ```blocks
        kiedy kliknięto zieloną flagę
    pokaż
    
    kiedy duszek kliknięty
    ukryj
    nadaj [start v]
    ```
    
    Ten kod pokazuje przycisk "Zagraj" po uruchomieniu projektu. Po kliknięciu przycisku jest on ukrywany, a następnie nadajemy komunikat, który uruchomi grę.

+ Będziesz musiał edytować kod swojej postaci, aby gra zaczęła się, gdy otrzymasz komunikat `start`{:class="blockevents"}, a nie po kliknięciu flagi.
    
    Zamień `kiedy kliknięto zieloną flagę`{:class="blockevents"} na `kiedy otrzymam [start v]`{:class="blockevents"}.
    
    ![zrzut ekranu](images/brain-start.png)

+ Kliknij zieloną flagę, a następnie kliknij nowy przycisk odtwarzania, aby go przetestować. Powinieneś zobaczyć, że gra nie rozpocznie się, dopóki przycisk nie zostanie kliknięty.

+ Czy zauważyłeś, że licznik czasu zaczyna się po kliknięciu zielonej flagi, a nie po rozpoczęciu gry?
    
    ![zrzut ekranu](images/brain-timer-bug.png)
    
    Czy możesz rozwiązać ten problem?

+ Kliknij na scenie i zamień wszystkie `zatrzymaj wszystko`{:class="blockcontrol"} bloki na komunikat `koniec`{:class="blockevents"}.
    
    ![zrzut ekranu](images/brain-end.png)

+ Możesz teraz dodać kod do przycisku, aby pokazać go ponownie na końcu każdej gry.
    
    ```blocks
        kiedy otrzymam [koniec v]
    pokaż
    ```

+ Będziesz także musiał przestać zadawać pytania dla swojej postaci pod koniec każdej gry:
    
    ```blocks
        kiedy otrzymam [koniec v]
    zatrzymaj [inne skrypty duszka v]
    ```

+ Sprawdź swój przycisk odtwarzania, grając w kilka gier. Powinieneś zauważyć, że przycisk "Zagraj" pokazuje po każdej grze. Aby ułatwić testowanie, możesz skrócić każdą grę, tak, aby trwała tylko kilka sekund.
    
    ```blocks
        ustaw [czas v] na [10]
    ```

+ Możesz nawet zmienić wygląd przycisku, gdy najedzie na niego mysz.
    
    ```blocks
        kiedy kliknięto zieloną flagę
    pokaż
    zawsze 
      jeżeli <touching [mouse-pointer v]?> to 
        ustaw efekt [rybie oko v] na (30)
     w przeciwnym razie
        ustaw efekt [rybie oko v] na (0)
      end
    end
    ```
    
    ![zrzut ekranu](images/brain-fisheye.png)