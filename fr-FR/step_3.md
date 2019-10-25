## Défi: Changement de costumes

\--- task \--- Crée un compte à rebours sur la scène à l'aide d'une nouvelle variable appelée `temps`{:class="block3variables"}. La minuterie devrait commencer à 30 secondes et décompter jusqu'à 0 secondes.

![Sprite Scène](images/stage-sprite.png)

\--- hints \--- \--- hint \---

Crée une `variable`{:class="block3variables"}, appelle-la "temps" et définis sa valeur sur `30`.

Ajoute ensuite du code pour décompter `temps`{: class = "block3variables"} jusqu'à 0 dans les 30 secondes. Pour ce faire, soustrais `1` de `temps`{:class="block3variables"} toutes les `1` seconde et répète cette opération jusqu'à ce que le `temps`{:class="block3variables"} soit égal à `0`.

\--- /hint \--- \--- hint \--- Voici les blocs dont tu as besoin :

```blocks3
répéter jusqu'à < >

fin

attendre (1) secondes

changer [temps v] par (1)

(temps)

lorsque le drapeau est cliqué

<() = ()>

définir [temps v] sur [0]
```

\--- / hint \--- \--- hint \--- Voici à quoi devrait ressembler ton nouveau code:

```blocks3
lorsque le drapeau est cliqué
définir [temps v] sur [30]
répéter jusqu'à ce que <(temps) = (0)>
    attendre (1) secondes
    changer [temps v] par (-1)
fin
```

\--- /hint \--- \--- /hints \---

\--- /task \---

\--- task \---

Crée un `envoyer à tous`{:class="block3control"} qui envoie le message "fin". Un `envoyer à tous`{:class="block3control"} est comme une annonce par haut-parleur: elle peut être entendue par tous tes sprites. Ajoute le bloc `envoyer à tous`{:class="block3control"} à la fin du code du minuteur pour que le code soit envoyé et le message "fin" lorsque le `temps`{: class = "block3variables"} est décompté à `0`.

![Sprite Scène](images/stage-sprite.png)

```blocks3
    envoyer à tous (fin v)
```

\--- /task \---

\--- task \--- Sélectionne ton sprite personnage et ajoute du code pour que le sprite `arrête les autres scripts`{:class="block3control"} lorsqu'il reçoit le message `fin`{:class="block3control"}.

![Giga Sprite](images/giga-sprite.png)

```blocks3
    quand je reçois [fin v] 
    stop [autres scripts du lutin v]
```

\--- /task \---

\--- task \---

Teste ton jeu à nouveau. Il devrait continuer à poser des questions jusqu'à ce que le chronomètre se soit écoulé jusqu'à zéro.

\--- /task \---