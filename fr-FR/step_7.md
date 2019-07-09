## Ajout de graphisme

Pour le moment, le personnage du personnage dit seulement `oui! :)` ou `non :(` aux réponses du joueur. Ajoutez des graphiques pour indiquer au joueur si sa réponse est correcte ou incorrecte.

\--- task \---

Créez une nouvelle image-objet appelée "Résultat" et donnez-lui un "tick / check" et un costume de "croix".

![Sprite avec tiques et costumes croisés](images/brain-result.png)

\--- /task \---

\--- task \---

Modifier le code de votre sprite de caractères de sorte que, au lieu de dire quelque chose au joueur, il `émissions`{: class = « block3events »} les messages « correct » ou « mauvais ».

![Personnage de sprite](images/giga-sprite.png)

```blocks3
si <(réponse) = ((numéro 1) * (numéro 2))> alors

- dites [oui! :)] pendant (2) secondes
+ diffusion (correct v)
sinon
- dites [nope :(] pendant (2) secondes
+ diffusion (mauvais v)

```

\--- /task \---

\--- task \---

Maintenant , vous pouvez utiliser ces messages à `Afficher`{: class = "block3looks"} le costume 'TICK' ou 'croix'. Ajoutez le code suivant à l'image-objet 'Résultat':

![Résultat sprite](images/result-sprite.png)

```blocks3
    quand je reçois [correct v]
    change de costume en (tick v)
    montre
    attend (1) secondes
    cache

    quand je reçois [faux v]
    change de costume en (croix v)
    montre
    attend (1) seconde
    masquer

    lorsque le drapeau a cliqué
    masquer
```

\--- /task \---

\--- tâche \--- Testez à nouveau votre jeu. Vous devriez voir la coche chaque fois que vous répondez correctement à une question et la croix lorsque vous répondez incorrectement!

![Cochez pour corriger, cocher pour mauvaise réponse](images/brain-test-answer.png)

\--- /task \---

Pouvez-vous voir que le code pour `lorsque je reçois les correctes`{: class = "block3events"} et `lorsque je reçois le mauvais`{: class = "block3events"} est presque identique?

Pour modifier votre code plus facilement, vous allez créer un bloc personnalisé.

\--- task \---

Sélectionnez le sprite 'Résultat'. Cliquez ensuite sur `My Blocks`{: class = "block3myblocks"}, puis sur **Make a Block**. Créez un nouveau bloc et appelez-le `animate`{: class = "block3myblocks"}.

![Résultat sprite](images/result-sprite.png)

![Créer un bloc appelé animer](images/brain-animate-function.png)

\--- /task \---

\--- tâche \--- Déplacez le code vers `affichez`{: class = "block3looks"} et `masquez`{: class = "block3looks"} le sprite "Résultat" dans le `animé`{: class = " block3myblocks "} bloc:

![Résultat sprite](images/result-sprite.png)

```blocks3
définir animer
afficher
attendre (1) secondes
masquer
```

\--- /task \---

\--- tâche \--- Assurez-vous que vous avez supprimé les `shows`{: class = "block3looks"} et `masquer`{: class = "block3looks"} blocs en dessous de **fois** ``: class = "block3looks"} blocs.

Ajoutez ensuite le bloc `animate`{: class = "block3myblocks"} sous les deux blocs de `commutateurs`{: class = "block3looks"}. Votre code devrait maintenant ressembler à ceci:

![Résultat sprite](images/result-sprite.png)

```blocks3
    lorsque je reçois [correct v]
    change de costume en (tick v)
    animate :: custom

    quand je reçois [faux v]
    change de costume en (croix v)
    animate :: custom
```

\--- /task \---

En raison du bloc personnalisé `animate`{: class = "block3myblocks"}, il vous suffit maintenant de modifier votre code si vous souhaitez afficher les costumes du sprite "Résultat" plus ou moins longtemps.

\--- task \---

Changez votre code pour que les costumes "tick" ou "cross" s'affichent pendant 2 secondes.

\--- /task \---

\--- tâche \--- Au lieu de `montrant`{: class = "block3looks"} et `masquant`{: class = "block3looks"} les costumes "tick" ou "cross", vous pouvez changer votre `animé`{: class = "block3myblocks"} bloque pour que les costumes disparaissent.

![Résultat sprite](images/result-sprite.png)

```blocks3
    définir animer
    régler [effet fantôme] sur (100)
    afficher
    répéter (25)
        changer effet [effet fantôme] de (-4)
    fin

```

\--- /task \---

Pouvez-vous améliorer l'animation des graphiques "tick" ou "cross"? Vous pouvez également ajouter du code pour faire disparaître les costumes ou utiliser d'autres effets sympas:

![capture d'écran](images/brain-effects.png)