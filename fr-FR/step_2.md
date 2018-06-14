## Création des questions

Commençons par créer des questions aléatoires auxquelles le joueur devra répondre.

+ Démarrez un nouveau projet Scratch et supprimez le lutin de chat afin que votre projet soit vide. Vous pouvez trouver l'éditeur en ligne de Scratch à <a href="http://jumpto.cc/scratch-new" target="_blank"> jumpto.cc/scratch-new </a> .

+ Choisissez un personnage et un arrière plan pour votre jeu. Vous pouvez choisir ce que vous aimez! Voici un exemple:
    
    ![capture d'écran](images/brain-setting.png)

+ Créer 2 nouvelles variables appelées {: class = "blockdata"} ` numéro 1 ` et {: class = "blockdata"} ` numéro 2 ` . Ces variables vont stocker les 2 nombres qui seront multipliés ensemble.
    
    ![capture d'écran](images/brain-variables.png)

+ Ajoutez un code à votre personnage, pour définir ces deux variables sur un{: class = "blockoperators"} ` nombre aléatoire ` entre 2 et 12.
    
    ```blocks
        lorsque le drapeau est cliqué
        mettre [nombre 1 v] sur (choisissez aléatoire (2) à (12)) 
        mettre [nombre 2 v] sur (choisissez aléatoire (2) à (12))
    ```

+ Vous pouvez alors demander au joueur la réponse et lui faire savoir s'il s'est tromper ou non.
    
    ```blocks
        quand le drapeau est cliqué 
        mettre [nombre 1 v] à (nombre aléatoire (2) à (12))  
        mettre [nombre 2 v] à (nombre aléatoire (2) à (12)) 
        demander ((numéro 1) [x ] (numéro 2)) et attendez 
        si ((réponse) = ((numéro 1) * (numéro 2))) 
         alors dire [oui!] sinon dire [non :(] pendant 2 secondes
        end  
    ```

+ Testez entièrement votre projet en répondant correctement à une question et à une avec une mauvaise réponse.

+ Ajouter un {: class = "blockcontrol"}` répéter indéfiniment ` autour de ce code, de sorte que le joueur ait beaucoup de question.

+ Créer un compte à rebours sur la scène, en utilisant une variable appelée {: class = "blockdata"} ` temps ` . Le projet 'Ghostbusters' a des instructions pour chronométrer (à l'étape 5) si vous avez besoin d'aide!

+ Testez à nouveau votre projet - vous devriez être en mesure de continuer à répondre au question jusqu'à la fin du temps imparti.