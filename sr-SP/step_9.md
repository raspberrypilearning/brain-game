## Изазов: трка до 10 бодова

Можете ли промијенити игру тако да играч, умјесто да одговори на што више питања у 30 секунди, одговори на 10 питања што је брже могуће.

Да бисте извршили ову промену, потребно је само да промените тајмер. Видите који блокови морају бити различити?

```blocks3
    када примим [старт в]
    сет [време в] до (30)
    понављај до <(време) = [0]>
        чекај (1) секунде
        промени [време в] до (-1)
    крај
    емитовање (крај в)
```