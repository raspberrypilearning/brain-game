## 질문 만들기

플레이어가 대답할 수 있도록 임의의 질문을 만들어 보겠습니다.

+ 새 스크래치 프로젝트를 시작하고 프로젝트가 비어 있도록 고양이 스프라이트를 삭제하십시오. 온라인 편집기를 사용하여 새 스크래치 프로젝트를 작성하려면 <a href="http://jumpto.cc/scratch-new" target="_blank">jumpto.cc/scratch-new</a>로 이동하십시오. 

+ 게임의 캐릭터와 배경을 선택하십시오. 당신이 좋아하는 것을 선택할 수 있습니다! 다음은 그 예입니다:
    
    ![screenshot](images/brain-setting.png)

+ `번호 1`{:c클래스="blockdata"} 과 `번호 2`{:c클래스="blockdata"}<0> 이라는 2 개의 새로운 변수를 만듭니다. 이 변수들은 함께 곱해질 2 개의 숫자를 저장합니다.
    
    ![screenshot](images/brain-variables.png)

+ 문자에 코드를 추가하여 두 변수 모두 `무작위` {: class = "blockoperators"}에 2에서 12 사이의 숫자를 설정하십시오.
    
    ```blocks
        플래그를 클릭했을 때
        [ 1 번 v]에 (2)에서 (12)을 무작위 선택하여 설정
        [2 번 v]에 (2)에서 (12)을 무작위 선택하여 설정
    ```

+ You can then ask the player for the answer, and let them know if they were right or wrong.
    
    ```blocks
        when flag clicked
        set [number 1 v] to (pick random (2) to (12))
        set [number 2 v] to (pick random (2) to (12))
        ask (join (number 1)(join [ x ] (number 2))) and wait
        if <(answer) = ((number 1)*(number 2))> then
            say [yes! :)] for (2) secs
        else
            say [nope :(] for (2) secs
        end
    ```

+ Test your project fully, by answering one question correctly and one with the wrong answer.

+ Add a `forever`{:class="blockcontrol"} loop around this code, so that the player is asked lots of questions.

+ Create a countdown timer on the stage, using a variable called `time`{:class="blockdata"}. The 'Ghostbusters' project has instructions for making a timer (in step 5) if you need help!

+ Test your project again - you should be able to continue asking questions until the time runs out.