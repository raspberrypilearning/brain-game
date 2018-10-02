\--- challenge \---

## Izazov: Utrka do 10 bodova

Možeš li promijeniti igru ​​tako da, umjesto odgovaranja na što više pitanja u 30 sekundi, igrač provjeri koliko brzo može točno odgovoriti na 10 pitanja?

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