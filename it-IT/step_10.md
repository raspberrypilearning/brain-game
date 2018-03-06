--- challenge ---
## Sfida: Gareggia fino ai 10 punti
Puoi cambiare il gioco per far in modo che, invece di dover rispondere a più domande possibili in 30 secondi, il giocatore veda in quanto tempo riesce a rispondere a 10 domande correttamente?

Per fare ciò, dovrai solo cambiare il codice del tuo timer. Vedi cosa deve essere cambiato?

```blocks
	quando ricevo [inizio v]
	porta [tempo v] a (30)
	ripeti fino a quando <(tempo) = [0]>
  		attendi (1) secondi
  		cambia [tempo v] di (-1)
	end
	invia a tutti [fine v]
```




--- /challenge ---