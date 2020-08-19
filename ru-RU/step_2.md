## Создай вопросы

Ты начнешь с создания случайных вопросов, на которые игрок должен ответить.

--- task ---

Открой новый проект Scratch.

**Онлайн:** открой новый онлайн проект Scratch [rpf.io/scratch-new](http://rpf.io/scratch-new){:target="_blank"}.

**Офлайн:** открой новый проект в автономном редакторе.

Если тебе нужно скачать и установить оффлайн редактор Scratch, ты можешь найти его по адресу [rpf.io/scratchoff](http://rpf.io/scratchoff){:target="_blank"}.

--- /task ---

--- task ---

Добавь спрайт персонажа и фон для твоей игры. Ты можешь выбрать любой понравившийся! Вот пример:

![снимок экрана](images/brain-setting.png)

--- /task ---

--- task ---

Убедись, что ты выбрал спрайт своего персонажа. Создай две новые переменные, с именами `число 1`{:class="block3variables"} и `число 2`{:class="block3variables"}, чтобы сохранить числа для вопросов викторины.

![снимок экрана](images/giga-sprite.png)

![снимок экрана](images/brain-variables.png)

[[[generic-scratch3-add-variable]]]

--- /task ---

--- task ---

Добавь код к спрайту твоего персонажа, чтобы установить обеим `переменным`{:class="block3variables"} `случайные`{:class="block3operators"} числа от 2 до 12.

![снимок экрана](images/giga-sprite.png)

```blocks3
when flag clicked
set [число 1 v] to (pick random (2) to (12))
set [число 2 v] to (pick random (2) to (12))
```

--- /task ---

--- task ---

Добавь код, чтобы `спросить`{:class="block3sensing"} игрока, а затем `говори в течение 2 секунд`{:class="block3looks"}, был ли ответ правильным или неправильным:

![снимок экрана](images/giga-sprite.png)

```blocks3
when flag clicked
set [число 1 v] to (pick random (2) to (12))
set [число 2 v] to (pick random (2) to (12))
+ ask (join (число 1)(join [ x ] (число 2))) and wait
+ if <(answer) = ((число 1)*(число 2))> then
+ say [да! :)] for (2) seconds
+ else
+ say [нет :(] for (2) seconds
+ end
```

--- /task ---

--- task ---

Протестируй свой проект дважды: ответь на один вопрос правильно, а другой – неправильно.

--- /task ---

--- task ---

Добавь цикл `повторять всегда`{:class="block3control"} вокруг этого кода, чтобы игра задавала игроку много вопросов подряд.

--- hints ---


--- hint ---

Тебе нужно добавить блок `повторять всегда`{:class="block3control"} и поместить в него весь код, кроме блока `когда щёлкнут по зелёному флагу`{:class="block3control"}.

--- /hint ---

--- hint ---

Вот блок, который тебе понадобится:

```blocks3
forever
end
```

--- /hint ---

--- hint ---

Вот как должен выглядеть твой код:

```blocks3
when flag clicked
+ forever
	set [число 1 v] to (pick random (2) to (12))
	set [число 2 v] to (pick random (2) to (12))
	ask (join (число 1)(join [ x ] (число 2))) and wait
	if <(answer) = ((число 1)*(число 2))> then
		say [да! :)] for (2) seconds
	else
		say [нет :(] for (2) seconds
	end
end
```

--- /hint ---

--- /hints ---

--- /task ---