## Přidej grafiku

Zatím tvá postava reaguje na hráčovy odpovědi bublinkou `jo! :)` nebo `ne :(`. Pojďme hru vylepšit novou grafikou ze které hráč pozná jestli jeho odpověď byla správná nebo ne.

\--- task \---

Vytvoř novou postavu 'Výsledek' a přidej ji kostým 'Fajfka' a 'Křížek'.

![Postava s kostýmem fajfky a křížku](images/brain-result.png)

\--- /task \---

\--- task \---

Uprav scénář u postavy tak, aby namísto povídání odesílala `zprávu`{:class="block3events"} 'správně' nebo 'špatně'.

![Postava](images/giga-sprite.png)

```blocks3
if <(answer) = ((number 1)*(number 2))> then

- say [yes! :)] for (2) seconds
+ broadcast (correct v)
else
- say [nope :(] for (2) seconds
+ broadcast (wrong v)
end
```

\--- /task \---

\--- task \---

Teď můžeš díky zprávám `zobrazit` kostým 'fajfky' nebo 'křížku'. Přidej následující kód ke scénaři postavy 'Výsledek':

![Postava Výsledek](images/result-sprite.png)

```blocks3
    when I receive [correct v]
    switch costume to (tick v)
    show
    wait (1) seconds
    hide

    when I receive [wrong v]
    switch costume to (cross v)
    show
    wait (1) seconds
    hide

    when flag clicked
    hide
```

\--- /task \---

\--- task \--- Čas na testování! Po každé správné odpovědi by se ti měla zobrazit fajka a křížek po každé chybě.

![Fajfka pro správnou, křížek pro špatnou odpověď](images/brain-test-answer.png)

\--- /task \---

Všiml sis že kód pro `po obdržení zprávy správně`{:class="block3events"} a `po obdržení zprávy špatně`{:class="block3events"} je skoro stejný?

Aby se nám v budoucnu kód lépe spravoval uděláme z něj tzv. vlastní blok.

\--- task \---

Vyber postavu 'Výsledek'. Klikni do sekce `Moje bloky`{:class="block3myblocks"} a pak na na tlačítko **Vytvořit blok**. Vytvoř nový blok a pojmenuj jej `animuj`{:class="block3myblocks"}.

![Postava Výsledek](images/result-sprite.png)

![Vytvoř vlastní blok s názvem animuj](images/brain-animate-function.png)

\--- /task \---

\--- task \--- Přesuň kód který `zobrazoval`{:class="block3looks"} a `schovával`{:class="block3looks"} postavu 'Výsledek' do bloku `animuj`{:class="block3myblocks"}:

![Postava Výsledek](images/result-sprite.png)

```blocks3
define animate
show
wait (1) seconds
hide
```

\--- /task \---

\--- task \--- Zkontroluj že jsi opravdu odstranil bloky `ukaž se`{:class="block3looks"} a `skryj se`{:class="block3looks"} pro **obě** verze bloku `změň kostým`.

A teď přidej blok `animuj`{:class="block3myblocks"} k oboum blokům `změň kostým`{:class="block3looks"}. Tvůj kód by měl vypadat takto:

![Postava Výsledek](images/result-sprite.png)

```blocks3
    when I receive [correct v]
    switch costume to (tick v)
    animate:: custom

    when I receive [wrong v]
    switch costume to (cross v)
    animate:: custom
```

\--- /task \---

Když by si chtěl zobrazit postavu 'Výsledek' na delší či kratší dobu, budeš teď díky vlastnímu bloku `animuj`{:class="block3myblocks"} muset upravit pouze jediné místo v kódu.

\--- task \---

Uprav kód tak aby se kostým 'Fajfka' nebo 'Křížek' zobrazil na 2 sekundy.

\--- /task \---

\--- task \--- Co kdyby se kostým Fajfky či Křížku namísto okamžitého `zobrazení`{:class="block3looks"} pomalinku, jakoby z mlhy, objevoval? Stačí upravit blok `animuj`{:class="block3myblocks"}.

![Postava Výsledek](images/result-sprite.png)

```blocks3
    define animate
    set [ghost v] effect to (100)
    show
    repeat (25)
        change [ghost v] effect by (-4)
    end
    hide
```

\--- /task \---

Dokázal by si animaci dále vylepšit? Můžeš například použít opačný efekt i při mizení postavy, anebo vymysli svůj vlastní způsob s použitím některého z efektů:

![screenshot](images/brain-effects.png)