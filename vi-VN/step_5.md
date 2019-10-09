## Nhiều trò chơi

Bây giờ bạn sẽ thêm nút 'Phát' để người chơi có thể chơi trò chơi của bạn nhiều lần.

\--- task \--- Tạo một sprite nút 'Play' mới mà người chơi cần nhấp để bắt đầu một trò chơi mới.

Bạn có thể tự vẽ sprite hoặc chỉnh sửa sprite từ thư viện.

![Hình ảnh của nút phát](images/brain-play.png)

\--- /task \---

\--- task \--- Thêm mã này vào sprite nút của bạn:

![Nút sprite](images/button-sprite.png)

```blocks3
    khi cờ nhấp
    hiển thị

    khi sprite này nhấp
    ẩn
    phát (bắt đầu v)
```

\--- /task \---

Mã mới bao gồm một khối `phát`{: class = "block3events"} khác, sẽ gửi thông báo 'bắt đầu'.

Mã mới làm cho nút 'Phát' hiển thị khi người chơi nhấp vào cờ. Khi người chơi nhấp vào nút sprite, sprite sẽ ẩn và sau đó phát đi một thông điệp mà các sprite khác có thể phản ứng.

Hiện tại, nhân vật bắt đầu đặt câu hỏi khi người chơi nhấp vào cờ. Thay đổi mã trò chơi của bạn để sprite nhân vật bắt đầu đặt câu hỏi khi nhận được 'bắt đầu' `quảng bá`{: class = "block3events"}.

\--- task \--- Chọn sprite ký tự của bạn và, trong phần mã của nó, thay thế `khi cờ nhấp vào khối`{: class = "block3events"} bằng khối `khi tôi nhận được start`{: class = "block3events" } khối.

![Đối tượng nhân vật](images/giga-sprite.png)

```blocks3
<br />- khi cờ nhấp
+ khi tôi nhận được [bắt đầu v]
bộ [số 1 v] thành (chọn ngẫu nhiên (2) đến (12))
đặt [số 2 v] thành (chọn ngẫu nhiên (2) thành (12) )
hỏi (tham gia (số 1) (tham gia [x] (số 2))) và đợi
nếu <(trả lời) = ((số 1) * (số 2))> rồi
    nói [có! :)] trong (2) giây
khác
    nói [không :(] cho (2) giây
kết thúc
```

\--- /task \---

\--- task \---

Nhấp vào cờ màu xanh lục, rồi nhấp vào nút 'Phát' mới để kiểm tra xem nó có hoạt động không. Bạn sẽ thấy rằng trò chơi không bắt đầu trước khi bạn nhấp vào nút.

\--- /task \---

Bạn có thể thấy rằng bộ hẹn giờ bắt đầu khi cờ xanh được nhấp, thay vì khi trò chơi bắt đầu không?

![Hẹn giờ đã bắt đầu](images/brain-timer-bug.png)

\--- task \---

Bạn có thể thay đổi mã cho bộ hẹn giờ để bộ hẹn giờ bắt đầu khi người chơi nhấp vào nút không?

\--- /task \---

\--- task \--- Thêm mã vào sprite nút của bạn để nút hiển thị lại vào cuối mỗi trò chơi.

![Nút sprite](images/button-sprite.png)

```blocks3
    khi tôi nhận được [kết thúc v]

```

\--- /task \---

\--- task \---

Kiểm tra nút 'Play' bằng cách chơi một vài trò chơi. Nút sẽ hiển thị ở cuối mỗi trò chơi.

Để kiểm tra trò chơi nhanh hơn, bạn có thể thay đổi giá trị `lần`{: class = "block3variables"} để mỗi trò chơi chỉ dài vài giây.

![Sân khấu](images/stage-sprite.png)

```blocks3
    đặt [thời gian v] thành [10]
```

\--- /task \---

\--- task \--- Bạn có thể thay đổi giao diện của nút khi con trỏ chuột di chuyển qua nó.

![Nút](images/button-sprite.png)

```blocks3
    khi cờ nhấp
    hiển thị
    mãi mãi
    nếu <touching (mouse-pointer v)?> thì
        đặt hiệu ứng [fisheye v] thành (30)
    khác
        đặt hiệu ứng [fisheye v] thành (0)
    kết thúc
    kết thúc
```

![ảnh chụp màn hình](images/brain-fisheye.png) \--- /task \---