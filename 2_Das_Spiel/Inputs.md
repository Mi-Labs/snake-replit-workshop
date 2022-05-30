JS Workshop für Beginner - Summer Coding Festival THB 2022

## Inputs
Jedes Spiel und auch jedes Software ist auf die Eingabe vom Nutzer angewiesen. In JS können wir mit speziellen Funktionen(Listenern) jede Eingabe erkennen und diese dann für unsere Zwecke nutzen.
Wir werden mit der Funktion ``onKeyPress()`` arbeiten.

<br>

### onKeyPress()
Mit der Funktion onKeyPress kann in Kaboom.js ein Tastendruck erkannt werden. 

Das kann beispielsweise so aussehen:

````js
onKeyPress("down",function(){
    // Hier passiert jetzt etwas wie zum Beispiel:
    player.move(0,-10)
})
````

Als erster Parameter wird hier die gewünschte Taste eingebunden, hier ``"down"`` also hier der Tastendruck nach unten. Der zweite Parameter ist ein Funktionsaufruf. Diese Funktion wird ausgeführt, wenn der entsprechende Tastendruck erkannt wird. 


Was ihr in der [Dokumentation](https://kaboomjs.com/#onKeyDown) seht, ist dazu fast identisch
````js
onKeyPress("down",() => {
    // Hier passiert jetzt etwas wie zum Beispiel:
    player.move(0,-10)
})
````
Hierbei ist die Schreibweise angepasst worden. Diese Art von Funktion nennt sich Arrow-Funktion und spart einiges an Schreibarbeit. Die Parameter kommen in die ``()`` und dann wird mit dem Pfeil auf den Funktionskörper verwiesen.

<br>

### Welche Tasten werden erkannt
Aus der Dokumentation:

````text
"f1" | "f2" | "f3" | "f4" | "f5" | "f6" | "f7" | "f8" | "f9" | "f10" | "f11" | "f12" |
"`" | "1" | "2" | "3" | "4" | "5" | "6" | "7" | "8" | "9" | "0" | "-" | "=" |
"q" | "w" | "e" | "r" | "t" | "y" | "u" | "i" | "o" | "p" |
"[" | "]" | "\" |
"a" | "s" | "d" | "f" | "g" | "h" | "j" | "k" | "l" |
"" | "'" |
"z" | "x" | "c" | "v" | "b" | "n" | "m" |
"," | "." | "/" | "backspace" | "enter" | "tab" | "space" | " " | "left" | "right" | "up" | "down"
````

<br>

### A - Schreibe eine Tastenerkennung für die Pfeiltaste nach unten
Für das Spiel brauchen wir jetzt verschiedene Tastendruckfunktionen.
Als erstes schreiben wir die Funktion mit dem Tastendruck nach unten. Von dieser Funktion können wir dann die andernen Tasten ableiten.

*Schreibe ein Funktion, die bei einem Tastendruck auf die Pfeiltaste nach unten auslöst*


### A- Schreibe die restlichen Tastenerkennungen für das Spiel

*Schreibe nun die Funktionen für die verbleibenden Richtungen (oben|rechts|links)*
