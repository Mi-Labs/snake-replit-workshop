JS Workshop für Beginner - Sommer Coding Festival THB 2022

## Leveldesign

In kaboom.js lässt sich über die Funktion ``addLevel()`` eine Spielfläche (Map) erzeugen.
Dies kann beispielsweise so aussehen:

````text

            I
    ==      I
            I 
 =======  ==I
````
So könnte beispielsweise ein SuperMario-Level aussehen, die Plattformen mit "="-Zeichen und die Fahne mit "I".

Die Dokumentation zu der Funktion befindet sich [hier](https://kaboomjs.com/#addLevel)

### A - Erzeuge ein Spielfeld für das Snake-Spiel
Um Snake zu spielen wird ein Spielfeld mit Rändern benötigt. Diese sollen später dann bei Kollision das Spiel beenden.
Als erster Schritt brauchen wir ein einfaches Spielfeld.

*Erzeuge ein Spielfeld (15 mal 15 Felder) für das Spiel*


### Weitere Informationen zu addLevel
``addLevel()`` kann neben der Map noch weitere Optionen entgegennehmen.

- Breite jedes Blocks: ``width: 32``
- Höhe jedes Blocks:   ``heigth: 32``
- Definition von jedem Symbol:
````
"=": () =>[
  rect(32,32),
  color(0,255,0),
  area(),
  "boden"
  ],
````
_Kleine Erklärung zum Quellcode oben:_

_Für `=` wird eine anonyme Funktion aufgerufen, die für jeden Block neu ausgeführt wird. Diese definiert das Blockobjekt und das wird dann später dem Spiel hinzugefügt._

_Mit der Funktion `rect(width,height)` wird ein Rechteck von den angegeben Maßen erzeugt_

_Mit der Funktion `color(r,g,b)` wird die Farbe für den Block festgelegt._

_Mit der Funktion `area()` wird eine Kollisionsfläche erzeugt und für diese wird die Kollison aktiviert._

_Mit `"boden"` wird dem Block ein Tag gegeben. Diesen Tag kann man dann später zu Identifikation des Blocks nutzen._


### A - Schreibe für die erzeugte Spielfläche Definitionen für den Rand
Damit die Kollision mit den Rändern gut funktioniert, müssen die Blöcke hierfür definiert werden.

*Schreibe die Definition für den Rand des Spielfelds. Orientiere dich hierbei an dem Beispiel oben.*

