JS Workshop für Beginner - Summer Coding Festival THB 2022

## Die Schlange

Für Snake brauchen wir natürlich die Schlange, die der Spieler steuert.

Nach den Regeln wird die Schlange immer länger, wenn sie Essen aufnimmt und sie kann sich immer nur in eine vorbestimmte Richtung bewegen.

### Der Schlangenkörper
Man kann sich den Schlangenkörper als eine Reihe von Schlangensegmenten vorstellen

````text
Schlange = [o][o][o][o]
````
Jedes Segement besitzt folgende Eigenschaften:
- Rechteck (zum Zeichnen auf dem Spielfeld)
- Position (wo befindet sich das Segment auf dem Spielfeld)
- Farbe
- Kollisionerkennung
- Tag (Zugehörigkeit zur Schlange)

Diese Segmente können beispielsweise in einem Array gespeichert werden, sodass diese leicht erreichbar sind und sich gut organisieren lassen.
<br>

### A - Erzeuge ein Schlangensegment als Gameobjekt
Aus den Eigenschaften des Schlangensegments müssen für das Spiel Gameobjekte erzeugt werden. 
Falls du nicht genau weißt, wie du das Programmieren kannst, schau gerne in das Dokument `Game_Objekte.md`

*Schreibe den Quellcode für ein Schlangensegment*

<br>

### Zusammenführen der Segmente
Damit wir den Code für die Schlangensegemente nicht vielfach aufschreiben müssen, nutzen wir eine Schleife und Array-Funktionen um dynamisch die Schlange zu erzeugen.

In unsere Fall ist eine For-Schleife sinnvoll.
````text
for(let i = 1; i <= SCHLANGENLAENGE; i++){
 1 // Erzeuge das Segment
 2 // Speichere das SEGMENT
 3 SCHLANGENKOERPER.push(SEGMENT)
}
````
Was diese Schleife macht, ist Folgendes:
1. Die Schleife wiederholt sich so lange bis ``i`` größer ist als die Schlangenlänge
2. Bei jedem Schleifendurchlauf wird ``i`` um 1 erhöht
3. Der Inhalt der Schleife ``1-3`` wird bei jedem Durchlauf ausgeführt
4. Bei ``3`` wird das Segement an einen Array mit dem Schlangenkörper angehängt

<br>

### A - Deklariere die Schlange im Quellcode
Damit wir während der gesamten Laufzeit des Spiels auf die Schlange zugreifen können.

Ein Array lässt sich so deklarieren: ``let array = [];``

*Deklariere den Schlangenkörper (array) und die Schlangenlänge (int) im Quellcode*

<br>

### A - Schreibe eine Funktion, die die komplette Schlange erzeugt
Nutze jetzt deinen Quellcode für das Schlangensegment und die Schleife um eine Funktion zu schreiben, die eine Schlange erzeugt.

Es macht Sinn, die Variablen für den Schlangenkörper und die Schlangenlänge auf ihre Standardwerte zurückzusetzen, bevor du die Schlange erzeugst.

*Schreibe den Quellcode für die Erzeugung einer Schlange mit 3 Segementen*











