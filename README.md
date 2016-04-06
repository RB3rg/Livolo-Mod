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

Working on......
