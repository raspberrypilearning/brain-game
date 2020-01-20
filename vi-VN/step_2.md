## Tạo câu hỏi

Bạn sẽ bắt đầu bằng cách tạo các câu hỏi ngẫu nhiên mà người chơi phải trả lời.

\---nhiệm vụ\---

Mở một dự án Scratch mới.

**Online:** open a new online Scratch project at [rpf.io/scratch-new](http://rpf.io/scratch-new){:target="_blank"}.

**Ngoại tuyến:** mở một dự án mới trong trình chỉnh sửa ngoại tuyến.

Nếu bạn cần tải xuống và cài đặt trình soạn thảo ngoại tuyến Scratch, bạn có thể tìm thấy nó tại [rpf.io/scratchoff](http://rpf.io/scratchoff){: target = "_ blank"}.

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
khi cờ nhấp
đặt [số 1 v] thành (chọn ngẫu nhiên (2) thành (12))
đặt [số 2 v] thành (chọn ngẫu nhiên (2) thành (12)
```

\--- /task \---

\--- task \---

Add code to `ask`{:class="block3sensing"} the player for the answer, and then `say for 2 seconds`{:class="block3looks"} whether the answer was right or wrong:

![screenshot](images/giga-sprite.png)

```blocks3
khi cờ nhấp
đặt [số 1 v] thành (chọn ngẫu nhiên (2) thành (12))
đặt [số 2 v] thành (chọn ngẫu nhiên (2) đến (12))

+ hỏi (tham gia (số 1) (tham gia [x] (số 2))) và đợi
+ nếu <(trả lời) = ((số 1) * (số 2))> thì
+ nói [có! :)] trong (2) giây
+ khác
+ nói [không :(] trong (2) giây
+ kết thúc
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
mãi mãi
kết thúc
```

\--- /hint \---

\--- hint \---

Here is what your code should look like:

```blocks3
khi cờ nhấp

+ mãi mãi
    bộ [số 1 v] thành (chọn ngẫu nhiên (2) thành (12))
    đặt [số 2 v] thành (chọn ngẫu nhiên (2) đến (12))
    hỏi (tham gia (số 1) (tham gia [x] (số 2))) và đợi
    nếu <(câu trả lời) = ((số 1) * (số 2))> thì
        nói [có! :)] for (2) giây
    khác
        nói [không có :(] for (2) giây
    cuối
cuối
```

\--- /hint \---

\--- /hints \---

\--- /task \---