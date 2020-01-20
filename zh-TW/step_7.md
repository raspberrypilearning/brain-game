## 添加圖形

目前，角色精靈只是說 `是的！ :)` 或 `否:(` 到玩家的答案。添加一些圖形讓玩家知道他們的答案是正確還是不正確。

\---任務\---

創建一個名為'Result'的新精靈，並給它一個'tick / check'和'cross'服裝。

![精靈與蜱和交叉服飾](images/brain-result.png)

\--- /任務\---

\---任務\---

改變你的性格精靈的代碼，這樣，而不是說事的球員，這 `播放`{：類=“block3events”}消息“正確”或“錯誤”。

![人物精靈](images/giga-sprite.png)

```blocks3
如果 <（回答）=（（數字1）*（數字2））> 然後

- 說[是的！ :)] for（2）秒
+廣播（正確v）
其他
- 說[nope :(] for（2）秒
+廣播（錯誤v）
結束
```

\--- /任務\---

\---任務\---

現在，您可以使用這些消息 `顯示`{：類=“block3looks”}的'滴答'或'交叉'服裝。將以下代碼添加到'Result'精靈：

![結果精靈](images/result-sprite.png)

```blocks3
    當我收到[正確的v]
    開關服裝（勾選v）
    顯示
    等待（1）秒
    隱藏

    當我收到[錯誤的v]
    開關服裝到（交叉v）
    顯示
    等待（1）秒
    當標記點擊
    隱藏時隱藏


```

\--- /任務\---

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
定義動畫
顯示
等待（1）秒
隱藏
```

\--- /task \---

\--- task \---

Make sure you have removed the `show`{:class="block3looks"} and `hide`{:class="block3looks"} blocks below **both** of the `switch costume`{:class="block3looks"} blocks.

Then add the `animate`{:class="block3myblocks"} block below both of the `switch costume`{:class="block3looks"} blocks. Your code should now look like this:

![Result sprite](images/result-sprite.png)

```blocks3
    當我收到[正確的v]
    開關服裝（勾選v）
    animate :: custom

    當我收到[錯誤的v]
    開關服裝到（交叉v）
    animate :: custom
```

\--- /task \---

Because of the custom `animate`{:class="block3myblocks"} block, you now only need to make one change to your code if you want to show the 'Result' sprite's costumes a longer or shorter time.

\--- task \---

Change your code so that the 'tick' or 'cross' costumes display for 2 seconds.

\--- /任務\---

\--- task \---

Instead of `showing`{:class="block3looks"} and `hiding`{:class="block3looks"} the 'tick' or 'cross' costumes, you could change your `animate`{:class="block3myblocks"} block so that the costumes fade in.

![Result sprite](images/result-sprite.png)

```blocks3
    定義動畫
    集[鬼v]效果到（100）
    表示
    重複（25）
        變化[鬼v]效果由（-4）
    結束
    隱藏
```

\--- /task \---

Can you improve the animation of the 'tick' or 'cross' graphics? You could add code to make the costumes fade out as well, or you could use other cool effects:

![screenshot](images/brain-effects.png)