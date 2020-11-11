## Add graphics

No momento, o personagem apenas diz `sim! :)` ou `não :(` às respostas do jogador. Adicione algumas figuras para que o jogador saiba se a resposta dele está certa ou errada.

\--- task \---

Crie um novo ator chamado 'Resultado', e de um fantasia de "sinal de visto" e uma de "sinal de errado".

![Ator com as fantasias de sinal de visto e sinal de errado](images/brain-result.png)

\--- /task \---

\--- task \---

Mude o código do seu ator de personagem para que, em vez de dizer algo ao jogador, ele `transmita/`{:class="block3events"} as mensagens 'certo' ou 'errado'.

![Ator de Personagem](images/giga-sprite.png)

```blocks3
if <(answer) = ((number 1)*(number 2))> then

- say [yes! :)] for (2) seconds
+ broadcast (correct v)
else
- say [nope :(] for (2) seconds
+ broadcast (wrong v)
end
```

\--- /task \---

\--- task \---

Agora você pode usar essas mensagens para que `mostre`{:class="block3looks"} o "sinal de visto" ou o "sinal de errado". Adicione o seguinte código ao ator de 'Resultado':

![Ator de Resultado](images/result-sprite.png)

```blocks3
    when I receive [correct v]
    switch costume to (tick v)
    show
    wait (1) seconds
    hide

    when I receive [wrong v]
    switch costume to (cross v)
    show
    wait (1) seconds
    hide

    when flag clicked
    hide
```

\--- /task \---

\--- task \---

Teste o seu jogo novamente. Você deve ver um "sinal de visto" sempre que responder uma questão corretamente e um "sinal de errado" sempre que responder errado!

![Sinal de visto para certo e sinal de errado para errado](images/brain-test-answer.png)

\--- /task \---

Você notou que o código para `quando eu receber correto`{:class="block3events"} e `quando eu receber errado`{:class="block3events"} são quase idênticos?

Para alterar seu código mais facilmente, você vai criar um bloco personalizado.

\--- task \---

Selecione o ator 'Resultado'. Depois clique em `Meus Blocos`{:class="block3myblocks"}, e depois em **Criar um bloco**. Crie um bloco novo e chame de `animar`{:class="block3myblocks"}.

![Ator de Resultado](images/result-sprite.png)

![Criar um bloco chamado animar](images/brain-animate-function.png)

\--- /task \---

\--- task \---

Mova o código `mostre`{:class="block3looks} e `esconda`{:class="block3looks"} do ator 'Resultado', para o bloco `animar`{:class="block3myblocks"}:

![Ator de Resultado](images/result-sprite.png)

```blocks3
define animate
show
wait (1) seconds
hide
```

\--- /task \---

\--- task \---

Tenha certeza de que removeu os blocos `mostre`{:class="block3looks"} e `esconda`{:class="block3looks"} que estão abaixo de **ambos** os blocos `mude para fantasia 
`{:class="block3looks"}.

Em seguida adicione o bloco `animar`{:class="block3myblocks"} abaixo de ambos os blocos `mude para fantasia`{:class="block3looks"}. O seu código agora deve estar parecido com isto:

![Ator de Resultado](images/result-sprite.png)

```blocks3
    when I receive [correct v]
    switch costume to (tick v)
    animate:: custom

    when I receive [wrong v]
    switch costume to (cross v)
    animate:: custom
```

\--- /task \---

Por causa do bloco personalizado `animar`{:class="block3myblocks"}, agora você só precisa fazer uma mudança no seu código se quiser mostrar o ator 'Resultado' um tempo maior ou menor.

\--- task \---

Mude o seu código para que as fantasias de "sinal de visto" ou de "sinal de errado" sejam exibidas por 2 segundos.

\--- /task \---

\--- task \---

Em vez de `mostrar`{:class="block3looks"} e `esconder`{:class="block3looks"} as fantasias de "sinal de visto" ou "sinal de errado", você pode mudar o seu bloco `animar`{:class = "block3myblocks"} para que as fantasias apareçam aos poucos.

![Ator de Resultado](images/result-sprite.png)

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

Você pode melhorar a animação do "sinal de visto" ou "sinal de errado"? Você pode adicionar código para fazer os sinais desaparecerem aos poucos também, ou você pode usar outros efeitos legais:

![screenshot](images/brain-effects.png)