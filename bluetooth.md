## Bluetooth Details

Vorze uses Bluetooth LE to communicate with other machines. 

### A10 Cyclone

The main service UUID for the A10 Cyclone is

```
40ee1111-63ec-4b7f-8ce7-712efd55b90e
```

To send data to the A10 Cyclone Unit, use the following characteristic

```
40ee2222-63ec-4b7f-8ce7-712efd55b90e
```

### UFO

Bluetooth details of the UFO are currently unknown.

### USB Dongle

Vorze toys are distributed with a USB dongle that will cause the BTLE
connection to emulate a serial port on windows. This allows the toy to
be easily used on all operating systems that do not have BTLE
capabilities, such a Windows XP/7/8/10 (though Windows 10 will have
BTLE capabilities sometime in 2017), OS X < 10.6, or Linux with Bluez
< 5.28.

Since the dongle is emulating a serial port, baud rate/data bits/etc
do not matter since the serial protocol is not actually being used.
