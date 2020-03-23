## 그래픽 추가

현재 문자 스프라이트는 단순히 `맞습니다! :) ` 혹은 `틀립니다! :( ` 만 말합니다. 여기에 그래픽을 추가하여 정답이 맞는지 틀린지 시각적으로 표현하세요.

\--- task \---

'체크'와 'x표'를 모두 포함하는 '결과'라는 새로운 스프라이트를 만듭니다.

![점과 교차 모습으로 된 스프라이트](images/brain-result.png)

\--- /task \---

\--- task \---

캐릭터 스프라이트의 코드를 변경하여, '맞음' 과 '틀림' 신호를 `방송하기`{:class="block3events"}할 수 있도록 하세요.

![캐릭터 스프라이트](images/giga-sprite.png)

```blocks3
만약 <(답) = ((1번) × (2번))> \(이\) 라면 
 [맞습니다! :)] 을 (2) 초 동안 말하기
 + (맞음 v) 신호 보내기
아니면 
 [틀립니다 :(] 을 (2) 초 동안 말하기
 + (틀림 v) 신호보내기
end
```

\--- /task \---

\--- task \---

이제 `보이기`{:class="block3looks"} 메시지를 사용하여 '체크' 또는 'x표' 의상을 표시할 수 있습니다. 결과 스프라이트에 다음 코드를 추가하세요.

![결과 스프라이트](images/result-sprite.png)

```blocks3
    [맞음] 신호를 받았을 때
모양을 (체크) 로 바꾸기
보이기
(1) 초 기다리기
숨기기

[틀림] 신호를 받았을 때
모양을 (x표) 로 바꾸기
보이기
(1) 초 기다리기
숨기기

⚑ 클릭했을 때
숨기기
```

\--- /task \---

\--- task \---

Test your game again. You should see the tick whenever you answer a question correctly, and the cross whenever you answer incorrectly!

![Tick for correct, cross for wrong answer](images/brain-test-answer.png)

\--- /task \---

`내가 정답일 때`{:class="blockevents"} 와 `내가 오답일 때`{:class="blockevents"}의 코드는 거의 동일합니까?

So you can change your code more easily, you are going to create a custom block.

\--- task \---

Select the 'Result' sprite. 그런 다음 `내 블록`{: class = "block3myblocks"}을 클릭 한 다음 **블록 추가하기**를 누릅니다. 새 블록을 만들고 `애니메이션`{: class = "block3myblocks"} 이라고 합니다.

![Result sprite](images/result-sprite.png)

![Create a block called animate](images/brain-animate-function.png)

\--- /task \---

\--- task \---

Move the code to `show`{:class="block3looks"} and `hide`{:class="block3looks"} the 'Result' sprite into the `animate`{:class="block3myblocks"} block:

![Result sprite](images/result-sprite.png)

```blocks3
애니메이션 정의하기
보이기
(1) 초 기다리기
숨기기
```

\--- /task \---

\--- task \---

Make sure you have removed the `show`{:class="block3looks"} and `hide`{:class="block3looks"} blocks below **both** of the `switch costume`{:class="block3looks"} blocks.

그런 다음 `모양을 바꾸기`{: class = "block3looks"} 블록 아래에 `애니메이션`{: class = "block3myblocks"} 블록을 추가하십시오. 이제 코드는 다음과 같이 보입니다.

![Result sprite](images/result-sprite.png)

```blocks3
    [맞음] 신호를 받았을 때
모양을 (체크) 로 바꾸기
애니메이션:: 모습

[틀림] 신호를 받았을 때
모양을 (x표) 로 바꾸기
애니메이션:: 모습
```

\--- /task \---

사용자 정의 `애니메이션`{: class = "block3myblocks"} 블록으로 인해 '결과' 스프라이트의 의상을 더 길거나 더 짧은 시간으로 표시하려면 코드를 한 번만 변경하면 됩니다.

\--- task \---

Change your code so that the 'tick' or 'cross' costumes display for 2 seconds.

\--- /task \---

\--- task \---

Instead of `showing`{:class="block3looks"} and `hiding`{:class="block3looks"} the 'tick' or 'cross' costumes, you could change your `animate`{:class="block3myblocks"} block so that the costumes fade in.

![Result sprite](images/result-sprite.png)

```blocks3
    애니메이션 정의하기
[유령] 효과를 (100) 로 정하기
보이기
(25) 번 반복하기 
  [유령] 효과를 (-4) 만큼 바꾸기
끝
숨기기
```

\--- /task \---

'체크' 또는 'x표' 그래픽의 애니메이션을 개선 할 수 있습니까? 복장을 페이드 아웃하기위한 코드를 추가하거나 다른 멋진 효과를 사용할 수 있습니다.

![스크린샷](images/brain-effects.png)