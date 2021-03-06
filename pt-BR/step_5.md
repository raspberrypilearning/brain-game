## Vários jogos

Agora você vai adicionar um botão 'Jogar', para que o jogador possa jogar o seu jogo muitas vezes.

--- task ---

Crie um novo botão 'Jogar' que o jogador precisa clicar para iniciar um novo jogo.

Você pode desenhar o ator você mesmo, ou editar um ator da biblioteca.

![Imagem do botão Jogar](images/brain-play.png)

--- /task ---

--- task ---

Adicione este código ao seu ator de botão:

![Ator de Botão](images/button-sprite.png)

```blocks3
    when flag clicked
    show

    when this sprite clicked
    hide
    broadcast (começar v)
```

--- /task ---

O novo código inclui outro bloco `transmita`{:class="block3events"}, que envia a mensagem 'começar'.

O novo código faz o botão 'Jogar' aparecer quando o jogador clicar na bandeira. Quando o jogador clica no ator de botão, o ator desaparece e então transmite uma mensagem que outros atores podem reagir.

No momento, o ator de personagem começa a fazer perguntas quando o jogador clica na bandeira. Altere o código do seu jogo para que o ator de personagem comece a fazer perguntas quando o `transmita`{:class="block3events"} de 'começar' for recebida.

--- task ---

Selecione seu personagem e, em sua seção de código, substitua o bloco `quando bandeira for clicado`{:class="block3events"} por um bloco `quando eu receber começar`{:class="block3events"}.

![Ator de Personagem](images/giga-sprite.png)

```blocks3
- when flag clicked
+ when I receive [começar v]
set [número 1 v] to (pick random (2) to (12))
set [número 2 v] to (pick random (2) to (12))
ask (join (número 1)(join [ x ] (número 2))) and wait
if <(answer) = ((número 1)*(número 2))> then
    say [sim! :)] for (2) seconds
else
    say [não :(] for (2) seconds
end
```

--- /task ---

--- task ---

Clique na bandeira verde e, em seguida, clique no novo botão 'Jogar' para testar se funciona. Você deve ver que o jogo não começa antes de você clicar no botão.

--- /task ---

Você notou que o cronômetro inicia quando a bandeira verde é clicada, e não quando o jogo começa?

![Cronômetro iniciado](images/brain-timer-bug.png)

--- task ---

Você consegue alterar o código do cronômetro para que o cronômetro comece quando o jogador clicar no botão?

--- /task ---

--- task ---

Adicione código ao seu ator de botão para que o botão seja exibido novamente no final de cada jogo.

![Ator de Botão](images/button-sprite.png)

```blocks3
    quando eu receber [fim v]
    mostrar
```

--- /task ---

--- task ---

Teste o botão 'Jogar' jogando alguns jogos. O botão deve ser exibido no final de cada jogo.

Para testar o jogo mais rapidamente, você pode mudar o valor de `tempo`{:class="block3variables"} para que cada jogo tenha apenas alguns segundos de duração.

![Palco](images/stage-sprite.png)

```blocks3
    set [tempo v] to [10]
```

--- /task ---

--- task ---

Você pode mudar a aparência do botão quando o mouse passar por cima dele.

![Botão](images/button-sprite.png)

```blocks3
  when green flag clicked
  mostrar
  para sempre
  se <touching (mouse-pointer v)?> então
    set [fisheye v] effect to (30)
  senão
    set [fisheye v] effect to (0)
  fim
  fim
```

![screenshot](images/brain-fisheye.png)

--- /task ---