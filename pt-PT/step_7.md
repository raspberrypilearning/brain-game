## Adicionar gráficos

De momento, o actor do personagem só diz `certo! :)` ou `errado :(` às respostas do jogador. Adiciona alguns gráficos para informar o jogador se sua resposta está correta ou incorreta.

\--- task \---

Cria um novo actor com o nome ‘resultado’, com trajes de ‘correcto’ e ‘incorrecto’.

![Actor com trajes de correcto e incorrecto e errado](images/brain-result.png)

\--- /task \---

\--- task \---

Altera o código do teu actor personagem para que, em vez de dizer algo ao jogador, ele `difunda a mensagem`{:class="block3events"} 'certo' ou 'errado'.

![Actor personagem](images/giga-sprite.png)

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

Agora podes usar estas mensagens para `mostrar`{:class="block3look"} o traje 'correto' ou 'incorrecto'. Adiciona o seguinte código ao actor 'resultado':

![Actor Resultado](images/result-sprite.png)

```blocks3
    quando recebo [certo v]
    alterna o traje para (correto v)
    motra-te
    espera (1) segundos
    esconde-te

    quando recebo [v errado]
    alterna o traje para (incorrecto v)
    motra-te
    espera (1) segundos
    esconde-te

    quando alguém clicar na bandeira 
    esconde-te
```

\--- /task \---

\--- task \--- Testa o teu jogo novamente. Deves ver o 'certo' sempre que responderes uma pergunta corretamente e o 'errado' sempre que responderes incorretamente!

![Correcto para a resposta certa, Incorreto para resposta errada](images/brain-test-answer.png)

\--- /task \---

Notaste que o código para `quando receberes a mensagem certo`{: class = "block3events"} e `quando receberes a mensagem a errado`{: class = "block3events"} é quase idêntico?

Então para poderes alterar o teu código mais facilmente, vais criar um bloco personalizado.

\--- task \---

Seleciona o actor 'Resultado'. Depois clica em `Meus Blocos`{:class="block3myblocks"}, e depois em **Criar um Bloco**. Cria um bloco novo e chama-lhe `animar`{:class="block3myblocks"}.

![Actor Resultado](images/result-sprite.png)

![Cria um bloco chamado animar](images/brain-animate-function.png)

\--- /task \---

\--- task \--- Move o código para `mostra-te`{:class="block3looks} e `esconde-te`{:class="block3looks"} do actor 'Resultado', para o bloco `animar`{:class="block3myblocks"}:

![Actor Resultado](images/result-sprite.png)

```blocks3
definir animar
mostra-te
espera (1) segundos
esconde-te
```

\--- /task \---

\--- task \--- Certifica-te de que removeste os blocos `mostra-te`{:class="block3looks"} e `esconde-te`{:class="block3looks"} debaixo de **ambos** os blocos `muda o teu traje`{:class="block3looks"}.

Em seguida adiciona o bloco `animar`{:class="block3myblocks"} abaixo dos blocos `muda o teu traje`{:class="block3looks"}. O teu código agora deve estar parecido com isto:

![Actor Resultado](images/result-sprite.png)

```blocks3
    quando eu receber [certo v]
    alternar traje para (correto v)
    animar:: personalizado

    quando recebo [v errado]
    alternar traje para (incorreto v)
    animar:: personalizado
```

\--- /task \---

Por causa do bloco personalizado `animar`{:class="block3myblocks"}, agora só precisas de fazer uma mudança ao teu código se quiseres mostrar os trajes do actor 'Resultado' um tempo maior ou menor.

\--- task \---

Altera o teu código para que o 'correto' ou 'incorreto' sejam mostrados por 2 segundos.

\--- /task \---

\--- task \--- Em vez de `mostrar` {: class = "block3looks"} e `esconder` {: class = "block3looks"} os trajes 'correto' ou 'incorreto', podes mudar o teu bloco `animar`{: class = "block3myblocks"} para que os trajes apareçam gradualmente.

![Actor Resultado](images/result-sprite.png)

```blocks3
    define animar
    altera [efeito fantasma v] para (100)
    mostra-te
    repetição (25)
        mudança [efeito fantasma v] por (-4)
    fim
    esconde-te
```

\--- /task \---

Podes melhorar a animação dos gráficos 'certo' e 'errado'? Podes adicionar código para também fazer os trajes desaparecerem gradualmente, ou podes usar outros efeitos interessantes:

![captura de ecrã](images/brain-effects.png)