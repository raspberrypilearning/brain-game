## Múltiplas jogadas

Agora vais adicionar um botão 'Jogar', para que o jogador possa jogar o teu jogo muitas vezes.

--- task --- Cria um novo actor botão 'Play' que o jogador precisa clicar para iniciar um novo jogo.

Podes desenhar o actor tu mesmo, ou editar um actor da biblioteca.

![Imagem do botão Play](images/brain-play.png)

--- /task ---

--- task --- Adiciona este código ao teu actor botão:

![Actor botāo](images/button-sprite.png)

```blocks3
Quando alguém clicar na bandeira verde
mostra-te

Quando alguém clicar em ti
esconde-te
difunde a mensagem (começar v)
```

--- /task ---

O novo código inclui outro bloco `difunde a mensagem`{:class="block3events"} que envia a mensagem 'começar'.

O novo código faz com que o actor do botão 'Jogar' apareça quando o jogador clicar na bandeira. Quando o jogador clica no actor do botão, o actor esconde-se e difunde uma mensagem a que outros actores podem reagir.

De momento, o actor personagem começa a fazer perguntas quando o jogador clicar na bandeira. Altera o código do teu jogo para que o actor do personagem comece a fazer perguntas quando `Quando receberes a mensagem`{:class="block3events"} 'começar'.

--- task --- Seleciona o teu actor e, na sua seção de código, substitui o bloco `Quando alguém clicar na bandeira`{:class="block3events"} com um bloco `quando receberes a mensagem começar`{:class="block3events"}.

![Actor personagem](images/giga-sprite.png)

```blocks3
- Quando alguém clicar na bandeira verde
+ Quando receberes a mensagem [start v]
altera [numero 1 v] para (um valor ao acaso entre (2) e (12))
altera [numero 2 v] para (um valor ao acaso entre (2) e (12))
pergunta (a junção de (numero 1) com (a junção de [ x ] com (numero 2))) e espera pela resposta
se <(a resposta) = ((numero 1) × (numero 2))> , então 
  diz [Certo! :)] durante (2) s
senão, 
  diz [Errado :(] durante (2) s
```

--- /task ---

--- task ---

Clica na bandeira verde e clica no novo botão 'Jogar ' para testar se ele funciona. Deves observar que o jogo não começa antes de clicares no botão.

--- /task ---

Reparas-te que o temporizador começa a contagem quando fazes clique na bandeira verde, e não quando começas o jogo?

![Temporizador iniciado](images/brain-timer-bug.png)

--- task ---

Podes alterar o código do temporizador para que o temporizador comece quando o jogador clicar no botão?

--- /task ---

--- task --- Adiciona código ao actor do teu botão para que o botão apareça novamente no final de cada jogo.

![Actor botāo](images/button-sprite.png)

```blocks3
    Quando receberes a mensagem [acabar v]
    mostra-te
```

--- /task ---

--- task ---

Testa o botão 'Jogar' jogando um par de jogos. O botão deve aparecer no final de cada jogo.

Para testar o jogo mais rapidamente, podes alterar o valor de `tempo`{:class="block3variables"} para que cada jogo tenha apenas alguns segundos.

![Palco](images/stage-sprite.png)

```blocks3
    altera [tempo v] para [10]
```

--- /task ---

--- task --- Podes alterar a aparência do botão quando o ponteiro do rato paira sobre ele.

![Botão](images/button-sprite.png)

```blocks3
    Quando alguém clicar na bandeira verde
    mostra-te
    repete para sempre 
    se <estás a tocar em (o ponteiro do rato v)> , então 
        altera o teu efeito [olho de peixe v] para (30)
    senão, 
        altera o teu efeito [olho de peixe v] para (0)
```

![captura de ecrã](images/brain-fisheye.png) --- /task ---