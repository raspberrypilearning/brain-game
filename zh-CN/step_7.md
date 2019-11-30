## 添加图形

此刻，角色精灵只根据玩家的答案说`对！ :) `或`不对:( `。添加一些图形，让玩家知道他们的答案是正确还是错误。

\--- task \---

创建一个名为“结果”的新精灵，并为其赋予“对勾/检查”和“叉”的外观。

![带有对勾和叉号的精灵。](images/brain-result.png)

\--- /task \---

\--- task \---

更改角色精灵的代码，使它`不再向玩家说些什么，而是广播` {：class =“ block3events”}“正确”或“错误”的消息。

![角色精灵](images/giga-sprite.png)

```blocks3
如果 <(回答) = ((数字1)*(数字2))> 那么

- 说 [对! :)] (2) 秒
+ 广播 (正确 v)
else
- 说 [不对 :(] (2) 秒
+ 广播 (错误 v)
end
```

\--- /task \---

\--- task \---

现在，您可以用这些消息来`显示` {：class =“ block3looks”}”对勾“或”叉“。将以下代码添加到“结果”精灵中：

![结果精灵](images/result-sprite.png)

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

![对勾表示正确，叉号表示错误](images/brain-test-answer.png)

\--- /task \---

你注意到`when I receive correct`{:class="block3events"}和`when I receive wrong`{:class="block3events"}的代码几乎相同吗？

所以你可以更容易地更改你的代码，你可以创建一个自定义块。

\--- task \---

选择“结果”精灵。 然后点击`My Blocks` {:class =“ block3myblocks”}，接着**Make a Block** 。 创建一个新块并将其命名为`animate` {:class="block3myblocks"}。

![结果精灵](images/result-sprite.png)

![创建一个名为动画的块](images/brain-animate-function.png)

\--- /task \---

\--- task \--- 将`show`{:class="block3looks"}与`hide`{:class="block3looks"}“结果”精灵的代码块移到`animate`{:class="block3myblocks"}模块中。

![结果精灵](images/result-sprite.png)

```blocks3
define animate
show
wait (1) seconds
hide
```

\--- /task \---

确保在**两个** `switch costume`{:class="block3looks"}块下面移除了`show`{:class="block3looks"}和`hide`{:class="block3looks"}模块。

然后在两个`switch costume`{:class="block3looks"}块下面添加` animate`{:class="block3myblocks"}块。你的代码现在应如下所示：

![结果精灵](images/result-sprite.png)

```blocks3
    when I receive [correct v]
    switch costume to (tick v)
    animate:: custom

    when I receive [wrong v]
    switch costume to (cross v)
    animate:: custom
```

\--- /task \---

由于 `animate`{:class="block3myblocks"} 块是自定义的， 如果你想要“结果”显示的时间更长或更短，现在只需要对你的代码做简单修改，。

\--- task \---

更改您的代码，以使“ 对勾”或“叉号”显示2秒钟。

\--- /task \---

\--- task \--- 你可以修改你的` animate`代码，是的“对勾”与“叉号”淡入淡出，而不是使用`showing`{:class="block3looks"}或`hiding`{:class="block3looks"} 。

![结果精灵](images/result-sprite.png)

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

您能改进“tick”或“cross”图形动画吗？ 您可以添加代码使图形淡出。或者您可以使用其他酷炫效果：

![截屏](images/brain-effects.png)