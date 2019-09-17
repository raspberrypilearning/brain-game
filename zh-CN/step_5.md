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

\--- task \--- Select your character sprite and, in its code section, replace the `when flag clicked`{:class="block3events"} block with a `when I receive start`{:class="block3events"} block.

![Character sprite](images/giga-sprite.png)

```blocks3
<br />- when flag clicked
+ when I receive [start v]
set [number 1 v] to (pick random (2) to (12))
set [number 2 v] to (pick random (2) to (12))
ask (join (number 1)(join [ x ] (number 2))) and wait
if &lt;(answer) = ((number 1)*(number 2))&gt; then
    say [yes! :)] for (2) seconds
else
    say [nope :(] for (2) seconds
end
```

\--- /task \---

\--- task \---

Click the green flag, and then click on the new 'Play' button to test whether it works. You should see that the game doesn't start before you click on the button.

\--- /task \---

Can you see that the timer starts when the green flag is clicked, instead of when the game starts?

![Timer has started](images/brain-timer-bug.png)

\--- task \---

Can you change the code for the timer so that the timer starts when the player clicks on the button?

\--- /task \---

\--- task \--- Add code to your button sprite so that the button shows again at the end of each game.

![Button sprite](images/button-sprite.png)

```blocks3
    when I receive [end v]
    show
```

\--- /task \---

\--- task \---

Test the 'Play' button by playing a couple of games. The button should show at the end of each game.

To test the game more quickly, you can change the value of `time`{:class="block3variables"} so that each game is only a few seconds long.

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