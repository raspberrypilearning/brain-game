## Vytvorte otázky

Začnete tým, že vytvoríte náhodné otázky, ktoré musí hráč odpovedať.

\--- úloha \---

Otvorte nový projekt Scratch.

**Online:** open a new online Scratch project at [rpf.io/scratch-new](http://rpf.io/scratchon){:target="_blank"}.

**Offline:** otvorte nový projekt v režime offline.

Ak potrebujete stiahnuť a nainštalovať editor Scratch offline, môžete ho nájsť na adrese [rpf.io/scratchoff](http://rpf.io/scratchoff){: target = "_ blank"}.

\--- / úloha \---

\--- task \--- Pridajte postavu sprite a pozadie pre hru. Môžete si vybrať ľubovoľné! Tu je príklad:

![screenshot](images/brain-setting.png)

\--- / úloha \---

\--- task \--- Uistite sa, že ste vybrali vašu postavu sprite. Vytvorte dve nové premenné, nazývané `číslo 1`{: class = "block3variables"} a `number 2`{: class = "block3variables"}, aby ste uložili čísla pre otázky kvízu.

![screenshot](images/giga-sprite.png) ![screenshot](images/brain-variables.png)

[[[generic-scratch3-add-variable]]]

\--- / úloha \---

\--- úloha \--- pridať kód svojej postave pohyblivému symbolu nastaviť obe `premenných`{: class = "block3variables"} do `náhodných`{: class = "block3operators"} číslo od 2 do 12.

![screenshot](images/giga-sprite.png)

```blocks3
keď príznak kliknutí
sadu [číslo 1] pre (vybrať náhodné (2) až (12)),
sada [číslo 2] pre (vyberať náhodne (2) až (12))
```

\--- / úloha \---

\--- úloha \--- Pridajte kód na `spýtajte sa`{: class = "block3sensing"} pre odpoveď prehrávača a potom `na 2 sekundy`{: class = "block3looks"}, či bola odpoveď správna alebo zle:

![screenshot](images/giga-sprite.png)

```blocks3
keď príznak kliknutí
sadu [číslo 1] pre (vybrať náhodné (2) až (12)),
sada [číslo 2] pre (vyberať náhodne (2) až (12))

+ požiadať (pripojiť (číslo 1) (spojiť [x] (číslo 2))) a čakať
+ ak <(odpoveď) = (číslo 1) * (číslo 2)> a
+ :)] za (2) sekundy
+ iný
+ povedať [no :(] za (2) sekundy
+ koniec
```

\--- / úloha \---

\--- úloha \---

Otestujte svoj projekt dvakrát: odpovedzte na jednu otázku správne a druhú nesprávne.

\--- / úloha \---

\--- úloha \---

Pridajte okruh `navždy`{: class = "block3control"} okolo tohto kódu, aby sa hra spýtala hráča veľa otázok v rade.

\--- rady \--- \--- názov \---

Musíte pridať blok `navždy`{: class = "block3control"} a vložiť všetok kód okrem `keď do nej zablokujete vlajku`{: class = "block3control"}.

\--- / hint \--- \--- tip \--- Tu je blok, ktorý potrebujete:

```blocks3
navždy
koniec
```

\--- / hint \--- \--- tip \--- Tu je to, ako mal by váš kód vyzerať:

```blocks3
keď príznak kliknutí

+ navždy
    sada [číslo 1] pre (vybrať náhodné (2) až (12))
    sady [číslo 2] pre (vybrať náhodné (2) až (12)),
    požiadať (pripojiť (číslo 1) (spojiť [x] (číslo 2))) a čakajte
    ak <(odpoveď) = ((číslo 1) * (číslo 2))> potom
        povedzte [yes! :)] za (2) sekundy
    inak
        povedať [no :(] za (2) sekundy
    koniec
koniec
```

\--- / náznak \--- \--- / rady \---

\--- / úloha \---