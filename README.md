# ATS Mini

![](docs/source/_static/esp32-si4732-ui-theme.jpg)

This firmware is for use on the SI4732 (ESP32-S3) Mini/Pocket Receiver

Based on the following sources:

* Volos Projects:    https://github.com/VolosR/TEmbedFMRadio
* PU2CLR, Ricardo:   https://github.com/pu2clr/SI4735
* Ralph Xavier:      https://github.com/ralphxavier/SI4735
* Goshante:          https://github.com/goshante/ats20_ats_ex
* G8PTN, Dave:       https://github.com/G8PTN/ATS_MINI

## Releases

Check out the [Releases](https://github.com/esp32-si4732/ats-mini/releases) page.

## Documentation

The hardware, software and flashing documentation is available at <https://esp32-si4732.github.io/ats-mini/>

### Firmware mit arduino-cli erstellen

1. Arduino CLI installieren und in das Projektverzeichnis wechseln.
2. Firmware kompilieren und auf den Empfänger flashen:

```shell
arduino-cli compile --clean -e -p <PORT> -u ats-mini
```

`<PORT>` steht für den seriellen Anschluss, z. B. `COM3` oder `/dev/ttyUSB0`.
Optionale Build-Flags lassen sich mit `--build-property` anhängen, etwa:

```shell
arduino-cli compile --build-property "compiler.cpp.extra_flags=-DENABLE_HOLDOFF" --clean -e -p <PORT> -u ats-mini
```
