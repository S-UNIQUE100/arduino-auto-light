# arduino-auto-light
# Auto Light System (Arduino)

An LDR-controlled LED that automatically adjusts brightness to the room's light level, built and simulated in Tinkercad.

## How it works
- The LDR and a 10kΩ resistor form a voltage divider read on A0.
- The sketch maps the reading (54 dark to 974 bright) to a PWM value (255 to 0).
- The LED on pin 9 gets brighter as the room gets darker.

## Components
- Arduino Uno
- LDR (photoresistor)
- LED
- 220Ω resistor
- 10kΩ resistor
- Breadboard and jumper wires

## Wiring
| Component | Connection |
|---|---|
| LDR + 10kΩ divider midpoint | A0 |
| LED (+) via 220Ω | Pin 9 (PWM) |
| LED (-) | GND |
| Divider and rails | 5V / GND |

## Test results
| Condition | Reading | LED |
|---|---|---|
| Bright | ~974 | Off |
| Medium | ~500 | Dim |
| Dark | ~54 | Full brightness |

## Files
- `autolight.ino` - Arduino sketch
- `wiring-diagram.png` - circuit diagram
- Demo video: [Drive link]