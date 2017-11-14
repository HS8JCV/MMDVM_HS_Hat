# MMDVM_HS_Hat (VHF)
MMDVM_HS Hat for the Raspberry Pi (Zero)

This project forked from https://github.com/mathisschmieder/MMDVM_HS_Hat

This project provides a Raspberry Pi Hat for the [MMDVM_HS Hotspot](https://github.com/juribeparada/MMDVM_HS). It was designed for the Raspberry Pi Zero, but should work on any other Pi with the Hat interface. 

![PCB](https://github.com/HS8JCV/MMDVM_HS_Hat/blob/master/mmdvm_hs-hat.png)

The PCB is designed in KiCad and the necessary libraries are included. The supplied Gerber files can be used to order PCBs, for example at Elecrow or DirtyPCBs. The board's dimensions are 65x30mm.

You can order 3 beautiful, purple Revision 1.2.1(VHF) PCBs for $15 at [OSHPark](https://oshpark.com/shared_projects/D5eErGib)! 

## Revisions
If you want to know about other revisions ,Please goto  orginal repository https://github.com/mathisschmieder/MMDVM_HS_Hat
### Revision 1.2.1(VHF)
This Revision forked from revision 1.2 of https://github.com/mathisschmieder/MMDVM_HS_Hat
Detail
- Remove ceramic UHF antenna
- Add Inductor for External VCO
- Changed resistor and capacitor loop filter value
- Changed Lowpass filter circuit and value

## BOM
* All necessary parts for the Revision 1.2.1(VHF) board can be ordered at Mouser using the following [Comming soon]

Either the ADF7021 or the ADF7021-N can be used. Define the proper version in the firmware!

## Firmware Installation
For specific details about the firmware installation, check [these](https://github.com/juribeparada/MMDVM_HS#build-de-firmware-and-upload-to-zumspot-rpi) instructions. The process is similar to the installation on the ZumSpot Pi. 

Enable the following settings in Config.h:

    #define MMDVM_HS_HAT_REV12
    #define ENABLE_ADF7021
    #define ADF7021_14_7456
    #define STM32_USART1_HOST
    #define ENABLE_SCAN_MODE

Build the firmware:

    make

And finally upload the firmware to the MMDVM_HS_Hat:

    sudo make mmdvm_hs_hat

## License
This project is released under the Creative Commons Attribution-NonCommercial-ShareAlike 3.0 (CC-BY-NC-SA 3.0, https://creativecommons.org/licenses/by-nc-sa/3.0/) license. You may edit and share it as you like, as long as credit is given and the license is not changed. You can build as many boards for you and your friends as you like and you can even sell it to them to cover your costs, **however it is strictly forbidden to turn this into a commercial product! You are not allowed to build and sell these boards for profit!**
