## Creu cwestiynau

Fe wnawn ni ddechrau trwy greu cwestiynau ar hap i’r chwareuwr ateb.

\--- task \---

Agora prosiect Scratch newydd.

**Online:** open a new online Scratch project at [rpf.io/scratch-new](http://rpf.io/scratch-new){:target="_blank"}.

**All-lein** agora brosiect newydd yn y golygydd all-lein.

Os oes angen i ti lawrlwytho a gosod golygydd Scratch all-lein, mae modd dod o hyd iddo yma [rpf.io/scratchoff](http://rpf.io/scratchoff){:target="_blank"}.

\--- /task \---

\--- task \---

Add a character sprite and a backdrop for your game. You can choose any you like! Here's an example:

![screenshot](images/brain-setting.png)

\--- /task \---

\--- task \---

Make sure you have your character sprite selected. Create two new variables, called `number 1`{:class="block3variables"} and `number 2`{:class="block3variables"}, to store the numbers for the quiz questions.

![screenshot](images/giga-sprite.png)

![screenshot](images/brain-variables.png)

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- task \---

Add code to your character sprite to set both of the `variables`{:class="block3variables"} to a `random`{:class="block3operators"} number between 2 and 12.

![screenshot](images/giga-sprite.png)

```blocks3
pan fo'r flag werdd yn cael ei glicio
gosod [rhif 1 v] i (dewis ar hap (2) i (12))
gosod [rhif 2 v] i (dewis ar hap (2) i (12))
```

\--- /task \---

\--- task \---

Add code to `ask`{:class="block3sensing"} the player for the answer, and then `say for 2 seconds`{:class="block3looks"} whether the answer was right or wrong:

![screenshot](images/giga-sprite.png)

```blocks3
pan fo'r flag werdd yn cael ei glicio
gosod [rhif 1 v] i (dewis ar hap (2) i (12))
gosod [rhif 2 v] i (dewis ar hap (2) i (12))

+ gofyn (uno (rhif 1) (uno [ x ] (rhif 2))) ac aros
+ os <(ateb) = ((rhif 1) * (rhif 2))> yna 
+ dweud [Ie! :)] am (2) eiliad
+ fel arall 
+ dweud [Na :(] am (2) eiliad
+ end
```

\--- /task \---

\--- task \---

Test your project twice: answer one question correctly, and the other incorrectly.

\--- /task \---

\--- task \---

Add a `forever`{:class="block3control"} loop around this code, so that the game asks the player lots of questions in a row.

\--- hints \---

\--- hint \---

You need to add a `forever`{:class="block3control"} block, and put all of the code except the `when flag clicked`{:class="block3control"} block into it.

\--- /hint \---

\--- hint \---

Here is the block you need:

```blocks3
am byth
end
```

\--- /hint \---

\--- hint \---

Here is what your code should look like:

```blocks3
+ pan fo'r flag werdd yn cael ei glicio

am byth 
  gosod [rhif 1 v] i (dewis ar hap (2) i (12))
  gosod [rhif 2 v] i (dewis ar hap (2) i (12))
  gofyn (uno (rhif 1) (uno [ x ] (rhif 2))) ac aros
  os <(ateb) = ((rhif 1) * (rhif 2))> yna 
    dweud [Ie! :)] am (2) eiliad
  fel arall 
    dweud [Na :(] am (2) eiliad
  end
end
```

\--- /hint \---

\--- /hints \---

\--- /task \---