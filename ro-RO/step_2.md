## Creați întrebări

Veți începe prin a crea întrebări aleatorii pe care jucătorul trebuie să le răspundă.

\--- proba\---

Deschideți un nou proiect Scratch.

**Online:** deschideți un nou proiect Scratch online la [rpf.io/scratchon](http://rpf.io/scratchon){: target = "_ blank"}.

**Offline:** deschideți un nou proiect în editorul offline.

Dacă trebuie să descărcați și să instalați editorul Scratch offline, îl puteți găsi la [rpf.io/scratchoff](http://rpf.io/scratchoff){: target = "_ blank"}.

\--- /proba\---

\--- task \--- Adăugați un personaj sprite și un fundal pentru jocul dvs. Puteți alege orice doriți! Iată un exemplu:

![captură de ecran](images/brain-setting.png)

\--- /task \---

\--- task \--- Asigurați-vă că ați selectat caracterul tău sprite. Creați două variabile noi, numite `numărul 1`{: class = "block3variables"} și `numărul 2`{: class = "block3variables"}}, pentru a stoca numerele pentru întrebările testului.

![captură de ecran](images/giga-sprite.png) ![captură de ecran](images/brain-variables.png)

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- sarcină \--- Adăugați cod pentru sprite dvs. de caractere pentru a seta ambele `variabile`{: class = "block3variables"} la un `aleatoare`{: class = "block3operators"} număr între 2 și 12.

![captură de ecran](images/giga-sprite.png)

```blocks3
când se dă clic pe pictograma
setează [numărul 1 v] la (alegeți aleatoriu (2) la (12))
setați [numărul 2 v] la (alegeți aleatoriu (2) la (12))
```

\--- /task \---

\--- sarcină \--- Adăugați cod la `întreb`{: class = "block3sensing"} player -ul pentru răspunsul, și apoi `spun timp de 2 secunde`{: class = "block3looks"} dacă răspunsul a fost corect sau gresit:

![captură de ecran](images/giga-sprite.png)

```blocks3
când pavilion a făcut clic
set [numărul 1 v] pentru a (alege aleator (2) până la (12))
set [numărul 2 v] pentru a (alege aleator (2) până la (12))

+ cere (JOIN (numărul 1) (asociază [x] (numărul 2))) și așteptați
+ dacă <(răspuns) = ((numărul 1) * (numărul 2))> apoi
+ :)] pentru (2) secunde
+ altceva
+ spune [no :(] pentru (2) secunde
+ sfârșit
```

\--- /task \---

\--- task \---

Testați-vă proiectul de două ori: răspundeți corect la o întrebare și celălalt incorect.

\--- /task \---

\--- task \---

Adăugați o buclă `pentru totdeauna`{: class = "block3control"} în jurul acestui cod, astfel încât jocul să îi adreseze jucătorului o mulțime de întrebări la rând.

\--- Sugestii \--- \--- Indicație \---

Trebuie să adăugați un bloc `pentru totdeauna`{: class = "block3control"} și să puneți tot codul, cu excepția celor `când blochează`{: class = "block3control"}.

\--- / hint \--- \--- sugestie \--- Aici este blocul de care aveți nevoie:

```blocks3
pentru totdeauna
sfârșit
```

\--- / hint \--- \--- sugestie \--- Aici este ceea ce ar trebui să arate codul dvs.:

```blocks3
când pavilion a făcut clic

+ pentru totdeauna
    set [numărul 1 v] pentru a (alege aleator (2) până la (12))
    set [numărul 2 v] pentru a (alege aleator (2) până la (12))
    Numărul cere ( se alăture ( 1) (asociați [x] (numărul 2))) și așteptați
    dacă <(răspuns) = ((numărul 1) * (numărul 2))> apoi
        spuneți [da! :)] pentru (2) secunde
    altceva
        spune [no :(] pentru (2) secunde
    sfârșitul
sfârșit
```

\--- /hint \--- \--- /hints \---

\--- /task \---