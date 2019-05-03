## Lav spørgsmål

Du skal begynde med at oprette tilfældige spørgsmål, som spilleren skal svare på.

\--- task \---

Åbn et nyt Scratch-projekt.

**Online:** open a new online Scratch project at [rpf.io/scratch-new](http://rpf.io/scratchon){:target="_blank"}.

**Offline:** Åbn et nyt projekt i offline-editoren.

Hvis du skal downloade og installere Scratch offline editoren, kan du finde den på [rpf.io/scratchoff](http://rpf.io/scratchoff){: target = "_ blank"}.

\--- /task \---

\--- opgave \--- Tilføj et tegnsprite og et baggrund for dit spil. Du kan vælge noget du kan lide! Her er et eksempel:

![skærmbillede](images/brain-setting.png)

\--- /task \---

\--- opgave \--- Sørg for at du har valgt din karaktersprite. Opret to nye variabler, kaldet `nummer 1`{: class = "block3variables"} og `nummer 2`{: class = "block3variables"}, for at gemme tallene for quiz-spørgsmålene.

![skærmbillede](images/giga-sprite.png) ![skærmbillede](images/brain-variables.png)

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- opgave \--- Tilføj kode til din karaktersprite for at indstille begge `variablerne`{: class = "block3variables"} til et `tilfældige`{: class = "block3operators"} tal mellem 2 og 12.

![skærmbillede](images/giga-sprite.png)

```blocks3
når flag klikket
sæt [nummer 1 v] til (vælg tilfældigt (2) til (12))
sæt [nummer 2 v] til (vælg tilfældigt (2) til (12))
```

\--- /task \---

\--- opgave \--- Tilføj kode til `spørg`{: class = "block3sensing"} afspilleren til svaret og derefter `sige i 2 sekunder`{: class = "block3looks"} om svaret var rigtigt eller forkert:

![skærmbillede](images/giga-sprite.png)

```blocks3
når flag klikker
sæt [nummer 1 v] til (vælg tilfældigt (2) til (12))
sæt [nummer 2 v] til (vælg tilfældigt (2) til (12))

+ spørg (join [x] (nummer 2))) og vent
+ hvis <(svar) = ((nummer 1) * (nummer 2))> så
+ siger [ja! :)] for (2) sekunder
+ ellers
+ siger [nej :(] for (2) sekunder
+ ende
```

\--- /task \---

\--- task \---

Test dit projekt to gange: Svar et spørgsmål korrekt, og det andet forkert.

\--- /task \---

\--- task \---

Tilføj en `altid`{: class = "block3control"} loop rundt denne kode, så spillet spørger spilleren mange spørgsmål i træk.

\--- hints \--- \--- hint \---

Du skal føje en `evigt`{: class = "block3control"} blok, og sæt al koden bortset fra `når flag klikket`{: class = "block3control"} blokere ind i den.

\--- / hint \--- \--- hint \--- Her er den blok du har brug for:

```blocks3
for evigt
ende
```

\--- / hint \--- \--- hint \--- Her er, hvad din kode skal se ud:

```blocks3
når flag klikker

+ for evigt
    sæt [nummer 1 v] til (vælg tilfældigt (2) til (12))
    sæt [nummer 2 v] til (vælg tilfældigt (2) til (12))
    spørg 1) (join [x] (nummer 2))) og vent
    hvis <(svar) = ((nummer 1) * (nummer 2))> så
        siger [ja! :)] for (2) sekunder
    andet
        siger [nej :(] for (2) sekunder
    ende
ende
```

\--- /hint \--- \--- /hints \---

\--- /task \---