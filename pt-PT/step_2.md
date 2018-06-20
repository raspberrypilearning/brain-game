## Criação de perguntas

Vamos começar criando perguntas aleatórias para o jogador responder.

+ Inicie um novo projeto do Scratch e apague o sprite do gato para que seu projeto fique vazio. Pode encontrar o editor de Scratch online em <a href="http://jumpto.cc/scratch-new" target="_blank"> jumpto.cc/scratch-new </a>.

+ Escolha um personagem e um pano de fundo para o seu jogo. Você pode escolher o que quiser! Aqui está um exemplo:
    
    ![screenshot](images/brain-setting.png)

+ Crie 2 novas variáveis ​​chamadas ` numero 1 ` {: class = "blockdata"} e ` número 2 ` {: class = "blockdata"}. Essas variáveis ​​armazenarão os 2 números que serão multiplicados juntos.
    
    ![screenshot](images/brain-variables.png)

+ Adicione o código ao seu personagem, para definir ambas as variáveis ​​para ` um valor ao acaso entre ` {: class = "blockoperators"} 2 e 12.
    
    ```blocks
        quando alguém clicar na bandeira
      altera [número 1] para (um valor ao acaso entre (2) e (12)) 
      altera [número 2] para (um valor ao acaso entre (2) e (12))
    ```

+ Pode então perguntar ao jogador a resposta e confirmar se ele estava certo ou errado.
    
    ```blocks
        quando alguém clicar na bandeira
         altera [número 1] para (um valor ao acaso entre (2) e (12)) 
         altera [número 2] para (um valor ao acaso entre (2) e (12))
         pergunta (a junção de (número 1) com a junção de [ x ] com (número 2)) e espera pela resposta
    se <( a resposta) = ((número 1)*(número 2))> , então 
            Difunde a mensagem [correto! :)] durante (2) segundos 
    senão 
              difunde  [errado :(] durante (2)
    terminar
    ```

+ Test your project fully, by answering one question correctly and one with the wrong answer.

+ Add a `forever`{:class="blockcontrol"} loop around this code, so that the player is asked lots of questions.

+ Create a countdown timer on the stage, using a variable called `time`{:class="blockdata"}. The 'Ghostbusters' project has instructions for making a timer (in step 5) if you need help!

+ Test your project again - you should be able to continue asking questions until the time runs out.