JS Workshop für Beginner - Summer Coding Festival THB 2022

## Texturen

Texturen sind ein wichtiger Bestandteil von jedem Spiel. Sie sorgen dafür, dass Objekte ein Muster oder eine Grafik
haben.

Ohne Texturen wären alle Objekte nur einfarbig oder nur grau. 
Zudem lasse sich so in 3D-Spielen viel Rechenleistung einsparen, da man beispielsweise bei Bäumen alle Blätter durch 2D-Grafiken ersetzen kann.


Bisher ist unser Snake Spiel auch nur farbig und optisch noch nicht super ansprechend. Das können wir aber mit Texturen ändern.

### Texturen laden

Damit wir in kaboom.js Texturen (oder auch Sprites) nutzen können, müssen wir diese erstmal laden.

Mit folgendem Befehl kannst du eine Grastextur laden und später dann mit ``sprite("gras")`` im Spiel nutzen.


``loadSprite("gras","sprites/gras.jpg")``

Hierfür muss aber die entsprechende Datei in Replit hochgeladen werden.

Auf der linken Seite sollte sich ein Menü befinden, in dem ein Unterpunkt ``Sprites`` vorhanden ist.
Dort sollte bean (grüner Kreis mit Gesicht) bereits vorhanden sein.

Bei diesem Unterpunkt gibt es mehrere Möglichkeiten, um neue Sprites hinzuzufügen.

1. Die Library von replit (Wolkensymbol)
2. Eigener Upload von Sprites (Upload-Symbol)
3. Zeichnen von Sprites (+ Symbol)

<br>
 
### Einbinden von Sprites
Innerhalb des Spiels werden die Sprites in der Regel in den GameObjekte verankert.
Hierfür bekommen diese die Komponente ``sprite()``.

Diese würde dann etwa so eingebunden. Der Parameter entspricht hierbei dem ersten Parameter, den du beim Laden angibst.
````js
[
    sprite("gras"),
    ...
]
````

<br>

### A - Ersetze die Blöcke durch Sprites
Um das Snake-Spiel schöner zu gestalten, macht es Sinn, die bisherigen farbigen Blöcke durch Sprites zu ersetzen.


*Ersetze alle Blöcke durch Sprites*

Für den Hintergrund kann folgender Code genutzt werden
````js
layers([
    "background",
    "game"
], "game");

add([
    sprite("background"),
    layer("background")
]);
````
