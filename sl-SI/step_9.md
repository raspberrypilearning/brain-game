## Izziv: dirka do 10 točk

Ali lahko spremeniš igro, tako da bo igralec moral namesto tega, da odgovori na čim več vprašanj v 30 sekundah, moral odgovoriti na 10 vprašanj v čim krajšem času.

Da bi to dosegel, moraš spremeniti le kodo časovnika. Ali veš, kateri bloki bi morali biti drugačni?

```blocks3
    ko prejmem [začni v]
  nastavi [čas v] na (30)
  ponavljaj do <(čas) = [0]>
    počakaj (1) sekund
    spremeni [čas v] za (-1)
  konec
  objavi (konec v)
```