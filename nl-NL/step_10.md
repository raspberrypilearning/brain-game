--- challenge ---

## Uitdaging: race naar 10 punten

Kun je je spel veranderen, zodat de speler in plaats van zoveel vragen te beantwoorden als ze kunnen in 30 seconden, moet zien hoe snel ze 10 vragen goed kunnen beantwoorden?

Om dit te doen, hoef je alleen je timercode te wijzigen. Kun je zien wat er moet worden veranderd?

```blocks
    wanneer ik signaal [start v] ontvang
maak [time v] (30)
herhaal tot <(time) = [0]>
   wacht (1) sec.
   verander [time v] met (-1)
einde
zend signaal [einde v]
```

--- /challenge ---
