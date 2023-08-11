## Vragen maken

Laten we beginnen met het maken van willekeurige vragen die de speler moet beantwoorden.

\--- task \---

Open een nieuw Scratch project.

**Online:** open a new online Scratch project at [rpf.io/scratch-new](https://rpf.io/scratch-new){:target="_blank"}.

**Offline:** open een nieuw project in de offline editor.

If you need to download and install the Scratch offline editor, you can find it at [rpf.io/scratchoff](https://rpf.io/scratchoff){:target="_blank"}.

\--- /task \---

\--- task \---

Kies een personage en een achtergrond voor je spel. Je kunt kiezen wat je wilt! Hier is een voorbeeld:

![screenshot](images/brain-setting.png)

\--- /task \---

\--- task \---

Zorg ervoor dat je je personage geselecteerd hebt. Maak twee nieuwe variabelen, genaamd `nummer 1`{:class="block3variables"} en `nummer 2`{:class="block3variables"}. Deze variabelen slaan de twee getallen op die samen worden vermenigvuldigd.

![screenshot](images/giga-sprite.png)

![screenshot](images/brain-variables.png)

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- task \---

Voeg code toe aan je personage, om beide `variabelen`{:class="block3variables"} in te stellen op een `willekeurig`{:class="block3operators"} getal tussen 2 en 12.

![screenshot](images/giga-sprite.png)

```blocks3
wanneer groene vlag wordt aangeklikt
maak [nummer 1 v] (willekeurig getal tussen (2) en (12))
maak [nummer 2 v] (willekeurig getal tussen (2) en (12))
```

\--- /task \---

\--- task \---

Voeg code toe waarin je aan de speler om het antwoord `vraagt`{:class="block3sensing"}, en vervolgens `zeg voor 2 seconden`{:class="block3looks"} of het antwoord juist of verkeerd was:

![screenshot](images/giga-sprite.png)

```blocks3
wanneer groene vlag wordt aangeklikt
maak [nummer 1 v] (willekeurig getal tussen (2) en (12))
maak [nummer 2 v] (willekeurig getal tussen (2) en (12))

+ vraag (voeg (nummer 1) en (voeg [ x ] en (nummer 2) samen) samen) en wacht
+ als <(antwoord) = ((nummer 1) * (nummer 2))> dan 
+ zeg [goed! :)] (2) seconden
+ anders
+ zeg [fout :(] (2) sec.
+ einde
```

\--- /task \---

\--- task \---

Test jouw project twee keer: beantwoord de ene vraag goed en de andere verkeerd.

\--- /task \---

\--- task \---

Voeg een `herhaal`{:class="block3control"} lus toe aan de code, zodat de speler veel vragen achter elkaar krijgt.

\--- hints \---

\--- hint \---

Je moet een `herhaal`{:class="block3control"} blok toevoegen en alle code behalve de `wanneer groene vlag wordt aangeklikt`{:class="block3control"} daar naartoe verplaatsen.

\--- /hint \---

\--- hint \---

Dit is het blok dat je nodig hebt:

```blocks3
herhaal
einde
```

\--- /hint \---

\--- hint \---

Dit is hoe je code eruit zou moeten zien:

```blocks3
wanneer groene vlag wordt aangeklikt

+ herhaal
   maak [nummer 1 v] (willekeurig getal tussen (2) en (12))
   maak [nummer 2 v] (willekeurig getal tussen (2) en (12))
   vraag (voeg (nummer 1) en (voeg [ x ] en (nummer 2) samen) samen) en wacht
   als <(antwoord) = ((nummer 1) * (nummer 2))> dan 
     zeg [goed! :)] (2) sec.
    anders
        zeg [fout :(] (2) sec.
    einde
einde
```

\--- /hint \---

\--- /hints \---

\--- /task \---