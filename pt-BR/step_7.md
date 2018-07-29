## Adicionando gráficos

Ao invés do personagem somente dizer `sim! :)` ou `não :(` para o jogador, vamos adicionar alguns gráficos para que ajudem o jogador a entender como está indo.

+ Crie um novo objeto chamado 'Resultado', contendo ambos um 'sinal de visto' e um 'sinal de errado'.
    
    ![screenshot](images/brain-result.png)

+ Mude o código de seu personagem, para que ao invés de dizer ao jogador o resultado, mostrar as mensagens `correto`{:class="blockevents"} e `errado`{:class="blockevents"}.
    
    ![screenshot](images/brain-broadcast-answer.png)

+ You can now use these messages to show the 'tick' or 'cross' costume. Add this code to your new 'Result' sprite:
    
    ![screenshot](images/brain-show-answer.png)

+ Test out your game again. You should see a tick whenever you get a question correct, and a cross whenever you get one wrong!
    
    ![screenshot](images/brain-test-answer.png)

+ Have you noticed that the code for `when I receive correct`{:class="blockevents"} and `when I receive wrong`{:class="blockevents"} is nearly identical? Let's create a function to make it easier for you to make changes to your code.
    
    On your 'Result' sprite, click `More Blocks`{:class="blockmoreblocks"}, and then 'Make a Block'. Create a new function called `animate`{:class="blockmoreblocks"}.
    
    ![screenshot](images/brain-animate-function.png)

+ You can then add the animation code into your new animation function, and then just use the function twice:
    
    ![screenshot](images/brain-use-function.png)

+ Now, if you want to show the tick and the cross for a longer or shorter time, you only need to make one change to your code. Try it!

+ Instead of just showing and hiding the tick and the cross, you could change your animation function, so that the graphics fade in.
    
    ```blocks
        define [animate]
        set [ghost v] effect to (100)
        show
        repeat (25)
            change [ghost v] effect by (-4)
        end
        hide
    ```