## Sfida: guadagna 10 punti

Puoi cambiare il gioco in modo che il giocatore, invece di rispondere a quante più domande possibili in 30 secondi, risponda a 10 domande il più rapidamente possibile.

Per apportare questa modifica, è sufficiente modificare il codice del timer. Riesci a vedere quali blocchi devono essere diversi?

```blocks3
    when I receive [inizio v]
    set [tempo v] to (30)
    repeat until <(tempo :: variables) = [0]>
        wait (1) seconds
        change [tempo v] by (-1)
    end
    broadcast (fine v)
```
