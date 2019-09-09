## Einen Countdown hinzufügen

\--- task \--- Erstelle auf der Bühne einen Countdown-Timer mit Hilfe einer neuen Variablen namens `Countdown` {: class = "block3variables"}. Der Countdown soll bei 30 Sekunden beginnen und bis 0 Sekunden herunterzählen.

![Bühnenbilder](images/stage-sprite.png)

\--- hints \--- \--- hint \---

Erstelle eine `Variable` {: class = "block3variables"}, nenne sie "Countdown" und setze seinen Wert auf `30` Sekunden.

Füge nun Code hinzu, um die Zeit in `Countdown` {: class = "block3variables"} innerhalb von 30 Sekunden auf 0 zu bringen. Um das zu erreichen, subtrahiere `1` von `Countdown` {: class = "block3variables"} alle `1` Sekunden und wiederholen dies bis `Countdown` {: class = "block3variables"} bei `0` angekommen ist.

\--- /hint \--- \--- hint \--- Hier sind die Code Blöcke die du brauchst:

```blocks3
wiederholen bis < >

ende

warten (1) Sekunden

ändere [Countdown v] um (-1)

(Countdown)

Wenn die grüne Flagge angeklickt wird

<() = ()>

setze [Countdown v] auf [30]
```

\--- /hint \--- \--- hint \--- So sollte dein Code Block aussehen:

```blocks3
Wenn die grüne Flagge angeklickt wird
setze [Countdown v] auf [30]
wiederhole bis < (Countdown) = [0] >
warte (1) Sekunden
ändere [Countdown v] um (-1)
ende
```

\--- /hint \--- \--- /hints \---

\--- /task \---

\--- task \---

Erstelle einen `sende`{:class="block3control"} Block der die Nachricht 'Ende' sendet. Das Nachrichten `senden` {: class = "block3control"} ist wie eine Ansage über einen Lautsprecher: Sie kann von allen Figuren gleichzeitig empfangen werden. Füge einen `sende` {: class = "block3control"} Block am Ende des Countdown Timer Codes hinzu, damit eine 'Ende' Nachricht geschickt wird, wenn `Countdown` {: class = "block3variables"} den Wert `0` erreicht hat.

![Bühnenbilder](images/stage-sprite.png)

```blocks3
    sende (Ende v) an alle
```

\--- /task \---

\--- task \--- Wähle deine Figur von vorhin aus und fügen den Code hinzu, damit die Figur `stoppe andere Skripte der Figur` {: class = "block3control"} ausführt, wenn es die Nachricht `Ende` {: class = "block3control"} empfängt.

![Giga Figur](images/giga-sprite.png)

```blocks3
    Wenn ich [Ende v] empfange
stoppe [andere Skripte der Figur v]
```

\--- /task \---

\--- task \---

Teste dein Spiel erneut. Es sollte immer neue Fragen stellen, bis der Countdown bis 0 gezählt hat.

\--- /task \---