## Több játék

Most hozzáad egy "Play" gombot, hogy a játékos sokszor játszhasson a játékban.

\--- task \--- Hozzon létre egy új 'Play' gombot, amire a játékosnak szüksége van egy új játék elindításához.

A Sprite-ot magad is rajzolhatod, vagy szerkeszthetsz egy sprite-ot a könyvtárból.

![A lejátszás gomb képe](images/brain-play.png)

\--- / feladat \---

\--- task \--- Adja hozzá ezt a kódot a gomb sprite-hez:

![Button sprite](images/button-sprite.png)

```blocks3
    amikor zászló kattintott
    mutatják

    , ha ez a szellem kattintottak
    hide
    adás (start v)
```

\--- / feladat \---

Az új kód egy másik `sugárzást tartalmaz`{: class = "block3events"} blokkot, amely elküldi az "start" üzenetet.

Az új kód a „Play” gomb sprite-t mutatja, amikor a játékos rákattint a zászlóra. Amikor a játékos rákattint a sprite-ra, a sprite elrejti és aztán üzenetet küld, hogy más spritek reagálhatnak.

Abban a pillanatban, a karakter sprite elkezdi kérdéseket feltenni, amikor a játékos rákattint a zászlóra. Változtassa meg a játékkódját úgy, hogy a karakterlövész megkérdezzen kérdéseket, amikor megkapja a ' `' sugárzást`{: class = "block3events"}.

\--- task \--- Jelölje ki a karakterláncot, és a kódrészében cserélje ki az `amikor a`jelzésre kattintott: {= class = "block3events"} egy `mal, amikor elkezdem a`indítást {: class = "block3events" } Blokk.

![Karakter sprite](images/giga-sprite.png)

```blocks3
<br />- amikor a zászló +
+ -ra kattintott, amikor [start v]
kapok, állítsuk be a [szám 1 v] -ta (véletlenszerű (2) -ig (12))
állítsuk be a [2-es számot] a (véletlenszerű (2) -ig (12) -ig) )
kérje (csatlakozzon (1. szám) (csatlakozzon az [x] -hez (2-es szám))) és várjon
ha <(válasz) = ((1-es szám) * (2. szám))> majd
    mondja [igen! :)] (2) másodpercig
más
    mondja [nope :(] (2) másodperc
végére
```

\--- / feladat \---

\--- feladat \---

Kattintson a zöld zászlóra, majd kattintson az új "Play" gombra, hogy tesztelje, hogy működik-e. Látnia kell, hogy a játék nem indul el, mielőtt a gombra kattint.

\--- / feladat \---

Láthatja, hogy az időzítő akkor kezdődik, amikor a zöld zászlót rákattintják ahelyett, hogy a játék elindulna?

![Megkezdődött az időzítő](images/brain-timer-bug.png)

\--- feladat \---

Megváltoztathatja az időzítő kódját, hogy az időzítő elinduljon, amikor a játékos rákattint a gombra?

\--- / feladat \---

\--- task \--- Add kódot a gomb sprite-hez, hogy a gomb ismét megjelenik a játék végén.

![Button sprite](images/button-sprite.png)

```blocks3
    mikor megkapom a [vége v]
    show-t
```

\--- / feladat \---

\--- feladat \---

Teszteld a 'Play' gombot néhány játék lejátszásával. A gombnak minden játék végén meg kell jelennie.

A játék gyorsabb teszteléséhez módosíthatja a `time`{: class = "block3variables"} értékét, hogy minden játék csak néhány másodperc legyen.

![Színpad](images/stage-sprite.png)

```blocks3
    állítsa be az [idő v] értékét [10]
```

\--- / feladat \---

\--- task \--- Megváltoztathatja, hogyan néz ki a gomb, amikor az egérmutató fölé mozog.

![Gomb](images/button-sprite.png)

```blocks3
    ha a jelző
    kattint,
    örökre
    ha <touching (mouse-pointer v)?> majd
        állítsa be a [halszem v] hatást (30)
    másikra
        állítsa be a [halszem v] hatást a (0)
    vég
    végére
```

![screenshot](images/brain-fisheye.png) \--- / feladat \---