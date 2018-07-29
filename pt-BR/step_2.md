## Criação de perguntas

Vamos começar por criar perguntas aleatórias para o jogador responder.

+ Inicie um novo projeto do Scratch e exclua o sprite do gato para que seu projeto fique vazio. Para criar um novo projeto Scratch usando o editor online, acesse <a href="http://jumpto.cc/scratch-new" target="_blank">jumpto.cc/scratch-new</a>.

+ Escolha um personagem e um pano de fundo para o seu jogo. Você pode escolher o que quiser! Aqui está um exemplo:
    
    ![captura de tela](images/brain-setting.png)

+ Crie 2 novas variáveis ​​chamadas `numero 1` {:class="blockdata"} e `numero 2 ` {:class="blockdata"}. Essas variáveis ​​armazenarão os 2 números que serão multiplicados juntos.
    
    ![captura de tela](images/brain-variables.png)

+ Adicione o código ao seu personagem, para definir ambas as variáveis ​​para um número `aleatório` {:class="blockoperators"} entre 2 e 12.
    
    ```blocks
        quando alguém clicar na bandeira verde
            altera [número 1 v] para (um valor aleatório entre (2) e (12))
            altera [número 2 v] para (um valor aleatório entre (2) e (12))
    ```

+ Você pode então pedir ao jogador a resposta e dizer se estava certo ou errado.
    
    ```blocks
        quando alguém clicar na bandeira verde
            altera [numero 1 v] para (um valor aleatório entre (2) e (12))
            altera [numero 2 v] para (um valor aleatório entre (2) e (12))
            pergunta (a junção de (numero 1) com (a junção de [ x ] com (numero 2))) e espera pela resposta
            se <(resposta) = ((numero 1) * (numero 2))> então 
                diz [certo! :)] durante (2) s
            senão
                diz [errado:(] durante (2) s
            fim
    ```

+ Teste seu projeto completamente, respondendo uma questão corretamente e outra com a resposta errada.

+ Adicione um `para sempre` {:class="blockcontrol"} circula em torno deste código, de modo que o jogador receba muitas questões.

+ Crie um cronômetro de contagem regressiva no palco, usando uma variável chamada `tempo`{:class="blockdata"}. O projeto 'Ghostbusters' tem instruções para fazer um temporizador (no passo 5) se você precisar de ajuda!

+ Teste seu projeto novamente - você deve poder continuar fazendo questões até que o tempo acabe.