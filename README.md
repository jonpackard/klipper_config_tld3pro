# klipper_config
### This is my own config adapted from matti125's Hands 2 config. This is what I use on my Tenlog TL-D3 Pro.

### Notes from matti125:
The repository contains the Klipper configurations for a Tenlog Hands 2 printer. Tenlog tends to change their design without changing the product names, and my Hands 2 has a bed size of 220x220, whereas the more recent ones are 235x235.
The printer itself is upgraded/changed with a few items:
- Printheads replaced with Titan extruders
- Heatblocks changed to Maxiwatt 40W models
- Power supply moved abt 10mm away from the side panel, to improve air circulation
- Thermal insulation added below the heated bed
- VGA cables (going to the printheads) tied to the top horizontal bar (Verrrry important to reduce Z errors caused by cables pulling the heads)
- X-axis optical sensor cables tied to the case, as otherwise the z-axis movement will eventually break the soldering or (as in my case) the sensor
- Z-axis top bushings greased to get rid of the screeching noise with any considerable z-axis movement
- Display removed and replaced with a grill to improve air circulation in the case, which hopefully reduces thermal expansion
- Filement fed directly from a pair of Sunlu filament dryers. Filement feeds over the top bar with a help of "bearing" system built from two empty spools and some support structures.
- The roller guides readjusted to remove slack
- The z axis endstop sensors adjusted such that the x-rail rests equally on both z-rods, i.e. the x-rail is not exposed to torque caused be different z heights on either side
- Yet Anothet Design for using the silicone heat block socks to prevent oozing when the print head is parked.
- A microswitch installed as a bed mesh measuring probe. The probe needs to be manually moved/turned into its measuring position.  The sensor uses the pin that used to be used for filament rounout detection, so the lack of filament runout sensor is a downside of this design.

With Klipper, Input Shaping, Pressure Advance and Bed Mesh the Tenlog is now quite reliable. The max speeds are now mostly limited by the hotend melting capacity, I am not able to go much beyond 12mm3/s or 150mm/s for a 0.4 nozzle with PLA.

The board on Tenlog Hands2 has an ATMega2560 chip. The file klipper/.config has the selections made with `make menuconfig`, but you do not need that file to run klipper: the `make menuconfig` will generate the file for you (in the correct place, i.e. ~/klipper/.config), so it is included here just for reference.
