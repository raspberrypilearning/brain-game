\--- challenge \---

## Desafío: Carrera hasta 10 puntos

¿Puedes cambiar tu juego para que en lugar de responder tantas preguntas como sea posible en 30 segundos, el jugador vea en cuanto tiempo puede responder 10 preguntas correctas?

Para hacer esto sólo necesitarás cambiar el código del contador de tiempo. ¿Ves lo que hay que cambiar?

```blocks
    al recibir [comienzo v]
    fijar[time v] a (30)
    repetir hasta <(tiempo) = [0]>
        espera (1) seg
        cambiar[time v] por (-1)
    fin
    enviar[end v]
```

\--- /challenge \---