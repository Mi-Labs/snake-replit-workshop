JS Workshop für Beginner - Summer Coding Festival THB 2022

## Kollisionserkennung

In vielen Spielen wird eine Kollisionserkennung verwendet. 
Diese sorgt beispielsweise dafür, dass Treffer bei einem
Shooter richtig erkannt werden oder aber auch dass der Spieler nicht durch den Boden fällt.

Technisch funktioniert diese Erkennung folgendermaßen (stark vereinfacht):
1. Alle Objekte, bei denen eine Kollision erkannt werden soll, erhalten eine einfache unsichtbare Box um das Objekt
2. Während des Spiels wird abgefragt, ob ein Bestandteil eines Objekts innerhalb der Box des anderen Objekts liegt.
3. Wenn das der Fall ist -> Kollision | Ansonsten wird weiter geprüft.

In kaboom.js funktioniert das Ganze mit der Funktion ``onCollide(tag1,tag2,action())``.

Dies könnte dann beispielsweise in einem Shooter so aussehen:

````text
onCollide("player","bullet",(p,b)=>{
    // Reduziere das Leben nach einem Treffer um 1
    player.hurt(1);
    // Zerstöre die Pistolenkugel
    destroy(b);
})
````
Anmerkung zum Codebeispiel: Hier wird die Arrow-Funktion noch um zwei Parameter ergänzt ``p`` und ``b``. Mit diesen Parametern werden die beiden bei der Kollision beteiligten Objekte an die Funktion übergeben.

**Wichtig:** Für eine erfolgreiche Kollisionserkennung benötigen beide Objekte die Komponente ``area()``

<br>

### A - Schreibe eine Kollisionserkennung für die Kollision zwischen Schlange/Wand

Für das Spiel ist es wichtig, dass die Kollision zwischen Wand und Schlange erkannt wird. 
Dies ist dann ein GameOver und das Spiel soll zurückgesetzt werden.

*Schreibe eine Kollisionserkennung für die Kollision Schlange/Wand*

*Bei einer Kollision soll die Schlange auf ihre Anfangswerte zurückgesetzt werden*

*Eventuell musst du hierbei das Skript für die Schlangengeneration anpassen*

<br> 

### A - Weitere Kollisionen

Neben der Kollision Schlange/Wand gibt es ja auch die Kollision Schlange/Schlange. Diese tritt auf, wenn die Schlange sich selbst berührt.

*Schreibe für die Kollision Schlange/Schlange eine weitere Kollisionserkennung*

