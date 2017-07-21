# 4 - Maker

## Klar?
Husk å koble Arduinoen fra Raspberry Pien før du går i gang med å koble egne kretser.

## Steg 01 - Koble
![alt text](https://github.com/vegardga/workshop/blob/master/jam/images/03_01.png "Arduino og koblingsbrett")

## Steg 02 - Kode
```javascript
var five = require("johnny-five");
var board = new five.Board();

board.on("ready", function() {

});
```

## Steg 03 - Prøv!
Skriv følgende i kommandolinja:
```
node maker.js
```

Bruk kombinasjonen `ctrl` + `c` på tastaturet et par ganger for å stoppe kjøringen.

## Ferdig?
Skriv følgende i kommandolinja:
```
./done.sh
```

Husk å koble fra hverandre kretsene før du går videre :)
