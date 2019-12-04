## Jeux multiples

Tu vas maintenant ajouter un bouton "Jouer" pour que le joueur puisse jouer à ton jeu plusieurs fois.

--- task --- Crée un nouveau sprite de bouton "Jouer" sur lequel le joueur doit cliquer pour commencer une nouvelle partie.

Tu peux dessiner le sprite toi-même ou éditer un sprite à partir de la bibliothèque.

![Image du bouton jouer](images/brain-play.png)

--- /task ---

--- task --- Ajoute ce code à ton sprite bouton:

![Sprite bouton](images/button-sprite.png)

```blocks3
    lorsque le drapeau est cliqué
    afficher

    lorsque ce sprite est cliqué
    masquer
    envoyer à tous(démarrer v)
```

--- /task ---

Le nouveau code comprend un autre bloc `envoyer à tous`{:class="block3events"}, qui envoie le message "démarrer".

Le nouveau code fait apparaître le sprite bouton "Jouer" lorsque le joueur clique sur le drapeau. Lorsque le joueur clique sur le sprite bouton, celui-ci se cache et diffuse ensuite un message auquel les autres sprites peuvent réagir.

Pour le moment, le sprite personnage commence à poser des questions lorsque le joueur clique sur le drapeau. Modifie le code de ton jeu pour que le sprite personnage commence à poser des questions lorsqu’il reçoit la diffusion `'démarrer'`{:class="block3events"}.

--- task --- Sélectionne ton sprite personnage et, dans sa section de code, remplace le bloc `lorsque le drapeau est cliqué`{:class="block3events"} par un bloc `lorsque je reçois démarrer`{:class="block3events" }.

![Sprite personnage](images/giga-sprite.png)

```blocks3
<br />- lorsque le drapeau est cliqué
+ lorsque je reçois [démarrer v]
définir [numéro 1 v] sur (choisir au hasard (2) sur (12))
définir [numéro 2 v] sur (choisir au hasard (2) à (12) )
demander (rejoindre (numéro 1) (rejoindre [x] (numéro 2))) et attendre
si <(réponse) = ((numéro 1) * (numéro 2))> alors
    dire [oui!] :)] pendant (2) secondes
sinon
    dire [nope :(] pendant (2) secondes
fin
```

--- /task ---

--- task ---

Clique sur le drapeau vert, puis sur le nouveau bouton "Jouer" pour vérifier si cela fonctionne. Tu devrais voir que le jeu ne commence pas avant de cliquer sur le bouton.

--- /task ---

Peux-tu voir que le chronomètre commence lorsque le drapeau vert est cliqué, au lieu de commencer le jeu?

![La minuterie a commencé](images/brain-timer-bug.png)

--- task ---

Peux-tu changer le code de la minuterie pour que celle-ci démarre lorsque le joueur clique sur le bouton?

--- /task ---

--- task --- Ajoute du code à ton sprite pour que le bouton apparaisse à la fin de chaque partie.

![Sprite bouton](images/button-sprite.png)

```blocks3
    quand je reçois [fin v]
    montrer
```

--- /task ---

--- task ---

Teste le bouton "Jouer" en jouant à quelques jeux. Le bouton devrait apparaître à la fin de chaque partie.

Pour tester le jeu plus rapidement, tu peux modifier la valeur de `temps`{:class="block3variables"} afin que chaque jeu dure seulement quelques secondes.

![Scène](images/stage-sprite.png)

```blocks3
    mettre [temps v] à [10]
```

--- /task ---

--- task --- Tu peux modifier l'apparence du bouton lorsque le pointeur de la souris le survole.

![Button](images/button-sprite.png)

```blocks3
    quand le drapeau est cliqué
montrer
répéter indéfiniment
si <touching (mouse-pointer v)?> alors
ajouter l’effet [œil de poisson] (30)
sinon 
ajouter l’effet [œil de poisson] (0)
fin
fin
```

![capture d'écran](images/brain-fisheye.png) --- /task ---