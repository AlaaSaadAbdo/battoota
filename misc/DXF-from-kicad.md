# How to generate a DXF from kicad to use in Fusion 360

I will be using [Qeshda](../boards/34keys/Qeshda/Qeshda/) as an example to generate a DXF for.  
![PCB](./images/initial_pcb.png)

1. Make a footprint with the dimentions you need. I have a footprint for Choc and MX. The footprint has an edge cut for the switch 14x14 and a user drawing for the keycap 20x20 or 18x19 
   ![footprint](./images/footprint.png)
2. Replace all the switch footprints in pcbnew with the desired footprints 
   ![mass_replace](./images/mass_replace.png)
3. You'll end up with a pcb that looks similar to this 
   ![dirty_plate](./images/dirty_plate.png)
4. You can now export the layers you want as an SVG 
   ![svg_export_1](./images/svg_export_1.png)  
   ![svg_export_2](./images/svg_export_2.png) 
5. You can now open the SVG in incape and save the file as a DXF file 
   ![inkscape_1](./images/inkscape_1.png)
   ![inkscape_save](./images/inkscape_save.png)
6. You can now import the DXF into fusion and use it as a sketch to base your design on 
   ![fusion](./images/fusion.png)

## Alternative DXF export via kicad directly

You can always use the Plot (File > Plot) function to plot DXF directly from kicad.  
The catch is that kicad doesn't handle curves well and will end up generating a lot of small lines instead of an arc which makes using the sketch very slow.
![dxf_from_kicad](plot_dxf)


