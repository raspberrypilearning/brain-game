## צור שאלות

אתה הולך להתחיל על ידי יצירת שאלות אקראיות כי השחקן צריך לענות.

\--- \---

פתח פרוייקט חדש של Scratch.

**Online:** open a new online Scratch project at [rpf.io/scratch-new](http://rpf.io/scratch-new){:target="_blank"}.

**מקוון:** פתח פרוייקט חדש בעורך הלא מקוון.

אם עליך להוריד ולהתקין את העורך הלא מקוון של Scratch, תוכל למצוא אותו ב [rpf.io/scratchoff](http://rpf.io/scratchoff){: target = "_ _ blank"}.

\--- / משימה \---

\--- task \---

Add a character sprite and a backdrop for your game. You can choose any you like! Here's an example:

![screenshot](images/brain-setting.png)

\--- /task \---

\--- task \---

Make sure you have your character sprite selected. Create two new variables, called `number 1`{:class="block3variables"} and `number 2`{:class="block3variables"}, to store the numbers for the quiz questions.

![screenshot](images/giga-sprite.png)

![screenshot](images/brain-variables.png)

[[[generic-scratch3-add-variable]]]

\--- / משימה \---

\--- task \---

Add code to your character sprite to set both of the `variables`{:class="block3variables"} to a `random`{:class="block3operators"} number between 2 and 12.

![screenshot](images/giga-sprite.png)

```blocks3
כאשר הדגל לחץ על
קבע מספר [1] כדי לבחור (אקראי) 2 (עד) 12 ()
[מספר 2 v] ל (בחר אקראי) 2 (עד) 12
```

\--- /task \---

\--- task \---

Add code to `ask`{:class="block3sensing"} the player for the answer, and then `say for 2 seconds`{:class="block3looks"} whether the answer was right or wrong:

![screenshot](images/giga-sprite.png)

```blocks3
כאשר מספר הדקות לחץ על
[מספר [1]] ל (בחר אקראי) 2 (עד) 12 ()
[מספר 2 v] ל (בחר אקראי (2) עד (12))

+ שאל (הצטרף למספר 1) (2)) והמתן
+ אם <(תשובה) = (מספר 1) * (מספר 2))> ואז
+ אומר [כן! :)] עבור (2) שניות
+ אחר
+ say [no :(] עבור (2) שניות
+ סוף
```

\--- /task \---

\--- task \---

Test your project twice: answer one question correctly, and the other incorrectly.

\--- /task \---

\--- task \---

Add a `forever`{:class="block3control"} loop around this code, so that the game asks the player lots of questions in a row.

\--- hints \---

\--- hint \---

You need to add a `forever`{:class="block3control"} block, and put all of the code except the `when flag clicked`{:class="block3control"} block into it.

\--- /hint \---

\--- hint \---

Here is the block you need:

```blocks3
לנצח
סוף
```

\--- /hint \---

\--- hint \---

Here is what your code should look like:

```blocks3
כאשר הדגל לוחץ

+ לנצח
    סט [מספר 1 v] כדי (איסוף אקראי (2) עד (12))
    סט [מספר 2 v] כדי (איסוף אקראי (2) עד (12))
    לשאול (להצטרף (מספר 1) (הצטרף [x] (מספר 2)) והמתן
    אם <(תשובה) = ((מספר 1) (מספר 2))> ואז
        אומר [כן! :)] עבור (2) שניות
    אחר
        לומר [no :(] עבור (2) שניות
    סוף
סוף
```

\--- /hint \---

\--- /hints \---

\--- /task \---