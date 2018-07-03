## Erzeugen von Aufgaben

Beginne damit zufällige Fragen zu generieren, die der Spieler beantworten soll.

+ Starte mit einem neuen Scratch-Projekt und lösche die Spielfigur 'Katze". Dein Projekt ist nun leer. Du findest den Online-Editor für Scratch unter <a href="http://jumpto.cc/scratch-new" target="_blank">jumpto.cc/scratch-new</a>.

+ Wähle eine Spielfigur und einen passenden Bühnenhintergrund für dein Spiel. Entscheide selbst, wie dein Spiel aussehen soll! Hier ein Beispiel:
    
    ![screenshot](images/brain-setting.png)

+ Erstelle 2 neue Variablen mit den Namen `Zahl 1`{:class="blockdata"} und `Zahl 2`{:class="blockdata"}. Diese beiden Variablen speichern die beiden Zahlen, die miteinander multipliziert werden sollen.
    
    ![screenshot](images/brain-variables.png)

+ Füge deiner Spielfigur Programmcode hinzu, damit beide Variablen per Zufall eine Zahl zwischen 2 und 12 zugewiesen bekommen `random`{:class="blockoperators"}.
    
    ```blocks
        wenn Fahne angeklickt
    setze [Zahl 1 v] auf (Zufallszahl von (2) bis (12))
    setze [Zahl 2 v] auf (Zufallszahl von (2) bis (12))
    ```

+ Du kannst nun deinen Spieler nach der Antwort fragen und ihn wissen lassen. ob diese falsch oder richtig ist.
    
    ```blocks
        when flag clicked
        set [number 1 v] to (pick random (2) to (12))
        set [number 2 v] to (pick random (2) to (12))
        ask (join (number 1)(join [ x ] (number 2))) and wait
        if <(answer) = ((number 1)*(number 2))> then
            say [yes! :)] for (2) secs
        else
            say [nope :(] for (2) secs
        end
    ```

+ Test your project fully, by answering one question correctly and one with the wrong answer.

+ Add a `forever`{:class="blockcontrol"} loop around this code, so that the player is asked lots of questions.

+ Create a countdown timer on the stage, using a variable called `time`{:class="blockdata"}. The 'Ghostbusters' project has instructions for making a timer (in step 5) if you need help!

+ Test your project again - you should be able to continue asking questions until the time runs out.