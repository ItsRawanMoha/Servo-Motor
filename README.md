# Servo Motor Task

Welcome to the Servo Motor task! This task demonstrates how to control a servo motor using an Arduino. Servo motors are commonly used in robotics and automation for precise control of angular position. 

## Introduction

The Servo Motor task aims to provide a practical example of controlling a servo motor with an Arduino microcontroller. Servo motors are special types of motors that can rotate to a specific angle based on the electrical signal they receive. They are widely used in various applications such as robotics, remote-controlled vehicles, and camera stabilization systems.

## How it Works

Servo motors work by receiving a control signal, typically a pulse-width modulation (PWM) signal, from a microcontroller like Arduino. The width of the PWM signal determines the position of the servo motor's shaft. By varying the width of the PWM signal, we can control the angle of rotation of the servo motor.

## Getting Started

To get started with this task, you will need the following components:

- Arduino board (e.g., Arduino Uno)
- Servo motor
- Jumper wires

## Steps

Follow these steps to set up the task:

1. Connect the signal wire of the servo motor to one of the PWM pins on the Arduino (e.g., pin 9).
2. Connect the power (VCC) wire of the servo motor to the 5V pin on the Arduino.
3. Connect the ground (GND) wire of the servo motor to the GND pin on the Arduino.
4. Ensure all connections are secure.

| Arduino Pin    | Servo Motor    |
| -------------- | -------------- |
| PWM (e.g., 9)  | Signal         |
| 5V             | VCC            |
| GND            | GND            |

## Connection

The following table summarizes the wiring connections between the Arduino and the servo motor:

![screen-gif](https://github.com/ItsRawanMoha/Servo-Motor/blob/main/ServoMotor.png)

## Output

Once the circuit is set up and the code is uploaded to the Arduino board, the servo motor should start rotating according to the instructions in the code.

## Code
```
#include <Servo.h>

Servo myservo;  // create servo object to control a servo
// twelve servo objects can be created on most boards

int pos = 0;    // variable to store the servo position

void setup() {
  myservo.attach(9);  // attaches the servo on pin 9 to the servo object
}

void loop() {
  for (pos = 0; pos <= 180; pos += 1) { // goes from 0 degrees to 180 degrees
    // in steps of 1 degree
    myservo.write(pos);              // tell servo to go to position in variable 'pos'
    delay(15);                       // waits 15 ms for the servo to reach the position
  }
  for (pos = 180; pos >= 0; pos -= 1) { // goes from 180 degrees to 0 degrees
    myservo.write(pos);              // tell servo to go to position in variable 'pos'
    delay(15);                       // waits 15 ms for the servo to reach the position
  }
}
```

## Pictures

<img src="https://github.com/ItsRawanMoha/Servo-Motor/blob/main/ServoMotorP.jpeg" alt="Alt text" width="300" height="400">  ![screen-gif](https://github.com/ItsRawanMoha/Servo-Motor/blob/main/ServoMotorG.gif)

## Conclusion

The Servo Motor task provides a hands-on introduction to controlling servo motors with Arduino. By understanding the basics of servo motor control, you can explore more advanced tasks and applications in robotics, automation, and beyond.
