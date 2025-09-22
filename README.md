# Klipper-Smart-ADXL
Smart_ADXL is an open-source project to facilitate resonance testing and applying input shaping.
A compact PCB the size of an Adafruit ADXL345 Breakout integrating a microcontroller (SAMD21G18) and an accelerometer (ADXL345),
makes resonance testing plug-and-play, just flash the Klipper firmware and include adxl.cfg to your klipper.cfg

# Why

Fast FDM printing can result in ringing or ghosting. Measuring the machine’s frequency response with an accelerometer enables input shaping (ZV/ZVD/EI, …) for cleaner corners and higher speeds. 
This project packages that workflow into a tiny board and a simple software toolconfiguration.
