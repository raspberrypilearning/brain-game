## Défi: Changement de costumes

\--- task \--- Créez un compte à rebours sur la scène à l'aide d'une nouvelle variable appelée `fois`{: class = "block3variables"}. La minuterie devrait commencer à 30 secondes et compter jusqu'à 0 secondes.

![Sprite de scène](images/stage-sprite.png)

\--- hints \--- \--- hint \---

Créez une variable ``{: class = "block3variables"}, appelez-la "heure" et définissez sa valeur sur `30`.

Ajoutez ensuite du code pour compter `fois`{: class = "block3variables"} jusqu'à 0 dans les 30 secondes. Pour ce faire, soustrayez `1` de `fois`{: class = "block3variables"} toutes les `1` secondes et répétez cette opération jusqu'à `fois`{: class = "block3variables"} est égal à `0`.

\--- / indice \--- \--- indice \--- Voici les blocs dont vous avez besoin:

```blocks3
répéter jusqu'à < >

end

wait (1) secondes

changer [heure v] de (1)

(heure)

lorsque le drapeau est cliqué

<() = ()>

régler [heure v] sur [0]
```

\--- / hint \--- \--- hint \--- Voici à quoi devrait ressembler votre nouveau code:

```blocks3
lorsque le drapeau est cliqué sur
définissez [heure v] sur [30]
répétez jusqu'à ce que <(heure) = (0)>
    attend (1) secondes
    change [heure v] de (-1)
fin
```

\--- /hint \--- \--- /hints \---

\--- /task \---

\--- task \---

Créer une diffusion ``: {: class = "block3control"} qui envoie le message "end". Une diffusion ``{: class = "block3control"} est comme une annonce par haut-parleur: elle peut être entendue par tous vos sprites. Ajoutez le bloc `broadcast`{: class = "block3control"} à la fin du code du temporisateur pour que le code soit envoyé et le message "end" lorsque le `fois`{: class = "block3variables"} est passé à `0`.

![Sprite de scène](images/stage-sprite.png)

```blocks3
    diffusion (fin v)
```

\--- /task \---

\--- task \--- Sélectionnez votre sprite de personnage et ajoutez du code pour que le sprite `arrête les autres scripts`{: class = "block3control"} lorsqu'il reçoit le message `end`{: class = "block3control"} .

![Giga Sprite](images/giga-sprite.png)

```blocks3
    quand je reçois [fin v] 
    stop [autres scripts du lutin v]
```

\--- /task \---

\--- task \---

Testez votre jeu à nouveau. Il devrait continuer à poser des questions jusqu'à ce que le chronomètre se soit écoulé jusqu'à zéro.

\--- /task \---