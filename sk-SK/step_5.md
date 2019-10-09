## Viacnásobné hry

Teraz pridáte tlačidlo "Prehrať", aby hráč mohol hrať vašu hru veľa krát.

\--- task \--- Vytvorenie nového tlačidla "Play", ktoré musí hráč kliknúť, aby spustil novú hru.

Môžete nakresliť sprite sami alebo upraviť sprite z knižnice.

![Obrázok tlačidla prehrávania](images/brain-play.png)

\--- / úloha \---

\--- task \--- Pridajte tento kód do vášho tlačidla sprite:

![Button sprite](images/button-sprite.png)

```blocks3
    keď klaksón klikne
    zobrazí

    keď tento sprite klikol
    skryť
    vysielanie (štart v)
```

\--- / úloha \---

Nový kód obsahuje ďalší blok `vysielania`{: class = "block3events"}, ktorý odošle správu "štart".

Nový kód spôsobí, že tlačidlo Play (Hra) sa zobrazuje, keď hráč klikne na príznak. Keď hráč klikne na tlačidlo Sprite, skript sa skryje a potom vysiela správu, na ktorú môžu reagovať iné scény.

V súčasnej dobe spriahnutá postava začína klásť otázky, keď hráč klikne na príznak. Zmeňte kód svojej hry tak, aby spriaty znak začal klásť otázky, keď dostane vysielanie "štart" ``{: class = "block3events"}.

\--- úloha \--- Zvoľte svoj znakový sprite a v jeho sekcii kód nahraďte `keď klepnete na blok`{: class = "block3events"} a `pri prijatí štartu`{: class = "block3events" } blok.

![Sprite znakov](images/giga-sprite.png)

```blocks3
<br />- ak príznak ukážete
+ keď dostanem [start v]
nastaviť [číslo 1 v] na (vybrať náhodné (2) až (12))
nastaviť [číslo 2 v] )
pýtať (join (číslo 1) (pripojiť [x] (číslo 2))) a počkajte
v prípade <(odpoveď) = ((číslo 1) * (číslo 2))> potom
    povedať [áno! :)] za (2) sekundy
inak
    povedal [nope :(] za (2) sekundy
koniec
```

\--- / úloha \---

\--- úloha \---

Kliknite na zelenú vlajku a potom kliknite na nové tlačidlo "Prehrať" a otestujte, či to funguje. Mali by ste vidieť, že hra sa nespustí predtým, ako kliknete na tlačidlo.

\--- / úloha \---

Vidíte, že časovač sa spúšťa po kliknutí na zelenú vlajku namiesto toho, kedy sa začne hra?

![Časovač začal](images/brain-timer-bug.png)

\--- úloha \---

Môžete zmeniť kód časovača tak, aby sa časovač spustil, keď hráč klikne na tlačidlo?

\--- / úloha \---

\--- task \--- Pridajte kód do vášho tlačidla Sprite tak, aby sa tlačidlo znovu zobrazilo na konci každej hry.

![Button sprite](images/button-sprite.png)

```blocks3
    keď dostanem [end v]
    show
```

\--- / úloha \---

\--- úloha \---

Otestujte tlačidlo "Play" tak, že budete hrať pár hier. Tlačidlo by sa malo zobraziť na konci každej hry.

Ak chcete hru otestovať rýchlejšie, môžete zmeniť hodnotu `času`{: class = "block3variables"} tak, aby každá hra mala iba niekoľko sekúnd.

![štádium](images/stage-sprite.png)

```blocks3
    nastavte čas [v] na [10]
```

\--- / úloha \---

\--- task \--- Môžete zmeniť spôsob, akým tlačidlo vyzerá, keď sa nad ním pohybuje ukazovateľ myši.

![gombík](images/button-sprite.png)

```blocks3
    keď vlajka klikne
    zobrazí
    navždy
    ak <touching (mouse-pointer v)?> potom
        nastaviť [rybie oko] efekt na (30)
    iný
        nastaviť [rybie oko] efekt na (0)
    koniec
    koniec
```

![screenshot](images/brain-fisheye.png) \--- / úloha \---