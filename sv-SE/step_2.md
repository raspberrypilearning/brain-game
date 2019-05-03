## Skapa frågor

Du ska börja med att skapa slumpmässiga frågor som spelaren måste svara på.

\--- uppgift \---

Öppna ett nytt Scratch-projekt.

**Online:** open a new online Scratch project at [rpf.io/scratch-new](http://rpf.io/scratchon){:target="_blank"}.

**Offline:** Öppna ett nytt projekt i offline-editoren.

Om du behöver ladda ner och installera Scratch offline editoren kan du hitta den på [rpf.io/scratchoff](http://rpf.io/scratchoff){: target = "_ blank"}.

\--- / uppgift \---

\--- uppgift \--- Lägg till ett tecken och ett bakgrund för ditt spel. Du kan välja vilken du vill! Här är ett exempel:

![skärmdump](images/brain-setting.png)

\--- / uppgift \---

\--- uppgift \--- Se till att du har valt din karaktärssprite. Skapa två nya variabler, kallad `nummer 1`{: class = "block3variables"} och `nummer 2`{: class = "block3variables"}, för att lagra numren för frågesfrågorna.

![skärmdump](images/giga-sprite.png) ![skärmdump](images/brain-variables.png)

[[[generic-scratch3-add-variable]]]

\--- / uppgift \---

\--- uppgift \--- Lägg till kod till din karaktärsprite för att ange båda de `variablerna`{: class = "block3variables"} till ett `slumpmässigt`{: class = "block3operators"} nummer mellan 2 och 12.

![skärmdump](images/giga-sprite.png)

```blocks3
När flaggan klickade på
satt [nummer 1 v] till (välj slumpvis (2) till (12))
uppsättning [nummer 2 v] till (välj slumpvis (2) till (12))
```

\--- / uppgift \---

\--- uppgift \--- Lägg till kod till `fråga`{: class = "block3sensing"} spelaren för svaret och sedan `säg i 2 sekunder`{: class = "block3looks"} om svaret var rätt eller fel:

![skärmdump](images/giga-sprite.png)

```blocks3
När flaggan klickade på
satt [nummer 1 v] till (välj slumpvis (2) till (12))
uppsättning [nummer 2 v] till (välj slumpvis (2) till (12))

+ fråga (gå med i [x] (nummer 2))) och vänta
+ om <(svar) = ((nummer 1) * (nummer 2))> sedan
+ säg [ja! :)] för (2) sekunder
+ annat
+ säg [nej :(] för (2) sekunder
+ slut
```

\--- / uppgift \---

\--- uppgift \---

Testa ditt projekt två gånger: svara en fråga korrekt och den andra felaktigt.

\--- / uppgift \---

\--- uppgift \---

Lägg till en `alltid`{: class = "block3control"} loop runt denna kod, så att spelet frågar spelaren många frågor i rad.

\--- tips \--- \--- tips \---

Du måste lägga till ett `alltid`{: class = "block3control"} block och sätt in hela koden utom `när flaggan klickade på`{: class = "block3control"} blockera in den.

\--- / hint \--- \--- tips \--- Här är det block du behöver:

```blocks3
för evigt
slut
```

\--- / hint \--- \--- tips \--- Här är vad din kod ska se ut:

```blocks3
när flaggan klickade

+ för alltid
    set [nummer 1 v] till (välj slumpvis (2) till (12))
    set [nummer 2 v] till (välj slumpvis (2) till (12))
    fråga 1) (gå med [x] (nummer 2))) och vänta
    om <(svar) = ((nummer 1) * (nummer 2))> då
        säga [ja! :)] för (2) sekunder
    annars
        säga [nej :(] för (2) sekunder
    slut
slut
```

\--- / hint \--- \--- / tips \---

\--- / uppgift \---