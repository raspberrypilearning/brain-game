## Desafio: corrida até 10 pontos

Podes mudar o teu jogo para que o jogador, em vez de responder o maior número possível de perguntas em 30 segundos, responda 10 perguntas o mais rapidamente possível.

Para fazer esta alteração, só precisas de alterar o teu código do temporizador. Podes ver quais sāo os blocos que precisam de ser diferentes?

```blocks3
    Quando receberes a mensagem [começar v]
    altera [tempo v] para (30)
    até que <(tempo) = [0]> , repete 
        espera (1) s
        adiciona a [tempo v] o valor (-1)
    end
    difunde a mensagem (acabar v)
```