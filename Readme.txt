This is a demostration program written for hacking a USBasp programmer (any AliExpress/Dealextreme USBasp should work).
I found this code here: http://jethomson.wordpress.com/2011/08/18/project-ouroboros-reflashing-a-betemcu-usbasp-programmer
However, it was not working and cannot compile, so I updated v-usb library version and generate a new makefile.

Fuses are ready for atmega8 too.

Dependencies:
- avr-gcc
- another usbasp to flash this
- avr-dude

Just run
make clean
make hex
make program

Here is the original Readme:

If you want to reuse this code you MUST read USB-IDs-for-free.txt and change 
#define USB_CFG_VENDOR_NAME and #define USB_CFG_SERIAL_NUMBER in usbconfig.h
accordingly. 

Disclaimer: This device provides keyboard input to a computing device outside of user control. It is intended for experimentation and demonstration purposes only. It should never be used in a situation that can result in loss of data, property, or finances. It should never be used in a situation that could cause harm to a person via operation or failure. Usage of this device is beyond my control and I am not responsible for any damages resulting.

The idea for this project came a comment at the Stealth USB CapsLocker article at
http://macetech.com/blog/?q=node/46

 * Description: Simulates a USB HID keyboard that prints out "All work and no
 *              play makes Jack a dull boy." This code is only a slightly
 *              modified version of Frank Zhao's "USB Business Card" with some
 *              code added from Donald Papp's "Haunted, Mystery USB Device"
 *              both of which are based on Christian Starkjohann's "V-USB".
 * Instructions: Compile and flash the program to your USB AVR device, open an
 *               empty text file, and press Caps Lock or Num Lock to activate.
 * Author: Jonathan Thomson
 * Based on: Frank Zhao's "USB Business Card" -- http://frank.circleofcurrent.com/cache/usbbusinesscard.htm
 *           Donald Papp's "Haunted, Mystery USB Device" -- http://imakeprojects.com/Projects/haunted-usb-cable/
 *           Christian Starkjohann's "V-USB" -- http://www.obdev.at/products/vusb/index.html
 * Creation Date: 2011-10-18
 * Copyright: (c) 2011 Jonathan Thomson
 * License: GNU GPL v2 (see License.txt), GNU GPL v3
 * V-USB License: GNU GPL v2 (see License.txt), GNU GPL v3 or proprietary (usbdrv/CommercialLicense.txt)
