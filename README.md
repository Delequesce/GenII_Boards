## Rev 3 Changes

### Pi Interface and Power Board
1) ~~Set 4 LSBs of each color going into the RGB interface HIGH. This still allows for 4096 possible colors but frees up 12 total GPIOs.~~
2) ~~Replaced source switching circuitry with a source selector IC (LTC4412)~~. ~~Also implemented circuitry to enable the STM32 to shutdown and wakeup the Pi with the power button for better power management.~~ 
3) ~~Replaced the Pi Zero W with a Pi Zero 2 W.~~
4) ~~Added I2C RESET pin for enabling the capacitive touch screen~~
5) ~~Moved the FPC connector to the Measurement Board to the top of the board to ease assembly.~~ 
6) ~~Moved the RGB and I2C connectors to the screen closer to the edge (or top with flipped connections) to ease assembly.~~ 
7) ~~Fixed wiring issues for Vdd and Vcc out to the Measurement Board.~~
8) ~~Increased the size of the mounting holes for the battery cables to ease connection. (0.65 mm diameter for 22 AWG)~~
9) ~~Generally improved power routing~~
10) ~~Improved PWM backlight enable routing for better fidelity.~~
11) ~~Specced out smaller battery connectors to ease assembly and reduce size. (22 AWG, Amazon)~~
12) ~~Moved the Vdd Main LDO to the Measurement Board~~
13) ~~Added a fuse to the TPS2400 circuit and also a fuse after the source selector.~~
14) ~~Added a small board meant to be separated for interfacing the pushbutton reset switch with the rest of the circuit.~~

### Measurement Board
1) ~~Fixed PWM Heater signal routing~~ 
2) ~~Flipped FPC connector to Pi Board to top of board to ease assembly. Checked wiring against the Pi board.~~
3) ~~Moved Vdd Main LDO from Pi Board.~~ 
4) Added external interrupt pin and Vcc controller output pin to interface with external pushbutton board.

### Heater Board
1) Reduced the size of vias and made more of them for better heating and lower losses. 
2) Moved the thermistors slightly farther from the center to improve temperature tracking. Alternately just reduced the size of the heating area to improve tracking without separating the thermistors from the chip. (Maybe)