## Criar perguntas

Vamos começar criando perguntas aleatórias para o jogador responder.

\--- task \---

Abra um novo projeto Scratch.

**Online:** abra um novo projeto online de Scratch em [rpf.io/scratch-new](http://rpf.io/scratch-new){:target="_blank"}.

**Offline:** abra um novo projeto no editor offline.

Se você precisar baixar e instalar o editor offline do Scratch, poderá encontrá-lo em [rpf.io/scratchoff](http://rpf.io/scratchoff){:target="_blank"}.

\--- /task \---

\--- task \---

Escolha um ator de personagem e um cenário para o seu jogo. Você pode escolher o que você quiser! Aqui está um exemplo:

![screenshot](images/brain-setting.png)

\--- /task \---

\--- task \---

Certifique-se de ter selecionado o seu ator de personagem. Crie duas novas variáveis, chamadas `número 1`{:class="block3variables"} e `número 2`{:class="block3variables"}, para armazenar os números para as perguntas do teste.

![screenshot](images/giga-sprite.png)

![screenshot](images/brain-variables.png)

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- task \---

Adicione código ao seu ator de personagem para definir ambas as `variáveis`{:class="block3variables"} ​​para um número `aleatório`{:class="block3operators"} entre 2 e 12.

![screenshot](images/giga-sprite.png)

```blocks3
when flag clicked
set [number 1 v] to (pick random (2) to (12))
set [number 2 v] to (pick random (2) to (12))
```

\--- /task \---

\--- task \---

Adicione código para `perguntar`{:class="block3sensing"} ao jogador a resposta, e então `diga durante 2 segundos`{:class="block3looks"} se a resposta está certa ou errada:

![screenshot](images/giga-sprite.png)

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

Teste seu projeto duas vezes: responda uma pergunta corretamente e a outra incorretamente.

\--- /task \---

\--- task \---

Adiciona um ciclo `sempre`{:class="block3control"} a este código, para que o jogo pergunte muitas questões seguidas ao jogador.

\--- hints \---

\--- hint \---

Você precisa adicionar um bloco `sempre`{:class="block3control"} e colocar todo o código exceto o bloco `quando bandeira for clicado`{:class="block3control"} dentro dele.

\--- /hint \---

\--- hint \---

Aqui está o bloco que você precisa:

```blocks3
forever
end
```

\--- /hint \---

\--- hint \---

É assim que seu código deve estar:

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