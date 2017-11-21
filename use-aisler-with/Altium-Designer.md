<!-- --- title: Using Altium Design with AISLER -->
# Using Altium Designer with AISLER
To use AISLER with Altium Designer you will need to export your project as a Gerber-Package. Please make sure you zip your Gerber-Files. 

### Most important design rules to use with Altium Designer ###
Use these design rules to get optimal results with AISLER's production. 

- Min. trace width: 100 μm
- Min. trace spacing: 100 μm
- Min. pitch between traces: 140 μm
- Spacing PCB edge to trace: 200 μm
- Spacing via to via: 0.30 mm
- Spacing drill to drill: 0.15 mm
- Min. drill diameter for vias: 0.2 mm
- Min. via pad diameter: Via drill + 0.25 mm
- Min. stroke width of legend print: 100 μm

### Exporting Gerber Files with Altium Designer ###
To properly export Gerber Files with Altium for use with AISLER, you will have to setup your NC Drill files and your Gerber setup as displayed in the screenshots below:

#### NC Drill Setup ####

Please navigate to **File » Fabrication Outputs » NC Drill Files** to setup NC Drill Files.

![Select Inches and 2:4 Format, Keep leading zeroes, reference to relative origin, Optimize change location commands, and Generate separate NC Drill files for plated and non-plated holes](/use-aisler-with/Altium-Designer/assets/nc_drill_setup.png)

#### Gerber Setup Dialog ####

Please navigate to **File » Fabrication Outputs » Gerber Files** to setup Gerber Export.


**Setup General:**

![Select inches and 2:4 format in General tab](/use-aisler-with/Altium-Designer/assets/gerber_setup_general.png)


**Setup Layers:**

![Only select Top and Bottom Overlay, Paste, Layer and Overlay, and Mechanical 1 in Setup Layer Tab](/use-aisler-with/Altium-Designer/assets/gerber_setup_layers.png)


**Setup Drill Drawing:**

![Deselect all options in Drill Drawing tab](/use-aisler-with/Altium-Designer/assets/gerber_setup_drill_drawing.png)


**Setup apertures:**

![Select Embedded apertures (RX274X)](/use-aisler-with/Altium-Designer/assets/gerber_setup_apertures.png)


**Setup advanced:**

![Select Separate File per Layer in Batch Mode, Suppress leading zeroes in Leading/Trailing zeroes, Reference to relative origin in Position on Film, unsorted (raster) in Plotter type in Advance Tab. Also select Optimize change location commands.](/use-aisler-with/Altium-Designer/assets/gerber_setup_advanced.png)

*Note:* In this screen the Film size and Aperture Matching Tolerances are project specific, so please add the project's relevant settings here.


<table>
<tr><th>Gerber Layer Name</th><th>Layer</th></tr>
<tr> <td>project_name.toplayer.ger</td><td>Top Layer</td> </tr>
<tr> <td>project_name.bottomlayer.ger</td><td>Bottom Layer</td> </tr>
<tr> <td>project_name.topsoldermask.ger</td><td>Top Soldermask</td> </tr>
<tr> <td>project_name.bottomsoldermask.ger</td><td>Bottom Soldermask</td> </tr>
<tr> <td>project_name.topsilkscreen.ger</td><td>Top Silkscreen</td> </tr>
<tr> <td>project_name.bottomsilkscreen.ger</td><td>Bottom Silkscreen</td> </tr>
<tr> <td>project_name.boardoutline.ger</td><td>Board Outline</td> </tr>
<tr> <td>project_name.xln</td><td>PTH Drills</td> </tr>
<tr> <td>project_name_npth.xln</td><td>NPTH Holes</td> </tr>
</table>

**Please note:** Altium is known to generate a lot of other stuff in the output files, please ensure to only include the ones relevant and named above, otherwise our import will get confused. If you have sanitized the output files, upload them as a zip file. 

### Steps to upload your project to AISLER ###

1. Navigate to [Start new project](https://go.aisler.net/p/new "Start new Project")
2. Upload your Gerber zip-file (*.zip)
3. Give your Project a nice name
4. (optional) order a copy of your board

### Steps to document your Bill-of-Materials
There are two ways to document your bill-of-materials

1. Navigate to the project you want to document 
2. Click the 'Edit' button under the Bill-of-Materials section
3. Click 'Manually add part' and assign a part
4. Repeat until you have everything documented
