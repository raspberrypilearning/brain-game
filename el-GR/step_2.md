## Δημιουργία ερωτήσεων

Θα ξεκινήσεις δημιουργώντας τυχαίες ερωτήσεις για να απαντήσει ο παίκτης.

\--- task \---

Δημιούργησε ένα νέο έργο Scratch.

**Online:** άνοιξε ένα νέο έργο Scratch στη διεύθυνση [rpf.io/scratch-new](http://rpf.io/scratch-new){:target="_blank"}.

**Offline: ** άνοιξε ένα νέο έργο στον επεξεργαστή εκτός σύνδεσης.

Αν χρειαστεί να κατεβάσεις και να εγκαταστήσεις τον offline editor για το Scratch, μπορείς να το βρεις στο [rpf.io/scratchoff](http://rpf.io/scratchoff){:target="_blank"}.

\--- /task \---

\--- task \---

Add a character sprite and a backdrop for your game. You can choose any you like! Here's an example:

![screenshot](images/brain-setting.png)

\--- /task \---

\--- task \---

Make sure you have your character sprite selected. Create two new variables, called `number 1`{:class="block3variables"} and `number 2`{:class="block3variables"}, to store the numbers for the quiz questions.

![screenshot](images/giga-sprite.png)

![screenshot](images/brain-variables.png)

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- task \---

Add code to your character sprite to set both of the `variables`{:class="block3variables"} to a `random`{:class="block3operators"} number between 2 and 12.

![screenshot](images/giga-sprite.png)

```blocks3
Όταν στην πράσινη σημαία γίνει κλικ
όρισε [αριθμός 1 v] σε (επίλεξε τυχαίο (2) εώς (12))
όρισε [αριθμός 2 v] σε (επίλεξε τυχαίο (2) εώς (12))
```

\--- /task \---

\--- task \---

Add code to `ask`{:class="block3sensing"} the player for the answer, and then `say for 2 seconds`{:class="block3looks"} whether the answer was right or wrong:

![screenshot](images/giga-sprite.png)

```blocks3
Όταν στην πράσινη σημαία γίνει κλικ
όρισε [αριθμός 1 v] σε (επίλεξε τυχαίο (2) εώς (12))
όρισε [αριθμός 2 v] σε (επίλεξε τυχαίο (2) εώς (12))

+ ρώτησε (ένωσε (αριθμός 1) (ένωσε [ x ] (αριθμός 2))) και περίμενε
+ εάν <(απάντηση) = ((αριθμός 1) * (αριθμός 2))> τότε 
+  πες [ναι!]
end :\)\] για (2) δευτερόλεπτα
+ αλλιώς
+ πες [όχι :(] για (2) δευτερόλεπτα
+ end
```

\--- /task \---

\--- task \---

Test your project twice: answer one question correctly, and the other incorrectly.

\--- /task \---

\--- task \---

Add a `forever`{:class="block3control"} loop around this code, so that the game asks the player lots of questions in a row.

\--- hints \---

\--- hint \---

You need to add a `forever`{:class="block3control"} block, and put all of the code except the `when flag clicked`{:class="block3control"} block into it.

\--- /hint \---

\--- hint \---

Here is the block you need:

```blocks3
forever
end
```

\--- /hint \---

\--- hint \---

Here is what your code should look like:

```blocks3
Όταν στην πράσινη σημαία γίνει κλικ

+ για πάντα 
  όρισε [αριθμός 1 v] σε (επίλεξε τυχαίο (2) εώς (12))
  όρισε [αριθμός 2 v] σε (επίλεξε τυχαίο (2) εώς (12))
  ρώτησε (ένωσε (αριθμός 1) (ένωσε [ x ] (αριθμός 2))) και περίμενε
  εάν <(απάντηση) = ((αριθμός 1) * (αριθμός 2))> τότε 
    πες [ναι!]
  end
end :\)\] για (2) δευτερόλεπτα
αλλιώς
πες [όχι :(] για (2) δευτερόλεπτα
end
end
```

\--- /hint \---

\--- /hints \---

\--- /task \---