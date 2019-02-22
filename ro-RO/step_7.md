## Adăugați grafică

În momentul de față, personajul sprite spune doar `da! :)` sau `nu :(` la răspunsurile jucătorului. Adăugați unele grafice pentru a lăsa jucătorul să știe dacă răspunsul lor este corect sau incorect.

\--- proba\---

Creați un nou sprite numit "Rezultat" și dați-i un costum "bifați / verificați" și "încrucișați".

![Sprite cu bici și costume încrucișate](images/brain-result.png)

\--- /task \---

\--- task \---

Schimbați codul sprite al caracterului, astfel încât, în loc să spună ceva jucătorului, acesta `transmite`{: class = "block3events"} mesajele "corecte" sau "greșite".

![Sprite de caractere](images/giga-sprite.png)

```blocks3
dacă <(răspuns) = ((numărul 1) * (numărul 2))> atunci

- spuneți [da! :)] pentru (2) secunde
+ broadcast (v corect)
altceva
- spun [nope :(] pentru (2) secunde
+ broadcast (v greșit)
capăt
```

\--- /task \---

\--- task \---

Acum puteți utiliza aceste mesaje de la `show -`{: class = „block3looks“} „capusa“ sau costum „cruce“. Adăugați următorul cod la sprite "Rezultat":

![Sprite rezultat](images/result-sprite.png)

```blocks3
    atunci când primesc [v corect]
    costum comutator la (căpușe v)
    arată
    wait (1) secunde
    ascunde

    atunci când primesc [v greșit]
    costum comutator la (cruce v)
    arată
    așteptați (1) secunde
    ascunde

    când steagul a făcut clic pe
    ascunde
```

\--- /task \---

\--- task \--- Testați-vă din nou jocul. Ar trebui să vedeți bifarea ori de câte ori răspundeți la o întrebare corectă și crucea ori de câte ori răspundeți incorect!

![Bifați pentru corect, cruce pentru răspuns greșit](images/brain-test-answer.png)

\--- /task \---

Puteți vedea că codul pentru `când primesc corect`{: class = "block3events"} și `când primesc greșit`{: class = "block3events"} este aproape identic?

Deci, puteți schimba codul mai ușor, veți crea un bloc personalizat.

\--- task \---

Selectați sprite "Rezultat". Apoi faceți clic pe `My Blocks`{: class = "block3myblocks"}, apoi pe **Faceți un bloc**. Creați un nou bloc și apelați-l `animați`{: class = "block3myblocks"}.

![Sprite rezultat](images/result-sprite.png)

![Creați un bloc numit animați](images/brain-animate-function.png)

\--- /task \---

\--- sarcina \--- mutați codul la `arată`{: class = "block3looks"} și `ascunde`{: class = "block3looks"} "Sprite rezultat" în `animate`{: class = bloc3myblocks "} bloc:

![Sprite rezultat](images/result-sprite.png)

```blocks3
defini animat
arată
așteptați (1) secunde
ascunde
```

\--- /task \---

\--- Sarcina \--- Asigurați - vă că ați scos `afișează`{: class = "block3looks"} și `ascunde`{: class = "block3looks"} blocuri de mai jos , **ambele** din `costumului comutator`{: class = "block3looks"} blocuri.

Apoi adăugați blocul `animat`{: class = "block3myblocks"} deasupra ambelor blocuri de `comutatoare de costum`{: class = "block3looks"}. Codul dvs. ar trebui să arate astfel:

![Sprite rezultat](images/result-sprite.png)

```blocks3
    când primesc costumul de schimb [corect v]
    comuta la (bifați v)
    animați :: personalizat

    când primesc [greșit v]
    costum de comutare la (cruce v)
    animate :: personalizat
```

\--- /task \---

Din cauza blocului personalizat `animate`{: class = "block3myblocks"}, acum trebuie doar să faceți o schimbare a codului dvs. dacă doriți să afișați costumele Sprite "Rezultat" un timp mai lung sau mai scurt.

\--- task \---

Modificați codul astfel încât costumele "bifați" sau "încrucișați" să fie afișate timp de 2 secunde.

\--- /task \---

\--- Sarcina \--- În loc de `prezentând`{: class = "block3looks"} și `ascund`{: class = "block3looks"} 'capusei' sau costumele 'cruce', ai putea schimba `insufletit`{block: block3myblocks}}, astfel încât costumele să se estompeze.

![Sprite rezultat](images/result-sprite.png)

```blocks3
    defineste animat
    set [ghost v] efect la (100)
    arata
    repeta (25)
        schimba [ghost v] efect prin (-4)
    end
    ascunde
```

\--- /task \---

Puteți îmbunătăți animația graficei "tick" sau "cross"? Puteți adăuga codul pentru a face costumele să se estompeze, de asemenea, sau puteți utiliza alte efecte interesante:

![captură de ecran](images/brain-effects.png)