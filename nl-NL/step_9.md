## Uitdaging: race naar 10 punten

Kun je je spel veranderen zodat de speler, in plaats van zo veel mogelijk vragen in 30 seconden te beantwoorden, zo snel mogelijk 10 vragen beantwoordt.

Om deze verandering aan te brengen, hoef je alleen je timercode te wijzigen. Kun je zien welke blokken anders moeten zijn?

```blocks3
when I receive [start v]
set [tijd v] to (30)
repeat until <(tijd) = [0]> 
  wait (1) seconds
  change [tijd v] by (-1)
end
broadcast (einde v)
```