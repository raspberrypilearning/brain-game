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
    when flag clicked
    show

    when this sprite clicked
    hide
    broadcast (start v)
```

\--- /task \---

새로운 코드에는 또 다른 `방송하기`{: class = "block3events"} 블록이 포함되어 있습니다. 이 블록은 '시작' 메시지를 보냅니다.

새로운 코드는 플레이어가 깃발을 클릭 할 때 '시작' 버튼 스프라이트를 보여줍니다. 플레이어가 버튼 스프라이트를 클릭하면 스프라이트가 숨겨지고 다른 스프라이트가 반응 할 수 있는 메시지를 방송합니다.

현재 캐릭터 스프라이트는 플레이어가 깃발을 클릭 할 때 질문을 하기 시작합니다. 그 캐릭터의 스프라이트가 `방송하기`{: 클래스 = "block3events"} 에 의한 '시작' 메시지를 수신할 때 질문을 시작 있도록 게임의 코드를 변경합니다.

\--- task \---

Select your character sprite and, in its code section, replace the `when flag clicked`{:class="block3events"} block with a `when I receive start`{:class="block3events"} block.

![Character sprite](images/giga-sprite.png)

```blocks3
<br />- when flag clicked
+ when I receive [start v]
set [number 1 v] to (pick random (2) to (12))
set [number 2 v] to (pick random (2) to (12))
ask (join (number 1)(join [ x ] (number 2))) and wait
if <(answer) = ((number 1)*(number 2))> then
    say [yes! :)] for (2) seconds
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
    when I receive [end v]
    show
```

\--- /task \---

\--- task \---

Test the 'Play' button by playing a couple of games. The button should show at the end of each game.

게임을 더 빠르게 테스트하려면 각 게임이 불과 몇 초 길이가되도록 `시간`{: = block3variables} 의 변수 값을 변경할 수 있습니다.

![Stage](images/stage-sprite.png)

```blocks3
    set [time v] to [10]
```

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