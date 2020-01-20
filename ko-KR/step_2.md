## 질문 만들기

플레이어가 대답할 수 있도록 임의의 질문을 만들어 보겠습니다.

\--- task \---

새 Scratch 프로젝트를 엽니다.

**온라인:** [rpf.io/scratch-new](http://rpf.io/scratch-new){:target="_ blank"}에서 새로운 온라인 스크래치 프로젝트 열기

**오프라인 :** 오프라인 편집기에서 새 프로젝트를 엽니다.

Scratch 오프라인 편집기를 다운로드하여 설치해야하는 경우 [rpf.io/scratchoff](http://rpf.io/scratchoff){: target = "_ blank"}에서 찾을 수 있습니다.

\--- /task \---

\--- task \---

Add a character sprite and a backdrop for your game. You can choose any you like! Here's an example:

![screenshot](images/brain-setting.png)

\--- /task \---

\--- task \---

Make sure you have your character sprite selected. Create two new variables, called `number 1`{:class="block3variables"} and `number 2`{:class="block3variables"}, to store the numbers for the quiz questions.

![screenshot](images/giga-sprite.png)

![screenshot](images/brain-variables.png)

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- task \---

Add code to your character sprite to set both of the `variables`{:class="block3variables"} to a `random`{:class="block3operators"} number between 2 and 12.

![screenshot](images/giga-sprite.png)

```blocks3
녹색 깃발을 클릭했을 때
[1번 v] 을 ((2)부터 (12) 까지의 난수)로 설정
[2번 v] 을 ((2)부터 (12) 까지의 난수)로 설정
```

\--- /task \---

\--- task \---

Add code to `ask`{:class="block3sensing"} the player for the answer, and then `say for 2 seconds`{:class="block3looks"} whether the answer was right or wrong:

![screenshot](images/giga-sprite.png)

```blocks3
녹색 깃발을 클릭했을 때
[1번 v] 을 ((2)부터 (12) 까지의 난수)로 설정
[2번 v] 을 ((2)부터 (12) 까지의 난수)로 설정

 + ((number 1) 와 ([x] 와 (number 2) 결합하기) 결합하기)) 묻고 기다리기
 + 만약 <(answer) = ((1번)*(2번))> 이라면
 + 말하기 [맞습니다! :)] (2) 초 동안
+ 아니면
+ (2) 초 동안 [틀렸습니다!])
+ 끝
```

\--- /task \---

\--- task \---

Test your project twice: answer one question correctly, and the other incorrectly.

\--- /task \---

\--- task \---

Add a `forever`{:class="block3control"} loop around this code, so that the game asks the player lots of questions in a row.

\--- hints \---

\--- hint \---

You need to add a `forever`{:class="block3control"} block, and put all of the code except the `when flag clicked`{:class="block3control"} block into it.

\--- /hint \---

\--- hint \---

Here is the block you need:

```blocks3
영원히
끝
```

\--- /hint \---

\--- hint \---

Here is what your code should look like:

```blocks3
녹색 깃발을 클릭했을 때

+ 무한 반복
    [1번 v] 을 ((2) 부터 (12) 까지의 난수) 로 설정
    [2번 v] 을 ((2) 부터 (12) 까지의 난수) 로 설정
    ((number 1)과 (join [ x ] (number 2) 결합하기) 결합하기) 묻고 기다리기
    만약 <(answer) = ((1번)*(2번))> 이라면
       말하기 [맞습니다! :)] (2) 초 동안
    아니면
        (2) 초 동안 [틀렸습니다 :(]) 말하기
    끝
끝
```

\--- /hint \---

\--- /hints \---

\--- /task \---