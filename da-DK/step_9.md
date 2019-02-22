## Udfordring: Race til 10 point

Kan du ændre dit spil, så spilleren, i stedet for at svare så mange spørgsmål som muligt om 30 sekunder, besvare 10 spørgsmål så hurtigt som muligt.

For at gøre denne ændring er du kun nødt til at ændre din timerkode. Kan du se, hvilke blokke der skal være forskellige?

```blocks3
    når jeg modtager [start v]
    sæt [tid v] til (30)
    gentag til <(tid) = [0]>
        vent (1) sekunder
        skift [tid v] af (-1)
    slut
    udsendelse v)
```