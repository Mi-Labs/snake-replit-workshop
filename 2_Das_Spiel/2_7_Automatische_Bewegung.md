JS Workshop für Beginner - Summer Coding Festival THB 2022

## Automatische Bewegung

Damit das ganze Spiel jetzt zusammenkommt, brauchen wir eine automatische Bewegung der Schlange.
Es gibt hierfür verschiedene Ansätze, dies zu bewerkstelligen.

Hier stelle ich folgenden Ansatz vor:

1. Herausfinden in welche Richtung sich die Schlange bewegt
2. Einen Segment in Bewegungsrichtung hinzufügen
3. Den ältesten Teil der Schlange löschen

Mit diesem Vorgehen gibt es den typischen Snake-Look

### Voraussetzungen

Für die automatische Bewegung brauchen wir zwei weitere globale Variablen.

````
let bewegt_sich = false;
let aktuelle_richtung = richtung.RECHTS
````

Wenn das Spiel startet, soll ``bewegt_sich`` dann ``true`` werden und die aktuelle Bewegungsrichtung soll angepasst
werden

Für die Bewegungsrichtung nutzen wir eine Objekt mit Konstanten für die jeweiligen Richtungen. Die Richtungen ändern
sich ja nicht, nur die aktuelle Richtung ist eine der vier Richtungen.

Daher sieht das Richtungsobjekt so aus

````text
const richtung = {
  HOCH: "up",
  RUNTER: "down",
  RECHTS: "left",
  LINKS: "right"
}
````

Damit kann jetzt die aktuelle Richtung aus einem der vier Fälle angegeben werden.

<br>

### A - Ergänze die Inputs

Mit den neuen Voraussetzungen müssen wir jetzt die Inputs anpassen. Das ist der erste Schritt für das funktionierende
Spiel.

*Ergänze die Eingaben für den Input so, dass bei jedem Input nun die richtige Richtung auf die
Variable ``aktuelleRichtung`` zugewiesen wird.*

### Automatisierung

Spiele haben meistens einen Mechanismus, der bestimmte Funktionen jedes Frame abfragt. Das heißt, bei einer üblichen
Framerate von 60 Frames pro Sekunde werden diese Funktionen entsprechend auch 60x abgerufen.

Ein Anwendungsfall hierfür
wäre die Kollisionserkennung für den Spieler. Hier sollte immer überprüft werden, ob dieser von einer Kugel getroffen
wurde.

Mit der Funktion ``onUpdate(function(){...})`` stellt kaboom.js auch diese Funktionalität bereit.

Wir wollen aber nicht jedes Frame die Schlange bewegen, sondern nur alle x Frames oder Sekunden. Ansonsten wäre die
Bewegung sehr schnell und das Spiel nicht wirklich spielbar. Dafür nutzen wir folgenden Code:

````text
let verzoegerung = 0.2;
let timer = 0;

onUpdate(()=>{
    if(bewegt_sich == false){
        return; // Wenn sich die Schlange nicht bewegt, höre hier auf
    }
    timer +=  dt();  // Erhöhe den Timer um die Zeit für ein Frame
    
    if(timer < verzoegerung){
        return;     // Wenn der Timer nicht den Verzögerungswert erreicht hat - höre auf 
    }
    // Wenn der Timer den aktuellen Verzögerungswert erreicht hat, setze ihn auf 0
    timer = 0;
    
    // HIER WEITEREN CODE EINFÜGEN
}
````

<br>

### A - Erzeuge einen Codeblock, der anhand der aktuellen Richtung die Verschiebung des neuen Blocks errechnet.

Für diese Verschiebung brauchen wir zwei weitere Variablen.

- Verschiebung in X Richtung
- Verschiebung in Y Richtung

*Lege diese Variablen in der onUpdate-Methode an*

Für den Codeblock ist eine switch-case-Konstruktion am einfachsten. Diese ist eine elegantere Abfolge von
if-else-Abfragen.

````text
 // Variable um den aktuellen Wochentag zu speichern
let outputWochentag = "";

// Der aktuelle Wochentag wird als Zahl zwischen 1 und 7 gespeichtert
switch(wochentag){
    // Case 1 = if(wochentag == 1)
    case 1: 
        outputWochentag = "Montag";
        break; //
    // Case 2 = if(wochentag == 2)
    case 2:
        outputWochentag = "Montag";
        break;
    case 3:
        outputWochentag = "Mittwoch";
        break;  // Ist wichtig, weil sonst auch noch case 4 mit ausgeführt wird
    ...    
    // Der default case greift, wenn alle anderen Cases nicht genutzt werden
    default: 
        outputWochentag = "Sonntag";
        break;
}
return outputWochentag;
````

*Nutze nun die Bewegungsrichtungen von oben im Switch-Case und passe das Movement in die jeweilige Richtung an*

*Bei einer Bewegung nach unten sollte das X nicht bewegt werden und das Y um einen Block erhöht werden*

<br>

### A - Füge eine neues Segment der Schlange hinzu

Um den Schlangenkopf zu ermitteln, müssen wir uns weitere Array-Funktionen zunutze machen.

Den Schlangenkopf brauchen wir, damit wir den neuen Schlangenkopf an die neuste Position (Schlangenkopf + Berechnung von
oben) setzen können.

``let schlangenkopf = schlangenkoerper[schlangenkoerper.length - 1];``

Was in dem Snippet oben passiert ist Folgendes:

1. Deklarierung der Variable für den Schlangenkopf
2. Zugriff auf den Array ``schlangenkoerper[ ]``
3. Zugriff auf das letzte Element des Arrays ``schlangenkoerper``
4. Zuweisung des letzten Elements auf die Variable ``schlangenkopf``

Auf Array-Elemente kann man mit einem Index zugreifen.

Dieser nummeriert die Elemente von ``0 bis (n-1)``.

Bei 4 Elementen hat dann das letzte Element den Index ``3`` und das erste Element den Index ``0``.

Mit ``.length`` kann man sich die Anzahl an Elementen aus dem Array geben lassen.

Damit wir den letzten Eintrag im Array finden, nutzen wir jetzt die ``.length -1``. Dies gibt uns automatisch immer den
letzten Eintrag, egal wie viele Einträge der Array hat.

*Erstelle ein neues Schlangensegment und hänge es dem Schlangenkörper an.*

*Beachte hierbei, dass du die Position aus dem Schlangenkopf und der Verschiebung neu berechnen musst!*

*Falls du nicht mehr weißt wie das geht, schau nochmal bei ``2_2_Die_Schlange``*

<br>

### Entfernen des nun überflüssigen alten Schlangenparts
Für das oben gezeigte Ansatz müssen wir nun den ältesten Teil der Schlange entfernen. Dies lässt sich mit dem folgenden Code gut bewerkstelligen. Du musst hier dann nur die Variablen austauschen.
````text
// Wenn die Schlange größer sein sollte als erwartet :D
if(schlangenkoerper.length > schlangenlaenge){
    // Gibt das erste Element des Arrays aus und entfernt es aus dem Array
    let ende = schlangenkoerper.shift();
    // Entferne das Gameobjekt aus dem Spiel
    destroy(ende);
}
````
