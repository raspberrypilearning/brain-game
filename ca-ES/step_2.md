## Crea preguntes

Començaràs creant preguntes aleatòries que el jugador ha de respondre.

\--- tasca \---

Obriu un nou projecte Scratch.

**Online:** open a new online Scratch project at [rpf.io/scratch-new](http://rpf.io/scratch-new){:target="_blank"}.

**Desconnectat:** obre un nou projecte a l'editor fora de línia.

Si necessiteu descarregar i instal·lar l'editor Scratch offline, podeu trobar-lo a [rpf.io/scratchoff](http://rpf.io/scratchoff){: target = "_ blank"}.

\--- / tasca \---

\--- tasca \--- Afegiu un sprite de caràcter i un teló de fons per al vostre joc. Podeu triar qualsevol que vulgueu! Aquí teniu un exemple:

![captura de pantalla](images/brain-setting.png)

\--- / tasca \---

\--- tasca \--- Assegureu-vos que heu seleccionat el vostre sprite del caràcter. Creeu dues variables noves, anomenades `número 1`{: class = "block3variables"} i `número 2`{: class = "block3variables"}, per emmagatzemar els números de les preguntes del qüestionari.

![captura de pantalla](images/giga-sprite.png) ![captura de pantalla](images/brain-variables.png)

[[[generic-scratch3-add-variable]]]

\--- / tasca \---

\--- \--- tasca Afegir codi al seu sprite de caràcter per definir tant de les `variables de`{: class = ""} block3variables a uns `aleatòries`{: class = "block3operators"} nombre entre 2 i 12.

![captura de pantalla](images/giga-sprite.png)

```blocks3
quan l'indicador fa clic a
estableix [número 1 v] a (seleccioneu aleatòries (2) a (12))
conjunt [número 2 v] a (seleccioneu aleatòries (2) a (12))
```

\--- / tasca \---

\--- tasca \--- Afegiu un codi a `pregunta`: {: class = "block3sensing"} el jugador de la resposta i, a continuació, `per 2 segons`{: class = "block3looks"} si la resposta era correcta o mal:

![captura de pantalla](images/giga-sprite.png)

```blocks3
quan l'indicador fa clic a
estableix [número 1 v] a (seleccioneu aleatòries (2) a (12))
conjunt [número 2 v] a (seleccioneu aleatòries (2) a (12))

+ pregunteu (uniu-vos (número 1) (uniu-vos [x] (número 2))) i espereu
+ si <(resposta) = ((número 1) * (número 2))> i
+ digueu [sí! :)] per (2) segons
+ més
+ dir [no :(] per (2) segons
+ final
```

\--- / tasca \---

\--- tasca \---

Proveu el vostre projecte dues vegades: responeu una pregunta correctament i l'altra incorrectament.

\--- / tasca \---

\--- tasca \---

Afegiu `per sempre`{: class = "block3control"} loop al voltant d'aquest codi, de manera que el joc demana al jugador moltes preguntes seguides.

\--- consells \--- \--- suggeriment \---

Heu d'afegir un bloc `per sempre`{: class = "block3control"} i posar tot el codi, excepte el `quan el bloc hagi fet clic a`blocs {: class = "block3control"}.

\--- / indici \--- \--- indici \--- Aquí teniu el bloc que necessiteu:

```blocks3
per sempre
final
```

\--- / indici \--- \--- indici \--- Aquí teniu el que hauria de tenir el vostre codi:

```blocks3
quan es fa clic a la bandera

+ per sempre
    conjunt [número 1 v] a (seleccioneu aleatòries (2) a (12))
    conjunt [número 2 v] a (seleccioneu aleatòries (2) a (12))
    pregunteu (uniu-vos (nombre 1) (uniu-vos [x] (número 2)) i espereu
    si <(resposta) = ((número 1) * (número 2))> i
        digueu [sí! :)] durant (2) segons
    més
        digue [no :(] per (2) segons
    final
final
```

\--- / indici \--- \--- / indicacions \---

\--- / tasca \---