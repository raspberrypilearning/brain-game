## Giochi multipli

Ora aggiungerai un pulsante "Gioca", in modo che il giocatore possa giocare molte volte.

--- task ---

Crea un nuovo pulsante "Gioca" su cui il giocatore deve fare clic per iniziare una nuova partita.

Puoi disegnare tu stesso lo sprite o modificare uno sprite dalla libreria.

![Immagine del pulsante gioca](images/brain-play.png)

--- /task ---

--- task ---

Aggiungi questo codice allo sprite del tuo pulsante:

![Sprite pulsante](images/button-sprite.png)

```blocks3
    when flag clicked
    show

    when this sprite clicked
    hide
    broadcast (start v)
```

--- /task ---

Il nuovo codice include un altro blocco `broadcast`{:class="block3events"}, che invia il messaggio 'inizio'.

Il nuovo codice fa apparire lo sprite del pulsante 'Gioca' quando il giocatore fa clic sulla bandiera. Quando il giocatore fa clic sul pulsante sprite, lo sprite sparisce e trasmette un messaggio a cui altri sprite possono reagire.

Al momento, lo sprite del personaggio inizia a fare domande quando il giocatore fa clic sulla bandiera. Cambia il codice del tuo gioco in modo che lo sprite personaggio inizi a fare domande quando riceve il messaggio 'start' `broadcast`{:class="block3events"}.

--- task ---

Seleziona il tuo sprite del personaggio e, nella sua sezione di codice, sostituisci il blocco `quando si clicca sulla bandiera`{:class="block3events"} blocca con un blocco `quando ricevo start`{:class="block3events"}.

![Sprite personaggio](images/giga-sprite.png)

```blocks3
<br />- when flag clicked
+ when I receive [inizio v]
set [numero 1 v] to (pick random (2) to (12))
set [numero 2 v] to (pick random (2) to (12))
ask (join (numero 1)(join [ x ] (numero 2))) and wait
if <(answer) = ((numero 1)*(numero 2))> then
    say [si! :)] for (2) seconds
else
    say [nope :(] for (2) seconds
end
```

--- /task ---

--- task ---

Fai clic sulla bandiera verde, quindi fai clic sul nuovo pulsante "Gioca" per verificare se funziona. Dovresti vedere che il gioco non parte prima di aver fatto clic sul pulsante.

--- /task ---

Riesci a vedere che il timer inizia quando viene cliccata la bandiera verde, invece che quando il gioco inizia?

![Il timer è partito](images/brain-timer-bug.png)

--- task ---

Riesci a modificare il codice del timer in modo che il timer inizi quando il giocatore clicca sul pulsante?

--- /task ---

--- task ---

Aggiungi del codice al tuo pulsante in modo che il pulsante venga mostrato nuovamente alla fine di ogni gioco.

![Sprite pulsante](images/button-sprite.png)

```blocks3
    when I receive [fine v]
    show
```

--- /task ---

--- task ---

Prova il pulsante "Gioca" giocando un paio di giochi. Il pulsante dovrebbe apparire alla fine di ogni partita.

Per testare il gioco più velocemente, puoi cambiare il valore di `tempo`{:class="block3variables"} in modo che ogni gioco duri solo pochi secondi.

![Stage](images/stage-sprite.png)

```blocks3
    set [tempo v] to [10]
```

--- /task ---

--- task ---

Puoi anche modificare l'aspetto del pulsante di gioco quando il mouse passa ci passa sopra.

![Pulsante](images/button-sprite.png)

```blocks3
    when flag clicked
    show
    forever
    if <touching (mouse-pointer v)?> then
        set [fisheye v] effect to (30)
    else
        set [fisheye v] effect to (0)
    end
    end
```

![schermata](images/brain-fisheye.png)

--- /task ---