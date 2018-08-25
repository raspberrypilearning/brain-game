\--- challenge \---

## Izazov: utrka do 10 bodova

Možete li promijeniti igru ​​tako da, umjesto da odgovaranja na što više pitanja u 30 sekundi, igrač mora vidjeti koliko brzo mogu točno odgovoriti na 10 pitanja?

Da biste to učinili, morat ćete samo promijeniti svoj kôd brojača. Možete li vidjeti što treba mijenjati?

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