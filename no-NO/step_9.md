## Utfordring: løp til 10 poeng

Kan du endre spillet ditt slik at spilleren, i stedet for å svare på så mange spørsmål som mulig på 30 sekunder, svare på 10 spørsmål så raskt som mulig.

For å gjøre denne endringen trenger du bare å endre timerkoden. Kan du se hvilke blokker som må være forskjellige?

```blocks3
    Når jeg mottar [start v]
    set [tid v] til (30) som
    tilbakevendende inntil <(tid) = [0]>
        vente (1) sekunder
        forandring [tid v] av (-1)
    ende
    sending (enden v)
```