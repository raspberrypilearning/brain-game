## Kérdések létrehozása

Először véletlenszerű kérdéseket hoz létre, amelyeket a játékosnak meg kell válaszolnia.

\--- feladat \---

Nyisson meg egy új Scratch projektet.

**Online:** open a new online Scratch project at [rpf.io/scratch-new](http://rpf.io/scratch-new){:target="_blank"}.

**Offline:** új projektet nyit meg az offline szerkesztőben.

Ha le kell töltenie és telepítenie kell a Scratch offline szerkesztőt, akkor azt [rpf.io/scratchoff](http://rpf.io/scratchoff){: target = "_ blank"} címen találja meg.

\--- / feladat \---

\--- task \--- Adjunk hozzá egy karaktergömböt és egy hátteret a játékhoz. Kiválaszthatja a tetszését! Íme egy példa:

![screenshot](images/brain-setting.png)

\--- / feladat \---

\--- task \--- Győződjön meg róla, hogy kiválasztottad a karakteredet. Hozzon létre két új változót, az úgynevezett `szám 1`{: class = "block3variables"} és `szám 2`{: class = "block3variables"}, hogy tárolja a számokat a kvíz kérdésekhez.

![screenshot](images/giga-sprite.png) ![screenshot](images/brain-variables.png)

[[[generic-scratch3-add-variable]]]

\--- / feladat \---

\--- feladat \--- kódot megadni a karakter sprite beállítani mindkét `változó`{: class = "block3variables"}, hogy a `random`{: class = "block3operators"} száma 2 és 12 közötti.

![screenshot](images/giga-sprite.png)

```blocks3
amikor a zászló a
kattint, a [szám 1 v] -ra állította (véletlenszerűen (2) - (12))
állítsa be a [2-es szám] -t (válassza ki a véletlenszerű (2) - (12) -et)
```

\--- / feladat \---

\--- task \--- Kód hozzáadása `kérés`{: class = "block3sensing"} a válaszhoz, majd `mondjuk 2 másodpercig`{: class = "block3looks"}, hogy a válasz helyes-e vagy rossz:

![screenshot](images/giga-sprite.png)

```blocks3
amikor a jelző
kattint, a [szám 1 v] -ra állította (véletlenszerűen (2) - (12))
állítsa be a [2-es szám] -t (véletlenszerű (2) -ig (12))

+ kérje (csatlakozzon (1. szám)) (csatlakozzon az [x] -hez (2-es szám))) és várjon
+, ha <(válasz) = ((1-es szám) * (2. szám))> majd
+ mondja [igen! :)] (2) másodpercig
+
+ mondjuk [nem :(] (2) másodpercig
+ vége
```

\--- / feladat \---

\--- feladat \---

Tesztelje a projektet kétszer: helyesen válaszoljon egy kérdésre, a másik helytelenül.

\--- / feladat \---

\--- feladat \---

Adjon hozzá egy `forever`{: class = "block3control"} hurkot a kód köré, hogy a játék egy sor kérdésben kéri a játékosokat.

\--- hints \--- \--- tipp \---

Hozzá kell adnunk egy `forever`{: class = "block3control"} blokkot, és az összes kódot, kivéve a `amikor a`{: class = "block3control"} blokkot rákattintott rá.

\--- / tipp \--- \--- tipp \--- Itt van a szükséges blokk:

```blocks3
örökre
vég
```

\--- / hint \--- \--- tipp \--- Íme, hogy milyen legyen a kódod:

```blocks3
amikor a jelző

+ örökre
    állított be [1-es szám] -ra (véletlenszerű (2) -ig (12))
    állítsa be a [2-es számot] a (véletlenszerű (2) -ig (12))
    kérjen (csatlakozzon (szám) 1) (csatlakozzon az [x] -hez (2-es szám))) és várjon
    ha <(válasz) = ((1-es szám) * (2. szám))> majd
        mondja [igen! :)] (2) másodpercig
    más
        mondjuk [no :(] (2) másodperc
    vég
végére
```

\--- / tipp \--- \--- / hints \---

\--- / feladat \---