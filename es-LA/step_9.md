## Desafío: correr hasta 10 puntos

Puedes cambiar tu juego de manera que el jugador, en vez de contestar tantas preguntas como pueda en 30 segundos, conteste 10 preguntas tan rápido como pueda.

Para hacer este cambio, necesitas cambiar el código del temporizador. ¿Puedes ver qué bloques tienen que ser diferentes?

```blocks3
    when I receive [inicio v]
    set [tiempo v] to (30)
    repeat until <(tiempo) = [0]>
        wait (1) seconds
        change [tiempo v] by (-1)
    end
    broadcast (fin v)
```