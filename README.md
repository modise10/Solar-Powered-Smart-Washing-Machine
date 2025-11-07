# Solar-Powered Smart Washing Machine

## Description
This project is an **embedded control system for a solar-powered washing machine**.  
It uses an Arduino microcontroller and IR remote input to manage washing, rinsing, and spinning cycles. The system simulates power levels and ensures the drum is filled before washing or rinsing, and only spins once washing cycles are complete.  

Key features:
- Automated drum filling and drainage
- Wash, rinse, and spin cycles with sequence control
- Power-level simulation using IR remote
- Embedded LEDs simulate motor/coils operations

## Languages and Tools Used
- **Arduino / C++**
- **IRremote library**  
- **Tinkercad for simulation**

## Environments
- **Arduino IDE**
- **Tinkercad Simulation**

## Code Snippet
```cpp
#include <IRremote.hpp>

int ledPins[4] = {4, 5, 6, 7};  // LEDs/coils
int potIn = 0;

void setup() {
  Serial.begin(9600);
  IrReceiver.begin(3, ENABLE_LED_FEEDBACK);
  for (int i=4; i<=7; i++) pinMode(i, OUTPUT);
  pinMode(10, INPUT_PULLUP);
  pinMode(8, OUTPUT);
  pinMode(9, OUTPUT);
  pinMode(A5, INPUT);
}

// Main loop with power level detection, wash/rinse/spin cycles
void loop() {
  // (Your loop code here)
}
```
[Tinkercad Project](https://www.tinkercad.com/things/ccpbv1fgIvP-solar-powered-smart-washing-machine/editel?returnTo=https%3A%2F%2Fwww.tinkercad.com%2Fdashboard%2Fdesigns%2Fcircuits&sharecode=waecapH3zyDhFD8hZUO-Lveamf8x29OU6zoYnRObiP4)


