# After mounting

When you have your PCB, the next step is to flash the klipper firmware in the microcontroller, so that it can be recognised by your mainboard.

As the (klipper doc)[https://www.klipper3d.org/Installation.html?h=flashing+klipper#building-and-flashing-the-micro-controller] says, you have to get yourself a klipper.bin file, it can be downloaded from (here)[Firmware], or you can create a new one

## How to create a new klipper.bin

The firmware file `klipper.bin` can be built using **WSL (Windows Subsystem for Linux)** on your computer, following the workflow below.

If this is the first configuration, clone the official Klipper Git repository:

```
git clone https://github.com/Klipper3d/klipper.git
```

Go to the Klipper directory
```
cd klipper
```
Clean remaining files from previous build.
```
make clean
```
5. Choose the options for the build.
```
make menuconfig
```
Use the following settings:
```
Microcontroller Architecture: SAMC21/SAMD21/SAMD51/SAMD5x	
Processor model: SAMD21G18	
Bootloader offset: 8KiB bootloader	
Clock Reference: 32.765 KHz crystal
```

To compile the file and move it to a known folder outside WSL:

```
make
cp ~/klipper/out/klipper.bin "Destination Folder Path"
```
Finally, the generated file must be uploaded to the microcontroller (using BOSSA), which must be switched to bootloader mode (check in the Windows Device Manager):

```
"C:\Users\”Nome Utente”\AppData\Local\Arduino15\packages\arduino\tools\bossac\ 1.7.0-arduino3/bossac.exe" -i -d –port= -U true -i -e -w -v 
"C:\Users\”Nome Utente”/”Cartella destinazione" -R

```

Now get into your Raspberry Pi using ssh and find the SAMD21 device using:

```
ls -l /dev/serial/by-id/
```

You will get an ID, that you'll insert in the (adxl.cfg)[Firmware/adxl.cfg.txt] file.

