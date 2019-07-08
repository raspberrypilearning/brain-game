## Criar perguntas

Vais começar por criar perguntas aleatórias para o jogador responder.

\--- task \---

Abre um projeto Scratch novo.

**Online:** abre um novo projeto online Scratch em [rpf.io/scratch-new](http://rpf.io/scratchon){:target="_blank"}.

**Offline:** abre um novo projeto no editor offline.

Se precisares de descarregar e instalar o editor offline do Scratch, podes encontrá-lo em [rpf.io/scratchoff](http://rpf.io/scratchoff){:target="_blank"}.

\--- /task \---

\---- task \---- Adiciona um actor e um cenário ao teu jogo. Podes escolher os que quiseres! Aqui está um exemplo:

![captura de ecrã](images/brain-setting.png)

\--- /task \---

\--- task \--- Certifica-te de que tens o teu actor selecionado. Cria duas novas variáveis, chamadas `number 1`{:class="block3variáveis"} e `number 2`{:class="block3variable"}, para armazenar os números para as perguntas do teste.

![captura de ecrã](images/giga-sprite.png) ![captura de ecrã](images/brain-variables.png)

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- task \--- Adiciona código ao teu actor para alterar ambas as variáveis `variáveis`{:class="block3variables"} para um `valor ao acaso`{:class="block3operators"} entre 2 e 12.

![captura de ecrã](images/giga-sprite.png)

```blocks3
quando a bandeira for clicada
altera [numero 1 v] para (valor ao acaso entre (2) e (12))
altera [numbero 2 v] para (valor ao acaso entre (2) e (12))
```

\--- /task \---

\--- task\--- Adiciona código para `perguntar`{:class="block3sensing"} ao jogador a resposta, e depois `diz por 2 segundos`{:class="block3looks"} se a resposta estava certa ou errada:

![captura de ecrã](images/giga-sprite.png)

```blocks3
quando a bandeira for clicada
definir [number 1 v] para (escolha aleatório (2) para (12))
defina [number 2 v] para (selecionar aleatório (2) para (12))

+ pergunta (a junçāo de (number 1) com (a junçāo de [ x ] com (number 2))) e aguarde
+ se <(resposta) = ((number 1)*(number 2))> , então
+ diga [certo! :)] por (2) segundos
+ senão
+ dizer [errado :(] por (2) segundos
+ fim
```

\--- /task \---

\--- task \---

Testa o teu projeto duas vezes: responde uma pergunta corretamente, e a outra incorretamente.

\--- /task \---

\--- task \---

Adiciona um ciclo `repete para sempre`{:class="block3control"} a este código, para que o jogo pergunte muitas questões seguidas ao jogador.

\--- hints \--- \--- hint \---

Precisas adicionar um bloco `repete para sempre`{:class="block3control"} e colocar todo o código, exceto o bloco `quando alguém clicar na bandeira`{:class="block3control"}, nele.

\--- / hint \--- \--- hint \--- Aqui está o bloco que precisas:

```blocks3
sempre
fim
```

\--- /hint \--- \--- hint \--- Aqui está como o teu código deve parecer:

```blocks3
quando alguém clicar na bandeira verde

        altera [number 1 v] para (um valor ao acaso entre (2) e (12))
        altera [number 2 v] para (um valor ao acaso entre (2) e (12))
        pergunta (a junção de (number 1) com (a junção de [ x ] com (number 2))) e espera pela resposta
        se <(resposta) = ((number 1) * (number 2))> então 
            diz [certo! :)] por (2) segundos
    senão
        diga [errado :(] por (2) segundos
    termina
termina
```

\--- /hint \--- \--- /hints \---

\--- /task \---