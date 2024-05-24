# Custom Arduino Program To Enable Special Toggles
**Legal Disclaimer: This program is FOR OFF-ROAD AND EXHIBITION USE ONLY. Winking and sleepy headlight mode are probably not legal on most public roads.**

*Personal disclaimer: I am not a programmer by trade nor am I a particularly good one. Use my modifications at your own risk.*

## How to Use
Program the file "Fiero Headlight Toggle Modes 1_0.ino" to your Arduino in place of the standard programming. It contains most of the same code as the original but with additions to enable fun headlight behaviors.

Modes are activated using the headlight switch. Upon turning the headlight switch off, you have 1 second to enter a command (detailed below).

If the headlight switch is left off for more than 1 second, the headlights will close and the module will turn off.

## Available Toggles
### Wink
You can wink either the left or right headlight by turning the headlight switch off, then back on within 1 second.\
The amount of time between turning the switch off and on determines which side will wink.

**Right headlight:** turn the headlight switch off and on within half a second.

**Left headlight:** turn the headlight switch off, wait half a second, then turn it back on.

### Sleepy Mode
Sleepy mode and normal mode are toggled back and forth using the same command.\
To switch between normal and sleepy mode, turn the headlight switch off and on twice. (off>on>off>on)

Each flip must be completed within one second of the last action.

Winking in sleepy mode works the same as normal.

## Troubleshooting
**Sleepy mode winks are not returning the lights to the correct height.**
  * You will need to adjust the motor run timing manually for your own car.
    * For the left light, adjust the value of 'count' on line 385.
    * For the right light, adjust the value of 'count' on line 489.
  * Setting 'count' to a higher value will reduce the motor run time, lifting the light lower.
  * Setting 'count' to a lower value will increase the motor run time, lifting the light higher.
  * 'count' has a maximum limit of 150. Setting it to 150 or higher will not run the motor at all.
