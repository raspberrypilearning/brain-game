--- challenge ---
## Défi : Course à 10 points
Au lieu de répondre au plus grand nombre de réponses possibles en 30 secondes, pouvez-vous changer votre jeu afin qu'il demande au joueur d'obtenir 10 bonnes réponses le plus rapidement possible?  

Pour ce faire, vous devrez seulement changer votre code de minuterie. Pouvez-vous voir quoi doit être modifié?

```blocks
	quand je reçois [start v]
	[time v] prend la valeur (30)
	répéter jusqu’à <(time) = [0]>
   		attendre (1) secondes
   		ajouter à [time v] (-1)
	fin
	envoyer à tous [fin v]
```




--- /challenge ---