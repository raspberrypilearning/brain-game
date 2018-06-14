## Jeux multiples

Ajoutons un bouton "play" à votre jeu, afin que vous puissiez jouer plusieurs fois.

+ Créez un nouveau lutin bouton de lecture, sur lequel votre joueur cliquera pour lancer une nouvelle partie. Vous pouvez le dessiner vous-même ou modifier un lutin à partir de la bibliothèque Scratch.
    
    ![capture d'écran](images/brain-play.png)

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
    
    ![capture d'écran](images/brain-start.png)

+ Cliquez sur le drapeau vert, puis cliquez sur votre nouveau bouton de lecture pour le tester. Vous devriez voir que le jeu ne démarre pas tant que le bouton n'est pas cliqué.

+ Avez-vous remarqué que la minuterie commence quand on clique sur le drapeau vert, et non quand la partie commence?
    
    ![capture d'écran](images/brain-timer-bug.png)
    
    Pouvez-vous résoudre ce problème?

+ Cliquez sur la scène, et remplacez le {: class = "blockcontrol"} ` tout arrêter ` avec un bloc {: class = "blockevents"} ` fin`
    
    ![capture d'écran](images/brain-end.png)

+ Vous pouvez maintenant ajouter du code à votre bouton, pour le montrer à la fin de chaque partie.
    
    ```blocks
        quand je reçois [fin v]
        montrer
    ```

+ Vous aurez également besoin d’arrêter votre personnage de poser des questions à la fin de chaque partie :
    
    ```blocks
        quand je reçois [fin v] 
        stop [autres scripts du lutin v]
    ```

+ Testez votre bouton de jeu en jouant quelques parties. Vous devriez remarquer que le bouton de lecture s'affiche après chaque partie. Pour faciliter les tests, vous pouvez raccourcir chaque partie de sorte qu'elle ne dure que quelques secondes.
    
    ```blocks
        régler [temps v] sur [10]
    ```

+ Vous pouvez même changer l'aspect du bouton lorsque la souris passe dessus.
    
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
    
    ![capture d'écran](images/brain-fisheye.png)