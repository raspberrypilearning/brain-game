## 创建问题

首先，你需要创建随机问题，这些问题玩家必须回答。

\--- task \---

打开一个新的Scratch项目

**在线：**在[rpf.io/scrath-new](http://rpf.io/scratch-new){:target="_blank"}打开一个新的Scratch在线项目 。

**离线：**在离线编辑器中打开一个新项目。

如果您需要下载并安装Scratch离线编辑器，可以在[ rpf.io/scratchoff ](http://rpf.io/scratchoff)中获取 {:target="_blank"}。

\--- /task \---

\--- task \--- 为你的游戏添加精灵角色和背景。你可以选择你喜欢的！比如：

![截图](images/brain-setting.png)

\--- /task \---

\--- task \--- 确保你拥有选择的角色精灵。 创建两个新变量，命名为`数字1 ` {:class =“block3variables”}和`数字2 ` {:class =“block3variables”}，用于存储测验题目的数字。

![截图](images/giga-sprite.png) ![截图](images/brain-variables.png)

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- task \--- Add code to your character sprite to set both of the `variables`{:class="block3variables"} to a `random`{:class="block3operators"} number between 2 and 12.

![screenshot](images/giga-sprite.png)

```blocks3
when flag clicked
set [number 1 v] to (pick random (2) to (12))
set [number 2 v] to (pick random (2) to (12))
```

\--- /task \---

\--- task \--- Add code to `ask`{:class="block3sensing"} the player for the answer, and then `say for 2 seconds`{:class="block3looks"} whether the answer was right or wrong:

![screenshot](images/giga-sprite.png)

```blocks3
when flag clicked
set [number 1 v] to (pick random (2) to (12))
set [number 2 v] to (pick random (2) to (12))

+ ask (join (number 1)(join [ x ] (number 2))) and wait
+ if <(answer) = ((number 1)*(number 2))> then
+ say [yes! :)] for (2) seconds
+ else
+ say [no :(] for (2) seconds
+ end
```

\--- /task \---

\--- task \---

Test your project twice: answer one question correctly, and the other incorrectly.

\--- /task \---

\--- task \---

Add a `forever`{:class="block3control"} loop around this code, so that the game asks the player lots of questions in a row.

\--- hints \--- \--- hint \---

You need to add a `forever`{:class="block3control"} block, and put all of the code except the `when flag clicked`{:class="block3control"} block into it.

\--- /hint \--- \--- hint \--- Here is the block you need:

```blocks3
forever
end
```

\--- /hint \--- \--- hint \--- Here is what your code should look like:

```blocks3
when flag clicked

+ forever
    set [number 1 v] to (pick random (2) to (12))
    set [number 2 v] to (pick random (2) to (12))
    ask (join (number 1)(join [ x ] (number 2))) and wait
    if <(answer) = ((number 1)*(number 2))> then
        say [yes! :)] for (2) seconds
    else
        say [no :(] for (2) seconds
    end
end
```

\--- /hint \--- \--- /hints \---

\--- /task \---