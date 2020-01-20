## Lägg till grafik

För tillfället säger teckenspiralen bara `ja! :)` eller `nej :(` till spelarens svar. Lägg till lite grafik för att låta spelaren veta om deras svar är korrekt eller felaktigt.

\--- uppgift \---

Skapa en ny sprite som heter "Resultat", och ge den en "tick / check" och en "cross" -dräkt.

![Sprite med kryss och korskostymer](images/brain-result.png)

\--- / uppgift \---

\--- uppgift \---

Ändra din bokstavs kod så att istället för att säga något till spelaren sänder ``{: class = "block3events"} meddelandena "korrekta" eller "fel".

![Karaktärsprite](images/giga-sprite.png)

```blocks3
om <(svar) = ((nummer 1) * (nummer 2))> då

- säg [ja! :)] för (2) sekunder
+ sändning (korrekt v)
annat
- säg [nope :(] för (2) sekunder
+ sändning (fel v)
slutet
```

\--- / uppgift \---

\--- uppgift \---

Nu kan du använda dessa meddelanden till `visa`{: class = "block3looks"} "tick" eller "cross" kostym. Lägg till följande kod till "Resultat" sprite:

![Resultat sprite](images/result-sprite.png)

```blocks3
    när jag tar emot [korrekt v]
    byt kostym till (kryssa v)
    visa
    vänta (1) sekunder
    dölja

    när jag tar emot [fel v]
    byta kostym till (korsa v)
    visa
    vänta (1) sekunder
    göm

    när flaggan klickade
    gömma
```

\--- / uppgift \---

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
definiera animera
visa
vänta (1) sekunder
gömma
```

\--- /task \---

\--- task \---

Make sure you have removed the `show`{:class="block3looks"} and `hide`{:class="block3looks"} blocks below **both** of the `switch costume`{:class="block3looks"} blocks.

Then add the `animate`{:class="block3myblocks"} block below both of the `switch costume`{:class="block3looks"} blocks. Your code should now look like this:

![Result sprite](images/result-sprite.png)

```blocks3
    när jag tar emot [korrekt v]
    byta kostym till (tick v)
    animera :: anpassad

    när jag tar emot [fel v]
    byta kostym till (cross v)
    animera :: anpassade
```

\--- /task \---

Because of the custom `animate`{:class="block3myblocks"} block, you now only need to make one change to your code if you want to show the 'Result' sprite's costumes a longer or shorter time.

\--- task \---

Change your code so that the 'tick' or 'cross' costumes display for 2 seconds.

\--- / uppgift \---

\--- task \---

Instead of `showing`{:class="block3looks"} and `hiding`{:class="block3looks"} the 'tick' or 'cross' costumes, you could change your `animate`{:class="block3myblocks"} block so that the costumes fade in.

![Result sprite](images/result-sprite.png)

```blocks3
    definiera animera
    set [ghost v] effekt till (100)
    visa
    upprepa (25)
        ändra [spöke v] effekt av (-4)

    göm
```

\--- /task \---

Can you improve the animation of the 'tick' or 'cross' graphics? You could add code to make the costumes fade out as well, or you could use other cool effects:

![screenshot](images/brain-effects.png)