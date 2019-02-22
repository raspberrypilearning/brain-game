## Tilføj grafik

I øjeblikket siger character sprite bare `ja! :)` eller `nej :(` til afspillerens svar. Tilføj nogle grafik for at lade spilleren vide, om deres svar er korrekt eller forkert.

\--- task \---

Opret en ny sprite kaldet 'Resultat', og giv det et 'tick / check' og et 'cross' kostume.

![Sprite med kryds og kryds kostumer](images/brain-result.png)

\--- /task \---

\--- task \---

Skift din karaktersprogskode, så i stedet for at sige noget til afspilleren sender ``{: class = "block3events"} meddelelserne 'korrekt' eller 'forkert'.

![Character sprite](images/giga-sprite.png)

```blocks3
hvis <(svar) = ((nummer 1) * (nummer 2))> derefter

- sig [ja! :)] for (2) sekunder
+ udsendelse (korrekt v)
andet
- sig [nope :(] for (2) sekunder
+ broadcast (forkert v)
ende
```

\--- /task \---

\--- task \---

Nu kan du bruge disse meddelelser til `vise`{: class = "block3looks"} 'tick' eller 'cross' kostume. Tilføj følgende kode til 'Resultat' sprite:

![Resultat sprite](images/result-sprite.png)

```blocks3
    når jeg modtager [korrekt v]
    skifter kostume til (kryds v)
    vis
    vent (1) sekunder
    skjul

    når jeg modtager [forkert v]
    skifter kostume til (kryds v)
    vis
    vent (1) sekunder
    skjul

    når flag klikket
    skjul
```

\--- /task \---

\--- opgave \--- Test dit spil igen. Du bør se markeringen, når du besvarer et spørgsmål korrekt, og korset, når du svarer ukorrekt!

![Tjek for korrekt, kryds for forkert svar](images/brain-test-answer.png)

\--- /task \---

Kan du se, at koden for `når jeg modtager korrekt`{: class = "block3events"} og `når jeg modtager forkert`{: class = "block3events"} er næsten identisk?

Så du kan lettere ændre din kode, du skal oprette en brugerdefineret blok.

\--- task \---

Vælg "Resultat" sprite. Klik derefter på `Mine blokke`{: class = "block3myblocks"}, og derefter på **Lav en blok**. Opret en ny blok og kalder det `animere`{: class = "block3myblocks"}.

![Resultat sprite](images/result-sprite.png)

![Opret en blok kaldet animere](images/brain-animate-function.png)

\--- /task \---

\--- opgave \--- Flyt koden til `vis`{: class = "block3looks"} og `skjul`{: class = "block3looks"} "Resultat" sprite i `animere`{: class = " block3myblocks "} blok:

![Resultat sprite](images/result-sprite.png)

```blocks3
definer animere
vis
vent (1) sekunder
skjul
```

\--- /task \---

\--- opgave \--- Sørg for at du har fjernet `show`{: class = "block3looks"} og `skjul`{: class = "block3looks"} blokke under **begge** af `switch kostume`{: class = "block3looks"} blokke.

Tilføj derefter `animerede`{: class = "block3myblocks"} -blokken under begge de `switch-kostume`{: class = "block3looks"} -blokke. Din kode skal nu se sådan ud:

![Resultat sprite](images/result-sprite.png)

```blocks3
    når jeg modtager [correct v]
    switch kostume til (tick v)
    animere :: brugerdefineret

    når jeg modtager [forkert v]
    switch kostume til (cross v)
    animere :: brugerdefineret
```

\--- /task \---

På grund af den brugerdefinerede `animere`{: class = "block3myblocks"} blok, skal du kun lave en ændring til din kode, hvis du vil vise 'Result'-spritens kostumer en længere eller kortere tid.

\--- task \---

Skift din kode, så de 'tick' eller 'cross' kostumer vises i 2 sekunder.

\--- /task \---

\--- opgave \--- I stedet for `viser`{: class = "block3looks"} og `gemmer`{: class = "block3looks"} de "tick" eller "cross" kostumer, kan du ændre dine `animere`{: class = "block3myblocks"} blokere, så kostumerne falder ind.

![Resultat sprite](images/result-sprite.png)

```blocks3
    definere animere
    sæt [ghost v] effekt til (100)
    vis
    gentag (25)
        skift [spøgelse v] effekt af (-4)
    ende
    skjul
```

\--- /task \---

Kan du forbedre animationen af 'tick' eller 'cross' grafikken? Du kan tilføje kode for at få kostumerne til at falme ud, eller du kan bruge andre kølige effekter:

![skærmbillede](images/brain-effects.png)