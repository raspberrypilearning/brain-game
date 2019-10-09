## Flera spel

Nu ska du lägga till en "Play" -knapp så att spelaren kan spela ditt spel många gånger.

\--- uppgift \--- Skapa en ny "Play" -knappsprite som spelaren behöver klicka för att starta ett nytt spel.

Du kan rita spritet själv eller redigera en sprite från biblioteket.

![Bild på spelknappen](images/brain-play.png)

\--- / uppgift \---

\--- uppgift \--- Lägg till den här koden till din knapp sprite:

![Button Sprite](images/button-sprite.png)

```blocks3
    när flaggan klickade
    visar

    när den här sprite klickade
    hide
    broadcast (start v)
```

\--- / uppgift \---

Den nya koden innehåller ett annat `sändningsblock`{: class = "block3events"} som skickar meddelandet "start".

Den nya koden gör spelshowen "Play" när när spelaren klickar på flaggan. När spelaren klickar på knappspriten, skjuter sprite och sänder sedan ett meddelande som andra sprites kan reagera på.

För tillfället börjar teckensprayen ställa frågor när spelaren klickar på flaggan. Ändra ditt spelets kod så att charactersprite börjar ställa frågor när den tar emot "start" `sändningen`{: class = "block3events"}.

\--- uppgift \--- Välj din karaktärsprite och ersätt `när flaggan klickar`{: class = "block3events"} blockera med en `när jag får start`{: class = "block3events" } block.

![Karaktärsprite](images/giga-sprite.png)

```blocks3
<br />- när flaggan klickade
+ när jag mottar [start v]
set [number 1 v] till (välj slumpvis (2) till (12))
set [nummer 2 v] till (välj slumpvis (2) till (12) )
fråga (ansluta (nummer 1) (gå med i [x] (nummer 2))) och vänta
om <(svar) = ((nummer 1) * (nummer 2))> då
    säga [ja! :)] för (2) sekunder
annars
    säga [nope :(] för (2) sekunder
slutet
```

\--- / uppgift \---

\--- uppgift \---

Klicka på den gröna flaggan och klicka sedan på den nya "Play" -knappen för att testa om det fungerar. Du bör se att spelet inte startar innan du klickar på knappen.

\--- / uppgift \---

Kan du se att timern börjar när den gröna flaggan klickas, istället för när spelet börjar?

![Timern har startat](images/brain-timer-bug.png)

\--- uppgift \---

Kan du ändra koden för timern så att timern börjar när spelaren klickar på knappen?

\--- / uppgift \---

\--- uppgift \--- Lägg till kod till din knappsprid så att knappen visar igen i slutet av varje spel.

![Button Sprite](images/button-sprite.png)

```blocks3
    när jag får [end v]
    show
```

\--- / uppgift \---

\--- uppgift \---

Testa "Spela" -knappen genom att spela ett par spel. Knappen ska visas i slutet av varje spel.

För att testa spelet snabbare kan du ändra värdet på `time`{: class = "block3variables"} så att varje spel är bara några sekunder lång.

![Skede](images/stage-sprite.png)

```blocks3
    sätt [tid v] till [10]
```

\--- / uppgift \---

\--- uppgift \--- Du kan ändra hur knappen ser ut när muspekaren svänger över den.

![Knapp](images/button-sprite.png)

```blocks3
    när flaggan klickade
    visa
    alltid
    om <touching (mouse-pointer v)?> sedan
        sätt [fisheye v] effekt till (30)
    annat
        set [fisheye v] effekt till (0)
    slutet
    slutet
```

![skärmdump](images/brain-fisheye.png) \--- / uppgift \---