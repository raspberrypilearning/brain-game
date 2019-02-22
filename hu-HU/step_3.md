## Idõzítõ hozzáadása

\--- task \--- Hozzon létre egy visszaszámlálót a színpadon egy új, `idő`{: class = "block3variables"} változó segítségével. Az időzítőnek 30 másodpercig kell kezdődnie, és 0 másodpercre kell számítania.

![Színpad sprite](images/stage-sprite.png)

\--- hints \--- \--- tipp \---

Létrehozása `változó`{: class = "block3variables"}, nevezzük 'idő', és az értékét a `30`.

Ezután adjunk hozzá egy kódot `idő`számlálásához {: class = "block3variables"} 0-ra 30 másodpercen belül. Ehhez kivonjuk a `1` -et ``{: class = "block3variables"} minden `1` másodpercben, és ismételjük meg ezt `ig`ig </code> {: class = "block3variables"} egyenlő `0`.

\--- / tipp \--- \--- tipp \--- Íme a szükséges blokkok:

```blocks3
ismételje meg addig, amíg < >

vége

várakozás (1) másodperc

változtatás [idő v] (1)

(idő)

amikor a zászlóra kattintott

<() = ()>

beállítva [idő v] - [0]
```

\--- / tipp \--- \--- tipp \--- Itt az, amit az új kódnak kell kinéznie:

```blocks3
ha a jelző
állított [idő v] [30]
ismételve, amíg <(idő) = (0)>
    várakozás (1) másodperc
    változtatás [idő v] a (-1)
végével
```

\--- / tipp \--- \--- / hints \---

\--- / feladat \---

\--- feladat \---

Hozzon létre egy `sugárzást`{: class = "block3control"}, amely elküldi az üzenetet. A `sugárzás`{: class = "block3control"} olyan, mint egy hangszórón belüli bejelentés: az összes sprites hallható. Adja hozzá a `sugárzás`{: class = "block3control"} blokkot az időzítő kód végéhez, hogy a kód elküldje és a "vége" üzenet, amikor a `idő`{: class = "block3variables"} `0`.

![Színpad sprite](images/stage-sprite.png)

```blocks3
    sugárzás (vége v)
```

\--- / feladat \---

\--- task \--- Válassza ki a karakterláncot, és adjon hozzá néhány kódot, hogy az `es sprite megállítsa a többi`{: class = "block3control"} parancsfájlt, amikor megkapja a `vég`{: class = "block3control"} üzenetet .

![Giga sprite](images/giga-sprite.png)

```blocks3
    mikor kapok [vége v]
    stop [más szkriptek sprite v]
```

\--- / feladat \---

\--- feladat \---

Tesztelje újra a játékot. Folytatni kell a kérdéseket, amíg az időzítő 0-ra nem számít.

\--- / feladat \---