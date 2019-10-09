## Dodaj časovnik

\--- task \--- Na odru ustvari štoparico, ki bo odštevala, s pomočjo nove spremenljivke imenovane `čas`{:class="block3variables"}. Ta časovnik naj začne pri 30 sekundah in odšteva do 0 sekund.

![Odrska figura](images/stage-sprite.png)

\--- hints \--- \--- hint \---

Ustvari `spremenljivko`{:class="block3variables"}, poimenuj jo 'čas' in nastavi njeno vrednost na `30`.

Potem dodaj kodo, ki bo odštevala `čas`{:class="block3variables"} do 0 v 30 sekundah. V ta namen odštej `1` od `čas`{:class="block3variables"} vsako `1` sekundo in to ponavljaj dokler `čas`{:class="block3variables"} ni enak 0 `0`.

\--- /hint \--- \--- hint \--- To so bloki kode, ki jih potrebuješ:

```blocks3
ponavljaj < >

konec

počakaj (1) sekund

spremeni [čas v] by (-1)

(čas)

ko kliknemo na zastavico

<() = ()>

nastavi [čas v] na [0]
```

\--- /hint \--- \--- hint \--- Tako bi morala izgledati tvoja koda:

```blocks3
ko kliknemo na zastavico
nastavi [čas v] na [30]
ponavljaj dokler <(čas) = (0)>
  počakaj (1) sekund
  spremeni [čas v] za (-1)
konec
```

\--- /hint \--- \--- /hints \---

\--- /task \---

\--- task \---

Sedaj `objavi`{:class="block3control"} sporočilo 'konec'. `Objava`{:class="block3control"} je kot oznanilo preko zvočnika, ki ga lahko slišijo vse tvoje figure. Dodaj blok `objavi`{:class="block3control"} na konec kode časovnika, tako da bo koda objavila sporočilo 'konec', ko bo `čas`{:class="block3variables"} dosegel `0`.

![Odrska figura](images/stage-sprite.png)

```blocks3
    objavi (konec v)
```

\--- /task \---

\--- task \--- Izberi figuro tvojega lika in ji dodaj ustrezno kodo, da bo figura `zaustavila druge ukaze`{:class="block3control"}, ko bo prejela sporočilo `konec`{:class="block3control"}.

![Giga figura](images/giga-sprite.png)

```blocks3
    ko prejmem [konec v]
  ustavi [ostale ukaze za to figuro v]
```

\--- /task \---

\--- task \---

Ponovno preizkusi svojo igro. Še naprej bi morala postavljati vprašanje, dokler časovnik ne pride do 0.

\--- /task \---