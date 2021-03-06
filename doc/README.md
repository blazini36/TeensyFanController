# Teensy Fan Controller

A PC fan controller with temperature sensor input, for **[Teensy](https://www.pjrc.com/teensy/index.html) 3.x** USB Development Board\(s\).

Supports up to 6 fans \(4pin/PWM\), and up to 5 temperature sensors \(thermistors\). Each fan may individually operate in PID, temperature-percent table, or fixed-percent control modes.

Designed to control radiator fans on a PC water cooling loop \(to maintain supply water temperature\), but may be configured for other purposes \(for example, see [Demo/Router Cooling Demo](demo/router-cooling-demo.md)\).

![Simple 001 PCB in a Raspberry Pi 3 case](images/simple001.photo.2.png)

## Releases

- v0.1.0
  - [Firmware (Teensy 3.2, 3.5)](https://github.com/mstrthealias/TeensyFanController/releases/tag/v0.1.0)
  - [Configuration UI (Windows 10)](https://github.com/mstrthealias/TFC-ui/releases/tag/v0.1.0)

## Hardware

The following hardware has been used with Teensy Fan Controller:

* [Prototype - Simple PCB](hardware/simple-pcb.md): requires PCB fabrication \(gerber files provided\) and through-hole soldering
* [Breadboard](hardware/breadboard.md): breadboard example with a single fan/single sensor
* [Prototype - Hand-made \(Schmart Board based\)](hardware/prototype.md): uses over-the-shelf components

Related files are available in the [TeensyFanController/Hardware](https://github.com/mstrthealias/TeensyFanController/tree/master/Hardware) folder.

### Hardware Interface

The Teensy Micro USB port is used to configure and monitor the fan controller.

{% hint style="info" %}
It is possible to connect the Micro USB port to an internal motherboard USB 1.1/2.0 header, by making a custom cable, or purchasing a _Micro USB 5pin Male to 1x 5Pin Female 0.1" USB Header PCB Motherboard Cable_.
{% endhint %}

## Software

### Qt UI

[Teensy Fan Controller UI \(Qt5\)](https://github.com/mstrthealias/TFC-ui): provides a user interface to configure or monitor the fan controller (only needed for initial configuration).

### Linux Kernel module \(hwmon\)

[Fork of liquidtux](https://github.com/mstrthealias/liquidtux): Linux kernel module for reading temperatures and fan RPMs using *lm-sensors* or *psensor*.  Tested on Ubuntu 18.04.

