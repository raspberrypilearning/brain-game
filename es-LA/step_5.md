## Varias partidas

Ahora vas a agregar un botón "Jugar", para que el jugador pueda jugar el juego muchas veces.

--- task ---

Crea un nuevo botón objeto "Jugar" para que el jugador haga clic y empiece un nuevo juego.

Puedes dibujar el objeto tú mismo, o editar un objeto de la librería.

![Imagen del botón de jugar](images/brain-play.png)

--- /task ---

--- task ---

Agrega este código al botón objeto:

![Objeto del botón](images/button-sprite.png)

```blocks3
    when flag clicked
    show

    when this sprite clicked
    hide
    broadcast (inicio v)
```

--- /task ---

El nuevo código incluye otro bloque de `transmisión`{:class="block3events"}, el cual envía el mensaje "inicio".

El nuevo código hace que el botón objeto "Jugar" aparezca cuando el jugador hace clic en la bandera. Cuando el jugador hace clic en el botón objeto, el objeto se oculta y luego transmite un mensaje a la que otros objetos pueden reaccionar.

Por el momento, el objeto empieza a hacer preguntas cuando el jugador hace clic en la bandera. Cambia el código de tu juego para que el objeto empiece a hacer preguntas cuando reciba la `transmisión`{:class="block3events"} "inicio".

--- task ---

Selecciona el objeto y, en la sección del código, reemplazar el bloque de `al hacer clic en la bandera`{:class="block3events"} con un bloque `al recibir inicio`{:class="block3events"}.

![Objeto del personaje](images/giga-sprite.png)

```blocks3
- when flag clicked
+ when I receive [inicio v]
set [número 1 v] to (pick random (2) to (12))
set [número 2 v] to (pick random (2) to (12))
ask (join (número 1)(join [ x ] (número 2))) and wait
if <(answer) = ((número 1)*(número 2))> then
    say [¡sí! :)] for (2) seconds
else
    say [nope :(] for (2) seconds
end
```

--- /task ---

--- task ---

Haz clic en la bandera verde, y después en el nuevo botón "Jugar" para ver si funciona. Deberías notar que el juego no empieza antes de que hagas clic en el botón.

--- /task ---

¿Puedes ver que el temporizador empieza al hacer clic en la bandera verde, y no cuando el juego empieza?

![El cronómetro ha comenzado](images/brain-timer-bug.png)

--- task ---

¿Puedes cambiar el código del temporizador para que este empiece cuando el jugador haga clic en el botón?

--- / task ---

--- task ---

Agrega un código al botón objeto para que este se muestre de nuevo al final de cada partida.

![Objeto del botón](images/button-sprite.png)

```blocks3
    when I receive [fin v]
    show
```

--- /task ---

--- task ---

Prueba el botón "Jugar" jugando un par de partidas. El botón debería aparecer al final de cada partida.

Para probar el juego más rápido, puedes cambiar el valor de `tiempo`{:class="block3variables"} para que cada partida dure solo pocos segundos.

![Escenario](images/stage-sprite.png)

```blocks3
    set [tiempo v] to [10]
```

--- /task ---

--- task ---

Puedes cambiar el aspecto del botón cuando el puntero del mouse pase por encima.

![Botón](images/button-sprite.png)

```blocks3
    when flag clicked
    show
    forever
    if <touching (mouse-pointer v)?> then
        set [fisheye v] effect to (30)
    else
        set [fisheye v] effect to (0)
    end
    end
```

![captura de pantalla](images/brain-fisheye.png)

--- /task ---