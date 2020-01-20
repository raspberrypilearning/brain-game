## Πρόσθεσε γραφικά

Αυτή τη στιγμή ο χαρακτήρας sprite λέει ` ναι! :) ` ή ` όχι :( ` στις απαντήσεις του παίκτη. Πρόσθεσε μερικά γραφικά για να ενημερώσεις τον παίκτη, εάν η απάντησή του είναι σωστή ή λάθος.

\--- task \---

Δημιούργησε ένα νέο αντικείμενο που ονομάζεται 'Αποτέλεσμα', το οποίο περιλαμβάνει τις ενδυμασίες 'tick' (τικ) και 'cross' (x).

![Αντικείμενο με τις ενδυμασίες τικ και χι](images/brain-result.png)

\--- /task \---

\--- task \---

Άλλαξε τον κώδικα του χαρακτήρα σου έτσι ώστε, αντί να λέει κάτι στον παίκτη, να `μεταδίδει`{:class="block3events"} τα μηνύματα "σωστό" ή "λάθος".

![Χαρακτήρας](images/giga-sprite.png)

```blocks3
εάν <(απάντηση) = ((νούμερο 1) * (νούμερο 2))> τότε 
-  πες [ναι! :)] για (2) δευτερόλεπτα
+  μετάδωσε (σωστό v)
αλλιώς 
 - πες [όχι :(] για (2) δευτερόλεπτα
  + μετάδωσε (λάθος v)
end
```

\--- /task \---

\--- task \---

Τώρα μπορείς να χρησιμοποιήσεις αυτά τα μηνύματα για να `εμφανίσεις`{:class="block3looks"} την ενδυμασία "tick" ή "cross". Πρόσθεσε τον παρακάτω κώδικα στο αντικείμενο "Αποτέλεσμα":

![Αντικείμενο Αποτέλεσμα](images/result-sprite.png)

```blocks3
    όταν λάβω [σωστό v]
άλλαξε ενδυμασία σε (tick v)
εμφανίσου
περίμενε (1) δευτερόλεπτα
εξαφανίσου

όταν λάβω [λάθος v]
άλλαξε ενδυμασία σε (cross v)
εμφανίσου
περίμενε (1) δευτερόλεπτα
εξαφανίσου

Όταν στην (πράσινη) σημαία γίνει κλικ,
εξαφανίσου
```

\--- /task \---

\--- task \---

Test your game again. You should see the tick whenever you answer a question correctly, and the cross whenever you answer incorrectly!

![Tick for correct, cross for wrong answer](images/brain-test-answer.png)

\--- /task \---

Can you see that the code for `when I receive correct`{:class="block3events"} and `when I receive wrong`{:class="block3events"} is nearly identical?

So you can change your code more easily, you are going to create a custom block.

\--- task \---

Select the 'Result' sprite. Then click on `My Blocks`{:class="block3myblocks"}, and then on **Make a Block**. Create a new block and call it `animate`{:class="block3myblocks"}.

![Result sprite](images/result-sprite.png)

![Create a block called animate](images/brain-animate-function.png)

\--- /task \---

\--- task \---

Move the code to `show`{:class="block3looks"} and `hide`{:class="block3looks"} the 'Result' sprite into the `animate`{:class="block3myblocks"} block:

![Result sprite](images/result-sprite.png)

```blocks3
ορισμός κίνηση
εμφανίσου
περίμενε (1) δευτερόλεπτα
εξαφανίσου
```

\--- /task \---

\--- task \---

Make sure you have removed the `show`{:class="block3looks"} and `hide`{:class="block3looks"} blocks below **both** of the `switch costume`{:class="block3looks"} blocks.

Then add the `animate`{:class="block3myblocks"} block below both of the `switch costume`{:class="block3looks"} blocks. Your code should now look like this:

![Result sprite](images/result-sprite.png)

```blocks3
    όταν λάβω [σωστό v]
άλλαξε ενδυμασία σε (tick v)
κίνηση:: custom

όταν λάβω [λάθος v]
άλλαξε ενδυμασία σε (cross v)
κίνηση:: custom
```

\--- /task \---

Because of the custom `animate`{:class="block3myblocks"} block, you now only need to make one change to your code if you want to show the 'Result' sprite's costumes a longer or shorter time.

\--- task \---

Change your code so that the 'tick' or 'cross' costumes display for 2 seconds.

\--- /task \---

\--- task \---

Instead of `showing`{:class="block3looks"} and `hiding`{:class="block3looks"} the 'tick' or 'cross' costumes, you could change your `animate`{:class="block3myblocks"} block so that the costumes fade in.

![Result sprite](images/result-sprite.png)

```blocks3
    ορισμός κίνηση
όρισε εφέ [ghost v] σε (100)
εμφανίσου
επανάλαβε (25) 
  άλλαξε εφέ [ghost v] κατά (-4)
end
εξαφανίσου
```

\--- /task \---

Can you improve the animation of the 'tick' or 'cross' graphics? You could add code to make the costumes fade out as well, or you could use other cool effects:

![screenshot](images/brain-effects.png)