# Lab 1: 5-Bit DAC with PadFrame

## Table of Contents
- [Lab Description](#lab-description)
- [General Schematic](#general-schematic)
- [Technology Description](#technology-description)
- [Pad Cell](#pad-cell)
  - [Pad Schematic](#pad-schematic)
  - [Pad Layout](#pad-layout)
- [Pad Frame](#pad-frame)
  - [Pad Frame Schematic](#pad-frame-schematic)
  - [Pad Frame Layout](#pad-frame-layout)
- [Final IC](#final-ic)
  - [Final IC Schematic](#final-ic-schematic)
  - [Final IC Layout](#final-ic-layout) 

## Lab Description
The goal with this lab is to design a die in order to connect the 5-Bit-DAC to the outside
world.

## General Schematic
The DAC from the last lab needs pads in order to acces outside connections. For 5 bits only 7 pad are needed.

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab2/images/genral_sch.png)

## Technology Description
Using a die size of 1.5mm and a technology of 300nm. The pad cells, bonding pads, and overgalss sizes are calculated.

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab2/images/technology.jpg)

## Pad Cell
First we need to desing one pad cell.

### Pad Schematic
Begin by creating a schematic for the pad. The export will be called inout. Create a icon for the schematic aswell.

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab2/images/pad_sch.png)

### Pad Layout
Next create the layout. Make sure the sizes match the calculated sizes.

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab2/images/pad_lay.png)

## Pad Frame
Now a pad frame will be created. 

### Pad Frame Schematic
For the pad frame schematic drag in the pad icon and name it "pad[1:8]". Connect an export called "pin[1:8]" with a bus to the icon.
Create an icon from the schematic.

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab2/images/padframe_sch.png)

### Pad Frame Layout
To create the pad frame layout, drag in a pad layout and use the array tool to create a 4 by 4 grid.
Delete the corners, and middle pads. Name the pads "pad[#]" using an export.

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab2/images/padframe_lay.png)

## Final IC
For the Final IC you will need the 5-Bit-DAC schematic form last lab. Change the export of the pins to match the names of the padframe. Exclude pin[3]. since only 7
pad are needed.

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab2/images/DAC_sch.png)

### Final IC Schematic
Drag in the 5-Bit-DAC and padframe icons into the Final IC schematic.

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab2/images/final_ic_sch.png)

### Final IC Layout
For the layout drag in the 5-Bit-DAC and padframe layouts. Wire the DAC to the pads.

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab2/images/final_ic_lay.png)


