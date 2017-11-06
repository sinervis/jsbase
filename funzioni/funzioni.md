---
author: Rocco De Patto
title: Javascript Base <br> Sinervis
date: Novembre 7, 2017
---
# Metodi/Funzioni
## Funzioni
<style>
	div.sourceCode {
		font-size: 1.3em;
	}

	.reveal {
		font-size: 27px;
		color: #2d373a;
	}

	.reveal p {
		text-align: left;
	}

	.reveal blockquote {
		text-align: left;
		padding-left: 45px;
		font-size: 1.3em;
		border-left: 5px solid;
		background: #eee;
	}

	body {
		background: white;
	}

	.container {
		width: 100%;
		box-sizing: border-box;
	}

	.container textarea {
		width: 50%;
	}

	.container .output {
		width: 50%;
	}

	.reveal pre.sourceCode {
		width: 100%;
		box-shadow: none;
		border: 1px solid #bbb;
		border-left: 5px solid #bbb;
		background: #f5f5f5;
		padding: 5px;
		margin: 0px;
		box-sizing: border-box;
	}

	li > code,
	p  > code {
		border-radius: 6px;
		color: black;
		background: #f4f4f4;
		padding: 0px 4px !important;
	}
</style>
In javascript è possibile creare delle funzioni per contenere
del codice da poter richiamare a nostro piacimento da altre parti.

Per dichiarare una funzione si usa la seguente sintassi:

```javascript
function nomeFunzione () {

}
```

## Funzioni
Vogliamo mostrare un popup di errore ogni volta che l'utente
sbaglia qualcosa nella compilazione di un form.

Possiamo immaginare che questa operazione serva in piu' posti
nel nostro codice (lunghezza minima password, mail corretta.)

```javascript
function mostraErrore () {
	alert("Form non valido!");
}

// per richiamarla:
mostraErrore();
```

## Funzioni
Vogliamo poter mostrare all'utente anche quale campo non è
valido. Per fortuna nelle funzioni possiamo specificare degli argomenti:

```javascript
function mostraErrore (campoNonValido) {
	alert("Form non valido! Controlla il campo: " + campoNonValido);
}

// per richiamarla
mostraErrore("password");
```

## Funzioni
Possiamo utilizzare quanti parametri vogliamo:

```javascript
function mostraErrore (campoNonValido, tipoErrore) {
	alert("Form non valido: " + campoNonValido + " " + tipoErrore);
}

// per richiamarla:
mostraErrore("password", "troppo corta");
```

## Funzioni
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