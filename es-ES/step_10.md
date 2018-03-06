--- challenge ---
## Desafío: Corre por 10 puntos
¿Puedes cambiar tu juego para que el jugador, en lugar de contestar tantas preguntas como pueda en 30 segundos, vea cuánto tiempo necesita para conseguir 10 respuestas correctas?

Para hacer esto, sólo tendrás que cambiar el código del cronómetro. ¿Ves lo que necesitas cambiar?

```blocks
	al recibir [inicio v]
	fijar [tiempo v] a (30)
	repetir hasta que <(tiempo) = [0]>
   		esperar (1) segundos
   		cambiar [tiempo v] por (-1)
	fin
	enviar [fin v]
```




--- /challenge ---