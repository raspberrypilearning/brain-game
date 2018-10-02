\--- challenge \---

## Izazov: Utrka do 10 bodova

Možeš li promijeniti igru ​​tako da, umjesto odgovaranja na što više pitanja u 30 sekundi, igrač provjeri koliko brzo može točno odgovoriti na 10 pitanja?

To možeš napraviti mijenjanjem kôda brojača. Vidiš li što treba promijeniti?

```blocks
    kada primim [kreni v]
postavi [vrijeme v] na (30)
ponavljaj dok nije <(vrijeme) = [0]>
čekaj (1) sekundi
promijeni [vrijeme v] za (-1)
end
pošalji [kraj v]
```

\--- /challenge \---