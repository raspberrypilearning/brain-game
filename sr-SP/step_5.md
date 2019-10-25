## Мултипле гамес

Сада ћете додати 'Плаи' дугме, тако да играч може играти вашу игру много пута.

\--- таск \--- Направите нови 'Плаи' дугме за играње које играч мора кликнути да би покренуо нову игру.

Можете сами нацртати сприте или уредити сприте из библиотеке.

![Слика дугмета за репродукцију](images/brain-play.png)

\--- /задатак \---

\--- задатак \--- Додајте овај код свом дугмету:

![Буттон сприте](images/button-sprite.png)

```blocks3
    када је флаг кликнуо
    прикажи

    када је овај сприте кликнуо
    сакриј
    емитовање (старт в)
```

\--- /задатак \---

Нови код укључује још један `емитовани`{: цласс = "блоцк3евентс"} блок, који шаље поруку 'старт'.

Нови код чини 'Плаи' дугме сприте схов када играч кликне на заставу. Када играч кликне на дугме сприте, сприте скрива и затим емитује поруку на коју други духови могу да реагују.

У овом тренутку, сприте ликова почиње да поставља питања када играч кликне на заставу. Промените код игре тако да Сприте знакова почне да поставља питања када прими 'старт' `емитовање`{: цласс = "блоцк3евентс"}.

\--- задатак \--- Одаберите свој знак и, у одјељку кода, замијените `када је заставица кликнула`{: цласс = "блоцк3евентс"} блок с `када примим старт`{: цласс = "блоцк3евентс" } блокирати.

![Цхарацтер сприте](images/giga-sprite.png)

```blocks3
<br />- када је заставица кликнула
+ када примим [старт в]
постави [број 1 в] на (изабери случајне (2) до (12))
постави [број 2 в] на (изабери случајне (2) до (12) )
питај (придружи се (број 1) (придружи се [к] (број 2))) и чекај
ако <(одговор) = ((број 1) * (број 2))> затим
    реци [да! :)] за (2) секунди
друго
    кажу [нопе :(] за (2) секунди
крај
```

\--- /задатак \---

\--- задатак \---

Кликните на зелену заставу, а затим кликните на ново дугме „Репродукуј“ да бисте тестирали да ли ради. Требало би да видите да игра не почиње пре него што кликнете на дугме.

\--- /задатак \---

Видите ли да се тајмер покреће када се кликне на зелену заставу, а не на почетак игре?

![Тимер је почео](images/brain-timer-bug.png)

\--- задатак \---

Можете ли промијенити код за тајмер тако да тајмер започне када играч кликне на гумб?

\--- /задатак \---

\--- задатак \--- Додајте код у свој тастер за дугме тако да се тастер поново приказује на крају сваке игре.

![Буттон сприте](images/button-sprite.png)

```blocks3
    када добијем [крај в]
    схов
```

\--- /задатак \---

\--- задатак \---

Тестирајте 'Плаи' дугме играјући неколико игара. Дугме треба да се прикаже на крају сваке игре.

Да бисте брже тестирали игру, можете промијенити вриједност од `тиме`{: цласс = "блоцк3вариаблес"} тако да свака игра траје само неколико секунди.

![Фаза](images/stage-sprite.png)

```blocks3
    подесите [тиме в] на [10]
```

\--- /задатак \---

\--- таск \--- Можете да промените како изгледа дугме када показивач миша лебди над њим.

![Буттон](images/button-sprite.png)

```blocks3
    када је заставица кликнула
    показала
    заувек
    ако <touching (mouse-pointer v)?> затим
        сет [фисхеие в] ефект на (30)
    друго
        сет [фисхеие в] ефекат на (0)
    крај
    крај
```

![сцреенсхот](images/brain-fisheye.png) \--- /задатак \---