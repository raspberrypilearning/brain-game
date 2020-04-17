## 그래픽 추가

현재 문자 스프라이트는 단순히 `맞습니다! :) ` 혹은 `틀립니다! :( ` 만 말합니다. 여기에 그래픽을 추가하여 정답이 맞는지 틀린지 시각적으로 표현하세요.

--- task ---

'체크'와 'x표'를 모두 포함하는 '결과'라는 새로운 스프라이트를 만듭니다.

![점과 교차 모습으로 된 스프라이트](images/brain-result.png)

--- /task ---

--- task ---

캐릭터 스프라이트의 코드를 변경하여, '맞음' 과 '틀림' 신호를 `방송하기`{:class="block3events"}할 수 있도록 하세요.

![캐릭터 스프라이트](images/giga-sprite.png)

```blocks3
if <(answer) = ((1번)*(2번))> then
- say [맞습니다! :)] for (2) seconds
+ broadcast (맞음 v)
else
- say [틀립니다 :(] for (2) seconds
+ broadcast (틀림 v)
end
```

--- /task ---

--- task ---

이제 `보이기`{:class="block3looks"} 메시지를 사용하여 '체크' 또는 'x표' 의상을 표시할 수 있습니다. 결과 스프라이트에 다음 코드를 추가하세요.

![결과 스프라이트](images/result-sprite.png)

```blocks3
when I receive [맞음 v]
    switch costume to (체크 v)
    show
    wait (1) seconds
    hide

    when I receive [틀림 v]
    switch costume to (x표 v)
    show
    wait (1) seconds
    hide

    when flag clicked
    hide
```

--- /task ---

--- task ---

게임을 다시 테스트 해보세요. 정확한 질문을 할 때마다 체크가 보일 것이며, 잘못 될 때마다 x표가 보일 것입니다.

![체크는 맞음, x표는 틀린 답변](images/brain-test-answer.png)

--- /task ---

`내가 정답일 때`{:class="block3events"} 와 `내가 오답일 때`{:class="block3events"}의 코드는 거의 동일합니까?

따라서 코드를 더 쉽게 변경할 수 있으므로 사용자 지정 블록을 만들게됩니다.

--- task ---

'결과' 스프라이트를 선택하십시오. 그런 다음 `내 블록`{:class="block3myblocks"}을 클릭 한 다음 **블록 추가하기**를 누릅니다. 새 블록을 만들고 `애니메이션`{:class="block3myblocks"} 이라고 합니다.

![결과 스프라이트](images/result-sprite.png)

![애니메이션 이름의 블록을 만듭니다](images/brain-animate-function.png)

--- /task ---

--- task ---

'결과' 스프라이트 내 `보이기`{:class="block3looks"} 및 `숨기기`{:class="block3looks"} 코드를 `애니메이션`{:class="block3myblocks"} 블록으로 옮기세요:

![결과 스프라이트](images/result-sprite.png)

```blocks3
define 애니메이션
show
wait (1) seconds
hide
```

--- /task ---

--- task ---

`모습을 (으)로 바꾸기`{:class="block3looks"}블록의 **사이**의 아레에 위치한`보이기`{:class="block3looks"} 그리고 `숨기기`{:class="block3looks"}을 지웠는지 확인하세요

그런 다음 `모양을 바꾸기`{:class="block3looks"} 블록 아래에 `애니메이션`{:class="block3myblocks"} 블록을 추가하십시오. 이제 코드는 다음과 같이 보입니다.

![결과 스프라이트](images/result-sprite.png)

```blocks3
    when I receive [맞음 v]
    switch costume to (체크 v)
    애니메이션:: custom

    when I receive [틀림 v]
    switch costume to (x표 v)
    애니메이션:: custom
```

--- /task ---

사용자 정의 `애니메이션`{:class="block3myblocks"} 블록으로 인해 '결과' 스프라이트의 의상을 더 길거나 더 짧은 시간으로 표시하려면 코드를 한 번만 변경하면 됩니다.

--- task ---

'체크'또는 'x표' 모습이 2 초 동안 표시되도록 코드를 변경하십시오.

--- /task ---

--- task ---

`보이기`{:class="block3looks"} 및 `숨기기`{:class="block3looks"} 를 사용하여 맞고 틀림의 모습을 표현하는 대신, `애니메이션`{:class="block3myblocks"} 을 사용하여 모습이 페이드인 되도록 할 수 있습니다.

![결과 스프라이트](images/result-sprite.png)

```blocks3
    define 애니메이션
	set [ghost v] effect to (100)
	show
	repeat (25)
		change [ghost v] effect by (-4)
	end
	hide
```

--- /task ---

'체크' 또는 'x표' 그래픽의 애니메이션을 개선 할 수 있습니까? 복장을 페이드 아웃하기위한 코드를 추가하거나 다른 멋진 효과를 사용할 수 있습니다.

![스크린샷](images/brain-effects.png)