## Додавання графіки

Instead of your character just saying `yes! :)` or `nope :(` to the player, let's add some graphics that will let the player know how they are doing.

+ Create a new sprite called 'Result', containing both a 'tick' and a 'cross' costume.
    
    ![знімок екрану](images/brain-result.png)

+ Change your character's code, so that instead of telling the player how they did, it broadcasts `correct`{:class="blockevents"} and `wrong`{:class="blockevents"} messages instead.
    
    ![знімок екрану](images/brain-broadcast-answer.png)

+ You can now use these messages to show the 'tick' or 'cross' costume. Add this code to your new 'Result' sprite:
    
    ![знімок екрану](images/brain-show-answer.png)

+ Test out your game again. You should see a tick whenever you get a question correct, and a cross whenever you get one wrong!
    
    ![знімок екрану](images/brain-test-answer.png)

+ Have you noticed that the code for `when I receive correct`{:class="blockevents"} and `when I receive wrong`{:class="blockevents"} is nearly identical? Let's create a function to make it easier for you to make changes to your code.
    
    On your 'Result' sprite, click `More Blocks`{:class="blockmoreblocks"}, and then 'Make a Block'. Create a new function called `animate`{:class="blockmoreblocks"}.
    
    ![знімок екрану](images/brain-animate-function.png)

+ You can then add the animation code into your new animation function, and then just use the function twice:
    
    ![знімок екрану](images/brain-use-function.png)

+ Now, if you want to show the tick and the cross for a longer or shorter time, you only need to make one change to your code. Try it!

+ Instead of just showing and hiding the tick and the cross, you could change your animation function, so that the graphics fade in.
    
    ```blocks
        визначити [animate]
        встановити ефект [привид v] в (100)
        показати
        повторити (25) 
              змінити ефект [привид v] на (-4)
        end
        сховати
    ```