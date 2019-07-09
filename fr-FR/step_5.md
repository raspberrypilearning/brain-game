## Jeux multiples

Vous allez maintenant ajouter un bouton "Jouer" pour que le joueur puisse jouer à votre jeu plusieurs fois.

\--- task \--- Créez un nouveau sprite de bouton "Jouer" sur lequel le joueur doit cliquer pour commencer une nouvelle partie.

Vous pouvez dessiner vous-même l'image-objet ou éditer une image-objet à partir de la bibliothèque.

![Image du bouton de lecture](images/brain-play.png)

\--- /task \---

\--- task \--- Ajoutez ce code à votre sprite de bouton:

![Bouton sprite](images/button-sprite.png)

```blocks3
    lorsque flag a cliqué sur
    afficher

    lorsque ce sprite a cliqué sur
    masquer
    diffusion (démarrer v)
```

\--- /task \---

Le nouveau code comprend un autre bloc `broadcast`{: class = "block3events"}, qui envoie le message "start".

Le nouveau code fait apparaître le sprite du bouton "Lecture" lorsque le joueur clique sur le drapeau. Lorsque le joueur clique sur le bouton image-objet, celui-ci se cache et diffuse ensuite un message auquel les autres images-objets peuvent réagir.

Pour le moment, le personnage du personnage commence à poser des questions lorsque le joueur clique sur le drapeau. Modifiez le code de votre jeu pour que l’image-objet de personnage commence à poser des questions lorsqu’elle reçoit la diffusion 'début' ``: {: class = "block3events"}.

\--- task \--- Sélectionnez votre image-objet de personnage et, dans sa section de code, remplacez le bloc `lorsque l'indicateur est cliqué sur le bloc`{: class = "block3events"} par un `lorsque je reçois le début de`: {: class = "block3events" } bloquer.

![Personnage de sprite](images/giga-sprite.png)

```blocks3
<br />- lorsque l'indicateur a été cliqué sur
+ lorsque je reçois [début v]
régler [numéro 1 v] sur (prendre au hasard (2) sur (12))
régler [numéro 2 v] sur (prendre au hasard (2) à (12) )
demander (rejoindre (numéro 1) (rejoindre [x] (numéro 2))) et attendre
si &lt;(réponse) = ((numéro 1) * (numéro 2))&gt; puis
    répondre [oui! :)] pendant (2) secondes
sinon
    dire [nope :(] pendant (2) secondes
fin
```

\--- /task \---

\--- task \---

Cliquez sur le drapeau vert, puis sur le nouveau bouton "Lecture" pour vérifier si cela fonctionne. Vous devriez voir que le jeu ne commence pas avant de cliquer sur le bouton.

\--- /task \---

Pouvez-vous voir que le chronomètre commence lorsque le drapeau vert est cliqué, au lieu de commencer le jeu?

![La minuterie a commencé](images/brain-timer-bug.png)

\--- task \---

Pouvez-vous changer le code de la minuterie pour que celle-ci démarre lorsque le joueur clique sur le bouton?

\--- /task \---

\--- tâche \--- Ajoutez du code à votre image-objet pour que le bouton apparaisse à la fin de chaque partie.

![Bouton sprite](images/button-sprite.png)

```blocks3
    quand je reçois [fin v]
    montrer
```

\--- /task \---

\--- task \---

Testez le bouton "Jouer" en jouant à quelques jeux. Le bouton devrait apparaître à la fin de chaque partie.

Pour tester le jeu plus rapidement, vous pouvez modifier la valeur de `fois`{: class = "block3variables"} afin que chaque jeu dure seulement quelques secondes.

![Étape](images/stage-sprite.png)

```blocks3
    mettre [temps v] à [10]
```

\--- /task \---

\--- task \--- Vous pouvez modifier l'apparence du bouton lorsque le pointeur de la souris le survole.

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

![capture d'écran](images/brain-fisheye.png) \--- /task \---