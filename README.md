ST7735 FrameBuffer for Raspberry Pi
===================================

The ST7735 is a single-chip controller/driver for 262K-color, graphic type 
TFT-LCD, which can be picked up on eBay relatively cheaply with pin-outs on
a break-out board.

![1.8" 160x128 pixel TFT-LCD](http://www.adafruit.com/adablog/wp-content/uploads/2011/12/window-57.jpg)

Originally based on code from https://github.com/ohporter/linux-am33x/tree/st7735fb

Further technical details for the LCD screen can be found in the 
[datasheet](https://raw.github.com/rm-hull/st7735-fb/master/doc/tech-spec/datasheet.pdf) [PDF]. Tested working
with Rev B 512Mb Rasberry Pi (Raspbian "Wheezy" & latest [RPi-Firmware](https://github.com/Hexxeh/rpi-update))

Pre-requisites
--------------
- to do

This kernel module also requires the SPI module from https://github.com/bootc/linux/tree/rpi-i2cspi; 
however in recent kernel versions (e.g. 3.6.11), the SPI modules should be already pre-built 

Building and installing the frame buffer driver
-----------------------------------------------
- to do

Once compiled, installed and inserted, you should get a second frame buffer at `/dev/fb1`.

Pin-outs
--------
There appear to be a large number of break-out boards for this device; this one works for me:

| Pin | Name    | Description              |
|----:|:--------|:-------------------------|
| 1   | GND     | 0V                       |
| 2   | VCC     | 3V3                      |
| 3   | NC      |                          |
| 4   | NC      |                          |
| 5   | NC      |                          |
| 6   | RESET   | Set low to reset         |
| 6   | A0      | SPI data/command         |
| 7   | SDA     | SPI data                 |
| 8   | SCK     | SPI clock                |
| 9   | CS      | Chip select - set low    |
| 10  | SD-SCK  | SD serial clock          |
| 11  | SD-MISO | SD master in, slave out  |
| 12  | SD-MOSI | SD master out, slave in  |
| 13  | SD-CS   | SD chip select           |
| 14  | LED+    |   aligned                |
| 15  | LED-    |   aligned                |

Wiring Schematic
----------------
- to do

Stripboard Layout
-----------------
- to do

TODO
----
* Extended documentation

* Improve build instructions

* Schematics & stripboard wiring

* Example code (SDL / Python)

References
----------
* http://www.sitronix.com.tw/sitronix/product.nsf/Doc/ST7735?OpenDocument

* http://learn.adafruit.com/1-8-tft-display

* http://www.raspberrypi.org/phpBB3/viewtopic.php?t=28696&p=262909

* https://github.com/ohporter/linux-am33x/tree/st7735fb

* http://elinux.org/images/1/19/Passing_Time_With_SPI_Framebuffer_Driver.pdf

* https://github.com/ngreatorex/st7735fb 

* http://www.flickr.com/photos/ngreatorex/7672743302/

* http://fritzing.org
