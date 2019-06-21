## Uitdaging: race naar 10 punten

Kun je je spel veranderen zodat de speler, in plaats van zo veel mogelijk vragen in 30 seconden te beantwoorden, zo snel mogelijk 10 vragen beantwoordt.

Om deze verandering aan te brengen, hoef je alleen je timercode te wijzigen. Kun je zien welke blokken anders moeten zijn?

```blocks3
    wanneer ik signaal [start v] ontvang
  maak [tijd v] (30)
  herhaal tot <(tijd) = [0]>
    wacht (1) sec.
    verander [tijd v] met (-1)
  end
  zend signaal (einde v)
```