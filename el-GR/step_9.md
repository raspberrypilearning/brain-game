## Πρόκληση: αγώνας ταχύτητας μέχρι τους 10 βαθμούς

Μπορείς να αλλάξεις το παιχνίδι έτσι ώστε ο παίκτης, αντί να απαντήσει σε όσο το δυνατόν περισσότερες ερωτήσεις σε 30 δευτερόλεπτα, να απαντήσει 10 ερωτήσεις το συντομότερο δυνατόν.

Για να κάνεις αυτήν την αλλαγή, χρειάζεται μόνο να αλλάξεις τον κώδικα του χρονομέτρου. Μπορείς να δεις ποια μπλοκ πρέπει να τροποποιηθούν;

```blocks3
όταν λάβω [έναρξη v]
όρισε [χρόνος v] σε (30)
επανάλαβε ώσπου <(χρόνος) = [0]> 
  περίμενε (1) δευτερόλεπτα
  άλλαξε [χρόνος v] κατά (-1)
end
μετάδωσε (τέλος v)
```