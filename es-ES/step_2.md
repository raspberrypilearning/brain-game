## Crear preguntas

Vas a empezar por crear preguntas aleatorias que el jugador tendrá que contestar.

\--- task \---

Abre un nuevo proyecto en Scratch.

**Online:** open a new online Scratch project at [rpf.io/scratch-new](https://rpf.io/scratch-new){:target="_blank"}.

**Sin conexión:** abre un nuevo proyecto en el editor offline.

If you need to download and install the Scratch offline editor, you can find it at [rpf.io/scratchoff](https://rpf.io/scratchoff){:target="_blank"}.

\--- /task \---

\--- task \---

Añade un personaje y un fondo para tu juego. ¡Puedes escoger el que quieras! Aquí tienes un ejemplo:

![captura de pantalla](images/brain-setting.png)

\--- /task \---

\--- task \---

Asegúrate de tener tu personaje seleccionado. Crea dos nuevas variables llamadas `número 1`{:class="block3variables"} y `número 2`{:class="block3variables"} para almacenar los número de las preguntas del test.

![captura de pantalla](images/giga-sprite.png)

![captura de pantalla](images/brain-variables.png)

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- task \---

Añade código a tu personaje para dar a tus dos `variables`{:class="block3variables"} un número `aleatorio`{:class="block3operators"} entre 2 y 12.

![captura de pantalla](images/giga-sprite.png)

```blocks3
al hacer clic en la bandera
fijar [número 1 v] a (número aleatorio entre (2) y (12))
fijar [número 2 v] a (número aleatorio entre (2) y (12))
```

\--- /task \---

\--- task \---

Añade código a `pregunta`{:class="block3sensing"} el jugador para la respuesta, y luego `decir durante 2 segundos`{:class="block3looks"} si la respuesta era correcta o incorrecta:

![captura de pantalla](images/giga-sprite.png)

```blocks3
al presionar la bandera
 fijar [número 1 v] a (número al azar entre (2) y (12))
  ar [number 2 v] a (número al azar entre(2) y (12))
   tar (une (número 1)(une [ x ] (número 2))) y esperar
    sspuesta) = ((úmero 1)*(número 2))> entonces
        :)] durante (2) segundos
+ si no
+ decir [no :(] durante (2) segundos
+ fin
```

\--- /task \---

\--- task \---

Prueba tu proyecto dos veces: responde una pregunta correctamente, y la otra incorrectamente.

\--- /task \---

\--- task \---

Añade un bucle `continuo`{:class="block3control"} que englobe este código para que el juego haga muchas preguntas seguidas.

\--- hints \---

\--- hint \---

Necesitas añadir un bloque `continuo`{:class="block3control"}, y poner todo el código excepto el bloque `al hacer clic en bandera`{:class="block3control"}.

\--- /hint \---

\--- hint \---

Éste es el bloque que necesitas:

```blocks3
continuo
fin
```

\--- /hint \---

\--- hint \---

Así debería ser tu código:

```blocks3
al seleccionar la bandera
+ continuo
    dar a [número 1 v] el valor (número aleatorio entre (2) y (12))
    dar a [número 2 v] el valor (número aleatorio entre (2) y (12))
    preguntar (unir (número 1)(unir [ x ] (número 2))) y esperar
    si <(respuesta) = ((número 1)*(número 2))> entonces
        decir [¡sí! :)] durante (2) segundos
    sino
        decir [no :(] durante (2) segundos
    end
end
```

\--- /hint \---

\--- /hints \---

\--- /task \---