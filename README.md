# adcAMradio

Making an AM radio for ADC Fall 2017


# Notes:

AM freq: `850 kHz`

## RC Bandpass filter:
### Low Pass:
R = 475 Ohm

C = 330 pF

`1/(2Pi*RC) ~= 1MHz`

### High Pass:
R = 475 Ohm

C = 470 pF

`1/(2Pi*RC) ~= 720KHz`

## RF amp (Opamp):
Using a [LT1222CN8](http://cds.linear.com/docs/en/datasheet/1222fc.pdf):
GBWP: 500 MHz
Input freq 850 kHz
Max gain: 588.2 (Recommended gain is 100 - 1000, so we will probably be okay)``

`A = Vout/Vin = 1+(Rf/Rg)
A = 500 = 1 + (Rf/Rg)
A = 1 + (487kΩ/1kΩ) = 488
`

Note: Op amp is bi-polar, Power must be v+ (6v) and v- (-6v) relative to GND

## 

Gain 500:
A = 1+Rf/Rg
500 = 1 + Rf/Rq

## Analog Multiplier
Using an [AD633AN](http://www.analog.com/media/en/technical-documentation/data-sheets/AD633.pdf):

Using both noninverting inputs, inverting inputs and summing input to ground.
Attenuates by a factor of 10.

