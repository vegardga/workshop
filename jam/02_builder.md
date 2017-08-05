# 2 - Builder
Så bra, du har klart oppgave 1, og er nå klar for oppgave 2!

Denne oppgaven går ut på å bruke en knapp for å lage lyd. Hvis alt er koblet rett, så blir det spilt av en sang hver gang du trykker på knappen.

Lykke til!

## Klar?
Husk å koble Arduinoen fra Raspberry Pien før du går i gang med å koble egne kretser.

## Steg 01 - Koble

### 1/11
<img width="500" src="https://github.com/vegardga/workshop/blob/master/jam/images/02_01.png" alt="Arduino og koblingsbrett"/>

### 2/11
<img width="500" src="https://github.com/vegardga/workshop/blob/master/jam/images/02_02.png" alt="Knapp"/>

### 3/11
<img width="500" src="https://github.com/vegardga/workshop/blob/master/jam/images/02_03.png" alt="Motstand"/>

### 4/11
<img width="500" src="https://github.com/vegardga/workshop/blob/master/jam/images/02_04.png" alt="Jord"/>

### 5/11
<img width="500" src="https://github.com/vegardga/workshop/blob/master/jam/images/02_05.png" alt="Jord 2"/>

### 6/11
<img width="500" src="https://github.com/vegardga/workshop/blob/master/jam/images/02_06.png" alt="Power"/>

### 7/11
<img width="500" src="https://github.com/vegardga/workshop/blob/master/jam/images/02_07.png" alt="Power 2"/>

### 8/11
<img width="500" src="https://github.com/vegardga/workshop/blob/master/jam/images/02_08.png" alt="GPIO"/>

### 9/11
<img width="500" src="https://github.com/vegardga/workshop/blob/master/jam/images/02_09.png" alt="Piezo"/>

### 10/11
<img width="500" src="https://github.com/vegardga/workshop/blob/master/jam/images/02_10.png" alt="Piezo jord"/>

### 11/11
<img width="500" src="https://github.com/vegardga/workshop/blob/master/jam/images/02_11.png" alt="Piezo GPIO"/>

## Steg 02 - Kode
```javascript
var five = require("johnny-five");
var board = new five.Board();

board.on("ready", function() {
  var button = new five.Button(4);
  var piezo = new five.Piezo(6);

  button.on("down", function() {
    piezo.play({
      song: [
        ["E5", 1/4],
        [null, 1/4],
        ["E5", 1/4],
        [null, 3/4],
        ["E5", 1/4],
        [null, 3/4],
        ["C5", 1/4],
        [null, 1/4],
        ["E5", 1/4],
        [null, 3/4],
        ["G5", 1/4],
        [null, 7/4],
        ["G4", 1/4],
        [null, 7/4]
      ],
      tempo: 220
    });
  });
});
```

Det er viktig at det er store bokstaver der det står store bokstaver, og små bokstaver der det står små.

Husk å lagre filen! Enten gjennom menyen, `Fil` -> `Save`, eller trykk kombinasjonen `ctrl` + `s` på tastaturet.

## Steg 03 - Prøv!
Skriv følgende i terminalen:
```
node builder.js
```

Bruk kombinasjonen `ctrl` + `c` på tastaturet et par ganger for å stoppe kjøringen.

## Ferdig?
Kult, du har nå gjennomført oppgave 2 av 3!

Husk å koble fra hverandre kretsene før du går videre :)

## Problemer?
Bare å spørre, vi er her for å hjelpe til!
