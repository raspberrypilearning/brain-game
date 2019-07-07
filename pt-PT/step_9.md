## Desafio: corrida até 10 pontos

Podes mudar o teu jogo para que o jogador, em vez de responder o maior número possível de perguntas em 30 segundos, responda 10 perguntas o mais rapidamente possível.

Para fazer esta alteração, só precisas de alterar o teu código do temporizador. Podes ver quais sāo os blocos que precisam de ser diferentes?

```blocks3
    when I receive [start v]
    set [time v] to (30)
    repeat until <(time) = [0]>
        wait (1) seconds
        change [time v] by (-1)
    end
    broadcast (end v)
```