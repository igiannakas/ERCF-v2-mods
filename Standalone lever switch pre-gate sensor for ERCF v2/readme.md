# Standalone Filament Sensor Using Lever Switches

A standalone filament pre-gate sensor that uses lever switches instead of the more typical ball bearings and switch approach.

This sensor can be used both for the ERCF/Tradrack MMUs using Happy Hare, as well as a standalone filament runout sensor. By using the Omron D2F-L3-D3 switches, the effective actuation range of the switch is increased. This results in reduced false positives caused by filament diameter variation, filament grinding in the ERCF/Extruder gears, and also reduces wear on the switch itself as the contact is stationary.

## Design Inspiration
This design was inspired by and based on the CAD work done by [Juliusjj25](https://github.com/juliusjj25/ERCF-Pregate-Sensors). The filament path has been optimized for reduced friction and improved reliability with the endless spool in Happy Hare. Additionally, the design has been amended to allow for printing without supports.

## Benefits of Using with Happy Hare and ERCF/Tradrack

1. **Improved Endless Spool Reliability**: The sensor is designed to be placed at a distance from the MMU gates. This helps improve endless spool reliability by reducing the likelihood that the filament travels past the MMU gate before Klipper pauses the print.
   
2. **Optimized Filament Path**: The carefully designed filament path allows for low friction and low "collision" retraction from the MMU back to your buffer of choice. This reduces the probability of filament stalling and getting stuck before reaching the buffer.

## Print Settings

1. **Layer Height**: 0.16-0.2mm layer height (0.16mm recommended), with a 0.25mm first layer height.
2. **Walls**: 4 walls, with a 0.4mm forced extrusion width.
3. **Wall Generation**: Use classic wall generator with thin wall detection enabled.
4. **Bridges**: Ensure thick bridges are disabled in your slicer.

## Images

![Screenshot 2024-10-24 at 13 57 57](https://github.com/user-attachments/assets/507c8fd9-7792-4fab-a567-e7e5adab493b)

**Filament path is right to left.**
![Screenshot 2024-10-24 at 13 58 23](https://github.com/user-attachments/assets/8da40195-634e-4c02-842d-6898f07d21f8)

![Screenshot 2024-10-24 at 14 01 01](https://github.com/user-attachments/assets/bc9114a0-b743-4bb9-8fc9-481b2cf26509)
