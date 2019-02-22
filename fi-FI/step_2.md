## Luo kysymyksiä

Aloitatte luomalla satunnaisia kysymyksiä, jotka pelaajan on vastattava.

\--- tehtävä \---

Avaa uusi Scratch-projekti.

**Online:** avaa uusi online-Scratch-projekti osoitteessa [rpf.io/scratchon](http://rpf.io/scratchon){: target = "_ blank"}.

**Offline:** avaa uuden projektin offline-editorissa.

Jos haluat ladata ja asentaa Scratch offline -editorin, löydät sen osoitteesta [rpf.io/scratchoff](http://rpf.io/scratchoff){: target = "_ blank"}.

\--- / tehtävä \---

\--- tehtävä \--- Lisää hahmo-sprite ja taustan peliin. Voit valita haluamasi! Tässä esimerkki:

![kuvakaappaus](images/brain-setting.png)

\--- / tehtävä \---

\--- tehtävä \--- Varmista, että olet valinnut hahmon sprite. Luo kaksi uutta muuttujaa, joita kutsutaan nimellä `numero 1`{: class = "block3variables"} ja `numero 2`{: class = "block3variables"}, tallentaa tietokilpailujen numerot.

![kuvakaappaus](images/giga-sprite.png) ![kuvakaappaus](images/brain-variables.png)

[[[generic-scratch3-add-variable]]]

\--- / tehtävä \---

\--- tehtävä \--- Lisää koodin hahmosi sprite-asetukseen asettamaan molemmat `muuttujaa`{: class = "block3variables"} `satunnaiseksi`{: class = "block3operators"} numeroksi 2 - 12.

![kuvakaappaus](images/giga-sprite.png)

```blocks3
kun lippu napsautti
asettaa [numero 1 v] (valitse satunnainen (2) - (12))
aseta [numero 2 v] (valitse satunnainen (2) - (12))
```

\--- / tehtävä \---

\--- tehtävä \--- Lisää koodi `kyselyyn`{: class = "block3sensing"} soittimeen vastausta varten ja sitten `sanoa 2 sekunnin ajan`{: class = "block3looks"} onko vastaus oikea vai väärä:

![kuvakaappaus](images/giga-sprite.png)

```blocks3
kun lippu napsautti
asettaa [numero 1 v] (valitse satunnainen (2) - (12))
aseta [numero 2 v] (valitse satunnainen (2) - (12))

+ kysy (liity (numero 1)) (liity [x] (numero 2))) ja odota
+, jos <(vastaus) = ((numero 1) * (numero 2))> sitten
+ sanoa [kyllä! :)] (2) sekunnille
+ muuta
+ sanoa [no :(] (2) sekunnille
+ loppuun
```

\--- / tehtävä \---

\--- tehtävä \---

Testaa projekti kahdesti: vastaa yhteen kysymykseen oikein ja toinen väärin.

\--- / tehtävä \---

\--- tehtävä \---

Lisää tämän koodin ympärille `ikuisesti`{: class = "block3control"}, niin että peli kysyy soittimelta paljon kysymyksiä peräkkäin.

\--- vinkkejä \--- \--- vihje \---

Sinun täytyy lisätä `ikuisesti`{: class = "block3control"} lohko ja aseta kaikki koodi paitsi `kun lippu napsautti`{: class = "block3control"} lohkon siihen.

\--- / vihje \--- \--- vihje \--- Tässä on lohko, jota tarvitset:

```blocks3
ikuisesti
loppuun
```

\--- / vihje \--- \--- vihje \--- Tässä on, mitä koodisi näyttää:

```blocks3
kun lippu napsautti

+ ikuisesti
    aseta [numero 1 v] (valitse satunnainen (2) - (12))
    aseta [numero 2 v] (valitse satunnainen (2) - (12))
    kysy (liity 1) (liity [x] (numero 2))) ja odota
    jos <(vastaus) = ((numero 1) * (numero 2))> sitten
        sanoa [kyllä! :)] (2) sekunnin ajan
    muu
        sanoa [no :(] (2) sekunnin
    pään
loppuun
```

\--- / vihje \--- \--- / vihjeitä \---

\--- / tehtävä \---