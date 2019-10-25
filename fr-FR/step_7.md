## Ajouter des graphiques

Pour le moment, le sprite personnage dit seulement `oui! :)` ou `non :(` aux réponses du joueur. Ajoute des graphiques pour indiquer au joueur si sa réponse est correcte ou incorrecte.

\--- task \---

Crée une nouveau sprite appelé "Résultat" et donne-lui un "cocher / vérifier" et un costume "croix".

![Sprite avec coche et costumes croix](images/brain-result.png)

\--- /task \---

\--- task \---

Modifie le code de ton sprite personnage de sorte que, au lieu de dire quelque chose au joueur, il `envoyer à tous`{:class=« block3events»} les messages « correct » ou « mauvais ».

![Sprite Personnage](images/giga-sprite.png)

```blocks3
si <(réponse) = ((numéro 1) * (numéro 2))> alors

- dites [oui! :)] pendant (2) secondes
+ envoyer à tous (correct v)
sinon
- dire [non :(] pendant (2) secondes
+ envoyer à tous (mauvais v)
fin
```

\--- /task \---

\--- task \---

Maintenant , tu peux utiliser ces messages à `montrer`{:class="block3looks"} le costume 'coche' ou 'croix'. Ajoute le code suivant au sprite 'Résultat':

![Sprite Résultat](images/result-sprite.png)

```blocks3
    quand je reçois [correct v]
    basculer sur le costume (coche v)
    montrer
    attendre (1) secondes
    cacher

    quand je reçois [faux v]
    basculer sur le costume (croix v)
    montrer
    attendre (1) seconde
    masquer

    lorsque le drapeau est cliqué
    masquer
```

\--- /task \---

\--- task \--- Teste à nouveau ton jeu. Tu devrais voir la coche chaque fois que tu réponds correctement à une question et la croix lorsque tu réponds incorrectement!

![Coche pour correct, cocher pour mauvaise réponse](images/brain-test-answer.png)

\--- /task \---

Peux-tu voir que le code pour `lorsque je reçois correctes`{:class="block3events"} et `lorsque je reçois mauvais`{:class="block3events"} est presque identique?

Pour modifier ton code plus facilement, tu vas créer un bloc personnalisé.

\--- task \---

Sélectionne le sprite 'Résultat'. Clique ensuite sur `Mes Blocs`{:class="block3myblocks"}, puis sur **Créer un Bloc**. Crée un nouveau bloc et appelle-le `animer` {:class="block3myblocks"}.

![Sprite Résultat](images/result-sprite.png)

![Créer un bloc appelé animer](images/brain-animate-function.png)

\--- /task \---

\--- task \--- Déplace le code sur `montrer`{:class= block3looks"} et `masquer`{:class="block3looks"} le sprite "Résultat" dans le bloc `animer`{:class="block3myblocks"}:

![Sprite Résultat](images/result-sprite.png)

```blocks3
définir animer
montrer
attendre (1) secondes
masquer
```

\--- /task \---

\--- task \--- Assure-toi que tu as supprimé les blocs `montrer`{:class="block3looks"} et `masquer`{:class="block3looks"} en dessous de **tout les deux** des blocs `basculer sur le costume`{:class="block3looks"}.

Ajoute ensuite le bloc `animer`{:class="block3myblocks"} sous les deux blocs de `basculer sur le costume`{:class="block3looks"}. Ton code devrait maintenant ressembler à ceci:

![Sprite Résultat](images/result-sprite.png)

```blocks3
    lorsque je reçois [correct v]
    basculer sur le costume (coche v)
    animer :: personnalisé

    lorsque je reçois [faux v]
    basculer sur le costume (croix v)
    animer :: personnalisé
```

\--- /task \---

En raison du bloc personnalisé `animer`{:class="block3myblocks"}, il te suffit maintenant de modifier ton code si tu souhaites montrer les costumes du sprite "Résultat" plus ou moins longtemps.

\--- task \---

Change ton code pour que les costumes "coche" ou "croix" s'affichent pendant 2 secondes.

\--- /task \---

\--- task \--- Au lieu de `montrant`{:class="block3looks"} et `masquant`{:class="block3looks"} les costumes "coche" ou "croix", tu peux changer ton bloc`animer`{:class="block3myblocks"} pour que les costumes disparaissent.

![Sprite Résultat](images/result-sprite.png)

```blocks3
    définir animer
    définir effet [fantôme] sur (100)
    montrer
    répéter (25)
        changer effet [fantôme] sur (-4)
    fin
    cacher
```

\--- /task \---

Peux-tu améliorer l'animation des graphiques "coche" ou "croix"? Tu peux également ajouter du code pour faire disparaître les costumes ou utiliser d'autres effets sympas:

![capture d'écran](images/brain-effects.png)