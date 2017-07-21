# Creator

## Klar?
Husk å koble Arduinoen fra Raspberry Pien før du går i gang med å koble egne kretser.

## Steg 01 - Koble
Følg stegen under:
![alt text](https://github.com/vegardga/workshop/blob/master/jam/images/01_01.png "Arduino og koblingsbrett")

![alt text](https://github.com/vegardga/workshop/blob/master/jam/images/01_02.png "LED")

![alt text](https://github.com/vegardga/workshop/blob/master/jam/images/01_03.png "Motstand")

![alt text](https://github.com/vegardga/workshop/blob/master/jam/images/01_04.png "Jord")

![alt text](https://github.com/vegardga/workshop/blob/master/jam/images/01_05.png "GPIO")

## Steg 02 - Kode
Skriv følgende i teksteditoren:
```javascript
var five = require("johnny-five");
var board = new five.Board();

board.on("ready", function() {
  var led = new five.Led(12);
  led.blink(500);
});
```

## Steg 03 - Prøv!
Skriv følgende i kommandolinja:
```
node creator.js
```

## Ferdig?
Skriv følgende i kommandolinja:
```
./done.sh
```

Husk å koble fra hverandre kretsene før du går videre :)
