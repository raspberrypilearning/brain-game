## Aggiungi grafica

Al momento, lo sprite del personaggio dice solo `sì! :)` o `no :(` alle risposte del giocatore Aggiungi alcuni elementi grafici per far sapere al giocatore se la loro risposta è corretta o errata.

--- task ---

Crea un nuovo sprite chiamato "Risultato" e dagli un costume "spunta" e un "croce".

![Sprite con costumi spunta e croce](images/brain-result.png)

--- /task ---

--- task ---

Cambia il codice dello sprite del tuo personaggio in modo che, invece di dire qualcosa al giocatore, `trasmetta`{:class = "block3events"} i messaggi "corretto" o "sbagliato".

![Sprite personaggio](images/giga-sprite.png)

```blocks3
if <(answer) = ((numero 1)*(numero 2))> then

- say [si! :)] for (2) seconds
+ broadcast (correttov)
else
- say [no :(] for (2) seconds
+ broadcast (sbagliato v)
end
```

--- /task ---

--- task ---

Ora è possibile utilizzare questi messaggi per `mostrare`{:class="block3looks"} il costume 'spunta' o 'croce'. Aggiungi il seguente codice allo sprite 'Risultato':

![Risultato sprite](images/result-sprite.png)

```blocks3
    when I receive [corretto v]
    switch costume to (spunta v)
    show
    wait (1) seconds
    hide

    when I receive [sbagliato v]
    switch costume to (croce v)
    show
    wait (1) seconds
    hide

    when flag clicked
    hide
```

--- /task ---

--- task ---

Prova di nuovo il tuo gioco. Dovresti vedere la spunta ogni volta che rispondi correttamente a una domanda, e la croce ogni volta che rispondi scorrettamente!

![Spunta per corretto, croce per risposta sbagliata](images/brain-test-answer.png)

--- /task ---

Puoi vedere che il codice per `quando ricevo corretto`{:class="block3events"} e `quando ricevo sbagliato`{:class="block3events"} è quasi identico?

Al fine di modificare il tuo codice più facilmente, creerai un blocco personalizzato.

--- task ---

Seleziona lo sprite "Risultato". Quindi fai clic su `I Miei Blocchi`{:class="block3myblocks"}, quindi su **Crea un blocco**. Crea un nuovo blocco e chiamalo `anima`{:class="block3myblocks"}.

![Sprite risultato](images/result-sprite.png)

![Crea un blocco chiamato anima](images/brain-animate-function.png)

--- /task ---

--- task ---

Sposta il codice per `mostrare`{:class="block3looks"} o `nascondere`{:class="block3looks"} lo sprite 'Result' nel blocco `anima`{:class=" blocco3myblocks"}:

![Sprite risultato](images/result-sprite.png)

```blocks3
define animate
show
wait (1) seconds
hide
```

--- /task ---

--- task ---

Assicurati di aver rimosso i blocchi `mostra`{:class="block3looks"} e `nascondi`{:class="block3looks"} al di sotto di **entrambi** i blocchi `cambia costume`{:class="block3looks"}.

Quindi aggiungere il blocco `anima`{:class="block3myblocks"} sotto entrambi i blocchi `cambia costume`{:class="block3looks"}. Il tuo codice dovrebbe ora apparire come questo:

![Sprite risultato](images/result-sprite.png)

```blocks3
    when I receive [corretto v]
    switch costume to (spunta v)
    anima:: custom

    when I receive [sbagliato v]
    switch costume to (croce v)
    anima:: custom
```

--- /task ---

Gazie al blocco personalizzato `anima`{:class="block3myblocks"}, ora è sufficiente apportare una modifica al codice se si desidera mostrare i costumi dello sprite "Risultato" più o meno a lungo.

--- task ---

Cambia il codice in modo che i costumi 'spunta' o 'croce' per 2 secondi.

--- /task ---

--- task ---

Invece di `mostrare`{:class="block3looks"} e `nascondere`{:class="block3looks"} i costumi "spunta" o "croce", puoi cambiare `anima`{:class="block3myblocks"} in modo che i costumi sbiadiscano.

![Sprite risultato](images/result-sprite.png)

```blocks3
    define animate
    set [ghost v] effect to (100)
    show
    repeat (25)
        change [ghost v] effect by (-4)
    end
    hide
```

--- /task ---

Puoi migliorare l'animazione della grafica 'spunta' o 'croce'? Puoi aggiungere del codice per far svanire anche i costumi, oppure potresti usare altri effetti interessanti:

![schermata](images/brain-effects.png)