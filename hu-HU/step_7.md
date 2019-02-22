## Grafika hozzáadása

Abban a pillanatban, a karakter sprite csak azt mondja `igen! :)` vagy `nem :(` a játékos válaszaihoz. Adjunk hozzá néhány grafikát, hogy a játékos tudja, hogy helyes-e vagy sem helyes.

\--- feladat \---

Hozzon létre egy új "Sprite" nevet, és adjon neki egy "kullancsot / csekket" és egy "kereszt" jelmezet.

![Sprite kullancs és kereszt jelmezekkel](images/brain-result.png)

\--- / feladat \---

\--- feladat \---

Módosítsa a karakteres sprite kódját úgy, hogy ahelyett, hogy mondaná valamit a játékosnak, `sugároz`{: class = "block3events"} az üzeneteket "helyes" vagy "rossz".

![Karakter sprite](images/giga-sprite.png)

```blocks3
ha <(válasz) = ((1-es szám) * (2. szám))> majd

- mondjuk [igen! :)] (2) másodpercig
+ sugárzás (helyes v)
másik
- mondjuk [nope :(] (2) másodpercre
+ sugárzás (rossz v)
vég
```

\--- / feladat \---

\--- feladat \---

Most már használhatja ezeket az üzeneteket `:`{: class = "block3looks"} a "kullancs" vagy a "kereszt" jelmezre. Adja hozzá a következő kódot az 'Eredmény' Sprite-hoz:

![Eredmény sprite](images/result-sprite.png)

```blocks3
    amikor kapok [helyes v]
    kapcsolót jelmezek (k jelölés)
    show
    várakozás (1) másodperc
    elrejtés

    ha kapok [rossz v]
    kapcsoló jelmez (kereszt v)
    show
    várakozás (1) másodperc
    elrejti a

    amikor a zászló
    kattintott
```

\--- / feladat \---

\--- task \--- Tesztelje újra a játékot. Amikor a kérdésre helyesen válaszol, a kullancsot meg kell látni, és a keresztet, ha helytelenül válaszolsz!

![Jelölje be a helyes, keresztet a helytelen válaszért](images/brain-test-answer.png)

\--- / feladat \---

Láthatjuk, hogy a `kód, ha helyes`{: class = "block3events"} és `ha rosszul kapok`{: class = "block3events"}, majdnem azonos?

Így könnyebben megváltoztathatja a kódját, létrehozhat egy egyéni blokkot.

\--- feladat \---

Jelölje ki az 'Eredmény' spritet. Ezután kattintson a `My Blocks`{: class = "block3myblocks"}, majd a **blokk**. Hozzon létre egy új blokkot, és hívja `animate`{: class = "block3myblocks"}.

![Eredmény sprite](images/result-sprite.png)

![Hozzon létre egy animált blokkot](images/brain-animate-function.png)

\--- / feladat \---

\--- task \--- Mozgassa a kódot `show`{: class = "block3looks"} és `hide`{: class = "block3looks"} az 'Eredmény' Sprite-t az `animate`{: class = " block3myblocks "} blokk:

![Eredmény sprite](images/result-sprite.png)

```blocks3
animate
megjelenítése
várakozás (1) másodperc
elrejtés
```

\--- / feladat \---

\--- feladat \--- Győződjön meg arról, hogy eltávolította a `mutatják`{: class = "block3looks"}, és `elrejtése`{: class = "block3looks"} blokkok alább **mind** a `kapcsoló ruha`{: class = "block3looks"} blokkok.

Ezután adjuk hozzá a `élő`{: class = "block3myblocks"} blokk alatt mind a `kapcsoló ruha`{: class = "block3looks"} blokkok. A kódodnak így kell kinéznie:

![Eredmény sprite](images/result-sprite.png)

```blocks3
    ha [helyes v]
    kapcsolót kapok (jelölje be a v)
    animációt :: custom

    ha [rossz v]
    kapcsolót kapok (kereszt v)
    animáció :: custom
```

\--- / feladat \---

Az egyéni `animate`{: class = "block3myblocks"} blokk miatt most csak egy módosítást kell végrehajtania a kódjához, ha hosszabb vagy rövidebb ideig szeretné megjeleníteni az 'Eredmény' sprite jelmezeit.

\--- feladat \---

Módosítsa a kódot úgy, hogy a „kullancs” vagy a „kereszt” jelmezek 2 másodpercig jelenjenek meg.

\--- / feladat \---

\--- task \--- </code>{: class = "block3looks"} és a `{`:: class = "block3looks"} `megjelenítés helyett a "kullancs" vagy a "kereszt" jelmezek megváltoztathatják az <code>animát`{: class = "block3myblocks"} blokk, hogy a jelmezek elhalványuljanak.

![Eredmény sprite](images/result-sprite.png)

```blocks3
    animate
    set [ghost v] hatás definiálása (100)
    show
    ismétlés (25)
        [ghost v] hatás módosítása (-4)
    vég
    elrejtés
```

\--- / feladat \---

Javíthatja-e a „kullancs” vagy a „kereszt” grafikák animációját? Kódot adhat hozzá, hogy a jelmezek elhalványuljanak, vagy más hűvös hatásokat is használhat:

![screenshot](images/brain-effects.png)