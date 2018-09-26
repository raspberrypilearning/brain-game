## Vários jogos

Vamos inserir um botão de ‘Jogar’ ao seu jogo, para que você possa jogar várias vezes.

+ Crie um novo objeto para o botão de "Jogar", no qual o jogador vai clicar para iniciar um novo jogo. Você mesmo pode desenhar o botão ou editar um ator da biblioteca do Scratch.
    
    ![captura de tela](images/brain-play.png)

+ Adicione este código ao seu novo botão.
    
    ```blocks
        quando alguém clicar na bandeira verde
           mostre
           Quando alguém clicar no objeto
           esconde
           transmita a mensagem [começar v]
    ```
    
    Este código mostra um botão Jogar quando seu projeto é iniciado. O botão se esconde quando é clicado e então é transmitida uma mensagem que vai iniciar jogo.

+ Você vai precisar editar o código do seu personagem, para que o jogo comece quando eles receberem o `início`{:class="blockevents"}, e não quando a bandeira é clicada.
    
    Substitua o código de`quando a bandeira for clicada`{:class="blockevents"} por `quando iniciar`{:class="blockevents"}.
    
    ![captura de tela](images/brain-start.png)

+ Clique na bandeira verde e então clique no seu novo botão Jogar para testá-lo. Você vai ver que o jogo não inicia mesmo quando o botão é clicado.

+ Você notou que o contador de tempo inicia quando a bandeira verde é clicada, e não quando o jogo começa?
    
    ![captura de tela](images/brain-timer-bug.png)
    
    Consegue resolver este problema?

+ Clique no palco, e substitua o bloco `para tudo`{:class="blockcontrol"} por uma mensagem `fim`{:class="blockevents"}.
    
    ![captura de tela](images/brain-end.png)

+ Você agora pode adicionar código ao seu botão, para mostrá-lo de novo ao fim de cada partida.
    
    ```blocks
        quando eu receber [fim v]
      mostrar
    ```

+ Você também precisa impedir que o personagem faça novas perguntas ao fim de cada jogo:
    
    ```blocks
        quando recebo [fim v]
      pare [outros scripts no objeto v]
    ```

+ Teste o seu botão ao jogar algumas partidas. Você pode observar que o botão Jogar aparece após cada partida. Para tornar o teste mais fácil, você pode encurtar cada partida, de modo que ela dure apenas alguns segundos.
    
    ```blocks
        alterar[tempo v] para [10]
    ```

+ Você pode até mesmo mudar a aparência do botão quando o mouse passar por cima dele.
    
    ```blocks
        quando a bandeira verde for clicada
      mostrar
      para sempre
      se <touching [mouse-pointer v]?> então
        altere efeito [olho de peixe v] para (30)
      senão
         altere o efeito [olho de peixe v] para (0)
      fim
      fim
    ```
    
    ![captura de tela](images/brain-fisheye.png)