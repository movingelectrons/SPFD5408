#SPFD5408 Library specifically for MEGA boards ONLY
	Origional Author: Joao Lopes
	Modified by: Jerome Stonebridge

This library is the Adafruit TFT Libraries changed to works in TFT 2.4 shields with the SPFD5408 controller.
Tested on Mega.

It is based in the last version of Adafruit, inclusive with buttons features.

The TFT 2.4 is cheap TFT, that generally is from China, 
without documentation or libraries for it.

When we try to use the TFT 2.4 with SPFD5408 controller in sketches with Adafruit TFT libraries,

DISCLAIMER:

This Library is NOT provided by AdaFruit and they have not
endorsed it. This library is just a lot of modifications in the Adafruit Library,
to works in TFT with SPFD5408 controller (cheap shields)

ATTENTION: 

I test with success in my aliexpress TFTs, and Mega Arduino boards.

Also please send me feedback, problems or suggestions.

INSTALATION:

Download zip then you access the Arduinos IDE menu : sketch/add library, add .zip

Restart the IDE

If you download any code that uses Adafruit Libraries, please verify it:

-  Pinout XM XP, must be:
	\#define YP A1  // must be an analog pin, use "An" notation!
	\#define XM A2  // must be an analog pin, use "An" notation!
	\#define YM 7   // can be a digital pin
	\#define XP 6   // can be a digital pin
	(please verify it, if only a blank screen or noise is showed or touch doesnt works)

- tft.begin: insert after block commented
	tft.begin(0x9341); // SDFP5408

- Calibrate before run 

	Exists one sketch written for my, to help in calibration of touch
	See it in examples folder
	Run it and change this parameters:

	#define TS_MINX 150
	#define TS_MINY 120
	#define TS_MAXX 920
	#define TS_MAXY 940
	
	(please verify it if the point of touch is not accurate)

  
--------------------------------

Examples:
	
	spfd5408_calibrate

		Help the calibration of touch (resistive)

	spfd5408_tftpaint

		example of Adafruit changed to work with the SPFD5408

	spfd5408_graphictest

		example of Adafruit changed to work with the SPFD5408

	spfd5408_rotationtest

		example of Adafruit changed to work with the SPFD5408

