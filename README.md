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

#software structure


