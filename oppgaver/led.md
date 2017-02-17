# Oppgaver - LED
En beskrivelse om hvilke typer oppgaver dette er. Fylle ut med noe greier, og kanskje legge ved noen tegninger/beskrivelser for hva man trenger for å fulleføre oppgavene.

## Oppgave 1 - La det bli lys!
For å lære seg noe nytt må man starte i det små, og så gradvis øke vanskelighetsgraden og skaffe seg mer kunnskap.
Derfor går den første oppgaven ut på å få lys i én enkelt LED.

> **Oppgave:**
>
> Skru på lyset i en LED.

<details>
<summary>Klikk her for løsningsforslag</summary>
```javascript
var five = require("johnny-five");
var board = new five.Board();

board.on("ready", function() {
  var led = new five.Led(13);
  led.on();
});
```
</details>

## Oppgave 2 - Blink-blink
Så bra, du fikk lys i LED-lyset! Men, det er jo litt kjedelig at det bare lyser hele dagen, så hva med å la LED-lyset blinke i stedet?
For å løse denne oppgaven må du altså få LED-lyset til å blinke hvert sekund. Av. På. Av. På. Av. På. Mennesker syns dette blir kjedelig etter hvert, men en datamaskin syns slike oppgaver er kjempegøy!

![alt text](https://camo.githubusercontent.com/2d2513641c0cd782d42d8aa261c3f41dd11ed5a4/687474703a2f2f6a6f686e6e792d666976652e696f2f696d672f6c65642d7363656e652d302e676966 "Blinkende LED-lys")

> Oppgave: Få LED-lyset til å blinke.

<details>
<summary>Klikk her for løsningsforslag</summary>
```javascript
var five = require("johnny-five");
var board = new five.Board();

board.on("ready", function() {
  var led = new five.Led(13);
  led.blink(1000);
});
```
</details>
