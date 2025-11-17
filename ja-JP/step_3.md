## タイマーを追加

--- task ---

`時間`{:class="block3variables"}という新しい変数を使用して、ステージ上にカウントダウンタイマーを作成します。 タイマーは30秒で始まり、0秒までカウントダウンします。

![ステージのスプライト](images/stage-sprite.png)

--- hints ---

--- hint ---

`変数`{:class="block3variables"}を作成して、名前を「時間」に変更し、値を `30` に設定します。

次に、30秒以内に `時間`{:class="block3variables"}を0までカウントするコードを追加します。 これをするには、 `1` を`タイマー`{:class="block3variables"} から`1` 秒ごとに引きます。そして、これを`タイマー`{:class="block3variables"} が`0`と一緒になるまで繰り返します。

--- /hint ---

--- hint ---

必要なブロックは次のとおりです。

```blocks3
repeat until < >

end

wait (1) seconds

change [時間 v] by (1)

(時間)

when flag clicked

<() = ()>

set [時間 v] to [0]
```

--- /hint ---

--- hint ---

新しいコードは次のようになります。

```blocks3
when flag clicked
set [時間 v] to [30]
repeat until <(時間) = (0)>
    wait (1) seconds
    change [時間 v] by (-1)
end
```

--- /hint ---

--- /hints ---

--- /task ---

--- task ---

メッセージ「終わり」を送信する `ブロードキャスト`{:class="block3control"}を作成します。 `ブロードキャスト`{:class="block3control"}はスピーカーでのアナウンスのようなものです。すべてのスプライトで聞くことができます。 `ブロードキャスト`{:class="block3control"}ブロックをタイマーコードの最後に追加して、 `時間`{:class="block3variables"}が `0 までカウントダウンされたとき`、コードが「終わり」メッセージを送信するようにします。

![ステージのスプライト](images/stage-sprite.png)

```blocks3
    broadcast (終了 v)
```

--- /task ---

--- task ---

キャラクタースプライトを選び、コードを追加して、スプライトが `他のスクリプトを停止する`{:class="block3control"} ようにします。`終わり`{:class="block3control"} メッセージを受信したときに。

![ギガスプライト](images/giga-sprite.png)

```blocks3
    when I receive [終了 v]
    stop [スプライトの他のスクリプト v]
```

--- /task ---

--- task ---

ゲームをもう一度テストします。タイマーが0になるまで質問を続ける必要があります。

--- /task ---