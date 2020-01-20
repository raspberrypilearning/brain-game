## Añadir gráficos

Por ahora el objeto del jugador solo responde `¡sí! :)` o `no :(` a las respuestas del jugador. Añade algunos gráficos para que el jugador sepa si la respuesta es correcta o errónea.

\--- task \---

Crea un nuevo objeto llamado "Resultado" y dale dos disfraces: un "tick" y una "cruz".

![Objeto con los disfraces "tick" y "cruz"](images/brain-result.png)

\--- /task \---

\--- task \---

Cambia el código de tu objeto de personaje para que, en vez de decirle algo al jugador `envíe`{:class="block3events"} los mensajes "correcto" o "incorrecto".

![Objeto de personaje](images/giga-sprite.png)

```blocks3
si <(respuesta) = ((número 1)*(número 2))> entonces

- decir [¡sí! :)] durante (2) segundos
+ enviar (correcto v)
si no
- decir [no :(] durante (2) segundos
+ enviar mensaje (incorrecto v)
fin
```

\--- /task \---

\--- task \---

Ahora puedes usar los mensajes para `mostrar`{:class="block3looks"} los disfraces de "tick" o de "cruz". Añade el siguiente código al objeto "Resultado":

![Objeto de resultado](images/result-sprite.png)

```blocks3
    al recibir [correcto v]
    cambiar disfraz a (tick v)
    mostrar
    esperar (1) segundos
    esconder

    al recibir [incorrecto v]
    cambiar disfraz a (cruz v)
    mostrar
    esperar (1) segundos
    esconder

    al hacer clic en la bandera verde
    esconder
```

\--- /task \---

\--- task \---

Test your game again. You should see the tick whenever you answer a question correctly, and the cross whenever you answer incorrectly!

![Tick for correct, cross for wrong answer](images/brain-test-answer.png)

\--- /task \---

Can you see that the code for `when I receive correct`{:class="block3events"} and `when I receive wrong`{:class="block3events"} is nearly identical?

So you can change your code more easily, you are going to create a custom block.

\--- task \---

Select the 'Result' sprite. Then click on `My Blocks`{:class="block3myblocks"}, and then on **Make a Block**. Create a new block and call it `animate`{:class="block3myblocks"}.

![Result sprite](images/result-sprite.png)

![Create a block called animate](images/brain-animate-function.png)

\--- /task \---

\--- task \---

Move the code to `show`{:class="block3looks"} and `hide`{:class="block3looks"} the 'Result' sprite into the `animate`{:class="block3myblocks"} block:

![Result sprite](images/result-sprite.png)

```blocks3
definir animar
mostrar
esperar (1) segundos
ocultar
```

\--- /task \---

\--- task \---

Make sure you have removed the `show`{:class="block3looks"} and `hide`{:class="block3looks"} blocks below **both** of the `switch costume`{:class="block3looks"} blocks.

Then add the `animate`{:class="block3myblocks"} block below both of the `switch costume`{:class="block3looks"} blocks. Your code should now look like this:

![Result sprite](images/result-sprite.png)

```blocks3
    al recibir [correcto v]
    cambiar disfraz a (tick v)
    animar:: custom

    al recibir [incorrecto v]
    cambiar disfraz a (cruz v)
    animar:: custom
```

\--- /task \---

Because of the custom `animate`{:class="block3myblocks"} block, you now only need to make one change to your code if you want to show the 'Result' sprite's costumes a longer or shorter time.

\--- task \---

Change your code so that the 'tick' or 'cross' costumes display for 2 seconds.

\--- /task \---

\--- task \---

Instead of `showing`{:class="block3looks"} and `hiding`{:class="block3looks"} the 'tick' or 'cross' costumes, you could change your `animate`{:class="block3myblocks"} block so that the costumes fade in.

![Result sprite](images/result-sprite.png)

```blocks3
    definir animar
    dar al efecto [desvanecer v] el valor (100)
    mostrar
    repetir (25)
        sumar al efecto [desvanecer v] (-4)
    fin
    esconder
```

\--- /task \---

Can you improve the animation of the 'tick' or 'cross' graphics? You could add code to make the costumes fade out as well, or you could use other cool effects:

![screenshot](images/brain-effects.png)