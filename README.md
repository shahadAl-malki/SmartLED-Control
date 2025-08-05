Overview

This Arduino project controls an LED using two input methods:

A push button: the LED turns on only if the button is held for more than 1 second.
A PIR motion sensor: detects motion and turns on the LED. The current LED state is displayed on a 16x2 LCD screen.
Components • Arduino Uno • Push button • PIR motion sensor • LED • 220Ω resistor (for LED) • 16x2 LCD display • Breadboard

Wiring • Button connected to digital pin 2 • PIR sensor signal connected to digital pin 3 • LED connected to digital pin 13 through a resistor • LCD connected using standard pins or I2C (depending on your setup) • All components share common GND and 5V from the Arduino

Code Logic • Uses millis() to check how long the button is pressed (non-blocking timing) • If the button is held > 1000 ms → LED turns on • If motion is detected by the PIR sensor → LED turns on • If neither is active → LED turns off • The LCD continuously displays the LED status as “LED ON” or “LED OFF”
