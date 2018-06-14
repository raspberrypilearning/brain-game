## Ajout de graphisme

Au lieu que votre personnage dise simplement ` oui! :) ` ou ` non :( ` au joueur, ajoutons quelques graphiques qui permettront au joueur de savoir comment il repond.

+ Créez un nouveau lutin appelé 'Résultats', contenant à la fois un costume 'tic' et 'croix'.
    
    ![screenshot](images/brain-result.png)

+ Changez le code de votre personnage, de sorte que, il diffuse les messages {: class = "blockevents"} ` correct ` et {: class = "blockevents"} ` faux ` à la place.
    
    ![screenshot](images/brain-broadcast-answer.png)

+ Vous pouvez maintenant utiliser ces messages pour montrer le costume «tic» ou «croix». Ajoutez ce code à votre nouveau lutin "Résultat":
    
    ![screenshot](images/brain-show-answer.png)

+ Testez votre jeu à nouveau. Vous devriez voir une coche chaque fois que vous obtenez une question correcte, et une croix chaque fois que vous vous trompez!
    
    ![screenshot](images/brain-test-answer.png)

+ Avez-vous remarqué que le code pour {: class = "blockevents"} ` quand je reçois correct ` et {: class = "blockevents"} ` quand je reçois faux ` est presque identique? Créons une fonction pour faciliter la modification de votre code.
    
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