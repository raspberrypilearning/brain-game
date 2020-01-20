## Afbeeldingen toevoegen

Op dit moment zegt de personage-sprite gewoon `goed! :)` of `fout :(` op de antwoorden van de speler. Voeg wat grafische afbeeldingen toe om de speler te laten weten of hun antwoord goed of fout is.

\--- task \---

Maak een nieuwe sprite met de naam 'Resultaat', die zowel een 'vinkje'- als een 'kruis'-uiterlijk bevat.

![Sprite met vinkje en kruis uiterlijk](images/brain-result.png)

\--- /task \---

\--- task \---

Wijzig de code van je personage-sprite zodat, in plaats van iets tegen de speler te zeggen, het een `zend signaal`{:class="block3events"} 'goed' of 'fout' verstuurt.

![Personage-sprite](images/giga-sprite.png)

```blocks3
als <(antwoord) = ((nummer 1) * (nummer 2))> dan

- zeg [goed! :)] (2) sec.
+ zend signaal (goed v)
anders
- zeg [jammer :(] (2) sec.
+ zend signaal (fout v)
end
```

\--- /task \---

\--- task \---

Nu kun je deze signalen gebruiken om het 'vinkje'- of 'kruis'-uiterlijk te kiezen bij `verander uiterlijk naar`{:class="block3looks"}. Voeg de volgende code toe aan de sprite 'Resultaat':

![Resultaat sprite](images/result-sprite.png)

```blocks3
    wanneer ik signaal [goed v] ontvang
    verander uiterlijk naar (vinkje v)
    verschijn
    wacht (1) sec.
    verdwijn

 wanneer ik signaal [fout v] ontvang
    verander uiterlijk naar (kruis v)
    verschijn
    wacht (1) sec.
    verdwijn

  wanneer groene vlag wordt aangeklikt
    verdwijn
```

\--- /task \---

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
definieer animatie
verschijn
wacht (1) sec.
verdwijn
```

\--- /task \---

\--- task \---

Make sure you have removed the `show`{:class="block3looks"} and `hide`{:class="block3looks"} blocks below **both** of the `switch costume`{:class="block3looks"} blocks.

Then add the `animate`{:class="block3myblocks"} block below both of the `switch costume`{:class="block3looks"} blocks. Your code should now look like this:

![Result sprite](images/result-sprite.png)

```blocks3
    wanneer ik signaal [goed v] ontvang
    verander uiterlijk naar (vinkje v)
    animatie

wanneer ik signaal [fout v] ontvang
    verander uiterlijk naar (kruis v)
    animatie
```

\--- /task \---

Because of the custom `animate`{:class="block3myblocks"} block, you now only need to make one change to your code if you want to show the 'Result' sprite's costumes a longer or shorter time.

\--- task \---

Change your code so that the 'tick' or 'cross' costumes display for 2 seconds.

\--- /task \---

\--- task \---

Instead of `showing`{:class="block3looks"} and `hiding`{:class="block3looks"} the 'tick' or 'cross' costumes, you could change your `animate`{:class="block3myblocks"} block so that the costumes fade in.

![Result sprite](images/result-sprite.png)

```blocks3
    definieer animatie
  zet [geest v] effect op (100)
  verschijn
  herhaal (25)
    verander [geest v] effect met (-4)
  einde
  verdwijn
```

\--- /task \---

Can you improve the animation of the 'tick' or 'cross' graphics? You could add code to make the costumes fade out as well, or you could use other cool effects:

![screenshot](images/brain-effects.png)