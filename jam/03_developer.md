# Developer

## Klar?
Husk å koble Arduinoen fra Raspberry Pien før du går i gang med å koble egne kretser.

## Steg 01 - Koble
![alt text](https://github.com/vegardga/workshop/blob/master/jam/images/03_01.png "Arduino og koblingsbrett")

![alt text](https://github.com/vegardga/workshop/blob/master/jam/images/03_02.png "Jord")

![alt text](https://github.com/vegardga/workshop/blob/master/jam/images/03_03.png "Power")

![alt text](https://github.com/vegardga/workshop/blob/master/jam/images/03_04.png "Servo")

![alt text](https://github.com/vegardga/workshop/blob/master/jam/images/03_05.png "Servo - Jord")

![alt text](https://github.com/vegardga/workshop/blob/master/jam/images/03_06.png "Servo - Power")

![alt text](https://github.com/vegardga/workshop/blob/master/jam/images/03_07.png "Servo - GPIO")

![alt text](https://github.com/vegardga/workshop/blob/master/jam/images/03_08.png "Servo - GPIO 2")

![alt text](https://github.com/vegardga/workshop/blob/master/jam/images/03_09.png "HC-SR04")

![alt text](https://github.com/vegardga/workshop/blob/master/jam/images/03_10.png "HC-SR04 - Jord")

![alt text](https://github.com/vegardga/workshop/blob/master/jam/images/03_11.png "HC-SR04 - Power")

![alt text](https://github.com/vegardga/workshop/blob/master/jam/images/03_12.png "HC-SR04 - Trig")

![alt text](https://github.com/vegardga/workshop/blob/master/jam/images/03_13.png "HC-SR04 - Echo")

![alt text](https://github.com/vegardga/workshop/blob/master/jam/images/03_14.png "HC-SR04 - GPIO")

## Steg 02 - Kode
```javascript
var five = require("johnny-five");
var board = new five.Board();

board.on("ready", function() {
  var servo = new five.Servo(10);
  var proximity = new five.Proximity({
    controller: "HCSR04",
    pin: 7,
    freq: 1000
  });

  proximity.on("data", function() {
    if (this.cm < 20) {
      servo.min();
    } else if (this.cm < 40) {
      servo.center();
    } else {
      servo.max();
    }
  });
});
```

## Steg 03 - Prøv!
Skriv følgende i kommandolinja:
```
node developer.js
```

## Ferdig?
Skriv følgende i kommandolinja:
```
./done.sh
```

Husk å koble fra hverandre kretsene før du går videre :)
