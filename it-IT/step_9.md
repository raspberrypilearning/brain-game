## Sfida: Guadagna 10 punti

Puoi cambiare il gioco in modo che il giocatore, invece di rispondere a quante più domande possibili in 30 secondi, risponda a 10 domande il più rapidamente possibile.

Per apportare questa modifica, è sufficiente modificare il codice del timer. Riesci a vedere quali blocchi devono essere diversi?

```blocks3
    quando ricevo [inizio v]
porta [tempo v] a (30)
ripeti fino a quando <(tempo) = [0]> 
  attendi (1) secondi
  cambia [tempo v] di (-1)
end
invia a tutti (fine v)
```