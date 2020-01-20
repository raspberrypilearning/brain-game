## Afegeix gràfics

De moment, el sprite del personatge només diu `sí! :)` o `no :(` a les respostes del jugador. Afegiu alguns gràfics per permetre al jugador saber si la seva resposta és correcta o incorrecta.

\--- tasca \---

Creeu un nou sprite anomenat 'Resultat', i doneu-li un 'tick / check' i un vestit 'cross'.

![Sprite amb disfresses i taques](images/brain-result.png)

\--- / tasca \---

\--- tasca \---

Canvieu el codi del vostre personatge Sprite perquè, en lloc de dir alguna cosa al jugador, `emet`{: class = "block3events"} els missatges "correctes" o "incorrectes".

![Sprite de caràcters](images/giga-sprite.png)

```blocks3
si <(resposta) = ((número 1) * (número 2))> després

- digueu [sí! :)] per a (2) segons
+ emissió (correcte v)
més
- digue [nope :(] per (2) segons
+ emissió (v incorrecta)
final
```

\--- / tasca \---

\--- tasca \---

Ara podeu utilitzar aquests missatges a `mostrar`{: class = "block3looks"} la marca "tick" o "cross". Afegiu el següent codi al sprite "Resultat":

![Sprite de resultats](images/result-sprite.png)

```blocks3
    quan rebo [v correcte]
    canvia de disfressa a (tick v)
    mostra
    espera (1) segons
    ocultar

    quan rebo [v incorrecta]
    canviar de disfressa a (creu v)
    mostra
    espera (1) segons
    amaga

    quan es fa clic a la bandera
    esculpeu
```

\--- / tasca \---

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
define animate
show
wait (1) seconds
hide
```

\--- /task \---

\--- task \---

Make sure you have removed the `show`{:class="block3looks"} and `hide`{:class="block3looks"} blocks below **both** of the `switch costume`{:class="block3looks"} blocks.

Then add the `animate`{:class="block3myblocks"} block below both of the `switch costume`{:class="block3looks"} blocks. Your code should now look like this:

![Result sprite](images/result-sprite.png)

```blocks3
    quan rebo [v correcte]
    canvia de disfressa a (tick v)
    animi :: custom

    quan rebo [v incorrecta]
    switch suit to (cross v)
    animate :: custom
```

\--- /task \---

Because of the custom `animate`{:class="block3myblocks"} block, you now only need to make one change to your code if you want to show the 'Result' sprite's costumes a longer or shorter time.

\--- task \---

Change your code so that the 'tick' or 'cross' costumes display for 2 seconds.

\--- / tasca \---

\--- task \---

Instead of `showing`{:class="block3looks"} and `hiding`{:class="block3looks"} the 'tick' or 'cross' costumes, you could change your `animate`{:class="block3myblocks"} block so that the costumes fade in.

![Result sprite](images/result-sprite.png)

```blocks3
    defineix animate
    set [ghost v] effect to (100)
    show
    repeat (25)
        change [ghost v] effect by (-4)
    end
    hide
```

\--- /task \---

Can you improve the animation of the 'tick' or 'cross' graphics? You could add code to make the costumes fade out as well, or you could use other cool effects:

![screenshot](images/brain-effects.png)