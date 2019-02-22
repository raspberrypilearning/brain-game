## Výzva: závod na 10 bodov

Môžete zmeniť svoju hru tak, aby hráč namiesto odpovede na čo najviac otázok v priebehu 30 sekúnd odpovedal na 10 otázok čo najrýchlejšie.

Ak chcete vykonať túto zmenu, stačí zmeniť kód časovača. Môžete vidieť, ktoré bloky musia byť odlišné?

```blocks3
    pri príjme [štart V]
    sadu [čas] pre (30),
    opakovanie až <(čas) = [0]>
        čakania (1) sekundy
        zmene [čas v] o (-1)
    koniec
    vysielania (koniec v)
```