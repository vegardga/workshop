# 1 - Creator
Velkommen!

Håper du er klar for å koble og kode :) Den første oppgaven går ut på å få et LED-lys til å blinke.

## Klar?
Husk å koble Arduinoen fra Raspberry Pien før du går i gang med å koble egne kretser.

## Steg 01 - Koble
Følg stegen under:

### 1/5
<img width="500" src="https://github.com/vegardga/workshop/blob/master/jam/images/01_01.png" alt="Arduino og koblingsbrett"/>

### 2/5
<img width="500" src="https://github.com/vegardga/workshop/blob/master/jam/images/01_02.png" alt="LED"/>

### 3/5
<img width="500" src="https://github.com/vegardga/workshop/blob/master/jam/images/01_03.png" alt="Motstand"/>

### 4/5
<img width="500" src="https://github.com/vegardga/workshop/blob/master/jam/images/01_04.png" alt="Jord"/>

### 5/5
<img width="500" src="https://github.com/vegardga/workshop/blob/master/jam/images/01_05.png" alt="GPIO"/>

## Steg 02 - Kode
Etter at koblingene er gjort er det tid for å kode litt!

Skriv følgende i teksteditoren:
```javascript
var five = require("johnny-five");
var board = new five.Board();

board.on("ready", function() {
  var led = new five.Led(12);
  led.blink(500);
});
```

Det er viktig at det er store bokstaver der det står store bokstaver, og små bokstaver der det står små.

Husk å lagre filen! Enten gjennom menyen, `Fil` -> `Save`, eller trykk kombinasjonen `ctrl` + `s` på tastaturet.

## Steg 03 - Prøv!
Skriv følgende i terminalen:
```
node creator.js
```

Bruk kombinasjonen `ctrl` + `c` på tastaturet et par ganger for å stoppe kjøringen.

## Ferdig?
Kult, du har nå gjennomført oppgave 1 av 3!

Husk å koble fra hverandre kretsene før du går videre :)

## Problemer?
Bare å spørre, vi er her for å hjelpe til!
