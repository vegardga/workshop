# Oppgaver - REPL

## Oppgave 1 - Skru av og på lyset
Lag et program som kan ta imot brukerinput, slik at du kan skru av og på lyset uten å måtte restarte programmet.

> **Oppgave:** Skru av og på lyset med egne kommandoer mens programmet kjører.

<details>
<summary>Klikk her for løsningsforslag</summary>
```javascript
var five = require("johnny-five");
var board = new five.Board();

board.on("ready", function() {
  var led = new five.Led(13);
  this.repl.inject({
    on: function() {
      led.on();
    },
    off: function() {
      led.off();
    }
  });
});
```

Lyset kan så kontrolleres gjennom følgende kommandoer:
```javascript
>> on() // skrur på lyset
eller
>> off() // skrur av lyset
```
</details>

## Oppgave 2 - Gjør som du vil mens programmet kjører!
Lag et program som gir deg tilgang til LED-lyset mens programmet kjører, slik at du kan bytte mellom f.eks. blinking og pulsering.

> **Oppgave:** Styr lyset mens programmet kjører.

<details>
<summary>Klikk her for løsningsforslag</summary>
```javascript
var five = require("johnny-five");
var board = new five.Board();

board.on("ready", function() {
  var led = new five.Led(13);
  this.repl.inject({
    led: led
  });
});
```

Lyset kan så kontrolleres gjennom følgende kommandoer:
```javascript
>> led.on()
>> led.off()
>> led.blink()
>> led.stop()
>> led.pulse()
```
</details>
