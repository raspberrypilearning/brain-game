\--- challenge \---

## Aufgabe: Wettrennen zu 10 Punkten

Kannst du dein Spiel so ändern, dass der Spieler nicht so viele Frage beantworten muss, wie er in 30 Sekunden schaft, sondern wie schnell er 10 Fragen richtig beantworten kann?

Um das zu machen, musst du lediglich den Code von deiner Uhr ändern. Weißt du was geändert werden muss?

```blocks
    when I receive [start v]
    set [time v] to (30)
    repeat until <(time) = [0]>
        wait (1) secs
        change [time v] by (-1)
    end
    broadcast [end v]
```

\--- /challenge \---