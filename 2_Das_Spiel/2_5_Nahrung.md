JS Workshop für Beginner - Summer Coding Festival THB 2022

## Nahrung

Die Nahrung in Snake macht den Spielfortschritt aus. Mit jeder Nahrungsaufnahme wird die Schlange länger und das Spiel
wird schwieriger.

Für dieses Spielelement müssen wir einiges anpassen.

### Welche Regeln brauchen wir?

Für die Implementation von Nahrung brauchen wir einige Regeln:

1. Die Nahrung muss auf dem Spielfeld erreichbar sein
2. Es gibt immer nur ein Nahrungsstück
3. Bei Kontakt mit der Schlange passiert folgendes:
    1. Die Nahrung verschwindet und eine neue Nahrung erscheint
    2. Die Schlange wächst um 1 Segment

Aus diesen Regeln leitet sich verschiedene Aufgaben ab:

<br>

### A - Erzeugung von Nahrung

Für die Erzeugung der Nahrung müssen wir verschiedene Dinge beachten.

Die Nahrung sollte ein Gameobjekt sein. Dieses soll später auf der globalen Ebene gespeichert werden.

Die Position der Nahrung soll zufällig innerhalb des Spielfelds sein. Hierfür kann beispielsweise die
Funktion ``rand()`` genutzt werden. Diese erzeugt Zufallszahlen in einem gewählten Bereich.

Für unsere Zwecke können wir hier sogar die minmale und maximale Position eingeben und bekommen dann eine zufällige
Position. Dies könnte dann so aussehen:

``rand(vec2(1,1),vec2(5,5))``

*Erzeuge ein Nahrungsobjekt (siehe Game Objekte) und gebe diesem eine zufällige Position auf dem Spielfeld*

*Lagere die Erzeugung von Nahrung in eine Methode aus*

<br>

Hinweis: Das erzeugte GameObjekt könnte von der Größe der anderen Objekte abweichen. Mit ``scale(int)`` kann man die
Position auf die richtige Größe skalieren.

<br>

### A - Kollisionserkennung - Schlange/Nahrung

Für die Nahrungsaufnahme benötigen wir eine Kollisionserkennung.

Hierfür gibt es im Dokument ``Kollisionserkennung.md`` weitere Informationen und Aufgaben.

*Erstelle eine Kollisionserkennung für die Kollision Schlange/Nahrung*

<br>

### A - Wachstum der Schlange

Innerhalb der Kollisionserkennung aus der letzten Aufgabe erweiteren wir jetzt um das Wachstum der Schlange und die
Neuerzeugung der Nahrung.

*Sorge dafür, dass bei der Kollision die Schlange um 1 Segment wächst (Anpassen der Schlangenlänge) und neue Nahrung erzeugt wird*
