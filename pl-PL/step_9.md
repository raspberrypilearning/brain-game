## Wyzwanie: wyścig do 10 punktów

Czy możesz zmienić swoją grę tak, aby gracz, zamiast odpowiadać na jak najwięcej pytań w ciągu 30 sekund, odpowiedział na 10 pytań tak szybko, jak to możliwe.

Aby to zmienić, wystarczy zmienić kod czasowy. Czy widzisz, które bloki muszą być różne?

```blocks3
    kiedy otrzymam [start v]
    ustaw [czas v] na (30)
    powtórz, aż <(czas) = [0]>
        zaczekaj (1) sekund
        zmień [czas v] przez (-1)
    koniec
    transmisji (koniec v)
```