## 그래픽 추가

현재 문자 스프라이트는 단순히 `맞습니다! :) ` 혹은 `틀립니다! :( ` 만 말합니다. 여기에 그래픽을 추가하여 정답이 맞는지 틀린지 시각적으로 표현하세요.

\--- task \---

'체크'와 'x표'를 모두 포함하는 '결과'라는 새로운 스프라이트를 만듭니다.

![틱과 크로스 의상으로 된 스프라이트](images/brain-result.png)

\--- /task \---

\--- task \---

캐릭터 스프라이트의 코드를 변경하여, '맞음' 과 '틀림' 신호를 `방송하기`{:class="block3events"}할 수 있도록 하세요.

![문자 스프라이트](images/giga-sprite.png)

```blocks3
만약 <(답) = ((1번) × (2번))> \(이\)라면 
  [맞습니다! :)] 을\(를\) (2) 초 동안 말하기
  + (맞음 v) 신호 보내기
아니면 
  [틀립니다 :(] 을\(를\) (2) 초 동안 말하기
  + (틀림 v) 신호 보내기
end
```

\--- /task \---

\--- task \---

이제 `show`{:class="block3looks"} 메시지를 사용하여 '체크' 또는 'x표' 의상을 표시할 수 있습니다. 결과 스프라이트에 다음 코드를 추가하세요.

![결과 스프라이트](images/result-sprite.png)

```blocks3
    [맞음 v] 신호를 받았을 때
모양을 (체크 v) \(으\)로 바꾸기
보이기
(1) 초 기다리기
숨기기

[틀림 v] 신호를 받았을 때
모양을 (x표 v) \(으\)로 바꾸기
보이기
(1) 초 기다리기
숨기기

⚑ 클릭했을 때
숨기기
```

\--- /task \---

게임을 다시 테스트 해보십시오. 정확한 질문을 할 때마다 체크가 보일 것이며, 잘못 될 때마다 x표가 보일 것입니다.

![올바른 답변을 위해 십자 표시하십시오.](images/brain-test-answer.png)

\--- /task \---

`내가 옳음을 받았을 때`{:class="blockevents"} 와 `내가 틀림을 받았을 때`{:class="blockevents"}의 코드는 거의 동일합니까?

따라서 코드를 더 쉽게 변경하고 사용자 정의 블록을 생성 할 수 있습니다.

\--- task \---

'Result'스프라이트를 선택하십시오. 그런 다음 `내 블록`{: class = "block3myblocks"}을 클릭 한 다음 **블록 추가하기**를 누릅니다. 새 블록을 만들고 `애니메이션`{: class = "block3myblocks"} 이라고 합니다.

![결과 스프라이트](images/result-sprite.png)

![animate라는 블록 만들기](images/brain-animate-function.png)

\--- /task \---

\--- task \--- 결과 스프라이트 내 `보이기`{:class="block3looks"} 및 `숨기기`{:class="block3looks"} 코드를 `애니메이션`{:class="block3myblocks"} 블록으로 옮기세요:

![결과 스프라이트](images/result-sprite.png)

```blocks3
애니메이션 정의하기
보이기
(1) 초 기다리기
숨기기
```

\--- /task \---

\--- task \--- 결과 스프라이트 내 `보이기`{:class="block3looks"} 및 `숨기기`{:class="block3looks"} 코드를 `애니메이션`{:class="block3myblocks"} 블록으로 옮기세요.

그런 다음 `스위치 코스튬`{: class = "block3looks"} 블록 아래에 `애니메이션`{: class = "block3myblocks"} 블록을 추가하십시오. 이제 코드는 다음과 같이 보입니다.

![결과 스프라이트](images/result-sprite.png)

```blocks3
    [correct v] 신호를 받았을 때
모양을 (체크 v) \(으\)로 바꾸기
animate :: custom

[wrong v] 신호를 받았을 때
모양을 (x표 v) \(으\)로 바꾸기
animate :: custom
```

\--- /task \---

사용자 정의 `애니메이션`{: class = "block3myblocks"} 블록으로 인해 '결과' 스프라이트의 의상을 더 길거나 더 짧은 시간으로 표시하려면 코드를 한 번만 변경하면됩니다.

\--- task \---

'tick'또는 'cross'복장이 2 초 동안 표시되도록 코드를 변경하십시오.

\--- /task \---

\--- 작업 \--- ` 보이기 ` {: class = "block3looks"} 및 ` 숨기기 ` {: class = "block3looks"} 를 사용하여 맞고 틀림의 의상을 표현하는 대신, `애니메이션`{:class="block3myblocks"} 을 사용하여 의상이 페이드인되도록 할 수 있습니다.

![결과 스프라이트](images/result-sprite.png)

```blocks3
    정의하기 animate
[ghost v] 효과를 (100) 로 정하기
보이기
(25) 번 반복하기 
  [ghost v] 효과를 (-4) 만큼 바꾸기
end
숨기기
```

\--- /task \---

'체크' 또는 'x표' 그래픽의 애니메이션을 개선 할 수 있습니까? 복장을 페이드 아웃하기위한 코드를 추가하거나 다른 멋진 효과를 사용할 수 있습니다.

![스크린샷](images/brain-effects.png)