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
quando a bandeira for clicada
altera [time v] para [30]
repete até <(time) = (0)>
    espera (1) segundos
    adiciona a [time v] o valor  (-1)
fim
```

\--- /hint \--- \--- /hints \---

\--- /task \---

\--- task \---

Cria um `difunde a mensagem`{:class="block3control"} que envia a mensagem 'end'. Um ` difunde a mensagem ` {: class = "block3control"} é como um anúncio em um alto-falante: ele pode ser ouvido por todos os seus actores. Adiciona o bloco `difunde a mensagem`{:class="block3control"} ao final do código do temporizador, para que o código envie a mensagem 'end' quando `time`{:class="block3variable"} chega a `0`.

![Stage sprite](images/stage-sprite.png)

```blocks3
    difunde a mensagem (end v)
```

\--- /task \---

\--- Tarefa \--- Seleciona o teu actor e adiciona código para que o actor `pare os outros guiōes`{:class="block3control"} quando recebe a mensagem `end`{:class="block3control"}.

![Giga sprite](images/giga-sprite.png)

```blocks3
    quando receberes a mensagem [end v]
    pára [os teus outros guiões v]
```

\--- /task \---

\--- task \---

Test your game again. It should continue to ask questions until the timer has counted down to 0.

\--- /task \---