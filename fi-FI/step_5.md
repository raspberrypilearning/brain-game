## Useita pelejä

Nyt lisäät Play-painikkeen, jotta pelaaja voi pelata peliäsi monta kertaa.

\--- tehtävä \--- Luo uusi 'Play' -painike, jota pelaaja tarvitsee napsauttamalla aloittaakseen uuden pelin.

Voit piirtää sprite itse tai muokata spriteä kirjastosta.

![Kuva toistopainikkeesta](images/brain-play.png)

\--- / tehtävä \---

\--- tehtävä \--- Lisää tämä koodi painikkeeseesi:

![Button sprite](images/button-sprite.png)

```blocks3
    kun lippu napsautti
    näyttää

    kun tämä sprite napsautti
    piilota
    lähetystä (alku v)
```

\--- / tehtävä \---

Uusi koodi sisältää toisen `lähetyksen`{: class = "block3events"}, joka lähettää viestin "start".

Uusi koodi tekee Play-painikkeen sprite-näyttelystä, kun pelaaja napsauttaa lippua. Kun pelaaja napsauttaa painiketta sprite, sprite piilottaa ja lähettää sitten viestin, jonka mukaan muut spritit voivat reagoida.

Tällä hetkellä merkki sprite alkaa kysyä kysymyksiä, kun pelaaja napsauttaa lippua. Muuta pelisi koodia niin, että hahmon sprite alkaa kysyä kysymyksiä, kun se vastaanottaa ' `' lähetyksen`{: class = "block3events"}.

\--- tehtävä \--- Valitse hahmosi sprite ja korvaa sen koodiosassa `kun lippu napsautti`{: class = "block3events"} lohkolla `kun saan aloituksen`{: class = "block3events" } lohko.

![Merkin sprite](images/giga-sprite.png)

```blocks3
<br />- kun lippu napsautti
+, kun saan [start v]
valitse [numero 1 v] (valitse satunnainen (2) - (12))
aseta [numero 2 v] (valitse satunnainen (2) - (12) )
kysy (liity (numero 1) (liity [x] (numero 2))) ja odota
jos <(vastaus) = ((numero 1) * (numero 2))> sitten
    sanoa [kyllä! :)] (2) sekunnin ajan
muu
    sanoa [nope :(] (2) sekunnin
päähän
```

\--- / tehtävä \---

\--- tehtävä \---

Napsauta vihreää lippua ja napsauta sitten uutta 'Toista' -painiketta testataksesi, toimiiko se. Sinun pitäisi nähdä, että peli ei käynnisty ennen kuin napsautat painiketta.

\--- / tehtävä \---

Näetkö, että ajastin käynnistyy, kun vihreää lippua napsautetaan sen sijaan, että peli alkaa?

![Ajastin on alkanut](images/brain-timer-bug.png)

\--- tehtävä \---

Voitko muuttaa ajastimen koodia niin, että ajastin käynnistyy, kun pelaaja napsauttaa painiketta?

\--- / tehtävä \---

\--- tehtävä \--- Lisää koodi painikkeeseesi niin, että painike näkyy uudelleen kunkin pelin lopussa.

![Button sprite](images/button-sprite.png)

```blocks3
    kun saan [lop. v]
    näyttää
```

\--- / tehtävä \---

\--- tehtävä \---

Testaa Play-painiketta pelaamalla pari peliä. Painikkeen pitäisi näkyä kunkin pelin lopussa.

Jos haluat testata peliä nopeammin, voit muuttaa arvoa `aika`{: class = "block3variables"} niin, että jokainen peli on vain muutaman sekunnin pituinen.

![vaihe](images/stage-sprite.png)

```blocks3
    aseta [aika v] - arvoksi [10]
```

\--- / tehtävä \---

\--- tehtävä \--- Voit muuttaa, miten painike näyttää, kun hiiren osoitin liikkuu sen yli.

![nappi](images/button-sprite.png)

```blocks3
    kun lippu napsautti
    näyttää
    ikuisesti
    jos <touching (mouse-pointer v)?> sitten
        asettaa [kalansilmä v] vaikutus (30)
    muuta
        aseta [kalansilmä v] vaikutus (0)
    loppuun
    loppuun
```

![kuvakaappaus](images/brain-fisheye.png) \--- / tehtävä \---