\--- challenge \---

## Desafio: Corrida até 10 pontos

Você pode mudar o seu jogo, de modo que, em vez de responder a todas as perguntas possíveis em 30 segundos, o jogador tenha que ver o quão rápido consegue responder 10 questões corretamente?

To do this, you'll only need to change your timer code. Can you see what needs to be changed?

```blocks
    when I receive [start v]
    set [time v] to (30)
    repeat until <(time) = [0]>
        wait (1) secs
        change [time v] by (-1)
    end
    broadcast [end v]
```

\--- /challenge \---