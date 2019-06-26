## Πρόσθεσε γραφικά

Αυτή τη στιγμή ο χαρακτήρας sprite λέει ` ναι! :) ` ή ` όχι :( ` στις απαντήσεις του παίκτη. Πρόσθεσε μερικά γραφικά για να ενημερώσεις τον παίκτη εάν η απάντησή του είναι σωστή ή λανθασμένη.

\--- task \---

Δημιούργησε ένα νέο αντικείμενο που ονομάζεται 'Αποτέλεσμα', το οποίο περιλαμβάνει τις ενδυμασίες 'tick' (τικ) και 'cross' (χι).

![Αντικείμενο με τις ενδυμασίες τικ και χι](images/brain-result.png)

\--- /task \---

\--- task \---

Άλλαξε τον κώδικα του χαρακτήρα σου έτσι ώστε, αντί να λέει κάτι στον παίκτη, να `μεταδίδει`{:class="block3events"} τα μηνύματα "σωστό" ή "λάθος".

![Χαρακτήρας](images/giga-sprite.png)

```blocks3
if <(answer) = ((number 1)*(number 2))> then

- say [yes! :)] for (2) seconds
+ broadcast (correct v)
else
- say [nope :(] for (2) seconds
+ broadcast (wrong v)
end
```

\--- /task \---

\--- task \---

Τώρα μπορείς να χρησιμοποιήσεις αυτά τα μηνύματα για να `εμφανίσεις`{:class="block3looks"} την ενδυμασία "tick" ή "cross". Πρόσθεσε τον παρακάτω κώδικα στο αντικείμενο "Αποτέλεσμα":

![Αντικείμενο Αποτέλεσμα](images/result-sprite.png)

```blocks3
    when I receive [correct v]
    switch costume to (tick v)
    show
    wait (1) seconds
    hide

    when I receive [wrong v]
    switch costume to (cross v)
    show
    wait (1) seconds
    hide

    when flag clicked
    hide
```

\--- /task \---

\--- task \--- Δοκίμασε ξανά το παιχνίδι σου. Θα δεις ένα τικ κάθε φορά που θα έχεις μια σωστή απάντηση και ένα χι κάθε φορά που θα έχεις μια λάθος!

![Τικ για τη σωστή και χι για τη λανθασμένη απάντηση ](images/brain-test-answer.png)

\--- /task \---

Βλεπεις ότι ο κώδικας για το `when I receive correct`{:class="block3events"} και `when I receive wrong`{:class="block3events"} είναι σχεδόν πανομοιότυπος;

Για να μπορείς να αλλάξεις τον κώδικά σου πιο εύκολα, θα δημιουργήσεις ένα προσαρμοσμένο μπλοκ.

\--- task \---

Επίλεξε το αντικείμενο "Αποτέλεσμα". Στη συνέχεια, κάνε κλικ στο `Τα μπλοκ μου`{:class="block3myblocks"}, και στη συνέχεια στο **Δημιουργία μπλοκ** . Δημιούργησε ένα νέο μπλοκ και ονόμασέ το `κίνηση`{:class="block3myblocks"}.

![Αντικείμενο Αποτέλεσμα](images/result-sprite.png)

![Δημιούργησε ένα μπλοκ που ονομάζεται κίνηση](images/brain-animate-function.png)

\--- /task \---

\--- task \--- Μετακίνησε τον κώδικα για την `εμφάνιση`{:class="block3looks"} και την `απόκρυψη`{:class="block3looks"} του αντικειμένου 'Αποτέλεσμα' στο μπλοκ `κίνηση`{:class="block3myblocks"}:

![Αντικείμενο Αποτέλεσμα](images/result-sprite.png)

```blocks3
define animate
show
wait (1) seconds
hide
```

\--- /task \---

\--- task \--- Βεβαιώσου ότι έχεις αφαιρέσει τον κώδικα για την `εμφάνιση`{:class="block3looks"} και την `απόκρυψη`{:class="block3looks"} κάτω **και από τα δύο** μπλοκ των `ενδυμασιών`{:class="block3looks"}.

Στη συνέχεια, πρόσθεσε το μπλοκ `κίνηση`{:class="block3myblocks"} κάτω από τα δύο μπλοκ των `ενδυμασιών`{:class="block3looks"}. Ο κώδικας θα πρέπει τώρα να φαίνεται ως εξής:

![Αντικείμενο Αποτέλεσμα](images/result-sprite.png)

```blocks3
    when I receive [correct v]
    switch costume to (tick v)
    animate:: custom

    when I receive [wrong v]
    switch costume to (cross v)
    animate:: custom
```

\--- /task \---

Λόγω του προσαρμοσμένου μπλοκ `κίνηση`{:class="block3myblocks"}, πρέπει να κάνεις μόνο μία αλλαγή στον κώδικά σου, εάν θέλεις να εμφανίσεις τις ενδυμασίες του αντικειμένου 'Αποτέλεσμα' για μεγαλύτερο ή μικρότερο χρονικό διάστημα.

\--- task \---

Άλλαξε τον κώδικά σου έτσι ώστε οι ενδυμασίες 'tick' ή 'cross' να εμφανίζονται για 2 δευτερόλεπτα.

\--- /task \---

\--- task \--- Αντί να `εμφανίζεις`{:class="block3looks"} και να `εξαφανίζεις`{:class="block3looks"} τις ενδυμασίες "tick" ή "cross", μπορείς να αλλάξεις το μπλοκ `κίνηση`{:class="block3myblocks"}, έτσι ώστε οι ενδυμασίες να εμφανίζονται σταδιακά.

![Αντικείμενο Αποτέλεσμα](images/result-sprite.png)

```blocks3
    define animate
    set [ghost v] effect to (100)
    show
    repeat (25)
        change [ghost v] effect by (-4)
    end
    hide
```

\--- /task \---

Μπορείς να βελτιώσεις την κίνηση των γραφικών 'tick' ή 'cross'; Θα μπορούσες να προσθέσεις κώδικα για να κάνεις τις ενδυμασίες να ξεθωριάζουν, ή θα μπορούσες να χρησιμοποιήσεις άλλα φοβερά εφέ:

![screenshot](images/brain-effects.png)