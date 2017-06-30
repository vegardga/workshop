# Creator

## Steg 01 - Utstyr
Finn fram følgende utstyr:
- 1 stk LED
- 1 stk motstand
- 1 stk svart ledning
- 1 stk rød ledning

## Steg 02 - Koblinger
![alt text](https://github.com/vegardga/workshop/blob/master/jam/images/01_01.png "Arduino og koblingsbrett")

![alt text](https://github.com/vegardga/workshop/blob/master/jam/images/01_02.png "LED")

![alt text](https://github.com/vegardga/workshop/blob/master/jam/images/01_03.png "Motstand")

![alt text](https://github.com/vegardga/workshop/blob/master/jam/images/01_04.png "Jord")

![alt text](https://github.com/vegardga/workshop/blob/master/jam/images/01_05.png "GPIO")

## Steg 03 - Kode
```javascript
var five = require("johnny-five");
var board = new five.Board();

board.on("ready", function() {
  var led = new five.Led(12);
  led.blink(500);
});
```

## Steg 04 - Kjør!
terminal og kjør
