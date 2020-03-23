## 과제: 10 점까지 레이스

플레이어가 30 초 안에 가능한 많은 질문에 대답하는 대신 가능한 한 빨리 10개의 질문에 대답하도록 게임을 변경할 수 있습니까?

이렇게 변경하려면 타이머 코드만 수정하면 됩니다. 어떻게 수정할 수 있을까요?

```blocks3
    when I receive [start v]
    set [time v] to (30)
    repeat until <(time) = [0]>
        wait (1) seconds
        change [time v] by (-1)
    end
    broadcast (end v)
```