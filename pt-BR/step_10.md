\--- challenge \---

## Desafio: Corrida de 10 pontos

Você pode mudar o seu jogo de modo que, ao invés de ter que responder todas as perguntas possíveis em 30 segundos, o jogador tenha que ver o quão rápido consegue responder 10 questões corretamente?

Para fazer isso, você só vai precisar alterar o código do seu cronômetro. Você consegue ver o que precisa ser mudado?

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