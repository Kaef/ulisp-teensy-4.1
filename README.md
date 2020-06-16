# ulisp-3.3-arm
Many thanks to David and the members of the ulisp forum for supporting ulisp.
Kaef, 16.06.2020

# Note for Teensy-4.1 board support
This is a fork of ulisp.arm with added support for Teensy-4.1 board.
The board is made by pjrc, please see documentation at their webpage.

## Motivation
Teensy-4.1 uses the same ARM cortex M7 processor as the Teensy-4.0 boards, so I
*think* this version of ulisp could also be used with the Teensy-4.0 boards, but
I haven't tested it.

This is an additional 'proof of concept' I made with ulisp-2.8-arm for the
Teensy-4.0 board.
ulisp is able to use the on-board sd-card socket to store uLisp-Images
and other Files (i.e. uLisp code files) on the sd-card.
Not all functions are tested yet on the Teensy-4.1 board, just some
basic ulisp code was used (tak, q), i2c, spi, analog-read/-write are not tested yet.

I added four functions to ulisp to use the sd-card more confortable:
(ls), (rm "file-name"), (mkdir "dir-name") and (rmdir "dir-name").
There are also functions written in ulisp to load, save and cat out (ulisp-) files
from/to the sd-card. You'll find these functions in the lisp-library.
All functions are described in the file documentation/reference-sd-card-functions.md

## iMXRT1062 basic features (for details look at pjrc page)
* ARM cortex M7 processor at 600 MHz with a NXP iMXRT1062 chip
* 1024k RAM, 2048k flash
* USB, CAN, I2S, SPI, I2C, ADC, RTC, FP unit and much more
* needs 0.42 seconds for the (tak 18 12 6) benchmark,
  which is about 14 times faster than the Maxim MAX32620FTHR,
  currently the fastest ulisp board and about 17 times faster than the ESP32!

# ulisp-arm
A version of the Lisp programming language for boards based on the ARM processor:

* Arduino Due, Zero, and MKRZero.
* Adafruit ItsyBitsy M0, Feather M0, and Gemma M0.
* Adafruit Metro M4, ItsyBitsy M4, Feather M4, and Grand Central M4.
* BBC Micro Bit.
* Maxim MAX32620FTHR.

For more information see: http://www.ulisp.com/
