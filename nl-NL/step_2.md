## Vragen maken

Laten we beginnen met het maken van willekeurige vragen die de speler moet beantwoorden.

+ Start een nieuw Scratch-project en verwijder de cat-sprite zodat uw project leeg is. Je kunt de online Scratch-editor vinden op <a href="http://jumpto.cc/scratch-new" target="_blank"> jumpto.cc/scratch-new </a>.

+ Kies een personage en een achtergrond voor je spel. Je kunt kiezen wat je wilt! Hier is een voorbeeld:
    
    ![screenshot](images/brain-setting.png)

+ Maak 2 nieuwe variabelen met de naam ` nummer 1 ` {: class = "blockdata"} en ` nummer 2 ` {: Class = "blockdata"}. Deze variabelen slaan de 2 nummers op die samen worden vermenigvuldigd.
    
    ![screenshot](images/brain-variables.png)

+ Voeg code toe aan uw karakter, om beide variabelen willekeurig in te stellen op ` ` {: class = "blockoperators"} een getal tussen 2 en 12.
    
    ```blocks
    when flag clicked
    set [number 1 v] to (pick random (2) to (12))
    set [number 2 v] to (pick random (2) to (12))
```

+ U kunt de speler vervolgens om het antwoord vragen en hem laten weten of ze gelijk hebben of niet.
    
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

+ Test uw project volledig, door één vraag goed te beantwoorden en één vraag met het verkeerde antwoord.

+ Add a `forever`{:class="blockcontrol"} loop around this code, so that the player is asked lots of questions.

+ Create a countdown timer on the stage, using a variable called `time`{:class="blockdata"}. The 'Ghostbusters' project has instructions for making a timer (in step 5) if you need help!

+ Test your project again - you should be able to continue asking questions until the time runs out.