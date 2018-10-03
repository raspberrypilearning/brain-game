## Više igara

Želiš li igrati igru više puta, možeš dodati gumb 'Pokreni'.

+ Dodaj lik gumba iz biblioteke likova (možeš ga i nacrtati) na kojeg će igrač kliknuti kako bi pokrenuo novu igru. U kostimima dodaj na gumb tekst 'Pokreni'.
    
    ![screenshot](images/brain-play.png)

+ Gumbu dodaj sljedeće naredbe:
    
    ```blocks
        kada je zastavica kliknut
    prikaži
    
    kada je lik kliknut
    sakrij
    pošalji [kreni v]
    ```
    
    Ovaj kôd će prikazati gumb 'Pokreni' kada se projekt pokrene. Kada igrač klikne na njega, gumb nestaje i šalje se poruka koja će pokrenuti igru.

+ Promijeni kôd svog lika tako da igra započne kada on dobije poruku `kreni`{:class="blockevents"}, a ne kada je zastavica kliknuta.
    
    Zamijenite `when flag clicked` {:class="blockevents"} kod sa `when I receive start` {:class="blockevents"}.
    
    ![screenshot](images/brain-start.png)

+ Kliknite na zelenu zastavu, a zatim kliknite svoj novi igraj gumb biste je testirali. Trebali biste vidjeti da se igra ne počinje dok se ne klikne na gumb.

+ Jeste li primijetili da brojač počinje kada se klikne na zelenu zastavu, a ne kada počne igra?
    
    ![screenshot](images/brain-timer-bug.png)
    
    Možete li rješiti ovaj problem?

+ Kliknite na pozornicu i zamijenite `stop all` {:class="blockcontrol"} blok sa `end` {:class="blockevents"} poruku.
    
    ![screenshot](images/brain-end.png)

+ Sada možete dodati kôd na vaš gumb, da biste ga ponovno prikazali na kraju svake igre.
    
    ```blocks
        when I receive [end v]
        show
    ```

+ Također ćete morati zaustaviti svoj znak postavljanjem pitanja na kraju svake igre:
    
    ```blocks
        when I receive [end v]
        stop [other scripts in sprite v]
    ```

+ Testirajte vaš igraj gumb igranjem nekoliko igara. Trebali biste primijetiti da se igraj gumb prikazuje nakon svake igre. Da biste olakšali testiranje, možete skratiti svaku igru, ​​tako da traje samo nekoliko sekundi.
    
    ```blocks
        set [time v] to [10]
    ```

+ Čak možete promijeniti i način na koji gumb izgleda kada mišem prijeđete preko njega.
    
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