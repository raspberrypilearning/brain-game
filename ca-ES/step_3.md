## Afegiu un temporitzador

\--- tasca \--- Crea un temporitzador de compte enrere a l'Estadi amb l'ajuda d'una nova variable anomenada `vegada`{: class = "block3variables"}. El temporitzador ha de començar a 30 segons i comptar fins a 0 segons.

![Sprite d'etapa](images/stage-sprite.png)

\--- consells \--- \--- suggeriment \---

Crear un `variable d'`{: class = "block3variables"}, en diuen 'temps' i estableixi el seu valor a `30`.

A continuació, afegiu el codi per comptar `temps`{: class = "block3variables"} fins a 0 en 30 segons. Per a això, restar `1` des `temps`{: class = "block3variables"} cada `1` En segon lloc, i repetir això fins `temps`{: class = "block3variables"} és igual a `0`.

\--- / indici \--- \--- indici \--- Aquests són els blocs que necessiteu:

```blocks3
repetiu fins a < >

final

espera (1) segons

canvi [temps v] per (1)

(temps)

quan es fa clic a la bandera

<() = ()>

fixar [temps v] a [0]
```

\--- / indici \--- \--- suggeriment \--- Aquí teniu el que hauria de tenir el vostre nou codi:

```blocks3
quan l'indicador fa clic a
estableix [temps v] a [30]
repeteix fins a <(temps) = (0)>
    espera (1) segons
    canvia [hora v] per (-1)
final
```

\--- / indici \--- \--- / indicacions \---

\--- / tasca \---

\--- tasca \---

Crear un `emissió`{: class = "block3control"} que envia el missatge 'fi'. A `broadcast`{: class = "block3control"} és com un anunci sobre un altaveu: tots els sprites poden escoltar-lo. Afegiu-hi el `emissió`{: class = "block3control"} bloquejar al final del codi de temporitzador perquè el codi va a enviar i missatge de 'fi' quan el `temps`{: class = "block3variables"} ha comptat fins `0`.

![Sprite d'etapa](images/stage-sprite.png)

```blocks3
    emissió (final v)
```

\--- / tasca \---

\--- tasca \--- Seleccioneu el vostre caràcter de sprite i afegiu un codi perquè la sprite `atura els altres scripts`{: class = "block3control"} quan rebi el missatge `end`{: class = "block3control"} .

![Giga sprite](images/giga-sprite.png)

```blocks3
    quan rebo [final v]
    stop [altres scripts en sprite v]
```

\--- / tasca \---

\--- tasca \---

Torneu a provar el joc. Hauria de continuar fent preguntes fins que el cronòmetre hagi baixat fins a 0.

\--- / tasca \---