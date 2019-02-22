## Diversos jocs

Ara, afegireu un botó "Reproduir", perquè el jugador pugui jugar moltes vegades.

\--- tasca \--- Creeu un nou sprite del botó "Reprodueix" que el jugador necessita fer clic per iniciar un nou joc.

Podeu dibuixar el sprite o editar un sprite de la biblioteca.

![Imatge del botó de reproducció](images/brain-play.png)

\--- / tasca \---

\--- tasca \--- Afegiu aquest codi al vostre botó sprite:

![Sprite del botó](images/button-sprite.png)

```blocks3
    quan es fa clic a l'indicador
    mostra

    quan es fa clic a aquest sprite
    ocultar
    emissions (inici v)
```

\--- / tasca \---

El nou codi inclou un altre `emissió`: bloc, que envia el missatge de 'inici' {class = "block3events"}.

El nou codi fa que el botó "Reprodueix" mostri el sprite quan el jugador faci clic a la bandera. Quan el jugador fa clic al botó Sprite, la sprite s'amaga i emet un missatge que altres sprites poden reaccionar.

De moment, el sprite de caràcters comença a fer preguntes quan el jugador fa clic a la bandera. Canvieu el codi del vostre joc perquè el sprite de caràcters comenci a fer preguntes quan rep la "sortida" `emissió`{: class = "block3events"}.

\--- tasca \--- Seleccioneu el vostre sprite de caràcter i, en la seva secció de codi, reemplaça el `quan es fa clic a la bandera`{: class = "block3events"} bloc amb un `quan rebo l'inici`{: class = "block3events" } bloc.

![Sprite de caràcters](images/giga-sprite.png)

```blocks3
<br />- quan es fa clic a la bandera
+ quan rebo [inici v]
conjunt [número 1 v] a (seleccioneu aleatòries (2) a (12))
establir [número 2 v] a (seleccioneu aleatòries (2) a (12) )
pregunteu (uniu-vos (número 1) (uniu-vos [x] (número 2))) i espereu
si &lt;(resposta) = ((nombre 1) * (número 2))&gt; i
    digueu [sí! :)] per (2) segons
més
    digue [nope :(] per (2) segons
final
```

\--- / tasca \---

\--- tasca \---

Feu clic a la bandera verda i, a continuació, feu clic al botó "Reproduir" per comprovar si funciona. Hauríeu de veure que el joc no comença abans de fer clic al botó.

\--- / tasca \---

Pot veure que el temporitzador comença quan es fa clic a la bandera verda, en comptes de quan s'inicia el joc?

![S'ha iniciat el temporitzador](images/brain-timer-bug.png)

\--- tasca \---

Es pot canviar el codi del temporitzador perquè el temporitzador comenci quan el jugador faci clic al botó?

\--- / tasca \---

\--- tasca \--- Afegiu un codi al vostre sprite del botó perquè el botó es mostri novament al final de cada joc.

![Sprite del botó](images/button-sprite.png)

```blocks3
    quan rebo l'exhibició [final v]

```

\--- / tasca \---

\--- tasca \---

Proveu el botó "Reprodueix" jugant un parell de jocs. El botó hauria de mostrar al final de cada joc.

Per provar el joc amb més rapidesa, podeu canviar el valor de `temps`{: class = "block3variables"} perquè cada joc tingui només uns segons de llarg.

![Etapa](images/stage-sprite.png)

```blocks3
    estableixi [temps v] en [10]
```

\--- / tasca \---

\--- tasca \--- Podeu canviar la manera de veure el botó quan el punter del ratolí passa per sobre.

![Botó](images/button-sprite.png)

```blocks3
    quan es fa clic a la bandera
    mostren
    per sempre
    si <touching (mouse-pointer v)?> i
        defineixen [fisheye v] efecte a (30)
    més
        conjunt [fisheye v] efecte a (0)
    final
    final
```

![captura de pantalla](images/brain-fisheye.png) \--- / tasca \---