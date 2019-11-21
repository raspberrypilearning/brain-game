## Desafío: Carrera hasta 10 puntos

¿Puedes cambiar tu juego de manera que en vez de contestar tantas preguntas como pueda en 30 segundos el jugador tenga que contestar 10 preguntas tan rápido como pueda?

Para hacerlo solo tienes que cambiar el código del cronómetro. ¿Ves qué bloques tienen que ser diferentes?

```blocks3
    al recibir [empezar v]
    dar a [tiempo v] el valor (30)
    repetir hasta que <(tiempo) = [0]>
        esperar (1) segundos
        sumar a [tiempo v] (-1)
    fin
    enviar (final v)
```