## Lag spørsmål

Du skal begynne med å lage tilfeldige spørsmål som spilleren må svare på.

\--- oppgave \---

Åpne et nytt Scratch-prosjekt.

**Online:** Åpne et nytt online Scratch-prosjekt på [rpf.io/scratchon](http://rpf.io/scratchon){: target = "_ blank"}.

**Frakoblet:** Åpne et nytt prosjekt i offline-editoren.

Hvis du trenger å laste ned og installere Scratch offline editoren, kan du finne den på [rpf.io/scratchoff](http://rpf.io/scratchoff){: target = "_ blank"}.

\--- / oppgave \---

\--- Oppgave \--- Legg til et tegnsprite og et bakteppe for spillet ditt. Du kan velge noe du liker! Her er et eksempel:

![skjermbilde](images/brain-setting.png)

\--- / oppgave \---

\--- Oppgave \--- Pass på at du har valgt din karaktersprite. Opprett to nye variabler, kalt `nummer 1`{: class = "block3variables"} og `nummer 2`{: class = "block3variables"}, for å lagre tallene for quiz-spørsmålene.

![skjermbilde](images/giga-sprite.png) ![skjermbilde](images/brain-variables.png)

[[[generic-scratch3-add-variable]]]

\--- / oppgave \---

\--- oppgave \--- Legg til kode til karaktersprite for å sette begge `variablene`{: class = "block3variables"} til et `tilfeldig`{: class = "block3operators"} tall mellom 2 og 12.

![skjermbilde](images/giga-sprite.png)

```blocks3
når flagget klikket
sett [nummer 1 v] til (velg tilfeldig (2) til (12))
sett [nummer 2 v] til (velg tilfeldig (2) til (12))
```

\--- / oppgave \---

\--- oppgave \--- Legg til kode til `spør`{: class = "block3sensing"} spilleren for svaret, og så `si i 2 sekunder`{: class = "block3looks"} om svaret var riktig eller feil:

![skjermbilde](images/giga-sprite.png)

```blocks3
når flagget klikket
sett [nummer 1 v] til (velg tilfeldig (2) til (12))
sett [nummer 2 v] til (velg tilfeldig (2) til (12))

+ spør (bli med [x] (nummer 2))) og vent
+ hvis <(svar) = ((nummer 1) * (nummer 2))> så
+ si [ja! :)] for (2) sekunder
+ annet
+ si [nei :(] for (2) sekunder
+ slutt
```

\--- / oppgave \---

\--- oppgave \---

Test prosjektet ditt to ganger: Svar ett spørsmål riktig, og det andre feil.

\--- / oppgave \---

\--- oppgave \---

Legg en `alltid`{: class = "block3control"} loop rundt denne koden, slik at spillet spør spilleren mange spørsmål på rad.

\--- hint \--- \--- hint \---

Du må legge til en `alltid`blokkering av blokkene {: class = "block3control"}, og sett all koden unntatt `når flagget klikket`{: class = "block3control"} blokkert inn i det.

\--- / hint \--- \--- hint \--- Her er blokken du trenger:

```blocks3
for alltid
ende
```

\--- / hint \--- \--- hint \--- Her er hva koden din skal se ut som:

```blocks3
når flagget klikkte

+ for alltid
    sett [tall 1 v] til (velg tilfeldig (2) til (12))
    sett [nummer 2 v] til (velg tilfeldig (2) til (12))
    spør 1) (bli med [x] (nummer 2))) og vent
    hvis <(svar) = ((nummer 1) * (nummer 2))> så
        si [ja! :)] for (2) sekunder
    annet
        si [nei :(] for (2) sekunder
    ende
ende
```

\--- / hint \--- \--- / hint \---

\--- / oppgave \---