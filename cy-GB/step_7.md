## Ychwanegu graffeg

Yn lle bod dy gymeriad ond yn dweud `ie! :)` neu `na :(`, beth am ychwanegu peth graffeg fel bod y chwareuwr yn gwybod os yw'r ateb yn gywir neu anghywir.

\--- task \---

Bydd angen creu corlun newydd o’r enw ‘Canlyniad’, yn cynnwys gwisg ‘tic’ a ‘chroes’.

![Corlun tic a chroes](images/brain-result.png)

\--- /task \---

\--- task \---

Newida côd dy gymeriad, fel ei fod yn `darlledu`{:class="block3events"} negeseuon 'cywir' ac 'anghywir'.

![Corlun cymeriad](images/giga-sprite.png)

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

Fe alli di nawr ddefnyddio’r negeseuon yma i `ddangos`{:class="block3looks"} y wisg ‘tic’ neu ‘groes’. Ychwanega’r côd yma i dy gorlun ‘Canlyniad’:

![Corlun canlyniad](images/result-sprite.png)

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

\--- task \--- Profa dy gêm eto. Fe ddyle ti weld tic pan gei di ateb yn gywir, a chroes pan gei di ateb yn anghywir!

![Tic i cywir, croes i anghywir](images/brain-test-answer.png)

\--- /task \---

Wyt ti wedi sylwi fod y côd `pan dderbyniaf cywir`{:class="block3events"} a `pan dderbyniaf anghywir`{:class="block3events"} bron yn union yr un peth?

Fe wnawn ni greu gweithred i wneud hi’n hawdd i ti wneud newidiadau i dy gôd.

\--- task \---

Dewisa'r corlun 'Canlyniad'. Clicia `Mwy o flociau`{:class="block3myblocks"} yna **Creu Bloc**. Bydd angen creu bloc newydd o’r enw `animeiddio`{:class="block3myblocks"}.

![Corlun canlyniad](images/result-sprite.png)

![Creu bloc o'r enw animeiddio](images/brain-animate-function.png)

\--- /task \---

\--- task \--- Symuda'r côd i `ddangos`{:class="block3looks"} a `chuddio`{:class="block3looks"} y 'Canlyniad' yn y bloc `animeiddio`{:class="block3myblocks"}:

![Corlun canlyniad](images/result-sprite.png)

```blocks3
define animate
show
wait (1) seconds
hide
```

\--- /task \---

-- task \--- Sicrha dy fod wedi tynnu'r blociau `dangos`{:class="block3looks"} a `chuddio`{:class="block3looks"} o dan **y ddau floc** o'r `newid gwisgoedd`{:class="block3looks"}.

Yna ychwanega'r bloc `animeiddio`{:class="block3myblocks"} o dan y ddau floc `newid gwisgoedd`{:class="block3looks"}. Fe ddylai dy gôd edrych fel hyn:

![Corlun canlyniad](images/result-sprite.png)

```blocks3
    when I receive [correct v]
    switch costume to (tick v)
    animate:: custom

    when I receive [wrong v]
    switch costume to (cross v)
    animate:: custom
```

\--- /task \---

Oherwydd y bloc `animeiddio`{:class="block3myblocks"}, rwyt ti ond angen gwneud un newid i dy gôd os wyt ti eisiau dangos gwisg 'Canlyniad' dy gorlun am amser llai neu hirach.

\--- task \---

Newida dy gôd fel bod y wisg 'tic' neu 'groes' yn ymddangos am 2 eiliad.

\--- /task \---

\--- task \--- Yn hytrach na `dangos`{:class="block3looks"} a `chuddio`{:class="block3looks"} y wisg 'tic' neu 'groes', fe alli di newid dy floc`animeiddio`{:class="block3myblocks"} fel bod y wisg yn pylu mewn.

![Corlun canlyniad](images/result-sprite.png)

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

Alli di wella animeiddiad y 'tic' a'r 'groes'? Fe alli di ychwanegu côd fel bod y wisg yn pylu allan hefyd, neu ddefnyddio effeithiau cŵl arall:

![sgrinlun](images/brain-effects.png)