# Aztec-Platforms-ESP32-C6-PB-V1
In this Documentation we will explore the Aztec Platforms ESP32-C6-PB-V1. This board is designed to be a versitile project board that can be used in many ways. The main reason I design these boards is to reduce the amount of wiring for simple tasks like voltage reduction, common pinout placement, PSU jankery, etc.

Designed to get your projects off the ground faster, and, suitable for use in long term and permanent projects.

## Design Overview

### Board Size and hole spacing

<p align="center">
<img src="https://github.com/user-attachments/assets/1544f7ed-0271-4d81-82d0-7321f58d19ca" alt="Board and Hole Size" width="600">
</p>


### Power Rails

This board provides three usable voltage rails — 12 V, 5 V, and 3.3 V — making it versatile for a wide range of projects and connected devices.

Power is supplied through the USB-C female connector on the edge of the board. The USB-C controller negotiates with the charger to request 12 V at 3 A.

⚠️ Important: Not all USB-C chargers provide a 12 V profile. Some only support 9 V or 15 V, so be sure to check the fine print on your power brick to confirm it can supply 12 V at 3 A.

Once the board receives 12 V, the power is stepped down in two stages:

12 V → 5 V

12 V → 3.3 V

The ESP32-C6 runs on 3.3 V, which is also the voltage used by most sensors and peripherals. The 5 V line is useful for certain modules, and the raw 12 V input remains available as well.

This simple but flexible design ensures that whatever you’re connecting, you’ll have the right voltage available.

### Level Translator (Level Shifter) and Pin Voltages

Another key feature of this board, made possible by the 3.3 V and 5 V rails, is the level shifter. This component translates signals between 3.3 V (from the ESP32-C6) and 5 V, enabling you to control devices that require 5 V inputs. For example, the PWM input on a computer fan expects a 5 V signal, so you couldn’t drive it directly from the ESP32 alone.

The level shifter also works in reverse: it safely steps down 5 V input signals to 3.3 V, protecting the ESP32-C6 pins. This is particularly useful when working with sensors that output only 5 V, as connecting them directly could damage the microcontroller.

For each level-shifted signal, you’ll notice duplicate pins: one for the 3.3 V side and one for the 5 V side. ⚠️ Important: these pairs are electrically connected. You can use either the 3.3 V or the 5 V version of a pin (e.g., D0), but not both at the same time.

<p align="center">
<img src="https://github.com/user-attachments/assets/0776d2c0-86ce-46ed-93fa-f2099d2330b8" alt="Board and Hole Size" width="600">
</p>


## License
This repository is licensed under a custom Source-Available License.  
- ✅ Personal, hobbyist, and educational use of the code is allowed.  
- ❌ Commercial use, redistribution, and modification of images/docs are prohibited.  
- ℹ️ See [LICENSE](./LICENSE) for details. 
