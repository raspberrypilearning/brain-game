## Adicionar um temporizador

--- task --- Cria um temporizador de contagem regressiva no palco com a ajuda de uma nova variável chamada `tempo`{:class="block3variable"}. O temporizador deve começar em 30 segundos e contar até 0 segundos.

![Actor do palco](images/stage-sprite.png)

--- hints ---
 --- hint ---

Cria uma `variável`{:class="block3variables"}, nomeia-a 'tempo', e define o valor para `30`.

Em seguida, adiciona código para diminuir `tempo`{:class="block3variables"} até 0 em 30 segundos. Para fazer isso, subtrai `1` de `tempo`{:class="block3variables"} a cada `1` segundo, e repete até `tempo`{:class="block3variables"} igual a `0`.

--- /hint --- --- hint --- Aqui estão os blocos que precisas:

```blocks3
espera (1) s

adiciona a [tempo v] o valor (1)

tempo :: variables

Quando alguém clicar na bandeira verde

<() = ()>

altera [tempo v] para [0]

até que <> , repete
```

--- /hint --- --- hint --- Aqui está o aspeto que o teu novo código deve ter:

```blocks3
Quando alguém clicar na bandeira verde
altera [tempo v] para [30]
até que <(tempo :: variables) = (0)> , repete 
  espera (1) s
  adiciona a [tempo v] o valor (-1)
```

--- /hint --- --- /hints ---

--- /task ---

--- task ---

Cria um bloco `difunde a mensagem`{:class="block3control"} que envia a mensagem 'acabar'. Um `difunde a mensagem`{:class="block3control"} é como um anúncio em um alto-falante: ele pode ser ouvido por todos os teus actores. Adiciona o bloco `difunde a mensagem`{:class="block3control"} ao final do código do temporizador, para que o código envie a mensagem 'acabar' quando `tempo`{:class="block3variable"} chegar a `0`.

![Actor do palco](images/stage-sprite.png)

```blocks3
    difunde a mensagem (acabar v)
```

--- /task ---

--- task --- Seleciona o teu actor e adiciona código para que o actor `pare os outros guiōes`{:class="block3control"} quando recebe a mensagem `acabar`{:class="block3control"}.

![Actor Giga](images/giga-sprite.png)

```blocks3
    quando receberes a mensagem [acabar v]
    pára [os teus outros guiões v]
```

--- /task ---

--- task ---

Testa o teu jogo novamente. Deve continuar a fazer perguntas até que o temporizador tenha contado até 0.

--- /task ---