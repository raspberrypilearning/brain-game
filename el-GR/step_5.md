## Πολλαπλά παιχνίδια

Τώρα θα προσθέσεις ένα κουμπί "Έναρξη", έτσι ώστε ο παίκτης να μπορεί να παίξει το παιχνίδι σου πολλές φορές.

\--- task \---

Create a new 'Play' button sprite that the player needs to click to start a new game.

You can draw the sprite yourself, or edit a sprite from the library.

![Picture of the play button](images/brain-play.png)

\--- /task \---

\--- task \---

Add this code to your button sprite:

![Button sprite](images/button-sprite.png)

```blocks3
    όταν στην πράσινη σημαία γίνει κλικ,
εμφανίσου

όταν γίνει κλικ σε αυτό το αντικείμενο
εξαφανίσου
μετάδωσε (έναρξη v)
```

\--- /task \---

The new code includes another `broadcast`{:class="block3events"} block, which sends the message 'start'.

The new code makes the 'Play' button sprite show when when player clicks on the flag. When the player clicks on the button sprite, the sprite hides and then broadcasts a message that other sprites can react to.

At the moment, the character sprite starts asking questions when the player clicks the flag. Change your game's code so that character sprite starts asking questions when it receives the 'start' `broadcast`{:class="block3events"}.

\--- task \---

Select your character sprite and, in its code section, replace the `when flag clicked`{:class="block3events"} block with a `when I receive start`{:class="block3events"} block.

![Character sprite](images/giga-sprite.png)

```blocks3
<br />Όταν στην πράσινη σημαία γίνει κλικ

+ όταν λάβω [έναρξη v]
όρισε [αριθμός 1 v] σε (επίλεξε τυχαίο (2) εώς (12))
όρισε [αριθμός 2 v] σε (επίλεξε τυχαίο (2) εώς (12))
ρώτησε (ένωσε (αριθμός 1) (ένωσε [ x ] (αριθμός 2))) και περίμενε
εάν <(απάντηση) = ((αριθμός 1) * (αριθμός 2))> τότε 
  πες [ναι!]
end :\)\] για (2) δευτερόλεπτα
αλλιώς
πες [όχι :(] για (2) δευτερόλεπτα
end
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
    when I receive [end v]
    show
```

\--- /task \---

\--- task \---

Test the 'Play' button by playing a couple of games. The button should show at the end of each game.

To test the game more quickly, you can change the value of `time`{:class="block3variables"} so that each game is only a few seconds long.

![Stage](images/stage-sprite.png)

```blocks3
    όρισε [χρόνος v] σε [10]
```

\--- /task \---

\--- task \---

You can change how the button looks when the mouse pointer hovers over it.

![Button](images/button-sprite.png)

```blocks3
    Όταν στην πράσινη σημαία γίνει κλικ
εμφανίσου
για πάντα 
  εάν <touching (mouse-pointer v)?> τότε 
    όρισε εφέ [fisheye v] σε (30)
  αλλιώς 
    όρισε εφέ [fisheye v] σε (0)
  end
end
```

![screenshot](images/brain-fisheye.png)

\--- /task \---