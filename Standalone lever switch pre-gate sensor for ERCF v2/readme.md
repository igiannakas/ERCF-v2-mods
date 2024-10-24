Stand alone filament sensor using lever switches

A stand alone filament pre-gate sensor that uses lever switches instead of the more typical ball bearings and switch approach.

This sensor can be used with both for the ERCF/Tradrack MMU's using Happy Hare but also as a stand alone filament runout sensor. By using the Omron D2F-L3-D3 switches, the effective actuation range of the switch is increased, resulting reduced false positives happening from filament diameter variation, filament grinding in the ERCF/Extruder gears and reduces wear on the switch itself as the contact is stationary.

This design was inspired and based on the CAD work done by: https://github.com/juliusjj25/ERCF-Pregate-Sensors. The filament path has been tweaked for reduced friction and improved reliability with endless spool in Happy Hare and the design amended to allow for printing without supports.

Benefits when using with Happy Hare and ERCF/Tradrack:
1. The sensor has been specifically designed to allow it to be placed at a distance from the MMU gates. This helps with endless spool reliability as it reduces the likelihood that the filament travels past the MMU gate before Klipper pauses the print.
2. The carefully designed filament path allows for a low friction, low "collision" retraction from the MMU back to your buffer of choice. This reduces the probability of the filament stalling and getting stuck before reaching the buffer.

Print settings:
1. 0.16-0.2mm layer height. 0.16mm recommended. 0.25mm first layer height
2. 4 walls, 0.4mm forced extrusion width
3. Classic wall generator with thin wall detection enabled
4. Thick bridges disabled in your slicer

Images:

