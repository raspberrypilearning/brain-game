## Jeux multiples

Ajoutons un bouton 'jeu' à votre jeu, pour que vous puissiez jouer plusieurs fois.



+ Créez un nouveau lutin du bouton 'Jouer', sur lequel votre joueur cliquera pour commencer un nouveau jeu. Vous pouvez le dessiner vous-même, ou modifier un lutin de la bibliothèque de Scratch.

	![screenshot](images/brain-play.png)

+ Ajoutez ce code à votre nouveau bouton.

	```blocks
		quand le drapeau vert pressé
		montrer

		quand ce lutin est cliqué
		cacher
		envoyer à tous [début v]
	```

	Ce code montre le bouton de jeu lorsque votre projet est commencé. Quand le bouton est cliqué, il est caché et diffuse ensuite un message qui commencera le jeu.

+ Vous devrez modifier le code de votre personnage afin que le jeu débute lorsqu'il recevra le message 'début'{.blockevents} et non pas quand le drapeau est cliqué.

	Remplacez le code ` quand le drapeau cliqué ` {.blockevents} par ` quand je reçois le début `{.blockevents}.

	![screenshot](images/brain-start.png)

+ Cliquez sur le drapeau vert et cliquez ensuite sur votre nouveau bouton de jeu pour le tester. Vous devriez voir que le jeu ne débute pas tant que vous ne cliquez pas sur le bouton.

+ Avez-vous remarqué que la minuterie commence lorsque le drapeau vert est cliqué et non quand le jeu commence?

	![screenshot](images/brain-timer-bug.png)

	Pouvez-vous réparer ce problème ?

+ Cliquez sur la scène et remplacez le bloc 'arrêter tout'  {.blockcontrol} avec le message 'fin' {.blockevents}.

	![screenshot](images/brain-end.png)

+ Vous pouvez maintenant ajouter ce code à votre bouton pour le montrer de nouveau à la fin de chaque jeu.

	```blocks
		quand je reçois [end v]
		montrer
	```

+ Vous devrez aussi arrêter votre personnage qui pose des questions à la fin de chaque jeu :

	```blocks
		quand je reçois [end v]
		stop [D'autres scénarios dans lutin v]
	```

+ Testez votre bouton de jeu en jouant deux ou trois fois. Vous devriez remarquer que le bouton de jeu apparaît après chaque jeu. Pour le tester plus facilement, vous pouvez raccourcir chaque jeu afin qu'il ne dure seulement que quelques secondes.

	```blocks
		[time v] prend la valeur [10]
	```

+ Vous pouvez même changer l'apparence du bouton lorsque la souris le survole.

	```blocks
		quand le drapeau vert pressé
		montrer
		répéter indéfiniment
   		si <[pointeur de souris v] touché?> alors
      		choisir l'effet [oeil de poisson v] pour (30)
   		sinon
      		choisir l'effet [oeil de poisson v] pour (0)
   		fin
		fin
	```

	![screenshot](images/brain-fisheye.png)



