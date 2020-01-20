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
animate
megjelenítése
várakozás (1) másodperc
elrejtés
```

\--- /task \---

\--- task \---

Make sure you have removed the `show`{:class="block3looks"} and `hide`{:class="block3looks"} blocks below **both** of the `switch costume`{:class="block3looks"} blocks.

Then add the `animate`{:class="block3myblocks"} block below both of the `switch costume`{:class="block3looks"} blocks. Your code should now look like this:

![Result sprite](images/result-sprite.png)

```blocks3
    ha [helyes v]
    kapcsolót kapok (jelölje be a v)
    animációt :: custom

    ha [rossz v]
    kapcsolót kapok (kereszt v)
    animáció :: custom
```

\--- /task \---

Because of the custom `animate`{:class="block3myblocks"} block, you now only need to make one change to your code if you want to show the 'Result' sprite's costumes a longer or shorter time.

\--- task \---

Change your code so that the 'tick' or 'cross' costumes display for 2 seconds.

\--- / feladat \---

\--- task \---

Instead of `showing`{:class="block3looks"} and `hiding`{:class="block3looks"} the 'tick' or 'cross' costumes, you could change your `animate`{:class="block3myblocks"} block so that the costumes fade in.

![Result sprite](images/result-sprite.png)

```blocks3
    animate
    set [ghost v] hatás definiálása (100)
    show
    ismétlés (25)
        [ghost v] hatás módosítása (-4)
    vég
    elrejtés
```

\--- /task \---

Can you improve the animation of the 'tick' or 'cross' graphics? You could add code to make the costumes fade out as well, or you could use other cool effects:

![screenshot](images/brain-effects.png)