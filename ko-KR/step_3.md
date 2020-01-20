## 타이머 추가

\--- task \---

Create a countdown timer on the Stage with the help of a new variable called `time`{:class="block3variables"}. The timer should begin at 30 seconds and count down to 0 seconds.

![Stage sprite](images/stage-sprite.png)

\--- hints \---

\--- hint \---

Create a `variable`{:class="block3variables"}, call it 'time', and set its value to `30`.

Then add code to count `time`{:class="block3variables"} down to 0 within 30 seconds. To do this, subtract `1` from `time`{:class="block3variables"} every `1` second, and repeat this until `time`{:class="block3variables"} equals `0`.

\--- /hint \---

\--- hint \---

Here are the blocks you need:

```blocks3
무한 반복 < >

끝

(1) 초 기다리기

[시간 v] 을 (1) 로 변경

(시간)

녹색 깃발이 클릭되었을 때

<() = ()>

[시간 v]를 [0]으로 설정
```

\--- /hint \---

\--- hint \---

Here is the what your new code should look like:

```blocks3
녹색 깃발을 클릭했을 때
[시간 v]를 [30] 으로 설정
 <(시간) = (0)>
    (1) 초 기다리기
    [시간 v]를 (-1) 만큼 바꾸기
끝
```

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

Create a `broadcast`{:class="block3control"} that sends the message 'end'. A `broadcast`{:class="block3control"} is like an announcement over a loudspeaker: it can be heard by all of your sprites. Add the `broadcast`{:class="block3control"} block to the end of the timer code so that the code will send and 'end' message when the `time`{:class="block3variables"} has counted down to `0`.

![Stage sprite](images/stage-sprite.png)

```blocks3
    방송하기 (끝 v)
```

\--- /task \---

\--- task \---

Select your character sprite and add some code so that the sprite `stops the other scripts`{:class="block3control"} when it receives the `end`{:class="block3control"} message.

![Giga sprite](images/giga-sprite.png)

```blocks3
    [end v] 신호를 받았을 때
    멈추기 [other scripts in sprite v]
```

\--- /task \---

\--- task \---

Test your game again. It should continue to ask questions until the timer has counted down to 0.

\--- /task \---