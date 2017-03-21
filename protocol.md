## Vorze Protocol

To communicate with the A10 Cyclone, a simple one-way protocol is used.

Each packet consists of 3 bytes in the following format:

```
0x01 0x01 0xZZ
```

### Reserved Bytes

The first and second byte have been observed (by tapping A10 Cyclone
communication) to always be 0x01, but this may not always be the case.
It is assumed these bytes are reserved for future use, (for instance,
specifying which cup of the UFO to turn). The third byte, denoted
0xZZ, sets the speed and direction of the toy.

### Direction

Direction is specified by most signicant bit of the 3rd byte. 0
denotes clockwise movement, 1 denotes counterclockwise movement.

### Speed

Speed is specified by the 7 remaining bits of the 3rd byte. There are
100 steps of speeds available. All speeds > 100 are ignored.

### Examples

To set the A10 Cyclone spinning clockwise at 50% speed, use the following command:

```
0x01 0x01 0x32
```

To set the A10 Cyclone spinning counterclockwise at 100% speed, use the following command:

```
0x01 0x01 0xe4
```

A speed over 100 will be ignored, so if, after the previous command,
the following command were sent

```
0x01 0x01 0xef
```

The toy would just continue spinning at 100% speed.
