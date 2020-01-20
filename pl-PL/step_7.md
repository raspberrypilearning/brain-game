## Dodaj grafikę

W tej chwili duszek postaci po prostu mówi `tak! :)` lub `nie :(` na odpowiedzi gracza. Dodaj grafikę, aby poinformować gracza, czy odpowiedź jest poprawna, czy niepoprawna.

\--- task \---

Utwórz nowy duszek o nazwie „Wynik” i nadaj mu kostium „zaznaczony/sprawdzony” oraz „krzyżyk”.

![Duszek z kostiumami „zaznaczony” i „krzyżyk”](images/brain-result.png)

\--- /task \---

\--- task \---

Zmień kod duszka postaci, aby zamiast mówić coś graczowi, `nadawał komunikat`{:class="block3events"} „dobrze” lub „źle”.

![Duszek postaci](images/giga-sprite.png)

```blocks3
jeżeli <(odpowiedź) = ((liczba 1) * (liczba 2))> to
- powiedz [tak! :)] przez (2) sekund
+ nadaj komunikat (poprawnie v)
w przeciwnym razie
- powiedz [nie :(] przez (2) sekund
+ nadaj komunikat (niepoprawnie v)
koniec
```

\--- /task \---

\--- task \---

Teraz możesz użyć tych komunikatów do `pokazania`{:class="block3looks"} kostiumu „zaznaczony” lub „krzyżyk”. Dodaj następujący kod do duszka „Wynik”:

![Duszek wyniku](images/result-sprite.png)

```blocks3
    kiedy otrzymam [dobrze v]
    zmień kostium na (zaznaczony v)
    pokaż
    czekaj (1) sekund
    ukryj

    kiedy otrzymam [źle v]
    zmień kostium na (krzyżyk v)
    pokaż
    czekaj (1) sekund
    ukryj

    kiedy zielona flaga kliknięta
    ukryj
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
definiuj animacja
pokaż
czekaj (1) sekund
ukryj
```

\--- /task \---

\--- task \---

Make sure you have removed the `show`{:class="block3looks"} and `hide`{:class="block3looks"} blocks below **both** of the `switch costume`{:class="block3looks"} blocks.

Then add the `animate`{:class="block3myblocks"} block below both of the `switch costume`{:class="block3looks"} blocks. Your code should now look like this:

![Result sprite](images/result-sprite.png)

```blocks3
    
kiedy otrzymam [poprawnie v]
zmień kostium na (zaznaczony v)
animacja:: własna

kiedy otrzymam [niepoprawnie v]
zmień kostium na (krzyżyk v)
animacja:: własna
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
    definiuj animacja
    ustaw efekt [duch v] na (100)
    pokaż
    powtórz (25)
        zmień efekt [duch v] przez (-4)
    koniec
    ukryj
```

\--- /task \---

Can you improve the animation of the 'tick' or 'cross' graphics? You could add code to make the costumes fade out as well, or you could use other cool effects:

![screenshot](images/brain-effects.png)