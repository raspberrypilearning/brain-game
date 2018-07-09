## Jeux multiples

Ajoutons un bouton "play" à votre jeu, afin que vous puissiez jouer plusieurs fois.

+ Crée un nouveau lutin "bouton de lecture", sur lequel votre joueur cliquera pour lancer une nouvelle partie. Tu peux le dessiner toi-même ou modifier un lutin à partir de la bibliothèque Scratch.
    
    ![capture d'écran](images/brain-play.png)

+ Ajoute ce code à ton nouveau bouton.
    
    ```blocks
        quand le drapeau est cliqué
    montrer
    
    quand ce lutin est cliqué 
    cacher
    envoyer à tous [début v]
    ```
    
    Ce code affiche le bouton de lecture lorsque votre projet est démarré. Lorsque le bouton est cliqué, il est masqué et envoie ensuite un message qui lancera le jeu.

+ Tu devras modifier le code de ton personnage afin que le jeu commence quand il recevra le message `début`{:class="blockevents"}, et non lorsque le drapeau est cliqué.
    
    Remplace le code `lorsque le drapeau est cliqué`{:class="blockevents"} avec `quand je reçois début`{:class="blockevents"}.
    
    ![capture d'écran](images/brain-start.png)

+ Clique sur le drapeau vert, puis clique sur ton nouveau bouton de lecture pour le tester. Tu devrais voir que le jeu ne démarre pas tant que le bouton n'est pas cliqué.

+ As-tu remarqué que la minuterie commence quand on clique sur le drapeau vert, et non quand la partie commence?
    
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
        quand le drapeau est cliqué
        montrer
        répéter indéfiniment
         si (pointeur de souris v touché)
            mettre l’effet [œil de poisson] à (30)
         sinon mettre l’effet [œil de poisson] à (0)
        fin 
    ```
    
    ![capture d'écran](images/brain-fisheye.png)