## Tạo câu hỏi

Bạn sẽ bắt đầu bằng cách tạo các câu hỏi ngẫu nhiên mà người chơi phải trả lời.

\---nhiệm vụ\---

Mở một dự án Scratch mới.

**Trực tuyến:** mở dự án Scratch trực tuyến mới tại [rpf.io/scratchon](http://rpf.io/scratchon){: target = "_ blank"}.

**Ngoại tuyến:** mở một dự án mới trong trình chỉnh sửa ngoại tuyến.

Nếu bạn cần tải xuống và cài đặt trình soạn thảo ngoại tuyến Scratch, bạn có thể tìm thấy nó tại [rpf.io/scratchoff](http://rpf.io/scratchoff){: target = "_ blank"}.

\--- /task \---

\--- task \--- Thêm một nhân vật và bối cảnh cho trò chơi của bạn. Bạn có thể chọn bất kỳ bạn thích! Đây là một ví dụ:

![ảnh chụp màn hình](images/brain-setting.png)

\--- /task \---

\--- task \--- Hãy chắc chắn rằng bạn đã chọn nhân vật của mình. Tạo hai biến mới, được gọi là `số 1`{: class = "block3variables"} và `số 2`{: class = "block3variables"}, để lưu số cho các câu hỏi đố.

![ảnh chụp màn hình](images/giga-sprite.png) ![ảnh chụp màn hình](images/brain-variables.png)

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- Nhiệm vụ \--- Thêm mã để sprite nhân vật của bạn để thiết lập cả hai `biến`{: class = "block3variables"} với `ngẫu nhiên`{: class = "block3operators"} số từ 2 đến 12.

![ảnh chụp màn hình](images/giga-sprite.png)

```blocks3
khi cờ nhấp
đặt [số 1 v] thành (chọn ngẫu nhiên (2) thành (12))
đặt [số 2 v] thành (chọn ngẫu nhiên (2) thành (12)
```

\--- /task \---

\--- task \--- Thêm mã vào `hỏi`{: class = "block3sensing"} người chơi cho câu trả lời, và sau đó `nói trong 2 giây`{: class = "block3looks"} xem câu trả lời có đúng hay không sai rồi:

![ảnh chụp màn hình](images/giga-sprite.png)

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

Kiểm tra dự án của bạn hai lần: trả lời đúng một câu hỏi và câu hỏi còn lại không chính xác.

\--- /task \---

\--- task \---

Thêm một vòng lặp `mãi mãi`{: class = "block3control"} xung quanh mã này, để trò chơi hỏi người chơi rất nhiều câu hỏi liên tiếp.

\--- gợi ý \--- \--- gợi ý \---

Bạn cần thêm khối `mãi mãi`{: class = "block3control"} và đặt tất cả mã ngoại trừ khối `khi cờ nhấp vào khối`{: class = "block3control"}.

\--- / gợi ý \--- \--- gợi ý \--- Đây là khối bạn cần:

```blocks3
mãi mãi
kết thúc
```

\--- / gợi ý \--- \--- gợi ý \--- Đây là mã của bạn sẽ như thế nào:

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

\--- /hint \--- \--- /hints \---

\--- /task \---