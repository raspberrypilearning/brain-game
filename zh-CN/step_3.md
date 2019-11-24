## 添加计时器

\--- task \--- 创建一个新变量名为`time`{:class="block3variables"}，以此在舞台中创建一个倒计时器。计时器应从30秒开始减至0秒。

![Stage sprite](images/stage-sprite.png)

\--- hints \--- \--- hint \---

创建一个`变量`{:class="block3variables"}，命名为“time”，并设置其值为`30`。

然后添加代码使`time`{:class="block3variables"}从30秒减至0。 为此，将`time`{:class="block3variables"} 每经过`1`秒减`1`，重复执行直到`time`{:class="block3variables"} 等于`0`。

\--- /hint \--- \--- hint \--- 以下是您需要的代码块：

```blocks3
repeat until < >

end

wait (1) seconds

change [time v] by (1)

(time)

when flag clicked

<() = ()>

set [time v] to [0]
```

\--- /hint \--- \--- hint \--- 你的新代码应该是这个样子：

```blocks3
when flag clicked
set [time v] to [30]
repeat until <(time) = (0)>
    wait (1) seconds
    change [time v] by (-1)
end
```

\--- /hint \--- \--- /hints \---

\--- /task \---

\--- task \---

创建一个`broadcast` {:class =“ block3control”}发送消息“end”。 `broadcast` {：class =“ block3control”}就像是通过扬声器发出的公告：您的所有精灵都可以听到。 在计时器代码的后面添加`broadcast`{:class="block3control"}代码块，这样当`time`{:class="block3variables"}减至`0`时就能发出“end”消息。

![Stage sprite](images/stage-sprite.png)

```blocks3
    broadcast (end v)
```

\--- /task \---

\--- task \--- Select your character sprite and add some code so that the sprite `stops the other scripts`{:class="block3control"} when it receives the `end`{:class="block3control"} message.

![Giga sprite](images/giga-sprite.png)

```blocks3
    when I receive [end v]
    stop [other scripts in sprite v]
```

\--- /task \---

\--- task \---

Test your game again. It should continue to ask questions until the timer has counted down to 0.

\--- /task \---