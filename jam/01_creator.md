# Creator

## Steg 01 - Koble
![alt text](https://github.com/vegardga/workshop/blob/master/jam/images/01_01.png "Arduino og koblingsbrett")

![alt text](https://github.com/vegardga/workshop/blob/master/jam/images/01_02.png "LED")

![alt text](https://github.com/vegardga/workshop/blob/master/jam/images/01_03.png "Motstand")

![alt text](https://github.com/vegardga/workshop/blob/master/jam/images/01_04.png "Jord")

![alt text](https://github.com/vegardga/workshop/blob/master/jam/images/01_05.png "GPIO")

## Steg 02 - Kode
```javascript
var five = require("johnny-five");
var board = new five.Board();

board.on("ready", function() {
  var led = new five.Led(12);
  led.blink(500);
});
```

## Steg 03 - Prøv!
terminal og kjør
