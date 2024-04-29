ERCF V2 RC2 mods list

While building and setting up my ERCF v2 kit I stumbled upon a few improvements in the available component designs that are aiming to improve multi material printing reliability.

This repo is an archive of my mods. 

**Galileo 2 Extruder - Twinsor smoothed filament entry:** Smooths out the G2E filament path entry to improve extruder feeding reliability when using a 3mm ID/4mm OD reverse Bowden tube

**Pre-gate sensors ERCF V2 RC2:** This is a mod that integrates the ERCT pre-gate sensors into the main filament path, to enable the use of alternative filament buffers while also retaining the pre-gate sensor functionality (better endless spool detection and operation)

**Filament slot buffer for 1.4m buffered filament:** I've tried a few buffer solutions (ERCT, PIKA) but neither worked well for my use case. I needed to buffer around 1.4-1.5m worth of filament and PIKA struggled with tangles on the wheel while the ERCT was a pain to load and also created tangles from escaping filament. This mod is adding an extension to the slot buffer by Char so it can buffer a longer filament length (up to 1.4-1.5m) and also uses the excellent magnetic ECAS couplers from the PIKA buffer.


