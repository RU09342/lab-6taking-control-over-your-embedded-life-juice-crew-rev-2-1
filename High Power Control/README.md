# Lab 6: "High Power" Control
## Switching
### Relays
![Relay](https://github.com/RU09342/lab-6taking-control-over-your-embedded-life-juice-crew-rev-2-1/blob/master/High%20Power%20Control/MOSTFET.gif)

An automotive relay was used for this section. This relay required 12V across the coil to actuate the relay. in addition to the 12 volts the coil drew 120mA. Because of this high voltage and current requirement to acctuate the coil a mosfet in a low side switch configuration was used provide power to the coil of the relay which then would close the contacts. One important addition to this circuit is a flywheel diode across the coil of the coil of the relay this prevents the voltage from skyrocketting when the coil is switched off. The frequency of the PWM signal was increased to find the limits of switching speed of the relay. After about 50Hz the frequency is high enough that the coil doesn't have enough time to fully de-energize, resulting in the relay being on all the time despite the PWM input.

### MOSFET Switching
![FET](https://github.com/RU09342/lab-6taking-control-over-your-embedded-life-juice-crew-rev-2-1/blob/master/High%20Power%20Control/mosfet%20high%20frequency.jpg)

The mosfet switch was done with an IRLB8721 N-Channel MOSFET. This FET has a V threshold of 1.8V putting it at a good range for switching with a 3.3V digital output. The mosfet was configured in a low side switch arrangement to power an 8ohm power resistor. Because the mosfet is electrically isolated there is practically no current draw out of the gpio pin of the G2553. When the frequency of the pwm signal was increased there oscilations started to become more and more prevalent on the output of the low side switch. ch1 waveform is the pwm output and ch2 waveform is the voltage at the drain of the mosfet.

![Relay](https://github.com/RU09342/lab-6taking-control-over-your-embedded-life-juice-crew-rev-2-1/blob/master/High%20Power%20Control/MOSTFET.gif)

## Best Config for High Current
![Relay](https://github.com/RU09342/lab-6taking-control-over-your-embedded-life-juice-crew-rev-2-1/blob/master/High%20Power%20Control/Best%20Config.JPG)
Using a N-MOSFET as a low side switch to energize the coil of a relay. Then the relay would be used to switch power to the load. The relay I used for this section of the lab was capable of 30 Amps. The LSS with the N-MOSFET is necessary because energizing the coil of the relay requires 120mA. This current is much greater than the 6mA a gpio pin is capable of providing. This would be the best configuraiton for high current where the application does not require any fast switching.
