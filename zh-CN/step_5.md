## 重复游戏

现在，您将添加一个“开始”按钮，以便玩家可以多次开始游戏。

--- task ---

创建一个新的“开始”按钮精灵，让玩家点击来开始新游戏。

您可以自己绘制精灵，也可以从库中编辑精灵。

![开始按钮图片](images/brain-play.png)

--- /task ---

--- task ---

将此代码添加到按钮精灵中：

![按钮精灵](images/button-sprite.png)

```blocks3
    当 ⚑ 被点击
    显示

    当角色被点击
    隐藏
    广播(开始 v)
```

--- /task ---

新代码包括另一个`广播`{:class="block3events"}积木，它发送“开始”消息。

当玩家点击旗帜时，新代码会显示“开始”按钮精灵。 当玩家点击按钮精灵时，精灵会隐藏，然后广播信息，让其他精灵做出反馈。

此时，角色精灵在玩家点击旗帜时开始提问。 更改游戏代码，以便当它收到“开始”`广播`{:class="block3events"}时，角色精灵开始提问。

--- task ---

选择您的角色精灵，并在其代码部分中，用`当接收到开始`{:class="block3events"}积木替换`当 ⚑ 被点击`{:class="block3events"}积木。

![角色精灵](images/giga-sprite.png)

```blocks3
- when flag clicked
+ when I receive [开始 v]
set [数字1 v] to (pick random (2) to (12))
set [数字2 v] to (pick random (2) to (12))
ask (join (数字1)(join [ x ] (数字2))) and wait
if <(answer) = ((数字1)*(数字2))> then
	say [对! :)] for (2) seconds
else
	say [不对 :(] for (2) seconds
end
```

--- /task ---

--- task ---

点击绿色旗帜，然后单击新的“开始”按钮以测试其是否正常工作。您应该看到在点击按钮之前游戏不会开始。

--- /task ---

您能看到计时器是在绿色旗帜被点击时开始计时，而不是游戏开始时开始的吗？

![计时器开启](images/brain-timer-bug.png)

--- task ---

您可以更改计时器的代码，以便在玩家点击按钮时启动计时器吗？

--- /task ---

--- task ---

为您的按钮精灵添加代码，使按钮在每次游戏结束时再次显示。

![按钮精灵](images/button-sprite.png)

```blocks3
    当接收到 [结束 v]
    显示
```

--- /task ---

--- task ---

通过玩几场游戏来测试“开始”按钮。按钮应在每场游戏结束时显示。

为了更快地测试游戏，你可以更改`时间`{:class="block3variables"}的值，这样每次游戏只持续几秒钟。

![舞台](images/stage-sprite.png)

```blocks3
    将 [时间 v] 设为 [10]
```

--- /task ---

--- task ---

当鼠标指针悬停在按钮上时，您可以更改其外观。

![按钮](images/button-sprite.png)

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

![截屏](images/brain-fisheye.png)

--- /task ---