## Creare domande

Inizierai creando domande casuali a cui il giocatore deve rispondere.

\--- task \---

Inizia un nuovo progetto Scratch.

**Online:** apri un nuovo progetto Scratch online su [rpf.io/scratch-new](http://rpf.io/scratchon){:target="_blank"}.

**Offline:** apri un nuovo progetto nell'editor offline.

Se hai bisogno di scaricare ed installare l'editor Scratch offline, puoi trovarlo su [rpf.io/scratchoff](http://rpf.io/scratchoff){:target="_blank"}.

\--- /task \---

\--- task \--- Aggiungi uno sprite personaggio e uno sfondo per il tuo gioco. Puoi scegliere quello che ti piace! Ecco un esempio:

![schermata](images/brain-setting.png)

\--- /task \---

\--- task \--- Assicurati di avere selezionato il tuo sprite del personaggio. Crea due nuove variabili, chiamate `numero 1`{: class = "block3variables"} e `numero 2`{: class = "block3variables"}, per memorizzare i numeri per le domande del quiz.

![screenshot](images/giga-sprite.png) ![schermata](images/brain-variables.png)

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- \--- compito aggiungere il codice per il tuo sprite personaggio per impostare entrambe le `variabili`{: class = "block3variables"} ad un `casuale`{: class = "block3operators"} numero compreso tra 2 e 12.

![schermata](images/giga-sprite.png)

```blocks3
quando il flag ha fatto clic su
impostare [numero 1 v] su (selezionare casuale (2) a (12))
impostare [numero 2 v] su (selezionare casuale (2) a (12))
```

\--- /task \---

\--- task \--- Aggiungi il codice a `ask`{: class = "block3sensing"} il giocatore per la risposta, e poi `dirai per 2 secondi`{: class = "block3looks"} se la risposta era giusta o sbagliato:

![schermata](images/giga-sprite.png)

```blocks3
quando il flag ha cliccato
impostato [numero 1 v] su (selezionare casuale (2) a (12))
impostare [numero 2 v] a (selezionare casuale (2) a (12))

+ chiedere (partecipare (numero 1) (unirsi a [x] (numero 2))) e attendere
+ se <(risposta) = ((numero 1) * (numero 2))> poi
+ dire [sì! :)] per (2) secondi
+ altro
+ dire [no :(] per (2) secondi
+ fine
```

\--- /task \---

\--- task \---

Metti alla prova il tuo progetto due volte: rispondi correttamente a una domanda e l'altra in modo errato.

\--- /task \---

\--- task \---

Aggiungi un `per sempre`{: class = "block3control"} aggira questo codice, in modo che il gioco chieda al giocatore molte domande di seguito.

\--- suggerimenti \--- \--- suggerimento \---

È necessario aggiungere un `per sempre`{: class = "block3control"} blocco, e mettere tutto il codice, tranne il `quando il flag cliccato`{: class = "block3control"} blocco in esso.

\--- / suggerimento \--- \--- suggerimento \--- Ecco il blocco di cui hai bisogno:

```blocks3
per sempre
fine
```

\--- / suggerimento \--- \--- suggerimento \--- Ecco come dovrebbe apparire il tuo codice:

```blocks3
quando il flag ha fatto clic su

+ per sempre
    set [numero 1 v] su (selezionare casuale (2) a (12))
    impostare [numero 2 v] su (selezionare casuale (2) a (12))
    chiedere (partecipare (numero 1) (unire [x] (numero 2))) e attendere
    se <(risposta) = ((numero 1) * (numero 2))> poi
        dire [sì! :)] per (2) secondi
    altro
        dire [no :(] per (2) secondi
    fine
fine
```

\--- /hint \--- \--- /hints \---

\--- /task \---