# RUB
Makecode extension for 4tronix Really Useless Box

The Really Useless Box (RUB) is the 4tronix take on an idea that has been around for a long while. The RUB contains 4 Fireleds (RGB LEDs) a servo and a switch.
The Makecode extension provides blocks optimised for these components when used in the RUB

## Switch Blocks
You can either check the current state of the switch using CheckSwitch) or you can react to a change of state using OnSwitch<event>
```blocks
let myState = rub.checkSwitch();
```

## Servo Blocks
You can either drive the servo to selected positions by using the number of degrees, or you can move to the preset positions: Closed, Open or Switched
The Switched position is the position required to push the toggle switch closed
The movement can be at the full speed of the servo (equivalent to the VeryFast speed) or at a slower speed.
Note that the very first movement of the servo in the program will use the VeryFast speed to directly set the servo position.
If using degrees to set the servo position, note that the servo is constrained to be between the Closed position (default = 70) and the Switched position (default = 150)
```blocks
// set the preset positions of the servo to 70 (Closed), 90 (Open) and 150 (Switched)
rub.setServoPresets(70, 90, 150);

// Move the servo directly to positon 107 degrees
rub.setServo(107);

// Move the servo at defined speed to position 120 degrees
rub.moveServo(120, servoSpeed.Medium);

// Move the servo fairly slowly to Open position
rub.positionServo(servoPos.Open, servoSpeed.Medium);

// Wait for the servo to finish moving before continuing with program
rub.waitServo()
```

## Fireled Blocks



## Supported targets

* for PXT/microbit

## License

MIT
