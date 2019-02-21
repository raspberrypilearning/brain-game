## Thử thách: cuộc đua tới 10 điểm

Bạn có thể thay đổi trò chơi của bạn để cho người chơi, thay vì trả lời càng nhiều câu hỏi càng tốt trong vòng 30 giây, hãy trả lời 10 câu hỏi càng nhanh càng tốt.

Để thay đổi nó, bạn chỉ cần đổi mã trong bộ đếm giờ. Bạn có thể nhìn thấy những khối nào cần để khác biệt không?

```blocks3
    khi tôi nhận được [bắt đầu v]
đặt [thời gian v] thành (30)
lặp cho tới khi <(thời gian) = [0]>
chờ (1) giây
thay [thời gian v] bằng (-1)
kết thúc
phát tín hiệu (kết thúc v)
```