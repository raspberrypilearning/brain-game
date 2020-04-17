## 타이머 추가

--- task ---

`시간`{:class="block3variables"}이라는 새 변수를 사용하여 스테이지에 카운트 다운 타이머를 만듭니다. 타이머는 30 초에서 시작하여 0초까지 카운트다운 됩니다.

![무대 스프라이트](images/stage-sprite.png)

--- hints ---


--- hint ---

`변수`{:class="block3variables"}}를 만들고, '시간'이라고 이름을 설정합니다. 그리고 초기값을 `30` 으로 설정합니다.

그런 다음 30 초 내에 `시간`{class="block3variables"}}을 0까지 카운트다운하는 코드를 제작하세요. 이렇게 하려면 매 `1` 초마다 `시간`{:class="block3variables"}을 `1` 감소하는 코드를 추가하고 무한반복합니다. 이 과정은 `시간`{:class="block3variables"} 변수가 `0`과 같을 때까지 진행합니다.

--- /hint ---

--- hint ---

필요한 코드 블록은 다음과 같습니다.

```blocks3
<> 까지 반복하기

끝

(1) 초 기다리기

[시간] 을 (1) 만큼 바꾸기

(시간)

⚑ 클릭했을 때

<() = ()>

[시간] 을 [0] 로 정하기
```

--- /hint ---

--- hint ---

코드는 다음과 같이 설계되어야 합니다:

```blocks3
⚑ 클릭했을 때
[시간] 을 [30] 로 정하기
<(time) = (0)> 까지 반복하기 
  (1) 초 기다리기
  [시간] 을 (-1) 만큼 바꾸기
끝
```

--- /hint ---

--- /hints ---

--- /task ---

--- task ---

'end'라는 메시지를 보내는 `방송하기`{:class="block3control"} 블록을 만듭니다. `방송하기`{:class="block3control"}은 스피커를 통한 방송과 같으며 모든 스프라이트에서 들을 수 있습니다. `시간`{:class="block3variables"}이 `0` 이 경과하면 게임이 종료되도록 타이머 코드 끝에 `방송`{:class="block3control"} 블록을 추가하십시오

![무대 스프라이트](images/stage-sprite.png)

```blocks3
    방송하기 (끝)
```

--- /task ---

--- task ---

캐릭터 스프라이트를 선택하고 스프라이트가 `끝`{:class="block3control"} 메시지를 받았을 때</code>{{class = "block3control"} `다른 스프라이트를 중지</0>하도록 코드를 추가하십시오.</p>

<p><img src="images/giga-sprite.png" alt="기가 스프라이트" /></p>

<pre><code class="blocks3">    [끝] 신호를 받았을 때
멈추기 [스프라이트 안의 다른 스크립트]
`</pre> 

--- /task ---

--- task ---

다시 게임을 테스트 하세요. 타이머가 0으로 카운트 다운 될 떄까지 질문해야 합니다,

--- /task ---