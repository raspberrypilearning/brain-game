## Criando questões

Vamos começar criando questões aleatórias para o jogador responder.

+ Inicie um novo projeto do Scratch e exclua o sprite do gato para que seu projeto fique vazio. Você pode encontrar o editor online do Scratch em <a href="http://jumpto.cc/scratch-new" target="_blank"> jumpto.cc/scratch-new </a>.

+ Escolha um personagem um plano de fundo para o seu jogo. Você pode escolher qualquer coisa que gostar! Um exemplo:
    
    ![screenshot](images/brain-setting.png)

+ Cria duas novas variáveis ​​chamadas `número 1` {:class="blockdata"} e `número 2` {: class = "blockdata"}. Estas variáveis vão ​​guardar os dois números que vão ser multiplicados.
    
    ![screenshot](images/brain-variables.png)

+ Adicione o código ao seu personagem, para definir ambas as variáveis ​​para um número `aleatório` {:class="blockoperators"} entre 2 e 12.
    
    ```blocks
        when flag clicked
        set [number 1 v] to (pick random (2) to (12))
        set [number 2 v] to (pick random (2) to (12))
    ```

+ You can then ask the player for the answer, and let them know if they were right or wrong.
    
    ```blocks
        when flag clicked
        set [number 1 v] to (pick random (2) to (12))
        set [number 2 v] to (pick random (2) to (12))
        ask (join (number 1)(join [ x ] (number 2))) and wait
        if <(answer) = ((number 1)*(number 2))> then
            say [yes! :)] for (2) secs
        else
            say [nope :(] for (2) secs
        end
    ```

+ Test your project fully, by answering one question correctly and one with the wrong answer.

+ Add a `forever`{:class="blockcontrol"} loop around this code, so that the player is asked lots of questions.

+ Create a countdown timer on the stage, using a variable called `time`{:class="blockdata"}. The 'Ghostbusters' project has instructions for making a timer (in step 5) if you need help!

+ Test your project again - you should be able to continue asking questions until the time runs out.