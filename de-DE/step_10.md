\--- challenge \---

## Herausforderung: 10 Punkte-Partie

Kannst du dein Spiel so verändern, dass der Spieler nicht so viele Fragen wie möglich in 30 Sekunden, sondern möglichst schnell 10 Fragen richtig beantworten muss?

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