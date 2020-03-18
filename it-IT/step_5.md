## Giochi multipli

Ora aggiungerai un pulsante "Gioca", in modo che il giocatore possa giocare molte volte.

\--- task \---

Crea un nuovo pulsante "Gioca" su cui il giocatore deve fare clic per iniziare una nuova partita.

Puoi disegnare tu stesso lo sprite o modificare uno sprite dalla libreria.

![Immagine del pulsante gioca](images/brain-play.png)

\--- /task \---

\--- task \---

Aggiungi questo codice allo sprite del tuo pulsante:

![Sprite pulsante](images/button-sprite.png)

```blocks3
    quando si clicca sulla bandiera verde
mostra

quando si clicca questo sprite
nascondi
invia a tutti (inizio v)
```

\--- /task \---

Il nuovo codice include un altro blocco `broadcast`{:class="block3events"}, che invia il messaggio 'inizio'.

Il nuovo codice fa apparire lo sprite del pulsante 'Gioca' quando il giocatore fa clic sulla bandiera. Quando il giocatore fa clic sul pulsante sprite, lo sprite sparisce e trasmette un messaggio a cui altri sprite possono reagire.

Al momento, lo sprite del personaggio inizia a fare domande quando il giocatore fa clic sulla bandiera. Cambia il codice del tuo gioco in modo che lo sprite personaggio inizi a fare domande quando riceve il messaggio 'start' `broadcast`{:class="block3events"}.

\--- task \---

Seleziona il tuo sprite del personaggio e, nella sua sezione di codice, sostituisci il blocco `quando si clicca sulla bandiera`{:class = "block3events"} blocca con un blocco `quando ricevo start`{:class = "block3events"}.

![Sprite personaggio](images/giga-sprite.png)

```blocks3
<br />-  quando si clicca sulla bandiera verde
+ quando ricevo [inizio v]
porta [numero 1 v] a (numero a caso tra (2) e (12))
porta [numero 2 v] a (numero a caso tra (2) e (12))
chiedi (unione di (numero 1) e (unione di [ x ] e (numero 2))) e attendi
se <(risposta) = ((numero 1) * (numero 2))> allora 
  dire [si! :)] per (2) secondi
altrimenti 
  dire [no :(] per (2) secondi
```

\--- /task \---

\--- task \---

Fai clic sulla bandiera verde, quindi fai clic sul nuovo pulsante "Gioca" per verificare se funziona. Dovresti vedere che il gioco non parte prima di aver fatto clic sul pulsante.

\--- /task \---

Riesci a vedere che il timer inizia quando viene cliccata la bandiera verde, invece che quando il gioco inizia?

![Il timer è partito](images/brain-timer-bug.png)

\--- task \---

Riesci a modificare il codice del timer in modo che il timer inizi quando il giocatore clicca sul pulsante?

\--- /task \---

\--- task \---

Aggiungi del codice al tuo pulsante in modo che il pulsante venga mostrato nuovamente alla fine di ogni gioco.

![Sprite pulsante](images/button-sprite.png)

```blocks3
    quando ricevo [fine v]
mostra
```

\--- /task \---

\--- task \---

Prova il pulsante "Gioca" giocando un paio di giochi. Il pulsante dovrebbe apparire alla fine di ogni partita.

Per testare il gioco più velocemente, puoi cambiare il valore di `tempo`{:class="block3variables"} in modo che ogni gioco duri solo pochi secondi.

![Stage](images/stage-sprite.png)

```blocks3
    set [tempo v] to [10]
```

\--- /task \---

\--- task \---

Puoi anche modificare l'aspetto del pulsante di gioco quando il mouse passa ci passa sopra.

![Pulsante](images/button-sprite.png)

```blocks3
    quando si clicca sulla bandiera verde
mostra
per sempre 
  se <0> allora 
    porta effetto [fisheye v] a (30)
  altrimenti 
    porta effetto [fisheye v] a (0)
  end
end
```

![schermata](images/brain-fisheye.png)

\--- /task \---