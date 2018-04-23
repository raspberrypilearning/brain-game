--- challenge ---

## Desafío: Carrera hasta 10 puntos

¿Puedes cambiar tu juego para que en lugar de responder tantas preguntas como sea posible en 30 segundos, el jugador vea en cuanto tiempo puede responder 10 preguntas correctas?

Para hacer esto sólo necesitarás cambiar el código del contador de tiempo. ¿Ves lo que hay que cambiar?

```blocks
al recibir [start v]
fijar [hora v] a (30)
repetir hasta que <(tiempo) = [0]> 
  esperar (1) segundos
  cambiar [hora v] por (-1)
end
enviar [fin v]
```

--- /challenge ---
