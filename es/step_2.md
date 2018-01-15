## Creando preguntas

Comencemos creando preguntas al azar para que el jugador responda.

+ Empieza un nuevo proyecto de Scratch y borra el objeto gato para que el proyecto esté vacío. Puedes encontrar el editor en línea de Scratch en <a href="http://jumpto.cc/scratch-new" target="_blank">jumpto.cc/scratch-new </a>.

+ Escoge un personaje y un fondo para tu juego. ¡Puedes escoger el que más te guste! Aquí tienes un ejemplo:
    
    ![screenshot](images/brain-setting.png)

+ Crea 2 nuevas variables llamadas `número 1`{:class="blockdata"} y `número 2`{:class="blockdata"}. Estas variables almacenarán los 2 números que se van a multiplicar.
    
    ![screenshot](images/brain-variables.png)

+ Añade código a tu personaje, para fijar estas dos variables a un número `aleatorio`{:class="blockoperators"} entre 2 y 12.
    
    ```blocks
    al presionar bandera verde
    fijar [número 1 v] a (número al azar entre (2) y (12))
    fijar [número 2 v] a (número al azar entre (2) y (12))
```

+ A continuación puedes pedir al jugador que dé una respuesta, y decirle si es correcta o incorrecta.
    
    ```blocks
    al presionar bandera verde
fijar [number 1 v] a (número al azar entre (2) y (12))
fijar [number 2 v] a (número al azar entre (2) y (12))
preguntar (unir (number 1) (unir [x] (number 2))) y esperar
if < (respuesta) = ((number 1) * (number 2)) > then
decir [yes!] :)] por (2) segundos
si no
decir [nope :(] por (2) segundos
fin
```

+ Prueba tu proyecto del todo, dando una respuesta correcta y una incorrecta.

+ Agrega un ` para siempre ` {: class = "blockcontrol"} gira alrededor de este código, de modo que al jugador se le hacen muchas preguntas.

+ Crea un cronómetro de cuenta atrás en el escenario, usando una variable que se llame `tiempo`{:class="blockdata"}. Si necesitas ayuda, ¡el proyecto ‘Globos’ tiene las instrucciones para hacer un cronómetro (en el paso 6)!

+ Vuelve a probar tu proyecto. Deberías de poder continuar haciendo preguntas hasta que se agote el tiempo.