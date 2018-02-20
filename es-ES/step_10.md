\--- challenge \---

## Challenge: Carrera hasta 10 puntos

¿Puede cambiar su nombre, así que en lugar de responder tantas preguntas como sea posible en 30 segundos, el jugador tenga que ver cómo rápidamente puede obtener 10 preguntas correctas?

Para hacer esto, solo necesitará cambiar su código de temporizador. ¿Puede ver lo que necesita ser cambiado?

```blocks
    when I receive [start v]
    set [time v] to (30)
    repeat until <(time) = [0]>
        wait (1) secs
        change [time v] by (-1)
    end
    broadcast [end v]
```

\--- /challenge \---