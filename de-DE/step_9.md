## Herausforderung: Rennen zu 10 Punkten

Kannst du dein Spiel so ändern, dass anstatt der Spieler so viele Fragen wie möglich in 30 Sekunden zu beantworten hat, so schnell wie möglich 10 Fragen beantworten muss.

Um diese Änderung vorzunehmen, musst du nur den Countdown Code ändern. Siehst du, welche Blöcke anders sein müssen, damit dies funktioniert?

```blocks3
    when I receive [Start v]
    set [Countdown v] to (30)
    repeat until <(Countdown) = [0]>
        wait (1) seconds
        change [Countdown v] by (-1)
    end
    broadcast (Ende v)
```