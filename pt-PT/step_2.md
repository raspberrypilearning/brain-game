## Criação de perguntas

Vamos começar por criar perguntas aleatórias para o jogador responder.

+ Cria um novo projeto no Scratch, e apaga o actor gato de maneira a que o projeto fique totalmente vazio. Podes encontrar o editor online do Scratch em <a href="http://jumpto.cc/scratch-new" target="_blank"> jumpto.cc/scratch-new </a>.

+ Escolhe uma personagem e um pano de fundo para o teu jogo. Podes escolher os que mais gostares! Exemplo:
    
    ![screenshot](images/brain-setting.png)

+ Cria duas novas variáveis ​​chamadas ` numero 1 ` {: class = "blockdata"} e ` número 2 ` {: class = "blockdata"}. Estas variáveis vão ​​guardar os dois números que vão ser multiplicados.
    
    ![captura de ecrã](images/brain-variables.png)

+ Adiciona o código à tua personagem, para defenir ambas as variáveis ​​em ` um valor ao acaso entre ` {: class = "blockoperators"} 2 e 12.
    
    ```blocks
        Quando alguém clicar na bandeira verde
            altera [numero 1 v] para (um valor ao acaso entre (2) e (12))
            altera [numero 2 v] para (um valor ao acaso entre (2) e (12))
    ```

+ Podes então pedir ao jogador a resposta e dizer-lhe se está certa ou errada.
    
    ```blocks
        Quando alguém clicar na bandeira verde
            altera [number 1 v] para (um valor ao acaso entre (2) e (12))
            altera [number 2 v] para (um valor ao acaso entre (2) e (12))
            pergunta (a junção de (number 1) com (a junção de [ x ] com (number 2))) e espera pela resposta
            se <(answer) = ((number 1) * (number 2))>, então 
                diz [certo! :)] durante (2) s
            senão
                diz [errado:(] durante (2) s
            end
    ```

+ Experimenta o teu projeto duas vezes, na primeira escrevendo uma resposta correta e depois uma resposta incorreta.

+ Adicione um loop ` repete para sempre ` {: class = "blockcontrol"} em torno deste código, de modo que o jogador é questionado com muitas perguntas.

+ Cria um cronometro de conta decrescente no cenário, utilizando uma variável que se chame ` tempo ` {: class = "blockdata"}. O projeto 'Ghostbusters' tem instruções para fazer um temporizador (no passo 5) se você precisar de ajuda!

+ Experimenta novamente o teu projeto. Deveras de poder continuar a fazer perguntas até que o tempo acabe.