## 질문 만들기

플레이어가 대답할 수 있도록 임의의 질문을 만들어 보겠습니다.

--- task ---

새로운 스크래치 프로젝트를 엽니다.

**온라인:** [rpf.io/scratch-new](https//rpf.io/scratch-new){:target="_blank"}에서 새로운 온라인 스크래치 프로젝트 열기

**오프라인:** 오프라인 편집기에서 새 프로젝트를 엽니다.

스크래치 오프라인 편집기를 다운로드하여 설치해야 하는 경우 [rpf.io/scratchoff](https//rpf.io/scratchoff){:target="_blank"}에서 찾을 수 있습니다.

--- /task ---

--- task ---

캐릭터 스프라이트 그리고 배경을 너의 게임에 추가하세요. 당신이 좋아하는 것을 선택할 수있슨디다.! 다음은 그 예시 입니다:

![스크린샷](images/brain-setting.png)

--- /task ---

--- task ---

캐릭터 스프라이트가 선택되어 있는지 확인하십시오 퀴즈 질문 번호를 저장하기 위해 `1번`{:class="block3variables"}과 `2번`{:class="block3variables"}이라는 두 개의 새로운 변수를 만듭니다.

![스크린샷](images/giga-sprite.png)

![스크린샷](images/brain-variables.png)

[[[generic-scratch3-add-variable]]]

--- /task ---

--- task ---

캐릭터 스프라이트에 `변수`{:class="block3variables"} 를 추가하고, 변수값을 2부터 12까지의 `무작위`{:class="block3operators"} 로 설정합니다.

![스크린샷](images/giga-sprite.png)

```blocks3
when flag clicked
set [1번 v] to (pick random (2) to (12))
set [2번 v] to (pick random (2) to (12))
```

--- /task ---

--- task ---

`묻기`{:class="block3sensing"} 코드를 추가하여 플레이어에게 답을 요구하세요. 플레이어가 답을 입력하면 `2초 후 말하기`{:class="block3looks"} 블록을 활용하여 2초 기다린 후 답이 맞았는지, 틀렸는지를 입력되게 하세요.

![스크린샷](images/giga-sprite.png)

```blocks3
when flag clicked
set [1번 v] to (pick random (2) to (12))
set [2번 v] to (pick random (2) to (12))
+ ask (join (1번)(join [ x ] (2번))) and wait
+ if <(answer) = ((1번)*(2번))> then
+ say [맞습니다! :)] for (2) seconds
+ else
+ say [틀렸습니다 :(] for (2) seconds
+ end
```

--- /task ---

--- task ---

프로젝트를 두 번 테스트하십시오: 한 질문에 올바르게 대답하고 다른 질문에 올바르지 않게 답하십시오.

--- /task ---

--- task ---

`무한 반복하기`{:class="block3control"}를 추가하십시오. 이 코드를 반복하면 플레이어에게 많은 질문을 할 수 있습니다.

--- hints ---


--- hint ---

`무한 반복하기`{:class="block3control"} 블록 내에 `녹색 깃발을 클릭했을 때`{:class="block3control"} 블록을 제외하고 모든 블록을 넣으세요.

--- /hint ---

--- hint ---

필요한 코드 블록은 다음과 같습니다:

```blocks3
forever
end
```

--- /hint ---

--- hint ---

코드는 다음과 같이 설계되어야 합니다:

```blocks3
when flag clicked
+ forever
	set [1번 v] to (pick random (2) to (12))
	set [2번 v] to (pick random (2) to (12))
	ask (join (1번)(join [ x ] (2번))) and wait
	if <(answer) = ((1번)*(2번))> then
		say [맞습니다! :)] for (2) seconds
	else
		say [틀렸습니다 :(] for (2) seconds
	end
end
```

--- /hint ---

--- /hints ---

--- /task ---
