\--- challenge \---

## Wyzwanie: Wyścig do 10 punktów

Czy możesz zmienić swoją grę, aby zamiast odpowiadać na pytania w ciągu 30 sekund, gracz musi sprawdzić, jak szybko mogą poprawnie odpowiedzieć na 10 pytań?

Aby to zrobić, musisz tylko zmienić kod stopera. Czy widzisz, co trzeba zmienić?

```blocks
    kiedy otrzymam [start v]
  ustaw [czas v] na (30)
  powtarzaj aż <(czas) =[0]>
      czekaj(1) s
      zmień [czas v] o (-1)
  koniec
  nadaj [ koniec v]
```

\--- /challenge \---