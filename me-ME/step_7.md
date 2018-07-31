## Dodavanje grafika

Umjesto da tvoj karakter igraču samo govori `da! :)` ili `ne :(`, dodajmo i nekoliko grafika koje će igraču pokazivati kako mu ide.

+ Kreiraj novi lik (sprite) pod nazivom 'Rezultat' koji će imati dva kostima (costumes) - 'kvačica' i 'krstić'.
    
    ![screenshot](images/brain-result.png)

+ Izmijeni kôd svog karaktera tako da, umjesto da samo govori igraču kako mu ide, šalje poruke `tačno`{:class="blockevents"} i `netačno`{:class="blockevents"}.
    
    ![screenshot](images/brain-broadcast-answer.png)

+ Sada možeš upotrijebiti ove poruke za prikazivanje kostima 'kvačica' ili 'krstić'. Dodaj sljedeći kôd svom novom liku 'Rezultat':
    
    ![screenshot](images/brain-show-answer.png)

+ Isprobaj ponovo svoju igru. Trebalo bi da vidiš kvačicu svaki put kada je odgovor tačan, a krstić svaki put kada je netačan!
    
    ![screenshot](images/brain-test-answer.png)

+ Da li primjećuješ da su kôdovi za `when I receive tačno`{:class="blockevents"} i `when I receive netačno`{:class="blockevents"} gotovo identični? Kreirajmo funkciju koja će ti olakšati da napraviš izmjene u svom kôdu.
    
    On your 'Result' sprite, click `More Blocks`{:class="blockmoreblocks"}, and then 'Make a Block'. Create a new function called `animate`{:class="blockmoreblocks"}.
    
    ![screenshot](images/brain-animate-function.png)

+ You can then add the animation code into your new animation function, and then just use the function twice:
    
    ![screenshot](images/brain-use-function.png)

+ Now, if you want to show the tick and the cross for a longer or shorter time, you only need to make one change to your code. Try it!

+ Instead of just showing and hiding the tick and the cross, you could change your animation function, so that the graphics fade in.
    
    ```blocks
        define [animate]
        set [ghost v] effect to (100)
        show
        repeat (25)
            change [ghost v] effect by (-4)
        end
        hide
    ```