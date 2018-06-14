\--- défi \---

## Défi: Course à 10 points

Pouvez-vous changer votre jeu, de sorte qu'au lieu de répondre à autant de questions que possible en 30 secondes, le joueur doit voir en combien de temps il peut obtenir 10 réponses correctes?

Pour ce faire, vous aurez seulement besoin de changer votre code temporel. Pouvez-vous voir ce qui doit être changé?

```blocks
    when I receive [start v]
    set [time v] to (30)
    repeat until <(time) = [0]>
        wait (1) secs
        change [time v] by (-1)
    end
    broadcast [end v]
```

\--- /défi \---