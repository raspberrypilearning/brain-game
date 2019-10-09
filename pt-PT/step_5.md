## Múltiplas jogadas

Agora vais adicionar um botão 'Jogar', para que o jogador possa jogar o teu jogo muitas vezes.

\--- task \--- Cria um novo actor botão 'Play' que o jogador precisa clicar para iniciar um novo jogo.

Podes desenhar o actor tu mesmo, ou editar um actor da biblioteca.

![Imagem do botão Play](images/brain-play.png)

\--- /task \---

\--- task \--- Adiciona este código ao teu actor botão:

![Actor botāo](images/button-sprite.png)

```blocks3
    when flag clicked
show

when this sprite clicked
hide
broadcast (start v)
```

\--- /task \---

O novo código inclui outro bloco `difunde a mensagem`{:class="block3events"} que envia a mensagem 'começar'.

O novo código faz com que o actor do botão 'Jogar' apareça quando o jogador clicar na bandeira. Quando o jogador clica no actor do botão, o actor esconde-se e difunde uma mensagem a que outros actores podem reagir.

De momento, o actor personagem começa a fazer perguntas quando o jogador clicar na bandeira. Altera o código do teu jogo para que o actor do personagem comece a fazer perguntas quando `Quando receberes a mensagem`{:class="block3events"} 'começar'.

\--- task \--- Seleciona o teu actor e, na sua seção de código, substitui o bloco ` Quando alguém clicar na bandeira `{: class = "block3events"} com um bloco ` quando receberes a mensagem começar`{: class = "block3events"}.

![Actor personagem](images/giga-sprite.png)

```blocks3
<br />- when flag clicked
+ when I receive [start v]
set [number 1 v] to (pick random (2) to (12))
set [number 2 v] to (pick random (2) to (12))
ask (join (number 1)(join [ x ] (number 2))) and wait
if <(answer) = ((number 1)*(number 2))> then
say [yes! :)] for (2) seconds
else
say [nope :(] for (2) seconds
end
```

\--- /task \---

\--- task \---

Clica na bandeira verde e clica no novo botão 'Jogar ' para testar se ele funciona. Deves observar que o jogo não começa antes de clicares no botão.

\--- /task \---

Reparas-te que o temporizador começa a contagem quando fazes clique na bandeira verde, e não quando começas o jogo?

![Temporizador iniciado](images/brain-timer-bug.png)

\--- task \---

Podes alterar o código do temporizador para que o temporizador comece quando o jogador clicar no botão?

\--- /task \---

\--- task \--- Adiciona código ao actor do teu botão para que o botão apareça novamente no final de cada jogo.

![Actor botāo](images/button-sprite.png)

```blocks3
    when I receive [end v]
show
```

\--- /task \---

\--- task \---

Testa o botão 'Jogar' jogando um par de jogos. O botão deve aparecer no final de cada jogo.

Para testar o jogo mais rapidamente, podes alterar o valor de `tempo`{:class="block3variables"} para que cada jogo tenha apenas alguns segundos.

![Palco](images/stage-sprite.png)

```blocks3
    altera [tempo v] para [10]
```

\--- /task \---

\--- task \--- Podes alterar a aparência do botão quando o ponteiro do rato paira sobre ele.

![Botão](images/button-sprite.png)

```blocks3
    when flag clicked
show
forever
if <touching (mouse-pointer v)?> then
set [fisheye v] effect to (30)
else
set [fisheye v] effect to (0)
end
end
```

![captura de ecrã](images/brain-fisheye.png) \--- /task \---