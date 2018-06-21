## Inserir ícones

Em vez de a tua personagem apenas dizer ` certo! :) ` ou ` errado! :(` ao jogador, vamos inserir alguns ícones para que ajudem o jogador a saber como lhe está a correr.

+ Cria um novo actor com o nome ‘resultado’, que contenha os trajes de ‘correcto’ e ‘incorrecto’.
    
    ![screenshot](images/brain-result.png)

+ Muda o código do teu personagem, para que em vez de dizer o resultado ao jogador ao jogador difunda mensagens ` certo ` {: class = "blockevents"} e ` errado ` {: class = "blockevents"}.
    
    ![screenshot](images/brain-broadcast-answer.png)

+ Agora, podes usar estas mensagens para mostrar os trajes 'correcto' ou 'incorrecto'. Adiciona este código ao teu novo actor 'Resultado':
    
    ![screenshot](images/brain-show-answer.png)

+ Testa o teu jogo novamente. Deverás ver um "certo" sempre que tiveres uma pergunta correta e uma cruz sempre que estiveres errado!
    
    ![screenshot](images/brain-test-answer.png)

+ Notaste que o código para ` quando eu recebo a resposta correta? ` {: class = "blockevents"} e ` quando eu recebo a resposta errada ` {: class = "blockevents"} é quase idêntico? Vamos criar uma função para facilitar a alteração do teu código.
    
    No teu actor 'Resultado', clica em ` Mais Blocos ` {: class = "blockmoreblocks"} e, em seguida, "Criar um Bloco". Crie uma nova função chamada ` animação ` {: class = "blockmoreblocks"}.
    
    ![screenshot](images/brain-animate-function.png)

+ Podes adicionar o código da animação na tua nova função de animação, e depois usa a função duas vezes:
    
    ![screenshot](images/brain-use-function.png)

+ Se quiseres mostrar o "certo" e a cruz por um tempo maior ou menor, só precisas fazer uma alteração ao teu código. Experimenta!

+ Em vez de apenas mostrar e esconder os ícones "certo" e cruz, podes alterar a tua função de animação, para que os ícones se materializem.
    
    ```blocks
        define [animate]
        set [ghost v] effect to (100)
        show
        repeat (25)
            change [ghost v] effect by (-4)
        end
        hide
    ```