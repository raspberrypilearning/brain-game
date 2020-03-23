## 여러가지 게임

이제 플레이어가 게임을 여러 번 할 수 있도록 '재생' 버튼을 추가 할 것입니다.

\--- task \---

Create a new 'Play' button sprite that the player needs to click to start a new game.

You can draw the sprite yourself, or edit a sprite from the library.

![Picture of the play button](images/brain-play.png)

\--- /task \---

\--- task \---

Add this code to your button sprite:

![Button sprite](images/button-sprite.png)

```blocks3
    ⚑ 클릭했을 때
보이기

이 스프라이트를 클릭했을 때
숨기기
(시작) 신호 보내기
```

\--- /task \---

새로운 코드에는 또 다른 `방송하기`{: class = "block3events"} 블록이 포함되어 있습니다. 이 블록은 '시작' 메시지를 보냅니다.

새로운 코드는 플레이어가 깃발을 클릭 할 때 '시작' 버튼 스프라이트를 보여줍니다. 플레이어가 버튼 스프라이트를 클릭하면 스프라이트가 숨겨지고 다른 스프라이트가 반응 할 수 있는 메시지를 방송합니다.

현재 캐릭터 스프라이트는 플레이어가 깃발을 클릭 할 때 질문을 하기 시작합니다. 그 캐릭터의 스프라이트가 `방송하기`{: 클래스 = "block3events"} 에 의한 '시작' 메시지를 수신할 때 질문을 시작 있도록 게임의 코드를 변경합니다.

\--- task \---

Select your character sprite and, in its code section, replace the `when flag clicked`{:class="block3events"} block with a `when I receive start`{:class="block3events"} block.

![Character sprite](images/giga-sprite.png)

```blocks3
<br />+ [start v] 신호를 받았을 때
[number 1 v] 을\(를\) ((2) 부터 (12) 사이의 난수) 로 정하기
[number 2 v] 을\(를\) ((2) 부터 (12) 사이의 난수) 로 정하기
((number 1) 와\(과\) ([ x ] 와\(과\) (number 2) 결합하기) 결합하기) 라고 묻고 기다리기
만약 <(대답) = ((number 1) × (number 2))> \(이\)라면 
말하기 [맞습니다! :)] for (2) seconds
else
    say [nope :(] for (2) seconds
end
```

\--- /task \---

\--- task \---

녹색 깃발를 클릭 한 다음 새로운 '재생'버튼을 클릭하여 작동 여부를 테스트하십시오. 버튼을 클릭하기 전에 게임이 시작되지 않는 것을 확인해야 합니다.

\--- /task \---

게임이 시작될 때가 아니라 녹색 깃발이 클릭되었을 때 타이머가 시작된다는 것을 확인했습니까?

![Timer has started](images/brain-timer-bug.png)

\--- task \---

Can you change the code for the timer so that the timer starts when the player clicks on the button?

\--- /task \---

\--- task \---

Add code to your button sprite so that the button shows again at the end of each game.

![Button sprite](images/button-sprite.png)

```blocks3
    [끝] 신호를 받았을 때
보이기
```

\--- /task \---

\--- task \---

Test the 'Play' button by playing a couple of games. The button should show at the end of each game.

⚑ 클릭했을 때 보이기 무한 반복하기 만약 ` \(이\)라면 
    [fisheye] 효과를 (30) 로 정하기
  아니면 
    [fisheye] 효과를 (0) 로 정하기
  end
end</p>

<p><img src="images/stage-sprite.png" alt="Stage" /></p>

<pre><code class="blocks3">    [시간] 을 [10] 으로 설정
`</pre> 

\--- /task \---

\--- task \---

You can change how the button looks when the mouse pointer hovers over it.

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

\--- /task \---