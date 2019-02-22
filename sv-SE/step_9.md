## Utmaning: ras till 10 poäng

Kan du ändra ditt spel så att spelaren, i stället för att svara på så många frågor som möjligt på 30 sekunder, svara på 10 frågor så snabbt som möjligt.

För att göra denna ändring behöver du bara ändra din tidskodskod. Kan du se vilka block som behöver vara annorlunda?

```blocks3
    när jag tar emot [start v]
    set [tid v] till (30)
    upprepa tills <(tid) = [0]>
        vänta (1) sekunder
        ändra [tid v] av (-1)
    slut
    sändning v)
```