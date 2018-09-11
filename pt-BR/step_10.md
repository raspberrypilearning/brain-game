\--- challenge \---

## Desafio: Corrida até 10 pontos

Você pode mudar o seu jogo, de modo que, em vez de responder a todas as perguntas possíveis em 30 segundos, o jogador tenha que ver o quão rápido consegue responder 10 questões corretamente?

Para fazer isso, você só precisará alterar seu código do temporizador. Você consegue ver o que precisa ser mudado?

```blocks
    quando receber a mensagem [começar v]
    alterar [tempo v] para (30)
    até que <(tempo) = [0]>, repete 
        espera (1) s
        adiciona a [tempo v] o valor (-1)
    end
    difunde a mensagem [acabar v]
```

\--- /challenge \---