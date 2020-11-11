## Desafio: corrida até 10 pontos

Você pode mudar seu jogo para que o jogador, ao invés de responder o maior número de perguntas possível em 30 segundos, responda a 10 perguntas o mais rápido possível.

Para fazer essa mudança, você só precisa alterar o código do cronômetro. Você consegue ver quais blocos precisam ser diferentes?

```blocks3
    when I receive [começar v]
    set [tempo v] to (30)
    repeat until <(tempo) = [0]> ::variable
        wait (1) seconds
        change [tempo v] by (-1)
    end
    broadcast (fim v)
```