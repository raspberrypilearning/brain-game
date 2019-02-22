## Afegeix gràfics

De moment, el sprite del personatge només diu `sí! :)` o `no :(` a les respostes del jugador. Afegiu alguns gràfics per permetre al jugador saber si la seva resposta és correcta o incorrecta.

\--- tasca \---

Creeu un nou sprite anomenat 'Resultat', i doneu-li un 'tick / check' i un vestit 'cross'.

![Sprite amb disfresses i taques](images/brain-result.png)

\--- / tasca \---

\--- tasca \---

Canvieu el codi del vostre personatge Sprite perquè, en lloc de dir alguna cosa al jugador, `emet`{: class = "block3events"} els missatges "correctes" o "incorrectes".

![Sprite de caràcters](images/giga-sprite.png)

```blocks3
si <(resposta) = ((número 1) * (número 2))> després

- digueu [sí! :)] per a (2) segons
+ emissió (correcte v)
més
- digue [nope :(] per (2) segons
+ emissió (v incorrecta)
final
```

\--- / tasca \---

\--- tasca \---

Ara podeu utilitzar aquests missatges a `mostrar`{: class = "block3looks"} la marca "tick" o "cross". Afegiu el següent codi al sprite "Resultat":

![Sprite de resultats](images/result-sprite.png)

```blocks3
    quan rebo [v correcte]
    canvia de disfressa a (tick v)
    mostra
    espera (1) segons
    ocultar

    quan rebo [v incorrecta]
    canviar de disfressa a (creu v)
    mostra
    espera (1) segons
    amaga

    quan es fa clic a la bandera
    esculpeu
```

\--- / tasca \---

\--- tasca \--- Torneu a provar el joc. Hauríeu de veure la marca cada vegada que responeu una pregunta correctament, i la creu sempre que us respongui incorrectament.

![Marqueu la resposta correcta, creu per incorrecta](images/brain-test-answer.png)

\--- / tasca \---

Pot veure que el codi de `quan rebo correctament`{: class = "block3events"} i `quan rebo incorrecte`{: class = "block3events"} és gairebé idèntic?

Per tant, podeu canviar el codi amb més facilitat, es crearà un bloc personalitzat.

\--- tasca \---

Seleccioneu el sprite "Resultats". A continuació, feu clic a `My Blocks`{: class = "block3myblocks"} i, a continuació, a **Faci un bloc**. Creeu un bloc nou i anomeneu `animate`{: class = "block3myblocks"}.

![Sprite de resultats](images/result-sprite.png)

![Creeu un bloc anomenat animate](images/brain-animate-function.png)

\--- / tasca \---

\--- tasca \--- moure el codi a `espectacle`{: class = "block3looks"} i `Amaga`{: class = "block3looks"} el sprite 'resultat' al `animat`{: class = " block3myblocks "} bloc:

![Sprite de resultats](images/result-sprite.png)

```blocks3
define animate
show
wait (1) seconds
hide
```

\--- / tasca \---

\--- tasca \--- Assegureu-vos que heu eliminat l' `show`{: class = "block3looks"} i `oculteu`blocs {: class = "block3looks"} per sota de **tant** del `switch suit`{: blocs class = "block3looks"}.

A continuació, afegir el `animat`{: class = "block3myblocks"} bloc per sota tant de la `vestit interruptor`{: class = "block3looks"} blocs. Ara el codi hauria de ser així:

![Sprite de resultats](images/result-sprite.png)

```blocks3
    quan rebo [v correcte]
    canvia de disfressa a (tick v)
    animi :: custom

    quan rebo [v incorrecta]
    switch suit to (cross v)
    animate :: custom
```

\--- / tasca \---

A causa del bloqueig personalitzat `animate`{: class = "block3myblocks"}, ara només heu de fer un canvi al vostre codi si voleu mostrar el costum del sprite de "Resultat" un temps més llarg o curt.

\--- tasca \---

Canvieu el codi per tal que la disfressa "tick" o "cross" es mostri durant 2 segons.

\--- / tasca \---

\--- \--- tasca en lloc de `mostrant`{: class = ""} block3looks i `s'amaguen`{: class = ""} block3looks el 'tick' o vestits 'creuades', que podria canviar la seva `animat`{: class = "block3myblocks"} bloqueja perquè es desapareguin els vestits.

![Sprite de resultats](images/result-sprite.png)

```blocks3
    defineix animate
    set [ghost v] effect to (100)
    show
    repeat (25)
        change [ghost v] effect by (-4)
    end
    hide
```

\--- / tasca \---

Es pot millorar l'animació dels gràfics "tick" o "cross"? Podeu afegir codi per fer que les disfresses també es desapareixin o podeu utilitzar altres efectes genials:

![captura de pantalla](images/brain-effects.png)