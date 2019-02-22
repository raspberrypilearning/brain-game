## Lisää ajastin

\--- tehtävä \--- Luo ajastin lavalla avulla uuden muuttujan nimeltään `kerran`{: class = "block3variables"}. Ajastimen pitäisi alkaa 30 sekunnista ja laskea 0 sekuntia.

![Vaihe sprite](images/stage-sprite.png)

\--- vinkkejä \--- \--- vihje \---

Luo `muuttuja`{: class = "block3variables"}, soita se "aika" ja aseta sen arvo `30`.

Lisää sitten koodi laskeaksesi `aikaa`{: class = "block3variables"} alas 0: een 30 sekunnin kuluessa. Voit tehdä tämän vähentämällä `1` `kertaa`{: class = "block3variables"} joka `1` sekunnin välein ja toista tämä kunnes `kertaa`{: class = "block3variables"} vastaa `0`.

\--- / vihje \--- \--- vihje \--- Tässä ovat lohkot, joita tarvitset:

```blocks3
toista, kunnes < >

loppuun

odota (1) sekuntia

muutos [aika v] (1)

(aika)

kun lippu napsautti

<() = ()>

set [aika v] - [0]
```

\--- / vihje \--- \--- vihje \--- Tässä on se, mitä uusi koodi näyttää:

```blocks3
kun lippu napsautti
asetusta [aika v] [30]
toistoa, kunnes <(aika) = (0)>
    odota (1) sekuntia
    muutos [aika v] (-1)
loppuun
```

\--- / vihje \--- \--- / vihjeitä \---

\--- / tehtävä \---

\--- tehtävä \---

Luo `lähetys`{: class = "block3control"}, joka lähettää viestin 'loppuun'. `lähetys`{: class = "block3control"} on kuin ilmoitus kaiuttimen yli: se voidaan kuunnella kaikilla spriteilläsi. Lisää `lähetyksen`{: class = "block3control"} lohko ajastinkoodin loppuun siten, että koodi lähettää ja 'lopettaa' viestin, kun `kertaa`{: class = "block3variables"} on laskenut `0`.

![Vaihe sprite](images/stage-sprite.png)

```blocks3
    lähetys (loppu v)
```

\--- / tehtävä \---

\--- tehtävä \--- Valitse hahmosi sprite ja lisää koodi niin, että sprite `pysäyttää muut skriptit`{: class = "block3control"}, kun se vastaanottaa `loppu`{: class = "block3control"} -viestin .

![Giga sprite](images/giga-sprite.png)

```blocks3
    kun saan [loppu v]
    stop [muut skriptit sprite v]
```

\--- / tehtävä \---

\--- tehtävä \---

Testaa peliä uudelleen. Sen pitäisi jatkaa kysymysten esittämistä, kunnes ajastin on laskenut 0: een.

\--- / tehtävä \---