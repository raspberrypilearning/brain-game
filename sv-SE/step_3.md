## Lägg till en timer

\--- uppgift \--- Skapa en nedräkningstimer på scenen med hjälp av en ny variabel som heter `gång`{: class = "block3variables"}. Timern bör börja om 30 sekunder och räkna ner till 0 sekunder.

![Stagesprit](images/stage-sprite.png)

\--- tips \--- \--- tips \---

Skapa en `variabel`{: class = "block3variables"}, kalla det "tid" och sätt dess värde till `30`.

Lägg sedan till kod för att räkna `gång`{: class = "block3variables"} ner till 0 inom 30 sekunder. För att göra detta, subtrahera `1` från `tid`{: class = "block3variables"} varje `1` sekund, och upprepa detta tills `tid`{: class = "block3variables"} lika `0`.

\--- / tips \--- \--- tips \--- Här är de block du behöver:

```blocks3
upprepa till < >

slut

vänta (1) sekunder

ändra [tid v] av (1)

(tid)

när flaggan klickas

<() = ()>

set [tid v] till [0]
```

\--- / hint \--- \--- tips \--- Här är vad din nya kod ska se ut:

```blocks3
när flaggan klickade
set [tid v] till [30]
upprepa tills <(tid) = (0)>
    vänta (1) sekunder
    ändra [tid v] av (-1)
slutet
```

\--- / hint \--- \--- / tips \---

\--- / uppgift \---

\--- uppgift \---

Skapa en `sändning`{: class = "block3control"} som skickar meddelandet "slutet". En `sändning`{: class = "block3control"} är som ett meddelande över en högtalare: det kan höras av alla dina sprites. Lägg till `sändningen`{: class = "block3control"} blocken till slutet av timerkoden så att koden skickas och "avsluta" meddelandet när `tiden`{: class = "block3variables"} har räknats ner till `0`.

![Stagesprit](images/stage-sprite.png)

```blocks3
    sändning (slutet v)
```

\--- / uppgift \---

\--- uppgift \--- Välj din karaktärssprite och lägg till någon kod så att sprite `stannar de andra skript`{: class = "block3control"} när den tar emot `slutet`{: class = "block3control"} meddelande .

![Giga sprite](images/giga-sprite.png)

```blocks3
    när jag får [end v]
    stop [andra skript i sprite v]
```

\--- / uppgift \---

\--- uppgift \---

Testa ditt spel igen. Det borde fortsätta att ställa frågor tills timern har räknat ner till 0.

\--- / uppgift \---