## Δημιουργία ερωτήσεων

Θα ξεκινήσεις δημιουργώντας τυχαίες ερωτήσεις για να απαντήσει ο παίκτης.

--- task ---

Δημιούργησε ένα νέο έργο Scratch.

**Online:** άνοιξε ένα νέο έργο Scratch στη διεύθυνση [rpf.io/scratch-new](https//rpf.io/scratch-new){:target="_blank"}.

**Offline:** άνοιξε ένα νέο έργο στον επεξεργαστή εκτός σύνδεσης.

Αν χρειαστεί να κατεβάσεις και να εγκαταστήσεις τον offline editor για το Scratch, μπορείς να το βρεις στο [rpf.io/scratchoff](https//rpf.io/scratchoff){:target="_blank"}.

--- /task ---

--- task ---

Επίλεξε έναν χαρακτήρα και ένα σκηνικό για το παιχνίδι σου. Μπορείς να επιλέξεις ότι σου αρέσει! Ακολουθεί ένα παράδειγμα:

![στιγμιότυπο οθόνης](images/brain-setting.png)

--- /task ---

--- task ---

Βεβαιώσου ότι έχεις επιλέξει τον χαρακτήρα σου. Δημιούργησε δύο νέες μεταβλητές, που ονομάζονται `αριθμός 1`{:class="block3variables"} και `αριθμός 2`{:class="block3variables"}, για να αποθηκεύσεις τους αριθμούς για τις ερωτήσεις του κουίζ.

![στιγμιότυπο οθόνης](images/giga-sprite.png)

![στιγμιότυπο οθόνης](images/brain-variables.png)

[[[generic-scratch3-add-variable]]]

--- /task ---

--- task ---

Πρόσθεσε κώδικα στον χαρακτήρα σου, ώστε να ορίσεις και για τις δύο αυτές `μεταβλητές`{:class="block3variables"} μία `τυχαία`{:class="block3operators"} τιμή μεταξύ 2 και 12.

![στιγμιότυπο οθόνης](images/giga-sprite.png)

```blocks3
Όταν στην πράσινη σημαία γίνει κλικ
όρισε [αριθμός 1 v] σε (επίλεξε τυχαίο (2) εώς (12))
όρισε [αριθμός 2 v] σε (επίλεξε τυχαίο (2) εώς (12))
```

--- /task ---

--- task ---

Πρόσθεσε τον κώδικα για να `ζητήσεις`{:class="block3sensing"} από τον παίκτη την απάντηση και στη συνέχεια για να `πεις για 2 δευτερόλεπτα`{:class="block3looks"} αν η απάντηση ήταν σωστή ή λάθος:

![στιγμιότυπο οθόνης](images/giga-sprite.png)

```blocks3
when flag clicked
set [αριθμός 1 v] to (pick random (2) to (12))
set [αριθμός 2 v] to (pick random (2) to (12))
+ ask (join (αριθμός 1)(join [ x ] (αριθμός 2))) and wait
+ if <(answer) = ((αριθμός 1)*(αριθμός 2))> then
+ say [ναι! :)] for (2) seconds
+ else
+ say [όχι :(] for (2) seconds
+ end
```

--- /task ---

--- task ---

Δοκίμασε το έργο δύο φορές: απάντησε μία ερώτηση σωστά και μία λάθος.

--- /task ---

--- task ---

Πρόσθεσε έναν βρόχο `για πάντα`{:class="block3control"} που να περιβάλλει αυτόν τον κώδικα, ώστε το παιχνίδι να κάνει πολλές ερωτήσεις στον παίκτη.

--- hints ---


--- hint ---

Πρέπει να προσθέσεις ένα block `για πάντα`{:class="block3control"} και να τοποθετήσεις όλο τον κώδικα εκτός από το block `όταν πατήσεις τη σημαία`{:class="block3control"} σε αυτό.

--- /hint ---

--- hint ---

Εδώ είναι το μπλοκ που χρειάζεσαι:

```blocks3
forever
end
```

--- /hint ---

--- hint ---

Έτσι πρέπει να φαίνεται ο νέος σου κώδικας:

```blocks3
when flag clicked
+ forever
	set [αριθμός 1 v] to (pick random (2) to (12))
	set [αριθμός 2 v] to (pick random (2) to (12))
	ask (join (αριθμός 1)(join [ x ] (αριθμός 2))) and wait
	if <(answer) = ((αριθμός 1)*(αριθμός 2))> then
		say [ναι! :)] for (2) seconds
	else
		say [όχι :(] for (2) seconds
	end
end
```

--- /hint ---

--- /hints ---

--- /task ---
