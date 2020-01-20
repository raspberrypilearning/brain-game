## 创建问题

首先，你需要创建随机问题，这些问题玩家必须回答。

\--- task \---

打开一个新的Scratch项目

**在线：**在[rpf.io/scrath-new](http://rpf.io/scratch-new){:target="_blank"}打开一个新的Scratch在线项目 。

**离线：**在离线编辑器中打开一个新项目。

如果您需要下载并安装Scratch离线编辑器，可以在[ rpf.io/scratchoff ](http://rpf.io/scratchoff)中获取 {:target="_blank"}。

\--- /task \---

\--- task \---

Add a character sprite and a backdrop for your game. You can choose any you like! Here's an example:

![screenshot](images/brain-setting.png)

\--- /task \---

\--- task \---

Make sure you have your character sprite selected. Create two new variables, called `number 1`{:class="block3variables"} and `number 2`{:class="block3variables"}, to store the numbers for the quiz questions.

![screenshot](images/giga-sprite.png)

![screenshot](images/brain-variables.png)

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- task \---

Add code to your character sprite to set both of the `variables`{:class="block3variables"} to a `random`{:class="block3operators"} number between 2 and 12.

![screenshot](images/giga-sprite.png)

```blocks3
当 ⚑ 被点击
将 [数字1 v] 设为 (在 (2) 和 (12) 之间取随机数)
将 [数字2 v] 设为 (在 (2) 和 (12) 之间取随机数)
```

\--- /task \---

\--- task \---

Add code to `ask`{:class="block3sensing"} the player for the answer, and then `say for 2 seconds`{:class="block3looks"} whether the answer was right or wrong:

![screenshot](images/giga-sprite.png)

```blocks3
当 ⚑ 被点击
将 [数字1 v] 设为 (在 (2) 和 (12) 之间取随机数)
将 [数字2 v] 设为 (在 (2) 和 (12) 之间取随机数)

+ 询问 (连接 (数字1) 和(连接 [ x ] (数字2))) 并等待
+ 如果 <(回答) = ((数字1)*(数字2))> 那么
+ 说 [对! :)] (2) 秒
+ 否则
+ 说 [不对 :(] (2) 秒
+ end
```

\--- /task \---

\--- task \---

Test your project twice: answer one question correctly, and the other incorrectly.

\--- /task \---

\--- task \---

Add a `forever`{:class="block3control"} loop around this code, so that the game asks the player lots of questions in a row.

\--- hints \---

\--- hint \---

You need to add a `forever`{:class="block3control"} block, and put all of the code except the `when flag clicked`{:class="block3control"} block into it.

\--- /hint \---

\--- hint \---

Here is the block you need:

```blocks3
重复执行
end
```

\--- /hint \---

\--- hint \---

Here is what your code should look like:

```blocks3
当 ⚑ 被点击

+ 重复执行
    将 [数字1 v] 设为 (在 (2) 和 (12) 之间取随机数)
    将 [数字2 v] 设为 (在 (2) 和 (12) 之间取随机数)
    询问 (连接 (数字1) 和 (连接 [ x ] 和 (数字2))) 并等待
    如果 <(回答) = ((数字1)*(数字2))> 那么
        说 [对! :)] (2) 秒
    否则
        说 [不对 :(] (2) 秒
    end
end
```

\--- /hint \---

\--- /hints \---

\--- /task \---