# Bike_generator_controlled_DMX
System to monitor the power output of a bicycle generator (or any other DC source) and control light fixtures using the DMX protocol

The system is designed to illustrate that batteries allow you to run more powerful loads than your generator is able to power. 
A (fictional) battery can be switched in and out and a large (fictional) load - some bright lights -  can be switched in and out.
The effect is that it's hard/impossible to power the bright lights directly but it's easy to charge the battery and then run the light (for a much shorted ammount of time)

The user can switch between putting power into a (relatively easy) dump load - a heat-sunk power resistor - or short circuiting the DC input which simulates a the big load - this switching is done using 40A automotive relays.

The current is recorded using a 50A allegro current sensor and used to control the brightness of the first 4 channels of a DMX512 universe. 

The DMX is done using a MAX485 "TTL to RS485" module with the output enable pin held low.  

It also outputs a pattern over a string of neopixels to represent the "state of charge" of a fictional battery that has been charged up and then is discharged by running the DMX lights (at full brightness)


Info on current sensor: 

https://www.allegromicro.com/en/Products/Current-Sensor-ICs/Zero-To-Fifty-Amp-Integrated-Conductor-Sensor-ICs.aspx
