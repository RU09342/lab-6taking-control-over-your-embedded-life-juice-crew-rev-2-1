# Lab 6: Precision Control
## Low Pass Filter DAC
### Hardware
![pic](https://github.com/RU09342/lab-6taking-control-over-your-embedded-life-juice-crew-rev-2-1/blob/master/Precision%20Control/pics/lpfDAC.JPG)

The opamp is the low pass filter with a cutt off frequency of around 1kHz. The second opamp is an inverting op amp with a gain of 1. This just makes the final output a positive voltage from 0 to Vcc depending on the duty cycle of the PWM input.
### Loading Effects
The loading effects on this circuit were tested with a 100 and 10k ohm resitors. Because low pass filter is active it will have a good deal of current gain and should be able to support a moderate current output. 
### Triangle Wave FFT
![pic]()

## R2R DAC
### Hardware
![pic](https://github.com/RU09342/lab-6taking-control-over-your-embedded-life-juice-crew-rev-2-1/blob/master/Precision%20Control/pics/R-2R.JPG)
### Loading Effects
The loading effects on this circuit were tested with a 100 and 10k ohm resitors.
### Triangle Wave FFT
![pic]()

##Bill of Materials
4x 100k 1/4 watt resistors

9x 10k 1/4 watt resistors

7x 5.1k 1/4 watt resistors

1x 1.5nF capacitor

1x TL072

![Digikey Cart](http://www.digikey.com/short/q3tpvn)