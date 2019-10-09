## Mange spil

Nu skal du tilføje en 'Play' -knap, så spilleren kan spille dit spil mange gange.

\--- opgave \--- Opret en ny 'Play' knap sprite, som afspilleren skal klikke for at starte et nyt spil.

Du kan tegne sprite dig selv eller redigere et sprite fra biblioteket.

![Billede af afspilningsknappen](images/brain-play.png)

\--- /task \---

\--- opgave \--- Føj denne kode til din knap sprite:

![Button sprite](images/button-sprite.png)

```blocks3
    når flag klikket
    viser

    da dette sprite klikket
    skjul
    udsendelser (start v)
```

\--- /task \---

Den nye kode indeholder en anden `udsendt`{: class = "block3events"} blok, som sender meddelelsen 'start'.

Den nye kode gør 'Play' knappen sprite show, når spilleren klikker på flag. Når afspilleren klikker på knappen sprite, skjuler sprite og sender derefter en besked, som andre sprites kan reagere på.

I øjeblikket begynder tegnsprogen at stille spørgsmål, når spilleren klikker på flagget. Skift dit spil kode, så tegnsprite begynder at stille spørgsmål, når den modtager 'start' `udsendelsen`{: class = "block3events"}.

\--- opgave \--- Vælg din tegnsprit og erstat `når flag klikket`{: class = "block3events"} bloker med en `når jeg modtager start`{: class = "block3events" } blok.

![Character sprite](images/giga-sprite.png)

```blocks3
<br />- når flag klikker
+ når jeg modtager [start v]
sæt [nummer 1 v] til (vælg tilfældigt (2) til (12))
sæt [nummer 2 v] til (vælg tilfældigt (2) til (12) )
spørg (join nummer 1) (join [x] (nummer 2))) og vent
hvis <(svar) = ((nummer 1) * (nummer 2))> så
    siger [ja! :)] for (2) sekunder
andet
    siger [nope :(] for (2) sekunder
ende
```

\--- /task \---

\--- task \---

Klik på det grønne flag, og klik derefter på den nye 'Afspil' knap for at teste om det virker. Du skal se, at spillet ikke starter, før du klikker på knappen.

\--- /task \---

Kan du se, at timeren starter, når det grønne flag klikkes, i stedet for når spillet starter?

![Timeren er startet](images/brain-timer-bug.png)

\--- task \---

Kan du ændre koden til timeren, så timeren starter, når afspilleren klikker på knappen?

\--- /task \---

\--- opgave \--- Tilføj kode til din knap sprite, så knappen vises igen i slutningen af hvert spil.

![Button sprite](images/button-sprite.png)

```blocks3
    når jeg modtager [end v]
    show
```

\--- /task \---

\--- task \---

Test 'Play' knappen ved at spille et par spil. Knappen skal vise i slutningen af hvert spil.

For at teste spillet hurtigere kan du ændre værdien på `time`{: class = "block3variables"}, så hvert spil er kun få sekunder lang.

![Scene](images/stage-sprite.png)

```blocks3
    indstil [tid v] til [10]
```

\--- /task \---

\--- opgave \--- Du kan ændre, hvordan knappen ser ud, når musemarkøren svæver over den.

![Knap](images/button-sprite.png)

```blocks3
    når flag klikket
    viser
    evigt
    hvis <touching (mouse-pointer v)?> derefter
        sæt [fisheye v] effekt til (30)
    andet
        sæt [fisheye v] effekt til (0)
    ende
    ende
```

![skærmbillede](images/brain-fisheye.png) \--- /task \---