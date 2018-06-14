## Création des questions

Commençons par créer des questions aléatoires auxquelles le joueur devra répondre.

+ Démarrez un nouveau projet Scratch et supprimez le lutin de chat afin que votre projet soit vide. Vous pouvez trouver l'éditeur en ligne de Scratch à <a href="http://jumpto.cc/scratch-new" target="_blank"> jumpto.cc/scratch-new </a> .

+ Choisissez un personnage et un arrière plan pour votre jeu. Vous pouvez choisir ce que vous aimez! Voici un exemple:
    
    ![screenshot](images/brain-setting.png)

+ Créer 2 nouvelles variables appelées {: class = "blockdata"} ` numéro 1 ` et {: class = "blockdata"} ` numéro 2 ` . Ces variables vont stocker les 2 nombres qui seront multipliés ensemble.
    
    ![screenshot](images/brain-variables.png)

+ Ajoutez un code à votre personnage, pour définir ces deux variables sur un{: class = "blockoperators"} ` nombre aléatoire ` entre 2 et 12.
    
    ```blocks
        when flag clicked
        set [number 1 v] to (pick random (2) to (12))
        set [number 2 v] to (pick random (2) to (12))
    ```

+ Vous pouvez alors demander au joueur la réponse et lui faire savoir s'il s'est tromper ou non.
    
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