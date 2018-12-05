\--- challenge \---

## Udfordring: Kapløb til 10 point

Kan du ændre dit spil, så i stedet for at besvare så mange spørgsmål som muligt inden for 30 sekunder, skal spilleren se, hvor hurtigt de kan få 10 spørgsmål korrekt?

For at gøre dette skal du kun ændre din timerkode. Kan du se, hvad der skal ændres?

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