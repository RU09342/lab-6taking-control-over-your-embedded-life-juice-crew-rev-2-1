# Lab 6: Open Loop Systems
## Hardware
The circuit is setup as shown in the picture.

![pic](https://github.com/RU09342/lab-6taking-control-over-your-embedded-life-juice-crew-rev-2-1/blob/master/Open%20Loop%20Systems/schematic.JPG)

PWM with a low side switch was used to controll the fan because with a variable voltage input to the fan it took about 4 volts for the 5 volt fan to even start moving. whereas with PWM the fan would continue to spin down to 10% duty cycle

Decoupling capacitors were used to stabilize the power rails and the adc output from the LM35.

## System Modeling
![pic](https://github.com/RU09342/lab-6taking-control-over-your-embedded-life-juice-crew-rev-2-1/blob/master/Open%20Loop%20Systems/table.jpg)

The system was tested at duty cycles ranging from 0 to 100% duty cycle. The stabilized temperature is shown in the table. This information was then graphed with a trend line

![pic](https://github.com/RU09342/lab-6taking-control-over-your-embedded-life-juice-crew-rev-2-1/blob/master/Open%20Loop%20Systems/Graph.jpg)

The resulting equation y = -14.474x + 58.167 where y is Degrees C and x is duty cycle can be converted to (C-58.167)/-14.474 = Duty cycle. This can be used later when the user will input a degrees celsius over UART. The program will then calculate the appropriate duty cycle.

## Code Flow
The code uses the adc set up in a repeat single channel conversion mode so it constantly reads from the adc pin and updates the coresponding memory register. This is then converted to temperature in degrees C and transmitted over uart. when the user can then transmit a desired celsius set point over UART. The program will use the formula calculated in the previous part to determine the desired duty cycle.

## expected inputs
the code is designed to work for temperature inputs over UART ranging from 40 to 65 degrees celsius


