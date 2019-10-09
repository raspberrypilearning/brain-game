## Dodaj grafiko

Trenutno figura lika na odgovor igralca reče zgolj `da! :)` ali `ne :(`. Dodaj nekaj grafike, da bo igralec vedel ali je odgovor pravilen ali ne.

\--- task \---

Ustvari novo figuro z imenom 'Rezultat' in ji dodaj videz 'kljukice' in 'križca'.

![Figura z videzom kljukice in križca](images/brain-result.png)

\--- /task \---

\--- task \---

Spremeni kodo figure lika na tak način, da bo namesto tega, da nekaj reče, `objavil` {:class="block3events"} sporočilo 'pravilno' ali 'narobe'.

![Figura lika](images/giga-sprite.png)

```blocks3
če <(odgovor) = ((število 1)*(število 2))> potem

- reci [da! :)] za (2) sekund
+ objavi (pravilno v)
sicer
- reci [ne :(] za (2) sekund
+ objavi (narobe v)
konec
```

\--- /task \---

\--- task \---

Ta sporočila lahko sedaj uporabiš, da `pokažeš`{:class="block3looks"} videza 'kljukica' ali 'križec'. Dodaj sledečo kodo figuri 'Rezultat':

![Figura rezultata](images/result-sprite.png)

```blocks3
    ko prejmem [pravilno v]
  zamenjaj videz na (kljukica v)
  pokaži
  počakaj (1) sekund
  skrij

ko prejmem [narobe v]
  zamenjaj videz na (križec v)
  pokaži
  počakaj (1) sekund
  skrij

ko kliknemo na zastavico
  skrij
```

\--- /task \---

\--- task \--- Ponovno preizkusi igro. Kadar odgovoriš pravilno, bi sedaj moral videti kljukico, kadar odgovoriš narobe, pa križec!

![Kljukica za pravilen, križec za napačen odgovor](images/brain-test-answer.png)

\--- /task \---

Si opazil, da sta kodi za `ko prejmem pravilno`{:class="block3events"} in `ko prejmem narobe` {:class="block3events"} skorajda enaki?

Za bolj enostavno spreminjanje kode boš ustvaril svoj blok.

\--- task \---

Izberi figuro 'Rezultat'. Nato klikni na `Moji bloki`{:class="block3myblocks"} in potem še na **Ustvari blok**. Ustvari nov blok in ga poimenuj `animiraj`{:class="block3myblocks"}.

![Figura rezultata](images/result-sprite.png)

![Ustvari blok, imenovan animiraj](images/brain-animate-function.png)

\--- /task \---

\--- task \--- Premakni kodo, ki `pokaže`{:class="block3looks"} in `skrije`{:class="block3looks"} figuro 'Rezultat' v blok `animiraj`{:class="block3myblocks"}:

![Figura rezultata](images/result-sprite.png)

```blocks3
definiraj animiraj
pokaži
počakaj (1) sekund
skrij
```

\--- /task \---

\--- task \--- Prepričaj se, da si umaknil bloka `pokaži`{:class="block3looks"} in `skrij`{:class="block3looks"} pod **obema** blokoma `zamenjaj videz`{:class="block3looks"}.

Potem dodaj blok `animiraj`{:class="block3myblocks"} pod oba bloka `zamenjaj videz`{:class="block3looks"}. Tovja koda naj bo videti tako:

![Figura rezultata](images/result-sprite.png)

```blocks3
    ko prejmem [pravilno v]
  zamenjaj videz na (kljukica v)
  animiraj:: custom

ko prejmem [narobe v]
  zamenjaj videz na (križec v)
  animiraj:: custom
```

\--- /task \---

Zaradi lastnega bloka `animiraj`{:class="block3myblocks"}, lahko sedaj opraviš le eno eno spremembo kode, če želiš prikazati figuro 'Rezultat' za daljši ali krajši čas.

\--- task \---

Spremeni kodo, tako da se bosta videza 'kljukica' in 'križec' prikazala za dve sekundi.

\--- /task \---

\--- task \--- Namesto tega, da se videza 'kljukica' in 'križec' `pokažeta`{:class="block3looks"} ali `skrijeta`{:class="block3looks"}, lahko spremeniš blok `animiraj`{:class="block3myblocks"}, tako da se figura prelije v sliko.

![Figura rezultata](images/result-sprite.png)

```blocks3
    definiraj animiraj
  nastavi učinek [duh v] na (100)
  pokaži
  ponovi (25) krat
    spremni učinek [duh] za (-4)
  konec
  skrij
```

\--- /task \---

Ali lahko izboljšaš animacijo 'kljukice' ali 'križca'? Lahko bi dodal kodo, ki bo poskrbela, da se bodo videzi tudi mehko izginili ali pa lahko uporabiš druge zanimive učinke:

![posnetek zaslona](images/brain-effects.png)