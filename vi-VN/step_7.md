## Thêm đồ họa

Lúc này, nhân vật sprite chỉ nói `có!)`hoặc`không:(` cho câu trả lời của người chơi. Thêm một vài đồ hoạ để người chơi biết câu trả lời của họ chính xác hay không.

\--- task \---

Tạo một đối tượng mới gọi là 'Kết quả', và cho nó 'chọn/kiểm tra' và bộ trang phục 'gạch ngang'.

![Đối tượng với trang phục chọn và chéo](images/brain-result.png)

\--- /task \---

\--- nhiệm vụ \---

Thay mã đối tượng của bạn để, thay vì nói gì đó với người chơi, nó ` phát tin ` {: class = "block3events"} các thông báo 'chính xác' hoặc 'sai'.

![Đối tượng nhân vật](images/giga-sprite.png)

```blocks3
nếu <(đáp án) = ((số 1) * (số 2))> thì

- nói [có! :)] trong (2) giây
+ phát tin (đúng v)
ngược lại
- nói [không :(] trong (2) giây
+ phát sóng (sai v)
kết thúc
```

\--- /task \---

\--- task \---

Bây giờ bạn có thể sử dụng các tin nhắn này để ` hiển thị ` {: class = "block3looks"} trang phục 'tick' hoặc 'cross'. Thêm mã sau vào sprite 'Kết quả':

![Đối tượng kết quả](images/result-sprite.png)

```blocks3
    khi tôi nhận được [đúng v]
    chuyển trang phục sang (chọn v)
    hiển thị
    chờ (1) giây
    ẩn

    khi tôi nhận [sai v]
    chuyển trang phục sang (chéo v)
    hiển thị
    chờ (1) giây
    ẩn

    khi cờ được nhấp
    ẩn
```

\--- /task \---

\---nhiệm vụ\--- Kiểm tra lại trò chơi của bạn. Bạn có thể thấy dấu chọn bất cứ khi nào bạn trả lời đúng, và dấu chéo khi bạn trả lời câu hỏi không chính xác!

![Chọn cho đúng, chéo cho câu trả lời sai](images/brain-test-answer.png)

\--- /task \---

Bạn có thể thấy rằng mã cho ` khi tôi nhận được chính xác ` {: class = "block3events"} và ` khi tôi nhận được sai ` {: class = "block3events"} gần giống nhau?

Vì vậy bạn có thể thay đổi mã của mình dễ dàng hơn, bạn sẽ tạo một khối tùy chỉnh.

\--- task \---

Chọn đối tượng 'Kết quả'. Sau đó nhấp vào ` Khối của tôi ` {: class = "block3myblocks"}, và sau đó trên ** Tạo khối **. Tạo một khối mới và gọi nó là ` animate ` {: class = "block3myblocks"}.

![Đối tượng kết quả](images/result-sprite.png)

![Tạo một khối gọi là animate](images/brain-animate-function.png)

\--- /task \---

\--- task \--- Di chuyển mã đến ` hiển thị ` {: class = "block3looks"} và ` ẩn ` {: class = "block3looks"} sprite 'Kết quả' thành ` animate ` {: class = "block3myblocks"}:

![Đối tượng kết quả](images/result-sprite.png)

```blocks3
định nghĩa animate
hiển thị
chờ (1) giây
ẩn
```

\--- /task \---

\--- nhiệm vụ \--- Đảm bảo bạn đã loại bỏ `hiển thị` {: class = "block3looks"} và ` ẩn ` {: class = "block3looks"} khối bên dưới ** cả hai ** đổi trang phục ` ` {: class = "block3looks"} khối.

Sau đó thêm ` animate ` {: class = "block3myblocks"} bên dưới cả hai ` đổi trang phục`khối {: class = "block3looks"}. Mã của bạn bây giờ trông như thế này:

![Đối tượng kết quả](images/result-sprite.png)

```blocks3
    khi tôi nhận được [đúng v]
đổi trang phục thành (tick v)
animate:: custom

khi tôi nhận được [sai v]
đổi trang phục thành (chéo v)
animate:: custom
```

\--- /task \---

Vì tuỳ chỉnh khối`animate`khối{:class="block3myblocks"}, bây giờ chỉ cần làm một thay đổi cho mã của bạn nếu bạn muốn hiện đối tượng tuỳ chỉnh 'Kết quả' với thời gian lâu hơn hoặc nhanh hơn.

\--- task \---

Thay đổi mã của bạn để trang phục 'chọn' hoặc 'chéo' hiển thị trong 2 giây.

\--- /task \---

\--- nhiệm vụ \--- Thay vì `hiển thị` {:class="block3looks"} và `ẩn` {:class="block3looks"} trang phục 'chọn' hoặc 'chéo', bạn có thể thay đổi khối `animate` {:class="block3myblocks"} của bạn để trang phục mờ dần đi.

![Đối tượng kết quả](images/result-sprite.png)

```blocks3
    xác định hiệu ứng animate
    đặt [ghost v] thành (100)
    hiển thị
    lặp lại (25) lần
        thay đổi hiệu ứng [ghost v] bằng (-4)
    kết thúc
    ẩn
```

\--- /task \---

Bạn có thể cải thiện ảnh động của đồ họa 'chọn' hoặc 'chéo' không? Bạn có thể thêm mã để làm cho trang phục mờ dần, hoặc bạn có thể sử dụng các hiệu ứng thú vị khác:

![ảnh chụp màn hình](images/brain-effects.png)