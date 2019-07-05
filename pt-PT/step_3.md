## Adicionar temporizador

\--- Tarefa \--- Cria um temporizador de contagem regressiva no palco com a ajuda de uma nova variável chamada `time`{:class="block3variable"}. O temporizador deve começar em 30 segundos e contar até 0 segundos.

![Stage sprite](images/stage-sprite.png)

\--- hints \--- \--- hint \---

Cria uma `variável`{:class="block3variables"}, nomeia-a 'time', e define o valor para `30`.

Em seguida, adiciona código para diminuir `time` {: class = "block3variables"} até 0 em 30 segundos. Para fazer isso, subtrai `1` de `time`{:class="block3variables"} a cada `1` segundo, e repete até `time`{:class="block3variables"} igual a `0`.

\--- /hint \--- \--- hint \--- Aqui estão os blocos que precisas:

```blocks3
repita até < >

final

espera (1) segundos

altere [time v] por (1)

(time)

quando a bandeira for clicada

<() = ()>

defina [time v] para [0]
```

\--- /hint \--- \--- hint \--- Aqui está o que seu novo código deve parecer:

```blocks3
when flag clicked
set [time v] to [30]
repeat until <(time) = (0)>
    wait (1) seconds
    change [time v] by (-1)
end
```

\--- /hint \--- \--- /hints \---

\--- /task \---

\--- task \---

Create a `broadcast`{:class="block3control"} that sends the message 'end'. A `broadcast`{:class="block3control"} is like an announcement over a loudspeaker: it can be heard by all of your sprites. Add the `broadcast`{:class="block3control"} block to the end of the timer code so that the code will send and 'end' message when the `time`{:class="block3variables"} has counted down to `0`.

![Stage sprite](images/stage-sprite.png)

```blocks3
    broadcast (end v)
```

\--- /task \---

\--- task \--- Select your character sprite and add some code so that the sprite `stops the other scripts`{:class="block3control"} when it receives the `end`{:class="block3control"} message.

![Giga sprite](images/giga-sprite.png)

```blocks3
    Quando receberes a mensagem [acabar v]
    pára [os teus outros guiões v]
```

\--- /task \---

\--- task \---

Test your game again. It should continue to ask questions until the timer has counted down to 0.

\--- /task \---