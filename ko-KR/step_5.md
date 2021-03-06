## 여러가지 게임

이제 플레이어가 게임을 여러 번 할 수 있도록 '재생' 버튼을 추가 할 것입니다.

--- task ---

플레이어가 새로운 게임을 시작하기 위해 클릭해야하는 새로운 '재생' 버튼 스프라이트를 만드세요.

스프라이트를 직접 그리거나, 라이브러리에서 스프라이트를 수정 할 수 있습니다.

![재생 버튼 그림](images/brain-play.png)

--- /task ---

--- task ---

이 코드를 당신의 버튼 스프라이트에 추가 해 보세요:

![버튼 스프라이트](images/button-sprite.png)

```blocks3
    ⚑ 클릭했을 때
    보이기

    when this sprite clicked
	  hide
	  broadcast (시작 v)
```

--- /task ---

새로운 코드에는 또 다른 `방송하기`{:class="block3events"} 블록이 포함되어 있습니다. 이 블록은 '시작' 메시지를 보냅니다.

새로운 코드는 플레이어가 깃발을 클릭 할 때 '시작' 버튼 스프라이트를 보여줍니다. 플레이어가 버튼 스프라이트를 클릭하면 스프라이트가 숨겨지고 다른 스프라이트가 반응 할 수 있는 메시지를 방송합니다.

현재 캐릭터 스프라이트는 플레이어가 깃발을 클릭 할 때 질문을 하기 시작합니다. 그 캐릭터의 스프라이트가 `방송하기`{:class="block3events"} 에 의한 '시작' 메시지를 수신할 때 질문을 시작 있도록 게임의 코드를 변경합니다.

--- task ---

캐릭터 스프라이트를 선택하고, `⚑ 클릭했을 때`{:class="block3events"} 블록을 `시작 신호를 받았을 때`{:class="block3events"} 블록으로 바꾸세요.

![캐릭터 스프라이트](images/giga-sprite.png)

```blocks3
- when flag clicked
+ when I receive [시작 v]
set [1번 v] to (pick random (2) to (12))
set [2번 v] to (pick random (2) to (12))
ask (join (1번)(join [ x ] (2번))) and wait
if <(answer) = ((1번)*(2번))> then
	say [맞습니다! :)] for (2) seconds
else
	say [아닙니다 :(] for (2) seconds
end
```

--- /task ---

--- task ---

녹색 깃발를 클릭 한 다음 새로운 '재생'버튼을 클릭하여 작동 여부를 테스트하십시오. 버튼을 클릭하기 전에 게임이 시작되지 않는 것을 확인해야 합니다.

--- /task ---

게임이 시작될 때가 아니라 녹색 깃발이 클릭되었을 때 타이머가 시작된다는 것을 확인했습니까?

![타이머 시작됨](images/brain-timer-bug.png)

--- task ---

플레이어가 버튼을 클릭 할 때 타이머가 시작되도록 타이머 코드를 변경할 수 있습니까?

--- /task ---

--- task ---

버튼 스프라이트에 코드를 추가하여 각 게임이 끝날 때 버튼이 다시 표시되도록 합니다.

![버튼 스프라이트](images/button-sprite.png)

```blocks3
    [끝 v] 신호를 받았을 때
    보이기
```

--- /task ---

--- task ---

여러 번 게임을 하여 '재생'버튼을 테스트 하십시오. 게임이 끝날 때마다 버튼이 표시됩니다.

게임을 더 빠르게 테스트하려면 각 게임이 불과 몇 초가 되도록 `시간`{:class="block3variables"} 의 변수 값을 변경할 수 있습니다.

![무대](images/stage-sprite.png)

```blocks3
set [시간 v] to [10]
```

--- /task ---

--- task ---

마우스 포인터로 버튼을 가리킬 때 버튼 모양을 변경할 수 있습니다.

![버튼](images/button-sprite.png)

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

![스크린샷](images/brain-fisheye.png)

--- /task ---