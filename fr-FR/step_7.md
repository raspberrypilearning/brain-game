## Ajout de graphisme

Afin que votre personnage ne dise pas seulement ` oui! :) ` ou ` non `, ajoutons un graphisme qui permettra au joueur de savoir si la réponse est bonne ou mauvaise.

+ Créez un nouveau lutin appelé 'le Résultat', qui contient les costumes 'coché' et ' croix '.

	![screenshot](images/brain-result.png)

+ Changez le code de votre personnage afin qu'il diffuse les messages 'correct'{.blockevents} et 'mal' {.blockevents} au lieu de dire `oui` et `non`.

	![screenshot](images/brain-broadcast-answer.png)

+ Vous pouvez maintenant utiliser ces messages afin de montrer le costume 'coché' ou ' croix '. Ajoutez ce code à votre nouveau lutin 'résultat' :

	![screenshot](images/brain-show-answer.png)

+ Testez votre jeu de nouveau. Vous devriez voir un crochet quand vous obtenez une bonne question et une croix quand vous obtenez une mauvaise réponse!

	![screenshot](images/brain-test-answer.png)

+ Avez-vous remarquer que le code ` quand je reçois correct ` {.blockevents} et ` quand je reçois mal ` {.blockevents} est presque identique ? Créons une fonction pour rendre la modifiation du code plus facile.

	Sur votre lutin 'Résultat', cliquez sur ` Ajouter blocs ` {.blockmoreblocks} et cliquez ensuite sur ' Créer un Bloc '. Créez une nouvelle fonction appelée 'animée' {.blockmoreblocks}.

	![screenshot](images/brain-animate-function.png)

+ Vous pouvez alors ajouter le code d'animation dans votre nouvelle fonction d'animation et utiliser ensuite la fonction deux fois:


	![screenshot](brain-use-function.png)

+ Maintenant, si vous voulez montrer l'animation plus longtemps, vous devez faire un seul changement à votre fonction. Essayez-le!

+ Plutôt que de simplement afficher et cacher le crochet et la croix, vous pourriez changer votre fonction d'animation afin que le graphisme apparaisse en fondu. 

	```blocks
		définir [animate]
		choisir l'effet [fantôme v] pour (100)
		montrer
		répéter (25) fois
   			ajouter à l'effet [fantôme v] (-4)
		fin
		cacher
	```



