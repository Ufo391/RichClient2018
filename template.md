# ReactJS
##### Nikolai Kloß

---

# Agenda

1. Was ist React?
2. Motivation
1. Eine Bibliothek, kein Framework
4. Expression Interpolation
5. Implizite Rückgaben
6. Array Iterationen
7. Default Parameter
8. Klassendefinition
9. Vererbung
10. Module - Import/Export
11. Promises/Callbacks

---

## 1. Variablen Deklaration

``` js
let x = 1;

if (x === 1) {
  let x = 2;

  console.log(x); // Ausgabe: 2
}

console.log(x); // Ausgabe: 1
```

Durch das Statement "let" lassen sich Variablen in Ihrer Gültigkeit,
auf den Scope/Block, in dem sie sich bei ihrer Erzeugung befinden,
beschränken.

---

## 2. Contstant Deklaration

``` js
function abc(){

  const x = 42;

  x = 12; // Fehler: Der Wert der Variable kann nur gelesen werden!

  const x = 33; // Fehler: x wurde in diesem Scope bereits deklariert!

  if(true){

    const x = 99; // Erfolg: Es befindet sich nur ein "const x" in diesem Scope!


  }

}
```

Durch "const" besteht die Möglichkeit schreibgeschützte Variablen zu deklarieren.
Diese besitzen wie "let" Variablen nur eine begrenzte Gültigkeit innerhalb ihres
Scopes.

---

## 3. Arrow function Syntax

``` js
var foo = function(a){
  console.log(a);
}

foo(55);
```

``` js
var foo = a => {console.log(a);}

foo(55);
```

Die Arrow-Function-Syntax erlaubt eine gekürzte Schreibweise von
Funktionsausdrücken.

---

## 4. Expression Interpolation
``` js
var a = 5;
var b = 10;
console.log('Fifteen is ' + (a + b) + ' and\nnot ' + (2 * a + b) + '.');
// "Fifteen is 15 and
// not 20."
```

``` js
var a = 5;
var b = 10;
console.log(`Fifteen is ${a + b} and not ${2 * a + b}.`);
// "Fifteen is 15 and
// not 20."
```
"Expression interpolation" erlaubt eine übersichtlichere Schreibweise von Variablen
innerhalb einer Zeichenkette.

---

## 5. Implizite Rückgaben

``` js
function func(a, b, c) { return a + b + c; }
```

``` js
let func = (a, b, c) => a + b + c;
```

Erlaubt bei simplen Funktionen eine Kurzschreibweise, da der Funktionsblock
und das Schlüsselwort "return" wegfallen.

---

## 6. Array Iterationen

``` js
var arr = ['a', 'b', 'c'];
for (var i = 0; i < arr.length; i++) {
    console.log(arr[i]);
}
```

``` js
var arr = ['a', 'b', 'c'];
for (let i of arr) {
    console.log(i);
}
```

ES6 verfügt nun die Möglichkeit "foreach" ähnliche Schleifen zu implementieren,
wie sie aus anderen Hochsprachen bekannt sind. Dies erlaubt eine übersichtlichere
Schreibweise der Schleife.

---

## 7. Default Parameter

``` js
let add = (a, b = 2) => {
    return a + b;
}

add(10);   // returns 12
add(10, 5) // returns 15
```
Die Funktion "add" verfügt über den Standardparameter "b".
Sofern die Funktion "add" ohne Parameter aufgerufen wird, greift die
in der Funktionsparameterliste vordefinierte Anweisung "b = 2".

---

## 8. Klassendefinition
ES5:
``` js
function Func(a, b) {
    this.a = a;
    this.b = b;
}

Func.prototype.getSum = function() {
    return this.a + this.b;
}

var x = new Func(3, 4);
x.getSum(); // returns 7
```

---
## 8. Klassendefinition

ES6:
``` js
class Func {
    constructor(a, b) {
        this.a = a;
        this.b = b;
    }

    getSum() {
        return this.a + this.b;
    }
}

let x = new Func(3, 4);
x.getSum(); // returns 7
```

In ES6 sind die Schlüsselwörter "class" und "constructor" hinzugekommen, dagegen wird "prototype" nun nicht mehr benötigt. In ES6 stehen alle Klassenelemente
, wie Funktionen und Attribute, innerhalb eines Blockes.

---

## 9. Vererbung

ES5:
``` js
function Inheritance(a, b, c) {
    Func.call(this, a, b);

    this.c = c;
}

Inheritance.prototype = Object.create(Func.prototype);
Inheritance.prototype.getProduct = function() {
    return this.a * this.b * this.c;
}

var y = new Inheritance(3, 4, 5);
```
---
## 9. Vererbung
ES6:
``` js
class Inheritance extends Func {
    constructor(a, b, c) {
        super(a, b);

        this.c = c;
    }

    getProduct() {
        return this.a * this.b * this.c;
    }
}

let y = new Inheritance(3, 4, 5);
```
Vererbung wurde durch die Schlüsselwörter "extends" und "super" (Basisklassenkonstruktoraufruf) sehr vereinfacht.

---

## 10. Module - Import/Export

HTML:
``` html
<script src="export.js"></script>
<script type="module" src="import.js"></script>
```

export.js:
``` js
let func = a => a + a;
let obj = {};
let x = 0;

export { func, obj, x };
```

import.js
``` js
import { func, obj, x } from './export.js';

console.log(func(3), obj, x);
```

Es besteht nun die Möglichkeit, Funktionen eines Skripts zu einem Modul
zusammenzufassen und diese dann in anderen Skripten wieder verfügbar
zu machen.

---
## 11.Promises/Callbacks

ES5 Callback:
``` js
function doSecond() {
    console.log('Do second.');
}

function doFirst(callback) {
    setTimeout(function() {
        console.log('Do first.');

        callback();
    }, 500);
}

doFirst(doSecond);
```
---
## 11.Promises/Callbacks
ES6 Promise:
``` js
let doSecond = () => {
    console.log('Do second.');
}

let doFirst = new Promise((resolve, reject) => {
    setTimeout(() => {
        console.log('Do first.');

        resolve();
    }, 500);
});

doFirst.then(doSecond);
```

Promises erhalten die Übersichtlichkeit bei Verkettungen von asynchronen
Funktionsaufrufen, welche bei klassischen Callbacks meist leidet.

---

# Ende :)
