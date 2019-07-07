## Adicionar gráficos

De momento, o actor do personagem só diz `certo! :)` ou `errado :(` às respostas do jogador. Adiciona alguns gráficos para informar o jogador se sua resposta está correta ou incorreta.

\--- task \---

Cria um novo actor com o nome ‘resultado’, que contenha os trajes de ‘correcto’ e ‘incorrecto’.

![Sprite with tick and cross costumes](images/brain-result.png)

\--- /task \---

\--- task \---

Altera o código do teu actor personagem para que, em vez de dizer algo ao jogador, ele `difunda as mensagem`{:class="block3events"} 'correto' ou 'errado'.

![Character sprite](images/giga-sprite.png)

```blocks3
se <(resposta) = ((numero 1) * (numero 2))> entao

- diga [certo! :)] para (2) segundos
+ broadcast (v correto)
else
- diga [errado :(] para (2) segundos
+ broadcast (v errado)
end
```

\--- /task \---

\--- task \---

Agora podes usar estas mensagens para `mostrar`{:class="block3look"} o traje 'correto' ou 'incorrecto'. Adiciona o seguinte código ao actor 'Resultado':

![Result sprite](images/result-sprite.png)

```blocks3
    quando recebo [correto v]
    alterna o traje para (tick v)
    show
    wait (1) segundos
    ocultar

    quando recebo [v errado]
    alterna o traje para (cruz v)
    show
    wait (1) segundos
    ocultar

    quando alguém clicar na bandeira 
    ocultar
```

\--- /task \---

\--- task \--- Testa o teu jogo novamente. Deves ver o certo sempre que responderes uma pergunta corretamente e a errado sempre que responderes incorretamente!

![Tick for correct, cross for wrong answer](images/brain-test-answer.png)

\--- /task \---

Notaste que o código para ` quando receberes a mensagem correto` {: class = "blockevents"} e ` quando receberes a mensagem a incorreto` {: class = "blockevents"} é quase idêntico?

Então para poderes alterar o teu código mais facilmente, vais criar um bloco personalizado.

\--- task \---

Seleciona o actor 'Resultado'. Depois clica em `Meus Blocos`{:class="block3myblocks"}, e depois em **Criar um Bloco**. Cria um bloco novo e chama-lhe `animar`{:class="block3myblocks"}.

![Result sprite](images/result-sprite.png)

![Create a block called animate](images/brain-animate-function.png)

\--- /task \---

\--- task \--- Move o código para `mostra-te`{:class="block3look"} e `esconde-te`{:class="block3look"} do actor 'Resultado' para o bloco `animar`{:class="block3myblocks"}:

![Result sprite](images/result-sprite.png)

```blocks3
definir animar
mostra-te
espera (1) segundos
esconde-te
```

\--- /task \---

\--- task \--- Certifica-te de que removeste os blocos `mostra-te`{:class="block3look"} e `esconde-te`{:class="block3look"} abaixo de **ambos** os blocos `muda o teu traje`{:class="block3look"}.

Em seguida adiciona o bloco `animar`{:class="block3myblocks"} abaixo dos blocos `muda o teu traje`{:class="block3look"}. O teu código agora deve estar parecido com isto:

![Result sprite](images/result-sprite.png)

```blocks3
    quando eu receber [correto v]
    alternar traje para (tick v)
    animar:: custom

    quando recebo [v errado]
    alternar traje para (cruz v)
    animar:: personalizado
```

\--- /task \---

Por causa do bloco personalizado `animar`{:class="block3myblocks"}, agora só precisas de fazer uma mudança ao teu código se quiseres mostrar os trajes do actor 'resultado' um tempo maior ou menor.

\--- task \---

Altera o teu código para que o 'certo' ou 'errado' sejam mostrados por 2 segundos.

\--- /task \---

\--- task \--- Em vez de ` mostrar ` {: class = "block3looks"} e ` esconder ` {: class = "block3looks"} os trajes 'certo' ou 'errado', podes mudar o teu bloco ` animar `{: class = "block3myblocks"} para que os trajes apareçam.

![Result sprite](images/result-sprite.png)

```blocks3
    define animar
    set [efeito fantasma v] para (100)
    mostra
    repetição (25)
        mudança [efeito fantasma v] por (-4)
    fim
    esconder
```

\--- /task \---

Pode melhorar a animação dos gráficos 'certo' e 'errado'? Pode adicionar código para também fazer os trajes desaparecerem, ou podes usar outros efeitos interessantes:

![captura de ecrã](images/brain-effects.png)