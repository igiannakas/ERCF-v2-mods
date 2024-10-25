# Standalone Filament Sensor Using Lever Switches

A standalone filament pre-gate sensor that uses lever switches instead of the more typical ball bearings and switch approach.

This sensor can be used both for the ERCF/Tradrack MMUs using Happy Hare, as well as a standalone filament runout sensor. By using the Omron D2F-L3-D3 switches, the effective actuation range of the switch is increased. This results in reduced false positives caused by filament diameter variation, filament grinding in the ERCF/Extruder gears, and also reduces wear on the switch itself as the contact is stationary.

## Design Inspiration
This design was inspired by and based on the CAD work done by [Juliusjj25](https://github.com/juliusjj25/ERCF-Pregate-Sensors). The filament path has been optimized for reduced friction and improved reliability with the endless spool in Happy Hare. Additionally, the design has been amended to allow for printing without supports.

## Benefits of Using with Happy Hare and ERCF/Tradrack

1. **Improved Endless Spool Reliability**: The sensor is designed to be placed at a distance from the MMU gates. This helps improve endless spool reliability by reducing the likelihood that the filament travels past the MMU gate before Klipper pauses the print.
2. **Optimized Filament Path**: The carefully designed filament path allows for low friction and low "collision" retraction from the MMU back to your buffer of choice. This reduces the probability of filament stalling and getting stuck before reaching the buffer.
3. **Improved integration with the Filamentalist buffer**, allowing for more reliable endless spool and flexible placement of the sensor and filamentalist.

## Print Settings

1. **Layer Height**: 0.16-0.2mm layer height (0.16mm recommended), with a 0.25mm first layer height.
2. **Walls**: 4 walls, with a 0.4mm forced extrusion width.
3. **Wall Generation**: Use classic wall generator with thin wall detection enabled.
4. **Wall Odering:** Inner - Outer only. Outer-inner (External perimeter first) and Inner-Outer-Inner **will not** provide the level of overhang quality needed to print the model with the right tolerances. If using Orca slicer, enable the Precise Wall option for better surface finish. 
5. **Bridges**: Ensure thick bridges are disabled in your slicer.
6. **Infill:** 40%, gyroid.
7. **Top and Bottom surfaces:** 5 (when using 0.16 LH), or 4 (when using 0.2 LH)
8. **Print in ABS or ASA** - model has been designed to account for material shrinkage, so please disable shrinkage compensation in the slicer.
9. **Make sure your filament flow rate is calibrated correctly.** The part requires a well calibrated printer to deliver the required tolerances for reliable operation. If in doubt, prit the ERCF / Voron calibration tests.

## BOM
Per sensor:
| **Item**                            | **Quantity**         | **Sourcing**                                                                                               |
|-------------------------------------|----------------------|------------------------------------------------------------------------------------------------------------|
| Omron D2F-L3-D3 switch              | 1 per sensor         | [Digikey](https://www.digikey.co.uk/en/products/detail/omron-electronics-inc-emc-div/D2F-L3-D3/6071977) / [Mouser](https://www.mouser.co.uk/ProductDetail/Omron-Electronics/D2F-L3-D3?qs=i1w9Bv2NFd0l%252B7zEPgxolg%3D%3D) / [Farnell](https://uk.farnell.com/omron/d2f-l3-d3/microswitch-spdt-3a-125vac-80gf/dp/3460475) |
| M2x6 or 8mm Self-Tapping screws     | 2 per sensor         | Amazon, Aliexpress, included in the ERCF kit                                                                                   |
| Ziptie                              | 1 per sensor         | Amazon, Aliexpress                                                                                 |
| 22AWG silicone cable                | As needed            | Amazon, Aliexpress, included in the ERCF kit                                                                                |
| Heatshrink tubing (optional)        | As needed            | Amazon, Aliexpress, Hardware stores                                                                                |
| Soldering iron & solder             | As needed          | Amazon, Aliexpress, Hardware stores                                                                                |
| ECAS fittings             | 2 per sensor          | Amazon, Aliexpress, Hardware stores                                                                                |

## Assembly tips
1. Make sure your bridges have printed cleanly, so the switch slides in the housing without any force. If your bridges are not "clean" you may end up depressing the level switch at installation!
2. Position the switch and set the two screws. Dont screw them in fully as you may need to slightly adjust the switch position below.
3. Taking turns, screw one screw a bit at a time till both are tight. If the switch clicks, back the screw out a bit and reposition the switch slightly so it is secure without it being activated!
4. Place the ecas fittings and solder the wires to the switches as per your MMU's instructions.
5. Run a fragment of filament through by hand to clear out and loosen thr filament path.

**IMPORTANT:** The sensor is directional! The arrows must point to the filament path direction - i.e. pointing towards your MMU/printer. While the sensor can be installed in reverse, its performance will be sub optimal as the filament path drag has been optimised to enable smooth filament re-wind when performing endless spool operations.

If you're using this as a stand alone filament sensor install it flipped so the arrows point to your filament spool and not the printer. This will make filament loading easier since automated endlews spool operation is not needed in that case.

**IMPORTANT:** When loading your MMU make sure the end of the filament is straight - this will help the filament ease through the sensor without it catching.

## Images
![image](https://github.com/user-attachments/assets/663353b0-848a-48ab-8baf-64ccd3c2d612)
![image](https://github.com/user-attachments/assets/40528144-d372-4c17-aae7-4c8dc8b981d7)
![IMG_4764](https://github.com/user-attachments/assets/5445c45a-4c29-48b3-8b34-6efb6d59fb14)
![IMG_4765](https://github.com/user-attachments/assets/bf8ff659-4ab3-4ba1-bb87-c28252ebd128)
![IMG_4770](https://github.com/user-attachments/assets/ad9b905e-0ab4-4336-8e66-c246596be65c)


**Please note the sensor is directional. The arrows must point towards the MMU / printer.** 

**In the image below the filament path is right to left**

**MMU on the left** - **Buffer on the right**
![image](https://github.com/user-attachments/assets/5d4f4fe8-3db2-4e3f-aa86-e33346bbaf78)
Notice the smooth entry when the filament is pushed back into the buffer.


**Print without supports. Holes are supported internally.**
![image](https://github.com/user-attachments/assets/bf6911ec-0818-4278-aac5-82e57f537b78)
![image](https://github.com/user-attachments/assets/b547bf06-97c1-4813-b0c9-f0d8f3700148)
![image](https://github.com/user-attachments/assets/8722af79-81c0-419e-b5c2-1008977f9646)
![image](https://github.com/user-attachments/assets/89cb71cf-327e-45c3-87ff-d1bf9207fd4a)


