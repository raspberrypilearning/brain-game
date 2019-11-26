## 挑战：争得 10 分

您是否可以更改游戏方式，使玩家不必在30秒内回答尽可能多的问题，而应尽快回答10个问题。

要做此更改，您只需更改计时器代码。您可以看出哪些模块需要不同吗？

```blocks3
    when I receive [start v]
    set [time v] to (30)
    repeat until <(time) = [0]>
        wait (1) seconds
        change [time v] by (-1)
    end
    broadcast (end v)
```