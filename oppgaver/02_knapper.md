# Oppgaver - Knapper
En beskrivelse om hvilke typer oppgaver dette er. Fylle ut med noe greier, og kanskje legge ved noen tegninger/beskrivelser for hva man trenger for å fulleføre oppgavene.

## Oppgave 1 - Trykk. Logg.
Beskrivelse av oppgaven.

> Oppgave: Logg teksten "Tøft, jeg kan trykke på en knapp" når du trykker på knappen.

<details>
<summary>Klikk her for løsningsforslag</summary>
```javascript
var five = require("johnny-five");
var board = new five.Board();

board.on("ready", function() {
  var button = new five.Button(2);

  button.on("press", function() {
    console.log( "Button pressed" );
  });
});
```
</details>

## Oppgave 2 - Skill mellom tilstandene til knappen
Beskrivelse av oppgaven.

> Oppgave: Logg ulike meldinger basert på om knappen er trykt ned, holdes nede eller slippes opp.

<details>
<summary>Klikk her for løsningsforslag</summary>
```javascript
var five = require("johnny-five");
var board = new five.Board();

board.on("ready", function() {
  var button = new five.Button(2);

  button.on("hold", function() {
    console.log( "Button held" );
  });

  button.on("press", function() {
    console.log( "Button pressed" );
  });

  button.on("release", function() {
    console.log( "Button released" );
  });
});
```
</details>

## Oppgave 3 - Skru på lyset
En beskrivelse av oppgaven

> Oppgave: Skru på LED-lyset når du trykker på knappen.

<details>
<summary>Klikk her for løsningsforslag</summary>
```javascript
var five = require("johnny-five");
var board = new five.Board();

board.on("ready", function() {
  var led = new five.Led(13);
  var button = new five.Button(2);
  button.on("press", function() {
    led.on();
  });
});
```
</details>
