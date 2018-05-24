## Створення запитань

Розпочнемо зі створення випадкових запитань для гравців.

+ Почніть новий проект у Scratch і видаліть з нього спрайт кота. Ознайомитись із редактором Scratch можна за посиланням <a href="http://jumpto.cc/scratch-new" target="_blank">jumpto.cc/scratch-new</a>.

+ Оберіть об'єкт і фон гри. Ви можете обрати що завгодно! Ось приклад:
    
    ![screenshot](images/brain-setting.png)

+ Створіть 2 нові змінні `1`{:class="blockdata"} і `2`{:class="blockdata"}. Ці змінні збережуть 2 числа, що будуть перемножуватись.
    
    ![screenshot](images/brain-variables.png)

+ Додайте код до вашого об'єкта, надавши змінним значення ` випадкове`{:class="blockoperators"} число від 2 до 12.
    
    ```blocks
        when flag clicked
        set [number 1 v] to (pick random (2) to (12))
        set [number 2 v] to (pick random (2) to (12))
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