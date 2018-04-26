# ReactJS
##### Nikolai Kloß

---

# Agenda

1. Was ist React?
2. Motivation
3. Eine Bibliothek, kein Framework
4. Kompoentenarchitektur
5. JSX
6. State
7. Prop
8. Virtueller DOM

---

## 1. Was ist React?

Eine modulare Komponentenbasierte JavaScript-Bibliothek zur Erstellung von Benutzeroberflächen.
Entwickelt von Facebook, ist es trotz des neuartigen Ansatzes, aufgrund der hohen Renderingperformanz in der JS-Frontendentwicklung weit verbreitet und beliebt.
<p/>Es bildet typischerweise die Basis für Single-Page-Applications

---

## 2. Motivation

- Frontendcode verständlicher und besser wartbar machen.
- Facebook: Bugs wie unsychrone Zähler und Nachrichten traten immer wieder auf und waren vorallem bei sehr komplexen Zusammenhängen ein großes undurchsichtiges Problem.

---

## 3. Eine Bibliothek, kein Framework

- Ein flexibles Werkzeug, welches erlaubt Anwendungen in der Sprache ihrer
eigenen Entwicklungsumgebung - und nicht in der Sprache des Frameworks - zu erstellen.
- Gibt keine Grundstruktur vor und lässt sich deshalb einfach in bestehende Codebasen integrieren.

---

## 4. Kompoentenarchitektur

![Diagramm](react.png)
- Zentraler und einziger Baustein von React sind Komponenten welche unteinander
kommunizieren.

---

## 4. Kompoentenarchitektur

- Folgt NICHT dem MVC-Modellen
- Logik für Interaktion und Darstellung werden innerhalb eines Objekts gebündelt
