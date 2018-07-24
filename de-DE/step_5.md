## Mehrfache Spiele

Lass uns einen 'start' Knopf zu deinem Spiel hinzufügen, damit du es mehrmals spielen kannst.

+ Erstelle eine neue 'start' Figur, welche der Spieler anklicken muss, um ein neues Spiel zu starten. Du kannst die Figur selber malen, oder eine Figur aus der Scratch Bibliothek berabeiten.
    
    ![screenshot](images/brain-play.png)

+ Füge diesen Code zu deinem Knopf hinzu.
    
    ```blocks
        Wenn die grüne Flagge angeklickt
    zeige dich
    
    Wenn ich angeklickt werde
    verstecke dich
    sende [start v] an alle
    ```
    
    Dieser Code zeigt deinen Start-Knopf, wenn dein Projekt gestartet wird. Wenn der Knopf angeklickt wird, wird er versteckt und sendet dann eine Nachricht, die das Spiel startet.

+ Du musst den Code deiner Spielfigur anpassen, damit das Spiel beginnt, wenn die Figur die `start`{:class="blockevents"} Startmeldung erhält, und nicht erst wenn die Flagge angeklickt wird.
    
    Replace the `when flag clicked`{:class="blockevents"} code with `when I receive start`{:class="blockevents"}.
    
    ![screenshot](images/brain-start.png)

+ Click the green flag and then click your new play button to test it. You should see that the game doesn't start until the button is clicked.

+ Did you notice that the timer starts when the green flag is clicked, and not when the game starts?
    
    ![screenshot](images/brain-timer-bug.png)
    
    Can you fix this problem?

+ Click on the stage, and replace the `stop all`{:class="blockcontrol"} block with an `end`{:class="blockevents"} message.
    
    ![screenshot](images/brain-end.png)

+ You can now add code to your button, to show it again at the end of each game.
    
    ```blocks
        when I receive [end v]
        show
    ```

+ You'll also need to stop your character asking questions at the end of each game:
    
    ```blocks
        when I receive [end v]
        stop [other scripts in sprite v]
    ```

+ Test your play button by playing a couple of games. You should notice that the play button shows after each game. To make testing easier, you can shorten each game, so that it only lasts a few seconds.
    
    ```blocks
        set [time v] to [10]
    ```

+ You can even change how the button looks when the mouse hovers over it.
    
    ```blocks
        when flag clicked
        show
        forever
        if <touching [mouse-pointer v]?> then
            set [fisheye v] effect to (30)
        else
            set [fisheye v] effect to (0)
        end
        end
    ```
    
    ![screenshot](images/brain-fisheye.png)