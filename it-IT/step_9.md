## Sfida: Suono e musica

Puoi cambiare il gioco in modo che il giocatore, invece di rispondere a quante più domande possibili in 30 secondi, risponda a 10 domande il più rapidamente possibile.

Per apportare questa modifica, è sufficiente modificare il codice del timer. Riesci a vedere quali blocchi devono essere diversi?

```blocks3
    quando ricevo [start v]
    set [time v] to (30)
    repeat fino a <(time) = [0]>
        wait (1) secondi
        change [time v] di (-1)
    end
    broadcast (fine v)
```