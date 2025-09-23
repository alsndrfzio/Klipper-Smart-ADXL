# Klipper-Smart-ADXL
Smart_ADXL is an open-source project to facilitate resonance testing and applying input shaping.
A compact PCB the size of an Adafruit ADXL345 Breakout integrating a microcontroller (SAMD21G18) and an accelerometer (ADXL345),
makes resonance testing plug-and-play, just flash the Klipper firmware and include adxl.cfg to your klipper.cfg

## Why

Fast FDM printing can result in ringing or ghosting. Measuring the machine’s frequency response with an accelerometer enables input shaping algorithms (ZV/ZVD/EI, …) for cleaner corners and higher speeds. 
This project packages that workflow into a tiny board and a simple software toolconfiguration.

## Instructions
[Smart_ADXL Tutorial](Tutorial.md)


## Bill of Materials 

| Part   | Value                   | Device                                                                 | Footprint           |
|:-------|:------------------------|:-----------------------------------------------------------------------|:--------------------|
| /RTS   | ?1.0mm,SMD              | CIRCULARTESTPAD$20$1.0MM | TP_SMD_?1.0MM       |
| 3.3V   | ?1.0mm,SMD              | CIRCULARTESTPAD$20$1.0MM | TP_SMD_?1.0MM       |
| C1     | 0.1u                    | C-EUC0402                                                              | C0402               |
| C2     | 10u                     | C-EUC0402                                                              | C0402               |
| C3     | 100u                    | C-EUC0402                                                              | C0402               |
| C4     | 0.1u                    | C-EUC0402                                                              | C0402               |
| C5     | 0.1u                    | C-EUC0402                                                              | C0402               |
| C6     | 0.1u                    | C-EUC0402                                                              | C0402               |
| C7     | 0.1u                    | C-EUC0402                                                              | C0402               |
| C8     | 0.1u                    | C-EUC0402                                                              | C0402               |
| C9     | 18p                     | 1%                                                                     | C-EUC0402           |
| C10    | 18p                     | 1%                                                                     | C-EUC0402           |
| D1     | CHIP-FLAT-Y_0603-0.35MM | CHIP-FLAT-Y_0603-0.35MM                                                | LEDC1608X35N_FLAT-Y |
| L1     | BLM18PG471SN1D          | INDUCTOR0603                                                           | 0603                |
| R1     | 470                     | RESISTOR__CHIP-0402(1005-METRIC)                                       | RESC1005X40         |
| R2     | 10k                     | RESISTOR__CHIP-0402(1005-METRIC)                                       | RESC1005X40         |
| U1     | ACCEL_ADXL345           | LGA14                                                                  | ADXL345             |
