## Desafiament: carrera fins a 10 punts

Pots canviar el joc perquè el jugador, en lloc de respondre tantes preguntes com sigui possible en 30 segons, respongui 10 preguntes el més aviat possible.

Per realitzar aquest canvi, només heu de canviar el vostre cronòmetre. Pot veure quins blocs han de ser diferents?

```blocks3
    quan recepció [començar v]
    conjunt [temps v] a (30)
    repetir fins a <(temps) = [0]>
        wait (1) segon
        canvi [temps v] per (-1)
    final
    de difusió (final v)
```