## Više igara

Dodajmo u tvoju igru dugme 'igraj', tako da možeš da je igraš više puta.

+ Izradi novi lik (sprite) dugmeta 'Igraj' na koje će tvoj igrač kliknuti da započne novu igru. Možeš sam/sama da ga nacrtaš ili da preurediš lik iz Scratch biblioteke (library).
    
    ![screenshot](images/brain-play.png)

+ Dodaj sljedeći kôd svom novom dugmetu.
    
    ```blocks
        when flag clicked
        show
    
        when this sprite clicked
        hide
        broadcast [igraj v]
    ```
    
    Ovaj kôd prikazuje dugme 'igraj' kada se započne projekat. Kada se klikne na dugme, ono se sakrije i, nakon toga, šalje poruku koja će započeti igru.

+ Biće potrebno da promijeniš kôd svog karaktera tako da igra počne kada karakter dobije poruku `kreni`{:class="blockevents"}, a ne kada se klikne na zastavicu.
    
    Zamijeni kôd `when flag clicked`{:class="blockevents"} (kada se klikne na zastavicu) sa `when I receive start`{:class="blockevents"} (kada primim kreni).
    
    ![screenshot](images/brain-start.png)

+ Klikni na zelenu zastavicu, a zatim na novo dugme 'Igraj' da ga isprobaš. Trebalo bi da vidiš da igra ne počinje sve dok se ne pritisne dugme.

+ Da li primjećuješ da brojač vremena počinje da odbrojava kada se klikne na zelenu zastavicu, a ne kada igra počne?
    
    ![screenshot](images/brain-timer-bug.png)
    
    Možeš li to da popraviš?

+ Klikni na pozornicu (stage) i zamijeni blok `stop all`{:class="blockcontrol"} (zaustavi sve) porukom `kraj`{:class="blockevents"}.
    
    ![screenshot](images/brain-end.png)

+ Sada možeš da dodaš kôd svom dugmetu kako bi se ono ponovo pojavilo na kraju svake igre.
    
    ```blocks
        when I receive [kraj v]
        show
    ```

+ Takođe će biti potrebno da zaustaviš svog karaktera da postavlja pitanja na kraju svake igre:
    
    ```blocks
        when I receive [kraj v]
        stop [other scripts in sprite v]
    ```

+ Isprobaj dugme 'Igraj' tako što ćeš odigrati nekoliko igara. Trebalo bi da vidiš da se dugme 'Igraj' pojavljuje nakon svake igre. Da olakšaš isprobavanje, svaku igru možeš da skratiš, tako da traje samo nekoliko sekundi.
    
    ```blocks
        set [vrijeme v] to [10]
    ```

+ Možeš čak i da promijeniš izgled dugmeta kada mišem pređeš preko njega.
    
    ```blocks
        when flag clicked
        show
        forever
        if <touching [mouse-pointer v]?> then
            set [fisheye v] effect to (30)
        else
            set [fisheye v] effect to (0)
        end
        end
    ```
    
    ![screenshot](images/brain-fisheye.png)