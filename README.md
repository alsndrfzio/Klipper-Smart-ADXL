# Klipper-Smart-ADXL
Smart_ADXL is an open-source project to facilitate [resonance testing](https://www.klipper3d.org/Measuring_Resonances.html) and applying [input shaping](https://www.klipper3d.org/Resonance_Compensation.html) on [klipper](https://www.klipper3d.org/) based 3D Printers.
A compact PCB the size of an Adafruit ADXL345 Breakout integrating a microcontroller (SAMD21G18) and an accelerometer (ADXL345),
makes resonance testing plug-and-play, just flash the Klipper firmware and include adxl.cfg to your klipper.cfg

## Why

Fast FDM printing can result in ringing or ghosting. Klipper has some integrated input shaping algorithms, that can [drastically reduce those effects.](https://www.youtube.com/watch?v=5fOhi-LL9dU)\
To apply them you need to measure the resonance frequency of the system, so an accelerometer is needed.\
As seen in the documentation says, it is quite an annoying task to connect the module via SPI using shielded cables,\
so this project packages that workflow into a tiny board and a simple software configuration. 

## Instructions
[Smart_ADXL Tutorial](Tutorial.md)


