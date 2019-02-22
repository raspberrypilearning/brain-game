## Legg til grafikk

For øyeblikket sier karaktersprite bare `ja! :)` eller `no :(` til spillerens svar. Legg til litt grafikk for å la spilleren vite om svaret deres er riktig eller feil.

\--- oppgave \---

Opprett en ny sprite som heter 'Resultat', og gi den en 'tick / check' og en 'cross' kostyme.

![Sprite med kryss og kryss kostymer](images/brain-result.png)

\--- / oppgave \---

\--- oppgave \---

Endre karakterskiltens kode slik at, i stedet for å si noe til spilleren, sender ``{: class = "block3events"} meldingene "riktig" eller "feil".

![Character sprite](images/giga-sprite.png)

```blocks3
hvis <(svar) = ((nummer 1) * (nummer 2))> deretter

- si [ja! :)] for (2) sekunder
+ kringkasting (riktig v)
andre
- si [nope :(] for (2) sekunder
+ kringkasting (feil v)
ende
```

\--- / oppgave \---

\--- oppgave \---

Nå kan du bruke disse meldingene til `vise`{: class = "block3looks"} 'tick' eller 'cross' kostyme. Legg til følgende kode i resultatruten:

![Resultat sprite](images/result-sprite.png)

```blocks3
    når jeg mottar [feil v]
    byttekostyme til (kryss v)
    vis
    vent (1) sekunder
    skjul

    når jeg mottar [feil v]
    bryter kostyme til (kryss v)
    vis
    vente (1) sekunder
    skjul

    når flagget klikket
    skjul
```

\--- / oppgave \---

\--- Oppgave \--- Test spillet ditt igjen. Du bør se krysset når du svarer på et spørsmål riktig, og krysset når du svarer feil!

![Kryss for korrekt, kryss for feil svar](images/brain-test-answer.png)

\--- / oppgave \---

Kan du se at koden for `når jeg mottar riktig`{: class = "block3events"} og `når jeg mottar feil`{: class = "block3events"} er nesten identisk?

Så du kan endre koden din lettere, du skal lage en egendefinert blokk.

\--- oppgave \---

Velg "Resultat" sprite. Deretter klikker du på `Mine blokker`{: class = "block3myblocks"}, og deretter på **Lag en blokk**. Opprett en ny blokk og ring den `animere`{: class = "block3myblocks"}.

![Resultat sprite](images/result-sprite.png)

![Lag en blokk som kalles animere](images/brain-animate-function.png)

\--- / oppgave \---

\--- oppgave \--- Flytt koden til `vis`{: class = "block3looks"} og `skjul`{: class = "block3looks"} "Resultat" sprite i `animere`{: class = " block3myblocks "} blokk:

![Resultat sprite](images/result-sprite.png)

```blocks3
definer animere
vis
vent (1) sekunder
skjul
```

\--- / oppgave \---

\--- Oppgave \--- Kontroller at du har fjernet `Vis`{: class = "block3looks"} og `skjul`{: class = "block3looks"} Blokker under **begge** av `byttekostyme`{: class = "block3looks"} blokker.

Deretter legger du til `animere`{: class = "block3myblocks"} -blokken under begge de `bryterkostymen`{: class = "block3looks"} blokkene. Koden din skal nå se slik ut:

![Resultat sprite](images/result-sprite.png)

```blocks3
    når jeg mottar [korrekt v]
    byttekostyme til (kryss v)
    animate :: tilpasset

    når jeg mottar [feil v]
    byttekostyme til (kryss v)
    animere :: tilpasset
```

\--- / oppgave \---

På grunn av den tilpassede `animere`{: class = "block3myblocks"} -blokken, trenger du nå bare å gjøre en endring til koden din hvis du vil vise «Resultat» -spritens kostymer en lengre eller kortere tid.

\--- oppgave \---

Endre koden din slik at "tick" eller "cross" kostymer vises i 2 sekunder.

\--- / oppgave \---

\--- oppgave \--- I stedet for `viser`{: class = "block3looks"} og `gjemmer`{: class = "block3looks"} 'tick' eller 'cross' kostymer, kan du endre dine `animate`{: class = "block3myblocks"} blokkere slik at kostymer falmer inn.

![Resultat sprite](images/result-sprite.png)

```blocks3
    definer animere
    sett [spøkelse v] effekt til (100)
    vis
    gjenta (25)
        endre [spøkelse v] effekt av (-4)
    ende
    skjul
```

\--- / oppgave \---

Kan du forbedre animasjonen av "tick" eller "cross" grafikken? Du kan legge til koden for å få kostymer til å falle ut, eller du kan bruke andre, kule effekter:

![skjermbilde](images/brain-effects.png)