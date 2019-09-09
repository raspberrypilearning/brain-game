## Create questions

You're going to start by creating random questions that the player has to answer.

\--- task \---

නව Scratch ව්යාපෘතියක්(project එකක්) විවෘත්ත කරන්න.

**අන්තර්ජාල මාර්ගගත(Online):** [rpf.io/scratch-new](http://rpf.io/scratch-new){:target="_blank"} හි අන්තර්ජාල මාර්ගගතව නව Scratch ව්‍යාපෘතියක් විවෘත කරන්න.

**අන්තර්ජාලයට නොබැඳිව(Offline):** නොබැඳි සංස්කාරකයේ(offline editor එකේ) නව ව්‍යාපෘතියක්(new project එකක්) විවෘත කරන්න.

ඔබට Scratch නොබැඳි සංස්කාරකය(offline editor එක) බාගත(download) කර ස්ථාපනය(install) කිරීමට අවශ්‍ය නම්, ඔබට එය [rpf.io/scratchoff](http://rpf.io/scratchoff){:target="_blank"} වෙතින් ලබාගත හැකිය.

\--- /task \---

\--- task \--- Add a character sprite and a backdrop for your game. You can choose any you like! Here's an example:

![තිර රුව(screenshot)](images/brain-setting.png)

\--- /task \---

\--- task \--- Make sure you have your character sprite selected. Create two new variables, called `number 1`{:class="block3variables"} and `number 2`{:class="block3variables"}, to store the numbers for the quiz questions.

![තිර රුව(screenshot)](images/giga-sprite.png) ![තිර රුව(screenshot)](images/brain-variables.png)

[[[generic-scratch3-add-variable]]]

\--- /task \---

\--- task \--- Add code to your character sprite to set both of the `variables`{:class="block3variables"} to a `random`{:class="block3operators"} number between 2 and 12.

![තිර රුව(screenshot)](images/giga-sprite.png)

```blocks3
when flag clicked
set [number 1 v] to (pick random (2) to (12))
set [number 2 v] to (pick random (2) to (12))
```

\--- /task \---

\--- task \--- Add code to `ask`{:class="block3sensing"} the player for the answer, and then `say for 2 seconds`{:class="block3looks"} whether the answer was right or wrong:

![තිර රුව(screenshot)](images/giga-sprite.png)

```blocks3
when flag clicked
set [number 1 v] to (pick random (2) to (12))
set [number 2 v] to (pick random (2) to (12))

+ ask (join (number 1)(join [ x ] (number 2))) and wait
+ if <(answer) = ((number 1)*(number 2))> then
+ say [yes! :)] for (2) seconds
+ else
+ say [no :(] for (2) seconds
+ end
```

\--- /task \---

\--- task \---

Test your project twice: answer one question correctly, and the other incorrectly.

\--- /task \---

\--- task \---

Add a `forever`{:class="block3control"} loop around this code, so that the game asks the player lots of questions in a row.

\--- hints \--- \--- hint \---

You need to add a `forever`{:class="block3control"} block, and put all of the code except the `when flag clicked`{:class="block3control"} block into it.

\--- /hint \--- \--- hint \--- Here is the block you need:

```blocks3
forever
end
```

\--- /hint \--- \--- hint \--- Here is what your code should look like:

```blocks3
when flag clicked

+ forever
    set [number 1 v] to (pick random (2) to (12))
    set [number 2 v] to (pick random (2) to (12))
    ask (join (number 1)(join [ x ] (number 2))) and wait
    if <(answer) = ((number 1)*(number 2))> then
        say [yes! :)] for (2) seconds
    else
        say [no :(] for (2) seconds
    end
end
```

\--- /hint \--- \--- /hints \---

\--- /task \---