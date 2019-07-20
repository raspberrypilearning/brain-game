## Aggiungi grafica

Al momento, lo sprite del personaggio dice solo `sì! :)` o `no :(` alle risposte del giocatore Aggiungi alcuni elementi grafici per far sapere al giocatore se la loro risposta è corretta o errata.

\--- task \---

Crea un nuovo sprite chiamato "Risultato" e dagli un costume "tick / check" e un "cross".

![Sprite con zecche e costumi incrociati](images/brain-result.png)

\--- /task \---

\--- task \---

Cambia il codice dello sprite del tuo personaggio in modo che, invece di dire qualcosa al giocatore, `trasmetta`{: class = "block3events"} i messaggi "corretto" o "sbagliato".

![Sprite personaggio](images/giga-sprite.png)

```blocks3
if <(answer) = ((number 1)*(number 2))> then

- say [si! :)] for (2) seconds
+ broadcast (corretto v)
else
- say [no :(] for (2) seconds
+ broadcast (sbagliato v)
end
```

\--- /task \---

\--- task \---

Ora è possibile utilizzare questi messaggi per mostrare `show`{: class = "block3looks"} il costume 'tic' o 'croce'. Aggiungi il seguente codice allo sprite 'Risultato':

![Risultato sprite](images/result-sprite.png)

```blocks3
    when I receive [corretto v]
    switch costume to (tick v)
    show
    wait (1) seconds
    hide

    when I receive [sbagliato v]
    switch costume to (cross v)
    show
    wait (1) seconds
    hide

    when flag clicked
    hide
```

\--- /task \---

\--- task \--- Metti alla prova il tuo gioco. Dovresti vedere il segno di spunta ogni volta che rispondi correttamente a una domanda e la croce ogni volta che rispondi in modo errato!

![Segna per corretto, croce per risposta sbagliata](images/brain-test-answer.png)

\--- /task \---

Puoi vedere che il codice per `quando ricevo corretto`{: class = "block3events"} e `quando ricevo sbagliato`{: class = "block3events"} è quasi identico?

Così puoi cambiare il tuo codice più facilmente, creerai un blocco personalizzato.

\--- task \---

Seleziona lo sprite 'Risultato'. Quindi fai clic su `I Miei Blocchi`{: class = "block3myblocks"}, quindi su **Crea un blocco**. Crea un nuovo blocco e chiamalo `animate`{: class = "block3myblocks"}.

![Risultato sprite](images/result-sprite.png)

![Crea un blocco chiamato animato](images/brain-animate-function.png)

\--- /task \---

\--- task \--- Sposta il codice per mostrare `show`{: class = "block3looks"} o nascondere `hide`{: class = "block3looks"} lo sprite 'Result' nel blocco `animate`{: class = " blocco3myblocks "}:

![Risultato sprite](images/result-sprite.png)

```blocks3
define animate
mostra
wait (1) secondi
nascondi
```

\--- /task \---

\--- task \--- Assicurati di aver rimosso i blocchi `show`{: class = "block3looks"} e `hide`{: class = "block3looks"} al di sotto di **entrambi** dei `switch costume`{: class = "block3looks"} blocchi.

Quindi aggiungere il `animato`{: classe = "block3myblocks"} blocco inferiore sia del `dell'interruttore costume`{: class = "block3looks"} blocchi. Il tuo codice dovrebbe ora apparire come questo:

![Risultato sprite](images/result-sprite.png)

```blocks3
    quando ricevo [corretto v]
    passa costume a (tick v)
    animate :: custom

    quando ricevo [errato v]
    passa costume a (cross v)
    animate :: custom
```

\--- /task \---

A causa del blocco personalizzato `animate`{: class = "block3myblocks"}, ora è sufficiente apportare una modifica al codice se si desidera mostrare i costumi dello sprite "Risultato" più o meno a lungo.

\--- task \---

Cambia il tuo codice in modo che i costumi "tick" o "cross" vengano visualizzati per 2 secondi.

\--- /task \---

\--- task \--- Invece di `mostrando`{: class = "block3looks"} e `nascondendo`{: class = "block3looks"} i costumi "tick" o "cross", puoi cambiare i `animate`Blocco {: class = "block3myblocks"} in modo che i costumi sbiadiscano.

![Risultato sprite](images/result-sprite.png)

```blocks3
    define animate
    set [ghost v] effect a (100)
    show
    repeat (25)
        cambia [ghost v] effect di (-4)
    end
    nascondi
```

\--- /task \---

Puoi migliorare l'animazione della grafica 'tick' o 'cross'? Puoi aggiungere del codice per far sparire anche i costumi, oppure puoi usare altri effetti interessanti:

![schermata](images/brain-effects.png)