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

+ Zatim možete dodati kôd animacije u svoju novu animacijsku funkciju, a zatim dvaput upotrijebiti funkciju:
    
    ![screenshot](images/brain-use-function.png)

+ Sada, ako želite pokazati kvačicu i križ duže ili kraće vrijeme, samo trebate napraviti jednu promjenu u kodu. Probaj!

+ Umjesto da samo prikazujete i skrivate kvačicu i križ, možete promijeniti svoju animacijsku funkciju, tako da grafika nestaje.
    
    ```blocks
        define [animate]
        set [ghost v] effect to (100)
        show
        repeat (25)
            change [ghost v] effect by (-4)
        end
        hide
    ```