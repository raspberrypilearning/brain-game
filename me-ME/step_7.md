## Dodavanje grafika

Umjesto da tvoj karakter igraču samo govori `da! :)` ili `ne :(`, dodajmo i nekoliko grafika koje će igraču pokazivati kako mu ide.

+ Izradi novi lik pod nazivom 'Rezultat', koji ima dva kostima - 'kvačicu' i 'krstić'.
    
    ![screenshot](images/brain-result.png)

+ Izmijeni kôd svog karaktera tako da, umjesto da govori igraču kako je odgovorio, šalje poruke `tačno`{:class="blockevents"} i `netačno`{:class="blockevents"}.
    
    ![screenshot](images/brain-broadcast-answer.png)

+ Sada možeš upotrijebiti ove poruke za prikazivanje kostima 'kvačica' ili 'krstić'. Dodaj sljedeći kôd svom novom liku 'Rezultat':
    
    ![screenshot](images/brain-show-answer.png)

+ Isprobaj ponovo svoju igru. Trebalo bi da vidiš kvačicu svaki put kada je tvoj odgovor tačan, a krstić svaki put kada je netačan!
    
    ![screenshot](images/brain-test-answer.png)

+ Da li primjećuješ da su kôdovi za `when I receive tačno`{:class="blockevents"} i `when I receive netačno`{:class="blockevents"} gotovo identični? Kreirajmo funkciju koja će ti olakšati da napraviš izmjene u svom kôdu.
    
    U liku 'Rezultat', klikni na `More Blocks`{:class="blockmoreblocks"} (Više blokova), a zatim na 'Make a Block' (Napravi blok). Kreiraj novu funkciju i nazovi je `animiraj`{:class="blockmoreblocks"}.
    
    ![screenshot](images/brain-animate-function.png)

+ Nakon toga, možeš da dodaš kôd za animaciju u svoju novu funkciju animacije, a zatim samo da je upotrijebiš dva puta:
    
    ![screenshot](images/brain-use-function.png)

+ Sada, ako želiš da prikazuješ kvačicu i krstić duže ili kraće vrijeme, potrebno je da napraviš samo jednu izmjenu u svom kôdu. Pokušaj!

+ Umjesto da se kvačica i krstić samo prikazuju i nestaju, možeš promijeniti svoju funkciju animacije tako da se grafike postepeno pojavljuju.
    
    ```blocks
        define [animate]
        set [ghost v] effect to (100)
        show
        repeat (25)
            change [ghost v] effect by (-4)
        end
        hide
    ```