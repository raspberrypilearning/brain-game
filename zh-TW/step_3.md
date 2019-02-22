## 添加計時器

\--- task \--- 在一個名為 `time`{：class =“block3variables”}的新變量的幫助下，在舞台上創建一個倒數計時器。計時器應從30秒開始並倒計時至0秒。

![舞台精靈](images/stage-sprite.png)

\---提示\--- \---提示\---

創建一個 `變量`{：class =“block3variables”}，將其稱為'time'，並將其值設置為 `30`。

然後在30秒內添加代碼以將 `時間`{：class =“block3variables”}計數到0。 為此，每 `1` 秒從 `次`{：class =“block3variables”}中減去 `1` ，並重複此操作直到 `次`{：class =“block3variables”}等於 `0`。

\--- /提示\--- \---提示\--- 以下是您需要的塊：

```blocks3
重複直到 < >

結束

等待（1）秒

將[時間v]改變為（1）

（時間）

當標記被點擊時

<（）=（）>

將[時間v]設置為 [0]
```

\--- /提示\--- \---提示\--- 這是你的新代碼應該是這樣的：

```blocks3
當標記點擊時
設置[時間v]為 [30]
重複直到 <（時間）=（0）>
    等待（1）秒
    將[時間v]改變為（-1）
結束
```

\--- /提示\--- \--- /提示\---

\--- /任務\---

\---任務\---

創建一個發送消息'end'的 `廣播`{：class =“block3control”}。 `廣播`{：class =“block3control”}就像是通過揚聲器宣布：所有精靈都可以聽到它。 將 `廣播`{：class =“block3control”}塊添加到計時器代碼的末尾，以便代碼將在 `次`{：class =“block3variables”}計數到 `時發送和'結束'消息0`

![舞台精靈](images/stage-sprite.png)

```blocks3
    廣播（結束v）
```

\--- /任務\---

\--- task \--- 選擇你的角色精靈並添加一些代碼，以便sprite `在收到 <code>end`{：class =“block3control”}消息時停止其他腳本</code>{：class =“block3control”} 。

![千兆精靈](images/giga-sprite.png)

```blocks3
    當我收到[結束v]
    停止[精靈v中的其他腳本]
```

\--- /任務\---

\---任務\---

再次測試你的遊戲。在計時器倒計時到0之前，它應該繼續提問。

\--- /任務\---