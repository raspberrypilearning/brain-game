## Vários jogos

Vamos inserir um botão de ‘Jogar’ ao seu jogo, para que possa jogar várias vezes.

+ Cria um novo objeto com um botão de ‘Jogar’, no qual o jogador irá clicar para iniciar um novo jogo. Você mesmo pode desenhar ou editar um ator da biblioteca do Scratch.
    
    ![screenshot](images/brain-play.png)

+ Adicione este código ao seu novo botão.
    
    ```blocks
        quando alguém clicar na bandeira verde
           mostre
           Quando alguém clicar no objeto
           esconde
           transmita a mensagem [começar v]
    ```
    
    Este código mostra um botão Jogar quando seu projeto é iniciado. Quando o botão é clicado se escode e então uma mensagem é transmitida que o jogo irá iniciar.

+ Você precisará editar o código do seu personagem, para que o jogo comece quando eles receberem o `início`{:class="blockevents"}, e não quando a bandeira é clicada.
    
    Substitua o código de`quando a bandeira for clicada`{:class="blockevents"} por `quando iniciar`{:class="blockevents"}.
    
    ![screenshot](images/brain-start.png)

+ Clique na bandeira verde e então clique no seu novo botão Jogar para testá-lo. Você verá que o jogo não inicia mesmo quando o botão é clicado.

+ Did you notice that the timer starts when the green flag is clicked, and not when the game starts?
    
    ![screenshot](images/brain-timer-bug.png)
    
    Can you fix this problem?

+ Click on the stage, and replace the `stop all`{:class="blockcontrol"} block with an `end`{:class="blockevents"} message.
    
    ![screenshot](images/brain-end.png)

+ You can now add code to your button, to show it again at the end of each game.
    
    ```blocks
        when I receive [end v]
        show
    ```

+ You'll also need to stop your character asking questions at the end of each game:
    
    ```blocks
        when I receive [end v]
        stop [other scripts in sprite v]
    ```

+ Test your play button by playing a couple of games. You should notice that the play button shows after each game. To make testing easier, you can shorten each game, so that it only lasts a few seconds.
    
    ```blocks
        set [time v] to [10]
    ```

+ You can even change how the button looks when the mouse hovers over it.
    
    ```blocks
        when flag clicked
        show
        forever
        if <touching [mouse-pointer v]?> then
            set [fisheye v] effect to (30)
        else
            set [fisheye v] effect to (0)
        end
        end
    ```
    
    ![screenshot](images/brain-fisheye.png)