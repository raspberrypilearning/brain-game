## Vytvoření otázek

Začneme s vytvořením náhodných otázek na které bude hráč odpovídat.

\--- task \---

Otevři nový Scratch projekt.

**Online:** otevři nový online Scratch projekt na adrese [rpf.io/scratchon](http://rpf.io/scratchon){:target="_blank"}.

**Offline:** otevři nový projekt v offline editoru.

Pokud chceš Scratch používat offline, stáhni si jej a nainstaluj z adresy [rpf.io/scratchoff](http://rpf.io/scratchoff){:target="_blank"}.

\--- /task \---

\--- task \--- Přidej do hry postavu a pozadí které se ti líbí, například:

![screenshot](images/brain-setting.png)

\--- /task \---

\--- task \--- Ujisti se že máš vybranou postavu. Vytvoř dvě nové proměnné nazvané `číslo 1`{:class="block3variables"} a `číslo 2`{:class="block3variables"}. Do nich si budeš ukládat čísla pro kvízové otázky.

![screenshot](images/giga-sprite.png) ![screenshot](images/brain-variables.png)

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- task \--- Přidej k postavě následující scénář, který do obou `proměnných`{:class="block3variables"} vloží `náhodné`{:class="block3operators"} číslo mezi 2 a 12.

![screenshot](images/giga-sprite.png)

```blocks3
when flag clicked
set [number 1 v] to (pick random (2) to (12))
set [number 2 v] to (pick random (2) to (12))
```

\--- /task \---

\--- task \--- Nyní přidej scénář který se bude hráče `ptát`{:class="block3sensing"} na odpověď a poté mu na `2 sekundy zobrazí bublinu`{:class="block3looks"} s hláškou, jestli jeho odpověď byla správná nebo ne:

![screenshot](images/giga-sprite.png)

```blocks3
when flag clicked
set [number 1 v] to (pick random (2) to (12))
set [number 2 v] to (pick random (2) to (12))

+ ask (join (number 1)(join [ x ] (number 2))) and wait
+ if <(answer) = ((number 1)*(number 2))> then
+ say [yes! :)] for (2) seconds
+ else
+ say [no :(] for (2) seconds
+ end
```

\--- /task \---

\--- task \---

Otestuj si svůj projekt pro oba možné případy: jednou odpověz správně a podruhé špatně.

\--- /task \---

\--- task \---

Vlož svůj kód do bloku `opakuj stále`{:class="block3control"} aby Scratch pokládal hráčům jednu otázku za druhou.

\--- hints \--- \--- hint \---

Musíš do scénáře přidat blok `opakuj stále`{:class="block3control"} a všechen svůj kód s vyjímkou `po kliknutí na zelenou vlajku`{:class="block3control"} vložit dovnitř.

\--- /hint \--- \--- hint \--- Tohle je blok který potřebuješ:

```blocks3
forever
end
```

\--- /hint \--- \--- hint \--- Takto by měl vypadat tvůj upravený kód:

```blocks3
when flag clicked

+ forever
    set [number 1 v] to (pick random (2) to (12))
    set [number 2 v] to (pick random (2) to (12))
    ask (join (number 1)(join [ x ] (number 2))) and wait
    if <(answer) = ((number 1)*(number 2))> then
        say [yes! :)] for (2) seconds
    else
        say [no :(] for (2) seconds
    end
end
```

\--- /hint \--- \--- /hints \---

\--- /task \---