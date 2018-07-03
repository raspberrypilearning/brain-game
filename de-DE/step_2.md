## Erzeugen von Aufgaben

Beginne damit zufällige Fragen zu generieren, die der Spieler beantworten soll.

+ Starte mit einem neuen Scratch-Projekt und lösche die Spielfigur 'Katze". Dein Projekt ist nun leer. Du findest den Online-Editor für Scratch unter <a href="http://jumpto.cc/scratch-new" target="_blank">jumpto.cc/scratch-new</a>.

+ Wähle eine Spielfigur und einen passenden Bühnenhintergrund für dein Spiel. Entscheide selbst, wie dein Spiel aussehen soll! Hier ein Beispiel:
    
    ![Screenshot](images/brain-setting.png)

+ Erstelle 2 neue Variablen mit den Namen `Zahl 1`{:class="blockdata"} und `Zahl 2`{:class="blockdata"}. Diese beiden Variablen speichern die beiden Zahlen, die miteinander multipliziert werden sollen.
    
    ![Screenshot](images/brain-variables.png)

+ Füge deiner Spielfigur Programmcode hinzu, damit beide Variablen per Zufall eine Zahl zwischen 2 und 12 zugewiesen bekommen `random`{:class="blockoperators"}.
    
    ```blocks
        wenn Fahne angeklickt
    setze [Zahl 1 v] auf (Zufallszahl von (2) bis (12))
    setze [Zahl 2 v] auf (Zufallszahl von (2) bis (12))
    ```

+ Du kannst nun deinen Spieler nach der Antwort fragen und ihn wissen lassen. ob diese falsch oder richtig ist.
    
    ```blocks
        wenn Fahne angeklickt
    setze [Zahl 1 v] auf (Zufallszahl von (2) bis (12))
    setze [Zahl 2 v] auf (Zufallszahl von (2) bis (12))
    frage (verbinde (Zahl 1)(verbinde [x] (number 2))) und warte
    falls <(Antwort) = ((Zahl 1)*(Zahl 2))> dann
    sage [Richtig! :) für (2) Sek.
    sonst
    sage [Falsch! :(] für (2) Sek.
    end
    ```

+ Teste dein Projekt vollständig, indem du einmal die richtige und einmal die falsche Lösung eingibst.

+ Füge um diesen Code eine `Wiederhole fortlaufend`-Schleife ein, sodass der Spieler viele Aufgaben gestellt bekommt.

+ Erstelle einen Countdown-Timer auf der Bühne, indem du eine Variable namens `Zeit`{:class="blockdata"} erstellst. Falls du Hilfe brauchst: Das Ghostbuster-Projekt beinhaltet (in Schritt 5) eine Anleitung zur Erstellung eines Timers!

+ Teste dein Projekt nochmals - du solltest nun solange Fragen gestellt bekommen, bis die Zeit abgelaufen ist.