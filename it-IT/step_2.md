## Creare le domande

Iniziamo creando domande casuali per consentire al giocatore di rispondere.

+ Avvia un nuovo progetto Scratch ed elimina lo sprite a forma di gatto in modo che il tuo progetto sia vuoto. Per creare un nuovo progetto di Scratch usando l'editor online, vai su <a href="http://jumpto.cc/scratch-new" target="_blank">jumpto.cc/scratch-new</a>.

+ Scegli un personaggio e uno sfondo per il tuo gioco. Puoi scegliere quello che ti piace! Ecco un esempio:
    
    ![screenshot](images/brain-setting.png)

+ Crea 2 nuove variabili chiamate `numero 1` {:class="blockdata"} e `numero 2` {:class="blockdata"}. Queste variabili memorizzeranno i 2 numeri che verranno moltiplicati insieme.
    
    ![screenshot](images/brain-variables.png)

+ Aggiungi del codice al tuo personaggio, per impostare entrambe le variabili su un valore `casuale` {:class="blockoperators"} un numero compreso tra 2 e 12.
    
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

+ Add a `forever`{:class="blockcontrol"} loop around this code, so that the player is asked lots of questions.

+ Create a countdown timer on the stage, using a variable called `time`{:class="blockdata"}. The 'Ghostbusters' project has instructions for making a timer (in step 5) if you need help!

+ Test your project again - you should be able to continue asking questions until the time runs out.