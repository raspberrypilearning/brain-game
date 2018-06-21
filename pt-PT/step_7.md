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

+ Have you noticed that the code for `when I receive correct`{:class="blockevents"} and `when I receive wrong`{:class="blockevents"} is nearly identical? Let's create a function to make it easier for you to make changes to your code.
    
    On your 'Result' sprite, click `More Blocks`{:class="blockmoreblocks"}, and then 'Make a Block'. Create a new function called `animate`{:class="blockmoreblocks"}.
    
    ![screenshot](images/brain-animate-function.png)

+ You can then add the animation code into your new animation function, and then just use the function twice:
    
    ![screenshot](images/brain-use-function.png)

+ Now, if you want to show the tick and the cross for a longer or shorter time, you only need to make one change to your code. Try it!

+ Instead of just showing and hiding the tick and the cross, you could change your animation function, so that the graphics fade in.
    
    ```blocks
        define (animação)
    altera o teu efeito [fantasma v] para (100)
    mostra-te
    repete (25) vezes 
      adiciona ao teu efeito [fantasma v] o valor (-4)
    end
    esconde-te
    ```