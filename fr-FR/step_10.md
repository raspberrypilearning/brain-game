\--- défi \---

## Défi: Course à 10 points

Pouvez-vous changer votre jeu, de sorte qu'au lieu de répondre à autant de questions que possible en 30 secondes, le joueur doit voir en combien de temps il peut obtenir 10 réponses correctes?

Pour ce faire, vous aurez seulement besoin de changer votre code temporel. Pouvez-vous voir ce qui doit être changé?

```blocks
    Quand je reçois [début v]
    mettre [temps v] à (30)
    répéter jusqu’à (temps) = [0]
         attendre (1) seconde
         mettre [temps v] à (-1)

    fin
    envoyer a tous [fin]
```

\--- /défi \---