# macchina-imaginis-framework
Drivers and utilities for macchina imaginis arts machines

# description
The macchina imaginis art machines mostly have the same structure.
Sounds are played and lamps controlled with buttons or switches.
In addition, there are various display and input devices that have to be controlled.
Depending on the requirements of the machine, different
output and input modules use different interfaces and protocols.
Such as SPI, I2c or Modbus.

A Raspberry PI 3 or 4 is used as the control and sound output device.
The control software is written in C++.

The first control software was satisfactory in function, but not very flexible to reflect the demands of the artists and the diversity of the modules.
Therefore, the software prototype is now divided into different libraries in order to obtain greater flexibility.
The io's using are now event driven instead using an io process image (miio is deprecated)

#yocto 
The libraries are included in the meta-macchinaimaginis yocto layer

# software konzept
# overview

![alt text](https://github.com/SigiMcArcel/macchina-imaginis-framework/blob/main/blob/Overview.png)

The Framework contains following libraries:
Further Informations are find in the library repository itself

## drivers -> midriver
Contains the low level acces to the Raspberry PI Interfaces and GPIO.
Used by mimodules
## io modules  -> mimodules
Contains the abstraction of the hardware interfaces and managing of the mimodules 
## sound -> misound
Contains classes for playing sounds
## timers,thread handling -> miutils
Contains classses for Timing, Threading ...

## hardware abstraction
As with a PLC, the inputs and outputs are written to a process image or read from the process image.
For this purpose, the hardware interfaces are standardized with a C++ interface.
The control software uses the mimodules to set outputs and uses events (callbacks) for the inputs.
