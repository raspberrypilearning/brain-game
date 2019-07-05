## Přidej časovač

\--- task \--- Vytvoř novou proměnnou `čas`{:class="block3variables"}, která bude reprezentovat časovač. Nastav ji na 30 vteřin a odpočítávej až k 0.

![Postava](images/stage-sprite.png)

\--- hints \--- \--- hint \---

Vytvoř `proměnnou`{:class="block3variables"}, pojmenuj ji 'čas' a nastav její hodnotu na `30`.

Potom přidej kód který bude zmenšovat `čas`{:class="block3variables"} až na 0. Mužeš to provést tak, že každou `1` sekundu odečteš od `čas`{:class="block3variables"} číslo `1`. A to tak dlouho, dokud `čas`{:class="block3variables"} nebude roven `0`.

\--- /hint \--- \--- hint \--- Tohle jsou bloky které potřebuješ:

```blocks3
repeat until < >

end

wait (1) seconds

change [time v] by (1)

(time)

when flag clicked

<() = ()>

set [time v] to [0]
```

\--- /hint \--- \--- hint \--- Takto by měl vypadat tvůj kód:

```blocks3
when flag clicked
set [time v] to [30]
repeat until <(time) = (0)>
    wait (1) seconds
    change [time v] by (-1)
end
```

\--- /hint \--- \--- /hints \---

\--- /task \---

\--- task \---

Vlož blok `vyšli zprávu`{:class="block3control"}, který odešle zprávu 'konec'. `Vysílání`{:class="block3control"} si můžeš představit jako hlášení místního rozhlasu: hlasitě do širého okolí vyšleš zprávu, kterou uslyší všechny tvé postavy. Blok `vyšli zprávu`{:class="block3control"} přidej na konec časovače tak, aby se zpráva 'konec' odeslala až ve chvíli kdy proměnná `čas`{:class="block3variables"} bude obsahovat hodnotu `0`.

![Postava](images/stage-sprite.png)

```blocks3
    broadcast (end v)
```

\--- /task \---

\--- task \--- Vyber svou postavu a přidej k ní kód který po obdržení zprávy `konec`{:class="block3control"} `zastaví ostatní scénáře`{:class="block3control"}.

![Postava Giga](images/giga-sprite.png)

```blocks3
    when I receive [end v]
    stop [other scripts in sprite v]
```

\--- /task \---

\--- task \---

Znovu si svou hru otestuj. Měla by ti pokládat jednu otázku za druhou až do chvíle, kdy časovač klesne na 0.

\--- /task \---