## Добавить графику

На данный момент спрайт персонажа просто говорит `да! :)` или `нет :(` к ответам игрока. Добавьте графику, чтобы игрок знал, является ли его ответ правильным или неправильным.

\--- задача \---

Создайте новый спрайт под названием «Результат» и дайте ему костюм «галочка / чек» и «крест».

![Спрайт с клещами и крестовыми костюмами](images/brain-result.png)

\--- / задача \---

\--- задача \---

Измените код спрайта вашего персонажа так, чтобы вместо того, чтобы что-то сказать игроку, он `транслировал`{: class = "block3events"} сообщения "правильно" или "неправильно".

![Спрайт персонажа](images/giga-sprite.png)

```blocks3
если <(ответ) = ((номер 1) * (номер 2))> то

- сказать [да! :)] в течение (2) секунд
+ широковещание (правильное v)
противном случае
- произнесите [nope :(] в течение (2) секунд
+ широковещание (неправильное v)
конец
```

\--- / задача \---

\--- задача \---

Теперь вы можете использовать эти сообщения `показать`{: класс = «block3looks»} «тик» или «крест» костюм. Добавьте следующий код к спрайту Result:

![Результат спрайт](images/result-sprite.png)

```blocks3
    когда я получаю [правильный v]
    переключаю костюм на (отметьте v)
    шоу
    жду (1) секунды
    скрываем

    когда я получаю [неправильный v]
    переключаю костюм на (крест v)
    показываю
    жду (1) секунды
    скрыть

    когда флаг нажал
    скрыть
```

\--- / задача \---

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
определить анимацию
показать
ждать (1) секунды
скрыть
```

\--- /task \---

\--- task \---

Make sure you have removed the `show`{:class="block3looks"} and `hide`{:class="block3looks"} blocks below **both** of the `switch costume`{:class="block3looks"} blocks.

Then add the `animate`{:class="block3myblocks"} block below both of the `switch costume`{:class="block3looks"} blocks. Your code should now look like this:

![Result sprite](images/result-sprite.png)

```blocks3
    когда я получаю [правильный v]
    меняю костюм на (tick v)
    animate :: custom

    когда я получаю [неправильный v]
    меняю костюм на (cross v)
    animate :: custom
```

\--- /task \---

Because of the custom `animate`{:class="block3myblocks"} block, you now only need to make one change to your code if you want to show the 'Result' sprite's costumes a longer or shorter time.

\--- task \---

Change your code so that the 'tick' or 'cross' costumes display for 2 seconds.

\--- / задача \---

\--- task \---

Instead of `showing`{:class="block3looks"} and `hiding`{:class="block3looks"} the 'tick' or 'cross' costumes, you could change your `animate`{:class="block3myblocks"} block so that the costumes fade in.

![Result sprite](images/result-sprite.png)

```blocks3
    определить animate
    установить эффект [ghost v] на (100)
    показать
    повтор (25)
        изменить эффект [ghost v] на (-4)
    end
    hide
```

\--- /task \---

Can you improve the animation of the 'tick' or 'cross' graphics? You could add code to make the costumes fade out as well, or you could use other cool effects:

![screenshot](images/brain-effects.png)