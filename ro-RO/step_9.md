## Provocare: Cursa la 10 puncte

Puteți schimba jocul astfel încât jucătorul, în loc să răspundă la cât mai multe întrebări posibil în 30 de secunde, răspunde la 10 întrebări cât mai repede posibil.

Pentru a face această schimbare, trebuie doar să modificați codul cronometrului. Puteți vedea care blocuri trebuie să fie diferite?

```blocks3
    atunci când primesc [start v]
    set [timp v] până la (30)
    repeta pana <(timp) = [0]>
        wait (1) secunde
        schimbare [dată v] de (-1)
    final
    difuzare (end v)
```