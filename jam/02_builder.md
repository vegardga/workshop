# Builder

## Klar?
Husk å koble Arduinoen fra Raspberry Pien før du går i gang med å koble egne kretser.

## Steg 01 - Koble
![alt text](https://github.com/vegardga/workshop/blob/master/jam/images/02_01.png "Arduino og koblingsbrett")

![alt text](https://github.com/vegardga/workshop/blob/master/jam/images/02_02.png "Knapp")

![alt text](https://github.com/vegardga/workshop/blob/master/jam/images/02_03.png "Motstand")

![alt text](https://github.com/vegardga/workshop/blob/master/jam/images/02_04.png "Jord")

![alt text](https://github.com/vegardga/workshop/blob/master/jam/images/02_05.png "Jord 2")

![alt text](https://github.com/vegardga/workshop/blob/master/jam/images/02_06.png "Power")

![alt text](https://github.com/vegardga/workshop/blob/master/jam/images/02_07.png "Power 2")

![alt text](https://github.com/vegardga/workshop/blob/master/jam/images/02_08.png "GPIO")

![alt text](https://github.com/vegardga/workshop/blob/master/jam/images/02_09.png "Piezo")

![alt text](https://github.com/vegardga/workshop/blob/master/jam/images/02_10.png "Piezo jord")

![alt text](https://github.com/vegardga/workshop/blob/master/jam/images/02_11.png "Piezo GPIO")

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
      tempo: 100
    });
  });
});
```

## Steg 03 - Prøv!
Skriv følgende i kommandolinja:
```
node builder.js
```

## Ferdig?
Skriv følgende i kommandolinja:
```
./done.sh
```

Husk å koble fra hverandre kretsene før du går videre :)
