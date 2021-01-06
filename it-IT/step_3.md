## Aggiungere un timer

\--- task \---

Crea un timer per il conto alla rovescia sullo schermo con l'aiuto di una nuova variabile chiamata `secondi`{:class="block3variables"}. Il timer dovrebbe iniziare a 30 secondi e contare fino a 0 secondi.

![Sprite dello scenario](images/stage-sprite.png)

\--- hints \---

\--- hint \---

Crea una `variabile`{:class = "block3variables"}, chiamala "secondi" e imposta il suo valore a `30`.

Quindi aggiungi il codice per portare `secondi`{:class = "block3variables"} fino a 0 entro 30 secondi. Per fare ciò, sottrai `1` da `secondi`{:class = "block3variables"} ogni `1` secondo, e ripeti fino a quando `secondi`{:class = "block3variables"} non sarà uguale a `0`.

\--- /hint \---

\--- hint \---

Ecco i blocchi che ti serviranno:

```blocks3
repeat until < >

end

wait (1) seconds

change [secondi v] by (1)

(secondi)

when flag clicked

<() = ()>

set [secondi v] to [0]
```

\--- /hint \---

\--- hint \---

Ecco come dovrebbe apparire il risultato:

```blocks3
when flag clicked
set [secondi v] to [30]
repeat until <(secondi) = (0)>
    wait (1) seconds
    change [secondi v] by (-1)
end
```

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

Creare una trasmissione `broadcast`{:class = "block3control"} che invii il messaggio 'fine'. Una trasmissione `broadcast`{:class = "block3control"} è come un annuncio su un altoparlante: può essere ascoltato da tutti i tuoi sprite. Add the `broadcast`{:class="block3control"} block to the end of the timer code so that the code will send an 'end' message when the `time`{:class="block3variables"} has counted down to `0`.

![Sprite dello scenario](images/stage-sprite.png)

```blocks3
    broadcast (fine v)
```

\--- /task \---

\--- task \---

Seleziona il tuo sprite personaggio e aggiungi del codice in modo che lo sprite `fermi gli altri script`{:class = "block3control"} quando riceve il messaggio `fine`{:class = "block3control"}.

![Giga sprite](images/giga-sprite.png)

```blocks3
    when I receive [fine v]
    stop [other scripts in sprite v]
```

\--- /task \---

\--- task \---

Prova di nuovo il tuo gioco. Dovrebbe continuare a fare domande fino a quando il timer non sarà arrivato a 0.

\--- /task \---