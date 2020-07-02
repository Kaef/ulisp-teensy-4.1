# ulisp-3.3-arm
Many thanks to David and the members of the ulisp forum for supporting ulisp.

Kaef, 16.06.2020


# Update, 02.07.2020
I'm very happy that the Teensy-4.0 and the Teensy-4.1 boards are now supported by uLisp-3.3a.

Therefore, I will not continue investing in this fork of uLisp, it has done what it was made for:
showing, that uLisp runs very well on the Teensy-4.0 / 4.1 platforms.

Of cause I will continue supporting uLisp. I think this is a great project and I always have fun using it.

If you like to use uLisp on Teensy-4.1 please use the version found at http://www.ulisp.com/ .


# Note for Teensy-4.1 board support
This is a fork of ulisp-3.3-arm with added support for Teensy-4.1 board.
The board is made by pjrc, please see documentation at their webpage.

Not many changes were needed to run ulisp-3.3-arm on the Teensy-4.1 board.
I add a comment to all code changes using "// Kaef" and/or "Teensy-4.1" comments
to make it easy finding my changes.
I include the (almost) original version of ulisp-3.3-arm (named "ulisp-arm.ino.org")
so you can create a diff to see all changes I made.

I did not test this version with any other supported arm processor boards, so it
may have problems using this version with one of these boards.
For all other arm processor boards already supported by ulisp I strongly recommend using David's original version of ulisp-3.3-arm.

## Motivation
This is an additional 'proof of concept' I made with ulisp-2.8-arm for the Teensy-4.0 board.

This version of ulisp-3.3-arm is able to use the on-board sd-card socket of the Teensy-4.1 board to store uLisp-Images
and other Files (i.e. uLisp code files) on the sd-card.
Not all functions are tested yet on the Teensy-4.1 board, just some
basic ulisp code was used (tak, q), i2c, spi, analog-read/-write are not tested yet.

I added four functions to ulisp to use the sd-card more confortable:
(ls), (rm "file-name"), (mkdir "dir-name") and (rmdir "dir-name").
There are also functions written in ulisp to load, save and cat out (ulisp-) files
from/to the sd-card. You'll find these functions in the lisp-library.

All functions are described in the file 'documentation/reference-sd-card-functions.md'.

Teensy-4.1 uses the same ARM cortex M7 processor as the Teensy-4.0 boards, so I
*think* this version of ulisp could also be used with the Teensy-4.0 boards, but
I haven't tested it.

## iMXRT1062 basic features (for details look at pjrc page)
* ARM cortex M7 processor at 600 MHz with a NXP iMXRT1062 chip
* 1024k RAM, 2048k flash
* USB, CAN, I2S, SPI, I2C, ADC, RTC, FP unit and much more
* needs ~0.5 seconds for the (tak 18 12 6) benchmark,
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
