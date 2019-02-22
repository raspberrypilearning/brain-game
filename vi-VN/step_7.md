## Thêm đồ họa

Lúc này, nhân vật sprite chỉ nói `có!)`hoặc`không:(` cho câu trả lời của người chơi. Thêm một vài đồ hoạ để người chơi biết câu trả lời của họ chính xác hay không.

\---nhiệm vụ\---

Tạo một đối tượng mới gọi là 'Kết quả', và cho nó 'chọn/kiểm tra' và bộ trang phục 'gạch ngang'.

![Sprite with tick and cross costumes](images/brain-result.png)

\---/nhiệm vụ\---

\--- nhiệm vụ \---

Thay mã đối tượng của bạn để, thay vì nói gì đó với người chơi, nó ` phát tin ` {: class = "block3events"} các thông báo 'chính xác' hoặc 'sai'.

![Character sprite](images/giga-sprite.png)

```blocks3
nếu <(đáp án) = ((số 1) * (số 2))> thì

- nói [có! :)] trong (2) giây
+ phát tin (đúng v)
ngược lại
- nói [không :(] trong (2) giây
+ phát sóng (sai v)
kết thúc
```

\---/nhiệm vụ\---

\---nhiệm vụ\---

Bây giờ bạn có thể sử dụng các tin nhắn này để ` hiển thị ` {: class = "block3looks"} trang phục 'tick' hoặc 'cross'. Thêm mã sau vào sprite 'Kết quả':

![Result sprite](images/result-sprite.png)

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

\---/nhiệm vụ\---

\---nhiệm vụ\--- Kiểm tra lại trò chơi của bạn. Bạn có thể thấy dấu chọn bất cứ khi nào bạn trả lời đúng, và dấu chéo khi bạn trả lời câu hỏi không chính xác!

![Tick for correct, cross for wrong answer](images/brain-test-answer.png)

\---/nhiệm vụ\---

Bạn có thể thấy rằng mã cho ` khi tôi nhận được chính xác ` {: class = "block3events"} và ` khi tôi nhận được sai ` {: class = "block3events"} gần giống nhau?

Vì vậy bạn có thể thay đổi mã của mình dễ dàng hơn, bạn sẽ tạo một khối tùy chỉnh.

\---nhiệm vụ\---

Chọn đối tượng 'Kết quả'. Sau đó nhấp vào ` Khối của tôi ` {: class = "block3myblocks"}, và sau đó trên ** Tạo khối **. Tạo một khối mới và gọi nó là ` animate ` {: class = "block3myblocks"}.

![Result sprite](images/result-sprite.png)

![Create a block called animate](images/brain-animate-function.png)

\---/nhiệm vụ\---

\--- task \--- Move the code to `show`{:class="block3looks"} and `hide`{:class="block3looks"} the 'Result' sprite into the `animate`{:class="block3myblocks"} block:

![Result sprite](images/result-sprite.png)

```blocks3
define animate
show
wait (1) seconds
hide
```

\---/nhiệm vụ\---

\--- nhiệm vụ \--- Đảm bảo bạn đã loại bỏ `hiển thị` {: class = "block3looks"} và ` ẩn ` {: class = "block3looks"} khối bên dưới ** cả hai ** đổi trang phục ` ` {: class = "block3looks"} khối.

Then add the `animate`{:class="block3myblocks"} block below both of the `switch costume`{:class="block3looks"} blocks. Your code should now look like this:

![Result sprite](images/result-sprite.png)

```blocks3
    when I receive [correct v]
    switch costume to (tick v)
    animate:: custom

    when I receive [wrong v]
    switch costume to (cross v)
    animate:: custom
```

\---/nhiệm vụ\---

Because of the custom `animate`{:class="block3myblocks"} block, you now only need to make one change to your code if you want to show the 'Result' sprite's costumes a longer or shorter time.

\---nhiệm vụ\---

Change your code so that the 'tick' or 'cross' costumes display for 2 seconds.

\---/nhiệm vụ\---

\--- task \--- Instead of `showing`{:class="block3looks"} and `hiding`{:class="block3looks"} the 'tick' or 'cross' costumes, you could change your `animate`{:class="block3myblocks"} block so that the costumes fade in.

![Result sprite](images/result-sprite.png)

```blocks3
    define animate
    set [ghost v] effect to (100)
    show
    repeat (25)
        change [ghost v] effect by (-4)
    end
    hide
```

\---/nhiệm vụ\---

Can you improve the animation of the 'tick' or 'cross' graphics? You could add code to make the costumes fade out as well, or you could use other cool effects:

![screenshot](images/brain-effects.png)