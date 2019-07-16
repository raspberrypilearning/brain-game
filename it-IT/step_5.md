## Giochi multipli

Ora aggiungerai un pulsante "Gioca", in modo che il giocatore possa giocare molte volte.

\--- task \--- Crea un nuovo sprite pulsante 'Gioca' che il giocatore deve cliccare per iniziare una nuova partita.

Puoi disegnare lo sprite da solo o modificare uno sprite dalla libreria.

![Immagine del pulsante di riproduzione](images/brain-play.png)

\--- /task \---

\--- task \--- Aggiungi questo codice al tuo sprite pulsante:

![Sprite pulsante](images/button-sprite.png)

```blocks3
    quando il flag ha fatto clic su
    mostra

    quando questo sprite ha fatto clic su
    nascondi
    broadcast (avvia v)
```

\--- /task \---

Il nuovo codice include un altro blocco `broadcast`{: class = "block3events"}, che invia il messaggio 'start'.

Il nuovo codice fa apparire lo sprite del pulsante "Gioca" quando il giocatore fa clic sulla bandiera. Quando il giocatore fa clic sul pulsante sprite, lo sprite nasconde e trasmette un messaggio a cui altri sprite possono reagire.

Al momento, lo sprite del personaggio inizia a fare domande quando il giocatore fa clic sulla bandiera. Cambia il codice del gioco in modo che lo sprite del personaggio inizi a porre domande quando riceve la trasmissione "start" `broadcast`{: class = "block3events"}.

\--- task \--- Seleziona il tuo sprite del personaggio e, nella sua sezione di codice, sostituisci il `quando il flag ha cliccato`{: class = "block3events"} blocca con un `quando ricevo start`{: class = "block3events" } blocco.

![Sprite personaggio](images/giga-sprite.png)

```blocks3
<br />- quando il flag ha fatto clic su
+ quando ricevo [start v]
set [numero 1 v] a (scegli casuale (2) a (12))
set [numero 2 v] a (scegli casuale (2) a (12) )
ask (join (numero 1) (join [x] (numero 2))) e attendere
se &lt;(answer) = ((numero 1) * (numero 2))&gt; quindi
    dire [sì! :)] per (2) secondi
altro
    dire [nope :(] per (2) secondi
fine
```

\--- /task \---

\--- task \---

Fare clic sulla bandiera verde, quindi fare clic sul nuovo pulsante "Riproduci" per verificare se funziona. Dovresti vedere che il gioco non parte prima di aver fatto clic sul pulsante.

\--- /task \---

Riesci a vedere che il timer inizia quando viene cliccata la bandiera verde, invece di quando inizia il gioco?

![Il timer è iniziato](images/brain-timer-bug.png)

\--- task \---

È possibile modificare il codice per il timer in modo che il timer inizi quando il lettore fa clic sul pulsante?

\--- /task \---

\--- task \--- Aggiungi codice al tuo sprite pulsante in modo che il pulsante si mostri di nuovo alla fine di ogni partita.

![Sprite pulsante](images/button-sprite.png)

```blocks3
    quando ricevo [fine]
       mostra
```

\--- /task \---

\--- task \---

Prova il pulsante "Gioca" giocando un paio di giochi. Il pulsante dovrebbe mostrare alla fine di ogni partita.

Per testare il gioco più velocemente, puoi cambiare il valore di `volte`{: class = "block3variables"} in modo che ogni gioco abbia solo pochi secondi.

![Palcoscenico](images/stage-sprite.png)

```blocks3
    porta [tempo] a [10]
```

\--- /task \---

\--- task \--- È possibile modificare l'aspetto del pulsante quando il puntatore del mouse passa sopra di esso.

![Pulsante](images/button-sprite.png)

```blocks3
    quando si clicca su ⚑
      mostra
      per sempre
      se <touching (mouse-pointer v)?> allora
        porta [effetto fisheye] a (30)
      altro
        porta [effetto fisheye] a (0)
      fine
    fine
```

![schermata](images/brain-fisheye.png) \--- /task \---