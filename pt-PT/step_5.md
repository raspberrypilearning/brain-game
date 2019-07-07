## Múltiplas jogadas

Agora vais adicionar um botão 'Play', para que o jogador possa jogar o teu jogo muitas vezes.

\--- task \--- Cria um novo actor botão 'Play' que o jogador precisa clicar para iniciar um novo jogo.

Podes desenhar o actor tu mesmo, ou editar um actor da biblioteca.

![Imagem do botão Play](images/brain-play.png)

\--- /task \---

\--- task \--- Adiciona este código ao teu actor botão:

![Actor botāo](images/button-sprite.png)

```blocks3
    quando alguém clicar na bandeira verde
       mostra-te

       quando alguém clicar em ti
       esconde-te
       difunde a mensagem (start v)
```

\--- /task \---

O novo código inclui outro bloco `difunde a mensagem`{:class="block3events"} que envia a mensagem 'start'.

O novo código faz com que o sprite do botão 'Play' apareça quando o jogador clica na bandeira. Quando o jogador clica no actor do botão, o actor esconde-se e difunde uma mensagem a que outros actores podem reagir.

De momento, o actor personagem começa a fazer perguntas quando o jogador clica na bandeira. Altera o código do teu jogo para que o actor do personagem comece a fazer perguntas quando `Quando receberes a mensagem`{:class="block3events"} 'start'.

\--- task \--- Selecione o teu actor e, na sua seção de código, substitui o bloco ` quando alguém clicar na bandeira `{: class = "block3events"} com um bloco ` quando receberes a mensagem start `{: class = "block3events"}.

![Actor personagem](images/giga-sprite.png)

```blocks3
<br />- quando alguém clicar na bandeira verde
+quando eu receber a mensagem start
        altera [number 1 v] para (um valor ao acaso entre (2) e (12))
        altera [number 2 v] para (um valor ao acaso entre (2) e (12))
        pergunta (a junção de (number 1) com (a junção de [ x ] com (number 2))) e espera pela resposta
        se &lt;(answer) = ((number 1) * (number 2))>&gt; então 
            diz [certo! :)] por (2) segundos
senão
    diz [Errado :(] por (2) segundos
fim
```

\--- /task \---

\--- task \---

Clica na bandeira verde e clica no novo botão 'Play' para testar se ele funciona. Deves ver que o jogo não começa antes de clicares no botão.

\--- /task \---

Reparas-te que o temporizador começa a contagem quando fazes clique na bandeira verde, e não quando começas o jogo?

![Temporizador iniciado](images/brain-timer-bug.png)

\--- task \---

Podes alterar o código para o temporizador para que o temporixzador comece quando o jogador clica no botão?

\--- /task \---

\--- task \--- Adiciona código ao actor do teu botão para que o botão apareça novamente no final de cada jogo.

![Actor botāo](images/button-sprite.png)

```blocks3
    quando receberes a mensagem [acabar v]
    mostra-te
```

\--- /task \---

\--- task \---

Teste o botão 'Play' jogando um par de jogos. O botão deve aparecer no final de cada jogo.

Para testar o jogo mais rapidamente, você pode alterar o valor de `time`{:class="block3variáveis"} para que cada jogo tenha apenas alguns segundos.

![Palco](images/stage-sprite.png)

```blocks3
    altera [tempo v] para [10]
```

\--- /task \---

\--- task \--- Podes alterar a aparência do botão quando o ponteiro do mouse paira sobre ele.

![Botão](images/button-sprite.png)

```blocks3
    quando alguém clicar na bandeira verde
    mostra-te
    repete para sempre 
    se &lt;touching (mouse-pointer v)?&gt;estás a tocar no ponteiro do rato </0>, então 
        altera o teu efeito [olho de peixe v] para (30)
    senão
        altera o teu efeito [olho de peixe v] para (0)
  end
end
```

![captura de ecrã](images/brain-fisheye.png) \--- /task \---