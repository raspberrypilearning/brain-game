## 重複遊玩

現在，你將添加一個「遊玩」按鈕，玩家就能重複玩這個遊戲。

--- task ---

創建一個名為「遊玩」的按鈕角色，玩家必須要點擊這個按鈕才可以讓遊戲開始。

你可以自己畫一個，或是從角色範例庫中挑選然後修改。

![遊玩按鈕的圖片](images/brain-play.png)

--- /task ---

--- task ---

編寫遊玩按鈕的程式：

![按鈕角色](images/button-sprite.png)

```blocks3
    當 @greenflag 被點擊
    顯示

    當角色被點擊
    隱藏
    廣播訊息 (開始 v)
```

--- /task ---

新的程式包含了另一個`廣播`{:class="block3events"}積木，用來發送「開始」訊息。

這個新程式會在玩家點擊綠旗時，在畫面中出現「遊玩」的按鈕。 玩家只要點擊，按鈕就會隱藏然後廣播，聽到這個訊息的其它程式就能做出反應。

不過，目前玩家只要點擊綠旗，Giga 就會開始發問。 修改你的程式，讓角色在收到「開始」的`廣播`{:class="block3events"}後，才開始問問題。

--- task ---

選取 Giga，把`當綠旗被點擊`{:class="block3events"}積木換成`當收到訊息開始`{:class="block3events"}。

![角色](images/giga-sprite.png)

```blocks3
- when flag clicked
+ when I receive [開始 v]
set [被乘數 v] to (pick random (2) to (12))
set [乘數 v] to (pick random (2) to (12))
ask (join (被乘數)(join [ x ] (乘數))) and wait
if <(answer) = ((被乘數)*(乘數))> then
	say [答對！] for (2) seconds
else
	say [答錯！] for (2) seconds
end
```

--- /task ---

--- task ---

點擊綠旗運行程式，接著點擊新的「遊玩」按鈕，測試程式是否正常運行。在點擊這個按鈕前，遊戲應該不會開始。

--- /task ---

你發現這個問題了嗎？計時是在點擊綠旗開始，而不是按下遊玩的按鈕？

![計時已開始](images/brain-timer-bug.png)

--- task ---

你可以修改計時的程式，讓它在點擊遊戲的按鈕後再倒數嗎？

--- /task ---

--- task ---

添加程式到你的按鈕角色，讓它在每次遊戲結束時再顯示該按鈕。

![按鈕角色](images/button-sprite.png)

```blocks3
    當收到訊息 (結束 v)
    顯示
```

--- /task ---

--- task ---

多玩幾次，測試「遊玩」按鈕是不是正常運行，按鈕應該只會在每次遊戲結束才顯示。

為了加快測試，你可以先把`計時`{:class="block3variables"}的值改小一點，這樣每次遊戲的時間就會比較短。

![舞台](images/stage-sprite.png)

```blocks3
    變數 [計時 v] 設為 (10)
```

--- /task ---

--- task ---

你可以在滑鼠懸停在按鈕上時，加入一些外觀效果。

![按鈕](images/button-sprite.png)

```blocks3
    when flag clicked
	show
	forever
	if <touching (mouse-pointer v)?> then
		set [fisheye v] effect to (30)
	else
		set [fisheye v] effect to (0)
	end
	end
```

![截圖](images/brain-fisheye.png)

--- /task ---