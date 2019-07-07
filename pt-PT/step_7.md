## Adicionar gráficos

De momento, o actor do personagem só diz `certo! :)` ou `errado :(` às respostas do jogador. Adiciona alguns gráficos para informar o jogador se sua resposta está correta ou incorreta.

\--- task \---

Cria um novo actor com o nome ‘resultado’, que contenha os trajes de ‘correcto’ e ‘incorrecto’.

![Sprite with tick and cross costumes](images/brain-result.png)

\--- /task \---

\--- task \---

Altera o código do teu actor personagem para que, em vez de dizer algo ao jogador, ele `difunda as mensagem`{:class="block3events"} 'correto' ou 'errado'.

![Character sprite](images/giga-sprite.png)

```blocks3
se <(resposta) = ((numero 1) * (numero 2))> entao

- diga [certo! :)] para (2) segundos
+ broadcast (v correto)
else
- diga [errado :(] para (2) segundos
+ broadcast (v errado)
end
```

\--- /task \---

\--- task \---

Agora podes usar estas mensagens para `mostrar`{:class="block3look"} o traje 'correto' ou 'incorrecto'. Adiciona o seguinte código ao actor 'Resultado':

![Result sprite](images/result-sprite.png)

```blocks3
    quando recebo [correto v]
    alterna o traje para (tick v)
    show
    wait (1) segundos
    ocultar

    quando recebo [v errado]
    alterna o traje para (cruz v)
    show
    wait (1) segundos
    ocultar

    quando alguém clicar na bandeira 
    ocultar
```

\--- /task \---

\--- task \--- Testa o teu jogo novamente. Deves ver o certo sempre que responderes uma pergunta corretamente e a errado sempre que responderes incorretamente!

![Tick for correct, cross for wrong answer](images/brain-test-answer.png)

\--- /task \---

Can you see that the code for `when I receive correct`{:class="block3events"} and `when I receive wrong`{:class="block3events"} is nearly identical?

So you can change your code more easily, you are going to create a custom block.

\--- task \---

Select the 'Result' sprite. Then click on `My Blocks`{:class="block3myblocks"}, and then on **Make a Block**. Create a new block and call it `animate`{:class="block3myblocks"}.

![Result sprite](images/result-sprite.png)

![Create a block called animate](images/brain-animate-function.png)

\--- /task \---

\--- task \--- Move the code to `show`{:class="block3looks"} and `hide`{:class="block3looks"} the 'Result' sprite into the `animate`{:class="block3myblocks"} block:

![Result sprite](images/result-sprite.png)

```blocks3
define animate
show
wait (1) seconds
hide
```

\--- /task \---

\--- task \--- Make sure you have removed the `show`{:class="block3looks"} and `hide`{:class="block3looks"} blocks below **both** of the `switch costume`{:class="block3looks"} blocks.

Then add the `animate`{:class="block3myblocks"} block below both of the `switch costume`{:class="block3looks"} blocks. Your code should now look like this:

![Result sprite](images/result-sprite.png)

```blocks3
    when I receive [correct v]
    switch costume to (tick v)
    animate:: custom

    when I receive [wrong v]
    switch costume to (cross v)
    animate:: custom
```

\--- /task \---

Because of the custom `animate`{:class="block3myblocks"} block, you now only need to make one change to your code if you want to show the 'Result' sprite's costumes a longer or shorter time.

\--- task \---

Change your code so that the 'tick' or 'cross' costumes display for 2 seconds.

\--- /task \---

\--- task \--- Instead of `showing`{:class="block3looks"} and `hiding`{:class="block3looks"} the 'tick' or 'cross' costumes, you could change your `animate`{:class="block3myblocks"} block so that the costumes fade in.

![Result sprite](images/result-sprite.png)

```blocks3
    define animate
    set [ghost v] effect to (100)
    show
    repeat (25)
        change [ghost v] effect by (-4)
    end
    hide
```

\--- /task \---

Can you improve the animation of the 'tick' or 'cross' graphics? You could add code to make the costumes fade out as well, or you could use other cool effects:

![captura de ecrã](images/brain-effects.png)