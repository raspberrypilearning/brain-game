--- challenge ---
## Aufgabe: Wettrennen zu 10 Punkten
Kannst du dein Spiel ändern, damit (statt so viele Fragen wie möglich innerhalb von 30 Sekunden richtig zu beantworten) der Spieler sehen kann, wie schnell er 10 Fragen richtig beantworten kann?

Um dies zu tun brauchst du nur den Code deiner Zeituhr zu ändern. Kannst du sehen, was geändert werden muss?

```blocks
	Wenn ich [start v] empfange
	setze [time v] auf (30)
	wiederhole bis <(time) = [0]>
   		warte (1) Sek.
   		ändere [time v] um (-1)
	Ende
	sende [Ende v] an alle
```




--- /challenge ---