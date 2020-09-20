
Compact amplifier
=================

This amplifier is intended to be used as a small desktop amplifier. It has no
fancy stuff. It does not even have a volume knob.

It has a short-circuit protection and all the necessary filtering on the inputs
and outputs.

The input is single-ended. 

Architecture
------------

The amplifier consists of the following boards:
 - Amplifier boards (left and right channels)
 - Power supply and control board with mute and LED indication.
 - Input/output board with speaker protection and necessary input and output
   filtering.
   
![Image of Architecture](https://github.com/nradulovic/hw_harmonious/raw/master/Board%20overview.png)

The complete model of the amplifier case layout is based on Dayens Ampino power 
amplifier.

Amplifier board (AMP)
=====================

Description
-----------

The board contains one amplifier with short-circuit proction.

Dimensions
----------

Max width: 80mm
Max height: 100mm

Connections
-----------

* Power Supply Input - PSI: Vcc, GND, Vee
* Speaker Output - SPO: Out, GND
* Signal Input - SGI: In, SGND


Power supply and control board (PSC)
====================================

Description
-----------

* Provides power supply.
* Provides turn-on delay for muting relay on input/output board.
* Provides control of mute relay (mute control)

Dimensions
----------

Max width: 140mm
Max height: 100mm

Connections
-----------

* AC Voltage input - ACI: Live, Neutral, Earth
* Power Switch - PSW: CN1, CN2
* Transformer Primary - TRP: Live, Neutral, Earth
* Transformer Secondary - TRS: AC1, GND, AC2
* Power Supply output 1 - PS1: Vcc, GND, Vee
* Power Supply output 2 - PS2: Vcc, GND, Vee
* Power Supply output 3 - PS3: Vcc, GND, Vee
* Speaker delay and mute control - SDM: speaker-on, GND
* LED indicator (POWER, MUTE) - LI: Anode, Cathode.
* Mute key - MK: K1, K2.

Input/output filtering and Interface board (IOI)
================================================

Description
-----------

* Provides necessary input and output filtering
* Provides speaker protection against DC voltage
* Provides MUTE functionality controlled by Power Supply and Control Board

Connections
-----------

* Speaker delay and mute control - SDM: speaker-on, GND
* Input cinch connectors - ICL: Left,GND
* Input cinch connectors - ICR: Right,GND
* Output terminal connectors - OTL: Left,GND
* Output terminal connectors - OTR: Right,GND
* Power Supply Input - PSI: Vcc, GND, Vee
* AMP Output - AOL: LeftA,GND
* AMP Output - AOR: RightA,GND
* AMP Input - AIL: LeftA,GND
* AMP Input - AIR: RightA,GND
