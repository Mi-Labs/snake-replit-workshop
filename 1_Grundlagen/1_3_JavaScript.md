JS Workshop für Beginner - Summer Coding Festival THB 2022

## JavaScript

### Wofür brauche ich JavaScript (JS)?
JavaScript ist eine Skriptsprache, die hauptsächlich für die Interaktivität von Webseiten eingesetzt wird.

Wenn man mit einem Mausklick die Webseite verändern kann oder eine Werbeanzeige auftaucht, in den meisten Fällen steckt JavaScript dahinter.

JavaScript wird direkt im Browser ausgeführt und benötigt meist ein HTML-Dokument zum Laden. In der replit-Umgebung ist schon dafür gesorgt, sodass du nur noch den Code ausführen musst.

### Variablen 
Variablen sind Codebestandteile, die einen bestimmten Inhalt für eine bestimmte Zeit speichern.

**Was können Variablen speichern?**
- Zahlen (Int/Float/Double)
- Text (String)
- Buchstaben (Char)
- Wahr / Falsch (Boolean)
- Objekte (Können alles von den oberen Typen enthalten)

Jede Variable kann aber nur Daten von einem Typ zu einem Moment speichern - Eine String-Variable kann daher eigentlich immmer nur Text enthalten. In vielen Programmiersprachen kann eine Variable immer nur einen vordefinierten Typ enthalten, also eine String-Variable kann immer nur einen String enthalten.

Bei JavaScript ist das etwas anders. Hier können Variablen während des Programm-Ablaufs mit unterschiedlichen Inhalten bespielt werden. Im einen Moment enthält die Variable Text, im nächsten Moment eine Zahl. Das ist tendenziell möglich, aber nicht sinnvoll :D

<br>

**Wie lange können Variablen Inhalte speichern** 
- Für die Ausführung des Programms
- Für die Ausführung der Methode/Funktion
- Für die Schleife/Kontrollstruktur

Der Inhalt der Variablen wird unterschiedlich lange im Programm gespeichert, je nachdem wo und wie die Variable deklariert wird.

Eine dauerhafte Speicherung ist aber auf diesem Weg nicht möglich. Spätestens wenn du das Programm beendest, verfallen die Inhalte. Um beispielsweise Spielstände dauerhaft zu speichern ist zusätzliche Programmierung notwendig.

<br>

**Wie schreibe ich jetzt Variablen in JS**

In JS werden Variablen folgendermaßen deklariert:

````js
Variante 1:
let meineVariable = 23;

Variante 2 (nicht veränderbar):
const meineKonstante = 42;

Variante 3:
var meineVariable2 = 24;

Variante 4 (implizite globale Variable):
meineVariable3 = 25;
````
Im Rahmen dieses Workshops werden wir mit ``let`` sowie `const` arbeiten. 

### Zuweisungen oder Wie lese ich JS
Zuweisungen sind die Zeilen mit `=`

Hierbei wird ein Wert auf eine Variable zugewiesen <- Daher auch der Name.
Die Lese-Reihenfolge ist hierbei wichtig.
Der Wert auf der rechten Seite des Gleichzeichens wird auf die Variable auf der linken Seite zugewiesen.

``let meineVariable = 23;`` dient hierzu als Beispiel.

Was passiert hier?
- Die Variable meineVariable wird deklariert ``let meineVariable``
- Der Wert 23 wird mit `=` auf die Variable geschrieben
- Das `;` beendet die Anweisung

### Methoden / Funktionen
In JS können wir häufig genutzten Code in Methoden/Funktionen auslagern.

Eine Funktion kann beispielsweise so aussehen:
````js
function dasIstEineTestfunktion(parameter1){
    // Hier passiert etwas Spannedes
    let neueZahl = 42 + parameter1;
    return neueZahl;
}
````

Diese Funktion zerlegen wir jetzt in ihre Bestandteile:
- ``function`` ist das Keyword um eine Funktion zu signalisieren
- ``dasIstEineTestfunktion`` ist der Name der Funktion
- ``(parameter1)`` ist der Parameter für die Funktion. Hiermit ist es möglich, Werte von außerhalb der Funktion mit in die Funktion zu übergeben. In diesem Fall wäre es eine Zahl.
- ``return`` signalisiert, dass die Funktion mit dieser Anweisung beendet wird. Der Wert nach dem return kann auf eine Variable zugewiesen werden.

Die generelle Struktur sieht also so aus:
`````js
function name(parameter){
    ///...
    return; //Muss nicht zwangsläufig hier stehen, aber bei vielen Funktionen macht es Sinn
}
`````

Diese Funktion könnte man beispielsweise so einsetzen:
````js
let zahl = 0;
// Ausführen der Funktion mit dem Parameter 8
zahl = dasIstEineTestfunktion(8);
// Die Zahl sollte jetzt 50 sein
console.log(zahl);
````

### Sammlungen & Objekte

Mit Objekten können verschiedene Variablen und Funktionen gebündelt an eim Punkt gepackt werden.
Wir werden Objekte vor allem als GameObjekte kennenlernen - hier erfüllen sie dann unterschiedlichste Funktionen. 

Um beispielsweise alle Daten zu einem Spieler zu speichern, kann man beispielsweise ein Objekt anlegen.

`````js
const spieler = {
    age: 20,
    health: 100,
    money: 10000,
    nickname: "Micha"
}
`````
Diese Objekt kann ich jetzt im Spiel besser benutzen und hab nicht vier weitere Variablen, die ich für jeden Spieler neu anlegen muss.

In einem Multiplayer-Spiel kann man das Objekt jetzt beispielsweise in eine Sammlung packen. Ein gutes Beispiel hierfür wären alle Spieler in diesem Match.

In JS gibt es verschiedene Möglichkeiten für eine Sammlung. Wir werden uns aber nur einen Array anschauen.

<br>

**Array**

Ein Array ist eine Sammlung, die durch einen Index bedient wird, d.h. jeder Eintrag ist nummeriert. 

````js
let neuerArray = [];
neuerArray[0] = 9;
neuerArray[1] = 18;
````
So sieht eine Array-Erstellung mit zwei Elementen aus. Die Nummerierung startet immer bei 0.

Mit ``neuerArray.length`` lässt sich die Anzahl an Elementen in dem Array herausfinden.












