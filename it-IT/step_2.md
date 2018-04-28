## Creare le domande

Iniziamo creando domande casuali a cui il giocatore deve rispondere.

+ Avvia un nuovo progetto Scratch ed elimina lo sprite a forma di gatto in modo che il tuo progetto sia vuoto. Per creare un nuovo progetto di Scratch usando l'editor online, vai su <a href="http://jumpto.cc/scratch-new" target="_blank">jumpto.cc/scratch-new</a>.

+ Scegli un personaggio e uno sfondo per il tuo gioco. Puoi scegliere quello che più ti piace! Ecco un esempio:
    
    ![screenshot](images/brain-setting.png)

+ Crea 2 nuove variabili chiamate `numero 1`{:class="blockdata"} e `numero 2`{:class="blockdata"}. Queste variabili memorizzeranno i 2 numeri che verranno moltiplicati tra loro.
    
    ![screenshot](images/brain-variables.png)

+ Aggiungi del codice al tuo personaggio in modo da impostare entrambe le variabili su un valore `a caso`{:class="blockoperators"} compreso tra 2 e 12.
    
    ```blocks
    when flag clicked
    set [numero 1 v] to (pick casuale (2) to (12))
    set [numero 2 v] to (pick casuale (2) to (12))
```

+ Puoi quindi chiedere al giocatore la risposta e far sapere loro se avevano ragione o torto.
    
    ```blocks
    when flag clicked
    set [numero 1 v] to (pick casuale (2) to (12))
    set [numero 2 v] to (pick casuale (2) to (12))
    ask (join (numero 1)(join [ x ] (numero 2))) and wait
    if <(answer) = ((numero 1)*(numero 2))> then
        say [si! :)] for (2) secs
    else
        say [no :(] for (2) secs
    end
```

+ Metti alla prova il tuo progetto completamente, rispondendo a una domanda correttamente e ad un'altra con la risposta sbagliata.

+ Aggiungi un ciclo continuo `per sempre` {:class="blockcontrol"}, in modo che al giocatore vengano poste molte domande.

+ Crea un timer per il conto alla rovescia sullo stage, usando una variabile chiamata `tempo` {:class="blockdata"}. Se hai bisogno di aiuto, il progetto 'Ghostbusters' contiene istruzioni per fare un timer (nel passaggio 5)!

+ Metti alla prova di nuovo il tuo progetto - dovresti essere in grado di continuare a porre domande fino al termine del tempo.