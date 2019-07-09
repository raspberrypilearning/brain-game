## Défi: Son et musique

Pouvez-vous changer votre jeu pour que le joueur, au lieu de répondre au plus grand nombre de questions possible en 30 secondes, réponde à 10 questions le plus rapidement possible

Pour effectuer ce changement, il vous suffit de changer votre code de minuterie. Pouvez-vous voir quels blocs doivent être différents?

```blocks3
    quand je reçois [début v]
    régler [heure v] à (30)
    répéter jusqu'à <(heure) = [0]>
        attendre (1) secondes
        changer [heure v] de (-1)
    fin
    v)
```