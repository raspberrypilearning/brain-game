## Adicionando gráficos

Ao invés do personagem dizer somente `sim! :)` ou `não :(` para o jogador, vamos adicionar alguns gráficos que vão ajudar o jogador a entender como ele está indo.

+ Crie um novo objeto chamado 'Resultado', contendo ambos um "sinal de visto" e um "sinal de "errado".
    
    ![captura de tela](images/brain-result.png)

+ Mude o código de seu personagem para que, ao invés de dizer ao jogador o resultado, ele mostre as mensagens `correto`{:class="blockevents"} e `errado`{:class="blockevents"}.
    
    ![captura de tela](images/brain-broadcast-answer.png)

+ Agora você pode usar essas mensagens para mostar o "sinal de visto" ou o "sinal de errado". Adicione esse código ao seu novo objeto "Resultado":
    
    ![captura de tela](images/brain-show-answer.png)

+ Teste o seu jogo novamente. Você deve ver um "sinal de visto" sempre que responder uma questão corretamente e um "sinal de errado" sempre que responder errado!
    
    ![captura de tela](images/brain-test-answer.png)

+ Você notou que o código para `quando eu recebo correto`{:class="blockevents"} e `quando eu recebo errado`{:class="blockevents"} são quase idênticos? Vamos criar uma função para facilitar as alterações no código.
    
    No seu objeto 'Resultado', clique em `Mais Blocos`{:class="blockmoreblocks"}, e então 'Criar um Bloco'. Crie uma nova função chamada `animar`{:class="blockmoreblocks"}.
    
    ![captura de tela](images/brain-animate-function.png)

+ Você pode então adicionar o código de animação em sua nova função de animação, e então usar a função duas vezes:
    
    ![captura de tela](images/brain-use-function.png)

+ Agora, se você quiser mostrar o "sinal de visto" e o "sinal de errado" por um tempo mais longo ou curto, você só vai precisar fazer uma alteração no código. Tente!

+ Ao invés de somente mostrar e esconder o "sinal de visto" e o "sinal de errado" você pode mudar sua função de animação para que os ícones apareçam.
    
    ```blocks
        defina [animate]
     alterar efeito [ghost v] para (100)
     mostrar
     repetir (25)
       mudar efeito [ghost v] para (-4)
     fim
    esconder
    ```