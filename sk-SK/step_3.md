## Pridať časovač

\--- task \--- Pomocou novej premennej nazývanej `čas`{: class = "block3variables"} vytvorte odpočítavanie na štádiu. Časovač by mal začať od 30 sekúnd a odpočítavať na 0 sekúnd.

![Stage sprite](images/stage-sprite.png)

\--- rady \--- \--- názov \---

Vytvorte `premennú`{: class = "block3variables"}, zavolajte jej "time" a nastavte jej hodnotu na `30`.

Potom pridajte kód do počítania `čas`{: class = "block3variables"} do 0 do 30 sekúnd. Vykonajte to, odčítajte `1` z `času`{: class = "block3variables"} každých `1` sekúnd a opakujte to do `času`{: class = "block3variables"} sa rovná `0`.

\--- / tip \--- \--- tip \--- Tu sú bloky, ktoré potrebujete:

```blocks3
opakovať až do < >

koniec

čakania (1) sekundy

zmeny [čas v] o (1)

(čas),

, keď príznak kliknutí

<() = ()>

set [čas v] do [0]
```

\--- / tip \--- \--- tip \--- Tu je to, ako mal by váš nový kód vyzerať:

```blocks3
keď príznak kliknutí
sadu [čas] pre [30]
opakovanie do <(čas) = (0)>
    čakania (1) sekundy
    zmene [čas v] o (-1)
konca
```

\--- / náznak \--- \--- / rady \---

\--- / úloha \---

\--- úloha \---

Vytvorte `vysielanie`{: class = "block3control"}, ktoré odošle správu 'end'. A `vysielanie`{: class = "block3control"} je ako oznámenie cez reproduktor: môže to počuť všetci tvoji sprites. Pridajte blok `vysielania`{: class = "block3control"} na koniec kódu časovača tak, aby kód vysielal a končil, keď `čas`{: class = "block3variables"} započítaval do `0`.

![Stage sprite](images/stage-sprite.png)

```blocks3
    vysielanie (koniec v)
```

\--- / úloha \---

\--- task \--- Vyberte svoj znakový sprite a pridajte nejaký kód tak, aby sprite `zastavil ostatné skripty`{: class = "block3control"}, keď dostane správu `end`{: class = "block3control"} ,

![Giga sprite](images/giga-sprite.png)

```blocks3
    keď dostanem [end v]
    stop [iné skripty v sprite v]
```

\--- / úloha \---

\--- úloha \---

Otestujte svoju hru znova. Mala by sa naďalej klásť otázky, kým sa časovač nezapočíta na hodnotu 0.

\--- / úloha \---