## Jocuri multiple

Acum, vei adăuga un buton "Play", astfel încât jucătorul să poată juca jocul tău de mai multe ori.

\--- task \--- Creează un nou buton "Play" pe care jucătorul trebuie să dea click pentru a porni un joc nou.

Poți desena personajul singur sau poți edita un personaj din bibliotecă.

![Imagine a butonului de redare](images/brain-play.png)

\--- /task \---

\--- task \--- Adaugă acest cod la butonul personajului tău:

![Button sprite](images/button-sprite.png)

```blocks3
    când dăm click pe steagul verde
    arată

    când dăm click pe personaj 
    ascunde
    difuzează (începe v)
```

\--- /task \---

Noul cod include un alt bloc `broadcast`{: class = "block3events"}, care trimite mesajul "start".

Noul cod face ca butonul "Play" să fie afișat atunci când un jucător dă clic pe steagul verde. Când jucătorul dă clic pe butonul personajului, personajul se ascunde și transmite apoi un mesaj la care pot reacționa alte personaje.

În acest moment, personajul începe să pună întrebări imediat ce jucătorul dă clic pe steagul verde. Schimbă codul jocului astfel încât personajul să înceapă să pună întrebări atunci când primește mesajul "start" `broadcast`{: class = "block3events"}.

\--- task \--- Selectați caracterul dvs. sprite și, în secțiunea sa de cod, înlocuiți `când blițul a făcut clic pe blocul`{: class = "block3events"} cu `atunci când primesc startul`{: class = "block3events" } bloc.

![Sprite de caractere](images/giga-sprite.png)

```blocks3
<br />- atunci când pavilionul a făcut clic pe
+ când primesc [start v]
set [numărul 1 v] la (alegeți aleatoriu 2 la 12)
setați [numărul 2 v] )
cere (JOIN (numărul 1) ( se alăture [x] (numărul 2))) și așteptați
dacă <(răspuns) = ((numărul 1) * (numărul 2))> , apoi
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