## Adăugați un cronometru

\--- task \--- Creați un cronometru de numărătoare inversă pe Etapa cu ajutorul unei noi variabile numite `timp`{: class = "block3variables"}. Timerul ar trebui să înceapă la 30 de secunde și să conta până la 0 secunde.

![Scena sprite](images/stage-sprite.png)

\--- Sugestii \--- \--- Indicație \---

Creați o variabilă `{`= class = "block3variables"}, numiți-o "timp" și setați-o la `30`.

Apoi adăugați codul pentru a număra `timpul`{: class = "block3variables"} până la 0 în 30 de secunde. Pentru a face acest lucru, scade `1` din `timp`{: class = "block3variables"} la fiecare `1` secunde și repetați acest lucru până la `timp`{: class = "block3variables"} este egal cu `0`.

\--- / hint \--- \--- indiciu \--- Aici sunt blocurile de care ai nevoie:

```blocks3
repeta pana la < >

capăt

wait (1) secunde

schimbare [dată v] de (1)

(timp)

când pavilion apasat

<() = ()>

set [timp v] până la [0]
```

\--- / indiciu \--- \--- indiciu \--- Iată ce ar trebui să arate noul dvs. cod:

```blocks3
când pavilion apasat
set [timp v] până la [30]
repeta pana <(timp) = (0)>
    wait (1) secunde
    schimbare [dată v] de (-1)
final
```

\--- /hint \--- \--- /hints \---

\--- /task \---

\--- task \---

Creați o emisiune `{`} {: class = "block3control"} care trimite mesajul "sfârșit". A `difuzat`{: class = "block3control") este ca un anunț pe un difuzor: acesta poate fi audiat de toate spritele tale. Adăugați blocul `difuzare`{: class = "block3control"} la sfârșitul codului temporizatorului, astfel încât codul să trimită și mesajul "final" atunci când `timp`{: class = "block3variables"} a numărat până la `0`.

![Scena sprite](images/stage-sprite.png)

```blocks3
    difuzare (sfârșitul v)
```

\--- /task \---

\--- task \--- Selectați sprite-ul caracterelor și adăugați un cod astfel încât sprite `oprească celelalte scripturi`{: class = "block3control"} atunci când primește mesajul `{end =`} {block3control} .

![Giga Sprite](images/giga-sprite.png)

```blocks3
    când primesc [end v]
    stop [alte scripturi în sprite v]
```

\--- /task \---

\--- task \---

Testați-vă din nou jocul. Ar trebui să continue să pună întrebări până când timerul a fost numit până la 0.

\--- /task \---