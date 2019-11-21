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

\--- task \--- 确保你已选中你的角色精灵。 创建两个新变量，命名为`number1 ` {:class =“block3variables”}和`number2 ` {:class =“block3variables”}，用于存储测验题目的数字。

![截图](images/giga-sprite.png) ![截图](images/brain-variables.png)

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- task \--- 为你的角色精灵添加代码以设置两个`变量` {：class =“ block3variables”}为2到12之间的`随机` {：class =“ block3operators”}数字。

![截屏](images/giga-sprite.png)

```blocks3
when flag clicked
set [number 1 v] to (pick random (2) to (12))
set [number 2 v] to (pick random (2) to (12))
```

\--- /task \---

\--- task \--- 在`ask`{:class="block3sensing"} 模块中添加代码以向玩家询问答案，无论回答正确还是错误，都添加`say for 2 seconds`{:class="block3looks"}模块。

![截屏](images/giga-sprite.png)

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

测试你的项目两次：正确回答一个问题，错误回答另一个问题。

\--- /task \---

\--- task \---

对这段代码添加一个`forever`{:class="block3control"}循环，这样游戏就会连续询问玩家更多问题。

\--- hints \--- \--- hint \---

你需要添加一个`forever`{:class="block3control"}模块，然后把除了`when flag clicked`{:class="block3control"}模块的其它所有模块都放入其中。

\--- /hint \--- \--- hint \--- 以下是您需要的代码块：

```blocks3
forever
end
```

\--- /hint \--- \--- hint \--- 你的代码应该是这个样子：

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