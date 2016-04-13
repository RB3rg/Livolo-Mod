# Livolo-Mod

What is it?
-----------

LIVOLO-Mod is a custom firmware for LIVOLO light switch

Why a custom firmware?
----------------------

Livolo is a really nice switch for a modern house, it's touch, nice look and electronic made. It's great for a Smarthome project however it doesn't come with an interface for external device to be remote controlled and have its status updated. 

There is a RF remote version that could make it partially useful in such way you can send code to turn it on/off but, how to know the status if someone turn the light on touching the switch? You won't.

The Solution
----------------

LIVOLO switch uses a PIC 16F690, this PIC has built in UART serial, We ca use this feature to communicate with other device.

The Modification
---------------------

One of the great things in the LIVOLO switch is the ability to use the AC current to supply the power (3VDC) for the PIC.
With this mod you will lose this feature and LIVOLO must be powered from external 5VDC supply.** We might change this in the future, for now, yes it needs 5VDC supply.

It sounds a big deal to bring an external DC power cable, but don't forget we are doing this mod to have a Serial line to communicate with other device so You HAVE to bring up 3 wires to the Livolo (TX,RX, GND) then it's not a big deal to bring one more wire (+5V). I use at my home a phone cable with RJ11. 

The Mod consist in:
  - Isolate the AC power from the electronic circuit;
  - Save the custom firmware in the PIC;
  - Change the internal relays, it comes with 12VDC relay, we need 5VDC to make things simple (unless you want to keep the       12V relay and drop the voltage with a regulator);
  - Solder a whip with 4 wires and Connector(+5V, TX, RX, GND). I'm using a RJ11 female, it works very well.

What you need:
  - To program the PIC: Microchip’s PICkit™ 3 or any other programmer;
  - Soldering iron and knowledge to use it;
  - 5VDC relay model: 005-HS3(555), google it.
  - Not necessary but Recommended to extend the range for the Serial comms: A pair of MAX3232 module, google it. 
  - If you want to work in the source code, you will need a PICBasic compiler (PICBASIC PRO™), plans to switch to C              compiler.

How to Do it?
-------------
	See file docs/howto.html (working on... coming soon)

Authors
----------
	Doug Schafer
	Rhaurison Bergamin

Contributors
---------------
	

License
----------
	Mozilla Public License Version 2.0 – See License file.
