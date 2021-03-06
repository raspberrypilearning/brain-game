## 添加计时器

--- task ---

用一个名为`时间`{:class="block3variables"}的新变量，在舞台中创建一个倒计时器。计时器应从30秒开始减至0秒。

![舞台精灵](images/stage-sprite.png)

--- hints ---


--- hint ---

创建一个`变量`{:class="block3variables"}，并命名为“time”，将其值设为`30`。

然后添加代码使`时间`{:class="block3variables"}在30秒内倒计至0。 为此，将`时间`{:class="block3variables"} 每经过`1`秒减`1`，重复执行直到`时间`{:class="block3variables"} 等于`0`。

--- /hint ---

--- hint ---

以下是你需要的积木：

```blocks3
重复执行直到 < >

end

等待 (1) 秒

将 [时间 v] 增加 (1)

(时间)

当 ⚑ 被点击

<() = ()>

将 [时间 v] 设为 [0]
```

--- /hint ---

--- hint ---

您的代码看起来应该是这样的：

```blocks3
当 ⚑ 被点击
将 [时间 v] 设为 [30]
重复执行直到 <(时间) = (0)>
    等待 (1) 秒
    将 [时间 v] 增加 (-1)
end
```

--- /hint ---

--- /hints ---

--- /task ---

--- task ---

创建一个`广播`{:class="block3control"}发送消息“结束”。 `广播`{:class="block3control"}就像是通过扬声器发出的公告：你的所有精灵都可以听到。 在计时器代码的后面添加`广播`{:class="block3control"}积木，这样当`时间`{:class="block3variables"}减至`0`时就能发出“结束”消息。

![舞台精灵](images/stage-sprite.png)

```blocks3
    广播 (结束 v)
```

--- /task ---

--- task ---

选择您的角色精灵并添加一些代码，以使精灵在收到`结束`{:class="block3control"}消息时`停止其他脚本`{:class="block3control"}。

![Giga精灵](images/giga-sprite.png)

```blocks3
    当接收到 [结束 v]
    停止 [该角色的其他脚本 v]
```

--- /task ---

--- task ---

再次测试您的游戏。它应该继续提出问题，直到计时器倒数至0。

--- /task ---