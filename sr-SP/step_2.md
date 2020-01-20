## Направите питања

Почећете тако што ћете креирати случајна питања на која играч мора да одговори.

\--- задатак \---

Отворите нови Сцратцх пројекат.

**Online:** open a new online Scratch project at [rpf.io/scratch-new](http://rpf.io/scratch-new){:target="_blank"}.

**Оффлине:** отворите нови пројекат у оффлине уређивачу.

Ако желите да преузмете и инсталирате Сцратцх оффлине едитор, можете га пронаћи на [рпф.ио/сцратцхофф](http://rpf.io/scratchoff){: таргет = "_ бланк"}.

\--- /задатак \---

\--- task \---

Add a character sprite and a backdrop for your game. You can choose any you like! Here's an example:

![screenshot](images/brain-setting.png)

\--- /task \---

\--- task \---

Make sure you have your character sprite selected. Create two new variables, called `number 1`{:class="block3variables"} and `number 2`{:class="block3variables"}, to store the numbers for the quiz questions.

![screenshot](images/giga-sprite.png)

![screenshot](images/brain-variables.png)

[[[generic-scratch3-add-variable]]]

\--- /задатак \---

\--- task \---

Add code to your character sprite to set both of the `variables`{:class="block3variables"} to a `random`{:class="block3operators"} number between 2 and 12.

![screenshot](images/giga-sprite.png)

```blocks3
када је заставица кликнула
поставила [број 1 в] на (изабери случајне (2) до (12))
сет [број 2 в] до (изабери случајне (2) до (12))
```

\--- /task \---

\--- task \---

Add code to `ask`{:class="block3sensing"} the player for the answer, and then `say for 2 seconds`{:class="block3looks"} whether the answer was right or wrong:

![screenshot](images/giga-sprite.png)

```blocks3
кад је заставица кликнула
поставила [број 1 в] на (изабери случајне (2) до (12))
сет [број 2 в] до (изабери случајне (2) до (12))

+ питај (придружи се (број 1) (придружите се [к] (број 2))) и сачекајте
+ ако <(одговор) = ((број 1) * (број 2))> затим
+ реците [да! :)] фор (2) сецондс
+ елсе
+ саи [но :(] за (2) секунди
+ крај
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
заувек
крај
```

\--- /hint \---

\--- hint \---

Here is what your code should look like:

```blocks3
када је заставица кликнула

+ заувек
    поставила [број 1 в] на (изабери случајне (2) до (12))
    постави [број 2 в] на (изабери случајне (2) до (12))
    питај (придружи се (број) 1) (придружите се [к] (број 2))) и сачекајте
    ако <(одговор) = ((број 1) * (број 2))> затим
        кажите [да! :)] за (2) секунди
    друго
        кажу [но :(] за (2) секунди
    крај
крај
```

\--- /hint \---

\--- /hints \---

\--- /task \---