## 多次游戏

现在，您将添加一个“开始”按钮，以便玩家可以玩多次游戏。

\--- 任务 \--- 创建一个新的“开始”按钮，让玩家点击来开始新游戏。

您可以自己绘制精灵，也可以从库中编辑精灵。

![Picture of the play button](images/brain-play.png)

\--- /任务 \---

\--- 任务 \--- 将此代码添加到按钮精灵中：

![Button sprite](images/button-sprite.png)

```blocks3
    当旗子被点击
    显示

    当角色被点击
    隐藏
    广播(start v)        
```

\--- /任务 \---

新代码包括另一个`广播` {class =“block3events”}块，它发送消息'start'。

当玩家点击旗帜时，新代码会显示“开始”按钮精灵。 当玩家点击按钮精灵时，精灵会隐藏，然后广播信息，让其他精灵可以做出反应。

此时，角色精灵在玩家点击旗帜时开始提问。 更改游戏代码，以便当它收到“start”`广播`{:class="block3events"}时，字符精灵开始提问。

\--- task \--- 选择你的角色精灵，并在其代码部分中，用`when I receive start`{:class="block3events"}代码块替换`when flag clicked`{:class="block3events"}代码块。

![Character sprite](images/giga-sprite.png)

```blocks3
<br />- when flag clicked
+ when I receive [start v]
set [number 1 v] to (pick random (2) to (12))
set [number 2 v] to (pick random (2) to (12))
ask (join (number 1)(join [ x ] (number 2))) and wait
if <(answer) = ((number 1)*(number 2))> then
    say [yes! :)] for (2) seconds
else
    say [nope :(] for (2) seconds
end
```

\--- /task \---

\--- task \---

点击绿色旗帜，然后单击新的“Play”按钮以测试其是否正常工作。你应该看到在点击按钮之前游戏不会开始。

\--- /task \---

你能看到计时器是在绿色旗帜被点击时开始计时，而不是游戏开始时开始的吗？

![Timer has started](images/brain-timer-bug.png)

\--- task \---

你可以更改计时器的代码，以便在玩家点击按钮时启动计时器吗？

\--- /task \---

\--- task \--- 为你的按钮精灵添加代码，使按钮在每次游戏结束时再次显示。

![Button sprite](images/button-sprite.png)

```blocks3
    when I receive [end v]
    show
```

\--- /task \---

\--- task \---

通过玩几场游戏来测试“Play”按钮。该按钮应在每场游戏结束时显示。

为了更快地测试游戏，你可以更改`time`{:class="block3variables"}的值，这样每次游戏只持续几秒钟。

![Stage](images/stage-sprite.png)

```blocks3
    set [time v] to [10]
```

\--- /task \---

\--- task \--- You can change how the button looks when the mouse pointer hovers over it.

![Button](images/button-sprite.png)

```blocks3
    when flag clicked
    show
    forever
    if <touching (mouse-pointer v)?> then
        set [fisheye v] effect to (30)
    else
        set [fisheye v] effect to (0)
    end
    end
```

![screenshot](images/brain-fisheye.png) \--- /task \---