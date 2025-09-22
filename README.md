# Aztec-Platforms-ESP32-C6-PB-V1
In this Documentation we will explore the Aztec Platforms ESP32-C6-PB-V1. This board is designed to be a versitile project board that can be used in many ways. The main reason I design these boards is to reduce the amount of wiring for simple tasks like voltage reduction, common pinout placement, PSU jankery, etc.

Designed to get your projects off the ground faster, and, suitable for use in long term and permanent projects.

## Design Overview

### Board Size and hole spacing

<img src="https://github.com/user-attachments/assets/1544f7ed-0271-4d81-82d0-7321f58d19ca" alt="Board and Hole Size" width="600">

### Power Rails

When looking at the design of this board, it’s fairly straightforward. Power comes in through the USB-C female connector on the edge of the board. The USB-C controller negotiates with the charger and requests 12 V at 3 A.

⚠️ Important: Make sure your USB-C power supply (wall brick or equivalent) supports the 12 V/3 A profile. Not all USB-C chargers are required to offer 12 V — some only provide 9 V or 15 V. Many do support 12 V, but you’ll need to check the fine print on your power brick to confirm.

Once 12 V is supplied to the board, it is stepped down in two stages:

12 V → 5 V

12 V → 3.3 V

The ESP32-C6 itself runs on 3.3 V, and most sensors and peripherals you’ll use also run at 3.3 V. However, having 5 V available is convenient for certain modules, and the raw 12 V input is also accessible.

That gives you three usable voltage rails on this board — 12 V, 5 V, and 3.3 V — making it versatile for a wide range of projects and connected devices.



## License
This repository is licensed under a custom Source-Available License.  
- ✅ Personal, hobbyist, and educational use of the code is allowed.  
- ❌ Commercial use, redistribution, and modification of images/docs are prohibited.  
- ℹ️ See [LICENSE](./LICENSE) for details. 
