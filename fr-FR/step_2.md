## Création des questions

Tu vas commencer par créer des questions aléatoires auxquelles le joueur doit répondre.

--- task ---

Ouvre un nouveau projet Scratch.

**En ligne:** ouvre un nouveau projet Scratch en ligne sur [rpf.io/scratch-new](https//rpf.io/scratch-new){:target="_blank"}.

**Hors ligne:** ouvre un nouveau projet dans l'éditeur hors ligne.

Si tu dois télécharger et installer l'éditeur hors ligne Scratch, tu peux le trouver à [rpf.io/scratchoff](https//rpf.io/scratchoff){:target="_blank"}.

--- /task ---

--- task --- Ajoute un sprite personnage et un arrière-plan pour ton jeu. Tu peux choisir celui que tu aimes! Voici un exemple:

![capture d'écran](images/brain-setting.png)

--- /task ---

--- task --- Assure-toi d'avoir sélectionné ton sprite personnage. Crée deux nouvelles variables, appelées `numéro 1`{:class="block3variables"} et `numéro 2`{:class="block3variables"}, pour stocker les numéros des questions du quiz.

![screenshot](images/giga-sprite.png) ![capture d'écran](images/brain-variables.png)

[[[generic-scratch3-add-variable]]]

--- /task ---

--- task --- Ajoute du code à ton sprite personnage pour définir les deux `variables`{:class="block3variables"} à un nombre `aléatoire`{:class="block3operators"} entre 2 et 12.

![capture d'écran](images/giga-sprite.png)

```blocks3
quand le drapeau vert pressé
mettre [numéro 1 v] à (nombre aléatoire entre (2) et (12))
mettre [numéro 2 v] à (nombre aléatoire entre (2) et (12))
```

--- /task ---

--- task --- Ajouter le code à `demander`{:class="block3sensing"} au joueur pour la réponse, puis `dire pendant 2 secondes`{:class="block3looks"} si la réponse était correcte ou fausse:

![capture d'écran](images/giga-sprite.png)

```blocks3
quand le drapeau vert pressé
mettre [numéro 1 v] à (nombre aléatoire entre (2) et (12))
mettre [numéro 2 v] à (nombre aléatoire entre (2) et (12))
+ demander (regrouper (numéro 1) et (regrouper [ x ] et (numéro 2))) et attendre
+ si <(réponse) = ((numéro 1) * (numéro 2))> alors 
+ dire [oui! :)] pendant (2) secondes
+ sinon 
+ dire [non :(] pendant (2) secondes
+ fin
```

--- /task ---

--- task ---

Teste ton projet deux fois: réponds correctement à une question et à l’autre incorrectement.

--- /task ---

--- task ---

Ajoute une boucle `répéter indéfiniment`{:class="block3control"} autour de ce code, afin que le jeu pose de nombreuses questions au joueur d'affilée.

--- hints ---
 --- hint ---

Tu dois ajouter un bloc `répéter indéfiniment`{:class="block3control"} et y placer tout le code, à l'exception du bloc `lorsque le drapeau est cliqué`{:class="block3control"}.

--- /hint --- --- hint --- Voici le bloc dont tu as besoin :

```blocks3
répéter indéfiniment
fin
```

---/hint--- ---hint--- Voici a quoi devrait ressembler ton bloc

```blocks3
quand le drapeau vert pressé
+ répéter indéfiniment 
    mettre [numéro 1 v] à (nombre aléatoire entre (2) et (12))
    mettre [numéro 2 v] à (nombre aléatoire entre (2) et (12))
    demander (regrouper (numéro 1) et (regrouper [ x ] et (numéro 2))) et attendre
    si <(réponse) = ((numéro 1) * (numéro 2))> alors 
        dire [oui! :)] pendant (2) secondes
    sinon 
        dire [non :(] pendant (2) secondes
    fin
fin
```

--- /hint ------ /hints ---

--- /task ---
