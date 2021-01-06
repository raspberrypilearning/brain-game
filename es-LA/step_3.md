## Agregar un temporizador

\--- task \---

Crea un temporizador con cuenta regresiva en el escenario con la ayuda de una nueva variable llamada `tiempo`{:class="block3variables"}. El temporizador debería comenzar en 30 segundos y con cuenta regresiva hasta 0 segundos.

![Objeto escenario](images/stage-sprite.png)

\--- hints \---

\--- hint \---

Crea una `variable`{:class="block3variables"}, llámala "tiempo", y dale el valor de `30`.

Luego agrega código para que la variable `tiempo`{:class="block3variables"} baje a 0 en 30 segundos. Para hacer esto, réstale `1` a `tiempo`{:class="block3variables"} cada `1` segundo, y repite esto hasta que `tiempo`{:class="block3variables"} sea igual a `0`.

\--- /hint \---

\--- hint \---

Aquí están los bloques que necesitas:

```blocks3
repeat until < >

end

wait (1) seconds

change [time v] by (1)

(time)

when flag clicked

<() = ()>

set [time v] to [0]
```

\--- /hint \---

\--- hint \---

Así es como tu nuevo código debería verse:

```blocks3
when flag clicked
set [time v] to [30]
repeat until <(time) = (0)>
    wait (1) seconds
    change [time v] by (-1)
end
```

\--- /hint \---

\--- /hints \---

\--- / task \---

\--- task \---

Crea una `transmisión`{:class="block3control"} que envíe el mensaje "fin". Una `transmisión`{:class="block3control"} es como un anuncio que se hace con un altavoz: todos tus personajes lo pueden escuchar. Add the `broadcast`{:class="block3control"} block to the end of the timer code so that the code will send an 'end' message when the `time`{:class="block3variables"} has counted down to `0`.

![Objeto escenario](images/stage-sprite.png)

```blocks3
    broadcast (end v)
```

\--- /task \---

\--- task \---

Selecciona tu personaje y agrega código para que el personaje `detenga los otros objetos`{:class="block3control"} cuando reciba el mensaje `fin`{:class="block3control"}.

![Objeto de Giga](images/giga-sprite.png)

```blocks3
    when I receive [end v]
    stop [other scripts in sprite v]
```

\--- /task \---

\--- task \---

Prueba el juego de nuevo. Este debería continuar haciendo las preguntas hasta que el temporizador llegue a 0.

\--- /task \---