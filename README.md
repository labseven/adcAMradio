# adcAMradio

Making an AM radio for ADC Fall 2017


# Notes:

AM freq: 850 kHz

## RLC Bandpass filter:
Using a 1mH Inductor:
1/(2Pi*Sqrt(1/mH * C)) = 850kHz
C = 35pF

Using a variable capacitor (12-60pF)

## RF amp (Opamp):
Using an LT1222:
GBWP: 500 MHz
Input freq 850 kHz
Max gain: 588.2 (Reccomended gain is 100 - 1000, so we will probably be okay)

