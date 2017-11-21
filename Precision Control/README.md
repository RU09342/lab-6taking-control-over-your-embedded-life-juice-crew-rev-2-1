# Lab 6: Precision Control
## Low Pass Filter DAC
### Hardware
![pic](https://github.com/RU09342/lab-6taking-control-over-your-embedded-life-juice-crew-rev-2-1/blob/master/Precision%20Control/pics/lpfDAC.JPG)

The opamp is the low pass filter with a cutt off frequency of around 1kHz. The second opamp is an inverting op amp with a gain of 1. This just makes the final output a positive voltage from 0 to Vcc depending on the duty cycle of the PWM input.
### Loading Effects
The loading effects on this circuit were tested with a 100 and 1k ohm resitors. Because low pass filter is active it will have a good deal of current gain and should be able to support a moderate current output. With no load and a 50% duty cycle input the DAC put out 1.63V. With loads of 100 and 1k ohms the DAC put out 1.60V and 1.63V.
### Triangle Wave FFT
![pic]()
![pic](https://github.com/RU09342/lab-6taking-control-over-your-embedded-life-juice-crew-rev-2-1/blob/master/Precision%20Control/pics/20171115_130149.jpg)
as can be seen in the picture the harmonics that should be present in a FFT of a triangle wave are not there. This happens because this type of DAC does not work well for signal generation.

## R2R DAC
### Hardware
![pic](https://github.com/RU09342/lab-6taking-control-over-your-embedded-life-juice-crew-rev-2-1/blob/master/Precision%20Control/pics/R-2R.JPG)
### Loading Effects
The loading effects on this circuit were tested with a 100 and 1k ohm resitors.With no load and an input of 127 the DAC put out 1.48V. With loads of 100 and 1k ohms the DAC put out 1.60mV and 15.85mV.
### Triangle Wave FFT
![pic](https://github.com/RU09342/lab-6taking-control-over-your-embedded-life-juice-crew-rev-2-1/blob/master/Precision%20Control/pics/20171115_144405.jpg)
![pic](https://github.com/RU09342/lab-6taking-control-over-your-embedded-life-juice-crew-rev-2-1/blob/master/Precision%20Control/pics/20171115_145043.jpg)
As can be seen in the picture. The harmonics from triangle wave gennerated using the R2R ladder are very clear and easy to see. 
## Bill of Materials
4x 100k 1/4 watt resistors

9x 10k 1/4 watt resistors

7x 5.1k 1/4 watt resistors

1x 1.5nF capacitor

1x TL072

![Digikey Cart](http://www.digikey.com/short/q3tpvn)
