---
author: Rocco De Patto
title: Javascript Base <br> Sinervis
date: Novembre 7, 2017
---
# Metodi/Funzioni
## Valori di ritorno
Mostrare dialoghi, o scrivere a schermo sono `side effect`.
Molte funzioni sono utili proprio per questo, ma le funzioni
possono produrre anche **valori**.  
Quando una funzione produce un valore, questo di chiama
__valore di ritorno__ e si dice che la funzione __ritorna__
quel dato valore.  

## Valori di ritorno
Ad esempio la funzione `Math.max` ritorna il numero massimo
tra gli __argomenti__ che gli vengono passati tra parentesi:

```javascript
var etaMassima = Math.max(20, 25, 26);
alert(etaMassima);
```

## Valori di ritorno // stringhe

```javascript
var nomeUtente = "Mario";

var nomeUtenteMaiuscolo = nomeUtente.toUpperCase();
```
la funzione toUpperCase() __ritorna__ la stringa nomeUtente in maiuscolo.

## Valori di ritorno // stringhe

```javascript
var giornoSettimana = 'Lunedì';
var abbreviato = giornoSettimana.substr(0, 3);
```
[substr](https://www.w3schools.com/jsref/jsref_substr.asp) __ritorna__ una parte di stringa.

## Funzioni

```javascript
function ...
```

# DOM in JS
## La base
```javascript
var barraDiNavigazione = document.getElementById('id');
barraDiNavigazione.style.color = "red";
```

## Eventi nel DOM
```html
<button onclick="faiQuesto()"></a>
```