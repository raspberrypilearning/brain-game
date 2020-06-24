## Añadir un cronómetro

\--- task \---

Crea un cronómetro para una cuenta atrás en el Escenario con la ayuda de una nueva variable llamada `tiempo`{:class="block3variables"}. El cronómetro debería empezar en 30 segundos y hacer una cuenta atrás hasta 0.

![Objeto escenario](images/stage-sprite.png)

\--- hints \---

\--- hint \---

Crea una `variable`{:class="block3variables"}, llámala "tiempo" y dale el valor `30`.

Después añade código para hacer que el valor de `tiempo`{:class="block3variables"} llegue a 0 en 30 segundos. Para hacerlo, réstale `1` a `tiempo`{:class="block3variables"} cada `1` segundo. Repítelo hasta que `tiempo`{:class="block3variables"} sea igual a `0`.

\--- /hint \---

\--- hint \---

Aquí están los bloques que necesitas:

```blocks3
repetir hasta que < >

fin

esperar (1) segundos

sumar a [tiempo v] (1)

(tiempo)

al hacer clic en la bandera

<() = ()>

dar a [tiempo v] el valor [0]
```

\--- /hint \---

\--- hint \---

El código debería quedar así ahora:

```blocks3
al hacer clic en la bandera
dar a [tiempo v] el valor [30]
repetir hasta que <(tiempo) = (0)>
    esperar (1) segundos
    sumar a [tiempo v] (-1)
fin
```

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

Crea una `transmisión`{:class="block3control"} que envíe el mensaje "terminar". Utiliza el bloque <0>enviar</0>{:class="block3events"} para enviar transmisiones. Una `transmisión`{:class="block3control"} es como un anuncio que se hace con un altavoz: todos los objetos lo pueden escuchar. Añade el bloque `enviar`{:class="block3control"} al final del código del cronómetro para que el código envíe el mensaje "terminar" cuando el `tiempo`{:class="block3variables"} llegue a `0`.

![Objeto escenario](images/stage-sprite.png)

```blocks3
    transmisión (terminar v)
```

\--- /task \---

\--- task \---

Selecciona tu personaje y añade algo de código para que el objeto `detenga los otros scripts`{:class="block3control"} cuando reciba el mensaje `end`{:class="block3control"}.

![Objeto de Giga](images/giga-sprite.png)

```blocks3
    al recibir [terminar v]
    detener[otros programas en el objeto v]
```

\--- /task \---

\--- task \---

Prueba tu juego otra vez. Debería hacer preguntas hasta que el cronómetro llegue a 0.

\--- /task \---