# workshop
Repo for workshops.

## Info
Tegninger/beskrivelse. Bla bla bla. Fylle ut noe greier her.

### Raspberry Pi
![alt text](https://www.raspberrypi.org/wp-content/uploads/2015/01/Pi2ModB1GB_-comp.jpeg "Raspberry Pi")

Tegninger/beskrivelse. Bla bla bla. Fylle ut noe greier her.

### Arduino
![alt text](https://www.arduino.cc/en/uploads/Products/Uno.jpg "Raspberry Pi")

Tegninger/beskrivelse. Bla bla bla. Fylle ut noe greier her.

### Johnny-Five
Tegninger/beskrivelse. Bla bla bla. Fylle ut noe greier her.

```javascript
var five = require("johnny-five");
var board = new five.Board();

board.on("ready", function() {
  var led = new five.Led(13);
  led.on();
});
```

# Oppgaver
For å komme i gang er det fint å kunne ta det gradvis gjennom oppgaver. Derfor er det lagt ved en del oppgaver under, som man kan ta i den rekkefølgen man selv ønsker. De er selvfølgelig lagt opp i en spesiell rekkefølge, som gradvis blir vanskeligere og vanskeligere. Men hvis man syns det går for sakte fremover, eller hvis man kan mye fra før av, så er det bare å hoppe over visse oppgaver og heller prøve seg på mer avanserte saker!

## 01 - Led
En beskrivelse om hvilke typer oppgaver dette er. Fylle ut med noe greier, og kanskje legge ved noen tegninger/beskrivelser for hva man trenger for å fulleføre oppgavene.

### La det bli lys!
For å lære seg noe nytt må man starte i det små, og så gradvis øke vanskelighetsgraden og skaffe seg mer kunnskap.
Derfor går den første oppgaven ut på å få lys i én enkelt LED.

> Oppgave: Skru på lyset i en LED.

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

### Blink-blink
Så bra, du fikk lys i LED-lyset! Men, det er jo litt kjedelig at det bare lyser hele dagen, så hva med å la LED-lyset blinke i stedet?
For å løse denne oppgaven må du altså få LED-lyset til å blinke hvert sekund. Av. På. Av. På. Av. På. Mennesker syns dette blir kjedelig etter hvert, men en datamaskin syns slike oppgaver er kjempegøy!

![alt text](https://camo.githubusercontent.com/2d2513641c0cd782d42d8aa261c3f41dd11ed5a4/687474703a2f2f6a6f686e6e792d666976652e696f2f696d672f6c65642d7363656e652d302e676966 "Blinkende LED-lys")

> Oppgave: Få LED-lyset til å blinke.

<details>
<summary>Klikk her for løsningsforslag</summary>
<p></p>
```javascript
var five = require("johnny-five");
var board = new five.Board();

board.on("ready", function() {
  var led = new five.Led(13);
  led.blink(1000);
});
```
<p></p>
</details>
