## Desafio: corrida até 10 pontos

Você pode mudar seu jogo para que o jogador, ao invés de responder o maior número de perguntas possível em 30 segundos, responda a 10 perguntas o mais rápido possível.

Para fazer essa mudança, você só precisa alterar o código do cronômetro. Você consegue ver quais blocos precisam ser diferentes?

```blocks3
    when I receive [start v]
    set [time v] to (30)
    repeat until <(time) = [0]>
        wait (1) seconds
        change [time v] by (-1)
    end
    broadcast (end v)
```