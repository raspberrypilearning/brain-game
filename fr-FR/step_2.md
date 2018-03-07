## Création des questions

Commençons en créant des questions aléatoires pour le joueur.



+ Commencez un nouveau projet Scratch et supprimez le lutin de chat pour que votre projet soit vide. Vous pouvez trouver l'éditeur Scratch en ligne à <a href="http://jumpto.cc/scratch-new">jumpto.cc/scratch-new</a>.

+ Choisissez un personnage et un arrière-plan pour votre jeu. Vous pouvez choisir ce que vous aimez! Voici un exemple :

	![screenshot](images/brain-setting.png)

+ Créez 2 nouvelles variables appelées ` numéro 1`{:class="blockdata"} Et `numéro 2`{:class="blockdata"}. Ces variables stockeront les 2 nombres qui seront multipliés ensemble.

	![screenshot](images/brain-variables.png)

+ Ajoutez le code à votre personnage afin de mettre ces deux variables à un `nombre aléatoire entre`{:class="blockoperators"} 2 et 12.

	```blocks
		quand le drapeau vert pressé
		[number 1 v] prend la valeur (nombre aléatoire entre (2) et (12))
	[number 2 v] prend la valeur (nombre aléatoire entre (2) et (12))
	```

+ Vous pouvez alors demander la réponse au joueur et lui indiquer si c'était vrai ou faux. 

	```blocks
		quand le drapeau vert pressé
		[number 1 v] prend la valeur (nombre aléatoire entre (2) et (12))
		[number 2 v] prend la valeur (nombre aléatoire entre (2) et (12))
		demander (regroupe (number 1) (regroupe [x] (number 2))) et attendre
		si <(réponse) = ((number 1) * (number 2))> alors
   			dire [oui! :)] pendant (2) secondes
		sinon
   			dire [non :(] pendant (2) secondes
		fin
	```

+ Testez votre projet entièrement en répondant une fois avec une bonne réponse et une fois avec une mauvaise réponse.

+Ajoutez la boucle `répéter indéfiniment`{:class="blockcontrol"} autour de ce code, afin que plusieurs questions soient posées au joueur.

+ Créez une minuterie sur la scène en utilisant une variable appelée `temps`{:class="blockdata"}. Si vous avez besoind d'aide, le projet 'GhostBuster' possède des instructions sur comment créer une minuterie (dans l'étape 6).

+ Testez votre projet de nouveau, vous devriez pouvoir continuer à poser des questions jusqu'à ce que le temps soit écoulé.



