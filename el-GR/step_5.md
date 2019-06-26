## Πολλαπλά παιχνίδια

Τώρα θα προσθέσεις ένα κουμπί "Έναρξη", έτσι ώστε ο παίκτης να μπορεί να παίξει το παιχνίδι σου πολλές φορές.

\--- task \--- Δημιούργησε ένα καινούργιο κουμπί "Έναρξη" το οποίο πρέπει να κάνει κλικ ο παίκτης για να ξεκινήσει ένα νέο παιχνίδι.

Μπορείς να το σχεδιάσεις ο ίδιος ή να τροποποιήσεις κάποιο χαρακτήρα από τη βιβλιοθήκη του Scratch.

![Picture of the play button](images/brain-play.png)

\--- /task \---

\--- task \--- Πρόσθεσε αυτόν τον κώδικα στο αντικείμενο κουμπιού:

![Button sprite](images/button-sprite.png)

```blocks3
    when flag clicked
    show

    when this sprite clicked
    hide
    broadcast (start v)
```

\--- /task \---

Ο νέος κώδικας περιλαμβάνει μία διαφορετική `εκπομπή`{:class="block3events"}, η οποίο στέλνει το μήνυμα 'έναρξη'.

Ο νέος κώδικας κάνει το κουμπί 'Έναρξη' να εμφανίζεται όταν ο παίκτης κάνει κλικ στη σημαία. Όταν ο παίκτης κάνει κλικ στο κουμπί, το κουμπί εξαφανίζεται και μετά μεταδίδει ένα μήνυμα ώστε να αντιδράσουν και οι άλλοι χαρακτήρες.

Προς το παρόν, ο χαρακτήρας αρχίζει να θέτει ερωτήσεις όταν ο παίκτης κάνει κλικ στη σημαία. Άλλαξε τον κώδικα του παιχνιδιού σου έτσι ώστε ο χαρακτήρας να ξεκινά να κάνει ερωτήσεις όταν λάβει την `εκπομπή`{:class="block3events"} 'Έναρξη'.

\--- task \--- Select your character sprite and, in its code section, replace the `when flag clicked`{:class="block3events"} block with a `when I receive start`{:class="block3events"} block.

![Character sprite](images/giga-sprite.png)

```blocks3
<br />- when flag clicked
+ when I receive [start v]
set [number 1 v] to (pick random (2) to (12))
set [number 2 v] to (pick random (2) to (12))
ask (join (number 1)(join [ x ] (number 2))) and wait
if &lt;(answer) = ((number 1)*(number 2))&gt; then
    say [yes! :)] for (2) seconds
else
    say [nope :(] for (2) seconds
end
```

\--- /task \---

\--- task --

Click the green flag, and then click on the new 'Play' button to test whether it works. You should see that the game doesn't start before you click on the button.

\--- /task \---

Can you see that the timer starts when the green flag is clicked, instead of when the game starts?

![Timer has started](images/brain-timer-bug.png)

\--- task --

Can you change the code for the timer so that the timer starts when the player clicks on the button?

\--- /task \---

\--- task \--- Add code to your button sprite so that the button shows again at the end of each game.

![Button sprite](images/button-sprite.png)

```blocks3
    when I receive [end v]
    show
```

\--- /task \---

\--- task --

Test the 'Play' button by playing a couple of games. The button should show at the end of each game.

To test the game more quickly, you can change the value of `time`{:class="block3variables"} so that each game is only a few seconds long.

![Φάση](images/stage-sprite.png)

```blocks3
    set [time v] to [10]
```

\--- /task \---

\--- task \--- You can change how the button looks when the mouse pointer hovers over it.

![Button](images/button-sprite.png)

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

![screenshot](images/brain-fisheye.png) \--- /task \---