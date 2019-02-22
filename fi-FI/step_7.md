## Lisää grafiikkaa

Tällä hetkellä hahmo sprite sanoo vain `kyllä! :)` tai `ei :(` pelaajan vastauksiin. Lisää grafiikkaa, jotta pelaaja tietää, onko heidän vastauksensa oikea tai virheellinen.

\--- tehtävä \---

Luo uusi sprite nimeltään "Tulos" ja anna sille "rasti / tarkista" ja "rajat" puku.

![Sprite, jossa on rasti ja ristipuvut](images/brain-result.png)

\--- / tehtävä \---

\--- tehtävä \---

Muuta hahmosi sprite-koodia niin, että sen sijaan, että sanoisit jotain soittimelle, se `lähettää`{: class = "block3events"} viestejä "oikein" tai "vääräksi".

![Merkin sprite](images/giga-sprite.png)

```blocks3
jos <(vastaus) = ((numero 1) * (numero 2))> ja

- sano [kyllä! :)] (2) sekunnin ajan
+ lähetys (oikea v)
muu
- sano [nope :(] (2) sekunnin ajan
+ lähetys (väärä v)
loppuun
```

\--- / tehtävä \---

\--- tehtävä \---

Nyt voit käyttää näitä viestejä `osoittamaan`{: class = "block3looks"} "tick" tai "cross" -vaatteita. Lisää seuraava koodi Tulos-sprite:

![Tulos sprite](images/result-sprite.png)

```blocks3
    kun saan [oikea v]
    kytkin puku (rasti v)
    näytä
    odota (1) sekuntia
    piilota

    kun saan [väärin v]
    kytkimen puku (rajat v)
    näytä
    odota (1) sekuntia
    piilota

    kun lippu napsautti
    piiloutua
```

\--- / tehtävä \---

\--- task \--- Testaa peliä uudelleen. Sinun pitäisi nähdä rasti aina, kun vastaat kysymykseen oikein, ja risti aina, kun vastaat väärin!

![Merkitse oikea, risti väärää vastausta varten](images/brain-test-answer.png)

\--- / tehtävä \---

Näetkö, että koodi `kun saan oikean`{: class = "block3events"} ja `kun saan väärän`{: class = "block3events"} on lähes identtinen?

Voit siis muuttaa koodiasi helpommin, luodaan mukautetun lohkon.

\--- tehtävä \---

Valitse 'Tulos' sprite. Napsauta sitten `My Blocks`{: class = "block3myblocks"} ja sitten **Tee lohko**. Luo uusi lohko ja kutsu se `animoi`{: class = "block3myblocks"}.

![Tulos sprite](images/result-sprite.png)

![Luo animaattiseksi kutsuttu lohko](images/brain-animate-function.png)

\--- / tehtävä \---

\--- tehtävä \--- Siirrä koodi `esitykseen`{: class = "block3looks"} ja `piilota`{: class = "block3looks"} 'tuloksen' sprite `animate`{: class = " block3myblocks "} lohko:

![Tulos sprite](images/result-sprite.png)

```blocks3
määritellä animate
Näytä
odota (1) sekuntia
piilota
```

\--- / tehtävä \---

\--- tehtävä \--- Varmista, että olet poistanut `näyttää`{: class = "block3looks"} ja `piilota`{: class = "block3looks"} lohkojen alle **sekä** ja `kytkimen puku`{: class = "block3looks"} lohkot.

Lisää sitten `animate`{: class = "block3myblocks"} lohko molempien `kytkinpuvun`{: class = "block3looks"} lohkojen alle. Koodisi pitäisi nyt näyttää tältä:

![Tulos sprite](images/result-sprite.png)

```blocks3
    kun saan [oikea v]
    -kytkimen puku (rasti v)
    animoi :: custom

    kun saan [väärin v]
    kytkinpukua (ristiin)
    animate :: custom
```

\--- / tehtävä \---

Custom `animate`{: class = "block3myblocks"} -lohkon takia sinun on nyt tehtävä vain yksi muutos koodiin, jos haluat näyttää tuloksen sprite-puvut pidempään tai lyhyempään aikaan.

\--- tehtävä \---

Muuta koodia niin, että "rasti" tai "rajat" puvut näkyvät 2 sekunnin ajan.

\--- / tehtävä \---

\--- tehtävä \--- Sen sijaan, että `näyttää`{: class = "block3looks"} ja `piiloutua`{: class = "block3looks"}, voit valita `animate`{: class = "block3myblocks"} lohko niin, että puvut haalistuvat.

![Tulos sprite](images/result-sprite.png)

```blocks3
    määritä animaatio
    sarja [ghost v] -toiminto (100)
    näytä
    toistoa (25)
        muutos [ghost v] vaikutus (-4)
    loppuun
    piilota
```

\--- / tehtävä \---

Voisitko parantaa "tick" - tai "cross" -grafiikan animaatiota? Voit lisätä koodin, jotta puvut häviävät, tai voit käyttää muita viileitä vaikutuksia:

![kuvakaappaus](images/brain-effects.png)