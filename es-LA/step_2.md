## Crear preguntas

Vas a empezar por crear preguntas aleatorias que el jugador tiene que responder.

\--- task \---

Abre un nuevo proyecto de Scratch.

**Online:** open a new online Scratch project at [rpf.io/scratch-new](https://rpf.io/scratch-new){:target="_blank"}.

** Offline: ** Abre un nuevo proyecto en el editor offline.

If you need to download and install the Scratch offline editor, you can find it at [rpf.io/scratchoff](https://rpf.io/scratchoff){:target="_blank"}.

\--- task \---

\--- task \---

Agrega un personaje y un fondo para tu juego. ¡Puedes elegir el que gustes! Aquí tienes un ejemplo:

![captura de pantalla](images/brain-setting.png)

\--- /task \---

\--- task \---

Asegúrate que tienes tu personaje seleccionado. Crea dos nuevas variables, llamadas `número 1`{:class="block3variables"} y `número 2`{:class="block3variables"}, para almacenar los números de las preguntas de la prueba.

![captura de pantalla](images/giga-sprite.png)

![captura de pantalla](images/brain-variables.png)

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- task \---

Agrega código a tu personaje para dar a ambas `variables`{:class="block3variables"} un número `aleatorio`{:class="block3operators"} entre 2 y 12.

![captura de pantalla](images/giga-sprite.png)

```blocks3
when flag clicked
set [number 1 v] to (pick random (2) to (12))
set [number 2 v] to (pick random (2) to (12))
```

\--- /task \---

\--- task \---

Agrega código para `preguntar`{:class="block3sensing"} al jugador por la respuesta, y luego `decir por dos segundos`{:class="block3looks"} si la respuesta fue correcta o incorrecta:

![captura de pantalla](images/giga-sprite.png)

```blocks3
when flag clicked
set [number 1 v] to (pick random (2) to (12))
set [number 2 v] to (pick random (2) to (12))

+ ask (join (number 1)(join [ x ] (number 2))) and wait
+ if <(answer) = ((number 1)*(number 2))> then
+ say [yes! :)] for (2) seconds
+ else
+ say [no :(] for (2) seconds
+ end
```

\--- /task \---

\--- task \---

Prueba tu proyecto dos veces: responde una respuesta correctamente, y otra incorrectamente.

\--- /task \---

\--- task \---

Agrega un bucle `infinito`{:class="block3control"} que englobe este código, para que el juego haga muchas preguntas seguidas al jugador.

\--- hints \---

\--- hint \---

Necesitas agregar un bloque `infinito`{:class="block3control"}, y poner todo el código excepto el bloque `al hacer click en la bandera`{:class="block3control"}.

\--- /hint \---

\--- hint \---

Aquí está el bloque que necesitas:

```blocks3
forever
end
```

\--- /hint \---

\--- hint \---

Tu código debería lucir así:

```blocks3
when flag clicked

+ forever
    set [number 1 v] to (pick random (2) to (12))
    set [number 2 v] to (pick random (2) to (12))
    ask (join (number 1)(join [ x ] (number 2))) and wait
    if <(answer) = ((number 1)*(number 2))> then
        say [yes! :)] for (2) seconds
    else
        say [no :(] for (2) seconds
    end
end
```

\--- /hint \---

\--- /hints \---

\--- /task \---