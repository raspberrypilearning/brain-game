## Adicionar um cronômetro

\--- task \---

Crie um cronômetro de contagem regressiva no palco com a ajuda de uma nova variável chamada `tempo`{:class="block3variable"}. O cronômetro deve começar em 30 segundos e contar até 0 segundos.

![Ator palco](images/stage-sprite.png)

\--- hints \---

\--- hint \---

Crie uma `variável`{:class="block3variables"}, chamada 'tempo', e defina o seu valor para `30`.

Em seguida, adicione código para diminuir o `tempo` {:class="block3variables"} até 0 em 30 segundos. Para fazer isso, subtraia `1` do `tempo`{:class="block3variables"} a cada `1` segundo, e repita até que o `tempo`{:class="block3variables"} seja igual a `0`.

\--- /hint \---

\--- hint \---

Aqui estão os blocos que você precisa:

```blocks3
repeat until < >

end

wait (1) seconds

change [time v] by (1)

(time)

when flag clicked

<() = ()>

set [time v] to [0]
```

\--- /hint \---

\--- hint \---

É assim que seu novo código deve estar:

```blocks3
when flag clicked
set [time v] to [30]
repeat until <(time) = (0)>
    wait (1) seconds
    change [time v] by (-1)
end
```

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

Crie uma `transmita`{:class="block3control"} que envie a mensagem 'fim'. Um `transmita`{:class="block3control"} é como um anúncio em um alto-falante: pode ser ouvido por todos os seus atores. Add the `broadcast`{:class="block3control"} block to the end of the timer code so that the code will send an 'end' message when the `time`{:class="block3variables"} has counted down to `0`.

![Ator palco](images/stage-sprite.png)

```blocks3
    broadcast (end v)
```

\--- /task \---

\--- task \---

Selecione o seu ator de personagem e adicione um código para que o ator `pare outros scripts`{:class="block3control"} quando receber a mensagem `fim`{:class="block3control"}.

![Ator Giga](images/giga-sprite.png)

```blocks3
    quando recebo [fim v]
  pare [outros scripts no objeto v]
```

\--- /task \---

\--- task \---

Teste seu jogo novamente. Ele deve continuar fazendo perguntas até que o cronômetro chegue a 0.

\--- /task \---