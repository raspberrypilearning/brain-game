--- challenge ---

## Izazov: Trka do 10 bodova

Možeš li da izmijeniš svoju igru tako da, umjesto da odgovori na što više pitanja u 30 sekundi, igrač treba da provjeri koliko brzo može odgovoriti tačno na 10 pitanja?

Da to uradiš, potrebno je samo da izmijeniš svoj kôd za odbrojavanje vremena. Možeš li da uočiš šta treba da se izmijeni?

```blocks
    when I receive [kreni v]
    set [vrijeme v] to (30)
    repeat until <(vrijeme) = [0]>
        wait (1) secs
        change [vrijeme v] by (-1)
    end
    broadcast [kraj v]
```

--- /challenge ---