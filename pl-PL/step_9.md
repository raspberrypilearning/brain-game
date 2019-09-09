## Wyzwanie: wyścig do 10 punktów

Czy możesz zmienić swoją grę tak, aby gracz, zamiast odpowiadać na jak najwięcej pytań w ciągu 30 sekund, odpowiedział na 10 pytań tak szybko, jak to możliwe.

Aby to zmienić, wystarczy zmienić kod minutnika. Czy widzisz, które bloki muszą być różne?

```blocks3
    kiedy otrzymam [start v]
    ustaw [czas v] na (30)
    powtarzaj aż <(czas) = [0]> 
        czekaj (1) sekund
        zmień [czas v] o (-1)
    koniec
    nadaj komunikat (koniec v)
```