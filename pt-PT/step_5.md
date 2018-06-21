## Jogadas múltiplas

Vamos inserir um botão de ‘Jogar’ ao teu jogo, para que possas jogar múltiplas vezes.

+ Cria um novo objeto com um botão de ‘Jogar’, no qual o jogador irá clicar para iniciar um novo jogo. Podes desenha-lho tu mesmo ou editar um actor da biblioteca do Scratch.
    
    ![captura de ecrã](images/brain-play.png)

+ Adiciona este código ao teu botão novo:
    
    ```blocks
        Quando alguém clicar na bandeira verde
           mostra-te
    
           Quando alguém clicar em ti
           esconde-te
           difunde a mensagem [começar v]
    ```
    
    Este código mostra o botão de jogar quando o projeto começa. Ao clicar no botão, este esconde-se e envia uma mensagem para que o jogo comece.

+ Precisas de editar o código da tua personagem para que o jogo comece quando receber a mensagem de `começar` {: classe = "blockevents"}, e não quando a bandeira é clicada.
    
    Substitui o código `quando alguém clicar na bandeira verde` {: classe = "blockevents"} com `quando receberes a mensagem começar ` {: classe = "blockevents"}.
    
    ![captura de ecrã](images/brain-start.png)

+ Faz clique na bandeira verde e depois pressiona o teu novo botão de jogo para o experimentares. O jogo só deve de começar depois de clicares no botão.

+ Reparas-te que o cronómetro começa a contagem quando fazes clique na bandeira verde, e não quando começas o jogo?
    
    ![captura de ecrã](images/brain-timer-bug.png)
    
    Can you fix this problem?

+ Faz clique no cenário, e substitui o bloco ` parar todos ` Bloco {: class = "blockcontrol"} com uma mensagem ` Acabar` {: class = "blockevents"}.
    
    ![captura de ecrã](images/brain-end.png)

+ Agora podes inserir código ao botão para que ele volte a aparecer no fim de cada jogo.
    
    ```blocks
        quando eu recebo [terminar] 
        mostra-me
    ```

+ Também terás de fazer com que a tua personagem deixe de fazer perguntas no fim de cada jogo:
    
    ```blocks
        quando eu recebo [terminar] 
        pare [outros scripts no sprite v]
    ```

+ Testa o botão jogando varias vezes. Deverás ver aparecer o botão de jogar depois de cada jogo. Para tornar o teste mais fácil, você pode encurtar cada jogo, de maneira a durar apenas alguns segundos.
    
    ```blocks
        altera [tempo v] para [10]
    ```

+ Podes também fazer que a forma do botão mude quando lhe aproximes o rato.
    
    ```blocks
        Quando alguém clicar na bandeira
        mostra-te
        repete para sempre
        se estas a tocar em o ponteiro do rato, entao
            altera o teu efeito olho de peixe para (30)
        senao
            altera o teu efeito olho de peixe para (0)
    ```
    
    ![captura de ecrã](images/brain-fisheye.png)