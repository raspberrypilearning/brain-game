## 그래픽 추가하기

` 예! :) ` 또는 ` 없음 :( `이라고 당신의 캐릭터에게 단지 말하는 것 대신에 플레이어에게 그들이하는 일을 플레이어가 알 수 있게 해주는 그래픽을 추가합시다.

+ '체크'와 'x표'를 모두 포함하는 '결과'라는 새로운 스프라이트를 만듭니다.
    
    ![screenshot](images/brain-result.png)

+ 캐릭터의 코드를 변경하여 플레이어에게 어떻게 했는지 알려주는 것 대신에 `옳음` {: class = "blockevents"} 및 `틀림` {: class = "blockevents"} 메시지를 보내주십시오.
    
    ![screenshot](images/brain-broadcast-answer.png)

+ 이제 메시지를 사용하여 '체크'또는 'x표'를 표시 할 수 있습니다. 이 코드를 새 '결과'스프라이트에 추가하십시오.
    
    ![screenshot](images/brain-show-answer.png)

+ 게임을 다시 테스트 해보십시오. 정확한 질문을 할 때마다 체크가 보일 것이며, 잘못 될 때마다 x표가 보일 것입니다.
    
    ![screenshot](images/brain-test-answer.png)

+ Have you noticed that the code for `when I receive correct`{:class="blockevents"} and `when I receive wrong`{:class="blockevents"} is nearly identical? Let's create a function to make it easier for you to make changes to your code.
    
    On your 'Result' sprite, click `More Blocks`{:class="blockmoreblocks"}, and then 'Make a Block'. Create a new function called `animate`{:class="blockmoreblocks"}.
    
    ![screenshot](images/brain-animate-function.png)

+ You can then add the animation code into your new animation function, and then just use the function twice:
    
    ![screenshot](images/brain-use-function.png)

+ Now, if you want to show the tick and the cross for a longer or shorter time, you only need to make one change to your code. Try it!

+ Instead of just showing and hiding the tick and the cross, you could change your animation function, so that the graphics fade in.
    
    ```blocks
        define [animate]
        set [ghost v] effect to (100)
        show
        repeat (25)
            change [ghost v] effect by (-4)
        end
        hide
    ```