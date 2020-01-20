## 創建問題

您將首先創建玩家必須回答的隨機問題。

\---任務\---

打開一個新的Scratch項目。

**Online:** open a new online Scratch project at [rpf.io/scratch-new](http://rpf.io/scratch-new){:target="_blank"}.

**離線：** 在離線編輯器中打開一個新項目。

如果您需要下載並安裝Scratch離線編輯器，可以在 [rpf.io/scratchoff](http://rpf.io/scratchoff){：target =“_ blank”}找到它。

\--- /任務\---

\--- task \---

Add a character sprite and a backdrop for your game. You can choose any you like! Here's an example:

![screenshot](images/brain-setting.png)

\--- /task \---

\--- task \---

Make sure you have your character sprite selected. Create two new variables, called `number 1`{:class="block3variables"} and `number 2`{:class="block3variables"}, to store the numbers for the quiz questions.

![screenshot](images/giga-sprite.png)

![screenshot](images/brain-variables.png)

[[[generic-scratch3-add-variable]]]

\--- /任務\---

\--- task \---

Add code to your character sprite to set both of the `variables`{:class="block3variables"} to a `random`{:class="block3operators"} number between 2 and 12.

![screenshot](images/giga-sprite.png)

```blocks3
當標記點擊時
設置[數字1 v]到（選擇隨機（2）到（12））
設置[數字2 v]到（選擇隨機（2）到（12））
```

\--- /task \---

\--- task \---

Add code to `ask`{:class="block3sensing"} the player for the answer, and then `say for 2 seconds`{:class="block3looks"} whether the answer was right or wrong:

![screenshot](images/giga-sprite.png)

```blocks3
當標記點擊時
設置[數字1 v]到（選擇隨機（2）到（12））
設置[數字2 v]到（選擇隨機（2）到（12））

+問（加入（數字1）） （加入[x]（數字2）））並等待
+如果 <（回答）=（（數字1）*（數字2））> 然後
+說[是！ :)] for（2）seconds
+ else
+ say [no :(] for（2）seconds
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
永遠
結束
```

\--- /hint \---

\--- hint \---

Here is what your code should look like:

```blocks3
當標誌點擊

+永遠
    集[數字1 v]到（挑選隨機（2）到（12））
    設置[數字2 v]到（挑選隨機（2）到（12））
    問（加入（數字） 1）（加入[x]（數字2）））並等待
    如果 <（回答）=（（數字1）*（數字2））> 然後
        說[是！ :)] for（2）秒
    else
        說[no :(] for（2）seconds
    end
end
```

\--- /hint \---

\--- /hints \---

\--- /task \---