## Meerdere spellen

Laten we een 'speel' knop toevoegen aan je spel, zodat je heel vaak kunt spelen.

+ Maak een nieuwe 'speel'-knop sprite, waarop uw speler zal klikken om een ​​nieuw spel te starten. Je kunt het zelf tekenen of een sprite bewerken vanuit de Scratch-bibliotheek.
    
    ![screenshot](images/brain-play.png)

+ Voeg deze code toe aan je nieuwe knop.
    
    ```blocks
    when flag clicked
    show

    when this sprite clicked
    hide
    broadcast [start v]
```

Deze code geeft de afspeelknop weer wanneer uw project is gestart. Wanneer op de knop wordt geklikt, wordt deze verborgen en wordt vervolgens een bericht uitgezonden dat het spel start.

+ You'll need to edit your character's code, so that the game starts when they receive the `start`{:class="blockevents"} message, and not when the flag is clicked.
    
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