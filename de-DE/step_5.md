## Mehrfach spielen

Jetzt wirst du eine Taste "Spielen" hinzufügen, damit der Spieler dein Spiel mehrmals spielen kann.

\--- task \---

Create a new 'Play' button sprite that the player needs to click to start a new game.

You can draw the sprite yourself, or edit a sprite from the library.

![Picture of the play button](images/brain-play.png)

\--- /task \---

\--- task \---

Add this code to your button sprite:

![Button sprite](images/button-sprite.png)

```blocks3
    Wenn die grüne Flagge angeklickt wird
    zeige dich

    Wenn diese Figur angeklickt wird
    verstekce dich
    sende (Start v) an alle
```

\--- /task \---

The new code includes another `broadcast`{:class="block3events"} block, which sends the message 'start'.

The new code makes the 'Play' button sprite show when when player clicks on the flag. When the player clicks on the button sprite, the sprite hides and then broadcasts a message that other sprites can react to.

At the moment, the character sprite starts asking questions when the player clicks the flag. Change your game's code so that character sprite starts asking questions when it receives the 'start' `broadcast`{:class="block3events"}.

\--- task \---

Select your character sprite and, in its code section, replace the `when flag clicked`{:class="block3events"} block with a `when I receive start`{:class="block3events"} block.

![Character sprite](images/giga-sprite.png)

```blocks3
<br />- wenn die grüne Flagge angeklickt wird
+ Wenn ich [Start v] empfange
setze [Zahl 1 v] auf (Zufallszahlen von (2) bis (12))
setze [Zahl 2 v] auf (Zufallszahlen von (2) bis (12))
frage (verbinde (Zahl 1) und (verbinde [ x ] und (Zahl 2))) und warte
wenn <(Antwort) = ((Zahl 1)*(Zahl 2))> dann
    sage [Genau! :)] für (2) Sekunden
sonst
    sage [nein :(] für (2) Sekunden 
ende
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
    Wenn ich [Ende v] empfange
    zeige dich
```

\--- /task \---

\--- task \---

Test the 'Play' button by playing a couple of games. The button should show at the end of each game.

To test the game more quickly, you can change the value of `time`{:class="block3variables"} so that each game is only a few seconds long.

![Stage](images/stage-sprite.png)

```blocks3
    setze [Zeit v] auf [10]
```

\--- /task \---

\--- task \---

You can change how the button looks when the mouse pointer hovers over it.

![Button](images/button-sprite.png)

```blocks3
    Wenn die grüne Flagge angeklickt wird
    zeige dich 
    wiederhole fortlaufend
    falls <touching (mouse-pointer v)?> dann
        setze Effekt [Fischauge v] auf (30)
    sonst
        setze Effekt [Fischauge v] auf (0)
    ende
    ende
```

![screenshot](images/brain-fisheye.png)

\--- /task \---