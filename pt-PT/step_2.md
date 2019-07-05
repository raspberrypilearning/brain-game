## Crie perguntas

Vamos começar por criar perguntas aleatórias para o jogador responder.

\--- task \---

Abra um novo projeto Scratch.

**Online:** abre um novo projeto online Scratch em [rpf.io/scratch-new](http://rpf.io/scratchon){:target="_blank"}.

**Offline:** abre um novo projeto no editor offline.

Se precisares de descarregar e instalar o editor do Scratch offline, podes encontrá-lo em [rpf.io/scratchoff](http://rpf.io/scratchoff){:target="_blank"}.

\--- /task \---

\---- task \---- Escolhe um actor e um cenário para o teu jogo. Podes escolher os que quiseres! Aqui está um exemplo:

![captura de ecrã](images/brain-setting.png)

\--- /task \---

\--- Tarefa \--- Certifica-te de que tens o teu actor selecionado. Cria duas novas variáveis, chamadas `number 1`{:class="block3variáveis"} e `number 2`{:class="block3variable"}, para armazenar os números para as perguntas do teste.

![captura de ecrã](images/giga-sprite.png) ![captura de ecrã](images/brain-variables.png)

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- task \--- Adiciona código ao teu actor para definir as variáveis `variáveis`{:class="block3variables"} para um `valor ao acaso`{:class="block3operators"} entre 2 e 12.

![captura de ecrã](images/giga-sprite.png)

```blocks3
quando a bandeira clicada
definir [number 1 v] para (escolha aleatória (2) a (12))
defina [number 2 v] para (escolha aleatória (2) a (12))
```

\--- /task \---

\--- Tarefa \--- Adiciona código para `perguntar`{:class="block3sensing"} ao jogador a resposta, e depois `diz por 2 segundos`{:class="block3look"} se a resposta estava certa ou errada:

![captura de ecrã](images/giga-sprite.png)

```blocks3
quando a bandeira for clicada
definir [number 1 v] para (escolha aleatório (2) para (12))
defina [number 2 v] para (selecionar aleatório (2) para (12))

+ pergunta (a junçāo de (number 1) com (a junçāo de [ x ] com (number 2))) e aguarde
+ se <(resposta) = ((number 1)*(number 2))> , então
+ diga [sim! :)] por (2) segundos
+ senão
+ dizer [não :(] por (2) segundos
+ fim
```

\--- /task \---

\--- task \---

Testa o teu projeto duas vezes: responde uma pergunta corretamente, e a outra incorretamente.

\--- /task \---

\--- task \---

Adiciona um ciclo `repete para sempre`{:class="block3control"} a este código, para que o jogo pergunte muitas questões seguidas ao jogador.

\--- hints \--- \--- hint \---

You need to add a `forever`{:class="block3control"} block, and put all of the code except the `when flag clicked`{:class="block3control"} block into it.

\--- /hint \--- \--- hint \--- Here is the block you need:

```blocks3
forever
end
```

\--- /hint \--- \--- hint \--- Here is what your code should look like:

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

\--- /hint \--- \--- /hints \---

\--- /task \---