## Адд грапхицс

У овом тренутку, лик сприте само каже `да! :)` или `не :(` до одговора играча. Додајте неке графике како би играч знао да ли је њихов одговор тачан или нетачан.

\--- задатак \---

Направите нови сприте назван 'Ресулт', и дајте му 'тицк / цхецк' и 'цросс' костим.

![Сприте са костимима са крпељима и крстовима](images/brain-result.png)

\--- /задатак \---

\--- задатак \---

Промена кода ваш карактер Сприте тако да, уместо да кажете нешто на плејера, `емитује`{: цласс = "блоцк3евентс"} поруке "исправан" или "погрешан".

![Цхарацтер сприте](images/giga-sprite.png)

```blocks3
ако је <(одговор) = ((број 1) * (број 2))> затим

- реци [да! :)] фор (2) сецондс
+ броадцаст (ригхт в)
елсе
- саи [нопе :(] фор (2) сецондс
+ броадцаст (вронг в)
енд
```

\--- /задатак \---

\--- задатак \---

Сада можете користити ове поруке у `схов`{: цласс = "блоцк3лоокс"} костим 'квачица' или 'крст'. Додајте следећи код у 'Резултат':

![Резултат сприте](images/result-sprite.png)

```blocks3
    када примим [исправити в]
    пребацити костим на (откуцати в)
    показати
    чекати (1) секунди
    сакрити

    када примим [погрешно в]
    пребацити костим на (цросс в)
    показати
    чекати (1) секунде
    сакриј

    када је заставица кликнула
    сакриј
```

\--- /задатак \---

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
дефине анимате
схов
ваит (1) сецондс
хиде
```

\--- /task \---

\--- task \---

Make sure you have removed the `show`{:class="block3looks"} and `hide`{:class="block3looks"} blocks below **both** of the `switch costume`{:class="block3looks"} blocks.

Then add the `animate`{:class="block3myblocks"} block below both of the `switch costume`{:class="block3looks"} blocks. Your code should now look like this:

![Result sprite](images/result-sprite.png)

```blocks3
    када примим [исправан в]
    пребаците костим на (откуцајте в)
    анимате :: цустом

    када примим [погрешно в]
    пребаците костим на (цросс в)
    анимате :: цустом
```

\--- /task \---

Because of the custom `animate`{:class="block3myblocks"} block, you now only need to make one change to your code if you want to show the 'Result' sprite's costumes a longer or shorter time.

\--- task \---

Change your code so that the 'tick' or 'cross' costumes display for 2 seconds.

\--- /задатак \---

\--- task \---

Instead of `showing`{:class="block3looks"} and `hiding`{:class="block3looks"} the 'tick' or 'cross' costumes, you could change your `animate`{:class="block3myblocks"} block so that the costumes fade in.

![Result sprite](images/result-sprite.png)

```blocks3
    дефинирајте анимате
    сет [гхост в] ефект на (100)
    прикажи
    понављање (25)
        промени [гхост в] ефекат (-4)
    крај
    сакриј
```

\--- /task \---

Can you improve the animation of the 'tick' or 'cross' graphics? You could add code to make the costumes fade out as well, or you could use other cool effects:

![screenshot](images/brain-effects.png)