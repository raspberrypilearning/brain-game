\--- challenge \---

## Aufgabe: Wettrennen zu 10 Punkten

Kannst du dein Spiel so ändern, dass der Spieler nicht so viele Frage beantworten muss, wie er in 30 Sekunden schaft, sondern wie schnell er 10 Fragen richtig beantworten kann?

Um das zu machen, musst du lediglich den Code von deiner Uhr ändern. Weißt du was geändert werden muss?

```blocks
    Wenn ich [Start v] empfange
    setze [zeit v] auf (30)
    wiederhole bis <(zeit) = [0]>
        warte (1) Sek.
        ändere [zeit v] um (-1)
    end
    sende [Ende v] an alle
```

\--- /challenge \---