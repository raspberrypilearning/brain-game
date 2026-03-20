## Ychwanegu Amserydd

--- task ---

Byddwn yn creu amserydd ar y Llwyfan gyda chymorth newidyn newydd i'r enw `amser`{:class="block3variables"}. Fe ddylai'r amserydd gychwyn ar 30 eiliad a chyfrif lawr i 0 eiliad.

![Corlun llwyfan](images/stage-sprite.png)

--- hints ---
--- hint ---

Creu `newidyn`{:class="block3variables"}, ei alw'n 'amser', a gosod ei werth i `30`.

Yna ychwanegu côd i gyfrif `amser`{:class="block3variables"} lawr i 0 o 30 eiliad. I wneud hyn, bydd angen tynnu `1` o `amser`{:class="block3variables"} bob `1` eiliad, ac ail-adrodd hyn tan bod `amser`{:class="block3variables"} yn cyfateb â `0`.

--- /hint ---

--- hint ---

Dyma'r blociau rwyt ti eu hangen:

```blocks3
repeat until < >

end

wait (1) seconds

change [amser v] by (1)

(amser)

when flag clicked

<() = ()>

set [amser v] to [0]
```

--- /hint ---

--- hint ---

Dyma sut ddylai dy gôd edrych:

```blocks3
when flag clicked
set [amser v] to [30]
repeat until <(amser) = (0)> 
  wait (1) seconds
  change [amser v] by (-1)
end
```

--- /hint ---

--- /hints ---

--- /task ---

--- task ---

Creu `darllediad`{:class="block3control"} sy'n anfon y neges 'diwedd'. Mae `darllediad`{:class="block3control"} fel cyhoeddiad dros uchelseinydd: mae modd i bob corlun ei glywed. Ychwanega'r bloc `darllediad`{:class="block3control"} i ddiwedd côd dy amserydd fel bod y côd yn anfon neges 'diwedd' pan fod yr `amser`{:class="block3variables"} yn cyrraedd `0`.

![Corlun llwyfan](images/stage-sprite.png)

```blocks3
    broadcast (diwedd v)
```

--- /task ---

--- task ---

Dewisa dy gymeriad ac ychwanega gôd fel bod y corlun yn `stopio sgriptiau eraill`{:class="block3control"} pan mae'n derbyn y neges `diwedd`{:class="block3control"}.

![Corlun giga](images/giga-sprite.png)

```blocks3
    when I receive [diwedd v]
    stop [sgriptiau eraill yn y ciplun v]
```

--- /task ---

--- task ---

Profa dy gêm eto. Fe ddylai barhau i ofyn cwestiynau tan bod yr amserydd yn cyfrif lawr i 0.

--- /task ---
