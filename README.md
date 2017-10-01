# adcAMradio

Making an AM radio for ADC Fall 2017


# Notes:

AM freq: `850 kHz`

## RLC Bandpass filter:
Using a 1mH Inductor:
`1/(2Pi*Sqrt(1/mH * C)) = 850kHz
C = 35pF`

Using a variable capacitor (12-60pF)

Note: Calibrate Cap after the amp, the probes have a ~20 pF capacitance, so it affects your reading

## RF amp (Opamp):
Using an LT1222CN8:
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
