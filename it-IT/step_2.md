## Creare domande

Inizierai creando domande casuali a cui il giocatore deve rispondere.

\--- task \---

Inizia un nuovo progetto Scratch.

**Online:** apri un nuovo progetto Scratch online su [rpf.io/scratch-new](http://rpf.io/scratchon){:target="_blank"}.

**Offline:** apri un nuovo progetto nell'editor offline.

Se hai bisogno di scaricare ed installare l'editor Scratch offline, puoi trovarlo su [rpf.io/scratchoff](http://rpf.io/scratchoff){:target="_blank"}.

\--- /task \---

\--- task \--- Aggiungi uno personaggio sprite e uno sfondo per il tuo gioco. Puoi scegliere quello che ti piace! Ecco un esempio:

![schermata](images/brain-setting.png)

\--- /task \---

\--- task \--- Assicurati di avere selezionato il tuo sprite del personaggio. Crea due nuove variabili, chiamate `numero 1`{: class = "block3variables"} e `numero 2`{: class = "block3variables"}, per memorizzare i numeri per le domande del quiz.

![screenshot](images/giga-sprite.png) ![schermata](images/brain-variables.png)

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- task \--- Aggiungi il codice per il tuo sprite personaggio per impostare entrambe le `variabili`{: class = "block3variables"} ad un numero `random`{: class = "block3operators"} compreso tra 2 e 12.

![schermata](images/giga-sprite.png)

```blocks3
when flag clicked
set [numero 1 v] to (pick random (2) to (12))
set [numero 2 v] to (pick random (2) to (12))
```

\--- /task \---

\--- task \--- Aggiungi il codice a `ask`{: class = "block3sensing"} per chiedere al giocatore la risposta, e poi dirai per 2 secondi `say for 2 seconds`{: class = "block3looks"} se la risposta era giusta o sbagliato:

![schermata](images/giga-sprite.png)

```blocks3
when flag clicked
set [numero 1 v] to (pick random (2) to (12))
set [numero 2 v] to (pick random (2) to (12))

+ ask (join (numero 1)(join [ x ] (numero 2))) and wait
+ if <(answer) = ((numero 1)*(numero 2))> then
+ say [si! :)] for (2) seconds
+ else
+ say [no :(] for (2) seconds
+ end
```

\--- /task \---

\--- task \---

Metti alla prova il tuo progetto due volte: rispondi correttamente a una domanda e l'altra in modo errato.

\--- /task \---

\--- task \---

Aggiungi un `forever`{: class = "block3control"} attorno a questo codice, in modo che il gioco chieda al giocatore molte domande di seguito.

\--- hints \--- \--- hint \---

È necessario aggiungere un blocco `forever`{: class = "block3control"}, e mettere tutto il codice, tranne al blocco `when flag clicked`{: class = "block3control"}.

\--- /hint \--- \--- hint \--- Ecco il blocco di cui hai bisogno:

```blocks3
forever
end
```

\--- /hint \--- \--- hint \--- Ecco come dovrebbe apparire il tuo codice:

```blocks3
when flag clicked

+ forever
    set [numero 1 v] to (pick random (2) to (12))
    set [numero 2 v] to (pick random (2) to (12))
    ask (join (numero 1)(join [ x ] (numero 2))) and wait
    if <(answer) = ((numero 1)*(numero 2))> then
        say [si! :)] for (2) seconds
    else
        say [no :(] for (2) seconds
    end
end
```

\--- /hint \--- \--- /hints \---

\--- /task \---