## Dodavanje grafike

Umjesto da tvoj lik igraču samo govori `točno! :)` ili `netočno:(`, možeš dodati grafiku koja će igraču pokazivati kako mu ide.

+ Dodaj novog lika i nazovi ga 'Rezultat'. Liku dodaj dva prikladna kostima - jedan za točan (kvačica), a jedan za netočan (križić) rezultat.
    
    ![screenshot](images/brain-result.png)

+ Promijeni kôd lika tako da, umjesto da samo govori igraču kako napreduje, šalje poruke `točno`{:class="blockevents"} i `netočno`{:class="blockevents"}.
    
    ![screenshot](images/brain-broadcast-answer.png)

+ Sada možeš upotrijebiti ove poruke za prikazivanje 'kvačica' ili 'križić' kostima. Dodaj sljedeći kôd svom novom liku:
    
    ![screenshot](images/brain-show-answer.png)

+ Ponovno isprobaj igru. Trebaš vidjeti kvačicu svaki put kad je odgovor točan, a križić svaki put kad je pogrešan!
    
    ![screenshot](images/brain-test-answer.png)

+ Primjećuješ li da su kôdovi za `kada primim točno`{:class="blockevents"} i `kada primim netočno`{:class="blockevents"} gotovo identični? Napravimo funkciju koja će olakšati izmjene u kôdu.
    
    Odaberi lik 'Rezultat' i grupu naredbi `Više blokova`{:class="blockmoreblocks"}. Zatim klikni na gumb 'Napravi blok' i napravi novu funkciju koju ćeš nazvati `animiraj`{:class="blockmoreblocks"}.
    
    ![screenshot](images/brain-animate-function.png)

+ Dodaj sljedeće naredbe u svoju novu funkciju, a zatim ju dva puta upotrijebi:
    
    ![screenshot](images/brain-use-function.png)

+ Želiš li da se kvačica i križić prikazuju dulje ili kraće vrijeme, trebaš napraviti samo jednu promjenu u kôdu. Pokušaj!

+ Umjesto da se kvačica i križić samo prikazuju i nestaju, možeš promijeniti funkciju animacije tako da se grafika polako pojavljuje i nestaje.
    
    ```blocks
        definiraj [animate]
    postavi efekt [duh v] na (100)
    prikaži
    ponovi (25)
    promijeni efekt [duh v] za (-4)
    end
    sakrij
    ```