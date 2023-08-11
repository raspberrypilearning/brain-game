## Creare domande

Inizierai creando domande casuali a cui il giocatore deve rispondere.

\--- task \---

Apri un nuovo progetto Scratch.

**Online:** open a new online Scratch project at [rpf.io/scratch-new](https://rpf.io/scratch-new){:target="_blank"}.

**Offline:** apri un nuovo progetto nell'editor offline.

If you need to download and install the Scratch offline editor, you can find it at [rpf.io/scratchoff](https://rpf.io/scratchoff){:target="_blank"}.

\--- /task \---

\--- task \---

Scegli un personaggio e uno sfondo per il tuo gioco. Puoi scegliere quello che più ti piace! Ecco un esempio:

![schermata](images/brain-setting.png)

\--- /task \---

\--- task \---

Assicurati di aver selezionato lo sprite del personaggio. Crea due nuove variabili chiamate `numero 1`{:class="block3variables"} e `numero 2`{:class="block3variables"} per memorizzare i numeri per le domande del quiz.

![schermata](images/giga-sprite.png)

![schermata](images/brain-variables.png)

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- task \---

Aggiungi del codice al tuo personaggio in modo da impostare entrambe le `variabili`{:class="block3variables"} su un valore `a caso`{:class="block3operators"} compreso tra 2 e 12.

![schermata](images/giga-sprite.png)

```blocks3
when flag clicked
set [numero 1 v] to (pick random (2) to (12))
set [numero 2 v] to (pick random (2) to (12))
```

\--- /task \---

\--- task \---

Aggiungi il codice a `chiedi`{:class = "block3sensing"} per creare la domanda da fare al giocatore, e poi `dire per 2 secondi`{:class="block3looks"} se la risposta era giusta o sbagliata:

![schermata](images/giga-sprite.png)

```blocks3
when flag clicked
set [numero 1 v] to (pick random (2) to (12))
set [numero 2 v] to (pick random (2) to (12))

+ + ask (join (numero 1)(join [ x ] (numero 2))) and wait
+ if <(answer) = ((numero 1) * (numero 2))> then 
 + say [si! :)] for (2) seconds
+ else
+ say [no :(] for (2) seconds
+ end
```

\--- /task \---

\--- task \---

Prova il tuo progetto due volte: rispondi correttamente a una domanda e in modo errato all'altra.

\--- /task \---

\--- task \---

Aggiungi un ciclo `per sempre`{:class="block3control"} attorno a questo codice, in modo che il gioco faccia al giocatore molte domande di seguito.

\--- hints \---

\--- hint \---

È necessario aggiungere un blocco `per sempre`{:class = "block3control"}, e mettere tutto il codice, tranne al blocco `quando si clicca su bandiera`{:class = "block3control"}.

\--- /hint \---

\--- hint \---

Ecco il blocco che ti serve:

```blocks3
forever
end
```

\--- /hint \---

\--- hint \---

Ecco come dovrebbe apparire il risultato:

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

\--- /hint \---

\--- /hints \---

\--- /task \---