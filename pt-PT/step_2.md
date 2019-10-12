## Criar perguntas

Vais começar por criar perguntas aleatórias para o jogador responder.

\--- task \---

Abre um projeto Scratch novo.

**Online:** abre um novo projeto Scratch em [rpf.io/scratch-new](http://rpf.io/scratch-new){:target="_blank"}.

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

\--- task \--- Adiciona código ao teu actor para alterar ambas as `variáveis`{:class="block3variables"} para um `valor ao acaso`{:class="block3operators"} entre 2 e 12.

![captura de ecrã](images/giga-sprite.png)

```blocks3
when flag clicked
set [number 1 v] to (pick random (2) to (12))
set [number 2 v] to (pick random (2) to (12))
```

\--- /task \---

\--- task\--- Adiciona código para `perguntar`{:class="block3sensing"} ao jogador a resposta, e depois `diz por 2 segundos`{:class="block3looks"} se a resposta estava certa ou errada:

![captura de ecrã](images/giga-sprite.png)

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

Testa o teu projeto duas vezes: responde uma pergunta corretamente, e a outra incorretamente.

\--- /task \---

\--- task \---

Adiciona um ciclo `repete para sempre`{:class="block3control"} a este código, para que o jogo pergunte muitas questões seguidas ao jogador.

\--- hints \--- \--- hint \---

Precisas adicionar um bloco `repete para sempre`{:class="block3control"} e colocar todo o código, exceto o bloco `quando alguém clicar na bandeira`{:class="block3control"}, dentro dele.

\--- / hint \--- \--- hint \--- Aqui está o bloco que precisas:

```blocks3
forever
end
```

\--- /hint \--- \--- hint \--- Aqui está como o teu código deve parecer:

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