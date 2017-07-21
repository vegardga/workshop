# Generell info
Her kommer det diverse generell informasjon.

## Backup av sd-kort (macOS)
Følgende kommandoer:
```
diskutil list
```

Finn så riktig disk, gjerne `/dev/disk2` eller `/dev/disk3`. Se etter størrelsen på kortet.

```
sudo dd bs=4m if=/dev/disk3 of=raspbian.img
```

Det blir da laget en backup av sd-kortet, som kan kopieres over til andre sd-kort.

## Oppsett av sd-kort (macOS)
Last ned etcher. Et gratisprogram som hjelper til med oppsett av sd-kort.

Etchet kan [lastes ned her](https://etcher.io/).

Følg instruksjonene i programmet.

## Oppsett av Arduino (macOS)
Last ned Arduino-software fra [nettsidene deres](https://www.arduino.cc/en/Main/Software).

Finn og velg StandardFirmataPlus under _File_ > _Examples_ > _Firmata_ > _StandardFirmataPlus_.
Det er denne som trengs for at johnny-five skal fungere.
