## Kihívás: verseny 10 pontra

Megváltoztathatja a játékát úgy, hogy a játékos, ahelyett, hogy 30 másodpercen belül annyi kérdésre válaszolna, a lehető leggyorsabban válaszoljon 10 kérdésre.

A módosításhoz csak az időzítő kódját kell módosítania. Láthatja, hogy melyik blokkoknak másnak kell lenniük?

```blocks3
    mikor kapok [start v]
    beállítást [idő v] - (30)
    ismétlés, amíg <(idő) = [0]>
        várakozás (1) másodperc
        változtatás [idő v] a (-1)
    vég
    sugárzás (vége) v)
```