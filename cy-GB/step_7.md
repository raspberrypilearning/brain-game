## Ychwanegu graffeg

Yn lle bod dy gymeriad ond yn dweud `ie! :)` neu `na :(`, beth am ychwanegu peth graffeg fel bod y chwareuwr yn gwybod os yw'r ateb yn gywir neu anghywir.

\--- task \---

Bydd angen creu corlun newydd o’r enw ‘Canlyniad’, yn cynnwys gwisg ‘tic’ a ‘chroes’.

![Corlun tic a chroes](images/brain-result.png)

\--- /task \---

\--- task \---

Newida côd dy gymeriad, fel ei fod yn `darlledu`{:class="block3events"} negeseuon 'cywir' ac 'anghywir'.

![Corlun cymeriad](images/giga-sprite.png)

```blocks3
os <(ateb) = ((rhif 1) * (rhif 2))> yna 
-  dweud [Ie! :)] am (2) eiliad
+ darlledu (correct v)
fel arall 
-  dweud [Na :(] am (2) eiliad
+ darlledu (wrong v)
end
```

\--- /task \---

\--- task \---

Fe alli di nawr ddefnyddio’r negeseuon yma i `ddangos`{:class="block3looks"} y wisg ‘tic’ neu ‘groes’. Ychwanega’r côd yma i dy gorlun ‘Canlyniad’:

![Corlun canlyniad](images/result-sprite.png)

```blocks3
    pan rwy'n derbyn [correct v]
newid gwisg i (tick v)
dangos
aros (1) eiliad
cuddio

pan rwy'n derbyn [wrong v]
newid gwisg i (cross v)
dangos
aros (1) eiliad
cuddio

pan fo'r flag werdd yn cael ei glicio
cuddio
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
diffinio animeiddio
dangos
aros (1) eiliad
cuddio
```

\--- /task \---

\--- task \---

Make sure you have removed the `show`{:class="block3looks"} and `hide`{:class="block3looks"} blocks below **both** of the `switch costume`{:class="block3looks"} blocks.

Then add the `animate`{:class="block3myblocks"} block below both of the `switch costume`{:class="block3looks"} blocks. Your code should now look like this:

![Result sprite](images/result-sprite.png)

```blocks3
    pan rwy'n derbyn [correct v]
newid gwisg i (tick v)
animeiddio :: custom

pan rwy'n derbyn [wrong v]
newid gwisg i (cross v)
animeiddio :: custom
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
    diffinio animeiddio
gosod effaith [ghost v] effaith i (100)
dangos
ailadrodd (25) 
  newid effaith [ghost v] gan (-4)
end
cuddio
```

\--- /task \---

Can you improve the animation of the 'tick' or 'cross' graphics? You could add code to make the costumes fade out as well, or you could use other cool effects:

![screenshot](images/brain-effects.png)