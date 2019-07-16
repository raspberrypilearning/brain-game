## Sfida: Cambia costumi

\--- task \--- Crea un timer per il conto alla rovescia sullo stage con l'aiuto di una nuova variabile chiamata `volta`{: class = "block3variables"}. Il timer dovrebbe iniziare a 30 secondi e contare fino a 0 secondi.

![Stage sprite](images/stage-sprite.png)

\--- suggerimenti \--- \--- suggerimento \---

Crea una variabile ``{: class = "block3variables"}, chiamala "time" e imposta il suo valore su `30`.

Quindi aggiungi il codice per contare `volte`{: class = "block3variables"} fino a 0 entro 30 secondi. Per fare ciò, sottrai `1` da `time`{: class = "block3variables"} ogni `1` secondi, e ripeti questo fino a `volte`{: class = "block3variables"} uguale a `0`.

\--- / suggerimento \--- \--- suggerimento \--- Ecco i blocchi necessari:

```blocks3
ripetere fino a < >

fine

attendere (1) secondi

cambiare [tempo v] di (1)

(tempo)

quando si fa clic con il flag

<() = ()>

impostare [tempo v] su [0]
```

\--- / suggerimento \--- \--- suggerimento \--- Ecco come dovrebbe apparire il tuo nuovo codice:

```blocks3
quando il flag ha fatto clic su
impostare [tempo v] su [30]
ripetere fino a <(tempo) = (0)>
    attendere (1) secondi
    cambiare [tempo v] di (-1)
fine
```

\--- /hint \--- \--- /hints \---

\--- /task \---

\--- task \---

Creare un `trasmissione`{: class = "block3control"} che invia il messaggio 'fine'. A `trasmissione`{: class = "block3control"} è come un annuncio su un altoparlante: può essere ascoltato da tutti i tuoi sprite. Aggiungere il `trasmissione`{: class = "block3control"} bloccare alla fine del codice timer in modo che il codice invierà e il messaggio 'fine', quando il `tempo di`{: class = "block3variables"} ha contato fino a `0`.

![Stage sprite](images/stage-sprite.png)

```blocks3
    trasmissione (fine v)
```

\--- /task \---

\--- task \--- Seleziona il tuo sprite personaggio e aggiungi del codice in modo che lo sprite `fermi gli altri script`{: class = "block3control"} quando riceve il messaggio `end`{: class = "block3control"} .

![Giga sprite](images/giga-sprite.png)

```blocks3
    quando ricevo [fine]
       stop [altri script negli sprite]
```

\--- /task \---

\--- task \---

Metti alla prova il tuo gioco. Dovrebbe continuare a fare domande finché il timer non ha contato fino a 0.

\--- /task \---