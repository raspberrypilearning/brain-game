\--- 과제 \---

## 과제: 10 점까지의 레이스

그들은 30 초 내에 많은 질문에 대답 하는 대신 플레이어가 얻을 수 있는 10개 질문이 게임을 올바르게 변경할 수 있습니까?

이렇게 하려면, 타이어 코드만 변경하면 됩니다. 무엇을 변경해야 볼 수 있습니까?

```blocks
    when I receive [start v]
    set [time v] to (30)
    repeat until <(time) = [0]>
        wait (1) secs
        change [time v] by (-1)
    end
    broadcast [end v]
```

\--- /challenge \---