## 질문 만들기

플레이어가 응답해야하는 무작위 질문을 만들어서 시작하겠습니다.

\--- task \---

새 Scratch 프로젝트를 엽니 다.

**Online:** open a new online Scratch project at [rpf.io/scratch-new](http://rpf.io/scratchon){:target="_blank"}.

**오프라인 :** 오프라인 편집기에서 새 프로젝트를 엽니 다.

Scratch 오프라인 편집기를 다운로드하여 설치해야하는 경우 [rpf.io/scratchoff](http://rpf.io/scratchoff){: target = "_ blank"}에서 찾을 수 있습니다.

\--- /task \---

\--- task \--- 게임에 문자 스프라이트와 배경을 추가합니다. 당신은 당신이 좋아하는 것을 선택할 수 있습니다! 다음은 그 예입니다.

![스크린샷](images/brain-setting.png)

\--- /task \---

\--- task \--- 캐릭터 스프라이트를 선택했는지 확인하십시오. 퀴즈 질문에 대한 번호를 저장하기 위해 `번 1`{: class = "block3variables"} 및 `2`{{class = "block3variables"}라는 두 개의 새로운 변수를 만듭니다.

![스크린샷](images/giga-sprite.png) ![스크린샷](images/brain-variables.png)

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- 작업 \--- 캐릭터 스프라이트에 추가 코드는 모두 설정 `변수`A를 : {클래스 = "block3variables을"} `무작위로`2와 12 사이의 숫자 : {클래스 = "block3operators"}.

![스크린샷](images/giga-sprite.png)

```blocks3

클릭하면 [number 1 v]를 (임의의 (2) ~ (12) 선택)
[number 2 v] ((임의의 (2) ~ (12) 선택)
```

\--- /task \---

\--- task \--- `코드를 추가하여 답을 플레이어에게`{: class = "block3sensing"} 묻고, 2 초 동안 `말하십시오.`{: class = "block3looks"} 답이 맞는지 잘못된:

![스크린샷](images/giga-sprite.png)

```blocks3
플래그가 클릭하면
세트 [수 1 V] 내지 (임의의 (2) ~ (12) 선택)
세트를 [수 2 V]로 (선택 랜덤 (2) 내지 (12))

+는 (요청 (번호 1 가입) (
+ <(대답) = ((1) * (2))> 다음
+ 말하기 [예! :)] (2) 초 동안
+ else
+ (2) 초 동안 [no :(])
+ end
```

\--- /task \---

\--- task \---

프로젝트를 두 번 테스트하십시오 : 한 질문에 올바르게 대답하고 다른 질문에 올바르지 않게 답하십시오.

\--- /task \---

\--- task \---

추가 `영원히`게임을 연속으로 질문의 플레이어를 많이 요구 있도록이 코드 주위에 루프 : {클래스 = "block3control을"}.

\--- hints \--- \--- hint \---

당신은 추가 할 필요가 `영원히`를 제외하고 모든 코드를 블록 넣어 : {클래스 = "block3control을"} `플래그를 클릭하면`{: 클래스 = "block3control는"} 그것으로 차단합니다.

\--- / 힌트 \--- \--- 힌트 \--- 다음은 필요한 블록입니다.

```blocks3
영원히 끝

```

\--- / hint \--- \--- 힌트 \--- 다음은 코드의 모양입니다.

```blocks3


+ 영원히
    클릭했을 때 [1 번 v]를 (2 번에서 12 번 선택)
    설정 [2 번에서 2 번까지] (
    번) 1) (조인 [X] (번호 2))) 기다리
    경우 <(답) = ((수 1) * (번호 2))> 다음
        말 [예! :)] (2) 초 동안
    else
        (2) 초 동안 [no :(])
    end
end
```

\--- /hint \--- \--- /hints \---

\--- /task \---