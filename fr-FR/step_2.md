## Création des questions

Vous allez commencer par créer des questions aléatoires auxquelles le joueur doit répondre.

\--- task \---

Ouvre un nouveau projet Scratch.

** En ligne :** ouvre un nouveau projet Scratch en ligne à [rpf.io/scratch-new](http://rpf.io/scratchon){:target="_blank"}.

**Hors ligne:** ouvre un nouveau projet dans l'éditeur hors ligne.

Si tu dois télécharger et installer l'éditeur hors ligne Scratch, tu peux le trouver à [rpf.io/scratchoff](http://rpf.io/scratchoff){:target="_blank"}.

\--- /task \---

\--- task \--- Ajouter un sprite de personnage et une toile de fond pour votre jeu. Vous pouvez choisir celui que vous aimez! Voici un exemple:

![capture d'écran](images/brain-setting.png)

\--- /task \---

\--- tâche \--- Assurez-vous d'avoir sélectionné votre sprite de personnage. Créez deux nouvelles variables, appelées `numéro 1`{: class = "block3variables"} et `numéro 2`{: class = "block3variables"}, pour stocker les numéros des questions du quiz.

![screenshot](images/giga-sprite.png) ![capture d'écran](images/brain-variables.png)

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- \--- tâche code Ajouter à l' image - objet de caractères pour définir les deux `des variables`{: class = "block3variables"} à un `aléatoires`: nombre {class = "block3operators"} entre 2 et 12.

![capture d'écran](images/giga-sprite.png)

```blocks3
lorsque le drapeau est cliqué
définissez [numéro 1 v] sur (prendre au hasard (2) sur (12))
définissez [numéro 2 v] sur (prendre au hasard (2) à (12))
```

\--- /task \---

\--- tâche \--- Ajouter le code à `demande`{: class = "block3sensing"} au joueur pour la réponse, puis `dire pendant 2 secondes`{: class = "block3looks"} si la réponse était correcte ou faux:

![capture d'écran](images/giga-sprite.png)

```blocks3
lorsque le drapeau a cliqué sur
définissez [numéro 1 v] sur (sélectionnez au hasard (2) à (12))
définissez [numéro 2 v] sur (sélectionnez au hasard (2) à (12))

+ ask (rejoindre (numéro 1) (rejoindre [x] (numéro 2))) et attendez
+ si <(réponse) = ((numéro 1) * (numéro 2))> puis
+ dites [oui! :)] pendant (2) secondes
+ sinon
+ dites [non :(] pendant (2) secondes
+ fin
```

\--- /task \---

\--- task \---

Testez votre projet deux fois: répondez correctement à une question et à l’autre.

\--- /task \---

\--- task \---

Ajoutez une boucle `jamais`{: class = "block3control"} autour de ce code, afin que le jeu pose de nombreuses questions au joueur.

\--- hints \--- \--- hint \---

Vous devez ajouter un bloc `pour toujours`{: class = "block3control"} et y placer tout le code, à l'exception du bloc `lorsque l'indicateur a été cliqué`.

\--- / indice \--- \--- indice \--- Voici le bloc dont vous avez besoin:

```blocks3
toujours
fin
```

\---/hint\--- \---hint\--- Voici a quoi devrait ressembler votre bloc

```blocks3
lorsque le drapeau est cliqué

+ indéfiniment
    définissez [numéro 1 v] sur (choisissez au hasard (2) à (12))
    définissez [numéro 2 v] sur (sélectionnez au hasard (2) à (12))
    1) (rejoindre [x] (numéro 2))) et attendre
    si <(réponse) = ((numéro 1) * (numéro 2))> puis
        répondre [oui! :)] pendant (2) secondes
    sinon
        dire [non :(] pour (2) secondes
    end
end
```

\--- /hint \--- \--- /hints \---

\--- /task \---