## Einen Countdown hinzufügen

--- task --- Erstelle auf der Bühne einen Countdown-Timer mit Hilfe einer neuen Variablen namens `Countdown`{:class="block3variables"}. Der Countdown soll bei 30 Sekunden beginnen und bis 0 Sekunden herunterzählen.

![Bühnenbilder](images/stage-sprite.png)

--- hints ---
 --- hint ---

Erstelle eine `Variable`{:class="block3variables"}, nenne sie "Countdown" und setze ihren Wert auf `30` Sekunden.

Füge nun Code hinzu, um den `Countdown`{:class="block3variables"} innerhalb von 30 Sekunden auf 0 zu bringen. Um das zu erreichen, subtrahiere `1` von `Countdown`{:class="block3variables"} jede `1` Sekunde und wiederhole das bis `Countdown`{:class="block3variables"} gleich `0` ist.

--- /hint --- --- hint --- Hier sind die Code Blöcke die du brauchst:

```blocks3
wiederhole bis <>

ändere [Countdown v] um (1)

(Countdown)

Wenn die grüne Flagge angeklickt

<() = ()>

setze [Countdown v] auf [0]

warte (1) Sekunden
```

--- /hint --- --- hint --- So sollte dein Code Block aussehen:

```blocks3
Wenn die grüne Flagge angeklickt
setze [Countdown v] auf [30]
wiederhole bis < (Countdown) = [0] >
warte (1) Sekunden
ändere [Countdown v] um (-1)
ende
```

--- /hint ------ /hints ---

--- /task ---

--- task ---

`Sende`{:class="block3control"} die Nachricht 'Ende' an alle. `Senden`{:class="block3control"} ist wie eine Ansage über einen Lautsprecher: Sie kann von allen Figuren gleichzeitig empfangen werden. Füge einen `sende an alle`{:class="block3control"} Block am Ende des Countdown-Code hinzu, sodass eine 'Ende' Nachricht geschickt wird, wenn `Countdown`{:class="block3variables"} den Wert `0` erreicht hat.

![Bühnenbilder](images/stage-sprite.png)

```blocks3
    sende (Ende v) an alle
```

--- /task ---

--- task --- Wähle deine Figur und füge den Code hinzu, damit die Figur `andere Skripte der Figur stoppt`{:class="block3control"}, wenn es die Nachricht `Ende`{:class="block3control"} empfängt.

![Giga Figur](images/giga-sprite.png)

```blocks3
Wenn ich [Ende v] empfange
stoppe [andere Skripte der Figur v]
```

--- /task ---

--- task ---

Teste dein Spiel erneut. Es sollte neue Fragen stellen, bis der Countdown 0 erreicht.

--- /task ---