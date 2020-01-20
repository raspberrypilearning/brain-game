## הוסף גרפיקה

כרגע, הדמות ספרייט רק אומר `כן! :)` או `לא: (` לתשובות השחקן, הוסף כמה גרפיקה כדי לתת לשחקן לדעת אם התשובה נכונה או לא נכונה.

\--- \---

יצירת ספרייט חדש בשם 'תוצאה', ולתת לו 'סמן / לבדוק' ו 'לחצות' תחפושת.

![ספרייט עם טיק ותלבושות לחצות](images/brain-result.png)

\--- / משימה \---

\--- \---

שינוי הקוד של ספרייט הדמות שלך כך, במקום לומר משהו לשחקן, זה `שידורים`{: class = "block3events"} המסרים "נכון" או "לא נכון".

![שדון תווים](images/giga-sprite.png)

```blocks3
אם <(תשובה) = ((מספר 1) (מספר 2))> ואז

- לומר [כן! :)] עבור (2) שניות
+ שידור (נ נכונה)
אחר
- אומרים [nope :(] עבור (2) שניות
+ שידור (נ טועה)
סוף
```

\--- / משימה \---

\--- \---

עכשיו אתה יכול להשתמש בהודעות אלה ל `הצג`{: class = "block3looks"} את "טיק" או "לחצות" תלבושת. הוסף את הקוד הבא לספרייט 'תוצאה':

![תוצאה ספרייט](images/result-sprite.png)

```blocks3
    כאשר אני מקבל [תלבושת נכונה]
    תלבושת ל (טיק v)
    הצג
    לחכות (1) שניות
    הסתר

    כאשר אני מקבל [לא נכון]
    תלבושת לעבור ל (לחצות v)
    להראות
    לחכות (1) שניות
    להסתיר

    כאשר דגל נלחץ
    להסתיר
```

\--- / משימה \---

\--- task \---

Test your game again. You should see the tick whenever you answer a question correctly, and the cross whenever you answer incorrectly!

![Tick for correct, cross for wrong answer](images/brain-test-answer.png)

\--- /task \---

Can you see that the code for `when I receive correct`{:class="block3events"} and `when I receive wrong`{:class="block3events"} is nearly identical?

So you can change your code more easily, you are going to create a custom block.

\--- task \---

Select the 'Result' sprite. Then click on `My Blocks`{:class="block3myblocks"}, and then on **Make a Block**. Create a new block and call it `animate`{:class="block3myblocks"}.

![Result sprite](images/result-sprite.png)

![Create a block called animate](images/brain-animate-function.png)

\--- /task \---

\--- task \---

Move the code to `show`{:class="block3looks"} and `hide`{:class="block3looks"} the 'Result' sprite into the `animate`{:class="block3myblocks"} block:

![Result sprite](images/result-sprite.png)

```blocks3
הגדר אנימציה
הצג
המתן (1) שניות
הסתר
```

\--- /task \---

\--- task \---

Make sure you have removed the `show`{:class="block3looks"} and `hide`{:class="block3looks"} blocks below **both** of the `switch costume`{:class="block3looks"} blocks.

Then add the `animate`{:class="block3myblocks"} block below both of the `switch costume`{:class="block3looks"} blocks. Your code should now look like this:

![Result sprite](images/result-sprite.png)

```blocks3
    כאשר אני מקבל [v נכונה]
    תחפושת מתג ל (טיק v)
    הנפשת :: מותאם אישית

    כאשר אני מקבל [v טועה]
    תחפושת לעבור (לחצות v)
    הנפשת :: מותאם אישית
```

\--- /task \---

Because of the custom `animate`{:class="block3myblocks"} block, you now only need to make one change to your code if you want to show the 'Result' sprite's costumes a longer or shorter time.

\--- task \---

Change your code so that the 'tick' or 'cross' costumes display for 2 seconds.

\--- / משימה \---

\--- task \---

Instead of `showing`{:class="block3looks"} and `hiding`{:class="block3looks"} the 'tick' or 'cross' costumes, you could change your `animate`{:class="block3myblocks"} block so that the costumes fade in.

![Result sprite](images/result-sprite.png)

```blocks3
    מגדירים להנפיש
    סט [v רפאים] תוקף (100)
    הראה
    חוזר (25)
        שינוי אפקט [רפאים v] (-4)
    סוף
    להסתיר
```

\--- /task \---

Can you improve the animation of the 'tick' or 'cross' graphics? You could add code to make the costumes fade out as well, or you could use other cool effects:

![screenshot](images/brain-effects.png)