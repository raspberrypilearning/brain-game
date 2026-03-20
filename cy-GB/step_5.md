## Gemau lluosog

Fe wnawn ni ychwanegu botwm ‘chwarae’ i dy gêm fel dy fod di’n gallu chwarae sawl gwaith.

--- task ---

Bydd angen creu corlun botwm ‘Chwarae’, sef beth fydd y chwareuwr yn clicio i ddechrau gêm newydd.

Fe alli di ei lunio dy hunan, neu olygu corlun o lyfrgell Scratch.

![Llun o'r botwm chwarae](images/brain-play.png)

--- /task ---

--- task ---

Ychwanega'r côd yma i gorlun dy fotwm:

![Corlun botwm](images/button-sprite.png)

```blocks3
when flag clicked
show

when this sprite clicked
hide
broadcast (ddechrau v)
```

--- /task ---

Mae'r côd newydd yma yn cynnwys bloc arall `darlledu`{:class="block3events"}, sydd yn anfon neges i 'ddechrau'.

Mae'r côd newydd yn gwneud i'r corlun 'Chwarae' ymddangos pan mae'r chwareuwr yn clicio ar y faner. Pan fydd y botwm yn cael ei glicio, fe fydd yn cuddio a darlledu neges fydd yn cychwyn y gêm.

Ar hyn o bryd, mae'r cymeriad yn gofyn cwestiynau pan mae'r chwareuwr yn clicio ar y faner. Bydd angen i ti olygu côd dy gymeriad fel bod y gêm yn cychwyn pan mae’n derbyn neges `dechrau`{:class="block3events"}.

--- task ---

Dewisa dy gymeriad, ac yn yr adran gôd, ailosoda `pan fo baner wedi ei glicio`{:class="block3events"} gyda `pan dderbyniaf dechrau`{:class="block3events"}.

![Corlun cymeriad](images/giga-sprite.png)

```blocks3
- when flag clicked
+ when I receive [ddechrau v]
set [rhif 1 v] to (pick random (2) to (12))
set [rhif 2 v] to (pick random (2) to (12))
ask (join (rhif 1) (join [ x ] (rhif 2))) and wait
if <(answer) = ((rhif 1) * (rhif 2))> then 
  say [Ie! :)] for (2) seconds
else 
  say [Na :(] for (2) seconds
end
end
```

--- /task ---

--- task ---

Clicia’r faner werdd ac yna clicia dy fotwm 'chwarae' newydd i’w brofi. Ni ddylai’r gêm gychwyn tan fod y botwm yn cael ei glicio.

--- /task ---

A wnes di sylwi fod yr amserydd yn cychwyn pan mae’r faner werdd wedi ei chlicio, ond nid pan mae’r gêm yn cychwyn?

![Amserydd wedi dechrau](images/brain-timer-bug.png)

--- task ---

Alli di newid y côd yr amserydd fel fod yr amserydd yn cychwyn pan mae'r chwareuwr yn clicio ar y botwm?

--- /task ---

--- task ---

Fe alli di nawr ychwanegu côd i dy fotwm i’w ddangos eto ar ddiwedd pob gêm.

![Corlun botwm](images/button-sprite.png)

```blocks3
	when I receive [diwedd v]
	show
```

--- /task ---

--- task ---

Profa dy fotwm 'chwarae' trwy chwarae cwpwl o gemau. Fe ddyle ti sylwi fod y botwm chwarae yn dangos ar ôl pob gêm.

I wneud y profi yn gynt, fe alli di leihau pob gêm trwy newid gwerth yr `amser`{:class="block3variables"} fel fod pob gêm ond yn para rhai eiliadau.

![Llwyfan](images/stage-sprite.png)

```blocks3
    set [amser v] to [10]
```

--- /task ---

--- task ---

Fe alli di newid sut mae'r botwm yn edrych pan mae'r llygoden arno.

![Botwm](images/button-sprite.png)

```blocks3
when flag clicked
show
forever 
  if <touching (pwyntydd llygoden v) ?> then 
    set [llygad pysgodin v] effect to (30)
  else 
    set [llygad pysgodin v] effect to (0)
  end
end
```

![sgrinlun](images/brain-fisheye.png)

--- /task ---
