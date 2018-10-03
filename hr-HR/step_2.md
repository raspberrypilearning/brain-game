## Izrada pitanja

Krenimo s izradom slučajnih pitanja na koja igrač mora odgovoriti.

+ Otvori novi Scratch projekt i obriši lik mačke da dobiješ prazan projekt. Online Scratch nalazi se na adresi <a href="http://jumpto.cc/scratch-new" target="_blank">jumpto.cc/scratch-new</a>.

+ Odaberi lika i pozadinu za igru. Možeš odabrati što god želiš! Na primjer:
    
    ![screenshot](images/brain-setting.png)

+ Kreiraj dvije nove varijable koje se zovu `broj 1`{:class="blockdata"} i `broj 2`{:class="blockdata"}. U njih će se spremiti dva broja koja će se pomnožiti.
    
    ![screenshot](images/brain-variables.png)

+ Za postavljanje varijabli na na `slučajan`{:class="blockoperators"} broj između 2 i 12, dodaj svom liku sljedeće naredbe:
    
    ```blocks
        kada je zastavica kliknut
    postavi [broj 1 v] na (slučajni broj (2) do (12))
    postavi [broj 2 v] na (slučajni broj (2) do (12))
    ```

+ Zatim možeš zatražiti od igrača odgovor i obavijestiti ga je li točan ili netočan.
    
    ```blocks
        kada je zastavica kliknut
    postavi [broj 1 v] na (slučajni broj od (2) do (12))
    postavi [broj 2 v] na (slučajni broj od (2) do (12))
    pitaj (spoji (broj 1)(spoji [ x ] (broj 2))) i čekaj
    ako <(odgovor) = ((broj 1)*(broj 2))> onda
    govori [Točno! :)] (2) sekundi
    inače
    govori [Netočno :(] (2) sekundi
    end
    ```

+ Isprobaj projekt odgovarajući na jedno pitanje točno, a na drugo pogrešno.

+ Dodaj petlju `ponavljaj`{:class="blockcontrol"} oko ovog kôda. Na taj način će igraču biti postavljeno više pitanja.

+ Napravite odbrojavanje na pozornici pomoću varijable pod nazivom `time` {:class = "blockdata"}. Projekt "Ghostbusters" sadrži upute za izradu mjerača vremena (u koraku 5) ukoliko vam je potrebna pomoć!

+ Ponovno testirajte svoj projekt - trebali biste nastaviti s postavljanjem pitanja dok ne istekne vrijeme.