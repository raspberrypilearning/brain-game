\--- challenge \---

## Завдання: Забіг на 10 балів

Чи можна змінити гру так, щоб замість відповідати на максимальну кількість запитань за 30 секунд гравець міг дізнатись наскільки швидко він може правильно відповісти на 10 запитань?

To do this, you'll only need to change your timer code. Can you see what needs to be changed?

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