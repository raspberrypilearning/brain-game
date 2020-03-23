## 타이머 추가

\--- task \---

Create a countdown timer on the Stage with the help of a new variable called `time`{:class="block3variables"}. The timer should begin at 30 seconds and count down to 0 seconds.

![무대 스프라이트](images/stage-sprite.png)

\--- hints \---

\--- hint \---

`변수`{{class = "block3variables"}}를 만들고, '시간'이라고 이름을 설정합니다. 그리고 초기값을 `30` 으로 설정합니다.

그런 다음 30 초 내에 `시간`{{class = "block3variables"}}을 0까지 카운트다운하는 코드를 제작하세요. 이렇게 하려면 매 `1` 초마다 `시간`{:class="block3variables"}을 `1` 감소하는 코드를 추가하고 무한반복합니다. 이 과정은 `시간`{:class="block3variables"} 변수가 `0`과 같을 때까지 진행합니다.

\--- /hint \---

\--- hint \---

필요한 코드 블록은 다음과 같습니다.

```blocks3
repeat until < >

end

wait (1) seconds

change [time v] by (1)

(time)

when flag clicked

<() = ()>

set [time v] to [0]
```

\--- /hint \---

\--- hint \---

Here is the what your new code should look like:

```blocks3
when flag clicked
set [time v] to [30]
repeat until <(time) = (0)>
    wait (1) seconds
    change [time v] by (-1)
end
```

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

'end'라는 메시지를 보내는 `방송`{: class = "block3control"} 블록을 만듭니다. `방송`{: class = "block3control"}은 스피커를 통한 방송과 같으며 모든 스프라이트에서 들을 수 있습니다. `시간`{: class = "block3variables"}이 `0` 이 경과하면 게임이 종료되도록 타이머 코드 끝에 `방송`{: class = "block3control"} 블록을 추가하십시오

![무대 스프라이트](images/stage-sprite.png)

```blocks3
    broadcast (end v)
```

\--- /task \---

\--- task \---

Select your character sprite and add some code so that the sprite `stops the other scripts`{:class="block3control"} when it receives the `end`{:class="block3control"} message.

![기가 스프라이트](images/giga-sprite.png)

```blocks3
    when I receive [end v]
    stop [other scripts in sprite v]
```

\--- /task \---

\--- task \---

Test your game again. It should continue to ask questions until the timer has counted down to 0.

\--- /task \---