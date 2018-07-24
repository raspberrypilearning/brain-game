## Grafiken hinzufügen

Anstellt, dass deine Spielfigur nur `Richtig!` oder `Leider falsch!` zum Spieler sagt, können wir jetzt Grafik hinzufügen, damit der Spieler weiß, wie es um ihn bestellt ist.

+ Erstelle eine neue Figur namens Ergebnis, die sowhol ein "Häkchen" als auch ein "Kreuz" Kostüm enthält.
    
    ![screenshot](images/brain-result.png)

+ Ändere den Code deiner Spielfigur, damit du, statt nur dem Spieler mitzuteilen, welchen Punktzahl er erreicht hat, ihm statt dessen auch die entsprechenden `richtig`{:class="blockevents"} und `falsch`{:class="blockevents"} Nachrichten senden kannst.
    
    ![screenshot](images/brain-broadcast-answer.png)

+ Du kannst jetzt diese Meldungen dazu benutzen, um entweder das "Häkchen" oder das "Kreuz" Kostüm anzuzeigen. Füge diesen Code zu deiner neuen Ergbnis Figur hinzu:
    
    ![screenshot](images/brain-show-answer.png)

+ Teste dein Spiel erneut. Du solltest jedes mal, wenn du eine Frage richtig beantwortet hast, ein Häkchen sehen oder, wenn du die Frage falsch beantwortet hast, ein Kreuz sehen!
    
    ![screenshot](images/brain-test-answer.png)

+ Have you noticed that the code for `when I receive correct`{:class="blockevents"} and `when I receive wrong`{:class="blockevents"} is nearly identical? Let's create a function to make it easier for you to make changes to your code.
    
    On your 'Result' sprite, click `More Blocks`{:class="blockmoreblocks"}, and then 'Make a Block'. Create a new function called `animate`{:class="blockmoreblocks"}.
    
    ![screenshot](images/brain-animate-function.png)

+ You can then add the animation code into your new animation function, and then just use the function twice:
    
    ![screenshot](images/brain-use-function.png)

+ Now, if you want to show the tick and the cross for a longer or shorter time, you only need to make one change to your code. Try it!

+ Instead of just showing and hiding the tick and the cross, you could change your animation function, so that the graphics fade in.
    
    ```blocks
        define [animate]
        set [ghost v] effect to (100)
        show
        repeat (25)
            change [ghost v] effect by (-4)
        end
        hide
    ```