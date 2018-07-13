--- challenge ---

## Défi: Course à 10 points

Peux-tu changer ton jeu, de sorte qu'au lieu de répondre à autant de questions que possible en 30 secondes, le joueur doit voir en combien de temps il peut obtenir 10 réponses correctes?

Pour ce faire, tu auras seulement besoin de changer le code de ton chronomètre. Peux-tu voir ce qui doit être changé?

```blocks
    quand je reçois [début v]
mettre [temps v] à (30)
répéter jusqu’à <(temps) = [0]> 
  attendre (1) secondes
  ajouter à [temps v] (-1)
end
envoyer à tous [fin v]
```

--- /challenge ---
