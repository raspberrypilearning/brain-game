## Legg til en tidtaker

\--- oppgave \--- Opprett en nedtellingstimer på scenen ved hjelp av en ny variabel kalt `gang`{: class = "block3variables"}. Timeren skal begynne på 30 sekunder og telle ned til 0 sekunder.

![Stage sprite](images/stage-sprite.png)

\--- hint \--- \--- hint \---

Opprett en `variabel`{: class = "block3variables"}, kall det 'tid', og sett verdien til `30`.

Legg deretter til kode for å telle `time`{: class = "block3variables"} ned til 0 innen 30 sekunder. For å gjøre dette trekker du `1` fra `tid`{: class = "block3variables"} hver `1` sekund, og gjenta dette til `gang`{: class = "block3variables"} er `0`.

\--- / hint \--- \--- hint \--- Her er blokkene du trenger:

```blocks3
gjenta til < >

slutt

vent (1) sekunder

endre [tid v] av (1)

(tid)

når flagget klikket

<() = ()>

sett [tid v] til [0]
```

\--- / hint \--- \--- hint \--- Her er hva din nye kode skal se ut:

```blocks3
når flagget klikket
sett [tid v] til [30]
gjenta til <(tid) = (0)>
    vent (1) sekunder
    endre [tid v] av (-1)
ende
```

\--- / hint \--- \--- / hint \---

\--- / oppgave \---

\--- oppgave \---

Lag en `sending`{: class = "block3control"} som sender meldingen 'slutt'. En `kringkasting`{: class = "block3control"} er som en kunngjøring over en høyttaler: den kan bli hørt av alle dine sprites. Legg til `sendingen`{: class = "block3control"} -blokka til slutten av timekoden slik at koden vil sende og "avslutt" meldingen når `tiden`{: class = "block3variables"} er telt ned til `0`.

![Stage sprite](images/stage-sprite.png)

```blocks3
    kringkasting (slutt v)
```

\--- / oppgave \---

\--- oppgave \--- Velg din karaktersprite og legg til noe kode slik at sprite `stopper de andre skriptene`{: class = "block3control"} når den mottar `end`{: class = "block3control"} meldingen .

![Giga Sprite](images/giga-sprite.png)

```blocks3
    når jeg mottar [end v]
    stop [andre skript i sprite v]
```

\--- / oppgave \---

\--- oppgave \---

Test spillet ditt igjen. Det bør fortsette å stille spørsmål til timeren har talt ned til 0.

\--- / oppgave \---