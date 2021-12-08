# Wemos-D1-Mini-Tricks
Tricks I learned with working with the Wemos D1 Mini

## Reflashing a bricked D1 Mini V4.0
Put WeMos D1 Mini on breadboard
- connect GPIO 0 to GND
- connect GPIO 15 to GND
- connect GPIO 2 to 3.3V
then flash the new firmware.

I had to use CMD on Administrator

```
python3 -m esptool --port PORT_NAME --baud 1000000 write_flash --erase-all --flash_size=4MB -fm dio 0 FIRMWARE.bin
```
where PORT_NAME is COM4 or similar on windows and FIRMWARE.bin is the most recent firmware from [Micropython Firmware Downloads](https://micropython.org/download)
