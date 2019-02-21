## Thử thách: cuộc đua tới 10 điểm

Bạn có thể thay đổi trò chơi của bạn để cho người chơi, thay vì trả lời càng nhiều câu hỏi càng tốt trong vòng 30 giây, hãy trả lời 10 câu hỏi càng nhanh càng tốt.

Để thay đổi nó, bạn chỉ cần đổi mã trong bộ đếm giờ. Bạn có thể nhìn thấy những khối nào cần để khác biệt không?

```blocks3
    when I receive [start v]
    set [time v] to (30)
    repeat until <(time) = [0]>
        wait (1) seconds
        change [time v] by (-1)
    end
    broadcast (end v)
```