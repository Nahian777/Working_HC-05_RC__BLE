
# HC-05 RC Bluetooth Controller

Control a 2-motor RC car using an Arduino and an HC-05 Bluetooth module.  
Includes the Arduino sketch and an Android controller app.

## Overview
This project uses an HC-05 Bluetooth module to receive single-character commands from an Android app and drive two DC motors through a motor driver.

- Main sketch: `working_HC-05_RC_BLE.ino`
- Android app: `Arduino Car.apk`

## Files
- working_HC-05_RC_BLE.ino
- Arduino Car.apk

## Hardware & Wiring
## Diagram
![Wiring Diagram](https://github.com/Nahian777/Working_HC-05_RC__BLE/blob/main/diagram.png?raw=true)

### Motor Driver Pins (as used in the sketch)
| Function | Arduino Pin |
|----------|-------------|
| in1      | D12 |
| in2      | D11 |
| in3      | D10 |
| in4      | D9  |
| LED      | D13 |

### HC-05 Bluetooth Module
- HC-05 TX → Arduino RX  
- HC-05 RX → Arduino TX  
- Common ground between Arduino, HC-05, and motor power

### Power
Use a separate power source for the motors. Do not power motors directly from the Arduino.

## Serial Commands
Send a *single ASCII character* from the controller app:

| Command | Action |
|----------|--------|
| F | Move forward |
| B | Move backward |
| L | Turn left |
| R | Turn right |
| C | Left backward, right forward |
| A | Left forward, right backward |
| S | Stop |
| O | LED on |
| s | LED off |

## Usage
1. Upload `working_HC-05_RC_BLE.ino` to the Arduino.
2. Connect motors and HC-05 as described above.
3. Pair your phone with the HC-05 module.
4. Open `Arduino Car.apk` and connect.
5. Send commands to control the car.
EOF
