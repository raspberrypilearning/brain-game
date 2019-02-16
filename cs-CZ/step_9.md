## Výzva: desetibodový závod

Dokázal by si upravit hru tak, aby se namísto počítání správných odpovědí během 30 sekund počítal nejkratší čas během kterého hráč správně odpoví na 10 otázek?

Stačí upravit kód u časovače. Poznáš které bloky se změní?

```blocks3
    when I receive [start v]
    set [time v] to (30)
    repeat until <(time) = [0]>
        wait (1) seconds
        change [time v] by (-1)
    end
    broadcast (end v)
```