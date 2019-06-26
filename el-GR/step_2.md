## Δημιουργία ερωτήσεων

Θα ξεκινήσεις δημιουργώντας τυχαίες ερωτήσεις για να απαντήσει ο παίκτης.

\--- task \---

Δημιούργησε ένα νέο έργο Scratch.

**Online:** άνοιξε το αρχικό έργο στο [rpf.io/scratch-new](http://rpf.io/scratchon){:target="_blank"}.

**Offline: ** άνοιξε ένα νέο έργο στον επεξεργαστή εκτός σύνδεσης.

Αν χρειαστεί να κατεβάσεις και να εγκαταστήσεις τον offline editor για το Scratch, μπορείς να το βρεις στο [rpf.io/scratchoff](http://rpf.io/scratchoff){:target="_blank"}.

\--- /task \---

\--- task \--- Επίλεξε έναν χαρακτήρα και ένα σκηνικό για το παιχνίδι σου. Μπορείς να επιλέξεις ότι σου αρέσει! Ακολουθεί ένα παράδειγμα:

![screenshot](images/brain-setting.png)

\--- /task \---

\--- task \--- Βεβαιώσου ότι έχεις επιλέξει το χαρακτήρα σου. Δημιούργησε δύο νέες μεταβλητές, που ονομάζονται `αριθμός 1`{:class="block3variables"} και `αριθμός 2`{:class="block3variables"}, για να αποθηκεύσεις τους αριθμούς για τις ερωτήσεις του κουίζ.

![screenshot](images/giga-sprite.png) ![screenshot](images/brain-variables.png)

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- task \--- Πρόσθεσε κώδικα στον χαρακτήρα σου, ώστε να ορίσεις και για τις δύο αυτές μεταβλητές μία `τυχαία`{:class="blockoperators"} τιμή μεταξύ 2 και 12.

![screenshot](images/giga-sprite.png)

```blocks3
when flag clicked
set [number 1 v] to (pick random (2) to (12))
set [number 2 v] to (pick random (2) to (12))
```

\--- /task \---

\--- task \--- Πρόσθεσε τον κώδικα για να `ζητήσεις`{:class= "block3sensing"}} από τον παίκτη την απάντηση και στη συνέχεια για να `πεις για 2 δευτερόλεπτα`{:class="block3looks"} αν η απάντηση ήταν σωστή ή λάθος:

![screenshot](images/giga-sprite.png)

```blocks3
when flag clicked
set [number 1 v] to (pick random (2) to (12))
set [number 2 v] to (pick random (2) to (12))

+ ask (join (number 1)(join [ x ] (number 2))) and wait
+ if <(answer) = ((number 1)*(number 2))> then
+ say [yes! :)] for (2) seconds
+ else
+ say [no :(] for (2) seconds
+ end
```

\--- /task \---

\--- task \---

Δοκίμασε το έργο δύο φορές: απάντησε μία ερώτηση σωστά και μία λάθος.

\--- /task \---

\--- task \---

Πρόσθεσε ένα βρόχο `για πάντα`{:class="blockcontrol"} που να περιβάλλει αυτόν τον κώδικα, ώστε το παιχνίδι να κάνει πολλές ερωτήσεις στον παίκτη.

\--- hints \--- \--- hint \---

Πρέπει να προσθέσεις ένα block `για πάντα`{block:block3control}} και να τοποθετήσεις όλο τον κώδικα εκτός από το block `όταν πατήσεις τη σημαία`{:class="block3control"} σε αυτό.

\--- /hint \--- \--- hint \--- Εδώ είναι το μπλοκ που θα χρειαστείς:

```blocks3
forever
end
```

\--- /hint \--- \--- hint \--- Έτσι πρέπει να μοιάζει με ο κώδικάς σου:

```blocks3
when flag clicked

+ forever
    set [number 1 v] to (pick random (2) to (12))
    set [number 2 v] to (pick random (2) to (12))
    ask (join (number 1)(join [ x ] (number 2))) and wait
    if <(answer) = ((number 1)*(number 2))> then
        say [yes! :)] for (2) seconds
    else
        say [no :(] for (2) seconds
    end
end
```

\--- /hint \--- \--- /hints \---

\--- /task \---