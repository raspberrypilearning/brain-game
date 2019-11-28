## 添加图形

此刻，角色精灵只根据玩家的答案说`是！ :) `或`否:( `。添加一些图形，让玩家知道他们的答案是正确还是错误。

\--- task \---

创建一个名为“结果”的新精灵，并为其赋予“对勾/检查”和“叉”的外观。

![Sprite with tick and cross costumes](images/brain-result.png)

\--- /task \---

\--- task \---

更改角色精灵的代码，使它`不再向玩家说些什么，而是广播` {：class =“ block3events”}“正确”或“错误”的消息。

![Character sprite](images/giga-sprite.png)

```blocks3
if <(answer) = ((number 1)*(number 2))> then

- say [yes! :)] for (2) seconds
+ broadcast (correct v)
else
- say [nope :(] for (2) seconds
+ broadcast (wrong v)
end
```

\--- /task \---

\--- task \---

现在，您可以用这些消息来`显示` {：class =“ block3looks”}”对勾“或”叉“。将以下代码添加到“结果”精灵中：

![Result sprite](images/result-sprite.png)

```blocks3
    when I receive [correct v]
    switch costume to (tick v)
    show
    wait (1) seconds
    hide

    when I receive [wrong v]
    switch costume to (cross v)
    show
    wait (1) seconds
    hide

    when flag clicked
    hide
```

\--- /task \---

\---任务\--- 再次测试您的游戏。每当您正确回答问题时，您都应该看到对勾；而当您回答错误时，您将看到叉号！

![Tick for correct, cross for wrong answer](images/brain-test-answer.png)

\--- /task \---

你注意到`when I receive correct`{:class="block3events"}和`when I receive wrong`{:class="block3events"}的代码几乎相同吗？

所以你可以更容易地更改你的代码，你可以创建一个自定义块。

\--- task \---

选择“结果”精灵。 然后点击`My Blocks` {:class =“ block3myblocks”}，接着**Make a Block** 。 创建一个新块并将其命名为`animate` {:class="block3myblocks"}。

![Result sprite](images/result-sprite.png)

![Create a block called animate](images/brain-animate-function.png)

\--- /task \---

\--- task \--- 将`show`{:class="block3looks"}与`hide`{:class="block3looks"}“结果”精灵的代码块移到`animate`{:class="block3myblocks"}模块中。

![Result sprite](images/result-sprite.png)

```blocks3
define animate
show
wait (1) seconds
hide
```

\--- /task \---

\--- task \--- Make sure you have removed the `show`{:class="block3looks"} and `hide`{:class="block3looks"} blocks below **both** of the `switch costume`{:class="block3looks"} blocks.

Then add the `animate`{:class="block3myblocks"} block below both of the `switch costume`{:class="block3looks"} blocks. Your code should now look like this:

![Result sprite](images/result-sprite.png)

```blocks3
    when I receive [correct v]
    switch costume to (tick v)
    animate:: custom

    when I receive [wrong v]
    switch costume to (cross v)
    animate:: custom
```

\--- /task \---

Because of the custom `animate`{:class="block3myblocks"} block, you now only need to make one change to your code if you want to show the 'Result' sprite's costumes a longer or shorter time.

\--- task \---

Change your code so that the 'tick' or 'cross' costumes display for 2 seconds.

\--- /task \---

\--- task \--- Instead of `showing`{:class="block3looks"} and `hiding`{:class="block3looks"} the 'tick' or 'cross' costumes, you could change your `animate`{:class="block3myblocks"} block so that the costumes fade in.

![Result sprite](images/result-sprite.png)

```blocks3
    define animate
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