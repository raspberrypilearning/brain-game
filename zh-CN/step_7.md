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
    当接收到 [正确 v]
    换成 (对勾 v) 造型
    显示
    等待 (1) 秒
    隐藏

    当接收到 [错误 v]
    换成 (叉 v) 造型
    显示
    等待 (1) 秒
    隐藏

    当 ⚑ 被点击
    隐藏
```

\--- /task \---

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
定义 动画
显示
等待 (1) 秒
隐藏
```

\--- /task \---

\--- task \---

Make sure you have removed the `show`{:class="block3looks"} and `hide`{:class="block3looks"} blocks below **both** of the `switch costume`{:class="block3looks"} blocks.

Then add the `animate`{:class="block3myblocks"} block below both of the `switch costume`{:class="block3looks"} blocks. Your code should now look like this:

![Result sprite](images/result-sprite.png)

```blocks3
    当接收到 [正确 v]
    换成 (对勾 v) 造型
    动画:: custom

    当接收到 [错误 v]
    换成 (叉 v) 造型
    动画:: custom
```

\--- /task \---

Because of the custom `animate`{:class="block3myblocks"} block, you now only need to make one change to your code if you want to show the 'Result' sprite's costumes a longer or shorter time.

\--- task \---

Change your code so that the 'tick' or 'cross' costumes display for 2 seconds.

\--- /task \---

\--- task \---

Instead of `showing`{:class="block3looks"} and `hiding`{:class="block3looks"} the 'tick' or 'cross' costumes, you could change your `animate`{:class="block3myblocks"} block so that the costumes fade in.

![Result sprite](images/result-sprite.png)

```blocks3
    定义 动画
    将 [虚像 v] 特效设定为 (100)
    显示
    重复执行 (25)
        将 [虚像 v] 特效增加 (-4)
    end
    隐藏
```

\--- /task \---

Can you improve the animation of the 'tick' or 'cross' graphics? You could add code to make the costumes fade out as well, or you could use other cool effects:

![screenshot](images/brain-effects.png)