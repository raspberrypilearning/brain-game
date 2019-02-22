## Tilføj en timer

\--- opgave \--- Opret en nedtællingstimer på scenen ved hjælp af en ny variabel kaldet `gang`{: class = "block3variables"}. Timeren skal begynde om 30 sekunder og tæller ned til 0 sekunder.

![Stage sprite](images/stage-sprite.png)

\--- hints \--- \--- hint \---

Opret en `variabel`{: class = "block3variables"}, kald det 'tid', og angiv dens værdi til `30`.

Tilføj derefter kode for at tælle `time`{: class = "block3variables"} ned til 0 inden for 30 sekunder. For at gøre dette skal du trække `1` fra `gang`{: class = "block3variables"} hver `1` sekund, og gentag dette indtil `gang`{: class = "block3variables"} svarer til `0`.

\--- / hint \--- \--- tip \--- Her er de blokke du har brug for:

```blocks3
gentag til < >

slut

vent (1) sekunder

skift [tid v] ved (1)

(tid)

når flag klikkes

<() = ()>

sæt [tid v] til [0]
```

\--- / hint \--- \--- tip \--- Her er hvad din nye kode skal se ud:

```blocks3
når flag klikket
sæt [tid v] til [30]
gentag til <(tid) = (0)>
    vent (1) sekunder
    skift [tid v] ved (-1)
ende
```

\--- /hint \--- \--- /hints \---

\--- /task \---

\--- task \---

Opret en `udsendelse`{: class = "block3control"}, der sender meddelelsen 'ende'. En `udsendelse`{: class = "block3control"} er som en meddelelse over en højttaler: den kan høres af alle dine sprites. Tilføj `udsendelsen`{: class = "block3control"} -blokken til slutningen af timer-koden, så koden vil sende og 'slutte' besked, når `tiden`{: class = "block3variables"} er talt ned til `0`.

![Stage sprite](images/stage-sprite.png)

```blocks3
    udsendelse (slut v)
```

\--- /task \---

\--- opgave \--- Vælg din tegnsprite og tilføj kode, så sprite `stopper de andre scripts`{: class = "block3control"}, når den modtager meddelelsen `end`{: class = "block3control"} .

![Giga sprite](images/giga-sprite.png)

```blocks3
    når jeg modtager [end v]
    stop [andre scripts i sprite v]
```

\--- /task \---

\--- task \---

Test dit spil igen. Det skal fortsætte med at stille spørgsmål, indtil timeren er talt ned til 0.

\--- /task \---