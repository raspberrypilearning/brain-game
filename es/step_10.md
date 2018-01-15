\--- challenge \---

## Desafío: Corre por 10 puntos

¿Puedes cambiar tu juego para que el jugador, en lugar de contestar tantas preguntas como pueda en 30 segundos, vea cuánto tiempo necesita para conseguir 10 respuestas correctas?

Para hacer esto, sólo tendrás que cambiar el código del cronómetro. ¿Ves lo que necesitas cambiar?

```blocks
    al recibir [start v]
fijar [hora v] a (30)
repetir hasta que <(time) = [0]> 
  esperar (1) segundos
  cambiar [hora v] por (-1)
end
enviar [end v]
```

\--- /challenge \---