## Adăugați grafică

În momentul de față, personajul sprite spune doar `da! :)` sau `nu :(` la răspunsurile jucătorului. Adăugați unele grafice pentru a lăsa jucătorul să știe dacă răspunsul lor este corect sau incorect.

\--- proba\---

Creați un nou sprite numit "Rezultat" și dați-i un costum "bifați / verificați" și "încrucișați".

![Sprite cu bici și costume încrucișate](images/brain-result.png)

\--- /task \---

\--- task \---

Schimbați codul sprite al caracterului, astfel încât, în loc să spună ceva jucătorului, acesta `transmite`{: class = "block3events"} mesajele "corecte" sau "greșite".

![Sprite de caractere](images/giga-sprite.png)

```blocks3
dacă <(răspuns) = ((numărul 1) * (numărul 2))> atunci

- spuneți [da! :)] pentru (2) secunde
+ broadcast (v corect)
altceva
- spun [nope :(] pentru (2) secunde
+ broadcast (v greșit)
capăt
```

\--- /task \---

\--- task \---

Acum puteți utiliza aceste mesaje de la `show -`{: class = „block3looks“} „capusa“ sau costum „cruce“. Adăugați următorul cod la sprite "Rezultat":

![Sprite rezultat](images/result-sprite.png)

```blocks3
    atunci când primesc [v corect]
    costum comutator la (căpușe v)
    arată
    wait (1) secunde
    ascunde

    atunci când primesc [v greșit]
    costum comutator la (cruce v)
    arată
    așteptați (1) secunde
    ascunde

    când steagul a făcut clic pe
    ascunde
```

\--- /task \---

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
defini animat
arată
așteptați (1) secunde
ascunde
```

\--- /task \---

\--- task \---

Make sure you have removed the `show`{:class="block3looks"} and `hide`{:class="block3looks"} blocks below **both** of the `switch costume`{:class="block3looks"} blocks.

Then add the `animate`{:class="block3myblocks"} block below both of the `switch costume`{:class="block3looks"} blocks. Your code should now look like this:

![Result sprite](images/result-sprite.png)

```blocks3
    când primesc costumul de schimb [corect v]
    comuta la (bifați v)
    animați :: personalizat

    când primesc [greșit v]
    costum de comutare la (cruce v)
    animate :: personalizat
```

\--- /task \---

Because of the custom `animate`{:class="block3myblocks"} block, you now only need to make one change to your code if you want to show the 'Result' sprite's costumes a longer or shorter time.

\--- task \---

Change your code so that the 'tick' or 'cross' costumes display for 2 seconds.

\--- /task \---

\--- task \---

Instead of `showing`{:class="block3looks"} and `hiding`{:class="block3looks"} the 'tick' or 'cross' costumes, you could change your `animate`{:class="block3myblocks"} block so that the costumes fade in.

![Result sprite](images/result-sprite.png)

```blocks3
    defineste animat
    set [ghost v] efect la (100)
    arata
    repeta (25)
        schimba [ghost v] efect prin (-4)
    end
    ascunde
```

\--- /task \---

Can you improve the animation of the 'tick' or 'cross' graphics? You could add code to make the costumes fade out as well, or you could use other cool effects:

![screenshot](images/brain-effects.png)