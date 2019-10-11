## Herausforderung: 10-Punkte-Partie

Kannst du dein Spiel so ändern, dass der Spieler anstatt so viele Fragen wie möglich in 30 Sekunden zu beantworten hat, so schnell wie möglich 10 Fragen beantworten muss.

Um diese Änderung vorzunehmen, musst du nur den Countdown Code ändern. Siehst du, welche Blöcke anders sein müssen, damit dies funktioniert?

```blocks3
    wenn ich [Start v] empfange
    setze [Countdown v] auf (30)
    wiederhole bis <(Countdown) = [0]>
        warte (1) Sekunden
        ändere [Countdown v] um (-1)
    ende
    sende (Ende v) an alle
```