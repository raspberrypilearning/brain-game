## Mai multe jocuri

Acum, veți adăuga un buton "Play", astfel încât jucătorul să poată juca jocul dvs. de multe ori.

\--- task \--- Creați un nou buton de joc "Sprite" pe care trebuie să faceți clic pentru a porni un nou joc.

Puteți desena sprite singur, sau puteți edita un sprite din bibliotecă.

![Imagine a butonului de redare](images/brain-play.png)

\--- /task \---

\--- task \--- Adăugați acest cod la butonul dvs. sprite:

![Button sprite](images/button-sprite.png)

```blocks3
    când steagul a făcut clic pe
    arată

    când acest sprite a făcut clic pe
    ascunde
    difuzat (începe v)
```

\--- /task \---

Noul cod include un alt bloc `transmisie`{: class = "block3events"}, care trimite mesajul "start".

Noul cod face ca butonul "Play" să fie afișat atunci când un jucător dă clic pe pavilion. Când jucătorul dă clic pe butonul Sprite, sprite-ul se ascunde și transmite apoi un mesaj pe care pot reacționa alte sprite.

În momentul de față, personajul sprite începe să pună întrebări atunci când jucătorul dă clic pe pavilion. Schimbați codul jocului astfel încât sprite de caractere să înceapă să pună întrebări atunci când primește difuzarea "start" ``{: class = "block3events"}.

\--- task \--- Selectați caracterul dvs. sprite și, în secțiunea sa de cod, înlocuiți `când blițul a făcut clic pe blocul`{: class = "block3events"} cu `atunci când primesc startul`{: class = "block3events" } bloc.

![Sprite de caractere](images/giga-sprite.png)

```blocks3
<br />- atunci când pavilionul a făcut clic pe
+ când primesc [start v]
set [numărul 1 v] la (alegeți aleatoriu 2 la 12)
setați [numărul 2 v] )
cere (JOIN (numărul 1) ( se alăture [x] (numărul 2))) și așteptați
dacă &lt;(răspuns) = ((numărul 1) * (numărul 2))&gt; , apoi
    spun [da! :)] pentru (2) secunde
altceva
    spune [nope :(] pentru (2) secunde
sfarsit
```

\--- /task \---

\--- task \---

Faceți clic pe steagul verde, apoi faceți clic pe noul buton "Redare" pentru a testa dacă funcționează. Ar trebui să vedeți că jocul nu începe înainte de a da clic pe buton.

\--- /task \---

Puteți vedea că cronometrul începe când se face clic pe steagul verde, în loc de când începe jocul?

![Timerul a început](images/brain-timer-bug.png)

\--- task \---

Puteți schimba codul pentru cronometru astfel încât să înceapă cronometrul când player-ul face clic pe buton?

\--- /task \---

\--- task \--- Adăugați codul la butonul dvs. sprite, astfel încât butonul să apară din nou la sfârșitul fiecărui joc.

![Button sprite](images/button-sprite.png)

```blocks3
    când primesc [sfârșitul v]
    arată
```

\--- /task \---

\--- task \---

Testați butonul "Redare" jucând câteva jocuri. Butonul ar trebui să apară la sfârșitul fiecărui joc.

Pentru a testa jocul mai repede, puteți modifica valoarea `timp`{: class = "block3variables"} astfel încât fiecare joc să dureze doar câteva secunde.

![Etapă](images/stage-sprite.png)

```blocks3
    setați ora [v] la [10]
```

\--- /task \---

\--- task \--- Puteți schimba modul în care arată butonul când indicatorul mouse-ului se află peste el.

![Buton](images/button-sprite.png)

```blocks3
    când pavilionul apăsat
    arată
    pentru totdeauna
    dacă <touching (mouse-pointer v)?> apoi
        setați [fishheye v] effect to (30)
    altceva
        set [efect fisheye v] efect la (0)
    sfârșitul

```

![captură de ecran](images/brain-fisheye.png) \--- /task \---