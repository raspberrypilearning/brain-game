## Haaste: kilpailu 10 pisteen

Voisitko vaihtaa pelisi niin, että pelaaja vastaisi mahdollisimman moniin kysymyksiin 30 sekunnin kuluessa 10 kysymykseen mahdollisimman nopeasti.

Jos haluat tehdä muutoksen, sinun tarvitsee vain muuttaa ajastinkoodiasi. Voitteko nähdä, mitkä lohkot täytyy olla erilaiset?

```blocks3
    kun vastaanotan [aloitus v]
    asetettu [aika v] - (30)
    toistoa, kunnes <(aika) = [0]>
        odota (1) sekuntia
        muutos [aika v] (-1)
    loppuun
    lähetys (loppu) v)
```