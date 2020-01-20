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

\--- task \---

Test your game again. You should see the tick whenever you answer a question correctly, and the cross whenever you answer incorrectly!

![Tick for correct, cross for wrong answer](images/brain-test-answer.png)

\--- /task \---

Can you see that the code for `when I receive correct`{:class="block3events"} and `when I receive wrong`{:class="block3events"} is nearly identical?

So you can change your code more easily, you are going to create a custom block.

\--- task \---

Select the 'Result' sprite. Then click on `My Blocks`{:class="block3myblocks"}, and then on **Make a Block**. Create a new block and call it `animate`{:class="block3myblocks"}.

![Result sprite](images/result-sprite.png)

![Create a block called animate](images/brain-animate-function.png)

\--- /task \---

\--- task \---

Move the code to `show`{:class="block3looks"} and `hide`{:class="block3looks"} the 'Result' sprite into the `animate`{:class="block3myblocks"} block:

![Result sprite](images/result-sprite.png)

```blocks3
määritellä animate
Näytä
odota (1) sekuntia
piilota
```

\--- /task \---

\--- task \---

Make sure you have removed the `show`{:class="block3looks"} and `hide`{:class="block3looks"} blocks below **both** of the `switch costume`{:class="block3looks"} blocks.

Then add the `animate`{:class="block3myblocks"} block below both of the `switch costume`{:class="block3looks"} blocks. Your code should now look like this:

![Result sprite](images/result-sprite.png)

```blocks3
    kun saan [oikea v]
    -kytkimen puku (rasti v)
    animoi :: custom

    kun saan [väärin v]
    kytkinpukua (ristiin)
    animate :: custom
```

\--- /task \---

Because of the custom `animate`{:class="block3myblocks"} block, you now only need to make one change to your code if you want to show the 'Result' sprite's costumes a longer or shorter time.

\--- task \---

Change your code so that the 'tick' or 'cross' costumes display for 2 seconds.

\--- / tehtävä \---

\--- task \---

Instead of `showing`{:class="block3looks"} and `hiding`{:class="block3looks"} the 'tick' or 'cross' costumes, you could change your `animate`{:class="block3myblocks"} block so that the costumes fade in.

![Result sprite](images/result-sprite.png)

```blocks3
    määritä animaatio
    sarja [ghost v] -toiminto (100)
    näytä
    toistoa (25)
        muutos [ghost v] vaikutus (-4)
    loppuun
    piilota
```

\--- /task \---

Can you improve the animation of the 'tick' or 'cross' graphics? You could add code to make the costumes fade out as well, or you could use other cool effects:

![screenshot](images/brain-effects.png)