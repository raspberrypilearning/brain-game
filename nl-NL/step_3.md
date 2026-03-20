## Een tijdklok toevoegen

--- task ---

Maak een afteltimer op het speelveld met behulp van een nieuwe variabele genaamd `tijd`{:class="block3variables"}. De timer moet op 30 seconden beginnen met aftellen tot 0 seconden.

![Speelveld sprite](images/stage-sprite.png)

--- hints ---
 --- hint ---

Maak een `variabele`{:class="block3variables"}, noem hem 'tijd', en stel de waarde in op `30`.

Voeg vervolgens code toe om `tijd`{:class="block3variables"} af te tellen tot 0 binnen 30 seconden. Om dit te doen, trek je elke `1` seconde `1` van `tijd`{:class="block3variables"} af, en herhaal dit totdat `tijd`{:class="block3variables"} gelijk is aan `0`.

--- /hint ---

--- hint ---

Dit zijn de codeblokken die je nodig hebt:

```blocks3
repeat until < >

end

wait (1) seconds

change [tijd v] by (1)

(tijd)

when flag clicked

<() = ()>

set [tijd v] to [0]
```

--- /hint ---

--- hint ---

Zo zou je nieuwe code er uit moeten zien:

```blocks3
when flag clicked
set [tijd v] to [30]
repeat until <(tijd) = (0)>
  wait (1) seconds
  change [tijd v] by (-1)
end
```

--- /hint ---

--- /hints ---

--- /task ---

--- task ---

Maak een `zend signaal`{:class="block3control"} die het signaal 'einde' verstuurt. Een `zend signaal`{:class="block3control"} is als een aankondiging over een luidspreker: het kan worden gehoord door al je sprites. Voeg het `zend signaal`{:class="block3control"} blok toe aan het einde van de timercode zodat de code het signaal 'einde' verstuurt wanneer de `tijd`{:class="block3variables"} is afgeteld tot `0`.

![Speelveld sprite](images/stage-sprite.png)

```blocks3
    broadcast (einde v)
```

--- /task ---

--- task ---

Selecteer je personage en voeg code toe zodat de sprite `stop andere scripts`{:class="block3control"} uitvoert wanneer het het signaal `einde`{:class="block3control"} ontvangt.

![Giga sprite](images/giga-sprite.png)

```blocks3
    when I receive [einde v] 
stop [andere scripts in sprite v]
```

--- /task ---

--- task ---

Test je spel opnieuw. Het moet vragen blijven stellen totdat de timer is afgeteld tot 0.

--- /task ---