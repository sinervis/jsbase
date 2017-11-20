---
author: Rocco De Patto
title: Javascript Base <br> Sinervis
date: Novembre 21, 2017
---
# Oggetti
## Oggetti
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
Abbiamo visto finora dei tipi di dati semplici (numeri, stringhe)
```javascript
var numeroStudenti = 4;
var nomeDocente = 'Rocco';
```
e anche gli array (liste di variabili).
```javascript
var lezioni = ['Introduzione', 'Variabili, condizioni, cicli', 'Funzioni'];
```

In javascript esiste un'altra struttura dati molto comoda, gli **oggetti**.


## Oggetti
Gli oggetti possono contenere delle proprietà e dei metodi.
Ad esempio possiamo creare un oggetto di nome studente con le proprietà
età, nome, cognome:

```javascript
var studente = {
	nome: "Mario",
	cognome: "Rossi",
	eta: 28
}
```

## Oggetti
Per accedere ad una proprietà di oggetto possiamo usare due
notazioni diverse:

```javascript
alert( studente.nome );
alert( studente['nome'] );
```
con il punto o tra parentesi graffe.


## Oggetti
Possiamo aggiungere a piacimento nuove proprietà ad un oggetto:

```javascript
studente.promosso = true;
```

## Oggetti
Le proprietà degli oggetti possono contenere qualsiasi tipo di variabile, anche altri oggetti:

```javascript
var studente = {
	nome: 'Mario',
	cognome: 'Rossi',
	indirizzo: {
		via: 'Corso Francia',
		numero: '197',
		cap: '10100',
		citta: 'Torino'
	}
}

alert(studente.indirizzo.cap)

```

## Oggetti
Una proprietà degli oggetti puo' contenere anche una funzione:

```javascript
var studente = {
	nome: 'Mario',
	cognome: 'Rossi',
	nomeCompleto: function () {
		return 'Mario Rossi';
	}
}

alert(studente.nomeCompleto());
```

## Oggetti
Per fare riferimento alle proprietà dell'oggetto dall'interno di una sua funzione si utilizza la parola chiave `this`:

```javascript
var studente = {
	nome: 'Mario',
	cognome: 'Rossi',
	nomeCompleto: function () {
		return this.nome + ' ' + this.cognome;
	}
}

studente.nome = 'Paperino';
alert(studente.nomeCompleto())
```

# Esempio
## TODO
Abbiamo bisogno di salvare una lista di `task`, che dovranno avere
un titolo, un livello di priorita' da 1 a 3 e se sono completati o meno.

## Task
```javascript
var task = {
	titolo: 'Comprare il pane',
	priorita: 1,
	fatto: false
}
```

## Tasks

```javascript
var coseDaFare = [
	{ titolo: 'Comprare il pane', priorita: 1, fatto: false },
	{ titolo: 'Fare benzina', priorita: 2, fatto: false },
	{ titolo: 'Fare le slides', priorita: 3, fatto: true }
];
```

## Aggiungere un task
Come si aggiunge un elemento ad un array?
C'e' il metodo `push`:

```javascript
var listaDellaSpesa = ['pane', 'latte'];
listaDellaSpesa.push('uova');
```
Come riempio le proprieta' del nuovo task?


## Aggiungere un task
- Lo creo:
```javascript
var task = { titolo: "prendo da un input", priorita: 1, fatto: false };
```
- Lo aggiungo alla lista:
```javascript
coseDaFare.push(task);
```

## Mostare la lista
Dove lo mostro? Una lista, perfetto un `<ul> <li>...`

Per ogni task ripeto:

- Mostro il titolo
- Imposto il colore secondo la priorita'
- Se e' fatto, linea in mezzo e in grigio