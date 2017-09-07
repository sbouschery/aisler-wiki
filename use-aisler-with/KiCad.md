<!-- --- title: Using KiCad with AISLER -->
# Using KiCad with AISLER
We allow you to directly import your .kicad_pcb and .sch files into AISLER. We support KiCad Versions 3, 4 and all nightly builds natively. 

### Most important design rules to use with KiCad
- Min. trace width: 100 μm
- Min. trace spacing: 100 μm
- Min. pitch between traces: 140 μm
- Spacing PCB edge to trace: 200 μm
- Spacing via to via: 0.30 mm
- Spacing drill to drill: 0.15 mm
- Min. drill diameter for vias: 0.2 mm
- Min. via pad diameter: Via drill + 0.25 mm
- Min. stroke width of legend print: 100 μm


### Steps to upload your project to AISLER

1. Navigate to [Start new project](https://go.aisler.net/p/new "Start new Project")
2. Upload your Board (*.kicad_pcb)
3. Give your Project a nice name
4. (optional) order a copy of your board

### Steps to document your Bill-of-Materials
There are two ways to document your bill-of-materials

1. Navigate to the project you want to document 
2. Upload a schematic (*.sch)
3. All of your parts should appear in the Bill-Of-Materials
4. Click the Edit Button and Assign parts

The second option is to document the parts manually

1. Navigate to the project you want to document 
2. Click the 'Edit' button under the Bill-of-Materials section
3. Click 'Manually add part' and assign a part
4. Repeat until you have everything documented
