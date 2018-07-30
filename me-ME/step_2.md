## Izrada pitanja

Počnimo sa izradom slučajno odabranih pitanja na koje igrač treba da odgovori.

+ Otvori novi Scratch projekat i obriši lik mačke tako da tvoj projekat bude prazan. Online Scratch editor možeš naći na <a href="http://jumpto.cc/scratch-new" target="_blank">jumpto.cc/scratch-new</a>.

+ Izaberi karaktera i pozadinu za svoju igru. Možeš da izabereš koje god želiš! Evo primjera:
    
    ![screenshot](images/brain-setting.png)

+ Kreiraj 2 nove promjenljive (variables) i nazovi ih `broj 1`{:class="blockdata"} i `broj 2`{:class="blockdata"}. U ovim promjenljivim biće sačuvana 2 broja koja će biti pomnožena.
    
    ![screenshot](images/brain-variables.png)

+ Dodaj kôd svom karakteru kako bi obje promjenljive bile postavljene na `slučajan`{:class="blockoperators"} (random) broj između 2 i 12. 
    
    ```blocks
        when flag clicked
        set [broj 1 v] to (pick random (2) to (12))
        set [broj 2 v] to (pick random (2) to (12))
    ```

+ You can then ask the player for the answer, and let them know if they were right or wrong.
    
    ```blocks
        when flag clicked
        set [number 1 v] to (pick random (2) to (12))
        set [number 2 v] to (pick random (2) to (12))
        ask (join (number 1)(join [ x ] (number 2))) and wait
        if <(answer) = ((number 1)*(number 2))> then
            say [yes! :)] for (2) secs
        else
            say [nope :(] for (2) secs
        end
    ```

+ Test your project fully, by answering one question correctly and one with the wrong answer.

+ Add a `forever`{:class="blockcontrol"} loop around this code, so that the player is asked lots of questions.

+ Create a countdown timer on the stage, using a variable called `time`{:class="blockdata"}. The 'Ghostbusters' project has instructions for making a timer (in step 5) if you need help!

+ Test your project again - you should be able to continue asking questions until the time runs out.