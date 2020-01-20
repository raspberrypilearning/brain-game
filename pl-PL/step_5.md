## Wielokrotne gry

Teraz dodasz przycisk „Graj”, aby gracz mógł grać w twoją grę wiele razy.

\--- task \---

Create a new 'Play' button sprite that the player needs to click to start a new game.

You can draw the sprite yourself, or edit a sprite from the library.

![Picture of the play button](images/brain-play.png)

\--- /task \---

\--- task \---

Add this code to your button sprite:

![Button sprite](images/button-sprite.png)

```blocks3
    kiedy kliknięto zieloną flagę
    pokaż

kiedy ten duszek kliknięty
    ukryj
    nadaj komunikat (start v)
```

\--- /task \---

The new code includes another `broadcast`{:class="block3events"} block, which sends the message 'start'.

The new code makes the 'Play' button sprite show when when player clicks on the flag. When the player clicks on the button sprite, the sprite hides and then broadcasts a message that other sprites can react to.

At the moment, the character sprite starts asking questions when the player clicks the flag. Change your game's code so that character sprite starts asking questions when it receives the 'start' `broadcast`{:class="block3events"}.

\--- task \---

Select your character sprite and, in its code section, replace the `when flag clicked`{:class="block3events"} block with a `when I receive start`{:class="block3events"} block.

![Character sprite](images/giga-sprite.png)

```blocks3
<br />- kiedy kliknięto zieloną flagę
+ kiedy otrzymam [start v]
ustaw [liczba 1 v] na (losuj liczbę od (2) do (12))
ustaw [liczba 2 v] na (losuj liczbę od (2) do (12))
zapytaj (połącz (liczba 1)(połącz [ x ] i (liczba 2))) i czekaj
jeżeli <(odpowiedź) = ((liczba 1) * (liczba 2))> to
    powiedz [tak!] przez 2 sekund 
w przeciwnym razie
    powiedz [niestety :(] przez (2) sekund
koniec
```

\--- /task \---

\--- task \---

Click the green flag, and then click on the new 'Play' button to test whether it works. You should see that the game doesn't start before you click on the button.

\--- /task \---

Can you see that the timer starts when the green flag is clicked, instead of when the game starts?

![Timer has started](images/brain-timer-bug.png)

\--- task \---

Can you change the code for the timer so that the timer starts when the player clicks on the button?

\--- /task \---

\--- task \---

Add code to your button sprite so that the button shows again at the end of each game.

![Button sprite](images/button-sprite.png)

```blocks3
    kiedy otrzymam [koniec v]
    pokaż
```

\--- /task \---

\--- task \---

Test the 'Play' button by playing a couple of games. The button should show at the end of each game.

To test the game more quickly, you can change the value of `time`{:class="block3variables"} so that each game is only a few seconds long.

![Stage](images/stage-sprite.png)

```blocks3
    ustaw [czas v] na [10]
```

\--- /task \---

\--- task \---

You can change how the button looks when the mouse pointer hovers over it.

![Button](images/button-sprite.png)

```blocks3
    kiedy kliknięto zieloną flagę
    pokaż
    zawsze 
    jeżeli <dotyka (wskaźnik myszy)> to 
         ustaw efekt [rybie oko v] na (30)
    w przeciwnym razie
          ustaw efekt [rybie oko v] na (0)
    end
end
```

![screenshot](images/brain-fisheye.png)

\--- /task \---