## Jeux multiples

Ajoutons un bouton "play" à votre jeu, afin que vous puissiez jouer plusieurs fois.

+ Créez un nouveau lutin bouton de lecture, sur lequel votre joueur cliquera pour lancer une nouvelle partie. Vous pouvez le dessiner vous-même ou modifier un lutin à partir de la bibliothèque Scratch.
    
    ![screenshot](images/brain-play.png)

+ Ajoutez ce code à votre nouveau bouton.
    
    ```blocks
        Lorsque le drapeau est cliqué
        afficher
    
        quand ce lutin est cliqué 
        masquer
        envoyer a tous [début v]
    ```
    
    Ce code affiche le bouton de lecture lorsque votre projet est démarré. Lorsque le bouton est cliqué, il est masqué et envoie ensuite un message qui lancera le jeu.

+ Vous devrez modifier le code de votre personnage afin que le jeu commence quand il recevra le message {: class = "blockevents"} ` début ` , et non lorsque le drapeau est cliqué.
    
    Remplacer le code {: class = "blockevents"} ` lorsque le drapeau est cliqué ` avec {: class = "blockevents"} ` quand je reçois début ` 
    
    ![screenshot](images/brain-start.png)

+ Cliquez sur le drapeau vert, puis cliquez sur votre nouveau bouton de lecture pour le tester. Vous devriez voir que le jeu ne démarre pas tant que le bouton n'est pas cliqué.

+ Avez-vous remarqué que la minuterie commence quand on clique sur le drapeau vert, et non quand la partie commence?
    
    ![screenshot](images/brain-timer-bug.png)
    
    Pouvez-vous résoudre ce problème?

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