## 建立隨機問題

首先，你需要建立隨機問題，讓玩家回答。

--- task ---

建立一個新的 Scratch 專案。

**線上版：**你可以連結 [rpf.io/scratch-new](https//rpf.io/scratch-new){:target="_blank"} 以新建專案。

**離線版：**在離線編輯器的工作列中開啟選單並點擊新建專案。

如果你需要 Scratch 離線版編輯器，可以連結到 [rpf.io/scratchoff](https//rpf.io/scratchoff){:target="_blank"}。

--- /task ---

--- task ---

為遊戲添加角色和背景，你可以選擇你喜歡的，這裡我要用 Giga 當角色：

![截圖](images/brain-setting.png)

--- /task ---

--- task ---

確定選取了你的角色後， 創建兩個變數，第一個叫`被乘數`{:class="block3variables"}，第二個叫`乘數`{:class="block3variables"}，用來暫時儲存要測驗的題目。

![截圖](images/giga-sprite.png)

![截圖](images/brain-variables.png)

[[[generic-scratch3-add-variable]]]

--- /task ---

--- task ---

在 Giga 角色上編程，把這兩個`變數`{:class="block3variables"}設為`隨機取數`{:class="block3operators"}，數字範圍介於 2 到 12 之間。

![截圖](images/giga-sprite.png)

```blocks3
when flag clicked
set [被乘數 v] to (pick random (2) to (12))
set [乘數 v] to (pick random (2) to (12))
```

--- /task ---

--- task ---

接著讓 Giga `詢問`{:class="block3sensing"}乘法問題，玩家在看到題目後輸入答案。等到回答後，Giga `說出 2 秒`{:class="block3looks"}，告訴玩家是答對還是答錯：

![截圖](images/giga-sprite.png)

```blocks3
when flag clicked
set [被乘數 v] to (pick random (2) to (12))
set [乘數 v] to (pick random (2) to (12))
+ ask (join (被乘數)(join [ x ] (乘數))) and wait
+ if <(answer) = ((被乘數)*(乘數))> then
+ say [答對！] for (2) seconds
+ else
+ say [答錯！] for (2) seconds
+ end
```

--- /task ---

--- task ---

測試你的專案兩次：一次答對，另一次故意答錯。

--- /task ---

--- task ---

用`重複無限次`{:class="block3control"}迴圈，讓玩家就會永無寧日，一直被問乘法問題。

--- hints ---


--- hint ---

你要用`重複無限次`{:class="block3control"}積木把整個程式包住（除了`點擊綠旗`{:class="block3control"} ）。

--- /hint ---

--- hint ---

這裡是你需要的程式積木：

```blocks3
forever
end
```

--- /hint ---

--- hint ---

你的程式看起來應該像這樣：

```blocks3
when flag clicked
+ forever
	set [被乘數 v] to (pick random (2) to (12))
	set [乘數 v] to (pick random (2) to (12))
	ask (join (被乘數)(join [ x ] (乘數))) and wait
	if <(answer) = ((被乘數)*(乘數))> then
		say [答對！] for (2) seconds
	else
		say [答錯！] for (2) seconds
	end
end
```

--- /hint ---

--- /hints ---

--- /task ---
