\--- challenge \---

## Desafio: Corrida até 10 pontos

Consegues mudar o teu jogo, de modo que, em vez de responder a tantas perguntas quanto possível em 30 segundos, o jogador tenha que ver a rapidez com que consegue responder a 10 perguntas corretamente?

Para fazeres isso, só precisas de alterar o teu código do temporizador. Consegues ver o que necessita ser mudado?

```blocks
    Quando receberes a mensagem [comecar v]
    altera [tempo v] para (30)
    até que <(tempo) = [0]>, repete 
        espera (1) s
        adiciona a [tempo v] o valor (-1)
    end
    difunde a mensagem [acabar v]
```

\--- /challenge \---