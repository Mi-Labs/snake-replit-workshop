JS Workshop für Beginner - Summer Coding Festival THB 2022

## Gameobjekte

Computerspiele nutzen Gameobjekte um ihren Code verständlicher und modularer zu machen.
So ist beispielsweise jeder Baum, jeder Charakter oder auch jeder Spieler ein eigenes GameObjekt mit eigenen Funktionen und Eigenschaften

Gameobjekte können z.B. diese Eigenschaften besitzen
- 3D-Modell oder 2D-Grafik
- Kollisionserkennung
- Namen
- Physik-Eigenschaften (Gravitation, Beschleunigung)
- Position (Koordinatensystem)
- Rotation ()
- Funktion wie Laufen, Springen
- Speichermöglichkeiten für weitere Objekte

### Was bedeutet das für unser Snake-Spiel?

In Snake können wir viele Bestandteile in GameObjekte auslagern wie:
- Die Schlange
  - Hierbei kann die Schlange noch in autonome Segmente aufgeteilt werden
- Den Level
- Das Essen

In kaboom.js wird ein GameObject mit der Funktion ``add([...]);`` erzeugt.

````text
const player = add([
    pos(100,200),  // Position auf dem Spielfeld
    area(),        // Sorgt dafür, dass der Spieler eine Kollision hat
    health(8),     // Würde für eine Healthbar genutzt werden
    "player",      // Tag für die Zugehörigkeit
]); 
````
So sieht das verkürzte Beispiel aus der [Dokumentation](https://kaboomjs.com/#add) aus.
Wichtig hierbei ist, dass innerhalb der ``add()``-Funktion immer die `[]` Klammern zu nutzen und die einzelnen Komponenten mit Komma abzutrennen. 
