## Défi: course à 10 points

Peux-tu changer ton jeu pour que le joueur, au lieu de répondre au plus grand nombre de questions possible en 30 secondes, réponde à 10 questions le plus rapidement possible.

Pour effectuer ce changement, il te suffit de changer ton code de minuterie. Peux-tu voir quels blocs doivent être différents?

```blocks3
when I receive [démarrer v]
set [temps v] to (30)
repeat until <(tempo) = [0]> 
  wait (1) seconds
  change [temps v] by (-1)
end
broadcast (fin v)
```