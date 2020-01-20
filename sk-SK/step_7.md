## Pridajte grafiku

V súčasnej dobe postava sprite hovorí `áno! :)` alebo `no :(` odpovede hráča. Pridajte nejakú grafiku a nechajte prehrávač vedieť, či je jeho odpoveď správna alebo nesprávna.

\--- úloha \---

Vytvorte nový skript nazývaný "Výsledok" a zverte ho "krížikom" a "krížovým" kostýmom.

![Sprite s kliešťami a krížovými kostýmami](images/brain-result.png)

\--- / úloha \---

\--- úloha \---

Zmeňte kód vášho znakového sprite tak, že namiesto toho, aby niečo povedal hráčovi, `vysiela`{: class = "block3events"} správy "správne" alebo "zlé".

![Sprite znakov](images/giga-sprite.png)

```blocks3
ak <(odpoveď) = ((číslo 1) * (číslo 2))> potom

- povedzte [yes! :)] pre (2) sekúnd,
+ vysielanie (správny objem)
iný
- povedzme [Nie :(] pre (2) sekúnd,
+ vysielanie (zle v)
koniec
```

\--- / úloha \---

\--- úloha \---

Teraz môžete použiť tieto správy na `zobraziť`{: class = "block3looks"} "kliešť" alebo "cross" kostým. Pridajte nasledujúci kód do výsledku Sprite:

![Výsledok sprite](images/result-sprite.png)

```blocks3
    keď dostanem [správne v]
    prepínač kostým na (začiarknite v)
    zobraziť
    čakať (1) sekundy
    skryť

    keď dostanem [nesprávne v]
    kostým prepnúť na (kríž v)
    zobraziť
    čakať (1) sekúnd
    skryť

    keď sa vlajka klikne
    skryť
```

\--- / úloha \---

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
definovať animovať
zobraziť
čakať (1) sekundy
skryť
```

\--- /task \---

\--- task \---

Make sure you have removed the `show`{:class="block3looks"} and `hide`{:class="block3looks"} blocks below **both** of the `switch costume`{:class="block3looks"} blocks.

Then add the `animate`{:class="block3myblocks"} block below both of the `switch costume`{:class="block3looks"} blocks. Your code should now look like this:

![Result sprite](images/result-sprite.png)

```blocks3
    keď dostanem [správne v]
    kostým prepnúť na (zaškrtnite v)
    animate :: vlastné

    keď dostanem [nesprávne v]
    prepnúť kostým na (kríž v)
    animate :: vlastné
```

\--- /task \---

Because of the custom `animate`{:class="block3myblocks"} block, you now only need to make one change to your code if you want to show the 'Result' sprite's costumes a longer or shorter time.

\--- task \---

Change your code so that the 'tick' or 'cross' costumes display for 2 seconds.

\--- / úloha \---

\--- task \---

Instead of `showing`{:class="block3looks"} and `hiding`{:class="block3looks"} the 'tick' or 'cross' costumes, you could change your `animate`{:class="block3myblocks"} block so that the costumes fade in.

![Result sprite](images/result-sprite.png)

```blocks3
    definovať animovať
    nastaviť [ghost v] efekt na (100)
    zobraziť
    opakovať (25)
        zmeniť [ghost v] efekt podľa (-4)
    koniec
    skryť
```

\--- /task \---

Can you improve the animation of the 'tick' or 'cross' graphics? You could add code to make the costumes fade out as well, or you could use other cool effects:

![screenshot](images/brain-effects.png)