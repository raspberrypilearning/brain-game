## Více her

Nyní přidáme do projektu tlačítko, kterým budou moci hráči tvou hru spustit vícekrát po sobě.

\--- task \--- Vytvoř novou postavu v podobě tlačítka 'Hrát'. Po kliknutí na něj spusť hru.

Tlačítko můžeš nakreslit sám nebo si vyber již hotové z knihovny a uprav jej podle libosti.

![Obrázek tlačítka pro spuštění hry](images/brain-play.png)

\--- /task \---

\--- task \--- Přidej následující kód k postavě tlačítka:

![Obrázek tlačítka](images/button-sprite.png)

```blocks3
    when flag clicked
    show

    when this sprite clicked
    hide
    broadcast (start v)
```

\--- /task \---

Kód obsahuje další blok `vyšli`{:class="block3events"}, který tentokrát odešle zprávu 'start'.

Po spuštění hry zelenou vlajkou se tlačítko ukáže na obrazovce. Když na něj hráč klikne, tlačítko se skryje a odešle zprávu na kterou mohou zareagovat ostatní postavy.

Zatím tvůj kód kód funguje tak, že postava začne hráči pokládat otázky ihned po kliknutí na vlajku. To musíme změnit! Uprav svůj kód tak aby postava začala klást otázky až ve chvíli kdy obdrží `zprávu`{:class="block3events"} 'start'.

\--- task \--- Vyber svou postavu a nahraď v jejím scénaři blok `po kliknutí na zelenou vlajku`{:class="block3events"} za `po obdržení zprávy start`{:class="block3events"}.

![Obrázek postavy](images/giga-sprite.png)

```blocks3
<br />- when flag clicked
+ when I receive [start v]
set [number 1 v] to (pick random (2) to (12))
set [number 2 v] to (pick random (2) to (12))
ask (join (number 1)(join [ x ] (number 2))) and wait
if &lt;(answer) = ((number 1)*(number 2))&gt; then
    say [yes! :)] for (2) seconds
else
    say [nope :(] for (2) seconds
end
```

\--- /task \---

\--- task \---

A nyní je třeba kód pořádně protestovat! Klikni na zelenou vlajku a pak na nové tlačítko 'Hrát'. Pokud vše funguje jak má, hra by měla začít až po kliknutí na tlačítko.

\--- /task \---

Všiml sis že časovač začal odpočítávat hned po kliknutí na zelenou vlajku?

![Časovač spuštěn](images/brain-timer-bug.png)

\--- task \---

Dokážeš změnit kód časovače tak aby odpočet začal až po kliknutí na tlačítko?

\--- /task \---

\--- task \--- Přidej k postavě tlačítka nový kód, který zajistí jeho opětovné vykreslení na konci hry.

![Obrázek tlačítka](images/button-sprite.png)

```blocks3
    when I receive [end v]
    show
```

\--- /task \---

\--- task \---

Pořádně prověř chování tlačítka 'Hrát'. Zahraj si hru několikrát po sobě a zkontroluj, že na konci každé z nich se tlačítko znovu objeví na obrazovce.

Aby sis testování trochu urychlil, můžeš změnit hodnotu `čas`{:class="block3variables"} na menší hodnotu, takže hra bude trvat jen pár sekund.

![Scéna](images/stage-sprite.png)

```blocks3
    set [time v] to [10]
```

\--- /task \---

\--- task \--- Vzhled tlačítka můžeš změnit pokud nad něj najedeš kurzorem myši.

![Tlačítko](images/button-sprite.png)

```blocks3
    when flag clicked
    show
    forever
    if <touching (mouse-pointer v)?> then
        set [fisheye v] effect to (30)
    else
        set [fisheye v] effect to (0)
    end
    end
```

![screenshot](images/brain-fisheye.png) \--- /task \---