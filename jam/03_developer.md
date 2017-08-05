# 3 - Developer
Ferdig med oppgave 1 og 2 allerede? Wow, dette går unna!

I denne siste oppgaven skal du bruke en avstandsmåler for å styre en servo (eller motor om du vil).
Avstandsmåleren er den dingsen som har "to øyne", så husk å koble denne med "øynene" utover på koblingbrettet.

Lykke til!

## Klar?
Husk å koble Arduinoen fra Raspberry Pien før du går i gang med å koble egne kretser.

## Steg 01 - Koble

### 1/14
<img width="500" src="https://github.com/vegardga/workshop/blob/master/jam/images/03_01.png" alt="Arduino og koblingsbrett"/>

### 2/14
<img width="500" src="https://github.com/vegardga/workshop/blob/master/jam/images/03_02.png" alt="Jord"/>

### 3/14
<img width="500" src="https://github.com/vegardga/workshop/blob/master/jam/images/03_03.png" alt="Power"/>

### 4/14
<img width="500" src="https://github.com/vegardga/workshop/blob/master/jam/images/03_04.png" alt="Servo"/>

### 5/14
<img width="500" src="https://github.com/vegardga/workshop/blob/master/jam/images/03_05.png" alt="Servo - Jord"/>

### 6/14
<img width="500" src="https://github.com/vegardga/workshop/blob/master/jam/images/03_06.png" alt="servo - Power"/>

### 7/14
<img width="500" src="https://github.com/vegardga/workshop/blob/master/jam/images/03_07.png" alt="Servo - GPIO"/>

### 8/14
<img width="500" src="https://github.com/vegardga/workshop/blob/master/jam/images/03_08.png" alt="Servo - GPIO 2"/>

### 9/14
OBS! Denne må kobles riktig vei på koblingsbrettet. Koble den slik at "øynene" peker utover.
<img width="500" src="https://github.com/vegardga/workshop/blob/master/jam/images/03_09.png" alt="HC-SR04"/>

### 10/14
OBS! Se på avstandsmåleren, og finn ut hvilken ledning som er "GND". Det er denne som er jord.
<img width="500" src="https://github.com/vegardga/workshop/blob/master/jam/images/03_10.png" alt="HC-SR04 - Jord"/>

### 11/14
<img width="500" src="https://github.com/vegardga/workshop/blob/master/jam/images/03_11.png" alt="HC-SR04 - Power"/>

### 12/14
<img width="500" src="https://github.com/vegardga/workshop/blob/master/jam/images/03_12.png" alt="HC-SR04 - Trig"/>

### 13/14
<img width="500" src="https://github.com/vegardga/workshop/blob/master/jam/images/03_13.png" alt="HC-SR04 - Echo"/>

### 14/14
<img width="500" src="https://github.com/vegardga/workshop/blob/master/jam/images/03_14.png" alt="HC-SR04 - GPIO"/>

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

Det er viktig at det er store bokstaver der det står store bokstaver, og små bokstaver der det står små.

Husk å lagre filen! Enten gjennom menyen, `Fil` -> `Save`, eller trykk kombinasjonen `ctrl` + `s` på tastaturet.

## Steg 03 - Prøv!
Skriv følgende i terminalen:
```
node developer.js
```

Bruk kombinasjonen `ctrl` + `c` på tastaturet et par ganger for å stoppe kjøringen.

## Ferdig?
Kult, du har nå gjennomført oppgave 3 av 3!

Husk å koble fra hverandre kretsene før du avslutter :)

## Problemer?
Bare å spørre, vi er her for å hjelpe til!
