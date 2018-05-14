# Software Qualität
##### Nikolai Kloß

---

# Agenda

1. Testing Functional JavaScript
2. Mocha
3. Chai
4. SinonJS
5. Jest

---

## 1. Testing Functional JavaScript

### Warum testen?
* Zeigen ob Code im System das tut was entsprechend erwartet wird
* Änderungen im Code müssen zu dem im Test definierten Ergebnis führen,
ansonsten --> Fehler im Code.


### Arten:
* Unit-Tests:
  * Testet die Funktionalität eines bestimmten Teils im Code
* Integrationstests:
  * Prüft den Datenfluss und die Kommunikation unter den Komponenten
* Funktionale-Tests:
  * Betrachtet das Verhalten des gesamten Systems

### Vorteil:
* Einfach zu testen, weil jede Eingabe eine feste Ausgabe erzeugt
* Es müssen kein Kontext, Zustand oder interfunktionalen Abhängigkeiten
beatrachtet werden

---

## 2. Mocha

### Mocha?
* Mocha ist ein "Test Runner" der sich via npm einfach einbinden lässt
  * Tests sind nicht in Mocha geschrieben
  * Mocha führt die Tests nur aus

---

## 3. Chai

### Chai?
* Chai ist eine Assertion Bibliothek
* Es bietet gegenüber der "Assert" Bibliothek eine bessere lesbarkeit

---

## 4. SinonJS

### SinonJS?
* Bietet Spies, Stubs und Mocks zum Testen des Systems an.

### Spies:
* Ermöglicht "fake" Funktionen zu schreiben
* Ziel ist das Aufzeigen der Aufrufe der Funktion
* Kann auch bestehende Funktionen beobachten

### Stubs:
* Funktionen lassen sich einfach durch andere Funktionen auswechseln
* So lässt sich eine bestimmte Funktion auch in einem anderen Kontext testen

### Mocks:
* "Fake" Methoden mit vorprogrammierten Verhalten und vorprogrammierten erwarteten Ergebnissen
* Nützlich um ein noch nicht existierendes Teilsystem zu Simulieren
  * Bsp.: Logik zu einer Datenbank Applikation implementieren, ohne, dass die DB schon existiert --> Datenbankeinträge werden gemockt

---

## 5. Jest

### Jest?
* Ein Test-Runner, welcher expectations, spies, mocks und Snapshot-Tests beinhaltet

### Snapshot-Test?

* Vorraussetzung: funktionierende zu testende Komponente
* Wird nicht während der Entwicklungszeit der Komponente erzeugt
* Ablauf:
  * 1: Ausführung der funktionierenden Komponente & speichern von dessen Zustand (Snapshot)
  * 2: Jede weitere Ausführung wird mit dem Snapshot verglichen
  * 3: Bei Unterschieden --> Fehler im System erkannt
