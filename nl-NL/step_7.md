## Afbeeldingen toevoegen

In plaats van dat je alleen maar ` Ja! :) ` of ` nee :( ` zegt tegen de speler, gaan we wat afbeeldingen toevoegen die de speler laten weten hoe ze het doen.

+ Maak een nieuwe sprite met de naam 'Result', die zowel een 'vinkje'- als een 'kruis'-uiterlijk bevat.
    
    ![screenshot](images/brain-result.png)

+ Verander de code van je personage, zodat in plaats van de speler te vertellen hoe ze het deden, het ` correct ` {: class = "blockevents"} en ` fout ` {: class = "blockevents"} berichten uitzend.
    
    ![screenshot](images/brain-broadcast-answer.png)

+ U kunt deze berichten nu gebruiken om het 'vinkje'- of' kruis'-kostuum te laten zien. Voeg deze code toe aan uw nieuwe 'Result' sprite:
    
    ![screenshot](images/brain-show-answer.png)

+ Test je spel opnieuw. Je moet een vinkje zien als je een vraag goed hebt, en een kruisje als je er één fout hebt!
    
    ![screenshot](images/brain-test-answer.png)

+ Is het je opgevallen dat de code voor ` wanneer ik correct ontvang ` {: class = "blockevents"} en ` wanneer ik verkeerd ontvang ` {: class = "blockevents"} is bijna identiek? Laten we een functie maken om het gemakkelijker voor u te maken om uw code aan te passen.
    
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