# Aztec-Platforms-ESP32-C6-PB-V1
In this Documentation we will explore the Aztec Platforms ESP32-C6-PB-V1. This board is designed to be a versitile project board that can be used in many ways. The main reason I design these boards is to reduce the amount of wiring for simple tasks like voltage reduction, common pinout placement, PSU jankery, etc.

Designed to get your projects off the ground faster, and, suitable for use in long term and permanent projects.

## Design Overview

### Board Size and hole spacing

<img src="https://github.com/user-attachments/assets/1544f7ed-0271-4d81-82d0-7321f58d19ca" alt="Board and Hole Size" width="600">

### Power Rails

This board provides three usable voltage rails — 12 V, 5 V, and 3.3 V — making it versatile for a wide range of projects and connected devices.

Power is supplied through the USB-C female connector on the edge of the board. The USB-C controller negotiates with the charger to request 12 V at 3 A.

⚠️ Important: Not all USB-C chargers provide a 12 V profile. Some only support 9 V or 15 V, so be sure to check the fine print on your power brick to confirm it can supply 12 V at 3 A.

Once the board receives 12 V, the power is stepped down in two stages:

12 V → 5 V

12 V → 3.3 V

The ESP32-C6 runs on 3.3 V, which is also the voltage used by most sensors and peripherals. The 5 V line is useful for certain modules, and the raw 12 V input remains available as well.

This simple but flexible design ensures that whatever you’re connecting, you’ll have the right voltage available.



## License
This repository is licensed under a custom Source-Available License.  
- ✅ Personal, hobbyist, and educational use of the code is allowed.  
- ❌ Commercial use, redistribution, and modification of images/docs are prohibited.  
- ℹ️ See [LICENSE](./LICENSE) for details. 
