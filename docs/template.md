# Node-Package-Manager
##### Nikolai Kloß

---

# Agenda

1. Was ist NPM?
2. Bedienung
3. package.json

---

![](npm.png)
## 1. Was ist NPM?
- Node-Package-Manager ist ein Paketmanager für die JavaScript Umgebung NodeJS.
- Das npm-Repository ermöglicht das einfache Hinzufügen von Modulen ins eigene System.
- An Open-Source-Modulen gibt es weit über 350.000 Pakete.
- Ähnlich: Advance-Packaging-Tool (APT) für Debian GNU/Linux - Ubuntu.

---

![](npm_console.png)
## 2. Bedienung
- npm wird meist über ein Terminal bedient und bietet einen breiten Umfang an Befehlen.
- Beispiel: >_ $ npm install %Modulname

---
![](package.json.png)
## 3. package.json
- Die Basis für npm ist die "package.json" Datei, welche pro Projekt einmal existert.
- Enthält: Projektnamen, run scripts, Paketabhängigkeiten und deren Versionen

---

# Webpack
##### Nikolai Kloß

---

# Agenda

1. Was ist Webpack?
2. Loader
3. Webpack-Dev-Server
4. Konfiguration

---

![](Webpack_Overview.png)
## 1. Was ist Webpack ?
- Ein "Bundler", der aus einer Reihe von Ressourcen wie z.B. mehreren
JavaScript-Dateien/Modulen, eine große statische JavaScript-Datei(Asset) erzeugt.

---


![](Webpack_Loader.png)
## 2. Loader
- Pflegt eine bündelbare Ressource(SASS,JS,PNG..) ins Asset ein.

- Jede Ressourcenart braucht individuellen Umgang.

- Deshalb: existieren viele Loader für viele Ressourcenarten.

- Lassen sich einfach via. require() oder config einbinden.

---

## 3. Webpack-Dev-Server

- Webpack stellt die Möglichkeit, einen einfache Webserver zum Testen der Anwendung
zu verwenden.

- "Hot"-Mode: Server erkennt Quellcode Änderungen automatisch und übersetzt die
neuen Teile des Systems. Somit wird ein Neuladen der Anwendung im Browser unnötig.

---

## 4. Konfiguration
![](Config.png)
- Die Konfiguration von Webpack wird in "webpack.config.js"definiert.
- "entry" und "output" legen den Pfad zur Einstiegsdatei fest und wohin
Webpack Artefakte schreiben soll.
- "resolve.extensions" definiert die Dateiendungen die Webpack zum bauen
einbeziehen soll.
- "devtool" veranlasst Webpack, "Source Maps" für das erzeugte Bundle-File zu
erzeugen. Dies vereinfacht das Debuggen des Systems.
