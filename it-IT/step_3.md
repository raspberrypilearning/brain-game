## Aggiungere un timer

--- task ---

Crea un timer per il conto alla rovescia sullo schermo con l'aiuto di una nuova variabile chiamata `tempo`{:class="block3variables"}. Il timer dovrebbe iniziare a 30 secondi e contare fino a 0 secondi.

![Sprite dello scenario](images/stage-sprite.png)

--- hints ---

--- hint ---

Crea una `variabile`{:class="block3variables"}, chiamala "tempo" e imposta il suo valore a `30`.

Quindi aggiungi il codice per portare `tempo`{:class="block3variables"} fino a 0 entro 30 secondi. Per fare ciò, sottrai `1` da `tempo`{:class="block3variables"} ogni `1` secondo, e ripeti fino a quando `tempo`{:class="block3variables"} non sarà uguale a `0`.

--- /hint ---

--- hint ---

Ecco i blocchi che ti serviranno:

```blocks3
repeat until < >

end

wait (1) seconds

change [tempo v] by (1)

(tempo)

when flag clicked

<() = ()>

set [tempo v] to [0]
```

--- /hint ---

--- hint ---

Ecco come dovrebbe apparire il risultato:

```blocks3
when flag clicked
set [tempo v] to [30]
repeat until <(tempo) = (0)>
    wait (1) seconds
    change [tempo v] by (-1)
end
```

--- /hint ---

--- /hints ---

--- /task ---

--- task ---

Creare una trasmissione `broadcast`{:class="block3control"} che invia il messaggio 'fine'. Una trasmissione `broadcast`{:class="block3control"} è come un annuncio su un altoparlante: può essere ascoltato da tutti i tuoi sprite. Aggiungere il blocco trasmissione `broadcast`{:class="block3control"} alla fine del codice timer in modo che il codice invierà e il messaggio 'fine', quando il `tempo`{:class="block3variables"} avrà raggiunto il valore `0`.

![Sprite dello scenario](images/stage-sprite.png)

```blocks3
    broadcast (fine v)
```

--- /task ---

--- task ---

Seleziona il tuo sprite personaggio e aggiungi del codice in modo che lo sprite `fermi gli altri script`{:class="block3control"} quando riceve il messaggio `fine`{:class="block3control"}.

![Giga sprite](images/giga-sprite.png)

```blocks3
    when I receive [fine v]
    stop [other scripts in sprite v]
```

--- /task ---

--- task ---

Prova di nuovo il tuo gioco. Dovrebbe continuare a fare domande fino a quando il timer non sarà arrivato a 0.

--- /task ---