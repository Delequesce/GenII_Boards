## Rev 3 Changes

### Pi Interface and Power Board
1) Set 4 LSBs of each color going into the RGB interface HIGH. This still allows for 4096 possible colors but frees up 12 total GPIOs. 
2) Removed the TPS2400 detector and instead put in a TVS diode with a source selector IC (LTC4412). Also implemented circuitry to enable the STM32 to shutdown and wakeup the Pi with the power button for better power management. 
3) Replaced the Pi Zero W with a Pi Zero 2 W. 
4) Added I2C RESET pin for enabling the capacitive touch screen
5) Moved the FPC connector to the Measurement Board to the top of the board to ease assembly. 
6) Moved the RGB and I2C connectors to the screen closer to the edge (or top with flipped connections) to ease assembly. 
7) Fixed wiring issues for Vdd and Vcc out to the Measurement Board.
8) Increased the size of the mounting holes for the battery cables to ease connection.
9) Generally improved power routing
10) Improved PWM backlight enable routing for better fidelity. 
11) Improved battery level monitoring circuitry to go into the STM32 ADC. 
12) Specced out smaller battery connectors to ease assembly and reduce size. 

### Measurement Board
1) Fixed PWM Heater signal routing 
2) Flipped FPC connector to Pi Board to top of board to ease assembly. Checked wiring against the Pi board.

### Heater Board
1) Reduced the size of vias and made more of them for better heating and lower losses. 
2) Moved the thermistors slightly farther from the center to improve temperature tracking. Alternately just reduced the size of the heating area to improve tracking without separating the thermistors from the chip. (Maybe)
