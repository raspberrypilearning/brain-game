## Défi: course à 10 points

Peux-tu changer ton jeu pour que le joueur, au lieu de répondre au plus grand nombre de questions possible en 30 secondes, réponde à 10 questions le plus rapidement possible.

Pour effectuer ce changement, il te suffit de changer ton code de minuterie. Peux-tu voir quels blocs doivent être différents?

```blocks3
quand je reçois [démarrer v]
mettre [temps v] à (30)
répéter jusqu'à ce que <(temps ::variables) = [0]> 
  attendre (1) secondes
  ajouter (-1) à [temps v]
fin
envoyer à tous (fin v)
```