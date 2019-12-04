## Adăugați un cronometru

\--- task \--- Creează o numărătoare inversă pe Scenă cu ajutorul unei noi variabile numite `timp`{: class = "block3variables"}. Cronometrul ar trebui să înceapă la 30 de secunde și să se scurgă până la 0 secunde.

![Scena sprite](images/stage-sprite.png)

\--- hints \--- \--- hint \---

Creează o variabilă `{`= class = "block3variables"}, numește-o "timp" și seteaz-o la `30`.

Apoi adaugă codul pentru a reduce `timpul`{: class = "block3variables"} până la 0 în 30 de secunde. Pentru a face acest lucru, scade `1` din `timp`{: class = "block3variables"} la fiecare `1` secunde și repetă acest lucru până când `timp`{: class = "block3variables"} este egal cu `0`.

\--- /hint \--- \--- hint \--- Aici sunt blocurile de care ai nevoie:

```blocks3
repetă până la < >

sfârșit

așteaptă (1) secunde

schimbă [timp v] cu (1)

(timp)

când faci click pe steagul verde

<() = ()>

setează [timp v] la [0]
```

\--- /hint \--- \--- hint \--- Iată cum ar trebui să arate noul tău cod:

```blocks3
când faci click pe steagul verde
setează [timp v] la [30]
repetă pana <(timp) = (0)>
    așteaptă (1) secunde
    schimbă [timp v] cu (-1)
sfârșit
```

\--- /hint \--- \--- /hints \---

\--- /task \---

\--- task \---

Creează un eveniment `{`} {: class = "block3control"} care transmite mesajul "sfârșit". Un `eveniment`{: class = "block3control") este ca un anunț pe un difuzor: acesta poate fi auzit de toate personajele tale. Adăugați blocul `difuzare`{: class = "block3control"} la sfârșitul codului temporizatorului, astfel încât codul să trimită și mesajul "final" atunci când `timp`{: class = "block3variables"} a numărat până la `0`.

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