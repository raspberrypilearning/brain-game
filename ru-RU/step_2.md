## Создай вопросы

Ты начнешь с создания случайных вопросов, на которые игрок должен ответить.

\--- task \---

Открой новый проект Скретч.

**Online:** open a new online Scratch project at [rpf.io/scratch-new](http://rpf.io/scratch-new){:target="_blank"}.

**Офлайн:** открой новый проект в автономном редакторе.

Если тебе нужно скачать и установить оффлайн редактор Scratch, ты можешь найти его по адресу [rpf.io/scratchoff](http://rpf.io/scratchoff)\--- /task"}.

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
когда щёлкнут по зелёному флагу
задать [число 1 v] значение (выдать случайное от (2) до (12))
задать [число 2 v] значение (выдать случайное от (2) до (12))
```

\--- /task \---

\--- task \---

Add code to `ask`{:class="block3sensing"} the player for the answer, and then `say for 2 seconds`{:class="block3looks"} whether the answer was right or wrong:

![screenshot](images/giga-sprite.png)

```blocks3
когда щёлкнут по зелёному флагу
задать [число 1 v] значение (выдать случайное от (2) до (12))
задать [число 2 v] значение (выдать случайное от (2) до (12))

+ спросить (объединить (число 1) (объединить [ x ] (число 2))) и ждать
+ если <(ответ) = ((число 1) * (число 2))>, то 
+ говорить [да! :)] (2) секунд
+ иначе 
+ говорить [нет :(] (2) секунд
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
повторять всегда
конец
```

\--- /hint \---

\--- hint \---

Here is what your code should look like:

```blocks3
когда щёлкнут по зелёному флагу

+ повторять всегда 
  задать [число 1 v] значение (выдать случайное от (2) до (12))
  задать [число 2 v] значение (выдать случайное от (2) до (12))
  спросить (объединить (число 1) (объединить [ x ] (число 2))) и ждать
  если <(ответ) = ((число 1) * (число 2))>, то 
    сказать [да! :)] (2) секунд
  иначе 
    говорить [no :(] (2) секунд
  конец
конец
```

\--- /hint \---

\--- /hints \---

\--- /task \---