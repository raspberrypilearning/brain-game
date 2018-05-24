## Створення запитань

Розпочнемо зі створення випадкових запитань для гравців.

+ Почніть новий проект у Scratch і видаліть з нього спрайт кота. Ознайомитись із редактором Scratch можна за посиланням <a href="http://jumpto.cc/scratch-new" target="_blank">jumpto.cc/scratch-new</a>.

+ Оберіть об'єкт і фон гри. Ви можете обрати що завгодно! Ось приклад:
    
    ![screenshot](images/brain-setting.png)

+ Створіть 2 нові змінні `1`{:class="blockdata"} і `2`{:class="blockdata"}. Ці змінні збережуть 2 числа, що будуть перемножуватись.
    
    ![screenshot](images/brain-variables.png)

+ Додайте код до вашого об'єкта, надавши змінним значення ` випадкове число`{:class="blockoperators"} від 2 до 12.
    
    ```blocks
        коли натиснуто ⚑    надати [number 1 v] значення (випадкове від (2) до (12))
        надати [number 2 v] значення (випадкове від (2) до (12))
    ```

+ Тоді ви можете попросити гравця дати відповідь і повідомити його чи була вона правильною.
    
    ```blocks
        коли натиснуто ⚑
    надати [number 1 v] значення (випадкове від (2) до (12))
    надати [number 2 v] значення (випадкове від (2) до (12))
    запитати (з'єднати (number 1) (з'єднати [ x ] (number 2))) і чекати
    якщо <(answer) = ((number 1) * (number 2))>; то 
      говорити [yes! :\)\] for (2) secs
    else
    говорити [nope :(] (2) сек
    end
    ```

+ Перевірте свій проект повною мірою: на одне питання дайте правильну відповідь, а на інше - неправильну.

+ Додайте команду `завжди`{:class="blockcontrol"} біля цього коду, щоб гравець мав багато запитань.

+ Create a countdown timer on the stage, using a variable called `time`{:class="blockdata"}. The 'Ghostbusters' project has instructions for making a timer (in step 5) if you need help!

+ Test your project again - you should be able to continue asking questions until the time runs out.